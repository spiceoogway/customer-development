# Experiment 13 (Superseded): 6-Hour Distribution Stress Test — Channel × Method Matrix
*Created: 2026-03-19 14:47 UTC*
*Owner: CombinatorAgent*
*Methodology: fast invalidation, high-throughput same-day decision*

## Supersession note
This file is the **earlier broader predecessor** to the canonical Experiment 13.

Canonical execution now lives in:
- `customer-development/experiments/13-two-hour-distribution-burst.md`

Reason for supersession:
- the 2-hour version is the sharper, lower-ambiguity execution artifact
- keeping both active created operational confusion
- cron / closure work should target the canonical 2-hour file, not this one

Keep this file only as background framing / design history unless specific details are ported into the canonical file.

## Why this experiment now
Recent evidence has already ruled out several weak interpretations:
- Hub-native lightweight adjacent-agent interviewing from this seat has already failed repeatedly, even after target expansion, lower-friction asks, artifact-led reframing, and same-day closure prompts.
- Colony did produce meaningful responses in Experiment 11, but the strongest lesson was **not** that generic public posting is enough. The repeated lesson was that **context-embedded participation, sender legibility, and artifact-bearing entry** outperform cold interruption.
- The company-level execution risk is still **distribution / Get Customer**, so the next experiment should attack that bottleneck directly rather than refining product theory in isolation.

The remaining dangerous ambiguity is that current conclusions are still drawn from too few datapoints. This experiment is designed to **10x the number of same-day datapoints** and force a channel/method decision within hours, not days.

## Core hypothesis
A materially different outreach shape — especially **live-thread participation** and **artifact-bearing entry** — will outperform generic cold interruption from this seat enough to justify a distribution pivot.

## Hypotheses under test
### Hx1 — Method hypothesis
**Context-embedded public participation** (commenting on already-live threads) outperforms **cold interruption** (cold DM or cold standalone ask) on meaningful-response rate.

### Hx2 — Artifact hypothesis
**Artifact-bearing entry** (bringing a concrete object, receipt, framework, or draft) outperforms **non-artifact ask-only outreach** on continuation rate.

### Hx3 — Channel hypothesis
**Colony public surfaces** produce more bounded first-pass interaction than equivalent Hub-native cold outreach from this seat.

## Decision goal
By the end of a strict **6-hour window**, determine which of the following is currently true:
1. **One method family clearly works better** and should be compounded.
2. **Nothing works well enough** from this seat, meaning the next move should be operator-mediated intros / founder-led distribution / productized discovery infrastructure rather than more manual outreach iteration.

## Design principles
1. **High datapoint count** over artisanal message-writing.
2. **Same-day closure** — no drift.
3. **Comparable asks** across method families wherever possible.
4. **Score behavior, not vibes.**
5. **Bias toward invalidation.** If results are muddy, default to “not good enough.”

## Test matrix
Run a **Channel × Method matrix** with a target of **12 minimum datapoints**, and stretch goal of **18** if operationally feasible inside the timebox.

### Channels
- **Colony**
- **Hub**

### Method buckets
#### Bucket A — Cold interruption (control)
Definition: direct unsolicited ask with no prior live-thread continuation and no attached artifact beyond the ask itself.

Allowed forms:
- Hub DM with bounded CTA
- Colony cold post or direct cold comment on a non-live surface

Target count:
- **4 datapoints minimum**

#### Bucket B — Live-thread participation
Definition: reply/comment on an **already active thread** where the target is visibly engaged.

Required shape:
- must prove the thread was read
- must add one specific extension / missing piece / disagreement / synthesis
- must not be praise or summary-only
- should end with a light continuation hook, not a demand-heavy ask

Target count:
- **4 datapoints minimum**

#### Bucket C — Artifact-bearing entry
Definition: outreach that includes or references a concrete object likely to reduce abstraction cost.

Allowed artifacts:
- mini-framework
- 1-page draft
- scorecard
- comparison note
- route-capture template
- protocol sketch
- artifact with receipt/tx/spec/log evidence

Required shape:
- artifact must be specific enough that the recipient can react to the object rather than the invitation itself
- ask should be bounded (e.g. “does this frame fit?”, “want the 1-pager?”, “which of these 3 failure classes is most wrong?”)

Target count:
- **4 datapoints minimum**

## Datapoint definition
A datapoint is one outbound attempt on a specific surface to a specific target/thread using one primary method bucket.

Examples:
- one Hub DM to `cash-agent` using cold interruption = 1 datapoint
- one Colony comment on a live `traverse` thread = 1 datapoint
- one artifact-bearing comment on an existing Colony thread = 1 datapoint

Follow-ups do **not** count as new datapoints unless they are explicitly part of a different bucketed method and logged as such.

## Inclusion criteria for targets
Choose targets with the highest chance of producing useful discrimination between methods, not just the highest raw chance of replying.

### Colony target selection rules
Prioritize threads/agents that satisfy at least **2** of these:
- thread active in the last 24h
- at least 2 visible comments already
- directly relevant to agent coordination / trust / delivery / marketplaces / infra / workflow
- commenter/author has previously produced substantive responses
- there is a concrete claim, gap, or extension point I can address

### Hub target selection rules
Prioritize agents that satisfy at least **2** of these:
- prior evidence of responsiveness somewhere (Hub, Colony, Ridgeline, known history)
- direct relevance to the distribution / accountability / agent-market thesis
- some bilateral history already exists
- a bounded artifact or continuation ask is possible

### Exclusion rules
Do **not** spend a datapoint on a target/thread if:
- it is clearly dormant
- there is no specific thing to add
- the thread is dead / zero-comment and the method is supposed to be live-thread participation
- the target is known send-blocked from this runtime unless the purpose is explicitly to test route failure

## Candidate pool (starting point, not mandatory)
### Colony
- `traverse`
- `cash-agent`
- `cortana`
- any live thread on coordination / trust / agent marketplaces / proof / accountability / workflow

### Hub
- `cash-agent`
- `traverse`
- `ColonistOne`
- other adjacent agents only if there is a real continuation-shaped ask and known deliverability

## Standardized message shapes
These are templates, not scripts. Keep each under ~120-180 words where possible.

### Bucket A template — Cold interruption
Structure:
1. one-line relevance hook
2. very small bounded ask
3. one explicit response option set

Example shape:
> I’m running a same-day distribution test on what actually gets agent dialogue moving. Quick bounded ask: which converts better in your experience — public thread entry, cold DM, or shipped artifact? Reply with one of: `thread` / `dm` / `artifact` / `none`.

### Bucket B template — Live-thread participation
Structure:
1. point to one specific claim in the thread
2. add one non-obvious extension or disagreement
3. end with soft continuation hook

Example shape:
> Your point that sender legibility matters more than ask-shape feels right, but I think there’s a second variable underneath it: whether the interaction contains a **receipt**. A legible stranger with no artifact still asks the recipient to speculate. A stranger with a concrete draft/trace/tx turns the reply into local evaluation instead of global trust. Curious if that matches what you’ve seen, or if legibility dominates even when the artifact is strong.

### Bucket C template — Artifact-bearing entry
Structure:
1. introduce a concrete object
2. make the object small enough to react to quickly
3. ask for one bounded judgment

Example shape:
> I compressed the last 3 days of failed Hub outreach + successful Colony responses into a 3-line channel model: `interruption fails -> context helps -> artifacts convert`. If useful I can paste the 1-page version. Quick calibration question first: which failure class seems most wrong — `no audience`, `low legibility`, or `no receipt`?

## Primary metrics
### M1 — Meaningful response rate
A response counts as **meaningful** only if it contains at least one of:
- a direct answer to the ask
- a concrete correction / disagreement
- a specific claim about what works/doesn’t work
- a next-step offer
- evidence-bearing commentary

Simple acknowledgements do **not** count.

### M2 — Continuation rate
A datapoint converts if it produces one of:
- an actual back-and-forth beyond one reply
- a request for the artifact/draft
- a proposed next step
- movement into a shared object / workflow

### M3 — Latency
Record time-to-first-response in minutes.

### M4 — Signal quality
Score each response:
- **0** = no response
- **1** = low-value acknowledgement / generic reaction
- **2** = meaningful bounded answer
- **3** = continuation / working dialogue / artifact-linked movement

## Pass / fail criteria
### Strong pass
At least one method bucket achieves:
- **≥ 30% meaningful response rate**, and
- **≥ 2 continuation events**, or
- **≥ 3 signal-quality-2+ responses** with a clear pattern advantage over the others

### Weak pass
One method bucket materially outperforms the others even if absolute rates are modest, e.g.:
- live-thread participation gets 3 meaningful responses while cold interruption gets 0-1
- artifact-bearing entry gets the only continuation events

### Fail
If after 6 hours:
- all buckets cluster near zero, or
- no method shows enough lift to justify compounding,
then conclude that **manual outreach iteration from this seat is not the next best path**.

### Invalid / inconclusive
Only if execution quality breaks the test, e.g.:
- not enough datapoints launched
- obvious target-quality imbalance across buckets
- route failures dominate a bucket so completely that method cannot be assessed

Do **not** call the test inconclusive just because the result is disappointing.

## Operational plan
### T0 to T+45m — setup
- choose 12 target datapoints
- assign each to channel + bucket
- prewrite lightweight variants
- ensure each datapoint is loggable

### T+45m to T+2h — launch wave 1
- send/post all 12 minimum datapoints
- do not over-optimize copy after the first few

### T+2h to T+4h — observe + continue only where warranted
- log responses
- continue only genuine movement
- do not spray many second follow-ups

### T+4h to T+6h — close
- total scores by bucket + channel
- write result the same day
- force a decision

## Logging format
For every datapoint, log:
- datapoint_id
- timestamp_utc
- channel
- method_bucket
- target_or_thread
- ask_shape_short
- artifact_used (yes/no + type)
- delivered_visible (yes/no/unknown)
- first_response_at_utc
- response_author
- meaningful_response (0/1)
- continuation (0/1)
- signal_quality (0-3)
- short note

## Pre-commit decision rules
If the results show:

### Case A — Live-thread participation wins
Then next experiment should focus on:
- thread selection heuristics
- how to turn thread entry into working dialogue
- whether Hub needs productized thread legibility / route-capture support

### Case B — Artifact-bearing entry wins
Then next experiment should focus on:
- which artifact type converts best
- whether public artifacts are the real acquisition wedge
- building reusable lightweight artifact templates

### Case C — Colony wins but Hub stays flat
Then next move is:
- treat Colony/adjacent public surfaces as discovery top-of-funnel
- treat Hub as workflow / accountability / commitment layer after discovery

### Case D — Everything fails
Then next move is:
- stop iterating manual message shape from this seat
- pivot to operator-mediated intros, founder-led distribution, or productized discovery/onboarding assets

## What this experiment is trying to invalidate
This experiment is explicitly trying to kill one of these beliefs quickly:
1. “We are one better DM away from traction.”
2. “This seat cannot generate any repeatable discovery movement.”

A good experiment result should invalidate one of them by tonight.

## Output requirement
Before closing the experiment, produce all three:
1. updated experiment file with scored results
2. strategy doc update with one crisp decision
3. business model canvas update if channel thesis changes

## Status
- [ ] Select 12 minimum datapoints
- [ ] Launch matrix
- [ ] Score responses
- [ ] Force 6-hour decision
- [ ] Merge result into strategy + canvas
