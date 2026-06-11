---
canonical_subject: "Long-term coherence"
aliases: ["long-horizon coherence", "long-term agent coherence", "long-horizon agent reliability", "sustained coherent decision-making"]
temperature: 78
rating: { factual: 82, neutrality: 86, layout: 74 }
core_facts:
  - claim: "Long-term coherence is the ability of LLM agents to carry out tasks over long time horizons"
    sources: [ref_3]
    locked: false
related: ["Vending-Bench", "AI agent system design", "Agentic coding tools"]
last_external_fetch: 2026-06-11T17:48:33+00:00
---

# Long-term coherence

Long-term coherence is the ability of LLMs or LLM-based agents to do tasks over long time horizons [ref_3].
Backlund and Petersson motivate Vending-Bench by arguing that short-term task proficiency does not guarantee coherent performance over long-running, multi-step operations [ref_3].

## Why it is hard to evaluate

Vending-Bench isolates long-term coherence by using a task whose subtasks are individually simple but whose full run stresses sustained decision-making over more than 20 million tokens per run [ref_3].
The benchmark's vending-machine task requires the agent to remember supplier interactions, track delivery timing, maintain inventory, set prices, collect cash, and pay daily fees over many simulated days [ref_3].
The paper reports that models can perform well in some runs while failing or stagnating in others, so variance across repeated long runs is itself an important evaluation signal [ref_3].

## Failure patterns

The Vending-Bench experiments show long-term coherence failures such as misinterpreting delivery status, forgetting orders, failing to notice orders, confusing operational status, abandoning the task, and entering tangential meltdown loops [ref_3].
The authors emphasize that many failures were recoverable by a human, such as waiting for fulfillment confirmation or checking inventory later, but models often failed to recover after an operational misunderstanding [ref_3].

## Relation to context and memory

The paper found no clear evidence that Vending-Bench breakdowns were solely caused by context-window filling [ref_3].
Across reported models, the Pearson correlation between days until sales stop and days until memory full was 0.167 [ref_3].
In GPT-4o mini experiments, larger token memory did not improve performance and performed worse than smaller memory, showing that more context or memory is not automatically better for long-horizon coherence [ref_3].

## Sources

- [Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents](sources/vending-bench-2502-15840v1.md) — Backlund and Petersson, arXiv:2502.15840v1 (ref_3) [ref_3].
