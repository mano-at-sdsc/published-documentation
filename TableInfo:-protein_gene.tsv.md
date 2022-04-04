This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

Each row in this table is equivalent to the statement "protein X is known to be associated with gene Y", for one particular (protein X, gene Y) pair; contents are autoloaded where available from UniProtKB by the submission prep script, which adds one row for every gene term associated with every protein term used in [collection_protein.tsv](./TableInfo:-collection_protein.tsv).

**USERS PLEASE NOTE: the creation of this table is currently stubbed pending reevaluation of the benefits of automating its construction in this way. The submission prep script will generate a header-only version of the TSV for this table, independent of any included protein values. This is expected and will not invalidate your submission.**

All associations expressed in this table have been predetermined by the UniProt curators: associations included in `protein_gene.tsv` for a given submission will be those that contain protein terms used in submitter-prepared tables.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**protein** | A UniProt Knowledgebase (UniProtKB) protein accession (AC)| Required | string | Example: `Q6GZX4`
**gene** | An Ensembl gene ID | Required |  string |  Example: `ENSG00000010404`