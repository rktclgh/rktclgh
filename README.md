<div align="center">

# Chiho Song

### Backend Engineer building reliable AI-powered products.

**신뢰할 수 있는 AI 기반 제품을 만드는 백엔드 개발자 송치호입니다.**

[Portfolio](https://www.rktclgh.site) · [Resume](https://www.rktclgh.site/resume) · [LinkedIn](https://www.linkedin.com/in/%EC%B9%98%ED%98%B8-%EC%86%A1-63b791390/)

</div>

---

## About | 소개

I build backend systems with **Kotlin, Java, and Spring Boot**. My work spans API and domain design, authentication and session security, data-intensive workflows, real-time communication, deployment and operations, and the integration of RAG and LLM capabilities into real products.

**Kotlin, Java, Spring Boot**를 중심으로 API와 도메인 설계, 인증·세션 보안, 데이터 처리, 실시간 통신, 배포와 운영까지 연결하는 백엔드 시스템을 개발합니다. AI는 별도의 데모가 아니라 제품의 일부라는 관점에서 **RAG, 벡터 검색, LLM API**를 기존 백엔드 흐름에 통합해 왔습니다.

> I care about explicit system boundaries, observable failure paths, and improvements verified with data.  
> 명확한 시스템 경계, 추적 가능한 실패 경로, 수치로 검증되는 개선을 중요하게 생각합니다.

---

## Featured Projects | 주요 프로젝트

### [VlaInter](https://vlainter.rktclgh.site) — AI Interview Service

**Solo Project · Backend / Infrastructure**

Designed and operated a backend that turns resumes, cover letters, and portfolios into personalized interview sessions through document extraction, chunking, embedding, retrieval, question generation, and answer evaluation.

이력서·자기소개서·포트폴리오를 문서 추출, 청킹, 임베딩, 검색, 질문 생성, 답변 평가로 연결해 개인화된 면접 세션을 제공하는 백엔드를 설계하고 운영했습니다.

- PostgreSQL/pgvector-based RAG and Gemini → Amazon Bedrock provider fallback
- Redis-backed HttpOnly cookie sessions, S3 document storage, OCR fallback, Docker deployment
- Reduced session creation errors by **85.7%** and shortened representative question-generation time from **20.6s to 14.8s**

`Kotlin` `Spring Boot` `PostgreSQL` `pgvector` `Redis` `Gemini` `Amazon Bedrock` `AWS` `Docker`

[Backend Repository](https://github.com/rktclgh/VlaInter_BE) · [Live Service](https://vlainter.rktclgh.site)

---

### [Ieum](https://ieum.rktclgh.site) — Location-based Community Platform

**Team Lead · Backend · Innovation Award, Shinhan Youth Hackathon**

Led backend development for a location-based community platform for international residents in Korea. The system separates real-time application traffic from AI inference and combines geospatial, vector, and knowledge-based retrieval.

한국 거주 외국인을 위한 위치 기반 커뮤니티의 백엔드 개발을 이끌었습니다. 실시간 서비스 트래픽과 AI 추론 부하를 분리하고, 위치·벡터·지식 기반 검색을 결합했습니다.

- Two-server architecture for REST/WebSocket/SSE workloads and AI inference
- PostgreSQL with PostGIS and pgvector, Redis-backed sessions, secure HttpOnly cookie authentication
- RAG pipeline combining semantic relevance, location context, and source reliability
- Pre-decode image subsampling reduced decoded pixels by **88.9%** in a representative case

`Java` `Spring Boot` `PostgreSQL` `PostGIS` `pgvector` `Redis` `WebSocket` `SSE` `Spring AI` `Docker`

[Backend Repository](https://github.com/rktclgh/ieum_BE) · [Live Service](https://ieum.rktclgh.site)

---

### FairPlay — Event Reservation & Operations Platform

**Team Lead · Backend**

Built backend features for event reservation and operations, including real-time communication, notifications, authentication, administrative workflows, and an AI support chatbot.

행사 예약과 운영을 위한 API, 인증·인가, 관리자 흐름, 실시간 채팅과 알림, AI 고객지원 챗봇을 구현했습니다.

- WebSocket/STOMP real-time chat and SSE notifications
- Redis-backed session and messaging flows
- Gemini-based RAG chatbot and GitHub Actions deployment pipeline

`Java` `Spring Boot` `MySQL` `Redis` `WebSocket` `STOMP` `SSE` `Gemini` `AWS`

[Backend Repository](https://github.com/rktclgh/FairPlay_BE)

---

### Codex Discord Agents — Local Multi-Agent Orchestration

A local orchestration tool that routes Discord conversations to role-specific Codex sessions, maintains long-running context, exposes runtime state through tmux, and supports task tracking and scoped commits.

Discord 대화를 역할별 Codex 세션으로 라우팅하고 장기 컨텍스트 유지, tmux 기반 관찰, 작업 추적과 범위 제한 커밋을 지원하는 로컬 멀티에이전트 도구입니다.

`Python` `Discord` `Codex CLI` `tmux` `Git`

[Repository](https://github.com/rktclgh/Codex_Discord_Agents)

---

## Engineering Focus | 엔지니어링 관심사

- **Backend architecture & domain modeling** — 백엔드 아키텍처와 도메인 모델링
- **Authentication, session management & security** — 인증·세션 관리와 보안
- **Real-time systems with WebSocket, STOMP and SSE** — 실시간 통신 시스템
- **PostgreSQL, Redis, vector and geospatial search** — 데이터 처리와 검색
- **RAG, LLM integration and provider failure handling** — AI 기능 통합과 실패 대응
- **Deployment, observability and measurable optimization** — 배포·관측성과 수치 기반 최적화

---

## Tech Stack

| Area | Technologies |
| --- | --- |
| **Backend** | Kotlin, Java, Spring Boot, Spring Security, JPA/Hibernate, REST API |
| **Data** | PostgreSQL, pgvector, PostGIS, Redis, MySQL |
| **AI** | RAG, Vector Search, Spring AI, Gemini, Amazon Bedrock |
| **Realtime** | WebSocket, STOMP, SSE, Web Push |
| **Infrastructure** | AWS EC2/RDS/S3, Docker, Nginx, GitHub Actions, Cloudflare |

---

## Contact | 연락

- [Portfolio](https://www.rktclgh.site)
- [Resume](https://www.rktclgh.site/resume)
- [LinkedIn](https://www.linkedin.com/in/%EC%B9%98%ED%98%B8-%EC%86%A1-63b791390/)
