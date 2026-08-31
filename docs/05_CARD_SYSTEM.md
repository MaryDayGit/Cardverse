# 05 — Card System

## Card definition

A Card is an internal CARDVERSE collectible tied to a canonical Content entity.

Structure:

Card → Content → External Sources

Never make a provider object the card itself.

## Card types

Games:
- GAME
- GAME_CHARACTER
- DEVELOPER
- PUBLISHER
- FRANCHISE
- PLATFORM

Anime:
- ANIME
- ANIME_CHARACTER
- CREATOR
- STUDIO
- FRANCHISE

Future:
- MOVIE
- ACTOR
- DIRECTOR
- BOOK
- AUTHOR
- ALBUM
- ARTWORK
- HISTORICAL_PERSON
- SPACE_OBJECT

## Card variants

- Standard
- Special
- Foil
- Anniversary
- Event
- Limited
- Alternate Art

Variants should have a real design purpose.

## Card levels

Cards can be upgraded using duplicates and Essence.

Leveling primarily improves:

- frame;
- visual effects;
- prestige;
- collection score;
- selected non-PvP bonuses.

Do not turn upgrades into combat power.

## Optional passive card bonuses

Most cards should have no significant economic modifier.

Rare/Legendary cards may have small thematic bonuses.

Example:

Legendary Elden Ring:
+2% income from RPG Sets.

This is intentionally small. The Set is the main income engine.
