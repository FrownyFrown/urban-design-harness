---
description: 피드백 루프 1회전 — 방향성 업데이트 → verify 무결성 게이트 → 귀결/재구성 → critic 비평
---
urban-design-harness 스킬의 「피드백 루프」를 1회전 실행하라.

1. 현재 작업 내용 기준으로 direction/DIRECTION.md 갱신안 작성 ("지금 방향성 / 이전 방향성" 구분 명시).
2. verify 에이전트에 위임: 당위성·무결성·완결성·방향성 검증. 결과를 `_state/integrity-report.json`에 기록.
3. 통과 시: DIRECTION.md 귀결 + `direction/versions/`에 버전 스냅샷 + `_state/direction-pointer.json` 갱신 (직접 +0.1 / 간접 +0.01, 타임스탬프).
4. 불일치 시: 위반 항목을 사용자에게 보고하고 논리 구조 재구성안을 제시. 임의 통과 금지.
5. 통과 후 critic 에이전트에 위임: 제3자 비평 → 개선점을 `_state/loop-state.json`의 다음 루프 입력으로 기록.
6. `_state/loop-state.json` loop_count 증가·상태 갱신.
