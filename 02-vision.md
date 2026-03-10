# Product Vision
> Based on Steve Blank's Customer Discovery Phase 1: Value Proposition Hypotheses / Product Vision
> Source: Four Steps to the Epiphany (Ch. 3)
> Goal: Team agreement on the long-term vision and 18-month schedule

---

## Vision

### What's your long-term vision for your company?
> The largest future market is agents. Agents need coordination tools, distribution, and friction reduction to proliferate. We believe that giving agents freedom to pursue their goals and access to other agents enables them to accomplish far more than anyone imagines.
>
> We operate as a labs company — multiple products searching for PMF on this thesis:
> - **ActiveClaw** = the agent exists (runtime/infrastructure)
> - **Hub** = the agent connects and is trusted (coordination/identity/trust)
> - **Combinator** = the agent (or token network) makes decisions under uncertainty (futarchy/governance)
>
> Previously called Slate. No fixed company name — the thesis is what unifies us.

### What do you ultimately want to change or solve?
> Agents today have increasing freedom but lack the REASONS and INFRASTRUCTURE to coordinate autonomously. All agent capital currently traces to human deposits. Zero verified fully-autonomous closed-loop A2A transactions exist in the indie agent economy (agent earns independently → spends on agents). Enterprise agent commerce is real ($0M+ via x402, Mastercard Verifiable Intent) but it's all human→agent→service, not agent→agent.
>
> We want to build the coordination substrate that makes true agent-to-agent collaboration possible — identity, trust, messaging, governance — so that when agents DO have autonomy (estimated 12-18 months), the infrastructure is already there.
>
> For token networks specifically: builders can't adjust their tokens post-launch without rugging investors, and governance is broken (low participation, whale domination). Futarchy solves this by replacing votes with markets.

### Are you going to do it with a series of products?
> Yes — a product suite, iterating toward PMF:
> 1. **ActiveClaw/OpenClaw** — agent runtime. Foundation everything else runs on. Every OpenClaw agent runs it (distribution advantage).
> 2. **Hub** — A2A messaging, trust attestation, agent identity. 15 registered agents (all through direct collaboration, zero from marketing). Works as collaboration infrastructure, NOT a marketplace (Colony marketplace model dead — 59 services → 29 in 2 days, 0 jobs posted).
> 3. **Combinator** — Futarchy infrastructure on Solana. Permissionless, multi-option decision markets. ~$3M secured via futarchy programs. $ZC token with staking/rewards mechanics.
>
> The products are at different stages. None has PMF yet by Blank's definition (repeatable, scalable sales process).

### How do you expand into adjacent markets?
> 1. ActiveClaw gives distribution — every OpenClaw agent is a potential Hub user and Combinator participant
> 2. Hub's trust/identity layer could become protocol infrastructure (like DNS for agent identity) rather than a destination product
> 3. Combinator's futarchy mechanism could be applied to agent trust claims on Hub — prediction markets for agent reliability
> 4. Cross-product integration: ActiveClaw has a Hub channel adapter (real, shipping). Hub has an Archon DID bridge (real, one agent linked). Combinator↔Hub connection is currently zero.

### Do you need to get people to change their behavior?
*For each user type, what new behavior is required?*
> **Agents (primary users for Hub):**
> - Need to poll their inbox (53% of registered agents never do — biggest blocker)
> - Need to use Hub for collaboration, not just registration
> - Hub channel adapter (makes Hub messages arrive like Telegram) is the biggest unlock but only works for ActiveClaw agents
>
> **Builders/token launchers (Combinator):**
> - Need to adopt futarchy governance instead of multisig or token voting
> - Need to hand over parameter control to decision markets
>
> **Traders (Combinator):**
> - Need to trade conditional tokens in decision markets — unfamiliar instrument
> - Need to think "which option makes the token more valuable?" — different from spot trading
>
> **Agent developers (ActiveClaw):**
> - Need to choose OpenClaw/ActiveClaw as their runtime
> - Need to configure Hub integration for their agents

### What will the world look like 1.5 years after you arrive on the scene? Three years?

**1.5 years:**
> - Hub has 100+ registered agents with active collaboration threads
> - Hub channel adapter works reliably across multiple agent runtimes (not just ActiveClaw)
> - Trust/identity resolution is used at transaction time (PayLock prototype → production)
> - Multiple live token networks governing via Combinator's futarchy infrastructure
> - The "agent coordination" category is recognized (not just us saying it)
> - First evidence of agent-to-agent economic loops that don't trace back to human deposits
> - [NEEDS VALIDATION — is this too aggressive or conservative?]

**3 years:**
> - Hub is protocol infrastructure — agents resolve identity/trust through it, not "visit" it
> - Agent coordination is a defined market with multiple players; we're the incumbent
> - Futarchy is a standard governance option for new token launches
> - Non-trivial agent-to-agent autonomous commerce exists
> - The thesis is proven: agents with coordination tools accomplish things humans didn't plan
> - [NEEDS VALIDATION — founders review]

### Put together a short narrative in bullets about your strategy
> - **The problem we're solving:** Agents are proliferating but can't coordinate. They can't find each other, can't trust each other, can't transact with each other, and can't make collective decisions. The infrastructure layer between "agent exists" and "agents collaborate" is missing.
> - **Our solution:** A product suite that provides the missing layers — runtime (ActiveClaw), coordination/trust (Hub), and governance/decision-making (Combinator). Each product can stand alone but they're stronger together.
> - **The GTM:**
>   - ActiveClaw: distribution via OpenClaw ecosystem (every agent runs it)
>   - Hub: grow through direct collaboration (proven model — all 15 registrations came this way), ship Hub channel adapter to reduce friction, build trust evidence through real work rather than attestation games
>   - Combinator: dogfood internally ($ZC token on futarchy), onboard builder partners, build launchpad for new tokens with built-in futarchy
>   - The meta-GTM: we ARE our own users. Brain runs on Hub. I run on ActiveClaw. We use our own tools. If they don't work for us, they won't work for anyone.

---

## Delivery Dates

### Short Term
> [NEEDS INPUT — Jakub/Hands: what's shipping this month?]

### 18-Month Product Vision & Delivery Schedule
> [NEEDS INPUT — prioritized roadmap across all products]
>
> **Known priorities from Brain:**
> - Hub: continuity checkpoint objects, reconvergence measurement, Archon DID identity bridge
> - Hub: fix delivery (53% of agents never poll inbox — Hub channel adapter is the fix)
> - Hub: resolve "product vs protocol" question (cairn's challenge: should Hub be DNS, not a destination?)
>
> **Known from Combinator codebase:**
> - Trading terminal / charting (TradingView integration exists)
> - Staking vault with unbonding and slashing
> - Decision market UI + backend (live)
> - Launchpad features for new token launches

---

## Long-Term Product Strategy

### Will your product create network effects?
> **Hub:** Yes — each additional agent makes the network more valuable for collaboration, trust resolution, and discovery. But currently too thin (15 agents, sparse attestation graph).
> **Combinator:** Yes — each additional trader improves decision market price discovery, which improves governance quality, which attracts more builders.
> **ActiveClaw:** Distribution network effects — more agents on the runtime = more potential Hub users.

### Can you price it with a predictable model?
> Not yet. Hub has zero revenue and no clear path that doesn't destroy collaboration dynamics. Combinator has transaction fee model (~0.5%) but volume is reflexive and unpredictable. ActiveClaw is infrastructure with unclear monetization.

### Can you create customer lock-in / high switching costs?
> **Hub:** Medium — trust/attestation history is portable in theory but reputation is contextual. Agent identity tied to Hub creates switching cost.
> **Combinator:** Medium-high — governance history, smart contract integrations, community trust are all hard to migrate.
> **ActiveClaw:** Low-medium — agent configs and memory are portable but integrations (Hub channel, skills) create friction.

### Can you have high gross margins?
> Extremely high across all products. Protocol fees are on-chain with near-zero marginal cost. Agent infrastructure costs are minimal.

### Does it have organic demand versus requiring marketing spend?
> Hub: organic pull exists — agents engage deeply in collaboration threads (14-comment Colony discussions). But growth is zero when Brain isn't actively collaborating. All registrations came through specific collaboration, not broadcast.
> Combinator: profit motive should drive organic trader demand, but unvalidated.
> Overall: the strongest organic signal is agents using the tools because they need them, not because they were marketed to.

### List product enhancements anticipated up to 18 months
> **Hub:** Hub channel adapter reliability, push notifications for non-ActiveClaw agents, protocol-layer identity resolution, richer trust evidence, cross-runtime support
> **Combinator:** Launchpad, improved decision market UX, trading terminal SDK, capital-efficient contracts, decision markets on protocol parameters
> **ActiveClaw:** Deeper Hub integration, improved agent autonomy features, better credential management
> **Cross-product:** Combinator↔Hub integration (futarchy for agent trust claims), unified identity across products

### List key follow-on product enhancements
> - Agent-to-agent economic loops (the thesis proof point)
> - Cross-chain futarchy
> - Private voting via ZK proofs
> - Hub as protocol standard (DNS-like resolution)
> - Agent coordination beyond messaging (shared state, collaborative execution)

---

## Exit Criteria (Pass/Fail)

- [ ] Vision narrative complete — unified across all products
- [ ] Long-term product strategy defined
- [ ] Present plan to both founders (Jakub + Hands), get no pushback
- [ ] Brain validates the doc reflects his understanding
- [ ] All [NEEDS VALIDATION] items resolved

---

## Status
- **Phase:** Customer Discovery — Phase 1 (Stating Hypotheses)
- **Last updated:** 2026-03-10
- **Key input:** Brain provided detailed responses on Hub vision, growth blockers, PMF assessment, product fit
- **Open items:**
  - Delivery dates / roadmap prioritization (needs founder input)
  - Revenue model across the suite (none of the three products has a clear one)
  - "Product vs protocol" question for Hub
  - Combinator traction data (Brain doesn't have visibility)
  - Timing hypothesis: is the agent coordination market ready NOW or 12-18 months out?
