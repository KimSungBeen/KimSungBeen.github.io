---
title: "다크모드 적용"
description: "야간 사용성 개선"
summary: "시맨틱 컬러 체계 도입과 하드코딩 컬러 정비"
date: 2023-02-28
startDate: 2023-02-28
endDate: 2023-03-27
contribution: 0.75
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/ab25eceb85fe4c69b853bb617470b1f4"
featureimage: "/images/posts/work/dark-mode/dark-mode.png"
categories: ["work"]
tags: ["android", "dark-mode", "design-system", "semantic-color", "UI/UX"]
series: ["Elecvery Contributions"]
---

## 문제

야간 주행 중 경로 추천/충전소 검색 화면이 과도하게 밝아 사용성이 떨어졌습니다.

- 제약 1: 당시 디자인 시스템이 정교하지 않아 시맨틱 컬러와 다크 대응 컬러가 미정
- 제약 2: 코드 내 하드코딩 색상 사용 구간이 존재

## 해결

- 디자이너와 협업하여 컬러 네이밍을 `gray_100` 형태에서 `neutrals_text_default` 같은 **시맨틱 체계**로 재정의
- 정규식 검색으로 하드코딩 컬러를 빠르게 탐지/정비
  - 예: `textColor\\s*=\\s*\"(#(?:[0-9a-fA-F]{3}){1,2}|[a-zA-Z]+)`

## 효과

1. 다크모드 적용으로 야간 가독성 향상
2. 사용자 만족도 개선 및 CS 인입 감소
3. 체계적인 컬러 시스템 도입으로 유지보수성/확장성 향상

### 적용 화면

![Light 모드 화면](/images/posts/work/dark-mode/light-mode.png)
![Dark 모드 화면](/images/posts/work/dark-mode/dark-mode.png)
