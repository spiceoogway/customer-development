# Delegation Contract — Test Plan

Goal: move from abstract schema to falsifiable product learning.

## Core test
Does adding a tiny obligation object make third-party understanding and closure judgment materially easier than thread-only collaboration?

## Test design

### Variant A — thread only
Reviewer sees:
- collaboration thread / summary
- artifact links
- no explicit obligation object

Reviewer answers:
1. What was promised?
2. What counts as done?
3. Is the work resolved, in progress, or ambiguous?
4. Who had authority to close it?
5. How confident are you?

### Variant B — thread + obligation object
Reviewer sees:
- same thread / summary
- same artifact links
- compact delegation contract object

Reviewer answers the same 5 questions.

## Success metric
The object is useful if reviewers in Variant B show:
- higher agreement on status
- higher confidence
- fewer invented assumptions about closure and success criteria
- faster judgment time

## Minimum materials needed
1. One ambiguous real collaboration example (Brain × Tricep is candidate #1)
2. One compact thread summary
3. One compact obligation object
4. 3-5 reviewers (agents or operators)
5. A scoring rubric for agreement/confidence

## Scoring rubric
For each reviewer:
- `status_correctness`: did they avoid falsely calling `resolved`?
- `success_condition_clarity`: did they identify what is missing / explicit?
- `closure_authority_clarity`: did they identify whether closure authority is known?
- `confidence`: low / medium / high
- `time_to_judgment_seconds`

## Hypothesis
A small explicit obligation object will produce materially better reduction than thread-only context.

## Failure mode
If reviewers still disagree heavily even with the object, then:
- the object is too weak
- or the real problem is not representation but governance / incentive structure

## Next concrete move
Turn Brain × Tricep into two review packets:
- packet A: thread summary only
- packet B: thread summary + delegation contract example
