title: "Settings > Service interaction"
linkTitle: "Service interaction"
date: 2025-05-14
weight: 228
tags: ["subtopic"]


The Service Interaction section of the Settings App is where you can configure central settings like the number generators and number generator sequences.

For enabling number generators for Apps like Inventory, Receiving, Organizations please view descriptions in those Settings areas. Number generators need to be enabled separately and in addition FOLIO users need permissions listed below.

## Permissions

In order to interact with Service interaction settings, a user needs to be assigned the following permissions:


| Capability Set (Eureka) | Type | Application | Action | Descriptions |
| ---------- | ----- | ---------- | ----- | ---------- |

| Settings Service-Interaction Enabled | Settings | app-platform-complete | view | This permission/capability set allows the user to view Settings > Service Interaction |
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | view | This permission/capability set allows the user to view the number generators and number generator sequences settings and allows the user to generate numbers within apps. |
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | manage | This permission/capability allows the user to manage (view, create, edit, delete) the number generators and number generator sequences settings and allows the user to generate numbers within apps. |


In order to view or manage settings user needs to be assigned **Settings Service-Interaction Enabled** and **UI-Service-Interaction NumberGenerator** either with Action **view** or **manage**.

In order to generate numbers within apps in addition to the appropriate create and edit permissions for the individual apps user needs to be assigned **UI-Service-Interaction NumberGenerator** either with Action **view** or **manage**.
This applies for the use of number generators in Inventory, Receiving, Organizations as well as Serials Management and Open Access.


## Settings > Service Interaction > Number generators

New number generators need frontend and backend development work to integrate them with FOLIO apps. In this case use **New** to create a row for the new number generator to match with the development work.

The following number generators are available. In case the reference data is not included in your FOLIO environment please add the corresponding row (Name + Code) via **New** and store by clicking Save. Especially important are the exact codes as indicated in the following table as identifiers of the number generators.

| Name | Code | Descriptions | Type |
| ----- | ----- | ---------- | ---- |

| Inventory: Accession number | inventory\_accessionNumber | Used for Accession number in Inventory as well as in Receiving (Item level) | A |
| Inventory: Call number | inventory\_callNumber | Used for Call number on Item level in Inventory as well as in Receiving and in addition in Inventory on Holdings level | A |
| Inventory: Item barcode | inventory\_itemBarcode | Used for Item Barcode on Item level in Inventory as well as in Receiving | A |
| Open access: Publication request number | openAccess | Used as identifier "Publication request number" in the Open Access App | B |
| Organizations: Vendor code | organizations\_vendorCode | Used for Code in Organizations | A |
| Serials management: Pattern number | serialsManagement\_patternNumber | Used as identifier "Pattern number" in the Serials Management App | B |


Type A:

* One or more sequences possible to select from when create or edit records and using the number generator
* Sequences need to be defined before use at Settings > Service Interaction > Number generator sequences

Type B:

* Number automatically assigned to the record defined by one sequence
* If reference data is not included in your FOLIO environment, one sequence with the following code needs to be defined before use at Settings > Service Interaction > Number generator sequences or sequence might be changed to your requirements

| Number generator | Code of sequence |
| ----------- | --------- |
| Open access: Publication request number | requestSequence |
| Serials management: Pattern number | patternNumber |

The display in **Service interaction > Number generators** can be used as overview of possible number generators and the count of sequences:

* **Name**. The display label of the number generator. Used to group number generator sequences, and select from them in certain circumstances. Naming recommendation: App: Field e.g. Inventory: Accession number
* **Code**. A unique string representing the number generator for technical purposes. Must not contain whitespaces. Once set, this field can no longer be changed. Naming recommendation: app\_field e.g. inventory\_accessionNumber
* **Sequences**. The count of the number of sequences assigned to this generator in Settings > Service interaction > Number generator sequences.

Click the **pencil icon** under **Actions** to edit the name.

Click the **trash can icon** under **Actions** to delete the row for a number generator. Only available if no sequences are assigned. This number generator is then no longer functional.


## Settings > Service Interaction > Number generator sequences

A sequence of a number generator defines how the number will be generated and then displayed by settings of several values.

To select a number generator for managing its number generator sequences use the drop-down menu **Generator**. In the section **Sequences** existing number generator sequences will then be displayed or made searchable.

In case the reference data is included in your FOLIO environment example sequences are defined. Please delete or change according to your own requirements.

### Creating new number generator sequences

1. Select the **Generator** in the drop-down menu for which sequences should be created
2. In the **Number generator sequences** pane, click **New**.
3. In the **New sequence** window enter
       * **Name**. Name of the number generator sequence. In cases where a selection from number sequences is required, this name will be displayed in the window for generating a new number. This field is editable.
       * **Code**. Unique code of the number generator sequence. This must be unique within the number generator and contain no whitespaces. Once set, this field can no longer be changed.
       * **Enabled**. An enabled number generator sequence will be displayed when selecting the sequence in the App UI. A sequence with the status false will not be displayed in the App UI until it is enabled again.
       * **Note**. Description or information about this sequence can be entered here e.g. disabled sequence because of this reason
       * Sequence settings
            * **Maximum value**. This is the maximum possible value for the sequence. When the maximum is reached, the sequence will no longer be usable.
            * **Warning threshold value**. When set, a warning will be displayed to users of the sequence when its value is reached. Must be lower than the maximum value.
            * **Next value**. This field shows the next value in the sequence based on the current value in the database. It can be set manually as the starting value for a new sequence.
            * **Format**. The Format field defines the length of the generated number (excluding the check digit, prefix, and suffix) and supports optional padding. Use # for digits without padding (e.g., #### for four digits). To add padding, specify the character. E.g., 0000 for leading zeros, resulting in outputs like 0045. If a Maximum value is set, the Format length must match it.
       * Checksum settings
            * **Method**. The checksum method for the check digit. Use the checksum input template to define what needs to be included in the calculation e.g. prefix or suffix.
            * **Input template**. Create rules to define the number to be inputted when calculating the check digit. Both the prefix and suffix can be templated, using Groovy markup. Use ${generated\_number} as placeholder for the generated number. E.g. 05${generated\_number}01
       * Output settings
            * **Output template**. The output template defines the rules applied to create the sequence. Templates are formed using Groovy. See below for more information.
4. Once you have included all of the information you want about the sequence, click Save & close. A confirmation message appears, and the sequence is saved and appears in the Number generator sequences table.


#### Checksum settings

**Method**

Select “None” for no checksum calculation.
Methods for calculating check digits differ in weighting, direction, calculation like mod10 or mod11, calculation of remainder and other factors.
Additionally some methods are named after its creator e.g. Luhn, others may be named after the number which is generated e.g. ISSN. Those methods can be used to generally generate numbers not related to numbers they are named after.

| Name | Weighting | Direction | mod10/mod11 | Remainder | Additional information | Length |
| ---------- | ----- | ----- | ---------- | ---------- | ----------- | ------ |
| 21-RTL-mod10-I (Luhn) | 21 | right to left | 	weighted values greater than 9 have 9 subtracted <br>mod10 | (I) 10-remainder = check digit <br>no remainder = 0 | Luhn / Double-Add-Double | scalable |
| 31-RTL-mod10-I (EAN) <br>former name: EAN13 | 31 | right to left | mod10 | (I) 10-remainder = check digit <br>no remainder = 0 | Method is used for the European Article Number (EAN) / ISBN13 | scalable |
| 12-LTR-mod10-R | 12 |	left to right |	mod10 |	(R) remainder = check digit <br>no remainder = 0 | | scalable |
| 1793-LTR-mod10-R | 1793 | left to right | mod10 | (R) remainder = check digit <br>no remainder = 0 | | scalable |
| 8765432-LTR-mod11-I-X (ISSN) | 8765432 | left to right | mod11 | (I) 11-remainder = check digit <br>result = 10 → check digit = X | Method is used for ISSN <br>pattern for calculation: 8-7-6-5-4-3-2-1-0-10-9-8-... | 7 + check digit <br>scalable |
| 2345678910-RTL-mod11-I-X (ISBN10) | 2345678910 | right to left | mod11 | (I) 11-remainder = check digit <br>result = 10 → check digit = X | Method is used for ISBN10 <br>pattern for calculation: ...-14-13-12-11-10-9-8-7-6-5-4-3-2 |9 + check digit <br>scalable |


**Input template**

In those cases where the prefix and/or suffix needs to be included in addition to the sequential number generated into the calculation it can be defined via the field input template. Use ${generated_number} as placeholder for the generated number.

Examples

| Included in calculation | Example |
| ----------- | ----------- |
| no prefix/suffix | ${generated\_number} |
| prefix | 05${generated\_number} <br>358${generated\_number} |
| suffix | ${generated\_number}01 <br>${generated\_number}1 |
| prefix and suffix | 05${generated\_number}01 <br>358${generated\_number}2 |


**Output settings**

**Output template** defines the rules applied to create the sequence.

Please use Maximum value for the length and Format for padding.

        * Prefix and/or suffix can be included in the output template. (space characters are allowed)
        * In case the prefix or suffix includes $ please use \$ for displaying $
        * Use ${generated_number} for the sequential generated number
        * To include the check digit (calculation defined by method and input template) use ${checksum}

**Examples**

| Output template | Format | Next value | Display of number |
| ----------- | ------ | ------ | ---------- |
| 2025-ABC ${generated\_number} | 000 | 1 | 2025-ABC 001 |
| 2025-ABC ${generated\_number} | ### | 1 | 2025-ABC 1 |
| A1/${generated\_number}-B | 0000 | 51 | A1/0051-B |
| \$ABC ${generated\_number} | 00000 | 7 | $ABC 00007 |
| \$ABC ${generated\_number} | ##### | 7 | $ABC 7 |
| 1 N ${generated\_number}: 2013 | 0000 | 325 | 1 N 0325: 2013 |
| ${generated\_number}-${checksum} | 0000 | 45 | 0045-5 |
| A${generated\_number}${checksum} | 0000 | 45 | A00455 |
| 05${generated\_number}01${checksum} | 0000 | 45 | 050045012 |

Depending on the method selected check digits are calculated differently. In those examples check digits are examples.


### Searching and viewing number generator sequences

1. Select the number generator in the drop-down menu Generator

2. To search for number generator sequences for a number generator, enter your search term in the search box in the section **Sequences** and click **Search**. The search box searches through the Name and Code fields. In order to limit your search to specific fields, check or uncheck one or more of the **Name**, **Code**, **Note** and/or **Output template** check boxes below the search box, and the search will only search through the selected fields.

3. You can also filter on Enabled and Usage status. For more information on the filters, see the filter descriptions below.

**Enabled**

To filter sequences by enabled, select one of the following:

        * **All**. All enabled and disabled sequences.
        * **True**. Enabled sequences, which are displayed for selection in the window of the App UI
        * **False**. Disabled sequences, which are not displayed for selection in the window of the App UI.

**Usage status**

To filter sequences by Usage status, select one of the following:

        * **All**. All values are displayed
        * **At maximum**. Maximum number is reached. Sequence is no longer available for generating numbers.
        * **Below threshold**. Below warning threshold number, defined in sequence configuration for displaying warnings if desired.
        * **Over threshold**. Between warning threshold number and maximum number, defined in sequence configuration if desired.
        * **No maximum set**. No maximum number was set.


   * Results are listed in a table with pagination of 25. Use the buttons previous or next to display other pages. Number of results can be found at the right top corner of the result table.
   * To sort by a column, click the column name.
   * To view details of a sequence in the 4th pane, click on the name of the sequence in the first column.

### Editing number generator sequences

    1. Select number generator in drop-down menu **Generator**.
    2. Search for the sequence and click on name of sequence in the left column of the table to open the detail view in the 4th pane.
    3. To edit the sequence click **Edit** in **Actions** menu in the 4th pane
    4. Window **Edit sequence** will be displayed
    5. Edit sequence and **Save & close** or Cancel

Apart from the code of the sequences you can edit all other content in the edit sequence window - please be aware that changing content in edit sequences has impact on numbers being generated from this sequence in the future (e.g. it could cause duplicates or different length)

### Disable number generator sequences

    1. Select number generator in drop-down menu **Generator**.
    2. Search for the sequence and click on name of sequence in the left column of the table to open the detail view in the 4th pane.
    3. To edit this sequence click **Edit** in **Actions** menu in the 4th pane
    4. To deactivate this sequence disable the checkbox **Enabled**
    5. **Save & close** or Cancel

Deactivated sequences are no longer selectable and usable for generating numbers in the App UI.

For enabling the sequence again select the checkbox Enabled. The sequence will be displayed again when selecting the sequence in the App UI and will then continue to generate numbers from where it left off, if the sequence has not reached its maximum.

### Deleting number generator sequences

    1. Select number generator in drop-down menu **Generator**.
    2. Search for the sequence and click on name of sequence in the left column of the table to open the detail view in the 4th pane.
    3. To delete the sequence click **Delete** in **Actions** menu in the 4th pane
    4. Click **Delete** in the window Delete sequence to delete the sequence permanently or Cancel

The sequence may be in use in one or more apps. If in doubt, consider disabling the sequence instead.



## Using Number generator
## Settings > App > Number generator options

**Permissions**

In order to interact with Number generator options settings for Apps, a user needs to be assigned the following permissions:

| Capability Set (Eureka) | Type | Application | Action | Descriptions |
| ---------- | ------ | ---------- | -------- | ---------- |
| UI-Inventory Settings Mange-Number-Generator-Options | Settings | app-platform-complete | view | This permission/capability set allows the user to view and edit Number generator options for Barcode, Accession number and Call number in Settings > Inventory > Holdings, Items > Number generator options. |
| UI-Oders Settings Number-Generator | Settings | app-acquisitions | manage | This permission/capability set allows the user to view and edit Number generator options for Barcode, Accession number and Call number in Receiving in Settings > Orders > General > Number generator options. |
| UI-Organizations Settings NumberGenerator | Settings | app-acquisitions | manage | This permission/capability set allows the user to view and edit Number generator options for Code in Settings > Organizations > Number generator options. |

### Enabling Number generators for Apps like Inventory, Receiving, Organizations

In Settings > App > Number generator options three options are available via drop-down (existing radio buttons will be changed to drop-down)

    * Off = Number generator off: number can be filled manually only.
    * On, field editable = Number generator on, editable: number can be filled using the generator and be edited, or filled manually.
    * On, field not editable = Number generator on, fixed: number can be filled using the generator only.

Default setting is Off

To enable the Number generator please select either **On, field editable** or **On, field not editable**

| App | Number generator settings for |
| ---------- | ---------- |
| Settings > **Organizations** > Number generator options | Code |
| **Receiving** (Settings > Orders > General > Number generator options) | Barcode <br>Accession number <br>Call number |
| Settings > **Inventory** > General > Number generator options | Call number (Holdings) <br>Barcode (Items) <br>Accession number (Items) <br>Call number (Items) |


### Use the same generated number for accession number and call number

When the option "Use the same generated number for accession number and call number" is selected, the same generated number for accession number will be entered automatically in the main call number field by using the accession number sequences. This additional feature is available for Inventory and Receiving.

Number generator for Accession number and Call number must be enabled via "On, field editable" or "On, field not editable" to enable the checkbox.


## Using Number generators within Apps

**Preconditions for using the Number generators within Apps**

    * Number generator is enabled in Settings > "App" > Number generator options
         * On, field editable = Number generator on, editable: number can be filled using the generator and be edited, or filled manually.
         * On, field not editable = Number generator on, fixed: number can be filled using the generator only.
    * User has permissions either

| Capability Set (Eureka) | Type | Application | Action | Descriptions |
| ---------- | ----- | -------- | ------ | ---------- |
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | view | This permission/capability set allows the user to view the number generators and number generator sequences settings and allows the user to generate numbers within apps. |
| or |||||
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | manage | This permission/capability allows the user to manage (view, create, edit, delete) the number generators and number generator sequences settings and allows the user to generate numbers within apps. |


    * User has permissions to create and/or edit records (e.g. Inventory, Receiving, Organizations, Users, Serials Management, Open Access) in FOLIO depending on tasks
    * In Settings > Service interaction > Number generator sequences > Generator
        * at least one sequence is predefined for every number generator which is enabled



#### Using Number generators

**Inventory / Organizations**

If the number generator is enabled and user has the applicable permissions then a button is displayed next to the field (e.g. user barcode, vendor code, item barcode, accession number, call number).

    1. Click **Generate "field name"**
    2. Window "field name" generator is displayed
    3. Search by Name or Code of the sequences in the window "field name" generator
    4. Optional: Use check box "Include sequences which have reached their maximum value" for displaying those sequences for information. Sequences which have reached their maximum value cannot be generated from.
    5. Optional: Use check box "Exact code match" for searching the exact code
    6. Select sequence
    7. Click **Generate "field name"** to close window and generate number (or Cancel)
    8. Generated number of the selected sequence is displayed in the field
    9. After filling in all data save the entire record by clicking "Save & close" otherwise the generated number is not saved and a gap has been created.

**Receiving**

If the number generator is enabled, user has the applicable permissions and an item record is available then the number generator icon is displayed

    * Next at the right side of the item details in the Add/Edit piece window
    * In the Action column at the right side of the receive all table

    1. Click icon **Generate numbers**
    2. Window "Generate numbers" is displayed
    3. Depending on settings in Settings > Orders > Number generator options up to three sequence search fields for Barcode, Accession number and/or Call number are displayed
    4. Search by Name or Code of the sequences for each field you would like to generate a number
    5. Optional: Use check box "Include sequences which have reached their maximum value" for displaying those sequences for information. Sequences which have reached their maximum value cannot be generated from.
    6. Optional: Use check box "Exact code match" for searching the code with exact match
    7. Select at least on sequence
    8. Use x at the right side of the search fields if you would like to delete your selection
    9. Click Generate numbers to close window and generate number (or Cancel)
    10. Next value of the sequence is displayed in the field
    11. After filling in all data save the entire record by clicking "Save & close" or Receive otherwise the generated numbers are not saved and gaps have been created.

In case that **Use the same generated number for Accession number and call number** is activated in Settings (Inventory and/or Receiving)

    * In Inventory the button "Generate accession and call numbers" is displayed
    * In Receiving the selection for "Accession and call number sequence" is displayed in the window Generate numbers

Accession number sequences apply and the same generated number is inserted into the accession number and the main call number field on item level.


**Open Access and Serial management**

For the Request number in Open Access App and for the Publication pattern ID in Serials Management App numbers will be automatically assigned defined by one sequence.

In addition to the permissions for Open Access and/or Serials Management users need permission

| Capability Set (Eureka) | Type | Application | Action | Descriptions |
| ---------- | ----- | -------- | ------ | ---------- |
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | view | This permission/capability set allows the user to view the number generators and number generator sequences settings and allows the user to generate numbers within apps. |
| or |||||
| UI-Service-Interaction NumberGenerator | Data | app-platform-complete | manage | This permission/capability allows the user to manage (view, create, edit, delete) the number generators and number generator sequences settings and allows the user to generate numbers within apps. |

