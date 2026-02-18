---
title: "Resume"
description: "Sungbeen Kim 경력 및 기술"
summary: "Android 개발자 Sungbeen Kim의 경력과 기술"
showDate: false
showAuthor: true
showLikes: true
showReadingTime: false
showTableOfContents: true
---

## 👨‍💻 Work Experience

### TBU <span class="resume-chip">2022.01.10 ~ 현재</span>

<div class="resume-company-frame">
<ul>
  <li><code>elecvery</code> Android 앱 개발 및 유지보수
    <ul>
      <li>전기차 충전소 지도 View 기반 마커 렌더링을 <code>Bitmap</code>/<code>Canvas</code> 방식으로 전환하여 Main Thread 부하 완화를 통한 성능 개선</li>
      <li>WearOS(워치)앱 개발 및 컴플리케이션 기능 구현</li>
      <li>POI 카테고리의 Android Auto 개발 (<code>MapWithContentTemplate</code> 활용)</li>
    </ul>
  </li>
</ul>

<details class="resume-collapsible">
  <summary class="resume-collapsible__summary">Elecvery Contributions</summary>
  <div class="resume-collapsible__content">
  <div class="resume-frame resume-frame--flat">

#### Jenkins 기반 PR 제목/본문 자동화 <span class="resume-chip">2025.05.12 ~ 2025.05.14</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- PR 생성 시 커밋/변경 파일 기반 AI 초안 자동 생성
- 반복 문서화 작업 감소 및 PR 포맷 일관성 향상
- 실패 시 빌드 성공 여부에 영향 없도록 안전 구성
- 관련 글: [Jenkins 기반 PR 제목/본문 자동화](/posts/work/jenkins-pr-automation/)

#### XML -> Compose 마이그레이션 <span class="resume-chip">2023.10.27 ~ 진행중</span> <span class="resume-chip resume-chip--impact">기여도 50%</span>

- XML 기반 UI를 Jetpack Compose로 점진적 전환
- 반복 UI 코드 및 디버깅 비용 감소
- 컴포저블 단위 재사용성, 유지보수성 향상
- 관련 글: [XML -> Compose 마이그레이션](/posts/work/xml-to-compose/)

#### 채팅 기능 개발 <span class="resume-chip">2023.09.05 ~ 2023.09.19</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- WebSocket/API/로컬 DB 동기화 구조 설계
- `ChatRepository` 중심 데이터 일관성 관리
- 네트워크 불안정 상황 재연결 전략 적용
- 관련 글: [채팅 기능 개발](/posts/work/chat-feature/)

#### 글로벌 앱 대응 <span class="resume-chip">2023.08.24 ~ 2023.11.02</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- iOS/Android 문자열 리소스 key/value 통일
- 하드코딩 문자열 정리 및 다국어 대응 체계 정비
- `traduora` + Custom Gradle Task로 문자열 동기화 자동화
- 관련 글: [글로벌 앱 대응](/posts/work/global-app-localization/)

#### 멀티모듈 작업 <span class="resume-chip">2023.06.12 ~ 2023.09.11</span> <span class="resume-chip resume-chip--impact">기여도 70%</span>

- 클린 아키텍처 기준 멀티 모듈 리팩터링
- 빌드 시간 약 3분 -> 1분 40초(약 44%) 개선
- Phone/Watch 코드 재활용 기반 확보
- 관련 글: [멀티모듈 작업](/posts/work/multi-module-refactoring/)

#### Apple 로그인 연동 <span class="resume-chip">2023.04.05 ~ 2023.04.06</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- Firebase Authentication 기반 Android Apple 로그인 지원
- Android <-> iOS 계정 연속성 개선
- 계정 이관 관련 CS 부담 감소
- 관련 글: [Apple 로그인 연동](/posts/work/apple-login/)

#### 디자인 토큰 도입 <span class="resume-chip">2023.03.08 ~ 2023.03.14</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- 디자인 토큰 변경 시 Custom Gradle Task로 자동 반영
- Android/iOS 간 UI 일관성 강화
- 유지보수 비용 절감
- 관련 글: [디자인 토큰 도입](/posts/work/design-token/)

#### 다크모드 적용 <span class="resume-chip">2023.02.28 ~ 2023.03.27</span> <span class="resume-chip resume-chip--impact">기여도 75%</span>

- 시맨틱 컬러 네이밍 체계 도입
- 하드코딩 컬러 정리 및 다크모드 전반 적용
- 야간 사용성 개선 및 CS 인입 감소
- 관련 글: [다크모드 적용](/posts/work/dark-mode/)

#### Amplitude 적용 <span class="resume-chip">2023.02.25 ~ 2023.03.15</span> <span class="resume-chip resume-chip--impact">기여도 45%</span>

- 사용자 행동 이벤트 로깅 체계 구축
- 운영/마케팅 분석 및 버그 재현 경로 추적 기반 마련
- 관련 글: [Amplitude 적용](/posts/work/amplitude/)

#### 워치앱 개발 <span class="resume-chip">2022.11.25 ~ 2022.12.24</span> <span class="resume-chip resume-chip--impact">기여도 100%</span>

- WearOS 기반 워치앱 연동 구현
- MessageClient/DataClient 구조 검증 및 적용
- 모바일-워치 간 토큰/데이터 교환 안정화
- 관련 글: [워치앱 개발](/posts/work/watch-app/)
</div>
</div>
</details>
</div>

### BOXNET <span class="resume-chip">2020.05.06 ~ 2021.12.31</span>

<div class="resume-company-frame">
<ul>
  <li>B2B AndroidTV 앱 <code>PlayInTV</code> 개발</li>
  <li>QR 코드 스캐너 앱 <code>씨네호텔</code> 개발</li>
  <li>웹툰 플랫폼 <code>애니툰</code> 개발 및 유지보수</li>
  <li>건설현장 출퇴근 관리 앱 <code>근태도우미</code> 프로토타입 개발
    <ul>
      <li>Beacon(BLE) 기반 출퇴근 기능 개발 경험</li>
    </ul>
  </li>
  <li>LeanBack API/UI, ZXing, 커스텀 캘린더 뷰 구현 경험</li>
</ul>
</div>

## 🚴‍♂️ Side Projects

### 모두의 보관함 <span class="resume-chip">2025.04 ~ 진행중</span>

<div class="resume-company-frame">
<ul>
  <li>전국 무인 보관함 정보 제공 앱 개발 중</li>
  <li>Supabase Auth/Storage 기반 사용자 인증 및 데이터 관리</li>
</ul>
</div>

### 플리 <span class="resume-chip">2020.09 ~ 2024.06</span>

<div class="resume-company-frame">
<ul>
  <li>프로젝트 팀 매칭 서비스 개발/운영</li>
  <li>Android 개발자 4인 + 디자이너 1인 협업</li>
  <li>Firebase Firestore 기반 구현</li>
  <li>Google Play: <a href="https://play.google.com/store/apps/details?id=org.fakedev.plie.release&hl=ko">플리</a></li>
  <li>시연 영상: <a href="https://home-plie.tistory.com/5">바로가기</a></li>
  <li>프로젝트 기록: <a href="https://docs.google.com/spreadsheets/d/1A2bThC7TDQmkODyIA4X_U1GSpmNJq2O2QY-GcZkRUC8/edit?usp=sharing">Google Sheets</a></li>
</ul>
</div>

## 📚 Library

### ClickableText <span class="resume-chip">2024.10 ~ 진행중</span>

<div class="resume-company-frame">
<ul>
  <li>연속 텍스트 내 특정 구간에 클릭 액션을 지정할 수 있는 라이브러리</li>
</ul>
</div>

## 🔨 Skills

| Category | Stack |
| --- | --- |
| Language | `Kotlin`, `Java` |
| Architecture / Pattern | `Clean Architecture`, `MVVM` |
| Build Configuration | `Build-Logic` |
| DI | `Hilt` |
| Asynchronous / Stream | `Coroutine`, `Flow`, `RxJava3` |
| Background | `WorkManager` |
| Android UI / Jetpack | `Compose`, `Navigation`, `ViewModel`, `LiveData`, `DataBinding`, `ViewBinding` |
| Data / Storage | `Room`, `DataStore`, `SharedPreferences` |
| Networking | `OkHttp3`, `Ktor Client` |
| Collaboration / Tools | `Slack`, `Jira`, `Figma`, `Notion` |
| Library | `Coil`, `Glide`, `Lottie` |
