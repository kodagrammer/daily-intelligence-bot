## 🤖 Daily Intelligence Bot

매일 쏟아지는 AI 정보 속에서, 실제로 엔지니어링 관점에서 중요한 신호(signal)만 추적하기 위한 개인용 인텔리전스 봇 프로젝트입니다.

단순 뉴스 요약이나 AI hype를 수집하는 것이 아니라, 백엔드/소프트웨어 엔지니어 관점에서 다음 질문들에 대한 판단 기준을 장기적으로 축적하는 것을 목표로 합니다.

- 왜 사람들이 이 기술에 열광하는가?
- 실제로 어떤 문제를 해결하는가?
- 어떤 트레이드오프가 존재하는가?
- 운영/보안 관점에서 어떤 문제가 발생할 수 있는가?
- 앞으로 어떤 방향으로 발전할 가능성이 높은가?
- 백엔드 환경에서는 어떤 상황에서 어떻게 적용하는 것이 적절한가?


## Why

AI 관련 정보량은 이미 개인이 의미 있게 소화할 수 있는 수준을 넘어섰습니다.

특히 개발자 입장에서는 아래와 같은 문제가 반복적으로 발생합니다.

- 정보는 많지만 실제 운영 사례는 적음
- hype와 production reality가 혼재됨
- 단순 요약형 콘텐츠가 대부분임
- 장기적인 기술 흐름보다 단기 이슈 소비 중심임
- "왜 중요한가"보다 "무엇이 나왔는가"에 집중됨

이 프로젝트는 이러한 문제를 해결하기 위해 시작되었습니다.

목표는 단순한 뉴스 수집기가 아니라,
장기적으로 엔지니어링 판단 기준을 축적하는 시스템을 만드는 것입니다.


## Current Scope

현재 iteration 범위는 아래에 한정됩니다.

- AI 트렌드 데일리 리포트 생성
- 엔지니어링 관점 분석
- Markdown 리포트 저장
- GitHub 자동 적재
- Telegram 요약 알림

현재 범위에 포함하지 않는 것:

- 주식/시장 분석
- 포트폴리오 관리
- Vector DB
- RAG
- Dashboard
- Multi-Agent Orchestration
- 장기 메모리 시스템


## Architecture

~~~text
GitHub Actions Scheduler
        ↓
Perplexity API
        ↓
Trend Filtering & Analysis
        ↓
Markdown Report Generation
        ↓
GitHub Commit & Push
        ↓
Telegram Notification
~~~

현재는 단순성과 유지보수성을 우선으로 하며,
복잡한 인프라보다 iteration 속도와 판단 품질 검증에 집중합니다.


## Report Structure

매일 생성되는 리포트는 아래 구조를 기준으로 작성됩니다.

~~~text
# AI Backend Trend Daily Report

## 오늘의 핵심 이슈

## 왜 주목받는가

## 원리와 활용 방향성

## 장단점 / 트레이드오프

## 보안 관점 리스크

## 백엔드 적용 판단

## 앞으로의 확장 가능성

## 오늘의 판단

## References
~~~

목표는 단순 정보 전달이 아니라,
"엔지니어 관점의 구조적 해석"을 제공하는 것입니다.


## Repository Structure

~~~text
daily-intelligence-bot/
├── .github/
│   └── workflows/
├── bots/
│   └── ai_trend/
├── shared/
├── reports/
│   └── ai-trend/
├── prompts/
├── config/
└── README.md
~~~

- shared: 공통 유틸리티
- bots: 도메인별 분석 로직
- reports: 생성된 markdown 리포트
- prompts: AI 프롬프트
- config: 봇 설정값


## Future Direction

향후 아래 방향들을 고려하고 있습니다.

- GPT 기반 후처리 분석 레이어
- 장기 thesis 추적
- 추가적인 관심 분야 별 봇 추가
- 엔지니어링 signal scoring
- reasoning accumulation

다만 현재 단계에서는,
과도한 설계보다 실제로 "매일 읽을 가치가 있는 리포트가 생성되는가"를 먼저 검증하는 것을 우선합니다.


## Principles

이 프로젝트는 아래 원칙을 중요하게 생각합니다.

- Signal over noise
- Engineering over hype
- Simplicity over complexity
- Long-term reasoning over short-term consumption
- Iteration over over-engineering
