---
project: My Wiki
domain: business
created: 2026-04-12
---

# Wiki Configuration

## Project Info

- **Name**: My Wiki
- **Domain**: business
- **Description**: [Add description here]
- **Created**: 2026-04-12

## Entity Types

```yaml
entities:
  types:
    - person
    - organization
    - product
    - technology
    - event
  
  required_attributes:
    person: [role, affiliation, expertise]
    organization: [industry, size, location]
    product: [category, company, status]
    technology: [category, maturity, adopters]
    event: [date, type, significance]
```

## Concept Categories

```yaml
concepts:
  categories:
    - theory
    - method
    - framework
    - metric
    - principle
```

## Workflow Configuration

```yaml
workflow:
  default_mode: interactive
  interactive_keywords:
    - important
    - key
    - critical
    - strategic
  batch_threshold: 3
  auto_save_queries: false
  ask_before_save: true
  confirm_new_pages: true
```

## Lint Rules

```yaml
lint:
  check_frequency: weekly
  rules:
    - check_contradictions
    - check_orphans
    - check_stale_claims
    - check_missing_pages
    - check_incomplete_metadata
    - check_data_gaps
```

## Output Preferences

```yaml
output:
  default_format: markdown
  enable_marp: true
  enable_charts: true
  include_citations: true
```

## Tag Taxonomy

```yaml
tags:
  priority:
    - p1-critical
    - p2-important
    - p3-normal
    - p4-low
  
  status:
    - draft
    - reviewed
    - verified
    - deprecated
```

## Integration Settings

```yaml
integrations:
  qmd:
    enabled: false
    index_path: .qmd-index
    rerank_by_default: true
  
  obsidian:
    dataview: true
    graph_view: true
    canvas: true
    templates: true
```

## Custom Instructions

```
[Add domain-specific instructions here]

Examples:
- Always include quantified metrics when available
- Prefer primary sources over secondary
- Flag speculation explicitly
- Use consistent date format: YYYY-MM-DD
```

---
*Configuration version: 1.0*
