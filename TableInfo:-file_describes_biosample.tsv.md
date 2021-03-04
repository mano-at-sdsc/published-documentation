If fully filled, `file_describes_biosample.tsv` will contain one row for every combination of file and biosample in your program.

If a row is filled, it must be filled for all columns, but there is no minimum number of rows that must be filled. You can choose any subset of files/biosamples.

Some examples:   
- If you have exactly one biosample in each file, this table will have the same number of rows as [file.tsv](./TableInfo:-file.tsv)
- If you have two biosamples in every file, this table will have two rows for each file, each linking to a single biosample
- If you have 3 files for each biosample, this table will have 3 rows for each biosample, each linking to a single file


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**file_id_namespace** |Identifier namespace for this file  | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [file.tsv](./TableInfo:-file.tsv) for this file. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**file_local_id**|The ID of this file | Required if table is populated |  For each row this will be the value of `local_id` in [file.tsv](./TableInfo:-file.tsv) for the file that describes this biosample. If a biosample has multiple files, it should have multiple *rows*. **Concatenating values in this column will invalidate your submission**
**biosample_id_namespace** |Identifier namespace for this biosample | Required if table is populated|  If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [biosample.tsv](./TableInfo:-biosample.tsv) for the file that describes this biosample. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**biosample_local_id** | The ID of this biosample | Required if table is populated|  If a row has this value, it must have a value for every column<br /><br /> Value type is string | For each row this will be the value of `local_id` in [biosample.tsv](./TableInfo:-biosample.tsv) for the file that describes this biosample. 