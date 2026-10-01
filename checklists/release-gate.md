# Release Gate

## Result levels

- **Pass:** all relevant MUST and MUST NOT rules are satisfied.
- **Conditional Pass:** no Critical or Major issue remains; documented SHOULD issues have owners and plans.
- **Fail:** any Critical issue, unresolved Major issue, violated mandatory accessibility requirement, misleading data, dark pattern, blocked primary task, or undocumented high-risk exception remains.

## Required checks

- [ ] Scope and target users are defined.
- [ ] Primary tasks can be completed.
- [ ] Relevant standards and rule IDs were reviewed.
- [ ] Accessibility was evaluated manually where required.
- [ ] Loading, empty, error, success, and permission states were considered.
- [ ] Responsive behavior was checked.
- [ ] Data meaning, units, periods, and comparison context are honest.
- [ ] Destructive actions have proportional protection.
- [ ] Exceptions include evidence, risk, mitigation, owner, and review date.
- [ ] No Critical or unresolved Major issue remains.
