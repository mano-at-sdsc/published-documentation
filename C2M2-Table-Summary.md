- All tables must be submitted simultaneously (and with the provided JSON specification) to create a valid datapackage
- Unused tables should be submitted with only the header row populated
- Table names must exactly match the list below (and JSON specification)
- Table headers must exactly match the headers listed in that table (and JSON specification)
- Table columns must appear in the order listed in that table (and JSON specification)
- Tables must not contain empty rows between populated rows (trailing empty rows are fine)

Table (click for detailed information)|Requirement for Submission|Table Features
-----------| -----------| -------------
anatomy|Automatically created by submission software|
assay_type|Automatically created by submission software|
biosample|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have biosamples
biosample_from_subject|Table must be submitted with all headers. Fields are all optional.|
biosample_in_collection|Table must be submitted with all headers. Fields are all optional.|The biosample_in_collection table will contain one row per biosample-collection pair in your project
collection|Table must be submitted with all headers. Fields are all optional.|This table will have as many rows as you have Collections
collection_defined_by_project|Table must be submitted with all headers. Fields are all optional.|
collection_in_collection|Table must be submitted with all headers. Fields are all optional.|
data_type|Automatically created by submission software|
[file](./TableInfo:-file.tsv)|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have files
file_describes_biosample|Table must be submitted with all headers. Fields are all optional.|
file_describes_subject|Table must be submitted with all headers. Fields are all optional.|
file_format|Automatically created by submission software|
file_in_collection|Table must be submitted with all headers. Fields are all optional.|
ncbi_taxonomy|Automatically created by submission software|
primary_dcc_contact|Table must be submitted with all headers and with required fields populated|This table will have exactly one row 
project|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have Projects
project_in_project|Table must be submitted with all headers. Fields are all optional.|If you have more than one project in the project table, then you must populate this table.
subject|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have subjects
subject_in_collection|Table must be submitted with all headers. Fields are all optional.|
subject_role_taxonomy|Table must be submitted with all headers. Fields are all optional.|This table will have as many rows as you have subjects
id_namespace|Table must be submitted with all headers and with required fields populated|This table will have as many rows as you have namespaces