# Metrics — Definitions & Interpretation

## Brier Score

- Definition: mean((p - y)^2), lower is better (0 = perfect).
- Interpretation: compares forecast probability to binary outcome; penalizes confident errors.

## Calibration (Reliability)

- Definition: group predictions into bins; compare bin midpoint vs observed frequency.
- Good calibration ≈ points lie on diagonal; deviations indicate over/under‑confidence.

## Sharpness (Distribution)

- Histogram of forecast probabilities; sharper distributions (more mass near 0/1) indicate more decisive markets but say nothing about correctness on their own.

## Reporting

- Overall + per‑category Brier & calibration; include **n** per bin and binomial CIs where feasible.
