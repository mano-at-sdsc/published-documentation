This table does *not* need to be manually created (but it can be). Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

The file_format.tsv table should have as many rows as you have unique EDAM IDs in the `file_format` column of [file.tsv](./TableInfo:-file.tsv)


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An EDAM CV term | Required | Value type is string 
**name** | A short, human-readable, machine-read-friendly label for this EDAM term| Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this EDAM term |  Non-required: Any number of rows after the header can be filled | Value type is string
