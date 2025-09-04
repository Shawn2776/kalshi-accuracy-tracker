# ADR-001: Closing Probability Definition

Status: Accepted | Date: 2025-09-04

## Context

We need a consistent, auditable definition of “closing probability”.

## Decision

Use the **last 1‑minute candle close** within **≤30 minutes** before official close.
Fallback: last available candle in that window. Store as **cents** [0..100].

## Consequences

- Deterministic & reproducible
- Less sensitive to microstructure noise than last trade

* If no candles in window, rely on fallback and flag low‑confidence
