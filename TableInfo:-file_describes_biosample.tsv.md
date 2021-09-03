Association between a file and a biosample that it describes

If populated, `file_describes_biosample.tsv` will contain one row for every file linked to a biosample that it describes.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any files that describe one or more specific biosamples, this table should be left empty.
- If you have exactly one file describing or summarizing each biosample, this table will have the same number of rows as [biosample.tsv](./TableInfo:-biosample.tsv).
- If you have five files describing each biosample, this table will have five times as many rows as [biosample.tsv](./TableInfo:-biosample.tsv).
- If your biosamples are grouped in batches of five, with each batch described by a single file, then this table will have one fifth as many rows as [biosample.tsv](./TableInfo:-biosample.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**file_id_namespace** | Identifier namespace for this file | Required | string | This will be the value of `id_namespace` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**file_local_id** | The ID of this file | Required | string | This will be the value of `local_id` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row.
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namnespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
