# FDE Framework

A Claude skill that turns a customer's stated problem into the one worth solving, using six Forward Deployed Engineering translation levers.

---

## The problem this solves

An **ordinary problem** is what a customer describes when they ask for help. An **extraordinary problem** is what they actually need — usually something they cannot articulate because they are too close to their own situation.

The gap between the two is where defensible systems get built. Most problem statements never cross it. They get tidied, formatted, and shipped as a brief that describes a symptom, mirrors the customer's words, and produces automation rather than intelligence.

This skill is machinery for crossing that gap. It restates a problem from six angles the customer has not considered, then synthesises the sharpest into a single actionable statement — and checks its own output to confirm the problem actually changed rather than just getting better vocabulary.

---

## Before and after

**Ordinary:**

> "Our risk analysts spend three days every month assembling the regulatory exposure report. Can you automate the report generation?"

**Extraordinary:**

> Capture the analyst override trail as first-class data and encode it into a decision trace that proposes exposure adjustments with the institution's own reasoning attached — turning a three-day assembly task into a defensible, self-improving judgment layer that answers regulator challenges directly.

The first problem is a document pipeline whose value is capped at the labour it replaces. The second is an institutional judgment asset that compounds with use and cannot be replicated by a competitor. Different build, different data model, different buyer conversation.

---

## The six levers

| Lever | The question it forces |
|---|---|
| **Economic Forces** | Will someone pay for this? Name the customer, quantify the value in dollars or hours. Functions as a gate — a problem that fails it can still be interesting, but should be labelled a research problem, not a business one. |
| **Data Liquidity** | What data is dormant, discarded, or never combined? Every organisation throws away data worth more than the systems built to collect it. |
| **Algorithmic Leverage** | Can this domain's decision-making be encoded into a decision trace no competitor has? About *how decisions are made*, not the code that implements them. |
| **Network Effect** | Does solving this for one customer make it better for the next? Name the feedback loop, or its absence. |
| **First Principles** | What is the irreducible truth of what the customer wants, stripped of interface, history, and habit? |
| **Job To Be Done** | What job are they hiring this to do? The stated request and the actual job are almost always different. |

First Principles and JTBD are strongest run as a pair.

---

## Modes

The levers are independent. Apply them in any order — lead with whichever one the problem is most obviously blind to.

- **Full pass** (default) — all six levers, then synthesis. For new problems, discovery, and proposals.
- **Quick pass** — the three highest-yield levers for the problem at hand, then synthesis. For time-boxed work.
- **Single lever** — one lever in depth. `"Run data liquidity on this"`.

The skill will not write an extraordinary problem statement from fewer than three levers. The first framing of a problem is almost always the ordinary one, and one or two levers rarely move it far enough.

---

## Install

**Claude.ai** (Free, Pro, Max) — download `fde-framework.skill` from Releases, then go to **Customize → Skills** and upload it. Code execution must be enabled under Settings → Capabilities. On Team and Enterprise plans, skills are managed under **Organization settings → Skills**.

**Claude Code** — clone into your skills directory:

```bash
# personal — available in every project
git clone https://github.com/<your-username>/fde-framework.git ~/.claude/skills/fde-framework

# project — travels with the repo
git clone https://github.com/<your-username>/fde-framework.git .claude/skills/fde-framework
```

The path must resolve to `<skills-dir>/fde-framework/SKILL.md`. Nesting one level too deep is the most common install error.

**Claude Developer Platform** — upload via the Skills API (`/v1/skills`).

---

## Use

The skill triggers on its own when you describe a customer problem, project brief, feature request, or product idea and ask for it to be sharpened, reframed, or pressure-tested. You do not need to name it.

```
Here's the brief from yesterday's discovery call: [...]. Sharpen this.
```

```
Run just the data liquidity lever on this problem statement.
```

```
Is this worth building? [...]
```

To invoke it explicitly in Claude Code: `/fde-framework`.

---

## Output structure

A full pass produces:

- **Ordinary problem** — verbatim, as stated
- **Context and assumptions** — inferences marked explicitly so they can be corrected
- **Lever analysis** — one section each, with honest "this lever doesn't apply because…" where true
- **Extraordinary problem** — one synthesised statement, naming which levers drove it
- **What changed** — how this differs from the ordinary framing, and what you'd now build that you wouldn't have before
- **Technical debt to name now** — predictable failure modes at design time: data drift, stale context, missing guardrails, model coupling

---

## Design notes

Three choices worth knowing about if you plan to fork it:

**Levers are allowed to fail.** A lever that genuinely produces nothing is reported as such. Forcing six sections of content onto a problem that only supports three produces confident filler, which is worse than a gap.

**Synthesis picks, it doesn't average.** The failure mode for frameworks like this is six sections of decent analysis followed by a conclusion that blends them. The skill is instructed to choose the one or two strongest levers and build from those.

**The output is checked against the input.** Before delivering, the skill puts the ordinary and extraordinary statements side by side. If they differ in polish rather than substance, it rewrites rather than appending a caveat.

---

## Built on

The framework draws on Jobs To Be Done (Christensen's milkshake study), and on patterns visible in how AI-native companies build moats — intelligence held in the retrieval and context layer rather than the model layer, so that a model upgrade is a swap and not a migration.

---

## Author

**Sanjaya Kumar Panigrahy**

## Contributing

Issues and pull requests welcome — particularly worked examples from domains not yet represented, and cases where a lever produced a genuinely surprising reframing.
