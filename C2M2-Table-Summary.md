- All tables in this summary must be submitted simultaneously (and with the [master C2M2 datapackage JSON Schema file](https://osf.io/vzgx9/)) to create a valid datapackage
- Empty (unused) tables should be submitted with only the header row filled in
- Table (TSV) filenames must exactly match those listed below (and in the JSON Schema file)
- Table column headers must exactly match those listed below (and in the JSON Schema file)
- Table columns must appear in the order listed here (and in the JSON Schema file)
- Table (TSV) files must not contain any empty rows or extra lines
- Every TSV file should end with the final row of table data, terminated by a newline

Table (click for detailed information)|Requirement for Submission|Table Features
-----------| -----------| -------------
[anatomy.tsv](./TableInfo:-anatomy.tsv)|Automatically created by submission software|
[assay_type.tsv](./TableInfo:-assay_type.tsv)|Automatically created by submission software|
[biosample.tsv](./TableInfo:-biosample.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have biosamples
[biosample_from_subject.tsv](./TableInfo:-biosample_from_subject.tsv)|Table must be submitted with all headers. Fields are all optional.|
[biosample_in_collection.tsv](./TableInfo:-biosample_in_collection.tsv)|Table must be submitted with all headers. Fields are all optional.|The biosample_in_collection table will contain one row per biosample-collection pair in your project
[collection.tsv](./TableInfo:-collection.tsv)|Table must be submitted with all headers. Fields are all optional.|This table will have as many rows as you have Collections
[collection_defined_by_project.tsv](./TableInfo:-collection_defined_by_project.tsv)|Table must be submitted with all headers. Fields are all optional.|
[collection_in_collection.tsv](./TableInfo:-collection_in_collection.tsv)|Table must be submitted with all headers. Fields are all optional.|
[data_type.tsv](./TableInfo:-data_type.tsv)|Automatically created by submission software|
[file](./TableInfo:-file.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have files
[file_describes_biosample.tsv](./TableInfo:-file_describes_biosample.tsv)|Table must be submitted with all headers. Fields are all optional.|
[file_describes_subject.tsv](./TableInfo:-file_describes_subject.tsv)|Table must be submitted with all headers. Fields are all optional.|
[file_format.tsv](./TableInfo:-file_format.tsv)|Automatically created by submission software|
[file_in_collection.tsv](./TableInfo:-file_in_collection.tsv)|Table must be submitted with all headers. Fields are all optional.|
[id_namespace.tsv](./TableInfo:-id_namespace.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have namespaces
[ncbi_taxonomy.tsv](./TableInfo:-ncbi_taxonomy.tsv)|Automatically created by submission software|
[primary_dcc_contact.tsv](./TableInfo:-primary_dcc_contact.tsv)|Table must be submitted with all headers and with required fields populated|This table will have exactly one row 
[project.tsv](./TableInfo:-project.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have Projects
[project_in_project.tsv](./TableInfo:-project_in_project.tsv)|Table must be submitted with all headers. Fields are all optional.|If you have more than one project in the project table, then you must populate this table.
[subject.tsv](./TableInfo:-subject.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have subjects
[subject_in_collection.tsv](./TableInfo:-subject_in_collection.tsv)|Table must be submitted with all headers. Fields are all optional.|
[subject_role_taxonomy.tsv](./TableInfo:-subject_role_taxonomy.tsv)|Table must be submitted with all headers. Fields are all optional.|This table will have as many rows as you have subjects
