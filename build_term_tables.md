# Overview

build_term_tables.py is a simple python script that builds the anatomy, assay_type, data_type, file_format tables. (ncbi_taxonomy tables and JSON schema functionality coming soon). 

# Usage

### 1. Downloads

[Download the script](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/build_term_tables.py)

Download the latest supported tables: [EDAM](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/EDAM.version_1.21.tsv), [OBI](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/OBI.version_2020-12-16.obo), [Uberon](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_external_CV_term_table_generator_script/external_CV_reference_files/uberon.version_2019-06-27.obo)

### 2. Add script and tables to a directory

### 3. Edit line 41 of the script to the location of your tables

### 4. Use the command line to run script: `python build_term_tables.py`

This script is still in beta, please contact us with any questions by emailing the helpdesk: support@cfde.atlassian.net or posting in [Discussions](https://github.com/nih-cfde/published-documentation/discussions)
