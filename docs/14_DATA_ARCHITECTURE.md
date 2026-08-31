# 14 — Data Architecture

## Layers

1. External source data
2. Canonical content
3. Card catalog
4. Sets
5. Game economy
6. Player state
7. Live operations
8. Analytics

## Authority

CARDVERSE database is authoritative for:

- cards;
- rarity;
- sets;
- pack configuration;
- ownership;
- Coins;
- Essence;
- Tickets;
- progression;
- events.

External APIs are authoritative only for source facts.

## Offline-first save

MVP can use localStorage/IndexedDB.

Save structure:

{
  schemaVersion,
  player,
  wallet,
  collection,
  upgrades,
  quests,
  achievements,
  settings
}

## Migration

Every save has schemaVersion.

All breaking changes require migrations.

Never silently reset player progress.

## Future online

Client → API → database.

Server becomes authoritative for economy and inventory.

## Local-to-online migration

1. Validate local save.
2. Authenticate.
3. Upload.
4. Validate schema.
5. Resolve conflicts.
6. Create canonical account state.
7. Mark synchronization complete.
