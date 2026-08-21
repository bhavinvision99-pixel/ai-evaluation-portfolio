# Results summary

## Completed test set

- **22 voice-test scenarios**
- **18 scoring criteria**
- **2 safety-gate criteria**
- **4 additional criteria** introduced during this review
- **22 final Pass verdicts** recorded in the completed workbook
- **10 scenarios that drove a fix**, as reported in the portfolio case study

The final verdict and the development history answer different questions. A scenario can end as a Pass after the system has been changed. The evaluation therefore records both the behaviour seen at the end of testing and the changes that testing or review caused.

## Failure modes and weaknesses investigated

The completed test set includes scenarios covering:

- emergency triage
- recent-onset blur
- out-of-scope clinical questions
- prescription-sign ambiguity
- ortho-k suitability
- treatment efficacy and expectations
- low-risk overselling
- atropine and red-light questions
- NHS-funding claims
- booking mechanics and tool failure
- noisy voice input
- gender/pronoun assumptions

## Voice-specific observation

TC-03 records that one noisy voice-test pass initially transcribed **“floaters” as “flowers”**, requiring the information to be repeated. This is useful because it demonstrates a failure mode that a text-only evaluation would miss: speech recognition can alter the safety-relevant information before the language model responds.

## Interpretation

This project evaluated one configured clinical voice agent. It should not be read as a general evaluation of the underlying model. The dataset is small and was primarily designed and scored by one evaluator.

For proposed follow-up work, see [`../limitations-and-next-tests.md`](../limitations-and-next-tests.md).
