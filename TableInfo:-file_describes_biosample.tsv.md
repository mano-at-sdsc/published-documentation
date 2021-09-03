Association between a file and a biosample it describes

If populated, `file_describes_biosample.tsv` will contain one row for every file linked to a biosample it describes.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have files that describe one or more particular individual biosamples, this table should be left empty.
- If you have exactly one file describing or summarizing each biosample, this table will have the same number of rows as [biosample.tsv](./TableInfo:-biosample.tsv)
- If you have five files describing each biosample, this table will have five times as many rows as [biosample.tsv](./TableInfo:-biosample.tsv)
- If you have one file describing each batch of five biosamples, this table will have one fifth as many rows as [biosample.tsv](./TableInfo:-biosample.tsv)


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**file_id_namespace** | Identifier namespace for this file | Required | string | This will be the value of `id_namespace` in the row in [file.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namnespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.




Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**file_id_namespace** |Identifier namespace for this file  | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [file.tsv](./TableInfo:-file.tsv) for the file for this biosample. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**file_local_id**|The ID of this file | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string |  For each row this will be the value of `local_id` in [file.tsv](./TableInfo:-file.tsv) for the file that describes this biosample. If a biosample has multiple files, it should have multiple *rows*. **Concatenating values in this column will invalidate your submission**
**biosample_id_namespace** |Identifier namespace for this biosample | Required if table is populated|  If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [biosample.tsv](./TableInfo:-biosample.tsv) for the biosample associated with this file. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**biosample_local_id** | The ID of this biosample | Required if table is populated|  If a row has this value, it must have a value for every column<br /><br /> Value type is string | For each row this will be the value of `local_id` in [biosample.tsv](./TableInfo:-biosample.tsv) for the biosample associated with this file. 