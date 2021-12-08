This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The gene.tsv table will have as many rows as the number of unique Emsembl terms appearing in the `gene` column of [biosample_gene.tsv](./TableInfo:-biosample_gene.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | List of Ensembl genes directly referenced in this C2M2 submission | Required |  string |  Example: `ENSG00000010404`
**name** | The Ensembl 'Name' for this gene (e.g. 'BRCA1')| Required | string
**description** | The Ensembl 'Description' of this gene (e.g. 'BRCA1 DNA repair associated' |  Optional | string
**synonyms** | A list of Ensembl 'Gene synonyms' for this gene (e.g. ['BRCC1', 'FANCS', 'PPP1R53', 'RNF53']) | Optional | array
**organism** | An NCBI Taxonomy Database ID identifying this gene's source organism (e.g. 'NCBItxid9606' | string 
