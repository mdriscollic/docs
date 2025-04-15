---
title: "eUsage"
linkTitle: "eUsage"
date: 2025-02-21
weight: 30
tags: ["parenttopic"]
---

The eUsage app allows you to manage usage data reports for electronic resources.

The app provides automatic harvesting of COUNTER standard usage reports via SUSHI and manual uploading of standard and non-standard statistics. Usage data providers managed in eUsage can be referred to from the Agreements app.


## Definition of terms

* **Aggregator**. A service that aggregates pre-processing statistics for multiple statistics providers and offers an endpoint to download the reports. eUsage allows you to harvest statistics for a usage data provider either directly from the provider via SUSHI or from an aggregator. The only aggregator service currently supported in FOLIO is the German National Statistics Server. 
* **COUNTER** and **SUSHI.** Standard format and protocol for electronic resource usage statistics. Detailed information is available at[ Project COUNTER](https://www.projectcounter.org/).
* **Report.** The usage data for a certain set of electronic resources within a certain reporting period in a specific type.
* **Usage data provider.** The agent that provides usage statistics for a set of electronic resources. Most likely, this is a vendor or a platform provider. The usage data provider record is the basic entity in eUsage used to manage all associated reports and harvesting processes.


## **Permissions**

The permissions listed below allow you to interact with the eUsage app and determine what you can or cannot do within the app. You can assign permissions to users in the Users app. If none of these permissions are assigned to a user, they are unable to see the eUsage app or any related information.

The following are all the eUsage permissions:


* **eUsage: All permissions.** Ths permission includes all other eUsage permissions.
* **eUsage: Can view usage data providers and view/download usage reports.** This is the eUsage read permission which allows the user to view usage data provider records and view and download the associated usage reports.
* **eUsage: Can create and edit usage data providers.** This permission allows the user to create and edit UDP records. It does not include the upload of usage reports to the provider.
* **eUsage: Can delete usage data providers.** This permission allows the user to delete UDP records. It does not include the deletion of the associated usage reports.
* **eUsage: Can upload usage reports.** This permission allows the user to upload COUNTER and non-COUNTER usage reports.
* **eUsage: Can start harvesting for a single provider.** This permission allows the user to start the harvester service for one UDP.
* **eUsage: Can delete usage reports.** This permission allows the user to delete COUNTER and non-COUNTER usage reports.
* **Settings (eUsage): Can view and edit settings.** This permission allows the user to view and edit the eUsage settings. It also includes starting the harvester for all usage data providers in the tenant.


## Creating a usage data provider

When you create a usage data provider, you are asked to enter the configuration details for automated harvesting. If the provider only supports manual data download, you still need to create a provider record in order to upload reports manually to this provider. For more information on manual report upload, see Uploading reports manually.

1. In the **Usage data provider** pane, click **New**.
2. In the **Create usage data provider** window, fill in the **Usage data provider information** and **Harvesting configuration** sections. For more information on the fields and actions available in these sections, see the section descriptions below.
3. Once you have included all of the information you want about the Usage data provider, click **Save & close**. The usage data provider is saved and added to the Usage data providers pane.


### Usage data provider information

* **Provider name (required).** Enter the name of the usage data provider.
* **Description.** A description of the usage data provider. You can use this field to enter additional information in order to identify the provider or any other data corresponding to the usage data provider or reports that should be displayed in a prominent place at the record.


### Harvesting configuration

* **Harvesting status (required).** Select a Harvesting status: Active or Inactive. The status you select here defines whether reports from the usage data provider are harvested in the automated or manually triggered harvesting processes.
* **Harvest statistics via (required).** Select how to harvest statistics: Aggregator or Sushi. Note: The only aggregator currently supported by FOLIO is the German National Statistics Server.
* **Aggregator (required).** If you have selected to harvest statistics via an aggregator, select the aggregator that should be used to harvest statistics. Note: The only aggregator currently supported by FOLIO is the German National Statistics Server.
* **Vendor code.** If you have selected to harvest statistics via an aggregator, enter the code by which the aggregator identifies the vendor for which statistics are requested. The German National Statistics Server requires the vendor names as displayed in the server’s user interface.
* **Service type (required).** If you have selected to harvest statistics via a SUSHI protocol, select the SUSHI service type implementation to be used by the harvester. The service type normally corresponds to the requested Report release. 
    * Counter-Sushi 4.1
    * Counter-Sushi 5.0
    * Counter-Sushi 5.1
* **Service URL (required).** If you have selected to harvest statistics via a SUSHI protocol, enter the URL to access the SUSHI service. The URL is usually listed on the provider’s backend information pages. \
Note: Only enter the_ base URL_ to the service, not the complete URL for an API request. For example, if the provider lists the URL[ https://usage.catsanddogs.org/sushi/reports/tr_b1](https://usage.catsanddogs.org/sushi/reports/tr_b1), only enter the part _before (and excluding) "reports"_:[ https://usage.catsanddogs.org/sushi](https://usage.catsanddogs.org/sushi). Everything else is added by the harvester.
* **Report release (required).** Select a Report release. Note: FOLIO does not support the simultaneous harvesting of reports of different releases for a usage data provider. If you want to harvest other report releases as it is configured, first reconfigure the harvester and select the desired release with the corresponding time period.
    * Counter 4
    * Counter 5
    * Counter 5.1
* **Requested report (required).** Add the report types requested to be harvested for the usage data provider. For more information, see Adding a report type.
* **Harvesting start (required)**. Enter the first month for the reports that are to be harvested.
* **Harvesting end.** Enter the last month for the reports that are to be harvested. Note: You may want to add an end month in case no more resources are licensed from a provider, a provider stops supporting usage statistics, or for any other reason that no ongoing harvesting is wanted. If no harvesting end is configured, reports are harvested continuously until the Harvesting status is changed to Inactive.
* **Customer ID (required for SUSHI).** If you have selected to harvest statistics via a SUSHI protocol, enter the customer ID assigned by the provider. This information is usually listed on the provider’s backend information pages.
* **Requestor ID.** Enter the Requestor ID assigned by the provider. If needed, this information is usually listed on the provider’s backend information pages. Not all SUSHI services require a Requestor ID.
* **API key.** Enter the API key assigned by the provider. If needed, this information is usually listed on the provider’s backend information pages. Not all SUSHI services require an API key.
* **Platform.** Enter the Platform for which reports are requested. If needed, this information is usually listed on the provider’s backend information pages. Most SUSHI services default on all platforms for which a customer has licensed resources.
* **Requestor name.** Enter the requestor name assigned by the provider. If needed, this information is usually listed on the provider’s backend information pages. Not all SUSHI services require a Requestor name.
* **Requestor mail.** Enter the requestor mail assigned by the provider. If needed, this information is usually listed on the provider’s backend information pages. Not all SUSHI services require a Requestor mail.


#### Adding a report type

1. Click **Add report type**.
2. Choose a **Report type** from the list of available report types for the chosen Report Release. You can filter the list.
3. Repeat as needed. The report type saves once you save the usage data provider.


#### Deleting a report type

1. Find the Report type you want to delete.
2. Click the **trash can icon**. The Report type is deleted and is removed from the record once you save the usage data provider.


#### Setting up an aggregator

It is possible to use an aggregator to retrieve statistics. Setting up an aggregator can be done in the Settings app. For more information on this, see [Settings > General > Aggregators](../../settings/settings_eusage/settings_eusage/#settings--general--aggregators).


#### Hide sushi credentials in detail views

If you want, you can hide the display of SUSHI credentials in the detailed view for a usage data provider in the UI. For more information on this, see [Settings > General > Display settings](../../settings/settings_eusage/settings_eusage/#settings--general--display-settings).


## Starting the harvesting process

### Starting the harvester for a specific usage data provider

1. Find the usage data provider for which you want to start the harvesting process.
2. In the **usage data provider details** pane, click **Actions > Start harvester**. A confirmation message appears.
3. Optional: If you want to view the current results of the harvesting process, you can refresh the table content in the **COUNTER statistics** table. To do this, click **Actions > Refresh statistics table**. Otherwise, the table content will be refreshed the next time you select the usage data provider or refresh the browser window.


### Starting the harvester for all usage data providers 

Starting the harvester for all usage data providers is an optional way. This can be done in the Settings app. For more information on this, see [Settings \> General \> Start harvester](../../settings/settings_eusage/settings_eusage/#settings--harvester--start-harvester).


### Setting up periodic harvesting

It is possible to set the interval for the automatic harvesting process. This can be done in the Settings app. For more information on this, see [Settings \> General \> Periodic harvesting](../../settings/settings_eusage/settings_eusage/#settings--harvester--periodic-harvesting).

## Editing a usage data provider

1. Find the usage data provider you want to edit and select it.
2. In the **usage data provider details** pane, click **Actions > Edit**.
3. Edit the usage data provider.
4. Click **Save & close**. The usage data provider is saved and updated.


### Changing the harvesting configuration

Note: Changing the harvesting configuration for a usage data provider doesn’t affect reports already stored in the system. No reports are lost. The configuration is only applied to future harvesting processes. For information on how reports are deleted, see Deleting reports.


1. Find the usage data provider you want to edit and select it.
2. In the **usage data provider details** pane, click **Actions > Edit**.
3. Edit the **Harvesting configuration**.
4. Make any additional changes to the usage data provider.
5. Click **Save & close**. The usage data provider is saved and updated.


### Adding a tag to a usage data provider

1. Find the usage data provider you want to tag and select it.
2. In the **usage data provider details** pane, click the **tag icon**.
3. In the **Tags** pane, either select a tag from the box or enter a tag. 
4. Click the **X** on the **Tags** pane to close the pane and save the tag. The tag number updates to the number of tags applied to the usage data provider.


### Adding a note to a usage data provider

1. Find the usage data provider to which you want to add a note and select it.
2. In the **usage data provider details** pane, click **Notes > New**.
3. In the **New note** window, select the **Note type** from the drop-down list. Note types are created in the Settings app. For more information, see Settings > Notes.
4. Enter a **Note title** in the box.
5. Optional: Enter any **Details** about the note in the box.
6. Click **Save & close**. The note is saved and appears in the Notes section in the usage data provider details pane.


### Deleting a usage data provider

1. Find the usage data provider you want to delete and select it.
2. In the **usage data provider details** pane, click **Actions > Edit**.
3. In the **usage data provider edit** window, click **Delete**.
4. In the **Delete usage data Provider** dialog, click **Delete**. The usage data provider and all associated reports are deleted and a confirmation message appears.


## Management of statistics

### Viewing stored COUNTER reports for a usage data provider

1. Find the usage data provider for which you want to view the stored reports and select it.
2. In the **usage data provider details** pane, click **COUNTER statistics**.
3. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.

The **COUNTER statistics table** displays a row for each report type and a column for each month, grouped by release. If a report is stored or has tried to harvest, a **Report button** is displayed in the appropriate cell of the table. The buttons show the state of the report with an icon:

* **Green/checkmark.** A valid report is available for the month.
* **Orange/exclamation mark.** The report tried to harvest but failed. The harvester tries again in the next harvesting cycle.
* **Red/Cross.** The report tried to harvest for the maximum number of attempts defined in the Settings. In order to attempt another harvest, the report needs to be deleted. For more information, see Setting maximum number of harvesting attempts and Deleting reports.

In the **COUNTER statistics table,** click on a **Report button**. The **Report info** dialog displays with additional information about the report:

* **Usage data provider.** The name of the usage data provider.
* **Type.** The report type.
* **Date.** The reporting period, always one month.
* **Info.** If the report failed to harvest correctly, the error message provided by the SUSHI service is displayed here.
* **Failed attempts.** Number of attempted harvestings, which is also the number of maximum attempts.
* **Manual changes.** If the report has been manually altered, this heading appears along with the reason the report was manually edited.
* **Actions.** Possible actions, for more information see Deleting reports and Downloading reports.


### Uploading a COUNTER report manually

1. Find the usage data provider for which you want to manually upload a COUNTER report.
2. In the **usage data provider details** pane, click **Actions > Upload Counter report**.
3. The window **Upload COUNTER report** opens to select and upload the file. Select a file by dragging and dropping the file into the upload form field or select a file via your file manager using **or select file** button. 
4. Click on **Save**.

**File types**
* Please note the information on the file type for each report release.
* You can only use COUNTER Master Reports. It is not possible to upload standard views. Standard views can be generated by the program using the download function if you have saved a COUNTER Master Report.
* COUNTER 5.1: With FOLIO Release Sunflower, reports for Release 5.1 can only be uploaded manually as JSON. Other formats will follow with the next FOLIO release.

**Options in the upload form for COUNTER reports**
* You can mark a manual upload as manually edited. To do this, use the checkbox **Report data has been edited manually** in the upload form. 
* **Edit reason** is a text field to create a comment.


### Uploading a non-COUNTER report

1. Find the usage data provider for which you want to manually upload a non-COUNTER report.
2. In the **usage data provider details** pane, click **Actions > Upload non-Counter report**.
3. The window **Upload non-COUNTER report** opens to enter information about the non-Counter report and select and upload the file.
4. Fields in the upload form
* **YEAR** (required) Specify the year in the form YYYY.
* **Note** A note can be left.
* Type of data storage can be chosen by using the radio buttons.
    * **Upload file** With this option you can upload a non-Counter report to the system. Select a file by dragging and dropping the file into the upload form field or select a file via your file manager using **or select file** button. Then click **Save**.
    * **Link file** This option allows you to enter a URL or a file path as text. Then click **Save**. Please note: The file paths are displayed as links in the user interface, but the browser requires permissions so that the links to the file paths are executed when they are clicked.


### Downloading a COUNTER report

1. Find the usage data provider from which you want to download a COUNTER report.
2. In the **usage data provider details** pane, click **COUNTER statistics**.
3. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.
4. Select the COUNTER report by clicking on its icon in the table.
5. The window **Report info** opens.
6. Under **Actions** you can select one of the listed file types for download.
7. The window of the file manager opens and you can save the report on your system via the file manager.


### Downloading COUNTER reports for multiple months

1. Find the usage data provider from which you want to download one ore more COUNTER reports.
2. In the **usage data provider details** pane, click **COUNTER statistics**. If reports are stored, they are displayed in a separate table for each year. You can click on the year you want to view or click **Expand all years**.
3. Under the **COUNTER statistics** there is an area **Download reports for multiple months**. In this form you can enter information about the time period required, the report type and the export format required.
4. Then click **Download**.
5. The window of the file manager opens and you can save the report on your system via the file manager. Please note that if you have a large amount of data, processing takes some time and the file manager opens with a delay.


### Downloading a non-COUNTER report

1. Find the usage data provider from which you want to download a non-COUNTER report.
2. In the **usage data provider details** pane, click **Non-COUNTER statistics**.
3. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.
4. Select the non-COUNTER report by clicking on its **information icon** in the table.
5. The window **Customreport info** opens.
6. Under **Actions** you can select one of the listed file types for download.
7. The window of the file manager opens and you can save the report on your system via the file manager.


### Deleting a single COUNTER report

1. Find the usage data provider for which you want to view the stored reports and select it.
2. In the **usage data provider details** pane, click **COUNTER statistics**.
3. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.
4. Select the COUNTER report by clicking on its **icon** (Green/checkmark or Orange/exclamation mark or Red/Cross) in the table.
5. The window **Report info** opens.
6. Under **Actions** you can click on **Delete report**.
7. Confirm the question **Delete Counter report?** by clicking **Yes**.


### Deleting multiple COUNTER reports

1. Find the usage data provider for which you want to view the stored reports and select it.
2. In the **usage data provider details** pane, click **Actions > Delete reports**.
3. The window **Delete multiple reports** opens.
4. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.
5. You can select the reports that should be deleted using the associated checkbox.
6. Then click **Delete reports**.
7. Confirm the question **Are you sure to delete multiple reports?** by clicking **Delete**.


### Deleting a non-COUNTER report

1. Find the usage data provider for which you want to view the stored reports and select it.
2. In the **usage data provider details** pane, click **Non-COUNTER statistics**.
3. If reports are stored, they are displayed in a separate table for each year. Click on the year you want to view or click **Expand all years**.
4. Select the COUNTER report by clicking on its **information icon** in the table.
5. The window **Customreport info** opens.
6. Under **Actions** you can click on **Delete custom report**.
7. Confirm the question **Delete non-counter report?** by clicking **Yes**.


## Searching for a usage data provider

You can search for usage data providers in the **Search & filter** pane. To search for a usage data provider, enter your search terms into the box and click **Search**. Once you search for a usage data provider, the following information appears in the usage data providers pane:

* **Provider name.** The name of the usage data provider.
* **Harvesting status.** The status of the usage data provider.
* **Latest statistics.** The month of the most current report stored in FOLIO.
* **Aggregator.** The aggregator from which reports are currently configured to harvest.

In the search results, click on a usage data provider to view it. The **usage data provider details** pane displays with additional information about the usage data provider and the associated reports stored in FOLIO.

You can also search for usage data providers by selecting any of the filters in the **Search & filter** pane. Additionally, you can apply the filters after you perform a search to limit your results. See the sections below for more information.


### Harvesting status

To filter usage data providers by their status, select one of the following:

* **Active.** Usage data providers included in the current harvesting processes.
* **Inactive.** Usage data providers for which no reports are currently being harvested.


### Harvest via

To filter usage data providers by the harvest method of their reports, select one of the following:

* **Sushi.** Usage data providers where reports are currently configured to be harvested directly from the provider via SUSHI.
* **Aggregator.** Usage data providers where reports are currently configured to be harvested via an aggregator.


### Aggregators

To filter usage data providers by the aggregator used for the harvesting, select one of the Aggregators configured for the tenant. For more information, see Aggregator configuration.


### Report types

To search for usage data providers for which reports of a specific type are stored in FOLIO, follow these steps:

1. In the **Search & filter** pane, click **Report types**.
2. Select the type(s) from the drop-down list. Your results appear in the usage data provider pane.


### Report releases

To search for usage data providers with specific versions of COUNTER reports that have been saved, follow these steps:

1. In the **Search & filter** pane, click **Report releases**.
2. Select the versions of COUNTER reports from the drop-down list. Your results appear in the usage data provider pane. The list shows usage data providers that have reports with one of the selected versions.


### Has failed report(s)

To filter usage data providers based on whether harvesting errors have occurred, select one of the following:

* **Yes.** Usage data providers where at least one requested report has not been harvested correctly.
* **No.** Usage data providers where no reports have failed to be harvested.


### Tags

To search for usage data providers assigned with specific tags, follow these steps:

1. In the **Search & filter** pane, click **Tags**.
2. Select the tag(s) from the drop-down list. Your results appear in the usage data provider pane.


### Error codes

To search for usage data providers with reports that have failed with a specific SUSHI error code, follow these steps:

1. In the **Search & filter** pane, click **Error code**.
2. Select the error code(s) from the drop-down list. Your results appear in the usage data provider pane. The list shows usage data providers that have reports failed with either of the selected error codes.


## Plugin: eUsage reports

* All features of the eUsage Reports software still need to be documented. It is a plugin for eUsage. At the moment there are only instructions in the FOLIO wiki.
