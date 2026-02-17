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
featureimage: "/images/posts/work/chat-feature/chat-sequence.png"
categories: ["work"]
tags: ["android", "chat", "websocket", "data-sync", "repository-pattern"]
series: ["Elecvery Contributions"]
---

## 목표

실시간 메시지 송수신, 네트워크 불안정 상황 복원, 로컬 기록 유지까지 포함한 채팅 기능을 구현했습니다.

## 아키텍처 구성

- `ChatApi`: 채팅 API wrapper
- `ChatWebSocket`: 웹소켓 open/송수신/재연결 보장
- `ElecveryLoungeMessageDao`: 로컬 DB CRUD
- `ChatRepository`: 웹소켓 + sync API + 로컬 DB 동기화 오케스트레이션

뷰모델은 `ChatRepository` 중심으로만 의존하도록 구성해, 데이터 일관성과 책임 경계를 명확히 했습니다.

## 핵심 포인트

- 네트워크 단절 시 재연결 전략 내장
- 서버/로컬 데이터의 동기화 시점 제어
- 실시간성과 안정성을 동시에 확보하도록 레이어 역할 분리

### 시퀀스 다이어그램

![채팅 기능 시퀀스 다이어그램](/images/posts/work/chat-feature/chat-sequence.png)
