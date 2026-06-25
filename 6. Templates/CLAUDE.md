# 6. Templates — 운영 가이드

## 폴더 목적

**일관된 노트 작성을 위한 템플릿**을 보관합니다.  
Obsidian의 Templates 또는 Templater 플러그인과 연동합니다.

## 어떤 파일이 들어오는가

- 각 노트 타입별 템플릿 파일
- Templater 스크립트 (`.js` 파일)
- 재사용 가능한 노트 구조

## 표준 템플릿 목록

| 파일명 | 대상 폴더 | 용도 |
|--------|-----------|------|
| `template-project.md` | 1. Projects/ | 프로젝트 허브 노트 |
| `template-area.md` | 2. Areas/ | 영역 허브 노트 |
| `template-resource.md` | 3. Resources/ | 리소스 노트 |
| `template-literature.md` | 5. Zettelkasten/10. Literature/ | 문헌 노트 |
| `template-permanent.md` | 5. Zettelkasten/20. Permanent/ | 영구 노트 |
| `template-daily.md` | (Daily Notes) | 일일 노트 |

## Templater 동적 값 예시

```
<% tp.date.now("YYYY-MM-DD") %>          # 오늘 날짜
<% tp.file.title %>                       # 현재 파일 제목
<% tp.date.now("YYYY-MM-DD", 0, "week") %> # 이번 주
```

## 작업 규칙

1. **템플릿 수정 시**: 기존 노트에 소급 적용하지 않음. 새 노트부터 적용
2. **Frontmatter 일관성**: 모든 템플릿의 공통 필드(`type`, `status`, `created`, `updated`, `tags`)는 동일하게 유지
3. **버전 표기**: 템플릿 하단에 `<!-- template version: X.X -->` 주석으로 버전 관리
4. **플러그인 의존성 표기**: Templater 문법 사용 시 파일 상단에 의존 플러그인 명시

## Obsidian 설정

- **Templates 플러그인**: Settings → Templates → Template folder location: `6. Templates`
- **Templater 플러그인**: Settings → Templater → Template folder location: `6. Templates`
