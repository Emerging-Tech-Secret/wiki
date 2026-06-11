---
canonical_subject: "AI agent system design"
aliases: ["agent architecture design", "AI agent architecture", "agent system architecture"]
temperature: 82
rating: { factual: 78, neutrality: 82, layout: 75 }
core_facts:
  - claim: "AI agent system design includes recurring choices about reasoning loops, permission boundaries, context management, extensibility, delegation, and persistence"
    sources: [ref_2]
    locked: false
related: ["Claude Code", "OpenClaw", "Agentic coding tools", "ReAct (reasoning and acting)"]
last_external_fetch: 2026-06-10T23:32:38-03:00
---

# AI agent system design

Liu et al. define a design space for coding agents around recurring questions about where reasoning lives, how iteration loops are structured, what safety posture to adopt, how extension surfaces are partitioned, how context is managed, how work is delegated across subagents, and how sessions persist [ref_2].
The paper uses Claude Code and OpenClaw to show that the same design questions can produce different architectural answers under different deployment contexts [ref_2].

## Design principles from Claude Code

The paper identifies thirteen principles for production coding agents: deny-first with human escalation, graduated trust spectrum, defense in depth, externalized programmable policy, context as a scarce resource with progressive management, append-only durable state, minimal scaffolding with maximal operational harness, values over rules, composable multi-mechanism extensibility, reversibility-weighted risk assessment, transparent file-based configuration and memory, isolated subagent boundaries, and graceful recovery and resilience [ref_2].
These principles are traced to Claude Code implementation choices in permissioning, context management, extensibility, session persistence, and subagent isolation [ref_2].

## Architectural trade-offs

The paper contrasts per-action safety evaluation with perimeter-level access control as alternative safety architectures for agent systems [ref_2].
The paper contrasts a single CLI-centered loop with an embedded runtime inside a gateway control plane as alternative runtime architectures [ref_2].
The paper contrasts context-window extension mechanisms with gateway-wide capability registration as alternative extension and capability-management architectures [ref_2].

## Open directions

The paper identifies six open directions for future agent systems: silent failure and the observability-evaluation gap, persistence and longitudinal human-agent relationships, harness-boundary evolution, horizon scaling, governance and oversight at scale, and long-term human capability preservation [ref_2].

## Sources

- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) — Liu et al., arXiv:2604.14228v1 (ref_2) [ref_2].
