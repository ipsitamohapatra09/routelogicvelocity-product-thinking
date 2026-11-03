# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** B1 One-Click Compliance Checklist - Attacks the 14.6-minute step head-on, but pre-fill needs reliable source data and must keep records complete for the guardrail.
- **My finalized Must-Haves (after overriding the AI):** Pre-fill fields the system already holds: driver, vehicle, route, date and time, and the last known values. This is where the minutes come from.
One screen, with human-input fields first. The checks that need a judgment sit at the top, and pre-filled fields are collapsed below, replacing today’s multi-screen admin flow.
Review and edit every pre-filled value before submitting. Without this, wrong data gets submitted silently and the completeness guardrail fails.
Write the same complete record as today. Same fields, same format, nothing dropped, so manager reporting and audits are unaffected.
Time-to-submit and completion tracking per coordinator. The pilot exists to test the primary metric, so it’s useless without the measurement.
Turn it on per account, with the current form as a fallback. If something breaks at one of the 3 pilot accounts, coordinators can switch back without losing records.
- **What I demoted from Must → Should/Won’t, and why:** SHOULD HAVE (if capacity allows)

“Confirm all unchanged” in one click for pre-filled fields the coordinator agrees with.
Highlight stale or missing source data, so coordinators know which pre-fills to double-check.
Save a draft and resume, for checks interrupted by a live dispatch issue.
Pre-fill driver-side compliance steps for the secondary persona (64% of drivers use Compliance daily, CSAT 2.8).

COULD HAVE (V2)

Defaults learned per vehicle or route from previous submissions.
Exceptions-only view that shows only the checks that changed since last time.
A mobile-optimised layout of the same form.
A link to B5, the step progress indicator, across compliance and handoff.

WON’T HAVE (NOW)

A rules engine, or any change to which checks are required. That’s a compliance and legal decision, not a speed fix.
AI-generated answers to compliance questions, which carry accuracy risk for the records managers rely on.
Account-specific checklist configuration, which would recreate the complexity being removed.
Changes to reporting or audit export, which belong to B9 and B8.
Shift handoff, daily report, or driver route alerts, which belong to B3, B2 and B6.
A new mobile surface, which belongs to B4 and stays in LATER.

One dependency to check before the PRD: Must 1 assumes the system already has reliable values for most compliance fields. That’s assumption 3 in the brief, and the field audit in weeks 1–2 should confirm it. If most fields can’t be pre-filled, the time savings shrink and B1’s Value score drops.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** **One thing my PRD makes explicit:** the system never answers a compliance judgment question, and it never guesses a missing value.

A vague brief like "pre-fill the compliance form to save time" would let a team, or an AI prototype builder, fill in "inspection: pass" from yesterday's record. That would hit the 7-minute target by producing compliance records nobody actually checked. The PRD rules this out in three places: a hallucination guard (inspection, defects and driver hours always need a human answer), a smart behavior (missing values stay empty and become required), and an eval (0 judgment questions submitted without a human answer). That protects the guardrail the brief only named: complete, trustworthy records for managers.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** 626f6c742d63632d6167656e74The biggest gap is a conflict in the numbers. The PRD requires at least 7 of 10 fields pre-filled on every check, but it also asks for 2 missing values in the sample data. Any check with a missing value can have at most 6 pre-filled fields, so the two targets can't both hold. I kept the missing values, so two of the six sample checks fall short of 7.

Other unclear points I had to decide myself:

- **Where missing values go.** The "Smart behaviors" table puts them under "Needs your answer," but the screen spec puts them under "Needs a quick look" and counts only three answers. I followed the screen spec.
- **Whether stale values count as pre-filled.** The PRD doesn't say. I treated them as not pre-filled, which affects the 7-of-10 count.
- **Odometer check with no reading.** The rule that an edited odometer can't be lower than the last reading has no answer when the last reading is stale or missing. I only apply it when a reading exists.
- **Defect details as a field.** The record must have exactly 10 fields, but defect details would be an 11th. I folded it into the defects answer.
- **"Confirm all unchanged."** The PRD gives the button no effect on Submit, so I made it visual only.
- **Classic form fallback.** The PRD requires that switching keeps every answer, but never defines the classic form. That's why the switch links are still dead.
- **Time away from a check.** The PRD doesn't say whether time spent away counts. I counted only active time.
- **"Few values available."** The threshold isn't defined; I chose 4 of 7 missing.

I'd settle the first three with you before building further, since they change what the sample data and checks should look like.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://bolt.new/p/72632053
