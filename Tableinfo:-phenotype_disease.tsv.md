This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

Each row in this table is equivalent to the statement "phenotype X is known to be associated with disease Y", for one particular (phenotype X, disease Y) pair; contents are autoloaded from HPO by the submission prep script, which adds two sets of records (with any redundancies removed):

* one row for every disease term associated with every phenotype term used in [collection_phenotype.tsv](./TableInfo:-collection_phenotype.tsv) or [subject_phenotype.tsv](./TableInfo:-subject_phenotype.tsv)
* one row for every phenotype term associated with every disease term appearing in [biosample_disease.tsv](./TableInfo:-biosample_disease.tsv), [collection_disease.tsv](./TableInfo:-collection_disease.tsv) or [subject_disease.tsv](./TableInfo:-subject_disease.tsv)

All associations expressed in this table been predetermined by the curators of the Human Phenotype Ontology.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**phenotype** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`