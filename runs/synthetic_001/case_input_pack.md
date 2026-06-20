# Case Input Pack — synthetic_001

> **⚠ SYNTHETIC / TEST DATA — All location, premise, financial, and operational data in this file is entirely fictional. No real city, address, business, or market is represented. This file exists solely to dry-run the methodology.**

```yaml
# CASE INPUT PACK — one location, neutral data only.
case_id:                 synthetic_001
language_for_report:     en
evidence_mode:           synthetic-only   # live-web / user-provided / synthetic / hybrid

location:
  city:                  Valdenfurt | SYNTHETIC/TEST DATA
  country:               Halvenia (fictional) | SYNTHETIC/TEST DATA
  district_or_zone:      Kesselmoor | SYNTHETIC/TEST DATA
                         # Mixed-use district on the northern edge of the Valdenfurt
                         # central business district, adjacent to a post-2000
                         # residential precinct (Neue Kessel). One commercial high-street
                         # (Mühlenweg) runs east–west; a smaller retail strip on
                         # Kesseler Allee runs north–south.
  area_character:        mixed — office (CBD fringe), residential (Neue Kessel), light
                         retail strip | SYNTHETIC/TEST DATA

premises:
  size_sqm:              85 | USER-PROVIDED ASSUMPTION
                         # Landlord-stated, not independently verified.
  seating_capacity:      ~30 | USER-PROVIDED ASSUMPTION
                         # Estimated from hand-sketched floor plan; not formally surveyed.
  kitchen_capacity:
    hood_extraction:     yes | USER-PROVIDED ASSUMPTION
                         # Landlord confirmed presence; BTU/CFM rating not provided.
    gas_available:       yes | USER-PROVIDED ASSUMPTION
                         # Landlord confirmed; supply pressure not tested.
    ventilation:         limited | USER-PROVIDED ASSUMPTION
                         # Single rear exhaust duct; no mechanical make-up air system.
                         # Rated for light café use; may not support high-volume baking or
                         # heavy fry-line. Professional HVAC assessment not yet conducted.
    prep_area_sqm:       UNKNOWN
                         # Open-plan layout; prep zone not formally demarcated.
                         # Approximately 18–22 sqm estimated by eye only.
  service_capacity:      counter-primary + limited table service (4–6 tables possible)
                         | USER-PROVIDED ASSUMPTION
  property_context:      Ground-floor corner unit at Mühlenweg 14 / Kesseler Allee 3
                         intersection. Two glass frontages (east + south). Estimated
                         800–1,200 pedestrians per weekday past the corner
                         (PROBABLE — see F02). No dedicated parking. Public-transit
                         stop (Bus line 7 + Tram 12) approximately 50 m south.
                         | USER-PROVIDED ASSUMPTION (property description)
                         | PROBABLE (foot-traffic estimate — F02)

financials:
  budget_capex:          HVK 120,000 | USER-PROVIDED ASSUMPTION
                         # Owner-stated ceiling; not yet committed or financed.
  budget_monthly_opex_ceiling:
                         HVK 22,000 | USER-PROVIDED ASSUMPTION
  financial_target:
    target_monthly_revenue:
                         HVK 35,000 | USER-PROVIDED ASSUMPTION
    target_margin_pct:   18 | USER-PROVIDED ASSUMPTION
    target_payback_months:
                         30 | USER-PROVIDED ASSUMPTION

operational_constraints:
  operating_hours_limits:
    - No service before 07:00 | USER-PROVIDED ASSUMPTION — lease clause
    - No service after 22:00  | USER-PROVIDED ASSUMPTION — lease clause
  noise_limits:          Residential noise ordinance applies after 21:00
                         (Halvenia Municipal Code §14 — SYNTHETIC reference)
                         | USER-PROVIDED ASSUMPTION
  renovation_limits:     No structural changes permitted. Exterior façade listed
                         (pre-1950 classified building) — cosmetic interior changes
                         only | USER-PROVIDED ASSUMPTION
  mandatory_services:    none
  licensing_constraints: No alcohol license currently held. Application possible
                         under Halvenia Licensing Act §7 — SYNTHETIC reference.
                         Approval timeline UNKNOWN.
                         | USER-PROVIDED ASSUMPTION
  staffing_constraints:  Maximum 4 staff on premises simultaneously
                         | USER-PROVIDED ASSUMPTION — lease/planning restriction

fixed_restrictions:
  - No structural or exterior alterations
  - No service before 07:00 or after 22:00
  - Maximum 4 simultaneous staff
  - No current alcohol license (acquisition timeline UNKNOWN)

time_horizon_months:     6 | USER-PROVIDED ASSUMPTION
                         # Owner targets open within 6 months of decision.

unknown_data:
  - prep_area_sqm: open-plan; prep zone not formally demarcated
  - hood_extraction capacity rating: presence confirmed, BTU/CFM unknown
  - alcohol license approval timeline in Halvenia
  - delivery platform coverage and commission rates in Kesselmoor
  - exact weekday office worker headcount in the 10-minute catchment radius
  - evening and weekend residential foot traffic (estimated only, not counted)
  - local labor market: kitchen and service staff wage rates and availability
  - Halvenia food-service regulatory requirements (hygiene certification timelines)
```

## Filling notes

- Every value is tagged per methodology rules.
- `evidence_mode: synthetic-only` — no live web searches performed; all findings in the Evidence Ledger are fabricated for methodology testing and labeled SYNTHETIC/TEST DATA.
- The `unknown_data` block was seeded before any research phase; each item surfaces as UNKNOWN in the Evidence Ledger and is carried into the report's Missing Evidence section.
- No brand name, menu, history, website, prior performance data, or visual-identity content is present in this pack (bias firewall).
