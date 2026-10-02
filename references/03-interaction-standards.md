# Interaction Standards

- **Document ID:** UIXS-IN
- **Version:** 0.10.0
- **Status:** Draft
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Review cadence:** On normative change and before each stable release
- **Related standards:** FP, IA, VF, CB, AX, RS, CT, EP, QA

## Contents

- [Purpose](#purpose)
- [Scope](#scope)
- [Out of scope](#out-of-scope)
- [Terminology](#terminology)
- [Core principles](#core-principles)
- [IN-001 — Make interactions discoverable and predictable](#in-001--make-interactions-discoverable-and-predictable)
- [IN-002 — Provide clear affordances and signifiers](#in-002--provide-clear-affordances-and-signifiers)
- [IN-003 — Communicate feedback and system status](#in-003--communicate-feedback-and-system-status)
- [IN-004 — Define complete and consistent interaction states](#in-004--define-complete-and-consistent-interaction-states)
- [IN-005 — Design loading, progress, and asynchronous behavior](#in-005--design-loading-progress-and-asynchronous-behavior)
- [IN-006 — Use motion purposefully and safely](#in-006--use-motion-purposefully-and-safely)
- [IN-007 — Prevent, identify, and correct errors](#in-007--prevent-identify-and-correct-errors)
- [IN-008 — Support undo, cancellation, and recovery](#in-008--support-undo-cancellation-and-recovery)
- [IN-009 — Protect destructive and irreversible actions](#in-009--protect-destructive-and-irreversible-actions)
- [IN-010 — Support keyboard, pointer, touch, and assistive interaction](#in-010--support-keyboard-pointer-touch-and-assistive-interaction)
- [Interaction Standards conformance](#interaction-standards-conformance)
- [Planned rules](#planned-rules)
- [Evidence basis](#evidence-basis)

## Purpose

Define technology-agnostic interaction rules that help users recognize available actions, predict outcomes, understand system response, prevent errors, and recover without losing control or context.

## Scope

Applies to navigation actions, buttons, links, direct manipulation, gestures, commands, forms, filters, tables, dashboards, dialogs, drawers, menus, notifications, loading, feedback, errors, recovery, destructive actions, keyboard, pointer, touch, and assistive interaction.

## Out of scope

This document does not define detailed component anatomy, visual token values, accessibility success criteria, content wording, or implementation APIs except where they directly change interaction meaning. CB owns component-specific behavior, VF owns visual presentation, AX owns accessibility conformance, and CT owns final interface language.

## Terminology

- **Interaction:** an exchange in which user input or system change affects state, data, navigation, or presentation.
- **Affordance:** what an object or control allows a user to do.
- **Signifier:** a perceivable cue indicating that an interaction is available and how it works.
- **Outcome:** the observable result of an interaction.
- **Scope:** the object, records, page, workspace, or system affected by an action.
- **Direct manipulation:** interaction with a visible object through dragging, resizing, reordering, or similar control.
- **Mode:** a state in which the same input has a different meaning or effect.
- **Gesture:** pointer, touch, stylus, or motion input beyond a simple activation.
- **Command:** an action that changes data, system state, or output rather than navigating to a location.
- **Reversible action:** an action whose prior state can be restored reliably.
- **Destructive action:** an action that removes, overwrites, revokes, publishes, sends, or otherwise creates meaningful loss or commitment.

## Core principles

- **IN-P01 Discoverable:** available actions and controls can be found without guesswork.
- **IN-P02 Predictable:** users can anticipate scope, consequence, and state change before activation.
- **IN-P03 Responsive:** the system acknowledges input and communicates progress and outcome.
- **IN-P04 Preventive:** predictable errors are prevented before recovery is required.
- **IN-P05 Reversible:** recoverable actions support undo, cancellation, or restoration.
- **IN-P06 Modality inclusive:** essential operation does not depend on one input modality.
- **IN-P07 Context preserving:** interactions do not silently discard scope, state, or work.
- **IN-P08 Proportional:** friction and confirmation match consequence and reversibility.

---

## IN-001 — Make interactions discoverable and predictable

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-007, FP-008, FP-009, IA-003, IA-004, IA-005, VF-001, VF-008

### Rule

Interactive elements and behaviors MUST provide sufficient cues for users to discover that an interaction is available and predict its target, scope, consequence, and resulting context before activation.

### Rationale

Users should not need to experiment with risky actions, memorize hidden gestures, or infer outcomes from visual novelty. Discoverability supports first use; predictability supports trust, speed, and error prevention.

### Interaction declaration

For each meaningful interaction, document:

- trigger and input modalities;
- visible and accessible label;
- affected object and scope;
- expected outcome;
- reversibility and risk;
- required permission;
- state before, during, and after activation;
- alternate path when the primary interaction is unavailable.

### Requirements

- **IN-001-A — Make interactive elements recognizable — MUST.** Controls must be distinguishable from static content before activation.
- **IN-001-B — Avoid false affordance — MUST.** Static content must not appear interactive, and interactive surfaces must not appear inert.
- **IN-001-C — Label actions by outcome — MUST.** Users must be able to predict the action and affected object; generic labels such as “Proceed” require sufficient context.
- **IN-001-D — Communicate target and scope — MUST.** Actions must make clear which record, selection, page, workspace, account, or dataset they affect.
- **IN-001-E — Communicate meaningful consequence — MUST.** Cost, publication, sharing, permission, deletion, overwrite, and irreversible effects must be visible before commitment.
- **IN-001-F — Keep interaction meaning consistent — MUST.** Equivalent triggers and patterns must produce equivalent outcomes unless a contextual difference is explicit.
- **IN-001-G — Distinguish navigation from commands — MUST.** Links and destinations must not be confused with actions that modify data or system state.
- **IN-001-H — Make interaction availability visible — MUST.** Users must be able to determine whether an action is available, unavailable, restricted, or pending.
- **IN-001-I — Explain unavailable actions when needed — SHOULD.** Disabled or hidden behavior must not leave users unable to understand how to proceed or obtain permission.
- **IN-001-J — Do not require hover for discovery — MUST NOT.** Essential controls, labels, scope, and consequences must be discoverable through keyboard and touch as well as pointer input.
- **IN-001-K — Provide alternatives to complex gestures — MUST.** Drag, swipe, pinch, multi-touch, path, or motion gestures require a simpler operable alternative when they perform essential functions.
- **IN-001-L — Avoid hidden mode changes — MUST NOT.** If input meaning changes because of a mode, the active mode, available actions, and exit path must be visible.
- **IN-001-M — Preserve context across activation — MUST.** The result must not silently change workspace, period, selection, permission scope, or analytical meaning.
- **IN-001-N — Disclose new context — MUST.** Opening a new tab, external service, download, full-screen mode, or separate workspace should be predictable when it changes workflow materially.
- **IN-001-O — Keep controls near affected objects — SHOULD.** Contextual actions should remain associated with the object or selection they affect.
- **IN-001-P — Avoid interaction by decoration — MUST.** Animation, shadow, color, icon, or novelty alone must not be the only indication of interactivity.
- **IN-001-Q — Make direct manipulation explicit — MUST.** Draggable, resizable, or reorderable objects need visible handles, instructions, or another discoverable cue plus an alternative method.
- **IN-001-R — Prevent accidental activation — MUST.** Placement, target, gesture, and activation behavior must account for destructive consequences and common input errors.
- **IN-001-S — Make selection state perceivable — MUST.** Users must know which objects, rows, filters, or ranges an action will affect before activation.
- **IN-001-T — Keep command search explicit — MUST.** Command palettes and unified search must label result types and distinguish navigation, creation, modification, and external actions.
- **IN-001-U — Support input modalities — MUST.** Essential interactions must not depend exclusively on precise pointer movement, touch, keyboard shortcuts, voice, or another single modality.
- **IN-001-V — Keep accessible and visible meaning aligned — MUST.** Accessible names, roles, states, and descriptions must match the visible interaction and consequence.

### Dashboard policy

- Global filters, local filters, navigation, drill-down, selection, and export must have distinct cues.
- Chart points and visual regions requiring interaction must provide keyboard/touch alternatives or an equivalent data view.
- Selection and multi-selection must remain visible before batch action.
- Download, refresh, recalculate, and share must not appear as equivalent navigation destinations.
- Interaction must not silently change metric definition, period, population, or aggregation.

### Validation

- **Expectation test:** ask users what will happen, what will be affected, and whether it can be reversed before activation.
- **First-use discovery test:** observe whether a user can find the action without instruction.
- **False-affordance audit:** identify static elements that appear clickable and interactive elements that appear static.
- **Scope test:** select multiple objects and verify users can identify affected records and workspace.
- **Modality test:** operate essential interactions with keyboard, touch, and pointer alternatives where applicable.
- **Mode test:** enter and exit every mode and verify active mode remains visible.
- **Gesture-alternative test:** complete gesture-based tasks using a non-gesture path.
- **Direct-entry test:** verify commands remain understandable from deep links or alternate entry points.
- **Accessibility alignment test:** compare visible labels and states with accessible names, roles, and properties.

### Exceptions

Expert tools MAY use compact shortcuts, gestures, or command syntax when a discoverable standard path remains available and training context is appropriate. Game, canvas, map, or creative tools MAY use specialized direct manipulation when orientation, alternatives, and safe recovery are provided.

### Failure examples

- A static card and clickable card use identical treatment.
- An unlabeled icon publishes or permanently deletes content.
- Swipe is the only method to remove or reveal an item.
- A disabled action provides no explanation or path to permission.
- “Apply” silently changes workspace and date range.
- Dragging is possible but no handle, instruction, or keyboard alternative exists.
- A command palette mixes navigation and destructive commands without type labels.
- Batch action gives no visible indication of selected records.
- An active editing mode is not visible and Escape behavior is unknown.

### Acceptance

**Fail** when essential interactions are undiscoverable, consequences or scope are hidden, risky actions are easily activated by mistake, modes are invisible, or operation depends on one inaccessible modality. **Conditional Pass** may cover non-blocking discoverability improvements with an owner and verification plan. **Pass** requires all relevant MUST and MUST NOT requirements or approved exceptions.

---

## IN-002 — Provide clear affordances and signifiers

**Level:** MUST  
**Status:** Draft  
**Related:** IN-001, VF-005, VF-006, VF-007, CB, AX

### Rule

Controls MUST expose perceivable and consistent signifiers that communicate how they can be operated and whether they are interactive, selected, unavailable, or in a mode.

### Rationale

Affordance is ineffective when users cannot perceive it. False or weak signifiers cause missed actions and accidental activation.

### Requirements

- **IN-002-A — Distinguish controls from content — MUST.** Interactive and static elements require different perceivable treatment.
- **IN-002-B — Match appearance to behavior — MUST.** Buttons act, links navigate, fields accept input, and handles manipulate visible objects.
- **IN-002-C — Use redundant signifiers — MUST.** Critical interaction must not depend on color, hover, shadow, or icon alone.
- **IN-002-D — Keep signifiers consistent — MUST.** Equivalent behaviors use equivalent cues across contexts.
- **IN-002-E — Show focus and selection separately — MUST.** Keyboard focus, selected state, and active state must not be conflated.
- **IN-002-F — Make handles and targets perceivable — MUST.** Resize, drag, disclosure, and overflow triggers need visible or discoverable cues.
- **IN-002-G — Preserve signifiers across themes — MUST.** Light, dark, high-contrast, and forced-color modes retain interaction meaning.
- **IN-002-H — Avoid decorative false affordance — MUST NOT.** Static cards, labels, and images must not resemble controls without behavior.
- **IN-002-I — Keep target and visual object associated — MUST.** Large invisible hit areas must not trigger unrelated nearby actions.
- **IN-002-J — Validate unfamiliar patterns — SHOULD.** Novel signifiers require comprehension testing and a familiar alternative where risk is material.

### Validation

Run false-affordance, first-click, focus-versus-selection, theme, touch-target, and unfamiliar-pattern comprehension tests.

### Exceptions

Expert canvases MAY use specialized handles or cursors when onboarding and keyboard alternatives exist.

### Failure examples

Clickable and static cards look identical; a disclosure chevron is decorative; focus disappears inside selection; shadow is the only button cue.

### Acceptance

Fail when essential controls appear static, static content appears actionable, or focus and selection cannot be distinguished.

---

## IN-003 — Communicate feedback and system status

**Level:** MUST  
**Status:** Draft  
**Related:** FP-011, IA-004, VF-008, CT, AX

### Rule

The system MUST acknowledge input and communicate current state, progress, outcome, and required next action at the time and location users need it.

### Rationale

Without timely feedback users repeat actions, abandon work, or misinterpret stale and failed results.

### Requirements

- **IN-003-A — Acknowledge activation — MUST.** Input receives immediate perceivable acknowledgement.
- **IN-003-B — Communicate outcome — MUST.** Success, failure, partial success, and cancellation are distinguishable.
- **IN-003-C — Place feedback near context — SHOULD.** Messages remain associated with the action or affected object.
- **IN-003-D — Announce dynamic status — MUST.** Assistive technology receives important status without disruptive focus changes.
- **IN-003-E — Preserve feedback long enough — MUST.** Users have adequate time to perceive and act on messages.
- **IN-003-F — Avoid notification overload — MUST.** Routine success must not compete with critical alerts.
- **IN-003-G — Identify changed data — SHOULD.** Refresh, save, recalculation, and collaboration changes expose what changed.
- **IN-003-H — Distinguish stale and live state — MUST.** Freshness, offline, cached, and synchronization status are clear.
- **IN-003-I — Provide next action — MUST.** Failure and blocking status include recovery or escalation where available.
- **IN-003-J — Prevent duplicate submission — MUST.** Feedback and control state reduce repeated consequential actions.

### Validation

Test slow, failed, partial, offline, stale, duplicate, background, and assistive-announcement scenarios.

### Exceptions

Low-risk instantaneous actions MAY use subtle feedback when the changed state itself is unambiguous.

### Failure examples

Silent saves, disappearing errors, generic success for partial completion, and stale data presented as current.

### Acceptance

Fail when users cannot tell whether input was received, whether work succeeded, or how to recover.

---

## IN-004 — Define complete and consistent interaction states

**Level:** MUST  
**Status:** Draft  
**Related:** VF-008, IN-002, IN-003, CB, AX

### Rule

Every component MUST define all applicable states and preserve distinct meaning, operation, focus, and feedback across them.

### Requirements

- **IN-004-A — Define applicable states — MUST.** Consider default, hover, focus, active, selected, disabled, loading, success, warning, error, empty, and permission states.
- **IN-004-B — Distinguish state meanings — MUST.** Focus, hover, selected, error, and disabled are not interchangeable.
- **IN-004-C — Preserve focus visibility — MUST.** No state treatment may erase focus.
- **IN-004-D — Expose state semantically — MUST.** Accessible role, value, expanded, selected, checked, invalid, busy, and disabled state align with visible state.
- **IN-004-E — Keep state transitions valid — MUST.** Impossible or contradictory state combinations are prevented.
- **IN-004-F — Explain disabled state where needed — SHOULD.** Users can understand prerequisites or permission paths.
- **IN-004-G — Avoid disabled when read-only is intended — MUST.** Read-only information remains perceivable and selectable as appropriate.
- **IN-004-H — Keep states consistent across themes — MUST.** Meaning survives visual-theme changes.
- **IN-004-I — Define rare states — MUST.** Expired, stale, conflict, partial, and permission states are not omitted.
- **IN-004-J — Prevent state-only layout shift — SHOULD.** State changes do not move targets unexpectedly.

### Validation

Create a state matrix and test every applicable state with keyboard, assistive technology, themes, and unusual data.

### Exceptions

A state may be marked not applicable when behavior and evidence justify omission.

### Failure examples

Selected and error share one border; focus vanishes on hover; read-only data is dimmed as disabled; permission state is missing.

### Acceptance

Fail when critical states are absent, contradictory, visually or semantically misrepresented, or focus is lost.

---

## IN-005 — Design loading, progress, and asynchronous behavior

**Level:** MUST  
**Status:** Draft  
**Related:** FP-011, IN-003, IN-004, RS, AX

### Rule

Asynchronous interactions MUST communicate start, progress or indeterminate activity, available cancellation, completion, failure, and freshness without fabricating certainty or blocking unrelated work unnecessarily.

### Requirements

- **IN-005-A — Indicate delayed activity — MUST.** Users know when work has started.
- **IN-005-B — Use determinate progress honestly — MUST.** Percent or remaining time appears only when credible.
- **IN-005-C — Use indeterminate state for unknown duration — MUST.** Do not display fake linear progress.
- **IN-005-D — Preserve layout and context — SHOULD.** Loading does not replace page identity or move critical actions unexpectedly.
- **IN-005-E — Support cancellation where meaningful — SHOULD.** Long or costly work exposes safe cancellation and its consequence.
- **IN-005-F — Distinguish queued, running, paused, cancelled, failed, and complete — MUST.** Status labels remain accurate.
- **IN-005-G — Communicate background completion — MUST.** Users can leave and later identify outcome when background work is supported.
- **IN-005-H — Prevent duplicate jobs — MUST.** Repeated activation does not create unintended copies.
- **IN-005-I — Expose partial results carefully — MUST.** Partial data is labeled and does not appear complete.
- **IN-005-J — Provide timeout recovery — MUST.** Timeouts explain retained work and safe retry.

### Validation

Simulate fast, slow, queued, paused, cancelled, timeout, offline, retry, partial, and background completion.

### Exceptions

Very brief low-risk activity may use changed control state instead of a separate indicator.

### Failure examples

Endless spinner, fake 99% progress, retry creating duplicates, partial data shown as final, and navigation destroying a background job.

### Acceptance

Fail when users cannot identify activity or outcome, progress is deceptive, or retry creates harmful duplication.

---

## IN-006 — Use motion purposefully and safely

**Level:** MUST  
**Status:** Draft  
**Related:** FP-004, VF, RS, AX

### Rule

Motion MUST communicate relationship, orientation, state, or feedback without becoming the only carrier of meaning, delaying tasks, or causing avoidable discomfort.

### Requirements

- **IN-006-A — Give motion a functional purpose — MUST.** Motion explains change, hierarchy, continuity, or feedback.
- **IN-006-B — Do not rely on motion alone — MUST NOT.** State and meaning remain available when motion is removed.
- **IN-006-C — Respect reduced-motion preference — MUST.** Non-essential animation is removed or simplified.
- **IN-006-D — Avoid seizure and vestibular risk — MUST.** Flashing, large movement, parallax, and zoom effects follow accessibility limits.
- **IN-006-E — Keep routine interaction fast — SHOULD.** Animation does not delay repeated work.
- **IN-006-F — Preserve input during motion — MUST.** Controls do not become unpredictably unavailable or move under the pointer.
- **IN-006-G — Allow stopping persistent motion — MUST.** Auto-playing or repeated movement can be paused where applicable.
- **IN-006-H — Use consistent transition meaning — SHOULD.** Similar spatial changes use similar motion.
- **IN-006-I — Avoid decorative dashboard motion — SHOULD NOT.** Live data does not pulse or animate without decision value.
- **IN-006-J — Test low-performance behavior — SHOULD.** Dropped frames do not hide state or block completion.

### Validation

Test reduced motion, keyboard use during transitions, low performance, persistent animation, flashing, parallax, and auto-updating dashboards.

### Exceptions

Media, simulation, and creative tools may require motion when controls, alternatives, and warnings are provided.

### Failure examples

Meaning disappears with reduced motion, controls move while being targeted, and decorative KPI animation repeats continuously.

### Acceptance

Fail when motion is required to understand or operate, violates safety, ignores reduced motion, or causes accidental activation.

---

## IN-007 — Prevent, identify, and correct errors

**Level:** MUST  
**Status:** Draft  
**Related:** FP-010, CT, CB, AX

### Rule

Interactions MUST prevent predictable errors, identify remaining errors clearly, preserve valid work, and provide a specific path to correction.

### Requirements

- **IN-007-A — Prevent invalid choices — SHOULD.** Constraints, defaults, formats, and dependencies reduce errors before submission.
- **IN-007-B — Validate at appropriate time — MUST.** Do not report errors before meaningful interaction; do not delay high-risk validation until too late.
- **IN-007-C — Preserve valid input — MUST.** Errors do not clear correct work.
- **IN-007-D — Identify error in text — MUST.** Color or icon alone is insufficient.
- **IN-007-E — Associate errors with source — MUST.** Field, row, record, or step relationship is clear programmatically and visually.
- **IN-007-F — Provide correction guidance — MUST.** State what failed and how to fix it.
- **IN-007-G — Provide error summary for complex forms — SHOULD.** Summary links to affected locations.
- **IN-007-H — Focus safely — MUST.** Correction flow does not trap or unexpectedly move users.
- **IN-007-I — Distinguish user, system, network, permission, and conflict errors — MUST.** Recovery matches cause.
- **IN-007-J — Review high-impact submissions — MUST.** Legal, financial, destructive, and sensitive submissions support review or correction before final commitment.

### Validation

Test empty, malformed, conflicting, duplicate, expired, permission, server, network, and multi-error cases with keyboard and assistive technology.

### Exceptions

Immediate server validation may be required where correctness depends on remote state, but input and context remain preserved.

### Failure examples

“Invalid input” without guidance, errors shown only in red, valid fields cleared, and a server failure blamed on the user.

### Acceptance

Fail when errors are unidentified, inaccessible, destructive to valid work, or lack a correction path.

---

## IN-008 — Support undo, cancellation, and recovery

**Level:** MUST  
**Status:** Draft  
**Related:** FP-009, IN-003, IN-005, EP

### Rule

Users MUST be able to cancel, exit, undo, retry, restore, or otherwise recover in proportion to the action's consequence and technical reversibility.

### Requirements

- **IN-008-A — Provide a clear exit — MUST.** Users can leave modes, dialogs, and flows without hidden commitment.
- **IN-008-B — Explain cancellation consequence — MUST.** Users know what is retained, discarded, or continues in background.
- **IN-008-C — Prefer undo for reversible actions — SHOULD.** Immediate action plus reliable undo may replace confirmation for low-risk changes.
- **IN-008-D — Make undo discoverable and timely — MUST.** Scope and expiry are clear.
- **IN-008-E — Preserve drafts — SHOULD.** Long or high-effort work supports recovery after interruption.
- **IN-008-F — Support safe retry — MUST.** Retry does not duplicate consequential work.
- **IN-008-G — Resolve conflicts explicitly — MUST.** Concurrent edits expose versions and consequences.
- **IN-008-H — Restore context — MUST.** Recovery returns users to meaningful scope, selection, and focus.
- **IN-008-I — Avoid coercive exit friction — MUST NOT.** Cancellation and refusal are not obstructed for business goals.
- **IN-008-J — Communicate irrecoverability — MUST.** When recovery is impossible, explain before commitment.

### Validation

Test cancel at each step, undo expiry, retry, interruption, refresh, session loss, concurrent edits, and recovery focus.

### Exceptions

Security may require draft expiry or irreversible revocation; consequences and timing remain clear.

### Failure examples

Closing a dialog saves silently, retry duplicates payment, undo gives no scope, and cancellation requires unrelated steps.

### Acceptance

Fail when users are trapped, recovery duplicates harm, cancellation is coercively obstructed, or irrecoverability is hidden.

---

## IN-009 — Protect destructive and irreversible actions

**Level:** MUST  
**Status:** Draft  
**Related:** FP-009, FP-010, FP-013, IN-007, IN-008, EP

### Rule

Destructive, irreversible, externally committing, or high-impact actions MUST receive protection proportional to consequence, likelihood of error, reversibility, and affected scope.

### Requirements

- **IN-009-A — Name action and object — MUST.** Labels identify consequence and affected item.
- **IN-009-B — Show affected scope — MUST.** Counts, selections, workspace, recipients, and dependencies are visible.
- **IN-009-C — Use proportional confirmation — MUST.** Friction increases with impact and irreversibility.
- **IN-009-D — Avoid confirmation fatigue — SHOULD.** Routine reversible actions prefer undo.
- **IN-009-E — Separate destructive controls — MUST.** Placement and styling reduce accidental activation.
- **IN-009-F — Require explicit high-risk confirmation — MUST.** Typed names or equivalent checks may be used for exceptional irreversible scope.
- **IN-009-G — Explain downstream effects — MUST.** Revocation, deletion, publish, send, overwrite, and permission consequences are visible.
- **IN-009-H — Protect batch actions — MUST.** Selection count and review are available.
- **IN-009-I — Verify current authority — MUST.** Permission and stale state are rechecked before commitment.
- **IN-009-J — Provide audit and recovery where possible — SHOULD.** High-impact action records support accountability.

### Validation

Test single, bulk, stale, wrong-workspace, insufficient-permission, repeated, keyboard, and touch activation.

### Exceptions

Emergency and safety-critical actions may require immediate activation when delay causes greater harm; prevention and recovery are documented.

### Failure examples

Generic “Confirm,” delete beside save, hidden recipient list, stale permission, and bulk action without count.

### Acceptance

Fail when scope or consequence is hidden, accidental activation is likely, or irreversible actions lack proportional protection.

---

## IN-010 — Support keyboard, pointer, touch, and assistive interaction

**Level:** MUST  
**Status:** Draft  
**Related:** FP-004, IN-001, IN-002, AX, RS, CB

### Rule

Essential interaction MUST be operable and understandable across applicable input modalities without requiring device-specific precision, hidden gestures, or inaccessible timing.

### Requirements

- **IN-010-A — Support keyboard operation — MUST.** Every essential action is reachable and operable without pointer input.
- **IN-010-B — Maintain logical focus order — MUST.** Focus follows task and semantic sequence.
- **IN-010-C — Avoid keyboard traps — MUST NOT.** Users can enter and leave components and overlays.
- **IN-010-D — Provide visible focus — MUST.** Focus survives all states and themes.
- **IN-010-E — Support pointer and touch safely — MUST.** Targets and spacing reduce accidental activation.
- **IN-010-F — Avoid precision-only interaction — MUST NOT.** Drag, small targets, and narrow paths have alternatives.
- **IN-010-G — Do not depend on hover — MUST NOT.** Essential content and action work with touch and keyboard.
- **IN-010-H — Manage focus in overlays — MUST.** Focus enters, remains appropriately contained, and returns meaningfully.
- **IN-010-I — Expose roles, names, states, and values — MUST.** Assistive technology receives equivalent interaction semantics.
- **IN-010-J — Avoid timing barriers — MUST.** Time limits can be extended, adjusted, or explained where required.
- **IN-010-K — Support orientation and zoom — MUST.** Input remains operable under reflow and magnification.
- **IN-010-L — Preserve shortcut safety — MUST.** Single-key and global shortcuts avoid conflicts and accidental activation.

### Validation

Complete primary flows with keyboard only, touch, pointer, zoom, screen reader, switch-like navigation where applicable, and overlays at viewport edges.

### Exceptions

Path-dependent drawing or freehand input may require pointer movement when an equivalent outcome or accessible alternative is documented.

### Failure examples

Hover-only menu, drag-only reorder, focus trapped in a dialog, tiny adjacent targets, and screen reader state differing from visible state.

### Acceptance

Fail when essential tasks cannot be completed through required modalities, focus is lost or trapped, or accessible semantics contradict visible behavior.

---

## Interaction Standards conformance

A design conforms only when every relevant MUST and MUST NOT requirement from IN-001 through IN-010 passes or has an approved exception. SHOULD findings may produce Conditional Pass when no safety, accessibility, correctness, or user-control risk remains.

### Required evidence

- interaction declaration and scope inventory;
- affordance and false-affordance review;
- feedback and state matrix;
- loading and asynchronous scenarios;
- reduced-motion and transition review;
- error, validation, and correction evidence;
- cancellation, undo, retry, and conflict tests;
- destructive-action scope and protection review;
- keyboard, pointer, touch, focus, and assistive interaction results;
- completed checklist and documented exceptions.

## Evidence basis

- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — visibility, match with the real world, user control, consistency, recognition, and error prevention.
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) — keyboard, pointer, target, focus, labels, status, and input-modality requirements.
- [Material Design 3: Interaction States](https://m3.material.io/foundations/interaction/states) — intentional and consistent component-state communication.
- [GOV.UK: Writing for User Interfaces](https://www.gov.uk/service-manual/design/writing-for-user-interfaces) — clear action language and task-oriented labels.
