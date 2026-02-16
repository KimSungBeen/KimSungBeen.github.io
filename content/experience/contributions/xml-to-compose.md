---
title: "XML -> Compose 마이그레이션"
description: "선언형 UI 전환"
summary: "UI 생산성/유지보수성 향상"
date: 2023-10-27
startDate: 2023-10-27
contribution: 0.5
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/ffb032cab870498ba3f2759e4cfa2f6d"
---

## 문제

- XML 기반 UI에서 상태 관리 복잡도와 가독성 저하가 있었습니다.
- 동적 UI/Background 처리 비용이 컸습니다.

## 해결

- Jetpack Compose 도입으로 선언형 UI로 전환
- 상태와 UI를 직접 연결해 수작업 View 제어 코드 감소

## 효과

- 반복 UI 코드 단순화 및 디버깅 시간 절감
- 컴포저블 단위 재사용/유지보수성 향상
- 애니메이션 적용 용이성 증가
- XML/Kotlin 의존성 축소로 프로젝트 구조 단순화
