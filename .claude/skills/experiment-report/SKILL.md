---
name: experiment-report
description: Write the weekly experiment status report from the data in this repo. Use when asked to run the weekly report, check the experiment, or report on the Discover beta.
---

# Experiment Report

Write the weekly status report for the experiment defined in `data/experiment-config.md`, using `data/discover-beta-daily.csv`. Save it as `reports/YYYY-MM-DD-experiment-report.md` (today's date) and nothing else.

## Process

1. Read `data/experiment-config.md` fully: the success criteria, guardrails, and reporting notes are the spec for this report.
2. Read the CSV. Compute, for the most recent 7 days of data, beta vs control:
   - Tab open rate (vs the 4.0% target), with the weekday/weekend split reported separately per the config's notes
   - Saves per session vs the baseline (flat-to-down-5% rule)
   - Scroll depth vs the 40% target
   - Both guardrails (article depth delta, crash rate delta)
3. Compare against the previous 7 days: is each metric trending toward or away from its target?

## Report format

1. **Verdict line** at the very top: one sentence, plain language. "On track", "Mixed", or "Guardrail breach" plus the single most important fact.
2. **Guardrails** section, first if anything is breached, otherwise after the metrics.
3. **Metrics table**: metric, target, this week, last week, direction. Weekend/weekday split shown for open rate and saves.
4. **What changed**: 2-3 bullets, plain sentences.
5. **Watch next week**: 1-2 bullets.

Keep the whole report under a page. Numbers rounded to one decimal where percentages, two where ratios.

## What this skill should never do

- Never average weekend and weekday cohorts together silently (the config forbids it).
- Never bury a guardrail breach below the fold. Breach means it leads.
- Never invent a number that isn't computable from the CSV. If data is missing for a day, say so in "What changed".
- Never edit anything outside `reports/`.
