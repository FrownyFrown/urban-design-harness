# SESSION_BOOTSTRAP — 진입 로드 순서

1. CLAUDE.md (자동) — 원칙·구조 숙지
2. `_state/direction-pointer.json` → 현재 방향성 버전 확인 → `direction/DIRECTION.md` 로드
3. `_state/loop-state.json` — 진행 중 루프·재구성 대기 여부 확인
4. 작업 섹션이 있으면 `panel/PANEL_SPEC.md` + 해당 `panel/sections/<id>/SPEC.md`
5. 정본 필요 시: urban-design-harness 플러그인 docs/SPEC.md

우선 참조: 인스턴스 결정 항목(CLAUDE.md 하단)은 임의 결정 금지 — 사용자 질의.
