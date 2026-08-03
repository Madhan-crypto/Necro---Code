# Refactor Radar agent guide

## Setup

- Use Node.js 20.9+ and npm 10+.
- Install with `npm install`, then run `npm run dev`.
- Run `npm test`, `npm run typecheck`, and `npm run build` before handing off changes.

## Architecture

- `lib/scan.ts` is the deterministic analysis boundary. Keep its public API pure and side-effect free.
- `data/sample-project` is a deliberately seeded fixture. Preserve exactly one instance of each documented core issue.
- UI state belongs in client components; API routes may only enrich wording and must never expose secrets.

## Conventions

- Prefer small, accessible React components and semantic controls.
- Keep refactor previews simulated unless an explicit safe-mutation feature is being extended.
- Do not add authentication or require an API key for the demo flow.
