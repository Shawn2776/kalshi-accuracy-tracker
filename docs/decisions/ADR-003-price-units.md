# ADR-003: Price Storage Units

Status: Accepted | Date: 2025-09-04

## Decision

Store prices as integer **cents** (0–100). Avoids FP rounding issues; compact and precise for probability space.
