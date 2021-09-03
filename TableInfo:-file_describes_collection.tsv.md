If populated, `file_describes_collection.tsv` will contain one row for every file that describes an entire collection defined by your program.

All fields are required; this table can be empty (header-row only), but any non-header rows must have all fields populated

Some examples:   
- If you don't have any files that summarize entire collections, this table should be left empty.
- If you have exactly one file describing each of your collections, this table will have the same number of rows as [collection.tsv](./TableInfo:-collection.tsv)
- If you have five files summarizing each collection, this table will have five times as many rows as [collection.tsv](./TableInfo:-collection.tsv)


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**file_id_namespace** |Identifier namespace for this file  | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [file.tsv](./TableInfo:-file.tsv) for the file for this biosample. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**file_local_id**|The ID of this file | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string |  For each row this will be the value of `local_id` in [file.tsv](./TableInfo:-file.tsv) for the file that describes this biosample. If a biosample has multiple files, it should have multiple *rows*. **Concatenating values in this column will invalidate your submission**
**biosample_id_namespace** |Identifier namespace for this biosample | Required if table is populated|  If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row this will be the value of `id_namespace` in [biosample.tsv](./TableInfo:-biosample.tsv) for the biosample associated with this file. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**biosample_local_id** | The ID of this biosample | Required if table is populated|  If a row has this value, it must have a value for every column<br /><br /> Value type is string | For each row this will be the value of `local_id` in [biosample.tsv](./TableInfo:-biosample.tsv) for the biosample associated with this file. 