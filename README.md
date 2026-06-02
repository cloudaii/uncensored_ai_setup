# 🔒 Portable Uncensored AI (USB)
Run a 100% private, offline AI assistant directly from any USB drive. No internet required after setup. Zero data footprints left behind.
Works on **Windows**, **Mac**, and **Linux**.
---
## ⚡ Available Models

| # | Model | Size | Label | Best For |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **NemoMix Unleashed 12B** | ~7.0 GB | 🔓 UNCENSORED | ⭐ Best overall quality |
| 2 | **Dolphin 2.9 Llama 3 8B** | ~4.9 GB | 🔓 UNCENSORED | Balanced uncensored |
| 3 | **Mistral 7B Instruct v0.3** | ~4.1 GB | 🔒 STANDARD | Reasoning & coding |
| 4 | **Qwen 2.5 7B Instruct** | ~4.7 GB | 🔒 STANDARD | Multilingual tasks |
| 5 | **Llama 3.2 3B Instruct** | ~2.0 GB | 🔒 STANDARD | Fast on old PCs |
| 6 | **Phi-3.5 Mini 3.8B** | ~2.2 GB | 🔒 STANDARD | Light reasoning |
| C | **Custom GGUF** | Varies | 🎨 CUSTOM | Any HuggingFace link |

> **🔓 UNCENSORED:** No filters. | **🔒 STANDARD:** Normal safety filters apply.
---
## 🚀 Quick Setup
### Requirements
* **USB Drive:** $\ge$ 16 GB (32 GB+ recommended) formatted as **exFAT**.
* Internet connection (for initial downloads only).
### Installation Steps
1. **Copy** all repository files to your USB drive root.
2. **Run the installer** from the USB:
   * **Windows:** Double-click `install.bat`
   * **Mac/Linux:** Run `bash install.sh`
3. **Select models** from the on-screen menu prompt.
4. **AnythingLLM Window:** When prompted, click **Browse** and set the installation path to the `anythingllm` folder on your USB.
### Advanced Tweaks
* **Manual Download:** If a download fails, put the `.gguf` file directly into `models/` and restart the installer.
* **Context Size:** Edit `anythingllm_data/storage/.env` and modify `OLLAMA_MODEL_TOKEN_LIMIT=4096` to your choice (e.g., `8192`), then restart.
---
## ▶️ How to Run
### Windows
* Launch **`start-windows.bat`**. (Auto-wipes path cache when changing PCs).
* Select models inside the UI: **Settings → LLM**.
* Keep the terminal open; press any key to safely close.
### Mac
* Launch **`start-mac.command`**. (Downloads engine on first run, ~2 min).
* Press **Enter** in the terminal window to safely close.
### Linux
Terminal copy-paste:
```bash
chmod +x start-linux.sh preflight-check.sh install.sh install-core.sh
```

```
bash preflight-check.sh
```

1. Run the AnythingLLM AppImage from the `anythingllm/` folder.
2. Press **Enter** in the terminal window to safely close when finished.

---

## 📁 Drive Structure & Requirements

```text
USB Drive/
├── install.bat / install.sh   ← Installer files
├── start-windows.bat          ← Windows launcher
├── start-mac.command          ← Mac launcher
├── start-linux.sh             ← Linux launcher
├── ollama/ / models/          ← AI engine & downloaded GGUF files
└── anythingllm/ / _data/      ← Interface app & private chat logs
```

## Hardware Requirements
Depending on the model size you choose to run, ensure your system meets the following minimum or recommended hardware specifications.

| Configuration | Recommended Model | Minimum RAM | Recommended RAM | Hardware Speed / Performance |
| :--- | :--- | :--- | :--- | :--- |
| **Lightweight** | 3B to 3.8B models | **4 GB** | 16 GB | Runs acceptably on standard CPU |
| **Recommended** | 7B to 12B models | **8 GB** | 32 GB | 10–30s generation latency |

> ⚠️ **Note:** For optimal performance and lower latency, running models on a dedicated GPU is highly recommended, though lightweight models are fully capable of running on CPU-only setups.


## Essential Rules

• Portability: You must change the AnythingLLM path to your USB directory during setup.


• Errors: If switching PCs causes a "JavaScript Error", close it and rerun the launcher script.


• Eject: Always safely eject the USB drive before physical removal to prevent corruption.

