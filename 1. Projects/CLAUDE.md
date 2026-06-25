# 1. Projects — 운영 가이드

## 폴더 목적

**명확한 목표와 마감일이 있는 프로젝트**를 관리합니다.  
프로젝트란 "완료 가능한 결과물"이 있는 작업 묶음입니다. 끝이 없으면 프로젝트가 아닌 Area입니다.

## 어떤 노트가 들어오는가

- 프로젝트 허브 노트 (`type: project`)
- 프로젝트에 종속된 실행 노트 (회의록, 결정 사항, 작업 로그 등)
- 프로젝트 산출물 초안

**들어오지 않는 것**
- 영구적인 지식 → `5. Zettelkasten/20. Permanent/`
- 완료/중단된 프로젝트 → `4. Archive/`
- 지속 관리 영역 → `2. Areas/`

## 파일 구조

```
1. Projects/
├── CLAUDE.md
├── 00_Projects_Hub.md          # 전체 프로젝트 대시보드
├── [프로젝트명]/               # 프로젝트별 하위 폴더
│   ├── [프로젝트명]_Hub.md     # 프로젝트 허브 노트
│   ├── 회의록_YYYY-MM-DD.md
│   └── ...
└── ...
```

## 프로젝트 허브 노트 Frontmatter

```yaml
---
type: project
status: in-progress          # todo | in-progress | completed | archived
created: YYYY-MM-DD
updated: YYYY-MM-DD
due: YYYY-MM-DD              # 마감일 (필수)
tags: [project]
area: "[[연결된 Area]]"      # 이 프로젝트가 속한 영역 (선택)
---
```

## 작업 규칙

1. **프로젝트 시작 시**: 허브 노트를 먼저 생성하고 목표·마감·성공 기준을 정의
2. **완료 기준 명시**: "언제 이 프로젝트는 끝나는가"를 허브 노트 상단에 기재
3. **완료/중단 시**: `4. Archive/`로 폴더째 이동하고 status를 `completed` 또는 `archived`로 변경
4. **지식 생성 시**: 프로젝트 중 얻은 통찰은 `5. Zettelkasten/20. Permanent/`에 분리 저장하고 허브 노트에서 링크
5. **복사 금지**: 다른 노트의 내용은 복사하지 말고 `[[링크]]`로 참조

## Dataview 대시보드

```dataview
TABLE due, status, area
FROM "1. Projects"
WHERE type = "project" AND status != "completed" AND status != "archived"
SORT due ASC
```
