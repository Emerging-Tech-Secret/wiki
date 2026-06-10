---
canonical_subject: "ReAct (reasoning and acting)"
aliases: ["ReAct", "ReAct prompting", "reasoning and acting"]
temperature: 80
rating: { factual: 80, neutrality: 85, layout: 70 }
core_facts:
  - claim: "ReAct interleaves reasoning traces and task-specific actions in LLMs"
    sources: [ref_1]
    locked: false
related: ["AI agents", "tool use", "chain-of-thought prompting"]
last_external_fetch: 2026-06-10T12:00:00-03:00
---

# ReAct (reasoning and acting)

**ReAct** uses LLMs to generate both **reasoning traces** and **task-specific actions** in an
**interleaved** manner, creating synergy between the two [ref_1]. Reasoning traces help the model
induce, track, and update action plans and handle exceptions; actions let it interface with external
sources to gather information [ref_1]. Introduced by Yao et al. (2022) [ref_1].

## Knowledge-intensive tasks
On **HotpotQA** and **Fever**, ReAct interacts with a simple Wikipedia API and overcomes the
hallucination and error-propagation issues of chain-of-thought-only reasoning [ref_1].

## Interactive decision making
On **ALFWorld** and **WebShop**, ReAct outperforms imitation- and reinforcement-learning methods by
an **absolute success rate of 34% and 10%** respectively, with only one or two in-context
examples [ref_1].

## Sources
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) — Yao et al., arXiv:2210.03629 (ref_1)
