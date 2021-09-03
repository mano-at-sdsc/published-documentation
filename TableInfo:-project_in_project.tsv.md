Each row in this table asserts "the second listed project is a subproject of the first listed project."

Usage notes:
* If you have more than one data (non-header) row in your [project.tsv](./TableInfo:-project.tsv) table, then you must populate `project_in_project.tsv` with all top-level projects for your program, listed as children of the program's root project row. `project_in_project.tsv` will have one row for each parent->child (project->subproject) relationship.

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-expressing-containment-relationships) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**parent_project_id_namespace** | ID of the identifier namespace for the parent in this parent-child project pair | Required | string | 
**parent_project_local_id** | The ID of the containing (parent) project in this parent-child project pair | Required | string |
**child_project_id_namespace** | ID of the identifier namespace for the child in this parent-child project pair | Required | string |
**child_project_local_id** | The ID of the contained (child) project in this parent-child project pair | Required | string |