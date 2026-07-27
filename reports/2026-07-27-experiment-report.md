# Discover Tab Beta — Weekly Report (2026-07-27)

**On track, but the read is stale.** Tab open rate cleared the 4.0% target for a full week on both splits (weekday 4.1%, weekend 4.6%) with both guardrails well clear — however no data has landed since 07-20, so this is the same window the 07-22 report covered.

*Window: most recent 7 days of data (07-14→07-20) vs previous 7 (07-07→07-13). Beta figures unless noted. Weekend = Sat/Sun — 07-18/19 this week, 07-11/12 last.*

## Metrics

| Metric | Target | This week | Last week | Direction |
|---|---|---|---|---|
| Open rate — weekday | ≥4.0% | 4.1% | 3.5% | ↑ toward (first week clearing) |
| Open rate — weekend | ≥4.0% | 4.6% | 4.1% | ↑ toward |
| Saves/session — weekday | ≥0.29 (0.31 −5%) | 0.30 (−1.9% vs baseline) | 0.30 (−3.5%) | ↑ toward |
| Saves/session — weekend | ≥0.29 (0.31 −5%) | 0.57 (1.85× baseline) | 0.59 (1.89×) | ↓ slightly, far above floor |
| Scroll depth (P8) — weekday | ≥40% | 41.3% | 41.2% | → flat, above target |
| Scroll depth (P8) — weekend | ≥40% | 41.8% | 40.1% | ↑ toward |

Control open rate this week: 1.4% weekday / 1.4% weekend — beta runs ~3× control on both splits. Within each split beta also leads control on saves (weekday +4.3%, weekend +4.5%), so the weekend lift is a day-of-week effect, not a beta effect.

## Guardrails — both clear

| Guardrail | Limit | This week | Last week |
|---|---|---|---|
| Article depth delta (tab-visit sessions) | ≥ −3% | −0.9% avg, −1.5% worst day | −0.7% avg, −1.7% worst day |
| Crash rate delta vs control | within ±0.1pp | +0.01pp avg, +0.04pp worst day | +0.01pp avg, +0.04pp worst day |

Crash delta stayed inside half the limit every day. Depth's worst single day (−1.7%, 07-07) used just over half the −3% allowance, but no day in either window came close to breach.

## What changed

- **Nothing in the data.** The CSV still ends 07-20; days 07-21 through 07-26 are absent. Every figure above restates the 07-22 report. Rows for 07-06→07-20 are complete — two cohorts per day, no gaps.
- On that window, the primary metric is genuinely sustained rather than weekend-carried: weekday open rate rose 3.5% → 4.1% and clears the target on its own, which it did not do last week.
- Saves recovered slightly on weekdays (−3.5% → −1.9% vs the 0.31 baseline) while weekends held at ~1.9× baseline. Article-depth delta drifted marginally more negative on average (−0.7% → −0.9%) with a less severe worst day, so there is still no visible substitution cost.

## Watch next week

- **Unblock the pipeline first.** Six missing days mean the "sustained over a full week" criterion has not been re-tested since 07-20; this verdict is a week old and should not be used for a ship decision as-is.
- Weekday open rate clears by only 0.1pp, and two of seven days (Tue 4.0%, Wed 3.9%) sat at or below target. Confirm the margin holds once fresh days land rather than reverting toward 3.5%.
