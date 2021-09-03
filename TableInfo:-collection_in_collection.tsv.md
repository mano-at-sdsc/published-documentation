Each row in this table asserts "the second listed collection is a subcollection of the first listed collection."

Usage notes:
* Collections need only be explicitly linked to their _immediate parents_ via `collection_in_collection.tsv`. Transitive containment of each project (by more distant ancestor projects than its immediate parent project) will be automatically inferred.

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-expressing-containment-relationships) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**superset_collection_id_namespace** | ID of the identifier namespace for the parent in this parent-child project pair | Required | string | This will be the value of `id_namespace` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _parent_ project referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**superset_collection_local_id** | The ID of the containing (parent) project in this parent-child project pair | Required | string | This will be the value of `local_id` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _parent_ project referenced in this row.
**subset_collection_id_namespace** | ID of the identifier namespace for the child in this parent-child project pair | Required | string | This will be the value of `id_namespace` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _child_ project referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subset_collection_local_id** | The ID of the contained (child) project in this parent-child project pair | Required | string | This will be the value of `local_id` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _child_ project referenced in this row.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**superset_collection_id_namespace** | ID of the identifier namespace corresponding to the top-level C2M2 metadataset containing the superset collection  | Required if table is populated | Value type is string | This will be the value of `id_namespace` in [collection.tsv](./TableInfo:-collection.tsv) for this collection. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows of this column and the `subset_collection_id_namespace` column 
**superset_collection_local_id** | The ID of the superset collection | Required if table is populated |Value type is string |  This will be a value of `local_id` in [collection.tsv](./TableInfo:-collection.tsv)
**subset_collection_id_namespace** |ID of the identifier namespace corresponding to the top-level C2M2 metadataset containing the subset collection | Required if table is populated | Value type is string | This will be the value of `id_namespace` in [collection.tsv](./TableInfo:-collection.tsv) for this collection. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows of this column and the `superset_collection_id_namespace` column
**subset_collection_local_id** | The ID of the subset collection | Required if table is populated |Value type is string | This will be a value of `local_id` in [collection.tsv](./TableInfo:-collection.tsv)