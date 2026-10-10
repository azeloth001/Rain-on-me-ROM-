# Rain On Me ∞

An evolution archive of a large TradingView Pine Script v6 research project built around PHI/Fibonacci geometry, multi-engine market reasoning, prospective calibration and mobile-readable visual design.

This repository is intentionally both a code archive and a research diary. It preserves successful releases, failed hypotheses and the reasoning that connected them.

## Start here

- Current golden production/control build: [`src/golden/Rain_On_Me_INFINITY_V3.2f_Hierarchical_Calibration.pine`](src/golden/Rain_On_Me_INFINITY_V3.2f_Hierarchical_Calibration.pine)
- Full development story: [`docs/ROM_JOURNEY.md`](docs/ROM_JOURNEY.md)
- Version-by-version map: [`docs/VERSION_INDEX.md`](docs/VERSION_INDEX.md)
- Experimental conclusions: [`docs/RESEARCH_FINDINGS.md`](docs/RESEARCH_FINDINGS.md)
- Current status: [`PROJECT_STATUS.md`](PROJECT_STATUS.md)

## Project identity

ROM is not meant to be a random collection of indicators. Its design goals are:

- mathematically faithful PHI/Fibonacci price geometry;
- explainable multi-family reasoning rather than one opaque score;
- confirmed, non-repainting behavior for actionable events;
- prospective forecasts frozen before their outcomes;
- evidence-calibrated `FOLLOW / FADE / WAIT / LEARN` routing;
- a visually expressive but readable Aurora/Ocean chart identity;
- research dashboards that reveal weakness instead of hiding it.

The central rule is simple: **a new idea becomes a challenger before it is allowed to change production behavior.**

## Repository map

| Folder | Meaning |
|---|---|
| `src/golden/` | Frozen trusted production/control build |
| `src/evolution/` | Main V3.0–V3.2 milestones in chronological order |
| `src/research/adaptive_labs/` | Recent-memory and PHI-permeability factorial experiments |
| `src/research/structural_phi/` | Structural event and adaptive-salience research |
| `src/research/reaction_labs/` | HOLD/PASS/WHIP/STALL and personality research |
| `src/research/scale_packs/` | Final MICRO/INTRADAY/MACRO packs and prospective validators |
| `archive/intermediate_research/` | Superseded or diagnostic builds retained for provenance |
| `docs/` | Architecture, journey, testing method and findings |
| `checksums/` | SHA-256 integrity manifest |

## Important status warning

The newest filename is not automatically the best trading build. Many later scripts are deliberately isolated research instruments.

**V3.2f remains the golden production/control reference.** Later H-series files ask narrower scientific questions and must not be treated as promoted live logic without their accompanying research status.

## TradingView use

1. Open the desired `.pine` file.
2. Copy the complete source into TradingView's Pine Editor.
3. Save and add it to the chart.
4. Use normal candles for validation unless a build explicitly states otherwise.
5. For historical comparison, keep symbol, exchange, timeframe and settings consistent.

The project was developed heavily from Android, so many research builds intentionally open with useful defaults and mobile-sized dashboards.

## Scope and disclaimer

This archive is research software, not financial advice. Backtests, dashboard probabilities and historical screenshots do not guarantee future performance. Several files are preserved precisely because an idea failed and taught the project something useful.

No open-source license is included. Public visibility alone does not grant reuse rights; choose and add a license deliberately if broader reuse is intended.

