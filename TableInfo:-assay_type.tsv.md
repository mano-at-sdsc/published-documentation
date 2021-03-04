This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

The assay_type.tsv table should have as many rows as you have unique OBI IDs in the `assay_type` column of [file.tsv](./TableInfo:-file.tsv)

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An OBI CV term | Required | Value must be a valid OBI ID | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) <br />Example valid OBI IDs: <br />`OBI:0000366`<br /> `OBI:0001177`<br /> `OBI:0002763` 
**name** | A short, human-readable, machine-read-friendly label for this OBI term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this OBI term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms (alternate OBI terms) equivalent to this OBI term | Non-required: Any number of rows after the header can be filled | Value must be valid OBI ID(s) separated by `\|` characters | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070)<br /> Example valid OBI IDs:<br /> `OBI:0000366`<br /> `OBI:0001177`<br />`OBI:0002763` 