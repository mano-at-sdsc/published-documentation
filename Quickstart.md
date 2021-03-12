# QuickStart: Participating in the CFDE Portal

## Joining the CFDE

The Data Coordination Center (DCC) for each participating Common Fund Program needs to onboard with the CFDE-CC before we can accept submissions. You do not need to be funded by a CFDE award to participate, however awards are available (see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information). To begin your onboarding, please email the helpdesk: support@cfde.atlassian.net.

## Onboarding to the CFDE portal

Each person who needs access to submit data on behalf of your DCC, see submitted your DCCs pending data submission, or approve a pending data submission will need to be [onboarded to the Submission System](./Onboarding-to-the-CFDE-Portal-Submission-System). 

## Creating your datapackage

A datapackage consists of 22 tab separated value (.tsv) files populated with interrelated metadata about the data assets owned by your DCC. Assuming you fill all of the tables, a datapackage submission will make your data searchable by concepts such as anatomical location, species, assay type, and other similar terms that are useful to researchers who are looking for new datasets. This datapackage can be created at several arbitrary levels of complexity, as many of the columns and several entire tables can be left empty and still produce a valid package. However, search-ability in the CFDE portal is highly correlated with model completeness, and as such the Coordination Center recommends making your datapackage as complete as possible. The full specification for all tables is available in the [technical documentation](https://docs.nih-cfde.org/). See the [C2M2-Table-Summary](./C2M2-Table-Summary) for an high level description the tables.


## Installing the tools

### OPTIONAL: Helper script

Five of the tables required by the C2M2 can be automatically generated from the other tables. Once you have created the other tables, run our [helper script](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/build_term_tables.py) to create the anatomy, assay_type, data_type, file_format tables. (ncbi_taxonomy tables and JSON schema functionality coming soon):

`python build_term_tables.py`

See the full [build_term_tables](./build_term_tables) documentation for more information.

### cfde-submit

To submit your data you will need to install the `cfde-submit` tool

To avoid potential conflicts, we recommended installing cfde-submit from within a Python 3 virtual environment ([more info](https://docs.nih-cfde.org/en/latest/cfde-submit/docs/install/))

To install the tool:

`pip3 install cfde-submit`

To use the tool, give it the path to the directory containing all 22 tables plus the required JSON schema file:

`cfde-submit run PATH/TO/DIRECTORY`

See the full [cfde-submit](https://docs.nih-cfde.org/en/latest/cfde-submit/docs/) documentation for more information.

Note that only users who have been [onboarded as Data Submitters](./Onboarding-to-the-CFDE-Portal-Submission-System) for a DCC will be able to successfully run the cfde-submit tool. 

### OPTIONAL: frictionless

Our submission system runs the [frictionless validator](https://pypi.org/project/frictionless/) on our servers as part of the submission process. You do *not* need to install or run frictionless to use our tool, however if you would like to use the validator locally, you can install it using these commands:

`pip install frictionless-py`

`frictionless validate data/datapackage.json`

## Checking your submission

Once a datapackage has been submitted you can view it in the portal to see how it will appear for portal users. See [How to review your datapackage](./How-to-review-a-datapackage) for more details.

## Approving your submission

One person at your DCC will have the role of Data Approver. This person verifies that a datapackage is acceptable to the DCC and approves it for inclusion in the next data release. Although DCCs can have any number of Reviewable Submissions, each can have only a single Approved Submission for public release. See [How to approve your datapackage](./How-to-approve-your-datapackage)

## Troubleshooting

If your datapackage submits, it has passed very basic error checking, but a much more extensive check happens when it is ingested into the database. If your datapackage has a problem, the error message will be included both in the email telling you submission is completed, and in the data submission system in the portal. In the portal, your error message will appear as 'Diagnostics'. For more help with your specific error message please search the left sidebar for common errors, ask questions in [Discussions](https://github.com/nih-cfde/published-documentation/discussions) or email the helpdesk: support@cfde.atlassian.net for assistance.

