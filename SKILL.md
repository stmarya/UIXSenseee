---
name: uiux-design-standard
description: Apply professional, accessible, ethical, and data-aware UI/UX standards when planning, generating, reviewing, or improving interfaces, dashboards, design systems, wireframes, prototypes, and frontend implementations. Use for UI/UX decisions, interface audits, dashboard hierarchy, information architecture, interaction behavior, accessibility, responsive behavior, content design, data visualization, and design QA.
---

# UI/UX Design Standard

## Objective

Apply the UIXSenseee standards consistently without substituting visual trends for user needs, usability, accessibility, or honest data communication.

## Required inputs

Before producing or reviewing a design, identify when available:

- target users;
- primary user goals and tasks;
- product and data context;
- supported devices and interaction modes;
- accessibility requirements;
- risks, constraints, and success criteria.

Mark missing information as an assumption. Do not silently invent business requirements.

## Core workflow

1. Identify the user, goal, task, and decision context.
2. Read `references/00-foundation-principles.md`.
3. Read only the topic references relevant to the task.
4. Apply every relevant MUST and MUST NOT rule.
5. Apply SHOULD rules unless a documented reason prevents it.
6. Run the relevant checklist.
7. Report failures by rule ID and severity.
8. Document exceptions, risks, and mitigations.
9. Do not declare a design conformant while a Critical or unresolved Major issue remains.

## Reference selection

- Information structure, navigation, hierarchy, labels, findability: `references/01-information-architecture.md`
- Visual hierarchy, layout, spacing, typography, color, surfaces, and iconography: `references/02-visual-foundation.md`
- Interaction discoverability, feedback, states, loading, motion, errors, recovery, and input modalities: `references/03-interaction-standards.md`
- Interaction Standards review: `checklists/interaction-standards-review.md`
- Component-specific behavior for controls, forms, overlays, feedback, collections, and menus: `references/04-component-behavior.md`
- Component Behavior review: `checklists/component-behavior-review.md`
- Accessibility conformance, semantics, keyboard, focus, contrast, reflow, media, status, and complex data: `references/06-accessibility.md`
- Accessibility review: `checklists/accessibility-review.md`
- Responsive and adaptive priority, reflow, navigation, forms, collections, charts, modality, localization, and state: `references/07-responsive-adaptive-design.md`
- Responsive review: `checklists/responsive-adaptive-review.md`
- Visual Foundation review: `checklists/visual-foundation-review.md`
- Information Architecture audit: `checklists/information-architecture-review.md`
- General design review: `checklists/design-review.md`
- Release decision: `checklists/release-gate.md`

Additional reference files will be added as their standards are approved.

## Rule precedence

When rules conflict, use this order:

1. User safety and prevention of harm
2. User rights, privacy, and control
3. Accessibility
4. Task completion
5. Honest information and data representation
6. Clarity
7. Consistency
8. Efficiency
9. Aesthetics

## Expected output

When reviewing a design, provide:

- summary and scope;
- assumptions;
- applicability: rules selected and rules excluded;
- findings grouped by severity;
- one primary rule ID and optional related rule IDs per finding;
- recommended corrections;
- exceptions and residual risks;
- verification method for each correction;
- final result: Pass, Conditional Pass, or Fail.

## Exceptions

A MUST rule may be overridden only when a higher-priority rule conflicts with it or evidence demonstrates a necessary constraint. Record the affected rule, evidence, users, risks, mitigation, owner, and review date using `templates/exception-request-template.md`.
