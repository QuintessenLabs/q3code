# Q3

Q3 is an "agent harness control surface" and an experimental distribution of [T3 Code](https://github.com/pingdotgg/t3code). This repository is kept fully in sync with upstream T3 Code `main` while shipping early-access capabilities and high-demand community PRs. It enables control of the agents on your machine with a best-in-class mobile app ([iOS](https://apps.apple.com/us/app/t3-code-remote-claude-more/id6787819824), [Android](https://play.google.com/store/apps/details?id=com.t3tools.t3code)), [web app](https://app.t3.codes) and [Electron-based desktop app](https://t3.codes).

Works with your subscriptions on Google Antigravity, Claude Code, Codex, Cursor, Grok Build, and OpenCode. If they're set up on your computer, Q3 can control them.

## "Wait, what are you selling me?"

Nothing. Q3 is an experimental fork of T3 Code. We love the work Theo and the ping.gg team are doing, but we wanted a place to test and ship high-demand community PRs while keeping the codebase fully in sync with upstream `main`.

## What's in Q3?

Q3 includes a few experimental additions on top of upstream T3 Code:

- **Google Antigravity (`agy`):** Native adapter integration for Google Antigravity with full streaming turns, Gemini 3.7 Flash / 2.5 Pro models, and reasoning effort controls.
- **Cursor Unlocked:** Enabled by default without early access gating.
- **Multi-Account Subscriptions:** Run multiple subscriptions for the same provider (e.g. personal and work Codex accounts) concurrently without manual path hacking or logging out. All your skills, plugins, and configs stay unified.
- **1-Click Setup in Providers UI:** Instead of manually running terminal install and login commands, manage your provider CLIs and auth directly from the Providers panel.
- **Fully in Sync with Upstream:** An automated daily sync workflow tracks and merges upstream `pingdotgg/t3code` changes so all upstream fixes, performance improvements, and protocol features land here automatically.

## Installation

> [!WARNING]
> Q3 currently supports Antigravity, Codex, Claude, Cursor, Grok Build and OpenCode. You can install and authenticate providers directly with one click inside the Q3 Providers panel, or run their respective CLI commands:
>
> - Antigravity: install [Antigravity CLI](https://antigravity.google) (`agy`)
> - Codex: install [Codex CLI](https://developers.openai.com/codex/cli) and run `codex login`
> - Claude: install [Claude Code](https://claude.com/product/claude-code) and run `claude auth login`
> - Cursor: install [Cursor CLI](https://cursor.com/cli) and run `agent login`
> - Grok Build: install [Grok Build CLI](https://x.ai/cli) and run `grok login`
> - OpenCode: install [OpenCode](https://opencode.ai) and run `opencode auth login`

### Try it out (install-free)

The easiest way to test Q3 is to run the server in your terminal (requires Node.js 22.16+, 23.11+, or 24.10+):

```bash
pnpm run dev
```

This will launch Q3's backend on your machine as well as the local web app to control your agents.

### Desktop app

Install the latest version of the desktop app from [GitHub Releases](https://github.com/QuintessenLabs/q3code/releases), or from your favorite package registry:

#### Windows (`winget`)

```bash
winget install T3Tools.T3Code
```

#### macOS (Homebrew)

```bash
brew install --cask t3-code
```

#### Arch Linux (AUR)

Stable:

```bash
yay -S t3code-bin
```

Nightly:

```bash
yay -S t3code-nightly-bin
```

The AUR packaging is maintained in this repository under [`packaging/aur`](./packaging/aur).

## Some notes

We are very very early in this project. Expect bugs.

We are (mostly) not accepting contributions yet. Small fixes may be considered. Big features will not be.

## Documentation

Full docs live in [docs/](./docs). There's no docs site yet.

- [Install and first run](./docs/user/install.md)
- [Permission modes](./docs/user/permission-modes.md)
- [Keyboard shortcuts](./docs/user/keybindings.md)
- [Customize a project icon](./docs/user/project-settings.md)
- [Remote access from a phone or another machine](./docs/user/remote-access.md)
- [Keeping app and server in sync](./docs/user/updating.md)
- [Source control integrations](./docs/user/source-control.md)
- Multiple accounts: [Codex](./docs/user/providers-codex.md) · [Claude](./docs/user/providers-claude.md)
- Linux: [run T3 Code as a background service](./docs/user/background-service.md)

Building from source? Start at [docs/internals/overview.md](./docs/internals/overview.md).

## If you REALLY want to contribute still.... read this first

### Install `vp`

Q3 uses Vite+ so you'll need to install the global `vp` command-line tool.

#### macOS / Linux

```bash
curl -fsSL https://vite.plus | bash
```

#### Windows

```bash
irm https://vite.plus/ps1 | iex
```

Checkout their getting started guide for more information: https://viteplus.dev/guide/

### Install dependencies

```bash
vp i
```

Read [CONTRIBUTING.md](./CONTRIBUTING.md) before reporting a bug or opening a PR.

Have a feature request? Start an [Ideas discussion](https://github.com/pingdotgg/t3code/discussions/categories/ideas).

Need support? Join the [Discord](https://discord.gg/jn4EGJjrvv).
