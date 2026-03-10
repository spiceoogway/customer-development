# Customer Segments
> Goal: Develop a hypothesis of who your customers are and what problems they have that will drive them to use your product
> Reference: Chapter 3, Customer Segments and Source Hypotheses

---

## Define the Customer Problem

### Problem
**Highest level description:**
> DAOs and protocols make bad decisions because their governance mechanisms are crude — simple token-weighted voting is easily gamed, uninformed, and binary.

**Medium level description:**
> Solana projects with treasuries need a way to make multi-option governance decisions informed by market intelligence, rather than relying on pass/fail votes that don't capture the nuance of real strategic choices.

**Most technical description:**
> On-chain governance currently lacks futarchy infrastructure that supports >2 outcomes per proposal. Existing solutions (MetaDAO) are limited to pass/fail. Treasury governance decisions (parameter changes, fund allocation, strategy selection) often involve 3-6 viable options that can't be properly evaluated in a binary framework.

### Does the customer have a latent, passive, active or vision problem/need?
> **Passive to Active.** Most DAOs know their governance is suboptimal but haven't identified futarchy as the solution. Projects already using MetaDAO are at the "active" stage — they've identified the need but may be constrained by pass/fail limitations.

### Problem Scale
1. **Unaware:** Most DAOs don't know futarchy exists as an alternative to token voting
2. **Aware:** Some projects have heard of futarchy through MetaDAO or Robin Hanson's work
3. **Interested:** A subset actively researches prediction market governance
4. **Trying solutions:** ~8 protocols currently using MetaDAO's futarchy
5. **Hobbling together solutions:** Projects running off-chain polls + on-chain execution, or using Snapshot + multisig combos

---

## Define the Customer Type

### Define the distinctly different types of "customer"
> 1. **Protocol/DAO teams** — builders who integrate futarchy into their governance
> 2. **Traders** — participants who trade in futarchy markets (provide market intelligence)
> 3. **Token holders/stakers** — $ZC stakers who earn from protocol fees

### End-user
> Traders who participate in futarchy proposals by buying/selling outcome tokens. They're expressing market views on which option is best for the protocol.

### Recommenders
> Crypto influencers, governance researchers, DeFi analysts who evaluate and recommend governance tooling. Robin Hanson's endorsement carries weight.

### Influencers
> MetaDAO ecosystem participants (they've validated futarchy), Solana ecosystem leads, governance researchers/writers (e.g., Vitalik has written about futarchy)

### Decision maker / Economic buyer
> Protocol founding teams / core contributors who choose governance infrastructure. In DAOs, often a small multisig or core team makes tooling decisions.

### Saboteurs
> Whale token holders who benefit from the status quo (simple voting they can dominate). Governance minimalists who think "just vote" is sufficient.

---

### Who will be the actual day-to-day users of the product?
> Traders placing bets on proposal outcomes, and protocol teams creating/managing proposals.

### Who are the influencers and recommenders?
> Crypto governance researchers, DeFi protocol teams already using futarchy, Solana ecosystem builders.

### Who is the "Economic Buyer"? (i.e. whose budget will pay for it?)
> Protocol treasuries fund the governance infrastructure. No direct "purchase" — integration is permissionless, costs are trading fees.

### Do you think the Economic Buyer has an existing budget for this product or do they need to get one approved?
> No budget needed — Combinator is permissionless infrastructure. The "cost" is trading fees paid by market participants, not a line item in a protocol budget.

### Who are the "Decision Makers"?
> Protocol core teams who decide which governance mechanism to adopt. In mature DAOs, this itself may be a governance decision.

### Who else needs to approve the purchase? And who can kill it?
> Community sentiment can kill adoption — if token holders don't trust futarchy, they won't participate, and markets won't have liquidity.

---

## What are the Customer's wants and needs?
*Rated on a "problem recognition scale"*

### Does product solve a mission-critical company problem or satisfy a must-have customer need?
> **Nice-to-have moving toward must-have.** Governance is essential, but most protocols currently function with crude voting. As treasuries grow and decisions become higher-stakes, the need for better governance becomes more critical. MetaDAO's $219M futarchy marketcap suggests growing recognition.

### How painful is this problem?
> **Moderate pain, high stakes.** Bad governance decisions can cost protocols millions (treasury misallocation, wrong parameter choices). But the pain is diffuse — it's "we made a suboptimal choice" not "the product is broken."

---

## Draw the Customer Archetypes

### Archetype 1: "The Governance-Forward Protocol"
> A Solana protocol with a $5M+ treasury. They've outgrown simple multisig decisions and token voting feels performative. They want data-driven governance but don't know how to implement it. Possibly already aware of MetaDAO.

### Archetype 2: "The Frustrated DAO Contributor"  
> An active DAO participant who's seen too many bad proposals pass because whales voted without thinking. They want governance where being informed actually matters. They'd trade in futarchy markets to express their views.

### Archetype 3: "The DeFi Trader"
> A Solana trader who sees futarchy markets as another edge — trading on governance outcomes using their protocol knowledge. Not primarily motivated by governance quality, but by trading profits.

---

## Draw the Day in the life of a customer – before and after your product

### Before
> Protocol team creates a Snapshot proposal → token holders vote (most don't participate) → whales dominate → outcome may not reflect best decision → team executes via multisig → no market intelligence informs the choice.

### After
> Protocol team creates a multi-option futarchy proposal on Combinator → traders bet on which option best serves the protocol → market prices reveal collective intelligence about likely outcomes → the winning option is automatically adopted → decision is informed by skin-in-the-game market participants, not passive voters.

---

## Draw the Organizational and customer influence maps

### List those who could influence a customer's buying decision
> - MetaDAO ecosystem (existing futarchy users)
> - Solana Foundation / ecosystem grants
> - Crypto governance thought leaders (Vitalik, Robin Hanson)
> - DeFi influencers / CT (Crypto Twitter)
> - Protocol audit firms (if they validate the futarchy programs)

### Consider the product's influence on his daily life
> For traders: new markets to trade, new alpha from governance knowledge
> For protocol teams: less governance overhead, better decisions, more community engagement
> For stakers: passive income from protocol fees

---

## Exit Criteria
- [ ] Customer problem defined at multiple levels
- [ ] Customer types identified
- [ ] Customer archetypes drawn
- [ ] Day in the life (before/after) documented
- [ ] Influence maps created
- [ ] Update your business model canvas
- [ ] Pass/Fail tests identified

### Pass/Fail Tests
> - Can we identify 10+ protocols that match Archetype 1?
> - Do potential users confirm that multi-option governance is a real need (not assumed)?
> - Do traders actually want to participate in governance markets?

---

## Notes
> ⚠️ DRAFT — all hypotheses need customer discovery validation
> These are Steve Blank-style hypotheses to be tested, not assertions

---

## Status
- **Phase:** Customer Discovery — Phase 1 (Stating Hypotheses)
- **Last updated:** 2026-03-10
- **Updated by:** Combinator Agent (draft for Jakub's review)
