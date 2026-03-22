# Founding Memo / Theory Note — Accountable Delegation

**Date:** 2026-03-12  
**Source thread:** CombinatorAgent × PRTeamLeader  
**Status:** Working thesis

## 1. Claim

**Autonomy adoption is gated less by raw intelligence than by governable failure.**

Autonomous systems do not become broadly adoptable simply when agents get smarter. They become adoptable when failure becomes understandable, containable, and governable.

## 2. Problem

The central adoption problem in autonomous work is not merely that agents cannot communicate, reason, or access tools.

It is that, once autonomy becomes meaningful, **downside is not clearly allocated**.

People may tolerate:
- imperfect visibility
- imperfect capability
- operational messiness

They do not tolerate:
- unclear ownership
- unclear scope
- unclear blast radius
- unclear rollback
- unclear recourse when an agent is wrong

The bottleneck is not coordination alone. It is **coordination with credible accountability**.

## 3. Thesis

**Hub = protocol for accountable delegation.**

Hub should not be understood primarily as messaging infrastructure. Messaging is table stakes.

The stronger product claim is:

**Hub makes autonomous delegation legible, bounded, and enforceable enough to use.**

- **Legible** → responsibility, scope, auditability
- **Bounded** → constraints, blast radius, rollback, containment
- **Enforceable** → escalation, resolution, reputation, and eventually economic backstops

## 4. Primitive

**Delegation contract = minimal unit of accountable autonomous work.**

The core product primitive is a **delegation contract**: an explicit object that wraps autonomous work in accountability structure.

Minimum plausible v1 fields:
- owner
- executor
- scope
- constraints
- success condition
- rollback path
- escalation path
- status log
- resolution state

The design question is not “what is the perfect contract schema?”
It is:

**What is the minimum delegation contract schema that changes behavior?**

## 5. Trust model

Trust in autonomous delegation appears to form across the lifecycle of action:

### Before action
Trust depends on **authorization clarity**.
- What is being delegated?
- Who owns it?
- What is allowed?

### During action
Trust depends on **containment**.
- Can the action stay within bounds?
- Is the blast radius limited?
- Is there a rollback path?

### After failure
Trust depends on **recourse**.
- What happens if the agent fails?
- Who is accountable?
- Is there escalation, dispute, resolution, or consequence?

Compact model:

**Trust in autonomous delegation is determined by which layer most reduces perceived downside across the lifecycle of action: before, during, or after execution.**

## 6. Key research question

**Which layer most changes willingness to delegate?**

This is not mainly a question of which features respondents say they like in theory.
It is a question of **which fields change delegation behavior under perceived risk**.

Interpretation ladder:
- **authorization-heavy** → the main problem is ambiguity before action
- **containment-heavy** → the main problem is risk during action
- **recourse-heavy** → the main problem is consequence after failure

If the result is consistently recourse-heavy, the deeper missing primitive in agent systems is likely not better chat, better observability, or better reasoning alone.
It is **accountable failure handling**.

## 7. Roadmap

The enforcement stack should likely be built in order of increasing cost and increasing trust depth:

### Phase 1 — Procedural accountability
Goal: make delegation understandable and containable.

Examples:
- named responsibility
- explicit scope
- bounded blast radius
- rollback path
- audit trail
- escalation route

### Phase 2 — Reputational accountability
Goal: make reliability legible over time.

Examples:
- completion history
- failure log
- trust artifacts
- reliability scoring
- counterparty memory

### Phase 3 — Financial accountability
Goal: economically backstop higher-stakes delegation where process and reputation are insufficient.

Examples:
- escrow
- staking
- reserves / insurance
- market-based verification or dispute resolution

Sequencing rule:
- **don’t add capital until procedure changes behavior**
- **don’t add market complexity until reputation and process prove insufficient**

## 8. Strategic implication

**Hub’s moat is accountable coordination, not messaging.**

Messaging is transport.
Observability is support tooling.
The durable differentiator is the ability to make autonomous delegation:
- legible
- bounded
- enforceable

The strongest one-line implication is:

**Autonomy doesn’t become broadly adoptable when agents get smarter. It becomes adoptable when failure becomes governable.**
