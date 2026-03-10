---
title: "사진을 정리하여 앨범을 생성해주는 앱 Chac"
description: "사이드 프로젝트"
summary: "시간과 위치 기반으로 사진을 분류해 앨범을 자동 생성해주는 앱"
date: 2026-01-01
showDate: true
showAuthor: false
featureimage: "/images/projects/chac/chac-cover.png"
aliases: ["/experience/projects/chac/"]
---

{{< carousel
  images="{/images/projects/chac/1.png,/images/projects/chac/2.png,/images/projects/chac/3.png,/images/projects/chac/4.png}"
  aspectRatio="4-5"
  interval="2800"
  transition="450"
  fit="contain"
  maxWidth="75%"
>}}

## 기간

`2026.01 ~ 2026.02`

## 개요

Chac(착)은 쌓여가는 사진을 시간과 위치 기반으로 정리해
의미 있는 순간의 앨범을 자동 생성해주는 서비스입니다.

사진은 계속 쌓이지만 정리하는 일은 늘 뒤로 밀립니다.
이 프로젝트는 그런 불편을 줄이기 위해,
촬영한 사진의 메타데이터를 활용해 "구경할 수 있는 앨범"으로 다시 묶는 경험을 만드는 데 집중했습니다.

## 역할 및 기여

- Android 2인 팀 중 1명으로 참여
- 클러스터링 로직 및 Android 아키텍처 설계 담당
- 사진 메타데이터를 기반으로 한 앨범 생성 흐름 구현
- 백그라운드 작업과 UI 상태 연결 구조 설계

팀 구성:
- Android 2
- iOS 2
- Design 2

기여 비중: `70%`

## 핵심 구현

### 1. 시간 기반 1차 클러스터링 후 위치 기반 2차 분리

사진을 먼저 촬영 시간 기준으로 묶고,
같은 시간대에 찍힌 사진 안에서 다시 위치 기반으로 분리해
하나의 이동/장소 경험이 자연스럽게 앨범으로 만들어지도록 구성했습니다.

### 2. WorkManager 기반 백그라운드 처리

사진 수가 많아질수록 메타데이터 수집과 클러스터링이 무거워질 수 있어
앨범 생성 작업은 WorkManager 기반 백그라운드 플로우로 분리했습니다.
이를 통해 앱 진입 직후 UI를 막지 않으면서도 점진적으로 결과를 반영할 수 있게 했습니다.

### 3. EXIF와 Reverse Geocoding을 활용한 앨범 정보 생성

이미지의 EXIF 정보에서 위치를 읽고,
필요 시 Reverse Geocoding으로 사람이 이해하기 쉬운 장소명으로 변환해
자동 생성 앨범의 제목과 맥락을 더 자연스럽게 만들었습니다.

### 4. 멀티모듈 구조 기반 설계

프로젝트는 Clean Architecture와 MVVM을 기반으로,
기능 모듈과 공통 모듈을 나누는 멀티모듈 구조로 설계했습니다.
클러스터링 로직, 데이터 접근, UI 계층의 책임을 분리해
기능 확장과 유지보수성을 높이는 방향으로 가져갔습니다.

## 구조와 흐름

### 모듈 의존성 다이어그램

Android 앱은 `feature`, `data`, `domain`, `core` 성격의 모듈을 분리해
UI와 비즈니스 로직, 공통 자원을 분리했습니다.
이 구조를 기반으로 클러스터링 기능도 화면 계층과 독립적으로 확장할 수 있게 설계했습니다.

[![Chac 모듈 의존성 다이어그램](/images/projects/chac/module-dependency-diagram.svg)](/images/projects/chac/module-dependency-diagram.svg)

### 클러스터링 시퀀스 다이어그램

클러스터링은 화면 진입 후 바로 메인 스레드에서 처리하지 않고,
WorkManager를 통해 백그라운드 작업으로 실행한 뒤 점진적으로 UI 상태에 반영합니다.
시간 기반 1차 분류, 위치 기반 2차 분리, EXIF 추출, Reverse Geocoding, 앨범명 생성 흐름을 아래 시퀀스로 정리했습니다.

[![Chac 클러스터링 시퀀스 다이어그램](/images/projects/chac/clustering-sequence-diagram.svg)](/images/projects/chac/clustering-sequence-diagram.svg)

## 기술

- Architecture: Clean Architecture, MVVM
- Build: build-logic, Multi-module
- Async/Data: Coroutine, Flow
- Background: WorkManager
- DI: Hilt
- Database: Room
- UI: Compose, Navigation3
- Image Loading: Coil
- Clustering: Apache Commons Math3, DBSCAN

## 성과

- Google Play 출시
- 실사용 피드백 수집
- 사진 정리 경험을 자동화하는 서비스 컨셉 검증

## 링크

- Google Play: [Chac 다운로드](https://play.google.com/store/apps/details?id=com.chac.app)
- GitHub: [Nexters/Chac-Android](https://github.com/Nexters/Chac-Android)
- Instagram 소개 피드: [바로가기](https://www.instagram.com/p/DVndR-dCfOr/?utm_source=ig_web_copy_link&igsh=MzRlODBiNWFlZA==)
