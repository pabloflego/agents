---
name: jj-commit
description: 'Workflow for generating conventional commit messages for jj (Jujutsu). Guides users to create standardized, descriptive commit messages in line with the Conventional Commits specification using jj commit.'
---

### Workflow

1. Run `jj diff` to inspect current changes.
2. Construct your commit message using the XML structure below.
3. Run:

```bash
jj commit -m "type(scope): description"
```

### Commit Message Structure

```xml
<commit-message>
  <type>feat|fix|docs|style|refactor|perf|test|build|ci|chore|revert</type>
  <scope>(optional)</scope>
  <description>Short imperative summary</description>
  <body>(optional: more detail)</body>
  <footer>(optional: BREAKING CHANGE or issue refs)</footer>
</commit-message>
```

### Examples

```xml
<examples>
  <example>feat(parser): add ability to parse arrays</example>
  <example>fix(ui): correct button alignment</example>
  <example>docs: update README with usage instructions</example>
  <example>chore: update dependencies</example>
  <example>feat!: send email on registration (BREAKING CHANGE: email service required)</example>
</examples>
```

### Validation

- Type must be one of the allowed values
- Description: required, imperative mood ("add", not "added")
- Scope: optional but recommended
- Body/footer: optional, for context and breaking changes
