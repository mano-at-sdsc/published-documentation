The `subject_role_taxonomy.tsv` table is used to attach taxonomic labels to subjects.

Usage notes:

* Please see the [technical docs](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#taxonomy-and-the-subject-entity-the-subject_role_taxonomy-association-table) for a complete discussion of the rules governing the use of this table.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for the subject | Required if table is populated
**subject_local_id** | The ID of this subject string | Required if table is populated
**role_id** | The ID of the role assigned to this organism-level constituent component of this subject string | Required if table is populatedpopulated
**taxonomy_id** | An NCBI Taxonomy Database ID identifying this taxon string | Required if table is populated