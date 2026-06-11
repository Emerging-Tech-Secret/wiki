---
canonical_subject: "Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems"
aliases: ["Dive into Claude Code", "arXiv:2604.14228v1", "Liu et al. 2026 Claude Code"]
type: source-summary
temperature: 80
rating: { factual: 85, neutrality: 80, layout: 75 }
core_facts:
  - claim: "The paper analyzes Claude Code's architecture from publicly available TypeScript source code and compares it with OpenClaw"
    sources: [ref_2]
    locked: false
related: ["Claude Code", "OpenClaw", "AI agent system design", "Agentic coding tools"]
last_external_fetch: 2026-06-10T23:32:38-03:00
---

# Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems

**Source:** Jiacheng Liu, Xiaohan Zhao, Xinyi Shang, and Zhiqiang Shen, *Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems*, arXiv:2604.14228v1, 14 Apr 2026 [ref_2].
**Trust tier:** A (arXiv) [ref_2].
**Snapshot:** `raw/arxiv_2604_14228v1.md` [ref_2].

## What it studies

- The paper studies Claude Code as an agentic coding tool that can run shell commands, edit files, and call external services on behalf of a user [ref_2].
- The paper bases its architectural description on publicly available TypeScript source code for Claude Code v2.1.88 and states that it did not use private, confidential, or unauthorized materials [ref_2].
- The paper compares Claude Code with OpenClaw as an independent open-source AI agent system that answers related design questions in a different deployment context [ref_2].

## Main findings

- The paper identifies five motivating values for Claude Code's architecture: human decision authority, safety and security, reliable execution, capability amplification, and contextual adaptability [ref_2].
- The paper maps those values to thirteen design principles, including deny-first human escalation, graduated trust, defense in depth, externalized programmable policy, progressive context management, append-only durable state, isolated subagent boundaries, and graceful recovery [ref_2].
- The paper describes Claude Code's core as a simple loop that calls the model, runs tools, collects results, and repeats until a stop condition is reached [ref_2].
- The paper argues that much of Claude Code's architecture sits around that loop in permissioning, context management, extensibility, subagent orchestration, and session persistence systems [ref_2].

## Architectural details highlighted

- Claude Code's permission model includes seven modes: plan, default, acceptEdits, auto, dontAsk, bypassPermissions, and bubble [ref_2].
- Claude Code's permission rules are evaluated in deny-first order, so a deny rule takes precedence over an allow rule even when the allow rule is more specific [ref_2].
- Claude Code's context-management pipeline uses five layers: budget reduction, snip, microcompact, context collapse, and auto-compact [ref_2].
- Claude Code exposes four extension mechanisms: MCP servers, plugins, skills, and hooks [ref_2].
- Claude Code's Agent tool can spawn isolated subagents, including built-in roles such as Explore, Plan, general-purpose, Claude Code Guide, Verification, and Statusline-setup when the relevant feature flags and entrypoints allow them [ref_2].
- Claude Code stores session transcripts as mostly append-only JSONL files, while resume and fork rebuild conversations without restoring session-scoped permissions [ref_2].

## Comparison and future directions

- The paper contrasts Claude Code's per-action safety evaluation with OpenClaw's perimeter-level access-control model for a persistent multi-channel gateway [ref_2].
- The paper contrasts Claude Code's single CLI-centered loop with OpenClaw's embedded runtime inside a gateway control plane [ref_2].
- The paper identifies six future design directions: silent failure and observability, persistent memory and longitudinal human-agent relationships, harness-boundary evolution, horizon scaling, governance and oversight, and long-term human capability preservation [ref_2].

## Related pages

- [Claude Code](../claude-code.md) [ref_2].
- [OpenClaw](../openclaw.md) [ref_2].
- [AI agent system design](../ai-agent-system-design.md) [ref_2].
- [Agentic coding tools](../agentic-coding-tools.md) [ref_2].
