# The ROM Journey

## 1. Why ROM was rebuilt

Rain On Me began as an ambitious Pine v4 indicator combining ATR, VPT, PSAR, SuperTrend, support/resistance, divergences, Bollinger structures, Ichimoku, trendlines, Fibonacci geometry and an information panel.

Its greatest promise was also the reason a careful rebuild was necessary: the Fibonacci lattice appeared unusually connected to price, but the surrounding legacy systems contained structural weaknesses. The early audit found broken or misleading VPT/SuperTrend/PSAR behavior, reversed divergence logic, unsafe support/resistance handling, object inefficiency, mislabeled Fibonacci information, correlated votes and repaint/indexing risk.

The original Pine v4 source is not present in this archive. Its role is documented from the project discussion; no missing source has been reconstructed or fabricated.

## 2. PHI first

V3.0a deliberately started again from geometry rather than migrating every legacy feature at once. It established confirmed previous-period anchors, three ratio families and 21 persistent levels. ROM's unusual legacy ratios—including 0.235, 0.728, 1.235 and 1.328—were preserved as an explicit family rather than silently normalized away.

The next question was not simply whether price touched a line. V3.0b introduced continuous Gaussian affinity: price could approach, enter or move through a resonance field. V3.0b1 then corrected an important human lesson: mathematically cleaner was not automatically visually better. The indicator needed to preserve its emotional readability and line hierarchy.

## 3. From signals to a Council

V3.0c separated reasoning into four families:

- Cycle
- Flow
- ATR structure
- PHI Geometry

The Council required breadth rather than allowing several correlated variants of one idea to imitate independent agreement. Thresholds, confidence, minimum family agreement and cooldown made signals sparse enough to be meaningful.

## 4. The dashboard became a laboratory

V3.0d/d1 and V3.1a/b changed the nature of development. The dashboard stopped being decoration and began to show what the model knew, how much evidence supported it and whether a result was mature.

Prospective event studies measured MFE, MAE and response in ATR units. Bayesian shrinkage and Wilson bounds prevented a handful of early successes from looking authoritative. Trend and Chop cohorts exposed regime dependence. Evidence recency allowed current behavior to matter without erasing the lifetime anchor.

## 5. Routing and outcome honesty

V3.2a introduced `FOLLOW / FADE / WAIT / LEARN`. V3.2b began freezing routes before their outcomes. V3.2c/d then forced the outcome definitions to become honest.

Ordered first passage mattered. A route could finish positive but still have failed if the adverse barrier was crossed first. Round trips needed their own identity. This removed the comforting but false habit of grading only the final candle.

## 6. The forecast humbled the system

V3.2e showed that sophistication did not equal edge. CLEAN forecasts inherited a neutral 50% prior even though strict clean passage occurred only about 12–18% of the time. Brier skill remained near or below zero; FADE often looked better than FOLLOW across parts of the intraday range.

This was a successful failure: the dashboard exposed the problem rather than letting attractive visuals hide it.

## 7. The time-coordinate repair

A long BTCUSDT 1m test failed near bar 23,965 because a weekly drawing used `bar_index`. A crypto week can span 10,080 minute candles, beyond Pine's historical coordinate buffer.

V3.2e1 moved persistent primary/secondary lines, zones, labels and the confluence beam to timestamps using `xloc.bar_time`. This preserved full D/W geometry without clipping and became a permanent integrity rule.

## 8. V3.2f became golden

Hierarchical Calibration replaced the fictional 50% prior with empirical climatology. Predictions were shrunk toward real base rates, confidence buckets were frozen at event birth, multiclass probabilities normalized correctly and strict CLEAN was separated from practical utility.

The resulting predicted CLEAN rates aligned closely with actual rates across most tested timeframes. The remaining near-zero skill versus climatology was not hidden: Council agreement still did not reliably predict a clean passage.

V3.2f therefore became the frozen golden control—not because it claimed perfect edge, but because it was stable, calibrated and honest.

## 9. G1 isolated a bad idea

V3.2g added recent action memory and directional PHI permeability. Its combined challenger lost overall. V3.2g1 separated the hypotheses into four identical-event arms.

Memory at 15% stayed near the control and remained mildly interesting. The 8% PHI term was broadly harmful, and Combined inherited that weakness. The correct response was not to blame PHI; it was to reject the encoding.

The paired laboratory—frozen predictions, Brier deltas, Welford variance and confidence intervals—was retained.

## 10. Structural PHI and reaction behavior

H1 moved from continuous permeability to event meaning: reject, accept, retest and touch. H2 studied interaction morphology. H3/H4 tested density and adaptive salience.

H5 then asked a better question: after touching PHI, does price HOLD, PASS, WHIP or STALL? It added retention, NEXT progression and dwell. This was a shift from forcing every level into a directional probability toward learning each level's behavior.

## 11. Time itself became part of the model

Fixed bar horizons mean different real durations on 1m and 4h charts. H5e/f introduced real-clock Immediate, Tactical and Structural horizons. The research supported real time—for example 1h/3h/6h—as a fairer description of reaction behavior.

The next layer described PHI personalities: WALL, GATE, MAGNET, MIXED, WEAK or EARLY. Some levels such as 0.235, 0.500 and the pivot showed stronger WALL priors; 0.382, 0.618 and 0.728 behaved more like adaptive hinges whose role changed by symbol and regime.

## 12. The practical limit

H5g reached 101,959 compiled tokens, beyond Pine's 100,256 ceiling. Strings, tables, duplicated research logic and MTF requests all contributed.

That failure clarified the architecture: production should remain lean and stable; research should be split into purpose-built artifacts. The later scale packs and PV validators follow that rule.

## 13. Human lessons

- A beautiful chart can be informative, but beauty must not conceal calibration failure.
- A model should be allowed to say `WAIT`, `LEARN` or `INCONCL`.
- Rejected hypotheses belong in the history; they prevent future developers from repeating them.
- Default settings matter when testing from Android.
- Screenshots are valuable, but frozen prospective statistics are stronger evidence.
- The latest version number is not the same thing as the production champion.

