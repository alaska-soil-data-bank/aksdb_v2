# Vocabularies::vocab

This section defines **controlled vocabularies** used across the registry and (optionally) across harmonized products.

## Authoritative principle
- If a field references a controlled vocabulary (via `controlled_vocab` in `data_dictionary.csv`), the allowed values must be defined here (human-readable) and mirrored in a machine-readable vocab file (.csv).

## Registry vocabularies
- [role_scheme](role_scheme.md)
- [eml_responsibility](eml_responsibility.md)
- [role_degree](role_degree.md)
- [party_type](party_type.md)
- [entity_type](entity_type.md)
- [dataset_status](dataset_status.md) (optional)

## How to reference vocabs
In `data_dictionary.csv`, use:
- `controlled_vocab = <vocab_name>` (e.g., `entity_type_vocab`)
and include a `doc_ref` pointing to the relevant vocab page anchor.
