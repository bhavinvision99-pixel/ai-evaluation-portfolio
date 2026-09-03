# MISMATCH — London Social Housing Policy Intelligence

**Data analysis · Behavioural science · AI-assisted development · Responsible AI · Data storytelling**

[**View the live MISMATCH application →**](https://mismatchlondon-beryl.vercel.app/)

> **London has an acute social-housing shortage. But does it also have a social-housing mismatch?**

MISMATCH is an interactive policy-intelligence project exploring how overcrowding and under-occupation vary across London's social-rented housing.

Built from public housing data, the project started with a simple question: **does treating London's housing challenge as a single problem hide important differences between boroughs?**

Rather than proposing a solution first, MISMATCH uses data to **diagnose the problem, challenge assumptions and identify better questions for further investigation.**

## Project at a glance

| | |
|---|---|
| **Live application** | https://mismatchlondon-beryl.vercel.app/ |
| **Geography** | 32 London boroughs |
| **Core population represented** | 790,221 social-rented households |
| **Primary dataset** | ONS Census 2021 — occupancy rating (bedrooms) by tenure |
| **Additional research** | GLA affordable-housing delivery; MHCLG / Local Authority Housing Statistics |
| **Current stage** | Build 1 — DIAGNOSE |
| **Approach** | Human-led, AI-assisted analysis and development |

## What this project demonstrates

MISMATCH was built as more than a dashboard. It demonstrates an end-to-end workflow from an ambiguous public-policy question to a working interactive product.

**Data & quantitative analysis**  
Data cleaning · data integration · exploratory analysis · quantitative reasoning · sensitivity analysis · metric design · data visualisation

**AI & technology**  
AI-assisted development · prompt engineering · rapid prototyping · interactive web development · responsible AI · AI evaluation

**Strategy & human behaviour**  
Behavioural science · human-centred design · policy analysis · problem framing · systems thinking · choice architecture

**Communication**  
Data storytelling · information design · technical communication · translating complex analysis for non-technical audiences

## Tech stack & workflow

The project used a combination of analytical, AI-assisted and web-development tools.

| Layer | Tools / approach |
|---|---|
| **Data** | ONS Census 2021, GLA housing datasets, MHCLG / Local Authority Housing Statistics |
| **Analysis** | Python-assisted data cleaning, joins, calculations, exploratory analysis and sensitivity testing |
| **AI workflow** | ChatGPT and AI-assisted coding/building for analysis acceleration, methodology exploration, iteration and review |
| **Product build** | AI-assisted web application development |
| **Frontend** | Interactive responsive web interface and data visualisations |
| **Deployment** | Vercel |
| **Version control / portfolio** | GitHub |
| **Design** | Human-centred information architecture, policy-dashboard UI and Canva communication assets |

> **Note:** AI accelerated the work, but the research question, methodological choices, interpretation, behavioural analysis, safety boundaries and final validation remained human-led.

## Repository data policy

The analysis uses public aggregate datasets, but **raw and processed CSV files are intentionally not distributed in this repository**.

This keeps the portfolio focused on the methodology and outputs while respecting source licensing, attribution and redistribution requirements.

The repository instead documents:

- the datasets used
- relevant source organisations
- definitions and transformations
- analytical methodology
- derived metrics
- limitations and comparability caveats

No patient-level, tenant-level or personally identifiable data is used in MISMATCH.

For reproducibility, the methodology documents the calculations required to recreate the analysis from the relevant source datasets, subject to their original licensing terms.

## My role

I framed the research question, sourced and interrogated the datasets, developed and tested the analytical methodology, applied behavioural-science principles, established claim and human-impact guardrails, directed the product design and used AI-assisted tools to accelerate analysis, coding and iteration.

## What I found

Analysis of 2021 Census data representing **790,221 social-rented households across 32 London boroughs** found:

- **19.4%** were overcrowded
- **24.8%** were under-occupied by at least one bedroom
- **6.7%** were under-occupied by two or more bedrooms

But London-wide averages concealed substantial borough differences.

| Borough | Overcrowded | Under-occupied | Pattern |
|---|---:|---:|---|
| Tower Hamlets | 26.8% | 20.4% | Overcrowding pressure |
| Merton | 21.5% | 26.4% | Mixed / mismatch |
| Bromley | 12.5% | 29.6% | Under-occupation pressure |

**Same city. Same broad housing crisis. Very different local pictures.**

## From data to diagnostic

Simply comparing two percentages wasn't enough.

During development I explored several approaches to classifying boroughs, including:

- comparison with London-wide averages
- absolute percentage-point differences
- statistical significance
- relative differences between overcrowding and under-occupation

Each approach had limitations.

For example, because Census data represents population counts rather than a conventional sample, large borough populations can make very small differences statistically significant without necessarily making those differences meaningful for policy.

I therefore developed an exploratory **Relative Imbalance** measure:

```text
Relative Imbalance =
(Underoccupation - Overcrowding)
-------------------------------- × 100
(Underoccupation + Overcrowding)
```

Positive values indicate stronger under-occupation pressure; negative values indicate stronger overcrowding pressure.

I then sensitivity-tested alternative thresholds before selecting **±12.5% as an exploratory diagnostic threshold**.

This is deliberately presented as a **modelling choice rather than an official housing standard**.

The methodology is designed to remain transparent, challengeable and replaceable as additional evidence becomes available.

## Two analytical lenses

### 1. Borough Diagnosis

**Which pressure dominates within this borough?**

This compares overcrowding and under-occupation within the borough using Relative Imbalance.

### 2. London Context

**How unusual are those pressures compared with London overall?**

This compares each borough with the London benchmarks.

A borough can therefore have relatively balanced internal pressures while still experiencing high levels of both compared with London.

Separating these questions avoids compressing different types of information into a single classification.

## Behavioural science

Data can identify an apparent housing mismatch.

**It cannot tell us how the people living in those homes will behave.**

An administrative dataset might describe an:

> **“Under-occupied three-bedroom property.”**

The resident might describe:

> **“My home of 30 years.”**

That distinction matters.

Several behavioural factors could affect voluntary housing mobility:

- **Loss aversion** — moving may involve losing valued features, relationships and familiarity.
- **Status quo bias** — remaining requires no active decision, while moving involves uncertainty and change.
- **Place attachment** — homes are embedded within communities, identities, routines and social networks.
- **Friction costs** — applications, finding an appropriate property, removals, accessibility, utilities and uncertainty can make moving difficult even when someone wants to move.

This leads to two important distinctions:

> **Under-occupation ≠ willingness to move.**

> **Willingness to move ≠ ability to move.**

Rather than asking:

> *“How do we get people to downsize?”*

a more human-centred behavioural question is:

> **“What would a voluntary housing alternative need to look like for someone to genuinely prefer it to remaining in their current home?”**

MISMATCH therefore treats housing mobility as a **choice-design problem**, not simply a stock-optimisation problem.

## Responsible AI, claims and human impact

Housing data describes people's homes and can easily support conclusions that go beyond what the evidence actually shows.

I therefore introduced explicit boundaries between:

### Observation

> 29.6% of Bromley's social-rented households are under-occupied.

**Directly supported by the data.**

### Analytical interpretation

> Under-occupation is the stronger observed occupancy pressure in Bromley.

**Derived from the analytical methodology.**

### Hypothesis

> Voluntary housing mobility may warrant further investigation.

**A question for further evidence and research.**

### Unsupported conclusion

> Under-occupying tenants should be moved into smaller properties.

**Not supported by the data.**

The project therefore applies several explicit guardrails:

- under-occupied **does not mean** willing to move
- under-occupied **does not mean** a property is available
- an apparently spare bedroom **does not mean** unnecessary space
- borough-level patterns cannot determine individual household circumstances
- correlation must not be presented as causation
- a diagnostic classification does not prescribe a policy intervention
- voluntary mobility should not be reframed as forced downsizing
- observed evidence must remain distinguishable from interpretation and hypothesis

The objective is to use AI and data to **improve human decision-making without allowing analytical convenience to erase human context.**

## Adding registered housing demand

The next stage of the analysis introduced local-authority housing-register data.

More than **341,000 households were recorded on London's local-authority housing waiting lists in 2024–25**.

I joined borough-level waiting-list data to the MISMATCH dataset using ONS geographic codes and created an exploratory indicator:

> **Registered demand relative to existing social-rented stock**

This revealed another important finding:

**Relative Imbalance alone should not determine policy priority.**

For example, a borough can appear relatively balanced between overcrowding and under-occupation while simultaneously experiencing very high registered housing demand.

Waiting-list figures also require careful interpretation because local authorities can operate different eligibility criteria, register-management processes and review procedures.

MISMATCH therefore describes this layer as **registered housing demand**, rather than treating it as a definitive measure of housing need.

## Data storytelling and product design

The analysis was translated into an interactive web application rather than presented only as a spreadsheet.

MISMATCH includes:

- interactive London borough mapping
- borough-level diagnosis
- overcrowding and under-occupation metrics
- Relative Imbalance
- London benchmark comparisons
- comparative borough case studies
- transparent methodology and assumptions

The interface is deliberately designed to move users through:

> **DATA → PATTERN → INTERPRETATION → QUESTION**

rather than:

> **DATA → AUTOMATIC POLICY RECOMMENDATION**

This was an important product and responsible-AI design decision.

## How I used AI

MISMATCH was developed using an **AI-assisted, human-led workflow**.

### Human-led

- problem framing
- research questions
- dataset selection
- behavioural-science analysis
- methodology decisions
- interpretation
- policy reasoning
- safety boundaries
- product direction
- final validation

### AI-assisted

- exploratory data analysis
- code generation
- data cleaning and transformation
- statistical calculations
- methodology exploration
- sensitivity analysis
- UI development
- visualisation
- research acceleration
- copy and interface iteration

### Human-validated

- source definitions
- calculations
- methodology
- assumptions
- classifications
- policy claims
- behavioural interpretation
- public-facing outputs

AI was used to **accelerate analysis and building, not outsource judgement**.

## Skills demonstrated

**Data & quantitative**  
`Data Analysis` · `Data Cleaning` · `Data Integration` · `Exploratory Analysis` · `Sensitivity Analysis` · `Quantitative Reasoning` · `Data Visualisation`

**AI & technology**  
`AI-Assisted Development` · `Prompt Engineering` · `Web Development` · `Rapid Prototyping` · `Responsible AI` · `AI Evaluation`

**Strategy & human behaviour**  
`Behavioural Science` · `Human-Centred Design` · `Policy Analysis` · `Problem Framing` · `Systems Thinking`

**Communication**  
`Data Storytelling` · `Information Design` · `Technical Communication` · `Stakeholder Communication`

## Data sources

The project currently draws on public data from:

- **ONS Census 2021** — occupancy rating by bedroom and tenure
- **Greater London Authority** — affordable/social housing delivery data
- **MHCLG / Local Authority Housing Statistics** — local-authority housing waiting lists

Source definitions, transformations and limitations are documented separately so that the analysis can be inspected and challenged.

## Limitations

MISMATCH is an **exploratory policy-intelligence tool, not a policy recommendation engine**.

Important limitations include:

- Census occupancy data is from 2021.
- Under-occupation does not establish whether a household wants or is able to move.
- Bedroom standards cannot capture every accessibility, caring or family requirement.
- Waiting-list practices differ between local authorities.
- Borough-level observations cannot be applied to individual households.
- The Relative Imbalance threshold is exploratory.
- The current analysis cannot establish causation.
- Existing data does not yet show the complete relationship between bedroom requirements, existing stock and the bedroom mix of newly delivered homes.

These limitations are treated as part of the analysis rather than hidden from the user.

## What's next

MISMATCH is being developed in stages:

**01 — DIAGNOSE** ✓  
Identify borough-level overcrowding and under-occupation patterns.

**02 — UNDERSTAND**  
Add registered demand, bedroom requirements, housing delivery, bedroom mix and household characteristics.

**03 — SIMULATE**  
Explore transparent scenarios around new supply, voluntary housing mobility and stock matching without presenting simulations as predictions.

**04 — ACT / COMMUNICATE**  
Turn evidence into borough-level intelligence, comparisons and decision-support outputs.

The next major research question is:

> **Do the homes London has — and the homes it is building — align with the types of homes households appear to need?**

## The question behind MISMATCH

London clearly needs more social housing.

MISMATCH doesn't challenge that.

It asks whether **supply is the entire problem** — and whether better data can help us understand the interaction between supply, housing mix, allocation and voluntary mobility.

Ultimately:

> **How can we make better use of London's social housing without forgetting that every data point represents someone's home?**
