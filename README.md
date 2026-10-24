<p align="center">
  <img src="assets/kora-icon.png" width="112" height="112" alt="Kora">
</p>

# Kora

A Mac app for coding agents: Claude Code, Codex, OpenCode and Antigravity, with a local code graph that keeps their context small and a swarm of workers that takes the legwork off your main agent.

**[Download Kora for Mac](https://github.com/agilkatakam/kora/releases/latest/download/Kora-arm64.dmg)** · Apple Silicon · macOS 13.5 or later · at least one of the four agents · [All releases](https://github.com/agilkatakam/kora/releases)

## What it does

- **Chat with your coding agents, per project.** Claude Code, Codex, OpenCode and Antigravity, side by side in one app.
- **Code graph.** Click to index a project (nothing is indexed until you ask). Your agents look code up in a local map instead of re-reading files: fewer tokens, faster answers.
- **Swarm.** Claude, Codex or OpenCode leads. Cheaper workers do the legwork in their own git worktrees, in live panes you can watch and steer. You approve every worker.
- **Plan mode.** Each agent plans in its own native mode, with the graph behind it.
- **"Kora saved you $X".** A meter of what the graph and routing saved, estimated at each model's own API list price (Claude at Anthropic's, GPT at OpenAI's, Gemini at Google's) and refreshed automatically for new models. It is an estimate, not a bill.
- **Your plans in one place.** Usage of your Claude, Codex and Antigravity plans, side by side.
- **Local.** No Kora account, no analytics. See [Privacy](#privacy).
- **Coming soon: Kora**, a team of assistants with memory, routines and a browser.

## Install

1. Download **Kora-arm64.dmg** from the [latest release](https://github.com/agilkatakam/kora/releases/latest).
2. Open it and drag Kora to Applications. It is signed and notarized, so it opens like any Mac app.
3. Open Kora and sign in to any of the agents you use. Claude has a one-click login on the first screen; the others use their own (`codex login`, `opencode auth login`, install `agy` for Antigravity), and the first screen lists them. One working agent is enough.

## Privacy

Kora has no account and no analytics or telemetry. Your code, chats and the code graph stay on your Mac. Your agents talk to their own providers exactly as they would without Kora.

The network calls Kora itself makes:

- the update check, against this repository's releases;
- the public model price list ([models.dev](https://models.dev)), at most once a day, so the savings meter knows each model's price;
- for Swarm, the list of free worker models (models.dev and OpenCode Zen's public model list).

None of them carries anything about you, your code or your chats.

## Updates

Kora checks for updates hourly and downloads them in the background. When one is ready, **Restart to update** appears at the bottom of the sidebar. You can also check by hand from **Settings → About** or **Kora → Check for Updates…**.

## Report a bug

**Help → Report a Bug…** opens the [bug form](https://github.com/agilkatakam/kora/issues/new?template=bug_report.yml). **Help → Show Logs in Finder** reveals `server.log`; skim it for anything private before you attach it. For a feature request use the [feature form](https://github.com/agilkatakam/kora/issues/new?template=feature_request.yml), or start a thread in [Discussions](https://github.com/agilkatakam/kora/discussions). Security issues: see [SECURITY.md](SECURITY.md).

## Uninstall

Quit Kora, run `kora uninstall` in Terminal (add `--purge` to also delete your chats, settings and code graph), then drag Kora from Applications to the Trash.

---

This repository holds Kora's releases, the update feed and issues. Kora is open source under the MIT licence: the source is at [Koragraph/Kora](https://github.com/Koragraph/Kora). © 2026 Akhil Katakam and the Kora contributors. Open-source notices are in `Kora.app/Contents/Resources/THIRD_PARTY_NOTICES.md`.
