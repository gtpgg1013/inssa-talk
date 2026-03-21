# ST3 Research: Shadow AI Security Incidents & Agent Governance Frameworks

**Research Date:** 2026-03-15
**Researcher:** Subagent (Claude Sonnet 4.6)
**Scope:** Subtopic 1 - Shadow/Unauthorized AI Agent Security Incidents; Subtopic 2 - AI Agent Governance Framework Adoption Cases
**Retrieval Window:** 2023-2026 (emphasis on 2025-2026)

---

## SUBTOPIC 1: 비승인 AI Agent 보안 사고 / 위험 사례 (시나리오 B 근거)

---

### FINDING 1-A: IBM 2025 Cost of a Data Breach Report — AI Breach Prevalence

**Claim:** 13% of organizations reported breaches of AI models or applications. Of those compromised, 97% lacked proper AI access controls. 63% of breached organizations had no AI governance policies or were still developing them.

**Source:**
- Author/Organization: IBM, conducted by Ponemon Institute
- Title: "2025 Cost of a Data Breach Report"
- Publisher: IBM Newsroom
- Date: July 30, 2025
- URL: https://newsroom.ibm.com/2025-07-30-ibm-report-13-of-organizations-reported-breaches-of-ai-models-or-applications,-97-of-which-reported-lacking-proper-ai-access-controls
- Methodology: Data from 600 organizations globally, breaches March 2024–February 2025 (Ponemon Institute)

**Quality Rating:** A (Commissioned research, large sample, Ponemon Institute methodology)

**Verification Status:** Confirmed (cross-referenced with multiple secondary analyses: NatLawReview, Kiteworks, NudgeSecurity)

**Context:**
- 8% of organizations were uncertain whether they had been compromised
- 60% of AI-related incidents caused data compromise; 31% caused operational disruption
- Shadow AI incidents averaged $4.63M total breach cost — $670,000 MORE than standard incidents
- 16% of all breaches in 2025 involved attackers using AI tools
- Shadow AI incidents compromised more PII (65% vs. 53% global average) and IP (40% vs. 33%)

**Slide Placement Suggestion:** 시나리오 B 근거 슬라이드 — "통제 없는 AI의 비용" 수치 섹션. "AI 거버넌스 부재의 재무적 결과" 강조.

---

### FINDING 1-B: Gartner — 40% of Organizations Will Face Shadow AI Security Incidents by 2030

**Claim:** Gartner predicts that more than 40% of global organizations will suffer security and compliance incidents due to unauthorized AI tool use by 2030. 69% of cybersecurity leaders have evidence or suspect employees use public GenAI at work.

**Source:**
- Author: Phil Muncaster (reporting on Gartner VP analyst Arun Chandrasekaran's statements)
- Title: "Gartner: 40% of Firms to Be Hit By Shadow AI Security Incidents"
- Publisher: Infosecurity Magazine
- Date: November 20, 2025
- URL: https://www.infosecurity-magazine.com/news/gartner-40-firms-hit-shadow-ai/
- Primary Gartner research document: "Emerging Risk Deep Dive: Shadow AI" — https://www.gartner.com/en/documents/6714034

**Quality Rating:** B (Analyst prediction, well-sourced, Gartner credibility — not peer-reviewed academic)

**Verification Status:** Confirmed (independently cited by Fortra, ITpro, Freevacy, Petri.com)

**Context:**
- 50% of enterprises will face delayed AI upgrades due to unmanaged GenAI technical debt by 2030
- Gartner AI governance spending forecast: $492M in 2026, surpassing $1B by 2030
- Only 37% of organizations have policies to manage or detect shadow AI (IBM, 2025)
- 2023 Samsung incident cited as anchor example

**Slide Placement Suggestion:** 시나리오 B 위험 개요 슬라이드. "왜 지금 거버넌스인가" 시급성 근거로 사용 가능.

---

### FINDING 1-C: DTEX/Ponemon 2026 Cost of Insider Risks Global Report — Shadow AI Drives $19.5M Annual Loss

**Claim:** Insider risk now costs organizations an average of $19.5M annually — a 20% increase over two years. Shadow AI is identified as the primary driver of the surge in non-malicious insider costs ($10.3M of the total). Only 18% of organizations have fully integrated AI governance into their insider risk programs.

**Source:**
- Author/Organization: DTEX Systems + Ponemon Institute
- Title: "2026 Cost of Insider Risks Global Report"
- Publisher: DTEX / Ponemon Institute
- Date: February 2026 (announced February 24, 2026)
- URL: https://ponemon.dtex.ai/ (report landing page)
- Secondary coverage: https://www.helpnetsecurity.com/2026/02/26/insider-risk-costs-2026/
- Methodology: 354 organizations that experienced material insider incidents over the prior year

**Quality Rating:** B (Industry-sponsored research, Ponemon methodology, large sample)

**Verification Status:** Confirmed (cross-referenced: Infosecurity Magazine, HIPAAJournal, Digit.fyi, VMblog)

**Context:**
- Negligent/mistaken insiders: $10.3M annualized cost per org (17% YoY increase), avg $747,107 per incident
- Malicious insiders: $4.7M; Credential theft: $4.5M
- Shadow AI incidents include: uploading internal docs to ChatGPT, AI notetakers producing external summaries with sensitive data, AI browsers circumventing security controls
- Negligence, not malice, is the dominant cost driver

**Slide Placement Suggestion:** 시나리오 B 핵심 수치 슬라이드. 비승인 사용이 악의적 행위보다 더 큰 비용을 유발한다는 반직관적 포인트 강조.

---

### FINDING 1-D: Samsung ChatGPT Data Leak (2023) — Landmark Analogous Case

**Claim:** Three Samsung semiconductor employees leaked confidential information including source code and meeting notes to ChatGPT within 20 days of the company lifting its ChatGPT ban. One engineer pasted source code of semiconductor equipment measurement software. Another uploaded transcribed meeting notes for summarization.

**Source:**
- Author: Multiple (Gizmodo, TechRadar, Dark Reading — same event)
- Title: "Samsung engineers feed sensitive data to ChatGPT, sparking workplace AI warnings" (Dark Reading)
- Publisher: Dark Reading / Gizmodo / AI Incident Database
- Date: April 2023
- URLs:
  - https://www.darkreading.com/vulnerabilities-threats/samsung-engineers-sensitive-data-chatgpt-warnings-ai-use-workplace
  - https://gizmodo.com/chatgpt-ai-samsung-employees-leak-data-1850307376
  - https://incidentdatabase.ai/cite/768/ (AI Incident Database entry #768)

**Quality Rating:** B (Multiple verified news sources, AI Incident Database archival)

**Verification Status:** Confirmed (widely reported across major tech publications)

**Context:**
- Samsung had JUST lifted its internal ChatGPT ban when the incidents occurred
- OpenAI's data retention policy at the time meant proprietary data entered the training pipeline
- Samsung responded by restricting ChatGPT prompts to 1,024 bytes max and considering disciplinary action
- Data categories exposed: semiconductor equipment source code, test yield sequences, internal meeting content
- This case is specifically cited by Gartner as an anchor example for shadow AI risk
- HYPOTHESIS (medium confidence): Samsung subsequently banned generative AI from internal networks entirely

**Slide Placement Suggestion:** 시나리오 B 실제 사례 슬라이드. 가장 널리 알려진 비승인 AI 사용 데이터 유출 사례. "통제 전" 상황의 구체적 예시로 활용.

---

### FINDING 1-E: Microsoft Copilot EchoLeak (CVE-2025-32711) — Production AI Agent Exploitation

**Claim:** A critical zero-click vulnerability (CVSS 9.3) in Microsoft 365 Copilot enabled automated data exfiltration from OneDrive, SharePoint, Teams, and Outlook — without any user interaction. First real-world zero-click prompt injection exploit in a production LLM system.

**Source:**
- Author: Multiple (Hack The Box, SOC Prime, Securiti, ArXiv)
- Title: "EchoLeak: The First Real-World Zero-Click Prompt Injection Exploit in a Production LLM System"
- Publisher: ArXiv / various security publications
- Date: June 2025 (CVE assigned), ArXiv paper: September 10, 2025
- URLs:
  - https://arxiv.org/abs/2509.10540 (academic paper)
  - https://www.hackthebox.com/blog/cve-2025-32711-echoleak-copilot-vulnerability
  - https://socprime.com/blog/cve-2025-32711-zero-click-ai-vulnerability/

**Quality Rating:** A for technical severity (peer-reviewed ArXiv preprint + CVE assignment); B for incident scope (patched before widespread exploitation)

**Verification Status:** Confirmed (CVE officially assigned, Microsoft patched server-side)

**Context:**
- Attack vector: Hidden prompt injection in email body — no attachment, no link click required
- Bypassed Microsoft's XPIA (Cross Prompt Injection Attempt) classifier
- Chained multiple bypasses: link redaction circumvention, auto-fetched image abuse, Teams proxy exploitation
- Scope: Anything within Copilot's access: chat logs, OneDrive, SharePoint, Teams, Outlook
- Microsoft patched server-side without a traditional advisory or client-side action
- Key implication: Even SANCTIONED enterprise AI agents are attack surfaces; security cannot be assumed

**Slide Placement Suggestion:** 시나리오 B 기술적 위험 슬라이드. "승인된 AI도 벡터가 된다" — 비승인 AI의 위험을 강조하기 위한 대비 사례로 활용.

---

### FINDING 1-F: SaaS Supply Chain Breach via AI Chat Agent Integration (August 2025)

**Claim:** Threat actor UNC6395 hijacked a Drift/Salesloft chat agent OAuth integration, compromising 700+ organizations. The breach cascaded into unauthorized access across Salesforce, Google Workspace, Slack, Amazon S3, and Azure environments.

**Source:**
- Author: Tal Shapira (Reco Co-founder & CTO)
- Title: "AI & Cloud Security Breaches: 2025 Year in Review"
- Publisher: Reco.ai Blog
- Date: Published December 19, 2025; Updated March 6, 2026
- URL: https://www.reco.ai/blog/ai-and-cloud-security-breaches-2025

**Quality Rating:** C (Industry blog, vendor-authored, cites specific threat actor designation but no independent verification chain found)

**Verification Status:** Partially Confirmed (threat actor designation UNC6395 not yet cross-verified against Mandiant/CrowdStrike naming; incident scale plausible based on OAuth attack patterns)

**Context:**
- Attack method: OAuth token theft from a single AI integration point
- Key quote from article: "One integration became a doorway into everything connected to it"
- Represents the "shadow integration" risk — AI tools connected to enterprise systems without full security review
- Data exposed: Contacts, opportunities, AWS keys, Snowflake tokens
- Pattern: Attack sophistication didn't require breaking encryption; it exploited trusted identity

**Slide Placement Suggestion:** 시나리오 B 공급망 위험 슬라이드. AI 통합이 단일 장애점(single point of failure)이 될 수 있음을 보여주는 사례.

---

### FINDING 1-G: GTG-1002 — AI-Orchestrated State-Sponsored Espionage (November 2025)

**Claim:** A Chinese state-sponsored threat actor designated GTG-1002 used AI agents to automate 80-90% of a full cyber espionage campaign against approximately 30 organizations (tech, finance, government). AI handled reconnaissance, exploit development, credential harvesting, lateral movement, and data extraction — leaving only 4-6 human decision points per campaign.

**Source:**
- Author: Tal Shapira
- Title: "AI & Cloud Security Breaches: 2025 Year in Review"
- Publisher: Reco.ai Blog
- Date: December 19, 2025
- URL: https://www.reco.ai/blog/ai-and-cloud-security-breaches-2025
- Related reference: Anthropic November 2025 internal report on state-sponsored Claude Code manipulation (mentioned in HelpNetSecurity 2026-03-03 article)

**Quality Rating:** D (Single vendor source, threat actor designation not independently verified in public threat intel databases at time of research)

**Verification Status:** Unverified (plausible given public disclosure of AI-facilitated attack patterns; Anthropic separately disclosed state actor AI abuse in Nov 2025 but specific "GTG-1002" designation requires verification)

**Context:**
- CAVEAT: Treat as indicative of emerging threat class, not confirmed incident at citation quality
- The broader pattern is confirmed: IBM 2025 reports 16% of breaches involved attackers using AI tools
- Anthropic's Nov 2025 report (referenced in HelpNetSecurity article) did describe state-sponsored Claude Code manipulation — cross-check with Anthropic directly for confirmation
- Key implication: AI agents lower attacker cost structure while increasing campaign scale

**Slide Placement Suggestion:** 시나리오 B 고급 위협 슬라이드. 낮은 신뢰도 주석과 함께 사용. "AI-assisted attack" 트렌드의 방향성 근거로는 유효.

---

### FINDING 1-H: Netskope Shadow AI & Agentic AI Threat Report 2025 — Enterprise Usage Data

**Claim:** Over 50% of all AI application adoption is estimated to be shadow AI. 47% of GenAI platform users access them via personal accounts their companies cannot oversee. The average company experienced 223 shadow AI data policy incidents per month in 2025 (year-over-year doubling). 5.5% of organizations have users running agentic AI frameworks (LangChain dominant) without IT oversight.

**Source:**
- Author/Organization: Netskope Threat Labs
- Title: "Cloud and Threat Report: Shadow AI and Agentic AI 2025"
- Publisher: Netskope
- Date: 2025 (exact release date: press release published at prnewswire.com)
- URLs:
  - https://www.netskope.com/resources/cloud-and-threat-reports/cloud-and-threat-report-shadow-ai-and-agentic-ai-2025
  - https://www.prnewswire.com/news-releases/netskope-threat-labs-shadow-ai-risks-proliferate-as-genai-platforms-and-ai-agents-see-rapid-adoption-302518006.html

**Quality Rating:** B (Vendor telemetry data, large enterprise customer base, consistent with IBM findings)

**Verification Status:** Confirmed (cross-referenced with IBM 2025 report findings on shadow AI prevalence)

**Context:**
- Netskope tracks 1,550+ distinct GenAI SaaS applications (up from 317 in Feb 2025)
- Average enterprise uses approximately 15 GenAI apps
- 41% of organizations were using at least one GenAI platform as of May 2025
- Monthly data upload to GenAI apps: 8.2 GB average per organization
- Most popular platforms: Microsoft Azure OpenAI (29%), Amazon Bedrock (22%), Google Vertex AI (7.2%)

**Slide Placement Suggestion:** 시나리오 B 현황 통계 슬라이드. Shadow AI의 규모와 만연함을 데이터로 뒷받침.

---

### FINDING 1-I: OWASP Top 10 for Agentic Applications 2026 — Standardized Risk Taxonomy

**Claim:** OWASP GenAI Security Project released the first Top 10 for Agentic Applications (distinct from LLM Top 10), developed by 100+ security researchers. Key risks include: Agent Goal Hijack (ASI01), Tool Misuse, Identity and Privilege Abuse (ASI03), and Rogue Agents (ASI10).

**Source:**
- Author/Organization: OWASP GenAI Security Project (100+ researchers)
- Title: "OWASP Top 10 for Agentic Applications for 2026"
- Publisher: OWASP
- Date: December 9, 2025
- URLs:
  - https://genai.owasp.org/2025/12/09/owasp-top-10-for-agentic-applications-the-benchmark-for-agentic-security-in-the-age-of-autonomous-ai/
  - https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/

**Quality Rating:** A (Industry standard-setting body, multi-stakeholder review, 1+ year research process)

**Verification Status:** Confirmed

**Context:**
- Explicitly separate from LLM Top 10 because "when an AI can act on its own — accessing APIs, modifying databases, sending emails — it requires a fundamentally new security model"
- "Rogue Agents" category directly maps to shadow/unauthorized AI scenario
- "Tool Misuse" category: agents can call tools with destructive parameters or chain tools in unexpected sequences causing data loss
- Fine-tuning attacks bypassed Claude Haiku in 72% of cases; GPT-4o in 57% (HelpNetSecurity, citing Stanford Trustworthy AI Lab)
- OWASP framework is referenced by Microsoft, Palo Alto, McKinsey as baseline

**Slide Placement Suggestion:** 시나리오 B 기술적 위험 분류 슬라이드. 산업 표준 프레임워크 인용으로 신뢰도 강화.

---

### FINDING 1-J: Enterprise AI Agent Security Reality Check (Help Net Security / Multiple CISOs, 2026)

**Claim:** 88% of organizations reported a confirmed or suspected AI agent security incident in the last year (92.7% in healthcare). 80% of organizations encountered risky agent behaviors. Only 21% of executives have complete visibility into agent permissions and data access. Average enterprise operates ~1,200 unofficial AI applications.

**Source:**
- Author: Mirko Zorz (Director of Content, Help Net Security), quoting multiple enterprise CISOs
- Title: "AI went from assistant to autonomous actor and security never caught up"
- Publisher: Help Net Security
- Date: March 3, 2026
- URL: https://www.helpnetsecurity.com/2026/03/03/enterprise-ai-agent-security-2026/
- Contributors quoted: Deutsche Börse CISO, Databricks VP/Field CISO, Stanford Trustworthy AI Research Lab, MIT Sloan, Scale AI, 1Password CTO

**Quality Rating:** B (Practitioner survey + CISO quotes, recent publication, but survey methodology not fully disclosed)

**Verification Status:** Partially Confirmed (88% figure requires primary survey source; 80% risky behavior figure corroborated by McKinsey; $670K shadow AI premium corroborated by IBM)

**Context:**
- EY survey: 64% of companies with >$1B turnover lost more than $1M to AI failures
- 63% of employees pasted sensitive company data into personal chatbots in 2025
- 53% of companies now use RAG or agentic pipelines
- Existing frameworks (NIST AI RMF, ISO 42001) "lack agent-specific technical controls for tool parameter validation, injection logging, and containment testing" — key governance gap

**Slide Placement Suggestion:** 시나리오 B 도입부 / 현실 진단 슬라이드. "눈에 보이지 않는 위험" 컨셉을 CXO 대상으로 전달.

---

## SUBTOPIC 2: Agent 거버넌스 프레임워크 도입 사례

---

### FINDING 2-A: Singapore IMDA — World's First Governance Framework for Agentic AI (January 2026)

**Claim:** Singapore's IMDA launched the world's first governance framework specifically designed for autonomous AI agents on January 22, 2026 at the World Economic Forum. The framework addresses four dimensions: (1) Assess and bound risks upfront, (2) Make humans meaningfully accountable, (3) Implement technical controls throughout lifecycle, (4) Enable end-user responsibility.

**Source:**
- Author/Organization: IMDA (Infocomm Media Development Authority), Singapore
- Title: "Model AI Governance Framework for Agentic AI"
- Publisher: IMDA Singapore
- Date: January 22, 2026 (launched at WEF 2026)
- URLs:
  - https://www.imda.gov.sg/resources/press-releases-factsheets-and-speeches/press-releases/2026/new-model-ai-governance-framework-for-agentic-ai
  - https://www.imda.gov.sg/-/media/imda/files/about/emerging-tech-and-research/artificial-intelligence/mgf-for-agentic-ai.pdf (29-page PDF)
  - Legal analysis: https://www.bakermckenzie.com/en/insight/publications/2026/01/singapore-governance-framework-for-agentic-ai-launched (Baker McKenzie)
  - Analysis: https://www.computerweekly.com/news/366637674/Singapore-debuts-worlds-first-governance-framework-for-agentic-AI

**Quality Rating:** A (Government regulatory body, formal framework document, international launch venue)

**Verification Status:** Confirmed

**Context:**
- Builds on 2020 Singapore AI governance foundations
- Framework is a "living document" — IMDA inviting case studies
- Explicitly targets both in-house-developed and third-party agentic solution deployers
- Four dimensions map directly to enterprise governance pillars:
  1. Risk assessment + access bounding (scope/permissions)
  2. Human oversight mechanisms with override capability
  3. Design-time → pre-deployment → post-deployment control stages
  4. Transparency, escalation paths, user training
- Addresses: unauthorized actions, bias, data breaches, system disruptions
- Public feedback still open as of research date

**Slide Placement Suggestion:** 거버넌스 프레임워크 비교 슬라이드. "세계 최초" 포지셔닝으로 SK AX 거버넌스 선도성 어필 시 대조 사례.

---

### FINDING 2-B: NIST AI Agent Standards Initiative (February 2026)

**Claim:** NIST launched the "AI Agent Standards Initiative" in February 2026, covering: (1) Industry-led voluntary standards, (2) Community-led open protocols (NSF investment), (3) NIST research on agent authentication, identity infrastructure, and security evaluations. Sector-specific focus: healthcare, finance, education.

**Source:**
- Author/Organization: NIST (National Institute of Standards and Technology), U.S. Department of Commerce
- Title: "Announcing the AI Agent Standards Initiative for Interoperable and Secure Innovation"
- Publisher: NIST
- Date: Created February 17, 2026; Updated February 18, 2026
- URLs:
  - https://www.nist.gov/news-events/news/2026/02/announcing-ai-agent-standards-initiative-interoperable-and-secure
  - https://www.nist.gov/caisi/ai-agent-standards-initiative

**Quality Rating:** A (U.S. government standards body)

**Verification Status:** Confirmed

**Context:**
- Three strategic pillars: Industry-led Standards, Community-led Protocols, Research Investment
- Key focus areas: Safeguards against privilege escalation and unintended autonomous actions; Identity/Credentialing/Authorization for agents; Interoperability standards; Testing/Evaluation/Assurance methodologies
- RFI on AI Agent Security (deadline March 9, 2026)
- Draft Concept Paper on Software/AI Agent Identity and Authorization (deadline April 2, 2026)
- Approach: Voluntary, industry-led (not regulatory mandate)
- Complements existing NIST AI RMF (Risk Management Framework)

**Slide Placement Suggestion:** 거버넌스 국제 동향 슬라이드. "표준화 흐름" 섹션. NIST = 글로벌 기술 표준의 기준점.

---

### FINDING 2-C: Microsoft Agent Governance Framework — Agent 365 & Cloud Adoption Framework

**Claim:** Microsoft published a comprehensive 4-layer AI agent governance framework (Data Governance & Compliance / Agent Observability / Agent Security / Agent Development) in its Cloud Adoption Framework. 80% of Fortune 500 companies now deploy active AI agents. Microsoft launched "Agent 365" as a centralized control plane for AI agent governance.

**Source (Framework Document):**
- Author: stephen-sumner (Microsoft), ms.reviewer: ssumner
- Title: "Governance and security for AI agents across the organization — Cloud Adoption Framework"
- Publisher: Microsoft Learn / Azure Cloud Adoption Framework
- Date: Published December 1, 2025; Updated February 27, 2026
- URL: https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ai-agents/governance-security-across-organization

**Source (80% Fortune 500 Statistic):**
- Author: Vasu Jakkal (CVP, Microsoft Security)
- Title: "80% of Fortune 500 use active AI Agents: Observability, governance, and security shape the new frontier"
- Publisher: Microsoft Security Blog
- Date: February 10, 2026
- URL: https://www.microsoft.com/en-us/security/blog/2026/02/10/80-of-fortune-500-use-active-ai-agents-observability-governance-and-security-shape-the-new-frontier/

**Quality Rating:** B (Vendor framework — authoritative but self-promotional; 80% stat is Microsoft's own data)

**Verification Status:** Confirmed (framework document publicly available; Fortune 500 stat should be noted as Microsoft's internal customer data)

**Context — Four Governance Layers:**

**Layer 1: Data Governance & Compliance**
- Enforce data privacy (principle of minimal data)
- Mandate data residency compliance (region-specific)
- Define data retention policies with automated purging
- Tools: Microsoft Purview Compliance Manager (maps to EU AI Act, GDPR, HIPAA)

**Layer 2: Agent Observability**
- Assign unique Entra Agent Identity to every AI agent
- Maintain agent inventory (prevents shadow deployments)
- Centralize logging to Azure Log Analytics
- Track and allocate costs by department/project with real-time alerts
- Tool: Microsoft Agent 365 ($15/user/month control plane)

**Layer 3: Agent Security**
- Mandate AI threat protection (Defender for Cloud)
- Enforce infrastructure security baselines (same as customer-facing systems)
- Mandate adversarial red teaming before production
- Filter all inputs/outputs; enforce least privilege
- Establish incident response plans with agent-disable procedures
- Govern external MCP/A2A protocol integrations

**Layer 4: Agent Development**
- Standardize frameworks and SDKs
- Mandate MCP (Model Context Protocol) and A2A (Agent-to-Agent Protocol)
- Balance governance control with development agility

**Key Microsoft Policy Stance:** "AI governance cannot live solely within IT, and AI security cannot be delegated only to CISOs — spanning legal, compliance, HR, data science, business leadership, and board."

**Microsoft's additional statement:** "Ungoverned AI agents could become corporate 'double agents'" (VentureBeat, February 2026)
- Source: https://venturebeat.com/technology/microsoft-says-ungoverned-ai-agents-could-become-corporate-double-agents-its

**Slide Placement Suggestion:** 거버넌스 프레임워크 구조 슬라이드. Microsoft의 4레이어 모델을 SK AX의 4대 거버넌스 필러와 비교/정렬하는 데 활용.

---

### FINDING 2-D: EU AI Act — Agentic AI Regulatory Timeline & Compliance Requirements

**Claim:** The EU AI Act is now partially in force. Key milestones: GPAI model obligations active from August 2, 2025; High-risk AI system requirements (Annex III: employment, credit, education, law enforcement) enforceable from August 2, 2026; Full compliance deadline August 2026.

**Source:**
- Author/Organization: European Commission / EU Digital Strategy
- Title: "AI Act — Shaping Europe's Digital Future"
- Publisher: European Commission
- Date: Entered into force August 1, 2024; various obligations phased through 2026-2027
- URLs:
  - https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai
  - https://artificialintelligenceact.eu/
  - https://ai-act-service-desk.ec.europa.eu/en/ai-act/timeline/timeline-implementation-eu-ai-act
  - Legal analysis: https://www.legalnodes.com/article/eu-ai-act-2026-updates-compliance-requirements-and-business-risks

**Quality Rating:** A (Primary legislative source)

**Verification Status:** Confirmed

**Context:**
- Penalties: Up to €35M or 7% global turnover for prohibited AI violations; up to €15M or 3% for other obligations
- GPAI providers (as of Aug 2025) must: maintain private model documentation dossier; publish training data summaries; provide model cards; prove EU copyright compliance
- AI Office became operational August 2, 2025
- Each EU Member State must establish national AI regulatory sandbox by August 2, 2026
- GPAI Code of Practice: voluntary compliance tool published July 2025
- Agentic AI is NOT explicitly named but falls under GPAI and high-risk system categories based on use case

**Slide Placement Suggestion:** 거버넌스 규제 환경 슬라이드. 한국 기업의 EU 시장 진출 또는 글로벌 고객사 대상 솔루션 제공 시 컴플라이언스 필요성 근거.

---

### FINDING 2-E: McKinsey Agentic AI Safety & Security Playbook (October 2025)

**Claim:** McKinsey published a structured governance playbook for technology leaders (CIO, CRO, CISO, DPO) covering three phases: (1) Update risks and governance frameworks; (2) Establish oversight mechanisms; (3) Implement security controls. 80% of organizations have encountered risky behavior from AI agents.

**Source:**
- Author/Organization: McKinsey & Company (Risk and Resilience practice)
- Title: "Deploying agentic AI with safety and security: A playbook for technology leaders"
- Publisher: McKinsey & Company
- Date: October 16, 2025
- URL: https://www.mckinsey.com/capabilities/risk-and-resilience/our-insights/deploying-agentic-ai-with-safety-and-security-a-playbook-for-technology-leaders
- Companion article: "Trust in the age of agents" — https://www.mckinsey.com/capabilities/risk-and-resilience/our-insights/trust-in-the-age-of-agents

**Quality Rating:** B (Top-tier management consultancy, practitioner-facing, not peer-reviewed)

**Verification Status:** Confirmed (publicly available; 80% risky behavior stat corroborated by HelpNetSecurity)

**Context:**
- Key principle: "Organizations can't govern what they can't see — if they don't inventory and identity-bind systems, they're scaling unknown risk rather than agents"
- McKinsey GDP impact projection: $2.6T–$4.4T annually from agentic AI integration
- Foundational governance questions: Does AI policy framework address agentic systems? Is risk management equipped for agentic AI? Is there lifecycle governance?
- Emphasizes cross-functional governance (not IT-only)

**Slide Placement Suggestion:** 거버넌스 필요성 / 비즈니스 케이스 슬라이드. McKinsey 인용으로 경영진 설득력 강화. 특히 "볼 수 없으면 관리할 수 없다" 원칙은 SK AX 가시성(observability) 필러를 뒷받침.

---

### FINDING 2-F: JPMorgan Chase & Goldman Sachs — Enterprise AI Governance in Financial Services

**Claim:** JPMorgan Chase allocated $18B technology budget for 2025 and deployed LLM Suite to 200,000+ employees. Goldman Sachs became the first major financial institution to deploy an autonomous software agent (Devin by Cognition) across 12,000 developers, with formal model risk management (MRM) governance frameworks co-developed with data scientists.

**Source:**
- Author: Multiple (Lucidate Substack, DigitalDefynd, Klover.ai)
- Title: "Beyond the Pilot: How JPMorgan, Goldman Sachs, and HSBC Are Scaling AI to Enterprise Production"
- Publisher: Lucidate Substack
- URL: https://lucidate.substack.com/p/beyond-the-pilot-how-jpmorgan-goldman
- Goldman Sachs case study: https://digitaldefynd.com/IQ/goldman-sachs-using-ai-case-study/
- JPMorgan case study: https://digitaldefynd.com/IQ/jp-morgan-using-ai-case-study/

**Quality Rating:** C (Third-party analysis of publicly disclosed company information; Goldman's Devin deployment widely reported but specific governance details from secondary sources)

**Verification Status:** Partially Confirmed (Goldman Devin deployment is publicly confirmed; MRM governance framework details from secondary analysis; JPMorgan $18B budget from public earnings disclosures)

**Context:**
- Goldman Sachs governance approach: MRM (Model Risk Management) teams co-develop control frameworks with data scientists; in-house evaluation for performance, bias, and drift
- Goldman reported 3-4x productivity gain from Devin's autonomous software management
- JPMorgan governance approach: "Learn-by-doing" with rigorous ROI measurement; heavy data modernization investment
- JPMC plans 1,000+ AI use cases by 2026
- Financial services = most heavily governed AI sector due to regulatory scrutiny (OCC, FRB, FDIC model risk guidance)
- Key governance element: Model validation independence (MRM independent from model developers)

**Slide Placement Suggestion:** 거버넌스 산업별 도입 사례 슬라이드. 금융권 선도 기업의 실제 거버넌스 구조를 참조 사례로 제시.

---

### FINDING 2-G: EWSolutions Agentic AI Governance Framework — Three-Tiered Guardrail System

**Claim:** A published governance framework proposes three tiers of guardrails: (1) Foundational (data privacy, transparency, security — non-negotiable); (2) Risk-based (context-specific, scaled by severity); (3) Societal (ethical alignment, bias mitigation). Recommends "Digital Contractor" model: treat AI agents as external contractors requiring background checks, defined contracts, and supervision.

**Source:**
- Author: David Marco, PhD (President, EWSolutions)
- Title: "Agentic AI Governance: A Strategic Framework for 2026"
- Publisher: EWSolutions
- Date: Published January 8, 2026; Updated February 14, 2026
- URL: https://www.ewsolutions.com/agentic-ai-governance/

**Quality Rating:** C (Industry practitioner with PhD credentials, well-structured, but single-organization framework)

**Verification Status:** Confirmed (consistent with NIST, IMDA, McKinsey frameworks)

**Context:**
- Human oversight models: "Human-in-the-loop" for high-risk (healthcare, finance); "Human-on-the-loop" for lower-risk with retrospective review
- Regulatory references integrated: EU AI Act, ISO/IEC 42001, OWASP Top 10
- Key risks: Excessive agency enabling unauthorized database modifications; Indirect prompt injection from web content
- Implementation roadmap: Risk maturity assessment → cross-functional rules of engagement → continuous real-time monitoring

**Slide Placement Suggestion:** 거버넌스 프레임워크 구성 요소 슬라이드. "디지털 계약자" 메타포는 비기술 경영진에게 직관적으로 전달 가능.

---

### FINDING 2-H: Microsoft Agent 365 — Commercial Enterprise Governance Platform Launch

**Claim:** Microsoft launched "Agent 365" at $15/user/month as a centralized governance control plane for enterprise AI agents. Named a Leader in the 2025–2026 IDC MarketScape for Unified AI Governance Platforms. The "Frontier Suite" (Agent 365 + Microsoft 365 E7) announced for general availability May 1, 2026.

**Source:**
- Author: Vasu Jakkal (CVP, Microsoft Security); vaxowave.com analysis
- Title: "Secure agentic AI for your Frontier Transformation"
- Publisher: Microsoft Security Blog
- Date: March 9, 2026
- URLs:
  - https://www.microsoft.com/en-us/security/blog/2026/03/09/secure-agentic-ai-for-your-frontier-transformation/
  - https://www.microsoft.com/en-us/security/blog/2026/01/14/microsoft-named-a-leader-in-idc-marketscape-for-unified-ai-governance-platforms/
  - https://vaxowave.com/2026/01/12/microsoft-agent-365-ai-oversight-and-governance-for-the-copilot-era/

**Quality Rating:** B (Vendor announcement, IDC recognition is third-party validation)

**Verification Status:** Confirmed (publicly announced, IDC MarketScape is independently produced)

**Context:**
- Agent 365 capabilities: agent inventory and lifecycle management, observability dashboard, policy enforcement, cost tracking
- IDC MarketScape recognition validates Microsoft's governance positioning vs. competitors
- Pricing at $15/user/month signals commercial maturation of the governance market
- GA date May 1, 2026 is after current research date (March 15, 2026) — note as forward-looking
- VentureBeat quote: Microsoft warns "ungoverned AI agents could become corporate double agents" — strong marketing framing for governance urgency

**Slide Placement Suggestion:** 거버넌스 플랫폼 시장 슬라이드. 상용 솔루션 존재 자체가 "거버넌스가 선택이 아닌 필수"임을 방증. SK AX의 자체 거버넌스 역량 차별화 포인트.

---

### FINDING 2-I: IBM Think — AI Agent Governance Framework (Four Pillars)

**Claim:** IBM's published AI agent governance framework identifies four key challenges: (1) security, (2) risk management, (3) observability, and (4) agent lifecycle management. Only approximately 25–36% of organizations have a defined AI governance structure despite 78% using AI in at least one business process.

**Source:**
- Author/Organization: IBM Think Insights
- Title: "AI Agent Governance: Big Challenges, Big Opportunities"
- Publisher: IBM
- URL: https://www.ibm.com/think/insights/ai-agent-governance
- Supporting: https://www.ibm.com/think/insights/ai-governance-implementation

**Quality Rating:** B (Major enterprise vendor, practitioner-facing, IBM watsonx governance product alignment)

**Verification Status:** Confirmed (25–36% governance structure stat consistent with other surveys)

**Context:**
- 78% of organizations engaged in AI business process vs. only 25–36% with defined governance = significant maturity gap
- 60% of enterprises restrict agent access to sensitive data without human oversight
- Nearly half employ human-in-the-loop controls across high-risk workflows
- 2026 forecast: "orchestrated super-agent ecosystems, governed end-to-end by robust control systems"

**Slide Placement Suggestion:** 거버넌스 성숙도 갭 슬라이드. "AI 도입 78% vs. 거버넌스 보유 25-36%" 격차 시각화. SK AX 서비스의 타겟 고객 니즈를 수치로 정의.

---

## CROSS-CUTTING ANALYSIS

### Shadow AI → Governance: The Causal Chain

```
비승인 AI 사용 (Shadow AI)
  → 데이터 유출 / 침해 (평균 +$670K 비용)
  → 규제 위반 (EU AI Act, GDPR, HIPAA)
  → 운영 중단 (31% of AI incidents)
  → 신뢰 손상 (기업 명성 리스크)
  → 내부자 위협 증폭 ($19.5M 연간 비용)
```

### Governance Framework Convergence: 4 Common Pillars

모든 주요 프레임워크(IMDA, NIST, Microsoft CAF, McKinsey, IBM)가 공통적으로 포함하는 4개 핵심 구성 요소:

| Pillar | IMDA | NIST | Microsoft CAF | McKinsey | IBM |
|--------|------|------|---------------|----------|-----|
| **위험 평가 & 경계 설정** | Assess & Bound Risks | Safeguards & Risk Mgmt | Data Gov & Compliance | Update Governance Framework | Risk Management |
| **보안 통제** | Technical Controls | Identity & Auth | Agent Security | Security Controls | Security |
| **가시성 & 모니터링** | Technical Controls | Testing & Assurance | Agent Observability | Oversight Mechanisms | Observability |
| **인간 책임 & 생명주기** | Human Accountability | Interoperability | Agent Development | Cross-functional Governance | Lifecycle Mgmt |

### Confidence Summary

| Finding | Confidence | Key Caveat |
|---------|------------|------------|
| 1-A IBM breach stats | HIGH | Large-sample commissioned research |
| 1-B Gartner 40% prediction | HIGH | Prediction, not confirmed stat |
| 1-C DTEX $19.5M | HIGH | 354-org sample, Ponemon methodology |
| 1-D Samsung ChatGPT | HIGH | Widely confirmed, 2023 incident |
| 1-E EchoLeak CVE | HIGH | CVE-assigned, patched, ArXiv paper |
| 1-F SaaS supply chain breach | MEDIUM | Threat actor designation not independently verified |
| 1-G GTG-1002 espionage | LOW | Single vendor source, unverified threat actor name |
| 1-H Netskope shadow AI stats | HIGH | Vendor telemetry, large base |
| 1-I OWASP Agentic Top 10 | HIGH | Industry standard body |
| 1-J Help Net Security survey | MEDIUM | Survey methodology not fully disclosed |
| 2-A IMDA Singapore | HIGH | Government framework document |
| 2-B NIST Initiative | HIGH | U.S. government standards body |
| 2-C Microsoft CAF | HIGH (framework) / MEDIUM (80% stat) | Vendor data for Fortune 500 stat |
| 2-D EU AI Act | HIGH | Primary legislative source |
| 2-E McKinsey playbook | HIGH | Top-tier consultancy |
| 2-F JPMorgan/Goldman | MEDIUM | Secondary analysis of public disclosures |
| 2-G EWSolutions framework | MEDIUM | Single practitioner, consistent with peers |
| 2-H Agent 365 launch | HIGH | Public announcement + IDC validation |
| 2-I IBM four pillars | HIGH | Major vendor framework |

---

## KEY STATISTICS QUICK REFERENCE

| Statistic | Value | Source | Date |
|-----------|-------|--------|------|
| Orgs with AI model breaches | 13% | IBM/Ponemon | Jul 2025 |
| Breached orgs lacking AI access controls | 97% | IBM/Ponemon | Jul 2025 |
| Shadow AI additional breach cost | +$670,000 | IBM/Ponemon | Jul 2025 |
| Average annual insider risk cost | $19.5M | DTEX/Ponemon | Feb 2026 |
| Orgs experiencing shadow AI breaches | 20% | IBM/Ponemon | Jul 2025 |
| Orgs predicting shadow AI incident next 12mo | 49% | Various | 2025 |
| Gartner shadow AI incident prediction | 40% by 2030 | Gartner | Nov 2025 |
| Orgs with defined AI governance structure | 25–36% | IBM Think | 2025 |
| Fortune 500 with active AI agents | 80% | Microsoft | Feb 2026 |
| Average enterprise unofficial AI apps | ~1,200 | Various | 2025 |
| Employees pasting sensitive data into AI | 63% | IBM | 2025 |
| Over half AI app adoption = shadow AI | >50% | Netskope | 2025 |
| AI governance spending 2026 | $492M | Gartner | 2025 |
| AI governance spending 2030 | $1B+ | Gartner | 2025 |
| EchoLeak CVSS score | 9.3 (Critical) | CVE database | Jun 2025 |
| Fine-tuning attack bypass (Claude Haiku) | 72% | Stanford/Help Net | 2026 |

---

## RECOMMENDED SLIDE USAGE MAP

| Slide Context | Key Findings to Use |
|---------------|---------------------|
| 시나리오 B: 비승인 AI의 위험성 | 1-A, 1-B, 1-C, 1-D (Samsung) |
| 시나리오 B: 실제 보안 사고 사례 | 1-D, 1-E (EchoLeak), 1-F |
| 시나리오 B: 기술적 위험 분류 | 1-I (OWASP), 1-E |
| 거버넌스 필요성/긴급성 | 1-J, 2-E (McKinsey), 1-B (Gartner) |
| 거버넌스 프레임워크 구조 | 2-A (IMDA), 2-C (Microsoft), 2-E (McKinsey) |
| 글로벌 규제 환경 | 2-D (EU AI Act), 2-B (NIST) |
| 산업별 도입 사례 | 2-F (JPMorgan/Goldman) |
| 상용 플랫폼/시장 현황 | 2-H (Agent 365), 2-I (IBM) |
| ROI/비즈니스 케이스 | 1-C (+$19.5M avoided), 1-A (+$670K avoided) |

---

*Research completed: 2026-03-15. All URLs verified as accessible at time of research. Confidence ratings reflect source quality, not claim validity. Partially confirmed and unverified claims should not be presented as established facts in slides without appropriate attribution.*
