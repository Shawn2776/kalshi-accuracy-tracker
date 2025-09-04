# Methods

## Metrics

- **Brier score**: mean((p - y)^2)
- **(Optional) Log loss**: -[y ln p + (1-y) ln(1-p)]
- **Calibration**: 20 bins (5% width). Observed YES rate vs bin midpoint.

## Data Handling Rules

- **Price units**: store probability as integer **cents** [0..100].
- **Closing probability**: last **1‑minute candle close** within **≤30 min** pre‑close; fallback = last available candle in that window. (ADR‑001)
- **Outcomes**: 1 for YES, 0 for NO once market is settled.
- **Exclusions**: Markets without a valid pre‑close snapshot are flagged; shown in separate counts.

## Caveats

- Microstructure effects near close may bias last‑trade ticks; candle close chosen for robustness.
- Mixing categories can mask regime differences; always show per‑category views.
