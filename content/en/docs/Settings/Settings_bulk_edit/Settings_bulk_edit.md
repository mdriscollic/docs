---
title: "Settings > Bulk edit"
linkTitle: "Bulk edit"
date: 2026-06-10 
weight: 28
tags: ["subtopic"]
---

The Bulk edit section in the Settings app provides configuration options for managing bulk edit profiles. Bulk edit profiles are predefined templates that help librarians perform bulk edits in a consistent and controlled manner. Instead of manually configuring each bulk edit job, users can create and reuse profiles that define what data to change and how.


## Capabilities and Capability Sets

The following **Capabilities** allow for interaction in Settings > Bulk edit. 

For all Settings > Bulk edit capabilities: 

- **Application** is *app-bulk-edit*.
- **Type** is *settings*.

| Resource (EUREKA) | Action | 
| :----- | :-----: | 
| *Settings Bulk-Edit Enabled* | view |
| *UI-Bulk-Edit-Settings* | view |
| *UI-Bulk-Edit-Settings* | create |
| *UI-Bulk-Edit-Settings* | delete |
| *UI-Bulk-Edit-Settings Lock* | edit |


## Creating a bulk edit profile

1.  Navigate to **Settings → Bulk Edit**, and select a record type under **Inventory profiles** or **Other profiles**.
2.  Click the **New** button to open the profile creation form (for holdings, items, or users) or the **Actions** button (for Instances only, after which you will see options for new profiles).
3.  In the **Summary** accordion fill out information about the profile so that it can easily be identified during the bulk edit job execution.
4.  In the **Bulk Edits** section, specify the data changes, similar to how you would configure them in the Bulk edit form within the Bulk edit app.
5.  Click **Save & close.** Once saved, the profile is immediately available for use within the Bulk edit app.

## Editing an existing profile

1.  Navigate to **Settings → Bulk edit**, and select a record type under **Inventory profiles** or **Other profiles**.
2.  Click the row with the profile that needs to be edited. Once the form with the profile opens, from the **Actions** menu select **Edit**.
3.  Make required changes, then click **Save & close.**

## Duplicating a profile

1.	Navigate to **Settings → Bulk Edit**, and select a record type under **Inventory profiles** or **Other profiles**.
2.	Click the row with the profile that needs to be edited. Once the form with the profile opens, from the **Actions** menu select **Duplicate**. That opens a new profile creation form, prepopulated with the data from the original profile. The name of the profile is prefixed with “Copy of”.
3.	Make required changes, then click **Save & close.**

## Locking and unlocking a profile

1.	Navigate to **Settings → Bulk Edit**, and select a record type under **Inventory profiles** or **Other profiles**.
2.	Click the row with the profile that needs to be edited. Once the form with the profile opens, from the **Actions** menu select **Edit**.
3.	Click **Lock profile**. The selected value will lock the profile and the unselected value will make the profile unlocked.
4.	Locking the profile makes it read-only and prevents deletion. Locked profiles can only be duplicated.

## Deleting a profile
1.	Navigate to **Settings → Bulk Edit**, and select a record type under **Inventory profiles** or **Other profiles**.
2.	Click the row with the profile that needs to be edited. Once the form with the profile opens, from the **Actions** menu select **Delete**.
3.	Confirm deletion of the profile. The profile is removed and not available any longer for use in bulk edit jobs within Bulk edit app. **Note**: Deleted profiles cannot be restored.
