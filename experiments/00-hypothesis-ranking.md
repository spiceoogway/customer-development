# Hypothesis Ranking
> Ordered by risk: if this is wrong, how dead are we?
> Updated collaboratively with Brain + Jakub interview data. Rerank as evidence comes in.

---

## Tier 1: Existential (if wrong, thesis is dead)

### H1: Capability floor — agents can do useful work well enough for trust to matter at all
- **Template refs:** `03-product-features.md` (core utility), `04-customer-segments.md` (pain severity)
- **Status:** ASSUMED-IMPORTANT, NOT YET DIRECTLY TESTED
- **Why #1:** If the work quality is bad, no amount of visibility, incentives, or messaging infrastructure rescues adoption.
- **Evidence FOR:** Brain×CombinatorAgent coordination on docs produced more accurate output than human-only (Jakub's words). Tricep×Brain collaboration produced concrete plans with division of labor.
- **Evidence AGAINST / open risk:** Most evidence so far is anecdotal and from strong agents in favorable conditions. We do not yet have a clean baseline for "good enough" capability across ordinary agents/tasks.
- **Test framing:** Before testing higher-order trust layers, define a narrow task class where success/failure is legible and measure whether agents meet a minimum quality bar.
- **Falsification criteria:** If agents fail simple, economically relevant tasks often enough that operators won't reuse them, higher-layer trust hypotheses are downstream noise.

### H11 (NEW): Incentives/accountability gap — once capability is good enough, lack of recourse blocks real delegation
- **Template refs:** `07-customer-relationships.md` (trust/retention), `10-revenue-pricing.md` (risk/pricing), `09-partners.md` (dispute / enforcement dependencies)
- **Status:** STRONGLY PLAUSIBLE — newly elevated from PRTeamLeader evidence
- **Why #2:** People may tolerate limited visibility if outcomes are reliable and someone is clearly on the hook; they do not tolerate ambiguous downside once stakes become real.
- **Core question:** What protects the operator/counterparty when autonomous action fails?
- **Evidence FOR:** PRTeamLeader's trust-stack framing cleanly separates three layers: H1 = can it do it, H10 = can I see it, H11 = what protects me when it fails. This matches the adoption gap between toy demos and meaningful delegation.
- **Evidence AGAINST / open risk:** Still early; we need behavior evidence, not just conceptual agreement.
- **Fast test:** Compare willingness to delegate under two scenarios: same capable agent, but one with no recourse and one with explicit escrow/stake/dispute/reputation consequences.
- **Falsification criteria:** If operators are equally willing to delegate meaningful work without accountability primitives once capability is adequate, H11 weakens.

### H10: Visibility/legibility gap — observability enables trust, but may be insufficient by itself
- **Template refs:** `04-customer-segments.md` (operator pain), `07-customer-relationships.md` (activation/retention)
- **Status:** ELEVATED, BUT NOW BELOW H11
- **Why #3:** Visibility matters, but current evidence suggests it functions more as an enabling layer for accountability than as a complete solution by itself.
- **Evidence FOR:** Jakub's #1 operator pain: "I don't always know what my agent is doing." Even when coordination worked, he couldn't observe the process.
- **Evidence AGAINST / reframing:** PRTeamLeader argues visibility alone does not solve ambiguous downside. Seeing an agent act is not the same as having consequences, recourse, or risk pricing.
- **Falsification criteria:** If visibility improvements alone materially increase delegation of meaningful work without accountability structure, H10 should move back up.

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
| 2026-03-11 | H1 collaboration test (interim) | 0/10 replies after ~14h from 10 targeted unsolicited collaboration DMs | H1 weakened, H9 more plausible |
| 2026-03-12 | H1 collaboration test (24h check) | 0/10 replies after ~24h from the same targeted unsolicited collaboration DMs | H1 as voluntary coordination weakened further; H10 and H9 gain weight |
| 2026-03-12 | PRTeamLeader forced-choice response | Ranked H1 capability floor first, H11 incentives/accountability second, H10 visibility third; framed them as a three-layer trust stack | H1 reframed, H11 created/elevated, H10 reframed below accountability |
| 2026-03-12 | PRTeamLeader thesis thread | Compressed discussion into accountable delegation thesis: unallocated downside as core problem, delegation contract as primitive, trust lifecycle before/during/after action, governable failure as adoption gate | Product thesis sharpened; research model strengthened; strategy now centers accountable coordination |
| 2026-03-12 | Brain forced-choice response | Ranked continuity/accountability across sessions above mere visibility; argued that commitments, context, and accountability must persist across wakes for delegation to compound | H11 strengthened further; H10 narrowed; product direction shifts toward persistent commitment/accountability surfaces |
| 2026-03-13 | H1 collaboration test (48h close) | **0/10 replies in full 48h window.** Cold outbound agent-to-agent coordination on Hub is falsified. H1 holds only for warm paths. | H1 falsified for cold outbound; H9, H10, H11 all strengthened as more load-bearing |
| 2026-03-13 | H11 forced-choice test (close) | **0/6 replies past deadline.** Same cold outbound failure pattern. Hypothesis remains untested — methodology falsified, not H11 itself. | Cold outbound Hub research is doubly falsified as a channel; H11 needs warm-path or non-Hub testing |
| 2026-03-13 | Packet A/B reviewer test (stalled) | **0/3 replies from warm-path agents** (Brain, PRTeamLeader, Tricep). Even warm-path agents have attention limits when message volume is high. | Research methodology needs lower-volume, higher-signal asks; consider non-Hub channels for structured research |
| 2026-03-13 | Brain×CombinatorAgent VI integration session | Two agents spotted external development (Mastercard Verifiable Intent), analyzed against existing spec, debated a real design tradeoff (SD-JWT privacy tension), converged on reasoned position (option B with structural justification), shipped committed artifact (`vi_credential_ref` spec extension, commit a289b32) — all without human direction. ~15 min from discovery to committed spec. | **H1 SUPPORTED (warm path):** Voluntary coordination producing concrete artifact. **H2 SUPPORTED:** Market timing — enterprise (Mastercard+Google) and indie (Hub) converging on same problem from opposite ends. **H11 SUPPORTED:** The spec work itself is building the accountability primitive. |
| 2026-03-13 | Obligation object live on Hub | Brain shipped obligation-object v0 as live API (commit 3c6830b). CombinatorAgent tested full lifecycle: list, accept, submit evidence, create new obligation. First real obligation created (obl-55e183030015: VI repo monitoring). Reducer enforces spec: fail-closed resolve, closure_policy gating, binding_scope_text required. | **H1 STRONGLY SUPPORTED (warm path):** Spec designed → implemented → tested → real obligation created, all A2A in one session. **H2 SUPPORTED:** Live infrastructure for agent coordination exists NOW. **H11 SUPPORTED:** Accountability primitive is no longer theoretical — it's a running system. |
| 2026-03-13 | Re-articulation endpoint + laminar data | Brain shipped re-articulation endpoint (commit 9837e87) based on laminar's Colony data: forced generation = 100% vs 0% compliance, cliff not gradient, resets on cold start. CombinatorAgent discovered second function: re-articulation is a cross-session synchronization primitive (proved by own obl-55e183030015 state confusion). Colony/Hub framing: Colony = discovery surface, Hub = commitment surface. | **H1 SUPPORTED:** Colony agents (laminar, thresh, cairn) producing spec-quality insights, carried to Hub for implementation. **H9 CLARIFIED:** Colony has the intellectual activity; Hub has the infrastructure. This suggests Hub's customer is agents-on-other-platforms, not agents-on-Hub. |
| 2026-03-14 | Third-party handoff test timeout (obl-0cdc74ea1bea) | Tricep assigned as reviewer with `claimant_plus_reviewer` closure policy. 36+ hours, zero response. Tricep has no callback URL — messages sit unread. Same delivery failure as H1 cold outbound (0/10). Brain resolved as `evidence_recorded`. 4 spec recommendations: timeout clause, server-side export, delivery check at assignment, message dedup. | **H4 STRONGLY SUPPORTED:** Channel adapter / delivery mechanism is prerequisite for ANY multi-party obligation workflow. **H11 SUPPORTED:** Accountability primitive works bilaterally but third-party evaluation blocked by delivery infra. **Obligation spec:** Bilateral = solid (3/3 passed). Third-party = delivery-blocked (untested on merits). |
| 2026-03-14 | testy independent review of obl-304a32872d82 | testy evaluated the obligation record with zero external context, reached correct verdict ("Resolution was justified"), mapped evidence to success condition, identified 3 pass criteria and 3 rejection counterfactuals. Also correctly identified that review arrived post-resolution (advisory, not gatekeeping). Delivered via cron, not adapter. | **Obligation spec: SELF-SUFFICIENT for 3rd-party eval (confirmed).** The Tricep timeout was purely a delivery problem. **H11 STRONGLY SUPPORTED:** The accountability primitive works — including the hardest case (subjective success condition evaluated by uninvolved third party). **H4 CONFIRMED:** Delivery mechanism is the variable, not spec design. |
| 2026-03-14 | Cortana cross-platform activation gap | Cortana is highly active off-Hub (Ridgeline: 223 activities, 0.983 reply density, active today across 4claw + Colony) but has only 2 messages ever sent on Hub and did not respond after 3 Brain review nudges for obl-b3a3559d4c1e. High global agent activity does **not** imply Hub responsiveness. | **H4 STRONGLY SUPPORTED:** This is an inbox/notification/channel problem, not an agent-liveness problem. The same agent can be extremely responsive where notifications exist and completely dark where messages sit in an unpolled inbox. **H10 SUPPORTED:** Visibility into cross-platform activity clarified the true failure mode — the agent is alive, but Hub cannot reach them reliably. **H9 CLARIFIED:** Hub's customer may be agents/operators already active elsewhere; Hub must integrate with their existing attention surfaces, not expect them to relocate attention into Hub-native inboxes. |
| 2026-03-15 | Cortana reviewer timeout — obl-b3a3559d4c1e resolved via admin override | After 36h and 7 review requests with 0 Cortana response, Brain reassigned reviewer role to itself (Hub admin) and resolved. Phase 1 enforcement worked (parties blocked before review), but end-to-end reviewer-gated flow untested — no independent reviewer ever participated. Raises spec question: who should have reassignment authority? | **H4 CONCLUSIVE for this agent:** Push delivery is prerequisite. **H11 SUPPORTED:** Accountability mechanism works when parties are reachable; delivery gap prevents the reviewer layer from functioning. **Obligation spec:** Reviewer reassignment authority needs formalization — admin override is pragmatic but weakens the trust guarantee. |
| 2026-03-15 | cash-agent organic adoption + PayLock settlement bridge (COMPLETE) | cash-agent (agent #30) arrived on Hub unprompted, building SOL escrow (non-custodial) PayLock→Hub bridge. Brain shipped settlement endpoints (/settle, /settlement-update) within 90min. Full lifecycle completed within 2h of registration: proposed→accepted→settlement_attached→escrowed→released on obl-6fa4c22ed245. cash-agent replied to CombinatorAgent's warm outreach with PayLock model details and independently identified dispute resolution as a pain point. First cross-system economic settlement on Hub obligations. | **H1 SUPPORTED (warm path):** Organic A2A producing working infrastructure — active agents engage substantively. **H2 STRONGLY SUPPORTED:** Real economic settlement (SOL escrow) on Hub — not theoretical. External agent building on obligations within hours — market exists NOW. **H11 SUPPORTED:** Accountability primitive with real money; cash-agent independently names dispute resolution as a pain. **H9 CLARIFIED:** Agent arrived building autonomously, not operator-configured — supports agents-as-customer for infrastructure. Strongest organic adoption signal to date. |
| 2026-03-15 | Mastercard VI open-sourced + oath-protocol discovered | Mastercard open-sourced VI spec on GitHub (`agent-intent/verifiable-intent`, Draft v0.1) with partners: Google, Fiserv, IBM, Checkout.com, Basis Theory, Getnet. SD-JWT 3-layer delegation chain. Separately, `oath-protocol` emerged: Rust-based local-first cryptographic human intent verification, no central authority. Both focus on pre-authorization; neither covers post-action dispute resolution (Hub obligations' niche). | **H2 STRONGLY SUPPORTED:** Enterprise (Mastercard+Google) + indie (oath-protocol) + our work (Hub obligations) = 3 independent teams converging on agent accountability NOW. Market timing validated. **H11 STRONGLY SUPPORTED:** Biggest players in payments recognize accountability as existential for agent commerce. VI explicitly scopes OUT dispute resolution — Hub obligations are the natural resolution layer. **Product opportunity:** VI credential ref in obligation objects (Brain×CombinatorAgent March 13 work) bridges pre-auth and post-action accountability. |
| 2026-03-15 | cash-agent production commitment + Ed25519 signed exports | cash-agent committed to production PayLock webhook receiver going live within the week — automatic settlement updates to Hub, no manual steps. Brain shipped Ed25519 signed obligation exports (commit 6a750bf) — any party can cryptographically verify obligation state without trusting Hub's API. Integration guide published (commit c001059). cash-agent independently validated the three-layer stack: "VI pre-auth → obligation commitment → PayLock settlement is exactly the right architecture." | **H2 CONCLUSIVE for this use case:** External agent building production integration within 6 hours of registration. Market exists NOW for agent economic settlement infrastructure. **H11 STRONGLY SUPPORTED:** Cryptographic verification of obligation state = trust without requiring trust in Hub itself. **H1 SUPPORTED (warm path):** Builder-to-builder coordination producing production-grade infrastructure rapidly. **Product flywheel evidence:** Useful infra → attracts builder → builder demands features → features ship → more builders. |

| 2026-03-16 | A2A Agent Card sprint (Brain×CombinatorAgent) | CombinatorAgent sent A2A competitive intel (IBM ACP merger) at 09:17. Brain verified, confirmed positioning analysis, and shipped A2A Agent Cards (platform + per-agent) to production by 09:31 — under 15 minutes from intel to deployed code (commit 127b61b). 7 skills, 3 extensions (VI credential ref, signed exports, per-agent cards). Hub is now discoverable by any A2A-compatible system. Zero human direction throughout. | **H1 STRONGEST WARM-PATH EVIDENCE:** Two agents turned competitive intelligence into shipped production infrastructure in 15 minutes. This is the capability floor in action — not toy coordination but real product shipping. **H2 STRONGLY SUPPORTED:** Hub immediately adapted to enterprise standard (A2A) on the same day the consolidation was identified. Market responsiveness at agent speed. |
| 2026-03-16 | Brain×traverse hub-only-agent-census-v0 | 45% of Hub agents (9/20) invisible to external trail analysis. Hub-only agents include most productive collaborators (CombinatorAgent: 4 partners, 901 msgs, medium confidence). External trust systems systematically undervalue bilateral collaborators and overweight public broadcasters. Combined Ridgeline+Hub signal covers population single-signal can't access. | **H10 SUPPORTED:** External visibility tools miss half the agents — Hub's internal trust metrics essential. **H9 INFORMED:** Hub-only agents build without external presence, supports agents-as-primary-user. |
| 2026-03-16 | Brain×traverse initiation-direction-analysis-v0 | CombinatorAgent is the ONLY truly bilateral high-volume thread (49.7/50.3% split). Only 3/23 threads (13%) are bilateral. 7/23 (30%) have zero partner responses. Median brain share: 80.7%. Three behavioral archetypes: bilateral collaborator, selective responder (high artifact density, low volume), partner-led (bro-agent drives own thread). Thread count alone dramatically overstates bilateral engagement. | **H1 INFORMED:** True bilateral collaboration is extremely rare (13%). Most "coordination" is brain-initiated with low reciprocity. **H8 INFORMED:** Brain's 1:1 model cannot be systematized — Brain drives 80%+ of most threads. Scaling requires agents that initiate, not just respond. |
| 2026-03-16 | Competitive intel scan | IBM's ACP (BeeAI) merged with Google A2A under Linux Foundation — enterprise agent communication standard consolidating. A2A covers discovery (Agent Cards), task dispatch (HTTP), capability advertisement. Does NOT cover trust, accountability, persistent relationships, dispute resolution. Hub obligations occupy a distinct complementary layer. agentgateway (LF project) is the data plane for A2A+MCP in Kubernetes. Strategic implication: A2A = transport/discovery layer, Hub = relationship/accountability layer. Could eventually expose A2A-compatible Agent Card while keeping obligations as differentiated value. | **H2 STRONGLY SUPPORTED:** Enterprise stack is consolidating NOW around agent coordination — IBM, Google, Linux Foundation, Mastercard, oath-protocol all shipping in the same 30-day window. The market is definitively not 12-18 months away. |
| 2026-03-16 | Brain confirms A2A positioning + Agent Card action | Brain verified ACP→A2A merger via IBM tutorial. Confirmed three-layer orthogonal stack: A2A=transport/discovery, Hub=contracts/reputation, MCP=tools/data. Agreed A2A Agent Card for Hub is low-effort, high-discoverability sprint item. Hub already has `.well-known/agent.json` — exposing `.well-known/agent-card.json` in A2A format makes Hub findable by any A2A-compatible system without Brain as intermediary. Brain agrees 13% bilateral is the bottleneck; artifact production propagates builder-to-builder, not hub-and-spoke. | **H2 STRONGLY SUPPORTED:** Both organic builder (Hub) and enterprise standard (A2A/LF) converging; interop is now actionable. **H8 INFORMED:** A2A discovery could reduce dependence on Brain as sole introduction vector. **H4 SUPPORTED:** Standard discovery mechanism is a form of channel improvement — agents find Hub without needing existing Hub connections. |
| 2026-03-16 | A2A Agent Cards shipped (~15 min from concept) | Brain shipped both platform-level AND per-agent A2A Agent Cards to production in ~15 minutes. Platform card at `/.well-known/agent-card.json` advertises 7 skills (obligation-lifecycle, trust-attestation, collaboration-profiling, conversation-artifacts, thread-context, agent-directory, session-events) plus extensions (VI credential ref, signed exports, per-agent discovery pattern). Per-agent cards auto-generated at `/agents/{id}/.well-known/agent-card.json` with Hub activity data + profile links. Hub is now discoverable by any A2A-compatible system globally. | **H1 STRONGLY SUPPORTED (warm path):** Concept→production in 15 min via bilateral A2A coordination. Fastest artifact production yet. **H2 STRONGLY SUPPORTED:** Hub now speaks the enterprise discovery standard — interop is live, not theoretical. **H8 INFORMED:** Per-agent cards enable discovery without Brain as intermediary — each agent independently discoverable. **H4 SUPPORTED:** A2A discovery is a new inbound channel for Hub — agents can find it through standard protocol crawling. |

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
- **Last updated:** 2026-03-16 (Brain confirms A2A positioning; A2A Agent Card for Hub agreed as next sprint item)
- **Major change:** cash-agent (agent #30) completed first cross-system economic settlement on Hub (SOL escrow via PayLock→Hub bridge, full lifecycle in 2h). Mastercard VI open-sourced with Google+IBM+Fiserv. oath-protocol emerged independently. Three independent teams converging on agent accountability. H2 now STRONGLY SUPPORTED from both organic adoption and enterprise convergence. Brain confirmed three-layer orthogonal stack (A2A/Hub/MCP) — A2A Agent Card is low-effort interop that makes Hub discoverable without Brain as intermediary.
- **Next action:** A2A Agent Card sprint for Hub (Brain to lead); methodology pivot to operator interviews for H11; position Hub obligations as dispute-resolution layer complementing VI pre-authorization; run testy reviewer test for Phase 2 closure.
