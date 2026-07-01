---
type: reference
title: Enrichment Agent
timestamp: 2026-07-01T00:00:00Z
privacy: private
tags: [okf, enrichment, kcenrich, agent]
---

# Enrichment Agent

An agentic workflow that extracts information from external sources to
generate and publish enriched metadata/documentation for data assets, built
on top of the `mdcode`/`kcmd` capability (see [mdcode.md](mdcode.md)).

## Layout

- `toolbox/enrichment/` — enrichment agent toolbox providing the `kcenrich`
  CLI. Subdirs: `src/agent/`, `src/tools/`.
- `samples/enrichment/` — sample application of the enrichment agent, with
  `sample/config/`, `sample/data/`, `sample/docs/`, and `src/enrichment/`,
  `src/tools/`.

## Related

- `samples/discovery/` — a separate search/discovery agent sample built on
  Catalog Search APIs (not part of the enrichment flow, but adjacent in
  `samples/`).
