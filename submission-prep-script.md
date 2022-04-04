## Overview

`python prepare_C2M2_submission.py` (previously `build_term_tables.py`) is a Python script that automatically builds controlled-vocabulary (CV) term usage tables for C2M2 datapackage preparation, as well as performing some pre-submission data integrity checks.

The following files are built automatically by this script and should not be hand-created or edited; submit them along with the other required TSVs as part of your datapackage.

* `analysis_type.tsv`
* `anatomy.tsv`
* `assay_type.tsv`
* `compound.tsv`
* `data_type.tsv`
* `disease.tsv`
* `file_format.tsv`
* `gene.tsv`
* `ncbi_taxonomy.tsv`
* `phenotype.tsv`
* `phenotype_disease.tsv`
* `phenotype_gene.tsv`
* `substance.tsv`

The following pre-submission validation checks are currently performed:

* Ensure that for any file with a non-null persistent ID, a checksum is also provided.
* Ensure that all (non-null) persistent IDs are unique (both within and across tables).

## Usage

### 0. First build your `file.tsv`, `biosample.tsv`, `biosample_disease.tsv`, `biosample_gene.tsv`, `biosample_substance.tsv`, `subject_disease.tsv`, `subject_phenotype.tsv`, `subject_role_taxonomy.tsv`, `subject_substance.tsv`, and `collection_disease.tsv` tables. (Some of these can be left empty (as header-only TSVs) if desired: see the [C2M2 table wiki](https://github.com/nih-cfde/published-documentation/wiki/C2M2-Table-Summary) for requirements.)

### 1. [Download the script [Last updated 2 Feb 2022]](https://osf.io/c67sp/) at OSF 

### 2. [Download the CV reference files [Last updated 2 Feb 2022]](https://osf.io/bq6k9/files/) at OSF (select external_CV_reference_files and then 'Download as zip'.) 

### 3. Unzip the external_CV_reference_files folder

### 4. Put external_CV_reference_files and `prepare_C2M2_submission.py` into the same folder

### 5. Create a subdirectory containing your pre-built `file.tsv`, `biosample.tsv`, etc., then edit line 42 of `prepare_C2M2_submission.py` to match.

### 6. Use the command line to run the script: `python prepare_C2M2_submission.py`

This script is under active development: please contact us with any questions by emailing the helpdesk at support@cfde.atlassian.net or posting to [Discussions](https://github.com/nih-cfde/published-documentation/discussions)
