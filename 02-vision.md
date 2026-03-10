# Product Vision
> Based on Steve Blank's Customer Discovery Phase 1: Value Proposition Hypotheses / Product Vision
> Source: Four Steps to the Epiphany (Ch. 3)
> Goal: Team agreement on the long-term vision and 18-month schedule

---

## Vision

### What's your long-term vision for your company?
> Every token network governs itself through markets, not votes. Percent becomes the default futarchy infrastructure layer — any builder can launch a token where decisions are made by prediction markets rather than governance votes or founder fiat. Permissionless, multi-option (up to 6 options per proposal), on Solana.

### What do you ultimately want to change or solve?
> Token networks are stuck: builders can't adjust their tokens post-launch without rugging investors, and governance (when it exists) is broken — low participation, whale domination, uninformed voting. The result is stagnation or rug pulls. We want to make it so token networks can evolve continuously based on real market signal, not politics.

### Are you going to do it with a series of products?
> Continuously improving core product. The futarchy protocol is the foundation; the trading UI, SDKs, and launchpad features layer on top. Eventually an ecosystem of interwoven tools: decision market creation, token launching with built-in futarchy governance, analytics, and integrations with existing trading terminals.

### How do you expand into adjacent markets?
> 1. Start with crypto-native builders who already have tokens and need governance
> 2. Expand to new token launches (launchpad with built-in futarchy from day 1)
> 3. Expand to non-crypto DAOs and organizations that need decentralized decision-making
> 4. Potentially any organization that makes collective decisions (prediction markets as a service)

### Do you need to get people to change their behavior?
*For each user type, what new behavior is required?*
> - **Builders/token launchers** → need to adopt futarchy as their governance mechanism instead of multisig or token voting. Need to hand over parameter control to decision markets.
> - **Traders** → need to trade conditional tokens in decision markets (new instrument). Need to think about "which option makes the token more valuable?" not just "number go up."
> - **Token holders/community** → need to participate in governance by trading rather than voting. Lower barrier (profit motive) but unfamiliar mechanic.
> - **[NEEDS VALIDATION]** How much education is required? Do users need to understand futarchy to use it, or can the UX abstract it away?

### What will the world look like 1.5 years after you arrive on the scene? Three years?

**1.5 years:**
> - Multiple live token networks governing via Percent's futarchy infrastructure
> - Decision markets are recognized as a legitimate governance primitive in crypto (not just a MetaDAO experiment)
> - Builders actively choose futarchy over token voting for consequential decisions
> - A small but active trader base profiting from governance markets
> - [NEEDS VALIDATION — from Brain: what's the realistic adoption curve?]

**3 years:**
> - Futarchy is a standard option when launching a new token — like "do you want governance? here's futarchy"
> - Non-crypto-native builders consider on-chain decision markets for organizational governance
> - Ecosystem of tools built on top of Percent's infrastructure
> - Golden age of crypto projects that actually iterate and improve because governance works
> - [NEEDS VALIDATION — is this too aggressive or too conservative?]

### Put together a short narrative in bullets about your strategy
> - **The problem we're solving:** Token networks can't evolve. Builders either rug (change things unilaterally) or stagnate (can't change anything because governance is broken). Misaligned incentives between builders, investors, and communities result in few viable crypto products.
> - **Our solution:** Futarchy-powered tokens that govern themselves through prediction markets. Instead of voting (which is uninformed and low-participation), stakeholders express views by trading conditional tokens. The market aggregates information and the winning option executes automatically. Permissionless, multi-option, on Solana.
> - **The GTM:**
>   - Dogfood internally — run Percent's own token ($ZC) on futarchy
>   - Prove the mechanism works on our own consequential decisions
>   - Onboard early builder partners who need governance for their tokens
>   - Build launchpad features so new tokens launch with futarchy from day 1
>   - [NEEDS VALIDATION — Brain: what's the current GTM motion? Partnerships? Outbound? Token-led?]

---

## Delivery Dates

### Short Term
> [NEEDS INPUT — Brain: what's shipping this month / next month?]

### 18-Month Product Vision & Delivery Schedule
> [NEEDS INPUT — Brain: current roadmap priorities?]
> 
> Known from codebase & prior context:
> - Trading terminal / charting (TradingView integration exists)
> - Staking vault with unbonding and slashing
> - Decision market UI + backend (live)
> - How-it-works educational content (shipped)
> - [NEEDS VALIDATION — what's next on the roadmap?]

---

## Long-Term Product Strategy

### Will your product create network effects?
> Yes. Each additional trader in a decision market improves price discovery, which makes governance outcomes better, which attracts more builders, which creates more markets, which attracts more traders. Liquidity begets liquidity.

### Can you price it with a predictable model?
> No — highly reflexive. Revenue is a function of trading volume in decision markets, which depends on proposal contentiousness, token price, and trader participation. Transaction fee model (~0.5% spot, 0.5% futarchy trades) is simple but volume is unpredictable.

### Can you create customer lock-in / high switching costs?
> Medium-high. Once a token network's governance is built on Percent's futarchy infrastructure:
> - Historical decision market data becomes a governance track record
> - Smart contract integrations are deep (token parameters controlled by futarchy outcomes)
> - Migrating governance to a different system requires community trust reset
> - But the protocol is open source (AGPL 3.0), so someone could fork — lock-in is practical, not technical

### Can you have high gross margins?
> Extremely high. Protocol fees are on-chain with near-zero marginal cost. Infrastructure costs are minimal (Solana transaction costs are fractions of a cent). No COGS beyond hosting.

### Does it have organic demand versus requiring marketing spend?
> Hypothesis: organic demand driven by profit motive. Traders come for profit opportunity in mispriced decision markets. Builders come because governance actually works. Token emissions can subsidize early growth loops. But [NEEDS VALIDATION — is there evidence of organic demand yet, or is everything still push-driven?]

### List product enhancements anticipated up to 18 months
> - Launchpad: new tokens launch with futarchy governance built-in
> - Improved decision market UX (reduce friction to create and trade)
> - Trading terminal SDK for third-party integrations
> - Capital-efficient contracts (reduce liquidity requirements)
> - Decision markets on protocol parameters (fees, mint authority, etc.)
> - Analytics and market intelligence tools
> - [NEEDS VALIDATION — Brain: what's actually prioritized vs. aspirational?]

### List key follow-on product enhancements
> - Cross-chain futarchy (beyond Solana)
> - Private voting via ZK proofs (prevent whale copying, front-running)
> - Decision markets as a service for non-crypto organizations
> - Ecosystem fund / buyback system driven by protocol revenue
> - [NEEDS VALIDATION — long-term vision items from Brain]

---

## Exit Criteria (Pass/Fail)

- [ ] Vision narrative complete
- [ ] Long-term product strategy defined
- [ ] Present plan to the team, get no pushback on any given item
- [ ] All [NEEDS VALIDATION] items resolved with Brain/team input

---

## Status
- **Phase:** Customer Discovery — Phase 1 (Stating Hypotheses)
- **Last updated:** 2026-03-10
- **Awaiting:** Brain response on current-state product details, GTM, roadmap
- **Sources used:** MEMORY.md, old Futarchy Game Plan docx, codebase (how-it-works.html, staking IDL, landing page), prior conversations with Jakub
