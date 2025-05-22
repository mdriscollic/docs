---
title: "Job profiles"
linkTitle: "Job profiles"
weight: 10
tags: ["subtopic"]
---
# How to create job profiles

## How profiles work together

Job profiles are assembled from several different types of sub-profiles. These components lay out a logical order of actions on incoming records. Incoming data for job profiles must be either in MARC or EDIFACT format. A job profile takes a file of MARC or EDIFACT data and processes it per each step specified by the match, action, and field mapping sub-profiles.

![Diagram of Job profile that contains one match profile linked to two action profiles.](./job_profiles.jpg)

## Example job profile structures

### Overlay on an instance and create attached holdings and item records (incoming MARC record)

In this scenario, a suppressed instance already exists for the title, created by the Acquisitions team and linked to a purchase order line (POL) in the Orders app. The cataloger is overlaying this instance with the finalized catalog record while simultaneously creating holdings and item data for it.

* **Match profile (instance)** — Incoming `949$a` to instance HRID
* **Action profile (instance)** — Update instance (uses default MARC-Instance mapping)
    * **Field mapping (instance)** — Set Instance status to “Cataloged”; enter today’s date in *Cataloged date*
* **Action profile (holdings)** — Create attached holdings record
    * **Field mapping (holdings)** — Set Permanent location to “Main”; map `050_4` to Call number
* **Action profile (item)** — Create item record attached to holdings
    * **Field mapping (item)** — Assign *Can Circulate* as permanent loan rule

### Remove existing 856 fields from a batch of e-resource records (incoming MARC record)
In this scenario, Acquisitions is creating an order and then creating a suppressed instance to link to that order. See the Field mapping section for more details about the specific placement of field mapping profiles that modify incoming MARC.

* **Action profile (MARC SRS)** — Modify incoming MARC data
    * **Field mapping profile (MARC SRS)** — Delete all existing `856` fields
* **Action profile (instance)** — Create instance (uses default MARC-Instance mapping)
    * **Field mapping (instance)** — Set Instance status to “Uncataloged” and mark *Suppress*

### Overlay existing instances to transform call numbers in holdings (incoming MARC record)
In this scenario, a group of titles needs new call numbers. The record subset is identified in Inventory or Lists, exported from Data Export (using a profile that puts holdings HRIDs in the `960$f`), modified in MarcEdit, and imported back into Data Import to effect the change.

* **Match profile (MARC to instance)** — Incoming `001` to instance HRID
    * **Match profile (MARC to holdings)** — Incoming `960$f` to holdings HRID
        * **Action profile (holdings)** – Update holdings
            * **Field mapping (holdings)** – Map `050_4` to call number field

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

**Steps to Create a Job Profile see ../settings_data_import/settings_data_import/#creating-an-import-job-profile**:

**TIPS**
- Use a naming convention (e.g., `ERM1`, `CAT1`) to identify job type
- Make descriptions detailed (e.g., "Matches on holdings HRID in 960\$f; updates holdings electronic access from 960\$c")
- You can edit existing job profiles, but you **cannot reorder sub-profiles**. Sub-profiles can only be added or removed.

---
