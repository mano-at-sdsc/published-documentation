This table does *not* need to be manually created. Users can build the rest of their data package and then use the CFDE Helper script to automatically build this table from the completed tables.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | An NCBI Taxonomy Database ID identifying a particular taxon | Required | Value type is string 
**clade** | The phylogenetic level (e.g. species, genus) assigned to this taxon| Required | Value type is string
**name** | A short, human-readable, machine-read-friendly label for this taxon | Non-required: Any number of rows after the header can be filled | Value type is string
**description** | A human-readable description of this Uberon term |  Non-required: Any number of rows after the header can be filled | Value type is string
**synonyms** | Pipe-separated list of synonyms alternate NCBI Taxonomy IDs) equivalent to this taxon | Non-required: Any number of rows after the header can be filled | Value must be a valid NCBI Taxonomy Database ID | 