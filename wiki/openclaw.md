---
canonical_subject: "OpenClaw"
aliases: ["OpenClaw agent gateway", "OpenClaw multi-channel personal assistant gateway"]
temperature: 75
rating: { factual: 75, neutrality: 80, layout: 70 }
core_facts:
  - claim: "OpenClaw is compared with Claude Code as a multi-channel personal assistant gateway that answers similar agent-system design questions in a different deployment context"
    sources: [ref_2]
    locked: false
related: ["Claude Code", "AI agent system design", "Agentic coding tools"]
last_external_fetch: 2026-06-10T23:32:38-03:00
---

# OpenClaw

OpenClaw is presented by Liu et al. as an independent open-source AI agent system and a multi-channel personal assistant gateway used for comparison with Claude Code [ref_2].
The paper treats OpenClaw as an example of how similar agent-system design questions can lead to different architectural answers when the deployment context changes [ref_2].

## Comparison with Claude Code

The paper compares Claude Code and OpenClaw across six dimensions: system scope and deployment model, trust model and security architecture, agent runtime and tool orchestration, extension architecture, memory and context management, and multi-agent architecture and routing [ref_2].
Claude Code is characterized as an ephemeral CLI or IDE coding harness, while OpenClaw is characterized as a persistent WebSocket gateway daemon and multi-channel control plane [ref_2].
Claude Code is described as using deny-first per-action rule evaluation with hooks, optional ML classification, and seven permission modes, while OpenClaw is described as using a single trusted operator per gateway plus DM pairing, inbound-channel allowlists, and configurable opt-in sandboxing [ref_2].
Claude Code's runtime is described as an iterative async-generator loop, while OpenClaw's runtime is described as a Pi-agent runner embedded inside gateway RPC dispatch with per-session queue serialization [ref_2].
Claude Code's extension architecture is described as MCP, plugins, skills, and hooks, while OpenClaw's extension architecture is described as a manifest-first plugin system with twelve capability types and a central registry plus a separate skills layer and MCP support [ref_2].

## Sources

- [Dive into Claude Code: The Design Space of Today's and Future AI Agent Systems](sources/dive-into-claude-code-2604-14228v1.md) — Liu et al., arXiv:2604.14228v1 (ref_2) [ref_2].
