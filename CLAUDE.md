# ClawHub — Claude Code Context

## Role & Scope
This is the **ClawHub skill registry** — the public skill directory for OpenClaw AI agent tools. Live at clawhub.ai.

Users publish, version, search, and install text-based agent skills (SKILL.md + supporting files).

## What Lives Here
1. **Web app** (src/) — TanStack Start (React, Vite/Nitro)
2. **Backend** (convex/) — Convex DB + file storage + HTTP actions + auth (GitHub OAuth)
3. **Search** — OpenAI embeddings (text-embedding-3-small) + Convex vector search
4. **CLI** — clawhub login, search, install, publish, sync
5. **Schema** (packages/schema/) — shared API types/routes for CLI and app
6. **Souls** — onlycrabs.ai SOUL.md registry (host-based routing)
7. **E2E tests** (e2e/) — Playwright test suite

## What Does NOT Live Here
- OpenClaw runtime (that's github.com/openclaw/openclaw)
- tradesman-verify skill (that's gitlab.com/lv8rlabs/tradesman-verify)
- MicroPay settlement (that's MicroPayTechnologies/)
- LV8R Labs operations (that's ProjectAtlas)

## Key Conventions
- **TanStack Start** for routing and SSR
- **Convex** for all backend (no separate API server)
- **Skills** are SKILL.md + supporting files, published via CLI
- **Souls** are SOUL.md, published to onlycrabs.ai host
- **New skills should go to ClawHub first**, not OpenClaw core
- **bun** as package manager (bun.lock)
- **Vitest** for unit tests, **Playwright** for E2E

## CLI Commands
- `clawhub login` / `clawhub whoami` — auth
- `clawhub search` / `clawhub explore` — discover
- `clawhub install <slug>` / `clawhub uninstall <slug>` — manage
- `clawhub publish <path>` / `clawhub sync` — publish

## Repo Info
- **Remote**: github.com/tradesmantools/clawhub (public)
- **Branch**: main
- **License**: MIT
- **Live**: clawhub.ai (Vercel) + onlycrabs.ai
- **Owner**: JC — Jonathon Chambless
- **Related**: github.com/openclaw/openclaw (runtime), gitlab.com/lv8rlabs/tradesman-verify (example skill)
