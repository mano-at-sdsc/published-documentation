Each row in this table asserts "the second listed collection is a subcollection of the first listed collection."

Usage notes:
* Collections need only be explicitly linked to their _immediate parents_ via `collection_in_collection.tsv`. Transitive containment of each collection (by more distant ancestor collections than its immediate parent collection) will be automatically inferred.

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-expressing-containment-relationships) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**superset_collection_id_namespace** | ID of the identifier namespace for the parent in this parent-child collection pair | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the _parent_ collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**superset_collection_local_id** | The ID of the containing (parent) collection in this parent-child collection pair | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the _parent_ collection referenced in this row.
**subset_collection_id_namespace** | ID of the identifier namespace for the child in this parent-child collection pair | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the _child_ collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subset_collection_local_id** | The ID of the contained (child) collection in this parent-child collection pair | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the _child_ collection referenced in this row.
