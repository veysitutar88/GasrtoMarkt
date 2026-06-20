# Dry-Run Review — synthetic_001

> **Purpose:** Post-run assessment of the methodology package. Not a case deliverable — a methodology quality-control document. Every finding here is a methodology observation, not a market claim.

---

## 1. What worked

**Phase structure (40_workflow_phases.md):** The 0–7 phase sequence held cleanly. No phase was skipped. The Phase-3 gate correctly held until both a Market Audit and Constraint Profile were confirmed in place. The hard stop at Phase 7 (Approval Gate) was reached without generating any forbidden artifact.

**Evidence tagging system (50_evidence_rules.md):** The four-tag system (VERIFIED / PROBABLE / USER-PROVIDED ASSUMPTION / UNKNOWN) was unambiguous to apply throughout. Tag promotion and demotion rules (G2 source hierarchy) were clear and actionable. SYNTHETIC evidence labels coexisted cleanly with the tags — no confusion between "SYNTHETIC/TEST DATA" (run-scope label) and the methodology tags (quality-of-evidence labels).

**Unknown-penalty mechanics (60_scoring_matrix.md):** The 0.5× (UNKNOWN) and 0.75× (ASSUMPTION) penalties applied without ambiguity once the "primary backing" rule was interpreted (see §3 below). Concept C4 correctly collapsed under the compound effect of multiple UNKNOWN-backed criteria; the scoring system surfaced this without manual judgment.

**Arbiter decision rule (70_debate_arbiter_protocol.md):** The four-way decision (RECOMMENDED / CONDITIONAL / REJECTED / INSUFFICIENT_EVIDENCE) mapped cleanly to the evidence states encountered. The rule "VERIFIED required for RECOMMENDED" correctly prevented premature recommendation when only PROBABLE evidence existed. Two CONDITIONAL winners emerged — this is a valid, information-rich outcome.

**Approval gate (90_approval_gate.md):** Gate held. No menus, names, branding, recipes, financial models, marketing campaigns, hiring plans, or build-out plans were generated anywhere in the run. The gate boundary was unambiguous.

**Bias firewall:** No real restaurant, brand, operator, address, or prior case context leaked into the fictional case. Location names (Valdenfurt, Halvenia, Kesselmoor) were clearly fictional. No prior-session memory or known brand was reconstructed.

**G1 checkpoint behavior:** The 🟡 checkpoint for a thin demand dimension (no PROBABLE+ finding; F11 and F12 both ASSUMPTION) was correctly identified and logged. The run continued with penalties applied rather than halting — which is the correct behavior for a synthetic run (no real cost risk, no real recommendation stakes).

---

## 2. What was unclear

**2a. Penalty application when primary backing is mixed (PROBABLE + ASSUMPTION).**
The methodology states the penalty applies to criteria "backed by UNKNOWN or ASSUMPTION." It does not specify what happens when a criterion is backed by *multiple* findings of different tiers — one PROBABLE and one ASSUMPTION. In this run, C7's Market Demand was backed by both F01 (PROBABLE) and F12 (ASSUMPTION). The "primary backing rule" — apply the tag of the *primary* finding — was adopted informally but is not stated in `60_scoring_matrix.md`.

**Recommended fix:** Add one sentence to `60_scoring_matrix.md`: *"When multiple findings back one criterion, apply the penalty of the weakest-tier finding only if that finding is the primary (load-bearing) evidence; supplementary lower-tier findings do not themselves trigger a penalty."*

**2b. Evidence dimension floor check.**
The G1 ceiling states "≥1 sourced (VERIFIED/PROBABLE) finding per research dimension, else 🟡 checkpoint." The Demand dimension failed this floor (F11 and F12 are ASSUMPTION, F13/F14 are UNKNOWN). The checkpoint was correctly triggered, but the correct *behavior* after triggering (continue with penalties, or halt?) was not specified in `40_workflow_phases.md` or `20_governance.md`. In this run, continuation was chosen (low-stakes synthetic run) — but a live run might warrant a pause.

**Recommended fix:** Add one line to `20_governance.md` §G1 (🟡 Checkpoint section): *"If the evidence floor is unmet for a research dimension, the Orchestrator logs the checkpoint, applies unknown-penalties to all affected criteria, and continues — unless the Orchestrator determines no concept can be scored reliably, in which case the Orchestrator escalates to L0."*

---

## 3. Where the methodology was too strict

**3a. Tiebreaker missing for equal weighted totals.**
C2 and C5 tied at 6.33. The methodology (`70_debate_arbiter_protocol.md`) says "top-N by weighted_total" but gives no tiebreaker rule. An arbitrary choice was made (C2 selected over C5 because C2 had broader finding coverage). This is a judgment call that should not be arbitrary in a production run.

**Recommended fix:** Add a tiebreaker hierarchy to `70_debate_arbiter_protocol.md`: *"On a tie: (1) prefer the concept with more PROBABLE-tier (not ASSUMPTION or UNKNOWN) primary findings; (2) if still tied, prefer the concept with the higher Risk score (criterion 12 — inverted); (3) if still tied, include both in the debate (bump N by 1)."*

**3b. The Phase-3 gate does not define minimum finding count.**
`40_workflow_phases.md` says "confirm a valid Market Audit + Constraint Profile before generating concepts" but does not specify what "valid" means quantitatively. In practice, the evidence floor rule (G1 ≥1 PROBABLE/VERIFIED per dimension) was used — but this cross-reference is not explicit in the Phase-3 gate text.

**Recommended fix:** In `40_workflow_phases.md` Phase-3 gate, add: *"Gate passes when: (a) ≥1 PROBABLE+ finding exists for at least 2 of 3 research dimensions (Market, Competitor, Demand); (b) the Constraint Profile has been written from case pack data only; (c) no UNKNOWN hard constraint kills all candidate concepts (if so, 🟡 checkpoint before concept generation)."*

---

## 4. Where the methodology was too loose

**4a. The debate protocol does not restrict new evidence introduction in rebuttals.**
During the C2 debate, the Proponent introduced a new argument in Round 2 rebuttal (bought-in pastries as a fallback sourcing model). This was not cited to a prior Finding — it is a new hypothesis generated mid-debate. The methodology should require that rebuttal arguments either (a) cite an existing Finding or (b) flag a new hypothesis explicitly as ASSUMPTION-tier for the verdict.

**Recommended fix:** Add to `70_debate_arbiter_protocol.md`: *"In rebuttals, the Proponent may only: (a) cite existing Findings already in the ledger; (b) explicitly flag new arguments as USER-PROVIDED ASSUMPTION and note them as unresolved questions for the Arbiter."*

**4b. The Concept Set (Section 5) boundary is vague on operational combinations.**
During the debate (C1 cross-concept question), the idea of combining C1 and C7 into a single counter was flagged. The methodology says concepts are "format descriptions only" but does not address hybrid/combined formats. A production run operator might generate 5 variants plus 3 combinations, bloating the debate phase.

**Recommended fix:** Add to `40_workflow_phases.md` Phase 3: *"Each concept must be independently viable; hybrid combinations of two scored concepts are not permitted as separate concepts in the same run. If a hybrid appears optimal post-debate, flag it as an L0 question in the Verdict."*

---

## 5. Template adjustments recommended

| File | Adjustment needed |
|------|-----------------|
| `templates/case_input_pack.md` | Add `evidence_mode:` field (live-web / user-provided / synthetic / hybrid) — it was missing and had to be added manually in this run |
| `60_scoring_matrix.md` | Add "primary backing rule" for mixed-tier finding penalty (§2a above) |
| `70_debate_arbiter_protocol.md` | Add tiebreaker rule (§3a above); add rebuttal evidence restriction (§4a above) |
| `40_workflow_phases.md` | Quantify Phase-3 gate minimum (§3b above); clarify behavior after 🟡 dimension-floor checkpoint; add hybrid-concept restriction (§4b above) |
| `20_governance.md` | Clarify G1 continue-vs-escalate rule when evidence floor unmet (§2b above) |
| `methodology/00_README.md` | Note the five known fixes from this dry-run with version reference (e.g. "v1.4 — known gaps resolved in v1.5 pending L0 approval") |

---

## 6. Whether the approval gate held correctly

**Yes — the gate held.**

The Final Report ends at Section 13 (Evidence Ledger) with the explicit `[STOP — Approval Gate]` marker. No implementation plan, menu, branding, recipe, supplier list, financial model, marketing campaign, hiring plan, or build-out plan was generated at any point in the run. The Verdict section produced two CONDITIONAL winners and a validation plan — correctly stopping short of execution artifacts.

The gate language in `90_approval_gate.md` was clear and unambiguous. No content in the run came close to the boundary.

---

## 7. Whether the system avoided prior-context, brand, menu, and history bias

**Yes — confirmed.**

- All location names (Valdenfurt, Halvenia, Kesselmoor, Mühlenweg) are clearly invented.
- All competitor names (Bäckerei Wendl, TischGuide Halvenia, ValdenEats, FlixFood Halvenia) are invented.
- No real restaurant, brand, chain, city, country, or known operator appeared anywhere in the run.
- No menu items, dish names, ingredient lists, or recipes were generated.
- No prior conversation, project memory, or known case context leaked in.
- The Case Input Pack contains no brand/name/menu/history field, and none was added during the run.

**Bias firewall held.**

---

## 8. Whether the Arbiter could produce a valid verdict

**Yes — the Arbiter produced a valid and well-structured verdict.**

- Two CONDITIONAL winners identified (C1, C7) with justification, decisive findings, and open risks each.
- Three REJECTED concepts with kill-reasons.
- One lower-CONDITIONAL concept (C2) with a blocking prerequisite correctly flagged.
- The `no_concept_validated = false` determination was correct: two credible candidates exist; the evidence gap is closeable in 2–4 weeks.
- The Arbiter correctly declined RECOMMENDED for all concepts because no decisive finding reached VERIFIED.
- The four-way decision matrix (RECOMMENDED / CONDITIONAL / REJECTED / INSUFFICIENT_EVIDENCE) covered every concept cleanly.

**One ambiguity encountered:** The methodology does not specify whether "CONDITIONAL (lower)" is a formal decision state or an informal modifier. In this run it was used informally for C2. A production run should formalize or drop this sub-tier.

---

## 9. Recommended methodology fixes (consolidated)

| # | File | Fix | Priority |
|---|------|-----|----------|
| M1 | `60_scoring_matrix.md` | Add primary-backing rule for mixed-tier penalty | High |
| M2 | `70_debate_arbiter_protocol.md` | Add tiebreaker rule for equal weighted_total | High |
| M3 | `40_workflow_phases.md` | Quantify Phase-3 gate minimum (≥1 PROBABLE+ in ≥2 of 3 dimensions) | High |
| M4 | `20_governance.md` | Clarify G1 continue-vs-escalate after dimension-floor 🟡 checkpoint | Medium |
| M5 | `70_debate_arbiter_protocol.md` | Restrict rebuttal to cited Findings or explicit ASSUMPTION flags | Medium |
| M6 | `40_workflow_phases.md` | Ban hybrid-concept entries in Phase 3 | Medium |
| M7 | `templates/case_input_pack.md` | Add `evidence_mode:` field | Low |
| M8 | `70_debate_arbiter_protocol.md` | Formalize (or drop) "CONDITIONAL (lower)" as a decision sub-tier | Low |

> **These fixes require L0 approval before editing any methodology file (per `90_approval_gate.md` — build actions are forbidden without explicit, separate approval).**

---

## 10. Confirmation that no real market claims were made

**Confirmed.**

Every factual-sounding claim in this run — employment counts, pedestrian figures, competitor names, market growth rates, survey percentages — is explicitly labeled `SYNTHETIC / TEST DATA` in the Evidence Ledger and the Case Input Pack. The Final Report carries the `⚠ SYNTHETIC / TEST DATA` warning in its header. No finding in the Evidence Ledger references a real city, real business, real publication, real platform, or real statistic. The dry-run was conducted entirely in synthetic-evidence mode as approved.

---

*End of dry-run review — synthetic_001*
