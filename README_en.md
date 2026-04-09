# FSI Local AI Type-Drill (Closed-loop)

**Designed for keyboard workers and language learners**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Local--AI-orange)](https://ollama.com/)

---

<p align="center">
  <a href="./docs/README.md">繁體中文</a>
</p>

## Online Access

> **Note:** Since this project connects to your locally running Ollama service, please ensure the service is started according to the [Quick Deployment](#-quick-deployment) steps.

- **GitHub Pages:** [https://rtyrtyrtyqw.github.io/FSI-Type-Drill/](https://rtyrtyrtyqw.github.io/FSI-Type-Drill/)
- **Local Access:** Download `index.html` and open it directly in your browser.

---

## Design Philosophy

The inspiration for this software comes from **Qwerty Learner**, combined with the core concepts of the **FSI (Foreign Service Institute) Language Teaching Method**.

For keyboard workers, muscle memory for English input is often weaker than that of their native language, leading to sluggishness during grammatical transitions. Traditional teaching emphasizes visual memory while neglecting the **muscle memory of language generation**.

**Core Logic of FSI Type-Drill:**
- **Substitution Drills:** Generates varied sentences via local models, allowing you to repeat input within the same grammatical structure until the grammar becomes intuitive.
- **Closed-loop Reinforcement:** When the model detects a grammatical error, it automatically generates personalized exercises targeting that weakness for immediate correction.
- **Integrated Listening & Typing (TTS):** Built-in pronunciation functionality.
- **100% Localized:** Runs on Ollama to ensure all learning data and privacy remain entirely on your local machine.

---

## 🛠 Features

- [x] **Model Adaptation:** Automatically detects the list of installed models in your local Ollama and allows one-click switching.
- [x] **Three Training Levels:**
    * **Simple (Substitution):** Basic substitution to expand vocabulary and improve typing feel.
    * **Morphology (Grammar):** Changes subjects and tenses to correct common verb conjugation errors.
    * **Transformation (Syntax):** Practices logical transitions between affirmative, negative, and interrogative sentences.
- [x] **Weakness Analysis Dashboard:** Tracks error rates across five major categories: Tense, Word Order, Prepositions, Articles, and Vocabulary.
- [x] **Error Tracking Log:** Visually displays a "Diff" comparison between the original and corrected sentences, recording input duration and WPM.
- [x] **AI Auto-Reinforcement:** One-click activation of "Remedial Mode" for targeted training when errors are detected in free-form input.

---

## Quick Deployment

### 1. Environment Preparation
- Install [Ollama](https://ollama.com/).
- Download recommended models: `ollama pull llama3.2` (balanced) or `ollama pull qwen2.5` (excellent Chinese comprehension).

### 2. Start Ollama (CORS Configuration)
To allow the web page to communicate with the local API, CORS settings must be enabled:

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```


**macOS/Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```


### 3. Run the Project
1. Download `index.html`.
2. Open it in your browser and confirm that the **Ollama: Online** indicator in the top right is green.

---

## Training Mode Descriptions

| Mode | Corresponding Level | Description |
| :--- | :--- | :--- |
| **Simple** | Substitution | Keeps the sentence structure unchanged, replacing only specific vocabulary. |
| **Morphology** | Grammar | Changes the subject (I/He/They) or tense to strengthen grammatical accuracy. |
| **Transformation** | Syntax | Converts sentences into questions or negatives to train logical reflexes. |

---

## Data Tracking & Privacy

All training data, error records, and personal statistics for this project are stored in the browser's `localStorage`.
- **100% Privacy:** No login required, no internet connection needed.
- **Clear Anytime:** A "Clear Data" function is provided to reset all learning progress with one click.

---

**If this project helps you, feel free to give it a Star!**
