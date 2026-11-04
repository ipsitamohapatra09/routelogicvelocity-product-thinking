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

# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | B1 One-Click Compliance Checklist: one pre-filled compliance screen with judgment questions first and stale values to confirm |
| Persona | Frontline coordinators at 3 pilot accounts (secondary: drivers like Dana, reported directionally only) |
| Expected outcome | Coordinators complete compliance logging inside RouteLogic Velocity instead of abandoning the workflow for texts, WhatsApp and paper |
| Primary success metric | Median time per completed compliance check, timed from opening compliance in the dispatch view to Submit in both arms |
| Baseline rate | 14.6 minutes |
| Guardrail metric | Checks logged per coordinator-day (stops coordinators "saving time" by logging fewer checks) |
| Guardrail boundary | Variant must stay within 5% of control; a larger drop pauses the test |
| Second guardrail | Post-submission correction rate (records corrected later by managers or audits); variant must not rise more than 2 points above control. Manager Compliance CSAT (baseline 3.9) is surveyed at the end and must stay at 3.5 or above |
| Minimum Detectable Effect | 25% reduction (14.6 to about 11 minutes, about 3.7 minutes saved); target 50% (about 7 minutes) |
| Sample size per arm | About 30 coordinators (about 600 coordinator-days over 4 weeks). Powered at coordinator level against each coordinator's own 2-week baseline; standard deviation confirmed from the baseline before launch |
| Traffic split | 50/50, randomized by coordinator within each pilot account |
| Test duration | 4 weeks if the pilot accounts have about 60 coordinators, 6 weeks if about 40; fixed before launch, after a 2-week baseline. Covers at least 4 weekly cycles |
| Significance threshold | p < 0.05, two-sided, for the primary metric. Guardrails act on their boundaries without waiting for significance |

## Control vs. Variant
- **Control (A):** Today's multi-screen compliance form, built for admins. Coordinators re-enter driver, vehicle and route details the system already holds. Compliance logging takes 14.6 minutes against a 3-minute benchmark, coordinators rate it 2.2 out of 5 though 77% use it daily, and only 31% complete the workflow through shift handoff in the product.
- **Variant (B):** One pre-filled compliance screen (PRD Screens 1–3, FR1–FR7): fields the system already holds are pre-filled with source tags and collapsed; the three judgment questions (pre-trip inspection, defects found, driver hours confirmed) come first; stale or missing values are surfaced for confirmation; Submit stays disabled until 3 of 3 answers and all confirmations are given; every value is editable, and the classic form is one click away. To keep this a single change, the visible timer and 7-minute target, the "Confirm all unchanged" button and the progress panel are removed, and the banner reads neutrally ("Compliance form updated").
- **Held constant (isolation check):** App build apart from the feature flag; Live Dispatch Board and Route Optimizer; which compliance questions are required and their rules; the compliance record format and every field stored; shift handoff, daily report and driver notifications (B3, B2 and B6 unreleased to both arms); manager tools, with B9 going to both arms if it ships; bug fixes for BUG-2031 and BUG-2044 shipping to everyone; the same neutral briefing and CS support; devices, accounts, depots and shift patterns; silent timing from the same starting point in both arms. Coordinators who switch to the classic form are analysed in the arm they were assigned to.

## Hypothesis
> I believe that **the One-Click Compliance Checklist** for **frontline coordinators** will result in **coordinators completing compliance logging inside the product instead of through texts, WhatsApp and paper**, as measured by a **50%** change in **median time per completed compliance check (14.6 to about 7 minutes)** within **4 weeks (6 if the pilot accounts have about 40 coordinators)**. We will protect **checks logged per coordinator-day and the post-submission correction rate** throughout the test.

## Shipping criteria
> We will **ship** if **median time per completed compliance check** improves by ≥ **25% relative to control** at **p < 0.05, two-sided** and **checks logged per coordinator-day or the correction rate** does not reach **a drop of more than 5% or a rise of more than 2 points versus control** after **4 weeks (6 if about 40 coordinators)**.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of **the 4-week test (6 weeks if about 40 coordinators), set once the baseline confirms headcount**, no results reviewed before this date.
