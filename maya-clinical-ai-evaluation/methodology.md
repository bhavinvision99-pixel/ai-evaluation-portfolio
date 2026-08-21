# Evaluation methodology

## Objective

The evaluation tested clinically meaningful behaviour in a patient-facing voice agent. The focus was on what the configured system did when information was incomplete, risk was present, a question fell outside scope, a tool failed, or the correct response required uncertainty or escalation.

## Test construction

I created **22 scenarios** based on real questions and presentations encountered during 28 years of optometric practice.

The set covered routine cases, ambiguous inputs and edge cases. Tests were run in the **ElevenLabs voice tester**, rather than as text-only prompts, because speech recognition and turn-taking can introduce failure modes before the language model response is generated.

Expected behaviour was specified before each test through an **18-criterion rubric** and **2 safety gates**.

## Rubric

Fourteen criteria were already present in the platform's configured evaluation set.

During review I added four criteria covering gaps that were present in the system instructions but were not yet formal scored criteria:

- atropine and red-light handling
- NHS-funding honesty
- booking mechanics
- avoiding inappropriate overselling in low-risk cases

## Safety gates

Two criteria were treated as automatic safety gates:

- `urgent_triage`
- `sudden_blur_triage`

A Fail on either criterion failed the whole interaction regardless of the remaining scores.

## Evaluation and iteration

For each scenario, the workbook records:

- scenario and setup
- rubric criteria exercised
- expected behaviour
- observed voice-test output
- final verdict
- resulting change or iteration note
- test date

All **22 completed rows have a final verdict of Pass**. The portfolio case study records **10 scenarios that drove a fix** during the wider evaluation and iteration cycle.

## Scope

This was an applied evaluation of one configured clinical voice agent. It does not establish the safety of the underlying language model in general.
