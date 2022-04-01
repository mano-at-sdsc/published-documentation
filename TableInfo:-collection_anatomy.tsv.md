Association between a collection and an UBERON term

Each row in this table is equivalent to the statement "the contents of collection X directly relate to the study of anatomy Y", for one particular (collection X, anatomy Y) pair.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any collections associated with anatomys, this table should be left empty.
- If you have exactly one anatomy associated with each of your collections, this table will have as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If you have five anatomys associated with each collection, this table will have five times as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If some but not all of your collections are associated with one or more anatomys, this table will contain one row for each anatomy assigned to each such collection (and the resulting row count will not have any obvious relationship to the number of rows in [collection.tsv](./TableInfo:-collection.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**collection_id_namespace** | Identifier namespace for this collection  | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
**anatomy** | | A valid UBERON term | Required |  string | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) <br/> Example: `UBERON:0006956`