# Introduction

This home lab is designed to provide a reproducible and secure environment for experimenting with artificial intelligence in cybersecurity. The lab combines penetration testing workflows with local large language model (LLM) orchestration, enabling controlled experiments in automation, benchmarking, and agent‑driven infosec tasks.

The foundation of the lab is a high‑end desktop running **Linux Mint 22.2 Zara (Ubuntu 24.04 base)**, equipped with an **Intel Core Ultra 9 285K CPU**, **256 GiB ECC RAM**, and an **NVIDIA GeForce RTX 5090 GPU with 32 GiB VRAM**. Within this environment, a **virtual machine running Kali Linux** is used for penetration testing and agent orchestration, while **LM Studio** is installed locally on the host system to serve and manage LLMs.

At the core of the orchestration is **CAI (Cybersecurity AI)**, an open‑source framework designed to benchmark, evaluate, and automate infosec workflows. By integrating CAI with LM Studio inside the Kali VM, the lab enables end‑to‑end testing: from model selection and benchmarking to agent‑driven exploitation and reporting.

This setup is guided by three principles:  
- **Reproducibility**: Every workflow is documented and benchmarked for future contributors.  
- **Security**: Experiments are isolated in controlled environments to prevent unintended exposure.  
- **Transparency**: Commit history, environment variables, and benchmark tables ensure traceability of every change.

The following sections outline the step‑by‑step process: setting up Kali, installing LM Studio, selecting models, running CAI benchmarks, configuring environment variables, and orchestrating agents for practical infosec tasks.



# ⚙️ Home Lab Core Specs

| Component | Details |
|-----------|---------|
| **CPU**   | Intel Core Ultra 9 285K (Arrow Lake, 24 cores, up to ~5.4 GHz, 36 MiB L3 cache) |
| **GPU**   | NVIDIA GeForce RTX 5090 — 32 GiB VRAM (CUDA‑accelerated, Vulkan 1.3, OpenGL 4.6, driver 580.95.05) |
| **RAM**   | 256 GiB DDR5 ECC (approx. 251 GiB available) |
| **Storage** | NVMe0: WD Black SN850P 1 TB (system) <br> NVMe1: WD Black SN850P 8 TB (data) <br> **Total**: 8.19 TiB |
| **CUDA Toolkits** | CUDA 12.8 (TensorFlow compatibility) <br> CUDA 13.0 (PyTorch + future frameworks) |
