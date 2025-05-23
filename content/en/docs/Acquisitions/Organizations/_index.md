---
title: "Organizations"
linkTitle: "Organizations"
date: 2025-05-05
weight: 40
tags: ["parenttopic"]
---

The Organizations app allows you to manage information about organizations associated with your library. Organization records are a place where you can store information about an organization, including contact information, websites, interfaces, and accounts. The organizations you create are shared with the acquisitions and electronic resources management areas of FOLIO in the following apps: Orders, Invoices, Receiving, Agreements, Licenses, and eUsage.

Definition of terms related to the Organizations app:



*   **Acquisition units.** An additional layer you can add to acquisitions records that restricts a user’s ability to interact with those records unless they have been assigned to that unit. For example, you may create acquisition units to represent the different libraries within your library system. Units are defined and determined by your library in the Settings app. See [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/) for more information.
*   **Organization.** Any institution with which your library interacts.  An organization may or may not be an institution from which you purchase materials.
*   **Vendor.** Any institution from which your library purchases materials.


## Capabilities

The capabilities listed below allow you to interact with the Organizations app and determine what you can or cannot do within the app. You can assign capabilities to users via user roles. If none of these capabilities are assigned to a user, they are unable to see the Organizations app or any related information.

It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities.

|**Permission Display name (OKAPI)** | **Resource (EUREKA)** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Organizations: Assign acquisition units to new organization.** | **UI-Organizations AcqUnits** | procedural | execute | This capability allows the user to assign acquisition units to the organization when creating a new record.|
|**Organizations: Can view privileged donor information.** | **UI-Organizations Privileged-Contacts** | data | view | This capability allows the user to view the information in the Privileged donor information accordion that appears on Organization records with the donor designation.|
|**Organizations: Can view, create, edit, delete privileged donor information.** | **UI-Organizations Privileged-Contacts** | data | edit | This capability allows the user to create, edit, and delete the information contained in the Privileged donor information accordion that appears on Organization records with the donor designation. Note: This capability must always be assigned in conjunction with either the **UI-Organizations** capability (either **create** or **delete** action.|
|**Organizations: Integration usernames and passwords: view.** | **UI-Organizations Integrations Creds** | data | view | This capability allows the user to view the usernames and passwords that appear in the Integration details accordion FTP section.|
|**Organizations: Integration usernames and passwords: view, edit.**| **UI-Organizations Integrations Creds** | data | edit | This capability allows the user to view and edit the usernames and passwords that appear in the Integration details accordion FTP details section.|
|**Organizations: Interface usernames and passwords: view.** | **UI-Organizations Creds** | data | view | This capability allows the user to view the usernames and passwords that appear in the Interface section.|
|**Organizations: Interface usernames and passwords: view, edit, create, delete.** | **UI-Organizations Creds** | data | manage | This capability allows the user to create, edit, and delete the usernames and passwords that appear in the Interface section. Note: This capability must always be assigned in conjunction with either the **UI-Organizations** capability (either **create** or **delete** action.|
|**Organizations: Manage acquisition units.** | **UI-Organizations AcqUnits** | data | manage | This capability allows the user to change the assignment of acquisition units for the organization when editing a record.|
|**Organizations: View.** | **UI-Organizations** | data | view | This capability allows the user to search and view organization records and settings. The user can also access Contacts and Interfaces but cannot access Interface usernames and passwords.|
|**Organizations: View and edit banking information.** | **UI-Organizations Banking-Information**| data | edit | This capability allows the user to view and edit the information contained in the Banking information accordion of an Organization record with a vendor designation. Note: Banking information must also be enabled in [Settings > Organizations > Banking information](../../settings/settings_organizations/settings_organizations/#settings--organizations--banking-information).|
|**Organizations: View banking information.** | **UI-Organizations Banking-Information** | data | view | This capability allows the user to view the information contained in the Banking information accordion of an Organization record with a vendor designation. Note: Banking information must also be enabled in [Settings > Organizations > Banking information](../../settings/settings_organizations/settings_organizations/#settings--organizations--banking-information).|
|**Organizations: View, edit.** | **UI-Organizations** | data | edit | This capability allows the user to edit and view organizations. The user can also access Contacts, but they cannot access Interface usernames and passwords.|
|**Organizations: View, edit and create banking information.** | **UI-Organizations Banking-Information** | data | create | This capability allows the user to view and edit information contained in the Banking information accordion of an Organization record with a vendor designation, as well as create new entries. Note: Banking information must also be enabled in [Settings > Organizations > Banking information](../../settings/settings_organizations/settings_organizations/#settings--organizations--banking-information).|
|**Organizations: View, edit, create.** | **UI-Organizations** | data | create | This capability allows the user to create, edit, and view organizations. The user can also access Contacts, but they cannot access Interface usernames and passwords.|
|**Organizations: View, edit, create and delete banking information.** | **UI-Organizations Banking-Information** | data | delete | This capability allows the user to view, edit, and delete information contained in the Banking information accordion of an Organization record with a vendor designation, as well as create new entries. Note: Banking information must also be enabled in [Settings > Organizations > Banking information](../../settings/settings_organizations/settings_organizations/#settings--organizations--banking-information).|
|**Organizations: View, edit, delete.** | **UI-Organizations** | data | delete | This capability allows the user to view, edit, and delete organizations. The user can also access Contacts, but they cannot access Interface usernames and passwords.|



## Keyboard shortcuts
Keyboard shortcuts allow you to perform actions in this app using the keyboard.  See [Platform essentials > Keyboard shortcuts](../../platform-essentials/keyboard-shortcuts/keyboardshortcuts/) for more information.


## Creating an organization

When creating an organization, you either create it as a general organization or specifically as a vendor. If you create the organization as a vendor, you can add additional vendor-related information. For more information on creating a vendor, see [Creating a vendor](#creating-a-vendor).

1. In the **Organizations** pane, click **New**.

2. In the **Create organization** window, fill in the Summary, Contact information, Contact people, and Interface sections. For more information on the fields and actions available in these sections, see the section descriptions below.

3. Once you have included all of the information you want about the organization, click **Save & close**. The organization is saved and added to the Organizations pane.


### Summary



*   **Name (required).** The name of the organization.
*   **Code (required).** A unique identifier for the organization. Note: You cannot have duplicate vendor codes. The codes for each organization must be different. If your institution has [enabled the number generator for the Organizations app](../../settings/settings_organizations/settings_organizations/#settings--organizations--number-generator-options) and your user has the applicable capabilities, you may use the number generator to generate the code. For more information, see [Using Number Generators Within Apps](../../settings/settings_service_interaction/settings_service_interaction).
*   **Accounting code.** The accounting code used by your library in your payment system in reference to the organization.
*   **Organization status (required).** Select an organization status: Active, Inactive, or Pending. The status you select here is evaluated by the Orders and Invoices apps. Orders can only be opened and invoices can only be paid if the organization is a vendor with an Active status. You may want to use the Pending status to signify that the organization record is a draft.
*  **Type.**  Select one or more organization types.  See [Settings > Organizations > Creating a new type](../../settings/settings_organizations/settings_organizations/#creating-a-new-type) for more information.
*   **Default language.** Select the organization’s default language.
*   **Acquisition units.** Select the Acquisition units you want to apply to the organization record. See [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/) for more information.
*   **Description.** Enter a description of the organization.
*   **Donor.** If you wish to include donor information on the Organization record, select the **Donor** checkbox. See [Privileged donor information](#privileged-donor-information) for more information.
*   **Vendor.** If you are creating a vendor organization, select the **Vendor** checkbox . See [Creating a vendor](#creating-a-vendor) for more information.
*   **Alternative names.** Alternative names used by the organization, such as abbreviations or prior names.


#### Adding an alternative name

Note: Adding an alternative name is optional, but if you click **Add alternative names**, you must enter an **Alias** or [delete the alternative name](#deleting-an-alternative-name) in order to save the organization record.

1. Click **Add alternative names**.

2. Enter the organization’s **Alias** in the box.

3. Optional: Enter a **Description** about the alias in the box.

4. Repeat as needed. The alternative name saves once you save the organization.


#### Deleting an alternative name

1. Find the Alternative name you want to delete.

2. Click the **trash can icon**. The alternative name is deleted and is removed from the record once you save the organization.


### Contact information

The Contact information section stores organizational contact information that is not specific to individual people at the organization. You can add contact information for specific individuals in the [Contact people](#contact-people) section, which is described below.

Categories for contact information are configured in the Settings app. If you assign a category to any type of contact information you enter in this section, the contact information is then sorted by that category when you view the organization.



*   **Address.** The addresses associated with the organization. You can add multiple addresses. 
*   **Phone numbers.** The phone numbers associated with the organization. You can add multiple phone numbers.
*   **Email address**. The email addresses associated with the organization. You can add multiple email addresses.
*   **URLs.** The URLs associated with the organization. You can add multiple websites or FTP connections.


#### Adding an address

1. Click **Add address**.

2. Fill in the address information.

3. Repeat as needed. The address saves once you save the organization. Note: If you are adding multiple addresses, select the **Use as primary address** checkbox at the top of the organization’s primary address.  The primary address is included in the invoice voucher extract.  See [Invoices > Voucher information](../invoices/#voucher-information) for more information.


#### Deleting an address

1. Find the address you want to delete.

2. Click the **trash can icon**. The address is deleted and is removed from the record once you save the organization.


#### Adding a phone number

1. Click **Add phone number**.

2. Enter the Phone number in the box.

3. Optional: Select the **Type** of phone number from the drop-down list: Office, Mobile, Fax, or Other.

4. Optional: Select the **Language** spoken at that number from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed. The phone number saves once you save the organization. Note: If you are adding multiple numbers, select the **Use as primary phone** checkbox at the top of the organization’s primary number.


#### Deleting a phone number

1. Find the phone number you want to delete.

2. Click the **trash can icon**. The phone number is removed and is deleted once you save the organization.


#### Adding an email address

1. Click **Add email**.

2. Enter the **Email address** in the box.

3. Optional: Enter a **Description** of the email in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed.The email address saves once you save the organization. Note: If you are adding multiple email addresses, select the **Use as primary email** checkbox at the top of the organization’s primary email address.


#### Deleting an email address

1. Find the email address you want to delete.

2. Click the **trash can icon**. The email address is removed and is deleted once you save the organization.


#### Adding a URL

The URL can be a website or FTP link.

1. Click **Add URL**.

2. Enter the **URL** in the box.

3. Optional: Enter a **Description** of the URL in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the URL.

6. Repeat steps 1-5 as needed. The URL saves once you save the organization. Note: If you are adding multiple URLs, select the **Use as primary URL** checkbox at the top of the organization’s primary URL.


#### Deleting a URL

1. Find the URL you want to delete.

2. Click the **trash can icon**. The URL is removed and is deleted once you save the organization.


### Contact people


#### Creating a new contact

If you need to create a new contact, see [Creating a contact person](#creating-a-contact-person).


#### Adding an existing contact 

1. Click **Add contact**.

2. In the **Add contacts** dialog, search for the contact you want to add.

3. In the **Search results**, select the **checkbox** next to the contact(s) you want to add. You can add multiple contacts at a time.

4. Click **Save**. The contact(s) appear under the Contact people section. 


#### Deleting a contact

1. Find the contact you want to delete.

2. Click the **x**. The contact is deleted and is removed from the record once you save the organization.


### Interface

An interface is a website, software, or portal that you use to manage orders or gather statistics from the organization.


#### Creating a new interface

For more information, see [Creating an interface](#creating-an-interface).


#### Adding an existing interface

1. Click **Add interface**.

2. In the **Add interfaces** dialog, search for the interface you want to add.

3. In the **Search results**, select the checkbox next to the interface(s) you want to add. You can add multiple interfaces at a time.

4. Click **Save**. The interface(s) appear under the Interface section.


#### Removing an interface from the organization record

1. Find the interface you want to delete.

2. Click the **x**. The interface is deleted and is removed from the record once you save the organization.

### Privileged donor information
This accordion appears on any Organization record with the **Donor** checkbox selected. Only staff members with authorization to view data in this accordion will be able to access this information. Donors can be associated with both fund records and purchase order lines.

#### Creating a new donor

For more information, see [Creating a donor](#creating-a-donor).


#### Adding an existing donor

1. Click **Add donor**.

2. In the **Add contacts** dialog, search for the donor you want to add.

3. In the **Search results**, select the checkbox next to the donor(s) you want to add. You can add multiple donors at a time.

4. Click **Save**. The donor(s) appear under the Privileged donor information section.


#### Removing a donor from the organization record

1. Find the donor you want to delete.

2. Click the **x**. The donor is deleted and is removed from the record once you save the organization.


## Creating a vendor

1. In the **Organizations** pane, click **New**.

2. In the **Create organization** window, in the **Summary** section, select the **Vendor** checkbox. Vendor sections appear.

3. Continue filling in the Summary section. Fill in the Contact information, Contact people, Interface, Vendor information, Vendor terms, and Accounts sections. For more information on the fields and actions available in these sections, see the section descriptions below.

3. Once you have included all of the information you want about the vendor, click **Save & close**. The vendor is saved and added to the Organizations pane.

4. In the newly created Organization record’s detail pane, see the accordion sections to add **Notes** and **Integration details**.  For more information, see [Adding a note to an organization](#adding-a-note-to-an-organization) and [Adding integration details to a vendor organization](#adding-integration-details-to-a-vendor-organization).


### Summary

For more information, see [Summary](#summary).


### Contact information

For more information, see [Contact information](#contact-information).


### Contact people

For more information, see [Contact people](#contact-people).


### Interface

For more information, see [Interface](#interface).


### Vendor information

The information that you enter under Vendor information sets some of the defaults that appear when you apply the vendor to an order or invoice.



*   **Payment method.** The payment method that you want to appear as the default payment method for the vendor on an invoice. See [Invoices > Extended information](../invoices/#extended-information) for more information.
*   **Vendor currencies.** The currencies accepted by the vendor.
*   **Expected activation interval.** The standard activation period for the vendor, in days. Note: The interval you enter here is used in the Activation due field in the E-resources details section of an order line associated with the vendor. For example, if you set the interval to 365, the Activation due field is populated with the date that falls one year from the date the order line is created.
*   **Expected invoice interval.** The standard invoice interval for the vendor, in days. Currently, this information does not display on invoices.
*   **Claiming interval.** The standard claim period for the vendor, in days. This value will carry over to the purchase order lines (POL) associated with this vendor. The default value may be overridden on an individual POL or receiving title. This interval represents how long after a piece's expected receipt date it should be marked 'Late' if the piece is not received.
*   **Expected receipt interval.** The standard period during which ordered items are received from the vendor, in days.
*   **Discount percent.** The discount negotiated with the vendor, as a percent value. When creating an order line for an order with the vendor, this value appears as the default in the discount field.
*   **Renewal activation interval.** The standard renewal activation period for this vendor, in days.
*   **Subscription interval.** The standard subscription period for the vendor, in days.
*   **Export to accounting.** To indicate that invoices for the vendor should create voucher records for export to an external accounts payable system, select the **Export to accounting** checkbox. When creating an invoice for the vendor, the value on the Organization record sets the default value for the invoice Export to accounting field.


### Tax

The information that you enter under Tax sets the defaults that appear when you apply the vendor to an order.



*   **Tax ID.** The Federal Tax Identification Number for the vendor. This is also known as an Employer Identification Number (EIN) and is used to identify a business entity.
*   **Tax percentage.** The standard tax rate for the vendor. For vendors liable for a value added tax (VAT), the percentage value can be stored here for reference.
*   **Liable for VAT.** To indicate that the vendor is liable for value-added tax (VAT), select the **Liable for VAT** checkbox.


### Vendor terms

Vendor terms are the summary of an agreement with the vendor. The agreements may be acquisitions/fulfillment-related or e-resource-related. The values entered here do not appear on orders or invoice records.

Note: Adding vendor terms is optional, but if you click **Add**, you must add a **Name** or delete the vendor term in order to save the organization record.


#### Adding a vendor term

1. Click **Add**.

2. Enter the **Name** of the term in the box.

3. Optional: Enter or select the **Discount %** in the box.

4. Optional: Enter a **Reference URL** in the box.

5. Optional: Enter any **Notes** about the agreement in the box.

6. Repeat steps 1-5 as needed. Terms are saved once you save the vendor.


#### Deleting a vendor term

1. Find the vendor term you want to delete.

2. Select the **trash can icon**. The term is removed and is deleted once you save the vendor.




### Accounts

The account section describes your library accounts with a vendor used for ordering materials.

Note: Adding an account is optional, but if you click **Add**, you must fill in the required fields or delete the account in order to save the organization record.


#### Adding an account

1. Click **Add**.

2. Enter the account **Name** in the box.

3. Enter the **Account number** in the box. This number is usually assigned by the vendor. Note: The account number entered here appears as a default value on any orders or invoices for the vendor. If you have multiple accounts set up in this section, the first account number displays as the default on orders and invoices, but you can select the appropriate number from a drop-down list that contains all the account numbers associated with the vendor.

4. Optional: Enter a **Description** of the account in the box.

5. Optional: Enter the **Accounting code** in the box.

6. Optional: Select the **Payment method** from the drop-down list.

7. Select the **Account status** from the drop-down list.

8. Optional: Enter **Contact** info in the box.

9. Optional: Enter the **Library code** in the box. This is the library-supplied code for the account with the vendor.

10. Optional: Enter the **Library EDI code** in the box.

11. Optional: Enter any **Notes** about the account in the box.

12. Optional: Select any **Acquisition units** from the drop-down list. For more information on acquisition units, see [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/).

13. Repeat steps 1-12 as needed. Accounts are saved once you save the vendor.


#### Deleting an account

1. Find the account you want to delete.

2. Click the **trash can icon**. The account is removed and is deleted once you save the vendor.

### Banking information
This accordion will appear on Organization records where the **Vendor** checkbox is selected, only if activated in [Settings > Organizations > Banking information](../../settings/settings_organizations/settings_organizations/#settings--organizations--banking-information). This section allows storage of banking details to fulfil payments to the associated vendor. Staff users must have authorization to view and interact with the data in this accordion.

#### Adding banking information
1. Click **Add banking information.**
2. Enter the **Bank name.**
3. Enter the **Bank account number.**
4. Enter the **Transit number.**
5. Select an **Address category** from the dropdown menu. The address category is derived from the addresses added in the [Contact information](#contact-information) accordion. The category you select here will determine which address is associated with the banking information.
6. Select an **Account type** from the dropdown menu. Account types are configured in [Settings > Organizations > Account types](../../settings/settings_organizations/settings_organizations/#settings--organizations--account-types).
7. Add notes, if desired.

#### Deleting banking information
1. Find the banking information you want to delete.
2. Click the **trash can icon**. The banking informaton is removed and is deleted once you save the vendor.


## Searching for an organization

You can search for organizations in the **Search & filter** pane. To search for an organization, enter your search terms into the box. Select the **All** drop-down list to search through one of the following fields: 



*   **All.** All fields. This is the default search.
*   **Name.** The name of the organization. 
*   **Code.** A unique identifier for the organization.
*   **Language.** The default language of the organization.  Enter the language code (ex: ‘eng’ or ‘fra’) to search for organizations with this default language.  Entering the language name in this search box will not retrieve results.
*   **Alias.** Alternative names used by the organization, such as abbreviations or prior names.
*   **Accounting code.** The accounting code used by your library in your payment system in reference to the organization.
*   **Tax ID.** Your library’s tax identifier number.
*   **Bank account number.** The bank account number associated with the organization's banking information, if configured.

You can also search for organizations by selecting any of the filters in the **Search & filter** pane. Additionally, you can apply the filters after you perform a search to limit your results. See the sections below for more information.


### Organization status

To filter organizations by their status, select one of the following:



*   **Active.** Organizations currently used by your library.
*   **Inactive.** Organizations previously used by your library.
*   **Pending.** Organizations that are not yet available for use. Pending could indicate that the organization record is not yet complete.


### Types

To search for organizations assigned with specific types, follow these steps:

1. In the **Search & filter** pane, click **Types**.

2. Select the type(s) from the drop-down list. Your results appear in the Organizations pane.


### Tags

To search for organizations assigned with specific tags, follow these steps:

1. In the **Search & filter** pane, click **Tags**.

2. Select the tag(s) from the drop-down list. Your results appear in the Organizations pane.

### Is donor

To filter organizations by whether or not they are a donor, select one of the following:



*   **Yes.** Organizations that are donors (have the Donor checkbox selected).
*   **No.** Organizations that are not donors.

### Is vendor

To filter organizations by whether or not they are a vendor, select one of the following:



*   **Yes.** Organizations that are vendors (have the Vendor checkbox selected).
*   **No.** Organizations that are not vendors.


### Country

To search for organizations with offices in a specific country, follow these steps:

1. In the **Search & filter** pane, click **Country**.

2. Select the country from the drop-down list. Your search results appear in the Organizations pane.


### Languages

To search for organizations that communicate in a specific language, follow these steps:

1. In the **Search & filter** pane, click **Languages**.

2. Select the language from the drop-down list. Your search results appear in the Organizations pane. Note:  This filter may not retrieve all expected records for organizations loaded to FOLIO through an API. This tool is filtering by language name rather than language code.  For records created directly in FOLIO this filter does retrieve the expected records by language.



### Payment method

To filter organizations by their default payment method, as indicated in the [Vendor information](#vendor-information) section of a vendor record, select one of the following options:



*   **Cash.** Default payment method of cash.
*   **Credit card.** Default payment method of credit card.
*   **EFT.** Default payment method of electronic funds transfer.
*   **Deposit account.** Default payment method of deposit account.
*   **Physical check.** Default payment method of physical check.
*   **Bank draft.** Default payment method of bank draft.
*   **Internal transfer.** Default payment method of internal transfer.
*   **Other.** Default payment method of other.


### Acquisitions unit

To search for organizations to which one or more acquisitions units have been assigned, follow these steps:

1. In the **Search & filter** pane, click **Acquisitions unit**.

2. Select the acquisitions unit from the drop-down list. The search results appear in the Organizations pane.

### Created by

To search for organizations created by a specific user, follow these steps:

1. In the **Search & filter** pane, click **Created by**.

2. Click **Find User**.

3. In the **Select User** dialog, search for the user.

4. Select the user you want to filter by. The search results appear in the Organizations pane.


### Date created

To search for organizations based on the date they were created, follow these steps:

1. In the **Search & filter** pane, click **Date created**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. Click **Apply**. The search results appear in the Organizations pane.

### Updated by

To search for organizations updated by a specific user, follow these steps:

1. In the **Search & filter** pane, click **Updated by**.

2. Click **Find User**.

3. In the **Select User** dialog, search for the user.

4. Select the user you want to filter by. The search results appear in the Organizations pane.


### Date updated

To search for organizations based on the date they were created, follow these steps:

1. In the **Search & filter** pane, click **Date updated**.

2. Enter a start date in the **From** box and an end date in the **To** box.

3. Click **Apply**. The search results appear in the Organizations pane.


## Viewing organization details

Once you search for an organization, the following information appears in the Organizations pane:



*   **Name.** The name of the organization.
*   **Code.** A unique identifier for the organization.
*   **Description.** A description of the organization.
*   **Organization status.** The status of the organization: Active, Inactive, or Pending.
*   **Vendor.** Whether the organization is a vendor or not.

In the search results, click on an organization to view it. The Organization details pane displays with additional information about the organization in the following accordion sections:

*   **Summary.** See [Summary](#summary).
*   **Notes.** See [Adding a note to an organization](#adding-a-note-to-an-organization).
*   **Contact information.** See [Contact information](#contact-information).
*   **Contact people.** See  [Contact people](#contact-people).
*   **Interface.**  See [Interface fields](#interface-fields).
*   **Privileged donor information.** See [Privileged donor information] (#privileged-donor-information).
*   **Vendor information.**  See [Vendor information](#vendor-information).
*   **Vendor terms.**  See [Vendor terms](#vendor-terms). 
*   **Integration details.**  See [Adding integration details to a vendor organization](#adding-integration-details-to-a-vendor-organization).
*   **Accounts.**  See [Accounts](#accounts).
*   **Banking information.** See [Banking information](#banking-information).
*   **Agreements.**  The agreements section displays a table list containing the following information for all agreements linked to the organization:

*   **Agreement name.**  The title of the agreement record.
*   **Period start.**  The date the agreement period starts.
*   **Period end.**  The date the agreement period ends.
*   **Agreement status.** The status of the agreement: Active, Closed, Draft, In negotiation, Requested.



## Editing an organization

1. [Find the organization you want to edit](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Actions > Edit**.

3. Edit the organization.

4. Click **Save & close**. The organization is saved and updated.


### Changing a vendor to an organization

Note: Changing a vendor to an organization removes all Vendor information, Vendor terms, Accounts, and Banking information from the record.

1. [Find the organization you want to edit](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, clear the **Vendor** checkbox.

3. In the Confirm vendor data deletion dialog, click **Confirm**. The Vendor information, Vendor terms, Accounts, and Banking information sections are removed.

4. Make any additional changes to the organization.

5. Click **Save & close**. The organization is saved and updated.


## Deleting an organization

The system allows you to delete a vendor organization even if there are orders or invoices associated with the vendor.  If you try to take actions such as adding a PO line or paying an invoice associated with the deleted vendor you will see error messages explaining that that vendor has been deleted.   

1. [Find the organization you want to delete](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Actions > Delete**.

3. In the **Delete organization** dialog, click **Delete**. The organization is deleted and a confirmation message appears.

## View export log

To view a log of orders exported to a vendor organization that is set up for EDI integration, follow these steps:

1. [Find the organization for which you want to view an export log](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Actions > View export log**.

3. The Export Manager app opens with the Search & Filter pane set to view exports related to the selected vendor organization.  See the [Export Manager documentation](../../export-manager/#viewing-export-jobs) for more information about viewing export jobs.


## Adding a tag to an organization

1. [Find the organization you want to tag](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click the **tag icon**.

3. In the **Tags** pane, either select a tag from the box or enter a tag. 

4. Click the **X** on the **Tags** pane to close the pane and save the tag. The tag number updates to the number of tags applied to the organization.


## Adding a note to an organization

1. [Find the organization to which you want to add a note](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click **Notes > New**.

3. In the **New note** window, select the **Note type** from the drop-down list. Note types are created in the Settings app. For more information, see Settings > Notes.

4. Enter a **Note title** in the box.

5. Optional: Enter any **Details** about the note in the box.

6. Click **Save & close**. The note is saved and appears in the Notes section in the Organization details pane.


## Adding integration details to a vendor organization

This section houses additional configuration to export orders or claims to a vendor. Orders may be transmitted via FTP in EDI fomrat. Claims may be transmitted via FTP or file download in either CSV or EDI format.

To add information about one or more integrations for a vendor organization, follow these steps:

1. [Find the organization to which you want to add an integration](#searching-for-an-organization) and select it.

2. In the **Organization details** pane, click on **Integration details** to expand the accordion section.

3. Click **Add integration**. The **Create integration** window opens.

4. Add information to the Integration information, EDI configuration, FTP details, and Scheduling sections. For more information on the fields and actions available in these sections, see the section descriptions below.

5. Click **Save & close**. The integration is saved and appears in the Integration details section in the Organization details pane.




### Integration information

*   **Integration name (required).** The name for this integration.
*   **Description.** A description of this integration.
*   **Default integration.** Select this checkbox if your organization doesn’t have any account numbers. This indicates that any order tagged for export that is not related to a specific account for this organization should follow this default configuration.
*   **Integration type (required).** Select Claiming or Ordering.
*   **Transmission method (required).** Select File download or FTP. Please note: If the selected integration type is 'Ordering', FTP is the only supported transmission method.
*   **File format (required).** Select CSV or EDI. Please note: If the selected integration type is 'Ordering', EDI is the only supported file format.
*   **Account numbers (required).** All account numbers created in **Vendor account** section of the organization are listed.  Click on all vendor account numbers to be included in this configuration.  To select multiple account numbers for this configuration, use shift+click. When you move your cursor to another field you will see the highlight persist on the selected account number(s).

### EDI configuration


*   **Automate order export for acquisition methods.**   All order acquisition methods are listed. To automatically export orders for this vendor using specific order acquisitions methods, click on the acquisition method name.  When creating orders, you can override this default behavior by checking the [Manual](../orders/#purchase-order) checkbox on the purchase order.  To select multiple acquisition methods to export automatically, use shift+click. When you move your cursor to another field you will see the highlight persist on the selected acquisition methods.
*   **Vendor EDI code (required).** The vendor identifier for EDI transactions
*   **Vendor EDI type.** Select one of the Vendor EDI types, which designates the type of identifier used as the vendor identifier: 014/EAN, 31B/US-SAN, 091/Vendor-assigned, or 092/Customer-assigned.
*   **Library EDI code (required).** The library identifier for EDI transactions
*   **Library EDI type.** Select one of the Library EDI types, which designates the type of identifier used as the library identifier: 014/EAN, 31B/US-SAN, 091/Vendor-assigned, or 092/Customer-assigned.
*   **EDI naming convention.** The naming convention that sets the expected structure to be used for outgoing FOLIO EDI files. This is currently a static value, using system-defined tokens. The naming convention will be configurable in a future release.
*   **Send account number.** If you send your account number with orders or invoices, select this checkbox. If selected, the account number is required for the PO/POL and is included in the EDI order file.
*   **What messages are expected for this vendor?** If your library expects to send EDI orders to the vendor, select the **Orders** checkbox. If your library expects to receive EDI invoices from the vendor, select the **Invoices** checkbox. Please note: EDI invoices are imported using the Data import app and do not require this integration configuration.
*   **Notes.** Notes about the integration details for this vendor.



### FTP details



*   **EDI FTP.** Select FTP format in which the library expects to transact with the vendor: SFTP or FTP.
*   **FTP mode.** Select the transmission mode the library expects to use with the vendor: ASCII or Binary.
*   **Server address.** The address for the vendor’s FTP server. Please note: this field is required if the selected transmission method is FTP.
*   **FTP connection mode.** Select the connection mode: Active or Passive.
*   **Username.** The username for the FTP, if a login username is required for this vendor. 
*   **Password.** The password for the FTP, if a login password is required for this vendor. The password is automatically hidden. Click **Show** to display the password. Click **Hide** to stop displaying the password.
*   **FTP port.** The FTP port number. Please note: this field is required if the selected transmission method is FTP.
*   **Order directory.** The subdirectory where orders should be placed, if different from the main FTP directory for this vendor. Ex: /directory.
*   **Invoice directory.** The subdirectory where invoices should be retrieved, if different from the main FTP directory for this vendor. Ex: /directory.
*   **Notes.** Notes about the FTP details for this vendor integration.



### Scheduling
Please note: this accordion is only visible if the selected integration type is Ordering.

*   **Schedule EDI.** If you want to schedule the EDI, select the **Schedule EDI** checkbox. This will make the following fields appear.
*   **Schedule period.**  The period between automated exports to the vendor.  Choose from Hourly, Daily, Weekly, or Monthly.
*   **Schedule frequency (required).**  If you choose a schedule period of Hourly, Daily, or Weekly, the schedule frequency field appears.  Enter the numeric value for the hourly, daily, or weekly frequency of this scheduled integration.
*   **Date.** If you choose a schedule period of Daily, the date field appears.  Use the calendar function to select the start date for this schedule.
*   **Time (required).**  Click on this field to view an hour and time select list.  Choose the scheduled time for this automated export.
*   **S M T W Th F S.**  If you choose a schedule period of Weekly, the day of the week checkboxes appear. Choose the days for this weekly automated export.
*   **Day (required).** If you choose a schedule period of monthly, enter the day of the month the automatic export should occur.




## Creating a contact person

Note: If you need to create a new contact, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the new contact process. Creating a new contact takes you out of the organization window.

1. Click **Add contact**.

2. In the **Add contacts** dialog, click **New**. If you have not saved your organization information, you are prompted to do so before continuing.

3. In the **Create contact** window, fill in the fields in the Name, Emails, Phone numbers, URLs, and Addresses sections. See below for more information.

4. Click **Save & close**. A confirmation message appears and the contact is saved.

5. A new accordion is added to the contact person detail pane containing the following information:

*   **Record last updated.**  Date and time of the last record update.
*   **Source.**   Name of the user who last updated the record.
*   **Record created.** Date and time of record creation.
*   **Source.**   Name of the user who last created the record.


##### Name



*   **Prefix.** Title of the contact.
*   **Last name.** The surname of the contact.
*   **First name.** The given name of the contact.
*   **Status.** Select the status of the contact from the drop-down list: Active or Inactive.
*   **Language.** The primary language spoken by the contact.
*   **Categories.** Select any categories from the drop-down list that describe the contact. Categories are configured in the Settings app. See [Settings > Organizations > Categories](../../settings/settings_organizations/settings_organizations/#settings--organizations--categories) for more information.
*   **Notes.** Any notes related to the contact.


##### Emails


###### Adding an email address

1. Click **Add email**.

2. Enter the **Email address** in the box.

3. Optional: Enter a **Description** of the email in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed.The email address saves once you save the contact. Note: If you are adding multiple emails, click **Primary** to indicate the contact’s primary email address.  The **Primary** email will display as the first result.


###### Deleting an email address

1. Find the email address you want to delete.

2. Click the **trash can icon**. The email address is removed and is deleted once you save the contact.


##### Phone numbers


###### Adding a phone number

1. Click **Add phone number**.

2. Enter the **Phone number** in the box.

3. Optional: Select the **Type** of number from the drop-down list: Office, Mobile, Fax, or Other.

4. Optional: Select the **Language** spoken at that number from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed. The phone number saves once you save the contact. Note: If you are adding multiple phone numbers, click **Primary** to indicate the contact’s primary phone number. The **Primary** phone number will display as the first result.


###### Deleting a phone number

1. Find the phone number you want to delete.

2. Click the **trash can icon**. The phone number is removed and is deleted once you save the contact.


##### URLs


###### Adding a URL

The URL can be a website or FTP link.

1. Click **Add URL**.

2. Enter the **URL** in the box.

3. Optional: Enter a **Description** of the URL in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the URL.

6. Repeat steps 1-5 as needed. The URL saves once you save the contact. Note: If you are adding multiple URLs, click **Primary** to indicate the contact’s primary URL.  The **Primary** URL will display as the first result.


###### Deleting a URL

1. Find the URL you want to delete.

2. Click the **trash can icon**. The URL is removed and is deleted once you save the contact.


##### Addresses


###### Adding an address

1. Click **Add address**.

2. Fill in the address information.

3. Repeat steps 1-2 as needed. The address saves once you save the contact. Note: If you are adding multiple addresses, click **Primary** to indicate the contact’s primary address. The **Primary** address will display as the first result.


###### Deleting an address

1. Find the address you want to delete.

2. Click the **trash can icon**. The address is deleted and is removed from the record once you save the contact.


## Editing a contact person

Note: If you need to edit a contact, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the new contact process. Editing contact takes you out of the organization window.

1. [Add the contact you want to edit to Contact people](#adding-an-existing-contact) if you have not already.

2. Click the contact you want to edit. If you have not saved your organization information, you are prompted to do so before continuing.

3. In the contact window, click **Actions > Edit**.

4. Edit the contact.

5. Click **Save & close**. A confirmation message appears and the contact is updated.



## Unassigning a contact person

See [Deleting a contact](#deleting-a-contact) for an alternate way to remove a contact from an organization.

1. [Add the contact you want to unassign to Contact people](#creating-a-contact-person) if you have not already.

2. Click the contact you want to unassign. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Unassign**.

4. In the **Unassign from organization** dialog, click **Confirm**. A confirmation message appears, the contact is removed from the organization, and the organization window appears.


## Deleting a contact person

Deleting a contact person removes that person from your library’s list of contacts. If you only need to remove a contact from an organization record, see [Deleting a contact](#deleting-a-contact-person).

1. [Add the contact you want to delete to Contact people](#creating-a-contact-person) if you have not already.

2. Click the contact you want to delete. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Delete**.

4. In the **Delete contact** dialog, click **Confirm**. The contact is deleted and the organization window appears.


## Creating an interface

Note: If you need to create a new interface, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the new interface process. Creating an interface takes you out of the organization window.

1. Click **Add interface**.

2. In the **Add interfaces** dialog, click **New**. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the **Create interface** window, fill in the fields. See below for more information.

4. Click **Save**. A confirmation message appears and the interface is saved.


### Interface fields



*   **Type.** The type of interface you are adding: Admin, End user, Reports, Orders, Invoices, or Other.
*   **Name.** The name of the interface.
*   **URI.** The URI of the interface.
*   **Username.** The username needed to log into the interface. 
*   **Password.** The password needed to log into the interface. Click **Show** to display the password. Click **Hide** to stop displaying the password.
*   **Notes.** Any notes about the interface.
*   **Available.** Select the **Available** checkbox to indicate whether statistics are available through this interface.
*   **Delivery method.** Select the statistics’ **Delivery method** from the drop-down list: Online, FTP, Email, or Other.
*   **Statistics format.** Select the statistics’ **Statistics format** from the drop-down list: Counter, Delimited, Excel, PDF, ASCII, HTML, or Other.
*   **Locally stored.** The location of the statistics if they are locally stored.
*   **Online location.** The online location of the statistics. For example, a vendor website.
*   **Statistics notes.** Any notes about the statistics.


## Editing an interface

Note: If you need to edit an interface, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the new interface process. Editing an interface takes you out of the organization window.

1. [Add the interface you want to edit to the Interface section](#adding-an-existing-interface) if you have not already.

2. Click the interface you want to edit. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Edit**.

4. Edit the interface.

5. Click **Save**. A confirmation message appears and the interface is updated.


## Unassigning an interface

See [Deleting an interface](#deleting-an-interface) for an alternate way to remove an interface from an organization.

1. [Add the interface you want to unassign to the Interface section](#adding-an-existing-interface) if you have not already.

2. Click the interface you want to unassign. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Unassign**.

4. In the **Unassign from organization** dialog, click **Confirm**. A confirmation message appears, the contact is removed from the organization, and the organization window appears.


## Deleting an interface

Deleting an interface removes it from your library’s list of interfaces. If you only need to remove an interface from an organization record, see Deleting an interface.

1. Add the interface you want to delete to the Interface section if you have not already.

2. Click the interface you want to delete. If you have not saved your organization information, you will be prompted to do so before continuing.

3. In the contact window, click **Actions > Delete**.

4. In the **Delete interface** dialog, click **Confirm**. The contact is deleted and the organization window appears.

## Creating a donor

Note: If you need to create a new donor, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the new donor process. Creating a new donor takes you out of the organization window.

1. Click **Add donor**.

2. In the **Add contacts** dialog, click **New**. If you have not saved your organization information, you are prompted to do so before continuing.

3. In the **Create contact** window, fill in the fields in the Name, Emails, Phone numbers, URLs, and Addresses sections. See below for more information.

4. Click **Save & close**. A confirmation message appears and the contact is saved.

5. A new accordion is added to the donor detail pane containing the following information:

*   **Record last updated.**  Date and time of the last record update.
*   **Source.**   Name of the user who last updated the record.
*   **Record created.** Date and time of record creation.
*   **Source.**   Name of the user who last created the record.


##### Name



*   **Prefix.** Title of the donor.
*   **Last name.** The surname of the donor.
*   **First name.** The given name of the donor.
*   **Status.** Select the status of the donor from the drop-down list: Active or Inactive.
*   **Language.** The primary language spoken by the donor.
*   **Categories.** Select any categories from the drop-down list that describe the donor. Categories are configured in the Settings app. See [Settings > Organizations > categories](../../settings/settings_organizations/settings_organizations/#settings--organizations--categories) for more information.
*   **Note.** Any notes related to the donor.


##### Emails


###### Adding an email address

1. Click **Add email**.

2. Enter the **Email address** in the box.

3. Optional: Enter a **Description** of the email in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed.The email address saves once you save the contact. Note: If you are adding multiple emails, click **Primary** to indicate the donor’s primary email address.  The **Primary** email will display as the first result.


###### Deleting an email address

1. Find the email address you want to delete.

2. Click the **trash can icon**. The email address is removed and is deleted once you save the donor.


##### Phone numbers


###### Adding a phone number

1. Click **Add phone number**.

2. Enter the **Phone number** in the box.

3. Optional: Select the **Type** of number from the drop-down list: Office, Mobile, Fax, or Other.

4. Optional: Select the **Language** spoken at that number from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the email address.

6. Repeat steps 1-5 as needed. The phone number saves once you save the donor. Note: If you are adding multiple phone numbers, click **Primary** to indicate the donor’s primary phone number. The **Primary** phone number will display as the first result.


###### Deleting a phone number

1. Find the phone number you want to delete.

2. Click the **trash can icon**. The phone number is removed and is deleted once you save the donor.


##### URLs


###### Adding a URL

The URL can be a website or FTP link.

1. Click **Add URL**.

2. Enter the **URL** in the box.

3. Optional: Enter a **Description** of the URL in the box.

4. Optional: Select a **Language** from the drop-down list.

5. Optional: Select any **Categories** from the drop-down list that describe the URL.

6. Repeat steps 1-5 as needed. The URL saves once you save the donor. Note: If you are adding multiple URLs, click **Primary** to indicate the donor’s primary URL.  The **Primary** URL will display as the first result.


###### Deleting a URL

1. Find the URL you want to delete.

2. Click the **trash can icon**. The URL is removed and is deleted once you save the donor.


##### Addresses


###### Adding an address

1. Click **Add address**.

2. Fill in the address information.

3. Repeat steps 1-2 as needed. The address saves once you save the donor. Note: If you are adding multiple addresses, click **Primary** to indicate the donor’s primary address. The **Primary** address will display as the first result.


###### Deleting an address

1. Find the address you want to delete.

2. Click the **trash can icon**. The address is deleted and is removed from the record once you save the donor.


## Editing a donor

Note: If you need to edit a donor, you should save your progress on the organization you are creating or wait until you have completed entering all organization information before you start the edit donor process. Editing the donor takes you out of the organization window.

1. Click the donor you want to edit. If you have not saved your organization information, you are prompted to do so before continuing.

2. In the contact window, click **Actions > Edit**.

3. Edit the donor.

4. Click **Save & close**. A confirmation message appears and the donor is updated.


## Deleting a donor

Deleting a donor removes that person from your library’s list of donors. 

1. Click the donor you want to delete. If you have not saved your organization information, you will be prompted to do so before continuing.

2. In the donor window, click **Actions > Delete**.

3. In the **Delete contact** dialog, click **Confirm**. The donor is deleted and the organization window appears.

## Viewing organization version history

1. [Search for the organization you want to view](#searching-for-an-organization) and select it.
2. In the organization's view pane, click the **clock icon** which is to the right of the tag icon.
4. A fourth pane titled **Version history** opens.  Versions are displayed in a card list sorted by date.  The following information is displayed for each version:  
*   **Source.**  The user who saved this version of the organization record.
*   ***Current Version, Original Version,* or blank.**  This information displays only for the current and original versions of the organization record.
*   **Changes.**  Displays the list of fields that were edited in this version.
4. To view the organization pane for a version, either click on the underlined version date mm/dd/yyyy, hh:mm or the clock icon for the version you want to open.
5. The organization pane displays the data for that version.  Changes from the prior version are highlighted in yellow.
6. To close the version history view, click on the X in the top left of the **Version history** pane.  The fourth pane closes and the organization pane displays the current version.
