---
title: "Settings > Export manager"
linkTitle: "Export manager"
date: 2026-06-30
weight: 110
tags: ["subtopic"]   
---

The Export manager section of the Settings app allows you to define your deletion intervals for job logs managed in the Export manager app. 

## Capabilities & capability Sets

The capabilities and capability sets listed below allow you to interact with the Export manager settings. You can assign capabilities and capability sets to users via user roles. If none of these capabilities or capability sets are assigned to a user, they are unable to see the Export manager settings or any related information.

All capabilities and capability sets listed below are part of the app-platform-complete application. It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities and capability sets.


|**Permission Display name** | **Resource** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Settings (Export manager): Export manager settings enabled.** | **Settings Export-Manager Enabled** | settings | view | This capability set includes all capabilities needed to see Export manager appear in the Settings sidebar, but not to allow viewing and editing of the intervals.|
|**Settings (Export manager): Can view and edit settings.**| **UI-Export-Manager Settings** | settings | edit | This capability set includes all capabilities needed to view and edit job deletion intervals.|
|**Settings (Export manager): Can view only settings.**| **UI-Export-Manager Settings** | settings | view | This capability set includes all capabilities needed to view job deletion intervals. |

**Settings > Export manager > Jobs**
Use this setting to define the interval (in days) after which jobs listed in the Export manager app should be deleted. The delete function is executed daily and unless otherwise specified in this table, records produced by jobs are deleted after 7 days, except for EDIFACT orders exports and claims, which have a default deletion interval of 730 days.

The deletion interval may be adjusted for the following job types:
* Authority control
* Bursar
* Circulation log
* Claims
* EDIFACT orders export
* eHoldings
