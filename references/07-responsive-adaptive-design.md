# Responsive & Adaptive Design

- **Document ID:** UIXS-RS
- **Version:** 0.10.0
- **Status:** Draft
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Related standards:** FP, IA, VF, IN, CB, AX, DV, CT, QA

## Purpose

Ensure interfaces preserve meaning, priority, operation, accessibility, and state across viewport, container, orientation, input, zoom, localization, performance, and connectivity conditions.

## Ownership

RS owns adaptive layout and behavior. AX is authoritative for accessibility conformance; VF owns visual composition; IA owns information structure; IN and CB own interaction and component semantics.

---

## RS-001 — Preserve task and content priority

**Level:** MUST  
**Status:** Draft

### Rule

Adaptive layouts MUST preserve primary tasks, critical status, scope, and required actions rather than merely shrinking desktop composition.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-001-A — Keep critical content visible — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-B — Preserve primary action and scope — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-C — Do not promote secondary content above risk — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-D — Document intentional reprioritization — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-E — Keep hidden content discoverable — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-F — Test task completion at each layout — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-G — Avoid desktop-first omission — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-001-H — Preserve semantic order — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-002 — Reflow content without loss

**Level:** MUST  
**Status:** Draft

### Rule

Content MUST reflow without loss of information or operation and avoid page-level two-dimensional scrolling except allowed complex content.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-002-A — Support single-direction page flow — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-B — Bound necessary component overflow — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-C — Prevent clipping and overlap — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-D — Keep focus and anchors visible — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-E — Avoid fixed dimensions that block growth — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-F — Preserve reading order — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-G — Keep errors and controls available — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-002-H — Test complete flows under reflow — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-003 — Use content-driven breakpoints and containers

**Level:** MUST  
**Status:** Draft

### Rule

Breakpoints and container changes MUST respond to content failure and task needs rather than device labels alone.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-003-A — Define breakpoint trigger evidence — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-B — Use container context where appropriate — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-C — Avoid device-name assumptions — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-D — Prevent breakpoint oscillation — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-E — Test intermediate widths — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-F — Allow component-level adaptation — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-G — Document layout state changes — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-003-H — Avoid arbitrary pixel proliferation — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-004 — Adapt navigation and wayfinding safely

**Level:** MUST  
**Status:** Draft

### Rule

Navigation MAY change form across widths but MUST preserve current location, parent context, destinations, and predictable return.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-004-A — Preserve current location — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-B — Keep navigation labels and meaning — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-C — Expose collapsed navigation clearly — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-D — Provide route back — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-E — Avoid hidden essential destinations — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-F — Maintain keyboard and focus behavior — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-G — Preserve permission-aware structure — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-004-H — Test direct entry and deep links — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-005 — Adapt forms and controls to available space

**Level:** MUST  
**Status:** Draft

### Rule

Forms and controls MUST retain labels, order, errors, targets, and completion flow across layout and input changes.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-005-A — Keep labels persistent — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-B — Preserve logical field order — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-C — Stack columns when order becomes ambiguous — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-D — Keep validation associated — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-E — Use suitable input and keyboards — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-F — Maintain target separation — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-G — Protect unsaved values — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-005-H — Keep actions reachable above overlays — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-006 — Make tables and collections usable on narrow views

**Level:** MUST  
**Status:** Draft

### Rule

Tables and collections MUST preserve row identity, critical columns, comparison, actions, and access to omitted detail.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-006-A — Prioritize critical columns — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-B — Provide full-detail access — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-C — Keep headers associated — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-D — Support bounded horizontal scrolling when needed — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-E — Preserve selection and row action scope — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-F — Avoid card conversion that hides comparison — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-G — Keep sort filter and pagination usable — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-006-H — Provide accessible alternative — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-007 — Adapt charts and dashboards without distorting meaning

**Level:** MUST  
**Status:** Draft

### Rule

Charts and dashboards MUST preserve metric definition, scale, labels, uncertainty, filters, and data access when adapting.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-007-A — Preserve axes units and baseline — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-B — Avoid unreadable compression — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-C — Reduce simultaneous detail deliberately — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-D — Keep global and local filters distinct — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-E — Provide table or data alternative — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-F — Preserve uncertainty and missing data — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-G — Avoid changing chart type without meaning review — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-007-H — Test extreme labels and values — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-008 — Support modality, orientation, and safe areas

**Level:** MUST  
**Status:** Draft

### Rule

Essential tasks MUST work across applicable pointer, touch, keyboard, orientation, viewport, and safe-area conditions.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-008-A — Do not lock orientation without need — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-B — Respect display cutouts and safe areas — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-C — Support pointer and touch without hover dependency — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-D — Preserve keyboard operation — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-E — Adapt targets for input context — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-F — Avoid gesture-only operation — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-G — Handle virtual keyboard occlusion — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-008-H — Test split screen and window resize — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-009 — Support zoom, text expansion, and localization

**Level:** MUST  
**Status:** Draft

### Rule

Layouts MUST tolerate zoom, text resize, user spacing, long translation, bidirectionality, and fallback fonts without lost meaning or operation.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-009-A — Meet applicable text resize and reflow — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-B — Tolerate user text spacing — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-C — Avoid truncating distinguishing content — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-D — Support long translations — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-E — Support right-to-left structure — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-F — Preserve numeric and unit association — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-G — Use resilient font fallback — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-009-H — Test mixed-script content — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

---

## RS-010 — Preserve state and performance across adaptive changes

**Level:** MUST  
**Status:** Draft

### Rule

Adaptive changes MUST preserve relevant state and avoid excessive performance or connectivity costs that block core tasks.

### Rationale

Responsive design must preserve task success and meaning rather than produce a visually smaller copy of one preferred viewport.

### Requirements

- **RS-010-A — Preserve filters selection drafts and focus — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-B — Avoid state reset at breakpoints — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-C — Use progressive loading responsibly — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-D — Keep core tasks usable on slow connections — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-E — Avoid downloading hidden heavy content unnecessarily — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-F — Communicate adaptation and refresh — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-G — Prevent layout shift during hydration — MUST.** Verify the complete task across realistic adaptive conditions.
- **RS-010-H — Test resume after interruption — MUST.** Verify the complete task across realistic adaptive conditions.

### Validation

Test narrow, intermediate, and wide containers; 200% text resizing; 400% page zoom/reflow where applicable; touch, pointer, and keyboard; long translations; orientation; errors; loading; permissions; and variable data.

### Exceptions

Specialized maps, canvases, timelines, and data grids MAY use bounded two-dimensional interaction when orientation, alternatives, and accessibility are provided.

### Failure examples

Lost priority, clipped content, hidden actions, reset state, unreadable charts, ambiguous order, inaccessible overflow, and interaction that works only at one viewport or modality.

### Acceptance

Fail when adaptation removes information or operation, changes analytical meaning, reverses critical priority, or blocks an essential task. Pass requires all relevant mandatory rules or approved exceptions.

## Responsive conformance

Conformance requires RS-001 through RS-010 plus applicable Accessibility requirements. Responsive screenshots alone are insufficient; complete task and state transitions must be tested.

### Required evidence

- priority and layout maps;
- breakpoint and container rationale;
- reflow, zoom, and text-spacing results;
- navigation, forms, tables, and chart adaptation;
- modality, orientation, safe-area, and virtual-keyboard tests;
- localization and bidirectional tests;
- state, performance, and interruption tests;
- checklist and exceptions.

## Evidence basis

- [W3C WCAG 2.2: Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html)
- [W3C WCAG 2.2: Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html)
- [W3C WCAG 2.2: Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html)
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
