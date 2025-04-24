---
title: "Finance"
linkTitle: "Finance"
date: 2025-04-24
weight: 10
tags: ["parenttopic"]
---

**This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may not be aligned with the current release of FOLIO.**

The Finance app allows you to create fund structures and manage money.

Definitions of terms used in the Finance app:

*   **Acquisition units.** An additional layer you can add to acquisitions records that restricts a user’s ability to interact with those records unless they have been assigned to that unit. For example, you may create acquisition units to represent the different libraries within your library system. Units are defined and determined by your library in the Settings app. See [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/) for more information.
*   **Amount allocated.** The amount of money assigned to a fund at the start of a fiscal year. Additional money can also be allocated during the year.
*   **Budget.** A finance record that describes the amount of money available for a fiscal year within a fund that includes a definition of the allowed expenditure percentage and allowed encumbrance percentage. Transfer and allocation transactions are performed against a budget. Expense classes can be assigned to a budget.
*   **Encumbrance.** An amount of money that the library commits to pay to a vendor from a fund’s budget for ordered materials that are invoiced in the future.
*   **Expense class.** A fiscal entity used to track transactions against a specific purpose or function within a Fund. Optional, tenant-defined, and can be assigned to one or more funds.  Applied to order lines and invoice lines during fund distribution. Each fund can support multiple expense classes.
*   **Fiscal year.** The twelve-month period your library uses to manage its finances.
*   **Fund.** A fiscal entity used to track transactions against a general purpose or function within a ledger. Funds are associated with only one ledger. Fund information persists from year to year as new budgets are created for the fund each year.
*   **Group.** A collection of one or more funds grouped together.
*   **Ledger.** A collection of funds that need to be kept fiscally separate from another ledger’s collection of funds.  All funds within a ledger share future fiscal year rollover behavior.
*   **Net transfers.** Money transferred between funds during a fiscal year.
*   **Transaction.** A record to keep track of a specific change to a budget. For instance, an allocation, a transfer, an encumbrance, a pending payment or a payment.


## Capabilities

The capabilities listed below allow you to interact with the Finance app and determine what you can or cannot do within the app. You can assign capabilities to users via user roles. If none of these capabilities are assigned to a user, they are unable to see the Finance app or any related information.

It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities.

|**Permission Display name (OKAPI)** | **Resource (EUREKA)** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Finance: Assign acquisition units to new record.** | **UI-Finance Acq Unit Assignment** | procedural | execute | This capability allows the user to assign acquisition units to the record when creating a new record.|
|**Finance: Create allocations.** | **UI-Finance Allocations** | data | create | This capability allows users to create allocation transactions against budgets. Must include view and edit fund and budget capabilities.|
|**Finance: Create transfers.** | **UI-Finance Transfers** | data | create | This capability allows users to create transfer transactions against budgets. Must include view and edit fund and budget capabilities.|
|**Finance: Delete batch allocation logs**| **UI-Finance Fund-Update-Logs** | data | delete | This capability allows users to delete the logs produced by a batch allocation job.| 
|**Finance: Execute fiscal year rollover.** | **UI-Finance Ledger Rollover** | procedural | execute | This capability allows the user to perform fiscal year rollover.|
|**Finance: Export finance records.** | **UI-Finance** | procedural | execute | This capability allows the user to run an export of finance records for a ledger.|
|**Finance: Manage acquisition units.** | **UI-Finance Acq Unit Assignment** | data | manage | This capability allows users to change the assignment of acquisition units for the record when editing a record.|
|**Finance: Manually release encumbrance.** | **UI-Finance Encumbrance Release-Manually** | procedural | execute | This capability allows the user to release an encumbrance from a fund using the **Release encumbrance** action on the budget transaction log.|
|**Finance: Recalculate budget totals.** | **UI-Finance Fund-Budget Recalculate-Totals** | procedural | execute | This capability allows the user to recalculate budget totals after having deleted financial transactions by using the **Recalculate budget total** action on the budget record.|
|**Finance: Unrelease encumbrance.**| **UI-Finance Encumbrance Unrelease** | procedural | execute | This capability allows the user to manually unrelease an encumbrance that may have been erroneously released either by an invoice approval or a manual action.|
|**Finance: View batch allocation logs** | **UI-Finance Fund-Update-Logs** | data | view | This capability allows users to view the logs produced by a batch allocation job.| 
|**Finance: View fiscal year.** | **UI-Finance Fiscal-Year** | data | view | This capability allows searching and viewing of fiscal year records.|
|**Finance: View fund and budget.** | **UI-Finance Fund-Budget** | data | view | This capability allows the user to search and view funds and budgets.|
|**Finance: View group.** | **UI-Finance Group** | data | view | This capability allows the user to search and view groups.|
|**Finance: View ledger.** | **UI-Finance Ledger** | data | view | This capability allows the user to search and view ledgers.|
|**Finance: View, edit fiscal year.** | **UI-Finance Fiscal-Year** | data | edit | This capability allows the user to view and edit fiscal years.|
|**Finance: View, edit fund and budget.** | **UI-Finance Fund-Budget** | data | edit | This capability allows the user to view and edit funds and budgets.|
|**Finance: View, edit group.** | **UI-Finance Group** | data | edit | This capability allows the user to view and edit groups.|
|**Finance: View, edit ledger.** | **UI-Finance Ledger** | data | edit | This capability allows the user to view and edit ledgers.|
|**Finance: View, edit, create fiscal year.** | **UI-Finance Fiscal-Year** | data | create | This capability allows the user to view, edit, and create fiscal years.|
|**Finance: View, edit, create fund and budget.** | **UI-Finance Fund-Budget** | data | create | This capability allows the user to view, edit, and create funds and budgets.|
|**Finance: View, edit, create group.** | **UI-Finance Group** | data | create | This capability allows the user to view, edit, and create groups.|
|**Finance: View, edit, create ledger.** | **UI-Finance Ledger** | data | create | This capability allows the user to view, edit, and create ledgers.|
|**Finance: View, edit, delete fiscal year.** | **UI-Finance Fiscal-Year** | data | delete | This capability allows the user to view, edit, and delete fiscal year.|
|**Finance: View, edit, delete fund and budget.** | **UI-Finance Fund-Budget | data | delete | This capability allows the user to view, edit, and delete funds and budgets.|
|**Finance: View, edit, delete group.** | **UI-Finance Group** | data | delete | This capability allows the user to view, edit, and delete groups.|
|**Finance: View, edit, delete ledger.** | **UI-Finance Ledger** | data | delete | This capability allows the user to view, edit, and delete ledgers.|


## Keyboard shortcuts
Keyboard shortcuts allow you to perform actions in this app using the keyboard.  See [Platform essentials > Keyboard shortcuts](../../platform-essentials/keyboard-shortcuts/keyboardshortcuts/) for more information.



## Creating a fiscal year

A fiscal year is the twelve-month period your library uses for accounting and budgetary purposes. In FOLIO, a fiscal year serves as the basis for the entire fund structure and its parts. Note: Before creating a new fiscal year, be sure to check the **Primary currency** value specified in your [Settings > Tenant > Language and localization](../../settings/settings_tenant/settings_tenant/#settings--tenant--language-and-localization). The currency on a budget is set to the Tenant currency value at the time the fiscal year record is created; therefore, if the Tenant currency value is updated, any budgets created prior to the update will still operate based on the Tenant currency that existed when the Fiscal year associated with the budget was created.


1. In the **Search & filter** pane, click **Fiscal year**.
2. In the **Fiscal year** pane, click **New**.
3. In the **Create fiscal year** window, enter all required information for the fiscal year. For more information on the fields and actions available in this section, see the descriptions below.
4. Click **Save & Close**. The fiscal year is saved.  


### Fiscal year information

*   **Name (required).** The name of the fiscal year. A suggested naming convention is the term “Fiscal Year” followed by the numeric year. For example, Fiscal Year 2021.
*   **Code (required).** The code must be an alpha followed by a four-digit number. It can be based on name and year; for example, FY2021. The code that you establish for your fiscal year one will determine the code structure moving forward. In this example, FY2021 would be followed in succession by FY2022, FY2023, etc. Adherence to this code structure is essential to the success of fiscal year rollover. A single FOLIO tenant may have multiple fiscal years running in parallel. For example, an academic library with a July 1 - June 30 fiscal year may share a tenant with a government library operating on an October 1 - September 30 fiscal year. The academic library may configure FYA2021 with the government library configuring FYG2021 to allow rollover at different points in the calendar year.
*   **Acquisition units.** If you only want particular users within certain acquisition units to be able to edit the fiscal year, enter or select the Acquisition units from the drop-down list. You can select multiple units. If blank, any users with the appropriate capabilities are allowed to edit the fiscal year information. For more information, see [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/).
*   **Period Begin Date (UTC) (required).** The date when the fiscal year begins.
*   **Period End Date (UTC) (required).** The date when the fiscal year ends.
*   **Description.** A description of the fiscal year.



## Creating a ledger

A ledger is a collection of funds that need to be kept fiscally separate from another ledger’s collection of funds. Multiple ledgers can be associated with a fiscal year and each ledger can persist in future fiscal years. A fund can be associated with only one ledger.


1. In the **Search & filter** pane, click **Ledger**.
2. In the **Ledger** pane, click **New**.
3. In the **Create ledger** window, enter all required information for the ledger. For more information on the fields and actions available in this section, see the descriptions below.
4. Click **Save & Close**. The ledger is saved.


### Ledger information

*   **Name (required).** Name of the ledger. For example, Law Library.
*   **Code (required).** User-created, based on name.
*   **Fiscal year one (required).** The first fiscal year for the ledger. Ledgers can continue to be used for multiple fiscal years. If the fiscal year does not appear in the list, you can click **New fiscal year** to create a new one.
*   **Status (required).** Select the status of the ledger: Active, Frozen, or Inactive. Active means the ledger is ongoing, Frozen means the ledger has been put on pause, and Inactive means the ledger is no longer in use.
*   **Acquisition Units.** If you only want particular users within certain acquisition units to be able to edit the ledger, enter or select the Acquisition units from the drop-down list. You can select multiple units. If blank, any users with the appropriate capabilities are allowed to edit the ledger's information. For more information, see [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/).
*   **Enforce all budget encumbrance limits.**  This box is checked by default.  Leave this box checked if you want the system to reject any encumbrances against funds related to this ledger that would exceed the available amount of the current budget.  Uncheck this box to allow encumbrance amounts on the current year budget without restrictions.
*   **Enforce all budget expenditure limits.**  This box is checked by default.  Leave this box checked if you want the system to reject any expenditures against funds related to this ledger that would exceed the available amount of the current budget.  Uncheck this box to allow expenditure amounts on the current year budget without restrictions.
*   **Description.** A description of the ledger.


## Creating a group

Groups categorize funds and bring multiple funds together as a single group regardless of fiscal year or ledger. This enables the total amount available or allocated across multiple funds to be summarized by group, ledger, or fiscal year.



1. In the **Search & filter** pane, click **Group**.
2. In the **Group** pane, click **New**.
3. In the **Create group** window, enter all required information for the group. For more information on the fields and actions available in this section, see the descriptions below.
4. Click **Save & Close**. The group is saved.


### Group information

*   **Name (required).** Name of the group. For example, History.
*   **Code (required).** User-created, based on name.
*   **Status (required).** Select the status of the group: Active, Frozen, or Inactive. Active means the group is ongoing, Frozen means the group has been put on pause, and Inactive means the group is no longer in use.
*   **Acquisition units.** If you only want particular users within certain acquisition units to be able to edit the group, enter or select the Acquisition units from the drop-down list. You can select multiple units. If blank, any users with the appropriate capabiltiies are allowed to edit the group's information. For more information, see [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/).
*   **Description.** A description of the group. For example, you may want to include why the group was created and the relation between the different funds.


## Creating a fund

Funds show information regarding an ongoing ledger with a budget for the current fiscal year. There can be many funds in a ledger, but each fund may only be associated with a single ledger. Many funds can be placed in a group and a fund can be assigned to multiple groups.



1. In the **Search & filter** pane, click **Fund**.
2. In the **Fund** pane, click **New.**
3. In the **Create fund** window, enter all required information for the fund. For more information on the fields and actions available in this section, see the descriptions below.
4. Click **Save & Close**. The fund is saved.


### Fund information

*   **Name (required).** Name of the fund.
*   **Code (required).** User-created, based on name. The code must be unique. It is recommended to use alphanumeric and intuitive codes.
*   **Ledger (required).** Select the ledger associated with the fund. A fund may only be associated with a single ledger.
*   **Status (required).** Select the status of the fund: Active, Frozen, or Inactive. Active means the fund is ongoing, Frozen means the fund has been put on pause, and Inactive means the fund is no longer in use. Note: The fund must be active to successfully open an order or for an invoice to be fully paid.
*   **Currency.** This field is prefilled based on the currency associated with the fiscal year when the fiscal year was created. For more information, see [Creating a Fiscal Year](#creating-a-fiscal-year). Note that when an order is opened, the system creates an encumbrance transaction on the current budget for the fund selected in the fund distribution section of the order.  If the currency of the PO line is different than the budget currency, the encumbrance will display on the budget as a converted amount.  The budget currency is set to the Tenant currency value at the time the [Finance > Fiscal year](#fiscal-year-information) record is created; therefore, if the Tenant currency value is updated, any budgets created prior to the update will still operate based on the Tenant currency that existed when the Fiscal year associated with the budget was created.
*   **Type.** A category to describe the fund. Fiscal year rollover of funds is often defined by fund type, so definition of the type values should consider fiscal year rollover requirements. For example, endowment or restricted. For more information about creating fund types, see [Settings > Finance > Fund types](../../settings/settings_finance/settings_finance/#settings--finance--fund-types). Funds that are not assigned a fund type will be grouped under **No fund type** at fiscal year rollover.
*   **Acquisition units.** If you only want particular users within certain acquisition units to be able to edit the fund, enter or select the Acquisition units from the drop-down list. You can select multiple units. If blank, any users with the appropriate capabilities are allowed to edit the fund's information. For more information, see [Settings > Acquisition units](../../settings/settings_acquisition_units/settings_acquisition_units/). Please note: if the assigned acquisition unit restricts view, the fund will be filtered out of the selection list that appears in **Fund distribution** accordions on purchase order lines and invoices. Users will only be able to apply funds that are "public" or with which they share an acquisition unit.
*   **Group.** To associate this fund with a group, select the group from the drop-down list.  You can assign multiple groups. See [Creating a group](#creating-a-group) for more information. 
*   **Transfer from.** To allow transfers to this fund from any other fund, leave this field blank. To restrict transfers to this fund, enter or select the allowed funds from the drop-down list. You can select multiple funds.
*   **Transfer to.** To allow transfers from this fund to any other fund, leave this field blank. To restrict transfers from this fund, enter or select the allowed funds from the drop-down list. You can select multiple funds.
*   **External account (required).** The identifier for this account in an external financial system. If no integration with a financial system is desired, a library may use a hyphen (-) or other special character to satisfy the field requirement.
*   **Description.** A description of the fund. For example, you may want to include the purpose of the fund.
*   **Restrict use by location.** When selected, this checkbox exposes the **Locations** accordion on the fund record, allowing a user to link the fund with certain physical locations.

### Locations

This accordion will appear only if the **Restrict use by location** box is selected. When a fund is restricted to a specific location or locations and the fund is selected in a fund distribution on a purchase order line (POL), only the specified locations will appear in the location accordion dropdown on the POL.

To add a location:
1. Click **Add location**.
2. Use the **Search & filter** options to locate the location(s) you wish to restrict fund usage to.
3. Check the box(es) next to the location(s) you wish to restrict.
4. Click **Save**.

To remove a location:
1. Click the **X** to the right of the location you wish to remove.

To unassign all locations:
1. Click **Unassign all locations**.
Note: If you would like to unrestrict the fund, be sure to also uncheck **Restrict use by location** in the Fund information accordion.

### Donor information

Funds can be associated with donors who may have provided the money allocated to the fund's budget. Donor records are created within the Organizations app. For more information, see [Creating an Organization](../organizations/#creating-an-organization). When a donor is associated with a fund, and that fund is applied to a purchase order line (POL) as a fund distribution, the donor information is automatically added to the POL. It can be subsequently removed, if not required or desired.

To add a donor:
1. Click **Add donor**.
2. Use the **Search & filter** options to locate the donor(s) you wish to associate with the fund.
3. Check the box(es) next to the donor(s) you wish to select.
4. Click **Save**.

To remove a donor:
1. Click the **X** to the right of the donor you wish to remove.


## Creating a new budget

A budget is a finance record that describes the amount of money available for a fiscal year within a fund. You can create a current or planned budget for a fund from the fund details pane. To create a planned budget, one or more upcoming fiscal years must already be set up in the fiscal year series associated with the Ledger.  See  [Creating a fiscal year](#creating-a-fiscal-year) for more information. Previous budgets for past fiscal years will also appear on the fund details pane.



1. In the **Search & filter** pane, click **Fund**.
2. [Find the fund](#searching-for-a-fiscal-year-ledger-group-or-fund) to which you want to add a budget and select it.
3. In the fund details pane, in the **Current budget** or **Planned budget** section, click **New**.
4. In the **Current budget** or **Planned budget** dialog, enter all the required information for the budget. For more information on the fields and actions available in this window, see the descriptions below.
5. Click **Save**. The budget is saved.


### Budget information

*   **Fiscal year (required).** For a current budget, this value is defaulted to the current fiscal year value. For a planned budget, select a future fiscal year from the drop-down list.
*   **Status (required).** Select the status of the budget: Active, Closed, Frozen, Inactive, Planned. Active means the budget is open, Closed means the budget is closed, Frozen means the budget has been put on pause, Inactive means the fund is no longer in use, and Planned means the budget is assigned to a future fiscal year. Note: The budget must be active to successfully open an order or for an invoice to be approved and paid.
*   **Allowable expenditure percentage.** The percentage of the budget balance allowed for expenditures (including pending payments, but ignoring encumbrances). Leave this field blank to allow unrestricted expenditures. A value of 100 restricts expenditures to the available balance. A value greater than 100 allows expenditures beyond the available balance. A value of 0 restricts expenditures to 0.  
    This is only effective if the ledger has the **Enforce all budget expenditure limits** option enabled.
*   **Allowable encumbrance percentage.** The percentage of the budget balance allowed for encumbrances. Leave this field blank to allow unrestricted encumbrances. A value of 100 restricts encumbrances to the available balance. A value greater than 100 allows encumbrances beyond the available balance. A value of 0 restricts encumbrances to 0.  
    This is only effective if the ledger has the **Enforce all budget encumbrance limits** option enabled.
*   **Allocated (required).** Enter a numeric value of money to initially allocate to the budget. Values with or without decimals are accepted (100 or 100.00). To create a budget without allocated money, enter a value of 0. Inputting a value of 0 does not generate an allocation transaction. An initial allocation can be made after creating the budget. For more information, see [Allocating money to a budget](#allocating-money-to-a-budget).



### Adding expense classes to a budget

1. [Find the fund](#searching-for-a-fiscal-year-ledger-group-or-fund) to which you want to add an expense class and select it.
2. Click on the budget to access the **Budget details** window.
3. In the **Budget details** window, click **Actions > Edit**.
4. In the **Expense classes** section, click **Add expense class**.
5. Select an expense class from the drop-down list. See [Settings > Finance > Expense classes](../../settings/settings_finance/settings_finance/#settings--finance--expense-classes) for more information about creating expense classes.
6. Repeat steps 4 & 5 for all expense classes you wish to add.
7. Click **Save & close**. A confirmation message appears and the expense class is saved.



## Searching for a fiscal year, ledger, group or fund

You can search for fiscal years, ledgers, groups, or funds by clicking on either **Fiscal year**, **Ledger**, **Group**, or **Fund** in the **Search & filter** pane. To search for a fiscal year, ledger, group, or fund, enter your search terms into the box when you are in the Fiscal year, Ledger, Group, or Fund pane. Select the **All** drop-down list to search through one of the following fields:


*   **All.** Searches through names, codes, and descriptions. For funds, this will also search the external account field. This is the default search.
*   **Name.** The name of the fiscal year, ledger, group, or fund.
*   **Code.** A unique identifier for the fiscal year, ledger, group, or fund.
*   **External account number.** The identifier for this account in an external financial system. Appears only on the fund pane. 

You can also search for fiscal year, ledger, group, or fund by selecting any of the filters in the **Search & filter** pane when in the appropriate Finance pane. The filters available vary depending on whether you are searching for a fiscal year, ledger, group, or fund.  The following instructions are for searches in the **Fund** tab.


### Ledger

To search for funds belonging to a certain ledger, follow these steps:


1. In the **Search & filter** pane, click **Ledger**.
2. Select the ledger from the drop-down list. The funds are listed in the results pane.


### Status

To filter ledgers, groups, or funds by their status, select one of the following:


*   **Active.** Ledger, group, or fund currently used by your library.
*   **Inactive.** Ledger, group, or fund previously used by your library.
*   **Frozen.** Ledger, group, or fund that is paused.


### Type

To search for funds by type, follow these steps:


1. In the **Search & filter** pane, click **Type**.
2. Select the fund type from the drop-down list. The funds are listed in the result pane.


### Group

To search for funds assigned to a group, follow these steps:


1. In the **Search & filter** pane, click **Group**.
2. Select the group from the drop-down list. The funds are listed in the result pane.


### Acquisition units

To search for fiscal years, ledgers, groups, or funds assigned with a specific acquisition unit, follow these steps:

1. In the **Search & filter** pane, click **Acquisition units**.
2. Select the acquisition unit from the drop-down list. The search results appear in the Fiscal year, Ledger, Group, or Fund pane.


### Tags

To search for funds assigned with specific tags, follow these steps:


1. In the **Search & filter** pane, click **Tags**.
2. Select the tag(s) from the drop-down list. Your results appear in the Fund pane.


## Viewing fiscal year, ledger, group, fund, and budget details

The type of information displayed in your search results depends upon the type of search performed (fiscal year, ledger, group, or fund). That information can include:


*   **Name.** The name of the fiscal year, ledger, group, or fund record.
*   **Code.** A unique identifier for the fiscal year, ledger, group, or fund record.
*   **Description.** The purpose of the fiscal year record.
*   **Status.** Whether the fund is Active, Inactive, or Frozen.
*   **Ledger.** The ledger associated with the fund.

In the search results, click any result to view it. The fiscal year, ledger, group, or fund details pane each display additional information, including financial summaries. Funds that have a budget for the fiscal year appear on the fiscal year details pane. Funds that have a budget for the current fiscal year appear on the ledger, or group details panes. Funds without any budgets created only appear in the fund search results pane.


### Viewing fiscal year details

The fiscal year details pane contains fiscal year financial summary information and all ledgers, groups, and funds associated with a fiscal year. 


* To view fiscal year details, [find the fiscal year](#searching-for-a-fiscal-year-ledger-group-or-fund) you want to view and select it. The fiscal year details pane appears.


#### Fiscal year information

The Fiscal year information section contains the following fields:

*   **Record last updated.** Date and time when the record was last updated. Click **Record last updated** to see the next three fields.
*   **Source.** Name of the user who last updated the record.
*   **Record created.** Date and time when the record was created.
*   **Source.** Name of the user who created the record.
*   **Name.** Name of the fiscal year.
*   **Code.** Code for the fiscal year.
*   **Period begin date.** Date when the fiscal year begins.  
*   **Period end date.** Date when the fiscal year ends.
*   **Acquisition units.** All acquisition units assigned to the fiscal year.
*   **Description.** Description of the fiscal year.
*   **Currency.** The tenant currency at the time the fiscal year was created. This will be the currency of all the budgets associated with the fiscal year.


##### Financial Summary

This section displays a table containing summary financial information for all fund budgets associated with the fiscal year.

**Funding Information**
*   **Initial allocation.** The amount of the first allocation made to a budget, summarized for all fund budgets for the fiscal year.
*   **Total allocated.** The sum of all allocation amounts  across all fund budgets for the fiscal year (initial allocation plus increase in allocation minus decrease in allocation)
*   **Total funding.** The **Total allocated** amount plus the **Net transfers** amount. Note: For the fiscal year summary, the net transfers amount is not displayed since the system only allows transfers between budgets within the same fiscal year.  Net transfer amounts will only appear on the **Ledger**, **Group**, and **Budget** summary tables.
*   **Cash Balance.** The **Total funding** amount minus the **Expended** amount.

**Financial activity and overages**
*   **Encumbered.** The sum of all encumbrance transaction amounts against all fund budgets for the fiscal year.
*   **Awaiting Payment.** The sum of all pending payment transaction amounts against all fund budgets for the fiscal year.  
*   **Expended.** The sum of all payment transaction amounts against all fund budgets for the fiscal year.
*   **Credited.** The sum of all credit transaction amounts against all fund budgets for the fiscal year.
*   **Unavailable.** The total amount unavailable across all fund budgets for the fiscal year, calculated as the sum of the encumbered, awaiting payment, and expended amounts.
*   **Over encumbrance.** The encumbrance going beyond what is available in the fund budgets for the fiscal year (not taking allowable encumbrance into account).
*   **Over expended.** The total amount expended and awaiting payment minus the total funding amount for all fund budgets for the fiscal year (or zero if that value is negative).
*   **Available balance.** Total amount available across all fund budgets for the fiscal year, calculated as **Total funding** amount minus the **Unavailable** amount.  

#### Ledger

This section displays a table of all ledgers associated with the fiscal year. To sort by a column, click the column name. To view details about a ledger in the table, click anywhere in the ledger’s row.

The ledger table contains the following columns:



*   **Name.** Name of the ledger.
*   **Code.** Code for the ledger.
*   **Allocated.** Total amount allocated across all funds with a budget for the fiscal year that are associated with the ledger.
*   **Unavailable.** Total amount unavailable across all funds with a budget for the fiscal year that are associated with the ledger.
*   **Available.** Total amount available across all funds with a budget for the fiscal year that are associated with the ledger.


#### Group

This section displays a table of all groups associated with the fiscal year. The table contains the same columns as the [Ledger](#ledger) table.


#### Fund

This section displays a table of all funds associated with the fiscal year. The table contains the same columns as the [Ledger](#ledger) table.


### Viewing ledger details

The ledger details pane contains ledger financial summary information and all groups and funds associated with the ledger. 


* To view ledger details, [find the ledger](#searching-for-a-fiscal-year-ledger-group-or-fund) you want to view and select it. The ledger details pane appears.


#### Ledger information

The Ledger information section contains the following fields:


*   **Record last updated.** Date and time when the record was last updated. Click **Record last updated** to see the next three fields.
*   **Source.** Name of the user who last updated the record.
*   **Record created.** Date and time when the record was created.
*   **Source.** Name of the user who created the record.
*   **Name.** Name of the ledger.
*   **Code.** Code for the ledger.
*   **Current fiscal year.** The current fiscal year name. The system determines which fiscal year is current based on the current date and the period start and end dates for the fiscal year.
*   **Status.** Status of the ledger: Active, Inactive, Frozen.
*   **Acquisition units.** All acquisition units assigned to the ledger.
*   **Enforce all budget encumbrance limits.** When checked, the system rejects any encumbrances against funds related to this ledger that would exceed the available amount of the current budget.
*   **Enforce all budget expenditure limits.** When checked, the system rejects any expenditures against funds related to this ledger that would exceed the available amount of the current budget.
*   **Description.** Description of the ledger.



##### Financial Summary

**Funding Information**
*   **Initial allocation.** The amount of the first allocation made to a budget, summarized for all fund budgets for the ledger.
*   **Increase in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **to** all fund budgets for the ledger.
*   **Decrease in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **from** all fund budgets for the ledger.
*   **Total allocated.** The sum of all allocation amounts across all fund budgets for the current fiscal year that are associated with the ledger (initial allocation plus increase in allocation minus decrease in allocation).
*   **Net transfers.** Total net transfer amount for all fund budgets for the current fiscal year that are associated with the ledger.
*   **Total funding.** The **Total allocated** amount plus the **Net transfers** amount. 
*   **Cash Balance.** The **Total funding** amount minus the **Expended** amount.


**Financial activity and overages**
*   **Encumbered.** The sum of all encumbrance transaction amounts against all fund budgets for the ledger during the current fiscal year.
*   **Awaiting Payment.** The sum of all pending payment transaction amounts against all fund budgets for the ledger during the current fiscal year.  
*   **Expended.** The sum of all payment transaction amounts against all fund budgets for the ledger during the current fiscal year.
*   **Credited.** The sum of all credit transaction amounts against all fund budgets for the ledger during the current fiscal year.
*   **Unavailable.** The total amount unavailable across all fund budgets for the ledger during the current fiscal year, calculated as the sum of the encumbered, awaiting payment, and expended amounts.
*   **Over encumbrance.** The encumbrance going beyond what is available in the fund budgets for the ledger during the current fiscal year (not taking allowable encumbrance into account). 
*   **Over expended.**  The total amount expended and awaiting payment minus the total funding amount for all fund budgets for the ledger during the current fiscal year (or zero if that value is negative).
*   **Available balance.** Total amount available across all fund budgets for the ledger during the current fiscal year, calculated as **Total funding** amount minus the **Unavailable** amount.  


#### Group

This section displays a table of all groups associated with the ledger. To sort by a column, click the column name. To view details about a group in the table, click anywhere in the group’s row.

The Group table contains the following columns:

*   **Name.** Name of the group.
*   **Code.** Code for the group.
*   **Allocated.** Total amount allocated across all funds with a budget for the fiscal year that are associated with the group.
*   **Unavailable** Total amount unavailable across all funds with a budget for the fiscal year that are associated with the group.
*   **Available.** Total amount available across all funds with a budget for the fiscal year that are associated with the group.


#### Fund

This section displays a table of all funds associated with the ledger. The table contains the same columns as the Group table.


#### Fiscal year rollover error log

This section displays the list of rollover error logs. Click on the .csv file name to download the error log.

### Exporting ledger funds and budgets

To export a file of budget information for funds associated with a ledger in comma-separated values (.csv) format, follow these steps:

In the **Search & filter** pane, use the search and filter options to select a ledger.  Click on the ledger in the result table list.
In the ledger detail pane, click **Actions** and select,**Export budget information (CSV)**.

In the **Export settings** dialog, the following message will display: “This export could take a few minutes. If you reload or close the page the export will not be completed. Once the file is ready it could take another minute for your browser to finish downloading the file. You can continue to work with finance records in a different browser tab if needed.”

Select the **Fiscal year** to export from the drop-down list.

Select the **Expense classes** to export from the drop-down list: All, Active, Inactive, None.

Click **Export**.  The file downloads to your local download location and contains the following fields:

#### Ledger fund budgets export file fields list:

*   Name (Fund)
*   Code (Fund)
*   Status (Fund)
*   Type
*   Group (Code)
*   Acquisition unit
*   Transfer from
*   Transfer to
*   External account number
*   Description
*   Name (Budget)
*   Status (Budget)
*   Allowable encumbrance
*   Allowable expenditure
*   Date created (Budget)
*   Initial allocation
*   Increase
*   Decrease
*   Total allocation
*   Transfers
*   Total Funding
*   Encumbered (Budget)
*   Awaiting payment (Budget)
*   Expended (Budget)
*   Credited (Budget)
*   Unavailable
*   Over encumbered
*   Over expended
*   Cash balance
*   Available
*   Name (Exp Class)
*   Code (Exp Class)
*   Status (Exp Class)
*   Encumbered (Exp Class)
*   Awaiting payment (Exp Class)
*   Expended (Exp Class)
*   Credited (Exp Class)
*   Percentage of total expended   



### Viewing group details

The group details pane contains group financial summary information and lists all funds and expense classes associated with the group. 


* To view group details, [find the group](#searching-for-a-fiscal-year-ledger-group-or-fund) you want to view and select it. The group details pane appears.


#### Group information

*   **Record last updated.** Date and time when the record was last updated. Click **Record last updated** to see the next three fields.
*   **Source.** Name of the user who last updated the record.
*   **Record created.** Date and time when the record was created.
*   **Source.** Name of the user who created the record.
*   **Name.** Name of the group.
*   **Code.** Code for the group.
*   **Fiscal year.** Name of the twelve-month period your library uses to manage its finances. The current fiscal year displays as the default. Use the drop-down list to select a different fiscal year.  The financial summary information displays for the fiscal year selected.
*   **Status.** Status of the group: Active, Inactive, Frozen.
*   **Acquisition units.** All acquisition units assigned to the group.
*   **Description.** Description of the group.

##### Financial Summary

**Funding Information**
*   **Initial allocation.** The amount of the first allocation made to a budget, summarized for all fund budgets for the group.
*   **Increase in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **to** all fund budgets for the group.
*   **Decrease in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **from** all fund budgets for the group.
*   **Total Allocated.** The sum of all allocated amounts across all fund budgets for the fiscal year selected that are associated with the group (initial allocation plus increase in allocation minus decrease in allocation).
*   **Net transfers.** Total net transfer amount for all fund budgets for the fiscal year selected that are associated with the group.
*   **Total funding.** The **Total allocated** amount plus the **Net transfers** amount. 
*   **Cash Balance.** The **Total funding** amount minus the **Expended** amount.


**Financial activity and overages**
*   **Encumbered.** The sum of encumbrance transaction amounts against all fund budgets for the group during the fiscal year selected.
*   **Awaiting Payment.** The sum of pending payment transaction amounts against all fund budgets for the group during the fiscal year selected.  
*   **Expended.** The sum of payment transaction against all fund budgets for the group during the fiscal year selected.
*   **Credited.** The sum of credit transaction against all fund budgets for the group during the fiscal year selected.
*   **Unavailable** Total amount unavailable across all fund budgets for the group during the fiscal year selected, calculated as the sum of the encumbered, awaiting payment, and expended amounts.
*   **Over encumbrance.** The encumbrance going beyond what is available in the fund budgets for the group during the fiscal year (not taking allowable encumbrance into account). 
*   **Over expended.**  The total amount expended and awaiting payment minus the total funding amount for all fund budgets for the group during the current fiscal year (or zero if that value is negative).
*   **Available balance.** Total amount available across all fund budgets for the group during the fiscal year selected, calculated as **Total funding** amount minus the **Unavailable** amount.  


#### Fund

This section lists all funds assigned to the group. To assign the group to a fund that is not yet assigned to the group, follow these steps:

1. Click **Add to group** in the fund accordion section.
2. In the **Select funds** dialog, find the fund or multiple funds using the search box and/or filters.
3. Click the fund(s) to select. 
4. Click Save.  The funds are added to the group. The funds will display only if they have a budget allocated for the selected fiscal year.

To remove a fund from the group, click on the **X** at the end of the fund row in the Fund accordion table list.


The Fund table contains the following columns:

*   **Name.** Name of the fund.
*   **Code.** Code for the fund.
*   **Allocated.** Total amount allocated across all funds with a budget for the fiscal year that are associated with the group.
*   **Unavailable.** Total amount unavailable across all funds with a budget for the fiscal year that are associated with the group.
*   **Available.** Total amount available across all funds with a budget for the fiscal year that are associated with the group.


#### Expense classes

This section lists all expense classes associated with funds assigned to the group. The Expense classes table contains the following columns:

*   **Expense class.** Name of the expense class, a fiscal entity used to track transactions against a specific purpose or function within a fund.
*   **Encumbered.**  Total amount encumbered for the expense class.
*   **Awaiting payment.**  Total amount awaiting payment for the expense class.
*   **Expended.** Total amount expended for the expense class.
*   **Percent of total expended.** Total amount expended for the expense class as a percentage of total expended from across all expense classes for funds in the group.

### Viewing fund details

The fund details pane contains fund information and all current, planned, and previous budgets as well as expense classes associated with a fund. The budget sections in the pane display total allocated, net transfers, unavailable, and available for the budget. The expense class detail is further broken down by encumbered, awaiting payment, expended, and percent of total expended. To view a list of transactions for the current budget of a fund, click **Actions > View transactions for current budget**. See [Viewing budget transactions](#viewing-transactions-for-a-current-budget) for more information.



* To view fund details, [find the fund](#searching-for-a-fiscal-year-ledger-group-or-fund) you want to view and select it. The fund details pane appears.


#### Fund information

The Fund information section contains details about the fund.  For descriptions of each field in this section, see  [Fund information](#fund-information).  

#### Current budget

This section contains a table of information about the current budget, if one exists.  The current year is based on the fiscal year period and the current date/time.

#### Current expense classes

This section contains a table of information about expenses classes assigned to the current budget, if applicable.


#### Planned budget

This section contains a table of any future budgets, if any exist. An upcoming fiscal year must be created prior to creating a planned budget.  See [Creating a fiscal year](#creating-a-fiscal-year).  To create a new planned budget, click **New**. See [Creating a new budget](#creating-a-new-budget) for more information.



#### Previous budget

This section contains a table of all budgets from fiscal years prior to the current fiscal year, if any exist.



### Viewing budget details

The budget details window contains a summary of the budget, including funding information and financial activity and overages, and budget information.

To view budget details, follow these steps:



1. [Find the fund](#searching-for-a-fiscal-year-ledger-group-or-fund) with the budget you want to view and select it.
2. In the **fund details** pane, in the **Current budget**, **Planned budget**, or **Previous budget** sections, click the budget **Name**. The budget details window appears.


#### Budget summary

The Budget summary section contains the following fields:

*   **Record last updated.** Date and time when the record was last updated. Click **Record last updated** to see the next three fields.
*   **Source.** Name of the user who last updated the record.
*   **Record created.** Date and time when the record was created.
*   **Source.** Name of the user who created the record.

**Funding Information**

*   **Initial Allocation.** The amount of the first allocation made to the budget.
*   **Increase in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **to** the budget.
*   **Decrease in allocation.** The sum of all allocation transaction amounts, not including the initial allocations, made **from** the budget.
*   **Total Allocated.** The sum of all allocated amounts for the budget (initial allocation plus increase in allocation minus decrease in allocation).
*   **Net transfers.** Total net transfer amount for the budget.
*   **Total funding.** The **Total allocated** amount plus the **Net transfers** amount. 
*   **Cash Balance.** The **Total funding** amount minus the **Expended** amount.


**Financial activity and overages**
*   **Encumbered.** The sum of all encumbrance transaction amounts against the budget.
*   **Awaiting Payment.** The sum of pending payment transaction amounts against the budget.
*   **Expended.** The sum of payment transaction amounts against the budget.
*   **Credited.** The sum of credit transaction amounts against the budget.
*   **Unavailable** The total amount unavailable for the budget, calculated as the sum of the encumbered, awaiting payment, and expended amounts.
*   **Available balance.** Total amount available for the budget, calculated as **Total funding** amount minus the **Unavailable** amount.  

#### Budget information

The Budget information section contains the following fields:

*   **Name.** Budget name. The structure of this name is the fund code, followed by a hyphen and the fiscal year code, e.g. ACCOUNTING-FY2021.
*   **Status.** Status of the ledger: Active, Closed, Frozen, Inactive, or Planned.
*   **Fiscal start.** Fiscal year start date.
*   **Fiscal end.** Fiscal year end date.
*   **Allowable expenditure.** Expenditure allowed, expressed as a percentage.
*   **Allowable encumbrance.** Encumbrance allowed, expressed as a percentage.
*   **Transactions.** Click **View transactions** to view budget transactions. See [Viewing budget transactions](#viewing-transactions-for-a-current-budget) for more information.


## Editing a budget


1. Find the budget you want to edit and select it.
2. In the **Budget details** window, click **Actions > Edit.**
3. Edit the budget.
4. Click **Save & close.** A confirmation message appears and the budget is updated.


## Allocating money to a budget

Use the **Actions** menu to allocate money to a budget.  You can **Increase allocation**, **Decrease allocation**, or **Move allocation**.


### Increasing allocation to a fund budget

1. [Find the budget](#viewing-budget-details) to which you want to allocate money and select it.
2. In the **Budget details** window, click **Actions > Increase allocation.**
3. In the **Increase allocation** dialog, enter the following information:

    *   **Fund.**  The name of the fund to which you want to increase an allocation of money. This field displays the fund name and code for the budget you selected and is not editable. The display format is Fund name (fund code).
    *   **Amount (required).** Enter an amount as a numeric value. Values with or without decimals are accepted (100 or 100.00). The amount must be a positive number.
    *   **Tags.** Enter or select any tags from the drop-down list to apply to the allocation transaction.
    *   **Description.** Enter a description of the allocation increase.

4. Click **Confirm.** A confirmation message appears and the increase allocation transaction is complete.



### Decreasing allocation to a fund budget

1. [Find the budget](#viewing-budget-details) to which you want to submit a decreased allocation and select it.
2. In the **Budget details** window, click **Actions > Decrease allocation.**
3. In the **Decrease allocation** dialog, enter the following information:

    *   **Fund.**  The name of the fund to which you want to submit a decreased allocation of money. This field displays the fund name and code for the budget you selected and is not editable. The display format is Fund name (fund code).
    *   **Amount (required).** Enter an amount as a numeric value. Values with or without decimals are accepted (100 or 100.00). The amount must be a positive number. 
    *   **Tags.** Enter or select any tags from the drop-down list to apply to the decrease allocation transaction.
    *   **Description.** Enter a description of the allocation decrease.

4. Click **Confirm.** A confirmation message appears and the decrease allocation transaction is complete.


### Moving allocation to another fund budget

Use the **Move allocation** action to move money between current fiscal year budgets as allocation transactions. Allocated amounts can be included in the next fiscal year allocation amount for a fund, depending on your fiscal year rollover settings . See [Transferring money between funds](#transferring-money-between-funds) for information about transfers to determine whether you want to move money using **Move allocation** or **Transfer**.

1. [Find the budget](#viewing-budget-details) to which you want to move an allocation and select it.
2. In the **Budget details** window, click **Actions > Move allocation.**
3. In the **Move allocation** dialog, enter the following information:

    *   **From (required).** Select the fund from which you want to allocate money. The display format is Fund name (fund code).
    *   **To (required).** Select the name of the fund to which you want to allocate money. This field displays the fund name (code) with which this budget is associated. You must populate either **From** or **To** with the fund for the budget you are currently viewing.
    *   **Amount (required).** Enter an amount as a numeric value. Values with or without decimals are accepted (100 or 100.00). The amount must be a positive number. 
    *   **Tags.** Enter or select any tags from the drop-down list to apply to the decrease allocation transaction.
    *   **Description.** Enter a description of the allocation move.

4. Click **Confirm.** A confirmation message appears and the decrease allocation transaction is complete.


## Batch allocation tools

From a ledger record, you can use batch allocation tools to grant or adjust allocation totals to the funds associated with the ledger. These tools do not support transferring money between funds associated with the ledger. Funds must be setup before these tools can be used to allocate money to the fund's budgets, but the budgets do not need to be created prior to using the batch allocation tools.

To access these tools, open the Finance app to the ledger pane and open the applicable ledger record so it is visible in the third pane for viewing.

### Batch allocations via the user interface
1. Click **Actions > Batch allocations**.
2. In the **Select fiscal year** window, select the applicable fiscal year from the dropdown menu.
3. Click **Save & close**.
4. On the **Batch edit budgets** screen, each fund name associated with the ledger will be listed, along with the following fields for each:
   * **Fund status**
   * **Budget name**
   * **Total allocated (before)**
   * **Budget status**
   * **Allocation increase/decrease**
   * **Total allocated (after)**
   * **Allowable encumbrance %**
   * **Allowable expenditure %**
   * **Transaction description**
   * **Transaction tags**
5. Fill in fields as desired.
6. Click **Recalculate** to validate the allocation updates. Please note: if you make additional changes after clicking **Recalculate**, you will need to click **Recalculate** again prior to saving.
7. Click **Save & close** to submit the updates.

### Batch allocations via CSV upload

## Transferring money between funds


You can transfer money between the current fiscal year budgets of two funds. This action is only allowed if both the **From** and **To** funds have current fiscal year budgets. Transfers are a one-time movement of money within a fiscal year. Unlike with moving allocations, fiscal year rollover will not consider transfer amounts in the initial allocation amounts for new budgets created as a result of fiscal year rollover.  



1. [Find the budget](#viewing-budget-details) to which you want to transfer money and select it.
2. In the **budget details** window, click **Actions > Transfer.**
3. In the **Transfer** dialog, enter the following information:

    *   **From (required).** Select the fund from which you want to transfer money.  
    *   **To (required).** Select the fund to which you want to transfer money. This field displays the fund name (code) with which this budget is associated. You must populate either **From** or **To** with the fund for the budget you are currently viewing.
    *   **Amount (required).** Enter an amount as a numeric value. Values with or without decimals are accepted (100 or 100.00). Negative values are accepted.  
    *   **Tags.** Enter or select any tags from the drop-down list you would like to apply to the transfer transaction.
    *   **Description.** Enter a description of the transfer.  

4. Click **Confirm.** A confirmation message appears and the transfer transaction is complete.



## Recalculating budget totals

There are cases when, after deleting financial transactions like pending payments, credits, payments, and encumbrances, a library may need to recalculate the totals on the impacted budget. Budget totals are recalculated entirely based on transactions.

1. [Find the budget](#viewing-budget-details) you want to recalculate and select it.
2. In the **Budget details** window, click **Actions > Recalculate budget totals.**
3. A confirmation message appears that says **Budget totals have been updated based on current budget transactions**. 


## Deleting a budget


Note: Financial structure records cannot be deleted if they have other records assigned to them. Budgets cannot be deleted once they have any type of transaction other than allocation transactions against them.


1. [Find the budget](#viewing-budget-details) you want to delete and select it.
2. In the **Budget details** window, click **Actions > Delete.**
3. Click **Delete** in the confirmation window. A confirmation message appears and the budget is deleted.


## Viewing transactions for a current budget

There are two methods to view a list of all transactions for a budget:

1. From a fund: [Find the fund](#searching-for-a-fiscal-year-ledger-group-or-fund) for which you want to view transactions and select it to open the fund details pane.  Click **Actions > View transactions for current budget.**
2. From a budget: [Find the budget](#viewing-budget-details)  for which you want to view transactions and select it.  In the **Budget details** window, under **Transactions**, click **View transactions**. The budget transactions window opens listing all transactions.


### Searching for budget transactions

To search budget transactions, follow these steps:


1. To search budget transactions by amount, in the **Transactions** window **Search & Filter** pane, enter a numeric value into the search box and click **Search**. A list of transactions containing the amount value entered is returned.
2. You may filter results by Type, Source, Source POL number, Source invoice number, Tags, or Expense class. See below for more information on the filters. Your results display in the Transactions pane.


#### Type

To filter transactions by Type, select one or more of the following:


*   **Allocation.** Filter transactions by type of Allocation. This includes initial allocations, as well as increases, decreases, and movements of allocations to the budget.
*   **Credit.** Filter transactions by type of Credit. Credit transactions are produced by paid invoices with negative totals.
*   **Encumbrance.** Filter transactions by type of Encumbrance. Encumbrance transactions are created on open orders based on the fund distribution(s) on the corresponding purchase order line (POL).
*   **Payment.** Filter transactions by type of Payment. Payment transactions are produced by paid invoices with positive totals.
*   **Pending payment.** Filter transactions by type of Pending payment. Pending payment transactions are produced by approved invoices. 
*   **Rollover transfer.**  Filter transactions by type of Rollover transfer. Rollover transfer transactions are the result of fiscal year rollover operations when a previous fiscal year's surplus funds are rolled over to the new fiscal year budget as a transfer.
*   **Transfer.** Filter transactions by type of Transfer. Transfer transactions result from the transfer of funds between budgets in a given fiscal year.


#### Source

To filter transactions by Source, select one of the following:


*   **Fiscal year.** Transactions generated during the fiscal year rollover process. For example, automated allocations during fiscal year rollover, as defined in [Rollover fiscal year](#rollover-fiscal-year) settings.
*   **Invoice.** Transactions generated through invoicing, specifically transaction types of **Credit**, **Payment**, and **Pending payment.**
*   **PO line** Transactions generated from a PO line, specifically **Encumbrance** transaction types.
*   **User.** Transactions created by a user through the fund action menu, specifically **Allocation** and **Transfer** transaction types.



#### Source POL number

To filter transactions by the Source POL number, follow these steps:


1. In the **Search & filter** pane, click **Source POL number.**
2. Begin typing the POL number and select from the drop-down list. Your result appears in the Transactions pane.



#### Source invoice number

To filter transactions by the Source invoice number, follow these steps:


1. In the **Search & filter** pane, click **Source invoice number.**
2. Begin typing the invoice number and select from the drop-down list. Your result appears in the Transactions pane.




#### Tags

To filter for transactions assigned with specific tags, follow these steps:


1. In the **Search & filter** pane, click **Tags.**
2. Select the tag(s) from the drop-down list. Your results appear in the Transactions pane.


#### Expense class

To filter transactions by expense class, follow these steps:


1. In the **Search & filter** pane, click **Expense class.**
2. Select an expense class from the drop-down list. Your results appear in the Transactions pane.

#### Encumbrance status

To filter transactions by encumbrance status, follow these steps:


1. In the **Search & filter** pane, click **Encumbrance status.**
2. Select **Released** or **Unreleased**. Your results appear in the Transactions pane.
   
Once you view budget transactions, the following columns appear in the Transactions pane search results table. Click the column name to sort by that column.


*   **Transaction date.** Date of the transaction.
*   **Type.** Transaction type: Allocation, Credit, Encumbrance, Payment, Pending Payment, Rollover transfer, or Transfer.
*   **Amount.** Amount for the transaction. Negative values are in parentheses.
*   **From.** Fund code of the fund from which a transfer was made into the budget.
*   **To.** Fund code of the fund to which a transfer was made from the budget.
*   **Source.** Fiscal year, Invoice, PO Line, or User.
*   **Tags.** Any tags associated with the transaction.


To view additional information about a transaction, click the transaction row in the table to open a detail pane.  Each transaction type displays a different set of fields relevant to that type.  See information below about the fields that display for each type.



### Viewing allocation transactions

*   **Record last updated.** Date and time when the record was last updated. Click **Record last updated** to see the next three fields.
*   **Source.** Name of the user who last updated the record.
*   **Record created.** Date and time when the record was created.
*   **Source.** Name of the user who created the record.
*   **Transaction date.** Date and time of the transaction.
*   **Fiscal year.**  The fiscal year for the budget.
*   **Amount.** Amount of the transaction. Negative values are in parentheses.
*   **Source.** Fiscal year or User.
*   **Type.** Transaction type: Allocation.
*   **From.** Fund name and fund code from which the allocation was made into this budget, if applicable.  See [Allocating money to a budget](#allocating-money-to-a-budget) for more information.
*   **To.** Fund name and fund code of this budget to which the allocation was made.
*   **Expense class.**  This field will be blank for allocation transactions since expense class designations for allocations aren’t supported by the system.
*   **Tags.** Any tags associated with the transaction.
*   **Description.**  A description entered by the user when [Allocating money to a budget](#allocating-money-to-a-budget).



### Viewing credit transactions

The credit transaction detail pane contains many of the same fields as the [allocation detail pane](#viewing-allocation-transactions).  Some fields are populated differently for credit transactions:

*   **Source.** Invoice number or identifier that generated this credit transaction.  Click on the invoice identifier to open the Invoices app invoice detail pane for that invoice.
*   **Type.** Transaction type: Credit.
*   **From.** This field will be blank for credit transactions. 
*   **To.** Fund name and fund code of this budget to which the credit was made.
*   **Description.**  This field is blank for credit transactions.


### Viewing encumbrance transactions

When an order containing a PO Line with a fund distribution is opened, an **Encumbrance** transaction against the current fiscal year budget for the fund is created. The encumbrance transaction detail pane contains many of the same fields as the [allocation detail pane](#viewing-allocation-transactions).  Some fields are populated differently for encumbrance transactions:

*   **Source.** Purchase order line (PO Line) number that generated this encumbrance transaction.  Click on the POL number to open the Orders app PO Line detail pane for that order line.
*   **Type.** Transaction type: Encumbrance.
*   **From.** Fund name and code for this budget to which this encumbrance was applied.  
*   **To.** This field will be blank for encumbrance transactions.
*   **Expense class.**  The expense class assigned to this encumbrance transaction.
*   **Initial encumbrance.**  The amount originally encumbered by the related PO Line; the estimated price value.  
*   **Awaiting payment.**  The amount awaiting payment. This amount is populated after an invoice for the related PO Line is approved.
*   **Expended.**  The amount expended.  This amount is populated after an invoice for the related PO Line is paid.
*   **Status.** The status of this encumbrance: Unreleased or Released.  The encumbrance can be [released manually](#releasing-encumbrances-manually) by the user or automatically by the system upon payment of an invoice.
*   **Description.**  This field will be blank for encumbrance transactions.



#### Releasing encumbrances manually

If you need to unencumber an order, this action is available from the transaction detail on the encumbered budget. This may be needed to manage charges related to ongoing orders. To release an encumbrance the user must have the corresponding capability assigned. 

To release an encumbrance, follow these steps:

1. Find the transaction list for the encumbered budget.  See [Viewing transactions for a current budget](#viewing-transactions-for-a-current-budget) for more information.
2. Select the encumbrance transaction from the result list. 
3. On the encumbrance detail pane, click **Release encumbrance.**
4. In the confirmation window, click **Confirm** for the message “Are you sure you want to release this encumbrance? Any remaining amount will be added back to the budget."
5. The encumbrance is released.  The amount is restored to the budget and the status value on the encumbrance detail pane changes from **Unreleased** to **Released.**


#### Unreleasing encumbrances manually

There are situations where encumbrances may erroneously end up with a status of released. In these circumstances users should be able to unrelease encumbrances manually. To unrelease an encumbrance, the user must have the corresponding capability assigned. 

To unrelease an encumbrance, follow these steps:

1. Find the transaction list for the budget you wish to re-encumber.  See [Viewing transactions for a current budget](#viewing-transactions-for-a-current-budget) for more information.
2. Select the encumbrance transaction from the result list. 
3. On the encumbrance detail pane, click **Unrelease encumbrance.**
4. In the confirmation window, click **Confirm** for the message “Are you sure you want to unrelease this encumbrance? Any remaining amount will be encumbered against the budget."
5. The encumbrance is unreleased.  The amount is re-encumbered on the budget and the status value on the encumbrance detail pane changes from **Released** to **Unreleased.**

### Viewing payment transactions

When an invoice is paid, the existing **Pending payment** transaction record type value is updated from type [Pending payment](#viewing-pending-payment-transactions) to type **Payment.** The payment transaction detail pane contains many of the same fields as the [allocation detail pane](#viewing-allocation-transactions).  Some fields are populated differently for payment transactions:


*   **Source.** Invoice number or identifier that generated this payment transaction.  Click on the invoice identifier to open the Invoices app invoice detail pane for that invoice.
*   **Type.** Transaction type: Payment.
*   **From.** Fund name and code for this budget to which this payment was applied.  
*   **To.** This field will be blank for payment transactions. 
*   **Description.**  This field will be blank for payment transactions. 


### Viewing pending payment transactions

When an invoice is approved, a **Pending payment** type transaction record is created for the fund’s current fiscal year budget. The original encumbrance transaction record for a related PO Line will persist on the transaction list for the budget.  The amount value of the encumbrance transaction is updated when an invoice is approved since approval of the invoice releases the pending payment amount of the encumbrance.  Once an invoice is paid, the transaction’s type value is changed from **Pending payment** to **Payment.** The pending payment transaction detail pane the same fields as the [payment transaction detail pane](#viewing-payment-transactions).  


### Viewing rollover transfer transactions

The fiscal year rollover process creates transfer transactions if the [rollover settings](#fiscal-year-rollover-information) are defined to create transfers to new fiscal year budgets.  



### Viewing transfer transactions

When a [transfer of money](#transferring-money-between-funds) is made between two funds, a **Transfer** transaction is created. The transfer transaction detail pane contains many of the same fields as the [allocation detail pane](#viewing-allocation-transactions).  Some fields are populated differently for transfer transactions:


*   **Source.**  Set to User for transfer transactions.  
*   **Type.** Transaction type: Transfer.
*   **From.** Fund name and fund code from which the transfer was made into this budget. 
*   **To.** Fund name and fund code of this budget to which the transfer was made.
*   **Description.**  A description added by the user during the [transfer](#transferring-money-between-funds).



## Editing a fiscal year, ledger, group, fund, or budget records


1. In the **Search & filter** pane, click the appropriate option: **Fiscal year**, **Ledger**, **Group**, or **Fund**.
2. In the corresponding pane, select the record you want to edit.
3. In the corresponding details pane, click **Actions > Edit**.
4. Make your desired changes.
5. Click **Save & close**. The record is saved and updated. Note: if another user edited and saved the same record while you were editing, the following message appears: “This record cannot be saved because it is not the most recent version. View latest version.” Click on the hyperlink text “View latest version” to refresh the record and repeat steps 3-5 above to successfully edit.


## Deleting a fiscal year, ledger, group, or fund

Note: Financial structure records cannot be deleted if they have other records assigned to them. 


1. In the **Search & filter** pane, click the appropriate option: **Fiscal year**, **Ledger**, **Group**, or **Fund**.
2. In the corresponding pane, select the record you want to edit.
3. In the corresponding details pane, click **Actions > Delete**.
4. In the **Delete record** dialog, click **Delete**. A confirmation message appears and the record is deleted.



## Rollover fiscal year


Fiscal year rollover is initiated from the ledger detail pane.  This process can close current fiscal year budgets, create upcoming fiscal year budgets with or without allocated funds based on fund type, and roll encumbrances onto new fiscal year budgets based on order type (one-time, ongoing, and ongoing subscription). This action is applied only to the funds associated with the ledger, so rollover must be run separately for each ledger.  

Note: Prior to running the fiscal year rollover process, it is recommended to do the following:
1. Review open orders to determine if the **Re-encumber** check box is selected where desired. If **Re-encumber** is not selected, but the order's workflow status is **Open**, an encumbrance transaction will be created in the new fiscal year's budget, but the transaction will be released and will not earmark any funds in the new budget.
2. Review and resolve approved invoices.
3. Run at least one test of rollover to identify any remaining unpaid invoices and to view the rollover log prior to running the actual rollover.

To run a test of fiscal year rollover, follow these steps:

1. In the **Search & filter** pane, click **Ledger.**
2. Use the search and filter tools, if needed, to find the ledger to rollover.
3. In the ledger results pane, select the name of the ledger to rollover.
4. The ledger detail pane will open. Open the Action menu and select **Rollover.**
5. In the Rollover window, complete the form to indicate your preferences for rollover settings.  For more information on the fields on the rollover screen, see the descriptions below.
6. Click the **Test rollover** button to initiate a test of fiscal year rollover for this ledger.
7. If any unpaid invoices exist, a dialog window displays, “FOLIO has found invoices that are not yet paid or canceled. If you are sure you want to continue with rollover click continue.”  A table list of invoices displays the following information:
    *   **Vendor invoice number.**
    *   **Vendor.**  
    *   **Invoice date.** 
    *   **Status.**
    *   **Total amount (system)**
8. Click **Cancel** to exit the dialog list without proceeding with the rollover test, click **Export list** to download a .csv file list unpaid invoices, or click **Continue** to proceed with the rollover test.
9.  After continuing, a dialog displays “Please confirm that you have completed the necessary details and are ready to proceed with your rollover TEST. This process may take several minutes to complete. A link to the results will be sent to [user email address] when the process is complete.” 
10. Click **Confirm.**  A green toast message indicates that the rollover test started successfully and focus returns to the three pane layout for the ledger.  A confirmation email is sent to the user’s email address.
11. To [view the test rollover results](#viewing-rollover-log-results) in the log, open the Actions menu and select **Rollover logs.** 


To run fiscal year rollover, follow these steps:


1. In the **Search & filter** pane, click **Ledger.**
2. Use the search and filter tools, if needed, to find the ledger to rollover.
3. In the ledger results pane, select the name of the ledger to rollover.
4. The ledger detail pane will open. Open the Action menu and select **Rollover.**
5. In the Rollover window, complete the form to indicate your preferences for rollover settings.  For more information on the fields on the rollover screen, see the descriptions below.
6. Click the **Rollover** button to initiate a test of fiscal year rollover for this ledger.
7. If any unpaid invoices exist, a dialog window displays, “FOLIO has found invoices that are not yet paid or canceled. If you are sure you want to continue with rollover click continue.”  A table list of invoices displays the following information:
    *   **Vendor invoice number.**
    *   **Vendor.**  
    *   **Invoice date.** 
    *   **Status.**
    *   **Total amount (system)**
8. Click **Cancel** to exit the dialog list without proceeding with the rollover test, click **Export list** to download a .csv file list unpaid invoices, or click **Continue** to proceed with the rollover.
9.  After continuing, a dialog displays “Please confirm that you have completed the necessary details and are ready to proceed with your rollover. This process may take several minutes to complete. A link to the results will be sent to [user email address] when the process is complete.” 
10. Click **Confirm.**  A green toast message indicates that the rollover started successfully and focus returns to the three pane layout for the ledger.  A confirmation email is sent to the user’s email address.
11. To [view the rollover results](#viewing-rollover-log-results) in the log, open the Actions menu and select **Rollover logs.** 


### Fiscal year rollover information

When you select the **Rollover** action, the system displays the current year for the ledger at the top left of the rollover form.  The current year is based on the fiscal year period and the current date/time.

If your institution runs rollover before or after the fiscal year end date, you’ll need to return to the fiscal year tab and adjust the dates of both the fiscal year you are rolling from and the upcoming fiscal year such that the current date now fits into the fiscal year you are rolling from. Remember to readjust the fiscal year dates back to the actual fiscal year dates after rollover is complete.  See [Editing a fiscal year, ledger, group, fund, or budget records](#editing-a-fiscal-year-ledger-group-fund-or-budget-records) for more information.


*   **Period begin date.**  The fiscal year begin date for the **Fiscal year** selected.   See [Creating a fiscal year](#creating-a-fiscal-year) for more information about period dates.
*   **Period end date.** The Fiscal Year end date for the Fiscal year selected.  Note: The **Period end date** must be greater than the current date to initiate rollover from the current year to an upcoming year. 
*   **Fiscal year.**  Select the next fiscal year.  If the next fiscal year has not yet been set up, click **New fiscal year** to create one.  See  [Creating a fiscal year](#creating-a-fiscal-year) for more information.
*   **Enforce all budget encumbrance limits.** This box is checked by default. Leave this box checked if you want the system to reject any encumbrances that would exceed the available amount. For example, if your institution typically does not roll over allocations and adds initial allocation amounts manually after rollover, you might want to uncheck this box to allow current year encumbrances to be applied to the upcoming year budgets that are awaiting initial allocations.  
*   **Enforce all budget expenditure limits.** This box is checked by default. Uncheck this box to allow expenditures to rollover even if the new budget has insufficient funds allocated.  
*   **Close all current budgets.**  This checkbox is selected by default and indicates that you want to close all the current fiscal year budgets as part of this rollover. Uncheck this box if you wish to leave the budget active if you must pay future invoices against past fiscal years.


#### Rollover budgets 

The information in this section defines rollover behavior for budgets by fund type.  For more information about creating fund types, see [Settings > Finance > Fund types](../../settings/settings_finance/settings_finance/#settings--finance--fund-types).  For each fund type listed, select the appropriate settings for each of the fields defined below.  These settings will be applied to all upcoming fiscal year budgets of that fund type. If a fund does not have a fund type assigned, it will be listed under **No fund type**.


*   **Rollover allocation.**  Check this box if you want the upcoming fiscal year budget initial allocation amount to equal the current fiscal year budget total allocation amount.
*   **Adjust allocation, %.**  The percentage amount to be applied to the current fiscal year budget total allocation amount to set the upcoming fiscal year's budget initial allocation amount. For example, if the current budget total allocation is $1000 and you enter two percent, the upcoming budget initial allocation value is set to $1020.
*   **Rollover budget value.**  Select which value from the current fiscal year budget to roll over to the new fiscal year budget, if your library allows the rollover of surplus funds: Select **None** to ignore the current fiscal year budget values, **Available** to use the available amount, and **Cash balance** to use the remaining cash balance which is the total funding amount minus the total expended amount.  See [Viewing budget details](#viewing-budget-details) for a full description of the Available and Cash balance values.
*   **Rollover value as.**  Indicates whether any available amounts that are rolled over should be categorized as a **Transfer** or an **Allocation.**
*   **Set allowances.** Check this box to activate the  **Allowed encumbrance, %.** and **Allowed expenditure, %.** fields. 
*   **Allowed encumbrance, %.**  The percentage amount to be applied to the upcoming fiscal year's budget allocated amount to calculate allowed encumbrances against funds of this fund type.  To allow all encumbrances with no limit, leave this field blank.  For example, if the budget’s total funding is $1000 and you set an **Allowed encumbrance, %** of 110 percent, the system will allow opening orders up to $1100. Similarly, a value of 90 percent will limit encumbrances to $900. Note: You can only enter a value in this field if the **Set allowances** checkbox is checked.
*   **Allowed expenditure, %.**  The percentage amount to be applied to the upcoming budget’s allocated amount to calculate allowed expenditures against funds of this fund type.  To allow all expenditures with no limit, leave this field blank. For example, if the budget’s total funding is $1000 and you set an **Allowed expenditure, %** of 110 percent, the system will allow approval of invoices up to $1100.  Similarly, a value of 90 percent will limit expenditures to $900. Note: You can only enter a value in this field if the **Set allowances** checkbox is checked.



#### Rollover encumbrances

The information in this section defines rollover behavior for encumbrances by order type: one-time, ongoing, or ongoing-subscription.  An order is considered an ongoing-subscription if the order type is **Ongoing** and the **Subscription** checkbox is checked. See [Orders > Creating an ongoing order > Ongoing order information](../orders/#ongoing-order-information) for more information about the subscription checkbox.  An open order must have the **Re-encumber** checkbox activated to be eligible for fiscal year rollover. For each order type listed, select the appropriate settings for each of the fields defined below:

*   **Rollover.**  Check this box if you want encumbrances for open orders of this type of order to roll over to the upcoming fiscal year budget associated with each order.  Checking this box will activate the  **Based on** and **Increase by, %** fields.
*   **Based on.**  From the drop-down list, select **Expended** to encumber the total amount that was expended during the current fiscal year. Select **Initial encumbrance** to encumber the purchase order line estimated price. Select **Remaining** to encumber the amount that has not yet been paid.
*   **Increase by, %.**  Enter a value if you want to increase the encumbrance amount by a defined percentage.   


### Viewing rollover log results

Rollover logs and results  are available for each rollover event.  To view rollover log results, follow these steps:

1. In the **Search & filter** pane, click **Ledger.**
2. Use the search and filter tools, if needed, to find the ledger for which to view rollover log results.
3. In the ledger results pane, select the name of the ledger.
4. The ledger detail pane will open. Open the Action menu and select **Rollover logs.**
5. The rollover log window opens containing a search and filter pane on the left and a table list of rollover logs on the right that displays the following information:

*   **Start time.** Date and time at which rollover or rollover test was initiated.
*   **End time.** Date and time at which rollover or rollover test was completed.
*   **Status.** Status of the rollover or rollover test: In progress, Successful, Failed.
*   **Errors.** If errors exist, a file name in format ‘mm/dd/yyyyy-error’ displays.  Click on the file name to download a .csv file containing error information.
*   **Results.** If rollover completes successfully, a file name in format ‘mm/dd/yyyyy-result’ displays. Click on the file name to download a .csv file containing results information.  See [Rollover log results file](#rollover-log-results-file) below for the list of fields in the file.
*   **Settings.** A file name in format ‘mm/dd/yyyyy-settings’ displays. Click on the file name to download view a screen capture of the settings in place for the rollover or rollover test.
*   **Source.** The name of the process that created the rollover log: Rollover or Rollover test.

#### Rollover log results file

The following fields are included in the downloadable rollover log results file:

*   Name (Fund)
*   Code (Fund)
*   Status (Fund)
*   Type
*   Group (Code)
*   Acquisition unit
*   Transfer from
*   Transfer to
*   External account number
*   Description
*   Name (Budget)
*   Status (Budget)
*   Allowable encumbrance
*   Allowable expenditure
*   Initial allocation
*   Increase
*   Decrease
*   Total allocation
*   Transfers
*   Total Funding
*   Encumbered (Budget)
*   Awaiting payment (Budget)
*   Expended (Budget)
*   Credited (Budget)
*   Unavailable
*   Over encumbered
*   Over expended
*   Cash balance
*   Available
*   Name (Exp Class)
*   Code (Exp Class)
*   Status (Exp Class)
*   Encumbered (Exp Class)
*   Awaiting payment (Exp Class)
*   Expended (Exp Class)
*   Credited (Exp Class)
*   Percentage of total expended


#### Filtering the rollover log table list

To filter the rollover log table list using the **Search & filter** pane, apply one of the following filters: 

*   **Start time.** Date and time at which rollover or rollover test was initiated. Enter a start from and to date/times and click **Apply** to filter log results to a start date/time range.
*   **End time.** Date and time at which rollover or rollover test was completed. Enter from and to date/times and click **Apply** to filter log results to an end date/time range.
*   **Status.** Status of the rollover or rollover test: In progress, Successful, Failed.
*   **Source.** The name of the process that created the rollover log: Rollover or Rollover test.
