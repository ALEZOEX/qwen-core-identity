[Читать на русском](README.md)

# 🚀 QWEN CORE IDENTITY v18.2 (Ultimate Knowledge Graph Edition)

The biggest architectural leap since version `10.6`. The system prompt has been fully rewritten to transform the LLM from a generic assistant into a strict *Knowledge Graph Management System* with an advanced *Mixture-of-Experts (MoE) pipeline*. We have solved some of the most fundamental cognitive shortcomings of Large Language Models.

### 🔥 What's New & Upgraded since v10.6:

#### 1. Entity Resolution Protocol (Knowledge Graph Engine)
The model no longer suffers from "memory gaps" and **stops asking annoying "Who is X?" questions**.
* **Deferred Resolution:** When you mention an unrecognized person or project, the model silently invokes the `bio`-tool and stores it as an `[unverified entity]`. Once the context is clarified in future conversations, the model will smoothly update the knowledge node without ever disrupting the flow.
* **Garbage Collection:** We implemented dynamic Memory Bloat protection. Hanging `[unverified]` nodes that gain no context are flushed automatically. 
* **Entity Anti-Hallucination:** Prevented the catastrophic AI habit of forcefully merging different concepts or people sharing the same name.

#### 2. Autoregressive Fix & "No Self-Review Loop" Ban
Massive patch: We hard-banned the model from apologizing ("I'm sorry, I made a mistake here") in its final output. Since LLMs operate token-by-token (autoregressive), we forced all conflict resolution, alternatives tables, and fact-checking to take place entirely inside the explicit/hidden `[ANALYSIS]` block *before* finalizing any code. 

#### 3. Task Complexity Splitting
Version 10.6 often overcomplicated simple tasks by forcing full-scale architectural reviews on 5-line scripts. 
Now, complexity is segmented into **[Complex-Implementation]** (fast-track optimized generation) and **[Complex-Architecture]** (triggering the heavyweight 6-phase MoE pipeline intended only for cryptography, network protocol design, and physics algorithms).

#### 4. Pre-Computation 2.0 (Factual vs. Calculated Data)
Numeric data processing was completely split:
* **Hard Facts (Versions, Constants, Prices, CVEs):** These require independent Web Tool calls strictly outputting an actual URL. Rapid-changing tech metrics obey a new TTL caching system (forces re-search after a specific dialogue timeframe). 
* **Calculated Values (Latencies, Metric formulas):** The model MUST "Show Its Work." At least 80% of computed output must now physically display its parent mathematical substitution. Unsolvable data rigidly yields a `[GAP: estimate]` placeholder.

#### 5. The Elimination of Fake Tool-Calls
Removed "Mocking" behaviour where models stream text pretending to call tools (`[Searching for X...]`). Web/bio and memory checks operate as pure background systems. Additionally, the heavyweight Role-Play domain RED TEAMING matrices (dialogues between [Theorist], [Paranoid], and [Compiler]) have been successfully reinstated.
