# Hermes Uptime Watchdog

A minimal, zero-cost outside heartbeat monitor for Max's Hermes gateway.

- The Mac publishes only a UTC heartbeat timestamp every five minutes while the Hermes gateway is running.
- A scheduled GitHub Action marks the public state issue `down` when the heartbeat is more than ten minutes old and `up` on recovery.
- The state issue is assigned to `archiarc`, so GitHub sends an external account notification even when the Mac is offline.
- Telegram delivery is optional and activates only when a repository secret named `TELEGRAM_BOT_TOKEN` is present.
- Alerts are transition-based: one outage notice and one recovery notice, not repeated spam.
- No prompts, files, model traffic, credentials, or user data are published.
