Association between a biosample and a gene of interest

If populated, `biosample_gene.tsv` will contain one row for every biosample linked to an Ensembl gene especially relevant to it. This field is meant to be used for cases such as knockouts, knockins, genetic diseases or other use cases that tie a small number of genes to a biosample. It should not be used to enumerate all genes tied to an object: don't (for example) explicitly link each gene (of thousands) that happens to be expressed in a biosample: the gene associations here should be those that are specific and directly relevant to the study being performed.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any biosamples associated with genes, this table should be left empty.
- If you have exactly one gene of interest for each biosample, this table will have the same number of rows as [biosample.tsv](./TableInfo:-biosample.tsv)
- If you have two genes especially relevant to each biosample, this table will have twice as many rows as [biosample.tsv](./TableInfo:-biosample.tsv)


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
**gene** | An Ensembl gene ID | Required | string | This must be a valid Ensembl gene ID <br/> Example: `ENSG00000010404`