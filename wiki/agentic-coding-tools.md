---
canonical_subject: "Agentic coding tools"
aliases: ["coding agents", "agentic software development tools", "AI coding agents"]
temperature: 83
rating: { factual: 79, neutrality: 83, layout: 73 }
core_facts:
  - claim: "Agentic coding tools can autonomously plan multi-step code modifications, execute shell commands, read and write files, iterate on their own outputs, and therefore need reliability mechanisms for long-running tool-use loops"
    sources: [ref_2, ref_3]
    locked: false
related: ["Claude Code", "AI agent system design", "ReAct (reasoning and acting)", "Long-term coherence", "Vending-Bench"]
last_external_fetch: 2026-06-11T17:48:33+00:00
---

# Agentic coding tools

Liu et al. describe AI-assisted software development as moving from autocomplete-style tools through IDE-integrated assistants toward agentic systems that plan multi-step modifications, execute shell commands, read and write files, and iterate on outputs [ref_2].
The paper presents Claude Code as an example of an agentic coding tool that can call tools, evaluate results, and continue until a task is done [ref_2].

## Architectural requirements

The paper argues that the move from suggestions to autonomous action introduces architectural requirements around safety, context management, extensibility, delegation, and session persistence [ref_2].
The paper frames these requirements as a design space that production coding agents must navigate [ref_2].
Vending-Bench shows that long-running agent loops can fail through operational misunderstandings, forgotten orders, incorrect tool use, task abandonment, and tangential meltdown loops, which are reliability concerns for any tool-using agent that must maintain state over many steps [ref_3].

## Relation to ReAct

Claude Code's core loop is described as reactive and is explicitly related to the ReAct pattern of model-generated reasoning, tool invocations, environmental feedback, and repeated action [ref_2][ref_1].
The paper says Claude Code chooses a simple reactive loop instead of explicit graph-based routing or tree-search trajectories for the core loop [ref_2].

## Long-running tool use

Vending-Bench uses a basic LLM agent loop with context management, memory tools, task-specific tools, and sub-agent delegation to test long-horizon coherence [ref_3].
Its runs last 2,000 messages and typically consume about 25 million tokens over 5-10 real-world hours, making it a stress test for sustained tool use rather than short benchmark completion [ref_3].
The benchmark's failure analysis suggests that larger context or memory alone may not solve long-run reliability, because breakdowns did not clearly correlate with memory filling and larger GPT-4o mini memory performed worse than smaller memory in the reported variation [ref_3].

## Sources

- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) — Liu et al., arXiv:2604.14228v1 (ref_2) [ref_2].
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) — Yao et al., arXiv:2210.03629 (ref_1) [ref_1].
- [Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents](sources/vending-bench-2502-15840v1.md) — Backlund and Petersson, arXiv:2502.15840v1 (ref_3) [ref_3].
