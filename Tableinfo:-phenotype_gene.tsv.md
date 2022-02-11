This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

Each row in this table is equivalent to the statement "phenotype X is known to be associated with gene Y", for one particular (phenotype X, gene Y) pair; contents are autoloaded from HPO by the submission prep script, which adds two sets of records (with any redundancies collapsed):

* one row for every gene term associated with every phenotype term used in [collection_phenotype.tsv](./TableInfo:-collection_phenotype.tsv) or [subject_phenotype.tsv](./TableInfo:-subject_phenotype.tsv)
* one row for every phenotype term associated with every gene term appearing in [biosample_gene.tsv](./TableInfo:-biosample_gene.tsv)

All associations expressed in this table have been predetermined by the curators of the Human Phenotype Ontology: the associations included in `phenotype_gene.tsv` for a given submission will be those that contain terms from either of the two ontologies (HPO, Ensembl) in submitter-prepared tables.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**phenotype** | A valid Human Phenotype Ontology term | Required | string | [Human Phenotype Ontology lookup](https://hpo.jax.org/app/) <br /> Examples: `HP:0000349`, `HP:0012425`
**gene** | An Ensembl gene ID | Required |  string |  Example: `ENSG00000010404`