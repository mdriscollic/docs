---
title: "Reading room access"
linkTitle: "Reading room access"
weight: 45
date: 2024-11-18
---


The Reading room access app allows you to approve or deny access to Reading rooms. Reading rooms are created in [Settings > Tenant > Reading room access](../../../settings/settings_tenant/settings_tenant/#settings--tenant--reading-room-access). You can edit a user’s [Reading room access](../../../users/#reading-room-access) and [Reading room notes](../../../users/#reading-room-access) in the Users app. 

## Permissions
The permissions listed below allow you to interact with the Reading room access app, create Reading rooms, and edit users access to Reading rooms. You can assign permissions to users in the Users app. If the first permission is not assigned to a user, then they will be unable to see the Reading room access app or any related information.

* **Reading room access: In app - track access.** This permission allows users to open and use the Reading room access app.
* **Settings (tenant): Can create, edit and remove reading room access.** This permission allows users to view, create, edit, and delete reading rooms in [Settings > Tenant > Reading room access](../../../settings/settings_tenant/settings_tenant/#settings--tenant--reading-room-access).
* **Settings (tenant): Can view reading room access.** This permission allows users to view reading rooms in [Settings > Tenant > Reading room access](../../../settings/settings_tenant/settings_tenant/#settings--tenant--reading-room-access).
* **Users: Can view reading room access.** This permission allows users to view the Reading rooms a user has and has not access to. It does not allow editing which reading rooms the user has access to. Note that the user needs to have an assigned User type.
* **Users: Can view, and edit reading room access.** This permission allows users to view and edit a user’s [Reading room access status](../../../users/#reading-room-access) and add [Reading room notes](../../../users/#reading-room-access). Note that the user needs to have an assigned User type. This permission also allows editing of other areas of the User record.

## Locating a patron in the system
You need to be signed into a service point the reading room is associated with before looking up a patron. 

You can find the patron by either:

* Scanning / entering the barcode provided by the patron.
* Using the Patron Look-up function.

Locate the patron using a barcode:

1. Either scan the barcode on the patron’s library card, or enter the patron barcode number.
2. Click **Enter**. Patron details are displayed. The access status to the Reading room associated with the logged in user’s service point is shown.

Locate the patron using the Patron look-up function:
1. In the Scan patron card pane, click **Patron look-up**.
2. In the **Select User** dialog, in the **User search** box, enter part or all of the patron’s name, email, or username.
3. Optional: Filter results by Status (active/inactive), or by Patron group.
4. Click **Search**.
5. Click the patron to use. The Select User dialog closes, the barcode appears in the Scan patron card pane, and the patron details are displayed. The access status to the Reading room associated with the logged in user’s service point is shown.

Note: Unlike in the **Check out** app, Patron look-up will only return results if the patron has a barcode. 

## Allowing reading room access

1. [Look up the patron](#locating-a-patron-in-the-system).
2. You will see the patron’s reading room access (**allowed** or **not allowed**) and any notes.
3. Select **Allowed** or **Not allowed**.

Note: Inactive users will display an Inactive user message under their patron details. The allowed and not allowed buttons do not display for inactive users.

You can access the log of approvals and denials via the **/reading-room/access-log** API endpoint.
