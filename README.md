# uncensored_ai_setup

# DME — Portable Uncensored AI 🔒
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
A completely private, portable, and uncensored AI assistant configured to run 100% locally from a USB flash drive. Zero internet connection required after the initial setup. No data ever leaves your drive. Cross-platform compatibility for Windows, macOS, and Linux.
Now featuring **multi-model support**! Select from 6 pre-configured AI models or integrate your own custom builds.
📺 **[Watch the Complete Video Tutorial Here](your-video-link-here)**
---
## ⚡ Supported Models
During the setup process, an interactive menu will allow you to select and deploy your preferred model(s):

| # | Model Name | File Size | Classification | Optimal Use Case |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **NemoMix Unleashed 12B** | ~7.0 GB | 🔓 UNCENSORED | ⭐ *Recommended* — Premier uncensored quality |
| **2** | **Dolphin 2.9 Llama 3 8B** | ~4.9 GB | 🔓 UNCENSORED | Classic versatile, unfiltered performance |
| **3** | **Mistral 7B Instruct v0.3** | ~4.1 GB | 🔒 STANDARD | Exceptional logical reasoning & programming |
| **4** | **Qwen 2.5 7B Instruct** | ~4.7 GB | 🔒 STANDARD | Robust multilingual processing capabilities |
| **5** | **Llama 3.2 3B Instruct** | ~2.0 GB | 🔒 STANDARD | Ultra-lightweight — optimized for legacy hardware |
| **6** | **Phi-3.5 Mini 3.8B** | ~2.2 GB | 🔒 STANDARD | Compact profile with strong analytical output |
| **C** | **Custom GGUF** | Varies | 🎨 CUSTOM | Load any compatible HuggingFace model |

> 🔓 **UNCENSORED:** Completely unfiltered outputs; bypasses standard guardrails.  
> 🔒 **STANDARD:** Operates under standard safety guidelines and alignment.
---
## 💾 Hardware & Storage Allocation Guide

| Selected Presets | Minimum Storage | Recommended Storage |
| :--- | :--- | :--- |
| **1 Lightweight Model (3B/3.8B)** | 16 GB | 16 GB |
| **1 Recommended Model (NemoMix 12B)** | 16 GB | 32 GB |
| **2 to 3 Models Co-existing** | 32 GB | 64 GB |
| **Full Suite (All 6 Presets ~25 GB)** | 64 GB | 64 GB |

---
## 🚀 Initial Environment Setup (One-Time Only)
### Prerequisites
* A USB flash drive with a minimum of 16 GB free space (32 GB+ highly recommended).
* **Important:** Format the USB drive file system to **exFAT** for universal compatibility (Windows, Mac, Linux).
* An active internet connection (required solely for initial asset downloads).
### Implementation Steps
1. Clone or download this repository and transfer **all** files directly into the root directory of your USB drive.
2. Launch the deployment script:
   * **Windows:** Double-click `install.bat`
3. Select your desired AI engine(s) via the interactive console prompt.
4. **AnythingLLM Guided Configuration:**
   * The AnythingLLM installer UI will launch automatically.
   * ⚠️ **CRITICAL:** When prompted for the *Install Location*, select **Browse** and point the target path explicitly to the `anythingllm` folder located on your USB drive. 
5. Allow the installation wizard to complete, then close the setup window. 
Your self-contained portable environment is now operational!
### Troubleshooting Interrupted Downloads
If a specific network drop causes a model download to fail, the installer will automatically attempt a retry. If it completely fails:
1. Extract the direct HuggingFace download URL displayed in the terminal logs.
2. Manually download the `.gguf` file via your browser.
3. Drop the downloaded `.gguf` asset directly into the `models/` directory on your USB.
4. Restart `install.bat` — it will immediately index your manual asset and skip the download phase.
---
## 🔧 Advanced Configurations
### 🔄 Expanding Your Model Library
To add extra models post-installation, simply run `install.bat` again. The system automatically scans your environment and will only fetch newly requested models while retaining current data intact.
### 🎨 Custom HuggingFace Integrations
To deploy a model outside our curated presets, select **Option C** during installation and paste the direct link to any valid `.gguf` payload from HuggingFace.
### 🗄️ Adjusting Ollama Token Limits & Context Size
The framework initializes with a balanced 4K (4096) token limit designed for maximum performance across general hardware configurations. To scale this capacity:
1. Navigate to `anythingllm_data/storage` on your USB drive.
2. Open the `.env` configuration file using any text editor.
3. Locate `OLLAMA_MODEL_TOKEN_LIMIT=4096` and update the value (e.g., `8192` for an 8K context window).
4. Save adjustments and restart your environment using the OS-specific launcher script (`start-windows.bat`, `start-mac.command`, or `start-linux.sh`).
> 📝 **Note:** Running `install.bat` or `install.sh` again will reset this environment property to `4096`. On macOS, recycling the environment through `start-mac.command` preserves your modified `.env` values seamlessly.
---
## ▶️ Execution & Daily Usage
### 🪟 Windows Environments
1. Double-click `start-windows.bat` on your USB drive.
   * *Improved Portability:* The execution layer dynamically flushes outdated path caches across host devices, completely eliminating standard "JavaScript runtime errors."
2. The AnythingLLM interface will launch seamlessly. 
3. **Model Selection:** Head to `Settings` ➡️ `LLM` ➡️ select your downloaded model from the dropdown.
4. Keep the host command prompt window active while interacting with the AI. 
5. To close down your session safely, focus on the terminal and press any key.
### 🍎 macOS Environments
1. Double-click `start-mac.command` from the USB directory.
   * *First Launch:* The wrapper will spend ~2 minutes provisioning the local macOS core.
2. The AnythingLLM chat ecosystem will initialize automatically.
3. To safely unmount resources, tap `ENTER` inside the terminal window.
### 🐧 Linux Environments
1. Initialize a terminal terminal path matching your USB root folder.
2. Modify file execution permissions and launch the diagnostic checker:
```bash
   chmod +x start-linux.sh preflight-check.sh install.sh install-core.sh
```
```
   bash preflight-check.sh
```

3. The preflight script automatically builds   system checks and launches setup.

4. Navigate inside the anythingllm subdirectory and execute the AppImage file.

5. Select your engine via Settings ➡️ LLM.

6. Terminate runtime sessions cleanly by pressing Enter inside the active terminal.

## 🔐 Privacy Framework

• Zero Footprint: All conversational history, parameters, and application configurations are locked to the USB drive. No data writes to the host machine's drive.
• No Host Alterations: Zero Windows Registry modifications, local system folder mutations, or trace files left behind.
• Air-Gapped Operation: Operates flawlessly in full-isolation mode without requiring network access.
• No Tracking: Features zero telemetry, no third-party cloud handshakes, and completely disabled tracking.


