---
title: "Settings > Mosaic integration"
linkTitle: "Mosaic integration"
date: 2026-05-15
weight: 173
tags: ["subtopic"]   
---

**This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may be aligned with a different FOLIO release.**

The Mosaic integration section of the Settings app allows you to define your configuration for an integration with the provider Mosaic. This integration supports the creation of FOLIO orders initiated from the Mosaic platform. This integration applies only to firm orders for electronic monographs. For more information on the Mosaic integration with FOLIO, please review [this FAQ on EBSCO Connect](https://connect.ebsco.com/s/article/Mosaic-Integration-with-FOLIO-Frequently-Asked-Questions?language=en_US). Please note: the Mosaic integration was developed to be compatible with FOLIO’s Eureka platform.

## Capabilities & capability Sets

The capabilities and capability sets listed below allow you to interact with the Mosaic integration settings. You can assign capabilities and capability sets to users via user roles. If none of these capabilities or capability sets are assigned to a user, they are unable to see the Mosaic integration settings or any related information.

All capabilities and capability sets listed below are part of the app-mosaic application. It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities and capability sets.


|**Permission Display name** | **Resource** | Type | Action | Description |
| -------- | ------- | ------- | ------- | ------- |
|**Mosaic API module - all permissions.** | **Mosaic** | data | manage | This capability set includes all capabilities needed to change the default template used by the Mosaic integration. This is a recommended capability set to assign to users requiring access to Mosaic integration settings for this version.|
|**Settings (Mosaic integration): View and edit settings.**| **UI-Mosaic-Settings Settings** | settings | edit | This capability set includes all capabilities needed to view the Mosaic integration settings and update the template used within configuration options. This is a recommended capability set to assign to users requiring access to Mosaic integration settings for this version.|
|**Mosaic Configuration API - all permissions.**| **Mosaic Configuration** | data | manage | This capability set is a subset of the capabilities included in the Mosaic capability set. |
|**Mosaic settings module is enabled.**| **Settings Mosaic-Settings Enabled** | settings | view | This capability set includes all capabilities needed to view the Mosaic integration settings and configuration options. |
|**Settings (Mosaic integration): View settings.**| **UI-Mosaic-Settings Settings** | settings | view | This capability set includes the capabilities required to view the Configuration options heading within the Mosaic integration area of Settings. |

## Implementation considerations
Libraries planning to implement the Mosaic integration will be required to work with the Mosaic team to configure the integration. To begin, a library will communicate the following to the Mosaic team:
* Mosaic account number
* Institution name
* Contact person email address

Once configuration is completed with the Mosaic team, a library may need to update the default order template referenced by the integration within FOLIO. 

**Settings > Mosaic integration > Configuration options**
The Mosaic integration uses an order template to populate fields in the order and purchase order line on the resulting record in FOLIO. 

Libraries may [create an order template] (../../settings_orders/settings_orders/#creating-an-order-template) for use with the integration or click the **Generate integration templates** button to have the system create the template and organization record for use with the integration. Note: system-generated templates and organization records may be edited and deleted by authorized users.

To select or change the default template to be used by the Mosaic integration:
1.	Ensure the template has been created under [Settings > Orders > Order templates](../../settings_orders/settings_orders/#settings--orders--general--order-templates). 
2.	Open Settings > Mosaic integration > Configuration options.
3.	Select the desired template from the dropdown menu.
4.	Click Save.
   
When placing an order in Mosaic, an institution may choose any existing order template from their FOLIO environment to be applied when Mosaic creates that order in FOLIO. If no template is chosen at point of order, the template selected in settings will be applied. 

