This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The assay_type.tsv table will have as many rows as the number of unique OBI terms appearing in the `assay_type` column of [file.tsv](./TableInfo:-file.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | An OBI CV term | Required | Value must be a valid OBI ID | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) <br />Example valid OBI IDs: <br />`OBI:0000366`<br /> `OBI:0001177`<br /> `OBI:0002763` 
**name** | A short, human-readable, machine-read-friendly label for this OBI term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this OBI term |  Non-required: Any number of rows after the header can be filled | Value type is string
