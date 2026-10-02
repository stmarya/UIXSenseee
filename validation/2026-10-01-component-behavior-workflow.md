# Component Behavior Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-CB-001
- **Standard version:** 0.11.0
- **Decision:** Promote to Candidate

## Scenario 1 — Controls, forms, and selection

A link submits data, a button navigates, icon-only delete has no name, form placeholders replace labels, validation clears values, checkboxes are used for exclusive choice, and a switch waits for a separate Save action.

Expected rules: CB-001, CB-002, CB-003. Decision: **Fail**.

## Scenario 2 — Tabs, overlays, help, and feedback

Tabs represent sequential checkout steps, required instructions exist only in a tooltip, nested modal dialogs trap focus, a critical error auto-dismisses as a toast, and background interaction remains active behind a modal.

Expected rules: CB-004, CB-005, CB-006, CB-007. Decision: **Fail**.

## Scenario 3 — Collections and command surfaces

A data table has unlabeled columns, hidden row selection, sort removes records, reset changes workspace, every empty/error state says No data, an overflow menu hides the only delete action, and command search mixes navigation with destructive actions.

Expected rules: CB-008, CB-009, CB-010. Decision: **Fail**.

## Aggregate results

| Metric | Result |
|---|---:|
| Expected primary rule routes | 10/10 |
| Correct decisions | 3/3 |
| Findings with correction and verification | 19/19 |
| Overlap cases deduplicated | 6/6 |
| Unexpected primary rules | 0 |
| Critical issues incorrectly passed | 0 |

## Candidate decision

Promote Component Behavior to Candidate. Rendered, keyboard, screen-reader, touch, zoom, localization, and rare-state evidence remains required before Stable status.
