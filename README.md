<div align="center">

# Hi, I'm Chiho 👋

### Backend Engineer · Building reliable AI-powered products

I build backend systems across APIs, data, realtime communication, infrastructure, and AI integration.<br/>
Kotlin·Spring Boot로 서비스를 만들고, Python으로 문서 파싱 엔진을 만듭니다. AI 기능이 실제 제품 안에서 안정적으로 동작하도록 만드는 데 관심이 있습니다.

<a href="https://www.rktclgh.site"><img src="https://img.shields.io/badge/View_Portfolio-111827?style=for-the-badge&logo=readme&logoColor=white" alt="Portfolio"/></a>
<a href="https://www.rktclgh.site/resume"><img src="https://img.shields.io/badge/View_Resume-374151?style=for-the-badge&logo=googledocs&logoColor=white" alt="Resume"/></a>
<a href="https://www.linkedin.com/in/%EC%B9%98%ED%98%B8-%EC%86%A1-63b791390/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>

</div>

## What I'm building | 현재 만들고 있는 것

### [ko-parser](https://github.com/rktclgh/Ko-Parser)

> A Korean-first document parsing engine. Deterministic core, versioned output, incremental change feed.
>
> 한국어 문서를 먼저 고려해 만드는 파싱 엔진입니다. 같은 문서를 다시 넣어도 다시 파싱하지 않고, 고친 부분만 변경 내역으로 내보냅니다.

RAG 파이프라인을 만들다 보면 검색 품질보다 **입력 문서가 제대로 안 읽히는 것**이 먼저 발목을 잡습니다. 표가 문단으로 흩어지고, 스캔 쪽은 빈 페이지로 나오고, 문서를 고칠 때마다 전체를 다시 넣어야 합니다. ko-parser는 그 앞단을 결정론적으로 푸는 엔진입니다.

- **증분 파싱** — 원본 해시가 같으면 새 버전을 만들지 않고, 고친 문서는 바뀐 블록만 변경 내역으로 냅니다. 바뀌지 않은 블록의 `block_id`는 유지되므로 소비자가 임베딩을 다시 만들지 않아도 됩니다
- **커서 기반 변경 피드** — `changes(cursor)`로 여러 문서의 변경을 순서대로 증분 수신합니다
- **저장소 비의존** — 엔진은 저장 방법을 모릅니다. `Store` 포트와 두 구현(메모리·SQLite)이 같은 테스트 묶음을 통과합니다
- **계약 우선** — 엔진·VLM 레이어·소비자가 주고받는 데이터 계약을 별도 패키지로 고정하고, 골든 예제로 호환을 검증합니다
- **선택 설치** — 한글 글꼴·OCR·레이아웃 모델을 extras로 분리해, 기본 설치는 모델 의존성 없이 돕니다

현재 다루는 것: Markdown · 디지털 PDF 텍스트 레이어 · 선 있는 표 · 스캔 쪽 OCR · 레이아웃 기반 그림·캡션 추출

#### 측정 결과 | Measured

개발용 채점 세트(공공누리 공개문서 8건, 정답 표 45개)에서 잰 값입니다. 데이터셋이 작으므로 절대 성능이 아니라 기준선 대비 비교로 읽어 주세요.

| 항목 | 결과 |
| --- | --- |
| 선 있는 표 (정답 45) | 찾은 표 37 · 완벽 재현 30 · 칸 글자 정확도 **0.936** |
| 스캔 쪽 OCR | 글자 F1 **0.97** · 정렬 CER **0.058** |
| 레이아웃 기반 그림 | 재현율 **0.89** · 정밀도(느슨) **1.00** |
| 글자 보존 | 레이아웃을 켜도 블록 글자 다중집합 동일 (**누락 0**) |

<a href="https://github.com/rktclgh/Ko-Parser"><img src="https://img.shields.io/badge/ko--parser_Repository-181717?style=for-the-badge&logo=github&logoColor=white" alt="ko-parser repository"/></a>
<img src="https://img.shields.io/badge/Python_3.12-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.12"/>
<img src="https://img.shields.io/badge/Apache--2.0-D22128?style=for-the-badge" alt="Apache-2.0"/>

## Selected projects | 주요 프로젝트

| Project | What it is | Core stack |
| --- | --- | --- |
| [**ko-parser**](https://github.com/rktclgh/Ko-Parser) | Korean-first document parsing engine with incremental re-parsing.<br/>증분 재파싱을 지원하는 한국어 특화 문서 파싱 엔진 | Python · ONNX Runtime · SQLite · uv |
| [**Ieum**](https://github.com/rktclgh/ieum_BE) | Location-based community combining realtime services and RAG.<br/>실시간 서비스와 RAG를 결합한 위치 기반 커뮤니티 | Java · Spring Boot · PostgreSQL · PostGIS · pgvector · Redis |
| [**VlaInter**](https://github.com/rktclgh/VlaInter_BE) | Personalized AI interview service built from uploaded career documents.<br/>경력 문서를 기반으로 개인화 질문을 생성하는 AI 면접 서비스 | Kotlin · Spring Boot · PostgreSQL · pgvector · Redis · Bedrock |
| [**FairPlay**](https://github.com/rktclgh/FairPlay_BE) | Event reservation and operations platform with realtime communication.<br/>실시간 소통 기능을 갖춘 행사 예약·운영 플랫폼 | Java · Spring Boot · MySQL · Redis · WebSocket · SSE |
| [**Codex Discord Agents**](https://github.com/rktclgh/Codex_Discord_Agents) | Local role-based multi-agent orchestration through Discord and Codex.<br/>Discord와 Codex를 연결한 역할 기반 로컬 멀티에이전트 도구 | Python · Discord · Codex CLI · tmux · Git |

> **Ieum** — 한국 거주 외국인을 위한 위치 기반 커뮤니티. 팀장 겸 백엔드 개발자로 REST·WebSocket·SSE를 처리하는 서비스와 AI 추론을 분리하고, 위치 검색·벡터 검색·검증된 커뮤니티 지식을 결합한 백엔드를 설계했습니다. 신한 스퀘어브릿지 해커톤 **혁신상** 수상.

## Tech stack

#### Languages

<p>
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white" alt="Kotlin"/>
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
</p>

#### Backend

<p>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot"/>
  <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white" alt="Spring Security"/>
  <img src="https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white" alt="JPA"/>
  <img src="https://img.shields.io/badge/REST_API-111827?style=flat-square" alt="REST API"/>
</p>

#### Data & search

<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white" alt="Redis"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white" alt="MySQL"/>
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite"/>
  <img src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="pgvector"/>
  <img src="https://img.shields.io/badge/PostGIS-2E8B57?style=flat-square&logo=postgresql&logoColor=white" alt="PostGIS"/>
</p>

#### Document parsing & AI

<p>
  <img src="https://img.shields.io/badge/Document_Parsing-0F766E?style=flat-square" alt="Document Parsing"/>
  <img src="https://img.shields.io/badge/Layout_Analysis-0F766E?style=flat-square" alt="Layout Analysis"/>
  <img src="https://img.shields.io/badge/OCR-0F766E?style=flat-square" alt="OCR"/>
  <img src="https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white" alt="ONNX Runtime"/>
  <img src="https://img.shields.io/badge/RAG-6D28D9?style=flat-square" alt="RAG"/>
  <img src="https://img.shields.io/badge/Vector_Search-6D28D9?style=flat-square" alt="Vector Search"/>
  <img src="https://img.shields.io/badge/Knowledge_Graph-4F46E5?style=flat-square" alt="Knowledge Graph"/>
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/Amazon_Bedrock-FF9900?style=flat-square&logo=amazonaws&logoColor=white" alt="Amazon Bedrock"/>
</p>

#### Realtime

<p>
  <img src="https://img.shields.io/badge/WebSocket-111827?style=flat-square" alt="WebSocket"/>
  <img src="https://img.shields.io/badge/STOMP-59666C?style=flat-square" alt="STOMP"/>
  <img src="https://img.shields.io/badge/SSE-0284C7?style=flat-square" alt="Server-Sent Events"/>
  <img src="https://img.shields.io/badge/Web_Push-0EA5E9?style=flat-square" alt="Web Push"/>
</p>

#### Infrastructure & tooling

<p>
  <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions"/>
  <img src="https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare"/>
  <img src="https://img.shields.io/badge/Testcontainers-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Testcontainers"/>
</p>

## Current focus | 현재 관심 분야

Document Parsing · Backend Architecture · Reliable AI Integration · RAG & Retrieval · Agentic Development  
문서 파싱 · 백엔드 아키텍처 · 안정적인 AI 통합 · RAG와 검색 · 에이전틱 개발
