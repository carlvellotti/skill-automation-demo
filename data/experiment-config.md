# Experiment: Discover Tab Beta

Status: running · Started: 2026-07-06 · Owner: Maya Chen

## What we're testing

Discover tab beta (editorial-curated fallback), gated to app version 14.2+, 5% of eligible users.

## Success criteria

- **Tab open rate** (primary): 4.0% of eligible DAU or higher, sustained over a full week
- **Saves per session**: at least flat vs the 0.31 baseline (no decline beyond 5%)
- **Scroll depth**: 40% or more of tab sessions reach position 8

## Guardrails

- Article page depth for sessions that include a tab visit must not fall more than 3% vs baseline (substitution check)
- Crash rate for 14.2+ beta cohort must stay within 0.1pp of control

## Reporting notes

- Weekend and weekday behavior differ (weekend cohorts save ~2x more). Call out the split, never average across it silently.
- Data lands in `data/discover-beta-daily.csv` (one row per day per cohort).
- If any guardrail is breached, lead the report with it. Never bury a guardrail.
