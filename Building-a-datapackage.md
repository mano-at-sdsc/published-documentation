There are many valid ways to build a datapackage depending on the underlying structure of your DCC's data. Although you must submit all tables to have a valid package, most tables, and most columns within most tables, can be left blank. This allows you to use only the pieces of the C2M2 that best fit your data. This page does not discuss modeling per se, and is instead designed to give a quick overview of how to finalize your datapackage. If you need help turning your internal data model into something compatible with the C2M2 please contact [the helpdesk](support@cfde.atlassian.net) directly for individualized support.


1. Build the tables that your DCC has data for according to the [technical documentation](https://docs.nih-cfde.org/). Supplemental table information is also available [in this wiki](./C2M2-Table-Summary).
2. Download the [C2M2 JSON file from CFDE OSF space](https://osf.io/c63aw/) and save in the same directory as your tables.
3. Follow [submission prep script instructions](https://github.com/nih-cfde/published-documentation/wiki/submission-prep-script) to generate controlled vocabulary tables from your data.
4. If you do not have 48 table files, [download blank headers for the missing tables here](https://osf.io/3tzqu/) and save them to the same directory.
5. OPTIONAL: run the [frictionless validator script](./Quickstart#optional-frictionless).
6. Submit your datapackage using [the cfde-submit tool](./Quickstart#cfde-submit). **NOTE: [This will only work if you have been onboarded as a data submitter](./Onboarding-to-the-CFDE-Portal-Submission-System).**