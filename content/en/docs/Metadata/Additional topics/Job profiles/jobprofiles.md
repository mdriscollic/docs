---
title: "Job profiles"
linkTitle: "Job profiles"
weight: 10
tags: ["subtopic"]
---
# How to Create Job Profiles

## How Profiles Work Together

Job profiles are assembled from several different types of sub-profiles. These components define a logical sequence of actions on incoming records. Job profile data must be in **MARC** or **EDIFACT** format. A job profile processes a MARC or EDIFACT data file by applying match, action, and field mapping sub-profiles in order.

## Example Job Profile Structures

### Overlay on an Instance and Create Attached Holdings and Item Records (Incoming MARC Record)

> A suppressed instance already exists, created by Acquisitions and linked to a POL. The cataloger overlays it with the finalized catalog record and simultaneously creates holdings and item data.

* **Match profile (instance)** — Incoming `949$a` to instance HRID
* **Action profile (instance)** — Update instance (uses default MARC-Instance mapping)
* **Field mapping (instance)** — Set Instance status to “Cataloged”; enter today’s date in *Cataloged date*
* **Action profile (holdings)** — Create attached holdings record
* **Field mapping (holdings)** — Set Permanent location to “Main”; map `050_4` to Call number
* **Action profile (item)** — Create item record attached to holdings
* **Field mapping (item)** — Assign *Can Circulate* as permanent loan rule

### Remove Existing 856 Fields from a Batch of E-Resource Records (Incoming MARC Record)
Acquisitions creates a suppressed instance linked to an order. MARC field mapping removes existing 856s.

* **Action profile (MARC SRS)** — Modify incoming MARC data
* **Field mapping profile (MARC SRS)** — Delete all existing `856` fields
* **Action profile (instance)** — Create instance (uses default MARC-Instance mapping)
* **Field mapping (instance)** — Set Instance status to “Uncataloged” and mark *Suppress*



### Overlay Existing Instances to Transform Call Numbers in Holdings (Incoming MARC Record)
Titles need new call numbers. Records are exported (with holdings HRIDs in `960$f`), edited in MarcEdit, and re-imported.

* **Match profile (MARC to Instance)** — Incoming `001` to instance HRID
* **Match profile (MARC to holdings)** — Incoming `960$f` to holdings HRID
* **Action profile (holdings)** – Update holdings
* **Field mapping (holdings)** – Map `050_4` to Call number field

## Different Types of Profiles

### Match Profiles

* **Optional** — Used when operating on existing records in Inventory
* Designate a match point between incoming data and a FOLIO record or SRS field
* Enable overlay/update logic
* Can be **nested** for cascading logic

  * Example: Match on instance HRID → Update instance → Match on holdings HRID → Update holdings

### Action Profiles

* **Required**
* Define **what** operation to perform and **on what** type of record

  * Example: Create item record, Update instance
* Must be **paired** with a **field mapping profile**
* One action profile can be linked to **only one** field mapping profile
* Must be tailored for specific scenarios

### Field Mapping Profiles

* **Required**
* Insert incoming data into Inventory record fields

  * Example: Map `999` from MARC to holdings permanent location
* Must be **paired with** an action profile
* Can be reused with **multiple** action profiles
* Consider creating consistent **naming conventions** for easier search and organization
* Can coordinate with **Data Export** profiles

  * Example: Export maps holdings location to `960$a`, which is used in Data Import as a match point

## Creating a Job Profile

All sub-profiles must be created before creating a job profile. 
_Guides for creating sub-profiles are forthcoming_

**Steps to Create a Job Profile**:

 1. Open **Settings**
 2. Choose **Data Import** from the left-hand menu
 3. Click **Job profiles** in the Profiles pane
 4. Click **Actions** (top-right) → **+New Job Profile**
 5. Enter a **name** and **description**
    **TIP**: Use a naming convention (e.g., `ERM1`, `CAT1`) to identify job type
    **TIP**: Make descriptions detailed (e.g., "Matches on holdings HRID in 960\$f; updates holdings electronic access from 960\$c")
 6. Click the **plus** button under **Overview**
 7. Add the necessary sub-profiles
 8. Click **Save and close**
  
**NOTE:** You can edit existing job profiles, but you **cannot reorder sub-profiles**. Sub-profiles can only be added or removed.

---
