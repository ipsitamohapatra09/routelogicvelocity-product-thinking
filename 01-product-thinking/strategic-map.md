# Strategic Discovery Map

> **Module 1 · Lab 1.** Repo file `01-product-thinking/strategic-map.md` — part of your submission.
> Do the lab in the **Module 1 · Exercise 1 Guide** (linked from the Module 1 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It's the discovery groundwork behind your `problem-hook.md`.

## Responses

- **Feature with no strategic answer (why is this a 12-week priority?):** Weeks 1–3: Logging

  Why first: Every other feature reads from this data. Goals, insights and streaks all have nothing to work with until logging exists.

  Strategic bet: The biggest reason people stop using water apps is friction. If logging takes more than one tap, nothing built later will save retention. So quick-add and custom cup sizes come first, not polish.

  Why “other drinks” is included: Without it, users who drink tea or coffee see wrong totals and lose trust in the app early.

  What it unblocks: The data model (entries, volumes, timestamps) that everything else is built on.

- **Feature that looks "correct" but has zero strategic weight:** Water type tagging: let users tag each drink as tap, filtered, sparkling, or a specific bottled brand, with a breakdown chart of “your water sources this week.”

  Why it looks correct: It fits the product, sounds like richer data, and would demo nicely in a sprint review. It even suggests future ideas like brand partnerships or water quality insights.

  Why it has zero strategic weight:

  No user asked for it. None of the core needs (know how much, log fast, remember, see progress, stay motivated) depend on where the water came from.

  No link to revenue. There’s no premium tier, partnership, or retention metric it clearly moves. “Brand partnerships someday” is a guess, not a plan.

  It works against the core loop. Adding a tag to every log adds friction to the one action that already has the biggest drop-off risk: logging.

  It doesn’t change behavior. Knowing that 60% of your water was filtered doesn’t make you drink more.

  What would give it weight: user interviews where people bring up water sources unprompted, a tested partnership deal with a filter or bottled water brand, or data showing that users who tag more retain better. Without any of those, it stays in the backlog.

- **V3 vs your Step 1 baseline — what changed, and was it your PM knowledge that forced usefulness?:** What changed

  The Step 1 baseline was a feature inventory: six branches (logging, goals, reminders, insights, motivation, integrations), each with three sub-features. It answered "what could this app have?" and nothing else. It had no user, no reasoning, no priorities, and no risks.

  V3 answers different questions:
  - **Who it's for:** busy adults 25–40 who know they should drink more but forget. That one constraint reshaped everything, from the jobs ("remember without breaking focus") to the friction ("notifications blend into noise") to the tone ("existing apps feel childish").
  - **Why each thing matters:** features are tied back to jobs and ranked by effort and impact, so some get killed (smart bottles, leaderboards, AI coach) instead of everything being listed as equal.
  - **How it makes money and how it fails:** monetization tradeoffs and retention risks didn't exist in the baseline.
  - **Where reasonable people would disagree:** the six tensions are the most useful part for a sprint, because they turn a map into a discussion agenda.

  Did the AI get smarter?

  No. It's the same model across every version in this conversation. Everything in V3, including JTBD framing, effort/impact quadrants, the "streaks cause quitting" risk, and B2B privacy concerns, was available at Step 1. It just wasn't asked for, so it didn't show up. A vague prompt gets the most generic reasonable answer, and a generic mindmap for a water app is a feature list.

  So was it your PM knowledge?

  Mostly, yes. Your prompt did three things the first one didn't:
  1. **Named a specific user and their problem.** This is the biggest change. "People who know but forget" means the product is about cues and friction, not education.
  2. **Imposed frameworks.** JTBD, effort/impact and retention forced reasoning, not just listing. A framework is a set of questions the output has to answer.
  3. **Asked for tensions.** This explicitly permitted disagreement and tradeoffs, which models tend to smooth over unless told otherwise.

  Your iterations in between also helped. The "zero strategic weight" exercise and the engineer's "why this priority" question pushed toward justification, which carried into V3.

  A small part came from the model, not the prompt. You asked for tensions, but not which ones. Spotting that "success means the user leaves" is a business-model problem, or that B2B distribution conflicts with health data trust, is the model applying domain knowledge once the frame allowed it. The prompt opened the door, and the model's knowledge filled the room.

  Is V3 objectively better?

  It's better for a discovery sprint, which is what it was built for. It isn't better in every way:
  - If someone needed a quick feature inventory to start a spec, the baseline did that in one glance, and V3 is slower to read.
  - V3 looks more authoritative, but it's still entirely hypotheses. None of the jobs, friction points or impact rankings come from real users. The polish can make unvalidated guesses look like findings, which is a real risk in a sprint.
  - The effort and impact rankings are rough judgment calls, not estimates from your engineering team.

  The takeaway: the quality of the output tracked the quality of the question, not the capability of the model. The AI is a good amplifier of the thinking you bring. It won't supply the strategic frame on its own, and it can't replace the user research that would turn V3's hypotheses into facts.

- **Key takeaway: how does this prove the PM’s role is to think while the AI’s role is to execute?:** The takeaway: the quality of the output tracked the quality of the question, not the capability of the model. The AI is a good amplifier of the thinking you bring. It won’t supply the strategic frame on its own, and it can’t replace the user research that would turn V3’s hypotheses into facts.
