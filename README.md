# Azure-Stock-Learning-System
# EasyStock: AI 기반 주식 투자 교육 시뮬레이터

> AI가 만들어내는 가장 현실적인 주식 시장, 그리고 완벽한 학습 루프
> 사용자의 레벨에 맞는 주식용어, 개념에 대한 퀴즈와 레벨업을 위한 퀘스트 그리고
행동경제학 기반 생성형 에이전트 사회를 활용하여  
실제 증권시장과 유사한 환경에서 투자를 하고 투자 성향별 전략을 학습할 수 있도록 설계된  
Azure 클라우드 기반 AI 투자 교육 플랫폼입니다.

---

## Demo Video

[![EasyStock Demo Video](https://img.youtube.com/vi/EAhGR9fCeow/hqdefault.jpg)](https://youtu.be/EAhGR9fCeow)
> Click the image to watch the full demo video.

---

## 기획 배경

- 이론 중심 투자 교육의 한계
- 실전 투자 경험 부족으로 인한 심리적 오류 반복
- 단순 시세 반영형 모의투자 플랫폼의 구조적 한계
- 생성형 AI 기반 실전형 학습 환경 필요성

단순 모의투자가 아닌,  
**AI 시장과 상호작용하는 실전형 학습 플랫폼**을 목표로 설계했습니다.

---

## 서비스 핵심 가치

- 행동경제학 기반 투자 심리 학습
- 실시간 AI 에이전트 시장과의 상호작용
- 개인화 AI 멘토 피드백 시스템
- 비용 최적화를 고려한 상용화 가능 구조

---

# 주요 기능

---

## 1️. 생성형 에이전트 사회 (Agent Society)

- 500명 규모 AI 투자자 생태계 구축
- 고래/개미 자본 규모 분리
- 가치/모멘텀/역발상 전략 성향 부여
- 탐욕·공포·군중심리 파라미터 반영
- 인간 투자 심리 74% 유사도 구현 (백테스팅 기준)
<img width="350" height="700" alt="스크린샷 2026-02-11 193459" src="https://github.com/user-attachments/assets/9c3761f6-2f65-4a3f-9f4f-e81d10ec4374" />
<img width="350" height="720" alt="스크린샷 2026-02-12 095528" src="https://github.com/user-attachments/assets/b2d63d22-6da3-49d1-b619-733bea032078" />

---

## 2. AI 멘토 대시보드

- 4가지 투자 철학 기반 멘토 구성
  - 가치 투자형 (안정형)
  - 퀀트 전략형 (공격형)
  - 모멘텀 전략형 (공격형)
  - 역발상 전략형 (비관형)
- 실시간 포트폴리오 분석
- 매매 기록 기반 개인화 피드백
- 양방향 챗봇 인터페이스 지원
<img width="333" height="688" alt="image" src="https://github.com/user-attachments/assets/7a01c920-c919-4a85-bba6-71a30b940a29" />
<img width="335" height="685" alt="image" src="https://github.com/user-attachments/assets/7ee6cef9-b6fb-4c21-9eb1-046c9529b576" />

---

## 3. 레벨 기반 학습 시스템

- Beginner → Expert 단계별 구조
- 퀘스트 & 퀴즈 시스템
- "개념 → 실습 → 피드백 → 전략 수정" 학습 루프
- 행동 데이터 기반 성장 지표 제공
<img width="306" height="606" alt="image" src="https://github.com/user-attachments/assets/15956338-8d7f-48c1-a3c7-579948204096" />
<img width="300" height="600" alt="image" src="https://github.com/user-attachments/assets/f1cfd3b2-d210-495a-9ba4-ad699af8be40" />
<img width="301" height="601" alt="image" src="https://github.com/user-attachments/assets/4b77bf72-5ec1-43df-ba22-9c0527cdca8b" />



---

# 기술적 챌린지 및 해결

---

## 🔹 LLM API 비용 폭증 문제

### 문제
- 500명 에이전트가 매 틱마다 뉴스 분석 수행
- Azure OpenAI 토큰 비용 급증

### 해결
- 메타 휴리스틱 기반 워크플로우 최적화
  - Genetic Algorithm (GA)
  - Simulated Annealing (SA)
- 프롬프트 압축률 최적화
- 동적 라우팅 구조 설계
- 자가 검증 노드 배치 구조 개선

### 결과
- API 비용 49.5% 절감
- 에이전트 지능 점수 93.4 유지
- 파레토 최적점 도달

---

## 🔹 Human-in-the-Loop 병목 현상

### 문제
- AI 주문 대기열로 인한 사용자 체결 지연

### 해결
- Market Maker 기반 동적 유동성 공급 로직 설계
- 정상 호가 범위 내 즉시 체결 구조 구현

### 결과
- 사용자 주문 1초 이내 체결
- 체감 UX 대폭 개선

---

## 🔹 DB 과부하 문제

### 문제
- trades 테이블 수십만 건 누적
- Full Table Scan 발생

### 해결
- Timestamp 인덱싱 적용
- 거래량 계산 로직 비동기 분리
- 메모리 플러시 스크립트 설계

---

# 시스템 아키텍처

4-Tier 구조

- Client (React)
- Backend (FastAPI)
- AI Service (Azure OpenAI)
- Database (Azure PostgreSQL)
<img width="568" height="219" alt="image" src="https://github.com/user-attachments/assets/00883194-aad1-4bff-a2e0-08a06b8dbacd" />

---


# 데이터 파이프라인
<img width="799" height="539" alt="image" src="https://github.com/user-attachments/assets/1ed8f0d3-01d2-43e9-b7f0-b13eefd502c1" />


---


# 기술 스택

<img width="6000" height="258" alt="image" src="https://github.com/user-attachments/assets/cea14294-0e17-4c44-8d8e-fcf23b0be320" />
| 영역 | 기술 |
|------|------|
| Frontend | React, Vite |
| Backend | FastAPI, Uvicorn, Python Asyncio |
| AI | Azure OpenAI (GPT-4o, GPT-4o-mini) |
| Infra | Azure App Service |
| DB | Azure PostgreSQL |
| Algorithm | Genetic Algorithm, Simulated Annealing |


---

# 👩‍💼 Role (기획)

- 인앱 UI/UX 정보 구조 설계
- 사용자 학습 동선 및 인터랙션 설계
- AI 멘토 피드백 UX 기획
- 행동경제학 기반 학습 루프 구조 설계
- 기술 제약을 고려한 서비스 구조 기획
- 시연 영상 스토리라인 구성 및 제작

---

# 📊 Impact

- Azure OpenAI API 비용 49.5% 절감
- 사용자 주문 Sub-second 체결 구조 구현
- 대규모 생성형 에이전트 기반 상용화 가능 아키텍처 설계
- 실전형 투자 학습 플랫폼 완성
