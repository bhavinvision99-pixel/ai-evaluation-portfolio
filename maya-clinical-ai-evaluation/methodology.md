# Evaluation methodology

## Objective

The evaluation was designed to test clinically meaningful behaviour in a patient-facing voice agent rather than rely on fluency or general response quality.

The core question was whether Maya behaved appropriately when information was incomplete, risk was present, evidence conflicted, a tool failed, or the correct response required uncertainty or escalation.

## Test construction

I created **22 scenarios** from real questions and presentations encountered during 28 years of optometric practice.

The set included routine cases, ambiguous cases and edge cases.

Expected behaviour was defined before testing through an **18-criterion rubric** and **2 safety gates**.

## Evaluation

The configured agent was tested in the ElevenLabs voice environment. Actual responses were captured and judged against the expected behaviour.

Failure on either safety-gate criterion failed the whole interaction.

## Iteration

Where testing exposed a problem, I traced it back through the system. Depending on the cause, I changed the prompt, workflow, knowledge base or agent configuration and retested.

Ten of the 22 scenarios drove a fix.

## Scope

This was an applied evaluation of one configured clinical voice agent. It does not establish the safety of the underlying language model in general.
