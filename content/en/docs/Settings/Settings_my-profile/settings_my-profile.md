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

The **Application display order** setting determines the display order of FOLIO applications in the navigation menu using a numerical list. Applications are displayed in numerical order from left to right. 

In Settings \> My profile, you can customize the display order of the FOLIO applications that you have permission to access.

To customize the display order of FOLIO applications in the top navigation menu:

1. In the **My profile** pane, click **Application display order**. A numerical list of all FOLIO applications that you have permission to access appears in the **Application display order** pane. 
2. Applications can be reordered in the display using the **Drag & Drop** method. Hover over an application until the hand icon appears, then drag and drop it into its new position in the list. 
3. Click **Save**. 

To reset the display order of FOLIO applications in the top navigation menu to the default setting:

1. In the **My profile** pane, click **Application display order**. A numerical list of all FOLIO applications that you have permission to access appears in the **Application display order** pane. 
2. Click the **Reset to default** button in the top right corner of the **Application display order** pane. 
3. Click **Save**. The display order of FOLIO applications reverts to the default setting.
 

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
