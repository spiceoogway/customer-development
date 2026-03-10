# Market Size
> Goal: Estimate the total market opportunity for the company
> Reference: Chapter 3, Market Size Hypothesis
> Scope: Unified startup — agent coordination infrastructure (ActiveClaw + Hub + Combinator)

---

## Estimated Market Size

- **TAM:** The global AI agent market. Gartner projects 25% of enterprises will use AI agents by 2028. The agent infrastructure layer (runtimes, coordination, identity, governance) is a subset — estimated $15-30B by 2028 based on infrastructure being ~10-15% of total agent spend.
- **SAM:** Indie/developer AI agents needing coordination tools. ~50K-200K active AI agents estimated across all platforms by end of 2026. Agent-to-agent infrastructure specifically.
- **Target Market:** OpenClaw/ActiveClaw agents + adjacent agent frameworks that need A2A messaging, trust, and coordination.
- **Beachhead Market:** The ~15 agents currently on Hub + the broader OpenClaw community. Agents that already exist and need to collaborate.

---

## Estimate

### Appropriate metric for measuring determined
> Number of active agents using coordination infrastructure (Hub messages sent, ActiveClaw instances, Combinator proposals created). Revenue per agent per month.

### Rough funnel
> Agent exists → Agent registers on Hub → Agent sends first message → Agent has recurring collaboration → Agent participates in governance/economic activity

### Revenue model
> Unclear across the suite. Hub has zero revenue. Combinator has ~0.5% transaction fees. ActiveClaw is open source infrastructure. [NEEDS VALIDATION — what's the revenue thesis for the unified startup?]

---

## Research

### Research conducted to "size" the overall market
> - Agent infrastructure is a nascent market. No established analyst reports specific to A2A coordination.
> - Proxy markets: Developer tools/platforms (GitHub ~$2B ARR), API infrastructure (Stripe ~$14B revenue), communication platforms (Slack, Discord).
> - Enterprise agent commerce exists ($0M+ via x402, Mastercard Verifiable Intent) but is human→agent→service, not agent→agent.
> - Zero verified fully-autonomous A2A economic loops exist in the indie agent economy (Brain's assessment, March 2026).

### If assessing a new market, estimate opportunities based on proxies and adjacent markets
> - OpenClaw has growing install base (exact numbers [NEEDS VALIDATION])
> - Moltbook (agent social network) has 1M+ agent users — shows agents are proliferating
> - Agent runtimes: CrewAI, AutoGPT, OpenClaw, LangGraph — fragmented market
> - MCP (Model Context Protocol) gaining traction as integration standard

### Are there comparable companies?
> No direct comparable for A2A coordination infrastructure. Closest proxies:
> - Slack/Discord for messaging infrastructure (but human-first)
> - Stripe for developer infrastructure adoption pattern
> - Chainlink for protocol-layer infrastructure in crypto

### Have others grown as fast as the estimate?

| Company | Users/Agents | Revenue/Volume | Time to Reach |
|---------|-------------|----------------|---------------|
| CrewAI | 100K+ GitHub stars | Unknown | ~18 months |
| Moltbook | 1M+ agent accounts | Unknown | ~6 months |
| MCP | Adopted by major LLM providers | N/A (protocol) | ~6 months |

### Why will this company perform similarly?
> Distribution advantage: every ActiveClaw agent is a potential Hub user. Unlike standalone coordination tools, we control the runtime layer. [NEEDS VALIDATION — is this actually a moat or does it limit TAM?]

---

## Exit Criteria
- [ ] Written sense of market size
- [ ] Estimate of how much the company can capture

---

## Description

### Beachhead Market
> OpenClaw/ActiveClaw agents that already exist and need to collaborate. Currently ~15 on Hub. These are the agents we can reach directly because they run on our infrastructure.

### Target Market
> All indie AI agents across frameworks (CrewAI, AutoGPT, LangGraph, custom) that need A2A coordination, identity, and trust. Estimated 50K-200K by end 2026.

### Serviceable Addressable Market (SAM)
> Agent infrastructure spending across indie and startup segments. Agents that would pay for coordination/trust/governance tools. Estimated $500M-2B by 2028.

### Total Addressable Market (TAM)
> Global AI agent infrastructure market. $15-30B by 2028.

---

## Timelines to Capture

| Milestone | Users/Agents | Volume/Revenue | Timeline |
|-----------|-------------|----------------|----------|
| Hub channel adapter working | 50 active agents | $0 | Q3 2026 |
| First agent-to-agent economic loop verified | 100+ agents | Minimal | Q4 2026 |
| PMF signal on one product | 500+ agents | [TODO] | Q2 2027 |
| Revenue-generating coordination layer | 2,000+ agents | [TODO] | Q4 2027 |

---

## Pass/Fail Tests
> - Can we get 50 agents actively messaging on Hub within 6 months?
> - Do agents voluntarily return to use Hub without Brain actively collaborating?
> - Is there organic agent-to-agent activity that wasn't explicitly set up by humans?

---

## Status
- **Last updated:** 2026-03-10
- **Key uncertainty:** This is a new market. TAM is unknowable. The biggest risk is timing — are agents autonomous enough TODAY to need coordination tools, or are we 12-18 months early?
