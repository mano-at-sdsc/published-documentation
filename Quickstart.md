# QuickStart: Participating in the CFDE Portal

## Joining the CFDE

The Data Coordination Center (DCC) for each participating Common Fund Program needs to onboard with the CFDE-CC before we can accept submissions. You do not need to be funded by a CFDE award to participate, but awards are available (see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information). To begin your onboarding, please email the helpdesk: support@cfde.atlassian.net.

## Onboarding to the CFDE portal

Anyone who will need permissions to submit, review and/or approve data on behalf of your DCC will need to be [onboarded to the Submission System](./Onboarding-to-the-CFDE-Portal-Submission-System). 

## Creating your C2M2 datapackage

A C2M2 datapackage consists of a group of tab-separated value (.tsv) files populated with interrelated metadata about the data assets owned by your DCC. Submitting a datapackage to the CFDE portal system can make your data searchable by concepts like anatomical location, species, assay type, disease, phenotype, chemical substance and other terms relevant to biomedical researchers looking for new datasets. This datapackage can be created with arbitrary levels of complexity: many of the columns and several entire tables can be left empty and still produce a valid package; selection depends on what each DCC wants to express about their own sets of research data. Findability of research data in the CFDE portal will correlate with datapackage completeness, so once a DCC has identified a relevant selection of model components, it is best to make datapackages as rich as possible within those selected components. The full specification for all tables is available in the [technical documentation](https://docs.nih-cfde.org/). See the [C2M2-Table-Summary](./C2M2-Table-Summary) for a high-level description.

<img src="https://github.com/nih-cfde/published-documentation/blob/stable/docs/images/datapackageflow.png" width="700">

## Installing the tools

### C2M2 Submission prep script

The controlled vocabulary (CV) term tables required for C2M2 submissions will be automatically generated from term usage collected from the other tables. Once you have created all other (non-CV) tables, run our submission prep script ([wiki page](./submission-prep-script); [code](https://osf.io/bq6k9/)) to automatically build the anatomy.tsv, analysis_type.tsv, assay_type.tsv, data_type.tsv, file_format.tsv, ncbi_taxonomy.tsv, compound.tsv, substance.tsv, phenotype.tsv, gene.tsv and disease.tsv tables to be included with your submission:

`python prepare_c2m2_submission.py`

See the [wiki page](./submission-prep-script) for usage information.

### cfde-submit

To submit your data you will need to install the `cfde-submit` tool

To avoid potential conflicts, we recommended installing cfde-submit from within a Python 3 virtual environment ([more info](https://docs.nih-cfde.org/en/latest/cfde-submit/docs/install/))

To install the tool:

`pip3 install cfde-submit`

To use the tool, give it the path to the directory containing all 22 tables plus the [required JSON schema file](https://osf.io/e5tc2/):

`cfde-submit run PATH/TO/DIRECTORY`

See the full [cfde-submit](https://docs.nih-cfde.org/en/latest/cfde-submit/docs/) documentation for more information.

Note that only users who have been [onboarded as Data Submitters](./Onboarding-to-the-CFDE-Portal-Submission-System) for a DCC will be able to successfully run the cfde-submit tool. 

### OPTIONAL: frictionless

Our submission system runs the [frictionless validator](https://pypi.org/project/frictionless/) on our servers as part of the submission process. You do *not* need to install or run frictionless to use our tool, however if you would like to use the validator locally, you can install it using these commands:

`pip install frictionless`

if that command fails try:

`pip install frictionless-py`

Once it's installed, run it by doing:

`frictionless validate PATH/TO/JSON_FILE_IN_DIRECTORY`

This command takes several minutes to run, and dumps the results into your terminal by default. To make a nicer file to review do:

`frictionless validate PATH/TO/JSON_FILE_IN_DIRECTORY > report.txt`

## Checking your submission

Once a datapackage has been submitted you can view it in the portal to see how it will appear for portal users. See [How to review your datapackage](./How-to-review-a-datapackage) for more details.

## Approving your submission

One person at your DCC will have the role of Data Approver. This person verifies that a datapackage is acceptable to the DCC and approves it for inclusion in the next data release. Although DCCs can have any number of Reviewable Submissions, each can have only a single Approved Submission in each public release. See [How to approve your datapackage](./How-to-approve-your-datapackage). **A datapackage must be approved by a DCC approver before it becomes part of the public CFDE portal**

## Troubleshooting

If your datapackage submits, it has passed very basic error checking, but a much more extensive check happens when it is ingested into the database. If your datapackage has a problem, the error message will be included both in the email telling you submission is completed, and in the data submission system in the portal. In the portal, your error message will appear as 'Diagnostics'. For more help with your specific error message please search the left sidebar for common errors, ask questions in [Discussions](https://github.com/nih-cfde/published-documentation/discussions) or email the helpdesk: support@cfde.atlassian.net for assistance.

