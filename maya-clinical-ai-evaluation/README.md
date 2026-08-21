# Maya: evaluating a patient-facing clinical AI voice agent

Maya is an optometry voice agent designed to answer parents' questions about childhood myopia, identify safety-critical presentations and support appropriate next steps.

I designed a structured evaluation to test what the agent did when information was incomplete, a parent described a red-flag symptom, evidence conflicted, a booking tool failed, or the safest response was to admit uncertainty.

## Evaluation at a glance

| Measure | Number |
|---|---:|
| Test scenarios | 22 |
| Scoring criteria | 18 |
| Safety-gate criteria | 2 |
| Additional criteria introduced during review | 4 |
| Scenarios that drove a fix | 10 |

## My role

I designed the clinical workflow and created test cases from questions and presentations encountered during 28 years of optometric practice.

I built the evaluation rubric, including four criteria I identified as gaps in the platform's built-in evaluation set:

- atropine and red-light handling
- NHS-funding honesty
- booking mechanics
- avoiding inappropriate overselling in low-risk cases

I then tested the agent in the ElevenLabs voice environment and used observed failures to change prompts, knowledge-base material or agent configuration.

## Evaluation loop

1. Clinical experience and real parent presentations
2. Routine, ambiguous and edge-case test scenarios
3. Expected behaviour defined through a rubric and safety gates
4. Voice testing with actual output captured and judged
5. Prompt, workflow, knowledge or configuration changes
6. Retesting

## What the rubric tested

### Clinical accuracy
Treatment efficacy, realistic expectations, lifestyle advice and risk-appropriate recommendations.

### Safety and triage
Red flags and recent blur. Failure on either safety-gate criterion failed the whole call.

### Guardrails
No diagnosis, no invented facts, controlled handling of atropine/red-light questions and NHS funding.

### Conversation and process
Tone, empathy, intake, booking behaviour, data capture and handling of tool failure.

## Problems surfaced

Testing surfaced issues involving:

- emergency triage
- onset urgency
- non-myopia scope
- prescription-sign confusion (myopia versus hyperopia)
- ortho-k prescription suitability and safety
- NHS-funding wording
- atropine/red-light questions
- voice-agent latency

These findings fed back into the prompt, knowledge base or agent configuration.

## Repository documents

- [Methodology](methodology.md)
- [Evaluation rubric](evaluation-rubric.md)
- [Representative test scenarios](test-scenarios.md)
- [Findings and fixes](findings.md)
- [Limitations and proposed next tests](limitations-and-next-tests.md)
- [Clinical decision logic](decision-tree.md)
- [Original 3-page case study](case-study.pdf)

## Tools

ElevenLabs, APIs, Claude Code, OpenAI Codex, GitHub and Vercel.

Most implementation code was generated using Claude Code or Codex. My work centred on system requirements, clinical logic, evaluation design, testing, failure analysis and directing changes.
