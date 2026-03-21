# Research Report: AI Coding Productivity & Palantir FDE Case Studies
**Generated:** 2026-03-15
**Agent:** Researcher (claude-sonnet-4-6)
**Scope:** Subtopic 1 (AI 코딩 툴 생산성) + Subtopic 2 (Palantir FDE/AIP)

---

## SUBTOPIC 1: SI/IT서비스 AI 코딩 툴 도입 후 생산성 변화 사례

---

### FINDING ST1-001

**Claim:** Accenture RCT 연구: GitHub Copilot 도입 후 빌드 성공률 84% 증가, PR 병합률 15% 상승, PR 건수 8.69% 증가

**Source:**
- Author: GitHub Research Team & Accenture
- Title: "Research: Quantifying GitHub Copilot's impact in the enterprise with Accenture"
- Publisher: GitHub Blog (github.blog)
- Date: May 13, 2024
- URL: https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/

**Quality Rating:** B (기업 내 RCT, 대규모 표본, 동료 검토 수준이지만 벤더 주도 연구)

**Verification Status:** Confirmed (복수 2차 소스에서 동일 수치 인용됨)

**Key Statistics:**
- 84% increase in successful builds
- 15% increase in pull request merge rate
- 8.69% increase in pull requests per developer
- 67% of participants used Copilot at least 5 days/week
- 96% success rate among initial installers (81.4% installed same day)
- 30% code suggestion acceptance rate
- 88% of generated code characters retained in editor
- 90% reported greater job fulfillment; 95% enjoyed coding more

**Methodology:**
- Study type: Randomized Controlled Trial (RCT) + company-wide adoption analysis
- Sample: Accenture developers (entry-level to management), various roles
- Data: DevOps telemetry, surveys, GitHub/Azure DevOps APIs
- Note: specific sample size not publicly disclosed

**Context:**
- Vendor-sponsored study (GitHub/Microsoft)이므로 편향 가능성 존재
- 빌드 성공률 84% 증가는 코드 품질 개선을 시사하나, 절대적 결함 수 감소와는 구별 필요
- Copilot 사용자는 도입 전부터 상대적으로 활발한 개발자였을 가능성 (선택 편향)

**Slide Placement Suggestion:** 슬라이드 "AI 코딩 툴 도입 효과 - 엔터프라이즈 실증 데이터" (대표 RCT 사례로 활용)

---

### FINDING ST1-002

**Claim:** Faros AI 연구 (10,000+ 개발자, 1,255팀): 개인 수준에서는 태스크 완료 21% 증가, PR 98% 증가지만, 기업(조직) 수준에서는 DORA 메트릭/처리량/품질 KPI에 유의미한 상관관계 없음 — "AI 생산성 역설"

**Source:**
- Author: Faros AI Research Team
- Title: "The AI Productivity Paradox Research Report"
- Publisher: Faros AI (faros.ai)
- Date: July 23, 2025
- URL: https://www.faros.ai/blog/ai-software-engineering

**Quality Rating:** B (대규모 텔레메트리 데이터 기반, 방법론 공개, 독립 연구기관)

**Verification Status:** Confirmed (METR 연구 등 복수 독립 연구에서 유사 결론)

**Key Statistics:**
- 10,000+ developers, 1,255 teams, up to 2 years of data
- High-AI-adoption teams: 21% more tasks completed, 98% more PRs merged
- BUT: PR review time increases 91%, PR size increases 154%, bugs per developer +9%
- Company-level: no significant correlation with DORA metrics, throughput, or quality KPIs
- Adoption pattern: highest usage among newer employees; senior engineers resist
- Most developers use only autocomplete; advanced features "largely untapped"

**Methodology:**
- Telemetry from task management, IDEs, static analysis, CI/CD, VCS, incident management, HR systems
- Spearman rank correlation analysis
- Reported metrics from ≥6 companies with p-value < 0.05

**Context:**
- 개인 생산성 ≠ 조직 생산성: AI가 개인 코딩 속도를 높여도, 리뷰·QA·배포 병목이 기업 수준 개선을 흡수
- Amdahl의 법칙 적용: 전체 파이프라인을 혁신하지 않으면 한 단계 가속의 효과가 희석
- "AI 생산성 역설"은 발표에서 균형 잡힌 시각 제공에 활용 가능

**Slide Placement Suggestion:** 슬라이드 "AI 도입의 역설 - 왜 조직 수준 성과는 다른가" (비판적 관점 균형 자료)

---

### FINDING ST1-003

**Claim:** METR 독립 RCT: 숙련 오픈소스 개발자 16명 대상, AI 툴 사용 시 태스크 완료 시간 19% 더 걸림 (AI 없을 때보다 느림). 그러나 개발자들은 주관적으로 20% 빠르다고 인식.

**Source:**
- Author: METR (Model Evaluation & Threat Research)
- Title: "Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity"
- Publisher: METR Blog / arXiv:2507.09089
- Date: July 10, 2025 (arXiv submission)
- URL: https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/

**Quality Rating:** A (독립 비영리기관, peer-reviewed, arXiv 게재, 사전 등록 RCT)

**Verification Status:** Confirmed (arXiv 논문 및 복수 기술 미디어에서 교차 확인)

**Key Statistics:**
- 16 experienced developers (평균 5년 이상 해당 프로젝트 경험)
- 246 tasks completed (평균 약 2시간/task)
- Repositories: 22k+ stars, 1M+ lines of code
- AI tools: Cursor Pro + Claude 3.5/3.7 Sonnet (당시 frontier)
- Result: AI 허용 시 19% 더 오래 걸림 (실제 기록 기준)
- Perception gap: 도입 전 24% 빠를 것으로 예상, 도입 후에도 20% 빨라진 것으로 느낌 (실제와 반대)
- AI suggestion acceptance rate: < 44%

**Methodology:**
- Randomized crossover design (각 태스크를 AI 사용/미사용 조건에 무작위 배정)
- Self-reported implementation times + session recordings

**Context:**
- 중요한 한계: 숙련 개발자 + 대규모 성숙 코드베이스에 한정된 결과
- 신규 개발자나 그린필드(새 코드베이스) 환경에서는 결과가 다를 수 있음
- 50시간 이상 사용 후 학습 효과는 미측정
- AI가 복잡하고 성숙한 레거시 코드베이스에서 가장 낮은 효과를 보임

**Slide Placement Suggestion:** 슬라이드 "주의사항 - AI 코딩 툴의 한계" 또는 "숙련도별 차별화 적용 전략" (ST1-002와 함께 균형 시각 제공)

---

### FINDING ST1-004

**Claim:** GitHub Copilot 사용자, 특정 작업에서 51% 더 빠른 코딩 속도. 개발자의 81%가 태스크를 더 빠르게 완료한다고 응답.

**Source:**
- Author: GitHub Research Team
- Title: "Research: quantifying GitHub Copilot's impact on developer productivity and happiness"
- Publisher: GitHub Blog
- Date: September 7, 2022 (원본; 이후 기업 연구들로 계속 인용됨)
- URL: https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-on-developer-productivity-and-happiness/

**Quality Rating:** C (벤더 주도 초기 연구, 통제된 실험 환경, 실제 복잡한 업무 환경과 차이 가능)

**Verification Status:** Partially Confirmed (벤더 수치는 독립 연구에서 자주 과대평가됨이 지적됨)

**Key Statistics:**
- 55% faster task completion in controlled experiment (완전한 코딩 태스크 기준)
- 81% of users say they help complete tasks faster
- 126% more projects per week (일부 소스에서 인용; 방법론 불명확)

**Context:**
- GitHub(Microsoft) 자체 연구로 이해충돌 존재
- 통제 실험은 실제 기업 환경(레거시 코드베이스, 팀 협업)을 반영하지 않을 수 있음
- NAV IT 종단연구(ST1-005)에서 통계적으로 유의미한 활동 증가 없음

**Slide Placement Suggestion:** 슬라이드 "AI 코딩 툴 도입 효과 - 개인 수준 작업 가속" (벤더 데이터임을 명시하며 활용)

---

### FINDING ST1-005

**Claim:** NAV IT(노르웨이 공공기관) 2년 종단 연구(703개 repo, 26,317 커밋): Copilot 사용자와 비사용자 간 커밋 활동의 통계적 유의미한 차이 없음. Copilot 사용자는 도입 전부터 이미 더 활발했음(선택 편향).

**Source:**
- Author: NAV IT / Norwegian Labor and Welfare Administration research team
- Title: "Developer Productivity With and Without GitHub Copilot: A Longitudinal Mixed-Methods Case Study"
- Publisher: arXiv (2509.20353); 발표 예정: HICSS-59 (2026)
- Date: September 24, 2025 (submission); January 28, 2026 (revised)
- URL: https://arxiv.org/abs/2509.20353

**Quality Rating:** A (peer-reviewed, 독립 기관, 종단 설계)

**Verification Status:** Confirmed

**Key Statistics:**
- 26,317 unique non-merge commits analyzed
- 703 GitHub repositories
- 25 Copilot users vs 14 non-users
- 13 interviews conducted
- No statistically significant change in commit-based activity after Copilot adoption
- Pre-existing gap: Copilot adopters were already more active before adoption

**Context:**
- 객관적 지표와 주관적 인식의 괴리: 개발자들은 생산성이 향상됐다고 느끼지만 커밋 수는 증가 안 함
- "체감 생산성"의 원천은 반복 작업 감소, 정신적 부담 완화일 가능성
- SI 기업 발표 시 "효율 체감 ≠ 산출량 증가"를 구별해 설명하는 근거로 활용 가능

**Slide Placement Suggestion:** 슬라이드 "AI 코딩 툴 - 올바른 측정 방법론" (기업이 어떤 지표를 봐야 하는지 논의)

---

### FINDING ST1-006

**Claim:** Microsoft CEO Satya Nadella 공개 발언(2025년 4월): Microsoft 내부적으로 AI가 전체 코드의 약 30%를 작성. "AI가 쓰는 코드 비중이 단조 증가 중."

**Source:**
- Author: Satya Nadella (인터뷰 발언)
- Title: "Satya Nadella says as much as 30% of Microsoft code is written by AI"
- Publisher: CNBC
- Date: April 29, 2025
- URL: https://www.cnbc.com/2025/04/29/satya-nadella-says-as-much-as-30percent-of-microsoft-code-is-written-by-ai.html

**Quality Rating:** B (CEO 직접 발언, 내부 데이터 인용; 독립 검증 불가)

**Verification Status:** Confirmed (여러 기술 미디어에서 동일 발언 보도)

**Key Statistics:**
- ~30% of Microsoft code now generated by AI
- "Going up monotonically" (꾸준히 증가 중)
- AI acceptance rates tracked internally: "30-40%"
- AI performs best on new code (Python: "fantastic"); less effective on legacy (C++: "not that great")

**Context:**
- 내부 지표를 공개한 희귀한 사례 (검증 불가하나 신뢰도 높음)
- Python 신규 코드 vs C++ 레거시 코드의 효과 차이는 SI 기업에 시사점 있음

**Slide Placement Suggestion:** 슬라이드 "산업 리더의 AI 코딩 도입 현황" (빅테크 내부 데이터 사례)

---

### FINDING ST1-007

**Claim:** Google 내부 RCT(~100명 엔지니어): AI 코딩 툴 사용 시 태스크 완료 21% 빠름 (AI 사용: 평균 96분 vs 미사용: 114분)

**Source:**
- Author: Google Research (LinearB Blog 인용)
- Title: "Gen AI Research: Software Development Productivity At Google"
- Publisher: LinearB Blog (분석 기사)
- Date: 2025 (원본 Google 연구 날짜 불명확)
- URL: https://linearb.io/blog/gen-AI-research-software-development-productivity-at-google

**Quality Rating:** C (Google 내부 연구, 원본 논문 미공개, 2차 보도 출처)

**Verification Status:** Partially Confirmed (2차 인용이며 원본 Google 보고서 직접 접근 불가)

**Key Statistics:**
- ~100 Google software engineers in RCT
- AI tools tested: AI Code Completion, Smart Paste, Natural Language to Code
- AI group: 96 min average task completion
- Control group: 114 min average task completion
- Result: 21% faster with AI

**Context:**
- 내부 연구로 세부 방법론 비공개
- Google 자체 AI 툴(Gemini 기반) 대상으로 제3자 툴과 다를 수 있음
- METR 연구(숙련자 대상 19% 느려짐)와 상충 - 개발자 경험 수준 및 코드베이스 성숙도 차이가 결정적 변수

**Slide Placement Suggestion:** 슬라이드 "AI 코딩 툴 도입 효과 - 빅테크 내부 실험 결과"

---

### FINDING ST1-008

**Claim:** 2025 Stack Overflow 개발자 설문(글로벌): 84%가 AI 툴 사용 또는 계획. 그러나 신뢰도는 하락 - 46%가 AI 정확성 불신, 긍정 감정은 2023/24년 70%+에서 2025년 60%로 하락.

**Source:**
- Author: Stack Overflow
- Title: "2025 Stack Overflow Developer Survey"
- Publisher: Stack Overflow (survey.stackoverflow.co)
- Date: December 2025 (결과 공개)
- URL: https://survey.stackoverflow.co/2025/ai/

**Quality Rating:** B (대규모 연례 설문, 방법론 공개; 자기보고 편향 존재)

**Verification Status:** Confirmed

**Key Statistics:**
- 84% use or plan to use AI tools (up from 76% in 2024)
- 51% of professional developers use AI tools daily
- 52% agree AI tools positively affected productivity
- Positive sentiment: 60% in 2025 (vs 70%+ in 2023/2024)
- Trust: only 3.1% "highly trust" AI output; 19.6% "highly distrust"
- 46% actively distrust AI accuracy
- Top frustration: 66% cite "almost right, but not quite" solutions
- 45.2% say debugging AI-generated code is time-consuming
- 76% won't use AI for deployment/monitoring
- AI agents: 23% use regularly; 87% concerned about accuracy

**Context:**
- 신뢰도 하락이 채택률 상승과 동시에 발생 — "불신하며 사용"하는 패턴
- 고위험 영역(배포, 모니터링)에서의 저항감은 SI 기업 리스크 관리 논의에 활용 가능

**Slide Placement Suggestion:** 슬라이드 "개발자 AI 툴 인식 현황 2025" (업계 현황 배경 자료)

---

### FINDING ST1-009

**Claim:** McKinsey 2025 조사(600개 이상 기관): AI 채택 기관의 60%+가 최소 25% 생산성 향상 경험. 개발자 채택률 80-100% 기업은 110%+ 생산성 향상.

**Source:**
- Author: McKinsey & Company
- Title: "The state of AI in 2025: Agents, innovation, and transformation"
- Publisher: McKinsey (mckinsey.com)
- Date: 2025
- URL: https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai

**Quality Rating:** B (대규모 기업 설문, 글로벌 커버리지; 자기보고 방식)

**Verification Status:** Partially Confirmed (특정 수치는 2차 인용으로 원문 직접 검증 필요)

**Key Statistics:**
- 60%+ of organizations see at least 25% productivity improvement from AI
- Companies with 80-100% developer adoption: 110%+ productivity gains
- Top performers: 16-30% improvement in team productivity, time to market; 31-45% in software quality
- 88% of organizations use AI in at least one business function (up from 78%)
- ~2/3 still in "experiment or pilot" mode

**Context:**
- 자기보고(self-reported) 설문으로 실제 측정값과 차이 있을 수 있음
- 채택률 80-100% 달성 자체가 이미 선도 기업 특성 (역인과 가능성)
- 발표용: "적극적 도입 시 성과가 다름" 논거로 활용 유효

**Slide Placement Suggestion:** 슬라이드 "AI 도입 성숙도와 생산성 - McKinsey 데이터"

---

### FINDING ST1-010

**Claim:** Walgreens: Palantir AIP로 4,000개 매장에 AI 워크플로우 배포, 매장당 30% 업무 시간 절감, 384B 일일 수동 의사결정 자동화. 8개월 내 완전 배포.

**Source:**
- Author: PYMNTS Staff
- Title: "Palantir Reinvents Wendy's Supply Chain Network, Walgreens' Operations"
- Publisher: PYMNTS.com
- Date: 2025
- URL: https://www.pymnts.com/news/artificial-intelligence/2025/palantir-reinvents-wendys-supply-chain-network-walgreens-operations/

**Quality Rating:** C (기술 미디어 보도; 원본 데이터는 Palantir 발표 기반)

**Verification Status:** Partially Confirmed (Palantir 공식 발표에서 수치 유래; 독립 검증 없음)

**Key Statistics:**
- Pilot: 10 stores over 6 months → Full: 4,000 stores in 8 months (45일 내 digital twin 완성)
- 30% reduction in time spent on tasks
- 384 billion daily manual decisions automated
- Serves 9M customers/day, 8,500 US locations, 220,000 employees
- System tracks pharmacy task inflow/outflow in 15-minute intervals

**Context:**
- SI 관점에서 주목할 점: "10개 파일럿 → 4,000개 전사 배포를 8개월 내 달성"한 확장성
- 30% 시간 절감은 약사/기술자 업무 배분 최적화를 통한 것 (전체 인력 비용 절감 아님)

**Slide Placement Suggestion:** 슬라이드 "Palantir AIP - 대규모 리테일 배포 사례" 또는 "엔터프라이즈 AI 확장성 벤치마크"

---

### FINDING ST1-011

**Claim:** Wendy's: Palantir AIP 디지털 트윈으로 네트워크 전체 음료 부족 문제를 15명이 하루 걸려 해결하던 것을 5분 내 해결. 10,200 케이스 부족분 중 8,300 케이스 즉시 위치 파악.

**Source:**
- Author: PYMNTS Staff
- Title: "Palantir Reinvents Wendy's Supply Chain Network, Walgreens' Operations"
- Publisher: PYMNTS.com
- Date: 2025
- URL: https://www.pymnts.com/news/artificial-intelligence/2025/palantir-reinvents-wendys-supply-chain-network-walgreens-operations/

**Quality Rating:** C (기술 미디어; 원본은 Palantir 발표 기반)

**Verification Status:** Partially Confirmed

**Key Statistics:**
- Before: 15 people, 1 full day to manage supply chain shortage
- After: 5 minutes to identify and resolve
- Network scope: 3,500 transport units, 60 partners, 250+ shipping points, 34 DCs, 6,450 restaurants
- Prior inventory model: $370 million tied up across network
- System recommended exact reorder quantity (3,500 cases) with source locations

**Context:**
- "의사결정 지원"에서 "의사결정 자동화"로의 전환을 보여주는 사례
- 물류·SCM 담당 SI 기업에 특히 관련성 높음

**Slide Placement Suggestion:** 슬라이드 "Palantir AI - Supply Chain 실시간 의사결정 사례"

---

## SUBTOPIC 2: Palantir AI FDE 최신 사례 연구

---

### FINDING ST2-001 [핵심 인용문]

**Claim:** Palantir Q3 2025 실적 발표 (Shyam Sankar CTO 직접 발언): "두 명의 FDE가 AIFDE 군단을 동원해 고객의 레거시 데이터 웨어하우스를 5일 만에 마이그레이션했다. 이는 SI 군단도 최대 2년이 걸렸을 작업이다." (원문: "two human FTEs spawned an army of AI FTEs to migrate a customer off their legacy data warehouse in five days, something that would have taken an army of SIs up to two years.")

**Source:**
- Author: Shyam Sankar (Palantir CTO)
- Title: "Palantir (PLTR) Q3 2025 Earnings Call Transcript"
- Publisher: The Motley Fool (earnings call transcript)
- Date: November 3-4, 2025
- URL: https://www.fool.com/earnings/call-transcripts/2025/11/04/palantir-pltr-q3-2025-earnings-call-transcript/

**Quality Rating:** B (C-level 임원의 공개 실적 발표 발언; SEC 규제 환경하에서 허위 진술 리스크 낮음. 그러나 독립 검증 없음)

**Verification Status:** Confirmed (복수 금융 보도, 분석 기사에서 동일 인용 확인)

**Key Statistics:**
- 2 human FDEs + AIFDE agents = 5 days
- Traditional approach: "army of SIs" + up to 2 years
- Context: Headcount grew ~10% while revenue grew 63% (AIFDE가 내부 생산성 향상의 핵심)
- 발표: "not a prototype—this is production"

**Context:**
- SI 산업에 직접적 위협 시사: SI의 멀티이어 마이그레이션 프로젝트가 AI에 의해 며칠로 압축
- 고객명 비공개; 익명 처리됨
- Q4 2025 실적에서도 "AI FDE replaced multi-year projects with five-day implementations"로 재확인

**Slide Placement Suggestion:** 슬라이드 "Palantir AIFDE - SI를 대체하는 AI 에이전트" (발표의 핵심 메시지로 활용 가능한 최강 슬라이드)

---

### FINDING ST2-002

**Claim:** Palantir AI FDE(제품): Foundry를 자연어로 조작하는 대화형 AI 에이전트. 2025년 11월 베타 출시. 데이터 파이프라인, 온톨로지, 코드 레포, 앱 빌딩을 자연어 명령으로 수행.

**Source:**
- Author: Palantir Technologies (공식 문서)
- Title: "AI FDE - Overview"
- Publisher: Palantir Documentation (palantir.com)
- Date: November 2025 (베타 출시)
- URL: https://www.palantir.com/docs/foundry/ai-fde/overview

**Quality Rating:** B (공식 제품 문서; 마케팅 편향 가능)

**Verification Status:** Confirmed (Palantir November 2025 Announcements 페이지에서 교차 확인)

**Key Capabilities:**
- Python transforms 및 Pipeline Builder로 데이터 통합
- Object types, link types, action types, interfaces 온톨로지 구축
- React 앱 및 커스텀 위젯 빌딩 (OSDK React)
- 권한, 접근 제어, 마킹 감사
- Anthropic, OpenAI, Google, xAI 모델 지원

**Context:**
- AIP 활성화 enrollment에 한정 (모든 Foundry 고객이 아님)
- Foundry Branching 권장 (온톨로지 변경 시 PR 방식으로 제안, 직접 반영 아님)
- "Closed-loop" 실행: 실행 → 결과 관찰 → 다음 단계 반영

**Slide Placement Suggestion:** 슬라이드 "Palantir AI FDE - 제품 아키텍처 소개"

---

### FINDING ST2-003

**Claim:** Palantir AIP Bootcamp: 고객이 0에서 AI 유즈케이스까지 5일 내 구현. 전환율 약 75%. 이전에는 거의 1년이 걸리던 영업 사이클을 5일로 압축.

**Source:**
- Author: MarketMinute / Financial Content
- Title: "Palantir Shares Surge as 'AIP Bootcamp' Strategy Cementing Dominance in Enterprise AI"
- Publisher: markets.financialcontent.com
- Date: March 6, 2026
- URL: https://markets.financialcontent.com/stocks/article/marketminute-2026-3-6-palantir-shares-surge-as-aip-bootcamp-strategy-cementing-dominance-in-enterprise-ai

**Quality Rating:** C (금융 분석 기사; 원본 데이터는 Palantir 보고서 기반)

**Verification Status:** Confirmed (복수 투자 분석 보고서에서 동일 수치 인용)

**Key Statistics:**
- ~75% conversion rate from bootcamp to contract
- Sales cycle: ~1 year → 5 days (5개월 사이클을 5일 스프린트로)
- US commercial revenue: +137% Y/Y (Q4 2025)
- Fortune 500 industrial company: 5x expansion from initial engagement
- Fortune 100 retailer: pilot → $12M ACV within months
- Walgreens: AI workflows to 4,000 stores in 8 months

**Context:**
- Bootcamp은 판매 전술이자 고객 교육 프로그램: 5일 동안 고객 데이터로 실제 유즈케이스 구현
- SI 기업에 시사: 긴 컨설팅 프로젝트보다 단기 고강도 "PoC → 즉각 확장" 모델의 경쟁 압박

**Slide Placement Suggestion:** 슬라이드 "Palantir AIP Bootcamp - 판매/배포 혁신 모델"

---

### FINDING ST2-004

**Claim:** Palantir Q3 2025 재무 결과: 미국 상업 매출 121% Y/Y 성장. 총 계약 가치(TCV) $2.8B (151% Y/Y). 순 달러 유지율(NDR) 134%. 고객 수 45% Y/Y 증가.

**Source:**
- Author: Palantir Technologies (공식 보도자료)
- Title: "Palantir Reports Q3 2025 U.S. Comm Revenue Growth of 121% Y/Y and Revenue Growth of 63% Y/Y"
- Publisher: Palantir IR (investors.palantir.com)
- Date: November 3, 2025
- URL: https://investors.palantir.com/news-details/2025/Palantir-Reports-Q3-2025-U-S--Comm-Revenue-Growth-of-121-YY-and-Revenue-Growth-of-63-YY-Guides-Q4-Revenue-to-61-YY-and-U-S--Comm-Revenue-to-121-YY-Raises-FY-2025-Revenue-Guidance-to-53-YY-Crushing-Consensus-Expectations/

**Quality Rating:** A (SEC 규제 기업 공식 보도자료)

**Verification Status:** Confirmed

**Key Statistics:**
- Q3 2025 Revenue: $1.181B (+63% Y/Y, +18% Q/Q)
- US Commercial Revenue: +121% Y/Y, +29% Q/Q
- TCV bookings: $2.8B (+151% Y/Y) — "highest-ever quarter"
- NDR: 134% (+600 bps Q/Q)
- Customer count: +45% Y/Y (commercial: +49%)
- Deals >$1M: 204; Deals >$10M: 53
- Medical device manufacturer: ACV increased 8x in 5 months after initial contract

**Context:**
- AIP 중심 성장의 직접적 증거
- NDR 134%는 기존 고객이 연간 34% 더 지출함을 의미 (확장 판매 강도)

**Slide Placement Suggestion:** 슬라이드 "Palantir AIP 성장 지표 - 2025 결산"

---

### FINDING ST2-005

**Claim:** Palantir Q4 2025 재무 결과: 미국 상업 매출 137% Y/Y. 전체 매출 70% Y/Y (공개기업 이후 최고 성장률). Rule of 40: 127. FY2026 가이던스: +61% Y/Y ($7.19B).

**Source:**
- Author: Palantir Technologies
- Title: "Palantir Reports Q4 2025 U.S. Comm Revenue Growth of 137% Y/Y and Revenue Growth of 70% Y/Y"
- Publisher: BusinessWire / Palantir IR
- Date: February 1, 2026
- URL: https://www.businesswire.com/news/home/20260201154946/en/Palantir-Reports-Q4-2025-U.S.-Comm-Revenue-Growth-of-137-YY-and-Revenue-Growth-of-70-YY-Issues-FY-2026-Revenue-Guidance-of-61-YY-and-U.S.-Comm-Revenue-Guidance-of-115-YY-Crushing-Consensus-Expectations/

**Quality Rating:** A (SEC 규제 공식 보도자료)

**Verification Status:** Confirmed

**Key Statistics:**
- Q4 2025 Revenue: $1.41B (+70% Y/Y) — highest growth rate as public company
- US Commercial Revenue: $507M (+137% Y/Y)
- US Business overall: +93% Y/Y, +22% Q/Q
- TCV bookings (Q4): $4.3B (highest-ever)
- Rule of 40: 127 (+46 pts Y/Y)
- Deals >$10M: 61 (Q4)
- FY2026 guidance: $7.19B (+61% Y/Y)
- US Commercial FY2026 guidance: +115% Y/Y
- Utility company: $7M ACV (Q1 2025) → $31M ACV (year-end 2025)
- Energy company: $4M ACV → $20M+ ACV within 2025

**Context:**
- Johnson Controls 인용: "140년 된 기업이 AI로 변혁되는 것을 보는 것은 정말 놀랍습니다"
- Thomas Kavanaugh Construction: "97%의 직원이 매일 Foundry 사용; 다른 모든 소프트웨어가 존재를 정당화해야 함"

**Slide Placement Suggestion:** 슬라이드 "Palantir - 엔터프라이즈 AI 시장 성장의 증거"

---

### FINDING ST2-006

**Claim:** AIPCon 9 (2026년 3월 12일): Centrus Energy, Palantir AIP로 우라늄 농축 시설 확장에 약 $3억 달러 비용 절감 및 효율화 기회 식별.

**Source:**
- Author: Palantir Technologies
- Title: "Palantir's Newest Customers Reveal the Secrets Behind Their Success at AIPCon 9"
- Publisher: BusinessWire
- Date: March 12, 2026
- URL: https://www.businesswire.com/news/home/20260312975769/en/Palantirs-Newest-Customers-Reveal-the-Secrets-Behind-Their-Success-at-AIPCon-9

**Quality Rating:** C (기업 PR 보도자료; 독립 검증 없음)

**Verification Status:** Partially Confirmed (금융 뉴스에서 동일 수치 인용됨)

**Key Statistics:**
- Centrus Energy: nearly $300M in potential cost savings and efficiencies identified
- Presenting customers: U.S. Dept. of Navy, World View, Moder, SAP, Accenture, GE Aerospace, Joint Commission, Centrus Energy, CDAO
- Key use cases: AI-driven naval fleet readiness (ShipOS), aerospace manufacturing, nuclear energy, mortgage/financial services, SAP enterprise modernization

**Context:**
- "Potential" 절감은 실현된 절감이 아님 — 과대평가 리스크
- SAP+Accenture+Palantir 협력: "SAP 여정에 AI를 추가하는 것이 아니라, SAP 여정 자체를 바꾸는 것"
- Rackspace 파트너십 (발표: 2026년 2월 18일): AI 배포 기간을 "months or years → weeks"로 단축, 30명 Palantir 엔지니어 → 12개월 내 250명 확대 계획

**Slide Placement Suggestion:** 슬라이드 "AIPCon 9 - Palantir 최신 고객 사례 (2026년 3월)"

---

### FINDING ST2-007

**Claim:** GE Aerospace + Palantir 파트너십 확대 (2026년 3월): AIP로 미군 항공기 준비태세 혁신. T-38 제트 파일럿 프로그램(2024 초)에서 전체 생산 시스템(부품 수급, MRO, 신규 엔진 생산)으로 확장.

**Source:**
- Author: ASD News
- Title: "GE Aerospace and Palantir Expand Partnership to Transform Military Aircraft Readiness with AI"
- Publisher: ASD News (asdnews.com)
- Date: March 12, 2026
- URL: https://www.asdnews.com/news/defense/2026/03/12/ge-aerospace-palantir-expand-partnership-transform-military-aircraft-readiness-with-ai

**Quality Rating:** C (언론 보도; 계량 결과 미공개)

**Verification Status:** Partially Confirmed

**Key Statistics:**
- Scale: "A GE Aerospace engine takes off somewhere in the world every 2 seconds"
- AI covers: fulfillment, sourcing, allocation, maintenance, repair, customer service
- Pilot: J85 engine sustainment (early 2024) → Full production system
- No specific quantified before/after results disclosed

**Context:**
- 방산 AI 배포의 최신 사례지만 구체적 성과 지표 미공개
- 미국 공군의 "TrueChoice Defense" 디지털 에코시스템 일부

**Slide Placement Suggestion:** 슬라이드 "Palantir - 방산/항공우주 AI 에이전트 배포"

---

### FINDING ST2-008

**Claim:** Palantir AIP 데이터 마이그레이션 가속: Rackspace 협업 초기 결과 — 2주 내 99%+ 검증 정확도, 70%+ 타임라인/비용 절감, 전문가 투입 2/3 감소.

**Source:**
- Author: vktr.com staff
- Title: "Palantir & Rackspace Partner to Cut AI Deployment Timelines to Weeks"
- Publisher: vktr.com
- Date: 2026
- URL: https://www.vktr.com/ai-news/palantir-rackspace-team-up-to-fast-track-governed-ai-rollouts/

**Quality Rating:** D (기술 뉴스 블로그; 원본 Palantir/Rackspace 보도자료 2차 인용)

**Verification Status:** Unverified (독립 고객 검증 없음; Palantir-Rackspace 마케팅 자료 기반)

**Key Statistics:**
- >99% validation accuracy within 2 weeks
- >70% timeline and cost reduction for migration
- 2/3 reduction in expert involvement
- One Fortune 500 company: discovery sprint → validated plan → executed in <4 months
- Another customer: ~5 migrations/2 weeks → dozens/week

**Context:**
- Rackspace 파트너십 발표 (2026년 2월 18일)는 초기 단계
- 위 수치들은 초기 pilot 결과로 대규모 배포 시 재현 여부 불확실

**Slide Placement Suggestion:** 슬라이드 "Palantir AIP - 데이터 마이그레이션 가속 사례" (주의: 출처 등급 D로 스타 슬라이드 활용 시 검증 강화 필요)

---

### FINDING ST2-009

**Claim:** Nebraska Medicine + Palantir: 의료 필요성 검증(의료비 청구) 가이드라인 평가 워크플로우를 단 10시간 만에 구축. (AIPCon 8, 2025년 9월 4일 발표)

**Source:**
- Author: Palantir Technologies
- Title: "A New Set of Palantir Customers Takes the Spotlight at AIPCon 8"
- Publisher: BusinessWire / Palantir IR
- Date: September 4, 2025
- URL: https://investors.palantir.com/news-details/2025/A-New-Set-of-Palantir-Customers-Takes-the-Spotlight-at-AIPCon-8/

**Quality Rating:** C (기업 PR 발표; 독립 검증 없음)

**Verification Status:** Partially Confirmed

**Key Statistics:**
- Guideline Evaluation workflow built in just 10 hours
- Use case: intelligent automation for medical necessity validation and reimbursement optimization
- Presenter: Jana Danielson, VP of Revenue Cycle Management, Nebraska Medicine

**Context:**
- 10시간 빌드는 AIP Bootcamp 모델의 스피드를 잘 보여주는 사례
- 의료비 청구 최적화라는 구체적 비즈니스 가치와 연결
- AIPCon 8: 70+ speakers from US commercial customer base

**Slide Placement Suggestion:** 슬라이드 "AIPCon 8 - 의료 부문 AI 배포 사례 (10시간 PoC → Production)"

---

## 요약 및 슬라이드 활용 가이드

### AI 코딩 툴 (Subtopic 1) 핵심 포인트:

| 연구 | 결과 | 품질 | 활용 |
|------|------|------|------|
| Accenture RCT (GitHub) | 빌드 성공 +84%, PR 병합 +15% | B | 긍정 사례 대표 |
| METR RCT | 숙련 개발자 19% 느려짐 | A | 주의사항/균형 |
| Faros AI 10K+ devs | 개인 ↑ but 기업 수준 변화 없음 | B | AI 역설 논거 |
| NAV IT 종단 | 커밋 변화 통계적 유의성 없음 | A | 측정 방법론 |
| Stack Overflow 2025 | 신뢰도 하락(60%), 채택은 84% | B | 업계 현황 |
| McKinsey 2025 | 도입 조직의 60%+는 25%+ 향상 | B | 전략적 프레임 |
| Microsoft (Nadella) | 내부 코드의 30% AI 작성 | B | 빅테크 벤치마크 |

**핵심 메시지:** AI 코딩 툴은 개인 수준의 생산성(특히 신규 코드, 보일러플레이트)은 향상시키지만, 조직 수준의 성과로 자동 전환되지 않는다. 성공 조건: 리뷰·QA·배포 파이프라인의 동시 혁신 필요.

### Palantir FDE/AIP (Subtopic 2) 핵심 포인트:

| 사례 | 결과 | 품질 | 활용 |
|------|------|------|------|
| AIFDE 레거시 마이그레이션 | 2년 → 5일 (2 FDE 투입) | B | 핵심 슬라이드 |
| AIP Bootcamp | ~75% 전환율, 영업 1년 → 5일 | C | 비즈니스 모델 |
| Walgreens 4000개 매장 | 30% 업무 시간 절감, 8개월 배포 | C | 대규모 확장 사례 |
| Wendy's SCM | 15명·1일 → 5분 해결 | C | 의사결정 자동화 |
| Nebraska Medicine | 10시간 만에 워크플로우 구축 | C | PoC 속도 |
| Q4 2025 재무 | US 상업 매출 137% Y/Y | A | 성장 신뢰성 |
| Centrus Energy | $3억 절감 기회 식별 | C | 원자력 부문 |

**핵심 메시지:** Palantir의 AIFDE는 SI의 전통적 멀티이어 프로젝트를 수 일로 압축하는 잠재력을 실증했다. FDE(사람) + AIFDE(AI 에이전트)의 결합이 새로운 배포 패러다임을 만들고 있으며, 이는 SI 산업의 비즈니스 모델에 직접적인 위협/기회 요인이다.

---

## 주요 출처 목록

1. GitHub Blog - Accenture RCT: https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/
2. Faros AI Productivity Paradox: https://www.faros.ai/blog/ai-software-engineering
3. METR RCT Study: https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/
4. arXiv METR paper: https://arxiv.org/abs/2507.09089
5. NAV IT Longitudinal Study: https://arxiv.org/abs/2509.20353
6. Stack Overflow 2025 Survey: https://survey.stackoverflow.co/2025/ai/
7. McKinsey State of AI 2025: https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-state-of-ai
8. Microsoft/Nadella CNBC: https://www.cnbc.com/2025/04/29/satya-nadella-says-as-much-as-30percent-of-microsoft-code-is-written-by-ai.html
9. Palantir Q3 2025 Earnings Call Transcript: https://www.fool.com/earnings/call-transcripts/2025/11/04/palantir-pltr-q3-2025-earnings-call-transcript/
10. Palantir Q3 2025 IR: https://investors.palantir.com/news-details/2025/Palantir-Reports-Q3-2025-U-S--Comm-Revenue-Growth-of-121-YY-and-Revenue-Growth-of-63-YY-Guides-Q4-Revenue-to-61-YY-and-U-S--Comm-Revenue-to-121-YY-Raises-FY-2025-Revenue-Guidance-to-53-YY-Crushing-Consensus-Expectations/
11. Palantir Q4 2025 IR: https://www.businesswire.com/news/home/20260201154946/en/Palantir-Reports-Q4-2025-U.S.-Comm-Revenue-Growth-of-137-YY-and-Revenue-Growth-of-70-YY-Issues-FY-2026-Revenue-Guidance-of-61-YY-and-U.S.-Comm-Revenue-Guidance-of-115-YY-Crushing-Consensus-Expectations/
12. AIPCon 9 BusinessWire: https://www.businesswire.com/news/home/20260312975769/en/Palantirs-Newest-Customers-Reveal-the-Secrets-Behind-Their-Success-at-AIPCon-9
13. Palantir AI FDE Docs: https://www.palantir.com/docs/foundry/ai-fde/overview
14. PYMNTS Walgreens/Wendy's: https://www.pymnts.com/news/artificial-intelligence/2025/palantir-reinvents-wendys-supply-chain-network-walgreens-operations/
15. AIPCon 8 BusinessWire: https://investors.palantir.com/news-details/2025/A-New-Set-of-Palantir-Customers-Takes-the-Spotlight-at-AIPCon-8/
16. Palantir Bootcamp FinancialContent: https://markets.financialcontent.com/stocks/article/marketminute-2026-3-6-palantir-shares-surge-as-aip-bootcamp-strategy-cementing-dominance-in-enterprise-ai
17. a16z FDE Analysis: https://a16z.com/the-palantirization-of-everything/
18. Rackspace-Palantir Partnership: https://www.vktr.com/ai-news/palantir-rackspace-team-up-to-fast-track-governed-ai-rollouts/
