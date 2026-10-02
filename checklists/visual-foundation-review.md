# Visual Foundation Review Checklist

- **Checklist ID:** UIXS-VF-CHECK
- **Version:** 0.1.0
- **Status:** Draft
- **Related standard:** `references/02-visual-foundation.md`

## Applicability preflight

- [ ] Target users, tasks, risk, and content density are stated.
- [ ] The reviewed screens, states, themes, and viewport conditions are listed.
- [ ] Relevant VF rules are selected and exclusions are explained.

## VF-001 — Visual hierarchy

- [ ] Page purpose and primary task or decision are identifiable.
- [ ] Primary, secondary, tertiary, and critical roles are defined.
- [ ] A clear first focus exists without suppressing critical status.
- [ ] Hierarchy does not depend on one visual cue.
- [ ] Visual, semantic, reading, and keyboard order align.
- [ ] Related information is grouped and unrelated content is separated.
- [ ] Primary, secondary, and destructive actions are distinguishable.
- [ ] Metric name, value, unit, period, comparison, and status are differentiated.
- [ ] Loading, empty, error, success, disabled, and permission states retain hierarchy.
- [ ] Narrow layouts, zoom, localization, alternate themes, and high contrast preserve priority.
- [ ] Decoration remains subordinate to required information and action.

## VF-002 — Layout, grid, and alignment

- [ ] Page regions and columns support task hierarchy rather than arbitrary symmetry.
- [ ] Related content shares meaningful alignment anchors.
- [ ] Labels, values, controls, and actions remain spatially associated.
- [ ] Visual, semantic, reading, and keyboard order align.
- [ ] Text, forms, tables, charts, and controls have purpose-appropriate widths.
- [ ] Narrow layouts and zoom reflow without changing meaning.
- [ ] Page-level horizontal scrolling is avoided; bounded component overflow is clear.
- [ ] Sticky and fixed regions do not cover content, focus, errors, or anchors.
- [ ] Comparable values and records align for accurate scanning.
- [ ] Card placement reflects relationships rather than filling the grid.
- [ ] Variable and translated content does not overlap or lose meaning.
- [ ] Overlays remain anchored, dismissible, and within usable viewport bounds.

## VF-003 — Spacing, proximity, and density

- [ ] A documented spacing scale is used for repeated gaps and insets.
- [ ] Related items are closer than unrelated groups.
- [ ] Labels, helpers, errors, units, and values remain associated.
- [ ] Density matches the task and compact modes preserve focus and grouping.
- [ ] Dynamic and localized content does not overlap or detach.

## VF-004 — Typography

- [ ] Semantic type roles and heading hierarchy are defined.
- [ ] Body text, line height, measure, and alignment support reading.
- [ ] Zoom, text expansion, localization, and fallback fonts preserve content and operation.
- [ ] Links and actions remain recognizable without color alone.
- [ ] Numeric precision, alignment, units, and truncation preserve meaning.

## VF-005 — Color

- [ ] Color roles are semantic and documented.
- [ ] Text and non-text contrast meet applicable requirements.
- [ ] Status, selection, errors, and chart series do not rely on color alone.
- [ ] Focus remains visible on every surface and state.
- [ ] Light, dark, high-contrast, transparency, and data palettes preserve meaning.
- [ ] Missing, uncertain, estimated, and projected data are distinguishable.

## VF-006 — Surfaces, borders, shape, and elevation

- [ ] Containers and layers communicate meaningful grouping.
- [ ] Borders and boundaries remain perceivable in every theme.
- [ ] Shadow is not the only boundary or state cue.
- [ ] Static and interactive surfaces do not create false affordance.
- [ ] Overlays, transparency, scrolling, focus, error, and selection remain clear.

## VF-007 — Iconography and imagery

- [ ] Ambiguous and consequential icons have visible labels.
- [ ] Interactive icons have accurate accessible names and adequate targets.
- [ ] Icon meaning, style, state, and directional behavior are consistent.
- [ ] Informative imagery has an equivalent alternative; required text is not image-only.
- [ ] Decorative and generated imagery does not compete with or mislead critical tasks.

## VF-008 — Consistency, states, and themes

- [ ] Semantic tokens and component roles are governed.
- [ ] Applicable default, hover, focus, active, selected, disabled, loading, empty, success, warning, error, and permission states are defined.
- [ ] State meaning and focus remain stable across components and themes.
- [ ] Loading and validation do not create destructive layout shift.
- [ ] Rare states, user customization, and theme assets preserve critical meaning.
- [ ] Breaking token or role changes include migration guidance.

## Conformance evidence

- [ ] Hierarchy, layout, spacing, typography, color, surface, icon, state, and theme evidence is attached.
- [ ] Relevant MUST and MUST NOT rules pass or have approved exceptions.

## Decision

- [ ] Every failed item includes evidence, severity, primary rule ID, correction, owner, and verification method.
- [ ] Critical and unresolved Major findings prevent Pass.
