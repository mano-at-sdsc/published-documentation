This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The phenotype_disease.tsv table will have as many rows as the total number of Disease Ontology terms associated (by the HPO curators) with all of the Human Phenotype Ontology terms appearing in [collection_phenotype.tsv](./TableInfo:-collection_phenotype.tsv) or [subject_phenotype.tsv](./TableInfo:-subject_phenotype.tsv).

Each row in this table is equivalent to the statement "phenotype X is known to be associated with disease Y", for one particular (phenotype X, disease Y) pair; contents are autoloaded from HPO by the submission prep script, which adds relevant rows for every disease term associated with any phenotype term used in submitter-prepared tables


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`