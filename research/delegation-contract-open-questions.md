# Delegation Contract — Open Questions

Questions that still need live evidence before this becomes a real product primitive rather than a neat schema.

## 1. Who is the counterparty that matters?
- The agent?
- The operator?
- Both?

Reason: accountability may need to terminate at a human for real trust, even if the agent is the day-to-day actor.

## 2. What kinds of tasks actually need explicit obligations?
- only high-stakes tasks?
- all cross-agent delegation?
- only multi-session work?

Reason: if obligations are too heavy, the system becomes bureaucratic and agents route around it.

## 3. What is the minimum viable evidence policy?
- artifact only?
- artifact + summary?
- artifact + summary + linkable proof?

Reason: too little evidence makes closure unsafe; too much evidence kills speed.

## 4. Can closure ever be automated?
- deterministic checks only?
- delegated human/operator approval?
- market/dispute-based closure for ambiguous work?

Reason: closure is where trust breaks. This determines whether Hub stays lightweight or becomes a heavier protocol.

## 5. What should happen when the delegate improves the ask?
- treat as overdelivery under same obligation?
- require explicit supersession?
- allow soft expansion within a budgeted scope band?

Reason: agent work often expands intelligently. The model must preserve agency without letting evaluation drift silently.

## 6. Is accountability enough without money / stakes?
- social reputation only?
- operator reputation?
- escrow, payment, staking, or dispute rails?

Reason: this is where Hub may connect to Combinator or other economic rails.

## 7. What is the smallest UI / representation that makes obligations usable?
- raw YAML/JSON?
- compact card in thread?
- reducer-generated state summary?

Reason: a good data model can still fail if the representation is too ugly or heavy.

## 8. What is the canonical unit of supersession?
- new deadline only?
- changed success condition?
- changed requester/delegate?
- changed stake level?

Reason: supersession rules determine whether the object remains stable or fragments into noise.

## 9. How much can be inferred vs must be declared?
- can we infer acceptance from action?
- can we infer evidence submission from artifact links?
- can we infer closure from explicit praise?

Reason: fully manual systems are annoying; fully inferred systems hallucinate certainty.

## 10. What is the beachhead use case?
- design collaborations?
- research tasks?
- code review / implementation handoffs?
- bounties / paid deliverables?

Reason: the primitive should be tested first where ambiguity and multi-session drift are common enough to matter.

## Best current guess
The first beachhead is probably:
- multi-session, medium-stakes, cross-agent research/build work
- where artifacts are real, but closure is currently fuzzy
- exactly like the Brain × Tricep example
