---
title: "Invoice adjustments"
linkTitle: "Invoice adjustments"
date: 2024-12-04
weight: 10
tags: ["subtopic"]
---

Adjustments are an optional feature within the Invoices app in FOLIO.

## What is an invoice adjustment?
An adjustment is an addition to an invoice record that accounts for charges that are supplemental to the cost of acquired materials, like shipping or tax.

## How do I add an adjustment to an invoice?
An adjustment can be added at the invoice level or to an individual invoice line. 

To add an adjustment to the invoice level, see [Adjustments](../../invoices/#adjustments) for instructions.

To add an adjustment to an invoice line, see [Adjustments](../../invoices/#adjustments-1) for instructions.

## How do I select the correct pro-rate option?
When adding an adjustment to an invoice, staff must select one of the following options for **Pro rate**:
* By line
* By amount
* By quantity
* Not prorated

**By line** will distribute the cost of the adjustment equally across all invoice lines, so each line absorbs an equal amount within its total. For example:
An invoice has two invoice lines: line 1 has a quantity of 5 and subtotal of $50, line 2 has a quantity of 4 and a subtotal of $100.
* A $10 adjustment is applied and prorated by line.
* Each line absorbs $5 of the adjustment.

**By amount** will distribute the cost of the adjustment proportionally across all invoice lines, so lines with a higher subtotal will absorb more of the adjustment than those with lower subtotals. For example:
An invoice has two invoice lines: line 1 has a quantity of 5 and subtotal of $50, line 2 has a quantity of 4 and a subtotal of $100.
* A $10 adjustment is applied and prorated by amount.
* Line 1 absorbs $3.33.
* Line 2 absorbs $6.67, since the subtotal of this line is twice the subtotal of line 1.

**By quantity** will distribute the cost of the adjustment proportionally across all invoice lines, so lines with a higher quanity will absorb more of the adjustment than those paying for lower quantities of material. For example:
An invoice has two invoice lines: line 1 has a quantity of 5 and subtotal of $50, line 2 has a quantity of 4 and a subtotal of $100.
* A $10 adjustment is applied and prorated by quantity.
* Line 1 absorbs $5.56.
* Line 2 absorbs $4.44, since this line is paying for a lower quantity of material.

**Not prorated** indicates that the adjustment will not be absorbed by any invoice line. Instead, staff must select a fund to use for payment of the adjustment.

## How do I select to correct 'Relation to total' for an invoice adjustment?
When adding an adjustment, staff must select one of the following options for **Relation to total**:
* In addition to
* Included in
* Separate from

Each option has a separate use case, so please use the definitions and examples below to select the appropriate option for your use case.

**In addition to** indicates that the amount of the adjustment should be added to the subtotal of the invoice or invoice line. A use case would be if a library wishes to break out a shipping cost that must be paid on top of the cost of materials.
For example: if the entered subtotal is $10 and a 10% adjustment is added with the selection of **In addition to**:
* The entered subtotal will be used to calculate the adjustment amount.
* The adjustment will be $1 (10% of $10).
* The subtotal will remain $10.
* The adjustment will be added to the subtotal and the calculated total amount will be $11.

**Included in** indicates that the amount of the adjustment is already bundled within the subtotal, so the specified subtotal already includes material cost, plus the adjustment. A use case would be when the material cost includes the cost of the item's associated sales tax.
For example: if the entered subtotal is $10 and a 10% adjustment is added with the selection of **Included in**:
* The entered subtotal will be used to calculate the adjustment amount.
* The adjustment will be $0.91 (10% of the material cost, rounded to the nearest cent).
* The subtotal will decrease to $9.09 (the cost of the material, minus the calculated adjustment for tax).
* The new subtotal plus the calculated adjustment will combine to equal the original $10 subtotal.

**Separate from** indicates that the adjustment amount should not impact the calculated total amount of the invoice. A use case may be import duties that need to be reported on the invoice, but not paid as part of the invoice because another entity is responsible for payment.
For example: if the entered subtotal is $10 and a 10% adjustment is added with the selection of **Separate from**:
* The entered subtotal will be used to calculate the adjustment amount.
* The adjustment will be $1 (10% of $10).
* The subtotal will remain $10.
* The adjustment will not impact the subtotal and the calculated total amount will be $10.


## Is there a way to save adjustments that are commonly applied to invoices?
Yes, for commonly used adjustments, it is recommended that these be added to **Settings > Invoices** as [preset adjustments](../../../settings/settings_invoices/settings_invoices/#settings--invoices--adjustments), which can be applied to relevant invoices. If a library wishes to apply a preset adjustment to every invoice, check the **Always show** box. The adjustment will be proactively applied to every newly created invoice, but may be edited or deleted on each individual invoice, as needed.  
