<p align="center">
  <h1 align="center">awesome-free-llm-apis</h1>
  <p align="center"><strong>17プロバイダー、128以上の無料LLM API</strong> — 無料モデルを検索・比較・設定。</p>
</p>

<p align="center">
  <a href="https://freellm.net"><strong>🌐 freellm.net を見る</strong></a> —
  <a href="https://freellm.net/models/">モデル一覧</a> ·
  <a href="https://freellm.net/playground/">プレイグラウンド</a> ·
  <a href="https://freellm.net/config/">設定生成</a> ·
  <a href="https://freellm.net/free-llm-api-keys/">APIキー</a>
</p>

<p align="center"><strong>🔄 <a href="https://freellm.net">freellm.net</a> から毎日自動更新</strong></p>

<p align="center">
  🌐 <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

---

## このプロジェクトの目的

無料のLLM APIを探すために、複数のGitHub READMEを読み漁ったり、いくつものプラットフォームに登録したり、どのモデルがまだ無料枠を提供しているか推測したりするのは非効率です。

このリポジトリは**構造化された機械可読な無料LLM APIディレクトリ**です — レート制限、コンテキストウィンドウ、ワンクリック設定スニペット、APIキー入手リンクをまとめ、毎日更新しています。

**私たちが解決する問題：**

- ❌ 「無料LLM APIリスト」を見つけたら、2年前のもので半分のリンクが切れている
- ❌ プロバイダーに登録したら、クレジットカードや電話番号認証を要求される
- ❌ やっとAPIキーを入手したら、設定ツール（Claude Code、Cursor、Codex）がそれぞれ異なるフォーマットを要求する
- ❌ 2つの無料モデルを比較するのに、8つのブラウザタブを開いて各ドキュメントを見比べる

**このリポジトリ + [freellm.net](https://freellm.net) がすべて解決します。**

---

## クイックスタート — 30秒で無料APIを使う

以下の全プロバイダーが**OpenAI互換エンドポイント**を提供しています（Geminiは簡単なラッパーで対応）。つまり、`baseURL` + `apiKey` を受け付けるツールならすべて動作します。

### Claude Code (cc)

```bash
export ANTHROPIC_BASE_URL="https://api.openai.com/v1"  # または Groq, OpenRouter, NVIDIA NIM
export ANTHROPIC_AUTH_TOKEN="your-api-key-here"
# Claude Codeが無料バックエンド経由で動作
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
    base_url="https://api.openai.com/v1",  # 以下の任意のプロバイダーに変更可
    api_key="YOUR_FREE_API_KEY",
)

response = client.chat.completions.create(
    model="gpt-oss-120b",
    messages=[{"role": "user", "content": "こんにちは！"}],
)
print(response.choices[0].message.content)
```

> Aider、Cline、OpenCode、Continue、Open WebUI、Gemini CLI の設定は [freellm.net/config/](https://freellm.net/config/) からコピーできます。

---

## プロバイダーディレクトリ & 人気の無料モデル

プロバイダー比較表と週間使用量トップ10モデルは **[英語版 README](README.md)** をご覧ください — テーブルデータは毎日自動同期され最新の状態を保っています。

主要データ：
- ⚡ **17の永久無料枠**プロバイダー — ほとんどのプロバイダーでクレジットカード不要
- 💰 **OpenRouter** 更新型クレジットモデル
- 🖥️ **ローカル/セルフホスト**（Ollama、LM Studio、llama.cpp 等）— 無制限・完全プライベート・永久無料

---

## コントリビューション

貢献を歓迎します！

- **不足している無料モデルの追加** — [issue](https://github.com/open-free-llm-api/awesome-free-llm-apis/issues) または PR を提出
- **不正確なデータの修正** — レート制限は変更され、プロバイダーも進化します。PR歓迎
- **設定スニペットの追加** — お使いのツールの設定方法があれば `code-examples/` に追加

### 収録基準

以下の条件を満たすモデルが対象です：
1. プロバイダーが明示的に**無料枠**を提供している（単なるトライアルクレジットではない）
2. APIが**公開アクセス可能**（待機リスト、クローズドベータ、リバースエンジニアリングではない）
3. トライアルクレジット：明示的に表示され、最低$1相当

---

## リンク

- 🌐 **ライブサイト**: [freellm.net](https://freellm.net) — 検索、比較、プレイグラウンド、設定生成
- 🔑 **APIキーディレクトリ**: [freellm.net/free-llm-api-keys/](https://freellm.net/free-llm-api-keys/)
- ⚙️ **設定ジェネレーター**: [freellm.net/config/](https://freellm.net/config/)
- 🎮 **プレイグラウンド**: [freellm.net/playground/](https://freellm.net/playground/)
- 📊 **モデル比較**: [freellm.net/compare/](https://freellm.net/compare/)

## ライセンス

MIT © [open-free-llm-api](https://github.com/open-free-llm-api)

---

<p align="center">
  <sub>毎日自動更新 · 最終更新: 2026-05-11</sub>
</p>
