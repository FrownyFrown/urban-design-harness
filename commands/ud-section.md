---
description: 판넬 섹션 1개를 섹션 파이프라인으로 작업한다. 인자: 섹션 ID (예/ud-section s01)
---
urban-design-harness 스킬의 「섹션 파이프라인」 절차를 따르라.

1. `panel/PANEL_SPEC.md`에서 인자 섹션 ID의 좌표·크기·핵심 1문장을 확인 (없으면 사용자에게 섹션 정의를 먼저 요청).
2. architect 에이전트에 위임: 논리 구성 → 텍스트 구성 ("기존 문제→변경→영향" 서술 필수).
3. design 에이전트에 위임: 영역 크기 맞는 시각화 형태·템플릿 결정 → SVG/이미지 생성 → assets/ 저장.
4. `panel/sections/<id>/SPEC.md` 갱신 (버전·타임스탬프).
5. /ud-loop 1회 실행 (verify 게이트 통과까지).
