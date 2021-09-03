The `subject_role_taxonomy.tsv` table is used to attach taxonomic labels to subjects.

Usage notes:

* https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#taxonomy-and-the-subject-entity-the-subject_role_taxonomy-association-table

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**subject_id_namespace** | Identifier namespace for this subject string | Required if table is populated
**subject_local_id** | The ID of this subject string | Required if table is populated
**role_id** | The ID of the role assigned to this organism-level constituent component of this subject string | Required if table is populatedpopulated
**taxonomy_id** | An NCBI Taxonomy Database ID identifying this taxon string | Required if table is populated