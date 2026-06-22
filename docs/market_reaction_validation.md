# Market Reaction Validation

## Row Counts

Validated file:

```text
data/us_china_market_reaction_pilot.csv
```

Observed counts:

- Total rows: 14.
- Covered events: 7.
- Covered return windows: 2.
- Rows per covered event: 2.

## Missing Values

Required fields were checked for missing values:

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

Validation result: no missing values in required fields.

## Duplicate Checks

Duplicate key checked:

```text
event_id + ticker_or_index + benchmark + return_window
```

Validation result: no duplicate keys identified.

## Benchmark Checks

Observed benchmark values:

- `SPY`
- `SMH`

Validation result: benchmark field is populated for every row.

## Event Coverage Checks

Covered V2 pilot events:

- V2P001
- V2P002
- V2P003
- V2P006
- V2P007
- V2P008
- V2P011

Validation result: every market row maps to an event in `data/us_china_strategic_competition_pilot.csv`.

## Integration Assessment

The market-reaction pilot is sufficient for static documentation and methodology validation.

It is not yet sufficient for full workbench integration because:

- V2 event fields still require transformation for V1 retrieval;
- only 7 of 15 V2 events have market rows;
- only one proxy per event is included;
- confound flags are not yet systematically coded;
- no tests yet validate V2 market rows inside the workflow.

Recommendation: do not force integration. Use the dataset as a market intelligence layer pilot and proceed to a separate integration sprint only after transformation and tests are added.
