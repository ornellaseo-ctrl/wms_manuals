---
title: "Inventário Físico (Physical Inventory)"
description: "Parâmetros, tickets, entrada de contagens, reconciliação e relatórios de inventário físico."
layout: default
---

# Inventário Físico (Physical Inventory)

Parâmetros, tickets, entrada de contagens, reconciliação e relatórios de inventário físico.

**Fluxo principal:** `ENPH -> PHTI -> PPIT -> ENTI -> PHUP`

> Fonte: manuais F do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction And Overview <a id="introduction-and-overview"></a>

*Manual F — Physical Inventory*

# Manual F — Physical Inventory Guide (Inventário Físico)
> **ID do Manual:** F  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Inventário físico completo: parâmetros (ENPH), criação de tickets (PHTI), impressão (PPIT), entrada de tickets (ENTI), reconciliação e atualização (PHUP), relatórios (PHRE/PHTL/PIAR/BKDT/BOOK/TIDE). Processos de freeze/thaw do armazém.
---
---

### Overview <a id="overview"></a>

There are two types of physical counts in AccellosOne 3PL:
▪ blind counts
▪ non-blind counts
Blind counts generate one ticket for each location in your warehouse(s). Each ticket will show the ticket number and location code. The customer code will also be shown unless you select .ALL as your customer. 
No item codes or inventory levels will appear on the ticket. If you use preprinted tickets for your physical, you must perform a blind count. You cannot perform a non-blind count using preprinted tickets. 
Non-blind counts generate one ticket for each physical inventory unit* in each location (that is, multiple tickets for the same location if you have mixed product in that location). Each ticket for a non-blind count will show the ticket number, customer code and location code. As well, the item code and/or inventory levels and quantities will be shown depending on the options that you select when setting up your physical.
* A physical inventory unit in AccellosOne 3PL is defined as all product belonging to the same customer, placed in the 
same warehouse and location with the same level 1, level 2, level 3 and level 4 values, and assigned the same hold code. 
For example, if you placed two pallets of identical product in the same location and then placed one pallet on a damaged hold and left the other pallet with no hold, you would have two physical inventory units on your system for that location:
1) item 1/lot A/warehouse 1/location 101 + damaged hold
2) item 1/lot A/warehouse 1/location 101
There are two types of tickets in AccellosOne 3PL:
▪ non-blank tickets (the default)
▪ blank tickets
Regular or non-blank tickets show the ticket number, location and warehouse. If you specify a customer, the customer code will also be shown on the ticket; if you select .ALL as your customer, no customer is shown. 
Depending on which Show flags you set to Yes, the item, inventory levels and quantity will also be printed. 
Blank tickets, on the other hand, show the ticket number and customer code only (no customer is shown if you select .ALL as your customer); no location is printed on the ticket. Blank tickets are extra tickets that you use to count inventory found in the wrong location or in an unexpected location.
There are eight main steps to follow in performing a physical:
Ticket Location Warehouse Quantity |
---------------------------------------------------------------------| 
1 A100 1 |
---------------------------------------------------------------------| 
CUST1 Customer 1 | 
 | 
 | 
 | 
Ticket Location Warehouse Quantity | 
---------------------------------------------------------------------|
1 A100 1 |
---------------------------------------------------------------------| 
CUST1 Customer 1 | 
 | 
ITEM-1 Item 1 | 
 | 
101 | 
Ticket for blind count Ticket for non-blind count showing item and lot number-e 
---

REPORT
ENPH
PHTI
RFPH
BOOK or
BKDT
PHUP
You run one inventory report and one location report for the customer(s) 
included in the physical.
You define the parameters for your physical.
You generate your tickets.
You print your tickets.
If you are performing a dual count, you reconcile your A and B counts.
You run the Physical vs. Book report(s) 
to find out the variances between your physical and your book. 
You perform the physical to book update.
You compare the on-hand quantity of an inventory report like INHK to the total physical count to ensure that the two figures match.
REPORT
You perform the count using an RF device OR you perform the count manually.
PPIT
ENTI
You perform the count.
You enter your counts.
TIDE-e 
---

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting reports
Introduction Guide logging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating product, entering hold adjustments
Operations 2 Guide appointment planner, back orders, batch picking, manual packing, customer relationship management, EDI, faxing and auto-printing, item substitution, kitting, labor tracking, Operational Board, pallet control, inventory attributes, item process values, outbound load building, quick response labels
Physical Inventory 
Guide setup and operational programs for physical inventory as well as the physical inventory reports
RF Guide setup programs for RF (Radio Frequency), RF receiving, RF picking, entering process values in RF, voice-activated picking, order assignment system, equipment tracking, tasking, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager-e 
---

### Before You Begin <a id="before-you-begin"></a>

▪ You must have an adjustment type code set up in ADJU (Adjustment Type Codes) to use for physicals. 
Refer to the Setup Guide for instructions on setting up an adjustment type code.
▪ You must have a document set up in DOCU (Documents) to print your tickets. If you do not have a ticket printing document on your system, refer to the section [Physical Inventory Tickets Document (DOCU)](inventario-fisico.html#physical-inventory-tickets-document-docu) for information on how to set one up.
▪ You must print one inventory report and one location report for the customer(s) included in your physical. These reports are essential reference should it become necessary to investigate discrepancies in your physical to inventory update.

### Open Receipts and Orders <a id="open-receipts-and-orders"></a>

Open receipts during a physical are relatively safe if the receipt is not confirmed during the physical. Leave the receipt on the dock and make sure that its status remains “Enter Receipt.” Then perform your physical without counting the product on the receipt.
Open orders during a physical are very risky and must be managed with extreme care. The two major problems that occur with open orders are:
▪ product is not counted because it was picked during the physical
▪ orders cannot be confirmed because the new book quantity after the physical is less than the order quantity 
The product not counted problem is manageable if handled with care. For example, suppose you start a physical and then get an urgent order for 100 cases. Location A101 contains 100 cases and you decide to pick the order from this location. When you do your physical, you must count 100 cases for location A101 even though the location is now empty. If you do not count 100 cases for that location, your physical value will be 0 and your book value will be 100. This will lead to a “loss” of 100 cases for that item when you perform your physical to inventory update.
The inability to confirm orders because of lack of inventory is far more serious. For example, if you enter an order for 100 cases but during the physical you find only 90 cases, you should not perform the physical to inventory update. If you do, you will be unable to confirm the order because there is now insufficient product. 
If there is sufficient product for the order but it is not in the locations that were assigned to that order, the same problem will occur. You will not be able to confirm the order because the system will think that there is insufficient product.
When the order quantity is greater than the book quantity as a result of a physical, there are three possible solutions:
CAUTION It is strongly recommended that you confirm and fully process all your orders and receipts before performing a physical. It is possible to perform a physical inventory with open orders and receipts, but such physicals are risky and must be managed with care. Refer to the following section for special instructions.-e 
---

▪ you can delete the entire order
▪ you can delete the order line
▪ you can adjust the order quantity

### Adding New Inventory by Means of a Physical <a id="adding-new-inventory-by-means-of-a-physical"></a>

You can use the physical inventory programs to add new product to a warehouse (for example, you are adding a new customer or a new warehouse to your system). First, you set up your customer and items in 
CUST and ITEM. Then you add your inventory information such as locations and balances by means of the physical. 
If you use AccellosOne 3PL for billing, no initial storage will be charged for the new inventory. However, renewal storage will be charged effective the date of the physical inventory.
TIP Before starting your physical, pick all orders and mark their locations so that you can enter a count for that location. Then, before you perform the physical to inventory update, confirm the open orders. These two procedures will avoid the vast majority of problems that occur with open orders.-e 
---

## Physical Inventory Operations <a id="physical-inventory-operations"></a>

*Manual F — Physical Inventory*

---

### Setting Up Your Physical <a id="setting-up-your-physical"></a>

You set up your physicals in ENPH (Enter Physical Parameters). The main parameters that you define in 
ENPH are:
▪ the customer or customers whose inventory you wish to count
▪ the physical type (single team count or dual team count)
▪ whether or not to allow duplicates per location (that is, allow entry of two or more tickets for the same inventory entity in the same location)
▪ whether the physical is blind (Show flags = No) or not blind (Show flags = Yes)
▪ the adjustment code for the physical (when you run your physical to inventory update, any adjustments that you make will be assigned this adjustment code)
▪ the sort sequence for your physical inventory tickets
If you set your Show Item/Level 2/3/4 flags to Yes, you can specify whether or not to count empty locations.
The parameters that you define in ENPH (Enter Physical Parameters) are for a single physical only. The next time that you want to run a physical, you must re-enter ENPH and redefine your physical inventory parameters.
When you finish defining your parameters, AccellosOne 3PL generates a physical number for the physical. 
You use this number when you generate your tickets in PHTI (Create Physical Inventory Tickets) and in all other physical inventory programs. 
NOTE The physicals that you create in ENPH remain inactive until you run PHUP (Physical to Inventory Update). When you run PHUP, the changes are permanent and cannot be undone. Therefore, you can create as many physicals as you wish in 
ENPH for training or testing purposes without any danger to your system. When your training or testing is complete, you can delete the physicals.-e 
---

FIELD DESCRIPTIONS
Customer Code Mandatory
The customer for whom the physical inventory will be conducted. The customer that you enter in this field will determine the number of inventory levels displayed (for example, Show Item Code on Ticket, Show Lot Number on 
Ticket, etc.).
If you wish to perform a physical for multiple customers, use the .ALL option.
Document Code Mandatory
The document code for your physical inventory tickets (usually PHTI). You can have multiple document codes on your system if this is required to meet the different needs of your customers.
Refer to the section [Physical Inventory Tickets Document (DOCU)](inventario-fisico.html#physical-inventory-tickets-document-docu) for further information on setting up this document.-e 
---

Type of Count A = Single Count
B = Double Count
If you are using only one team to count your inventory, select option A. If you are using two teams to make two separate counts of your inventory, use option B.
Physical Inventory Date Mandatory
The date on which you will actually perform the physical. This date need not be the same as the date on which you set up the physical in ENPH. For example, you can set up the physical on a Friday and make the physical inventory date Saturday.
This date serves two functions when you update your inventory. First, any adjustments made will be assigned the date that you enter in this field. Second, if you find new inventory during a physical, the date that you enter in this field will be the effective date used to charge for renewal storage.
Allow Duplicates per 
Location
N = No
Y = Yes
If you specify No, the system will not allow you to enter multiple tickets for the same physical inventory unit in ENTI (Enter Tickets) or RFPH (RF Physical 
Count). A multiple ticket means two or more tickets for the same physical inventory unit in the same location. 
If you specify Yes, the system will allow you to enter multiple tickets for the same physical inventory unit. The Yes option is intended for two situations: 
you have a bulk location where the same inventory entity might be scattered around in different places or you allow mixed product in the same location. 
NOTE A physical inventory unit in AccellosOne 3PL is defined as all product belonging to the same customer, placed in the same warehouse and location with the same level 1, level 2, level 3, level 4 values and the same hold code. For example, if you placed two pallets of identical product in the same location and then placed one pallet on hold and left the other pallet with no hold, you would have two physical inventory units on your system for that location:
1) item 1/lot A/warehouse 1/location 101 + hold X
2) item 1/lot A/warehouse 1/location 101
FIELD DESCRIPTIONS-e 
---

Item Entry Mask Only available for blind counts
If all or a majority of your item codes begin with the same character or characters, you can use an entry mask to facilitate data entry by eliminating the need to enter redundant characters.
For example, if all your item codes for a particular customer started with 0 (06433A, 07663J, etc.), you could use 0 as your entry mask. When you keyed in your item codes in ENTI (Enter Tickets), you would omit the leading zero from the code. AccellosOne 3PL would automatically add the zero to your item codes.
Show Item/Level 2/3/4 on 
Ticket
N = No
Y = Yes
The number of inventory levels displayed depends on the customer that you select in the Customer Code field. If you specify No, the inventory level will not be printed on the ticket. If you specify Yes, the inventory level will be printed on the ticket. 
For customers with two or more inventory levels, if you select No at one inventory level, all inventory levels “lower” than that level (that is, a higher number) 
will be automatically set to No. This restriction does not apply to the Yes option; that is, you can set lower inventory levels to either Yes or No.
Show Inventory Quantity on Ticket
Yes option only available if Show Level 2/3/4 flag = Yes
N = No
Y = Yes
If you specify No, no inventory quantity will be printed on the ticket. If you specify Yes, the inventory quantity will be printed on the ticket. Inventory quantities do not display in ENTI.
FIELD DESCRIPTIONS-e 
---

Flag Ticket Quantity as 
Entered
Yes option only available if Show Level 2/3/4 flag and the Show Inventory 
Quantity on Ticket flag have been set to Yes
N = No
Y = Yes
If you set this flag to Yes, the RF operator in RFPH or the office operator in 
ENTI will not be required to enter a count for the ticket; the system count will be deemed to be correct and the only requirement for the operator is to navigate through the ticket by means of arrow keys or the F9 (previous field) command. If you set this flag to No (default value), the operator must enter the quantity in either RFCH or ENTI.
Clear Non-Ticketed 
Inventory
N = No
Y = Yes
Non-ticketed inventory refers to inventory belonging to the customer you are doing the physical for that was not recorded on a ticket.
If you specify Yes, any existing inventory that was not on a physical Inventory ticket will be zeroed out when you run PHUP. If you specify No, any non-ticketed existing inventory will not be zeroed out by PHUP.
Ignore Blank Quantity 
Tickets
N = No
Y = Yes
Blank quantity tickets are tickets for which the following conditions have been met:
▪ no quantity was entered for a ticket with all inventory levels entered
▪ a blank ticket was generated in PHTI and was not updated in ENTI or RFPH
▪ the ticket has NOT been cleared using the Clear Ticket command
If you specify Yes, blank quantity tickets will be ignored in the PHUP process. 
If you select No, PHUP will not run until the physical ticket is fully entered or the ticket has been cleared. 
Starting Ticket Number Mandatory
The ticket number that you wish to start from. If you are using preprinted tickets, you enter the starting number from your printed tickets in this field.
FIELD DESCRIPTIONS-e 
---

Include Empty Locations Only available if one of the Show Item Code or Show Inventory Level fields is set to Yes.
N = No
Y = Yes
An empty location in AccellosOne 3PL is a location with an on-hand quantity of 0 for the customer or customers you specify in the Customer Code field. It may contain no product at all or it may contain product belonging to other customers.
If you specify No, only locations with an on-hand quantity of greater than 0 for the customer(s) that you specify will have tickets printed for them. If you specify Yes, the system will print tickets for all locations — that is, locations with an on-hand quantity of greater than 0 for the customer(s) you specify as well as locations without any product for the customer(s) that you specify. 
Adjustment Code (defined in ADJU)
Mandatory
The adjustment code that you enter in this field is defined in ADJU (Adjustment Type Codes). When you run PHUP (Physical to Inventory Update), any adjustments to inventory that are required will be assigned the adjustment code that you specify in this field.
Sort Sequence Code (defined in SOSE)
Optional
This field allows you to customize the sort sequence of your locations so that tickets are printed in an order that makes sense for your warehouse. Refer to 
See [Defining the Sort Sequence of Your Locations](inventario-fisico.html#defining-the-sort-sequence-of-your-locations) for further information.
Warehouse Code Optional
If you enter a warehouse code in this field, the physical will be restricted to inventory in that warehouse.
Alternate Reporting Type (defined in ITAS)
Optional
If specified, only those items with the alternate reporting type that you enter in this field will be included in the physical.
FIELD DESCRIPTIONS-e 
---

### CREATING A PHYSICAL <a id="creating-a-physical"></a>

1 Enter ENPH.
2 Click on Create Record.
3 Key in your customer code and press Enter.
You can use your pick list (press F10 to enter the pick list, click on Execute Query to query and then click on Select to select) or you can use .ALL to select multiple customers.
When you select your customer, the system will display the number of inventory levels that you have defined for that customer in DILP (Depositor Inventory Level Profile).
Enter Physical Parameters (ENPH) screen for a customer with two inventory levels
4 Key in your document code and press Enter or use your pick list to select it.
Alternate Reporting Code Optional
If specified, only those items with the alternate reporting code that you enter in this field will be included in the physical.
FIELD DESCRIPTIONS-e 
---

The document code that you enter in this field is the document that was set up for you in DOCU (Documents) for printing your tickets.
5 Key in your type of count (A for a single count or B for a double count) and press Enter.
6 Key in your physical inventory date and press Enter or press Enter to accept the current system date. 
The date that you enter in this field will be the date used for any adjustments to inventory that are made as a result of the physical.
7 Key in your Allow Duplicates in Location option (Y for Yes or N for No) and press Enter.
8 If required, key in an item code entry mask and press Enter or press Enter with the field blank to bypass this option.
9 In the Show Item Code on Ticket field, key in Y for Yes or N for No and press Enter. If you specify Yes, the item code will be printed on the ticket. If you specify No, no item code will be printed on the ticket. You use the No option if you wish to perform a blind count or if you are using your own preprinted tickets.
10 If the customer that you selected in step 3 has multiple inventory levels, you must specify for each inventory level whether you want the value for that inventory level to print on the ticket.
11 In the Show Inventory Quantity field, key in Y for Yes or N for No and press Enter. If you are performing a blind count (that is, all your Show flags are set to No), the value that you enter in this field will be ignored and no inventory quantity will print on the ticket.
12 If prompted to do so, in the Flag Ticket Quantity as Entered field, key in Y for Yes or N for No and press 
Enter.
13 In the Clear Non-Ticketed Inventory field, key in Y for Yes or N for No and press Enter.
14 In the Ignore Blank Quantity Tickets field, key in Y for Yes or N for No and press Enter.
15 In the Starting Ticket Number field, key in the ticket number that you wish to start from and press Enter.
16 If prompted to do so, key in Y for Yes or N for No in the Include Empty Locations field and press Enter.
This field is only available if one of the Show Item Code or Show Inventory Level fields is set to Yes.-e 
---

Enter Physical Parameters (ENPH)
17 In the Adjustment Code field, key in your adjustment code and press Enter or use your pick list to select the appropriate code.
The adjustment code that you enter in this field is defined in ADJU (Adjustment Type Codes). When you run PHUP (Physical to Inventory Update), any adjustments to inventory that are required will be assigned the adjustment code that you specify in this field.
18 If required, key in your sort sequence code in the Sort Sequence Code field and press Enter or press 
Enter with the field blank to bypass this option.
19 If required, key in your warehouse restriction and press Enter or press Enter with no warehouse restriction to bypass this option.-e 
---

20 If required, key in an alternate reporting type and press Enter or press Enter to bypass this field. You use alternate reporting types if you wish to perform a physical limited to certain items only. If you enter an alternate reporting type, you must also specify an alternate reporting code.
The header portion of ENPH will appear and a system-generated physical number is assigned to the physical. You will use this number in the other physical programs to print your tickets, enter your physical counts, update your inventory, etc. 
21 Click on Exit to exit ENPH.
22 Proceed to next step (PHTI) to generate your tickets.

### MODIFYING A PHYSICAL <a id="modifying-a-physical"></a>

If you have created a physical in ENPH but not generated your tickets in PHTI, you can change any field in 
ENPH except Customer Code. Once you generate your tickets in PHTI, the only fields that you can modify in 
ENPH are the following:
▪ Document Code
▪ Physical Inventory Date
▪ Item Entry Mask
▪ Starting Ticket Number
1 Enter ENPH.
2 Key in the physical number and press Enter. 
If you specified a specific customer in the Customer Code field:
If you specified .ALL in the 
Customer Code field, the 
Customer Block will be displayed:
a) Proceed to next step. a) Press F10 to activate the pick list then click on Execute Query to activate the query.
b) Using your arrow keys to position the cursor beside the appropriate customer, click on Select Code to select a given customer and click on Deselect Code to deselect a customer.
c) When you finish selecting your customers, click on Previous 
Form to display the Customer 
Block.
d) In the Customer Block, press 
Enter once for each customer that you selected in the pick list.
e) When you have accepted each customer, click on Return to 
Main and Return to return to 
ENPH.-e 
---

3 When the ENPH record that you specified is displayed, press Enter until you reach the field that you wish to modify.
4 Key in your change and press Enter.
5 Click on Return to Main and Exit to exit.

### DELETING A PHYSICAL <a id="deleting-a-physical"></a>

Once you have run your physical (that is, generated and printed the tickets, entered your counts and performed the physical to inventory update) and you are satisfied with the results, you should delete it after a reasonable period of time. If you do not delete your physicals, they will take up space in your database and your system performance may suffer.
1 Enter ENPH.
2 Key in the physical number and press Enter. 
3 When the ENPH record you specified is displayed, click on Delete to delete the record.
4 Click on Return to Main and Exit to exit.

### CANCELLING A PHYSICAL <a id="cancelling-a-physical"></a>

The physicals that you create in ENPH remain inactive until you run PHUP (Physical to Inventory Update). 
When you run PHUP, the changes are permanent and cannot be undone. Therefore, you can cancel a physical at any stage in the process up until the time that you run the physical to inventory update. For example, you could create a physical in ENPH, generate and print tickets for it and then enter your counts. If at this point you decided to cancel the physical because some of the parameters were wrong, you would delete the physical in ENPH and then start all over again. 

### DEFINING THE SORT SEQUENCE OF YOUR LOCATIONS <a id="defining-the-sort-sequence-of-your-locations"></a>

If necessary, you can customize the sort sequence or “snaking” of your locations. If you do not specify a sort sequence, your tickets will be generated in alphanumeric order (for example, locations A101, A102, A103, 
B101, B102, etc.).
Special sort sequences must be set up in SOSE (Sort Sequence Code) before they can be used. 
CAUTION If you run a physical and you are not satisfied with the results, you must not delete the physical in ENPH. HighJump’ technical support staff will need to see your physical in order to determine what went wrong. If your physical has been deleted, it will be impossible to identify the problem and work out an effective solution.-e 
---

### Generating Your Physical Inventory Tickets <a id="generating-your-physical-inventory-tickets"></a>

You generate your physical inventory tickets in PHTI (Physical Inventory Tickets) based on the parameters that you set up in ENPH.
You can generate two types of tickets in PHTI:
▪ non-blank tickets 
▪ blank tickets 
If you are using your own preprinted tickets, you must still run PHTI to generate your tickets but you will not print your tickets in PPIT.
Non-blank tickets show the ticket number, customer code and location. Depending on the parameters that you select in ENPH, they also show the item code, inventory level and quantity. Blank tickets, on the other hand, show the ticket number and customer code only. There is no location, item code or quantity. Blank tickets are extra tickets that you use to count inventory found in the wrong location or in an unexpected location. As well, you can use blank tickets to record multiple entities in the same location.
If you set the wrong parameters in PHTI and as a result generate tickets that you do not wish to use, you cannot delete the job in PHTI. You must delete the physical in ENPH and create another physical.
Tickets generated in numerical order (location 
101, 102, 103, 104, etc.)
Tickets generated using a custom sort sequence (location 103, 106, 109, 112, 111, 
108, etc.)
NOTE If you wish to generate both non-blank and blank tickets for the same physical, you must do so in two separate batches. For example, first you run PHTI for your non-blank tickets and print the tickets using PPIT. Then you rerun PHTI for your blank tickets and return to PPIT to print your second batch. You cannot generate both types of tickets in the same job.
103 106 109 112
102 105 108 111
101 104 107 110
103 106 109 112
102 105 108 111
101 104 107 110-e 
---

### RUNNING PHTI IN BATCHES <a id="running-phti-in-batches"></a>

PHTI can be run in separate batches if you are generating non-blank tickets; for example, batch 1 could be locations in warehouse 1, batch 2 could be locations in warehouse 2, batch 3 could be locations with a location type of COOLER, etc. PHTI supports up to five parameters for your batches: warehouse, location bill code, location type, location code and isolator code. If you do not wish to generate tickets in separate batches, you can run PHTI in a single batch — that is, all locations regardless of warehouse, location type, etc.
If you rerun PHTI to generate separate batches of non-blank tickets, only those tickets that do not result in duplicates will be generated. For example, if you run PHTI with warehouse 1 as your warehouse parameter and then rerun PHTI with the same parameter, no tickets will be generated the second time as this would result in duplicates. However, you can rerun PHTI a second time with warehouse 2 as your warehouse parameter and tickets for all your warehouse 2 locations will be generated.
If you rerun PHTI to generate separate batches of blank tickets, no such restriction applies. You can rerun 
PHTI at any time to generate as many additional blank tickets as you require. 
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical that you wish to generate tickets for.
Number of Blank Tickets Optional
The number of extra blank tickets (if any) that you want to print. The blank tickets that you create in this field show the customer code and ticket number only; there is no location, no quantity and no item codes or inventory levels on them. You use this option to count product that has no location or has been placed in the wrong location. You can also use blank tickets to record multiple entities in the same location.-e 
---

Number of Non-Blank 
Tickets per Location
Only available for blind counts (that is, all your Show flags in ENPH are set to 
No).
In this field, you specify the number of non-blank tickets (that is, location plus whichever inventory levels you specified in ENPH) you want to print for each location.
If you do not wish to create a fixed number of extra tickets for each location in your warehouse, you can set this field to 1 and print an appropriate number of blank tickets for those locations with mixed product.
If you never place mixed product in the same location, enter 1. If you do place mixed product in the same location, enter the appropriate number (for example, 3 if you allow up to three different entities in the same location).
Warehouse Code (defined in WARE)
Only available if you did not specify a warehouse restriction in ENPH.
If you specify a warehouse, only tickets for locations in that warehouse will be generated.
Location Bill Code (defined in LODE)
Optional
If you specify a location bill code defined in LODE, only tickets for locations that have been assigned that location bill code will be generated.
Location Type Code (defined in LOTP)
Optional
If you specify a location type code defined in LOTP, only tickets for locations that have been assigned that location type code will be generated.
Location Code (defined in LOCA)
Optional
If you enter a location code defined in LOCA, only tickets for that location will be generated. You can specify a range of locations by using the percent sign (%) as your wildcard character. For example, to specify all locations in your A1 aisle (A100, A101, A102, A103, etc.), you would key in A1%. 
FIELD DESCRIPTIONS-e 
---

### GENERATING NON-BLANK TICKETS <a id="generating-non-blank-tickets"></a>

Non-blank tickets will show a ticket number, customer code and location. Depending on which of the Show flags you set to Yes in ENPH, item codes and/or inventory levels plus quantities will also be printed.
1 Enter PHTI.
2 Key in your physical number and press Enter.
3 Press Enter to bypass the Number of Blank Tickets field.
4 In the Number of Non-Blank Tickets per Location field, key in the number of non-blank tickets that you require for each location and press Enter.
Isolator Code (defined in ISOL)
Optional
If you specify an isolator code defined in ISOL, only tickets for locations that have been assigned that isolator code will be generated.
If you set up a blind count in 
ENPH:
If you set up a non-blind count in 
ENPH:
a) If you never place mixed product in the same location, enter 1 to print a single ticket per location. 
If, on the other hand, you do place mixed product in the same location, enter the number of inventory entities that you allow per location.
For example, if you have a single entity in a location, the system will print one ticket for that location. If you have multiple entities in a location, the system will print one ticket per entity.
a) Key in 1 and press Enter to bypass this field. The number of tickets printed per location will depend on the number of entities in the location — not on the value that you enter in this field. 
FIELD DESCRIPTIONS-e 
---

PHTI screen showing 1 as the number of non-blank tickets per location 
5 Set the parameters for your batch. If you wish to produce all your tickets in a single batch without setting any parameters, press Enter on each field to bypass it and proceed to step 6.
6 When you have specified all your parameters, click on Create Tickets to generate your tickets.
7 If you are generating your tickets in batches, print your first batch in PPIT before you proceed to generate your second batch.

### GENERATING BLANK TICKETS <a id="generating-blank-tickets"></a>

Blank tickets will show a ticket number and customer code only but no location. You can generate as many blank tickets as you need and you can rerun PHTI as often as required to generate additional blank tickets.
1 Enter PHTI.
2 Key in your physical number and press Enter.
3 In the Number of Blank Tickets field, key in the number of blank tickets that you require and press Enter. 
4 Click on Create Tickets to generate your tickets.

### Printing Your Physical Inventory Tickets <a id="printing-your-physical-inventory-tickets"></a>

You print the physical inventory tickets that you generated in PHTI in PPIT (Print Physical Inventory Tickets). 
In order to print your tickets, you need a print ticket document set up in DOCU (Documents). If you do not -e 
---

have such a document on your system (usually called PHTI), refer to the section [Physical Inventory Tickets 
Document (DOCU)](inventario-fisico.html#physical-inventory-tickets-document-docu) for further information on setting up this document.
This program is not used if you enter your counts using an RF device or if you use preprinted tickets.

### PRINTING NEW TICKETS <a id="printing-new-tickets"></a>

When you print tickets for the first time, you must print all tickets. You cannot print a range of tickets or tickets belonging to a particular type (A count or B count).
1 Enter PPIT.
2 Key in your physical number and press Enter.
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical that you wish to print tickets for. 
Reprint Tickets Only available if you have printed all tickets at least once and the Allow 
Reprint flag in DOCU is set to Y for Yes.
N = No
Y = Yes
If you specify Yes, you can reprint physical inventory tickets. 
Type of Count Only available when reprinting tickets.
A = A Count
B = B Count blank = A and B
The type of count whose tickets you are reprinting.
From Ticket Number Only available when reprinting tickets.
Your starting ticket number for reprinting tickets. 
To Ticket Number Only available when reprinting tickets.
Your ending ticket number for reprinting tickets. -e 
---

Print Physical Inventory Tickets (PPIT) for physical # 104
3 Click on Execute Report.
4 Key in your printer code and press Enter.
5 Click Ok to print.
6 When printing is complete, click on Exit to exit PPIT.

### REPRINTING TICKETS <a id="reprinting-tickets"></a>

If you have printed all your tickets and if the Allow Reprint flag in DOCU has been set to Y for Yes for your physical inventory tickets document, you can reprint tickets as many times as you wish. You can reprint all tickets or a specified range of tickets. 
1 Enter PPIT.
2 Key in your physical number and press Enter.
3 In the Reprint Tickets field, key in Y for Yes and press Enter.
4 In the Type of Count field, key in the appropriate value (A for your A count only, B for your B count only or blank for both your A and B count) and press Enter.
5 Do one of the following:
6 Click on Execute Report.
If you wish to specify a range:
If you do NOT wish to specify a range:
a) Key in your starting number and press Enter.
b) Key in your ending number and press Enter.
a) Proceed to next step.-e 
---

7 Key in your printer code and press Enter.
8 When printing is complete, click on Exit to exit PPIT.

### Entering Your Physical Counts <a id="entering-your-physical-counts"></a>

You enter your physical counts in ENTI (Enter Tickets/Count Sheets). If you set your Show flags in ENPH to 
No in order to perform a blind count, you must enter an item code, all inventory levels and a quantity for each ticket. If you set your Show flags in ENPH to Yes, your item codes and lot numbers, etc. will already be entered and you input the quantity only.
You can input your tickets in batches and re-enter ENTI as many times as required in order to add another batch or correct or update your ticket count, item code, lot number, warehouse code or hold code. For example, you can count aisle 1 and enter your aisle 1 counts, then count aisle 2 and enter your aisle 2 counts, and continue in this manner aisle by aisle.
There are four scenarios that you may encounter when entering your tickets:
If … then … there is no product in a location enter a count of zero or clear the ticket the right product is found in a location that was not included in the physical use a blank ticket to enter the product product is found whose level 2, 3 or 4 value does not match any level 2, 3 or 4 values for that item already on the system you may be prompted to enter a description or expiry date for that inventory level product belonging to a customer not included in the physical is found in a location (for example, the physical is for Customer A and location 101 is a 
Customer A location, but you find product for Customer B in that location)
Enter a count of zero or clear the ticket because there is no product for Customer A in the location. 
Then check LOLO or LOEN to see whether Customer B’s product belongs in the location. If necessary, make a manual adjustment for Customer B’s product.
NOTE You must enter a count for each ticket in ENTI for which you have inventory. 
If you fail to enter all your counts, AccellosOne 3PL may assume a quantity of zero for the inventory not counted when you run the physical to inventory update in PHUP.
If you want to perform a “partial physical,” you must use the Alternate Reporting Type field in ENPH to specify those items that you wish to count.-e 
---

If you set up a dual count in ENPH (Enter Parameters), you must input ENTI twice: once for your A count and once for your B count.
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical that you wish to generate tickets for.
Starting Ticket Mandatory
Your starting ticket number. 
Ending Ticket Mandatory
Your ending ticket number. You can improve system performance by entering your ENTI counts in batches of 50 or 100. For example, if your starting ticket number is 100, you can enter a batch of 50 by making your ending ticket number 150.
Type of Count A = A Count
B = B Count
The count whose tickets you are entering.
Item Code Mandatory for blind counts
Your item code.
Level 2/3/4 Mandatory for blind counts if the customer whose inventory you are counting has two, three or four inventory levels.
Your level 2/3/4 values.
Location Mandatory for blank tickets only
Your location code.-e 
---

### ENTERING A BLIND COUNT <a id="entering-a-blind-count"></a>

You use this procedure if you have set all your Show flags to No in ENPH.
1 Enter ENTI.
2 Key in your physical number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your type of count (A or B) and press Enter.
Warehouse Mandatory for blank tickets only
Your warehouse code.
Hold Mandatory for blank tickets only
If you wish to correct a hold code that was entered incorrectly for a non-blank ticket, press F9 to jump back to the Hold field and key in your correct code.
Count Mandatory
The number of pallets, cases, etc. for the inventory entity.
TIP You can improve system performance by entering your tickets in batches. You enter your tickets in batches by specifying an ending ticket number in the Ending 
Ticket field. For example, if your starting ticket number is 100, you can enter a batch of 50 by making your ending ticket number 149.
FIELD DESCRIPTIONS-e 
---

Enter Tickets/Count Sheets (ENTI) for a blind physical
6 Key in the item code for your first ticket and press Enter. If you have no product for that location, click on 
Clear Ticket.
7 If required, key in your level 2, 3 and 4 values (lot number, production date, etc.) and press Enter.
If you make a mistake when entering a value, press F9 to jump back to the appropriate field and enter your changes.
8 Key in your count and press Enter. If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts. 
Regardless of the SKU code that you use, the Adjustment Process flag must be set to Yes in the SKU 
Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.
9 If you need to correct a hold code or inventory level, press F9 to jump back to the appropriate field and enter your changes.
10 Repeat steps 6 to 8 for each ticket.
11 If you are performing a dual count, repeat the count for your second count type (A or B).
12 When you finish entering your tickets, click on Return to Main and Exit to exit ENTI.

### ENTERING A NON-BLIND COUNT <a id="entering-a-non-blind-count"></a>

You use this procedure if you have set one or more of your Show flags to Yes in ENPH.
1 Enter ENTI.-e 
---

2 Key in your physical number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your type of count (A or B) and press Enter.
Enter Tickets/Count Sheets (ENTI) for a non-blind physical
TIP You can improve system performance by entering your tickets in batches. You enter your tickets in batches by specifying an ending ticket number in the Ending 
Ticket field. For example, if your starting ticket number is 100, you can enter a batch of 50 by making your ending ticket number 149.-e 
---

6 If you need to correct a hold code or a warehouse code, press F9 to jump back to the field that requires modification and key in the correct code.
7 Repeat the above steps for each ticket.
8 If you are performing a dual count, repeat the count for your second count type (A or B).
9 When you finish entering your tickets, click on Return to Main and Exit to exit ENTI.

### ENTERING A BLANK TICKET <a id="entering-a-blank-ticket"></a>

1 Enter ENTI.
2 Key in your physical number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your count type (A or B) and press Enter.
6 If required, cursor down to the blank ticket.
If the item code and inventory levels are correct: 
If the item code and inventory levels are NOT correct:
a) If the item code and inventory levels are correct (that is, the book value matches the physical value), key in your count and press Enter. 
▪ If you have no product for that location, key in a quantity of zero.
▪ If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.*
a) If the item code and inventory levels are NOT correct (that is, the book value does not match the physical value), click on 
Clear Ticket to clear the ticket. 
Then key in the correct item code and inventory level(s) plus your count and press Enter.
▪ If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.*
▪ If your item code is not accepted (for example, your count is for customer A and the item belongs to customer B), click on Clear Ticket to clear the ticket. 
Then use ENAJ to enter the correct item in the location.
 * Regardless of the SKU code that you use, the Adjustment Process flag must be set to Yes in the 
SKU Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.-e 
---

Enter Tickets/Count Sheets (ENTI) screen for blank tickets
7 Key in your location code and press Enter.
8 Key in your warehouse code and press Enter.
9 If required, key in your hold code and press Enter.
10 Key in your item code and press Enter.
11 If required, key in your level 2, 3 and 4 values and press Enter.
If you make a mistake when entering a value, press F9 to jump back to the appropriate field and enter your changes.
12 Key in your quantity and press Enter. If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.
Regardless of the SKU code that you use, the Adjustment Process flag must be set to Yes in the SKU 
Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.
13 Repeat steps 7 to 12 for each additional blank ticket that you wish to enter.
14 When you finish entering your blank tickets, click on Return to Main and Exit to exit.

### ADDING NEW INVENTORY <a id="adding-new-inventory"></a>

If you are adding new inventory during your physical (that is, the level 2, 3 or 4 value that you key in for your physical is not already on the system), you may be prompted to enter a level description and/or an expiry date. This prompt will only be displayed if one of the following conditions is met:-e 
---

▪ the Assign Description to New Entity flag in DILP (Depositor Inventory Level Profile) for the customer has been set to Yes for the inventory level whose value is not already on the system
▪ the Enter Expiry Dates flag has been set to Yes in ITSH (Item Shipping Profile) and that profile has been attached to the item whose inventory level value is not already on the system
If neither of these two conditions is met, the new product will be added to inventory but no screen will be displayed. If one or both of these conditions is met, the following screen will be displayed:
Enter Tickets/Count Sheets (ENTI) screen for an item requiring a level 2 description 
1 If a level description is required, key in your level description and press Enter. 
2 If an expiry date is required, key in your expiry date and press Enter.
3 Click on Ticket Block to exit to ENTI and enter the quantity for the ticket.

### CLEARING TICKETS <a id="clearing-tickets"></a>

You use the Clear Ticket function in the following two situations:
▪ the level 1, 2, 3 or 4 values are wrong and you wish to re-enter the information
▪ there is no inventory for the ticket
NOTE If you make a mistake when entering a level description or expiry date, you cannot overtype the wrong information. Instead, you must clear the ticket and then reenter it. Refer to the section [Clearing Tickets](inventario-fisico.html#clearing-tickets) for instructions on clearing a ticket.-e 
---

When you clear a ticket, the ticket is considered by AccellosOne 3PL to have been entered. The physical to inventory update will run and the quantity for the inventory in that location will be set to zero.
1 Enter ENTI.
2 Key in your physical number and press Enter.
3 Key in your starting and ending ticket numbers and press Enter.
4 Key in your type of count (A or B) and press Enter.
5 Using your arrow keys, cursor down to the ticket that you wish to clear.
6 Click on Clear Ticket.
7 Click on Return to Main and Exit.

### CHANGING THE LOCATION OF A TICKET <a id="changing-the-location-of-a-ticket"></a>

If the warehouse or location is wrong on a ticket, use the pick list function to select the correct location. You cannot key in a new location in the Location field.

### WORKING WITH ITEM MASKS <a id="working-with-item-masks"></a>

If some items do not begin with the entry masks characters, you can temporarily deactivate the entry mask in 
ENPH, enter your counts in ENTI for those items and then reactivate the entry mask in EMPH and resume your counts in ENTI for the entry mask inventory.

### Entering Your Counts With RF <a id="entering-your-counts-with-rf"></a>

If you are entering your tickets by means of an RF device, you use the program RFPH (RF Physical Count) 
instead of ENTI. The procedures for entering tickets, clearing tickets, correcting quantities and entities, etc., are similar in both programs. Refer to [Entering Your Physical Counts](inventario-fisico.html#entering-your-physical-counts) for full instructions on how to enter tickets in RFPH.
You can validate level numbers in RFPH if you activate level validation in MRFP (RF Profile Code). You activate level validation by entering the appropriate level number in the Validate Level Number field. For example, if you enter 2 in the Validate Level Number field in MRFP and level 2 is defined as lot number, you will not be able to enter a new lot number in RFPH. 
If you discover a new lot number during your physical and level validation is activated in MRFP, you will have to enter the ticket in ENTI instead of in RFPH.
Refer to the RF User’s Guide for further information on setting up MRFP.-e 
---

RF Physical Count screen
FIELD DESCRIPTION
PH# Physical Number
STI Starting Ticket
ETI Ending Ticket
CNT Count
TICK Ticket
CUST Customer
LOC. Location
WHSE Warehouse
HOLD Hold
L1 Level 1/UPC Code
If an item has been assigned a UPC code, you can enter or scan in an item’s 
UPC code and AccellosOne 3PL will retrieve the matching item code. RFPH first searches ITEM for a UPC code. If no code can be found in ITEM, RFPH searches ALIT (Alternate Item and Language) for a UPC code.
L2. Level 2
L3 Level 3
L4 Level 4
QTY Quantity-e 
---

### Reconciling a Dual Count <a id="reconciling-a-dual-count"></a>

If you set up a dual count in ENPH (Enter Parameters), you must input ENTI twice: once for your A count and once for your B count. After you have entered both counts, you must perform a reconciliation in TIDE (Ticket 
Discrepancy Report A vs. B). This report show all items where the A count differs from the B count. When 
TIDE is empty, this means that your A count and B count are identical and you are ready to run your book versus physical reports. 
Your cannot update your inventory until your A count equals your B count.
BK Breakdown
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Search for the records that meet the criteria that you specify.
F3 CQ (Count Tickets) Count the number of tickets.
F4 Rt (Return) Return to Main
Results Mode
F1 EN (Enter Ticket) Position the cursor in the STI field.
F2 CT (Clear Ticket) Clear wrong level 1, 2, 3 and 4 information so that you can re-enter your inventory levels.
F3 CQ (Count Tickets) Count the number of tickets.
F4 Rt (Exit) Switch to Main Mode.
F9 Previous Field Return to Hold or Whse field.
FIELD DESCRIPTION-e 
---

Ticket Discrepancy A vs. B Report (TIDE) 

### RUNNING TIDE <a id="running-tide"></a>

1 Enter TIDE.
2 Click on Enter Criteria.
3 Key in your physical number, customer code and physical inventory date restrictions and click on Execute Query.
4 If your query retrieves more than one physical, use your arrow keys to select the physical whose tickets you wish to print.
FIELD DESCRIPTIONS
Physical Number The number of the physical whose A and B count you wish to reconcile. 
Customer Code If you enter a customer code in this field, your query in TIDE will retrieve all physicals for that customer. If you leave this field blank, your query will retrieve all physicals regardless of customer.
Physical Inventory Date If you enter a physical inventory date in this field, your query in TIDE will retrieve all physicals with that physical inventory date. If you leave this field blank, your query will retrieve all physicals regardless of physical inventory date.
Location Code If you enter a location code in this field, the report will be restricted to that location. If you leave this field blank, the report will show inventory for all locations. 
You can use the wildcard character (“%”) report on a range of locations. For example, if you enter A%, TIDE will show all locations beginning with the letter 
A such as A100, A101, A102, A103, etc.-e 
---

Ticket Discrepancy Report A vs. B (TIDE)
5 Press Enter to position your cursor in the Location Code field.
6 Key in your location code restriction and press Enter or press Enter with this field blank to report on all locations.
7 Key in your printer code and press Enter.
8 Click Ok to print.
9 When the report is printed, note any discrepancies and recount those items to arrive at the correct count.
10 Re-enter ENTI and make any necessary corrections to either your A count or your B count.
11 Rerun TIDE to ensure that it is now empty.

### Updating Your Inventory <a id="updating-your-inventory"></a>

You perform your physical to inventory update in PHUP (Physical to Inventory Update). This update will perform the following:
▪ The quantities of existing inventory will be positively or negatively adjusted according to your A count and the adjustment will be assigned the physical inventory date and the adjustment code that you specified in ENPH. If you use AccellosOne 3PL for billing, any changes to billing because of a positive or negative adjustment to the quantity will take effect the next renewal date.
▪ Warehouse codes and hold codes of existing inventory will be updated if required.-e 
---

▪ New inventory that was found during the inventory will be added to your system. If you use AccellosOne 
3PL for billing, the renewal date for billing purposes of the new inventory will be the date that you specified as your physical inventory date in ENPH. 
▪ Inventory that could not be found during the physical will be assigned a quantity of zero. If you use 
AccellosOne 3PL for billing, the change in quantity will take effect on the next renewal date.
The following two validations will occur in PHUP:
▪ If the Ignore Blank Quantity Tickets field in ENPH is set to No, all tickets must be entered in ENTI. A ticket is considered entered if you have performed any one of the following actions: you have entered a count for it, you have navigated through it using the F9 key or your arrow keys, or you have cleared it using the Clear Ticket command. 
▪ If you are performing a dual count, the A and B counts must match. A match means that all the inventory levels, quantities and hold codes of the A count must be identical to the inventory levels, quantities and hold codes of the B count.
If either of these validations fail, PHUP will not run. You must return to ENTI, correct the appropriate tickets and then rerun PHUP.
If you wish to make your physical to inventory update manually item by item, use ENAJ (Enter Adjustment) 
instead of PHUP.
1 Make sure that you have printed any required reports. You cannot run the following reports — BOOK, 
BKDT, PHRE or PHTL — after you perform your physical to inventory update.
2 Enter PHUP.
CAUTION PHUP is final and cannot be reversed or undone. Therefore, make sure that you run BOOK or BKDT. All entities listed in the Inventory Not Counted section of this report will be considered as not found and their quantities will be set to zero in 
LOEN.
If you have open orders on your system, it is best to confirm your orders before doing your physical to inventory update. If you cannot confirm your orders, you must make sure that you have sufficient inventory in the warehouse to fill all orders. If your physical quantity is less than your order quantity, you will not be able to confirm the order after you perform your physical to inventory update.
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical. -e 
---

Physical to Inventory Update (PHUP)
3 Key in your physical number and press Enter.
Physical to Inventory Update (PHUP)
4 Click on Update Inventory to update your inventory.

### TROUBLESHOOTING PHUP PROBLEMS <a id="troubleshooting-phup-problems"></a>

Most PHUP problems are caused by input errors that occur in ENTI. The two most common errors occur when:
▪ you type over the level 2, 3 or 4 values of a ticket that you want to change instead of clearing the ticket
▪ you enter a location code that does not match the warehouse code (that is, the location that you enter is not found in the warehouse that you specify)
You correct these errors by identifying the ticket causing the problem, clearing it using the F2 command and then re-entering it correctly. You then rerun PHUP.-e 
---

### Final Steps <a id="final-steps"></a>

1 Run a short inventory report like INHK at the item level only.
2 Check the total on-hand of your inventory report against the total physical count shown in one of your physical reports.
3 If the two numbers match, the adjustments have been properly posted and no further action is required.
If the two numbers do not match, compare your book report (BKDT or BOOK) to the system values in 
LOEN. When you find the inventory entities causing the problem, make any necessary adjustments through ENAJ.
4 If the update is correct and you are satisfied with the results of your physical, wait a suitable period (say, one month) and then delete the physical in ENPH. If you do not delete your physicals, they will take up space in your database and your system performance may suffer.
Error Message Cause Solution can’t find inventory informationThis error is caused by typing over a level 2, 3 or 4 value in ENTI instead of using F2 to clear the ticket. 
When you type over an inventory level, you are not deleting the old level. Instead, you are creating a new record and there now are two records on the system for the same entity.
1. Note the customer code, item code and inventory level(s) for the inventory entity that cannot be updated.
2. Run PHRE (Physical Inventory Ticket Report) to find all tickets that were entered in ENTI for that inventory entity.
3. In ENTI clear one ticket identified in the previous step and then re-enter the tickets correctly.
4. Rerun PHUP.
problem in invt_cursor A record in ENTI is not found in both C_LOC (Location Block of LOEN) and C_INVT (Inventory Block of 
LOEN) because of a wrong inventory level.
EXAMPLE
Note the customer code, item code and inventory level(s) for the inventory entity that cannot be updated. Then look up the inventory access code for the entity in LOEN and contact HighJump’ customer support for assistance. They will correct the ticket causing the problem and you can then rerun PHUP.
C_LOC
ITEM: 101
LOT: A
ID: *
C_INVT
ITEM: 101
LOT: A
ID: 123
Level 3 of C_LOC (*) does not match level 3 of C_INVT (123).-e 
---

### FAQ’s <a id="faq-s"></a>

Can I perform a physical with open orders and receipts
Yes, but such physicals are risky and must be managed with care. Refer to [Open Receipts and Orders](inventario-fisico.html#open-receipts-and-orders) for further information.
How do I count a bulk location with multiple inventory entities in it
Set the Allow Duplicates per Location flag in ENPH to Yes and use blank tickets to enter your bulk location counts.
Can I use my own preprinted tickets for a physical
Yes, but only if you are doing a blind count. AccellosOne 3PL does not support non-blind counts using preprinted tickets.
Can I print my tickets in batches
Yes. If you enter a restriction like warehouse code or location in PHTI, only tickets for that warehouse or range of locations will print.
Can I use a physical to add new product or a new customer to my warehouse
Yes, you can bypass ENRE and add product to your warehouse by means of a physical. However, no initial storage will be charged when you bypass ENRE.
If I make a mistake in ENPH, how do I correct it
If the system does not allow you to change a value in a field, you must delete the physical in ENPH and then re-enter it.
I run PPIT but no tickets are printed
Make sure that you have a physical inventory tickets document set up in DOCU and that the parameters of this document are correct.
How do I enter a ticket for product found in a location not included in the physical
Use a blank ticket.
What does “Inventory Not Counted” mean in the BOOK report
Inventory not counted refers to inventory that is in the system but was not counted because either no ticket was entered for it in ENTI or a ticket was entered for it in ENTI but the ticket was later cleared or the hold code of the book inventory does not match the hold code of the physical inventory. Any item in the Inventory Not 
Counted section of BOOK will be adjusted to zero when you run PHUP.-e 
---

## Reports And Documents <a id="reports-and-documents"></a>

*Manual F — Physical Inventory*

---

Physical vs. Book Report (BOOK)
Physical vs. Book Report (BOOK)
This report shows variances between your book count and your physical count. There are two sections in this report:
▪ Inventory Counted
▪ Inventory Not Counted (only included if the Print Inventory Not Counted flag is set to Yes or Mixed)
BOOK report with Print Inventory Not Counted flag set to Yes and Report Lot Number flag set to Y
Counted inventory includes all inventory that was counted; that is, you entered a ticket — either blank or nonblank — for the entity in ENTI. If the quantity for a ticket in ENTI is zero, the ticket is still considered counted inventory and will appear in BOOK with a quantity of zero.
Inventory not counted includes the following:
▪ cleared tickets
▪ tickets for which you did not enter a quantity in ENTI (non-blind counts only)
▪ inventory with no ticket because it was not found in that location (blind counts only)
The totals in the Physical column of BOOK show what will happen when you update your inventory in PHUP (Physical to Inventory Update). For inventory in the Counted Inventory section of the report, the book value will be overwritten by the physical value. For inventory in the Not Counted Inventory section of the report, all quantities will be adjusted to zero.
You can generate this report at any inventory level you wish. For example, if you generate BOOK at the item level, the report will show your physical versus book quantities for items only and no level 2, 3 or 4 quantities -e 
---

Physical vs. Book Report (BOOK)
will be printed. Alternatively, if you generate BOOK at the lot level (level 2), the report will show your physical versus book quantities for each lot - not each item.

### TIPS ON RUNNING BOOK <a id="tips-on-running-book"></a>

You can rerun BOOK as many times as you like with different options each time. For example, you can run 
BOOK once with the Print Inventory Not Counted flag set to Yes so that inventory not counted will be printed at the end of the report after all the counted inventory. You can then rerun BOOK with the Print Inventory Not 
Counted flag set to Mixed. 
The Mixed option will merge counted and uncounted inventory so that a counted item (for example, Item 1/Lot 
A) will appear beside similar uncounted items (for example, Item 1/Lot B). This will allow you to see at a glance that Item 1/Lot A will replace Item 1/Lot B after you run the update.
For a customer with two inventory levels, a minimum of four separate BOOK reports with the following parameters is recommended:
▪ Print Inventory Not Counted = Yes
▪ Print Inventory Not Counted = Mixed
▪ Report Level 2 (lot # or whatever) = No
▪ Report Level 2 (lot # or whatever) = Yes
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical. 
Print Mixed/Lowest SKU L = Lowest
M = Mixed
If you specify L for Lowest, all quantities will be shown in the lowest SKU for that item. For example, if an item has a quantity breakdown of PALLETS/
CASES, its quantities will be shown in cases only.
If you specify M for Mixed, quantities will be shown using the standard quantity breakdown defined in IQBP. For example, if the quantity breakdown is PALLETS/CASES and there are 60 cases to a pallet, a quantity of 80 cases would be expressed as 1 pallet, 20 cases.-e 
---

Physical vs. Book Report (BOOK)
Quantity in Expanded 
Field
N = No
Y = Yes
If you specify N for No, the size of the quantity field in the report’s output will 
10 characters. If you specify Y for Yes, the column for the quantity in the report’s output will be expanded to 18 characters. 
You use the Yes option when printing quantities in mixed SKU or when you have large numbers of eaches or some other very small SKU type in each location.
Print Inventory Not 
Counted
N = No
Y = Yes
M = Mixed
In this field, you specify your print options for inventory not counted. Inventory not counted means all cleared tickets plus all tickets that were not counted in 
ENTI.
If you specify No, inventory not counted will not appear in the BOOK report. If you specify Yes, inventory not counted will be shown at the end of the report after all the inventory that was counted. If you specify Mixed, inventory not counted will be merged with counted inventory — that is, not placed at the end of report.
The Mixed option is intended to make it easy to adjust inventory levels that were entered incorrectly during receipt entry because of operator error or missing information. 
For example, suppose your level three value of Pallet ID is wrong for certain pallets. When you do your physical, the correct values will be entered and will no longer match your book values, which will be listed in the Inventory Not 
Counted section of the report. If you select the Mixed option, the book and physical values for your pallet ID’s will be shown together and it will be easy to see which pallet ID’s will be corrected.
NOTE It is essential to run BOOK at least once with this flag set to Yes before updating your inventory in PHUP. All entities shown under the Print 
Inventory Not Counted heading will be considered as inventory that was not found and therefore will be adjusted to zero after your physical update.
FIELD DESCRIPTIONS-e 
---

Physical vs. Book Report (BOOK)
Display Variances Only N = No
Y = Yes
If you specify No, all items included in the physical will be printed in the report. 
If you specify Yes, only variances will be included on the report. A variance occurs when the physical quantity does not match the book quantity for an identical inventory entity.
Display Item Value N = No
Y = Yes
If you specify No, item values will not be printed on the report. If you specify 
Yes, any item values defined in ITEM will appear on the report.
Display Physical Ticket 
Numbers
N = No
Y = Yes
If you specify No, ticket numbers not be printed on the report. If you specify 
Yes, ticket numbers will be shown for each item.
Sort by Location Only available if Display Location Details is set to Yes and Print Inventory Not 
Counted is set to Yes or No
N = No
Y = Yes
If you specify No, the report will print in item code sequence. If you specify 
Yes, the report will print in location code sequence.
Display Location Details N = No
Y = Yes
If you specify No, locations will not be printed on the report. If you specify Yes, locations and all inventory levels will be shown for each item. Therefore, when you enter Yes, you will not have access to the Report Level 2, Level 3 and 
Level 4 fields.
FIELD DESCRIPTIONS-e 
---

Physical vs. Book Report (BOOK)

### PROCEDURE <a id="procedure"></a>

1 Enter BOOK.
2 Click on Enter Criteria.
3 Key in your physical number and/or physical inventory date restrictions and click on Execute Query.
Report Level 2/3/4 Only available if your customer has two or more inventory levels
N = No
Y = Yes
The number of inventory levels displayed depends on the customer for whom you are performing a physical. If you specify No, no level 2/3/4 values (lot number, production date, etc.) will be printed on the report. Instead, BOOK will be consolidated at the item level. If you specify Yes, level 2/ 3/4 values will appear on the report.
If you specify the No option for any inventory level (for example, No for level 
2), the Yes option is not available for lower inventory levels (for example, level 
3). If you specify the Yes option for any inventory level, you can select either 
Yes or No for lower inventory levels.
CAUTION It is essential to run BOOK at least once with the Print Inventory Not 
Counted flag set to Yes before updating your inventory. All entities shown under the 
Print Inventory Not Counted heading will be considered as inventory that was not found and will therefore be adjusted to zero after you update your inventory in PHUP.
FIELD DESCRIPTIONS-e 
---

Physical vs. Book Report (BOOK)

Physical versus Book Report (BOOK) for customer with three inventory levels
4 If your query retrieves more than one physical, use your arrow keys to select the physical that you wish to report on.
5 In the Print Mixed or Lowest SKU field, key in L for Lowest or M for Mixed and press Enter.
6 In the Quantity in Expanded Field, key in N for No or Y for Yes and press Enter.
7 In the Print Inventory Not Counted field, key in the appropriate value (N for No, Y for Yes or M for Mixed) 
and press Enter.
8 In the Display Variances Only field, key in N for No or Y for Yes and press Enter.
9 In the Display Item Value field, key in N for No or Y for Yes and press Enter.
10 In the Display Physical Ticket Numbers field, key in N for No or Y for Yes and press Enter.
11 In the Sort by Location field, key in N for No or Y for Yes and press Enter.
12 In the Location Details field, key in Y for Yes or N for No and press Enter.
13 Do one of the following:
If you selected Y for Yes in the 
Location Details field:
If you selected N for No in the 
Location Details field:
a) Proceed to next step. a) In the Report Level 2 field, key in 
Y for Yes or N for No and press 
Enter.
b) If you selected Y for Yes in the previous step, repeat this step for levels 3 and 4 (if any).-e 
---

14 When the Select Printer window appears, key in your printer code and press Enter.
15 Click Ok to print.

### Detail Book Report (BKDT) <a id="detail-book-report-bkdt"></a>

BKDT is an alternate version of BOOK with a slightly different output format. If you select the Display Location 
Details option, BKDT will show the ticket quantity, book quantity and variance quantity (if any) for each item reported on. This information is not available in BOOK.
BKDT report showing Location Details set to Yes
ABC Warehousing Physical No : 22 Page 2 of 2
Detail Book Report (BKDT) 03.02.09 14:26
------------------------------------------------------------------------------------------------------------------------------------
Customer : MAR07 - Maria's Sa
 Ticket Ticket Book Var Physical------------ Book----------------
Product Number Lot Number Size Pallet ID Number Qty Qty Qty Whse Location Hold Whse Location Hold
--------------- --------------- --------------- -------------- ------ ------ ------ ------ -------------------- --------------------
IT001 032007 LARGE 5 2 14 14 0 1 D003Z 1 D003Z
Item 1 Pallet/C 032107 MEDIUM 1 3 87 88 -1 1 D003Z 1 D003Z
 032207 LARGE 10 4 93 92 1 1 D003Z 1 D003Z
 032207 LARGE 9 5 88 88 0 1 D003Z 1 D003Z
 ------ ------ ------
 Item Total 282 282 0
IT002 032007 SMALL 6 6 490 480 10 1 D005Z 1 D005Z
Item 2 Pallet/C 032107 MEDIUM 7 7 1197 1197 0 1 D005Z 1 D005Z
 ------ ------ ------
 Item Total 1687 1677 10
IT003 031907 MEDIUM 8 8 30 30 0 1 D007Z 1 D007Z
 ------ ------ ------
Item 3 Pallet/Case Item Total 30 30 0
IT004 020209 LARGE ABCD 0 7 -7 GSF A001Z
Test KILO w/ pr 102407 LARGE ABC 1 281 281 0 1 C007Z 1 C007Z
 102407 LARGE ABC 9 71 71 0 1 S100G 1 S100G
 ------ ------ ------
 Item Total 352 359 -7
 ------ ------ ------
 Report Physical Total : 2351
 Report Book Total : 2348
 Report Variance Total : 3-e 
---

1 Enter BKDT.
2 Click on Enter Criteria.
3 Key in your physical number and click on Execute Query.
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical. 
Display Location Details N = No
Y = Yes
If you specify No, locations will not be printed on the report. If you specify Yes, locations and all inventory levels will be shown for each item. Therefore, when you enter Yes, you will not have access to the Report Level 2, Level 3 and 
Level 4 fields.
The Yes option will print the ticket quantity, book quantity and variance quantity (if any) for each item reported on.
Report Level 2/3/4 Only available if Location Details = N for No
N = No
Y = Yes
The number of inventory levels displayed depends on the customer for whom you are performing a physical. If you specify No, no level 2/3/4 values (lot number, production date, etc.) will be printed on the report. Instead, BKDT will be consolidated at the item level. If you specify Yes, level 2/ 3/4 values will appear on the report.
If you specify the No option for any inventory level (for example, No for level 
2), the Yes option is not available for lower inventory levels (for example, level 
3). If you specify the Yes option for any inventory level, you can select either 
Yes or No for lower inventory levels.-e 
---

4 In the Location Details field, key in Y for Yes or N for No and press Enter.
5 Do one of the following:
6 When the Select Printer window appears, key in your printer code and press Enter.
7 Click Ok to print.

### Physical Inventory Ticket Report (PHRE) <a id="physical-inventory-ticket-report-phre"></a>

This report shows all your physical inventory tickets in item code order as well as subtotals for each inventory level and each item. As an option, you can print this report for a single item. You use this report if you are unable to update your inventory because an item or inventory level was incorrectly entered in ENTI. PHRE will show all tickets for the item that could not be updated.
If you selected Y for Yes in the 
Location Details field:
If you selected N for No in the 
Location Details field:
a) Proceed to next step. a) In the Report Level 2 field, key in 
Y for Yes or N for No and press 
Enter.
b) If you selected Y for Yes in the previous step, repeat this step for levels 3 and 4 (if any).-e 
---

This report should be printed before performing your physical to inventory update in PHUP.
1 Enter PHRE.
2 Click on Enter Criteria.
3 Key in your physical number, customer code and physical inventory date restrictions and click on Execute Query.
4 If your query retrieves more than one physical, use your arrow keys to select the physical whose tickets you wish to print.
FIELD DESCRIPTIONS
Physical Number The number of the physical. 
Customer Code If you enter a customer code in this field, your query in PHRE will retrieve all physicals for that customer. If you leave this field blank, your query will retrieve all physicals regardless of customer.
Physical Inventory Date If you enter a physical inventory date in this field, your query in PHRE will retrieve all physicals with that physical inventory date. If you leave this field blank, your query will retrieve all physicals regardless of physical inventory date.
Item Code If you enter an item code in this field, the report will be restricted to that item. If you leave this field blank, the report will show inventory for all items.-e 
---

5 Press Enter again to position your cursor in the Item Code field.
6 Key in your item code and press Enter or press Enter with the field blank to generate a report including all items.
7 Key in your printer code and press Enter.
8 Click Ok.

### Physical Inventory Ticket List (PHTL) <a id="physical-inventory-ticket-list-phtl"></a>

This report shows all your physical inventory tickets in ticket number order. It is essentially a printout of the information in ENTI (Enter Tickets/Count Sheets).
This report should be printed before performing your physical to inventory update in PHUP. -e 
---

FIELD DESCRIPTIONS
Physical Number The number of the physical. 
Customer Code If you enter a customer code in this field, your query in PHTL will retrieve all physicals for that customer. If you leave this field blank, your query will retrieve all physicals regardless of customer.
Physical Inventory Date If you enter a physical inventory date in this field, your query in PHTL will retrieve all physicals with that physical inventory date. If you leave this field blank, your query will retrieve all physicals regardless of physical inventory date.
From / To Ticket Number If you enter a from and to ticket number, the report will be restricted to those tickets. If you do NOT enter a from and to ticket number, the report will include all tickets.-e 
---

1 Enter PHTL.
2 Click on Enter Criteria.
3 Key in your physical number, customer code and physical inventory date restrictions and click on Execute Query.
4 If your query retrieves more than one physical, use your arrow keys to select the physical whose tickets you wish to print.
Tickets With Blank Quantity OnlyY = Yes
N = No
If you select Y for Yes, the report will be restricted to tickets with a blank quantity. If you select N for No, the report will not be restricted to tickets with a blank quantity and you can select the appropriate option in the Tickets 
<E>ntered / <N>ot entered /<B>oth field.
A ticket is considered to have a blank quantity if the ticket is marked as “entered” but has no quantity; that is, the Count field in ENTI is blank. If you enter a quantity of zero, the ticket is no longer blank.
NOTE Blank quantity tickets must be either cleared or assigned a quantity in ENTI before you can run PHUP. 
Tickets <E>ntered / 
<N>ot entered / <B>oth
E = Entered
N = Not entered
B = Both
If you select E for Entered, the report will include entered tickets only. If you select N for Not entered, the report will include non-entered tickets only. If you select B for Both, the report will show both entered and non-entered tickets.
A ticket is considered entered is any one of the following actions has occurred:
▪ you have entered a count for it
▪ you have navigated through it using the F9 key or your arrow keys
▪ you have cleared it using the Clear Ticket command
Physical Count Flag A = A Count
B = B Count (only available if you selected a double count in ENPH)
If you select A for A Count, the report will include your A count only. If you select B for B Count, the report will include your B count only. 
FIELD DESCRIPTIONS-e 
---

5 In the From Ticket Number field, key in your starting ticket number and press Enter or press Enter with the default value displayed to accept the first ticket on the physical as your starting ticket number.
6 In the To Ticket Number field, key in your ending ticket number and press Enter or press Enter with the default value displayed to accept the last ticket on the physical as your ending ticket number.
7 In the Tickets With Blank Quantity Only field, key in Y for Yes or N for No and press Enter.
8 In the Tickets <E>ntered, <N>ot Entered or <B>oth field, key in the appropriate value (E, N or B) and press Enter.
9 If you set up the physical as a dual count physical in ENPH, key in your physical count flag value (A or B) 
and press Enter.
10 Key in your printer code and press Enter.
11 Click on Execute Report.

### Physical Inventory Adjustment Report (PIAR) <a id="physical-inventory-adjustment-report-piar"></a>

This report shows all items whose quantities were adjusted during the physical to inventory update. For each item adjusted, both the change in quantity (for example, pallets and cases) and the change in gross and net weight are given.-e 
---

1 Enter PIAR.
2 Click on Enter Criteria.
3 Key in your physical number and click on Execute Query.
4 If your query retrieves more than one physical, use your arrow keys to select the physical whose adjustments you wish to print.
FIELD DESCRIPTIONS
Physical Number Mandatory
The number of the physical. 
Report Level 2/3/4 Y = Yes
N = No
If you specify Yes, level 2/3/4 values (lot number, production date, etc.) will appear on the report. If you specify No, level 2/3/4 values will not appear on the report.
Location Details Y = Yes
N = No
If you specify Yes, locations will print on the report. If you specify No, locations will not print on the report.
ABC Warehousing Inc. Page 1 of 1
Physical Inventory Adjustment Report (PIAR) 04.18.08 15:27
 Customer : A Customer A
------------------------------------------------------------------------------------------------------------------------------------
Physical Number : 100
 -----------------------------Adjust------------------------------
Item Description Quantity Gross Weight Net Weight Meas Wgt
A1 Item A1 5CASE 7.0833 6.6667 KILO
 1 A100 -5CASE
 1 A101 A 5CASE
 1 A104 -10CASE
 1 A105 15CASE
 Total : 5 7.0833 6.6667-e 
---

5 If the customer has two or more inventory levels, press Enter to position your cursor in the Level 2 field and key in the appropriate value (Y for Yes or N for No) and press Enter.
6 Repeat this step for any other inventory levels that this customer may have.
7 In the Location Details field, key in the appropriate value (Y for Yes or N for No) and press Enter.
8 Click on Select Printer.
9 Key in your printer code and press Enter.
10 Click Ok.

### Physical Inventory Tickets Document (DOCU) <a id="physical-inventory-tickets-document-docu"></a>

The standard document for printing physical inventory tickets is PHTI. This document must be set up as follows:
▪ Print Form Source Type = C
▪ Print Form Name = DP210-e 
---

Documents (DOCU) screen for document PHTI (Physical Inventory Tickets)-e 
---

Physical Inventory Tickets For CUST2 (Customer #2)
 Physical Number 58 Physical Type A Counted By ______________
 Entered By ______________
| Ticket Location Whse Hold | Quantity |
+---------------------------------------------------------------+--------------+
| 1 C100 1 | |
+---------------------------------------------------------------+ |
| CUST2 Customer #2 | |
| | |
+---------------------------------------------------------------+--------------+
| 2 C101 1 | |
+---------------------------------------------------------------+ |
| CUST2 Customer #2 | |
| | |
+---------------------------------------------------------------+--------------+
| 3 C102 1 | |
+---------------------------------------------------------------+ |
| CUST2 Customer #2 | |
| | |
+---------------------------------------------------------------+--------------+
| 4 C103 1 | |
+---------------------------------------------------------------+ |
| CUST2 Customer #2 | |
| | |
| 7 D100 1 | |
+---------------------------------------------------------------+--------------+
Non-blank tickets for blind count showing locations but no item information-e 
---

---

A adding new inventory 6, 32
B batches, running in PHTI 20
BKDT (Detail Book Report) 50 blank tickets entering 31 generating 23 blank vs. non-blank tickets 2 blind counts, entering 28 blind vs. non-blind counts 2
BOOK (Physical vs. Book Report) 44 cancelling a physical 18 clearing tickets 33
Create Physical Inventory Tickets (PHTI) 19
D deleting a physical 18
DOCU (Physical Inventory Tickets Document) 59 double or dual counts 10
E
ENPH (Enter Physical Parameters) 8
Enter Physical Parameters (ENPH) 8
Enter Tickets/Count Sheet (ENTI) 26 entering tickets 26, 34
ENTI (Enter Tickets/Count Sheet) 26 entry masks overview 11 working with 34
F
FAQ’s 42 level validation in RFPH 34
M modifying a physical 17
MRFP (RF Profile Code) 34
N new inventory, adding 6, 32 non-blank tickets vs. blank tickets 2 non-blank tickets, generating 22 non-blind counts vs. blind counts 2 non-blind counts, entering 29
O open receipts and orders 5
P
PHRE (Physical Inventory Ticket Report) 52
PHTI (Create Physical Inventory Tickets) 19
PHTL (Physical Inventory Ticket List) 54
PHUP (Physical to Inventory Update) 38
Physical Inventory Adjustment Report (PIAR) 57
Physical Inventory Ticket List (PHTL) 54
Physical Inventory Ticket Report (PHRE) 52 physical inventory tickets document 59 physical inventory unit, definition of 2
Physical to Inventory Update (PHUP) 38
Physical vs. Book Report (BOOK) 44
PIAR (Physical Inventory Adjustment Report) 57
PPIT (Print Physical Inventory Tickets) 23 preprinted tickets 19
Print Physical Inventory Tickets (PPIT) 23 printing physical inventory tickets 23
R receipts, open 5 reprinting tickets 25
INDEX-e 
---

INDEX
RF Physical Count (RFPH) 34
RFPH (RF Physical Count) 34
S show flags logic in ENPH 9 single counts 10
Sort Sequence Code field (ENPH) 13 sort sequence of locations, defining 18
T tickets clearing 33 entering 26, 34 printing 23, 25
TIDE (Ticket Discrepancy Report A vs. B) 37 troubleshooting PHUP errors 40-e 
---
