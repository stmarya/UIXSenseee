# Information Architecture

- **Document ID:** UIXS-IA
- **Version:** 0.1.0
- **Status:** Draft
- **Related standards:** FP, CT, AX, RS, QA

## Purpose

Ensure information, features, and navigation are structured around user needs and mental models so people can find information, understand their location, preserve context, and complete tasks without knowing an organization's internal structure.

## Scope

Applies to navigation, page hierarchy, taxonomy, labeling, search, filter, sort, overview/detail relationships, dashboards, portals, forms, and data-heavy products.

## Out of scope

Detailed visual styling, technical routing implementation, source-code structure, database schemas, and component animation are covered elsewhere unless they directly change information structure.

## Terminology

- **Information Architecture:** structure, grouping, labeling, and relationships that support finding and understanding information.
- **Mental model:** how users expect a system to work.
- **Hierarchy:** importance or parent–child relationships between information.
- **Taxonomy:** classification and naming system.
- **Findability:** ease of locating known information or functions.
- **Discoverability:** ease of noticing that information or a function exists.
- **Wayfinding:** cues that explain current location, possible destinations, and a route back.
- **Progressive disclosure:** showing primary information first and revealing detail when needed.
- **Drill-down:** moving from a summary to more detailed information.
- **Information scent:** cues that help users predict what a destination contains.
- **Canonical location:** the primary structural home of a page or object.

## Core principles

- **IA-P01 User-task oriented:** structure follows user goals and tasks.
- **IA-P02 Predictable:** location and navigation outcomes can be anticipated.
- **IA-P03 Findable:** important information is easy to locate.
- **IA-P04 Context preserving:** movement does not silently discard context.
- **IA-P05 Clear labeling:** labels use language users recognize.
- **IA-P06 Progressive complexity:** complexity is introduced when needed.
- **IA-P07 Multiple paths, consistent meaning:** alternative entry points preserve identity and context.
- **IA-P08 Scalable:** structure remains understandable as content grows.

---

## IA-001 — Organize information around user tasks

**Level:** MUST  
**Status:** Draft  
**Related:** FP-001, FP-002, IA-P01

### Rule

Information and navigation MUST be organized around user goals and tasks rather than the organization's internal structure.

### Rationale

Users arrive to make a decision, find information, or complete a task. They should not need to know which department owns a feature, how a database is structured, or what an internal system is called.

### Requirements

- **IA-001-A — Identify primary users — MUST.** Record the user, primary goal, frequent tasks, critical information, expected terminology, and risk if information cannot be found.
- **IA-001-B — Identify primary tasks — MUST.** Every major area must map to a defined user task.
- **IA-001-C — Group related tasks — SHOULD.** Group tasks that share a goal, sequence, or information context.
- **IA-001-D — Use recognized language — MUST.** Labels must use terms users understand; internal terms require evidence that users recognize them.
- **IA-001-E — Do not expose internal structure by default — MUST NOT.** Department, team, service, or database structure must not define navigation unless that structure is itself the user's work object.
- **IA-001-F — Prioritize by value and frequency — SHOULD.** Consider value, frequency, urgency, risk, and dependency. Rare but critical tasks must remain findable.

### Validation

Use task inventories, card sorting, tree testing, first-click testing, and terminology review. Document assumptions when user evidence is unavailable.

### Exceptions

Organizational structure MAY be used when it is the user's actual domain model, is required by regulation, or evidence shows it is expected. Record the affected users, evidence, risks, mitigation, owner, and review date.

### Failure examples

- Department-driven navigation that requires knowing feature ownership.
- System-driven labels such as “Transaction Processor” for user-facing tasks.
- Catch-all categories such as “Other,” “More,” or “General.”
- Similar labels such as “Analytics,” “Insights,” “Reports,” and “Statistics” without distinct definitions.

### Acceptance

Pass only when primary users and tasks are defined, major areas map to tasks, labels use recognized language, grouping follows user purpose, and exceptions are documented.

---

## IA-002 — Define a clear and predictable hierarchy

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-005, IA-P02, IA-P04, IA-P08

### Rule

Information MUST be arranged in a clear and predictable hierarchy so users can understand relationships, determine their current location, and anticipate where information can be found.

### Rationale

A useful hierarchy answers: Where am I? What contains this page? What choices exist at this level? How do I return or continue? Hierarchy applies to navigation, headings, overview/detail relationships, filters, and drill-down paths.

### Requirements

- **IA-002-A — Define levels — MUST.** Every level must have a distinct purpose. Do not add levels that provide no new context.
- **IA-002-B — Establish parent–child relationships — MUST.** A child must be a logical part, detail, object, or continuation of its parent.
- **IA-002-C — Separate categories, views, objects, and actions — MUST.** Do not place “Export” or “Delete” at the same structural level as destinations.
- **IA-002-D — Keep hierarchy stable — MUST.** Primary navigation must not reorder or change meaning unexpectedly. Personalized shortcuts must remain separate from structural navigation.
- **IA-002-E — Communicate current location — MUST.** Use page titles, active navigation, breadcrumbs, tabs, or context labels. Active state must not rely on color alone.
- **IA-002-F — Preserve drill-down context — MUST.** Preserve or explicitly change filters, period, sorting, search, selection, and scope.
- **IA-002-G — Provide a route back — MUST.** Detail views must provide a clear return to the parent or prior result context.
- **IA-002-H — Balance depth and breadth — SHOULD.** Base depth on domain complexity and evidence, not an arbitrary click limit.
- **IA-002-I — Avoid single-child levels — SHOULD NOT.** Keep them only for meaningful context, permission boundaries, or proven near-term scale.
- **IA-002-J — Avoid overlapping categories — MUST.** Categories at the same level must have distinguishable definitions.
- **IA-002-K — Define a canonical location — SHOULD.** Search, notifications, favorites, and shortcuts should lead to one structurally consistent object identity.
- **IA-002-L — Match heading and content hierarchy — MUST.** Semantic and visual order must reflect information structure.
- **IA-002-M — Support scale — SHOULD.** Test growth, long labels, role differences, localization, and similar item names without adding speculative empty categories.

### Suitable hierarchy models

- **Hub-and-spoke:** overview leading to several major areas.
- **Hierarchical tree:** category, subcategory, and item relationships.
- **Sequential:** ordered steps with review and completion.
- **Faceted:** one collection filtered by multiple dimensions.
- **Matrix:** multiple valid dimensions with a defined canonical location.

### Validation

- Build a hierarchy map with level, parent, child, purpose, task, entry point, exit point, and required context.
- Use tree testing for representative findability tasks.
- Test breadcrumb and active-location cues.
- Apply filters and sorting, open detail, return, and verify context persistence.
- Simulate twice the content, longer labels, and different permission sets.

### Exceptions

Exceptions MAY be accepted for regulated taxonomies, established expert-domain structures, temporary migrations, or permission boundaries. Users must still understand location, relationships, and a route back.

### Failure examples

- Deep nesting without additional meaning.
- Mega-menus without grouping.
- Breadcrumbs that do not represent the real structure.
- Lost filters or period after returning from detail.
- Categories, objects, views, and actions mixed at one level.
- Navigation that reorders itself dynamically.
- Duplicate destinations with different identities.

### Acceptance

Fail when users cannot identify location, parent–child relationships mislead, drill-down silently changes scope, detail lacks a route back, or primary categories cannot be distinguished. Conditional Pass may be used for justified non-blocking SHOULD issues. Otherwise Pass.

## Planned rules

- IA-003 — Use clear, descriptive, and consistent labels.
- IA-004 — Provide effective wayfinding.
- IA-005 — Separate navigation, search, filter, and sort.
- IA-006 — Preserve context across navigation.
- IA-007 — Apply progressive disclosure without hiding critical information.
- IA-008 — Design scalable taxonomies.
