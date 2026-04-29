# OHOUSE-DESIGN.md — Version History

`OHOUSE-DESIGN.md` 단일 파일의 변경 이력. 최신 사양은 항상 `OHOUSE-DESIGN.md` 파일 기준이며, 본 문서는 시간순 변경 내역만 추적한다.

| 버전 | 날짜 | 비고 |
|---|---|---|
| **0.4.1** | 2026-04-29 | **아이콘 sprite 분리** — §13 본문에 있던 ~214KB sprite 데이터를 [`ICONS.md`](./ICONS.md)로 분리. `OHOUSE-DESIGN.md` 본체는 ~44KB로 슬림화 (스펙·룰만 유지). §13은 ICONS.md 사용법으로 축약. AI 에이전트 컨텍스트 입력 시 두 파일을 함께 전달. zip에는 둘 다 포함. |
| 0.4.0 | 2026-04-29 | **245 아이콘 인라인 임베드** — §13 Icon Sprite Library 부록 추가. 실제 SVG path 데이터(`bucketplace/design-assets` regular 1종, 좌표 1자리 정밀도, ~211KB)를 본 파일에 인라인. 외부 fetch / npm install 없이 HTML에서 `<use href="#i-<name>"/>` 로 245개 모두 사용 가능. §7.11 인라인 Sprite 사용법 추가. 파일 단일화: 버전 스냅샷(`OHOUSE-DESIGN-v0.x.0.md`) 폐기, `HISTORY.md`로 이력 분리. |
| 0.3.0 | 2026-04-27 | **자족 재현 가능** — §7 Icons 신규 (`bucketplace/design-assets` 245 아이콘, 카테고리 12종, weight·페어·금지·미러 룰). §8 컴포넌트 9종 추가 (ProductCard / BottomNav / ChipScroll / Avatar / Hero+Body / Author Row / Stats Row / Section Header / Topic-Filter Chip 트랙 분리). §8.0 ODS Sourcing Rule 신규. 시나리오별 적용 가이드 7개 (A~G) 추가. §11.3 비ODS 마커(`@non-ods`) + Figma 보라/회오리 매핑 추가. 7 시나리오(상품/Empty/Error/Dark/Form/Home/Content) 자족 재현 가능. |
| 0.2.0 | 2026-04-27 | **하이브리드** — Google design.md alpha 스펙 호환 YAML front matter 추가 (colors 33 + typography 14 + rounded 5 + spacing 7 + components 15). 토큰 참조 `{colors.x}` 사용. `npx @google/design.md lint` 통과 가능. |
| 0.1.0 | 2026-04-27 | 초판. apps-web ODS 기준, foundations(color/typography/layout/shadow) 인라인. Shapes·Grid 정확값은 TBD. |

## 관리 원칙

- **단일 진실 원본 (Single Source of Truth)**: `OHOUSE-DESIGN.md` 한 파일만 유지. 버전별 스냅샷 파일을 만들지 않는다.
- 과거 버전이 필요하면 `git log OHOUSE-DESIGN.md` 또는 GitHub에서 해당 commit/tag로 조회.
- 버전 태그는 git tag로 관리 (`git tag v0.4.0`).
- 버전 업 시 본 파일 상단에 새 행 추가 (최신이 위로 오도록 시간 역순).

피드백·이슈: `#des_pd` Slack 또는 ohouse-design-atlas repo.
