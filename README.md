# AI Evaluation & Experimental Projects

I'm Bhavin Shah, a former clinician, behavioural science practitioner and independent AI builder developing a research focus in AI evaluation and safety.

This repository documents selected work involving AI evaluation, behavioural testing, digital measurement and AI-assisted software development.

## Featured project: Maya clinical AI evaluation

I designed a structured evaluation of Maya, a patient-facing clinical AI voice agent answering parents' questions about childhood myopia.

The completed evaluation contains:

- **22 voice-test scenarios**
- **18 scoring criteria**
- **2 safety-gate criteria**
- **4 additional criteria** identified during review
- **22 final Pass verdicts** in the completed workbook
- **10 scenarios that drove a fix**, as reported in the case-study summary

The repository now includes a cleaned scenario-level dataset, an inspectable rubric, worked findings and the original case-study PDF.

[Explore the Maya evaluation](maya-clinical-ai-evaluation/README.md)  
[View the 3-page case study](maya-clinical-ai-evaluation/case-study.pdf)

### MISMATCH — London social-housing policy intelligence

**Data analysis · Behavioural science · Responsible AI · Data storytelling · AI-assisted development**

An interactive policy-intelligence project investigating whether London's
social-housing shortage is also partly a problem of housing mismatch.

I analysed Census data representing **790,221 social-rented households
across 32 London boroughs**, developed and sensitivity-tested a new
**Relative Imbalance** diagnostic, and used behavioural science to examine
why an apparent housing mismatch in a dataset does not automatically
translate into willingness or ability to move.

The project demonstrates the full workflow from:

**public data → analysis → methodology → behavioural interpretation →
responsible-AI guardrails → interactive product → public communication**

[Explore the MISMATCH case study](./mismatch-london/)

[View the live application](https://mismatchlondon-beryl.vercel.app/)

## Selected projects

### Flower federated healthcare evaluation

A prototype evaluation of federated post-operative complication monitoring using Flower and synthetic cataract-surgery data.

The hospital agents calculated their local metrics correctly. System-level testing then found inconsistent clinical terminology, a Python error that stopped one hospital sending data, incomplete collation and a separate client dropout.

The evaluation covers 6 domains and records the first result, investigation, change and retest across 14 test cases. It also includes critical-failure rules, regression tests and a visual of the evaluation loop.

**What this demonstrates:** AI safety evaluation, known-answer testing, federated-system testing, failure analysis, clinical reasoning, privacy checks and human oversight.

[Explore the Flower evaluation →](flower-federated-healthcare-evaluation/)


### Rapid visual naming and scanning assessment
A tablet-based system for measuring rapid visual naming and scanning behaviour.

[Project notes](rapid-visual-naming/README.md)

### AI agents and applied LLM systems
Selected notes on voice agents and AI-assisted systems.

[Project notes](ai-agents/README.md)

### Dyslexia Vision
Public information and tools for people with dyslexia.

https://www.dyslexia.vision/

[Project notes](other-projects/dyslexia-vision.md)

### ADHD Unfreeze
Public information and tools project.

https://adhdunfreeze.com/

[Project notes](other-projects/adhd-unfreeze.md)

### Behavioural research
Behavioural science in myopia management
Applied behavioural research into a difficult preventative-health decision involving parents, children, clinicians and long-term adherence.
The work combined behavioural diagnosis, system modelling, intervention design and longitudinal practice outcomes. It reached approximately 80% consultation-to-enrolment conversion and under 6% attrition across four years.
Read the project

### Research and scientific writing
These earlier projects are included as evidence of research synthesis and scientific communication. They are not AI safety research.
Defusing the Myopia Time-Bomb
Clinical evidence synthesis covering myopia prevalence, risk, mechanisms, prediction and management.
Read the project
Vision and Dyslexia
Evidence synthesis in a contested clinical area, with attention to conflicting findings, association versus causation and limits of visual interventions.
Read the project

### Music therapy in Parkinson’s disease

An independent narrative literature review examining the evidence for music-based interventions in Parkinson’s disease. The review considers rhythmic auditory stimulation, gait and motor symptoms, speech, mood, cognition, quality of life and the role of music therapy alongside pharmacological and multidisciplinary treatment.

The project also discusses limitations in the evidence base, including small samples, heterogeneous interventions, short follow-up periods and limited representation of people with advanced Parkinson’s disease.

[Read the literature review](research/music-therapy-parkinsons/music-therapy-parkinsons-literature-review.pdf)

### Confidently Wrong — Interactive AI Literacy & Learning Design

Built an interactive learning experience for non-technical users exploring a deceptively difficult problem: **how do you know when an AI-generated answer deserves your trust?**

The experience uses plausible AI answers, immediate explanatory feedback and a behavioural framework I developed called **STOP — Source, Truth, Overconfidence, Pause**. Learners progressively discover the framework before applying it independently to a final scenario.

**What this demonstrates:** AI-assisted product development, learning design, behavioural science, LLM literacy, evaluation, UX thinking, factual QA and human oversight.

[View case study →](ai-learning/confidently-wrong/README.md)

## Development approach

I use Claude Code and OpenAI Codex extensively for software implementation. Most Python and JavaScript/TypeScript used in these projects was generated with AI coding agents.

My contribution focuses on problem definition, system behaviour and requirements, workflow design, connecting services and APIs, evaluation, testing, failure analysis, directing subsequent changes and deployment.

Tools used across projects include **Claude Code, OpenAI Codex, GitHub, Vercel, ElevenLabs and APIs**.

## Portfolio scope

This portfolio brings together applied AI evaluation, responsible AI,
behavioural science, data analysis and AI-assisted product development.

The projects deliberately cover different parts of the AI lifecycle:

- **Maya** — evaluating the safety and behaviour of a patient-facing clinical AI
- **MISMATCH** — turning public data into human-centred policy intelligence
- **Flower federated evaluation** — testing data, mathematical, federated and privacy integrity
- **Behavioural research** — applying behavioural science to real-world decision systems
- **AI-assisted products** — defining, building, testing and deploying working digital systems

Across the portfolio, my focus is less on writing software manually and more
on defining the right problem, designing system behaviour, interrogating
evidence, evaluating outputs, identifying failure modes and using AI tools
to turn ideas into working systems.
