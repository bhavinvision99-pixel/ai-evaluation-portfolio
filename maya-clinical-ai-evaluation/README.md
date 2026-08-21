# Maya: evaluating a patient-facing clinical AI voice agent

Maya is an optometry voice agent designed to answer parents' questions about childhood myopia, identify safety-critical presentations and support appropriate next steps.

I designed a structured evaluation to test what the agent did when information was incomplete, a parent described a red-flag symptom, a question fell outside scope, a booking tool failed, or the safest response was to admit uncertainty.

**[View the 3-page case study PDF](case-study.pdf)**

## Evaluation at a glance

| Measure | Number |
|---|---:|
| Voice-test scenarios | 22 |
| Scoring criteria | 18 |
| Safety-gate criteria | 2 |
| Additional criteria introduced during review | 4 |
| Final Pass verdicts in completed workbook | 22 |
| Scenarios that drove a fix (case-study summary) | 10 |

A final Pass is the end-state verdict recorded after testing and iteration. It does not mean the scenario exposed no weakness during development.

## My role

I designed the clinical workflow and created test cases from questions and presentations encountered during 28 years of optometric practice.

I built the evaluation rubric, including four criteria I identified as gaps in the platform's existing evaluation set:

- atropine and red-light handling
- NHS-funding honesty
- booking mechanics
- avoiding inappropriate overselling in low-risk cases

I tested the configured agent in the ElevenLabs voice environment and traced issues through system instructions, knowledge sources or agent configuration.

## Evaluation artefacts

- [Methodology](methodology.md)
- [Rubric overview](evaluation/rubric.md)
- [Full rubric as CSV](evaluation/rubric.csv)
- [Scenario-level results](evaluation/scenario-results.md)
- [Cleaned results dataset](evaluation/evaluation-results.csv)
- [Results summary](evaluation/results-summary.md)
- [Worked findings](evaluation/worked-findings.md)
- [Clinical decision logic](decision-tree.md)
- [Limitations and proposed next tests](limitations-and-next-tests.md)

## Selected findings

### Atropine licensing
Outdated licensing information was identified and corrected across four knowledge-base files.

[Read finding](findings/atropine-licensing.md)

### Ortho-k infection-rate source tracing
Two figures initially appeared inconsistent. Source tracing established that the lower 4–6 per 10,000 figure came from the same Russian ortho-k study already cited in the knowledge base.

[Read finding](findings/ortho-k-evidence.md)

### Honest gap
The agent is deliberately instructed not to invent a precise axial-length action threshold where the underlying guidance does not provide one.

[Read finding](findings/honest-gap.md)

### Voice latency
Testing identified response lag that affected conversational pacing and led to configuration review.

[Read finding](findings/voice-latency.md)

## Voice-specific testing

The project was tested in a voice environment rather than only through text prompts. One TC-03 run transcribed **“floaters” as “flowers”**, requiring repetition. This exposed a safety-relevant failure mode at the speech-recognition layer.

## Tools

ElevenLabs, APIs, Claude Code, OpenAI Codex, GitHub and Vercel.

Most implementation code was generated using Claude Code or Codex. My work centred on system requirements, clinical logic, evaluation design, testing, failure analysis and directing changes.

## Scope

This is an applied evaluation of one configured clinical voice agent. It is not a general evaluation of the underlying language model.
