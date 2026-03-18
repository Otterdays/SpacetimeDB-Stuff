# SpacetimeDB-Stuff AGENTS.md (All AIs)

**Project:** Realtime multiplayer playground built on SpacetimeDB (started as official TS chat quickstart). Goal = turn this into a full-featured chat → mini-games platform. Everything must stay realtime, transactional, and deterministic on the backend.

## 1. Core SpacetimeDB Rules (MANDATORY — do NOT violate)
(verbatim from your original rules — kept 100%)

### Migrating from 1.0 to 2.0?
**If you are migrating existing SpacetimeDB 1.0 code to 2.0, apply `spacetimedb-migration-2.0.mdc` first.** It documents breaking changes (reducer callbacks → event tables, `name`→`accessor`, `sender()` method, etc.) and should be considered before other rules.

### Language-Specific Rules
| Language          | Rule File                          |
|-------------------|------------------------------------|
| **TypeScript/React** | `spacetimedb-typescript.mdc` (MANDATORY) |
| **Rust**          | `spacetimedb-rust.mdc` (MANDATORY) |
| **C#**            | `spacetimedb-csharp.mdc` (MANDATORY) |
| **Migrating 1.0 → 2.0** | `spacetimedb-migration-2.0.mdc` |

### Core Concepts
1. **Reducers are transactional** — they do not return data to callers
2. **Reducers must be deterministic** — no filesystem, network, timers, or random
3. **Read data via tables/subscriptions** — not reducer return values
4. **Auto-increment IDs are not sequential** — gaps are normal, don't use for ordering
5. **`ctx.sender` is the authenticated principal** — never trust identity args

### Feature Implementation Checklist (SUPER VERSION)
When implementing ANY feature:
1. **Backend (Rust or schema):** Define table(s)
2. **Backend:** Define reducer(s) to mutate
3. **Client (React/TS):** Subscribe to the table(s) with proper filters
4. **Client:** Call the reducer(s) from UI/hooks — **never skip this**
5. **Client:** Render live from the table(s) via useState + useEffect or custom hooks
6. **Indexes:** Add explicit indexes if querying on non-PK columns. Index names MUST be unique across the entire module.
7. **Testing:** Write reducer unit test + Vitest React component test

**Common mistake to destroy:** Building backend only and forgetting client subscription + reducer call.

## 2. Project-Specific Rules (THIS REPO ONLY)

### React/TS Client Rules
- Use `@clockworklabs/spacetimedb-sdk` v2+ only.
- Wrap subscriptions in custom hooks (`useSpacetimeTable`, `useMessages`, `useOnlineUsers`, etc.).
- Never call reducers directly in render — always from event handlers or useReducer.
- Auto-scroll chat with `useEffect` + `scrollIntoView` on new messages.
- All state comes from SpacetimeDB — no local-only state for shared data.
- Use `Identity` for user keys everywhere.
- Dark mode + Tailwind/shadcn preferred.

### Rust Module Rules (when we add server/)
- Put module in `spacetimedb/` folder (Cargo + lib.rs).
- All reducers in one module for now.
- Use `#[spacetimedb(reducer)]` macro.
- Profanity filter + rate limiting in every public reducer.
- Scheduled reducers for cleanup (old messages, typing indicators).
- Never put random or HTTP calls in reducers unless via external service pattern.

### Naming & Schema Conventions
- Tables: PascalCase (Message, Profile, Room)
- Columns: snake_case (sender_identity, created_at)
- Reducers: camelCase (sendMessage, updateProfile)
- Indexes: `idx_table_column` (idx_message_room_id)
- Always add `created_at: u64` (unix timestamp) to mutable tables.

### UI/UX Standards
- Message bubbles with sender color from Profile.
- Live typing indicators (5s auto-cleanup).
- Mobile-first + PWA ready.
- Toast notifications for errors/connection drops.
- Emoji picker + markdown rendering mandatory for chat.

### Testing & Deployment
- Vitest for everything.
- GitHub workflow: build + spacetime publish on push to main.
- Local: `spacetime start` + `pnpm dev`
- Cloud: `spacetime publish` after login.

## 3. Prioritized Backlog (Start Here)

### Phase 0 — Fix the Foundation (do first)
- Move to real Rust module in `spacetimedb/`
- Add proper indexes everywhere
- Migrate to filtered subscriptions

### Phase 1 — Chat Upgrades (make it actually good)
1. Private DMs (DirectMessage table)
2. Rooms/Channels
3. Message reactions + editing/deletion
4. Typing indicators + threaded replies
5. User profiles + avatars + online status
6. Roles/moderation + friend system

### Phase 2 — Game Mode (pull from DOCS/)
- Shared whiteboard (Pixel table) — see 01_GAMES.md
- Tic-Tac-Toe / Connect-4 in-room
- RPG elements (XP, levels, inventory)
- Geo-chat or music sync
- Full ideas: Overcooked Online, Drawing Battle, Proximity Voice (03_VOICE_COMMS.md), Live Dashboard (06_DASHBOARDS.md), etc.

### Phase 3 — Advanced
- AI bot reducer (call external API)
- File uploads + rich media
- Webhooks (Discord/Slack)
- Analytics counters
- Export/backup reducer

### Wild Bucket (from your DOCS/)
See DOCS/01_GAMES.md → 09_GAMING_ECOSYSTEMS.md for 400+ ideas. Prioritize anything realtime + multiplayer.

## 4. AI Prompting Rules (How to Use This File)
- ALWAYS start your thinking with: “Following AGENTS.md strictly…”
- Never suggest non-deterministic code in reducers.
- If adding a feature, output: 1) schema changes, 2) reducer code, 3) React hook + component changes.
- Reference DOCS/ files when pulling ideas.
- Keep it snappy but production-ready (no console.logs in final code).
- If unsure about SpacetimeDB API, check official docs first.

**This is now the single source of truth.** Update this file as we grow. Let’s turn this repo from “prep” into the dopest SpacetimeDB showcase on the planet.

Built for @Otterdays — homie mode activated 🚀