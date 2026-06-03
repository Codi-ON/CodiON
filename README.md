# CodiON - AI 기반 날씨 코디 추천 서비스

> 날씨·일정·보유 의류 정보를 기반으로 오늘 입기 좋은 옷을 추천해주는 AI 서비스

<p align="center">
  <img src="https://github.com/user-attachments/assets/18011b07-4a46-4318-a298-18b61dbdac70" width="80%" alt="랜딩 페이지"/>
</p>

<br>

## 목차

1. [프로젝트 소개](#1-프로젝트-소개)
2. [주요 기능 화면](#2-주요-기능-화면)
3. [기술 스택](#3-기술-스택)
4. [시스템 아키텍처](#4-시스템-아키텍처)
5. [프로젝트 구조](#5-프로젝트-구조)
6. [실행 방법](#6-실행-방법)

---

## 1. 프로젝트 소개

**CodiON**은 사용자의 날씨 환경, 활동 유형, 보유 의류 데이터를 종합하여  
"오늘 입을 옷을 고민하는 시간과 비용"을 줄이기 위해 시작된 프로젝트입니다.

### 핵심 목표

- 날씨·환경·활동 맥락을 반영한 현실적인 옷 추천
- 단순 추천이 아닌 **체크리스트 기반 선택 보조**
- 추천 결과에 대한 사용자 피드백 수집 및 개선
- 데이터 기반 의사결정이 가능한 **관리자 대시보드** 제공

### AI 성과 요약

| 영역 | 개선 전 | 개선 후 |
|------|---------|---------|
| 소재 추천 모델 (R²) | 90% | **97%** |
| 소재 추천 모델 (MAE) | 5.1 | **3.89** |
| 의류 소재 분류 정확도 | 50% | **94%** |

---

## 2. 주요 기능 화면

### 랜딩 페이지
서비스 소개 및 로그인/회원가입 진입점

<p align="center">
  <img src="https://github.com/user-attachments/assets/18011b07-4a46-4318-a298-18b61dbdac70" width="80%" alt="랜딩 페이지"/>
</p>

---

### 로그인 / 회원가입
이메일 로그인 및 Google·Apple 소셜 로그인 지원

<p align="center">
  <img src="https://github.com/user-attachments/assets/5d5f1fde-0d91-4117-bc90-2f9592776080" width="80%" alt="로그인"/>
</p>

---

### 오늘의 코디
현재 날씨를 기반으로 AI가 오늘 입을 옷을 추천하고 날씨 리포트 제공</b>


<p align="center">
 <img width="1920" height="904" alt="main_2" src="https://github.com/user-attachments/assets/0174c01e-0116-485b-a63d-a2500d57e071" />
</p>

---

### 코디 추천 결과

<p align="center">
  <img src="https://github.com/user-attachments/assets/c05d4e4d-6d66-49d3-82f0-876a121730c1" width="80%" alt="코디 추천 결과"/>
</p>

---

### 활동 체크리스트
4단계 흐름(날씨 분석 → 활동 체크 → 스타일 생성 → 최종 제안)으로 추천 정확도 향상

<p align="center">
 <img width="1363" height="889" alt="체크리스트3" src="https://github.com/user-attachments/assets/d22968de-24e5-48a8-86f0-046b86af9bb1" />
</p>

---

### 나의 옷장
보유 의류를 카테고리·시즌별로 필터링하여 관리

<p align="center">
  <img src="https://github.com/user-attachments/assets/039bf374-40bf-42f9-99a7-32a0396abbf6" width="80%" alt="옷장 관리"/>
</p>

---

### 의류 등록
사진 업로드 시 AI가 소재·색상·계절·카테고리를 자동 분류 (정확도 94%)  

소재 제한 :`면, 폴리에스테르, 울, 실크, 린넨, 데님, 가죽, 나일론, 스판, Unknown`  

혼방율 제한 : 면,폴리

<p align="center">
  <img src="https://github.com/user-attachments/assets/a91a1daa-99e6-43d5-a09c-9d391014952b" width="80%" alt="의류 등록"/>
</p>

---

### 추천 히스토리

<p align="center">
  <img src="https://github.com/user-attachments/assets/3f5e61c8-1906-44f7-9f63-d5acc5988296" width="80%" alt="추천 히스토리"/>
 <img width="1140" height="647" alt="히스토리" src="https://github.com/user-attachments/assets/ea2ae22f-7be2-499a-80bc-8a66eef0b942" />

</p>

---

### 히스토리 캘린더
날짜별 코디 이력 및 당일 날씨·미션·피드백 조회

<p align="center">
  <img src="https://github.com/user-attachments/assets/0a48af19-4608-414b-9d42-a6ec53f4aaf9" width="80%" alt="캘린더"/>
</p>

---

### 챗봇 기능
n8n을 이용하여 gemini 2.0 flash를 탑재하고 프롬프트를 입력하여 CodiON 시스템에 관한 질의응답

<p align="center">
<img width="404" height="519" alt="챗봇1" src="https://github.com/user-attachments/assets/04d0485c-e687-4b59-b080-4d97e8e11526" />
<img width="387" height="502" alt="챗봇2_2(날씨api 후)" src="https://github.com/user-attachments/assets/c8c0f962-bbae-4439-a32e-1249051f7f7f" />
</p>

---

### 관리자 대시보드
일별 세션·클릭 이벤트, Top N 아이템, KPI 지표 실시간 확인

<p align="center">
  <img src="https://github.com/user-attachments/assets/c2fa063a-2ab6-45ed-8a40-7366c50c73e0" width="80%" alt="관리자 대시보드"/>
</p>

---

## 3. 기술 스택

### Frontend

| 구분 | 기술 |
|------|------|
| 프레임워크 | React 18, Vite, TypeScript |
| 상태 관리 | Zustand |
| UI | Tailwind CSS |

### Backend

| 구분 | 기술 |
|------|------|
| 프레임워크 | Java 17, Spring Boot |
| 데이터베이스 | PostgreSQL 16 |
| API 문서 | Swagger UI |

### AI / ML

| 구분 | 기술 |
|------|------|
| API 서버 | FastAPI, Python |
| 추천 모델 | LightGBM, PMV (ISO 7730 기반) |
| 소재 분류 | Gemini 2.0 Flash (n8n 워크플로) |
| 날씨 데이터 | OpenWeather API |

### 워크플로 & 인프라

| 구분 | 기술 |
|------|------|
| 워크플로 자동화 | n8n |
| LLM | Google Gemini 2.0 Flash |
| 컨테이너 | Docker, Docker Compose |
| 배포 | AWS EC2 |
| 데이터베이스 | PostgreSQL (서비스 DB + n8n DB 분리) |

---

## 4. 시스템 아키텍처

```
┌─────────────────────────────────────────────────────────────────────┐
│                         CodiON 시스템 아키텍처                        │
└─────────────────────────────────────────────────────────────────────┘

                            ┌───────────────┐
                            │   Frontend    │
                            │ React / Vite  │
                            └───────┬───────┘
                                    │
             ┌──────────────────────┼──────────────────────┐
             │                      │                      │
             ▼                      ▼                      ▼
     ┌───────────────┐      ┌───────────────┐      ┌───────────────┐
     │  /api         │      │  /api/n8n     │      │  OpenWeather  │
     │  Spring Boot  │      │  (n8n Proxy)  │      │  (외부 API)   │
     │  :8080        │      └───────┬───────┘      └───────┬───────┘
     └───────┬───────┘              │                      │
             │                      ▼                      │
             │              ┌───────────────┐              │
             │              │   codi_n8n    │◄─────────────┘
             │              │   :5678       │   날씨 데이터
             │              │  ├ 챗봇        │
             │              │  ├ 일일 코멘트  │
             │              │  └ 이미지 분석  │
             │              └───────────────┘
             │
             ▼
     ┌───────────────┐
     │  codion-ai    │
     │  FastAPI :8000│
     │  ├ /blend-ratio│
     │  └ /material_ │
     │     ratio     │
     └───────┬───────┘
             │
     ┌───────┴───────┐
     ▼               ▼
┌─────────┐   ┌─────────────────────────┐
│ blend_  │   │  material_weather        │
│ ratio   │   │  LightGBM + PMV 보정    │
│ 모델    │   │  (R² 97%, MAE 3.89)     │
└─────────┘   └─────────────────────────┘
             │
             ▼
     ┌───────────────┐
     │  PostgreSQL   │
     │  :5432        │
     │  (서비스 DB   │
     │   + n8n DB)   │
     └───────────────┘
```

### 데이터 플로우 - 소재 추천

```
1. 사용자 추천 요청 (Frontend)
   └─> Spring Boot Backend (ClothingRecommendationService)

2. AI 서비스 호출
   └─> POST /recommend/material_ratio (FastAPI)

3. 모델 추론 (predictor.py)
   └─> 소재 물성 조회 (warmth, breathability, water_res)
   └─> LightGBM 예측 (temp, humidity, precip, wind, temp_diff + 소재물성)

4. 응답 반환
   └─> { clothingId, material_name, materialRatioScore, analysis }
```

### n8n 워크플로 연동

| 기능 | Webhook | 연동 |
|------|---------|------|
| 챗봇 | `/webhook/chat` | Gemini 2.0 Flash |
| 일일 날씨 코멘트 | `/webhook/daily-comment` | OpenWeather API + Gemini |
| 이미지 소재 분석 | `/webhook/analyze-image` | Gemini Vision (94% 정확도) |

---

## 5. 프로젝트 구조

```
CodiON/
├── frontend/                      # React + Vite + TypeScript
│   └── src/
│       ├── pages/
│       │   ├── user/              # 사용자 화면
│       │   │   ├── TodayPage.tsx          # 오늘 코디 추천
│       │   │   ├── RecommendationPage.tsx # 추천 결과
│       │   │   ├── ChecklistPage.tsx      # 체크리스트
│       │   │   ├── ClosetPage.tsx         # 옷장 관리
│       │   │   ├── CalendarPage.tsx       # 캘린더
│       │   │   ├── HistoryPage.tsx        # 추천 히스토리
│       │   │   └── MyPage.tsx             # 마이페이지
│       │   ├── admin/             # 관리자 대시보드
│       │   ├── auth/              # 로그인/회원가입
│       │   └── landing/           # 랜딩 페이지
│       ├── app/                   # 라우팅, 레이아웃, 프로바이더
│       ├── shared/                # 공통 컴포넌트, API
│       └── state/                 # Zustand 전역 상태
│
├── backend/                       # Spring Boot (Java 17)
│   └── src/main/java/com.codion.backend/
│       ├── api/
│       │   ├── controller/        # REST 컨트롤러
│       │   ├── service/           # 비즈니스 로직
│       │   └── dto/               # 요청/응답 DTO
│       ├── domain/
│       │   ├── entity/            # JPA 엔티티
│       │   ├── repository/        # DB 접근
│       │   └── enum/              # 도메인 열거형
│       └── global/
│           ├── config/            # Spring 설정
│           └── exception/         # 전역 예외 처리
│
├── ai/                            # Python AI 서비스
│   ├── ml_api/                    # FastAPI 서버
│   │   └── api/
│   │       ├── routers/           # /recommend 엔드포인트
│   │       └── services/
│   │           ├── predictor.py   # WeatherRecommender (PMV 모델)
│   │           └── material_data.py  # 소재 물성 DB
│   ├── material_weather/          # 소재 추천 ML 모델
│   │   └── ml/
│   │       ├── pipeline/
│   │       │   └── train_model_pmv.py  # PMV 보정 + LightGBM 학습
│   │       └── artifacts/
│   │           └── weather_material_pmv.pkl
│   └── ratio_based/               # 블렌드 비율 추천 모델
│
├── infra/                         # 인프라 설정
├── n8n_data/                      # n8n 워크플로 데이터
├── docker-compose.yaml            # 전체 서비스 오케스트레이션
└── docs/                          # 문서
    ├── Data_Contract.md           # Spring ↔ AI 데이터 계약
    └── material.md                # Material/n8n 담당 아키텍처
```

---

## 6. 실행 방법

### 사전 요구사항

- Docker Desktop
- Docker Compose v2

### 환경 변수 설정

프로젝트 루트에 `.env` 파일 생성:

```env
# Database
POSTGRES_DB=codion
POSTGRES_USER=codion
POSTGRES_PASSWORD=1234

# Spring Boot
SPRING_DATASOURCE_URL=jdbc:postgresql://db:5432/codion
SPRING_DATASOURCE_USERNAME=codion
SPRING_DATASOURCE_PASSWORD=1234

# OpenWeather API
OPENWEATHER_API_KEY=your_api_key_here
```

### Docker Compose로 전체 실행

```bash
# 전체 서비스 빌드 및 실행
docker-compose up -d

# 로그 확인
docker-compose logs -f

# 서비스 종료
docker-compose down
```

### 서비스 포트

| 서비스 | URL |
|--------|-----|
| Frontend | http://localhost:5173 |
| Backend (Swagger) | http://localhost:8080/swagger-ui.html |
| AI API | http://localhost:8000 |
| n8n 워크플로 | http://localhost:5678 |
| PostgreSQL | localhost:5434 |

### 로컬 개발 환경

**Frontend**

```bash
cd frontend
npm install
npm run dev
```

**Backend**

```bash
cd backend
./gradlew bootRun
```

**AI 서비스**

```bash
cd ai
pip install -r ml_api/requirements.txt
uvicorn ml_api.api.main:app --reload --port 8000
```

### 헬스체크 확인

```bash
# Backend
curl http://localhost:8080/actuator/health

# AI 서비스
curl http://localhost:8000/recommend/blend-ratio/health
curl http://localhost:8000/recommend/material_ratio/health
```
