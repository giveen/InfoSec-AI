# 📥 Picking and Downloading a Model in LM Studio

LM Studio makes it easy to browse, download, and run large language models (LLMs) locally.  
Follow these steps to select the right model for your workflow:

---

## 1. Open the Model Tab
- Launch LM Studio.
- Navigate to the **Models** tab in the sidebar.

---

## 2. Browse Available Models
- LM Studio provides a curated list of popular open‑source models (e.g., Llama, Mistral, Qwen, Gemma, Phi).
- Use the **search bar** to quickly find a specific model.

---

## 3. Check Model Details
For each model, LM Studio shows:
- **Model size** (e.g., 7B, 13B, 30B parameters).
- **Quantization formats** (e.g., Q4_K_M, Q8_0) to balance speed vs accuracy.
- **VRAM requirements** (important for GPU compatibility).
- **Tags** (chat, instruct, reasoning, etc.).
- **Tool Capable** (look for models that support tools).

---

## 4. Download the Model
- Click **Download** next to the desired model.
- LM Studio will fetch the model weights and store them locally.
- Progress is shown in the download manager.

---

## 5. Load and Run
- Once downloaded, click **Load** to start the model.
- LM Studio will automatically configure GPU acceleration (CUDA 12/13 supported).
- You can now chat with the model or connect it via the local API (`http://127.0.0.1:1234/v1`).

---

## ✅ Tips
- **Match VRAM to model size**:  
  - 7B models → ~8 GiB VRAM  
  - 13B models → ~16 GiB VRAM  
  - 30B models → ~32 GiB VRAM
- **Use quantized formats** (Q4/Q8) for faster inference and lower memory usage.
- **Experiment**: Try multiple models to benchmark reasoning, speed, and accuracy.

---

📖 Full reference: [LM Studio Docs — Downloading Models](https://lmstudio.ai/docs/app/basics/download-model)
