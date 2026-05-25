# pnpm (pnpm)
pnpm is a fast, disk space efficient package manager for JavaScript and Node.js projects. It uses a content-addressable store and a strict, symlinked `node_modules` layout so every version of every package is stored exactly once on disk and projects can only access dependencies they explicitly declare. pnpm provides first-class monorepo support via `pnpm-workspace.yaml`, the `workspace:` protocol, Catalogs, package filtering, and a shared lockfile, and ships supply-chain safety features such as `minimumReleaseAge`, opt-in lifecycle scripts, dependency overrides, and a built-in `pnpm patch` workflow. Developed in the open under the MIT license on GitHub with an Open Collective sponsorship model, pnpm is used by major JavaScript projects including Next.js, Vue, Vite, Nuxt, Material UI, Prisma, Astro, and SvelteKit.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/pnpm/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=opensource-api-evangelist&utm_content=repo)

## Tags

 - Node.js, Package Manager, Monorepo, JavaScript, Open Source, Developer Tools, Dependency Management, CLI

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## At a Glance

| | |
|---|---|
| License | MIT |
| Primary language | TypeScript (with Rust components) |
| Latest major | pnpm 11 (requires Node.js v22+) |
| Distribution | `pnpm` on npm, `@pnpm/exe` standalone binary, Homebrew, Scoop, Chocolatey, winget, Corepack, standalone install script |
| Source | [github.com/pnpm/pnpm](https://github.com/pnpm/pnpm) |
| Funding | Open Collective + GitHub Sponsors |

## APIs

### pnpm CLI
The pnpm command-line interface for managing JavaScript/Node.js packages. Provides commands for installing, updating, and removing dependencies; running package scripts; executing one-off packages via `pnx` (formerly `dlx`); publishing to registries; auditing for vulnerabilities; managing the content-addressable store; inspecting the dependency graph; and patching installed packages. As of pnpm 11, `pn` is a shorthand for `pnpm` and `pnx` replaces `pnpm dlx`.

**Human URL:** [https://pnpm.io/pnpm-cli](https://pnpm.io/pnpm-cli)

- [Documentation — pnpm CLI overview](https://pnpm.io/pnpm-cli)
- [Documentation — pnpm install](https://pnpm.io/cli/install)
- [Documentation — pnpm add](https://pnpm.io/cli/add)
- [Documentation — pnpm update](https://pnpm.io/cli/update)
- [Documentation — pnpm remove](https://pnpm.io/cli/remove)
- [Documentation — pnpm run](https://pnpm.io/cli/run)
- [Documentation — pnpm exec](https://pnpm.io/cli/exec)
- [Documentation — pnpm dlx (pnx)](https://pnpm.io/cli/dlx)
- [Documentation — pnpm publish](https://pnpm.io/cli/publish)
- [Documentation — pnpm audit](https://pnpm.io/cli/audit)
- [Documentation — pnpm store](https://pnpm.io/cli/store)
- [Documentation — pnpm list](https://pnpm.io/cli/list)
- [Documentation — pnpm why](https://pnpm.io/cli/why)
- [Documentation — pnpm outdated](https://pnpm.io/cli/outdated)
- [Documentation — pnpm patch](https://pnpm.io/cli/patch)

### pnpm Workspaces
Native monorepo support driven by a `pnpm-workspace.yaml` file at the repository root. Supports the `workspace:` protocol for explicit local package references, a shared workspace lockfile, package filtering via `--filter`, recursive commands across all workspace packages, and Catalogs for centralized dependency version management across a monorepo. Integrates with Changesets and Rush for multi-package releases.

**Human URL:** [https://pnpm.io/workspaces](https://pnpm.io/workspaces)

- [Documentation — Workspaces](https://pnpm.io/workspaces)
- [Documentation — pnpm-workspace.yaml](https://pnpm.io/pnpm-workspace_yaml)
- [Documentation — Catalogs](https://pnpm.io/catalogs)
- [Documentation — Filtering](https://pnpm.io/filtering)
- [Documentation — pnpm recursive](https://pnpm.io/cli/recursive)

### pnpm Content-Addressable Store
A content-addressable store that holds every version of every package exactly once on disk and hard-links (or reflinks) files into project `node_modules`. This produces a strict, non-flat dependency layout where packages can only access their declared dependencies, and saves significant disk space across projects on the same machine. Includes commands to inspect, prune, verify, and configure the store.

**Human URL:** [https://pnpm.io/symlinked-node-modules-structure](https://pnpm.io/symlinked-node-modules-structure)

- [Documentation — Symlinked node_modules structure](https://pnpm.io/symlinked-node-modules-structure)
- [Documentation — Motivation](https://pnpm.io/motivation)
- [Documentation — pnpm store CLI](https://pnpm.io/cli/store)
- [Documentation — store-dir config](https://pnpm.io/npmrc#store-dir)

### pnpm Hooks
Programmatic extension points for customizing dependency resolution and installation behavior. `.pnpmfile.cjs` exposes lifecycle hooks (`readPackage`, `afterAllResolved`) that let projects rewrite package manifests before installation. The `pnpm` block in `package.json` adds `overrides`, `packageExtensions`, `patchedDependencies`, `peerDependencyRules`, and `neverBuiltDependencies` for fine-grained dependency control without forking packages.

**Human URL:** [https://pnpm.io/pnpmfile](https://pnpm.io/pnpmfile)

- [Documentation — .pnpmfile.cjs](https://pnpm.io/pnpmfile)
- [Documentation — pnpm.overrides](https://pnpm.io/package_json#pnpmoverrides)
- [Documentation — pnpm.packageExtensions](https://pnpm.io/package_json#pnpmpackageextensions)
- [Documentation — pnpm.patchedDependencies](https://pnpm.io/package_json#pnpmpatcheddependencies)

### pnpm Configuration
Configuration surface for pnpm spanning `.npmrc`, environment variables, and `pnpm`-prefixed fields in `package.json`. Controls registry selection, authentication tokens, store location, hoisting behavior, lockfile settings, lifecycle script policy (including the supply-chain safety settings such as `minimumReleaseAge` and `ignoredBuiltDependencies`), peer dependency rules, and workspace behavior.

**Human URL:** [https://pnpm.io/npmrc](https://pnpm.io/npmrc)

- [Documentation — .npmrc](https://pnpm.io/npmrc)
- [Documentation — package.json pnpm fields](https://pnpm.io/package_json)
- [Documentation — pnpm config CLI](https://pnpm.io/cli/config)
- [Documentation — Settings](https://pnpm.io/settings)

## Common Properties

- [Portal — pnpm.io](https://pnpm.io)
- [GettingStarted — Installation](https://pnpm.io/installation)
- [Documentation — Motivation](https://pnpm.io/motivation)
- [Documentation — pnpm CLI Reference](https://pnpm.io/pnpm-cli)
- [Documentation — Feature comparison vs npm/Yarn](https://pnpm.io/feature-comparison)
- [Documentation — Benchmarks](https://pnpm.io/benchmarks)
- [GitHubRepository — pnpm/pnpm](https://github.com/pnpm/pnpm)
- [GitHubOrganization — pnpm](https://github.com/pnpm)
- [ReleaseNotes — Releases](https://github.com/pnpm/pnpm/releases)
- [ChangeLog](https://github.com/pnpm/pnpm/blob/main/CHANGELOG.md)
- [Legal — MIT License](https://github.com/pnpm/pnpm/blob/main/LICENSE)
- [Support — GitHub Issues](https://github.com/pnpm/pnpm/issues)
- [Support — GitHub Discussions](https://github.com/pnpm/pnpm/discussions)
- [Contact — Discord](https://chat.pnpm.io/)
- [X — @pnpmjs](https://x.com/pnpmjs)
- [Contact — Bluesky](https://bsky.app/profile/pnpm.io)
- [YouTube — @pnpmjs](https://www.youtube.com/@pnpmjs)
- [StackOverflow — `pnpm` tag](https://stackoverflow.com/questions/tagged/pnpm)
- [SDK — `pnpm` on npm](https://www.npmjs.com/package/pnpm)
- [SDK — `@pnpm/exe` standalone binary](https://www.npmjs.com/package/@pnpm/exe)
- [Integrations — pnpm/action-setup (GitHub Action)](https://github.com/pnpm/action-setup)
- [Integrations — pnpm/setup (multi-runtime GitHub Action)](https://github.com/pnpm/setup)
- [Integrations — pnpm/exec](https://github.com/pnpm/exec)
- [Pricing — Open Collective](https://opencollective.com/pnpm)
- [Pricing — GitHub Sponsors](https://github.com/sponsors/pnpm)
- [Blog](https://pnpm.io/blog)
- [FAQ](https://pnpm.io/faq)
- [Showcase — Who uses pnpm](https://pnpm.io/uses)
- [Documentation — pnpm RFCs](https://github.com/pnpm/rfcs)

## Features

- **Content-addressable store** — Each package version is stored once on disk and hard-linked into projects, saving substantial disk space across all projects on the machine.
- **Strict, non-flat node_modules** — A symlinked `node_modules` layout means packages can only access dependencies they explicitly declare, catching phantom-dependency bugs at install time.
- **Up to 2x faster installs** — Optimized installation pipeline that is consistently faster than npm and Yarn on cold and warm installs, especially for large monorepos.
- **Native workspace and monorepo support** — First-class workspaces driven by `pnpm-workspace.yaml` with the workspace protocol, recursive commands, package filtering, and Catalogs for shared version pinning.
- **Catalogs** — Centralized dependency-version management across a monorepo so every package shares a single pinned version of common dependencies.
- **Deterministic lockfile** — `pnpm-lock.yaml` captures the exact resolved dependency graph, peer relationships, and patches for reproducible installs.
- **Supply-chain safety controls** — `minimumReleaseAge` to delay adoption of brand-new package versions, `ignoredBuiltDependencies` and `onlyBuiltDependencies` to opt into lifecycle scripts, and removal of `postinstall` scripts by default.
- **pnpm patch** — Built-in workflow to patch installed dependencies and persist the patch in `pnpm.patchedDependencies` without forking the package.
- **pnpm overrides and packageExtensions** — Repository-level dependency rewriting and peer-dependency repair without forking upstream packages.
- **`.pnpmfile.cjs` hooks** — `readPackage` and `afterAllResolved` hooks let you programmatically rewrite manifests during resolution and installation.
- **`pnx` (dlx) and `pnpm exec`** — Run packages without installing them globally, with caching in the store.
- **Built-in runtime management** — `pnpm env install` lets you manage Node.js (and other JavaScript runtime) versions directly through pnpm.
- **Cross-platform standalone binary** — Distributed as `@pnpm/exe`, a single self-contained executable that does not require an existing Node.js installation.
- **Corepack-compatible** — First-class support for Node.js Corepack so projects can pin a specific pnpm version via `packageManager` in `package.json`.
- **MIT-licensed open source** — Permissively licensed and developed in the open on GitHub with an Open Collective sponsorship model.

## Use Cases

- **Large JavaScript monorepos** — Manage hundreds of interdependent packages with a single shared lockfile, the workspace protocol, Catalogs, and recursive commands.
- **CI/CD pipeline acceleration** — Cut install time substantially in CI by leveraging the content-addressable store and the official pnpm/action-setup GitHub Action.
- **Disk-constrained developer machines** — Share a single copy of each package version across every project on a machine, dramatically reducing disk usage compared to npm or Yarn.
- **Supply-chain hardening** — Use `minimumReleaseAge`, `ignoredBuiltDependencies`, and strict lifecycle script policy to reduce exposure to malicious or compromised npm packages.
- **Phantom dependency detection** — The strict non-flat `node_modules` layout surfaces undeclared dependencies during local development rather than in production.
- **Reproducible builds** — `pnpm-lock.yaml` plus `pnpm.overrides` and `pnpm.patchedDependencies` make installations byte-reproducible across machines.
- **Multi-runtime JavaScript projects** — Use the pnpm/setup action and `pnpm env` to standardize Node.js, Bun, or Deno versions across teams.

## Integrations

- **Node.js Corepack** — pnpm is one of the package managers managed by Corepack, enabling version pinning via `packageManager` in `package.json`.
- **GitHub Actions** — Official `pnpm/action-setup` and `pnpm/setup` actions for installing pnpm and a JavaScript runtime in a single step.
- **Changesets** — Recommended workflow tool for versioning and publishing packages in pnpm monorepos.
- **Microsoft Rush** — Rush uses pnpm under the hood for large monorepos at Microsoft and elsewhere.
- **Nx** — Nx integrates with pnpm workspaces for monorepo task orchestration and caching.
- **Turbo (Turborepo)** — First-class pnpm workspace support for incremental builds and remote caching.
- **Docker** — Official guidance for using pnpm in Docker images, including the standalone binary and lockfile-aware multi-stage builds.
- **Verdaccio and private registries** — Works with any npm-compatible registry including Verdaccio, JFrog Artifactory, GitHub Packages, and AWS CodeArtifact.
- **Bit** — Bit Cloud (a Platinum sponsor) uses pnpm as a foundation for component-based development.
- **Vercel, Netlify, Cloudflare Pages** — First-class support for pnpm in major JavaScript deployment platforms with workspace-aware installs.

## Maintainers

- **Kin Lane** — [apievangelist.com](https://apievangelist.com)
