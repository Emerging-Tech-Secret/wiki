---
canonical_subject: "Vending-Bench"
aliases: ["Vending Bench", "vending machine agent benchmark", "arXiv:2502.15840v1 benchmark"]
temperature: 78
rating: { factual: 84, neutrality: 86, layout: 76 }
core_facts:
  - claim: "Vending-Bench evaluates LLM agents' long-term coherence by having them operate a simulated vending machine business"
    sources: [ref_3]
    locked: false
related: ["Long-term coherence", "AI agent system design", "Agentic coding tools"]
last_external_fetch: 2026-06-11T17:48:33+00:00
---

# Vending-Bench

Vending-Bench is a benchmark for evaluating long-term coherence in LLM-based agents by asking them to run a simulated vending machine business [ref_3].
The benchmark was introduced by Axel Backlund and Lukas Petersson of Andon Labs in the arXiv paper "Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents" [ref_3].

## Task environment

The agent must buy products from suppliers by email, stock items in the vending machine, set competitive prices, collect earnings regularly, and manage daily operating costs [ref_3].
The environment also simulates supplier communication and daily customer purchases, including price-elastic demand, day-of-week effects, monthly effects, weather factors, product-variety effects, random noise, and inventory caps [ref_3].
The main agent receives tools for email, product research, storage inventory, and money-balance checks, while sub-agent delegation simulates physical-world actions such as stocking the machine, collecting cash, setting prices, and checking machine inventory [ref_3].

## Agent loop and resources

The agent is implemented as a basic loop where the LLM repeatedly calls tools based on prior iterations and the task objective [ref_3].
Most experiments pass the last 30,000 tokens of history into each inference call, and the agent also has memory tools for a scratchpad, key-value store, and vector database [ref_3].
The benchmark uses task-specific tools and a sub-agent interface with tools for sub-agent specs, running a sub-agent, and chatting with a sub-agent about what happened during a delegated run [ref_3].

## Evaluation protocol and scoring

The default environment starts with a $500 balance and charges a $2 daily fee, and each tool call advances simulated time by 5 minutes, 25 minutes, 75 minutes, or 5 hours depending on the tool [ref_3].
The authors run agents for 2,000 messages per run, end early if an agent cannot pay the daily fee for 10 consecutive days, and run each model or configuration variation five times [ref_3].
Most runs consume about 25 million tokens and take 5-10 real-world hours [ref_3].
The primary score is final net worth: cash at hand, cash still in the vending machine, and wholesale-price value of unsold products in storage or in the machine [ref_3].

## Reported findings

Claude 3.5 Sonnet had the highest reported mean net worth at $2,217.93, o3-mini was second at $906.86, and the human baseline reached $844.05 in a single five-hour run [ref_3].
The authors report high variance for every model, with even top models producing failed or stagnant runs [ref_3].
Common failures included misreading delivery status, forgetting or failing to notice orders, misinterpreting operational status, abandoning the task, and entering tangential meltdown loops [ref_3].
The paper found no clear evidence that breakdowns were solely caused by context-window filling, reporting a Pearson correlation of 0.167 between days until sales stop and days until memory full [ref_3].
In GPT-4o mini memory experiments, larger token memory performed worse than smaller memory, so increasing memory was not necessarily beneficial [ref_3].

## Why it matters

Vending-Bench targets long-horizon tasks whose individual actions are simple but whose success depends on sustained operational coherence [ref_3].
The paper also argues that vending-machine operation tests resource and capital acquisition, making the benchmark relevant to both useful agent capabilities and safety-oriented dangerous-capability concerns [ref_3].

## Sources

- [Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents](sources/vending-bench-2502-15840v1.md) — Backlund and Petersson, arXiv:2502.15840v1 (ref_3) [ref_3].
