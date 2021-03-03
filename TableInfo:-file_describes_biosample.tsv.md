The collection_in_collection table will contain one row per nested collection in your organization. If you are nesting multiple collections within each other, you should only specify the most proximate relationships. e.g. if you have the collections Dogs, Cats, Animals, LivingThings your table should have a for each of: Cats in Animals, Dogs in Animals, and Animals in LivingThings. But you should not additionally specify 'Dogs in LivingThings', as that relationship will be derived from the inherent tree-like structure.


Field | Field Description | Required? |  Attributes | Extra Info 
------|-------------------|-----------|-------------|------------
**superset_collection_id_namespace** | ID of the identifier namespace corresponding to the top-level C2M2 metadataset containing the superset collection string | Required if table is populated
**superset_collection_local_id** | The ID of the superset collection string | Required if table is populated
**subset_collection_id_namespace** |ID of the identifier namespace corresponding to the top-level C2M2 metadataset containing the subset collection string. | Required if table is populated
**subset_collection_local_id** | The ID of the subset collection string |Required if table is populated