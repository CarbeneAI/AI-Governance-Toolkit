# AI Governance Maturity Self-Assessment

## A 5-minute check on whether your AI is ready for what is coming next

> Built by CarbeneAI, grounded in the NIST AI Risk Management Framework (AI RMF 1.0) and ISO/IEC 42001:2023. Free to use and adapt under CC BY 4.0.

---

## Why this exists

You know your company should be doing more with AI governance. You also know that hiring a Big 4 firm to assess your maturity costs $50,000 and takes three months. Your internal team is too busy to build the assessment from scratch. And you want an honest answer in less time than it takes to drink a coffee.

That is what this is. Ten questions. Five minutes. A score that places you in one of three bands, a peer benchmark, and three concrete next steps to move up.

It is not an audit. It is a directional indicator. Use it to start a real conversation, not to satisfy a regulator.

---

## The Six Dimensions This Assessment Covers

| # | Dimension | What it measures |
|---|---|---|
| 1 | **Data Governance** | How you collect, label, mask, and retain the data your AI uses. |
| 2 | **Model Governance** | How you select, validate, and monitor the AI models you deploy. |
| 3 | **Human Oversight** | Where humans review AI outputs and where they do not. |
| 4 | **Transparency** | What you tell employees, customers, and regulators about your AI. |
| 5 | **Security** | How you protect AI systems from misuse, manipulation, and breach. |
| 6 | **Continuous Monitoring** | How you catch drift, bias, and performance degradation over time. |

---

## The 10 Questions

> **Scoring instructions.** Each question is worth 0 to 3 points. Add your scores at the end. Maximum score is 30.

### Q1. Data Governance: How is the data you feed into AI systems handled?

- [ ] **0 points.** We do not have a documented process. Whoever uses the AI provides whatever data they have.
- [ ] **1 point.** We have informal practices but no written policy.
- [ ] **2 points.** We have a documented data-handling policy, applied inconsistently across teams.
- [ ] **3 points.** We have a documented and enforced policy, including PII masking, retention limits, and explicit "do not train" agreements with our AI vendors.

### Q2. Model Governance: How do you decide which AI models or vendors to use?

- [ ] **0 points.** Whoever found the tool decided.
- [ ] **1 point.** IT or procurement reviewed the vendor at sign-up but has not revisited it.
- [ ] **2 points.** We evaluate models against documented criteria (accuracy, bias, privacy, vendor stability) at adoption.
- [ ] **3 points.** We re-evaluate annually and have a documented process for swapping models when better options ship.

### Q3. Human Oversight: How often does a human review AI-generated output before it reaches a customer or regulator?

- [ ] **0 points.** Rarely. The AI output goes out as-is.
- [ ] **1 point.** Sometimes, when the team remembers or has time.
- [ ] **2 points.** For high-stakes outputs, but not consistently.
- [ ] **3 points.** Always. Maker-checker is mandatory and audit-logged on every customer-facing output.

### Q4. Transparency: Do your customers know when they are interacting with AI?

- [ ] **0 points.** No. We do not disclose AI involvement.
- [ ] **1 point.** We disclose when asked but do not lead with it.
- [ ] **2 points.** We disclose in our terms of service.
- [ ] **3 points.** We disclose proactively at first contact and document AI involvement in our engagement letters.

### Q5. Hallucination and Accuracy Controls: How do you handle AI outputs that might be wrong?

- [ ] **0 points.** We trust the AI and assume it is right.
- [ ] **1 point.** We have informal practices for spot-checking.
- [ ] **2 points.** Critical outputs are reviewed by a subject-matter expert before they ship.
- [ ] **3 points.** Outputs use retrieval-augmented generation with source citations. Every claim is traceable to a source. Drift detection runs automatically.

### Q6. Bias and Fairness: Have you tested your AI systems for bias?

- [ ] **0 points.** No. We have not considered it.
- [ ] **1 point.** We have read about bias risk but have not done formal testing.
- [ ] **2 points.** We have done one bias audit at deployment.
- [ ] **3 points.** We test for bias at deployment and re-test annually. Results are reviewed by a named owner with authority to pause the system.

### Q7. Security: How is the data your AI processes protected?

- [ ] **0 points.** We are not sure.
- [ ] **1 point.** Standard IT controls apply but AI-specific risks are not addressed.
- [ ] **2 points.** We have controls for AI-specific risks (prompt injection, data leakage to model providers, model poisoning).
- [ ] **3 points.** Our AI system is included in our SOC 2 or ISO 27001 audit scope and we run regular AI-specific red-team testing.

### Q8. Audit Logging: Could you reconstruct what your AI did and why, six months from now?

- [ ] **0 points.** No.
- [ ] **1 point.** For some systems, partially.
- [ ] **2 points.** Yes, with effort. Logs exist but are not centralized or queryable.
- [ ] **3 points.** Every AI action is logged with inputs, outputs, model version, prompt, human approver, and timestamp. The logs are queryable and retained per a documented schedule.

### Q9. Workforce Readiness: How prepared is your team to work with AI?

- [ ] **0 points.** No formal training. People figure it out themselves.
- [ ] **1 point.** One-time training at rollout. No follow-up.
- [ ] **2 points.** Ongoing training is offered but adoption is uneven.
- [ ] **3 points.** AI literacy is part of every role's expectations. Paid learning time is built into the operating model.

### Q10. Regulatory Readiness: How current is your AI governance with the regulations that affect you?

- [ ] **0 points.** We are not tracking AI regulation.
- [ ] **1 point.** We are aware of major regulations (EU AI Act, state biometric laws) but have no active program.
- [ ] **2 points.** We have a named owner who tracks regulatory change but the process is reactive.
- [ ] **3 points.** We have an active program aligned with NIST AI RMF, ISO 42001, and the regulations specific to our industry. Reviews are scheduled, not reactive.

---

## Scoring Bands

Add up your scores from Q1 through Q10. Match your total to the band below.

### **Score 24–30: AI Native**

You are in the top tier of mid-market AI governance maturity. You have built the discipline that most companies are still trying to figure out. The next phase is staying there as the regulatory landscape evolves and as agentic AI changes what governance even means.

### **Score 12–23: AI Emergent**

You are doing real work but with gaps. Your governance program exists, but it is uneven across systems and teams. The risk is not that you have nothing. The risk is that you have something inconsistent enough that an auditor or regulator could find the weak spot. The path forward is closing the gaps, in priority order.

### **Score Under 12: At Risk**

You are exposed. Not because you are using AI badly, but because you are using AI without the controls that keep AI from going wrong. The good news is that the gap is closeable in 90 to 120 days with focused work. Most peers in your position do not realize how close they are to a regulatory or reputational incident.

---

## Personalized Next Steps

Based on the dimension where you scored lowest, focus your next 90 days on the corresponding action.

### If your lowest score was in Data Governance

1. Document your current data handling practices for AI. Even if they are informal.
2. Introduce a PII masking layer between your data sources and any AI prompt.
3. Add "do not train" clauses to every AI vendor contract on renewal.

### If your lowest score was in Model Governance

1. Inventory every AI tool currently in use. Most companies underestimate the count by 3x.
2. Document the selection criteria you would have used if you had been more deliberate.
3. Schedule annual re-evaluation against those criteria.

### If your lowest score was in Human Oversight

1. Identify your three highest-stakes AI use cases.
2. Implement a maker-checker review on each one. Log the review.
3. Expand the pattern to lower-stakes use cases over the next two quarters.

### If your lowest score was in Transparency

1. Add AI disclosure language to your customer-facing terms.
2. Update your engagement letters and proposals to identify which deliverables involve AI.
3. Train your customer-facing teams to disclose AI involvement proactively.

### If your lowest score was in Security

1. Add AI systems to your SOC 2 or ISO 27001 audit scope.
2. Run a red-team exercise focused on prompt injection and data leakage.
3. Review every AI vendor's security posture against your standard third-party assessment.

### If your lowest score was in Continuous Monitoring

1. Implement audit logging on every AI system. Inputs, outputs, model version, human approver, timestamp.
2. Schedule quarterly drift and bias reviews with a named owner.
3. Build an alert when an AI system's output volume or pattern shifts unexpectedly.

---

## What Happens Next

This assessment is a starting point, not a destination. Your score today is a snapshot. The gap between where you are and where the regulators expect you to be in 12 months is the conversation worth having.

If you would like a 30-minute working session to translate this score into a roadmap, CarbeneAI is happy to schedule one. There is no sales pitch on the call. We will look at your three lowest-scoring dimensions, talk through what your peers are doing, and leave you with a written summary you can share with your board.

**[Book a working session →](https://carbene.ai/contact)**

---

## How This Assessment Was Built

This assessment was developed through a structured, iterative process with an AI partner (Anthropic Claude): the question set was drafted, pressure-tested, and refined across three iterations, then reviewed against the NIST AI RMF and ISO 42001 for alignment.

The maturity bands are calibrated to early observations from mid-market companies in regulated industries. They will be re-calibrated as more responses come in.

---

## Trust Architecture Disclosure

In the spirit of the transparency principle this assessment measures, here is the standard CarbeneAI applies to its own tools.

- This assessment is free to run on your own. If you use a hosted version, responses are stored only if you opt in to receive a personalized report.
- Responses are never used to train any model.
- Responses are never shared with third parties.
- You can request deletion at any time.

This is the same trust architecture we apply to every client engagement. Practice what we preach.

---

## Acknowledgments

- **NIST AI RMF 1.0** for the governance framework structure
- **ISO/IEC 42001:2023** for the AI management system grounding
- **Paul Roetzer** ("The Future of Business Is AI, or Obsolete") for the Native / Emergent framing
- **Deloitte** ("Opening up to AI") for the three-pillar trust framework that informed the question set

---

*Published by CarbeneAI as an open governance resource. Licensed CC BY 4.0, free to use and adapt with attribution. It is a directional tool, not legal advice. Learn more at [carbene.ai](https://carbene.ai).*
