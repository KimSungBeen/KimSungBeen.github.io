---
title: "Apple 로그인 연동"
description: "Android-iOS 계정 연속성 개선"
summary: "Firebase Authentication 기반 Apple 로그인 지원"
date: 2023-04-05
startDate: 2023-04-05
endDate: 2023-04-06
contribution: 1.0
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/a6dd9b27bf8342e9bfc6c1caf7ee5252"
featureimage: "/images/posts/work/apple-login/firebase-apple-users.png"
categories: ["work"]
tags: ["android", "authentication", "firebase-auth", "apple-sign-in"]
series: ["Elecvery Contributions"]
---

## 문제

소셜 로그인 중심으로 운영되던 서비스에서, **Apple 로그인으로 가입한 사용자가 Android 기기로 전환할 때 계정 연속성이 끊기는 문제**가 있었습니다. 
기존에는 고객센터를 통한 계정 이관 요청이 필요했고, 사용자/CS 모두에게 반복적인 부담이 발생했습니다.

## 해결

- Firebase Authentication 기반으로 Android에서도 Apple 로그인을 처리하도록 연동
- iOS에서 생성된 계정과 Android 로그인 흐름이 동일 사용자로 연결되도록 인증 체계 정리

## 효과

- Android ↔ iOS 간 계정 전환 가능
- 계정 이관 관련 CS 인입 감소
- 고객센터의 반복 업무를 줄여 다른 고부가 업무에 리소스 집중 가능

### 참고 이미지

![Firebase Authentication에서 Android 기기 Apple 로그인 사용자 집계](/images/posts/work/apple-login/firebase-apple-users.png)
