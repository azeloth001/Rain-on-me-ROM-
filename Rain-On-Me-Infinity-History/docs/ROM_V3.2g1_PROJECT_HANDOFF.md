# Rain On Me ∞ (ROM) — Project Handoff

**Handoff state:** after V3.2g1 Factorial Adaptive Lab testing  
**Target:** TradingView Pine Script v6, primarily BTCUSDT/ETHUSDT scalping and multi-timeframe context  
**Production champion:** `Rain_On_Me_INFINITY_V3.2f_Hierarchical_Calibration.pine`  
**Latest research build:** `Rain_On_Me_INFINITY_V3.2g1_Factorial_Adaptive_Lab.pine`

---

## 1. What this project is trying to become

ROM is not intended to be a generic indicator bundle. Its goal is to combine:

- mathematically faithful PHI/Fibonacci price geometry;
- explainable, non-repainting multi-family market reasoning;
- evidence-calibrated FOLLOW/FADE/WAIT/LEARN routing;
- prospective testing that freezes every prediction before the future outcome;
- a beautiful, readable chart that remains useful on mobile;
- scientific dashboards that expose weaknesses instead of hiding them.

The user values both **signal potential and visual soul**. New mathematics must not casually deform the PHI lattice, destroy the Aurora/Ocean visual identity, or turn the dashboard into repetitive clutter.

Core working principle: every new idea is a **challenger** first. It must be measured on the same frozen events as the trusted control before it is allowed to change production signals.

---

## 2. Current branch discipline

### Golden production/control branch

**V3.2f — Hierarchical Calibration** is the current golden reference.

Do not modify it in place. Do not promote a later experiment merely because it sounds more sophisticated.

V3.2f has already passed:

- TradingView loading from 1m through 6h;
- plot-budget checks (27 plot-bearing calls, below 64);
- long-history 1m testing without the old buffer failure;
- calibrated CLEAN probabilities close to actual CLEAN rates;
- stable time-based D/W geometry;
- visual and signal-behavior checks.

### Latest research branch

**V3.2g1 — Factorial Adaptive Lab** is observational research only.

It contains four forecasts evaluated on identical independent events:

| Arm | Memory | PHI term | Purpose |
|---|---:|---:|---|
| C — Control | 0% | 0% | Frozen V3.2f-compatible forecast |
| M — Memory | 15% | 0% | Short-memory FOLLOW/FADE adaptation |
| P — PHI | 0% | 8% | Current directional permeability hypothesis |
| X — Combined | 15% | 8% | Memory plus current PHI hypothesis |

The challengers cannot alter routes, signals, drawings, alerts, or candle colors.

---

## 3. V3.2g1 screenshot verdict

The ten-timeframe Factorial Lab pass is decisive enough to choose the next direction.

### Final verdict

- **V3.2f remains GOLDEN.** Nothing in G1 deserves promotion to live logic yet.
- **Memory-only (M15/0) is safe and mildly interesting, but not proven.** It generally remained near the control and did not show robust cross-timeframe superiority. Preserve it as a research candidate.
- **PHI-only (P0/8) is rejected in its current form.** The 8% permeability adjustment was broadly harmful rather than a reliable improvement.
- **Combined (X15/8) is also rejected.** It inherits the PHI arm's weakness; memory does not rescue it.
- The experiment itself succeeded: matched events, paired Brier-score differences, Welford variance, and 95% intervals are valuable infrastructure and should be retained.

### How to read the dashboard correctly

- Lower Brier score is better.
- For challenger-minus-control paired error, negative delta is favorable.
- Positive skill percentage is favorable.
- `AHEAD` means the paired 95% interval is entirely favorable.
- `BEHIND` means it is entirely unfavorable.
- `INCONCL` means the interval crosses zero; it is not evidence of equality.

Do not overreact to rounded Brier values that look identical. The paired event-level delta and its interval are more informative than three-decimal displayed averages.

### What G1 taught us

The current PHI term is not testing rich PHI behavior. It compresses geometry, pressure, side, and route direction into one additive probability nudge. That is too crude and can cancel or reverse the intended meaning. The failure does **not** show that PHI geometry lacks predictive information. It shows that this particular permeability encoding and 8% strength are unsuitable.

The memory arm is also not genuine multidimensional regime conditioning. It mostly represents short-memory adaptation by action (FOLLOW versus FADE), with decay 0.97 and a maximum 15% blend. Its effective recent sample is small, so it should remain conservative until it proves a repeated advantage.

---

## 4. Important version history and discoveries

### V3.0a–V3.1b: foundation and evidence integrity

- Built the PHI lattice, spectral resonance field, Signal Council, dashboard intelligence, evidence calibration, and integrity controls.
- Four independent council families: Cycle, Flow, ATR, and PHI Geometry.
- Added Trend/Chop cohorts, Bayesian shrinkage, Wilson bounds, evidence maturity, recency weighting, MFE/MAE in ATR, and bar-close event gating.

### V3.2a–V3.2d: router and outcome integrity

- Added FOLLOW/FADE/WAIT/LEARN routing.
- Added prospective router auditing with forecasts frozen at event birth.
- Repaired outcome taxonomy and introduced ordered first passage.
- CLEAN means the favorable barrier occurs first, the adverse barrier is not reached, and the terminal close confirms the route.
- Profitable round trips are kept separate from strict CLEAN outcomes.

### V3.2e: forecast-skill audit

The first full audit exposed poor calibration:

- CLEAN base rates were only around 12–18%, but forecasts began from an unrealistic 50% prior.
- Brier skill was slightly negative across timeframes.
- FADE often outperformed FOLLOW between approximately 5m and 2h.
- Round trips were frequently damaging.
- Council confidence did not map monotonically to strict clean-passage probability.

### V3.2e1: critical 1m history repair

TradingView failed around bar 23,965 because a weekly secondary PHI drawing used `bar_index`. A crypto week can contain 10,080 one-minute bars, exceeding Pine's historical coordinate buffer.

The repair converted persistent geometry to timestamp coordinates (`xloc.bar_time`) for:

- primary and secondary PHI lines;
- ATR resonance zones;
- level labels;
- MTF confluence beam.

Never restore long-anchor drawings to historical `bar_index` coordinates.

### V3.2f: successful hierarchical calibration

V3.2f replaced the fixed 50% CLEAN prior with frozen empirical climatology and shrinkage toward the genuine base rate.

It added or formalized:

- adaptive confidence buckets frozen at event birth;
- normalized five-class outcome probabilities;
- strict CLEAN probability and separate practical utility (`UT`);
- utility: CLEAN = 1.0, profitable round trip = 0.5, other outcomes = 0;
- `BASE` learned climatology;
- Brier skill versus frozen baseline;
- FOLLOW/FADE horizon curves;
- reliability diagnostics.

Observed calibration improved dramatically. On six of eight inspected timeframes, predicted CLEAN was within 0–1 percentage point of actual CLEAN. CLEAN remained naturally rare (about 12–18%); UT was higher (about 18–24%).

Remaining weakness: the action/confidence model did not consistently beat climatology (`SK` around zero), and high Council agreement was not the same as high CLEAN probability.

### V3.2g: first adaptive challenger

Added recent-regime memory, a directional PHI adjustment, cycle-health diagnostics, and Welford moments while leaving production behavior frozen.

Across six inspected timeframes, the challenger was approximately 1.6% worse in descriptive weighted skill overall. Only 1m showed a small gain; most other timeframes lost or tied.

Cycle diagnostics were healthy:

- phase validity: 100%;
- rail contact: about 0–4%;
- jitter: roughly 11–21%.

Therefore the proposed replacement of the Ehlers/Hilbert core was not justified.

### V3.2g1: clean factorial isolation

Separated Memory-only, PHI-only, and Combined challengers on the exact same events and added paired Brier differences with 95% intervals. This made it possible to reject the faulty PHI term without discarding the potentially useful memory idea.

---

## 5. Current architecture and defaults that matter

### Geometry

- Primary anchor: D
- Secondary anchor: W
- Ratio family: ROM Legacy
- Range: Previous Range
- Zone half-width: 0.08 ATR
- Confluence distance: 0.22 ATR
- Resonance radius: 0.85 ATR
- Approach radius: 3.0 zones
- Acceptance buffer: 0.35 zone
- Retest memory: 40 bars

### Engines

- Dominant-cycle trend uses confirmed MTF values by default.
- Trend deadband: 0.06 ATR.
- Pressure lengths: 14 / 28 / 34 / 8.
- ATR trail: length 14, multiplier 2.0.
- Council preset: Balanced.
- Council trigger / strong: 0.42 / 0.68.
- Minimum agreement: 3 of 4 families.
- Minimum Council confidence: 0.52.
- Council cooldown: 8 bars.
- PHI-event memory: 13 bars.

### Research

- Horizon: 20 bars.
- Success target: 0.60 ATR.
- Excursion envelope: 3.0 × square-root horizon.
- Developing evidence: 12 samples.
- Trusted evidence: 55 samples.
- Neutral prior strength: 8.
- Evidence decay: 0.97.
- Edge probability: 0.60.

### Router

- Mode: Advisory.
- Minimum cohort samples: 20.
- Minimum edge: 0.10 ATR.
- Confirmation confidence: 0.30.
- Route memory: 20 bars.
- Auditor: enabled.
- Terminal confirmation: 0.10 ATR.

### G1 research defaults

- Adaptive regime decay: 0.97.
- Memory blend: 0.15.
- PHI permeability weight: 0.08.
- Display: Research Lab.
- Theme: Ocean Deep.
- Dashboard: Research → Adaptive Lab.
- Confirmed events only: On.

These zero-setup research defaults were intentional so the user only needed to change timeframes and capture screenshots.

---

## 6. Design preferences and non-negotiable constraints

- Pine Script v6.
- Non-repainting/confirmed behavior where an event becomes actionable.
- Preserve V3.2f unchanged as a fallback/control.
- Never train on an event before scoring its frozen prediction.
- No future leakage; buckets and probabilities are frozen at event birth.
- Compare challengers on identical events.
- Use paired statistics where possible.
- Keep lifetime evidence as stability anchor; recent evidence may supplement, not erase it.
- Do not deform symmetric PHI geometry to make a flow hypothesis look intelligent.
- Keep geometry and directional reaction/permeability as separate concepts.
- Preserve timestamp-based long-anchor drawings.
- Maintain mobile readability and avoid repeated dashboard information.
- Preferred visual style: Aurora/Ocean Deep, gradual multi-stop spectral colors, smooth candle transitions, elegant line hierarchy, strong but controlled aura.
- The user works heavily from Android, so defaults and zero-setup test builds matter.
- Test primarily on BTCUSDT, same exchange across screenshots; ETHUSDT is also important.
- Main trading focus is 1–5m scalping, but 15m/45m/1h/2h/4h/6h context is deliberately inspected.

---

## 7. External Gemini audit: accepted and rejected ideas

Gemini's audit was treated as hypotheses, not authority.

### Retain or explore

- Welford variance: retained for numerical stability.
- Lifetime versus recent memory: valid research direction, but must be conservatively weighted and tested.
- Directional PHI behavior: valuable concept, but it must be modeled separately from geometric affinity.
- Adaptive ATR: possible future challenger only, with bounded multipliers, smoothing, and hysteresis.
- User-defined `AuditRecord` type: useful future maintainability refactor after behavior is frozen.

### Rejected or corrected

- Fibonacci loops were not the claimed unbounded performance problem; drawing loops are first/last-bar gated and per-bar work is bounded.
- Audit memory was not unbounded; statistics use fixed counters/sums and active records expire at the horizon.
- Gemini's proposed Hilbert replacement was mathematically flawed and is not supported by healthy cycle telemetry.
- A UDT rewrite is not assumed to improve runtime and should not be mixed with a mathematical release.
- Welford alone is lifetime streaming variance, not a rolling window; recency requires weighted Welford or an explicit window.

---

## 8. Recommended next experiment

Do **not** tune the failed 8% PHI term blindly.

The clean next branch should be a small, observational **structural-PHI challenger** built on G1's paired infrastructure while V3.2f remains the frozen control.

### Hypothesis

PHI predictive value may live in the **event meaning**, not in a continuous pressure-based deformation.

Use confirmed PHI event semantics:

- `REJECT`
- `ACCEPT`
- `RETEST`
- `TOUCH`

Map each event to FOLLOW or FADE only according to its actual structural meaning and learned evidence. Keep the maximum probability influence very small initially (about 2%), rather than repeating the failed 8% additive nudge.

### Experimental arms

- Control: V3.2f-compatible frozen probability.
- Memory: existing 15% short-memory arm.
- Structural PHI: event-semantic PHI arm at a 2% cap.
- Combined: Memory + Structural PHI.

All arms must:

- share the same independent events, entry, ATR, direction, and horizon;
- freeze probabilities before the future path;
- report paired Brier deltas and 95% intervals;
- remain observational;
- leave live routes, signals, drawings, alerts, and candle colors unchanged.

### Decision rule

Promote nothing after one attractive timeframe. Require coherent cross-timeframe behavior, adequate sample maturity, and a paired interval that supports genuine improvement. If structural PHI is still harmful at 2%, retire that encoding and change the research question rather than repeatedly shrinking a bad additive term.

---

## 9. Known statistical cautions

- CLEAN is a strict event and its base rate is low; raw accuracy can be misleading.
- Brier score should be compared with frozen climatology and between paired arms.
- A dashboard deadband is not a statistical test.
- `INCONCL` means insufficient separation, not proof that models are equal.
- Rounded dashboard scores can hide small paired differences.
- Historical multi-timeframe screenshots are useful development evidence, but they are not equivalent to an out-of-sample forward deployment.
- An experiment must not be promoted merely because one timeframe is favorable.
- Council confidence measures engine agreement; it is not automatically a calibrated probability of clean passage.

---

## 10. Source integrity

Local source hashes at handoff:

```text
V3.2f  dab08cd6b6886085f61d50592e2836340050786dde09bd730b2829a699015cc1
V3.2g1 5330f8e2f09d54d0ccda07e5613a41d7e0acd1ec78c86158f4a5c70b2da322b8
```

V3.2g1 source length: 2,435 lines.

Do not reconstruct either file from this summary. Use the actual `.pine` file as source of truth.

---

## 11. Suggested opening message for the new chat

> We are continuing my TradingView Pine v6 project, Rain On Me ∞. Read the attached project handoff and the complete V3.2g1 source before proposing or changing code. V3.2f is the frozen golden production/control branch. V3.2g1 is a research-only factorial lab. The latest ten-timeframe test rejected the current 8% PHI permeability arm and its Combined arm; Memory 15% is safe/interesting but not proven. Preserve the paired same-event Brier/CI infrastructure, time-safe `xloc.bar_time` geometry, visuals, and production behavior. The next experiment should test structural PHI event semantics (`REJECT/ACCEPT/RETEST/TOUCH`) at a small 2% cap as an observational challenger. First audit the handoff and source, then state the exact experimental design before editing.

---

## 12. Files to attach in the new chat

Required:

1. `ROM_V3.2g1_Project_Handoff.md`
2. `Rain_On_Me_INFINITY_V3.2g1_Factorial_Adaptive_Lab.pine`

Recommended golden fallback:

3. `Rain_On_Me_INFINITY_V3.2f_Hierarchical_Calibration.pine`

The screenshots are useful supporting evidence, but the handoff contains their decision-level conclusion, so they do not all need to be uploaded again unless the new model wants to re-read exact displayed numbers.
