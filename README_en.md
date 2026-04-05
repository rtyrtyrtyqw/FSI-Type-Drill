# FSI Local AI Type-Drill

[繁體中文](README.md)

**A high-performance "Language Muscle Memory" trainer for keyboard workers and language learners, powered by Local LLMs.**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Local--AI-orange)](https://ollama.com/)

---

## 📸 Demo & Access

> **Note:** Since this project connects to your local Ollama service, ensure you have followed the [Quick Start](#-quick-start) steps to enable the service.

- **GitHub Pages:** [Your GitHub Pages Link]
- **Local Access:** Simply download `index.html` and open it in your browser.

---

## ✨ Design Philosophy

Inspired by **Qwerty Learner** and rooted in the **FSI (Foreign Service Institute) Substitution Drill** methodology.

For professionals who use English as a secondary working language, typing fluency often lags behind their native tongue. This results in "mental blocks" or grammatical hesitation during real-time communication. Traditional apps focus on visual recognition, but **FSI Type-Drill** focuses on **Motor Memory**.

**Core Logic of FSI Type-Drill:**
- **Substitution Drills:** Leveraging Local LLMs (e.g., DeepSeek-R1) to generate real-time sentence variations. By practicing the same grammatical structure with different vocabulary, you turn grammar rules into a physical instinct.
- **Audio-Visual-Tactile Integration:** Built-in Text-to-Speech (TTS) reinforces learning by syncing sound, meaning, and finger movement.
- **100% Privacy:** Powered by **Ollama**, ensuring your practice data and personal patterns stay entirely on your machine. No cloud, no tracking.

---

## 🛠 Feature List

- [x] **Model Autodetect:** Automatically detects your local Ollama models for seamless switching.
- [x] **Three Difficulty Tiers:**
  - **Simple:** Basic vocabulary substitution.
  - **Morphology:** Randomly changes subjects (I/He/They) or tenses to fix common grammar slips.
  - **Transformation:** Practice converting statements into questions or negatives on the fly.
- [x] **AI Recommendations:** Generates 3 daily patterns (Speech/Conversation/Business) based on your level.
- [x] **Instant TTS Feedback:** Uses Web Speech API for high-quality, offline pronunciation.
- [x] **Progress Tracking:** Locally saved history to quantify your improvement over time.

---

## 🚀 Quick Start

### 1. Requirements
- Install [Ollama](https://ollama.com/).
- Pull your preferred model (e.g., `deepseek-r1:8b` or `llama3`).
  ```bash
  ollama run deepseek-r1:8b
  ```

### 2. Launch Ollama (CORS Configuration)
To allow the browser to communicate with your local API, restart Ollama with the following command:

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```

**macOS/Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```

### 3. Run the App
1. Clone or download this repository.
2. Open `index.html` in your browser.
3. Select your model from the dropdown, input a pattern, and click **Start Training**.

---

## 📗 Drill Mode Guide

| Mode | Description | Best For |
| :--- | :--- | :--- |
| **Simple** | Keeps sentence structure, changes only keywords | Expanding vocabulary & basic speed |
| **Grammar** | Shifts Subject (I/He/They) or Tense | Fixing "Third-person S" & Tense errors |
| **Syntax** | Converts to Questions or Negatives | Training oral flexibility & public speaking |

---

## 🏄‍♂️ Contribution

Contributions are welcome! Feel free to:
- Optimize AI Prompts.
- Improve the Typing UI/UX.
- Add more pre-defined local API wordbanks.

---

## 🎁 Acknowledgments

- **Qwerty Learner:** Core inspiration for the visual and typing logic.
- **Ollama:** Providing a robust local LLM environment.
- **Local AI Community:** For the amazing push toward data sovereignty.

---

**🌟 If this project helps you, please give it a Star!**
