Assignment of a subject as a member of a collection

If populated, `file_in_collection.tsv` will contain one row for every assignment of a file as a member of a collection.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any files contained in collections, this table should be left empty.
- If each file is contained in exactly one collection, this table will have the same number of rows as [file.tsv](./TableInfo:-file.tsv).
- If each file is simultaneously a member of three collections, this table will have three times as many rows as [file.tsv](./TableInfo:-file.tsv).

Usage note:
- If a file is a member of collection `X`, and collection `X` is itself a subcollection of some other collection `Y` (as expressed in the [collection_in_collection](./TableInfo:-collection_in_collection.tsv) table), then `file_in_collection.tsv` should only record the membership of the file in collection `X`: the file's (transitive) membership in collection `Y` will be automatically computed. In general, `file_in_collection.tsv` should record only the most specific (leaf-most) collection memberships: transitive membership of files in ancestor/superset collections will be automatically inferred from the containment relationships expressed in [collection_in_collection](./TableInfo:-collection_in_collection.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**file_id_namespace** | Identifier namespace for this file  | Required | string | This will be the value of `id_namespace` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**file_local_id** | The ID of this file | Required | string | This will be the value of `local_id` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row.
**collection_id_namespace** | Identifier namespace for this collection | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
