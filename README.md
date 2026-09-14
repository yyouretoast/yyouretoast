# Yassin Yasser
Applied AI Engineer & CS Student | Cairo, Egypt

Applied AI Engineer building LLM agent pipelines integrated with CRM systems. Previously API Engineering Intern at Cloudypedia, working on GCP Apigee X REST/SOAP APIs.

[LinkedIn](https://www.linkedin.com/in/yassinyasser/) | [Email](mailto:yyasso2005@gmail.com) | [Hugging Face Profile](https://huggingface.co/yyouretoast)

---

## Tech Stack
PyTorch, OpenCV, SciPy, LangGraph, ChromaDB, SQLite, Docker, GCP, Streamlit

---

## Projects

### Dual-Stream Deepfake Detector
[GitHub Repo](https://github.com/yyouretoast/deepfake-detection) | [Live Demo](https://huggingface.co/spaces/yyouretoast/deepfake-detector)

- **Architecture**: Fuses ConvNeXt-Small spatial embeddings with SRM + Bayar-Stamm 2D Real FFT spectral embeddings via a sigmoid residual gate.
- **Identity Splitting**: Graph connected-component partitioning (`networkx.Graph`) over actor IDs to enforce 0% identity overlap across train/val/test splits.
- **Calibration & Interpretability**: SciPy L-BFGS-B temperature scaling ($T^*=2.2018$, ECE = 0.0195) paired with an on-demand 4-panel Grad-CAM diagnostic engine.
- **Metrics & Testing**: 0.9883 test AUC [95% CI 0.9869–0.9896], 0.9759 F1-score, verified by a 132-test pytest suite.

### FreightIQ
[GitHub Repo](https://github.com/yyouretoast/freightiq) | [Live Demo](https://huggingface.co/spaces/yyouretoast/freightiq)

- **Two-Stage Retrieval Engine**: Fuses ChromaDB dense vector search with SQLite FTS5 BM25 via Reciprocal Rank Fusion, then reranks with a pretrained cross-encoder (`ms-marco-MiniLM-L-6-v2`) for carrier dispatch ranking.
- **LangGraph Multi-Tool Agent**: Autonomous tool-calling agent routing between SQL queries, semantic vector search, and density-based NMFC freight class calculations.
- **Guardrails & Resilience**: Connection-level read-only SQLite isolation, SELECT-only SQL validation, and exponential backoff retry wrappers for LLM rate limits.
- **Benchmarked Retrieval**: On a 60-query benchmark, hybrid reranked search hits 0.700 Recall@1 / 0.867 Recall@5 / 0.764 MRR vs. 0.300/0.667/0.429 for dense-only retrieval.

---

## Open Source

### [huggingface/transformers](https://github.com/huggingface/transformers/pull/46770)
- Fixed documentation bug miscategorizing SmolLM3 under Multimodal models in `_toctree.yml`. Merged into `huggingface:main`.
