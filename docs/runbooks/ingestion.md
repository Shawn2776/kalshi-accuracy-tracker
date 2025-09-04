# Runbook — Ingestion

## Schedules

- Discover markets: hourly
- Pre‑close snapshots: tighter cadence near scheduled close windows
- Outcome sync: every 30–60 min

## Procedure

1. Fetch paginated markets; idempotent upsert
2. Identify markets within T‑30min of close; fetch 1‑min candles; compute pre‑close
3. Detect settled markets; write outcomes (0/1)
4. Log counts, durations, and errors; retry with backoff

## Backfill

- Range‑based historical job; idempotent writes; checkpoint cursors

## Failure Handling

- Network/API errors → exponential backoff + jitter
- Partial writes → transaction per market batch; resume from cursor
