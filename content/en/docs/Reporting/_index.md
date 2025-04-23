---
title: "Reporting with Metadb"
linkTitle: "Reporting with Metadb"
date: 2024-12-04
weight: 650
---

The [Library Data Platform (LDP)](https://librarydataplatform.org) is a project that develops an open-source platform which is utilized by both the [FOLIO](http://folio.org/) and [ReShare](https://projectreshare.org/) projects to provide statistical and operational analytics. One of the core technologies being developed as part of the LDP project is Metadb, an open-source data integration system that transforms, versions, and annotates streaming data from multiple sources. The Metadb software extracts data from FOLIO modules into a relational database, making it possible to engage in complex reporting and analytics using FOLIO data. While some FOLIO apps have built-in reports or the ability to download results from a search-and-filter workflow, Metadb supports larger and more complex queries that combine data from across the FOLIO apps. Metadb has been adopted by many institutions. Find detailed and very recent information about the platforms on the [project website](https://librarydataplatform.org).

Some FOLIO apps include functionality that allows the user to download data as a CSV (comma separated values) file. For example, the Users app allows you to run an overdue loans report and download the results as a CSV file. See the documentation on individual apps for more details on this functionality where it is available.


## Data Flow from FOLIO to Metadb

The basic flow of data from FOLIO to Metadb is described in the figure below. Metadb extracts data from the database used by FOLIO apps. From Metadb, data flows into two types of queries: derived tables (which simplify the FOLIO data and save the results back into Metadb) and report queries (which meet specific needs of report users). These queries are shared via the [FOLIO Analytics query repository](folio-analytics) and also form the backbone of [ad hoc querying](folio-analytics/#ad-hoc-querying-using-metadb-tables).

![The Metadb software extracts data from the FOLIO database and loads into its own Metadb database. The FOLIO Analytics repository stores derived table queries, which add derived tables to the Metadb database, and report queries, which build reports for reporting end users. The Metadb database can also be used to store non-FOLIO data in custom tables.](/img/dataflow.png)


## Features of Metadb

* Open-source software and query development
* Built on trusted database platforms
* Ability to create custom tables to import non-FOLIO data
* Historical tracking of FOLIO records
* Ability to connect from a wide variety of reporting applications
* Ability to perform cross-app FOLIO queries
* Ability to query FOLIO data without impacting production application performance
* Ability to query a simplified FOLIO data model through the use of derived tables
* Nearly real time data through streaming technique
* JSON data array extraction
* Full FOLIO data coverage