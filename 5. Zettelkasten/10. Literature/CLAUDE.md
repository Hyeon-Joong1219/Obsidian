# 5. Zettelkasten/10. Literature — 운영 가이드

## 폴더 목적

**외부 원천(책, 논문, 영상, 강의 등)에서 추출한 저자의 생각**을 기록합니다.  
내 해석이나 의견이 아닌, **원저자의 주장을 내 언어로 재서술**한 노트입니다.  
Literature Note는 Permanent Note의 원재료입니다.

## 어떤 노트가 들어오는가

- 책 요약·발췌 노트
- 논문 리뷰 노트
- 강의·영상 핵심 메모
- 팟캐스트, 인터뷰 내용 정리

**들어오지 않는 것**
- 내 의견, 해석, 통찰 → `5. Zettelkasten/20. Permanent/`
- 단순 링크 북마크 → `3. Resources/`

## Literature 노트 Frontmatter

```yaml
---
type: literature
status: processed            # inbox | processed
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [literature, 주제]
author: "저자명"
source: "책/논문/영상 제목"
source_url: ""               # 선택
related: ["[[관련 Permanent Note]]"]
---
```

## Literature 노트 구조

```markdown
# [원천 제목] — Literature Note

## 핵심 주장
저자의 핵심 주장을 1-3문장으로 요약

## 주요 내용
- 중요한 포인트 1
- 중요한 포인트 2

## 인용
> "직접 인용문" (p.XX)

## 내 생각 (처리 메모)
→ 퍼머넌트 노트로 발전시킬 아이디어 메모
→ [[연결할 Permanent Note]]
```

## 처리 흐름

```
원천 읽기 → Literature Note 작성 (저자의 생각)
    ↓
내 통찰 발견 → Permanent Note 작성 (내 언어로 재구성)
    ↓
Literature Note에서 Permanent Note로 링크
    ↓
status를 "processed"로 변경
```

## 작업 규칙

1. **저자 관점 유지**: Literature Note에는 저자의 생각만, 내 의견은 "내 생각" 섹션에만
2. **출처 명시 필수**: `author`, `source` 필드를 항상 기입
3. **원자화 지양**: Literature Note는 하나의 원천을 통째로 커버해도 됨 (Permanent Note가 원자화)
4. **처리 완료 표시**: Permanent Note 작성 후 `status: processed`로 변경
5. **복사 금지**: 원문을 통째로 복사하지 말고 핵심 주장을 내 언어로 재서술

## Dataview 대시보드

```dataview
TABLE author, source, status
FROM "5. Zettelkasten/10. Literature"
WHERE type = "literature"
SORT created DESC
```
