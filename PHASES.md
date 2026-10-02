# UIXSenseee Delivery Phases

- **Last updated:** 2026-10-01
- **Current phase:** Phase 2 — Interaction Architecture
- **Overall progress toward Stable:** 27%
- **Canonical progress record:** `STATUS.md`

This document divides all remaining work into ordered delivery phases. A phase may begin in preparation before the previous phase is fully Stable, but it may not be marked complete until its exit criteria are satisfied.

## Status legend

- `Completed` — exit criteria satisfied.
- `In progress` — active work exists.
- `Planned` — scope agreed; work not started.
- `Blocked` — cannot proceed without a dependency or decision.

## Phase overview

| Phase | Name | Standard areas | Status | Current result |
|---:|---|---|---|---|
| 0 | Repository Foundation | Skill, governance, templates, status tracking | Completed | Baseline infrastructure available |
| 1 | Core Foundations | FP, IA, VF | Completed | FP, IA, and VF Candidate |
| 2 | Interaction Architecture | IN, CB | In progress | Interaction Standards Candidate; starting Component Behavior |
| 3 | Inclusive & Adaptive Systems | AX, RS | Planned | Not started |
| 4 | Data & Communication | DV, CT | Planned | Not started |
| 5 | Trust & Release Governance | EP, QA | Planned | Not started |
| 6 | Integration & Stable Release | Cross-standard validation and release | Planned | Not started |

---

## Phase 0 — Repository Foundation

**Status:** Completed

### Scope

- Repository structure
- `SKILL.md` and `AGENTS.md`
- Governance and contribution policy
- Rule and exception templates
- Changelog
- General review and release-gate checklists
- Audit and validation directories
- Canonical `STATUS.md` and this phase plan

### Exit criteria

- [x] AI and human entry points exist.
- [x] Normative rule format is defined.
- [x] Lifecycle and progress calculation are defined.
- [x] Audit, validation, exception, and release paths exist.
- [x] Team handoff procedure is documented.

---

## Phase 1 — Core Foundations

**Status:** Completed  
**Current marker:** FP, IA, and VF Candidate

### Scope

1. Foundation Principles (`FP`)
2. Information Architecture (`IA`)
3. Visual Foundation (`VF`)

### Completed

- [x] Foundation Principles initial draft
- [x] Information Architecture IA-001 through IA-008
- [x] IA internal audit
- [x] IA workflow validation
- [x] IA Candidate promotion
- [x] Visual Foundation VF-001 through VF-008
- [x] VF internal audit
- [x] VF workflow validation
- [x] VF Candidate promotion

### Remaining

- [x] Foundation Principles internal audit
- [x] Foundation Principles workflow validation
- [x] Foundation Principles Candidate promotion
- [ ] Rendered and representative-user evidence for IA Stable status
- [ ] Rendered, contrast, focus, reflow, icon, and theme evidence for VF Stable status

### Immediate next action

Phase 1 Candidate exit criteria are complete. Stable evidence remains scheduled for Phase 6.

### Exit criteria

- FP, IA, and VF are at least Candidate.
- Rule ownership and precedence between FP, IA, VF, AX, EP, and QA are documented.
- Candidate audit and validation evidence exists in the repository.
- No unresolved Critical or Major structural finding remains.

---

## Phase 2 — Interaction Architecture

**Status:** In progress
**Immediate next action:** Create Component Behavior structure and CB-001.

### Scope

1. Interaction Standards (`IN`)
2. Component Behavior (`CB`)

### Interaction Standards planned coverage

- Discoverability and predictability
- Affordance
- Feedback and system status
- Interaction states
- Loading and progress
- Motion
- Error prevention
- Undo and recovery
- Destructive actions
- Keyboard interaction

### Component Behavior planned coverage

- Button and link
- Input and form
- Select, checkbox, and radio
- Tabs
- Modal and drawer
- Tooltip and popover
- Notification
- Table
- Search and filter
- Pagination

### Progress

- [x] Interaction Standards document structure
- [x] IN-001 — Make interactions discoverable and predictable
- [x] IN-002 through IN-010
- [x] Interaction Standards internal audit
- [x] Interaction Standards workflow validation
- [x] Interaction Standards Candidate promotion
- [ ] Component Behavior draft, audit, validation, and Candidate promotion

### Deliverables

- `references/03-interaction-standards.md`
- `references/04-component-behavior.md`
- Rule-mapped checklists
- Internal audit reports
- Controlled workflow validations and fixtures

### Exit criteria

- IN and CB reach Candidate.
- Visual state ownership with VF is resolved.
- Accessibility behavior dependencies are documented.
- Component states and destructive flows pass controlled validation.

---

## Phase 3 — Inclusive & Adaptive Systems

**Status:** Planned

### Scope

1. Accessibility (`AX`)
2. Responsive & Adaptive Design (`RS`)

### Accessibility planned coverage

- WCAG 2.2 AA baseline
- Keyboard and focus
- Contrast and non-color cues
- Target size
- Semantic structure
- Forms and errors
- Motion and media
- Charts and complex data
- Screen-reader behavior

### Responsive planned coverage

- Reflow and content priority
- Narrow-screen behavior
- Touch and pointer modality
- Tables and charts
- Orientation
- Zoom and text resizing
- Adaptive density
- Long content and localization

### Deliverables

- `references/06-accessibility.md`
- `references/07-responsive-adaptive-design.md`
- Accessibility and responsive checklists
- Automated and manual test policy
- Internal audits and workflow validations

### Exit criteria

- AX and RS reach Candidate.
- AX is established as the accessibility-conformance authority.
- VF, IN, CB, and RS boundary ownership is reconciled.
- Keyboard, focus, reflow, zoom, and assistive behavior have testable evidence requirements.

---

## Phase 4 — Data & Communication

**Status:** Planned

### Scope

1. Dashboard & Data Visualization (`DV`)
2. Content Design & Microcopy (`CT`)

### Dashboard and visualization planned coverage

- Dashboard hierarchy
- KPI definition
- Chart selection
- Axis and scale
- Comparison and benchmark
- Data color
- Filters and tables
- Missing data
- Forecast and uncertainty
- Prevention of misleading visualization

### Content planned coverage

- User language
- Navigation and action labels
- Instructions
- Error messages
- Empty states
- Confirmation
- Terminology governance
- Number, date, currency, and units
- Localization

### Deliverables

- `references/05-dashboard-data-visualization.md`
- `references/08-content-design-microcopy.md`
- Dashboard and content checklists
- Misleading-data and terminology test fixtures
- Internal audits and workflow validations

### Exit criteria

- DV and CT reach Candidate.
- Data-honesty ownership with FP and EP is resolved.
- Dashboard rules integrate IA, VF, AX, RS, and CT.
- Metrics, units, periods, uncertainty, and labels are testable.

---

## Phase 5 — Trust & Release Governance

**Status:** Planned

### Scope

1. Ethics & Privacy (`EP`)
2. Quality Assurance (`QA`)

### Ethics and privacy planned coverage

- Dark-pattern prohibition
- Consent and refusal
- Privacy and data minimization
- Cancellation
- False urgency and manipulative defaults
- AI disclosure
- Automated decisions
- Notification ethics

### Quality Assurance planned coverage

- Requirement review
- IA and visual review
- Interaction and component review
- Accessibility review
- Dashboard and data review
- Responsive and content review
- Ethics review
- Severity model
- Evidence requirements
- Release decision

### Deliverables

- `references/09-ethics-privacy-policy.md`
- `references/10-quality-assurance.md`
- Consolidated QA checklist
- Severity and release-decision matrix
- Internal audits and workflow validations

### Exit criteria

- EP and QA reach Candidate.
- Dark patterns and high-risk violations block release.
- Every standard maps into the final QA process.
- Pass, Conditional Pass, Fail, exception, and regression policies are consistent.

---

## Phase 6 — Integration & Stable Release

**Status:** Planned

### Scope

- Cross-standard conflict and duplication audit
- End-to-end skill routing validation
- Rendered-interface testing
- Keyboard and screen-reader testing
- Contrast, focus, text-resize, and page-reflow testing
- Localization and right-to-left stress testing
- Representative-user testing
- Dashboard and data-integrity validation
- Rare-state and permission-state regression
- Documentation and link integrity
- Stable release decision

### Deliverables

- Cross-standard ownership matrix
- Integrated regression fixture suite
- Final audit report
- Stable release checklist
- Versioned Stable release and changelog

### Exit criteria

- All 11 standard areas are Stable or explicitly deferred with approved governance.
- No unresolved Critical or Major finding remains.
- Rendered, accessibility, localization, and representative-user evidence exists.
- All repository links, IDs, checklists, and status records pass integrity checks.
- `STATUS.md` reports 100% weighted progress.

## Phase transition policy

A phase transition requires:

1. exit criteria checked in this document;
2. lifecycle updates in `STATUS.md`;
3. corresponding entry in `CHANGELOG.md`;
4. audit and validation evidence linked;
5. mechanical checks for rule IDs, links, and status consistency;
6. one focused commit reporting completed and next work.

## Mandatory progress update policy

Whenever any document, rule group, checklist, audit, validation, or fixture is added or completed:

1. update the relevant phase checklist in this file;
2. update the corresponding standard row and overall metrics in `STATUS.md`;
3. update `CHANGELOG.md`;
4. update the current phase and next action if they changed;
5. push all related progress changes in the same commit.

Work is not considered complete if the normative document was added but `STATUS.md` and this phase record were not updated.
