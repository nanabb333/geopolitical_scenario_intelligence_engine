# V2 Market Data Codebook

## Purpose

This codebook defines the market reaction data layer required before the US-China Strategic Competition pilot dataset can support market reaction comparison.

It is a design artifact only. It does not add market data, calculate returns, forecast outcomes, estimate probabilities, or provide investment advice.

## Why Market Data Is Needed

The V1 workbench can compare historical market reactions only when event-linked return rows exist. The V2 pilot dataset currently has coded geopolitical events but no market-return rows.

Without a V2 market data layer:

- V2 analogues cannot support market reaction comparison;
- report output would show missing return records;
- analysts could overread historical analogues without observed market context;
- integration would be weaker for portfolio manager or risk committee review.

## Event-to-Market Matching Logic

Each market row should represent one event-asset or event-index observation.

Matching sequence:

1. Confirm `event_id` exists in `data/us_china_strategic_competition_pilot.csv`.
2. Confirm the event date and event-date confidence.
3. Select the trading date convention.
4. Identify the asset, sector proxy, or index affected by the event.
5. Assign exposure role before calculating returns.
6. Select benchmark before calculating abnormal return.
7. Calculate raw return, benchmark return, and abnormal return for a defined window.
8. Add calculation notes and limitations.

## Required Fields

Required fields for future market reaction rows:

- `event_id`
- `event_date`
- `event_t0_trade_date`
- `asset_type`
- `asset_name`
- `ticker_or_index`
- `sector`
- `geography`
- `exposure_role`
- `benchmark`
- `return_window`
- `raw_return`
- `benchmark_return`
- `abnormal_return`
- `data_source`
- `calculation_notes`
- `coding_confidence`
- `limitations`

## Optional Fields

Optional fields:

- `asset_id`
- `benchmark_name`
- `benchmark_ticker_or_index`
- `currency`
- `price_adjustment`
- `trading_calendar`
- `event_date_confidence`
- `earnings_conflict`
- `macro_conflict`
- `policy_conflict`
- `liquidity_flag`
- `data_quality_flag`
- `review_status`
- `reviewer_notes`

## Field Definitions

| Field | Definition | Expected Values |
| --- | --- | --- |
| `event_id` | V2 pilot event identifier. | Existing event ID from pilot file. |
| `event_date` | Historical event date from pilot dataset. | `YYYY-MM-DD`. |
| `event_t0_trade_date` | Trading date used as event day. | `YYYY-MM-DD`. |
| `asset_type` | Type of market proxy. | `single_equity`, `sector_etf`, `index`, `adr`, `commodity`, `fx`, `rates`, `other`. |
| `asset_name` | Human-readable asset or proxy name. | Plain text. |
| `ticker_or_index` | Ticker, index code, or identifier. | Plain text. |
| `sector` | Sector represented by asset. | Controlled sector label where possible. |
| `geography` | Asset or index geography. | Country, region, or `global`. |
| `exposure_role` | Why this asset is relevant to the event. | `named_target`, `named_beneficiary`, `supplier`, `customer`, `substitute`, `sector_proxy`, `market_proxy`, `commodity_proxy`. |
| `benchmark` | Benchmark used for abnormal return. | Ticker, index, or benchmark ID. |
| `return_window` | Event window for row. | `t0`, `m1_p1`, `m3_p3`, `m7_p7`, or documented alternative. |
| `raw_return` | Observed asset return for window. | Decimal return, blank if not calculated. |
| `benchmark_return` | Observed benchmark return for window. | Decimal return, blank if not calculated. |
| `abnormal_return` | Raw return minus benchmark return. | Decimal return, blank if not calculated. |
| `data_source` | Price data source. | Vendor/source name and date if available. |
| `calculation_notes` | Method and caveats. | Plain text. |
| `coding_confidence` | Confidence in mapping and calculation. | `high`, `medium`, `low`. |
| `limitations` | Row-specific limitations. | Plain text. |

## Return Window Design

Use short windows first:

- `t0`: event-day return.
- `m1_p1`: one trading day before through one trading day after.
- `m3_p3`: three trading days before through three trading days after.
- `m7_p7`: seven trading days before through seven trading days after.

Design rules:

- Use the same window definitions across assets.
- Document non-trading-day adjustments.
- Avoid long windows unless the event has a clearly staged implementation.
- Preserve missing values when clean calculation is not possible.

## Benchmark Selection Logic

Benchmark selection must happen before returns are calculated.

Recommended hierarchy:

1. Broad market benchmark for geography.
2. Sector benchmark for asset sector.
3. Technology or semiconductor benchmark where appropriate.
4. Commodity or thematic benchmark only when it directly matches the exposure.

Benchmark choice must be documented in `calculation_notes` or a benchmark rationale field if added later.

## Sector / Asset Mapping Logic

Map assets based on exposure role:

- Named firms in event source: `named_target` or `named_beneficiary`.
- Firms in direct supply chain: `supplier` or `customer`.
- Plausible substitute beneficiaries: `substitute`.
- Broad sector comparison: `sector_proxy`.
- Broad geography comparison: `market_proxy`.
- Critical minerals exposure: `commodity_proxy` or relevant sector ETF/index.

Do not add an asset solely because it moved around the event date. Exposure must be justified before return calculation.

## Missing-Data Handling

- Leave return fields blank when not calculated.
- Use `unknown` for unresolved text values.
- Use `not_applicable` when a field does not apply.
- Explain missing data in `limitations`.
- Do not fill missing returns with zero.
- Do not infer abnormal returns without benchmark data.

## Data-Source Standards

Acceptable market data sources should be:

- reproducible;
- documented;
- adjusted for corporate actions where relevant;
- tied to a known trading calendar;
- stable enough for repeated validation.

Document:

- source name;
- access date;
- price adjustment convention;
- benchmark source;
- calculation method.

## Validation Rules

Before any populated V2 market file is used:

- every `event_id` must exist in the V2 pilot dataset;
- `event_date` and `event_t0_trade_date` must be non-empty valid dates;
- `return_window` must be controlled;
- `raw_return`, `benchmark_return`, and `abnormal_return` must be numeric or blank;
- `coding_confidence` must be `high`, `medium`, or `low`;
- no fake or placeholder returns are allowed;
- each row must include `data_source`, `calculation_notes`, and `limitations`;
- duplicate event-asset-window rows must be reviewed.

## Limitations

This codebook does not solve:

- data licensing;
- event-date ambiguity;
- benchmark disputes;
- sparse asset coverage;
- confounded event windows;
- mapping from geopolitical mechanisms to investable proxies.

It defines the data layer needed before the existing workbench can responsibly compare V2 market reactions.
