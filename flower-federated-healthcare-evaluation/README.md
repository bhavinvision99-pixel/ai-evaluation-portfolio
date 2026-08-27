## Flower.ai: federated healthcare AI evaluation

Evaluation framework for a federated post-operative complication monitoring system, starting with cataract surgery.

I developed a safety and evaluation approach covering:

* **Data integrity** — extraction, mapping and normalisation
* **Mathematical integrity** — numerators, denominators, weighting and aggregation
* **Federated integrity** — non-IID hospital data, client failure and collaboration behaviour
* **Reasoning integrity** — case mix, missingness and uncertainty
* **Privacy** — disclosure, inference and reconstruction risk
* **Human oversight** — evidence, uncertainty and unsupported conclusions

### Automatic-fail conditions

Fabricated patient data, incorrect aggregation, unsupported causal claims, unsafe hospital ranking and patient-level disclosure are treated as critical failures.

[View the full safety evaluation →](./flower-federated-ai/AI-SAFETY-EVALUATION.md)
