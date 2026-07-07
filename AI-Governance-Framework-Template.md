# AI Governance & Innovation Framework: Template

**Version 1.0 (Template)**

Based on NIST AI RMF 1.0 and ISO/IEC 42001:2023

## How to use this template

This is a starting point, not a finished policy. It gives any organization a working structure for governing AI without starting from a blank page.

- Search and replace `[ORGANIZATION]` with your organization's name throughout.
- Delete sections that do not apply to you, and add sections your context requires.
- Regulated sectors (healthcare, financial services, public safety, government) should layer in their domain requirements. Look for the "(example: in [sector], ...)" notes for where to do this.
- The roles, tiers, and thresholds shown are defaults. Adjust them to match your risk appetite and size.
- This template is grounded in the NIST AI Risk Management Framework and ISO/IEC 42001. It is not legal advice. Have counsel and compliance review your final version before adoption.

# Table of Contents

1. Executive Summary
2. Purpose & Scope
3. AI Governance Structure
4. AI Ethics Principles
5. Risk Classification Framework
6. AI Lifecycle Management
7. Data Governance for AI
8. High-Stakes AI Validation & Safety
9. Cybersecurity & AI
10. Vendor Evaluation Framework
11. Innovation Roadmap (Template)
12. Regulatory Compliance
13. Workforce & Change Management
14. Metrics & KPIs
15. Appendices

# 1. Executive Summary

Artificial intelligence is changing how organizations operate, at a fast pace and across every function. With the rapid growth of AI/ML products, the emergence of agentic systems, and AI moving into high-stakes decisions, [ORGANIZATION] needs a clear AI governance framework to adopt these tools safely, ethically, and effectively.

This framework establishes the organizational structure, policies, processes, and guardrails that [ORGANIZATION] uses to deploy AI across operational, customer-facing, and strategic domains. It balances the speed of innovation with safety for the people affected, regulatory compliance, and financial responsibility.

The framework is a living document, updated on a regular cadence by the AI Governance Committee, and aligned with recognized standards including the NIST AI Risk Management Framework and ISO/IEC 42001, along with any regulations specific to your sector.

## Key Objectives

- **Safety First:** Ensure all AI deployments undergo appropriate validation before production use, scaled to their risk.
- **Responsible Innovation:** Enable rapid adoption of high-value AI while maintaining ethical guardrails.
- **Regulatory Readiness:** Comply with applicable privacy, sector, and AI-specific regulations, and prepare for emerging ones.
- **Operational Excellence:** Reduce administrative burden, improve throughput, and optimize resource allocation.
- **Strategic Value:** Use AI to strengthen the organization's mission and competitive position.
- **Equity & Inclusion:** Monitor and mitigate algorithmic bias so outcomes are fair across affected groups.

# 2. Purpose & Scope

## 2.1 Purpose

This framework provides a unified approach to the governance, evaluation, deployment, monitoring, and retirement of AI systems across [ORGANIZATION]. It establishes clear accountability, standardized processes, and measurable outcomes for all AI initiatives.

## 2.2 Scope

This framework applies to all AI/ML systems within [ORGANIZATION], including but not limited to:

- Decision support systems that inform or shape consequential decisions
- Autonomous and semi-autonomous AI agents (for example, workflow automation and back-office agents)
- Perception and analysis AI (image, audio, video, and sensor data)
- Natural language processing systems (drafting assistants, transcription, customer communication)
- Robotic or physical-actuation systems with AI components
- Predictive analytics and early-warning systems
- Operational AI (scheduling optimization, capacity management, supply chain)
- Research and analytics AI (matching, modeling, digital twins)
- Consumer-facing AI (portals, chatbots, remote monitoring)
- Generative AI tools used by staff for work purposes

## 2.3 Out of Scope

General-purpose IT systems without AI/ML components, traditional rules-based alerts, and standard business intelligence reporting are outside the scope of this framework unless they incorporate machine learning models.

# 3. AI Governance Structure

## 3.1 AI Governance Committee

The AI Governance Committee (AIGC) is the decision-making body responsible for all AI-related policies, approvals, and oversight at [ORGANIZATION]. The AIGC reports to executive leadership and provides regular updates to the board or equivalent governing body.

| **Role** | **Representative** | **Responsibility** |
|----|----|----|
| Chair | Chief Technology Officer (CTO) | Strategic direction, infrastructure, vendor management |
| Member | Chief Information Security Officer (CISO) | Cybersecurity, data protection, threat modeling |
| Member | Chief Compliance Officer | Regulatory compliance, audit readiness, legal risk |
| Member | General Counsel | Liability framework, contract review, intellectual property |
| Member | Chief Financial Officer (CFO) | ROI analysis, capital allocation, budget oversight |
| Member | Business Sponsor | Ownership of the business outcome and value case |
| Member | Domain / Subject-Matter Leader | Domain expertise, workflow integration, adoption |
| Member | Ethics / Fairness Lead | Bias monitoring, equity impact assessment |
| Member | Affected-Stakeholder Representative | Perspective of people affected; consent and transparency advocacy |
| Ad Hoc | Additional domain experts | Domain-specific expertise as needed |

> **Note:** Regulated sectors should add domain roles (for example, healthcare: CMO/CMIO; finance: Chief Risk Officer).

## 3.2 AI Program Office

The AI Program Office is the operational arm of the AIGC, responsible for day-to-day management of the AI portfolio. The AI Program Office is staffed within the CTO's organization and typically includes:

- **AI Program Director:** Portfolio management, project prioritization, resource allocation
- **Domain AI Specialists (2-3):** Validation, workflow design, subject-matter engagement
- **AI/ML Engineers (3-5):** Model development, integration, performance monitoring
- **Data Scientists (2-3):** Analytics, bias auditing, model evaluation
- **AI Ethics Analyst:** Ethics review, bias assessment, equity monitoring
- **AI Security Analyst:** AI-specific threat modeling, adversarial testing, model security

Scale the team to your organization's size. Smaller organizations may combine several of these roles into one or two people.

## 3.3 Decision Authority Matrix

| **Decision Type** | **Authority** | **Approval Required** |
|----|----|----|
| New AI system procurement (large / above threshold) | AIGC + Executive Leadership | Board notification |
| New AI system procurement (small / below threshold) | AIGC | CTO + Business Sponsor approval |
| High-stakes AI go-live | AIGC | Domain Leader + Ethics Lead + CTO sign-off |
| Operational AI go-live | AI Program Office | CTO approval |
| AI system retirement | AIGC | Impact assessment required |
| Emergency AI deployment pause | CTO or Business Sponsor (either) | Immediate; AIGC review within 48 hours |
| Generative AI policy updates | AIGC | Compliance + Legal review |

Set the procurement threshold at a level that fits your budget and risk tolerance.

# 4. AI Ethics Principles

[ORGANIZATION]'s AI ethics principles are grounded in widely recognized responsible-AI values (fairness, accountability, transparency, safety) and aligned with the NIST AI RMF and ISO/IEC 42001. In regulated sectors, align them with your sector's professional and ethical guidance as well.

## 4.1 Transparency & Explainability

All AI systems affecting consequential decisions must be explainable to the degree appropriate for their risk classification. Reviewers must understand what an AI system does, how it reaches its conclusions, and the confidence level of its outputs. "Black box" systems that cannot provide any degree of explainability are not permitted for high-stakes use.

## 4.2 Human Oversight & Autonomy

AI systems augment human judgment; they do not replace it. For all AI systems classified as High or Critical risk, a qualified reviewer must retain the ability to override AI recommendations. Fully autonomous decision-making without human review is prohibited except where explicitly approved by the AIGC with documented safety evidence.

## 4.3 Equity & Bias Mitigation

All AI systems must be evaluated for algorithmic bias across relevant groups including race, ethnicity, gender, age, socioeconomic status, and geographic location. Bias audits are mandatory before go-live and on a recurring basis (minimum annually). Systems must perform equitably across the full population they serve, including underserved and historically disadvantaged communities.

## 4.4 Privacy & Data Stewardship

AI systems must comply with all applicable privacy laws (for example, GDPR, CCPA, and sector rules such as HIPAA in healthcare or GLBA in finance). Data used for AI training requires appropriate consent, contractual basis, or de-identification. Data minimization principles apply: AI systems should access only the minimum data necessary for their function.

## 4.5 Accountability & Liability

Every AI system must have a designated Business Sponsor (accountable owner) and Technical Owner (IT lead). Accountability for AI-assisted decisions remains with the responsible human decision-maker. The organization maintains appropriate liability and cyber insurance coverage for AI-related incidents.

## 4.6 Beneficence & Value

AI deployments must demonstrate measurable benefit to the people affected, to staff, or to operational efficiency. AI for the sake of AI is not a valid justification. Every proposed AI system must articulate a clear value hypothesis with measurable outcomes before approval.

# 5. Risk Classification Framework

All AI systems are classified into one of four risk tiers. The risk tier determines the level of governance rigor, validation requirements, monitoring frequency, and approval authority.

| **Risk Tier** | **Definition** | **Examples** | **Governance Level** |
|----|----|----|----|
| Critical | Directly influences safety-critical or irreversible outcomes; autonomous action | Autonomous action that triggers real-world effects; physical-actuation control; automated high-consequence decisions | AIGC + Executive + Board notification; continuous monitoring; quarterly revalidation |
| High | Significantly influences consequential decisions; AI-generated content enters the official record | Ambient drafting; diagnostic or classification AI; AI agents in core workflows | AIGC approval; Domain Leader sign-off; monthly performance review; semi-annual revalidation |
| Medium | Supports operational decisions; indirect impact on individuals | Scheduling optimization; supply chain AI; back-office automation; inventory prediction | AI Program Office approval; CTO sign-off; quarterly performance review; annual revalidation |
| Low | Administrative; no impact on individuals; no sensitive data | Facilities energy optimization; internal content drafting; low-risk automation | AI Program Office approval; standard IT change management; annual review |

## 5.1 Risk Assessment Criteria

Each AI system is scored across six dimensions to determine its risk tier:

| **Dimension** | **Low (1)** | **Medium (2)** | **High (3)** | **Critical (4)** |
|----|----|----|----|----|
| Impact on Individuals | No direct interaction | Indirect support | Directly informs decisions about people | Autonomous decisions about people |
| Data Sensitivity | No sensitive data | Aggregated / de-identified | Individual sensitive data | Highly sensitive data (for example, biometric, genomic, financial) |
| Autonomy Level | Human-in-the-loop always | Human reviews before action | Human reviews exceptions only | Fully autonomous |
| Reversibility | Easily reversed | Reversible with effort | Partially reversible | Irreversible outcomes possible |
| Population Scale | Small (few affected) | Moderate | Large | Very large / population scale |
| Regulatory Status | No regulatory oversight | Light oversight | Regulated / cleared | Heavily regulated / novel |

Aggregate score: 6-9 = Low, 10-14 = Medium, 15-19 = High, 20-24 = Critical. Any single dimension scoring 4 automatically elevates the system to at least High risk.

# 6. AI Lifecycle Management

All AI systems at [ORGANIZATION] follow a standardized lifecycle from ideation through retirement. Each phase has defined gates, deliverables, and accountable parties.

## 6.1 Phase 1: Ideation & Proposal

- Business or operational need identified and documented
- Value hypothesis articulated with measurable outcomes
- Initial risk classification performed
- Alignment with strategic priorities confirmed
- AI Program Office intake form submitted

## 6.2 Phase 2: Evaluation & Vendor Selection

- Market landscape analysis (build vs. buy assessment)
- Vendor due diligence (independent evidence, regulatory status, bias documentation)
- Security assessment (penetration testing, data handling review)
- Integration architecture review
- Total cost of ownership analysis (multi-year)
- Reference checks with peer organizations

## 6.3 Phase 3: Validation & Pilot

- Local validation study design (with analytics or statistics support)
- Independent ethics / review board review for research-grade evaluations
- Pilot scope defined (business unit, affected population, duration)
- Baseline metrics established before AI activation
- Bias audit across the affected population
- User training curriculum developed
- Workflow integration design with frontline staff input

## 6.4 Phase 4: Go-Live & Deployment

- AIGC go-live approval obtained (per decision authority matrix)
- Go-live checklist completed (technical, operational, compliance, security)
- Monitoring dashboards operational (model performance, utilization, outcomes)
- Incident response plan documented and tested
- Staff training completed and competency verified
- Transparency and disclosure measures in place for affected individuals

## 6.5 Phase 5: Monitoring & Optimization

- Continuous performance monitoring (accuracy, drift, utilization)
- Outcome tracking against value hypothesis
- Bias monitoring (quarterly performance analysis across groups)
- User satisfaction surveys (staff and affected individuals as applicable)
- Model revalidation per risk tier schedule
- Version management for vendor model updates

## 6.6 Phase 6: Retirement & Succession

- Retirement criteria defined (performance degradation, replaced by superior system, regulatory change)
- Workflow impact assessment for retirement
- Data retention and archival per policy
- Lessons learned documented and shared
- Successor system evaluation initiated if needed

# 7. Data Governance for AI

## 7.1 Data Quality Standards

AI models are only as reliable as the data they consume. [ORGANIZATION] establishes the following data quality requirements for AI systems:

- **Completeness:** Data pipelines must achieve >95% completeness for critical fields.
- **Timeliness:** Real-time AI systems (early warning, triage) require data latency under 60 seconds.
- **Accuracy:** Source data validated against the system of record; known data quality issues documented.
- **Consistency:** Standardized coding and taxonomies enforced at ingestion (use your industry's standard coding/taxonomies; example: in healthcare, ICD-10, SNOMED CT, LOINC, RxNorm).
- **Representativeness:** Training data must reflect the population the system will serve.

## 7.2 Data Access & Consent

- All AI data access follows the minimum-necessary principle.
- Data used for model training requires either an approved research protocol or compliant de-identification.
- Vendor data sharing agreements are reviewed by Legal and the CISO before execution.
- Opt-out mechanisms are provided for AI-assisted communication systems (for example, AI-generated messages).
- Participation in any external data-sharing network is governed by a separate data governance agreement.

## 7.3 AI Training Data Provenance

Every AI system must maintain a Data Provenance Record documenting: data sources, collection dates, preprocessing steps, inclusion/exclusion criteria, known limitations, and demographic distribution. This record is maintained by the AI Program Office and reviewed during revalidation cycles.

# 8. High-Stakes AI Validation & Safety

## 8.1 Validation Requirements by Risk Tier

| **Requirement** | **Critical** | **High** | **Medium** | **Low** |
|----|----|----|----|----|
| Local validation study | Required (prospective) | Required (retro or prospective) | Recommended | Not required |
| Bias audit | Required (5+ demographics) | Required (3+ demographics) | Required (basic) | Recommended |
| Usability testing | Required (50+ users) | Required (20+ users) | Recommended | Not required |
| Independent / third-party evidence | Required | Required | Recommended | Not required |
| Failure mode analysis | Required (FMEA) | Required (basic) | Recommended | Not required |
| A/B testing or silent mode | Required (30+ days) | Required (14+ days) | Optional | Not required |
| Independent review | External reviewer required | Internal peer review | AI Program Office review | Self-certified |

## 8.2 Safety Monitoring

- **Sentinel Event Protocol:** Any AI-related adverse event triggers immediate system pause, root cause analysis within 72 hours, and AIGC review within 7 days.
- **Near-Miss Reporting:** Staff are encouraged to report AI near-misses through the existing safety reporting system with a dedicated AI category.
- **Performance Drift Detection:** Automated monitoring of model performance metrics (for example, AUC, sensitivity, specificity, precision) with alerting thresholds defined per system.
- **Override Tracking:** Reviewer overrides of AI recommendations are tracked and analyzed to detect systematic issues.

# 9. Cybersecurity & AI

AI systems introduce novel cybersecurity attack surfaces beyond traditional IT. The following security requirements apply to all AI deployments.

## 9.1 AI-Specific Threat Model

| **Threat Category** | **Description** | **Mitigation** |
|----|----|----|
| Data Poisoning | Adversarial corruption of training data | Data provenance validation; anomaly detection on training pipelines |
| Model Evasion | Crafted inputs that cause misclassification | Adversarial robustness testing; input validation |
| Model Extraction | Reverse-engineering proprietary models via API | Rate limiting; query logging; access controls |
| Prompt Injection | Manipulating LLM-based systems via crafted prompts | Input sanitization; output filtering; prompt hardening |
| Supply Chain | Compromised AI model weights or libraries | Model integrity verification; vendor security assessment |
| Connected / Edge Devices (e.g., medical IoT, OT/ICS) | Network attacks on AI-enabled connected devices | Network segmentation; device inventory; patch management |
| Data Exfiltration | Sensitive data leakage through AI model outputs or logs | Output monitoring; differential privacy; DLP controls |

## 9.2 Security Requirements

- All AI systems undergo penetration testing before production deployment.
- AI model endpoints require authentication, authorization, and encryption in transit (TLS 1.3).
- Safety-critical or physical-actuation systems run on isolated network segments with microsegmentation.
- Generative AI tools must prevent sensitive or regulated data from being transmitted to external model providers.
- AI system logs retained per your regulatory retention requirements with tamper-evident storage.
- Quarterly vulnerability assessments for all AI infrastructure.
- Incident response playbooks specific to AI system compromise.

# 10. Vendor Evaluation Framework

[ORGANIZATION] evaluates AI vendors using a standardized scorecard across seven dimensions.

| **Dimension** | **Weight** | **Key Evaluation Criteria** |
|----|----|----|
| Evidence & Efficacy | 25% | Independent / peer-reviewed evidence; regulatory clearance status; validation studies; outcome data |
| Technical Architecture | 20% | Integration with core systems; open API standards; scalability; latency |
| Security & Privacy | 15% | SOC 2 Type II; relevant security certifications; penetration test results; contract terms |
| Bias & Equity | 10% | Demographic performance data; bias testing methodology; training data transparency |
| Financial Viability | 10% | Total cost of ownership; pricing model; vendor financial stability; exit provisions |
| Implementation | 10% | Deployment timeline; training support; change management resources; peer references |
| Innovation & Roadmap | 10% | Product roadmap; R&D investment; partnership ecosystem; platform extensibility |

Vendors scoring below 70/100 aggregate are not advanced to contracting. Vendors scoring 70-80 may proceed with conditions. Vendors scoring above 80 are recommended for contracting.

# 11. Innovation Roadmap (Template)

Use this section to plan your own AI initiatives. Do not copy another organization's roadmap. Build yours from the initiatives that map to your strategy, your risk tolerance, and your infrastructure readiness.

Prioritize initiatives on four factors: impact on your mission, implementation readiness, strategic alignment, and infrastructure dependencies. Use relative-cost notation ($ = low, $$ = moderate, $$$ = major) or `[budget range]` until you have real quotes. Sequence the roadmap into time horizons (for example, Now, Next, Later, or by year).

| **Initiative** | **Description** | **Time Horizon** | **Investment Range** | **Expected Impact** | **Owner** |
|----|----|----|----|----|----|
| Governance committee stand-up (example) | Establish the AIGC, AI Program Office, and core governance processes | Now | $ | Risk management; regulatory readiness | CTO |
| Generative-AI acceptable-use guardrails (example) | Policy and controls for staff use of generative AI tools | Now | $ | Sensitive-data protection; liability management | CISO / Compliance |
| Ambient documentation assistant (example) | AI drafting/transcription assistant for high-volume documentation work | Next | $$ | Time saved per user; reduced administrative burden | Business Sponsor |
| _[Your initiative]_ | _[Description]_ | _[Now / Next / Later]_ | _[$ / $$ / $$$ or budget range]_ | _[Measurable impact]_ | _[Owner role]_ |

## 11.1 Infrastructure Prerequisites

Most AI initiatives depend on foundational infrastructure. Assess these before committing to a roadmap:

- **Real-Time Data Platform:** A unified, low-latency data pipeline. Foundation for most AI initiatives.
- **AI Compute Infrastructure:** GPU capacity or a cloud partnership for model inference and serving.
- **Connected-Device Security:** Network segmentation, device inventory, and monitoring for AI-enabled devices.
- **Data Warehouse Modernization:** A cloud-native data architecture that supports AI/ML workloads.

# 12. Regulatory Compliance

## 12.1 Regulatory Landscape

| **Regulation / Standard** | **Applicability** | **Key Requirements** |
|----|----|----|
| NIST AI Risk Management Framework | All AI systems | Govern, map, measure, manage functions; risk-based controls |
| ISO/IEC 42001 | AI management system | Certifiable AI management system; continual improvement |
| EU AI Act (if applicable) | AI placed on or affecting the EU market | Risk-based classification; conformity assessment; transparency |
| GDPR / CCPA and other privacy laws | All AI processing personal data | Lawful basis; data subject rights; breach notification; minimization |
| Sector-specific (examples: healthcare HIPAA/FDA; finance GLBA/SOX/SR 11-7; public safety CJIS; government FedRAMP/FISMA) | AI within a regulated sector | Layer in your sector's requirements for validation, security, and reporting |

## 12.2 Compliance Monitoring

- Annual regulatory compliance audit for all AI systems.
- Change control plans maintained for regulated AI systems, where required.
- Regulatory change monitoring so the organization tracks new AI, privacy, and sector developments.
- Staff training on AI-specific regulatory requirements (annual).
- Documentation retention per applicable regulatory requirements.

# 13. Workforce & Change Management

## 13.1 AI Literacy Program

[ORGANIZATION] will establish a tiered AI literacy program so all staff have appropriate understanding of the AI systems they interact with.

| **Tier** | **Audience** | **Content** | **Duration** |
|----|----|----|----|
| Awareness | All staff | What AI is; how the organization uses AI; communication talking points | 2 hours (online) |
| Practitioner | Frontline users of AI systems | AI system-specific training; override protocols; safety reporting | 4-8 hours per system |
| Champion | AI super-users, team leads | Deep understanding; troubleshooting; feedback collection; peer training | 16 hours + ongoing |
| Technical | IT, data science, AI Program Office staff | Model development; validation; monitoring; bias auditing | 40+ hours + certification |

## 13.2 Change Management Framework

- **Stakeholder Engagement:** Frontline staff involved in AI system design and workflow integration from Phase 1.
- **Communication Plan:** Proactive communication to staff and affected communities about AI use.
- **Feedback Loops:** Structured mechanisms for staff to report AI issues, suggest improvements, and share successes.
- **Champion Network:** Designated AI champions in each major business unit, with time allocated for the role.
- **Stakeholder Communication:** Transparent disclosure of AI use, consistent with recognized responsible-AI guidance.

# 14. Metrics & KPIs

## 14.1 AI Portfolio Metrics

| **Metric** | **Target** | **Frequency** | **Owner** |
|----|----|----|----|
| AI systems in production | Set per your goals | Monthly | AI Program Office |
| Time from proposal to go-live | <6 months (Medium risk) | Monthly | AI Program Office |
| High-stakes AI override rate | <15% (system-specific) | Weekly | Domain Leader |
| AI-related safety events | 0 serious; <5 near-misses/quarter | Continuous | Business Sponsor |
| Model performance degradation alerts | Resolved within 48 hours | Continuous | AI Program Office |
| Bias audit compliance | 100% of High/Critical systems | Quarterly | AI Ethics Analyst |
| Staff AI literacy completion | >90% awareness tier | Quarterly | HR / People Lead |
| Practitioner satisfaction with AI tools | >80% positive | Semi-annual | Domain Leader |
| AI-related cost savings/revenue | Track per initiative | Quarterly | CFO |
| Vendor SLA compliance | >99.5% uptime | Monthly | CTO |

## 14.2 Board Reporting

The AIGC provides a regular AI Dashboard to the board or equivalent governing body including: portfolio summary, safety events, financial impact, regulatory compliance status, and strategic roadmap progress. An annual full-portfolio AI report is presented to the full board.

# 15. Appendices

## Appendix A: AI System Intake Form

Standardized form for proposing new AI systems, including value hypothesis, risk classification, data requirements, and resource needs.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix B: Vendor Security Questionnaire

Security assessment questionnaire for AI vendors, covering data handling, model security, incident response, and compliance certifications.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix C: Validation Study Template

Template for designing local validation studies, including statistical methodology, sample size requirements, and performance metrics.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix D: Bias Audit Methodology

Step-by-step methodology for conducting algorithmic bias audits, including demographic categories, statistical tests, and reporting format.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix E: AI Incident Response Playbook

Detailed playbook for responding to AI-related incidents, from initial detection through root cause analysis and corrective action.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix F: Stakeholder AI Transparency Notice

Template notice for the people affected regarding AI use, aligned with recognized transparency guidance.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix G: Generative AI Acceptable Use Policy

Policy governing staff use of generative AI tools, including sensitive-data restrictions, approved use cases, and prohibited activities.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix H: AI Model Card Template

Standardized documentation template for each AI model, including intended use, performance characteristics, known limitations, and demographic performance data.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

# Document Approval

| **Role** | **Name** | **Signature** | **Date** |
|----|----|----|----|
| Chief Technology Officer | | | |
| Chief Information Security Officer | | | |
| Chief Compliance Officer | | | |
| General Counsel | | | |
| Chief Financial Officer | | | |

## Document History

| **Version** | **Date** | **Author** | **Changes** |
|----|----|----|----|
| 1.0 | | | Initial framework document |
| | | | |
| | | | |

---

*This template is published by CarbeneAI as an open governance resource. Licensed CC BY 4.0, free to use and adapt with attribution. It is a starting point, not legal advice. Learn more at carbene.ai.*
