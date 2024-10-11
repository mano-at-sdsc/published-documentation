Association between a collection and a Gene Ontology term

For collections with gene metadata, this table will have one row for each gene associated with each such collection.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any collections associated with genes, this table should be left empty.
- If you have exactly one gene associated with each collection, this table will have as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If you have five genes associated with each collection, this table will have five times as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If some but not all of your collections are associated with one or more genes, this table will contain one row for each gene assigned to each such collection (and the resulting row count will not have any obvious relationship to the number of rows in [collection.tsv](./TableInfo:-collection.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**collection_id_namespace** | Identifier namespace for this collection [part 1 of 3-component composite primary key] | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection [part 2 of 3-component composite primary key] | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
**gene** | An Ensembl gene ID [part 3 of 3-component composite primary key] | Required | string | This must be a valid Ensembl gene ID <br/> Example: `ENSG00000010404`