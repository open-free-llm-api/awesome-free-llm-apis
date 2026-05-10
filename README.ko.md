<p align="center">
  <h1 align="center">awesome-free-llm-apis</h1>
  <p align="center"><strong>17개 제공업체, 128개 이상의 무료 LLM API</strong> — 무료 모델을 검색, 비교, 설정하세요.</p>
</p>

<p align="center">
  <a href="https://freellm.net"><strong>🌐 freellm.net 방문</strong></a> —
  <a href="https://freellm.net/models/">모델 찾기</a> ·
  <a href="https://freellm.net/playground/">플레이그라운드</a> ·
  <a href="https://freellm.net/config/">설정 생성</a> ·
  <a href="https://freellm.net/free-llm-api-keys/">API 키</a>
</p>

<p align="center"><strong>🔄 <a href="https://freellm.net">freellm.net</a>에서 매일 자동 업데이트</strong></p>

<p align="center">
  🌐 <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a>
</p>

---

## 이 프로젝트가 필요한 이유

무료 LLM API를 찾기 위해 여러 GitHub README를 뒤지고, 여러 플랫폼에 가입하고, 어떤 모델이 아직 무료 티어를 제공하는지 추측해서는 안 됩니다.

이 저장소는 **구조화된 기계 판독 가능 무료 LLM API 디렉토리**입니다 — 속도 제한, 컨텍스트 윈도우, 원클릭 설정 스니펫, API 키 링크를 매일 업데이트합니다.

**이 저장소 + [freellm.net](https://freellm.net)을 선택하는 이유:**

- ✅ **항상 최신** — 매일 자동 모니터링으로 업데이트, 2년 된 정적 목록이 아닙니다
- ✅ **신용카드 투명성** — 신용카드 필요, 전화 인증 필요, 완전 무료 제공업체를 명확히 표시
- ✅ **원클릭 설정** — Claude Code, Cursor, Codex, Aider 등 10개 이상 도구 지원
- ✅ **나란히 비교** — 컨텍스트 윈도우, 속도 제한, 멀티모달 지원을 즉시 비교

---

## 빠른 시작 — 30초 안에 무료 API 사용

아래 모든 제공업체는 **OpenAI 호환 엔드포인트**를 제공합니다(Gemini는 간단한 래퍼 필요). 즉, `baseURL` + `apiKey`를 허용하는 모든 도구가 작동합니다.

### Claude Code (cc)

```bash
export ANTHROPIC_BASE_URL="https://api.openai.com/v1"  # 또는 Groq, OpenRouter, NVIDIA NIM
export ANTHROPIC_AUTH_TOKEN="your-api-key-here"
# Claude Code가 무료 백엔드를 통해 라우팅됨
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
    base_url="https://api.openai.com/v1",  # 아래 아무 제공업체로 변경 가능
    api_key="YOUR_FREE_API_KEY",
)

response = client.chat.completions.create(
    model="gpt-oss-120b",
    messages=[{"role": "user", "content": "안녕하세요!"}],
)
print(response.choices[0].message.content)
```

> Aider, Cline, OpenCode, Continue, Open WebUI, Gemini CLI 설정은 [freellm.net/config/](https://freellm.net/config/)에서 복사하세요.

---

## 제공업체 디렉토리 & 인기 무료 모델

제공업체 비교 표와 주간 사용량 기준 Top 10 모델은 **[영어 README](README.md)**를 확인하세요 — 테이블 데이터는 매일 자동 동기화됩니다.

주요 데이터:
- ⚡ **17개 영구 무료 티어** 제공업체 — 대부분 신용카드 불필요
- 💰 **OpenRouter** 갱신형 크레딧 모델
- 🖥️ **로컬/자체 호스팅** (Ollama, LM Studio, llama.cpp 등) — 무제한, 완전 비공개, 영구 무료

---

## 기여하기

기여를 환영합니다!

- **누락된 무료 모델 추가** — [이슈](https://github.com/open-free-llm-api/awesome-free-llm-apis/issues) 또는 PR 제출
- **부정확한 데이터 수정** — 속도 제한은 변경되고 제공업체도 발전합니다. PR 환영
- **설정 스니펫 추가** — 사용 중인 도구의 설정 방법이 있다면 `code-examples/`에 추가

### 포함 기준

다음 조건을 충족하는 모델이 대상입니다:
1. 제공업체가 명시적으로 **무료 티어**를 제공 (단순 체험 크레딧이 아님)
2. API가 **공개적으로 접근 가능** (대기자 명단, 비공개 베타, 리버스 엔지니어링이 아님)
3. 체험 크레딧: 명확히 표시되고 최소 $1 상당

---

## 링크

- 🌐 **라이브 사이트**: [freellm.net](https://freellm.net) — 검색, 비교, 플레이그라운드, 설정 생성
- 🔑 **API 키 디렉토리**: [freellm.net/free-llm-api-keys/](https://freellm.net/free-llm-api-keys/)
- ⚙️ **설정 생성기**: [freellm.net/config/](https://freellm.net/config/)
- 🎮 **플레이그라운드**: [freellm.net/playground/](https://freellm.net/playground/)
- 📊 **모델 비교**: [freellm.net/compare/](https://freellm.net/compare/)

## 라이선스

MIT © [open-free-llm-api](https://github.com/open-free-llm-api)

---

<p align="center">
  <sub>매일 자동 업데이트 · 마지막 업데이트: 2026-05-11</sub>
</p>
