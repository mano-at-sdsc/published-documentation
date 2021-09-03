This table *must not* be manually created. Users should skip this (and all other controlled vocabulary term tables) when preparing the rest of their datapackage's TSV files for submission. Once the other tables are built, users should then use the [CFDE term-table builder script](https://osf.io/bq6k9/) to automatically build this table (and the other term tables) from the information stored in the other already-completed table files.

The assay_type.tsv table will have as many rows as the number of unique OBI terms appearing either in the `assay_type` column of [file.tsv](./TableInfo:-file.tsv) or in the `assay_type` column of [biosample.tsv](./TableInfo:-biosample.tsv).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | An valid OBI term | Required | string | [OBI lookup service](http://www.ontobee.org/ontology/OBI?iri=http://purl.obolibrary.org/obo/OBI_0000070) <br/> Example: `OBI:0002763` 
**name** | A short, human-readable, machine-read-friendly label for this OBI term| Required | string
**description** | A human-readable description of this OBI term | Optional | string
**synonyms** | A list of synonyms for this term as identified by the OBI metadata | Optional | JSON array of strings | provide empty JSON array `[]` if value is null
