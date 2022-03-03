Association between a subject and self-identified race.

If populated, `subject_race.tsv` will contain one row for every assignment of a race to a subject.

Note on context: these values are supplied by study subjects themselves as a vehicle for their self-identification. Obtaining, storing and using this information should not be taken to imply that any concept of race has a well-defined biological analogue: none does. Research involving race metadata has the potential to cause great harm, and should be continuously and carefully scrutinized, especially with respect to its potential to support existing harmful disparities in medical care (or even to create new ones). So why store it at all? Because, carefully used, this information also has the potential to offer systematic improvements to care unobtainable through other means: for example, by exposing systematic differences in treatment decisions or health outcomes that disproportionately affect racialized minorities.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any subjects associated with race, this table should be left empty.
- If you have exactly one race associated with each subject, this table will have as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If you have two races associated with each subject, this table will have twice as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If some but not all of your subjects are associated with one or more races, this table will contain one row for each race assigned to each such subject (and the resulting row count will not have any obvious relationship to the number of rows in [subject.tsv](./TableInfo:-subject.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for this subject  | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**race** | A race self-identified by this subject | Required | string | [Table of allowed values](https://osf.io/jp492/) <br /> Examples: `cfde_subject_race:0`