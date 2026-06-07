# AI Risk Management & Governance Program

## Phase 4: AI Monitoring, Continuous Compliance & Governance

**Organization:** [Enterprise / Federal Contractor]  
**Program Owner:** Chief Risk Officer & Chief AI Officer  
**Phase Duration:** Ongoing (Month 9+)  
**Key Outcome:** Continuous AI system monitoring with automated compliance tracking and re-assessment schedule  

---

## Executive Summary

Phase 4 operationalizes continuous AI governance. Rather than assessing AI systems once and forgetting about them, Phase 4 establishes ongoing monitoring to catch issues early, automatically tracks compliance status, and schedules re-assessments to ensure systems stay within acceptable risk levels.

**Key Objectives:**
1. Establish automated monitoring procedures by AI system criticality
2. Continuously track compliance against NIST AI RMF, EU AI Act, sector-specific requirements
3. Detect AI system performance degradation and bias drift early
4. Schedule and execute re-assessments at appropriate intervals
5. Escalate issues through governance committees
6. Track AI system health over time

**Key Outcomes:**
- Automated monitoring system (dashboards, alerts, escalations)
- Continuous compliance tracking (NIST AI RMF, EU AI Act, sector-specific)
- Re-assessment schedule (CRITICAL annual, HIGH biennial, MEDIUM triennial, LOW as-needed)
- Monitoring procedures by scenario (performance degradation, bias drift, data drift, hallucination)
- Escalation procedures with clear ownership
- Executive reporting on AI governance and compliance status

---

## Part 1: Monitoring Strategy by AI System Risk Level

### CRITICAL AI Systems - Continuous Monitoring

**Monitoring Frequency:** Real-time to daily

**Monitoring Methods:**

**Method 1: Real-Time Bias Monitoring (Daily)**
- Continuous measurement of demographic parity metrics
- Alert if fairness metrics degrade >2% from baseline
- Tools: Custom dashboards, MLOps monitoring
- Action: Escalate to Chief AI Officer if drift detected

**Method 2: Performance Degradation Detection (Daily)**
- Monitor model accuracy, precision, recall metrics
- Alert if overall accuracy drops >2% from baseline
- Alert if performance degrades for specific demographic groups
- Action: Investigate and remediate within 7 days

**Method 3: Data Drift Monitoring (Daily)**
- Monitor input data distribution
- Alert if data characteristics change significantly
- Example: If training data had 60% male candidates, alert if production data >70% male
- Action: Evaluate if model needs retraining

**Method 4: Model Output Anomaly Detection (Daily)**
- Monitor for unusual output patterns
- Example: If AI suddenly rejects 90% of candidates (vs. 30% baseline)
- Action: Immediate investigation and potential rollback

**Method 5: Adversarial Attack Detection (Daily)**
- Monitor for signs of adversarial manipulation
- Example: Unusual input patterns designed to fool AI
- Tools: Security monitoring, rate limiting alerts
- Action: Block suspicious requests, escalate

**Method 6: Compliance Tracking (Weekly)**
- Verify NIST AI RMF controls remain implemented
- Verify data security controls are in place
- Verify human oversight processes are being followed
- Action: Log compliance status, escalate gaps

**Method 7: Automated Fairness Audit (Monthly)**
- Full bias testing (demographic parity, equalized odds, calibration)
- Compare to Phase 3 assessment baseline
- Report any regression
- Action: Escalate if bias metrics worsen

**Method 8: Executive Health Check (Monthly)**
- Steering committee review of all CRITICAL systems
- Status: Operating normally, degraded, or at-risk
- Upcoming re-assessments
- Mitigation tracking (any open findings?)

---

### HIGH AI Systems - Frequent Monitoring

**Monitoring Frequency:** Weekly to monthly

**Monitoring Methods:**

**Method 1: Performance Monitoring (Weekly)**
- Track accuracy and key metrics
- Alert if performance drops >3% from baseline
- Tools: Automated dashboards

**Method 2: Compliance Tracking (Monthly)**
- Verify controls remain in place
- Verify monitoring is occurring
- Document compliance status

**Method 3: Fairness Audit (Quarterly)**
- Run bias testing quarterly
- Compare to baseline
- Log results

**Method 4: Executive Review (Monthly)**
- Monthly steering committee check-in
- Status updates and escalations

---

### MEDIUM AI Systems - Periodic Monitoring

**Monitoring Frequency:** Monthly to quarterly

**Monitoring Methods:**

**Method 1: Performance Review (Monthly)**
- Review accuracy metrics
- Check for significant degradation

**Method 2: Compliance Status (Quarterly)**
- Verify controls documented
- Spot-check compliance

**Method 3: Fairness Review (Semi-Annual)**
- Run bias testing twice per year
- Log results

---

### LOW AI Systems - Annual Monitoring

**Monitoring Frequency:** Quarterly to annual

**Monitoring Methods:**

**Method 1: Annual Status Check**
- Verify system still in production
- Performance acceptable
- No major issues

**Method 2: Annual Compliance Review**
- Confirm controls still in place

---

## Part 2: Continuous Compliance Tracking

### What is Continuous Compliance?

Automatically tracking whether AI systems remain compliant with applicable regulations and frameworks throughout their lifecycle (not just at initial assessment).

---

## Part 2A: NIST AI RMF Compliance Tracking

### GOVERN Function - Continuous Compliance

**Control 1.1: AI Governance Structure in Place**
- Monitor: Does governance committee meet monthly?
- Compliance Threshold: 100% of scheduled meetings conducted
- Frequency: Monthly verification
- Action: Escalate if meetings missed

**Control 1.2: AI Risk Appetite Defined**
- Monitor: Is risk appetite still documented and current?
- Compliance Threshold: Document updated annually
- Frequency: Annual review
- Action: Schedule review if overdue

**Control 1.3: AI Policies Documented**
- Monitor: Are AI policies current and being followed?
- Compliance Threshold: All policies updated within 2 years
- Frequency: Quarterly policy review
- Action: Update policies if overdue

---

## Part 2B: EU AI Act Compliance Tracking (If Applicable)

### High-Risk AI Systems Compliance

**Control: High-Risk AI Register Maintained**
- Monitor: Is master list of high-risk AI systems current?
- Compliance Threshold: All high-risk systems documented
- Frequency: Monthly verification
- Action: Update register if systems added/removed

**Control: Risk Assessment Documentation**
- Monitor: Do all high-risk systems have documented risk assessments?
- Compliance Threshold: 100% documented
- Frequency: Quarterly verification
- Action: Escalate if gap found

**Control: Human Oversight Process**
- Monitor: Is human override/appeal available for high-risk decisions?
- Compliance Threshold: 100% of high-risk systems have process
- Frequency: Semi-annual testing
- Action: Escalate if process breaks

**Control: Transparency & Documentation**
- Monitor: Are users informed about AI decisions?
- Compliance Threshold: All high-risk systems document their approach
- Frequency: Quarterly review
- Action: Update user communication if needed

---

## Part 2C: Sector-Specific Compliance Tracking (Examples)

### Healthcare AI Compliance (HIPAA/FDA)

**Control: Data Privacy Maintained**
- Monitor: Is patient data encrypted and access controlled?
- Frequency: Monthly
- Action: Escalate if controls lapse

**Control: Bias Testing for Demographics**
- Monitor: Is model tested for demographic bias regularly?
- Frequency: Quarterly
- Action: Escalate if bias testing skipped

### Financial AI Compliance (Algorithmic Accountability)

**Control: Fair Lending Practices**
- Monitor: Loan approval AI doesn't discriminate by protected class
- Frequency: Quarterly fairness audit
- Action: Escalate if bias detected

**Control: Model Documentation**
- Monitor: Decision logic documented for audit purposes
- Frequency: Annual review
- Action: Update documentation if model changed

---

## Part 3: Continuous Compliance Dashboard

### Dashboard 1: NIST AI RMF Compliance Status (Monthly)

**Key Metrics:**
- GOVERN Function: 4/4 controls compliant (100%)
- MAP Function: 8/8 systems assessed on schedule (100%)
- MEASURE Function: 24/24 systems monitored (100%)
- MANAGE Function: 3/5 remediation findings resolved (60%)

**Overall Compliance:** 35/41 controls compliant (85%)

**Actions Needed:**
- 2 CRITICAL remediation findings overdue (escalate)
- 1 HIGH system monitoring tool not yet deployed (action item)

---

### Dashboard 2: Regulation-Specific Compliance (Quarterly)

**NIST AI RMF:**
- Governance: ✅ Compliant
- Assessment: ✅ Compliant (24/24 systems)
- Monitoring: ✅ Compliant
- Management: ⚠️ Partial (remediation in progress)

**EU AI Act (If applicable):**
- High-Risk Register: ✅ Current (3 systems documented)
- Risk Assessments: ✅ Complete (3/3)
- Human Oversight: ✅ Implemented (3/3 systems)
- Documentation: ⚠️ Partial (1 system needs updated docs)

**Sector-Specific (Healthcare example):**
- HIPAA Data Privacy: ✅ Compliant
- FDA Validation: ✅ Current
- Bias Testing: ✅ Quarterly (next: Q2 2026)

---

## Part 4: Re-Assessment Schedule

### When to Re-Assess AI Systems

**CRITICAL AI Systems:**
- **Re-assessment Frequency:** Annual
- **Trigger Events:** Any major model change, control lapse, incident, regulatory requirement
- **Procedure:** Full reassessment (Phase 3 CRITICAL level)
- **Timeline:** 4-6 weeks per system
- **Example Schedule:**
  - Hiring AI: Assessed Jan 2026, next assessment: Jan 2027
  - Medical AI: Assessed Feb 2026, next assessment: Feb 2027
  - LLM Chatbot: Assessed Mar 2026, next assessment: Mar 2027

**HIGH AI Systems:**
- **Re-assessment Frequency:** Biennial (every 2 years)
- **Trigger Events:** Major model update, new version deployed, regulatory change
- **Procedure:** Comprehensive reassessment (Phase 3 HIGH level)
- **Example Schedule:**
  - Fraud Detection: Assessed Q1 2026, next assessment: Q1 2028
  - Recommendation Engine: Assessed Q2 2026, next assessment: Q2 2028

**MEDIUM AI Systems:**
- **Re-assessment Frequency:** Triennial (every 3 years)
- **Trigger Events:** Model retrain, deployment to new data, regulatory change
- **Procedure:** Streamlined reassessment (Phase 3 MEDIUM level)
- **Example Schedule:**
  - Content Moderation: Assessed Q1 2026, next assessment: Q1 2029

**LOW AI Systems:**
- **Re-assessment Frequency:** As-needed / Upon major change
- **Trigger Events:** Significant model change, new use case, regulatory requirement
- **Procedure:** Lightweight reassessment (Phase 3 LOW level)

---

## Part 4A: Re-Assessment Procedures

### Step 1: Schedule (60 Days in Advance)

- Calendar alert generated
- Contact AI system owner
- Propose reassessment date
- Request documentation updates

### Step 2: Pre-Assessment Data Collection (30 Days Before)

- Collect current system information
- Gather monitoring data from past assessment period
- Review any incidents or issues
- Document any system changes/updates

### Step 3: Conduct Reassessment (Same as Phase 3)

- Run same tests as initial assessment (bias, adversarial, performance, etc.)
- Document findings
- Compare to Phase 3 baseline

### Step 4: Score & Compare (Upon Completion)

- Calculate new risk score (Threat × Vulnerability × Impact × Trust)
- Compare to previous score
- Note improvements or deterioration
- Identify new findings

**Example Comparison:**

| Dimension | Previous | Current | Change |
|-----------|----------|---------|--------|
| Threat | 2 | 2 | ✓ Stable |
| Vulnerability | 2 | 1 | ↓ Improved (security hardened) |
| Impact | 3 | 3 | ✓ Stable |
| Trust | 1 | 2 | ↑ Improved (explainability added) |
| **Overall** | **CRITICAL (1.2)** | **HIGH (1.6)** | **↓ Improved** |

### Step 5: Update Risk Classification

- If risk improved: May reduce monitoring frequency
- If risk stayed same: Continue current monitoring
- If risk worsened: May increase monitoring, escalate

### Step 6: Report & Document

- Generate reassessment report
- Update AI system record with new risk score
- Update next reassessment date
- Schedule follow-up verification (in 90 days if findings)

---

## Part 5: Monitoring Procedures by Scenario

### Scenario 1: Model Performance Degradation Detected

**Situation:** Fairness monitoring alerts that hiring AI approval rate for women dropped from 60% to 45% (15% decline)

**Step 1: Alert (Immediate)**
- Real-time dashboard shows alert
- Auto-notification to Chief AI Officer

**Step 2: Investigation (Same Day)**
- Query recent model predictions
- Identify when degradation started (specific date/time)
- Check if recent data changed (new input distribution?)
- Verify no model was accidentally updated

**Step 3: Analysis (24 Hours)**
- Root cause analysis: Why did fairness degrade?
  - Option A: New hiring data pool (different demographics)
  - Option B: Model wasn't retrained recently (using stale patterns)
  - Option C: Buggy model update deployed
  - Option D: Adversarial manipulation (unlikely but check)

**Step 4: Decision**
- If cause is data drift: Retrain model on current data
- If cause is stale model: Schedule immediate retraining
- If cause is bug: Rollback to previous model version
- If cause is attack: Investigate and implement defenses

**Step 5: Remediation**
- Implement fix (retrain, rollback, or update)
- Re-test to verify fairness metrics recovered
- Document root cause and remediation

**Step 6: Close**
- Update monitoring dashboard
- Log incident
- Schedule follow-up verification (1 week later)

---

### Scenario 2: Bias Drift Detected During Quarterly Audit

**Situation:** Quarterly fairness audit shows medical diagnosis AI has higher false positive rate for older patients (65+) vs. younger patients

**Procedure:**
1. Document finding (bias in age discrimination)
2. Quantify impact (how many patients affected?)
3. Create remediation plan (retrain on balanced age groups)
4. Implement fix (4-week timeline)
5. Re-test to verify bias reduced
6. Escalate to governance committee
7. Schedule re-assessment (bring forward to 6 months instead of 12)

---

### Scenario 3: New Regulatory Requirement (EU AI Act Update)

**Situation:** EU AI Act expands to cover recommendation systems (currently only applied to high-risk AI); your Recommendation Engine becomes "high-risk"

**Procedure:**
1. Reclassify system from MEDIUM to HIGH risk
2. Update governance (more frequent monitoring)
3. Add compliance controls (human oversight, documentation)
4. Conduct reassessment immediately (instead of waiting for triennial)
5. Update compliance dashboard
6. Brief steering committee

---

## Part 6: Escalation Procedures

### Level 1: Operational (AI Governance Team)

| Finding | Action | Timeline |
|---------|--------|----------|
| Performance degradation (<2%) | Investigate, monitor closely | 48 hours |
| Minor compliance gap | Document, create action plan | 1 week |
| Scheduled monitoring due | Execute monitoring | Within schedule |

---

### Level 2: Steering Committee (CISO, Chief AI Officer, CRO)

| Finding | Action | Timeline |
|---------|--------|----------|
| Performance degradation (>2%) | Escalate, demand remediation plan | 7 days |
| Bias drift detected | Formal investigation, remediation required | 14 days |
| Compliance violation (regulatory) | Review, risk acceptance decision | Immediate |
| CRITICAL system at-risk | Executive review, potential model retirement | 48 hours |

---

### Level 3: Board / Executive

| Finding | Action | Timeline |
|---------|--------|----------|
| Regulatory non-compliance (fine risk) | Board notification, legal review | Immediate |
| AI system fails in production (user impact) | Executive response, business continuity | Immediate |
| Pattern of recurring issues from same system | Consider system replacement/retirement | Emergency meeting |

---

## Part 7: Monitoring Tools & Automation

### Tool 1: Bias Monitoring Dashboard

**What it does:** Continuously tracks fairness metrics by demographic group

**Setup:**
1. Connect to AI model output stream
2. Define demographic groups to monitor
3. Set fairness metric thresholds (alert if >2% drift)
4. Configure alerts (email, dashboard, Slack)

**Cost:** $10K-$50K/year (depending on volume)

**Tools:** Fiddler, WhyLabs, custom Prometheus/Grafana setup

---

### Tool 2: Performance Monitoring

**What it does:** Tracks model accuracy, drift, data quality in real-time

**Setup:**
1. Integration with model serving infrastructure
2. Define baseline performance metrics
3. Configure alerts for degradation
4. Dashboard for trending

**Cost:** Often included in MLOps platforms ($5K-$20K/year)

**Tools:** DataRobot, Fiddler, AWS SageMaker Model Monitor

---

### Tool 3: Compliance Tracking System

**What it does:** Automates compliance checklist tracking

**Setup:**
1. Create compliance matrix (controls × systems)
2. Document control owner
3. Set compliance verification frequency
4. Alert when verification due

**Cost:** $0-$10K/year (can use spreadsheet or Jira)

**Tools:** Spreadsheet (free), Jira (if have license), ServiceNow

---

### Tool 4: Re-Assessment Scheduling System

**What it does:** Automatically schedules reassessments by risk level

**Setup:**
1. List all AI systems with risk levels
2. Set reassessment frequency (annual for CRITICAL, biennial for HIGH, etc.)
3. Calendar alerts (60 days before due)
4. Tracking dashboard

**Cost:** $0-$5K/year (spreadsheet or project management tool)

**Tools:** Excel with calendar (free), Jira, Asana

---

## Part 8: Executive Reporting & KPIs

### Monthly Monitoring Dashboard (Operations)

**Key Metrics:**
- CRITICAL systems monitored on schedule: 3/3 (100%)
- HIGH systems monitored on schedule: 5/5 (100%)
- MEDIUM systems monitored on schedule: 8/8 (100%)
- Alert response time (avg): 4 hours
- Open findings remediation status: 3 in progress, 0 overdue

**Issues This Month:**
- Hiring AI fairness metric drifted 3%, remediation in progress
- Medical AI bias testing completed, all metrics within threshold
- 1 HIGH system monitoring tool deployment delayed (reschedule for next month)

---

### Quarterly Compliance Report (Board/Steering Committee)

**Compliance Status:**
- NIST AI RMF: 35/41 controls compliant (85%)
- EU AI Act: 4/4 high-risk systems compliant (100%)
- Sector-Specific: 12/12 controls compliant (100%)
- Overall: 51/57 requirements met (89%)

**Re-Assessment Status:**
- CRITICAL systems: 0/3 overdue (on schedule)
- HIGH systems: 0/5 overdue (2 upcoming next quarter)
- MEDIUM systems: 0/8 overdue (next batch in 1.5 years)
- LOW systems: No reassessments due

**Key Incidents:**
- 1 CRITICAL: Performance degradation (resolved in 7 days)
- 2 HIGH: Bias drift detected and mitigated
- 0 Regulatory violations

**Recommendations:**
- Deploy performance monitoring tool (improve detection speed)
- Advance 1 HIGH system reassessment (regulatory change imminent)

---

### Annual AI Governance Report

**Program Health:**
- 24 AI systems under monitoring
- 100% monitoring compliance
- 95% remediation compliance (1 finding overdue, escalated)
- 0 regulatory violations
- 3 systems improved risk classification

**Compliance Trends:**
- Bias detection: Decreasing (more detections in Year 1, fewer in Year 2 = controls working)
- Performance stability: Improving (fewer alerts over time)
- Governance adoption: Strong (committees meeting consistently)

**Forecast (Next 12 Months):**
- 3 CRITICAL systems due for reassessment (Q1-Q3 2027)
- 2 HIGH systems due for reassessment (Q4 2027)
- 1 new AI system expected (Autonomous system) - plan intake
- EU AI Act enforcement begins - ensure compliance ahead of deadline

---

## Part 9: Success Metrics

### Program Health Metrics

| KPI | Target | Owner |
|-----|--------|-------|
| Monitoring compliance (% systems monitored on schedule) | 100% | Risk Operations |
| Compliance verification completion rate | 100% | Governance Lead |
| Average alert response time (CRITICAL findings) | <24 hours | Chief AI Officer |
| Remediation closure rate | 100% by due date | AI Governance Team |
| Re-assessment schedule adherence | 100% | Assessment Lead |

### Governance Effectiveness Metrics

| KPI | Target | Owner |
|-----|--------|-------|
| Governance committee attendance | 80%+ | Chief AI Officer |
| Risk score improvement rate (systems with findings) | 50%+ improve after mitigation | Chief Risk Officer |
| Compliance violation incidents | 0 per year | Compliance Officer |
| Time to detect issues (avg) | <7 days | Risk Operations |
| Time to remediate (avg) | <30 days | AI Governance Team |

---

## Part 10: Continuous Improvement Cycle

### Quarterly Governance Review

1. **Review monitoring data** (Are we catching issues early?)
2. **Review compliance status** (Are systems staying compliant?)
3. **Review remediation progress** (Are findings getting fixed?)
4. **Adjust monitoring** (Do we need more frequent monitoring for some systems?)
5. **Update tools/processes** (Can we automate more?)
6. **Plan reassessments** (Which systems are due soon?)

### Annual Strategy Review

1. **Assess program effectiveness** (Did we prevent incidents?)
2. **Review compliance posture** (Do we meet all regulations?)
3. **Evaluate tools/processes** (Are they working? Do we need upgrades?)
4. **Plan next year** (New systems coming? Regulatory changes?)
5. **Update governance** (Do governance structures still work?)

---

**Phase 4 Complete. This concludes the 4-phase AI Risk Management Program.**
