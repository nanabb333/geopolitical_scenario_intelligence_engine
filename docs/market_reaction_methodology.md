# Market Reaction Methodology

## Return Windows

The V2 market reaction pilot uses short historical event windows.

| Window | Definition |
| --- | --- |
| `t0` | Close-to-close return from the prior trading day to the event trading day. |
| `m3_p3` | Close-to-close return from three trading days before through three trading days after the event trading day. |

The event trading day is the first trading day on or after the coded event date.

## Benchmark Logic

Benchmarks are selected before calculating returns.

Current benchmark choices:

- `SPY` for broad US market comparison.
- `SMH` for firm-level semiconductor or AI-chip comparisons.

Benchmark choice is intentionally simple for the pilot. Future versions may add regional, sector, commodity, or thematic benchmarks after proxy rules are reviewed.

## Abnormal-Return Logic

The pilot uses a simple historical comparison metric:

```text
abnormal_return = raw_return - benchmark_return
```

This is not a forecast, expected return, probability estimate, or investment signal. It is a descriptive event-window comparison.

## Assumptions

- Adjusted close data is appropriate for pilot-level historical return calculation.
- The first trading day on or after the event date is the event trading day.
- One proxy per event is sufficient for an initial market-reaction pilot.
- Short windows reduce, but do not eliminate, confounding risk.
- Benchmark selection should be documented before return calculation.

## Limitations

- Some geopolitical events unfold across multiple dates.
- Policy actions may be anticipated before the coded event date.
- Broad market, earnings, macro, and sector news can confound returns.
- Proxy assets may not perfectly represent event exposure.
- Critical-minerals exposure is difficult to isolate through broad market proxies.
- The pilot does not include event-firm rows for all V2 events.

## Reproducibility Notes

The pilot was calculated from Yahoo Finance chart endpoint adjusted close data fetched on 2026-06-22.

For each row, `calculation_notes` records:

- adjusted close-to-close convention;
- event window;
- asset start and end dates;
- benchmark start and end dates;
- event trading day convention.

Future reproducibility hardening should add:

- a checked-in calculation script;
- data-source access notes;
- benchmark rationale fields;
- event-window confound flags;
- tests for row-level calculations.
