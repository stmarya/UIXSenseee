# Foundation Principles

- **Document ID:** UIXS-FP
- **Version:** 0.1.0
- **Status:** Draft

## Purpose

Define the non-negotiable values used to resolve UI/UX decisions across every standard area.

## Principles

### FP-001 — Start with user needs — MUST
Every design decision MUST connect to an identified user need, goal, task, or risk. Features MUST NOT be added only because they are fashionable or technically available.

### FP-002 — Prefer clarity over cleverness — MUST
Users MUST be able to understand meaning, state, and the next action without guessing. Visual novelty MUST NOT reduce comprehension.

### FP-003 — Prioritize effectiveness — MUST
Task completion, safety, accessibility, and correct outcomes take precedence over efficiency, engagement, and aesthetics.

### FP-004 — Make accessibility the default — MUST
Accessibility MUST be considered from the start. Color, pointer input, sound, or motion MUST NOT be the only way to perceive or operate essential information.

### FP-005 — Build hierarchy from purpose — MUST
Visual and information emphasis MUST follow user priority rather than decoration or internal stakeholder preference.

### FP-006 — Reveal complexity progressively — SHOULD
Show information needed for the current task first. Critical consequences, costs, risks, and controls MUST NOT be hidden.

### FP-007 — Prefer recognition over recall — SHOULD
Make options, context, and instructions visible where needed. Users SHOULD NOT need to remember information from another screen to complete a task.

### FP-008 — Be consistent, not blindly uniform — MUST
Equivalent functions MUST behave consistently. Different contexts MAY use different patterns when evidence supports the difference.

### FP-009 — Preserve user control — MUST
Users MUST understand and control meaningful actions. Risky actions require proportional protection; recoverable actions SHOULD support Undo.

### FP-010 — Prevent errors — MUST
Design MUST reduce predictable errors before they occur and preserve user input when validation fails.

### FP-011 — Communicate system status — MUST
The interface MUST communicate loading, success, failure, empty, and changed states at the relevant time and location.

### FP-012 — Represent data honestly — MUST
Metrics, scales, comparisons, uncertainty, missing data, and time context MUST NOT be presented in a misleading way.

### FP-013 — Protect user interests — MUST
Dark patterns, false urgency, hidden consequences, manipulative defaults, and obstructed refusal or cancellation MUST NOT be used.

### FP-014 — Base decisions on evidence — MUST
Important assumptions MUST be identified. High-risk and critical flows SHOULD be validated with representative evidence and iterated after evaluation.

## Conflict resolution

Safety → rights/privacy/control → accessibility → task completion → honest information → clarity → consistency → efficiency → aesthetics.
