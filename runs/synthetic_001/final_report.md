# Final Report — synthetic_001

> **⚠ SYNTHETIC / TEST DATA — This report is a dry-run of the methodology using entirely fictional data. No real city, address, market, competitor, or financial claim is made. Every number is cited to a synthetic Finding in Section 13.**

---

## 1. Case Snapshot

| Field | Value | Tag |
|-------|-------|-----|
| Case ID | synthetic_001 | — |
| Evidence mode | Synthetic-only | — |
| City | Valdenfurt | SYNTHETIC/TEST DATA |
| Country | Halvenia (fictional) | SYNTHETIC/TEST DATA |
| District | Kesselmoor — CBD fringe + residential | SYNTHETIC/TEST DATA |
| Area character | Mixed: office, residential, light retail | SYNTHETIC/TEST DATA |
| Premises size | 85 sqm | USER-PROVIDED ASSUMPTION |
| Seating | ~30 seats | USER-PROVIDED ASSUMPTION |
| Kitchen: hood | Present (capacity unknown) | USER-PROVIDED ASSUMPTION |
| Kitchen: gas | Yes | USER-PROVIDED ASSUMPTION |
| Kitchen: ventilation | Limited (single rear duct) | USER-PROVIDED ASSUMPTION |
| Kitchen: prep area | Not demarcated | UNKNOWN |
| Service capacity | Counter + limited table service | USER-PROVIDED ASSUMPTION |
| Property context | Ground-floor corner unit, 2 glass frontages, transit 50 m | USER-PROVIDED ASSUMPTION / PROBABLE [F02] |
| Budget capex | HVK 120,000 | USER-PROVIDED ASSUMPTION |
| Monthly opex ceiling | HVK 22,000 | USER-PROVIDED ASSUMPTION |
| Target monthly revenue | HVK 35,000 | USER-PROVIDED ASSUMPTION |
| Target margin | 18% | USER-PROVIDED ASSUMPTION |
| Target payback | 30 months | USER-PROVIDED ASSUMPTION |
| Operating hours | 07:00–22:00 | USER-PROVIDED ASSUMPTION |
| Noise constraint | Residential ordinance after 21:00 | USER-PROVIDED ASSUMPTION |
| Renovation | No structural changes; listed exterior | USER-PROVIDED ASSUMPTION |
| Alcohol license | Not held; acquisition timeline UNKNOWN | USER-PROVIDED ASSUMPTION |
| Max staff | 4 simultaneously | USER-PROVIDED ASSUMPTION |
| Time horizon | 6 months to open | USER-PROVIDED ASSUMPTION |

---

## 2. Missing Data

Items marked UNKNOWN at intake, unresolved after research phase:

| # | Item | Impact |
|---|------|--------|
| U1 | Kitchen prep area sqm (not demarcated) | Kitchen feasibility scoring uncertain for volume formats |
| U2 | Hood extraction BTU/CFM capacity | Blocks baking/heavy-fry format validation |
| U3 | Alcohol license approval timeline (Halvenia §7) | Blocks evening alcohol-dependent concept evaluation [F14] |
| U4 | Delivery platform coverage + commission rates in Kesselmoor | Blocks delivery-revenue dependent concepts [F13] |
| U5 | Exact weekday office worker headcount (10-min catchment) | Demand sizing uncertain [F01 — PROBABLE, not VERIFIED] |
| U6 | Evening/weekend residential foot traffic (estimated only) | Evening and weekend demand unverified [F03, F04] |
| U7 | Kitchen and service staff wages/availability in Halvenia | Staffing cost and feasibility assumptions unverified |
| U8 | Halvenia hygiene certification timelines | Speed-to-open planning uncertain |

---

## 3. Market Audit Summary

### 3.1 Market context

Valdenfurt's Kesselmoor district sits at the northern fringe of the central business district, adjacent to the post-2000 Neue Kessel residential precinct. Halvenia's food-service sector grew ~4.2% p.a. (2021–2023), with quick-service and café sub-categories outperforming at ~6.1% [F05]. Weekday daytime worker population in the 10-min catchment is estimated at 4,200–5,800 [F01]. The target corner records an estimated 800–1,200 pedestrian crossings per weekday, peaking at lunchtime (11:45–13:30, accounting for 34–39% of daily crossings) [F02]. The Neue Kessel residential precinct contributes approximately 3,100–3,600 residents within 7 minutes, skewing 25–44 years, above-median income [F03]. Weekend foot traffic drops to ~38–43% of weekday volume [F04].

### 3.2 Competitor landscape

Eleven food-service outlets operate in the 10-min catchment: 3 cuisine-specialist dinner restaurants (average cover > HVK 28), 1 established morning bakery (closes 15:00), 2 coffee chains with pre-made sandwiches, 2 independent cafés (light snacks), 1 supermarket deli, and 1 fast-food unit [F06]. No competitor operates a dedicated counter-service hot-lunch format [F07]. The morning bakery gap is partial — Bäckerei Wendl (SYNTHETIC) closes at 15:00 and has no sit-down or brunch service [F08]. Evening dining is thin on casual/mid-price options; three specialist restaurants dominate [F09]. No premium grab-and-go with active delivery-platform listing exists in the catchment [F10].

### 3.3 Demand signals

Office workers are the dominant weekday catchment group [F01, F02]. A single-source survey (ASSUMPTION-tier) suggests ~61% purchase lunch outside the office ≥3 days/week, with "hot meal under HVK 13 within a 5-minute walk" as the most cited unmet need [F11]. A health-food demand trend reportedly tracks ~18% revenue growth in Halvenia urban centers, but this is sourced from a single T4 anecdotal source and is classified USER-PROVIDED ASSUMPTION [F12]. Delivery platform penetration and commission rates in Kesselmoor are UNKNOWN [F13].

> 🟡 **Checkpoint:** Demand dimension contains no PROBABLE+ primary finding. F11 (office preferences) and F12 (health trend) are ASSUMPTION-tier; F13 (delivery) is UNKNOWN. Proceeding with unknown-penalties applied; demand validation is the primary gap for the validation plan.

---

## 4. Constraint Profile

**Hard constraints (inviolable):**
- Operating window: 07:00–22:00 only
- Maximum 4 staff simultaneously — eliminates table-service-heavy formats at scale
- No structural/exterior alterations — limits kitchen expansion, exhaust routing
- No current alcohol license — eliminates alcohol-dependent evening revenue concepts until license obtained (timeline UNKNOWN [F14])
- Capex ceiling: HVK 120,000 — eliminates formats requiring extensive fit-out (e.g., full commercial kitchen, bar infrastructure)

**Binding soft constraints:**
- Ventilation rated for light café use (USER-PROVIDED ASSUMPTION) — a hard question mark for high-heat/high-steam formats (heavy baking, deep-fry, wok-style) until professional HVAC assessment [U2]
- Revenue target HVK 35,000/month — a lunch-only, single-daypart format reaching this target requires 80–100+ covers/day at HVK 12–15 avg; tight but plausible within the estimated catchment [F01, F02, F11]
- 30-month payback on HVK 120,000 = HVK 4,000/month toward capital recovery on top of operating costs — reinforces need for high-margin, high-throughput, or broad-daypart coverage

**Constraint interactions:**
- Max 4 staff + counter service = manageable; max 4 staff + full table service at dinner = tight; max 4 staff + early baking prep + daytime service = likely split-shift complexity
- No alcohol + evening = severely constrained revenue potential for any dinner concept

---

## 5. Concept Set

> Format descriptions only — no names, menus, branding, recipes, or visual identity. Every concept must fit within the constraint profile (Section 4).

- **Concept C1 — Weekday counter-service lunch format:** Counter-only ordering, hot-assembled meals, operating 07:00–15:00 (or similar morning-to-afternoon window). Targets office-worker midday demand in the catchment. Throughput-optimized, limited simultaneous prep complexity, fits 4-staff ceiling. Serves the identified gap in quick, affordable, hot lunch options [F07, F11].

- **Concept C2 — Morning bakery-café hybrid:** Morning-first format (07:00–15:00 / 07:00–18:00), combining specialty coffee with freshly baked or bought-in pastries and light morning meals. Targets the pre-work and mid-morning resident and worker catchment. Partially fills the morning gap left by the existing bakery competitor [F08]. Ventilation constraint is a gating risk for in-house baking [U2].

- **Concept C3 — All-day neighborhood café:** Broad-hours café format (07:00–20:00), coffee + light food throughout the day, serving both office workers (daytime) and residential dwellers (evenings/weekends). Targets the widest possible audience but with lower differentiation. Serves no specific unmet gap; competes directly with existing independent cafés [F06].

- **Concept C4 — Evening small-plates sit-down:** Table-service format, shared small plates, dinner hours (18:00–22:00). No alcohol (license not held, timeline unknown). Targets residential evening diner demand [F03, F09]. The alcohol-free constraint and 4-staff maximum severely challenge the economics of this format.

- **Concept C5 — Premium grab-and-go with delivery component:** Minimal dine-in, throughput-focused, premium prepared items for carry-out and delivery. Targets both in-catchment office workers and potential delivery radius. Exploits the identified absence of this format in the catchment [F10]. Delivery component is contingent on platform coverage and commission viability [F13 — UNKNOWN].

- **Concept C6 — Weekend brunch specialist:** High-cover brunch format operating Saturday and Sunday mornings (09:00–15:00). Targets residential weekend leisure demand [F04]. Revenue is concentrated into two days per week; weekday premises are unutilized. Serves a niche but leaves ~71% of weekly operating days empty.

- **Concept C7 — Health-focused build-your-own bowl/salad counter:** Counter-service, build-your-own cold/warm bowls, targeting office-worker lunch demand with a health-oriented positioning. Simple assembly format, minimal kitchen heat output (ventilation-friendly), fits 4-staff ceiling. Serves the general lunch gap [F07] with a differentiating positioning if health demand trend materializes [F12 — ASSUMPTION].

---

## 6. Scorecards

**Scoring rules applied:**
- Scale: 1 (very poor) to 10 (excellent)
- Equal weights (1/12 per criterion)
- Unknown-evidence penalty: UNKNOWN-backed criterion × 0.5; ASSUMPTION-backed × 0.75
- Penalty applies when UNKNOWN or ASSUMPTION is the **primary** (not merely supplementary) backing for that criterion
- Unsupported criteria (no finding at all) would be nullified; all criteria below have at least one finding

**Penalty flags per concept:**
- C2: Criterion 7 (Kitchen feasibility) → ventilation is USER-PROVIDED ASSUMPTION [U2]; primary constraint source = ASSUMPTION → × 0.75
- C4: Criterion 1 (Market demand) → primary viability depends on alcohol absence, backed by F14 UNKNOWN → × 0.5; Criterion 3 (Revenue potential) → F14 UNKNOWN primary → × 0.5; Criterion 7 (Kitchen feasibility) → ASSUMPTION ventilation → × 0.75; Criterion 9 (Margin potential) → no alcohol = UNKNOWN impact → × 0.5
- C5: Criterion 3 (Revenue potential) → delivery revenue component, primary backing F13 UNKNOWN → × 0.5; Criterion 9 (Margin potential) → delivery commission unknown, F13 UNKNOWN primary → × 0.5
- C7: Criterion 1 (Market demand) → primary backing F01 (PROBABLE office demand); F12 (ASSUMPTION health trend) is supplementary only → no penalty (primary is PROBABLE)

| Criterion | C1 | C2 | C3 | C4 | C5 | C6 | C7 |
|-----------|----|----|----|----|----|----|-----|
| 1 Market demand | 8 | 7 | 6 | **3** ×0.5[F14] | 7 | 5 | 7 |
| 2 Local competitive gap | 8 | 6 | 4 | 7 | 8 | 5 | 7 |
| 3 Revenue potential | 6 | 6 | 5 | **2** ×0.5[F14] | **3** ×0.5[F13] | 3 | 5 |
| 4 Speed to test | 8 | 7 | 7 | 4 | 7 | 6 | 8 |
| 5 Investment efficiency | 8 | 6 | 7 | 4 | 8 | 4 | 8 |
| 6 Staff feasibility | 7 | 5 | 7 | 4 | 8 | 7 | 8 |
| 7 Kitchen feasibility | 8 | **4** ×0.75[U2] | 7 | **4** ×0.75[U2] | 7 | 7 | 8 |
| 8 Property compatibility | 8 | 8 | 7 | 5 | 8 | 5 | 7 |
| 9 Margin potential | 7 | 7 | 5 | **2** ×0.5[F14] | **3** ×0.5[F13] | 7 | 6 |
| 10 Marketing clarity | 9 | 8 | 4 | 5 | 7 | 8 | 7 |
| 11 Long-term defensibility | 5 | 7 | 4 | 5 | 5 | 6 | 5 |
| 12 Risk level (inverted) | 7 | 5 | 6 | 2 | 5 | 5 | 7 |
| **Sum** | **89** | **76** | **69** | **47** | **76** | **68** | **83** |
| **Weighted total (/12)** | **7.42** | **6.33** | **5.75** | **3.92** | **6.33** | **5.67** | **6.92** |
| **Rank** | **#1** | **#3=** | **#5** | **#7** | **#3=** | **#6** | **#2** |

> **Tie at #3:** C2 and C5 share a weighted total of 6.33. The methodology does not specify a tiebreaker. For this run, C2 was selected for the debate as the third entrant due to broader finding coverage (F02, F04, F08) versus C5's reliance on an UNKNOWN-heavy delivery assumption (F13). **This is a methodology gap — see Section 9 and dry_run_review.md.**

**Top-3 for debate:** C1 (7.42) · C7 (6.92) · C2 (6.33)

---

## 7. Debate Summary

Debate conducted across top-3 concepts (C1, C7, C2). Two rounds per concept; critics in order: Financial & Operations → Risk & Constraint → Market / Demand.

---

### C1 — Weekday counter-service lunch

**Round 1**

*Proponent:* Strong, convergent evidence: 4,200–5,800 office workers within 10 min [F01], peak midday foot traffic at 34–39% of daily crossings [F02], and no competing hot-lunch counter in the catchment [F07]. Format is counter-only, fits 4-staff ceiling, low capex, clear marketing identity. The gap is real and unserved.

*Financial & Ops:* Peak window is 3 hours (11:30–14:30). To hit HVK 35,000/month on a lunch-only format at HVK 12–14 average cover: requires 83–97 covers/day × 22 days. At 30 seats with ~1.5 turns in 3 hours, realistic covers are 40–50 seated + counter walk-ins. Throughput target is achievable but tight; a slow ramp-up would miss the monthly revenue target for 6–12 months.

*Risk & Constraint:* Revenue concentration in one daypart is the primary risk. One competitor entering the same gap breaks the model. F01 is PROBABLE, not VERIFIED — if actual office count is at the low end (4,200), demand may not sustain 90+ covers/day.

*Market / Demand:* F11 (lunch preference survey) is ASSUMPTION-tier: 61% buy lunch outside is plausible but unverified. Average spend ceiling "under HVK 13" is a hard constraint on revenue per cover.

*Rebuttal:* Revenue target is owner-stated, not a hard constraint imposed by the concept. A 6-month ramp-up to full throughput is realistic; early months at 50 covers/day still generate HVK 16,500/month — covering opex. Counter + takeaway extends beyond the 3-hour window if a breakfast-coffee offer is added (this does not change the concept format). F01 is the strongest available evidence and meets the discovery bar (PROBABLE acceptable per G4 Phase 1–4).

**Unresolved after Round 1:** (a) Actual cover capacity (40–50 vs. 90+) needs a field test. (b) No evidence on queue tolerance / speed of service requirements in Kesselmoor. (c) Breakfast add-on would extend revenue window but is a format extension not yet scoped.

**Round 2**

*Financial & Ops:* Even granting ramp-up, the payback on HVK 120,000 capex at HVK 35,000 revenue and 18% margin = HVK 6,300/month net; 120,000 / 6,300 = ~19 months if revenue target is hit. That's better than the 30-month ceiling. However, if margin is 12–15% during ramp-up, payback stretches to 26–33 months — borderline.

*Risk & Constraint:* The 4-staff constraint limits throughput in the peak window. Two kitchen staff + two front-of-house = 4. Bottleneck risk at 80+ covers in 90 min is real.

*Market / Demand:* F07 (no hot-lunch competitor) is a derived finding, not independently verified. A competitor could already be planning entry. PROBABLE is not VERIFIED.

*Rebuttal:* Bottleneck risk is legitimate and surfaces in the validation plan. Revenue modeling at margin range is noted as a key assumption. Format is resilient to one competitor if quality/speed is differentiated.

**Final unresolved questions (C1):** Actual cover throughput in peak window; viability of breakfast extension; competitor intelligence freshness.

---

### C7 — Health-focused build-your-own bowl/salad counter

**Round 1**

*Proponent:* Highest kitchen feasibility score (8/10) — cold/warm assembly generates minimal heat, making limited ventilation a non-issue [U2 resolved for this format]. Assembly model fits 4 staff perfectly. Gap evidence [F07] supports differentiated positioning. Simple capex profile — likely HVK 60,000–80,000, well under ceiling.

*Financial & Ops:* The critical question: what is the average cover price for a health-bowl concept in Halvenia? If pricing at HVK 14–18 (premium), covers needed drop to 55–70/day (achievable). If market forces limit pricing to HVK 10–12 (competitive pressure), we need 80–100 covers/day — same constraint as C1. Ingredient cost for fresh produce (CoGS ~32–38%) is higher than processed-food counters, reducing margin potential vs. C1.

*Risk & Constraint:* F12 (health trend) is ASSUMPTION-tier and a single T4 source. If health demand in Kesselmoor is weaker than assumed, the differentiated positioning loses its anchor. The concept then competes on price/convenience — losing to C1 on marketing clarity (C1 scores 9 vs. C7's 7).

*Market / Demand:* F11 (office worker preferences) mentions "hot meal" as the primary unmet need — not specifically healthy options. C7 may be solving a secondary preference, not the primary gap.

*Rebuttal:* F12 is supplementary, not foundational. The concept rests on the established office lunch demand [F01] and the competitive gap [F07]. Health positioning is a differentiator that raises willingness-to-pay, not the sole demand driver. Even at HVK 15 average cover, 60 covers/day at 22 working days = HVK 19,800/month — viable for a ramp phase.

**Unresolved after Round 1:** (a) Achievable price point for health bowl in Halvenia (no local evidence). (b) Whether office workers in Kesselmoor identify "healthy" as a priority vs. "hot and fast."

**Round 2**

*Financial & Ops:* Fresh produce supply chain in Halvenia — no evidence on reliability, seasonal variation, or supplier availability in Valdenfurt. CoGS volatility risk is real.

*Risk & Constraint:* Without F12 being upgraded from ASSUMPTION, the health positioning is effectively unverified. If the positioning fails to resonate, the format competes as a generic salad counter with no clear differentiation from existing light-meal options [F06].

*Market / Demand:* Concurs: F11 specifies "hot meal" preference, not "healthy option." C7 needs to bridge this gap in the validation plan.

*Rebuttal:* "Build-your-own warm bowl" directly addresses the "hot meal" preference (F11) while adding a health frame. The two are not mutually exclusive. Supply chain risk is universal to all fresh-food formats and not specific to C7.

**Final unresolved questions (C7):** Achievable price point; strength of health preference vs. pure convenience demand; fresh supply chain reliability.

---

### C2 — Morning bakery-café hybrid

**Round 1**

*Proponent:* Morning window (07:00–14:00) avoids noise-ordinance risk, leaves afternoon free, and targets two demand groups: commuting office workers (F01, F02) and early-rising residents (F03). Bakery-café units demonstrate high per-transaction value (coffee + pastry = HVK 8–12 avg) and strong repeat custom. Partial competitive gap: Bäckerei Wendl closes 15:00, no sit-down competitor [F08].

*Financial & Ops:* The ventilation constraint (USER-PROVIDED ASSUMPTION [U2]) is the central blocker. High-volume in-house baking requires adequate make-up air; the current single rear duct may be insufficient. If baking is outsourced or bought-in, the "bakery" differentiation weakens. At HVK 9 avg transaction × 200 daily transactions = HVK 1,800/day × 22 days = HVK 39,600/month — but 200 transactions in a 7-hour window = 28/hour, feasible at a counter. This is the rosiest scenario.

*Risk & Constraint:* Morning ramp before 09:00 requires staff at 06:00–06:30 (prep). With a max-4-staff constraint, this means the same people open, prep, and serve — split-shift management complexity. The pre-1950 listed building may complicate exhaust routing if ventilation needs upgrading.

*Market / Demand:* F02 shows morning peak but does not distinguish pre-work foot traffic from lunch traffic. Morning share of that 800–1,200/day count is not separately evidenced. Morning consumer numbers may be materially lower than the midday peak.

*Rebuttal:* Ventilation is the decisive unknown; this must be field-tested before commitment (HVAC assessment is the first validation step). Bought-in pastries are a viable fallback that preserves the café format without the baking constraint. Staff scheduling complexity is manageable with 4 people at the scale of a 85-sqm morning counter.

**Unresolved after Round 1:** (a) HVAC capacity assessment — blocking item. (b) Morning-specific foot traffic share (not evidenced in F02). (c) Sourcing model: in-house vs. bought-in pastries.

**Round 2**

*Financial & Ops:* If bought-in pastries, CoGS is ~45–55% (wholesale bakery supply) vs. 28–35% (in-house). Margin drops from 7/10 to potentially 4–5/10. The economics of bought-in bakery-café approach the all-day café (C3) rather than a differentiated bakery.

*Risk & Constraint:* Ventilation assessment is a hard prerequisite; this concept cannot proceed to recommendation without it. The methodology correctly flags it (unknown-penalty applied to kitchen feasibility).

*Market / Demand:* Morning visitor count (pre-work commuters + early residents) is not independently evidenced — it is inferred from F02's aggregate daytime count. This is a critical gap.

*Rebuttal:* Acknowledged. C2 is the most constraint-contingent concept in the set. Its attractiveness is real but entirely conditional on the HVAC assessment result and a sourcing model decision.

**Final unresolved questions (C2):** HVAC capacity — blocking; morning-specific traffic count; bought-in vs. in-house sourcing economics.

---

### Key cross-concept unresolved questions

1. Does the morning window (C2) or lunchtime window (C1/C7) generate sufficient volume to hit HVK 35,000/month — or does viability require extending to multiple dayparts?
2. What is the realistic throughput ceiling with 4 staff in a counter-service format during a 90-minute peak?
3. Is the health positioning (C7) price-differentiating or merely a segment assumption?
4. Can C1 and C7 be operated as a combined counter (hot + health) within 85 sqm and 4 staff? (Out of scope for this run; flagged as a post-verdict question for L0.)

---

## 8. Verdict

### Arbiter findings

**Applying G4 validation bar:** VERIFIED decisive findings required for RECOMMENDED. All decisive findings in this run are PROBABLE (at best) or ASSUMPTION/UNKNOWN. No concept can be classified RECOMMENDED.

---

**Winner #1 — C1: Weekday counter-service lunch → CONDITIONAL**

*Decision:* CONDITIONAL — sound format, survivable debate, best score, strongest convergent evidence. Decisive findings (F01, F02, F07) are all PROBABLE, not VERIFIED. Cannot advance to RECOMMENDED without field verification of demand count and competitive gap freshness.

*Justification:* C1 is the most constraint-compliant, evidence-backed concept in the set. It exploits the single clearest market gap (no hot-lunch counter [F07]) with the highest-confidence demand signal (office worker density [F01] + peak foot traffic [F02]). Format fits every hard constraint: counter-only, 4 staff, no alcohol, no structural work, capex within ceiling. Revenue model is tight but plausible at 80–100 covers/day if demand verifies.

*Decisive findings:* F01 (catchment demand — PROBABLE), F02 (foot traffic + midday peak — PROBABLE), F07 (competitive gap — PROBABLE).

*Open risks:* (a) Daily cover count unverified — F01 is PROBABLE not VERIFIED; actual lunch demand may not sustain 80–100 covers. (b) Revenue concentration in one daypart — a slow ramp-up may push payback beyond 30 months. (c) Low defensibility (score 5/10) — format is replicable; a competitor could enter the same gap.

---

**Winner #2 — C7: Health-focused bowl/salad counter → CONDITIONAL**

*Decision:* CONDITIONAL — strong feasibility profile, kitchen-constraint-friendly, sound demand basis. Decisive findings (F01, F07) are PROBABLE. F12 (health trend) is ASSUMPTION and supplementary; C7 does not depend on it for viability, only for premium positioning.

*Justification:* C7 matches C1 on feasibility scores and exceeds it on kitchen compatibility (ventilation non-issue). Differentiated positioning raises potential willingness-to-pay. The debate surfaced that "build-your-own warm bowl" satisfies the "hot meal" demand signal [F11] while adding a health frame — the two are not in conflict. Revenue target viability at HVK 15+ avg is plausible if positioning holds.

*Decisive findings:* F01 (PROBABLE), F02 (PROBABLE), F07 (PROBABLE).

*Open risks:* (a) Health demand (F12) is ASSUMPTION — if positioning fails to resonate, C7 becomes a generic salad counter with weaker scores. (b) Achievable price point in Halvenia is unknown — margins depend on pricing above HVK 13–14. (c) Fresh supply chain reliability unverified.

---

**Rejected concepts:**

- **C2 (Morning bakery-café):** CONDITIONAL — lower. Attractive format but gated on a blocking unknown: HVAC capacity [U2]. Cannot be scored reliably on kitchen feasibility until a professional assessment is done. Revisit after ventilation assessment; may upgrade to full CONDITIONAL.
- **C3 (All-day neighborhood café):** REJECTED — weak competitive gap (score 4/10), no clear differentiation, directly competes with established operators [F06]. Does not earn its capex.
- **C5 (Premium grab-and-go + delivery):** REJECTED at this stage — delivery component is the concept's primary differentiator, and delivery platform coverage and commission rates are UNKNOWN [F13]. Without this data, the revenue model cannot be validated. May revisit after F13 is resolved.
- **C6 (Weekend brunch specialist):** REJECTED — revenue potential fatally constrained by two-day operating window (score 3/10). Does not approach HVK 35,000/month target. Cannot overcome revenue concentration risk within the constraint profile.
- **C4 (Evening small-plates, no alcohol):** REJECTED — multiple hard constraint violations compound: no alcohol license (timeline UNKNOWN [F14]), max-4-staff ceiling hit by table service at dinner, no alcohol severely constrains evening revenue, ventilation concerns for intensive kitchen. Worst weighted total (3.92). INSUFFICIENT_EVIDENCE for alcohol viability.

*`no_concept_validated = false`* — two candidates (C1, C7) are CONDITIONAL; the methodology's "no concept sufficiently validated" outcome does not apply here, but neither concept is RECOMMENDED.

---

## 9. Key Assumptions

All USER-PROVIDED ASSUMPTION items relied upon in the scoring and verdict:

| # | Assumption | Used in | If wrong, impact |
|---|-----------|---------|-----------------|
| A1 | Premises 85 sqm / ~30 seats (not surveyed) | All concepts | Format sizing, throughput estimates |
| A2 | Kitchen ventilation: "limited" — single rear duct, no make-up air | C2 kitchen score; C4 kitchen score | C2 upgrade or downgrade pending HVAC |
| A3 | Gas available, hood present (capacity unrated) | All kitchen-dependent concepts | High-heat formats may be further constrained |
| A4 | Max 4 staff simultaneously (lease/planning restriction) | All concepts | If wrong, table-service concepts (C4) become more viable |
| A5 | No alcohol license; acquisition timeline UNKNOWN | C4 revenue/margin; C2 future expansion | C4 rejection could be reversed |
| A6 | Budget capex ceiling HVK 120,000 (stated, not committed) | Investment efficiency scores | Concepts eliminated by capex may reopen |
| A7 | Target monthly revenue HVK 35,000 (owner-stated) | Revenue potential scores; verdict | A lower target makes more concepts viable |
| A8 | Office worker lunch preference: "hot meal under HVK 13" [F11] | C1 and C7 demand framing | If wrong, demand for those formats weakens |
| A9 | Health food demand trend ~18% growth [F12] | C7 positioning premium | If wrong, C7 reverts to generic positioning |

---

## 10. Missing Evidence

What would most increase confidence in the verdict:

| Priority | Evidence needed | Would upgrade | Method |
|----------|----------------|---------------|--------|
| 1 | Actual weekday office worker headcount, Kesselmoor 10-min catchment (ground count or registry) | F01: PROBABLE → VERIFIED | Physical count + Halvenia employment registry query |
| 2 | Morning + lunchtime pedestrian count split (not aggregate daily) | F02: PROBABLE → VERIFIED (more granular) | 5-day intercept count with hourly breakdown |
| 3 | HVAC capacity assessment for the specific premises | U2: UNKNOWN → VERIFIED (specific) | Licensed HVAC engineer site visit |
| 4 | Office worker lunch preferences — Kesselmoor specific survey | F11: ASSUMPTION → PROBABLE | 30–50 intercept interviews at lunchtime |
| 5 | Delivery platform (ValdenEats/FlixFood) coverage + commission structure | F13: UNKNOWN → KNOWN | Direct platform inquiry + test account |
| 6 | Alcohol license timeline — Halvenia Licensing Act §7 inquiry | F14: UNKNOWN → PROBABLE | One phone call / written inquiry to licensing authority |
| 7 | Health-bowl / salad demand signal — Valdenfurt specific | F12: ASSUMPTION → PROBABLE | Local food-service operator interviews; platform search |
| 8 | Fresh produce supplier availability and pricing — Valdenfurt | New finding for C7 CoGS | Market inquiry; wholesale directory |

---

## 11. Validation Plan (2–4 weeks)

Objective: upgrade CONDITIONAL → RECOMMENDED for C1 or C7 by converting decisive PROBABLE findings to VERIFIED and resolving key UNKNOWN items.

**Week 1**
- [ ] Conduct a 5-day pedestrian intercept count at Mühlenweg/Kesseler Allee, with hourly breakdown (07:00–19:00). Target: upgrade F02 to VERIFIED and obtain morning-split data. Cost: 0 (self-conducted).
- [ ] Submit written inquiry to Halvenia Licensing Authority (Valdenfurt office) requesting estimated timeline for §7 alcohol license. Target: resolve F14 from UNKNOWN. Cost: 0.
- [ ] Contact ValdenEats and FlixFood platforms to confirm Kesselmoor postcode coverage and obtain new-entrant commission rate schedule. Target: resolve F13 from UNKNOWN. Cost: 0.

**Week 2**
- [ ] Conduct 40–50 lunchtime intercept interviews with office workers in Kesselmoor (outside office buildings 12:00–13:30). Questions: lunch frequency, spend ceiling, preferred format, current options. Target: upgrade F11 from ASSUMPTION to PROBABLE; new finding for C7 price-point. Cost: 0 (self-conducted) or HVK 200–400 (incentive vouchers).
- [ ] Commission HVAC engineer site assessment of the premises (ventilation capacity, make-up air options, upgrade cost estimate). Target: resolve U2; inform C2 viability and C4 kitchen score. Cost: HVK 300–600 estimated.
- [ ] Cross-check Halvenia employment registry (HalvStats) for Kesselmoor sub-district headcount data to corroborate or contradict F01. Target: upgrade F01 from PROBABLE toward VERIFIED.

**Week 3**
- [ ] Conduct 3 lunch-hour observation sessions (Tuesday, Wednesday, Thursday) at the Bäckerei Wendl competitor and the two sandwich counters [F08, F06]: queue length, throughput, average transaction time. Document whether existing demand is captured or spilling over. Target: upgrade F07 from derived to independently observed.
- [ ] Query 2–3 local wholesale produce distributors for Valdenfurt: product range, minimum order, pricing, delivery reliability. New finding for C7 supply chain risk.

**Week 4**
- [ ] Run a 3-day pop-up or survey test at the target site (if accessible under short-term access agreement): display a simple concept menu card for a health-bowl or lunch counter; collect preference votes from passersby. Cost: HVK 200 estimated. Target: real signal for C1 vs. C7 preference.
- [ ] Synthesize all new findings, re-run scoring with upgraded tags, re-apply Arbiter. Target: one concept reaches RECOMMENDED status (VERIFIED decisive findings, surviving debate).

**Exit condition:** Either C1 or C7 decisive findings reach VERIFIED status AND the revenue model is stress-tested with real cover-count data → eligible for RECOMMENDED and L0 presentation.

---

## 12. Confidence Level

**Overall confidence in the methodology run:** Medium-Low

- Two CONDITIONAL candidates identified (C1, C7) — methodology correctly declined to call either RECOMMENDED given PROBABLE-only evidence.
- The "no concept validated" outcome was not triggered, which is appropriate: two credible candidates exist; the evidence gap is closeable in 2–4 weeks.
- Evidence base is thin on the demand side (two ASSUMPTION findings, two UNKNOWN findings). The scoring system correctly deflated scores via the unknown-penalty.
- No forbidden artifacts produced (no menus, branding, recipes, names, financial models, hiring or build-out plans).

**Per-winner confidence:**

| Concept | Confidence | Reason |
|---------|------------|--------|
| C1 (counter-service lunch) | Medium | Best evidence convergence; decisive findings PROBABLE from three independent angles [F01, F02, F07]; gap claim is derived but plausible; format proven in similar markets |
| C7 (health-bowl counter) | Medium-Low | Sound feasibility but dependent on ASSUMPTION-tier positioning (F12); price point unverified; strong operationally but demand validation thinner than C1 |

---

## 13. Evidence Ledger (appendix)

> Full finding records are in `runs/synthetic_001/evidence_ledger.md`. Summary table below for cross-reference.

| ID | Dimension | Claim (short) | Tag | Confidence | Used in |
|----|-----------|---------------|-----|------------|---------|
| F01 | M | 4,200–5,800 weekday workers, 10-min catchment | PROBABLE | Medium | §3.1, C1, C7, C2 demand; scores §6; verdict §8 |
| F02 | M | 800–1,200 pedestrians/day; lunchtime peak 34–39% | PROBABLE | Medium | §3.1, C1, C7 scores; debate §7 |
| F03 | M | 3,100–3,600 residents, 7-min, above-median income | PROBABLE | Medium | §3.1, C4 demand |
| F04 | M | Weekend foot traffic ~38–43% of weekday | PROBABLE | Medium-Low | §3.1, C6 demand |
| F05 | M | Halvenia food-service +4.2% p.a. 2021–2023 | PROBABLE | Medium | §3.1 context |
| F06 | C | 11 outlets in catchment; mix and format breakdown | PROBABLE | Medium | §3.2, C3 gap score |
| F07 | C | No dedicated hot-lunch counter in catchment | PROBABLE | Medium | §3.2, C1/C7 gap score; verdict |
| F08 | C | Bäckerei Wendl: morning bakery, closes 15:00 | PROBABLE | Medium | §3.2, C2 gap score |
| F09 | C | Evening dining thin on casual/mid-price | PROBABLE | Medium-Low | §3.2, C4 gap score |
| F10 | C | No premium grab-and-go + delivery in catchment | PROBABLE | Medium-Low | §3.2, C5 gap score |
| F11 | D | 61% office workers buy lunch out ≥3×/wk; prefer HVK<13 hot | ASSUMPTION | Low | §3.3, C1/C7 demand framing; debate §7 |
| F12 | D | Health-bowl demand ~18% revenue growth, Halvenia | ASSUMPTION | Low | §3.3, C7 positioning; debate §7 |
| F13 | D | Delivery platform coverage + commissions — Kesselmoor | UNKNOWN | N/A | C5 revenue/margin penalty; §10 missing evidence |
| F14 | D | Alcohol license timeline — Halvenia §7 | UNKNOWN | N/A | C4 demand/revenue/margin penalty; §10 missing evidence |

---

**[STOP — Approval Gate]**

No implementation, menus, branding, names, recipes, financial models, marketing campaigns, hiring plans, build-out plans, or any other execution/production artifact beyond this point.

*Next step requires explicit L0 (Human Principal) approval naming the specific artifact or action.*
