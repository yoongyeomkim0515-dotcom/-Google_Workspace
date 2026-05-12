# Antigravity Workspace

AI 코딩 에이전트(Kilocode 등)의 행동 규칙과 스킬을 정의하는 템플릿 프로젝트입니다.

---

## 프로젝트 구조

```
.
├── .agents/
│   ├── rules/                          # 에이전트 행동 규칙
│   │   ├── harness.md                  # 공통 하네스 규칙 (작업 절차 표준)
│   │   ├── safety.md                   # 공통 안전 규칙
│   │   ├── Antigravity harness Protocol.clinerules
│   │   └── Python Antigravity Harness Rules.clinerules
│   └── skills/                         # 에이전트 스킬 정의
│       ├── api-review/SKILL.md         # API 설계·검토 스킬
│       ├── frontend-polish/SKILL.md    # 프론트엔드 UI 개선 스킬
│       └── python-refactor/SKILL.md    # Python 리팩토링 스킬
├── .antigravity/
│   └── MEMORY.md                       # 프로젝트 메모리 (세션 간 컨텍스트 유지)
├── .kilocode/
│   ├── package.json                    # Kilocode 플러그인 의존성
│   └── .gitignore
└── .vscode/
    └── settings.json
```

---

## 주요 규칙 파일

| 파일 | 설명 |
|------|------|
| `harness.md` | 작업 시작·수정·검증·기록 절차 표준 |
| `safety.md` | 절대 금지 항목, 승인 필요 작업, 실패 처리 기준 |
| `Antigravity harness Protocol.clinerules` | 자율 실행 범위 및 메모리 관리 규칙 |
| `Python Antigravity Harness Rules.clinerules` | Python 코드 작성·검증 기준 |

## 스킬 목록

| 스킬 | 설명 |
|------|------|
| `api-review` | API 엔드포인트 보안·검증·에러 처리 점검 |
| `frontend-polish` | UI 레이아웃·접근성·반응형 개선 |
| `python-refactor` | 타입 힌트·독스트링·린트·테스트 보강 |

---

## 메모리 시스템

`.antigravity/MEMORY.md` 파일에 작업 중 발견한 특이사항, 결정, 수정 이력을 기록합니다.
에이전트는 세션 시작 시 이 파일을 가장 먼저 읽습니다.

---

## 의존성

- [@kilocode/plugin](https://www.npmjs.com/package/@kilocode/plugin) `7.2.52`
