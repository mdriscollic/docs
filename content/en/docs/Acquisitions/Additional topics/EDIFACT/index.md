---
title: "EDIFACT"
linkTitle: "EDIFACT"
date: 2025-11-26
weight: 08
tags: ["subtopic"]
---

This section of the documentation contains links to external sites. Please be advised that these sites are not maintained by the FOLIO Documentation Group and may be aligned with a different FOLIO release.

FOLIO supports electronic ordering, claiming, and invoicing using the EDIFACT standard. More information about the EDIFACT standard is available on the [FOLIO Wiki](https://folio-org.atlassian.net/wiki/spaces/FOLIOtips/pages/467435632/EDIFACT+Invoices+Field+Mapping+Profiles). It is recommended that libraries contact their vendors to notify them when they plan to use FOLIO for EDIFACT ordering, claiming, and/or invoicing so that the vendor can provide all required infromation and additional testing support, as needed.

Setup for EDIFACT ordering, claiming, and invoicing spans multiple FOLIO apps. A library may choose to configure only those areas that are relevent to local institutional procedures. The sections below cover relevant setup for each area and information related to corresponding workflows.

## EDIFACT Ordering
FOLIO allows a user to initiate an order within the Orders app, then transmit that order to a vendor in EDIFACT format.

### Setup
Initial setup for EDIFACT ordering occurs within the [Organizations app](../../organizations/). An organization record must be created and configured with an **Active** status and a **Vendor** designation. Once created and saved, the record must have [integration details configured](../../organizations/#adding-integration-details-to-a-vendor-organization). 

Ensure the integration type is set to **Ordering** and contact the vendor to request the following information:
* **Vendor EDI code**
* **Vendor EDI type**
* **Library EDI code**
* **Library EDI type**
* **EDI FTP**
* **FTP mode**
* **FTP address**
* **FTP connection mode**
* **FTP username and password, if needed**
* **FTP port**
* **Order directory**

Once all required and desired information is entered into the **Create integration** page, save the integration.

### Initiating EDIFACT Orders


## EDIFACT Claiming
FOLIO allows a user to initiate an claim for unreceived materials within the Claiming or Receiving apps, then transmit that order to a vendor in EDIFACT format. 

### Setup
Initial setup for EDIFACT claiming occurs within the [Organizations app](../../organizations/). An organization record must be created and configured with an **Active** status and a **Vendor** designation. Once created and saved, the record must have [integration details configured](../../organizations/#adding-integration-details-to-a-vendor-organization). 

Ensure the integration type is set to **Claiming** and contact the vendor to request the following information:
* **Vendor EDI code**
* **Vendor EDI type**
* **Library EDI code**
* **Library EDI type**
* **EDI FTP**
* **FTP mode**
* **FTP address**
* **FTP connection mode**
* **FTP username and password, if needed**
* **FTP port**

**Please note:** If a library wishes to use **File download** as the **Transmission method** for claims, the FTP information is not required.

Once all required and desired information is entered into the **Create integration** page, save the integration.

### Initiating EDIFACT Claims

## EDIFACT Invoicing
FOLIO allows a user to import an electronic invoice in EDIFACT format using the Data import app, resulting in a new invoice record within the Invoices app.

### Setup
Initial setup for EDIFACT invoicing occurs within the [Settings app, under Data import settings](../../../settings/settings_data_import/settings_data_import/). Each vendor requires a separate data import job profile, which will consist of both a field mapping and an action profile. The FOLIO community has worked with several common industry vendors to create default field mapping profiles that adhere to the mapping decisions used by each vendor. It is recommended that FOLIO libraries duplicate the default field mapping profiles to retain the originals in case mistakes are made with configuration or a vendor requires multiple job profiles.

**Within Settings > Data import > Field mapping profiles:**
1. Locate the default profile for the relevant vendor. If the vendor is not listed, iecommended to contact the FOLIO Community Data Import SIG for assistance.
2. Duplicate the default profile.
3. In the duplicated profile:
   * Update the profile name.
   * Update the profile description.
   * Assign an acquisition unit, if desired. **Please note:** if the profile uses an acquisition unit, the FOLIO user that initiates the Data import job must be a member of the assigned acquisition unit.
   * Assign a batch group.
   * Assign a vendor.
   * Assign a payment method.
   * Verify the remaining default mapping values are correct based on the data included within an EDIFACT invoice file from your vendor.
   * Configure optional fields as desired.
   * Save as profile & Close.
  
**Within Settings > Data import > Action profiles:**
1. Create a new action profile.
2. Within the new action profile:
   * Name the action profile.
   * Add a description if desired.
   * Select **Create** as the **Action**.
   * Select **Invoice** as the **FOLIO record type**.
   * Link the field mapping profile created using the steps listed above.
   * Save as profile & Close.

**Within Settings > Data import > Job profiles:**
1. Create a new job profile.
2. Within the new job profile:
   * Name the job profile.
   * Add a description, if desired.
   * Add the action profile created using the steps listed above.
   * Save as profile & Close.
  
This process may be repeated for each vendor with whom a library wishes to participate in EDIFACT invoicing.

### Initiating EDIFACT Invoicing
After Data import job profiles are configured in the Settings app, imports can be initiated within the [Data import app](../../../data-import/) using a file received from the vendor. Please note that the file from the vendor must have one of the following file extensions:
* .edi
* .inv

1. Upload the file from the vendor by locating it within the file explorer or dragging and dropping the file into the app.
2. Select the appropriate job profile.
3. Click **Actions > Run**.

When the job completes, the resulting job log will provide a link to the created invoice line(s). If the job results in errors, the error messages may be viewed within the log.

Imported invoices can be located in the **Invoices app** by using the **Source** filter and selecting **EDI**. All invoices created using Data import will have an **Open** status, so that they can be reviewed and edited, if desired, prior to [approval](../../invoices/#approving-an-invoice) and [payment](../../invoices/#paying-an-invoice). They may also be deleted without any impact to your financial transactions in FOLIO since the transaction does not begin until the invoice is approved.

**Please note:** FOLIO uses the FOLIO POL number and the vendor reference number as matchpoints to link purchase order lines to invoice lines. If the link is not created on import, this typically indicates one of the following:
1. No matching POL exists within the FOLIO Orders app,
2. The field mapping profile used within the job profile contains an incorrect mapping for one or both of these fields, or
3. The file from the vendor omits these fields or contains inaccurate values.

FOLIO users may manually link POLs to invoice lines after import or may delete the originally imported invoice, correct the error, and re-import.



