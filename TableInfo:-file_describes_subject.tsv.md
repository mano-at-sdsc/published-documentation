Association between a file and a subject that it describes

If populated, `file_describes_subject.tsv` will contain one row for every file linked to a subject that it describes.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any files that describe one or more specific subjects, this table should be left empty.
- If you have exactly one file describing or summarizing each subject, this table will have the same number of rows as [subject.tsv](./TableInfo:-subject.tsv).
- If you have five files describing each subject, this table will have five times as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If your subjects are grouped in batches of ten, with each batch described by a single file, then this table will have one tenth as many rows as [subject.tsv](./TableInfo:-subject.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**file_id_namespace** | Identifier namespace for this file | Required | string | This will be the value of `id_namespace` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**file_local_id** | The ID of this file | Required | string | This will be the value of `local_id` in the row in [file.tsv](./TableInfo:-file.tsv) corresponding to the file referenced in this row.
**subject_id_namespace** | Identifier namespace for this subject  | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namnespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
