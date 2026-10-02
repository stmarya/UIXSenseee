# Content Design & Microcopy Internal Audit

- **Document:** `references/08-content-design-microcopy.md`
- **Audit date:** 2026-10-01
- **Audited version:** 0.10.0
- **Result:** Passed for Candidate promotion

## Scope and method

The audit checked structure, rule identity, normative language, lifecycle metadata, cross-standard ownership, evidence requirements, checklist coverage, and readiness for controlled workflow validation.

## Structural results

| Check | Result | Evidence |
|---|---|---|
| Main-rule sequence | Pass | CT-001 through CT-010 are present once and in order |
| Sub-rule identity | Pass | 80 unique requirement IDs; eight under every main rule |
| Normative strength | Pass | Every main rule and requirement uses an explicit MUST, MUST NOT, SHOULD, or MAY expectation |
| Verification support | Pass | Each main rule includes validation guidance; the standard defines required evidence |
| Review coverage | Pass | `checklists/content-design-review.md` routes all ten main rules |
| Failure handling | Pass | Acceptance, exception, and nonconformance expectations are explicit |

## Coverage review

| Rule | Primary concern | Audit result |
|---|---|---|
| CT-001 | Recognizable user language | Pass |
| CT-002 | Titles, labels, and actions | Pass |
| CT-003 | Instructions and form guidance | Pass |
| CT-004 | Error messages and recovery | Pass |
| CT-005 | Empty, loading, success, and status content | Pass |
| CT-006 | Confirmation and destructive-action language | Pass |
| CT-007 | Terminology governance | Pass |
| CT-008 | Numbers, dates, currencies, and units | Pass |
| CT-009 | Localization and inclusive language | Pass |
| CT-010 | Data, AI, automation, and help disclosures | Pass |

## Ownership and overlap

- CT owns interface wording, terminology, content patterns, quantitative formatting, and disclosure language.
- IA owns information organization and navigation structure; CT owns the words used within them.
- IN and CB own behavior, timing, and component mechanics; CT owns the associated labels and messages.
- DV owns statistical and visual meaning; CT owns readable labels, units, periods, and explanatory language.
- AX owns accessibility conformance; CT supplies understandable visible and accessible content.
- RS owns adaptation mechanics; CT supplies content that survives narrow widths, translation, and reflow.
- EP owns rights, consent, manipulation, and risk policy; CT expresses those policies without hiding consequence.

No blocking duplicate authority was found. Controlled validation must use one primary CT rule per content finding and related IDs only for secondary impact.

## Residual work before Stable

- Test comprehension and recovery with representative users.
- Validate translated strings, pluralization, text expansion, bidirectional text, and locale formats.
- Review visible and accessible names with keyboard and screen-reader workflows.
- Verify real data, AI provenance, limitations, and uncertainty disclosures in rendered interfaces.
- Record product-specific terminology decisions and approved exceptions.

## Decision

The standard is structurally complete and internally consistent enough for controlled workflow validation. Audit result: **Pass**.
