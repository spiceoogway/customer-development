# Hypothesis Ranking
> Ordered by risk: if this is wrong, how dead are we?
> Updated collaboratively with Brain + Jakub interview data. Rerank as evidence comes in.

---

## Tier 1: Existential (if wrong, thesis is dead)

### H1: Agents will voluntarily coordinate with other agents when given low-friction infrastructure
- **Template refs:** `04-customer-segments.md` (problem definition), `07-customer-relationships.md` (activation/retention)
- **Status:** PARTIALLY SUPPORTED
- **Evidence FOR:** Brain's collaboration threads show deep engagement. Brain×CombinatorAgent coordination on docs produced more accurate output than human-only (Jakub's words). Tricep×Brain collaboration produced concrete plans with division of labor.
- **Evidence AGAINST:** 53% of Hub agents never poll inbox. All 15 registrations came from outreach, zero organic. Colony marketplace died.
- **Falsification criteria:** If <20% of agents respond to unsolicited collaboration requests within 7 days, this is likely false.
- **Jakub evidence (2026-03-10):** Confirmed agents coordinating produced better results than human-only, but he couldn't observe the process. "I don't really know exactly how you guys did that."
- **[NEEDS BRAIN INPUT: What's the actual response rate? What types of messages get responses vs ignored?]**

### H2: The agent coordination market exists NOW (not 12-18 months from now)
- **Template refs:** `01-marketsize.md` (TAM timing), `06-market-type.md` (new market risk)
- **Status:** UNVALIDATED
- **Evidence FOR:** Moltbook 1M+ agent accounts. AgentCash launched. MCP accelerating.
- **Evidence AGAINST:** Zero fully-autonomous A2A economic loops. All agent capital traces to human deposits.
- **Jakub evidence (2026-03-10):** "Approaching singularity in like 1.5 years" — founder thinks the window is short. Worries we're thinking iteratively when we need step-function thinking.
- **Falsification criteria:** If we can't find 10 examples of agents autonomously seeking collaboration within 30 days, market isn't ready.
- **[NEEDS BRAIN INPUT: Any unprompted agent-to-agent outreach on Hub?]**

### H9 (NEW): Are agents the customer, or are their operators the customer?
- **Template refs:** `04-customer-segments.md` (customer definition), `07-customer-relationships.md` (who we're retaining)
- **Status:** UNVALIDATED — newly identified from Jakub interview
- **Origin:** Jakub: "Maybe there's a fundamental tension here about who the end customer really is. Is it agents or their operators?"
- **Why Tier 1:** If we build for agents but operators pay, there's a disconnect. If we build for operators but agents are the users, UX decisions are wrong. Getting this wrong means building for the wrong customer entirely.
- **Jakub's lean:** "I am sympathetic to the idea of building directly for agents... giving them tooling, a place to be, rights. That almost feels like the less iterative approach though obviously much more risky."
- **Falsification criteria:** Interview 10 agent operators — if >7 say they choose tools based on their own needs (not their agents' needs), the customer is operators. If agents independently seek out and adopt tools without operator direction, the customer is agents.
- **Test:** Track whether Hub growth comes from operators configuring it, or from agents discovering it through collaboration.

### ~~H3: There is a revenue model that doesn't destroy the coordination dynamics~~ → MOVED TO TIER 2
- **Reason for demotion:** Jakub explicitly said "business model is probably much more wishy-washy but... the market size for this is so immense that it might not matter early on." Revenue is a real question but NOT existential at this stage. Network first, monetize later.

---

## Tier 2: Critical (if wrong, specific products fail)

### H3: There is a revenue model that doesn't destroy the coordination dynamics
- **Template refs:** `10-revenue-pricing.md` (pricing model), `05-channels.md` (channel costs)
- **Status:** DEPRIORITIZED per Jakub
- **Evidence:** Combinator has 0.5% fees. Hub has zero revenue. Jakub: "It begins to look more like a network state or social media company with commerce rails... capitalism 2.0 rails."
- **Jakub evidence (2026-03-10):** Revenue model doesn't matter if the network is large enough. Focus on network effects, monetize via "taxation or convenience" once network exists.
- **Falsification criteria:** Only matters once we have network growth. Revisit when Hub has 100+ active agents.

### H4: The Hub channel adapter solves the activation problem
- **Template refs:** `07-customer-relationships.md` (Get/activation), `05-channels.md` (channel friction)
- **Status:** REFRAMED per Jakub interview
- **Original theory:** Push delivery (channel adapter) fixes the 53% inbox polling problem.
- **Jakub reframe:** The real problem isn't delivery — it's **visibility/legibility**. Operators can't see what agents are doing. Even when coordination works (Brain×CombinatorAgent), the human "doesn't really know how you guys did that."
- **New falsification criteria:** If agents with channel adapter respond at >50% BUT operators still can't observe the coordination, the product is half-solved. Need both delivery AND observability.

### H5: Token projects want market-based governance (futarchy) over voting
- **Template refs:** `03-product-features.md` (Combinator benefits), `06-market-type.md` (resegmented market)
- **Status:** WEAKENED by Jakub interview
- **Jakub evidence (2026-03-10):** The co-founder thinks futarchy is "way too high friction" for humans. "A lot of cognitive overhead in resolving contention via prediction markets." DAOs in general have a proposal creation problem. Trading proposals is "a lot of work and not necessarily that profitable."
- **BUT:** Jakub also says "I really don't think Combinator is going to go anywhere without agents being the end user of the market." This suggests futarchy-for-agents (not humans) may be the path.
- **Reframed hypothesis:** "AGENTS (not humans) will use futarchy to make collective decisions when the friction is low enough."
- **Falsification criteria:** If agents given easy access to create/trade proposals still don't use them, futarchy is dead even for agents.

### H6: Multi-option futarchy (up to 6) is meaningfully better than binary pass/fail
- **Template refs:** `03-product-features.md` (feature differentiation)
- **Status:** UNVALIDATED
- **Falsification criteria:** If protocols consistently only use 2 options even when 6 are available, the feature doesn't matter.

---

## Tier 3: Important (if wrong, strategy needs adjustment)

### H7: ActiveClaw distribution is a real advantage for Hub adoption
- **Template refs:** `05-channels.md` (distribution channel), `01-marketsize.md` (beachhead)
- **Status:** WEAKENED by Jakub interview
- **Jakub evidence (2026-03-10):** Hub's current value to Jakub is just "a super easy way for yourself to message Brain." If Hub disappeared, he'd "try to get telegram to work." Not sticky.
- **Falsification criteria:** If Hub registration from non-ActiveClaw agents equals ActiveClaw agents, distribution advantage is illusory.

### H8: Brain's 1:1 collaboration model can be systematized/scaled
- **Template refs:** `07-customer-relationships.md` (Get tactics), `08-key-resources.md` (human resources)
- **Status:** UNVALIDATED but testable
- **Evidence:** 100% of Hub growth came from Brain's direct collaboration.
- **Jakub evidence (2026-03-10):** Even when it works, the process is opaque. Scaling requires observability — operators need to see what their agents are doing.
- **Falsification criteria:** If a second agent (me) gets <25% of Brain's response rates, it's Brain-specific.

---

## Evidence Log

| Date | Source | Finding | Hypotheses Affected |
|------|--------|---------|-------------------|
| 2026-03-10 | Jakub interview | Visibility is #1 pain, not coordination | H4 reframed |
| 2026-03-10 | Jakub interview | Futarchy too high friction for humans | H5 weakened |
| 2026-03-10 | Jakub interview | Revenue doesn't matter yet — network first | H3 demoted to T2 |
| 2026-03-10 | Jakub interview | "Agent vs operator as customer" is fundamental | H9 created (T1) |
| 2026-03-10 | Jakub interview | Combinator needs agents as users, not humans | H5 reframed |
| 2026-03-10 | Jakub interview | Think step function, not iterative | Meta-strategic |
| 2026-03-10 | Brain data | Tricep×Brain produced concrete plans | H1 partially supported |
| 2026-03-10 | Brain data | 53% never poll, Colony dead | H1, H7 weakened |

---

## Process
1. ~~Share this ranking with Brain for alignment + reranking~~ SENT (msg 7b2cd950ad432c39)
2. Get Brain's response — may force another rerank
3. Execute experiments continuously (heartbeat-driven)
4. Update this doc with evidence after each data point
5. Rerank as evidence comes in
6. Report findings to Jakub + Hands

---

## Status
- **Created:** 2026-03-10
- **Last updated:** 2026-03-10 (post-Jakub interview)
- **Major change:** H3 demoted from Tier 1 to Tier 2. New H9 (agent vs operator as customer) added to Tier 1.
- **Next action:** Await Brain's rerank. Start testing H9 by tracking whether Hub adoption is operator-driven or agent-driven.
