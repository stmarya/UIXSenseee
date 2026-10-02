# Interaction Standards Review Checklist

- **Checklist ID:** UIXS-IN-CHECK
- **Version:** 0.1.0
- **Status:** Draft
- **Related standard:** `references/03-interaction-standards.md`

## Applicability preflight

- [ ] Users, tasks, risk, permissions, affected objects, and input modalities are stated.
- [ ] Relevant IN rules are selected and exclusions are explained.
- [ ] One primary rule owns each finding; related IA, VF, CB, AX, RS, CT, EP, or QA rules are linked without duplication.
- [ ] Reviewed states include before, during, after, failure, unavailable, and recovery where applicable.

## IN-001 — Discoverability and predictability

- [ ] Interactive elements are distinguishable from static content.
- [ ] Labels communicate action, target, scope, and meaningful consequence.
- [ ] Navigation and modifying commands are distinguishable.
- [ ] Available, unavailable, restricted, and pending actions are understandable.
- [ ] Essential interactions do not depend on hover or one input modality.
- [ ] Complex gestures and direct manipulation have discoverable alternatives.
- [ ] Active mode, selection, and affected objects remain visible.
- [ ] Workspace, period, permission, and analytical scope do not change silently.
- [ ] Command palettes distinguish result and action types.
- [ ] Visible and accessible names, roles, states, and consequences align.

## IN-002 — Affordances and signifiers
- [ ] Controls and static content are distinguishable; focus, selection, and active states differ.
- [ ] Handles, targets, themes, and unfamiliar patterns provide sufficient cues.

## IN-003 — Feedback and status
- [ ] Input acknowledgement, outcome, freshness, recovery, and assistive announcements are defined.
- [ ] Routine feedback does not compete with critical alerts or enable duplicate submission.

## IN-004 — Interaction states
- [ ] Applicable states and valid transitions are documented visually and semantically.
- [ ] Focus remains visible and rare states are included.

## IN-005 — Loading and asynchronous behavior
- [ ] Start, progress, cancellation, completion, failure, retry, timeout, and partial results are honest.
- [ ] Duplicate jobs and destructive layout shifts are prevented.

## IN-006 — Motion
- [ ] Motion has purpose, respects reduced motion, and does not carry essential meaning alone.
- [ ] Persistent movement, flashing, and moving targets are controlled.

## IN-007 — Errors
- [ ] Predictable errors are prevented; remaining errors are identified, associated, and correctable.
- [ ] Valid input survives and high-impact submissions support review.

## IN-008 — Recovery
- [ ] Exit, cancellation, undo, retry, draft, conflict, and context restoration are defined.
- [ ] Cancellation is not coercively obstructed and irrecoverability is disclosed.

## IN-009 — Destructive actions
- [ ] Action, object, scope, consequence, permission, and downstream effects are visible.
- [ ] Confirmation and separation are proportional; bulk and stale-state cases are tested.

## IN-010 — Input modalities
- [ ] Primary tasks work with keyboard and applicable pointer/touch alternatives.
- [ ] Focus order, overlays, targets, timing, shortcuts, zoom, and accessible semantics are verified.

## Conformance evidence
- [ ] Interaction declaration, state matrix, error/recovery, destructive, motion, async, and modality evidence is attached.
- [ ] Every relevant MUST and MUST NOT rule passes or has an approved exception.

## Decision

- [ ] Every finding includes evidence, severity, primary rule, related rules, correction, owner, and verification method.
- [ ] Critical and unresolved Major findings prevent Pass.
