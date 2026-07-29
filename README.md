# AI Governance Toolkit

**Free, open AI governance templates from [CarbeneAI](https://carbene.ai).**

Most organizations know they need AI governance. What they do not have is a starting point that is not a $50,000 consulting engagement or a 200-page standard written for someone else's company. This repository is that starting point.

Two documents, both grounded in the [NIST AI Risk Management Framework (AI RMF 1.0)](https://www.nist.gov/itl/ai-risk-management-framework) and [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html). Read them, fork them, adapt them to your organization. No sign-up, no email wall.

## What's inside

| Document | Use it to |
|---|---|
| **[AI Governance Maturity Self-Assessment](AI-Governance-Maturity-Assessment.md)** | Find out where you stand in five minutes. Ten questions across six dimensions, three maturity bands, and a prioritized set of next steps. A directional indicator to start the conversation, not an audit. |
| **[AI Governance & Innovation Framework: Template](AI-Governance-Framework-Template.md)** | Stand up an actual governance program. A full framework template: governance structure, ethics principles, a four-tier risk classification, an end-to-end AI lifecycle, data governance, security threat model, agentic AI governance, vendor evaluation, regulatory mapping, workforce readiness, and metrics. Search-and-replace `[ORGANIZATION]` and delete what does not apply. |

### New in v1.1: Agentic AI Governance (Section 10)

Most AI governance material still assumes a model that returns an answer for a person to check. Agents plan, call tools, hold memory, and act. Section 10 adds the controls that autonomy actually requires: a five-level autonomy scale, agent identity and registration, tool and action authorization by blast radius, memory governance, multi-agent trust boundaries, tested stop controls, decision-trace logging, an agent-specific threat model, adversarial testing, lifecycle gates, vendor questions, and metrics. Informed by the [OWASP Agentic Security Initiative](https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/) and NIST's [Control Overlays for Securing AI Systems (COSAiS)](https://csrc.nist.gov/projects/cosais) project.

## Who this is for

Executives, boards, and operators in risk-driven environments who have to answer for how AI is used. The templates are sector-neutral, with regulated industries (healthcare, financial services, public safety, government) called out as examples where the requirements differ.

## Why we publish these

CarbeneAI is an AI security and strategy practice. These templates are not our product. They are how we show our work. The judgment behind adapting a framework to your specific risk, regulatory, and operating reality is where the real work happens, and that is the conversation worth having.

The rest of what we build in the open lives at [github.com/CarbeneAI](https://github.com/CarbeneAI) and [carbene.ai/open-source](https://carbene.ai/open-source).

## How to use

1. Start with the **Maturity Self-Assessment** to find your weakest dimensions.
2. Pull the **Framework Template** and keep the sections that match where you scored low.
3. Replace `[ORGANIZATION]` throughout, and layer in your sector's specific requirements.
4. Have the right people own it. A template does not govern anything. People do.

## A note on scope

These are starting points, not legal advice, and not a substitute for counsel or a formal audit. They reflect good practice as of publication and general alignment with NIST AI RMF and ISO 42001. Your regulators, your contracts, and your risk tolerance decide the rest.

## License

Licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). Free to use, adapt, and redistribute, including commercially, with attribution to CarbeneAI.

---

Built by CarbeneAI. Questions or want a working session? [carbene.ai/contact](https://carbene.ai/contact)
