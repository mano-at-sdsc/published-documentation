This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables. 

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An Uberon CV term | Required |  Value must be a valid UBERON ID | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) Example valid UBERON IDs: `UBERON:0001988`, `UBERON:0001052`, `UBERON:0006956`
**name** | A short, human-readable, machine-read-friendly label for this Uberon term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this Uberon term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms (alternate Uberon terms) equivalent to this Uberon term | Non-required: Any number of rows after the header can be filled | Value must be valid UBERON ID(s) separated by `\|` characters | [UBERON lookup service](https://www.ebi.ac.uk/ols/ontologies/uberon) Example valid UBERON IDs: `UBERON:0001988`, `UBERON:0001052`, `UBERON:0006956`