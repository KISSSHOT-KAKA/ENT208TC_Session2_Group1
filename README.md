<div align="center">

![X Space Banner](https://img.shields.io/badge/X%20Space-On--computer%20Voice%20Assistant-33b5e5?style=for-the-badge&labelColor=000&padding=50)

# 🎙️ On-computer Voice Assistant
### 🚀 ENT208TC - Session 2 Group 1
</div>

[![Project Status: Active](https://img.shields.io/badge/Status-In--Development-yellow?style=for-the-badge&logo=github)](https://github.com/)
[![Hardware: M5Stack](https://img.shields.io/badge/Hardware-M5Stick%20Atom%20S3%20R-orange?style=for-the-badge&logo=espressif)](https://docs.m5stack.com/en/core/atom_s3)
[![Software: Python](https://img.shields.io/badge/Language-Python%203.9+-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Course: ENT208TC](https://img.shields.io/badge/Course-ENT208TC-red?style=for-the-badge)](https://www.xjtlu.edu.cn)

---

**“Empowering desktop interaction with the sound of your voice.”**
**“用声音赋能桌面交互，记录成长的每一步。”**

<p align="center">
  <a href="#-english-overview">🇬🇧 Overview</a> • 
  <a href="#-中文项目概览">🇨🇳 项目概览</a> • 
  <a href="#-software-features">🛠️ Software</a> • 
  <a href="#-hardware-stack">⚙️ Hardware</a> • 
  <a href="#-progress-timeline">📈 Progress</a> • 
  <a href="#-acknowledgments">🤝 Acknowledgments</a>
</p>

</div>

---

## 🛠️ Software Features / 功能实现

> 🚀 **Current Development Status & Conceptual Vision**

<div align="center">
  <img src="Cat_Waving.gif" width="120" />
  <p><i>🚧 Software System in Active Development...</i></p>
</div>

- [x] **Core Framework**: Basic speech command recognition infrastructure. (语音指令识别基础框架)
- [x] **CV Module**: Real-time "Campus Cat" detection algorithm 🐾. (校园猫咪实时检测算法)
- [ ] **UI/UX**: Interactive desktop assistant interface. (语音助手 UI 界面交互)
- [ ] **Navigation**: Integrated path-finding services. (路径导航集成)

---

## 🧩 Recommended Library Stack / 技术选型建议（Atom S3 R + 桌面语音助手）

### 1) Device Side (Atom S3 R / ESP32-S3)
- **ESP-SR**: Wake word + on-device speech recognition capability, best ecosystem fit with ESP32-S3.
- **ESP-ADF**: Audio capture, codec handling, and stream pipeline support.
- **arduino-audio-tools**: Practical option when using Arduino workflow for I2S/audio pipeline.

### 2) Desktop ASR (Speech-to-Text)
- **faster-whisper**: Strong local accuracy and mature community support.
- **Vosk**: Lightweight offline recognition with good real-time performance.
- **sherpa-onnx**: Flexible offline streaming ASR deployment.

### 3) Wake Word (Desktop Optional)
- **Porcupine**: Fast integration and production-grade keyword spotting.
- **openWakeWord**: Open-source and customizable for project-specific wake words.

### 4) TTS (Text-to-Speech)
- **Piper**: Good quality/latency balance for offline local TTS.
- **Coqui TTS**: Strong extensibility and model customization (heavier runtime).
- **edge-tts**: High-quality online voices if network access is acceptable.

### 5) Dialogue & Orchestration
- **Ollama + (LangChain or LlamaIndex)** for local intent handling, tool calls, and multi-turn conversation.
- For an MVP, use a simpler chain first: **ASR → Rules/LLM → TTS**.

### 6) Device–Desktop Communication
- **pyserial** (Python) / **serialport** (Node.js): preferred for direct serial communication.
- **paho-mqtt** / **mqtt.js**: recommended when scaling to multi-device architecture.

### ✅ Suggested Fastest MVP Combination
- **Device**: ESP-SR + ESP-ADF
- **Desktop**: faster-whisper + Piper + pyserial
- **Optional wake word**: Porcupine (faster integration) or openWakeWord (more customizable)

---

## 🇬🇧 English Overview

### 📖 Introduction
This project for the **ENT208TC** module focuses on creating a responsive, intelligent local assistant. By integrating **NLP**, **Computer Vision**, and **M5Stack hardware**, we aim to bridge the gap between physical triggers and desktop automation. Our core mission includes voice-driven productivity and a specific "Campus Cat" detection module to enhance campus interaction.

### ⚙️ Hardware Stack
Our project leverages the ESP32-S3 ecosystem for low-latency processing:
* **Core Controller**: `M5Stick Atom S3 R` (High-performance ESP32-S3)
* **Audio Base**: `Echo Base` (Equipped with high-sensitivity Mic & Speaker)

### 📈 Progress Timeline
- [x] **Week 1-3**: Project Setup & Requirement Analysis
- [x] **Week 4-6**: Hardware Driver Integration & Basic UI
- [ ] **Week 7-9**: NLP Model Training & Command Mapping
- [ ] **Week 10-12**: CV Integration & Final Optimization

[⬆ Back to Top](#-on-computer-voice-assistant)

---

## 🇨🇳 中文项目概览

### 📖 项目简介
欢迎来到 **X Space** 小组的开源仓库！本项目致力于开发一款智能本地语音助手。通过硬件与软件的深度联动（NLP + CV），实现流畅的交互体验。我们不仅关注桌面自动化指令，还特别开发了“校园猫咪识别”功能，旨在提升校园生活的趣味性与便捷度。

### ⚙️ 硬件架构
本项目基于 ESP32-S3 生态系统进行开发，确保低延迟的音频与图像处理：
* **核心控制器**: `M5Stick Atom S3 R` (高性能 ESP32-S3 主控)
* **音频底座**: `Echo Base` (内置高灵敏度麦克风与扬声器)

### 📈 项目进度图
- [x] **Week 1-3**: 🟢 项目启动与需求分析
- [x] **Week 4-6**: 🟡 硬件驱动集成与初步 UI 设计
- [ ] **Week 7-9**: 🔵 NLP 模型训练与指令映射
- [ ] **Week 10-12**: 🔴 视觉算法集成与最终优化

---

### 📁 Repository Map
```text
.
├── 📂 Evidences            # Weekly growth & Meeting minutes
│   └── 📑 Meeting_Minutes  # Meeting records
├── 📂 Weekly Tasks        # Task assignments & Feedback
├── 📂 Source_Code         # 🚧 Core Implementation
│   ├── 📄 voice_engine.py  # Speech recognition logic
│   └── 📄 main_ui.py       # Desktop assistant interface
└── 📄 Cat_Waving.gif      # Our Campus Mascot 🐾
```
---

## 🤝 Acknowledgments / 致谢

<p align="left">
We express our sincere gratitude to our mentors for their invaluable guidance and support throughout the development of this project:
</p>
<p align="left">
我们衷心感谢以下导师对本项目的支持与指导：
</p>

| Role (角色) | Mentor (导师) |
| :--- | :--- |
| **Module Leader** | 👨‍🏫 Bogdan Marculescu |
| **Module Leader** | 👨‍🏫 Stefan Seedorf |
| **Pathfinder** | 👨‍🏫 Kai Liu |
| **Pathfinder** | 👨‍🏫 Victor Perez |

---

## 👥 The Team / 团队成员

<table align="center">
  <tr>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/manager.png" width="40"/><br />
      <b>Chengren Pang</b><br />
      <sub>Project Leader &<br />Engineering Manager<br /><i>(工程经理 / 技术主管)</i></sub>
    </td>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/programming.png" width="40"/><br />
      <b>Hengyu Wan</b><br />
      <sub>Full-Stack Developer &<br />Project Supervisor<br /><i>(全栈开发工程师 / 项目主管)</i></sub>
    </td>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/bullish.png" width="40"/><br />
      <b>Zihang Zeng</b><br />
      <sub>Market Insights<br />Analyst<br /><i>(市场洞察分析师)</i></sub>
    </td>
  </tr>
  
  <tr>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/books.png" width="40"/><br />
      <b>Chenyi Zhuang</b><br />
      <sub>Knowledge Management<br />Specialist<br /><i>(知识管理专家)</i></sub>
    </td>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/design.png" width="40"/><br />
      <b>Jinkun Zhou</b><br />
      <sub>Visual Interaction<br />Designer<br /><i>(视觉交互设计师)</i></sub>
    </td>
    <td align="center" width="33%">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/creativity.png" width="40"/><br />
      <b>Tianze Xu</b><br />
      <sub>Creative Assets<br />Specialist<br /><i>(创意资产专家)</i></sub>
    </td>
  </tr>

  <tr>
    <td align="center" colspan="3">
      <br />
      <img src="https://img.icons8.com/fluency/48/000000/creativity.png" width="40"/><br />
      <b>Yancheng Li</b><br />
      <sub>Creative Assets<br />Specialist<br /><i>(创意资产专家)</i></sub>
    </td>
  </tr>
</table>

---

<div align="center">

  <p><b>© 2026 X Space - ENT208TC Group 1</b></p>
  <p><i>Built with ❤️, Python, and M5Stack</i></p>

![X Space Banner](https://img.shields.io/badge/X%20Space-On--computer%20Voice%20Assistant-33b5e5?style=for-the-badge&labelColor=000&padding=50)

</div>
