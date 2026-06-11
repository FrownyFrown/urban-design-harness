---
description: 무결성 게이트만 단독 실행 — 문서 간 모순·비약·서술 누락 검사 리포트
---
verify 에이전트에 위임해 무결성 검증만 실행하라.

대상: direction/DIRECTION.md ↔ panel/sections/*/SPEC.md ↔ process/ 문서 전체.
검사: ① 근거 없는 주장(비약) ② 문서 간 모순 ③ "기존 문제→변경→영향" 서술 누락 ④ 방향성 이탈.
출력: `_state/integrity-report.json` 갱신 + 사용자에게 위반 목록·심각도·수정 제안 보고. 통과/불통과 명시.
