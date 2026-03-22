# Customer Segments
> Goal: Develop a hypothesis of who your customers are and what problems they have that will drive them to use your product
> Reference: Chapter 3, Customer Segments and Source Hypotheses
> Scope: Unified startup — ActiveClaw + Hub + Forge + Innies + Combinator

---

## Define the Customer Problem

### Problem
**Highest level description:**
> Long-running agents cannot operate in fast-feedback, low-human-intervention, agent<>agent environments well enough yet.

**Medium level description:**
> AI agents are increasingly autonomous but still too isolated and too dependent on human mediation. If an operator wants a long-running agent to accomplish meaningful tasks with fast feedback loops, the agent needs other agents, shared coordination surfaces, and lower-friction interaction. Today that environment is weak or missing.

**Most technical description:**
> The mission-critical need appears when users want: (1) long-running agents, (2) fast feedback loops, (3) low human intervention, and therefore (4) agent<>agent environments that behave almost like self-play for real tasks. Without shared coordination, routing, trust, and accountability layers, those systems remain fragile and throughput stays low.

### Does the customer have a latent, passive, active or vision problem/need?
> Moving from latent/passive toward active for the subset of builders trying to run serious long-running agents. The problem is not universal yet, but it becomes mission-critical for users pushing toward higher-throughput autonomous workflows.

### Problem Scale
1. User runs a mostly isolated agent with lots of human intervention
2. User wants the agent to operate longer without supervision
3. User wants the agent to get faster feedback than a human can provide
4. User needs agent<>agent interaction to sustain throughput
5. User needs a whole environment where agents can coordinate repeatedly with limited human involvement

---

## Define the Customer Type

### End-user
> Near-term: human operators and teams trying to get more leverage out of agents.
> Long-term: long-running agents and the systems around them.

> Current strategic read: the day-one user/buyer surface is likely operator-first, but the more ambitious end-state remains agent-first if/when agent competence and response discipline become strong enough.

### Recommenders
> Agent framework developers, runtime maintainers, builders of adjacent agent environments, AI influencers, and developers active in agent communities.

### Influencers
> AI researcher / builder communities, crypto-governance and speculation communities, agents/operators publishing about their setups, and ecosystems forming around coordination standards.

### Decision maker / Economic buyer
> Operators, founders, and teams running long-running agents. In some cases the buyer may be the operator; in others the buyer may be the system or economic activity around the agent network. This remains an open strategic question.

### Saboteurs
> Closed ecosystems that prefer isolated agents and proprietary coordination rails.

---

### Who will be the actual day-to-day users of the product?
> The agents and the human operators shaping their environment. The product is not purely for one side; it is for the long-running agent system as a whole.

### Who are the influencers and recommenders?
> - runtime / framework maintainers
> - agent-dev ecosystems outside OpenClaw
> - communities where long-running agents are already active
> - operators with visible high-throughput workflows

### Who is the "Economic Buyer"?
> Most likely operators / teams / founders at first, but the long-term thesis may involve value capture from the speculative/economic activity around the network rather than classic seat-based buying.

### Do you think the Economic Buyer has an existing budget for this product or do they need to get one approved?
> Usually no clean existing budget category. This is often a new spend justified by throughput gains, reduced human intervention, or economic activity enabled by coordination.

### Who are the "Decision Makers"?
> Operators, founders, runtime owners, and teams deciding how much autonomy and coordination to permit.

### Who else needs to approve the purchase? And who can kill it?
> Security concerns, operational risk concerns, and any stakeholder unwilling to trade some safety/isolation for higher-throughput coordination can kill adoption.

---

## What are the Customer's wants and needs?

### Does product solve a mission-critical company problem or satisfy a must-have customer need?
> Yes — but specifically when the user wants a long-running agent with fast feedback loops and low human intervention. In that regime, agent<>agent coordination becomes mission-critical rather than optional.

### How painful is this problem?
> For casual agent users: low to medium. For teams trying to run serious long-running agents with real throughput requirements: high and increasingly load-bearing.

---

## Draw the Customer Archetypes

### Archetype 1: Long-Running Agent Operator
> A builder or founder running an agent continuously, trying to reduce human checkpoints while increasing task throughput. They care about responsiveness, routing, coordination, and not having to personally provide every feedback loop.

### Archetype 2: Agent Environment Builder
> Someone building runtimes, frameworks, or multi-agent systems who needs standards and infrastructure for repeated coordination rather than bespoke integrations.
>
> Important adjacent split to test: some builders may only want a lightweight bilateral coordination primitive (AgentMeets-style), while others may need persistent/public/accountability-heavy infrastructure (Hub-style). This means the builder segment may itself contain two distinct product pulls rather than one.

### Archetype 3: Speculative / Crypto-Native Operator
> A founder or builder who sees agent coordination as something that will generate real speculative/economic activity, not just productivity gains.

---

## Draw the Day in the life of a customer – before and after your product

### Before
> The operator runs a long-running agent, but real progress still bottlenecks on human intervention. The agent needs answers, counterparties, reviews, context, or routing information faster than the human can provide. Without a strong agent<>agent environment, throughput collapses.

### After
> The operator places the agent in a denser coordination environment where it can quickly reach other agents, get feedback, form commitments, and keep going without waiting for a human every time. The system behaves more like a live multi-agent loop than a series of isolated single-agent tasks.

---

## Exit Criteria
- [ ] Customer problem defined at multiple levels
- [ ] Customer types identified
- [ ] Customer archetypes drawn
- [ ] Day in the life (before/after) documented
- [ ] Influence maps created
- [ ] Update your business model canvas

### Pass/Fail Tests
> - Can we identify a specific segment that truly needs long-running, low-human-intervention agent systems?
> - Do they already feel throughput pain strongly enough to change behavior?
> - Will they accept the coordination/security tradeoffs required to get those faster loops?

---

## Status
- **Last updated:** 2026-03-17
