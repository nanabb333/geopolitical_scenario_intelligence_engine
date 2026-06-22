# US-China Strategic Competition Pilot Dataset Summary

## Executive Summary

`data/us_china_strategic_competition_pilot.csv` is a schema-governed V2 pilot dataset for future expansion of Geopolitical Intelligence Analyst Copilot.

The pilot contains 15 real historical events adjacent to the current semiconductor-centered V1 dataset but broader than semiconductors alone. It is designed to test whether the V1 workflow architecture can later generalize into a broader US-China strategic competition dataset without adding product features or changing retrieval logic during this sprint.

This dataset is not currently wired into the V1 workflow. It is a data architecture and coverage-expansion artifact.

## Dataset Scope

The pilot focuses on US-China strategic competition mechanisms:

- export controls;
- sanctions and entity-list actions;
- AI chip restrictions;
- semiconductor and technology industrial policy;
- strategic investment screening;
- critical minerals;
- supply-chain relocation;
- Taiwan-related tension as one subcategory only.

The dataset avoids forecasts, probabilities, expected returns, trading signals, and investment recommendations.

## Categories Covered

| Category | Event Count |
| --- | ---: |
| AI Chip Restrictions | 2 |
| Critical Minerals | 3 |
| Export Controls | 2 |
| Industrial Policy | 2 |
| Sanctions / Entity List | 2 |
| Strategic Investment Screening | 2 |
| Supply Chain Relocation | 1 |
| US-China Strategic Competition Pilot Dataset | 1 |

The Taiwan-related event is coded under the pilot umbrella with subcategory `taiwan_related_tension` so that Taiwan remains part of the broader US-China strategic competition frame rather than the central product narrative.

## Time Period Covered

The pilot covers events from 2022-08-09 through 2024-12-02.

This period extends the current V1 validation period and includes several policy updates that are useful for future data-expansion planning.

## Inclusion Criteria

Events were included when they met these conditions:

- clear US-China strategic competition relevance;
- identifiable event date;
- credible public source;
- plausible market, sector, supply-chain, security, or strategic relevance;
- fit with V2 schema fields;
- adjacent to the current semiconductor validation dataset or useful for broader expansion.

## Exclusion Criteria

Events were excluded or deferred when they required:

- forecasting future outcomes;
- probability estimates;
- investment recommendations;
- unsupported market-impact claims;
- invented or weakly sourced facts;
- broad geopolitical interpretation without a clear event trigger.

## Coverage Strengths

- Expands beyond the current semiconductor dataset while staying adjacent to V1.
- Covers multiple US-China competition mechanisms rather than one event family.
- Includes both US actions and China-side responses.
- Adds critical minerals and strategic investment screening as broader risk categories.
- Keeps Taiwan-related tension as a subcategory rather than a dominant frame.
- Uses source URLs and coding notes for every event.

## Coverage Gaps

- The pilot is still small and should not be treated as comprehensive.
- Market-return rows were not added.
- Some rows rely on major media rather than normalized official sources.
- Supply-chain relocation is represented by a semiconductor-linked case, not broad relocation coverage.
- Taiwan-related tension is represented by one event only.
- Energy security, cyber operations, shipping disruption, and defense industrial policy are not meaningfully covered in this pilot.

## How This Extends V1

V1 is validated on semiconductor-centered historical analogues. This V2 pilot extends the data architecture toward broader US-China strategic competition by adding:

- critical-minerals controls;
- outbound investment screening;
- China-side industrial policy;
- China-side procurement restriction;
- newer AI-chip restriction events;
- a Taiwan-related tension example as a subcategory.

It preserves the V1 architecture and does not modify source logic.

## Product Implications

The pilot supports the product positioning that Geopolitical Intelligence Analyst Copilot is a generalizable workflow platform currently validated on a narrower dataset.

The next product step should be data review and schema validation, not new UI, LLM integration, forecasting, or report-generation changes.

## Limitations

- The pilot is not production-ready.
- Category labels may require review after additional rows are coded.
- Some event dates represent announcements, while others represent final rules or implementation milestones.
- The dataset does not yet support robust market-reaction comparison.
- The V1 classifier and retriever are not modified to consume this file.
- No claims should be made that the current workflow already supports all US-China strategic competition questions.
