# 📦 StoryTracks

**StoryTracks는 위치 기반으로 경험을 기록·탐색할 수 있는 소셜 블로그 플랫폼입니다.**  
사용자는 사진 업로드 → 위치·시간 메타데이터 분석 → 게시물 작성까지 한 번에 진행하며,  
Google Maps 위에서 전 세계 사용자들의 기록을 탐색할 수 있습니다.

✨ **Try it now → https://story-tracks.vercel.app/**

---

## 🚀 Tech Stack

### **Frontend**
- Next.js (App Router)
- React
- Google Maps API  
- Gemini API  

### **Backend**
- Spring Boot  
- Spring Security (JWT)  
- JPA / QueryDSL  
- PostgreSQL  
- Redis Cache  
- AWS S3  

### **DevOps**
- **AWS EC2 운영 환경**
- **Docker / Docker Compose 기반 컨테이너 구성**
- **GitHub Actions — Backend 자동 배포 파이프라인 구축**
- **Vercel — Frontend Hosting**

---

## 🧱 Repository Structure
| Repo | Description | 
|------|-------------| 
| **[StoryTracks-fe](https://github.com/julsweonCodes/StoryTracks-fe)** | Next.js 기반 프론트엔드. UI, 라우팅, Google Maps 및 Gemini API 연동 | 
| **[StoryTracks-be](https://github.com/julsweonCodes/StoryTracks-be-new)** | Spring Boot 기반 백엔드. 인증, 게시물 처리, API 및 비즈니스 로직 제공. |

---

## ✨ 주요 기능

### 🗺️ 위치 기반 게시물 탐색
- 지도 위 클러스터링된 게시물 탐색  
- 지역 마커 클릭 시 해당 위치 게시물 리스트 노출

### 🔮 AI 요약 기반 게시물 작성
- 이미지 메타데이터(위경도/시간) 분석  
- Gemini API 기반 요약문 자동 생성  
- 글쓰기 스타일 지정 기능 제공

### 👤 My Blog
- 작성한 게시물 관리  
- 블로그 정보 및 프로필 관리

---

## 🧩 Architecture Overview

```
            ┌───────────────────────┐
            │     Frontend          │
            │       (Next.js)       │
            └────────────┬──────────┘
                         │
                         ▼
            ┌────────────────────────┐
            │     Backend API        │
            │      (Spring Boot)     │
            └────────────┬───────────┘
                         │
        ┌────────────────┴────────────────┐
        │                                 │
        ▼                                 ▼
┌──────────────────┐            ┌─────────────────┐
│   Database       │            │      Cache      │
│   PostgreSQL     │            │      Redis      │
└──────────┬───────┘            └─────────┬───────┘
           │                              │
           ▼                              │
┌─────────────────────────┐               │
│        AWS S3           │               │
│     (Image Storage)     │               │
└──────────┬──────────────┘               │
           │                              │
           ▼                              ▼
   ┌────────────────────────────────────────────┐
   │      External APIs (Google Maps, Gemini)   │
   └────────────────────────────────────────────┘
```


---

## 🔧 Backend – 주요 기술 구현

| 기능 영역 | 상세 내용 |
|----------|-----------|
| **지도 기반 클러스터링 & 지역 피드 조회** | 위·경도 기반 정밀도(1~3) 클러스터링, Redis 캐싱으로 응답 최적화 |
| **JWT 인증/인가** | 사용자 검증 및 게시물/좋아요 접근 권한 제어 |
| **Redis Caching** | 사용자 이미지 클러스터, 지역 기반 게시물 캐싱 → 응답 속도 향상 |
| **AWS S3 이미지 저장소 연동** | Multipart 업로드 및 이미지 경로 관리 |
| **Docker & CI/CD** | Dockerfile + docker-compose.prod.yml 구축, **GitHub Actions로 EC2 자동 배포** |

---

## 📌 향후 추가 기능
- 댓글 기능
- 팔로우 기반 추천 피드
- 모바일 UI 고도화
- 소셜 공유 기능


