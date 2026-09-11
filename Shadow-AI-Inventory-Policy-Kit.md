# Shadow AI Inventory & Policy Kit

**A starting point for finding and governing the AI your workforce already uses, before it finds you.** From [CarbeneAI](https://carbene.ai).

Recent survey data puts the problem plainly: a majority of healthcare providers and payers report employees using unauthorized AI tools, while fewer than 40% have detailed policies governing that use, and only about a third say they are prepared for AI-assisted attacks. The gap is not enthusiasm. It is the absence of a first inventory and a policy people can actually follow.

This kit is that first inventory. It pairs a one-page worksheet with the minimum policy language to make the worksheet mean something. It is grounded in the [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) Govern and Map functions and aligns with [ISO/IEC 42001:2023](https://www.iso.org/standard/81230.html). Sector-neutral, with healthcare and other regulated industries called out where the requirements differ.

## How to use it

1. Circulate the worksheet to team leads. Ask them to list every AI tool their people touch, sanctioned or not. Amnesty, not audit, on the first pass. You cannot govern what nobody will admit to.
2. Score each entry for PHI/sensitive-data exposure and whether a contract covers it.
3. Rank by risk. The high-exposure, no-contract, no-logging rows are your fire.
4. Adopt the policy statements below, adjusted to your reality.
5. Re-run quarterly. Shadow AI is a moving target, not a one-time cleanup.

---

## The Shadow AI Inventory Worksheet

One row per tool per use. Copy into a spreadsheet or print it. The columns map to NIST AI RMF outcomes so the inventory feeds a real program instead of a drawer.

| # | Column | What to capture | NIST AI RMF tie |
|---|---|---|---|
| 1 | **Tool / service** | Name and vendor (e.g. ChatGPT, Copilot, a scribe app, an internal agent) | MAP 1 |
| 2 | **Owner / team** | Who uses it and who is accountable | GOVERN 2 |
| 3 | **Purpose** | The actual task it does | MAP 1.1 |
| 4 | **Sanctioned?** | Approved / tolerated / unknown / prohibited | GOVERN 1.1 |
| 5 | **Sensitive-data touch** | None / PII / PHI / PCI / regulated-other. Does prompt or output contain it? | MAP 2.3 |
| 6 | **Contract / BAA** | Is there a signed agreement? For PHI, a Business Associate Agreement? None = red | GOVERN 6.1 |
| 7 | **Data retention & training** | Does the vendor retain inputs or train on them? Opt-out set? | MAP 3 |
| 8 | **Logging** | Is use logged anywhere you can review? | MEASURE 2 |
| 9 | **Access control** | Individual accounts, SSO, or a shared/personal login? | GOVERN 6 |
| 10 | **Kill switch** | Can you disable access today, and who can? | GOVERN 1.7 |
| 11 | **Risk rating** | High / Medium / Low, from columns 5-10 | MAP 5.1 |
| 12 | **Action** | Sanction / restrict / replace / retire / needs contract | GOVERN 1 |

### Fast risk rule

Any row that is **PHI or regulated data (col 5)** with **no contract/BAA (col 6)** or **no logging (col 8)** is **High** by default. Start there.

---

## Minimum policy statements

Adopt and adapt. Short enough that people will read them.

1. **Register before you use.** Any AI tool touching company or customer data goes on the inventory before use, not after.
2. **No regulated data in unsanctioned tools.** No PHI, PII, PCI, or confidential data into any AI tool without a signed agreement (a BAA where PHI is involved) and an approved data-handling review.
3. **Personal accounts are not work accounts.** Work AI use runs through managed identity (SSO), never a personal login.
4. **Assume retention until proven otherwise.** Treat vendor inputs as retained and possibly used for training unless the contract and settings say they are not.
5. **Every sanctioned tool has an owner and a kill switch.** Someone is accountable, and access can be revoked the same day.
6. **Report, do not hide.** Surfacing an unsanctioned tool is expected and safe. Quiet use is the risk.

---

## Where this fits

Use this before or alongside the [AI Governance Framework Template](AI-Governance-Framework-Template.md). The inventory feeds Section 6 (data governance) and Section 10 (agentic AI governance) of that template. Run the [Maturity Self-Assessment](AI-Governance-Maturity-Assessment.md) first if you want to know which dimensions are weakest.

## A note on scope

A starting point, not legal advice, and not a substitute for counsel or a formal audit. Aligns generally with NIST AI RMF and ISO 42001 as of publication. Your regulators, your contracts, and your risk tolerance decide the rest.

## License

Licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). Free to use, adapt, and redistribute, including commercially, with attribution to CarbeneAI.
