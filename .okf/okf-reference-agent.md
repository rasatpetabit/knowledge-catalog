---
type: reference
title: Open Knowledge Format Reference Agent
timestamp: 2026-07-01T00:00:00Z
privacy: private
tags: [okf, reference-agent, agent, bundles]
---

# Open Knowledge Format Reference Agent

Python-based reference agent at `okf/` (package `okf/src/reference_agent/`)
that produces Open Knowledge Format bundles for sample datasets — GA4,
StackOverflow, and Bitcoin crypto data. Documented in `okf/README.md`.

## Layout

- `okf/src/reference_agent/` — agent source, split into submodules:
  `web`, `viewer`, `bundle`, `tools`, `sources`, `prompts`.
- `okf/bundles/` — prebuilt output bundles per dataset:
  - `okf/bundles/ga4/` (`datasets/`, `tables/`, `references/`)
  - `okf/bundles/stackoverflow/` (`datasets/`, `tables/`, `references/`)
  - `okf/bundles/crypto_bitcoin/` (`datasets/`, `tables/`)
- `okf/samples/` — per-dataset samples: `ga4_merch_store`, `stackoverflow`,
  `crypto_bitcoin`.
- `okf/tests/` — test suite.

Note: this OKF "Open Knowledge Format" (Google's bundle format for catalog
metadata) is distinct from the petabit-sysadmin OKF doc-compiler format used
to author *these* index/reference docs — the acronym collision is
coincidental (see `/srv/dev/petabit/sysadmin/docs/okf/okf-format-v0.1.md`,
"Related, out-of-scope prior art").

## Pointers

- `okf/README.md`
