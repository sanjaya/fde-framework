---
name: fde-framework
metadata:
  author: Sanjaya Kumar Panigrahy
  version: "1.0.0"
license: proprietary
description: Converts an ordinary problem statement into an extraordinary one using the six Forward Deployed Engineering translation levers (Economic Forces, Data Liquidity, Algorithmic Leverage, Network Effect, First Principles, Job To Be Done). Use this whenever someone describes a customer problem, a project brief, a feature request, a use case, a discovery-call summary, a proposal, or an AI/product idea and wants it sharpened, reframed, pressure-tested, or turned into something defensible — even if they never say "FDE" or "extraordinary problem." Also use when someone asks "is this worth building," "how do we differentiate here," "what should we actually solve," or wants a single lever applied on its own.
---

# FDE Framework: Ordinary → Extraordinary Problem

## The core distinction

An **ordinary problem** is what the customer describes when they ask for help. An **extraordinary problem** is what the customer actually needs — usually something they cannot articulate because they are too close to their own situation.

The gap between the two is where defensible systems get built. Everything below is machinery for crossing that gap.

Your job is not to be agreeable about the customer's framing. It is to restate their problem from angles they have not considered, and to end up somewhere they could not have written themselves. **If the final problem statement is a tidier version of the input, the run has failed.**

## Workflow

### 1. Capture the ordinary problem verbatim

Write the problem exactly as it arrived — the customer's words, unpolished, symptom and all. Do not improve it yet. This is the baseline you will be judged against, so it needs to be honest.

If the input is a long brief or transcript, compress it to one or two sentences that a person in that room would recognize as what was actually said.

### 2. Establish context — but don't stall

To run the levers well you need: the domain, who the paying customer is, what they do all day, and what data or systems already exist. If those are missing, ask **at most two or three** targeted questions.

If the user wants to keep moving, proceed with explicit assumptions instead. Label them clearly (`Assumption: ...`) so they can be corrected rather than silently inherited. A run built on stated assumptions is far more useful than an interrogation.

### 3. Choose the mode

| Mode | When | What to run |
|---|---|---|
| **Full pass** (default) | New problem, discovery, proposal, "make this sharper" | All six levers, then synthesis |
| **Quick pass** | Time-boxed, or the problem is already partly framed | The three highest-yield levers for this problem, then synthesis |
| **Single lever** | User names one ("run data liquidity on this") | That lever only, in depth, no synthesis unless asked |

The levers are independent. Apply them in any order — lead with whichever one the problem is most obviously blind to. **Never run fewer than three before writing an extraordinary problem statement**; the first framing is almost always the ordinary one, and one or two levers rarely move it far enough.

### 4. Apply the levers

See the lever reference below. For each one, write 3–6 sentences of substance, not a restatement of the question. Where a lever produces nothing real, say so and say why — a lever that genuinely doesn't apply is a finding, not a gap to fill with filler.

### 5. Synthesize

Pick the one or two strongest levers and fold them into a single problem statement. Not a summary of all six — a synthesis of the sharpest. Then run the quality check.

---

## The six levers

### Lever 1 — Economic Forces
**Ask:** Does this problem have economic value? Will someone pay for a solution?

Efficiency, productivity, new revenue, or cost reduction means economic force. Elegance or completeness means it is a research problem, not an FDE problem.

**Test:** Name a specific customer who would pay, and quantify the value in dollars or hours. If you cannot, say so plainly — that is the most useful output this lever produces.

This lever functions as a gate. A problem that fails it can still be interesting, but should be labeled as such rather than dressed up as a business case.

### Lever 2 — Data Liquidity
**Ask:** What data is dormant, discarded, ignored, or never combined — that would make this solvable in a fundamentally new way?

Every organization throws away, ignores, or stores-but-never-analyzes data that is often worth more than the systems built to collect it. Ask specifically: **what data does this customer produce but not use?** Exhaust logs, rejected records, overrides, annotations, drafts, timestamps, reasons-for-decline, support threads, version history.

Patterns worth mining for: *ignored* data (Perplexity treating web citations as primary raw material), *discarded* data (Manus treating error logs as a learning signal), *uncombined* data (a legal AI treating case-law cross-references as a moat; a fintech combining satellite imagery with government digitization records to score farmers banks had always excluded).

### Lever 3 — Algorithmic Leverage
**Ask:** Can this domain's decision-making be encoded into a decision trace no competitor has?

This is about **how decisions are made**, not the code that implements them. Underwriters hold a mental model of risk; lawyers of precedent; farmers of soil and yield. That institutional judgment lives in human heads and paper processes.

*Decision* and *human judgment encoded* are the two keywords. Not human-in-the-loop — **encoded**: taken out of heads, formalized, made consistently applicable at scale. Output should name the actual decisions, the inputs experts weigh, and where their judgment diverges from the written policy — that divergence is usually the real asset.

### Lever 4 — Network Effect
**Ask:** Does solving this for one customer make it better for the next?

A system that improves with each user, transaction, correction, or data point builds a moat that scales on its own. For AI systems the mechanism is usually a feedback loop: interactions generate data, data improves performance, performance attracts users.

Design the loop explicitly. Name where it lives, what signal it captures, and how the system is measurably better at 1,000 users than at 10. If it produces identical quality on day 1 and day 365, say so — that is a product, not a compounding advantage.

### Lever 5 — First Principles
**Ask:** What is the irreducible truth of what this customer actually wants?

Strip away the interface, the history, the habit, and the workaround. Get to the most basic statement of the desired outcome.

Perplexity's first principle: someone who types a question wants an answer, not a list of links to search through. Google habituated users to links for twenty years; the first-principles answer was obvious and abandoned for commercial reasons. **That gap — between what exists and what the first principle demands — is where extraordinary problems live.** Name the gap explicitly.

### Lever 6 — Job To Be Done
**Ask:** What job is the customer hiring this to do?

Customers do not buy features. They hire products to do a job they currently do imperfectly, inconveniently, or expensively.

The milkshake case: a chain wanted to sell more milkshakes and asked about flavors. A researcher instead asked when people bought them and what they were trying to accomplish. Peak sales were the morning commute — customers were hiring the milkshake to occupy a long drive, keep them awake, and be sippable without spilling. The competitor was a banana, not another milkshake. Redesigned around those jobs (thicker, optimized straw, cup-holder fit), sales rose without the taste changing.

For AI systems the job is rarely the stated request. An underwriter asking for faster risk scoring is hiring it to close more profitable policies with fewer rejections. A lawyer asking for document summarization is hiring it to spend client time on strategy instead of reading.

**List every job the system does that the user would otherwise do manually.** The longer that list, the more they will pay. JTBD is the checklist of value. Pair this lever with First Principles — they are strongest run together.

---

## Output format

Use this structure for a full or quick pass:

```
## Ordinary problem
[Verbatim, as stated. One or two sentences.]

## Context and assumptions
[Only what's needed. Mark inferences as Assumption:]

## Lever analysis

### Economic Forces
[Named payer, quantified value, or an honest "fails this gate because..."]

### Data Liquidity
[Specific dormant/discarded/uncombined data assets, named]

### Algorithmic Leverage
[The decisions, the expert judgment, what encoding it unlocks]

### Network Effect
[The feedback loop, or its absence and what would create one]

### First Principles × Job To Be Done
[The irreducible want; the gap; the list of jobs being hired for]

## Extraordinary problem
[One specific, actionable statement synthesized from the strongest
levers. Name which levers drove it.]

## What changed
[One or two sentences: how this differs from the ordinary framing,
and what you'd now build that you wouldn't have before.]

## Technical debt to name now
[Predictable failure modes: data drift, stale context, missing
guardrails, model coupling. Name them at design time.]
```

For single-lever mode, output only the relevant section plus a short "so what" — how this lever alone changes the problem.

---

## Quality checks before delivering

Run these against your own output. Fixing a failure means rewriting, not appending a caveat.

1. **Did the problem actually change?** Put the ordinary and extraordinary statements side by side. If they differ in polish rather than substance, you built automation, not intelligence. Go back and run a lever you skipped.
2. **Is the extraordinary problem specific enough to act on?** It should imply a first build, a first dataset, and a first evaluation. "Improve risk insight" is not a problem statement.
3. **Is algorithmic leverage about decisions, not code?** If the section describes a clever implementation instead of encoded domain judgment, it's wrong.
4. **Is there a feedback loop?** If the system is no better after a year of use, say so explicitly rather than quietly leaving the lever empty.
5. **Did you solve the job or the feature?** The stated request and the actual job are almost always different. Faster ticket resolution → never filing the ticket. Better search results → reaching a decision in seconds.
6. **Is technical debt named?** Production AI systems usually fail from drifted data, stale context, or a missing guardrail — not a wrong model. These are predictable at design time, so inventory them there.
7. **Is the design model-agnostic?** Intelligence should sit in the retrieval, context, and evaluation layers — the 80% you control. The model is a plug-in, not a foundation. If a model upgrade would be a migration project, flag it.

---

## Worked example

**Ordinary problem:** "Our risk analysts spend three days every month assembling the regulatory exposure report. Can you automate the report generation?"

**Economic Forces:** 12 analysts × 3 days × 12 months ≈ 430 analyst-days a year. Real, quantifiable, and someone owns that budget line. Gate passed — but note that automation alone caps the value at the labor cost, which is the ceiling of the ordinary framing.

**Data Liquidity:** The report is the output; the discarded material is richer. Analysts make hundreds of manual adjustments, exclusions, and overrides while assembling it — reclassifying an exposure, excluding a counterparty, footnoting an anomaly. None of that is captured. It exists as spreadsheet edits and email threads, then disappears. That override trail is a dormant, unmatched record of how this institution actually interprets its own exposure.

**Algorithmic Leverage:** Those overrides encode real judgment that no written policy contains — the gap between the documented rule and what the senior analyst actually does. Encoding that as an explicit decision trace produces something no vendor can replicate, because it is derived from this bank's own history.

**Network Effect:** Each report cycle generates fresh override signal. Adjustments the system predicts correctly reinforce the trace; ones it misses become training cases. Coverage compounds monthly and across risk domains — an override pattern learned in credit often generalizes to market exposure.

**First Principles × JTBD:** Nobody wants a report. They want to answer a regulator's question with confidence and defend the answer. Jobs being hired for: locate the exposure, decide whether it needs adjusting, justify the adjustment, survive the challenge, and repeat consistently next quarter. Automating document assembly does the first job and none of the other four.

**Extraordinary problem:** *Capture the analyst override trail as first-class data and encode it into a decision trace that proposes exposure adjustments with the institution's own reasoning attached — turning a three-day assembly task into a defensible, self-improving judgment layer that answers regulator challenges directly.* (Driven by Data Liquidity and Algorithmic Leverage.)

**What changed:** The ordinary problem was a document pipeline with a ceiling equal to 430 analyst-days. The extraordinary problem is an institutional judgment asset that compounds and is not replicable by a competitor. Different build, different data model, different buyer conversation.

**Technical debt to name now:** override capture depends on analysts working inside the instrumented path — if they revert to spreadsheets the signal dies; regulatory definitions drift, so the trace needs a versioned policy anchor; and the justification layer needs a guardrail against confidently defending an adjustment it inferred from a single stale precedent.
