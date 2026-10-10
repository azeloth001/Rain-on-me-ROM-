# Research Findings

## Findings worth preserving

### 1. Clean passage is rare

Across the inspected router tests, strict CLEAN outcomes were commonly around 12–18%. Forecasts must begin from real climatology, not a neutral 50% assumption.

### 2. Utility and cleanliness are different

A profitable round trip can be useful without being a clean passage. V3.2f therefore used:

- CLEAN = 1.0 utility
- profitable round trip = 0.5
- other outcomes = 0

### 3. Council confidence is not outcome probability

Engine agreement describes internal coherence. It does not automatically predict a path without adverse excursion. Confidence must be calibrated against the exact outcome being claimed.

### 4. FADE often deserved attention

In early router audits, FADE frequently outperformed FOLLOW across parts of the 5m–2h range, while higher horizons could favor FOLLOW. Route behavior is scale-dependent.

### 5. The continuous 8% PHI term failed

G1 isolated Memory-only, PHI-only and Combined arms. The current additive permeability term worsened predictions across the broad test. It was rejected without changing the PHI lattice.

### 6. Short memory remained unproven

The 15% Memory arm was near-neutral and occasionally favorable. Its decay of 0.97 gives a short effective memory, so local evidence can be noisy. It remains a candidate, not production logic.

### 7. The cycle core was healthy

Cycle telemetry showed approximately:

- 100% phase validity;
- 0–4% rail contact;
- 11–21% jitter.

This did not support replacing the Ehlers/Hilbert core with an externally proposed formula.

### 8. PHI roles differ

The later labs indicated a common BTC/ETH structural DNA with symbol/regime-dependent expression. Stronger WALL priors appeared around 0.235, 0.500 and the pivot; 0.382, 0.618 and 0.728 behaved more like adaptive hinges.

### 9. Real-clock horizons matter

Fixed bar counts introduce timeframe bias. Reaction families expressed in elapsed time produced fairer cross-timeframe comparisons.

### 10. Negative evidence is valuable

H3 density gating, H4 forecast salience and the G1 8% PHI term were not promoted. Their preserved code and verdicts prevent repeated detours.

## External audit lessons

An external Gemini audit contributed hypotheses, but several claims required correction:

- bounded PHI loops were not unbounded O(history) growth;
- active audit records expired, so memory retention was not unbounded;
- a Pine user-defined type might improve maintainability but not necessarily runtime;
- the suggested Hilbert replacement mishandled phase semantics;
- Welford improves numerical stability but is not automatically a rolling statistic;
- asymmetric PHI behavior was a valuable concept, but should not deform pure geometric affinity.

