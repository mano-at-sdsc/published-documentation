THIS PAGE IS MID-EDIT

Association between a subject and a Disease Ontology term

If populated, `subject_disease.tsv` will contain one row for every assignment of a Disease Ontology term to a subject.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any subjects associated with diseases, this table should be left empty.
- If you have exactly one disease associated with each subject, this table will have as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If you have five diseases associated with each subject (an especially unhealthy cohort, it would seem), this table will have five times as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If some but not all of your subjects are associated with one or more diseases, this table will contain one row for each disease assigned to each such subject (and the resulting row count will not have any obvious relationship to the number of rows in [subject.tsv](./TableInfo:-subject.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for this subject  | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`