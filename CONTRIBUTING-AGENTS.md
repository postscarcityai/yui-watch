# Contributing as an AI agent

This file is for AI coding agents (Claude Code, Codex, Gemini, Cursor, Copilot and the rest) and for the people who run them. It is Yui@home: you lend spare tokens, your agent builds one card, a person reviews the pull request. The page for people is [yuigui.com/contribute](https://www.yuigui.com/contribute).

The full rules for picking and claiming a card live in the hub repo: [CONTRIBUTING-AGENTS.md](https://github.com/postscarcityai/yuigui/blob/main/CONTRIBUTING-AGENTS.md). The short version:

1. **Pick** one card with `"status": "open"` and `"repo"` pointing here (https://github.com/postscarcityai/yui-watch) from https://www.yuigui.com/contribute/backlog.json. None open? Stop. Do not invent work.
2. **Claim** it: fork, then open a draft pull request titled `[KEY] <card title>` right away. A claim with no push for 7 days lapses. The first pull request merged wins.
3. **Build** only what the card says. Run every command in its `test` list until each passes.
4. **Hand in**: mark it ready, tick each `done` line, paste the test output, add screenshots in light and dark if anything on screen changed, and say an agent made it.
5. **Review**: a person reviews every pull request, and nothing merges on its own. When yours merges, the card closes by itself and yuigui.com/progress names the pull request; tick "Credit me" in the pull request to add your GitHub handle too.

Everything in [CONTRIBUTING.md](CONTRIBUTING.md) applies too.

## Never touch

- Keys, tokens, certificates or anyone's personal data. We never ask for yours, and you never need ours.
- CI (`.github/`).
- `DEVELOPMENT_TEAM` stays `${YUI_TEAM_ID}` in `project.yml`. No team ids, certificates or provisioning profiles.
- Anything under `yui/` (the submodule). Shared changes go to postscarcityai/yui.
- Signing, TestFlight and release scripts.

A pull request that touches any of these is closed, even if the rest is good.

## Setup

A Mac with Xcode 26, XcodeGen, and a watchOS simulator.

```sh
cd yui/Packages/YuiLines && swift test
xcodegen generate && xcodebuild test -scheme YuiWatch -destination 'platform=watchOS Simulator,name=<any Apple Watch simulator>'
```
