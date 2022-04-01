This table *must not* be manually created. Users should skip this, and all other tables marked "Built by script" in [this summary](./C2M2-Table-Summary), preparing only the rest of their datapackage's TSV files (those marked "Prepared by submitter") for submission. Once the "Prepared by submitter" tables are ready, users should then use the [C2M2 submission prep script](https://osf.io/bq6k9/) to automatically generate this table (and the other "Built by script" tables) using the information in the "Prepared by submitter" tables.

The compound.tsv table will have at most as many rows as the number of unique PubChem terms appearing in the [substance.tsv](./TableInfo:-substance.tsv) table (fewer rows, if multiple substances map to the same compound).


Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A GlyTouCan ID or a PubChem compound ID (CID) | Required |  string | 
**name** | A short, human-readable, machine-read-friendly label for this PubChem CID| Required | string
**description** | A human-readable description of this PubChem CID |  Optional | string
**synonyms** | A list of synonyms for this PubChem CID | Optional | JSON array of strings | provide empty JSON array `[]` if value is null 
