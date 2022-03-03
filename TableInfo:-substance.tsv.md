This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The substance.tsv table will have as many rows as the number of unique UBERON terms appearing in the `substance` column of [biosample_substance.tsv](./TableInfo:-biosample_substance.tsv).



Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A PubChem substance ID (SID) | Required |  string | Example: `SID:5381226`
**name** | A short, human-readable, machine-read-friendly label for this PubChem SID| Required | string
**description** | A human-readable description of this PubChem SID |  Optional | string
**synonyms** | A list of synonyms for this PubChem SID | Optional | array of strings
**compound**| The (unique) PubChem compound ID (CID) associated with this PubChem SID| Required | string

