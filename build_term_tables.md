# Overview

`build_term_tables.py` is a Python script that builds C2M2 controlled-vocabulary term usage tables for anatomy, assay type, file data type, file format, disease and taxonomy metadata.

# Usage

### 0. First build your `file.tsv`, `biosample.tsv`, `biosample_disease.tsv`, `subject_disease.tsv`, and `subject_role_taxonomy.tsv` tables. (Some of these can be left empty (as header-only TSVs) if desired: see the [C2M2 table wiki](https://github.com/nih-cfde/published-documentation/wiki/C2M2-Table-Summary) for requirements.)

### 1. [Download the script [Last updated 9/7/21]](https://osf.io/c67sp/) at OSF 

### 2. [Download the CV reference files [Last updated 9/7/21]](https://osf.io/bq6k9/files/) at OSF (select external_CV_reference_files and then 'Download as zip'.) 

### 3. Unzip the external_CV_reference_files folder

### 4. Put external_CV_reference_files and `build_term_tables.py` into the same folder

### 3. Edit line 42 of the script to match the location of your `file.tsv`, `biosample.tsv`, (etc.) TSV files

### 4. Use the command line to run the script: `python build_term_tables.py`

This script is under active development: please contact us with any questions by emailing the helpdesk at support@cfde.atlassian.net or posting to [Discussions](https://github.com/nih-cfde/published-documentation/discussions)
