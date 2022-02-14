Each row in this table asserts "the second listed project is a subproject of the first listed project."

Usage notes:
* `project_in_project.tsv` will contain one row for every parent->child (project->subproject) relationship in the project hierarchy a DCC has chosen to express. (If no subprojects are defined -- i.e. if a DCC is representing its data as governed by one big DCC-wide project -- this table may contain no data (non-header) rows.)

* Projects need only be explicitly linked to their _immediate parents_ via `project_in_project.tsv`. Transitive containment of each project (by more distant ancestor projects than its immediate parent project) will be automatically inferred.

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-expressing-containment-relationships) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**parent_project_id_namespace** | The identifier namespace for the parent in this parent-child project pair | Required | string | This will be the value of `id_namespace` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _parent_ project referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**parent_project_local_id** | The ID of the containing (parent) project in this parent-child project pair | Required | string | This will be the value of `local_id` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _parent_ project referenced in this row.
**child_project_id_namespace** | The identifier namespace for the child in this parent-child project pair | Required | string | This will be the value of `id_namespace` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _child_ project referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**child_project_local_id** | The ID of the contained (child) project in this parent-child project pair | Required | string | This will be the value of `local_id` in the row in [project.tsv](./TableInfo:-project.tsv) corresponding to the _child_ project referenced in this row.