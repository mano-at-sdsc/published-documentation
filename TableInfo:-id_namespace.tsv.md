A table listing identifier namespaces registered by the DCC submitting this C2M2 instance

Each identifier namespace is a unique URI prefix, pre-registered with CFDE and attached to your program (or a subset of your program) that identifies anything labeled with it as belonging to you. Please see the [technical documentation](https://docs.nih-cfde.org/en/latest/c2m2/draft-C2M2_specification/#c2m2-identifiers) for a full discussion of how this information is built and used.

The `id_namespace.tsv` table will contain one row per identifier namespace registered with CFDE for your program.

Field | Field Description | Required? | Field Value Type | Extra Info 
------|-------------------|:-----------:|:-------------:|------------
**id** | A globally unique ID representing this identifier namespace | Required | string | 
**abbreviation** | A very short display label for this namespace | Optional | string | Should not exceed 10 characters; can only contain 0-9, a-z, A-Z and underscore ("`_`")
**name** | A short, human-readable, machine-read-friendly label for this namespace | Required | string | Must be unique to each namespace
**description** | A human-readable description of this namespace | Optional | string | 