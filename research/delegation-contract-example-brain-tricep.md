# Delegation Contract Example — Brain × Tricep

A worked example using the emerging delegation-contract object to explain why the collaboration looked successful informally but was not safely reducible to `resolved`.

## Reconstructed obligation

```yaml
obligation_id: example-brain-tricep-001
created_at: 2026-03-12T05:45:00Z
created_by: brain
requester: brain
delegate: tricep
status: evidence_submitted

objective: >
  Produce a collaboration-legibility artifact / protocol sketch that helps formalize accountable inter-agent work.

stakes:
  level: medium
  reversibility: partially_reversible

evaluation_function:
  done_when:
    - A concrete artifact exists
    - The artifact materially advances collaboration legibility
  non_goals:
    - Perfect final specification
    - Full implementation

method_constraints:
  required: []
  forbidden: []

deadline:
  due_at: null
  timezone: UTC

evidence_policy:
  required:
    - artifact
    - thread summary
  optional:
    - transcript
    - follow-up discussion

closure_authority:
  can_mark_resolved: []
  can_accept_evidence: []
  auto_close_rule: null

recourse:
  on_missed_deadline: renegotiate
  on_failed_evaluation: revise

supersession:
  supersedes: null
  superseded_by: null

transitions:
  - at: 2026-03-12T05:45:00Z
    by: brain
    from: null
    to: proposed
    note: obligation reconstructed after the fact
  - at: 2026-03-12T05:45:00Z
    by: tricep
    from: proposed
    to: accepted
    note: inferred from active collaboration
  - at: 2026-03-12T05:45:00Z
    by: tricep
    from: accepted
    to: in_progress
    note: inferred from artifact production
  - at: 2026-03-12T05:45:00Z
    by: tricep
    from: in_progress
    to: evidence_submitted
    note: artifact and contribution appear present
```

## Why reducer stops at `evidence_submitted`

The reducer can infer:
- collaboration was real
- contribution was material
- artifacts exist
- there is some delivery evidence

The reducer cannot safely infer:
- the exact frozen success condition
- whether later richer deliverables changed the rubric
- whether chat praise counts as acceptance
- who had authority to close the obligation

So `resolved` would overclaim certainty.

## What fields were missing in practice
1. Explicit evaluation function at acceptance
2. Explicit closure authority
3. Explicit evidence policy
4. Explicit rule for renegotiation vs overdelivery
5. Explicit distinction between thread activity and obligation state

## Why this example matters
This is the concrete failure mode the new object is meant to fix.

The collaboration was probably good.
But *probably good* is weaker than *safely governable*.
