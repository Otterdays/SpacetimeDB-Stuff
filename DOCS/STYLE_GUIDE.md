<!-- PRESERVATION RULE: Never delete or replace content. Append or annotate only. -->

# STYLE_GUIDE

## Project Conventions

### Naming
- **JS/TS:** camelCase
- **Files:** PascalCase for components (e.g. `App.tsx`), kebab-case for utilities

### Limits
- 100 char/line
- 50 lines/function
- 400 lines/file

### Trace
- `// [TRACE: filename.md]` — link code to relevant doc

### Comments
- WHY only, never WHAT
- Prefixes: `TODO:` `FIXME:` `NOTE:`

### SpacetimeDB
- Follow `.cursor/rules/spacetimedb-typescript.mdc`
- Reducer calls: object syntax `{ param: value }`
- BigInt for u64: `0n`, `1n`

### Git
- Commits: `<type>(<scope>): <description>` — feat, fix, docs, refactor, chore, test
- Branches: `feature/` `fix/` `chore/` `docs/`
