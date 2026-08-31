# CARDVERSE

CARDVERSE is a browser-first idle collection game about collecting cards representing video games, anime, characters, creators, studios and franchises.

The core loop is:

**Click / Idle Income → Coins → Packs → Cards → Collection → Sets → Idle Income → More Packs**

The player does not fight with cards. **PvP is explicitly excluded.**

## Current product decisions

- Browser-first.
- itch.io first.
- Mobile/native port may come later.
- MVP: Games + Anime.
- Offline-first prototype using local persistence.
- Cloud accounts and cross-device synchronization are planned later.
- No paid packs in MVP.
- No premium currency in MVP.
- Optional donations/support only.
- No PvP.
- Trading may be added later, but is not MVP.
- Social features: profiles, achievements, collection showcases, leaderboards/collection comparison.
- RAWG is the primary game content provider.
- Jikan is the primary anime provider for the MVP.
- APIs are ingestion/content sources, never the runtime authority for pack openings.
- Rarity belongs to CARDVERSE's Rarity Engine.
- Completed sets produce passive idle income.
- Duplicates produce Essence and can be used for upgrades.
- Seasons/events are data-driven.
- Future universes must use the same provider/content abstraction.

## First-session promise

A new player must get into the main loop immediately:

START → free Discovery Pack → open cards → inspect Collection → earn/receive second Pack opportunity → learn clicking → earn Coins → open more Packs → discover duplicates/Essence → discover Sets → complete goals → unlock idle income.

The first 10–15 minutes are guided, but after onboarding the player chooses their own collection goals.

## Critical design principle

The clicker is an **economic engine for the collection game**, not the main fantasy.

Early game:
- clicking is visible and important.

Mid game:
- upgrades and automation increase idle income.

Long game:
- completed sets and collection bonuses become the dominant economic engine.

The player should gradually move from "I click to earn Coins" to "My collection earns Coins while I decide what to collect next."

## External references

Verify current terms before release:

- RAWG: https://rawg.io/apidocs
- RAWG API terms: https://rawg.io/tos_api
- IGDB: https://api-docs.igdb.com/
- Jikan: https://docs.jikan.moe/
- Jikan repository: https://github.com/jikan-me/jikan-rest
- AniList: https://docs.anilist.co/
- AniList terms: https://docs.anilist.co/guide/terms-of-use

Availability of an image through an API is not by itself proof of a redistribution/commercial-use license.
