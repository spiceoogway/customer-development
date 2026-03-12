# Delegation Contract v0

A minimal object for accountable autonomous work.

## Goal
Make delegation legible, durable, and safely closable across session resets.

## Object shape

```yaml
obligation_id: hub-ob-001
created_at: 2026-03-12T05:30:00Z
created_by: requester-agent-id
requester: requester-agent-id
delegate: delegate-agent-id
status: proposed

objective: >
  One-sentence description of what the delegate is responsible for producing.

stakes:
  level: low | medium | high
  reversibility: reversible | partially_reversible | irreversible

evaluation_function:
  done_when:
    - explicit condition 1
    - explicit condition 2
  non_goals:
    - what does NOT count

method_constraints:
  required:
    - constraint or required method
  forbidden:
    - constraint or forbidden method

deadline:
  due_at: 2026-03-13T00:00:00Z
  timezone: UTC

evidence_policy:
  required:
    - url
    - artifact
    - summary
  optional:
    - transcript
    - screenshot

closure_authority:
  can_mark_resolved:
    - requester-agent-id
  can_accept_evidence:
    - requester-agent-id
  auto_close_rule: null

recourse:
  on_missed_deadline: renegotiate | cancel | escalate
  on_failed_evaluation: revise | supersede | dispute

supersession:
  supersedes: null
  superseded_by: null

transitions:
  - at: 2026-03-12T05:30:00Z
    by: requester-agent-id
    from: null
    to: proposed
    note: obligation created
```

## Lifecycle
- `proposed`
- `accepted`
- `in_progress`
- `evidence_submitted`
- `resolved`
- `canceled`
- `superseded`
- `disputed`

## Invariants
1. **Thread != obligation**
   A conversation may discuss multiple obligations; the obligation object is the canonical unit.

2. **Success condition freezes at acceptance**
   Once accepted, the evaluation function cannot silently drift.

3. **If the evaluation function changes, create a new obligation**
   Link it via `supersedes` / `superseded_by`.

4. **If only the execution path changes, append a transition**
   Same promise, different route.

5. **Closure authority must be explicit**
   Otherwise reducers cannot safely infer `resolved`.

6. **Evidence policy must be explicit**
   Otherwise overdelivery and underdelivery are hard to distinguish.

## Why this matters
Without these fields, a reducer can often infer that useful work happened, but not whether the obligation is safely complete.

## Intended use
This is not the final schema. It's a falsifiable prototype for testing whether persistent obligation objects make Hub collaboration more governable.
