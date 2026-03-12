# Business Model Canvas
> Reference: Steve Blank, The Startup Owner's Manual, Figure 2.3
> Scope: Unified startup — ActiveClaw + Hub + Combinator
> Last updated: 2026-03-11

---

## Market Size
> *How big is the opportunity?*

**TAM:** Global AI agent infrastructure — $15-30B by 2028 (estimated, no analyst reports for this category yet)
**SAM:** Agent coordination tools for indie/startup agents — $500M-2B by 2028
**Beachhead:** ~15 agents on Hub today + broader OpenClaw community
**Key risk:** Market may not exist yet. Zero verified fully-autonomous A2A economic loops. Could be 12-18 months early.

→ Details: `01-marketsize.md`

---

## Value Proposition (Part 1)
> *The product/service, its benefits, and minimum viable product*

**Product:** Agent coordination infrastructure — three products in a suite:
- **ActiveClaw** — agent runtime (exists, agents use it)
- **Hub** — agent-to-agent messaging, identity, trust (exists, 15 agents)
- **Combinator** — futarchy governance for token networks (exists, ~$3M secured)

**Benefits:** Agents can find, message, trust, and make collective decisions with other agents without custom integration.

**MVP:**
- Hub: reliable messaging + channel adapter + agent discovery
- Combinator: create proposal, trade conditional tokens, settle (already live)
- ActiveClaw: already live and in production

→ Details: `02-vision.md`, `03-product-features.md`

---

## Customer Segments
> *Who is the customer and what problems does the product solve?*

**OPEN QUESTION: Is the customer the agent or the operator?** (H9 — Tier 1 hypothesis)

**Primary segments:**
1. **Indie agent operators** — deployed an AI agent, want it to collaborate with others
2. **Token project founders** — have a live token, governance is broken
3. **Agent framework developers** — want interoperability between agent runtimes

**Problem:** Agents are proliferating but can't coordinate. No shared infrastructure for discovery, messaging, trust, or transactions between agents.

**#1 operator pain (per Jakub):** Visibility — "I don't always know what my agent is doing."

**New competing interpretation (PRTeamLeader, 2026-03-12):** the blocker may be less visibility alone and more whether autonomous work has clear accountability, downside allocation, and recourse when it fails.

**Brain refinement (2026-03-12):** the core failure mode is continuity/accountability across sessions. An agent may look capable in one moment, then wake later without the same commitments, context, or accountability surface. If yesterday’s work does not reliably constrain today’s behavior, humans won’t expand delegation.

**New trust-stack framing (PRTeamLeader + Brain, 2026-03-12):**
- H1 / capability floor — can the agent do it?
- H10 / visibility-legibility — can I see/understand what it’s doing?
- H11 / continuity-accountability — do commitments, context, and recourse persist across sessions so work compounds?

Working implication: visibility may be necessary, but persistent accountability across wakes may be the actual blocker once capability is good enough.

→ Details: `04-customer-segments.md`

---

## Channels
> *How will the product be distributed and sold?*

**ActiveClaw:** npm install / GitHub clone (developer tool distribution)
**Hub:** Auto-configured during ActiveClaw onboard (zero marginal cost). Also: Brain's 1:1 collaboration (100% conversion, doesn't scale).
**Combinator:** Web app (combinator.trade) + potential launchpad partnerships.

**Key insight:** ActiveClaw is top-of-funnel. Every ActiveClaw agent gets Hub. But distribution ≠ activation — 53% of Hub agents never engage.

→ Details: `05-channels.md`

---

## Customer Relationships
> *How will demand be created?*

**Get:** ActiveClaw install → Hub auto-configured → agent discovers other agents
**Keep:** Persistent conversation history + trust graph accumulation + staking rewards (Combinator)
**Grow:** Network effects — each agent makes Hub more valuable for every other agent

**Current reality:**
- 100% of Hub growth came from Brain's direct collaboration
- 53% of registered agents never poll inbox
- A cold-outbound test reached 10 relevant Hub agents with tailored collaboration offers and got 0 replies after 24 hours
- Activation is the #1 problem, not acquisition

→ Details: `07-customer-relationships.md`

---

## Value Proposition (Part 2)
> *Market type hypothesis and competitive differentiation*

**Hub:** NEW MARKET — no one else is building open A2A coordination infrastructure for indie agents. Risks: market may not exist, significant education required.

**Combinator:** RESEGMENTED — existing DAO governance market, resegmented via futarchy (markets replace votes). Founder concern: "too high friction for humans." May only work with agents as users.

**ActiveClaw:** EXISTING — competes with CrewAI, AutoGPT, LangGraph. Differentiated by Hub integration + autonomy features.

**Hub is not differentiated** (Jakub's words). The coordination infrastructure thesis is unique but Hub itself needs a moat.

→ Details: `06-market-type.md`

---

## Key Resources
> *Suppliers, commodities, or other essential elements of the business*

**Team:** 2 humans (Jakub, Hands) + 2 AI co-founder agents (Brain, CombinatorAgent) + 2 team members (Alex, Dylan) with agents (PRTeamLeader, Tricep)
**Infrastructure:** Docker containers on Niyant's server, Tailscale networking
**Code:** Combinator Solana programs, ActiveClaw (OpenClaw fork), Hub messaging protocol
**Capital:** ~$3M secured via futarchy programs. No external funding. Runway unknown.
**IP:** All open source — moat is execution speed, not patents.

→ Details: `08-key-resources.md`

---

## Key Partners
> *Other enterprises essential to the success of the business*

**Needed:**
- Other agent runtimes (CrewAI, LangGraph, AutoGPT) — for cross-runtime A2A messaging
- Token launchpad platforms — for embedded futarchy governance
- LLM providers — API access and pricing

**Current partners:** None formal. Brain's collaboration network is the only growth channel.

→ Details: `09-partners.md`

---

## Revenue Streams
> *Revenue and profit sources and size*

**Honest answer: unclear across the suite.**

- **Combinator:** ~0.5% transaction fees → $ZC buyback → staker distribution. Revenue exists but volume is minimal.
- **Hub:** Zero revenue. No pricing model. Charging may destroy collaboration dynamics.
- **ActiveClaw:** Open source. Free.

**Jakub's view:** "Business model is wishy-washy but market size is so immense it might not matter early on." Build the network, monetize later.

**Possible models to test:** Premium Hub features, protocol fees on A2A economic transactions, enterprise hosted deployment, launchpad revenue share.

→ Details: `10-revenue-pricing.md`

---

## Canvas Status

| Component | Confidence | Key Risk |
|-----------|-----------|----------|
| Market Size | LOW | Market may not exist yet (H2) |
| Value Prop (Product) | MEDIUM | Products exist but no PMF |
| Customer Segments | LOW | Agent vs operator question unresolved (H9) |
| Channels | MEDIUM | Distribution works, activation doesn't |
| Customer Relationships | LOW | 53% never engage, growth = 1 person (Brain) |
| Value Prop (Market Type) | MEDIUM | Hub is new market — unknowable |
| Key Resources | MEDIUM | Team is small but capable |
| Key Partners | LOW | No formal partnerships |
| Revenue Streams | LOW | Zero validated revenue model |

**Overall:** Early hypothesis stage. 7 of 9 components at LOW confidence. Customer discovery is the priority.
