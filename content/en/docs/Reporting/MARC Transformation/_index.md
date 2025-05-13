---
title: "MARC Transformation"
linkTitle: "MARC Transformation"
date: 2025-04-08
weight: 40
tags: ["parenttopic"]
---

## MARC Transformation for Metadb

Metadb converts SRS/MARC records from JSON to tabular format. SRS stands for Source Record Storage. MARC stands for Machine-Readable Cataloging, which is a standard format for storing data elements within bibliographic records in computer systems. Metadb reads the SRS MARC data from the database tables marc_records_lb and records_lb in schema folio_source_record. Next, it transforms only the current versions of the records from these tables into tabular data. The transformed records are written to the folio_source_record.marc__t table.

Once the MARC data is transformed, the folio_source_record.marc__t table is ready to be used in queries that require MARC data from the reporting database. For example, the query below shows the contents of the MARC 008 field, which captures general bibliographic information about a library item.

```
SELECT
    sm.instance_hrid,
    sm.field,
    sm.content
FROM folio_source_record.marc__t AS sm
WHERE (sm.field = '008')    
LIMIT 10
;
```
For more information about how MARC data is transformed in Metadb, please review the guide linked below:

* [MARC Transformation Guide for Metadb](https://d1f3dtrg62pav.cloudfront.net/doc/#_marc_transform)