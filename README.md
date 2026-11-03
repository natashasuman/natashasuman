<h1 align="center">Natasha Suman</h1>
<h3 align="center">ML Engineer · LLMs, RAG & Agentic AI</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/natasha-suman/"><img src="https://img.shields.io/badge/LinkedIn-Natasha_Suman-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:natasha13suman@gmail.com"><img src="https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/natashasuman"><img src="https://img.shields.io/badge/GitHub-natashasuman-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&pause=1000&center=true&vCenter=true&width=900&lines=Machine+Learning+Engineer;Hybrid+RAG+%7C+QLoRA+Fine-Tuning+%7C+LangGraph+Agents;LLM+Systems+You+Can+Measure" alt="Typing SVG" />
</p>

---

## 👩‍💻 About Me

MSc Data Science graduate from **University College Dublin**, based in **Bengaluru**, and open to ML, GenAI and LLM engineering roles.

I build LLM systems that can **prove they work**. Each project ships with its own evaluation,
compares itself against a simpler baseline, and fails loudly instead of quietly returning something plausible.
Before LLMs, I built production PySpark pipelines for global portfolio managers at **Swiss Re**.

---

## 💼 Experience

**Machine Learning Intern (Founding Team)** · Crypto Analytics Startup · *Apr 2024 – Present*
Forecasting pipeline on live Binance market data and GNews headlines (XGBoost, Random Forest), with rolling-window retraining, feature ablations and anomaly monitoring.

**Data Analyst, Risk & Economics** · Swiss Re, Bangalore · *Jun 2021 – Aug 2022*
Rebuilt Excel/DAX forecasting logic as PySpark pipelines in Palantir Foundry, and built ETL feeding risk dashboards for global portfolio managers. Received the **Best Employee** award.

**ML Industry Project (Microsoft-sponsored)** · University College Dublin · *Jun – Aug 2023*
Bi-LSTM misinformation classifier deployed on Azure; presented to Microsoft product leaders.

---

## 📊 Engineering Highlights

| Area | Highlight |
|---|---|
| Data Engineering | Forecasting refresh cut from **18 hours → 15 minutes** (Swiss Re) |
| Analytics | **10+ dashboards** tracking **50+ risk KPIs** for global portfolio managers |
| Retrieval | **4 retrieval setups** benchmarked head-to-head: dense, BM25, hybrid (RRF), hybrid + rerank |
| Fine-Tuning | **7B model** trained in **4-bit** on a free **16 GB T4**, tested on **companies held out of training** |
| Evaluation | LLM judge with **position swapping**, plus a deterministic **hallucinated-figure check** |
| Agents | LLM decisions behind **code-level guardrails**, with a **human-approval interrupt** before any trade |
| Quality | **57 automated tests** across 3 repos, with CI on every push |

---

## 🚀 Featured Projects

### 1. 🔎 Financial Filings RAG

Question answering over SEC 10-K / 10-Q filings, with answers that can be traced to their sources.

**Highlights**
- **Hybrid search:** dense embeddings and BM25 run inside Qdrant and are merged with Reciprocal Rank Fusion.
- **Cross-encoder reranking** (bge-reranker-large) over a 4× wider candidate pool.
- **Citation checking:** an answer that cites a passage it was never given is flagged as ungrounded.
- **Evaluation harness:** Recall@1/5/10, MRR@10, p50/p95 latency and grounded-answer rate.
- If embedding fails, ingestion stops with an error. Re-ingesting a document replaces its chunks instead of duplicating them.

**Stack:** `Python` `FastAPI` `Qdrant` `Gemini` `bge-reranker` `Docker` `GitHub Actions`
🔗 [Repository](https://github.com/natashasuman/RAG)

### 2. 🎯 Credit-Risk Fine-Tuning with QLoRA

Teaches Qwen2.5-7B to assess the credit-risk impact of 10-K liquidity disclosures.

**Highlights**
- Dataset built from **real EDGAR filings of 60 companies**, labelled by a stronger teacher model.
- **Company-level split:** the model is tested only on companies it never saw in training.
- **4-bit NF4 QLoRA** (r=16), with loss computed on the answer only.
- Compared against **the same weights with the adapter switched off**, so the fine-tune is the only difference.
- Metrics: accuracy, macro-F1, hallucinated-figure rate, and a position-swapped pairwise judge.

**Stack:** `Transformers` `PEFT` `TRL` `bitsandbytes` `FastAPI` `Colab`
🔗 [Repository](https://github.com/natashasuman/fine_tune)

### 3. 🤖 Multi-Agent Portfolio Risk & Rebalancing

An LLM analyst decides *whether* and *how far* to de-risk a portfolio. **It never produces a number.**

**Highlights**
- VaR, CVaR and **each holding's share of total risk**, computed from real market data.
- **SciPy SLSQP optimiser** finds the smallest change that satisfies every policy limit.
- **Guardrails** override the LLM when it ignores a breach or sets a target above the policy limit.
- **Compliance loop:** failed checks retry with tighter targets, then escalate to a person.
- **Human approval** via LangGraph `interrupt()`, with a full audit trail of every decision.

**Stack:** `LangGraph` `SciPy` `pandas` `Gemini` `pytest`
🔗 [Repository](https://github.com/natashasuman/Agents)

---

## 🛠️ Technical Expertise

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,pytorch,sklearn,fastapi,docker,githubactions,azure,linux" />
</p>

**LLM Engineering:** LangGraph · LangChain · Hugging Face Transformers · PEFT / QLoRA · TRL · bitsandbytes · Gemini API · structured outputs
**Retrieval & Evaluation:** Qdrant · hybrid search (BM25 + dense) · cross-encoder reranking · Recall@k / MRR · LLM-as-a-Judge
**Machine Learning:** PyTorch · scikit-learn · XGBoost · LSTM · time-series forecasting · NLP (spaCy)
**Data & Backend:** Python · SQL · PySpark · Airflow · Palantir Foundry · FastAPI · Docker · pytest

---

## 🎓 Education & Certifications

**MSc Data Science**, University College Dublin · 2:1 · *2023*
**B.Tech Computer Science**, REVA University · *2021*

<img src="https://img.shields.io/badge/DeepLearning.AI-MLOps_(ML_Engineering_for_Production)-FF6F00?style=for-the-badge&logo=coursera&logoColor=white" />

---

## 📈 GitHub Analytics

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=natashasuman&show_icons=true&theme=tokyonight" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=natashasuman&layout=compact&theme=tokyonight" />
</p>

---

## 🔭 Current Focus

- Running the full retrieval and fine-tuning benchmarks and publishing the results
- Adding tracing and cost monitoring to LLM pipelines
- Agent evaluation: scoring the path an agent took, not just its final answer

---

<p align="center"><i>LLM systems you can measure, explain and trust.</i></p>

<p align="center">
  <a href="https://www.linkedin.com/in/natasha-suman/">LinkedIn</a> ·
  <a href="mailto:natasha13suman@gmail.com">Email</a> ·
  <a href="https://github.com/natashasuman">GitHub</a>
</p>
