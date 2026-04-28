# OHOUSE-DESIGN.md

오늘의집 디자인 시스템을 단일 마크다운 파일에 담은 자족(self-contained) 명세 + A/B 시나리오 비교 사이트.

AI 코딩 에이전트(Cursor / Claude Code / Stitch / v0)에 컨텍스트로 입력하면 일관된 오늘의집 UI를 생성합니다.

## 🌐 웹사이트

GitHub Pages 활성화 후: <https://ohouse-product-design.github.io/design.md/>

## 📥 다운로드

| 파일 | 용도 |
|---|---|
| [`OHOUSE-DESIGN.md`](OHOUSE-DESIGN.md) | latest (항상 최신) |
| [`OHOUSE-DESIGN-v0.3.0.md`](OHOUSE-DESIGN-v0.3.0.md) | v0.3.0 스냅샷 (버전 고정) |

## 📂 구조

```
.
├── README.md                       # 이 파일
├── OHOUSE-DESIGN.md                # latest 명세
├── OHOUSE-DESIGN-v0.3.0.md         # 버전 고정본
├── index.html                      # 메인 (시나리오 비교 + 다운로드)
├── about.html                      # About (목적·할 수 있는 것·할 수 없는 것)
├── changelog.html                  # 버전 이력
├── colors.html                     # 컬러 토큰 33종
├── typography.html                 # 타이포 14 스케일
├── components.html                 # 컴포넌트 17종
├── icons.html                      # 아이콘 245종
├── shared.css                      # 공통 스타일
├── ohouse-3d.png                   # 로고
└── 01..07-*.html                   # 시나리오별 with/without/compare (21개)
```

## 사용법

1. `OHOUSE-DESIGN.md` 또는 `OHOUSE-DESIGN-v0.3.0.md`를 다운로드
2. AI 코딩 도구의 프로젝트 루트에 두기
3. 프롬프트 시 참조: `@OHOUSE-DESIGN.md를 따라서 [화면명] 만들어줘`
4. 결과물에 마커(`@ods-component:`, `@non-ods:`)가 자동으로 박힙니다

## 버전

**v0.3.0** (2026-04-28) — Icons 섹션 신규, 컴포넌트 9종 추가, 시나리오 7개 자족 재현 가능. 자세한 변경은 [`changelog.html`](changelog.html) 또는 명세 §12 참조.

## 피드백

Slack `#des_pd`
