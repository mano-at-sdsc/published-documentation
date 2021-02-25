
This wiki is a companion to the detailed [technical documentation](https://docs.nih-cfde.org/) for participating the Common Fund Data Ecosystem. Use the sidebar to search for key words, error messages and more, or get started with our QuickStart below.

# What is the C2M2?

The Crosscut Metadata Model (C2M2), a flexible metadata standard for describing experimental resources in biomedicine and related fields. At the Common Fund Data Ecosystem (CFDE) we use the C2M2 as our centralized model of participating datasets in a rich relational database hosted at [https://app.nih-cfde.org/](https://app.nih-cfde.org/). This portal supports faceted search of metadata concepts such as anatomical location, species, and assay type, across a wide variety of datasets using a controlled vocabulary. This allows researchers to find a wide variety of data that would otherwise need to be searched individually, using varying nomenclatures. Currently, the portal only accepts C2M2 datapackages from Common Fund Programs. If you represent the Data Coordination Center from a Common Fund Program, and would like to know more about joining the Common Fund Data Ecosystem please contact us by emailing [support@cfde.atlassian.net](support@cfde.atlassian.net). Funding is available for Common Fund Programs who wish to participate, see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information.

# QuickStart: Participating in the CFDE 

## Joining the CFDE

The Data Coordination Center (DCC) for each participating Common Fund Program needs to onboard with the CFDE-CC before we can accept submissions. You do not need to be funded by a CFDE award to participate, however awards are available (see [Engagement Opportunities for Common Fund Programs](https://www.nih-cfde.org/engagement_page/engagement-opportunities-for-common-fund-programs/) for more information). To begin your onboarding, please email [the helpdesk](support@cfde.atlassian.net).

## Creating your datapackage

A datapackage consists of 22 tab separated value (.tsv) files populated with interrelated metadata about the data assets owned by your DCC. Assuming you fill all of the tables, a datapackage submission will make your data searchable by concepts such as anatomical location, species, assay type, and other similar terms that are useful to researchers who are looking for new datasets. This datapackage can be created at several arbitrary levels of complexity, as many of the columns and several entire tables can be left empty and still produce a valid package. However, search-ability in the CFDE portal is highly correlated with model completeness, and as such the Coordination Center recommends making your datapackage as complete as possible. The full specification for all tables is available in the [technical documentation](https://docs.nih-cfde.org/). See the [C2M2-Table-Summary](https://github.com/nih-cfde/published-documentation/wiki/C2M2-Table-Summary) for an abbreviated description of just the tables.


## Installing the tools

To submit your data you will need to install the `cfde-submit` tool. 

## Checking your submission


