# PNPM workspace monorepo

PoC of a monorepo using pnpm workspace.

## Prerequisites

- PNPM installed: [installation guide](https://pnpm.io/installation)


## Getting started

1. Install workspace dependencies (used across packages): `pnpm install`
1. To build a single package: `pnpm --filter "@pnpm-monorepo/express-app" build p`
1. To build all packages: `pnpm --filter "*" build`
