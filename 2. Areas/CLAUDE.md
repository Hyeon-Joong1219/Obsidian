# 2. Areas — 운영 가이드

## 폴더 목적

**마감일 없이 지속적으로 유지해야 하는 책임 영역**을 관리합니다.  
Area는 "기준 이하로 떨어지면 안 되는 상태"를 유지하는 공간입니다. 끝이 있으면 Area가 아닌 Project입니다.

## 어떤 노트가 들어오는가

- 영역 허브 노트 (`type: area`)
- 영역 내 정기 검토 노트 (주간/월간 리뷰)
- 영역 관련 기준·정책·루틴 기록

**들어오지 않는 것**
- 마감일이 있는 작업 → `1. Projects/`
- 참고 자료 모음 → `3. Resources/`
- 영구 지식 → `5. Zettelkasten/20. Permanent/`

## Area 예시

- 건강 (운동, 식단, 수면)
- 재무 (예산, 투자, 보험)
- 커리어 (역량 개발, 네트워킹)
- 관계 (가족, 친구, 동료)
- 학습 (독서, 강의, 연구)

## 파일 구조

```
2. Areas/
├── CLAUDE.md
├── 00_Areas_Hub.md             # 전체 영역 대시보드
├── [영역명]/
│   ├── [영역명]_Hub.md         # 영역 허브 노트
│   ├── 주간리뷰_YYYY-WW.md
│   └── ...
└── ...
```

## 영역 허브 노트 Frontmatter

```yaml
---
type: area
status: active               # active | archived
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [area]
related: ["[[관련 Resource]]", "[[관련 Permanent Note]]"]
---
```

## 작업 규칙

1. **기준 정의**: 각 영역 허브 노트에 "이 영역이 잘 관리되는 상태의 기준"을 명시
2. **정기 검토**: 주간/월간 리뷰 노트를 생성하여 기준 충족 여부 점검
3. **프로젝트 분리**: 영역 내 구체적 과제가 생기면 `1. Projects/`에 프로젝트로 분리
4. **지식 분리**: 영역에서 축적된 지식은 `5. Zettelkasten/20. Permanent/`에 영구 노트로 저장
5. **비활성화**: 더 이상 관리하지 않는 영역은 `4. Archive/`로 이동

## Dataview 대시보드

```dataview
TABLE status, updated
FROM "2. Areas"
WHERE type = "area"
SORT file.name ASC
```
