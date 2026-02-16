---
title: "멀티모듈 작업"
description: "클린 아키텍처 기반 모듈 리팩터링"
summary: "빌드 시간 개선 및 워치앱 코드 재활용 기반 확보"
date: 2023-06-12
startDate: 2023-06-12
endDate: 2023-09-11
contribution: 0.7
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/0b728ede2a254e5d9e228effd15286ba"
---

## 문제

- 레이어 중심 모듈 분리가 빌드 부하를 특정 모듈에 집중시켰습니다.
- 워치앱 개발 시 비즈니스 로직 재활용이 어려웠습니다.

## 해결

- 클린 아키텍처 기준으로 멀티 모듈화 리팩터링
- 공통 비즈니스 로직을 재사용 가능한 구조로 정리

## 효과

- 1파일 수정 기준 빌드 시간 약 3분 -> 1분 40초로 개선(약 44%)
- Phone/Watch 앱 간 코드 재활용 가능
- 유지보수성 향상
