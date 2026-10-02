# Visual Foundation

- **Document ID:** UIXS-VF
- **Version:** 0.2.0
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
- [VF-002 — Use coherent layout, grid, and alignment](#vf-002--use-coherent-layout-grid-and-alignment)
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

---

## VF-002 — Use coherent layout, grid, and alignment

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-004, FP-005, IA-002, IA-004, VF-001, RS

### Rule

Layout, grid, and alignment MUST create a coherent spatial structure that reflects information relationships, supports scanning and comparison, and preserves logical reading and interaction order across content and viewport changes.

### Rationale

A grid is an alignment and relationship system, not a decorative template. Coherent layout helps users predict where information and actions appear, compare values, perceive groups, and maintain orientation. Arbitrary placement, excessive centering, rigid columns, and visual order that differs from semantic order increase cognitive and accessibility costs.

### Layout model

Document the intended structure of each major screen:

- page regions and their purpose;
- primary content container;
- column relationships;
- alignment anchors;
- fixed, sticky, scrollable, or overlay regions;
- expected reading and focus order;
- behavior under narrow width, zoom, localization, and variable content.

### Requirements

- **VF-002-A — Derive layout from tasks and hierarchy — MUST.** Page regions, columns, and ordering must support the primary task and VF-001 hierarchy rather than fill available space symmetrically.
- **VF-002-B — Establish consistent alignment anchors — MUST.** Related headings, labels, values, controls, and content blocks must share meaningful edges or baselines.
- **VF-002-C — Use a grid as a relationship system — MUST.** Columns and tracks must express grouping, proportion, or comparison; elements must not snap to a grid when doing so obscures their relationship.
- **VF-002-D — Preserve logical reading order — MUST.** Visual placement must not contradict semantic, keyboard, or assistive-technology reading order.
- **VF-002-E — Keep related content spatially connected — MUST.** Labels remain visually associated with values and controls; actions remain associated with the objects they affect.
- **VF-002-F — Separate unrelated regions — MUST.** Spacing, headings, boundaries, or surfaces must prevent accidental grouping.
- **VF-002-G — Use predictable page regions — SHOULD.** Global navigation, local navigation, title, scope, primary content, supporting detail, and contextual actions should remain in stable locations within the same product area.
- **VF-002-H — Size columns according to content purpose — MUST.** Text, tables, charts, forms, and controls require widths that preserve readability, comparison, and operation; equal columns are not a default requirement.
- **VF-002-I — Avoid arbitrary full-width content — SHOULD NOT.** Use full width only when comparison, visualization, table density, or workflow benefits. Long prose should remain within a readable measure.
- **VF-002-J — Avoid arbitrary centering — SHOULD NOT.** Center alignment may support short, low-density content but should not be used for long text, forms, tables, or scan-heavy information.
- **VF-002-K — Reflow without changing meaning — MUST.** Narrow widths and zoom may stack or reorder visual regions only when semantic sequence, task priority, and relationships remain correct.
- **VF-002-L — Prevent page-level horizontal scrolling — MUST.** The primary page must reflow. Bounded components such as wide tables or timelines MAY scroll horizontally when the boundary, direction, and fixed context are clear.
- **VF-002-M — Keep sticky and fixed regions safe — MUST.** Persistent headers, sidebars, toolbars, and bottom actions must not cover content, focus indicators, errors, anchors, or keyboard targets.
- **VF-002-N — Use nested grids deliberately — SHOULD.** A nested grid may support local component alignment but must not break the page's major alignment anchors or create unnecessary visual noise.
- **VF-002-O — Preserve comparison alignment — MUST.** Comparable values, chart baselines, table columns, and repeated KPI structures must align consistently enough to support accurate comparison.
- **VF-002-P — Treat cards as groups, not grid filler — MUST.** Card dimensions and placement must reflect relationship and content; empty space must not be filled with unrelated cards solely to complete a row.
- **VF-002-Q — Avoid masonry for ordered comparison — SHOULD NOT.** Masonry or irregular arrangements must not be used when users need predictable scanning, sequence, or cross-item comparison.
- **VF-002-R — Support variable content — MUST.** Layout must tolerate long labels, translated text, large numbers, missing data, validation messages, and user-generated content without overlap or lost meaning.
- **VF-002-S — Support bidirectional layouts when applicable — SHOULD.** Direction-sensitive placement, icons, and alignment must adapt for right-to-left languages without reversing semantic charts or universal controls incorrectly.
- **VF-002-T — Keep overlays within context — MUST.** Drawers, popovers, menus, dialogs, and tooltips must remain anchored to a perceivable trigger or task context and must not obscure essential information without a route to dismiss or recover.
- **VF-002-U — Make forms follow completion flow — SHOULD.** A single clear progression is preferred; multi-column form layouts require evidence that fields are independent, short, and read correctly across widths.
- **VF-002-V — Do not encode importance only by position — MUST NOT.** Position supports hierarchy but requires labels, headings, status, or other cues because reading patterns vary across devices, languages, and assistive technologies.

### Dashboard policy

- Keep page identity, scope, period, and global controls in a stable region.
- Align repeated KPI labels, values, units, and comparisons.
- Give trends and diagnostic views enough width to preserve scales and labels.
- Place filters near the data scope they control and distinguish global from local controls.
- Avoid forcing every card into equal dimensions when information roles differ.
- Preserve row and column comparison where comparison is the user task.
- Move detail below summary on narrow layouts unless the task is direct record manipulation.

### Validation

- **Alignment audit:** draw major vertical and horizontal anchors and identify unexplained offsets.
- **Reading-order audit:** compare visual order with document, screen-reader, and keyboard order.
- **Reflow test:** inspect narrow widths and at least 200% zoom without page-level horizontal loss.
- **Content stress test:** use long translations, maximum values, error messages, missing data, and multiple actions.
- **Comparison test:** verify comparable metrics and records can be scanned along consistent axes.
- **Sticky-region test:** navigate anchors and keyboard focus while persistent regions are present.
- **Bidirectional test:** mirror eligible structure for right-to-left content when supported.
- **Overlay test:** open menus, drawers, popovers, and dialogs near every viewport edge.
- **Responsive sequence test:** confirm stacking preserves task priority and semantic order.

### Exceptions

Intentional asymmetry MAY be used to communicate priority or support editorial composition when reading order remains clear. Horizontal scrolling MAY be used inside bounded data components where reflow would destroy comparison. Canvas, map, timeline, and node-graph tools MAY use spatial navigation when controls, orientation, alternatives, and keyboard access are provided.

### Failure examples

- A twelve-column grid is applied even when it breaks label–value relationships.
- Visual columns are read in a different order by keyboard or screen reader.
- Every card is stretched to equal height despite unrelated content.
- A long form uses multiple columns and produces an ambiguous completion order.
- A sticky header covers focused controls or anchor destinations.
- The whole page scrolls horizontally at zoomed or narrow widths.
- A wide chart is compressed until labels and scale become unreadable.
- Global and local filters appear in one undifferentiated toolbar.
- Masonry layout prevents row-by-row comparison.
- Translated labels overlap neighboring controls.

### Acceptance

**Fail** when visual and semantic order conflict, related content becomes detached, page-level reflow fails, persistent regions obscure operation, or layout prevents accurate comparison. **Conditional Pass** may cover non-blocking alignment or density issues with an owner and correction plan. **Pass** requires every relevant MUST and MUST NOT requirement to be satisfied or covered by an approved exception.

## Planned rules

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
