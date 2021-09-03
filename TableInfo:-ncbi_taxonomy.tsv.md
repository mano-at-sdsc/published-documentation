This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The ncbi_taxonomy.tsv table will have as many rows as the number of unique NCBI Taxon IDs appearing in the `taxonomy_id` column of [subject_role_taxonomy.tsv](./TableInfo:-subject_role_taxonomy.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | An NCBI Taxonomy Database ID | Required | string | [NCBI Taxonomy Browser](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi) <br/> --- <br/> Note formatting: be sure to prefix numeric taxon IDs with "`NCBI:txid`" <br/> --- <br/> Example (for "[9606](https://www.ncbi.nlm.nih.gov/Taxonomy/Browser/wwwtax.cgi?mode=Info&id=9606)"): `NCBI:txid9606`
**clade** | The phylogenetic level (e.g. species, genus) assigned to this taxon | Required | string | Examples: `species`, `genus`, `order`
**name** | A short, human-readable, machine-read-friendly label for this taxon | Required | string
**description** | A human-readable description of this taxon | Optional | string
**synonyms** | A list of synonyms for this taxon as identified by the NCBI metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null
