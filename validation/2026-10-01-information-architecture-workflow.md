# Information Architecture Workflow Validation — 2026-10-01

- **Validation ID:** UIXS-VAL-IA-001
- **Standard version:** 0.7.0
- **Previous status:** Draft
- **Decision:** Promote to Candidate
- **Method:** Controlled tabletop validation using three representative interface scenarios

## Objectives

Validate whether the skill can:

1. select relevant rules without reviewing every IA requirement indiscriminately;
2. classify severity consistently;
3. avoid duplicate findings across overlapping rules;
4. recommend actionable corrections;
5. produce a correct Pass, Conditional Pass, or Fail decision;
6. trace every finding to a rule ID and evidence.

## Output contract used

Each finding contains:

- finding ID and severity;
- observed evidence;
- primary rule ID;
- related rule IDs when applicable;
- user impact;
- recommended correction;
- verification method.

One user problem is recorded once under the owning rule. Related rules do not create duplicate findings.

---

## Scenario 1 — Operations dashboard navigation and drill-down

### Fixture

An operations dashboard uses top-level navigation named “Ops Team,” “Data Team,” “Analytics,” “Insights,” “Reports,” and “Export.” No active navigation state is shown. A user filters to Region = Bengkulu and Q3 2026, opens a team detail page, then returns to an unfiltered current-month overview. Active filters are visible only inside a closed mobile drawer. A shared detail link shows “Details” without workspace or parent context.

### Expected routing

IA-001, IA-002, IA-003, IA-004, IA-006, IA-007.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| S1-01 | Major | IA-001 | IA-003 | Navigation reflects team ownership. Replace with user-task areas validated through task inventory and tree testing. |
| S1-02 | Major | IA-003 | IA-002 | Analytics, Insights, and Reports are not distinguishable. Define category boundaries or consolidate them. |
| S1-03 | Major | IA-002 | IA-005 | Export is an action mixed with destinations. Move it into a contextual command area. |
| S1-04 | Major | IA-004 | IA-003 | No active state and deep-linked “Details” lacks parent and workspace context. Add a descriptive title, active parent, scope, and route back. |
| S1-05 | Major | IA-006 | IA-004 | Date and region are lost after return. Restore list state and show restored filters. This is one finding, not two. |
| S1-06 | Major | IA-007 | IA-005 | Active mobile filters are hidden. Show active-filter summary and removable chips outside the drawer. |

### Decision

**Fail.** Six Major findings affect findability, orientation, and analytical meaning.

### Result

Expected rule families selected: 6/6. Duplicate context-loss finding successfully consolidated under IA-006.

---

## Scenario 2 — Incident search, filter, sort, and state

### Fixture

A table labeled “All incidents” searches only the current visible page. Tabs named Open, Critical, and My Team behave as filters. “Sort by priority” also excludes records below a hidden threshold. Reset filters silently changes the workspace and date range. Every zero state says “No data.” Returning from incident detail resets query, sort, and pagination.

### Expected routing

IA-005 and IA-006, with IA-004 as a related rule for the return path.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| S2-01 | Major | IA-005 | IA-003 | Search scope is misleading. Label the actual scope or search the complete incident collection. |
| S2-02 | Major | IA-005 | IA-002 | Tabs mix status, severity, and ownership dimensions. Replace with explicit filters or distinct views with defined scope. |
| S2-03 | Critical | IA-005 | — | Sorting changes membership through a hidden threshold. Separate filtering from sorting and disclose the threshold. |
| S2-04 | Critical | IA-006 | IA-005 | Reset changes workspace and period silently. Restrict reset to filters and require explicit scope changes. |
| S2-05 | Major | IA-005 | — | Empty, no-result, permission, and failure states are indistinguishable. Provide cause-specific recovery states. |
| S2-06 | Major | IA-006 | IA-004 | Returning discards query, sort, and pagination. Restore the prior working state and meaningful focus. |

### Decision

**Fail.** Critical issues can produce incorrect interpretation and actions in the wrong scope.

### Result

Expected primary rule families selected: 2/2. IA-004 used only as a related rule, preventing duplicate reporting.

---

## Scenario 3 — Operational taxonomy governance

### Fixture

A taxonomy contains Customer Support, Support, CS, and Customer Success without definitions. “Other” contains 43% of records. Category IDs are generated from labels, so renaming changes historical trend grouping. Restricted categories appear in filter counts for unauthorized users. An AI clustering job creates new official categories automatically without review.

### Expected routing

IA-008, with IA-003 and IA-005 as related rules.

### Findings

| ID | Severity | Primary rule | Related | Finding and correction |
|---|---|---|---|---|
| S3-01 | Major | IA-008 | IA-003 | Duplicate and near-duplicate categories lack controlled vocabulary. Define preferred terms, synonyms, boundaries, and canonical IDs. |
| S3-02 | Major | IA-008 | — | Label-derived IDs break history after rename. Introduce stable canonical identifiers and migrate saved state. |
| S3-03 | Major | IA-008 | — | “Other” is the largest category. Review contained records and create evidence-based categories with an owner and threshold. |
| S3-04 | Critical | IA-008 | IA-005 | Restricted labels and counts leak through filters. Permission-filter taxonomy metadata before presentation. |
| S3-05 | Major | IA-008 | — | Generated clusters become authoritative automatically. Mark them generated and require accountable review before promotion. |

### Decision

**Fail.** Permission leakage and unstable category identity block conformance.

### Result

Expected primary rule family selected: 1/1. Related terminology and filter concerns were linked without duplicating the taxonomy findings.

---

## Aggregate results

| Metric | Result | Target |
|---|---:|---:|
| Expected scenario-rule routes selected | 9/9 | 100% |
| Expected conformance decisions matched | 3/3 | 100% |
| Findings with rule ID | 17/17 | 100% |
| Findings with actionable correction | 17/17 | 100% |
| Known overlap cases deduplicated | 3/3 | 100% |
| Unexpected primary rule families | 0 | 0 |
| Critical issues incorrectly allowed to pass | 0 | 0 |

## Observations

### Strengths

- Rule ownership boundaries prevented duplicate reporting.
- IA-005 and IA-006 clearly separated control behavior from state persistence.
- IA-008 covered taxonomy identity, permissions, governance, and generated categories.
- The output format remained traceable and actionable.

### Limitations

- Tests used written fixtures rather than rendered interfaces.
- No representative user participated.
- Localization, assistive technology, and extremely large taxonomies were not exercised end to end.
- Acceptance wording still needs editorial normalization before Stable status.

## Candidate decision

Promote `references/01-information-architecture.md` from **Draft** to **Candidate**. Before Stable status, complete at least:

1. one audit of a rendered dashboard;
2. one keyboard and screen-reader wayfinding review;
3. one tree test or equivalent findability study with representative users;
4. one localization stress test;
5. editorial normalization of every Acceptance section.
