# Information Architecture Audit Checklist

- **Checklist ID:** UIXS-IA-CHECK
- **Version:** 0.1.0
- **Status:** Draft
- **Related standard:** `references/01-information-architecture.md`

Use this checklist after selecting only the rules relevant to the reviewed product and flow. Record evidence, severity, owner, and resolution for every failed item.

## Applicability preflight

- [ ] Review scope, users, tasks, entry points, and risk are stated.
- [ ] Relevant IA rules are selected before detailed evaluation.
- [ ] Excluded IA rules have a short applicability reason.
- [ ] One primary owner rule is selected for overlapping symptoms.
- [ ] Expected output includes evidence, severity, primary rule, related rules, correction, and verification.

## IA-001 — User tasks

- [ ] Primary users, goals, frequent tasks, critical information, and risks are documented.
- [ ] Every major area maps to a user task rather than internal ownership.
- [ ] Related tasks are grouped using user-recognized language.

## IA-002 — Hierarchy

- [ ] Every hierarchy level has a distinct purpose.
- [ ] Parent–child relationships are valid and categories, views, objects, and actions are distinct.
- [ ] Users can identify their location and a structural route back.
- [ ] Sibling categories do not overlap without an explicit model.
- [ ] Heading structure matches content structure.

## IA-003 — Labels

- [ ] One preferred term represents each concept.
- [ ] Sibling labels are distinguishable and predict their destination or result.
- [ ] Action labels name the action and affected object.
- [ ] Filters, metrics, units, periods, and destructive consequences are explicit.
- [ ] Visible and accessible labels align and remain usable under localization.

## IA-004 — Wayfinding

- [ ] Page title, active destination, parent context, and risk-relevant scope are visible.
- [ ] Breadcrumbs represent hierarchy, not visit history.
- [ ] Direct links and small-screen layouts retain orientation.
- [ ] Navigation regions and current state are available to assistive technology.

## IA-005 — Navigation, search, filter, and sort

- [ ] Each mechanism has a distinct purpose, label, scope, state, and outcome.
- [ ] Active query, filters, and sort are visible and individually resettable.
- [ ] Sorting changes order only, not record membership or metric meaning.
- [ ] Empty dataset, no result, permission limit, and failure states are distinguished.

## IA-006 — Context preservation

- [ ] State is classified as persistent, resettable, transient, work-in-progress, or sensitive.
- [ ] Detail-and-return, browser navigation, refresh, and direct entry preserve a coherent state.
- [ ] Scope changes reset only incompatible state and explain material changes.
- [ ] Unsaved work is protected and sensitive state is not exposed in shareable persistence.
- [ ] Restored state remains visible and focus returns to a meaningful location.

## IA-007 — Progressive disclosure

- [ ] Primary state, required input, primary action, and active context are visible.
- [ ] Cost, risk, consent, destructive consequences, uncertainty, and blocking errors appear before commitment.
- [ ] Disclosure triggers describe what they reveal and communicate expanded state.
- [ ] Partial, sampled, aggregated, or truncated data is identified.
- [ ] Essential content works without hover and remains available on small screens.

## IA-008 — Taxonomy

- [ ] Purpose, object type, category boundaries, canonical IDs, and owner are documented.
- [ ] Preferred terms, synonyms, deprecated terms, and category lifecycle are governed.
- [ ] Hierarchies and independent facets are modeled deliberately.
- [ ] Duplicate, “Other,” uncategorized, and restricted categories are monitored safely.
- [ ] Rename, merge, split, deprecation, localization, permission, and historical migration behavior are defined.

## Conformance decision

- [ ] All relevant MUST and MUST NOT requirements pass or have approved exceptions.
- [ ] Duplicate symptoms are recorded once under the owning rule with related rule IDs.
- [ ] Every Critical or Major finding has been resolved before Pass.
- [ ] Conditional Pass findings have an owner, rationale, mitigation, and review date.
- [ ] Evidence and assumptions are attached to the audit result.
