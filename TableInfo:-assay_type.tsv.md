This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An OBI CV term | Required | Value must be a valid OBI ID | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) Example valid OBI IDs: `OBI:0000366`, `OBI:0001177`, `OBI:0002763` 
**name** | A short, human-readable, machine-read-friendly label for this OBI term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this OBI term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms (alternate OBI terms) equivalent to this OBI term | Non-required: Any number of rows after the header can be filled | Value must be valid OBI ID(s) separated by `\|` characters | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) Example valid OBI IDs: `OBI:0000366`, `OBI:0001177`, `OBI:0002763` 