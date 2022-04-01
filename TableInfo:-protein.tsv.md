This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically proteinrate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The protein.tsv table will have as many rows as the number of unique UniProt terms appearing in the `protein` column of [biosample_protein.tsv](./TableInfo:-biosample_protein.tsv) and [collection_protein](./TableInfo:-collection_protein.tsv)


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A UniProt Knowledgebase (UniProtKB) protein ID (e.g. 'P94485') | Required |  string |  Example: `P0AFN4`
**name** | The UniProt recommended name of this protein (e.g. 'Uncharacterized protein YnaG')| Required | string
**description** | A description of this protein |  Optional | string
**synonyms** | A list of alternate names for this protein | Optional | array
**organism** | OPTIONAL: An NCBI Taxonomy Database ID identifying this protein's source organism (e.g. 'NCBI:txid9606') | string 
