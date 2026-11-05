# GTM Strategy & Success Dashboard (Module 6)

## Get your prior work ready
- **The feature you're launching from your M4 PRD, one feature, not a list:** **The feature you're launching:**

**B1 One-Click Compliance Checklist:** one pre-filled screen where frontline coordinators log a vehicle's compliance check. Fields the system already holds are filled in with their source shown. The three judgment questions come first (pre-trip inspection, defects found, driver hours confirmed). Stale values are flagged for confirmation, and Submit stays locked until the record is complete. The aim is to cut the time coordinators spend logging compliance checks each day from 14.6 minutes to about 7.
Briefly,
B1 One-Click Compliance Checklist, launched only if the A/B test meets the ship criteria (25% or more off time per completed check, guardrails holding)
- **What your M5 experiment told you shipped / iterating, the evidence behind the launch:** **What your M5 experiment told you:**

**Status: not shipped yet. The test design is being refined before it runs live.**

The run was a simulation on synthetic data, so it tells you whether the experiment works, not whether the feature works. Here's what it showed:
- **The test can detect the effect.** With 30 coordinators per arm, a true 25% reduction in compliance time is detected in 100% of simulated runs, and even a 10% effect in 73% of them. The sample size isn't a risk.
- **The ship rule needed fixing.** A feature that truly delivers the 25% MDE would ship only 48% of the time, because the measured result must also reach 25%. The rule was changed to ship when the reduction is significant (p < 0.05) and the measured reduction is 20% or more.
- **Guardrails needed smoothing.** Random noise caused about 2% false kills. A breach now has to hold for two consecutive weeks.
- **There are no gaps in the decision rule.** Every simulated outcome mapped to ship, iterate or kill.

**The evidence behind the launch so far:** the problem is measured (14.6 minutes against a 3-minute benchmark, CSAT 2.2, 31% completion through handoff, and 4 of 5 churned accounts citing complexity), the prototype works end to end, and the experiment is now designed to give a reliable answer. The launch still waits on two things: the coordinator usability test, and the live A/B result against the corrected ship rule.
- **Your persona pull your M2 persona, this anchors your audience:** **Your persona (from M2):**

**Dana, a frontline delivery driver** (a composite built from interviews UXR-01, 03, 06, 07, 11 and 12)
- **Role:** runs a multi-stop route each shift, often in bad weather with weak signal, and works alongside the coordinators and dispatchers who manage her route.
- **Goal:** finish every stop on time without calling the office or reaching for a backup.
- **Friction:** marking a stop delivered takes three taps across three screens (BUG-2055), and the route disappears when the app crashes or loses signal (BUG-2031, BUG-2050). Her workaround is texting the dispatcher, and 5 of 7 drivers in the focus group keep a paper manifest "just in case the app dies" (UXR-12).

**How this anchors the GTM audience:** the Module 3 data moved the primary persona to the **frontline coordinator** (14.6 minutes a day on compliance logging, CSAT 2.2), so the launch targets coordinators and the ops managers who switch the feature on. Dana remains the secondary persona: 64% of drivers use Compliance daily and rate it 2.8. In the GTM plan, the in-app message reaches both, but the CSM walkthroughs and renewal conversations aim at coordinators and their managers, not drivers.

## Set your goal, then your audience
- **Primary GTM goal awareness · engagement · conversion, pick one:** Primary GTM goal: Conversion

The goal is to convert coordinators at at-risk accounts from workarounds (texts, WhatsApp, paper) to logging compliance checks in RouteLogic Velocity.
Awareness isn’t the problem: these accounts already have the product, and 77% of coordinators already open Compliance every day. The task is changing behaviour inside existing accounts in two steps. First, the ops manager switches the feature on. Then coordinators choose the new form over their workaround. Success shows up as protected renewals, since 4 of 5 churned accounts cite complexity.
- **Why this goal? what makes this the right goal for this feature right now:** **Why this goal?**

- **The audience already knows the product, so awareness isn't the gap.** 77% of coordinators open Compliance every day. Their problem is how they use it: the step takes 14.6 minutes against a 3-minute benchmark, so many finish the job in WhatsApp, texts or paper. Only 31% complete the workflow through handoff in the product.
- **The revenue risk is in existing accounts.** Coordinator NPS has fallen from +18 to −12, and 4 of 5 churned accounts cite complexity. Every coordinator who switches from a workaround to the new form weakens the case for a leaner rival at renewal.
- **The timing comes from the renewal calendar.** Accounts renewing in the next two quarters are deciding now whether the depth is worth the friction. A conversion push before those renewals protects revenue. An awareness campaign would only pay off after the decisions are made.
- **Conversion here is measurable and within our control.** It has two clear steps (the ops manager switches the feature on, then coordinators use it for most checks), each with a number and an owner, which fits a team of 2 engineers, 1 designer and 1 CS lead better than a broad engagement goal.
- **Target audience the specific segment your goal implies, be precise:** **Target audience:**

Frontline coordinators and their ops managers at about 20 existing RouteLogic Velocity accounts *(assumed: confirm with your renewal list)*. Each account must meet three conditions:

1. **It renews in the next two quarters,** ranked by churn risk (accounts with complexity complaints, falling coordinator NPS, or open evaluations of a leaner rival come first).
2. **Its coordinators already use Compliance daily,** so there is a habit to convert, not one to create.
3. **It passes the field audit,** meaning the system holds enough data to pre-fill most compliance fields. Accounts without that data get little benefit and wait.

Within each account, two people matter:
- **The ops manager** is the decision-maker. They turn the feature on for the account and care about complete compliance records.
- **The coordinators** are the users who must choose the new form over WhatsApp, texts and paper. They're the people whose 14.6 minutes a day the feature is meant to save.

**Excluded for now:**
- **New prospects:** they wait until there's a quantified pilot result to show them.
- **Accounts not up for renewal:** they come later.
- **Drivers like Dana:** they see the in-app message but aren't a campaign target.

## Size your launch
- **Launch tier S (minimal) · M (targeted) · L (multi-channel) · XL (full GTM):** **Launch tier: M (targeted)**

**Why M:**
- **The reach is narrow:** about 20 existing accounts, not the market.
- **The revenue stakes are high.** Those accounts' renewals depend on it, so the launch needs to be high-touch, not just a release note (that would be S).
- **The team can deliver M, not L or XL.** There's 1 CS lead and a team of 2 engineers and 1 designer. That supports CSM-led rollout to priority accounts, but not paid media or a market-wide campaign.
- **No proof yet for a bigger claim.** The A/B test and the usability test haven't run, so there's no customer result to put in front of prospects.

**When to move to L:** if the A/B test meets the 50% target, a pilot account agrees to be a public reference, and the feature then goes to all accounts and prospects.
- **Justification reach + revenue impact + what silence would risk:** **Justification for Tier M:**

- **Reach:** narrow by design. The audience is about 20 existing accounts renewing in the next two quarters, made up of each account's ops manager and their frontline coordinators. That isn't a market-wide audience, so Tier L or XL channels (paid media, press) would mostly reach people who can't use the feature yet.
- **Revenue impact:** high and concentrated. The renewal revenue of those priority accounts is at stake (**$____ ARR**, to fill in from your renewal list). Complexity is the leading churn reason, cited by 4 of 5 churned accounts, and coordinator NPS has fallen from +18 to −12. Keeping even one or two enterprise accounts would likely outweigh the launch's cost, which is why this needs more than a quiet release (Tier S).
- **What silence would risk:** the feature is switched on per account, so without a targeted push it stays off.
  - Ops managers wouldn't know to enable it.
  - Coordinators would keep spending 14.6 minutes a day and falling back on WhatsApp and paper.
  - Renewal decisions would be made before customers see the fix, which hands leaner rivals the "simpler" argument at the moment the account is deciding.
  - Every month of workarounds also keeps compliance data out of the system, weakening the reporting buyers pay for.
- **Is this a launch or a release? does it need go-to-market, or can it just ship?:** **It's a launch: it needs go-to-market. It can't just ship.**

A quiet release only works when users find and use a feature on their own, and here they won't:
- **It's off by default.** The feature is switched on per account, so someone has to tell each ops manager it exists and why to enable it.
- **It has to break a habit.** Coordinators already rely on WhatsApp, texts and paper. Changing that takes a reason, a short demo and a bit of trust in pre-filled values, not a release note.
- **The timing matters for revenue.** At-risk accounts are deciding at this year's renewals, so the fix needs to be in front of them before those decisions, not discovered afterwards.
- **It changes a compliance process.** Managers need to know records stay complete, and coordinators need to know they must still check stale values. That takes enablement, not just a changelog.

The scope is still small, which is why it's a targeted Tier M launch to about 20 accounts rather than a market-wide one.

## Choose your top three channels and plan assets
- **Channel 1 owned / earned / paid, and why it reaches your audience:** Channel 1: Owned, an in-app message inside the compliance step
It reaches coordinators where they already are. 77% open Compliance every day, so a short message at the moment they start a check (“Your checks are now pre-filled: answer 3 questions, confirm anything flagged”) lands at the exact point of friction. It appears only for accounts where the feature has been switched on, and it links to a 2-minute video. It doesn’t go on the dashboard, which coordinators skip.
- **Channel 2 owned / earned / paid, and why:** Channel 2: Owned, CSM-led walkthroughs at account reviews and renewal calls
This reaches the ops managers who decide whether to switch the feature on. They already meet their CSM at account reviews and renewal conversations, so the walkthrough uses a meeting that already exists. The CSM shows the feature on the account’s own data, confirms the account passes the field audit, and agrees an activation date. For the 5 highest-risk accounts, it becomes an on-site session with the coordinators.
- **Channel 3 owned / earned / paid, and why:** Channel 3: Earned, a case study from a pilot account
Buyers trust results from peers more than vendor claims. A one-page case study with the pilot account’s measured time saved (for example, “compliance logging cut from 14.6 to X minutes a day”) gives CSMs and Sales proof to use in renewal conversations. It depends on the A/B result and on the customer’s and Legal’s approval.
Paid: none for this launch. Coordinators don’t look for work tools on LinkedIn or ad networks, and existing buyers can be reached directly for free. The budget goes to on-site enablement instead.
- **Enablement & assets what Sales / CS / Support need, plus the assets to build (one-pager, demo, etc.):** Team	What they need
CS / CSMs	Playbook covering which accounts to activate first, the field-audit eligibility check, how to switch the feature on per account, and what to do if coordinators fall back to the classic form · walkthrough script and demo on sample data · activation tracker
Sales / account managers	Renewal talk track (“the fix for frontline complexity, with records as complete as today”) · objection handling (“Will pre-filled values make our records wrong?”) · the case study once approved
Support	Help replies for common questions (stale values, missing values, switching to the classic form, defect details) · how to escalate if a record is missing a field
Ops managers (customer admins)	Admin guide: what changes, how to switch it on, what stays the same in reports and audits
Coordinators	2-minute in-app video · one-page quick guide (answer, confirm, submit)

Assets to build: CSM playbook and walkthrough script · renewal talk track and objection sheet · admin guide · 2-minute coordinator video · coordinator quick guide · support help replies and FAQ · one-page case study after the A/B result · in-app message copy.

## Make it executable
- **Ownership named owner per key activity, individual, not department:** **Ownership:** one named person per activity. I don't know your team's names, so fill in the blanks. The role shows who each person should be.

| Key activity | Owner (one person) | Role |
|---|---|---|
| Overall launch: go/no-go and timeline | **You** | Product Manager |
| Fixing the two blockers (classic form link, failed-inspection flag) | __________ | Engineering lead |
| Switching the feature on per account and in-app message targeting | __________ | Engineering lead |
| In-app message copy and the 2-minute coordinator video | __________ | Product Designer |
| Priority account list and field-audit eligibility check | **You** | Product Manager |
| CSM playbook, walkthrough script and CSM training | __________ | CS Lead |
| Activation at each priority account | __________ (one per account) | Account's assigned CSM |
| Renewal talk track and objection sheet | __________ | Product Marketing Manager |
| Case study, including customer and legal approval | __________ | Product Marketing Manager |
| Renewal conversations at priority accounts | __________ | Account Executive |
| Admin guide and coordinator quick guide | __________ | Product Marketing Manager |
| Support help replies, FAQ and escalation path | __________ | Support Lead |
| Launch metrics dashboard and the bad-signal check in weeks 1–2 | **You** | Product Manager |

**Two gaps to close before launch:**
- **The CS lead is overloaded.** One person can't train CSMs and run activation at about 20 accounts. Activation has to sit with each account's own CSM, by name.
- **Product marketing may not have an owner.** If your team has no PMM, these items fall to you, and they're the first to slip: the talk track, case study, guides and video script. Decide now who takes them.
- **Budget & resource gaps what costs extra, and any asset you can't currently build:** **Budget and resource gaps**

**What costs extra** *(no budget is set yet, so each line needs an estimate)*

| Item | Why it's needed | Cost to estimate |
|---|---|---|
| On-site enablement at the 5 highest-risk accounts | In-person sessions with coordinators at the accounts most likely to churn | Travel and CSM time: $____ |
| 2-minute coordinator video | The designer can storyboard it, but a polished video may need outside production | $____, or $0 if it's a simple screen recording |
| Case study production | Interview, writing, design and customer and legal review | $____ in PMM or agency time, plus legal hours |
| Usability test participant thank-yous | 5–8 coordinators giving 45 minutes each | Small gift cards: $____ |
| CSM time | About 20 walkthroughs plus follow-ups, taken from their normal accounts | No direct cost, but less time for other customers |

**Assets you can't build yet**

| Asset | What's blocking it | Unblocked by |
|---|---|---|
| Case study with measured time saved | No A/B result, and no customer has agreed to be a reference | A/B read date, then customer and legal approval |
| Any claim in sales material about time saved | Only synthetic simulation data exists | The A/B test or, at minimum, the usability test |
| A working classic form fallback | The link is still a placeholder in the prototype (FR7) | Engineering, before launch |
| A flag for failed inspections and unconfirmed hours | It's not in the PRD; the gap was found in the prototype | A design decision, then engineering |
| Priority account list | The field audit hasn't run, so you don't know which accounts have enough data to pre-fill | Field audit during the 2-week baseline |
| Activation tracker for CSMs | Needs per-account usage data and engineering time from a team of 2 | A shared spreadsheet now; a dashboard later |
| Driver-side pre-fill for Dana | A Should-have, not in the launch scope | A later release |

**Resource gaps**
- **People:** there's 1 CS lead and possibly no product marketing manager, so the talk track, guides, case study and video script have no clear owner.
- **Engineering:** the same 2 engineers must fix the two blockers, build per-account switching and support the A/B test.

Agree on the budget and these owners before setting a launch date. Otherwise the plan depends on work nobody has time for.

=====based on synthetic numbers==============
Here are the estimates with **synthetic numbers**. They're illustrative placeholders for planning, not quotes or real data, so replace them as real figures come in.

**Cash budget (synthetic)**

| Item | How it's calculated | Estimate |
|---|---|---|
| On-site enablement at 5 highest-risk accounts | 5 trips × $1,200 (flight, 1 hotel night, meals) | $6,000 |
| 2-minute coordinator video | Freelance edit of designer-scripted screen recording | $2,500 |
| Case study | Freelance writer and layout ($3,000) + legal review (4 hrs × $250) | $4,000 |
| Usability test thank-yous | 8 coordinators × $50 gift card | $400 |
| Contingency | 10% of the above | $1,290 |
| **Total cash** | | **$14,190** |

**Optional: fill the product marketing gap**

| Item | How it's calculated | Estimate |
|---|---|---|
| Contract product marketing manager | 10 days × $700 (talk track, guides, case study, in-app copy) | $7,000 |
| **Total with contractor** | | **$21,190** |

**Internal time (synthetic, no cash cost)**

| Team | Work | Time | Loaded cost |
|---|---|---|---|
| Engineering (2 engineers) | Classic form fallback (3 days) · failed-inspection and hours flag (2) · per-account switch (3) · in-app message (1) | 9 engineer-days | $9,000 at $1,000/day |
| CSMs | 20 walkthroughs × 2.5 hrs, including follow-up | 50 hours | $3,750 at $75/hr |
| CS lead | Playbook, CSM training, weekly activation review | 6 days | $3,600 at $600/day |
| Designer | In-app copy, video storyboard, quick guide | 4 days | $2,400 at $600/day |
| **Total internal time** | | | **$18,750** |

**What's at stake (synthetic)**

| | Estimate |
|---|---|
| Priority accounts | 20 |
| Average annual contract value | $120,000 |
| Renewal revenue at stake | $2.4M |
| Revenue protected if the launch saves 2 accounts | $240,000 |
| Full launch cost (cash, contractor and internal time) | ~$40,000 |

Saving even one $120,000 account would cover the full launch cost about three times over, which supports a Tier M investment.

**Gaps that still can't be bought**
- **Case study and time-saved claims:** they wait on the A/B result and customer approval.
- **Priority account list:** it waits on the field audit.
- **Engineering capacity:** the 9 engineer-days compete with the A/B test for the same 2 engineers. Schedule the blockers before the feature is switched on, or the launch date slips.

I built GTM-Launch-Budget.xlsx with two sheets, both clearly labeled as synthetic:

- **Launch Budget:** cash budget, the optional contractor, internal time and the full launch cost. The totals match my last answer: $14,190 cash, $21,190 with the contractor, $18,750 of internal time, and $39,940 in all.
- **What's at Stake:** revenue at risk, revenue protected, return on the launch cost and break-even. Its launch-cost figure is linked to the first sheet, so it updates automatically.

Every quantity, unit cost and scenario input is a blue cell you can change, and all totals recalculate from them. With these assumptions, saving 2 accounts protects $240,000, about 6 times the launch cost. Break-even is about a third of one account.
- **Timeline Phase 1 beta → Phase 2 launch moment → Phase 3 post-launch:** **Timeline** *(relative weeks: set real dates once the coordinator headcount and A/B read date are confirmed)*

**Phase 1: Beta (weeks 1–6), proving it works before anyone hears about it**
- **Weeks 1–2:**
  - **Measurement:** 2-week A/B baseline and the field audit, which produces the eligible account list.
  - **Usability test:** 5–8 coordinators.
  - **Product fixes:** engineering fixes the two blockers (the classic form fallback and the failed-inspection and hours flag).
- **Weeks 3–6:**
  - **A/B test:** 4-week test at the 3 pilot accounts.
  - **Assets:** the CS lead drafts the playbook, and the designer scripts the video and in-app message.
- **Gate at the end of week 6:** go/no-go at the fixed A/B read date. Ship only if the time per completed check is significantly lower (p < 0.05) by 20% or more, and both guardrails hold.

**Phase 2: Launch moment (weeks 7–10), switching it on account by account**
- **Week 7:**
  - **Enablement:** CSM training and the final talk track and admin guide.
  - **Case study:** request customer and legal approval, drafting from the real result.
- **Weeks 8–9:** activation at the top 10 priority accounts, with:
  - CSM walkthroughs with each ops manager
  - the feature switched on per account
  - the in-app message going live for those coordinators
  - on-site sessions at the 5 highest-risk accounts
- **Week 10:** activation at the remaining 10 priority accounts, and the case study used in renewal conversations once approved.

**Phase 3: Post-launch (weeks 11–22), turning activation into kept renewals**
- **First 2 weeks at each account:** watch the bad signal. If coordinators switch back to the classic form on more than 20% of checks, or the correction rate rises more than 2 points, the CSM visits within 5 working days.
- **Day 14 after the first activations:** if fewer than 40% of priority accounts are switched on, the CS lead escalates to Sales for executive outreach.
- **Day 30 review:**
  - 60% of priority accounts switched on
  - 70% of their coordinators using the new form for most checks
  - compliance time down from each account's baseline
- **Day 90 (about week 22):** renewal review, which also decides whether to move to a Tier L launch to all accounts and prospects. The target is no priority account lost citing complexity.

## Define how you'll know it worked
- **Success metrics 2 to 3 metrics that match your GTM goal:** **Success metrics (Conversion goal):**

1. **Account activation:** 60% of the about 20 priority accounts have the checklist switched on within 30 days of their CSM walkthrough. This measures whether ops managers say yes.
2. **Coordinator adoption:** 70% of coordinators at activated accounts use the new form for 80% or more of their compliance checks by day 30. This measures whether coordinators leave WhatsApp, texts and paper behind, which is the conversion itself.
3. **Renewal retention:** no priority account lost citing complexity at its next renewal, reviewed at day 90. This measures whether the conversion protects revenue.

Time per completed check (down 25% or more from each account's baseline) is tracked as the value check behind these three. The A/B test has already measured it, so it confirms the feature still delivers outside the pilot rather than serving as a GTM goal.
- **Bad signal to watch for e.g. high reach, zero signups = message-market mismatch:** **Bad signal to watch for:**

**Ops managers switch the feature on, but coordinators keep switching back to the classic form.** This is high activation with low adoption. Treat it as a bad signal if, within the first 2 weeks at any activated account, coordinators open the classic form on **more than 20% of checks**.

**What it means:** the buyer bought the story, but the user doesn't trust or prefer the new form. Typical causes:
- pre-filled values are wrong or missing because the account's data is poor
- coordinators don't trust confirming stale values
- the new form doesn't fit how that account actually works

That's a product-fit mismatch at the account level, not a messaging problem.

**A second warning to watch alongside it:** the correction rate rises **more than 2 points**. That means coordinators are accepting pre-filled values without checking them, which puts the manager's records, and the renewal argument, at risk.

**Action:** within 5 working days, the account's CSM visits or calls the coordinators to find out why. The PM checks that account's pre-fill rate against the field audit. If the data is the cause, the account pauses until it's fixed rather than staying on a form coordinators avoid.
- **Most likely post-launch decision double-down · iterate · pivot · deprioritize, and what would trigger it:** **Most likely post-launch decision: iterate**

**Why iterate is most likely:** adoption will probably be uneven across accounts. Pre-fill depends on each account's data quality, which the field audit already shows varies. Accounts with good data should adopt quickly, while those with gaps will see more missing values and more switching back to the classic form. That mixed picture, strong in some accounts and weak in others, points to fixing the weak cases before expanding, not to doubling down or abandoning the feature.

**What would trigger each decision at the day-30 review:**

| Decision | Trigger |
|---|---|
| **Double down** (move to Tier L for all accounts and prospects) | 60% or more of priority accounts activated, 70% or more of their coordinators using the new form for most checks, time per check down 25% or more, guardrails holding, and a pilot account agreeing to be a public reference |
| **Iterate** (most likely) | Activation on target but adoption below 70%, or strong in good-data accounts and weak in poor-data ones. Fix pre-fill coverage and the reasons coordinators fall back, then re-review in 30 days |
| **Pivot** (to the next-largest gap, the B3 Shift Handoff Wizard) | Coordinators adopt the form but time per check barely moves (under 10% down), meaning compliance wasn't where their time really goes |
| **Deprioritize** | Activation under 40% despite CSM outreach, or a guardrail breach (correction rate up more than 2 points, or manager Compliance CSAT below 3.5) that a fix can't resolve. In that case, renewals depend on something other than this feature |

The day-90 renewal review confirms the decision. If priority accounts renew without citing complexity, iterating was enough. If they still cite complexity, the next decision is a pivot.
