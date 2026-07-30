---
title: "Back Orders, Batch Picking, Kitting e Substituição"
description: "Tratamentos especiais de pedido: pendências, lotes, kits e substituição de item."
layout: default
---

# Back Orders, Batch Picking, Kitting e Substituição

Tratamentos especiais de pedido: pendências, lotes, kits e substituição de item.

**Fluxo principal:** `CBOR (back order) | GEBA/POBA (batch) | kitting | EOSU/PSPR (substituicao)`

> Fonte: manuais E do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Back Orders <a id="back-orders"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

The back order system allows you to automatically create back orders for product that could not be shipped because of insufficient inventory when the order was allocated. There are two options for creating back orders in AccellosOne 3PL:
 you can create your back orders at allocation
 you can create your back orders at a specific flow by attaching a special verify program to that flow
When you create a pending order in ENOR in which the ordered quantity is greater than the available quantity, allocation will create a regular line or lines for the product that is available for shipping. When you perform allocation or advance to a specific flow to which you have attached the special verify program, AccellosOne 3PL will check your back order conditions to see whether a back order is required. If the answer is 
Yes, the system will create a back order for that portion of the original order that could not be fulfilled. Once you receive the missing stock, you allocate it to the back order. 
EXAMPLE item on order: ABC1 order quantity: 20 available quantity: 15 allocation allocates 15 and creates a back order for the balance of 5
If insufficient stock is received to completely fill the back order, you have two options. You can wait until further stock is received and then process the entire back order or you can fill a portion of the back order with the new stock. If you decide to fill a portion of the back order, a second back order will be created for the balance that was not in inventory.

### SHIP FULL ORDER LINE OPTION <a id="ship-full-order-line-option"></a>

With this option, order lines will only be allocated if the full order line quantity can be shipped at the time of allocation. If the full order line quantity cannot be shipped at the time of allocation, AccellosOne 3PL will create a back order for the full order line quantity.
EXAMPLE item on order: ABC1 order quantity: 20 available quantity: 15 allocation allocates 0 as the item cannot be shipped in full and creates a back order for the original order quantity of 20

OPERATIONS 2 GUIDE 4.2* 51
The back order cycle consists of seven steps. 
ENOR
CHRF
CHOF
When you advance to the back order flow or you allocate the order by printing order documents or by running an RF program, the system creates a back order for that portion of the original order that could not be fulfilled. The back order will consist of (P)ending lines.
You enter a pending order in which the order quantity is greater than the available quantity.
You receive stock.
You confirm the new stock.
If you have auto-processing, the system automatically allocates the back order. If you do not have auto-processing, you must allocate the back order by means of PROM, 
PROR, ASOR or an RF program. When the back order is allocated, the system changes the back order lines from P to R.
The back order is now ready to be confirmed and shipped like a regular order.
ENRE advance to flow / allocation
ENOR (back order)
ENOR (back order)
allocation
You confirm the original order.
CHOF

There are a number of back order options:
 you can define the flow at which back orders are generated
 you can activate back orders at the customer level (that is, only product for certain customers is back ordered)
 you can specify which inventory levels of the back order must match the inventory levels of the original order 
 you can activate back orders at the consignee level (that is, only product going to certain consignees is back ordered)
The following flow chart shows the various back ordering options at the customer and consignee level.
Certain options at the consignee level override options at the Depositor Shipping & Receiving Profile level as shown in the following table: 
DSRP
A = Always N = Never C = Consignee dependent
CONS
A = Always N = Never
Depositor Shipping and 
Receiving Profile
Consignees

OPERATIONS 2 GUIDE 4.2* 53

### Setting Up Back Orders <a id="setting-up-back-orders"></a>

There are up to five setup programs for back orders:
 COMP (Company Parameters Block)
 DSRP (Depositor Shipping & Receiving Profile)
 ITSH (Item Shipping Profile)
 DIFP (Depositor Workflow Profile)
 CONS (Consignees) — only required if you select C for Consignee Dependent in DSRP
In DSRP, you set up your customer level defaults. In ITSH, you specify the inventory level at which you wish to back order. In DIFP, you define the flow at which back orders are generated and in CONS you set up your consignee-level options.

### ACTIVATING THE BACK ORDER SYSTEM IN COMP <a id="activating-the-back-order-system-in-comp"></a>

The Back Order System Activated flag in COMP must be set to Yes.
1 Enter COMP.
2 Select the company that you wish to activate for back orders.
3 Click on Company Parameters .
CONSIGNEES
Always Never
DSRP 
PROFILE
Always back order generated no back order generated
Never no back order generated no back order generated
Consignee dependent back order generated no back order generated

COMP screen showing Back Order System Activated flag set to Yes
4 If required, set the Activate Back Orders flag to Yes.
5 Click on Save .
6 Click on Return.
7 Click on Exit.

### SETTING UP YOUR BACK ORDER OPTIONS IN DSRP <a id="setting-up-your-back-order-options-in-dsrp"></a>

There are two back order flags that require setup in DSRP: Allow Back Orders and Ship Full Order Line 
Quantity.

OPERATIONS 2 GUIDE 4.2* 55
If you wish to activate back orders for some customers but not others or you wish to create back orders at allocation for some customers but not others, you will have to set up multiple DSRP profiles and attach them to the appropriate customers.
1 Enter DSRP. 
2 Retrieve the profile whose back order defaults you wish to adjust.
FIELD DESCRIPTIONS
Allow Back Orders A for Always
Back orders will always be allowed for the customer to which this profile is attached and there will be no restrictions on consignee; that is, back orders will be created for all of a customer’s orders regardless of consignee.
N for Never
Back orders will never be allowed for the customer to which this profile is attached.
C for Consignee Dependent
Back orders will be allowed for the customer to which this profile is attached and will be consignee dependent; that is, back orders will be generated for certain consignees only.
If you select this option, you must enter CONS (Consignees) and specify for each consignee the appropriate back order option. 
Ship Full Order Line 
Quantity
Yes option only available if Allow Back Orders flag set to Always or Consignee dependent
N = No
Y = Yes
If you select No, existing back order rules will apply; that is, create a back order for the unallocated portion of the order line. 
If you select Yes, order lines will only be allocated if the full order line quantity can be shipped at the time of allocation. If the full order line quantity cannot be shipped at the time of allocation, AccellosOne 3PL will create a back order for the full order line quantity.

Depositor Shipping and Receiving Profile (DSRP) showing Allow Back Orders flag set to Always
3 Make sure that the Change Zero Pending Line to R-Type Line field is set to N for No. You cannot generate back orders if this flag is set to Y for Yes.
4 Set the Allow Back Orders flag to the appropriate value (A for Always, N for Never or C for Consignee 
Dependent).
5 Set the Ship Full Order Line Quantity flag to the appropriate value (Y for yes or N for No).
6 Click on Return to Main and Exit to exit.
SPECIFYING THE NUMBER OF INVENTORY LEVELS FOR BACK ORDERS IN 
ITSH
In ITSH (Item Shipping Profile), you specify the degree to which the items on the back order must match the items on the original order. For example, suppose your inventory level setup for an item is as follows:
Level 1 = ITEM
Level 2 = LOT # 
Level 3 = PRODUCTION DATE 
If you specify 1, level 1 (item) of the back order will match level 1 of the original order but levels 2 and 3 will be left blank.
If you specify 2, levels 1 and 2 (item and lot #) of the back order will match levels 1 and 2 of the original order but level 3 will be left blank.

OPERATIONS 2 GUIDE 4.2* 57
If you specify 3, all three inventory levels of the back order will match the three inventory levels of the original order.
1 Enter ITSH.
2 Retrieve the profile whose back order options you wish to set up.

Item Shipping Profile (ITSH)
3 In the Generate Back Orders at Level Number field, key in the appropriate inventory level and press 
Enter.
4 Click on Return to Main and Exit to exit.

### DEFINING THE FLOW AT WHICH BACK ORDERS ARE GENERATED IN DIFP <a id="defining-the-flow-at-which-back-orders-are-generated-in-difp"></a>

You define the flow at which back orders are generated by attaching the special verifier program CBOR (Create Back Order) to the appropriate flow. You can attach CBOR to any outbound flow on your system except ENOR (Enter Order) as long as the order has been allocated. For example, if you allocate your orders at flow 3, you can attach CBOR to flow 3, 4, 5 or 6 but not to flows 1 or 2.
1 Enter DIFP.
NOTE If you want to vary your matching conditions by item (for example, for item X all inventory levels must match while for item Y only the first level must match), you must set up multiple ITSH profiles.
at Level Number field

2 Retrieve the workflow profile code that you wish to set up for back orders.
3 Click on In/Out/Repi/Relo Block. The first record in this block will be your Inbound record.
4 Select the Outbound option and click on Flow Block.
5 In the Flow Block, use your arrow keys to select the flow at which you wish to create your back orders.
6 Click on Document Block.
7 In the Document Block, click on Special Verifier Block.

Depositor Workflow Profile screen showing Special Verification Details
8 Key in your sequence number for the special verification program (for example, 10) and press Enter.
9 Key in CBOR and press Enter.
10 Press Enter to bypass the remaining fields on your screen.

OPERATIONS 2 GUIDE 4.2* 59

Depositor Workflow Profile screen showing special verify CBOR attached to the flow STPI (Confirm 
Order)
11 When you cursor is again positioned in the Sequence field, press F4 the required number of times to exit 

### SETTING UP YOUR CONSIGNEES IN CONS <a id="setting-up-your-consignees-in-cons"></a>

If you specified C for Consignee Dependent in DSRP, you must set up for each consignee on your system the appropriate back order option. There are two back order options for any given consignee:
FIELD DESCRIPTIONS
Allow Back Orders A for Always
Back orders will always be generated for this consignee.
N for Never
Back orders will never be generated for this consignee. If there is insufficient product to fill an order line, the order line will be split into two lines — an Rtype line and a P-type lines — and you will be unable to confirm the P-type line.

1 Enter CONS.
2 Retrieve the consignee whose back order options you wish to set up.
3 Press Enter until you reach the Allow Back Orders field.
Consignees (CONS)
4 In the Allow Back Orders field, enter the appropriate option (A for Always or N for Never).
5 Set the Ship Full Order Line Quantity flag to the appropriate value (Y for yes or N for No).
6 Click on Return to Main and Exit to exit.
Ship Full Order Line 
Quantity
Only available if Allow Back Orders flag = Always
N = No
Y = Yes
If you select No, existing back order rules will apply; that is, create a back order for the unallocated portion of the order line. 
If you select Yes, order lines will only be allocated if the full order line quantity can be shipped at the time of allocation. If the full order line quantity cannot be shipped at the time of allocation, AccellosOne 3PL will create a back order for the full order line quantity.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 61

### Processing Orders with the Back Order System Activated <a id="processing-orders-with-the-back-order-system-activated"></a>

When allocation or your back order flow is complete, the following will occur:
 the lines on the original order that could be fulfilled will be assigned locations and changed from P to R lines
 the lines on the original order that could not be fulfilled will be removed from the original order and placed on a new back order; these lines will remain as P-type lines
1 Enter ENOR.
2 Press F9 to position your cursor in the Order Type field.
3 Key in P for Pending and press Enter.
4 Enter the remainder of the Header Block normally.
5 In the Line Block, enter your order lines.
6 Exit ENOR and proceed to print any documents and time-stamp your flows in CHOF in the normal manner.

Creating Back Order message in CHOF
7 Press Enter to acknowledge the “Creating Back Order” message.
8 Confirm the original order in CHOF or COOL in the normal manner.

### LOOKING UP A BACK ORDER IN LOOR <a id="looking-up-a-back-order-in-loor"></a>

You look up a back order in LOOR by performing a query on the original order number.

1 Enter LOOR (Look Up Orders).
2 In the Order Number field, key in the order number of the original order and click on Execute Query. The original order that you query should display on your screen.

Look Up Orders (LOOR) screen showing the original order (1665)
3 In the Back Order Reference field on the left-hand side of the screen, you will see the characters <…> followed by a number. This number is the back order created when the order documents for the original order were printed. 
4 If you look up the back order in LOOR, you will see the original order number in the Back Order Reference field. The original order number will appear before the characters <…>.
Back order created from original order

OPERATIONS 2 GUIDE 4.2* 63

Look Up Orders (LOOR) screen showing the back order (1666)
5 Click on Line Block to enter the Line Block. Because the lines have not yet been allocated, their line type will be P for Pending. 
6 When you finish looking up your back order, press F4 the required number of times to exit.

### RECEIVING STOCK (MANUAL PROCESSING) <a id="receiving-stock-manual-processing"></a>

When the product on back order is received and confirmed, you allocate the back order using whichever method of allocation is followed in your warehouse. You can allocate by printing a shipping document in 
PROR (Print Shipping Documents - All) or PROM (Print Shipping Documents - Specific), by running an RF program or by using auto-processing. When allocation is complete, the new inventory will be allocated to the back order and the order lines in ENOR for the back order will change from P to R. 
If sufficient product is received to completely fill the back order, the order lines will change from P to R. If insufficient stock is received to completely fill the back order, the first back order will be fulfilled and a second back order will be created for the balance that is not in inventory.

### RECEIVING STOCK (AUTO-PROCESSING) <a id="receiving-stock-auto-processing"></a>

If your system has been configured to perform auto-processing, there is no need to print the shipping documents for the back order in PROR (Print Shipping Documents - All) or PROM (Print Shipping Documents 
- Specific). When new stock is received and a back order can be fully or partially filled, the system will print the 
shipping documents automatically and allocate the order.
If you assign priorities to your orders, the priority of any back orders created will match the priority of the original order and the system will allocate the back orders based on priority level.
Original order number

### DELETING BACK ORDERS AND ORIGINAL ORDERS <a id="deleting-back-orders-and-original-orders"></a>

If a back order is unconfirmed, you can delete it at any time in ENOR. You delete a back order by means of the F2 (Delete) command in ENOR. 
If you delete the original order but not the back order, the back order will remain active on your system. If you do not want to ship out the back order, you must delete it in ENOR.

### Item Back Order Report (IBOR) <a id="item-back-order-report-ibor"></a>

See the Standard Reports Guide.

OPERATIONS 2 GUIDE 4.2* 65

## Batch Picking <a id="batch-picking"></a>

*Manual E — Operations 2*

5 — Printing the Order Documents (Optional) and Confirming the Original 

### Overview <a id="overview"></a>

Batch picking allows you to group multiple orders in a single batch and pick the consolidated quantity of the batch rather than the individual quantities of the original orders. There are two advantages to batch picking: 
 if there is incomplete stock to fill all orders, you can decide which orders you wish to fill and which orders you wish to ship short or not at all
 picking is more efficient because if the quantities allow it you can pick full pallets from bulk rather than partials from the pick line
The way in which quantities are consolidated depends upon which inventory levels you specify when entering your order. If you have two inventory levels (ITEM and LOT) but specify only the item code on your orders, the system will consolidate all order lines containing the same item and allocate the consolidated quantity of those order lines. 
BEFORE CONSOLIDATION AT ITEM LEVEL
AFTER CONSOLIDATION AT ITEM LEVEL
If you specify both item and lot when entering your order, the system will consolidate by lot number; that is, the system will consolidate all order lines containing the same lot number and allocate the consolidated quantity of those lots.

### ALLOCATION AND BATCH PICKING <a id="allocation-and-batch-picking"></a>

In batch picking, quantities of a given item are consolidated before allocation and if the order quantity exceeds the quantity in the pick line location, the allocation routine will pick from bulk rather than from the pick line. 
Consider the following example in which the same item is on five orders:
Order 1
Item A
Quantity = 25 CS
Order 2
Item B
Quantity = 10 CS
Order 3
Item A
Quantity = 25 CS
Batch Order
Item A
Quantity = 50 CS
Batch Order
Item B
Quantity = 10 CS
NOTE Batch picking is only available for orders with pending lines. You cannot batch pick orders with regular lines.
GEBA does not support line remarks. Therefore, any line remarks on the original orders will not be available in the batch order that you generate in GEBA.

OPERATIONS 2 GUIDE 4.2* 67
Number of orders: 5
Number of cases per order: 20
Consolidated total number of cases for all orders: 100
Quantity breakdown of item: 80 cases per pallet
As the above example shows, batch picking is more efficient than individual order picking because it makes it possible to pick full pallet quantities from bulk instead of multiple partials from the pick line.

### Setting Up Batch Picking <a id="setting-up-batch-picking"></a>

In order to perform batch picking, you must allocate your orders at the ENOR flow. Make sure that the Assign 
Location flag in DIFP is set to Yes for ENOR (Enter Order).
Allocation With Individual Order Picking
Pick line (quantity = 35 cases)
one pick of 20 cases from the pick line
Pick line (quantity = 15 cases)
Replenishment of pick line from bulk
Bulk area four picks of 20 cases each from the pick line
Allocation With Batch Picking
Pick line (quantity = 35 cases)
one pick of 20 cases from the pick line
Bulk area one pick of a full pallet (80 cases) from bulk

Depositor Workflow Profile (DIFP)

### CHANGE ZERO PENDING LINE TO R-TYPE LINE FLAG IN DSRP <a id="change-zero-pending-line-to-r-type-line-flag-in-dsrp"></a>

This option is not available for batch picking. Regardless of the value of this flag, any order lines created by 
AccellosOne 3PL to indicate that there is insufficient product to fill an order line will be P-type lines.

### PRINTING REQUIREMENTS <a id="printing-requirements"></a>

If you have special printing requirements for batch picking (for example, print pick sheet X or do not print any pick sheet), you must create a workflow profile in DIFP with the appropriate document attached and then assign the DIFP profile to your batch order in GEBA (Generate Batch Order). If you do not have special printing requirements for batch picking, you can use an existing workflow profile and whichever documents are attached to it will be the printing requirement for batch picking.

### Performing Batch Picking <a id="performing-batch-picking"></a>

There are a maximum of seven steps to perform in batch picking.
Assign Location flag set to Y for Yes for ENOR flow

OPERATIONS 2 GUIDE 4.2* 69
ENOR
GEBA
Print?
PROM/
PROR
Yes
POBA
Print?
PROM/
PROR
Yes
RFPIC
You generate your batch order in GEBA. 
The system allocates the batch order and changes the original orders to consolidated orders. The consolidated orders remain unallocated.
You enter your orders with pending lines in ENOR (not required if your orders are generated through EDI). 
If you have a document attached to your batch order, you print the document.
You assign the batch order to the consolidated orders in POBA. The system changes the C lines of the consolidated orders to R lines and deletes the batch order that you generated in step 2.
If you have documents attached to your consolidated orders, you print these documents.
You pick the individual orders in the normal way.
No
No
CHOF/
COOL
You confirm the individual orders in the normal way.

### 1 — ENTERING YOUR ORDERS IN ENOR <a id="1-entering-your-orders-in-enor"></a>

In this step, you enter the orders that you wish to batch pick. When entering your orders, you must change the line type from R for Regular to P for Pending in order to place the order on a batch order.
1 Enter ENOR.
2 Enter the header information for the order in the normal manner.

ENOR screen showing the line type set to R for Regular
3 In the Line Block, set the line type to P for Pending.
4 Enter your item information and quantities.
5 Repeat the above steps for any additional orders that you wish to place on the batch.

### 2 — GENERATING YOUR BATCH ORDER IN GEBA <a id="2-generating-your-batch-order-in-geba"></a>

In this step, you select the orders that you wish to place on the batch order as well as the appropriate workflow profile code. Then you generate your batch. During generation, the system allocates the batch order and changes the original orders to consolidated orders. The consolidated orders remain unallocated at this stage.
1 Enter GEBA.
Set the Type field to P for 
Pending

OPERATIONS 2 GUIDE 4.2* 71

Generate Batch Order (GEBA)
2 Enter your restrictions and click on Execute Query. The restrictions that you enter determine which orders will be placed on the batch. 
For example, if you specify Customer A as your restriction, only orders belonging to that customer will be placed on the batch. You can restrict the batch by load number, range of order number, customer, consignee, carrier or any other field in the Query Restriction Block.
Refer to “FIELD DESCRIPTIONS FOR QUERY RESTRICTION BLOCK (GEBA)” (ver [1 — Entering Your Orders in ENOR](pedidos-especiais.html#1-entering-your-orders-in-enor)) for the options on this screen.

GEBA screen showing restrictions by customer (customer code = A) and by consignee (consignee code = CONS1)
3 When you click on Execute Query, the Orders Block will appear.

Generate Batch Order (GEBA) screen showing Orders Block

OPERATIONS 2 GUIDE 4.2* 73
4 In the Orders Block, select the orders that you wish to pick by means of the Select Order or Select All commands. To deselect an order, click on De-Select Order.
5 If there are no orders displayed in the Orders Block, make sure that the orders that you created were pending-type orders. Regular-type orders cannot be placed on a batch in GEBA.
6 Click on Allocate Batch.
7 In the Workflow Profile Code field, key in your workflow profile code and press Enter. The system will start allocating the batch order.

Generate Batch Order (GEBA) screen showing workflow profile assigned to batch order
8 Once the batch is allocated, GEBA will close and you will be returned to the Orders submenu.
FIELD DESCRIPTIONS FOR QUERY RESTRICTION BLOCK (GEBA)
Load Number The order’s load number. You can enter up to eight load numbers in this field.
From / To Order Number The range of order numbers.
Purchase Order Number The order’s purchase order number. You can enter up to six purchase order numbers in this field.
Customer Order Number The order’s customer order number.
Item Location Profile 
Code
The order’s item location profile code. You can enter up to eight item location profile codes in this field.

Customer Code The order’s customer.
Consignee Code The order’s consignee.
Carrier Code The order’s carrier.
Order Date The order’s order date. The order date is the date entered in the Order Date field in ENOR.
Ship Date The order’s ship date. The ship date is the date entered in the To Ship Date field in ENOR.
Order Type The order’s type.
R = Regular
P = Pending
Order Priority The order’s priority. You can set an order’s priority in two ways:
 you can enter a value in the Priority field in CONS (Consignees)
 you can change the value in the Priority field in ENOR during order entry
EDI Group Value The order’s internal EDI grouping — EDI customers only.
Weight Restriction There are three weight restrictions supported in GEBA: greater than (>), less than (<) and equal to (=). For example, if you enter <500, only orders with a total weight of less than 500 lbs. or kilos will be shown. AccellosOne 3PL uses the weight measure code and weight defined in ITEM.
Single/Multiple Lines S = Single (Single line orders only)
M = Multiple (Multi-line orders only)
blank = both
Maximum Number of 
Orders in Batch
The maximum number of orders in the batch. Suppose you have 100 orders on your system for customer A. If you restrict by customer A and enter 10 in this field, AccellosOne 3PL will show the first 10 orders for customer A and exclude the remaining 90.
Order with Item Only orders with the item that you specify will be shown. If the order has multiple lines, only one line on the order has to contain the item code that you specify in this field in order for the entire order to be included in the batch.
You can enter up to three items in this field.
FIELD DESCRIPTIONS FOR QUERY RESTRICTION BLOCK (GEBA)

OPERATIONS 2 GUIDE 4.2* 75

### 3 — PRINTING YOUR BATCH ORDER DOCUMENTS <a id="3-printing-your-batch-order-documents"></a>

If the workflow profile that you entered in GEBA has a document attached to it, you must print that document or documents.
1 Enter PROM or PROR and print the required documents for your batch order.

### 4 — ASSIGNING THE BATCH ORDER TO THE CONSOLIDATED ORDERS IN POBA <a id="4-assigning-the-batch-order-to-the-consolidated-orders-in-poba"></a>

In this step, you assign the batch order to the consolidated orders (that is, the individual orders on the batch). 
If there is no exact match between the order quantity and the available quantity (for example, your order quantity is 10 cases but your available quantity is 8 cases), POBA allows you to view the entity and decide which product you wish to assign to which orders. As well, if there is insufficient product to fill all your orders, you can decide which orders you wish to short ship.
When you finish processing your orders in POBA, the Unallocated Batch Orders Report is automatically run. 
In the “Orders With Pending Lines” section of this report, AccellosOne 3PL lists all order lines that were short shipped.
There are two blocks in POBA: the Detail Block and the Consolidated Orders Block. The Detail Block shows the remaining entities to be assigned and the available quantity for each batch line. The Consolidated Orders 
Block shows the quantity required for each order line of the appropriate Detail Block record.
EXAMPLE
You enter two orders for the same item in ENOR.
After allocation, AccellosOne 3PL finds four entities representing a total quantity of 125 units.
In POBA you will see the following in the Detail Block:
Order without Item Only orders without the item that you specify will be shown. If the order has multiple lines and one line on the order contains the item that you specify in this field, the entire order will be excluded from the batch.
You can enter up to three items in this field.
ORDER NUMBER ITEM QUANTITY
10 A 100
11 A 50
ITEM LOT QUANTITY
A 101 25
A 102 30
A 107 15
FIELD DESCRIPTIONS FOR QUERY RESTRICTION BLOCK (GEBA)

You assign the appropriate lot shown in the Detail Block to the appropriate order line shown in the Consolidated Orders Block.

Post Batch Order to Consolidated (POBA)
A = the item to be assigned — item B1, lot 101
B = the number of lines left on the batch order that remain to be assigned
C = the available quantity of item B1, lot 101 (15 cases) for orders 1625, 1626 and 1627
D = the orders that require this item
E = the quantities of the item required for each order
You assign product to an individual order by entering the quantity to be assigned in the Ship Quantity field of the Consolidated Orders Block. If the order contains product on hold, the hold code of the order line must match the hold code of the available inventory.
A 122 65
ITEM LOT QUANTITY
A
D
E
B

OPERATIONS 2 GUIDE 4.2* 77
A = the item and lot to be assigned (B1, lot 101)
B = the quantity of item B1, lot 101, that you are assigning to order 1625 (10 cases)
C = the available quantity of item B1, lot 101, after you assign 10 cases to order 1625 (5 cases)

### PROCEDURE <a id="procedure"></a>

1 Enter POBA.
A
B

Post Batch Order to Consolidated (POBA)
2 Key in the number of the batch order that was created in GEBA and click on Execute Query. If you have multiple batch orders, you can leave the Batch Number field blank and click on Execute Query to retrieve all batch orders.

OPERATIONS 2 GUIDE 4.2* 79

Post Batch Orders to Consolidated (POBA) screen showing two inventory entities on three orders
3 Click on Detail Block. The Detail Block shows all items in the batch order as well as their available quantities. Use your arrow keys to scroll forward and backward through each line in the Detail Block.
4 When your cursor is positioned on the item that you wish to assign, click on Consolidation Block to enter the Consolidated Orders Block. 
5 Use your arrow keys to scroll forward and backward in the Consolidated Orders Block. When your cursor is positioned in the Ship Quantity field of the order that you wish to process, key in the quantity that you want to assign to that order line and press Enter. 
If there is an exact match between the order quantity and the available quantity:
If there is NOT an exact match between the order quantity and the available quantity:
The Detail and Consolidated 
Orders Blocks will be blank. You will not be able to assign product to specific orders because the order quantity equals the available quantity (for example, the order quantity is 10 cases of item X and you have exactly 10 cases of item X in your warehouse). 
a) Proceed to step 9.
a) You must manually assign product to each order line. Proceed to next step. 

When you enter a quantity in the Ship Quantity field, that quantity is subtracted from the available quantity in the Detail Block. For example, if you have 50 cases of item 1 (available = 50 in the Detail Block) 
and assign 10 cases to order 4, the available quantity in the Detail Block will decrease from 50 to 40.

Post Batch Orders to Consolidated (POBA) screen showing 10 cases of B1, lot 101, allocated to order 
6 If there is more product available in the Detail Block, continue to assign it to your orders. When there is no more product to assign in the Detail Block, click on Detail Block to return to the Detail Block.
7 Select another record in the Detail Block and repeat steps 4 to 6 for the second record. Make sure that you assign all product in the Detail Block (that is, available = 0) as you cannot run POBA until the value in 
Available field equals zero for each line in the Detail Block.
8 When you finish entering all your lines, click on Batch Block to exit to the Batch Block.
9 Click on Process Batch. The system will delete the batch order, update the consolidated orders with the appropriate item and location information and change the P lines of the consolidated orders to R lines. 
The Unallocated Batch Orders Report will open in a separate window.

OPERATIONS 2 GUIDE 4.2* 81
POBA report screen showing two orders with pending lines
10 If required, you can print the report in Acrobat by clicking on File/Print.
11 When you finish viewing or printing the report, click on File/Close.
12 Click on Exit to exit POBA.
5 — PRINTING THE ORDER DOCUMENTS (OPTIONAL) AND CONFIRMING THE 
ORIGINAL ORDERS
You can confirm the original orders individually in CHOF or COOL in the usual way or you can confirm the batch order only in CHOF and AccellosOne 3PL will automatically confirm the original orders.
1 If required, enter PROM or PROR and print your shipping documents for the original orders.
In PROR, you can enter the batch number in the Query Restriction Block and AccellosOne 3PL will retrieve all orders on the batch.
ABC Warehousing, Inc. Page 1 of 1
 UNALLOCATED BATCH ORDERS REPORT
BATCH NUMBER: 1401 PRINTED ON: 06-May-2005 10:14
CUSTOMER ORDER# ITEM ORDER QTY SHIP QTY
================================================================================
UNALLOCATED ORDERS TO BE DELETED IN JOB COCB
 NO PENDING ORDERS ON THE BATCH WERE FOUND
--------------------------------------------------------------------------------
ORDERS WITH THE PENDING LINES
B 1399 B1 5 5
B 1400 B1 5 5
--------------------------------------------------------------------------------
ORDERS WITH SHORTAGES
 NO ORDERS WITH SHORTAGES ON THE BATCH WERE FOUND

Print Shipping Documents - All (PROR) screen showing batch order 1620
2 Proceed to confirm the individual orders in CHOF or COOL in the usual way or confirm the batch order only in CHOF.

CHOF screen showing batch order number

### Working With Batch Orders <a id="working-with-batch-orders"></a>

Like regular orders, batch orders can be deleted or modified at any time provided that they have not been confirmed.
Batch Order 
Number field

OPERATIONS 2 GUIDE 4.2* 83

### LOOKING UP A BATCH ORDER <a id="looking-up-a-batch-order"></a>

You look up a batch order in LOOR (Look Up Orders) by performing a query on the batch order number. If you do not know the batch order number or wish to look up all your batch orders, you can perform a query in the 
Type field of LOOR.
The Batch Order Block in LOOR shows all consolidated orders in the batch.
1 Enter LOOR.
2 Key in your batch order number and click on Execute Query. If you wish to look up all your batch orders, press Enter until your cursor is positioned in the Type field. Then key in B% for Batch and click on Execute Query.

Look Up Orders (LOOR) screen showing the batch order
3 Click on Time Block.
4 Click on Batch Order Block.
Type = Batch

Look Up Orders (LOOR) screen showing consolidated orders in the batch
5 When you finish looking up the consolidated orders on the batch, click on Time Block and Master Block. 
Then click on Exit to exit.

### LOOKING UP A CONSOLIDATED ORDER <a id="looking-up-a-consolidated-order"></a>

You look up a consolidated order in LOOR (Look Up Orders) by performing a query on the order number. If you do not know the order number or wish to look up all your consolidated orders, you can perform a query in the Type field of LOOR.
1 Enter LOOR.
2 Key in your order number and click on Execute Query. If you wish to view all your consolidated orders, press Enter until your cursor is positioned in the Type field. Then key in C% for Consolidated and click on 
Execute Query.

OPERATIONS 2 GUIDE 4.2* 85

Look Up Orders (LOOR) screen showing the original order (1849)
3 Click on Exit to exit.

### DELETING ORDERS ON A BATCH <a id="deleting-orders-on-a-batch"></a>

If you wish to delete an order on a batch after generating the batch in GEBA, you must delete the batch order first. Once you have deleted the batch order, you can then delete the original orders. You delete orders by entering ENOR, retrieving the order to be deleted and clicking Delete.
If you wish to delete an order after allocating the batch order to the consolidated orders in POBA, you enter 
ENOR, retrieve the order to be deleted and click on Delete. There is no need to delete the batch order as the system will have already deleted it. 

### REMOVING ORDERS FROM A BATCH IN COCB <a id="removing-orders-from-a-batch-in-cocb"></a>

If you need to make changes to an order after placing it on a batch, you must first remove it from the batch in 
COCB (Clear Order from Closed Batch). When you finish making your changes to the order in ENOR, you rerun GEBA and POBA to place it on a new batch.
The orders that you remove in COCB can be either allocated or unallocated. If the order is allocated, COCB will automatically deallocate the order.
NOTE You should only remove orders from a batch at the flow ENOR. If the order is at a later flow in your flow profile, you can remove it from the batch in COCB, but you will not be able to place it on a new batch in GEBA.
The batch order (1945) created by the system

1 Enter COCB.

Clear Order from Closed Batch (COCB) screen
2 Do one of the following:

Clear Order from Closed Batch (COCB) screen
3 Press Enter to position your cursor in the Order Type field.
If you know the order number that you wish to remove:
If you do NOT know the order number that you wish to remove:
a) Key in your order number and press Enter.
a) Click on Enter Criteria to enter query mode.
b) Click on Execute Query to retrieve all consolidated orders or press Enter to position your cursor in the Batch Order Number field, key in your batch order number and click on Execute 
Query to execute your query.

OPERATIONS 2 GUIDE 4.2* 87
4 Click on Delete.
5 Click on Return to Main and Exit.

### DELETING A BATCH ORDER <a id="deleting-a-batch-order"></a>

If the batch order that you generate in GEBA is in error, delete the batch order in ENOR. When you delete the batch order, the consolidated orders that were part of it will be restored to pending orders. 

### MODIFYING A BATCH ORDER <a id="modifying-a-batch-order"></a>

If you have generated your batch in GEBA but not yet run POBA, you must first delete the batch order in 
ENOR. Then retrieve the original orders in ENOR and make your required changes. Lastly, generate a new batch in GEBA and rerun POBA.
If you have allocated the batch order to the consolidated orders in POBA, you can make any required changes to the original orders by retrieving them in ENOR. There is no need to rerun POBA after making your changes.

### Consolidated Picking in COPI <a id="consolidated-picking-in-copi"></a>

Consolidated picking allows you to consolidate multiple orders belonging to any customer and print them on a single outbound document such as a pick sheet or a bill of lading. You perform consolidated picking in COPI (Consolidated Pick). The use of COPI is restricted to allocated orders; you cannot consolidate unallocated orders in this program.
COPI is typically used when you pick and allocate an order at one point during the day and later on receive a second order from the same customer. You then pick the second order and use COPI to produce a consolidated bill of lading containing both orders.
If you wish to consolidate orders before allocation in order to pick more efficiently, you must use GEBA (Generate Batch Order) and POBA (Post Batch Order to Consolidated).
Consolidated picking can be combined with batch picking. For example, you generate a batch order in GEBA and then post the batch order to the consolidated orders in POBA. You then run COPI to print the consolidated orders on a single pick sheet or bill of lading. 
1 Enter COPI.

Consolidated Pick (COPI)
2 Do one of the following:
If you know the order numbers that you wish to consolidate:
If you do NOT know the order numbers that you wish to consolidate:
a) Press Enter to position your cursor in the Order Number field.
b) Key in your order number and press Enter.
c) Repeat the previous two steps for each additional order that you wish to print on the pick sheet or bill of lading.
a) Click on Query Block.
b) Key in your query criteria and click on Execute Query.

OPERATIONS 2 GUIDE 4.2* 89

Consolidated Pick (COPI) screen showing three orders: 1486, 1504 and 1506
3 When you finish entering your orders, click on Execute Query then Location.
4 Press Enter to bypass the Location Profile Code field. 
5 In the Document Code field, key in your document code and press Enter.

Consolidated Pick (COPI) screen showing a bill of lading document being printed
6 Click on Print Block.
7 In the Printer Code field, key in your printer code and press Enter.
8 Click Ok to print.

### LOOKING UP YOUR CONSOLIDATED PICK ORDER IN LOOR <a id="looking-up-your-consolidated-pick-order-in-loor"></a>

Once you print your consolidated pick document, AccellosOne 3PL will create a new batch-type order containing the orders that were consolidated. The batch-type order will have a status of “Deleted”.
1 Enter LOOR.
2 Press Enter until your cursor is positioned in the Type field.
3 Key in BATCH and click on Execute Query.
4 If your query retrieves multiple batch type orders, use your arrow keys to retrieve the correct order.

OPERATIONS 2 GUIDE 4.2* 91

Look Up Orders (LOOR) screen showing batch type order
5 Click on Time Block.
6 Click on Batch Order Block.

Look Up Orders (LOOR) screen showing three orders in Batch Order Block
7 When you finish looking up the consolidated orders on your batch-type order, press F4 the required number of times to exit.

OPERATIONS 2 GUIDE 4.2* 93

## Item Substitution <a id="item-substitution"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

The item substitution function allows you to define one or more items as substitutes for another item when you are unable to fill an order because of lack of inventory. AccellosOne 3PL item substitution logic tells you which items if any can be shipped instead of the item ordered.
When you run allocation, the allocation program will fulfill any part of the order line that it can and create a new line for the unfulfilled part. At this point, if the item has any defined substitutes, the Change Zero Pending 
Line to R-Type Line flag will NOT be used to change the line to a zero to-ship regular line even if it is set to 
Yes. Instead, the allocation program will try again with the first defined substitute item, continuing on to further substitute items as long as is necessary and as long as further substitutes exist.
If after trying all valid substitute items an order line still cannot be fulfilled, the allocation program will return to the original item for a final pass. At this point, the Change Zero Pending Line to R-Type Line flag will be used: 
the unfilled line of the original item will be left as a pending line or set to a zero to-ship regular line depending on the status of the flag.

### Setting Up Item Substitution <a id="setting-up-item-substitution"></a>

There are two setup programs for item substitution:
 Item Shipping Profile Code (ITSH)
 Item Codes (ITEM)

### ACTIVATING ITEM SUBSTITUTION IN ITSH <a id="activating-item-substitution-in-itsh"></a>

In ITSH you set the Use Substitute Item Codes flag to A for Always. 
1 Enter ITSH.
2 Retrieve the item shipping profile that you wish to modify.
3 Press Enter until your cursor is positioned in the Use Substitute Item Codes field.
4 Key in A for Always and press Enter.
FIELD DESCRIPTIONS
Use Substitute Item 
Codes
N = No
A = Always
E = Enter at Order Entry Time (reserved for future use)
If you select N for No, item substitution will be deactivated. If you select A for 
Always, item substitution is activated for all items that have valid substitutes defined for them in ITEM. 

OPERATIONS 2 GUIDE 4.2* 227

Item Shipping Profile (ITSH) screen showing Use Substitute Item Codes flag set to A for Always
5 When you finish making your changes, click on Return to Main and Exit.
6 Repeat the above steps for any additional item shipping profiles that you wish to activate for item substitution.

### SETTING UP YOUR SUBSTITUTE ITEMS IN ITEM <a id="setting-up-your-substitute-items-in-item"></a>

In the Substitution Block of ITEM, you specify which items — if any — can serve as a substitute item for the base item. In the event that you are unable to ship the base item, the system will ship the substitute item or items that you specify. The substitute item or items that you specify must all be regular items set up in ITEM and must belong to the same customer.
Substitute items can also have substitutes if the first substitute item cannot be shipped and those substitutes can have further substitutes of their own. 
FIELD DESCRIPTIONS (SUBSTITUTION BLOCK)
Seq. Mandatory
The sequence number defines the order in which substitute items will be considered.

Item Code Mandatory
The item that will serve as a substitute. 
Type I = Inbound (reserved for future use)
O = Outbound
B = Both (reserved for future use)
Set to O for Outbound.
Chain Y = Yes
N = No
If you set the Chain flag to Y for Yes for an item, the system will also search for any substitutes defined for that item in ITEM.
EXAMPLE
Item A (Chain = N)
Item B (Chain = Y)
Item C (Chain = N)
AccellosOne 3PL will query in the following order: Item A, Item B, Item C and then substitutes for Item B defined in ITEM.
If you set the Chain flag to N for No for an item, the system will search for the next record, if any, in the Substitution Block of the base item. It will not query the ITEM record of the first substitute item to see whether this item has its own substitutes.
See the following diagram for a detailed example of multi-level chaining logic.
FIELD DESCRIPTIONS (SUBSTITUTION BLOCK)

OPERATIONS 2 GUIDE 4.2* 229
Item Substitution for Outbound Shipping
1 Enter ITEM.
2 Retrieve the item to which you wish to add a substitute item.
3 Click on Quantity Breakdown Block and Substitution Block.
White telephones — a substitute for red — are in stock and order is allocated.
You wish to ship black telephones but have no black telephones in stock.
Allocation checks to see whether there is any stock for green, blue or yellow telephones, which are all valid substitutes for black.
If there is no stock for green, blue or yellow telephones, allocation searches for substitutes for blue telephones whose Chain flag has been set to Yes.
Because there is no stock for either red or green telephones, allocation searches for substitutes for red telephones.
Base item = Black Telephone
Substitution Block (Black)
Green Telephone Chain = No
Blue Telephone Chain = Yes
Yellow Telephone Chain = No
Substitution Block (Blue)
Red Telephone Chain = Yes
Green Telephone Chain = No
Substitution Block (Red)
White Telephone Chain = No

Substitution Block
4 Click on Create Record.
5 In the Sequence field, key in 1 as your sequence number and press Enter.
6 Use your pick list to select the first substitute item. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and press F3 to select it. 
7 Key in O for Outbound and press Enter.
8 Key in the appropriate Chain option (Y for Yes or N for No) and press Enter.

Substitution Block showing two substitute items — one chained and one not chained

OPERATIONS 2 GUIDE 4.2* 231
9 If you have another substitute item to add, key in another line in the Substitution Block and press Enter after each field. If you have finished entering your substitute items, click on Return to Main and Master 
Block. Then click on Exit to exit ITEM.

### Entering an Order in ENOR <a id="entering-an-order-in-enor"></a>

Item substitution requires an order line type of P for Pending in ENOR.
1 Enter ENOR.
2 Enter the header information for the order in the normal manner.
3 In the Line Block, set the line type to P for Pending.
4 Enter your level 1 value.
5 If required, enter any level 2 or higher values.

ENOR screen showing P-type line
6 Enter the rest of the order line normally.
7 Enter your remaining order lines or click on Return to Main, Master Block and Exit to exit.

OPERATIONS 2 GUIDE 4.2* 233

## Kitting <a id="kitting"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

A kit is two or more items belonging to the same customer that are assembled together and shipped as one entity. The items are received and stored in the warehouse as individual items in separate locations. If the kit belongs to a broker customer, the kit items can belong to any customer that the broker customer is authorized to ship.
A kit could be a snack pack containing one package of potato chips and one package of corn chips. You receive the potato chips and corn chips as separate items and store them in separate locations. When an order comes in for snack packs, you assemble the product and ship it as a kit.
A kit could also be a complete stereo set consisting of a receiver, tuner, tape player and a pair of speakers. 
You receive the stereo components as individual items and ship them out in kit form as a single unit.
A kit consists of two elements:
 the master or kit item
 the kit components
A kit component can be specific to one kit or can be attached to multiple kits; for example, monitor 1 can be part of computer kit A, computer kit B and computer kit C. As well, kit components can be shipped out as regular items — that is, not part of any kit.
There are two types of kits in AccellosOne 3PL:
 build and ship kits in which the kit components are picked and assembled at the time of order creation and shipped out of the warehouse as a regular item
 pre-built kits in which the kit components are assembled ahead of time and received back into inventory as a single item; when an order is received for the item, the kit is shipped as a regular item
NOTE Kit components can have different billing profiles, quantity breakdowns, shipping profiles, etc.; for example, component 1 could have a breakdown of pallets/ cases while component 2 could have a breakdown of cartons and eaches. Likewise, the billing profile, quantity breakdown and shipping profile of the master item may differ from that of the kit components.
ITEM
ITEM ITEM ITEM
Kit Item
 Kit flag = Yes
 Kit Block contains kit components
Kit Components
 Kit flag = No
 no Kit Block

OPERATIONS 2 GUIDE 4.2* 235

### Setting Up Kits <a id="setting-up-kits"></a>

There are two steps to follow in setting up a kit:
 setting up your kit components
 setting up your master item

### SETTING UP THE KIT COMPONENTS <a id="setting-up-the-kit-components"></a>

Kit components are set up like regular items.
1 Enter ITEM.
2 Create the kit components. Kit components are regular items in ITEM with their own billing profile codes, quantity breakdown profile codes, shipping profiles, etc.
3 Make sure that the Kit field is set to N for No. Kit components do not have a Kit Block attached.
4 Complete the ITEM blocks — Quantity Breakdown Block, Substitution Block and Alternate Reporting 
Block — in the usual manner.
5 Enter ITSH and retrieve the kit component’s item shipping profile. In this profile, make sure that the Ship by Weight flag is set to D for Disallow.
6 Repeat steps 3 to 5 until you have entered all of the kit components separately in ITEM.

### SETTING UP THE MASTER ITEM <a id="setting-up-the-master-item"></a>

Master items have the Kit flag set to Yes and a Kit Block containing all the kit components.
FIELD DESCRIPTIONS FOR KIT BLOCK
Customer Code The customer code for the kit component. If you are setting up a master item for a broker customer, the customer code in this field will be the owner of the item that the broker customer is authorized to ship.
Item Code The item code of the kit component.
Quantity The quantity of the kit component.
Hold Code If you specify a hold code for a kit component, only product on that hold can be added to the kit during allocation.
Sequence Optional
The sequence number of the kit component. When you enter a kit order in 
ENOR, the lines for the kit component will be generated according to the sequence number. If you do not enter sequence numbers for the kit components, the lines for the kit components will be generated in the order in which you enter the components in the Kit Block of ITEM.

1 Enter ITEM. 
2 Create your master or kit item as a separate entity in ITEM. The kit is a separate item with its own profiles that can differ from those of the component items.
3 Set the Kit flag to Y for Yes. This will allow you to enter the Kit Block when you finish adding your item.
4 Once you complete the ITEM fields including the Quantity Breakdown Block, click on Substitution Block.
5 Click on Alternate Reporting Block.
6 Click on Kit Block.
7 Click on Create Record.
8 In the Customer Code field, key in your customer code and press Enter.
9 In the Kit Block, key in your first component and press Enter.
10 Key in the quantity of the first component that you wish to place in the kit and press Enter.
11 If required, key in a hold code and press Enter.
12 Key in your sequence number and press Enter or press Enter without entering a value to bypass the 
Sequence field.
13 Key in your second kit component and press Enter. 
14 Key in the quantity of your second kit component and press Enter.
15 Key in your sequence number and press Enter.
16 Repeat steps 11 to 13 for each additional kit component that you want to add to the master item.

Kit Block of ITEM showing kit components
17 When you finish entering your kit components for the master item, click on Return to Main to exit create mode. Then click on Master Block and Exit to exit the program.

### DELETING A KIT <a id="deleting-a-kit"></a>

You delete or break up a kit by changing the Kit flag in ITEM for the master item to N for No. 
1 Enter ITEM. 
2 Look up the master item.

OPERATIONS 2 GUIDE 4.2* 237
3 Set the Kit flag to N for No. When you set this flag to No, the Kit Block is deleted and the kit components are no longer attached to the master item.
4 Click on Return to Main and Exit to exit.

### MODIFYING A KIT <a id="modifying-a-kit"></a>

You modify a kit by entering the Kit Block of the master item and adding or removing the appropriate components.
1 Enter ITEM. 
2 Look up the master item.
3 Click on Quantity Breakdown Block.
4 Click on Substitution Block.
5 Click on Alternate Reporting Block.
6 Click on Kit Block.
7 To add a kit component, click on Create Record. To remove a kit component, use your arrow keys to position your cursor over the item to be removed and press Enter. Then click on Delete.
8 When you finish making your changes, click on Return to Main and Master Block. Then click on Exit to exit.

### Creating a Build and Ship Kit <a id="creating-a-build-and-ship-kit"></a>

A build and ship kit is a kit in which the kit components are picked and assembled at the time of order creation and shipped out of the warehouse. The kit components are regular inventory items that you can look up in 
LOEN. The master item, on the other hand, appears in ENOR and LOOR only; you cannot look it up in LOEN.
Before you begin, make sure that you have the following:
 a master item with the Kit flag set to Yes
 component items attached to the Kit block of the master item with their respective quantities
 inventory available to be shipped out
 a custom pick document created by HighJump

### PROCEDURE <a id="procedure"></a>

In this procedure, you use the following order types and line types:
Order type = R for Regular
Line type for master item = K for Kitted
Line type for kit components = P for Pending (generated by system)
A build and ship kit order can contain any number of both kit and non-kit items. For example, you could add to the same order three separate kit items plus two non-kit items. For the kit items you would set the line type to 
K for Kitted, while for the non-kit items you would set the line type to R for Regular.
1 Enter ENOR.

2 Key in your customer code and press Enter. The system will automatically fill in the customer’s name and address information.
3 Key in your consignee code and press Enter.
4 Key in your sold-to code and press Enter.
5 Enter the remaining details in the Header Block of the order.
6 When you enter the Line Block, the cursor should be positioned in the Type field. Key in K for kit line type and press Enter.

Type field set to K in the Line Block of ENOR
7 Press Enter until your cursor is positioned in the Item Code field.
8 Key in the master item and press Enter.

OPERATIONS 2 GUIDE 4.2* 239

Line Block of ENOR
9 Press Enter to bypass your level 2/3/4 values.
10 In the Ordered Quantity and To Ship Quantity fields, key in the number of kits that you wish to ship and press Enter. The system will perform the following actions when you enter your quantities:
 it will display the master item’s weight code, unit weight, gross weight and net weight
 it will create one P-type order line for each kit component in the kit
 it will position your cursor in the Type field of the next line
For example, if your master item contains three components, your line count will now read 5 of 5. Line 1 will be for the master item, the next three lines will be for the kit components and line 5 will be your next line for any additional items or kits. 
NOTE The order line for the master item in ENOR contains the item code for the master item and the number of kits that you wish to ship but no location information. 
Only kit components can have locations because at this point the master item has yet to be built and therefore has no inventory.

11 Click on Master Block to exit the Line Block and return to the Header Block.
If you wish to review the kit components attached to the kit, click on Line Block and then use your up and down arrow keys to view each order line.
12 Click on Exit to exit ENOR.
13 Complete all the necessary process flows for this order and then confirm it.

### LOOKING UP THE MASTER ITEM ORDER LINE FOR A KIT COMPONENT <a id="looking-up-the-master-item-order-line-for-a-kit-component"></a>

The Component for Kit Line field in LOOR (Look Up Orders) shows the master item order line number for each kit component.
LOOR screen showing kit component line 2 matched to master item on order line 1
If you wish to add additional kits to the order:
If you wish to ship the order with a single kit:
a) Repeat steps 7 to 10 the necessary number of times until all of the kit orders have been entered.
b) When all your kit orders have been entered, click on Return to 
Main to return to main mode. The system will display the last created line.
a) Click on Return to Main to return to main mode. The system will display the last created line.

OPERATIONS 2 GUIDE 4.2* 241

### Creating a Pre-Built Kit <a id="creating-a-pre-built-kit"></a>

A pre-built kit is a kit in which the kit components are assembled ahead of time and received back into inventory as a single item; when an order is received for that item, the kit is shipped as a regular item.
After you ship a pre-built kit, the individual components are no longer considered to be “in inventory”; if you wish to look the item up in LOEN, you must do so under its master item code.
Before you begin, make sure that you have the following:
 a master item with the Kit flag set to Yes
 component items attached to the Kit block of the master item with their respective quantities
 inventory available to be picked and built into a kit

### CREATING THE KITTED ORDER <a id="creating-the-kitted-order"></a>

In this procedure, you use the following order types and line types:
Order type = K for Kitted
Line type for master item = K for Kitted
Line type for kit components = P for Pending (generated by system)
Because you are not actually shipping product out of the warehouse, you do not require a real consignee, carrier or sold-to code. You can use your N/A codes, you can create special codes called KIT for your carrier and consignee or you can use a manual consignee, carrier and sold-to if this function is activated on your system.
You can have multiple kits on the same order but you cannot mix kits and non-kit items. If you add non-kit items to a K-type order, those items will be deleted when you receive your kits back into inventory.
1 Enter ENOR.
2 Press F9 to position your cursor in the Order Type field.
3 Key in K as your order type and press Enter.
4 Key in your customer code and press Enter.
TIP If you press F12 instead of Enter, the system will take you to the next mandatory field. This command allows you to bypass all the optional fields in ENOR.

Enter Orders (ENOR) screen showing Order Type set to K
5 Press Enter to position your cursor in the Consignee Code field.
6 Key in your consignee code and press Enter. If you have set up a consignee code called KIT, you can enter this code rather than a real consignee. If your system has been configured to allow manual consignees, you can enter a backslash (/) in this field and type in the word KIT in the Name field.
7 Key in your sold to code and press Enter. If your system has been configured to allow manual sold-to’s, you can enter a backslash (/) in this field and type in the word KIT in the Name field.
8 Enter any required values in the Order Date, To Ship Date, To Arrive Date, Customer Order Number and 
Purchase Order Number fields.
9 Key in your carrier code and press Enter. If you have set up a carrier code called KIT, you can enter this code rather than a real carrier. If your system has been configured to allow manual carriers, you can enter a forward slash (/) in this field and type in the word KIT in the Name field.
10 Press Enter on each field in the Header Block until the Line Block appears.
11 When the Line Block appears, you will notice that the value in the Type field has been preset to a K. 
Press Enter until the cursor is at the item code field.
12 Key in your master item for the kit and press Enter.
Order type = K

OPERATIONS 2 GUIDE 4.2* 243

Line Block of ENOR
13 If your master item has a second, third or fourth level of inventory such as lot number, pallet ID, etc., press Enter to bypass these fields. You enter the second, third and fourth levels of a master item when you receive it back into inventory.
14 In the Ordered Quantity and To Ship Quantity fields, key in the number of kits that you wish to pre-build and press Enter. The system will perform the following actions when you enter your quantities:
 it will display the master item’s weight code, unit weight, gross weight and net weight
 it will create one P-type order line for each kit component in the kit
 it will position your cursor in the Type field of the next line
For example, if your master item contains three components, your line count will now read 5 of 5. Line 1 will be for the master item, the next three lines will be for the kit components and line 5 will be your next line for any additional items or kits. 
NOTE The order line for the master item in ENOR contains the item code for the master item and the number of kits that you wish to pre-build but no location information. Only kit components can have locations because at this point the master item has yet to be built and therefore has no inventory.

15 Click on Master Block to exit the Line Block and return to the Header Block.
If you wish to review the kit components attached to the kit, click on Line Block and then use your up and down arrow keys to view each order line.
16 Click on Exit to exit ENOR.
17 Complete all the necessary process flows for this order including allocation and then confirm it. When you confirm the order, the receipt number will be displayed on your screen. 

Receipt Number displayed in CHOF
18 Make a note of this number as you will need it to receive the kit back into inventory.

### LOOKING UP THE RECEIPT NUMBER IN LOOR <a id="looking-up-the-receipt-number-in-loor"></a>

If you were unable to note the receipt number of the kitted order during order confirmation, you must query the order in LOOR. Once you have the receipt number, you can receive the kit in ENRE.
1 Enter LOOR (Look Up Orders).
If you wish to add additional kits to the order:
If you wish to ship the order with a single kit:
a) Repeat steps 10 to 13 the necessary number of times until all of the kit orders have been entered.
b) When all your kit orders have been entered, click on Return to 
Main to return to main mode. The system will display the last created line.
a) Click on Return to Main to return to main mode. The system will display the last created line.

OPERATIONS 2 GUIDE 4.2* 245
2 In the Order Number field, key in the order number of the kitted item and click on Execute Query. The order that you query should display on your screen.

Header Block of LOOR showing order 1963 assigned to receipt 1487
3 In the Transfer Receipt field on the left-hand side of the screen, you will see a number. This number is the receipt created from the kit type order. 
4 Click on Exit to exit.

### LOOKING UP THE RECEIPT NUMBER IN LORE <a id="looking-up-the-receipt-number-in-lore"></a>

You can also look up the receipt number for a kitted order by performing a query in the Reference Number field of LORE.
1 Enter LORE (Look up Receipt).
2 Press Enter to position your cursor in the Reference Number field.
3 In the Reference Number field, key in the order number for the kitted order and click on Execute Query.
Receipt number for kitted order

LORE screen showing order 1963 assigned to receipt 1487
4 When the receipt is displayed, you will see in the Receipt Number field the receipt number for the kitted order.
5 Click on Exit to exit.

### RECEIVING THE KIT BACK INTO INVENTORY <a id="receiving-the-kit-back-into-inventory"></a>

In this procedure, you receive the kit back into inventory. The system will create one receipt line for each master item that you added to your order; the receipt will contain the master item or items only; the kit components are now considered part of the master item and are no longer available as separate entities.
When you receive the kit back into inventory, the kit item is treated as a regular receipt and all normal receipt, renewal and accessorial charges for the master item apply. If you do not charge initial storage and handling when you build a kit, you would have to attach no charge type IISP and IHAP profiles to the master item.
1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in your receipt number in the Receipt Number field and click on Execute Query. The system will display a K-type receipt for the kit.
Order number for receipt

OPERATIONS 2 GUIDE 4.2* 247

ENRE screen showing receipt of kitted item
4 If the master item has been defined as having multiple inventory levels, click on Line Block and enter your lot number, pallet ID, etc.
5 Complete all the necessary process flows for the receipt and then confirm it.

### Allocating Kits <a id="allocating-kits"></a>

Kit orders will only be allocated if there is sufficient product to allocate each kit component. If there is a single kit component that cannot be allocated, the entire kit order will remain unallocated.
Kit order allocation will be based on the ILOP parameters of the individual kit components. If you are receiving the kit back into inventory, any inbound allocation will be based on the ILOP parameters of the master item.

### Modifying Kit Orders <a id="modifying-kit-orders"></a>

If required, you can modify kit orders in ENOR at any time up to order confirmation. You can change the order quantities of kit components as well as delete one or more kit components. You change order quantities by entering ENOR and modifying the order quantity. You delete kit components by entering ENOR and deleting the appropriate order line.

### Reports <a id="reports"></a>

See the Standard Reports Guide.

OPERATIONS 2 GUIDE 4.2* 249
ALLOCATION BY WEIGHT FOR KIT 
ITEMS

## Allocation By Weight For Kit Items <a id="allocation-by-weight-for-kit-items"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

An allocation by weight kit is a kit in which the kit components are defined by weight rather than by number of units. For example, kit item 1 contains three components: 10 pounds of item A, 15 pounds of item B and 20 pounds of item C.
Kit components can be allocated by weight or number of units depending on the master item to which they are attached. For example, the same kit component can be allocated by weight for one master item and allocated by number of units for another master item. However, the master item itself must be defined as either an allocation by weight kit or an allocation by units kit; it cannot be both.

### Setting Up Kits <a id="setting-up-kits"></a>

There are four steps to follow in setting up a kit with allocation by weight:
 you select your ship by weight rounding option in ITSH for the master item
 you set up your kit components in ITEM
 you set up your master item in ITEM
 if you want AccellosOne 3PL to assign a system-generated number to the master item that will be attached to the master item when you receive it back into inventory, you must attach two special verify programs to your depositor workflow profile in DIFP 

### SELECTING YOUR ROUNDING OPTION IN ITSH FOR THE MASTER ITEM <a id="selecting-your-rounding-option-in-itsh-for-the-master-item"></a>

The Ship by Weight Rounding Method field in ITSH determines how you want AccellosOne 3PL to handle scenarios where the allocated weight does not match the order weight because the allocated weight does not correspond to a specific number of units. This value must always be set to U for Up for the master item.
The Ship by Weight Rounding Method value can be set to either U for Up or D for Down for any kit components, but this value is ignored when the kit component is shipped out as part of a kit.
1 Enter ITSH.
2 Retrieve the item shipping profile code that you wish to modify.

OPERATIONS 2 GUIDE 4.2* 251

ITSH screen showing rounding method of D for Down selected
3 Make sure that the Ship by Weight field is to set to N for Net or G for Gross.
4 Make sure that the Ship by Weight Rounding Method field is set to U for Up.
5 When you finish making your changes to ITSH, click on Return to Main and Exit to exit.

### SETTING UP THE KIT COMPONENTS <a id="setting-up-the-kit-components"></a>

Kit components are set up like regular items.
1 Enter ITEM.
2 Create the kit components. Kit components are regular items in ITEM with their own billing profile codes, quantity breakdown profile codes, shipping profiles, etc.
3 Make sure that you attach the modified ITSH profile to your kit components. Ship by weight must be activated in ITSH for each kit component.
4 Make sure that the Kit field is set to N for No. Kit components do not have a Kit Block attached.
5 Complete the ITEM blocks — Quantity Breakdown Block, Substitution Block and Alternate Reporting 
Block — in the usual manner.
6 Repeat steps 3 and 4 until you have entered all of the kit components separately in ITEM.

### SETTING UP THE MASTER ITEM <a id="setting-up-the-master-item"></a>

Master items have the Kit flag set to Yes and a Kit Block containing all the kit components. As well, the Order 
Line Type for Kit Components must be set to W for Weight.
1 Enter ITEM. 
2 Create your master or kit item as a separate entity in ITEM. The kit is a separate item with its own profiles that can differ from those of the component items.
3 Set the Kit flag to Y for Yes. This will allow you to enter the Kit Block when you finish adding your item.
4 In the Order Line Type for Kit Components field, key in W for Weight and press Enter.
FIELD DESCRIPTIONS FOR KIT BLOCK
Item Code The item code of the kit component.
Weight The weight of the kit component.
Weight Measure Code The kit component’s weight measure code as defined in ITEM. You can override this weight measure code if required.
Sequence Optional
The sequence number of the kit component. When you enter a kit order in 
ENOR, the lines for the kit component will be generated according to the sequence number. If you do not enter sequence numbers for the kit components, the lines for the kit components will be generated in the order in which you enter the components in the Kit Block of ITEM.

OPERATIONS 2 GUIDE 4.2* 253

ITEM screen showing Order Line Type for Kit Components set to W for Weight
5 Once you complete the ITEM fields including the Quantity Breakdown Block, click on Substitution Block.
6 Click on Alternate Reporting Block.
7 Click on Kit Block.
8 Click on Create Record.
9 In the Kit Block, key in your first component and press Enter.
10 Key in the weight of the first component that you wish to place in the kit and press Enter.
11 If required, key in a new weight measure code to replace the item’s default weight measure code and press Enter.
12 Key in your sequence number and press Enter or press Enter without entering a value to bypass the 
Sequence field.
13 Key in your second kit component and press Enter. 
14 Key in the weight of your second kit component and press Enter.
15 If required, key in a new weight measure code to replace the item’s default weight measure code and press Enter.
16 Key in your sequence number and press Enter.
17 Repeat steps 13 to 16 for each additional kit component that you want to add to the master item.

Kit Block of ITEM showing kit components
18 When you finish entering your kit components for the master item, click on Return to Main to exit create mode. Then click on Master Block and Exit to exit the program.

### MODIFYING YOUR WORKFLOW PROFILE IN DIFP <a id="modifying-your-workflow-profile-in-difp"></a>

If you want AccellosOne 3PL to assign a system-generated number to the master item that will be attached to the master item when you receive it back into inventory, you must attach the MKRO (Make Kit Receipt from 
Kit Order Lines) special verify program to the COOR flow in your depositor workflow profile in DIFP.
1 Enter DIFP.
2 Retrieve the depositor workflow profile attached to the customer whose items you wish to ship out and receive back in as a pre-built kit.
3 Click on In/Out/Repi/Relo Block and use your down arrow key to select Outbound.
4 Click on Flow Block.
5 Select the flow COOR.
6 Click on Document Block then on Special Verify Block.
7 In the Special Verification Block, key in 10 as your sequence number and press Enter.
8 Key in MKRO and press Enter.
9 Press Enter to accept the default values in the Complete, Sequence and Display fields.
10 Click on Return to Main.

OPERATIONS 2 GUIDE 4.2* 255

DIFP screen showing MKRO attached to the flow COOR
11 Click on Document Block, Flow Block and In/Out/Repi/Relo Block.
12 When you finish setting up your special verify program, press F4 the required number of times to exit 

### ASSIGNING A SYSTEM-GENERATED NUMBER TO THE MASTER ITEM <a id="assigning-a-system-generated-number-to-the-master-item"></a>

If you want AccellosOne 3PL to create a system-generated lot or other number for the master item, you must attach the AIKL (Assign Inventory Level to Kit Line) special verify program to early order flows in your workflow profile such as ENOR or SUAL.
You must also perform the normal setup for system-generated numbers in NUSE (Number Series), DIAP (Depositor Inventory Assign Profile) and DILP (Depositor Inventory Level Profile). See the Setup Guide for further information.
1 Enter DIFP.
2 Retrieve the depositor workflow profile that you wish to set up.
3 Select Outbound in the Inbound/Outbound/Replenishment/Relocation Block.
4 Select the flow at which you wish the lot number to be generated.
5 Go to the Special Verifier Block and add a new record for AIKL. If you are attaching the special verify to your ENOR flow, make sure that you set the Sequence field to A for After.

DIFP screen showing AIKL attached to the flow ENOR
6 When you finish your setup, click on F4 the required number of times to exit DIFP.

### Creating a Build and Ship Kit <a id="creating-a-build-and-ship-kit"></a>

A build and ship kit is a kit in which the kit components are picked and assembled at the time of order creation and shipped out of the warehouse. The kit components are regular inventory items that you can look up in 
LOEN. The master item, on the other hand, appears in ENOR and LOOR only; you cannot look it up in LOEN.
Before you begin, make sure that you have the following:
 a master item with the Kit flag set to Yes
 component items attached to the Kit block of the master item with their respective weights
 inventory available to be shipped out
 a custom pick document programmed by HighJump

### PROCEDURE <a id="procedure"></a>

In this procedure, you use the following order types and line types:
Order type = R for Regular
Line type for master item = K for Kitted
Line type for kit components = W for Weight (generated by system) until line is allocated

OPERATIONS 2 GUIDE 4.2* 257
A build and ship kit order can contain any number of both kit and non-kit items. For example, you could add to the same order three separate kit items plus two non-kit items. For the kit items you would set the line type to 
K for Kitted, while for the non-kit items you would set the line type to R for Regular.
1 Enter ENOR.
2 Key in your customer code and press Enter. The system will automatically fill in the customer’s name and address information.
3 Key in your consignee code and press Enter.
4 Key in your sold-to code and press Enter.
5 If you want AccellosOne 3PL to generate a lot number for master item, you must enter a warehouse code.
6 Enter the remaining details in the Header Block of the order.
7 When you enter the Line Block, the cursor should be positioned in the Type field. Key in K for kit line type and press Enter.

Type field set to K in the Line Block of ENOR
8 Press Enter until your cursor is positioned in the Item Code field.
9 Key in the master item and press Enter.

Line Block of ENOR
10 Press Enter to bypass your level 2/3/4 values.
11 In the Ordered Quantity and To Ship Quantity fields, key in the number of kits that you wish to ship and press Enter. The system will perform the following actions when you enter your quantities:
 it will display the master item’s weight code, unit weight, gross weight and net weight
 it will create one W-type order line for each kit component in the kit
 it will position your cursor in the Type field of the next line
For example, if your master item contains three components, your line count will now read 5 of 5. Line 1 will be for the master item, the next three lines will be for the kit components and line 5 will be your next line for any additional items or kits. 
NOTE The order line for the master item in ENOR contains the item code for the master item and the number of kits that you wish to ship but no location information. 
Only kit components can have locations because at this point the master item has yet to be built and therefore has no inventory.

OPERATIONS 2 GUIDE 4.2* 259
12 Click on Master Block to exit the Line Block and return to the Header Block.
If you wish to review the kit components attached to the kit, click on Line Block and then use your up and down arrow keys to view each order line.
13 Click on Exit to exit ENOR.
14 Complete all the necessary process flows for this order and then confirm it.

### Creating a Pre-Built Kit <a id="creating-a-pre-built-kit"></a>

A pre-built kit is a kit in which the kit components are assembled ahead of time and received back into inventory as a single item; when an order is received for that item, the kit is shipped as a regular item.
After you ship a pre-built kit, the individual components are no longer considered to be “in inventory”; if you wish to look the item up in LOEN, you must do so under its master item code.
Before you begin, make sure that you have the following:
 a master item with the Kit flag set to Yes
 component items attached to the Kit block of the master item with their respective quantities
 inventory available to be picked and built into a kit
 if you want AccellosOne 3PL to assign a system-generated number to the master item that will be attached to the master item when you receive it back into inventory, you must attach two special verify programs to your depositor workflow profile in DIFP: MKRO (Make Kit Receipt from Kit Order Lines) and 
AIKL (Assign Inventory Level for Kit Line)

### CREATING THE KITTED ORDER <a id="creating-the-kitted-order"></a>

In this procedure, you use the following order types and line types:
Order type = K for Kitted
Line type for master item = K for Kitted
Line type for kit components = P for Pending (generated by system) until line is allocated
Because you are not actually shipping product out of the warehouse, you do not require a real consignee, carrier or sold-to code. You can use your N/A codes, you can create special codes called KIT for your carrier 
If you wish to add additional kits to the order:
If you wish to ship the order with a single kit:
a) Repeat steps 7 to 10 the necessary number of times until all of the kit orders have been entered.
b) When all your kit orders have been entered, click on Return to 
Main to return to main mode. The system will display the last created line.
a) Click on Return to Main to return to main mode. The system will display the last created line.

and consignee or you can use a manual consignee, carrier and sold-to if this function is activated on your system.
You can have multiple kits on the same order but you cannot mix kits and non-kit items. If you add non-kit items to a K-type order, those items will be deleted when you receive your kits back into inventory.
1 Enter ENOR.
2 Press F9 to position your cursor in the Order Type field.
3 Key in K as your order type and press Enter.
4 Key in your customer code and press Enter.

Enter Orders (ENOR) screen showing Order Type set to K
5 Press Enter to position your cursor in the Consignee Code field.
6 Key in your consignee code and press Enter. If you have set up a consignee code called KIT, you can enter this code rather than a real consignee. If your system has been configured to allow manual consignees, you can enter a backslash (/) in this field and type in the word KIT in the Name field.
7 Key in your sold to code and press Enter. If your system has been configured to allow manual sold-to’s, you can enter a backslash (/) in this field and type in the word KIT in the Name field.
TIP If you press F12 instead of Enter, the system will take you to the next mandatory field. This command allows you to bypass all the optional fields in ENOR.
Order type = 
K

OPERATIONS 2 GUIDE 4.2* 261
8 Enter any required values in the Order Date, To Ship Date, To Arrive Date, Customer Order Number and 
Purchase Order Number fields.
9 Key in your carrier code and press Enter. If you have set up a carrier code called KIT, you can enter this code rather than a real consignee. If your system has been configured to allow manual carriers, you can enter a backslash (/) in this field and type in the word KIT in the Name field.
10 Press Enter on each field in the Header Block until the Line Block appears.
11 When the Line Block appears, you will notice that the value in the Type field has been preset to a K. 
Press Enter until the cursor is at the item code field.
12 Key in your master item for the kit and press Enter.

Line Block of ENOR
13 If your master item has a second, third or fourth level of inventory such as lot number, pallet ID, etc., press Enter to bypass these fields. You enter the second, third and fourth levels of a master item when you receive it back into inventory.
14 In the Ordered Quantity and To Ship Quantity fields, key in the number of kits that you wish to pre-build and press Enter. The system will perform the following actions when you enter your quantities:
 it will display the master item’s weight code, unit weight, gross weight and net weight
 it will create one P-type order line for each kit component in the kit
 it will position your cursor in the Type field of the next line

For example, if your master item contains three components, your line count will now read 5 of 5. Line 1 will be for the master item, the next three lines will be for the kit components and line 5 will be your next line for any additional items or kits. 
15 Click on Master Block to exit the Line Block and return to the Header Block.
If you wish to review the kit components attached to the kit, click on Line Block and then use your up and down arrow keys to view each order line.
16 Click on Exit to exit ENOR.
17 Complete all the necessary process flows for this order including allocation and then confirm it. When you confirm the order, the receipt number will be displayed on your screen. 
NOTE The order line for the master item in ENOR contains the item code for the master item and the number of kits that you wish to pre-build but no location information. Only kit components can have locations because at this point the master item has yet to be built and therefore has no inventory.
If you wish to add additional kits to the order:
If you wish to ship the order with a single kit:
a) Repeat steps 10 to 13 the necessary number of times until all of the kit orders have been entered.
b) When all your kit orders have been entered, click on Return to 
Main to return to main mode. The system will display the last created line.
a) Click on Return to Main to return to main mode. The system will display the last created line.

OPERATIONS 2 GUIDE 4.2* 263

Receipt Number displayed in CHOF
18 Make a note of this number as you will need it to receive the kit back into inventory.

### RECEIVING THE KIT BACK INTO INVENTORY <a id="receiving-the-kit-back-into-inventory"></a>

When you receive the kit back into inventory, AccellosOne 3PL will create one receipt line for each master item that you added to your order. The receipt will contain the master item or items only; the kit components are now considered part of the master item and are no longer available as separate entities.
A kit item being received is treated as a regular receipt and all normal receipt, renewal and accessorial charges for the master item apply. If you do not charge initial storage and handling when you build a kit, you would have to attach no charge type IISP and IHAP profiles to the master item.
1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in your receipt number in the Receipt Number field and click on Execute Query. The system will display a K-type receipt for the kit.

ENRE screen showing receipt of kitted item
4 If the master item has been defined as having multiple inventory levels, click on Line Block and enter your lot number, pallet ID, etc.
5 Complete all the necessary process flows for the receipt and then confirm it.

OPERATIONS 2 GUIDE 4.2* 265
