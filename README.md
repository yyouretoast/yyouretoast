# Yassin Yasser

**Applied AI & Machine Learning Engineer** | Cairo, Egypt  
Specializing in spatial-spectral deep learning systems and deterministic agent orchestration.

[LinkedIn](https://linkedin.com/in/yassinyasser) / [Hugging Face](https://huggingface.co/yyouretoast) / [Email](mailto:yyasso2005@gmail.com)

---

### Featured Systems

#### [Dual-Stream Deepfake Forensics Engine](https://github.com/yyouretoast/deepfake-detection)
`PyTorch` • `ConvNeXt` • `2D FFT` • `Bi-GRU` • `OpenCV` • `Streamlit`  
**Key Results**: 0.8994 Video ROC-AUC • 18.54% EER • 0.8651 Zero-Shot Google DFD AUC • 14.08 ms Latency (RTX 4060)

* **Dual-Stream Architecture**: Couples an ImageNet-pretrained ConvNeXt-Small spatial stream with a 20-channel ResSE spectral tower fed by 9 Spatial Rich Model (SRM) filters, learnable Bayar-Stamm constrained convolution, and 2D Real FFT decomposition.
* **Leakage-Free Partitioning**: Enforced zero source and target actor overlap across train, validation, and test splits by constructing a bipartite actor graph over 99,101 crops (2,248 source videos) and isolating connected components.
* **Artifact Suppression**: Suppressed high-frequency FFT edge leakage by >40 dB by applying a 2D separable Hann cosine tapering window to facial crops aligned via OpenCV YuNet and 5-point LMEDS similarity transforms.
* **Numerical Stability**: Prevented FP16 mixed-precision crashes in Bayar-Stamm layers using signed-sum epsilon flooring; suppressed gradient divergence at spectral nulls via sub-epsilon phase masking.
* **Sequence Modeling**: Processed feature velocity deltas through a 2-layer Bi-GRU with dual-path self-attention, lifting video ROC-AUC to 0.8994 (from a 0.8656 frame-level AUC) and cutting EER to 18.54% across 26,981 held-out test crops (outperforming uniform frame averaging).
* **Generalization & Calibration**: Reached 0.8651 zero-shot AUC on Google DFD and 0.9514 4-fold LOMO macro AUC; reduced Expected Calibration Error by 49.4% (0.1965 → 0.0994) via post-hoc affine Platt scaling fitted on validation split logits.
* **Benchmarks & Deployment**: Profiled end-to-end latency on an RTX 4060 GPU at 14.08 ms (71.0 FPS). Backed by a 147-test pytest suite under GitHub Actions CI, 4 SHA-256 verified checkpoints, a batch CLI, a Streamlit demo, and a 10-page CVPR/IEEE-format research manuscript with automated data parity verification.

#### [FreightIQ — Carrier Intelligence Agent](https://github.com/yyouretoast/freightiq)
`LangGraph` • `SQLite FTS5` • `ChromaDB` • `Cross-Encoder` • `Streamlit`  
**Key Results**: +126% Hit@1 Lift • +75% MRR Lift • 0.31 ms SQL Lookup • 20/20 Security & Trajectory Tests

* **ReAct Agent Routing**: Enforces single-turn sequential tool execution (`parallel_tool_calls=False`) in LangGraph to prevent inter-tool race conditions and argument hallucinations during multi-stage carrier dispatch queries.
* **Sibling Model Failover**: Built thread-safe dynamic failover between Qwen 27B models on Groq with an automated lock, 5-minute self-healing recovery cooldown, and fallbacks to OpenAI and local Ollama instances.
* **Loop & Memory Guardrails**: Implemented a turn-scoped loop breaker detecting cyclic tool calls and an 8-message turn-aligned sliding context window.
* **Two-Stage Hybrid Search**: Fuses SQLite FTS5 BM25 with ChromaDB dense embeddings via Reciprocal Rank Fusion ($k=60$) and Cross-Encoder re-ranking, boosting Hit@1 by 126% (0.317 → 0.717) and MRR by 75% (0.445 → 0.781) over dense-only vector search across a 60-query benchmark on 500 synthetic carrier profiles.
* **Read-Only SQLite Engine**: Enforces filesystem-level read-only access (`mode=ro`), AST query parsing, and automated constraint relaxation on zero-row returns while excluding safety ratings and hazmat codes from relaxation. Resolves deterministic lookups in 0.31 ms.
* **Compliance & Stress Testing**: Integrates live federal FMCSA QCMobile REST API safety gating, an NMFC freight density calculator, and Tavily market intelligence. Passed 100% of 20 self-authored integration scenario tests and executed lock-free reads across 15 concurrent threads on SQLite WAL.

---

### Ecosystem & Open Source

* **[huggingface/transformers](https://github.com/huggingface/transformers)**: Patched model architecture taxonomy misclassifying SmolLM3 under multimodal architectures in official documentation (`_toctree.yml`). Reviewed and merged into `main`.
* **[Hugging Face Hub](https://huggingface.co/yyouretoast)**: Published model weights, evaluation checkpoints, and interactive deployment Spaces for deepfake forensics and carrier intelligence.

---

### Technical Stack

* **Frameworks & Core Tools**: PyTorch, torchvision, OpenCV, Scikit-Learn, SciPy, LangGraph, LangChain, Streamlit
* **Retrieval & Databases**: SQLite (FTS5, WAL Mode), ChromaDB, Cross-Encoders, BM25, Reciprocal Rank Fusion (RRF)
* **Data Engineering & Scripting**: Python, SQL, Bash, BeautifulSoup, Selenium, Pandas, NetworkX, REST APIs
* **Infrastructure & Platforms**: Git, Git LFS, GitHub Actions CI/CD, Google Cloud Platform (GCP), Google Apigee X, Postman, Groq, Ollama, Docker
