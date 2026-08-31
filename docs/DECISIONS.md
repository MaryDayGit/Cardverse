# Architectural Decisions

## ADR-001 — No PvP

PvP is explicitly excluded.

Reason:
The product fantasy is collection + idle progression, not combat.

## ADR-002 — Idle/clicker as economic engine

Decision:
Coins are earned through clicking and passive income.

Reason:
Players need a free, repeatable way to fund Packs without real-money purchases.

## ADR-003 — Completed Sets generate income

Decision:
A completed Set becomes an idle income source.

Reason:
This creates the key bridge:

Collection → Economy → More Collection.

## ADR-004 — Free first Pack

Decision:
Every new player gets a free Beginner Discovery Pack.

Reason:
The core fantasy must be demonstrated immediately.

## ADR-005 — Self-starting onboarding economy

Decision:
The first onboarding quests cannot require Packs/resources the player does not own.

Reason:
Avoid deadlocks such as "open a Pack to complete a quest, but you have no Pack."

## ADR-006 — Local-first MVP

Decision:
Prototype starts with local persistence.

Reason:
Fastest validation and simplest itch.io deployment.

## ADR-007 — APIs are ingestion sources

Decision:
External APIs never control gameplay at runtime.

Reason:
Rate limits, outages, security and provider independence.

## ADR-008 — Canonical internal content model

Decision:
Provider IDs are references, not canonical identity.

Reason:
Provider replacement and multi-source enrichment.

## ADR-009 — Rarity is CARDVERSE logic

Decision:
External metrics influence rarity but do not determine it directly.

Reason:
Balance, explainability and editorial control.

## ADR-010 — No paid randomized Packs in MVP

Decision:
Only optional donations/support.

Reason:
Simple economy, lower legal/payment complexity and no pay-to-win.

## ADR-011 — Multi-universe architecture

Decision:
Games and Anime are first universes inside one shared content engine.

Reason:
Future expansion without rewriting collection/game systems.
