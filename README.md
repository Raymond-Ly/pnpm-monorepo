# PNPM workspace monorepo

PoC of a monorepo using pnpm workspace.

## Prerequisites

- PNPM installed: [installation guide](https://pnpm.io/installation)


## Getting started

1. Install workspace dependencies (used across packages): `pnpm install`
2. To build a single apps/package: `pnpm --filter "@pnpm-monorepo/express-app-1" build`
3. To build all apps: `pnpm --filter "*" build`
4. To build a single app (with dependencies installed): `pnpm --filter "@pnpm-monorepo/express-app-1"  deploy <dir-name>`

Note: to clear all node_modules from apps: `pnpm recursive exec -- find . -name "node_modules" -type d -exec rm -rf {} +`

## Creating deployable directories for specific apps

For `expressApp1`, run: `pnpm deploy:app1` from the root of the repository. This command will:
- pnpm install dependencies filtering for expressApp1, resulting in a `build` folder that includes source files and dependencies,
- build using tsc in the `build` folder created in the previous step 

**Notes:** the same command is available for expressApp2: `pnpm deploy:app2`
