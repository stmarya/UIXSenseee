# Component Behavior

- **Document ID:** UIXS-CB
- **Version:** 0.10.0
- **Status:** Draft
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Related standards:** FP, IA, VF, IN, AX, RS, CT, EP, QA

## Purpose

Define consistent, accessible, and predictable behavior for common interface components without prescribing a specific framework or visual library.

## Scope

Covers buttons, links, forms, selection controls, tabs, disclosure, dialogs, drawers, tooltips, popovers, alerts, notifications, tables, lists, search, filter, sort, pagination, menus, navigation, and command surfaces.

## Ownership

CB owns component-specific anatomy and behavior. IN owns cross-component interaction policy; VF owns visual presentation; AX owns accessibility conformance; CT owns final wording; IA owns information structure.

## Core principles

- Components expose purpose, state, scope, and consequence.
- Equivalent components behave consistently.
- Native semantics are preferred when they satisfy the requirement.
- Components remain operable across keyboard, pointer, touch, zoom, and assistive technology.
- Rare, error, loading, empty, permission, and recovery states are designed.

---

## CB-001 — Design buttons and links according to outcome

**Level:** MUST  
**Status:** Draft

### Rule

Buttons MUST trigger actions and links MUST navigate, with labels, priority, state, consequence, and semantics matching the actual outcome.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-001-A — Separate action and navigation — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-B — Use outcome-oriented labels — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-C — Limit primary actions per task region — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-D — Expose loading without duplicate activation — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-E — Keep icon-only actions low-risk and named — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-F — Distinguish destructive actions — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-G — Preserve focus and state — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-001-H — Avoid disabled controls without explanation — SHOULD.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-002 — Build usable text inputs and forms

**Level:** MUST  
**Status:** Draft

### Rule

Inputs and forms MUST provide persistent labels, understandable instructions, preserved values, appropriate validation, and a logical completion flow.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-002-A — Provide persistent labels — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-B — Identify required and optional fields — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-C — Explain format before error — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-D — Use appropriate input type and autocomplete — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-E — Preserve valid input — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-F — Associate helper and error text — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-G — Use logical grouping and order — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-H — Support review for high-impact submission — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-002-I — Avoid placeholder as label — MUST NOT.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-003 — Use selection controls by decision model

**Level:** MUST  
**Status:** Draft

### Rule

Checkboxes, radios, switches, and selects MUST match whether choices are independent, exclusive, immediate, or submitted later.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-003-A — Use checkbox for independent choices — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-B — Use radio for visible exclusive choices — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-C — Use switch for immediate binary state — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-D — Use select for constrained choice sets — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-E — Keep labels clickable and explicit — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-F — Expose selected and mixed states — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-G — Do not auto-submit surprising changes — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-003-H — Preserve keyboard and touch operation — MUST.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-004 — Use tabs and disclosure for the correct relationship

**Level:** MUST  
**Status:** Draft

### Rule

Tabs MUST represent peer views of one context; disclosure components MUST reveal subordinate content without hiding required information.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-004-A — Use tabs for peer views — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-B — Do not use tabs for sequential steps — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-C — Keep active tab perceivable and semantic — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-D — Preserve tab state when useful — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-E — Use disclosure for subordinate detail — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-F — Label disclosure by content — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-G — Expose expanded state — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-004-H — Avoid nested disclosure for primary tasks — SHOULD NOT.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-005 — Use dialogs and drawers without losing context

**Level:** MUST  
**Status:** Draft

### Rule

Dialogs and drawers MUST support focused secondary work while preserving context, focus, exit, consequence, and recovery.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-005-A — Use modal only for focused interruption — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-B — Provide title and explicit close — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-C — Manage initial and returned focus — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-D — Prevent background interaction when modal — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-E — Avoid stacked modals — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-F — Use pages for long complex work — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-G — Protect unsaved work — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-005-H — Keep destructive confirmation specific — MUST.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-006 — Use tooltips and popovers only for supplemental content

**Level:** MUST  
**Status:** Draft

### Rule

Tooltips and popovers MUST remain supplemental, dismissible, keyboard/touch accessible, and associated with their trigger.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-006-A — Do not hide required content — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-B — Use tooltip for brief explanation — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-C — Use popover for richer non-modal interaction — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-D — Support hover and focus or explicit activation — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-E — Provide dismissal — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-F — Keep trigger association — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-G — Avoid interactive content in simple tooltip — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-006-H — Prevent viewport clipping — MUST.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-007 — Use alerts, toasts, and notifications by urgency

**Level:** MUST  
**Status:** Draft

### Rule

Feedback components MUST match urgency, persistence, scope, and required action without interrupting users disproportionately.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-007-A — Use inline messages near context — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-B — Use toast for brief non-critical confirmation — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-C — Use alert for material status or action — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-D — Do not auto-dismiss critical messages — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-E — Announce dynamic status appropriately — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-F — Avoid notification duplication — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-G — Provide action and dismissal when relevant — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-007-H — Preserve notification history for durable events — SHOULD.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-008 — Design tables and lists for scanning and action

**Level:** MUST  
**Status:** Draft

### Rule

Tables and lists MUST preserve row identity, column meaning, selection, sorting, responsive access, and action association.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-008-A — Use table for comparable structured data — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-B — Provide meaningful headers — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-C — Align comparable values — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-D — Keep row actions associated — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-E — Expose selection and batch scope — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-F — Make sorting explicit — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-G — Preserve context through detail and return — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-H — Provide empty loading error and permission states — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-008-I — Support narrow access without losing meaning — MUST.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-009 — Coordinate search, filter, sort, and pagination

**Level:** MUST  
**Status:** Draft

### Rule

Collection controls MUST expose scope, active state, reset behavior, result cause, and persistence without changing unrelated context.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-009-A — Label search scope — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-B — Show query and active filters — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-C — Allow individual filter removal — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-D — Keep sort to ordering only — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-E — Make pagination position and total understandable — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-F — Preserve state through detail and return — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-G — Distinguish no data no result error and permission — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-H — Make reset effects explicit — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-009-I — Support shareable state when safe — SHOULD.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

---

## CB-010 — Design menus, navigation, and command surfaces predictably

**Level:** MUST  
**Status:** Draft

### Rule

Menus and command surfaces MUST distinguish destinations, actions, hierarchy, shortcuts, scope, and dangerous consequences.

### Rationale

The component must match the user's mental model, communicate state and consequence, and remain consistent across contexts and input modalities.

### Requirements

- **CB-010-A — Group related items and separate destructive items — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-B — Distinguish navigation and commands — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-C — Expose submenu relationships and state — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-D — Support keyboard navigation and escape — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-E — Keep context menus non-exclusive — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-F — Label command types and scope — MUST.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-G — Expose shortcut safely — SHOULD.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-H — Avoid hidden essential actions in overflow — MUST NOT.** Apply this requirement using native semantics and explicit state where available.
- **CB-010-I — Preserve current location in navigation — MUST.** Apply this requirement using native semantics and explicit state where available.

### Validation

Test default, focus, active, selected, disabled, loading, error, empty, permission, keyboard, touch, zoom, localization, and assistive-technology behavior as applicable.

### Exceptions

Specialized expert tools MAY vary presentation when equivalent semantics, operation, consequence, and recovery remain available.

### Failure examples

Wrong component model, hidden state or scope, inaccessible operation, lost input, ambiguous consequence, and inconsistent behavior across equivalent contexts.

### Acceptance

Fail when component purpose, state, scope, consequence, or essential operation is unavailable or misleading. Conditional Pass requires non-blocking issues with ownership and verification. Pass requires all relevant mandatory rules or approved exceptions.

## Component Behavior conformance

A design conforms only when every relevant MUST and MUST NOT requirement from CB-001 through CB-010 passes or has an approved exception.

### Required evidence

- component inventory and ownership;
- state matrix;
- labels, scope, and consequences;
- keyboard, touch, focus, and assistive semantics;
- loading, empty, error, permission, and recovery states;
- responsive and localization behavior;
- completed checklist and exceptions.

## Evidence basis

- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [WAI Forms Tutorials](https://www.w3.org/WAI/tutorials/forms/)
- [GOV.UK Design System Components](https://design-system.service.gov.uk/components/)
- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)
