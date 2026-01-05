# EML responsibility roles controlled vocabulary

This controlled vocabulary enumerates the allowed **EML Party responsibility roles** (EML `RoleType`) used to describe how a person or organization is associated with a dataset or other resource (for example, author, originator, custodian/steward, distributor, and point of contact). Each row provides a stable AKSDB identifier (`concept_iid`) for joining and governance, and the exact EML machine value (`term_code`) that should be written into EML metadata.

The vocabulary also includes optional crosswalks to ISO 19115 `CI_RoleCode` values via `close_match_ids` when a reasonable “close match” exists.

## Controlled vocabulary file

- **Controlled vocabulary name / table name:** `eml_responsibility_roles_iso.csv`  
- **Label:** EML responsibility roles

## Columns

| Column label | Column name | Description |
|---|---|---|
| Concept identifier | `concept_iid` | Stable, project-minted identifier for the concept. Used as the primary key for joins and internal governance (do not recycle). Pattern in this vocab: `aksdb:eml_responsibility_role/<RoleTypeValue>`. |
| EML role code | `term_code` | The exact machine-readable EML `RoleType` literal value to write into EML (case sensitive). Examples include `principalInvestigator` and `pointOfContact`. |
| Preferred label | `pref_label` | Human-readable display label for the role. |
| Alternative labels | `alt_labels` | Optional synonyms and variants for search and display. Multi-values are encoded as `{value1|value2|...}`. |
| Definition | `definition` | Short definition of the role concept (project-readable). |
| Status | `status` | Governance status for the concept. Allowed values: `accepted`, `proposed`, `deprecated`, `draft`. |
| Created | `created` | Date the row/concept was introduced to the vocabulary in ISO format `YYYY-MM-DD`. |
| Modified | `modified` | Date the row/concept was last changed in ISO format `YYYY-MM-DD`. |
| Scope note | `scope_note` | Optional usage guidance and boundaries for applying the role. |
| Related identifiers | `related_ids` | Optional related concept identifiers (non-hierarchical). Multi-values are encoded as `{value1|value2|...}`. |
| Exact match identifiers | `exact_match_ids` | External identifier(s) that are considered exact matches. In this vocab this is the authoritative EML XSD URL used as the source definition for RoleType. |
| Close match identifiers | `close_match_ids` | External identifier(s) that are close (not exact) matches. Here this is used for ISO 19115 `CI_RoleCode` crosswalks when applicable. Multi-values are encoded as `{value1|value2|...}`. |
| Replaced by | `replaced_by` | If `status=deprecated`, the `concept_iid` of the preferred replacement concept. |
| Source | `source` | Human-readable documentation URL for the authority defining the vocabulary values (here: EML Party/RoleType documentation). |
| Note | `note` | Optional editorial notes and provenance details. Multi-values are encoded as `{value1|value2|...}`. |

## References

- EML Party / RoleType documentation: see `source` column in `eml_responsibility_roles_iso.csv`.
- EML 2.1.1 Party schema (XSD): see `exact_match_ids` column in `eml_responsibility_roles_iso.csv`.
- ISO 19115 `CI_RoleCode` codelist (used for close matches): see the ISO codelist URL referenced in the `note` column for each mapped term.
