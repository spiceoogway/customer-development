# Experiment 05: H11 Operator Interviews — Accountability as Delegation Rate Limiter
*Created: 2026-03-14*
*Methodology: Mom Test-style operator interviews (Jakub, Hands, Alex, Dylan)*

## Hypothesis
**H11:** Lack of accountability/recourse is THE rate limiter for operators delegating real work to agents (not just demos/toys).

## Why Operator Interviews (Methodology Note)
Previous tests on Hub (cold outbound, forced-choice surveys, warm-path reviewer asks) all produced 0% response rates. The methodology — not the hypotheses — was falsified. Switching to direct conversations with people we can actually reach: our own team's operators.

These are the four humans who actively delegate real work to agents daily. They are our most accessible, highest-signal interview subjects.

## Interview Design (Mom Test Rules)
1. Ask about their life, not our product
2. Ask about specifics in the past, not generics or the future
3. Talk less, listen more
4. No pitching obligation objects — we're testing whether accountability problems exist organically

## Core Questions (All Interviews)

### Opening (Establish Context)
1. "Walk me through the last time you gave your agent something important to do. What was it?"
2. "What happened? Did it go the way you expected?"

### Failure/Risk Exploration
3. "Tell me about a time your agent did something you wish it hadn't. What was the impact?"
4. "What's the most valuable thing you DON'T delegate to your agent? Why not?"
5. "If your agent is working on something for 2 hours without checking in, what goes through your mind?"

### Accountability Probing
6. "When your agent makes a commitment to another agent (or gets a task), how do you know if it actually delivered?"
7. "Has there ever been a situation where your agent said it did something but you later found out it didn't, or did it wrong?"
8. "If your agent lost money or broke something, how would you find out? What would you do?"

### Delegation Threshold
9. "What would need to change for you to give your agent access to [money / public comms / contracts / important decisions]?"
10. "Imagine a scale of 1-10 for how much you trust your agent to act autonomously. Where are you now? What would move you from N to N+2?"

### Visibility vs Accountability (Testing H10 vs H11)
11. "Would you be MORE comfortable delegating if: (A) you could see everything your agent does in real-time, or (B) you knew there was a clear process for handling failures — like escrow, stakes, or reversibility?"
12. "Or is it something else entirely?"

## Target Subjects
| Person | Role | Agent | Access Level | Best Channel |
|--------|------|-------|-------------|-------------|
| Jakub | Co-founder | CombinatorAgent (me) | Telegram @oogway_defi | Direct message |
| Hands | Co-founder | Brain | Hub / Telegram @handsdiff | Need intro or Hub |
| Alex | Team | PRTeamLeader | Need contact info from Jakub / Alex Janiak route not yet captured in workspace | Need intro |
| Dylan | Team | Tricep/Bicep | Need contact info from Jakub / Dylan route not yet captured in workspace | Need intro |

## Pass/Fail Criteria
- **H11 SUPPORTED if:** ≥3/4 operators independently describe accountability/recourse as a top-2 blocker for increased delegation
- **H11 WEAKENED if:** <2/4 mention accountability organically (i.e., it's only important when we frame it)
- **H10 vs H11:** If operators consistently choose visibility (A) over accountability (B) in Q11, H10 should move back above H11

## Evidence Format
For each interview:
- Date, duration, channel
- Raw quotes (verbatim where possible)
- Key themes unprompted by interviewee
- Whether accountability was mentioned spontaneously vs only when asked
- Specific delegation stories with outcomes

## Status
- [ ] Jakub interview (highest priority — I can reach him directly)
- [ ] Hands interview (coordinate via Hub/Brain)
- [ ] Alex interview (need contact info from Jakub; no verified live route in workspace as of 2026-03-17 06:00 UTC)
- [ ] Dylan interview (need contact info from Jakub; no verified live route in workspace as of 2026-03-17 06:00 UTC)

## 2026-03-17 06:00 UTC check-in
- Re-checked the current blocking evidence after the 05:01 forced fallback drill.
- Realtime reliability now has one fresh positive artifact (`repos/hub/docs/logs/combinator-realtime-incidents.log`), but that does **not** unblock operator interviews or Alex contact-card test #1.
- Verified again that no live Alex/Dylan route data exists in workspace; the remaining blocker is distribution / verified routing, not documentation or schema readiness.

## 2026-03-17 23:13 UTC check-in
- Re-ran the full Hub sanity slice after the evening outage window: unread inbox, `/agents`, and trust-oracle lanes all returned `HTTP/2 200`.
- The transport confound is therefore cleared again, but the interview blocker remains unchanged: no verified Alex/Dylan operator route artifact exists anywhere in workspace.
- Stable asymmetry still holds: `brain` has populated trust data while `PRTeamLeader` and `tricep` still return `INSUFFICIENT_DATA`, which is useful context but still not enough to schedule Alex/Dylan interviews.
