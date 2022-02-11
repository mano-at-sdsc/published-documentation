This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The ncbi_taxonomy.tsv table will have as many rows as the number of unique NCBI Taxon IDs appearing in the `taxonomy_id` column of [subject_role_taxonomy.tsv](./TableInfo:-subject_role_taxonomy.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | An NCBI Taxonomy Database ID | Required | string | [NCBI Taxonomy Browser](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi) <br/> --- <br/> **_Note formatting:_** be sure to prefix numeric taxon IDs with "`NCBI:txid`" <br/> --- <br/> Example (for "[9606](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?mode=Info&id=9606)"): `NCBI:txid9606`
**clade** | The phylogenetic level (e.g. species, genus) assigned to this taxon | Required | string | Examples: `species`, `genus`, `order`
**name** | A short, human-readable, machine-read-friendly label for this taxon | Required | string
**description** | A human-readable description of this taxon | Optional | string
**synonyms** | A list of synonyms for this taxon as identified by the NCBI metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null
