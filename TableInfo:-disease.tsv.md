This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The disease.tsv table will have as many rows as the number of unique Disease Ontology terms appearing in either the [biosample_disease.tsv](./TableInfo:-biosample_disease.tsv) or [subject_disease.tsv](./TableInfo:-subject_disease.tsv) association table files.


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`
**name** | A short, human-readable, machine-read-friendly label for this Disease Ontology term | Required | string
**description** | A human-readable description of this Disease Ontology term |  Optional | string
**synonyms** | A list of synonyms for this term as identified by the Disease Ontology metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 