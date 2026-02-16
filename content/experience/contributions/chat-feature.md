---
title: "채팅 기능 개발"
description: "웹소켓/동기화/로컬저장소 설계"
summary: "실시간 채팅과 데이터 일관성 관리"
date: 2023-09-05
startDate: 2023-09-05
endDate: 2023-09-19
contribution: 1.0
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/24d96b6aa1c28008905ed7a11ced1a38"
---

## 구성

- `ChatApi`: 채팅 API 래퍼
- `ChatWebSocket`: 송수신/재연결 보장
- `ElecveryLoungeMessageDao`: 로컬 채팅 DB CRUD
- `ChatRepository`: 웹소켓, sync API, 로컬 DB 동기화 및 일관성 관리

## 핵심 포인트

- 뷰모델은 Repository 중심으로 의존하도록 구성
- 네트워크 불안정 상황에서 재연결 전략 적용
