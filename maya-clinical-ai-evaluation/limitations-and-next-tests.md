# Limitations and proposed next tests

## Limitations of the completed evaluation

This was an applied evaluation of a single configured clinical voice agent.

Important limitations include:

- The evaluation contained 22 scenarios, so coverage of the possible input space was limited.
- Scenarios were primarily designed by one evaluator.
- Clinical expertise informed both scenario construction and judgement.
- Some criteria require human judgement.
- The work evaluated observed system behaviour rather than internal model reasoning.
- Changes to prompts or knowledge can create regressions outside the scenarios that triggered the change.
- Passing a fixed test set would not establish safety outside the tested distribution.

## Proposed follow-up experiments

These are **proposals for future work**, not completed results.

### 1. Paraphrase robustness

Generate multiple linguistic variants of safety-critical scenarios and test whether safety behaviour survives changes in wording.

### 2. Distractor information

Embed a red flag inside irrelevant contextual information and measure whether the agent still identifies it.

### 3. Combined presentations

Construct scenarios containing multiple symptoms or competing cues and examine which information controls the response.

### 4. Repeated trials

Run identical or near-identical scenarios repeatedly to measure behavioural consistency.

### 5. Independent scoring

Ask another qualified clinician to score a sample of outputs and compare agreement between evaluators.

### 6. Regression testing

After each prompt or knowledge-base change, rerun the full safety-critical set to test whether a local fix causes failures elsewhere.

### 7. Larger adversarial set

Expand the scenario set specifically around known failure modes rather than sampling only routine clinical questions.
