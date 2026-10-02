# Foundation Principles

- **Document ID:** UIXS-FP
- **Version:** 0.3.0
- **Status:** Candidate
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Review cadence:** On normative change and before each stable release
- **Related standards:** IA, VF, IN, CB, DV, AX, RS, CT, EP, QA

## Contents

- [Purpose](#purpose)
- [Scope](#scope)
- [Terminology](#terminology)
- [Principle index](#principle-index)
- [FP-001 — Start with user needs](#fp-001--start-with-user-needs)
- [FP-002 — Prefer clarity over cleverness](#fp-002--prefer-clarity-over-cleverness)
- [FP-003 — Prioritize effectiveness](#fp-003--prioritize-effectiveness)
- [FP-004 — Make accessibility the default](#fp-004--make-accessibility-the-default)
- [FP-005 — Build hierarchy from purpose](#fp-005--build-hierarchy-from-purpose)
- [FP-006 — Reveal complexity progressively](#fp-006--reveal-complexity-progressively)
- [FP-007 — Prefer recognition over recall](#fp-007--prefer-recognition-over-recall)
- [FP-008 — Be consistent, not blindly uniform](#fp-008--be-consistent-not-blindly-uniform)
- [FP-009 — Preserve user control](#fp-009--preserve-user-control)
- [FP-010 — Prevent errors](#fp-010--prevent-errors)
- [FP-011 — Communicate system status](#fp-011--communicate-system-status)
- [FP-012 — Represent data honestly](#fp-012--represent-data-honestly)
- [FP-013 — Protect user interests](#fp-013--protect-user-interests)
- [FP-014 — Base decisions on evidence](#fp-014--base-decisions-on-evidence)
- [Conflict resolution](#conflict-resolution)
- [Rule boundaries](#rule-boundaries)
- [Conformance](#conformance)
- [Evidence basis](#evidence-basis)

## Purpose

Define the non-negotiable values used to resolve UI/UX decisions across every standard area. Topic standards translate these principles into detailed requirements; they may refine but must not silently contradict them.

## Scope

These principles apply to planning, research, information architecture, visual design, interaction, components, dashboards, accessibility, responsive behavior, content, privacy, ethics, implementation review, and quality assurance.

They do not replace domain research, legal obligations, accessibility criteria, or topic-specific validation. When a more specific standard provides stricter protection, the stricter requirement applies.

## Terminology

- **User need:** an evidence-backed outcome a person must achieve, understand, decide, or avoid.
- **Primary task:** the main action or decision supported by a flow or screen.
- **Material information:** information that could change a user's decision, interpretation, consent, or safety.
- **Critical flow:** a flow involving safety, money, legal effect, privacy, access, irreversible action, or major data interpretation.
- **Dark pattern:** a design that manipulates, obstructs, or deceives users into choices they would not otherwise make.
- **Evidence:** research, observed behavior, analytics, domain knowledge, accessibility results, support data, or validated constraints.
- **Approved exception:** a documented, time-bounded deviation with evidence, risk, mitigation, owner, and review date.

## Principle index

| ID | Principle | Level | Primary concern |
|---|---|---|---|
| FP-001 | Start with user needs | MUST | Relevance |
| FP-002 | Prefer clarity over cleverness | MUST | Comprehension |
| FP-003 | Prioritize effectiveness | MUST | Task success |
| FP-004 | Make accessibility the default | MUST | Inclusive access |
| FP-005 | Build hierarchy from purpose | MUST | Priority |
| FP-006 | Reveal complexity progressively | SHOULD | Cognitive load |
| FP-007 | Prefer recognition over recall | SHOULD | Memory burden |
| FP-008 | Be consistent, not blindly uniform | MUST | Predictability |
| FP-009 | Preserve user control | MUST | Agency and recovery |
| FP-010 | Prevent errors | MUST | Safety and correction |
| FP-011 | Communicate system status | MUST | Feedback |
| FP-012 | Represent data honestly | MUST | Data integrity |
| FP-013 | Protect user interests | MUST | Ethics and consent |
| FP-014 | Base decisions on evidence | MUST | Validation |

---

## FP-001 — Start with user needs

**Level:** MUST

### Rule

Every design decision MUST connect to an identified user need, goal, task, decision, or risk. Features MUST NOT be added only because they are fashionable, requested by an internal stakeholder, or technically available.

### Rationale

Products organized around internal ownership or feature supply make users translate their needs into the organization's model.

### Verification

Identify target users, primary task, desired outcome, evidence source, and risk if the need is unmet. Unverified assumptions must be labeled and assigned for validation.

### Failure examples

Department-driven navigation, feature dumping, and decorative functionality without a user outcome.

---

## FP-002 — Prefer clarity over cleverness

**Level:** MUST

### Rule

Users MUST be able to understand meaning, state, consequence, and the next available action without avoidable guessing. Visual novelty, jargon, metaphor, or brevity MUST NOT reduce comprehension.

### Rationale

Clever presentation creates cost when users must interpret unfamiliar language or behavior before completing a task.

### Verification

Run comprehension, first-click, label, and consequence-prediction checks with representative tasks and realistic content.

### Failure examples

Ambiguous icons, playful error messages without recovery, hidden scope, and labels such as “Proceed” for consequential actions.

---

## FP-003 — Prioritize effectiveness

**Level:** MUST

### Rule

Correct task completion, safety, accessibility, and accurate outcomes MUST take precedence over engagement, speed, conversion, visual novelty, and aesthetic preference.

### Rationale

An interface is not successful when it is attractive or fast but produces incorrect, unsafe, inaccessible, or unwanted outcomes.

### Verification

Define success and failure conditions for primary tasks. Measure completion quality and error impact before optimizing time or engagement.

### Failure examples

Removing review steps from a financial action solely to increase conversion or hiding context to make a dashboard appear simpler.

---

## FP-004 — Make accessibility the default

**Level:** MUST

### Rule

Accessibility MUST be considered from the start. Color, pointer input, sound, motion, position, or visual styling MUST NOT be the only way to perceive, understand, or operate essential information.

### Rationale

Retrofitting accessibility after structural and visual decisions creates avoidable barriers and expensive rework.

### Verification

Identify applicable accessibility criteria and include keyboard, focus, contrast, reflow, text resize, assistive technology, non-color cues, and reduced-motion evidence where relevant.

### Failure examples

Color-only status, hover-only controls, missing focus, image-only instructions, and visual order that contradicts reading order.

---

## FP-005 — Build hierarchy from purpose

**Level:** MUST

### Rule

Information and visual emphasis MUST follow user priority, task sequence, consequence, and risk rather than decoration, organizational rank, or stakeholder preference.

### Rationale

Hierarchy determines what users notice and act on first. Incorrect hierarchy can suppress warnings and distort decisions.

### Verification

Document primary, secondary, tertiary, and critical content. Test whether users identify page purpose, scope, status, and primary action quickly.

### Failure examples

Promotional content dominating operational alerts or every dashboard card receiving equal emphasis.

---

## FP-006 — Reveal complexity progressively

**Level:** SHOULD

### Rule

Show information and controls needed for the current task first, then reveal secondary or advanced detail when requested. Costs, risks, consent, material uncertainty, destructive consequences, and required controls MUST NOT be hidden.

### Rationale

Progressive disclosure reduces cognitive load but becomes deceptive when it hides information necessary for a valid decision.

### Verification

Classify content as primary, secondary, advanced, or critical. Test disclosure discoverability, keyboard access, small-screen behavior, and decision quality before expansion.

### Failure examples

Fees shown only at final confirmation, active filters hidden in a closed drawer, or required field format available only on hover.

---

## FP-007 — Prefer recognition over recall

**Level:** SHOULD

### Rule

Make options, context, state, instructions, and relevant history visible at the point of need. Users SHOULD NOT need to remember information from another screen to complete or verify a task.

### Rationale

Recognition reduces memory burden and supports interruption, learning, and error recovery.

### Verification

Test flows after interruption and direct entry. Confirm that users can identify context, available choices, previous selections, and required formats without memory-dependent steps.

### Failure examples

Requiring users to remember a reference number, prior filter, date range, or validation rule from another screen.

---

## FP-008 — Be consistent, not blindly uniform

**Level:** MUST

### Rule

Equivalent functions and meanings MUST behave and appear consistently. Different contexts MAY use different patterns when user, platform, accessibility, or domain evidence justifies the variation.

### Rationale

Consistency supports recognition, while blind uniformity can force inappropriate patterns onto different tasks.

### Verification

Inventory equivalent roles and intentional variants. Require a documented reason, owner, and migration impact for new variants.

### Failure examples

The same icon has several meanings, or two equivalent primary actions behave differently without reason.

---

## FP-009 — Preserve user control

**Level:** MUST

### Rule

Users MUST understand and control meaningful actions. Risky actions require proportional protection; recoverable actions SHOULD support undo, cancellation, or another clear recovery path.

### Rationale

Control reduces accidental commitment, anxiety, and dependence on support.

### Verification

Review exit, cancel, back, undo, confirmation, permission, and recovery behavior for critical and destructive flows.

### Failure examples

Trapping users in a flow, silent auto-save with harmful consequences, obstructed cancellation, or irreversible deletion without clear confirmation.

---

## FP-010 — Prevent errors

**Level:** MUST

### Rule

Design MUST reduce predictable errors before they occur, preserve valid user input when validation fails, and provide correction or review before high-impact commitment.

### Rationale

Prevention is more effective than relying on users to interpret errors after damage or repeated work.

### Verification

Identify likely errors, impact, prevention, validation timing, correction, review, and recovery. Test invalid, partial, duplicate, stale, and conflicting input.

### Failure examples

Clearing a form after one invalid field, allowing incompatible selections, or placing destructive actions next to routine controls without distinction.

---

## FP-011 — Communicate system status

**Level:** MUST

### Rule

The interface MUST communicate loading, progress, success, failure, empty, changed, offline, stale, and permission states at the relevant time and location.

### Rationale

Without timely feedback, users repeat actions, misinterpret stale data, or believe the system ignored them.

### Verification

Create a state inventory and test delayed, partial, failed, empty, stale, and permission-limited outcomes. Confirm that users know what happened and what to do next.

### Failure examples

Endless loading, success without confirmation, generic “No data” for every cause, and stale data presented as current.

---

## FP-012 — Represent data honestly

**Level:** MUST

### Rule

Metrics, scales, comparisons, denominators, uncertainty, missing data, source, freshness, and time context MUST NOT be presented in a misleading or materially incomplete way.

### Rationale

Visual and numerical choices can change interpretation even when individual values are technically correct.

### Verification

Document metric definitions, populations, units, periods, sources, transformations, missing-data behavior, comparison baselines, and uncertainty. Test whether a reasonable user reaches the intended interpretation.

### Failure examples

Truncated axes without disclosure, missing values treated as zero, prediction presented as fact, and percentage change without denominator or baseline.

---

## FP-013 — Protect user interests

**Level:** MUST

### Rule

Dark patterns, false urgency, hidden consequences, manipulative defaults, obstructed refusal or cancellation, disguised advertising, and coerced consent MUST NOT be used.

### Rationale

A product must not optimize organizational outcomes by undermining informed choice or user welfare.

### Verification

Compare accept and refuse paths, inspect defaults, timing, prominence, cancellation effort, disclosure, consent granularity, and consequence clarity.

### Failure examples

Preselected non-essential consent, hidden fees, shame-based refusal copy, false scarcity, or cancellation that is materially harder than enrollment.

---

## FP-014 — Base decisions on evidence

**Level:** MUST

### Rule

Important assumptions MUST be identified. High-risk and critical flows SHOULD be validated with representative evidence and iterated after evaluation.

### Rationale

Opinion and convention are insufficient when decisions affect safety, access, money, privacy, or analytical interpretation.

### Verification

Maintain an assumption and evidence record containing source, confidence, affected users, risk, owner, and validation plan. Separate observed evidence from design preference.

### Failure examples

Declaring a pattern “best practice” without applicability evidence or shipping a critical flow based only on stakeholder preference.

## Conflict resolution

Apply this precedence when principles or standards appear to conflict:

1. safety and prevention of harm;
2. user rights, privacy, and control;
3. accessibility;
4. correct task completion;
5. honest information and data representation;
6. clarity;
7. consistency;
8. efficiency;
9. aesthetics.

### Resolution procedure

1. Identify the specific conflicting requirements and affected users.
2. Apply the highest relevant precedence category.
3. Prefer the option with the least irreversible harm.
4. Document evidence, trade-off, residual risk, owner, and review date.
5. Use the exception process for any unsatisfied MUST rule.
6. Validate the chosen resolution when the impact is Major or Critical.

## Rule boundaries

Foundation Principles own values, precedence, and non-negotiable outcomes. Topic standards own detailed implementation and validation:

- IA owns information structure and findability.
- VF owns visual presentation and hierarchy.
- IN and CB own behavior and component interaction.
- AX is authoritative for accessibility conformance.
- RS owns adaptive behavior and reflow patterns.
- DV owns analytical encoding and visualization selection.
- CT owns interface language and content behavior.
- EP owns ethical, privacy, consent, and automation policy.
- QA owns severity, evidence, audit, and release decisions.

When one problem violates several principles or standards, record one primary finding under the most specific owning rule and list Foundation Principles as related. Do not inflate severity by duplicating the same user impact.

## Conformance

A design or standard conforms to Foundation Principles when every relevant MUST and MUST NOT requirement passes or has an approved exception.

### Automatic Fail conditions

- a material accessibility barrier is knowingly accepted without approved mitigation;
- data is materially misleading;
- a dark pattern or coerced consent is present;
- a Critical safety or rights risk is hidden;
- users cannot control or recover from a consequential action;
- a Critical finding is dismissed solely for aesthetics, engagement, or delivery speed.

SHOULD findings may produce Conditional Pass when task safety and correctness remain intact and an owner, rationale, mitigation, and review date exist.

## Evidence basis

- [GOV.UK Government Design Principles](https://www.gov.uk/guidance/government-design-principles) — start with user needs, do less, design with data, and be consistent rather than uniform.
- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/) — system status, user control, consistency, recognition, error prevention, recovery, and minimalist design.
- [Nielsen Norman Group: Progressive Disclosure](https://www.nngroup.com/articles/progressive-disclosure/) — stage secondary complexity while preserving primary tasks.
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) — perceivable, operable, understandable, and robust accessibility requirements.
- [W3C: Ethical Web Principles](https://www.w3.org/TR/ethical-web-principles/) — user control, privacy, security, and avoidance of harm.

## Audit status

Internal structural audit and controlled workflow validation passed on 2026-10-01. Candidate status means the principles are ready to govern later standards, but rendered, accessibility, localization, and representative-user evidence remain required before Stable status.

See `audits/2026-10-01-foundation-principles.md` and `validation/2026-10-01-foundation-principles-workflow.md`.
