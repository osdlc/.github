# Open SDLC

The [osdlc organization](https://github.com/osdlc) builds tools and libraries for software
development workflows, coding-agent integrations, and developer tooling. Its projects range from
the `sdlc` workflow CLI and agent plugins to reusable libraries and standalone tools.

## Projects

| Repository | What it is |
| --- | --- |
| [osdlc](https://github.com/osdlc/osdlc) | The `sdlc` CLI, the `sdlc` and `craft` agent plugins, and TypeScript and Rust libraries used by the tools. |
| [parley](https://github.com/osdlc/parley) | A plugin that turns an agent-authored document into a web review page where a person can comment and answer questions. |
| [skillwright](https://github.com/osdlc/skillwright) | A CLI and agent plugin for publishing, checking, authoring, and reorganizing markdown skill vaults across coding-agent tools. |
| [dashboard](https://github.com/osdlc/dashboard) | A modular developer dashboard with terminal and web interfaces. |
| [marketplace](https://github.com/osdlc/marketplace) | Generated plugin marketplace distributing the `sdlc` and `craft` plugins for Claude Code, Codex, Cursor, and Pi. |
| [homebrew-tap](https://github.com/osdlc/homebrew-tap) | Homebrew formulae for osdlc command-line tools, including `skillwright`. |
| [osdlc-acceptance](https://github.com/osdlc/osdlc-acceptance) | A small fixture repository used by automated `sdlc` acceptance runs. |
| [.github](https://github.com/osdlc/.github) | Organization-level profile and shared GitHub community information. |

## Packages

The [osdlc/osdlc package guide](https://github.com/osdlc/osdlc/blob/main/packages/README.md) has
package documentation, development conventions, and release instructions. Most libraries there
are published to npm or crates.io. The `skillwright` and `tradecraft` packages have moved to
[osdlc/skillwright](https://github.com/osdlc/skillwright); `osdlc/osdlc` retains a legacy
`tradecraft` crate that points to `skillwright`.

### TypeScript packages in `osdlc/osdlc`

| Package | Purpose |
| --- | --- |
| [`@osdlc/agent-call`](https://github.com/osdlc/osdlc/tree/main/packages/ts/agent-call) | A shared call specification for headless coding-agent CLIs. |
| [`@osdlc/cli-tool`](https://github.com/osdlc/osdlc/tree/main/packages/ts/cli-tool) | Common foundations for standalone command-line tools. |
| [`@osdlc/code-host`](https://github.com/osdlc/osdlc/tree/main/packages/ts/code-host) | Pull-request host interface with GitHub and Forgejo adapters. |
| [`@osdlc/color`](https://github.com/osdlc/osdlc/tree/main/packages/ts/color) | sRGB color arithmetic for contrast checks. |
| [`@osdlc/command-seam`](https://github.com/osdlc/osdlc/tree/main/packages/ts/command-seam) | Shared command execution seam for tools. |
| [`@osdlc/config-layers`](https://github.com/osdlc/osdlc/tree/main/packages/ts/config-layers) | Project and machine configuration layers and startup checks. |
| [`@osdlc/detect-harness`](https://github.com/osdlc/osdlc/tree/main/packages/ts/detect-harness) | Read-only detection of coding-agent harnesses and their settings. |
| [`@osdlc/etag-write`](https://github.com/osdlc/osdlc/tree/main/packages/ts/etag-write) | Conditional, compare-and-swap file writes. |
| [`@osdlc/frontmatter-lossless`](https://github.com/osdlc/osdlc/tree/main/packages/ts/frontmatter-lossless) | Lossless frontmatter parsing and editing. |
| [`@osdlc/gfm-table`](https://github.com/osdlc/osdlc/tree/main/packages/ts/gfm-table) | GitHub-flavored Markdown table utilities. |
| [`@osdlc/intersect`](https://github.com/osdlc/osdlc/tree/main/packages/ts/intersect) | Determines whether path patterns overlap and provides a witness path. |
| [`@osdlc/markdown-contract`](https://github.com/osdlc/osdlc/tree/main/packages/ts/markdown-contract) | Parse and validate contracts for Markdown documents. |
| [`@osdlc/markdown-link`](https://github.com/osdlc/osdlc/tree/main/packages/ts/markdown-link) | Parse wiki and relative Markdown links while excluding code spans. |
| [`@osdlc/observe`](https://github.com/osdlc/osdlc/tree/main/packages/ts/observe) | JSONL event records, correlation IDs, and agent-session observation. |
| [`@osdlc/path-guard`](https://github.com/osdlc/osdlc/tree/main/packages/ts/path-guard) | Lexical and symlink-aware path containment checks. |
| [`@osdlc/prettier-config`](https://github.com/osdlc/osdlc/tree/main/packages/ts/prettier-config) | Shared Prettier configuration. |
| [`@osdlc/pr-update`](https://github.com/osdlc/osdlc/tree/main/packages/ts/pr-update) | Bring pull-request branches up to date and help recover conflicts. |
| [`@osdlc/repo-cleaner`](https://github.com/osdlc/osdlc/tree/main/packages/ts/repo-cleaner) | Find and remove approved, already-merged branches and worktrees. |
| [`@osdlc/result`](https://github.com/osdlc/osdlc/tree/main/packages/ts/result) | Plain-object `Result` and `Failure` types. |
| [`@osdlc/system-model`](https://github.com/osdlc/osdlc/tree/main/packages/ts/system-model) | Wire model for repositories, packages, tools, and tasks. |
| [`@osdlc/tiered-dirs`](https://github.com/osdlc/osdlc/tree/main/packages/ts/tiered-dirs) | Machine-local directories organized by tier and home. |
| [`@osdlc/trust-repo`](https://github.com/osdlc/osdlc/tree/main/packages/ts/trust-repo) | Per-repository consent and policy checks before running repository scripts. |
| [`@osdlc/tsconfig`](https://github.com/osdlc/osdlc/tree/main/packages/ts/tsconfig) | Shared TypeScript configuration. |
| [`@osdlc/typed-gh`](https://github.com/osdlc/osdlc/tree/main/packages/ts/typed-gh) | Typed GitHub client for the `gh` CLI. |
| [`@osdlc/typed-git`](https://github.com/osdlc/osdlc/tree/main/packages/ts/typed-git) | Typed Git client with synchronous and awaitable interfaces. |
| [`@osdlc/ux`](https://github.com/osdlc/osdlc/tree/main/packages/ts/ux) | Design tokens and output helpers for web pages and terminal UIs. |
| [`@osdlc/wayfinder`](https://github.com/osdlc/osdlc/tree/main/packages/ts/wayfinder) | Browse and run repository tasks from a terminal UI, web view, or JSON. |
| [`@osdlc/yaml-splice`](https://github.com/osdlc/osdlc/tree/main/packages/ts/yaml-splice) | Lossless YAML edits, backed by a Rust WebAssembly build. |

### Rust crates in `osdlc/osdlc` and `osdlc/skillwright`

| Crate | Purpose |
| --- | --- |
| [`agent-adapt`](https://github.com/osdlc/osdlc/tree/main/packages/rust/agent-adapt) | Adapt agent skills and configuration for different coding-agent tools. |
| [`config-layers`](https://github.com/osdlc/osdlc/tree/main/packages/rust/config-layers) | Layered project and machine configuration. |
| [`etag-write`](https://github.com/osdlc/osdlc/tree/main/packages/rust/etag-write) | Conditional, compare-and-swap file writes. |
| [`frontmatter-lossless`](https://github.com/osdlc/osdlc/tree/main/packages/rust/frontmatter-lossless) | Lossless Markdown frontmatter handling. |
| [`glob-intersect`](https://github.com/osdlc/osdlc/tree/main/packages/rust/glob-intersect) | Rust implementation of `@osdlc/intersect`; not yet published to crates.io. |
| [`markdown-contract`](https://github.com/osdlc/osdlc/tree/main/packages/rust/markdown-contract) | Rust implementation of `@osdlc/markdown-contract`. |
| [`markdown-link`](https://github.com/osdlc/osdlc/tree/main/packages/rust/markdown-link) | Markdown and wiki-link parsing. |
| [`markdown-relink`](https://github.com/osdlc/osdlc/tree/main/packages/rust/markdown-relink) | Rewrite links when Markdown files move. |
| [`markdown-vault-fs`](https://github.com/osdlc/osdlc/tree/main/packages/rust/markdown-vault-fs) | Filesystem support for Markdown vaults. |
| [`path-guard`](https://github.com/osdlc/osdlc/tree/main/packages/rust/path-guard) | Path containment and traversal protection. |
| [`skillwright`](https://github.com/osdlc/skillwright/tree/main/packages/rust/skillwright) | CLI for publishing and maintaining coding-agent skill vaults. |
| [`slug-collate`](https://github.com/osdlc/osdlc/tree/main/packages/rust/slug-collate) | Collate and disambiguate slugs. |
| [`tiered-dirs`](https://github.com/osdlc/osdlc/tree/main/packages/rust/tiered-dirs) | Machine-local directories organized by tier and home. |
| [`tradecraft`](https://github.com/osdlc/osdlc/tree/main/packages/rust/tradecraft) | Legacy crate name that points to `skillwright`. |
| [`tradecraft-core`](https://github.com/osdlc/skillwright/tree/main/packages/rust/tradecraft-core) | Core model and operations for markdown skill vaults. |
| [`tradecraft-typegen`](https://github.com/osdlc/skillwright/tree/main/packages/rust/tradecraft-typegen) | TypeScript type generation for Tradecraft. |
| [`tradecraft-wasm`](https://github.com/osdlc/skillwright/tree/main/packages/rust/tradecraft-wasm) | WebAssembly build of the Tradecraft core. |
| [`typed-git`](https://github.com/osdlc/osdlc/tree/main/packages/rust/typed-git) | Typed Git client. |
| [`yaml-splice`](https://github.com/osdlc/osdlc/tree/main/packages/rust/yaml-splice) | Lossless YAML editing. |
| [`yaml-splice-wasm`](https://github.com/osdlc/osdlc/tree/main/packages/rust/yaml-splice-wasm) | WebAssembly build used by `@osdlc/yaml-splice`. |

The `skillwright` repository also publishes [`@osdlc/tradecraft-wasm`](https://github.com/osdlc/skillwright/tree/main/packages/ts/tradecraft-wasm),
the TypeScript package for the Tradecraft WebAssembly build.
