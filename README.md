# PNPM workspace monorepo

PoC of a monorepo using pnpm workspace.

## Prerequisites

- PNPM installed: [installation guide](https://pnpm.io/installation)


## Getting started

1. Install workspace dependencies (used across packages): `pnpm install`
1. To build a single apps/package: `pnpm --filter "@pnpm-monorepo/express-app-1" build`
1. To build all apps: `pnpm --filter "*" build`
1. To build a single app (with dependencies installed): `pnpm --filter "@pnpm-monorepo/express-app-1"  deploy <dir-name>`

Note: to clear all node_modules from apps: `pnpm recursive exec -- find . -name "node_modules" -type d -exec rm -rf {} +`
