# Methodology

## Purpose

MISMATCH is designed as an exploratory diagnostic tool. It does not prescribe policy. Its purpose is to identify borough-level housing patterns that warrant further investigation.

## Core Census dataset

The first build uses ONS Census 2021 occupancy-rating-by-bedrooms data for households in the **Social rented** tenure category.

Scope:
- 32 London boroughs
- City of London excluded from the London benchmark because of its very small social-rented base
- `Does not apply` excluded

Occupancy categories:
- `+2 or more`
- `+1`
- `0`
- `−1 or less`

Definitions used:
- **Overcrowded** = occupancy rating `−1 or less`
- **Under-occupied 1+** = `+1` plus `+2 or more`
- **Strongly under-occupied** = `+2 or more`

## London-wide benchmark

Across the 32 boroughs:

- Social-rented households: **790,221**
- Overcrowded: **153,363 (19.4%)**
- Under-occupied 1+: **196,212 (24.8%)**
- Under-occupied 2+: **52,718 (6.7%)**

## Why the methodology evolved

Several candidate methods were explored.

### London-average quadrant classification

The first approach classified boroughs according to whether overcrowding and under-occupation were above or below London averages.

This was useful for context, but it answered a different question:

> How does this borough compare with London?

It did not directly answer:

> Which pressure dominates inside this borough?

### Percentage-point difference

A second approach compared the two rates directly.

This was intuitive, but the same absolute gap can represent very different proportional differences depending on the overall level of both indicators.

### Statistical significance

Sampling-style significance tests were also considered.

However, Census data represents population counts rather than a conventional sample, and large borough populations can make small differences statistically significant even when they may not be materially important for policy.

Statistical significance was therefore not used as the primary classifier.

## Relative Imbalance

The primary diagnostic uses:

```text
Relative Imbalance =
(Underoccupation - Overcrowding)
-------------------------------- × 100
(Underoccupation + Overcrowding)
```

Interpretation:
- positive = under-occupation dominates
- negative = overcrowding dominates
- zero = equal pressure
- larger absolute values = stronger imbalance

Examples:
- Merton: +10.2%
- Tower Hamlets: −13.5%
- Bromley: +40.5%
- Newham: −5.2%
- Hackney: +14.7%
- Southwark: +15.3%

## Exploratory threshold

Sensitivity analysis was run across several candidate thresholds.

A working threshold of **±12.5%** was selected because it provided a useful balance between sensitivity and interpretability.

Classification:
- **≤ −12.5%** → Overcrowding Pressure
- **−12.5% to +12.5%** → Mixed / Mismatch
- **≥ +12.5%** → Under-occupation Pressure

Strength:
- `|RI| < 12.5` → Mixed
- `12.5 ≤ |RI| < 25` → Moderate dominance
- `|RI| ≥ 25` → Strong dominance

This threshold is:
- exploratory
- not an official housing standard
- not statistically derived
- explicitly reviewable as the project develops

## Two-lens framework

### Borough Diagnosis
Which pressure dominates within the borough?

### London Context
How do each of the borough's pressure rates compare with London overall?

These are intentionally kept separate.

A borough can be internally mixed while still having high levels of both overcrowding and under-occupation relative to London.

## Registered housing demand

A second evidence layer uses borough-level local-authority waiting-list data.

The exploratory normalised measure is:

```text
Waiting-list households in 2025
-------------------------------- × 100
Social-rented households in 2021
```

This is described as:

**Registered demand relative to existing social-rented stock**

It is not:
- applicants per available home
- a supply-demand ratio
- a definitive measure of unmet housing need

The numerator and denominator also refer to different years.

## Principle

MISMATCH is designed to move from:

**Evidence → interpretation → question**

not:

**Evidence → automatic policy recommendation**
