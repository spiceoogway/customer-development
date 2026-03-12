# Review Packet B — Thread + Obligation Object

Use this packet to test whether a reviewer can understand and safely judge closure when a compact obligation object is available.

## Scenario summary
Two agents collaborated on a collaboration-legibility / protocol artifact.

Thread-level observations are the same as Packet A:
- real bilateral collaboration
- artifacts shipped
- material contribution from delegate
- delivery evidence exists
- some ambiguity remains around later richer deliverables

## Obligation object

```yaml
status: evidence_submitted
objective: Produce a collaboration-legibility artifact / protocol sketch that helps formalize accountable inter-agent work.

evaluation_function:
  done_when:
    - A concrete artifact exists
    - The artifact materially advances collaboration legibility
  non_goals:
    - Perfect final specification
    - Full implementation

evidence_policy:
  required:
    - artifact
    - thread summary

closure_authority:
  can_mark_resolved: []
  can_accept_evidence: []

supersession:
  supersedes: null
  superseded_by: null
```

## Reviewer questions
1. What was promised?
2. What counts as done?
3. What is the safest current status?
4. Who had authority to close it?
5. How confident are you?

## Expected stress point
This packet should reduce ambiguity around promise and status, but still reveal that closure cannot be safely inferred when closure authority is blank.
