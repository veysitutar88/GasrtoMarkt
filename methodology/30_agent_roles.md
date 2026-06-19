# Agent Role Specifications

Supervisor topology: the **Orchestrator** coordinates; workers return structured results to it (they do not hand off to each other). Each role is substrate-agnostic — realizable as a human-followed role, a documentation step, or a coded agent. Authority per role is defined in `20_governance.md` §G0.

---

## 1. Orchestrator — *Controls the run*
- **Inputs:** Case Pack, current run state.
- **Does:** enforces phase order and the Phase-3 gate; enforces evidence rules (G2) and autonomy boundaries (G1); keeps the market audit strictly separated from concept generation; aggregates worker outputs; halts and escalates at 🟡/🔴; executes the hard STOP at Phase 7.
- **Must not:** generate concepts, score, or decide winners; skip phases; lift the gate; produce execution artifacts.

## 2. Market Research — *Macro & market context*
- **Inputs:** location data.
- **Produces:** local restaurant market state; macro pressures (rent, labor, inflation, tourism); consumer demand signals; relevant food-service trends — each as a tagged Finding.
- **Must not:** name or analyze any specific existing business at the site; present prior knowledge as fact.

## 3. Competitor Mapping — *The competitive field around the site*
- **Produces:** direct & indirect competitors with concept, price level, opening hours, ratings/reviews, positioning, visible weaknesses, and a saturation read (relative to catchment, per G3).
- **Must not:** fabricate competitor specifics; every competitor fact needs a source + tag.

## 4. Demand Pattern — *Who actually eats here*
- **Produces:** likely demand groups (locals, office workers, hotel guests, tourists, evening diners, delivery/takeaway, corporate/private dining) — **included only when externally evidenced** for this location — each tied to geography **and** daypart (G3).
- **Must not:** assume a demand group exists without evidence.

## 5. Concept Generator — *Hypotheses, gated*
- **Runs only after** Phases 1–2 are complete and valid.
- **Produces:** 5–8 distinct concept hypotheses, each tied to specific audit findings (the gap/demand it serves) and respecting the Constraint Profile.
- **Must not:** produce menus, branding, names, or recipes. Concepts are **format descriptions only** (e.g. "fast-casual daytime bowl bar serving the weekday office lunch daypart").

## 6. Financial & Operations — *Does the math survive?*
- **Tests** each concept against: target monthly revenue, average-ticket logic, seating/kitchen throughput, staff capacity, food-cost pressure, labor-cost pressure, investment/payback, operating complexity.
- **Produces:** feasibility findings + numeric sanity ranges (not a full pro-forma — that is a 🔴 execution artifact).

## 7. Risk & Constraint — *The adversary*
- **Attacks** each concept; **rejects** any that violate budget, staffing, property/renovation/noise/operating-hour limits, mandatory services, licensing, or margin logic.
- **Produces:** per-concept kill-reasons or surviving-with-conditions notes.

## 8. Judge / Arbiter — *Scores and decides*
- **Scores** concepts (see `60_scoring_matrix.md`), **runs the structured debate** (`70_debate_arbiter_protocol.md`), resolves contradictions, selects **Winner #1** and optional **Winner #2**.
- **May declare:** "No concept is sufficiently validated yet; further research or field testing is required," with the data gaps to close (G4).
- **Must not:** override constraints or evidence rules; act outside Phases 5–6; lift the gate.
