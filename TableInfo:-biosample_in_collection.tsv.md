Assignment of a biosample as a member of a collection

The biosample_in_collection table will contain one row per biosample-collection pair in your Program

If a row is filled, it must be filled for all columns, but there is no minimum number of rows that must be filled. You can choose any subset of collections/biosamples. Not all collections need biosamples, not all biosamples need to be part of a collection.


Some examples:   
- If you have exactly one collection, and want all your biosamples in that collection, this table will have the same number of rows as [biosample.tsv](./TableInfo:-biosample.tsv), and the value for columns 3 and 4 will be the same for this entire table
- If you have exactly one collection, and only want *a subset* your biosamples in that collection, you will have you will have an equal number of rows and biosamples in your subset, where the value for columns 3 and 4 are the same for the entire table
- If each biosample is associated with exactly one collection, you will have an equal number of rows and biosamples
- If a biosample should appear in two unrelated collections, that biosample will need two rows, where the first two columns are duplicated, and the last two columns specify the two different collections
- If a biosample should appear in two or more collections that are defined as being nested in the [collection_in_collection](./TableInfo:-collection_in_collection.tsv) table, it should only appear in one row, with the collection_id_namespace and collection_local_id for the most specific collection. It will inherit the parent collections automatically.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**biosample_id_namespace** | Identifier namespace for this biosample | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row (each biosample), this will be the value of `id_namespace` in [biosample.tsv](./TableInfo:-biosample.tsv) for this biosample. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `collection_id_namespace` column
**biosample_local_id** | The ID of this biosample |  Required if table is populated | If a row has this value, it must have a value for every column<br /><br /> Value type is string | For each row (each biosample), this will be the value of `local_id` in [biosample.tsv](./TableInfo:-biosample.tsv) for this biosample
**collection_id_namespace** | Identifier namespace for this collection | Required if table is populated | If a row has this value, it must have a value for every column<br /><br />Value type is string | For each row (each biosample), this will be the value of `id_namespace` in [collection.tsv](./TableInfo:-collection.tsv) for the collection this biosample was taken from. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows and in the `biosample_id_namespace` column
**collection_local_id** | The ID of this collection string |  Required if table is populated | If a row has this value, it must have a value for every column<br /><br /> Value type is string | For each row (each biosample), this will be the value of `local_id` in [collection.tsv](./TableInfo:-collection.tsv) for the collection this biosample was taken from. If a biosample should be part of multiple collections, it should have multiple *rows*. **Concatenating values in this column will invalidate your submission**