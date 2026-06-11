---
canonical_subject: "AI agent system design"
aliases: ["agent architecture design", "AI agent architecture", "agent system architecture"]
temperature: 84
rating: { factual: 80, neutrality: 83, layout: 77 }
core_facts:
  - claim: "AI agent system design includes recurring choices about reasoning loops, permission boundaries, context management, extensibility, delegation, persistence, and long-horizon reliability"
    sources: [ref_2, ref_3]
    locked: false
related: ["Claude Code", "OpenClaw", "Agentic coding tools", "ReAct (reasoning and acting)", "Vending-Bench", "Long-term coherence"]
last_external_fetch: 2026-06-11T17:48:33+00:00
---

# AI agent system design

Liu et al. define a design space for coding agents around recurring questions about where reasoning lives, how iteration loops are structured, what safety posture to adopt, how extension surfaces are partitioned, how context is managed, how work is delegated across subagents, and how sessions persist [ref_2].
The paper uses Claude Code and OpenClaw to show that the same design questions can produce different architectural answers under different deployment contexts [ref_2].
Backlund and Petersson add a benchmark-oriented view of agent system design by testing whether a basic LLM agent loop can sustain coherent business operations across long runs in Vending-Bench [ref_3].

## Design principles from Claude Code

The paper identifies thirteen principles for production coding agents: deny-first with human escalation, graduated trust spectrum, defense in depth, externalized programmable policy, context as a scarce resource with progressive management, append-only durable state, minimal scaffolding with maximal operational harness, values over rules, composable multi-mechanism extensibility, reversibility-weighted risk assessment, transparent file-based configuration and memory, isolated subagent boundaries, and graceful recovery and resilience [ref_2].
These principles are traced to Claude Code implementation choices in permissioning, context management, extensibility, session persistence, and subagent isolation [ref_2].

## Architectural trade-offs

The paper contrasts per-action safety evaluation with perimeter-level access control as alternative safety architectures for agent systems [ref_2].
The paper contrasts a single CLI-centered loop with an embedded runtime inside a gateway control plane as alternative runtime architectures [ref_2].
The paper contrasts context-window extension mechanisms with gateway-wide capability registration as alternative extension and capability-management architectures [ref_2].

## Long-horizon coherence and reliability

Vending-Bench evaluates long-term coherence by having an LLM-based agent run a simulated vending machine business over long horizons [ref_3].
The benchmark requires agents to handle inventory, ordering, pricing, cash collection, daily fees, and supplier and customer interactions [ref_3].
Its agent loop combines context management, memory tools for scratchpad, key-value, and vector-database storage, task-specific tools, and sub-agent delegation [ref_3].
The default Vending-Bench protocol runs 2,000 messages per run, consumes about 25 million tokens in most runs, takes 5-10 real-world hours, and repeats each model or configuration five times [ref_3].
The benchmark results showed high run-to-run variance across all models, including top models that sometimes failed, stagnated, or went bankrupt [ref_3].
Observed failure modes included misinterpreting delivery status, forgetting or failing to notice orders, confusing operational status, abandoning the task, and entering tangential meltdown loops [ref_3].
The paper found no clear evidence that failures were solely explained by context-window filling, reporting a Pearson correlation of 0.167 between days until sales stop and days until memory full [ref_3].
GPT-4o mini memory-variation experiments found that larger token memory performed worse than smaller memory, showing that simply expanding context or memory is not necessarily a reliability fix [ref_3].

## Open directions

The paper identifies six open directions for future agent systems: silent failure and the observability-evaluation gap, persistence and longitudinal human-agent relationships, harness-boundary evolution, horizon scaling, governance and oversight at scale, and long-term human capability preservation [ref_2].
Vending-Bench contributes a concrete horizon-scaling evaluation in which agent success depends on sustained operational coherence rather than one-shot task completion [ref_3].
The benchmark also probes capital acquisition and resource management, which the paper treats as relevant both to useful agent applications and to safety concerns [ref_3].

## Sources

- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) — Liu et al., arXiv:2604.14228v1 (ref_2) [ref_2].
- [Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents](sources/vending-bench-2502-15840v1.md) — Backlund and Petersson, arXiv:2502.15840v1 (ref_3) [ref_3].
