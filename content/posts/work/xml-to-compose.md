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
categories: ["work"]
tags: ["android", "jetpack-compose", "xml-migration", "refactoring"]
series: ["Elecvery Contributions"]
---

## 문제

대중적인 XML 방식의 한계인 복잡한 상태 관리/가독성 저하를 체감하고 있었습니다.
특히 동적인 UI 변경과 다양한 배경 Shape를 많이 다루는 화면에서 수작업 UI 제어 비용이 크게 발생했습니다.

## 해결

Jetpack Compose를 도입해 기존 XML 기반 UI를 선언형 UI로 전환했습니다.

- 상태와 UI를 직접적으로 연결
- View 제어를 위한 보일러플레이트 코드 축소

## 효과

- **생산성 향상**: 반복 UI 코드 단순화, 디버깅 소요 시간 단축
- **유지보수성 증가**: 컴포저블 단위 모듈화로 재사용/확장 용이
- **애니메이션 활용 확대**: 복잡한 애니메이션 구현 난이도 완화
- **구조 단순화**: XML/Kotlin 간 의존성 감소로 프로젝트 이해도 향상
