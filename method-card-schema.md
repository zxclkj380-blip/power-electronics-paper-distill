# Method-card schema

Every method card is a Markdown file with YAML front matter:

```yaml
---
name: kebab-case-name
status: accepted | needs-review
method_type: concise category
source: citation with PDF pages and artifacts
---
```

It must contain exactly these sections:

```markdown
## Intent
## Trigger conditions
## Inputs and outputs
## Assumptions
## Procedure
## Verification
## Failure boundaries
## Evidence and uncertainty
```

Set `accepted` only when the card gives a complete reusable procedure with explicit validation. Use `needs-review` when signs, stability, implementation, data quality, or transferability remain unresolved.
