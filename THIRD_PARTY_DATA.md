# Third-party / upstream datasets and terms

This project harmonizes and redistributes (where permitted) datasets from multiple
upstream sources. Upstream datasets may have their own licenses, attribution
requirements, and usage constraints.

## Source of truth
For each dataset release (source or harmonized), the following fields in the
registry record the relevant terms:
- `packages.license`
- `packages.intellectual_rights`
- `packages.source_citation`
- `packages.landing_page_url`
- `packages.doi` (if available)

See: `metadata/registry/packages.csv`

## What our licenses cover
- `LICENSE` covers project software.
- `LICENSE-DATA` covers harmonized outputs created by this project **to the extent
  those outputs are not restricted by upstream terms**.
- Where upstream terms impose additional requirements or restrictions, those apply.

## How to add a new upstream dataset
When adding a dataset, ensure the corresponding `packages.csv` row includes:
- license identifier (prefer SPDX or a clear label)
- rights statement (if non-standard)
- landing page URL
- preferred source citation text
- DOI if available

Also add a dataset page under:
- `docs/datasets/<ds_iid>/index.md`
and include any special licensing or attribution instructions.

## Redistribution caveat
If an upstream dataset’s terms do not allow redistribution, the public repo should:
- store only derived/harmonized outputs that are permitted, and/or
- store pointers (landing_page_url) and scripts to fetch upstream data, rather than
  the data itself.
