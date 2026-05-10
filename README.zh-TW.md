<p align="center">
  <h1 align="center">awesome-free-llm-apis</h1>
  <p align="center"><strong>128+ 免費大模型 API，來自 17 個提供商</strong> — 一站式發現、對比、配置免費模型。</p>
</p>

<p align="center">
  <a href="https://freellm.net"><strong>🌐 訪問 freellm.net</strong></a> —
  <a href="https://freellm.net/models/">瀏覽模型</a> ·
  <a href="https://freellm.net/playground/">線上體驗</a> ·
  <a href="https://freellm.net/config/">配置生成器</a> ·
  <a href="https://freellm.net/free-llm-api-keys/">API 金鑰</a>
</p>

<p align="center"><strong>🔄 資料每日從 <a href="https://freellm.net">freellm.net</a> 自動更新</strong></p>

<p align="center">
  🌐 <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

---

## 為什麼需要這個專案

找一個免費 LLM API，不應該翻十幾個 GitHub README、註冊五個不同平台、或者猜測哪些模型還有免費額度。

這個倉庫是一個**結構化、機器可讀的免費 LLM API 目錄** — 包含速率限制、上下文視窗、一鍵配置程式碼片段和直達 API 金鑰連結。每日更新。

**我們解決的問題：**

- ❌ 你找到一份「免費 LLM API 列表」— 結果是兩年前的，一半連結已失效
- ❌ 你註冊了一個提供商 — 結果悄悄要求信用卡，甚至手機驗證
- ❌ 你終於拿到金鑰 — 但你的配置工具（Claude Code、Cursor、Codex）需要不同格式
- ❌ 你想對比兩個免費模型 — 打開了 8 個瀏覽器分頁翻各自文件

**這個倉庫 + [freellm.net](https://freellm.net) 解決了以上所有問題。**

---

## 快速開始 — 30 秒接入任意免費 API

以下所有提供商都暴露了 **OpenAI 相容介面**（Gemini 需要簡單包裝）。這表示任何接受 `baseURL` + `apiKey` 的工具都能直接使用。

### Claude Code (cc)

```bash
export ANTHROPIC_BASE_URL="https://api.openai.com/v1"  # 或 Groq, OpenRouter, NVIDIA NIM
export ANTHROPIC_AUTH_TOKEN="your-api-key-here"
# Claude Code 現在透過免費後端路由
```

### Cursor

```
Settings → Models → Add Model
  Model name: gpt-oss-120b
  Base URL: https://api.openai.com/v1
  API key: your-free-api-key
```

### Codex CLI

```bash
export OPENAI_BASE_URL="https://api.openai.com/v1"
export OPENAI_API_KEY="your-api-key-here"
```

### OpenAI SDK (Python)

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://api.openai.com/v1",  # 換成以下任意提供商
    api_key="YOUR_FREE_API_KEY",
)

response = client.chat.completions.create(
    model="gpt-oss-120b",
    messages=[{"role": "user", "content": "你好！"}],
)
print(response.choices[0].message.content)
```

> 訪問 [freellm.net/config/](https://freellm.net/config/) 獲取 Aider、Cline、OpenCode、Continue、Open WebUI 和 Gemini CLI 的即用配置。

---

## 提供商目錄 & 熱門免費模型

完整的提供商對比表格和 Top 10 熱門模型（按週使用量排名）**請查看 [英文 README](README.md)** — 表格資料每日自動同步，保持最新。

核心資料：
- ⚡ **17 個永久免費層**提供商 — 大多數無需信用卡
- 💰 **OpenRouter** 可再生積分模式
- 🖥️ **本地/自託管方案**（Ollama、LM Studio、llama.cpp 等）— 無限使用、完全私密、永久免費

---

## 參與貢獻

歡迎貢獻！

- **補充缺失的免費模型** — 提交 [issue](https://github.com/open-free-llm-api/awesome-free-llm-apis/issues) 或 PR
- **修正不準確的資料** — 速率限制會變、提供商會升級，歡迎 PR
- **添加配置程式碼片段** — 有你常用工具的配置方案？添加到 `code-examples/`

### 收錄標準

模型列入本列表需滿足：
1. 提供商明確提供**免費層**（不僅僅是試用額度）
2. API **公開可訪問**（無需候補、封閉內測、或逆向工程）
3. 試用額度：明確標註且最低 $1 額度

---

## 連結

- 🌐 **線上網站**: [freellm.net](https://freellm.net) — 搜尋、對比、線上體驗、配置產生器
- 🔑 **API 金鑰目錄**: [freellm.net/free-llm-api-keys/](https://freellm.net/free-llm-api-keys/)
- ⚙️ **配置產生器**: [freellm.net/config/](https://freellm.net/config/)
- 🎮 **線上體驗**: [freellm.net/playground/](https://freellm.net/playground/)
- 📊 **模型對比**: [freellm.net/compare/](https://freellm.net/compare/)

## 授權

MIT © [open-free-llm-api](https://github.com/open-free-llm-api)

---

<p align="center">
  <sub>資料每日自動更新 · 最後更新: 2026-05-11</sub>
</p>
