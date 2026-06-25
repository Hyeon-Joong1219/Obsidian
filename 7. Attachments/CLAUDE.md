# 7. Attachments — 운영 가이드

## 폴더 목적

**이미지, PDF, 오디오 등 바이너리 첨부 파일**을 중앙 집중 보관합니다.  
마크다운 노트와 바이너리 파일을 분리하여 Git 관리와 검색을 용이하게 합니다.

## 어떤 파일이 들어오는가

- 이미지 (`.png`, `.jpg`, `.gif`, `.svg`)
- PDF 문서
- 오디오 파일 (`.mp3`, `.m4a`)
- 기타 임베드 가능한 바이너리 파일

## 파일 구조

```
7. Attachments/
├── CLAUDE.md
├── images/                    # 스크린샷, 다이어그램
├── pdfs/                      # PDF 문서
└── audio/                     # 오디오 녹음
```

## 파일 명명 규칙

```
YYYY-MM-DD_설명적이름.확장자
예: 2025-10-13_architecture-diagram.png
    2025-10-13_book-cover-atomic-habits.jpg
```

## Obsidian 설정

첨부 파일이 자동으로 이 폴더에 저장되도록:  
Settings → Files & Links → Default location for new attachments → `7. Attachments`

## 작업 규칙

1. **자동 저장 설정**: Obsidian 설정에서 첨부 파일 기본 경로를 이 폴더로 지정
2. **고아 파일 정리**: 주기적으로 어느 노트에서도 참조하지 않는 파일 삭제
3. **Git LFS 권장**: 대용량 PDF나 이미지는 Git LFS로 관리 (저장소 크기 제한)
4. **직접 편집 금지**: 첨부 파일 자체를 Obsidian에서 편집하지 않음
5. **노트 내 참조**: `![[파일명.png]]` 형식으로 노트에서 임베드하여 사용

## Git 관리 참고

```gitignore
# .gitignore에 대용량 파일 제외 예시
7. Attachments/pdfs/*.pdf
7. Attachments/audio/
```
