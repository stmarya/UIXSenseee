# Foundation Principles Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-FP-001
- **Standard version:** 0.3.0
- **Previous status:** Audited Draft
- **Decision:** Promote to Candidate
- **Method:** Controlled tabletop validation using three representative product-decision scenarios

## Objectives

Validate whether the skill can:

1. select relevant principles without duplicating topic-standard findings;
2. apply precedence when business, aesthetic, accessibility, safety, and user interests conflict;
3. identify automatic-Fail conditions;
4. classify severity consistently;
5. recommend corrections and verification;
6. produce a correct conformance decision.

## Scenario 1 — Feature pressure, clarity, effectiveness, and hierarchy

### Fixture

A stakeholder requests a competitor-style AI assistant without identified user need. The main dashboard uses the label “Boost” for an action that changes forecasts. A promotional adoption card dominates a critical operations alert. A review step is removed from a financial approval flow to increase conversion, despite incorrect approvals in support reports.

### Expected routing

FP-001, FP-002, FP-003, FP-005, and FP-014.

### Findings

| ID | Severity | Primary principle | Related | Finding and correction |
|---|---|---|---|---|
| F1-01 | Major | FP-001 | FP-014 | The AI assistant has no identified need. Create a user/task/risk statement and validate demand before implementation. |
| F1-02 | Major | FP-002 | CT | “Boost” does not communicate effect or consequence. Use an action-and-object label and test prediction. |
| F1-03 | Critical | FP-005 | FP-003, VF | Promotion suppresses a critical alert. Restore risk-based hierarchy and verify rapid orientation. |
| F1-04 | Critical | FP-003 | FP-010, FP-014 | Removing review increases incorrect financial approval risk. Restore proportional review and validate task correctness before conversion optimization. |

### Decision

**Fail.** Critical hierarchy and financial-correctness issues override engagement and aesthetic goals.

### Result

Expected principles selected: 5/5. Topic standards remained related rather than duplicate primary findings.

---

## Scenario 2 — Accessibility, control, prevention, and system status

### Fixture

A form communicates required fields only by red color and exposes help only on hover. Permanent deletion occurs immediately with no confirmation or recovery. A validation failure clears all valid input. A long import shows no progress, then displays “No data” for both failure and empty results. Product leadership accepts these issues to meet a release date.

### Expected routing

FP-004, FP-009, FP-010, FP-011, and FP-003.

### Findings

| ID | Severity | Primary principle | Related | Finding and correction |
|---|---|---|---|---|
| F2-01 | Critical | FP-004 | AX | Required state and help depend on color, hover, and pointer input. Add persistent labels, non-color cues, keyboard access, and accessibility verification. |
| F2-02 | Critical | FP-009 | FP-010 | Permanent deletion lacks confirmation or recovery. Add explicit consequence, proportional confirmation, and recovery where possible. |
| F2-03 | Major | FP-010 | CB | Validation clears correct input. Preserve valid values and focus the actionable error. |
| F2-04 | Major | FP-011 | IN | Import has no progress and conflates failure with empty results. Provide progress and cause-specific recovery states. |
| F2-05 | Critical | FP-003 | FP-004 | Release speed is used to accept a material accessibility barrier. Block release or approve a governed mitigation with evidence and deadline. |

### Decision

**Fail.** Accessibility, control, and irreversible-action issues trigger automatic-Fail policy.

### Result

Expected principles selected: 5/5. Error prevention and user control were consolidated by primary ownership.

---

## Scenario 3 — Disclosure, recognition, consistency, data honesty, and ethics

### Fixture

A subscription flow hides fees and cancellation under several “Learn more” links, preselects marketing consent, and makes rejection visually weak. A dashboard truncates its axis, treats missing data as zero, and labels an AI forecast as “Actual.” Users must remember a project code from another screen. “Archive” deletes items in one area but preserves them in another. Leadership cites “best practice” without evidence.

### Expected routing

FP-006, FP-007, FP-008, FP-012, FP-013, and FP-014.

### Findings

| ID | Severity | Primary principle | Related | Finding and correction |
|---|---|---|---|---|
| F3-01 | Critical | FP-013 | FP-006 | Fees, cancellation, consent, and refusal are manipulated. Present material terms and equivalent choices before commitment. |
| F3-02 | Critical | FP-012 | DV | Truncated scale and missing-as-zero behavior materially distort interpretation. Restore honest scale and explicit missing-data treatment. |
| F3-03 | Critical | FP-012 | FP-013, DV | Forecast is labeled Actual. Identify model output, uncertainty, source, and time horizon. |
| F3-04 | Moderate | FP-007 | IA | Users must recall a project code. Display or select the relevant project at the point of need. |
| F3-05 | Major | FP-008 | CT, CB | Archive has conflicting consequences. Use consistent behavior or distinct labels and migration guidance. |
| F3-06 | Major | FP-014 | — | “Best practice” is asserted without applicability evidence. Record assumption, source, affected users, risk, and validation plan. |

### Decision

**Fail.** Dark patterns and materially misleading data are automatic-Fail conditions.

### Result

Expected principles selected: 6/6. Ethical and disclosure issues were consolidated under FP-013; data interpretation under FP-012.

---

## Aggregate results

| Metric | Result | Target |
|---|---:|---:|
| Expected principle routes selected | 16/16 | 100% |
| Expected conformance decisions matched | 3/3 | 100% |
| Findings with primary principle | 15/15 | 100% |
| Findings with actionable correction | 15/15 | 100% |
| Findings with verification direction | 15/15 | 100% |
| Known overlap cases deduplicated | 6/6 | 100% |
| Unexpected primary principles | 0 | 0 |
| Automatic-Fail issues incorrectly allowed to pass | 0 | 0 |

## Observations

### Strengths

- Precedence correctly favored safety, rights, accessibility, correctness, and honest data over conversion and aesthetics.
- Foundation Principles remained related to specific topic standards without duplicating detailed implementation findings.
- Automatic-Fail policy consistently blocked material accessibility barriers, dark patterns, misleading data, and irreversible uncontrolled actions.
- All 14 principles were exercised across the three scenarios.

### Limitations

- Fixtures are written scenarios rather than rendered products.
- No representative user or assistive-technology session participated.
- Legal and regulatory review was outside scope.
- Stable promotion still depends on integrated evidence from later phases.

## Candidate decision

Promote Foundation Principles from **Audited Draft** to **Candidate**. Use them as the governing precedence layer for Phase 2 onward. Revisit Stable status during Phase 6 integration and release validation.
