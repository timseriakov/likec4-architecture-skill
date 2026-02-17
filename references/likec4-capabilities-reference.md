# LikeC4 Capabilities Reference

This file is a practical capability map for agents. It is intentionally not a full duplicated language spec.
For complete and current semantics, always use official docs.

## Why this file exists

- Fast discovery of available LikeC4 features
- Stable checklist for agent authoring
- Pointer map to canonical documentation

## Capability map

- Project and syntax basics
  - source file extensions and top-level blocks
  - docs: https://likec4.dev/dsl/intro/

- Notation and kinds
  - custom element kinds, relationship kinds, tags
  - docs: https://likec4.dev/dsl/specification/

- Relationships
  - directed relationships, nested relationships, styling
  - docs: https://likec4.dev/dsl/relationships/

- Views
  - named/unnamed views, default `index`, include/exclude, predicates
  - docs: https://likec4.dev/dsl/views/
  - predicates details: https://likec4.dev/dsl/views/predicates/

- Styling and notation
  - element/relationship style overrides, legends/notations
  - docs: https://likec4.dev/dsl/styling/
  - docs: https://likec4.dev/dsl/notations/

- Dynamic views
  - use-case/scenario focused interaction views
  - docs: https://likec4.dev/dsl/dynamic-views/

- Deployment modeling and deployment views
  - environments, zones, instances, deployment predicates
  - docs: https://likec4.dev/dsl/deployment/views/

- CLI and tooling
  - validate/start/build/export workflows
  - docs: https://likec4.dev/

- MCP server support
  - exposing model knowledge to LLMs
  - docs: https://likec4.dev/tooling/mcp/

## Agent decision rule

When a requested feature is not clearly covered by quickstart/pattern files:

1. Open this map.
2. Jump to the official section.
3. Apply the documented syntax.
4. Re-run `npx likec4 validate`.
