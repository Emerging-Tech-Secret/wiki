# Operation log

Append-only, chronological op-log (AGENTS.md §6). Keep the `## [YYYY-MM-DD] <op> | …` prefix so it
stays grep-parseable: `grep "^## \[" log.md | tail`.

## [2026-06-09] bootstrap | wiki initialized
Seeded `index.md`, `log.md`, and `source_registry.yaml`. No pages yet — awaiting the first ingest.

## [2026-06-10] ingest | "ReAct" (ref_1) [reproduction on fresh-booted instance]
Fetched+snapshotted arxiv.org/abs/2210.03629. Pages: wiki/react.md, wiki/sources/react-2210-03629.md.

## [2026-06-10] ingest | "Dive into Claude Code" (ref_2)
Fetched+snapshotted arxiv.org/html/2604.14228v1. Pages: wiki/sources/dive-into-claude-code-2604-14228v1.md, wiki/claude-code.md, wiki/openclaw.md, wiki/ai-agent-system-design.md, wiki/agentic-coding-tools.md.

## [2026-06-11] ingest | "Vending-Bench" (ref_3)
Fetched+snapshotted arxiv.org/html/2502.15840v1. Pages: wiki/sources/vending-bench-2502-15840v1.md, wiki/vending-bench.md, wiki/long-term-coherence.md, wiki/ai-agent-system-design.md, wiki/agentic-coding-tools.md.
