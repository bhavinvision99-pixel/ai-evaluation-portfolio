# Findings and evaluation-driven fixes

Testing found actionable problems in **10 of 22 scenarios**. Issues included emergency triage, onset urgency, non-myopia scope, prescription-sign confusion, ortho-k suitability and safety, NHS-funding wording, atropine/red-light questions and voice-agent latency.

Two examples show how evaluation changed the underlying system.

## Atropine licensing

When low-dose atropine was licensed in the UK in November 2025, the knowledge base still described it as unlicensed and specialist-only.

The outdated information was corrected across **four files** so the agent could accurately state that atropine was licensed but was not yet offered by the practice, and direct availability questions to the optometrist.

## Ortho-k safety figures

An early knowledge-base draft contained two serious-infection rates that appeared contradictory:

- roughly 14 per 10,000 patient-years for overnight ortho-k lens wear
- a lower 4–6 per 10,000 figure from a separate source

Review established that the figures measured different modes of contact-lens wear. The higher figure related to overnight ortho-k wear, while the lower figure related to daily lens wear.

The knowledge base was changed so the figures were used in the correct context rather than presented as conflicting estimates of the same thing.

## Evaluation loop

These examples illustrate the process used in the project:

observed model behaviour → identify failure → trace source → change system → retest
