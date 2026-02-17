---
title: "워치앱 개발 정리"
description: "WearOS 개발 시행착오 기록"
summary: "데이터 전송, 알림, 아키텍처 선택 과정"
date: 2022-12-24
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/4fa473ed7ced4f5d8749cf11498abdf9"
featureimage: "/images/posts/work/watch-app-notes/message-data-client-strategy.png"
categories: ["work"]
tags: ["android", "wear-os", "messageclient", "dataclient", "fcm"]
series: ["Elecvery Contributions"]
---

## 1) WearOS 개발 가능 범위

갤럭시 워치 앱은 WearOS 탑재 모델(워치4 이상)에서 안드로이드 기반 개발이 가능합니다. 
이전 모델은 타이젠 OS 기반이라 개발 체계가 완전히 달라, 동시 지원 시 별도 개발이 필요합니다.

## 2) 모바일 ↔ 워치 데이터 전송 시행착오

초기에는 레퍼런스가 매우 부족해 구현 난도가 높았습니다. 
`play-services-wearable` 기반으로 송수신을 구성했지만, 실제 동기화 과정에서 중요한 조건을 뒤늦게 확인했습니다.

- 휴대폰/워치 앱의 패키지명과 서명키 일치 필요
- 특히 휴대폰 앱은 Release 서명 설치가 중요

## 3) FCM 수신 조건

푸시가 휴대폰에는 오고 워치에는 오지 않는 문제가 있었고, 실제 확인 결과 워치 착용/설정 상태에 따라 동작이 달랐습니다.

- Galaxy Wearable 앱에서 알림 전달 허용
- 대상 앱 토글 ON 확인

## 4) DataClient 동작 오해와 구조 재설계

초기에는 요청/응답 모두 DataClient로 해결하려 했으나, `onDataChanged` 동작 특성 때문에 구조가 꼬였습니다.
결론적으로 다음 패턴으로 정리했습니다.

- 워치 → 모바일 요청: `MessageClient`
- 모바일 → 워치 동기화 데이터 전달: `DataClient`

### 구조 다이어그램

![DataClient 동작 구조](/images/posts/work/watch-app-notes/data-client-structure.png)
![MessageClient + DataClient 분리 전략](/images/posts/work/watch-app-notes/message-data-client-strategy.png)

## 5) 구현 특이사항

컴플리케이션 동작 시 토큰 재조회가 어려워, 워치에서는 전달받은 `accessToken`을 `SharedPreferences`에 저장해 사용했습니다.
