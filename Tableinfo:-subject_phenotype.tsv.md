Association between a subject and a Human Phenotype Ontology term

For subjects with phenotype metadata, this table will have one row for each phenotype associated with each such subject, along with an `association_type` field distinguishing "phenotype present" from "phenotype specifically ruled out."

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any subjects associated with phenotypes, this table should be left empty.
- If you have exactly one phenotype associated with each subject, this table will have as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If you have five phenotypes associated with each subject, this table will have five times as many rows as [subject.tsv](./TableInfo:-subject.tsv).
- If some but not all of your subjects are associated with one or more phenotypes, this table will contain one row for each phenotype assigned to each such subject (and the resulting row count will not have any obvious relationship to the number of rows in [subject.tsv](./TableInfo:-subject.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**subject_id_namespace** | Identifier namespace for this subject  | Required | string | This will be the value of `id_namespace` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row. If your program has not registered multiple CFDE identifier namespaces, this will be exactly the same value for all rows.
**subject_local_id** | The ID of this subject | Required | string | This will be the value of `local_id` in the row in [subject.tsv](./TableInfo:-subject.tsv) corresponding to the subject referenced in this row.
**association_type** | An indicator distinguishing "phenotype present" from "phenotype ruled out" | Required | one of `cfde_phenotype_association_type:0`<br>(meaning "phenotype ruled out")<br>or<br>`cfde_phenotype_association_type:1`<br>(meaning "phenotype observed") | 
**phenotype** | A valid Human Phenotype Ontology term | Required | string | [Human Phenotype Ontology lookup](https://hpo.jax.org/app/) <br /> Examples: `HP:0000349`, `HP:0012425`