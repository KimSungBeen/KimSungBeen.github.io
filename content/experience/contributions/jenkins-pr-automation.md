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
---

## 문제

- 커밋 메시지 작성 후에도 PR 제목/본문을 다시 수동 작성해야 하는 반복 작업이 있었습니다.

## 해결

- PR 생성 시 Jenkins 단계에서 커밋/변경 파일 수집
- 프롬프트 생성 후 AI로 제목/본문 초안 생성
- 생성된 내용을 PR에 자동 반영
- 실패 시 전체 빌드 성공 여부에는 영향 없도록 구성

## 효과

- 반복 문서화 작업 시간 절감
- PR 포맷 일관성 개선
- 자동화 + 수동 검토 균형 유지
