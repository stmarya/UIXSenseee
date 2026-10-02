# Content Design & Microcopy

- **Document ID:** UIXS-CT
- **Version:** 0.11.0
- **Status:** Candidate
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Related standards:** FP, IA, VF, IN, CB, DV, AX, RS, EP, QA

## Purpose

Ensure interface language helps users understand, decide, act, recover, and verify outcomes with clarity, consistency, inclusion, and honest context.

## Ownership

CT owns interface language, terminology, formatting, and content behavior. IA owns information structure; IN and CB own behavior and timing; DV owns data meaning; EP owns ethical policy; AX owns accessibility conformance.

---

## CT-001 — Use language users recognize

**Level:** MUST  
**Status:** Candidate

### Rule

Interface content MUST use familiar, direct, specific language appropriate to user expertise and task context.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-001-A — Prefer user vocabulary — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-B — Avoid internal jargon — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-C — Match expertise without condescension — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-D — Use concise active sentences — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-E — Front-load meaningful words — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-F — Avoid unnecessary metaphor — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-G — Explain uncommon abbreviations — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-001-H — Test comprehension — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-002 — Write descriptive titles, labels, and actions

**Level:** MUST  
**Status:** Candidate

### Rule

Titles, navigation, links, buttons, and controls MUST communicate destination, action, object, scope, and consequence.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-002-A — Name destination — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-B — Use verb plus object for action — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-C — Distinguish sibling labels — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-D — Name destructive consequence — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-E — Avoid generic click here or proceed — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-F — Keep visible and accessible labels aligned — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-G — Preserve meaning out of context — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-002-H — Use consistent capitalization — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-003 — Provide timely instructions and form guidance

**Level:** MUST  
**Status:** Candidate

### Rule

Instructions MUST appear at the point of need, explain required formats and constraints, and avoid replacing persistent labels.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-003-A — Place guidance before likely error — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-B — Provide examples where useful — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-C — Explain required and optional — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-D — State format and constraints — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-E — Keep helper text associated — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-F — Avoid instruction overload — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-G — Support progressive disclosure — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-003-H — Preserve guidance for assistive users — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-004 — Write errors that support recovery

**Level:** MUST  
**Status:** Candidate

### Rule

Error content MUST identify the problem, locate its source, preserve user dignity, and explain a specific correction or recovery path.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-004-A — State what happened — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-B — Use same term as affected field — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-C — Explain how to fix — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-D — Separate user and system causes — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-E — Avoid blame and humor at user expense — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-F — Preserve entered values — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-G — Link summaries to errors — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-004-H — Provide escalation when recovery unavailable — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-005 — Distinguish loading, empty, no-result, success, and status content

**Level:** MUST  
**Status:** Candidate

### Rule

System-state content MUST name the actual condition and provide the relevant next action without generic or misleading messages.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-005-A — Distinguish empty and no result — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-B — Distinguish permission and failure — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-C — Name loading or progress when material — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-D — Confirm meaningful success — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-E — Avoid success noise — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-F — Explain stale offline or partial state — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-G — Offer relevant next action — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-005-H — Keep critical status persistent — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-006 — Write confirmations and destructive warnings proportionally

**Level:** MUST  
**Status:** Candidate

### Rule

Confirmation content MUST state action, affected object, scope, consequence, reversibility, and safe alternative in proportion to risk.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-006-A — Name action and object — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-B — Show count and scope — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-C — Explain downstream effects — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-D — State reversibility — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-E — Use specific confirm and cancel labels — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-F — Avoid manipulative safe-option wording — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-G — Match friction to risk — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-006-H — Support review before commitment — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-007 — Govern terminology and naming

**Level:** MUST  
**Status:** Candidate

### Rule

Products MUST maintain preferred terms, definitions, synonyms, deprecated terms, status criteria, and ownership for important concepts.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-007-A — Maintain glossary — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-B — Choose one preferred term — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-C — Define status criteria — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-D — Record discouraged synonyms — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-E — Version terminology changes — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-F — Coordinate UI docs and support — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-G — Assign terminology owner — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-007-H — Validate with domain users — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-008 — Format numbers, dates, time, currency, and units clearly

**Level:** MUST  
**Status:** Candidate

### Rule

Quantitative and temporal content MUST use consistent locale-aware formats, precision, units, timezone, and unambiguous labels.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-008-A — Use locale-aware separators — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-B — State currency unambiguously — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-C — Place units consistently — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-D — Use appropriate precision — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-E — Distinguish percent and percentage points — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-F — State timezone when relevant — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-G — Use absolute date when relative is risky — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-008-H — Avoid ambiguous date formats — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-009 — Design for localization and inclusive language

**Level:** MUST  
**Status:** Candidate

### Rule

Content MUST support translation, bidirectionality, cultural context, respectful identity, and variation in length without stereotyping or exclusion.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-009-A — Avoid string concatenation assumptions — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-B — Allow text expansion — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-C — Support plural and grammar rules — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-D — Review right-to-left meaning — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-E — Avoid idioms and wordplay — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-F — Use inclusive identity language — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-G — Review cultural symbols and examples — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-009-H — Separate translation from canonical identifiers — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

---

## CT-010 — Communicate data, AI, help, and provenance responsibly

**Level:** MUST  
**Status:** Candidate

### Rule

Generated, estimated, recommended, or source-derived content MUST distinguish fact from interpretation and provide help, source, limitation, and verification where material.

### Rationale

Content is part of the interface behavior. Ambiguous, inconsistent, or manipulative language causes errors even when the visual component is technically correct.

### Requirements

- **CT-010-A — Label AI-generated content — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-B — Distinguish observation estimate and recommendation — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-C — Provide source and freshness — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-D — State uncertainty and limitations — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-E — Explain material automation — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-F — Offer correction or challenge path — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-G — Keep help task-oriented and searchable — MUST.** Apply the requirement consistently and validate with realistic context and locale.
- **CT-010-H — Avoid fabricated authority or certainty — MUST.** Apply the requirement consistently and validate with realistic context and locale.

### Validation

Run comprehension, first-click, prediction, error-recovery, content inventory, localization, screen-reader, and realistic-data tests with representative tasks.

### Exceptions

Legal, scientific, or regulated terms MAY be retained when required, but plain-language explanation should accompany them where users need it.

### Failure examples

Jargon, generic actions, placeholder-only guidance, blaming errors, undifferentiated states, hidden consequences, inconsistent terminology, ambiguous formats, untranslatable fragments, and unlabeled AI output.

### Acceptance

Fail when content hides consequence, causes task error, misrepresents data or AI, excludes users, or prevents recovery. Pass requires all relevant mandatory rules or approved exceptions.

## Content conformance

Conformance requires CT-001 through CT-010, realistic-content review, terminology governance, localization readiness, and alignment between visible and accessible language.

### Required evidence

- audience and language profile;
- content and terminology inventory;
- labels and action map;
- form, error, empty, status, and confirmation states;
- quantitative format rules;
- localization and inclusive-language review;
- AI/data source and limitation disclosures;
- comprehension and recovery tests;
- checklist and exceptions.

## Evidence basis

- [GOV.UK: Writing for User Interfaces](https://www.gov.uk/service-manual/design/writing-for-user-interfaces)
- [GOV.UK Content Design](https://www.gov.uk/guidance/content-design)
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [W3C Labels or Instructions](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html)


## Candidate validation status

Internal structural audit and controlled workflow validation passed on 2026-10-01. The validation routed all ten main rules, preserved one-primary-rule ownership, and detected all seeded findings. Candidate status does not imply Stable: rendered-interface, assistive-technology, localization, and representative-user evidence remain required.
