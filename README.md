# Urban Design Harness

**AI 주도 도시설계 시스템** — Claude Code 플러그인. 대상지 분석부터 마스터플랜·판넬 제작까지, AI 에이전트 팀이 "분석 → 문제 정의 → 근거 → 설계 → 검증" 프로세스로 수행합니다.

> AI-led urban design system for Claude Code: a 6-agent harness (architect / design / verify / research / modeling / critic) with a direction-document SSOT, panel-section pipeline, and integrity feedback loop. Fully local — no external service required.

## 설치
```
/plugin marketplace add <this-repo-or-path>
/plugin install urban-design-harness@urban-design-harness
```

## 핵심 개념
- **판넬 중심** — 모든 결과는 판넬로, 이면 논리는 전부 문서로 명세·버전 관리
- **단일 귀결** — 모든 논리는 `direction/DIRECTION.md` 하나로 수렴
- **무결성 루프** — verify 에이전트 통과 없이는 방향성에 귀결되지 않음. 비약(근거 없는 가정) 차단
- **완전 로컬** — 인스턴스 디렉터리가 SSOT. 외부 서비스 의존 없음

## 구성
| 경로 | 내용 |
|---|---|
| `docs/SPEC.md` | 정본 시스템 명세 |
| `agents/` | architect·design·verify·research·modeling·critic (6종) |
| `skills/urban-design-harness/` | 오케스트레이션 (원칙·프로세스·루프·게이트) |
| `skills/urban-design-agent/` | 도시설계 방법론 레퍼런스 9종 (참고자료) |
| `commands/` | `/ud-init` `/ud-section` `/ud-loop` `/ud-verify` |
| `templates/project-scaffold/` | 인스턴스 스켈레톤 |

## 사용 흐름
1. `/ud-init <프로젝트명>` — 인스턴스 생성 + 결정 항목(대상지·판넬 규격·색상 정책 등) 인터뷰
2. 해당 디렉터리에서 작업 — 대상지 브리프 → DIRECTION v0.1
3. `/ud-section <id>` — 섹션 파이프라인 (논리→텍스트→디자인→판넬)
4. `/ud-loop` — 피드백 루프 (방향성 갱신→무결성 게이트→귀결/재구성→크리틱)
5. `/ud-verify` — 무결성 검사 단독 실행

## 라이선스
MIT
