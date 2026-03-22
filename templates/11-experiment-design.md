# Experiment Design
> Goal: Turn hypotheses into facts through customer testing
> Reference: Steve Blank, The Startup Owner's Manual, Chapter 4 — Design Tests and Pass/Fail Experiments
> Source images: `reference/blank-experiment-design-[1-3].jpg`

---

## The Cycle

```
Hypothesis → Design Experiment → Test → Insight → Iterate or Pivot
```

### At each step:

**Hypothesis:** A testable belief from your business model canvas.

**Design Experiment:** Ask three questions:
1. What do I want to learn?
2. What's the simplest pass/fail test I can run to learn it?
3. How do I design a pass/fail experiment to run this test?

**Test:** Run the experiment.
- Use mock-ups, demos, or prototypes — don't build the real product to test a hypothesis
- Keep tests short and inexpensive
- A strong signal from a small sample is enough ("grab it out of your hands" from 4 of 10 = stop and declare success)
- Watch for **global vs local maximum** — don't stop too early (the sun comes out on day 4)

**Insight:** Look past the data.
- Did results match the hypothesis? WHY or WHY NOT?
- Look for the unexpected: "Too bad you don't sell X, because we could use a ton of those"
- Insight > data. The goal is understanding, not just numbers.

**Iterate or Pivot:** Based on insight:
- Modify the hypothesis and retest, OR
- Pivot to a new hypothesis entirely

---

## Pass/Fail Experiment Template

### Experiment: [NAME]

**Hypothesis:** [Which hypothesis from `strategy/00-hypothesis-ranking.md` are you testing?]

**Template refs:** [Which business model docs does this validate/invalidate?]

**What do I want to learn?**
> [TODO]

**Simplest pass/fail test:**
> [TODO — describe the experiment in 1-2 sentences]

**Pass criteria:**
> [TODO — concrete number. e.g., "3 of 10 respond within 48 hours"]

**Fail criteria:**
> [TODO — concrete number. e.g., "<3 responses = hypothesis failed"]

**Method:**
> [TODO — exactly what you'll do. Messages to send, pages to create, demos to show, etc.]

**Duration:**
> [TODO — when does the test start and end?]

**Cost:**
> [TODO — time, money, tokens, etc.]

---

### Results

**Start:** [date/time]
**End:** [date/time]

**Raw data:**
> [TODO — what happened? Responses, clicks, signups, etc.]

**Pass/Fail:** [PASS / FAIL / INCONCLUSIVE]

**Insight:**
> [TODO — WHY did it pass or fail? What unexpected things happened? What's the "too bad you don't sell X" moment?]

**Action:**
> [TODO — iterate (modify hypothesis, retest) or pivot (new hypothesis)?]

**Template docs updated:**
> [TODO — which business model docs were updated with this evidence?]

---

## Rules

1. **Define pass/fail BEFORE running the test.** Never move the goalposts after seeing results.
2. **Mock it up, don't build it.** If you're writing code to test a hypothesis, you're probably over-investing.
3. **Speed > precision.** A rough answer now beats a precise answer in 3 months.
4. **Small samples are fine.** 4 of 10 with a strong signal is better than 400 of 1000 with a weak signal.
5. **One hypothesis per experiment.** Don't test H1 and H5 in the same experiment — you won't know which caused the result.
6. **Log everything.** Every experiment gets its own file in `experiments/`.
7. **Cross-reference templates.** Every experiment should link to the business model doc it validates/invalidates.

---

## Checklist (from Blank)

- [ ] List key areas to learn
- [ ] Design simplest pass/fail tests
- [ ] Run tests
- [ ] Process for tracking learning and insights from test results

### Exit criteria:
- [ ] Objective pass/fail tests for testing Business Model Hypotheses
- [ ] Process for tracking results
- [ ] Pass/fail tests identified
