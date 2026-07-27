# Discover Tab Beta — Weekly Report (2026-07-27)

**On track.** Tab open rate held above the 4.0% target for a full week on both cohorts (weekday 4.1%, weekend 4.6%) with both guardrails clear — but no new data has landed since 07-20, so this is the same window the 07-22 report covered.

*Window: most recent 7 days of data (07-14→07-20) vs previous 7 (07-07→07-13). Beta figures unless noted. Weekend = Sat/Sun (07-18/19 this week; 07-11/12 last).*

## Metrics

| Metric | Target | This week | Last week | Direction |
|---|---|---|---|---|
| Open rate — weekday | ≥4.0% | 4.1% | 3.5% | ↑ toward (first week clearing) |
| Open rate — weekend | ≥4.0% | 4.6% | 4.1% | ↑ toward |
| Saves/session — weekday | ≥0.29 (0.31 −5%) | 0.30 (−1.9% vs baseline) | 0.30 (−3.5%) | ↑ toward |
| Saves/session — weekend | ≥0.29 (0.31 −5%) | 0.57 (~1.9× baseline) | 0.59 | ↓ slightly, far above floor |
| Scroll depth (P8) | ≥40% | 41.4% | 40.9% | ↑ toward |

Control open rate this week: 1.4% weekday / 1.4% weekend — beta runs ~3× control on both splits. Beta also leads control on saves within each split (weekday +4.3%, weekend +4.5%).

## Guardrails — both clear

| Guardrail | Limit | This week | Last week |
|---|---|---|---|
| Article depth delta (tab-visit sessions) | ≥ −3% | −0.9% avg, −1.5% worst day | −0.7% avg, −1.7% worst day |
| Crash rate delta vs control | within ±0.1pp | +0.01pp avg, +0.04pp worst day | +0.01pp avg, +0.04pp worst day |

No day in either window came within half the limit on either guardrail.

## What changed

- **Nothing in the data.** The CSV still ends 07-20; days 07-21 through 07-26 are absent, so the freshest available window is unchanged from the 07-22 report and every figure above is a restatement. Rows for 07-06→07-20 are complete (two cohorts per day, no gaps).
- On that window, the primary metric is genuinely sustained rather than weekend-carried: weekday open rate rose 3.5% → 4.1% and clears the target on its own, which it did not do last week.
- Saves recovered slightly on weekdays (−3.5% → −1.9% vs the 0.31 baseline) while weekends stayed ~1.9× baseline. Article-depth delta drifted marginally more negative on average (−0.7% → −0.9%) with a less severe worst day, so there is still no visible substitution cost.

## Watch next week

- **Get the pipeline unblocked first.** Six days of missing data means the "sustained over a full week" criterion has not actually been re-tested since 07-20; the verdict above is a week stale.
- Weekday open rate clears by a thin 0.1pp, and two of the seven days (Tue 4.0%, Wed 3.9%) sat at or below target. Confirm the margin holds once fresh days land rather than reverting toward 3.5%.
