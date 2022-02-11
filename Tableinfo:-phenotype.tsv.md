This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The phenotype.tsv table will have as many rows as the number of unique Human Phenotype Ontology terms appearing in [collection_phenotype.tsv](./TableInfo:-collection_phenotype.tsv) or [subject_phenotype.tsv](./TableInfo:-subject_phenotype.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A valid Human Phenotype Ontology term | Required | string | [Human Phenotype Ontology lookup](https://hpo.jax.org/app/) <br /> Examples: `HP:0000349`, `HP:0012425`
**name** | A short, human-readable, machine-read-friendly label for this Human Phenotype Ontology term | Required | string
**description** | A human-readable description of this Human Phenotype Ontology term |  Optional | string
**synonyms** | A list of synonyms for this term as identified by the Human Phenotype Ontology metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 