# 5. Zettelkasten/20. Permanent — 운영 가이드

## 폴더 목적

**나만의 언어로 재구성된 영구 지식**의 최종 저장소입니다.  
Zettelkasten의 핵심입니다. 이 폴더의 노트들이 시간이 지나도 가치를 갖는 지식 자산입니다.

## 핵심 원칙

- **One Idea, One Note**: 하나의 Permanent Note는 하나의 주장/개념만 담음
- **내 언어로**: 저자의 말이 아닌, 내가 이해한 방식으로 작성
- **2+ 연결**: 모든 Permanent Note는 최소 2개 이상 기존 노트와 연결
- **고아 노트 금지**: 연결 없는 노트는 지식 발전소의 고장

## 어떤 노트가 들어오는가

- 나만의 통찰과 주장 (`type: permanent`)
- 개념 정의 노트
- 원칙, 멘탈 모델
- 여러 원천을 종합한 통찰

**들어오지 않는 것**
- 저자의 생각 → `5. Zettelkasten/10. Literature/`
- 실행 작업 → `1. Projects/`
- 빠른 메모 → `5. Zettelkasten/00. Inbox/`

## Permanent 노트 Frontmatter

```yaml
---
type: permanent
status: active
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: [permanent, 주제]
source: ["[[Literature Note 1]]", "[[Literature Note 2]]"]
related: ["[[연결된 Permanent Note 1]]", "[[연결된 Permanent Note 2]]"]
---
```

## Permanent 노트 구조

```markdown
# [주장이나 개념을 담은 명료한 제목]

핵심 주장을 첫 단락에 명확하게 서술.
독자(미래의 나)가 첫 단락만 읽어도 핵심을 알 수 있어야 함.

## 상세 설명
더 깊은 맥락과 근거

## 연결된 생각
- [[관련 Permanent Note 1]] — 어떻게 연결되는지
- [[관련 Permanent Note 2]] — 어떻게 연결되는지

## 출처
- [[Literature Note]] — 이 생각의 원천
```

## 제목 가이드라인

좋은 제목 예시:
- "복잡계에서는 예측보다 적응이 우선한다"
- "지식의 저주는 전문가의 소통을 방해한다"
- "습관 형성의 핵심은 마찰 제거다"

나쁜 제목 예시:
- "복잡계" (너무 광범위)
- "책 요약" (Literature Note 역할)
- "메모" (의미 없음)

## 작업 규칙

1. **Literature → Permanent**: Literature Note를 읽고 통찰이 생기면 즉시 Permanent Note 작성
2. **연결 강제**: 작성 직후 기존 노트와 연결하지 않으면 나중에 고아가 됨
3. **발전 허용**: Permanent Note는 시간이 지나며 업데이트되고 분화될 수 있음
4. **삭제 지양**: 틀린 생각도 Archive로 이동, 지식의 흔적은 보존
5. **그래프 뷰 활용**: 주기적으로 그래프 뷰를 확인하여 고립된 노트 발견

## Dataview 대시보드

```dataview
TABLE length(related) as "연결 수", source
FROM "5. Zettelkasten/20. Permanent"
WHERE type = "permanent"
SORT length(related) DESC
```
