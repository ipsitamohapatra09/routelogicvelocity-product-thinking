# Experimentation Plan

> **Module 5 · ★ Deliverable 5.** Repo file `05-experimentation/experimentation-plan.md` — part of your submission.
> Do the lab in the **Module 5 · Exercise Guide** (linked from the Module 5 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Experimentation Plan** slide of your Module 6 final deck.

## Overview

_A high-level validation strategy to test your hypothesis before full-scale development._

Before building B1 One-Click Compliance Checklist for every RouteLogic Velocity account, we run a 50/50 A/B test with frontline coordinators at 3 pilot accounts. Today, coordinators spend 14.6 minutes a day logging compliance checks against a 3-minute benchmark (CSAT 2.2), and only 31% complete the dispatch workflow through shift handoff in the product. The test checks whether one pre-filled compliance screen cuts that time enough to ship, without coordinators logging fewer checks or accepting wrong pre-filled values.

## What you're testing

| Element | Detail |
|---|---|
| Hypothesis under test | I believe the One-Click Compliance Checklist for frontline coordinators will result in coordinators completing compliance logging inside the product instead of through texts, WhatsApp and paper, measured by a 50% reduction in median time per completed compliance check (14.6 to about 7 minutes) within 4 weeks. We will protect checks logged per coordinator-day and the post-submission correction rate. |
| Experiment design (A/B, etc.) | A/B test, 50/50 split randomized by coordinator within each of the 3 pilot accounts (~30 coordinators per arm, about 600 coordinator-days each). **Control (A):** today's multi-screen admin form. **Variant (B):** one pre-filled screen with judgment questions first and stale values to confirm (PRD Screens 1–3, FR1–FR7), with the timer, "Confirm all unchanged" and progress panel removed so pre-fill is the single change. A 2-week baseline sets each coordinator's starting time; timing starts at the same point in both arms. Duration: 4 weeks if the accounts have about 60 coordinators, 6 weeks if about 40, fixed before launch. |
| Primary metric | Median time per completed compliance check. Baseline 14.6 minutes; MDE 25% (to about 11 minutes); target 50% (about 7 minutes); p < 0.05, two-sided, read only on the fixed read date. |
| Guardrail metric | Checks logged per coordinator-day (must stay within 5% of control) and post-submission correction rate (must not rise more than 2 points above control). Manager Compliance CSAT (baseline 3.9) is surveyed at the end and must stay at 3.5 or above. A guardrail breach pauses the test early. |
| Decision rule (ship / kill / pivot) | **Ship** if time per completed check falls 25% or more against control at p < 0.05 and all guardrails hold. **Iterate** if the drop is significant but under 25%, or 25% or more but not significant: rerun with more coordinators. **Kill / pivot** to the next-largest gap (B3 Shift Handoff Wizard, +6.8 minutes) if the drop is under 10%, the variant is slower, or any guardrail is breached. |

## Findings & decision _(after running it)_

_Not run yet. To complete on the read date:_

| Result | Value |
|---|---|
| Coordinators per arm (confirmed headcount) | _____ |
| Test duration and read date | _____ |
| Time per completed check: control vs variant (change vs baseline) | _____ |
| Significance (p-value) | _____ |
| Checks logged per coordinator-day: variant vs control | _____ |
| Correction rate: variant vs control | _____ |
| Manager Compliance CSAT (end of test) | _____ |
| Decision: ship / iterate / kill | _____ |
| What we learned | _____ |
