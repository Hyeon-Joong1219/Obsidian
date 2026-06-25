# 3. Resources — 운영 가이드

## 폴더 목적

**관심 주제별 참고 자료와 큐레이션된 정보**를 보관합니다.  
현재 당장 쓰지 않더라도 미래에 유용할 수 있는 자료의 저장소입니다.  
"나중에 쓸 것 같다"는 자료는 모두 여기로 옵니다.

## 어떤 노트가 들어오는가

- 주제별 참고 자료 모음 (`type: resource`)
- 북마크 모음, 도구 목록, 체크리스트
- 분야 개요 노트 (특정 주제의 랜드마크 역할)
- 재사용 가능한 스니펫, 레퍼런스

**들어오지 않는 것**
- 원천 문헌 노트(책/논문에서 추출한 노트) → `5. Zettelkasten/10. Literature/`
- 나만의 통찰과 주장 → `5. Zettelkasten/20. Permanent/`
- 프로젝트/영역 종속 자료 → 해당 Project/Area 폴더

## 파일 구조

```
3. Resources/
├── CLAUDE.md
├── 00_Resources_Hub.md         # 주제별 인덱스
├── [주제명]/
│   ├── [주제명]_Hub.md         # 주제 허브
│   └── ...
└── ...
```

## 리소스 노트 Frontmatter

```yaml
---
type: resource
status: active               # active | archived
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [resource, 주제태그]
related: ["[[관련 Permanent Note]]"]
---
```

## 작업 규칙

1. **주제 단위 구성**: 큰 주제별로 하위 폴더를 만들고 허브 노트로 인덱싱
2. **원천 분리**: 특정 책/글에서 나온 내용은 `5. Zettelkasten/10. Literature/`에 먼저 작성 후 링크
3. **큐레이션 우선**: 단순 링크 모음보다 간단한 코멘트와 함께 가치 추가
4. **정기 정리**: 오래된 자료, 더 이상 유효하지 않은 링크 주기적으로 검토
5. **Archive 이동**: 더 이상 참고하지 않는 자료는 `4. Archive/`로 이동

## Dataview 대시보드

```dataview
TABLE tags, updated
FROM "3. Resources"
WHERE type = "resource" AND status = "active"
SORT updated DESC
```
