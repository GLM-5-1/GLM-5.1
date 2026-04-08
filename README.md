# GLM-5.1 Lightweight Installer

<div align="center">
<img src=resources/logo.svg width="15%"/>
</div>

Welcome to the **GLM-5.1 Lightweight Installer** repository — a universal tool for running one of the most powerful open-source language models in the world right on your device, in a single click.

## 💡 Project Concept: Your Personal AI Engineer Without the Pain and Setup

**GLM-5.1 (744B parameters)** is a revolution in the field of autonomous programming and agentic systems. But until today, using it required server hardware worth tens of thousands of dollars and complex environment setup.

**We solved this problem.** Why do you need this installer right now?

  * **Zero-Setup:** No terminals, Python dependencies, or version conflicts. Download the `.exe` — launch the chat.
  * **Access to Enterprise Power:** You get enterprise-grade intelligence for writing code, analyzing logs, and autonomous work, optimized for modern high-performance workstations.
  * **Flexibility:** You choose what is more important — the ultimate power of the 744-billion-parameter model via the cloud, or complete privacy and autonomy of running it locally on your hardware.

Our installer combines a powerful C++ engine and a beautiful UI so you can focus on tasks, not on configuring the environment.

-----

## 🛠 Core Features & Capabilities of GLM-5.1

![bench_51](resources/bench_51.png)

Unlike standard conversational AI, GLM-5.1 is built as a specialized "virtual engineer" for complex, multi-step tasks. Here is what it brings to your workstation:

  * **Long-Term Autonomy (Up to 8 Hours):** It doesn't just generate code snippets; it handles the entire software development lifecycle. Give it a complex task, and it can autonomously plan, write code, run tests, and debug for hours without human intervention.
  * **Massive 200K Context Window:** Feed it entire code repositories (NL2Repo workflow), massive API documentations, or heavy datasets. It understands your whole project architecture, not just isolated files.
  * **Self-Reflection & Auto-Debugging Loop:** If a test fails or the code crashes, GLM-5.1 does not give up. It reads the error logs, rolls back to its previous steps, adjusts its strategy, and finds a working workaround.
  * **Deep Environment Integration:** It acts as a true AI agent capable of executing real terminal commands, running scripts, and utilizing thousands of developer tools in a single prompt (fully compatible with Claude Code and OpenClaw).
  * **Algorithmic Optimization:** Proven to excel in complex machine learning optimization tasks (SWE-Bench Pro & KernelBench Level 3), the model can iteratively refactor your code to achieve performance boosts that surpass standard auto-compilers.

![bench](resources/bench.png)

-----

## ⚙️ Technologies Under the Hood

At the core of our local execution is a custom build of **`llama.cpp`**. This guarantees:

  * Maximum performance and resource utilization of modern hardware (NVIDIA CUDA, AMD ROCm, Apple Metal).
  * Intelligent load distribution with mandatory offloading of heavy model layers to a discrete graphics card.
  * Support for GGUF formats for extreme compression without critical loss of logic.

-----

## 🚀 Two Modes of Operation: Choose Your Path

During installation, you can choose one of two operation modes. You can always switch between them in the application settings.

### Option 1: Cloud-Hybrid (Full 744B Version)

*Ultimate power for complex agentic tasks without extreme load on your PC.*

  * **How it works:** The UI runs locally, but all heavy computations (inference) take place on our servers via a built-in API. You interact with the full version of the GLM-5.1 model (744 billion parameters, of which 44B are active per token).
  * **Requirements:** A modern mid-to-high-end PC, a stable high-speed internet connection.
  * **Conditions:** Absolutely free. To protect our servers from overloads, dynamic rate limits apply to the number of requests per hour.

### Option 2: Local Quantized (Compressed Offline Version)

*Complete privacy, zero ping, and independence from the internet.*

  * **How it works:** We use an extremely compressed (quantized) and partially distilled version of GLM-5.1 in GGUF format. The model is processed locally by the `llama.cpp` engine with a strong emphasis on GPU acceleration.
  * **Requirements:** 16 to 32 GB of system RAM. A high-end or upper-mid-range discrete graphics card (e.g., NVIDIA RTX 3080/4070 or AMD RX 6800/7800 and above) with sufficient VRAM is **strictly mandatory**.
  * **Conditions:** Works without the internet, with no limits, and all your data physically never leaves your workstation.

-----

## 🚀 Two Modes of Operation: Choose Your Installer

We provide two separate installers tailored to your specific hardware and privacy needs. You can choose which version to download from our repository.

### Option 1: [Cloud-Hybrid Installer](../../releases)
*Ultimate power for complex agentic tasks without extreme load on your PC.*

* **How it works:** The UI runs locally, but all heavy computations (inference) take place on our servers via a built-in API. You interact with the full version of the GLM-5.1 model (744 billion parameters).
* **Requirements:** A modern mid-to-high-end PC, a stable high-speed internet connection.
* **Conditions:** Absolutely free. To protect our servers from overloads, dynamic rate limits apply to the number of requests per hour.

### Option 2: [Local Quantized Installer](../../releases)
*Complete privacy, zero ping, and independence from the internet.*

* **How it works:** We use an extremely compressed (quantized) and partially distilled version of GLM-5.1 in GGUF format. The model is processed entirely on your machine using the `llama.cpp` engine. 
* **Requirements:** 16 to 32 GB of system RAM. A high-end or upper-mid-range discrete graphics card (e.g., NVIDIA RTX 3080/4070 or AMD RX 6800/7800 and above) with sufficient VRAM is **strictly mandatory**.
* **Conditions:** Works without the internet, with no limits, and all your data physically never leaves your workstation.

-----

## ❓ FAQ (Frequently Asked Questions)

**1. Is this really completely free? What's the catch?**
Yes. The local version is always free and unlimited (you are using your own hardware). The Cloud version is free thanks to our sponsors, but it has rate limits to prevent abuse.

**2. Can the compressed local version write code as well as the original 744B?**
Extreme compression inevitably reduces the overall logic of the model compared to the data center monster on 744B. The local version does an excellent job with auto-completion, bug hunting, and scripting, but for deep, multi-hour "agentic" autonomy, we recommend using the Cloud-Hybrid mode.

**3. Is my corporate source code safe?**
In **Local mode** — 100%. The model runs completely offline; you can even block the program's internet access through a firewall. In **Cloud mode**, your prompts are sent to our servers for generation, but we strictly follow a Zero-Data-Retention policy (your queries are not logged or used for further training).

**4. What should I do if I hit the request limit in the Cloud version?**
You can either wait for the quota to refresh (the counter usually resets every hour) or seamlessly switch to the Local version in the program settings to continue working using your graphics card's resources.

**5. Is a powerful graphics card (GPU) mandatory for local execution?**
Yes, absolutely. For running the Local Quantized mode, a high-end or upper-mid-range discrete graphics card is strictly required. The `llama.cpp` engine offloads the main computational burden to the VRAM, ensuring stable operation of the compressed model. The local version will not work on integrated graphics (iGPU) or entry-level GPUs.

-----

## 📄 License

This project is distributed under the **MIT License**. You are free to use, modify, and distribute this installer for both personal and commercial purposes.

> **Note:** The architecture and logic of the GLM-5.1 model itself belong to Z.ai and are also distributed under an open license compatible with our terms. See the `LICENSE` file for more details.
