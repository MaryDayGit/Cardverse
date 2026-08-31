# 12 — Content Model

## Canonical content

Core fields:

- id
- universe
- content_type
- title
- subtitle
- description
- release_date
- rating
- popularity
- legacy_score
- uniqueness_score
- status
- external_sources
- media_assets
- relationships
- rights_metadata

## External source

- provider
- provider_id
- source_url
- fetched_at
- source_hash
- attribution
- rights_status
- active

Unique:

(provider, provider_id)

## Media asset

- id
- content_id
- provider
- source_url
- local_url
- width
- height
- mime_type
- crop_strategy
- rights_status
- attribution
- checksum

## Game-specific relationships

Game → Developer
Game → Publisher
Game → Franchise
Game → Platform

## Anime relationships

Anime → Character
Anime → Studio
Anime → Creator
Anime → Franchise

## Content lifecycle

discovered → normalized → reviewed → approved → active → hidden/retired

Only approved content enters standard pools.

## Important separation

Source facts and CARDVERSE design metadata must remain separate.

For example:

RAWG rating ≠ CARDVERSE rarity.

Jikan popularity ≠ CARDVERSE rarity.
