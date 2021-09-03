- All table files listed in this summary must be bundled together, along with the [C2M2 datapackage JSON Schema file](https://osf.io/vzgx9/), to create a valid C2M2 datapackage for submission to CFDE
- TSV files for any empty (unused) tables should still be submitted, with only the (tab-separated) column-header row filled in
- Table (TSV) filenames must exactly match those listed in the JSON Schema file (and in these docs)
- Table column headers must exactly match those listed in the JSON Schema file (and in these docs)
- Table columns must appear in the order given in the JSON Schema file (and in these docs)
- All tables marked "CV term table" in the list below must be built using the [CFDE term-table builder script](https://osf.io/bq6k9/)
- Table (TSV) files must not contain any empty rows or extra lines
- Every TSV file should end with the final row of table data, terminated by a newline

Table (click for detailed information)|Construction|Notes
-----------| -----------| -------------
[anatomy.tsv](./TableInfo:-anatomy.tsv)|Automatically created by script|CV term table
[assay_type.tsv](./TableInfo:-assay_type.tsv)|Automatically created by script|CV term table
[biosample.tsv](./TableInfo:-biosample.tsv)|Prepared by submitter|This table will have as many rows as you have biosamples
[biosample_disease.tsv](./TableInfo:-biosample_disease.tsv)|Prepared by submitter|This table will have one row for each disease associated with each biosample
[biosample_from_subject.tsv](./TableInfo:-biosample_from_subject.tsv)|Prepared by submitter|
[biosample_in_collection.tsv](./TableInfo:-biosample_in_collection.tsv)|Prepared by submitter|This table will have one row for each biosample-collection pair in your project
[collection.tsv](./TableInfo:-collection.tsv)|Prepared by submitter|This table will have as many rows as you have collections
[collection_defined_by_project.tsv](./TableInfo:-collection_defined_by_project.tsv)|Prepared by submitter|
[collection_in_collection.tsv](./TableInfo:-collection_in_collection.tsv)|Prepared by submitter|
[data_type.tsv](./TableInfo:-data_type.tsv)|Automatically created by script|CV term table
[disease.tsv](./TableInfo:-disease.tsv)|Automatically created by script|CV term table
[file](./TableInfo:-file.tsv)|Prepared by submitter|This table will have as many rows as you have files
[file_describes_biosample.tsv](./TableInfo:-file_describes_biosample.tsv)|Prepared by submitter|
[file_describes_subject.tsv](./TableInfo:-file_describes_subject.tsv)|Prepared by submitter|
[file_format.tsv](./TableInfo:-file_format.tsv)|Automatically created by script|CV term table
[file_in_collection.tsv](./TableInfo:-file_in_collection.tsv)|Prepared by submitter|
[id_namespace.tsv](./TableInfo:-id_namespace.tsv)|Prepared by submitter|This table will have as many rows as you have identifier namespaces
[ncbi_taxonomy.tsv](./TableInfo:-ncbi_taxonomy.tsv)|Automatically created by script|CV term table
[primary_dcc_contact.tsv](./TableInfo:-primary_dcc_contact.tsv)|Prepared by submitter|This table will have exactly one row 
[project.tsv](./TableInfo:-project.tsv)|Prepared by submitter|This table will have as many rows as you have projects
[project_in_project.tsv](./TableInfo:-project_in_project.tsv)|Prepared by submitter|If you have more than one project in the project table, then you must populate this table
[subject.tsv](./TableInfo:-subject.tsv)|Prepared by submitter|This table will have as many rows as you have subjects
[subject_disease.tsv](./TableInfo:-subject_disease.tsv)|Prepared by submitter|This table will have one row for each disease associated with each subject
[subject_in_collection.tsv](./TableInfo:-subject_in_collection.tsv)|Prepared by submitter|
[subject_role_taxonomy.tsv](./TableInfo:-subject_role_taxonomy.tsv)|Prepared by submitter|This table will have as many rows as you have subjects
