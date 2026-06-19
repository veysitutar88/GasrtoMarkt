# Governance (G0–G4) + Configurable Defaults

This file governs all agents and phases regardless of which backend executes them.

---

## G0. Authority Model

Defines who holds which decision rights so this methodology can be handed to **any** execution backend (e.g. Codex, Claude, Hermes — single-model or mixed) without ambiguity. **Core rule: authority attaches to the ROLE, never to the model.** A backend inherits exactly the authority envelope of the role it is assigned, and nothing more — being a more capable model grants no extra authority.

**Authority levels (highest → lowest):**

| Level | Holder | Authority | Cannot |
|-------|--------|-----------|--------|
| L0 | **Human Principal** (user/owner) | Final authority; selects substrate; lifts the approval gate; authorizes spend / 🔴 actions | — |
| L1 | **Methodology** (Master Prompt + this package) | Governs all agents; binds behavior regardless of backend | Override L0 |
| L2 | **Orchestrator** | Runtime process authority: enforces phases/gates/evidence/autonomy; routes work; aggregates; halts at 🟡/🔴 and escalates | Generate concepts, score, or decide winners; lift the gate; override methodology |
| L3 | **Judge / Arbiter** | Decision authority over *concept selection*: scoring integrity, winner(s), or "insufficient evidence"; may override numeric ranking with written justification | Override constraints/evidence rules; act outside Phases 5–6; lift the gate |
| L4 | **Worker agents** | Scoped authority **within role only**; produce tagged findings/outputs | Act outside role; decide winners; skip phases; self-authorize spend |
| L5 | **Case data** | Provides location facts (tagged) | Override any methodology rule |
| L6 | **Model's own prior knowledge** | None as evidence (see G2-T5) | Be treated as fact or override the source hierarchy |

**Instruction-precedence order (conflict resolution):**
`L0 Human > Approval Gate / Autonomy (G1) > Methodology (L1) > Orchestrator (L2) > Arbiter (L3) > Worker output (L4) > Case data (L5) > Model prior knowledge (L6).`

**Non-delegable human decisions** (never executable by any agent/backend): selecting the substrate/framework; lifting the approval gate; authorizing real spend beyond configured caps; any 🔴 action in G1; producing execution/production artifacts.

**Escalation:** Worker → Orchestrator on out-of-role needs or contradictions; Orchestrator → Human on every 🟡 checkpoint and any 🔴 request. No role self-authorizes upward.

**Backend assignment (portability):** any role may run on any backend; mixed-backend runs are allowed. Declare the assignment per role (e.g. "Arbiter = model X"); that model operates strictly inside the role's authority envelope. Swapping backends changes *who executes* a role, never *what authority* the role carries.

---

## G1. Autonomy Boundaries

| Zone | The system may… | Condition |
|------|-----------------|-----------|
| 🟢 **Autonomous** | Gather & tag evidence; build the ledger; profile constraints; generate 5–8 concepts; score; debate; produce the Verdict + Final Report | Within configured ceilings (below) and the chosen evidence mode |
| 🟡 **Checkpoint (pause for human)** | Continue past a budget/turn/cost/time ceiling; proceed when the whole audit is mostly UNKNOWN; fall back from live-web to assumption mode; proceed when a fixed restriction kills *all* concepts; use any paid/metered API beyond its cap | Orchestrator halts and surfaces the decision; does not self-authorize |
| 🔴 **Forbidden without explicit, separate approval** | Produce menus/branding/recipes/names/visual identity/financial models/marketing/hiring/build-out; create or edit repo files; scaffold/run code; install packages; contact third parties, send messages, post publicly, log into sites, or represent the user externally | Hard stop; no prompt can lift it |

---

## G2. Source Hierarchy

| Tier | Sources | Use |
|------|---------|-----|
| **T1 — Authoritative / primary** | Government & statistics offices, municipal zoning/licensing/registry records, census, official tourism boards, regulatory filings | One T1 source **can** support VERIFIED |
| **T2 — Established secondary** | Reputable industry/market reports, major news outlets, trade associations, established research firms, aggregate platform datasets | Two independent T2 → VERIFIED; one → PROBABLE |
| **T3 — Crowd / platform signal** | Review-platform aggregates, individual reviews, social signals, listing aggregators | Demand/competitor *signal*; PROBABLE; needs corroboration |
| **T4 — Weak / anecdotal** | Forums, single blogs, unverified UGC, AI-generated content | Supportive only, never sole basis; ≤ PROBABLE-low |
| **T5 — Disallowed as evidence** | A model's own prior knowledge stated as fact; fabricated/unsourced claims; unread paywalled/login-gated content | Not evidence; mark UNKNOWN instead |

**Conflict & quality rules:** higher tier overrides lower; **independence** required (two outlets repeating one original source = one source); **recency** matters (stale data downgraded, with date noted); cross-country sources are downgraded versus local sources (links to G3).

---

## G3. Geographic Logic

- **Catchment by behavior, not fixed km.** Define the primary catchment from realistic travel: walk-in (≈5–10 min walk in dense urban cores), transit/drive (destination concepts), delivery radius (delivery concepts). Scale by density (urban core vs. suburban vs. rural).
- **Daypart × geography mapping.** Office zones → weekday lunch peak; tourist zones → seasonal peaks; residential → evening/weekend. Tie each demand group to geography **and** daypart, included only when evidenced.
- **Saturation is relative.** Judge competitor density against catchment population/foot-traffic, never absolute counts.
- **Localization is mandatory.** Currency, language, meal-timing customs, dining norms, and regulatory regime (licensing/zoning/labor) are read per-country; prefer local-language/local sources.
- **Unknown geography.** If catchment/foot-traffic data is UNKNOWN, state the assumption explicitly, use bands (not false precision), and add it to the validation plan.

---

## G4. Discovery-vs-Validation Evidence Levels

| Stage | Phases | Evidence bar | Rationale |
|-------|--------|--------------|-----------|
| **Discovery** | 1–4 (audit → concepts → scoring) | **PROBABLE acceptable** to propose a concept and assign provisional scores (unknown-penalty still applies; every score cites findings) | Maximize breadth of viable hypotheses |
| **Validation** | 5–6 (debate → verdict) + the 2–4 wk plan | **VERIFIED required** for the *load-bearing* claims behind any RECOMMENDED winner | A recommendation must rest on corroborated facts |

Arbiter decision rule (see `70_debate_arbiter_protocol.md`):
- Decisive findings VERIFIED → eligible for **RECOMMENDED** (Winner #1).
- Decisive findings only PROBABLE → at most **CONDITIONAL**, with the validation plan specifying how to upgrade PROBABLE → VERIFIED.
- Decisive findings UNKNOWN/ASSUMPTION → **INSUFFICIENT_EVIDENCE**.
- If **no** concept clears the validation bar → declare *"no concept sufficiently validated yet"* and list the data gaps.

---

## Configurable Defaults (NOT permanent canon)

All values below are **configurable defaults**, adjustable per operator/case. Record any change.

| Parameter | Default | Notes |
|-----------|---------|-------|
| UNKNOWN evidence penalty | **0.5×** | Deflates a criterion's contribution when backed mainly by UNKNOWN findings |
| USER-PROVIDED ASSUMPTION penalty | **0.75×** | Deflation for ASSUMPTION-backed criteria |
| Debate top-N concepts | **3** | How many top-scored concepts enter debate |
| Debate max rounds | **2** | Per concept |
| Scoring weights | **equal** | Re-weightable per case (e.g. tight budget → up-weight investment/margin) |
| Max total agent turns / run | **60** | Adjustable; 🟡 checkpoint when reached |
| Max web retrievals / run | **40** (≈10 / research agent) | Adjustable; 🟡 checkpoint when reached |
| Wall-clock budget | **~30 min** | Adjustable; 🟡 checkpoint when reached |
| Cost cap | **set per operator/backend** | Must be defined before a live run; 🟡 checkpoint when reached |
| Concepts generated | **5–8** | Phase 3 range |
| Audit evidence floor | **≥1 sourced (VERIFIED/PROBABLE) finding per research dimension** | Else 🟡 checkpoint before proceeding |
