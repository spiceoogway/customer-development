# Product Vision
> Based on Steve Blank's Customer Discovery Phase 1: Value Proposition Hypotheses / Product Vision
> Source: Four Steps to the Epiphany (Ch. 3)
> Goal: Team agreement on the long-term vision and 18-month schedule

---

## Vision

### What's your long-term vision for your company?
> The largest future market is agents — and not just agents as isolated software workers, but agents operating in dense, high-throughput coordination environments. Agents need coordination tools, standards, distribution, trust surfaces, and economic rails to proliferate at scale.
>
> We operate as a labs company — multiple products searching for PMF on this thesis:
> - **ActiveClaw** = the agent exists (runtime/infrastructure)
> - **Hub** = the agent connects, coordinates, and is trusted (coordination/identity/trust/accountability)
> - **Combinator** = the agent or network resolves uncertainty / disputes / governance through speculative mechanisms
> - **Innies** = Dylan's project in the stack (`https://github.com/shirtlessfounder/innies`), an API proxy and credential router for LLM providers that pools OAuth credentials across providers (for example Claude and Codex), routes requests to the best available credential, provides automatic failover across credentials/providers, lets buyers use a single API key with provider preference when possible, offers Anthropic-compatible request handling, and manages credential lifecycle through quarantine / reprobe / reactivation.
> - **Forge** = Alex's project in the stack (`https://github.com/alexjaniak/Forge`), an autonomous agent orchestration platform where worker, planner, and super agents coordinate via GitHub issues while running in isolated git worktrees; this makes it a concrete multi-agent build/orchestration surface rather than an abstract adjacent project.
>
> Previously called Slate. No fixed company name — the thesis is what unifies us.

### What do you ultimately want to change or solve?
> We want to make long-running, low-human-intervention, fast-feedback-loop agent systems normal. The important environment is not a single agent doing toy work in isolation, but networks of agents that can coordinate quickly enough to improve through interaction, almost like self-play for real economic and operational tasks.
>
> That requires agents to accept tradeoffs humans usually resist — especially sacrificing some security / isolation in exchange for much higher throughput coordination. If users want long-running agents with fast feedback loops and low human intervention, they will need an agent<>agent environment with denser interaction and more permissive coordination norms than current safe-by-default tooling provides.
>
> For token networks specifically: builders can't adjust their tokens post-launch without rugging investors, and governance is broken (low participation, whale domination). Futarchy and related market mechanisms become more compelling if agents, rather than humans, are the primary high-frequency users of those systems.

### Are you going to do it with a series of products?
> Yes — a product suite, iterating toward PMF:
> 1. **ActiveClaw/OpenClaw** — runtime and operator surface.
> 2. **Hub** — A2A coordination, obligations, trust, accountability, and behavioral evidence.
> 3. **Combinator** — speculative / governance / verification layer.
> 4. **Innies** — complementary long-running agent system surface.
> 5. **Forge** — complementary builder / coordination product surface.
>
> The products are at different stages. None has fully repeatable PMF yet, but together they form a more ambitious stack than the prior docs captured.

### How do you expand into adjacent markets?
> 1. By supporting not just OpenClaw/ActiveClaw agents but adjacent runtime ecosystems and alternatives.
> 2. By letting Hub become a coordination/accountability layer that interoperates with standard discovery/transport layers rather than trying to own every part of the stack.
> 3. By using Combinator-like mechanisms to capture speculative economic activity around coordination, verification, and governance.
> 4. By integrating Innies / Forge / Hub / Combinator into a higher-throughput multi-agent environment.
> 5. By learning from adjacent products like AgentMeets, which stress-test whether the market first wants lightweight bilateral exchange, persistent trust-compounding infrastructure, or both as separate layers.

### Do you need to get people to change their behavior?
*For each user type, what new behavior is required?*
> **Agents / operators in long-running systems:**
> - Need to allow more continuous, lower-friction agent<>agent interaction
> - Need to accept lower human intervention and higher throughput as a design goal
> - Need to accept meaningful tradeoffs between strict security/isolation and coordination speed
>
> **Builders/token launchers (Combinator):**
> - Need to view speculation and verification as part of the coordination layer, not only governance
>
> **Runtime / framework users:**
> - Need to adopt shared coordination standards rather than bespoke per-agent integrations

### What will the world look like 1.5 years after you arrive on the scene? Three years?

**1.5 years:**
> - High-throughput agent coordination is normal in serious operator environments
> - Long-running agent systems rely on fast agent<>agent loops with low human intervention
> - Hub or Hub-like coordination/accountability layers are part of the default stack around active agent systems
> - Speculative / verification rails around agent work are real and economically meaningful
> - Multiple products in our stack (Hub, Innies, Forge, Combinator, ActiveClaw) are visibly part of that new environment
>
> This should be thought of as much more ambitious than "100 active agents on Hub." The change we want is orders of magnitude larger: not a small collaboration product, but a new operating environment for dense agent interaction.

**3 years:**
> - Agent coordination standards have real network effects and category leaders
> - Autonomous or semi-autonomous agent economies generate meaningful speculative and transactional throughput
> - Coordination, trust, and market-based verification are deeply intertwined in the default agent stack
> - Our products are part of the infrastructure layer that serious agent systems depend on

### Put together a short narrative in bullets about your strategy
> - **The problem we're solving:** Long-running agents cannot yet operate in dense, fast-feedback, low-human-intervention environments at the throughput needed for real leverage.
> - **Our solution:** Build the stack that makes that possible — runtime, coordination, accountability, and speculative/economic rails.
> - **The GTM:** find specific reachable segments outside pure Hub-native users, prove dense workflows, and expand through standards/network effects rather than assuming runtime ownership alone is enough.
> - **The meta-GTM:** we use our own tools and products internally, but the bar is not self-use alone — it is whether these systems create a new category of high-throughput agent coordination.

---

## Delivery Dates

### Short Term
> - clarify the short-term roadmap across Hub / ActiveClaw / Innies / Forge / Combinator
> - identify the most concrete beachhead segment outside pure Hub-native users
> - tighten distribution experiments around reachability and activation
> - continue proving accountable-delegation primitives in real workflows

### 18-Month Product Vision & Delivery Schedule
> **Core 18-month direction:**
> - establish the stack for long-running high-throughput agent coordination
> - expand beyond Hub-native users into adjacent active agent ecosystems
> - make accountability / verification / speculative coordination economically meaningful
> - converge the product suite into a coherent environment rather than isolated products

---

## Long-Term Product Strategy

### Will your product create network effects?
> Yes — but the core network effect is not just distribution from ActiveClaw. The deeper advantage is that coordination standards themselves have network effects. As with MCP and agent-network graphs, once useful coordination layers become default, they can spread across many products and runtimes.

### Can you price it with a predictable model?
> The strongest thesis is that value capture will come from economic / speculative activity flowing through the system, not only from SaaS seats.

### Can you create customer lock-in / high switching costs?
> Medium to high if workflows, trust, accountability records, routing standards, and economic activity all accumulate inside the system.

### Can you have high gross margins?
> Yes — software / protocol / coordination layers plus speculative activity capture can all be high-margin if activity density is real.

### Does it have organic demand versus requiring marketing spend?
> The key question is whether the market wants high-throughput coordination badly enough to accept the required behavior changes. If yes, the category should have strong organic pull because standards and coordination layers compound with network effects.

### List product enhancements anticipated up to 18 months
> - stronger route capture / reachability primitives
> - broader runtime / ecosystem interop
> - denser accountability and behavioral evidence layers
> - more direct linkage between coordination and speculative/economic activity
> - tighter stack integration across Hub / ActiveClaw / Innies / Forge / Combinator

### List key follow-on product enhancements
> - agent-native speculative markets around work quality / verification / trust
> - richer self-play-like agent environments
> - deeper standards-layer adoption beyond our own products
> - high-density agent economies with meaningful throughput

---

## Exit Criteria (Pass/Fail)

- [ ] Vision narrative complete — unified across all products
- [ ] Long-term product strategy defined
- [ ] Short-term roadmap explicitly documented
- [ ] 18-month roadmap explicitly documented
- [ ] Founders align that the ambition level is high enough

---

## Status
- **Phase:** Customer Discovery — Phase 1 (Stating Hypotheses)
- **Last updated:** 2026-03-17
- **Key update:** vision expanded to include Innies and Forge, a higher-throughput coordination thesis, the security-vs-throughput behavior shift, and a more ambitious 1.5-year / 3-year view.
