Association between a file and a collection that it describes

If populated, `file_describes_collection.tsv` will contain one row for every file that describes an entire collection defined by your program.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any files that summarize entire collections, this table should be left empty.
- If you have exactly one file describing each of your collections, this table will have the same number of rows as [collection.tsv](./TableInfo:-collection.tsv)
- If you have five files summarizing each collection, this table will have five times as many rows as [collection.tsv](./TableInfo:-collection.tsv)

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**file_id_namespace** | Identifier namespace for this file  | Required | string | This will be the value of `id_namespace` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row. If your program has not registered multiple CFDE identifier namnespaces, this will be exactly the same value for all rows.
**file_local_id** | The ID of this file | Required | string | This will be the value of `local_id` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row.
**collection_id_namespace** | Identifier namespace for this collection | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
