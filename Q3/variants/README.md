# SYNAPEX Landing — 5 Variants

랜딩페이지 5종 시안. 사용자 피드백 3가지를 모든 시안에 공통 적용:

1. **투톤 컬러** — 각 시안마다 다른 2색 조합 (모던하게 정리)
2. **동적 요소 강화** — Live canvas, animated SVG, parallax, cursor follower, glow orbs 등
3. **디바이스가 한눈에** — 각 시안 hero 영역에 디바이스 mockup이 큰 비주얼로 등장

## 한눈에 비교

| # | 스타일 | 투톤 컬러 | 디바이스 폼팩터 | 핵심 동적 요소 | 추천 사용처 |
|---|---|---|---|---|---|
| **01** | **Linear v2** | `#06090F` Ink + `#00E5FF` Cyan | 헤드밴드 (정면) | Canvas **live EEG 파형**, 부유 디바이스, ambient orb pulse | SaaS 메인, 개발자·B2B IT |
| **02** | **Bento Grid** | `#000` Black + `#FFB547` Amber | 헤드밴드 (큰 hero card) | 카드별 hover tilt (perspective), bar pulse, scroll reveal stagger | Apple OS17 위젯 톤, B2C 친화 |
| **03** | **Apple** | `#F5F5F7` White + `#1D1D1F` Dark | **안경형 (EEG Glass)** | Hero parallax, 디바이스 회전, 큰 spec 카운터 | 컨슈머 프로덕트, 임원 프레젠테이션 |
| **04** | **Editorial** | `#F4F1EA` Paper + `#0A0A0A` Ink | **Blueprint 도면** (분해 사양도) | Cursor follower (mix-blend-mode), 매거진 grid | IR/리포트, 브랜드 매니페스토 |
| **05** | **Glassmorphism** | `#06060A` + Cyan·Violet·Pink gradient | 미래형 헤드밴드 + 글로우 | Mouse spotlight, 글라스카드 tilt, conic gradient spin | 첨단·미래 톤, 컨퍼런스 키노트 |

## 폴더 구조

```
variants/
├── 01-linear/index.html      ← Linear v2 (Two-tone Midnight + Cyan)
├── 02-bento/index.html       ← Bento Grid (Black + Amber)
├── 03-apple/index.html       ← Apple style (Light, EEG Glasses)
├── 04-editorial/index.html   ← Editorial (Magazine + Blueprint)
├── 05-glass/index.html       ← Glassmorphism (Neural gradient)
└── README.md
```

각 시안은 `../../img/logo/favicon.svg`를 참조합니다. 그 외 자산은 모두 시안 안에 인라인 SVG로 임베드되어 있어 단일 파일로 독립 작동합니다.

## 빠르게 열어보기

```bash
# 한 번에 5개 시안 모두 열기
open variants/01-linear/index.html variants/02-bento/index.html variants/03-apple/index.html variants/04-editorial/index.html variants/05-glass/index.html
```

## 디바이스 폼팩터 비교

| 시안 | 폼팩터 | 표현 방식 |
|---|---|---|
| 01 Linear | **헤드밴드 (4채널)** | 미니멀 line + 센서 노드 pulse + 라이브 EEG 캔버스 |
| 02 Bento | **헤드밴드** | Hero card에서 큰 mockup, glow halo + 센서 blink |
| 03 Apple | **EEG Glasses 안경형** | 측두엽 dry electrode + 이마 micro-sensor 3개 (Vision Pro 영감) |
| 04 Editorial | **헤드밴드 (도면)** | Engineering blueprint — 치수·라벨·축선·sensor pin 표기 |
| 05 Glass | **헤드밴드 (미래형)** | Iridescent stripe + 3색 sensor + 글로우 halo |

> 사용자 피드백을 받기 위해 일부러 같은 헤드밴드/안경 폼팩터를 다양한 표현으로 그려놓았습니다. 어떤 폼팩터가 가장 끌리는지 의견을 주시면 단일 안으로 통일하겠습니다.

## 폰트

- 01, 02, 03, 05: **Inter** + JetBrains Mono
- 04 Editorial: **Fraunces** (serif display) + Inter + JetBrains Mono

모두 Google Fonts CDN만 사용. Pretendard는 메인 페이지(`../index.html`)와의 어울림을 위해 제외하고 Inter로 통일 — 한글도 Inter가 fallback 처리.

## 다음 단계

1. 5개 시안을 브라우저에서 열어 비교 → 마음에 드는 방향 1~2개 선정
2. 선정된 방향으로 메인 `../index.html` 교체
3. 디바이스 폼팩터 확정 후 inline SVG → `img/device/` 별도 자산으로 분리
4. Lottie 또는 mp4 영상(실제 디바이스 360° 회전, 사용 장면 등) 합성 시 별도 발주
