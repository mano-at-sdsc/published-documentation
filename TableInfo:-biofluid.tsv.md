This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The biofluid.tsv table will have as many rows as the number of unique UBERON terms appearing in the `biofluid` column of [biosample.tsv](./TableInfo:-biosample.tsv) or [collection_biofluid.tsv](./TableInfo:-collection_biofluid.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid UBERON term | Required |  string | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) <br/> Example: `UBERON:0001090`
**name** | A short, human-readable, machine-read-friendly label for this UBERON term| Required | string
**description** | A human-readable description of this UBERON term |  Optional | string
**synonyms** | A list of synonyms for this term as identified by the UBERON metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 
