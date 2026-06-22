# US-China Market Reaction Pilot Dataset

## Event Coverage

`data/us_china_market_reaction_pilot.csv` contains a small market-reaction pilot for seven selected US-China Strategic Competition events.

Covered events:

| Event ID | Category | Event |
| --- | --- | --- |
| V2P001 | Industrial Policy | CHIPS and Science Act signed |
| V2P002 | Export Controls | BIS advanced computing and semiconductor manufacturing export controls |
| V2P003 | Sanctions / Entity List | YMTC and other Chinese entities added to Entity List |
| V2P006 | Critical Minerals | China announces gallium and germanium export controls |
| V2P007 | Strategic Investment Screening | US executive order on outbound investment in sensitive technologies |
| V2P008 | AI Chip Restrictions | BIS updates advanced computing and semiconductor export controls |
| V2P011 | Supply Chain Relocation | TSMC Arizona CHIPS preliminary terms announced |

The pilot includes two return windows for each event:

- `t0`
- `m3_p3`

Total rows: 14.

## Asset Coverage

The pilot uses one market proxy per event.

| Proxy | Role |
| --- | --- |
| SMH | Semiconductor sector proxy |
| MU | Memory-chip peer or substitute proxy |
| PICK | Broad metals and mining proxy for critical-minerals exposure |
| QQQ | Broad technology proxy |
| NVDA | Named AI-chip exposed equity |
| TSM | Named foundry and supply-chain relocation proxy |

Proxy choices are designed for a first market-reaction pilot. They are not definitive exposure models.

## Benchmark Coverage

Benchmarks used:

- `SPY`: broad US market benchmark.
- `SMH`: semiconductor sector benchmark for firm-level semiconductor or AI-chip proxies.

Benchmark choice was assigned before calculating abnormal returns.

## Methodology

Returns were calculated from Yahoo Finance chart endpoint adjusted close data fetched on 2026-06-22.

Calculation convention:

- `event_t0_trade_date`: first trading day on or after the coded event date.
- `t0`: close-to-close return from the prior trading day to `event_t0_trade_date`.
- `m3_p3`: close-to-close return from three trading days before through three trading days after `event_t0_trade_date`, implemented as close at `t+3` divided by close at the trading day before `t-3`, minus one.
- `abnormal_return`: `raw_return - benchmark_return`.

The data source was used only to create this static pilot dataset. No live market feed or product API was added to the repository.

## Limitations

- This is a small pilot, not a comprehensive market dataset.
- It includes only seven events and one proxy per event.
- Some proxies are indirect because direct target assets are not publicly traded or not easily isolated.
- No event-window confound review has been completed.
- Broad policy events may be anticipated before the event date.
- The dataset does not forecast returns, estimate probabilities, or recommend trades.
- The V2 pilot is not yet integrated into the V1 workbench.

## Data Quality Assessment

Current quality assessment:

- Row count: 14.
- Event coverage: 7 of 15 V2 pilot events.
- Window coverage: 2 windows per covered event.
- Missing return values: none.
- Duplicate event/proxy/window rows: none identified.
- Source consistency: all rows use Yahoo Finance adjusted close data.
- Coding confidence: `high` for clearer named or sector-mapped events; `medium` for broad policy or imperfect proxy mappings.

This market layer is sufficient for a static pilot dataset and portfolio demonstration of market-reaction data design. It is not yet sufficient for full V2 workbench integration.
