---
type: index
resource: /srv/dev/okf-workspace/repos/knowledge-catalog.md
title: knowledge-catalog repo index
timestamp: 2026-07-01T00:00:00Z
privacy: private
tags: [okf, index, knowledge-catalog, gcp, dataplex]
---

# knowledge-catalog repo index

`GoogleCloudPlatform/knowledge-catalog` (vendored under `/srv/dev/knowledge-catalog`)
is a reference/demo repository for **Knowledge Catalog** (formerly Dataplex),
Google Cloud's AI-powered data catalog and metadata management platform. It
demonstrates reference agents, CLI/MCP tooling, and samples for building
context management, metadata enrichment, and retrieval solutions on top of
Knowledge Catalog. It is explicitly **not an official Google product** (see
`README.md` disclaimer). Apache 2.0 licensed.

A repo-local `AGENTS.md` exists at the repository root; no `CLAUDE.md` exists.
These OKF docs use the default `.okf/` placement.

## Tech stack

- Python (`pyproject.toml`, `google-adk`, `google-cloud-bigquery`, `pydantic`, `pyyaml`)
- TypeScript (`toolbox/mdcode/src/libts`)
- Google ADK (Agent Development Kit)
- BigQuery
- YAML/Markdown metadata artifacts
- MCP server, CLI tools (`kcmd`, `kcagent`)

## Key components

- `okf/` — Open Knowledge Format reference agent, bundles, and samples.
  `okf/src/reference_agent/` contains submodules for `web`, `viewer`,
  `bundle`, `tools`, `sources`, `prompts`.
- `okf/bundles/` — prebuilt OKF bundles for `stackoverflow`, `crypto_bitcoin`,
  and `ga4` datasets (each with `datasets/`, `tables/`, and some with
  `references/` subdirs).
- `samples/discovery/` — search/discovery agent sample built on Catalog
  Search APIs.
- `samples/enrichment/` — agentic enrichment sample that generates and
  publishes documentation for data assets.
- `toolbox/mdcode/` — "Metadata as Code" TypeScript library, the
  `kcmd` CLI, and an MCP server for treating metadata artifacts as
  YAML/Markdown source code.
- `toolbox/enrichment/` — enrichment agent toolbox providing the `kcagent`
  CLI, depends on `toolbox/mdcode`.
- `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `LICENSE.md` — standard OSS
  governance files.

## Major subsystems

See per-subsystem OKF reference docs in this directory:

- [okf-reference-agent.md](okf-reference-agent.md) — Open Knowledge Format
  Reference Agent (`okf/`)
- [mdcode.md](mdcode.md) — Metadata as Code toolbox (`toolbox/mdcode/`)
- [enrichment-agent.md](enrichment-agent.md) — Enrichment Agent
  (`toolbox/enrichment/`, `samples/enrichment/`)

## Pointers

- `README.md` — repo overview, Cloud Shell quickstart link, licensing.
- `okf/README.md` — reference-agent-specific README.
- `CONTRIBUTING.md` — contribution instructions.
