This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The disease.tsv table will have as many rows as the number of unique Disease Ontology terms appearing in the `disease` field of [biosample_disease.tsv](./TableInfo:-biosample_disease.tsv), [collection_disease.tsv](./TableInfo:-collection_disease.tsv) or [subject_disease.tsv](./TableInfo:-subject_disease.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`
**name** | A short, human-readable, machine-read-friendly label for this Disease Ontology term | Required | string
**description** | A human-readable description of this Disease Ontology term |  Optional | string
**synonyms** | A list of synonyms for this term as identified by the Disease Ontology metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 