# Scoring Matrix

Each concept is scored **1–10** on **all 12** criteria. Every score carries a one-line rationale and **mandatory supporting Finding references** — no naked scores.

| # | Criterion | "10" means | "1" means |
|---|-----------|------------|-----------|
| 1 | Market demand | Strong, evidenced, growing demand | No evidenced demand |
| 2 | Local competitive gap | Clear underserved gap | Saturated, no gap |
| 3 | Revenue potential | Comfortably exceeds target | Cannot approach target |
| 4 | Speed to test | Testable in days, cheaply | Long, costly to test |
| 5 | Investment efficiency | Low capex per revenue unit | Capital-heavy, poor ratio |
| 6 | Staff feasibility | Runs within staffing constraint | Needs unavailable staff/skill |
| 7 | Kitchen feasibility | Fits kitchen capabilities | Needs unavailable kitchen capacity |
| 8 | Property compatibility | Fits size/property/zoning | Violates property limits |
| 9 | Margin potential | Robust, resilient margins | Structurally thin margins |
| 10 | Marketing clarity | Instantly explainable proposition | Confusing/undifferentiated |
| 11 | Long-term defensibility | Hard to copy, durable | Trivially copied |
| 12 | Risk level (inverted) | Low downside risk | High failure risk |

## Weights and total

`weighted_total = Σ(score_i × weight_i)`

- **Default:** equal weights across all 12 criteria (configurable).
- Re-weight per case when the Case Pack signals priorities — e.g. tight budget → up-weight #5 (investment efficiency) and #9 (margin potential); short time horizon → up-weight #4 (speed to test). Record any re-weighting.

## Unknown-evidence penalty

For each criterion whose score rests **mainly on UNKNOWN or ASSUMPTION** findings, deflate that criterion's contribution to the weighted total:

| Backing | Penalty factor (default, configurable) |
|---------|----------------------------------------|
| UNKNOWN-backed | **0.5×** |
| USER-PROVIDED ASSUMPTION-backed | **0.75×** |

This prevents a concept from "winning" on confident-but-unsupported scores: thin-evidence concepts are automatically deflated relative to evidenced ones.

## Anti-gaming rules

- A criterion score **without** supporting Finding references is **nullified** by the Judge (not averaged in).
- Scores must be consistent with the cited findings' status tags; a "10" on Market demand backed only by UNKNOWN is invalid.
- The Arbiter may override the numeric ranking, but only with written justification tied to findings (see `70_debate_arbiter_protocol.md`).
