# 🌌 OriønNull — Zero Trust Desktop Browser (v1.0)

[![Developer](https://shields.io)](#)
[![Stack](https://shields.io)](#)
[![License](https://shields.io)](#)

**OriønNull** is a minimalist, ultra-fast, and hyper-secure desktop web browser developed by **k0rkoww**. Built on a strict **Zero Trust** architecture, OriønNull is specifically engineered for maximum local privacy, volatile single-session browsing, and total anti-fingerprinting protection.

Unlike standard mainstream browsers, OriønNull acts as a digital "black box"—leaving **zero forensic footprint** on the host operating system once closed.

🌐 **Official Website:** [orionnull.de5.net](https://de5.net)

---

## 🛠️ Core Technology Stack

OriønNull achieves its fluid performance and robust rendering by leveraging standard open-source web technologies:
- **Language:** Python 3
- **GUI Framework:** PySide6 (Qt for Python)
- **Web Engine:** Qt WebEngine (Powered by a hardened Chromium core)

---

## 🔒 Advanced Privacy & Security Features

Every instance of OriønNull is executed with strict engine flags and profile configurations designed to bypass corporate tracking, hardware logging, and data persistence.

### 🧼 1. Physical Device Protection (Zero-Trace Memory)
- **`QWebEngineProfile.NoPersistentCookies`:** Cookies are volatile. They live strictly inside the active session and are instantly destroyed when the tab or window closes.
- **`MemoryHttpCache` (Max Size: 0):** HTTP cache is strictly sandboxed inside the volatile RAM (Random Access Memory). Absolutely no temporary cache files or media files are ever written to the physical SSD/HDD disk.
- **`LocalStorageEnabled = false`:** Web Storage APIs are completely disabled to block modern tracking techniques that bypass traditional cookie clearing.

### 🚫 2. Radical Anti-Fingerprinting & Attack Surface Reduction
- **`WebGLEnabled = false`:** WebGL and GPU hardware queries are completely disabled. Malicious websites cannot compute a unique hardware fingerprint of your graphics card.
- **`PluginsEnabled = false`:** Extension frameworks and binary plugins are blocked to eliminate standard remote execution vulnerabilities.
- **`PermissionDenyByUser`:** Location data, webcam, and microphone requests are globally denied by default at the engine level without triggering user-facing pop-ups.
- **`JavascriptCanOpenWindows = false`:** Pop-up script behaviors are strictly constrained.

### 🤫 3. De-Google & Network Isolation
- **Chromium Native Flaps Disabled:** Standard background communications are severed using native arguments during initialization:
  - `--disable-sync` (Blocks corporate account synchronization)
  - `--disable-background-networking` (Blocks silent backend pings)
  - `--disable-default-apps` (Removes default telemetry web-apps)

---

## 🔍 Search Engine Integration
OriønNull gives power back to the user by natively supporting privacy-respecting meta-search engines directly through its minimal UI, including:
- **SearXNG** (Default recommended stack)
- **Brave Search**
- **DuckDuckGo**
- **Qwant**
- *(Optional support for Google, Bing, and Ecosia)*

---

## ⚠️ Important Disclaimer (Honest Privacy)
OriønNull is an **ultra-secure local proxy/browser**, not an absolute network anonymizer. 
- It does **NOT** mask your public IP address out-of-the-box.
- It does **NOT** replace a VPN or the Tor network routing layers.
- For complete network stealth, it is highly recommended to stack **OriønNull with Mullvad VPN** or equivalent encrypted routing layers.

---

## 🚀 Getting Started

### Prerequisites
Ensure your environment has Python 3 and the required Qt dependencies installed:
```bash
pip install PySide6 shiboken6
```

### Installation & Launch
Clone the official repository by **k0rkoww** and run the main script:
```bash
git clone https://github.com
cd orionnull
python main.py
```

---
© 2026 OriønNull by k0rkoww — Released as Open Source for a freer web.
