# Q3 Code (Gamma)

**Q3 Code (Gamma)** is the bleeding-edge, experimental distribution of T3 Code. It integrates high-demand community PRs and advanced capabilities while staying continuously synchronized with upstream [`pingdotgg/t3code`](https://github.com/pingdotgg/t3code) `main`.

Works with your subscriptions on **Google Antigravity**, **OpenAI Codex**, **Anthropic Claude Code**, **Cursor**, **Grok Build**, and **OpenCode**.

---

## ⚡ What's in Q3 Code (Gamma)?

Q3 Code (Gamma) includes powerful experimental features on top of upstream T3 Code:

* 🌌 **Google Antigravity (`agy`) Integration:** Direct integration for the Antigravity CLI adapter, offering streaming turns, Gemini 3.7 Flash, Gemini 2.5 Pro, thinking token inspection, and reasoning effort controls (`low`, `medium`, `high`).
* 🔓 **Cursor Provider Unlocked:** Enabled by default without early access restrictions.
* 👥 **Seamless Multi-Subscription / Multi-Account Switching:** Run multiple independent subscriptions (e.g. personal and work Codex/Claude accounts) concurrently with separate auth vaults, while keeping all skills, plugins, and configs 100% shared.
* 🔄 **Continuous Upstream Sync:** Automatically tracks and merges upstream `pingdotgg/t3code` main releases and improvements daily via GitHub Actions.

---

## Providers & Setup

Install and authenticate your preferred provider CLI before launching:

* **Antigravity:** Install [Antigravity CLI](https://antigravity.google) (`agy`) and configure credentials.
* **Codex:** Install [Codex CLI](https://developers.openai.com/codex/cli) and run `codex login`.
* **Claude:** Install [Claude Code](https://claude.com/product/claude-code) and run `claude auth login`.
* **Cursor:** Install [Cursor CLI](https://cursor.com/cli) and run `agent login`.
* **Grok Build:** Install [Grok Build CLI](https://x.ai/cli) and run `grok login`.
* **OpenCode:** Install [OpenCode](https://opencode.ai) and run `opencode auth login`.

---

## Quickstart (Development)

### 1. Install Dependencies

```bash
pnpm install
```

### 2. Run Dev Server & Web App

```bash
pnpm run dev
```

### 3. Build

```bash
pnpm run build
```

---

## Upstream Synchronization

Q3 Code includes an automated GitHub Actions workflow (`.github/workflows/sync-upstream.yml`) that fetches and merges updates from `pingdotgg/t3code:main` to ensure you always have the latest server fixes, UI speedups, and protocol upgrades while preserving Q3 Gamma experimental features.

---

## License & Credits

Built on top of the open-source [T3 Code](https://github.com/pingdotgg/t3code) project by Theo Browne and the ping.gg team. Licensed under MIT.
