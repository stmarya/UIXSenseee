# Visual Foundation Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-VF-001
- **Standard version:** 0.9.0
- **Previous status:** Draft
- **Decision:** Promote to Candidate
- **Method:** Controlled tabletop validation using three representative visual-system scenarios

## Objectives

Validate whether the skill can:

1. select relevant VF rules without applying all visual rules indiscriminately;
2. distinguish Visual Foundation ownership from AX, RS, DV, IN, CT, and EP;
3. classify severity consistently;
4. consolidate overlapping symptoms under one primary rule;
5. recommend corrections with a verification method;
6. produce the correct conformance decision.

## Output contract

Each finding includes evidence, severity, primary rule, related rules, user impact, correction, and verification. Accessibility conformance concerns are related to AX when VF owns the visual implementation symptom.

---

## Scenario 1 — Dashboard hierarchy, layout, and density

### Fixture

An operations dashboard gives every card equal size and elevation. A promotional banner occupies the strongest position while a critical SLA breach appears as small gray text. KPI values have no units or period. Global filters and chart-local filters share one toolbar. On mobile, the chart moves above scope and alerts. A sticky header covers focused controls at 400% zoom. Compact mode removes section spacing and selected-row distinction.

### Expected routing

VF-001, VF-002, and VF-003, with AX and RS as related standards where applicable.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| V1-01 | Critical | VF-001 | AX | Promotion suppresses a critical SLA breach. Promote the breach above decorative content and verify five-second orientation and perceivability. |
| V1-02 | Major | VF-001 | DV | Equal card emphasis flattens KPI, trend, and detail hierarchy. Assign explicit primary, secondary, and diagnostic roles. |
| V1-03 | Major | VF-001 | DV, CT | KPI numbers lack name context, unit, period, and status. Add a consistent KPI information hierarchy. |
| V1-04 | Major | VF-002 | IA | Global and local filters share an undifferentiated region. Separate scopes and align controls with affected data. |
| V1-05 | Major | VF-002 | RS | Mobile stacking reverses hierarchy by moving scope and alerts below charts. Preserve semantic and task order. |
| V1-06 | Critical | VF-002 | AX | Sticky header obscures focused controls at zoom. Reserve safe space and verify keyboard focus at 400% page zoom/reflow. |
| V1-07 | Major | VF-003 | AX | Compact mode removes grouping and selected-row distinction. Restore minimum grouping and redundant selected-state cues. |

### Decision

**Fail.** Critical hierarchy and operability issues block conformance.

### Result

Expected primary rule families selected: 3/3. Reflow and perceivability remained related to AX/RS rather than duplicated as separate primary findings.

---

## Scenario 2 — Typography, color, and analytical meaning

### Fixture

A dashboard uses five unrelated font scales for the same card-title role. Labels are reduced to very small text to fit cards. Links differ from body text only through blue color. Status uses red and green dots without labels. Normal text contrast is 3.2:1. Dark mode is a direct color inversion. “Response time increased” is automatically green even though higher response time is harmful. Long team names truncate to identical prefixes.

### Expected routing

VF-004 and VF-005, with AX, DV, and CT as related standards.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| V2-01 | Moderate | VF-004 | — | Equivalent card-title roles use inconsistent typography. Define and apply one semantic role. |
| V2-02 | Major | VF-004 | AX | Labels are reduced until readability suffers. Change layout or wording rather than shrinking required text. |
| V2-03 | Major | VF-004 | AX | Links depend on color alone. Add underline or another persistent non-color cue and visible focus. |
| V2-04 | Critical | VF-005 | AX | Normal text contrast is 3.2:1. Use compliant text and surface roles and verify actual composited contrast. |
| V2-05 | Critical | VF-005 | AX | Red/green dots are the only status cue. Add text, icon/shape, and accessible status meaning. |
| V2-06 | Major | VF-005 | DV | Increased harmful response time is shown as positive green. Assign color from business meaning, not direction alone. |
| V2-07 | Major | VF-005 | AX | Direct inversion produces invalid dark-theme contrast and semantics. Define and test theme-specific roles. |
| V2-08 | Major | VF-004 | CT | Truncation removes the only distinction between team names. Preserve distinguishing text or provide a reliable full-value presentation. |

### Decision

**Fail.** Contrast and color-only status issues are Critical.

### Result

Expected primary rule families selected: 2/2. VF owns visual implementation; AX remains authoritative for accessibility conformance.

---

## Scenario 3 — Surfaces, icons, states, and themes

### Fixture

The interface uses glass cards over photographs, with shadow as the only boundary. Static cards and clickable cards look identical. Permanent deletion uses an unlabeled trash icon. The same star icon means favorite, featured, and quality rating. Focus disappears when rows are selected. Error and selected states share the same red border. Loading replaces the complete layout and moves actions. Permission-denied and stale-data states are not designed. A local team introduces ungoverned colors and radii.

### Expected routing

VF-006, VF-007, and VF-008, with IN, AX, CT, and EP as related standards.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| V3-01 | Critical | VF-006 | AX | Glass surfaces make contrast depend on photographs. Use stable opaque or controlled surfaces and retest all content. |
| V3-02 | Major | VF-006 | IN | Static and interactive cards are visually indistinguishable. Add consistent affordance to interactive surfaces. |
| V3-03 | Critical | VF-007 | CT, AX | Permanent deletion uses an ambiguous icon-only action. Add an explicit label, accessible name, and proportional confirmation. |
| V3-04 | Major | VF-007 | CT | The star icon has three meanings. Assign distinct symbols or visible labels and document icon semantics. |
| V3-05 | Critical | VF-008 | AX | Focus disappears on selected rows. Ensure focus remains visible over selected, error, and active states. |
| V3-06 | Major | VF-008 | IN | Error and selected states share one treatment. Separate state semantics and test the complete state matrix. |
| V3-07 | Major | VF-008 | IN | Loading replaces layout and moves actions. Use stable regions or meaningful skeleton structure. |
| V3-08 | Major | VF-008 | IN, AX | Permission-denied and stale-data states are missing. Design and validate rare states. |
| V3-09 | Moderate | VF-008 | — | Local tokens create visual drift. Route new tokens and variants through system governance and migration review. |

### Decision

**Fail.** Critical contrast, destructive-action, and focus issues block conformance.

### Result

Expected primary rule families selected: 3/3. Behavioral and accessibility concerns were linked without duplicating the visual findings.

---

## Aggregate results

| Metric | Result | Target |
|---|---:|---:|
| Expected primary rule routes selected | 8/8 | 100% |
| Expected conformance decisions matched | 3/3 | 100% |
| Findings with primary rule ID | 24/24 | 100% |
| Findings with actionable correction | 24/24 | 100% |
| Findings with verification direction | 24/24 | 100% |
| Known overlap cases deduplicated | 8/8 | 100% |
| Unexpected primary rule families | 0 | 0 |
| Critical issues incorrectly allowed to pass | 0 | 0 |

## Observations

### Strengths

- Rule boundaries kept accessibility, responsive, data, content, and interaction concerns related but not duplicated.
- The eight VF areas produced distinct and actionable findings.
- Severity correctly escalated suppressed critical status, contrast failure, color-only status, obscured focus, misleading surfaces, and ambiguous permanent deletion.
- Checklist evidence maps cleanly to the required conformance artifacts.

### Limitations

- Fixtures are written descriptions rather than rendered screens.
- No contrast tool, browser reflow, keyboard, or screen-reader run was executed against a live interface.
- No representative user participated in visual scanning or icon-comprehension tests.
- Cultural interpretation and localization were not tested end to end.

## Candidate decision

Promote Visual Foundation from **Draft** to **Candidate**. Before Stable status, complete at least:

1. one rendered dashboard hierarchy and density review;
2. measured light/dark contrast and focus review;
3. 200% text resize and 400% page zoom/reflow test where applicable;
4. keyboard and screen-reader order review;
5. icon-comprehension and localization stress tests;
6. rare-state and theme regression review.
