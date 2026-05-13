---
markmap:
  colorFreezeLevel: 2
  maxWidth: 320
  initialExpandLevel: 2
  duration: 500
---

# 업무 자동화 도구 설명서

## 1. 환경 구축

### 설치된 프로그램 8개
- Xcode CLT
- Homebrew (패키지 매니저)
- Node.js
- Python 3
- Git
- GitHub CLI (`gh`)
- Claude Code
- VS Code

### VS Code 확장 8개
- `anthropic.claude-code`
- `gabrielgrinberg.auto-run-command`
- `bierner.markdown-mermaid`
- `gera2ld.markmap-vscode`
- `peakchen90.open-html-in-browser`
- `cweijan.vscode-office`
- `tomoki1207.pdf`
- `pkief.material-icon-theme`

### 덮어쓴 설정
- `settings.json` (자동 백업)
- `keybindings.json` (자동 백업)

### 주의사항 3가지
- Claude 권한 우회 모드 ON
- GitHub Copilot 전역 OFF
- `Cmd+O` → 폴더 열기
- `Cmd+1` → HTML 브라우저 열기

---

## 2. Node.js & Python

### 왜 필요한가
- Claude 코드의 **실행 엔진**
- Python → `.py` 실행
- Node.js → `.js`/`.ts` 실행
- 엔진 없으면 코드 못 돌림

### 자동화 영역 90%를 커버
- 엑셀/PDF → Python (`pandas`, `openpyxl`)
- 웹 크롤링 → 둘 다
- 슬랙/노션/시트 → 둘 다 SDK
- 파일 일괄 처리 → Python
- 대시보드/웹 → Node.js

### 부속 패키지 매니저
- `pip` (Python 라이브러리)
- `npm` (Node 라이브러리)
- 한 줄로 부품 설치

### MCP 서버의 토대
- Claude 외부 연결 도구
- 대부분 Node/Python 기반

### 비유
- Claude = 요리사
- Node/Python = 가스레인지

---

## 3. VS Code & Extensions

### VS Code의 역할
- Claude 사이드바 배치
- 파일 변경 즉시 시각화
- 통합 터미널 내장
- 확장으로 무한 확장

### 핵심 확장
- `anthropic.claude-code`
  - 사이드바 Claude 대화
- `gabrielgrinberg.auto-run-command`
  - 시작 2초 후 Claude 자동 오픈

### 문서·파일 미리보기
- `tomoki1207.pdf` — PDF
- `cweijan.vscode-office` — Word/Excel/PPT
- `bierner.markdown-mermaid` — Mermaid
- `gera2ld.markmap-vscode` — 마인드맵

### 편의 기능
- `peakchen90.open-html-in-browser`
  - `Cmd+1` → 브라우저
- `pkief.material-icon-theme`
  - 파일 아이콘 가독성

### 통합 워크플로우
- VS Code 켜기
- Claude 자동 등장
- 코드 작성/수정
- 결과 즉시 미리보기
- 한 창에서 완결

---

## 4. Git & 협업 도구

### 기본 용어
- **터미널** = 검은 글자 화면
- **CLI** = 명령어로 조작
- **레포지토리** = 이력 기록 폴더

### Git이 필요한 이유
- **되돌리기 안전망**
  - `git diff` — 변경 확인
  - `git restore .` — 즉시 복귀
- **버전 관리**
  - 커밋으로 체크포인트
  - 시점 점프 자유
- **GitHub 연동**
  - 자동 백업
  - 공유 링크
  - 포트폴리오

### GitHub CLI (`gh`)
- `gh repo create` — 레포 생성
- `gh pr create` — PR 보내기
- `gh issue list` — 이슈 조회
- Claude가 직접 호출 가능

### 자동화 워크플로우 예시
- `mkdir & git init`
- Claude에 코드 요청
- 잘 되면 `git commit`
- 망가지면 `git restore`
- `gh repo create --push`

---

## 5. 문서 도구 3총사

### 공통점
- 글자로 쓰면 그림이 됨
- AI가 무한히 생성 가능
- Git 버전 관리 가능

### Markdown — Claude의 모국어
- 모든 협업 도구 호환
- GitHub/노션/슬랙/Obsidian
- AI 부분 수정 가능
- 워드 대체

### Mermaid — 텍스트 다이어그램
- 프로세스 플로우차트
- 시퀀스 다이어그램
- SOP·온보딩 자료
- "단계 추가해줘" 1초 수정

### Markmap — 마인드맵
- 마크다운 그대로 변환
- 회의록 시각화
- 보고서 구조 파악
- PPT 대체

### 합쳐진 흐름
- 주간 보고서 자동화
- MD 골격 + Mermaid 차트
- Markmap 임원 요약
- GitHub/노션 자동 게시

---

## 6. HTML — 자동화의 매개체

### 출력 표준
- 브라우저
- 이메일 HTML
- 노션·슬랙 미리보기
- PDF 변환 원본
- 대시보드

### 입력 통로 (웹 스크래핑)
- 경쟁사 가격
- 채용 공고
- 뉴스·공시
- HTML 파싱 라이브러리
  - Python: `BeautifulSoup`, `playwright`
  - Node: `puppeteer`, `cheerio`

### 인터랙티브 보고서
- 정렬/필터 가능
- 차트 호버 수치
- 검색·토글·탭
- Chart.js + Tailwind 인라인

### 이메일 자동화
- 표·버튼·이미지
- 브랜드 일관성
- 클릭 추적

### 다른 도구의 종착지
- Markdown → HTML 렌더
- Mermaid → HTML+SVG
- Markmap → HTML 페이지

### `Cmd+1` 셋업 의미
- HTML 즉시 미리보기
- 빠른 반복 주기
- 결과물 품질 가속

---

## 핵심 비유 한 줄씩

### 도구별 역할
- **Homebrew** — 모든 도구의 설치 통로
- **Node.js / Python** — 가스레인지 (실행 엔진)
- **Git** — 매 순간 사진 찍는 안전망
- **GitHub** — 인터넷 백업·공유 창고
- **터미널/CLI** — Claude와 컴퓨터의 대화 통로
- **레포지토리** — 이력이 기록된 프로젝트 폴더
- **VS Code** — 모든 도구를 다루는 작업실
- **Claude Code** — 요리사 (코드를 짜고 실행)
- **Markdown** — Claude의 모국어
- **Mermaid** — 텍스트로 그리는 다이어그램
- **Markmap** — 마크다운에서 마인드맵
- **HTML** — 결과물의 공용어 + 웹 데이터의 입구
