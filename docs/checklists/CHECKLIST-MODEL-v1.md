# CHECKLIST-MODEL-v1 — Logical Checklist Model for Gate 2

**Gate 2 Correction** — Redesigned logical model. Does NOT use `Not started / In progress / Completed` as the sole inspection result. Provides proper inspection result representation (Match / Non-match / Not-evaluable), deficiency/non-compliance recording, and explicit provenance tracking (DIRECT / DERIVED / PROJECT).

No Data Model, no schema, no UI, no code, no Gate 3.

---

## Purpose

This file defines the **logical model** for Gate 2 checklists. It is not the field checklist itself; it specifies the structure that both the model and the field checklist must conform to. The model ensures:

1. Every checklist item has a stable ID and clear title.
2. Inspection results are represented as Match / Non-match / Not-evaluable — not just a progress status.
3. Each item records provenance (DIRECT from source, DERIVED from other requirements, or PROJECT decision).
4. Deficiency or non-compliance can be recorded when a Non-match result obtain.
5. Text notes and optional evidence are supported.
6. Items can be marked "Not-evaluable" when a particular visit cannot assess the requirement.
7. Source constraints and open questions are documented.

---

## Model Schema (Logical Definition)

Each checklist item conforms to the following structure. The field checklist (FIELD-CHECKLIST-v1.md) instantiates this model.

| Field | Description | Constraints |
|-------|-------------|-------------|
| **id** | Stable checklist item identifier (e.g., `CL-001`, `CL-015`) | Must be unique within the model; not reassigned per visit |
| **title** | Short, descriptive title for the checklist item | Phrase as an inspection question or subject; no technical jargon beyond source terms |
| **inspection_question** | The practical question the inspector asks during a field visit | Phrase as "Can the inspector observe/verify …?" or "Is … present/absent?" |
| **linked_dom** | Inspection domain from `INSPECTION-DOMAINS-v1.md` | One or more of DOM-01 through DOM-13; may be blank if the item spans domains |
| **linked_req** | Direct requirement from `REQUIREMENTS-v1.md` (REQ-001 to REQ-036) | May be blank if the item is DERIVED or PROJECT-only; when present, provenance must be DIRECT |
| **linked_der** | Derived requirement from `REQUIREMENTS-v1.md` (DER-01 to DER-18) | May be blank; when present, provenance must be DERIVED |
| **provenance** | Source lineage of the item | Must be one of: `DIRECT`, `DERIVED`, `PROJECT` |
| **inspection_result** | Result of the field inspection | Must be one of: `match`, `non_match`, `not_evaluable` |
| **text_notes** | Free-form notes recorded by the inspector | Used for observations, owner-deferred decisions (H1–H13), or context |
| **not_evaluable_reason** | Why the inspection result is `not_evaluable` for this visit | Free text; required when `inspection_result = not_evaluable`; e.g., "rain prevented structural observation", "committee not yet formed" |
| **deficiency_recorded** | Whether a deficiency or non-compliance was recorded as a result of this item | Boolean; `true` when `inspection_result = non_match` and a finding is documented; `false` otherwise |
| **evidence_optional** | Whether optional evidence (phone photo/file) may be attached | Boolean; always `true` in v1; evidence is **not mandatory** |
| **finding_relationship** | How the checklist response relates to a deficiency or finding when `deficiency_recorded = true` | One of: `direct_link`, `contextual`, `none`; `direct_link` when the response itself is the finding; `contextual` when it supports a finding from another item; `none` when no explicit link |
| **source_constraint** | Known ambiguity or limitation from the source documents | Free text; e.g., "source does not define 'regularity' threshold (H4)", " 'special categories' undefined (H10)" |
| **open_question** | Open implementation question if the source does not resolve how to inspect this item | Free text; references H1–H13 as appropriate; left blank if the source sufficiently defines the inspection approach |

---

## Provenance Categories

| Provenance | Meaning | When Used |
|------------|---------|-----------|
| **DIRECT** | The item originates from a DIRECT requirement (REQ-001 … REQ-036) as extracted from the source documents. | Every checklist item must declare its primary provenance as DIRECT, DERIVED, or PROJECT. If DIRECT, `linked_req` must be filled. |
| **DERIVED** | The item is derived from one or more DIRECT requirements or from DERIVED requirements (DER-01 … DER-18). It adds organizational or synthetic value but does not have a new source text. | `linked_der` may be filled; `linked_req` may be left blank or filled if the derivation chains back to a DIRECT requirement. Provenance is marked `DERIVED`. |
| **PROJECT** | The item reflects a PROJECT decision (as defined in the Gate 2 decisions: structured field checklist, text notes during inspection, optional future phone photo/file evidence, evidence not mandatory). It does **not** come from the source documents directly and is not a technical data‑model decision. | Used for items that are administrative, governance‑related, or that deliberately avoid inventing technical criteria. `linked_req` and `linked_der` MAY be left blank. |

---

## Inspection Result Representation (Key — NOT `Not started / In progress / Completed`)

Each item records **one** of the following three results after (or during) a field visit:

| Result | Meaning | When to Use |
|--------|---------|-------------|
| **match** | The observed field condition meets the requirement’s expectation (or the expected condition is present). | The inspector can confirm the requirement is being satisfied in the field. |
| **non_match** | The observed field condition does **not** meet the requirement’s expectation; a deficiency or non‑compliance is identified. | The inspector records a finding; `deficiency_recorded` should typically be `true`. |
| **not_evaluable** | The inspector **cannot** evaluate this item during the particular visit (for valid reasons). | e.g., weather prevents structural observation, committee not yet formed, platform inaccessible, source does not define how to verify. `not_evaluable_reason` must be filled. |

**Important:** `not_evaluable` is **not** a "failed" result — it simply means the inspection could not assess the item this time. Decisions about recurring evaluation are left to the project (H4, H12, etc.).

---

## Deficiency / Non-compliance Recording

When `inspection_result = non_match`, the inspector may record a deficiency or non-compliance:

- **`deficiency_recorded`**: Set to `true` if a deficiency/non-compliance is being formally recorded as a result of this item; `false` if the inspector only notes a non‑match without initiating a formal record.
- **`finding_relationship`**: Explains the relationship between the checklist response and the deficiency finding:
  - `direct_link` — The checklist item itself IS the finding (e.g., "Structural crack observed" → direct finding).
  - `contextual` — The item provides context for a finding recorded elsewhere (e.g., "No tutoring observed" → supports a broader deficiency in DER-16).
  - `none` — The non‑match is noted but no formal deficiency is recorded at this time.
- **`text_notes`**: Used to describe the observed deficiency, quoting source terms where appropriate. Do not invent technical standards or thresholds not present in the sources.

When `inspection_result = match` or `not_evaluable`, set `deficiency_recorded = false` and `finding_relationship = none`.

---

## Optional Evidence (Phone Photo / File)

- **`evidence_optional`**: Always `true` in v1. Evidence is a **PROJECT decision** — it is optional and never mandatory.
- Evidence may be attached to any item, but the absence of evidence does **not** prevent recording a `non_match` or deficiency.
- When evidence is attached, reference it in `text_notes` (e.g., "See photo attached: cracked wall, REQ-005").

---

## Source Constraints / Unresolved Questions (H1–H13)

Each item may carry a `source_constraint` field documenting known ambiguities from the source documents. These are **not** resolved as part of this model; they are recorded so that future owners (decision‑maker) can address them. Examples:

- H1: "Source does not define density or surprise protocol for inspection visits."
- H2: "Source does not specify criteria for the five workshop inspection domains."
- H3: "Source does not define how the inspector accesses 'Tasir' platform statistics."
- H4: " 'Closest deadlines' and 'specified deadlines' are undated in the source."
- H5: " 'Actual needs' for human resources allocation are not methodologically defined."
- H6: " No threshold defined for 'delayed' or 'stalled' projects."
- H7: " 'Measurable indicators' for the weekly provincial report are not defined."
- H8: " The three digital platforms (Tasir, general digital, inspection) and document upload are not technically specified."
- H9: " 'Urgency‑impact' classification grid for deficiencies is not defined."
- H10: " 'Special categories' and 'suitable conditions' for beneficiary treatment are not defined."
- H11: " Specialized domain scope (convergence/English/specializations; excellence‑center criteria) is not defined."
- H12: " Conditional membership criteria for committee meetings ('when needed') are not defined."
- H13: " Proof of maintenance and operation is not defined (what is documented is not specified)."

---

## Model Instantiation

The field checklist (`FIELD-CHECKLIST-v1.md`) instantiates this model for each of the 36 DIRECT requirements (and selected DERIVED items). Not every DIRECT requirement becomes a field‑checklist item — only those that can reasonably be observed or verified during a field inspection. Requirements that are purely governance, administrative, reporting, or coordination‑oriented are excluded from the field checklist and documented in the Coverage Review (see `FIELD-CHECKLIST-v1.md`).

---

## Change Log

| Date | Version | Author | Change |
|------|---------|--------|--------|
| — | v1.0 | — | Initial logical model from Gate 2 correction, rebuilt from main; redesign of inspection results, provenance, and coverage review |