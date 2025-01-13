---
title: "Serials Management"
linkTitle: "Serials Management"
date: 2024-11-14
weight: 55
tags: ["parenttopic"]
---
**This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may be aligned with a different FOLIO release.**

The Serials app allows to create serial records that store information about the status of the order, the title in the Receiving app, a description, a purchase order (PO) line and notes. The app also allows to create publication patterns and generate predicted piece sets. The receiving pieces you generate in the Serials app are shared with the Receiving app. 
To create a serial it is necessary to create an order and PO line in the Orders app in advance. 

Definition of terms related to the Serials app:

*   **Combination rules.** Combination rules can be applied to combine issues in a publication cycle.
*   **Cycle length.** The amount of time it takes for a single cycle of the publication pattern to complete.
*   **Days of publication, per cycle.** The day(s) on which an issue is published, within one cycle of the publication pattern.
*   **Label.** Labels define the enumeration and chronology for the issues of a serial. 
*   **Omission rules.** Omission rules can be applied to remove individual issues in a publication cycle. 
*   **Pattern ID.** Is a unique ID that refers to a created publication pattern.
*   **Piece sets.** A predicted piece set shows information like date generated, pattern ID and a list of the next expected issues.
*   **Publication cycle.** This records how often issues are published, how many are published in that time and on what days they are published. 
*   **Publication pattern.** This sets up everything about the expected publications of a serial so that it can generate the appropriate pieces and label them correctly.
*   **Serial.** A serial record provides a way of linking together various pieces of information for a serial like order line, publication pattern and predicted piece sets.
*   **Template.** A template defines how values from the enumeration and chronology labels are to be used in each predicted piece. 
*   **Token.** In a template, tokens are used as a placeholder for different labels of the publication pattern.


## Permissions

The permissions listed below allow you to interact with the Serials app and determine what you can or cannot do within the app. You can assign permissions to users in the Users app. If none of these permissions are assigned to a user, they are unable to see the Serials app or any related information.

Serials permissions:

*    **Serials: Create predicted pieces.** This permission allows the user to generate predicted pieces.
*    **Serials: Delete predicted pieces.** This permission allows the user to delete predicted pieces.
*    **Serials: Edit publication patterns.** This permission allows the user to edit publication patterns.
*    **Serials: Edit serials.** This permission allows the user to edit serial records.
*    **Serials: Search & view predicted pieces.** This permission allows the user to search and view predicted pieces. 
*    **Serials: Search & view serials.** This permission allows the user to search and view predicted pieces.
*    **Settings (Serials): Manage pick lists and values.** This permission allows the user to manage pick lists and values in the settings.
*    **Settings (Serials): View pick lists and values.** This permission allows the user to view pick lists and values in the settings.
*    **Settings (Service-interaction). View number generator settings and use number generators within apps.** 
*    **Settings (Service-interaction). Manage number generator settings and use number generators within apps.** View, create, edit, delete number generators and sequences.

Note: Only one of the service-interaction permissions is required for the user to be able to work with the Serials app. 

## Keyboard shortcuts
Keyboard shortcuts allow you to perform actions in this app using the keyboard.  See [Platform essentials > Keyboard shortcuts](../../platform-essentials/keyboard-shortcuts/keyboardshortcuts/) for more information.


## Creating a new serial

To create a serial record it is necessary to create an order and PO line in the Orders app in advance. 

1. In the **Serials** pane, click **New**.

2. In the **New serial** window, select **Select PO line**. Search for the PO line you would like to link with this serial record and click on it in the **Order lines** pane. The PO line is now linked to the new serial record and information about the order number, order status, acquisition units, product IDs, vendor, funds, material type and the title is shown.

3. Set the **Status (required)** accordingly, active or closed, add an optional **description** and optional **notes**.

4. **Save & Close** 

After choosing a PO line it is still possible to replace the PO line by clicking **Replace PO line** in the Serial record. It is also possible to delete the PO line by clicking the trash bin icon next to the **Replace PO line** button.

Clicking on the PO line in the Serials record takes you to the **Orders app**. 

Clicking on **View in inventory** takes you to the **Inventory app**.




## Adding a publication pattern
To add a publication pattern, you first need to create a serial. A serial record can have one publication pattern with an "Active" status at any one time, but can have multiple publication patterns with non-active statuses: "Deprecated" for ones that are no longer used, and "Draft" for ones being planned or setup for the future. When adding a new pattern older patterns automatically receive the status "Deprecated".

1. In the **Search & filter** pane, search for the serial to which you would like to add a publication pattern. Click on the record in the **Serials** pane. 

2. In the **Serials** record under the tab **Publication pattern**, click **Add publication pattern**.

3. Select **Status (required)**, active or deprecated or draft, and add an optional description. 

4. Fill in the **Publication cycle**.

5. Optional: Add **Omission rules** when you would like to remove indivual issues in your publication cycle.

6. Optional: Add **Combination rules**, which can be applied to combine sequences of issues into a single issue. 

7. **Add label(s)**, which have two **label styles (required)**: chronology and enumeration. Use the **template (required)** to display the order of the specified labels correctly in the intended publication pattern.
  
8. Optional: **Preview** your publication pattern.

9. **Save & Close** 

### Publication cycle

The publication cycle consists of the **cycle length** and the **days of publication, per cycle**.

#### Cycle length
1.    **Time unit (required).** The time unit can be selected from the following options: Day, Week, Month and Year. 

2.    **Number of the time units (required).** Enter the number of the time unit you have specified before, or use the arrow icons to increase or decrease the number.

3.    **No. of issues published per cycle (required).** Enter the number of issues published within one cycle of the pattern,  or use the arrow icons to increase or decrease the number. 

For example, for a monthly publication an **publication cycle** might be setup as follows: 
* Time unit: Month
* Number of months: 1
* No. of issues published per cycle: 1

A mnemonic for defining the **cycle length** could be as follows: Every [number of the time unit] [time unit] [No. of issues] issue/s is/are published.


#### Days of publication, per cycle
Days of publication, per cycle is only displayed once you have entered the cycle length.

1. **Choose a day format (required)**: "Day (1-31)" or "Day (Mon-Sun), Week (1-4)"

2. Depending on which day format you have selected, only **Day** or **Day** and **Of week** will be visible for you to fill in.

For example, a monthly issue published on the fourth Monday would be created as follows: 
* Day format: Day (Mon-Sun), Week (1-4)
* Day: Monday
* Of week: 4

### Adding omission rules

Running the publication pattern will generate a minimum of one year's worth of predicted issues. Omission rules can be applied to remove individual issues. For example, to omit a public holiday, a specific month or week, or the "nth" issue from the year's set of predicted issues. 

1. Click **Add omission rule**. 

2. The **Time unit** can be selected from the following options: Day, Week, Month and Issue. After choosing a time unit, the **Omission rule type** becomes visible.

3. The **Omission rule type** varies depending on what **Time unit** is selected. For example, the time unit "Week" has two options: "Week (1-52)" and "Week (1-4), Month (Jan-Dec)". By selecting "Week (1-52)" you can then decide whether you want to omit one specific week or omit several weeks.
The checkbox **Omit range of [time unit]** only appears for the time units **Week** and **Month**.

4. Click **Add omission rule** again, if you need more than one omission rule.

#### Omission rule type

Time unit: **Day**
* Day (1-31), Month (Jan-Dec)
* Day (Mon-Sun), Week (1-52)
* Day (Mon-Sun), Week (1-52), Month (Jan-Dec)
* Day (1-31)
* Day (Mon-Sun)

Time unit: **Week**
* Week (1-52)
* Week (1-4), Month (Jan-Dec)

Time unit: **Month**
* Month (Jan-Dec)

Time unit: **Issue**
* Issue (1-n)
* Issue (1-n), Week (1-52)
* Issue (1-n), Week (1-4), Month (Jan-Dec) or 
* Issue (1-n), Month (Jan-Dec)

### Adding combination rules
1. Click **Add combination rule**. 

2. Select **Issue** under **Time unit**. Afterwards the **combination rule type** becomes visible.

3. Choose one of the following **Combination rule type**: 
    * Issue (1-n)
    * Issue (1-n), Week (1-52)
    * Issue (1-n), Week (1-4), Month (Jan-Dec) or 
    * Issue (1-n), Month (Jan-Dec)

    The rule type and associated fields will pinpoint the first issue to be    included in the combination. Depending on which rule type has been         selected, different fields are displayed that must be filled in. Afterwards enter the **Total number of issues to combine**.

4. Click **Add combination rule** again, if you need more than one combination rule.
    
For example, a combinded July and August issue of a monthly published publication would be defined as follows:

* Combination rule type: Issue (1-n), Month (Jan-Dec)
* Issue: 7
* Of month: July
* Total number of issues to combine: 2

### Define labelling
1. Click **Add label**.

2. Choose the **label style** for your first label. Choose from **Chronology** or **Enumeration**:
    * Chronology: Fill in Chronology format (Date, Month, Year) and Locale
        * Weekday format: Monday, MONDAY, Mon, MON
        * Month day format: 3, 3rd
        * Month format: October, 10, Oct
        * Year format: 2024, 24 
        
    * Enumeration: Fill in Enumeration format (Enumeration Numeric or Enumeration Textual)
    
        *Numeric:*
        * No. of units 
        * Format: Number (1, 2, 3), Ordinal (1st, 2nd 3rd), Roman numerals (I, II, III)
        * Sequence: Continuous, Reset
        * Internal note
        
        Click **Add level** if your label contains more than one enumeration, e.g. volume and issue.
        
        *Textual:*
        * Pick list: e.g. Season 
        * No. of issues
        * Label text
        * Internal note
        
        Click **Add value** if your label contains more than one textual enumeration.

3. If required, add another label with **Add label**.

4. Use the **Template** field to specify how values from the enumeration and chronology labels are to be used in each predicted piece. 

#### Using templates

Writing a template requires you to know to include the appropriate values from each chronology and enumeration label you have set up. To use a value from an enumeration or chronology in the template, you will need to put a token in double curly braces in the template. The token will identify which enumeration or chronology label is being used, and which part of the label is being used. All other text in the template (i.e. text not in double curly braces) will be treated as simple text that should be included. 

By clicking **Preview** it is possible to preview the labels for the publication pattern to make sure the expected pieces will be labeled and generated correctly.

Table for token examples:

| Type of label | Part of label | Token example |
| -------- | -------- | -------- |
| Chronology | Weekday | {{chronology1.weekday}} |
| Chronology | Month day | {{chronology1.monthDay}} |
| Chronology | Month   | {{chronology1.month}} |
| Chronology | Year     | {{chronology1.year}} |
| Enumeration (numeric) | Level 1 number | {{enumeration1.level1}} |
| Enumeration (numeric) | Level 2 number | {{enumeration1.level2}} |
| Enumeration (numeric) | Level n number | {{enumeration1.leveln}} |
| Enumeration (textual) | Value | {{enumeration1}} |

Note: If a second chronology label is added it is named chronology2. If a second enumeration label is added it is named enumeration2. 

For example, a pattern with 2 issues per year with labeling "Volume 45, number 1 (2024)" is defined as follows:

**Label 1:**
* Label style: Enumeration
* Enumeration Format: Enumeration Numeric 

*Level 1 (volume):* 
* No. of units: 1 
* Format: Number 
* Sequence: Continuous 

*Level 2 (issues):* 
* No. units: 2 
* Format: Number 
* Sequence: Reset 

**Label 2 (year):**
* Label style: Chronology 
* Chronology format: Chronology Year
* Locale: English
* Year format: 2024 

**Template:** 
Volume {{enumeration1.level1}}, number {{enumeration1.level2}} ({{chronology1.year}})


More information about templates: ["Using Templates" by Owen Stephens]( https://folio-org.atlassian.net/wiki/spaces/FOLIOtips/pages/154861687/Using+Templates) 

## Generating predicted pieces
To generate predicted pieces, you first need to add a publication pattern to your serial.

1. In the Serial record pane, click **Actions** and then **Generate predicted pieces**

2. Enter a **Start date (required)** and an optional note.

3. Enter the values to be used for the first issue **(required)**.

4. Optional: Click **Preview** to preview the predicted pieces.

5. Click **Generate**.

6. A predicted piece set record is created automatically and linked to the Serials record. An unique **Pattern ID** that refers to this publication pattern is created as well.

Clicking on the date in the Serial record pane under **Predicted piece sets** takes you to the Predicted piece set record. 

In the **Search & filter** pane with **Piece sets** selected you can search for the pattern ID (without leading zeros) of your piece set. 

The pattern ID can be customised. (Link will be added.)

## Generating receiving pieces
To generate receiving pieces, you first need to generate predicted pieces.

1. In the **Predicted piece set** record, click **Actions** and then **Generate receiving pieces**.

2. If there are locations or holdings for the linked PO line you are able to select location or holding for the receiving pieces. 

3. Fill in **Time between publication and receipt (days) (required)**. This describes the time interval between the date that the piece is published and when it is received at the location.

4. Select **Supplement** if the piece is a supplementary material such as a CD or a map.

6. Click **Generate receiving pieces**.

Selecting **Generate receiving pieces** will create new expected pieces in the **Receiving app**. You can view the pieces in the **Receiving app** under the **Expected** tab. 

The **Predicted piece set** record will be updated in the **Serials app**. 

Clicking on the publication title under **Title in Receiving** in the **Predicted piece set** record takes you to the title in the **Receiving app**. Clicking on the publication title under **Serial** takes you the Serial record of the title.
