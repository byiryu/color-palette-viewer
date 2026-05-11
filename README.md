# byiryu-studio-previews

byiryu studio 프로젝트 미리보기 · 디자인 시스템 · 검증 자료 저장소.

**랜딩:** https://byiryu.github.io/byiryu-studio-previews/

## 구조

```
byiryu-studio-previews/
├── index.html                       # 스튜디오 랜딩 (프로젝트 목록)
├── tools/
│   └── color-palette-viewer.html    # 컬러 팔레트 뷰어 (필터 기반)
│
├── weather-outfit/                  # PALETI 프로젝트
│   ├── index.html                   # 이 프로젝트 인덱스
│   ├── design/                      # 프로덕션 디자인 (출시 시 공개)
│   │   └── (출시 전 비어있음)
│   └── sanity/                      # 검증 자료 (의사결정 흔적)
│       ├── v4-1.html                # Claude즉답 색상 5 시나리오
│       ├── v4-2a.html               # 매트릭스+Opus 8 케이스
│       ├── v4-3a.html               # 나이 변수 6 케이스
│       └── design-system-*.html     # UI 컬러 톤 옵션 비교 (5개)
│
├── travel-illust/                   # (미래 — 설계 단계)
└── lego-builder/                    # (미래 — 설계 단계)
```

## 공개 정책

**디자인 작업물 (`{project}/design/`)** — 프로젝트 출시 후 공개. 출시 전엔 로컬 보관.

**검증 자료 (`{project}/sanity/`)** — 의사결정 흔적, 출시 전 작업물이지만 추적 가능성을 위해 공개 유지.

상세 규칙은 워크플로우 마스터 문서 참조: `ApplicationProject/_docs/workflow.md`

## 호스팅

GitHub Pages — 푸시하면 자동 배포.

## 이력

| 일자 | 변경 |
|------|------|
| 2026-05-08 | `color-palette-viewer` 이름으로 V4-1 컬러 팔레트 뷰어 생성 |
| 2026-05-10~11 | weather-outfit 검증 자료 8건 추가 |
| 2026-05-11 | **`byiryu-studio-previews` 로 이름 변경.** 스튜디오 단위 표준 구조 (`{project}/design/` + `{project}/sanity/`) 도입 |
