---
title: "Check out"
linkTitle: "Check out"
date: 2021-12-03
weight: 20
---

The Check out app allows you to check out items to patrons. To check out an item, first locate a patron in the system and then scan/enter an item to lend.


## Permissions

The permissions / capabilities listed below allow you to interact with the Check out app and determine what you can and cannot do within the app. You can assign User roles to users in the Users app, or in the Settings > Authorization roles app. You need to assign at least one of the following capabilities to a user to enable the user to see the Check out app or any related information.


To add a capability or capability set to an Authorization role: 

Select all applications to ensure access to all capabilities.

1. Open the Capability sets or Capability accordion (see description in the table below for whether to look for a Capability set or a Capability).
2. Look under the matching Type.
3. Find the Resource (you can search using Ctrl-f/Cmd-f).
4. Select the Action.

See [Settings > Authorization roles](../../../settings/settings_authorization-roles/settings_authorization-roles) for instructions on how to create and assign Authorization roles.



| Permission Display    Name (OKAPI)     | Resource (EUREKA)            | Type       | Action  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------|------------------------------|------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Check out: All permissions             | UI-Checkout                  | Data       | Manage  | This Capability set allows users to check out items to patrons (create new loans). It does not allow users to view open loans or requests or the entire user record.                                                                                                                                                                                                                                                                                                                                                                                                            |
| Check out: Check out circulating items | UI-Checkout Circulation      | Procedural | Execute | This Capability set allows users to check out items, but does not allow viewing open loans or requests or the entire user record.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Check out: View fees/fines             | UI-Checkout ViewFeeFines     | Data       | View    | This Capability allows users to click the fee in the **Scan patron card** pane to view the patron’s fees/fines in the Users app. For the link to work, the user must have permission to view fees/fines in the Users app. See, for example the capability set **Users: Can view fees/fines and loans** ([Users \> Capabilities and Capability Sets](../../../users/#capabilities-and-capability-sets)). A user who has **Check out: all permissions** but does not have **Check out: View fees/fines** will see a patron’s fee/fine amount in the **Scan patron card** pane as text (not as a link).                                                                                                                                                                                                                  |
| Check out: View loans                  | UI-Checkout ViewLoans        | Data       | View    | This Capability allows users to click the number of open loans in the **Scan patron card** pane to view the patron’s current loans in the Users app. For the link to work, the user must have permission to view loans in the Users app. See, for example the capability set **Users: User loans view** ([Users \> Capabilities and Capability Sets](../../../users/#capabilities-and-capability-sets)).  A user who has **Check out: all permissions** but does not have **Check out: View loans** will see how many loans a patron has in the **Scan patron card** pane as text (not as a link).                                                                                                                                                                                                                |
| Check out: View requests               | UI-Checkout ViewRequests     | Data       | View    | This Capability allows users to click the number of open requests in the **Scan patron card** pane to view the patron’s current requests in the Requests app. For the link to work, the user must have permission to view requests in the Requests app. See, for example the capability set **Requests: View** ([Requests \> Permissions](../../requests/requests/#permissions)). A user who has **Check out: all permissions** but does not have **Check out: View requests** will see how many requests a patron has in the **Scan patron card** pane as text (not as a link). |
| User: Can override item blocks         | UI-Users Override-Item-Block | Procedural | Execute | This Capability set allows users to override non-circulating loan policies.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Users: Can view profile pictures       | UI-Users Profile-Pictures    | Data       | View    | This Capability set allows users to view profile pictures at Check out.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



## Locating a patron in the system

You can find the patron by either:

*   Scanning / entering the barcode provided by the patron.
*   Using the Patron look-up function.

Locate the patron using a barcode:

1. Either scan the barcode on the patron's library card, or enter the patron barcode number.
2. Click **Enter**. Patron details are displayed.

Locate the patron using the Patron look-up function:

1. In the Scan patron card pane, click **Patron look-up**.
2. In the **Select User** dialog, in the **User search** box, enter part or all of the patron's name, email, or username.
3. Optional: Filter results by Status (active/inactive), or by Patron group.
4. Click **Search**.
5. Click the patron to use. The Select User dialog closes, the barcode appears in the Scan patron card pane, and the patron details are displayed.

If a patron's record has a note that is checked to display in the Check out app, the note will appear as a pop-up window after the patron details are displayed.

### Patron details displayed

After [Locating a patron](#locating-a-patron-in-the-system), patron details will display. 
Patron details include:

* Name: The patron’s name, displayed as \[Last name], \[Preferred first name]. If there is no [Preferred first name](../../../users/#user-information) in the patron’s user record, then \[First name] is displayed.
* Pronouns: The patron’s pronouns will display in parentheses after their name, if the pronoun field contains data in the patron’s user record.
* Barcode: The patron’s barcode.
* Profile picture: If [Profile pictures](#displaying-profile-pictures-at-check-out) are enabled in the FOLIO tenant, they will display after the patron’s name and barcode.
* Patron group: The patron’s Patron group.
* Status: either Active or Inactive.
* User expiration: The date the patron’s borrowing privileges will expire / have expired.
* Open loans: The number of open loans the patron has. If the logged-in user has the appropriate permissions, this displays as a link.
* Fees/fines owed: The total fees/fines owed. If the logged-in user has the appropriate permissions, this displays as a link.
* Open requests: The number of open requests the patron has. If the logged-in user has the appropriate permissions, this displays as a link.
* Patron blocks: If the patron has any blocks, they are shown here.

Note: If the patron is acting as a proxy, then the sponsor's patron details are displayed first.


### Accessing the patron's data

You can access additional information related to the user within the patron details area. Clicking on any linked information opens the appropriate app and displays the associated information. For example, if the FOLIO user has the appropriate permissions, clicking the number beneath Open requests will open a list of the patron's open requests in the Requests app.

Review the available information to determine if you can continue with check out. For example, fees or fines may be owed, and may need to be handled before proceeding.


## Checking out to a proxy borrower

Proxy borrowers are patrons who are checking out items on the behalf of another patron. For example, a graduate assistant may act as a proxy for a professor.

Note: A patron must first be assigned as a proxy for the borrower in their user record in the [Users app](../../../users/#add-a-proxy).

1. [Locate the proxy borrower in the system.](#locating-a-patron-in-the-system)
2. In the **Who are you acting as?** dialog, select the name of the user for whom the patron is acting as a proxy and click **Continue**. The Who are you acting as? dialog closes and patron and proxy details are displayed.

## Scanning the item to check out

Make sure you have [looked up the user record](#locating-a-patron-in-the-system) prior to scanning items.

To select the item for check out, scan or enter the barcode of the item and click **Enter**. The item appears in the Scan Items area with the **Due date** and **Time**. The total number of items scanned increases.

A flag icon will appear next to the item due date after checkout if the item will be due sooner than expected. This can happen if a service point will be closed when the item would normally be due, if there is a recall on the item, or if the patron's account is set to expire sooner than the expected due date/time.

### Pop-ups that can occur when checking out an item

While checking an item out to a patron, you may encounter one of the following pop-ups:

* Item status
* Check out notes
* Multiple and/or missing pieces
* Patron block
* Item block
* Override circulation policy


## Getting additional item information

To access more information about each item:

* Click **... > Item details** to open the Inventory app and get additional item details.
* Click **... > Loan details** to open the Users app and access options including renewals, claiming the item was returned, changing the due date, and declaring the item lost. You can also view or add patron info or staff info comments.
* Click **... > Loan policy** to open the Settings app for more loan policy information.


## Changing the due date of an item

To change the due date:

1. Click **... > Change due date**.
2. In the **Change Due Date** dialog, enter the date and/or time for the new due date.
3. Click **Save and Close**. The new due date is saved.

## Printing due date receipts

You can print due date receipts at check out. Due date receipts can include borrower and loan due date information. You can configure the information that appears on the due date receipt in the [Settings app](../../../settings/settings_circulation/settings_circulation/#settings--circulation--staff-slips).

To print due date receipts, follow these steps:

1. Click **… > Loan details** to open the Users app.
2. Click **Print due date receipt**. A print dialog appears.


## Adding a loan comment

You can use loan comments to store ILL transaction numbers, record a reason for a changed due date, or track how many times a claimed returned item was searched for. You can include patron info comments as a token in patron notices (only the most recent comment is included in the token). You need to have the appropriate permissions to be able to add patron or staff info loan comments -- see [Users \> Permissions](../../../users/#permissions).

To add a patron info loan comment:

1.	Click **… > Add patron info** to add a patron info note.
2.	In the **Add patron information** dialog, enter a comment in the box.
3.	Click **Save and Close**. The new comment is saved and any previous patron loan comment is superseded. The comment will appear in the Comment column in Loan details in the checkout app, and will also be recorded in the Circulation Log.
4.	Patron info loan comments can also be added in Loan details -- see [Getting additional item information](#getting-additional-item-information).

To add a staff info loan comment:

1.	Click **… > Add staff info** to add a staff info note.
2.	In the **Add staff information** dialog, enter a comment in the box.
3.	Click **Save and Close**. The new comment is saved. The comment will appear in the Comment column in Loan details in the checkout app, and will also be recorded in the Circulation Log. Old staff info comments cannot be edited; add a new staff info comment instead.
4.	Staff info loan comments can also be added in Loan details -- see [Getting additional item information](#getting-additional-item-information).

## Displaying profile pictures at check out 
To view profile pictures at check out:

* Profile pictures need to be enabled in the FOLIO tenant. 
* The logged in user needs to have permission to view profile pictures.

Profile pictures display in a 100 pixel x 100 pixel area to the right of the Borrower box. If the borrower has no profile picture, then a placeholder image is displayed. If the patron is acting as a proxy, then the profile pictures of the proxy and sponsor display to the right of their respective Borrower boxes.


## Ending the check out session

Once you have completed checking out items for a patron, you can end the session manually. To end your session and clear the Scanned Items table, click **End session**. Once you end the session, any applicable notices are sent to patrons.

By default, the Check out session is configured to end automatically after a 3 minute period of inactivity. You can turn this setting off or edit the number of minutes of inactivity the session will end after in the [Settings app](../../../settings/settings_circulation/settings_circulation/#automatically-end-check-in-and-check-out-session-after-period-of-inactivity).
