---
title: "글로벌 앱 대응"
description: "문자열 리소스 통합 및 번역 운영 자동화"
summary: "iOS/Android 문자열 통일 + traduora + Gradle 자동화"
date: 2023-08-24
startDate: 2023-08-24
endDate: 2023-11-02
contribution: 1.0
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/ea3df8b2339c4f23a83802d7efc2573e"
---

## 문제

- iOS/Android 문자열 key/value가 서로 달라 번역 진행이 어려웠습니다.
- 코드 내 하드코딩 문자열이 존재해 다국어 전환 대응이 불완전했습니다.
- 문자열 관리가 중앙화되지 않아 추후 일관성 붕괴 위험이 있었습니다.

## 해결

- iOS 팀과 함께 문자열 key/value 통일 작업 수행
- 하드코딩 문자열 리소스화 및 예외 구간 TODO 표식 처리
- 문자열 관리 도구 `traduora` 도입
- REST API 기반 Custom Gradle Task로 `strings.xml` 동기화 자동화

## 효과

- 플랫폼 간 문자열 리소스 일관성 확보
- 비개발 직군 포함 협업 가능한 문자열 운영 체계 확보
- 수동 import 작업 제거로 반복 작업/실수 감소
