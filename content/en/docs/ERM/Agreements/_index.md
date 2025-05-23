---
title: "Agreements"
linkTitle: "Agreements"
date: 2024-06-27
weight: 10
tags: ["parenttopic"]
---

The Agreements app allows you to create and manage your library’s agreements. The agreements you create here can link to licenses in the Licenses app.

Definition of terms related to the Agreements app:


*   **Agreement.** An agreement is a place where you can manage the content your library can access (based on resources described in a knowledge base) and link that content to licensing and acquisitions information.
*   **External knowledge base.** A knowledge base (see definition in this list) that is outside of the FOLIO system. For example, the EBSCO knowledge base.
*   **Internal knowledge base.** Managing your library’s knowledge base from within FOLIO.
*   **Knowledge base (KB).** A knowledge base is an extensive database maintained by a knowledge base supplier that contains information about electronic resources such as title lists and coverage dates, etc. Knowledge bases typically organize the resources provided by a content provider into collections or databases that reflect specific content provider offerings, for example packages of e-journals, e-books, or other materials.
*   **License.** A license explains what you can do with the content your library can access. The license is the contract or Terms of Use.

Library’s utilizing FOLIO can employ an external knowledge base, like EBSCO, or use FOLIO’s internal knowledge base. Note: Some instructions differ depending on your library’s use of an external or internal knowledge base.


## Permissions

The permissions listed below allow you to interact with the Agreements app and determine what you can or cannot do within the app. You can assign permissions to users in the Users app. If none of these permissions are assigned to a user, they are unable to see the Agreements app or any related information.



The following permissions are applicable to all libraries using the Agreements app:



*   **Agreements: Search & view agreements.** This permission allows the user to search and view existing agreements. It also allows the user to see and access the Agreement app in the FOLIO interface.
*   **Agreements: Edit agreements.** This permission allows the user to edit agreements, including the ability to add and edit agreement lines; to add and edit documents; and to view, add and edit tags on an agreement. It also grants all permissions included in "Agreements: Search & view agreements.”
*   **Agreements: Delete agreements.** This permission allows the user to delete agreements. (This does not include the ability to edit agreements, only to delete them.) It also grants all permissions included in "Agreements: Search & view agreements.”
*   **Agreements: File download.** (ui-agreements.agreements.file.download) This permission grants permission for document downloads, as separate from document uploads.

The following permissions are only applicable if your library is using the internal KB:



*   **Agreements: Search & view e-resources.** This permission allows the user to search and view e-resources (packages and titles in those packages) in the internal KB. This includes the permission to see and access the Agreements app in the FOLIO interface.
*   **Agreements: Edit e-resources.** This permission allows the user to edit the e-resources. It also grants all permissions included in "Agreements: Search & view e-resources."
*   **Agreements: Search & view platforms.** This permission allows the user to search and view platforms in the internal KB. This includes the permission to see and access the Agreement app in the FOLIO interface.
*   **Agreements: Edit platforms.** This permission allows the user to edit platform properties. It also grants all permissions included in "Agreements: Search & view e-resources."

If you want eUsage data in an agreement record, you also need to have the following eUsage permission:



*   **eUsage reports: charts may be viewed.** This permission adds an accordion to the Agreement record in the Agreement app that displays charts and graphs of eUsage data for the titles related to an agreement.


## Keyboard shortcuts


Keyboard shortcuts allow you to perform actions in this app using the keyboard.  See [Platform essentials \> Keyboard shortcuts](../../platform-essentials/keyboard-shortcuts/keyboardshortcuts/) for more information.


## Creating an agreement



1. In the **Agreements** pane, click **Actions** and select **New**.
2. In the **New agreement** window, fill in the Primary fields, Agreement periods, Internal contacts, Agreement lines, License information, Organizations, Supplementary properties, Supplementary documents, Usage data, and Related agreements sections. For more information on the fields and actions available in these sections, see the section descriptions below.
3. Once you have included all of the information you want about the agreement, click **Save & close**. The agreement is saved and added to the Agreements pane.


### Primary fields



*   **Name (required).** The title of the agreement record.
*   **Description**. Enter a description of the agreement.
*   **Status (required).** Select from the drop-down list the state of the agreement. For example, Active or Closed. You can configure the labels that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
*   **Reason for closure.** This option only becomes available if **Closed** is selected from the **Status** drop-down list. Select from the drop-down list why the agreement was closed. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
*   **Renewal priority.** Select from the drop-down list the level of interest in renewing the agreement. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
*   **Is perpetual.** If the agreement provides perpetual access to the purchased materials, select *Yes*. You can configure the labels that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
*   **Content type.** If the agreement represents a particular content type or types, add one or more content type field and select a type from the drop-down list. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
*   **Alternative names.** Alternative names for the agreement record.


#### Adding a content type

Note: Adding a content type is optional, but if you click **Add content type**, you must enter a content type or delete the content type in order to save the agreement record.



1. Click **Add content type**.
2. Select the agreement record’s content type from the drop-down list. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
3. Repeat as needed. The Content type saves once you save the agreement.


#### Deleting a content type



1. Find the Content type you want to delete.
2. Click the **trash can icon**. The Content type is deleted and is removed from the record once you save the agreement.


#### Adding an alternative name

Note: Adding an alternative name is optional, but if you click **Add alternative names**, you must enter an alternative name or delete the alternative name in order to save the agreement record.



1. Click **Add alternative name**.
2. Enter the agreement record’s **Alternative name** in the box.
3. Repeat as needed. The Alternative name saves once you save the agreement.


#### Deleting an alternative name



1. Find the Alternative name you want to delete.
2. Click the **trash can icon**. The Alternative name is deleted and is removed from the record once you save the agreement.


### Agreement periods

Agreement periods allow you to record and manage the ranges of time for which the agreement is active.

When adding agreement periods, you should consider the following:



*   Every record must have at least one agreement period.
*   If only a single agreement period is used, no other information is displayed in relation to periods.
*   If you add multiple periods to the record, their dates cannot overlap.
*   Each period must have a start date.
*   The earliest period start date is treated as the agreement start date.
*   End dates are optional, but only one period in a set can be left without an end date. This is referred to as an open-ended period, which has a start date but is assumed to continue for an indefinite amount of time.
*   The latest period end date is treated as the agreement end date, or if there is a blank period end date the agreement is treated as having no end date.
*   You can navigate between past, present, and future periods by clicking on the **Previous**, **Current**, or **Next** buttons.


#### Adding an agreement period



1. Enter the agreement period’s **Start date**.
2. Fill in the rest of the fields. See below for more information. The agreement period saves once you save the agreement.
3. To enter multiple agreement periods, click **Add agreement period** and repeat steps 1-2.
*   **Start date (required).** The date when the agreement begins.
*   **End date.** The date when the agreement terminates.
*   **Cancellation deadline.** The date by which you need to cancel the agreement if you do not want to renew the material covered by the agreement.
*   **Period note.** Any additional information about the agreement period that you want to include.


#### Deleting an agreement period



1. Find the Agreement period you want to delete.
2. Click the **trash can icon**. The Agreement period is deleted and is removed from the record once you save the agreement.


### Internal contacts

Internal contacts are generally the people within your library that you need to contact if you have questions about the agreement. For example, you may want to add the ERM librarian responsible for renewals, the authorized signatory for an agreement, or the subject matter expert responsible for reviewing content ahead of renewals. Multiple contacts can be assigned to a record, but each contact you add must have a user record in the Users app.


#### Adding an internal contact



1. Click **Add internal contact.**
2. Click **Link user.**
3. In the **Select User** dialog, enter the user’s name or portion of a name into the search box in the **User Search** pane, and click **Search.** User Search Results appear.
4. (Optional) Filter results by Status or by Patron group.
5. Click the user to select. The user is added to the agreement record as an internal contact.
6. Select the internal contact’s **Role** from the drop-down list. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
7. Repeat steps 1-6 as needed. The internal contacts are saved once you save the agreement.


#### Removing an internal contact



1. Identify the Internal contact you want to remove.
2. Click the **trash can icon**. The Internal contact is removed from the record once you save the agreement.


### Agreement lines

An agreement line represents the material covered by the agreement, for example, a package or title. If you want to add agreement lines, you should save your progress on the agreement record you are creating or wait until you have completed and saved all agreement information before you start the agreement line process. For instructions on adding agreement lines to a record, see [Adding an agreement line](#adding-an-agreement-line).


### License information

In the License information section, you can link your agreement record to a license record. There are two types of licenses you can add in this section: license records created in the Licenses app or external license records (for example, licenses maintained by a consortium).

Note: You can add multiple license records to an agreement record, but only one can be the Controlling license. All other licenses must be designated as Historical or Future. For more information, see step 6 under [Adding a license created in the Licenses app to an agreement](#adding-a-license-created-in-the-licenses-app-to-an-agreement).


#### Adding general notes about the license



*   At the top of the License information section, you can add **General notes about the agreement’s license** into the box.


#### Adding a license created in the Licenses app to an agreement

Note: If the license you link to the agreement has amendments present, once you link the license the amendments also display. They also need to have a status in relation to the agreement set. This is important as it is the combination of the applicable (controlling) licenses and amendments that dictate the terms that apply to the agreement.



1. Click **Add license**.
2. Click **Link license**.
3. In the **Select license** dialog, enter the license’s name or a portion of the name into the search box in the **Search & filter** pane, and click **Search**. Search results appear in the Licenses pane.
4. (Optional) Filter results using the filters in the **Search & filter** pane.
5. Click the license to select. The license is added to the agreement record.
6. Select the **Status (this agreement)** from the drop-down list: Controlling, Future, or Historical. Note: Only one license can have the status Controlling in relation to the agreement at one time. Controlling means the terms in the license are applied to the agreements right now. It is the terms from the Controlling license that are displayed as the agreement license terms in the agreement details pane. Future means that the license becomes controlling at some point in the future. Historical means that the license was the controlling license at some point in the past.
7. (Optional) Enter any notes about the license in the **Note** box.
8. Repeat steps 1-7 as needed. The license saves once you save the agreement.


#### Adding an external license to an agreement

External licenses are any license not available through the Licenses app.



1. Click **Add external license**.
2. Enter a **Name** in the box.
3. (Optional): Enter a **Note** about the license.
4. You must complete at least one of the following:
    * Upload a file into the license record by dragging and dropping the file in the **Drag & drop to upload** box, or click **or choose file**.
    * Enter the **Physical location** of the license in the box.
    * Enter the **URL** of the license in the box.
5. Repeat steps 1-4 as needed. The external license saves once you save the agreement record.


#### Removing a license



1. Find the license you want to remove.
2. Click the **trash can icon**. The license is removed from the record once you save the license.


#### Replacing a license



1. Find the license you want to replace.
2. Click **Replace license.**
3. Repeat steps 3-7 under [Adding a license created in the Licenses app to an agreement](#adding-a-license-created-in-the-licenses-app-to-an-agreement).


### Organizations

Organizations are any institution with which your library interacts. For example, you may want to add a vendor or consortium associated with the agreement. Multiple organizations can be added to a record, but the organizations must first be created in the [Organizations app](../../acquisitions/organizations/). To set one organization as the primary organization, check the **Set as primary organization** box.


#### Adding an organization



1. Click **Add organization.**
2. In the **Organization** box, click **Link organization.**
3. In the **Select Organization** dialog, in the **Search & filter** pane search box, enter the organization’s name or use the All drop-down list to search through specific organization parameters, and click **Search**. Search results appear in the Organizations pane.
4. (Optional) Filter results using the filters in the **Search & filter** pane.
5. Click the organization to select. The organization is added to the agreement record.
6. Select the organization's **Role** from the drop-down list. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
7. (Optional) Enter any notes about the organization in the **Note** box.
8. Repeat steps 1-7 as needed. The organization saves once you save the agreement.


#### Removing an organization



1. Find the Organization you want to remove.
2. Click the **trash can icon**. The Organization is removed from the record once you save the agreement.


#### Replacing an organization



1. Find the Organization you want to replace.
2. Click **Replace organization.**
3. Repeat steps 3-7 under [Adding an organization](#adding-an-organization).


### Supplementary properties

Supplementary properties are an optional way to record additional information about the agreement not captured anywhere else in the record. For example, the authentication method used to access the material covered by the agreement.

Note: This section only appears if you have configured supplementary properties in the Settings app. For more information on setting up properties, see [Settings \> Agreements \> Supplementary properties](../../settings/settings_agreements/settings_agreements/#settings--agreements--supplementary-properties).


#### Filling out a primary property

If a property is defined as primary in the Settings app, then it always appears as an option in an agreement record. You can leave the **Value** of a primary term blank or select **Not set**, but primary terms cannot be removed from the agreement record.



1. Complete the **Value** field either by inputting text, using the up and down arrows to set an integer, or selecting an option from the drop-down list. The value is the definition of, or answer to, the property.
2. (Optional) Enter an **Internal note** in the box. Any text you enter here displays internally to FOLIO users.
3. Select the property’s **Visibility** from the drop-down list. Visibility indicates whether the property should display internally (only within FOLIO), or externally to the public through, for example, your catalog.
4. (Optional) Enter a **Public note** in the box. Any text you enter here displays externally to the public.
5. Repeat steps 1-4 for as many primary properties as desired. The properties save once you save the agreement.


#### Adding an optional property

A property is optional if it is not defined as primary in the Settings app. Optional properties do not automatically display in an agreement record.



1. Click **Add property.**
2. Select the property **Name** from the drop-down list.
3. Follow steps 1-4 under [Filling out a primary property](#filling-out-a-primary-property).
4. Add as many optional properties as needed. The properties save once you save the agreement.


#### Removing an optional property



1. Find the optional term you want to remove.
2. Click the **trash can icon**. The optional property is removed from the record once you save the agreement.


### Supplementary documents

A supplementary document is any additional document relevant to the agreement record.


#### Adding a supplementary document



1. Click **Add supplementary document.**
2. Enter a **Name** in the box.
3. Select a **Category** from the drop-down list. You can configure the values that appear in the drop-down list in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).
4. (Optional) Enter a **Note** about the supplementary document.
5. You must complete at least one of the following:
    * Upload a file into the agreement record by dragging and dropping the file in the **Drag & drop to upload** box, or click **or choose file**.
    * Enter the **Physical location** of the document in the box.
    * Enter the **URL** of the document in the box.
6. Repeat steps 1-5 as needed. The supplementary document saves once you save the agreement.

If a supplementary document is present in an agreement record, then a **copy icon** will appear in the supplementary document accordion multi-column list under Reference. Clicking the **copy icon** will copy the text content of the Reference column to your clipboard. 


#### Removing a supplementary document



1. Find the supplementary document you want to remove.
2. Click the **trash can icon**. The supplementary document is removed from the record once you save the agreement.


### Usage data

A usage data provider is any organization that provides e-resource usage data to your library. Multiple usage data providers can be added to a record, but the usage data providers must first be created in the eUsage app.


#### Adding a usage data provider



1. Click **Add usage data provider.**
2. In the **Usage data provider** box, click **Link usage data provider.**
3. In the **Select usage data provider** dialog, enter the provider’s name or a portion of the name into the search box in the **Search & filter** pane, and click **Search**. Search results appear in the Usage Data Providers pane.
4. (Optional) Filter results using the filters in the **Search & filter** pane.
5. Click the usage data provider to select. The provider is added to the agreement record.
6. (Optional) Enter a **Note** about the usage data provider.
7. Repeat steps 1-6 as needed. The Usage data provider saves once you save the agreement.


#### Removing a usage data provider



1. Find the Usage data provider you want to remove.
2. Click the **trash can icon**. The Usage data provider is removed from the record once you save the agreement.


#### Replacing a usage data provider



1. Find the Usage data provider you want to replace.
2. Click **Replace usage data provider.**
3. Repeat steps 3-6 under [Adding a usage data provider](#adding-a-usage-data-provider).


### Related agreements

A related agreement is an agreement relevant to the current agreement. This section allows you to link agreements together to establish relationships among them. For example, you may want to add a post-cancellation agreement here.


#### Adding a related agreement



1. Click **Add related agreement.**
2. In the **Agreement** box, click **Link agreement.**
3. In the **Select agreement** dialog, enter the agreement’s name or a portion of the name into the search box in the **Search & filter** pane, and click **Search**. Search results appear in the Agreements pane.
4. (Optional) Filter results using the filters in the **Search & filter** pane.
5. Click the agreement to select. The agreement is added to the agreement record.
6. Select the **Linked agreement’s relationship to the agreement being edited** from the drop-down list. Note: The relationships are directional. For example, if Agreement A “has backfile in” Agreement B, then automatically Agreement B “has frontfile in” Agreement A. You can set these from either end (i.e. you can start by linking Agreement A to B or B to A).
7. (Optional) Enter a **Note** about the related agreement.
8. Repeat steps 1-6 as needed. The related agreement saves once you save the main agreement.


#### Removing a related agreement



1. Find the Related agreement you want to remove.
2. Click the **trash can icon**. The Related agreement is removed from the record once you save the agreement.


#### Replacing a related agreement



1. Find the Related agreement you want to replace.
2. Click **Replace agreement.**
3. Repeat steps 3-6 under [Adding a related agreement](#adding-a-related-agreement).


## Searching for agreements

You can search for agreements in the **Search & filter** pane. To search for agreements, enter your search terms in the search box and click **Search**. The search box searches through the Name, Description, and Alternative names fields. In order to limit your search to specific fields, check one or more of the  **Name**,  **Alternative name** and/or **Description** check boxes below the search box, and the search will only search through the selected fields.

Note: When using the internal KB, click **Agreements search** in order to search for agreements. 

You can also search for agreements by selecting any of the filters in the **Search & filter** pane: Status, Renewal priority, Is perpetual, Start date, End date, Organizations, Organization role, Internal contacts, Internal contacts role, Content type, Tags, Supplementary properties, Agreement content, and Documents. For more information on the filters, see the filter descriptions below.


### Status

To filter agreements by their status, select one of the following:



*   **Active.** Agreements currently in use by your library.
*   **Closed.** Agreements no longer in use by your library.
*   **Draft.** An agreement that is in draft form.
*   **In negotiation.** An agreement that is being negotiated between your library and a provider.
*   **Requested.** If your library has requested an agreement from a provider.


### Reason for closure

To filter agreements by their reason for closure, select one of the listed options. Possible priorities may include:



*   **Canceled.** Agreements you have canceled.
*   **Ceased.** Agreements that have ended.
*   **Rejected.** Agreements you have rejected.
*   **Superseded.** Agreements that have been superseded by another agreement.

Renewal priority values are configured in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).


### Renewal priority

To filter agreements by their renewal priority, select one of the listed options. Possible priorities may include:



*   **Definitely renew.** Agreements you want to renew.
*   **Definitely cancel.** Agreements you do not want to renew.

Renewal priority values are configured in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values).


### Is perpetual

To filter agreements by whether or not they are perpetual, select **Yes** or **No**.


### Start date

To filter agreements by their start date, enter a date into the **On or after** and/or **On or before** search box, or click the **calendar icon** to select a date from the calendar.


### End date

To filter agreements by their end date, enter a date into the **On or after** and/or **On or before** search box, or click the **calendar icon** to select a date from the calendar.

You can also check the box **Include agreements with no end date set** to locate agreements without end dates.




### Cancellation deadline

To filter agreements by their cancellation deadline, enter a date into the **On or after** and/or **On or before** search box, or click the **calendar icon** to select a date from the calendar.

You can also check the box **Include agreements with no cancellation deadline set** to locate agreements without cancellation deadlines.


### Organizations

To filter agreements associated with a specific organization, follow these steps:



1. In the **Search & filter** pane, click **Organizations**.
2. Click **Select an organization**.
3. In the drop-down list, search for the organization.
4. Select the organization by which you want to filter. The search results appear in the Agreements pane.


### Organizations role

To filter agreements by their associated organizations’ roles, follow these steps:



1. In the **Search & filter** pane, click **Organization role**.
2. Click **Select a role**.
3. In the drop-down list, search for the role.
4. Select the role by which you want to filter. The search results appear in the Agreements pane.


### Internal contacts

To filter agreements by their associated internal contacts, follow these steps:



1. In the **Search & filter** pane, click **Internal contacts**.
2. Click **Select an internal contact**.
3. In the drop-down list, search for the internal contact.
4. Select the internal contact by which you want to filter. The search results appear in the Agreements pane.


### Internal contacts role

To filter agreements by their associated internal contacts’ roles, follow these steps:



1. In the **Search & filter** pane, click **Internal contact role**.
2. In the drop-down list, search for the internal contact role.
3. Select the internal contact role by which you want to filter. The search results appear in the Agreements pane.


### Content type

To filter agreements by their content type, follow these steps:



1. In the **Search & filter** pane, click **Content type**.
2. Check the box next to the content type(s). The search results appear in the Agreements pane.


### Tags

To search for agreements assigned specific tags, follow these steps:



1. In the **Search & filter** pane, click **Tags**.
2. Select the tag(s) from the drop-down list. Your results appear in the Agreements pane.


### Supplementary properties

To filter agreements by their supplementary properties, follow these steps:



1. In the Search & filter pane, click **Supplementary properties**.
2. Click **Edit supplementary property filters**.
3. In the **Supplementary property filter builder** dialog, select a **Supplementary property** from the drop-down list.
4. Select a **Comparator** from the drop-down list. The comparator options depend on the term selected.
5. If the **Value** box is available, select or enter a value. Whether the value box is available depends on which comparator is selected.
6. (Optional) To continue to build the supplementary property filter, click **Add rule.**
7. (Optional) To search for agreements using multiple supplementary property filters, click **Add supplementary property filter**. Note: To delete a rule or supplementary property filter in the Supplementary property filter builder, click on the **trash can icon** next to the rule or supplementary property filter.
8. Click **Apply.** Your results appear in the Agreements pane.


### Agreement content

To filter agreements by their content, follow these steps:



1. In the Search & filter pane, click **Agreement content**.
2. Select Has or Has not from the drop-down list. 
3. Select one or more agreement content options from the list. These may include Alternative names, Content types, Internal contacts, Organizations, Agreement lines, Linked licenses, External licenses, Supplementary documents, Usage data, Related agreements, and Tags. Note, if you select multiple agreement content options, they are combined with OR (rather than AND). For example, if you select Alternative names and Content types, the returned results will include agreement records with Alternative names OR Content types. 
4. To add another filter, click **Add filter** and select And or Or. 
5. Repeat the above steps as desired. 
6. Your results will appear in the Agreements pane.


### Documents

To filter agreements by their documents, follow these steps:



1. In the Search & filter pane, click **Documents**.
2. Click **Edit document filters**.
3. In the **Document filter builder** dialog, select an **Attribute** from the drop-down list. Attributes include Name, Note, Category, Physical location, URL, Content type, and File name. 
4. Select an **Operator** from the drop-down list. Operators include Is, Contains, and Does not contain.
5. In the **Value** box, select or enter a value.
6. (Optional) To continue to build the document filter, click **Add rule.** Note, multiple rules in a single document filter card will apply to a single document. I.e. If you have a document filter card with two rules, then to find an agreement, a single document on that agreement must fulfill both rules. Whereas when you add a new document filter card in the filter builder, then it can apply to either the same or a different document. 
7. (Optional) To search for agreements using multiple document filters, click **Add filter**. Note: To delete a rule or document filter in the Document filter builder, click on the **trash can icon** next to the rule or document filter.
8. Click **Save & close.** Your results appear in the Agreements pane.


## Viewing an agreement

Once you search for an agreement, the following information appears in the Agreement pane:



*   **Name.** The name of the agreement.
*   **Status.** The order status.
*   **Period start.** The date the agreement period starts.
*   **Period end.** The date the agreement period ends.
*   **Cancellation deadline.** The date by which you need to cancel the agreement if you do not want to renew the material covered by the agreement.
*   **Description: A description of the agreement.

In the search results, click an agreement to view it. The agreement details pane displays with additional information about the agreement. In the agreement display, any accordions not populated with data and not otherwise required are not displayed to the user.


## Controlling which columns display in the Agreements multi-column list

1. In the **Agreements search** display, click **Actions**. 
2. At the bottom of the Actions menu is the heading **Show columns** followed by a list of available columns with checkboxes to display or hide those columns. All columns are displayed by default. The columns available should be (in order): Name, Status, Start date, End date, Cancellation deadline, and Description. 
3. When you uncheck a box, that column is removed from the display of the multi-column list.
   * Note: the Name column is the main column and cannot be selected or unselected.
5. When you check a box, that column is added to the display of the multi-column list.
6. When you go to the agreement search and sort view in the same session, the selection of which columns display persists.


## Editing an agreement



1. Find the agreement you want to edit.
2. In the **agreement details** pane, click **Actions > Edit**.
3. Make your desired changes to the agreement.
4. Click **Save & close**. The agreement is updated.


## Deleting an agreement

Note: You cannot delete an agreement that is linked to a license, has agreement lines, or is related to another agreement.



1. Find the agreement you want to delete.
2. In the **agreement details** pane, click **Actions > Delete**.
3. In the **Delete agreement** dialog, click **Delete**. A confirmation message appears and the agreement is deleted.


## Adding an agreement line

An agreement line represents the material covered by the agreement, for example, a package or title. The steps for adding agreement lines vary depending on whether your library is using the internal KB or an external KB.

Note, adding an agreement line cannot be done in an agreement that is open for editing.


### Adding an agreement line via the internal KB

When using the internal KB, you first have to add e-resources to a basket in the E-resources pane. Then you can apply those e-resources to agreement lines.


#### Adding e-resources to the basket

Before you can add e-resources to agreement lines in an existing or new agreement, you must first add them to a basket. The basket is a temporary container that holds any e-resources (titles or packages) with which you need to work. E-resources are added on a one-by-one basis to an agreement line, so you can add as many e-resources to the basket as you need.



1. In the **Search & filter** pane, click **E-resources**.
2. Search for the e-resource you want to add to the basket.
3. In the **E-resources** pane, click on the e-resource to select it.
4. In the **e-resource details** pane, click **Options for acquiring e-resource**.
5. In the **Options** table, in the **Actions** column, click **Add title** or **Add package** to add that e-resource to the basket. The e-resource is added to the basket and the number of items in the basket updates.
6. Repeat steps 2-5 for all e-resources you want to add to the basket.


#### Adding e-resources from the basket to an agreement

There are two ways to add an e-resource from the basket to agreement lines:


##### From the basket



1. Click the **View X item(s)** button to open the basket.
2. Select or unselect the items in the basket you wish to add to agreement lines using the checkboxes to the left of the resources in the basket.
3. Select **Create new agreement** to add the selected resource(s) to a completely new agreement (one agreement line per resource selected), or click **Select agreement** and use the Search & filter plugin to add the selected resource(s) to an existing agreement (one agreement line per resource selected).
4. The agreement for which the agreement lines have been created (whether this is a new or existing agreement) is displayed in the agreement view screen.



##### From the Agreement Line Edit screen



1. [Find the agreement](#searching-for-agreements) to which you want to add an agreement line and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click **Actions** and select **New agreement line**.
4. In the **New agreement line** window, if not already selected, click **Basket**.
5. In the E-resource drop-down select the resource from the Basket for which you want to create an agreement line.
6. (Optional) Enter a **Description** of the agreement line in the box.
7. (Optional) Enter a **Note** about the agreement line in the box.
8. (Optional) Enter **Active from** and **Active to** dates to indicate when the material covered by this agreement line was or is active in your collection.
9. (Optional) To hide this information from your discovery layer, select the **Suppress from discovery** checkbox. If you don’t want this checkbox to appear, or you would like the checkbox to display on agreement line records, see [Settings \> Agreements \> Display settings](../../settings/settings_agreements/settings_agreements/#settings--agreements--display-settings) for more information.
10. (Optional) To link the agreement line to a PO line, click **Add PO line**. See Adding a PO line to an agreement line for more information.
11. To add multiple agreement lines at once, check the **Create another** checkbox and repeat steps 1-10.
12. Click **Save & close**. A confirmation message appears and the agreement line is saved.


### Adding an agreement line via eHoldings


1. [Find the agreement](#searching-for-agreements) to which you want to add an agreement line and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click **Actions** and select **New agreement line**.
4. In the **New agreement line** window, if not already selected, click **eHoldings**.
5. Click **Link e-resource.**
6. In the **Select package** dialog, in the **Search & filter** pane, enter a **Package** name in the box, or click **Titles** and enter a **Title** name in the box. Click **Search**. Search results appear.
7. (Optional) Use the filters in the Search & filter pane to narrow down your results.
8. Click the **Package** or **Title** to select it. The package or title is added to the agreement line.
9. (Optional) Enter a **Description** of the agreement line in the box.
10. (Optional) Enter a **Note** about the agreement line in the box.
11. (Optional) Enter **Active from** and **Active to** dates to indicate when the material covered by this agreement line was or is active in your collection.
12. (Optional) To hide this information from your discovery layer, select the **Suppress from discovery** checkbox. If you don’t want this checkbox to appear, or you would like the checkbox to display on agreement line records, see [Settings \> Agreements \> Display settings](../../settings/settings_agreements/settings_agreements/#settings--agreements--display-settings) for more information.
13. (Optional) To link the agreement line to a PO line, click **Add PO line**. See [Adding a purchase order line to an agreement line](#adding-a-purchase-order-line-to-an-agreement-line) for more information.
14. To add multiple agreement lines at once, check the **Create another** checkbox and repeat steps 1-13.
15. Click **Save & close**. A confirmation message appears and the agreement line is saved.


### Adding a purchase order line to an agreement line

You have the option of adding a purchase order line (POL) to an agreement line. Linking the agreement line to a POL adds context to the agreement line. For example, it can show how you paid for, or the method by which you ordered, the material. 

When an agreement line is linked to a POL that is linked to an Inventory instance, a link directly to the Inventory instance is displayed in the Agreement Line display.

Note: If you are already editing an agreement line, skip to step 5.



1. [Find the agreement](#searching-for-agreements) with the agreement line to which you want to add a POL and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click the agreement line to which you want to add a POL.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. In the **Edit agreement line** window, click **Add PO line**.
6. Click **Link PO line**.
7. In the **Select order lines** dialog, in the **Search & filter** box, enter part or all of the title or package’s name, and click **Search**.
8. (Optional) Filter results using the filters in the Search & filter pane.
9. In the **Search results** pane, click the **POL** to select it. The Select order lines dialog closes and the POL is added to the agreement line.
10. Repeat steps 5-9 as needed. The POLs are saved when the agreement line is saved.


### Replacing a purchase order line in an agreement line



1. [Find the agreement](#searching-for-agreements) with the agreement line to which you want to replace a POL and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click the agreement line to which you want to replace a POL.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. In the **Edit agreement line** window, click **Replace PO line** and
6. Follow steps 7-9 under [Adding a purchase order line to an agreement line](#adding-a-purchase-order-line-to-an-agreement-line).


### Deleting a purchase order line from an agreement line



1. [Find the agreement](#searching-for-agreements) with the agreement line with the POL you want to delete and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click the agreement line with the POL you want to delete and select it.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. To remove the POL, click the **trash can icon** next to the PO line you want to delete.
6. Click **Save & close**. A confirmation message appears and the agreement line is updated.


### Adding a document to an agreement line

You have the option of adding a document to an agreement line. For example, if an agreement line represents a package, a document describing the package and content could be uploaded. Or if an agreement line is for an ebook that is catalogued, a URL could be added linking the relevant inventory item, holding or instance. 

Note: If you are already editing an agreement line, skip to step 5.



1. [Find the agreement](#searching-for-agreements) with the agreement line to which you want to add a document and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click the agreement line to which you want to add a document.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. In the **Edit agreement line** window, click **Add document**.
6. Enter a **Name** in the box.
7. (Optional): Select a **Category** from the drop-down list.
    * Categories include Consortium negotiation document, License, and Misc.
8. (Optional): Enter a **Note** about the document.
9. You must complete at least one of the following:
    * Upload a file into the agreement record by dragging and dropping the file in the **Drag & drop to upload** box, or click **or choose file**.
    * Enter the **Physical location** of the document in the box.
    * Enter the **URL** of the document in the box.
10. Repeat steps 5-9 as needed. The documents are saved when the agreement line is saved.


### Deleting a document from an agreement line



1. [Find the agreement](#searching-for-agreements) with the agreement line with the document you want to delete and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click the agreement line with the document you want to delete and select it.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. To remove the document, click the **trash can icon** next to the document you want to delete.
6. Click **Save & close**. A confirmation message appears and the agreement line is updated.


### Adding an unlinked agreement line

Use this feature to add an agreement line that has no connection to a record from either the internal KB or eHoldings.



1. [Find the agreement](#searching-for-agreements) to which you want to add an agreement line and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click **Actions** and select **New agreement line**.
4. Enter a **Description (required)**. You can also add a **Note** and/or **Active from** and **Active to** dates. The description will appear as the agreement line’s Name/Description in the agreement record.
5. (Optional) To link the agreement line to a PO line, click **Add PO line**. See [Adding a purchase order line to an agreement line](#adding-a-purchase-order-line-to-an-agreement-line) for more information.
6. To add multiple agreement lines at once, check the **Create another** checkbox and repeat steps 1-5.
7. Click **Save & close.**


## Editing an agreement line



1. [Find the agreement](#searching-for-agreements) with the agreement line you want to edit and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to edit.
4. In the **Agreement line** pane, click **Actions > Edit**.
5. Make your desired changes.
6. Click **Save & close**. A confirmation message appears and the agreement line is updated.


## Deleting an agreement line

Note: Agreements can also be unlinked from packages and titles in the eHoldings app.



1. [Find the agreement](#searching-for-agreements) with the agreement line you want to delete and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to delete.
4. In the **Agreement line** pane, click **Actions > Delete**.
5. In the **Delete agreement line** dialog, click **Delete**. A confirmation message appears and the agreement line is deleted.


## Viewing agreement lines

In order to view all of the agreement lines associated with a particular agreement at once, you can enter the **View in agreement lines search**. To do so, follow these steps: 

1. [Find the desired agreement](#searching-for-agreements).
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click **Actions** and select **View in agreement lines search**. 
4. The Agreement line search pane will open. Clicking on any agreement line will display the Agreement line details record from which you can edit or delete the agreement line. 

## Controlling which columns display in the agreement lines multi-column list


1. [Find the desired agreement](#searching-for-agreements).
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** section, click **Actions**. 
4. At the bottom of the Actions menu is the heading **Show columns** followed by a list of available columns with checkboxes to display or hide those columns. All columns are displayed by default. The columns available should be (in order): Name / Description, Provider, Publication type, Count, Note, Coverage, Custom coverage indicator, Active from, Active to, and PO Line. 
5. When you uncheck a box, that column is removed from the display of the multi-column list.
   * Note: the Name column is the main column and cannot be selected or unselected.
7. When you check a box, that column is added to the display of the multi-column list.
8. When you go to the agreement lines multi-column list view for any agreement in the same session, the selection of which columns display persists. 


## Searching for agreement lines



You can search for agreement lines in the **Search & filter** pane. To search for agreement lines, click **Agreement lines** and enter your search terms in the search box and click **Search**. The search box searches through the Name (for resources from the internal KB), Reference number (for resources from eHoldings), Description, and Note fields.

Note: When using the internal KB, click **Agreements search** in order to search for agreement lines. 

You can also search for agreement lines by selecting any of the filters in the **Search & filter** pane: Agreement, Agreement line type, Active from, Active to, PO line, and Tags. For more information on the filters, see the filter descriptions below.


### Agreement

To filter agreement lines by an agreement record, click **Select agreement**. In the **Select agreement** window, use the **Search & filter** feature to locate the desired agreement and click on it. See [Searching for agreements](#searching-for-agreements). Your agreement line search will be limited to that agreement record.


### Agreement line type

To filter agreement lines by type, check the **Unlinked**, **External**, and/or **Internal** checkboxes. An **unlinked agreement line** is not linked to a resource in a knowledge base. An **external agreement line** is linked to a resource in an external knowledge base (like the eHoldings app), and an **internal agreement line** is linked to a resource in the internal knowledge base.


### Active from

To filter agreement lines by their active from date, enter a date into the **On or after** and/or **On or before** search box, or click the **calendar icon** to select a date from the calendar. Click **Apply**.

You can also check the box **Include lines with no active from date set** to locate lines without start dates.


### Active to

To filter agreement lines by their active to date, enter a date into the **On or after** and/or **On or before** search box, or click the **calendar icon** to select a date from the calendar. Click **Apply**.

You can also check the box **Include lines with no active to date set** to locate lines without end dates.


### PO line

To filter agreement lines by PO line, click **Select PO line**. In the **Select order lines** window, use the **Search & filter** feature to locate the desired PO line and click on it.


### Tags

To search for agreement lines assigned specific tags, follow these steps:



1. In the **Search & filter** pane, click **Tags**.
2. Select the tag(s) from the drop-down list. Your results appear in the Agreement lines pane.


### Documents

To search for agreement lines linked to specific documents, follow these steps:



1. In the Agreement lines Search & filter pane, click **Documents**.
2. Click **Edit document filters**.
3. In the **Document filter builder** dialog, select an **Attribute** from the drop-down list. Attributes include Name, Note, Category, Physical location, URL, Content type, and File name. 
4. Select an **Operator** from the drop-down list. Operators include Is, Contains, and Does not contain.
5. In the **Value** box, select or enter a value.
6. (Optional) To continue to build the document filter, click **Add rule.** Note, multiple rules in a single document filter card will apply to a single document. I.e. If you have a document filter card with two rules, then to find an agreement line, a single document on that agreement line must fulfill both rules. Whereas when you add a new document filter card in the filter builder, then it can apply to either the same or a different document. 
7. (Optional) To search for agreement lines using multiple document filters, click **Add filter**. Note: To delete a rule or document filter in the Document filter builder, click on the **trash can icon** next to the rule or document filter.
8. Click **Save & close.** Your results appear in the Agreements lines pane.


## Adding a tag to an agreement



1. [Find the agreement](#searching-for-agreements) you want to tag and select it.
2. In the **Agreement details** pane, click the **tag icon**.
3. In the **Tags** pane, either select a tag from the box or enter a tag.
4. Click the **X** on the Tags pane to close the pane and save the tag. The tag number updates to the number of tags applied to the agreement.


## Duplicating an agreement

Note: Periods are not duplicated as part of the agreement, but a single period with the current date as the start date will be added automatically (because Agreements have to have at least one period with a start date).



1. Find the agreement you want to duplicate and select it.
2. In the **Agreement details** pane, click **Actions > Duplicate**.
3. In the **Duplicate agreement** dialog, select which sections of the agreement to duplicate. See [Creating an agreement](#creating-an-agreement) for the fields that appear in each of the sections.
4. Click **Save & close**.
5. In the **Copy of: [duplicated agreement’s name]** window, make your desired changes.
6. Click **Save & close**. A confirmation message appears and the duplicated agreement appears in the Agreements pane.


## Exporting an agreement

Exporting an agreement generates a JSON file. Note: Resources are only included for agreement lines that are linked to resources in the internal KB.



1. Find the agreement you want to export and select it.
2. In the **Agreement details** pane, select **Actions > Export**. Depending on your browser and its configurations, the file automatically downloads or you are prompted to save it.


## Exporting e-resources

Exporting e-resources covered by an agreement is only possible if using the internal KB, and if e-resources are linked to the agreement as agreement lines.

Note: E-resources can be filtered by Current, Future, or Dropped. These options indicate whether the e-resource is currently associated with the agreement, it will be in the future, or it is no longer associated with the agreement. Export options are only offered for e-resources that are current or all e-resources.



1. [Find the agreement](#searching-for-agreements) from which you want to export the linked e-resources.
2. In the **Agreement details** pane, click **Agreement lines**.
3. Under **E-resources covered by this agreement**, click **Current** or **All**.
4. Click **Export as… > JSON** or **KBART**. Depending on your browser and its configurations, the file automatically downloads or you are prompted to save it.


## Viewing an e-resource

Viewing e-resources covered by agreements is only possible if using the internal KB. 

You can view e-resources by clicking on **Packages** or **Titles** in the **Search & filter** pane. 

In the Packages or Titles pane, click an e-resource to view it. The e-resource details pane displays with additional information about the e-resource. Publication type, Material type, First author, First editor, Publication date, Edition, Volume, ISBN, and Related title fields are populated from the internal KB. The following accordions also display:

**Agreements for this e-resource.** This accordion displays agreements that cover this e-resource. To add an e-resource from the internal KB to an agreement see [Adding an agreement line via the internal KB](#adding-an-agreement-line-via-the-internal-kb).

**Options for acquiring this e-resource.** See [Adding e-resources to the basket](#adding-e-resources-to-the-basket). 

**Notes.** For information on Notes see [Adding and removing notes](#adding-and-removing-notes).

**Discovery settings.** For information on Discovery settings see [Editing e-resources](#editing-e-resources).


### Viewing an e-resource package

You can view packages in e-resources by clicking on **Packages** in the **Search & filter** pane. 

In the Packages pane, click an e-resource package to view it. The e-resource package details pane displays with additional information about the e-resource package, depending on the data that has been added to the internal KB. All packages will have a Provider, Source and Reference. They will also display when the record was created and when it was last updated. In addition packages may have:

* A Status: For example, Current or Deleted.
* Synchronisation status: Synchronising or Paused. 
* Content type: A list of content types in the package, for example, Serial, Monograph, or Video.
* Availability: The general availability of the package, for example, Global or Consortium, and any constraints on availability, such as the specific Consortia it is available to.
* Source created: The date and time the package was created in the external source the package data came from.
* Source last updated: The date and time the package was last updated in the external source the package data came from.
* One or more of the following package IDs: ISIL, ZDB, EZB, eBookPool, GOKb ID and GOKb. Note that ID fields will only display when an ID of that type is available for the package in the internal KB.

The following accordions also display:

**Extended package information.** This accordion displays additional metadata for this e-resource package including: a Description of the package; Package description URLs, which are links to descriptions of that package online (for example, in GOKb or on a publishers website); Alternative names for the package; and  all package Identifiers stored (this will include any IDs displayed in the package details but may include additional IDs as well).

**Agreements for this package.** This accordion displays agreements that cover this e-resource package. To add an e-resource from the internal KB to an agreement see [Adding an agreement line via the internal KB](#adding-an-agreement-line-via-the-internal-kb).

**E-resources in package.** This accordion displays all e-resources associated with the package. E-resources can be filtered by Current, Future, Dropped, and All.

**Notes.** For information on Notes see [Adding and removing notes](#adding-and-removing-notes).


### Viewing an e-resource title

You can view packages in e-resources by clicking on **Titles** in the **Search & filter** pane. 

In the Titles pane, click an e-resource title to view it. The e-resource title details pane displays with additional information about the e-resource title, depending on the data that has been added to the internal KB. It will also display when the record was created and when it was last updated. 

The following accordions also display:

**Agreements for this e-resource.** This accordion displays agreements that cover this e-resource title. To add an e-resource from the internal KB to an agreement see [Adding an agreement line via the internal KB](#adding-an-agreement-line-via-the-internal-kb).

**Options for acquiring e-resource.** From here you can add a package or title to your basket.

**Notes.** For information on Notes see [Adding and removing notes](#adding-and-removing-notes).

**Discovery settings.** Displays whether the title is suppressed from discovery.


## Editing e-resources



1. Find the e-resource you want to edit.
2. In the **e-resource details** pane, click **Edit**.
3. You can choose whether to suppress the e-resource from discovery by checking the **Suppress from discovery** box. 
4. Click **Save & close**. The e-resource is updated.


### Move identifier(s) between titles

If a title instance is related to an incorrect identifier, you can transfer identifiers between title instances by:


1. In the **E-resources** pane, click **Actions > Move identifier(s)**.
2. Under **Source title**, click **Select title**.
3. Select a title from the **Select e-resource** window. In the **Search & filter** pane of the **Select e-resource** window, you can search e-resources by Name, ISBN and ISSN, and filter by Type.
4. Select the **Identifier(s) to be moved** by checking the desired boxes.
5. Under **Destination title**, click **Select title**.
6. Repeat steps 3 and 4 for the Destination title.
7. Click **Preview**.
8. In the **Preview** window, click **Update titles & close** to complete the transaction, or **Update titles & move more identifiers** to continue moving identifiers. You can track the status of the job in the Local KB admin app.


## Adding a tag to an e-resource



1. [Find the e-resource](#searching-for-e-resources) you want to tag and select it.
2. In the **e-resource details** pane, click the **tag icon**.
3. In the **Tags** pane, either select a tag from the box or enter a tag.
4. Click the **X** on the Tags pane to close the pane and save the tag. The tag number updates to the number of tags applied to the e-resource.


## Local KB search

You can search for packages, titles, and platforms in the local KB by clicking on the **Local KB search** tab. 


### Searching for packages

Searching for packages covered by an agreement is only possible if using the internal KB. 

You can search for packages by clicking on the tab **Local KB search** and selecting **Packages** in the **Search & filter** pane. Enter your search terms in the search box and click **Search**. The search box searches the name field.

Packages can be further filtered by: 

* External data source: Select an external data source from the drop-down list. 
* Status
* Synchronization status
* Scope
* Availability
* Content type
* Tags: Select a tag(s) from the drop-down list, or search for one by typing the tag’s name. 

The values for Status, Scope, Availability, and Content type can be configured in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values). 


#### Synchronizing select package data to Agreements local KB from GOKb

When GOKb is setup as an external data source is setup for the Agreements local KB, packages are only fully synchronized if they are needed locally in the FOLIO tenant. 

* All package header information (i.e. the package name, ID, and other key information) is synchronized
* Each package will be marked in Folio as to be synchronized or not
* Package content (title lists → in GOKb terms these are TIPPs, in Folio called PCIs) will only be synchronized for those packages marked to synchronize

After searching for and selecting packages covered by an agreement in the local KB, under the **Actions** drop-down menu, select **Start synchronisation of selected packages**. To pause synchronization of the packages, select **Pause synchronisation of selected packages**.

Packages can also be synchronized individually by selecting the package record in the local KB search, and selecting **Start synchronisation** from the **Actions** drop-down menu. 


### Searching for titles

Searching for titles covered by an agreement is only possible if using the internal KB. 

You can search for titles by clicking on the tab **Local KB search** and selecting **Titles** in the **Search & filter** pane. Enter your search terms in the search box and click **Search**. The search box searches the name field.

Titles can be further filtered by: 

* Type
* Publication type
* Material type

The values for Type and Publication Type can be configured in [Settings \> Agreements \> Pick list values](../../settings/settings_agreements/settings_agreements/#settings--agreements--pick-list-values). 


## Searching for platforms

Searching for platforms covered by an agreement is only possible if using the internal KB. 

You can search for platforms by clicking on the tab **Local KB search** and selecting **Platforms** in the **Search & filter** pane. Enter your search terms in the search box and click **Search**. The search box searches the name field.


## Viewing a platform

Viewing platforms covered by agreements is only possible if using the internal KB. 

You can view platforms by clicking on the tab **Local KB search** and selecting **Platforms** in the **Search & filter** pane. 

In the **Platforms** pane, click a platform to view it. The platform details pane displays with additional information about the platform. The Locators field is populated with the platform’s base URL from the internal KB. For the Local platform code, see [Editing platforms](#editing-platforms). The following accordions also display:

**Platform URL customization settings.** See [Adding URL customization](#adding-url-customization). 

**Platform proxy server settings.** In Settings > Local KB admin > Proxy server settings, you can add a proxy server setting and exclude platforms one by one. Every platform that is not listed in the array of excluded platforms will contain a generated list of proxy URLs.


## Editing platforms



1. Find the platform you want to edit.
2. In the **platform details** pane, click **Actions > Edit**.
3. You can add a local platform code in the **Local platform code** box. 
4. Click **Save & close**. The platform is updated.


### Adding URL customization



1. Find the platform you want to edit.
2.  In the **platform details** pane under the **Platform URL customization settings** accordion, click **Add URL Customization**.
3. In the **New URL customization** window, enter a Name for the URL. 
4. Enter a **Customization code**. The Customization code is the template that will be used to generate a proxied URL. Please refer to [Proxy server configuration and URL customizations](https://wiki.folio.org/x/qYL-Ag) for further details about the available codes.
5. Click **Save & close**.


### Editing URL customization



1.  In the **platform details** pane under the **Platform URL customization settings** accordion, click on the URL customization.
2. In the **URL customization** window, click **Actions > Edit**. 
3. Make the desired changes to the Name or Customization code.
4. Click **Save & close**.


### Deleting URL customization



1.  In the **platform details** pane under the **Platform URL customization settings** accordion, click on the URL customization.
2. In the **URL customization** window, click **Actions > Delete**. 
3. In the **Delete URL customization** dialog box, click **Delete**.


## Adding and removing notes

You can add and assign notes to agreement records, agreement lines, and e-resources (internal KB only). Assigning a note means you are reusing a previously created note.


### Adding a new note to an agreement



1. [Find the agreement](#searching-for-agreements) to which you want to add a note and select it.
2. In the **Agreement details** pane, click **Notes > New**.
3. In the **New note** window, select the **Note type** from the drop-down list. Note types are created in the Settings app. For more information, see Settings > Notes.
4. Enter a **Note title** in the box.
5. (Optional) Enter any **Details** about the note in the box.
6. Click **Save & close**. The note is saved and appears in the Notes section in the agreement details pane.


### Assigning an existing note to an agreement



1. [Find the agreement](#searching-for-agreements) to which you want to add a note and select it.
2. In the **Agreement details** pane, click **Notes > Assign / Unassign**.
3. In the **Assign / Unassign note** dialog, search for a note using the search bar in the Search & filter pane, or select a **Note type** from the drop-down list. You can also filter by **Note assignment status**.
4. Select the checkbox next to the note you want to assign to the agreement and click **Save.** The note is saved and appears in the Notes section in the agreement details pane.


### Editing an agreement note



1. [Find the agreement](#searching-for-agreements) with the note you want to edit and select it.
2. In the **Agreement details** pane, click **Notes**.
3. Find the note you want to edit, and click **Edit** at the bottom of the Title and details section of the note.
4. In the **Edit: note** window, make your desired changes to the note.
5. Click **Save & close**. The note is saved.


### Removing a note on an agreement



1. [Find the agreement](#searching-for-agreements) with the note you want to remove and select it.
2. In the **Agreement details** pane, click **Notes**.
3. Click the note you want to remove.
4. In the **Note** window, click **Actions > Delete**.
5. In the **Delete note** dialog, click **Delete**. The note is deleted and removed from any records to which it was attached.


### Adding a note to an agreement line



1. [Find the agreement](#searching-for-agreements) with the agreement line to which you want to add a note and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to edit.
4. In the **Agreement lines** pane, under **Notes**, click **New**.
5. Follow steps 3-6 under Adding a new note to an agreement.


### Assigning an existing note to an agreement



1. [Find the agreement](#searching-for-agreements) with the agreement line to which you want to add a note and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to edit.
4. In the **Agreement lines** pane, under **Notes**, click **Assign / Unassign**.
5. Follow steps 3-4 under [Assigning an existing note to an agreement](#assigning-an-existing-note-to-an-agreement).


### Editing an agreement line note



1. [Find the agreement](#searching-for-agreements) with the agreement line with the note you want to edit and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to edit.
4. In the **Agreement lines** pane, under **Notes**, find the note you want to edit, and click **Edit** at the bottom of the Title and details section of the note.
5. In the **Edit: note** window, make your desired changes to the note.
6. Click **Save & close**. The note is saved.


### Removing a note from an agreement line



1. Find the agreement with the agreement line with the note you want to remove and select it.
2. In the **Agreement details** pane, click **Agreement lines**.
3. In the **Agreement lines** table, select the agreement line you want to edit.
4. In the **Agreement lines** pane, under **Notes**, find the note you want to remove and select it.
5. In the **Note** window, click **Actions > Delete**.
6. In the **Delete note** dialog, click **Delete**. The note is deleted and removed from any records to which it was attached.


### Dashboard widgets for the Agreements app

The Dashboard app is designed to enable a personalized view of key information from across FOLIO apps at a glance. In its first release (included in the Juniper flower release), the Dashboard includes the ability to display information from the Agreements and Licenses applications.

The Agreements app comes with two dashboard widgets ("ERM Agreements" and "ERM Agreement Jobs"). There are examples of how you can use these two 
widget definitions to achieve a wide range of outcomes in the Example widget configurations documentation.
