`collection_defined_by_project` optionally attaches a unique primary generating project to a C2M2 collection: this is meant to express the same relationship between a project and a collection as is (for example) expressed by the project foreign key in the [file.tsv](./TableInfo:-file.tsv) table: "collection `C` was defined under the auspices of project `P`," just as "file `F` was created by project `P`."

Usage notes:

* Not every collection will have a well-defined project under which it was created, so **populating `collection_defined_by_project.tsv` is optional.**

* The `collection_defined_by_project.tsv` table will contain _at most_ one row for each collection listed in [collection.tsv](./TableInfo:-collection.tsv).

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-inter-entity-linkages) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**collection_id_namespace** | Identifier namespace for this collection  | Required | string | This will be the value of `id_namespace` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**collection_local_id** | The ID of this collection | Required | string | This will be the value of `local_id` in the row in [collection.tsv](./TableInfo:-collection.tsv) corresponding to the collection referenced in this row.
**project_id_namespace** | Identifier namespace for this project | Required | string | This will be the value of `id_namespace` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the project referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**project_local_id** | The ID of this project | Required | string | This will be the value of `local_id` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the project referenced in this row.
