# Agent Instructions

Read `STATUS.md` first to identify the current phase and next action. Then read `SKILL.md` before creating or reviewing UI/UX work with this repository.

## Editing policy

- Normative standards live in `references/`.
- Operational review steps live in `checklists/`.
- Reusable structures live in `templates/`.
- Do not change a normative rule without explaining the problem, identifying affected rules, updating related checklists, and recording the change in `CHANGELOG.md`.
- Update `STATUS.md` in the same commit whenever a standard changes lifecycle status, an audit or validation completes, roadmap scope changes, or overall progress changes.
- Preserve published rule IDs. Never reuse a deprecated ID for another rule.
- Keep `SKILL.md` concise; move detailed knowledge into topic references.
- Write testable requirements. Avoid ambiguous terms such as “good,” “enough,” “modern,” or “beautiful” without measurable criteria.
- Treat undocumented assumptions as risks.

## Rule format

Every normative rule should include an ID, level, statement, rationale, requirements, validation, exceptions, failure examples, and related rules.
