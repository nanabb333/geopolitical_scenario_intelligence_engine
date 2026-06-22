# Data Coverage Audit

## Executive Summary

The current dataset supports a narrow but coherent V1 validation scope: semiconductor-centered geopolitical competition scenarios from 2022-2024, especially U.S. industrial policy, CHIPS Act support announcements, export controls, entity-list actions, and selected China/Japan/Taiwan-linked semiconductor cases.

The repository can credibly demonstrate deterministic workflow automation and historical analogue retrieval within this bounded domain. The product architecture is generalizable, but the current dataset is not yet a comprehensive geopolitical risk database or broad market-intelligence system.

Current data coverage:

- `data/events.csv`: 12 coded events.
- `data/event_firm_returns.csv`: 3 event-firm return rows.
- `data/sample_user_queries.csv`: 4 sample query rows.
- Event date range: 2022-08-09 to 2024-04-25.
- Market-return date range: 2024-03-20 to 2024-04-25.

## Current Dataset Scope

The current data boundary is a dataset limitation, not necessarily an architecture limitation. The workflow stages can support broader geopolitical risk categories once additional events and market-reaction rows are coded and validated.

### Events and Cases

The workflow uses `data/events.csv` as the historical analogue dataset. It contains 12 coded events:

- 1 broad policy event.
- 5 threat-contrast events.
- 6 support events.

Covered policy subtypes:

- `legislation`
- `export_control`
- `entity_list`
- `retaliation`
- `fab_investment`
- `subsidy_award`

### Geography Covered

The coded geography is concentrated in:

- `US`
- `China`
- `Japan`
- `Japan/Taiwan`
- `US/Taiwan`
- `US/South Korea`

Taiwan appears through semiconductor-linked investment and cross-border support cases, not through a standalone Taiwan blockade, invasion, military escalation, or shipping-disruption event.

### Sectors Covered

The current event dataset covers semiconductor-related sectors:

- `semiconductors`
- `AI chips`
- `memory chips`
- `semiconductor equipment`
- `foundry`
- `defense semiconductors`

It does not currently cover broad energy, shipping, agriculture, cyber, financial sanctions, critical minerals, telecom, or defense escalation datasets beyond semiconductor-related examples. Those categories are candidates for future data expansion rather than evidence that the workflow must remain semiconductor-only.

### Market Variables Covered

The workflow uses `data/event_firm_returns.csv` for observed market-reaction comparison. It contains 3 event-firm rows linked to events `E009`, `E010`, and `E012`.

Available market variables include:

- `event_day_return`
- `ar_market_event_day`
- `ar_tech_event_day`
- `ar_sector_event_day`
- `car_market_m1_p1`
- `car_tech_m1_p1`
- `car_sector_m1_p1`
- `car_market_m3_p3`
- `car_sector_m3_p3`
- `car_market_m7_p7`
- `car_sector_m7_p7`
- `earnings_conflict`
- `macro_conflict`
- `event_window_coverage`
- `data_quality_flag`
- `calculation_notes`

All current return rows are `named_beneficiary` records with `expected_direction` coded as `positive` and `data_quality_flag` coded as `clean`.

### Fields Available for Retrieval and Comparison

Retrieval fields in `data/events.csv` include:

- event metadata: `event_id`, `event_date`, `event_name`, `event_tier`, `primary_test_eligible`
- classification fields: `event_type`, `policy_subtype`, `country_or_region`, `sector`
- strategic coding fields: `geopolitical_competition_link`, `strategic_importance`
- support and threat fields: `state_support`, `state_support_type`, `support_directness`, `support_credibility`, `threat_signal`, `opportunity_signal`
- pathway-relevant fields: `substitution_reallocation`, `anticipation_level`, `beneficiary_visibility`, `support_materiality`
- quality/context fields: `event_date_confidence`, `confound_flag_event`, `source_url`, `coding_notes`

## Supported Question Types

The current data supports questions about:

- U.S. semiconductor subsidies and CHIPS Act preliminary awards.
- Semiconductor industrial policy and state-support mechanisms.
- Export controls on advanced chips, AI chips, semiconductor equipment, and related technology restrictions.
- Entity-list actions involving semiconductor or memory-chip firms.
- China retaliation against semiconductor firms.
- Japan semiconductor-equipment export controls.
- Foundry investment and state-backed fab examples involving Japan/Taiwan and U.S./Taiwan contexts.
- Historical analogue retrieval for semiconductor-centered geopolitical competition scenarios.

These are the strongest supported questions because they align with both the classifier vocabulary and the historical event dataset.

## Partially Supported Question Types

The system can answer the following only with explicit caution:

- Taiwan-risk questions framed through semiconductor supply chains, foundries, export controls, or state support.
- Military escalation questions if they are reframed as technology restrictions, semiconductor exposure, sanctions, or export-control risk.
- Strategic investment questions if they concern semiconductor fabs, CHIPS Act support, or state-backed chip capacity.
- Sanctions questions if they are close to entity-list or technology-restriction actions.
- Market-reaction questions where only a small subset of retrieved analogues has event-firm return rows.

These questions may retrieve useful analogues, but the data does not fully cover the broader geopolitical scenario.

## Unsupported Question Types

The current dataset does not support reliable analysis of:

- Taiwan blockade, invasion, or military conflict as direct historical analogues.
- General military exercises not connected to semiconductor restrictions or technology policy.
- Shipping disruption, port closure, maritime insurance, or logistics-specific impacts.
- Energy shocks, oil and gas sanctions, food security, agriculture, or commodities.
- Cyberattacks, telecom infrastructure, financial sanctions, sovereign debt, or banking restrictions.
- Broad defense-market reactions outside semiconductor-specific defense supply chains.
- Real-time monitoring, current-news triage, or newly unfolding events.
- Forecasts, probabilities, expected returns, investment recommendations, or trading signals.

## Coverage Gaps

- Small event count: 12 coded events limit retrieval depth and scenario diversity.
- Sparse return coverage: only 3 event-firm return rows are available.
- Narrow time period: events run from 2022-08-09 to 2024-04-25.
- Narrow sector coverage: semiconductor-centered cases dominate the dataset.
- Limited geography: coverage centers on the U.S., China, Japan, Taiwan-linked cases, and South Korea-linked support.
- No direct Taiwan military-conflict cases: Taiwan is represented through semiconductor-linked investment and support cases.
- No broad sanctions dataset: entity-list and export-control cases exist, but comprehensive sanctions coverage does not.
- No non-semiconductor market coverage: current market variables focus on selected semiconductor beneficiaries.
- Limited exposure roles: return rows currently cover named beneficiaries only.

## Product Risk

The main product risk is overclaiming. The workflow is credible as a deterministic analyst productivity platform, but current V1 evidence should be described as semiconductor-validated rather than broadly validated across all geopolitical domains.

Specific risks:

- Users may ask broad geopolitical questions that the data cannot support.
- Taiwan-risk examples may imply blockade or conflict coverage that does not exist in the dataset.
- Market-reaction summaries may appear more comprehensive than they are because only 3 return rows exist.
- Similarity scores may be misread as confidence or probability rather than deterministic retrieval scores.
- Recruiters may expect broader coverage if the README does not clearly state the supported question boundary.

## Recommended Data Expansion Priorities

If the project is expanded after freeze, broader geopolitical risk coverage should be added through coded data before feature work. Prioritize:

1. Direct Taiwan-risk events: military exercises, blockade-risk episodes, shipping disruptions, and Taiwan Strait escalation cases.
2. Additional semiconductor restriction cases: more export-control rounds, entity-list actions, procurement restrictions, and allied policy responses.
3. More market-return rows: expand event-firm coverage across beneficiaries, constrained firms, substitutes, suppliers, and customers.
4. Additional geographies: EU, South Korea, Netherlands, and other semiconductor-equipment or supply-chain jurisdictions.
5. Wider exposure roles: named beneficiaries, restricted firms, upstream suppliers, downstream customers, substitute beneficiaries, and market benchmarks.
6. Energy security, critical minerals, cyber operations, sanctions, defense industrial policy, and AI infrastructure competition as structured new event families.

## Freeze Recommendation

The repository remains freeze-ready if its scope is stated clearly.

Freeze with this boundary: the system is a general geopolitical intelligence workflow platform currently validated on a semiconductor-focused historical analogue dataset. It is not yet broadly validated across all geopolitical risk domains.

Before portfolio presentation, reviewers should treat Taiwan blockade, broad military escalation, shipping disruption, energy, cyber, and general sanctions examples as partially supported or unsupported by current data unless reframed around semiconductor policy and technology restrictions. Future dataset expansion can move these categories into direct support.
