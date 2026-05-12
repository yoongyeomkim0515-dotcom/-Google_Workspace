# Antigravity Memory

> 이 파일은 작업 중 발견한 특이사항, 결정, 제약, 실패 원인, 다음 작업을 기록하는 프로젝트 메모리 파일이다.
> 세션 시작마다 가장 먼저 읽는다.

---

## 프로젝트 개요

- 프로젝트명: 테스트2 (antigravity-workspace)
- 구성: AI 에이전트 규칙/스킬 템플릿 프로젝트
- 원격 저장소: https://github.com/yoongyeomkim0515-dotcom/-Antigravity_Workspace
- 주요 파일:
  - `.agents/rules/` — 에이전트 행동 규칙 (harness, safety, .clinerules)
  - `.agents/skills/` — 스킬 정의 (api-review, frontend-polish, python-refactor)
  - `.kilocode/` — Kilocode 플러그인 설정
  - `README.md` — 프로젝트 문서

---

## 결정 및 제약

| 날짜 | 내용 |
|------|------|
| 2026-05-13 | 프로젝트 초기 세팅. `.antigravity/MEMORY.md` 최초 생성 |
| 2026-05-13 | `git init` 후 GitHub 원격 저장소 연결 및 초기 push 완료 |
| 2026-05-13 | `README.md` 추가 및 push 완료 (rebase로 원격 충돌 해결) |

---

## 발견된 이슈

| 날짜 | 파일 | 내용 | 상태 |
|------|------|------|------|
| 2026-05-13 | `.antigravity/MEMORY.md` | 참조 파일이 존재하지 않음 | ✅ 해결 |
| 2026-05-13 | `.kilocode/.gitignore` | `.gitignore`가 자기 자신을 무시 목록에 포함 | ✅ 해결 |
| 2026-05-13 | `.kilocode/package.json` | `name`, `version` 필드 없음 | ✅ 해결 |
| 2026-05-13 | `Antigravity harness Protocol.clinerules` | 자율 실행 vs. 승인 필요 범위 모호 | ✅ 해결 |
| 2026-05-13 | `SKILL.md` 3개 | description 영어 / 내용 한국어 혼용 | ✅ 해결 |

---

## 수정 이력

| 날짜 | 커밋 | 파일 | 변경 내용 |
|------|------|------|-----------|
| 2026-05-13 | `db5d6ed` | `.antigravity/MEMORY.md` | 최초 생성 |
| 2026-05-13 | `db5d6ed` | `.kilocode/.gitignore` | `.gitignore` 자기 참조 항목 제거 |
| 2026-05-13 | `db5d6ed` | `.kilocode/package.json` | `name: "antigravity-workspace"`, `version: "1.0.0"` 추가 |
| 2026-05-13 | `db5d6ed` | `Antigravity harness Protocol.clinerules` | 자율 실행 범위를 테스트·린트로 한정, 위험 명령 승인 필요 규칙 명시 |
| 2026-05-13 | `db5d6ed` | `.agents/skills/*/SKILL.md` (3개) | `description` 필드를 한국어로 통일 |
| 2026-05-13 | `ed03b47` | `README.md` | 프로젝트 문서 최초 생성 |

---

## Git 이력

| 커밋 | 메시지 |
|------|--------|
| `db5d6ed` | init: 프로젝트 초기 설정 및 버그 수정 |
| `d0e8192` | Initialize project (GitHub 자동 생성) |
| `ed03b47` | docs: README.md 추가 |

---

## 다음 작업

- 없음 (발견된 이슈 전체 해결 완료)

---

## 메모

