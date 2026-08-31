# 16 — Backend Architecture

## MVP

Prototype can run locally.

All domain logic should already be separated from UI.

## Future backend

- Node.js
- TypeScript
- PostgreSQL
- optional Redis
- scheduled workers
- object storage/CDN

## Services

### Content Service
External ingestion and normalization.

### Card Catalog Service
Cards, variants, Sets.

### Rarity Service
Scoring and rarity assignment.

### Pack Service
Pack generation.

### Economy Service
Coins, Essence, Tickets.

### Idle Service
Click upgrades, passive income, offline income.

### Collection Service
Ownership and completion.

### Progression Service
XP, levels, quests, achievements.

### Live Ops Service
Seasons/events.

### Account Service
Auth/sync.

### Analytics Service
Gameplay events.

## Key endpoints

GET /catalog/sets
GET /catalog/cards/:id
GET /collection
GET /collection/missing
GET /economy
POST /packs/:id/open
POST /cards/:id/upgrade
POST /cards/:id/convert
POST /idle/claim
GET /quests
POST /quests/:id/claim
GET /achievements
GET /profile/:id

## Atomic pack opening

BEGIN
→ validate player
→ validate Pack
→ deduct Coins/Ticket
→ generate results
→ record opening
→ update inventory
→ update quests/achievements
→ commit

## Idempotency

Pack opening, upgrade and currency mutation endpoints require idempotency keys.

## Server authority

Once online:

Client cannot decide:

- Pack result;
- rarity;
- inventory quantity;
- Coin balance;
- Essence balance;
- completed quest.

## Idle authority

Server computes offline earnings from:

- last active timestamp;
- current valid income sources;
- configured cap.

Client only requests claim.
