# C++ AI Inference Engine

A custom, memory-efficient inference engine built to serve and stream quantized local language models. Rather than relying on external APIs, this project implements a full-stack AI deployment pipeline from the ground up, bridging low-level systems programming with a modern web interface.

### Architecture Overview
* **C++ Core (GGML):** Handles tensor operations, matrix multiplications, and memory-mapped model loading for high-throughput token generation.
* **Python Middleware (Pybind11 & FastAPI):** Wraps the C++ computational graph and exposes it via REST endpoints, utilizing Server-Sent Events (SSE) for real-time token streaming.
* **Frontend UI (React & TailwindCSS):** A modern, responsive chat interface that consumes the SSE stream and renders markdown dynamically as tokens are generated.