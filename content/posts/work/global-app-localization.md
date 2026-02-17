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
categories: ["work"]
tags: ["android", "localization", "i18n", "traduora", "gradle-automation"]
series: ["Elecvery Contributions"]
---

## 문제

영문 지원 요구사항이 생겼지만, 실제 프로젝트 상태는 다음과 같았습니다.

1. iOS/Android 문자열 key, value가 서로 다름
2. 코드 내 하드코딩 문자열 존재
3. 문자열 리소스 관리가 중앙화되지 않아 재발 위험 존재

## 해결

- iOS 팀과 협업해 문자열 key/value 통일 작업 수행
- 리소스 추출이 어려운 하드코딩 구간은 커스텀 TODO로 관리 포인트 명시
- 문자열 관리 솔루션으로 `traduora` 도입
- `traduora` REST API를 활용한 Custom Gradle Task로 `strings.xml` 자동 생성

## 효과

- 플랫폼 간 문자열 리소스 일관성 확보
- 개발자 외 구성원도 문자열 관리에 참여 가능한 운영 체계 구축
- 수동 export/import 제거로 반복 작업 및 실수 리스크 감소
