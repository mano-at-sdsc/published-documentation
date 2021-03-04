This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

The data_type.tsv table should have as many rows as you have unique EDAM IDs in the `data_type` column of [file.tsv](./TableInfo:-file.tsv)


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An EDAM CV term | Required | Value must be a valid EDAM ID | [EDAM data type lookup](https://www.ebi.ac.uk/ols/ontologies/edam/terms?iri=http%3A%2F%2Fedamontology.org%2Fdata_0006&viewMode=All&siblings=false) <br /> Example valid EDAM IDs: `data:2044`, `data:2050`, `data:2082` 
**name** | A short, human-readable, machine-read-friendly label for this EDAM term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this EDAM term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms (alternate EDAM terms) equivalent to this EDAM term | Non-required: Any number of rows after the header can be filled |  Value must be valid EDAM ID(s) separated by `\|` characters | [EDAM data type lookup](https://www.ebi.ac.uk/ols/ontologies/edam/terms?iri=http%3A%2F%2Fedamontology.org%2Fdata_0006&viewMode=All&siblings=false) <br />Example valid EDAM IDs: `data:2044`, `data:2050`, `data:2082` 