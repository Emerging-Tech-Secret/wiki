---
canonical_subject: "Agentic coding tools"
aliases: ["coding agents", "agentic software development tools", "AI coding agents"]
temperature: 82
rating: { factual: 78, neutrality: 82, layout: 72 }
core_facts:
  - claim: "Agentic coding tools can autonomously plan multi-step code modifications, execute shell commands, read and write files, and iterate on their own outputs"
    sources: [ref_2]
    locked: false
related: ["Claude Code", "AI agent system design", "ReAct (reasoning and acting)"]
last_external_fetch: 2026-06-10T23:32:38-03:00
---

# Agentic coding tools

Liu et al. describe AI-assisted software development as moving from autocomplete-style tools through IDE-integrated assistants toward agentic systems that plan multi-step modifications, execute shell commands, read and write files, and iterate on outputs [ref_2].
The paper presents Claude Code as an example of an agentic coding tool that can call tools, evaluate results, and continue until a task is done [ref_2].

## Architectural requirements

The paper argues that the move from suggestions to autonomous action introduces architectural requirements around safety, context management, extensibility, delegation, and session persistence [ref_2].
The paper frames these requirements as a design space that production coding agents must navigate [ref_2].

## Relation to ReAct

Claude Code's core loop is described as reactive and is explicitly related to the ReAct pattern of model-generated reasoning, tool invocations, environmental feedback, and repeated action [ref_2][ref_1].
The paper says Claude Code chooses a simple reactive loop instead of explicit graph-based routing or tree-search trajectories for the core loop [ref_2].

## Sources

- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) — Liu et al., arXiv:2604.14228v1 (ref_2) [ref_2].
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) — Yao et al., arXiv:2210.03629 (ref_1) [ref_1].
