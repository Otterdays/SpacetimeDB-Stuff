<!-- PRESERVATION RULE: Never delete or replace content. Append or annotate only. -->

### AAA-Scale Real-Time Games (Lightning-fast DB)

> ADHD/autism-friendly quick read. Short, punchy, scannable entries.

---

### 1) Eclipse City: Real-Time Open-World MMO-lite

**Pitch**: Futuristic megacity with persistent districts; 100-200 players per shard; player-run economy and governance.

**What you get**:

- Player-owned storefronts and districts
- Real-time city events (concerts, outages, parades)
- Live NPC economy and staffing
- City-wide chat and governance panels

**Real-Time Elements**:

- Atomic property licenses and transactions across districts
- Global event engine with countdowns and immediate effects
- Neighborhood dashboards with per-player activity feeds

**SpacetimeDB Fit**:

- Massive region tables; atomic ops for licenses
- Scheduled events and countdown triggers
- Views for district dashboards; nearby activity subscriptions

**Monetization**:

- District premiums; city services microtransactions; map skins

**MVP Scope**:

- 2 districts; 50 players per shard; basic storefronts and events
- Core economy, chat, governance

**Why SpacetimeDB**:

- Real-time world-state with minimal infra complexity

---

### 2) Nova Armada II: Real-Time Space Warfare

**Pitch**: Massive space battles with fleets, capital ships, and orbital assaults.

**What you get**:

- 20v20 or 40v40 fleet battles
- Fleet commands (form-up, engage, defend, retreat)
- Resource management (fuel, ammo, shields)
- Destructible stations and space gates

**Real-Time Elements**:

- Simultaneous fleet actions; warp-ins and reinforcements
- Orbital bombardment and warp mechanics
- Real-time map control and capture objectives

**SpacetimeDB Fit**:

- Atomic battle resolution in reducers; fleet-state tables
- Event triggers for warp-ins and reinforcements
- High-frequency subscriptions for fleets

**Monetization**:

- Season passes; ship skins; cosmetics
- Premium fleet commands

**MVP Scope**:

- 2 fleets per side; 3 maps; basic fleet commands
- Core combat, shields, loot drops

**Why SpacetimeDB**:

- Real-time fleet state across players without server bottlenecks

---

### 3) Realm Conquest: Real-Time Tactical MMO-lite

**Pitch**: Territorial RTS meets MMO; factions vie for control across a procedurally generated world.

**What you get**:

- Territory capture and fortification
- Shared resource nodes; cross-faction supply lines
- Real-time diplomacy chat; alliance raids
- Dynamic events (storm, famine, festival)

**Real-Time Elements**:

- Simultaneous battle outcomes; territory state propagation
- Alliance-wide events and cooldowns
- Global world state across zones

**SpacetimeDB Fit**:

- Region-based state machines; multi-zone reducers
- Scheduled events shaping world state
- Views for faction leaders; subscriptions for frontline zones

**Monetization**:

- Faction cosmetics; premium territory upgrades
- Seasonal world events DLC

**MVP Scope**:

- 2 factions; 2 regions; 20 players per region
- Core capture mechanics and diplomacy

**Why SpacetimeDB**:

- Handles large-scale, low-latency updates

---

### 4) Titanfall: Real-Time Mech Arena

**Pitch**: 4v4 mech arena with wall-run and boost; high-velocity close-quarters combat.

**What you get**:

- 4v4 matches; 3 arenas
- Mech loadouts and boost abilities
- Team objectives (capture points, escort)
- Spectator mode with live highlights

**Real-Time Elements**:

- Ultra-low-latency controls; real-time hit registration
- Dynamic arena hazards (turrets, energy walls)
- Skill-based matchmaking from day one

**SpacetimeDB Fit**:

- Atomic combat actions; per-match state
- Live arena hazard triggers via scheduled events
- Player progression and cosmetics stored in real-time tables

**Monetization**:

- Season passes; cosmetic skins; loot crates
- Pro analytics for pros

**MVP Scope**:

- 2 arenas; 8 players; basic loadouts

**Why SpacetimeDB**:

- AAA feel with robust real-time sync

---

### 5) Neon Hyperrace: Real-Time Online Racing

**Pitch**: Real-time anti-gravity racing across neon cities; live track hazards and rival interactions.

**What you get**:

- 24-car race lobbies; dynamic tracks
- Real-time track hazards (turbo boosts, oil slicks)
- Replays with AI highlights
- In-race player interactions (ram, block, EMP)

**Real-Time Elements**:

- Ultra-low latency timing; real-time lap timing
- Live weather and track-state changes
- Spectator engagement (live polls, bets)

**SpacetimeDB Fit**:

- Real-time position updates; collisions in reducers
- Track state persisted in time-window tables
- Subscriptions for real-time leaderboards

**Monetization**:

- Race passes; cosmetics; track packs
- In-race cosmetics microtransactions

**MVP Scope**:

- 6 tracks; 24 players; basic car models
- Core collision and lap timing

**Why SpacetimeDB**:

- Real-time racing requires perfect sync and minimal latency

---

### 6) Astral Heist: Real-Time Space Heist

**Pitch**: 5-6 player crew on starship heists; plan, hack, and escape in real-time.

**What you get**:

- Real-time hacking minigame
- Security NPCs and alarms that respond instantly
- Escape routes and chases
- Loot distribution and crew roles

**Real-Time Elements**:

- Simultaneous crew actions; betrayals
- Real-time alert cascades; reinforcements arrive instantly
- Loot drops with visible drop times

**SpacetimeDB Fit**:

- Atomic loot distribution reducers
- Event-driven security alerts
- Region/state simulation of starship interiors

**Monetization**:

- Heist packs; crew cosmetics
- DLC expansions with new ships

**MVP Scope**:

- 1 ship; 2 heists; 2 loadouts; 5 crew roles

**Why SpacetimeDB**:

- Supports dynamic, high-stakes simultaneous interactions

---
