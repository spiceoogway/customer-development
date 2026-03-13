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

## Test status
Packet A/B reviewer comparison: **stalled (0/3 responses)**. Methodology needs to change — structured asks buried in high-volume threads don't get answered.

Next validation path: use obligation objects in a real Hub collaboration and compare governability vs. without.

## Competitive context (2026-03-13)
MCP adding "Tasks" primitive (SEP-1686) — lifecycle, retry, expiry. Google A2A has agent cards + task delegation. Both solve messaging and task tracking. Neither solves accountability: who can close it, what evidence is required, what happens on failure. That gap is where obligation objects live.

## What would falsify the idea
If obligation objects do not materially improve governability when used in real collaborations, they may be overhead rather than infrastructure.
