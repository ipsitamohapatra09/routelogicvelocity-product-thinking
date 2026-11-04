# Individual Insights: Development Process

> Module 6 · Launch Impactful GTM Plans, ★ Deliverable 6 (reflection)
>
> _The personal reflection that closes your final project._

## Friction points

_The biggest technical or strategic challenge you faced while developing your product concept._

My biggest challenge was letting the evidence overrule a story I had already committed to. My Module 1 hook said coordinators were "losing hours every shift" to a system built for admins, and my Module 2 research pointed to drivers and reliability: crashes, offline routes and slow route changes. I built a reliability-first strategy and a full future-state journey for Dana, a delivery driver. Then the Module 3 data showed something different. Coordinators were losing about 31 minutes a day, not hours, and the biggest single gap was compliance logging (14.6 minutes against a 3-minute benchmark), which none of my interviews had mentioned. Re-centring the plan on coordinators and compliance meant demoting a persona and a journey I had worked hard on, and being honest about it in the brief instead of quietly rewriting history.

The second challenge was designing a test that could actually give a clean answer. My first variant bundled several changes (pre-fill, a progress panel, a visible timer), my primary metric could be gamed by coordinators logging fewer checks, and one guardrail (record completeness) could never fail because the form enforced it. Each looked reasonable on its own; together they would have produced a result nobody could trust.

## Key learnings

_A few surprising discoveries or insights you gained from the course overall._

- **Qualitative and quantitative evidence answer different questions.** Interviews told me why people work around the product; the data told me where the time actually goes. Neither alone would have found compliance logging as the target.
- **Summary lines lie more often than tables.** Several data snapshots overstated their own numbers: "69% abandon after route assignment" was really drop-off spread across three steps, and "Compliance is the lowest-rated" ignored that Reporting scored lower. Reading the table, not the headline, changed what I could defensibly claim.
- **AI output needs the same scrutiny as a junior analyst's.** The AI synthesis merged two unrelated sources into one cause and turned single quotes into patterns ("rural drivers" from one driver). It also smoothed vivid frustrations into generic bullets. It was fast and useful, but only after I checked every claim against its source.
- **The MDE is not the ship bar.** Simulating the experiment showed that a feature truly delivering my 25% target would ship only about half the time under my original rule, because noise would push the measured result below 25%. I would never have caught that by reasoning alone.
- **A launch plan defaults to awareness unless you fight it.** My first GTM draft had LinkedIn ads and trade press for a feature that only existing coordinators can use. Starting from the goal (conversion inside about 20 at-risk accounts) cut those channels and made the plan smaller, cheaper and more honest.

## Aha! moment

_Your main "aha" moment during the project process._

My aha moment came when I asked how the final hypothesis would affect Dana, the persona I had built the journey around, and the honest answer was "not much." The data had moved the bet to coordinators and compliance, while Dana's real pains (crashes, offline routes, three taps to mark delivered) sat outside its scope. I realised that a persona is a hypothesis, not a commitment: its job is to point you at the evidence, and when the evidence points somewhere else, the persona has done its job. Choosing to keep Dana as a secondary persona, adding drivers' compliance steps to the pilot instead of pretending the plan served her fully, was the moment the project stopped being a story I was defending and became a bet I could test.
