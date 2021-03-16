There are many valid ways to build a datapackage depending on the underlying structure of your DCCs data. [See several examples here.](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#c2m2-examples) This page does not discuss modeling per se, and is instead designed to give a quick overview of how to finalize your datapackage. If you need help turning your internal data model into something compatible with the C2M2 please contact [the helpdesk](support@cfde.atlassian.net) directly for individualized support.


1. Build the tables that your DCC has data for according to the [technical documentation](https://docs.nih-cfde.org/). Supplemental table information is also available [in this wiki](./C2M2-Table-Summary)
2. Download the [C2M2 JSON file from CFDE OSF space](https://osf.io/e5tc2/) and save in the same directory as your tables
3. Follow [helper script instructions](https://github.com/nih-cfde/published-documentation/wiki/build_term_tables) to generate controlled vocabulary tables: anatomy, assay_type, data_type, file_format tables
4. If you do not have 22 tables, [download blank headers for the missing tables here](https://osf.io/rdeks/files/) and save them to the same directory
5. If your `subject_role_taxonomy.tsv` is not empty, fill the taxonomy table. One row per unique `taxonomy_id` (This table will be built automatically in the next release of the helper script.
6. OPTIONAL: run the [frictionless validator script](./Quickstart#optional-frictionless)
7. Submit your datapackage using [the cfde-submit tool](./Quickstart#cfde-submit) **NOTE: [This will only work if you have been onboarded as a data submitter](./Onboarding-to-the-CFDE-Portal-Submission-System)**