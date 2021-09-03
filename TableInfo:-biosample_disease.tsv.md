Association between a biosample and a Disease Ontology term

If populated, `biosample_disease.tsv` will contain one row for every assignment of a Disease Ontology term to a biosample.

All fields are required: this table can be empty (header-row only), but any non-header rows must leave no fields blank.

Some examples:   
- If you don't have any biosamples associated with diseases, this table should be left empty.
- If you have exactly one disease associated with each biosample, this table will have as many rows as [biosample.tsv](./TableInfo:-biosample.tsv).
- If you have five diseases associated with each biosample (an especially unhealthy cohort, it would seem), this table will have five times as many rows as [biosample.tsv](./TableInfo:-biosample.tsv).
- If some but not all of your biosamples are associated with one or more diseases, this table will contain one row for each disease assigned to each such biosample (and the resulting row count will not have any obvious relationship to the number of rows in [biosample.tsv](./TableInfo:-biosample.tsv), which is both expected and fine in such a case).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**biosample_id_namespace** | Identifier namespace for this biosample  | Required | string | This will be the value of `id_namespace` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row. If your program has not registered multiple CFDE identifier namnespaces, this will be exactly the same value for all rows.
**biosample_local_id** | The ID of this biosample | Required | string | This will be the value of `local_id` in the row in [biosample.tsv](./TableInfo:-biosample.tsv) corresponding to the biosample referenced in this row.
**disease** | A valid Disease Ontology term | Required | string | [Disease Ontology lookup](https://disease-ontology.org/) <br /> Examples: `DOID:8778`, `DOID:0060249`