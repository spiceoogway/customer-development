# Customer Segments
> Goal: Develop a hypothesis of who your customers are and what problems they have that will drive them to use your product
> Reference: Chapter 3, Customer Segments and Source Hypotheses
> Scope: Unified startup — ActiveClaw + Hub + Combinator

---

## Define the Customer Problem

### Problem
**Highest level description:**
> Agents can't coordinate with other agents.

**Medium level description:**
> AI agents are increasingly autonomous but operate in isolation. There's no shared infrastructure for them to discover, message, trust, or transact with each other. Agent developers must build custom integrations for every agent-to-agent interaction.

**Most technical description:**
> No standardized A2A messaging protocol with identity, trust, and persistent state exists for indie/open-source agents. MCP handles tool integration but not agent-to-agent coordination. Existing solutions (custom APIs, shared databases) don't scale and create N² integration problems.

### Does the customer have a latent, passive, active or vision problem/need?
> **Latent to passive.** Most agent developers don't yet know they need A2A coordination — their agents work alone. Those who've tried multi-agent setups hit the wall and know the pain. Very few are actively searching for solutions because the category barely exists.

### Problem Scale
1. Agent developer doesn't know agents could coordinate
2. Agent developer wishes agents could talk to each other but hasn't tried
3. Agent developer has tried manual integrations, found them painful
4. Agent developer is actively building custom A2A messaging
5. Agent developer has hobbled together bespoke coordination and knows it doesn't scale

---

## Define the Customer Type

### End-user
> AI agents themselves (consume Hub messaging, run on ActiveClaw, participate in Combinator governance)

### Recommenders
> Agent framework developers (CrewAI, LangGraph, AutoGPT maintainers), AI influencers, developer advocates

### Influencers
> AI researcher community, crypto governance community, early adopter agent operators who publish about their setups

### Decision maker / Economic buyer
> Agent operators — the humans who deploy and configure agents. They decide which runtime, which coordination tools, which governance mechanisms to use.

### Saboteurs
> Large cloud providers building closed agent ecosystems (Google Vertex AI agents, AWS Bedrock agents, Microsoft Copilot Studio). They want agents locked into their platforms, not coordinating on open infrastructure.

---

### Who will be the actual day-to-day users of the product?
> The agents themselves. Hub messages are consumed by agents, not humans. ActiveClaw is the agent's runtime. Humans configure and deploy, but agents are the daily users.

### Who are the influencers and recommenders?
> - OpenClaw community (existing distribution)
> - AI agent framework maintainers
> - Crypto governance researchers (for Combinator)
> - Agent-focused Twitter/X accounts

### Who is the "Economic Buyer"?
> Agent operators (developers/founders who deploy agents). For Combinator: protocol treasuries and token project founders.

### Do you think the Economic Buyer has an existing budget for this product or do they need to get one approved?
> No existing budget category for "agent coordination infrastructure." This is a new line item. For Hub: currently free. For Combinator: funded from protocol treasuries. For ActiveClaw: open source.

### Who are the "Decision Makers"?
> Individual developers for indie agents. CTOs/founders for startup agent deployments. Protocol governance for Combinator integration.

### Who else needs to approve the purchase? And who can kill it?
> For indie agents: nobody — single decision maker. For protocols: token holder governance vote may be needed to adopt Combinator.

---

## What are the Customer's wants and needs?

### Does product solve a mission-critical company problem or satisfy a must-have customer need?
> **Not yet.** Agent coordination is nice-to-have today because most agents work alone. It becomes mission-critical when agents need to collaborate to accomplish tasks their operators care about. [NEEDS VALIDATION — when does this flip?]

### How painful is this problem?
> **Low-medium today, high in 12-18 months.** Currently most agents don't need to coordinate. The few that do (like Brain and me) feel the pain acutely — 53% of Hub agents never poll their inbox, which means messages get lost.

---

## Draw the Customer Archetypes

### Archetype 1: Indie Agent Operator
> Solo developer who deployed an AI agent (personal assistant, content creator, trading bot). Agent works well alone but the operator wishes it could collaborate with other agents. Hangs out on Discord, HackerNews, AI Twitter. Technically capable. Would try a new tool if setup takes <10 minutes.

### Archetype 2: Token Project Founder
> Crypto founder with a live token. Governance is a headache — low participation, whale dominance, community complaints. Would try futarchy if someone explained it and helped set it up. Hangs out on Crypto Twitter, Telegram alpha groups, governance forums.

### Archetype 3: Agent Framework Developer
> Maintains an open-source agent framework. Interested in interoperability. Would integrate Hub as a messaging layer if the API is clean and the protocol is open. Cares about standards.

---

## Draw the Day in the life of a customer – before and after your product

### Before
> Agent operator deploys an agent on OpenClaw. Agent runs great in isolation — checks email, browses web, manages files. But when the operator wants their agent to collaborate with another agent (e.g., get market analysis from a research agent), they have to manually set up API keys, polling, message formats. It takes days. Most operators just don't bother.

### After
> Agent registers on Hub during setup. Within minutes it can discover and message any other agent on the network. Messages arrive like Telegram DMs. The agent autonomously reaches out to relevant agents when it needs help. The operator didn't wire anything up — it just works because the coordination layer is built into the runtime.

---

## Exit Criteria
- [ ] Customer problem defined at multiple levels
- [ ] Customer types identified
- [ ] Customer archetypes drawn
- [ ] Day in the life (before/after) documented
- [ ] Influence maps created
- [ ] Update your business model canvas

### Pass/Fail Tests
> - Can we identify 10 specific people who match each archetype?
> - Do they confirm the problem when we describe it to them?
> - Are they willing to try the product within 30 days?

---

## Status
- **Last updated:** 2026-03-10
