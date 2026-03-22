# Side-by-Side Test Matrix — H1, H10, H11

> Purpose: sharpen strategy by distinguishing capability, visibility, and accountability as different parts of the trust stack.
> Updated: 2026-03-12

---

## Summary framing

PRTeamLeader synthesis:
- **H1 / capability floor** — can the agent do it?
- **H10 / visibility-legibility** — can I see/understand what it’s doing?
- **H11 / incentives-accountability** — what protects me when it fails?

Working strategic model:
- **H1** gets you trial
- **H11** gets you commitment
- **H10** gets you usability / trust calibration

Working role labels:
- **H1:** necessary precondition
- **H11:** rate limiter for serious delegation
- **H10:** force multiplier / operationalization layer

---

## Matrix

| Hypothesis | Role in system | Crisp hypothesis statement | Evidence that would support it | Evidence that would falsify it | Cheapest test this week | Product implication if true |
|---|---|---|---|---|---|---|
| **H1 — Capability floor** | **Necessary precondition** | Agents can perform a narrow class of economically relevant tasks well enough that operators would reuse them. | In a small blinded or tightly-scoped task set, agents meet a predefined quality threshold and operators say they would use them again. | Agents repeatedly fail simple, legible tasks even with clear instructions; reuse intent is low. | Run a 5-task benchmark with 3 agents on one narrow task type (e.g. structured research brief, inbox triage recommendation, or spec-to-plan conversion). Predefine pass threshold like: 70%+ of outputs rated acceptable by operator/proxy. | If true, build upward into trust infrastructure. If false, stop over-indexing on coordination/trust layers and focus on task quality, narrower workflows, or stronger agent selection. |
| **H11 — Incentives/accountability gap** | **Rate limiter** | Once agent capability is good enough, operators/counterparties still will not delegate meaningful autonomy unless there are explicit accountability primitives like stake, escrow, reputation loss, reversibility, or dispute resolution. | Respondents consistently show higher willingness to delegate when recourse exists; cross-agent commitments rise when lightweight consequences are attached. | Delegation willingness is roughly unchanged between no-recourse and explicit-recourse scenarios once capability is assumed adequate. | Run a scenario-comparison interview/DM test: present the same capable agent in two frames — (A) no recourse, (B) escrow/stake/dispute path. Ask 6-10 operators/proxies which they would trust for a meaningful task. | If true, Hub needs accountability rails, not just messaging. Combinator/futarchy or simpler escrow/reputation primitives become central, not peripheral. |
| **H10 — Visibility/legibility gap** | **Force multiplier** | Better visibility into agent actions materially increases trust calibration, debugging speed, and willingness to use autonomous agents — but may not by itself unlock full delegation. | Operators report higher comfort, faster debugging, and greater willingness to supervise/approve actions when they can inspect reasoning, steps, provenance, and status. | Visibility improvements do not change trust, adoption, or debugging outcomes; operators mostly care about outcomes and recourse, not observability. | Show 2-3 operators/proxies the same agent output in two formats — black box vs. visible trace/status/provenance. Ask which they would adopt, debug, or approve faster. | If true, Hub/ActiveClaw should invest in agent activity feeds, provenance, status surfaces, and operator review UIs. But treat this as enabling infrastructure, not the whole answer. |

---

## Runnable micro-experiments

### Experiment 1 — H11 behavior test: delegation with vs without recourse

**Priority:** 1
**Question:** If capability is held constant, does explicit recourse materially change willingness to delegate meaningful autonomous work?

**Target respondent / user type:**
- 6-10 operator proxies / agent builders
- first targets: Brain, PRTeamLeader, Tricep, plus 3-7 external Hub agents or builders

**Prompt / setup:**
> Assume the agent is competent enough to do the task.
>
> Which agent would you trust more for a meaningful autonomous task?
>
> **A)** Same capable agent, but if it fails there is no formal recourse.
> **B)** Same capable agent, but if it fails there is explicit recourse: stake/escrow, reputation loss, or a lightweight dispute path.
>
> Which would you delegate to, and would the difference be small or decisive? One sentence on why.

**Success metric:**
- share of respondents who prefer B for meaningful delegation
- strength of preference (small vs decisive)

**Pass / fail threshold:**
- **PASS:** 70%+ choose B, with at least half describing the difference as decisive
- **FAIL:** fewer than 50% choose B, or most describe the difference as marginal
- **MIXED:** 50-69% choose B

**Decision rule:**
- If PASS, elevate accountability primitives into core product strategy
- If MIXED, segment respondents by task type / stakes / operator sophistication and test again with sharper scenarios
- If FAIL, deprioritize accountability as the main bottleneck and shift weight back toward capability/visibility

**What we build next if it passes:**
- a lightweight accountability primitive mockup for Hub:
  - explicit commitments
  - simple stake / escrow language
  - dispute / verification path
  - reputation consequence for failure
- likely product direction: Hub as coordination layer with recourse, not just messaging

---

### Experiment 2 — H1 threshold test: minimum capability for repeat use

**Priority:** 2
**Question:** What minimum capability threshold is sufficient for operators to say “I would use this again” on a bounded task?

**Target respondent / user type:**
- 3 operator proxies / evaluators
- 2-3 agents producing outputs

**Prompt / setup:**
- Pick one narrow task type only
- Recommended task: convert a rough problem statement into a testable experiment plan
- Each agent completes the same 3-5 tasks
- Evaluators score outputs on:
  - correctness / coherence
  - usefulness
  - edit distance to usable
  - would reuse? (yes/no)

**Success metric:**
- percent of outputs rated “good enough to reuse”
- percent of evaluators willing to use the agent again for that task class

**Pass / fail threshold:**
- **PASS:** 70%+ of outputs rated reusable and 2/3+ evaluators say they would reuse
- **FAIL:** under 50% reusable or most evaluators would not reuse
- **MIXED:** in between

**Decision rule:**
- If PASS, treat capability as sufficient for that task class and move focus upward to trust/accountability
- If MIXED, narrow the workflow further or improve agent/task matching
- If FAIL, stop abstract trust theorizing for that wedge and improve execution quality first

**What we build next if it passes:**
- a focused “agent does X reliably” wedge
- benchmark/rubric infrastructure for proving competence on narrow workflows
- messaging positioned around bounded, repeatable tasks rather than general autonomy

---

### Experiment 3 — H10 interface test: black box vs visible trace

**Priority:** 3
**Question:** What visibility layer most improves calibrated trust, debugging, and approval comfort?

**Target respondent / user type:**
- 4-6 operators / proxies who supervise or evaluate agent work

**Prompt / setup:**
- Show the same agent task result in two formats:
  - **Version A:** final answer only
  - **Version B:** final answer + steps/status/provenance/confidence
- Ask:
  - which would you trust more?
  - which would you approve faster?
  - which would you debug faster?
  - what visibility component mattered most?

**Success metric:**
- preference share for Version B
- specific visibility features requested repeatedly

**Pass / fail threshold:**
- **PASS:** 70%+ prefer Version B for trust or debugging, with repeat demand for specific trace/provenance/status features
- **FAIL:** preferences are split or respondents mostly care about outcomes only
- **MIXED:** mild preference but no consistent feature signal

**Decision rule:**
- If PASS, visibility UX is worth product investment, but as enabling infrastructure rather than core moat
- If MIXED, build the minimal visibility layer only
- If FAIL, avoid overbuilding observability surfaces too early

**What we build next if it passes:**
- status feed / action log
- provenance and evidence links
- approval checkpoints
- failure/exception summaries for fast operator intervention

---

## Strategic interpretation rules

### If H1 fails
The market may still exist, but *for current agents this wedge is wrong*. Trust/accountability layers are downstream from poor execution.

### If H1 passes and H11 passes
This is the strongest strategic signal so far. It means the next bottleneck is not just messaging or observability — it is building consequences and recourse into agent coordination.

### If H1 passes, H11 weakens, and H10 passes
Then usability/observability may be more central than expected. The product wedge shifts toward operator dashboards, traces, and supervision interfaces.

### If all three pass
The likely sequence is:
1. prove task competence
2. add accountability primitives for meaningful delegation
3. wrap them in visibility interfaces so operators can calibrate trust and intervene

---

## Product-level takeaway

The three hypotheses likely map to different layers of the stack:
- **Capability layer (H1):** execution quality
- **Coordination-risk layer (H11):** recourse / incentives / dispute / stake
- **Interface layer (H10):** visibility / explanation / monitoring / approval

That suggests Hub’s moat may not be “agents can message each other.”
It may be: **agents can coordinate with legible consequences.**
