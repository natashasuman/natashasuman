# Hi, I'm Natasha Suman

### AI/ML Engineer | Generative AI | LLM Systems | Financial Intelligence

I build production-oriented AI systems that combine **Large Language Models, Retrieval-Augmented Generation, Agentic Workflows, and Parameter-Efficient Fine-Tuning** to solve complex problems in financial intelligence and decision support.

My work focuses on moving beyond simple LLM applications toward **reliable, evaluable, and domain-aware AI systems**.

---

## What I Build

* **Agentic AI Systems** — autonomous multi-agent workflows for financial analysis, risk assessment, optimization, and compliance
* **Production RAG Systems** — low-latency retrieval pipelines with vector search, metadata filtering, reranking, and citation-grounded generation
* **Domain-Specific LLMs** — PEFT/QLoRA fine-tuning for financial reasoning, credit-risk analysis, and earnings sentiment
* **LLM Evaluation** — automated evaluation pipelines using LLM-as-a-Judge methodologies
* **AI Engineering** — production APIs, containerization, testing, observability, and scalable inference architectures

---

## Featured Projects

### 1. Multi-Agent Portfolio Risk & Rebalancing System

**Python · LangGraph · Google Gemini · Agentic AI**

[View Repository →](https://github.com/natashasuman/Agents)

An autonomous multi-agent framework for portfolio risk analysis and rebalancing.

**Key capabilities:**

* Market intelligence and volatility analysis
* Parametric **Value-at-Risk (VaR)** computation
* LLM-assisted risk assessment
* Automated portfolio rebalancing recommendations
* Compliance and concentration-limit validation
* Structured agent state management and workflow orchestration
* Audit trails for decision traceability

**Architecture:**

`Market Data → Risk Assessment → Rebalancing Optimization → Compliance Audit → Simulation`

The system demonstrates how LLM agents can be combined with deterministic financial computation rather than relying on an LLM alone.

---

### 2. Financial Earnings RAG Intelligence System

**Python · FastAPI · Qdrant · Gemini · Cross-Encoder Reranking · Docker**

[View Repository →](https://github.com/natashasuman/RAG)

A production-oriented RAG platform designed for querying and analyzing financial filings and earnings documents.

**Pipeline:**

`Documents → Parsing → Chunking → Embeddings → Vector Search → Reranking → LLM → Cited Answer`

**Key capabilities:**

* PDF and text ingestion
* Financial document chunking with metadata preservation
* Vector retrieval using **Qdrant**
* Metadata-aware filtering by ticker/document
* Candidate retrieval followed by **Cross-Encoder reranking**
* Citation-grounded LLM generation
* FastAPI REST interface
* Docker-based deployment
* Automated testing with pytest

The retrieval layer uses dense candidate retrieval followed by `BAAI/bge-reranker-large` to improve semantic relevance before context is passed to the generation model.

---

### 3. Financial LLM Fine-Tuning with QLoRA

**Python · Hugging Face PEFT · TRL · bitsandbytes · QLoRA**

[View Repository →](https://github.com/natashasuman/fine_tune)

General-purpose LLMs can struggle with the quantitative and contextual nuance present in financial language.

For example:

> "Revenue expanded 4% while operating margin contracted 180 bps."

Correctly interpreting the relationship between growth, profitability, and basis-point movements requires domain-specific financial reasoning.

This project explores **Parameter-Efficient Fine-Tuning (PEFT)** using **4-bit quantization and QLoRA** to adapt smaller open-source language models for financial intelligence tasks.

**Target applications include:**

* Corporate credit-risk analysis
* Financial statement interpretation
* Earnings sentiment classification
* Financial reasoning
* Corporate disclosure analysis

**Technology stack:**

`Hugging Face Transformers → bitsandbytes → PEFT/QLoRA → TRL`

The broader evaluation strategy incorporates **LLM-as-a-Judge** methodologies with frameworks such as RAGAS / DeepEval to assess generated responses beyond traditional loss-based training metrics.

---

## Technical Focus

### Generative AI

`LLMs` · `RAG` · `Agentic AI` · `Prompt Engineering` · `LLM Evaluation` · `Fine-Tuning`

### LLM Engineering

`LangGraph` · `Hugging Face` · `PEFT` · `QLoRA` · `TRL` · `bitsandbytes`

### Retrieval & Search

`Qdrant` · `Embeddings` · `Vector Search` · `Hybrid Retrieval` · `Cross-Encoder Reranking`

### Backend & Deployment

`Python` · `FastAPI` · `Docker` · `REST APIs` · `Pytest`

### Financial AI

`Credit Risk` · `Financial Filings` · `Earnings Analysis` · `Portfolio Risk` · `VaR` · `Financial Sentiment`

---

## Engineering Philosophy

I am particularly interested in building AI systems that are:

**Reliable**
Grounded in verifiable information rather than relying solely on model-generated knowledge.

**Domain-Aware**
Adapted to the terminology, reasoning patterns, and constraints of the target industry.

**Evaluable**
Measured using systematic evaluation rather than relying on subjective impressions of LLM output quality.

**Production-Oriented**
Designed with APIs, testing, deployment, latency, observability, and maintainability in mind.

**Composable**
Built from modular retrieval, reasoning, orchestration, and evaluation components that can evolve independently.

---

## Currently Exploring

* Advanced agent orchestration and multi-agent architectures
* Efficient LLM fine-tuning and quantization
* Financial reasoning with domain-specific language models
* RAG evaluation and retrieval optimization
* LLM observability and production reliability
* Autonomous decision-support systems

---

## Selected Architecture

```text
                    ┌─────────────────────────┐
                    │      Financial Data     │
                    │ Filings • Reports • News │
                    └────────────┬────────────┘
                                 │
                 ┌───────────────▼───────────────┐
                 │       Retrieval Layer         │
                 │ Embeddings • Vector Search    │
                 │ Metadata • Reranking          │
                 └───────────────┬───────────────┘
                                 │
                 ┌───────────────▼───────────────┐
                 │        Reasoning Layer        │
                 │   RAG • Agents • Fine-Tuned   │
                 │            LLMs               │
                 └───────────────┬───────────────┘
                                 │
                 ┌───────────────▼───────────────┐
                 │       Evaluation Layer        │
                 │ RAGAS • DeepEval • LLM Judge  │
                 └───────────────┬───────────────┘
                                 │
                 ┌───────────────▼───────────────┐
                 │       Production APIs         │
                 │       FastAPI • Docker        │
                 └───────────────────────────────┘
```

---

## Projects

| Project       | Focus                                             | Technologies                           |
| ------------- | ------------------------------------------------- | -------------------------------------- |
| **Agents**    | Multi-Agent Financial Risk & Portfolio Simulation | LangGraph, Gemini, Python              |
| **RAG**       | Financial Earnings Intelligence                   | FastAPI, Qdrant, Gemini, Cross-Encoder |
| **Fine-Tune** | Financial Domain LLM Adaptation                   | PEFT, QLoRA, TRL, bitsandbytes         |

---

### Connect

If you're interested in **Generative AI, LLM engineering, financial AI, or production ML systems**, feel free to explore the repositories above.
<!--
**natashasuman/natashasuman** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
