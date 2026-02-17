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
featureimage: "/images/posts/work/multi-module-refactoring/module-after.png"
categories: ["work"]
tags: ["android", "multi-module", "clean-architecture", "build-optimization", "modularization"]
series: ["Elecvery Contributions"]
---

## 문제

기존 구조는 `domain`, `data-remote`, `data-local`, `model`처럼 레이어 중심 분리였고,
모듈 크기 불균형으로 인해 빌드 부하가 특정 모듈에 집중되었습니다.

또한 Watch 앱 개발 시 Phone 앱의 비즈니스 로직을 재사용하기 어려운 구조였습니다.

### 기존 모듈 구조

![멀티모듈 작업 이전 모듈 모식도](/images/posts/work/multi-module-refactoring/module-before.png)

## 해결

클린 아키텍처 기준으로 모듈 경계를 재설계하고, 공통 비즈니스 로직을 재사용 가능한 형태로 분리했습니다.

### 개선 후 모듈 구조

![멀티모듈 작업 이후 모듈 모식도](/images/posts/work/multi-module-refactoring/module-after.png)

참고:
- [모놀리틱에서 멀티 모듈로 탈출하기 — Android](https://medium.com/@kimdohun0104/%EB%AA%A8%EB%86%80%EB%A6%AC%ED%8B%B1%EC%97%90%EC%84%9C-%EB%A9%80%ED%8B%B0-%EB%AA%A8%EB%93%88%EB%A1%9C-%ED%83%88%EC%B6%9C%ED%95%98%EA%B8%B0-android-7d92db03a96)
- [Common modularization patterns | Android Developers](https://developer.android.com/topic/modularization/patterns)

## 효과

- 단일 파일 수정 기준 빌드 시간: 약 3분 → 1분 40초 (약 44% 개선)
- Phone/Watch 간 코드 재사용 기반 확보
- 구조적 유지보수성 향상
