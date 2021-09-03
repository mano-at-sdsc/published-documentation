- All table files listed in this summary must be bundled together, along with the [C2M2 datapackage JSON Schema file](https://osf.io/vzgx9/), to create a valid C2M2 datapackage for submission to CFDE
- TSV files for any empty (unused) tables should still be submitted, with only the (tab-separated) column-header row filled in
- Table (TSV) filenames must exactly match those listed in the JSON Schema file (and in these docs)
- Table column headers must exactly match those listed in the JSON Schema file (and in these docs)
- Table columns must appear in the order given in the JSON Schema file (and in these docs)
- All tables marked "CV term table" in the list below must be built using the [CFDE term-table builder script](https://osf.io/bq6k9/)
- Table (TSV) files must not contain any empty rows or extra lines
- Every TSV file should end with the final row of table data, terminated by a newline

Table (click for detailed information)|Construction|Can be empty?|Notes
-----------|:-----------:|:-------------:|-------------
[anatomy.tsv](./TableInfo:-anatomy.tsv)|Built by script|Y|CV term table
[assay_type.tsv](./TableInfo:-assay_type.tsv)|Built by script|Y|CV term table
[biosample.tsv](./TableInfo:-biosample.tsv)|Prepared&nbsp;by&nbsp;submitter|Y|This table will have one row for each biosample
[biosample_disease.tsv](./TableInfo:-biosample_disease.tsv)|Prepared by submitter|Y|This table will have one row for each disease associated with each biosample
[biosample_from_subject.tsv](./TableInfo:-biosample_from_subject.tsv)|Prepared by submitter|Y|This table will have one row for each attribution of a biosample to a subject
[biosample_in_collection.tsv](./TableInfo:-biosample_in_collection.tsv)|Prepared by submitter|Y|This table will have one row for each assignment of a biosample to a collection
[collection.tsv](./TableInfo:-collection.tsv)|Prepared by submitter|Y|This table will have one row for each collection
[collection_defined_by_project.tsv](./TableInfo:-collection_defined_by_project.tsv)|Prepared by submitter|Y|This table will have one row for each collection that was generated directly by a project listed in the [project.tsv](./TableInfo:-project.tsv) table
[collection_in_collection.tsv](./TableInfo:-collection_in_collection.tsv)|Prepared by submitter|Y|This table will have one row for each parent->child (collection->subcollection) relationship
[data_type.tsv](./TableInfo:-data_type.tsv)|Built by script|Y|CV term table
[disease.tsv](./TableInfo:-disease.tsv)|Built by script|Y|CV term table
[file](./TableInfo:-file.tsv)|Prepared by submitter|Y|This table will have one row for each file
[file_describes_biosample.tsv](./TableInfo:-file_describes_biosample.tsv)|Prepared by submitter|Y|This table will have one row for each association of a biosample with a describing file
[file_describes_subject.tsv](./TableInfo:-file_describes_subject.tsv)|Prepared by submitter|Y|This table will have one row for each association of a subject with a describing file
[file_format.tsv](./TableInfo:-file_format.tsv)|Built by script|Y|CV term table
[file_in_collection.tsv](./TableInfo:-file_in_collection.tsv)|Prepared by submitter|Y|This table will have one row for each assignment of a file to a collection
[id_namespace.tsv](./TableInfo:-id_namespace.tsv)|Prepared by submitter|N|This table will have one row for each C2M2 identifier namespace registered with CFDE
[ncbi_taxonomy.tsv](./TableInfo:-ncbi_taxonomy.tsv)|Built by script|Y|CV term table
[primary_dcc_contact.tsv](./TableInfo:-primary_dcc_contact.tsv)|Prepared by submitter|N|This table will have exactly one row
[project.tsv](./TableInfo:-project.tsv)|Prepared by submitter|N|This table will have one row for each project
[project_in_project.tsv](./TableInfo:-project_in_project.tsv)|Prepared by submitter|Y<sup>*</sup>|<sup>*</sup>If you have more than one project in your [project.tsv](./TableInfo:-project.tsv) table, then you must populate this table with all top-level projects listed as children of the DCC root project. This table will have one row for each parent->child (project->subproject) relationship
[subject.tsv](./TableInfo:-subject.tsv)|Prepared by submitter|Y|This table will have one row for each subject
[subject_disease.tsv](./TableInfo:-subject_disease.tsv)|Prepared by submitter|Y|This table will have one row for each disease associated with each subject
[subject_in_collection.tsv](./TableInfo:-subject_in_collection.tsv)|Prepared by submitter|Y|This table will have one row for each assigmment of a subject to a collection
[subject_role_taxonomy.tsv](./TableInfo:-subject_role_taxonomy.tsv)|Prepared by submitter|Y|This table will have one row for each taxon assigned to a subject