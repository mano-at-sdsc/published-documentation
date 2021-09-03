The `subject_role_taxonomy.tsv` table is used to attach taxonomic labels to subjects.

Usage notes:

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#taxonomy-and-the-subject-entity-the-subject_role_taxonomy-association-table) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for this subject | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**role_id** | The ID of the role assigned to this organism-level constituent component of this subject | Required | enum of strings |
**taxonomy_id** | An NCBI Taxonomy Database ID identifying this taxon string | Required | string | 