---
title: "Expedição (Outbound)"
description: "Saída de mercadoria: digitação de pedidos, confirmação e documentos de embarque."
layout: default
---

# Expedição (Outbound)

Saída de mercadoria: digitação de pedidos, confirmação e documentos de embarque.

**Fluxo principal:** `ENOR -> ASOR (aloca) -> CHOF (confirma) -> PROR/PROM (imprime)`

> Fonte: manuais D do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Shipping <a id="shipping"></a>

*Manual D — Operations 1*

### Overview of Shipping <a id="overview-of-shipping"></a>

The following is a simplified model of the shipping tasks that are involved in processing each order.
PICK
 ALLOCATE
Select and assign the locations from which the product will be picked.
PRODUCE PICKING 
INSTRUCTIONS AND OTHER
 SHIPPING DOCUMENTS
SHIP
RECEIVE 
THE
ORDER
RECORD THE 
PRODUCT DETAILS

### SHIPPING PROGRAMS <a id="shipping-programs"></a>

Several warehouse tasks are involved in the process of filling order requests and shipping out the inventory. 
Shipping is also referred to as the outbound process. The outline below lists the shipping tasks and their main functions:
ENOR is the first flow in the shipping process. You enter the details that apply to the entire order in the Header Block and you enter the details for each separate item of the shipment in the Line Block. 
You can also add any outbound charges and special details that may apply to this order in the Optional Blocks. 
You time-stamp and advance each flow process for the entire order.
You Execute Confirm. This command accepts the details for the entire order into the system and updates inventory data accordingly. 
In the program CHOF, you have already time-stamped and advanced all of the order’s flow processes — up to COOR (Confirm Order).
You Execute Confirm for the last flow — COOR (Confirm Order) in the program COOL. You do this only for the individual order lines that you specify. The system updates inventory data accordingly.
After each flow, you print any document(s) attached to that particular flow. The system will do this for the order(s) that you specify.
Printing of the designated picking document will allocate the order — that is, assign the product and the location(s) to be used for picking.
You use PROR to print the document(s) attached to a specific flow. The system will do this for all order numbers that are currently in the system and that are at the same stage in their flow process.
If necessary, you cancel the requirement to print an attached shipping document. This advances the system to the next flow process without actually printing the document. 
If the document has been printed before, you can set REOR to reprint the attached order document.
ENOR
Enter Order
CHOF
Time-Stamp and Confirm 
COOL
Confirm Orders - One 
PROM
Print Shipping 
PROR
Print Shipping 
REOR
Requeue Order 

### SHIPPING OPERATIONS PROCESS <a id="shipping-operations-process"></a>

You return to CHOF/COOL and PROM/PROR as many times as necessary until all flow processes and all attached shipping documents are processed.
CHOF or COOL
Flow Process 2
Flow Process 1
Flow Process 3
Execute Confirm
ENOR
CHOF or COOL
CHOF or COOL
PR0M or PROR
Need to print document?
PROM or PROR
Need to print document?
Yes
PROM or PROR
Need to print document?
No
Yes
No
No
Yes

### Entering a Regular (R-Type) Order <a id="entering-a-regular-r-type-order"></a>

You begin the shipping process in AccellosOne 3PL by entering an order record in the program ENOR (Enter 
Order). In ENOR you record details of the product that the warehouse is shipping out to a specific consignee (the receiver of the goods). 

### OVERVIEW <a id="overview"></a>

The ENOR program consists of the following sections:
 Order Block (also called the Header or Master Block)
 Remarks Block
 Carrier Block
 Accessorial Charges Block
 Line Block
The Header Block and Line Block are mandatory. The other blocks are optional.
The record created in ENOR has general information that applies to the whole shipment and specific information about the individual items that make up the shipment. To capture this in AccellosOne 3PL, ENOR has a Header Block and a Line Block. General information that applies to the whole transaction is entered in the 
Header Block. Particular information about each item is entered separately in the Line Block.
The following procedure will lead you through the ENOR program, field by field. You will obtain most of the information for completing the fields from the order request. Other fields will fill in automatically (populate) 
with data that was preset in other AccellosOne 3PL programs.
Some fields are mandatory. The system will not allow you to continue until you enter data into a mandatory field. Other fields are optional and the system will allow you to bypass them by pressing Enter without entering any information.
Certain fields have pick lists, which display the available options for that field. This is helpful when you do not remember the code that you need. 
There are various Header Block order types. R (Regular) is the usual type that you use when the product is available for filling the order. There are other Header Block order types for special circumstances when the ordered product is not available.
The procedure below is for an order that is R (Regular) type in the Header Block.

### ENTERING HEADER INFORMATION IN ENOR <a id="entering-header-information-in-enor"></a>

The Header Block is also called the Master Block. Data entered in the Header Block applies to all line records that will be created in the Line Block. 
1 Key in ENOR at the Enter Selection Prompt. Press Enter and the system displays the Enter Orders (Outbounds) screen. The program is in the Create Record mode.
2 Leave the Order Number field blank. The system will automatically generate a number later.
3 For a normal order type, leave the Order Type field with the R (Regular) that is generated by the system. 
4 The cursor is in the Customer Code field. Enter the code of the product owner and press Enter. 
If you do not know the code, press F10 and then click on Execute Query to display the pick list. Use the pointer (arrow) keys to move the cursor next to the applicable code. Click on Select Code. 

5 The system automatically fills in the next seven customer-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 

ENOR screen
6 Enter the Consignee Code of whomever will be receiving the product and press Enter. If you do not know the code, use the pick list. 
7 The system automatically fills in the next seven consignee-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. If you used a forward slash to bypass the Consignee 
Code field, see the information note above.
8 The system either bypasses or automatically populates the Priority field. Priorities determine the printing sequence of this order’s documents over other orders that have documents in the printing queue at the same time (auto-printed documents only) and whether this order’s product can be de-allocated and assigned to another order with a higher priority.
The system default is 5. If you need to change the default value, press F9 (Previous Field) until the cursor is in the Priority field. Key in the correct number and press Enter or use the pick list, if necessary.
NOTE If the Consignee Code that you need does not exist in the pick list and manual consignees are activated on your system, key in / (a forward slash) in the Consignee Code field and press Enter. Then, in the Name field, key in the actual name and press Enter. This will allow you to bypass these mandatory fields. Key in the 
Address 1, Address 2, Address 3, City, State/Province and ZIP Code fields as applicable or press Enter to bypass these optional fields.

9 The cursor is in the Sold To Code field, which refers to the party who will pay the product owner for the goods. The Consignee and the Sold to party may be different. For example, the head office of a department store chain will pay for the product but the product is being shipped to Store # 22. The head office is the Sold To and Store #22 is the Consignee.
If you do not need to capture Sold To information or if the Sold To and the Consignee are the same, key in S (for Same as Consignee).
If the Sold To and the Consignee are not the same, key in the Sold To Code and press Enter. If you do not know the code, use the pick list.
10 The system automatically fills in the next seven Sold To Code related fields: Name, Address 1, Address 
2, Address 3, City, State/Province and ZIP Code. If you used a forward slash to bypass the Sold To Code field, see the information note above.

ENOR screen
11 Press Enter to accept the default date as the order date. If a different order date is required, key in the correct date using the same date format as shown in the field and press Enter.
NOTE If the Sold To Code that you need is not in the pick list and manual Sold To’s are activated on your system, key in / (a forward slash) in the Sold To Code field and press Enter. Then, in the Name field, key in the actual name and press Enter. This will allow you to bypass these mandatory fields. Key in the Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code fields as applicable or press Enter to bypass these optional fields.
Order Date, To Ship 
Date and To Arrive 
Date fields

You can enter an order date that differs from the current system date by up to one month in the past or in the future.
12 If necessary, key in the order time based on a 24-hour clock (i.e. 14:00 for 2:00 p.m.) and press Enter. If the time is not required, press Enter to bypass the field. 
13 The default for the to ship date is the next working day based on the default date. If the default is correct as the date that the product is leaving the warehouse, press Enter. 
If you require a different to ship date, key in the correct date using the same date format as shown in the field and press Enter.
14 Key in the to ship time, if necessary, and press Enter. If the time is not required, press Enter to bypass the field.
15 The default for the to arrive date is the same as the to ship date. If the default is correct as the date that the product will arrive at its destination, press Enter. 
If you require a different to arrive date, key in the correct date using the same date format as shown in the field and press Enter.
16 Key in the to arrive time, if necessary, and press Enter. If the time is not required, press Enter to bypass the field.
17 If there is a number that references the order that you are creating, key it in the Customer Order Number field and press Enter. This is a free format field. If a reference number does not apply, press Enter to bypass the field. 
If you enter a customer order number that has already been used, you will be prompted to reuse it. Click on Yes to reuse or click on No to enter a new customer order number.
18 Key in the purchase order number that applies to this order and press Enter. This is a free format field. If a purchase order number is not used, press Enter to bypass the field.
If you enter a purchase order number that has already been used, you will be prompted to reuse it. Click on Yes to reuse or click on No to enter a new customer order number.
19 Enter the carrier code of the firm that will be transporting the product to the consignee and press Enter. If you do not know the code, use the pick list. 
If the pick list does not have a code set up for the required carrier and manual carriers are activated on your system, you can key in / and press Enter. Then key in the name of the carrier and press Enter. This option is referred to as a “manual carrier” because you, as the operator, keyed in the carrier name.
Note that the pick list has an “Unassigned” option if you do not know the carrier at this point in time.

ENOR screen
20 The system either bypasses or automatically populates the Logistics Management field depending on whether or not your system setup includes SmartFreight. If your system does include SmartFreight and if previous setups establish that the carrier for this order is a freight-type carrier, the system will automatically place this order into SmartFreight. 
21 Key in the load type code and press Enter. This is a mandatory field and must be completed. Use the code NA (Not Applicable) if this order does not involve a Load Type Code. If you do not know the code, use the pick list. 
The system automatically fills in the Description field of the Load Type Code.
If a carrier has not been assigned yet to deliver this order, select the unassigned option from the pick list

ENOR screen
22 The Freight Terms field refers to the type of freight charge payment that applies to the delivery of this order. 
Key in the applicable freight terms description and press Enter. This is a mandatory field and must be completed. Use the code NA (Not Applicable) if this order does not involve any freight charge payments. 
If you do not know the description, use the pick list to select it. 
23 If cash on delivery (COD) was chosen as the type of freight term for this order, the COD Amount field is mandatory. Key in the actual cash amount that is to be collected upon delivery of this order and press 
Enter. Do not use any monetary symbols.
If the freight term for this order is not cash on delivery, either press Enter to bypass the field or key in the amount that applies to the selected freight term. 
24 If the selected freight term requires the collection of payment upon delivery, the Payment Type field is mandatory. This field also uses the code description and not the code acronym (i.e. Post Dated Check and not PODS; Warehouse C.O.D. and not W.C.O.D.). 
Key in the code for the method of payment that will be used for the freight charges and press Enter. If you do not know the code, use the pick list.
If the freight term for this order does not require the collection of payment upon delivery, either press 
Enter to bypass the field or key in the amount that applies to the selected Freight Term.
25 The Message Code field will only apply if your company has standard messages that print on shipping documents. If this order requires a such a message to be printed on one of the shipping documents that is attached to this order, key in the appropriate code in the Message Code field. If you do not know the code, use the pick list. 
If your system does not have this option or if a message is not necessary, press Enter to bypass the field.
The Freight 
Terms field accepts the code description but not the code acronym. 
For example, it will accept “cash on delivery” but not “COD”.

The system automatically populates the Description field for the message code.
26 The default for the Remarks field is N (for No). If you do not need Header Block remarks to appear on the warehouse order form, press Enter to accept the default. 
If you do need Header Block remarks to appear on the warehouse order form, key in Y (for Yes) and press Enter. A block will appear later in the program to enter the remarks. 
27 There are four options to choose from in the Carrier Details field.
If your selection is N, press Enter to accept the default. If your selection is any of the other choices, key in the applicable letter and press Enter. 
28 Press Enter to bypass the Pallet Details field.
29 Press Enter twice to bypass the EDI Details and Accessorial Charges fields.
N (No) Use when you do not need to track carrier details 
E (Entry) Use to add carrier details during order entry. The Carrier 
Details Block will display later in ENOR. If your warehousing firm purchased the additional system printing option, the details will also print on the attached outbound document that was selected by your company.
C (Confirmation) Use to add carrier details during confirmation of the order. 
The Carrier Details Block will display during confirmation. If your warehousing firm purchased the additional system printing option, the details will also print on the attached outbound document that was selected by your company.
B (Both) Use to add carrier details twice — once during ENOR and again during confirmation of the order. The Carrier Details 
Block will display in ENOR and during confirmation. If your warehousing firm purchased the additional system printing option, the details will also print on the attached outbound document that was selected by your company.

ENOR screen
30 The Warehouse Code field is usually left blank. Press Enter to bypass the field. 
For further information on this field, refer to [Restricting Multiple Item Lines to a Common Warehouse](recebimento.html#restricting-multiple-item-lines-to-a-common-warehouse).
31 Press Enter to bypass the Material Handling Equipment Type Code field.
32 In the Extra Reference Number 1 and the Extra Reference Number 2 fields, key in the data defined by the customer and press Enter. 
If the customer does not require such reference data, press Enter to bypass each of the fields.
33 Press Enter to bypass the Distribution Type Code field.
34 If required, key in your account in the Parcel Shipping Account field and press Enter.
35 If you changed the default in any of the fields for Remarks, Carrier Details, EDI and Accessorial Charges, the corresponding blocks will display now on the screen in succession. 
Complete the applicable blocks by following the corresponding Optional Blocks procedures, which follow the Line Block procedure. Then return to the Line Block procedure listed directly below and complete it. 
If none of these optional blocks apply, proceed to the mandatory Line Block procedure directly below. 

### ENTERING LINE INFORMATION IN ENOR <a id="entering-line-information-in-enor"></a>

In the ENOR Line Block, you enter the details of the item that you will use to fill the order request. There are two ways of selecting and assigning the specific inventory that is to be used for filling the order that you are creating:
 you select the item by completing all of the inventory level fields 
 you allow the system to select the inventory entity through the allocation routine
If there are miscellaneous charges attached to this order, key in Y in the Accessorial Charges field.

If you wish to select the inventory yourself, use the R (Regular) Line Block type. Then complete all of the 
Inventory Level fields in the ENOR Line Block; for example, Item: ABC, Lot Number: 123 and Color: Blue. 
If you want the system to automatically select the inventory through the allocation routine, you use a P (Pending) Line Block type. You complete the Inventory Level 1 field and the system will allow you to bypass 
Inventory Level 2 and any other higher inventory level fields that apply to the item. 
For example, suppose you have an item setup that uses two inventory levels:
You key in the information in the Item field but you leave the Expiry Date field blank. Later, when you print the designated picking document, this will trigger the allocation routine. The allocation process will select the inventory with either the oldest or the most recent expiry date, depending on the First In, First Out/Last In, 
Last Out rules that are set up in your system. The system will populate the Expiry Date field in ENOR and show this date in the picking document.
The following table shows the differences between R-type and P-type lines.
Item (Inventory Level One)
Expiry Date (Inventory Level Two)
R-TYPE LINE P-TYPE LINE
Manual Allocation (you assign the inventory) Automatic Allocation (the system assigns the inventory through the allocation routine)
Inventory is reserved for that order and cannot be assigned to another order. 
Inventory is NOT reserved for that order; if both an Rtype and P-type order call for the same inventory entity and there is insufficient product to fill both orders, allocation will fill the R-type order first. Only then will any remaining units be assigned to the Ptype order.
Status of inventory in LOEN = “On Order”. Status of inventory in LOEN = “Available”.
Line type does not change after allocation. After allocation, P-type line becomes a R-type line.
If you do not enter your level 2 and higher values in 
ENOR, the system selects these values during order entry according to the options that you select in PIPR (Picking Profile). AccellosOne 3PL will create as many additional R-type lines as are required to fulfil the order quantity.
If you do not enter your level 2 and higher values in 
ENOR, the system selects these values during allocation — not order entry — according to your PIPR parameters. For example, you can enter your order today but your level 2 and higher values will be determined tomorrow when you run allocation.
If you enter the location in ENOR, no selection of location by ILOP (Item Location Profile) during allocation will occur.
You cannot enter the location in ENOR. During allocation, the system will select the locations according to your ILOP parameters.
Immediate information is provided in ENOR about an item’s availability.
No information is provided in ENOR about an item’s availability.

### ENTERING AN R-TYPE LINE <a id="entering-an-r-type-line"></a>

With R-type lines, you can enter all inventory levels if they are known, level 1 only or up to inventory level 2 or 
3. If you do not enter all inventory levels, AccellosOne 3PL will automatically select the inventory when you create a new line or exit ENOR. 
1 The system enters the Line Block in Create Record mode. Leave the Line field with the 1 that is generated by the system.

ENOR Line Block screen
2 If you want to select the product that is to be used in filling this order line, press Enter to accept the system-generated R (Regular) as the line type. 
Allocation may run faster because the inventory was selected in ENOR, but the full power of AccellosOne 
3PL to select the best possible inventory to pick will not be harnessed.
Allocation may run slower because any selection of inventory in ENOR was not final, but you will take full advantage of AccellosOne 3PL’s allocation routine to pick the best possible inventory based on receipt date, expiry date, product already in location and many other factors.
Inventory must be received and confirmed before you can place it on an order.
Inventory not yet received into the warehouse can be placed on an order.
Item substitution is not available. You can perform item substitution.
R-TYPE LINE P-TYPE LINE
This screen is ready to create a record for line 1 of this order.

3 If you need remarks to appear on the designated warehouse order form for this line item, key in Y (for 
Yes) in the Remark field and press Enter. 
Otherwise, press Enter to accept the N (for No) default.
4 If their completion is required, the cursor will enter the EDI, Charge, Warehouse Restriction, Customer 
Code and Hold Code fields. Otherwise, the system will skip over these fields. 
If the system skips over the field but you need to access it (for example, the Charge field), press F9 (Previous Field) the required number of times until the cursor is in the field. 
5 The system may skip over the Warehouse Restriction field leaving it blank. This means the field does not apply to this line and the system does not allow you access.
However, the cursor may enter the field and the Help Message Line indicates “Enter a warehouse restriction if required.” If picking of this item is to be restricted to a particular warehouse, key in the Warehouse 
Code and press Enter. If you do not know the code, use the pick list. 
If a restriction is not required, press Enter to bypass the field.
6 The Hold Code field applies to inventory entities that have a shippable hold code placed on them. 
If you wish to ship only product that has been placed on a specific hold, press F9 the required number of times until the cursor is in the Hold Code field. Key in the hold code that you wish to restrict the order line to and press Enter. If you do not know the code, use the pick list.
If the field is populated, this indicates that either this item or the location where the product has been stored has an automatic hold attached to it. Press Enter to accept the current code or use the pick list to select a new code. 
7 Key in the item code and press Enter. If you do not know the code, use the pick list. 
Note that item code is always Inventory Level 1.
8 Under the Item Code field, there can be — although none or not all may apply in your case — Inventory 
Level 2, Inventory Level 3 and Inventory Level 4. However, these fields will display with the correct terminology (for example, Lot Number, Production Date, Expiry Date, Pallet ID, etc.) that was preset for this customer. 
Complete all of the inventory level fields that display if you wish to select the product yourself. In Inventory Level 2, key in the code for this level and press Enter. If you do not know the code, use the pick list. 
Repeat for the other inventory levels, if applicable.
If you want the system to select the product that is to be shipped, enter the appropriate data up to the level that you want the system to select. For example, you need: 
Inventory Level 1 (Item) = One 
Inventory Level 2 (Lot) = 234 
Inventory Level 3 (Production Date) = oldest in stock
In order to allow the system to find and assign Item One, Lot 234 with the oldest production date, you would complete Inventory Level 1 and 2 but you would leave Inventory Level 3 blank. (The system would 

fill in the blank field after it has completed the allocation routine and has found the correct Production 
Date.)

ENOR screen
9 The system skips over the Alternate Description field either leaving it blank or populating it with preset data. 
10 In the Ordered Quantity field, key in the amount and the SKU that was ordered — the number of units that you expect to ship to the consignee. Press Enter.
You can key in the amount in any SKU that is valid for order entry. For example, if the item’s quantity breakdown is 100 cases per pallet, you can enter an amount of 1,010 cases as follows:
1010 CASES or 10PLT 10 CASES or 9PLT 110 CASES
Embedded spaces are allowed but not required. The total number of characters including blank spaces cannot exceed 20 characters.
NOTE When you select an inventory level in an inventory level pick list, you are selecting all inventory levels including the lowest inventory level. You cannot manually enter a value or select another value from a lower inventory level. For example, if you use the pick list for level 2 to select your lot number, you will be forced to select your pallet ID at the same time. As as result, you will not be able to access the level 3 field.
If you wish to leave certain inventory levels blank in the Line Block of ENOR, you must manually enter your values instead of selecting them from a pick list.

11 If there is enough inventory available, the system will populate the To Ship Quantity with the same amount as was entered in the Ordered Quantity field. Press Enter to accept the default entry.
If there is not enough inventory available, see the section “Shipping With Insufficient Inventory” in the 
Allocation Guide.
The system may now skip over the remaining fields and move you to the next Line Block record. If this occurs, proceed to step 19. 

ENOR screen showing the Line Block
12 The Quantity Breakdown field as completed by the system. This identifies the SKU that is used to track and bill this item. For example if the quantity breakdown field shows PLT: 50 (the largest SKU) and 
CASE: 1 (the smallest SKU), you read it as one pallet has 50 cases.
The system will only allow you to enter this field if the Variable Quantity Breakdown field was set to Y in the program ITEM for this product. If this product does have a variable quantity breakdown, key in the correct information and press Enter.
The system assumes that the amount ordered and the amount to be shipped will be the same.
For an R-type line, the system shows the quantity that is presently available for 

ENOR screen showing the Line Block
13 The system automatically calculates and fills in the item’s Weight Code, Unit Weight, Gross Weight and 
Net Weight.
F9 (Previous Field) will return you to any of these fields if you need to enter or change data in them. For instance, if the item has non-standard weights, you may be required to enter the Unit Weight.
14 The Location Code field assigns the location(s) from which the product is to be picked when filling this order. If you want the system to choose the location, leave the Location Code field blank. The allocation routine will assign the location according to the parameters set up in Item Location Profile (ILOP).
If you want to choose the location, 
If you wish to select the location from which this item is to be picked and . . . Then do the following . . .
You know the location Key in the location code of where the item is stored and press Enter. If you do not know the location code, use the pick list.
You do not know the location Press Enter to bypass the field. Once you do know the location, you can return to this order — as long as it has not been confirmed — and complete the location code field.
Weightrelated fields.
It may be necessary to enter the unit of an item that does not have a standard weight.

15 The system automatically completes the Warehouse Code field based on the location code entered in the previous field or based on a pre-set warehouse restriction. See [Understanding Warehouse Restrictions](recebimento.html#understanding-warehouse-restrictions) for further information.
16 The Remark, Accessorial and EDI blocks for this line will now appear on the screen for completion if you requested them above. If none of these blocks apply, proceed to the next step.
If you need to complete the Remarks Block and/or Accessorial Block, see the corresponding procedures in [Optional Blocks of ENOR](expedicao.html#optional-blocks-of-enor). 

ENOR screen
17 A new line displays for you to enter the next item line from the order documents. If a new line number does not display, click on Create Record.
This line involves product that has a shippable holdThe pick list will restrict your options. It will only display locations that have inventory with the selected shippable hold attached. 
If this line has to be picked from more than one location because there is not enough product in a single location
See [Assigning Multiple Locations to a Line Block Record](expedicao.html#assigning-multiple-locations-to-a-line-block-record).
If you wish to select the location from which this item is to be picked and . . . Then do the following . . .
Running total of the line details that have been entered up to this point. In this example, these details are for the totals of lines 1 and 2.
Current record counter.

Repeat the Line Block procedure for each line record (i.e., for each inventory entity). The upper right hand corner of the screen displays a current record counter for your reference. The Line Block also displays a running total of some key details for the line entries that have been entered up to this point.
When you have finished entering all of the order lines, click on Return to Main and Master Block. 
18 You are now taken back to the beginning of ENOR where the system shows the order number that it has generated.
19 If you wish to enter another order, click on Create Record. If you wish to exit the ENOR program, click on 
Exit.

### ENTERING A P-TYPE LINE <a id="entering-a-p-type-line"></a>

The procedure for entering a P-type line is identical to the procedure for entering an R-type line with two exceptions. With P-type lines:
 you leave the inventory levels that you want the system to select blank
 you cannot specify a location
The Allow P-Type Lines in Order Entry flag in COMP (Company Parameters Block) must be set to Y for Yes before you can enter P-type lines.

ENOR screen showing the Line Block
When your run allocation, the allocation routine will select the inventory and location for the P-type line and then change its type to R for Regular.

### QUERYING ON INVENTORY LEVELS IN ENOR <a id="querying-on-inventory-levels-in-enor"></a>

In the Line Block, you can query on any inventory level to see how much of that product is available. For example, the screen capture below has an inventory setup of two levels: 
With a P-type line, Show 
Totals displays as an option.
To view the amounts that are currently available, on hand and on order for the inventory entity, click on Show 
Totals.

Inventory Level 1 = Item 
Inventory Level 2 = Lot Number

ENOR screen showing Line Block
TO VIEW ALL ITEMS (INVENTORY LEVEL 1) FOR THIS CUSTOMER 
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 With your cursor in the blank Inventory Level 1 (Item) field, press F10 and then click on Execute Query. 
This will display the pick list with all items for this customer.
4 Select the Inventory Level 1 entity that you need or click on Cancel to exit the pick list.
5 Continue with the Line Block in the normal manner.

ENOR screen showing the pick list for inventory level 1
In ENOR, you can query on the inventory levels to view their entities and available quantities.

TO VIEW ALL LOT NUMBERS (INVENTORY LEVEL 2) FOR THIS CUSTOMER 
AND ITEM
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 Key in Inventory Level 1 (Item) and press Enter. If you do not know the code, use the pick list.
4 With your cursor in the blank Inventory Level 2 field (lot number, in this example), press F10 and then click on Execute Query. This will display the pick list with all Inventory Level 1 and Inventory Level 2 for this customer.

ENOR screen showing the pick list for inventory level 2
5 Select the Inventory Level 2 entity that you need or click on Cancel to exit the pick list.
6 Continue with the Line Block in the normal manner.
TO VIEW A SPECIFIC LOT NUMBER (INVENTORY LEVEL 2) FOR THIS 
CUSTOMER AND ITEM
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 Key in inventory level 1 (Item) and press Enter. If you do not know the code, use the pick list.
4 Key in the inventory level 2 data (Lot Number, in this example.) With your cursor in this same field, press 
F10 and then click on Execute Query. This will display the pick list with only the details for the specific 
Inventory Level 2 that you queried on.
This pick list displays all lot numbers (inventory level 2) for the customer and item selected in ENOR.

ENOR Line Block screen
5 Select the specific entity or click on Cancel to exit the pick list.
6 Continue with the Line Block in the normal manner.

### ASSIGNING MULTIPLE LOCATIONS TO A LINE BLOCK RECORD <a id="assigning-multiple-locations-to-a-line-block-record"></a>

It may happen that you need more units of an item than there is available in a single location. For example, the order line is for 20 cases and there are 15 cases in Location 1 and 5 cases in Location 2. If this occurs, use the Location Block. This block allows you to record picking from more than one location for an individual 
Line Block record.
1 Complete the ENOR Header Block. 
Querying on all inventory levels.
This pick list displays the specific lot number for the customer and item selected in ENOR.

2 Complete the Line Block fields until you reach the Location Code field.
3 Press Enter to bypass the Location Code field.
4 Click on Return to Main.
5 Click on Location Block. The Location Block appears on the screen and the system fills in the location line number.

ENOR screen showing the Location Block
6 Key in the location code from which the first portion of the product will be picked and press Enter. If you do not know the code, use the pick list. 
7 The system populates the Warehouse Code field and skips to the next field.
8 Key in the quantity that will be picked from this location and press Enter.
Location and amount that will be picked from the first location.

ENOR screen showing the Location Block
9 Check the Location Proof Box, which indicates the following information:
When the balance indicates 0, it means that all units have had picking locations assigned. 
Total Total units ordered and that need to be picked from inventory locations to fill this order line
Entered Number of units that have had picking locations assigned up to this point
Remaining Number of remaining units that still need to have picking locations assigned 
Location 
Proof box

ENOR screen showing the Location Block
10 In Line 2 of the Location Block, key in the location code and quantity for the next portion of the product that will be picked from this second location.
Repeat until the Location Proof Balance is zero. 
11 Click on Line Block.
12 If you need to enter another line in the Line Block, click on Create Record. To exit ENOR click on Master 
Block and Exit.

### OPTIONAL BLOCKS OF ENOR <a id="optional-blocks-of-enor"></a>

The Optional Blocks are the Remark, Carrier, EDI and Accessorial Charges Blocks. If you requested any of these in the Header Block of ENOR, they will display now in succession. Follow the procedures below to complete them.
REMARKS BLOCK
The Remarks Block will appear on the screen if the Remarks field in either the Header Block or the Line Block is set to Y (for Yes). A remark can be any useful message that will appear on the order. 
1 Key in your remarks. 
NOTE No individual “word” can exceed 40 characters and no line can exceed 45 characters.
Location 
Proof box must be zero or the system will not allow you to confirm the order later.

ENOR screen showing the Remarks Block
2 When you finish entering all remarks for this order, click on Return.
3 If you are in create record mode, the next optional block or the Line Block appears on the screen for completion. Continue to process the order in the usual manner.
EXTENDED REMARKS BLOCK
If activated in COMP (Company Code), the Extended Remarks screen allows you to attach one or more messages to a given order document. The message can be either a predefined message in MESS or a freetext message that you enter manually. Unlike the messages in DPME (Depositor Print Messages), these messages print for a specific order only.
For example, if you select Customer Message and BF (Blast Freezing) as your message code, the text “Customer Message” and “BF (Blast Freezing)” will print on your selected document.
1 Select the checkboxes that apply to your remarks: Customer Message, Consignee Message, Carrier 
Message, RF Picking/Voice Message.
2 If required, select your document from the Document Code pick list.
NOTE Adding the message to an actual document such as a bill of lading or receipt tally may require custom programming by HighJump.

3 Do one of the following:
Extended Remarks screen
4 Click on Save.
5 Click on Exit.
CARRIER BLOCK
The Carrier Block will appear on the screen if the Carrier Details field in the Header Block is set to E (Entry) or 
B (Both). It records data concerning the transportation vehicle and the driver that picks up the product from the warehouse. This information is important for reference purposes. 
You can also capture your pallet in and pallet out quantities. Unlike pallets entered in the Pallet Block, pallets entered in the Carrier Block are not assigned a pallet type or an account and are not tracked in LOPC (Look 
Up Pallet Control).
1 When you enter the Carrier Block, it is in the Create Record mode. Key in the driver code and press 
Enter. If you do not know the code, use the pick list. The system automatically fills in the Name field.
If the driver’s name is not in the pick list, key in / and press Enter. Then enter the driver’s name in the 
Name field.
2 Enter the Power Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
3 Enter the Carry Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
4 Enter the Vessel Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
If you are using a predefined message:
If you are entering a free-text message:
a) Select your message code from the Message Code pick list.
a) Key in a free-text message in the 
Message Text field.

5 Enter the Voyage Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
6 Enter the Seal 1 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
7 Repeat the above step for seal number 2.

ENOR screen showing the Carrier Block
8 Enter the temperature reading for the front, middle and back of the inside of the transportation vehicle, if applicable, and press Enter. If it does not apply, press Enter to bypass the three fields.
9 In the Setting field, if applicable, key in the temperature that the transportation vehicle’s thermostat control is set at and press Enter. If it does not apply, press Enter to bypass the field.
10 In the Ambient field, key in the temperature reading outside of the transportation vehicle, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
11 If required, key in your pallet in and/or pallet out quantities in the fields of the same name and press 
Enter.
12 When you finish, click on Return to Main. The next optional block or the Line Block appears on the screen for completion.
NOTE If your warehousing firm purchased the special printing option, information from the Carrier Block fields will print on the shipping document(s) that was selected by your warehousing firm.

### Entering a Manual Order in MAOE <a id="entering-a-manual-order-in-maoe"></a>

You can enter manual orders in MAOE. A manual order is a type of quick entry order restricted to P-type order lines consisting of just the item code and order quantity. Quick entry orders in MAOE are designed to speed up order line creation by eliminating the need to enter level 2/3/4 values, hold codes, a shelf life, etc. 
1 Enter MAOE.
MAOE screen
2 Click on New .
3 Enter your order header in the normal manner.
4 When the Manual Order Entry screen displays, select Pending from the Type dropdown list and press 
Enter.
5 Key in your item code or select it from the pick list.
6 Key in your order quantity and press Enter. 
MAOE screen
7 Repeat the above three steps for any additional order lines that you wish to enter.
8 When you finish entering your order lines, click on Process Order .
NOTE If you wish to edit an order that you created in MAOE, you must do so in 
ENOR. You cannot edit quick entry orders in MAOE.

9 Click on Exit to exit.

### Modifying an Order <a id="modifying-an-order"></a>

You can access and modify orders in ENOR as long as they have not been confirmed. It is possible to change data in both the Header Block and the Line Block.
You can check whether or not an order has been confirmed in the program LOOR (Look Up Orders). This program has a Status field. An order that has been confirmed will display as “Confirm Order…” in the LOOR 
Status field.

### MODIFYING HEADER BLOCK DATA <a id="modifying-header-block-data"></a>

If you modify an order’s consignee and if that consignee has a workflow profile that differs from the customer’s workflow profile, AccellosOne 3PL will use the order’s original workflow profile, not the new workflow profile.
1 Enter ENOR. The program is in Create Record mode.
2 Click on Enter Criteria.
3 Key in the system-generated number of the order you want to modify. 

ENOR screen showing the method for calling up an unconfirmed order
4 Click on Execute Query. The order will display on your screen.
Key in the number of the unconfirmed order that needs to be modified.
Click on Execute 
Query.

5 Press Enter to put the system in Modify Record mode.

ENOR screen showing Modify Record mode
6 Press Enter the required number of times until your cursor is in the field that you want to modify. Delete the existing data or press F11 (Clear Field).
7 Key in the new data and press Enter.
8 If you need to make additional changes to other Header Block fields, repeat steps 6 and 7 until all of the necessary changes are entered.
9 If you need to make changes to data in the Line Block, click on Line Block and follow the procedure below. 
When you have finished entering all necessary changes, click on Return to Main and Exit to exit ENOR.

### MODIFYING LINE BLOCK DATA <a id="modifying-line-block-data"></a>

The data that you can modify in the Line Block depends upon the order line type. If the line type is P for 
Pending, you can modify any field. If, on the other hand, the line type is R for Regular, you can modify the remarks, accessorial charges and locations only; if you wish to change the ordered quantity or inventory levels, you must delete the entire line. See [Deleting an Entire Line Block Record](expedicao.html#deleting-an-entire-line-block-record).
1 Enter ENOR. click on Enter Criteria. 
2 Key in the system-generated number of the order you want to modify. click on Execute Query. The order will display on your screen. 
3 Click on Line Block. 
4 If this order has more than one Line Block record, key in the number of the Line Block record that you wish to change and press Enter or click on Execute Query. If you do not know the line number, use your 
Press Enter until your cursor is in the field that needs to be changed.

up and down arrow keys to scroll through the Line Block records until you find the line needing modification.

ENOR Line Block screen showing the details for the Line 2 record
5 Press Enter until your cursor is positioned in the field that you wish to modify. Then press F11 (Clear Field and key in the new data and press Enter.
6 Click on Master Block. Repeat steps 6 and 7 if you need to change any other Line Block records for this order or click on Exit to exit the program.
CREATING A NEW ORDER LINE
If you need to add a new line to an order that has already been created but which has not yet been confirmed, follow the procedure below.
1 Enter ENOR. Click on Enter Criteria. 
2 Key in the system-generated number of the order you want to modify. click on Execute Query. The order will display on your screen. 
3 Click on Line Block. 
4 Click on Create Record.
5 Complete the Line Block in the normal manner.
6 When you finish entering your line, click on Return to Main and Master Block. Then click on Exit to exit the program.
Enter the line number of the line that you need to modify.

### MODIFYING LOCATION BLOCK DATA <a id="modifying-location-block-data"></a>

The following procedure applies to all types of Line Block records except for U (Unknown), which always allows you to open the order and fill in missing data as long as it has not been confirmed.
1 Enter ENOR. Click on Enter Criteria. Key in the system-generated number of the order that you want to modify. Click on Execute Query. The order will display on your screen. 
2 Click on Line Block. 
3 If this order has more than one Line Block record, key in the number of the Line Block record that you wish to change and press Enter. If this number is not known, use the up and down arrow keys to scroll through the Line Block records until you find the one needing modification.
4 Click on Location Block.
5 Press Enter. You are now in Modify Record mode.

ENOR Line Block screen showing the Location Block
6 Use the up and down arrow keys to move the cursor next to the location line that you need to modify.
7 Press Enter the required number of times until the cursor is in the field that you need to modify. Delete the previous data or press F11 (Clear Field). Key in the new data and press Enter or use the pick list to select the correct data.
Repeat this step if it is necessary to modify other Location Block lines.
8 When you have finished making all necessary changes to the Line Block, click on Line Block. If you need to create a new line, click on Create Record. 
9 When you need to exit ENOR, click on Master Block and Exit to exit.
Use your arrow keys to move the cursor next to the line that you need to modify.
Press Enter the required number of times to move the cursor to the field that you need to modify.

### MODIFYING OPTIONAL BLOCKS DATA <a id="modifying-optional-blocks-data"></a>

The procedure for modifying the Remarks, Carrier Details and Accessorial Charges blocks is the same. The following procedure uses the Remarks Block as an example of the procedure.
1 Enter ENOR. Click on Enter Criteria. Key in the system-generated number of the order that you want to modify. Click on Execute Query. The order will display on your screen. 

ENOR Header Block showing how to access the Optional Blocks
2 In the Header Block, press Enter until the cursor is positioned on the Y of the Remarks field.
3 Click on Remarks.
Place the cursor in the field of the optional block that you need to modify.
Then press the corresponding button.

ENOR Remarks Block screen
4 Delete the existing data and key in the new remark.
5 When you finish changing your remark, Click on Return to exit the Remarks Block. Then click on Return to Main and Exit to exit ENOR.

### UPDATING THE CARRIER DETAILS IN UOCP <a id="updating-the-carrier-details-in-uocp"></a>

You can update an order’s carrier and/or carrier details in UOCP (Update Order Carrier/Pallet) without entering ENOR.
1 Enter UOCP.
UOCP screen

2 Do one of the following:
UOCP screen showing a range of orders
3 If your query retrieved a range of orders, use your arrow keys to select the order whose carrier details you wish to update.
4 Do one of the following:
If you wish to update a specific order:
If you wish to update a range of orders:
a) Click on Create Record.
b) Key in your order number and press Enter.
c) Click on Return to Main.
a) Click on Query Block.
b) Key in your search criteria and click on Execute Query.
If you wish to update carrier only:
If you wish to update the carrier details:
a) Click on Carrier Update Block. a) Press Enter to position your cursor in the Carrier Details field.
b) Click on Carrier Details.
c) Proceed to step 8.

UOCP screen showing Carrier Update Block
5 Key in your new carrier code and press Enter or select your carrier code from the pick list.
6 Click on Process Carrier Update.
7 Click on Exit.
UOCP screen showing Carrier Details
8 Proceed to enter or update your carrier details.
9 When you finish entering or updating your carrier details, click on Return to Main.
10 Click on Return to Main again and then on Exit.

### Deleting an Order <a id="deleting-an-order"></a>

Orders may need to be deleted due to errors. You can delete orders in ENOR as long as they have not been confirmed.

In LOOR, you can view all details of deleted orders except for Line Block details. Deleted orders remain in 
LOOR until they are purged in the program Purge Orders, Receipts, Inventory (PURG).

### DELETING AN ENTIRE ORDER <a id="deleting-an-entire-order"></a>

1 Enter ENOR.
2 Click on Enter Criteria.
3 Key in the system-generated number of the order you want to delete.
4 Click on Execute Query. The order will display on your screen. 
5 Press Enter. You are now in Modify Record mode and the Delete button will appear at the bottom of the screen.

ENOR Header Block screen showing the Delete entire order option
6 Click on Delete. 
NOTE If product is in a staging location when you delete the order, you must do a manual relocation in RELO to return the product to the original non-staging location.
Delete displays as an option.

ENOR Header Block screen showing the Delete entire order option
7 A message block displays asking if you want to proceed with the deletion. Key in the letter of whichever of the following options applies to your situation and press Enter.
If you chose the R (Remarks Block), the order will be deleted and the Remarks Block will display. Key in the reason for deleting the order and press Enter. A message block appears indicating that the order is being deleted.
8 Click on Exit to exit the ENOR program.

### DELETING AN ENTIRE LINE BLOCK RECORD <a id="deleting-an-entire-line-block-record"></a>

There may be situations in which you need to delete an entire Line Block record from an unconfirmed order. 
For instance, this would be necessary under the following circumstances:
 to cancel the order for an item
 to change the Ordered Quantity or Weight Code fields on an order
 to change the inventory levels or locations
 to change the to ship quantity to zero
When you delete an order line record and then create a new order line, the line number of the new line depends on the number of lines on the order and the line number that you deleted. Refer to the following table for the renumbering rules in AccellosOne 3PL:
Y (Yes) If you wish to delete without entering any remarks as to why this order is being deleted.
N (No) If you do not want to delete this order.
R (Remarks) If you want to delete the order and include remarks explaining why this order is being deleted. The remarks will be saved with the deleted order.
If . . . then . . .
you delete the first line of an order with a single order line the next new line created will be line 1

1 Enter ENOR. Click on Return to Main then Enter Criteria. 
2 Key in the system-generated number of the order that you want to delete. Click on Execute Query and the order will display on your screen. 
3 Click on Line Block.
4 Key in the number of the Line Block record that you wish to delete and press Enter. If you do not know the line number, use your up and down arrow keys to scroll through the Line Block records until you find the one needing deletion. Then press Enter to switch to Modify Record mode.

ENOR Line Block screen showing the Delete entire line block option
5 Click on Delete. A message block displays asking if you want to proceed with the deletion. Click on the appropriate button.
you delete any line except the first line or the last line of an order with multiple order lines the next new line created will be the last line 
+ 1 you delete the last line of an order with multiple order linesthe next new line created will be line number of the line that you just deleted
Y (Yes) If you wish to proceed with the deletion.
N (No) If you do not want to delete this Line Block record.
If . . . then . . .
Delete displays as an option.

If you proceed with the deletion, the Line Block record that you were on will disappear and the previous line number and its details will be displayed.
6 If you wish to create a new line, click on Create Record and complete the Line Block in the usual manner. 
7 When you have finished making all necessary changes, click on Master Block to exit the Line Block. 
Then click on Exit to exit ENOR.

### DELETING LOCATION BLOCK DATA <a id="deleting-location-block-data"></a>

You use the following procedure to delete records from the Location Block. Records in the Location Block are composed of lines. When you delete in the Location Block, you delete the whole line record.
1 Enter ENOR.
2 Key in the order number.
3 Click on Line Block. 
4 Key in the line number of the record that you wish to modify and press Enter. If you do not know the number, use your up and down arrow keys to scroll through the Line Block records until you find the one that you need to change.
5 Click on Location Block.

ENOR screen showing the Location Block
6 Use the up and down arrow keys to move the cursor next to the line that you need to delete.
7 Press Enter until the Delete button appears. Then click on Delete.
8 If it is necessary to delete other lines in the Location Block, repeat steps 6 and 7.
Set the cursor at the beginning of the line that needs to be deleted.
Press Enter until the Delete button is available as an option.

9 When you have finished making all changes that are necessary, click on Master Block and Exit to exit 
ENOR.

### Order Header Types and Order Line Types <a id="order-header-types-and-order-line-types"></a>

There are various types of orders in AccellosOne 3PL. The normal order type is R (Regular). It indicates to the system that there is sufficient inventory available to fill the order. As you enter the items into an R type order, the system removes the ordered quantities from the warehouse inventory records and the changes show up in Look Up Entity Information (LOEN).
You use the other Header Block types in special circumstances.

### ORDER LINE TYPES <a id="order-line-types"></a>

The Line Block types allow you to control the product selection process based on the inventory level fields.
R (Regular) A regular order. Use when there is sufficient inventory available to fill the order. The system will remove the ordered quantities from inventory records and the changes will show in LOEN.
T (Transfer) Use when you need to transfer product from one warehouse customer to another. See [Transfer Orders](expedicao.html#transfer-orders) for further information.
I (Inspection) Use when you need to retrieve product from inventory for a government inspection. See [Inspection Orders](expedicao.html#inspection-orders) for further information.
K (Kit) Refer to the Kitting section of the Operations 2 Guide for further information on kit-type orders.
P (Pending) Sets the default for the Line Block Type
D (Distribution) Use when you need to cross-dock and ship an item at the same time. See [Distribution Orders](expedicao.html#distribution-orders) for further information.
R (Regular) Use when you wish to select the inventory levels yourself. You must know all of the inventory levels and there must be sufficient inventory available to fill the order request. The system will remove the product that is selected in an R type line from the warehouse inventory records. The change will display in LOEN.

### Looking Up Orders in LOOR <a id="looking-up-orders-in-loor"></a>

The program Look Up Orders (LOOR) allows you to view all orders that have been entered into AccellosOne 
3PL and that have not been purged. In LOOR, it is possible to view orders of any status — whether entered, confirmed or deleted. 
In LOOR, you can see all of an order’s details. The Status field shows the last outbound flow process that was completed for this order so you know where you are in the flow process sequence. LOOR also indicates whether or not there are outstanding documents to print for this order. 
P (Pending) Use when you want the allocation routine to select the inventory levels. The allocation routine will select the product based on the parameters that are preset in Picking Profile (PIPR).
K (Kit) Refer to the Kitting section of the Operations 2 Guide for further information on kit-type orders.
U (Unknown) Used for reserve logic customers only. See the Allocation Guide for further information.
W (Weight) Used to allocate product by weight. See the Allocation Guide for further information.

LOOR screen showing the Order Block details of order number 1893
LOOR consists of the following sections:
 Order Block (Header Block)
 Time-Stamping Block
 CRM Block
 Line Block
 Optional Detail Blocks (if applicable)
The following procedure allows you to view the details of an order in the various blocks of LOOR. An explanation of the LOOR fields and the data that they contain follows this procedure.
1 Enter LOOR. You are in the Enter Criteria Mode.
2 Do one of the following:
3 When you finish entering your criteria, click on Execute Query.
The Order Block details display for you to view.
4 Click on Time Block. The order’s time-stamping details display for you to consult.
5 Click on CRM Block.
6 Click on CRM / Manual Block.
If you wish to view a specific order: If you wish to view all orders:
If you wish to view orders that meet specific criteria:
a) Key in your order number. a) Proceed to next step. a) Enter your selection criteria in the corresponding field(s).
Order’s status in the flow process sequence.
Next document in the flow process sequence that needs to be printed.

7 Click on Master Block and then Line Block. The Line Block details display for you to view. Use your up and down arrow keys to move from one Line Block record to another.
8 Click on Master Block.

LOOR screen showing the Optional Blocks fields
9 Check the fields that apply to the optional blocks. If anything other than N (for No) has been entered in any of these fields, there are details. Press Enter until the cursor is in the optional block field that you wish to view. Then click on the appropriate button and the details of the optional block will display. 
10 Click on Return to exit the optional block. 
11 If you want to view another order’s details, click on Enter Criteria and key in the selection criteria for the next order that you wish to view.
12 When you have finished viewing the details, click on Exit. 

### ORDER BLOCK <a id="order-block"></a>

The LOOR Order Block contains basically the same information as the original ENOR record. It does, however, have some extra fields as described below: 
If anything other than 
No displays next to any of the optional blocks fields, there are details. Move your cursor to the field and click on the appropriate button for that field.

LOOR screen showing the Order Block details for order number 1830
FIELD DESCRIPTIONS
Status The latest flow process that has been completed for the order. The field also indicates the date and time that the flow was processed. Also displays if the order has been deleted. (The flow processes and their sequence were defined in DIFP.)
Transfer Receipt Number The corresponding order number if this is a transfer order type.
On Load(s) The order’s load number for loads created in SELO (Set Up Load). 
On External Load(s) The order’s load number for loads created in an external system such as 
Freight Logix. 
Back Order Reference If there was not enough product to fill the order and your system is set up to allow a back order for this product, this is the corresponding back order number.
If the system had to create more than one back order, the number range is provided, for example Back Order Ref: 56 <…> 69 indicates that the back orders created are numbers 56 to 69.

Freight Term The order’s freight terms code; for example, COD, collect, prepaid, etc.
Warehouse Code The warehouse that the order lines are restricted to. Only product in this warehouse can be allocated to the order lines.
Parcel Shipping Account The parcel shipping account (Canada Post, DHL, FedEx, etc.) for the order.
Document Status Indicates if there are any order documents that need to be printed for this order. Names the next document that requires printing according to the flow process sequence. 
Remarks and Carrier 
Details
Y = Yes
N = No
B = Both
C = Confirmed
E = Entry
If Y or E is displayed next to any of these fields, there are details entered in that block. To view the details, press Enter until the cursor is in the optional field that you want to view. Click on Return and the optional block details will display.
Quick Response Refer to the Quick Response Labels section in the Operations 2 Guide.
Order Date The date entered in the Order Date field of ENOR; the date when the order was created.
Shipped Date The date entered in the Ship Date field of CHOF (Time-Stamp and Confirm 
Orders). If you do not enter a date, the system will use the date that the order was confirmed in CHOF. 
Location Status Indicates whether all of the order’s lines have been assigned a location yet (Entered) or whether they are still unassigned (Missing). 
Shipped Weight Only available for confirmed orders
Refers to weights recorded on outbound labels. 
Pallets/Pieces Shipped Only available for confirmed orders
The total number of pallets/pieces shipped.
Total Units The total number of units for all of this order’s Line Block records. This is the total number of units entered in the To Ship field of the Line Block.
FIELD DESCRIPTIONS

### TIME-STAMPING BLOCK <a id="time-stamping-block"></a>

The Time-Stamping Block displays the details of the flow processes that have been completed up to this point for this order. If there is a document attached to a flow and this document has been printed, you can click on the View icon to see a PDF version of the document.
If the Appointment Remarks button is enabled, you can look up remarks entered in APPL (Appointment 
Planner) for the appointment’s order.

LOOR screen showing the Time-Stamping Block
Gross Weight The total gross weight of all the lines added together. 
Net Weight The total net weight of all the lines added together.
Load Type Code The order’s load type.
Reference Number 1/2 The order’s reference number 1/2 information.
Wave Number The order’s wave number (if any).
FIELD DESCRIPTIONS
Date The date when the flow displayed in the Flow Process column was performed.
Time The time when the flow displayed in the Flow Process column was performed.
FIELD DESCRIPTIONS

### LINE BLOCK <a id="line-block"></a>

The LOOR Line Block shows basically the same fields and details that appear in the original order’s ENOR 
Line Block. There are a few differences, however, which are noted below. 

LOOR screen showing the Line Block
This Shipped Date field is blank if the entire order has not been confirmed in Time-Stamp and Confirm Orders (CHOF) or the order line has not been confirmed individually in Confirm Orders - Lines (COOL). If the entire order was confirmed in CHOF, then all of the order’s Line Block records will have the same shipped date. This date is the same as in the Ship Date field of CHOF when the order was confirmed.
Flow Process The Flow Process column lists all of the flow processes that have been performed for this order at the time of viewing.
If the view icon is highlighted, you can click on the icon to view or print the document in PDF format.
If the e-File icon is highlighted, you can click on the icon to view and print the e-File or Signature Capture document.
Operator The operator who advanced the flow process.
FIELD DESCRIPTIONS
The date on which this line was confirmed.

If only individual lines of the order were confirmed in COOL, then the confirmed lines will display a date in the 
Shipped Date field. This will be the same as in the Ship Date field of COOL when the line was confirmed. The order lines that have not yet been confirmed, will have a blank Shipped Date field.

### OPTIONAL BLOCKS <a id="optional-blocks"></a>

The LOOR Optional Blocks show the same fields and details that appear in the original order’s ENOR 

### LOOKING UP AN ITEM SUMMARY <a id="looking-up-an-item-summary"></a>

The item summary command allows you to look up a summary of all order lines by item rather than by order line. That is to say, if you have multiple order lines for the same item, the lines will be consolidated into a single line.
1 Retrieve the order that you wish to look up.
2 Click on Item Summary.
LOOR screen showing item summary
3 When you finish looking up your item summary, click on Order Header and Exit to exit.

### CHANGING THE DEFAULT SORT SEQUENCE IN LOOR <a id="changing-the-default-sort-sequence-in-loor"></a>

The default sort sequence in LOOR is oldest order first, then second oldest order, followed by third oldest order, etc. You can change the default sort sequence to show the newest orders first by means of the Ctrl + A command.
1 Enter LOOR.
2 Query any order.
3 Press Ctrl + A. The message “Sequence will be descending” will display in the message area of your screen.
4 Perform your query. To retrieve all orders, leave all query fields blank.
NOTE Line Block details do not display for deleted orders.

AccellosOne 3PL will retrieve your orders in descending sequence; that is, newest order first, then second newest order, followed by third newest order, etc.

### Printing the Shipping Documents <a id="printing-the-shipping-documents"></a>

Orders may have shipping documents attached to them. Each document is attached to a specific flow process that was set up in DIFP. After a flow process is selected and time-stamped in CHOF, the documents that are attached to this flow need to be printed before the system allows you to proceed to the next flow. You print these documents individually in PROM (Print Shipping Documents - Specific) or in a batch print through 
PROR (Print Shipping Documents - All).
Your company may have a system that is set up to start the allocation procedure when you print a specific document. (Allocation is the process of selecting and assigning specific inventory to the order.) You will need to consider whether you want to allocate at this point in time before you proceed with printing of the document that triggers allocation. Your system administrator will advise you in this matter.

### PRINTING A DOCUMENT FOR SPECIFIC ORDERS IN PROM <a id="printing-a-document-for-specific-orders-in-prom"></a>

You use PROM (Print Shipping Documents - Specific) to print the same document for specific order numbers that have been entered in ENOR. You can print for a single specific order (for example, Order Number 5 needs its pick document printed) or for multiple specific orders (Order Numbers 1, 25 and 46 each need their pick document printed).
PROM consists of the following sections:
 Header Block
 Order Block
 Print Block
The Header Block in PROM lists all of the shipping documents. If you do not know which document to print at this point in the flow process sequence, you can check in LOOR. LOOR specifies the next document that needs to be printed in the field Document Status. 
The following example shows the steps required to process an order that has the outbound flow processes:
ENOR (Enter Order)
MANC (Manual Check)
PRBL (Print Bill of Lading)
COOR (Confirm Order)
FLOW 
PROCESS
ATTACHED 
DOCUMENTS REQUIRED ACTION
ENOR (Enter Order) Pick document a) Enter the order in ENOR
b) Print the Pick document in PROM
MANC (Manual Check) None Time stamp and confirm the MANC flow in CHOF 

1 Enter PROM.
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document that you need to print — the document attached to the flow that was most recently processed in CHOF.

PROM screen showing the Header and Order Blocks
3 Click on Order Block.
4 Click on Create Record.
5 Key in the number of the order whose attached document you need to print and press Enter.
If there are other ENOR orders that need this same document printed, key in each order number and press Enter.
PRBL (Print Bill of Lading)Bill of Lading a) Time stamp and confirm the PRBL flow in 
CHOF
b) Print the Bill of Lading in PROM
COOR (Confirm Order) None a) Time stamp and confirm the COOR flow in CHOF
b) Execute Confirm
FLOW 
PROCESS
ATTACHED 
DOCUMENTS REQUIRED ACTION
List of shipping documents
Place the cursor next to the document that needs to be printed.

PROM screen showing the Order Block
6 Click on Return to Main.
7 Click on Print Block.
8 Key in the code of the printer where this document is to print and press Enter. If you do not know the code, use the dropdown list.

PROM screen showing the Printer Block
9 Click Ok. The document will print and the system returns to the Main Menu.
The pick document that is attached to order numbers 4, 5 and 6 will be printed.
Printer Code
Click on OK to print.

### PRINTING A DOCUMENT FOR ALL ORDERS IN PROR <a id="printing-a-document-for-all-orders-in-pror"></a>

You use PROR (Print Order Documents - All) to print the same document for all orders that are at the same stage in their flow process sequence and that need this document printed. 
You can also use PROR to print the same document for all orders that meet common criteria and that are at the same stage in their flow process. In this case, you use the Query Block to enter the selection criteria that the orders have in common. The system will then call up only these orders. For example, if you need to print the Pick document for all orders that were entered on June 23rd for Customer A, you would fill in the date and the customer fields accordingly and instruct the system to execute the query for these restrictions.
PROR consists of the following sections:
 Header Block
 Query Restriction Block
 Order Block
 Print Block
1 Enter PROR.

PROR screen showing the Header and Order Blocks
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document that you need to print.
3 Click on Query Block.
List of shipping documents
Place the cursor next to the document that needs to be printed.

PROR screen showing the Query Restriction Block
4 Do one of the following:
If you wish to print the document selected in the Header Block for all orders that are at this step in their flow process sequence: 
If you wish to only print the selected document in the Header 
Block for orders that are at this step in their flow process sequence and that also have common criteria:
a) Click on Execute Query.
b) Proceed to step 7.
a) Key in the common selection criteria.
In the Header 
Block, a document has already been selected for printing. Now you are in the 
Query 
Restriction 
Block.

PROR screen showing the Order Block
5 Refer to the following table for further information on the common criteria that you can specify:
Completing this field . . .
will print the document selected in the 
Header Block for . . .
Customer Code all orders containing product belonging to this customer
Consignee Code all orders containing product to this consignee
Carrier Code all orders that were assigned this carrier for transporting product
Order Date - Start all orders that were created in ENOR with an Order Date starting from the date you specify here
Order Date - End all orders that were created in ENOR with an Order Date up to the date that you specify here
Ship Date - Start all orders that were shipped starting from the date that you specify here
Ship Date - End all orders that were shipped up to the date that you specify here
Arrive Date - Start all orders whose product is to arrive at the destination point starting from the date that you specify here
Arrive Date - End all orders whose product is to arrive at the destination point before the date that you specify here
If you click on Execute Query while you are in a blank Query 
Restriction Block, the system will display in the Order 
Block all orders that need the selected document printed according to their flow process sequence.

6 Click on Execute Query. The system moves to the Order Block where it displays all orders that meet the selection criteria that you specified.
7 Click on Print Block.
8 Key in the code of the printer where these documents are to print and press Enter. If you do not know the code, use the dropdown list.
9 Click on Ok. The documents will print and the system returns to the Main Menu.

### PRINTING A DOCUMENT FOR A SPECIFIC ORDER NUMBER <a id="printing-a-document-for-a-specific-order-number"></a>

You can also use PROR to produce the same result as PROM — that is, to print a shipping document for a specific order. If it is more convenient, you can use the following procedure rather than having to switch back and forth between the two programs.
1 In the Query Restriction Block, key in the specific order number in the Order Number field.
2 Click on Execute Query.
3 Click on Print Block.
4 Key in the printer code and press Enter.
Appointment Date - Start all orders that have an appointment date starting from the date that you specify here. This refers to appointments that are set up in the Appointment System — appointments scheduled at the warehouse doors for pick-up and delivery purposes.
Appointment Date - End all orders that have an appointment date up to the date that you specify here. This refers to appointments that are set up in the Appointment System — appointments scheduled at the warehouse doors for pickup and delivery purposes.
Type all orders that are of this ENOR Header Block order type
Priority all orders that have this priority code
Operator Code all orders that were entered by the operator that you specify here
Load Number the load number into which this order was grouped together for shipping
EDI Group Value the external group reference number used to group orders together for EDI tracking purposes. The field is automatically populated by EDI.
Batch Order Number the batch order number that you specify
Completing this field . . .
will print the document selected in the 
Header Block for . . .

5 Click on Ok. The document will print and the system returns to the Main Menu.

### Confirming an Order <a id="confirming-an-order"></a>

After you successfully enter an order in ENOR, the ordered product still appears in LOEN (Look Up Inventory) 
as both “On Hand” and “On Order.” You must now confirm the order. Then the system will remove the ordered product from the inventory records in LOEN. 
Confirming an order will perform all of the following tasks:
 adds the name of the operator who performed the confirmation
 adds the time and date when confirmation was performed
 removes the order’s product units from inventory records
 may rate the order with any applicable outbound charges, if the system is set up to rate automatically
You confirm an order in the program Time-Stamp and Confirm Orders (CHOF). In this program, the system individually time-stamps and advances each of the order’s outbound flow processes. Documents that are attached to these flow processes must also be printed in a separate program before the system allows you to proceed to the next flow. 

### TIME-STAMPING AND CONFIRMING ORDERS IN CHOF <a id="time-stamping-and-confirming-orders-in-chof"></a>

Before you can confirm an order in CHOF, the following conditions must be met:
 all documents have been printed for the order
 all locations have been entered for each order line
1 Enter CHOF.
2 Key in the order number and press Enter. The system fills in the other fields as applicable. 
If the system does not populate any of the fields in the bottom half of the screen and there is a message in the Help Message Line, see [Troubleshooting Help for Confirming an Order](expedicao.html#troubleshooting-help-for-confirming-an-order).
NOTE Advancing the flow of an order in CHOF is only required in a manual paperbased environment. In RF shipping, the flow is automatically advanced after each order line is picked, staged and loaded.

CHOF screen
3 The cursor moves to the Next Flow Process Code field. Press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select. If there is only one option in the pick list, it is a mandatory flow process. Click on Select.
If there is more than one option in the pick list, the last selection — the one with the highest sequence number — is mandatory. The other options are non-mandatory. You can bypass a non-mandatory process flow by not selecting it in the pick list. Use the up and down arrow keys to move the cursor next to the flow process that you wish to select. Then click on Select.
4 Click on Select Flow. The data in the CHOF screen blanks out as the system advances to the next flow in the flow process sequence.
5 Do one of the following:
If the Next Flow Process Code field is COOR (Confirm Order):
If the Next Flow Process Code field is NOT COOR (Confirm 
Order):
a) Go to step 6. a) Key in the order number again and press Enter. 
b) Click on Select Flow. The data in the CHOF screen blanks out as the system advances to the next flow. 
c) Repeat until the Next Flow Process Code field displays COOR.
The current flow has already been time-stamped and advanced.
The next flow process will be time-stamped and advanced when you click on 
Select Flow.

CHOF screen
6 When the Next Flow Process Code field displays COOR (Confirm Order), the system will populate the 
Ship Date field with the default date. Check that the default date is the correct date when the product for this order will be shipped. 
If you need a different date than the default, press Enter until the cursor is in the Ship Date field. Using the same date formatting, key in the applicable date over the existing one and press Enter.
7 Click on Select Flow.
Now that you have clicked on Select Flow the system advances again.
STPI becomes the current flow.
FIPI, the following flow process in the 
DIFP 

CHOF screen
8 Do one of the following:

### TROUBLESHOOTING HELP FOR CONFIRMING AN ORDER <a id="troubleshooting-help-for-confirming-an-order"></a>

If you receive any of the following messages in the Help Line, the following actions are required:
There are no more flow sequences for this order. 
The order has been either confirmed or deleted.
If you wish to confirm the order and exit CHOF:
If you wish to cancel the confirmation and exit CHOF 
If you wish to remain in CHOF to work on other orders:
a) Click on Exit. A message will appear indicating that the order is being confirmed.
a) Key in the same order number and press Enter.
b) Click on Order Number to exit.
a) Key in your next order number and press Enter.
b) If required, change the Ship date.
c) Click on Select Flow.
d) Repeat the above three steps for each additional order that you wish to confirm.
e) When you finish processing your orders, click on Confirm. 
A message will appear indicating that order 1 of xxx is being confirmed.
After you select the last flow, the 
CHOF screen becomes blank and the button 
Confirm displays as an option.

1 Click on Exit to exit CHOF.
2 Enter LOOR. 
3 Key in the order number and click on Execute Query.
4 Check the Status field. 
5 Click on Exit.
There is at least one document to print for this order. 
1 Click on Exit to exit CHOF.
2 Enter PROM. Print the document(s) for this flow. See [Printing the Shipping Documents](expedicao.html#printing-the-shipping-documents) for further instructions.
3 Once the document(s) is printed, return to CHOF. Key in the order number and press Enter. Click on 
Select Flow and continue the procedure for confirming the order in the usual manner.
You cannot set this flow since this order does not have all locations entered.
1 Click on Exit to exit CHOF. 
2 Enter ENOR.
3 Click on Enter Criteria.
4 Key in the order number and click on Execute Query.
5 Click on Line Block.
6 Press Enter until the cursor is in the Location Code field.
7 Key in the location code and press Enter. Press the down arrow key to move to the next Line Block record. Repeat this step as many times as necessary until you have entered the Location Code into all of the Lines.
8 Click on Exit.
9 Enter CHOF. Key in the order number and press Enter. Click on Select Flow and continue the procedure for confirming the order.

### CONFIRMING ORDERS ONE LINE AT A TIME IN COOL <a id="confirming-orders-one-line-at-a-time-in-cool"></a>

As you are advancing and time-stamping the outbound flow processes of an order in the program CHOF, you have two choices when you reach the mandatory flow process COOR (Confirm Order). If you wish to confirm the entire order, select the COOR flow process in CHOF (see [Time-Stamping and Confirming Orders in 
CHOF](expedicao.html#time-stamping-and-confirming-orders-in-chof)). If you wish to only confirm specific lines of the order, you use the program Confirm 
Orders - Lines (COOL).
The following conditions must be met before you can confirm an order line in COOL:
 the line or lines that you wish to confirm must be fully allocated
 the line or lines must be at the flow immediately preceding the flow COOR (Confirm Order) unless the flow immediately preceding COOR is defined as non-mandatory in DIFP
 all documents attached to any flow before COOR must be printed.
EXAMPLE
If your outbound flows are ENOR, FLOW1, FLOW2, FLOW3 and COOR and if FLOW3 is defined as mandatory in DIFP, the line or lines must be at FLOW3. If FLOW3 is not mandatory, the line or lines must be at FLOW2.
1 Enter COOL. 

2 Click on Create Record.
3 Key in your order number and press Enter.
4 Key in the line number and press Enter twice. “Confirm” displays under the order number and the Ship 
Date Block appears at the bottom of the screen.

COOL screen
5 Click on Return to Main.
6 Click on Ship Date. In the Ship Date field, you enter the date on which this order line’s product will be shipped out of the warehouse. If the ship date is the same as the default, press Enter. (The default is the current company date of your system.)
If you need a different ship date than the default, key in the applicable date and press Enter. 
7 If you need to confirm another order line, click on Master Block. click on Create Record and repeat steps 
3 to 6.
Confirm appears under the order number.
The Ship Date 
Block displays.

COOL screen
8 When you have finished entering all the lines that need to be confirmed, click on Confirm. A message will display on your screen indicating that the line(s) are being confirmed.

### CHECKING CONFIRMED LINES IN LOOR <a id="checking-confirmed-lines-in-loor"></a>

You can check that the individual lines entered in COOL have been confirmed. You do so in the program Look 
Up Orders (LOOR).
Although individual lines of the order have been confirmed, the order’s status will not display as confirmed in 
LOOR. The order still has remaining lines that have not yet been confirmed. Once all lines are confirmed, then the order’s status will show as confirmed.
1 Enter LOOR. 
2 Key in the order number and click on Execute Query.
3 Click on Line Block. 
4 Use the up or down arrow keys to scroll to the line record that you confirmed in COOL. 
Click on 
Confirm to confirm the line(s).

LOOR screen showing an order with a line that was confirmed in COOL
5 If the Shipped Date field is completed, you know that the line is confirmed. Click on Master Block and Exit to exit the program.
If the Shipped Date field is blank, the line was not confirmed.
6 Click on Master Block and Exit to exit LOOR. Enter COOL and re-enter the line.
To print the documents attached to your system’s flow processes, proceed to [Printing the Shipping 
Documents](expedicao.html#printing-the-shipping-documents).

### CHANGING THE CONFIRMATION DATE IN CHCD <a id="changing-the-confirmation-date-in-chcd"></a>

You can change the confirmation date of a confirmed order in CHCD (Change Confirmation Date).
1 Enter CHCD.
Order status
The Shipped 
Date shows the date on which line 2 was confirmed.

CHCD screen
2 Press Enter to accept O (Order) as your document type.
3 Key in your order number and press Enter.
4 Click on Change Block.

CHCD screen showing prompt for new confirmation date
5 Key in your new confirmation date and press Enter.
6 Click on Process Change.
7 If required, key in any remarks for the change in confirmation date. When you finish entering your remarks (if any), click on Return.
8 Click on Exit.

### Generating the VICS Bill of Lading <a id="generating-the-vics-bill-of-lading"></a>

You generate the VICS bill of lading in VBOL (VICS Bill of Lading). This program allows you to consolidate one or more orders belonging to the same customer and generate a VICS bill of lading. There are a number of options for attaching orders to a VICS bill of lading: you can attach individual orders, a range of orders, a batch order created in GEBA or COPI, or all orders assigned a given load number. You can also specify order restrictions such as order date, ship date, arrive date and appointment date.
Once a VICS bill of lading is created, new orders can be added to it and existing orders removed from it at any time until the bill of lading is confirmed. Confirmed bills of lading are closed and cannot be modified.
The VICS bill of lading is restricted to orders belonging to the same customer.

### CREATING A NEW BILL OF LADING <a id="creating-a-new-bill-of-lading"></a>

1 Enter VBOL

VBOL screen
2 Click on Create Record.
3 Key in your customer code and press Enter or select your customer code from the pick list.
4 In the Arrive Date field, press Enter to accept the current date as your arrive date or key in a new arrive date and press Enter.
5 Key in your consignee code and press Enter or select your consignee code from the pick list.
6 Key in your carrier code and press Enter or select your carrier code from the pick list.
7 If required, key in your SID reference information and press Enter. If you do not require SID reference information, press Enter without entering anything to bypass this field.

8 If required, key in your CID reference information and press Enter. If you do not require CID reference information, press Enter without entering anything in this field.
9 If required, key in your reference 1/2 information and press Enter.
10 In the Trailer Number field, key in your trailer number and press Enter. If you do not require a trailer number, press Enter without entering a number to bypass this field.
11 In the Seal Number field, key in your seal number and press Enter. If you do not require a seal number, press Enter without entering a number to bypass this field.
12 In the Probill Number field, key in your probill number and press Enter. If you do not require a probill number, press Enter without entering a number to bypass this field.
13 In the FOB field, press Enter to accept the default value of N for No or key in Y for Yes and press Enter.
14 Proceed to select the appropriate freight terms:
15 In the Remarks field, do one of the following:
If the shipment is prepaid: If the shipment is collect:
If the shipment is to be billed to a third party:
a) In the Prepaid field, key in Y for Yes and press Enter.
a) Press Enter to bypass the Prepaid field.
b) In the Collect field, key in Y for 
Yes and press Enter.
a) Press Enter twice to bypass the Prepaid and Collect fields.
b) In the 3rd Party field, key in Y for Yes and press Enter.
c) Key in the name of the third party.
d) Key in the street address of the third party.
e) Key in the city, state or province and ZIP/postal code of the third party.
If you wish to add remarks to the bill of lading:
If you do NOT wish to add remarks to the bill of lading:
a) Key in Y for Yes and press Enter. a) Key in N for No and press Enter.

16 In the Commodity field, do one of the following:
17 If you entered Y for Yes in the Remarks field, key in your remarks. When you finish entering your remarks, click on Master Block.

Commodity Block of VBOL
18 If you entered Y for Yes in the Commodity field, proceed to enter your commodity information. When you finish, click on Return to Main.
19 Click on Order Block.
20 Click on Query Block.
If you wish to add commodity information to the bill of lading:
If you do NOT wish to add commodity information to the bill of lading:
a) Key in Y for Yes and press Enter. a) Key in N for No and press Enter.

Query Restriction Block
21 Proceed to enter your query restrictions. You can query by order number range, batch order number, load number, customer order number, purchase order number or date range. When you finish entering your query restrictions, click on Execute Query.

Order Block of VBOL showing all orders attached to a given bill of lading
22 Click on Master Block to exit the Order Block.
23 Click on Exit to exit VBOL.

### LOOKING UP A BILL OF LADING <a id="looking-up-a-bill-of-lading"></a>

1 Enter VBOL.
2 Click on Enter Criteria.
3 Key in your search criteria such as VICS bill of lading number, customer code, consignee code, carrier code, etc. When you finish entering your search criteria, click on Execute Query.
4 If you wish to look up a bill of lading’s remarks, 3rd party details or commodity information, press Enter until your cursor is positioned in the 3rd Party, Remarks or Commodity field and press F3. When you finish looking up your remarks, 3rd party details or commodity information, press F4 to exit.
5 When you finish looking up your bill of lading, click on Return to Main and Exit to exit.
FIELD DESCRIPTIONS
VICS Sequence Number The VICS sequence number. This number is generated in sequential order by 
AccellosOne 3PL.
VICS BOL Number The full VICS bill of lading number. This number consists of the VICS sequence number plus the EAN UCC prefix plus a check digit.
Counter in Order 
Block showing currently selected record plus total number of records

Customer Code The shipment’s customer.
EAN UCC Prefix The customer’s EAN UCC prefix.
To Arrive Date The shipment’s to arrive date.
Consignee Code The shipment’s consignee.
Carrier Code The shipment’s carrier.
SCAC Code The carrier’s SCAC code.
SID Reference The shipment’s SID reference information.
CID Reference The consignee’s CID reference information.
Reference 1/2 The shipment’s extra reference number 1/2.
Trailer Number The shipment’s trailer number.
Seal Number The shipment’s seal number.
Probill Number The shipment’s probill number.
Total Units The total number of units of all orders on the bill of lading.
Total Weight The total weight of all orders on the bill of lading.
Pallet/Slip The pallet/slip flag (either Yes or No). This feature requires a customized document from HighJump.
FOB If the shipment is “Free on Board”, this field will be set to Y for Yes.
Prepaid If the shipment is prepaid, this field will be set to Y for Yes.
Collect If the shipment is collect, this field will be set to Y for Yes.
3rd Party If the shipment is to be billed to a third party, this field will be set to Y for Yes.
Remarks If there are miscellaneous remarks attached to the bill of lading, this field will be set to Y for Yes.
Commodity If there is commodity information attached to the bill of lading, this field will be set to Y for Yes.
FIELD DESCRIPTIONS

### PRINTING A BILL OF LADING <a id="printing-a-bill-of-lading"></a>

You can print a bill of lading as many times as required as long as the orders on it are active; that is, neither deleted nor confirmed.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to print.
3 Click on Print Block.
Status A = Active
C = Closed
The bill of lading’s status.
Date Created The date that the bill of lading was created.
Date Closed The date that the bill of lading was either confirmed or deleted.
Last Printed Date The date that the bill of lading was last printed.
Printed By The operator who last printed the bill of lading.
Print Count The total number of times that the bill of lading has been printed.
FIELD DESCRIPTIONS

VBOL screen showing Select Printer window
4 Key in the code of the printer where the bill of lading is to print and press Enter. If you do not know the code, use the dropdown list.
5 Click Ok to send the document to the printer.
6 Click on Exit to exit.

### MODIFYING THE ORDERS ON A BILL OF LADING <a id="modifying-the-orders-on-a-bill-of-lading"></a>

You can add orders to and remove orders from a VICS bill of lading at any time as long as the following conditions are met:
 the order is unconfirmed
 the bill of lading itself is unconfirmed
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to modify.
3 Press Enter to position your cursor in the To Arrive Date field, then click on Order Block.

Order Block of VBOL
4 Do one of the following:
5 Click on Master Block and Exit to exit.

### CONFIRMING A BILL OF LADING <a id="confirming-a-bill-of-lading"></a>

When you confirm a bill of lading, the bill of lading is considered closed and cannot be modified. Confirming a bill of lading does not change the status of the orders on it; open orders remain open and confirmed orders remain confirmed.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to confirm.
3 Press Enter to position your cursor in the To Arrive Date field.
4 Click on Confirm/Delete.
5 When prompted to proceed with the confirmation, click on Yes.
6 Click on Exit to exit.
If you wish to delete all orders on the bill of lading:
If you wish to delete selected orders on the bill of lading:
If you wish to add orders to the bill of lading:
a) Click on Delete All.
b) When prompted to confirm the deletion, click on Yes.
a) Use your arrow keys to position your cursor over the order to be deleted and click on 
Delete One.
a) Click on Query Block.
b) Key in your query criteria and click on Execute Query.

### DELETING A BILL OF LADING <a id="deleting-a-bill-of-lading"></a>

If you wish to delete a bill of lading, you must first remove any orders attached to it. Then you use the Confirm/
Delete command in VBOL.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to delete.
3 Enter the Order Block and remove any orders attached to the bill of lading.
4 Proceed to confirm the bill of lading in the normal manner.

### CONFIRMING ALL ORDERS ON A BILL OF LADING IN CHOF <a id="confirming-all-orders-on-a-bill-of-lading-in-chof"></a>

You can confirm all orders on a bill of lading by specifying the VICS sequence number in the field of the same name in CHOF. When you confirm by VICS sequence number, all orders on the bill of lading are automatically confirmed. This option is not available if the order has been assigned to a load; orders assigned to a load can only be confirmed individually or by load number.
When you confirm orders by VICS sequence number in CHOF, the normal conditions for confirming an order must be met:
 all documents have been printed for each order
 all locations have been entered for each order line
1 Enter CHOF.
2 Press Enter to position your cursor in the VICS Sequence Number field.
3 Key in your VICS sequence number and press Enter.

CHOF screen showing confirmation by bill of lading number

4 Proceed to confirm the orders on the bill of lading normally in CHOF.

### Cancelling or Reprinting Order Documents <a id="cancelling-or-reprinting-order-documents"></a>

Normally, order documents are printed according to the flow process sequence. The program Requeue Order 
Documents (REOR)) allows you to print an order document out of sequence under certain circumstances.
You use the program REOR when you have to:
 cancel the printing of a document that is attached to a flow process
 reprint a document that is attached to a flow process
When you enter an order number into REOR, the program indicates the following information:
 the orders’s current flow process status
 the document attached to this flow process
 the number of times that this document has been printed to date
 the print status of this document. 
REOR screen
In REOR, the print statuses for documents are:
 all documents have been printed
 to be printed
 printed
 cancel
 requeue
The last flow process that was completed for this order up to this time.
Document attached to this flow process
Number of times that this document has been printed.
Print status of this document

Depending on the document print status, you have the option of cancelling the printing of the document or reprinting it as necessary. The following table shows the options that are available depending on the document status.

### CANCELLING ORDER DOCUMENTS IN REOR <a id="cancelling-order-documents-in-reor"></a>

There may be times when you need to cancel the printing of a document that is attached to a flow process. 
This would occur, for example, if you need to advance to the next flow without printing the document that is attached to the current flow (the flow that was most recently confirmed in CHOF).
Use the following procedure when the REOR Print Status field indicates “To be printed” and you need to cancel the printing of that document.
1 Enter REOR.
2 Key in the order number and press Enter. The system displays the documents that are attached to this order’s current flow process.
3 Check that the print status indicates “To be printed.” If there is more than one document, use the up and down arrow keys to place the cursor beside the document that you wish to cancel.
4 Click on Cancel. 
Print Status Description Options 
All documents have been printed
The order has been confirmed. All process flows have been completed and all their attached documents have been printed. There are no remaining documents to either requeue (reprint) or cancel. 
None.
The Help Message Line displays “This order has no documents to be requeued or cancelled.”
To be printed The displayed document needs to be printed now according to the flow process sequence.
Click on Cancel to cancel printing of this document. 
This will allow the system to advance to the next flow process without printing of the displayed document.
If you want to print the document, exit REOR and 
Enter PROM to print the attached document.
Printed The displayed document has been printed before.
Click on Requeue to reprint this document. 

REOR screen
5 Click on Order Number and Exit to exit the program REOR.
6 Enter CHOF. In CHOF, the system will now allow you to select the next flow process in the sequence. 
Continue confirming the order in the usual manner.

### REPRINTING ORDER DOCUMENTS IN REOR <a id="reprinting-order-documents-in-reor"></a>

You may need to reprint a document that is attached to a flow process. For example, you need to replace a lost or damaged document or you need a duplicate for whatever reason. 
Use the following procedure when the REOR Print Status field indicates “Printed” and you need to reprint the attached document.
1 Enter REOR 
2 Key in the order number and press Enter. The system displays the documents that are attached to this order’s current flow process.
3 Check that the print status indicates “Printed.” If there is more than one document listed, use the up and down arrow keys to place the cursor beside the document that you need to reprint.
NOTE Depending on your system setup, some documents cannot be reprinted. 
The system will only allow you to reprint documents that have the Flag Reprint field set up to Y in the program DOCU.
The second function key button toggles between the “Cancel” 
and “Requeue” 
options.
Set the print status to “Cancel”.
Printing of the 
PICK is no longer needed and the system will allow you to advance to the next flow.

REOR screen
4 Click on Requeue.
5 If the message “Print all order lines or new lines only” appears, do one of the following:
If you wish to print all order lines:
If you wish to print only order lines added after the last printing of the document:
a) Click on All Lines. a) Click on New Lines Only.
The pick document has been printed once before.
Requeue is available as a reprinting option.

REOR screen
6 Click on Order Number and Exit to exit the REOR program. 
7 Enter PROM and reprint the document.

### REQUEUING A RANGE OF ORDER DOCUMENTS IN RERO <a id="requeuing-a-range-of-order-documents-in-rero"></a>

You can requeue a range of order documents in RERO (Requeue a Range of Orders). You requeue order documents when you wish to print or reprint order documents that have been cancelled.
1 Enter RERO.
2 Key in your starting order number and press Enter. If you wish to requeue all order documents, you can set your starting order number to zero.
3 Key in your ending order number and press Enter.
4 Key in your document code and press Enter or use the pick list function to select it.
Clicking on 
Requeue changes the print status and the pick document is now set to requeue (reprint).

RERO screen
5 Click on Process.
6 If auto-processing is activated for the document, you will be prompted to start auto-processing each order document. If you enter Y for Yes, the document will auto-print. If you enter N for No, no auto-printing will occur and you will have to print the document in PROM or PROR. 

### REPRINTING SHIPPING LABELS IN RELA <a id="reprinting-shipping-labels-in-rela"></a>

You use the program RELA (Reprint Labels) to reprint AccellosOne 3PL’s standard shipping label. RELA is a general purpose reprint program that is more flexible than PROR or PROM. It allows you to reprint labels for a specific line of an order, to specify the number of copies to be reprinted and to reprint at any flow.
RELA prints one label for each pallet; pallets are defined at the detail line level according to the item’s quantity breakdown profile. For example, if your standard quantity breakdown is 10 cases per pallet and your order line quantity is 35 cases, RELA will print four labels — one for each of the three full pallets and one for the partial pallet of five cases.
1 Enter RELA.
2 Key in your document code and press Enter or use your pick list to select it.
3 Key in O for Order as your document type.
4 Key in your order number and press Enter.
5 If you are reprinting an outbound pallet ID label, select the appropriate pallet ID from the dropdown list.
6 If required, key in your line number and press Enter.

RELA screen
7 In the Number of Labels field, key in the number of extra labels that you require and press Enter.
8 When the Printer Block appears, key in the code of the printer where these labels are to print and press 
Enter. If you do not know the code, use the dropdown list.
9 Click Ok. The labels will print and the system returns to the Main Menu.

### Inspection Orders <a id="inspection-orders"></a>

You use inspection orders when you need to retrieve product from inventory for a government inspection. If all product passes the inspection, the inspection order is confirmed with a ship quantity of zero. If product is damaged and does not pass the inspection, the inspection order is confirmed with a shipped quantity equal to the quantity of product that was destroyed.
Inspection orders are similar to R-type order lines. That means that if you do not enter all inventory levels in 
ENOR, AccellosOne 3PL will automatically select the appropriate values during order entry.
1 Create a dummy consignee in CONS for government inspections. For example, create a code called 
INSP.

Dummy consignee in CONS called INS
2 Enter ENOR
3 In the Customer Code field, key in the code of the customer whose product you are inspecting and press 
F9.
4 In the Order Type field, key in I for Inspection and press Enter.
5 Press Enter to bypass the Customer Code field.
6 Proceed to enter the order header in the normal manner. The consignee should be the dummy consignee that you created in CONS for inspection orders.
7 In the Line Block, enter the product that you wish to inspect. 

Line Block of ENOR showing five cases of product A1 being inspected
8 Do one of the following: 

### Distribution Orders <a id="distribution-orders"></a>

You use a D (Distribution) type order to cross dock and to ship an item at the same time. For example, you need to fill an order with product that has just arrived at the warehouse. However, this product has not been received into the system through ENRE. In this situation, you use a D type order, which allows you to receive and to ship out at the same time.
You create a D type order in which you record the details of the product that you are shipping out. The system takes the information from the order that you create and uses it to automatically generate a mirror image receipt.
If all the product passes the inspection:
If some of the product is damaged and does not pass the inspection:
a) Change the to ship quantity to zero and confirm the order in 
CHOF in the normal manner.
a) Change the to ship quantity to the quantity of product that must be destroyed and confirm the order in CHOF in the normal manner.

You create only one record — a Distribution Order type but the system generates two records:
 a Distribution Order type recording the process of shipping the product out of the warehouse
 a receipt recording the process of receiving the product into the warehouse and the order records

### SETTING UP DISTRIBUTION ORDERS <a id="setting-up-distribution-orders"></a>

Distribution orders require shipping lanes and shipping lane assignments. You set up your shipping lanes in 
SHLA. Shipping lanes must be attached to a staging location.
SHLA screen
You set up your shipping lane assignments in SLAS. In SLAS you assign your consignees to shipping lanes. 
A consignee can be assigned to only one shipping lane, but the same shipping lane can contain multiple consignees.
NOTE You can only use a Distribution Order if the entity has been received into the system on previous occasions. For example, your system has previously received the entities Item A, Lot 1 and Item A, Lot 2. The system would allow you to create a Distribution Order for Lot 1 or Lot 2.
Now, a new entity Item A, Lot 3 has just arrived at the warehouse and you would like to ship it out as a Distribution Order. The system would not allow you to do this, as it does not recognize an entity that has never been entered into the system before.

SLAS screen
You can override your shipping lane assignments in ENOR.

### ENTERING A DISTRIBUTION ORDER IN ENOR <a id="entering-a-distribution-order-in-enor"></a>

1 Enter ENOR.
2 Key in your customer code and press F9 (Previous Field) to move the cursor to the Type field. 
3 Key in D for Distribution and press Enter.
4 Complete the ENOR Header Block in the normal manner. In the Shipping Lane Code field, you can override your shipping lane assignment set up in SLAS.
5 In the Line Block, leave the Type field with the D that is generated by the system.

ENOR Line Block for a distribution order
You must complete all inventory levels for the entity.

6 Complete the Line Block in the normal manner. You must enter all inventory level fields for the entity that you are shipping. A pick list is available for each of the inventory level fields, if you need to use it.
7 When you have completed all lines for this order, click on Master Block to return to the order’s Header 
Block screen.
8 Click on Exit to exit the program. A Message Block will appear on the screen listing the number of this distribution order and the number of the corresponding receipt that the system generated.

Transferring message

### CONFIRMING A DISTRIBUTION ORDER <a id="confirming-a-distribution-order"></a>

1 Enter CHOF.
2 Confirm the order in CHOF in the normal manner.
If necessary, enter REOR to cancel the printing of documents attached to the outbound flows of this order and then return to CHOF.
3 In CHOF, after you click Execute Confirm, a Message Block will appear on the screen requesting a location code and a warehouse code.

CHOF screen showing prompt for location and warehouse

4 Key in your location code for the cross-dock product and press Enter. If you do not know the code, use the pick list and then press Enter. (This transaction will not affect Location Block inventory records in 
LOEN since the product was not actually received nor stored in a warehouse location — it was only cross docked.)

CHOF screen showing location and warehouse for cross-dock product
5 Press Enter to accept the system-generated Warehouse Code. If the Warehouse Code field is blank, key in the warehouse code for the location that you entered in the previous step and press Enter.
The confirmation Message Box appears on the screen. Both the distribution order and the corresponding receipt are being confirmed. The screen blanks out. 
6 Click on Exit to exit CHOF.
You can now go into LOOR to view the details of this Distribution Order and into LORE to view the details of the corresponding receipt. Both should be confirmed.

### LOOKING UP A DISTRIBUTION ORDER <a id="looking-up-a-distribution-order"></a>

1 Enter LOOR.
2 In the Order Number field, key in the number of the Distribution Order.
3 Click on Execute Query. The order will display on the screen.

LOOR screen showing details of a distribution order
4 Note the Transfer Receipt field. This displays the number of the mirror image receipt that the system created and that corresponds to the Distribution Order. 
5 Click on Exit to exit LOOR.
6 Enter LORE. In the Receipt Number field, key in the corresponding Receipt Number.
7 Click Execute Query.
corresponding receipt number distribution order number

LORE screen showing receipt that corresponds to a distribution order
8 Note the On Order(s) field, which displays the number of the distribution order.
9 Click on Exit to exit LORE.

### Transfer Orders <a id="transfer-orders"></a>

You use a transfer order to transfer product from one warehouse customer to another. For example, two warehouse customers have an identical item in common. Customer A is running low on the product and asks 
Customer B for a specified amount. 
The product is not being shipped out; it is only having its ownership transferred from one customer to another. 
To record the change, you create a transfer order. When you confirm the transfer order, AccellosOne 3PL will automatically create a confirmed receipt in the name of the new owner.

If the product being transferred has process values such as catch weights or serial numbers attached to it, the process values will be transferred as well provided that both the from item and the to item have the same item process code(s) defined in IPRO (the item process profiles defined in IPRP need not be the same).

### SETTING UP TRANSFER ORDERS <a id="setting-up-transfer-orders"></a>

You set up transfer orders by creating a transfer profile in TRPR (Transfer Profile). In this profile, you define the charges, if any, associated with the transfer, the renewal date for transferred product and the document, if any, that will be printed when product is transferred. The profile that you create in TRPR must be attached to all customers who wish to transfer product among each other.
In order to perform a transfer, several additional conditions apply at the customer level:
 both customers track product in the same way (i.e., they have the same number of SKU’s in their quantity breakdown profiles — pallets/cases, etc.)
 both customers have the same number of inventory levels defined in DILP though not necessarily the same inventory terminology code (for example, an item/lot/pallet ID customer can transfer product to an item/date/pallet ID customer)
Further conditions apply at the item level:
 both items have the same item code
 both items have the same weight type
 if customers calculate expiry dates by means of a formula in ITSH, both customers must use the same formula and the ITSH profile(s) containing this formula must be attached to the appropriate items
NOTE If you wish to transfer product from one customer to another to correct an error in your inventory records — that is, there is no change in ownership because customer A is transferring inventory to customer B — you enter a transfer adjustment in ENAJ.
FIELD DESCRIPTIONS
Transfer Profile Code Mandatory
Your transfer profile code.
Description Mandatory
Your description for this code.

Receipt Charge Type N = None
H = Handling
S = Storage
R = Regular
If you set this flag to None, there are no charges. If you set this flag to Handling, transferee pays handling only (that is, charges set up in IHAP). If you set this flag to Storage, transferee pays initial storage only (that is, charges set up in IISP). If you set this flag to Regular, transferee pays all charges associated with a regular receipt (that is, charges set up in IHAP and IISP).
Renewal Type O = Original Date
R = Receipt Date
EXAMPLE
Customer A (transferor) received product on August 10. Product was transferred to Customer B (transferee) on August 20.
Scenario 1 (Both customers have anniversary monthly billing)
If you set this flag to O for Original Date, product renews on September 10 and Customer B will pay all charges from this date on. The next renewal date will be October 10. If you set this flag to R for Receipt Date, Customer B will start paying on August 20 and product renews on September 20.
Scenario 2 (Customer A is on anniversary monthly billing and Customer B is on monthly first of month billing)
If you set this flag to O for Original Date, product renews on September 10 and Customer B will pay all charges from this date on. The next renewal date will October 1. If you set this flag to R for Receipt Date, Customer B will start paying on September 1 and product renews on October 1.
Scenario 3 (Customer A is on anniversary monthly billing and Customer B is on anniversary weekly billing)
If you set this flag to O for Original Date, product renews on September 10 and Customer B will pay all charges from this date on. The next renewal date will be September 17. If you set this flag to R for Receipt Date, Customer B will start paying on August 27 and product renews on September 3.
FIELD DESCRIPTIONS

Scenario 4 (Customer A is on anniversary monthly billing and Customer B is on anniversary weekly billing for first period and then anniversary monthly billing for subsequent periods)
If you set this flag to O for Original Date, product renews on September 10 and Customer B will pay all charges from this date on. The next renewal date will be October 10. If you set this flag to R for Receipt Date, Customer B will start paying on August 27 and product renews on September 27.
Document Code (DOCU) Optional
The document, if any, that you wish to print for each transfer. This document will print instead of any documents attached to the flow ENRE in the transferee’s workflow profile defined in DIFP. 
If you do not enter a document code in this field, AccellosOne 3PL will print the document or documents defined in the transferee’s DIFP profile for the flow CORE. Any documents attached to earlier flows such as ENRE will not be printable.
You enter a document code in this field when you wish to print an additional receiving document that is not attached to the transferee’s workflow profile at the CORE flow.
Extra Charge Profile 
Code (ECHP)
Optional
The extra charge profile code for the charges, if any, for the transfer itself excluding any normal receipt, storage or handling charges. These charges can apply to either the transferor or transferee.
Free Storage for TransfereeIf you select this checkbox, you can define a free storage period for the transferee in a transfer order. That is, although the transferee now owns the product, the transferor pays renewal storage.
Free Days for Transferee Only available if Free Storage for Transferee checkbox is selected
The number of free days for the transferee paid for by the transferor.
FIELD DESCRIPTIONS

1 Enter TRPR.
2 Click on New .
3 Key in a transfer profile code and press Enter. Then key in a meaningful description and press Enter again.
4 Key in the appropriate receipt charge type (N for None, H for Handling Only, S for Storage Only or R for 
Regular) and press Enter.
5 Key in the appropriate renewal type (O for Original Date or R for Receipt Date) and press Enter.
6 If you wish to print a particular document for each transfer, key in your document code and press Enter or select it using the pick list. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select.
7 In the Extra Charge Profile Code field, key in your extra charge code and press Enter or press Enter with the field blank to bypass this option.
8 If you wish to set up a free days storage period for the transferee, click on the Free Storage for Transferee checkbox and press Enter. Then key in the number of free days in the Free Days for Transferee field and press Enter. Next select the appropriate charge code from the Charge Code for Transferee Free 
Days pick list. Lastly, select the appropriate free days charge type from the dropdown list (Daily or Balance).
Charge Code for Transferee Free Days
Only available if Free Storage for Transferee checkbox is selected
The charge code used to calculate charges for the transferor during the free days period. The transferor’s rates will apply to this charge; not the transferee’s.
Free Days Charge Type Balance
Daily
If you select Balance, a single charge will be generated based on the balance of inventory still in the warehouse at the end of the free days period. If you select Daily, a charge will be created for each day in the free days period based on the balance of inventory at the end of each day.
FIELD DESCRIPTIONS

Transfer Profile
9 When you finish setting up your transfer profile, click on Save to save your changes.
10 Click on Exit to exit TRPR.
11 Attach your new profile to all customers who wish to transfer product among each other.

### ENTERING A TRANSFER ORDER <a id="entering-a-transfer-order"></a>

1 Enter ENOR
2 In the Customer Code field, key in the code of the customer from whom you are transferring product and press F9.
3 In the Order Type field, key in T for Transfer and press Enter.
4 Press Enter to bypass the Customer Code field.
5 In the Consignee Code field, key in the code of the customer to whom you are transferring product and press Enter.
6 Key in your same-type code for your sold-to code and press Enter.
7 Press Enter the required number of times to bypass the Order Date, To Ship Date and To Arrive Date fields.
8 If required, enter your customer order number or purchase order number.
9 In the Carrier Code field, key in your N/A code and press Enter.
10 In the Freight Term field, use your pick list to select the NA (Not Applicable) code.

11 Complete the rest of the Header Block fields in the normal manner as if you were entering an R-type order.

ENOR screen showing a transfer order
12 In the Line Block, leave the Type field with the T that is generated by the system. 
13 Complete the rest of the Line Block fields in the normal manner as you would for an R type order until you reach the Inventory Level fields.
14 In the Inventory Level fields, do one of the following:
15 In the Ordered Quantity field, key in the amount and SKU that is being transferred and press Enter.
If you wish to transfer a specific inventory entity:
If you wish to transfer multiple inventory entities (for example all lots belonging to a specific item or all pallet ID’s belonging to a specific lot):
a) Enter all inventory levels. a) Enter your item code only and leave the lot field blank (scenario one) or enter your item code and lot number only and leave the pallet ID field blank (scenario two).
Order type = T for 
Transfer

ENOR screen showing a transfer order
16 Complete the remaining Line Block fields in the normal manner. 
17 When you have finished entering all lines for this order, click on Return to Main. 
18 Note the order number and then click on Master Block and Exit.
19 Advance the flows of the order in CHOF and print any required documents.
You are now ready to confirm the transfer order and to print its attached documents.

### CONFIRMING A TRANSFER ORDER <a id="confirming-a-transfer-order"></a>

1 Enter CHOF.
2 Key in the transfer order number and press Enter.
3 Click on Select Flow for the flow COOR (Confirm Order).
4 Click on Exit to exit CHOF. 
A message box will appear on the screen to indicate that the order is being confirmed.
A second message box will then display indicating the corresponding receipt number.

CHOF screen showing the corresponding receipt number for the transfer order
Key in the amount that is to be transferred to another customer.

The order has been confirmed and you can now look up the transfer order in LOOR.

### LOOKING UP A TRANSFER ORDER <a id="looking-up-a-transfer-order"></a>

1 Enter LOOR.
2 Key in the order number in the Order Number field.
3 Click on Execute Query.

LOOR screen showing a transfer type order
4 When you have finished viewing the details of this order, click on Exit to exit LOOR.
5 Enter LORE
6 Key in the number of the corresponding receipt in the Receipt Number field.
7 Click on Execute Query.
Transfer order number
Transfer receipt number

LORE screen showing the receipt that corresponds to the transfer order
8 When you have finished viewing the details of this receipt, click on Exit to exit LORE.

### CLEARING A TRANSFER ORDER IN CHAT <a id="clearing-a-transfer-order-in-chat"></a>

If a transfer order fails to create a transfer receipt, a warning message will appear in CHOF each time that you confirm an order. To clear the message, you must run CHAT (Change Auto Transfer Order to Regular). After the message is cleared, it will no longer appear in CHOF.
The transfer receipt must be manually entered in ENRE when it is not automatically generated in CHOF.
1 Enter CHAT.
2 Key in your order number and press Enter.
Transfer receipt number
The transfer order number displays in the 
Reference 
Number field.

CHAT screen
3 Click on Clear Auto-Transfer.
4 Click on Exit to exit.

### Entering Freight Type or Non-Inventory Orders <a id="entering-freight-type-or-non-inventory-orders"></a>

You use freight-type or non-inventory orders to track the shipping of non-inventory items such as containers or other equipment that are empty and do not contain product. For example, you receive product from a shipper in containers and you want to return the containers to the original shipper.
You can also use freight-type or non-inventory orders to enter an order that will be automatically transferred to 
AccellosOne Transport.
1 Enter ENOR.
2 Press F9 to position your cursor in Order Type field.
3 Key in F for Freight and press Enter.

ENOR screen showing Order Type set to F for Freight 
4 Enter the order header in the normal manner by specifying your customer, consignee, carrier and other mandatory information.

ENOR screen showing the Class Block
5 When the Class Block appears, key in your freight class for the equipment that you are shipping and press Enter or select if from the pick list.
6 Key in the number of units and press Enter.
7 Key in the weight and press Enter.
8 If required, enter values in the Cube, Pallets and Amount fields.

ENOR screen showing 10 units of the freight class FAK being shipped
9 When you finish entering your freight information, click on Return to Main to exit create mode.
10 If you wish to add remarks to your freight class, click on Remarks and proceed to enter any remarks.
11 Click on Master Block and Exit to exit.
12 Proceed to advance the flows of the freight order in CHOF in the normal manner and print any required order documents in PROM or PROR.

### Picking to Clean <a id="picking-to-clean"></a>

The pick to clean option allows you to pick all inventory for a particular item, level 2, level 3 or level 4 without entering a quantity in the Ordered Quantity field. AccellosOne 3PL will automatically populate the Ordered 
Quantity field with the total quantity of all available inventory for the inventory levels that you specify. 
Pick to clean supports both R-type and P-type order lines. However, you cannot pick to clean inventory on shippable or non-shippable hold.
1 Enter ENOR.
2 Enter the order header information normally.
3 In the Line Block, enter the required number of inventory levels. You can pick to clean at the lowest inventory, the highest inventory level or any inventory level in between.
4 In the Ordered Quantity field, key in C and press Enter.

ENOR screen showing C in Order Quantity field
5 Continue to enter your order lines.
6 When you finish entering your order lines, click on Return to Main. Then click on Master Block and Exit to exit.

### Broker Orders <a id="broker-orders"></a>

A broker order is an order shipped by a broker account. A broker account is a customer who is allowed to sell and ship inventory from other non-broker or “owner” customers. A single broker order can contain product from many different owner customers.
Broker accounts do not pay renewal storage because they do not own the inventory.
Any charges attached to the order header are billed to the broker, while charges attached to the order line are billed to the owner customer.

### SETTING UP A BROKER CUSTOMER <a id="setting-up-a-broker-customer"></a>

To create a broker account, you set up a customer in CUST with an account type of B for Broker. In the Broker 
Block of the broker account, you enter all the customers whose products this broker is allowed to ship. You then set the Allow Replacement of Same Item flag to the appropriate value for each owner customer: Y for 
Yes or N for No.
You enter C in the Ordered 
Quantity field

When same item replacement is activated, AccellosOne 3PL will consider all items with the same item code as the same product and will allocate the order line according to the PIPR profile of the broker customer. For example, if you allocate product by absolute FIFO, AccellosOne 3PL will allocate the oldest product first regardless of ownership. Likewise, AccellosOne 3PL will ignore product ownership and pick to clean first, then pick from partial locations and lastly pick from full pallet locations according to your parameters in ILOP. 
The following restrictions apply to same item replacement:
 the two or more customers must share the same DILP profile
 the two or more items must have the same item code in ITEM and share the same ITSH profile
 the two or more items must share the same PIPR profile if a PIPR profile is attached to the item

CUST screen showing Account Type set to B for Broker
FIELD DESCRIPTIONS (BROKER BLOCK)
Customer Code The owner customer whose product the broker is authorized to ship.
Allow Replacement of 
Same Item
N = No
Y = Yes
If you set this flag to N for No, same item replacement is deactivated for the owner customer. That is, if you wish to ship product belonging to a specific owner customer when entering a broker order, you must key in that customer’s code in the Line Block of ENOR.
If you set this flag to Y for Yes, same item replacement is activated for the owner customer. That is, AccellosOne 3PL will ignore product ownership and allocate product based on the PIPR profile of the broker customer.

Broker Block with three customers shown

### SHIPPING A BROKER ORDER <a id="shipping-a-broker-order"></a>

A single broker order can contain product from many different owner customers. If the broker account has its own inventory, a broker order can also contain product belonging to the broker account.
If the workflow profile set up in DIFP for the broker account differs from the workflow profile of the owner customer, the profile of the broker account will override the profile of the owner customer.
1 Enter ENOR and create an order for the broker customer.
2 Enter the rest of the header information in ENOR in the normal manner.
3 When the Line Block appears, enter your line type, remarks, etc. in the normal manner.
4 When your cursor is positioned in the Item field, do one of the following:
If you are shipping product belonging to the owner customer and same item replacement is activated:
If you are shipping product belonging to the owner customer and same item replacement is deactivated:
If you are shipping product belonging to the broker:
a) Proceed to next step. a) Press F9 until your cursor is positioned in the Customer 
Code field.
b) Key in the customer code of the owner customer — that is, the customer whose product you are actually shipping — and press Enter.
a) Proceed to next step.

ENOR screen showing order for broker 1 containing product from customer A
5 Enter the remaining Line Block information normally.
6 Add another line to your broker order or click on Exit to exit.

### Processing Proof of Delivery in POD <a id="processing-proof-of-delivery-in-pod"></a>

The program Proof of Delivery (POD) validates the quantities of product that were actually delivered to the consignee and allows you to process product that is returned to the warehouse. 
Consignees may not accept all or some of the ordered quantities for various reasons. The following are two possible examples of undelivered product: 
EXAMPLE 1
Shipped Quantity = 10 cases to Consignee A
Delivered Quantity = 8 cases are accepted
Returned Quantity = 2 cases are returned due to damage
EXAMPLE 2
Shipped Quantity = 20 cases to Consignee B
Delivered Quantity = 0 cases
Returned Quantity = 20 cases as Consignee B cannot issue the COD payment
Once you have recorded the quantities that were delivered for an order, POD will also cause the system to perform the following functions: 
 update the Delivered field in LOOR

 create a new receipt to begin the process of re-receiving the undelivered product into the warehouse. 
(Later, you will need to confirm this receipt in order to update the inventory records.)
 show the transaction details in LOEN for the POD record, the transfer receipt and the original order 
There are two procedures in POD. You use one procedure when you need to validate that the order was delivered in full. You use the other procedure when the order has undelivered items that are returned to the warehouse.

### ENTERING PROOF OF DELIVERY FOR AN ORDER DELIVERED IN FULL <a id="entering-proof-of-delivery-for-an-order-delivered-in-full"></a>

This procedure will validate delivery of an entire order in full. The quantities that were shipped out were the same as the quantities that were delivered to and accepted by the consignee. If the order was made up of several products and therefore included multiple lines, the full quantity for each line was accepted by the consignee.
1 Enter POD.
2 Key in your order number and press Enter. The order must be confirmed before you can process it in 
POD.
3 Press Enter to accept the current date as your delivery date or key in a new delivery date and press 
Enter.
4 Key in your delivery time and press Enter or press Enter to accept the default value of 00:00 to indicate no delivery time.
NOTE You can only perform POD once for an order.

POD screen showing the Header Block details of order 1
5 Click on In Full. 
If the order was delivered in full, press F1 (In Full).

POD screen showing alert message
6 A message displays on the screen asking if you want to proceed with the update. Key in Y for Yes. You are taken out of POD.

### ENTERING PROOF OF DELIVERY FOR AN ORDER NOT DELIVERED IN FULL <a id="entering-proof-of-delivery-for-an-order-not-delivered-in-full"></a>

This procedure will process an order with undelivered product that was returned to the warehouse. If the order was made up of different items and therefore included multiple lines, each line will be validated individually. 
1 Enter POD.
2 Key in your order number and press Enter. The order must be confirmed before you can process it in 
POD.
3 Press Enter to accept the current date as your delivery date or key in a new delivery date and press 
Enter.
4 Key in your delivery time and press Enter or press Enter to accept the default value of 00:00 to indicate no delivery time.

POD screen showing the Header Block details of order 13
5 Click on Exceptions. The system populates the Line Block.
If the order was not delivered in full, press F3 (Exceptions).

POD screen showing the details of order 13
6 The cursor moves to the Delivered field of the first line and prompts you to complete it. 
7 Do one of the following:
If the quantity delivered to and accepted by the consignee matches the shipped quantity:
If the delivered quantity does 
NOT match the shipped quantity:
a) Click on Set to Shipped. a) Key in the actual amount that was delivered and press Enter.
The Line Block displays the line details of the order: 
the item, the order quantity and the shipped quantity.

POD screen showing the details of order 13
8 Repeat step 7 of this procedure for each line. 
9 When you have finished setting the delivered amount in the Delivery field for all lines of this order, click on Return to Main.
F2 (Set to 
Shipped) will fill in the 
Delivered field with the same quantity as the Shipped field.
Key in any corrections.

POD screen showing Process button
10 F1 (Process) now appears as an option. Click on Process. You are taken out of POD.
You can now enter LOOR, and LOEN to check that the Proof of Delivery has been recorded into the system. 
You can also enter LORE to check the details of the corresponding receipt that the system created in order to re-receive the returned product. 

### LOOKING UP A PROOF OF DELIVERY TRANSACTION IN LOOR <a id="looking-up-a-proof-of-delivery-transaction-in-loor"></a>

1 Enter LOOR.
2 Key in your order number.
3 Click on Execute Query and the order details will display on the screen.
NOTE You will need to finish processing the corresponding transfer receipt that the system has generated. You must enter the Location Code(s) in the transfer receipt, confirm it and print its attached documents. See [Looking Up a Proof of Delivery 
Transfer Receipt in LORE](expedicao.html#looking-up-a-proof-of-delivery-transfer-receipt-in-lore).
You must press F1 (Process) to enter the changes into the system; otherwise, the data will not be validated and processed.

LOOR screen showing transfer receipt for order 13
4 Note the Transfer Receipt Number and write it down for future reference.
5 Click on Line Block and the first line record will display.
6 Check the Deliver Quantity field. It shows the amount that was delivered and accepted by the Consignee. 
You can compare this to the data in the Ordered Quantity and Ship(ped) Quantity fields.
7 The difference between the Deliver(ed) Quantity and the Shipped Quantity is the quantity that was returned to the warehouse and it is the quantity that will show on the Transfer Receipt.
8 Use the up and down arrow keys to view all line records.
Transfer receipt number that the system created in order to re-receive the returned product.

LOOR screen showing the details of order 13
9 When you have finished viewing all line records, click on Order Block and Exit.

### LOOKING UP A PROOF OF DELIVERY TRANSFER RECEIPT IN LORE <a id="looking-up-a-proof-of-delivery-transfer-receipt-in-lore"></a>

1 Enter LORE.
2 Key in your receipt number.
3 Click on Execute Query and the receipt details will display on the screen.
The Deliver 
Quantity field now shows the amount that was entered in 
POD.

LORE screen showing the Header Block details of transfer receipt 22
4 Note the Reference Number and write it down for future reference. It is the number of the corresponding order with returned product.
5 Also note that the Location Status, which will likely display as “Missing.”
6 Click on Line Block and the first line record will display.
The reference number is the number of the corresponding order with the returned product.
Location status

LORE screen showing the Line Block details of transfer receipt 22
7 The Expect Quantity and Receive Quantity fields show the amount of this item that is being received into the warehouse. (This is the same quantity as was returned for the corresponding order.)
8 If this receipt has more than one Line Block record, use the up and down arrow keys to view the other records.
9 When you have finished viewing all line records, click on Receipt Block and Exit.

### LOOKING UP A PROOF OF DELIVERY RECORD IN LOEN <a id="looking-up-a-proof-of-delivery-record-in-loen"></a>

1 Enter LOEN.
2 Key in the customer code of the owner of the product and press Enter.
3 Key in the item code and press Enter. 
4 Key in the applicable Inventory Level fields.
5 Click on Execute Query and the details will display on the screen.
6 Click on History Block.
NOTE The Location Code will be missing for each Line Block record. Enter ENRE and key in the locations for each of the Line Block records of this order. 
You will also need to confirm the receipt in CHRF and to print the attached documents in PRRE or PRRM (or bypass the printing requirement in RERE).
The returned product is being rereceived into the warehouse.

LOEN screen showing the History Block
7 Use the up and down arrow keys to scroll down to the Proof of Delivery transaction that you are looking for. The transaction type will show as PD.
The corresponding transfer receipt and order numbers
The POD transaction
The original confirmed order transaction

LOEN screen showing the History Details Block
8 Click on History Detail Block. When you have finished viewing the details, Click on History Block.
9 If you wish to view the History Block details for the original order and the transfer receipt, use the up and down arrow keys to scroll down to the transaction that you are looking for. Then click on History Detail 
Block. When you have finished viewing the details, click on History Block. 
10 Repeat until you have finished viewing the details for all of the transactions that are related to this Proof of Delivery.
11 Click on History Block, Inventory Block and Exit.

A adjustments creating new inventory 153 to expiry dates 187 to holds 169 to inventory 140 to level 2 descriptions 188 to weights 189 transfer type 149 alternate type codes and alternate item codes, using in inventory queries 135
B broker orders 303 cancelling order documents 277 cancelling receipt documents 85
Carrier Block (ENRE) 33
Change Auto Transfer Order to Regular (CHAT) 299
Change Confirmation Date (CHCD) 264
Change Entity Information (CHEI) 187, 188
CHAT (Change Auto Transfer Order to Regular) 299
CHCD (Change Confirmation Date) 264
Check Qty Breakdown and Receipt Qty (CVQB) 65
CHEI (Change Entity Information) 187, 188
CHOF (Time-Stamp and Confirm Orders) 257
CHRF (Time-Stamp and Confirm Receipt) 90
CHRL (Change Inventory Level on Receipt Line) 46
CICP (Check-In Configuration Parameters) 103
Clear Weights (CLWE) 196 clearing weights 196
CLWE (Clear Weights) 196
Confirm Orders - Line at a Time (COOL) 261 confirming orders 257 receipts 89 confirm-type receipts 52
COOL (Confirm Orders - Line at a Time) 261
CORL (Confirm Receipts - Line at a Time) 94 cross-docking 284
CVQB (Check Qty Breakdown and Receipt Qty) 65
D default sort sequence in LOOR, changing 249 default sort sequence in LORE, changing 77 descriptions for level 2, adjusting in CHEI 188 distribution-type orders 284 documents for orders 250 for receipts 78
E
ENAJ (Enter Adjustment)
creating new inventory 153 negative 146 overview 140 positive 142 transfer 149
ENOR (Enter Orders) See orders
ENRE (Enter Receipts) See receipts
Enter Adjustment (ENAJ)
creating new inventory 153 negative 146 overview 140 positive 142 transfer 149
Entering 203 expiry dates, adjusting in CHEI 187
F flow processes looking up codes 7 overview 6 reversing 197 sequence 7 time-stamping in CHOF 257 time-stamping in CHRF 89

freight-type orders 300
H
HATO (Holds Auto Take-Off) 176
HOAD (Hold Adjustments)
adjusting hold code only 177 overview 169 placing inventory on hold 170 removing inventory from hold 173
Hold Adjustments (HOAD)
adjusting hold code only 177 overview 169 placing inventory on hold 170 removing inventory from hold 173 holds looking up off hold date 175 massive 177 on selected inventory 169 overview 169 removing 173
Holds Auto Take-Off HATO) 176 inspection orders 282 in-transit receipts 53 location capacity, looking up in LOLO 139 location codes, entering on the fly in ENRE 31
LOEN (Look Up Entity Information)
alternate type code and alternate item code 135
Drill Block 122
Header Block 114
History Block 128
History Details Block 131
History Remark Block 133
Location Block 124
Renewal Block 133
LOLO (Look Up Location Information) 136
Look Up Entity Information (LOEN)
Drill Block 122
Header Block 114
History Block 128
History Details Block 131
History Remark Block 133
Location Block 124
Renewal Block 133
Look Up Location Information (LOLO) 136
Look Up Orders (LOOR) 245
Look Up Pending Receipts (LOPR) 55
Look Up Receipts (LORE) 71
Look Up Telephone Numbers (LOTE) 70 looking up inventory 114 looking up locations 136 look-up programs 67
LOOR (Look Up Orders) 245
LOPR (Look Up Pending Receipts) 55
LORE (Look Up Receipts) 71
LOTE (Look Up Telephone Numbers) 70
M
MAHO (Take Off Holds) 181
MAOE (Manual Order Entry) 228
MARL (Massive Relocate) 165
Massive Adjustment (MATR) 154 massive adjustments 154 massive holds 177
Massive Relocate (MARL) 165
MATR (Massive Adjustment) 154
MOHO (Move Hold to Hold) 184
N non-inventory orders 300 non-standard weights, adjusting 189
O operations flow process 6 order documents See printing order documents orders adding to the VICS bill of lading 273 assigning locations 216 assigning multiple locations to a line block record 221 broker type 303
Carrier Block 226 changing default sort sequence 249 clearing out all inventory 302 confirmation date, changing in CHCD 264 confirming in CHOF 257 confirming in COOL 261 deleting entire line 238 deleting entire order 237 deleting Location Block data 240 distribution-type 284 entering Header Block information 203 entering Line Block information 210
Extended Remarks Block 225 freight-type 300 header types 241 inspection type 282 line types 241 looking up in LOOR 242 looking up item summary 249 manual order entry in MAOE 228 modifying Header Block data 229 modifying Line Block data 230 modifying Location Block data 232 modifying optional blocks data 233 non-inventory 300 overview 200 pending versus regular 211 picking to clean 302 printing documents for See printing order documents
P-type lines vs. R-type lines 211 querying on inventory levels 218
Remark Block 224 removing from the VICS bill of lading 273 requeuing a range 280
R-type lines vs. P-type lines 211 transfer type 290
