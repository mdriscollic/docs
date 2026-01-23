---
title: "Settings > Mosaic integration"
linkTitle: "Mosaic integration"
date: 2026-01-22
weight: 173
tags: ["subtopic"]   
---

**This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may be aligned with a different FOLIO release.**

The Mosaic integration section of the Settings app allows you to define your configuration for an integration with the provider Mosaic. This integration supports the creation of FOLIO orders initiated from the Mosaic platform. This integration applies only to firm orders for electronic monographs. For more information on the Mosaic integration with FOLIO, please review [this FAQ on EBSCO Connect](https://connect.ebsco.com/s/article/Mosaic-Integration-with-FOLIO-Frequently-Asked-Questions?language=en_US). Please note: the Mosaic integration was developed to be compatible with FOLIO’s Eureka platform.

## Capability Sets

The capability sets listed below allow you to interact with the Mosaic integration settings. You can assign capability sets to users via user roles. If none of these capability sets are assigned to a user, they are unable to see the Mosaic integration settings or any related information.

All capability sets listed below are part of the app-mosaic application. It is recommended that you select all applications prior to assigning capabilities to ensure you have access to all capabilities.


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
The Mosaic integration uses a Default order template to populate fields in the order and purchase order line on the resulting record in FOLIO. 

The default template that is used is called **Mosaic eBooks Default**. The contents of this template may be viewed by accessing the template under [Settings > Orders > Order templates](../../settings_orders/settings_orders/#settings--orders--general--order-templates).

To change the default template to be used by the Mosaic integration:
1.	Ensure the template has been created under [Settings > Orders > Order templates](../../settings_orders/settings_orders/#settings--orders--general--order-templates). 
2.	Open Settings > Mosaic integration > Configuration options.
3.	Select the desired template from the dropdown menu.
4.	Click Save.
   
When placing an order in Mosaic, an institution may choose any existing order template from their FOLIO environment to be applied when Mosaic creates that order in FOLIO. If no template is chosen at point of order, the template selected in settings will be applied. 

