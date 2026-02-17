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

## Work Experience

### 티비유 (2022.01.10 ~ 현재)

- `elecvery` Android 앱 개발 및 유지보수
  - 전기차 충전소 지도 View 기반 마커 렌더링을 `Bitmap`/`Canvas` 방식으로 전환하여 Main Thread 부하 완화를 통한 성능 개선
  - WearOS(워치)앱 개발 및 컴플리케이션 기능 구현
  - POI 카테고리의 Android Auto 개발 (`MapWithContentTemplate` 활용)

### (주)박스넷 개발팀 (2020.05.06 ~ 2021.12.31)

- B2B AndroidTV 앱 `PlayInTV` 개발
- QR 코드 스캐너 앱 `씨네호텔` 개발
- 웹툰 플랫폼 `애니툰` 개발 및 유지보수
- 건설현장 출퇴근 관리 앱 `근태도우미` 프로토타입 개발
- LeanBack API/UI, ZXing, 커스텀 캘린더 뷰 구현 경험

## Elecvery Contributions

### 글로벌 앱 대응 (2023.08.24 ~ 2023.11.02, 기여도 100%)

- iOS/Android 문자열 리소스 key/value 통일
- 하드코딩 문자열 정리 및 다국어 대응 체계 정비
- `traduora` + Custom Gradle Task로 문자열 동기화 자동화

### 멀티모듈 작업 (2023.06.12 ~ 2023.09.11, 기여도 70%)

- 클린 아키텍처 기준 멀티 모듈 리팩터링
- 빌드 시간 약 3분 -> 1분 40초(약 44%) 개선
- Phone/Watch 코드 재활용 기반 확보

### XML -> Compose 마이그레이션 (2023.10.27 ~, 기여도 50%)

- XML 기반 UI를 Jetpack Compose로 점진적 전환
- 반복 UI 코드 및 디버깅 비용 감소
- 컴포저블 단위 재사용성, 유지보수성 향상

### 다크모드 적용 (2023.02.28 ~ 2023.03.27, 기여도 75%)

- 시맨틱 컬러 네이밍 체계 도입
- 하드코딩 컬러 정리 및 다크모드 전반 적용
- 야간 사용성 개선 및 CS 인입 감소

### 디자인 토큰 도입 (2023.03.08 ~ 2023.03.14, 기여도 100%)

- 디자인 토큰 변경 시 Custom Gradle Task로 자동 반영
- Android/iOS 간 UI 일관성 강화
- 유지보수 비용 절감

### 채팅 기능 개발 (2023.09.05 ~ 2023.09.19, 기여도 100%)

- WebSocket/API/로컬 DB 동기화 구조 설계
- `ChatRepository` 중심 데이터 일관성 관리
- 네트워크 불안정 상황 재연결 전략 적용

### Amplitude 적용 (2023.02.25 ~ 2023.03.15, 기여도 45%)

- 사용자 행동 이벤트 로깅 체계 구축
- 운영/마케팅 분석 및 버그 재현 경로 추적 기반 마련

### Apple 로그인 연동 (2023.04.05 ~ 2023.04.06, 기여도 100%)

- Firebase Authentication 기반 Android Apple 로그인 지원
- Android <-> iOS 계정 연속성 개선
- 계정 이관 관련 CS 부담 감소

### 워치앱 개발 (2022.11.25 ~ 2022.12.24, 기여도 100%)

- WearOS 기반 워치앱 연동 구현
- MessageClient/DataClient 구조 검증 및 적용
- 모바일-워치 간 토큰/데이터 교환 안정화

### Jenkins 기반 PR 제목/본문 자동화 (2025.05.12 ~ 2025.05.14, 기여도 100%)

- PR 생성 시 커밋/변경 파일 기반 AI 초안 자동 생성
- 반복 문서화 작업 감소 및 PR 포맷 일관성 향상
- 실패 시 빌드 성공 여부에 영향 없도록 안전 구성

## Side Projects

### 플리 (2020.09 ~ 2024.06)

- 프로젝트 팀 매칭 서비스 개발/운영
- Android 개발자 4인 + 디자이너 1인 협업
- Firebase Firestore 기반 구현

링크:
- Google Play: [플리](https://play.google.com/store/apps/details?id=org.fakedev.plie.release&hl=ko)
- 시연 영상: [바로가기](https://home-plie.tistory.com/5)
- 프로젝트 기록: [Google Sheets](https://docs.google.com/spreadsheets/d/1A2bThC7TDQmkODyIA4X_U1GSpmNJq2O2QY-GcZkRUC8/edit?usp=sharing)

### 모두의 보관함 (2025.04 ~)

- 전국 무인 보관함 정보 제공 앱 개발 중
- Supabase Auth/Storage 기반 사용자 인증 및 데이터 관리

## Library

### ClickableText (2024.10 ~)

- 연속 텍스트 내 특정 구간에 클릭 액션을 지정할 수 있는 라이브러리

## Skills

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