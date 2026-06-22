# Generalization Strategy

## Product Vision

Geopolitical Intelligence Analyst Copilot is a general geopolitical intelligence workflow platform for turning analyst questions into structured, evidence-based intelligence briefs.

The V1 product demonstrates the workflow locally and deterministically:

```text
Question
  -> Scenario Classification
  -> Historical Analogue Retrieval
  -> Market Reaction Comparison
  -> Observed Pathways
  -> Executive Memo
  -> Markdown Export
```

The long-term product vision is broader than semiconductors. The current validation dataset is semiconductor-focused because it provides a coherent, auditable first domain for proving the workflow.

## Current Validation Scope

Current validation is strongest for semiconductor-centered geopolitical competition from 2022-2024:

- semiconductor industrial policy;
- CHIPS Act support announcements;
- semiconductor subsidy awards;
- export controls;
- entity-list actions;
- semiconductor-equipment restrictions;
- selected China/Japan/Taiwan-linked semiconductor cases.

This is a validation scope, not a permanent product boundary.

## Difference Between Product Architecture and Dataset Coverage

Product architecture refers to the workflow design and orchestration:

- classify a scenario;
- retrieve historical analogues;
- compare observed market reactions;
- generate observed pathways;
- produce an executive memo;
- export Markdown.

Dataset coverage refers to the historical events and market rows currently available for retrieval and comparison.

The architecture is generalizable because it uses structured event fields and modular workflow stages. The current dataset is narrow because only a limited set of semiconductor-centered historical events has been coded.

This distinction is critical for portfolio communication:

- Do say the workflow platform is generalizable.
- Do say V1 is validated on a semiconductor-focused dataset.
- Do not say the current data supports all geopolitical risk domains.
- Do not describe unsupported categories as if direct analogues already exist.

## How to Avoid Overclaiming

Use precise claims:

- "Currently validated on semiconductor-centered geopolitical competition."
- "Designed to generalize as additional event categories are coded."
- "Supports structured scenario analysis using the available historical analogue dataset."
- "Current data coverage is strongest for semiconductor policy, export controls, and technology restrictions."

Avoid broad claims:

- "Covers geopolitical risk."
- "Analyzes Taiwan blockade risk."
- "Predicts market reactions."
- "Identifies investment opportunities."
- "Monitors real-time events."
- "Supports all sanctions, energy, cyber, or military scenarios."

When handling unsupported questions, reframe them:

- Broad Taiwan blockade question -> semiconductor foundry exposure and technology-policy analogue question.
- Broad sanctions question -> entity-list or export-control analogue question.
- Broad military escalation question -> technology-restriction or supply-chain-risk analogue question.

## How Future Data Expansion Improves the Product

Future data expansion increases the range of questions that the same workflow can support.

Adding new event categories would improve:

- classification coverage;
- analogue retrieval depth;
- pathway diversity;
- market-reaction comparison across sectors;
- recruiter credibility for broader risk analytics roles;
- product realism for strategy, risk, and business analytics review.

Expansion should start with historical data, not new features. The next product risk is not lack of UI or model complexity; it is insufficient event coverage for broad claims.

## Recommended Language for README

Recommended short language:

```text
Geopolitical Intelligence Analyst Copilot is a general geopolitical intelligence workflow platform currently validated on a semiconductor-focused historical analogue dataset.
```

Recommended scope language:

```text
The V1 architecture is designed to generalize across geopolitical risk domains, but the current data coverage is strongest for semiconductor industrial policy, export controls, entity-list actions, and selected technology-restriction cases from 2022-2024. Broader categories such as Taiwan military tension, energy security, shipping disruption, critical minerals, cyber operations, sanctions, and defense industrial policy require future dataset expansion before they should be treated as directly supported.
```

Recommended boundary language:

```text
The system supports deterministic decision support using coded historical analogues. It does not forecast, estimate probabilities, produce expected returns, recommend trades, or monitor real-time events.
```
