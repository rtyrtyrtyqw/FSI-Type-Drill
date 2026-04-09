# FSI Local AI Type-Drill (Closed-loop)

**為鍵盤工作者與外語學習者設計的訓練軟體**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Ollama](https://img.shields.io/badge/Ollama-Local--AI-orange)](https://ollama.com/)

---

## 在線訪問

> **注意：** 由於本專案需連接你本地運行的Ollama服務，請確保已按照 [快速部署](#-快速部署) 步驟啟動服務。

- **GitHub Pages:** [https://rtyrtyrtyqw.github.io/FSI-Type-Drill/](https://rtyrtyrtyqw.github.io/FSI-Type-Drill/)
- **本地訪問:** 直接下載 `index.html` 並在瀏覽器打開。

---

## 設計思想

本軟體的靈感來自於 **Qwerty Learner**，並結合了美國外語協會 **FSI (Foreign Service Institute) 語言教學法** 的核心思想。

對於鍵盤工作者來說，英語輸入的肌肉記憶往往弱於母語，容易出現語法轉換遲鈍的現象。傳統教學偏重視覺記憶，而忽視了**語言生成的肌肉記憶**。

**FSI Type-Drill 的核心邏輯：**
- **Substitution Drills (替換練習)：** 透過本地模型生成不同句型，讓你在同一個語法結構中不停重複輸入，將語法轉化為直覺。
- **閉環補強 (Closed-loop)：** 當模型偵測到你的語法錯誤，會自動生成針對該弱點的專屬練習題，確保從錯誤中即時修正。
- **聽打合一 (TTS)：** 內建發音功能。
- **100% 本地化：** 基於Ollama運行，確保學習數據與隱私完全留在本地。

---

## 🛠 功能列表

- [x] **模型自適應：** 自動感應本地Ollama已安裝模型清單，一鍵切換。
- [x] **三大訓練等級：**
  - **Simple (Substitution):** 基礎替換，擴充詞彙與手感。
  - **Morphology (Grammar):** 變換人稱與時態，修正動詞變化錯誤。
  - **Transformation (Syntax):** 訓練肯定、否定與疑問句間的邏輯轉場。
- [x] **弱點分析儀表板：** 追蹤時態、語序、介系詞、冠詞、詞彙五大錯誤率。
- [x] **錯誤追蹤日誌：** 視覺化呈現原句與修正句的 Diff 對比，並記錄輸入用時與 WPM。
- [x] **AI 自動補強：** 偵測到自由輸入語法有誤時，一鍵啟動「補強模式」進行針對性訓練。

---

## 快速部署

### 1. 環境準備
- 安裝 [Ollama](https://ollama.com/)。
- 下載建議模型：`ollama pull llama3.2` (平衡) 或 `ollama pull qwen2.5` (中文理解佳)。

### 2. 啟動 Ollama (跨域設定)
為了讓網頁能與本地 API 通訊，必須開啟 CORS 設定：

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```

**macOS/Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```

### 3. 運行項目
1. 下載 `index.html`。
2. 在瀏覽器中打開，確認右上角 **Ollama: Online** 燈號為綠色。

---

## 練習模式說明

| 模式 | 對應層級 | 說明 |
| :--- | :--- | :--- |
| **Simple** | Substitution | 保持句架構不變，僅更換詞彙 |
| **Morphology** | Grammar | 變換主詞 (I/He/They) 或時態，強化語法準確度 |
| **Transformation** | Syntax | 轉為問句或否定句，訓練邏輯反應 |

---

## 數據追蹤與隱私

本專案所有的練習數據、錯誤紀錄與個人統計皆儲存在瀏覽器的 `localStorage` 中。
- **100% 隱私：** 無須登入，無須聯網。
- **隨時清除：** 提供「清除資料」功能，一鍵重置所有學習進度。

---

**如果這個專案對你有幫助，歡迎點個 Star！**
