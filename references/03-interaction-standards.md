# Interaction Standards

- **Document ID:** UIXS-IN
- **Version:** 0.1.0
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

## Planned rules

- IN-002 — Provide clear affordances and signifiers.
- IN-003 — Communicate feedback and system status.
- IN-004 — Define complete and consistent interaction states.
- IN-005 — Design loading, progress, and asynchronous behavior.
- IN-006 — Use motion purposefully and safely.
- IN-007 — Prevent, identify, and correct errors.
- IN-008 — Support undo, cancellation, and recovery.
- IN-009 — Protect destructive and irreversible actions.
- IN-010 — Support keyboard, pointer, touch, and assistive interaction.

## Evidence basis

- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — visibility, match with the real world, user control, consistency, recognition, and error prevention.
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) — keyboard, pointer, target, focus, labels, status, and input-modality requirements.
- [Material Design 3: Interaction States](https://m3.material.io/foundations/interaction/states) — intentional and consistent component-state communication.
- [GOV.UK: Writing for User Interfaces](https://www.gov.uk/service-manual/design/writing-for-user-interfaces) — clear action language and task-oriented labels.
