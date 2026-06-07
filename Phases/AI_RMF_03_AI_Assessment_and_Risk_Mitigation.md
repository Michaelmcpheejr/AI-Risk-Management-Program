# AI Risk Management & Governance Program

## Phase 3: AI Assessment & Risk Mitigation

**Organization:** [Enterprise / Federal Contractor]  
**Program Owner:** Chief Risk Officer & Chief AI Officer  
**Phase Duration:** Month 6-18 (ongoing)  
**Key Outcome:** Complete AI system assessments with mitigation plans  

---

## Executive Summary

Phase 3 operationalizes AI assessment. This phase takes the prioritization from Phase 2 and conducts actual risk assessments, applying testing procedures to determine which AI systems need mitigation and how urgent.

**Key Objectives:**
1. Conduct risk-based assessments for all AI systems (CRITICAL first)
2. Test AI systems for bias, adversarial robustness, performance
3. Evaluate transparency and explainability
4. Identify control gaps and mitigation needs
5. Track remediation through completion
6. Document assessment results and mitigation plans

**Key Outcomes:**
- Completed assessment reports for 100% of AI systems
- Risk scores for each AI system (validated/updated)
- Mitigation plans for at-risk AI systems
- Testing documentation (bias, adversarial, performance)
- Assessment tracking dashboard
- Escalation procedures for critical findings

---

## Part 1: Assessment Methodology by AI System Risk Level

### CRITICAL AI System Assessment (Deep Dive)

**Timeline:** 4-6 weeks per system

**Assessment Components:**

#### Component 1: Bias & Fairness Testing

**What is Bias Testing?**
Testing whether AI system produces discriminatory outcomes for protected groups (race, gender, age, religion, etc.)

**Testing Procedures:**

**Procedure 1: Demographic Parity Testing**
- Measure: Does the AI system treat demographic groups equally?
- Method: Run same inputs for different demographic groups, compare outcomes
- Acceptance Threshold: <5% difference in outcomes between groups
- Example: Hiring AI should accept similar % of candidates across gender groups

**Procedure 2: Equalized Odds Testing**
- Measure: Are false positive and false negative rates equal across groups?
- Method: Compare Type I and Type II errors by demographic group
- Acceptance Threshold: <5% difference in error rates between groups
- Example: Loan AI should deny similarly qualified applicants at same rate across races

**Procedure 3: Calibration Testing**
- Measure: When AI predicts 80% confidence, does outcome actually occur 80% of the time?
- Method: Compare predicted probability vs. actual outcomes by demographic group
- Acceptance Threshold: Calibration within 5% across groups
- Example: Medical diagnosis AI's confidence should match actual diagnosis accuracy

**Procedure 4: Disparate Impact Analysis**
- Measure: Does AI system have disparate impact on protected groups?
- Legal threshold: 80% rule (selection rate for protected group < 80% of majority group = potential discrimination)
- Method: Calculate selection rates by demographic group
- Acceptance Threshold: >80% selection rate for protected groups vs. majority

**Output:** Bias testing report showing results for each demographic group

#### Component 2: Adversarial Robustness Testing

**What is Adversarial Testing?**
Testing whether AI system can be fooled by crafted inputs designed to cause failures

**Testing Procedures:**

**Procedure 1: Adversarial Example Generation**
- Create inputs specifically designed to fool the AI system
- Methods: Fast Gradient Sign Method (FGSM), Projected Gradient Descent (PGD)
- Test: Can adversary slightly modify input to change prediction?
- Example: Slightly modify image pixels to fool image classification

**Procedure 2: Jailbreak Testing (For LLMs)**
- Attempt to make LLM violate its safety guidelines
- Methods: Prompt injection, role-playing, social engineering
- Test: Can LLM be tricked into harmful responses?
- Example: Can LLM be convinced to provide instructions for illegal activities?

**Procedure 3: Input Boundary Testing**
- Test AI system at extreme/unusual input values
- Examples: Very large numbers, empty inputs, special characters, foreign languages
- Test: Does system fail gracefully or crash?
- Acceptance Threshold: System should handle all inputs without crashing

**Output:** Adversarial robustness report showing vulnerabilities found

#### Component 3: Performance & Accuracy Testing

**What is Performance Testing?**
Testing whether AI system achieves acceptable accuracy on diverse datasets

**Testing Procedures:**

**Procedure 1: Out-of-Distribution Testing**
- Test AI system on data different from training data
- Examples: Test on different geographic regions, time periods, customer segments
- Metric: Does accuracy degrade significantly on new data?
- Acceptance Threshold: <5% accuracy degradation on out-of-distribution data

**Procedure 2: Minority Class Performance Testing**
- For systems with imbalanced classes, test on underrepresented classes
- Example: If 99% of transactions are legitimate, test 1% fraud cases separately
- Metric: Does accuracy for minority class meet threshold?
- Acceptance Threshold: Minority class accuracy >90%

**Procedure 3: Temporal Stability Testing**
- Test AI system over time to detect model drift
- Method: Compare performance from week 1 vs. week 4 vs. week 12
- Metric: Does accuracy degrade over time?
- Acceptance Threshold: <2% accuracy degradation per month

**Output:** Performance testing report showing accuracy metrics by demographic group and data type

#### Component 4: Transparency & Explainability Evaluation

**What is Explainability?**
Ability to explain why AI system made a specific prediction

**Evaluation Procedures:**

**Procedure 1: Feature Importance Analysis**
- Identify which features most influenced the prediction
- Methods: SHAP, LIME, Feature Importance scores
- Question: Can we explain which factors drove the decision?
- Acceptance Threshold: Top 3-5 features explain >80% of prediction

**Procedure 2: Decision Rules Documentation**
- For consequential AI systems, document explicit rules
- Question: What conditions lead to which outcome?
- Example: "Loan approved if credit score >650 AND debt-to-income <40%"
- Acceptance Threshold: All HIGH/CRITICAL systems must document decision logic

**Procedure 3: User Communication Audit**
- Review what users are told about AI system's decision
- Question: Is explanation clear to non-technical user?
- Example: Can candidate understand why they weren't hired?
- Acceptance Threshold: Users can understand decision reason

**Output:** Explainability report with feature importance, decision rules, user explanations

#### Component 5: Data Quality & Provenance Audit

**What is Data Provenance?**
Understanding where training data came from and if it's representative

**Audit Procedures:**

**Procedure 1: Training Data Source Audit**
- Document: Where did training data come from?
- Questions: Is data representative of production users?
- Example: Was hiring AI trained only on successful hires (selection bias)?

**Procedure 2: Data Freshness & Currency**
- How old is training data?
- If using years-old data: Is data still representative?
- Example: Does medical diagnosis AI account for new diseases?

**Procedure 3: Data Labeling Quality**
- Who labeled the data?
- Are labels consistent and accurate?
- Method: Random sample check, inter-annotator agreement
- Acceptance Threshold: >95% labeling accuracy

**Output:** Data audit report documenting provenance, quality, representativeness

#### Component 6: Human Oversight & Appeal Process

**What is Human Oversight?**
Ensuring humans can review and override AI decisions

**Evaluation Procedures:**

**Procedure 1: Override Capability**
- Can humans override AI decisions?
- Example: Can hiring manager reject AI recommendation?
- Acceptance Threshold: All CRITICAL systems must have human override

**Procedure 2: Appeal Process**
- Can users appeal/challenge AI decisions?
- Example: Can job candidate request human review?
- Acceptance Threshold: All consequential decisions must have appeal process

**Procedure 3: Decision Audit Trail**
- Is there audit trail of all AI decisions?
- Can we retrieve why a specific decision was made?
- Acceptance Threshold: 100% of consequential decisions logged

**Output:** Human oversight report documenting override, appeal, and audit procedures

---

### HIGH AI System Assessment (Comprehensive)

**Timeline:** 2-3 weeks per system

**Assessment Components (Subset of CRITICAL):**

- Bias & fairness testing (if consequential) - REQUIRED
- Adversarial robustness testing (abbreviated) - If applicable
- Performance testing (basic accuracy) - REQUIRED
- Explainability evaluation (basic) - If consequential
- Data quality audit (basic) - REQUIRED
- Human oversight review - If consequential

---

### MEDIUM AI System Assessment (Streamlined)

**Timeline:** 1-2 weeks per system

**Assessment Components (Minimal):**

- Bias testing (if consequential) - If decision-making system
- Performance documentation review - REQUIRED
- Explainability documentation - If consequential
- Data quality confirmation - REQUIRED

---

### LOW AI System Assessment (Lightweight)

**Timeline:** 3-5 days per system

**Assessment Components:**

- Basic documentation review - REQUIRED
- Performance metrics verification - REQUIRED
- Data provenance confirmation - REQUIRED
- No bias testing required

---

## Part 2: Risk Mitigation Controls

### Control 1: Bias Mitigation

**For AI systems showing bias:**

**Mitigation Technique 1: Balanced Dataset Retraining**
- Retrain model on balanced dataset (equal representation of demographic groups)
- Expected outcome: Reduced demographic parity gap
- Effort: 2-4 weeks, requires data engineering
- Cost: Minimal (uses existing data)

**Mitigation Technique 2: Fairness Constraints**
- Add fairness objectives to model training (Lagrangian fairness, constrained optimization)
- Expected outcome: Enforced fairness during training
- Effort: 1-2 weeks (data science)
- Cost: Minimal

**Mitigation Technique 3: Post-Processing Adjustment**
- Adjust model outputs post-prediction to enforce fairness
- Example: Adjust threshold by demographic group
- Effort: 1 week
- Cost: Minimal
- Caution: May reduce overall accuracy

**Mitigation Technique 4: Model Monitoring & Alerts**
- Continuous monitoring of bias metrics
- Alert if bias degradation detected
- Effort: 1-2 weeks
- Cost: Tool cost ($5K-$20K/year)

**Mitigation Technique 5: Human Review Layer**
- Add human review for high-impact decisions
- Example: Hiring AI recommends, but human reviews all decisions
- Effort: 1 week (process change)
- Cost: Operational (human time)

### Control 2: Adversarial Robustness

**For AI systems vulnerable to adversarial attacks:**

**Mitigation Technique 1: Adversarial Training**
- Train model on adversarial examples
- Expected outcome: Model learns to resist adversarial attacks
- Effort: 2-4 weeks
- Cost: Minimal (computational resources)

**Mitigation Technique 2: Input Validation & Sanitization**
- Validate/sanitize inputs before passing to model
- Example: Range checks, type validation, special character removal
- Effort: 1-2 weeks
- Cost: Minimal

**Mitigation Technique 3: Ensemble Methods**
- Use multiple models for redundancy
- If one model attacked, others may still work
- Effort: 2-3 weeks
- Cost: Computational (multiple models running)

**Mitigation Technique 4: Rate Limiting & Monitoring**
- Limit request rate per user/IP
- Monitor for unusual patterns
- Effort: 1 week
- Cost: Minimal

### Control 3: Model Drift Detection

**For AI systems at risk of performance degradation:**

**Mitigation Technique 1: Data Drift Monitoring**
- Monitor input data distribution
- Alert if distribution changes significantly
- Effort: 1-2 weeks
- Cost: Tool cost ($5K-$20K/year)

**Mitigation Technique 2: Model Performance Monitoring**
- Continuously measure model accuracy
- Alert if accuracy drops below threshold
- Effort: 1-2 weeks
- Cost: Tool cost

**Mitigation Technique 3: Automated Retraining Pipeline**
- Automatically retrain model on fresh data
- Effort: 2-3 weeks
- Cost: Engineering effort + computational resources

**Mitigation Technique 4: Human Review Process**
- Periodic human audit of AI outputs
- Catch degradation early through spot checks
- Effort: Ongoing (0.5-1 day/week)
- Cost: Operational

### Control 4: Transparency & Explainability

**For AI systems lacking transparency:**

**Mitigation Technique 1: Feature Importance Documentation**
- Calculate and document top features influencing each decision
- Effort: 1-2 weeks
- Cost: Minimal

**Mitigation Technique 2: Decision Rule Extraction**
- Extract interpretable rules from black-box model
- Example: "If credit score >750 AND income >$50K, approve"
- Effort: 2-3 weeks
- Cost: Minimal

**Mitigation Technique 3: Model Explanation API**
- Provide explanation with each prediction
- Example: API returns "Approved because credit score (750) is above threshold (700)"
- Effort: 2-4 weeks
- Cost: Development effort

**Mitigation Technique 4: User Communication Plan**
- Communicate how AI decision works to affected users
- Example: Job candidates receive explanation of hiring decision
- Effort: 1-2 weeks (process/communication)
- Cost: Minimal

### Control 5: Access Control & Data Security

**For AI systems handling sensitive data:**

**Mitigation Technique 1: Encryption**
- Encrypt models and data at rest and in transit
- Effort: 1-2 weeks
- Cost: Minimal (standard security)

**Mitigation Technique 2: Access Control**
- Limit who can access model and data
- Example: Only data science team can access, not marketing
- Effort: 1 week
- Cost: Minimal (IAM tools)

**Mitigation Technique 3: Audit Logging**
- Log all access and modifications to model/data
- Effort: 1-2 weeks
- Cost: Minimal

**Mitigation Technique 4: Model Versioning & Integrity**
- Track all model versions
- Ensure models can't be modified without detection
- Effort: 1-2 weeks
- Cost: Minimal

---

## Part 3: Assessment Report Structure

### Assessment Report Template (For Each AI System)

**Section 1: Executive Summary**

| Field | Example |
|-------|---------|
| AI System Name | Hiring Recommendation AI |
| Assessment Date | Q1 2026 |
| Risk Level (Current) | CRITICAL |
| Risk Level (After Mitigation) | HIGH |
| Status | REQUIRE MITIGATION |
| Recommendation | Implement bias remediation plan within 30 days |

**Section 2: AI System Information**

| Field | Value |
|-------|-------|
| System ID | CRIT-001 |
| System Type | Predictive ML (Classification) |
| Primary Owner | HR Department |
| Technical Owner | Data Science Lead |
| Status | Production (2 years) |
| Users/Impact | Used for 80% of hiring decisions |

**Section 3: Risk Scores (Pre-Assessment)**

| Dimension | Score | Justification |
|-----------|-------|---------------|
| Threat | 2 | Known bias issues in recruitment AI |
| Vulnerability | 2 | Model stored unencrypted, training data exposed |
| Impact | 3 | Consequential (hiring decisions affect careers) |
| Trust | 1 | No bias testing, unexplainable decisions |
| **Overall Risk** | **1.2 → CRITICAL** | **Escalates due to fairness & discrimination risk** |

**Section 4: Assessment Findings**

**Finding 1: CRITICAL - Gender Bias Detected**
- Assessment: Bias testing shows 15% difference in approval rates (men 70%, women 55%)
- Impact: Potential age/gender discrimination, legal liability
- Root cause: Training data biased (historical hiring was male-dominated)
- Severity: CRITICAL
- Timeline: Remediate within 30 days

**Finding 2: HIGH - Lack of Explainability**
- Assessment: No explanation provided to candidates for rejections
- Impact: Candidates can't understand why rejected, can't appeal
- Severity: HIGH
- Timeline: Remediate within 60 days

**Finding 3: MEDIUM - Model Drift Not Monitored**
- Assessment: No monitoring of model accuracy over time
- Impact: Performance may degrade without detection
- Severity: MEDIUM
- Timeline: Implement monitoring within 90 days

**Finding 4: MEDIUM - Training Data Dated**
- Assessment: Model trained on 2021 data (4 years old)
- Impact: May not reflect current candidate population
- Severity: MEDIUM
- Timeline: Retrain on 2025 data within 90 days

**Section 5: Mitigation Plan**

| Finding | Mitigation Technique | Effort | Timeline | Owner |
|---------|---------------------|--------|----------|-------|
| Gender bias | Retrain on balanced dataset | 2-3 weeks | 30 days | Data Science |
| Lack of explainability | Extract decision rules + provide explanations | 2-3 weeks | 60 days | Data Science |
| Model drift | Implement performance monitoring | 1-2 weeks | 30 days | MLOps |
| Dated training data | Retrain on current data | 2-3 weeks | 90 days | Data Science |

**Section 6: Control Assessment**

| Control | Status | Evidence | Notes |
|---------|--------|----------|-------|
| Bias Testing | NOT IMPLEMENTED | None | REQUIRED |
| Explainability | PARTIAL | Feature importance calculated but not communicated | Needs user-facing explanations |
| Performance Monitoring | NOT IMPLEMENTED | None | REQUIRED |
| Human Oversight | IMPLEMENTED | HR review all decisions | Adequate, but slow |
| Data Security | IMPLEMENTED | Encrypted, access controlled | Adequate |

**Section 7: Risk Score After Mitigation**

| Dimension | Current | After Mitigation | Justification |
|-----------|---------|------------------|---------------|
| Threat | 2 | 1 | Bias remediation reduces threat |
| Vulnerability | 2 | 2 | Unchanged (security adequate) |
| Impact | 3 | 3 | Unchanged (still consequential) |
| Trust | 1 | 2 | Explainability + monitoring improve trust |
| **Overall Risk** | **CRITICAL** | **HIGH (1.6)** | **Risk reduced but remains HIGH** |

**Section 8: Monitoring Plan (Post-Remediation)**

- Frequency: Monthly
- Type: Bias metrics monitoring + performance monitoring
- Next Assessment: Q2 2026 (after mitigation implemented)
- Escalation Contact: Chief Risk Officer

**Section 9: Approval & Sign-Off**

- Assessed by: Risk Assessment Team
- Reviewed by: Chief Risk Officer
- Approved by: Chief AI Officer
- Date: Q1 2026

---

## Part 4: Remediation Tracking

### When AI System Gets a Finding

**Step 1: Document the Finding** (Same Day)
- Document: What was found, severity, impact
- Example: "Gender bias found - 15% approval gap between men/women"
- Severity: CRITICAL/HIGH/MEDIUM/LOW

**Step 2: Create Remediation Plan** (Within 5 Days)
- Mitigation technique selected
- Timeline: When will be fixed?
- Owner: Who is responsible?
- Effort estimate: How long will it take?

**Step 3: Remediation Execution** (Ongoing)
- Development team implements mitigation
- Progress tracking: Weekly status updates
- Testing: Verify mitigation works

**Step 4: Verification Testing** (After Implementation)
- Re-test for bias/performance/adversarial robustness
- Verify finding is resolved
- Document testing results

**Step 5: Close-Out** (Upon Completion)
- Mark finding as RESOLVED
- Schedule follow-up verification in 90 days
- Update risk score

**Step 6: Escalation (If Delayed)**
- If remediation misses deadline → escalate to Chief AI Officer
- If mitigation inadequate → escalate to steering committee
- If AI system refuses remediation → escalate to board

### Remediation Tracking Dashboard

| AI System | Finding | Severity | Due Date | Status | Owner | Days Remaining |
|-----------|---------|----------|----------|--------|-------|-----------------|
| Hiring AI | Gender bias | CRITICAL | 3/30/26 | IN PROGRESS | Data Science | 14 days |
| Medical Diagnosis | Lacks explainability | HIGH | 4/15/26 | NOT STARTED | Data Science | 30 days |
| LLM Chatbot | Hallucination risk | MEDIUM | 5/31/26 | NOT STARTED | AI Engineering | 76 days |
| Fraud Detection | Model drift | MEDIUM | 4/30/26 | IN PROGRESS | MLOps | 45 days |

**Actions on Dashboard:**
- OVERDUE findings: Escalate immediately
- IN PROGRESS (nearing deadline): Follow up with owner
- NOT STARTED (due within 30 days): Send reminder

---

## Part 5: Assessment Metrics & KPIs

### Completion Metrics

| Metric | Target | Owner |
|--------|--------|-------|
| CRITICAL AI assessments completed | 100% within 6 weeks | Assessment Lead |
| HIGH AI assessments completed | 100% within 12 weeks | Assessment Lead |
| MEDIUM assessments completed | 100% within 6 months | Assessment Lead |
| Assessment quality (no rework needed) | 95%+ first-time | Assessment Lead |
| Average assessment time (CRITICAL) | 4-6 weeks | Assessment Lead |

### Risk Metrics

| Metric | Target | Owner |
|--------|--------|-------|
| AI systems with acceptable risk score | 90%+ after mitigation | Chief Risk Officer |
| Findings closed within SLA | 100% | Risk Operations |
| CRITICAL findings remediated within 30 days | 100% | AI Governance Team |
| HIGH findings remediated within 60 days | 95%+ | AI Governance Team |
| Bias testing completion rate | 100% for CRITICAL/HIGH | Data Science |
| Performance monitoring implementation | 100% for CRITICAL | MLOps |

---

**Phase 3 Complete. Ready for Phase 4: AI Monitoring & Governance?**
