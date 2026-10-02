# Visual Foundation

- **Document ID:** UIXS-VF
- **Version:** 0.9.0
- **Status:** Candidate
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
- [VF-003 — Apply consistent spacing, proximity, and density](#vf-003--apply-consistent-spacing-proximity-and-density)
- [VF-004 — Build a readable and scalable typography system](#vf-004--build-a-readable-and-scalable-typography-system)
- [VF-005 — Use color purposefully and accessibly](#vf-005--use-color-purposefully-and-accessibly)
- [VF-006 — Use surfaces, borders, shape, and elevation to communicate structure](#vf-006--use-surfaces-borders-shape-and-elevation-to-communicate-structure)
- [VF-007 — Use clear and consistent iconography and imagery](#vf-007--use-clear-and-consistent-iconography-and-imagery)
- [VF-008 — Maintain visual consistency across states and themes](#vf-008--maintain-visual-consistency-across-states-and-themes)
- [Rule boundaries](#rule-boundaries)
- [Visual Foundation conformance](#visual-foundation-conformance)
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
- **Adaptation test:** inspect narrow screens, 200% text resizing, 400% page zoom/reflow where applicable, alternate themes, high contrast, and localization.
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
- **Reflow test:** inspect 200% text resizing and 400% page zoom/reflow where applicable without page-level horizontal loss.
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

---

## VF-003 — Apply consistent spacing, proximity, and density

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-005, VF-001, VF-002, AX, RS

### Rule

Spacing, proximity, and density MUST communicate grouping and priority consistently while preserving readability, operability, and efficient scanning across user needs and viewport conditions.

### Rationale

Spacing is information. Small distances imply relationship; larger distances imply separation. Arbitrary gaps, excessive whitespace, and uncontrolled compression can all obscure structure. Density must follow task context rather than a universal preference for either minimal or compact interfaces.

### Requirements

- **VF-003-A — Use a documented spacing scale — MUST.** Repeated gaps and insets must use a limited, named scale rather than arbitrary values.
- **VF-003-B — Use proximity to express relationships — MUST.** Related items are closer to one another than to unrelated groups.
- **VF-003-C — Separate groups consistently — MUST.** Section, group, component, and inline spacing must have distinguishable roles.
- **VF-003-D — Distinguish internal and external spacing — MUST.** Component padding must not accidentally appear as separation between components.
- **VF-003-E — Preserve label association — MUST.** Labels, helper text, errors, units, and values remain closer to their associated control or data than to neighboring items.
- **VF-003-F — Match density to task — MUST.** Monitoring, comparison, entry, reading, and touch tasks may require different density; preference alone is not evidence.
- **VF-003-G — Provide density modes deliberately — MAY.** Compact and comfortable modes must preserve hierarchy, target operability, and content meaning.
- **VF-003-H — Avoid whitespace as decoration — SHOULD NOT.** Empty space should support hierarchy, focus, reading measure, or interaction rather than merely make an interface appear premium.
- **VF-003-I — Avoid compression that removes grouping — MUST NOT.** Dense interfaces must retain perceivable sections, labels, focus, errors, and active state.
- **VF-003-J — Keep repeated structures consistent — SHOULD.** Equivalent cards, rows, forms, and sections should use repeatable insets and gaps unless content requires a documented exception.
- **VF-003-K — Adapt spacing without reversing hierarchy — MUST.** Narrow layouts may reduce gaps, but critical separation and touch operability remain intact.
- **VF-003-L — Reserve space for dynamic content — SHOULD.** Errors, helper text, badges, long labels, and status changes should not cause destructive overlap or uncontrolled layout shift.
- **VF-003-M — Keep data density readable — MUST.** Tables and dashboards may be compact, but row identity, column tracking, selected state, and exceptional values remain distinguishable.
- **VF-003-N — Do not use indentation alone for structure — MUST NOT.** Hierarchy also requires labels, headings, lines, grouping, or semantic structure.
- **VF-003-O — Preserve rhythm across localization — MUST.** Longer text and different scripts must not collapse required spacing or detach related content.
- **VF-003-P — Document exceptions — MUST.** Values outside the spacing scale require a content, accessibility, or interaction reason.

### Dashboard policy

Use tighter spacing within one KPI or table row, larger spacing between analytical sections, and the strongest separation between global controls and local data. Dense mode must not hide alert boundaries, selected rows, filter state, or data-quality warnings.

### Validation

Map every gap to its spacing role, perform proximity and grouping tests, compare compact and comfortable modes, stress with errors and long translations, inspect tables at high density, and test zoom and narrow layouts for overlap and lost association.

### Exceptions

Data grids, timelines, canvases, and expert tools MAY use specialized dense spacing when task performance and accessibility are verified. Brand compositions MAY use exceptional whitespace outside task-critical product areas.

### Failure examples

- Every gap uses a different value.
- Helper text is closer to the next field than its own field.
- Compact mode removes visible grouping and focus indicators.
- Large decorative whitespace pushes status and action below the useful viewport.
- Error text overlaps the next component.
- Indentation is the only cue for a hierarchy.

### Acceptance

**Fail** when spacing creates false relationships, disconnects labels or errors, removes operability, or causes overlap. **Conditional Pass** may cover non-blocking scale inconsistencies. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## VF-004 — Build a readable and scalable typography system

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-004, VF-001, VF-002, VF-003, AX, RS, CT

### Rule

Typography MUST provide readable, distinguishable, and scalable roles for content, interface controls, and data without relying on size or weight alone to communicate meaning.

### Rationale

Typography carries hierarchy, tone, labels, instructions, data, and actions. A useful type system is defined by roles and behavior—not a collection of font sizes—and must survive zoom, localization, fallback fonts, dense data, and alternate themes.

### Requirements

- **VF-004-A — Define semantic type roles — MUST.** Page title, section heading, component title, body, label, helper, metadata, action, code, and data roles require documented purpose.
- **VF-004-B — Keep role styling consistent — MUST.** Equivalent roles use consistent family, size, weight, line height, and casing across the product.
- **VF-004-C — Maintain readable body text — MUST.** Body size, line height, contrast, and measure must support sustained reading for the target context.
- **VF-004-D — Use a restrained type scale — SHOULD.** Differences must be large enough to distinguish roles without producing unnecessary levels.
- **VF-004-E — Do not rely on size or weight alone — MUST NOT.** Headings, links, selected states, and warnings require semantic or additional visual cues.
- **VF-004-F — Preserve heading hierarchy — MUST.** Visual heading roles must align with semantic heading structure.
- **VF-004-G — Control line length — SHOULD.** Prose should use a readable measure; full-width long text is avoided even on wide layouts.
- **VF-004-H — Use appropriate alignment — MUST.** Long text, forms, and data columns must use alignment that supports reading and comparison; centered body text is discouraged.
- **VF-004-I — Support text resizing and zoom — MUST.** Content and operation remain available when text expands or the interface is zoomed.
- **VF-004-J — Avoid unnecessary uppercase — SHOULD NOT.** Long labels and sentences should not use all caps; meaning must not depend on casing.
- **VF-004-K — Use italics and decorative styles sparingly — SHOULD.** Emphasis must remain readable across scripts and users with low vision or dyslexia.
- **VF-004-L — Distinguish links and actions — MUST.** Interactive text remains recognizable without color alone and has visible focus.
- **VF-004-M — Format numeric data for comparison — SHOULD.** Use consistent precision, separators, alignment, and tabular numerals where available and useful.
- **VF-004-N — Keep units and qualifiers associated — MUST.** Unit, period, status, and comparison remain visually connected to the value.
- **VF-004-O — Handle truncation safely — MUST.** Do not truncate text that distinguishes objects, states, or actions without a reliable way to obtain the full value.
- **VF-004-P — Support localization and fallback fonts — MUST.** The system must tolerate different scripts, glyph widths, diacritics, bidirectionality, and fallback metrics.
- **VF-004-Q — Use monospace for function, not decoration — SHOULD.** Reserve it for code, identifiers, or alignment cases where fixed width adds meaning.
- **VF-004-R — Keep critical text as text — MUST.** Required labels, warnings, and data must not be embedded only in images.

### Dashboard policy

Numbers may receive emphasis, but metric name, unit, period, comparison, and status remain readable. Use consistent precision and alignment across comparable KPIs. Avoid shrinking labels to fit cards; change layout or wording instead.

### Validation

Audit role inventory, heading semantics, zoom and text spacing, long-form reading, numeric comparison, localization, fallback fonts, truncation, high density, and alternate themes. Test with long labels and large values rather than ideal sample content.

### Exceptions

Display typography MAY use expressive styles in low-risk editorial or campaign areas when required information remains readable. Brand fonts MAY fall back to system or language-specific fonts where glyph coverage, performance, or accessibility requires it.

### Failure examples

- Different styles represent the same heading role.
- Tiny labels are used to force content into cards.
- Center-aligned paragraphs reduce scanning.
- A link is distinguishable only by color.
- KPI values use inconsistent decimal precision.
- Truncation hides the only difference between two records.
- A custom font lacks required language glyphs.

### Acceptance

**Fail** when required text is unreadable, hierarchy conflicts with semantics, zoom loses content or operation, links cannot be identified, or truncation changes meaning. **Conditional Pass** may cover non-blocking role inconsistencies. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## VF-005 — Use color purposefully and accessibly

**Level:** MUST  
**Status:** Draft  
**Related:** FP-004, FP-012, VF-001, VF-004, AX, DV

### Rule

Color MUST have a defined role, meet applicable contrast requirements, and never be the only means of communicating information, state, identity, or available action.

### Rationale

Color can establish hierarchy, brand, status, and data relationships, but perception varies by vision, display, theme, environment, and culture. Uncontrolled palettes and color-only distinctions create inaccessible or misleading interfaces.

### Requirements

- **VF-005-A — Define color roles as tokens — MUST.** Separate brand, neutral, text, surface, border, interaction, focus, semantic status, and data-visualization roles.
- **VF-005-B — Meet text contrast — MUST.** Normal text requires at least 4.5:1 and large text at least 3:1 against its background, subject to applicable WCAG exceptions. For this rule, large text follows the WCAG definition: at least 18 point (approximately 24 CSS pixels), or 14 point (approximately 18.66 CSS pixels) when bold.
- **VF-005-C — Meet non-text contrast — MUST.** Required component boundaries, states, graphical objects, and focus indicators require sufficient contrast, generally at least 3:1 where WCAG applies.
- **VF-005-D — Do not use color alone — MUST NOT.** Status, selection, errors, chart series, and required fields require text, icon, shape, pattern, position, or another cue.
- **VF-005-E — Keep semantic meaning consistent — MUST.** Success, warning, danger, information, selected, and disabled colors must not change meaning across screens.
- **VF-005-F — Use semantic colors only for meaning — SHOULD.** Do not use danger or success colors decoratively where they could create false status.
- **VF-005-G — Preserve readable interaction states — MUST.** Hover, focus, active, selected, visited, and disabled states remain distinguishable without reducing text or control contrast below requirements.
- **VF-005-H — Keep focus visible — MUST.** Focus must remain perceivable against adjacent colors in every theme and surface.
- **VF-005-I — Treat disabled state carefully — MUST.** Disabled controls remain identifiable and their reason is available when users may need it; low opacity must not obscure essential context.
- **VF-005-J — Define dark and alternate themes independently — MUST.** Themes are not generated by simple inversion; surface, elevation, semantic meaning, contrast, and imagery require evaluation.
- **VF-005-K — Test transparency and overlays — MUST.** Contrast must be measured against the actual composited background, not the token in isolation.
- **VF-005-L — Limit simultaneous accent colors — SHOULD.** Accent competes with status and data colors; use it according to hierarchy.
- **VF-005-M — Keep brand subordinate to accessibility — MUST.** Brand colors that fail contrast require an accessible variant or different role.
- **VF-005-N — Design status palettes for color-vision differences — MUST.** Red/green and similar pairs require redundant cues and sufficient lightness or shape difference.
- **VF-005-O — Govern data palettes — MUST.** Sequential, diverging, categorical, and status palettes must match data meaning and remain distinguishable.
- **VF-005-P — Keep category colors stable — SHOULD.** The same category should retain color across related views unless a local legend clearly redefines it.
- **VF-005-Q — Avoid rainbow palettes by default — SHOULD NOT.** Use perceptually ordered palettes for quantitative data and limited categorical colors.
- **VF-005-R — Communicate uncertainty and missing data — MUST.** Missing, estimated, projected, and unavailable values require distinct, labeled treatment.
- **VF-005-S — Support forced and high-contrast modes — SHOULD.** Essential boundaries and states must not disappear when custom colors are replaced.
- **VF-005-T — Validate in context — MUST.** Test real content, states, themes, displays, and overlays rather than palette swatches alone.
- **VF-005-U — Do not encode moral judgment by color without context — MUST NOT.** Increase, decrease, or variance is not inherently good or bad; semantic color follows business meaning.

### Dashboard policy

Reserve semantic colors for status and exceptions. Use neutral structure for most surfaces. Chart colors require legends or direct labels, stable category mapping, and non-color cues. A positive increase and a harmful increase must not share an automatic green treatment.

### Validation

Measure text and non-text contrast, test grayscale and common color-vision simulations, inspect focus and every interaction state, composite transparency, compare light/dark/high-contrast themes, and verify data palettes with missing and uncertain values.

### Exceptions

Logos and purely decorative elements may follow applicable WCAG exceptions. Brand color may appear decoratively when it does not carry required meaning or reduce contrast of adjacent content.

### Failure examples

- Red and green are the only status cues.
- Placeholder text is the only field label and has low contrast.
- A focus ring disappears on a colored card.
- Dark mode is a direct inversion with glowing saturated status colors.
- A rainbow scale implies false data boundaries.
- “Increase” is always green despite harmful metrics.
- Disabled text becomes unreadable and hides the selected value.

### Acceptance

**Fail** when required contrast is not met, essential meaning depends on color, focus disappears, themes change semantics, or data colors misrepresent meaning. **Conditional Pass** may cover non-critical palette simplification. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## VF-006 — Use surfaces, borders, shape, and elevation to communicate structure

**Level:** MUST  
**Status:** Draft  
**Related:** VF-001, VF-002, VF-003, VF-005, IN, AX

### Rule

Surfaces, borders, shape, and elevation MUST communicate grouping, boundaries, hierarchy, and interaction state without creating false affordances or relying on decorative effects.

### Rationale

Containers and layers help users understand what belongs together and what sits above or below another element. Excessive cards, shadows, glass effects, and rounded containers flatten meaning, add noise, and can make static content appear interactive.

### Requirements

- **VF-006-A — Define surface roles — MUST.** Base, raised, overlay, selected, interactive, and critical surfaces require documented purpose.
- **VF-006-B — Use containers only when grouping is needed — SHOULD.** Prefer headings, alignment, and spacing when a card adds no structural meaning.
- **VF-006-C — Keep layer count restrained — SHOULD.** Additional elevation requires a meaningful spatial or interaction relationship.
- **VF-006-D — Make overlays clearly layered — MUST.** Dialogs, menus, popovers, and drawers must be distinguishable from underlying content without making context unreadable.
- **VF-006-E — Keep boundaries perceivable — MUST.** Required field, card, table, and region boundaries must remain visible in every theme and state.
- **VF-006-F — Use borders consistently — MUST.** Border weight, color, and placement must correspond to roles such as separation, focus, error, selection, or input boundary.
- **VF-006-G — Keep elevation consistent — MUST.** Equivalent layers use consistent elevation; higher shadow does not automatically mean greater business importance.
- **VF-006-H — Do not rely on shadow alone — MUST NOT.** Essential boundaries and active states require contrast, border, spacing, or another cue.
- **VF-006-I — Avoid false affordance — MUST.** Static surfaces must not look pressable, and interactive surfaces must provide perceivable interaction cues.
- **VF-006-J — Use shape semantically and consistently — SHOULD.** Radius and shape roles must be limited and repeatable; novelty does not justify inconsistent geometry.
- **VF-006-K — Preserve focus and selection — MUST.** Border, elevation, and surface changes must not obscure focus or make selection indistinguishable.
- **VF-006-L — Avoid transparency that harms readability — MUST.** Glass or translucent effects require stable contrast across all backgrounds and states.
- **VF-006-M — Avoid inset or raised effects that invert expectations — SHOULD NOT.** Neumorphic or ambiguous depth cues must not make controls difficult to identify.
- **VF-006-N — Communicate scroll boundaries — SHOULD.** Users should perceive when a surface contains independently scrollable content.
- **VF-006-O — Preserve structure in alternate themes — MUST.** Dark, high-contrast, and forced-color modes retain layer and boundary meaning.
- **VF-006-P — Keep destructive and critical surfaces proportionate — MUST.** Critical styling reflects actual consequence and must not be used for routine promotion.
- **VF-006-Q — Avoid nested container noise — SHOULD NOT.** Repeated cards inside cards require distinct structural purpose.

### Validation

Remove shadows to test whether grouping survives, inspect every layer and overlay, compare static and interactive surfaces, test light/dark/high-contrast themes, place translucent surfaces over varied content, and verify scroll, focus, selection, error, and disabled boundaries.

### Exceptions

Maps, canvases, media, and immersive tools MAY use specialized overlays or translucency when required controls remain readable and operable. Editorial compositions MAY use decorative surfaces outside critical workflows.

### Failure examples

- Every section is a card inside another card.
- Shadow is the only input boundary.
- A static card appears clickable.
- A clickable row has no interactive cue.
- Glassmorphism makes text contrast depend on the image behind it.
- Dark mode removes boundaries between surfaces.
- Error and selected borders use indistinguishable styles.

### Acceptance

**Fail** when structure or interaction depends on shadow alone, layers become indistinguishable, false affordance is created, or transparency breaks readability. **Conditional Pass** may cover non-blocking decorative inconsistency. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## VF-007 — Use clear and consistent iconography and imagery

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-004, IA-003, VF-001, VF-005, AX, CT, EP

### Rule

Icons and imagery MUST clarify meaning, action, identity, or context without replacing required text, introducing ambiguity, or creating inaccessible and culturally misleading communication.

### Rationale

Icons can accelerate recognition for familiar concepts, while imagery can establish context and identity. Both become harmful when style is inconsistent, meaning is assumed, decoration competes with tasks, or visual content carries information without an accessible alternative.

### Requirements

- **VF-007-A — Use icons for recognized concepts — MUST.** Unfamiliar, domain-specific, or ambiguous icons require visible labels.
- **VF-007-B — Provide accessible names — MUST.** Interactive icons require names matching their visible meaning; decorative icons must not create redundant assistive output.
- **VF-007-C — Keep icon meaning stable — MUST.** One icon must not represent conflicting actions or states within the same product.
- **VF-007-D — Use labels for consequential actions — MUST.** Delete, publish, payment, permission, and other high-risk actions must not rely on icon-only presentation.
- **VF-007-E — Maintain a coherent icon system — SHOULD.** Stroke, fill, perspective, corner style, optical size, and visual weight should be consistent.
- **VF-007-F — Align icons optically — SHOULD.** Icons align with text and controls by perceived rather than bounding-box geometry where necessary.
- **VF-007-G — Separate icon size from target size — MUST.** A small icon may have a larger interactive target; visual size must not determine operability.
- **VF-007-H — Distinguish state beyond icon replacement — MUST.** Selected, active, error, and disabled states require additional perceivable cues.
- **VF-007-I — Use directional icons correctly — MUST.** Direction-sensitive icons adapt to reading direction when meaning reverses; universal media or physical-direction symbols must not be mirrored blindly.
- **VF-007-J — Avoid emoji as the sole critical icon — SHOULD NOT.** Rendering and interpretation vary by platform, culture, and font.
- **VF-007-K — Keep badges and indicators associated — MUST.** Notification dots, counts, and status badges must clearly identify the object they describe and provide textual meaning.
- **VF-007-L — Use imagery with task relevance — SHOULD.** Images should support comprehension, identity, evidence, or appropriate emotional context rather than displace required content.
- **VF-007-M — Provide text alternatives according to purpose — MUST.** Informative images require equivalent text; decorative images must be ignored by assistive technology where possible.
- **VF-007-N — Do not embed required text only in images — MUST NOT.** Warnings, labels, metrics, and instructions must remain real text.
- **VF-007-O — Prevent decorative competition — MUST.** Hero art, illustration, and animation must not dominate critical status or primary action.
- **VF-007-P — Treat generated imagery transparently when material — MUST.** AI-generated or materially altered evidence, people, products, or events require disclosure and must not mislead.
- **VF-007-Q — Validate cultural meaning — SHOULD.** Gestures, symbols, animals, flags, maps, and colors require review for target locales.

### Validation

Run icon-without-context comprehension tests, compare icon and accessible names, inspect target size and focus, test selected/error/disabled states, review RTL mirroring, disable imagery to verify task continuity, inspect alternate text, and evaluate generated or culturally sensitive imagery.

### Exceptions

Icon-only controls MAY be used for low-risk, widely understood actions in constrained toolbars when accessible names, tooltips, and adequate targets exist. Decorative imagery MAY be omitted from text alternatives.

### Failure examples

- A trash icon alone performs permanent deletion.
- The same star means favorite, featured, and rating.
- A notification dot has no textual count or status.
- Icon size is adequate visually but target size is too small.
- Required instructions exist only inside an image.
- A hero illustration pushes a blocking error below the viewport.
- AI-generated operational evidence appears authentic without disclosure.

### Acceptance

**Fail** when critical actions use ambiguous icons, required information exists only in imagery, accessible names conflict with meaning, or imagery misleads. **Conditional Pass** may cover non-blocking style inconsistency. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## VF-008 — Maintain visual consistency across states and themes

**Level:** MUST  
**Status:** Draft  
**Related:** FP-008, FP-011, VF-001, VF-004, VF-005, VF-006, VF-007, IN, AX

### Rule

Visual roles, components, interaction states, and themes MUST remain consistent enough for users to recognize meaning and predict behavior while allowing documented variation required by context.

### Rationale

Consistency reduces relearning and supports recognition, but uniformity can hide meaningful differences. A governed visual system must define stable roles and complete state behavior across themes, surfaces, permissions, and data conditions.

### Requirements

- **VF-008-A — Use semantic design tokens — MUST.** Typography, spacing, color, border, radius, elevation, and motion references should use role-based names rather than context-free raw values.
- **VF-008-B — Define component roles — MUST.** Equivalent buttons, fields, links, cards, tables, alerts, and navigation items must have consistent appearance and behavior.
- **VF-008-C — Define a complete state matrix — MUST.** Relevant default, hover, focus, active, selected, disabled, loading, empty, success, warning, error, and permission states require intentional treatment.
- **VF-008-D — Keep state meanings stable — MUST.** Error, selected, disabled, and critical treatments must not change meaning across components or themes.
- **VF-008-E — Distinguish state and hierarchy — MUST.** A selected secondary item must not become visually indistinguishable from a primary action.
- **VF-008-F — Keep focus visible in every state — MUST.** Hover, selected, error, and disabled styling must not erase focus.
- **VF-008-G — Avoid layout shift between states — SHOULD.** Loading, validation, selection, and font-weight changes should not move controls unpredictably.
- **VF-008-H — Preserve content during loading — SHOULD.** Use stable regions or meaningful skeletons without presenting placeholder shapes as real data.
- **VF-008-I — Keep theme semantics equivalent — MUST.** Light, dark, high-contrast, and branded themes preserve hierarchy, status, interaction, and data meaning.
- **VF-008-J — Respect user theme preference — SHOULD.** System or explicit preference should persist without unexpected switching or flashes that reduce usability.
- **VF-008-K — Validate imagery and charts per theme — MUST.** Assets, logos, illustrations, screenshots, and data palettes require theme-compatible variants or boundaries.
- **VF-008-L — Govern intentional exceptions — MUST.** A variation requires a user, accessibility, platform, or domain reason and must not redefine a shared role silently.
- **VF-008-M — Prevent local style drift — MUST.** Product areas must not introduce new colors, shadows, typography, or component variants without system review.
- **VF-008-N — Preserve cross-platform meaning — SHOULD.** Platform conventions may change presentation while labels, consequences, state, and brand identity remain coherent.
- **VF-008-O — Version system changes — MUST.** Breaking changes to tokens or roles require migration guidance and affected-component review.
- **VF-008-P — Test rare states — MUST.** Empty, partial data, stale data, permission denied, offline, expired, and destructive confirmation states require review, not only the ideal path.
- **VF-008-Q — Keep user customization safe — MUST.** Density, theme, column, and display preferences must not remove critical state, labels, focus, or warnings.
- **VF-008-R — Prefer consistency over novelty — SHOULD.** New patterns require evidence that existing patterns cannot satisfy the task.

### State matrix minimum

For each interactive component, document applicable states, visible change, semantic meaning, keyboard behavior, assistive announcement, and theme behavior. “Not applicable” must be intentional rather than omitted.

### Validation

Inventory tokens and component variants, compare equivalent roles across screens, exercise the complete state matrix, inspect theme pairs, test focus over every state, measure layout shift, review rare states, and simulate migration after a token or role change.

### Exceptions

Native platform conventions MAY differ when they improve expected behavior and accessibility. Campaign or branded surfaces MAY vary visually while shared controls and critical semantics remain consistent.

### Failure examples

- “Primary” buttons use unrelated styles across pages.
- Selected and error states use the same border.
- Focus disappears when a row is selected.
- Dark theme changes warning yellow into a decorative accent.
- Loading swaps layouts and moves actions.
- A team creates ungoverned local token values.
- Rare permission and stale-data states have no visual treatment.

### Acceptance

**Fail** when equivalent roles conflict, critical states are missing, focus disappears, theme changes meaning, or customization removes essential information. **Conditional Pass** may cover documented non-blocking drift with migration ownership. **Pass** requires all relevant mandatory requirements or approved exceptions.

---

## Rule boundaries

Visual Foundation intentionally touches accessibility, responsive behavior, interaction, content, and data visualization. Use this ownership model to prevent conflicting standards and duplicate findings:

- **VF-001 owns visual prominence:** what attracts attention and how priority is perceived. IA owns information order; AX owns whether critical information is perceivable to users with disabilities.
- **VF-002 owns spatial composition:** page regions, visual alignment, and visual/semantic order. RS owns breakpoint and adaptive behavior; AX owns reflow conformance and assistive reading order.
- **VF-003 owns visible spacing and density:** grouping, rhythm, and compactness. AX owns minimum operability and target-size conformance.
- **VF-004 owns typographic presentation:** role, readability, scale, measure, and numeric formatting. CT owns wording; AX owns accessibility success criteria.
- **VF-005 owns visual color roles and palettes:** contrast implementation, semantic color, and theme color behavior. AX is authoritative for accessibility conformance; DV owns data encoding and chart-palette selection by analytical purpose.
- **VF-006 owns visible layers and boundaries:** surfaces, borders, shape, and elevation. IN owns overlay behavior, dismissal, and state transitions.
- **VF-007 owns icon and image presentation:** visual meaning, style, and association. CT owns labels; AX owns alternatives and accessible naming; EP owns ethical use and disclosure.
- **VF-008 owns cross-screen visual consistency:** tokens, visual states, and theme equivalence. IN owns component behavior and feedback timing; AX owns focus and assistive behavior conformance.

When one problem crosses standards, record one primary finding under the owning rule and list other rules as related. Accessibility requirements take precedence where visual guidance conflicts with conformance criteria.

## Visual Foundation conformance

A design conforms to this document only when every relevant MUST and MUST NOT requirement from VF-001 through VF-008 is satisfied or has an approved exception. SHOULD findings may produce Conditional Pass when they do not block safe task completion and have an owner, rationale, and review date.

### Required evidence

- page-purpose and hierarchy inventory;
- layout and reading-order map;
- spacing scale and density rationale;
- typography roles and localization behavior;
- color-role and contrast results;
- surface, border, shape, and elevation roles;
- icon and imagery inventory with accessible purpose;
- component state matrix and theme comparison;
- completed Visual Foundation review checklist;
- documented exceptions.

## Evidence basis

- [GOV.UK Government Design Principles](https://www.gov.uk/guidance/government-design-principles) — start with user needs and be consistent rather than mechanically uniform.
- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — visibility, consistency, recognition, and minimalist design.
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) — perceivable, operable, understandable, and robust presentation.
- [Material Design: Accessibility](https://m2.material.io/design/usability/accessibility.html) — accessible visual and interaction foundations.
- [W3C WCAG 2.2: Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html) — color must not be the only visual means of conveying information.
- [W3C WCAG 2.2: Contrast Minimum](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) — text contrast requirements.
- [W3C WCAG 2.2: Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) — contrast for controls and meaningful graphics.
- [W3C WCAG 2.2: Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html) — preserve content and operation under narrow presentation and zoom.
- [Material Design 3: Interaction States](https://m3.material.io/foundations/interaction/states) — consistent component-state communication.


## Audit status

Internal structural audit passed on 2026-10-01. Controlled workflow validation also passed across hierarchy/layout/density, typography/color, and surfaces/icons/states/themes scenarios. The standard contains eight main rules and 147 unique sub-rules.

Candidate status means the workflow is ready for rendered-interface and representative-user testing. See `audits/2026-10-01-visual-foundation.md` and `validation/2026-10-01-visual-foundation-workflow.md`.
