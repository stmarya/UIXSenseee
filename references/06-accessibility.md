# Accessibility

- **Document ID:** UIXS-AX
- **Version:** 0.11.0
- **Status:** Candidate
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Conformance baseline:** WCAG 2.2 Level AA where applicable
- **Related standards:** FP, IA, VF, IN, CB, RS, DV, CT, EP, QA

## Purpose

Establish accessibility as a default product requirement and provide an authoritative conformance layer for perceivable, operable, understandable, and robust interfaces.

## Scope

Applies to content, structure, controls, forms, navigation, focus, color, reflow, zoom, input modalities, motion, media, timing, dynamic updates, dashboards, and complex data.

## Ownership

AX is authoritative for accessibility conformance. Other standards own their domain implementation but must defer to AX when accessibility requirements conflict with visual, interaction, responsive, or business preferences.

## Principles

- Include disabled people and assistive technology from the start.
- Prefer native semantics and resilient platform behavior.
- Test complete tasks, not isolated components only.
- Combine automated checks with manual and representative-user evidence.
- Accessibility exceptions require criterion-level evidence, risk, mitigation, owner, and deadline.

---

## AX-001 — Establish WCAG 2.2 AA as the accessibility baseline

**Level:** MUST  
**Status:** Draft

### Rule

Products MUST meet applicable WCAG 2.2 Level A and AA success criteria and document scope, exceptions, evidence, and unresolved risk.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-001-A — Define conformance scope — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-B — Evaluate complete processes — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-C — Include third-party and embedded content — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-D — Do not claim partial conformance as full — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-E — Document criterion-level evidence — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-F — Treat automated tools as incomplete — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-G — Prioritize blockers and rights risks — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-001-H — Retest after material change — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-002 — Provide semantic structure, names, roles, and relationships

**Level:** MUST  
**Status:** Draft

### Rule

Content and controls MUST expose semantic structure, accessible names, roles, values, relationships, and reading order equivalent to visible meaning.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-002-A — Use native semantics where suitable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-B — Provide descriptive page titles and headings — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-C — Name landmarks and repeated navigation — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-D — Associate labels and descriptions — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-E — Expose state and value — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-F — Keep reading and visual order aligned — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-G — Use tables with valid headers — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-002-H — Avoid redundant or conflicting semantics — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-003 — Support keyboard access and visible focus

**Level:** MUST  
**Status:** Draft

### Rule

Every essential function MUST be operable by keyboard with logical focus order, visible focus, no trap, and predictable focus management.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-003-A — Reach all essential controls — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-B — Use logical focus order — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-C — Provide visible focus — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-D — Avoid keyboard traps — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-E — Manage overlay focus — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-F — Restore focus meaningfully — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-G — Avoid shortcut conflicts — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-003-H — Test custom widgets against expected keys — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-004 — Provide sufficient contrast and non-color meaning

**Level:** MUST  
**Status:** Draft

### Rule

Text, controls, focus, meaningful graphics, and status MUST meet applicable contrast criteria and MUST NOT rely on color alone.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-004-A — Meet 4.5 to 1 normal-text contrast — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-B — Meet 3 to 1 large-text contrast — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-C — Meet applicable non-text contrast — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-D — Provide redundant status cues — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-E — Keep focus contrast visible — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-F — Test actual composited backgrounds — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-G — Preserve meaning in themes — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-004-H — Support forced-colors where applicable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-005 — Make forms, errors, and instructions accessible

**Level:** MUST  
**Status:** Draft

### Rule

Forms MUST provide persistent labels, instructions, required state, error identification, correction guidance, and review for high-impact submissions.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-005-A — Provide programmatic and visible labels — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-B — Identify required fields — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-C — Explain formats and constraints — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-D — Associate errors with fields — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-E — Describe errors in text — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-F — Preserve valid input — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-G — Provide error summary for complex forms — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-005-H — Support review and correction for consequential submission — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-006 — Support pointer, touch, target, and gesture access

**Level:** MUST  
**Status:** Draft

### Rule

Pointer and touch interaction MUST provide adequate target size or spacing, avoid precision-only paths, and offer alternatives to complex gestures.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-006-A — Meet applicable target-size criteria — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-B — Avoid adjacent accidental targets — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-C — Provide single-pointer alternatives — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-D — Provide gesture alternatives — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-E — Avoid motion-only activation — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-F — Allow pointer cancellation — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-G — Keep visible label in accessible name — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-006-H — Support orientation-independent operation where applicable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-007 — Support reflow, zoom, text resize, and text spacing

**Level:** MUST  
**Status:** Draft

### Rule

Content and operation MUST remain available under applicable reflow, zoom, text resizing, and user text-spacing overrides without two-dimensional page scrolling except allowed content.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-007-A — Support 200 percent text resize — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-B — Support reflow at 320 CSS pixels where applicable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-C — Avoid loss at 400 percent page zoom where applicable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-D — Tolerate user text spacing — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-E — Prevent clipping and overlap — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-F — Keep controls and errors available — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-G — Bound necessary data overflow — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-007-H — Preserve semantic order after reflow — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-008 — Control motion, media, flashing, timing, and interruption

**Level:** MUST  
**Status:** Draft

### Rule

Motion, media, flashing, time limits, and interruptions MUST follow applicable accessibility criteria and user preferences.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-008-A — Respect reduced motion — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-B — Avoid seizure-risk flashing — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-C — Provide pause stop or hide controls — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-D — Provide captions for required media — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-E — Provide audio description or alternatives where applicable — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-F — Allow time adjustment where required — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-G — Avoid unexpected audio — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-008-H — Control auto-updating interruption — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-009 — Expose dynamic status, overlays, and changes accessibly

**Level:** MUST  
**Status:** Draft

### Rule

Dynamic updates, dialogs, menus, notifications, loading, validation, and route changes MUST communicate state without stealing focus or leaving assistive users disoriented.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-009-A — Use appropriate status announcements — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-B — Avoid unnecessary focus movement — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-C — Name dialogs and overlays — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-D — Contain and restore modal focus — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-E — Announce route and context changes — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-F — Expose busy and progress state — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-G — Keep critical messages persistent — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-009-H — Test virtual and incremental content — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

---

## AX-010 — Make charts and complex data perceivable and operable

**Level:** MUST  
**Status:** Draft

### Rule

Charts, dashboards, maps, tables, and complex visual data MUST provide equivalent names, summaries, values, relationships, and operable alternatives.

### Rationale

Accessibility barriers prevent equal perception, operation, understanding, or robust use and can invalidate otherwise successful task completion.

### Requirements

- **AX-010-A — Provide chart title and purpose — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-B — Provide text summary of key meaning — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-C — Provide accessible data or table alternative — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-D — Do not rely on color alone — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-E — Support keyboard access to interactive data — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-F — Expose units periods and uncertainty — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-G — Keep tooltip information available by focus — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.
- **AX-010-H — Provide non-visual path for map or spatial tasks — MUST.** Apply the relevant WCAG criterion, platform semantic, and manual verification for the complete user task.

### Validation

Use applicable automated checks plus manual keyboard, focus, zoom/reflow, contrast, screen-reader, touch, and content review. Test realistic states, permissions, errors, localization, and complete processes.

### Exceptions

Only exceptions allowed by the applicable accessibility criterion or an approved time-bounded risk decision may be used. Product convenience is not an exception.

### Failure examples

Missing semantics, inaccessible keyboard flow, color-only meaning, insufficient contrast, clipped zoomed content, unavailable alternatives, or dynamic changes that assistive users cannot perceive.

### Acceptance

Fail when an applicable Level A or AA requirement is unmet, an essential task is blocked, or equivalent information and operation are unavailable. Pass requires criterion-level evidence or approved governed exception.

## Accessibility conformance

Conformance requires all applicable WCAG 2.2 Level A and AA criteria across complete processes, plus UIXSenseee requirements in AX-001 through AX-010. Automated scans alone cannot establish conformance.

### Required evidence

- conformance scope and page/process inventory;
- automated scan results and manual review;
- keyboard and focus evidence;
- screen-reader and semantic evidence;
- contrast, color, zoom, reflow, and text-spacing results;
- form and error review;
- motion, media, timing, and dynamic-status review;
- complex-data alternatives;
- exceptions, owners, and retest dates.

## Evidence basis

- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [W3C Understanding WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/)
- [WAI ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/)
- [WAI Forms Tutorials](https://www.w3.org/WAI/tutorials/forms/)


## Validation status

Internal audit and controlled workflow validation passed on 2026-10-01. Accessibility is Candidate with 10 main rules and 80 unique sub-rules. Candidate status does not constitute product WCAG conformance; rendered complete-process testing remains required.
