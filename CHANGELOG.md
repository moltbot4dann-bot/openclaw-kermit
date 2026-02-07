# OpenClaw Manual Changes & Ops Log

This file tracks manual system-level changes, custom scripts, and architectural decisions made outside of the standard `openclaw.json` configuration.

## 2026-02-07
### System Configuration
- **Gateway Watchdog:** Implemented a `systemd` user timer and service (`openclaw-watchdog`) to monitor gateway health every 2 minutes. Restarts gateway after 10 minutes of unresponsiveness (extended to 30 minutes if `npm` or `install` is detected).
- **Git Identity:** Configured global git identity (Kermit <moltbot4dann@gmail.com>).
- **Model Switch:** Switched primary model to `openai/gpt-5.3-codex`.

### Automation
- **GitHub Sync:** Created `openclaw-kermit` repo to store redacted config and workspace behavior files.
- **Version Notifier:** (Pending) Scheduling twice-daily checks (8 AM / 8 PM) for new OpenClaw versions via cron.

### Infrastructure
- **GitHub Auth:** Authenticated `gh` CLI for account `moltbot4dann-bot`.
- **New Repos:** Created `open-chore` and `openclaw-kermit` on GitHub.
