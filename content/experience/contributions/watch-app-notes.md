---
title: "워치앱 개발 정리"
description: "WearOS 개발 시행착오 기록"
summary: "데이터 전송, 알림, 아키텍처 선택 과정"
date: 2022-12-24
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/4fa473ed7ced4f5d8749cf11498abdf9"
---

## 핵심 정리

- WearOS 기반 갤럭시 워치 앱 개발 가능 범위 확인
- 모바일 앱과 워치앱 간 데이터 교환 방식 검증
- `DataClient`, `MessageClient`, `ChannelClient` 동작 방식 비교
- 실제 구현은 "요청은 MessageClient, 동기화는 DataClient" 전략으로 정리

## 주요 시행착오

- 디버그/릴리즈 서명키 조건 차이로 인한 동기화 이슈
- FCM 수신 조건 및 워치 설정 의존성
- `onDataChanged` 호출 조건 오해로 인한 아키텍처 재설계

## 비고

원본 기록에는 이미지/레퍼런스 링크/실험 로그가 포함되어 있으며, 필요 시 후속으로 전체 본문을 그대로 이식할 수 있습니다.
