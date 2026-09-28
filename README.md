# Selected AI-assisted Projects

**박준수 | Software Engineer**

AI Coding Agent를 이용해 실제 아이디어를 구현하고,
직접 사용하면서 피드백 → 수정 → 검증을 반복한 프로젝트입니다.

---

## 1. Spirebound

### AI Coding Agent와 반복 개발한 웹 액션 로그라이크

[Repository](https://github.com/baggam-dev/spirebound) ·
[Build Journal](https://github.com/baggam-dev/spirebound/blob/main/docs/build-journal.md)

게임의 컨셉과 핵심 규칙을 텍스트 설계서로 먼저 작성하고,
기능 단위 구현을 AI Coding Agent에게 맡겨 개발했습니다.

    Design
      ↓
    AI Implementation
      ↓
    Play
      ↓
    Feedback
      ↓
    Review
      ↓
    Iterate

AI가 구현한 결과를 직접 플레이한 뒤
난이도, 전투 패턴, 성장 구조, 조작감 등에 대한 피드백을 작성하고
문제 원인과 수정 방향을 함께 검토하는 과정을 반복했습니다.

초기 4층 규모의 프로토타입에서 시작해
8층 규모의 게임으로 확장하면서 다음 기능을 단계적으로 추가했습니다.

- 보스 및 전투 패턴
- 화염·서리·독·번개 성장 시스템
- 스킬 / 유물 / 보상 시스템
- 저장 및 재개
- 모바일 터치 조작
- 보스 테스트 모드
- 전투 시뮬레이션 및 QA

기능이 확장될수록 변경에 따른 회귀 문제를 줄이기 위해
자동 테스트도 함께 보강했습니다.

**42 automated tests → 327 tests**

자동 테스트와 실제 플레이 검증을 구분하고,
테스트가 통과하더라도 체감 난이도나 조작감은 직접 플레이하며 확인했습니다.

**My role**  
컨셉 / 설계 / 요구사항 / 플레이 테스트 / 개선 방향 및 적용 판단

**AI Coding Agent**  
기능 구현 / 코드 분석 / 구현 대안 제시 / 테스트 작성 / 리팩터링

---

## 2. Workdog

### AI를 활용한 개인 문서 아카이브

[Backend](https://github.com/baggam-dev/workdog-archive) ·
[Frontend](https://github.com/baggam-dev/workdog-archive-web)

HWP, PDF, Excel 등 여러 형식의 문서를 저장해도
시간이 지나면 파일명만으로 필요한 내용을 다시 찾기 어렵다는 문제에서 시작했습니다.

전체 서비스 구조와 기능을 설계하고,
Codex에 기능 단위 구현을 맡겨 웹 애플리케이션으로 만들었습니다.

문서를 업로드하면 내용을 추출하고
AI가 한줄 요약, 핵심 내용, 카테고리와 태그를 생성합니다.

이후 제목, 태그, 카테고리, 파일 형식 등을 기준으로
검색하고 관리할 수 있도록 구성했습니다.

주요 기능

- HWP / PDF / XLSX / XLS / TXT 처리
- 문서 텍스트 추출
- AI 요약 / 핵심 포인트 / 카테고리 / 태그 생성
- 검색 / 필터 / 폴더 / 메모
- Node.js API + React Frontend
- 모바일 / 데스크톱 대응

특히 HWP의 표와 중첩 구조처럼
단순 텍스트 추출로 처리하기 어려운 부분은
여러 파싱 방식을 적용하고 결과를 비교하면서 반복적으로 보완했습니다.

**Document → Extract → AI Processing → Search / Manage**

---

### AI Tools

ChatGPT · Claude · Codex