# 19 — Security

## MVP

Local saves can be edited.

Therefore local mode is not authoritative for competitive claims.

## Online

Server authority for:

- Coins;
- Essence;
- Tickets;
- cards;
- Packs;
- upgrades;
- achievements;
- events;
- idle claims.

## Client cannot submit trusted state

Never trust client values for:

- rarity;
- card ownership;
- pack results;
- currencies;
- quest completion.

## Anti-abuse

- rate limiting;
- idempotency;
- transaction logs;
- validation;
- replay protection;
- race-condition protection.

## Secrets

Provider API keys must remain server-side.

Never ship privileged keys in the frontend.
