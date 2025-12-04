# 📦 StoryTracks

**StoryTracks는 위치 기반 게시물을 중심으로 개인의 경험을 기록하고 공유할 수 있는 모바일 최적화 웹 애플리케이션입니다.**  
사용자는 사진을 업로드하고, 위치·시간 정보와 텍스트를 입력하여 자신만의 게시물을 만들 수 있습니다.

Gemini API 기반 AI 요약 생성, Google Maps 기반 지도 피드 탐색,  
그리고 인증 및 좋아요 기능을 제공하여 풍부한 사용자 경험을 제공합니다.

Frameworks: Spring Boot (백엔드), NextJS (프론트엔드), AWS (Amazon S3), PostgreSQL, Redis


---

## 🚀 Tech Stack

**Frontend**
- Next.js  
- React  
- Google Maps API  
- Gemini API  

**Backend**
- Spring Boot  
- Spring Security  
- JPA / QueryDSL  
- PostgreSQL  
- Redis  
- AWS S3  

---

## 🧱 Repository Structure

| Repo | Description |
|------|-------------|
| **[StoryTracks-fe](https://github.com/julsweonCodes/StoryTracks-fe)** | Next.js 기반 프론트엔드. UI, 라우팅, Google Maps 및 Gemini API 연동 담당. |
| **[StoryTracks-be](https://github.com/julsweonCodes/StoryTracks-be-new)** | Spring Boot 기반 백엔드. 인증, 게시물 처리, API 및 비즈니스 로직 제공. |

---
## 🥁 StoryTracks 사용법

## ✨ 주요 기능

### 🗺️ 위치 기반 게시물 탐색
- Google Maps에서 전 세계 사용자의 게시물 탐색<br>
 <img src="/imgs/new-2.png" width="30%" height="auto"><img src="/imgs/new-1.png" width="30%" height="auto"><img src="/imgs/new-3.png" width="30%" height="auto">
<br>
- 지도 마커 클릭 시 해당 지역 게시물 목록 확인<br> 
  <img src="/imgs/feed-list.png" width="30%" height="auto">
  <br>

### 🔮 AI 기반 요약 생성하여 게시물 작성
- 사진 업로드, 대표 이미지의 위치 정보 추가<br>
 <img src="/imgs/new-7.png" width="30%" height="auto"><img src="/imgs/new-5.png" width="30%" height="auto"><img src="/imgs/new-6.png" width="30%" height="auto">
<br>

- 원하는 글쓰기 스타일 지정하여 Gemini API로 이미지·텍스트 분석 후 요약문 자동 생성<br>
<img src="/imgs/new-8.png" height="400px"><img src="/imgs/new-9.png" height="400px">
<br>

### 👤 My Blog

- 작성한 게시물을 한 곳에서 관리  
- 프로필 및 정보 관리  
 <img src="/imgs/new-10.png" height="400px"><img src="/imgs/new-11.png" height="400px">
<br>

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

## ⚙️ 주요 기술 구현 (Backend)
| 기능 영역                                     | 상세 내용                                                                                                            |
| ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **지도 기반 클러스터링 & 지역별 피드 조회**               | - 이미지 위도·경도 기반 클러스터링(도시/도/국가 단위)<br>- Spring Scheduler 기반 12시간 주기 이미지 클러스터링 배치 작업<br>- Google Maps API 응답 속도 최적화 |
| **JWT 기반 인증/인가 시스템**                      | - Access Token 기반 사용자 인증<br>- 게시물 작성/수정/삭제, 좋아요 등 액션 권한 제어  |
| **Redis 캐싱 기반 성능 최적화**                    | - 지도 기반 피드·게시물 목록 캐싱 전략 적용<br>- API 응답 속도 개선 및 서버 부하 감소                                                                            
| **Docker 기반 개발 환경 구성**                    | - Backend Dockerfile 작성<br>- 로컬/개발 환경에서 일관된 실행 환경 확보                                                             |

## 📌 향후 추가될 기능
- 댓글 기능
- 팔로우 기반 피드
- 모바일 UI 최적화
