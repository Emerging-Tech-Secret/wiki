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
- [Vending-Bench](vending-bench.md) - benchmark for long-term coherence in LLM agents running a simulated vending machine business - 1 source - updated 2026-06-11

## Concepts
- [ReAct (reasoning and acting)](react.md) - interleaving reasoning traces and actions in LLMs - 1 source - updated 2026-06-10
- [Agentic coding tools](agentic-coding-tools.md) - coding agents that plan, edit, run shell commands, and iterate on long-running tool results - 3 sources - updated 2026-06-11
- [AI agent system design](ai-agent-system-design.md) - recurring design choices for agent loops, permissions, context, extensibility, delegation, persistence, and long-horizon reliability - 2 sources - updated 2026-06-11
- [Long-term coherence](long-term-coherence.md) - ability of LLM agents to sustain coherent task performance over long horizons - 1 source - updated 2026-06-11

## Sources
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) - Yao et al., arXiv:2210.03629 (ref_1)
- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) - Liu et al., arXiv:2604.14228v1 (ref_2)
- [Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents](sources/vending-bench-2502-15840v1.md) - Backlund and Petersson, arXiv:2502.15840v1 (ref_3)

## Syntheses
_None yet._
