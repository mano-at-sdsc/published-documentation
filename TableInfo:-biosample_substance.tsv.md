Association between a biosample and a substance of interest

If populated, `biosample_substance.tsv` will contain one row for every biosample linked to a PubChem substance experimentally associated it. This field is meant to be used for biosample studies analyzing toxins or drugs; bench trials of chemicals on tissue samples; and any other use cases that tie a small number of substances to a biosample.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any biosamples associated with substances, this table should be left empty.
- If you have exactly one substance of interest for each biosample, this table will have the same number of rows as [biosample.tsv](./TableInfo:-biosample.tsv)
- If you have two substances especially relevant to each biosample, this table will have twice as many rows as [biosample.tsv](./TableInfo:-biosample.tsv)


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
**substance** | A PubChem substance ID (SID) describing this substance | Required | string | This must be a valid PubChem ID <br/> Example: `5381226`