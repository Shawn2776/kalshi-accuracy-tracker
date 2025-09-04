# Project Charter — Kalshi Accuracy Tracker

## Problem

There is no independent, transparent tracker showing how well Kalshi event odds calibrate to real outcomes across categories and time.

## Goal (MVP)

Ship a public site that:

- Ingests Kalshi binary markets and prices
- Records **pre‑close probability** and **final outcome** per market
- Publishes **calibration curves**, **Brier scores**, and CSV exports
- Explains methodology on a public **Methods** page

## Scope (MVP)

**In:** binary markets ingestion; pre‑close snapshot; settlement detection; calibration + Brier; dashboard (calibration + histogram + table + CSV); serverless cron; disclaimers

**Out:** auth/users, alerts, live streaming ticks, mobile apps, paywalls/monetization

## Success Criteria

- **Freshness:** outcomes reflected ≤ **3 hours** after settlement
- **Coverage:** ≥ **1,000** settled binary markets across ≥ 3 categories
- **Quality:** reliability plot with **20 bins** (5% width) + overall & per‑category Brier
- **Reproducibility:** metrics recompute identically from DB snapshot + commit
- **Transparency:** public Methods page + downloadable CSVs

## Constraints

- Respect API ToS & rate limits; keep cloud costs low (serverless)
- Non‑advisory research; clear disclaimers; transparent methodology

## Top Risks & Mitigations

- **Settlement detection ambiguity** → cross‑check status & price behavior; manual override table
- **Data gaps near close** → 30‑min fallback window; low‑confidence flag
- **API changes/rate limits** → centralized client with retries/backoff; configurable endpoints
