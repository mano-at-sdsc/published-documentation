
This wiki is a companion to the detailed [technical documentation](https://docs.nih-cfde.org/) for participating in the Common Fund Data Ecosystem Portal. Use the sidebar to search for key words, error messages and more, or get started with our QuickStart below.

# What is the C2M2?

The Crosscut Metadata Model (C2M2), a flexible metadata standard for describing experimental resources in biomedicine and related fields. At the Common Fund Data Ecosystem (CFDE) we use the C2M2 as our centralized model of participating datasets in a rich relational database hosted at [https://app.nih-cfde.org/](https://app.nih-cfde.org/). This portal supports faceted search of metadata concepts such as anatomical location, species, and assay type, across a wide variety of datasets using a controlled vocabulary. This allows researchers to find a wide variety of data that would otherwise need to be searched individually, using varying nomenclatures. Currently, the portal only accepts C2M2 datapackages from Common Fund Programs. If you represent the Data Coordination Center from a Common Fund Program, and would like to know more about joining the Common Fund Data Ecosystem please contact us by emailing [support@cfde.atlassian.net](support@cfde.atlassian.net). Funding is available for Common Fund Programs who wish to participate, see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information.

# How does the CFDE Data Submission System work?



DCCs submit data packages to the CFDE Data Submission System using the `cfde-submit` tool. This tool takes a directory as input, does some initial validation, then builds the directory into a [bdbag](https://github.com/fair-research/bdbag) and submits the data to an authenticated [Globus](https://www.globus.org/) endpoint. This process should take less than 30 seconds on your local computer, and the tool will report `Your dataset has been submitted`.

Once your data is in the in the Globus endpoint, our database [(Deriva)](http://isrd.isi.edu/deriva/) will automatically begin ingesting the datapackage, and doing further validation. This process will take several minutes, but is done completely on our servers, so you don't need to stay connected. However, you can check the status of your ingest using `cfde-submit status`. When your Deriva finishes your ingest, you will receive an email that contains information about the datapackage, including a link to view the data in the CFDE data portal. You can also navigate directly to the 

# QuickStart: Participating in the CFDE Portal

## Joining the CFDE

The Data Coordination Center (DCC) for each participating Common Fund Program needs to onboard with the CFDE-CC before we can accept submissions. You do not need to be funded by a CFDE award to participate, however awards are available (see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information). To begin your onboarding, please email [the helpdesk](support@cfde.atlassian.net).

## Onboarding to the CFDE portal

Each person who needs access to submit data on behalf of your DCC, see submitted your DCCs pending data submission, or approve a pending data submission will need to be [onboarded to the Submission System](https://github.com/nih-cfde/published-documentation/wiki/Onboarding-to-the-CFDE-Portal-Submission-System). 

## Creating your datapackage

A datapackage consists of 22 tab separated value (.tsv) files populated with interrelated metadata about the data assets owned by your DCC. Assuming you fill all of the tables, a datapackage submission will make your data searchable by concepts such as anatomical location, species, assay type, and other similar terms that are useful to researchers who are looking for new datasets. This datapackage can be created at several arbitrary levels of complexity, as many of the columns and several entire tables can be left empty and still produce a valid package. However, search-ability in the CFDE portal is highly correlated with model completeness, and as such the Coordination Center recommends making your datapackage as complete as possible. The full specification for all tables is available in the [technical documentation](https://docs.nih-cfde.org/). See the [C2M2-Table-Summary](https://github.com/nih-cfde/published-documentation/wiki/C2M2-Table-Summary) for an abbreviated description of just the tables.


## Installing the tools

### Helper script

### cfde-submit

To submit your data you will need to install the `cfde-submit` tool

To avoid potential conflicts, we recommended installing cfde-submit from within a Python 3 virtual environment ([more info](https://github.com/nih-cfde/cfde-submit/blob/main/docs/install/index.md))

To install the tool:

`pip3 install cfde-submit`

Full documentation is available here: https://github.com/nih-cfde/cfde-submit/blob/main/docs/index.md

Note that only users who have been [onboarded as Data Submitters](https://github.com/nih-cfde/published-documentation/wiki/Onboarding-to-the-CFDE-Portal-Submission-System) for a DCC will be able to successfully run the cfde-submit tool. 

### OPTIONAL: frictionless

Our submission system runs the [frictionless validator](https://pypi.org/project/frictionless/) on our servers as part of the submission process. You do *not* need to install or run frictionless to use our tool, however if you would like to use the validator locally, you can install it using these commands:

`pip install frictionless-py`

`frictionless validate data/datapackage.json`

## Checking and approving your submission

Once a datapackage has been submitted 

