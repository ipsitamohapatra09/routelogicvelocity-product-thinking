# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** RouteLogic Velocity’s frontline coordinators. In the research these are mainly delivery drivers running multi-stop routes, working with dispatchers (composite persona “Dana”, built from UXR-01, 03, 06, 07, 11 and 12).
- **Primary success metric (M3), your leading indicator:** Share of coordinators completing the dispatch workflow through shift handoff in the product
- **Moment of misery (M2), the specific friction blocking the goal:** The app is slowest and least reliable at the exact moments she depends on it: at the doorstep (3 taps across 3 screens to mark delivered), when the route changes (8–15 minutes to arrive, no alert), and when signal drops (blank route offline).
- **Guardrail metric (M3), what must not drop or break:** Manager Compliance CSAT and compliance-record completeness

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** B1 · One-Click Compliance Checklist
This is the core of the hypothesis. Compliance is the largest single time gap (14.6 minutes against 3), it’s used daily by 77% of coordinators and 64% of drivers, and it rates 2.2 and 2.8. Pre-filling what the system already knows could take minutes off every shift. It’s only “quick” if it’s limited to pre-filling existing fields, not redesigning the compliance rules.

B6 · Driver Alert Notifications
This is the fastest way to keep Dana in the story. It targets a Critical bug (BUG-2044: route changes arriving 8–15 minutes late, with no alert) and the WhatsApp workaround (UXR-02). Push notifications usually build on existing infrastructure. One caveat: an alert only helps once the change reaches the server. If the lag is in the data sync itself, B6 hides the problem without fixing it.

B5 · Step Progress Indicator (cheap third)
It’s low effort and speaks to the drop-off pattern, where only 31% finish through handoff. But it’s the weakest of the three. It shows coordinators where they are without removing any minutes, so it could improve completion a little while leaving the 31 minutes untouched.

What I’d deliberately leave off for now

B7 (AI ETA) fixes adoption of a feature nobody asked for.
B8 (manager analytics) serves the happiest group (Reporting CSAT 4.5).
B10 (training) teaches people to work around complexity instead of removing it.

Assumption: B1 is really low effort. 
If pre-filling needs new data integrations, B3 (Shift Handoff Wizard, +6.8 minutes) may be the better second pick for impact per unit of effort.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** B4 Mobile-First Coordinator Dashboard: the AI scored it Value 3 and Effort 5 and put it on the Cut List. I changed it to Value 2 and Effort 3 and moved it to LATER. I lowered the value because it adds a new screen without removing any minutes from compliance. I lowered the effort because it can wrap B1 and B3 once they’re proven rather than rebuild Core Dispatch. I kept it in LATER, not cut, because mobile access may matter once the core flows work.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** Not the obvious ones. It cut B8 (from Sales) and B7 (an AI headline feature), and neither has interview support. The closest case is B9 Compliance Audit Trail Export (from Legal and CS), which the AI put in NOW. No interview mentions audits. The AI justified it only as protection for the manager guardrail, so it’s a defensible risk choice rather than evidence-backed demand.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** Yes: B2 Smart Daily Report Auto-Fill. The funnel shows the daily report is the last major leak: only 18% complete it, and it takes 6.7 minutes longer than benchmark. The AI scored B2 a Time Sinker (Value 3, Effort 4) because of the risk in AI-generated reports. A version that reuses B1’s pre-filled data, with no AI, could be Value 4 at lower effort. It’s worth rescoring once B1 is proven.

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** B1	One-Click Compliance Checklist	5	3	Major Project	Attacks the 14.6-minute step head-on, but pre-fill needs reliable source data and must keep records complete for the guardrail.
B3	Shift Handoff Wizard	4	3	Major Project	Targets the +6.8-minute handoff gap and the 31% completion rate, the supporting metric and the step tied to the M2 workarounds.
- **What I cut, and the “no” I’m protecting the scope from:** B7 Contextual AI ETA Display, B8 Fleet Analytics Manager View
- **Prototype/roadmap screenshot link (paste into your deliverables):** https://claude.ai/chat/6ac34017-7410-42c1-be57-749fd78a438a
https://app.notion.com/p/feature-roadmap-module4-c1ff557174dd82069c32812f83afbf5b?source=copy_link

**ROADMAP**
### NOW, Pilot (4 weeks, 3 accounts)

- **B1 One-Click Compliance Checklist**, scoped to pre-filling compliance fields the system already holds, with no new rules engine. This is the most direct test of the primary metric, and the narrow scope keeps it within reach for 2 engineers.
- **B9 Compliance Audit Trail Export**, built alongside B1 as guardrail insurance: if compliance forms change, managers can still produce complete records for audits.

### NEXT, GA Release (weeks 5-8)

- **B3 Shift Handoff Wizard**, the second-largest gap (+6.8 minutes) and the step where today’s WhatsApp and text workarounds take over; it extends B1’s gains to the supporting metric.
- **B5 Step Progress Indicator**, a one-point add that gives coordinators visibility across the newly improved compliance and handoff steps.
- **B6 Driver Alert Notifications**, compliance flags for drivers like Dana, the secondary persona. Route-change alerts should wait until the server-side sync delay (BUG-2044) is fixed.

### LATER, backlog

- **B2 Smart Daily Report Auto-Fill**, revisit once B1 shows pre-filled compliance data is accurate enough to feed reports without AI generation risk.
- **B10 In-App Coordinator Training**, revisit after the workflow is simplified, when there is less to train.
- **B4 Mobile-First Coordinator Dashboard**, revisit once B1 and B3 are proven, as a mobile wrapper for flows that already work rather than a parallel build.

### ✂ Cut List

- **B7 Contextual AI ETA Display**, no link to the persona’s friction or the primary metric.
- **B8 Fleet Analytics Manager View**, serves the most satisfied group and comes from Sales, not the frontline.

*Capacity note: effort scores assumed a larger squad. With 2 engineers, NOW (B1 + B9) is achievable only if B1 stays scoped to pre-fill, and NEXT (B3 + B5 + B6) is tight; B6 is the first item to slip.*

**WIREFRAME**
626f6c742d63632d6167656e74Here are low-fidelity wireframes of the three screens, based on the PRD and the prototype as it stands.

**Screen 1: Today's checks**

```
+--------------------------------------------------------------------------+
| [Truck] RouteLogic Velocity · North Ridge Depot              Jordan E.   |
+--------------------------------------------------------------------------+
| North Ridge Depot                                  +--------------------+ |
| Today's checks                                      | Time so far today  | |
| Tuesday 3 November 2026                             | 4.2 min            | |
| 6 checks due today: 0 done · 1 in progress · 5 not started              | |
|                                                     | [=====----]        | |
|                                                     | Target: 7 min      | |
|                                                     +--------------------+ |
| +----------------------------------------------------------------------+ |
| | Checks are now pre-filled                     [Switch to classic form] | |
| +----------------------------------------------------------------------+ |
| +----------------------------------------------------------------------+ |
| | Van 14        Marcus Hale         [In progress]        [ Resume -> ] | |
| | Route R-204                                                          | |
| |----------------------------------------------------------------------| |
| | Van 15        Priya Nair          [Not started]       [ Start check ->]| |
| | Route R-211                                                          | |
| |----------------------------------------------------------------------| |
| | Van 16        Tomasz Kowal        [Done]                Took 3:12      | |
| |----------------------------------------------------------------------| |
| | Van 18        Lee Okafor          [Defect reported]     Took 4:01      | |
| +----------------------------------------------------------------------+ |
+--------------------------------------------------------------------------+
```

**Screen 2: Compliance checklist**

```
+--------------------------------------------------------------------------+
| < Back to today's checks                       Switch to classic form    |
|                                                                          |
| +----------------------------------------------------------------------+ |
| | Compliance check                                  Time on check 2:14 | |
| | Van 14                                                               | |
| | Marcus Hale · Route R-204 · Departs 06:10                            | |
| +----------------------------------------------------------------------+ |
| [Few values available notice - only if many fields are missing]          |
|                                                                          |
| +------------------------------------------+  +------------------------+ |
| | NEEDS YOUR ANSWER                        |  | PROGRESS               | |
| | Pre-trip inspection   (Pass) (Fail)      |  | 2 of 3 answers given   | |
| | Defects found         (Yes) (No)         |  | [====----]             | |
| |   Describe the defect: [__________]      |  |                        | |
| | Driver hours confirmed (Yes) (No)        |  | STILL NEEDED           | |
| +------------------------------------------+  | - Driver hours        | |
| +------------------------------------------+  | - Confirm odometer    | |
| | NEEDS A QUICK LOOK                       |  |                        | |
| | Odometer   118442   [Last updated        |  | Fields complete 5 of 10| |
| |            yesterday]  [edit]            |  |                        | |
| |  [ ] Confirm this value is still correct |  | [ Submit check -> ]    | |
| | Trailer ID  No value on file             |  |  (disabled until done) | |
| |  [________________ Enter this value]     |  +------------------------+ |
| +------------------------------------------+                             |
| +------------------------------------------+                             |
| | PRE-FILLED FOR YOU                 v     |                             |
| |  (collapsed by default)                  |                             |
| +------------------------------------------+                             |
+--------------------------------------------------------------------------+
```

**Screen 3: Check submitted**

```
+--------------------------------------------------------------------------+
| (check)  Check submitted for Van 14                                      |
|          10 of 10 fields complete                                       |
|                                                                          |
| EDITED FIELDS                                                            |
| +----------------------------------------------------------------------+ |
| | Odometer          Was 118442          Now 118510                     | |
| +----------------------------------------------------------------------+ |
|                                                                          |
| +-------------------------------+  +-----------------------------------+ |
| | Time for this check           |  | Today's total                     | |
| | 6:48                          |  | 11.4 min of 7 min target          | |
| +-------------------------------+  +-----------------------------------+ |
|                                                                          |
| < Back to today's checks                 [ Next check: Van 15 -> ]        |
+--------------------------------------------------------------------------+
```

Two notes: the wireframes show the intended layout, not the final visual style, and the "Switch to classic form" links are still placeholders in the prototype. I can also turn these into a clickable HTML wireframe if you want to review them in a browser.
