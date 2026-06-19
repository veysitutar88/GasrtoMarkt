# Universal Restaurant Market Research & Concept Discovery — Methodology Package

**Version:** 1.4 (framework-neutral)
**Status:** Methodology instruction package. Documentation-first. No code, no framework, no execution.

## Purpose

A reusable methodology for analyzing **any** restaurant location in **any** city/country/language and proposing economically viable food-service concepts grounded in market evidence and hard site constraints — **never** anchoring on a pre-existing business at the site.

Two firewalls define the whole method:
1. **Methodology ≠ Case data.** This package is reusable and contains no location specifics. All location data lives only in a per-case input pack (see `templates/case_input_pack.md`) and, when a case is run, under a `runs/<case-id>/` folder.
2. **Reasoning ≠ Evidence.** Every market claim must attach to a tagged, cited source. Unsourced market claims are invalid.

## How to use this package

1. Read `10_universal_master_prompt.md` — the system definition that any operator/backend adopts.
2. Read `20_governance.md` — authority, autonomy, source hierarchy, geographic logic, evidence levels, and the configurable defaults.
3. Copy `templates/case_input_pack.md` into `runs/<case-id>/` and fill it for one location (tag every value).
4. Follow `40_workflow_phases.md` Phases 0–7, applying the rules in `30`, `50`, `60`, `70`.
5. Produce the Final Report per `80_report_schema.md` (skeleton in `templates/final_report.md`).
6. Honor `90_approval_gate.md` — STOP at the gate; produce no execution artifacts.

The package is **backend-neutral**: it can be operated by a human, or by any LLM backend (e.g. Codex / Claude / Hermes), single-model or mixed, as a supervisor-authored methodology. Authority attaches to the **role**, never to the model (see `20_governance.md` §G0).

## Package index

| File | Contents |
|------|----------|
| `00_README.md` | This file: purpose, usage, index |
| `10_universal_master_prompt.md` | The reusable system prompt (with authority model embedded) |
| `20_governance.md` | G0 Authority · G1 Autonomy · G2 Source Hierarchy · G3 Geographic Logic · G4 Evidence Levels · Configurable Defaults |
| `30_agent_roles.md` | The 8 agent roles and their boundaries |
| `40_workflow_phases.md` | Phases 0–7 and the Phase-3 gate |
| `50_evidence_rules.md` | Evidence tags, citation requirements, discovery/validation bars |
| `60_scoring_matrix.md` | The 12 scoring criteria, weights, unknown-penalty |
| `70_debate_arbiter_protocol.md` | Structured debate + judge + arbiter decision rule |
| `80_report_schema.md` | The Final Report output schema |
| `90_approval_gate.md` | Hard-stop rules and non-delegable decisions |
| `templates/case_input_pack.md` | Blank, fully tagged case input template |
| `templates/final_report.md` | Empty Final Report skeleton |

## Configurable defaults are not permanent canon

All numeric values in this package (evidence penalties, debate size/rounds, scoring weights, autonomy ceilings) are **configurable defaults**, set per operator/case. They are documented in `20_governance.md`. None is fixed law; adjust them deliberately and record the change.

## What this package is NOT

It is not an implementation. It selects no framework (Python app, OpenAI Agents SDK, LangGraph, CrewAI, etc. all remain open). It runs no case. Building software or running a case requires separate, explicit approval from the Human Principal (L0).
