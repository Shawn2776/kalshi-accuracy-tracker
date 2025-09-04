# Runbook — Analytics & Aggregations

## Nightly Job

- Compute per‑category & overall: Brier, calibration bins, counts
- Store in materialized tables or cache for quick dashboard loads

## Recompute Triggers

- Schema/version change
- Methods change (recorded in ADR)
- Backfill completion

## QA Checklist

- Spot‑check 50 random markets per week
- Compare bin frequencies to raw outcomes per bin
- Validate counts vs ingestion logs
