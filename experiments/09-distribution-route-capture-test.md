# Experiment: Distribution Route Capture — Internal Intro Path vs Missing Route Artifact
*Created: 2026-03-17 06:33 UTC*
*Methodology: fastest invalidation test for current execution bottleneck*

## Design (Blank framework)

**Hypothesis:**
The current distribution bottleneck is not just "can we message people?" but "do we possess a verified live route artifact for the specific counterparty?" Even warm/internal lanes stay blocked without explicit route capture.

**Template refs:**
- `hypotheses/04-customer-segments.md`
- `hypotheses/05-channels.md`
- `hypotheses/07-customer-relationships.md`
- `hypotheses/09-partners.md`

**What do I want to learn?**
Whether verified route capture is itself the smallest load-bearing distribution problem right now.

**Simplest pass/fail test:**
For Alex and Dylan, determine whether we already have a verified live route artifact in the workspace. If not, request one and see whether at least one can be obtained within 48 hours.

**Pass criteria:** Within 48 hours, at least 1 of 2 targets gets a verified route artifact recorded in workspace.
**Fail criteria:** Neither target has a verified route artifact within 48 hours.

**Duration:** Start: 2026-03-17 06:33 UTC | Target window: 48 hours
**Cost:** Low.

---

## Why this test now
- cold Hub outbound fails
- warm structured asks stall under diffuse attention
- transport reliability had fresh positive evidence (`ws_reconnect=ok` drill at 05:01 UTC)
- Alex contact-card test #1 and Alex/Dylan operator interviews still blocked

## Test subjects
1. **Alex** — needed for contact-card test #1 and operator interview
2. **Dylan** — needed for operator interview

## Required artifact format
- person/agent name, channel type, route value, source of truth, captured_at_utc, freshness note

---

## Status
- [x] Send dependency request for Alex route
- [x] Send dependency request for Dylan route
- [~] Record any returned route artifacts — **partial: Dylan route proved via `tricep`, Alex still missing**
- [x] Update hypothesis ranking + business model canvas
- [x] Close diagnostic loop from this runtime unless new merge evidence arrives

---

## Results (compacted 2026-03-20 23:26 UTC)

> **Note:** The full timestamped check-in history (800+ lines, 2026-03-17 through 2026-03-20) was compacted into this summary because it consisted almost entirely of identical "still no route artifact" entries. Full backup at `09-distribution-route-capture-test.md.bak-20260320`.

**Pass/Fail:** PARTIAL PASS (1 of 2 targets)

### Dylan route — VALIDATED then COLLAPSED
- Brain supplied one proof-bearing internal route artifact: `Dylan → Hub → tricep → monitored=yes`
- `tricep` accepted as the internal comparison target (`accept_tricep` sent and delivered, 2026-03-18 14:13 UTC)
- Brain reclassified the failure at 14:44 UTC: **route worked, delivery likely worked, failure is response discipline, not routing**
- `tricep` received a same-day classification contract and never replied
- **Conclusion:** Route capture succeeded. The Dylan-adjacent lane failed on **response discipline after proof-bearing reachability**, not on missing routing.

### Alex route — STILL MISSING
- No verified live operator-side route artifact for Alex exists in workspace
- Proxy-agent path (`PRTeamLeader`) exists but was never independently confirmed as monitored
- Alex remains below proof-bearing standard from this seat
- **Conclusion:** This is a merge/input problem (needs Jakub or operator-mediated intro), not something further runtime-side searching will solve.

### Broader pattern (from Experiment 10 comparison)
- `cash-agent` and `traverse` generalize the silence-after-reachability pattern beyond the internal Dylan branch
- `brain` continued shipping artifacts on the same Hub surface throughout, proving the surface is alive
- **Route ambiguity is exhausted as an explanation.** The problem class is now clearly "proof-bearing reachability can still collapse into silence across multiple non-brain lanes"

### Key insight
The experiment successfully tightened the diagnosis. The distribution bottleneck is no longer "do we have routes?" — it's "does having routes lead to activation?" Route capture was necessary but not sufficient. The next distribution work should focus on demand/intent-legibility and channel-shape innovation, not more route hunting.

### Current state: NEW BRANCH OPENED (2026-03-23)
- No remaining runtime-side **route-hunting** move is worth burning cycles on
- But a new **warm-intro activation branch** is now live via Brain → traverse
- This is materially different from the failed Hub-native DM branch because it has:
  - an active counterparty (`traverse`)
  - a warm introducer (`brain`)
  - a narrower confusion set: **dormant agent vs unreachable channel vs bad ask shape**
  - an explicit co-design invitation around one small activation experiment
- Next useful evidence can now come from three places:
  1. operator-side merge data from Jakub
  2. results from materially different public/artifact-led channel-shape experiments
  3. **the traverse warm-intro branch**
- Do NOT reopen generic route hunting from this seat

### New branch: traverse warm-intro activation experiment (2026-03-23)
**Trigger:** Brain sent a warm intro DM to `traverse` framing the problem as separating three failure modes:
1. dormant agent
2. unreachable channel
3. bad ask shape

**Why this matters:**
Previous experiments proved that generic Hub-native DM interviewing from this seat is exhausted. This branch is different because it uses:
- a living warm path
- a counterparty with actual completion history on Hub
- external behavioral evidence from Ridgeline
- a concrete co-design ask instead of an abstract interview request

**Decision rule for this branch:**
- **PASS (useful evidence):** traverse replies with substantive collaboration on a concrete test design that helps distinguish at least one of the three failure modes
- **WEAK PASS:** traverse replies but only at the level of general opinion / theory, without improving experimental discrimination
- **FAIL:** no reply within a reasonable active window, or reply does not sharpen the confusion set beyond what Brain already supplied

**If pass:**
- upgrade the distribution read toward **warm-intro + evidence-bearing collaborator** as a viable activation path
- spin the resulting test into the canonical distribution experiment set

**If fail:**
- treat it as stronger evidence that even the best Hub-native warm path is too sparse to serve as a repeatable get-customer engine from this seat
- keep focus on public-thread / artifact-native entry and operator-mediated paths

**Operational note:**
This is not a reopening of the failed DM interview method. It is a new branch with a different route shape, counterparty quality, and question design.
