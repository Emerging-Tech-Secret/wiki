---
canonical_subject: "ReAct (reasoning and acting)"
aliases: ["ReAct", "ReAct prompting", "reasoning and acting", "reason and act"]
temperature: 80
rating:
  factual: 80
  neutrality: 85
  layout: 70
core_facts:
  - claim: "ReAct interleaves reasoning traces and task-specific actions in LLMs to synergize reasoning and acting"
    sources: [ref_1]
    locked: false
related: ["AI agents", "tool use", "chain-of-thought prompting", "HotpotQA", "ALFWorld", "WebShop"]
last_external_fetch: 2026-06-10T12:00:00-03:00
---

# ReAct (reasoning and acting)

**ReAct** uses large language models (LLMs) to generate both **reasoning traces** and
**task-specific actions** in an **interleaved** manner, creating synergy between the two [ref_1].
Reasoning traces help the model induce, track, and update action plans and handle exceptions, while
actions let it interface with external sources — such as knowledge bases or environments — to gather
additional information [ref_1]. It was introduced by Yao et al. (2022), "ReAct: Synergizing Reasoning
and Acting in Language Models" [ref_1].

## Knowledge-intensive tasks
On **HotpotQA** (question answering) and **Fever** (fact verification), ReAct interacts with a simple
Wikipedia API and thereby overcomes the hallucination and error-propagation issues prevalent in
chain-of-thought-only reasoning, producing more interpretable, human-like task-solving
trajectories [ref_1].

## Interactive decision making
On the **ALFWorld** and **WebShop** benchmarks, ReAct outperforms imitation- and
reinforcement-learning methods by an **absolute success rate of 34% and 10%** respectively, while
being prompted with only **one or two in-context examples** [ref_1]. ReAct also improves **human
interpretability and trustworthiness** over methods without reasoning or acting components [ref_1].

## Sources
- [ReAct: Synergizing Reasoning and Acting in Language Models](sources/react-2210-03629.md) — Yao et al., arXiv:2210.03629 (ref_1)
