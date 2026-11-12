### 👋 안녕하세요, 백엔드 개발자 **주상우**입니다.

**AI를 활용해 작업 효율을 극대화**하려고 하고 있습니다.

## 🚀 Side Projects

### 🎧 [결 gyeol](https://github.com/SANGWOO-JOO/gyeol) · [프로토타입 보기](https://claude.ai/artifact/YADs8B6nGSj92PNn62cc5U)
> 친구와 노래를 모으면 우리만의 음악 은하가 생기는 서비스. 가수는 행성, 담은 노래는 그 둘레를 도는 위성

`🛠 리뉴얼 진행 중 · 기획·프로토타입 단계`

**핵심 기능**
- 가입 없이 링크로 들어와(닉네임 + 4자리 암호) 각자 좋아하는 노래를 담으면, 비슷한 가수끼리 가까이 놓인 은하에 행성과 위성이 생김
- 친구와 **같은 노래를 고르면 금빛 위성 하나로 합쳐지고**, 두 사람 취향 사이에서 **함께 들으면 좋은 아티스트**를 추천
- 행성 배치는 음향 특성이 아니라 **근거 자료로 쓴 가수 설명(RAG) → 임베딩 → UMAP 2D**로 계산

**리뉴얼 배경**
- **문제:** 기존 "곡 몇 개 → 추천 20곡"은 결과가 늦고, 스트리밍 앱 추천과 차별점이 약해 다시 쓰거나 공유할 이유가 부족했음
- **결정:** 추천 정확도 경쟁 대신 "친구와 함께 취향을 비교하는 경험"으로 방향을 바꾸고, 기존 RAG·임베딩 파이프라인을 그대로 재사용

**현재 버전에서 검증한 것**
- **RAG가 정말 필요한지 측정:** 추천 이유와 근거가 일치한 비율 RAG 켬 **80%** / 끔 **13%**
- **규칙 대신 LLM:** 지저분한 영상 제목에서 곡명·가수 추출, 규칙 기반 4/28 → Bedrock tool use **28/28**
- **실제 데이터로 오류 줄이기:** 실제 청취 기록 기준 처리 오류 31 → **0건**, 원곡 확인 비율 32.0% → **52.2%**
- **실패에 강한 비동기 처리:** 단계별 SQS 큐 + 실패 큐(DLQ)로 외부 API 실패 격리·재처리

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot%204-6DB33F?style=flat&logo=springboot&logoColor=white)
![pgvector](https://img.shields.io/badge/PostgreSQL%20pgvector-4169E1?style=flat&logo=postgresql&logoColor=white)
![Amazon SQS](https://img.shields.io/badge/Amazon%20SQS-FF4F8B?style=flat&logo=amazonsqs&logoColor=white)
![Bedrock](https://img.shields.io/badge/Bedrock%20Claude-232F3E?style=flat&logo=amazonwebservices&logoColor=white)

<br/>

### 🧭 [Next Step](https://github.com/SANGWOO-JOO/next-step) · [서비스 바로가기](https://nextstep-plan.work)
> 공백 말고, 준비 기간. 이직 준비 기간을 계획하고, 실제로 쓴 시간을 기록하고, 매주 회고하는 서비스

`✅ 운영 중 · v0.1.2 · 기획부터 배포·운영까지 1인 개발`

**핵심 기능**
- 최종·월간·주간 목표와 하루 계획을 세우고, 실제로 쓴 시간을 시간 블록·집중 세션으로 기록
- 대시보드에서 **계획 대비 실제 시간**을 목표별로 비교하고, 주간 일지로 회고
- 주간 기록을 바탕으로 **AI가 회고 피드백**을 작성 (Google 로그인 기반 다중 사용자)

**설계 결정**
- **LLM에 맡길 범위:** 숫자를 LLM이 계산하면 틀릴 수 있어 집계·지표는 코드로 계산하고, Claude Haiku는 그 결과의 해석만 맡김
- **LLM 호출 비용·품질 관리:** 일지와 1시간 이상의 기록이 있을 때만 호출하고 하루 1번·주 3번으로 제한. 외부 전송 전 동의를 받고 설정에서 끌 수 있게 함
- **키 없는 배포:** 장기 AWS 키를 저장하지 않도록 태그 push → GitHub Actions(OIDC) → S3·CloudFront(프론트), SSM(백엔드)으로 배포

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot%203.5-6DB33F?style=flat&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Claude](https://img.shields.io/badge/Claude%20Haiku-D97757?style=flat&logo=anthropic&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
