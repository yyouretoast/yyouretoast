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
[Repo](https://github.com/yyouretoast/deepfake-detection) · [Demo](https://huggingface.co/spaces/yyouretoast/deepfake-detector) · [Preprint](https://github.com/yyouretoast/deepfake-detection/tree/main/manuscript)

Couples ConvNeXt-Small with a 20-channel SRM/Bayar-Stamm 2D Real FFT spectral tower via dynamic SNR-adaptive gating, Hann boundary tapering, and a 2-layer Bi-GRU video sequence head. Evaluated on strictly disjoint graph-partitioned splits (zero actor/pair overlap across 99,101 crops). Achieves **0.8994 video ROC-AUC** (0.8517 F1, 18.54% EER) and **0.8656 frame ROC-AUC** on a 26,981-crop held-out test set, including 0.8651 zero-shot AUC on Google DFD. Affine Platt scaling calibrates probabilities ($T_{\text{eff}}=3.593$, ECE cut 0.1965→0.0994) for Bayesian 3-zone operational triage. Real-time GPU inference runs at **71.0 FPS** (14.08 ms), validated by a 147-test pytest suite.

### FreightIQ
[Repo](https://github.com/yyouretoast/freightiq) · [Demo](https://huggingface.co/spaces/yyouretoast/freightiq)

LangGraph agent routing freight inquiries between deterministic SQLite (<1 ms), hybrid retrieval (FTS5 BM25 + ChromaDB fused via RRF k=60, neural Cross-Encoder re-ranked), and live FMCSA safety verification. Two-stage neural re-ranking lifts **Hit@1 0.317→0.717 (+126%), Hit@5 0.683→0.883, and MRR 0.445→0.781** over dense retrieval on a 60-query benchmark. Turn-scoped loop breaker and read-only URI enforcement verified across a 20-scenario trajectory evaluation suite.

---

## Open Source
[huggingface/transformers #46770](https://github.com/huggingface/transformers/pull/46770) — fixed a doc bug miscategorizing SmolLM3 under Multimodal models.

---

## Now
Finalizing arXiv submission for the dual-stream deepfake detector preprint on disjoint graph partitions and SNR-adaptive frequency gating.

---

*Email / Hugging Face in [LinkedIn](https://www.linkedin.com/in/yassinyasser/) contact info.*
