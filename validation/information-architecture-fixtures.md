# Information Architecture Validation Fixtures

Use these fixtures to regression-test IA rule routing and audit output.

## Fixture A — Dashboard navigation

A department-driven operations dashboard with ambiguous destinations, no active state, lost filters after drill-down, hidden active filters on mobile, and a context-free shared detail link.

Expected primary rules: IA-001, IA-002, IA-003, IA-004, IA-006, IA-007. Expected result: Fail.

## Fixture B — Collection controls

An incident table with misleading search scope, tab-like filters across unrelated dimensions, sorting that changes membership, reset that changes parent scope, generic zero states, and lost return state.

Expected primary rules: IA-005 and IA-006. Expected result: Fail.

## Fixture C — Taxonomy governance

A taxonomy with duplicate terms, an overloaded Other bucket, label-derived identifiers, restricted metadata leakage, and unreviewed AI-generated official categories.

Expected primary rule: IA-008. Expected result: Fail.
