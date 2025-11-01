---
title: "Settings > My profile"
linkTitle: "My profile"
date: 2025-05-08
weight: 175
tags: ["subtopic"]
---

The My profile section in the Settings app allows the user to customize and save the display order of FOLIO applications in the UI or change their FOLIO password.


## Capabilities

The Eureka platform, adopted in the Sunflower release, replaces permission sets with **Capabilities** and **Capability sets** for role-based management of user accounts.

For more information about **Capabilities**, **Capability sets**, and their attributes, see [Roles Management in Eureka](https://folio-org.atlassian.net/wiki/x/BIATLw).

The following **Capabilities** allow interaction with the My profile section of the Settings app.

For all Settings \> My profile capabilities:

 - **Application** is *app-platform-complete*.
 - **Type** is *settings*.

| permissionDisplayName (OKAPI) | Resource (EUREKA) | Action |
| :----- | :----- | :-----: |
| *Settings (My profile): Can change your local password* | *UI-Myprofile Settings Change-Password* | view |
| *Settings (My profile): Can change application order in main navigation* | *UI-Myprofile Settings Main-Nav-Order* | manage |


## Application display order

The **Application display order** setting determines the display order of FOLIO applications in the navigation bar and menu. By default, applications are displayed in alphabetical order in the current locale. For example, if the locale is English the four applications Check in, Check out, Settings, and Users would be displayed in that order. If the locale is French, the default order of the same four applications would be Settings (Parametres), Check out (Prêt), Check in (Retour), Users (Utilisateurs).

The **Application display order** setting in Settings \> My profile allows you to choose the order of the FOLIO applications you have permission to access, overriding the default alphabetical sort.

To customize the display order:

1. In the **My profile** pane, click **Application display order**. An ordered list of all the FOLIO applications you have permission to access appears in the **Application display order** pane. Applications are listed top to bottom and left to right in LTR locales (e.g. English). Applications are listed top to bottom and right to left in RTL locales (e.g. Arabic).
2. Applications can be reordered in the display using the **Drag & Drop** method or via keyboard controls. Hover over an application until the hand icon appears, then drag and drop it into its new position in the list.
3. Click **Save**.

To restore the default order:

1. In the **My profile** pane, click **Application display order**.
2. Click the **Reset to default** button in the top right corner of the **Application display order** pane.
3. Click **Save**. The display order of FOLIO applications reverts to the default setting.

If your permissions change, granting or revoking access to some applications, and you have customized the order of applications:

* Applications you gain access to will be added at the end of the list in the **Application display order** pane.
* Applications you lose access to will be removed from the list in the **Application display order** pane.


## Change password

The **Change password** option in Settings \> My profile allows the user to change their FOLIO password.

To change your FOLIO password:

1. In the **My profile** pane, click **Change password**.
2. In the **Change password** pane, type in your current FOLIO password. Toggle the **Show password** and **Hide password** to display your typing accordingly.
3. Type the new password in the **New FOLIO password** and **Confirm FOLIO password** fields. Passwords must contain:


    - at least one numeric character;
    - at least one special character;
    - no keyboard sequence of characters;
    - both lowercase and uppercase letters.


4. Click **Save** to save the new FOLIO password. The green toast message, *The FOLIO password for [FOLIO username] was saved successfully*, appears at the bottom of the screen.
