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
