<div align="center">

# 🏆 MoneyLog
### 청년 맞춤형 금융 생활관리 플랫폼

**[우리FISA 6기] 클라우드 엔지니어링 과정 5팀**

[![GitHub](https://img.shields.io/badge/GitHub-5kstration-181717?style=flat-square&logo=github)](https://github.com/5kstration)
[![Tech Stack](https://img.shields.io/badge/Tech-Spring%20Boot%20|%20React%20|%20AWS-blue?style=flat-square)](#-기술-스택)
[![Architecture](https://img.shields.io/badge/Architecture-MSA%20|%20K8s%20|%20Istio-green?style=flat-square)](#-아키텍처)

</div>

---

## 📑 목차

1. [팀원 소개](#-팀원-소개)
2. [프로젝트 개요](#-프로젝트-개요)
   - [프로젝트 주제](#프로젝트-주제)
   - [기획 배경 및 목적](#기획-배경-및-목적)
   - [개발 목표](#개발-목표)
3. [기술 스택](#-기술-스택)
4. [아키텍처](#-아키텍처)
   - [시스템 아키텍처](#시스템-아키텍처)
   - [소프트웨어 아키텍처](#소프트웨어-아키텍처)
5. [핵심 기능](#-핵심-기능)
   - [핵심 기술 구성](#핵심-기술-구성)
   - [세부 기능](#세부-기능)
     - [1. AI 기반 소비 분석](#1-ai-기반-소비-분석-및-맞춤형-추천)
     - [2. 실시간 이벤트 처리](#2-실시간-이벤트-처리-및-cdc-기반-데이터-동기화)
     - [3. Istio 서비스 메시](#3-istio-기반-서비스-메시service-mesh-및-트래픽-제어)
     - [4. Hot/Cold 아키텍처](#4-hotcold-데이터-아키텍처를-통한-데이터-라이프사이클-최적화)
     - [5. AIOps 인프라 운영](#5-aiops-및-sre-기반의-고가용성-인프라-운영)

---

## 👥 팀원 소개

<table align="center">
  <tr>
    <td align="center" width="200px">
      <img src="https://via.placeholder.com/150" width="150px" alt="팀원1"/><br/>
      <b>팀원 이름</b><br/>
      <sub>역할: Backend</sub><br/>
      <a href="https://github.com/username">GitHub</a>
    </td>
    <td align="center" width="200px">
      <img src="https://via.placeholder.com/150" width="150px" alt="팀원2"/><br/>
      <b>팀원 이름</b><br/>
      <sub>역할: Frontend</sub><br/>
      <a href="https://github.com/username">GitHub</a>
    </td>
    <td align="center" width="200px">
      <img src="https://via.placeholder.com/150" width="150px" alt="팀원3"/><br/>
      <b>팀원 이름</b><br/>
      <sub>역할: DevOps</sub><br/>
      <a href="https://github.com/username">GitHub</a>
    </td>
    <td align="center" width="200px">
      <img src="https://via.placeholder.com/150" width="150px" alt="팀원4"/><br/>
      <b>팀원 이름</b><br/>
      <sub>역할: Infrastructure</sub><br/>
      <a href="https://github.com/username">GitHub</a>
    </td>
    <td align="center" width="200px">
      <img src="https://via.placeholder.com/150" width="150px" alt="팀원5"/><br/>
      <b>팀원 이름</b><br/>
      <sub>역할: AI/ML</sub><br/>
      <a href="https://github.com/username">GitHub</a>
    </td>
  </tr>
</table>

---

## 프로젝트 개요

### 프로젝트 주제

**MoneyLog : 청년 맞춤형 금융 생활관리 플랫폼**

AI 기반 소비 분석과 소셜 피드를 결합하여, 청년들이 자신의 금융 생활을 즐겁게 관리하고 공유할 수 있는 참여형 금융 플랫폼입니다.

### 기획 배경 및 목적

<details>
<summary><b>기획 배경 자세히 보기</b></summary>

<br/>

최근 청년 세대에게 소비는 단순한 지출 행위를 넘어, 자신의 가치관과 개성을 드러내는 중요한 자기표현의 수단이 되었습니다. 'Todo Mate'나 'Setlog'와 같은 서비스의 흥행에서 알 수 있듯, 자신의 일상과 목표를 기록하고 공유하며 또래와 동기부여를 주고받는 문화는 이미 청년 세대의 주요 트렌드로 자리 잡고 있습니다.

그러나 기존의 금융 및 자산관리 애플리케이션은 대부분 계좌, 카드, 보험, 소비 내역과 같은 금융 데이터를 숫자와 통계 중심으로 제공하는 데 집중되어 있습니다.

**MoneyLog는 이러한 한계를 해결하기 위해:**
- ✅ AI를 활용한 사용자 소비 데이터 분석
- ✅ 가계부 작성과 관리 자동화 지원
- ✅ 월별 소비 리포트 및 청년정책 추천
- ✅ 소셜 피드 기반 소비 공유 및 피드백

</details>

#### 핵심 목적


**금융 데이터의 '연결'과 '스토리화'를 통해 청년들이 자신만의 소비 방식을 자연스럽게 돌아볼 수 있는 소셜 금융 생태계 구축**

#### 세부 목적 및 기대 효과

| 구분 | 내용 |
|------|------|
| **금융의 소셜화** | 단순 지출 기록을 '금융 피드'로 전환, 또래 피드백을 통한 리텐션 극대화 |
| **정보 비대칭 해소** | 파편화된 청년정책/금융상품 정보를 맞춤형으로 제공 |
| **사용자 측면** | 시각적 피드로 심리적 거부감 낮추고 지속적인 기록 습관 형성 |
| **플랫폼 측면** | 소셜 피드 기반 높은 리텐션과 생활 밀착형 플랫폼 확장 |
| **사회적 측면** | 청년 혜택 정보 접근성 향상, 금융 이해도 문화 확산 |

### 개발 목표

```mermaid
graph LR
    A[Infrastructure] --> F[고가용성 시스템]
    B[Application] --> F
    C[DevOps] --> F
    D[Testing] --> F
    E[AI/ML] --> F
    
    A -->|EKS, Auto-scaling| A1[탄력적 인프라]
    B -->|MSA, Spring Boot| B1[금융 소셜 기능]
    C -->|Jenkins, GitLab CI| C1[자동화 파이프라인]
    D -->|JUnit, 통합 테스트| D1[품질 검증]
    E -->|LangGraph, Claude| E1[AI 추천]
```

| 목표 | 설명 |
|------|------|
| **Infrastructure** | Amazon EKS 기반 컨테이너 환경, Auto-scaling, 서버 이중화 |
| **Application** | Java/TypeScript 기반 MSA, 인증·인가, 소셜 피드 기능 |
| **DevOps** | Jenkins/GitLab CI/CD 파이프라인, 실시간 모니터링 |
| **Testing** | DB 무결성 검증, JUnit 단위/통합 테스트, 문서화 |
| **AI/ML** | 소비 패턴 분석, 개인화 추천, 청년정책/카드/보험 추천 |

---

## 기술 스택

### Backend

<p align="left">
<img src="https://img.shields.io/badge/Java%2017-007396?style=for-the-badge&logo=openjdk&logoColor=white"/>
<img src="https://img.shields.io/badge/Python%203-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring%20Boot%203.5-6DB33F?style=for-the-badge&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white"/>
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white"/>
</p>


### Frontend

<p align="left">
<img src="https://img.shields.io/badge/Next.js%2016-000000?style=for-the-badge&logo=next.js&logoColor=white"/>
<img src="https://img.shields.io/badge/React%2019-61DAFB?style=for-the-badge&logo=react&logoColor=black"/>
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
<img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white"/>
<img src="https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white"/>
</p>

### Infrastructure & DevOps

<p align="left">
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white"/>
<img src="https://img.shields.io/badge/Istio-466BB0?style=for-the-badge&logo=istio&logoColor=white"/>
<img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white"/>
<img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white"/>
<img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white"/>
</p>

### AI/ML & Messaging

<p align="left">
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white"/>
<img src="https://img.shields.io/badge/Claude%20AI-8B5CF6?style=for-the-badge&logo=anthropic&logoColor=white"/>
<img src="https://img.shields.io/badge/Neo4j-008CC1?style=for-the-badge&logo=neo4j&logoColor=white"/>
<img src="https://img.shields.io/badge/NATS-27AAE1?style=for-the-badge&logo=nats.io&logoColor=white"/>
<img src="https://img.shields.io/badge/Debezium-FF6600?style=for-the-badge&logo=debezium&logoColor=white"/>
</p>

<details>
<summary><b>전체 기술 스택 상세 보기</b></summary>

<br/>

#### Backend
- **Language**: Java 17, Python 3.x
- **Framework**: Spring Boot 3.5.14, FastAPI 0.115.0, Node.js + TypeScript
- **Database**: PostgreSQL, Redis
- **Message Queue**: NATS JetStream
- **CDC**: Debezium
- **AI/ML**: LangGraph, LangChain, Anthropic Claude, Neo4j, Sentence Transformers

#### Frontend
- **Framework**: Next.js 16.2.6, React 19
- **Language**: TypeScript 5.7.3
- **UI Library**: Radix UI, Tailwind CSS 4.2.0
- **State Management**: Apollo Client (GraphQL)
- **Data Visualization**: Recharts

#### Infrastructure & DevOps
- **Container**: Docker, Kubernetes (Amazon EKS)
- **Orchestration**: Terraform, Helm
- **Service Mesh**: Istio
- **CI/CD**: Jenkins, GitLab CI/CD
- **Monitoring**: Prometheus, Grafana, Loki, Tempo, Alloy, Grafana Faro
- **Observability**: OpenTelemetry, SonarQube

</details>

---

## 아키텍처


### 시스템 아키텍처

<img width="1384" alt="시스템아키텍처" src="https://github.com/user-attachments/assets/72edaf97-db0b-4e79-9380-15b96c2dcaf7" />

#### 아키텍처 설명

하이브리드 클라우드 구조로 AWS와 온프레미스 환경을 Site-to-Site VPN으로 연결했습니다.

| 환경 | 구성 요소 | 설명 |
|------|-----------|------|
| **AWS 클라우드** | EKS, Multi-AZ, ALB, WAF | 고가용성 확보, Istio 인그레스 게이트웨이 라우팅 |
| **온프레미스** | vSphere(ESXi), K8s | HAProxy + Keepalived 이중화, NATS JetStream |

### 소프트웨어 아키텍처

<img width="476" alt="소프트웨어아키텍처" src="https://github.com/user-attachments/assets/50d8238b-6743-4830-9b6e-d8176b1e085d" />

#### 아키텍처 설명

마이크로서비스 아키텍처(MSA) 기반으로 도메인별 서비스를 분리했습니다.

| 계층 | 설명 |
|------|------|
| **게이트웨이** | S3/CloudFront → ALB → Istio Gateway → BFF → Spring Cloud Gateway |
| **마이크로서비스** | Social, Alarm, Budget, Auth, AI 서비스 (Controller-Service-Component-DBIO) |
| **데이터 동기화** | 독립 DB 사용, CDC(Change Data Capture)로 비동기 전파 |

---

## 핵심 기능

### 핵심 기술 구성

<table>
<tr>
<td width="50%" valign="top">

#### AI & Data
1. **Graph RAG + Reranker 기반 AI**
   - 지식 그래프 형태 금융 데이터 관계 구성
   - 개인화된 소비 인사이트 제공

2. **Hot/Cold 데이터 아키텍처**
   - 자동화된 티어링으로 비용 최적화
   - 성능과 비용 동시 개선

</td>
<td width="50%" valign="top">

#### Infrastructure & DevOps
3. **실시간 이벤트 처리 (CDC)**
   - CQRS 패턴으로 읽기/쓰기 분리
   - 데이터 일관성 유지

4. **Istio 서비스 메시**
   - 카나리 배포로 무중단 배포
   - mTLS 암호화 통신

5. **AIOps 기반 인프라 운영**
   - SLO 기반 Error Budget 관리
   - AI 자동 근본 원인 분석

</td>
</tr>
</table>

### 통합 워크플로우

<img width="1294" alt="전체 워크플로우" src="https://github.com/user-attachments/assets/b212fefa-32a0-4377-b049-f00ff6290afa" />

---

### 세부 기능

> 각 기능을 클릭하면 상세 설명으로 이동합니다.


---

## 1. AI 기반 소비 분석 및 맞춤형 추천

### 기능 개요

LangGraph 기반 AI 파이프라인을 통해 사용자의 소비 패턴을 분석하고, 개인 맞춤형 금융상품과 청년정책을 자동 추천합니다.

<table>
<tr>
<td width="50%" valign="top">

**핵심 기술**
- LangGraph 9단계 DAG 파이프라인
- Hybrid Search (pgvector + Neo4j + Reranker)
- AWS Bedrock (Claude Haiku + Titan Embed)
- Neo4j Graph DB 관계 표현

</td>
<td width="50%" valign="top">

**성능 개선**
- 코사인 유사도: 0.19 → **0.35**
- 256차원 축소로 검색 속도 향상
- Ablation Study: 55.1점 → **72.6점**

</td>
</tr>
</table>

### 추천 파이프라인 흐름

```mermaid
graph LR
    A[Profile<br/>사용자 데이터] --> B[Embed<br/>가중 평균 임베딩]
    B --> C[VectorSearch<br/>상위 30개]
    C --> D[Rerank<br/>7개 압축]
    D --> E[Filter<br/>조건 필터링]
    E --> F[GraphExpand<br/>관계 조회]
    F --> G[Conflict<br/>중복 감지]
    G --> H[LLM<br/>추천 생성]
    H --> I[Save<br/>DB 저장]
```

<details>
<summary><b>핵심 코드 보기</b></summary>

```python
# app/domain/recommend_ai/graph.py - LangGraph 파이프라인 구성
from langgraph.graph import StateGraph, START, END

def build_recommend_graph():
    graph = StateGraph(RecommendState)
    
    # 노드 등록
    graph.add_node("profile", profile_node)
    graph.add_node("embed", embed_node)
    graph.add_node("vector_search", vector_search_node)
    graph.add_node("rerank", rerank_node)
    graph.add_node("filter", filter_node)
    graph.add_node("graph_expand", graph_expand_node)
    graph.add_node("conflict", conflict_node)
    graph.add_node("llm", llm_recommend_node)
    graph.add_node("save", save_node)
    
    # 에지 연결
    graph.add_edge(START, "profile")
    graph.add_conditional_edges("profile", _has_error, {
        "save": "save", 
        "continue": "embed"
    })
    # ... (생략) ...
    
    return graph.compile()
```

**코드 링크**: [LangGraph Pipeline](https://github.com/5kstration/ai-service-be/blob/main/app/domain/recommend_ai/graph.py) | [Embedding Node](https://github.com/5kstration/ai-service-be/blob/main/app/domain/recommend_ai/nodes.py)

</details>

---

## 2. 실시간 이벤트 처리 및 CDC 기반 데이터 동기화

### 기능 개요

Debezium CDC와 NATS JetStream을 활용한 이벤트 기반 아키텍처로 데이터 일관성을 보장하면서 실시간 처리를 구현했습니다.


<table>
<tr>
<td width="50%" valign="top">

**핵심 아키텍처**
- Debezium: PostgreSQL WAL 실시간 캡처
- NATS JetStream: Pub/Sub 메시징
- Leaf Node: AWS EKS ↔ 온프레미스 연결
- CQRS: 읽기/쓰기 책임 분리

</td>
<td width="50%" valign="top">

**고가용성 보장**
- Durable Consumer (재시작 시 이어서 처리)
- Queue Group (중복 방지)
- Manual ACK (At-Least-Once 보장)
- Offset 저장 (재시작 복구)

</td>
</tr>
</table>

### 데이터 흐름

```
PostgreSQL → Debezium → NATS JetStream → AI/Alarm Service
   (WAL)      (CDC)      (Pub/Sub)        (Consumer)
```

<details>
<summary><b>핵심 코드 보기</b></summary>

```yaml
# debezium/aws_debezium/debezium-budget.yaml - CDC 설정
apiVersion: v1
kind: ConfigMap
metadata:
  name: debezium-budget-config
data:
  application.properties: |
    debezium.sink.type=nats-jetstream
    debezium.sink.nats-jetstream.url=nats://k8s_leaf:leaf_password@10.0.2.65:4222
    
    debezium.source.connector.class=io.debezium.connector.postgresql.PostgresConnector
    debezium.source.database.hostname=oka-budget.ctku6oc2yg75.ap-northeast-2.rds.amazonaws.com
    debezium.source.topic.prefix=budget-server
    debezium.source.plugin.name=pgoutput
```

**코드 링크**: [Debezium Config](https://github.com/5kstration/debezium/blob/main/aws_debezium/debezium-budget.yaml) | [NATS Consumer](https://github.com/5kstration/alarm-service-be/blob/main/src/main/java/com/project/backend/domain/notification/listener/NatsSocialEventListener.java)

</details>

---

## 3. Istio 기반 서비스 메시(Service Mesh) 및 트래픽 제어

### 기능 개요

Istio 서비스 메시와 Argo Rollouts를 결합하여 카나리 배포로 무중단 배포를 실현했습니다.

<table>
<tr>
<td width="50%" valign="top">

**핵심 기능**
- Envoy Sidecar 자동 주입
- 경로 기반 라우팅 (VirtualService)
- mTLS 암호화 통신
- Argo Rollouts 카나리 배포

</td>
<td width="50%" valign="top">

**배포 프로세스**
1. Canary Replica 생성 (0%)
2. 트래픽 점진 전환 (10%→30%→50%→100%)
3. LLM Judge 검증 (72점 이상)
4. 자동 롤백 (실패 시)

</td>
</tr>
</table>

<details>
<summary><b>핵심 코드 보기</b></summary>

```yaml
# infra/manifest/gateway-service/istio.yaml
apiVersion: networking.istio.io/v1beta1
kind: VirtualService
metadata:
  name: gateway-service-moneylog-vs
spec:
  hosts: ["*"]
  gateways: [moneylog-gateway]
  http:
    - match:
        - uri:
            prefix: "/graphql"
      route:
        - destination:
            host: bff-service
            port:
              number: 8085
```

**코드 링크**: [Istio Gateway](https://github.com/5kstration/infra/blob/main/manifest/gateway-service/istio.yaml) | [Jenkinsfile Canary](https://github.com/5kstration/ai-service-be/blob/main/Jenkinsfile)

</details>

---

## 4. Hot/Cold 데이터 아키텍처를 통한 데이터 라이프사이클 최적화

### 기능 개요

Hot Storage(S3)와 Cold Storage(MinIO)를 자동 티어링하여 성능과 비용을 동시에 최적화했습니다.


<table>
<tr>
<td width="50%" valign="top">

**저장소 구성**
- **Hot Storage (S3)**: 최근 30일 데이터
- **Cold Storage (MinIO)**: 30일 이상 데이터
- **Hybrid Cloud**: Site-to-Site VPN 연결

</td>
<td width="50%" valign="top">

**비용 절감**
- S3: $0.025/GB/월
- MinIO: ~$0.007/GB/월
- **월간 저장 비용 60% 절감**

</td>
</tr>
</table>

### 데이터 라이프사이클

```mermaid
graph LR
    A[HOT<br/>S3 업로드] --> B[ARCHIVING<br/>MinIO 복사]
    B --> C[BOTH<br/>체크섬 검증]
    C --> D[DELETING_HOT<br/>7일 대기]
    D --> E[COLD<br/>S3 삭제 완료]
```

**자동화 스케줄러**
- 📅 매일 03:00 KST: 아카이브 작업 (50개/배치)
- 📅 매일 03:30 KST: Hot 삭제 작업

<details>
<summary><b>핵심 코드 보기</b></summary>

```java
// FeedImageArchiveScheduler.java - 자동화 스케줄러
@Scheduled(cron = "0 0 3 * * *", zone = "Asia/Seoul")
public void archiveEligibleImages() {
    feedImageArchiveBatchService.archiveEligibleImages();
}

@Scheduled(cron = "0 30 3 * * *", zone = "Asia/Seoul")
public void deleteEligibleHotObjects() {
    feedImageHotDeletionService.deleteEligibleHotObjects();
}
```

**코드 링크**: [Archive Scheduler](https://github.com/5kstration/budget-service-be/blob/main/src/main/java/com/project/backend/domain/feedimage/service/FeedImageArchiveScheduler.java) | [MinIO StatefulSet](https://github.com/5kstration/budget-service-be/blob/main/k8s/minio/statefulset.yaml)

</details>

---

## 5. AIOps 및 SRE 기반의 고가용성 인프라 운영

### 기능 개요

Prometheus + Sloth로 SLO를 관리하고, AWS Lambda + Claude AI로 장애를 자동 분석하여 Slack으로 알림합니다.

<table>
<tr>
<td width="50%" valign="top">

**SLI/SLO 정의**
- Gateway: 99.0% 가용성, 500ms 레이턴시
- Core APIs: 99.0% 가용성
- AI Service: 95.0% 가용성, 30s 레이턴시
- CDC: 99.0% 시간 동안 3초 이내
- NATS: 99.0% 시간 동안 10k 미만

</td>
<td width="50%" valign="top">

**AIOps 효과**
- 평균 분석 시간(MTTR): **15초 이내**
- Slack 알림: 장애 후 **30초 이내**

</td>
</tr>
</table>

### AIOps 자동화 워크플로우

```mermaid
graph LR
    A[Prometheus<br/>SLO 감지] --> B[Alertmanager<br/>필터링]
    B --> C[SNS<br/>발행]
    C --> D[Lambda<br/>트리거]
    D --> E[Loki<br/>로그 수집]
    E --> F[Claude AI<br/>분석]
    F --> G[Slack<br/>알림]
```

<details>
<summary><b>핵심 코드 보기</b></summary>

```python
# aiops-lambda/lambda_function.py - AI 자동 분석
def lambda_handler(event, context):
    for record in event['Records']:
        alert_data = json.loads(record['Sns']['Message'])
        
        for alert in alert_data.get('alerts', []):
            if alert['status'] == 'firing':
                service_name = alert['labels'].get('service')
                
                # 1. Loki에서 로그 수집
                logs = get_loki_logs(service_name)
                
                # 2. Bedrock으로 AI 분석
                analysis = analyze_with_bedrock(alert_desc, logs)
                
                # 3. Slack으로 리포트 전송
                send_to_slack(alert_title, analysis)
```

**코드 링크**: [AIOps Lambda](https://github.com/5kstration/infra/blob/main/aiops-lambda/lambda_function.py) | [SLO Definitions](https://github.com/5kstration/infra/blob/main/manifest/monitoring/)

</details>

---


<div align="center">

---

### Contact & Links

[![GitHub Organization](https://img.shields.io/badge/GitHub-5kstration-181717?style=for-the-badge&logo=github)](https://github.com/5kstration)

**Made with ❤️ by Team 5kstration**

---

</div>
