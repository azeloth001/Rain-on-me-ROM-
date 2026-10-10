# Testing Methodology

## Core integrity rules

1. Freeze a forecast before observing its outcome.
2. Score all challengers on the same event, entry, ATR, route direction and horizon.
3. Keep production behavior unchanged during research.
4. Separate overlapping raw telemetry from independent evidence.
5. Confirm actionable events at bar close.
6. Compare against a frozen empirical baseline.

## Metrics

- CLEAN rate
- practical utility (`UT`)
- Brier score
- Brier skill versus climatology
- paired challenger-minus-control squared-error delta
- 95% confidence interval for paired delta
- reliability by confidence band
- MFE, MAE and terminal response in ATR
- HOLD/PASS/WHIP/STALL reaction rates
- personality maturity and distinctiveness

## Interpreting factorial dashboards

- Lower Brier score is better.
- Negative challenger-minus-control delta is favorable.
- Positive skill is favorable.
- `AHEAD`: the entire paired interval is favorable.
- `BEHIND`: the entire paired interval is unfavorable.
- `INCONCL`: the interval crosses zero; it does not prove equality.
- Rounded dashboard scores can look equal while paired event differences are not.

## Historical test sequence

Early ROM audits commonly inspected BTCUSDT across:

`1m · 3m · 5m · 7m · 15m · 45m · 1h · 2h · 4h · 6h`

The same exchange, symbol and settings should be retained across comparisons. Normal candles should be used unless the experiment explicitly concerns synthetic candles.

## Scale-specific packs

The later research separated market scales rather than pretending one bar horizon meant the same thing everywhere.

Final fair-pack families in this archive:

- MICRO
- INTRADAY
- MACRO

Later prospective validators used frozen prior personalities and untouched future events. Positive Brier improvement means the personality model beat its baseline; sample maturity and cross-symbol consistency remain necessary before promotion.

## Limits of the evidence

- Historical recalculation is not equivalent to live forward deployment.
- Multiple timeframe inspection creates selection risk.
- One favorable timeframe cannot justify promotion.
- Pine compilation/runtime must still be confirmed inside TradingView.
- Statistical calibration does not guarantee tradable profitability after fees, slippage and execution delay.

