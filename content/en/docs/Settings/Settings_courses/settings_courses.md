---
title: "Settings > Courses"
linkTitle: "Courses"
date: 2022-03-21
weight: 50
tags: ["subtopic"]   
---

The Courses section of the Settings app is where you manage your terms, course types, course departments, and other courses settings.

## Permissions 

Each setting within Courses has its own permission / capability set associated with it. If a user has one of the below capability sets, they will be able to view and interact with that particular setting. You can assign User roles to users in the Users app, or in the Settings > Authorization roles app.


To add a capability or capability set to an Authorization role: 

Select all applications to ensure access to all capabilities.
1. Open the Capability sets or Capability accordion (see description in the table below for whether to look for a Capability set or a Capability).
2. Look under the matching Type.
3. Find the Resource (you can search using Ctrl-f/Cmd-f).
4. Select the Action.

See [Settings > Authorization roles](../../../settings/settings_authorization-roles/settings_authorization-roles) for instructions on how to create and assign Authorization roles.

The following are all the Settings > Courses capability sets:

| Permission Display    Name (OKAPI)                              | Resource (EUREKA)        | Type     | Action | Description                                                                                                |
|-----------------------------------------------------------------|--------------------------|----------|--------|------------------------------------------------------------------------------------------------------------|
| Settings (Courses): Can create, edit and delete course settings | UI-Courses Settings      | Data     | Manage | This capability set allows users to maintain (view, add, edit, and delete) all course settings.            |
| Settings (Courses): Can view course settings                    | UI-Courses Settings View | Settings | View   | This capability set allows users to view course settings. They cannot add, edit or delete course settings. |


## Settings > Courses > Display settings

This setting controls FOLIO's behavior when duplicating a course in the Courses app via Actions > Duplicate.

If the user chooses this setting when duplicating a course, the "Duplicate all cross-listed courses" checkbox in the [Duplicate modal](../../../access/courses/courses/#duplicating-a-course) will be checked by default.

## Settings > Courses > Terms

Use this setting to create and manage Terms. Terms define the start and end date of a course. For example, when a user adds items to a course, Folio automatically assigns a Start Date and End Date to the new item as specified in the Term. If needed, you can edit the dates by editing the reserve item.


### Creating a term

1. Click **New**.
2. Enter a **Name**, **Start Date**, and **End Date** in the boxes.
3. Click **Save**. The Term is saved and appears alphabetically in the list.


### Editing a term

1. Find the Term you want to edit and click the **pencil icon**.
2. Edit the **Name**, **Start Date**, or **End Date**.
3. Click **Save**. The Term is saved.


### Deleting a term

1. Find the Term you want to delete and click the **trash can icon**.
2. In the **Delete Term** dialog, click **Delete**. A confirmation message appears and the term is deleted.


## Settings > Courses > Course Types

Use this setting to create and manage Course Types. Examples of Course Types include: Online, Hybrid, and In Person.


### Creating a course type

1. Click **New**.
2. Enter a **Name** in the box.
3. Optional: Enter a **Description** in the box.
4. Click **Save**. The Course Type is saved.


### Editing a course type

1. Find the Course Type you want to edit and click the **pencil icon**.
2. Edit the **Name** or **Description**.
3. Click **Save**. The Course Type is saved.


### Deleting a course type

1. Find the Course Type you want to delete and click the **trash can icon**.
2. In the **Delete Course Types** dialog, click **Delete**. A confirmation message appears and the term is deleted.


## Settings > Courses > Course Department

Use this setting to create and manage Course Departments. Examples of Course Departments include: Mathematics, English, and Business.


### Creating a course department

1. Click **New**.
2. Enter a **Name** in the box.
3. Optional: Enter a **Description** in the box.
4. Click **Save**. The Course Department is saved.


### Editing a course department

1. Find the Course Department you want to edit and click the **pencil icon**.
2. Edit the **Name** or **Description**.
3. Click **Save**. The Course Department is saved.


### Deleting a course department

1. Find the Course Department you want to delete and click the **trash can icon**.
2. In the **Delete Department** dialog, click **Delete**. A confirmation message appears and the department is deleted.


## Settings > Courses > Processing Statuses

Use this setting to create and manage Processing Statuses. These statuses are specific to the Courses app and can be used to reflect the status of a reserve item. Examples of Processing Statuses include: On Order, Cataloging, and Recalled.


### Creating a processing status

1. Click **New**.
2. Enter a **Name** in the box.
3. Optional: Enter a **Description** in the box.
4. Click **Save**. The Processing Status is saved.


### Editing a processing status

1. Find the Processing Status you want to edit and click the **pencil icon**.
2. Edit the **Name** or **Description**.
3. Click **Save**. The Processing Status is saved.


### Deleting a processing status

1. Find the Processing Status you want to delete and click the **trash can icon**.
2. In the **Delete Processing Status** dialog, click **Delete**. A confirmation message appears and the status is deleted.


## Settings > Courses > Copyright Statuses

Use this setting to create and manage Copyright Statuses. These statuses are specific to the Courses app and can be used to indicate the copyright of license of a reserve item. Examples of Copyright Statuses include: Public Domain, CC BY, and CC BY-SA.


### Creating a copyright status

1. Click **New**.
2. Enter a **Name** in the box.
3. Optional: Enter a **Description** in the box.
4. Click **Save**. The Copyright Status is saved.


### Editing a copyright status

1. Find the Copyright Status you want to edit and click the **pencil icon**.
2. Edit the **Name** or **Description**.
3. Click **Save**. The Copyright Status is saved.


### Deleting a copyright status

1. Find the Processing Status you want to delete and click the **trash can icon**.
2. In the **Delete Copyright Status** dialog, click **Delete**. A confirmation message appears and the status is deleted.
