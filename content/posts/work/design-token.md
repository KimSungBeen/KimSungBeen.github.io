---
title: "디자인 토큰 도입"
description: "디자인 시스템 자동 동기화"
summary: "Custom Gradle Task로 디자인 변경 반영 자동화"
date: 2023-03-08
startDate: 2023-03-08
endDate: 2023-03-14
contribution: 1.0
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/64a9478dbb02479daabd63b596d4d3db"
categories: ["work"]
tags: ["android", "design-token", "design-system", "gradle", "automation"]
series: ["Elecvery Contributions"]
---

## 문제

- 디자인 변경 시 Android/iOS 각각 수동 반영이 필요
- 플랫폼 간 UI 일관성 보장이 어렵고 유지보수 비용이 높음

## 해결

디자인 토큰 저장소에서 변경이 발생하면 **Custom Gradle Task**를 통해 앱 리소스가 자동으로 반영되도록 구성했습니다.

## 효과

- 플랫폼 공통 토큰 기반으로 스타일 변경 작업량 감소
- 색상/타이포/간격의 일관성 확보
- 수작업 누락 리스크 감소, 릴리즈 품질 안정화
