# AX 레볼루션 5·6부 퇴고 워크플로우 — 업무 흐름도

이 파일은 [automation-plan.md](automation-plan.md) 의 업무 흐름도 Mermaid 소스입니다. 렌더링 후 `flowchart.png` 로 저장해 automation-plan.md 의 이미지 자리에 사용합니다.

## 렌더링 방법

- **Mermaid Live Editor** (https://mermaid.live) — 코드 붙여넣고 PNG export
- **mermaid-cli** — `mmdc -i flowchart.md -o flowchart.png` (Node.js 환경)
- **VS Code Mermaid 확장** — 미리보기에서 우클릭 → 이미지로 저장

## 다이어그램

```mermaid
%%{init: {'theme':'base', 'themeVariables': { 'primaryColor':'#ffffff', 'primaryTextColor':'#1a1a1a', 'primaryBorderColor':'#555', 'lineColor':'#555', 'fontSize':'14px'}}}%%
flowchart TD
    Start([챕터 + reference + 통합원고]) --> A1

    subgraph A[Phase A — 이해]
      direction TB
      A1[1.outline ★] --> A2[2.분석 마인드맵] --> A3[3.논증 흐름 ★]
    end
    A3 --> GA{Phase A 게이트<br/>★ 검수 확인}

    GA -->|확인| B1
    subgraph B[Phase B — 검증 병렬]
      direction LR
      B1[4.팩트체크 ★★]
      B2[5.인용체크 ★★]
      B3[6.가상사례 ★★]
      B4[7.챕터 교차 ★]
      B5[8.전체원고 톤 ★★]
    end
    B1 --> GB
    B2 --> GB
    B3 --> GB
    B4 --> GB
    B5 --> GB
    GB{Phase B 게이트<br/>★★ 검수 5종 확인}

    GB -->|전부 확인| C1
    subgraph C[Phase C — 개선]
      direction TB
      C1[9.트리밍 ★★] --> C2[10.스타일 ★★] --> C3[11.주석 ★]
    end
    C3 --> GC{Phase C 게이트<br/>★★ 검수 확인}

    GC -->|확인| D1
    subgraph D[Phase D — 마감]
      direction TB
      D1[12.레퍼런스 ★] --> D2[13.독자 마인드맵]
    end
    D2 --> GD{Phase D 게이트<br/>★ 검수 + 미해결 항목}
    GD -->|마침| End([퇴고 완료])

    classDef star2 fill:#fca5a5,stroke:#7f1d1d,stroke-width:2px,color:#1a1a1a
    classDef star1 fill:#fde68a,stroke:#854d0e,stroke-width:1.5px,color:#1a1a1a
    classDef gate fill:#c7d2fe,stroke:#3730a3,stroke-width:1.5px,color:#1a1a1a
    classDef neutral fill:#e5e7eb,stroke:#4b5563,color:#1a1a1a
    classDef endpoint fill:#d1fae5,stroke:#065f46,stroke-width:2px,color:#1a1a1a
    class B1,B2,B3,B5,C1,C2 star2
    class A1,A3,B4,C3,D1 star1
    class GA,GB,GC,GD gate
    class A2,D2 neutral
    class Start,End endpoint
```
