# Information Architecture

- **Document ID:** UIXS-IA
- **Version:** 0.3.0
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

---

## IA-003 — Use clear, descriptive, and consistent labels

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-007, FP-008, IA-P02, IA-P03, IA-P05

### Rule

Labels MUST clearly and consistently communicate the meaning, destination, scope, or result of the element they represent.

### Rationale

Users use labels to predict destinations, actions, affected data, scope, and consequences. Weak labels force users to guess, inspect several destinations, or recover from avoidable mistakes.

### Requirements

- **IA-003-A — Use user language — MUST.** Prefer terms recognized by the intended users. Internal jargon and uncommon acronyms require explanation or evidence of familiarity.
- **IA-003-B — Describe destination or result — MUST.** Navigation labels identify locations; action labels identify actions and affected objects.
- **IA-003-C — Use one term for one concept — MUST.** Do not rotate synonyms for stylistic variety. Maintain a glossary for important domain terms.
- **IA-003-D — Distinguish sibling labels — MUST.** Categories at the same level must have differences users can explain.
- **IA-003-E — Remain understandable out of context — SHOULD.** Labels used in search, notifications, favorites, history, and breadcrumbs should identify their object or area.
- **IA-003-F — Front-load meaningful words — SHOULD.** Put the differentiating words early, especially in scannable lists and narrow layouts.
- **IA-003-G — Be concise but complete — SHOULD.** Do not shorten a label until its object, scope, period, or distinguishing meaning is lost.
- **IA-003-H — Use action-oriented labels — MUST.** Prefer verb + object, such as “Create report” or “Apply filters.”
- **IA-003-I — Name destructive consequences — MUST.** Use “Delete dashboard,” “Archive report,” or “Discard changes,” not “Confirm” or “Proceed.”
- **IA-003-J — Label filter dimension and scope — MUST.** Prefer “All teams,” “Select region,” and “Incident status” over “All,” “Select,” or “Type.”
- **IA-003-K — State units and time context — MUST.** Data labels include units, period, or calculation basis when needed for correct interpretation.
- **IA-003-L — Label ambiguous icons — MUST.** Icon-only controls are acceptable only when meaning is conventional, risk is low, and an accessible name exists.
- **IA-003-M — Match visible and accessible labels — MUST.** The accessible name must contain and align with the visible label.
- **IA-003-N — Support localization — SHOULD.** Avoid wordplay, string fragments, overly narrow containers, and truncation that removes the differentiator.
- **IA-003-O — Use consistent capitalization and grammar — SHOULD.** Capitalization must not be the only hierarchy cue.
- **IA-003-P — Do not mislead — MUST NOT.** The stated destination, action, cost, or result must match the actual behavior.

### Terminology governance

For important terms, record the preferred term, definition, discouraged alternatives, and usage context. Changes must be applied across navigation, content, filters, metrics, statuses, and support material.

### Validation

Use label-comprehension tests, first-click tests, terminology inventories, sibling-differentiation tests, out-of-context tests, and localization stress tests with longer strings and different formats.

### Exceptions

Technical, legal, or regulated terms MAY be retained for expert audiences. Compact icon-only labels MAY be used when evidence shows low ambiguity and accessible naming remains complete. Migration exceptions require a time limit.

### Failure examples

- Generic labels such as “More,” “Other,” “Manage,” or “View.”
- Several names for the same object.
- “Confirm” for a destructive action.
- A “Delete” label that actually archives an item.
- Metrics without units, period, or scope.
- Truncation that hides the distinguishing part of similar labels.

### Acceptance

Fail when labels hide consequences, primary sibling categories cannot be distinguished, visible and accessible names conflict, or the stated result differs from actual behavior. Otherwise, all MUST requirements and documented exceptions determine conformance.

---

## IA-004 — Provide effective wayfinding

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-007, FP-008, FP-009, IA-P02, IA-P04

### Rule

The interface MUST provide sufficient wayfinding cues for users to understand their current location, available destinations, navigation history, and route back to a meaningful context.

### Rationale

Users may enter through navigation, search, notifications, bookmarks, shared links, or browser history. Every important destination must remain understandable without requiring entry through the home page.

### Requirements

- **IA-004-A — Display a clear page title — MUST.** Titles identify the page, object, or task and remain understandable through direct entry.
- **IA-004-B — Indicate active navigation — MUST.** Use more than color alone and communicate current state semantically.
- **IA-004-C — Show current scope — MUST.** Workspace, organization, project, environment, region, dataset, or other risk-relevant scope must be visible and must not change silently.
- **IA-004-D — Use breadcrumbs for hierarchy — SHOULD.** Breadcrumbs represent structural location from general to specific; they do not replace page titles or step indicators.
- **IA-004-E — Provide contextual back navigation — MUST.** Prefer “Return to filtered results” or “Back to team performance” over a generic “Back.”
- **IA-004-F — Distinguish hierarchy from history — MUST.** Breadcrumbs show structure; contextual back links show the prior working context.
- **IA-004-G — Preserve return context — MUST.** Keep relevant filter, sort, search, pagination, date range, tab, selection, and scroll state.
- **IA-004-H — Orient deep-link entry — MUST.** Direct entry shows object identity, parent area, active scope, status, and a route to the parent where relevant.
- **IA-004-I — Communicate level transitions — SHOULD.** Maintain titles, selected objects, filters, or other cues when moving between overview and detail.
- **IA-004-J — Keep navigation placement predictable — MUST.** Structural navigation must not reorder itself dynamically; shortcuts and recent items remain separate.
- **IA-004-K — Distinguish navigation levels — MUST.** Global navigation, local navigation, tabs, breadcrumbs, in-page navigation, related links, and actions must not appear equivalent.
- **IA-004-L — Make destination changes visible — MUST.** Page title, active state, content, focus, loading, or assistive announcement must show that navigation occurred.
- **IA-004-M — Support new-tab and deep-link contexts — SHOULD.** Stable destinations retain identity, scope, and permission feedback outside the originating tab.
- **IA-004-N — Orient long pages — SHOULD.** Use headings, table of contents, in-page navigation, or progress cues without allowing sticky elements to obscure content.
- **IA-004-O — Adapt for small screens — MUST.** Preserve page title, parent context, critical scope, active state, and a route back even when full breadcrumbs are collapsed.
- **IA-004-P — Make wayfinding accessible — MUST.** Navigation regions need distinguishable names; current page, current step, focus order, breadcrumbs, and dynamic changes must be available to assistive technology.

### Pattern selection

- Global navigation: product-level areas.
- Local navigation: destinations within one area.
- Breadcrumb: structural hierarchy.
- Tabs: peer views of the same object or context.
- Step indicator: ordered process.
- Master–detail: list and selected detail in shared context.
- Contextual back link: return to a prior filtered or searched working state.

### Validation

Run direct-entry, location-identification, return-path, multi-entry, permission, responsive, keyboard, and screen-reader tests. A user should be able to identify the page, parent, scope, next destinations, and route back.

### Exceptions

Single-page products, short linear flows, security constraints, embedded contexts, or narrow screens MAY simplify wayfinding, but users must still recognize the page, critical scope, and route out or back.

### Failure examples

- No active navigation state or a color-only state.
- Breadcrumbs used as visit history.
- Generic “Back” links that discard filters.
- Hidden workspace or environment scope.
- Navigation items that move dynamically.
- Deep-linked pages without titles or parent context.
- Mobile layouts that remove all location cues.

### Acceptance

Fail when users cannot identify page or scope, no route back exists, drill-down silently discards context, direct links lack orientation, or users can act on the wrong workspace. Otherwise, all MUST requirements and documented exceptions determine conformance.

---

## IA-005 — Separate navigation, search, filter, and sort

**Level:** MUST  
**Status:** Draft  
**Related:** FP-002, FP-007, FP-008, IA-P02, IA-P03, IA-P04

### Rule

Navigation, search, filter, and sort MUST have distinct purposes, labels, states, and outcomes so users can predict whether an interaction changes location, finds items, narrows a collection, or changes order.

### Functional definitions

- **Navigation** changes location or information context.
- **Search** retrieves items that match a query.
- **Filter** narrows a known collection by attributes.
- **Sort** changes the order of the same collection.

### Requirements

- **IA-005-A — Navigation changes location — MUST.** Navigation items represent destinations, not commands or filter values.
- **IA-005-B — Search matches a query — MUST.** Search identifies its scope and returns matching items without silently changing unrelated filters.
- **IA-005-C — Filter narrows a collection — MUST.** Filters operate on clearly defined dimensions and do not silently navigate to a different information area.
- **IA-005-D — Sort changes order only — MUST.** Sorting must not add or remove records, change the metric definition, or alter scope.
- **IA-005-E — Distinguish controls — MUST.** Labels, placement, states, and visual treatment must make navigation, search, filter, and sort distinguishable.
- **IA-005-F — Communicate scope — MUST.** Users must know whether search or filtering applies globally, to the current page, table, chart, workspace, or dataset.
- **IA-005-G — Show active state — MUST.** Display the query, active filters, result count where useful, and current sort. Active filters must be individually removable.
- **IA-005-H — Provide reset behavior — MUST.** Users must be able to clear query and filters predictably. Reset must not remove unrelated preferences or change scope without notice.
- **IA-005-I — Preserve state appropriately — SHOULD.** Keep relevant query, filters, and sort through detail views, refresh, pagination, and return navigation.
- **IA-005-J — Explain zero results — MUST.** Distinguish an empty dataset, no query matches, no filter matches, loading failure, and permission limits. Offer a relevant recovery action.
- **IA-005-K — Separate commands — MUST.** Actions such as Export, Create, Delete, and Refresh are commands and must not be disguised as navigation, filters, or sort options.
- **IA-005-L — Support shareable analytical state — SHOULD.** Important dashboard or analysis states should be reproducible through a stable link, saved view, or explicit state summary when privacy permits.
- **IA-005-M — Avoid ambiguous combined controls — SHOULD NOT.** A single control should not mix navigation, command execution, search, and filtering unless modes and outcomes are explicit.
- **IA-005-N — Make controls accessible — MUST.** Controls require persistent labels, keyboard operation, announced active states, and a logical focus order. Placeholder text is not a sufficient label.

### Search policy

Search MUST state or imply its scope, support clear submission behavior, preserve the query on results, and distinguish suggestions from final results. Global and local search must not appear identical when their scopes differ. Search results should expose enough context to distinguish similar items.

### Filter policy

Filter labels identify dimensions; options identify values. Global and local filters must be visually and semantically distinguishable. Applied filters must remain visible, and dependent filters must disclose when one choice limits another. Missing values must not be silently treated as zero or “Other.”

### Sort policy

Sort options identify both field and direction when ambiguity exists, such as “Updated: newest first” or “Backlog: highest first.” Default order should be meaningful and documented for critical lists. Sorting a paginated collection must apply to the whole result set, not only the visible page.

### Validation

Test each control by asking users to predict its outcome before activation. Verify scope, active-state visibility, reset behavior, zero-result recovery, detail-and-return persistence, keyboard operation, and consistency across responsive layouts. Compare record membership before and after sorting to confirm that only order changed.

### Exceptions

Command palettes and unified search MAY combine navigation and actions when result types are clearly labeled and outcomes are previewed. Compact layouts MAY collapse filters into a drawer, but active filters and scope must remain visible outside it.

### Failure examples

- A navigation tab used to filter a table without communicating the behavior.
- Search that silently searches only the visible page.
- Sort that changes metric definition or record membership.
- A generic “All” option with unclear scope.
- Active filters hidden inside a closed drawer.
- Reset that also clears date range, workspace, or user preferences unexpectedly.
- “No data” used for query mismatch, permission denial, and server failure alike.

### Acceptance

Fail when control purpose or scope is ambiguous, sorting changes membership, active filtering is hidden, zero states misrepresent the cause, or reset causes undisclosed data-context changes. Otherwise, all MUST requirements and documented exceptions determine conformance.

## Planned rules

- IA-006 — Preserve context across navigation.
- IA-007 — Apply progressive disclosure without hiding critical information.
- IA-008 — Design scalable taxonomies.
