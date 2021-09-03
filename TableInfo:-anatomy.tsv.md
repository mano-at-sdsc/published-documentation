This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The anatomy.tsv table will have as many rows as the number of unique UBERON terms appearing in the `anatomy` column of [biosample.tsv](./TableInfo:-biosample.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid UBERON term | Required |  string | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) <br/> Example: `UBERON:0006956`
**name** | A short, human-readable, machine-read-friendly label for this UBERON term| Required | string
**description** | A human-readable description of this UBERON term |  Optional | string
**synonyms** | A list of synonyms for this term as identified by the UBERON metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 
