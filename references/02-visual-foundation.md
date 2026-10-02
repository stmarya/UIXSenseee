# Visual Foundation

- **Document ID:** UIXS-VF
- **Version:** 0.1.0
- **Status:** Draft
- **Related standards:** FP, IA, AX, RS, DV, QA
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Review cadence:** On normative change and before each stable release

## Contents

- [Purpose](#purpose)
- [Scope](#scope)
- [Out of scope](#out-of-scope)
- [Terminology](#terminology)
- [Core principles](#core-principles)
- [VF-001 — Establish purposeful visual hierarchy](#vf-001--establish-purposeful-visual-hierarchy)
- [Planned rules](#planned-rules)
- [Evidence basis](#evidence-basis)

## Purpose

Define a technology-agnostic visual system that makes importance, relationships, state, and available action perceivable without allowing decoration or visual trends to override user needs, accessibility, or information accuracy.

## Scope

Applies to visual hierarchy, composition, layout, alignment, spacing, density, typography, color, surfaces, borders, elevation, shape, iconography, imagery, emphasis, and the visual treatment of state across interfaces and dashboards.

## Out of scope

This document does not define brand identity, implementation frameworks, CSS architecture, component code, data-visualization chart selection, motion behavior, or responsive breakpoints except where they directly affect visual meaning. Those areas are governed by their own standards.

## Terminology

- **Visual hierarchy:** ordering of perceived importance through position, scale, contrast, spacing, typography, color, and grouping.
- **Emphasis:** deliberate visual prominence assigned to an element.
- **Grouping:** visual indication that elements belong together.
- **Density:** amount of information and controls within an available area.
- **Scanning path:** common sequence in which users inspect visible content.
- **Primary content/action:** information or action most important to the current task.
- **Secondary content/action:** supporting information or less-prominent action.
- **Tertiary content/action:** metadata, assistance, or infrequent action.
- **Surface:** visual container or layer that groups content.
- **Elevation:** perceived layering or distance between surfaces.
- **Semantic color:** color assigned to meaning such as success, warning, or danger.
- **Decorative element:** an element that does not communicate required information or operation.

## Core principles

- **VF-P01 Purpose before decoration:** every strong visual cue has an information or interaction purpose.
- **VF-P02 Importance drives emphasis:** prominence follows user priority, risk, and task sequence.
- **VF-P03 Relationships remain perceivable:** grouping, separation, and order clarify how information relates.
- **VF-P04 Multiple cues communicate meaning:** color, size, position, or shape is not used alone for critical distinctions.
- **VF-P05 Consistency supports recognition:** equivalent roles use consistent visual treatment.
- **VF-P06 Density follows context:** compactness supports expert scanning without reducing comprehension or operability.
- **VF-P07 Content survives adaptation:** hierarchy remains meaningful under zoom, narrow layouts, localization, and alternate themes.
- **VF-P08 Accessibility constrains aesthetics:** visual style never overrides contrast, focus, reading order, or perceivability.

---

## VF-001 — Establish purposeful visual hierarchy

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-003, FP-004, FP-005, IA-002, IA-003, IA-007

### Rule

Visual hierarchy MUST reflect user goals, information importance, task sequence, and risk so users can quickly identify what the interface is, what requires attention, and what action is available next.

### Rationale

Users rarely read every visible element in order. They scan for orientation, status, exceptions, and available action. When every element has equal prominence—or prominence follows decoration and stakeholder preference—users cannot reliably distinguish primary information from supporting detail.

### Hierarchy levels

- **Primary:** page purpose, critical status, core metric, or main task action.
- **Secondary:** explanation, comparison, related control, or supporting analysis.
- **Tertiary:** metadata, helper text, timestamps, secondary links, and low-frequency actions.
- **Critical override:** safety, destructive consequence, blocking error, or material data-quality warning may override the normal hierarchy.

### Requirements

- **VF-001-A — Define the page purpose — MUST.** Every screen or meaningful region must identify the user task, decision, or information outcome its hierarchy supports.
- **VF-001-B — Match prominence to user priority — MUST.** Position, scale, contrast, spacing, and typography must follow task importance, risk, and frequency rather than organizational rank or decoration.
- **VF-001-C — Establish a clear first focus — MUST.** Users should be able to identify the page purpose or most important current information without inspecting every element.
- **VF-001-D — Distinguish hierarchy levels — MUST.** Primary, secondary, and tertiary roles must be visibly different while remaining readable and operable.
- **VF-001-E — Limit competing focal points — SHOULD.** A task region should not contain several equally dominant elements unless the choices are genuinely equal and mutually exclusive.
- **VF-001-F — Use multiple visual cues — MUST.** Critical meaning and hierarchy must not depend only on color, size, weight, position, shape, or motion.
- **VF-001-G — Align visual and semantic order — MUST.** Visual sequence, heading structure, reading order, and keyboard order must not contradict one another.
- **VF-001-H — Group related information — MUST.** Proximity, alignment, shared surface, or headings should make relationships perceivable. Unrelated content must not appear grouped accidentally.
- **VF-001-I — Separate actions by priority — MUST.** Primary, secondary, tertiary, and destructive actions require distinct treatment proportional to consequence and task priority.
- **VF-001-J — Preserve critical prominence — MUST.** Blocking errors, destructive consequences, safety concerns, and material data-quality warnings must not be visually demoted beneath decorative or promotional content.
- **VF-001-K — Avoid hierarchy through size alone — SHOULD NOT.** Very large values or headings require supporting labels, context, and role-consistent typography.
- **VF-001-L — Preserve hierarchy across states — MUST.** Loading, empty, error, success, disabled, and permission states must retain page identity and the next meaningful action.
- **VF-001-M — Preserve hierarchy across adaptation — MUST.** Narrow layouts, zoom, text expansion, localization, dark mode, and high-contrast settings must not remove or reverse essential priority.
- **VF-001-N — Keep decoration subordinate — MUST.** Illustration, gradient, shadow, texture, or animation must not compete with required information or actions.
- **VF-001-O — Support expert density without flattening priority — SHOULD.** Dense dashboards and tools may use compact layouts, but status, exceptions, selected state, and primary action must remain distinguishable.
- **VF-001-P — Avoid card equality by default — SHOULD NOT.** Do not place every section in equally weighted cards when their importance, relationship, or interaction differs.
- **VF-001-Q — Make data hierarchy explicit — MUST.** A metric presentation must distinguish metric name, value, unit, period, comparison, and status; emphasis on the number alone is insufficient.
- **VF-001-R — Do not use stakeholder prominence as evidence — MUST NOT.** A request to “make it bigger” or “put it above the fold” must be evaluated against user need, risk, and task evidence.

### Dashboard policy

A dashboard should normally establish this scanning order:

1. identity, scope, and period;
2. critical alerts or data-quality limitations;
3. primary KPIs and status;
4. comparison or trend explaining change;
5. diagnostic breakdown;
6. detailed records and secondary actions.

This order MAY change when the user's primary task is investigation, triage, or direct record manipulation. The reason must be documented.

### Validation

- **Five-second orientation test:** ask what the page is, what is most important, and what action appears primary.
- **Blur or squint test:** confirm major groups and focal order remain visible without reading details.
- **Grayscale test:** confirm state and hierarchy do not depend on hue alone.
- **Semantic-order test:** compare visual order with headings, DOM/reading order, and keyboard focus.
- **Action-priority test:** ask users to distinguish primary, secondary, and destructive actions.
- **Content-stress test:** use long labels, large values, missing data, errors, and multiple alerts.
- **Adaptation test:** inspect narrow screens, 200% zoom or more, alternate theme, high contrast, and text expansion.
- **Dashboard scan test:** ask users to identify scope, period, status, anomaly, comparison, and evidence.

### Exceptions

Equal emphasis MAY be used for genuinely equal options, comparison tasks, or neutral selection before the user establishes a preference. Immersive or editorial experiences MAY use unconventional hierarchy when task success, accessibility, and orientation remain validated. Brand campaigns do not override critical-product requirements.

### Failure examples

- Every dashboard card uses the same size, color, and emphasis.
- A promotional banner dominates a blocking operational warning.
- Primary and destructive actions have identical styling.
- A large KPI number has no unit, period, or label.
- Visual order differs from keyboard or screen-reader order.
- Active state is communicated only through color.
- Shadows and gradients create false grouping or unnecessary focal points.
- A mobile layout moves secondary promotion above critical status.
- Empty or error state removes page identity and leaves no next action.

### Acceptance

**Fail** when users cannot identify page purpose or primary action, critical information is visually suppressed, visual and semantic order conflict, essential meaning uses one visual cue, or adaptation reverses priority. **Conditional Pass** may cover non-blocking competition between secondary elements with an owner and correction plan. **Pass** requires every relevant MUST and MUST NOT requirement to be satisfied or covered by an approved exception.

## Planned rules

- VF-002 — Use coherent layout, grid, and alignment.
- VF-003 — Apply consistent spacing, proximity, and density.
- VF-004 — Build a readable and scalable typography system.
- VF-005 — Use color purposefully and accessibly.
- VF-006 — Use surfaces, borders, shape, and elevation to communicate structure.
- VF-007 — Use clear and consistent iconography and imagery.
- VF-008 — Maintain visual consistency across states and themes.

## Evidence basis

- [GOV.UK Government Design Principles](https://www.gov.uk/guidance/government-design-principles) — start with user needs and be consistent rather than mechanically uniform.
- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — visibility, consistency, recognition, and minimalist design.
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) — perceivable, operable, understandable, and robust presentation.
- [Material Design: Accessibility](https://m2.material.io/design/usability/accessibility.html) — accessible visual and interaction foundations.
