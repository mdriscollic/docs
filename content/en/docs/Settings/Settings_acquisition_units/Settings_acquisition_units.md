---
title: "Settings > Acquisition units"
linkTitle: "Acquisition units"
date: 2025-04-16
weight: 10
tags: ["subtopic"]   
---

The Acquisition units section of the Settings app is where you can configure your acquisition units and assign users to the units you created.

Acquisition units are an additional layer you can add to acquisitions records that restrict a user’s ability to interact with those records unless they have been assigned to that unit. While acquisition capabilities may allow a user to perform certain actions within a particular app to any record within that app, acquisition units can further limit user access to only individual records.

For example, a university that shares FOLIO across multiple independent libraries, such as a Law Library, Medical Center Library, and Undergraduate Library could set up separate acquisition units for each library and assign staff from each library to the appropriate unit. Only staff within an assigned acquisition unit could take allowed actions on orders, organizations, invoices, or funds that share the same acquisition unit assignment. Even if a Law Library user has authorization to create and delete records within the Finance app, they would still be restricted from creating or deleting a Medical Center Library fund if they are not assigned to the Medical Center Library acquisition unit.

Acquisitions units can be applied to the following types of records in FOLIO:

*   Fiscal years
*   Ledgers
*   Groups
*   Funds
*   Invoices
*   Orders
*   Organizations
*   Receiving titles


## Capabilities

The capabilities listed below allow you to interact with the Acquisition units settings. You can assign capabilities to users via user roles. If none of these capabilities are assigned to a user, they are unable to see the Acquisition units settings or any related information.

It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities.

|**Permission Display name (OKAPI)** | **Resource (EUREKA)** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Settings (acquisition units): Can view, edit, create and delete acquisition units.** | **UI-Acquisition-Units Settings** | settings | manage | This capability allows you to view, edit, create, and delete acquisition units.|
|**Settings (acquisition units): display list of settings pages** | **Settings Acquisition-Units Enabled** | settings | view | This capability displays the acquisition units area of the Settings app to the user.|
|**Settings (acquisition units): Manage acquisition unit user assignments.** | **Acquisition Units Settings User Assignment** | settings | manage | This capability allows you to assign users to acquisition units.|
|**Settings (acquisition units): View acquisition units.** | **UI-Acquisition-Units Settings** | settings | view | This capability provides view-only access to the acquisition units area of the Settings app.|



## Creating an acquisition unit

1. In the **Acquisition units** pane, click **New**.

2. Enter the **Name** of the unit in the box.

3. Select the types of actions members in the unit can perform:



*   **View.** Users assigned to the unit are the only ones who can view records that have the unit assigned. If you want to allow all users to view the records that have this unit assigned, do not select this checkbox. 
*   **Edit.** Users assigned to the unit are the only ones who can edit records that have the unit assigned.
*   **Create.** Users assigned to the unit are the only ones who can add the unit to a record they are creating.
*   **Delete.** Users assigned to the unit are the only ones who can delete records that have the unit assigned.

4. Click **Save**. The unit is saved and appears in the Acquisition units pane.


## Assigning users to an acquisition unit

Note: Users can be assigned to more than one acquisition unit.

1. In the **Acquisition units** pane, find the acquisition unit you want to assign the user to and select it.

2. In the **Acquisition unit detail** pane, click **Assigned users > Assign users**.

3. In the **Select User** dialog, in the **User search** box, enter part or all of the user’s name.

4. Optional: Filter results by Status (Inactive/Active), or by Patron group.

5. Click **Search**.

6. Select the **checkbox** in the row of the users(s) you want to add to the unit and click **Save**. The Select User dialog closes and the user appears in the Assigned users section.


## Deleting a user from an acquisition unit

1. In the **Acquisition units** pane, find the acquisition unit you want to delete the user from and select it.

2. In the **Acquisition unit detail** pane, locate the user you wish to delete under the **Assigned users** accordion.

3. Click the **trash can icon** at the end of their row. The user is removed from the list and deleted from the unit.


## Editing an acquisition unit

1. In the **Acquisition units** pane, find the acquisition unit you want to edit and select it.

2. In the **Acquisition unit detail** pane, click **Actions > Edit**.

3. Edit the acquisition unit.

4. Click **Save**. The acquisition unit is updated.


## Deleting an acquisition unit

Note: You cannot delete acquisition units that have users assigned to them. Acquisition units can be deleted if in use on records in acquisition apps. This may leave a broken reference on these records, so it is recommended to check for usage of the acquisition unit within these apps prior to deletion.

1. In the **Acquisition units** pane, find the acquisition unit you want to delete and select it.

2. In the **Acquisition unit detail** pane, click **Actions > Delete**.

3. In the **Delete acquisition unit** dialog, click **Confirm**. The acquisition unit is deleted and is removed from the Acquisition units pane.
