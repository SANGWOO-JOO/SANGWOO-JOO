<!-- ===== HEADER ===== -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,16,20&height=180&section=header&text=SANGWOO%20JOO&fontSize=55&fontColor=ffffff&fontAlignY=40&desc=Backend%20Developer&descAlignY=62&descSize=18" />

<div align="center">

### 👋 안녕하세요, 백엔드 개발자 **주상우**입니다.

**AI를 활용해 작업 효율을 극대화**하려고 하고 있습니다.

</div>

<br/>

## 🚀 Side Projects

### 🧭 [Next Step](https://github.com/SANGWOO-JOO/next-step) · [서비스 바로가기](https://nextstep-plan.work)
> 공백 말고, 준비 기간. 이직 준비 기간을 계획하고, 실제로 쓴 시간을 기록하고, 매주 회고하는 서비스

- **혼자 기획부터 운영까지:** Google 로그인 기반 다중 사용자 서비스로 실제 배포(v0.1.2)
- **AI는 해석만 맡김:** 집계·지표는 코드로 계산하고 Claude Haiku는 그 결과를 해석해 주간 피드백만 작성. 기록이 충분할 때만 호출하고 하루 1번·주 3번으로 제한해 비용과 품질을 함께 관리
- **키 없는 배포:** 태그 push → GitHub Actions(OIDC) → S3·CloudFront(프론트), SSM(백엔드)

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot%203.5-6DB33F?style=flat&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Claude](https://img.shields.io/badge/Claude%20Haiku-D97757?style=flat&logo=anthropic&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)

<br/>

### 🎧 [결 gyeol](https://github.com/SANGWOO-JOO/gyeol)
> 유튜브 청취 기록으로 많이 들은 곡·가수와 들은 시기를 분석하고, 근거를 붙여 곡을 추천하는 서비스

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

## 🛠 Tech Stack

| 분야 | 기술 |
|---|---|
| Backend | Java · Kotlin · Spring Boot · JPA |
| Database | MySQL · PostgreSQL(pgvector) · Redis |
| AI | Amazon Bedrock · Claude API · RAG |
| DevOps & Cloud | AWS · Docker · Kubernetes(K3s) · GitHub Actions |
| Monitoring | Prometheus · Grafana |

<!-- ===== FOOTER ===== -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,16,20&height=120&section=footer" />
