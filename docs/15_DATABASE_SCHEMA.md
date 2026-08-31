# 15 — Database Schema

Suggested PostgreSQL schema.

## content

id, universe, content_type, title, description, release_date, rating, popularity, legacy_score, uniqueness_score, status, created_at, updated_at

## external_sources

id, content_id, provider, provider_id, source_url, source_hash, fetched_at, attribution, rights_status

Unique(provider, provider_id)

## media_assets

id, content_id, provider, source_url, local_url, mime_type, width, height, rights_status, attribution, checksum

## cards

id, content_id, card_type, rarity, variant, level_cap, active, set_id, created_at

## card_stats

card_id, stat_name, stat_value

## card_effects

card_id, effect_type, value, condition_json

Keep effects small and non-PvP.

## sets

id, universe, name, description, set_type, start_at, end_at, active, base_income, mastery_income

## set_cards

set_id, card_id, weight, guaranteed_eligible

## players

id, display_name, level, xp, created_at

## player_cards

player_id, card_id, quantity, level, first_obtained_at, last_obtained_at

Unique(player_id, card_id)

## wallets

player_id, coins, essence, tickets

## currency_transactions

id, player_id, currency, amount, transaction_type, reference_id, created_at

## packs

id, name, pack_type, cost_coins, cost_tickets, active, config_json

## pack_openings

id, player_id, pack_id, transaction_id, seed_reference, created_at

## pack_results

opening_id, card_id, rarity, variant, duplicate, created_at

## achievements

id, key, name, description, reward_json

## player_achievements

player_id, achievement_id, progress, completed_at

## quests

id, season_id, key, description, requirements_json, reward_json

## player_quests

player_id, quest_id, progress_json, completed_at

## seasons

id, name, start_at, end_at, config_json

## events

id, season_id, name, start_at, end_at, rules_json, active

## idle_sources

id, player_id, source_type, source_id, coins_per_second, active

This can be derived dynamically from completed Sets instead of being stored as a separate source table if preferred.

## offline_income_claims

id, player_id, started_at, ended_at, coins_granted, created_at
