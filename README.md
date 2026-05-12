# Antigravity Workspace

AI 코딩 에이전트(Kilocode 등)의 행동 규칙(Harness)과 스킬(Skill)을 정의하는 템플릿 프로젝트입니다.

---

## 프로젝트 구조

```
.
├── .agents/
│   ├── rules/                          # 에이전트 행동 규칙
│   │   ├── harness.md                  # 공통 작업 절차 규칙
│   │   ├── safety.md                   # 안전 규칙 (금지 행동, 승인 필요 작업)
│   │   ├── Antigravity harness Protocol.clinerules  # 자율 실행 및 메모리 관리 규칙
│   │   └── Python Antigravity Harness Rules.clinerules  # Python 코드 작성 기준
│   └── skills/                         # 재사용 가능한 스킬 정의
│       ├── api-review/SKILL.md         # API 보안·검증·테스트 점검
│       ├── frontend-polish/SKILL.md    # 프론트엔드 UI 완성도 개선
│       └── python-refactor/SKILL.md   # Python 코드 품질 개선
├── .antigravity/
│   └── MEMORY.md                       # 세션 간 프로젝트 메모리
├── .kilocode/
│   ├── package.json                    # Kilocode 플러그인 의존성
│   └── .gitignore
├── .vscode/
│   └── settings.json
├── requirements-dev.txt                # 개발 의존성 (ruff, pytest)
└── README.md
```

---

## 규칙 (Rules)

| 파일 | 역할 |
|------|------|
| `harness.md` | 작업 시작·수정·터미널·검증·기록 절차 표준화 |
| `safety.md` | 절대 금지 행동, 사용자 승인 필요 작업, 실패 처리 기준 |
| `Antigravity harness Protocol.clinerules` | 자율 실행 범위, 메모리 파일 관리, 보안 가드레일 |
| `Python Antigravity Harness Rules.clinerules` | Type Hint, Docstring, TDD, 환경변수 접근 기준 |

---

## 스킬 (Skills)

| 스킬 | 주요 사용 시점 |
|------|--------------|
| `api-review` | 새 API 엔드포인트 설계·수정·보안 점검 시 |
| `frontend-polish` | UI 완성도, 반응형, 접근성, 빈 상태 처리 시 |
| `python-refactor` | Python 코드 리팩토링, 린트, 테스트 보강 시 |

---

## 개발 환경 설정

```bash
pip install -r requirements-dev.txt
```

| 패키지 | 용도 |
|--------|------|
| `ruff` | 정적 분석 및 린트 (`ruff check .`) |
| `pytest` | 테스트 실행 (`pytest`) |

---

## 세션 메모리

에이전트는 세션 시작 시 `.antigravity/MEMORY.md`를 가장 먼저 읽고,
작업 중 발견한 특이사항·결정·이슈를 해당 파일에 기록합니다.

---

## 의존성

- [@kilocode/plugin](https://www.npmjs.com/package/@kilocode/plugin) `7.2.52`
