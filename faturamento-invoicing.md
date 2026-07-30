---
title: "Faturamento — Extra Charges e Emissão de Invoices"
description: "Extra charge rater, accessorials, batches de faturamento, invoices imediatas e de crédito."
layout: default
---

# Faturamento — Extra Charges e Emissão de Invoices

Extra charge rater, accessorials, batches de faturamento, invoices imediatas e de crédito.

**Fluxo principal:** `GEXC/ECHP (extra charges) -> ENAC (bill later) -> BILB/BACO (batch) -> ENIN/CRIN`

> Fonte: manuais A do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Extra Charge Rater <a id="extra-charge-rater"></a>

*Manual A — Billing and Invoicing*

### Overview <a id="overview"></a>

Extra charges are miscellaneous type charges such as a bill of lading charge, per order line charge or partial pallet charge that apply to a specific receipt or order. Extra charges can be based on either inbound or outbound transactions and can apply to a customer, carrier, consignee or shipper or any combination of these parties. A charge can apply to one party and be billed to another party; for example, whenever you ship to consignee A, an extra charge is created and billed to the customer on the order.
Extra charges are cumulative. When multiple extra charges apply to the same receipt or order, each charge is calculated separately and added to the total. For example, if you have an extra charge of $1/pallet each time you ship to consignee A and an extra charge of 50 cents/pallet each time you use carrier B, an order of one pallet going to consignee A via carrier B would result in a charge of $1.50.
There are two types of extra charges:
 general extra charges set up in GEXC (General Extra Charges)
 specific extra charges set up in ECHP (Extra Charge Profile)

### GENERAL EXTRA CHARGES <a id="general-extra-charges"></a>

General extra charges are extra charges such as a bill of lading charge, per order line charge or partial pallet charge that are applied automatically to a receipt or order. General extra charges are always treated as accessorial charges and appear on the accessorial invoice. 
General extra charges are automatic charges that cannot be adjusted or overridden when processing receipts or orders. If you want the capability of manually entering or adjusting extra charges while entering a receipt or order, you cannot use general extra charges. Instead, you must set up an extra charge in ECHP (Extra 
Charge Profile).

### SPECIFIC EXTRA CHARGES <a id="specific-extra-charges"></a>

Specific extra charges are similar to general extra charges in that you use them to generate charges such as a bill of lading charge, per order line charge or partial pallet charge. However, specific extra charges differ from general extra charges in four important respects:
 they are set up in a profile that is attached to a specific customer or item
 they can be “optional” — that is, require confirmation during receipt or order processing
 they can be manually entered in RF by the RF operator
 if they are inbound charges, they can be set up as either an accessorial charge appearing on the accessorial invoice or as a receipt charge appearing on the warehouse receipt invoice 
There are two factors that determine how the ECHP charge is applied: 
 the restrictions that you enter in ECHP 
 the entity that the ECHP profile is attached to (customer, item, shipper, consignee or carrier)
NOTE You cannot apply extra charges to manual shippers, carriers and consignees. Only shippers, carriers and consignees set up in their respective maintain program (SHIP, CARR, CONS) can trigger an extra charge.

During receipt or order processing, the system will look at the restrictions, if any, that you enter in ECHP and the entity to which your ECHP profile is attached. If the order or receipt meets all conditions, an extra charge will be generated when you create your extra charge batch. 
For example, if you restrict by carrier 1 in ECHP and attach your ECHP profile to all your customers, the following will occur. For an inbound charge, the charge will apply to all inbound product carried by carrier 1 regardless of shipper or customer; for an outbound charge, the charge will apply to all outbound product carried by carrier 1 regardless of customer or consignee.

### Understanding the Charge Per Options <a id="understanding-the-charge-per-options"></a>

The charge per defines the way in which an extra charge is applied (to an entire receipt or order, to an item, to a receipt or order line, etc.). There are 18 charge per options for extra charges:
COD = COD
DHOC = Document Header for Occurrence
DOCH = Document Header
DOCL = Document Line
DOCT = Document Total
ICTL = Initial Charge Total
IHTL = Initial Handling Total
ISTL = Initial Storage Total
ITCT = Item Count
LCNT = Document Line Count
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4

### COD (CASH ON DELIVERY) — CAN ONLY BE ATTACHED TO CUST <a id="cod-cash-on-delivery-can-only-be-attached-to-cust"></a>

With this option, the charge is applied to an entire order. COD has two requirements: first, a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE and second, the freight term of 
COD attached to the order header.
DHOC (DOCUMENT HEADER FOR OCCURRENCE) — CAN ONLY BE ATTACHED 
TO CUST
With this option, the charge is applied to an entire receipt or order even if the receipt/order quantity is zero. It requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

### DOCH (DOCUMENT HEADER) — CAN ONLY BE ATTACHED TO CUST <a id="doch-document-header-can-only-be-attached-to-cust"></a>

With this option, the charge is applied to an entire receipt or order. For unit-based SKU’s, the “charge on” 
SKU for the extra charge must match one of the SKU’s in the item’s quantity breakdown before a charge is created. For example, if your “charge on” SKU for the extra charge is pallets, AccellosOne 3PL will count the number of pallets on the receipt or order. If a particular item does not have pallets in its quantity breakdown (for example, it is set up as a CASE/EACH item), it will not be counted by the extra charge rater.
The item’s quantity breakdown must contain the SKU that the extra charge is charging on
EXAMPLE
You have a cased-based extra charge for outbound orders of $1.00 per case and you have the following items on your order:
 Item 1 (PALLET/CASE/EACH)
 Item 2 (PALLET)
 Item 3 (PALLET/CASE)
AccellosOne 3PL will charge $1.00 for each case of item 1 and item 3 on the order. There will be no extra charge for item 2 product because item 2 does not have cases in its quantity breakdown. 

### DOCL (DOCUMENT LINE) <a id="docl-document-line"></a>

With this option, the charge is applied to each receipt or order line regardless of the product on the receipt or order line. For example, if you have 10 receipt lines containing identical product and that product is subject to an extra charge, the system will generate 10 extra charges, one for each line.
Item A2 quantity breakdown =
PLT/CASE/EACH
Item A1 quantity breakdown =
PLT/CASE
Item A3 quantity breakdown =
PLT/EACH
You charge on pallets You charge on cases You charge on eaches
No count for this item because there are no cases
No count for this item because there are no eaches

### DOCT (DOCUMENT TOTAL) — CAN ONLY BE ATTACHED TO CUST <a id="doct-document-total-can-only-be-attached-to-cust"></a>

With this option, the charge is applied to all receipts or orders belonging to a particular customer on an extra charge batch. For unit-based SKU’s, the quantity breakdown for all of a customer’s items must be the same; 
that is, all items must have the same quantity breakdown (for example, PALLETS / CASES) and the number of units in the quantity breakdown must be identical (for example, 100 cases per pallet). For non-unit based 
SKU’s, this restriction does not apply.
Document total extra charges cannot be billed to a third party such as another customer, a carrier, a shipper or a consignee.

### ICTL (INITIAL CHARGE TOTAL) — CAN ONLY BE ATTACHED TO CUST <a id="ictl-initial-charge-total-can-only-be-attached-to-cust"></a>

With this option, a single charge is generated based on a percentage of the total initial storage charge plus the total initial handling charge of an entire receipt. For example, if the total of both initial storage and initial handling is $100 and the charge code has a rate of 0.5, the extra charge will $50 (that is, 50% of the total initial charge). ICTL requires a charge code whose “charge on” and “qualify on” SKU types are based on 
INTV.

### IHTL (INITIAL HANDLING TOTAL) — CAN ONLY BE ATTACHED TO CUST <a id="ihtl-initial-handling-total-can-only-be-attached-to-cust"></a>

With this option, a single charge is generated based on a percentage of the total initial handling charge of an entire receipt. For example, if the initial handling total is $100 and the charge code has a rate of 0.5, the extra charge will $50 (that is, 50% of the initial handling total). IHTL requires a charge code whose “charge on” and “qualify on” SKU types are based on INTV.

### ISTL (INITIAL STORAGE TOTAL) — CAN ONLY BE ATTACHED TO CUST <a id="istl-initial-storage-total-can-only-be-attached-to-cust"></a>

With this option, a single charge is generated based on a percentage of the total initial storage charge of an entire receipt. For example, if the initial storage total is $100 and the charge code has a rate of 0.5, the extra charge will $50 (that is, 50% of the initial storage total). ISTL requires a charge code whose “charge on” and “qualify on” SKU types are based on INTV.

### ITCT (ITEM COUNT) — CAN ONLY BE ATTACHED TO CUST <a id="itct-item-count-can-only-be-attached-to-cust"></a>

With this option, a single charge is created based on the number of items on the receipt or order. If there are duplicate items on the same receipt or order, the item count is not incremented for the duplicates. For example, if you receive five items on ten lines, your extra charge will be based on the number of items (five) 
— not the number of lines. ITCT requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

### LCNT (DOCUMENT LINE COUNT) — CAN ONLY BE ATTACHED TO CUST <a id="lcnt-document-line-count-can-only-be-attached-to-cust"></a>

With this option, a single charge is created based on the number of lines on the receipt or order regardless of the product on each line. The document line count does not consolidate duplicate items. For example, you can have two items on three lines — that is, two of your lines contain the same item — but your line count will remain three and the extra charge will be based on this line count.
LCNT requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

### LTCT (LOT COUNT) <a id="ltct-lot-count"></a>

With this option, your rate is based on the number of unique level 1 and 2 entities on the receipt or order. In the following example, you have four lines but your lot count is three because lines 1 and 4 are identical.
One extra charge is generated and this charge is based on the rate defined in RATE for a quantity of 3. LTCT requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

### ULV1 (UNIQUE LEVEL 1) <a id="ulv1-unique-level-1"></a>

With this option, a single charge is generated for each unique level one value on a receipt or an order. If there are duplicate items on the same receipt or order, they are consolidated and the charge is applied to the consolidated item quantities — not the item quantities before consolidation. ULV1 is not available for variable quantity breakdown items if you are using a charge code whose SKU type is based on UNIT.

### ULV2 (UNIQUE LEVEL 2) <a id="ulv2-unique-level-2"></a>

With this option, a single charge is generated for each unique level 1/2 value on a receipt or an order. If there are duplicate level 1/2 entities on the same receipt or order, they are consolidated and the charge is applied to the consolidated quantities — not the quantities before consolidation. ULV2 is available for standard quantity breakdown items without restriction. However, ULV2 is only available for variable quantity breakdown items with the following restriction: if the charge code has a SKU type based on UNIT, all inventory entities with the same level 2 value must have the same quantity breakdown.

### ULV3 (UNIQUE LEVEL 3) <a id="ulv3-unique-level-3"></a>

With this option, a single charge is generated for each unique level 1/2/3 value on a receipt or an order. If there are duplicate level 1/2/3 entities on the same receipt or order, they are consolidated and the charge is applied to the consolidated quantities — not the quantities before consolidation. ULV3 is available for standard quantity breakdown items without restriction. However, ULV3 is only available for variable quantity breakdown items with the following restriction: if the charge code has a SKU type based on UNIT, all inventory entities with the same level 3 value must have the same quantity breakdown.

### ULV4 (UNIQUE LEVEL 4) <a id="ulv4-unique-level-4"></a>

With this option, a single charge is generated for each unique level 1/2/3/4 value on a receipt or an order. If there are duplicate level 1/2/3/4 entities on the same receipt or order, they are consolidated and the charge is applied to the consolidated quantities — not the quantities before consolidation. ULV4 is available for standard quantity breakdown items without restriction. However, ULV4 is only available for variable quantity breakdown items with the following restriction: if the charge code has a SKU type based on UNIT, all inventory entities with the same level 4 value must have the same quantity breakdown.
Line Item Lot Number
1. A 101
2. A 201
3. B 101
4. A 101

### SLV2 (SINGLE LEVEL 2) <a id="slv2-single-level-2"></a>

With this option, a single charge is generated for mixed product received on the same pallet. To activate this option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at inventory level 2.

### SLV3 (SINGLE LEVEL 3) <a id="slv3-single-level-3"></a>

With this option, a single charge is generated for mixed product received on the same pallet. To activate this option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at inventory level 3.

### SLV4 (SINGLE LEVEL 4) <a id="slv4-single-level-4"></a>

With this option, a single charge is generated for mixed product received on the same pallet. To activate this option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at inventory level 4.

### Assigning Location Billing Codes to Inbound Extra Charges <a id="assigning-location-billing-codes-to-inbound-extra-charges"></a>

For inbound extra charges, the way in which location billing codes are assigned to receipts differs according to the charge per. For all charge pers except DOCL (Document Line), if you put-away the same receipt in multiple locations and these locations have different location billing codes, the system will be forced to allocate the entire receipt to a given location billing code. For example, suppose you have the following receipt:
The system will pick the receipt line with the largest quantity (line 2) and assign its location billing code to the extra charge.

### DOCL (DOCUMENT LINE) <a id="docl-document-line"></a>

If you put-away the same line in multiple locations and these locations have different location billing codes, the system will be forced to allocate the receipt line to a given location billing code. For example, suppose you have the following receipt:
Line
Location Billing Code of location Quantity
Location Billing Code assigned to receipt
1. ALL 20 CS ???????
2. COOL 30 CS ???????
3. BULK 15 CS ???????
Line
Location Billing Code of location Quantity
Location Billing Code assigned to receipt line
1. ALL ALL
2. COOL COOL
3. BULK 15 CS ???????

Line 1 is assigned exclusively to locations with the location billing code of ALL and poses no problem. 
Likewise, line 2 is assigned exclusively to locations with the location billing code of COOL and poses no problem. However, line 3 is split between locations with the location billing code of BULK and locations with the location billing code of FREZ. The system will pick the location with the largest quantity and assign its location billing code (FREZ) to the entire line.

### Specifying Extra Charge Restrictions <a id="specifying-extra-charge-restrictions"></a>

You specify your extra charge restrictions by entering the appropriate operand and code in the Customer, 
Consignee, Shipper and Carrier Code fields in GEXC and ECHP. For example, if you specify customer A as your restriction, only orders or receipts for customer A will be charged the general extra charge. If you specify consignee B as your restriction, all orders going to consignee B regardless of customer will be charged the general extra charge.
You can specify restrictions in more than one field and an extra charge will be generated each time that a restriction is met. For example, if you attach an extra charge to customers A and B as well as to consignee C, the following will occur:
 when customers A or B ship to consignee D, the extra charge attached to the customer will be generated
 when customers A or B ship to consignee C, two extra charges will be generated — one for the extra charge attached to the customer and one for the extra charge attached to the consignee
If there is no restriction for a particular field (for example, the charge applies to all customers), leave the field blank.
3. FREZ 30 CS ???????
EXAMPLE 1 (OUTBOUND)
CUST =
CONS =
CARR =
Since there are no customer, consignee or carrier restrictions, one charge is generated for each order.
EXAMPLE 2 (OUTBOUND)
CUST = ABC
CONS =
CARR =
One charge is generated for each order belonging to customer 
ABC.
EXAMPLE 3 (OUTBOUND)
CUST = ABC
CONS = 1
CARR =
One charge is generated for each order belonging to customer 
ABC. If the consignee is consignee 1, a second charge is generated for that order.
EXAMPLE 4 (OUTBOUND)
CUST = ABC
CONS = 1
CARR = 999
One charge is generated for each order belonging to customer 
ABC. If the consignee is consignee 1, a second charge is generated for that order. If the carrier is carrier 999, a third charge is generated for that order.

You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 (for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 (for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 (=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If you exceed this limit, AccellosOne 3PL will display an error message. Remove one or two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or “<“ and “>” in the same field.

### Charging for Partial Quantities of Unit-Based SKU’s <a id="charging-for-partial-quantities-of-unit-based-sku-s"></a>

If you have two or more unit-based SKU types in the item’s quantity breakdown (for example, PALLETS/
CASES or PALLETS/CASES/EACHES) and wish to charge for partial quantities, you have two options:
 you can charge for the Entered Quantity
 you can charge for the Actual Quantity Moved
The entered quantity is the actual number of remaining units. The actual quantity moved is the difference between the actual number of remaining units and the number of units that make up a full pallet, case, carton, etc. 
For example, if your quantity breakdown for the item is 36 cases per pallet and the order calls for 24 cases (.66 pallets), the partial quantity will be 24 if you select the entered quantity option and will be 12 (36 - 24) if you select the actual quantity moved option.
There are four pairs of options for defining which SKU’s can be partials and how you wish to count the number of units in the partial. 
Actual Quantity Moved
You need 24 cases and you remove 
12 cases from a pallet holding 36
Entered Quantity
You need 24 cases and you build the pallet from scratch
NOTE The actual quantity moved is only used if the number of remaining units is greater than half a pallet. If the number of remaining units is less than half a pallet, 
AccellosOne 3PL uses the entered quantity regardless of the option that you select.
 RM2A - Entered Qty (2nd SKU)
 RM2R - Actual Qty Moved (2nd SKU)
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/ cases/eaches, cases will be considered partials. 

You can define multiple partials for the same item. For example, if your quantity breakdown is PALLETS/
CASES/EACHES, you can define a partial as eaches only, cases only or cases and eaches. Each partial SKU can have its own charge code and its own rates.
EXAMPLE
Suppose you have the following breakdown for an item:
1 pallet = 4 cases (or 12 eaches)
1 case = 3 eaches
1 each = 1 each
 RM2A - Entered Qty (2nd SKU)
 RM2R - Actual Qty Moved (2nd SKU)
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/ cases, cases will be considered a partial.
 RM3A - Entered Qty (3rd SKU)
 RM3R - Actual Qty Moved (3rd SKU)
Use one of these options if you wish to define a partial as the third SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/ cases/eaches, eaches will be considered a partial.
 RM4A - Entered Qty (4th SKU)
 RM4R - Actual Qty Moved (4th SKU)
Use one of these options if you wish to define a partial as the fourth SKU in an item’s quantity breakdown. 
For example, if your quantity breakdown is pallets/ cases/cartons/packs, packs will be considered a partial.
 RM5A - Entered Qty (5th SKU)
 RM5R - Actual Qty Moved (5th SKU)
Use one of these options if you wish to define a partial as the fifth SKU in an item’s quantity breakdown. 
For example, if your quantity breakdown is pallets/ cases/cartons/packs/eaches, eaches will be considered a partial.
 RQ2A = Entered Qty (2nd SKU - Use Last Recd 
Qty Bkd)*
 RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty 
Bkd)*
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown and the item is a variable quantity breakdown item.
With these two options, if the quantity received is greater than the item's standard quantity breakdown, the definition of a full pallet will be based on the received quantity from the last confirmed receipt plus any manual adjustments that occurred in RFMI since the last confirmed receipt.

You receive an order for 34 eaches and ship the order as follows:
2 pallets = 24 eaches
3 cases = 9 eaches
1 each = 1 eaches total = 34 eaches

### IGNORE LAST QUANTITY <a id="ignore-last-quantity"></a>

The Ignore Last Qty option allows you to skip the generation of a charge for partial quantities when picking the last remaining inventory entity in a location. For example, suppose your quantity breakdown is 80 cases per pallet and you ship out the following orders:
This option is only available for RF picking.

### SETTING UP AN EXTRA CHARGE FOR CASE PARTIALS <a id="setting-up-an-extra-charge-for-case-partials"></a>

Your quantity breakdown is PALLETS/CASES and you wish to set up a handling charge that can deal with partial quantities of cases.
1 Create a charge code in CHAR for cases. Set the “charge on” and “qualify on” values to cases and set the Round Flag to N for No Rounding.
2 Create a record in ECHP for cases. Enter your charge code for cases and set the Value Interpretation 
Description to Entered Qty (2nd SKU) or Actual Qty Moved (2nd SKU).
If your partial SKU is case: If your partial SKU is each:
The extra charge will be based on the following number of units:
Entered Qty (2nd SKU) = 3 cases
Actual Qty Moved (2nd SKU) = 1 case (4 - 3)....................
The extra charge will be based on the following number of units:
Entered Qty (3rd SKU) = 1 each
Actual Qty Moved (3rd SKU) = 1 each*
*Because entered quantity (1) is less than half a case (3), 
entered quantity = actual quantity moved.
ORDER 
NUMBER
ORDER 
QTY
REMAINING 
QTY RESULT
1 40 40 partial quantity charge generated
2 25 15 partial quantity charge generated
3 10 5 partial quantity charge generated
4 5 0 no charge for this partial quantity

### SETTING UP AN EXTRA CHARGE FOR CASE PARTIALS AND EACH PARTIALS <a id="setting-up-an-extra-charge-for-case-partials-and-each-partials"></a>

Your quantity breakdown is PALLETS/CASES/EACHES and you wish to set up a handling charge that can deal with partial quantities of cases and eaches.
1 Create a charge code in CHAR for cases. Set the “charge on” and “qualify on” values to cases and set the Round Flag to N for No Rounding.
2 Create a charge code in CHAR for eaches. Set the “charge on” and “qualify on” values to eaches and set the Round Flag to N for No Rounding.
3 Create a record in ECHP for cases. Enter your charge code for cases and set the Value Interpretation 
Description to Entered Qty (2nd SKU) or Actual Qty Moved (2nd SKU).
4 Create a second record in ECHP for eaches. Make sure that this record is attached to the same extra charge profile code as the case record. Enter your charge code for eaches and set the Value Interpretation Description to Entered Qty (3rd SKU) or Actual Qty Moved (3rd SKU).

### SETTING UP AN EXTRA CHARGE FOR NON-PARTIAL QUANTITIES <a id="setting-up-an-extra-charge-for-non-partial-quantities"></a>

You can also set up an extra charge for non-partial quantities by means of the top SKU rounded down option. 
For example, suppose your quantity breakdown is PALLETS/CASES and you wish to set up a labelling charge for each pallet. If you select the top SKU rounded down option and ship 1.25 pallets, AccellosOne 3PL will charge for one pallet.
1 Create a charge code in CHAR for pallets. Set the “charge on” and “qualify on” values to pallets and set the Round Flag to N for No Rounding.
2 Create a record in ECHP for pallets. Enter your charge code for pallets and set the Value Interpretation 
Description to PRIS (Top SKU Rounded Down).

### Setting Up General Extra Charges in GEXC <a id="setting-up-general-extra-charges-in-gexc"></a>

General extra charges apply to all orders or receipts that meet the criteria that you specify in the Customer 
Code, Carrier Code, Shipper Code and Consignee Code fields. If you leave these fields blank, the general extra charge will apply to all customers, carriers, shippers and consignees. As a result, an extra charge will be generated for each order or receipt that you process!
FIELD DESCRIPTIONS
Type I = Inbound
O = Outbound
Select I for an inbound extra charge or O for an outbound extra charge.

Sequence Number Mandatory
Each general extra charge that you create requires a unique sequence number (1, 2, 3, 4, etc.). 
Charge Code (defined in CHAR)
Mandatory
Your charge code for the general extra charge.
CAUTION The SKU type that you qualify on and charge on in this charge code must match the SKU type of all items to which the general extra charge applies. For example, you cannot set up a pallet-based charge code in GEXC and apply it to a customer whose items are defined as cases.
Charge per COD = COD
DHOC = Document Header for Occurrence
DOCH = Document Header
DOCL = Document Line
DOCT = Document Total
ICTL = Initial Charge Total
IHTL = Initial Handling Total
ISTL = Initial Storage Total
ITCT = Item Count
LCNT = Document Line Count
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4
See [Understanding the Charge Per Options](faturamento-invoicing.html#understanding-the-charge-per-options) for further information.
FIELD DESCRIPTIONS

Customer / Consignee / 
Shipper / Carrier Code
Optional but if no values are entered, the general extra charge will be generated for each receipt or order that you process
See [Specifying Extra Charge Restrictions](faturamento-invoicing.html#specifying-extra-charge-restrictions) for further information on restricting by customer, consignee, shipper, etc. 
NOTE If you bill shippers, consignees or carriers for certain charges and if on occasion you use manual shippers, consignees or carriers, you must enter the restriction “(=/)” in the Shipper/Consignee/Carrier Code field to exclude the manual account from the batch.
EXAMPLE
Suppose when shipping orders to consignee ABC, you charge a special handling fee. In the Consignee Code field, you must enter the following code: 
“=ABC,(=/)”. 
Bill to CARR = Carrier
CONS = Consignee
CUST = Customer
SHIP = Shipper
The party that will be billed for the charge. If you wish to bill the carrier, consignee or shipper for a charge, that carrier, consignee or shipper must be set up as an “invoice only” customer in CUST.
FIELD DESCRIPTIONS

### PROCEDURE <a id="procedure"></a>

1 Enter GEXC.
Quantity Based on OTOO = One to One 
OTOZ = One to One - include 0 qty line
PRIS = Top SKU Rounded Down*
RM2A = Entered Qty (2nd SKU) - Ignore Last Qty*
RM2R = Actual Qty Moved (2nd SKU) - Ignore Last Qty*
RM3A = Entered Qty (3rd SKU) - Ignore Last Qty*
RM3R = Actual Qty Moved (3rd SKU) - Ignore Last Qty*
RM4A = Entered Qty (4th SKU) - Ignore Last Qty*
RM4R = Actual Qty Moved (4th SKU) - Ignore Last Qty*
RM5A = Entered Qty (5th SKU) - Ignore Last Qty*
RM5R = Actual Qty Moved (5th SKU) - Ignore Last Qty*
RM2A = Entered Qty (2nd SKU)*
RM2R = Actual Qty Moved (2nd SKU)*
RM3A = Entered Qty (3rd SKU)*
RM3R = Actual Qty Moved (3rd SKU)*
RM4A = Entered Qty (4th SKU)*
RM4R = Actual Qty Moved (4th SKU)*
RM5A = Entered Qty (5th SKU)*
RM5R = Actual Qty Moved (5th SKU)*
RQ2A = Entered Qty (2nd SKU - Use Last Recd Qty Bkd)*
RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty Bkd)*
*DOCL, ULV1, ULV2, ULV3 and ULV4 only
This field allows you to specify the way in which you wish to charge for partial quantities. If there are no partial quantities (for example, a bill of lading charge that applies to an entire order), use One to One. 
One to One is the most common option and can be used for both unit-based 
SKU’s and weight-based SKU’s. If any partial quantities are involved, the system will round up, round down or perform no rounding depending on the option that you specify in the Round Flag field in CHAR (Charge Code). 
See [Charging for Partial Quantities of Unit-Based SKU’s](faturamento-invoicing.html#charging-for-partial-quantities-of-unit-based-sku-s) for further information on the entered quantity and actual quantity moved options.
FIELD DESCRIPTIONS

General Extra Charges (GEXC)
2 Click on Create Record.
3 Key in your type (I for Inbound or O for Outbound) and press Enter.
4 Key in your sequence number for the charge and press Enter.
5 Key in your charge code for the general extra charge and press Enter.
6 Use your pick list to select the appropriate charge per. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on 
Select to select it.
7 If required, key in a customer code in the Customer Code field and press Enter. If the charge is not specific to a particular customer, press Enter to bypass this field.
8 Repeat the above step for the Consignee Code, Shipper Code and Carrier Code fields.
9 In the Bill to field, use your pick list to select the appropriate value. A general extra charge can be billed to a customer, carrier, consignee or shipper.
10 In the Quantity Based on field, use your pick list to select the appropriate value.
11 Click on Return to Main to exit create record mode.

General Extra Charges screen showing a BOL extra charge for customer A
12 Click on Exit to exit.
13 If you create your receipts or orders through EDI, refer to [Activating Extra Charges for EDI](faturamento-invoicing.html#activating-extra-charges-for-edi) for further setup instructions.

### Setting Up Specific Extra Charges in ECHP <a id="setting-up-specific-extra-charges-in-echp"></a>

There are two factors that determine how the ECHP charge is applied: 
 the restrictions that you enter in ECHP 
 the entity that the ECHP profile is attached to (CUST, ITEM, CARR, SHIP, CONS)
Refer to the chart below for sample setups:
How you wish to charge Setup in ECHP ECHP profile attached to
You charge all your customers an extra charge when you ship their product via carrier A.
Create an extra charge profile and restrict on carrier A.
Attach the ECHP profile to all your customers.
You charge an extra charge for shipping item 1.
Create an extra charge profile with no restrictions.
Attach the ECHP profile to item 1.
You charge an extra charge for shipping item 1 to consignee A.
Create an extra charge profile and restrict on consignee A.
Attach the ECHP profile to item 1.

You charge customers A and B an extra charge when you ship their product to consignee C via carrier D.
Create an extra charge profile and restrict on consignee C and carrier D.
Attach the ECHP profile to customers A and B.
You charge customers A and B an outbound extra charge when you ship their product to consignee C via carrier D and an inbound extra charge with no restrictions.
Create an extra charge profile. In the 
Sequence Block, create an outbound charge and restrict on consignee C and carrier D and create an inbound charge with no restrictions.
Attach the ECHP profile to customers A and B.
FIELD DESCRIPTIONS
Extra Charge Profile 
Code
Mandatory
Your code for this extra charge profile.
Description Mandatory
Your description for this extra charge profile.
SEQUENCE BLOCK
Type I = Inbound
O = Outbound
Select I for an inbound extra charge or O for an outbound extra charge.
Sequence Number Mandatory
Each extra charge that you create requires a unique sequence number (1, 2, 
3, 4, etc.). 
How you wish to charge Setup in ECHP ECHP profile attached to

Charge Code (defined in CHAR)
Mandatory
Your charge code for the extra charge.
CAUTION The SKU type that you qualify on and charge on in this charge code must match the SKU type of all items to which the extra charge applies. 
For example, you cannot set up a pallet-based charge code in ECHP and attach it to an item whose quantity breakdown is cases only.
Charge per Mandatory
COD = Cash on Delivery*
DHOC = Document Header for Occurrence*
DOCH = Document Header*
DOCL = Document Line
DOCT = Document Total*
ICTL = Initial Charge Total*
IHTL = Initial Handling Total*
ISTL = Initial Storage Total*
ITCT = Item Count*
LCNT = Document Line Count*
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4
CAUTION Charge per options marked by an asterisk (*) can only be attached to CUST. If you attach these charge per options to ITEM, no charge will be generated. 
See [Understanding the Charge Per Options](faturamento-invoicing.html#understanding-the-charge-per-options) for further information on these options.
SEQUENCE BLOCK

Action Type O = Optional
A = Automatic
If you select O for Optional, the system will prompt you to confirm or cancel the charge. If you select A for Automatic, the charges will be generated automatically and you will not be able to cancel or override them. 
CAUTION The optional action type is not available for extra charges generated through a special verify program.
Entry Type Only available if Action Type = O for Optional
E = Entry
C = Confirmation
B = Both
N = None
The flow at which you are prompted to confirm the extra charge. If you select 
E for Entry, the system prompt will appear when you enter the receipt or order. 
If you select C for Confirmation, the system prompt will appear when you confirm the receipt or order. If you select B for Both, the system prompt will appear at both entry and confirmation time.
If you select N for None, no manual intervention will be allowed and the charge will be generated automatically.
Override Quantity Rules Only available if Action Type = O for Optional
E = Entry
C = Confirmation
B = Both
N = None
This field allows you to override the quantity on which the charge is based. If you select E for Entry, you can override the quantity when you enter the receipt or order. If you select C for Confirmation, you can override the quantity when you confirm the receipt or order. If you select B for Both, you can override the quantity at both entry and confirmation time.
If you do not wish to allow the quantity to be overridden, select N for None.
SEQUENCE BLOCK

ENRE screen showing Override Quantity field
Charge Date Based on B = Batch Creation Date
C = Document Confirmation Date
If you select B for Batch Creation Date, the charge date for the extra charge will the date that the extra charge batch was created in BILB. If you select C for Document Confirmation Date, the charge date for the extra charge will be the date that the receipt or order containing the extra charge was confirmed.
The charge date prints on the accessorial audit report.
Invoice Type E = Extra Billing (only available for inbound charges)
A = Accessorial
This fields allows you to specify the invoice on which the charge appears. If you select E for Extra Billing and if you generate a warehouse receipt for the customer, the charge will appear on the warehouse receipt. If you select A for 
Accessorial, the charge will appear on the accessorial invoice.
The Extra Billing option is invalid for outbound charges as all outbound charges are automatically placed on the accessorial invoice.
Allow RF Entry See “Extra Charge Setup for RF” in the RF Guide.
Allow Charge Profile 
Override in RF
See “Extra Charge Setup for RF” in the RF Guide.
SEQUENCE BLOCK

Split Order Charge N = No
Y = Yes
If you select Y for Yes, you can charge for split loads. That is, if an order is split into three loads, an extra charge based on three loads would be generated. The following setups are required in ECHP:
 Charge Code = occurrence-based charge set up in CHAR
 Type = Outbound
 Charge per = Document Header
 Split Order Charge = Yes
Flow Process Code (FLPR) for RF
See “Extra Charge Setup for RF” in the RF Guide.
Customer / Consignee / 
Shipper / Carrier Code
Optional
See [Specifying Extra Charge Restrictions](faturamento-invoicing.html#specifying-extra-charge-restrictions) for further information on restricting by customer, consignee, shipper, etc. 
NOTE If you bill shippers, consignees or carriers for certain charges and if on occasion you use manual shippers, consignees or carriers, you must enter the restriction “(=/)” in the Shipper/Consignee/Carrier Code field to exclude the manual account from the batch.
EXAMPLE
Suppose when shipping orders to consignee ABC, you charge a special handling fee. In the Consignee Code field, you must enter the following code: 
“=ABC,(=/)”. 
Hold Code If you specify a hold code in this field, the extra charge will apply only to receipt or order lines that have been placed on that hold code. 
For example, if you specify DMG as your hold code and attach your ECHP profile to the item 001, an extra charge will be generated for each receipt and/ or order line containing item 001 that has been placed on the DMG hold.
This field supports two operands for hold codes: “=” for an exact match of all characters and “= + %” for a match of characters entered. For example, “=QA” 
will pick up hold QA only, while “=QA%” will pick up holds QA and QA7.
If required, you can enter multiple hold codes in the Hold Code field. For example, if you enter “=QA,=24HR, =DMG”, any product shipped or received with any of these holds would be charged. 
SEQUENCE BLOCK

Load Type Code Only available when charge per = DOCH (Document Header).
If you specify a load type code in this field, the extra charge will apply only to receipts or orders that have been assigned to that load type code. For example, if you attach a load type code to a profile, an extra charge will be generated only when the order or receipt has been assigned that load type.
Pallet Code See [Charging by Physical Pallet](faturamento-invoicing.html#charging-by-physical-pallet) for further information.
Location Type Code If you enter a location type restriction in this field, the extra charge will apply only to receipt or order lines whose final put-away location (for inbounds) or final pick or staging location (for outbounds) has been assigned that location type.
Bill to CARR = Carrier
CONS = Consignee
CUST = Customer
SHIP = Shipper
The party that will be billed for the charge. If you wish to bill the carrier, consignee or shipper for a charge, that carrier, consignee or shipper must be set up as an “invoice only” customer in CUST.
If you wish to bill to an account other than the carrier, consignee, customer or shipper, see [Third Party Billing in ECHP](faturamento-invoicing.html#third-party-billing-in-echp) for further information.
SEQUENCE BLOCK

Quantity Based on OTOO = One to One 
OTOZ = One to One - include 0 qty line
PRIS = Top SKU Rounded Down*
RM2A = Entered Qty (2nd SKU) - Ignore Last Qty*
RM2R = Actual Qty Moved (2nd SKU) - Ignore Last Qty*
RM3A = Entered Qty (3rd SKU) - Ignore Last Qty*
RM3R = Actual Qty Moved (3rd SKU) - Ignore Last Qty*
RM4A = Entered Qty (4th SKU) - Ignore Last Qty*
RM4R = Actual Qty Moved (4th SKU) - Ignore Last Qty*
RM5A = Entered Qty (5th SKU) - Ignore Last Qty*
RM5R = Actual Qty Moved (5th SKU) - Ignore Last Qty*
RM2A = Entered Qty (2nd SKU)*
RM2R = Actual Qty Moved (2nd SKU)*
RM3A = Entered Qty (3rd SKU)*
RM3R = Actual Qty Moved (3rd SKU)*
RM4A = Entered Qty (4th SKU)*
RM4R = Actual Qty Moved (4th SKU)*
RM5A = Entered Qty (5th SKU)*
RM5R = Actual Qty Moved (5th SKU)*
RQ2A = Entered Qty (2nd SKU - Use Last Recd Qty Bkd)*
RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty Bkd)*
*DOCL, ULV1, ULV2, ULV3 and ULV4 only
This field allows you to specify the way in which you wish to charge for partial quantities. If there are no partial quantities (for example, a bill of lading charge that applies to an entire order), use One to One. 
One to One is the most common option and can be used for both unit-based 
SKU’s and weight-based SKU’s. If any partial quantities are involved, the system will round up, round down or perform no rounding depending on the option that you specify in the Rounding Flag field in CHAR (Charge Code). 
See [Charging for Partial Quantities of Unit-Based SKU’s](faturamento-invoicing.html#charging-for-partial-quantities-of-unit-based-sku-s) for further information on the entered quantity and actual quantity moved options.
Process Code (IPRO) If you specify a process code in this field, the extra charge will apply only to receipt and order lines containing items that have been assigned to that process code.
SEQUENCE BLOCK

Type of Value If you specify a item process code type of value in this field (for example, 
CUBE, HGT, LEN, LEV2, SER, TEMP), the extra charge will apply only to receipt and order lines containing items that have been assigned to that process code with that type of value.
NOTE This restriction can be used in conjunction with a process code restriction or can be used in stand-alone mode; that is, if you specify CUBE, any process code whose type of value has been set to CUBE will generate an extra charge.
Exclude System-Populated Process ValuesN = No
Y = Yes
If set to Y for Yes, no catch weight charges will be generated for system-populated process values. If set to N for No, catch weight charges will be generated normally for system-populated process values.
A system-calculated process value is a process value created through either an EDI receipt creation process or an auto-transfer from inbound to outbound.
Some of the possible scenarios that you might need to deal with are as follows:
 If the customer transfers the process values on a receipt line via EDI, the catch weight charges should be excluded. However, if the expected quantities are incorrect forcing the operator to delete the EDI values and rescan, the catch weight charges should be included.
 If order allocation selects a full pallet that has not been touched and the weights are automatically transferred, the catch weight charges should be excluded.
 If a customer service representative is forced to manually enter weights in 
ENRE/ENOR, the catch weight charges should be included.
EDI Version Code These EDI fields allow you to set up an extra charge based on the number of occurrences of any EDI Data ID Code value. For example, suppose you set up an extra charge attached to the Customer EDI Line Number Data ID Code belonging to the 940 transaction set. AccellosOne 3PL will add up the number of occurrences of unique Customer EDI Line Number fields for the order or receipt and calculate an extra charges.
EDI Transaction Set 
Code (EDTS)
Only available if you enter an EDI version code.
Your EDI Transaction Set Code.
SEQUENCE BLOCK

### PROCEDURE <a id="procedure"></a>

1 Enter ECHP.
EDI Data ID Code (EDDI) Only available if you enter an EDI version code.
Your EDI Data ID Code.
Label Count N = No
Y = Yes
If you select Y for Yes, you can charge by label count. For example, you cartonize your outbound shipments and a single carton can contain multiple items. Rather than charge by the item, you wish to generate a single charge per carton.
Label count charges are only available for cartonized product. Product is considered cartonized when:
 you perform manual cartonization in RFSC
 you perform system-directed or first level cartonization in RFPK (also known as "Pick & Pack")
 you perform second level cartonization for product that cannot be cartonized in RFPK
 you perform manual packing in EPSD
SEQUENCE BLOCK

Extra Charge Profile (ECHP)
2 Click on Create Record.
3 Key in your extra charge profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 Key in your type (I for Inbound or O for Outbound) and press Enter.
6 Key in your sequence number for the charge and press Enter.
7 Key in your charge code for the extra charge profile and press Enter.
8 Use your pick list to select the appropriate charge per. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on 
Select to select it.
9 In the Action Type field, key in the appropriate option (O for Optional or A for Automatic) and press Enter.
10 In the Entry Type field, key in the appropriate option (E for Entry, C for Confirmation, B for Both or N for 
None) and press Enter.
11 In the Override Quantity Rules field, key in the appropriate option (E for Entry, C for Confirmation, B for 
Both or N for None) and press Enter.
12 In the Charge Date Based on field, key in B for Batch Creation Date or C for Document Confirmation 
Date.
13 In the Invoice Type field, key in A for Accessorial or E for Extra Billing and press Enter.
14 Press Enter the required number of times to position your cursor in the Customer Code field.
15 If required, key in a customer code in the Customer Code field and press Enter. If the charge is not specific to a particular customer, press Enter to bypass this field.
16 Repeat the above step for the Consignee Code, Shipper Code and Carrier Code fields.
17 If required, key in a hold code in the Hold Code field and press Enter. If a hold code is not required, press 
Enter to bypass this field.

18 In the Bill To field, use your pick list to select the appropriate value. A general extra charge can be billed to a customer, carrier, consignee or shipper.
19 In the Quantity Based on field, use your pick list to select the appropriate value.
20 Do one of the following:
21 Click on Return to Main to exit create record mode.

Extra Charge Profile screen showing extra charge for each receipt line with an action type of Optional 
22 Click on Master Block. Then click on Exit to exit.
23 Attach your extra charge profile to the appropriate item, customer, shipper, consignee or carrier.
If you wish to set up an extra charge based on an EDI Data ID 
Code value:
If you do NOT wish to set up an extra charge based on an EDI 
Data ID Code value:
a) Key in your EDI version code and press Enter.
b) Key in your EDI transaction set code and press Enter.
c) Key in your EDI Data ID Code and press Enter.
a) Press Enter to bypass the EDI 
Version Code field.
CAUTION Make sure that the charge per for the extra charge is compatible with the entity to which it is attached. For example, document total extra charges can only be attached to customers; they cannot be attached to items.

24 If you create your receipts or orders through EDI, refer to [Activating Extra Charges for EDI](faturamento-invoicing.html#activating-extra-charges-for-edi) for further setup instructions.

### Charging by Physical Pallet <a id="charging-by-physical-pallet"></a>

You can generate an inbound/outbound extra charge based on the number of physical pallets entered in the 
Pallet Block of ENRE/ENOR. When you confirm the receipt or order, AccellosOne 3PL will calculate an accessorial charge based on the pallet type and the number of shipped pallets. The charge quantity is calculated as follows:
EXAMPLE 1 (OUTBOUND)
ship quantity = 3 receive quantity = 2 charge quantity = 1
EXAMPLE 2 (OUTBOUND)
exchange quantity = 2 charge quantity = 0
EXAMPLE 3 (INBOUND)
ship quantity = 3 receive quantity = 1 charge quantity = 2
You set up your physical pallet charge in ECHP as follows:
 Charge Code = charge code set up in CHAR/RATE for physical pallet charges
 Charge per = DOCUMENT HEADER
 Pallet Code = pallet code in PALL (Pallet Types) using the standard AccellosOne 3PL operands such as "=", "(=)", "<", ">", etc.
After setting up your extra charge profile for physical pallet charges, you attach the profile to the appropriate customers and/or items.

ECHP screen showing outbound pallet charge for CHEP and CPC pallets

### Third Party Billing in ECHP <a id="third-party-billing-in-echp"></a>

You can bill a third party customer in ECHP by selecting the OVRR (Customer Override) option in the Bill to field. A third party customer is a customer other than the standard three accounts on any receipt /order; that is, a customer who is not a customer (inventory owner), carrier or shipper/consignee. The third party customer must be set up in CUST in order to be charged and can be either a regular or invoice only type customer.

ECHP screen showing third party billing for customer A

### Activating Extra Charges for EDI <a id="activating-extra-charges-for-edi"></a>

In order to activate extra charges, you must attache the appropriate special verify program to your workflow profile defined in DIFP. For receipt extra charges, the EDEC (EDI Receipt Extra Charge) special verify must be attached to the appropriate inbound flow. For order extra charges, the OREC (EDI order Extra Charge) 
special verify must be attached to the appropriate outbound flow.
EDEC and OREC can be attached to any flow following the printing of the last document and receipt/order confirmation.
1 Enter DIFP.
2 Retrieve the workflow profile that you wish to modify.
3 Click on In/Out Block.
4 Use your arrow keys to select the appropriate option: Inbound or Outbound.
5 Click on Flow Block to enter the Flow Block.
6 User your arrow keys to select the appropriate inbound or outbound flow.
7 Click on Document Block and Special Verify Block to enter the Special Verification Block.
8 Click on Create Record.
9 Key in your sequence number for the special verify and press Enter.
10 Key in the appropriate special verify (OREC or EDEC) and press Enter.

11 Press Enter three times to bypass the remaining fields.

Depositor Workflow Profile screen showing special verify OREC attached to the flow FIPI (Finish Picking)
12 Click on Return to Main and Document Block. Then click on Flow Block, In/Out Block, Master Block and 
Exit to exit DIFP.

### Confirming an Extra Charge <a id="confirming-an-extra-charge"></a>

If you set the Entry Type field in ECHP to E for Entry, C for Confirmation or B for Both, you will be prompted to confirm the extra charge at either the header or line level in ENRE or ENOR. During confirmation, you can override the quantity on which the charge is based if you set the Override Quantity Rules field in ECHP to E for Entry, C for Confirmation or B for Both.
1 Enter ENRE or ENOR and enter your receipt or order. When you finish entering the header or line information to which the extra charge is attached, the Extra Charge Block will be displayed.

ENOR showing Extra Charge Block
2 You have up to four options on this screen:
3 Continue entering your receipt or order in the normal manner.
To cancel an extra charge: Click on Cancel Charge
To restore an extra charge that you have cancelled:Click on Apply Charge
To override the quantity on which the extra charge is based: 
Press Enter to position your cursor in the 
Override Quantity field. Then key in your override quantity and press Enter. The override quantity is based on the charge on SKU code in CHAR (Charge Code).
NOTE If you enter a quantity in one or more lines and wish to undo the quantity in all lines, click on Clear All Lines. Then click on 
Yes when prompted to proceed with the update.
To accept the extra charge as is with no change:
Click on Exit to exit the Extra Charge Block.

## Invoicing <a id="invoicing"></a>

*Manual A — Billing and Invoicing*

### IND Invoicing <a id="ind-invoicing"></a>

IND invoicing generates three invoices:
 a warehouse receipt invoice containing receipt and extra charges
 an accessorial invoice containing receipt/order accessorial charges and other accessorial charges
 a renewal invoice containing renewal storage charges
Because IND invoicing generates three separate invoices, each invoice can be generated independently of the others. For example, you will generate your warehouse receipt invoice whenever you receive product, you can generate accessorial invoices each time that you run BILB (accessorial) and you can generate renewal invoices each time that you run BILB (renewal).
ENRE
CHRF
ENOR
CHOF BILB (renewal)
ENAC
BILB (accessorial)
Accessorial 
Invoice receipt/order receipt/order accessorial and extra charges receipt charges such as initial storage and handling handling charges (outbound)
Renewal Invoice print invoice
PRRE/PRRM
Warehouse 
Receipt Invoice receipt and extra charges
BILB (extra charge)
charges created in GEXC and ECHP

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the batch is correct, confirm it. 
4 Generate your accessorial batch in BILB. It will gather the receipt accessorial charges and extra charges that have already been generated and place them in an accessorial batch.
5 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes. 
6 Confirm the batch and print the accessorial invoice.
7 Generate your renewal batch in BILB.
8 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then delete the batch in BILB and create a new batch.
9 Confirm the batch and print the renewal invoice.

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Warehouse Receipt Invoice](faturamento-invoicing.html#generating-and-printing-the-warehouse-receipt-invoice) for complete instructions on the warehouse receipt.
2 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
3 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.
4 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal invoice.

### IND Invoicing With Extra Charges on a Warehouse Receipt <a id="ind-invoicing-with-extra-charges-on-a-warehouse-receipt"></a>

If you select a Invoice Type of E for Extra Billing in ECHP, the system will automatically generate the receipt extra charges when you confirm the receipt in CHRF (automatic rating) or when you rate the receipt in RCRA (manual rating). Therefore, there is no need to generate an extra charge batch in BILB for the receipt extra charges because the charges are automatically generated. If you look up the extra charge in ENAC, the receipt number for the extra charge preceded by a minus sign will appear in the Reference Description field.

ENAC (Bill Later - Enter Charges) screen

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your accessorial batch in BILB.
4 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes. 
5 Confirm the batch and print the accessorial invoice.
6 Generate your renewal batch in BILB.
7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then delete the batch in BILB and create a new batch.
If your only extra charges are receipt extra charges that appear on a warehouse receipt:
If you have other extra charges as well:
a) Proceed to next step. a) Generate your extra charge batch in BILB. 
b) Print the audit report for your extra charge batch in BILB. If the batch is correct, confirm it. Once confirmed, you can no longer print the batch.
Negative number indicates a receipt extra charge

8 Confirm the batch and print the renewal invoice.

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Warehouse Receipt Invoice](faturamento-invoicing.html#generating-and-printing-the-warehouse-receipt-invoice) for complete instructions on the warehouse receipt.
2 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
3 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.
4 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal invoice.

### UALL Invoicing <a id="uall-invoicing"></a>

UALL invoicing generates a single invoice for all charges. You normally perform UALL invoicing when you are ready to run your renewals. 

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Generate your renewal batch in BILB.
3 Print the audit report.
4 Confirm and print to VIEW the renewal batch.
5 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the batch is correct, confirm it.
6 Generate your accessorial batch in BILB. It will gather the receipt, renewal and extra charges that have already been generated and place them in an accessorial batch.
7 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes.
ENRE
CHRF
ENOR
CHOF BILB (renewal)
ENAC
BILB (accessorial)
Accessorial Invoice containing all charges all charges receipt/order accessorial and extra charges receipt charges such as initial storage and handling handling charges (outbound)
BILB (extra charge)
charges created in GEXC and ECHP

8 Confirm the batch and print the accessorial invoice.

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal invoice.
2 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
3 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.

### UREC Invoicing <a id="urec-invoicing"></a>

UREC invoicing generates two invoices:
 an accessorial invoice containing receipt, accessorial and extra charges
 a renewal invoice containing renewal storage charges 

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the batch is correct, confirm it.
3 Generate your accessorial batch in BILB. The accessorial batch for UREC invoicing will contain accessorial and receipt charges but no renewal charges.
4 Print the audit report.
5 Confirm the batch and print the accessorial invoice.
6 Generate your renewal batch in BILB. The renewal batch will contain renewal charges only.
ENRE
CHRF
ENOR
CHOF BILB (renewal)
ENAC
BILB (accessorial)
Accessorial Invoice containing receipt charges receipt, receipt/ order accessorial and extra charges receipt/order accessorial and extra charges receipt charges such as initial storage and handling handling charges (outbound)
Renewal Invoice print invoice
BILB (extra charge)
charges created in GEXC and ECHP

7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then reprint the batch.
8 Confirm the batch and print the renewal invoice.

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
2 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.
3 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal invoice.

### UREN Invoicing <a id="uren-invoicing"></a>

UREN invoicing generates two invoices:
 a warehouse receipt invoice containing receipt and extra charges
 an accessorial invoice containing receipt/order accessorial charges and renewal storage charges

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your renewal batch in BILB.
4 Print the audit report.
5 Confirm and print to VIEW the renewal batch.
6 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the batch is correct, confirm it.
7 Generate your accessorial batch in BILB. The accessorial batch for UREN invoicing will contain accessorial and renewal charges but no receipt charges.
8 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. 
9 Confirm the accessorial batch and print the accessorial invoice.
ENRE
CHRF
ENOR
CHOF BILB (renewal)
receipt charges such as initial storage and handling handling charges (outbound)
generate renewal charges
ENAC
BILB (accessorial)
Accessorial Invoice containing renewal charges renewal and receipt/order receipt/order accessorial and extra charges
PRRE/PRRM
Warehouse 
Receipt Invoice receipt and extra charges
BILB (extra charge)
charges created in GEXC and ECHP

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Warehouse Receipt Invoice](faturamento-invoicing.html#generating-and-printing-the-warehouse-receipt-invoice) for complete instructions on the warehouse receipt.
2 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal batch.
3 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
4 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.

### UREN Invoicing With Extra Charges on a Warehouse Receipt <a id="uren-invoicing-with-extra-charges-on-a-warehouse-receipt"></a>

If you select a Invoice Type of E for Extra Billing in ECHP, the system will automatically generate the receipt extra charges when you confirm the receipt in CHRF (automatic rating) or when you rate the receipt in RCRA (manual rating). Therefore, there is no need to generate an extra charge batch in BILB for the receipt extra charges because the charges are automatically generated. If you look up the extra charge in ENAC, the receipt number for the extra charge preceded by a minus sign will appear in the Reference Description field.
Negative number indicates a receipt extra charge

### QUICK STEPS <a id="quick-steps"></a>

1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your renewal batch in BILB.
4 Print the audit report.
5 Confirm and print to VIEW the renewal batch.
6 Generate your accessorial batch in BILB. The accessorial batch for UREN invoicing will contain accessorial and renewal charges but no receipt charges.
7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. 
8 Confirm the accessorial batch and print the accessorial invoice.

### DETAILED STEPS <a id="detailed-steps"></a>

1 Refer to [Generating and Printing the Warehouse Receipt Invoice](faturamento-invoicing.html#generating-and-printing-the-warehouse-receipt-invoice) for complete instructions on the warehouse receipt.
2 Refer to [Generating and Printing the Renewal Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-renewal-batch-invoice) for complete instructions on the renewal batch.
3 Refer to [Generating and Printing the Extra Charge Batch](faturamento-invoicing.html#generating-and-printing-the-extra-charge-batch) for complete instructions on generating an extra charge batch.
4 Refer to [Generating and Printing the Accessorial Batch/Invoice](faturamento-invoicing.html#generating-and-printing-the-accessorial-batch-invoice) for complete instructions on the accessorial invoice.

### Generating and Printing the Warehouse Receipt Invoice <a id="generating-and-printing-the-warehouse-receipt-invoice"></a>

You can print a warehouse receipt invoice from two programs: PRRM (Print Documents for Specific Receipts) 
or PRRE (Print Receiving Documents - All). You use PRRM if you know the receipt numbers of the receipts that you wish to invoice. You use PRRE if you wish to invoice multiple receipts that you will select based on certain criteria; for example, all receipts received on a certain date, all receipts from a specific customer, etc. 
If your only extra charges are receipt extra charges that appear on a warehouse receipt:
If you have other extra charges as well:
a) Proceed to next step. a) Generate your extra charge batch in BILB. 
b) Print the audit report for your extra charge batch in BILB. If the batch is correct, confirm it. Once confirmed, you can no longer print the batch.

In this procedure, you will print the warehouse receipt invoice from PRRM. If you wish to print it from PRRE, refer to your Operations 1 Guide for complete instructions.
1 Enter your receipt in ENRE.
2 Add any accessorial or extra charges to the receipt if required.
3 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
When you confirm a receipt, all receipt charges are loaded into ENAC. In this program, you can modify or delete any charge as required.
4 Enter PRRM.

Print Documents for Specific Receipts (PRRM)
5 Position your cursor beside the document that you wish to print.
6 Click on Receipt Block.
7 Press Enter once to position your cursor in the Receipt Number field.
8 Key in your receipt number and press Enter.

Print Documents for Specific Receipts (PRRM) screen showing receipt 1149
9 If you have additional documents to print, key in their receipt numbers and press Enter.
10 Click on Execute Query.
11 Click on Print Block.

12 Key in your printer code and press Enter or select it using the pick list. To select a code using the pick list, press F10 and then click on Execute Query to display your pick list of available printers. Use your arrow keys to position the cursor beside the print that you wish to select and then click on Select Code to select it. If you use UALL or UREC invoicing, print to VIEW the warehouse receipt.
13 Click Ok. 

### Generating and Printing the Accessorial Batch/Invoice <a id="generating-and-printing-the-accessorial-batch-invoice"></a>

You can generate an accessorial batch at any time and as often as required — for example, daily, weekly, monthly, twice a day, whenever you receive or ship, etc. Each time you generate a batch, all accessorial charges that have accumulated in ENAC since the confirming and printing of your last invoice will be placed in a batch and assigned a batch number by the system. 
If you are performing UALL invoicing, the accessorial invoice may contain receipt and renewal charges as well. If you are performing UREC invoicing, the accessorial invoice may contain receipt charges but no renewal charges; if you are performing UREN invoicing, the accessorial invoice may contain renewal charges but no receipt charges. 
The following conditions must be met before you can place a charge on an accessorial batch:
 if the accessorial charge is attached to a particular receipt, the receipt must be confirmed and rated
 if the accessorial charge is attached to a particular order, the order must be confirmed
 If accessorial authorization is activated in your system, the accessorial charge must be authorized in 
OAUD (Accessorial Charges Authorization Audit) and ACAU (Accessorial Authorization)

### GENERATING THE ACCESSORIAL BATCH IN BILB <a id="generating-the-accessorial-batch-in-bilb"></a>

1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing accessorial batches

4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all accessorial charges that were entered up to and including the cut-off date will be included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing accessorial batch restrictions
8 Proceed to specify restrictions on the charges you wish to place on your accessorial invoice. For example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 

EXAMPLES
9 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
10 In the Bill Profile Code field, key in your billing profile code restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter billing profile code restrictions in this field, only charges for items that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include all charges regardless of billing profile code.
Billing profile codes are set up in DBIP (Depositor Billing Profile) and assigned to the customer.
11 In the Accessorial Date field, key in your date restrictions and press Enter or press Enter with this field blank for no restrictions. You must enter your date restrictions in YYYY.MM.DD format.
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 (for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 (for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 (=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If you exceed this limit, AccellosOne 3PL will display an error message. Remove one or two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or “<“ and “>” in the same field.

If you enter a date in this field, only those accessorial charges with a Date to Charge date that meets the date restriction that you specify will be generated. If you leave this field blank, all accessorial charges regardless of their Date to Charge value will be generated.
12 In the Invoice Type field, key in your invoice type restrictions and press Enter or press Enter with this field blank for no restrictions.
If you enter invoice type restrictions in this field, only charges that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include all charge codes. In order to use this restriction, you must have invoice types set up in INTP (Invoice Types).
13 In the Charge Code field, key in your charge code restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter charge code restrictions in this field, only charges that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include all charge codes.

Billing Batch (BILB) screen showing a batch being generated for BF (Blast Freezing) charges
14 In the Source Flag field, key in your source flag restrictions and press Enter or press Enter with this field blank for no restrictions. 
The Source Flag field allows you to specify the source or sources of the charges that you wish to include in the invoice. If you leave this field blank, your invoice will include all charges regardless of their source. 
BILB supports the following types of charges:
R Receipt charges entered in ENRE or generated automatically in IISP (Initial Storage Profile)
O Order charges entered in ENOR 
NOTE Any restrictions that you enter in this field will operate within the cut-off date that you defined in the Create Date field in the Main Block of BILB. For example, you can specify Jan 1/05 as your cut-off date — that is, no charges later than that date — and you can specify > Dec 1/04 as your Accessorial Date restriction. This would result in a batch of all charges created between Dec 1/04 and Jan 1/05.

E Extra charges generated automatically in GEXC (General Extra Charges) or ECHP (Extra Charge 
Profile)
X Renewal charges created when a renewal batch is generated
A Maximum/minimum charges charged when the actual charge is less than the minimum charge or greater than the maximum charge
S Accessorial charges entered through ENAC
F Freight charges created in A1 Transport
15 If invoicing by inventory level is activated in CUST, you can key in any inventory level restrictions in the 
Billing Level 1/2/3 fields and press Enter. For example, if you bill by level (lot number) and you wish to generate a batch for lot 123 that you received last week, key in =123 in the Billing Level 2 field.
16 Click on Generate Batch. 

### PRINTING THE ACCESSORIAL AUDIT <a id="printing-the-accessorial-audit"></a>

The accessorial audit shows each charge that will appear on the invoice. The purpose of this report is to allow you to verify all charges before confirming and printing the final invoice.
Refer to [Working With Audit Batch Restrictions](faturamento-invoicing.html#working-with-audit-batch-restrictions) for further information on audit reports.
1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 116 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch (BILB) screen showing print audit restrictions for accessorial audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your print audit restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will be displayed.

### CONFIRMING THE BATCH AND PRINTING THE ACCESSORIAL INVOICE <a id="confirming-the-batch-and-printing-the-accessorial-invoice"></a>

If all the charges on the accessorial audit report are correct, you are ready to confirm the batch and print the invoice. If you wish to make changes to the batch before confirming it, see the section [Deleting and 
Modifying Charges on a Confirmed Batch](faturamento-invoicing.html#deleting-and-modifying-charges-on-a-confirmed-batch). 
1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
NOTE If you specify a minimum dollar value in the Threshold Ancillary Charge 
Code field in DBIP (Depositor Billing Profile), no accessorial invoice will be printed if the minimum value for a particular customer has not been reached.

Billing Batch (BILB) screen showing batch 116 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.

### Generating and Printing the Renewal Batch/Invoice <a id="generating-and-printing-the-renewal-batch-invoice"></a>

Each time that you generate a renewal batch, all renewal charges that have accumulated in ENAC since the confirming and printing of your last invoice will be placed in a batch and assigned a batch number by the system.
There are four steps to follow in generating and printing a renewal invoice:
 generate the batch
 print the audit report
 confirm the batch
 print or print to VIEW the invoice 

### BEFORE YOU BEGIN <a id="before-you-begin"></a>

 Make sure that there are no open or incomplete renewal batches in BILB for the customer that you are going to invoice. If there are, delete or confirm the old batch before you generate a new batch.
 It is recommended that you run RENW (Renewal Preprocessor) at least once before generating your renewal batch. 
TIP For best results, it is recommended that you confirm any orders and receipts that have been received or shipped before the cut-off date, but are still open. For example, if your cut-off date is the third Friday of each month, make sure that any orders shipped or receipts received during the billing period have been confirmed. 
Then run a suitable inventory report. A suitable inventory report is any report showing all inventory levels used in billing, the product’s weight (if you bill by weight) or the product’s SKU (if you bill by pallet, case, etc.). By following these two steps, it is easy to resolve any renewal billing discrepancies.

### GENERATING A RENEWAL BATCH IN BILB <a id="generating-a-renewal-batch-in-bilb"></a>

1 Enter BILB.
2 Select Renewal Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing renewal batches
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all inventory with a next renewal date that falls on or before this date will be included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing renewal batch restrictions
8 Proceed to specify restrictions on the charges that you wish to place on your renewal invoice. For example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 (for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 (for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 (=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)

9 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
10 In the Bill Profile Code field, key in your billing profile code restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter billing profile code restrictions in this field, only charges for items that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include all charges regardless of billing profile code.
Billing profile codes are set up in DBIP (Depositor Billing Profile) and attached to the customer.

Billing Batch (BILB) showing batch being generated for customer ABC
11 Click on Generate Batch. 

### PRINTING THE RENEWAL AUDIT <a id="printing-the-renewal-audit"></a>

The renewal audit shows each charge that will appear on the invoice. The purpose of this report is to allow you to verify all charges before confirming and printing the final invoice.
Refer to [Working With Audit Batch Restrictions](faturamento-invoicing.html#working-with-audit-batch-restrictions) for further information on audit reports.
1 Enter BILB.
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If you exceed this limit, AccellosOne 3PL will display an error message. Remove one or two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or “<“ and “>” in the same field.

2 Click on Enter Criteria.
3 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing renewal batch 79 with a status of Generated
4 Select Print Audit from the Action dropdown list.

Billing Batch (BILB) screen showing print audit restrictions for renewal audit
5 Select the appropriate option in the Summary or Detail field.
6 Key in a description for your audit report.
7 Proceed to enter your print audit restrictions, if any.
8 When you finish entering your print audit restrictions, click on Print.
9 Key in your printer code and press Enter or select it using the pick list.
10 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will be displayed.

### CONFIRMING THE BATCH AND PRINTING THE RENEWAL INVOICE <a id="confirming-the-batch-and-printing-the-renewal-invoice"></a>

If all the charges on the renewal audit report are correct, you are ready to confirm the batch and print the invoice. If you wish to make changes to the batch before confirming it, see the section [Deleting and 
Modifying Charges on a Confirmed Batch](faturamento-invoicing.html#deleting-and-modifying-charges-on-a-confirmed-batch).
1 Enter BILB.
2 Select Renewal Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing renewal batch 79 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.

### Generating and Printing the Extra Charge Batch <a id="generating-and-printing-the-extra-charge-batch"></a>

The extra charges discussed in this chapter are outbound extra charges set up in GEXC (General Extra 
Charges) and ECHP (Extra Charge Profile). If you have inbound extra charges set up in ECHP with an invoice type of E for Extra Billing or you have added inbound extra charges to a receipt in ENRE, CHRF or 
RCRA, you do not use the procedures in this chapter.

Extra charges print on the accessorial invoice. You must generate and confirm your extra charge batch in 
BILB before you generate and print the accessorial batch/invoice in BILB. As well, the order must be confirmed before any charges attached to it can be placed on a batch.

### GENERATING AN EXTRA CHARGE BATCH IN BILB <a id="generating-an-extra-charge-batch-in-bilb"></a>

1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch screen showing extra charge batches
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all extra charges that have been incurred up to and including the cut-off date will be included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting date for the charge.
NOTE You can automate the generation, printing and confirmation of extra charge batches by running RECH/ORCH as either a stand-alone program or a special verification program. This approach is recommended when all extra charges are automatically invoiced. However, if you use special extra charge logic based on all extra charges during a billing period — for example, the tenth and higher bill of lading per billing period is free — you cannot run RECH/ORCH. Instead, you must generate an extra charge batch in BILB and then manually adjust the charges to be invoiced.

If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing restrictions for extra charge batch
8 Proceed to enter your restrictions, if any, for the batch. If there are no restrictions for a particular field, press Enter with the field blank to bypass the restriction. For example, if you leave the Customer Code field blank, your batch will include charges for all customers.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
NOTE BILB supports the following extra charge restrictions: customer code, consignee code and carrier code. Restrictions apply to the selection of orders to be processed, not to the account that will be billed for the charges. For example, if you restrict your extra charge batch to customer ABC, any charges associated with customer ABC’s orders will be generated even if they are billed to the carrier or consignee.
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 (for example, CUST1, CUST111, CUST199, CUST1ABC)

9 When you finish entering your restrictions, click on Generate Batch. 

### PRINTING THE EXTRA CHARGE AUDIT <a id="printing-the-extra-charge-audit"></a>

The extra charge audit shows each extra charge that will appear on the invoice. The purpose of this report is to allow you to verify all charges before confirming and printing the final invoice. 
Refer to [Working With Audit Batch Restrictions](faturamento-invoicing.html#working-with-audit-batch-restrictions) for further information on audit reports.
1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 (for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 (=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If you exceed this limit, AccellosOne 3PL will display an error message. Remove one or two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or “<“ and “>” in the same field.

Billing Batch (BILB) screen showing batch 70 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch screen showing print audit restrictions for extra charge audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your print audit restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
When the batch finishes running, your report is printed.
CONFIRMING THE BATCH AND PRINTING TO VIEW THE EXTRA CHARGE 
INVOICE
If all the charges on the Extra Charge Audit report are correct, you are ready to confirm the batch and print the invoice. If you wish to make changes to the batch before confirming it, see the section [Deleting and 
Modifying Charges on a Confirmed Batch](faturamento-invoicing.html#deleting-and-modifying-charges-on-a-confirmed-batch).
1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.

3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 70 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in VIEW as your printer code and press Enter.
7 Click Ok. When the batch finishes running, you are ready to generate your accessorial batch.

### TROUBLESHOOTING EXTRA CHARGES <a id="troubleshooting-extra-charges"></a>

If you encounter an error message during batch generation, the status of the batch will read “Generated” even though the complete batch was not successfully generated. You can print a partial audit report to check that portion of the batch that was successfully generated, but you cannot confirm the batch until the entire batch is regenerated successfully.

### Working With Audit Batch Restrictions <a id="working-with-audit-batch-restrictions"></a>

Audit batch restrictions apply to the accessorial, renewal, extra charge and immediate batches. They allow you to summarize the audit report by customer code, inventory level and charge code and make it possible to limit the report to a specific customer, inventory level and charge code.
Audit batches together with invoices are stored in the del4/archive directory in Unix. They should be deleted when no longer needed in order to save disk space.
Audit batches are stored in the format CC_TTTT_NNNNNN_NNN where CC = company code, TTTT = batch type, NNNNNN = batch number and NNN = audit number. For example, W1_RENW_456_12.
NOTE Audit batch restrictions are for reporting purposes only. Unlike the restrictions that you specify when generating a batch, audit batch restrictions do not affect the charges on a batch. For example, if you specify customer ABC as your print audit restriction, the audit report will show only charges for that customer. However, when you confirm the audit in BILB, the confirmed invoice will contain charges for all customers on the batch.

Invoices are stored in the format CC_PP_NNNNNN where CC = company code, PP = invoice prefix and 
NNNNNN = batch number. For example, W1_RC_100000827.
FIELD DESCRIPTIONS
Summary or Detail Details
The audit report will show one line for each charge on the batch.
Customer
The audit report will show one line for each customer on the batch.
Customer, Level 1
The audit report will show one line for each customer/level 1 value on the batch.
Customer, Level 1/2
The audit report will show one line for each customer/level 2 value on the batch.
Customer, Level 1/2/3
The audit report will show one line for each customer/level 3 value on the batch.
Customer, Charge Code
The audit report will show one line for each customer/charge code on the batch.
Audit Description This description serves to identify the audit when you use the Reprint Archive command.
Customer Code If you enter a customer restriction in this field, the audit report will be restricted to charges for that customer. If you do not enter a customer restriction in this field, the audit report will contain all charges on the batch regardless of customer.
Level 1 Only available if you specify a customer code restriction
If you enter a level 1 restriction in this field, the audit report will be restricted to charges for the level 1 value that you enter. If you leave this field blank, the audit report will contain all charges regardless of level 1 value.

### REPRINTING AN AUDIT BATCH <a id="reprinting-an-audit-batch"></a>

1 Enter BILB.
2 Retrieve the audit batch that you wish to reprint.
3 Click on Print Archive.
Level 2 If you have a customer code restriction, this field will only be available if the customer has two or more inventory levels.
If you enter a level 2 restriction in this field, the audit report will be restricted to charges for that level 2 value. If you leave this field blank, the audit report will contain all charges regardless of level 2 value.
Level 3 If you have a customer code restriction, this field will only be available if the customer has two or more inventory levels.
If you enter a level 3 restriction in this field, the audit report will be restricted to charges for that level 3 value. If you leave this field blank, the audit report will contain all charges regardless of level 3 value.
Charge Code If you enter a charge code in this field, the audit report will be restricted to charges for that charge code. If you leave this field blank, the audit report will contain all charges regardless of charge code.
FIELD DESCRIPTIONS

Batch audits window in BILB screen showing two batch audits for batch 82
Audit batches are listed in batch number order. If you wish to resort your query results in audit file description or audit number sequence, click on the appropriate button.
4 Double click on the audit batch that you wish to print.
5 When the Select Printer window displays, select your printer from the dropdown list and click Ok.

### Running the Daily Invoice Register <a id="running-the-daily-invoice-register"></a>

The daily invoice register picks up all confirmed invoice revenue that has been generated since the last time that the register was run and posts it to the appropriate management and sales reports. If AccellosOne 3PL is linked to your accounting system, the daily invoice register will also create your general ledger interface file. 
When the register is run, all confirmed charges in ENAC and ENIN are removed and no longer available in these programs. If you wish to look up a charge that was removed from ENAC, you use the program LOAC (Look Up Accessorial).
The daily invoice register prints a report showing the following in three separate sections:
 a list of all invoices
 a breakdown of revenue by revenue analysis code — you define your breakdown in the program INRE (Invoice Register)
 a breakdown of revenue by general ledger account

If you do not assign a revenue analysis code to a column in INRE (Invoice Register), any revenue from that revenue analysis code will be assigned to the Miscellaneous column in the daily invoice register.
1 Enter BILB.
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing daily invoice registers
4 In the Description field, key in a description for your batch and press Enter.
5 Press Enter to bypass the Attention field.
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all invoices that have been confirmed on or before the cut-off date will be included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.
8 Click on Generate Batch. 

### PRINTING THE DAILY INVOICE REGISTER AUDIT <a id="printing-the-daily-invoice-register-audit"></a>

The daily invoice register audit report shows the invoice number and total charges for each invoice on the daily invoice register. The purpose of this report is to allow you to verify all invoices before confirming and printing the final daily invoice register.
Refer to [Working With Audit Batch Restrictions](faturamento-invoicing.html#working-with-audit-batch-restrictions) for further information on audit reports.
CAUTION If you are unable to confirm the batch because of an error condition, that batch will have a status “Begun Generation” or “Begun Confirmation”. You must correct the error and then regenerate the batch. DO NOT ATTEMPT TO GENERATE 
A NEW BATCH IF THE CURRENT BATCH IS NOT CONFIRMED AND DO NOT 
ATTEMPT TO DELETE AN UNCONFIRMED BATCH.

1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Daily Invoice Register (BILB) screen showing batch 16 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch (BILB) screen showing restrictions for daily invoice register
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will be displayed.

### CONFIRMING THE BATCH AND PRINTING THE DAILY INVOICE REGISTER <a id="confirming-the-batch-and-printing-the-daily-invoice-register"></a>

Depending on your setup, confirming the batch in BILB will create your general ledger interface file or populate your database with the updated financial information. 
1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 16 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When prompted to confirm the batch, click on Yes.
7 Key in your printer code and press Enter or select it using the pick list.
8 Click Ok. When the batch finishes running, your daily invoice register is printed.

9 Click Ok.
Daily Invoice Register showing section for renewal storage

### REPROCESSING THE FINANCIAL INTERFACE <a id="reprocessing-the-financial-interface"></a>

If you confirm your batch but need to recreate the interface file or repopulate the database with the updated financial information, you can use the FINI option (Reprocess Financial Interface).
1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
HighJump, INC. /usr1/del4/work/faxl Page 4 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 1 of 3
Print Date : 04-02-2000 Renewal Storage - Invoice List Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code & Name Total Charges
S-000111 19-01-2000 A Customer A 48643.16
S-000112 19-01-2000 B Customer B 757900.00
S-000113 19-01-2000 C Customer C 179559.64
S-000114 19-01-2000 D Customer D 107.00
S-000115 19-01-2000 E Customer E 2675.00
 ----------
Total Number of Invoices : 5 Total Charges : 988884.80
 ==========
HighJump, INC. /usr1/del4/work/faxl Page 5 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 2 of 3
Print Date : 04-02-2000 Renewal Storage - Revenue Analysis Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code Total Storage Miscell
S-000111 19-01-2000 A 48643.16 3182.36 0.00 0.00 0.00 0.00 0.00 45460.80
S-000112 19-01-2000 B 757900.00 757900.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000113 19-01-2000 C 179559.64 102879.64 0.00 0.00 0.00 0.00 0.00 76680.00
S-000114 19-01-2000 D 107.00 107.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000115 19-01-2000 E 2675.00 2675.00 0.00 0.00 0.00 0.00 0.00 0.00
 ---------- ---------- ------- ------- ------- ---------- ---------- --------
Totals 988884.80 866744.00 0.00 0.00 0.00 0.00 0.00 122140.80
 ========== ========== ======= ======= ======= ========== ========== 
HighJump, INC. /usr1/del4/work/faxl Page 6 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 3 of 3
Print Date : 04-02-2000 Renewal Storage - G.L. Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
General Ledger Code & Description Total Charges
G.L. Posting Date : 19-01-2000
104200 Handling 122140.80
123456 General 851632.80
123457 Goods & Services Taxes 15111.20
 ----------
Total for Day 988884.80
 ----------
 ----------
Total for All Days 988884.80
 ==========

5 Select Reprocess Financial Interface from the Action dropdown list.
6 When prompted to confirm reprocessing of the financial interface, click on Yes.

### EMAILING OF INVOICES <a id="emailing-of-invoices"></a>

You can email confirmed invoices from BILB (Billing Batch). Emailing of confirmed invoices must be set up for each customer in the configuration program AECS (Automatic Email Setup). In this program, you define the directory where you want to store a copy of your emailed invoices, the subject line for your email message and your email body text.
Invoices are attached to the email in the form of a PDF file.
AECS screen showing sample setup
1 Enter BILB.
2 Select your batch type from the dropdown list.
3 Select the confirmed invoice that you wish to email.
4 In the Action field, select Email Invoice.

### Working With Batches and Invoices <a id="working-with-batches-and-invoices"></a>

The procedures in this section apply to all batch types in BILB: accessorial invoice, daily invoice register, extra charge rater, immediate invoice and renewal invoice.

### REGENERATING A BATCH <a id="regenerating-a-batch"></a>

If a batch fails to generate successfully, the batch will have a status of BEGUN GENERATION. 
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Select Regenerate from the Action dropdown list.
6 When prompted to regenerate the batch, click on Yes.

### REPRINTING AN INVOICE <a id="reprinting-an-invoice"></a>

You can reprint a confirmed invoice as many times as required.
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Select Final Reprint from the Action dropdown list.
6 Key in your printer code and click Ok.

### DELETING A BATCH <a id="deleting-a-batch"></a>

If the status of a batch is GENERATED or PRINTED, you can delete it if required. When you delete a batch, all charges in the batch are released and will be picked up in the next batch that you generate. You use the 
Delete command when you have made a mistake in the generation of your batch and you wish to regenerate it.
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Click on Delete.
6 When prompted to confirm the deletion, click on Yes.

### LOOKING UP A CHARGE ON A BATCH <a id="looking-up-a-charge-on-a-batch"></a>

You look up a charge on a batch by performing a query in ENAC. You can query on the accessorial entry number, bill-to code, date to charge, charge code, batch number, renewal date and many other parameters. 
You can also query on a particular receipt or renewal. Receipt information is shown in the Source Reference 
Number field while the renewal date is shown in the Reference Description field.

For example, to query on all charges on receipt 25, you would enter 25 in the Source Reference Number field. To query on all renewal charges on a renewal batch, you could enter the date of the batch in the 
Reference Description field or you could enter the batch number in the Renewal Batch Number field. To query on all extra charges on a given extra charge batch, you would enter %EXIN Batch <xx> in the Reference 
Description field where xx equals the extra charge batch number.
If the batch has been confirmed and you have run DLRE (Daily Invoice Register), you cannot look up the charge in ENAC. Instead, you must look up the charge in LOAC (Look Up Accessorial). Refer to [Looking Up 
All Charges for a Given Item, Level 2/3/4 Value in LOAC](faturamento-invoicing.html#looking-up-all-charges-for-a-given-item-level-2-3-4-value-in-loac).
1 Enter ENAC.
2 Click on Enter Criteria.
3 Press Enter until you reach the field that you wish to query on. If you wish to query on the Source Reference Number to look up a particular receipt, you would press Enter to bypass all fields on the first page of 
ENAC. When the second page of ENAC is displayed, you would enter the receipt number in the Source 
Reference Number field. 

ENAC showing second page of this screen
4 Key in your query word or code and click on Execute Query.
ENAC will display all records that meet the criteria that you specify.

ENAC screen showing an initial storage on receipt 1417
5 When you finish your query, click on Exit to exit.

### DELETING AND MODIFYING CHARGES ON A CONFIRMED BATCH <a id="deleting-and-modifying-charges-on-a-confirmed-batch"></a>

You can delete or modify a charge on a confirmed batch as long as the daily invoice has not been run in 
DLRE. You delete and modify charges by entering ENAC and making the required changes. After making your changes, you must reprint the batch by means of the RAUD Selection Code. 

### DELETING A CHARGE <a id="deleting-a-charge"></a>

When you delete a charge in ENAC, the charge is permanently deleted and cannot be recreated when you generate a new batch. Should you delete a charge by mistake, you will have to re-enter it manually in ENAC.
1 Enter ENAC.
2 Look up the accessorial charge that you wish to delete. You can use your Enter Criteria and Execute 
Query buttons to query on the Accessorial Entry Number, Bill To Code, Date to Charge, Reference Number or Charge Code fields.
For example, if you wish to modify all charges on receipt 25, you would enter 25 in the Source Reference 
Number field and click on Execute Query to query.
3 When you find the charge that you wish to delete, press Enter to position your cursor in the Reference 
Description field
4 Click on Delete.
5 Click on Exit.

### MODIFYING A CHARGE <a id="modifying-a-charge"></a>

1 Enter ENAC. 
2 Look up the accessorial charge that you wish to modify. You can use your Enter Criteria and Execute 
Query buttons to query on the Accessorial Entry Number, Bill To Code, Date to Charge, Reference Number or Charge Code fields.
For example, if you wish to modify all charges on receipt 61, you would enter 61 in the Source Reference 
Number field and click on Execute Query to query.
3 Press Enter until your cursor is positioned on the field that you wish to change.
4 Key in your new value over the old value and press Enter.
5 Click on Return to Main and Exit to exit.

### TROUBLESHOOTING RENEWAL INVOICING <a id="troubleshooting-renewal-invoicing"></a>

The following chart shows some of the more common problems encountered with renewal invoicing.
batch cannot be confirmed Make sure that there are no previous unconfirmed batches in BILB. If there are, delete or confirm the previous batch and then confirm the current batch.
missing charges on a renewal batch
Check LORE or LOEN to ensure that the product was confirmed and rated. 
Make sure that you did not enter restrictions when generating the batch such as all charges later than June 1 or all charges except those incurred by Customer X.
Check LOEN to ensure that product should renew.
Check CHAR and RATE to ensure that the charge code has been properly set up. If your charge code is correct and has been attached to the proper profiles but there are no rates in RATE for the charge code, no charges will be generated. 
If you are still unable to identify the cause of the missing charge, delete the renewal batch in BILB. Then run 
RENW (Renewal Recalculations) to gather any renewal charges that were missed. Lastly, regenerate the batch in 
BILB.

### LOOKING UP AN INVOICE IN LOIN <a id="looking-up-an-invoice-in-loin"></a>

You look up invoices in the program LOIN (Look Up Invoices). For non-receipt charges, a batch must have a status of CONFIRMED before you can look up an invoice generated from that batch in LOIN. For receipt charges, the receipt must be confirmed and rated before you can look it up in LOIN.
1 Enter LOIN. 
2 Key in your invoice number or receipt number and click on Execute Query. If you do not know the invoice number or receipt number, use your Enter Criteria and Execute Query functions to perform a query on the values that you know (for example, the batch number, customer code, etc.).

Look Up Invoices (LOIN) screen showing invoice 20
3 Click on Revenue Block to display the revenue breakdown of the invoice.
batch takes too long to run Run RENW (Renewal Recalculations) on a regular basis or at least once before you run your renewals.
If you have made a change to a billing profile, the system may have to recalculate the billing history of the item and this may take much longer than usual. However, the next time you run renewals, the batch should take the usual amount of time.
If you have made weight adjustments to older lots, the system may take longer than usual to run.

Look Up Invoices (LOIN) screen showing Revenue Analysis Block
4 If required, click on G.L. Block to view the revenue by general ledger account.
5 Click on Invoice Block and Exit to exit.

### PRINTING AN INVOICE IN LOIN <a id="printing-an-invoice-in-loin"></a>

1 Enter LOIN.
2 Retrieve the invoice that you wish to print.
3 Press Enter. AccellosOne 3PL will display the message “Searching for File.”

Look Up Invoices screen showing the message “Found Invoice”
4 When the “Found invoice” message appears, key in your printer code and press Enter or use your pick list to select it.
5 Click Ok to print.
6 Click on Exit to exit.

### LOOKING UP ALL CHARGES FOR A GIVEN ITEM, LEVEL 2/3/4 VALUE IN LOAC <a id="looking-up-all-charges-for-a-given-item-level-2-3-4-value-in-loac"></a>

You look up all charges for a given item or level 2/3/4 value in the program LOAC (Look Up Accessorial). This program shows the following information about a charge:
 the accessorial entry number and date
 the charge code and amount
 if applicable, the receipt or order number and the line number
 the location billing code, qualifying quantity and SKU, charge on quantity and SKU as well as the rate
For each inventory record retrieved, LOAC shows the total invoiced, the total unbilled and the grand total — that is, both invoiced and unbilled.
Records in LOAC are permanent and cannot be deleted except through the program PURA (Purge Accessorial Batch). Refer to [LOAC (Look Up Accessorial)](faturamento-cash-relatorios.html#loac-look-up-accessorial) for detailed information on each field in 
LOAC.
1 Enter LOAC.

Look Up Accessorial (LOAC)
2 Key in your customer code and press Enter.
If you wish to look up charges not attached to a given item or level 2/3/4 value:
If you wish to look up all charges for a given item or level 2/3/4 value:
a) Click on Execute Query.
b) Use your down arrow key to scroll to the last record in LOAC. 
c) In the last record, the level 2/3/4 fields will be blank to indicate that the charge is not linked to a particular item.
a) Key in the item code and inventory levels that you wish to query and click on Execute Query.

Look Up Accessorial (LOAC) screen showing two charges for item A1, lot 108
3 Click on Accessorial Block to enter the Accessorial Block.
4 Use your arrow keys to position the cursor over the accessorial entry number that you wish to query.
5 Click on Detail Block.

Look Up Accessorial (LOAC) screen showing a receipt charge of 16.00
6 When you finish your query in LOAC, click on Accessl Block and Inventory. Then click on Exit to exit.

### USING INVOICE TYPES TO SPLIT OUT ACCESSORIAL CHARGES <a id="using-invoice-types-to-split-out-accessorial-charges"></a>

You use invoice types in the accessorial billing program BILB (Accessorial Invoicing) to restrict the types of charges that will appear on an invoice or to split out the charges on two or more invoices.
For example, you create an invoice type called LAB for Labor Charges in the program INTP (Invoice Type). 
Then you attach this invoice type to one or more charge codes in CHAR (Charge Code). When you enter 
BILB, you specify in the Select Block of this program that you want only charges whose invoice type is LAB to be included in the invoice. When you run the program, you will have an invoice restricted to accessorial labor charges.
If you do not need to split out your accessorial charges, you create a single invoice type in INTP called NA (Not Applicable).

### BACKDATING OPEN ORDERS AND RECEIPTS <a id="backdating-open-orders-and-receipts"></a>

Backdating open receipts and orders serves two functions in AccellosOne 3PL. First, it allows you to charge renewal storage immediately instead of waiting for the next month or billing period. Second, it can simplify your accounting and financial reporting by ensuring that orders and receipts are always entered and confirmed within the same month or billing period.
For example, suppose a customer has monthly first of month renewal storage billing and you receive product for that customer on November 30 but only confirm it on December 1. If you backdate your receipt to 
November 30, you can charge renewal storage for the month of December. If you do not backdate your receipt to November 30, no renewal storage would be charged for the product until January 1.

To backdate an open receipt or order, you confirm the receipt or order with a ship or receive date equal to the last day of the previous billing period. Then you run your renewal batch with a create date equal to the end of the previous billing period.
1 Do one of the following:

CHOF screen showing cursor in Ship Date field
2 Generate your renewal batch with a create date that equals the ship date or receive date that you entered in the previous step.
3 Print and confirm the renewal batch in the usual manner.
If you have open orders: If you have open receipts:
a) Enter CHOF.
b) Advance the order’s flow to 
COOR.
c) Position your cursor in the Ship 
Date field.
d) Enter the last day of the previous billing period as your ship date.
e) Confirm the order in the usual manner.
a) Enter CHRF.
b) Advance the receipt’s flow to 
CORE.
c) Position your cursor in the 
Receive Date field.
d) Enter the last day of the previous billing period as your receive date.
e) Confirm the receipt in the usual manner.

### Entering Accessorial Bill Later Charges <a id="entering-accessorial-bill-later-charges"></a>

Accessorial bill later charges are miscellaneous type charges such as blast freezing, shrink wrapping, palletization, etc. They accumulate in ENAC (Bill Later - Enter Charges) and can be either attached to a particular receipt or order or entered independently of any given receipt or order.

### ENTERING RECEIPT ACCESSORIAL CHARGES <a id="entering-receipt-accessorial-charges"></a>

You enter this type of charge in ENRE (Enter Receipts). You can enter receipt accessorial charges at either the header level or the line detail level.
1 Enter ENRE.
2 Key in your customer code and press Enter.
3 Key in your shipper code and press Enter.
4 Key in your bill-to code and press Enter.
5 If required, key in values in the various ENRE fields (Receipt Date, Receipt Time, Probill Number and 
Reference Number). If you wish to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 If required, key in a warehouse code and press Enter or press Enter with this field blank to bypass this option.
9 Key in your total number of units and press Enter.
10 Press Enter to bypass the remaining fields until your reach the Accessorial Charges field.
11 AccellosOne 3PL will display the Bill Later - Enter Charges (ENAC) screen.
If you are entering your accessorial charges at the header level:
If you are entering your accessorial charges at the line detail level:
a) In the Accessorial Charges field, key in Y for Yes and press Enter.
b) Continue to press Enter to bypass the Receipt Extra 
Charges and Extra Reference 
Number fields.
a) In the Accessorial Charges field, key in N for No and press Enter.
b) Continue to press Enter to bypass the Extra Charges and 
Extra Reference Number fields.
c) In the Line Detail Block, press 
Enter until your cursor is positioned in the Charge field.
d) In the Charge field, key in Y for 
Yes and press Enter.
e) Key in your item code, quantities, location and any other requested information for your line.

Bill Later - Enter Charges (ENAC)
12 Click on Create Record.
The system will display the customer information of the customer you entered in step 2. If you wish to bill to a party other than the customer who owns the goods, press F9 until your cursor is positioned in the Bill 
To Code field. Then key in the customer code of the bill-to party and press Enter.

Bill Later - Enter Charges (ENAC) screen showing prompt for charge code
13 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then key in Y for Yes and press Enter.
14 In the Charge Code field, key in your charge code and press Enter.
15 If prompted to do so, select the appropriate tax code from the tax code pick list.
16 If prompted to do so, key in your location bill code and press Enter.
17 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45. 

Bill Later - Enter Charges (ENAC) screen showing prompt for rate
18 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the standard rate, key in a new rate and press Enter.
19 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override the system-calculated total, key in a new total and press Enter.
20 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
21 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, click on Return to Main and Master Block to exit the Remark Block.
22 If required, repeat steps 13 to 20 for any additional charges that you wish to assign to the header or line detail blocks.
23 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
24 When you finish entering all your line details, click on Return to Main and Master Block. Then click on 
Exit to exit.

### ENTERING RECEIPT EXTRA CHARGES <a id="entering-receipt-extra-charges"></a>

You enter this type of charge in the header block of ENRE (Enter Receipts) only. You cannot enter receipt extra charges at the line detail level. Unlike receipt accessorial charges, receipt extra charges cannot be billed to a third party; that is, the bill-to party must equal the customer.

If you do not produce a separate warehouse receipt invoice — that is, you include receipt charges with your accessorial charges on an accessorial invoice — there is no need to create receipt extra charges. Instead, create a receipt accessorial charge.
1 Enter ENRE.
2 Key in your customer code and press Enter.
3 Key in your shipper code and press Enter.
4 Key in your bill-to code and press Enter.
5 If required, key in values in the various ENRE fields (Receipt Date, Receipt Time, Probill Number and 
Reference Number). If you wish to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 If required, key in a warehouse code and press Enter or press Enter with this field blank to bypass this option.
9 Key in your total number of units and press Enter.
10 Press Enter to bypass the remaining fields until your reach the Receipt Extra Charges field. Key in Y for 
Yes in this field and press Enter.
11 Press Enter to bypass the Extra Reference Number fields until AccellosOne 3PL displays the Bill Later - 
Enter Charges (ENAC) screen.

Bill Later - Enter Charges (ENAC)
12 Click on Create Record.
The system will display the customer information of the customer that you entered in step 2. 

Bill Later - Enter Charges (ENAC) screen showing prompt for charge code
13 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then key in Y for Yes and press Enter.
14 In the Charge Code field, key in your charge code and press Enter.
15 If prompted to do so, select the appropriate tax code from the tax code pick list.
16 If prompted to do so, key in your location bill code and press Enter.
17 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

Bill Later - Enter Charges (ENAC) screen showing prompt for rate
18 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the standard rate, key in a new rate and press Enter.
19 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override the system-calculated total, key in a new total and press Enter.
20 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
21 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, click on Return to Main and Master Block to exit the Remark Block.
22 If required, repeat steps 13 to 20 for any additional charges that you wish to assign to the header block.
23 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
24 Enter your line details in the normal way and then click on Return to Main and Master Block. Then click on Exit to exit.

### ENTERING ORDER ACCESSORIAL CHARGES <a id="entering-order-accessorial-charges"></a>

You enter this type of charge in ENOR (Enter Orders). You can enter order accessorial charges at the header level, at the line detail level or both. 
1 Enter ENOR.
2 Key in your customer code and press Enter.
3 Key in your consignee code and press Enter.

4 Key in your sold-to code and press Enter.
5 If required, key in values in the various ENOR fields (Order Date, Order Time, To Ship Date, To Ship 
Time, To Arrive Date, To Arrive Time, Customer Order Number and Purchase Order Number). If you wish to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 Key in your freight term and press Enter. If required, key in your COD amount, payment type and message code. 
9 Key in Y for Yes or N for No in the Remarks, Carrier Details, Pallet Details and EDI Details fields and press Enter.
10 AccellosOne 3PL will display the Bill Later - Enter Charges (ENAC) screen.
If you are entering your accessorial charges at the header level:
If you are entering your accessorial charges at the line detail level:
a) In the Accessorial Charges field, key in Y for Yes and press Enter.
b) Continue to press Enter to bypass the Warehouse Code and Extra Reference Number fields.
a) In the Accessorial Charges field, key in N for No and press Enter.
b) Continue to press Enter to bypass the Extra Charges and 
Extra Reference Number fields.
c) In the Line Detail Block, press 
Enter until your cursor is positioned in the Charge field.
d) In the Charge field, key in Y for 
Yes and press Enter.
e) Key in your item code, quantities, location and any other requested information for your line.

Bill Later - Enter Charges (ENAC)
11 Click on Create Record.
The system will display the customer information of the customer that you entered in step 2. If you wish to bill to a party other than the customer who owns the goods, press F9 until your cursor is positioned in the Bill To Code field. Then key in the customer code of the bill-to party and press Enter.

Bill Later - Enter Charges (ENAC) showing prompt for charge code
12 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then key in Y for Yes and press Enter.
13 In the Charge Code field, key in your charge code and press Enter.
14 If prompted to do so, select the appropriate tax code from the tax code pick list.
15 If prompted to do so, key in your location bill code and press Enter.
16 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

Bill Later - Enter Charges (ENAC) showing prompt for rate
17 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the standard rate, key in a new rate and press Enter.
18 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override the system-calculated total, key in a new total and press Enter.
19 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
20 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, click on Return to Main and Master Block to exit the Remark Block.
21 If required, repeat steps 13 to 19 for any additional charges that you wish to assign to the header or line detail blocks.
22 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
23 Enter your line details in the normal way and then click on Return to Main and Master Block. Then click on Exit to exit.

### ENTERING ACCESSORIAL CHARGES IN ENAC <a id="entering-accessorial-charges-in-enac"></a>

You can enter accessorial bill later charges directly in ENAC without creating a receipt in ENRE or an order in 
ENOR. This procedure is useful when you wish to add an accessorial charge to a receipt or order that is already confirmed or you wish create a one-time accessorial charge that is not connected to a particular receipt or order.
1 Enter ENAC.

2 Click on Create Record.
3 In the Bill To Code field, key in the customer that you wish to bill and press Enter.

Bill Later - Enter Charges (ENAC) showing prompt for date
4 In the Date to Charge field, key in your date to charge and press Enter. This date is only used if you enter a date restriction in the Accessorial Date field in BILB. For example, if you enter 25.01.05 in the Date to 
Charge field and (=25.01.05) in the Accessorial Date field, the charge will be excluded from the batch.
If you press Enter in the field without entering a date, ENAC will use the current system date.
5 If required, key in a reference description and/or reference number and press Enter. If the charge is related to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in Y or Yes or N for No and press Enter. Unlike reference descriptions, remarks are for internal purposes only and do not print on the invoice.
7 In the Charge Code field, key in your charge code and press Enter.
8 If prompted to do so, select the appropriate tax code from the tax code pick list.
9 If prompted to do so, key in your location bill code and press Enter.
10 In the Qualifying Quantity field, key in the quantity and press Enter. If you are entering an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

Bill Later - Enter Charges (ENAC) showing prompt for rate
11 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter.
12 In the Total field, press Enter to accept the system total or key in a new total and press Enter.
13 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
14 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your remarks, click on Return to Main and Master Block to return to the Main Block.
15 Repeat steps 7 to 13 for each additional charge for this customer.
16 When you finish entering all your charges, click on Return to Main to exit create mode.
The system will assign an Accessorial Entry Number to the charges. You may wish to write this number down for future reference. It will allow you to access the charge in ENAC directly without the need to scroll through records or query by customer or charge code.
17 Click on Exit to exit.

### ADDING ACCESSORIAL CHARGES TO A CONFIRMED ORDER IN OEXC <a id="adding-accessorial-charges-to-a-confirmed-order-in-oexc"></a>

You can add an accessorial charge to a confirmed order in OEXC (Add Accessorial Charge to Order). You can add this charge at either the header level or the line detail level.
1 Enter OEXC.

2 Key in your order number and press Enter.

Add Accessorial Charge to Order (OEXC) screen showing two order lines on order 1908
3 Position your cursor over the line to which you wish to apply the accessorial charge.
4 Key in Y for Yes and press Enter.
5 Click on Extra Charge.
If you wish to apply the charge to the order header:
If you wish to apply the charge to the order line:
a) In the Order Extra Charge Flag field, key in Y for Yes and press 
Enter.
b) Click on Extra Charge.
c) Proceed to step 6.
a) Click on Order Details.
b) Proceed to next step.

Bill Later - Enter Charges Block
6 When the Bill Later - Enter Charges Block appears, proceed to enter your accessorial charge(s). You add charges to this screen by following the instructions in [Entering Accessorial Charges in ENAC](faturamento-invoicing.html#entering-accessorial-charges-in-enac).
7 When you finish entering your charges, click on Return to Main and Exit to exit. 
ADDING ACCESSORIAL OR RECEIPT EXTRA CHARGES TO A CONFIRMED 
RECEIPT IN REXC
You can add an accessorial or receipt extra charge to a confirmed receipt in REXC (Enter Receipt Extra 
Charges). You can add receipt extra charges at either the header level or the line detail level. You can add accessorial extra charges at the header level only.
If you do not produce a separate warehouse receipt invoice — that is, you include receipt charges with your accessorial charges on an accessorial invoice — there is no need to create receipt extra charges in REXC. 
Instead, create a receipt accessorial charge.
1 Do one of the following:
If you rate your receipts automatically:
If you rate your receipts manually in RCRA (Receipt Rater):
a) Run RERA (Requeue Receipt for 
Rating) to “unrate” the receipt.
a) If you rated your receipt in 
RCRA, you cannot add further charges to it in REXC unless you first “unrate” the receipt in RERA (Requeue Receipt for Rating).

2 Enter REXC.
3 Key in your receipt number and press Enter.

Enter Receipt Extra Charges (REXC) screen showing receipt 1434
4 Position your cursor over the appropriate field (Receipt Extra Charge Flag or Receipt Accessorial Flag), key in Y for Yes and press Enter.

Enter Receipt Extra Charges (REXC) screen showing three receipt lines on receipt 1434
5 Position your cursor over the line to which you wish to apply the receipt extra charge.
If you wish to apply the charge to the receipt header:
If you wish to apply the receipt extra charge to the receipt line:
a) Click on Extra Charge or Accessorial Charge.
b) Proceed to step 7.
a) Click on Receipt Details.
b) Proceed to next step.

6 Key in Y for Yes and press Enter.
7 Click on Extra Charge.

Bill Later - Enter Charges Block
8 When the Bill Later - Enter Charges Block appears, proceed to enter your accessorial or receipt extra charge(s). You add charges to this screen by following the instructions in [Entering Accessorial Charges in ENAC](faturamento-invoicing.html#entering-accessorial-charges-in-enac).
9 When you finish entering your charges, click on Return to Main and Exit to exit. 
10 Do one of the following:

### ENTERING A CREDIT IN ENAC <a id="entering-a-credit-in-enac"></a>

Credits are similar to regular charges except that the quantity is entered as a negative value. If you wish the credit to appear on a separate invoice, you can use the immediate charge program (ENIN) instead of ENAC. 
If the charge code that you use for the credit has a minimum charge, you must enter the credit in ENIN. See [Entering a Credit in ENIN](faturamento-invoicing.html#entering-a-credit-in-enin) for instructions.
1 Enter ENAC.
2 Click on Create Record.
If you rate your receipts automatically:
If you rate your receipts manually in RCRA (Receipt Rater):
a) Run CHRF (Time Stamp and 
Confirm Receipt) to rerate the receipt.
a) Run RCRA to rerate the receipt.

3 In the Bill To Code field, key in the customer that you wish to credit and press Enter.

Bill Later - Enter Charges (ENAC) showing prompt for date
4 In the Date to Charge field, press Enter to accept the current date. 
5 If required, key in a reference description and/or reference number and press Enter. If the credit is related to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in Y or Yes or N for No and press Enter. Unlike reference descriptions, remarks are for internal purposes only and do not print on the invoice.
7 In the Charge Code field, key in your charge code and press Enter.
8 If prompted to do so, select the appropriate tax code from the tax code pick list.
9 If prompted to do so, key in your location bill code and press Enter.
10 In the Qualifying Quantity field, key in the quantity and press Enter. Because you are entering a credit, you must enter the quantity as a negative.
11 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter. 
12 In the Total field, press Enter to accept the system total or key in a new total and press Enter.
13 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your remarks, click on Return to Main and Master Block to return to the Main Block.
14 When you finish entering all your charges, click on Return to Main and Exit.

### ENTERING A CUSTOMER DEPARTMENT IN ENAC <a id="entering-a-customer-department-in-enac"></a>

You can assign a department code to a manual charge entered in ENAC. Department codes are used solely for reporting purposes and financial integration and serve no other function in AccelosOne 3PL. You maintain your customer/department relationships in CUDE and you activate customer department codes in COMP (Company Parameters) by selecting the appropriate option - None, Allow, Required - in the new field 
Department Entry for Charges.
CUDE screen
When customer departments are activated, the Department dropdown list in ENAC is populated with the departments that you set up in CUDE.

### Working With Accessorial Bill Immediately Charges <a id="working-with-accessorial-bill-immediately-charges"></a>

These charges are one-time miscellaneous charges that are not attached to a particular order or receipt — for example, overtime, faxing and long distance charges — and that you wish to invoice immediately. You enter this type of charge in ENIN (Enter Charges - Bill Immediately). Unlike bill later accessorial charges, immediate accessorial charges do not accumulate in ENAC. 
There are five main steps in billing and invoicing immediate accessorial charges:
 you enter your charges in ENIN
 you generate the batch in BILB
 you print the audit
 you confirm the batch
 you print the invoice

### ENTERING YOUR CHARGES IN ENIN <a id="entering-your-charges-in-enin"></a>

1 Enter ENIN.
2 Click on Create Record.
3 In the Bill-To Code field, key in the customer that you wish to bill and press Enter.

Bill Immediate - Enter Charges (ENIN)
4 In the Invoice Date field, press Enter to accept the current system date as your invoice date or key in a new date and press Enter. This date is only used if you enter a date restriction in the Invoice Date field in 
BILB. For example, if you enter 25.01.01 as your invoice date in ENIN and (=25.01.01) in the Invoice 
Date field in BILB, the charge will be excluded from the batch.
5 If required, key in a description in the Reference Description field and press Enter or press Enter with this field blank to bypass this option. This reference description is for internal purposes only and does not print on the invoice.
6 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field apply to the entire invoice. If you wish to enter remarks for each charge, you do so in the Charge Block, not the Main Block.
Unlike reference descriptions, remarks print on the invoice.
7 Do one of the following:
If you entered N for No: If you entered Y for Yes:
a) Proceed to next step. a) Key in your first line of your remarks and press Enter.
b) If required, key in your second and any additional lines that you require and press Enter at the end of each line. To exit the 
Remark Block, click on Return to 
Main and Master Block.
c) Click on Charge Block.

8 In the Charge Code field, key in your charge code and press Enter.
9 In the Reference Description field, key in a reference description and press Enter or press Enter with this field blank to bypass this option.
10 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field apply to each charge in the Charge Block.
11 If prompted to do so, key in your location bill code and press Enter.
12 In the Qualifying Quantity field, key in the quantity to be charged for and press Enter. If you are entering an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.
13 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the standard rate, key in a new rate and press Enter.
14 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override the system-calculated total, key in a new total and press Enter.
15 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
If you entered N for No in the 
Remarks field:
If you entered Y for Yes in the 
Remarks field:
a) Proceed to next step. a) Key in your first line of your remarks and press Enter.
b) If required, key in your second and any additional lines that you require and press Enter at the end of each line. To exit the 
Remark Block, click on Return to 
Main and Exit.
c) To add an additional charge, click on Charge Block then Create Record.

Bill Immediate - Enter Charges (ENIN) showing Charge Block
16 If required, repeat the above steps for any additional charges that you wish to assign to the invoice.
17 When you finish adding all your charges, click on Return to Main and, if required, Remark Block. Then click on Master Block and Exit.
Note the system-generated invoice number at the top of your screen. You will need this number if you wish to look up the invoice in LOIN (Look Up Invoices).

### ENTERING A CREDIT IN ENIN <a id="entering-a-credit-in-enin"></a>

Credits are similar to regular charges except that the quantity is entered as a negative value. If the charge code that you use for the credit has a minimum charge and the quantity that you enter triggers that minimum charge, the system will display the minimum charge (a positive number) rather than the credit amount (a negative number) as the charge total. When this happens, you must enter the credit amount manually in the 
Total field (for example, -15 for a credit amount of 15 currency units).
1 Enter ENIN.
2 Click on Create Record.
3 In the Bill To Code field, key in the customer that you wish to credit and press Enter.

Bill Immediate - Enter Charges (ENIN) showing prompt for date
4 In the Invoice Date field, press Enter to accept the current date. 
5 If required, key in a reference description and/or reference number and press Enter. If the credit is related to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field apply to the entire invoice. If you wish to enter remarks for each charge, you do so in the Charge Block, not the Main Block.
Unlike reference descriptions, remarks do print on the invoice.
7 If prompted to do so, key in your location bill code and press Enter.
8 In the Charge Code field, key in your charge code and press Enter.
If you entered N for No: If you entered Y for Yes:
a) Proceed to next step. a) Key in your first line of your remarks and press Enter.
b) If required, key in your second and any additional lines that you require and press Enter at the end of each line. To exit the 
Remark Block, click on Return to 
Main and Master Block.
c) Click on Charge Block.

9 In the Qualifying Quantity field, key in the quantity and press Enter. Because you are entering a credit, you must enter the quantity as a negative.
10 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter. 
11 In the Total field, press Enter to accept the system total or key in a new total and press Enter. If the charge code that you use has a minimum charge, you may need to override the total amount (a positive number representing the minimum charge) by the credit amount (a negative number).
12 If the GST field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and press Enter.
13 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your remarks, When you finish entering your remarks, click on Return to Main and Master Block to return to the Main Block.
14 When you finish entering all your charges, click on Return to Main and Exit.

### GENERATING AN IMMEDIATE ACCESSORIAL BATCH <a id="generating-an-immediate-accessorial-batch"></a>

Each time you generate an immediate accessorial batch, all immediate accessorial charges that have accumulated in ENIN since the confirming and printing of your last invoice will be placed in a batch and assigned a batch number by the system.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing immediate invoices
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
CAUTION Do not generate an immediate accessorial batch if another operator is entering a charge in ENIN. Wait until the operator has finished entering the charge before you begin working in BILB.

5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all immediate charges that were entered up to and including the cut-off date will be included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing immediate accessorial restrictions
8 Proceed to specify restrictions on the charges that you wish to place on your accessorial invoice. For example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 (for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 (for example, CUST1, CUST111, CUST299, CUST2ABC)

9 In the Invoice Number field, key in your invoice number restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter invoice number restrictions in this field, only charges for those invoices that meet the restriction will be included in the batch. If you leave this field blank, your invoice will include all charges regardless of invoice number.
10 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
11 In the Invoice Date field, key in your date restrictions and press Enter or press Enter with this field blank for no restrictions. You must enter your date restrictions in YYYY.MM.DD format.
If you enter a date in this field, only those immediate accessorial charges with a invoice date that meets the date restriction that you specify will be generated. If you leave this field blank, all accessorial charges regardless of their invoice value will be generated.
(=CUST1) All customers except customer 1 (=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If you exceed this limit, AccellosOne 3PL will display an error message. Remove one or two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or “<“ and “>” in the same field.
NOTE Any restrictions that you enter in this field will operate within the cut-off date that you defined in the Create Date field in the Main Block of BILB. For example, you can specify Jan 1/05 as your cut-off date — that is, no charges later than that date — and you can specify > Dec 1/04 as your Invoice Date restriction. This would result in a batch of all charges created between Dec 1/04 and Jan 1/05.

Immediate Invoice Invoicing (BILB) screen showing a batch being generated for all charges with an invoice date later than 06.08.07
12 Click on Generate Batch. 

### PRINTING THE IMMEDIATE ACCESSORIAL AUDIT <a id="printing-the-immediate-accessorial-audit"></a>

The immediate accessorial audit shows each charge that will appear on the invoice. The purpose of this report is to allow you to verify all charges before confirming and printing the final invoice.
Refer to [Working With Audit Batch Restrictions](faturamento-invoicing.html#working-with-audit-batch-restrictions) for further information on audit reports.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 79 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch screen showing restrictions for immediate audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will be displayed.
CONFIRMING THE BATCH AND PRINTING THE IMMEDIATE ACCESSORIAL 
INVOICE
If all the charges on the Immediate Invoice Audit report are correct, you are ready to confirm the batch and print the invoice. If the batch or any charge on it is not correct, you must delete the batch and generate a new one.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 79 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.

### Adding Charges to a Confirmed Receipt <a id="adding-charges-to-a-confirmed-receipt"></a>

If a receipt has been confirmed but not invoiced, you can add new accessorial charges to the receipt in RECH (Receipt Charges) as well as modify/delete existing charges. RECH also allows you to look up existing charges for the receipt without adding any new charges.
If there are extra charges on the receipt, running RECH will automatically generate and confirm the extra charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra charge audit and confirm the extra charge batch. 
1 Enter RECH.
2 Key in your receipt number and press Enter.
NOTE Extra charge batches created through RECH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra charges on the extra charge batch are fully editable in ENAC.

RECH screen showing previously entered charges for receipt
RECH displays all previously entered charges for the receipt. The A/O flag shows whether the charge is automatic or optional (that is, whether or not you can override the charge at receipt/order confirmation). 
3 If you click on Detail/Summary Records , you can toggle between detail view (all charges listed individually) and summary view (charges summarized by charge code).
4 Do one of the following:
If you wish to add an accessorial charge to the receipt:
If you wish to modify an existing charge on the receipt:
a) In the Header Block, click on All 
Charges/ENAC . 
b) Enter your accessorial charge(s) 
in the normal manner.
a) In the Detail Block, click on This 
Charge/ENAC beside the charge that you wish to modify. 
b) Proceed to modify the charge in the normal manner.

RECH screen showing existing charge
5 When you finish entering, modifying or deleting your charge(s), click on Exit .

### DELETING A CHARGE <a id="deleting-a-charge"></a>

1 In the Detail Block, click on the charge that you wish to delete and click on Delete All Charges/ENAC
. 
2 When prompted to confirm the deletion, click on Yes.

### Adding Charges to a Confirmed Order <a id="adding-charges-to-a-confirmed-order"></a>

If an order has been confirmed but not invoiced, you can add new accessorial charges to an order in ORCH (Order Charges) as well modify/delete existing charges. ORCH also allows you to look up existing charges for the order without adding any new charges. 

If there are extra charges on the order, running ORCH will automatically generate and confirm the extra charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra charge audit and confirm the extra charge batch. 
1 Enter ORCH.
2 Key in your order number and press Enter.
ORCH screen showing previously entered charge for order
ORCH displays all previously entered charges for the order. The A/O flag shows whether the charge is automatic or optional (that is, whether or not you can override the charge at receipt/order confirmation).
3 If you click on Detail/Summary Records , you can toggle between detail view (all charges listed individually) and summary view (charges summarized by charge code).
4 Do one of the following:
NOTE Extra charge batches created through ORCH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra charges on the extra charge batch are fully editable in ENAC.
If you wish to add an accessorial charge to the order:
If you wish to modify an existing charge on the order:
a) In the Header Block, click on All 
Charges/ENAC . 
b) Enter your accessorial charge(s) 
in the normal manner.
a) In the Detail Block, click on This 
Charge/ENAC beside the charge that you wish to modify. 
b) Proceed to modify the charge in the normal manner.

ORCH screen showing existing charge
5 When you finish entering, modifying or deleting your charge(s), click on Exit .

### DELETING A CHARGE <a id="deleting-a-charge"></a>

1 In the Detail Block, click on the charge that you wish to delete and click on Delete All Charges/ENAC
. 
2 When prompted to confirm the deletion, click on Yes.

### Rollup Invoicing <a id="rollup-invoicing"></a>

Rollup invoicing allows you to generate a single invoice for a customer across multiple companies based on the charges for that customer in each of the companies.
The charges need not be the same across companies. For example, you can charge for handling by the piece in company 1 and charge handling by weight in company 2. AccellosOne 3PL will calculate the correct charges in both companies and produce a single invoice in the rollup company showing the total handling for both companies. 
Rollup invoicing is only available for renewal and accessorial invoices and consequently should only be used with the UREC and UALL invoicing types. Receipt and immediate charges will be correctly calculated and 

invoiced in your separate companies for each customer; however, when you generate your rollup invoice, receipt and immediate charges will not be rolled up.
Rollup invoicing requires a minimum of three companies:
 a rollup company for creating a single cross-company invoice for the customers requiring such an invoice
 two or more child companies — a child company is the company in which the actual charges are generated
The customers in your child companies should all have the same invoicing type. It is not recommended to mix invoicing types for the same customer across multiple child companies.
The following diagram shows invoice processing for a renewal invoice (UREC) customer.
child receipt charges child renewal charges child daily invoice register rollup customer charges child accessorial invoice child extra charges child accessorial charges non-rollup customers posted to GL child renewal invoice rollup accessorial invoice rollup renewal invoice rollup daily invoice register rollup customers posted to GL all charges except receipt and immediate charges passed to rollup company

### SETTING UP ROLLUP INVOICING <a id="setting-up-rollup-invoicing"></a>

You define your rollup and child companies in COMP (Company Code) be entering the appropriate value in the Rollup Type field. There are three possible values for the Rollup Type field:
C = Child
N = Not Applicable
R = Rollup

### SETTING UP YOUR ROLLUP COMPANY <a id="setting-up-your-rollup-company"></a>

1 Enter COMP.
2 Click on Create Record.
3 Enter your company code, company description and the other requested information.
4 When you reach the Rollup Type field, key in R for Rollup and press Enter.
5 When you finish setting up your company, click on Return to Main to exit create record mode. Then click on Exit to exit.

Company Code (COMP) screen showing roll-up company R1

### SETTING UP YOUR CHILD COMPANIES <a id="setting-up-your-child-companies"></a>

1 Enter COMP.
2 Click on Create Record.
NOTE If your company is already set up, you cannot adjust its rollup type. Contact your HighJump consultant for assistance.

3 Enter your company code, company description and the other requested information.
4 When you reach the Rollup Type field, key in C for Child and press Enter.
5 When you finish setting up your company, click on Return to Main to exit create record mode. Then click on Exit to exit.
6 Repeat the above steps for each additional child company that you wish to set up.

Company Code (COMP) screen showing child company C1

### ATTACHING YOUR CHILD COMPANIES TO THE ROLLUP COMPANY <a id="attaching-your-child-companies-to-the-rollup-company"></a>

You attach your child companies to your rollup company in the Rollup Block of your rollup company. 
1 Enter COMP.
2 Key the company code for your rollup company and press Enter.
3 Click on Rollup Block.
4 If you are not in Create Record mode, click on Create Record.
5 Key in your child company code and press Enter.
6 Press Enter to bypass the Report field.
7 In the Invoice field, key in Y for Yes and press Enter.
8 Repeat the above steps for each additional child company that you wish to add to your rollup company.
9 When you finish adding your child companies, click on Return to Main.

Company Code (COMP) screen showing Rollup Block
10 Click on Master Block and Exit to exit.

### SETTING UP YOUR CUSTOMERS <a id="setting-up-your-customers"></a>

1 In the child companies, set up your customer(s) in the normal manner. These customers can have receipt invoices but the receipt charges on such invoices will NOT be rolled up to the rollup company’s accessorial invoice.
2 In the rollup company, set up the same customer or customers that you defined in your child companies. 
Your rollup customer must have the same customer code as your child customers and be defined as an invoice only customer — that is, a customer with no inventory.
The invoicing type that you define in DBIP for your rollup customer must be the same as the invoicing type defined in your child companies.

### GENERATING AND PRINTING ROLLUP INVOICES <a id="generating-and-printing-rollup-invoices"></a>

When generating and printing rollup invoices, you follow the same procedures that you use for accessorial (UALL) or renewal (UREC) invoicing.
1 For each child company, generate and print the appropriate batches according to the normal procedures for accessorial or renewal invoicing.
2 Run the daily invoice register (BILB) for each child company.
3 In your rollup company, generate and print the appropriate batches. If your child companies have accessorial invoicing, follow the normal procedures for accessorial invoicing. If your child companies have renewal invoicing, follow the normal procedures for renewal invoicing.
4 Run the daily invoice register (BILB) for your rollup company.

### Billing Audit System <a id="billing-audit-system"></a>

The billing audit system allows you to track changes to and deletions of any charge in ENAC or ENIN. For example, if an operator changes the charge code, qualifying quantity, rate or total of a charge in ENAC, AccellosOne 3PL will create a complete record of the change, showing the date and time of the change, the operator code, the accessorial number and what was changed.

When changing or deleting a charge in ENAC or ENIN, the operator will be required to enter a reason code describing the rationale for the change. Reason codes are user-defined in the setup program REAS.
You can look up your changes and deletions in ACAL (Look Up Changes to Accss. Charges) and you can print them in the report ACCA (Accessorial Charge Changes Report). Changes and deletions remain on your system until you purge them in PACA (Purge Changes to Accss. Charges).
If you activate the authorization component of the billing audit system, changes to any charge in ENAC must be individually approved in a separate program before it can be placed on a batch and invoiced. Likewise, manual charges1 created in ENAC will be subject to the same approval process.

### SETTING UP THE BILLING AUDIT SYSTEM <a id="setting-up-the-billing-audit-system"></a>

There are two steps to follow in setting up the billing audit system:
 you activate the billing audit system
 you set up your reason codes

### ACTIVATING THE BILLING AUDIT SYSTEM <a id="activating-the-billing-audit-system"></a>

The billing audit system must be activated by selecting the appropriate option in the Force Audit of Accessorial Charges field in COMP (Company Code). There are three options available for the billing audit system:
1 Enter COMP.
2 Retrieve the company that you wish to set up for the billing audit system.
3 Click on Company Parameters.
4 Click on the Miscellaneous tab.
5 Select the appropriate option from the Force Audit of Accessorial Charges dropdown list.
1. A manual charge is any charge that is not automatically generated by the system. For example, extra charges added to a receipt or order and accessorial charges entered through ENAC or ENIN are all considered to be manual charges.
OPTION DESCRIPTION
Neither Tracking nor 
Authorization
The billing audit system is deactivated. There is no tracking of changes, additions and deletions in ENAC or ENIN and no authorization is required.
Tracking Only The following logic applies:
 any changes made to existing charges in either ENAC or ENIN are tracked
 deletions of existing charges in either ENAC or ENIN are tracked
 manual charges added to ENAC are NOT tracked
 no authorization is required
Tracking and AuthorizationThe tracking options of A (Tracking Only) plus the following logic:
 authorization is required to add manual charges to ENAC
 authorization is required to make changes to existing charges in ENAC 

COMP screen showing three options in Force Audit of Accessorial Charges field
6 When you finish making your charges, click on Save.
7 Click on Return to exit the Company Parameters Block.
8 Click on Exit.

### SETTING UP YOUR REASON CODES IN REAS <a id="setting-up-your-reason-codes-in-reas"></a>

Reason codes are required whenever you modify or delete a charge in either ENAC or ENIN. They describe the reason why the record is being modified or deleted. You set up your reason codes in REAS (Reason 
Code). If you do not require reason codes, set up a single code called NA (Not Applicable). 
1 Enter REAS.
2 Click on Enter Criteria then Execute Query to see which reason codes have already been set up.
3 If the code that you require has not been set up, click on Create Record.
4 Key in your reason code and press Enter.
5 Key in a description for your new reason code and press Enter.
6 Key in I for Internal and press Enter.
7 Repeat the above steps for each additional reason code that you wish to set up.
8 When you finish adding your reason codes, click on Return to Main.

REAS screen showing two internal reason codes
9 Click on Exit to exit.

### CHANGING AND DELETING CHARGES <a id="changing-and-deleting-charges"></a>

You can change or delete any charge in ENAC or ENIN as long as the charge has not been posted to the daily invoice register in the program DLRE. When you change or delete a charge, you must enter a reason code explaining the rationale for the change.

### CHANGING AND DELETING CHARGES IN ENAC <a id="changing-and-deleting-charges-in-enac"></a>

1 Enter ENAC.
2 Retrieve the charge that you wish to modify or delete.

ENAC screen showing blast freezing charge
3 Do one of the following:
4 Click on Return to Main and Exit to exit.

### CHANGING AND DELETING CHARGES IN ENIN <a id="changing-and-deleting-charges-in-enin"></a>

1 Enter ENIN.
2 Retrieve the invoice containing the charge that you wish to modify or delete.
3 Click on the Charge Block.
If you wish to modify the charge: If you wish to delete the charge:
a) Press Enter until your cursor is positioned in the field that you wish to change. You can change the Qualifying Quantity, the Rate and/or the Total.
b) Proceed to make your changes.
c) Key in your reason code and press Enter.
a) Press Enter to display the Delete button.
b) Click on Delete.
c) Key in your reason code and press Enter.
d) Click on Delete again.

ENIN screen showing three charges on invoice 57
4 If there is more than one charge on the invoice, use your arrow keys to select the appropriate charge.
5 Do one of the following:
6 Click on Return to Main and Master Block.
7 Click on Exit to exit.

### TRACKING CHANGES TO ENAC AND ENIN CHARGES <a id="tracking-changes-to-enac-and-enin-charges"></a>

There are two programs that you can use for tracking changes to ENAC and ENIN charges: a look-up program called ACAL (Look Up Changes to Accss. Charges) and a report called ACCA (Accessorial Charge 
Changes Report). Both programs show the same information.
If you wish to modify the charge: If you wish to delete the charge:
a) Press Enter until your cursor is positioned in the field that you wish to change. You can change the Qualifying Quantity, the Rate and/or the Total.
b) Proceed to make your changes.
c) Key in your reason code and press Enter.
a) Press Enter once to position your cursor in the Charge field.
b) Click on Delete.
c) Key in your reason code and press Enter.
d) Make sure that your cursor is positioned on the charge that you just deleted.
e) Press Enter once to position your cursor in the Charge field.
f) Click on Delete again. The record will disappear from your screen.

If a charge has been modified in either ENAC or ENIN, the Action field will be set to UPD and the original and current values will be shown. One record in ACAL/ACCA will be created for each value that was changed.
If a charge has been deleted in either ENAC or ENIN, the Action field will be set to DEL and one record in 
ACAL/ACCA will be created for each enterable field in ENAC or ENIN (for example, Customer Code, Date to 
Charge, Reference Number, Remark Flag, Charge Code, etc.).

### LOOKING UP CHANGES IN ACAL <a id="looking-up-changes-in-acal"></a>

1 Enter ACAL.
2 Key in your search criteria and click on Execute Query.

ACAL screen showing eight updated records for ENAC
3 When you finish looking up your charges, click on Exit to exit.

### RUNNING THE ACCESSORIAL CHARGE CHANGES REPORT (ACCA) <a id="running-the-accessorial-charge-changes-report-acca"></a>

1 Enter ACCA.
2 Do one of the following:
If you wish to report on ENAC records only:
If you wish to report on ENIN records only:
a) Key in ENAC as your program name and press Enter.
a) Key in ENIN as your program name and press Enter.

ACCA screen showing ENAC option selected
3 Key in your start date and press Enter. Then key in your end date and press Enter. Only charges that were modified or deleted between the start and end dates that you specify will be reported on.
4 Key in your printer code and press Enter.
5 Click Ok.
ACCA report showing five changes

### AUTHORIZING YOUR CHARGES <a id="authorizing-your-charges"></a>

If the authorization component of the billing audit system is activated, you must authorize the following:
 any new manual charges added to ENAC
 any changes to existing charges in ENAC 
You authorize your charges in two steps: first you run the report OAUD (Accessorial Charges Authorization 
Audit) and second you individually approve each charge in ACAU (Accessorial Authorization). If you make a change to a charge in ENAC after performing these two steps, you must rerun OAUD and reauthorize the charge in ACAU.
ABC Warehousing, Inc. Page 1 of 1
Accessorial Charge Changes Report 02.24.06 09:49
------------------------------------------------------------------------------------------------------------------------------------
Accessorial Charges (ENAC)
 Accss Column Original Current
Update Date Operator Actn Number Name Value Value
------------------ -------- ---- --------- ---------------------- ------------------------------ ------------------------------
02.24.06 09:43:31 LORNE UPD 44012 Charge Rate 20 15
 UPD 44012 Charge Total 20 30
02.24.06 09:45:30 LORNE UPD 44015 Charge Code C1 CHAR-1
 UPD 44015 Loc Bill Code COOL
 UPD 44015 Charge Rate .825 1
 UPD 44015 Charge Total 20.63 25

### RUNNING THE ACCESSORIAL CHARGES AUTHORIZATION AUDIT (OAUD) <a id="running-the-accessorial-charges-authorization-audit-oaud"></a>

OAUD is an audit report. Each time that you run OAUD, AccellosOne 3PL will group all ENAC charges that meet the criteria that you specified on the parameter screen and assign those charges an audit number. The audit number that the system will assign is simply the next number in the audit number sequence. This audit number will also show on the report.
Each time that you run OAUD, only charges modified or added since the last time that you ran the report are included. You cannot generate the same report twice in OAUD. If you wish to report on charges assigned to a previous audit, you must set the Reprint flag to Y for Yes and enter your audit number in the Reprint Audit 
Number field.
1 Make sure that you have at least one manual charge to bill. If the manual charge is attached to a particular receipt or order, the receipt or order must be confirmed.
2 Enter OAUD.

OAUD screen
3 In the Customer Code field, key in your customer code and press Enter or press Enter with this field blank to include all customers.
4 In the Operator Code field, press Enter to accept your own operator code or key in another operator code and press Enter.
5 In the Location Bill Code field, key in your location billing code and press Enter or press Enter with this field blank to include all location billing codes.
6 Do one of the following:
If you are printing the report for the first time: If you are reprinting the report:
a) Proceed to next step. a) In the Reprint field, key in Y for 
Yes and press Enter.
b) Key in your audit number and press Enter.

7 Key in your printer code and press Enter.
8 Click Ok.
OAUD report showing a blast freezing charge for Customer A

### AUTHORIZING THE CHARGES IN ACAU <a id="authorizing-the-charges-in-acau"></a>

Once you have reviewed the ENAC charges on the report and approved them, you are ready to authorize them in ACAU.
1 Enter ACAU.
2 Click on Enter Criteria then Execute Query to retrieve all charges that require authorization.
ABC Warehousing, Inc. Page 1 of 1
Customer : A Operator : BJONES Location Billing : All
 Accessorial Charges Authorization Audit (OAUD) 02.16.09 15:45
 Accessorial Entry Number 47581 Audit Number 4
 Bill To Code A
 Name Customer A
 Address 1 100 Renfrew Drive, Suite 100
 Address 2
 Address 3
 City Markham State ON
 Zip Code L3R 9R6
 Date To Charge FEB.16.09
 Reference Description
 Reference Number
 Charge Code BF1
 Description Blast Freezing 1
Loc --Qualifying-- ----Charge----
Bill Quantity Sku Quantity Sku Rate Total
 20000 LBS 200 CWT .700 140.00
Remarks

Accessorial Authorization (ACAU)
3 Click on Authorize to authorize the first charge.
4 Press your down arrow key to display the next record and click on Authorize to authorize it.
5 Repeat the above step for each charge that you wish to authorize.
6 When you finish authorizing all your charges, click on Exit to exit.
The charges that you authorized can now be placed on a batch and invoiced. 

### PURGING CHANGE RECORDS IN PACA <a id="purging-change-records-in-paca"></a>

Change records are automatically created by AccellosOne 3PL in ACAL and ACCA whenever you change or delete an existing charge in either ENAC or ENIN. They remain on your system until you purge them in 
PACA.
When you purge change records in PACA, the records are permanently removed from the database and cannot be restored. You can no longer view the records in ACAL or print them in the report ACCA.
1 Enter PACA.
NOTE PACA should be run on a regular basis to remove old records from the database. Failure to purge these records could eventually lead to slower system performance and a lack of disk storage space.

2 Do one of the following:

PACA screen showing ENAC option selected
3 In the All Changes Before field, key in your cut-off date and press Enter.
4 Click on Process Purge.
5 When the “Do you want to proceed with DELETE” message appears, click on Yes.

### Invoicing by Warehouse <a id="invoicing-by-warehouse"></a>

Invoicing by warehouse allows you to generate separate batches and invoices in BILB by warehouse. For example, you could generate one renewal batch for product stored in warehouse 1 and a second renewal batch for product stored in warehouse 2. 
There are three setup programs for invoicing by warehouse:
 COMP (Company Parameters Block)
 LODE (Location Billing Code)
 DOCU (Documents)
If you wish to purge ENAC records only:
If you wish to purge ENIN records only:
If you wish to purge all records:
a) Key in ENAC as your program name and press Enter.a) Key in ENIN as your program name and press Enter.
a) Press Enter to bypass the Program Name field.

### ACTIVATING INVOICING BY WAREHOUSE IN COMP <a id="activating-invoicing-by-warehouse-in-comp"></a>

Invoicing by warehouse must be activated in COMP (Company Code). There are two possible configurations for invoicing by warehouse:
1 Enter COMP.
2 Key in your company code and press Enter.
3 Click on Company Parameters.
4 Click on the Miscellaneous tab.
FIELD DESCRIPTIONS (MISCELLANEOUS TAB)
Warehouse Code 
Optional for Invoicing by 
Warehouse
No
Yes
If you select Yes, the Warehouse Code field in BILB is optional. That is, you do not need to specify a warehouse when generating your accessorial, extra charge, renewal and immediate batches. If you select No, the Warehouse 
Code field in BILB is mandatory.
If you leave this field blank, invoicing by warehouse is deactivated.
Warehouse Code Mandatory for Invoicing by 
Warehouse
No
Yes
If you select Yes, the Warehouse Code field in BILB is mandatory. That is, you will not be able to generate a batch without specifying a warehouse restriction.If you select No, the Warehouse Code field in BILB is optional.
If you leave this field blank, invoicing by warehouse is deactivated.

COMP screen showing invoicing by warehouse deactivated
5 Select the appropriate value (Yes or No) in the two invoicing by warehouse fields.
6 When you finish making your changes, click on Save to save your changes.
7 Click on Return to exit the Company Parameters Block.
8 Click on Exit to exit.

### ASSIGNING YOUR LOCATION BILLING CODES TO WAREHOUSES IN LODE <a id="assigning-your-location-billing-codes-to-warehouses-in-lode"></a>

In LODE you must assign each location billing code to the appropriate warehouse(s). For example, suppose you had two location billing codes (COOL and DRY) in your company and three warehouses (1, 2 and 3). If 
COOL and DRY applied to all three warehouses, for each LODE record you would have to set up three detail records in the Warehouse Restriction Block: one for warehouse 1, a second for warehouse 2 and a third for warehouse 3.
If you had only two warehouses (1 and 2) and warehouse 1 was your COOL warehouse while warehouse 2 was your DRY warehouse, each LODE record would contain a single record in the Warehouse Restriction 
Block. 
1 Enter LODE.
2 Click on Enter Criteria and Execute Query to retrieve your location billing codes.
3 Select your first location billing code and press Enter.
4 Click on Warehouse Restriction.

LODE screen showing Location Billing Warehouse Restriction block
5 Click on Create Record.
6 Key in your warehouse code and press Enter.
7 Repeat the above steps for each additional warehouse that you wish to link to the location billing code.
8 When you finish assigning warehouse codes to location billing codes, click on Return to Main.

LODE screen showing location billing code COOL assigned to two warehouses
9 Click on Master Block and Exit to exit.

### SETTING UP YOUR ADDRESS OPTION IN DOCU <a id="setting-up-your-address-option-in-docu"></a>

In DOCU you must set the Print Company/Warehouse Address flag to the appropriate value for each invoice document. If you set this field to C for Company, the company’s address will print on the invoice. If you set this field to W for Warehouse, the warehouse address will print on the invoice. 
1 Enter DOCU.
2 Retrieve the invoice document or documents — ACCE, IINV and RENW — that you wish to set up for 
3 In the Print Company/Warehouse Address field, key in C for Company or W for Warehouse and press 
Enter.

DOCU screen showing Print Company/Warehouse Address to C for Company
4 Click on Return to Main and Exit to exit.

### ENTERING RECEIPTS AND ORDERS IN ENRE/ENOR <a id="entering-receipts-and-orders-in-enre-enor"></a>

When invoicing by warehouse is activated, the Warehouse Code field in the Header Block of ENRE and 
ENOR is a mandatory field.

ENRE screen showing Warehouse Code field

### ENTERING BATCH RESTRICTIONS IN BILB <a id="entering-batch-restrictions-in-bilb"></a>

If the Warehouse Code Mandatory for Invoicing by Warehouse flag in COMP (Company Parameters) is set to 
No, the warehouse code restriction in BILB is not mandatory. If the Warehouse Code Mandatory for Invoicing by Warehouse is set to Yes, the warehouse code restriction in BILB is a mandatory field.

Billing Batch (BILB) screen showing dropdown list for warehouse code

### ENTERING CHARGES IN ENAC/ENIN <a id="entering-charges-in-enac-enin"></a>

When invoicing by warehouse is activated, the Location Billing Code field in ENAC and ENIN is a mandatory field.

Bill Later Enter Charges (ENAC) showing Location Billing Code field

### Invoicing by Inventory Level <a id="invoicing-by-inventory-level"></a>

Invoicing by inventory level allows you to generate renewal and accessorial invoices for individual items, lots and pallet ID’s in BILB. You activate invoicing by inventory level in CUST by entering the inventory level that you wish to invoice by in the Invoices at Inventory Level field.

CUST screen showing invoicing by level 2
In BILB you enter your inventory level restrictions in the Billing Level 1, 2 or 3 fields when you create a new accessorial or renewal batch.
BILB screen showing new accessorial batch restricted to lots 101, 105 and 104 through 105

### Reversing Charges on Confirmed Invoices <a id="reversing-charges-on-confirmed-invoices"></a>

CRIN (Credit Invoice) allows you to reverse charges on accessorial, receipt, renewal and immediate invoice after they have been confirmed. When you run the daily invoice register, the reversed charges are listed in the register. If AccellosOne 3PL is linked to your accounting system, the reversed charges are also added to your general ledger interface file and posted to the appropriate account in your accounting system.
1 Enter CRIN.
2 Key in your search criteria: invoice number, prefix, type (RCPT, RENW, ACCE or IINV), date, customer code or amount.
3 When you finish entering your query values, click on Execute Query.
Credit Invoice (CRIN) showing accessorial invoices for customer RF009
AccellosOne 3PL will display the Accessorial tab showing all your accessorial charges. If you wish to reverse charges on an immediate invoice, click on the Immediate tab to display your immediate invoices.
4 Click on the charge(s) that you wish to reverse. If you wish to reverse all charges on an invoice, click on 
 Select All.
5 When you finish selecting your charge(s), click on Save.
Prompt to reprocess invoice
6 When prompted to reprocess the invoice through the Accounting Interface, click on Yes.

AccellosOne 3PL will create a negative charge in CRIN for the reversed charge. For example, if you reverse a bill of lading charge of $20 dated June 1, AccellosOne 3PL will create a bill of lading charge of 
-$20 dated with the current date.
7 Click on Exit to exit.

### CANCELING THE REVERSAL OF A CHARGE <a id="canceling-the-reversal-of-a-charge"></a>

When you cancel the reversal of a charge, AccellosOne 3PL creates a positive charge offsetting the negative charge created when you reversed the original charge.
1 Enter CRIN.
2 Retrieve the invoice containing the reversed charge(s) that you wish to cancel.
3 Select the reversed charge(s) that you wish to cancel and click on Save.
AccellosOne 3PL will create a positive charge offsetting the negative charge created when you reversed the charge.
4 Click on Exit to exit.

### Allocating Costs to an Invoice <a id="allocating-costs-to-an-invoice"></a>

You can manually allocate a cost against an invoice. The cost could for third party services, internal costs or for whatever else you determine is relevant. The cost is entered against an invoice and is reported to the financial system through the Daily Register Update.
You set up your costs in CHAR as normal charge codes with GL account codes. You activate costing by setting the Cost Entry flag in DBIP (Depositor Billing Profile) to Yes. When costing is activated, you must enter at least one cost for each invoice in CTIN (Cost Tracking in Invoice). Invoices without a cost cannot be added to the daily invoice register.
DBIP screen showing Cost Entry = Yes
1 Enter CTIN.

2 Click on Enter Criteria.
3 Key in your invoice number and click on Execute Query.
4 Click on Charge Block.
5 Click on Create Record.
6 Enter your cost (charge code) in the normal manner.
CTIN screen showing cost for BOL printing
7 When you finish entering your cost(s), click on Return to Main and Master Block.
8 Click on Return to Main and Exit to exit.
9 Click on Release Invoice to DLRE.
