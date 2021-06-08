# Overview

build_term_tables.py is a simple python script that builds the anatomy, assay_type, data_type, file_format tables. (ncbi_taxonomy tables and JSON schema functionality coming soon). 

# Usage

### 1. [Download the script [Last updated 6/8/21]](https://github.com/nih-cfde/published-documentation/files/6213409/build_term_tables.py.zip)

### 2. Unzip the script (its a single python file)

Download the latest supported tables [Last updated 6/8/2021. Be sure to get the latest script as well]: [EDAM](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/EDAM.version_1.25.tsv), [OBI](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/OBI.version_2021-04-06.obo), [Uberon](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/uberon.version_2021-02-12.obo)

### 4. Add script and tables to a directory

### 5. Edit line 41 of the script to the location of your tables

### 6. Use the command line to run script: `python build_term_tables.py`

This script is still in beta, please contact us with any questions by emailing the helpdesk: support@cfde.atlassian.net or posting in [Discussions](https://github.com/nih-cfde/published-documentation/discussions)
