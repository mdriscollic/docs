---
title: "Lists"
linkTitle: "Lists"
date: 2025-01-22        
weight: 525
---
**This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may not be aligned with the current release of FOLIO.**

The Lists app provides actionable lists in FOLIO at the point of need. Some use cases include:


- Create a custom list when a report isn’t available in FOLIO;
- Create lists of records across apps and record types;
- Enable actions and workflows on a list of records;
- Access a set of pre-generated (canned) lists.
- Perform a cross-tenant query in ECS-enabled tenants. See [Cross-tenant queries: Definitions, Functionality, Limitations](https://docs.google.com/presentation/d/13LzVYXMvx8eWvRDcqHk5hXTLP-tGJIGL/edit#slide=id.p5) for more information about **Cross-tenant queries**.


Functionality of the Lists app includes:


* Lists persist, can be refreshed and edited;
* List data updated in near real-time;
* User-friendly process for building a query to create a list;
* Duplication of lists;
* Export records from a list as a .csv file;
* Each list can include up to 1.25 million records.


Definition of terms related to the Lists app:


- **Record set**: The set (or list) of records retrieved through a query.
- **Operator**: The function applied in a query to match records by selected field and inputted value. 
- **Value**: The text and/or number(s) input to query records with a selected field and selected operator.
- **Field**: The identifier used to query records.
- **Query**: The search string used to generate a list that includes a field, operator, and value.
- **Source**: The FOLIO account used to create and save a list.
- **FQM**: FOLIO Query Machine. The query functionality in FOLIO.
- **Content permissions**. GET permissions that limit access to record types in Lists app (and FQM) based on the user’s assigned permissions to view record types in FOLIO.


## Permissions


**Lists app permissions** and **Content permissions** are applied together to determine a user’s access to the Lists app. See [Determining access in Lists app](https://folio-org.atlassian.net/wiki/spaces/FOLIOtips/pages/572948576/Lists+App+permissions+-#Determining-access-in-Lists-app) for more information.


The permissions listed below allow a user to interact with the Lists app and determine what the user can and cannot do within the app. If none of these permissions are assigned to a user, they are unable to see the Lists app or any related information. For more information on permissions, see [Platform Essentials \> Permissions](../platform-essentials/permissions/).


The following are the permissions for the Lists app:


- **Lists (Enable): Can view Lists**. This permission allows a user to view **Lists** and **List details**.
- **Lists (Edit): Can create, edit, and refresh lists**. This permission allows a user to view, create, edit, and refresh lists.
- **Lists (Export): Can create, edit, refresh, and export lists**. This permission allows a user to view, create, edit, refresh, and export lists.
- **Lists (Delete): Can create, edit, refresh, and delete lists**. This permission allows a user to view, create, edit, refresh, and delete lists. 
- **Lists (Admin): All permissions**. This permission allows a user to view, edit, refresh, export, and delete lists.

### Content permissions

**Content permissions** are GET permissions that limit access to Record types in Lists app (and FQM) based on the user’s assigned permission(s) to view record types in FOLIO. Content permissions ensure that sensitive and confidential data are available only to library staff who must have access to it. 

For a list of **Content permissions** by Record type, see [Lists app permissions: Content permissions](https://folio-org.atlassian.net/wiki/spaces/FOLIOtips/pages/572948576/Lists+App+permissions+-#Content-permissions). 


## Supported fields by record type

In the Lists app, the **Fields** available for building a query and displaying as column headings depend on the selected **Record type** of the list. See the appropriate table for more information about supported fields by record type:

- [Holdings](#holdings)
- [Instances](#instances)
- [Items](#items)
- [Loans](#loans)
- [Organizations](#organizations)
- [Purchase order lines](#purchase-order-lines)
- [Users](#users) 


### Holdings

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? |
| :----- | :-----: | :-----: | 
| *Effective library - Code* | YES | YES |
| *Effective library - Name* | YES | YES |
| *Effective location - Code* | YES | YES |
| *Effective location - Name* | YES | YES |
| *Holdings - Acquisition method* | YES | YES |
| *Holdings - Acquisition order format* | YES | YES |
| *Holdings - Acquisition receipt status* | YES | YES |
| *Holdings - Administrative notes* | NO |YES |
| *Holdings - Call number* | YES | YES |
| *Holdings - Call number prefix* | YES | YES |
| *Holdings - Call number suffix* | YES | YES |
| *Holdings - Copy number* | YES | YES |
| *Holdings - Created date* | YES | YES |
| *Holdings - Digitization policy* | YES | YES |
| *Holdings - Electronic access* | NO |YES |
| *Holdings - Former IDs* | NO |YES |
| *Holdings - HRID* | NO |YES |
| *Holdings - Instance UUID* | YES | YES |
| *Holdings - Number of items* | YES | YES |
| *Holdings - Record version* | YES | YES |
| *Holdings - Retention policy* | YES | YES |
| *Holdings - Shelving title* | YES | YES |
| *Holdings - Statements* | NO |YES |
| *Holdings - Statements for indexes* | NO |YES |
| *Holdings - Statements for supplements* | NO |YES |
| *Holdings - Statistical code names* | YES | YES |
| *Holdings - Statistical code UUIDs* | NO |YES |
| *Holdings - Tags* | NO |YES |
| *Holdings - Updated date* | YES | YES |
| *Holdings - UUID* | YES | YES |
| *Permanent location - Code* | YES | YES |
| *Permanent location - Name* | YES | YES |
| *Temporary location - Code* | YES | YES |
| *Temporary location - Name* | YES | YES |


### Instances

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----: | :-----: |
| *Instance - Administrative notes* | NO | YES |
| *Instance - Alternative titles* | NO | YES |
| *Instance - Cataloged date* | YES | YES |
| *Instance - Classifications* | NO | YES |
| *Instance - Contributors* | NO | YES |
| *Instance - Created date* | YES | YES |
| *Instance - Date 1* | YES | YES |
| *Instance - Date 2* | YES | YES |
| *Instance - Editions* | NO | YES |
| *Instance - Electronic access* | NO | YES |
| *Instance - Format names* | YES | YES |
| *Instance - Identifiers* | NO | YES |
| *Instance - Instance HRID* | YES | YES |
| *Instance - Instance UUID* | YES | YES |
| *Instance - Languages* | YES | YES |
| *Instance - Mode of issuance* | YES | YES |
| *Instance - Notes* | NO | YES |
| *Instance - Physical descriptions* | NO | YES |
| *Instance - Previously held* | YES | YES |
| *Instance - Primary contributor* | NO | YES |
| *Instance - Publication* | NO | YES |
| *Instance - Publication range* | NO | YES |
| *Instance - Series* | NO | YES |
| *Instance - Source* | YES | YES |
| *Instance - Statistical code names* | YES | YES |
| *Instance - Statistical code UUIDs* | NO | YES |
| *Instance - Subject headings* | NO | YES |
| *Instance - Suppress from discovery* | YES | YES |
| *Instance - Tags* | NO | YES |
| *Instance - Updated date* | YES | YES |
| *Instance date type - Name* | YES | YES |
| *Instance status - Code* | YES | YES |
| *Instance status - Term* | YES | YES |


### Items

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----:| :-----:| 
| *Effective library - Code* | YES | YES |
| *Effective library - Name* | YES | YES |
| *Effective location - Code* | YES | YES |
| *Effective location - Name* | YES | YES |
| *Holdings - Acquisition method* | YES | YES |
| *Holdings - Acquisition order format* | YES | YES |
| *Holdings - Acquisition receipt status* | YES | YES |
| *Holdings - Administrative notes* | NO |YES |
| *Holdings - Call number* | YES | YES |
| *Holdings - Call number prefix* | YES | YES |
| *Holdings - Call number suffix* | YES | YES |
| *Holdings - Copy number* | YES | YES |
| *Holdings - Created date* | YES | YES |
| *Holdings - Digitization policy* | YES | YES |
| *Holdings - Electronic access* | NO |YES |
| *Holdings - Former IDs* | NO |YES |
| *Holdings - HRID* | NO |YES |
| *Holdings - Instance UUID* | YES | YES |
| *Holdings - Number of items* | YES | YES |
| *Holdings - Record version* | YES | YES |
| *Holdings - Retention policy* | YES | YES |
| *Holdings - Shelving title* | YES | YES |
| *Holdings - Statements* | NO |YES |
| *Holdings - Statements for indexes* | NO |YES |
| *Holdings - Statements for supplements* | NO |YES |
| *Holdings - Statistical code names* | YES | YES |
| *Holdings - Statistical code UUIDs* | NO |YES |
| *Holdings - Tags* | NO |YES |
| *Holdings - Updated date* | YES | YES |
| *Holdings - UUID* | YES | YES |
| *Permanent location - Code* | YES | YES |
| *Permanent location - Name* | YES | YES |
| *Temporary location - Code* | YES | YES |
| *Temporary location - Name* | YES | YES |
| *Instances - Administrative notes* | NO | YES |
| *Instances - Alternative titles* | NO | YES |
| *Instances - Cataloged date* | YES | YES |
| *Instances - Classifications* | NO | YES |
| *Instances - Contributors* | NO | YES |
| *Instances - Created date* | YES | YES |
| *Instances - Date 1* | YES | YES |
| *Instances - Date 2* | YES | YES |
| *Instances - Editions* | NO | YES |
| *Instances - Electronic access* | NO | YES |
| *Instances - Format names* | YES | YES |
| *Instances - Identifiers* | NO | YES |
| *Instances - Instance HRID* | YES | YES |
| *Instances - Instance UUID* | YES | YES |
| *Instances - Languages* | YES | YES |
| *Instances - Mode of issuance* | YES | YES |
| *Instances - Notes* | NO | YES |
| *Instances - Physical descriptions* | NO | YES |
| *Instances - Previously held* | YES | YES |
| *Instances - Primary contributor* | NO | YES |
| *Instances - Publication* | NO | YES |
| *Instances - Publication range* | NO | YES |
| *Instances - Series* | NO | YES |
| *Instances - Source* | YES | YES |
| *Instances - Statistical code names* | YES | YES |
| *Instances - Statistical code UUIDs* | NO | YES |
| *Instances - Subject headings* | NO | YES |
| *Instances - Suppress from discovery* | YES | YES |
| *Instances - Tags* | NO | YES |
| *Instances - Updated date* | YES | YES |
| *Item call number - Type* | YES | YES |
| *Items - Accession number* | YES | YES |
| *Items - Administrative notes* | NO | YES |
| *Items - Barcode* | YES | YES |
| *Items - Chronology* | YES | YES |
| *Items - Copy number* | YES | YES |
| *Items - Created date* | YES | YES |
| *Items - Description of pieces* | YES | YES |
| *Items - Effective call number* | YES | YES |
| *Items - Effective shelving order* | YES | YES |
| *Items - Electronic access* | NO | YES |
| *Items - Item call number* | YES | YES |
| *Items - Item HRID* | YES | YES |
| *Items - Item UUID* | YES | YES |
| *Items - Last check in date time* | YES | YES |
| *Items - Number of missing pieces* | YES | YES |
| *Items - Number of pieces* | YES | YES |
| *Items - Purchase order line identifier* | YES | YES |
| *Items - Statistical code* | YES | YES |
| *Items - Suppress from discovery* | YES | YES |
| *Items - Tag list* | NO | YES |
| *Items - Updated date* | YES | YES |
| *Items - Version* | YES | YES |
| *Material type - Name* | YES | YES |
| *Permanent location - Code* | YES | YES |
| *Permanent location - Name* | YES | YES |
| *Temporary location - Code* | YES | YES |
| *Temporary location - Name* | YES | YES |


### Loans

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----: | :-----: | 
| *Check in service point - Code* | YES | YES |
| *Check in service point - Discovery display name* | YES | YES |
| *Check in service point - Name* | YES | YES |
| *Check out service point - Code* | YES | YES |
| *Check out service point - Discovery display name* | YES | YES |
| *Check out service point - Name* | YES | YES |
| *Holdings - Acquisition method* | YES | YES |
| *Holdings - Acquisition order format* | YES | YES |
| *Holdings - Acquisition receipt status* | YES | YES |
| *Holdings - Administrative notes* | NO |YES |
| *Holdings - Call number* | YES | YES |
| *Holdings - Call number prefix* | YES | YES |
| *Holdings - Call number suffix* | YES | YES |
| *Holdings - Copy number* | YES | YES |
| *Holdings - Created date* | YES | YES |
| *Holdings - Digitization policy* | YES | YES |
| *Holdings - Electronic access* | NO |YES |
| *Holdings - Former IDs* | NO |YES |
| *Holdings - HRID* | NO |YES |
| *Holdings - Instance UUID* | YES | YES |
| *Holdings - Number of items* | YES | YES |
| *Holdings - Record version* | YES | YES |
| *Holdings - Retention policy* | YES | YES |
| *Holdings - Shelving title* | YES | YES |
| *Holdings - Statements* | NO |YES |
| *Holdings - Statements for indexes* | NO |YES |
| *Holdings - Statements for supplements* | NO |YES |
| *Holdings - Statistical code names* | YES | YES |
| *Holdings - Statistical code UUIDs* | NO |YES |
| *Holdings - Tags* | NO |YES |
| *Holdings - Updated date* | YES | YES |
| *Holdings - UUID* | YES | YES |
| *Instances - Administrative notes* | NO | YES |
| *Instances - Alternative titles* | NO | YES |
| *Instances - Cataloged date* | YES | YES |
| *Instances - Classifications* | NO | YES |
| *Instances - Contributors* | NO | YES |
| *Instances - Created date* | YES | YES |
| *Instances - Date 1* | YES | YES |
| *Instances - Date 2* | YES | YES |
| *Instances - Editions* | NO | YES |
| *Instances - Electronic access* | NO | YES |
| *Instances - Format names* | YES | YES |
| *Instances - Identifiers* | NO | YES |
| *Instances - Instance HRID* | YES | YES |
| *Instances - Instance UUID* | YES | YES |
| *Instances - Languages* | YES | YES |
| *Instances - Mode of issuance* | YES | YES |
| *Instances - Notes* | NO | YES |
| *Instances - Physical descriptions* | NO | YES |
| *Instances - Previously held* | YES | YES |
| *Instances - Primary contributor* | NO | YES |
| *Instances - Publication* | NO | YES |
| *Instances - Publication range* | NO | YES |
| *Instances - Series* | NO | YES |
| *Instances - Source* | YES | YES |
| *Instances - Statistical code names* | YES | YES |
| *Instances - Statistical code UUIDs* | NO | YES |
| *Instances - Subject headings* | NO | YES |
| *Instances - Suppress from discovery* | YES | YES |
| *Instances - Tags* | NO | YES |
| *Instances - Updated date* | YES | YES |
| *Item - Accession number* | YES | YES |
| *Item - Administrative notes* | NO | YES |
| *Item - Barcode* | YES | YES |
| *Item - Chronology* | YES | YES |
| *Item - Copy number* | YES | YES |
| *Item - Created date* | YES | YES |
| *Item - Description of pieces* | YES | YES |
| *Item - Effective call number* | YES | YES |
| *Item - Effective shelving order* | YES | YES |
| *Item - Electronic access* | NO | YES |
| *Item - Item call number* | YES | YES |
| *Item - Item HRID* | YES | YES |
| *Item - Item UUID* | YES | YES |
| *Item - Last check in date time* | YES | YES |
| *Item - Number of missing pieces* | YES | YES |
| *Item - Number of pieces* | YES | YES |
| *Item - Purchase order line identifier* | YES | YES |
| *Item - Statistical code* | YES | YES |
| *Item - Suppress from discovery* | YES | YES |
| *Item - Tag list* | NO | YES |
| *Item - Updated date* | YES | YES |
| *Item - Version* | YES | YES |
| *Loan - Action* | YES | YES |
| *Loan - Checkout date* |YES | YES |
| *Loan - Claimed returned date* |YES | YES |
| *Loan - Created at* | YES | YES |
| *Loan - Declared lost date* | YES | YES |
| *Loan - Due date* | YES | YES |
| *Loan - Due date changed by recall* | YES | YES |
| *Loan - Renewal count* | YES | YES |
| *Loan - Return date* | YES | YES |
| *Loan - Status name* | YES | YES |
| *Loan - UUID* | YES | YES |
| *Loan policy - Name* | YES | YES |
| *Loan policy - UUID* | NO | YES |
| *Material type - Name* | YES | YES |
| *Patron group - Name* | YES | YES |
| *User - Active* | YES | YES |
| *User - Barcode* | YES | YES |
| *User - Expiration date* | YES | YES |
| *User - Last name, first name* | YES | YES |
| *User - UUID* | YES | YES |


### Organizations

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----: | :-----: |
| *Access provider* | YES | YES |
| *Accounting code* | YES | YES |
| *Accounts* | NO | YES |
| *Acquisition unit names* | YES | YES |
| *Addresses* | NO | YES |
| *Agreements* | NO | YES |
| *Aliases* | NO | YES |
| *Changelogs* | NO | YES |
| *Claiming interval* | YES | YES |
| *Code* | YES | YES |
| *Created at* | YES | YES |
| *Description* | YES | YES |
| *Discount percent* | YES | YES |
| *EDI job scheduled enabled* | YES | YES |
| *EDI notes* | YES | YES |
| *EDI organization code* | YES | YES |
| *EDI organization type* | YES | YES |
| *EDI vendor code* | YES | YES |
| *EDI vendor type* | YES | YES |
| *Email* | NO | YES |
| *Expected activation interval* | YES | YES |
| *Expected invoice interval* | YES | YES |
| *Expected receipt interval* | YES | YES |
| *Export to accounting* | YES | YES |
| *Governmental* | YES | YES |
| *Is donor* | YES | YES |
| *Is vendor* | YES | YES |
| *Language* | YES | YES |
| *Liable for VAT* | YES | YES |
| *Licensor* | YES | YES |
| *Material supplier* | YES | YES |
| *Name* | YES | YES |
| *Payment method* | YES | YES |
| *Renewal activation interval* | YES | YES |
| *SAN code* | YES | YES |
| *Status* | YES | YES |
| *Subscription interval* | YES | YES |
| *Tax ID* | YES | YES |
| *Tax percentage* | YES | YES |
| *Type names* | YES | YES |
| *Type UUIDs* | NO | YES |
| *Updated at* | YES | YES |
| *URLs* | NO | YES |
| *UUID* | NO | YES |
| *Vendor currencies* | NO | YES |


### Purchase order lines

| Field name in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----: | :-----: | 
| *Exchange rate - Currency* | YES | YES |
| *Exchange rate - Rate* | YES | YES |
| *PO - Acquisition unit names* | YES | YES |
| *PO - Acquisition unit UUIDs* | NO | YES |
| *PO - Approved* | YES | YES |
| *PO - Created at* | YES | YES |
| *PO - Order type* | YES | YES |
| *PO - PO number* | YES | YES |
| *PO - Re-encumber* | YES | YES |
| *PO - Tags tag list* | NO | YES |
| *PO - Updated at* | YES | YES |
| *PO - Workflow status* | YES | YES |
| *PO assigned to user - Email* | YES | YES |
| *PO assigned to user - Last name, first name* | YES | YES |
| *PO assigned to user - Username* | YES | YES |
| *PO created by user - Email* | YES | YES |
| *PO created by user - Last name, first name* | YES | YES |
| *PO created by user - Username* | YES | YES |
| *PO updated by user - Email* | YES | YES |
| *PO updated by user - Last name, first name* | YES | YES |
| *PO updated by user - Username* | YES | YES |
| *POL - Agreement UUID* | YES | YES |
| *POL - Cost currency* | YES | YES |
| *POL - Cost exchange rate* | YES | YES |
| *POL - Cost PO line estimated price* | YES | YES |
| *POL - Created at* | YES | YES |
| *POL - Description* | YES | YES |
| *POL - Details receiving note* | YES | YES |
| *POL - Donor* | YES | YES |
| *POL - E-resource create inventory* | YES | YES |
| *POL - E-resources expected activation* | YES | YES |
| *POL - E-resource is activated* | YES | YES |
| *POL - E-resource is trial* | YES | YES |
| *POL - E-resource resource URL* | YES | YES |
| *POL - Is rush* | YES | YES |
| *POL - Order format* | YES | YES |
| *POL - Payment status* | YES | YES |
| *POL - Physical expected receipt date* | YES | YES |
| *POL - PO line number* | YES | YES |
| *POL - Publication date* | YES | YES |
| *POL - Publisher* | YES | YES |
| *POL - Receipt date* | YES | YES |
| *POL - Receipt status* | YES | YES |
| *POL - Selector* | YES | YES |
| *POL - Source* | YES | YES |
| *POL - Tags* | NO | YES |
| *POL - Title or package* | YES | YES |
| *POL - Updated at* | YES | YES |
| *POL - UUID* | YES | YES |
| *POL created by user - Email* | YES | YES |
| *POL created by user - Last name, first name* | YES | YES |
| *POL created by user - Username* | YES | YES |
| *POL exchange rate* | YES | YES |
| *POL updated by user - Email* | YES | YES |
| *POL updated by user - Last name, first name* | YES | YES |
| *POL updated by user - Username* | YES | YES |
| *Vendor org - Code* | YES | YES |
| *Vendor org - EDI vendor code* | YES | YES |
| *Vendor org - EDI vendor type* | YES | YES |
| *Vendor org - Is donor* | YES | YES |
| *Vendor org - Is vendor* | YES | YES |
| *Vendor org - Name* | YES | YES |
| *Vendor org - Status* | YES | YES |
| *Vendor org - UUID* | NO | YES 


### Users

| *Field name* in Lists app | Can use to build query in UI? | Option to show as column heading in UI? | 
| :----- | :-----: | :-----: | 
| *Patron group - Name* | YES | YES |
| *User - Active* | YES | YES |
| *User - Address* | NO | YES |
| *User - Barcode* | YES | YES |
| *User - Created by user UUID* | YES | YES |
| *User - Created date* | YES | YES |
| *User - Date of birth* | YES | YES |
| *User - Department names* | YES | YES |
| *User - Department UUIDs* | NO | YES |
| *User - Email* | YES | YES |
| *User - Enrollment date* | YES | YES |
| *User - Expiration date* | YES | YES |
| *User - External system ID* | YES | YES |
| *User - First name* | YES | YES |
| *User - Last name* | YES | YES |
| *User - Last name, first name* | YES | YES |
| *User - Middle name* | YES | YES |
| *User - Mobile phone* | YES | YES |
| *User - Phone* | YES | YES |
| *User - Preferred contact type* | YES | YES |
| *User - Preferred first name* | YES | YES |
| *User - Proxy for* | NO | YES |
| *User - Tags tag list* | NO | YES |
| *User - Type* | YES | YES |
| *User - Updated by user UUID* | YES | YES |
| *User - Updated date* | YES | YES |
| *User - User created date* | YES | YES |
| *User - User updated date* | YES | YES |
| *User - User UUID* | YES | YES |
| *User - Username* | YES | YES |


## View a list


To view a list, open the Lists app. A list of Lists is displayed in the **Lists** pane. Select a list to view by highlighting and clicking on it. The selected list opens in a new window.


### Filters


The selection of lists in the **Lists** pane can be narrowed by applying filters. The following filters are available: 


- **Status**
  - **Active**. An active list contains a query and a resulting record set. 
  - **Inactive**. An inactive list contains a query but no record set.

- **Visibility**
  - **Shared:**. Shared lists can be accessed by all users with permissions to the Lists app in this organization. 
  - **Private**. Private lists can only be accessed by the user logged in.

- **Record Types**
  - **Holdings**. Record set includes holdings records.
  - **Instance**: Record set includes instance records.
  - **Items**: Record set includes item records. 
  - **Loans**: Record set includes loans.
  - **Organizations**: Record set includes organization information, such as contact information and agreements.
  - **Purchase order lines**: Record set includes information about purchase order lines (POLs).
  - **Users**: Record set includes user records.


### List information 


The **List information** section displays details about the list. 


- **Source**: Username or FOLIO account used to create and update the list.
- **List name**: Title of the list
- **Description**: A description of the list. This criteria is optional.
- **Visibility**: **Shared** or **Private**.  
- **Status**: **Active** or **Inactive**


### Query 


The **Query** section of the list displays the query string used to retrieve the record set. It also displays the number of records in the record set and a preview of the first 100 records in the record set.


### Field headings


In a list, the fields for the record set display as column headings. Customize the display of column headings in the record set by checking or unchecking the field(s) in **Actions \> Show columns** as appropriate. 


To view the refreshed list, click **Actions \> Refresh List** and click the **View updated list** link in the confirmation message.


## Create a list


A new list must have **List information** and a **Query** assigned to establish the record set for the list. A **Test query** must be performed before the query can be run and saved. 


### List information


To add list details for a new list:

1. In the Lists pane, click on **New**. 
2. In the **New List** modal, add the **List name**, **Description**, **Visibility**, and **Status** criteria in the **List information** section.
3. Select the appropriate **Record type** for the list: **Holdings**, **Instances**, **Items**, **Loans**, **Organizations**, **Purchase order lines**, and **Users**.
4. Select the appropriate **Visibility** setting for the list: *Shared* or *Private*.
5. Select the appropriate **Status** setting for the list: *Active* or *Inactive*.


### Build a query


The **Build query** function in the Lists app allows the user to build a query for these record types: **Holdings**, **Instances**, **Items**, **Loans**, **Organizations**, **Purchase order lines**, and **Users**. The query string populates in the **Query** field as the query is built. 


To set criteria and build a query for new list, follow these steps: 


1. Click the **Build query** button to open the **Build query** window. 
2. Select the **Record type** for the query. 
3. Select a **Field** from the **Filter options list** drop-down menu. The **Fields** available for selection are based on the **Record Type**. See [Supported fields by List record type](https://folio-org.atlassian.net/wiki/spaces/FOLIOtips/pages/264831080/Supported+fields+by+List+record+type+Lists+app) for more information. 

4. Select an **Operator** from the **Select operator** drop-down list. The operators available for selection are based on the selected **Field**. 

| Operator | Meaning |
| :----- | :----- |
| *equals* | Field equals the selected Value. |
| *not equal to* | Field does not equal the selected Value. |
| *contains* | Field appears in the selected Value. |
| *starts with* | Field starts with selected Value. |
| *Is null/empty* | Field is empty; the Field contains no data.|
    

5. Select a **Value** from the **Select value** drop-down list. The **Values** available for selection are based on the **Record Type** and **Field**.
6. Click on the **+ icon** to add additional lines to the query; Click on the **trash can icon** to delete a line from the query. 
7. **Test query** is required whenever building a query for a new list. Click the **Test query** button to test the query. The total number of records retrieved and a preview of the first 100 records in the record set displays.
8. Click **Run query & save**. If saved successfully, a *(Name of List) saved successfully* message appears momentarily. Once the query is completed, a *Refresh complete with (number of) records: View updated list* displays at the top of the window.
9. Click the **View updated list** link in the confirmation message to view the record set in the list.
10. In a list, the fields of the record type display as column headings. The default display of column headings is based on the record type assigned to the list. Customize the display of column headings in the record set by checking or unchecking the field(s) in **Actions \> Show columns** as appropriate for the selected record type. See [Supported fields by List record type (Lists app)](https://folio-org.atlassian.net/wiki/x/aADJDw) for a list of column heading options.


## Update a record set in a list


The record set in a list is static, but the metadata of each record is updated in near real-time. If modification is made to a record outside of the Lists app, the record remains in the record set of the list. The updated record can be viewed by refreshing the list.


To refresh or update the record set in a list:


1. Click **Actions \> Refresh list**. The system will re-run the query. A *Refresh complete with (number of) records* confirmation message appears at the top of the screen. 
2. Click the **View updated list** link in the confirmation message to view the updated record set in the list. 


## Edit a list


To edit the **List information** in a list: 


1. Select the list in the **Lists** pane. The list opens a new window.
2. Click **Actions \> Edit List**. 
3. In the **List information** section, edit the **List name**, **Description**, **Visibility**, and/or **Status** fields as appropriate.
4. Click **Save**. A *List _ListTitle_ was saved* confirmation message will appear in the lower right corner of the screen. 


To edit the **Query** in a list, follow these steps: 


1. Select the list in the **Lists** pane. The list opens a new window.
2. Click **Actions \> Edit List**. 
3. Open the **Query** accordion, if necessary, and click **Edit query**. Make changes to **Field**, **Operator**, and/or **Value** as appropriate. The **Query** field displays a preview of the query as it is edited.
4. If necessary, click on the **+ icon** to add additional rows to the query or click on the **trash can icon** to delete rows from the query. 
5. **Test query** is required whenever editing a query in an existing list. Click the **Test query** button to test the query. The total number of records retrieved and a preview of the first 100 records in the record set displays.
6. Click the **Run query & save** button. A confirmation message, *List _ListTitle_ was saved* will appear in the lower right corner of the screen. 


## Duplicate a list

To duplicate a list:

1. Select the list from the **Lists** pane. The selected list will open in a new window. 
2. Click **Actions \> Duplicate List**. If duplicating the list without making any changes, click **Save.** A confirmation message, *List (Original List Name) - copy was saved* appears in the lower right corner of the screen. 
3. Edit the **List name**, **Description** (optional), or change **Visibility** and **Status**,  if appropriate. 
4. Edit the query, if appropriate, by clicking the **Edit query** button.
5. Make changes to **Field**, **Operator**, and/or **Value**. The **Query** field displays a preview of the query string as it is edited. If necessary, click on the **+ icon** to add additional rows to the query; click on the **trash can icon** to delete rows from the query. 
6. Click the **Test query** button to see how many records are returned and to preview the record set of the list. Test query is required when editing the query of a list before the new query can be run and saved. 
7. Click the **Run query & save** button. A confirmation message, *List _DuplicateListName_) was saved* will appear in the lower right corner of the screen. 

## Delete a list


To delete a list: 


1. Select the list from the **Lists** pane. The selected list will open in a new window. 
2. Click **Actions \> Delete List**. 
3. A confirmation modal appears: *Are you sure you want to delete the list _ListTitle_?*
4. Click the **Delete** button to delete the list.


## Export a list 


A list can be exported from the Lists app and downloaded as a .csv file. To export a list: 


1. Select the list from the **Lists** pane. The selected list will open in a new window.  
2. Click the **Actions** button. Select or deselect the column headings to display in your exported file. 
3. Click **Actions \> Export list (CSV)** to download the list as a .csv file. When successfully completed, an *Exported list …* confirmation message appears in the bottom right corner of the screen. 
4. Depending on your browser settings, the exported list may be automatically saved in your Downloads folder.
