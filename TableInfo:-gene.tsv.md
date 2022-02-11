This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The gene.tsv table will have as many rows as the number of unique Emsembl terms appearing in the `gene` column of [biosample_gene.tsv](./TableInfo:-biosample_gene.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | An Ensembl gene ID | Required |  string |  Example: `ENSG00000010404`
**name** | The Ensembl 'Name' for this gene (e.g. 'BRCA1')| Required | string
**description** | The Ensembl 'Description' of this gene (e.g. 'BRCA1 DNA repair associated' |  Optional | string
**synonyms** | A list of Ensembl 'Gene synonyms' for this gene (e.g. ['BRCC1', 'FANCS', 'PPP1R53', 'RNF53']) | Optional | array
**organism** | An NCBI Taxonomy Database ID identifying this gene's source organism (e.g. 'NCBItxid9606' | string 
