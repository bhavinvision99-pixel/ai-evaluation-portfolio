# Confidently Wrong

### An interactive AI literacy experience for non-technical users

**Live demo:** https://a-inontechie.vercel.app/

**Confidently Wrong** is a short interactive learning experience designed to teach an increasingly important AI skill:

> How do you decide whether an AI-generated answer deserves your trust?

Rather than explaining AI reliability through a conventional article or training deck, the experience puts the learner directly into the problem. Each challenge presents three confident, plausible AI answers. Only one is the best answer, while the wrong answers are deliberately designed to sound convincing.

Learners progressively discover a simple framework for critically assessing AI output:

## STOP

**S — SOURCE** — Where did this information come from?  
**T — TRUTH** — Can the important claim be independently verified?  
**O — OVERCONFIDENCE** — Is the AI more certain than the evidence allows?  
**P — PAUSE** — What happens if this answer is wrong?

> **Before you trust AI, STOP.**

## The problem

Generative AI creates an unusual information problem: incorrect answers do not necessarily look incorrect. An LLM can produce an answer that is fluent, specific, professionally written, logically structured and confident — and still be wrong.

For non-technical users, this can create a shortcut:

**good writing → perceived expertise → trust**

The learning challenge was therefore not simply to explain hallucinations. It was to help users experience the gap between **plausibility and reliability**, then give them a practical method for responding to it.

## Target audience

The experience is designed for intelligent non-technical professionals using tools such as ChatGPT, Claude, Gemini, Microsoft Copilot and other generative AI systems. No technical or computer-science knowledge is assumed. The emphasis is on practical judgement.

## How the experience works

The learner is shown AI-related scenarios with three plausible answers and must commit before receiving feedback. The experience explains which answer is strongest, why it is stronger, why the alternatives are tempting, and what practical lesson to remember.

STOP is revealed progressively rather than presented upfront:

**question → decision → feedback → explanation → framework → application**

The final challenge asks the learner to apply the complete STOP framework to a new situation.

## Topics covered

- how LLMs generate answers
- hallucinations and fabricated citations
- verification of changing information
- AI overconfidence
- correlation versus causation
- privacy and confidential information
- appropriate human oversight
- risk-based verification

The objective is not comprehensive AI education. It is to teach one useful behaviour well.

## Learning design

The experience uses ask-before-explaining, plausible distractors, immediate feedback, progressive disclosure, chunking and a final transfer challenge. See [learning-design.md](learning-design.md).

## AI-assisted development

This project was built using an AI-native development workflow. AI coding tools accelerated prototyping, implementation, interface development, debugging and iteration.

### My role

I was responsible for:

- identifying the learning problem
- defining the audience
- designing the STOP framework
- designing the learning journey
- question and distractor logic
- feedback design
- behavioural principles
- requirements
- factual review
- testing
- acceptance criteria
- final product judgement

The purpose of AI coding agents was to increase what one person could build and test while retaining human responsibility for learning design and quality.

## Evaluation

The product was evaluated for defensible answers, plausible distractors, useful feedback, STOP mapping, appropriately qualified factual claims, transfer and usability. See [evaluation-notes.md](evaluation-notes.md).

## Why I built it

The project explores an area of AI that particularly interests me:

**building systems is becoming easier; knowing whether their outputs deserve trust remains difficult.**

As AI becomes accessible to increasingly non-technical users, AI literacy needs to extend beyond prompting to verification, uncertainty, provenance, appropriate scepticism, risk and human oversight.

## Project status

**MVP — live working prototype**

**Try it:** https://a-inontechie.vercel.app/

Potential future development includes larger randomised question banks, difficulty levels, adaptive learning, performance by STOP category, and additional scenarios covering RAG, grounding, agents, bias and model selection.

## Related documentation

- [Learning design](learning-design.md)
- [Evaluation notes](evaluation-notes.md)
- [Question bank](question-bank.md)

## Author

**Bhavin Shah**

AI evaluation, AI-assisted product development, behavioural science and healthcare technology.

Part of the **AI Evaluation Portfolio**.
