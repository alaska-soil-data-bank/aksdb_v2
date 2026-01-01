# How to cite AKSDB v2

## Please cite the harmonized product
If you use the harmonized AKSDB v2 data products, please cite the relevant product
release in `products/<product_slug>/releases/<release_slug>/`.

Recommended practice:
1) Cite the harmonized product (this project)
2) Cite the upstream datasets used to create it (see below)

## Also cite upstream datasets
Many upstream datasets have specific attribution requirements. The authoritative
citations are recorded in:
- `metadata/registry/packages.csv` (`source_citation`, `doi`, `landing_page_url`)

For a given harmonized product release, you can identify upstream components via:
- `packages.upstream_release_ids` (if populated), and then cite those releases.

## If you publish results
Please cite:
- the specific `release_slug` you used
- any DOI associated with that release (if minted)
- and upstream datasets per their required citations

## Questions
For questions, see the contacts listed in `metadata/registry/party_roles.csv`
for the relevant `release_id`.
