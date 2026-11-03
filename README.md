## Hi, I'm Natasha 👋

**ML Engineer: LLMs, RAG & Agentic AI** · Bengaluru, India · Open to ML / GenAI / LLM engineering roles

MSc Data Science graduate from **University College Dublin**, previously a data analyst at **Swiss Re**, where I cut a
forecasting refresh from **18 hours to 15 minutes** by rebuilding it in PySpark.

I care about one thing in LLM work above all: **being able to prove it works.** Each project below
comes with its own evaluation, compares itself against a simpler baseline, and fails loudly
instead of quietly returning something plausible.

---

### 🔎 [Financial Filings RAG](https://github.com/natashasuman/RAG)
`FastAPI` `Qdrant` `Gemini` `bge-reranker` `Docker` `GitHub Actions`

Question answering over SEC 10-K / 10-Q filings.

**How it works:** dense embeddings and BM25 run as a hybrid search inside Qdrant and are merged
with Reciprocal Rank Fusion. A cross-encoder then reranks a 4× wider candidate pool. Every answer
cites numbered sources, and the API checks each citation against what was actually retrieved, so
an answer citing a passage it was never given is flagged as ungrounded.

**How it's measured:** an evaluation harness compares four setups on the same question set: dense
only, BM25 only, hybrid, and hybrid + rerank. It reports Recall@1/5/10, MRR@10 and p50/p95 latency,
plus an end-to-end "grounded answer" rate.

**Why BM25 matters here:** filings are full of exact tokens (tickers, fiscal years, "Term Loan B",
"SOFR + 275 bps") that dense embeddings blur and keyword search matches exactly.

### 🎯 [Credit-Risk Fine-Tuning with QLoRA](https://github.com/natashasuman/fine_tune)
`Transformers` `PEFT` `TRL` `bitsandbytes` `Qwen2.5-7B`

Teaches a 7B model to assess the credit-risk impact of 10-K liquidity disclosures.

**How it's built:** liquidity passages are pulled from real EDGAR filings of 60 companies and
labelled by a stronger teacher model. The base model is loaded in 4-bit NF4 and trained with LoRA
(r=16), with loss computed on the answer only. It runs on a free Colab T4.

**How it's measured:**
- **No leakage:** train and test are split *by company*, so the model is tested on companies it has never seen.
- **Fair baseline:** the comparison model is the same 4-bit weights with the adapter switched off, so the fine-tune is the only difference.
- **Hallucination check:** a deterministic test flags any figure in the answer that doesn't appear in the source passage.
- **Unbiased judge:** the LLM judge compares each pair of answers twice in swapped order, and only consistent wins count. This cancels its known bias toward whichever answer it sees first.

### 🤖 [Multi-Agent Portfolio Risk & Rebalancing](https://github.com/natashasuman/Agents)
`LangGraph` `SciPy` `pandas` `Gemini`

An LLM analyst decides *whether* and *how far* to de-risk a portfolio. **It never produces a number.**

**How it works:**
- **Market data:** tools compute VaR, CVaR and each holding's share of total risk from real price history.
- **Rebalancing:** a constrained optimiser finds the smallest change that satisfies every policy limit.
- **Guardrails:** they override the LLM when it ignores a policy breach or sets a target above the limit.
- **Compliance loop:** failed checks send the plan back to the optimiser with a tighter target, then escalate to a person if nothing works.
- **Human approval:** the workflow pauses before any trade until someone approves or rejects it.

**How it's tested:** every path through the graph has a test, and so does the maths. Component VaR
must sum exactly to total VaR, and ~5% of days must breach a 95% VaR.

---

### 🛠️ Toolkit

| | |
|---|---|
| **LLM** | LangGraph · LangChain · Hugging Face Transformers · PEFT / QLoRA · TRL · Gemini API · structured outputs |
| **Retrieval** | Qdrant · hybrid search (BM25 + dense) · cross-encoder reranking · retrieval evaluation |
| **ML** | PyTorch · scikit-learn · XGBoost · time-series forecasting · NLP (spaCy) |
| **Data** | Python · SQL · PySpark · Airflow · Palantir Foundry |
| **Engineering** | FastAPI · Docker · pytest · GitHub Actions · Azure ML |

### 🎓 Education

**MSc Data Science**, University College Dublin (2:1) · Microsoft-sponsored industry project on misinformation detection<br>
**B.Tech Computer Science**, REVA University

### 📫 Contact

[LinkedIn](https://www.linkedin.com/in/natasha-suman/) · natasha13suman@gmail.com
