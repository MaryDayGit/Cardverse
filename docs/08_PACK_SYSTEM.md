# 08 — Pack System

## Pack types

### Beginner Discovery Pack
One-time onboarding pack.

### Discovery Pack
General Games + Anime pool.

### Game Pack
Games only.

### Anime Pack
Anime only.

### Set Pack
Targets a selected Set.

### Event Pack
Limited-time pool.

## Pack acquisition

Players obtain Packs through:

- starter rewards;
- Coins;
- Pack Tickets;
- quests;
- achievements;
- collection milestones;
- set completion;
- events;
- level-ups.

## Pack purchase rule

Only in-game Coins/Tickets are used in MVP.

No real-money randomized Packs.

## Pack generation

Inputs:

- player state;
- pack type;
- active set/event;
- rarity config;
- pity state if enabled;
- card pool.

Outputs:

- cards;
- rarity;
- variant;
- duplicate status.

## Duplicate weighting

Duplicates are allowed.

Optional future soft duplicate protection can slightly favor missing cards in targeted Sets.

## Pity

Future optional system:

If a player has gone many Packs without Epic+, temporarily increase Epic+ chance.

Must be deterministic, testable and independent of money.

## Pack UX

1. Choose Pack.
2. See price/reward.
3. Open.
4. Reveal cards.
5. Highlight first-time cards.
6. Highlight rare cards.
7. Show duplicates.
8. Offer Essence conversion.
9. Update Set progress.
10. Show next available goal.
