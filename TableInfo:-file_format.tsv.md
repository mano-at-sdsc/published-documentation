This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An EDAM CV term | Required | Value type is string 
**name** | A short, human-readable, machine-read-friendly label for this EDAM term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this EDAM term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms (alternate EDAM terms) equivalent to this Uberon term | Non-required: Any number of rows after the header can be filled |  Value must be a valid EDAM ID |  Example valid EDAM IDs: `format:1930`, `format:3712`, `format:2310` [EDAM format lookup](https://www.ebi.ac.uk/ols/ontologies/edam/terms?iri=http%3A%2F%2Fedamontology.org%2Fformat_1915&viewMode=All&siblings=false)