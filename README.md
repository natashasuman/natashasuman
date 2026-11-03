## Hi, I'm Natasha 👋

**ML Engineer: LLMs, RAG & agentic systems** · MSc Data Science, University College Dublin · Bengaluru

I build LLM systems that can be measured: retrieval with evaluation sets, fine-tunes benchmarked
against their base models, and agents whose decisions sit behind guardrails and leave an audit
trail. Before that I built PySpark data pipelines for global portfolio managers at Swiss Re.

### Featured projects

**[Financial Filings RAG](https://github.com/natashasuman/RAG)** · FastAPI · Qdrant · Gemini · bge-reranker · Docker
Question answering over SEC 10-K/10-Q filings. Hybrid retrieval (dense + BM25, fused with RRF
inside Qdrant), cross-encoder reranking, and **citation checking** that flags any answer citing a
passage it was never given. Includes an evaluation harness comparing dense, BM25, hybrid and reranked
retrieval on Recall@k, MRR and latency.

**[Credit-Risk Fine-Tuning with QLoRA](https://github.com/natashasuman/fine_tune)** · Transformers · PEFT · TRL · bitsandbytes
Qwen2.5-7B fine-tuned in 4-bit on liquidity disclosures from real 10-Ks, with labels distilled from
a stronger teacher model. It is benchmarked against the base model on **companies held out of
training**, using accuracy, macro-F1, an unsupported-figure (hallucination) rate and a
position-swapped pairwise LLM judge. Runs on a free Colab T4.

**[Multi-Agent Portfolio Risk](https://github.com/natashasuman/Agents)** · LangGraph · SciPy · Gemini
An LLM analyst decides whether to de-risk; deterministic tools compute VaR, CVaR and component VaR
from market data and solve a constrained rebalance. Guardrails override unsafe LLM decisions,
failed compliance checks loop back to the optimizer, and a human-approval interrupt sits before any
trade.

### Toolkit

**LLM:** LangGraph · LangChain · Hugging Face Transformers · PEFT/QLoRA · TRL · Gemini API · structured outputs<br>
**Retrieval:** Qdrant · hybrid search (BM25 + dense) · cross-encoder reranking · retrieval evaluation<br>
**ML & data:** PyTorch · scikit-learn · XGBoost · PySpark · SQL · Airflow<br>
**Engineering:** Python · FastAPI · Docker · pytest · GitHub Actions · Azure ML

### Contact

[LinkedIn](https://www.linkedin.com/in/natasha-suman/) · natasha13suman@gmail.com
