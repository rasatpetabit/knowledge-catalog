---
type: reference
title: mdcode - Metadata as Code toolbox
timestamp: 2026-07-01T00:00:00Z
privacy: private
tags: [okf, mdcode, kcmd, mcp, metadata]
---

# mdcode — Metadata as Code toolbox

`toolbox/mdcode/` defines a source-code-artifact model for Knowledge Catalog
metadata: YAML/Markdown files in a hierarchical directory layout mirroring
the resource hierarchy, with bi-directional sync to the catalog service.
Distributed as a TypeScript library, a `kcmd` CLI, and an MCP server.

## Layout

- `toolbox/mdcode/src/libts/` — TypeScript library.
- `toolbox/mdcode/src/tool/` — `kcmd` CLI / MCP server implementation.
- `toolbox/mdcode/tests/libts/` and `toolbox/mdcode/tests/scenarios/` — test
  suites.
- `toolbox/mdcode/demo/` — demo content, including `bq/`, `kb/`, and `okf/`
  subdirectories.
- `toolbox/mdcode/docs/` — additional documentation.

## Relationship to other subsystems

`toolbox/enrichment/` (the Enrichment Agent) depends on `mdcode`/`kcmd` for
reading and writing metadata artifacts.
