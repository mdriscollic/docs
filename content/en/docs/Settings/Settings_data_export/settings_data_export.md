---
title: "Settings > Data export"
linkTitle: "Data export"
date: 2023-11-06
weight: 60
tags: ["subtopic"]   
---

The Data export section of the Settings app is where you can configure the job profiles used in the data export process. Job profiles determine how information is exported to the MARC file that is generated as a result of the export.

The Data export app comes with one or more default job profiles that export instance, holdings, or authority data. Additional profiles can be created as needed. The mapping profiles allow you to customize the data that is used in the job profile.

The mapping and job profiles add flexibility to the data export and provide an easy way to execute a different type of export on the same data set or the same type of export on different data sets.  For example, one user can export bibliographic data only and another user can export instances with appended elements of the holdings and items records using the same set of data.

## Permissions

In order to interact with Data export settings, a user needs to be assigned the following permission:

-   **Settings (data-export): display list of settings pages.** This permission allows the user to set up data export profiles.

## Capabilities

The capabilities listed below allow you view and interact with Data Export settings. You can assign capabilities to users via user roles. If none of these capabilities are assigned to a user, they are unable to see Data Export settings or any related information.

See [Settings > Authorization roles](../../settings_authorization-roles/settings_authorization-roles/) for instructions on how to create and assign Authorization roles. It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities.

|**Permission Display name (OKAPI)** | **Resource (EUREKA)** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Settings (Data export): Can view only** | **UI-Data-Export Settings** | settings | view | This permission allows the user to see the Data Export settings but not make any changes to them.|
|**Settings (Data export): Can view, add, update profiles** | **UI-Data-Export Settings** | settings | edit | This capability allows the user to see and and change the Data Export settings.|

---

## Managing profiles

Job profiles and field mapping profiles can be locked, unlocked, edited, duplicated, or deleted based on your assigned capabilities.

### Locking and unlocking profiles
Locking or unlocking a profile requires special authorization.
* When a profile is locked, only authorized users may edit or unlock it. 
* Other users can view and duplicate the profile, but cannot edit or delete it.
* All default profiles are locked and cannot be unlocked.

---

## Settings \> Data export \> Job profiles

When exporting data, each export is associated with a job profile. The job profile provides a way of connecting a specific list of record identifiers with a field mapping profile. The field mapping profile determines how the data from FOLIO records appears in the generated MARC file.

Before you begin configuring job profiles, you should first configure your field mapping profiles. See [Settings \> Data export \> Field mapping profiles](#settings--data-export--field-mapping-profiles), below, for more information.

### Default export job profile

The system comes with one or more default job profiles that are associated with default field mapping profiles. Records exported with a default job profile generate a MARC file containing information for the provided record IDs. 

If you use a default job profile, simplified MARC bibliographic records are generated for instances without underlying MARC records. For instances with underlying MARC records stored in SRS, those records are used in the export.

### Creating an export job profile

1.  In the **Job profiles** pane, click **New**.
2.  Enter a **Name** for the job profile.
3.  Select a **Mapping profile** from the drop-down list. Field mapping profiles are created in Settings. See [Settings \> Data export \> Field mapping profiles](#settings--data-export--field-mapping-profiles) for more information.
4.  Optional: Enter a **Description** of the job profile.
5.  Click **Save & close**. A confirmation message appears and the job profile is created.

### Searching for an export job profile

Use the search bar to search for profiles contained in the Job profile list. 

The Job profiles list contains the following columns:

-   **Name.** Name of the job profile.
-   **Updated.** Date the job profile was last updated.
-   **Updated by.** User who last updated the job profile.

You can click on any column name to sort by that column.

### Viewing an export job profile

To view the details of a job profile, follow these steps:

-   In the **Job profiles** pane, find the profile you want to view and select it. The **export job profile details** window appears.

### Editing an export job profile

> **Note:** A job profile can only be edited if it is unlocked and you have the appropriate authorized capabilities.

1.  In the **Job profiles** pane, find the profile you want to edit and select it.
2.  In the **export job profile details** window, click **Actions \> Edit**.

### Duplicating an export job profile

1.  In the **Job profiles** pane, find the profile you want to duplicate and select it.
2.  In the **export job profile details** window, click **Actions \> Duplicate**.

### Deleting an export job profile

> **Note:** Job profiles can be deleted as long as they are not locked. 
> * If a job profile has previously been used for a data export, deleting it removes all generated export files associated with that profile from the download logs.
> * Data export logs will retain the profile name with a `(deleted)` suffix for traceability.
> * Deleting a job profile does not remove any associated field mapping profiles.

1.  In the **Job profiles** pane, find the job profile you want to delete and select it.
2.  In the **export job profile details** window, click **Actions \> Delete**.
3.  In the **Delete job profile** dialog, click **Delete**. A confirmation message appears and the job profile is deleted.

---

## Settings \> Data export \> Field mapping profiles

The system comes with one or more default field mapping profiles that are associated with a [default job profile](#default-export-job-profile). A field mapping profile determines how the data from FOLIO records appears in the generated MARC file.

### Creating an export field mapping profile

1.  In the **Field mapping profiles** pane, click **New**.
2.  In the **New field mapping profile** window, enter a **Name** for the field mapping profile.
3.  Select an **Output format** from the drop-down list. MARC is the only option.
4.  Select as many **FOLIO record types** that apply by selecting the checkbox next to the option: Source record storage (entire record), Inventory instance (selected fields), Holdings, and/or Item. You must select at least one option.
5.  Optional: Enter a **Description** for the field mapping profile.
6.  Optional: Exclude MARC fields from export with **Fields suppression**.
7.  Optional: To add a transformation, click **Add transformations** and follow these steps:
    <ol type="a">
      <li>In the <strong>Select transformations</strong> dialog, use the search box and filters to find the transformations you want to add to the field mapping profile.</li>
      <li>For every transformation you want to add, select the <strong>checkbox</strong> next to it and fill out the field number, indicators, and subfield boxes. Subfields must begin with a $.</li>
      <li>Once you have added all transformations, click <strong>Save & close</strong>. A confirmation message appears and the transformations are added to the field mapping profile.</li>
    </ol>
8.  Click **Save & close**. A confirmation message appears and the field mapping profile is created.

### Searching for an export field mapping profile

Use the search bar to search for profiles contained in the Field mapping profiles list. 

The Field mapping profiles list contains the following columns:

-   **Name.** Name of the job profile.
-   **FOLIO record type.** The types of records included in the export: Source record storage (entire record), Authority, Instance, Holdings, and/or Item.
-   **Format.** Format of the exported record.
-   **Updated.** Date the field mapping profile was last updated.
-   **Updated by.** User or system who last updated the field mapping profile.

You can click on any column name to sort by that column.

### Viewing an export field mapping profile

To view the details of a field mapping profile, follow these steps:

-   In the **Field mapping profiles** pane, find the profile you want to view and select it. The **field mapping profile details** window appears.

### Editing an export field mapping profile

> **Note:** A field mapping profile can only be edited if it is unlocked and you have the appropriate authorized capabilities.

1.  In the **Field mapping profiles** pane, find the profile you want to edit and select it.
2.  In the **field mapping profile details** window, click **Actions \> Edit**.
3.  Make your changes to the profile.
4.  Click **Save & close**. A confirmation message appears and the field mapping profile is updated.

### Duplicating an export field mapping profile

1.  In the **Field mapping profiles** pane, find the profile you want to duplicate and select it.
2.  In the **field mapping profile details** window, click **Actions \> Duplicate**.
3.  In the **New field mapping profile** window, make your desired changes to the duplicated policy.
4.  Click **Save & close**. A confirmation message appears and the field mapping profile is created.

### Deleting an export field mapping profile

> **Note:** Field mapping profiles can be deleted if they are not locked, and **only** when they are not referenced by any existing (non-deleted) job profiles. If a field mapping profile is in use, you must first remove or replace its references in all associated job profiles before deletion is permitted.

1.  In the **Field mapping profiles** pane, find the profile you want to delete and select it.
2.  In the **field mapping profile details** window, click **Actions \> Delete**.
3.  In the **Delete mapping profile** dialog, click **Delete**. A confirmation message appears and the field mapping profile is deleted.
