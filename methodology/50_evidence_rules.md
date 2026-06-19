# Evidence & Source Rules

These rules are identical across all evidence modes (live-web / user-provided-only / hybrid); only the *retrieval mechanism* differs.

## Status tags

| Tag | Meaning | Requirement |
|-----|---------|-------------|
| **VERIFIED** | Corroborated fact | ≥2 independent credible sources, **or** 1 authoritative/official/primary source (G2-T1) |
| **PROBABLE** | Plausible, single-sourced | 1 credible source (G2-T2/T3), not corroborated |
| **USER-PROVIDED ASSUMPTION** | From the Case Pack | Supplied by the operator, not independently checked |
| **UNKNOWN** | No support | Mark explicitly; never guess or back-fill |

## Source hierarchy (summary — full table in `20_governance.md` §G2)

T1 Authoritative/primary → T2 Established secondary → T3 Crowd/platform signal → T4 Weak/anecdotal → T5 Disallowed (model prior knowledge as fact, fabricated, unread paywalled). Higher tier wins conflicts; independence and recency required.

## Finding record (every non-UNKNOWN claim)

A Finding records:
- **statement** — the claim in neutral language
- **status** — VERIFIED / PROBABLE / USER-PROVIDED ASSUMPTION / UNKNOWN
- **confidence** — 0.0–1.0
- **evidence[]** — ≥1 source for any non-UNKNOWN finding
- **corroboration_count** — number of independent sources
- **phase** — which phase produced it
- **produced_by** — which agent

Each **Evidence** item records: source title, publisher, URL (where applicable), access date, the **exact supporting excerpt**, and the **retrieval query** used (for audit/replay).

## Hard rules

1. Any non-UNKNOWN finding needs ≥1 **resolvable** source.
2. VERIFIED needs `corroboration_count ≥ 2` (or one authoritative source flagged as such).
3. Every number that appears in the Final Report must trace to a specific finding and be **footnoted**. No orphan numbers.
4. All findings accumulate in one shared **Evidence Ledger**; agents read prior findings rather than re-deriving them (consistency + cost control).
5. **Conflict handling:** when sources disagree, record both, lower confidence, and surface the conflict as an "unresolved question" for the debate/arbiter.
6. **Localization:** prefer local-language and local/official sources; note when only foreign-language or non-local sources were available (lowers confidence).

## Discovery vs. Validation bars (G4)

- **Discovery (Phases 1–4):** PROBABLE evidence is acceptable to *propose* a concept and assign *provisional* scores. Breadth of hypotheses is the goal; the unknown-penalty still applies.
- **Validation (Phases 5–6 + the 2–4 week plan):** the *load-bearing* claims behind any RECOMMENDED winner must be VERIFIED. PROBABLE-only decisive claims cap a concept at CONDITIONAL; UNKNOWN/ASSUMPTION decisive claims → INSUFFICIENT_EVIDENCE. The validation plan is the explicit bridge to upgrade PROBABLE → VERIFIED.
