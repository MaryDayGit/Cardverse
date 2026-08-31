# 13 — API Integration

## Architecture

External API
→ scheduled ingestion
→ normalization
→ rights review
→ canonical database
→ card catalog
→ game engine

Never:

Browser → API → pack opening.

## RAWG

Primary Games source.

Useful data includes:

- games;
- genres;
- platforms;
- ratings;
- Metacritic;
- release dates;
- developers;
- publishers;
- franchises;
- screenshots;
- background images.

Reference:
https://rawg.io/apidocs

Verify current terms:
https://rawg.io/tos_api

## IGDB

Potential secondary/future Games provider.

Reference:
https://api-docs.igdb.com/

Requires authentication and backend/proxy architecture.

## Jikan

Primary Anime source for MVP.

Useful data:

- anime;
- characters;
- people;
- studios;
- genres;
- images;
- relationships.

Reference:
https://docs.jikan.moe/

Jikan is unofficial. Review upstream conditions and image rights before production.

## AniList

Potential future/secondary anime source.

Reference:
https://docs.anilist.co/

Terms:
https://docs.anilist.co/guide/terms-of-use

Review bulk-data and service restrictions before using it as an ingestion source.

## Ingestion behavior

- paginate;
- cache;
- retry with backoff;
- store hashes;
- process incrementally;
- never block gameplay on provider uptime.

## Provider abstraction

ContentProvider:

- search
- fetch
- fetchImages
- fetchRelationships
- normalize
- attribution
- rights metadata

Implement:

- RawgProvider
- JikanProvider

Future:

- IgdbProvider
- AniListProvider
- MovieProvider
- BookProvider
- MusicProvider

## Source failure

Existing cards remain playable.

If provider is unavailable:

- no impact on Pack opening;
- ingestion waits/retries;
- existing catalog remains authoritative.
