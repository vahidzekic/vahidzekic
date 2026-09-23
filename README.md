# Hi, I'm Vahid Zekić 👋

**Machine Learning & Computer Vision Engineer** · 15+ years in software engineering · Novi Pazar, Serbia

I build and run production computer vision systems: real-time video pipelines, GPU-accelerated inference and local AI infrastructure, from the multi-GPU hardware up to the application layer. I mostly work in **Python** and **C++**.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-vahid--zekic-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vahid-zekic-181488141/)
[![Email](https://img.shields.io/badge/Email-vahidzekic%40gmail.com-EA4335?logo=gmail&logoColor=white)](mailto:vahidzekic@gmail.com)

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
| [**A.I.D.A.**](https://github.com/vahidzekic/A.I.D.A.) | *Artificially Intelligent Deterministic Agent*: a neuro-symbolic agentic AI framework that combines deep learning with deterministic symbolic logic, built from scratch. Also the basis of a healthcare robot assistant. |
| [**Ouroboros AI Lab**](https://github.com/vahidzekic/Ouroboros-AI-Lab) | AI infrastructure on a GPU cluster with 288 GB of VRAM, plus a custom Python WebSocket relay that distributes local Ollama inference across networks. |

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
