# Content Design & Microcopy Validation Fixtures

Use these fixtures to regression-test rule routing, severity, remediation, and duplicate handling. Each seeded issue has one primary rule.

## Fixture A — Account setup language

1. Page title is “Provision Identity Artifact.” — CT-001
2. Primary action is “Proceed.” — CT-002
3. Email format exists only in placeholder text. — CT-003
4. Invalid input says “You entered it wrong.” with no correction. — CT-004
5. Loading, no-results, and service-failure states all say “No data.” — CT-005
6. Account deletion confirmation uses “Yes / No” and omits consequence. — CT-006

## Fixture B — Analytics dashboard content

7. The same measure is called “Revenue,” “Sales,” and “Value” without definitions. — CT-007
8. A date is shown as `03/04/26`; money has no currency; timestamps have no zone. — CT-008
9. Sentences are assembled from fragments that cannot support plural or reordered translations. — CT-009
10. Forecast output is presented as fact without source, method, limitation, or uncertainty. — CT-010

## Fixture C — Recovery and notification content

11. A payment failure exposes an internal error code as the main explanation. — CT-004
12. A critical completion message appears only in an auto-dismissing toast. — CT-005
13. “Save” silently starts a paid subscription. — CT-002
14. Refusal is described as “Lose all benefits,” while acceptance is “Continue safely.” — CT-006, with EP as related policy ownership
15. A filter label is visually “Status” but its accessible name is “Category.” — CT-002, with AX as related conformance ownership
16. A percentage lacks its denominator and comparison period. — CT-008, with DV as related data ownership

## Expected regression results

- Every seeded issue is detected.
- CT-001 through CT-010 are each selected at least once as a primary rule.
- Related IA, IN, CB, DV, AX, RS, or EP IDs never replace the primary CT owner for wording defects.
- Critical or Major content failures cannot produce Pass.
- No issue is counted twice merely because it has secondary cross-standard effects.
