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
---

## 문제

- Android/iOS 각각 수작업으로 디자인 변경을 반영해야 했습니다.
- 플랫폼 간 UI 일관성 유지 비용이 높았습니다.

## 해결

- 디자인 토큰 저장소 변경 시 Custom Gradle Task로 자동 반영

## 효과

- 플랫폼 공통 토큰 사용으로 작업량 감소
- 색상/타이포/간격의 일관성 확보
- 유지보수성 향상
