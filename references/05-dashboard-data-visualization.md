# Dashboard & Data Visualization

- **Document ID:** UIXS-DV
- **Version:** 0.10.0
- **Status:** Draft
- **Owner:** UIXSenseee maintainers
- **Last updated:** 2026-10-01
- **Related standards:** FP, IA, VF, IN, CB, AX, RS, CT, EP, QA

## Purpose

Ensure dashboards and visualizations support correct decisions through relevant metrics, honest encoding, transparent interaction, visible uncertainty, accessible detail, and traceable evidence.

## Ownership

DV owns analytical question, metric meaning, chart selection, encoding, comparison, data quality, and uncertainty. VF owns general visual presentation; AX owns accessibility conformance; CT owns final language; EP owns ethical and manipulative-data policy.

---

## DV-001 — Design dashboards around users and decisions

**Level:** MUST  
**Status:** Draft

### Rule

Dashboards MUST identify audience, decisions, tasks, scope, cadence, and actions before selecting metrics or visual forms.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-001-A — Define primary audience — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-B — Define decisions and actions — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-C — Identify task frequency — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-D — State global scope and period — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-E — Prioritize critical exceptions — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-F — Limit metrics to decision value — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-G — Provide route from overview to evidence — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-001-H — Document success criteria — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-002 — Define metrics and KPIs completely

**Level:** MUST  
**Status:** Draft

### Rule

Every metric MUST define name, purpose, formula, population, unit, period, grain, source, owner, freshness, and interpretation.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-002-A — Define formula and numerator denominator — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-B — Define population and exclusions — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-C — Define unit and precision — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-D — Define time grain and timezone — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-E — Identify source and owner — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-F — Show freshness — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-G — Distinguish target actual estimate — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-002-H — Version metric changes — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-003 — Select charts by analytical question

**Level:** MUST  
**Status:** Draft

### Rule

Visual form MUST match comparison, trend, distribution, relationship, composition, geography, flow, or target question.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-003-A — Use line for ordered trend where suitable — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-B — Use bars for category comparison — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-C — Use distribution forms for spread — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-D — Use scatter for relationships — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-E — Use composition only when meaningful — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-F — Avoid 3D quantitative charts — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-G — Use maps only for spatial questions — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-003-H — Provide table when exact lookup matters — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-004 — Use honest scales, axes, and baselines

**Level:** MUST  
**Status:** Draft

### Rule

Scales, axes, domains, baselines, intervals, and transformations MUST preserve proportional and contextual interpretation.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-004-A — Use zero baseline for bars unless justified — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-B — Disclose truncated domains — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-C — Keep intervals consistent — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-D — Label log and transformed scales — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-E — Avoid misleading dual axes — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-F — Use comparable domains for comparison — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-G — Do not encode quantity by decorative volume — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-004-H — Show reference lines only when meaningful — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-005 — Provide valid comparison and context

**Level:** MUST  
**Status:** Draft

### Rule

Values MUST include appropriate baseline, target, prior period, benchmark, denominator, or distribution context when needed for decisions.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-005-A — Compare equivalent periods and populations — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-B — Name denominator — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-C — Show target and benchmark source — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-D — Distinguish percent and percentage points — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-E — Provide distribution when average hides spread — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-F — Show sample size where material — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-G — Avoid correlation as causation — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-005-H — Explain favorable direction — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-006 — Use labels, legends, and visual encoding consistently

**Level:** MUST  
**Status:** Draft

### Rule

Position, length, area, color, shape, labels, and legends MUST encode data consistently and remain distinguishable.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-006-A — Use stable category encoding — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-B — Limit categorical colors — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-C — Use perceptually ordered quantitative palettes — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-D — Direct-label where practical — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-E — Keep legends near data — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-F — Avoid color-only distinction — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-G — Format numbers consistently — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-006-H — Prevent label overlap and truncation — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-007 — Design filters, selection, and drill-down transparently

**Level:** MUST  
**Status:** Draft

### Rule

Dashboard interactions MUST expose scope, active state, affected visuals, persistence, reset, and resulting analytical context.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-007-A — Show active filters — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-B — Distinguish global and local filters — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-C — Identify affected visuals — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-D — Preserve relevant context — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-E — Make reset predictable — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-F — Show selection and batch scope — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-G — Keep drill-down period and population — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-007-H — Support shareable state when safe — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-008 — Represent missing, stale, partial, and low-quality data honestly

**Level:** MUST  
**Status:** Draft

### Rule

Data availability, freshness, completeness, suppression, sampling, and quality limitations MUST be visible and must not be silently converted.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-008-A — Distinguish missing from zero — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-B — Show freshness and update state — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-C — Label partial and sampled data — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-D — Explain suppressed values — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-E — Expose quality warnings — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-F — Avoid imputation without disclosure — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-G — Handle outliers transparently — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-008-H — Provide recovery for failed data — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-009 — Communicate forecasts, uncertainty, and model output

**Level:** MUST  
**Status:** Draft

### Rule

Predictions, estimates, confidence, scenarios, assumptions, and generated insights MUST be distinguishable from observed facts.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-009-A — Label observed forecast and scenario — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-B — Show uncertainty where material — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-C — State horizon and model freshness — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-D — Expose assumptions and drivers — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-E — Avoid false precision — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-F — Distinguish AI narrative from source data — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-G — Allow verification against evidence — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-009-H — Communicate model limitations — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

---

## DV-010 — Provide accessible detail and prevent misleading presentation

**Level:** MUST  
**Status:** Draft

### Rule

Visualizations MUST provide accessible alternatives, source traceability, and safeguards against deceptive framing or unsupported conclusions.

### Rationale

A visualization can be technically correct yet lead to a wrong decision when scope, encoding, comparison, quality, or uncertainty is incomplete.

### Requirements

- **DV-010-A — Provide title summary and data alternative — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-B — Support keyboard access to interactive data — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-C — Expose units periods and status — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-D — Link source and definition — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-E — Avoid cherry-picked ranges — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-F — Avoid decorative distortion — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-G — Separate insight from recommendation — MUST.** Document and validate this requirement against the decision context and source data.
- **DV-010-H — Require evidence for causal or predictive claims — MUST.** Document and validate this requirement against the decision context and source data.

### Validation

Recompute values from source evidence, verify denominator and scope, test chart interpretation, inspect extreme and missing data, review accessibility, and compare the conclusion against a table or independent calculation.

### Exceptions

A specialized visual form MAY be used when the audience, analytical task, interpretation, and accessible alternative are validated.

### Failure examples

Undefined metrics, incompatible comparison, misleading scale, hidden filters, color-only encoding, missing-as-zero, unlabeled forecast, inaccessible detail, and unsupported causal claims.

### Acceptance

Fail when data meaning, scale, scope, quality, uncertainty, or access could materially mislead. Pass requires all relevant mandatory rules or approved exceptions.

## Dashboard and visualization conformance

Conformance requires DV-001 through DV-010, source-backed numeric verification, relevant Accessibility criteria, and evidence that the visual supports the intended decision without material misinterpretation.

### Required evidence

- audience, task, and decision brief;
- metric dictionary and ownership;
- chart-question mapping;
- numeric reconciliation;
- scale and comparison review;
- filter and drill-down state;
- quality, freshness, missing, and uncertainty treatment;
- accessibility alternative;
- source and claim traceability;
- checklist and exceptions.

## Evidence basis

- [Tableau: Data Visualization Best Practices](https://www.tableau.com/visualization/data-visualization-best-practices)
- [Tableau: How to Spot Misleading Charts](https://www.tableau.com/blog/spot-misleading-charts-checklist)
- [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [Nielsen Norman Group: 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)
