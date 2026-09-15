# Yassin Yasser
Applied AI Engineer & CS Student — Cairo, Egypt

Building agentic AI systems and retrieval pipelines. Previously API Engineering Intern at Cloudypedia (GCP Apigee X, REST/SOAP).

**[→ Full profile & experience on LinkedIn](https://www.linkedin.com/in/yassinyasser/)**

---

## Stack

| Area | Tools |
|---|---|
| ML / CV | PyTorch, OpenCV, SciPy |
| Agents / Retrieval | LangGraph, ChromaDB, SQLite |
| Infra | Docker, GCP, Streamlit |

---

## Projects

### Dual-Stream Deepfake Detector
[Repo](https://github.com/yyouretoast/deepfake-detection) · [Demo](https://huggingface.co/spaces/yyouretoast/deepfake-detector)

Fuses ConvNeXt-Small spatial embeddings with SRM/Bayar-Stamm 2D FFT spectral embeddings via sigmoid residual gating. Identity-disjoint train/val/test splits via graph connected-component partitioning (zero actor overlap). Calibrated via SciPy L-BFGS-B temperature scaling (T\*=4.288, ECE 0.0050). **0.8248 AUC, 0.8627 F1** on a 13,444-crop held-out test set — 132-test pytest suite.

### FreightIQ
[Repo](https://github.com/yyouretoast/freightiq) · [Demo](https://huggingface.co/spaces/yyouretoast/freightiq)

LangGraph agent routing freight carrier queries between exact SQL, hybrid retrieval (SQLite FTS5 + ChromaDB via Reciprocal Rank Fusion, cross-encoder reranked), and live FMCSA safety verification. Hybrid reranking lifts **Recall@1 0.30→0.70, Recall@5 0.667→0.867, MRR 0.429→0.764** over dense-only retrieval on a 60-query benchmark — though plain SQL still wins on structured queries.

---

## Open Source
[huggingface/transformers #46770](https://github.com/huggingface/transformers/pull/46770) — fixed a doc bug miscategorizing SmolLM3 under Multimodal models.

---

## Now
Writing up the deepfake detector's leakage-fix and generalization findings for an arXiv preprint.

---

*Email / Hugging Face in [LinkedIn](https://www.linkedin.com/in/yassinyasser/) contact info.*
