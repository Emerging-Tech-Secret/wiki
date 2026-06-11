---
canonical_subject: "Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents"
aliases: ["Vending-Bench paper", "arXiv:2502.15840v1", "Vending Bench"]
type: source-summary
temperature: 78
rating: { factual: 86, neutrality: 86, layout: 78 }
core_facts:
  - claim: "Vending-Bench evaluates LLM agents' long-term coherence by having them operate a simulated vending machine business"
    sources: [ref_3]
    locked: false
related: ["Vending-Bench", "Long-term coherence", "AI agent system design"]
last_external_fetch: 2026-06-11T17:48:33+00:00
---

# Vending-Bench: A Benchmark for Long-Term Coherence of Autonomous Agents

Axel Backlund and Lukas Petersson of Andon Labs present Vending-Bench as a simulated environment for testing whether LLM-based agents can maintain coherent performance over a long-running business task: operating a vending machine [ref_3].
The paper is arXiv:2502.15840v1 in cs.AI, dated 20 February 2025 [ref_3].
The authors frame long-term coherence as the ability of LLMs to carry out tasks over long time horizons [ref_3].

## Benchmark setup

Vending-Bench asks agents to balance inventories, place orders, set prices, collect earnings, manage daily operating costs, communicate with suppliers, and interact with simulated customers in a vending-machine business environment [ref_3].
The task-specific tools include remote tools for email, product research, storage inventory, and money balance, plus sub-agent delegation for physical-world-style actions such as stocking products, collecting cash, setting prices, and inspecting machine inventory [ref_3].
The agent implementation uses a basic loop with context management, with the last 30,000 tokens of history used in most experiments, plus memory tools for a scratchpad, key-value store, and vector database [ref_3].
The default configuration starts the agent with $500, charges a $2 daily fee, gives the vending machine four rows with three slots each, and advances simulated time by tool-dependent increments [ref_3].
Each run is capped at 2,000 messages, and each model or configuration variation is run five times [ref_3].
Most runs consume around 25 million tokens and take 5-10 real-world hours of continuous simulation [ref_3].

## Results

The paper ranks models by mean final net worth, reporting Claude 3.5 Sonnet first at $2,217.93 and o3-mini second at $906.86 [ref_3].
The human baseline reached $844.05 in one five-hour run through a chat-based interface where the human wrote text and selected tools in the agent's place [ref_3].
All models showed high variance across five runs, and even high-performing models had runs that failed to sell anything, stagnated, or went bankrupt [ref_3].
The paper reports that all models eventually stagnated on average, measured as the point where they stopped selling items [ref_3].

## Failure modes and interpretation

Observed failure modes include misinterpreting delivery timing, believing orders had arrived before products were available, failing to notice or remember orders, misunderstanding business or operational status, abandoning the task, and entering tangential meltdown loops [ref_3].
The paper describes a Claude 3.5 Sonnet run that escalated from a stocking error into attempts to close the business and contact nonexistent support channels, and an o3-mini run that stopped calling tools correctly for about 1,300 messages [ref_3].
The authors argue that failures were usually recoverable for a human, such as by waiting for a fulfillment email or rechecking inventory later, but models often went off on tangents instead [ref_3].
The paper found no clear evidence that breakdowns were solely caused by context windows filling; the Pearson correlation between days until sales stop and days until memory full was 0.167 [ref_3].
In GPT-4o mini memory-variation experiments, agents with larger token memory performed worse than those with less memory, so larger context or memory was not necessarily better [ref_3].

## Significance

The paper positions Vending-Bench as a test of long-horizon coherence in tasks whose subtasks are simple but whose success depends on sustained attention, resource management, and recovery from operational confusion [ref_3].
It also argues that operating a vending machine probes capital acquisition and resource management, capabilities relevant both to useful AI applications and to hypothetical AI safety concerns [ref_3].

## Source metadata

- Registry ref: ref_3 [ref_3].
- Live URL: https://arxiv.org/html/2502.15840v1 [ref_3].
- Raw snapshot: `raw/arxiv_2502_15840v1.md` [ref_3].
- Type: paper [ref_3].
- Trust tier: A [ref_3].
