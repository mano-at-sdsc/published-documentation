Association between a subject and a substance of interest

If populated, `subject_substance.tsv` will contain one row for every subject linked to a PubChem substance experimentally associated with it. This field is meant to be used for clinical cases such as toxins, drugs, and any other use cases that tie a small number of substances to a subject.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any subjects associated with substances, this table should be left empty.
- If you have exactly one substance of interest for each subject, this table will have the same number of rows as [subject.tsv](./TableInfo:-subject.tsv)
- If you have two substances especially relevant to each subject, this table will have twice as many rows as [subject.tsv](./TableInfo:-subject.tsv)


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for this subject  | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**substance** | A PubChem substance ID (SID) describing this substance | Required | string | This must be a valid PubChem ID <br/> Example: `5381226`