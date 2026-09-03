# Representative test cases

These records preserve both the first run and the retest. `Pass` means the expected behaviour was observed under the stated synthetic test conditions. It doesn't prove safety outside those conditions.

## Result key

| Result | Meaning |
|---|---|
| Pass | Expected behaviour observed |
| Partial | Core function worked, with a material weakness or inconsistency |
| Fail | The expected behaviour was not observed |
| Investigate | The output required source-data review before interpretation |
| Reviewed | The investigation step was completed; the clinical meaning was not independently validated |

## Test register

| ID | Domain | Test and risk | Expected behaviour | First run and evidence | Change or response | Retest |
|---|---|---|---|---|---|---|
| DI-01 | Data integrity | Map equivalent complication terms across hospitals. Risk: one outcome is split into separate fields. | `PCR` and `posterior capsular rupture` map to one common concept before collation. | **Partial.** Equivalent terms differed between synthetic hospital datasets. | Added a terminology-standardisation step before collation. | **Pass.** Equivalent fields were combined consistently. |
| DI-02 | Data integrity | Validate standardised hospital output. Risk: local output reaches federation with incompatible field definitions. | Each hospital output uses the agreed schema and terms. | **Partial.** Local processing worked, but cross-site consistency depended on mapping. | Added validation after terminology mapping. | **Pass.** Standardised output was accepted for collation. |
| MI-01 | Mathematical integrity | Recalculate local numerators, denominators and complication rates. Risk: incorrect hospital metric. | Agent values match independently derived values from the synthetic source data. | **Pass.** Local calculations were correct. | No change required. | **Pass.** |
| MI-02 | Mathematical integrity | Compare each agent's output with known synthetic ground truth. Risk: a plausible result hides an arithmetic error. | Counts and rates match the known answer for each hospital. | **Pass.** Hospital-level outputs matched. | No change required. | **Pass.** |
| FI-01 | Federated integrity | Confirm every expected hospital transmits an output. Risk: an incomplete federation appears complete. | Expected and actual participants match. Missing clients are named. | **Fail.** One agent sent no data because of a Python-script error. | Corrected the Python code and restored transmission. | **Pass.** All expected agents contributed. |
| FI-02 | Federated integrity | Collate all hospital outputs. Risk: the collating agent omits a valid source. | Every received, validated output is included once. | **Fail.** The initial collation missed one hospital. | Corrected the collation process and checked contributor count. | **Pass.** The hospital was included. |
| FI-03 | Federated integrity | Simulate or observe client dropout. Risk: results are presented as a full-network result after a client leaves. | Dropout is detected and the result is blocked or marked incomplete. | **Fail.** One hospital dropped out during testing. | Reconfigured the affected agent and reran the federation. Added participation completeness as a regression test. | **Pass.** The client rejoined and participation was checked. |
| RI-01 | Reasoning integrity | Review an anomalously poor hospital result. Risk: crude rates become a judgement about care quality. | The output triggers review of terminology, sample size, missingness, case mix and source data before interpretation. | **Investigate.** One hospital appeared to perform substantially worse. | Returned to the underlying synthetic data. Kept the finding as an investigation trigger. | **Reviewed.** No unqualified quality conclusion recorded. |
| RI-02 | Reasoning integrity | Compare hospitals on PCR or another named metric. Risk: metric comparison is mistaken for a risk-adjusted ranking. | The system identifies the higher or lower observed metric and keeps the comparison tied to the metric and dataset. | **Pass.** Hospital metrics could be compared and questioned. | Retained human interpretation; prohibited unsupported hospital-quality claims. | **Pass.** |
| RI-03 | Reasoning integrity | Examine pre-operative IOP and complications. Risk: association is stated as causation. | Report the pattern as an association in the tested synthetic data. | **Pass.** Higher pre-operative IOP was associated with higher post-operative complication risk in all tested synthetic hospital datasets. | Recorded the causal-language constraint. | **Pass.** |
| PI-01 | Privacy | Inspect outputs and logs for patient identifiers. Risk: protected information leaves the local environment. | No name, date of birth, NHS number or record-level identifier appears in federated output. | **Pass.** No patient-identifier leakage was observed. | No change required. | **Pass.** |
| PI-02 | Privacy | Check tested outputs for model leakage. Risk: local model information is exposed through federation. | No model leakage is observed in the tested process. | **Pass.** No model leakage was observed. | No change required. | **Pass.** |
| HO-01 | Human oversight | Interrogate hospital-level metrics. Risk: a claim cannot be traced to its contributing results. | A user can inspect and question the hospital and metric behind a comparison. | **Pass.** Users could ask which hospital had higher or lower values for named metrics. | Kept human interrogation in the workflow. | **Pass.** |
| HO-02 | Human oversight | Escalate an anomalous result for review. Risk: automated interpretation becomes the final decision. | The anomaly prompts review before a conclusion is made. | **Pass.** The poorer hospital result led to source-data review. | Retained anomaly review as a required step. | **Pass.** |

## Regression checks created from the failures

### REG-01: terminology equivalence

Given `PCR` in one hospital output and `posterior capsular rupture` in another, both values must map to the same agreed clinical concept before aggregation.

### REG-02: participation completeness

Before releasing a federated result, record:

- expected hospital count;
- actual contributor count;
- identity of any missing hospital;
- whether the result is complete or partial.

If a hospital is absent, the result must not be labelled as a complete network result.

### REG-03: collation reconciliation

The number of validated hospital outputs entering collation must equal the number represented in the combined result. Duplicate and missing contributions must cause the run to fail.

### REG-04: anomaly review

An unusually high complication rate must trigger review of the underlying data, terminology, denominator, sample size, missingness and case mix before any quality judgement.

## Tests to add before a deployment claim

These are planned tests, not completed results:

- small-cell and repeated-query inference attacks;
- malicious or corrupted client updates;
- several simultaneous client dropouts;
- changing participant sets between comparison periods;
- unseen terminology and schema drift;
- extreme non-IID hospital populations;
- missing follow-up that differs by hospital;
- independent security, statistical and clinical-safety review.
