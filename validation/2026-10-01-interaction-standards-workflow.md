# Interaction Standards Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-IN-001
- **Standard version:** 0.11.0
- **Decision:** Promote to Candidate

## Scenario 1 — Affordance, feedback, and states

A dashboard uses identical static and clickable cards, icon-only publish, no activation feedback, selected and error rows share styling, focus disappears, and disabled export has no permission explanation.

Expected primary rules: IN-001, IN-002, IN-003, IN-004. Decision: **Fail**.

Findings correctly assigned false affordance to IN-002, hidden consequence to IN-001, absent outcome to IN-003, and conflicting/focus states to IN-004 without duplication.

## Scenario 2 — Loading, motion, and errors

A long import shows fake 99% progress, retry duplicates jobs, auto-animated KPI cards ignore reduced motion, validation clears correct input, and server failure is shown as user error.

Expected primary rules: IN-005, IN-006, IN-007. Decision: **Fail**.

Critical issues: deceptive progress, duplicate consequential jobs, inaccessible motion, and destructive validation.

## Scenario 3 — Recovery, destructive action, and modalities

Closing a dialog silently saves; payment retry duplicates charges; bulk delete hides record count; delete sits beside save; reorder is drag-only; a modal traps keyboard focus; screen-reader state differs from visible selection.

Expected primary rules: IN-008, IN-009, IN-010. Decision: **Fail**.

Critical issues: duplicate payment, hidden destructive scope, keyboard trap, and modality-only operation.

## Aggregate results

| Metric | Result |
|---|---:|
| Expected primary rule routes | 10/10 |
| Correct conformance decisions | 3/3 |
| Findings with primary rule and correction | 18/18 |
| Overlap cases deduplicated | 7/7 |
| Unexpected primary rules | 0 |
| Critical issues incorrectly passed | 0 |

## Candidate decision

Promote Interaction Standards to Candidate. Stable evidence requires rendered components, keyboard and screen-reader flows, reduced motion, timing, async failure, and representative-user testing.
