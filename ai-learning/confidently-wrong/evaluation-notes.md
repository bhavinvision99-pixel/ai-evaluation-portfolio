# Evaluation Notes

## Purpose

Confidently Wrong is an AI learning product, so evaluation considers more than whether the code works. The MVP is reviewed across factual quality, learning quality, interaction quality and transfer.

## 1. Factual quality

### Is there a defensible best answer?
Questions should not depend on subjective preference where several options are equally valid. Where concepts contain nuance, wording should ask for the **best** or **most accurate** explanation.

### Are claims appropriately qualified?
AI systems differ. Statements about privacy, training data, model behaviour, agents, retention, browsing and retrieval should not imply every product behaves identically.

### Could the answer become outdated?
Where possible, the core bank focuses on concepts that remain useful as individual products change.

## 2. Distractor quality

For each distractor, ask:

- Could an intelligent beginner reasonably believe this?
- Does it represent a genuine misconception?
- Is it wrong for an identifiable reason?
- Does explaining the error teach something useful?

Avoid absurd distractors or stylistic clues that reveal the correct answer.

## 3. STOP mapping

**SOURCE:** question provenance or evidence.  
**TRUTH:** independently verify an important claim.  
**OVERCONFIDENCE:** identify unjustified certainty or overinterpretation.  
**PAUSE:** consider consequence and risk.

Early questions emphasise one dimension. The final challenge combines all four.

## 4. Feedback quality

For each question:

- Is the explanation understandable without technical knowledge?
- Does it explain why the correct answer is stronger?
- Does it explain why each wrong answer feels plausible?
- Is it concise?
- Is the takeaway memorable?
- Does the learner know what to do differently afterwards?

## 5. Overconfidence test

Because the product teaches AI overconfidence, its own language needs scrutiny. Review explanations for unjustified words such as always, never, definitely or guaranteed. The product should model the behaviour it teaches.

## 6. Transfer

The final challenge tests whether the learner can apply STOP to a new scenario. Success is not simply recalling the acronym; the stronger indicator is understanding why each question matters.

## 7. UX and interaction testing

Test desktop and mobile layout, answer selection, correct/incorrect states, feedback reveal, progress, STOP progression, final challenge, score calculation, restart behaviour, keyboard navigation, contrast, focus states, overflow and layout shifts.

## 8. Failure modes considered

### Correct answer is too obvious
**Risk:** The experience becomes a conventional quiz.  
**Mitigation:** Strengthen distractors and remove stylistic clues.

### More than one answer is defensible
**Risk:** Reasonable judgement is penalised.  
**Mitigation:** Rewrite or ask for the "best" / "most accurate" response.

### Explanation becomes a lecture
**Risk:** Learner disengagement.  
**Mitigation:** Keep explanations short and prioritise one takeaway.

### Framework becomes more important than behaviour
**Risk:** Learners remember the acronym but fail to apply it.  
**Mitigation:** Use a final transfer scenario.

### Excessive distrust of AI
**Risk:** The lesson becomes "AI is unreliable."  
**Mitigation:** Emphasise proportional verification.

> You don't need to distrust AI. You need to know when to stop and check.

## 9. Current limitations

The MVP does not currently attempt to measure long-term retention or post-training behaviour, personalise difficulty, generate questions dynamically, independently verify live AI-generated questions, compare model performance, or provide comprehensive AI literacy training.

## 10. Next evaluation stage

Lightweight user testing with non-technical AI users could investigate:

1. Which distractors are too easy?
2. Which explanations are unclear?
3. Can learners recall STOP afterwards?
4. Can they apply STOP to a new scenario?
5. Does it increase verification of consequential outputs?
6. Which parts are most memorable?
7. Does the tone feel useful rather than patronising?
