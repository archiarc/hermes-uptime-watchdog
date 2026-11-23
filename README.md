# Hermes Uptime Watchdog

A minimal, zero-cost outside heartbeat monitor for Max's Hermes gateway.

- The Mac publishes only a UTC timestamp and `status: up` every five minutes while the Hermes gateway is running.
- A scheduled GitHub Action alerts the private Hermes HQ Telegram thread when the heartbeat is more than ten minutes old.
- Alerts are transition-based: one outage notice and one recovery notice, not repeated spam.
- No prompts, files, model traffic, credentials, or user data are published.
