# 25 — Idle Economy Design

## Purpose

The idle/clicker system exists to solve a core collection problem:

The player needs a reliable way to earn Packs without real-money purchases.

## Three economic stages

### Stage A — Clicker

At the beginning:

Coins mostly come from clicking.

Example:

+1 Coin/click
0 Coins/sec

The player learns the economic loop.

### Stage B — Automation

The player unlocks:

- Auto Collector;
- Auto Collector II;
- collection assistants;
- click multipliers.

Example:

+20 Coins/click
+50 Coins/sec

Clicking remains useful but is no longer mandatory.

### Stage C — Collection economy

Completed Sets become major income sources.

Example:

Gaming Origins:
+10 Coins/sec

RPG Legends:
+35 Coins/sec

Anime Classics:
+25 Coins/sec

The collection becomes the player's economic infrastructure.

## Income formula

Conceptually:

Total CPS =
Base Automation
+ Sum(Set Income)
+ Collection Bonuses
+ Temporary Event Bonuses

Do not allow arbitrary stacking without a cap or balance review.

## Click formula

Click Reward =
Base Click Power
× Click Upgrades
× Temporary Bonuses

Avoid permanent multiplicative explosions.

## Offline income

Offline reward:

min(elapsed_time, offline_cap) × valid_CPS

Example:

CPS = 100
elapsed = 12h
cap = 8h

Reward = 100 × 8h

## Set income

Base Set income should depend on:

- Set size;
- rarity composition;
- intended completion time;
- Set tier.

Larger or harder Sets can provide more income.

Do not simply make every Set's income proportional to card count.

## Mastery

Completed Set:

+X CPS

Mastered Set:

+Y CPS

where Y > X.

Mastery may require:

- all unique cards;
- upgrades;
- variants;
- special achievement.

## Economic feedback

Home screen should make the relationship visible:

**Your collection earns +1,240 Coins/sec**

This reinforces the fantasy.

## Balance warning

Do not balance the clicker separately from Packs.

Always evaluate:

Click income
+
Idle income
+
Set income
vs
Pack costs
+
Upgrade costs
+
Essence generation

## Target experience

Early:
"Clicking gets me my next Pack."

Middle:
"My upgrades let me afford Packs faster."

Late:
"My collection earns enough that I can focus on collecting and Sets."

This progression is intentional.
