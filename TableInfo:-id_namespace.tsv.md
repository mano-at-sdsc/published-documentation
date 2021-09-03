A table listing identifier namespaces registered by the DCC submitting this C2M2 instance

Each identifier namespace is a unique URI prefix, pre-registered with CFDE and attached to your program (or a subset of your program) that identifies anything labeled with it as belonging to you. Please see the [technical documentation](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#c2m2-identifiers) for a full discussion of how this information is built and used.

The `id_namespace.tsv` table will contain one row per identifier namespace registered with CFDE for your program.

Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**id** | A globally unique ID representing this identifier namespace | Required | Every row must have a value; Value type is string | In the simplest case, your program would use the exact same value for the `id_namespace` column in every row for every table. More complex Programs may choose to use multiple namespaces. 
**abbreviation** | A very short display label for this namespace | Non-required: Any number of rows after the header can be filled | Value should be 10 characters or fewer<br /><br />  The value in each row must be different <br /><br /> Cannot contain special unix characters| This is the display abbreviation for this namespace in the portal
**name** | A short, human-readable, machine-read-friendly label for this namespace | Non-required: Any number of rows after the header can be filled |Value can be any string; The value in each row must be different | This is the display name for this namespace in the portal
**description** | A human-readable description of this namespace | Non-required: Any number of rows after the header can be filled | Value type is string | This is the display descripton for this namespace in the portal