# Final Report Schema

The only output of a run. It ends at the Approval Gate — no execution/production content.

```
FINAL REPORT
1.  Case Snapshot          : neutral inputs as provided (with status tags)
2.  Missing Data           : everything marked UNKNOWN at intake
3.  Market Audit Summary   : market + competitors + demand, each cited
4.  Constraint Profile     : binding constraints distilled from inputs
5.  Concept Set (5–8)      : each = format description + the gap/demand it serves
6.  Scorecards             : 12 criteria × concept, with rationales + Finding refs
7.  Debate Summary         : key arguments, rebuttals, unresolved questions
8.  Verdict
    - Winner #1            : decision, justification, decisive findings, open risks
    - Winner #2 (optional)
    - Rejected concepts    : with kill-reasons
    - OR "No concept sufficiently validated yet" + data gaps to close
9.  Key Assumptions        : all ASSUMPTION-tagged items relied upon
10. Missing Evidence       : what would raise confidence
11. Validation Plan (2–4 wk): cheap field tests to confirm the winner(s)
12. Confidence Level       : overall + per-winner, with the reasoning
13. Evidence Ledger        : full list of Findings + sources (appendix)
[STOP — Approval Gate]
```

## Rules

- Every number in sections 3–8 must be **footnoted** to a Finding in the Evidence Ledger (section 13).
- Each concept in section 5 is a **format description only** — no menus, names, branding, or recipes.
- Section 8 must reflect the Arbiter's G4-compliant decision, including the "insufficient evidence" outcome when applicable.
- Section 11 (validation plan) is the bridge from PROBABLE → VERIFIED: list concrete, cheap, 2–4 week field tests for the load-bearing claims behind any recommendation.
- The report **stops** at the gate. It does not propose implementation, build-out, or any execution artifact.

A blank skeleton is provided in `templates/final_report.md`.
