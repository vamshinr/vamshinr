# Hi, I'm Vamshi Nagireddy 👋

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vamshinr)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:vamshi.knagireddy@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://vamshinr-blog.netlify.app/)

## 🎯 Research Interests
I'm passionate about building AI systems that are fast, correct, and actually know what they're doing. Currently working at Intel on performance optimization and AI workload acceleration — and building at the intersection of LLM inference, knowledge systems, and agent infrastructure.

## 🔬 Featured Projects

### 🧠 [BrainOS — Multi-Agent Knowledge Graph for AI Agents](https://github.com/vamshinr/BrainOS)
The missing layer between scattered company knowledge and AI agents.
- **What it does:** 4-agent pipeline (Ingestion → Structuring → Execution → Feedback) that extracts atomic knowledge units from heterogeneous sources (Slack, PDFs, DOCX, architecture diagrams) into a reconciled directed knowledge graph
- **Core primitive:** Reconciliation engine with supersession, conflict detection, and temporal scoring — stale facts invalidated at ingest, not at query time
- **Retrieval:** 5-signal hybrid (vector + BM25 + entity + graph + multimodal) with reciprocal rank fusion and a verifier-revision loop on every answer
- **Model serving:** Open-weight 70B text + 7B VLM co-resident on a single AMD MI300X (192 GB HBM3) from scratch via vLLM with per-task model routing
- **Output:** Per-department `SKILLS.md` agent rules loadable directly into Claude Code, Cursor, or any LLM agent
- **Tech Stack:** Python, FastAPI, ChromaDB, Next.js 15, vLLM, LLaVA, Llama-3.1-70B, ROCm, AMD MI300X

### ⚡ [KVForge — Profile-Guided Kernel Optimization for LLM Inference](https://github.com/vamshinr/KVForge)
Amdahl-driven kernel optimization for production LLM inference.
- **What it does:** Profiles a real LLM end-to-end, ranks kernels by their contribution to total latency, and runs an iterative agent loop generating optimized Triton candidates gated by a 5-stage correctness harness
- **Key insight:** Treats kernel selection as a search problem over inference-specific shapes (memory-bound decode, KV cache layout) rather than training graphs
- **Correctness first:** Smoke test → shape sweep (8 configs × 3 dtypes) → numerical stability → determinism → non-power-of-2 edges — before any throughput measurement
- **Targets:** RMSNorm, RoPE, fused softmax, paged attention — the kernels vendor libraries leave on the table
- **Tech Stack:** Python, Triton, PyTorch, torch.profiler, CUDA/ROCm

### 🔐 [VaultASR - High-Performance Local Speech Intelligence](https://github.com/vamshinr/VaultASR)
Local, private speech-to-text pipeline with advanced diarization and hardware acceleration.
- **Key Features:** Multi-speaker diarization, Silero VAD v5, CoreML/Metal GPU acceleration, multi-format exports
- **Tech Stack:** C++, whisper.cpp, ONNX Runtime, Metal/CoreML, FFmpeg
- **Impact:** 100% offline transcription on Apple Silicon, hours of audio in minutes

### 🤖 [PEARL - Proactive Execution and Adaptive Reasoning Loop](https://github.com/vamshinr/pearl-agent-framework)
Autonomous AI agent with cognitive architecture for reliable code generation.
- **Key Features:** Dynamic task decomposition, constrained decoding, experience-based learning
- **Tech Stack:** Python, Gemini API, ChromaDB, LangChain

### 💊 [DrugGuard - LLM-Powered Pharmacovigilance System](https://github.com/vamshinr/RAG-GraphRAG-for-Pharmacovigilance-LLMs)
Comparative study of RAG vs GraphRAG for medical information retrieval.
- **Dataset:** 19,520 drug-side effect associations across 976 drugs
- **Innovation:** Graph-based knowledge representation for safety-critical medical AI

## 💼 Professional Experience

### Software Engineer @ Intel Corporation (2023-Present)
- 🔧 Performance optimization for AI/ML workloads (MLPerf, Geekbench, CrossMark)
- 🔍 Binary-level performance analysis and bottleneck detection
- 🚀 25% performance improvement through dynamic hardware tuning
- 🧪 80% test coverage with comprehensive testing frameworks

### Machine Learning Engineer @ Phenom (2019-2021)
- 🤗 BERT-based NLP models for document understanding (95% accuracy)
- 📊 End-to-end ML pipelines with MLFlow
- 🔄 Real-time data processing with Kafka and Elasticsearch

### Graduate Research Assistant @ CSU Sacramento (2023)
- 🎥 Multimodal AI for video understanding (71% accuracy, 35% improvement)
- 📈 Financial NLP analysis on 5,000+ SEC filings
- 📝 Master's thesis on graph-based recommendation systems

## 🛠️ Technical Skills

**Languages:** Python • C++ • C • Go • Java • Shell Scripting  
**ML/AI:** PyTorch • TensorFlow • Transformers • CUDA • ROCm • ONNX • MLIR • Triton  
**Inference:** vLLM • TensorRT-LLM • OpenVINO • quantization • RAG • kernel optimization  
**Tools:** Docker • Kubernetes • Git • CMake • LLVM/Clang • GDB  
**Data:** SQL • NoSQL • Elasticsearch • Kafka • Neo4j • ChromaDB

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=vamshinr&show_icons=true&theme=dark)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=vamshinr&layout=compact&theme=dark)

## 🎓 Education

**M.S. Computer Science** - California State University, Sacramento (GPA: 3.7/4.0)  
**Thesis:** [Job Recommendation System with NoSQL Databases](https://scholars.csus.edu/esploro/outputs/graduate/Job-recommendation-system-with-NoSQL-databases/99258056363901671)

## 📫 Let's Connect!

- 📧 Email: vamshi.knagireddy@gmail.com
- 💼 LinkedIn: [linkedin.com/in/vamshinr](https://linkedin.com/in/vamshinr)
- 📱 Phone: +1 (916) 707-2957

---
*"The bottleneck is never where you think it is — profile first, optimize second."*
