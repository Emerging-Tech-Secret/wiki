# Operation log

Append-only, chronological op-log (AGENTS.md §6). Keep the `## [YYYY-MM-DD] <op> | …` prefix so it
stays grep-parseable: `grep "^## \[" log.md | tail`.

## [2026-06-09] bootstrap | wiki initialized
Seeded `index.md`, `log.md`, and `source_registry.yaml`. No pages yet — awaiting the first ingest.

## [2026-06-10] ingest | "ReAct: Synergizing Reasoning and Acting in Language Models" (ref_1)
Fetched + snapshotted arxiv.org/abs/2210.03629 -> raw/arxiv_2210_03629.md. New pages: wiki/react.md, wiki/sources/react-2210-03629.md. Updated index.md, source_registry.yaml.
