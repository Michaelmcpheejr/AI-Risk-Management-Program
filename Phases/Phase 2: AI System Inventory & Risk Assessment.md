# AI Risk Management & Governance Program

## Phase 2: AI System Inventory & Risk Assessment

**Organization:** [Enterprise / Federal Contractor]  
**Program Owner:** Chief Risk Officer & Chief AI Officer  
**Phase Duration:** Month 3-5  
**Key Outcome:** Complete AI system inventory with risk scoring and portfolio analysis  

---

## Executive Summary

Phase 2 establishes a comprehensive AI system inventory and applies the risk assessment framework from Phase 1. This phase answers critical questions:

- **How many AI systems do we have?**
- **What AI systems are in production vs. development?**
- **Which AI systems are CRITICAL vs. LOW-risk?**
- **Where are our biggest AI risks?**
- **Which AI systems need assessment first?**

**Key Objectives:**
1. Complete AI system discovery across the enterprise
2. Classify AI systems by type and function
3. Apply multi-dimensional risk scoring (Threat × Vulnerability × Impact × Trust)
4. Create AI system portfolio view
5. Develop executive dashboards for AI risk oversight
6. Prioritize assessment and governance activities

**Key Outcomes:**
- Master AI system inventory (50-200+ systems depending on organization size)
- Risk scores for each AI system (1.0-3.0 scale)
- AI system portfolio analysis (distribution across risk levels)
- Assessment prioritization roadmap
- Executive reporting dashboard
- Data quality assessment (gaps in AI system information)

---

## Part 1: AI System Discovery Process

### Step 1: Multi-Source AI System Identification

**Source 1: Software/AI Platform Inventory**
- Cloud AI services (AWS SageMaker, Azure ML, Google Vertex AI)
- ML platforms (Databricks, DataRobot, H2O)
- LLM APIs (OpenAI, Anthropic, Cohere)
- Internal AI/ML infrastructure

**Source 2: Development Teams**
- Data science teams
- ML engineering teams
- AI/ML research teams
- Individual data scientists/developers

**Source 3: Business Systems & Applications**
- Customer-facing applications with AI (chatbots, recommendations)
- Internal business applications (forecasting, optimization)
- Decision support systems
- Operational AI systems

**Source 4: IT & Infrastructure**
- Containerized services (Docker, Kubernetes with AI models)
- API endpoints serving AI predictions
- Data pipelines with ML models
- Infrastructure monitoring (logs showing AI model usage)

**Source 5: Department/Business Owner Interviews**
- Marketing (personalization, recommendations)
- Sales (lead scoring, forecasting)
- Operations (optimization, anomaly detection)
- Finance (fraud detection, forecasting)
- HR (resume screening, employee analytics)
- Customer Service (chatbots, intent classification)
- Product (A/B testing with AI, feature recommendations)

**Source 6: Procurement & Vendor Management**
- Third-party AI services (SaaS AI, AI vendors)
- AI model providers
- AI consulting firms
- Open-source model usage

**Source 7: Existing Inventories**
- AI project management systems
- GitHub repositories (AI/ML projects)
- ML model registries
- Data science project repositories

### Step 2: AI System Consolidation & Deduplication

**Challenge:** Same AI system appears under multiple names/contexts

**Examples:**
- "Chatbot" vs. "Customer Service LLM" vs. "OpenAI GPT"
- "Fraud Detection Model" vs. "Transaction Anomaly Detection"
- Multiple instances of same model (production + staging)

**Process:**
1. Consolidate duplicate entries
2. Identify related systems (different versions of same model)
3. Link parent/child relationships (production vs. staging)
4. Create master record with all aliases

**Result:** One master AI system list (deduplicated)

### Step 3: AI System Master Data Collection

**Core Information to Collect:**

| Field | Description | Source | Required |
|-------|-------------|--------|----------|
| System ID | Unique identifier | Generated | Yes |
| System Name | Official name | Development team | Yes |
| Aliases | Alternative names | Multiple sources | No |
| AI Type | From Phase 1 categories (LLM, ML, etc.) | Classification | Yes |
| Primary Owner | Business owner/department | Business owner | Yes |
| Technical Owner | Data scientist/ML engineer | Development team | Yes |
| Status | Development/Production/Retired | Development team | Yes |
| Deployment Date | When did it go live? | IT/DevOps | For production |
| Business Purpose | What does this AI system do? | Business owner | Yes |
| Training Data | What data was used to train? | Data science | Yes |
| Update Frequency | How often is model retrained? | ML Engineering | Yes |
| Users/Impact | How many people use it? | Business owner | Yes |

### Step 4: AI System Data Quality Assessment

**Quality Levels:**

| Quality Level | Description | Completeness |
|---------------|-------------|-------------|
| Complete | All required fields populated, verified | 95%+ |
| Substantial | Most fields populated, some gaps | 75-95% |
| Partial | Basic information only | 50-75% |
| Minimal | Name and owner only | <50% |

**Action Items Based on Quality:**
- **Complete systems:** Ready for risk assessment
- **Substantial systems:** Collect missing data before assessment
- **Partial systems:** Data collection task needed
- **Minimal systems:** May need to reconcile (is this a real AI system?)

---

## Part 2: AI System Classification & Categorization

### AI System Type Classification (From Phase 1)

**Apply each AI system to one primary type:**

**Type 1: Large Language Models (LLMs)**
- Examples: ChatGPT integration, Claude API, internal LLM, GPT-4
- Typical Risk Level: CRITICAL to HIGH
- Assessment Depth: Comprehensive
- Governance Frequency: Monthly to Quarterly

**Type 2: Generative AI (Non-LLM)**
- Examples: Image generation, code generation, audio synthesis
- Typical Risk Level: HIGH to MEDIUM
- Assessment Depth: Comprehensive
- Governance Frequency: Quarterly

**Type 3: Predictive/Classification ML**
- Examples: Fraud detection, churn prediction, credit scoring, disease diagnosis
- Typical Risk Level: CRITICAL to HIGH (if consequential)
- Assessment Depth: Comprehensive
- Governance Frequency: Quarterly to Semi-annual

**Type 4: Computer Vision**
- Examples: Image classification, facial recognition, object detection
- Typical Risk Level: HIGH to MEDIUM
- Assessment Depth: Comprehensive (bias testing)
- Governance Frequency: Quarterly

**Type 5: Recommendation Systems**
- Examples: Product recommendations, content recommendations, personalization
- Typical Risk Level: MEDIUM
- Assessment Depth: Standard
- Governance Frequency: Semi-annual

**Type 6: Autonomous Systems**
- Examples: Self-driving vehicles, robotic systems, autonomous drones
- Typical Risk Level: CRITICAL
- Assessment Depth: Deep (safety-critical)
- Governance Frequency: Continuous monitoring

**Type 7: AI-Powered Decision Systems**
- Examples: Hiring decisions, loan approvals, content moderation, sentencing
- Typical Risk Level: CRITICAL (due to human impact)
- Assessment Depth: Comprehensive (fairness, explainability)
- Governance Frequency: Monthly

---

## Part 3: Multi-Dimensional Risk Scoring

### Apply Phase 1 Risk Scoring Formula to Each AI System

**Formula:** Risk Score = (Threat × Vulnerability × Impact × Trust) / 10

**Scale: 1.0 - 3.0**

### Dimension 1: Threat Level (1-3 Scale)

**Based on AI System Type & Maturity:**

| Score | Level | Criteria |
|-------|-------|----------|
| 3 | High Threat | New/unproven technology, complex model, limited testing, black box |
| 2 | Medium Threat | Proven technology, adequate testing, some interpretability |
| 1 | Low Threat | Well-established, extensively tested, proven in production, explainable |

**Examples:**
- LLM with hallucination history = Threat 3
- Fraud detection model with 2+ years production = Threat 1
- New computer vision model for faces = Threat 3

### Dimension 2: Vulnerability Level (1-3 Scale)

**Based on Security & Robustness:**

| Score | Level | Criteria |
|-------|-------|----------|
| 3 | High Vulnerability | No adversarial testing, unprotected API, training data exposed, model easily stolen |
| 2 | Medium Vulnerability | Some security measures, API authentication, training data partially secured |
| 1 | Low Vulnerability | Comprehensive security, adversarial testing, encrypted models, access control |

**Examples:**
- Public LLM API with no rate limiting = Vulnerability 3
- Fraud detection with access control and monitoring = Vulnerability 1

### Dimension 3: Impact Level (1-3 Scale)

**Based on Business/Regulatory Consequence:**

| Score | Level | Criteria |
|-------|-------|----------|
| 3 | High Impact | Consequential decisions (hiring, medical, criminal), regulatory exposure $10M+, user harm, reputational risk |
| 2 | Medium Impact | Important decisions (loan approval), regulatory exposure $1M-$10M, user inconvenience |
| 1 | Low Impact | Non-critical decisions (recommendations, content), minimal regulatory exposure, no user harm |

**Examples:**
- AI hiring system = Impact 3
- Product recommendation engine = Impact 1
- Medical diagnosis AI = Impact 3

### Dimension 4: Trust Level (1-3 Scale)

**Based on Fairness, Transparency, Reliability:**

| Score | Level | Criteria |
|-------|-------|----------|
| 3 | High Trust | Extensively bias tested, results explainable, transparent to users, validated on diverse data |
| 2 | Medium Trust | Some bias testing, partially explainable, works for common cases, standard validation |
| 1 | Low Trust | No bias testing, black box, unexplainable, limited validation, diverse data unknown |

**Examples:**
- Facial recognition with no bias testing on minorities = Trust 1
- Loan approval model with explainability + fairness testing = Trust 3

### Risk Scoring Examples

**Example 1: Customer Service Chatbot (LLM)**
- Threat: 2 (LLMs have known hallucination issues)
- Vulnerability: 2 (API authenticated, but model could be prompted to leak data)
- Impact: 2 (Customer frustration if hallucinations, not life-threatening)
- Trust: 1 (Limited bias/fairness testing)

**Risk Score = (2 × 2 × 2 × 1) / 10 = 0.8 (LOW)... but escalates to MEDIUM due to hallucination risk**

**Example 2: Medical Diagnosis AI**
- Threat: 2 (Proven ML technology, but medical context is high-stakes)
- Vulnerability: 1 (Secure infrastructure, access controlled)
- Impact: 3 (Consequential - medical decisions affect health)
- Trust: 1 (Limited bias testing on diverse populations)

**Risk Score = (2 × 1 × 3 × 1) / 10 = 0.6 (LOW mathematically)... escalates to CRITICAL due to impact + fairness**

**Adjusted: CRITICAL (requires extensive bias testing, explainability, human override)**

**Example 3: Fraud Detection Model (Predictive ML)**
- Threat: 1 (Proven technology, well-tested)
- Vulnerability: 1 (Secure, access controlled, encrypted)
- Impact: 2 (Important decision but mitigated by human review)
- Trust: 2 (Bias testing done, somewhat explainable)

**Risk Score = (1 × 1 × 2 × 2) / 10 = 0.4 (LOW)**

**Actual: MEDIUM (requires monitoring, but not critical)**

**Example 4: Hiring AI System**
- Threat: 2 (ML with known bias issues)
- Vulnerability: 2 (API access, potential training data bias)
- Impact: 3 (Consequential - hiring decisions affect careers, legal liability)
- Trust: 1 (No bias testing, unexplainable decisions, not validated on diverse candidates)

**Risk Score = (2 × 2 × 3 × 1) / 10 = 1.2 (MEDIUM... escalates to CRITICAL)**

**Adjusted: CRITICAL (requires extensive bias testing, fairness audit, explainability, human override)**

---

## Part 4: Sample AI System Portfolio (Example Organization)

**Example Organization:** TechSecure Inc. (500 employees, 25+ AI systems)

### Portfolio Overview

**Total AI Systems: 24**

| Risk Level | Count | % | Assessment Priority |
|------------|-------|---|-------------------|
| CRITICAL | 3 | 13% | Phase 1 (immediate) |
| HIGH | 5 | 21% | Phase 2 (weeks 1-4) |
| MEDIUM | 8 | 33% | Phase 3 (weeks 5-12) |
| LOW | 8 | 33% | Phase 4 (ongoing) |

### CRITICAL AI Systems (3 Total)

**CRIT-001: Hiring Recommendation AI**
- Type: Predictive ML (Candidate Ranking)
- Threat: 2 | Vulnerability: 2 | Impact: 3 | Trust: 1
- **Risk Score: 1.2 → CRITICAL (fairness & discrimination risk)**
- Status: Production (2 years)
- Impact: Used for 80% of hiring decisions
- Assessment Priority: IMMEDIATE

**CRIT-002: Medical Diagnosis Assistant**
- Type: Predictive ML (Medical Decision Support)
- Threat: 2 | Vulnerability: 1 | Impact: 3 | Trust: 1
- **Risk Score: 0.6 → CRITICAL (high impact, fairness concern)**
- Status: Production (1 year)
- Impact: Assists doctors in diagnosis (10+ hospitals using)
- Assessment Priority: IMMEDIATE

**CRIT-003: Internal LLM Chatbot**
- Type: LLM (Internal Customer Support)
- Threat: 2 | Vulnerability: 2 | Impact: 2 | Trust: 1
- **Risk Score: 0.8 → MEDIUM... escalates to CRITICAL (hallucination + data leakage risk)**
- Status: Production (6 months)
- Impact: Answers customer questions, potential to leak proprietary info
- Assessment Priority: IMMEDIATE

### HIGH AI Systems (5 Total - Sample)

**HIGH-001: Fraud Detection Model**
- Type: Predictive ML
- Threat: 1 | Vulnerability: 1 | Impact: 2 | Trust: 2
- **Risk Score: 0.4 → LOW... escalates to MEDIUM/HIGH (business critical)**
- Status: Production (3 years)
- Impact: Catches 95% of fraud

**HIGH-002: Product Recommendation Engine**
- Type: Recommendation System
- Threat: 1 | Vulnerability: 2 | Impact: 2 | Trust: 2
- **Risk Score: 0.4 → MEDIUM**
- Status: Production (2 years)
- Impact: 30% of revenue from recommended products

**HIGH-003: Sentiment Analysis (Customer Feedback)**
- Type: NLP Classification
- Threat: 2 | Vulnerability: 1 | Impact: 2 | Trust: 1
- **Risk Score: 0.4 → MEDIUM**
- Status: Production (1 year)
- Impact: Used for customer satisfaction metrics

*(2 more HIGH systems not listed)*

### MEDIUM AI Systems (8 Total - Sample)

**MED-001: Content Moderation AI**
- Type: Classification ML
- Risk Score: 0.6 → MEDIUM
- Status: Production

**MED-002: Demand Forecasting Model**
- Type: Time Series Prediction
- Risk Score: 0.4 → LOW/MEDIUM
- Status: Production

*(6 more MEDIUM systems not listed)*

### LOW AI Systems (8 Total)

**LOW-001: Product Category Classification**
- Type: Image Classification
- Risk Score: 0.2 → LOW
- Status: Production

**LOW-002: Email Spam Detection**
- Type: Text Classification
- Risk Score: 0.3 → LOW
- Status: Production

*(6 more LOW systems not listed)*

---

## Part 5: AI System Portfolio Analysis

### Risk Distribution

```
RISK DISTRIBUTION

CRITICAL (3 systems, 13%)
█████ 13%

HIGH (5 systems, 21%)
██████████ 21%

MEDIUM (8 systems, 33%)
█████████████████ 33%

LOW (8 systems, 33%)
█████████████████ 33%
```

### AI System Type Distribution

| Type | Count | % | Avg Risk |
|------|-------|---|----------|
| Predictive ML | 8 | 33% | MEDIUM |
| Recommendation | 5 | 21% | MEDIUM |
| LLM/Generative | 4 | 17% | HIGH |
| Computer Vision | 4 | 17% | MEDIUM |
| Decision Systems | 2 | 8% | CRITICAL |
| Autonomous | 1 | 4% | CRITICAL |

### Impact Risk Profile

**Systems Making Consequential Decisions: 5 (21%)**
- Hiring AI (CRITICAL)
- Medical diagnosis (CRITICAL)
- Content moderation (MEDIUM)
- Loan approval (HIGH)
- Employee analytics (MEDIUM)

**Implication:** 21% of AI systems directly affect people; require intensive fairness/explainability oversight

### Bias & Fairness Risk Profile

**Systems Tested for Bias: 8 (33%)**
- Bias testing complete: 5 systems
- Bias testing in progress: 3 systems

**Systems NOT Tested for Bias: 16 (67%)**
- High-risk (fairness-critical): 5 systems
- Medium-risk: 8 systems
- Low-risk: 3 systems

**Implication:** 67% of AI systems have no bias testing; high-risk systems require urgent assessment

---

## Part 6: Assessment Prioritization Roadmap

### Phase 1: CRITICAL AI Systems (Weeks 1-4)

**Priority:** Immediate

**Systems (3 total):**
- Hiring AI, Medical Diagnosis AI, LLM Chatbot

**Assessment Type:** Deep Assessment
- Bias testing (multiple demographic groups)
- Threat modeling (adversarial attacks)
- Explainability analysis
- Data provenance audit
- Human oversight review

**Deliverable:** Detailed assessment report per system

**Timeline:** 4 weeks

### Phase 2: HIGH AI Systems (Weeks 5-8)

**Priority:** High

**Systems (5 total):**

**Assessment Type:** Comprehensive Assessment
- Bias testing (where applicable)
- Performance monitoring baseline
- Security evaluation
- Documentation review

**Timeline:** 4 weeks

### Phase 3: MEDIUM AI Systems (Weeks 9-16)

**Priority:** Medium

**Systems (8 total):**

**Assessment Type:** Standard Assessment
- Risk questionnaire
- Bias testing (if consequential)
- Performance metrics
- Documentation verification

**Timeline:** 8 weeks

### Phase 4: LOW AI Systems (Weeks 17+)

**Priority:** Low

**Systems (8 total):**

**Assessment Type:** Lightweight Assessment
- Basic documentation review
- Status verification
- Owner confirmation

---

## Part 7: Executive Dashboard & Reporting

### Dashboard 1: AI Risk Portfolio (Board/Executive)

**Key Metrics:**
- Total AI systems: 24
- Assessed: 8 (33%)
- Pending assessment: 16 (67%)
- CRITICAL systems assessed: 3/3 (100%)
- HIGH systems assessed: 2/5 (40%)

**Visualization:**
- Risk distribution pie chart
- Assessment progress bar
- CRITICAL systems status (red/yellow/green)
- Bias testing completion rate

### Dashboard 2: Assessment Progress (Steering Committee)

**Key Metrics:**
- CRITICAL systems in assessment: 3 (Week 2/4)
- Bias testing completed: 5/24 systems
- Outstanding assessments: 16
- Timeline: On schedule

### Dashboard 3: AI System Risk Heatmap (Operations)

**Display:**
- Each system plotted on risk matrix (Threat vs. Impact)
- Color-coded by trust level (red=untested, yellow=partial, green=tested)
- Trend arrows (improving/worsening)

---

## Part 8: Success Metrics

### Phase 2 Completion Metrics

| Metric | Target | Evidence |
|--------|--------|----------|
| AI system inventory complete | 100% of systems identified | Master inventory with 24 systems |
| Risk scores calculated | 100% of systems | Risk scoring register |
| Assessment roadmap defined | Yes | Prioritization document with phases |
| Executive dashboards created | Yes | Dashboard mockups |
| Data quality verified | 95%+ complete | Data quality report |

### Ongoing Program Health Metrics

| Metric | Target | Owner |
|--------|--------|-------|
| Assessment completion rate | On schedule per roadmap | Governance Lead |
| Risk score accuracy | Spot check quarterly | Chief Risk Officer |
| Executive dashboard currency | 100% current | Risk Operations |
| AI system tracking accuracy | 95%+ | AI Governance Team |

---

**Phase 2 Complete. Ready for Phase 3: AI Assessment & Risk Mitigation?**
