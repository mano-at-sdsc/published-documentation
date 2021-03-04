Association between a biosample and its source subject


If fully filled, the biosample_from_subject table will contain one row for every `local_id` in [biosample.tsv](./TableInfo:-biosample.tsv), however this is not required.
If a row is filled, it must be filled for all columns, but there is no minimum number of rows that must be filled. You can choose any subset of biosamples.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**biosample_id_namespace** | Identifier namespace for this biosample | Required  if table is populated | If a row has this value, it must have a value for every column <br /><br /> Value type is string | For each row (each biosample), this will be the value of 'id_namespace' in [biosample.tsv](./TableInfo:-biosample.tsv) for this biosample. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows in this column and in the subject_id_namespace column
**biosample_local_id** | The ID of this biosample | Required if table is populated |  If a row has this value, it must have a value for every column<br /><br /> Value type is string |For each row (each biosample), this will be the value of 'local_id' in [biosample.tsv](./TableInfo:-biosample.tsv) for this biosample
**subject_id_namespace** | Identifier namespace for this subject | Required if table is populated | If a row has this value, it must have a value for every column <br /><br />Value type is string | For each row (each biosample), this will be the value of 'id_namespace' in [subject.tsv](./TableInfo:-subject.tsv) for the subject this biosample was taken from. If your program has not implemented multiple id_namespaces, this will be exactly the same for all rows in this column and in the biosample_id_namespace column
**subject_local_id** | The ID of this subject | Required if table is populated | If a row has this value, it must have a value for every column<br /><br /> Value type is string |For each row (each biosample), this will be the value of 'local_id' in the subject table for the subject this biosample was taken from