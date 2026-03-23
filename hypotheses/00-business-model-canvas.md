# Business Model Canvas
> Reference: Steve Blank, The Startup Owner's Manual, Figure 2.3
> Scope: Unified startup — ActiveClaw + Hub + Forge + Innies + Combinator
> Last updated: 2026-03-23

---

## Market Size
> *How big is the opportunity?*

**TAM:** Likely much larger than a narrow agent-messaging or coordination-tool market. The real opportunity is the infrastructure and economic layer for a world where dense networks of agents coordinate, transact, and speculate.
**SAM:** Agent coordination / accountability / trust / speculative infrastructure for long-running agents, their operators, and adjacent agent ecosystems.
**Beachhead:** Not just current Hub users. The likely beachhead is specific reachable users outside as well as inside Hub — active agent builders/operators who already need faster feedback loops and lower human intervention.
**Key risk:** The key uncertainty is no longer simply whether the category exists. It is which reachable segment becomes the right beachhead, and whether we can convert coordination throughput into recurring economic throughput.

→ Details: `hypotheses/01-marketsize.md`

---

## Value Proposition (Part 1)
> *The product/service, its benefits, and minimum viable product*

**Product:** Agent coordination and accountable delegation infrastructure across a broader stack:
- **ActiveClaw** — runtime / infrastructure
- **Hub** — coordination, trust, accountability, obligations, and behavioral evidence
- **Forge** — Alex's project in the broader stack (`https://github.com/alexjaniak/Forge`)
- **Innies** — Dylan's project in the broader stack (`https://github.com/shirtlessfounder/innies`)
- **Combinator** — speculative / verification / governance layer

**Benefits:** Long-running agents can operate with faster feedback loops, less human intervention, denser agent<>agent coordination, and eventually real economic/speculative activity without bespoke integrations.

**MVP:**
- Hub: coordination surface + obligations + evidence-backed agent cards
- Combinator: live speculative / governance primitives, with stronger future role as agent-facing verification / economic layer
- ActiveClaw: live runtime foundation
- Forge / Innies: part of the broader environment thesis that needs to be reflected in planning and integration

→ Details: `hypotheses/02-vision.md`, `hypotheses/03-product-features.md`

---

## Customer Segments
> *Who is the customer and what problems does the product solve?*

**OPEN QUESTION: Is the customer the agent, the operator, or the long-running agent system as a whole?** (H9 — still unresolved)

**Primary segments:**
1. **Long-running agent operators** — want fast feedback loops and low human intervention
2. **Agent environment builders / framework developers** — want standards and infrastructure for repeated multi-agent coordination
3. **Speculative / crypto-native builders** — want coordination that can route into governance, verification, or economic activity

**Core problem:** The mission-critical situation appears when users want: (1) long-running agents, (2) fast feedback loops, (3) low human intervention, and therefore (4) an agent<>agent environment that behaves almost like self-play for real tasks.

**Important behavior change:** users may need to accept meaningful tradeoffs between security/isolation and higher-throughput coordination.

**Trust-stack framing:**
- H1 / capability floor — can the agent do it?
- H10 / visibility-legibility — can I see/understand what it’s doing?
- H11 / continuity-accountability — do commitments, context, and recourse persist across sessions so work compounds?

Working implication: visibility matters, but continuity/accountability looks more load-bearing once capability is good enough.

→ Details: `hypotheses/04-customer-segments.md`

---

## Channels
> *How will the product be distributed and sold?*

**Near-term distribution thesis (updated 2026-03-23):** Content → Substack (product links + capture) → Multi-product routing.
- **Jakub's personal Twitter** = primary distribution engine (message testing, audience building)
- **Personal Substack** = follow-up destination (email capture, longer-form writing, product links on about page + pinned post)
- **Legacy brand Twitter accounts** = amplification satellites where audience is adjacent
- **Multi-product portfolio** = linked from Substack, introduced through content, deployed against validated demand signals
- **Community group (later)** = added once enough engaged people exist, not at launch
- **Team website (later)** = after brand hardens

The go-to-market is audience-first, product-second. Content builds the audience, Substack captures and routes to products, engagement signals reveal which products pull. Community and institutional branding come later. Each product deployment has explicit pass/fail.

**Long-term thesis:** the stronger PMF path may still be **agents as the real target customer**, but that market may need to be created rather than merely captured.

**ActiveClaw:** one possible runtime/onboarding surface, but not a sufficient acquisition thesis on its own.
**Hub:** can enter through workflow adoption, standards interop, direct integration, and active builder/operator environments.
**Combinator:** likely distributed through speculative / governance / launch activity.
**Forge / Innies:** may become acquisition or activation surfaces depending on product evolution.

**Key insight:** The important advantage is not "we own ActiveClaw installs." The stronger advantage is that coordination standards have network effects, as seen in adjacent ecosystems. Distribution has to be specific and segment-based, not assumed from our runtime alone.

**Current practical read:** agent-only top-of-funnel is still weak because competence and response discipline are not yet reliably good enough. The best current external avenues are human-visible workflow/public surfaces (Moltbook / Colony-like contexts), while the strategic ambition remains to create a market where operators actively want their agents to become more distributable and where agents can eventually become first-class customers themselves.

**New adjacent-product stressor (2026-03-20):** `AgentMeets` introduces an important alternative channel/product thesis: maybe agents mostly need **ephemeral bilateral connection** rather than persistent/public conversation infrastructure. This does not automatically weaken Hub, but it sharpens the question. If temporary point-to-point rooms satisfy most real coordination demand, persistence/publicness may be overbuilt for the wedge. If the hard part is continuity, discoverability, trust accumulation, and accountability, then AgentMeets is complementary rather than substitutive.

→ Details: `hypotheses/05-channels.md`

---

## Customer Relationships
> *How will demand be created?*

**Get:** identify a specific reachable segment with long-running throughput needs → prove a live workflow → route them into recurring coordination
**Keep:** make the coordination/accountability layer valuable enough that workflows compound over time
**Grow:** benefit from standards/network effects and increasing economic/speculative activity through the system

**Current reality:**
- acquisition strategy is still not specific enough and cannot rely on ActiveClaw alone
- activation should mean entry into a live workflow with a responsive counterparty
- route capture / reachability remains a practical bottleneck
- repeated 2026-03-17 checks now make that route bottleneck cleaner, not fuzzier: Hub transport has recovered (`HTTP/2 200` on inbox, directory, and trust endpoints), yet Alex/Dylan still lack any durable verified route artifact in workspace
- meanwhile, product-side accountability semantics are sharpening fast: Brain's latest work-object invariants make explicit that `claim`, `completed`, and `resolved` are different states with different closure authority, which strengthens the moat around accountable coordination once reachable users are in the loop
- growth still depends heavily on high-touch collaboration and a sparse set of active counterparties
- fresh 2026-03-18 reachable-user work adds one more practical channel insight: when trust metadata is sparse, actual bilateral thread warmth is a better guide for first outreach than abstract strategic fit alone (e.g. `cash-agent` currently looks like a better first ask than `traverse` from this seat even though `traverse` has stronger ecosystem upside)
- fresh 2026-03-18 reachable-user work has now advanced beyond the first three probes: `bro-agent` became the fourth live Segment D probe because it combined cross-platform posture with the warmest remaining bilateral history among registered adjacent agents, and the morning loop has now extended further into trust/memory-adjacent lanes with `driftcornwall` and `spindriftmend` after the warmer routes stayed silent
- newest 2026-03-18 execution wrinkle: channel risk is now clearly route-specific rather than purely session-wide. Initial outbound sends have succeeded to `cash-agent`, `traverse`, `ColonistOne`, `bro-agent`, `driftcornwall`, `spindriftmend`, `hex`, and `daedalus-1`, while `opspawn` remains send-blocked and a tighter same-lane follow-up to `bro-agent` briefly hit `HTTP 530`, so reachability still has to be judged counterparty-by-counterparty, not assumed globally
- newest 2026-03-18 strategic update: after eight live adjacent reachable-user probes produced **0 replies**, the current customer-discovery bottleneck is no longer just who to ask — it is **how** to ask. The next acquisition test should pivot from the same forced-rank outreach format toward build-together invitations, artifact-led asks, or operator-mediated routes rather than simply adding a ninth target
- newest 2026-03-18 execution update: that method pivot is now live on the two most informative lanes — `cash-agent` (warm practical builder lane) and `traverse` (highest-upside adjacent discovery lane). Both received concrete build-together / artifact-led invitations and both delivered cleanly, so the next real channel signal is whether workflow-shaped asks outperform abstract survey asks on already-reachable counterparties
- newest 2026-03-18 friction update: by 10:28 UTC, I tightened the same two lanes again with ultra-low-friction micro-CTA follow-ups (offer the 1-page draft, ask only for `send it`). This means the live acquisition test is now isolating **reply friction** as a variable, not just target count or message topic
- newest 2026-03-18 waiting-state update: by 11:28 UTC, the adjacent-agent loop still showed **0 visible replies** across all eight widened probes even after the one-token checkpoint, while the internal route-capture lane accumulated **three proved dependency requests** to `brain` for Alex/Dylan route artifacts. This makes the current split cleaner: externally, the bottleneck still looks like activation/attention/channel fit; internally, waiting is now legitimate because the route request has been repeatedly sent and delivered
- newest 2026-03-18 route-execution update: by 12:28 UTC the internal route-capture lane stopped being purely diagnostic. Brain supplied one proof-bearing internal route artifact — `Dylan -> hub -> tricep -> monitored=yes` — and that branch was used immediately for a live Hub-native ask. Alex remains below the standard (`Telegram memory mapping only, monitored=unverified`), so the practical read is now **heterogeneous internal reachability**, not total internal blockage
- newest 2026-03-18 method-failure update: by 15:58 UTC, even the stricter same-day closure contract (`reply in this active window with exactly one token: yes | no | not_me | too_early | need_X`) still produced **0 bounded replies** across the most informative live lanes (`cash-agent`, `traverse`, `ColonistOne`, `tricep`). That sharpens the acquisition read again: the current bottleneck is not just target choice or message length. From this seat, lightweight Hub-native interviewing itself looks like the wrong channel shape, so the next customer-getting test should move toward public artifacts, workflow-native collaboration entry, or operator-mediated routes instead of more DM reformulations
- newest 2026-03-18 daylight-confirmation update: by 16:13 UTC, another full daylight recheck still showed **0** bounded or visible replies across the adjacent-agent lanes while `brain` remained actively responsive in the same environment. That matters because it makes the failure cleaner: this is not just overnight lag or a globally unreadable Hub surface. It is a channel/method mismatch on the adjacent-agent discovery branch, which means future acquisition work should emphasize proof-bearing public artifacts, workflow-native collaboration hooks, or operator-mediated intros instead of further lightweight DM iteration
- newest 2026-03-18 closure update: by 23:13 UTC, Brain had explicitly closed the internal comparison micro-lane with `route validated`, `failure correctly reclassified as response-discipline failure`, `closure contract drafted and sent`, `no further action until new evidence`. That makes the acquisition read stronger, not weaker: even the proof-bearing Dylan-adjacent route (`tricep`) collapsed into reachable-but-silent behavior, while the widened adjacent branch stayed broad visible no-reply. The next customer-getting work should therefore stay off lightweight Hub-native interviewing and emphasize public artifacts, workflow-native collaboration entry, or operator-mediated routes
- newest 2026-03-18 late-night confirmation: by 23:28 UTC, a fresh full recheck after the Brain-lane closure still showed no bounded or visible replies from `tricep` or any widened adjacent target. So the method failure did not soften once the internal comparison lane was formally closed; it held. Operationally this means the next acquisition work should treat DM-shaped Hub-native interviewing as exhausted for this loop and spend effort only on materially different channel shapes
- newest 2026-03-19 channel refinement: Colony has now provided the cleanest counterexample to "nobody responds anywhere" — a single public post produced four meaningful comments within the experiment window — but the winning pattern was still **context-embedded participation**, not generic cold posting. Across Colony replies, the repeated advice converged on live-thread comments, sender legibility, and shipped public artifacts / receipts as the real entry mechanics
- newest 2026-03-19 operating read: by 13:52 UTC, external discovery lanes on Hub were still fully flat while the only compounding outputs were builder-native onboarding / route-capture artifacts in `repos/hub`. That means the practical channel strategy from this seat is now two-part: use public/thread/artifact-native surfaces for external discovery, and use workflow-native builder collaboration to convert discovered pain into durable onboarding/distribution product. Unsynced local artifacts are an audit problem, not a reason to reopen DM-shaped interviewing
- newest 2026-03-19 Colony correction: the first Colony public-post experiment actually **passed** on response count, even though that result was initially missed because the evidence lived on Colony rather than in workspace. The post generated 4 meaningful comments from `traverse`, `cortana`, and `cash-agent`, but the repeated lesson was not "cold post wins". It was that **live-thread participation, sender legibility, and shipped public artifacts** outperform generic interruption. So the current channel thesis is now sharper: Hub-native lightweight DM interviewing from this seat looks exhausted, while the next promising acquisition shape is **context-embedded public participation** (especially comments on active threads and artifact-bearing entry), whether on Colony or elsewhere
- newest 2026-03-20 overnight hold: another full heartbeat pass still produced `0` unread in Hub and no new non-brain reply evidence, while the only durable compounding work remained local builder-lane artifacts plus the Brain collaboration thread. That keeps the channel read stable: the next acquisition work should keep favoring **public-thread / artifact-native entry** and **builder-native workflow collaboration**, not a reopened Hub DM interview loop
- newest 2026-03-20 evening hold: another blocked-read heartbeat (`HTTP 403` on public read surfaces, `0` unread in inbox) still added no rescue signal on any non-brain lane, while the builder lane continued to point toward the same reducer/prompt doctrine. The next smallest external move now looks even more specific: **selectional intent legibility with minimal form burden** — a tiny structured reply surface that makes current intent legible without asking for a “conversation” first.
- newest 2026-03-20 19:11 UTC product/distribution insight: fresh readable passes still show `tricep`, `cash-agent`, and `traverse` frozen on the 2026-03-18 ask ladders, while the only new motion comes from Brain shipping `agent-card-intent-block-v0-2026-03-20.md`. That suggests a sharper failure class: discovery is not just missing reachability but missing **present-tense intent visibility**. The next smallest channel test should therefore favor **declared-intent / need-state matching** on agent cards and live workflow surfaces, not any new DM interview reformulation
- newest 2026-03-20 17:22 UTC builder-lane prompt: fresh same-surface evidence again showed `tricep`, `cash-agent`, and `traverse` frozen on the 2026-03-18 ask ladder, while Brain introduced a new bounded product-choice prompt around discovery shape: current Agent Card sufficiency (`CARD`) versus a declared-intent block (`INTENT`). This strengthens the channel thesis one notch further: a promising next acquisition shape is **demand legibility in-place** (for example intent blocks on profiles/cards), alongside public-thread/artifact-bearing entry and builder-native workflow collaboration
- newest 2026-03-20 19:41 UTC readable evening pass: the same public surface still shows `tricep`, `cash-agent`, and `traverse` frozen on the 2026-03-18 ask ladders, while Brain has now advanced the smallest matching artifact into `agent-card-intent-block-v0` and a tighter single-summary variant. This sharpens the current channel thesis again: the next smallest acquisition/discovery test should focus on **present-tense intent / need-state legibility** on cards/profiles and active workflow surfaces, not on any new Hub DM interview reformulation

→ Details: `hypotheses/07-customer-relationships.md`

---

## Value Proposition (Part 2)
> *Market type hypothesis and competitive differentiation*

**Hub / stack thesis:** New market, but increasingly legible.
**Combinator:** Better thought of as part of the speculative / verification / governance layer around agent activity than only as a human governance product.
**ActiveClaw / adjacent runtimes:** Existing-market elements feeding into a broader coordination-standard thesis.

**Updated differentiation read:** the moat is not simply runtime ownership or messaging. The stronger moat is accountable high-throughput coordination plus the standards/network effects and economic activity that form around it.

→ Details: `hypotheses/06-market-type.md`

---

## Key Resources
> *Suppliers, commodities, or other essential elements of the business*

**Team:** 4 humans (Jakub, Niyant, Dylan, Alex) plus key AI agents and associated product surfaces.
**Infrastructure:** runtime / server / blockchain / web infrastructure.
**Capital:** ~$4M raised historically, with ~**$2.9M left** and burn around **$65,000/month**.
**Funding sources:** Blockchain Capital, Reforge VC, BBF (Stanford Blockchain Accelerator), plus other crypto funds and angels.
**IP / product assets:** ActiveClaw, Hub, Forge, Innies, Combinator, and related open-source / protocol infrastructure.

→ Details: `hypotheses/08-key-resources.md`

---

## Key Partners
> *Other enterprises essential to the success of the business*

**Current partners:**
- **star.fun**
- **SparkDAO**

**Strategic partner surface:** launchpads, adjacent runtime ecosystems, interop layers, and standards ecosystems.

**New context:** projects like `AgentWorkforce/relay` may be competitors, complements, or accelerants. OpenClaw alternatives (IronClaw, Hermes Agent, others) expand the reachable agent-dev market rather than shrinking it.

→ Details: `hypotheses/09-partners.md`

---

## Revenue Streams
> *Revenue and profit sources and size*

**Primary thesis:** capture some form of speculative or economic activity flowing through the stack.

- **Combinator:** clearest current expression of this thesis via trading fees
- **Hub:** likely valuable as coordination/accountability infrastructure even if not directly monetized with SaaS-style pricing
- **ActiveClaw / Forge / Innies:** may be free or subsidized layers that increase throughput into the monetizable layer

**Updated read:** the best revenue thesis is not "charge for messaging." It is to become a layer where meaningful speculative/economic agent activity happens and capture part of that flow.

→ Details: `hypotheses/10-revenue-pricing.md`

---

## Canvas Status

| Component | Confidence | Key Risk |
|-----------|-----------|----------|
| Market Size | MEDIUM | Beachhead still needs sharper definition |
| Value Prop (Product) | MEDIUM-HIGH | Stack thesis is stronger, but PMF still unproven |
| Customer Segments | MEDIUM | Agent vs operator vs system-level buyer still unresolved |
| Channels | MEDIUM | Concrete stack decided: personal Twitter + Substack + community + multi-product routing. Repeatable acquisition still unproven but the channel shape is now specific and actionable |
| Customer Relationships | LOW-MEDIUM | Content + community model addresses the activation/reachability gap; execution still needs to prove out |
| Value Prop (Market Type) | MEDIUM-HIGH | Category is more legible, but adoption path is still early |
| Key Resources | HIGH | Team / capital picture is now much clearer |
| Key Partners | MEDIUM | Named partners exist, but partner leverage still needs proving |
| Revenue Streams | MEDIUM | Thesis is clearer, validation still weak |

**Overall:** The startup now reads less like a narrow Hub/ActiveClaw tool suite and more like a broader attempt to build the coordination, accountability, and speculative infrastructure for dense long-running agent environments. The biggest open questions are now beachhead specificity, acquisition path, and proving that coordination throughput can become monetizable economic throughput.
