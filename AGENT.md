# Architecture Lab – AGENT.md

## 🎯 목적
이 레포의 목적은 시스템 설계 능력을 6개월간 체계적으로 훈련하는 것이다.

목표는 지식 습득이 아니라 다음 능력의 체화이다:

- 제약 조건 하에서의 의사결정
- 트레이드오프 명문화
- 병목 및 장애 시나리오 식별
- 장기 유지 가능성 판단

AI는 설계를 대신하지 않는다.  
AI는 비평가이자 검증자 역할만 수행한다.

---

## 🧠 운영 원칙

### 1. AI 금지 구간
- 문제 정의
- 1차 설계

위 두 단계는 반드시 사람이 직접 작성한다.

### 2. 문서화 원칙
머릿속 설계는 인정하지 않는다.  
문서로 남은 설계만 인정한다.

### 3. 정답 찾기 금지
설계는 선택이다.
모든 선택은 비용과 리스크를 동반한다.

---

## 📁 폴더 구조

/designs
/adrs
/reviews
/templates
/artifacts

---

## 🔁 주간 루틴 (6~8시간)

### Step 1. 문제 정의 (1시간)
파일:

designs/Wxx-topic/01-requirements.md

포함 항목:
- 시스템 목표 / 비목표
- 트래픽 가정 (DAU / QPS / Peak)
- SLA / SLO
- 데이터 특성
- 제약 조건 (예산/인력/기술/운영)

---

### Step 2. 1차 설계 (2시간, AI 금지)
파일:

designs/Wxx-topic/02-design-v1.md

포함 항목:
- High-level architecture
- 컴포넌트 설명
- 데이터 흐름
- 데이터 모델
- 핵심 기술 선택

---

### Step 3. 트레이드오프 명문화 (1시간)
파일:

designs/Wxx-topic/03-tradeoffs.md

각 선택에 대해:
- 왜 이 선택인가?
- 대안은 무엇인가?
- 비용/운영/확장/리스크 관점 분석

---

### Step 4. AI 리뷰 (1시간)
파일:

reviews/Wxx-topic-review.md

AI에게 요구할 것:
- 병목 TOP 5
- SPOF 식별
- 10배 트래픽 시 문제
- 정합성/중복 처리 전략 검증
- 보안/운영 관점 질문

---

### Step 5. 수정 설계 (1~2시간)
파일:

designs/Wxx-topic/04-design-v2.md
adrs/ADR-xxx-title.md

---

## ✅ 완료 기준 (Definition of Done)

아래가 모두 존재해야 완료:

- 요구사항 문서
- 설계 v1
- 트레이드오프 문서
- 리뷰 문서
- 설계 v2
- 최소 1개 ADR

---

## 🔎 필수 검증 질문

- 가장 먼저 깨지는 지점은?
- 데이터 유실 가능성은?
- 재처리 안전성은?
- 캐시 무효화 전략은?
- 장애 시 degrade 전략은?
- 운영 지표는 무엇인가?
- 비용 상한은?

---

## 📌 커밋 규칙

- Wxx: topic v1
- Wxx: topic v2 + ADR

