Association between a collection and an UBERON term

Each row in this table is equivalent to the statement "the contents of collection X directly relate to the study of biofluid Y", for one particular (collection X, biofluid Y) pair.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any collections associated with biofluids, this table should be left empty.
- If you have exactly one biofluid associated with each of your collections, this table will have as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If you have five biofluids associated with each collection, this table will have five times as many rows as [collection.tsv](./TableInfo:-collection.tsv).
- If some but not all of your collections are associated with one or more biofluids, this table will contain one row for each biofluid assigned to each such collection (and the resulting row count will not have any obvious relationship to the number of rows in [collection.tsv](./TableInfo:-collection.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**collection_id_namespace** | Identifier namespace for this collection [part 1 of 3-component composite primary key] | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection [part 2 of 3-component composite primary key] | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
**biofluid** | | A valid UBERON term [part 3 of 3-component composite primary key] | Required |  string | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) <br/> Example: `UBERON:0001090`