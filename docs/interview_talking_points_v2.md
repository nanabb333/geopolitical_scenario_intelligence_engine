# Interview Talking Points V2

## What the Project Is

Geopolitical Intelligence Analyst Copilot is a deterministic workflow platform that turns geopolitical risk questions into structured intelligence briefs.

It combines scenario classification, historical analogue retrieval, market evidence where available, observed pathways, and executive memo generation.

## Why It Was Built

The project was built to show how ambiguous geopolitical risk questions can be converted into a reproducible analyst workflow.

The goal is analyst productivity and decision support, not prediction or investment advice.

## Biggest Challenge

The biggest challenge was managing scope honestly.

The workflow architecture is generalizable, but the data coverage is narrower. The project addresses that by documenting data coverage, supported question boundaries, V2 schema design, and integration readiness before claiming broader capability.

## Why Question-Centric Design Matters

Analysts start with questions, not event IDs.

Question-centric design makes the product easier to understand because it maps:

```text
Question -> Scenario Family -> Evidence -> Memo
```

This improves usability and recruiter readability.

## Why Market Evidence Was Added

Historical analogues alone are useful but incomplete. The market-reaction pilot adds observed historical return context for selected events.

The market layer remains descriptive. It does not forecast outcomes, estimate probabilities, or recommend investments.

## Lessons Learned

- Product credibility depends on clear scope boundaries.
- Data coverage matters as much as workflow design.
- Market evidence must be tied to documented proxies and benchmarks.
- A useful analytics product can be deterministic and still valuable.
- Portfolio reviewers need a fast path through the repo.

## Future Roadmap

Recommended future steps:

1. Keep V1 workflow stable.
2. Validate V2 field transformations.
3. Expand US-China strategic competition data coverage.
4. Add tests for V2 market rows.
5. Integrate V2 only after mapping and validation are complete.

Do not add LLMs, APIs, forecasts, dashboards, or investment advice before the data layer is ready.
