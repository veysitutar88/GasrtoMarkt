# Approval Gate Rules

## Hard stop

The run terminates at **Phase 7**, immediately after the Verdict and Final Report. No further generation occurs without a new, explicit approval from the Human Principal (L0).

## Forbidden without explicit, separate approval

**Production / execution artifacts:** menus, recipes, branding, names, visual identity, supplier/procurement lists, full financial models, marketing campaigns, hiring plans, build-out/renovation plans, or any other execution/production output.

**Build-side actions:** creating or editing repository files, scaffolding code, installing packages, running scripts, selecting/locking a framework, or running any case (synthetic or real).

**External actions:** contacting third parties, sending messages, posting publicly, logging into sites, or representing the user externally.

(These mirror the 🔴 zone in `20_governance.md` §G1.)

## Non-delegable human decisions (G0)

The following can be performed **only** by L0 (the Human Principal) and by no agent or backend:
- selecting the substrate/framework;
- lifting the approval gate;
- authorizing real spend beyond configured caps;
- any 🔴 action;
- producing execution/production artifacts.

## Resumption

Only an explicit user approval **naming the next artifact or step** lifts the gate, and only for that named step. A general "continue" does not authorize a forbidden action.

## Structural enforcement (for any future coded realization)

When this methodology is later implemented in software, the executed flow should contain **no capability** to produce the forbidden artifacts above — so the stop cannot be bypassed by a prompt. (Implementation of this enforcement is itself a build action requiring separate approval.)
