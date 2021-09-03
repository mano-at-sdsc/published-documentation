This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the others are complete, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the completed tables.

The disease.tsv table should have as many rows as the number of unique Disease Ontology IDs found in either the [biosample_disease.tsv](./TableInfo:-biosample_disease.tsv) or [subject_disease.tsv](./TableInfo:-subject_disease.tsv) association tables.


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | A Disease Ontology term | Required | Value must be a valid Disease Ontology ID | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Example valid Disease Ontology IDs: `DOID:8778`, `DOID:0060249`
**name** | A short, human-readable, machine-read-friendly label for this Disease Ontology term | Required | Value type is string
**description** | A human-readable description of this Disease Ontology term |  Optional | Value type is string
**synonyms** | A list of synonyms for this term as identified by the Disease Ontology metadata | Optional | Value type is JSON array of strings | provide empty JSON array `[]` if value is null 