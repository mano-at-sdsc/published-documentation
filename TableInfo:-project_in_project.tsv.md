Each row in this table asserts "the second listed project is a subproject of the first listed project."

Usage notes:
* If the [project.tsv](./TableInfo:-project.tsv) table contains more than one data row (non-header row), then `project_in_project.tsv` _must_ be populated, at minimum, with one row for each top-level project in your program, where each such top-level project is listed as a child/subproject of the program's root project. In addition to these mandatory rows, `project_in_project.tsv` will optionally also contain one row for every other parent->child (project->subproject) relationship (i.e. parent/child pairs below the top level of the program's project hierarchy).

* Projects need only be explicitly linked to their _immediate parents_ in `project_in_project.tsv`. Transitive containment of each project (by more distant ancestor projects than its immediate parent project) will be automatically inferred.

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#association-tables-expressing-containment-relationships) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**parent_project_id_namespace** | ID of the identifier namespace for the parent in this parent-child project pair | Required | string | 
**parent_project_local_id** | The ID of the containing (parent) project in this parent-child project pair | Required | string |
**child_project_id_namespace** | ID of the identifier namespace for the child in this parent-child project pair | Required | string |
**child_project_local_id** | The ID of the contained (child) project in this parent-child project pair | Required | string |