# Responsible AI: Claims and Guardrails

## Why this matters

Housing data can support interpretations that go beyond what the evidence actually shows.

MISMATCH therefore separates:

1. **Observed evidence**
2. **Analytical interpretation**
3. **Hypothesis**
4. **Unsupported or potentially harmful conclusion**

## Example

### Observation

> 29.6% of Bromley's social-rented households are under-occupied.

This is supported directly by the dataset.

### Analytical interpretation

> Under-occupation is the stronger observed occupancy pressure in Bromley.

This is derived from the diagnostic methodology.

### Hypothesis

> Voluntary housing mobility may warrant further investigation.

This is a research or policy question, not a conclusion.

### Unsupported conclusion

> Under-occupying tenants should be moved into smaller properties.

The dataset does not support this claim.

## Guardrails

MISMATCH should never infer:

- `under-occupied → willing to move`
- `under-occupied → property is available`
- `spare bedroom → unnecessary bedroom`
- `borough classification → household circumstances`
- `correlation → causation`
- `diagnosis → prescribed intervention`
- `registered waiting-list total → definitive housing need`
- `relative imbalance → policy priority`

## Language guardrails

Preferred:
- voluntary rightsizing
- housing mobility
- attractive alternatives
- suitable smaller homes
- potential opportunity
- could
- may
- investigate

Avoid:
- force downsizing
- remove under-occupiers
- wasted bedrooms
- unused homes
- spare-room capacity where it implies immediate availability

## Human oversight

AI was used to accelerate:
- analysis
- code generation
- sensitivity testing
- interface development
- drafting

Human judgement remained responsible for:
- source selection
- methodology
- interpretation
- claim boundaries
- public-facing language
- final validation

## Design principle

> **AI may help identify patterns. It should not erase the human context behind them.**
