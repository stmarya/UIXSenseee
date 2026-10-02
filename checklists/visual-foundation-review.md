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

## Decision

- [ ] Every failed item includes evidence, severity, primary rule ID, correction, owner, and verification method.
- [ ] Critical and unresolved Major findings prevent Pass.
