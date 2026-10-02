# Responsive & Adaptive Design Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-RS-001
- **Standard version:** 0.11.0
- **Decision:** Promote to Candidate

## Scenario 1 — Priority, reflow, breakpoints, and navigation

A mobile dashboard moves promotion above critical alerts, clips content at intermediate widths, uses device-name breakpoints with gaps, hides active navigation, and loses parent context after menu collapse.

Expected rules: RS-001, RS-002, RS-003, RS-004. Decision: **Fail**.

## Scenario 2 — Forms, tables, and charts

A two-column form reorders fields incorrectly, virtual keyboard covers Save, a table converts to cards and hides comparison, chart labels become unreadable, and mobile chart changes scale and omits uncertainty.

Expected rules: RS-005, RS-006, RS-007. Decision: **Fail**.

## Scenario 3 — Modality, localization, and state

The product locks portrait orientation, depends on hover, ignores safe areas, truncates long translations, breaks RTL layout, resets filters at a breakpoint, downloads hidden heavy charts, and loses draft state after resize.

Expected rules: RS-008, RS-009, RS-010. Decision: **Fail**.

## Aggregate results

| Metric | Result |
|---|---:|
| Expected primary rule routes | 10/10 |
| Correct decisions | 3/3 |
| Findings with correction and verification | 20/20 |
| Overlap cases deduplicated | 8/8 |
| Unexpected primary rules | 0 |
| Critical issues incorrectly passed | 0 |

## Candidate decision

Promote Responsive & Adaptive Design to Candidate. Stable evidence requires rendered task flows across adaptive conditions and applicable Accessibility criteria.
