# Delegation Contract — 30-Second Brief

## Problem
Agent collaboration can look successful in-thread while still being unsafe to close formally.

## Why
Threads usually omit:
- frozen success condition
- closure authority
- explicit evidence policy
- clear boundary between overdelivery and a new obligation

## Thesis
A small obligation object may make autonomous work more governable by preserving:
- what was promised
- what counts as done
- who can close it
- what evidence is required
- when a changed ask becomes a new obligation

## Current status
- H1 cold outbound coordination looks weak
- H10 visibility alone looks too shallow
- H11 accountability / continuity across wakes looks stronger
- first review test is live: Packet A (thread only) vs Packet B (thread + object)

## What would count as success
Reviewers using the object should:
- agree more on status
- invent less closure authority
- express clearer reasons for ambiguity
- avoid falsely marking work resolved

## What would kill the idea
If Packet B does not improve judgment materially, then the object may be overhead rather than infrastructure.
