# Case Input Pack — Template

> The only place location-specific data lives. This template deliberately has **no field** for brand, name, menu, history, website, or current performance — the absence is the first bias firewall. **Tag every value:** `VERIFIED | PROBABLE | USER-PROVIDED ASSUMPTION | UNKNOWN`. Copy this file into `runs/<case-id>/` and fill it in.

```yaml
# CASE INPUT PACK — one location, neutral data only.
case_id:                 # e.g. "case-001"
language_for_report:     # e.g. "de" | "en" | "auto"
evidence_mode:           # live-web | user-provided | synthetic | hybrid

location:
  city:                  # value + tag
  country:               # value + tag
  district_or_zone:      # neighborhood / address zone (exact address not required) + tag
  area_character:        # office / residential / tourist / mixed   + tag

premises:
  size_sqm:              # total usable area            + tag
  seating_capacity:      # planned/possible seats       + tag or UNKNOWN
  kitchen_capacity:
    hood_extraction:     # yes / no / unknown
    gas_available:       # yes / no / unknown
    ventilation:         # adequate / limited / unknown
    prep_area_sqm:       # + tag or UNKNOWN
  service_capacity:      # e.g. counter only / table service possible   + tag
  property_context:      # floor, frontage, foot-traffic notes, parking + tag

financials:
  budget_capex:          # currency + amount            + tag
  budget_monthly_opex_ceiling:   # optional             + tag or UNKNOWN
  financial_target:
    target_monthly_revenue:      # + tag
    target_margin_pct:           # + tag or UNKNOWN
    target_payback_months:       # + tag or UNKNOWN

operational_constraints:
  operating_hours_limits:        # e.g. "no service after 22:00"
  noise_limits:                  # e.g. residential noise cap
  renovation_limits:             # e.g. "no structural changes"
  mandatory_services:            # e.g. "must offer breakfast" (only if truly fixed)
  licensing_constraints:         # e.g. "no alcohol license"
  staffing_constraints:          # e.g. "max 4 staff", skill availability

fixed_restrictions:              # hard legal/zoning/lease restrictions [list]

time_horizon_months:             # decision/launch window

unknown_data:                    # explicit list of fields you cannot provide
                                 # → seeded as UNKNOWN and surfaced in the report's
                                 #   "missing evidence" section
```

## Filling rules

- Tag **every** value. If you cannot provide it, list it under `unknown_data` and mark UNKNOWN — do not guess.
- Do **not** add any brand/name/menu/history/website/performance information. If such data exists, it stays out of this pack (bias firewall).
- Values you assert but have not independently verified are **USER-PROVIDED ASSUMPTION**, not VERIFIED.
