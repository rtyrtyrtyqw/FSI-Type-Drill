# FSI Type-Drill: Local AI Language Learning Tool

**FSI Type-Drill** 是一款結合了 **FSI (Foreign Service Institute) 語言教學法** 與 **本地 LLM (DeepSeek-R1)** 的高效英語肌肉記憶練習工具。

透過「高頻句型替換練習 (Substitution Drills)」，本工具能幫助學習者在不需要雲端 API 的情況下，透過打字與即時語音回饋，建立直覺性的語法反應。

## ✨ 核心功能

- **DeepSeek-R1 驅動**：利用本地最強推論模型，自動生成 10 組具備邏輯性的句型變體。
- **三大難度梯度**：
  - **Simple**: 基礎單字替換。
  - **Morphology**: 隨機變換人稱與時態，強迫大腦注意語法細節。
  - **Transformation**: 肯定句、否定句與疑問句的快速切換練習。
- **即時語音 (TTS)**：輸入前聽一遍，輸入後再讀一遍，強化聽力與發音連結。
- **隱私安全**：100% 本地運行，你的練習內容與程式碼完全不會上傳到雲端。

## 快速開始

### 1. 安裝環境
確保你的電腦已安裝 [Ollama](https://ollama.com/)。

### 2. 下載模型
在終端機輸入：
```bash
ollama run 你的模型
```

### 3. 設定 CORS 權限 (重要)
為了讓瀏覽器能存取本地 API，請先關閉原本的 Ollama 並透過以下指令重啟：

**Windows (PowerShell):**
```powershell
$env:OLLAMA_ORIGINS="*"; ollama serve
```

**Mac/Linux:**
```bash
OLLAMA_ORIGINS="*" ollama serve
```

### 4. 運行程式
直接使用瀏覽器開啟專案中的 `index.html` 即可開始練習。

## 🛠️ 技術棧
- **Frontend**: Vue.js 3 (Composition API), Tailwind CSS
- **AI Backend**: Ollama 
- **Browser APIs**: Web Speech API (TTS), LocalStorage

## 📝 授權條款
本專案採用 [MIT License](LICENSE) 授權。
