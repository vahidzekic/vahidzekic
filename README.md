# Hi, I'm Vahid Zekić 👋

**Machine Learning & Computer Vision Engineer** · 15+ years in software engineering · Novi Pazar, Serbia

I build and run production computer vision systems: real-time video pipelines, GPU-accelerated inference and local AI infrastructure, from the multi-GPU hardware up to the application layer. I mostly work in **Python** and **C++**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-vahid--zekic-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vahid-zekic-181488141/)
[![Email](https://img.shields.io/badge/Email-vahidzekic%40gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:vahidzekic@gmail.com)
[![A.I.D.A. website](https://img.shields.io/badge/A.I.D.A.-aida.in.rs-00B37E?logo=googlechrome&logoColor=white)](https://aida.in.rs)
[![A.I.D.A. chat](https://img.shields.io/badge/Try%20A.I.D.A.-chat.aida.in.rs-7C3AED?logo=googlechat&logoColor=white)](https://chat.aida.in.rs)

---

## 🔭 What I work on

- **Real-time video surveillance with computer vision**: recognizes people, faces, vehicles and license plates. It runs on an FFmpeg transcoder server that normalizes mixed camera feeds into standard streams for OpenCV processing.
- **Local AI inference infrastructure**: I design and build multi-GPU nodes (RTX 3090, dual-socket Xeon) for on-premise and edge inference.
- **Retail analytics**: a camera-based system that detects queue congestion and recognizes items in real time for supermarket chains.
- **OCR and document digitization**: image-to-text pipelines for automated data extraction.
- **Agentic AI and LLMs**: local multi-agent environments, RAG document ingestion, and Ollama-based inference.

### 🧠 A.I.D.A. language model family

I build my own language models as edge nodes of the A.I.D.A. ecosystem. Each model runs on local hardware and connects to a cloud gateway over a WebSocket tunnel, so inference doesn't need cloud GPUs.

- **babyLLM (17.2M)**: a small domain-specific language model for pediatric and baby-care advice in Serbian, written from scratch in PyTorch. It uses a Mixture-of-Experts transformer (5 layers, 6 heads, 4 experts with top-2 routing) sized to fit the CPU's cache. Running it on the CPU instead of a Thunderbolt eGPU made inference more than 4× faster. A custom repetition penalty keeps generation from looping.
- **abiLLM (~300M)**: a 24-layer autoregressive transformer written from scratch in **Apple MLX** for Apple Silicon. It uses unified memory without copies and JIT-compiled Metal kernels (`@mx.compile`), with its own BPE tokenizer for Serbian Latin script and a training set scraped from medical and family-health articles.
- **zeinLLM (17.2B)**: a modular vision-language system designed to keep learning without catastrophic forgetting. It combines a frozen 4-bit quantized core, a vision RAG memory (CLIP embeddings in ChromaDB), a curiosity engine that rewards new discoveries, and a LoRA router that hot-swaps skill modules. It takes live camera and microphone input.
- **nanoLLM (3B)**: an autonomous robot rover on an **NVIDIA Jetson Nano**. A 3B vision-language model quantized to 4-bit GGUF runs on-device through llama.cpp. It sees through a camera, hears Serbian speech, remembers places with a FAISS vector memory, and drives DC motors via GPIO using JSON motor commands. It all runs locally in 4 GB of RAM.

## 🚀 Featured projects

| Project | Description |
|---|---|
| [**A.I.D.A.**](https://github.com/vahidzekic/A.I.D.A.) | *Artificially Intelligent Deterministic Agent*: a neuro-symbolic agentic AI framework that combines deep learning with deterministic symbolic logic, built from scratch. Also the basis of a healthcare robot assistant.<br>🌐 [aida.in.rs](https://aida.in.rs) · 💬 [Chat with A.I.D.A.](https://chat.aida.in.rs) |
| [**Ouroboros AI Lab**](https://github.com/vahidzekic/Ouroboros-AI-Lab) | AI infrastructure on a GPU cluster with 288 GB of VRAM, plus a custom Python WebSocket relay that distributes local Ollama inference across networks. |

## 🕰️ The A.I.D.A. journey: 2015 → 2026

A.I.D.A. started as my bachelor's thesis and has been my long-running research platform ever since. Each generation builds on the previous one. The full story is on [**aida.in.rs**](https://aida.in.rs), and you can talk to it at [**chat.aida.in.rs**](https://chat.aida.in.rs).

| Year | Milestone |
|---|---|
| **2015** | **Distributed rover cluster** (B.Sc. thesis): four networked Raspberry Pis. C++ camera nodes do stereo triangulation over raw TCP sockets and send 8 bytes per detection instead of whole frames. A Python master and motor node handle navigation. |
| **2017–2019** | **Face recognition system** (M.Sc. research): a web app with face detection, recognition and tracking, facial expression analysis (CNN), plus speech, vehicle and patient recognition. |
| **2019** | **A.I.D.A. CUDA Core**: YOLOv3 object detection with CUDA, multi-camera surveillance with up to 9 streams, automatic GPU/CPU switching, and Jetson Nano support. Also available as a Docker image. |
| **2024** | **A.I.D.A. M1**: YOLOv8 detection and tracking ported to Apple Silicon, up to 10 IP cameras, with benchmarks. |
| **2026** | **A.I.D.A. language model family**: custom LLMs from 17M to 17B parameters, plus the neuro-symbolic [A.I.D.A.](https://github.com/vahidzekic/A.I.D.A.) agent framework. |
| **2026** | **A.I.D.A. Humanoid OS**: a cognitive operating system for humanoid robots. It covers stereo depth vision, speech in and out, few-shot learning of new objects, reasoning with a local LLM, memory consolidation and curiosity-driven exploration. It runs fully offline, and the whole stack fits in under 300 MB of RAM on a Jetson Nano. Editions exist for RTX/CUDA desktops and Apple Silicon. |

## 📦 Products I've built

| Product | What it does | Stack |
|---|---|---|
| **StoreFlow** | In-store analytics: tracks shoppers' paths on CCTV feeds in real time and shows live camera views with AI overlays and heatmaps. | YOLOv8 · Flask · PostgreSQL · React |
| **eOptika** | ERP for optical stores: patients, prescriptions, frame and lens inventory, sales and finance. Includes a licensing service, auto-updates and a bridge to fiscal and thermal printers. | React · Flask · Docker |
| **KonobarAI / RestOS** | AI restaurant platform: guests order by voice or chat from a digital menu, the kitchen gets live orders, and inventory is linked to recipes. Multi-tenant SaaS. | Flask · PostgreSQL · Socket.IO · GPT-4o · Whisper · TTS |
| **AfterBefore** | A nightlife platform with a mobile app, web client and backend API. | Flutter · React · Flask · PostgreSQL |
| **Work Plus** | Tracks workforce productivity on construction sites, with a mobile app, dashboard and API. | Flutter · React · Flask · PostgreSQL |
| **eOrdinacija** | Patient management and reporting for medical practices. | Flask · JavaScript |

## 📊 Quantitative research

I apply ML to crypto markets and treat it as a scientific experiment, not a get-rich-quick bot.

- **BTC spot trading research log**: 44 tests with a locked holdout set, predictions recorded in advance, and random-selection controls. The honest result so far: the best rule is positive but **not statistically significant** (t < 2), so it stays a research project. The production setup runs as supervised, independent processes with heartbeat monitoring, a capital kill-switch, order-book recording and Telegram control.
- **Futures scalper**: a long/short signal engine for BTC/USDT that combines 9 weighted indicators with an XGBoost + Random Forest ensemble, plus strict risk and liquidation limits.
- **Market data aggregator**: an async pipeline that pulls macro, prediction-market, news and market data at the same time and turns it into model-ready features.

## ⚙️ Systems programming & infrastructure

- **Forensic data recovery**: a 9-layer recovery pipeline for corrupted JPEG and MP4 files from failing drives. Five CPU layers do header patching, binary carving and bitstream repair. Four optional GPU layers use CUDA to brute-force Huffman tables, a small transformer to predict missing marker bytes, a U-Net to rebuild damaged image areas, and bit-shift scanning to realign the data. Each layer only runs if the ones before it failed.
- **VPN Relay**: tunnels TCP traffic over WebSockets through a cloud broker. Agents at each site turn any local service (Ollama, RDP, web servers) into a remote port, without opening ports on the home network.
- **KontrolaNaDaljinu**: a cross-platform remote desktop app. The relay server is written in pure C11 (about 100 KB) and the GUI client is in C++/Qt5. It uses TLS-encrypted TCP+UDP and FFmpeg for screen streaming.
- [**Wahacoin**](https://github.com/vahidzekic/Wahacoin): a proof-of-work cryptocurrency forked from Bitcoin Core v22 (C++, SHA-256), with its own chain parameters and a phased CPU → GPU → ASIC rollout for fair early distribution. Around it I built a REST API and block indexer (PostgreSQL), a block explorer, and web and Flutter wallets.

## 🛠️ Tech stack

- **Computer vision & video:** OpenCV · FFmpeg · GStreamer · video transcoding
- **Deep learning:** PyTorch · TensorFlow
- **GPU & inference:** CUDA · TensorRT · ONNX Runtime · multi-GPU setups · edge inference
- **Generative AI:** Ollama · Open WebUI · RAG · agentic workflows
- **Languages:** Python · C++ · C#/.NET (10 years) · JavaScript
- **Backend & infra:** Flask · Django · REST · PostgreSQL · MySQL · Docker · Linux · Azure · n8n
- **Robotics & simulation:** ROS · PyBullet · PyChrono · OpenAI Gym

## 💼 Experience

- **Senior Python Developer**, State University of Novi Pazar *(2021 – present)*
- **Computer Vision Engineer**, independent projects and consulting *(2015 – present)*
- **Senior C# .NET Developer**, Bayer Business Services GmbH, Leverkusen *(2018 – 2020)*: IAM portal, Omada Identity Suite, CyberArk integration
- **Senior C# .NET Developer**, PATECCO GmbH, Bochum *(2017 – 2018)*: Azure MVC apps, Windows→Linux and Oracle→PostgreSQL migration
- **Senior Developer**, State University of Novi Pazar *(2011 – 2017)*
- **Founder & Software Developer**, ElixNET *(2007 – 2011)*

## 🎓 Education

- **M.Sc. Electrical Engineering & Computer Science**, State University of Novi Pazar *(in progress)*. Thesis: computer vision and custom object detection models.
- **B.Sc. Electrical Engineering & Computer Science**, State University of Novi Pazar. Thesis: real-time object tracking and recognition with OpenCV.

---

🌍 Languages: Serbian (native) · English (B1)
