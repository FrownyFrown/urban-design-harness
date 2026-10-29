---
description: 새 도시설계 프로젝트 인스턴스를 스캐폴드한다. 인자: 프로젝트 slug (예/ud-init wangsimni)
---
새 도시설계 모듈 인스턴스를 생성하라.

1. 대상 디렉터리 결정: 인자가 절대/상대 경로면 그 경로, 단순 slug면 현재 디렉터리 하위 `./ud-<slug>/`. 이미 존재하면 중단하고 사용자에게 알린다.
2. 스캐폴드 `${CLAUDE_PLUGIN_ROOT}/templates/project-scaffold/` 전체를 대상 디렉터리로 복사한다. 다른 경로에서 찾지 않는다(디스크를 검색하면 다른 버전 사본을 집을 수 있다). 이 경로가 없으면 중단하고 알린다 (CLAUDE.md, SESSION_BOOTSTRAP.md, direction/, panel/, process/01~04, design_system/, references/, _state/, _memory/, _sessions/, assets/).
3. 플레이스홀더 치환: CLAUDE.md `{{PROJECT_NAME}}`→slug, DIRECTION.md `{{DATE}}`→오늘 날짜. `_state/direction-pointer.json` timestamp 갱신.
4. 인스턴스 결정 항목(대상지·과업 성격·판넬 규격·색상·생성이미지 정책·크리틱 기준)을 사용자에게 묻고 CLAUDE.md 하단에 기록한다.
5. 사용자에게 보고: 생성 경로, 시작 방법(cd 후 claude), 다음 단계(대상지 브리프 → DIRECTION v0.1 수립).
