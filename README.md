# Yassin Yasser

**Applied AI Engineer | Agent systems with evals & deep learning for media forensics**  
Cairo, Egypt · Open to AI/ML Engineering & Research roles (Remote, UAE / Relocation) · Graduating July 2027

[LinkedIn](https://linkedin.com/in/yassinyasser) · [Hugging Face](https://huggingface.co/yyouretoast) · [Email](mailto:yyasso2005@gmail.com)

---

### Projects

#### [Dual-Stream Deepfake Forensics Engine](https://github.com/yyouretoast/deepfake-detection) · [Demo](https://huggingface.co/spaces/yyouretoast/deepfake-detector)
`PyTorch` `ConvNeXt` `2D FFT` `Bi-GRU` `OpenCV` `Streamlit`

**Test set:** 2,250 videos / 26,981 crops (FF++, Celeb-DF v2, and 1,300 unseen Google DFD videos)  
**Results:** 0.8994 video ROC-AUC (18.54% EER) vs 0.8962 (19.43%) for uniform frame averaging · 0.8651 frame-level AUC on zero-shot Google DFD · 14.08 ms/crop full pipeline at batch 32 (RTX 4060)

* Pairs a ConvNeXt-Small spatial stream with a frequency stream (SRM filters, Bayar-Stamm convolution, 2D FFT), fused with SNR-adaptive gating.
* Identity-disjoint splits: pair-disjoint FF++, actor-graph-partitioned Celeb-DF v2. Google DFD is never trained on and is used only as a zero-shot test set.
* Leave-one-manipulation-out on FF++ (4 folds, balanced cohorts): 0.9514 macro AUC. Platt scaling fit on validation only cuts calibration error 49.4% (0.1965 → 0.0994).
* Prevented FP16 division-by-zero crashes in Bayar layers and suppressed gradient divergence at spectral nulls. 147 tests (2 skipped) in CI. Paper: working draft, in preparation.

#### [FreightIQ: Carrier Intelligence Agent](https://github.com/yyouretoast/freightiq) · [Demo](https://huggingface.co/spaces/yyouretoast/freightiq)
`LangGraph` `SQLite FTS5` `ChromaDB` `Cross-Encoder` `Streamlit`

**Results (60 queries, 500 synthetic carrier profiles, hybrid + re-rank vs dense-only):** Hit@1 0.317 → 0.717 · MRR 0.446 → 0.781

* LangGraph ReAct agent with sequential tool calls to avoid race conditions. Failover between Qwen 27B models on Groq, with OpenAI and Ollama fallbacks.
* Hybrid retrieval: SQLite FTS5 BM25 plus ChromaDB embeddings fused with RRF, then cross-encoder re-ranking.
* Read-only SQLite lookups with constraint relaxation (safety ratings and hazmat codes are never relaxed). Live FMCSA API compliance checks.
* Loop breaker and 8-message context window. 20 self-written trajectory tests covering prompt injection and SQL mutation attempts.

---

### Open Source

* **[huggingface/transformers](https://github.com/huggingface/transformers/pull/46770)**: Docs fix. Moved SmolLM3 from Multimodal to Text models in `_toctree.yml`. Reviewed and approved by a maintainer.

### Experience

* **AusShop**, Applied AI Engineer (Mar 2026 – present): Built a multi-timezone outreach dispatch engine and Python scraping pipelines syncing 130 Goodwill HQ contacts into HubSpot.
* **Cloudypedia**, API Engineer Intern (Jul – Sep 2025): Deployed 10+ REST/SOAP API proxies on GCP Apigee X for enterprise clients and added Postman/Newman regression suites to CI/CD.

### Stack

PyTorch · OpenCV · LangGraph · LangChain · LangSmith · SQLite (FTS5, WAL) · ChromaDB · Pandas · Selenium · GitHub Actions · GCP · Apigee X · Groq · Ollama
