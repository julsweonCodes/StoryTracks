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
| **StoryTracks-fe** | Next.js 기반 프론트엔드. UI, 라우팅, Google Maps 및 Gemini API 연동 담당. |
| **StoryTracks-be** | Spring Boot 기반 백엔드. 인증, 게시물 처리, API 및 비즈니스 로직 제공. |

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

## 📌 향후 추가될 기능
- 댓글 기능
- 팔로우 기반 피드
- 모바일 UI 최적화