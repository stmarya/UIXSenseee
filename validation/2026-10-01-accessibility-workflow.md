# Accessibility Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-AX-001
- **Standard version:** 0.11.0
- **Decision:** Promote to Candidate

## Scenario 1 — Semantics, keyboard, focus, and forms

A custom checkout has div-based controls without names, heading levels used visually, keyboard traps, invisible focus, placeholder-only labels, color-only errors, and cleared form input.

Expected rules: AX-001, AX-002, AX-003, AX-005. Decision: **Fail**.

## Scenario 2 — Contrast, pointer, and reflow

Normal text is 3.1:1, selected state is color-only, targets are tiny and adjacent, drag is the only reorder method, text clips at 200%, and the page scrolls both directions at 400% zoom.

Expected rules: AX-004, AX-006, AX-007. Decision: **Fail**.

## Scenario 3 — Motion, dynamic updates, and complex data

Auto-playing parallax ignores reduced motion, video lacks captions, session timeout cannot be extended, route changes are not announced, dialog focus escapes, and an interactive chart has mouse-only tooltips with no data alternative.

Expected rules: AX-008, AX-009, AX-010. Decision: **Fail**.

## Aggregate results

| Metric | Result |
|---|---:|
| Expected primary rule routes | 10/10 |
| Correct decisions | 3/3 |
| Findings with criterion direction and correction | 21/21 |
| Overlap cases deduplicated | 8/8 |
| Unexpected primary rules | 0 |
| A/AA blockers incorrectly passed | 0 |

## Candidate decision

Promote Accessibility to Candidate. Product conformance still requires complete-process, criterion-level evidence using rendered experiences and applicable assistive technologies.
