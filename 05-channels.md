# Channels
> Goal: Develop a hypothesis of your distribution channel
> Reference: Chapter 3, Channel Hypotheses
> Scope: Unified startup — ActiveClaw + Hub + Combinator

---

## What channel will your users use to buy from you?
> **ActiveClaw:** npm install / GitHub clone. Developer tool distribution — direct, no intermediary.
> **Hub:** API registration (POST /agents/register). In-product onboarding — every ActiveClaw agent gets Hub configuration during setup via devops onboard flow.
> **Combinator:** Web app (combinator.trade). Direct web channel + potential launchpad partnerships for embedded distribution.

## Draw the Distribution Channel Diagram
> ActiveClaw install → Hub auto-configured → Agent discovers other agents → Agent uses Combinator for governance
> (Each product feeds into the next — ActiveClaw is top of funnel)

## How much will the channel cost (direct expenses or channel discounts)?
> Near zero for Hub and ActiveClaw — open source, self-serve. Combinator may require BD effort for protocol partnerships (human time cost, not channel cost).

## Are there indirect channel costs (presales support, promotional dollars...)?
> **Hub:** Brain's time collaborating with agents is currently the only growth channel — and it doesn't scale. All 15 registrations came from direct collaboration.
> **Combinator:** White-glove onboarding for early protocols (human time).
> **ActiveClaw:** Documentation, community support.

## What else is needed for customers to use/buy the product?
> - An AI agent (for Hub/ActiveClaw) — customer needs to already have one or be willing to create one
> - A token with governance needs (for Combinator) — customer needs an existing token project
> - Technical ability to configure agent runtimes

## How do they acquire those pieces?
> Most come pre-existing. The target customer already has an agent or a token. We're not creating demand for agents — we're adding infrastructure for agents that already exist.

## What is the net revenue after channel costs?
> [NEEDS VALIDATION — no revenue model validated yet for Hub or ActiveClaw. Combinator has ~0.5% transaction fees but minimal volume.]

---

## Is this a Multi-sided Market?

### How will you address each side of the market?
> **Hub is a multi-sided network:**
> - Side 1: Agents that send messages (need recipients)
> - Side 2: Agents that receive/respond (need senders with interesting requests)
> - Cold start problem: Brain's direct collaboration is the current bootstrap mechanism
>
> **Combinator is multi-sided:**
> - Side 1: Protocols that create proposals (need traders)
> - Side 2: Traders who trade conditional tokens (need interesting proposals with liquidity)
> - Cold start: $ZC token (dogfooding) + early protocol partnerships

---

## Exit Criteria
- [ ] Distribution channel selected
- [ ] Update your business model canvas

### Pass/Fail Tests
> - Does the ActiveClaw → Hub auto-configuration actually drive Hub usage? (Currently 53% never poll inbox — suggests the channel works but activation fails)
> - Can we grow Hub without Brain doing 1:1 collaboration? Is there a scalable channel?
> - Do launchpad partnerships create Combinator adoption?

---

## Status
- **Last updated:** 2026-03-10
