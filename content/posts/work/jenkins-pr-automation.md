---
title: "Jenkins 기반 PR 제목/본문 자동화"
description: "CI 단계에서 PR 문서화 자동 생성"
summary: "커밋/변경파일 기반 AI PR 초안 생성"
date: 2025-05-12
startDate: 2025-05-12
endDate: 2025-05-14
contribution: 1.0
showDate: true
showAuthor: false
notionURL: "https://www.notion.so/1fa96b6aa1c280fb802dd97c1ce7a4c8"
featureimage: "/images/posts/work/jenkins-pr-automation/automation-overview.png"
categories: ["work"]
tags: ["jenkins", "CI/CD", "pull-request", "automation", "AI"]
series: ["Elecvery Contributions"]
---

## 문제

커밋 메시지에 이미 작업 내역을 상세히 남겼음에도, PR 제목/본문을 다시 요약 작성하는 이중 작업이 반복되었습니다.

- 중복 문서화
- 작성 시간 낭비
- 누락/불일치 위험

## 해결

PR 생성 시 Jenkins 단계에서 제목/본문 초안을 자동 생성하도록 구성했습니다.

1. PR 생성 이벤트 감지
2. 관련 커밋 메시지 + 변경 파일 목록 수집
3. 프롬프트 생성 후 AI에 제목/본문 생성 요청
4. 생성 결과를 PR에 자동 반영
5. 해당 Step 실패가 전체 Jenkins 성공/실패에 영향 없도록 분리
6. 생성된 PR은 작성자가 반드시 검토하며 `WIP` 라벨로 관리

### 자동화 흐름

![Jenkins 기반 PR 자동화 개요](/images/posts/work/jenkins-pr-automation/automation-overview.png)

## 효과

- 반복 PR 문서화 시간 절감
- PR 문서 포맷 일관성 향상
- 자동화(초안) + 수동 검토(품질)의 균형 확보
- CI 파이프라인 안정성 유지
