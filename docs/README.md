# Kalshi Accuracy Tracker

Public, open-source dashboard that measures how well Kalshi market odds match real outcomes.
It ingests markets, captures pre-close probabilities, records outcomes, and publishes
calibration curves, Brier scores, and CSV exports.

> Status: **Planning phase (no prod code yet)** — see [/docs](./docs)

## Stack

Next.js (App Router) • Neon Postgres • Prisma • Recharts

## Why

Independent, transparent evaluation of event-market probabilities.

## Project Docs

- [Charter](./docs/charter.md)
- [Methods](./docs/methods.md)
- [Architecture Overview](./docs/architecture/overview.md)
- [Runbooks](./docs/runbooks/)
- [ADRs](./docs/decisions/)
- [Risk Register](./docs/risk-register.md)

## Roadmap (MVP)

- Ingest binary markets & pre-close snapshots
- Outcomes + scoring (Calibration/Brier)
- Dashboard + CSV exports
- Methods & disclaimers

## Disclaimer

Research project; **not** trading advice. Respect third-party ToS and rate limits.
