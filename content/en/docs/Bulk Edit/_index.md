---
title: "Bulk Edit"
linkTitle: "Bulk Edit"
date: 2025-01-22
weight: 550
---

**This section of the documentation contains links to external sites. Please be advised that these external sites are not maintained by the FOLIO Documentation Group and may not be aligned with a different FOLIO release.**


The Bulk Edit app allows a user to apply changes to multiple Inventory or User records simultaneously. 


## Permissions

The permissions listed below allow you to interact with the Bulk Edit app and determine what you can or cannot do within the app. Bulk edit permissions, combined with other functional app permissions, allow a user to access specific areas of the Bulk Edit app. 

Permissions are assigned to users in the Users app. If none of the Bulk edit permissions are assigned to a user, they are unable to see the Bulk Edit app or any related information. 
See [Users \> Assign or unassign permissions](../users/#assign-or-unassign-permissions) for more information. 

The following are the permissions for the Bulk edit app:

- **Bulk edit: Can build query**: This permission allows the user to build and test a query, and preview matched records in the Bulk edit app. 
- **Bulk edit: Can view logs** This permission allows the user to download and view logs in the Bulk Edit app.
- **Bulk edit: In app - Edit inventory records** This permission allows the user to edit a field in multiple inventory records in the Bulk Edit app.
- **Bulk edit: In app - Edit user records**. This permission allows the user to edit a field in multiple user records in the Bulk edit app. 
- **Bulk edit: In app - View inventory records** This permission allows the user to view a list of identified inventory records in the Bulk Edit app. 
- **Bulk edit: Local - Edit user records** This permission allows the user to edit a field in multiple identified user records in the Bulk Edit app by uploading a .csv file.
- **Bulk edit: Local - View user records** This permission allows the user to view a list of identified user records in Bulk Edit by uploading a .csv file.


## Identify records for bulk edit

The Bulk edit app provides two methods for setting criteria and identifying records for bulk edit: **Identifier** and **Query**.  In either method, the **Record identifiers** or **Fields** available for selection are based on the **Record type**.


### Identifier

The **Identifier** approach allows the user to set criteria for the bulk edit by uploading a list of record identifiers from a .csv file. 

To set criteria for bulk edit using **Identifier**: 

1. In the **Set Criteria** pane, select the **Identifier** button.
2. Select the **Record type**. The following **Record types** are available for bulk edit:
   
   - Inventory - holdings
   - Inventory - instances
   - Inventory - items
   - Users

     
4. Select the **Record identifier** from the **Select record identifier** drop-down menu. [Record identifiers available for selection](#record-identifiers-by-record-type) are based on the Record type.
5. **Drag and drop** your .csv file into the **Select a file with record identifiers** box, or click **or choose file** to upload the .csv file from your computer. Only .csv files containing one column of record identifiers are accepted for upload in the Bulk edit app. If the .csv file contains more than one column, the upload will not be successful and an error message, "_filename_ is formatted incorrectly. Please correct the formatting and upload the file again" displays. 

#### Record identifiers by record type

In the **Identifier** method, the **Record identifiers** available for selection are based on the selected **Record type**. 

| Record Type | Record identifier | 
| :-----: | :-----: |  
| *Inventory - holdings* | Holdings UUIDs | 
| *Inventory - holdings* | Holdings HRIDs |
| *Inventory - holdings* | Instance HRIDs |
| *Inventory - holdings* | Item barcodes |
| *Inventory - instances* | Instance UUIDs |
| *Inventory - instances* | Instance HRIDs |
| *Inventory - items* | Item barcodes |
| *Inventory - items* | Item UUIDs |
| *Inventory - items* | Item HRIDs |
| *Inventory - items* | Item former identifiers |
| *Inventory - items* | Item accession numbers |
| *Inventory - items* | Holdings UUID |
| *Users* | User UUIDs |
| *Users* | User Barcodes |
| *Users* | External IDs |
| *Users* | Usernames |


### Query

The **Query** function in the Bulk Edit app allows the user to build a query to identify records for bulk edit. The **Fields** available for building a query are based on the selected **Record type**. 


#### Fields by Record Type 

| Record type | Field | 
| :-----: | :-----: |
| *Inventory - holdings* | Effective library - Code |
| *Inventory - holdings* | Effective library - Name |
| *Inventory - holdings* | Effective location - Code |
| *Inventory - holdings* | Effective location - Name |
| *Inventory - holdings* | Holdings - Acquisition method |
| *Inventory - holdings* | Holdings - Acquisition order format |
| *Inventory - holdings* | Holdings - Acquisition receipt status |
| *Inventory - holdings* | Holdings - Call number |
| *Inventory - holdings* | Holdings - Call number prefix |
| *Inventory - holdings* | Holdings - Call number suffix |
| *Inventory - holdings* | Holdings - Copy number |
| *Inventory - holdings* | Holdings - Created date |
| *Inventory - holdings* | Holdings - Digitization policy |
| *Inventory - holdings* | Holdings - HRID |
| *Inventory - holdings* | Holdings - Instance UUID |
| *Inventory - holdings* | Holdings - Number of items |
| *Inventory - holdings* | Holdings - Record version |
| *Inventory - holdings* | Holdings - Retention policy |
| *Inventory - holdings* | Holdings - Shelving title |
| *Inventory - holdings* | Holdings - Statistical code names |
| *Inventory - holdings* | Holdings - Suppress from discovery |
| *Inventory - holdings* | Holdings - Updated date |
| *Inventory - holdings* | Holdings - UUID |
| *Inventory - holdings* | Permanent location - Code |
| *Inventory - holdings* | Permanent location - Name |
| *Inventory - holdings* | Temporary location - Code |
| *Inventory - holdings* | Temporary location - Name |
| *Inventory - instances* | Instance date type - Name |
| *Inventory - instances* | Instance status - Code |
| *Inventory - instances* | Instance status - Term |
| *Inventory - instances* | Instances - Cataloged date |
| *Inventory - instances* | Instances - Created date |
| *Inventory - instances* | Instances - Date 1 |
| *Inventory - instances* | Instances - Date 2 |
| *Inventory - instances* | Instances - Format names |
| *Inventory - instances* | Instances - Instance HRID |
| *Inventory - instances* | Instances - Instance UUID |
| *Inventory - instances* | Instances - Languages |
| *Inventory - instances* | Instances - Mode of issuance |
| *Inventory - instances* | Instances - Previously held |
| *Inventory - instances* | Instances - Record version |
| *Inventory - instances* | Instances - Resource title |
| *Inventory - instances* | Instances - Resource type |
| *Inventory - instances* | Instances - Source |
| *Inventory - instances* | Instances - Staff suppress |
| *Inventory - instances* | Instances - Statistical code names |
| *Inventory - instances* | Instances - Suppress from discovery |
| *Inventory - instances* | Instances - Updated date |
| *Inventory - items* | Effective call number - Type |
| *Inventory - items* | Effective location - Code |
| *Inventory - items* | Effective location - Name |
| *Inventory - items* | Holdings - Acquisition method |
| *Inventory - items* | Holdings - Acquisition order format |
| *Inventory - items* | Holdings - Acquisition receipt status |
| *Inventory - items* | Holdings - Call number |
| *Inventory - items* | Holdings - Call number prefix |
| *Inventory - items* | Holdings - Call number suffix |
| *Inventory - items* | Holdings - Copy number |
| *Inventory - items* | Holdings - Created date |
| *Inventory - items* | Holdings - Digitization policy |
| *Inventory - items* | Holdings - HRID |
| *Inventory - items* | Holdings - Instance UUID |
| *Inventory - items* | Holdings - Number of items |
| *Inventory - items* | Holdings - Record version |
| *Inventory - items* | Holdings - Retention policy |
| *Inventory - items* | Holdings - Shelving title |
| *Inventory - items* | Holdings - Suppress from discovery |
| *Inventory - items* | Holdings - Updated date |
| *Inventory - items* | Holdings - UUID |
| *Inventory - items* | Instances - Cataloged date |
| *Inventory - items* | Instances - Created date |
| *Inventory - items* | Instances - Date 1 |
| *Inventory - items* | Instances - Date 2 |
| *Inventory - items* | Instances - Format names |
| *Inventory - items* | Instances - Instance HRID |
| *Inventory - items* | Instances - Instance UUID|
| *Inventory - items* | Instances - Mode of issuance |
| *Inventory - items* | Instances - Previously held |
| *Inventory - items* | Instances - Record version |
| *Inventory - items* | Instances - Resource title |
| *Inventory - items* | Instances - Resource type |
| *Inventory - items* | Instances - Source |
| *Inventory - items* | Instances - Staff suppress |
| *Inventory - items* | Instances - Statistical code names |
| *Inventory - items* | Instances - Suppress from discovery |
| *Inventory - items* | Instances - Updated date |
| *Inventory - items* | Item call number - Type |
| *Inventory - items* | Items - Accession number |
| *Inventory - items* | Items - Barcode |
| *Inventory - items* | Items - Chronology |
| *Inventory - items* | Items - Copy number |
| *Inventory - items* | Items - Created date |
| *Inventory - items* | Items - Description of pieces |
| *Inventory - items* | Items - Effective call number |
| *Inventory - items* | Items - Effective shelving order |
| *Inventory - items* | Items - Enumeration |
| *Inventory - items* | Items - Item call number |
| *Inventory - items* | Items - Item HRID |
| *Inventory - items* | Items - Item UUID |
| *Inventory - items* | Items - Last check in date time |
| *Inventory - items* | Items - Number of missing pieces |
| *Inventory - items* | Items - Number of pieces |
| *Inventory - items* | Items - Purchase order line identifier |
| *Inventory - items* | Items - Statistical code |
| *Inventory - items* | Items - Status |
| *Inventory - items* | Items - Suppress from discovery |
| *Inventory - items* | Items - Updated date |
| *Inventory - items* | Items - Version |
| *Inventory - items* | Material type name |
| *Inventory - items* | Permanent location - Code |
| *Inventory - items* | Permanent location - Name |
| *Inventory - items* | Temporary location - Code |
| *Inventory - items* | Temporary location - Name |
| *Users* | Patron group - Name |
| *Users* | User - Active |
| *Users* | User - Barcode |
| *Users* | User - Created by User UUID |
| *Users* | User - Created date |
| *Users* | User - Custom field(s) |
| *Users* | User - Date of birth |
| *Users* | User - Department names |
| *Users* | User - Email |
| *Users* | User - Enrollment date |
| *Users* | User - Expiration date |
| *Users* | User - External system ID |
| *Users* | User - First name |
| *Users* | User - Last name |
| *Users* | User - Last name, first name |
| *Users* | User - Middle name |
| *Users* | User - Mobile phone |
| *Users* | User - Phone |
| *Users* | User - Preferred contact type |
| *Users* | User - Preferred first name |
| *Users* | User - Type |
| *Users* | User - Updated by user UUID |
| *Users* | User - Updated date |
| *Users* | User - User UUID |
| *Users* | User - Username|


#### Build a query to indentify records

To set criteria and identify records for bulk edit using the **Query** method: 

1. In the **Set Criteria** pane, click on the **Query** tab.
2. Select the **Record type**. The Bulk edit app allows changes to these **Record types**:
   
   - Inventory - holdings
   - Inventory - instances
   - Inventory - items
   - Users


3. Click the **Build query** button to open the **Build query** modal.
4. Select a **Field** from the *Select field* drop-down menu or filter the selection by typing the field in the *Filter options list* text box. The **Fields** available for selection are based on the **Record type**. See [Fields by Record Type](#fields-by-record-type) for more information.  

5. Select an **Operator** from the *Select operator* drop-down list. The **Operators** available for selection are based on the **Field**. 

| Operator | Meaning |
| :----- | :----- |
| *equals* | Field equals selected or input value. |
| *not equal to* | Field does not equal selected or input value. |
| *contains* | Field appears in selected or input value. |
| *starts with* | Field starts with selected or input value. |
| *is greater than* | Field is greater than the selected or input value. |
| *is less than* | Field is less than the selected or input value. |
| *is greater than or equal to* | Field is greater than or equal to the selected or input value. |
| *is less than or equal to* | Field is less than or equal to the selected or input value. |
| *is null/empty* | Field is blank; the field does not contain any data. |

6. Select a **Value** from the *Select value* drop-down list or type the value in the text box.  The values available for selection are based on the **Field** and **Operator**.
7. Click on the **+ icon** to add additional lines to the query or click on the **trash can icon** to delete a line from the query.
8. Once a query is built, it must be tested before the query can be run and saved. Click the **Test query** button to run the query and display a preview of matched records. The query string can be edited in the **Query string** field. If edited, another Test query must be done.
9. If the Test query is successful, click the **Run query** button to run the query and preview the matched records in the **Bulk edit query** modal.

### Preview matched records

If the **Identifier** method is used to identify records for bulk edit, the number of records matched and the filename display at the top of the **Bulk edit** modal. 

If the **Query** method is used to identify records for bulk edit, a **Test query** displays the query string and number of matched records at the top of the **Build query** modal. If the query is run, the **Query** and a preview of matched records display in the **Bulk edit query** modal. 

To add or remove **Field** columns in the preview pane:

1. Click the **Actions** button.
2. In the **Show columns** section of the Actions menu, check the box next to the name of the **Field** to include as a column heading in the preview.
3. Uncheck the box next to the name of the **Field** to remove the column from the preview.

### Download matched records

If desired, download the matched records as a .csv file:
   
1. In the **Preview** pane, click **Actions** and select **Download matched records (CSV)**.
2. Depending on the web browser settings, the .csv file may be opened and/or saved. 

### Download errors

If there are errors in the matched records, a message indicating the filename, number of entries, number of records matched, and number of errors displays in a two-column table in the **Errors** section. 

- **Record identifier.** The record identifier for the records that produced the error.
- **Reason for error.** The reason why the error was produced.

To download the list of errors as a .csv file:

1. In the **Preview** pane, select **Actions > Download errors (CSV)**.
2. Depending on the web browser settings, the .csv file may be opened and/or saved. 

## Bulk edit by record type

### Inventory - holdings

In the Bulk edit app, the **Fields** that can be changed in Holdings records include:

- **Administrative note**
- **Electronic access**
- **Holdings location**
- **Holdings notes**
- **Suppress from discovery**.

To identify **Inventory-holdings** records for bulk edit:

1. In the **Set criteria** pane, ensure **Record types** is set to **Inventory - holdings**.
2. [Identify holdings records for bulk edit](#identify-records-for-bulk-edit) by using the **Identifier** or **Query** method.
3. [Preview the list of matched holdings records](#preview-matched-records) in the **Preview of record matched** pane.
4. (Optional): [Download the matched holdings records](#download-matched-records) as a .csv file.
5. (Optional): [Download errors in matched holdings records](#download-errors) as a .csv file.

Once **Inventory-holdings** records are identified, you can start a bulk edit on the matching records. The **Options** and **Actions** available to perform the bulk edit vary for each **Field**. 


#### Administrative note

To bulk edit the **Administrative note** in the matched **Inventory-holdings** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, select **Administrative note** from the drop-down list.
3. Click **Actions** to select the action you want to apply from the drop-down list. The following **Actions** are available to bulk edit the **Administrative note** field:

| Actions | Data | Actions | Data |
| :-----: | :-----:| :-----: | :-----: |
| Add note | Text field | -| - |
| Change note type | Select note type | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search)  | Input text | Replace with | Input text |
| Find (full field search)  | Remove all | - | - | - |
   
4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will pop up with options of *Keep editing*, *Download preview*, or *Commit changes*.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. Click **Commit changes** to save the changes to the matched **Inventory-holdings** records.

#### Electronic access

To bulk edit the **Electronic access** in the matched **Inventory-holdings** records:

1. Click the **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the **Field** you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the holdings records. The following **Options** and **Actions** are available to bulk edit the **Electronic access** field in the matching **Inventory-holdings** records:

| Options | Actions | Data | Actions | Data |
| :-----:| :-----:| :-----:| :-----:| :-----:|
| *Electronic access - Link text* | Clear field | - | - | - |
| *Electronic access - Link text* | Find (full field search) | Input text | Remove | - |
| *Electronic access - Link text* | Find (full field search) | Input text | Replace with | Input text | 
| *Electronic access - Link text* | Replace with | Input text | - | - |
| *Electronic access - Materials specified* | Clear field | - | - | - |
| *Electronic access - Materials specified* | Find (full field search) | Input text | Remove | - | - |
| *Electronic access - Materials specified* | Find (full field search) | Input text | Replace with | Input text | 
| *Electronic access - Materials specified* | Replace with | Input text | - | - |
| *Electronic access - URI* | Clear field | - | - | - |
| *Electronic access - URI* | Find (full field search) | Input text | Remove | - | - |
| *Electronic access - URI* | Find (full field search) | Input text | Replace with | Input text |
| *Electronic access - URI* | Replace with | Input text | - | - |
| *Electronic access - URL public note* | Clear field | - | - | - |
| *Electronic access - URL public note* | Find (full field search) | Input text | Remove | - | - |
| *Electronic access - URL public note* | Find (full field search) | Input text | Replace with | Input text |
| *Electronic access - URL public note* | Replace with | Input text | - | - |
| *Electronic access - URL relationship* | Clear field | - | - | - |
| *Electronic access - URL relationship* | Find (full field search) | Input text | Remove | - | - |
| *Electronic access - URL relationship* | Find (full field search) | Input text | Replace with | Input text |
| *Electronic access - URL relationship* | Replace with | Input text | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will pop up with options of *Keep editing*, *Download preview*, or *Commit changes*.
   
   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device. Click **Commit changes** to save the changes to the matched holdings records. 


#### Holdings location

To bulk edit the **Holdings location** in the matched **Inventory-holdings** records:

1. Click the **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the **Field** you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the **Inventory-holdings** records. The following **Options** and **Actions** are available to bulk edit the **Holdings-location** field in the matching Holdings records:

| Options | Actions | Data | 
| :-----: | :-----: | :-----: | 
| *Holdings location - Permanent holdings location* | Replace with | Select location from drop-down or *Location lookup* | 
| *Holdings location - Temporary holdings location* | Clear field | - |
| *Holdings location - Temporary holdings location* | Replace with | Select location from drop-down or *Location lookup* | 

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.

     
8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device. 


#### Holdings notes

To bulk edit a **holdings note** in the matched **Inventory-holdings** records:

1. Click the **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the **Field** you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the holdings records. 

The following **Options** and **Actions** are available to bulk edit the **Holdings-notes** field in the matching Holdings records:

| Options | Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: | :-----: |
| *Holdings notes - Access restrictions* | Add note | Input text, *Staff only* check box | - | - |
| *Holdings notes - Access restrictions* | Change note type | Select note type | -| - |
| *Holdings notes - Access restrictions* | Find (full field search) | Input text | Remove | - |
| *Holdings notes - Access restrictions* | Find (full field search) | Input text | Replace with | Input text |
| *Holdings notes - Access restrictions* | Mark as staff only | - | - | - |
| *Holdings notes - Access restrictions* | Remove all | - | - | - |
| *Holdings notes - Access restrictions* | Remove mark as staff only | - | - | - |
| *Holdings notes - Binding* | Add note | Text field, *Staff only* check box | - | - |
| *Holdings notes - Binding* | Change note type | Select note type | - | - |
| *Holdings notes - Binding* | Find (full field search) | Input text | Remove | - |
| *Holdings notes - Binding* | Find (full field search) | Input text | Replace with | Input text |
| *Holdings notes - Binding* | Mark as staff only | - | - | - |
| *Holdings notes - Binding* | Remove all | - | - | - |
| *Holdings notes - Binding* | Remove mark as staff only | - | - | - |
| *Holdings notes - Copy note* | Add note | Input text, Staff only check box | - | - |
| *Holdings notes - Copy note* | Change note type | Select note type | - | - |
| *Holdings notes - Copy note* | Find (full field search) | Input text | Remove | - |
| *Holdings notes - Copy note* | Find (full field search) | Input text | Replace with | Input text |
| *Holdings notes - Copy note* | Mark as staff only | - | - | - |
| *Holdings notes - Copy note* | Remove all | - | - | - |
| *Holdings notes - Copy note* | Remove mark as staff only | - | - | - |
| *Holdings notes - Electronic bookplate* | Add note | Input text, *Staff only* check box | - | - |
| *Holdings notes - Electronic bookplate* | Change note type | Select note type | - | - |
| *Holdings notes - Electronic bookplate* | Find (full field search) | Input text | Remove | - |
| *Holdings notes - Electronic bookplate* | Find (full field search) | Input text | Replace with | Input text |
| *Holdings notes - Electronic bookplate* | Mark as staff only | - | - | - |
| *Holdings notes - Electronic bookplate* | Remove all | - | - | - |
| *Holdings notes - Electronic bookplate* | Remove mark as staff only | - | - | - |
| *Holdings notes - Note* | Add note | Input text, *Staff only* check box | - | - |
| *Holdings notes - Note* | Change note type | Select note type | - | - |
| *Holdings notes - Note* | Find (full field search) | Input text | Remove | - |
| *Holdings notes - Note* | Find (full field search) | Input text | Replace with | Input text |
| *Holdings notes - Note* | Mark as staff only | - | - | - |
| *Holdings notes - Note* | Remove all | - | - | - |
| *Holdings notes - Note* | Remove mark as staff only | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will pop up with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to save the changes to the matched holdings records.
     
8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


#### Suppress from discovery

To suppress the matched **Inventory-holdings** records from discovery in the Bulk edit app:

1. Click the **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the **Field** you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the Holdings records. The following **Actions** are available to bulk edit the **Suppress from discovery** field in the matching Holdings records:

   - Set false.
   - Set true.


4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click [*Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.

  
8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


### Inventory - instances

In the Bulk edit app, the **Fields** that can be changed in **Inventory-instance** records include:

- **Instances and Administrative data**
   - **Administrative note**
   - **Instance note**
   - **Staff suppress**
   - **Suppress from discovery**
- **Instances with source MARC (POC)**
   - **5xx fields**
   - **9xx fields**

#### Instances and Administrative data

**Administrative data**, **Instance notes**, **5XX**, and **9XX** fields in multiple **FOLIO Instance** and **MARC Instance** records can be changed simultaneously using  the Bulk edit app. For more information, see [FOLIO Instances - Editing Administrative Data and Instance Notes](https://folio-org.atlassian.net/wiki/x/AYAAIg) or [MARC Instances - Editing Administrative Data, 5XX and 9XX fields](https://folio-org.atlassian.net/wiki/x/AQABIg).  

##### Administrative note

To perform a bulk edit on the **Administrative note** field: 

1. Click **Actions \> Start bulk edit \> Instances and Administrative data**.
2. Under **Options**, click the drop-down list and select the **Field** you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the Instance records. The following **Actions** are available to bulk edit the **Administrative** field in the matching Instance records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: |
| Add note | Input text | - | - |
| Change note type | Select value | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Remove all | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

##### Instance note

To perform a bulk edit on the **Instance note** field:

1. Click **Actions \> Start bulk edit \> Instances and Administrative data**.
2. Under **Options**, select the **Instance note** from the drop-down list.
3. Click **Actions** to select the action you want to apply from the drop-down list. The following **Actions** are available to bulk edit the **Instance note** field in the matching Instance records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: |
| Add note | Input text | - | - |
| Change note type | Select value | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Mark as staff only | - | - | - |
| Remove all | - | - | - |
| Remove mark as staff only | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

##### Staff suppress

To suppress the matched **Inventory-instance** records from staff view:

1. Click **Actions \> Start bulk edit \> Instances and Administrative data**.
2. Under **Options**, select **Staff suppress** from the drop-down list.
3. Click **Actions** to select the action you want to apply from the drop-down list. The following **Actions** are available to bulk edit the **Staff suppress** option in the matching Instance records:

   - Set false.
   - Set true.

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

##### Suppress from discovery

To suppress the matched **Inventory-instance** records from discovery:

1. Click **Actions \> Start bulk edit \> Instances and Administrative data**.
2. Under **Options**, select **Staff suppress** from the drop-down list.
3. Click **Actions** to select the action you want to apply from the drop-down list. The following **Actions** are available to bulk edit the **Suppress from discovery** field in the matching Instance records:

   - Set false.
   - Set true.

     
4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. The selected action will be applied to the matched instance records. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


#### Instances with source MARC (POC)

To perform a bulk edit on the **5xx** or **9xx** fields in the matched **Inventory-instance** records:

1. Click **Actions \> Start bulk edit \> Instances with source MARC (POC)**.
2. Input the MARC field tag **only 5xx and 9xx supported**
3. Change **indicators 1 and 2** as required.
4. Indicate **subfield**
5. Click **Actions** to select the action you want to apply from the drop-down list. The following **Actions** are available to bulk edit the **5xx** or **9xx** fields in the matching Instance records:

| Field | ln. 1 | ln. 2| Subfield | Actions | Data | Actions | Data | 
| :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | 
| Input text | Input text | Input text | Add | Input text | - | - | - | 
| Input text | Input text | Input text | Add | Input text | Additional subfield | - | - |
| Input text | Input text | Input text | Find (entire subfield search) | Input text | Append | Input text | Input text | 
| Input text | Input text | Input text | Find (entire subfield search) | Input text | Remove field | - | - | 
| Input text | Input text | Input text | Find (entire subfield search) | Input text | Remove subfield | - | - | |
| Input text | Input text | Input text | Replace with | Input text | - | - | - | 

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. The selected action will be applied to the matched instance records. A new window will appear with a preview of the first 10 records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.

   - To return to the bulk edit, click **Keep editing**. The modal will close and you can continue editing.
   - To preview the entire list of records, click **Download preview**. A .csv file is downloaded to your local device.
   - Click **Commit changes** to apply the bulk edit changes to the matched holdings records. The modal closes and the message at the top of the **Bulk edit** pane displays the number of successfully changed records.


8. To download the list of changed records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


### Inventory - items

In the Bulk edit app, the **Fields** that can be changed in **Inventory-item** records include:

- **Administrative note**
- **Check in note**
- **Check out note**
- **Item notes**
- **Item status**
- **Loan type**
- **Location**
- **Suppress from discovery**

To identify **Inventory-item** records for bulk edit:

1. In the **Set criteria** pane, ensure **Record types** is set to **Inventory - items**.
2. [Identify item records for bulk edit](#identify-records-for-bulk-edit) by using the **Identifier** or **Query** method.
3. [Preview the list of matching item records](#preview-matched-records) in the **Preview of record matched** pane.
4. (Optional): [Download the matched item records](#download-matched-records) as a .csv file.
5. (Optional): [Download errors in the matched item records](#download-errors) as a .csv file.


#### Administrative note

To bulk edit the **Administrative note** in the matched **Inventory-items** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the field you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the Item records. The following **Actions** are available to bulk edit the **Administrative note** field in the matching Item records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: | 
| Add note | Input text | - | - |
| Change note type | Select value | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Remove all | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

#### Check in note

To bulk edit the **Check in note** in the matched item records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the field you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the Item records. The following **Actions** are available to bulk edit the **Check in note** field in the matching Item records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: | 
| Add note | Input text; *Staff only* checkbox | - | - |
| Change note type | Select value | - | - |
| Duplicate to | - | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Mark as staff only | - | - | - |
| Remove all | - | - | - |
| Remove mark as staff only | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


#### Check out note

To bulk edit the **Check out note** in the matched Item records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the field you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the item records. The following **Actions** are available to bulk edit the **Check out note** field in the matching Item records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: | 
| Add note | Input text; *Staff only* checkbox | - | - |
| Change note type | Select value | - | - |
| Duplicate to | - | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Mark as staff only | - | - | - |
| Remove all | - | - | - |
| Remove mark as staff only | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


#### Item notes

To bulk edit an **Item note** in the matched **Inventory-item** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the field you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the item records. The following **Actions** are available to bulk edit the **Item note** field in the matching **Item** records:

| Actions | Data | Actions | Data |
| :-----: | :-----: | :-----: | :-----: | 
| Add note | Input text; *Staff only* checkbox | - | - |
| Change note type | Select value | - | - |
| Duplicate to | - | - | - |
| Find (full field search) | Input text | Remove | - |
| Find (full field search) | Input text | Replace with | Input text |
| Mark as staff only | - | - | - |
| Remove all | - | - | - |
| Remove mark as staff only | - | - | - |

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.


#### Item status

To bulk edit the **item status** field in the matched **Inventory-item** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, select **Item status**.
3. Under **Actions**, *Replace with* is pre-selected and is the only action available for changing **Item status**.
4. Under **Data**, select a new **Item status** from the *Select item status* drop-down:

   - *Available*
   - *Missing*
   - *Withdrawn*
   - *In process*
   - *In process (non-requestable)*
   - *Intellectual item*
   - *Long missing*
   - *Restricted*
   - *Unavailable*
   - *Unknown*


5. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
6. To remove a field, click the **trash can icon** at the end of the row you want to remove.
7. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
8. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.

9. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

#### Loan type

To bulk edit the **Loan type** in the matched **Inventory-item** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, select **Loan type**.
3. Under **Actions**, select the action you want to apply to the item records. The following **Actions** are available to bulk edit the **Loan type** field in the matching Item records. Note that *Replace with* is preselected and is the only Action available for changing **Permanent loan type**.

| Options | Actions | Data |
| :-----: | :-----: | :----- |
| Permanent loan type | *Replace with* (pre-selected) | Select Loan type |
| Temporary loan type | Clear field | - |
| Temporary loan type | Replace with | Select Loan type |

**Loan types** are configured in Settings \> Inventory. See [Settings \> Inventory \> Loan types](../settings/settings_inventory/settings_inventory/#settings--inventory--loan-types) for more information. 

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

#### Location

To bulk edit the **Location** in the matched **Inventory-item** records:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, select the field you want to edit.
3. Under **Actions**, click **Select action** and select the action you want to apply to the item records. The following **Actions** are available to bulk edit the **Location** field in the matching **Inventory-item** records:

| Options | Actions | Data |
| :-----: | :-----: | :-----: |
| Permanent location | Clear field | - |
| Permanent location | Replace with | Select Location from drop-down or *Location lookup* |
| Temporary location | Clear field | - |
| Temporary location | Replace with | Select Location from drop-down or *Location lookup* |

**Locations** are configured in Settings \> Tenant. See [Settings \> Tenant \> Location setup](../settings/settings_tenant/settings_tenant/#settings--tenant--location-setup) for more information. 

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

#### Suppress from discovery

To suppress the matched **Inventory-item** records from discovery in the Bulk edit app:

1. Click **Actions \> Start bulk edit**.
2. Under **Options**, click the drop-down list and select the field you want to edit.
3. Under **Actions**, select the action you want to apply to the item records. The following **Actions** are available to bulk edit the **Suppress from discovery** field in the matching Item records:

   - Set false.
   - Set true.

4. To edit an additional field during the same bulk edit job, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.


8. To download the list of changed item records, click the **Actions** button at the top right of the pane. Select **Download changed records (CSV)**. The .csv file is downloaded to your local device.

### Users

In the Bulk edit app, it is possible to change any and all fields in multiple user records simultaneously, depending on which method is used to identify matching records.

- **Start bulk edit**: Allows editing of the **Email**, **Expiration date**, and the **Patron group** fields within the Bulk edit app. This approach is available in the **Identifier** and the **Query** methods.
- **Start bulk edit (Local)**: Allows editing of any and all fields of the matching user records by applying changes via an external .csv file uploaded to the Bulk edit app. This approach is available in the **Identifier** approach only. 

To identify **User** records for bulk edit:

1. In the **Set criteria** pane, ensure **Record types** is set to **Users**.
2. [Identify user records for bulk edit](#identify-records-for-bulk-edit) by using the **Identifier** or **Query** method.
3. [Preview the list of matching user records](#preview-matched-records) in the **Preview of record matched** pane. 
4. (Optional): [Download the matched user records](#download-matched-records) as a .csv file.
5. (Optional): [Download errors in matched user records](#download-errors) as a .csv file.

#### Start bulk edit

The **Start bulk edit** approach allows bulk edit to change the **Email**, **Expiration Date**, and **Patron Group** fields in matching user records. Bulk edit may be performed on each of these fields individually or simultaneously. The **Start bulk edit** approach is available in the **Identifier** and **Query** methods for identifying matching user records.

The **Options** and **Actions** available to perform bulk edit on matched **User records** depend on the selected **Field**.

1. Click **Actions > Start bulk edit**. 
2. Under **Options**, click the drop-down list and select the field you want to edit: **Email**, **Expiration date**, or **Patron group**. The **Actions** available for bulk edit are pre-selected based on the selected **Options**.
3. Under **Data**, input text in the text field or input date/select date from calendar picker as appropriate for the selected option. 

| Option | Action | Data | Action | Data |
| :-----: | :-----: | :-----: | :-----: | :-----: |
| **Email** | *Find* (pre-selected) | Input text | *Replace with* (pre-selected) | Input text |
| **Expiration date** | *Replace with* (pre-selected) | Input date | - | - |
| **Patron group** | *Replace with* (pre-selected) | Select value | - | - |

4. To edit an additional field, click the **+ sign** near the end of the row. Another row will appear under the existing row(s).
5. To remove a field, click the **trash can icon** at the end of the row you want to remove.
6. Click **Confirm changes**. A new window will appear with a preview of the first 10 item records to be changed.
7. The **Preview of records to be changed** will appear in the *Are you sure?* modal with options of **Keep editing**, **Download preview**, or **Commit changes**.
   
   - To return to the bulk edit, click **Keep editing**. The window will close and you can continue editing.
   - To preview the entire list of matched item records, click **Download preview**. A .csv file is downloaded to your local device.
   - To run the bulk edit and save changes to the matched item records, click **Commit changes**. The window closes and the banner at top of the **Bulk edit** pane displays the number of records successfully changed.

8. To change the column headings in the **Preview of record changed** table, click **Actions** and select or deselect the fields in the **Show columns** list as appropriate.
9. To download the list of changed user records, click **Actions > Download changed records (CSV)**. 


#### Start bulk edit (Local)

The **Start bulk edit (Local)** function allows the user to perform a bulk edit on user records edited locally (external to FOLIO) by uploading a .csv file of the changed, or edited, user records. Any and all fields in user records can be changed using the **Bulk edit (Local)** approach.

To perform bulk edit on user records using the **Start bulk edit (Local)** approach: 

1. After identifying user records, click **Actions \> Download matched records (CSV)** to download a .csv file of the matched user records; or select **Actions \> Download errors (CSV)** to download a .csv file of records that did not match your selected record identifier.
2. Edit the downloaded .csv file and make changes to the user records in the file itself. Save the edited .csv file to your computer.
3. Click **Actions \> Start bulk edit (Local)**.
4. In the **Bulk edit** window, **Drag and drop** the .csv file into the **Upload CSV file with edited records** box, or click **or choose file** to upload the .csv file from your computer. If the .csv file is uploaded successfully, the confirmation message, *(Name of File).csv successfully uploaded*, displays in a new window.
5. Click **Next**. The warning message, *(Number of) records will be updated if the **Commit changes** button is clicked.* appears in a new window.
6. Click **Commit changes**. Bulk edit will apply and save the local changes to the matched user records in FOLIO.

## Logs

The Bulk edit app allows users to preview **bulk edit logs** based on set criteria and download a .csv file associated with a bulk edit job. 

### Preview bulk edit logs

The options available for setting criteria include: **Statuses**, **Record types**, **Started**, **Ended**, and **User**.  

To set criteria and preview bulk edit logs:

1. Click on the **Logs** tab in the **Set criteria** pane.
2. Under the **Statuses** accordion, select the status for the bulk edit log by checking the appropriate box:  

   - **New**
   - **Retrieving records**
   - **Saving records**
   - **Data modification**
   - **Reviewing changes**
   - **Completed**
   - **Completed with errors**
   - **Failed**  


3. Under the **Record types** accordion, select the record type for the bulk edit log by checking the appropriate box: 

   - **Inventory - holdings**
   - **Inventory - instances**
   - **Inventory - items**
   - **Users**


4. In the **Started** accordion, use the **calendar icon** or type in the date using the YYYY-MM-DD format in the **From** and **To** fields to limit the preview by the start date of the bulk edit. Click **Apply**.
5. In the **Ended** accordion, use the **calendar icon** or type in the date using the YYYY-MM-DD format in the **From** and **To** fields to limit the preview by the end date of the bulk edit. Click **Apply**.
6. In the **Users** accordion, select the user, or FOLIO account, that ran the bulk edit job from the **Choose user** drop-down list.
7. A list of bulk edit logs displays in the **Bulk edit logs** pane. The number of bulk edit logs in the preview displays at the top of the pane as *(number of) records found*. The column headings display the following criteria for each bulk edit log: 

   - **Record type**: type of records changed in the bulk edit job
   - **Status**: status of the bulk edit job
   - **Editing**: method of bulk edit used
   - **# of records**: number of records retrieved for bulk edit job
   - **Processed**: number of records changed in bulk edit job
   - **Started**: start date and start time of bulk edit job
   - **Ended**: end date and end time of bulk edit job
   - **Run by**: user or FOLIO account used to run the bulk edit job
   - **ID**: system-generated number assigned to the bulk edit job

### Download a bulk edit log file

In the Bulk edit app, a file used to run a bulk edit job can be downloaded and saved from the **Bulk edit logs** pane. Bulk edit log files are available for download for 30 days after the bulk edit job is completed.

To download a file associated with a bulk edit log:

1. In the **Bulk edit logs** pane, click on the ellipses (...) in the **Actions** column next to the appropriate Bulk edit log.
2. Select the appropriate action from the **Download** drop-down list. The types of files available for download depend on the method used to identify records for bulk edit, the type of records changed, and/or the presence of errors during the matching or bulk edit process. 

   - **File that was used to trigger the bulk edit**
   - **File with identifiers of the records affected by bulk update**
   - **File with the preview of proposed changes**
   - **File with errors encountered during the record matching**
   - **File with updated records**
   - **File with errors encountered when committing the changes**.
   - **File with errors encountered during the record matching**

3. Depending on the web browser settings, the file can be opened and/or saved to your computer. 

