Software/command: cfde-submit run

Error text:
`TableSchema invalid due to the following errors:`

Possible solutions:

1. Missing a table(s) or misnamed table(s)

If your error message says something like

`TableSchema invalid due to the following errors:`
`[Errno 2] No such file or directory: '/tmp/bag__8k28zvv/HMP__sample_C2M2_Level_1_bdbag.contents_9f1b30a40cf2d0f345d453311041bc7a969716b3/data/collection_in_collection.tsv'`

Then you are either missing an expected table, or the name of the table is incorrect. The tables in your submission must exactly match the table names listed in the json file included in your submission. 
