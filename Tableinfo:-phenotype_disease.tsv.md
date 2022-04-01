This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

Each row in this table is equivalent to the statement "phenotype X (from HPO) is equivalent to disease Y (from the Disease Ontology)", for one particular (phenotype X, disease Y) pair; contents are autoloaded from HPO metadata by the submission prep script, which adds one row for every disease term associated with every phenotype term used in [collection_phenotype.tsv](./TableInfo:-collection_phenotype.tsv) or [subject_phenotype.tsv](./TableInfo:-subject_phenotype.tsv).

All associations expressed in this table have been predetermined by the curators of the Human Phenotype Ontology: associations included in `phenotype_disease.tsv` for a given submission will be those that contain HPO phenotype terms in submitter-prepared tables.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**phenotype** | A valid Human Phenotype Ontology term | Required | string | [Human Phenotype Ontology lookup](https://hpo.jax.org/app/) <br /> Examples: `HP:0000349`, `HP:0012425`
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`