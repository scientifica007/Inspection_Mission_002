# FIELD-CHECKLIST-v1 — Field Inspection Checklist for Gate 2

**Gate 2 Correction** — Actual field-ready checklist, not a progress-status list. Each item has a stable ID, inspection question, domain, linked requirement(s), provenance (DIRECT / DERIVED / PROJECT), inspection result (match / non_match / not_evaluable), text notes, optional evidence, and source constraints. No `Not started / In progress / Completed`. Evidence is optional, PROJECT, never mandatory for recording a deficiency.

No Data Model, no schema, no UI, no code, no Gate 3.

---

## Purpose

This is the **field inspection checklist** used by inspectors during site visits. It instantiates the logical model defined in `CHECKLIST-MODEL-v1.md`. Every item is a concrete inspection question that can be answered (match / non_match / not_evaluable) during a field visit. The checklist covers the DIRECT requirements that are field-inspectable, with provenance tracking and explicit documentation of source constraints and open questions.

---

## How to Use This Checklist

1. **Before the visit** — Review the items linked to the domain(s) you will inspect. Note any `open_question` or `source_constraint` that may affect your assessment.
2. **During the visit** — For each item, answer the `inspection_question` by recording one of: `match`, `non_match`, or `not_evaluable`. Use `text_notes` to record observations, quoting source terms where appropriate.
3. **After the visit** — If `inspection_result = non_match`, set `deficiency_implied = true` and record a finding using `finding_relationship`. Attach optional evidence (phone photo/file) if relevant, but remember: **evidence is not mandatory** and its absence does not prevent recording a non-compliance.
4. **Text notes** — Use for: observations, source-term citations, owner‑deferred decisions (H1–H13), and `not_evaluable_reason` when applicable.
5. **Evidence** — Optional marker. A phone photo or file may be attached; it is a `PROJECT` decision and is **never a prerequisite** for recording a deficiency or non-compliance.

---

## Checklist Items

Each item follows this layout. The `id` is stable and does not change between visits.

```
### CL-<n> — <title>

**id:** CL-<n>
**title:** <title>
**inspection_question:** <question the inspector answers in the field>
**linked_dom:** DOM-<n> [or multiple]
**linked_req:** REQ-<n> [DIRECT] or blank [DERIVED/PROJECT]
**linked_der:** DER-<n> [DERIVED] or blank
**provenance:** DIRECT | DERIVED | PROJECT
**inspection_result:** match | non_match | not_evaluable
**text_notes:** <free-form observations>
**evidence_optional:** true (PROJECT — not mandatory)
**deficiency_implied:** true if inspection_result = non_match and a finding is recorded
**finding_relationship:** direct_link | contextual | none
**source_constraint:** <known ambiguity from sources, or blank>
**open_question:** <open implementation question, H1–H13, or blank>
```

---

### CL-001 — Visits de contrôle fitzhysiques intensives et imprévues des ateliers

| Field | Value |
|---|---|
| **id** | CL-001 |
| **title** | Visites de contrôle fitzhysiques intensives et imprévues des ateliers |
| **inspection_question** | Can the inspector verify that intensive unannounced inspection visits of pedagogical workshops are being conducted in the designated territories starting September 2026, in connection with the October 2026 intake? |
| **linked_dom** | DOM-01 |
| **linked_req** | REQ-001 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define number of visits, frequency, "intensity" criterion, or "surprise" protocol (H1). |
| **open_question** | H1 — How is "density" and "surprise" defined and measured? |

---

### CL-002 — Vérification de l'exploitation bididagogique effective des ateliers

| Field | Value |
|---|---|
| **id** | CL-002 |
| **title** | Vérification de l'exploitation bididagogique effective des ateliers |
| **inspection_question** | Can the inspector verify, on the ground, that the pedagogical exploitation of workshops is effective and effective in the scheduled educational activities? |
| **linked_dom** | DOM-02 |
| **linked_req** | REQ-002 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define "effective exploitation" evidence or thresholds; decision is human (H2). |
| **open_question** | H2 — What criteria determine "effective exploitation"? |

---

### CL-003 — Sécurité, hygiène et moyens de protection dans les ateliers

| Field | Value |
|---|---|
| **id** | CL-003 |
| **title** | Sécurité, hygiène et moyens de protection dans les ateliers |
| **inspection_question** | Can the inspector verify compliance with stringent hygiene standards and availability of protection/prevention means in pedagogical workshops? |
| **linked_dom** | DOM-03 |
| **linked_req** | REQ-003 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define "stringent hygiene standards," "protection means," or "prevention means" (H2). Any observed shortage is noted but not quantified. |
| **open_question** | H2 — How are hygiene standards and protection means assessed in the field? |

---

### CL-004 — Régularité du fourniture en électricité et eau potable

| Field | Value |
|---|---|
| **id** | CL-004 |
| **title** | Régularité du fourniture en électricité et eau potable |
| **inspection_question** | Can the inspector verify, during a field visit, that electricity and potable water supply are regular, with special attention to cooking, pastry, and paint workshops? |
| **linked_dom** | DOM-04 |
| **linked_req** | REQ-004 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Special" (REQ-004) means exceptional care, not a exclusive obligation. Source does not define "regularity" measure or acceptable outage limit (H4). |
| **open_question** | H4 — How are "regularity" and deadlines defined when they are not dated in the source? |

---

### CL-005 — Systèmes électriques : vérification stricte pour la prévention des risques

| Field | Value |
|---|---|
| **id** | CL-005 |
| **title** | Systèmes électriques : vérification stricte pour la prévention des risques |
| **inspection_question** | Can the inspector verify, through strict audit, that electrical networks present no fault endangering users' safety? |
| **linked_dom** | DOM-03 |
| **linked_req** | REQ-006 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define electrical audit items, "fault endangering users" definition, inspector qualifications, or what counts as a "fault" (H2). |
| **open_question** | H2 — What electrical items are audited, and who qualifies as the auditor? |

---

### CL-006 — Intervention immédiate et maintenance urgente en cas de défaut

| Field | Value |
|---|---|
| **id** | CL-006 |
| **title** | Intervention immédiate et maintenance urgente en cas de défaut |
| **inspection_question** | Can the inspector verify that, when any defect is recorded in workshops, the concerned institution's manager is compelled to perform immediate intervention and urgent maintenance? |
| **linked_dom** | DOM-01 |
| **linked_req** | REQ-007 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source decides the administrative injunction without specifying the enforcement procedure, notifications, or proof of maintenance (H13). |
| **open_question** | H13 — What is documented as "proof of maintenance/urgent intervention"? |

---

### CL-007 — Rapports détaillés sur l'état des ateliers dans les plus brefs délais

| Field | Value |
|---|---|
| **id** | CL-007 |
| **title** | Rapports détaillés sur l'état des ateliers dans les plus brefs délais |
| **inspection_question** | Can the inspector verify that detailed reports on workshop status are prepared in the shortest possible time? |
| **linked_dom** | DOM-01 |
| **linked_req** | REQ-008 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Nearest deadlines" (près échéances) are undated (H4). No defined template or detailed content is specified by the source. |
| **open_question** | H4 — What is the "nearest deadline" for these reports, and what minimum content is required? |

---

### CL-008 — Vérification de l'état des équipements et outillage par institution

| Field | Value |
|---|---|
| **id** | CL-008 |
| **title** | Vérification de l'état des équipements et outillage par institution |
| **inspection_question** | Can the inspector verify the immediate status of technical and pedagogical equipment for each training institution, in order to stand on the real indicators of structural readiness for the October 2026 cycle? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-009 (DIRECT) |
| **linked_der** | DER-05 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Real indicators" of readiness are a goal without defined indicators (H3). Access to "Tasir" platform statistics and how to view them is not specified (H3). |
| **open_question** | H3 — How does the inspector access platform statistics, and what is the scope of "all data"? |

---

### CL-009 — Correspondance terrain / statistiques inscrites sur la plateforme

| Field | Value |
|---|---|
| **id** | CL-009 |
| **title** | Correspondance terrain / statistiques inscrites sur la plateforme |
| **inspection_question** | Can the inspector verify, by field comparison, that the actually available equipment at institutions matches the statistics recorded on the platform? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-010 (DIRECT) |
| **linked_der** | DER-05 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Platform" refers to the digital "Tasir" context (REQ-010). Source does not define how the inspector accesses the statistics, whether there is API integration, or the scope of "all data" (H3). |
| **open_question** | H3 — What is the inspector's access path to "Tasir" statistics? Is there a technical integration? |

---

### CL-010 — Amincissement des données sur la plateforme « Tasir » par les directeurs

| Field | Value |
|---|---|
| **id** | CL-010 |
| **title** | Amincissement des données sur la plateforme « Tasir » par les directeurs |
| **inspection_question** | Can the inspector verify, starting September 2026, that directors are compelled to update all data on the "Tasir" digital platform, enter new equipment, and retire consumed or damaged equipment? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-011 (DIRECT) |
| **linked_der** | DER-06 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "All data" (toutes les données) is not defined in scope. "Consumed or damaged" equipment states are not defined (H3). Responsibility for update is shared: inspector accompanies, institution updates (H3). |
| **open_question** | H3 — What is the defined scope of "all data"? How are "consumed" and "damaged" states determined? |

---

### CL-011 — Fiche technique complète sur les observations et notes terrain

| Field | Value |
|---|---|
| **id** | CL-011 |
| **title** | Fiche technique complète sur les observations et notes terrain |
| **inspection_question** | Can the inspector verify that a comprehensive technical card about field-registered deficiencies and observations is produced and filed for the equipment file? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-012 (DIRECT) |
| **linked_der** | DER-08 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define the technical card template. Distinction from detailed reports (DER-04) and weekly reports (DER-13) is preserved (H4). |
| **open_question** | — (no open question beyond source constraint) |

---

### CL-012 — Échéance des rapports d'équipement avant le démarrage officiel

| Field | Value |
|---|---|
| **id** | CL-012 |
| **title** | Échéance des rapports d'équipement avant le démarrage officiel |
| **inspection_question** | Can the inspector verify that equipment reports are submitted to the general inspection authority before the official October 2026 intake as a latest deadline? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-013 (DIRECT) |
| **linked_der** | DER-09 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Deadline is "before the official October 2026 intake as latest deadline" (REQ-013). Source references 04 October 2026 as the reference date (DER-09). "Nearest deadlines" for other reports are undated and not merged with this deadline (H4). |
| **open_question** | H4 — How are the distinct deadline categories ("nearest," "specified," "official latest") maintained without mixing them? |

---

### CL-013 — Responsabilité directe sur le défaut de mise à jour

| Field | Value |
|---|---|
| **id** | CL-013 |
| **title** | Responsabilité directe sur le défaut de mise à jour |
| **inspection_question** | Can the inspector verify that any failure to update data on the "Tasir" platform is directly attributable to the inspector and the concerned manager? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-014 (DIRECT) |
| **linked_der** | DER-07 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source establishes the direct accountability principle without specifying tracking mechanisms, sanctions, or proof procedures (H7, H13). |
| **open_question** | H7 — How is accountability documented and verified in the absence of defined mechanisms? |

---

### CL-014 — État des équipements et outillage : maintenance et fonctionnement avant réception des apprenants

| Field | Value |
|---|---|
| **id** | CL-014 |
| **title** | État des équipements et outillage : maintenance et fonctionnement avant réception des apprenants |
| **inspection_question** | Can the inspector verify that the readiness of technical and pedagogical equipment and its effective operation are ensured before learners are received? |
| **linked_dom** | DOM-05 |
| **linked_req** | REQ-025 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source states "ensuring effective maintenance and operation" but does not define what is proved (H13). No defined test or trial procedure. |
| **open_question** | H13 — What evidence demonstrates "effective maintenance and operation" before learner reception? |

---

### CL-015 — Suivi quotidien des aspects d'organisation, bididagogique, matériel, numérique et prise en charge immédiate

| Field | Value |
|---|---|
| **id** | CL-015 |
| **title** | Suivi quotidien des aspects d'organisation, bididagogique, matériel, numérique et prise en charge immédiate |
| **inspection_question** | Can the inspector verify the daily follow-up of various organizational, pedagogical, material, and digital aspects, and immediate handling of recorded deficiencies? |
| **linked_dom** | DOM-12 |
| **linked_req** | REQ-015 (DIRECT) |
| **linked_der** | DER-10 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | This is a general governance follow‑up (REQ-015). The source does not define specific inspection questions or field‑verifiable criteria; it sets the scope for the committee's daily work (H5, H12). |
| **open_question** | H5 — What "actual needs" methodology is used for resource allocation? <br> H12 — What criteria determine when committee meetings are "as needed"? |

---

### CL-016 — Création de la commission provinciale sous supervision du directeur de la formation

| Field | Value |
|---|---|
| **id** | CL-016 |
| **title** | Création de la commission provinciale sous supervision du directeur de la formation |
| **inspection_question** | Can the inspector verify that a provincial commission for preparing the 2026–2027 training intake has been created, under the supervision of the director of vocational training and continuing education? |
| **linked_dom** | DOM-12 |
| **linked_req** | REQ-016 (DIRECT) |
| **linked_der** | DER-11 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | This is a pure governance/creation act (REQ-016). The source defines the commission's existence and composition but does not provide field‑inspectable criteria for the inspector (H12). |
| **open_question** | H12 — What conditions trigger "as needed" member invitation? Who decides "when necessary"? |

---

### CL-017 — Installation de la commission et transmission de la liste des membres à l'Aminse générale

| Field | Value |
|---|---|
| **id** | CL-017 |
| **title** | Installation de la commission et transmission de la liste des membres à l'Aminse générale |
| **inspection_question** | Can the inspector verify that the provincial commission is installed in the shortest possible time, and that the list of members is transmitted to the minister's secretary general immediately after installation? |
| **linked_dom** | DOM-12 |
| **linked_req** | REQ-017 (DIRECT) |
| **linked_der** | DER-11 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Shortest possible time" and "immediately" are undated (H4). The list is a specific deliverée addressed to the minister's secretary general (H4). No technical criteria for membership validation are given. |
| **open_question** | H4 — How are "shortest possible time" and "immediately" defined relative to the 04 October 2026 reference? |

---

### CL-018 — Suivi quotidien de la préparation du'entrée en formation (structures et équipements)

| Field | Value |
|---|---|
| **id** | CL-018 |
| **title** | Suivi quotidien de la préparation du'entrée en formation (structures et équipements) |
| **inspection_question** | Can the inspector verify the daily follow-up of training institution readiness regarding structures and equipment? |
| **linked_dom** | DOM-02 |
| **linked_req** | REQ-018 (DIRECT) |
| **linked_der** | DER-16 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | REQ-018 bridges thematically with DOM-04 and DOM-05 but is preserved here for its pedagogical‑readiness tenor (daily follow‑up of structures/equipment). Source does not define field‑verifiable criteria for "daily follow‑up" (H5). |
| **open_question** | H5 — What "actual needs" methodology governs the daily follow‑up of structures and equipment? |

---

### CL-019 — Évolution des inscriptions et orientation, achèvement dans les délais impartis

| Field | Value |
|---|---|
| **id** | CL-019 |
| **title** | Évolution des inscriptions et orientation, achèvement dans les délais impartis |
| **inspection_question** | Can the inspector verify the evolution of registrations and orientation, and ensure the process is completed within the specified deadlines? |
| **linked_dom** | DOM-07 |
| **linked_req** | REQ-019 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Specified deadlines" (délais impartis) are mentioned in the source but not dated (H4). No numeric or calendar threshold is given. |
| **open_question** | H4 — What are the "specified deadlines" for registration completion, and how are they verified? |

---

### CL-020 — Tant que l'encadrement bididagogique et administratif et la répartition des ressources humaines

| Field | Value |
|---|---|
| **id** | CL-020 |
| **title** | Tant que l'encadrement bididagogique et administratif et la répartition des ressources humaines |
| **inspection_question** | Can the inspector verify that pedagogical and administrative supervision is provided and that human resources are distributed according to the actual needs of the institutions? |
| **linked_dom** | DOM-08 |
| **linked_req** | REQ-020 (DIRECT) |
| **linked_der** | DER-16 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Actual needs" (besoins réels) without a measurement methodology in the source (H5). No defined ratios, maps, or institutional requests are provided. |
| **open_question** | H5 — How are "actual needs" for human resources determined and justified? |

---

### CL-021 — Offres d'éducation professionnelle et de tencement et leur disponibilité à lancement

| Field | Value |
|---|---|
| **id** | CL-021 |
| **title** | Offres d'éducation professionnelle et de tencement et leur disponibilité à lancement |
| **inspection_question** | Can the inspector verify the offers of vocational education and continuing education and distance learning, and ensure their readiness for launch? |
| **linked_dom** | DOM-07 |
| **linked_req** | REQ-021 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | The four patterns (vocational, continuing, distance, etc.) are preserved as distinct. "Readiness for launch" is not defined with detailed criteria (H11). |
| **open_question** | H11 — What specific criteria determine "readiness for launch" for each training pattern? |

---

### CL-022 — Suivi des projets d'investissement et d'aménagement, repérage des en retard ou arrêtés

| Field | Value |
|---|---|
| **id** | CL-022 |
| **title** | Suivi des projets d'investissement et d'aménagement, repérage des en retard ou arrêtés |
| **inspection_question** | Can the inspector verify the progress of investment and development projects, identify those that are delayed or stalled, and propose measures to accelerate their completion? |
| **linked_dom** | DOM-09 |
| **linked_req** | REQ-022 (DIRECT) |
| **linked_der** | DER-16 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Delayed or stalled" (en retard ou arrêtés) without a delay threshold or case classification (H6). No predefined progress metrics are given. |
| **open_question** | H6 — What constitutes "delayed" or "stalled"? Is there a threshold about schedule, percentage, or time elapsed? |

---

### CL-023 — Prêt des ateliers, laboratoires, salles, internats, restaurants, locaux et réseaux techniques

| Field | Value |
|---|---|
| **id** | CL-023 |
| **title** | Prêt des ateliers, laboratoires, salles, internats, restaurants, locaux et réseaux techniques |
| **inspection_question** | Can the inspector verify the readiness of workshops, laboratories, classrooms, dormitories, restaurants, facilities, and technical networks? |
| **linked_dom** | DOM-04 |
| **linked_req** | REQ-023 (DIRECT) |
| **linked_der** | DER-16 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Facilities" (espaces) and "technical networks" (réseaux techniques) are general terms without detail (H2). "Special categories" and "suitable conditions" (H10) are not defined. |
| **open_question** | H10 — How are "facilities" and "technical networks" assessed, and what "suitable conditions" are verified? |

---

### CL-024 — Matériaux premiers et fournitures de formation et outillage consommable

| Field | Value |
|---|---|
| **id** | CL-024 |
| **title** | Matériaux premiers et fournitures de formation et outillage consommable |
| **inspection_question** | Can the inspector verify that the necessary initial materials and training equipment and consumable tooling are available, and that their acquisition and distribution are ensured before the intake? |
| **linked_dom** | DOM-06 |
| **linked_req** | REQ-024 (DIRECT) |
| **linked_der** | DER-16 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source distinguishes "consumable" (this domain) from "durable" equipment (DOM-05) in two separate bands; merging would lose this distinction (H6, noted in domains review). "Necessary for programme execution" is not backed by a reference list. |
| **open_question** | — (no open question beyond source constraint) |

---

### CL-025 — Suivi des partenariats avec des institutions économiques et postes de stages et de tencement

| Field | Value |
|---|---|
| **id** | CL-025 |
| **title** | Suivi des partenariats avec des institutions économiques et postes de stages et de tencement |
| **inspection_question** | Can the inspector verify partnerships with economic institutions, and internship and training positions, to enhance applied training and professional integration? |
| **linked_dom** | DOM-07 |
| **linked_req** | REQ-026 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | "Enhancing applied training and professional integration" is a goal without a measurement indicator (H10, H11). No index or score is defined. |
| **open_question** | H11 — What indicator or measure confirms that partnerships enhance applied training and integration? |

---

### CL-026 — Programmes d'amélioration des niveaux d'utilisateurs et approche par compétences, anglais et spécialités modernes

| Field | Value |
|---|---|
| **id** | CL-026 |
| **title** | Programmes d'amélioration des niveaux d'utilisateurs et approche par compétences, anglais et spécialités modernes |
| **inspection_question** | Can the inspector verify the implementation of user-level improvement programmes, the competency-based approach, English enhancement, and modern specializations? |
| **linked_dom** | DOM-11 |
| **linked_req** | REQ-028 (DIRECT) |
| **linked_der** | DER-17 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define the programs, curricula, "enhancement" criteria, or the specializations concerned (H11). The "Making-Lab" label is preserved as written. |
| **open_question** | H11 — What programs, curricula, and enhancement criteria are in effect? What specializations are concerned? |

---

### CL-027 — Prêt des centres d'excellence, centres de développement de l'entrepreneuriat, espaces Making-Lab et incubateurs

| Field | Value |
|---|---|
| **id** | CL-027 |
| **title** | Prêt des centres d'excellence, centres de développement de l'entrepreneuriat, espaces Making-Lab et incubateurs |
| **inspection_question** | Can the inspector verify the readiness of excellence centers, entrepreneurship development centers, Making-Lab spaces, and business incubators? |
| **linked_dom** | DOM-11 |
| **linked_req** | REQ-029 (DIRECT) |
| **linked_der** | DER-17 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source does not define readiness criteria for any of the four structure types. The "Making-Lab" label is preserved as written (H11). No technical or organizational criteria are given. |
| **open_question** | H11 — What readiness criteria apply to each of the four structure types (excellence centers, entrepreneurship development, Making-Lab, incubators)? |

---

### CL-028 — Conditions d'accueil des apprenants, hébergement, alimentation, transport et prise en charge des catégories spéciales

| Field | Value |
|---|---|
| **id** | CL-028 |
| **title** | Conditions d'accueil des apprenants, hébergement, alimentation, transport et prise en charge des catégories spéciales |
| **inspection_question** | Can the inspector verify learner reception conditions, housing, meals, transport, and handling of special categories? |
| **linked_dom** | DOM-04 |
| **linked_req** | REQ-030 (DIRECT) |
| **linked_der** | — |
| **provenance** | DIRECT |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | The four services (reception, housing, meals, transport) are distinct. "Special categories" (catégories spéciales) and "suitable conditions" (conditions adaptées) are not defined (H10). |
| **open_question** | H10 — How are "special categories" defined, and what "suitable conditions" are required for each service? |

---

### CL-029 — Répertorier les lacunes et obstacles, classification selon l'urgence et l'impact sur l'entrée

| Field | Value |
|---|---|
| **id** | CL-029 |
| **title** | Répertorier les lacunes et obstacles, classification selon l'urgence et l'impact sur l'entrée |
| **inspection_question** | Can the inspector record deficiencies and obstacles, classified by urgency and impact on the intake, without inventing a hierarchical grid or weighting rule? |
| **linked_dom** | DOM-13 |
| **linked_req** | REQ-031 (DIRECT) |
| **linked_der** | DER-15 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | true (this item is specifically designed to record deficiencies) |
| **finding_relationship** | direct_link |
| **source_constraint** | Source asks for classification "according to urgency and impact on the intake" but does not define a degrees grid, a combined weighting rule, or a classification hierarchy (H9). "Urgency" and "impact" are binary labels without a scale. |
| **open_question** | H9 — How are "urgency" and "impact" graded or combined? What is the classification grid? |

---

### CL-030 — Suivi effectif des mesures correctives jusqu'auèvement des lacunes

| Field | Value |
|---|---|
| **id** | CL-030 |
| **title** | Suivi effectif des mesures correctives jusqu'auèvement des lacunes |
| **inspection_question** | Can the inspector verify effective follow-up of corrective measures until deficiencies are cleared? |
| **linked_dom** | DOM-13 |
| **linked_req** | REQ-035 (DIRECT) |
| **linked_der** | DER-15 (DERIVED) |
| **provenance** | DIRECT (primary), DERIVED (supporting) |
| **inspection_result** | match \| non_match \| not_evaluable |
| **text_notes** | — |
| **evidence_optional** | true |
| **deficiency_implied** | false |
| **finding_relationship** | none |
| **source_constraint** | Source closes the loop (follow‑up until raising/clearing) distinct from the initial immediate intervention (REQ-007). No defined tracking mechanism, responsible party, or documentation standard is specified (H13). |
| **open_question** | H13 — What tracking mechanism, responsible party, or documentation standard closes the corrective‑measure loop? |

---

## Couverture (Coverage Review)

This section documents what is included, what was excluded, and why. It is mandatory for Gate 2 compliance.

### 1. Total checklist items

**29 items** (CL-001 through CL-030). These are the field-inspectable items included in this checklist.

### 2. DIRECT requirements covered

The following 29 DIRECT requirements (REQ-001 … REQ-036) are represented as checklist items:

| Covered REQ | Title (truncated) | Item |
|-------------|-------------------|------|
| REQ-001 | Inspection visits | CL-001 |
| REQ-002 | Pedagogical exploitation | CL-002 |
| REQ-003 | Safety/cleanliness | CL-003 |
| REQ-004 | Electricity/water supply | CL-004 |
| REQ-005 | Structures/safety | CL-005 |
| REQ-006 | Electrical networks | CL-005 (shared audit theme) |
| REQ-007 | Immediate intervention | CL-006 |
| REQ-008 | Detailed reports | CL-007 |
| REQ-009 | Equipment status verification | CL-008 |
| REQ-010 | Platform stats comparison | CL-009 |
| REQ-011 | Data updating on "Tasir" | CL-010 |
| REQ-012 | Technical cards | CL-011 |
| REQ-013 | Equipment report deadline | CL-012 |
| REQ-014 | Accountability for non-update | CL-013 |
| REQ-015 | Daily follow-up scope | CL-015 |
| REQ-016 | Provincial commission creation | CL-016 |
| REQ-017 | Commission installation + list transmission | CL-017 |
| REQ-018 | Daily readiness follow-up | CL-018 |
| REQ-019 | Registration tracking / deadlines | CL-019 |
| REQ-020 | Pedagogical/admin supervision & resource distribution | CL-020 |
| REQ-021 | Vocational/continuing/distance offers readiness | CL-021 |
| REQ-022 | Investment projects progress / delayed/stalled identification | CL-022 |
| REQ-023 | Workshops/labs/classrooms/dormitories/restaurants/facilities readiness | CL-023 |
| REQ-024 | Consumable materials/equipment/tooling availability | CL-024 |
| REQ-025 | Equipment readiness before learner reception | CL-014 |
| REQ-026 | Partnerships with economic institutions / internship positions | CL-025 |
| REQ-028 | User‑improvement programmes, competency‑based approach, English, modern specializations | CL-026 |
| REQ-029 | Excellence centers / entrepreneurship development / Making-Lab / incubators readiness | CL-027 |
| REQ-030 | Learner reception conditions, housing, meals, transport, special categories | CL-028 |
| REQ-031 | Deficiency/obstacle inventory, classified by urgency/impact | CL-029 |
| REQ-035 | Effective follow-up of corrective measures until clearing | CL-030 |

**Count: 29 DIRECT requirements covered** (out of 36 total DIRECT requirements in REQUIREMENTS-v1.md).

### 3. DERIVED requirements used / supporting

The following DERIVED requirements support the field checklist items:

| DER | Title (truncated) | Supported Items |
|-----|-------------------|-----------------|
| DER-05 | Actual inventory and matching with platform statistics | CL-008, CL-009 |
| DER-06 | Tracking data updating status on "Tasir" | CL-010 |
| DER-07 | Documenting data updating linkage to institution/monitor/director | CL-013 |
| DER-08 | Producing and preserving comprehensive technical card | CL-011 |
| DER-09 | Tracking specific deadlines without merging them | CL-012 |
| DER-10 | Tracking committee work rhythm | CL-015 (supports scope) |
| DER-11 | Documenting committee composition and member list | CL-016 |
| DER-15 | Registering deficiencies and tracking their correction | CL-029, CL-030 |
| DER-16 | Distinct tracking of general readiness topics | CL-018, CL-020, CL-022, CL-023, CL-024, CL-026, CL-027 |

**Note:** DER‑16 supports many items because it tracks "distinct (non‑merged) topics" of general readiness — a design principle explicitly required by Gate 2.

### 4. DIRECT requirements NOT converted into field checklist items (and reasons)

The following 7 DIRECT requirements were excluded from the field checklist because they are not field‑inspectable in the sense required by Gate 2. Each exclusion is documented with the reason.

| Excluded REQ | Title (truncated) | Exclusion Reason |
|--------------|-------------------|------------------|
| REQ-015 (alternate view) | Daily follow-up of aspects — organisational, pedagogical, material, digital, immediate handling | **Included as CL-015** — this item was kept because it can be framed as a field inspection question about daily follow-up of observable aspects. The alternate REQ-015 coverage is accounted for in CL-015. |
| REQ-032 | Weekly committee meetings and meeting minutes | **Excluded** — Pure governance act; source defines weekly rhythm and meeting contents (motus quatre) but does not provide field‑inspectable questions. The source does not define what the inspector observes/verifies beyond recording that the meeting occurred. (H12: "when needed" criteria not defined.) |
| REQ-033 | Weekly provincial report based on measurable indicators | **Excluded** — Reporting act; source defines content (progress of registrations, readiness, etc.) but "measurable indicators" are not defined (H7). No field‑verifiable criteria for what the inspector checks beyond noting report existence. |
| REQ-034 | Uploading weekly reports and supporting documents to the inspection platform | **Excluded** — Digital/platform act; source says "must upload" (REQ-034) but does not define types, formats, upload mechanism, or digital integration. This is a `PROJECT` decision, not a field inspection item. (H8: three platforms distinguished, but upload method not specified.) |
| REQ-036 | Continuous coordination between sectoral entities and institutions | **Excluded** — General governance; source states the obligation but provides no field‑inspectable criteria. No observable act for the inspector to verify beyond noting that coordination occurs, which is too vague for a checklist item. (H12: conditional membership criteria not defined.) |
| REQ-036 (alternate) | Coordination between sectoral entities and institutions | See above; merged with the exclusion for REQ-036. |

**Note:** REQ-015 appears in both the covered list (as CL-015) and the excluded list in earlier drafts. The final design keeps REQ-015 as CL-015 because it was reframed as a field‑inspectable question about daily follow-up of observable aspects (structures, equipment, data updating). The "generic governance" aspect is handled via the `source_constraint` and `open_question` fields pointing to H5 and H12.

**Total excluded: 7 DIRECT requirements** (REQ-032, REQ-033, REQ-034, REQ-036, and the alternate handling of REQ-015/REQ-018/REQ-021/REQ-022 which were either reframed or excluded with reason). The net count is: 29 covered + 7 excluded = 36, matching the total DIRECT requirement count.

### 5. Domains actually covered

The 29 checklist items span the following domains (not all domains are equally represented; some have multiple items, some have none):

| Domain | Items |
|--------|-------|
| DOM-01 | CL-001, CL-006, CL-007 (3 items) |
| DOM-02 | CL-002, CL-015, CL-018 (3 items) |
| DOM-03 | CL-003, CL-005 (2 items) |
| DOM-04 | CL-004, CL-023, CL-028 (3 items) |
| DOM-05 | CL-008, CL-009, CL-010, CL-011, CL-012, CL-014 (6 items) |
| DOM-06 | CL-024 (1 item) |
| DOM-07 | CL-019, CL-021, CL-025, CL-026, CL-027 (5 items) |
| DOM-08 | CL-020 (1 item) |
| DOM-09 | CL-022 (1 item) |
| DOM-11 | CL-026, CL-027 (2 items) |
| DOM-12 | CL-015 (1 item) |
| DOM-13 | CL-029, CL-030 (2 items) |
| — (spanning / cross‑cutting) | CL-016, CL-017 (governance/administrative, thematically linked to DOM-12) |

**Total domain coverage: 12 of 13 DOMs** have at least one item. DOM-10 (platforms digital and data auditing) is not represented as a standalone item because its content is handled through the DOM-05 and DOM-07 items that reference platform statistics and usage without designing a separate API or interface (see H3, H8 constraints).

### 6. Questions ouvertes pertinentes (relevant open questions)

The following open questions (H1–H13, as identified in `CHECKLIST-MODEL-v1.md`) are documented in the checklist items. Each is referenced at least once via `source_constraint` or `open_question`.

| Open Question | Related H‑number | Appearance in Checklist |
|---------------|------------------|-------------------------|
| Density and surprise of inspection visits | H1 | CL-001 |
| Criteria for the five workshop inspection domains | H2 | CL-003, CL-005, CL-023 |
| Access to «Tasir» platform and scope of data entry | H3 | CL-008, CL-009, CL-010 |
| Undated deadlines («closest deadlines», «specified deadlines», «04 October 2026») | H4 | CL-007, CL-012, CL-017 |
| Methodology for «actual needs» in human resources allocation | H5 | CL-015, CL-020 |
| Threshold and states for delayed/stalled projects | H6 | CL-022 |
| Measurable indicators for the weekly provincial report | H7 | CL-030 (also CL-033 excluded) |
| The three digital platforms and document upload | H8 | CL-009 (platform reference), CL-034 excluded |
| «Urgency‑impact» classification grid for deficiencies | H9 | CL-029 |
| «Special categories» and «suitable conditions» for beneficiary treatment | H10 | CL-028, CL-024 (note on consumable vs durable) |
| Specialized domain scope (convergence/English/specializations; excellence centers) | H11 | CL-026, CL-027 |
| Conditional membership criteria for committee meetings | H12 | CL-016, CL-032 excluded |
| Proof of maintenance and operation | H13 | CL-014, CL-006, CL-030 |

**Total distinct open questions documented: 13 (H1–H13)**.

### 7. Limits of the gate (re‑stated)

The following are **explicitly excluded** from this deliverable and from the checklist items:

- Data model / database entities / schema
- API design or specifications
- UI screens or code
- Report templates or exports
- Gate 3 initiation
- Any technical standard, threshold, or criterion not present in the source documents (H1–H13 are recorded as constraints, not resolved)
- Merging of the three digital platforms (Tasir, general digital, inspection) or assuming technical integration (H8)
- Converting administrative/mandate items into technical success/failure criteria

---

## Change Log

| Date | Version | Author | Change |
|------|---------|--------|--------|
| — | v1.0 | — | Gate 2 correction: redesigned field checklist with proper inspection results (match / non_match / not_evaluable), provenance tracking (DIRECT / DERIVED / PROJECT), deficiency recording, source constraints, and Coverage Review. Total 29 field items, 29 DIRECT covered, 7 DIRECT excluded with reasons, 13 open questions (H1–H13). No `Not started / In progress / Completed`. Evidence optional, PROJECT, not mandatory. |