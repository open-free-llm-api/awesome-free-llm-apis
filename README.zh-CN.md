<p align="center">
  <h1 align="center">awesome-free-llm-apis</h1>
  <p align="center"><strong>128+ 免费大模型 API，来自 17 个提供商</strong> — 一站式发现、对比、配置免费模型。</p>
</p>

<p align="center">
  <a href="https://freellm.net"><strong>🌐 访问 freellm.net</strong></a> —
  <a href="https://freellm.net/models/">浏览模型</a> ·
  <a href="https://freellm.net/playground/">在线体验</a> ·
  <a href="https://freellm.net/config/">配置生成器</a> ·
  <a href="https://freellm.net/free-llm-api-keys/">API 密钥</a>
</p>

<p align="center"><strong>🔄 数据每日从 <a href="https://freellm.net">freellm.net</a> 自动更新</strong></p>

<p align="center">
  🌐 <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

---

## 为什么需要这个项目

找一个免费 LLM API，不应该翻十几个 GitHub README、注册五个不同平台、或者猜测哪些模型还有免费额度。

这个仓库是一个**结构化、机器可读的免费 LLM API 目录** — 包含速率限制、上下文窗口、一键配置代码片段和直达 API 密钥链接。每日更新。

**我们解决的问题：**

- ❌ 你找到一份"免费 LLM API 列表" — 结果是两年前的，一半链接已失效
- ❌ 你注册了一个提供商 — 结果悄悄要求信用卡，甚至手机验证
- ❌ 你终于拿到密钥 — 但你的配置工具（Claude Code、Cursor、Codex）需要不同格式
- ❌ 你想对比两个免费模型 — 打开了 8 个浏览器标签页翻各自文档

**这个仓库 + [freellm.net](https://freellm.net) 解决了以上所有问题。**

---

## 快速开始 — 30 秒接入任意免费 API

以下所有提供商都暴露了 **OpenAI 兼容接口**（Gemini 需要简单包装）。这意味着任何接受 `baseURL` + `apiKey` 的工具都能直接用。

### Claude Code (cc)

```bash
export ANTHROPIC_BASE_URL="https://api.openai.com/v1"  # 或 Groq, OpenRouter, NVIDIA NIM
export ANTHROPIC_AUTH_TOKEN="your-api-key-here"
# Claude Code 现在通过免费后端路由
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
    base_url="https://api.openai.com/v1",  # 换成以下任意提供商
    api_key="YOUR_FREE_API_KEY",
)

response = client.chat.completions.create(
    model="gpt-oss-120b",
    messages=[{"role": "user", "content": "你好！"}],
)
print(response.choices[0].message.content)
```

> 访问 [freellm.net/config/](https://freellm.net/config/) 获取 Aider、Cline、OpenCode、Continue、Open WebUI 和 Gemini CLI 的即用配置。

---

## 提供商目录 & 热门免费模型

完整的提供商对比表格和 Top 10 热门模型（按周使用量排名）**请查看 [英文 README](README.md)** — 表格数据每日自动同步，保持最新。

核心数据：
- ⚡ **17 个永久免费层**提供商 — 大多数无需信用卡
- 💰 **OpenRouter** 可再生积分模式
- 🖥️ **本地/自托管方案**（Ollama、LM Studio、llama.cpp 等）— 无限使用、完全私密、永久免费

---

## 参与贡献

欢迎贡献！

- **补充缺失的免费模型** — 提交 [issue](https://github.com/open-free-llm-api/awesome-free-llm-apis/issues) 或 PR
- **修正不准确的数据** — 速率限制会变、提供商会升级，欢迎 PR
- **添加配置代码片段** — 有你常用工具的配置方案？添加到 `code-examples/`

### 收录标准

模型列入本列表需满足：
1. 提供商明确提供**免费层**（不仅仅是试用额度）
2. API **公开可访问**（无需候补、封闭内测、或逆向工程）
3. 试用额度：明确标注且最低 $1 额度

---

## 链接

- 🌐 **在线网站**: [freellm.net](https://freellm.net) — 搜索、对比、在线体验、配置生成器
- 🔑 **API 密钥目录**: [freellm.net/free-llm-api-keys/](https://freellm.net/free-llm-api-keys/)
- ⚙️ **配置生成器**: [freellm.net/config/](https://freellm.net/config/)
- 🎮 **在线体验**: [freellm.net/playground/](https://freellm.net/playground/)
- 📊 **模型对比**: [freellm.net/compare/](https://freellm.net/compare/)

## 许可证

MIT © [open-free-llm-api](https://github.com/open-free-llm-api)

---

<p align="center">
  <sub>数据每日自动更新 · 最后更新: 2026-05-11</sub>
</p>
