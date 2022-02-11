This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Built by submitter") for submission. Once the "Built by submitter" tables are prepared, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information in the user-built tables.

The analysis_type.tsv table will have as many rows as the number of unique OBI terms appearing in the `analysis_type` column of [file.tsv](./TableInfo:-file.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid OBI term | Required | string | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) <br/> Example: `OBI:0002763` 
**name** | A short, human-readable, machine-read-friendly label for this OBI term| Required | string
**description** | A human-readable description of this OBI term | Optional | string
**synonyms** | A list of synonyms for this term as identified by the OBI metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null
