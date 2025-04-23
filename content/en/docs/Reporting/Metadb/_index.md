---
title: "Metadb"
linkTitle: "Metadb"
date: 2024-12-04 
weight: 30
tags: ["parenttopic"]
---



<b>**Note**: This [WOLFcon 2024 presentation](https://youtu.be/ACBBSZ6Lx_s?feature=shared) gives an overview of the Metadb platform.
</b>

In order for the Metadb software to connect to FOLIO, it needs a [Kafka data source](https://d1f3dtrg62pav.cloudfront.net/doc/#_configuring_a_kafka_data_source) streaming the changes made in the FOLIO database. The Metadb reporting database can be hosted and administered locally by an institution's own staff or can be contracted out to a third party hosting service. You can find specific [system requirements](https://d1f3dtrg62pav.cloudfront.net/doc/#_system_requirements) in the Metadb documentation.

## Installing and configuring the Metadb software*

There are three main software components to install for your Metadb implementation: Metadb, marct, and Folio Analytics. In general, install the latest production release for the Metadb and marct software components, which do not have a dependency on FOLIO (flower) software release versions. For FOLIO Analytics, see https://github.com/folio-org/folio-analytics/blob/main/README.md.

### Documentation

For detailed information about how to set up and configure the Metadb software, please review this [link](https://github.com/library-data-platform/ldp#readme) to access individual links to guides in the Metadb repository. There you also will find the latest versions and fixes of the Metadb software.

## Setting up derived tables

To let report users take full advantage of the community-developed [report queries](../folio-analytics/#using-queries-from-the-folio-analytics-repository) as well as having a good starting point for [ad hoc querying](../folio-analytics/#ad-hoc-querying-using-ldp-tables), it is strongly recommended to set up a nightly update on [derived tables](https://github.com/folio-org/folio-analytics/blob/main/sql/derived_tables/README.md  ).


<b>
**Note**: Use of *views* and *materialized views* is not supported in Metadb databases and may cause the software to be unable to perform data updates.
</b>

You can find instructions in Github on how to set up [FOLIO Reporting Derived Tables](https://github.com/folio-org/folio-analytics/tree/main/sql/derived_tables#folio-reporting-derived-tables).

## Data privacy

The Metadb software is designed to support GDPR and other data privacy requirements. Administrators can exclude a predefined set of tables.

See the [Anonymization Guide](https://github.com/library-data-platform/ldp/blob/main/doc/Admin_Guide.md#6-data-privacy) for information on how to activate and configure these features.

The pages linked below list attributes that contain potential personal data:

* [Users module](https://wiki.folio.org/display/RPT/Potential+personal+data%3A+List+of+FOLIO+attributes?src=contextnavpagetreemode): tables that will not loaded in Metadb software when anonymization is turned on
* [Organizations module](https://wiki.folio.org/display/RPT/Potential+personal+data+in+mod-organizations-storage?src=contextnavpagetreemode): potential personal data in organizations module

<b>
**Note:** The Metadb software currently does not support anonymization. The above information is for LDP software only. 
</b>

## Adding local data
As documented in the [user guide](https://github.com/library-data-platform/ldp/blob/main/doc/User_Guide.md#4-local-tables), it is also possible to load and create local data into your Metadb reporting database.

### Using schemas
The concept of schemas allows you to organize tables and permissions within one database. In Metadb, we have separate schemas for each FOLIO application area:

* public: contains all extracted tables and its current data from the bound FOLIO tenant
* [history](https://github.com/library-data-platform/ldp/blob/main/doc/User_Guide.md#6-historical-data): stores data that have been updated in the past or may no longer exist
* [folio_reporting](https://github.com/folio-org/folio-analytics/blob/main/sql/derived_tables/README.md): contains all [derived tables](https://github.com/folio-org/folio-analytics/blob/main/sql/derived_tables) created and supported by the community
* [local](https://github.com/library-data-platform/ldp/blob/main/doc/User_Guide.md#4-local-tables): common area for report users to create or import own data

Besides using the local schema, you might consider setting up separate schemas for different report user groups or purposes. You are free to create more schemas for your local needs (e.g., to provide data for different departments or to separate and protect sensitive data).

Learn more about the schema concept and how to configure schemas using [Postgres's Schema Documentation](https://www.postgresql.org/docs/current/ddl-schemas.html).

For a granular setup of permissions, see also the built-in [Roles](https://www.postgresql.org/docs/current/user-manag.html) and [Privileges](https://www.postgresql.org/docs/current/ddl-priv.html) concepts of Postgres.

### Moving and loading data
Loading and moving data into a Metadb reporting database is as simple as it is for databases in general.

For Postgres there are two common approaches:

* [COPY](https://www.postgresql.org/docs/current/sql-copy.html): SQL command for moving table data via csv files
* [pg_dump](https://www.postgresql.org/docs/current/app-pgdump.html) / [pg_restore](https://www.postgresql.org/docs/current/app-pgrestore.html): Postgres command line tools for importing and exporting data

## Installing and configuring the Metadb software
For installing and configuring Metadb follow the *Metadb Documentation* at the [Library Data Platform - resources site](https://librarydataplatform.org/resources/).