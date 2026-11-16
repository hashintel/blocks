# Blocks

A public collection of [Block Protocol](https://blockprotocol.org/) blocks developed by HASH.

The [`blocks/`](blocks) directory contains 22 blocks, including their source code, assets and licenses. See the [block catalog](blocks/README.md) for descriptions and links to published blocks.

## Development

These blocks were moved from [`hashintel/labs`](https://github.com/hashintel/labs/tree/510e82a9e0276827e006acb698a48c9190ee026e/blocks), retaining the `blocks/<name>` paths and package versions.

The imported packages depend on tooling from the original HASH monorepo. A standalone build requires the following setup:

- A root Yarn workspace and lockfile must be restored.
- The shared `@local/eslint`, `@local/tsconfig` and `@local/hash-isomorphic-utils` packages must be provided or replaced.
- The Yarn patches referenced by the `embed` and `table` packages must be restored.

These requirements already existed in Labs. Once the shared tooling is available, each block's `package.json` provides its development, build and serve scripts.

## Repository setup

The repository uses HASH's shared PR checks and Renovate workflow. Scheduled dependency updates require the `CF_ACCESS_STAGE_CLIENT_SECRET` and `RENOVATE_TOKEN_ENC_KEY` organization secrets to be made available to this repository.

Block publishing workflows must also be configured before publishing from this repository.

## License

The blocks are dual-licensed under the MIT and Apache 2.0 licenses. Each block directory contains its license texts and notices.
