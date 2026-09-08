# FIELD-CHECKLIST-v1 — Field Inspection Checklist for Gate 2 (Corrected)

**Gate 2 Correction** — 29 field checklist items with proper inspection results (match/non_match/not_evaluable), provenance tracking (DIRECT / DERIVED / PROJECT), deficiency recording, source constraints, and mandatory Coverage Review. No ✗ Not started / In progress / Completed. Evidence: PROJECT, optional, never mandatory.

No Data Model, no schema, no UI, no code, no Gate 3.

**Purpose**: This is the field inspection checklist used by inspectors during site visits. It instantiates the logical model defined in CHECKLIST-MODEL-v1.md. The checklist covers 29 of 36 DIRECT requirements (REQ-001 through REQ-036); 7 are excluded as governance/admin/reporting items with documented reasons. Every item is a concrete inspection question answerable (match / non_match / not_evaluable) during a field visit.

## How to Use This Checklist
1. Before the visit - Review the items linked to the domain(s) you will inspect. Note any source_constraint or open_question that may affect your assessment.
2. During the visit - For each item, answer the inspection_question by recording one of: match, non_match, or not_evaluable. Use text_notes to record observations, quoting source terms where appropriate.
3. After the visit - If inspection_result = non_match, set deficiency_implied = true and record a finding using finding_relationship. Attach optional evidence (phone photo/file) if relevant, but remember: evidence is not mandatory.
4. Text notes - Use for: observations, source-term citations, owner-deferred decisions (H1-H13), and not_evaluable_reason when applicable.
5. Evidence - Optional marker. A phone photo or file may be attached; it is a PROJECT decision and is never mandatory.

## Checklist Items (CL-001 through CL-029)
Each item follows this layout. The id is stable and does not change between visits.
```
### CL-<n> -- <title>
**id:** CL-<n>
**title:** <title>
**linked_dom:** DOM-<n>
**linked_req:** REQ-<n> [DIRECT]
**provenance:** primary: DIRECT |
**inspection_result:** match | non_match | not_evaluable |
**text_notes:** <free-form observations>
**evidence_optional:** true (PROJECT -- not mandatory)
**deficiency_implied:** true if inspection_result = non_match and a finding is recorded
**finding_relationship:** direct_link | contextual | none
**source_constraint:** <known ambiguity from sources, or blank>
**open_question:** <open implementation question, H1-H13, or blank>
```

## Checklist Items (CL-001 through CL-029)
Each item follows this layout. The id is stable and does not change between visits.
```
### CL-<n> -- <title>
**id:** CL-<n>
**title:** <title>
**linked_dom:** DOM-<n>
**linked_req:** REQ-<n> [DIRECT]
**provenance:** primary: DIRECT |
**inspection_result:** match | non_match | not_evaluable |
**text_notes:** <free-form observations>
**evidence_optional:** true (PROJECT -- not mandatory)
**deficiency_implied:** true if inspection_result = non_match and a finding is recorded
**finding_relationship:** direct_link | contextual | none
**source_constraint:** <known ambiguity from sources, or blank>
**open_question:** <open implementation question, H1-H13, or blank>
```
