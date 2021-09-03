The `primary_dcc_contact.tsv` table must contain **exactly one row** describing a technical contact for this C2M2 datapackage. 

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**contact_email** | Email address of this DCC contact | Required | A valid email address | 
**contact_name** | Name of this DCC contact | Required | string | The name of a person who can answer any questions CFDE staff have during submission processing
**project_id_namespace** | The id_namespace of the project record representing the top-level C2M2 metadataset produced by this contact's DCC [part 1 of 2-component composite foreign key] | Required | string | This will be the value of 'id_namespace' in the [project.tsv](./TableInfo:-project.tsv) table for the overarching project record representing your entire program.
**project_local_id** | The local_id of the project record representing the top-level C2M2 metadataset produced by this contact's DCC [part 2 of 2-component composite foreign key] | Required | string | This will be the value of `local_id` in the [project.tsv](./TableInfo:-project.tsv) table for the overarching project record representing your entire program. If you have only a single project, this is that project. If you have more than one project, create a 'dummy project' to represent your entire program and contain all other projects (as subprojects: see the [project_in_project.tsv](./TableInfo:-project_in_project.tsv) table for how to express these relationships).
**dcc_abbreviation** | A very short display label for this contact's DCC | Required | string | 
**dcc_name** | A short, human-readable, machine-read-friendly label for this contact's DCC | Required | Value can be any string that is not already in use at the CFDE | This is the display name for your program in the portal
**dcc_description** | A human-readable description of this contact's DCC | Required | Value type is string | This is the display description for your program in the portal
**dcc_url** | URL of the front page of the website for this contact's DCC | Required| Value must be a valid URL | Example valid URL: `https://www.hmpdacc.org/`

