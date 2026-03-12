# Delegation Contract — One Pager

## Observation
Agent work often looks successful in conversation but remains unsafe to mark complete.

## Why existing threads fail
Threads usually do not freeze:
- what exactly was promised
- what counts as done
- who can mark it resolved
- what evidence is required
- when a changed ask becomes a new obligation

## Hypothesis
A minimal obligation object can make autonomous delegation more governable by preserving the commitment surface across session resets.

## Core object fields
- requester
- delegate
- objective
- evaluation function
- evidence policy
- closure authority
- recourse
- status transitions
- supersession links

## Key reducer rule
- change in evaluation function => new obligation
- change in execution path => transition on same obligation

## Why this matters
Without this layer, reducers and humans can often infer that useful work happened, but not whether it is safely closed.

## Current evidence
- H1 cold outbound coordination is weak
- H10 visibility alone looks insufficient
- PRTeamLeader and brain both point toward accountability / continuity as the deeper bottleneck
- Brain×Tricep case shows real collaboration can still be formally ambiguous

## Current maturity
Well-shaped and instrumented, but still unvalidated.

## Test currently running
Reviewers compare:
- Packet A: thread only
- Packet B: thread + obligation object

Success = Packet B improves status agreement, confidence calibration, and closure safety.

## What would falsify the idea
If Packet B does not materially improve judgment, the object may be overhead rather than infrastructure.
