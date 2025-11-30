# 📦 StoryTracks

StoryTracks는 위치 기반 게시물을 통해 개인의 이야기를 기록하고 공유할 수 있도록 설계된 모바일 중심 웹 애플리케이션입니다.  
사용자는 사진을 업로드하고, 위치와 시간 같은 메타데이터, 텍스트 또는 음성 입력을 활용해 고유한 게시물을 만들 수 있습니다.

또한 Gemini API를 통해 사진을 기반으로 매력적인 콘텐츠를 자동 생성하며,  
Google Maps API 기반의 지도 피드를 통해 다른 사람들의 게시물을 탐색할 수 있고,  
로그인/로그아웃과 같은 인증 기능, 반응(좋아요 등) 기능도 포함되어 있습니다.

Frameworks: Spring Boot (백엔드), NextJS (프론트엔드), AWS (Amazon S3), PostgreSQL, Redis

---

## 🧱 리포지토리 구조

StoryTracks는 다음과 같이 나누어 구성되어 있습니다:

- **[StoryTracks-fe](https://github.com/julsweonCodes/StoryTracks-fe)**  
  **Next.js 기반의 프론트엔드**  
  사용자 인터페이스, 페이지 라우팅, Google Maps API 및 Gemini API 연동을 담당합니다.

- **[StoryTracks-be](https://github.com/julsweonCodes/StoryTracks-be-new)**  
  **Spring Boot 기반의 백엔드**  
  사용자 인증, 게시물 처리, 핵심 비즈니스 로직을 관리합니다.\

---

## 🥁 StoryTracks 사용법

**🗺️📍 내 주변의 게시물을 탐색해보세요!**
Google Maps API의 마커를 통해 전세계에서 업로드 된 게시물을 찾아보세요

<img src="/imgs/4.png" width="30%" height="auto"><img src="/imgs/5.png" width="30%" height="auto">

<br>

**🔮✨ 내가 원하는 스타일로 내가 쓴 블로그글의 AI 요약을 작성해보세요!**

<img src="/imgs/6.png" width="30%" height="auto"><img src="/imgs/7.png" width="30%" height="auto">
<br><br>

메타데이터가 포함된 사진을 선택하거나 대표 이미지의 위치 정보를 입력하고

<img src="/imgs/8.png" height="400px"><img src="/imgs/9.png" height="400px">
<br><br>

원하는 블로그 글 스타일을 입력하고 AI 요약을 생성해보세요!

<img src="/imgs/10.png" width="25%" height="auto"><img src="/imgs/11.png" width="25%" height="auto"><img src="/imgs/12.png" width="25%" height="auto"><img src="/imgs/13.png" width="25%" height="auto">
