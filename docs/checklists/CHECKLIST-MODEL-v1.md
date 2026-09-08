# CHECKLIST-MODEL-v1 — Structured Field Checklist Model

**Gate 2 Output** — Structured field checklist, text notes, optional future phone photo/file evidence; evidence is not mandatory.

No Data Model, no schema, no UI, no code, no Gate 3.

---

## Overview

This checklist model derives its structure entirely from the approved source documents:

- `sources/01_field_control_and_equipment_aug_2026.md` (marcelles first and second)
- `sources/02_provincial_entry_readiness_committee_2026_2027.md`
- `docs/requirements/REQUIREMENTS-v1.md` (DIRECT requirements REQ-001 to REQ-036)
- `docs/requirements/INSPECTION-DOMAINS-v1.md` (DOM-01 to DOM-13)

The model does **not** introduce any new data model, schema, or code. It is a pure text checklist with structured fields and text notes.

---

## Checklist Structure

Each checklist entry follows this pattern:

```
### CHECK-<domain>-<number>

**Domain:** DOM-<number> — <domain name>
**Requirement:** REQ-<number> — <requirement title>
**Status:** [ ] Not started | [ ] In progress | [ ] Completed
**Text Notes:** <free-form notes>
**Evidence:** [ ] Optional — phone photo/file (not mandatory)
**Source Reference:** <source document and section>
```

The checklist covers all 13 inspection domains (DOM-01 through DOM-13) with their direct requirements.

---

## Domain Coverage

| Checklist Entry | Domain | Direct Requirements |
|----------------|--------|---------------------|
| DOM-01 | الزيارات الميدانية والتقارير التفصيلية للورشات | REQ-001, REQ-007, REQ-008 |
| DOM-02 | الاستغلال والجاهزية البيداغوجية | REQ-002, REQ-018 |
| DOM-03 | السلامة والنظافة والوقاية من الأخطار | REQ-003, REQ-006 |
| DOM-04 | البنية المادية والفضاءات وخدمات الإيواء والإطعام | REQ-004, REQ-005, REQ-023, REQ-030 |
| DOM-05 | التجهيزات والتحيين الرقمي على «تسيير» | REQ-009, REQ-010, REQ-011, REQ-012, REQ-013, REQ-014, REQ-025 |
| DOM-06 | المواد الأولية ولوازم التكوين | REQ-024 |
| DOM-07 | التسجيلات والعروض والشراكات | REQ-019, REQ-021, REQ-026 |
| DOM-08 | التأطير والموارد البشرية | REQ-020 |
| DOM-09 | المشاريع الاستثمارية والتهيئة | REQ-022 |
| DOM-10 | المنصات الرقمية وتدقيق المعطيات | REQ-027 |
| DOM-11 | البرامج والهياكل المتخصصة | REQ-028, REQ-029 |
| DOM-12 | حوكمة اللجنة والتقارير الولائية | REQ-015, REQ-016, REQ-017, REQ-032, REQ-033, REQ-034, REQ-036 |
| DOM-13 | النقائص والإجراءات التصحيحية | REQ-031, REQ-035 |

---

## Usage Instructions

1. **Inspect** — Review each domain and its direct requirements against the source documents.
2. **Status** — Mark `[ ]` → `[x]` as work progresses.
3. **Text Notes** — Use the free-form notes field to record observations, decisions, or owner‑deferred items (H1–H13).
4. **Evidence** — Optional marker for any phone photo/file that may be captured later. Evidence is **not mandatory** for v1.
5. **Source Reference** — Always trace any recorded fact back to one of the four approved source documents. Do not modify the source texts.

---

## Owner Decisions (H1–H13)

Each entry may have owner‑deferred decisions. Record them in the Text Notes field. Do not resolve them as part of this gate.

- H1: Density and surprise of inspection visits
- H2: Criteria for the five workshop inspection domains
- H3: Access to «Tasir» platform and scope of data entry
- H4: Undated deadlines («closest deadlines», «specified deadlines», «04 October 2026»)
- H5: Methodology for «actual needs» in human resources allocation
- H6: Threshold and states for delayed/stalled projects
- H7: Measurable indicators for the weekly provincial report
- H8: The three digital platforms (Tasir, general digital, inspection) and document upload
- H9: «Urgency‑impact» classification grid for deficiencies
- H10: «Special categories» and «suitable conditions» for beneficiary treatment
- H11: Specialized domain scope (user training, English, specializations; excellence centers)
- H12: Conditional membership criteria for committee meetings
- H13: Proof of maintenance and operation

---

## Change Log

| Date | Version | Author | Change |
|------|---------|--------|--------|
| — | v1.0 | — | Initial model from Gate 2 recovery from main |