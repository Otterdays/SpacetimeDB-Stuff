<!-- PRESERVATION RULE: Never delete or replace content. Append or annotate only. -->

# SUGGESTIONS

This doc is the **curation of ideas** for games, programs, and tools built on SpacetimeDB — what to explore, prototype, or ship. Not a backlog for any single app.
## Sources

- [SpacetimeDB Home](https://spacetimedb.com/home)
- `grok-4.20-suggestions.md` — raw brainstorm (kept verbatim in repo)
- `DOCS/01_GAMES.md` → `09_GAMING_ECOSYSTEMS.md` — 400+ ideas by category

---

## Where to Look

| Want to build… | Go to |
|----------------|-------|
| **Games** (party, MMO, BR, etc.) | [01_GAMES.md](01_GAMES.md) |
| **Dev tools** (plugins, BaaS, systems) | [02_DEVELOPER_TOOLS.md](02_DEVELOPER_TOOLS.md) |
| **Voice / chat / comms** | [03_VOICE_COMMS.md](03_VOICE_COMMS.md) |
| **Streaming / video** | [04_STREAMING_VIDEO.md](04_STREAMING_VIDEO.md) |
| **Business tools** | [05_BUSINESS_TOOLS.md](05_BUSINESS_TOOLS.md) |
| **Dashboards** | [06_DASHBOARDS.md](06_DASHBOARDS.md) |
| **Commerce / finance** | [07_COMMERCE_FINANCE.md](07_COMMERCE_FINANCE.md) |
| **Special industries** | [08_SPECIAL_INDUSTRIES.md](08_SPECIAL_INDUSTRIES.md) |
| **Gaming ecosystems** | [09_GAMING_ECOSYSTEMS.md](09_GAMING_ECOSYSTEMS.md) |

---

## Building Blocks (patterns for any SpacetimeDB project)

Reusable patterns you can pull into games or programs:

- **Private DMs** — `direct_message` table; filtered subscription per user pair
- **Rooms / channels** — `room` + `message.room_id`; create/join/leave reducers
- **Reactions** — `reaction` table linked to message; live counters
- **Typing indicators** — ephemeral table + scheduled cleanup
- **Profiles / online status** — `profile`, `online_status`; update in connect/disconnect
- **Friends / moderation** — `friend_request`, `friend`, `user_role`; role-gated reducers
- **Leaderboards** — counters or query-view aggregation
- **Scheduled jobs** — auto-cleanup, stats, archive; use scheduled tables/reducers

---

## (Legacy) Chat-specific patterns (for reference)

- **Private DMs**
  - **Data**: `direct_message` table with `id (u64 pk autoInc)`, `sender (identity)`, `receiver (identity)`, `sent (timestamp)`, `text (string)`
  - **Reducers**: `send_direct_message({ receiver, text })`
  - **Client**: filtered subscription / view per-user (avoid `public: true` on raw DM rows unless intentional)
- **Rooms / channels**
  - **Data**: `room` table + `message.room_id`
  - **Reducers**: `create_room`, `join_room`, `leave_room`, `send_message({ roomId, text })`
- **Reactions**
  - **Data**: `reaction` table referencing message id
  - **Reducers**: `add_reaction`, `remove_reaction`
- **Edit / delete (soft delete)**
  - **Data**: add `edited_at`, `deleted_at` (or `is_deleted`)
  - **Reducers**: `edit_message`, `delete_message` with ownership check (`ctx.sender`)
- **Typing indicators**
  - **Data**: `typing` table with last-updated timestamp
  - **Scheduled cleanup**: periodic reducer to remove stale typing rows
- **Threads / reply-to**
  - **Data**: `reply_to_message_id` on message rows
  - **UI**: grouped rendering for threads
- **Pinned messages / announcements**
  - **Data**: `pinned_message` table (room + message id)
  - **Auth**: role-gated reducers (see moderation section)
- **Search**
  - **Option A**: add index(es) for common lookups (sender, room, time)
  - **Option B**: add a view/query tailored for “latest N in room”
  - **NOTE**: if you introduce full-text search, document and test it (engine support varies)
- **Rich text / attachments**
  - **Option A**: markdown string with safe renderer on client
  - **Option B**: attachment rows storing URL + metadata

### Users & identity

- **Profiles**
  - **Data**: `profile` table (displayName, bio, avatarUrl, color)
  - **Lifecycle**: create profile in `clientConnected` if missing
- **Online / last seen**
  - **Data**: `online_status` table updated on connect/disconnect
- **Friends**
  - **Data**: `friend_request`, `friend` tables
  - **Reducers**: request/accept/reject
- **Roles / moderation**
  - **Data**: `user_role` (admin/mod/muted/banned)
  - **Reducers**: `set_role`, `mute_until`, `ban_user`
  - **Scheduled**: auto-unmute
- **Leaderboard**
  - **Data**: counters table, or query-view aggregation

### UI/UX polish (client)

- **Modern UI kit**
  - Tailwind + component library (shadcn/daisy) is optional; keep DX simple
- **Auto-scroll + “new messages” affordance**
- **Pagination / infinite scroll**
- **PWA**
- **Notifications**
  - browser Notification API on mentions / DMs
- **Themes**
  - local-only first; optionally “room theme” table later

### Backend/module direction

- **Keep module TypeScript-first (current)**
  - Continue iterating on `spacetimedb/src/index.ts` schema/reducers
- **OR add a Rust module alongside**
  - If you do: create a separate folder (don’t overwrite the TS module) and document the switch clearly

### Quality & delivery

- **Tests**
  - reducer-level tests (where supported) + vitest for UI
- **CI**
  - lint/test on push; optional publish workflow
- **Local one-click dev**
  - script that starts SpacetimeDB + publishes module + starts Vite

---

## “Idea Card” Template (pulled forward from legacy docs)

Use this structure when adding new entries to `DOCS/01_*`–`DOCS/09_*` so ideas stay scannable and actionable.

- **Pitch**: one sentence
- **What you get**: 4–7 bullets (features)
- **Real-time elements**: what must be realtime and why
- **SpacetimeDB fit**: which tables/reducers/subscriptions are the core
- **Monetization**: 1–3 options
- **MVP scope**: smallest playable/testable slice
- **Why SpacetimeDB**: 1–2 bullets (the “unfair advantage”)

