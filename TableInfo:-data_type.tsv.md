This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The data_type.tsv table will have as many rows as the number of unique EDAM terms appearing in the `data_type` column of [file.tsv](./TableInfo:-file.tsv).

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid EDAM `data:` term | Required | string | [EDAM `data:` term lookup](https://www.ebi.ac.uk/ols/ontologies/edam/terms?iri=http%3A%2F%2Fedamontology.org%2Fdata_0006&viewMode=All&siblings=false) <br/> Example: `data:2044`
**name** | A short, human-readable, machine-read-friendly label for this EDAM term| Required | string
**description** | A human-readable description of this EDAM term | Optional | string
**synonyms** | A list of synonyms for this term as identified by the EDAM metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null
