# Scenario Intelligence Layer

The Scenario Intelligence Layer describes how the product should think about analyst questions before producing an executive memo.

It does not change workflow logic. It clarifies the product interpretation layer that sits above the same deterministic workbench.

## Intelligence Flow

```text
Question
  -> Scenario Family
  -> Historical Analogues
  -> Market Evidence
  -> Observed Pathways
  -> Current Relevance
  -> Executive Memo
```

## Question

The analyst starts with an unstructured question. The question may include a policy action, geography, sector, firm, event type, or risk mechanism.

The product should preserve the question while identifying the scenario family that best organizes it.

## Scenario Family

Scenario family groups the question into a reusable analytical frame.

Examples:

- Technology Competition
- Industrial Policy
- Economic Security
- Resource Competition
- Supply Chain Risk
- Strategic Competition

Scenario families make the workflow question-centric rather than event-centric.

## Historical Analogues

Historical analogue retrieval identifies prior events that share classification, policy, sector, geography, or text-overlap features.

Analogues are evidence inputs, not predictions.

## Market Evidence

Market evidence summarizes observed historical return windows where sourced market rows exist.

It should disclose:

- covered events;
- covered proxies;
- benchmark logic;
- missing market rows;
- calculation caveats.

## Observed Pathways

Observed pathways convert retrieved analogues and coded features into analyst-review frames.

Examples:

- restriction pathway;
- state-support pathway;
- reallocation pathway;
- anticipation pathway.

Pathways are not forecasts.

## Current Relevance

Current relevance explains why the historical evidence may or may not apply to the current analyst question.

It should compare:

- historical similarity;
- structural similarity;
- policy similarity;
- sector exposure;
- market evidence;
- data limitations.

## Executive Memo

The executive memo packages the analysis for portfolio manager, risk committee, strategy team, or portfolio-review use.

It should include:

- concise bottom line;
- relevant analogues;
- market evidence if available;
- observed pathways;
- caveats;
- unsupported question boundaries.

It must not include forecasts, probabilities, expected returns, or investment advice.
