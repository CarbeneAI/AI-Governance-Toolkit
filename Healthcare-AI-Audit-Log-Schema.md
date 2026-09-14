# Healthcare AI Audit Log Schema

**Build the AI audit trail now, before anyone asks for it.**

Part of the [AI Governance Toolkit](README.md) from [CarbeneAI](https://carbene.ai). For health-tech CTOs shipping ambient scribes, coding assistants, patient-messaging summarizers, and any AI feature that touches PHI.

## Why now

The demand for an AI audit trail arrives in one of three ways: a health-system customer's security review, an OCR inquiry after an incident, or your own board asking who saw what. In all three, the answer "we log the API calls" is not enough. You need a per-inference record that ties a model output to the PHI it touched, the human who was accountable, and the vendor relationship that made it lawful.

The vendors that build this before they are asked win the security review instead of scrambling through it. This schema is the evidence pack, built vendor-side. It is not a hospital membership and it is not legal advice. Have counsel and your privacy officer review it against your BAAs.

## The schema

One record per inference (or per agent action). Store immutably, retain per your BAA and state law, and make it queryable by patient, by model, and by time window.

```json
{
  "event_id": "uuid-v4",
  "event_time": "2026-09-14T14:22:07Z",
  "event_type": "inference | agent_action | human_review",

  "actor": {
    "type": "user | agent | service",
    "id": "clinician-4821 | svc-agent-scribe-01",
    "on_behalf_of": "clinician-4821",
    "role": "physician | scribe_agent | billing"
  },

  "model": {
    "provider": "anthropic | openai | internal",
    "name": "claude-x.y",
    "version": "2026-08-01",
    "deployment": "vendor-baa-covered | on-prem | patient-consented",
    "hosted_by": "vendor | cloud-baa | local"
  },

  "phi": {
    "touched": true,
    "classes": ["demographics", "clinical_note", "diagnosis", "medication", "insurance"],
    "patient_ref": "tokenized-patient-id",
    "encounter_ref": "tokenized-encounter-id",
    "minimum_necessary_justification": "ambient documentation for active encounter",
    "input_hash": "sha256-of-redacted-input",
    "output_hash": "sha256-of-output"
  },

  "vendor": {
    "baa_on_file": true,
    "baa_ref": "BAA-2026-0142",
    "subprocessor": "cloud-region-us",
    "data_residency": "US",
    "training_use": "excluded_by_contract"
  },

  "human_review": {
    "required": true,
    "action_tier": "draft_only | write_ehr | send_external",
    "reviewer_id": "clinician-4821 | null",
    "reviewed_time": "2026-09-14T14:24:10Z | null",
    "decision": "accepted | edited | rejected | pending",
    "edit_distance": 0.12
  },

  "outcome": {
    "action_taken": "wrote_ehr_draft",
    "destination": "ehr-note-draft:enc-9931",
    "reversible": true,
    "stop_control_available": "disable_ingest_endpoint"
  },

  "integrity": {
    "prev_event_hash": "sha256-of-previous-record",
    "record_hash": "sha256-of-this-record"
  }
}
```

## The fields that carry the weight

- **`actor.on_behalf_of`** — When an agent acts, whose clinical authority is it acting under? A scribe agent with no accountable human behind it is a finding.
- **`phi.classes` + `minimum_necessary`** — HIPAA's minimum-necessary standard is a per-use question. Record the classes touched and the justification so you can answer it after the fact instead of guessing.
- **`phi.input_hash` / `output_hash`** — Hash, do not store, the raw PHI in the audit log itself. The hashes prove what was processed without turning your audit trail into a second copy of the record set to protect.
- **`vendor.baa_ref` + `training_use`** — Ties the inference to the BAA that made it lawful and records the contractual bar on training use. This is the field a health-system security review is really asking about.
- **`human_review.decision` + `edit_distance`** — Distinguishes "a human accepted this verbatim" from "a human rewrote it." Over time, `edit_distance` trending toward zero on a high-tier action is a signal that review has become rubber-stamping.
- **`integrity.prev_event_hash`** — Chain each record to the last so the log is tamper-evident. An audit trail you can silently edit is not evidence.

## Minimum viable version

If the full schema is more than you can ship this quarter, the non-negotiable core is: `event_time`, `actor` + `on_behalf_of`, `model` + `deployment`, `phi.classes` + `patient_ref`, `vendor.baa_ref`, and `human_review.decision`. Those six answer the six questions every reviewer and every regulator asks: when, who, which model, what PHI, under what contract, and who checked it.

## How health-tech CTOs use this

1. Emit one record per inference from the service that calls the model, not from the client.
2. Store it in a write-once path (append-only table, object store with retention lock, or a WORM-configured log).
3. Make it queryable by `patient_ref` so you can produce a per-patient AI history on request.
4. Alarm on the gaps: a `write_ehr` or `send_external` action with `human_review.decision == "pending"` past a threshold is an agent acting unreviewed.

Build this before the security review, not during it. The judgment to map it to your specific BAAs, EHR, and state law is the conversation worth having. More at [carbene.ai](https://carbene.ai).
