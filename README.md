# FSI Local AI Type-Drill

[English Version](./README_en.md)

**為鍵盤工作者與外語學習者設計的「本地 AI 句型肌肉記憶」鍛鍊軟體**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Local--AI-orange)](https://ollama.com/)

---

## 📸 在線訪問

> **注意：** 由於本專案需連接你本地運行的 Ollama 服務，請確保已按照 [快速部署](#-快速部署) 步驟啟動服務。

- **GitHub Pages:** https://rtyrtyrtyqw.github.io/FSI-Type-Drill/
- **本地訪問:** 直接下載 `index.html` 並在瀏覽器打開。

---

## ✨ 設計思想

本軟體的靈感來自於 **Qwerty Learner**，並結合了美國外語協會 **FSI (Foreign Service Institute) 語言教學法** 的核心思想。

對於鍵盤工作者來說，英語輸入的肌肉記憶往往弱於母語，容易出現「提筆忘字」或語法轉換遲鈍的現象。傳統的背單詞軟體偏重於視覺記憶，而忽視了**語言生成的肌肉記憶**。

**FSI Type-Drill 的核心邏輯：**
- **Substitution Drills (替換練習)：** 透過本地 AI (如 DeepSeek-R1) 即時生成句型變體，讓你在同一語法結構下高頻重複輸入，將語法轉化為直覺。
- **聽打合一 (TTS)：** 內建發音功能，在輸入前與完成後進行語音強化，建立「聲音-語義-手指」的連動。
- **100% 本地化：** 基於 Ollama 運行，確保你的學習數據、個人練習句型完全留在本地，隱私無虞。

---

## 🛠 功能列表

- [x] **模型自適應：** 自動感應本地 Ollama 已安裝的模型清單，一鍵切換。
- [x] **三大難度梯度：**
  - **Simple (簡單替換):** 僅替換核心單詞，適合初學者。
  - **Morphology (語法變換):** 隨機變換人稱與時態，強迫大腦處理動詞變化。
  - **Transformation (句型轉換):** 練習將肯定句轉為疑問或否定句，訓練邏輯反應。
- [x] **AI 每日推薦：** 根據選定難度，由 AI 生成 3 組日常對話或演講句型。
- [x] **即時語音回饋：** 採用 Web Speech API，無須聯網即可實現專業發音。
- [x] **歷史紀錄整理：** 自動保存練習次數與日期，量化你的進步。

---

## 🚀 快速部署

### 1. 環境準備
- 安裝 [Ollama](https://ollama.com/)。
- 下載你喜歡的本地模型（建議使用 `deepseek-r1:8b` 或 `llama3`）。
  ```bash
  ollama run deepseek-r1:8b
  ```

### 2. 啟動 Ollama (跨域設定)
為了讓瀏覽器網頁能與本地 API 通訊，請使用以下指令啟動：

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```

**macOS/Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```

### 3. 運行項目
1. 下載本倉庫。
2. 在瀏覽器中打開 `index.html`。
3. 在下拉選單中選擇你的模型，輸入或選擇句型，按下 **Start Training**。

---

## 📗 練習模式說明

| 模式 | 說明 | 適合場景 |
| :--- | :--- | :--- |
| **Simple** | 保持句架構不變，僅更換詞彙 | 擴充詞彙量與基本手感 |
| **Grammar** | 變換主詞 (I/He/They) 或時態 | 修正亞洲學生常犯的語法錯誤 |
| **Syntax** | 轉為問句或否定句 | 訓練口說與演講時的靈活轉場 |

---

## 🏄‍♂️ 貢獻指南

如果您對本項目感興趣，歡迎提交 PR：
- 貢獻更優化的 AI Prompt。
- 改進 UI/UX 打字體驗。
- 增加更多的本地 API 詞庫支援。

---

## 🎁 大感謝

- **Qwerty Learner:** 本專案的核心視覺與打字邏輯靈感來源。
- **Ollama:** 提供強大的本地模型運行環境。
- **DeepSeek:** 提供了極佳的本地推論能力。

---

**🌟 如果這個專案對你有幫助，歡迎點個 Star！**
