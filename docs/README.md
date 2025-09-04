# Kalshi Accuracy Tracker

These are the canonical, versioned documents for the project. All specs and decisions live here and are updated via PRs.

## Structure

- `charter.md` — approved project charter (scope, goals, success)
- `methods.md` — formulas & data handling (calibration, Brier, binning)
- `metrics.md` — definitions of computed metrics & how to interpret
- `architecture/overview.md` — components & data flow
- `runbooks/` — operational docs for ingestion & analytics
- `decisions/` — ADRs (Architecture Decision Records)
- `governance/contributing.md` — PR & documentation rules
- `risk-register.md` — open risks & mitigations
- `glossary.md` — domain vocabulary used in the project

## Contributing to Docs

- Treat docs like code. Any feature/change that affects behavior must update docs in the same PR.
- Use ADRs for non‑obvious decisions. New decisions supersede old ones; never silently edit an Accepted ADR.
