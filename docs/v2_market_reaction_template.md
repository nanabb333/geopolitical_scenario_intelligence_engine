# V2 Market Reaction Template

Use this template for future V2 market reaction rows. It mirrors the required market data layer for US-China Strategic Competition events.

Do not populate this template with fake returns. Blank values are preferred until data is sourced and calculated.

## Template Fields

| Field | Required | Description |
| --- | --- | --- |
| `event_id` | Yes | Must match a V2 pilot event ID. |
| `event_date` | Yes | Event date from the pilot dataset. |
| `event_t0_trade_date` | Yes | Trading date used as event day. |
| `asset_type` | Yes | Single equity, index, sector ETF, commodity, ADR, or other proxy type. |
| `asset_name` | Yes | Name of asset or market proxy. |
| `ticker_or_index` | Yes | Ticker, index code, or market identifier. |
| `sector` | Yes | Sector represented by the asset or proxy. |
| `geography` | Yes | Country, region, or global exposure. |
| `exposure_role` | Yes | Event exposure role such as named target, beneficiary, supplier, sector proxy, or market proxy. |
| `benchmark` | Yes | Benchmark ticker, index, or identifier used for comparison. |
| `return_window` | Yes | Window such as `t0`, `m1_p1`, `m3_p3`, or `m7_p7`. |
| `raw_return` | Yes | Historical observed return for asset/proxy over the window. Leave blank until calculated. |
| `benchmark_return` | Yes | Historical observed benchmark return over the window. Leave blank until calculated. |
| `abnormal_return` | Yes | Raw return minus benchmark return. Leave blank until calculated. |
| `data_source` | Yes | Source used for price and benchmark data. |
| `calculation_notes` | Yes | Calculation method, trading calendar rule, and caveats. |
| `coding_confidence` | Yes | `high`, `medium`, or `low`. |
| `limitations` | Yes | Row-level limitations or missing-data caveats. |

## CSV Template

The headers-only CSV template is:

```text
data/us_china_market_reaction_template.csv
```

## Usage Rules

- Add rows only after event-date alignment and asset mapping are reviewed.
- Select benchmarks before calculating returns.
- Preserve blank return fields until real data is calculated.
- Do not add forecast, probability, expected-return, or investment-advice fields.
- Do not infer a market reaction from narrative judgment.
