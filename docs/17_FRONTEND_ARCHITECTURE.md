# 17 — Frontend Architecture

## Recommended stack

- React
- TypeScript
- Vite
- IndexedDB/localStorage
- responsive CSS

## Screens

### Home
- Coins;
- Coins/sec;
- Click button;
- Pack shortcut;
- daily reward;
- active goals;
- featured Set.

### Collection
- card grid;
- owned/missing;
- filters;
- sorting;
- search;
- set progress.

### Packs
- available Packs;
- cost;
- probability information;
- opening animation.

### Card detail
- image;
- rarity;
- level;
- metadata;
- relationships;
- upgrade;
- duplicate conversion.

### Sets
- checklist;
- progress;
- reward;
- passive income;
- mastery.

### Idle/Hub
- click power;
- automation;
- passive income;
- offline cap;
- upgrades.

### Profile
- level;
- achievements;
- favorite cards;
- showcase;
- collection completion.

### Events
- season;
- active event;
- quests;
- rewards.

## State separation

UI state ≠ game state ≠ persisted state.

## Performance

- lazy images;
- responsive image sizes;
- virtualized collection grid;
- cache catalog;
- avoid loading all images at startup.

## Accessibility

- keyboard support;
- touch targets;
- reduced motion;
- rarity icon/text in addition to color;
- mobile-first layouts.
