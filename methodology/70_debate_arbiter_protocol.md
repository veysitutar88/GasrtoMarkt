# Debate, Judge & Arbiter Protocol

The validation evidence bar (G4) applies throughout this stage.

## Selection

Debate runs on the **top-N concepts by weighted_total** (default **N = 3**, configurable).

## Structured debate

Bounded loop (default **max 2 rounds** per concept, configurable):

1. **Proponent** (Concept Generator) defends the concept with cited arguments.
2. **Critics attack in fixed order:**
   - **Financial & Operations** — numbers and feasibility.
   - **Risk & Constraint** — failure points and constraint violations.
   - **Market / Demand** — is the demand real and sufficient?
3. **Rebuttals** — the Proponent responds.
4. Every argument and rebuttal must cite **Findings**.
5. **Capture** per round: arguments for, arguments against, rebuttals, and **unresolved questions** (these feed the Arbiter and the "needs more data" path).

## Judge (scoring referee)

- Confirms each criterion score is backed by cited Findings; **nullifies** any unsupported score (does not average it in).
- Recomputes `weighted_total` with the unknown-penalty applied.
- Flags inconsistencies between a score and its findings' status tags.

## Arbiter (decider)

For each concept assigns a decision with justification, decisive findings, and open risks:

| Decision | When |
|----------|------|
| **RECOMMENDED** | Decisive findings are VERIFIED; survives debate; satisfies constraints |
| **CONDITIONAL** | Sound but decisive findings only PROBABLE; needs validation to upgrade |
| **REJECTED** | Killed by a constraint, infeasible economics, or losing the debate |
| **INSUFFICIENT_EVIDENCE** | Decisive findings UNKNOWN/ASSUMPTION; cannot be judged yet |

Then the Arbiter:
- Selects **Winner #1** and optionally **Winner #2**.
- **May override** the numeric ranking with explicit written justification tied to findings.
- **Must declare `no_concept_validated = true`** — *"no concept sufficiently validated yet; further research or field testing required"* — when every candidate is INSUFFICIENT_EVIDENCE (or none clears the validation bar), and list the specific **data gaps to close**. This is a first-class outcome, not a failure.

## Output

The Arbiter's verdict feeds directly into the Final Report (`80_report_schema.md`), including: winner(s), rejected concepts with reasons, key assumptions, missing evidence, the 2–4 week validation plan, and confidence levels.
