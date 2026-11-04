# GTM Strategy & Success Dashboard

> **Module 6 · ★ Deliverable 6.** Repo file `06-launch/gtm-and-dashboard.md` — part of your submission.
> Do the lab in the **Module 6 · Exercise Guide** (linked from the Module 6 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **GTM Strategy & Success Dashboard** slide of your Module 6 final deck.

## Go-to-market summary

_A concise overview of your launch plan: channels, launch size, and overall strategy._

B1 One-Click Compliance Checklist launches as a **Tier M, targeted conversion launch** to existing RouteLogic Velocity accounts, gated on the A/B test's ship criteria. The goal is to convert coordinators at at-risk accounts from WhatsApp, texts and paper to logging compliance in the product, protecting renewals: 4 of 5 churned accounts cite complexity, and coordinator NPS has fallen from +18 to −12.

- **Audience:** frontline coordinators and their ops managers at about 20 accounts renewing in the next two quarters, ranked by churn risk and limited to accounts the field audit shows can be pre-filled. The ops manager switches the feature on; coordinators must choose it over their workaround.
- **Launch size:** Tier M. The reach is narrow, but each account's renewal is at stake, and the team (2 engineers, 1 designer, 1 CS lead) can deliver a CSM-led launch, not a market-wide one. Move to Tier L only with a 50% time reduction and a public reference account.
- **Channels:**
  1. **Owned:** an in-app message inside the compliance step, where 77% of coordinators already work every day.
  2. **Owned:** CSM-led walkthroughs at account reviews and renewal calls, which reach the ops managers who decide; on-site sessions at the 5 highest-risk accounts.
  3. **Earned:** a pilot-account case study with measured time saved, used in renewal conversations.
  - **Paid:** none. Coordinators don't look for work tools in ads, and existing buyers can be reached directly.
- **Enablement:** CSM playbook and walkthrough script, renewal talk track and objection sheet, admin guide, 2-minute coordinator video, coordinator quick guide, support help replies.
- **Timeline:** Phase 1 beta (weeks 1–6: baseline, usability test, A/B test, go/no-go) → Phase 2 launch (weeks 7–10: CSM training, then activation at the top 10 and remaining 10 accounts) → Phase 3 post-launch (day 14, 30 and 90 reviews).
- **Budget (synthetic estimate):** about $14,200 cash ($21,200 with a contract product marketing manager), plus about $18,750 of internal time, against about $2.4M of renewal revenue at stake.
- **Bad signal:** ops managers switch the feature on but coordinators open the classic form on more than 20% of checks in the first 2 weeks, or the correction rate rises more than 2 points. The CSM investigates within 5 working days, and the PM checks that account's pre-fill data.
- **Most likely post-launch decision:** iterate, because adoption will probably be uneven across accounts with different data quality.

## Success dashboard

| KPI | Baseline | Target | Measurement window |
|---|---|---|---|
| Account activation: priority accounts with the checklist switched on | 0% (feature not yet released) | 60% of about 20 priority accounts | Within 30 days of each account's CSM walkthrough |
| Coordinator adoption: coordinators at activated accounts using the new form for 80% or more of their checks | 0% (all checks on the classic form or workarounds) | 70% | Day 30 after activation |
| Time per completed compliance check (value check) | 14.6 minutes per coordinator per day | 25% or more lower than each account's baseline (about 11 minutes or less) | Day 30 after activation, against each account's own baseline |
| Renewal retention: priority accounts lost citing complexity | 4 of 5 churned accounts cited complexity | 0 priority accounts lost citing complexity | Day 90 renewal review |
| Guardrail: post-submission correction rate | Each account's pre-launch rate | No more than 2 points above baseline | Weekly, first 30 days |

## Launch plan detail

_Supporting detail behind the summary and dashboard: readiness, audience rules, ownership, budget, timeline and decision triggers._

### Feature and readiness

- **Feature:** B1 One-Click Compliance Checklist, one pre-filled screen where frontline coordinators log a vehicle's compliance check. Fields the system already holds are filled in with their source shown, the three judgment questions come first (pre-trip inspection, defects found, driver hours confirmed), stale values are flagged for confirmation, and Submit stays locked until the record is complete.
- **M5 status: not shipped yet.** A simulation on synthetic data validated the experiment design, not the feature:
  - With 30 coordinators per arm, a true 25% reduction is detected in 100% of simulated runs, and a 10% reduction in 73%.
  - The ship rule was corrected: a true 25% effect would have shipped only 48% of the time, so the rule is now p < 0.05 with a measured reduction of 20% or more.
  - A guardrail breach must now hold for two consecutive weeks, removing about 2% of false kills.
- **Evidence so far:** compliance logging takes 14.6 minutes against a 3-minute benchmark (CSAT 2.2), only 31% of coordinators complete the workflow through handoff, 4 of 5 churned accounts cite complexity, and the prototype works end to end.
- **Launch waits on:** the coordinator usability test and the live A/B result against the corrected ship rule.

### Persona and audience rules

- **Primary persona:** the frontline coordinator, who spends 14.6 minutes a day on compliance logging. The Module 3 data moved the focus here from the Module 2 persona.
- **Secondary persona:** Dana, a frontline delivery driver (composite of UXR-01, 03, 06, 07, 11 and 12) who wants to finish every stop without calling the office or reaching for a backup. 64% of drivers use Compliance daily and rate it 2.8. She sees the in-app message but isn't a campaign target.
- **An account qualifies only if it:**
  1. renews in the next two quarters, ranked by churn risk (complexity complaints, falling coordinator NPS, open evaluations of a leaner rival)
  2. has coordinators who already use Compliance daily
  3. passes the field audit, so most compliance fields can be pre-filled
- **Excluded for now:** new prospects (until there's a quantified result), accounts not up for renewal, and drivers as a campaign audience.

### Why conversion, why now, and why a launch

- **Awareness isn't the gap.** 77% of coordinators already open Compliance every day; the problem is that the step is slow enough to push work into WhatsApp, texts and paper.
- **The timing follows the renewal calendar.** Accounts renewing in the next two quarters are deciding now whether the depth is worth the friction.
- **It needs go-to-market, not just a release.** The feature is off by default per account, it has to break an established workaround habit, and it changes a compliance process that managers and coordinators both need to trust.
- **What silence would risk:** ops managers wouldn't know to switch it on, coordinators would keep losing 14.6 minutes a day, renewals would be decided before customers see the fix, and compliance data would keep leaking out of the system.

### Enablement by team

| Team | What they need |
|---|---|
| CS / CSMs | Playbook (activation order, field-audit eligibility, switching the feature on, handling fallback to the classic form) · walkthrough script and demo on sample data · activation tracker |
| Sales / account managers | Renewal talk track · objection handling ("Will pre-filled values make our records wrong?") · the case study once approved |
| Support | Help replies for stale values, missing values, the classic form and defect details · escalation path if a record is missing a field |
| Ops managers (customer admins) | Admin guide: what changes, how to switch it on, what stays the same in reports and audits |
| Coordinators | 2-minute in-app video · one-page quick guide (answer, confirm, submit) |

### Ownership

| Key activity | Owner | Role |
|---|---|---|
| Overall launch, go/no-go and timeline | You | Product Manager |
| Priority account list and field-audit eligibility | You | Product Manager |
| Launch metrics and the bad-signal check in weeks 1–2 | You | Product Manager |
| Fixing the two blockers; per-account switch and in-app targeting | __________ | Engineering lead |
| In-app message copy and the coordinator video | __________ | Product Designer |
| CSM playbook, walkthrough script and CSM training | __________ | CS Lead |
| Activation at each priority account | __________ (one per account) | Assigned CSM |
| Talk track, case study, admin guide and quick guide | __________ | Product Marketing Manager |
| Renewal conversations at priority accounts | __________ | Account Executive |
| Support help replies, FAQ and escalation path | __________ | Support Lead |

**Gaps to close:** one CS lead can't run activation at about 20 accounts, so each CSM owns their own accounts; if there's no product marketing manager, the talk track, case study, guides and video script fall to the PM unless a contractor is hired.

### Budget and resources (synthetic estimates)

_Illustrative placeholders for planning, not quotes or real data._

| Line | Estimate |
|---|---|
| Cash: on-site enablement at 5 accounts ($6,000), coordinator video ($2,500), case study and legal review ($4,000), usability test thank-yous ($400), 10% contingency ($1,290) | $14,190 |
| Optional contract product marketing manager (10 days × $700) | $7,000 |
| Internal time: engineering 9 days ($9,000), CSMs 50 hours ($3,750), CS lead 6 days ($3,600), designer 4 days ($2,400) | $18,750 |
| **Full launch cost** | **$39,940** |
| Renewal revenue at stake (20 accounts × $120,000) | $2.4M |
| Revenue protected if the launch saves 2 accounts | $240,000 (about 6× the launch cost) |

**Assets that can't be built yet:**

| Asset | Blocked by | Unblocked by |
|---|---|---|
| Case study and any time-saved claim | No real result; only synthetic data | Live A/B result, then customer and legal approval |
| Working classic form fallback | Still a placeholder in the prototype (FR7) | Engineering, before launch |
| Flag for failed inspections and unconfirmed hours | Not in the PRD; found in the prototype | A design decision, then engineering |
| Priority account list | Field audit hasn't run | Field audit during the 2-week baseline |
| Activation tracker | Needs usage data and engineering time | A shared spreadsheet now, a dashboard later |

The 9 engineer-days compete with the A/B test for the same 2 engineers, so the blockers must be scheduled before activation or the launch date slips.

### Timeline detail

| Phase | Weeks | What happens | Gate or check |
|---|---|---|---|
| 1. Beta | 1–2 | A/B baseline, field audit, usability test, both blockers fixed | |
| 1. Beta | 3–6 | 4-week A/B test at 3 pilot accounts; playbook, video and in-app message drafted | Go/no-go at the fixed read date: p < 0.05, 20% or more reduction, guardrails holding |
| 2. Launch | 7 | CSM training, final talk track and admin guide, case study approval requested | |
| 2. Launch | 8–9 | Activation at the top 10 accounts: walkthroughs, feature on, in-app message live, on-site at the 5 highest-risk | |
| 2. Launch | 10 | Activation at the remaining 10 accounts; case study in renewal conversations once approved | |
| 3. Post-launch | 11–22 | Bad-signal watch for 2 weeks per account; reviews at day 14, 30 and 90 | Day 14: escalate if under 40% activated · Day 30: dashboard targets · Day 90: renewal review and Tier L decision |

### Bad signal and response

- **Signal:** ops managers switch the feature on, but coordinators open the classic form on more than 20% of checks in the first 2 weeks at any account, or the correction rate rises more than 2 points.
- **Likely causes:** wrong or missing pre-filled values from poor account data, distrust of confirming stale values, or a form that doesn't fit how that account works. This is a product-fit problem at account level, not a messaging problem.
- **Response:** within 5 working days, the CSM talks to the coordinators and the PM checks the account's pre-fill rate against the field audit. If the data is the cause, the account pauses until it's fixed.

### Post-launch decision triggers (day 30)

**Most likely decision: iterate,** because adoption will probably be uneven across accounts with different data quality.

| Decision | Trigger |
|---|---|
| Double down (Tier L to all accounts and prospects) | 60% or more activated, 70% or more adoption, time per check down 25% or more, guardrails holding, and a pilot account agrees to be a public reference |
| Iterate | Activation on target but adoption below 70%, or strong in good-data accounts and weak in poor-data ones; fix pre-fill coverage and re-review in 30 days |
| Pivot (to B3 Shift Handoff Wizard) | Coordinators adopt the form but time per check falls less than 10% |
| Deprioritize | Activation under 40% despite outreach, or a guardrail breach (correction rate up more than 2 points, or manager Compliance CSAT below 3.5) that a fix can't resolve |

The day-90 renewal review confirms the call: if priority accounts renew without citing complexity, iterating was enough; if not, the next decision is a pivot.
