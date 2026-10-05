
# 🛡️️ HexaCode Enclave
&gt; **Air-Gapped Local NPU Co-Processing Engine via iQOO Office Kit**

---

## 💡 Overview
**HexaCode Enclave** turns your iQOO smartphone into a hardware-isolated, air-gapped AI co-processor for your laptop.

Enterprise software developers are strictly forbidden from pasting proprietary source code into cloud AI tools (e.g., ChatGPT, Claude) due to data exfiltration risks. **HexaCode Enclave solves this by keeping 100% of the AI processing local, offline, and secure.**

---

## ⚡ How It Works in 3 Steps

1. **Copy (`Ctrl + C` on Laptop)**  
   Select buggy or vulnerable code in your laptop IDE and copy it.
2. **Offload (via iQOO Office Kit)**  
   The iQOO Office Kit automatically syncs the snippet to your smartphone's **Snapdragon Hexagon NPU**.
3. **Paste (`Ctrl + V` on Laptop)**  
   The phone's local AI model analyzes the code and generates a security patch in **under 2 seconds**. Press paste in your IDE to apply the fix.

&gt; 🔒 **Zero bytes ever leave your physical devices or enter the cloud.**

---

## 🎯 Key Benefits

* **🔒 100% Zero-Trust Privacy:** Meets strict corporate data security policies.
* **📱 Phone-First Compute:** Powered natively on the mobile Snapdragon NPU via Meta ExecuTorch.
* **🌉 iQOO Office Kit Integration:** Continuous bidirectional clipboard synchronization.
* **💸 Zero Cloud Costs:** 100% open-source stack with no external API fees or cloud server costs.

---

## 🏗️ System Architecture

```text
+-------------------------------------------------------------------+
|                        1. LAPTOP IDE                              |
|   Developer selects vulnerable code &amp; presses Ctrl+C              |
+-------------------------------------------------------------------+
                                  │
                                  ▼  (iQOO Office Kit Sync)
+-------------------------------------------------------------------+
|                   2. iQOO SMARTPHONE (ENCLAVE)                    |
|   • Android BroadcastReceiver catches code snippet                |
|   • ExecuTorch runs INT4 Qwen3-Coder model on Snapdragon NPU      |
|   • Analyzes AST, fixes SQL injections &amp; memory leaks offline     |
+-------------------------------------------------------------------+
                                  │
                                  ▼  (iQOO Office Kit Return)
+-------------------------------------------------------------------+
|                        3. LAPTOP IDE                              |
|   Patched code fills clipboard — press Ctrl+V to apply fix        |
+-------------------------------------------------------------------+
\## 📽️ Video Walkthrough &amp; Resources
\* 🔗 \*\*[Watch YouTube Walkthrough (Unlisted)](https://youtube.com/shorts/1zDFdQBqvgs?si=Y8yU1Mws2H5lBAFW)\*\*

HexaCode-Enclave/
├── android/ # Kotlin Android app &amp; ExecuTorch NPU service
├── models/ # Model quantization scripts (Qualcomm QNN)
├── vscode-extension/ # Laptop IDE listener extension
└── docs/ # Architecture diagrams &amp; submission pitch deck

