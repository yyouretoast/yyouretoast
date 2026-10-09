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

Fuses ConvNeXt-Small spatial embeddings with SRM/Bayar-Stamm 2D Real FFT spectral embeddings and a Bi-GRU video sequence head. Identity-disjoint splits via graph connected-component partitioning (zero actor overlap). Calibrated via SciPy L-BFGS-B temperature scaling (T*=4.288, ECE 0.0785). 0.8719 AUC, 0.8818 F1 on a 13,444-crop held-out test set — 142-test pytest suite.

### FreightIQ
[Repo](https://github.com/yyouretoast/freightiq) · [Demo](https://huggingface.co/spaces/yyouretoast/freightiq)
LangGraph agent routing freight inquiries between deterministic SQLite (<1 ms), hybrid retrieval (FTS5 BM25 + ChromaDB fused via RRF k=60, neural Cross-Encoder re-ranked), and live FMCSA safety verification. Two-stage neural re-ranking lifts **Hit@1 0.317→0.717 (+126%), Hit@5 0.683→0.883, and MRR 0.445→0.781** over dense retrieval on a 60-query benchmark. Turn-scoped loop breaker and read-only URI enforcement verified across a 20-scenario trajectory evaluation suite.

---

## Open Source
[huggingface/transformers #46770](https://github.com/huggingface/transformers/pull/46770) — fixed a doc bug miscategorizing SmolLM3 under Multimodal models.

---

## Now
Writing up the deepfake detector's leakage-fix and generalization findings for an arXiv preprint.

---

*Email / Hugging Face in [LinkedIn](https://www.linkedin.com/in/yassinyasser/) contact info.*
