# SYNAPEX Image Assets

랜딩페이지/IR 자료에 사용할 SVG 자산 모음. 모든 파일은 코드 기반 SVG로 작성되어 무한 확대 가능하며, 브랜드 컬러를 직접 사용한다.

## 컬러 토큰
- Midnight Cortex `#0A1A3A`
- Synaptic Cyan `#00E5FF`
- Neural Amber `#FFB547`
- Theta Slate `#5A6B85`
- Bone White `#F4F1EA`

## 파일 구조

| 경로 | 용도 | 권장 사이즈 |
|---|---|---|
| `logo/mark.svg` | 심볼 단독 | 24 ~ 256px |
| `logo/wordmark.svg` | 심볼 + SYNAPEX 텍스트 (다크 배경) | 200 ~ 720px wide |
| `logo/favicon.svg` | 브라우저 favicon, app icon | 16 ~ 64px |
| `hero/eeg-waveform.svg` | 랜딩 Hero 배경 | full-bleed 1200 × 600 |
| `icons/observe.svg` | Cognitive Loop — Observe | 48 ~ 96px |
| `icons/reason.svg` | Cognitive Loop — Reason | 48 ~ 96px |
| `icons/act.svg` | Cognitive Loop — Act | 48 ~ 96px |
| `icons/market-academy.svg` | 학원 시장 | 48 ~ 96px |
| `icons/market-elite.svg` | 임원·전문직 | 48 ~ 96px |
| `icons/market-sports.svg` | 프로 스포츠 | 48 ~ 96px |
| `icons/market-exam.svg` | 수험생 | 48 ~ 96px |
| `patterns/synapse-bg.svg` | 시냅스 네트워크 반복 패턴 | 200 × 200 tile |
| `og/cover.svg` | Open Graph 메타 이미지 | 1200 × 630 |
| `diagrams/roadmap-5phase.svg` | 5-Phase 로드맵 | 1200 × 380 |
| `diagrams/competitor-map.svg` | 경쟁사 포지셔닝 맵 | 800 × 600 |

## OG 이미지 사용 시
HTML에 OG 메타로 `cover.svg`를 직접 쓸 수 있으나, 일부 플랫폼(카카오톡·페이스북 일부)은 SVG를 지원하지 않으므로 PNG로 export 권장:

```bash
# rsvg-convert (macOS: brew install librsvg)
rsvg-convert -w 1200 -h 630 og/cover.svg -o og/cover.png

# 또는 inkscape
inkscape og/cover.svg --export-type=png --export-filename=og/cover.png -w 1200 -h 630
```

## 변형 가이드
- **라이트 모드**: 배경 `#0A1A3A` → `#F4F1EA`, 텍스트는 currentColor 교체
- **인쇄·모노톤**: stroke를 모두 `currentColor`로 치환 후 사용처에서 색 결정
- **의료·보험 자료**: Neural Amber 비중을 낮추고 Midnight + Bone White 중심으로

## 누락 자산 (TODO)
- 디바이스 mockup (실제 EEG 헤드밴드 시제품 사진 확보 후)
- 임상 협력 로고 (병원·대학·제약사)
- 실제 사용자/팀 인물 사진
