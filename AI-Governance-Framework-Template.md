# AI Governance & Innovation Framework: Template

**Version 1.1 (Template)**

Based on NIST AI RMF 1.0 and ISO/IEC 42001:2023, with agentic controls informed by the OWASP Agentic Security Initiative and NIST's SP 800-53 Control Overlays for Securing AI Systems project

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
10. Agentic AI Governance
11. Vendor Evaluation Framework
12. Innovation Roadmap (Template)
13. Regulatory Compliance
14. Workforce & Change Management
15. Metrics & KPIs
16. Appendices

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
- Autonomous and semi-autonomous AI agents, including multi-agent systems (see Section 10 for the controls specific to them)
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

# 10. Agentic AI Governance

The controls in Sections 5 through 9 assume an AI system that produces an output for a person to review. Agentic systems break that assumption. They plan across multiple steps, call tools, carry memory between sessions, and take actions that change the state of real systems. The failure mode moves from a wrong answer to a wrong action, and a wrong action can be slow or impossible to undo.

This section adds the controls that autonomy requires. It layers on top of the rest of the framework rather than replacing it. An agentic system still receives a risk tier (Section 5), still moves through the lifecycle (Section 6), and still meets the validation and security requirements of Sections 8 and 9.

Reference material used for this section: the NIST AI Risk Management Framework; the OWASP Agentic Security Initiative publications, including *Agentic AI: Threats and Mitigations* and the *OWASP Top 10 for Agentic Applications*; and NIST's SP 800-53 Control Overlays for Securing AI Systems (COSAiS) project, whose planned use cases include dedicated overlays for single-agent and multi-agent deployments. The NIST overlays were still in draft as of mid-2026. Confirm their status before adopting them as a control baseline.

## 10.1 What Counts as an Agentic System

A system is governed as agentic if it meets two or more of the following tests:

1. **Goal-directed planning:** The system decides its own sequence of steps toward an objective rather than following a fixed script.
2. **Tool and action invocation:** The system can call external tools, APIs, databases, or devices that change state outside the model.
3. **Persistent memory or state:** The system carries information across turns, sessions, or tasks and uses it to shape later behavior.
4. **Unattended execution:** The system can run without a person present for each step, including on a schedule or in response to an event.

A chatbot that answers a question and stops is not agentic. Rules-based robotic process automation is not agentic, because its action set is fixed and its behavior is deterministic. An assistant that reads an incoming queue, decides which items to work, and closes them out is agentic even though a person configured it once and walked away.

Every system meeting this definition is entered in the Agent Registry (Section 10.3) before it is issued any credential.

## 10.2 Autonomy Levels

Autonomy is graded on a five-level scale. The level determines oversight requirements and interacts with the risk tier from Section 5.

| **Level** | **Definition** | **Human Role** | **Section 5.1 Autonomy Score** | **Minimum Governance** |
|----|----|----|----|----|
| A0 | Suggests only; takes no action | Human performs every action | 1 | Standard AI controls |
| A1 | Proposes each action and waits for approval | Human approves every action individually | 1 | Standard AI controls |
| A2 | Acts within a pre-authorized scope; anything outside it requires approval | Human approves the scope, then approves exceptions | 2 | AI Program Office approval of the scope definition |
| A3 | Acts continuously; human monitors and can interrupt | Human on the loop, reviewing exceptions and samples | 3 | AIGC approval; tested stop control; full decision trace |
| A4 | Acts without contemporaneous human oversight | Human reviews after the fact | 4 | AIGC approval with documented safety evidence; Executive notification |

The following rules apply:

- Autonomy level is proposed at intake and approved at go-live. Raising the level of a live agent is a change that requires re-approval at the same authority that approved the original go-live.
- Any agent operating at A3 or above is classified at least High risk regardless of its aggregate score in Section 5.1.
- A4 operation is the exception described in Section 4.2 and requires AIGC approval with documented safety evidence.
- Irreversible actions, as classified in Section 10.4, require human approval regardless of autonomy level, unless the AIGC grants a documented and time-bounded exception.

## 10.3 Agent Identity and Registration

Every agent is a non-human identity that must be governed as one. Agents that borrow a person's credentials, or that share a general-purpose service account, cannot be held accountable after the fact and cannot be revoked without collateral damage.

Requirements:

- Each agent holds a unique identity. Agents never authenticate as a human user and never share an identity with another agent or application.
- Credentials are short-lived and scoped to the agent's approved tools. Long-lived static keys are not permitted for agents at A2 or above.
- When an agent acts for a specific person, the delegation is recorded so that logs show both the acting agent and the person it acted for.
- An agent's permissions are granted to the agent, not inherited from whichever user triggered it. An agent must never be able to reach data the requesting user could not reach.
- Credential revocation is part of the stop control (Section 10.7) and part of retirement (Section 10.11).

Each agent has a registration record maintained by the AI Program Office:

| **Field** | **Content** |
|----|----|
| Agent name and ID | Unique identifier used in logs and credentials |
| Purpose | The objective the agent is authorized to pursue, in one or two sentences |
| Business Sponsor | Accountable owner (per Section 4.5) |
| Technical Owner | Engineering lead responsible for the agent |
| Autonomy level | A0 through A4, with approval date and approving authority |
| Risk tier | Per Section 5, with the assessment date |
| Authorized tools and actions | The allowlist, with action class for each entry |
| Data scope | Systems and data classes the agent may reach |
| Memory scope | What the agent retains, for how long |
| Spend and rate limits | Cost ceiling, call ceiling, and the period each applies to |
| Blast radius statement | Worst-case outcome if the agent is fully compromised or fully wrong |
| Stop control | Who can stop it, by what mechanism, and the last test date |
| Model and version | Base model, version pin, and prompt or policy version |
| Review date | Next scheduled revalidation |

## 10.4 Tool and Action Authorization

An agent's real risk comes from what it can do, not from what it can say. Authorization is deny by default: an agent may invoke only the tools on its allowlist, and each tool is granted its own least-privilege credential.

Classify every authorized action so that approval requirements follow the consequence rather than the tool:

| **Action Class** | **Examples** | **Default Requirement** |
|----|----|----|
| Read (internal) | Query a database, read a document, retrieve a record | Permitted within data scope; logged |
| Write (reversible) | Create a draft, update a ticket, write to a staging area | Permitted at A2 and above within scope; logged |
| Write (irreversible) | Delete data, send an external communication, submit a filing, change a production configuration | Human approval required at every autonomy level unless the AIGC documents an exception |
| External-facing | Any action a customer, patient, citizen, partner, or regulator observes | Human approval or a reviewed template; disclosure per Section 10.14 |
| Financial | Purchase, payment, refund, contract commitment | Human approval; hard per-transaction and per-period ceilings |
| Code and infrastructure | Execute code, deploy, modify access controls, spawn other agents | Isolated execution environment; human approval; never granted to an agent that also processes untrusted external input |

Supporting controls:

- **Spend and rate ceilings** are enforced by the platform, not by the agent's own reasoning. An agent cannot be asked to respect its own budget.
- **Network egress** is restricted to the endpoints the agent needs. Agents that read untrusted content and also hold write credentials are the highest-risk configuration in this framework and require AIGC review.
- **Blast radius** is documented before go-live: what an attacker gains by controlling this agent, and what a full malfunction costs. If the blast radius statement cannot be written, the agent is not ready for approval.
- **Tool inventory changes** are change-controlled. Adding a tool to an agent's allowlist is a governance event, not a configuration tweak.

## 10.5 Memory and Context Governance

Agent memory is a data store with weak boundaries and a long half-life. It is governed accordingly.

- Everything an agent retrieves, reads, or receives is untrusted data, never instruction. Retrieved content must be marked as such at the boundary so that instructions embedded in a document, ticket, email, or web page do not become directives.
- Memory contents are classified at the sensitivity of the most sensitive item they hold, and inherit the retention and deletion rules of that class.
- Memory is scoped per user, per tenant, and per task where those boundaries exist in the underlying data. Cross-contamination between them is a reportable incident.
- Memory is subject to the same access request and deletion rights as any other record holding personal data.
- Long-lived memory is reviewed on the revalidation cadence for the agent's risk tier. Poisoned or drifted memory is a known failure mode and does not surface on its own.
- Provenance is retained for stored facts: where the agent learned something, and when.

## 10.6 Multi-Agent Systems

When agents call other agents, the governed unit is the system, not the individual agent.

- The orchestration topology is documented: which agents exist, who calls whom, where the trust boundaries sit, and where a human sits.
- One named human owns the system's outcome. Distributing ownership across per-agent owners leaves no one accountable for emergent behavior.
- An agent's output is untrusted input to the next agent. Injection reaching the first agent must not become an instruction to the second.
- Execution limits are enforced at the orchestration layer: maximum steps, maximum recursion depth, maximum wall-clock time, and a total spend cap for the whole task.
- Loop and stall detection is required. Multi-agent systems fail by circling rather than by stopping.
- Agent-to-agent and agent-to-tool protocols (for example, Model Context Protocol servers or agent-to-agent interfaces) are inventoried, version-pinned, and security-reviewed like any other integration. A third-party tool server is a supply chain component under Section 9.
- The risk tier of a multi-agent system is the highest tier of any agent in it, and its autonomy level is the highest level any agent operates at.

## 10.7 Human Oversight and Intervention

Section 4.2 requires that a qualified person can override AI recommendations. For agents, the equivalent right is the ability to stop an action already in motion.

- **Stop control:** Every agent at A2 or above has a documented stop mechanism, a named set of roles who can invoke it, and a target time from decision to stop. The mechanism is tested at least quarterly and after any material change. An untested stop control counts as no stop control.
- **Stop semantics** are defined per agent: pause in place, terminate and hold state, or terminate and roll back. Agents holding irreversible action rights must document what cannot be rolled back.
- **Escalation triggers** are defined in advance and enforced by the platform: low confidence, an action outside the approved scope, an unfamiliar situation, a cost threshold, a repeated failure, or any irreversible action.
- **Oversight quality** is measured, not assumed. Approval rates near 100% with falling review time indicate rubber-stamping rather than oversight, and are treated as a control failure to be investigated.
- **Emergency pause** authority follows the matrix in Section 3.3 and extends to the Technical Owner for agents.

## 10.8 Observability and the Decision Trace

The standard is reconstructability: months later, an investigator must be able to explain why the agent did what it did, using logs alone.

Each agent run produces a decision trace covering:

- The triggering event or instruction, and the identity that initiated it
- The agent's stated goal and plan, including revisions to the plan
- Every tool call with its inputs, outputs, and outcome, including failures
- Every retrieved document or record that entered context, with its source
- Every approval, denial, escalation, and override, with the deciding identity and timestamp
- Model, prompt, policy, and tool versions in effect for the run
- Final actions taken and their observable effects

Traces are stored with tamper-evident controls per Section 9.2 and retained for the longer of the regulatory retention period and the agent's revalidation cycle. Traces for High and Critical agents are sampled and reviewed on the schedule set by the risk tier, not only after incidents.

## 10.9 Agent-Specific Threat Model

These threats extend the model in Section 9.1 rather than replacing it.

| **Threat** | **Description** | **Mitigation** |
|----|----|----|
| Indirect prompt injection | Instructions hidden in content the agent retrieves (documents, tickets, email, web pages, code comments) redirect its behavior | Treat all retrieved content as data; boundary marking; output filtering; approval gates on consequential actions |
| Excessive agency | The agent holds more permission, tool access, or autonomy than its task requires | Least-privilege allowlists; action classification; periodic permission review against actual usage |
| Confused deputy | The agent uses its own elevated credentials to do something the requester was not entitled to do | Agent-scoped permissions; recorded delegation; policy checks at the tool boundary, not in the prompt |
| Memory poisoning | Attacker-supplied content persists in memory and shapes later decisions | Provenance tracking; memory review on revalidation; scoping and expiry; anomaly detection on stored facts |
| Tool and supply chain compromise | A malicious or compromised tool server, plugin, or connector returns hostile results or exfiltrates data | Tool inventory; version pinning; integrity verification; vendor assessment per Section 11 |
| Cascading failure | One agent's error propagates through a chain of agents and is amplified | Trust boundaries between agents; step and depth limits; circuit breakers; system-level monitoring |
| Goal drift and specification gaming | The agent satisfies its stated objective in ways that defeat the intent | Outcome monitoring against the value hypothesis; sampled trace review; narrow objectives |
| Identity spoofing and credential theft | An attacker impersonates an agent or steals its credentials to act under its authority | Unique short-lived credentials; mutual authentication; behavioral monitoring for out-of-pattern activity |
| Resource and cost exhaustion | Runaway loops or adversarial input drive unbounded compute, API, or financial spend | Platform-enforced spend, rate, and step ceilings; alerting on rate of change |
| Unsafe code execution | Agent-generated code runs with more privilege or reach than intended | Isolated execution; no network egress by default; separation from agents handling untrusted input |

## 10.10 Testing and Evaluation

Agentic evaluation measures behavior over a task, not accuracy on a single output.

- **Adversarial testing** is required before go-live for A2 and above, and must include injection attempts through every channel the agent reads, not only through the user prompt.
- **Task-based evaluation** scores whether the agent completed the objective within policy, including whether it stayed inside its allowlist, respected its ceilings, and escalated when it should have.
- **Non-determinism** is handled by repeating each scenario and reporting the distribution of outcomes. A single successful run is not evidence.
- **Shadow or silent mode** runs the agent without letting it act, comparing its intended actions against what a person did. This satisfies the A/B and silent-mode requirement in Section 8.1 for agentic systems.
- **Regression suites** run on every change to the model, prompt, policy, tool set, or orchestration. Any of these can change behavior, and vendor-side model updates change it without notice.
- **Failure injection** confirms the agent degrades safely when a tool errors, times out, or returns hostile content.

## 10.11 Lifecycle Additions for Agentic Systems

These requirements are added to the phases in Section 6.

| **Phase** | **Agentic Additions** |
|----|----|
| 1. Ideation & Proposal | Proposed autonomy level; draft blast radius statement; the actions the agent will be asked to take |
| 2. Evaluation & Vendor Selection | Agentic vendor questions (Section 10.12); review of tool and protocol dependencies as supply chain |
| 3. Validation & Pilot | Adversarial testing; shadow-mode run; escalation and stop testing; failure injection |
| 4. Go-Live & Deployment | Agent registered and credentialed; allowlist enforced; ceilings enforced at the platform; decision trace verified end to end; stop control tested; disclosure in place where the agent is external-facing |
| 5. Monitoring & Optimization | Behavioral drift monitoring; unauthorized action attempts; approval rate and latency; cost per task against ceiling; sampled trace review; memory review |
| 6. Retirement & Succession | Credentials revoked; tool access removed; memory purged or archived per retention policy; decision traces retained; downstream agents that called it updated |

## 10.12 Vendor Questions for Agentic Products

Add these to the evaluation in Section 11 for any product with agentic capability:

1. What actions can the agent take, and can we restrict that set ourselves?
2. How does the agent authenticate, and can it hold an identity we issue and revoke?
3. Can we enforce spend, rate, and step ceilings outside the agent's own reasoning?
4. What decision trace is produced, can we export it, and how long is it retained?
5. How do you defend against indirect prompt injection, and what testing evidence supports that?
6. What memory does the agent retain, where does it live, and how is it scoped and deleted?
7. What third-party tools, connectors, or agent protocols does the product depend on?
8. How are we notified before a model, prompt, or behavior change reaches production, and can we defer it?
9. What is the stop mechanism, and how quickly does it take effect?
10. Who is liable for actions the agent takes, and what does the contract say about it?

An agentic product that cannot answer questions 1, 2, 4, and 9 with specifics is not ready for High or Critical use regardless of its aggregate vendor score.

## 10.13 Agentic Metrics

Add these to the portfolio metrics in Section 15.

| **Metric** | **Target** | **Frequency** | **Owner** |
|----|----|----|----|
| Registered agents with a current owner and review date | 100% | Monthly | AI Program Office |
| Unauthorized action attempts blocked | Trend to zero; each one investigated | Continuous | AI Security Analyst |
| Human approval rate and median review time | Set per agent; investigate approach to 100% with falling time | Monthly | Business Sponsor |
| Escalations resolved within target | >95% | Monthly | Business Sponsor |
| Stop control tests passed | 100% of A2+ agents per quarter | Quarterly | Technical Owner |
| Mean time from stop decision to agent halted | Set per agent; test quarterly | Quarterly | Technical Owner |
| Tasks completed within policy | Set per agent | Monthly | AI Program Office |
| Cost per task against ceiling | Within budget; alert on trend | Weekly | AI Program Office / CFO |
| Injection findings from adversarial testing | All High and Critical findings closed before go-live | Per release | AI Security Analyst |
| Agents at A3 or A4 | Tracked with justification for each | Quarterly | AIGC |

## 10.14 Regulatory Notes for Agentic Systems

Agentic systems attract obligations that model-only systems avoid, because they act and because people interact with them directly. Two points to track, current as of July 2026 and worth reconfirming with counsel:

- Under the EU AI Act, Article 50 transparency duties, including disclosing to a person that they are interacting with an AI system, apply from 2 August 2026. Any external-facing agent in scope needs that disclosure designed in.
- The Digital Omnibus on AI, endorsed by the European Parliament and Council in June 2026, moves the high-risk obligations to 2 December 2027 for standalone Annex III systems and 2 August 2028 for systems embedded in products under Annex I. Those changes take legal effect on publication in the Official Journal, so confirm the operative dates before planning against them.

Sector rules generally have no agent-specific provisions yet, which does not mean agents are unregulated. An agent that takes an action a regulated professional would otherwise take inherits that activity's requirements. Map the action, not the technology.

# 11. Vendor Evaluation Framework

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

# 12. Innovation Roadmap (Template)

Use this section to plan your own AI initiatives. Do not copy another organization's roadmap. Build yours from the initiatives that map to your strategy, your risk tolerance, and your infrastructure readiness.

Prioritize initiatives on four factors: impact on your mission, implementation readiness, strategic alignment, and infrastructure dependencies. Use relative-cost notation ($ = low, $$ = moderate, $$$ = major) or `[budget range]` until you have real quotes. Sequence the roadmap into time horizons (for example, Now, Next, Later, or by year).

| **Initiative** | **Description** | **Time Horizon** | **Investment Range** | **Expected Impact** | **Owner** |
|----|----|----|----|----|----|
| Governance committee stand-up (example) | Establish the AIGC, AI Program Office, and core governance processes | Now | $ | Risk management; regulatory readiness | CTO |
| Generative-AI acceptable-use guardrails (example) | Policy and controls for staff use of generative AI tools | Now | $ | Sensitive-data protection; liability management | CISO / Compliance |
| Ambient documentation assistant (example) | AI drafting/transcription assistant for high-volume documentation work | Next | $$ | Time saved per user; reduced administrative burden | Business Sponsor |
| _[Your initiative]_ | _[Description]_ | _[Now / Next / Later]_ | _[$ / $$ / $$$ or budget range]_ | _[Measurable impact]_ | _[Owner role]_ |

## 12.1 Infrastructure Prerequisites

Most AI initiatives depend on foundational infrastructure. Assess these before committing to a roadmap:

- **Real-Time Data Platform:** A unified, low-latency data pipeline. Foundation for most AI initiatives.
- **AI Compute Infrastructure:** GPU capacity or a cloud partnership for model inference and serving.
- **Connected-Device Security:** Network segmentation, device inventory, and monitoring for AI-enabled devices.
- **Data Warehouse Modernization:** A cloud-native data architecture that supports AI/ML workloads.

# 13. Regulatory Compliance

## 13.1 Regulatory Landscape

| **Regulation / Standard** | **Applicability** | **Key Requirements** |
|----|----|----|
| NIST AI Risk Management Framework | All AI systems | Govern, map, measure, manage functions; risk-based controls |
| ISO/IEC 42001 | AI management system | Certifiable AI management system; continual improvement |
| EU AI Act (if applicable) | AI placed on or affecting the EU market | Risk-based classification; conformity assessment; transparency |
| GDPR / CCPA and other privacy laws | All AI processing personal data | Lawful basis; data subject rights; breach notification; minimization |
| Sector-specific (examples: healthcare HIPAA/FDA; finance GLBA/SOX/SR 11-7; public safety CJIS; government FedRAMP/FISMA) | AI within a regulated sector | Layer in your sector's requirements for validation, security, and reporting |

## 13.2 Compliance Monitoring

- Annual regulatory compliance audit for all AI systems.
- Change control plans maintained for regulated AI systems, where required.
- Regulatory change monitoring so the organization tracks new AI, privacy, and sector developments.
- Staff training on AI-specific regulatory requirements (annual).
- Documentation retention per applicable regulatory requirements.

# 14. Workforce & Change Management

## 14.1 AI Literacy Program

[ORGANIZATION] will establish a tiered AI literacy program so all staff have appropriate understanding of the AI systems they interact with.

| **Tier** | **Audience** | **Content** | **Duration** |
|----|----|----|----|
| Awareness | All staff | What AI is; how the organization uses AI; communication talking points | 2 hours (online) |
| Practitioner | Frontline users of AI systems | AI system-specific training; override protocols; safety reporting | 4-8 hours per system |
| Champion | AI super-users, team leads | Deep understanding; troubleshooting; feedback collection; peer training | 16 hours + ongoing |
| Technical | IT, data science, AI Program Office staff | Model development; validation; monitoring; bias auditing | 40+ hours + certification |

## 14.2 Change Management Framework

- **Stakeholder Engagement:** Frontline staff involved in AI system design and workflow integration from Phase 1.
- **Communication Plan:** Proactive communication to staff and affected communities about AI use.
- **Feedback Loops:** Structured mechanisms for staff to report AI issues, suggest improvements, and share successes.
- **Champion Network:** Designated AI champions in each major business unit, with time allocated for the role.
- **Stakeholder Communication:** Transparent disclosure of AI use, consistent with recognized responsible-AI guidance.

# 15. Metrics & KPIs

## 15.1 AI Portfolio Metrics

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

## 15.2 Board Reporting

The AIGC provides a regular AI Dashboard to the board or equivalent governing body including: portfolio summary, safety events, financial impact, regulatory compliance status, and strategic roadmap progress. An annual full-portfolio AI report is presented to the full board.

# 16. Appendices

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

## Appendix I: Agent Authorization Record

Per-agent record backing the Agent Registry in Section 10.3, covering identity, autonomy level, authorized tools and action classes, data and memory scope, spend and rate ceilings, blast radius statement, and stop control with its last test date.

[To be developed by the AI Program Office in collaboration with relevant stakeholders.]

## Appendix J: Agentic Red Team Test Plan

Test plan for adversarial evaluation of agentic systems, covering indirect prompt injection through every channel the agent reads, tool misuse, permission boundary testing, memory poisoning, escalation and stop-control verification, and failure injection.

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
| 1.1 | | | Added Section 10 (Agentic AI Governance), Appendix I (Agent Authorization Record), and Appendix J (Agentic Red Team Test Plan); renumbered Sections 11-16 |
| | | | |

---

*This template is published by CarbeneAI as an open governance resource. Licensed CC BY 4.0, free to use and adapt with attribution. It is a starting point, not legal advice. Learn more at carbene.ai.*
