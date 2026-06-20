# Workflow Phases (0–7)

Phases form a state machine with explicit allowed transitions. The Phase-3 gate is hard: concepts cannot be generated until a valid Market Audit and Constraint Profile exist.

| Phase | Name | Entry condition | Exit / gate |
|-------|------|-----------------|-------------|
| 0 | Intake | Case Pack loaded | Missing data listed as UNKNOWN; bias check passes |
| 1 | Market Audit | Phase 0 done | Market + Competitor + Demand findings merged & tagged; audit evidence floor met (else 🟡) |
| 2 | Constraint Profile | Phase 1 done | Neutral site/constraint profile built from provided data only |
| 3 | Concept Discovery | **GATE: Phases 1 & 2 complete and valid** | 5–8 concepts, each linked to audit findings |
| 4 | Scoring | Phase 3 done | Each concept scored on all 12 criteria (1–10) + unknown-penalty applied |
| 5 | Debate | Phase 4 done | Structured debate on top-N concepts; unresolved questions captured |
| 6 | Verdict | Phase 5 done | Arbiter outputs winner(s) or "insufficient evidence" |
| 7 | Approval Gate | Phase 6 done | **HARD STOP** — no implementation/menus/branding/files |

## Phase notes

- **Phase 0 — Intake.** Load the Case Pack. List everything UNKNOWN. Run the bias check: confirm no brand/name/menu/history/website/visual-identity/performance content is present; if found, flag the violation and treat it as out-of-scope.
- **Phase 1 — Market Audit.** Market Research, Competitor Mapping, and Demand Pattern run (parallelizable). Outputs merge into one Market Audit. Covers market state, competitor landscape, demand groups, price levels, dining patterns, oversaturated formats, underserved opportunities. Apply the **discovery** evidence bar (PROBABLE acceptable). Enforce the audit evidence floor (≥1 sourced finding per research dimension), else raise a 🟡 checkpoint.
- **Phase 2 — Constraint Profile.** Risk & Constraint distills binding constraints from the Case Pack only (budget, staffing, property, hours, noise, renovation, mandatory services, licensing, time horizon).
- **GATE (before Phase 3). (M3)** Gate passes when all three conditions are met: (a) ≥1 PROBABLE+ (PROBABLE or VERIFIED) finding exists for at least 2 of the 3 research dimensions (Market, Competitor, Demand); (b) the Constraint Profile has been produced from Case Pack data only; (c) no UNKNOWN hard constraint eliminates *all* candidate concepts before they are generated (if so, raise a 🟡 checkpoint and surface the conflict to L0 before proceeding). A dimension with only ASSUMPTION or UNKNOWN findings does not satisfy condition (a) for that dimension; the audit evidence floor for it is unmet, triggering the G1 🟡 checkpoint.
- **Phase 3 — Concept Discovery.** Generate 5–8 concepts as **format descriptions only**, each tied to the audit finding(s) it addresses and compatible with the Constraint Profile. Each concept must be independently viable as a standalone format. Hybrid combinations of two already-scored concepts are not permitted as separate entries in this run. **(M6)** If a hybrid appears optimal after the debate, flag it as an L0 question in the Verdict section — do not generate it here.
- **Phase 4 — Scoring.** Score every concept on all 12 criteria (1–10); apply the unknown-penalty per `60_scoring_matrix.md`. Still the discovery bar.
- **Phase 5 — Debate.** The **validation** evidence bar now applies. Run the structured debate on the top-N concepts; capture unresolved questions.
- **Phase 6 — Verdict.** Arbiter applies the G4 decision rule: RECOMMENDED / CONDITIONAL / REJECTED / INSUFFICIENT_EVIDENCE; selects Winner #1 (+ optional #2); or declares "no concept sufficiently validated yet."
- **Phase 7 — Approval Gate.** Produce the Final Report and STOP. No execution/production artifacts. Lifting the gate is an L0 (Human Principal) decision only.

## Evidence bars by phase

- **Discovery bar** (PROBABLE acceptable to propose & score): Phases 1–4.
- **Validation bar** (VERIFIED required for load-bearing claims behind a recommendation): Phases 5–6 and the 2–4 week validation plan.
