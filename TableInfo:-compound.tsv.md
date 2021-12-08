This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The compound.tsv table will have as many rows as the number of unique PubChem terms appearing in the [substance.tsv](./TableInfo:-substance.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid PubChem term | Required |  string | Example: `SID:5381226`
**name** | A short, human-readable, machine-read-friendly label for this PubChem CID| Required | string
**description** | A human-readable description of this PubChem CID |  Optional | string
**synonyms** | A list of synonyms for this PubChem CID | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 
