---
title: "Central ordering"
linkTitle: "Central ordering"
date: 2024-12-04
weight: 05
tags: ["subtopic"]
---

FOLIO environments with Enhanced Consortial Support (ECS) enabled can be configured to support ordering actvities within the central tenant, while allowing authorized staff at member libraries to receive corresponding materials within their member library tenants. With this feature enabled, libraries may still create local orders, while also benefiting from central or network ordering programs that may be in use by their consortium.

## Enabling central ordering
Within the Central tenant of an ECS-enabled FOLIO environment:
1. Navigate to **Settings > Consortium manager**.
2. Click on **Central ordering**, listed under **Network ordering**.
3. Check the box next to **Allow user to select locations from other affiliations for central orders**.
4. Click **Confirm** in the modal that appears. **Please note:** This feature cannot be disabled once this action is confirmed.
5. Click **Save**. In the current version of FOLIO, a note will appear notifying administrators that the setting can no longer be disabled.

## Configuring Receiving app behavior
When Central ordering is activated in the Central tenant, the Receiving app in the corresponding member tenants provides visibility into both central orders - those created in the Central tenant - and local orders - those created in the member library tenant. Member libraries can establish default search behavior for the Receiving app.

Within each member tenant in an ECS-enabled FOLIO environment:
1. Navigate to **Settings > Orders**.
2. Click on **Central ordering**, listed under **Network ordering**.
3. In the **Set default for receiving search** dropdown, select the desired option: **Active affiliation only** indicates that a library will only be able to access receiving records for the current member library tenant. **Central only** indicates that a library will only be able to access receiving records for orders placed in the Central tenant.  **Central default** indicates that a library will have the 'Central' tab selected by default in the Search & Filter pane of Receiving app, but will be able to switch tabs and view local orders' receiving records, as well. **Active affiliation default** indicates that a library will have the 'Local' tab selected by default in the Search & Filter pane of Receiving app, but will be able to switch tabs and view central orders' receiving records, as well.
4. Click **Save**.
   
## Central ordering workflow
Central orders must originate in the Central tenant affiliation. Creating a central order largely mimics the workflow for [creating an order record](../../orders/#creating-an-order) in any FOLIO tenant. The variation emerges when [specifying location information](../../orders/#location) on the purchase order line (POL).

**With the active affiliation set to the Central tenant:**
1. Open the Orders app.
2. Create a new order record. See [Creating an order](../../orders/#creating-an-order) for instructions.
3. Add a POL. See [Adding an order line to an order](../../orders/#adding-an-order-line-to-an-order) for instructions. **Please note:** Central orders associated with an instance record may only be associated with a shared instance record.
4. In the **Location** accordion, select an **Affiliation**. A user will only see the affiliations for which they have associated permissions.
5. In the **Select holdings** dropdown, select a pre-existing holdings record to associate the quantity with, or use the **Create new holdings for location** link to lookup a location to which this quantity will be associated. **Please note:** The **Select locations** modal will be pre-limited to the locations within the selected affiliation.
6. Enter the appropriate quantity information.
7. Once all required and desired information is entered, **Save & close**.
8. Open the order. See [Opening an order](../../orders/#opening-an-order) for instructions.

**Please note:** For POL with a quantity greater than 1, staff may select multiple affiliations and locations within the **Location** accordion. If **Receiving workflow** is set to 'Synchronized order and receipt quantity' and **Create inventory** is set to create holdings and/or items, those Inventory records will be created within the selected affiliation(s) from the **Location** accordion.

### Receiving central orders
Central orders may be received from the Central tenant affiliation or within the applicable member tenants, if configured.

**In the Central tenant affiliation:**
1. Open the Receiving app.
2. Use the **Search & filter** options to locate the receiving title record.
3. Open the receiving title record. For POL with a **Receiving workflow** set to 'Synchronized order and receipt quantity', all the pieces that are associated with the order record **and** with the staff user's authorized affiliations will be displayed in the **Expected** accordion. For POL with a **Receiving workflow** set to 'Independent order and receipt quantity', pieces may be added. See [Adding an expected piece](../../receiving/#adding-an-expected-piece) for instructions. **Please note:** When creating pieces in the Central tenant, you must specify the affiliation for the piece in addition to its location within the affiliation.
4. Receive materials as needed. See [Receiving a piece](../../receiving/#receiving-a-piece) for instructions.

**In the member tenant affiliation:**
1. Open the Receiving app.
2. Use the **Search & filter** options to locate the receiving title record. **Please note**: The Receiving app must be configured to include central orders to view this receiving title.
3. Open the receiving title record. For POL with a **Receiving workflow** set to 'Synchronized order and receipt quantity', only the pieces that are associated with the order record **and** with the active tenant affiliations will be displayed in the **Expected** accordion. For POL with a **Receiving workflow** set to 'Independent order and receipt quantity', pieces may be added. See [Adding an expected piece](../../receiving/#adding-an-expected-piece) for instructions.
4. Receive materials as needed. See [Receiving a piece](../../receiving/#receiving-a-piece) for instructions.
