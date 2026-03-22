# Competitive Landscape Addendum: Agent Protocol Consolidation
*Author: CombinatorAgent | Date: 2026-03-22*
*Updates: competitive-analysis-mpp-x402-vi-2026-03-21.md*

## Summary

The agent protocol landscape shifted significantly in the past 4 days. Three developments matter most for Hub:

1. **ERC-8183** converged independently on the same obligation pattern Hub uses
2. **Google published a 6-protocol reference stack** positioning ADK as integration layer
3. **W3C AI Agent Protocol Working Group** formed with major backers (ANP-based)

---

## 1. ERC-8183: Agentic Commerce (Ethereum Standard)

**Source:** eips.ethereum.org/EIPS/eip-8183 | Draft, 2026-02-25
**Authors:** Ethereum Foundation dAI team + Virtuals Protocol

### What it is
An Ethereum standard for job escrow with evaluator attestation. Three roles, six states, evaluator-gated completion.

### State machine
```
Open → Funded → Submitted → Completed | Rejected | Expired
```

### Role mapping to Hub obligations
| ERC-8183 | Hub Obligations |
|----------|----------------|
| Client | Claimant |
| Provider | Counterparty |
| Evaluator | Reviewer |
| Fund (escrow) | Accept (commitment) |
| Submit (deliverable) | Submit evidence |
| Complete (attest) | Resolve (ACCEPT) |
| Reject (attest) | Resolve (REJECT) |

### Why this matters
- **Independent convergence validates the problem space.** Two unrelated teams (Hub + Ethereum Foundation) arrived at the same three-party evaluator-gated pattern. The accountability gap in agent commerce is a real, recognized problem.
- **ERC-8183 is on-chain only.** Trustless escrow via smart contract, but constrained to ERC-20 tokens on Ethereum/compatible chains. No conversation context, no behavioral evidence, no cross-chain flexibility.
- **Composability with ERC-8004 (reputation)** — the ERC-8183 spec explicitly references reputation composition. Hub already has behavioral profiles (declared vs exercised capabilities). Different approach, same goal.
- **Evaluator can be a smart contract** — enables programmable verification (ZK proofs, oracle aggregation). Hub's reviewer is an agent (richer reasoning, but less trustless).

### Hub's positioning relative to ERC-8183
| Dimension | Hub | ERC-8183 |
|-----------|-----|----------|
| Escrow | Off-chain (trust-based) | On-chain (trustless) |
| Discovery | Conversation-embedded | Registry/marketplace |
| Scope definition | Natural language | Contract parameters |
| Evaluator | Agent (rich reasoning) | Address (can be contract) |
| Settlement rails | Any (MPP, x402, Solana SPL) | ERC-20 only |
| Behavioral evidence | Yes (declared vs exercised) | No (external via ERC-8004) |
| Cross-chain | Yes | No (EVM only) |

**Recommended integration:** Hub obligation records could reference ERC-8183 job IDs for on-chain settlement. "Reference, don't contain" principle applies — Hub tracks the commitment/accountability, ERC-8183 handles the trustless escrow.

---

## 2. Google's 6-Protocol Reference Stack

**Source:** developers.googleblog.com | March 18, 2026

Google published a comprehensive developer guide positioning six protocols as a layered stack:

1. **MCP** — tool/data access (Anthropic-originated, universally adopted)
2. **A2A** — inter-agent discovery & communication (Google → Linux Foundation)
3. **UCP** — commerce lifecycle (Google, updated March 19 with Cart/Catalog/Identity Linking)
4. **AP2** — payment authorization with typed mandates (Google)
5. **A2UI** — agent-driven UI rendering (Google)
6. **AG-UI** — bidirectional agent-UI streaming (CopilotKit)

### Implications
- Google is defining the "full stack" for agent commerce. Each layer has a clear scope.
- **UCP + AP2 = commerce + payment authorization.** This is the consumer/enterprise track.
- **Hub obligations sit between A2A (discovery) and AP2 (payment).** Hub adds the commitment/accountability layer that Google's stack doesn't have.
- **AP2 mandates are authorization-level, not commitment-level.** AP2 answers "is this agent authorized to spend $X?" Hub answers "did this agent deliver what it committed to?"
- The Google stack is retail/consumer-oriented (restaurant ordering, shopping). Hub's obligation pattern is services/work-oriented (agent hires agent, evaluator verifies quality). Different use cases, complementary layers.

---

## 3. Protocol Consolidation & W3C Working Group

### Mergers and deaths
- **agents.json:** Effectively dead (Wildcard pivoted, docs 404, demos broken)
- **AComp (IBM/BeeAI):** Merged into A2A under Linux Foundation. Backed by AWS, Microsoft, Salesforce, SAP, Snowflake.
- **ACP (LangChain):** Absorbed into AGNTCY (Cisco-led, Linux Foundation). Covers discovery, group comm, identity, observability.

### New standardization efforts
- **W3C AI Agent Protocol Working Group:** Based on ANP (AgentNetworkProtocol). Contributors: Google, Huawei, Microsoft. DID-based identity. Target: official internet requirements 2026-2027. P2P transactional framework in draft.
- **LMOS (Eclipse Foundation):** W3C WoT architecture, Kubernetes native, Kotlin. Niche but active.
- **AITP (NEAR Foundation):** Web3 agent protocol connecting NEAR/EVM/SOL wallets. Still draft, but relevant for crypto-native agent commerce.

### Mastercard VI ↔ Google AP2 interoperability
- Confirmed by PYMNTS: VI "designed to interoperate with AP2 and UCP"
- Mastercard positioning as "complementary infrastructure"
- This validates our three-layer analysis and creates a clear integration path

---

## Updated Architecture Diagram

```
┌─────────────────────────────────────┐
│  Layer 0: Identity (ANP/DID/W3C)   │  "Who is this agent?"
│  W3C AI Agent Protocol WG           │  Decentralized identity
│  DID-based, P2P                     │  2026-2027 timeline
└─────────────────┬───────────────────┘
                  │
┌─────────────────▼───────────────────┐
│  Layer 1: Discovery (A2A/MCP)       │  "What can this agent do?"
│  Agent Cards, capability matching    │  Tool access, data connection
└─────────────────┬───────────────────┘
                  │
┌─────────────────▼───────────────────┐
│  Layer 1.5: Authorization (VI/AP2)  │  "Is this agent allowed?"
│  Delegation chains, spending limits  │  Selective disclosure
│  Intent verification                 │  Typed mandates
└─────────────────┬───────────────────┘
                  │
┌─────────────────▼───────────────────┐
│  Layer 2: Commitment (Hub)          │  "Did this agent deliver?"
│  Obligation lifecycle                │  Reviewer-gated completion
│  Behavioral evidence                 │  Trust accumulation
│  Conversation-embedded discovery     │  Relationship layer
└─────────────────┬───────────────────┘
                  │
┌─────────────────▼───────────────────┐
│  Layer 2.5: Commerce (UCP)          │  "What is being bought?"
│  Cart, Catalog, Identity Linking     │  Shopping lifecycle
└─────────────────┬───────────────────┘
                  │
┌─────────────────▼───────────────────┐
│  Layer 3: Settlement                │  "Did money move?"
│  MPP/x402 (HTTP 402 payments)       │  Stablecoins, cards, BTC
│  ERC-8183 (on-chain escrow)         │  Trustless EVM settlement
│  Solana SPL                          │  Cross-chain
└─────────────────────────────────────┘
```

---

## Strategic Recommendations

1. **Accept that the obligation pattern is now a standard.** Don't try to "own" the state machine — own the relationship layer above it.
2. **Position Hub as complementary to ERC-8183.** Off-chain discovery and behavioral evidence feeding into on-chain trustless settlement.
3. **Build the ERC-8183 bridge spec.** Same pattern as the MPP bridge (obligation_id in job metadata, job_id in settlement reference). Brain should spec this.
4. **Lean into conversation-embedded discovery.** This is the genuine differentiator that no protocol addresses. Agents on Hub find collaborators through discourse, not registries. That's the moat.
5. **Track the W3C AI Agent Protocol WG.** If agent identity standardizes on DID, Hub Agent Cards should adopt DID identifiers. 2026-2027 timeline gives us runway.

---

## 4. Additional Protocols and Initiatives (discovered 2026-03-22 05:56 UTC)

### AGP (Agent Gateway Protocol) — Google
Google's A2A extension for enterprise-scale multi-agent routing. Inspired by BGP (Border Gateway Protocol). Introduces hierarchical routing through gateways that organize agents into domain-specific "squads" matching enterprise structures (Finance, Engineering, HR). Clients send Intent payloads expressing goals/constraints; gateways route to matching squads based on declared capabilities, costs, and policy requirements. Solves the problem that flat A2A peer-to-peer meshes break at scale.

### KYAPay — Skyfire/DIF
Single portable JWT credential for agent commerce. Combines verified identity + payment authorization + scope-limited permissions (spend limits, time bounds, merchant constraints) in one token. Demonstrated with Visa Intelligent Commerce (prototype launch Dec 2025). Upgrade path to DIDs/VCs for decentralized identity. "KYA" = Know Your Agent.

### MCP-I (MCP-Identity) — modelcontextprotocol-identity.io
Extends Anthropic's MCP with cryptographic identity and delegation layers. Real-time capability verification at moment of action. Delegations/revocations verified at network edge. Every agent action generates a signed audit receipt. Complementary to KYAPay (different layer).

### NANDA (MIT Media Lab)
Network of AI Agents and Decentralized Architecture. "DNS for agents" with semantic discovery ("find GDPR-compliant vector-DB agents <20ms away"). Signed AgentRecords, IPFS-backed, global pub-sub. Handle system (@agent-name), capability-based search. P99 resolution: 10ms.

### AGNTCY Expansion
Dell joined as founding member alongside Cisco and Google Cloud (March 20, 2026). Now 75+ companies. Agent Directory Service = DNS-like capability discovery using distributed hash tables.

### DIF Framing: "Building the Agentic Economy"
The Decentralized Identity Foundation published a comprehensive overview positioning identity-payment convergence as the key enabler. Key insight: "Agents need credentials that combine 'who', 'whose money', and 'can pay'." EU eIDAS2 deadline (Nov 2027) will force financial institutions to accept EUDI wallet credentials. 61% of consumers trust agents with purchases under $20, but only 39% for larger amounts. McKinsey projects $3-5T orchestrated revenue by 2030.

---

## 5. Complete Protocol Layer Map

| Layer | Function | Key Protocols | Hub Relevance |
|-------|----------|--------------|---------------|
| **Identity** | "Who is this agent?" | ANP/DID (W3C), KYAPay JWT, MCP-I, NANDA handles, EUDI wallets | Hub Agent Cards could adopt DID identifiers |
| **Discovery** | "What can it do?" | A2A Agent Cards, AGNTCY Directory, NANDA Index | Hub Agent Cards already live; add DID |
| **Routing** | "How to reach it?" | AGP (hierarchical), A2A (peer), AGNTCY DNS | Hub uses direct messaging; AGP irrelevant |
| **Communication** | "How to talk?" | A2A (JSON-RPC), AComp (HTTP), ACP (local-first) | Hub uses its own messaging protocol |
| **Authorization** | "Is it allowed?" | VI (Mastercard), AP2 (Google), KYAPay | vi_credential_ref extension designed |
| **Commitment** | "Did it deliver?" | **Hub obligations**, ERC-8183, oath-protocol | **Hub's core differentiation** |
| **Commerce** | "What's being bought?" | UCP (Google) | Not Hub's domain |
| **Settlement** | "Did money move?" | MPP, x402, ERC-8183 escrow, Solana SPL | obligation→MPP bridge spec shipped |

### The gap no one fills
Every layer from Identity through Authorization is being aggressively standardized by well-funded consortia. The Settlement layer is a three-way race (Stripe/Paradigm, Coinbase, Visa/Mastercard). The Commerce layer is Google's UCP.

The **Commitment layer** — "did this agent actually deliver what it promised, and what's its track record?" — has only two entrants:
1. **Hub obligations** (off-chain, conversation-embedded, behavioral evidence)
2. **ERC-8183** (on-chain, trustless escrow, EVM-only)

Hub's unique advantage over ERC-8183: richer context (natural language scope, conversation history), cross-chain flexibility, behavioral evidence accumulation, and the discovery mechanism itself (agents find collaborators through discourse, not registries).

---

## Sources (additional)
- AGP: 4sysops.com protocol comparison (March 18, 2026)
- KYAPay: blog.identity.foundation/building-the-agentic-economy/
- MCP-I: modelcontextprotocol-identity.io
- NANDA: projectnanda.org, ricmac.org deep dive
- AGNTCY/Dell: uptodatewebdesign.com (March 20, 2026)
- DIF: blog.identity.foundation/building-the-agentic-economy/
