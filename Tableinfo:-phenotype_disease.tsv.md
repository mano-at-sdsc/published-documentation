WAIT FOR IT

Each row in this table is equivalent to the statement "phenotype X is known to be associated with disease Y", for one particular (phenotype X, disease Y) pair; contents are autoloaded from HPO by the submission prep script, which will add relevant rows for every phenotype term and every disease term used in submitter-prepared tables

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`