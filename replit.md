# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Artifacts

### SmartAlloc (`artifacts/smart-alloc`)
- React + Vite web app at preview path `/`
- Single-page volunteer resource matching platform
- Features:
  - **Smart Matching**: Keyword-based skill + location matching with % match scores
  - **Urgency Cards**: Red/yellow/green with pulse animations for high urgency
  - **Impact Dashboard**: Animated count-up stats (requests, completed, volunteers)
  - **Visual Map**: SVG placeholder with pulsing red dots for urgent areas, hover tooltips
  - **Request Help Modal**: Form with name, need type, location, description — shows success
  - **Floating FAB**: Bouncing "Request Help" button, opens modal
  - **Filter**: All/High/Medium/Low card filtering
  - **Section animations**: Scroll-triggered fade-in on all sections

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
