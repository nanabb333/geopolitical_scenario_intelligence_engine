# Supported Questions Boundary

## What the System Can Answer Reliably

The system can answer questions reliably when they match the current semiconductor-centered historical analogue dataset. This section describes current V1 data support, not the permanent boundary of the workflow architecture.

Strongly supported question types:

- U.S. semiconductor subsidy announcements.
- CHIPS Act preliminary award or funding scenarios.
- Semiconductor industrial policy and state-support mechanisms.
- Advanced chip export controls.
- Semiconductor-equipment export controls.
- Entity-list actions involving semiconductor or memory-chip firms.
- China retaliation against a semiconductor firm.
- State-backed fab investment linked to semiconductor supply chains.
- Historical analogue retrieval for technology-policy competition among the U.S., China, Japan, Taiwan-linked firms, and South Korea-linked firms.

Suggested reliable framing:

```text
What historical analogues are relevant if the United States announces a new semiconductor subsidy package?
```

```text
How should analysts compare new export controls on advanced AI chips against prior semiconductor restriction events?
```

## What the System Can Answer With Caution

The system can provide a partial structured response when the question is adjacent to the current dataset but not directly covered.

Partially supported question types:

- Taiwan-risk questions framed around semiconductor supply chains, foundries, or technology restrictions.
- Military escalation questions framed around export controls, sanctions, semiconductor exposure, or supply-chain restrictions.
- Strategic investment questions framed around fabs, semiconductor capacity, or state support.
- Semiconductor sanctions questions framed as entity-list, export-control, or procurement-restriction events.
- Market-reaction questions where only a subset of analogues has local return records.

Use caution because the system may retrieve semiconductor-policy analogues rather than direct analogues for the broader geopolitical event.

Suggested cautious framing:

```text
What semiconductor-policy analogues are relevant if Taiwan Strait tensions increase concern about foundry exposure?
```

```text
What technology-restriction analogues are relevant if a military escalation leads to new semiconductor export controls?
```

## What the Workflow Could Support After Dataset Expansion

The workflow architecture could support broader geopolitical risk categories after additional historical events, coding fields, and market-reaction rows are added.

Future directly supportable question types:

- Taiwan military tension, blockade-risk episodes, and military exercises.
- Shipping and maritime disruption.
- Energy security shocks.
- Critical-minerals restrictions or investment programs.
- Cyber operations with clear event dates and market channels.
- Broad sanctions beyond semiconductor entity-list cases.
- Defense industrial policy and procurement restrictions.
- AI infrastructure competition involving compute, cloud, data centers, power, and accelerators.

These categories should remain clearly labeled as future dataset expansion areas until events are coded and validated.

## What the System Should Not Answer

Some questions should remain outside system scope even after dataset expansion because they would require forecasting, investment advice, or real-time monitoring rather than deterministic historical-analogue analysis.

Unsupported question types:

- Real-time monitoring or current-news triage.
- Forecasts, probabilities, expected returns, trading signals, or investment recommendations.
- Advice about what to buy, sell, hedge, or allocate.
- Claims that a future event will produce a specific market outcome.
- Automated conclusions without analyst review.

Questions outside current data coverage should be reframed into currently supported semiconductor-policy or technology-restriction questions, or deferred until the dataset is expanded. Questions requiring forecasts, probabilities, expected returns, or investment advice should be refused or redirected to non-predictive historical context.

## Suggested User Question Framing

Use questions that name the mechanism and sector:

- "What historical analogues are relevant for a U.S. semiconductor subsidy announcement?"
- "How do prior semiconductor export-control events compare with a new advanced AI-chip restriction?"
- "What observed pathways appear in state-backed fab investment cases?"
- "What semiconductor-policy analogues are relevant if Taiwan-linked foundry risk increases?"
- "How should analysts frame an entity-list action against a memory-chip firm?"

Avoid broad questions unless the user explicitly accepts limited current-data coverage:

- "What happens if China invades Taiwan?"
- "What should investors do after a blockade?"
- "What is the probability of escalation?"
- "What stocks should benefit?"
- "How will markets react tomorrow?"

## Analyst Disclaimer Language

Use this disclaimer when presenting workbench outputs:

```text
This output is a deterministic historical-analogue report based on the repository's current local dataset. Current coverage is strongest for semiconductor industrial policy, technology restrictions, export controls, entity-list actions, and selected state-support cases from 2022-2024. It is not a forecast, probability estimate, trading signal, or investment recommendation. Questions outside the covered dataset should be reframed or treated as unsupported until additional historical cases are coded.
```

Generalized positioning language:

```text
The workflow architecture is designed to generalize across geopolitical risk domains, but V1 validation uses a semiconductor-focused historical analogue dataset. Broader risk categories require future data expansion before they should be treated as directly supported.
```
