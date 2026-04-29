---
version: alpha
name: OHOUSE
description: |
  오늘의집(OHOUSE) 디자인 시스템.
  Google design.md alpha 스펙 호환 YAML + VoltAgent awesome-design-md 프로즈 듀얼 레이어.
  YAML은 Light 모드 토큰. Dark 매핑·세부 가이드는 아래 본문 표 참조.
  canonical: Figma `aTdWM1sgdScr68GZdQ2sWO` · 구현: apps-web ODS.

colors:
  # === Background ===
  background: "#ffffff"
  background-weak: "#f5f5f5"
  background-inverse: "#141414"
  background-brand: "#00a1ff"
  background-brand-weak: "#f0f8fc"
  background-emphasis: "#00a1ff"
  background-emphasis-weak: "#f0f8fc"
  background-critical: "#ff7777"          # ⛔ Light 마이그 대기
  background-critical-weak: "#ffeded"     # ⛔ Light 마이그 대기
  background-attention: "#d19506"
  background-attention-weak: "#fcf4dd"
  background-dim: "#00000066"
  background-overlay: "#0000000d"
  background-disabled: "#ededed"
  # === Border ===
  border: "#e0e0e0"
  border-strong: "#141414"
  border-inverse: "#ffffff"
  border-thumbnail: "#0000000d"
  border-brand: "#00a1ff"
  border-emphasis: "#00a1ff"
  border-critical: "#ff7777"              # ⛔ Light 마이그 대기
  border-attention: "#d19506"
  # === Foreground ===
  foreground: "#141414"
  foreground-weak: "#8c8c8c"
  foreground-inverse: "#ffffff"
  foreground-brand: "#00a1ff"
  foreground-emphasis: "#00a1ff"
  foreground-critical: "#f05656"          # ⛔ Light 마이그 대기
  foreground-attention: "#b27800"
  foreground-disabled: "#c1c1c1"
  # === Accent ===
  accent-red: "#fd3d4a"
  accent-yellow: "#ffc300"
  accent-purple: "#6f3dde"
  # === Convention ===
  primary: "#00a1ff"                      # alias of background-brand (lint missing-primary 충족)

typography:
  heading-32-bold:
    fontFamily: Pretendard
    fontSize: 32px
    fontWeight: 700
    lineHeight: 42px
    letterSpacing: -0.3px
  heading-24-bold:
    fontFamily: Pretendard
    fontSize: 24px
    fontWeight: 700
    lineHeight: 32px
    letterSpacing: -0.3px
  heading-20-bold:
    fontFamily: Pretendard
    fontSize: 20px
    fontWeight: 700
    lineHeight: 28px
    letterSpacing: -0.3px
  heading-18-semibold:
    fontFamily: Pretendard
    fontSize: 18px
    fontWeight: 600
    lineHeight: 24px
    letterSpacing: -0.3px
  heading-17-medium:
    fontFamily: Pretendard
    fontSize: 17px
    fontWeight: 500
    lineHeight: 22px
    letterSpacing: -0.3px
  body-16-regular:
    fontFamily: Pretendard
    fontSize: 16px
    fontWeight: 400
    lineHeight: 24px
    letterSpacing: -0.3px
  body-16-medium:
    fontFamily: Pretendard
    fontSize: 16px
    fontWeight: 500
    lineHeight: 24px
    letterSpacing: -0.3px
  body-15-regular:
    fontFamily: Pretendard
    fontSize: 15px
    fontWeight: 400
    lineHeight: 24px
    letterSpacing: -0.3px
  body-14-regular:
    fontFamily: Pretendard
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
    letterSpacing: -0.3px
  detail-13-regular:
    fontFamily: Pretendard
    fontSize: 13px
    fontWeight: 400
    lineHeight: 18px
    letterSpacing: -0.3px
  detail-12-medium:
    fontFamily: Pretendard
    fontSize: 12px
    fontWeight: 500
    lineHeight: 16px
    letterSpacing: -0.3px
  detail-12-regular:
    fontFamily: Pretendard
    fontSize: 12px
    fontWeight: 400
    lineHeight: 16px
    letterSpacing: -0.3px
  detail-11-medium:
    fontFamily: Pretendard
    fontSize: 11px
    fontWeight: 500
    lineHeight: 14px
    letterSpacing: -0.3px
  detail-10-regular:
    fontFamily: Pretendard
    fontSize: 10px
    fontWeight: 400
    lineHeight: 14px
    letterSpacing: -0.3px

rounded:
  sm: 4px
  md: 8px
  lg: 12px
  xl: 16px
  full: 9999px

spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 20px
  "2xl": 24px
  "3xl": 32px

components:
  # === Avatar ===
  avatar:
    $note: "토큰 자세한 정의는 ods/components/Avatar/component.json 참조"
    sizes: [18, 24, 30, 40, 80]
  # === BottomSheet ===
  bottom-sheet:
    textColor: "{colors.foreground}"
  # === BoxButton ===
  box-button-brand-solid:
    backgroundColor: "{colors.background-brand}"
    textColor: "{colors.foreground-inverse}"
  box-button-brand-outlined:
    textColor: "{colors.foreground-brand}"
    borderColor: "{colors.border-brand}"
  box-button-outlined:
    textColor: "{colors.foreground}"
    borderColor: "{colors.border}"
  box-button-solid:
    backgroundColor: "{colors.background-inverse}"
    textColor: "{colors.foreground-inverse}"
  box-button-normal:
    backgroundColor: "{colors.background-weak}"
    textColor: "{colors.foreground}"
  box-button-subtle:
    backgroundColor: "transparent"
    textColor: "{colors.foreground}"
  # === Calendar ===
  calendar:
    backgroundColor: "transparent"
    textColor: "{colors.foreground-inverse}"
    rounded: "8px"
  # === CautionBox ===
  caution-box:
    rounded: "4px"
  # === Checkbox ===
  checkbox:
    rounded: "4px"
    borderColor: "{colors.border}"
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground-inverse}"
  # === Chip ===
  chip:
    $note: "토큰 자세한 정의는 ods/components/Chip/component.json 참조"
  # === CircleBadge ===
  circle-badge:
    rounded: "47px"
    sizes: [16, 20]
  # === Dialog ===
  dialog:
    rounded: "8px"
  # === Divider ===
  divider:
    $note: "토큰 자세한 정의는 ods/components/Divider/component.json 참조"
  # === DotBadge ===
  dot-badge:
    $note: "토큰 자세한 정의는 ods/components/DotBadge/component.json 참조"
  # === Dropdown ===
  dropdown:
    backgroundColor: "--ds-core-color-background (기본) · --ds-core-color-backgroundWeak (disabled)"
    borderColor: "--ds-core-color-border (기본) · --ds-core-color-borderBrand (focus) · --ds-core-color-borderCritical (error)"
    textColor: "--ds-core-color-foreground (complete) · --ds-core-color-foregroundWeak (placeholder) · --ds-core-color-foregroundDisabled (disabled)"
    rounded: "4px"
  # === Empty ===
  empty:
    $note: "토큰 자세한 정의는 ods/components/Empty/component.json 참조"
  # === FloatingBottomSheet ===
  floating-bottom-sheet:
    textColor: "--ds-core-color-foreground (#141414)"
  # === GridThumbnail ===
  grid-thumbnail:
    $note: "토큰 자세한 정의는 ods/components/GridThumbnail/component.json 참조"
  # === IconButton ===
  icon-button:
    $note: "토큰 자세한 정의는 ods/components/IconButton/component.json 참조"
  # === IndicatorDots ===
  indicator-dots:
    $note: "토큰 자세한 정의는 ods/components/IndicatorDots/component.json 참조"
  # === IndicatorNumber ===
  indicator-number:
    rounded: "30px"
  # === Input ===
  input:
    $note: "토큰 자세한 정의는 ods/components/Input/component.json 참조"
    sizes: [32, 40]
  # === PillBadge ===
  pill-badge:
    $note: "토큰 자세한 정의는 ods/components/PillBadge/component.json 참조"
    sizes: [16, 20]
  # === ProductCard ===
  product-card:
    $note: "토큰 자세한 정의는 ods/components/ProductCard/component.json 참조"
  # === RadioGroup ===
  radio-group:
    rounded: "9999px"
  # === ScrapButton ===
  scrap-button-normal:
  scrap-button-media:
  # === SearchField ===
  search-field:
    rounded: "8px"
  # === Section ===
  section:
    $note: "토큰 자세한 정의는 ods/components/Section/component.json 참조"
  # === Snackbar ===
  snackbar:
    backgroundColor: "{colors.background-inverse}"
    textColor: "{colors.foreground-inverse}"
    rounded: "4px"
  # === SquareBadge ===
  square-badge:
    $note: "토큰 자세한 정의는 ods/components/SquareBadge/component.json 참조"
  # === Switch ===
  switch:
    backgroundColor: "{colors.background-inverse}"
    sizes: [medium, small]
  # === Tab ===
  tab:
    $note: "토큰 자세한 정의는 ods/components/Tab/component.json 참조"
  # === TextButton ===
  text-button:
    rounded: "4px"
    sizes: [14, 16]
    variants: [primary, neutral-500, neutral-600]
  # === Thumbnail ===
  thumbnail:
    rounded: "8px"
  # === Tooltip ===
  tooltip:
    rounded: "4px"
  # === Card ===
  card:
    $note: "Compound card container. Card.Product/Card.Image/Card.Title/Card.Price/Card.Review/Card.Benefit 슬롯"
    backgroundColor: "{colors.background}"
    rounded: "{rounded.md}"
  # === ContentTooltip ===
  content-tooltip:
    $note: "콘텐츠 영역 인라인 툴팁. close 버튼 옵션. Tooltip보다 풍부한 콘텐츠"
    backgroundColor: "{colors.background-inverse}"
    textColor: "{colors.foreground-inverse}"
    rounded: "{rounded.sm}"

---

# OHOUSE-DESIGN.md

> **오늘의집(OHOUSE) 디자인 시스템 — 단일 마크다운 명세.**
> 이 파일을 프로젝트 루트(또는 AI 코딩 에이전트 입력)에 두면 Cursor / Claude Code / Stitch / v0 등 어떤 AI 도구도 오늘의집 비주얼 정체성에 맞는 UI를 일관되게 생성합니다.
> 자족적(self-contained) — 외부 파일 의존 없음.
> **하이브리드 포맷**: 위 YAML(Google design.md alpha 호환, 머신 파싱·`npx @google/design.md lint` 가능) + 아래 프로즈(VoltAgent awesome-design-md 스타일, 인간 가독성).

### 📌 버전 정보

| 항목 | 값 |
|---|---|
| **버전** | **v0.4.2** |
| **릴리즈** | 2026-04-29 |
| **기준** | apps-web ODS |
| **Figma canonical** | `aTdWM1sgdScr68GZdQ2sWO` |
| **아이콘 소스** | `bucketplace/design-assets` (245 icons × 4 weights) |
| **검증 방법** | `npx @google/design.md lint OHOUSE-DESIGN.md` |
| **파일 크기** | ~46KB (스펙 본체) + `ICONS.md` ~214KB (245 아이콘 sprite, 분리 관리) |

---

## 🛑 STOP — AI 에이전트가 이 파일을 컨텍스트로 받았다면 가장 먼저 읽을 것

> 이 박스는 §7.12와 §9 Don't 표의 핵심을 **선두에 못 박아둔 것**. 한 번이라도 어기면 결과물 폐기·재작업이다. 자세한 룰은 §7.12 참조.

**아이콘은 절대 직접 그리지 않는다.** 어떤 SVG path도 손으로 작성·추정·기억으로 재구성 금지. 이모지(`🛋️💡🪴🏠`)로 카테고리·기능 아이콘 대체 금지.

**무조건 이 순서로 처리한다:**

1. 화면에 아이콘이 필요하면 먼저 동봉된 **`ICONS.md`** 파일을 연다 (245개 sprite가 거기 있다).
2. 정적 HTML / single-file artifact → `ICONS.md`의 `## Sprite (붙여넣기용)` 블록에서 **필요한 `<symbol id="i-...">` 만 추출**해 `<body>` 직후에 인라인 (전체 245개를 통째로 박지 말고, 화면에서 실제 쓰는 것만 — 보통 15–40개).
3. 본문에선 항상 다음 패턴:
   ```html
   <svg viewBox="0 0 480 480" fill="currentColor"><use href="#i-cart"/></svg>
   ```
4. React/Next.js 프로젝트 → `import { IconCart } from '@bucketplace/icons'` (§7.3-A).
5. ICONS.md에 없는 아이콘이 필요하면? 유사 아이콘으로 대체하거나 placeholder + `@asset:icons/<name>` 마커. **추정 path 그려넣지 말 것.**
6. 출력 끝에 사용한 아이콘 ID 주석을 남긴다:
   ```html
   <!-- icons used: i-cart, i-bell, i-house-filled, i-magnifying-glass, ... -->
   ```

iOS 상태바(WiFi/배터리)처럼 **OS chrome**은 디자인 시스템 범위 외 — sprite 적용 대상 아님. 단 콘텐츠 영역의 모든 기능 아이콘(검색·장바구니·하트·별·홈·집들이·마이·카테고리)은 sprite 필수.

#### 🆕 v0.4.2 주요 업데이트 (2026-04-29)

- **§ STOP 박스 신규 (이 위 박스)** — AI 에이전트 아이콘 룰을 본문 최상단에 못 박음
- **§7.12 AI 에이전트 필수 룰 신규** — SVG path 손그림 / 이모지 아이콘 대체 명시 금지. 위반 시 결과물 폐기·재작업
- **§7.9 금지 항목 보강** — "AI가 SVG path를 직접 그려넣는 행위" 추가
- **§9 Do/Don't 표 13행 신규** — "ICONS.md sprite 사용 vs SVG 손그림·이모지 아이콘" 룰 명시
- **§11.1 사용법 STEP 0 신규** — 모든 화면 작업 시작 전 ICONS.md 동봉 확인 의무화
- 배경: 사내 공유용 zip 배포 직전 사용자 피드백 — "AI가 자꾸 path를 직접 그리거나 이모지로 카테고리 아이콘을 채운다"

이전 변경 내역은 §12 / `HISTORY.md` 참조.

---

## 1. Visual Theme & Atmosphere

**오늘의집(OHOUSE)** — 인테리어·라이프스타일 커머스 플랫폼.
**브랜드 약속**: "집이라는 공간에서 누구나 영감을 얻고, 자기다운 삶을 설계한다."

### 비주얼 원칙 3가지

1. **따뜻함 (Warm)** — 생활감 있는 톤. 과도한 채도·차가운 형광색을 피한다. 화이트 베이스 + 소프트 그레이 + 브랜드 블루 1점.
2. **정돈됨 (Clean)** — 화이트 스페이스 충분히. 정보 위계는 색이 아닌 **크기·위치·여백**으로 표현.
3. **영감을 주는 (Inspiring)** — 사진·콘텐츠가 주인공, UI는 조연. 카드 보더·그림자·테두리는 절제.

### 톤 키워드

`따뜻함` · `정돈됨` · `한국적 가독성` · `사진 우선` · `절제된 강조` · `한 화면 한 액션`

---

## 2. Color Palette & Roles

**룰 0**: **하드코드 hex 금지.** 항상 시멘틱 토큰 또는 팔레트 스케일 참조.
**룰 1**: 다크 모드는 토큰이 자동 매핑한다. `if dark` 분기 금지.
**CSS 변수 prefix**: `--ds-core-color-*` (ODS) · `--ds-ext-*` (트랙 확장) · `--ds-legacy-*` (BDS, 별도 마커 필요).

### 2.1 Background

| 토큰 | Light | Dark | 용도 |
|---|---|---|---|
| `background` | `#ffffff` | `#0a0a0a` | 기본 페이지 배경 |
| `backgroundWeak` | `#f5f5f5` | `#141414` | 약한 배경 (카드, 섹션) |
| `backgroundInverse` | `#141414` | `#f5f5f5` | 반전 배경 |
| `backgroundBrand` | `#00a1ff` | `#00a1ff` | 브랜드 배경 (CTA) |
| `backgroundBrandWeak` | `#f0f8fc` | `#01243f` | 브랜드 약배경 |
| `backgroundEmphasis` | `#00a1ff` | `#00a1ff` | 강조 |
| `backgroundEmphasisWeak` | `#f0f8fc` | `#01243f` | 강조 약배경 |
| `backgroundCritical` ⛔️ | `#ff7777` | `#ef2c3e` | 경고/에러 (Light 마이그 대기) |
| `backgroundCriticalWeak` ⛔️ | `#ffeded` | `#5b030e` | 경고 약배경 (Light 마이그 대기) |
| `backgroundAttention` | `#d19506` | `#b27800` | 주의 |
| `backgroundAttentionWeak` | `#fcf4dd` | `#472300` | 주의 약배경 |
| `backgroundDim` | `#00000066` | `#000000cc` | 딤 오버레이 |
| `backgroundOverlay` | `#0000000d` | `#ffffff0d` | 반투명 오버레이 |
| `backgroundDisabled` | `#ededed` | `#222222` | 비활성 |

### 2.2 Border

| 토큰 | Light | Dark |
|---|---|---|
| `border` | `#e0e0e0` | `#383838` |
| `borderStrong` | `#141414` | `#f5f5f5` |
| `borderInverse` | `#ffffff` | `#0a0a0a` |
| `borderThumbnail` | `#0000000d` | `#0000000d` |
| `borderBrand` | `#00a1ff` | `#00a1ff` |
| `borderEmphasis` | `#00a1ff` | `#00a1ff` |
| `borderCritical` ⛔️ | `#ff7777` | `#fd3d4a` |
| `borderAttention` | `#d19506` | `#b27800` |

### 2.3 Foreground (텍스트·아이콘)

| 토큰 | Light | Dark | 용도 |
|---|---|---|---|
| `foreground` | `#141414` | `#f5f5f5` | 기본 텍스트 |
| `foregroundWeak` | `#8c8c8c` | `#acacac` | 보조 텍스트 |
| `foregroundInverse` | `#ffffff` | `#0a0a0a` | 반전 텍스트 |
| `foregroundBrand` | `#00a1ff` | `#00a1ff` | 브랜드 |
| `foregroundEmphasis` | `#00a1ff` | `#00a1ff` | 강조 |
| `foregroundCritical` ⛔️ | `#f05656` | `#ef2c3e` | 에러 (Light 마이그 대기) |
| `foregroundAttention` | `#b27800` | `#d19506` | 주의 |
| `foregroundDisabled` | `#c1c1c1` | `#737373` | 비활성 |

### 2.4 Accent (포인트 컬러)

| 토큰 | Light | Dark |
|---|---|---|
| `accentRed` | `#fd3d4a` | `#fd3d4a` |
| `accentYellow` | `#ffc300` | `#ffc300` |
| `accentPurple` | `#6f3dde` | `#6f3dde` |

### 2.5 팔레트 (시멘틱 부족 시 fallback)

19단계(50~950) 7종. 직접 사용보다 시멘틱 토큰을 우선 검토.

| 팔레트 | 대표값 | 비고 |
|---|---|---|
| `genuineBlue` | `350` = `#00a1ff` | 브랜드 |
| `red` | `400` = `#fd3d4a` | 에러·강조 |
| `yellow` | `200` = `#ffc300`, `350` = `#d19506` | 주의·리뷰 |
| `purple` | `550` = `#6f3dde` | 액센트 |
| `gray` | `50` = `#f5f5f5` ~ `900` = `#141414` | 중성 |
| `whiteAlpha` / `blackAlpha` | `50` = `0d` ~ `900` = `e6` | 알파 오버레이 |

### 2.6 트랙 확장 (예시)

`--ds-ext-*`. 시멘틱·팔레트에 없을 때만.

- `commerce.color.accentOhousePick` = `#31A072` (오늘의집 Pick)
- `commerce.color.backgroundTodayDeals` = `#ff4747` (오늘의 딜)
- `commerce.color.foregroundReviewStar` = `#f7b401` (리뷰 별점)
- `commerce.color.foregroundTodayDeparture` = `#6131d2` (오늘 출발)
- `o2o.color.backgroundBrandO2OResponsibility` = `#12b667`

---

## 3. Typography Rules

**Font family**: `Pretendard` (Figma canonical) / 코드 fallback `Pretendard Variable, Noto Sans KR, Apple SD Gothic Neo, 맑은 고딕, sans-serif`
**Letter-spacing**: `-0.3px` 전역 고정.
**Weights**: `400 Regular` · `500 Medium` · `600 Semibold` · `700 Bold` (4종).
**한글 우선**. 한글·영문·숫자 동일 스케일 적용.

### 3.1 Heading (제목)

| 토큰 | Size / LineHeight | 권장 용도 |
|---|---|---|
| `Heading32` | 32 / 42 | 랜딩 히어로, 최대 강조 |
| `Heading24` | 24 / 32 | 페이지 타이틀 |
| `Heading20` | 20 / 28 | 섹션 타이틀 |
| `Heading18` | 18 / 24 | 서브 타이틀 / 카드 헤더 |
| `Heading17` | 17 / 22 | 리스트 아이템 헤더 |

### 3.2 Body (본문)

| 토큰 | Size / LineHeight | 권장 용도 |
|---|---|---|
| `Body16L28` | 16 / 28 | 문단 본문 (여유) |
| `Body16L24` | 16 / 24 | 기본 본문 |
| `Body16L20` | 16 / 20 | 빽빽한 UI 텍스트 |
| `Body15L24` | 15 / 24 | 보조 본문 |
| `Body14L20` | 14 / 20 | 작은 본문 |
| `Body14L18` | 14 / 18 | 빽빽한 작은 본문 |

### 3.3 Detail (캡션·라벨·메타)

| 토큰 | Size / LineHeight | 권장 용도 |
|---|---|---|
| `Detail13L18` | 13 / 18 | 캡션 |
| `Detail12L20` | 12 / 20 | 라벨 (여유) |
| `Detail12L16` | 12 / 16 | 라벨 (빽빽) |
| `Detail11L14` | 11 / 14 | 태그 |
| `Detail10L14` | 10 / 14 | 최소 메타 |

### 3.4 고르는 법

- **제목** → `Heading*` (중요도에 따라 17~32)
- **본문** → 기본 `Body16L24`, 문단이면 `Body16L28`
- **캡션·라벨·메타** → `Detail12*` 기본, 태그는 `Detail11`
- **강조 단계는 weight로** (Regular → Medium → Semibold → Bold)
- **letterSpacing 임의 조정 금지**, **임의 사이즈 (15.5/19px 등) 금지**

```css
.title { font-family: Pretendard, sans-serif; font-size: 24px; font-weight: 700;
         line-height: 32px; letter-spacing: -0.3px; }
```

---

## 4. Layout Principles

### 4.1 Breakpoints (4단)

| 이름 | Viewport | Outer Margin |
|---|---|---|
| **Mobile** | `< 768px` | `16px` |
| **Tablet** | `768 ≤ VW < 1024` | `40px` |
| **Laptop** | `1024 ≤ VW < 1256` | `60px` |
| **Desktop** | `≥ 1256px` | `60px` |

```css
.container { padding-inline: 16px; }
@media (min-width: 768px)  { .container { padding-inline: 40px; } }
@media (min-width: 1024px) { .container { padding-inline: 60px; } }
```

### 4.2 Inline Spacing (4의 배수 스케일)

ODS는 inline padding/gap 토큰을 별도 정의하지 않는다. **4의 배수**를 권장 (Tailwind 호환).

| 별칭 | Tailwind | 값 |
|---|---|---|
| xs | `p-1 / gap-1` | 4px |
| sm | `p-2 / gap-2` | 8px |
| md | `p-3 / gap-3` | 12px |
| lg | `p-4 / gap-4` | 16px |
| xl | `p-5 / gap-5` | 20px |
| 2xl | `p-6 / gap-6` | 24px |
| 3xl | `p-8 / gap-8` | 32px |

홀수 px (3·5·7·9 등) 사용 금지.

### 4.3 Grid

Margin(바깥) → Column(콘텐츠 정렬 영역) → Gutter(Column 간격) 3요소.
Mobile ~4col / Tablet ~8col / Laptop·Desktop ~12col 추정. **Gutter 정확값은 TBD** — Figma 명시 "유동적".

---

## 5. Depth & Elevation

**3단계만**. 모두 drop-shadow, offset `0 2`, 베이스 컬러 `#3F474D`.

| 토큰 | 별칭 | CSS box-shadow | 용도 |
|---|---|---|---|
| `Depth 10` | `shadow_thin` | `0 2px 5px 0 #3F474D0D` (5%) | 살짝 뜬 카드, 버튼 hover |
| `depth_20` | `shadow_basic` | `0 2px 5px 0 #3F474D26` (15%) | 일반 카드·패널 |
| `depth_30` | `shadow_thick` | `0 2px 10px 0 #3F474D40` (25%) | 모달·팝오버·드롭다운 |

### 다크 모드는 그림자 사용하지 않는다

대신 배경 대비로 elevation 표현:

```css
.card { box-shadow: 0 2px 5px 0 #3F474D26; }
@media (prefers-color-scheme: dark), [data-appearance="dark"] .card {
  box-shadow: none;
  background: var(--ds-core-color-background); /* backgroundWeak 위에 띄움 */
}
```

임의 box-shadow / depth_15 같은 중간 단계 금지.

---

## 6. Shapes (Border Radius)

**TBD — Tyler 컨펌 후 확정 예정.** 현재 권장값:

| 별칭 | 값 | 용도 |
|---|---|---|
| `radius-sm` | `4px` | 인풋, 칩, 작은 컨트롤 |
| `radius-md` | `8px` | 카드, 버튼 |
| `radius-lg` | `12px` | 모달, 큰 카드 |
| `radius-xl` | `16px` | 바텀시트 상단 |
| `radius-full` | `9999px` | 알약(pill) 형태 |

원형 썸네일·아바타는 `radius-full`. 임의 홀수 radius (3, 5, 7px 등) 금지.

---

## 7. Icons

**소스 (canonical)**: [`bucketplace/design-assets`](https://github.com/bucketplace/design-assets/tree/main/icons) · [Storybook 카탈로그](https://fe.co-workerhou.se/catalog/?path=/docs/documentation-1-icons--docs)
**Production import**: `@bucketplace/icons` (Nexus private registry)

### 7.1 스펙

| 항목 | 값 |
|---|---|
| 총 아이콘 수 | **245** |
| Weight | `regular` / `medium` / `semibold` / `bold` (4종) |
| Render mode | `monochrome` only |
| viewBox | `0 0 480 480` (전체 통일) |
| Fill | `currentColor` (CSS color로 색 컨트롤) |
| 네이밍 | kebab-case (`chevron-left`, `magnifying-glass`) |
| 파일 경로 | `icons/<kebab>/svgs/<kebab>_<weight>_monochrome.svg` |
| React 컴포넌트 | `Icon<PascalCase>` (예: `IconChevronLeft`) |

### 7.2 카테고리 (245 아이콘 분류)

| 분류 | 대표 아이콘 |
|---|---|
| **navigation** | `chevron-left/right/up/down`, `arrow-up/down/left/right`, `arrow-up-from-bracket` (share, iOS 표준) |
| **commerce** | `cart`, `plus-cart`, `tag`, `truck`, `won-sign`, `credit-card`, `store`, `ticket` |
| **engagement** | `heart`, `bookmark`, `star`, `gift`, `award`, `crown`, `sparkles` |
| **communication** | `bubble`, `bubble-left`, `envelope`, `bell`, `phone`, `bullhorn` |
| **control** | `check`, `check-circle`, `x`, `x-circle`, `plus`, `minus`, `circle-filled`, `checkbox-checked` |
| **search/filter** | `magnifying-glass`, `funnel`, `slider-horizontal` |
| **media** | `camera`, `photo`, `play`, `pause`, `video`, `speaker-wave-2` |
| **interior** | `house`, `place-house`, `paint-palette`, `cube`, `wallpaper`, `floor-plank` |
| **people** | `person`, `person-2`, `face-smiling-safety-helmet`, `figure-stand` |
| **status** | `info-circle`, `exclamation-triangle`, `clock`, `calendar`, `spinner-arc` |
| **layout** | `gear`, `ellipsis`, `ellipsis-vertical`, `line-3-horizontal`, `list-bullet`, `square-grid-2x2-filled` |
| **security/location** | `lock`, `shield`, `eye`, `pin`, `location-pin-dot` |

전체 카테고리·파일은 별도 manifest (`_assets/icons/manifest.json`) 참조. 새 아이콘 검색은 위 Storybook URL.

### 7.3 사용법

#### A. React (production) — 항상 이걸 쓸 것
```tsx
import { IconCart, IconHeart } from '@bucketplace/icons';

<IconCart size={24} weight="regular" />
<IconHeart size={20} weight="bold" color="var(--ds-core-color-foreground-brand)" />
```

#### B. SVG sprite (정적 HTML / 프로토타입 한정)
HTML `<body>` 직후 sprite block 인라인:
```html
<svg style="display:none" aria-hidden="true">
  <symbol id="i-cart" viewBox="0 0 480 480"><path d="..."/></symbol>
  <symbol id="i-heart" viewBox="0 0 480 480"><path d="..."/></symbol>
</svg>
```
이후 본문에서:
```html
<svg class="icon" aria-hidden="true"><use href="#i-cart"/></svg>
```
```css
.icon { width:24px; height:24px; fill:currentColor; display:block; }
```

#### C. 직접 SVG 인라인 (단발성)
```html
<!-- icons/cart/svgs/cart_regular_monochrome.svg 내용 그대로 -->
<svg viewBox="0 0 480 480" fill="currentColor">
  <path d="M161 386C175.912 386 ..."/>
</svg>
```

### 7.4 Weight 선택

| Weight | 권장 용도 |
|---|---|
| `regular` | UI 기본 (헤더 IconButton, 인라인 텍스트 옆) |
| `medium` | 약한 강조 |
| `semibold` | 강조 |
| `bold` | 최대 강조 (filled 페어가 있으면 그쪽 우선) |

UI 디폴트는 **`regular`**. 한 화면 안에서 weight 혼용 금지(시각 노이즈).

### 7.5 Outlined ↔ Filled 페어

선택/활성 상태 토글 시 **outlined → filled** 페어로 표현:

| 비활성 (outlined) | 활성 (filled) | 사용 예 |
|---|---|---|
| `heart` | `heart-filled` | 좋아요 |
| `bookmark` | `bookmark-filled` | 스크랩 |
| `star` | `star-filled` | 즐겨찾기·평점 |
| `bell` | `bell-filled` | 알림 받기 |
| `house` | `house-filled` | BottomNav 활성 탭 |
| `cart` | (filled 없음 — 커머스 정체성) | — |

### 7.6 Icon ↔ IconButton 관계

- **Icon** = 콘텐츠 (path 24×24 렌더). 단독 사용 의미 없음.
- **IconButton** (§8.2) = Icon을 감싸는 *컨테이너 컴포넌트* (44×44pt 터치 타깃, focus ring, `aria-label` 필수).
- 인라인 텍스트 옆 아이콘은 *IconText* 패턴 (Icon + 텍스트, 클릭 X).

```html
<!-- IconButton 패턴 -->
<button class="icon-btn" aria-label="장바구니">
  <svg class="icon"><use href="#i-cart"/></svg>
</button>

<!-- IconText 패턴 (별점 표시 등) -->
<span class="icon-text">
  <svg class="icon" style="color:var(--accent-yellow)"><use href="#i-star-filled"/></svg>
  4.8 (1,243)
</span>
```

### 7.7 색상 컨트롤

`fill="currentColor"` 이므로 부모 `color` 속성으로 컨트롤. 시멘틱 토큰 적용:

```css
.icon-default  { color: var(--ds-core-color-foreground); }       /* 기본 */
.icon-weak     { color: var(--ds-core-color-foreground-weak); }   /* 보조 */
.icon-brand    { color: var(--ds-core-color-foreground-brand); }  /* 브랜드 */
.icon-critical { color: var(--ds-core-color-foreground-critical); }/* 에러 */
.icon-yellow   { color: var(--ds-core-color-accent-yellow); }     /* 별점 */
```

### 7.8 사이즈

**16 / 20 / 24 / 32 / 40 / 48** (px) — 4의 배수만 허용.

| 사이즈 | 용도 |
|---|---|
| 14~16 | 인라인 텍스트 옆 (helper, meta) |
| 20 | 작은 IconButton, 본문 인라인 |
| **24** | **UI 기본** (헤더 IconButton) |
| 32 | 강조 IconButton, 빈 상태 미디엄 |
| 40 | IconButton 컨테이너 wrap (24px icon × 40px button) |
| 48 | 큰 컨테이너, 빈 상태 라지 |

### 7.9 금지

- **외부 아이콘 라이브러리** (Lucide, Heroicons, FontAwesome, Material Icons) production 사용 — 프로토타입 한정 OK
- **아이콘 커스텀** (path 손그림, viewBox 변경, weight 발명)
- **monochrome 외 채색** (브랜드 컬러로 그라디언트 등) — 일관성 위반
- **24×24 외 임의 사이즈** (15·17·21·26 등 홀수)
- **`<i data-lucide="...">` Lucide 마커** production 코드
- 🚫 **AI 에이전트가 SVG path를 직접 손으로 그려넣는 행위** — production이든 프로토타입이든 절대 금지. 아래 §7.12 참조.

### 7.12 🛑 AI 에이전트 필수 룰 (Hard Rule)

> **이 파일을 컨텍스트로 받은 모든 AI 코딩 에이전트(Claude Code / Cursor / Stitch / v0 등)는 아래 룰을 반드시 따른다.**

1. **HTML / TSX / JSX에 아이콘이 필요하면 `ICONS.md`를 먼저 연다.** 245개 sprite가 거기 있다.
2. **정적 HTML / single-file artifact** → `ICONS.md`의 `## Sprite (붙여넣기용)` 블록을 `<body>` 직후에 통째로 붙여넣고, 본문에서는 항상 `<svg><use href="#i-<name>"/></svg>` 패턴으로 참조한다.
3. **React 프로젝트** → `@bucketplace/icons` 패키지 import (§7.3-A).
4. **`<path d="...">` 를 직접 작성하지 않는다.** 메모리·추측·LLM-generated SVG path는 비주얼 정체성 깨짐의 가장 흔한 원인. ICONS.md에 없는 아이콘이 필요하면:
   - 먼저 §7.10 미러·`@bucketplace/icons` 카탈로그(Storybook)에서 유사 아이콘으로 대체 검토
   - 그래도 필요하면 `@asset:icons/<name>` 마커만 남기고 임시로 텍스트/이모지로 placeholder 처리. **추정 path 그려넣기 X**
5. **이모지로 아이콘 대체 X** (`🛋️` `💡` 등). 이모지는 OS·브라우저별 렌더가 달라 일관성 무너진다. quick category 같은 카테고리 그리드도 `i-floor-plank`(가구) `i-wallpaper`(패브릭) `i-lightbulb-on`(조명) `i-paint-palette`(데코) 등 ICONS.md sprite로 처리.
6. **status bar / 시스템 UI 아이콘**(WiFi, 배터리)은 OS chrome이므로 디자인 시스템 범위 외 — 이모지·간단 SVG 허용. 단 콘텐츠 영역의 모든 기능 아이콘은 sprite 필수.
7. 출력 마지막에 사용한 아이콘 ID를 주석으로 남길 것:
   ```html
   <!-- icons used: i-cart, i-bell, i-house-filled, i-magnifying-glass, i-photo, i-person, i-heart, i-heart-filled, i-star-filled, i-chevron-right, i-fire, i-sparkles, i-floor-plank, i-wallpaper, i-lightbulb-on, i-paint-palette, i-cube, i-gift, i-ticket -->
   ```

**위반 시 결과물 폐기·재작업 대상.** 이 룰은 v0.4.2 (2026-04-29) 신규 추가. 본문 최상단 🛑 STOP 박스와 §9 표 13행도 함께 참조.

### 7.10 Atlas 미러 (`_assets/icons/`)

자주 쓰는 ~20개만 미러 (regular + bold 2종): `cart`, `chevron-left/right`, `heart`, `heart-filled`, `bookmark`, `bookmark-filled`, `share`(=`arrow-up-from-bracket`), `x`, `x-circle`, `check`, `exclamation-triangle`, `magnifying-glass`, `bell`, `star`, `star-filled`, `house`, `house-filled`, `person`, `bubble`, `ellipsis`, `funnel`, `slider-horizontal`, `photo`, `plus`, `minus`, `calendar`.

그 외는 `@bucketplace/icons` 패키지 직접 import. `bucketplace/design-assets` repo의 다른 아이콘이 필요하면 `@asset:icons/<name>` 마커 + 미러 폴더에 추가 다운로드.

### 7.11 인라인 Sprite (자족성 100%)

정적 HTML / 프로토타입 / AI 에이전트 출력에서 245개 아이콘을 모두 사용 가능. 실제 SVG path 데이터는 **별도 파일 [`ICONS.md`](./ICONS.md)** 에 분리 관리 (~214KB). 본 파일과 `ICONS.md` 두 개를 함께 컨텍스트로 입력하면 됨. 자세한 사용법은 §13 참조.

```html
<!-- ICONS.md "Sprite (붙여넣기용)" 코드 블록을 body 직후에 한 번 붙여넣기 -->
<!-- 본문에서 -->
<svg width="24" height="24" fill="currentColor"><use href="#i-cart"/></svg>
```

production 코드는 §7.3-A (`@bucketplace/icons` import) 우선. 인라인 sprite는 정적 HTML / single-file artifact 한정.

---

## 8. Component Stylings

**컴포넌트 분기 룰 (ODS Sourcing Rule)**:

```
Figma 컴포넌트 사용 시 결정 트리:
  1. ODS에 있나? → ODS 컴포넌트 import (apps-web @bucketplace/design-system)
  2. ODS에 없나?
     a. BDS(레거시)에 있나? → BDS import + @bds-component:<name> 마커 (마이그 대상)
     b. 트랙 고유 변형(Plain Tab, Topic Chip, Filter Chip 등)? → 트랙 컴포넌트로 분리 + @non-ods:<name>
     c. 새 패턴이면 patterns/에 등록 + 근거 기록
  3. Figma에서 비ODS 마커(🟣 보라 / 🌀 회오리) 보이면 즉시 (b) 분기로
```

**비ODS 컴포넌트 표시는 코드 출력에 반드시 마커**: `@non-ods:<name>`, `@bds-component:<name>`, `@missing-ods:<설명>`. 자세한 룰 §11.3.

핵심 ODS 컴포넌트 + 합성 패턴 컴포넌트 정리. 모든 컴포넌트는 **포커스 링 절대 제거 금지**, **모바일 터치 타깃 44×44pt 이상**.

### 8.1 BoxButton

박스형 버튼. 페이지 이동은 `Link` 사용 (`BoxButton`은 액션 전용).

- **variants**: `normal` · `subtle` · `solid` · `outlined` · `brand-solid` · `brand-outlined`
- **sizes** (높이): `extra-large` 48 · `large` 44 · `medium` 40 · `small` 32 · `extra-small` 28 (px)
- **brand-solid 예시**: bg `backgroundBrand` (`#00a1ff`), label `foregroundInverse` (`#ffffff`), disabled bg `backgroundDisabled`
- **outlined**: bg transparent, border `border`, label `foreground`
- **slots**: `BoxButton.Slot side=left|center|right` + `BoxButton.Label` + `BoxButton.Icon`
- **금지**: 같은 화면에 동일 우선순위 `brand-solid` 2개

### 8.2 IconButton

아이콘만 가지는 버튼. 항상 `aria-label` 필수.
- **sizes**: 24 / 32 / 40 / 48 (px 정사각)
- **variants**: `ghost` (bg 없음) / `subtle` (bg `backgroundWeak`) / `inverse` (다크 배경 위)
- 페이지 이동은 X.

### 8.3 Input (TextField)

- **height**: `large` 48 · `medium` 40 · `small` 32
- **bg**: `background`, **border**: `border`, focus border: `borderEmphasis`
- **label**: `Detail12L16_Medium`, **placeholder**: `foregroundWeak`
- **에러 상태**: border `borderCritical`, helper text `foregroundCritical`
- 비활성 시 bg `backgroundDisabled` + label `foregroundDisabled`

### 8.4 Section

콘텐츠 그룹 컨테이너. 헤더(`Heading20` 또는 `Heading18`) + 옵션 RightAction(`TextButton`) + 본문.
좌우 padding은 outer margin과 동기화 (Mobile 16 / Tablet 40 / Laptop+ 60).

### 8.5 Chip

선택형 또는 라벨용 작은 컨트롤.
- **height**: 28 / 32
- **radius**: `radius-full` (pill) 기본
- **default**: bg `backgroundWeak`, label `foreground`
- **selected**: bg `backgroundBrandWeak`, border `borderBrand`, label `foregroundBrand`

### 8.6 BottomSheet

모바일 우선 패턴. 상단 라운드 `radius-xl` (`16px`), 핸들바(`gray-200` 4x40) 상단 노출.
백드롭 `backgroundDim`. 시트 본문 padding `16` (Mobile).
다크 모드에서는 shadow X — 배경 대비로 elevation 표현.

### 8.7 Snackbar

화면 하단에 일시 표시되는 피드백.
- bg `backgroundInverse`, label `foregroundInverse`
- duration: 2~4초, 단일 액션 슬롯 1개 허용
- 동시에 여러 개 띄우지 말 것 — 큐잉

### 8.8 Empty

빈 상태 컴포넌트. **에러·빈 상태는 퍼스트 시민.** 일러스트 또는 아이콘 + 안내 문구 + 다음 액션 1개.
- 일러스트 정사각, 콘텐츠는 가로 중앙 정렬
- 텍스트: 타이틀 `Heading18` + 설명 `Body14L20` (`foregroundWeak`)
- "데이터가 없습니다" 같은 한 줄 텍스트만 두지 말 것

### 8.9 ProductCard (커머스 상품 카드)

상품 그리드의 단위 카드. **카드 보더 없음** — 여백으로 구분 (콘텐츠 우선 원칙).
- **이미지**: 1:1 (피드) 또는 3:4 (상세 갤러리). `border-radius: var(--rounded.md)` 8px
- **이미지 위 floating FAV**: 우하단 28×28 반투명 흰 원 (`rgba(255,255,255,0.85)`) + `heart` 아이콘 16px
- **brand 라벨**: `Detail11_Regular` (`foregroundWeak`) — 셀러 이름
- **상품명**: `Body14L18` (`foreground`) · 2줄 클램프 (`-webkit-line-clamp: 2`)
- **가격 행**: 할인율 `Body14_Bold` `accentRed` "32%" + 가격 `Body14_Bold` `foreground` "1,290,000원"
- **메타**: 별점 `Detail11_Regular` `foregroundWeak` ("★ 4.8 (1,243)")
- **할인 표기**: 한국 관습 — `"32%"` (마이너스 부호 X), 통화는 `"1,290,000원"` (₩ X)

```html
<div class="pcard">
  <div class="pcard-img" style="background-image:url(...)"><div class="pcard-fav">♥</div></div>
  <div class="pcard-brand">자취살림</div>
  <div class="pcard-name">모듈 패브릭 4인 소파</div>
  <div class="pcard-price-row"><span class="discount">32%</span><span class="price">1,290,000원</span></div>
  <div class="pcard-meta">★ 4.8 (1,243)</div>
</div>
```

### 8.10 BottomNav (하단 4탭)

- **height**: 56px, `background`, `border-top: 1px solid backgroundWeak`
- **4탭 (오늘의집 표준)**: 홈 / 검색 / 집들이(콘텐츠) / 마이
- **아이콘**: 활성 = `*-filled` (예: `house-filled`) + `foreground`, 비활성 = outlined + `foregroundWeak`
- **라벨**: `Detail10_Medium` 10/14, 한글 짧게
- **활성 상태 색**: `foreground` (검정, 절제) — brand 블루 X (오늘의집 BottomNav 관습)

```html
<div class="bottomnav">
  <button class="nav-item active"><svg><use href="#i-house-filled"/></svg><span>홈</span></button>
  <button class="nav-item"><svg><use href="#i-magnifying-glass"/></svg><span>검색</span></button>
  <button class="nav-item"><svg><use href="#i-photo"/></svg><span>집들이</span></button>
  <button class="nav-item"><svg><use href="#i-person"/></svg><span>마이</span></button>
</div>
```

### 8.11 ChipScroll (가로 스크롤 카테고리)

피드 헤더 카테고리. `display:flex; overflow-x:auto`, scrollbar 숨김.
- chip selected = `background: foreground` (검정), `color: foregroundInverse` (흰)
- chip 비선택 = `background: backgroundWeak`, `color: foreground`
- chip height 32, padding `0 14`, `Detail13_Medium`, `radius-full`

### 8.12 Avatar

원형 아바타. `radius-full`. 사이즈 24 / 32 / 40 / 64 (px).
- 이미지 없으면 **그라디언트 background** (`linear-gradient(135deg,#ffc8a8,#ff9c7a)`) + 이니셜 (선택)
- 보더 X (특별한 경우 `border: 1px solid borderThumbnail` 0.05 alpha)

### 8.13 Hero + Body (콘텐츠 상세 레이아웃)

집들이·노하우 등 콘텐츠 상세의 표준 레이아웃.
- **Hero image**: `aspect-ratio: 3/4` (인테리어 콘텐츠 카드 원칙). full-bleed (좌우 padding 0)
- **Top bar**: hero 위에 floating, `position: absolute; top: 0`, `background: linear-gradient(180deg,rgba(0,0,0,0.4),transparent)` — 사진과 단절 X
- **Body padding**: 20 16 24 (top right bottom left mobile)
- **인라인 사진**: full-bleed (`margin: 20px -16px`), border-radius 0 — 콘텐츠 임팩트 우선

### 8.14 Author Row (콘텐츠 작성자)

콘텐츠 상세 상단의 작성자 정보 row. **왼쪽 정렬** (인스타식 가운데 정렬 X — 정보 위계 우선).
- Avatar 40 + 이름·메타 stack + 팔로우 버튼 (오른쪽)
- 이름: `Body14_Semibold`, 메타: `Detail12_Regular foregroundWeak` ("팔로워 12.4K · 게시물 47")
- **팔로우 버튼**: `box-button-outlined` size small (32) 한글 "팔로우". 강조 X — `brand-solid` 사용 시 다른 CTA와 충돌

### 8.15 Stats Row (좋아요·스크랩·댓글 카운트)

콘텐츠 액션 카운터 row. `border-top` + `border-bottom` `backgroundWeak`, padding 16 0.
- 항목 간 gap 24, 각 항목: 아이콘 20 + 카운트 `Body14_Regular`
- **활성 상태**: `bookmark-filled` 사용 + `foregroundBrand`
- 한국식 카운트 표기: "1.2K" (1,200) "8.9K" (8,900)

### 8.16 Section Header (섹션 헤더)

섹션 시작 헤더. 좌측 타이틀 + 우측 "더보기 →" (선택).
- 타이틀 `Heading18_Semibold` (페이지 내 섹션) 또는 `Heading20_Bold` (메인 섹션)
- 더보기 텍스트: `Detail13_Regular foregroundWeak` + chevron-right 14px
- margin-bottom 12px (본문과 거리)

### 8.17 Topic Chip / Filter Chip (트랙 컴포넌트, 비ODS)

ODS Chip(§8.5)이 커버 못 하는 변형. **트랙 컴포넌트로 분리** + `@non-ods:topic-chip` 마커.
- **Topic Chip**: 콘텐츠 태그용 (검색 결과·필터 외). 평형/스타일/거주민 메타. bg `backgroundWeak`, label `foreground`, height 24~28
- **Filter Chip**: 정렬·필터 토글. `funnel` 아이콘 + 라벨 + chevron-down. selected = bg `backgroundEmphasis-weak` + label `foregroundEmphasis`

이 두 변형은 ODS에 정식 포함되면 마커 제거.

---

## 시나리오별 적용 가이드 (자족 재현용)

이 섹션은 본 파일만으로 7개 핵심 시나리오를 AI 도구가 재현 가능하게 하는 조립 레시피.

### A. 상품 상세 (Product Detail)
컴포넌트: TopBar(IconButton ×3) + 갤러리(3:4) + Body padding 16 + Section divider 8px `bg-weak` + Heading18 타이틀 + Detail13 별점 행 + 가격 행 (할인율 `accent-red` + 가격 `foreground`) + Chip 컬러 옵션 + delivery-row (`bg-weak` 카드) + 리뷰 카드 + BottomBar(IconButton heart + brand-solid CTA)
핵심 토큰: `Pretendard -0.3px`, `radius-md` 8 버튼, 갤러리 3:4, padding 16 mobile

### B. 빈 장바구니 (Empty)
TopBar + Empty 패턴 (120 원형 컨테이너 `bg-weak` + cart 아이콘 60 `fg-weak`) + Heading18 + Body14L20 + Section "이런 상품은 어때요?" + 추천 ProductCard 2개 (3:4) + brand-solid CTA "쇼핑 계속하기"

### C. 결제 실패 (Error)
TopBar(X close) + Empty-like 패턴 (72 원형 `bg-critical-weak` + exclamation-triangle 36 `fg-critical`) + Heading18 + Body14 weak + info-card (`bg-weak`) + Bottom 액션 stack (brand-solid 메인 + TextButton 보조)
**룰**: critical 토큰은 컨테이너만, 본문은 정상 fg. CTA는 brand-solid (red 사용 X — 위계와 색 분리 원칙)

### D. 다크 모드
A 또는 B를 그대로, 단 §2 Dark 컬럼 hex 사용. **shadow 제거**, border 1px로 elevation 표현 (§5).

### E. 회원가입 폼 (Form)
TopBar + Heading24 페이지 타이틀 + Body14 weak 설명 + Field stack (label `Detail12_Medium` + Input 48 `radius-sm` + helper). error 상태: border `border-critical` + helper에 exclamation-triangle 14 + `fg-critical`. Checkbox 20×20 (체크 시 `bg-brand` + `fg-inverse`). Bottom brand-solid full-width.

### F. 홈 피드 (Home)
TopBar(로고 brand + IconButton ×3 + cart 배지) + ChipScroll 카테고리 (selected = fg) + Section "오늘의 추천" (헤더 + "더보기 →") + ProductCard 2×n 그리드 + BottomNav 4탭

### G. 콘텐츠 상세 (Content / 집들이)
TopBar floating 그라디언트 + Hero 3:4 + Body padding 20 16 + Author Row + Topic Chips (평형/스타일/거주민) + Heading24 제목 + Body16L28 본문 + 인라인 사진 full-bleed + Stats Row (heart/bookmark-filled brand/bubble) + Bottom 댓글 input + share IconButton

---

## 9. Do's and Don'ts

| # | Do | Don't |
|---|---|---|
| 1 | 카드 border 최소화, 여백으로 구분 | 과한 그림자·두꺼운 테두리·원색 배경으로 콘텐츠 시선 분산 |
| 2 | 1 화면 = 1 주요 액션, CTA는 `brand-solid` 1개 | 동일 우선순위 `brand-solid` 2개 이상 병치 |
| 3 | `word-break: keep-all`, `line-height: 1.5~1.7` | 영문 기준 타이포 스케일을 한글에 그대로 적용 |
| 4 | 중요한 것은 크게, 위로, 여백 크게 (위계는 사이즈·위치·여백으로) | "중요하니까 빨간색" — 색으로 위계 표현 |
| 5 | 빈 상태 일러스트 + 다음 액션 제시 | "데이터가 없습니다" 한 줄로 끝 |
| 6 | 0.3~2초는 스켈레톤(실제 레이아웃과 일치), 2초+는 진행률 | 모든 상황에 스피너 |
| 7 | 모바일 터치 타깃 44x44pt 이상, 인접 버튼 간격 8pt+ | 작은 터치 타깃·맞붙은 버튼 |
| 8 | 시멘틱 토큰 우선, 다크 자동 매핑 의존 | 하드코드 hex, `if dark` 분기, 팔레트 직접 참조 |
| 9 | 모션 duration `200ms` ease-out, 페이지 전환 `300ms` | 과한 애니메이션 (1세션 3건 초과 금지) |
| 10 | 포커스 링 유지, alt 텍스트 필수, 텍스트 대비 WCAG AA(4.5:1) 이상 | 포커스 링 제거, alt 누락, 저대비 텍스트 |
| 11 | 트랙 고유 패턴은 근거 기록 후 등록 | 일관성 깨고 트랙 고유 발명 |
| 12 | 디자인 근거를 데이터(A/B, 퍼널)로 기록 | "느낌"으로만 판단 |
| 13 🛑 | **`ICONS.md` sprite를 `<use href="#i-...">` 패턴으로** 사용 (§7.12 / 본문 최상단 STOP 박스) | **AI가 SVG `<path d=...>` 를 직접 그리거나 추정·기억으로 작성**, **이모지(🛋️💡🪴🏠)로 카테고리·기능 아이콘 대체** |

### 원칙 충돌 시 우선순위

1. 접근성 → 2. 가독성 → 3. 일관성 → 4. 결정 피로 절감 → 5. 나머지

---

## 10. Responsive Behavior

**Mobile-first.** Mobile 레이아웃을 기본으로 작성하고 Tablet 이상에서 점진적 확장.

| 브레이크포인트 | 전략 |
|---|---|
| Mobile (< 768) | 1-column 스택, outer margin 16, 풀폭 컴포넌트, BottomSheet 선호 |
| Tablet (768~1024) | 콘텐츠 폭 유지·좌우 마진 40 확장, 2-column 일부 |
| Laptop (1024~1256) | PC 최적화 전환, 사이드바·다단 카드 그리드 활성 |
| Desktop (≥1256) | Laptop과 동일 체계, 내부 grid만 확장 (margin 60 유지) |

- 이미지: 정사각 기본, 콘텐츠 카드는 3:4. `object-fit: cover` + alt 한글 필수.
- 텍스트: Heading은 모바일에서 한 단계 작게 (예: `Heading24` → `Heading20`) 운영 권장.
- 인터랙션: 호버 효과는 `(hover: hover)` 미디어 쿼리로 가드.

---

## 11. Agent Prompt Guide

### 11.1 이 파일 사용법

**STEP 0 (필수)**: 화면 작업 전, 본문 최상단 🛑 STOP 박스와 §7.12를 반드시 먼저 읽는다. 아이콘은 `ICONS.md` sprite + `<use href="#i-...">` 패턴 외 다른 방법 금지 (SVG path 손그림·이모지 대체 위반 시 결과물 폐기·재작업).

1. AI 코딩 에이전트(Cursor / Claude Code / Stitch / v0 등) 프로젝트 루트에 **`OHOUSE-DESIGN.md` + `ICONS.md` 둘 다** 저장 (zip 안에 함께 동봉되어 있음)
2. 첫 프롬프트에 "`@OHOUSE-DESIGN.md` `@ICONS.md` 를 따라 [화면명] 구현해줘. 아이콘은 ICONS.md sprite를 `<use>` 패턴으로 사용해줘."
3. 결과물에 마커가 자동 삽입되는지 확인 (10.3 참조) + `<!-- icons used: ... -->` 주석 확인

### 11.2 예시 프롬프트

```
@OHOUSE-DESIGN.md 를 따라 오늘의집 상품 상세 페이지를 만들어줘.
- 모바일 우선
- 상단 이미지 갤러리(3:4) + 타이틀(Heading24) + 가격(Heading20) + 리뷰 별점
- 하단 고정 CTA: brand-solid BoxButton(large)
- 라이트/다크 양쪽 토큰 적용
```

```
@OHOUSE-DESIGN.md 기준으로 빈 장바구니 화면을 만들어줘.
Empty 컴포넌트 패턴 사용, 일러스트 + 안내 문구 + "쇼핑 계속하기" 액션 1개.
```

```
@OHOUSE-DESIGN.md 의 컬러·타이포만 적용해서 기존 컴포넌트 라이트/다크 토큰화해줘.
하드코드 hex 전부 시멘틱 토큰으로 교체.
```

### 11.3 마커 컨벤션 (선택)

생성된 HTML/TSX에 다음 주석 마커를 남기면 다음 iteration에서 재조회 비용이 줄어듭니다.

- `@ods-component:<name>` — ODS 공식 컴포넌트 사용 (예: `BoxButton variant=brand-solid size=large`)
- `@bds-component:<name>` — 레거시 BDS 컴포넌트 (마이그 대상)
- `@non-ods:<name>` — **ODS 외 트랙 컴포넌트** (Plain Tab / Topic Chip / Filter Chip 등). Figma 비ODS 마커(🟣 보라 / 🌀 회오리)에 대응. ODS 정식 편입 시 마커 제거.
- `@figma-based:<node>` — Figma 노드 기반 직접 구현 (ODS 없음, 트랙으로 분리 안 된 상태)
- `@missing-ods:<설명>` — ODS에 없어서 임시 구현 (피드백 루프 대상, `#ds-feedback-loop` Slack)
- `@asset:icons/<name>` — `bucketplace/design-assets` 미러 외 아이콘 사용 — 추가 다운로드 필요 신호
- `@use-tailwind` — Tailwind 직접 사용 (ODS 외 임시)
- `@deprecated-critical-light` — Light 마이그 대기 토큰 직접 참조 (⛔️ 4개)
- `@typography-mismatch` — Figma↔코드 타이포 불일치 발견

#### Figma 비ODS 마커 ↔ 코드 마커 매핑

| Figma 마커 (시각) | 코드 마커 | 의미 |
|---|---|---|
| 🟣 (보라 동그라미) | `@non-ods:<name>` | ODS 후보지만 정식 미편입 |
| 🌀 (회오리) | `@non-ods:<name> reason=track-variant` | 트랙 고유 변형 (Plain Tab 등) |
| (마커 없음 + ODS 매핑 가능) | `@ods-component:<name>` | 정식 ODS |
| (마커 없음 + ODS 매핑 X) | `@figma-based:<node>` 또는 `@missing-ods:` | ODS·BDS 모두 없음 |

이 매핑은 디어님(이선진) 워크플로우 약점 ⑤ "비ODS 컴포넌트 표시 누락" 해결책. Tyler님이 정리한 Figma 컨벤션과 alignment.

### 11.4 Figma ↔ 코드 불일치 시 우선순위

1. **컬러**: 코드(`@bucketplace/tokens`) 우선 — 단, ⛔️ 표시된 4개 Critical Light는 Figma 신규 매핑 대기
2. **타이포 사이즈/네이밍**: Figma canonical 우선 (예: `Heading24_Bold`)
3. **shadow**: 둘 다 동일 (단일 진실)
4. **다크 모드**: 토큰이 자동 — 직접 매핑 금지

### 11.5 플랫폼 범위

- **Web** (apps-web ODS) — Phase 1, 본 파일 기준.
- **iOS / Android** — Phase 2 예정. 현재 컴포넌트 canonical 이름은 플랫폼 독립 (예: `BoxButton`은 SwiftUI / Compose에서도 동일 이름 권장).

---

## 12. 변경 이력

전체 변경 이력은 [`HISTORY.md`](./HISTORY.md) 참조. 본 파일은 항상 단일 최신본으로 유지하며, 과거 버전은 git log / git tag로 조회한다.

피드백·이슈: `#des_pd` Slack 또는 ohouse-design-atlas repo.


---


## 13. Icon Sprite — 별도 파일

245개 아이콘의 실제 SVG path는 본 파일에서 분리되어 [`ICONS.md`](./ICONS.md)에 별도 관리한다 (~214KB). 본 파일이 비대해지지 않도록 데이터 부록을 외부화한 것이며, 사용 룰·금지·페어 등 스펙은 모두 §7에 그대로 유지된다.

### 13.1 AI 에이전트 사용법

두 파일을 함께 컨텍스트로 입력:

```
@OHOUSE-DESIGN.md @ICONS.md 를 참고해서 [화면명] 만들어줘.
ICONS.md의 sprite 블록을 HTML <body> 직후에 그대로 붙여넣고,
본문에서는 <use href="#i-cart"/> 패턴으로 245개 아이콘 모두 사용 가능.
```

에이전트는 ICONS.md의 sprite를 그대로 HTML에 임베드해 §7 스펙(viewBox 480, currentColor, weight 룰, outlined↔filled 페어 등)에 맞게 사용하면 된다.

### 13.2 정적 HTML / 프로토타입

ICONS.md의 "## Sprite (붙여넣기용)" 섹션 코드 블록을 그대로 복사해 HTML `<body>` 직후에 붙여넣기. 이후 본문에서:

```html
<svg width="24" height="24" fill="currentColor"><use href="#i-cart"/></svg>
```

### 13.3 ICONS.md 자체 사양

- 총 245 symbol / `regular` weight 1종 / viewBox `0 0 480 480` / fill `currentColor`
- ID prefix `i-` (§7.2 카테고리 명칭과 동일)
- 좌표 정밀도 소수점 1자리 (원본 대비 22.7% 압축, 시각적 차이 없음)
- 다른 weight 필요 시 `@bucketplace/icons` 패키지 직접 import
