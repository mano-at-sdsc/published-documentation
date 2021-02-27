**Software/command:** cfde-submit run

**Error text:**
`Timeout`

Timeout errors usually indicate that a table that otherwise passed validation is subtlety malformed.

**Possible solutions:**

**1. Fix file encodings**

Our database takes flat text files, and expects ASCII type encodings. Especially if you have built parts of your table by scraping webservices, files or portions of your files, may use other encodings. You can check your encodings by running:

`file *` 

in the directory that holds your submission files. You should get back something like this:

```
[charbo24@dev-intel14 c2m2_level1]$ file *
anatomy.tsv:                       UTF-8 Unicode text, with very long lines
assay_type.tsv:                    ASCII text, with very long lines
biosample_from_subject.tsv:        ASCII text
biosample_in_collection.tsv:       ASCII text
biosample.tsv:                     ASCII text
collection_defined_by_project.tsv: ASCII text
collection_in_collection.tsv:      ASCII text
collection.tsv:                    ASCII text, with very long lines
datapackage.json:                  UTF-8 Unicode text, with very long lines
data_type.tsv:                     ASCII text
file_describes_biosample.tsv:      ASCII text
file_describes_subject.tsv:        ASCII text
file_format.tsv:                   ASCII text
file_in_collection.tsv:            ASCII text
file.tsv:                          ASCII text
id_namespace.tsv:                  ASCII text
ncbi_taxonomy.tsv:                 ASCII text
primary_dcc_contact.tsv:           ASCII text, with very long lines
project_in_project.tsv:            ASCII text
project.tsv:                       ISO-8859 text, with very long lines
subject_in_collection.tsv:         ASCII text
subject_role_taxonomy.tsv:         ASCII text
subject.tsv:                       ASCII text
```

ASCII or UTF encodings are fine. However ISO type encodings like the one for `project.tsv` above will need to be re-encoded.

**1. File size limitations**

If you have tried all the other solutions on this page, and are still getting timeout errors, it's possible that the size or complexity of your submission is exceeding our processing limits. If you suspect this is the case please email [the helpdesk](support@cfde.atlassian.net) for support.