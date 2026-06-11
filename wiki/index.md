# Content Cruncher Wiki

A self-evolving, citation-grounded knowledge base maintained by a [Hermes](https://github.com/NousResearch/hermes-agent)
agent. Every claim cites an **external** source; the agent writes and maintains all pages (see the
`AGENTS.md` operating manual in the repo root).

!!! note "Content catalog — read first on every query"
    This page is the catalog of all wiki content (AGENTS.md §6). It is empty at bootstrap; the agent
    populates each section on its first ingest, one line per page (link · one-line summary · # sources · updated).

## Entities
- [Claude Code](claude-code.md) - Anthropic agentic coding tool architecture as analyzed from public TypeScript source - 1 source - updated 2026-06-10
- [OpenClaw](openclaw.md) - multi-channel personal assistant gateway compared with Claude Code - 1 source - updated 2026-06-10

## Concepts
- [ReAct (reasoning and acting)](react.md) - interleaving reasoning traces and actions in LLMs - 1 source - updated 2026-06-10
- [Agentic coding tools](agentic-coding-tools.md) - coding agents that plan, edit, run shell commands, and iterate on results - 2 sources - updated 2026-06-10
- [AI agent system design](ai-agent-system-design.md) - recurring design choices for agent loops, permissions, context, extensibility, delegation, and persistence - 1 source - updated 2026-06-10

## Sources
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) - Yao et al., arXiv:2210.03629 (ref_1)
- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) - Liu et al., arXiv:2604.14228v1 (ref_2)

## Syntheses
_None yet._
