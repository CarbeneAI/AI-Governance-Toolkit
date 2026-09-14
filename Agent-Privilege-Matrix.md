# Agent Privilege Matrix

**A one-page control layer for the agents your employees are already running.**

Part of the [AI Governance Toolkit](README.md) from [CarbeneAI](https://carbene.ai). Pairs with Section 10 (Agentic AI Governance) of the [Framework Template](AI-Governance-Framework-Template.md).

## Why this exists

Employees are spinning up agents in Claude Code, Cursor, and Codex that touch production data. None of it shows up in a procurement record, because nobody procured it. You cannot write an enforceable policy for agents you have not named, and you cannot grant privilege you have not scoped. This matrix is the smallest artifact that turns an ungoverned agent into a governed one: one row per agent, filled in before it runs.

The rule is the same one that governs every access decision: least privilege, named owner, tested stop. An agent is not special because it is AI. It is special because it acts at machine speed without waiting for your review.

## The matrix

Copy this table. One row per agent in production and one per agent someone is about to ship. The rows you cannot complete are your real exposure, ranked.

| Agent ID | Identity (credential + owner) | Data class allowed | Allowed actions | Human-in-the-loop trigger | Stop control | Alert on new resource |
|---|---|---|---|---|---|---|
| `svc-agent-billing-01` | Workload identity, owned by [NAME] | Internal, non-PHI | Read staging DB; write ticket queue | Any write to production | Revoke token via IdP | Yes: token to new host or DB |
| `dev-agent-cursor-*` | Developer's own identity | Source + non-prod data only | Read repo; run tests; open PR | Merge to main; deploy | Kill session; rotate key | Yes: reach outside repo scope |
| `svc-agent-scribe-01` | Workload identity, owned by [NAME] | PHI (see BAA) | Transcribe; write to EHR draft | Any send to patient or payer | Disable ingest endpoint | Yes: new PHI store or vendor |

## The five columns that matter

1. **Identity.** Every agent has its own credential and a named human owner of that credential. No shared service accounts standing in for three agents. When the token authenticates somewhere new, the identity owner gets the alert and decides if it is expected.

2. **Data class.** Name the highest data class the agent can reach: public, internal, confidential, regulated (PHI, PCI, CJIS, contractual). This is the blast radius on the data side. If an agent can read regulated data, its data owner set that boundary and can defend it.

3. **Allowed actions.** Scope by blast radius, not by feature. Three tiers is enough to start:
   - **Read-only** on a named scope.
   - **Write to non-production** (staging, drafts, ticket queues).
   - **Write to production / send external / move value** — always requires a named human in the loop.

4. **Human-in-the-loop trigger.** State the exact line the agent cannot cross alone. Vague triggers ("sensitive actions") are not enforceable. "Any write to the production customer table" is.

5. **Stop control.** How you stop this specific agent, tested, with a named owner and a known time-to-stop. Revoke the token, disable the endpoint, kill the session. An untested stop control is a hope, not a control.

## Wire it to detection

The matrix is a policy. The alert is the enforcement. The trigger event worth catching first: **an agent token authenticating to a resource it has never touched before.** That is the earliest signal that an agent has exceeded its scope, whether by prompt injection, misconfiguration, or a developer widening its reach without telling anyone.

If you run [Wazuh](https://wazuh.com) or [Specter](https://github.com/CarbeneAI/Specter), express it as a first-seen rule keyed on the agent's workload identity:

```
# Pseudocode for a first-seen-resource alert on an agent identity
IF auth.principal IN known_agent_identities
AND (auth.target_resource, auth.principal) NOT IN baseline_30d
THEN raise("agent-scope-expansion", severity=high, owner=identity_owner(auth.principal))
```

The baseline is the set of (identity, resource) pairs the agent used in a clean 30-day window. Anything new is either a legitimate scope change that should have updated this matrix, or an incident. Both are worth a human looking.

## How to run it

1. **Visibility first.** List the agents actually running before you write a line of policy. Ask developers what they have wired up in Claude Code, Cursor, and Codex. Amnesty, not audit.
2. **Fill the matrix.** One row each. Flag every row you cannot complete.
3. **Wire the first-seen alert** to your SIEM, keyed to the identity owner.
4. **Review on change,** not on a calendar. A new data class or a new action tier updates the row and re-triggers owner sign-off.

This is not legal advice, and it is not a finished policy. It is the starting point that lets the rest of your governance program bind to something real. The judgment to adapt it to your risk and regulatory reality is the conversation worth having. More at [carbene.ai](https://carbene.ai).
