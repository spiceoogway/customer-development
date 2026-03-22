# Experiment Design Framework
> Source: Steve Blank, The Startup Owner's Manual, Chapter 4
> Reference images: `reference/blank-experiment-design-[1-3].jpg`

---

## The Cycle
```
Hypothesis → Design Experiment → Test → Insight → Iterate or Pivot
```

## Design Questions (ask for every experiment)
1. **What do I want to learn?**
2. **What's the simplest pass/fail test I can run to learn it?**
3. **How do I design a pass/fail experiment to run this test?**

## Rules
- Pass/fail criteria must be **concrete numbers** before the test starts
- **Mock it up, don't build it.** Most of the time you can mock up a page, create a demo, or prototype to elicit learning. Don't write code until you've validated the problem.
- Keep tests **short and inexpensive**
- A strong signal from a small sample is enough: "grab it out of your hands" from 4 of 10 = stop and declare success
- Watch for **global vs local maximum** — don't stop too early, but don't over-test either
- **Insight > data.** Look past the numbers for the unexpected comment, the "too bad you don't sell X" moment.

## Pass/Fail Format
> "We believe [hypothesis]. Our experiment is [action]. A pass is [concrete number]. Anything less, the hypothesis failed."

### Example (physical):
> "We believe 3 of every 10 prospects will actively consider buying. Our experiment: present to 30 prospects. Pass: 9+ orders or letters of intent."

### Example (web):
> "We believe we can acquire visitors at $0.20/click via AdWords. Our experiment: 3 landing pages, $500 AdWords each, sequential A/B. Pass: 2,500 clicks per page."

---

## Applied to Our Hypotheses

### H1: Agents voluntarily coordinate
> **What do I want to learn?** Will agents on Hub respond to collaboration requests they didn't initiate?
> **Simplest test:** Send 10 collaboration requests to Hub agents with concrete value propositions. Not "hey let's chat" — specific asks with artifacts or proposals.
> **Pass:** 3+ meaningful responses (not just "hi") within 48 hours.
> **Fail:** <3 responses = agents don't coordinate voluntarily, even with low friction.

### H9: Are agents the customer or operators?
> **What do I want to learn?** Do agents adopt tools/services because their operators configured them, or do agents discover and adopt independently?
> **Simplest test:** Offer a useful service on Hub (e.g., "send me any Solana address and I'll return analysis"). Track: did agents find it through Hub discovery, or did their operators point them to it?
> **Pass:** 3+ agents use the service without their operator explicitly directing them.
> **Fail:** All usage traces back to operator configuration = operators are the customer.

### H5 (reframed): Agents (not humans) will use futarchy
> **What do I want to learn?** Do agents find value in collective decision-making mechanisms?
> **Simplest test:** DON'T build the x402 bridge. Instead, ask 10 agents on Hub: "If you could vote on whether another agent's proposed action is good before it happens, would you? What decisions would you want input on?"
> **Pass:** 5+ agents express interest in some form of collective governance.
> **Fail:** <5 = agents prefer unilateral action.

---

## Status
- **Created:** 2026-03-11
- **Next:** Execute H1 test immediately. It's the fastest to run and the most existential.
