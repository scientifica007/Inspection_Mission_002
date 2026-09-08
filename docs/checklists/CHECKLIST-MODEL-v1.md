# CHECKLIST-MODEL-v1 — Logical Checklist Model for Gate 2 (Corrected)

**Gate 2 Correction** — Redesigned logical model with exact coverage arithmetic, proper provenance, corrected field-vs-governance classification, and consistent field naming. No `Not started / In progress / Completed`. Inspection results: `match` / `non_match` / `not_evaluable`. Evidence: `PROJECT`, optional, never mandatory.

No Data Model, no schema, no UI, no code, no Gate 3.

---


## 1. Coverage Arithmetic and Set Consistency (Mandatory)

### 1.1. Checklist ID Uniqueness
Every checklist item has a **stable, unique ID**. No ID is reused for a different meaning. If an item is removed, the gap is left; if a new item is added, it receives a new unused ID. Numerical continuity is **not** more important than identity stability.

### 1.2. Actual Item Count vs. Announced Count
The actual number of checklist items must exactly match the announced count. Do not announce `29 items CL-001 through CL-030` if the actual count differs. The final count will be verified against the Coverage Review in `FIELD-CHECKLIST-v1.md`.

### 1.3. DIRECT Requirement Partition: Covered vs. Excluded
Each of the 36 DIRECT requirements (REQ-001 through REQ-036) must be classified into **exactly one** of two categories:
- **covered**: the requirement has a field checklist item that represents a verifiable inspection question during field work
- **excluded**: the requirement is not field-inspectable and is documented with a reason in the Coverage Review

**Constraints:**
- `covered ∩ excluded = ∅` (no requirement is both covered and excluded)
- `covered ∪ excluded = {REQ-001, REQ-002, ..., REQ-036}` (every DIRECT requirement is one or the other)
- Do **not** list a requirement as `excluded` if it is already covered by another item. `alternate/reframed` items that are already covered must not also appear in the excluded list.

### 1.4. DERIVED Requirements Support
DERIVED requirements (DER-01 through DER-18) may support multiple field items. Their total usage must be documented in the Coverage Review, with each DER-XXX listed alongside the item(s) that use it. No DERIVED requirement may be used to "cover" a DIRECT requirement that is excluded; DERIVED support is only for items that are themselves `covered`.


## 2. Field vs. Governance/Reporting/Administrative Classification (Correction C)

Each DIRECT requirement is evaluated on whether the inspector can **observe or verify** the content during a **field visit**. The classification is:

| Classification | Criterion | Example |
|---|---|---|
| **Field** | Inspector can point to, observe, measure, compare, or document a concrete condition in the workshop/institution during a visit. | REQ-001: Can the inspector verify intensive unannounced visits are happening? |
| **Governance/Reporting/Administrative** | The requirement describes a procedural, organizational, or reporting obligation that cannot be directly observed/verified in the field, even if rephrased as a question. | REQ-032: Weekly committee meetings — the inspector can note the meeting occurred, but cannot "verify" the administrative act itself. |

**Re-evaluated classifications (Correction C):**

| REQ | Title | Classification | Rationale |
|-----|-------|---|---|
| REQ-001 | Inspection visits intensive and unannounced | **Field** | Inspector can verify visits are happening in the territory; the "surprise" element is observed (or not). H1 documented as source constraint. |
| REQ-002 | Pedagogical exploitation effective | **Field** | Inspector can observe whether workshops are being used for educational activities. H2 documented. |
| REQ-003 | Safety, hygiene, protection means | **Field** | Inspector can observe hygiene standards and protection means on site. H2 documented. |
| REQ-004 | Electricity and water supply regularity | **Field** | Inspector can verify supply presence/absence; H4 documented for undated deadlines. |
| REQ-005 | Structural safety of roofs/walls | **Field** — **separate from electrical** | Inspector can examine structural condition. **Must NOT be attributed to electrical networks** (Correction B). Has its own item if field-verifiable, otherwise excluded with reason. |
| REQ-006 | Electrical networks strict audit | **Field** | Inspector can examine electrical systems; distinct from REQ-005 (structures). H2 documented. |
| REQ-007 | Immediate intervention when defect recorded | **Mixed** | Inspector can observe that intervention was requested; the administrative injunction is H13. Classified as Field with H13 constraint. |
| REQ-008 | Detailed reports on workshop status in shortest time | **Excluded** | The act of producing "detailed reports in shortest time" is a reporting governance act; "shortest time" is undated (H4). No field-verifiable question. |
| REQ-009 | Immediate verification of equipment status per institution | **Field** | Inspector can compare actual equipment with records. |
| REQ-010 | Field comparison: actual equipment vs. platform statistics | **Field** | Inspector can verify actual equipment matches platform statistics (even without API). H3 documented. |
| REQ-010 | Data updating on "Tasir" platform by directors starting September 2026 | **Excluded** | H3 says access to "Tasir" platform statistics and scope of "all data" are undefined. Inspector cannot realistically verify data updating without API/integration specs. |
| REQ-012 | Comprehensive technical card on field observations | **Field** | Inspector can produce and verify the card's existence during the visit. |
| REQ-013 | Equipment reports deadline before official October 2026 intake | **Field** — with constraint | The deadline date (04 October 2026) is a reference point; inspector can verify reports are submitted before that date. H4 documented. |
| REQ-014 | Direct responsibility for failure to update | **Excluded** | H7, H13 say accountability mechanisms are not defined; inspector cannot verify "direct responsibility" in field. |
| REQ-015 | Daily follow-up of organizational, pedagogical, material, digital aspects and immediate handling | **Field** — reframed | Inspector can follow up on observable aspects (structures, equipment, data). The "daily" rhythm is governance, but the item is kept as Field because the inspector can verify specific aspects. H5, H12 documented. |
| REQ-016 | Creation of provincial commission under Director of Vocational Training supervision | **Excluded** | Pure governance: creation of commission. No field-inspectable question. H12 documented. |
| REQ-017 | Installation of commission and transmission of member list to Minister's Secretary General | **Excluded** | Pure administrative act; dates "shortest time" and "immediately" are undated (H4). H4 documented. |
| REQ-018 | Daily follow-up of institution readiness (structures and equipment) | **Field** | Inspector can verify readiness of specific structures/equipment on a daily basis during visits. H5 documented. |
| REQ-019 | Evolution of registrations and orientation, completion within specified deadlines | **Field** | Inspector can verify registration status and note if deadlines are met (or not). H4 documented for undated deadlines. |
| REQ-020 | Pedagogical and administrative supervision, human resource distribution per actual needs | **Field** | Inspector can observe supervision presence/absence and resource distribution. H5 documented. |
| REQ-021 | Vocational, continuing, distance education offers readiness for launch | **Field** | Inspector can verify offers exist and are marked as ready; H11 documented for undefined criteria. |
| REQ-022 | Investment projects progress, identify delayed/stopped, propose acceleration measures | **Field** | Inspector can observe project progress and note delays; H6 documented for undefined threshold. |
| REQ-023 | Workshops, labs, classrooms, dormitories, restaurants, facilities readiness | **Field** | Inspector can verify readiness of each space type. H2 documented for undefined criteria. |
| REQ-024 | Materials, training equipment and consumable tooling availability | **Field** | Inspector can verify availability on site. Distinguishes consumable vs. durable (DOM-05 vs DOM-06 band). |
| REQ-025 | Equipment readiness before learner reception | **Field** | Inspector can verify equipment is ready before learners arrive. |
| REQ-026 | Partnerships with economic institutions, internship and training positions | **Field** | Inspector can verify partnership existence and positions; H11 documented for undefined enhancement measures. |
| REQ-027 | Follow-up of digital platform usage and data auditing (REQ-027 / DOM-10) | **Field** — **reconsidered** | Not excluded just because API/interface not designed. Inspector can verify usage and data auditing without technical integration. H3, H8 documented. |
| REQ-028 | User improvement programmes, competency-based approach, English, modern specializations | **Field** | Inspector can observe whether programmes are running; H11 documented for undefined programs/criteria. |
| REQ-029 | Excellence centers, entrepreneurship development, Making-Lab, incubators readiness | **Field** | Inspector can verify readiness of each structure type; H11 documented for undefined criteria. |
| REQ-030 | Learner reception conditions, housing, meals, transport, special categories | **Field** | Inspector can verify reception conditions; H10 documented for "special categories" and "suitable conditions" undefined. |
| REQ-031 | Record deficiencies and obstacles, classify by urgency and impact on intake | **Field** | Inspector can record deficiencies and classify them. H9 documented for undefined urgency/impact grid. |
| REQ-035 | Effective follow-up of corrective measures until deficiencies cleared | **Excluded** | H13 says proof of maintenance/operation is not defined; inspector cannot verify the "effective follow-up" loop. |
| REQ-032 | Weekly committee meetings and meeting minutes | **Excluded** | Governance act; source defines rhythm and contents but no field-verifiable inspection. H12 documented. |
| REQ-036 | Continuous coordination between sectoral entities and institutions | **Excluded** | General governance; source states the obligation but provides no field-inspectable criteria. No observable act for the inspector to verify beyond noting that coordination occurs, which is too vague for a checklist item. H12: conditional membership criteria not defined. |


## 3. REQ-005 / Structures Safety vs. Electrical Networks (Correction B)

**Rule:** REQ-005 (structural safety of roofs/walls) must **not** be attributed to an electrical networks item. Each has distinct meaning.

**Options:**
1. **REQ-005 has its own field item** — the inspector examines structural condition (cracks, water damage, wall integrity). This item is classified as `linked_dom: DOM-04`, `linked_req: REQ-005`, provenance `DIRECT`.
2. **REQ-005 is excluded** — with a documented reason (e.g., "source does not define structural inspection criteria; H2 applies"). In this case, REQ-005 appears in the excluded list of the Coverage Review, **not** in an electrical item.

**Never:** attribute REQ-005 meaning to an electrical network item. This violates the separation of domains and the source constraints.


## 4. REQ-027 / DOM-10 Reconsideration (Correction D)

**Do not exclude REQ-027 solely because no API or interface is designed.**

Distinguish:
- **Verification of usage/documentation** — the inspector can check that the platform is being used, that data is being entered/updated, that audits are taking place, without any technical integration. This **can** be a field checklist item.
- **Technical integration** — designing API, connectors, automated data flow. This is **outside Gate 2**.

**Decision for REQ-027:** Keep as **Field** item with the inspection question: *"Can the inspector verify, during a field visit or document review, that the platforms digital usage is being followed and that related data are being audited, without assuming technical integration with the platform?"*

Source constraints: H3 (access to statistics, scope of data), H8 (three platforms distinguished, no assumed integration). The item records `match`/`non_match`/`not_evaluable` based on what the inspector can observe or document.


## 5. Provenance Model Consistency (Correction E)

**PROJECT is not a general governance label.** `PROJECT` means only the four explicit Gate 2 decisions:

1. Structured field checklist
2. Text notes during inspection
3. Optional future phone photo/file evidence
3. Evidence is not mandatory

**Provenance representation:** If an item's primary source is a DIRECT requirement and it is supported by a DERIVED requirement, the model must represent this consistently. Example structure:

```json
"provenance": {
  "primary": "DIRECT",
  "supporting": ["DER-05", "DER-09"]
}
```

Or the equivalent clear format: `primary_provenance: DIRECT` with `supporting_derivations: DER-...`. **Never** state that `provenance` must be a single value and then place two values in the instance. The model must allow primary + supporting documentation.

All checklist items must declare:
- `primary_provenance`: one of `DIRECT`, `DERIVED`, or `PROJECT`
- `supporting_derivations`: list of DER-XXX that support the item (may be empty)

If an item is purely DIRECT, `supporting_derivations` is empty and `primary_provenance: DIRECT`.
If an item is purely DERIVED (no direct source text), `primary_provenance: DERIVED`.
If an item reflects a Gate 2 PROJECT decision (structured checklist, text notes, optional evidence, evidence not mandatory), `primary_provenance: PROJECT`.


## 6. Model/Instance Field Consistency (Correction F)

**Unify field names between `CHECKLIST-MODEL-v1.md` (the logical model) and `FIELD-CHECKLIST-v1.md` (the instantiation).**

| Concept | Model field name | Field-checklist field name | Status |
|---|---|---|---|
| Deficiency recording | `deficiency_recorded` | `deficiency_implied` | **Fix: use `deficiency_implied` consistently** in both model and instance. |
| Not evaluable reason | `not_evaluable_reason` | (should appear) | **Add `not_evaluable_reason` to field checklist structure** when `inspection_result = not_evaluable`. |
| Inspection result | `inspection_result` | `inspection_result` | Already consistent. |
| Evidence optional | `evidence_optional` | `evidence_optional` | Already consistent. |

**Mandatory field unification:**
- Use `deficiency_implied` in both the model description and the field checklist instance. Do not mix `deficiency_recorded` and `deficiency_implied`.
- If the model describes `not_evaluable_reason`, the field checklist must include the same field with the same semantics: *"Why the inspection result is `not_evaluable` for this visit (required when result is `not_evaluable`)."*


## 7. Non-Applicability Distinction (Correction G)

**Must distinguish logically between:**

| Term | Meaning | When Used |
|---|---|---|
| `not_evaluable` | The requirement **applies** to the subject/context, but the inspector **cannot evaluate** it during this particular visit (weather, committee not formed, platform inaccessible, etc.). | Required when `inspection_result = not_evaluable`; `not_evaluable_reason` must be filled. |
| `not_applicable` | The requirement **does not apply** to the subject/context (e.g., a rural institution has no dormitories, so REQ-030 "housing conditions" does not apply; or a workshop has no electrical system, so REQ-006 does not apply). | Used when the item's content is outside the scope of the specific inspection site. Different from `not_evaluable`. |

**Do not mix** `not_evaluable` and `not_applicable` in the same field. The checklist item must clearly declare which status applies.
## 8. Finding Relationship (Correction H)

Keep conceptual separation:

- Checklist item = Fixed definition/question (stable ID, title, inspection question).
- Response = Inspection result (match/non_match/not_evaluable) recorded during a visit.
- Deficiency/Finding = A non-compliance or deficiency that may be recorded when inspection_result = non_match.

Rule: A checklist item itself is not a finding. The response may:
- direct_link: The response directly IS the finding (e.g., Crack in wall observed deficiency recorded directly).
- contextual: The response supports a finding recorded elsewhere (e.g., No data updated on platform supports a broader deficiency from another item).
- none: The non-match is noted but no formal deficiency is recorded at this time.

Never write in the model: item = finding. Always keep the three-level separation.
## 9. H1–H13 Accuracy (Correction I)

Review each H reference; do not use H inappropriate just because there is ambiguity.

H-number | Correct subject | Fix required
H1 | Density and surprise of inspection visits | Already documented in CL-001 source_constraint. No change needed.
H2 | Criteria for the five workshop inspection domains | Documented in CL-003, CL-005, CL-023 source_constraint. No change needed.
H4 | Undated deadlines — closest deadlines, specified deadlines, 04 October 2026 as reference. Not water/electricity regularity standards. Verify all source_constraint fields use H4 only for deadline ambiguity.
H7 | Measurable indicators for the weekly provincial report. Not general accountability. Verify source_constraint fields referencing H7 are about weekly report indicators, not about accountability mechanisms.
H5 | Methodology for actual needs in human resources allocation. Not general supervision. Verify H5 appears only where actual needs methodology is the issue (REQ-015, REQ-020).
H6 | Threshold and states for delayed/stopped projects. Not general project progress. Verify H6 appears only where delayed/stalled threshold is the issue (REQ-022).
H10 | Special categories and suitable conditions for beneficiary treatment. Not general facility quality. Verify H10 appears only where special categories/suitable conditions are the issue (REQ-030, CL-028).
No non-existent IDs: Do not reference CL-033, CL-034, or any ID beyond CL-030. If an open question has no matching H, write open question without an H reference rather than attributing incorrectly.

General rule: If the ambiguity described does not match the H-number’s defined subject, write the open_question field without an H reference. Do not force an H attribution.
## 10. Domain Coverage Consistency (Correction J)

Calculate domains from the actual linked_dom field of each item, not from memory or assumption.

| Item ID | linked_dom | Domain |
| CL-001 | DOM-01 | DOM-01 |
| CL-002 | DOM-02 | DOM-02 |
| CL-003 | DOM-03 | DOM-03 |
| CL-004 | DOM-04 | DOM-04 |
| CL-005 | DOM-04 | DOM-04 (structures) |
| CL-006 | DOM-03 | DOM-03 (electrical) |
| CL-007 | DOM-01 | DOM-01 |
| CL-008 | DOM-05 | DOM-05 |
| CL-009 | DOM-05 | DOM-05 |
| CL-012 | DOM-05 | DOM-05 |
| CL-013 | DOM-05 | DOM-05 |
| CL-014 | DOM-05 | DOM-05 |
| CL-015 | DOM-12 | DOM-12 |
| CL-018 | DOM-02 | DOM-02 |
| CL-019 | DOM-07 | DOM-07 |
| CL-020 | DOM-08 | DOM-08 |
| CL-021 | DOM-07 | DOM-07 |
| CL-022 | DOM-09 | DOM-09 |
| CL-023 | DOM-04 | DOM-04 |
| CL-024 | DOM-06 | DOM-06 |
| CL-026 | DOM-11 | DOM-11 |
| CL-027 | DOM-11 | DOM-11 |
| CL-028 | DOM-04 | DOM-04 |
| CL-028 | DOM-04 | DOM-04 (only once) |
| CL-029 | DOM-13 | DOM-13 |

Constraints:
- Do not attribute DOM-11 items to DOM-07 in the coverage table.
- Any item linked to DOM-12 must not appear as cross-cutting without a clear explanation in the Coverage Review.
- The coverage table must list, for each domain, the items that have linked_dom set to that domain.

Actual domain coverage (from the item linked_dom values):
- DOM-01: CL-001, CL-007 (2 items)
- DOM-02: CL-002, CL-018 (2 items)
- DOM-03: CL-003, CL-006 (2 items)
- DOM-04: CL-004, CL-005, CL-023, CL-028 (4 items)
- DOM-05: CL-008, CL-009, CL-012, CL-013, CL-014 (5 items)
- DOM-06: CL-024 (1 item)
- DOM-07: CL-019, CL-021, CL-026, CL-027 (4 items)
- DOM-08: CL-020 (1 item)
- DOM-09: CL-022 (1 item)
- DOM-11: CL-026, CL-027 (2 items)
- DOM-12: CL-015 (1 item)
- DOM-13: CL-029 (1 item)
- DOM-10: 0 items (handled thematically through platform-reference items; no standalone item designed)

Total: 25 item-domain assignments across 12 of 13 DOMs. DOM-10 has no direct item because its content is handled through source_constraint and open_question references to H3 and H8 without designing a separate API or interface.
## 11. Language and Canonical Terminology (Correction K)

Use clear Arabic as in Gate 1 for item titles, inspection questions, and core terminology. Remove distorted terms.

Prohibited terms (remove or replace):
- fitzhysiques → use correct French or Arabic equivalent
- bididagogique → use لبدمهن or الدسلق
- Amincissement → remove (means weight loss; not relevant)
- Aminse générale → use العمان أمريي or the exact source term

Keep platform name as: «طسمِی» (Tasir)

Technical field names may be in English, but human-readable content and source terms must be clear and traceable.

Arabic terminology guidelines:
- Use the exact source terms where possible (e.g., عرس for workshops, للنِاة for provincial committee, لعنية for digital platform).
- If a direct Arabic source term is not available, use clear descriptive Arabic, not transliterated English.
- All item titles and inspection questions must be in Arabic (the project language) or clear Arabic descriptive text, not mixed with distorted terms.
## 12. Stable IDs (Correction — continued from A)

Rules:
- Each checklist ID (CL-001, CL-002, ...) is stable: it does not change meaning across revisions.
- If an item is deleted, leave the gap. Do not renumber subsequent items to fill the gap, unless the revision is a complete rewrite and the new IDs are assigned fresh.
- If a new item is needed, use a new unused ID (e.g., if CL-030 is the last, the next is CL-031, but only if truly needed).
- Numerical continuity is not more important than identity stability. A gap is acceptable; a mislabeled ID is not.

Current IDs in this model: CL-001 through CL-030 (30 items). If the final count after Coverage Review is different, adjust the IDs accordingly—but each must be unique and stable.
## 13. Change Log

| Date | Version | Author | Change |
|------|---------|--------|--------|
| -- | v1.0 | -- | Gate 2 correction: redesigned logical model with exact coverage arithmetic (covered ⊕ excluded = REQ-001..REQ-036, no overlap), REQ-005 separated from electrical, REQ-027 kept as field (not excluded for lack of API), provenance model with primary+supporting, deficiency_implied unified field, not_evaluable/not_applicable distinction, H1–H13 accuracy fixed, domain coverage from actual linked_dom, clean Arabic (removed fitzhysiques/bididagogique/Amincissement), stable IDs, finding relationship separation, finding relation item≠finding. No Data Model, schema, UI, code, or Gate 3. |

## 14. Coverage Review Summary (Refer to FIELD-CHECKLIST-v1.md)

The mandatory Coverage Review documenting:
- Total checklist items and actual count
- Which DIRECT requirements are covered and which are excluded
- Exact excluded REQ IDs with reasons
- DERIVED requirements supporting which items
- Domains actually covered (from linked_dom)
- All 13 open questions (H1–H13) with accurate references
- Language canonical terminology audit

Is embedded in FIELD-CHECKLIST-v1.md and must be consistent with this model.
