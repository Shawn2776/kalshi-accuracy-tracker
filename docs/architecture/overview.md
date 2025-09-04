# Architecture Overview

## Components

- **Frontend**: Next.js (App Router) + Recharts
- **Backend**: Next.js API routes for ingestion & analytics (cron‑triggered)
- **DB**: Neon Postgres via Prisma ORM

## Data Flow

1. Discover markets (paginate) → upsert `Market`
2. For markets closing soon → fetch minute candles (last 30 min) → compute **pre‑close price** → write `MarketPrice(kind=preclose)`
3. Detect settlement → write `MarketOutcome(outcome ∈ {0,1})`
4. Nightly: aggregate & cache metrics → serve to dashboard

## ADRs (decision log)

- **ADR‑001**: Closing probability = last 1‑minute candle close ≤30 min pre‑close
- **ADR‑002**: Calibration bins = 20 bins (5% width)
- **ADR‑003**: Price units = cents (int 0..100)
- **ADR‑004**: Serverless cron hits HTTP jobs (portable on Vercel/GitHub Actions)

## Observability

- Structured logs; job run summaries (rows added, failures)
- Error notifications (e.g., email/webhook) optional post‑MVP
