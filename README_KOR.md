# 📦 StoryTracks

StoryTracks는 위치 기반 게시물을 통해 개인의 이야기를 기록하고 공유할 수 있도록 설계된 모바일 중심 웹 애플리케이션입니다.  
사용자는 사진을 업로드하고, 위치와 시간 같은 메타데이터, 텍스트 또는 음성 입력을 활용해 고유한 게시물을 만들 수 있습니다.

또한 Gemini API를 통해 사진을 기반으로 매력적인 콘텐츠를 자동 생성하며,  
Google Maps API 기반의 지도 피드를 통해 다른 사람들의 게시물을 탐색할 수 있고,  
로그인/로그아웃과 같은 인증 기능, 반응(좋아요 등) 기능도 포함되어 있습니다.

Frameworks: Spring Boot (백엔드), NextJS (프론트엔드), AWS (MySQL RDS, Amazon S3)

---

## 🧱 리포지토리 구조

StoryTracks는 하나의 프로젝트를 세 개의 모듈형 리포지토리로 나누어 구성되어 있습니다:

- **[StoryTracks-fe](https://github.com/T4-StoryTracks/fe)**  
  **Next.js 기반의 프론트엔드**  
  사용자 인터페이스, 페이지 라우팅, Google Maps API 및 Gemini API 연동을 담당합니다.

- **[StoryTracks-be](https://github.com/T4-StoryTracks/be)**  
  **Spring Boot 기반의 백엔드**  
  사용자 인증, 게시물 처리, 핵심 비즈니스 로직을 관리합니다.

- **[StoryTracks-infra](https://github.com/T4-StoryTracks/infra)**  
  **인프라 및 배포 설정 리포지토리**  
  AWS 리소스 설정, 데이터베이스 구성, CI/CD 파이프라인 등을 포함합니다.

이러한 구조는 각 구성 요소를 독립적으로 개발 및 유지보수할 수 있게 하며, 서비스 간의 유기적인 통합을 보장합니다.

---

## 🤔💭 아이디어는 어떻게 시작됐을까요?

<img src="/imgs/1.png" width="50%" height="auto">
<img src="/imgs/2.png" width="50%" height="auto">
<img src="/imgs/3.png" width="50%" height="auto">

---

## 🥁 StoryTracks 사용법

**🗺️📍 내 주변의 게시물을 탐색해보세요!**

<img src="/imgs/4.png" width="30%" height="auto"><img src="/imgs/5.png" width="30%" height="auto">

<br>

**🔮✨ 사진을 기반으로 AI가 자동으로 글을 작성해줍니다!**

<img src="/imgs/6.png" width="30%" height="auto"><img src="/imgs/7.png" width="30%" height="auto">
<br><br>

메타데이터가 포함된 사진을 선택하고

<img src="/imgs/8.png" height="400px"><img src="/imgs/9.png" height="400px">
<br><br>

사용자 내용을 입력하고 AI 텍스트를 생성해보세요!

<img src="/imgs/10.png" width="25%" height="auto"><img src="/imgs/11.png" width="25%" height="auto"><img src="/imgs/12.png" width="25%" height="auto"><img src="/imgs/13.png" width="25%" height="auto">
