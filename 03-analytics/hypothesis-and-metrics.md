# Hypothesis & Success Metrics

> **Module 3 · ★ Deliverable 3.** Repo file `03-analytics/hypothesis-and-metrics.md` — part of your submission.
> Do the lab in the **Module 3 · Exercise Guide** (linked from the Module 3 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It feeds the **Problem, Value & Hypothesis** slide of your Module 6 final deck.

## Finalized product hypothesis

> Based on an enterprise ops manager saying frontline staff “use maybe 5% of it and can’t find that 5%” (UXR-04), and data showing compliance checks take 14.6 minutes against a 3-minute benchmark with a CSAT of 2.2, I believe that streamlining compliance logging and shift handoff for frontline coordinators—including the compliance steps drivers complete in the field—will result in the dispatch workflow being completed inside the product instead of through manual workarounds. Success is a 50% reduction in median coordinator compliance-check time, from 14.6 to about 7 minutes. I will protect manager Compliance CSAT (3.9 or above) and compliance-record completeness, and make a go/no-go decision after a six-week pilot across 3–5 accounts, following a two-week baseline.

## Success metrics

| Metric | Type | Target | Why it matters |
|---|---|---|---|
| Share of coordinators completing the dispatch workflow through shift handoff in the product | North-star | Increase from 31% toward 50% during the pilot | Shows whether coordinators complete the workflow in RouteLogic Velocity instead of finishing through texts, WhatsApp, and paper. |
| Median time to log compliance checks per coordinator per day | Leading indicator | Reduce by 50%, from 14.6 minutes to about 7 minutes, by week 6 | Tracks the largest identified workflow time gap and is an initiative signal that can move sooner than NPS or churn. |
| Manager Compliance CSAT and compliance-record completeness | Guardrail | CSAT remains at or above 3.9; record completeness does not decline | Protects managers who rely on complete compliance records and ensures faster logging does not shift burden to buyers. |

**Pilot decision rule:** Scale if compliance-check time falls by at least 50% and guardrails hold; iterate at a 25–49% reduction; pivot to shift handoff or stop below 25%. Pause if manager Compliance CSAT falls below 3.5 or records become less complete. Minimum threshold to proceed: at least a 25% reduction with both guardrails holding.
