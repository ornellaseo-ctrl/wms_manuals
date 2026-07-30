---
title: "Ajustes de Inventário, Holds e Atributos"
description: "Ajustes manuais e massivos, relocações, holds, atributos e valores de processo do item."
layout: default
---

# Ajustes de Inventário, Holds e Atributos

Ajustes manuais e massivos, relocações, holds, atributos e valores de processo do item.

**Fluxo principal:** `ENAJ/MATR (ajuste) | POHO/MAHO/MOHO (holds) | RELO/MARL (relocacao)`

> Fonte: manuais D, E do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Inventory Maintenance And Adjustments <a id="inventory-maintenance-and-adjustments"></a>

*Manual D — Operations 1*

### Looking Up Inventory Information in LOEN <a id="looking-up-inventory-information-in-loen"></a>

The program Look Up Entity Information (LOEN) allows you to view details of all inventory that is stored in the warehouse. LOEN allows you to view all transactions that have been processed for this product. You can also view the locations where the product is stored and the amounts in each location.
Inventory setup in AccellosOne 3PL uses levels to identify product. Inventory levels are the various identifiable characteristics of an item. Some examples of inventory levels are: Lot Number, Pallet Identification 
Number, Expiry Date and Color. Customers can be set up with up to four inventory levels and each level may also have an optional description field. 
An item together with any of its inventory level combinations is called an inventory entity. For example, Item A, 
Lot Number 100 is one entity and Item A, Lot Number 200 is another entity.
The following are examples of possible inventory level setups for an entity:
Entity Level Setup
Description (Optional)
The product item is all the same model and color. It therefore requires a one- level setup.Level 1: Item 123 AA Printer Model BB
The product item is all the same model but it has various colors. It therefore requires a two-level setup.
Level 1: Item 456
Level 2: Color 
BB Telephone Model C
The product item has different lot numbers and expiry dates. It therefore requires a three-level setup.
Level 1: Item 789
Level 2: Lot: 001
Level 3: Expiry Date:
 Mar.16.99
Sweet Peas

LOEN screen showing the Inventory Block
The LOEN program is made up of the following parts:
 Inventory Block
 Drill Block (only available for inventory with more than one inventory level)
 History Block
 History Details Block
 Location Block 
 Renewal Block
The LOEN program provides inventory entity details such as:
 product availability, that is the number of units that are available, on hand, on order, or on receipt for each inventory level for your customers
 the location where the inventory entity is stored
 the inventory entity’s history (which receipts, orders and adjustments have been performed on the entity)
 history time-stamping activity, i.e. who performed the stamped activity and when
 the last billing renewal date and the next renewal date
Once a receipt has been created in ENRE, the product shows in LOEN as inventory that is “On Receipt”.’ 
After the same receipt has been confirmed, the same product shows in LOEN as inventory that is “On Hand.”
The following diagram shows the various blocks in LOEN.
Inventory levels 1 and 2 and their attached optional descriptions

### THE INVENTORY BLOCK AND QUERYING IN LOEN <a id="the-inventory-block-and-querying-in-loen"></a>

In the Inventory Block of LOEN, you enter the selection criteria for the inventory records that you want to view. 
You can query by:
customer only Completing only the customer code will retrieve all items owned by this selected customer. All Inventory Level One (Item) products will display along with all of their other inventory level combinations — their related entities.
item Completing the customer code and the item code will retrieve the selected item and all of its related entities. The selected Level One plus all of its Level 
2, 3, and higher inventory level combinations will display.
Header Block
History
Details Block
Location
Block
Renewal
Block
This block shows the locations where the inventory in the Header
Block is stored.
EXAMPLE
Location A100 15 CASES
Location A101 10 CASES
Location A102 0 CASES
This block shows the last renewal date and the next renewal date for the product in the Header Block. For each location billing code, the
Renewal Block shows the location billing code, total number of units, gross weight and net weight.
EXAMPLE
LOCATION BILL CODE UNITS
ALL 10 PLT
COOL 4 PLT
This block shows each transaction performed for the inventory in the
Header Block.
EXAMPLE
ER (Enter Receipt) 10 UNITS
CR (Confirm Receipt) 10 UNITS
A (Adjustment) 3 UNITS
EO (Enter Order) -5 UNITS
This block shows the operator who performed the transaction in the
EXAMPLE
JOHN DOE 10:30AM
This block shows the inventory that you are looking up.
EXAMPLE
Item A1
Lot 101
Pallet ID 123

When you enter the customer code and any additional inventory levels that you wish to query on, the 
Inventory Block displays an entity broken down into its component inventory levels. All of the other LOEN blocks for this record refer to this entity. However, when you query on an inventory level (for example, Lot X) 
without specifying a customer, the system will display every entity or customer that has a Lot X. 

LOEN screen showing the Inventory Block

### LOOKING UP ALL INVENTORY ENTITIES FOR A SPECIFIC CUSTOMER <a id="looking-up-all-inventory-entities-for-a-specific-customer"></a>

The following procedure allows you to view all inventory entities that a specific customer has in the system. 
All of the customer’s items (Level 1) will display along with any of their other inventory level combinations. LOEN will display a separate record for each entity.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
inventory level (level 2 and higher)
For product with more than one inventory level and with several entities under that level, you can query on its Inventory Level 2 and higher levels. Completing the customer code, item code and Inventory Level fields up to and including the one that you want to query on will display all entities for the selected inventory level. For example, if you query on a specific Inventory Level 3, all of its entities will display. The information will display in the Drill Block. 
specific entity Completing the customer code, item code and all displayed inventory level fields will retrieve only the record for the selected entity (for example, CUST1, 
ITEM1, Lot 100, Color: Blue).
All details provided in the other LOEN blocks apply to the entity displayed in the Inventory 
Block

2 To view all entities for this customer, key in the customer code. If you do not know the code, use the pick list. Click on Execute Query.
3 Click on Location Block to display the locations where this product is currently stored. If necessary, use the up and down arrow keys to scroll through the locations.

LOEN showing the Inventory and Location Blocks
4 Use the function key buttons to access and view this entity’s details in the History, History Details, 
Renewal and Drill Blocks. These blocks are explained later in this section.
5 Click on Inventory Block. If you want to view the details of another entity for this customer, check the current record counter. If there is more than one record, use the down arrow key to scroll to the next record. 
If you wish to view the inventory of another customer, click on Enter Criteria. Key in the customer code or use the pick list.
If you wish to exit the program, click on Return to Main.

### LOOKING UP ALL INVENTORY ENTITIES FOR A SPECIFIC ITEM <a id="looking-up-all-inventory-entities-for-a-specific-item"></a>

The following procedure allows you to view all inventory combinations (all entities) for one selected item.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
2 Key in the customer code and press Enter. If you do not know the customer code, use the pick list.
3 Key in the item code.
Use the buttons to access the other LOEN 
Blocks

LOEN showing the Inventory and Drill Blocks
4 Click on Execute Query.
5 If a Drill Block does not display, use the function key buttons to access and view the details in the Location, History, History Details and Renewal blocks. (These blocks are explained later in this section.) 
Then, click on Inventory Block and Exit and skip the remainder of the procedure.
If there is a Drill Block, continue with the remainder of the procedure.
6 You must view the detail blocks separately for each entity that is displayed in the Drill Block. In the Drill 
Block, use the up and down arrow keys to place the cursor next to the entity whose details you wish to view. 
Then use the function key buttons to access and view the details in the Location, History, History Details and Renewal blocks. These blocks are explained later in this section.
7 When you have finished viewing this entity’s details, click on Drill Block. 
If you wish to view another entity’s details, use the up and down arrow keys to place the cursor next to the entity whose details you wish to view and use the function key buttons to view its details.
8 When you have finished viewing all of the entities in the Drill Block that you needed to see, click on 
If you wish to view another item or the inventory of another customer, click on Enter Criteria.
If you wish to exit the program, click on Return to Main.

### LOOKING UP A SPECIFIC ENTITY <a id="looking-up-a-specific-entity"></a>

The following procedure will display the inventory for one selected entity.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
A query is made on Item D3
Item D3’s other inventory levels (lot and PID) display in the Drill 
Block

2 Key in the Customer Code and click on Enter. If you do not know the Customer Code, use the pick list.
3 Key in the Item Code and press Enter.
4 In each Inventory Level field that displays, key in the corresponding codes for the entity and press Enter.
5 Click on Execute Query.
6 Click on Location Block to display the locations where this product is currently stored. If necessary, use the up and down arrow keys to scroll through the locations.
7 Use the function key buttons to access and view this entity’s details in the History, History Details and 
Renewal and Blocks. These blocks are explained later in this section.
8 Click on Inventory Block. 
9 If you want to view another record, click on Enter Criteria.
10 If you wish to exit the program, click on Return to Main.

### LOOKING UP ALL ENTITIES FOR A SPECIFIC INVENTORY LEVEL <a id="looking-up-all-entities-for-a-specific-inventory-level"></a>

With the following procedure, you can query on any specific inventory level that is Level 2 or higher. The inventory level that you query on must also have several entities under that level. For example, if you are querying on Lot Number, there must be more than one lot number for this entity (Lot # 101, Lot # 102, Lot # 
103, etc.) 
The results of your query will display in the Drill Block. You can use the following procedure to restrict the records that are retrieved into the Drill Block.
1 Enter LOEN. You are in the Inventory Block.
2 Key in the item code and press Enter. The entity’s other inventory level fields will display for completion. 
3 Key in the applicable data for the inventory levels that you want to query on. 
To view details for all of an item’s inventory levels, key in the item code and click on Execute Query. The 
Drill Block will display details for all of the remaining levels. For example, an entity that has three inventory levels — Item, Lot Number and Color — would display all of the item’s entities with all Lot Number and Color combinations in the Drill Block.
To view details for an item’s specific Level 2 entities, key in the item code and the specific data that you want to query on in Inventory Level 2. Click on Execute Query. The Drill Block will display the specified 
Inventory Level 2’s details for all of the remaining levels. In our example, all of the item’s PID records will display in the Drill Block for the specific lot number that you queried on.

LOEN screen showing the selection criteria in the Inventory Block

LOEN screen showing the Drill Block
4 Use the function key buttons to access and view the details in the History, History Details, Renewal and 
Drill Blocks. These blocks are explained later in this section.
5 Click on Inventory Block. If you wish to view another entity or customer, click on Enter Criteria. 
If you wish to exit the program, click on Return to Main.
Executing this query will display all Customer D’s Item 
D3’s entities
All level 2 (lot) 
and level 3 (PID) entities display for item 
D3

### LOOKING UP ALL INVENTORY LEVEL CODES STARTING WITH A PREFIX <a id="looking-up-all-inventory-level-codes-starting-with-a-prefix"></a>

The following procedure allows you to view all records of an item that start with the prefix that you are searching for.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
2 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
3 Key in the inventory levels in the normal manner until you reach the Inventory Level field that you wish to search by. Key in the prefix you are looking for followed by % (e.g. 32%). 
4 Click on Execute Query. The system displays all of the codes that begin with 32 for the selected Inventory Level. If there is more than one record that meets this criteria, then the information will display in the 

### Drill Block. <a id="drill-block"></a>

5 Use the function key options to access and view the details in the History, History Details and Renewal 
Blocks. These blocks are explained later in this section.
If there is a Drill Block, first use the up and down arrow keys to place the cursor next to the entity whose details you wish to view. Then use the function key options to access and view the details in the History, 
History Details and Renewal Blocks.
6 Click on Inventory Block. 
7 If you want to view other records, click on Enter Criteria. If you wish to exit the program, click on Return to Main.
The Drill Block only displays if all of the following criteria are met:
 the entity has more than one inventory level, that is, it has Inventory Level 2 and possibly more levels 
 the inventory level that you are querying on (Level 2 or higher) has more than one record. For example, if you are querying on the inventory level lot number, there must be more than one lot for this entity (Lot 
# 101, Lot # 102, Lot # 103, etc.).
Inventory records in the Drill Block are sequenced according to the value that you selected in the FIFO/LIFO 
Based on field in PIPR (Picking Profile). There are five possible options in this field: receipt date, expiry date, inventory level 2, inventory level 3 and inventory level 4.
When you have multiple records for the same receipt date/expiry date/level 2, etc., AccellosOne 3PL will sort the records in ascending alphanumeric sequence. This means that even if you enter numbers as your level 2 value — for example, lot number — the system will treat these numbers as alphanumeric characters and sort them accordingly. As a result, your lots may appear to be out of sequence when you look up inventory in 
LOEN, perform allocation or run reports.
EXAMPLE
If you receive item A1, lot 1001 and item A1, lot 9, the two inventory entities will be sorted in ascending alphanumeric order as follows:
Lot 1001 will be listed before lot 9 because 1 is less than 9.
In order to avoid this sort sequence, you must define a fixed length for all your lots numbers and add leading zeros to all lot numbers that are less than the fixed length. For example, if the fixed length of your lot number is five characters and you are receiving lot # 6, you must enter 00006 — not 6.

LOEN screen showing lot 107 listed before lot 9
FIELD DESCRIPTIONS
Level 2 The item’s inventory level 2 data.
Level 3 The item’s inventory level 3 data.
Available Indicates the number of units of this entity that are in the warehouse for filling orders. See the “Available” field in the Location Block for the available formula. 
On Hand The total units of this entity that are Available, On Order and On Hold.
It would be necessary to remove units On Order from an unconfirmed order before they are actually available for shipping out. It would be necessary to remove the hold from units with non-shippable hold codes before they are actually available for shipping out.
On Order Indicates the number of units of this entity that are currently allocated to an unconfirmed order. Once the order is confirmed, the number will be subtracted from the On Hand Total.

### LOCATION BLOCK <a id="location-block"></a>

The Location Block shows product availability. It lists the locations in which the entity is currently stored and it provides a breakdown of the amount stored in each location. It also shows if any of this entity is on hold, onorder, in-transit or being replenished.
On Receipt Indicates the number of units of this entity that have arrived at the warehouse and have had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the receipt is confirmed, the product amount will move from the “On Receipt” column to the “On Hand” and “Available” columns.
Quantity Breakdown 
Setup
The entity’s quantity breakdown.
Conveyance Reserved for future use.
In-Transit The amount of this entity that is on its way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. 
For example, the pick location will show -10 cases and the bulk location will show 10 cases. Once the replenishment request has been processed and this amount is moved from the bulk location to the pick location, the replenishment amount for both locations will be zero and the Available amounts for each location will adjust accordingly as in the example below.
Before processing of the replenishment request:
LocationAvailableReplenishment
Bulk A1000 Cases 10 Cases
Pick A1 Case-10 Cases
After processing of the replenishment request:
LocationAvailableReplenishment
Bulk A990 Cases0 Cases
Pick A11 Cases0 Cases
NOTE A negative quantity in the Replenishment column indicates that product is being added to the location.
NOTE If the amounts in the On Order and the Available fields do not equal the total in the On Hand field, this could mean that some units are on a non-shippable Hold. 
Therefore, they are On Hand in the warehouse but are not available to be allocated to an order for shipping. Units that are On Hold display in the Location Block.
FIELD DESCRIPTIONS

If all quantities in a given location equal zero, this means that the product used to be in the location but no longer is. For example, if you move all product in location A100 to location A101, the available, on-hand, on order, on receipt, in-transit and replenishment quantities for location A100 will be set to zero.

LOEN showing the Location Block details
NOTE The fields in the Location Block continue to the right of what initially displays on the screen. Press Enter once to view the In-transit and Replenishment columns. 
Use the tab key to toggle between these columns and the On Order and On Receipt columns.
Totals for each of the corresponding columns above

LOEN screen showing the Location Block details
In the Location Block, you can choose to view either all locations for the entity you have selected or only the non-zero locations. This is useful when you have a large number of locations and you need to see only those locations with a balance.
8 Enter the Location Block of LOEN. The block displays all of the locations for the entity that you are querying on. Press CTRL + A to toggle between the following messages at the bottom of your screen: “Will query all locations” and “Will query only non-zero locations.”
9 When the message “Will query only non-zero locations” displays, click on Drill Block to exit the Location 
Block.
10 Click on Location Block to return to the Location Block. The Location Block will display only non-zero locations for the selected entity.
FIELD DESCRIPTIONS
Warehouse The Warehouse Code where the entity is stored. 
An * in the Warehouse and Location Columns is a temporary repository where the system places units that have been assigned to an order or to a receipt but that have not yet been assigned a location. 
Press the tab key to toggle between the hidden columns and the On 
Order and On 
Receipt columns

Location The Location Code where the entity is stored.
A Location Code with zero units (for example, location A101 in the preceding screen capture) indicates that this entity was stored here before. The entity has since been removed because of relocation, filling an order or an adjustment. If you need further details about this location’s transactions, go into the History Block.
Hold Indicates the type of Hold Code.
Available Indicates the number of units of this entity that is available in the warehouse for filling orders. The formula for calculating this value is as follows:
Available = On Hand - On Order - On Hold
If the available quantity is a negative, the product belongs to a reserve logic customer.
On Hand The total number of units that are Available, On Order and On Hold. 
It would be necessary to remove units On Order from an unconfirmed order before they are actually available for shipping out. It would be necessary to remove the hold from units with non-shippable hold codes before they are actually available for shipping out.
On Order Indicates the number of units that are currently allocated to an unconfirmed order. 
Once the order is confirmed, the number will be subtracted from the Available Total.
On Receipt Indicates the number of units of this entity that have arrived at the warehouse and have had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the receipt is confirmed, the product will move from the “On Receipt” column to the “On 
Hand” column.
Conv. Reserved for future use.
In-Transit The number of units for this entity that are on their way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. For example, the pick location will show -10 cases and the bulk location will show 10 cases. 
Once the replenishment request has been processed and this amount is moved from the bulk location to the pick location, the replenishment amount for both locations will be zero and the Available amounts for each location will adjust accordingly as in the example below.
Before processing of the replenishment request:
Location
Bulk A
Pick A
Available
1000 Cases
1 Case
Replenishment
10 Cases
-10 Cases
FIELD DESCRIPTIONS

### HISTORY BLOCK <a id="history-block"></a>

The History Block allows you to trace all inventory movement for a particular entity from when it was first entered into the system until the present. You can see everything that was done to the inventory. 
The first and second lines along the top of the History Block are headings. The other lines are individual transaction records.
Inventory transactions display as: 
 inventory received into the warehouse (a receipt) 
 inventory shipped out of the warehouse (an order) 
 inventory record that has been corrected (an adjustment)
 inventory placed on hold (a hold)
After processing of the replenishment request:
Location
Bulk A
Pick A
Available
990 Cases
11 Case
Replenishment
0 Cases
0 Cases
NOTE A negative quantity in the Replenishment column indicates that product is being added to the location.
Total The total inventory amount for the corresponding column above.
Quantity Breakdown 
Setup
The entity’s quantity breakdown.
FIELD DESCRIPTIONS

LOEN screen showing History Block
When viewing all details in the History Block, you can arrange the data in either ascending or descending order by date by using the following procedure.
1 Press Ctrl + A. The Help Message Line will indicate “Sequence will be descending.” 
2 Click on Enter Criteria and Execute Query and the data will display in descending order by date.
3 Press Ctrl + A. The Help Message Line will indicate “Sequence will be ascending.” 
4 Click on Enter Criteria and Execute Query and the data will display in ascending order by date.
To query in the History Block for specific information use the following procedure.
5 Enter the History Block.
6 Click on Enter Criteria.
7 Press Enter until the cursor is in the field that you wish to query on and key in your query. For example, if you want to query on Document # 4, press Enter until the cursor is in the Document # field and key in 4.
NOTE The Weight column changes from Gross Weight to Net Weight or vice versa when the cursor is in the History Block and you press Enter.
A hold transaction
A confirmed receipt transaction

8 Click on Execute Query and the information for Document 4 will display. 
FIELD DESCRIPTIONS
Transaction Date The date that the activity took place.
(Transaction) Type The type of activity. The acronyms used stand for:
A (Adjustment)
the inventory was adjusted in ENAJ
BF (Brought Forward)
inventory balances were brought forward after inventory was purged in PURG
CO (Confirmed Order)
the inventory was shipped on a confirmed order
CR (Confirmed Receipt)
the inventory was received on a confirmed receipt
EO (Entered Order)
the inventory is on an open order
ER (Entered Receipt)
the inventory is on an open receipt
HL (Hold Adjustment)
the inventory was placed on hold
IF (Information Only)
the inventory’s weight was adjusted or the level 2 description, expiry date, item value, etc. was modified in CHEI
OM (Order Move)
The inventory was moved as a result of an order move. An order move is a manual movement of inventory that occurs when product on an outbound order is moved from an assigned picking location to any other location (usually but not always an outbound staging or dock location). Order moves typically require an RF program.
PD (Proof of Delivery)
the inventory was shipped and then returned to the warehouse using POD
RL (Relocation)
the inventory was relocated in RELO or MARL
Document # The receipt, order or adjustment number assigned to this transaction.

### HISTORY DETAILS BLOCK <a id="history-details-block"></a>

If the History Details Block option appears at the bottom of your screen, you may enter this block for more information about the transaction. It provides new information about the transaction: the time it was completed, the operator who performed it and the number of item lines involved.
If the transaction is related to an order, you can click on LOOR Block to look up the order. If the transaction is related to a receipt, you can click on LORE Block to look up the receipt.
Units The number of units involved in this order, receipt or adjustment.
Weight Gross/ Weight 
Net
The total gross and net weight involved in the transaction.
Hold The hold code that has been placed on this entity. 
Carrier Name The name of the carrier.
Shipper/Consignee/ReasonThe name of the shipper or consignee involved in the transaction or the reason for the adjustment.
Audit # The audit number for this transaction.
EDI # The EDI number for this transaction.
Reference # 1 The first customer-defined reference number that refers to the inventory, if applicable.
Reference # 2 The second customer-defined reference number that refers to the inventory, if applicable.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.
FIELD DESCRIPTIONS

LOEN screen showing the History Details Block
FIELD DESCRIPTIONS
Time The time the transaction was entered into the system.
Operator The operator who entered the transaction into the system.
Type The transaction type. See [History Block](ajustes-inventario.html#history-block).
Document # The receipt, order or adjustment number assigned to this transaction.
Line The Line Block Line Number from ENRE in which the item involved in the transaction was first entered.
Units The number of units involved in the transaction.
Conv. Reserved for future use.
Hold The type of hold code placed on the item.
Whse The warehouse where this item is stored.
Location The location where this item is stored.

### HISTORY REMARKS BLOCK <a id="history-remarks-block"></a>

If you are in the History Details Block and you see the History Remarks Block button displayed as an option in the Help Message Line at the bottom of your screen, click on the button to view the Remark entries. This shows internal warehouse remarks that were entered by you or other operators to explain various activities that were performed on the selected inventory.

LOEN screen showing the History Remarks Block

### RENEWAL BLOCK <a id="renewal-block"></a>

This block shows the history of renewal transactions for storage of the inventory items.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.
FIELD DESCRIPTIONS
The History 
Remarks 
Block contains explanatory information regarding a transaction that was performed on the selected item

LOEN screen showing the Renewal Block
FIELD DESCRIPTIONS
Period Number The number of times the inventory has been renewed for storage.
Next Renewal Date The date when storage of this entity needs to be renewed and charged again.
Last Renewal Date The date when the current storage period began.
Loc. Bill The location billing code of the location where the inventory item is stored.
Units The number of inventory units for which renewal storage is being charged.
Gross Weight The gross weight of inventory units for which renewal storage is being charged.
Net Weight The net weight of inventory units for which renewal storage is being charged.
Conv. Qty Reserved for future use.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.

LOOKING UP INVENTORY BY ALTERNATE TYPE CODE AND ALTERNATE ITEM 
CODE
You can look up inventory by alternate type code and/or alternate item code if these values have been defined in ALIT (Alternate Item and Language) for a particular item.
1 Enter LOEN.
2 Key in your customer code and press Enter.
3 In the Item field, key in ! followed by your alternate type code or alternate item code.
You can look up inventory by both alternate type code and alternate item code by entering both values. 
For example, if your alternate type code were BX1 and your alternate item code were ALT_ITEM, you would key in !BX1!ALT_ITEM.

LOEN screen showing alternate item code ALT_ITEM
4 Click on Execute Query.

LOEN screen showing all inventory records for ALT_ITEM (equals D3)
5 When you finish looking up your inventory, click on Inventory and Exit to exit.

### Looking Up Locations in LOLO <a id="looking-up-locations-in-lolo"></a>

You use the program Look Up Location Information (LOLO) to view details of warehouse locations, the inventory that they contain and the amount of space that is still available for storing incoming product. 
LOLO has two blocks: the Location Block and the Inventory Block.
1 Enter LOLO.
2 If you want to view data for all locations, click on Enter Criteria and Execute Query. Use the up and down pointer keys to scroll through the locations. 
If you are looking for a specific location, key in the warehouse code and press Enter. Then key in the location code and click on Execute Query.
You can also query by capacity SKU code, % SKU utilized, maximum SKU capacity, isolator code and location type code.
3 Click on Inventory Block. The details of the inventory contained in this location will display. 

LOLO screen
4 If the current record indicator shows that there is more than one entity in this location, use the up and down pointer keys to scroll through the entities. 
5 Click on Location.
6 If you want to view another location and its details, click on Enter Criteria and repeat the procedure. To exit the program, click on Location and Exit.
NOTE When you are in the Location Block, the Inventory Block button will only appear if there is inventory in the location. If there is no inventory in the location, the 
Inventory Block button will be blank.
Location 
Code 
A103 contains four entities

### LOCATION BLOCK <a id="location-block"></a>

### INVENTORY BLOCK <a id="inventory-block"></a>

FIELD DESCRIPTIONS
Warehouse Code The Warehouse Code.
Location Code The Location Code.
Capacity SKU Code The SKU type that is used to measure the location’s capacity.
% SKU Utilized Percentage of the location that is full.
Maximum SKU Capacity The maximum number of SKU’s that can fit into this location.
Isolator Code The code that indicates the location’s isolation type for storing product that needs to be separated from other product. If it is not an isolation type of location, the code will be N/A (for Not Applicable).
Location Type Code The location type code assigned to the location.
FIELD DESCRIPTIONS
Customer Code The code of the product owner.
Item Code The code for the item.
Inventory Levels The inventory levels of the item.
Hold Code The hold type code attached to product in this location.
Available Indicates the number of units of this entity that is available in the warehouse for filling orders. 
On Hand Indicates the number of units of this entity that is in the warehouse. It is the total for this entity of all units that are Available, On Order and On Hold.
It would be necessary to remove units On Order from an unconfirmed order before they are actually available for shipping out. It would be necessary to remove the hold from units with non-shippable hold codes before they are actually available for shipping out.
On Order Indicates the number of units of this entity that is currently allocated to an unconfirmed order. Once the order is confirmed, the number will be subtracted from the Available 
Total.

On Receipt Indicates the number of units of this entity that has arrived at the warehouse and has had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the receipt is confirmed, the product will move from the “On Receipt” column to the “On 
Hand” column.
In-Transit Indicates the number of units of this entity that is on its way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. For example, the pick location will show -10 cases and the bulk location will show 10 cases. 
Once the replenishment request has been processed and this amount is moved from the bulk location to the pick location, the replenishment amount for both locations will be zero and the Available amounts for each location will adjust accordingly as in the example below.
Before processing of the replenishment request:
Location
Bulk A
Pick A
Available
1000 Cases
1 Case
Replenishment
10 Cases
-10 cases
After processing of the replenishment request:
Location
Bulk A
Pick A
Available
990 Cases
11 Case
Replenishment
0 Cases
0 cases
NOTE A negative quantity in the Replenishment column indicates that product is being added to the location.
Quantity The total quantity corresponding to each of the above columns: On Hand, On Order, 
On Receipt, In-Transit and Replenishment.
SKU Capacity % The percentage of this location’s SKU capacity that is occupied for each of the above columns: On Hand, On Order, On Receipt, In-Transit and Replenishment.
Weight Capacity % Only displays if you press tab key
The percentage of this location’s weight capacity that is occupied for each of the above columns: On Hand, On Order, On Receipt, In-Transit and Replenishment. Weight capacity requires a value in the Weight Limit field of LOCA.
FIELD DESCRIPTIONS

### Entering Adjustments to Inventory Amounts <a id="entering-adjustments-to-inventory-amounts"></a>

You use the program Inventory Adjustments (ENAJ) to correct errors in current warehouse inventory records. 
Transactions made in ENAJ are corrections to internal inventory records and therefore they do not involve any charges. In instances where the type of adjustment code does require a charge, the Bill Later - Enter 
Charges (ENAC) screen appears for completion during the procedure.
There are four types of inventory adjustments that you can perform in AccellosOne 3PL:
 positive adjustments in which you add inventory to the current recorded amount
 negative adjustments in which you subtract inventory from the current recorded amount
 transfer adjustments in which you subtract inventory currently recorded under one customer code/level 
1 value/level 2 value and add it to another customer code/level 1 value/level 2 value
 positive adjustments in which you create new inventory

### QUERYING IN ENAJ <a id="querying-in-enaj"></a>

When you enter ENAJ, you need to instruct the system as to which entity you need to adjust. ENAJ allows you to do this by querying on customer and/or on the item’s inventory levels:
 if you complete the Customer field, all of the customer’s inventory records will display when you click on 
Execute Query
 if you complete the Inventory Level 1 field, all of this item’s records will display 
 if you complete the Customer field, the Inventory Level 1 field (ITEM) and the Inventory Level 2 field (for example Lot Number), all records with this lot number will display when you click on Execute Query
The more information that you enter, the fewer the records that you will have to search through.
Cube Capacity % Only displays if you press tab key
The percentage of this location’s cube capacity that is occupied for each of the above columns: On Hand, On Order, On Receipt, In-Transit and Replenishment.
FIELD DESCRIPTIONS

ENAJ screen
QUERYING IN ENAJ BY PROCESS VALUE
If the item that you are looking up has a process code (IPRO) attached to it, you can query by process code and process value.
1 Enter ENAJ.
2 Press Enter to bypass the Customer Code and Level 1/2/3/4 fields.
ENAJ screen showing prompt for process code and process value
Complete as many of the inventory levels as possible

3 When prompted for the process code and value, key in your process code and press Enter. Then key in your process value and click on Execute Query.

### ENTERING A POSITIVE ADJUSTMENT IN ENAJ <a id="entering-a-positive-adjustment-in-enaj"></a>

You enter a positive adjustment in ENAJ to make inventory corrections that add product to the system records. 
1 Enter ENAJ. The program will be in the Enter Criteria Mode.
2 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels and press Enter. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the amount and the SKU of the entity that you wish to add and press Enter. If you do not enter a 
SKU, AccellosOne 3PL will use the item’s lowest SKU.
The system automatically updates the weight-related fields for standard weight items. For items of nonstandard weight, you will be required to key in the weight data in the corresponding fields.

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date field. 
If this entity has an expiry date or is part of an open lot, the system will automatically populate the corresponding fields.
Key in the amount that you are adding to inventory. Specify the SKU.

9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. Information from this field will print on the Adjustment Audit Report.

ENAJ screen
11 Click on Location Block. The Location Block displays the locations where this entity is currently stored and the amounts in each location.
Complete the adjustment code and adjustment reason fields.

ENAJ screen showing the Location Block
12 Use the up and down arrow keys to move the cursor next to the location where you will be adding the inventory. 
If you need to add the product to a location that is not listed, click on Create Record and then use the pick list to select a location.
Press Enter until the cursor is in the Adjust (From) Column. Key in the amount and SKU that you are adding to this location. Press Enter. 
If you are adding to more than one location, move your cursor to the next location where you will be adding inventory (for example, if you are adjusting ten cases and you place five cases in one location and the remaining five cases in a second location). Repeat until the proof is zero.
Check the Proof 
Box amount.
Set the cursor next to the 
Location Line where you will be adding the quantity that you are adjusting.

ENAJ screen showing the Location Block
13 Click on Process Adjustment.

ENAJ screen showing the Remarks Block
14 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
15 When you finish entering your remarks, click on Return. A message will display providing the number of the adjustment record.
16 If prompted to enter a charge for the transaction, click on Exit.
Press Enter across the Location Line until you are in the 
Adjust Column. Key in the amount that you will be adding to this location.

17 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit ENAJ.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the Adjustment record.

### ENTERING A NEGATIVE ADJUSTMENT IN ENAJ <a id="entering-a-negative-adjustment-in-enaj"></a>

You enter a negative adjustment in ENAJ to make inventory corrections that subtract product from locations in the system records. The procedure is the same as for a positive adjustment except that instead of adding product to a location or locations you will be subtracting quantities. You must therefore enter a negative number in the Adjust Quantity field in ENAJ.
You can also use negative adjustments to correct product that was recorded under an incorrect lot number. 
First, you make a negative adjustment to subtract product from the incorrect lot number. Next, you make a positive adjustment to add product to the correct lot number.
1 Enter ENAJ. The program will be in the Enter Criteria Mode.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the negative amount and the SKU of the entity that you wish to remove from the system and press 
Enter (for example, -5CASE). If you do not enter a SKU, AccellosOne 3PL will use the item’s lowest 
SKU.
The system automatically updates the weight-related fields and fills in the Adjustment Date. If this entity has an expiry date or is part of an open lot, the system will automatically populate the corresponding fields.

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date field. 
9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. This information will print on the Adjustment Audit Report (ADJ01).
11 Click on Location Block. The Location Block displays the locations where this entity is currently stored and the amounts in each location. Use the up and down arrow keys to move the cursor next to the location from which you will be removing the inventory. 
Press Enter until the cursor is in the Adjust (From) Column. Key in the negative amount and SKU that you are removing from this location. Press Enter.
If you are removing product from more than one location, move your cursor to the next location where you will be removing inventory (for example if you are adjusting ten cases and you remove five cases from one location and the remaining five cases from a second location). Repeat until the proof is zero.
Key in the amount that you are removing from inventory. 
This must be a negative SKU amount.

ENAJ screen showing Location Block
12 Click on Process Adjustment.
13 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.

ENAJ screen showing the Remarks Block
14 When you finish entering your remarks, click on Return. A message will display indicating the number of the adjustment record.
15 If prompted to enter a charge for the transaction, click on Exit.
Check the Proof 
Box.
The negative value of the proof must be entered in the to bring the proof to zero.

16 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit ENAJ.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the Adjustment record.

### CHANGING THE PRODUCT’S RECEIVED DATE <a id="changing-the-product-s-received-date"></a>

The product’s received date is the date that the product was confirmed in CHRF. When you perform a transfer adjustment in ENAJ, you can retain the product’s original received date or you can overwrite this date with the current date. You define your received date option in ADJU (Adjustment Type Codes) and then attach the appropriate adjustment type code to your adjustment in ENAJ.
If you select Original as your option in the Date Used for Adjustments / Renewals field in ADJU, the product to which you are applying this adjustment type will retain its original received date and will renew on that date (anniversary monthly and anniversary weekly billing only). 
If you select Current, the product to which you are applying this adjustment type will be assigned the current date as its received date and will renew on the day that the adjustment was made (anniversary monthly and anniversary weekly billing only).

### ENTERING A TRANSFER ADJUSTMENT IN ENAJ <a id="entering-a-transfer-adjustment-in-enaj"></a>

A transfer adjustment in ENAJ allows you to transfer product within the system without creating an invoice. 
You can use this program to adjust inventory records that have incorrect:
 customer codes
 item codes
 inventory level codes
 expiry dates
For example, product that was recorded under an incorrect lot number will need to be subtracted from that lot number and added to the correct one; product that was assigned to the wrong customer will need to be subtracted from that customer and added to the correct one, etc. You begin with a negative quantity in ENAJ since you must first subtract product from the incorrect detail category and then add it to the correct one.
Transfer adjustments do not require that both items have the same quantity breakdown. You can transfer product from a pallet/case item to an each item and vice versa.
1 Enter ENAJ. The program will be in the Enter Criteria mode.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the negative amount and the SKU of the entity that you wish to remove from the system because it was entered incorrectly and press Enter. If you do not enter a SKU, AccellosOne 3PL will use the item’s lowest SKU.
The system automatically updates the weight-related fields and fills in the Adjustment Date. If this entity has an expiry date or is part of an open lot, the system will automatically populate the corresponding fields.

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date field. 
9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. Information from this field will print on the Adjustment Audit Report.
11 Click on Transfer To Block. In this block, you will be entering the product’s correct details. 
12 Key in your customer code and press Enter. 
13 Key in your item code and press Enter. 
14 Key in all of the inventory levels and press Enter. 
Key in the negative amount that you are removing for the adjustment. Specify the SKU.

ENAJ screen showing the Transfer Block
15 The Transfer Quantity field fills in with the amount that you are transferring and the Help Line displays the 
Message, “The Transfer From Quantity is …” Press Enter. 
The system automatically updates the weight-related fields for items with a standard weight. If the item is of non-standard weight, key in the weight details in the corresponding fields.
16 If your system allows the manual entry of expiry dates, you can change the expiry date.
17 Click on Location Block. The Location Block displays the locations where this entity is currently stored and the amounts in each location.
Key in the correct customer code and all inventory levels.
Transfer Quantity field.

ENAJ screen showing the Location Block and the From and To Proof boxes
18 Use your up and down arrow keys to move the cursor next to the location from where you will be subtracting the inventory. 
Press Enter until the cursor is in the Adjust (From) Column. Key in the negative amount and SKU that you are subtracting from this location. Press Enter. 
19 Do one of the following:
20 When you finish entering your from and to locations and quantities, both the From Proof Box and the To 
Proof Box should show a quantity of zero.
21 If you are in create record mode, click on Return to Main to exit create record mode.
If the location to which you wish to transfer the inventory is displayed:
If the location to which you wish to transfer the inventory is NOT displayed:
a) Move your cursor to the location where you want to transfer the inventory. If you wish to transfer inventory to the same location, you skip this step.
b) Press Enter until the cursor is in the Adjust (To) Column. Key in the positive amount and SKU and press Enter. 
a) Press Enter to position your cursor in the Location field.
b) Click on Create Record and key in your to location code.
c) Key in the positive amount and 
SKU and press Enter. 

ENAJ screen showing the Location Block
22 Click on Process Adjustment.
A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
23 When you finish entering your remarks, click on Return. A message will display indicating the number of the adjustment record.
24 If prompted to enter a charge for the transaction, click on Exit.
25 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the adjustment record.

### CREATING NEW INVENTORY IN ENAJ <a id="creating-new-inventory-in-enaj"></a>

1 Enter ENAJ.
2 Click on Return to Main.
3 Click on Create Record.
4 Key in your customer code and press Enter.
5 Key in all inventory levels for the new product and press Enter.
6 In the Adjustment Quantity field, key in the quantity and SKU code of the inventory that you wish to add and press Enter.
In the From 
Adjust Column field, key in the negative amount that you are removing.
In the To Adjust 
Column field, key in the amount that you are adding

7 Press Enter until you reach the Adjustment Code field. Then key in your adjustment code and press 
Enter.
8 Click on Location Block to enter the Location Block.
9 Click on Create Record and enter the location for the new product.
10 Press Enter to bypass the Hold field.
11 Key in your adjustment quantity and press Enter.
12 When the proof equals zero, click on Process Adjustment.
13 If required, enter your remarks for the adjustment.
14 Click on Exit to exit.

### Performing Massive Adjustments in MATR <a id="performing-massive-adjustments-in-matr"></a>

A massive adjustment is an adjustment in which you transfer all product for a particular entity to another inventory entity. For example, you can:
 transfer all product from one item or inventory level to another item or inventory level
 transfer all product for one item from one customer to another 
Unlike ENAJ (Enter Adjustment), you do not specify any quantities in MATR because the adjustment applies to all product for up to the inventory level that you specify.
MATR is typically used when you want to rename an item or customer. You first create your new item or customer code and then you use MATR to transfer over the item(s)/customer. 
The following conditions apply to massive adjustments:
 If you are transferring product from one customer to another, the two customers must have similar inventory level profiles and quantity breakdowns. For example, you cannot transfer an item with two inventory levels to a customer with a single inventory level. Neither can you transfer a pallets/cases/ eaches item to a customer with a pallets/cases quantity breakdown.
 If you are transferring product from one item to another within the same customer, both items must have the same quantity breakdown (for example, both items must be pallet/case items).
 The product that you are adjusting may or may not be assigned a new received date depending on the option that you choose in ADJU (Adjustment Type Code). See [Changing the Product’s Received Date](ajustes-inventario.html#changing-the-product-s-received-date).
NOTE When transferring large numbers of inventory records, it is advisable to run an inventory or location report for the items that you are transferring so you can track the movement of each inventory entity.

When transferring inventory with multiple levels (for example, item/lot number), the following options are available:

### TRANSFERRING INVENTORY — PROCESS ONE OPTION <a id="transferring-inventory-process-one-option"></a>

You use the Process One option in the following cases:
 you are transferring item-only inventory
 you are performing a one-to-one transfer
1 Enter MATR.
2 Key in your customer code and press Enter.
3 Enter all inventory levels for the product that you wish to transfer. If you do not know your second level of inventory, you can perform your query with the Level 2 field blank. When the system retrieves all lots for the item that you specified, you can use your arrow keys to select the lot that you wish to transfer. 
Alternatively, you can transfer all product on a specific receipt by entering your item code and receipt number.
4 Click on Execute Query.
OPTION EXAMPLE PROCEDURE
One to One You wish to transfer item A, lot 1, to item 
B, lot 1.
Use the Process One command in MATR.
Many to One You wish to transfer all lots for item A (lots 
1, 2, 3, 4, etc.) to item B, lot 1.
Use the Process All command in MATR.
Many to Many You wish to transfer all lots for item A (lots 
1, 2, 3, 4, etc.) to equivalent lots for item 
B.
Use the Process All command in MATR.
Many to Many You wish to transfer a range of lots for item 
A (lots 101, 102, 103, 104, etc.) to equivalent lots for item B.
Retrieve the lots that you wish to transfer using the wildcard character (lot = 10%). 
Then use the Process All command in 
MATR.

MATR screen showing lot 101 for item ITEM01
5 Click on Relocate Block.
6 Key in your adjustment code and press Enter.
7 If required, key in an adjustment reason and press Enter.
8 Key in the customer code of the customer to which you are transferring the product and press Enter.
9 Key in all inventory levels for your “to” item. For example, if you are transferring a two-level item (item/ lot), you must specify both the item and lot number in the Relocate Block.

MATR screen showing Process One and Process All options
10 Click on Process One.
11 When the “STOP Do you want to proceed with UPDATE” message appears, key in Y for Yes.
12 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
13 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
14 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.

### TRANSFERRING INVENTORY — PROCESS ALL OPTION <a id="transferring-inventory-process-all-option"></a>

You use the Process All option when you wish to perform a many-to-one transfer or a many-to-many transfer.
1 Enter MATR.
2 Key in your customer code and press Enter.
3 Enter your level 1 value only and then click on Execute Query.

MATR screen showing all lots for ITEM01
4 Click on Relocate Block.
5 Key in your adjustment code and press Enter.
6 If required, key in an adjustment reason and press Enter.
7 Key in the customer code of the customer to which you are transferring the product and press Enter.
8 Key in your level 1 value and press Enter.
9 Do one of the following:
If you are doing a many-to-one transfer:
If you are doing a many-to-many transfer:
a) Enter all your inventory levels. 
For example, if you are transferring a two-level item (item/lot), you must specify both the item and lot number in the Relocate 
Block.
a) Proceed to next step.

MATR screen showing Process One and Process All options
10 Click on Process All.
11 When the “STOP Do you want to proceed with UPDATE” message appears, key in Y for Yes.
12 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
13 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
14 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.

### Relocating Inventory <a id="relocating-inventory"></a>

You use the program Relocate Inventory (RELO) to record changes that involve physical movement of inventory from one location to another in the warehouse. It is used most frequently to record consolidation or rearrangement of warehouse inventory. You can use RELO when the entire inventory amount has been moved from a location or when only a portion of it has been moved. 
The following restrictions apply to RELO:
 You cannot relocate product that is on an open order or receipt.
There are four lots for 
ITEM01

 If the Location Capacity Validation Type field in COMP (Company Code) is set to “No validation for userinitiated transactions”, relocating inventory does not take into account the location’s capacity. You can move inventory into a location that is considered “full”.
 If the product is on non-breakable hold, you must relocate all product in the location; you cannot relocate partial quantities.

### RELOCATING INVENTORY NOT ON HOLD <a id="relocating-inventory-not-on-hold"></a>

1 Enter RELO.
2 Key in the customer code. If you do not know the code, use the pick list to select it. 
3 Key in the inventory levels of the product that you wish to relocate.
4 Click on Execute Query.
5 Click on Location Block.

RELO screen showing the Location Block
6 Check the Available field in the Header Block to ensure that there is sufficient inventory to relocate. This is the total amount available for all locations.
7 The Location Block displays all locations that currently contain or have contained in the past the product to be relocated. Use the up and down arrow keys to move the cursor next to the location from which you will be removing product. 
The Available field in the Location Block shows the amount of inventory in this specific location. An amount of zero indicates that the location used to contain product but is currently empty.
8 Press Enter to move the cursor to the Adjust Quantity field. 
Displays total for all locations where this product is currently stored.
Displays amount in the specified location indicated by the amount.

If you are removing the entire amount of product that is available in this location, click on Delete while your cursor is in the Adjust Quantity field for this location.
If you are removing only part of the full amount that is available in this location, key in the negative value and SKU that you are removing (i.e., -15 CASE) and press Enter. The Proof field will show the number of units that are being removed.
9 Press Enter again to bypass the Conveyance field.
10 Use the up and down arrow keys to place the cursor next to the location where you will be moving the product. If you need to place the product in a location that is not displayed, use the pick list. Press Enter until the cursor is in the Adjust Quantity field. Key in the positive value that is being added here and press 
Enter. The proof indicates the number of remaining SKU’s that still need to be relocated.
If the location is not available in the pick list, click on Create Record. Then key in the location, the number and SKU that you are adding and press Enter. 

RELO screen showing the Location Block
11 Repeat until the proof is zero.
12 Click on Relocate.
13 A Remarks Block displays. If you wish to enter a remark for the relocation, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
14 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
15 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.
Product is being removed (subtracted) 
from location 
A101
The same product is being relocated (added) 
to location 
A102

You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who recorded the relocation. The Document Number is the number of the adjustment record.

### RELOCATING INVENTORY ON HOLD <a id="relocating-inventory-on-hold"></a>

When you relocate inventory on hold, the hold code may or may not “travel” with the inventory depending upon the type of hold. There are two types of holds in AccellosOne 3PL:
 item holds applied manually in HOAD/ENRE or attached automatically to inbound product through setup in IHOP
 location holds defined in LOCA (all product placed in a location with a pre-assigned hold code will be placed on that hold)
Item holds override all location holds and “travel” with the product
Location holds defined in LOCA are removed when the product leaves the location
FROM LOCATION TO LOCATION
Item Location Item Hold
Location Hold
Location Item Hold
Location Hold
EXAMPLE 1 A1 100 DMG 200 DMG
You move 10 units of item A1 from location 100 to location 200. Item A1 in location 100 is on DMG (Damaged) hold and that hold was applied in HOAD. When you relocate the inventory to location 200, the product remains on DMG hold.
EXAMPLE 2 A2 300 DMG 400 DMG QA
You move 10 units of item A2 from location 300 to location 400. Item A2 in location 300 is on DMG hold and that hold was applied in HOAD. When you relocate the inventory to location 400, the item hold of DMG applied in HOAD overrides the location hold of QA (Qualify Assurance) defined in LOCA.
FROM LOCATION TO LOCATION
Item Location Item Hold
Location Hold
Location Item Hold
Location Hold
EXAMPLE 3 A1 100 QA 200
You move 10 units of item A1 from location 100 to location 200. All inventory in location 100 is on QA hold and that hold is a location hold. When you relocate the inventory to location 200, the QA hold is removed.
EXAMPLE 4 A2 300 QA 400 DMG

### RELOCATING INVENTORY ON ITEM HOLD <a id="relocating-inventory-on-item-hold"></a>

When you relocate inventory on item hold, the from location hold code must match the to location hold code in the Location Block of RELO. A match means that both locations have no hold or have the same hold. You cannot move product from location A100 (hold code = DMG) to location A200 (no hold code).
Item holds in RELO have no check mark in the Loc. Hold column.
1 Enter RELO.
2 Key in the customer code and inventory levels of the product that needs to be relocated and press Execute Query.
3 Click on Location Block.
AccellosOne 3PL will show one line for each location/hold code combination. For example, if there are 10 units on hold in location A100 and 10 units not on hold in the same location, the Location Block of RELO will contain two lines: one for the product on hold and another for the product not on hold.
4 Proceed to enter your from and to locations/quantities in the normal manner. The from location and to location hold codes, if any, must match when relocating inventory on manual hold.
You move 10 units of item A2 from location 300 to location 400. All inventory in location 300 is on QA hold and that hold is a location hold. When you relocate the inventory to location 400, which is on DMG hold, the QA hold is replaced by the DMG hold.
NOTE When you relocate inventory on hold, AccellosOne 3PL creates two records in the History Block of LOEN: an RL (Relocation) transaction type with a quantity of zero and a HL (Hold) transaction type with a quantity equal to the quantity that was relocated.
FROM LOCATION TO LOCATION

RELO screen showing inventory on item hold DMG in location A101
5 When the proof quantity is zero, click on Relocate and complete the relocation in the normal manner.

### RELOCATING PRODUCT ON LOCATION HOLD <a id="relocating-product-on-location-hold"></a>

When you relocate inventory on location hold, no match is required between the from location hold code and the to location hold code in the Location Block of RELO. You can move product from any location to any location regardless of the location hold as location hold codes do not “travel” with the product.
Location holds in RELO are indicated by a check mark in the Loc. Hold column. 
1 Enter RELO.
2 Key in the customer code and inventory levels of the product that needs to be relocated and press Execute Query.
3 Click on Location Block.
AccellosOne 3PL will show all locations that currently contain or have contained in the past the product to be relocated.

RELO screen showing inventory in location A105 on location hold of DMG
4 Proceed to enter your from and to locations/quantities in the normal manner.
5 When the proof quantity is zero, click on Relocate and complete the relocation in the normal manner.

### Performing a Massive Relocation of Inventory in MARL <a id="performing-a-massive-relocation-of-inventory-in-marl"></a>

In MARL (Massive Relocate), you perform massive relocations. A massive relocation can involve the movement of any one of the following:
 all product belonging to a particular customer
 all product with a particular level 1, 2, 3 or 4 value
 all product stored in a particular warehouse
 all product stored in a particular location
 all product that has been placed on a particular hold

You can also relocate any combination of the above. For example, all product belonging to customer A, in warehouse 1 on the hold DMG.
There are two relocate options in MARL: you can move a specific inventory entity from one location to another (Process One) or you can move all inventory retrieved in your query to a single location (Process All). 
If the product to be relocated is on hold or if the from or to location is on hold, the rules described in [Relocating Inventory on Hold](ajustes-inventario.html#relocating-inventory-on-hold) apply to each inventory entity. That is, item holds override all location holds and “travel” with the product while location holds defined in LOCA are removed when product leaves the location.
1 Enter MARL.
2 Key in your search criteria. You can query by customer code, any inventory level or combination of inventory levels, from location code, from warehouse code or from hold code. 
3 When you finish entering your query criteria, click on Execute Query. AccellosOne 3PL will display all inventory entities that meet your search criteria.
4 If your query retrieved multiple inventory entities, you can use up and down arrow keys to view each inventory entity.
NOTE You cannot move partial quantities of inventory in MARL. For example, if you have ten units of Item A in location 100, you cannot move five units of this inventory to location 200. If you want to move partial quantities, you must use RELO instead of 
MARL.
TIP When relocating inventory, it is advisable to use the Print function in MARL to print a listing of the inventory that you are relocating so you can track the movement of each inventory entity.

MARL screen showing item A2, lot 101
5 Click on Location Block.
6 Check the Available to Relocate field in the Header Block to ensure that there is sufficient inventory to relocate. This amount is the total amount for the currently selected inventory in the Header Block.
7 Key in the warehouse code to which you are relocating the inventory and press Enter.
8 Key in the location code to which you are relocating the inventory and press Enter. If the to location has an automatic hold, the hold code will display in the Automatic Hold Code field.

MARL screen showing Process One and Process All commands
9 Do one of the following:
10 When the “STOP Do you want to proceed with UPDATE” message appears, click on Yes. If you selected the Process All option, the number of records being relocated will be shown.
11 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
12 When you have finished entering all applicable remarks, click on Return to exit. 
If you wish to relocate only the currently selected inventory in the Header Block:
If you wish to relocate all inventory in the Header Block to a single location:
a) Click on Process One. a) Click on Process All.
Product is being relocated to this warehouse and location.
To location has been assigned a location hold of DMG

MARL screen showing the number of the adjustment record (200) and each inventory entity being relocated
13 If required, you can jot down the number of the adjustment record for future reference. You can also scroll down the External Messages window to view all inventory entities being relocated.
14 When you finish viewing the individual relocation records, do one of the following:
15 If you need to process another adjustment, begin the next transaction. Otherwise, click on Return to Main and Exit to exit.

### Entering Hold Adjustments <a id="entering-hold-adjustments"></a>

In AccellosOne 3PL, product can be put on hold as it is received into the warehouse. Product can also be put on hold after it has been received into the warehouse as normal inventory. Product that is placed on hold must have the hold removed before it can be shipped (unless the hold is defined as shippable in HOLD). 
It is possible to place product on hold either automatically or manually. The following are various ways of putting a hold on product:
 The item always requires a hold to be put on it as it is received into the warehouse. A hold profile defined in IHOP was therefore attached to ITEM so that this product will automatically be placed on hold every time that it is received into the warehouse. The automatic hold code shows as the default in ENRE and is applied as the receipt is created in the program ENRE. 
 The item is stored in a hold-type location. When the receipt was created in ENRE, this item was placed into a hold-type location.
If you wish to print a listing of each relocation transaction:
If you do NOT wish to print a listing of each relocation transaction:
a) Click on Select Printer.
b) Key in your printer code and press Enter.
c) Click Ok.
d) Click on Exit to close the External Messages window.
a) Click on Exit to close the External Messages window.

 The item needs to be placed on hold after it has been received into the warehouse as regular non-hold inventory. This requires a manual hold entry in the program Hold Adjustments (HOAD).
You use the program Hold Adjustments (HOAD) for the following transactions: 
 putting product on hold 
 removing product from hold 
 adjusting existing hold data records

### PLACING INVENTORY ON HOLD IN HOAD <a id="placing-inventory-on-hold-in-hoad"></a>

1 Enter HOAD.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the entity’s other inventory levels if applicable.
5 Click on Execute Query. 
6 Click on Hold Block. This block shows all locations for the product that you queried on in which the product is on hold. If the on hold quantity is zero, that means that the product in the location used to be on hold but is currently free of any hold.

HOAD screen showing the Hold Block
7 Check the Available to Hold field that is located just above the Hold block to verify whether there is enough product for the required hold adjustment. This block shows all locations for the product that you queried on in which the product is currently on hold or was on hold in the past. If the on hold quantity is zero, that means that the product in the location used to be on hold but is currently free of any hold.
Displays total for all locations where this product is currently stored.
Displays the amount in the specified location indicated by the cursor.

There is one record in the Hold Block for each unique combination of location code/hold code. For example, if a given product used to be on hold BF (Blast Freezing) in location A100 and is now on hold DMG (Damaged) in the same location, you would see two records in the Hold Block:
A100BF0CASE
A100DMG5CASE
There are two ways of placing product on hold in HOAD:
if there is an existing record in the Hold Block for the location code/hold code, you modify the existing record if there is no record in the Hold Block for the location code/hold code, you must enter create record mode 
8 Do one of the following:
9 Key in your hold code and press Enter.
10 Check the Available to Hold field at the bottom of the Hold Block to verify the amount of product that is available in this location for the hold adjustment. 
11 Key in the positive value and SKU that you wish to put on hold.
If the product’s location/hold code is shown in the Hold Block:
If the product’s location/hold code is NOT shown in the Hold 
Block:
a) Use your up and down arrow keys to move the cursor next to the location line with the location code and hold code that you need.
b) Press Enter to position your cursor in the Hold field.
a) Click on Create Record.
b) Use your pick list to select the product’s location.

HOAD screen showing the Hold Block
12 Press Enter to complete the line.
13 If the Return to Main button is available, click on Return to Main.

HOAD screen showing the Hold Block
14 Click on Process Hold.
15 The Remarks Block will appear. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
16 When you finish entering your remarks, click on Return to exit.
17 A message will display on the screen showing the number of the adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
18 The cursor will return to the Customer Code field for the next hold transaction. If more product needs to be put on hold, begin the next transaction or click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN, key in the entity and click on History Block) It will show as HL (Hold) Type. You can also check who recorded the adjustment. The document number is the number of the processing adjustment record.

### REMOVING INVENTORY FROM HOLD IN HOAD <a id="removing-inventory-from-hold-in-hoad"></a>

1 Enter HOAD.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the entity’s other inventory levels.
5 Click on Execute Query. 
The adjusted amount from the above screen capture now becomes part of the On 
Hold column.
Click on Process Hold.

6 Click on Hold Block. This block shows all locations for the product that you queried on in which the product is on hold. If the on hold quantity is zero, that means that the product in the location used to be on hold but is currently free of any hold.

HOAD screen showing Hold Block
7 Use the up and down arrow keys to move the cursor next to the location line with the product that needs to be removed from hold.
8 Press Enter until you reach the Adjust column field and key in the negative value and SKU to be removed from hold. If you wish to remove all product in a given location from hold, click on Delete.
Location Column
On Hold Column
Place the cursor next to the location line with onhold product that needs to be adjusted.

HOAD screen showing Hold Block
9 If you did not use the Delete function, press Enter to complete the line.
10 Click on Process Hold.
11 The Remarks Block will appear. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
12 When you finish entering your remarks, click on Return to exit.
13 A message will display on the screen showing the number of the hold adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
14 The cursor will return to the Customer Code field for the next transaction. If more product needs to be put on hold, begin the next transaction. Otherwise, click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN, key in the entity and click on History Block. It will show as HL (Hold) Type. You can also check who recorded the adjustment. The Document Number is the number of the Processing Adjustment record.

### LOOKING UP THE OFF HOLD DATE IN LOEN <a id="looking-up-the-off-hold-date-in-loen"></a>

You can look up the off hold date for auto take-off holds in the Location Block of LOEN.
1 Enter LOEN.
2 Retrieve the inventory whose off hold date you wish to look up.
3 Press F3 to enter the Location Block.
4 Press the tab key to display the Off Hold Date column.
Key in the negative value of the amount that you want to take off.

LOEN showing off hold date column

### REMOVING AUTO TAKE-OFF HOLDS IN HATO <a id="removing-auto-take-off-holds-in-hato"></a>

If a hold is defined as an auto take-off hold in HOLD (Hold Types), you must remove the hold by running 
HATO (Holds Auto Take-Off). When you run HATO, any auto holds applied to inventory are removed according to the auto-hold rules defined in HOLD.
The Holds Auto Take-Off Audit Trail shows the customer, up to three inventory levels, the product’s current location, the auto-hold code and the quantity that was removed from hold. HATO can only be run once for inventory on hold; if you attempt to rerun HATO a second time for the same hold inventory, the message “Report has no data” will print.
If you defined a specific number of days in HOLD:
if the number of days plus 1 has passed, the hold will be removed 
If you defined a specific date in HOLD: the hold will be removed if this date has passed

1 Enter HATO.

Holds Auto Take-Off prompt
2 Click OK to proceed.
3 Key in your printer code or select it from the dropdown list. Then click Ok to print.

### ADJUSTING ONLY THE HOLD CODE IN HOAD <a id="adjusting-only-the-hold-code-in-hoad"></a>

If you only need to change the type of hold code in a Hold Block location line but the amount remains the same, you must perform two transactions in HOAD.
1 Enter HOAD.
2 Remove the inventory from hold. 
3 Exit HOAD and then re-enter the program.
4 Place the same product on the new hold code in the normal manner. 

### PUTTING INVENTORY ON A MASSIVE HOLD IN POHO <a id="putting-inventory-on-a-massive-hold-in-poho"></a>

You use the program Put on Hold (POHO) to place one hold code type on all inventory that you specify. In 
POHO, first you select the customer, item or entity on which you need to place a hold. Then you choose the specific hold code. The system will place this hold on the entire selected inventory in all locations within your company. 
NOTE POHO applies a hold only on inventory that is currently free of any hold code. If you have 10 cases on DMG hold and 20 cases of the same product on no hold, the hold that you specify in POHO will apply only to the 20 cases that are not on hold.
ABC Warehousing Inc. Adjustment Number: 204 Page 1 of 1
Holds Auto Take-Off Audit Trail 03.09.07 10:50
------------------------------------------------------------------------------------------------------------------------------------
Customer Level 1 Level 2 Level 3 Location Whse Hold Adjust
---------- -------------------- -------------------- -------------------- ------------ ---- ---- --------------------
A A2 102 * A101 1 24HR -15CASE
D D1 101 GN000344 D100 1 24HR -60CASE

If you wish to place a hold on inventory that is stored in specific location(s), use HOAD. To place a hold on a specific pallet(s), case(s) or other SKU(s), you would also use HOAD.
POHO does not display the amounts and locations for the inventory entity or customer that you are querying on. To find out this information, you must look them up in LOEN.
PUTTING A HOLD ON ONE RETRIEVED RECORD (PROCESS ONE)
This procedure will place one specified hold code type on one record that is retrieved by the system for a selected customer, item or inventory entity.
1 Enter POHO.
2 Key in your inventory selection criteria. 
To retrieve all of a customer’s inventory records, key in the customer code and click on Execute Query. 
To retrieve all of an item’s inventory records, key in the customer code and press Enter. Then key in the item code and click on Execute Query. 
To retrieve all records for a specific entity key in the customer code, the item code and the applicable inventory levels of the entity. Press Enter after each entry. Then click on Execute Query. 
3 With the cursor anywhere in the Header Block screen, use the up and down arrow keys to scroll through the retrieved records. Stop when the record with the selection criteria that you need displays on the screen.

POHO screen
4 Click on Hold Block. 
5 The cursor moves to the Hold Block field. Key in the hold code that you wish to place on the selected inventory and press Enter. If you do not know the code, use the pick list. 
Querying on 
A retrieves four records.
Use the up and down arrow keys to scroll through the other records.

6 Click on Process One.

POHO screen
7 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
8 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
9 When you finish entering your remarks, click on Return to exit.
10 A message block appears with the number of the adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
11 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks and viewing the transaction details.
PUTTING A HOLD ON ALL RETRIEVED RECORDS (PROCESS ALL)
This procedure will place one specified hold code type on all records retrieved by the system for a selected customer, item or inventory entity.
1 Enter POHO.
2 If you want to place a hold code on all of a customer’s inventory, key in the Customer Code. click on Execute Query. 
If you want to place a hold code on a specific item or inventory entity, key in the customer code and the applicable inventory levels of the entity. click on Execute Query. 
Selected item.
Process One will apply the selected hold code to the displayed record (only record 1 and not records 2, 3 or 4 of the current record counter).

To view the retrieved records individually, use the up and down arrow keys while your cursor is in the 
Header Block.

POHO screen
3 Click on Hold Block. 
4 The cursor moves to the Hold Block field. Key in the hold code that you wish to place on all retrieved records for the selected inventory and press Enter. If you do not know the code, use the pick list. 
5 Click on Process All.
Querying on A retrieved four records.
Use the up and down arrow keys to scroll through the other records.

POHO screen
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks and viewing the transaction details.

### REMOVING INVENTORY FROM A MASSIVE HOLD IN MAHO <a id="removing-inventory-from-a-massive-hold-in-maho"></a>

You use the program Take Off Holds (MAHO) to remove one hold or all holds from large quantities of selected inventory — regardless of location. In MAHO, first you select the customer, item or entity from which you need to remove the hold(s). Then you choose:
 to remove one specific hold code from the selected inventory in your entire company or 
 to remove all hold codes from the selected inventory in your entire company
If you wish to remove a hold or holds from inventory stored in specific location(s), use HOAD. To remove a hold from a specific pallet(s), case(s) or other SKU(s), you would also use HOAD.
MAHO only displays the hold code types for the customer or entity that you are querying on. To find out the amounts and the locations of the entity with this specific hold code type, you must look them up in LOEN.
Selected item.
Process All will apply the selected hold code to all retrieved records (four in this example according to the current record counter).

REMOVING ONE HOLD CODE (PROCESS ONE)
This procedure will remove one hold code that is currently placed on the product of a selected customer, item or inventory entity.
1 Enter MAHO.
2 Choose from the following options:
3 With the cursor anywhere in the header block screen, use the up and down arrow keys to move from one hold code type to another for this customer or entity. Stop when the hold code that you need to remove displays on the screen.
4 Click on Remove Hold. 

MAHO screen
If you want to remove a specific hold code that is currently placed on all of a customer’s products:
If you want to remove a specific hold code that is currently placed on a specific item or inventory entity:
a) Key in the customer code. Then click on Execute Query. This retrieves all hold codes for the selected customer.
a) Key in the customer code and the applicable inventory levels of the entity. Then click on Execute 
Query. This retrieves all hold codes for the selected item or entity.
Selected item.
The hold code that applies to the 
Remove Hold 
Code Block.
Process One will removed the displayed hold code from the selected item (DMG in this example).

5 The cursor moves to the Remove Hold Block and the buttons Process One and Process All display on the screen. click on Process One.
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks and viewing the transaction details. You can also verify by re-entering MAHO, keying in the same selection criteria that you used for this procedure. Then click on Execute Query. The system does not have any hold codes to retrieve because they were removed by the procedure.
REMOVING ALL HOLD CODES (PROCESS ALL)
This procedure will remove all hold codes that are currently placed on the product of a selected customer, item or inventory entity.
1 Enter MAHO.
2 If you want to remove all hold codes that are currently placed on a customer’s products, key in the customer code and click on Execute Query. This retrieves all hold codes for the selected customer.
If you want to remove all hold codes that are currently placed on a specific item or inventory entity, key in the customer code and the applicable inventory levels of the entity. click on Execute Query. This retrieves all hold codes for the selected item or entity.
If you wish to view the retrieved records individually, use the up and down arrow keys while your cursor is in the Header Block.
3 Click on Remove Hold. 
4 The cursor moves to the Remove Hold Block and the buttons Process One and Process All display on the screen.

MAHO screen
5 Click on Process All.
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks and viewing the transaction details. You can also verify by re-entering MAHO, keying in the same selection criteria that you used for this procedure. Then click on Execute Query. The system does not have any hold codes to retrieve because they were removed by the procedure.

### PERFORMING A MASS TRANSFER OF PRODUCT ON HOLD IN MOHO <a id="performing-a-mass-transfer-of-product-on-hold-in-moho"></a>

You can perform a mass transfer of product on hold in MOHO (Move Hold to Hold). For example, you want to transfer a large number of inventory entities from a non-shippable hold called DMG for Damaged to a shippable hold called RET for Return to customer.
Using MOHO to perform a mass transfer is equivalent to removing a hold from the inventory in MAHO (Take 
Off Holds) and then applying a new hold to the inventory in POHO (Put On Hold).
Selected item.
Process All will remove all hold codes that are currently applied to the selected item (one in this example).

There are two transfer options in MOHO: one-to-one and many-to-one. With a one-to-one transfer, you apply a new hold code to the currently selected record in the header block. With a many-to-one transfer, you apply a new hold code to all records in the header block.
1 Enter MOHO.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels if applicable.
5 If required, key in your hold code.
6 Click on Execute Query.
MOHO screen showing four inventory records on hold
A1 Transport will retrieve all inventory that meet the search criteria that you specified. Inventory records not on hold will not be retrieved and cannot be processed in MOHO.
The Existing Hold Code field shows the hold code of the currently selected inventory record.
7 Click on Change Hold to position your cursor in the Hold Code field. The key in your to hold code and press Enter.

MOHO screen showing new hold code SUSP
8 Do one of the following:
9 When prompted to proceed with the update, click on Yes.
10 Key in any required remarks and click on Return.
11 Click on Return to Main.
12 Click on Exit.

### Adjusting Inventory Details <a id="adjusting-inventory-details"></a>

When items were first recorded in AccellosOne 3PL, the records included details about the item’s weight, inventory levels, expiry dates and other applicable features. AccellosOne 3PL uses these details for various calculations. If any of these details change, AccellosOne 3PL has programs to accommodate the changes. 
Three of the most commonly used programs are Change Entity Information (CHEI), Weight Adjustments (WEAD) and Recalculate Standard Weight (RESW). 
If you wish to apply the new hold code to the currently selected record (one-to-one transfer):
If you wish to apply the new hold code to all records retrieved in your query (many-to-one transfer):
a) Click on Process One. a) Click on Process All.

### ADJUSTING THE EXPIRY DATE IN CHEI <a id="adjusting-the-expiry-date-in-chei"></a>

You use the program Change Entity Information (CHEI) to change the expiry date of inventory products. It may be necessary to change an item or entity’s expiry date due to incorrect data entry on the original receiving records or because the shelf life date has to be back-dated. The following procedure only applies to inventory items or entities that have expiry dates.
Once this procedure is processed, the system will update all existing inventory records for this selected item. 
The system will replace the currently recorded expiry date with the new one.
1 Enter CHEI.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the applicable Inventory Levels.
5 Click on Execute Query.
6 If you have retrieved more than one record, use the up and down arrow keys to find the record with the product details that you need.
7 Click on Change Block.
8 In the Expiry Date field the system displays the selected item or entity’s current expiry date. Key in the new expiry date over the existing one and press Enter.

CHEI screen showing the Change Block
9 Click on Process Change. 
10 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
11 When you have finished entering all remarks, click on Return to exit. 
A message will display to indicate that the system is processing the change.
Selected item
Expiry Date field

12 If you wish to perform another adjustment, key in the next inventory selection criteria. Otherwise, click on 
Exit to exit.
ADJUSTING THE DESCRIPTIONS FOR INVENTORY LEVEL 2 AND HIGHER IN 
CHEI 
You use the program Change Entity Information (CHEI) to change the descriptions of products with Inventory 
Levels 2 and higher. For example, it may be necessary to change the inventory level descriptions due to incorrect data entry on the original receiving records. The following procedure only applies to inventory levels that have the Assign Description to New Entity flag set to Y in DILP.
Once this procedure is processed, the system will update all existing inventory records for this selected item. 
The system will replace the currently recorded descriptions with the corrected one. 
1 Enter CHEI.
2 Key in your customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the applicable inventory levels.
5 Click on Execute Query.
6 If you have retrieved more than one record, use the up and down arrow keys to find the record with the product details that you need.
7 Click on Change Block. The Change Block will display the applicable Inventory Levels for this inventory product.
8 Press Enter the required number of times until the cursor is in the Inventory Level Description field that you need to change. The system displays the current description for this level. Press F11 (Clear Field) 
and key in the new description. Then press Enter. 
9 Repeat for any of the other levels that you need to change.

CHEI screen showing the Change Block
Selected inventory entity.
Inventory Level 2 and higher field descriptions display here.

10 Click on Process Change. 
11 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can exceed 45 characters.
12 When you have finished entering all remarks, click on Return to Main to exit. 
A message will display to indicate that the system is processing the change.
13 If you wish to perform another adjustment, key in the next inventory selection criteria. Otherwise, click on 
Exit to exit.

### ADJUSTING WEIGHT DETAILS <a id="adjusting-weight-details"></a>

When you need to change the weight details of an item, there are two program options depending on whether the item is of standard or non-standard weight. The two programs are Weight Adjustments (WEAD) and 
Recalculate Standard Weight (RESW).
You use WEAD to adjust the weight of an inventory item or entity that is of non-standard weight. Nonstandard weight items do not have a constant weight. Weight changes in WEAD apply to the lowest inventory level; for example, if you track pallet ID’s, you must change the weight of each pallet ID individually.
You use the program RESW to adjust the weight or the cube of an inventory item or entity that is of standard weight. Standard weight items have a constant weight. Weight changes in RESW apply to all inventory belonging to an item regardless of the level 2, 3 or 4 values.
ENTERING WEIGHT ADJUSTMENTS FOR NON-STANDARD WEIGHTS IN WEAD
You use the program Weight Adjustments (WEAD) when the non-standard weight was entered incorrectly on the original receiving records. The system will then adjust the weight for this entity for all inventory currently in the warehouse. The weight change is effective immediately.
In WEAD you work with the total net and gross weights of the product at the product’s lowest inventory level. 
For example, if you track pallet ID’s for the product, you must change the weight of each pallet ID individually.
There are three weight adjustment options in WEAD:
 you can adjust the gross weight of each lot, pallet ID, roll, etc.
 you can adjust the net weight of each lot, pallet ID, roll, etc.
 you can adjust both
When you adjust the weight of an inventory entity, you have two options: you can enter the adjustment weight (that is, the current weight plus or minus the adjustment weight, which is the amount by which the total weight must be adjusted because of the change) or you can enter the new total weight.
EXAMPLE
You currently have 5 cases of item A, lot 7, in your warehouse and the weight of this lot is 10 lb. (2 lb. per case). If you wish to change the weight of each case to 3 lbs., you can enter an adjustment weight of 5 lb. (5 
X 1 = 5) or you can enter a new total weight of 15 (10 + 5 = 15).
CURRENT WEIGHT NEW WEIGHT
2 pounds per case 3 pounds per case

1 Enter LOEN and look up the total number of on-hand units of the inventory entity whose weight you wish to change. You will need this information to calculate the adjustment weight or the new total gross or net weight.
2 Enter WEAD.
3 Key in the customer code. If you do not know the code, use the pick list.
4 Key in your item code.
5 Key in the applicable inventory levels.
6 Click on Execute Query.
7 Click on Weight Block. The Weight Block displays the Gross Current Total Weight and the Net Current 
Total Weight. These are the weight details of this entity’s total inventory that is currently Available and On 
Hand. The Weight Measure Code field indicates the unit of measure being used.

WEAD screen showing the Weight Block
8 If the Adjustment Date field is activated on your system, you can key in a new date and press Enter. If the system date is correct, press Enter to accept it.
9 If the weight measure code you are using to record the change is the same as the one that displays in the 
Weight Measure Code field, press Enter. 
If the Weight Measure Code you are using to record the change is not the same as the one in the Weight 
Measure Code field, key in the code and press Enter. If you do not know the code, use the pick list.
Current Total Weight is 10 lbs.
(5 cases X 2 lbs.)
Adjustment Amount is 5 lbs.
(5 cases X 1 lbs.)
CURRENT WEIGHT NEW WEIGHT
Selected inventory entity
The gross and net weights for the total amount of this inventory entity that is currently stored in your company.
The Weight Measure Code field indicates the unit of measure for the weight.

WEAD screen showing the Weight Block
10 If required, make any necessary changes to the inventory’s gross weight. If no change is required to the inventory’s gross weight, press Enter twice to bypass the Gross Adjustment Weight and Gross New Total 
Weight fields.
If you wish to enter the gross adjustment weight:
If you wish to enter the new total gross weight:
a) Key in your gross adjustment weight and press Enter. You key in a negative amount if the new weight is less than the currently recorded weight; you key in a positive amount if the new weight is more than the currently recorded weight. 
b) Press Enter to bypass the Gross 
New Total Weight field.
a) Press Enter to bypass the Gross 
Adjustment Weight field.
b) Key in your new total gross weight and press Enter.
Selected entity
The amount that you enter in the Gross 
Adjustment Weight and Net Adjustment 
Weight fields can be a positive or negative value.

11 If required, make any necessary changes to the inventory’s net weight. If no change is required to the inventory’s net weight, leave the Net Adjustment Weight and Net New Total Weight fields blank.
12 Click on Process.
13 A Remarks Block will appear to enter any necessary remarks. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 
40 characters and no line can exceed 45 characters.
14 When you finish entering your remarks, click on Return.
15 Click on Exit to exit.
You can verify weight adjustments in the History Details Block of LOEN. A weight adjustment made in WEAD will show in the inventory transaction’s history as a 0 (zero) quantity adjustment. The weight adjustment will only show the weight difference not the new total weight.
If you wish to enter the net adjustment weight:
If you wish to enter the new total net weight:
a) Key in your net adjustment weight and press Enter. You key in a negative amount if the new weight is less than the currently recorded weight; you key in a positive amount if the new weight is more than the currently recorded weight. 
b) Press Enter to bypass the Net 
New Total Weight field.
a) Press Enter to bypass the Net 
Adjustment Weight field.
b) Key in your new total net weight and press Enter.

LOEN screen showing the weight adjustment from the above procedure
ENTERING WEIGHT ADJUSTMENTS FOR STANDARD WEIGHTS IN RESW
You use the program Recalculate Standard Weight (RESW) to adjust the standard weight or cube of an item. 
An item must be set up as a standard weight item in order to use RESW. If the item is not a standard weight item, you must adjust its weight in Weight Adjustments (WEAD).
A standard weight may need to be changed because the item’s weight details were keyed in incorrectly in the original ITEM record or because the manufacturer changes the size of the standard container. For example, a case of paint is currently recorded in the system as having a standard gross weight of 15 lbs. The system uses this data in all applicable calculations. However, the manufacturer has now changed the size of the paint container and a case of paint now weighs only 14 lbs. 
First, you record the change in the Item Quantity Breakdown Block of the program ITEM. Then you run 
RESW to update the weight or cube data on existing inventory records. The system will apply the change effective from the date that you enter as the Adjustment Date. 
There are two adjustment options in RESW:
 post adjustment
 reprocess history
The post adjustment option will create a separate line for the adjustment. For example, if the original standard weight of the item was 2 lbs. per case and you adjust it to 3 lbs. per case, the adjustment for 5 cases of available inventory would appear as follows:
A 0 cases 5 lbs. (difference between old weight of 10 lbs. and new weight of 
15 lbs.)
A weight adjustment shows as a 
0 quantity adjustment.
Only the weight adjustment displays — not the new total weight.

If you select the reprocess option, the original lines in the History Block of LOEN will be adjusted to the new weight and there will be no separate adjustment line showing the difference between the original weight and the new standard weight.
1 Enter ITEM.
2 Click on Enter Criteria.
3 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
4 Click on Execute Query.
5 Click on Quantity Breakdown Block.
6 If necessary, use the up and down arrow keys to move to the SKU record with the weight and cube details. Press Enter until the cursor is in the cube or weight field that you need to change. Key in your new value and press Enter. 

ITEM screen showing the Item Quantity Breakdown Block
7 When you have finished changing all of the applicable fields, click on Master Block and Exit.
CO -5 cases -10 lbs. (you confirm the order of 5 cases)
CR 10 cases 20 lbs. (you confirm the receipt of 10 cases)
CO -5 cases -15 lbs. (you confirm the order of 5 cases)
CR 10 cases 30 lbs. (you confirm the receipt of 10 cases)
Cube fields of the selected item or entity.
Gross and Net 
Weight fields of the selected item or entity.

8 Enter RESW.
9 Key in your customer code and press Enter. If you do not know the code, use the pick list.
10 Key in A (Post Adjustment) or R (Re-Process History) and press Enter. A will create a separate line in the History Block of LOEN so that you can see both the original record and the adjustment record. R will adjust all history records in the History Block of LOEN to show the new weight.
11 If the Adjustment Date field is activated, key in the date when the weight change became effective and press Enter. If the date when the weight change began is the same as the default date, press Enter to accept the default date.
12 Key in the item code of the item whose weight or cube is being changed and press Enter. If you do not know the code, use the pick list.

RESW screen
13 Click on Process. A message will display to inform you that the system is processing the adjustment.
14 Click on Exit to exit.
You can verify that the RESW transaction was successful by looking up this transaction in the History Block of 
LOEN.
Adjusting the Weight of Open Orders and Receipts
RESW will not adjust the weight of product on open orders and receipts. Refer to the following table for specific instructions:
open receipts Delete the receipt lines and then re-add them. When you create a new receipt line, AccellosOne 3PL will retrieve the new weights defined in ITEM.
Post Adjustment or Reprocess field.
Adjustment 
Date field.
Process button

### CLEARING WEIGHTS IN CLWE <a id="clearing-weights-in-clwe"></a>

This program allows you to clear the weights — that is, set to zero — of all items with a positive or negative weight but a quantity of zero. If you do not clear your weights, you may generate invoices and reports for product that is no longer in your warehouse.
CLWE will clear all weights for the customer or customers that you specify and post a weight adjustment to the item. The effective date of the weight adjustment will be either the last transaction date for the item or lot or the adjustment date that you enter in CLWE.
When you run CLWE, the first renewal billing after you clear your weights may be slower than usual. 
However, all subsequent renewal billings will be normal.
1 Enter CLWE.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter.

Clear Weights (CLWE) screen pending order line AccellosOne 3PL will retrieve the new weights defined in ITEM during allocation.
regular order line with or without location enteredChange the to ship quantity of each order line to zero. Then reenter the correct to ship quantity. AccellosOne 3PL will retrieve the new weights defined in ITEM.
CAUTION Do not run CLWE while performing inventory activity for that customer. 
Inventory activity includes any transaction that affects inventory such as entering a receipt or order, confirming a receipt or order, making an adjustment or relocating product. If you run CLWE while performing any of these activities, your inventory could be out of balance.

4 In the Adjustment Date/Last Transaction Date field, key in A for Adjustment Date or L for Last Transaction Date and press Enter.
5 If you selected Adjustment Date in the previous field and if the Adjustment Date field is activated, you can press Enter to accept the current system date as your adjustment date or you can key in a new adjustment date and press Enter.
6 Click on Update Inventory. If the customer that you selected has non-zero weights for inventory whose quantity is zero, the message “Clearing out weights” will be displayed.

### Reversing a Document’s Flow in RVDF <a id="reversing-a-document-s-flow-in-rvdf"></a>

You can reverse an order or receipt’s flow for all new lines in the program RVDF (Reverse Document Flow). 
For example, you wish to add a new order line after picking or loading a given order. By reversing the order header to STPI (Start Picking) from FIPI (Finish Picking), you can allocate and pick the new order line. 
Existing order lines, however, will remain at the FIPI flow.
You can reverse a document’s flow to any flow that precedes the document’s current flow. However, you cannot reverse a flow back to ENRE (Enter Receipt) or ENOR (Enter Order).
The following restrictions apply if the order has been assigned to a load:
 you cannot reverse an order flow if the load is confirmed
 you cannot reverse an order flow if the order has been loaded in OLOP and is NOT the last stop (for example, if order 10 is assigned to stop 4 and order 11 is assigned to stop 3, you can reverse the order flow of order 11 because it is the last stop loaded but not order 10) 
 you cannot reverse the order flow if the load is locked
1 Enter RVDF.
2 Do one of the following:
If you wish to reverse the flow of an order:
If you wish to reverse the flow of a receipt:
a) Key in your order number and press Enter.
a) Key in your receipt number and press Enter.

RVDF screen showing order header at the flow STLO (Start Loading)
3 In the Reset Flow Process Code field, select from the dropdown list the previous flow code that you wish to assign to all new receipt or order lines. If the dropdown list is deactivated, this means that the document is already at the flow immediately following ENRE (Enter Receipt) or ENOR (Enter Order) and cannot be reversed.
4 Click on Accept to save your changes.
5 Click on Exit to exit.

## Bond System <a id="bond-system"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

The Bond System allows you to track and report on bonded product according to customs regulations. AccellosOne 3PL supports two types of bond operations: you can receive bonded product and remove the bond while the product is in the warehouse or you can receive bonded product and ship it out to another bonded facility without removing the bond. 
There are five steps to follow in processing a bond:
BOND
ENRE
CHRF
ENOR you ship the product in bond No Yes
You enter your receipt in 
ENRE.
You create your bond numbers in BOND (Bond 
Setup).
Bond status = NEW 
You assign bond numbers to individual receipt lines when you reach the appropriate flow in CHRF.
Bond status = OPEN 
If you wish to ship the product in bond to another bonded facility, you ship it in ENOR. If you wish to release the bond while product is still in the warehouse, you release it in 
BORL (Bond Release 
Adjustment).
Bond status = RELEASED 
You close the bond in BOND (Bond Setup).
Bond status = CLOSED
BOND
BORL

OPERATIONS 2 GUIDE 4.2* 95

### Setting up the Bond System <a id="setting-up-the-bond-system"></a>

There are three setup programs for the bond system:
 HOLD (Hold Types)
 CUBR (Custom Broker Code)
 DIFP (Depositor Workflow Profile)

### SETTING UP BOND HOLDS IN HOLD <a id="setting-up-bond-holds-in-hold"></a>

In HOLD you create a bond hold type by clicking on the Bond checkbox. If you ship product in bond, you must click on the Ship checkbox; if you receive bonded product but do not ship product in bond, you must leave the 
Ship checkbox unchecked.
1 Enter HOLD.
2 Click on Enter Criteria then Execute Query to display the hold types currently on your system.
3 Click on New .
4 Key in your hold type code and press Enter.
5 Key in your hold type code description and press Enter.
6 If required, click on the Ship, Renw and other checkboxes to select the appropriate hold option.
7 Click on the Bond checkbox to set your new hold type to a bond type hold.
8 Click on Save to save your changes.
HOLD screen showing BON1 as a bond type hold
9 Click on Exit to exit HOLD.

### SETTING UP CUSTOMS BROKERS IN CUBR <a id="setting-up-customs-brokers-in-cubr"></a>

In CUBR you set up your customs brokers. 

1 Enter CUBR.
CUBR screen
2 Key in your broker code and press Enter.
3 Key in the broker’s name and press Enter.
4 Key in the required number of address lines for this broker.
5 Key in your ZIP/postal code and press Enter. If the code is already on the system, the city, state or province and country will be filled in automatically. 
If the code that you enter is new and not yet on the system, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. 
If this occurs, click on Create Code. First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into CUST with the appropriate information filled in.
6 If the Telephone Block appears, click on Create Record and key in any required information for the customs broker. When you finish entering your information, click on Return to Main and Master Block to exit. 
If you do not wish to add telephone information to a customs broker, click on Master Block to exit the 
Telephone Block.
CUBR screen

OPERATIONS 2 GUIDE 4.2* 97
7 Click on Exit to exit CUBR.
ADDING THE SPECIAL VERIFY PROGRAM BOND TO YOUR WORKFLOW 
PROFILE IN DIFP
In DIFP you attach the special verification program BOND to the appropriate depositor workflow profile. 
BOND is normally attached to the CORE (Confirm Receipt) flow. You can attach BOND to earlier flows in a workflow profile as long as the receipt line has been assigned a location at that flow. BOND should never be attached to the ENRE (Enter Receipt) flow.
If only certain customers in your warehouse receive bonded product, you must set up multiple DIFP profiles: 
one profile for bonded product and another profile without the special verification program for non-bonded product.
1 Enter DIFP.
2 Key in your flow profile code and press Enter.
3 Click on In/Out/Repi/Relo Block. The first record in this block will be your Inbound record.
4 Click on Flow Block.
5 In the Flow Block, use your arrow keys to cursor down to the appropriate inbound flow.
6 Click on Document Block.
7 In the Document Block, click on Special Verify Block.
8 In the Special Verification Block, key in 10 as your sequence number and press Enter.
9 Key in BOND (Bond Entry) and press Enter.
10 Press Enter to accept the default values in the Complete, Sequence and Display fields.
11 Click on Return to Main to exit Create mode.
DIFP screen showing BOND special verify attached to the CORE (Confirm Receipt) flow

12 Setup is now complete. Click on Document Block, Flow Block, In/Out/Repi/Relo Block, Master Block and 
Exit to exit.

### Placing Product on Bond Hold <a id="placing-product-on-bond-hold"></a>

There are three steps to follow in placing product on bond:
 you create the bond in BOND (Bond Setup)
 you enter your receipt in ENRE (Enter Receipts)
 you assign your bond numbers to individual receipt lines in CHRF (Time-Stamp and Confirm Receipt)

### CREATING YOUR BOND NUMBERS IN BOND (OPTIONAL) <a id="creating-your-bond-numbers-in-bond-optional"></a>

You can create your bond numbers in BOND before entering your receipt or you can create your bond numbers in CHRF when you time-stamp and confirm the receipt.
1 Enter BOND.
BOND screen
2 Click on Create Record.
3 In the Bond Number field, key in your bond number and press Enter. The first three characters of the bond number are the broker code that you created in CUBR.
4 In the Type field, key in a description for your bond number and press Enter. If you do not require a description, press Enter with the field blank to bypass this option.
5 Press Enter to bypass the External Bond Number field.
6 In the Arrival Date field, key in your arrival date for the bond and press Enter. If the arrival date is the current date, press Enter to accept the system date.

OPERATIONS 2 GUIDE 4.2* 99
7 In the Entry Date field, key in your entry date for the bond and press Enter. If the entry date is the current date, press Enter to accept the system date.
8 In the Hold Code field, key in the hold code for this bond and press Enter. Only hold codes whose Bond checkbox has been selected in HOLD can be entered in this field.
BOND screen showing newly created bond number
9 Repeat the above steps for each additional bond that you wish to add.
10 When you finish adding your bonds, click on Exit to exit.

### ASSIGNING THE SAME BOND NUMBER TO MULTIPLE RECEIPTS <a id="assigning-the-same-bond-number-to-multiple-receipts"></a>

You can attach the same bond number to multiple receipts by means of the External Bond Number field. In this field, you enter your actual bond number. In the Bond Number field, on the other hand, you enter the bond number plus a unique suffix such as “-1”, “-2”, “-3”, etc. 
EXAMPLE
To attach the same bond number to three receipts, you would create three unique records in BOND.
First receipt
Bond Number = BR1001001-1
External Bond Number = BR1001001
Second receipt
Bond Number = BR1001001-2
External Bond Number = BR1001001
Third receipt
Bond Number = BR1001001-3
External Bond Number = BR1001001

BOND screen showing bond number BR1001001-1 attached to external bond number BR1001001

### ENTERING YOUR RECEIPT IN ENRE <a id="entering-your-receipt-in-enre"></a>

You enter your receipt normally in ENRE. 

### ASSIGNING BOND NUMBERS TO RECEIPT LINES IN CHRF <a id="assigning-bond-numbers-to-receipt-lines-in-chrf"></a>

In CHRF you assign your bond numbers to individual receipt lines; all lines can have same bond number or each line can be assigned a different number. Bond numbers are optional in CHRF; this means that you can receive both bonded and unbonded product on the same receipt.
1 Enter CHRF.
2 Key in your receipt number and press Enter.

OPERATIONS 2 GUIDE 4.2* 101
CHRF screen showing CORE as your next flow
3 Click on Select Flow to advance the receipt’s flow in the normal manner. 
When you reach your bond entry flow, the following screen will display.
CHRF screen showing prompt for bond number

4 Do one of the following:
AccellosOne 3PL will display the Receipt Detail Block. 
If you have already created your bond number(s) in BOND:
If you have NOT already created your bond number(s) in BOND:
a) Key in your bond number for the receipt and press Enter or use your pick list to select it.
a) Key in your new bond number and press Enter.
b) Click on Create Code.
c) In the Type field, key in a description for your bond number and press Enter or press Enter with the field blank to bypass the option.
d) If required, key in your external bond number and press Enter.
e) Key in your arrival date and press Enter.
f) Key in your entry date and press 
Enter.
g) Press Enter to bypass the Closing Date field.
h) Key in your hold code for the bond and press Enter.
i) Press Enter to position your cursor in the Receipt Detail Block.

OPERATIONS 2 GUIDE 4.2* 103
CHRF screen showing each detail line on the receipt
5 Do one of the following:
6 If required, key in a description for the receipt line and press Enter. If you do not require a description, press Enter to bypass this field.
7 Repeat the above steps for each additional receipt line.
8 When you finish assigning your bond numbers to the receipt line(s), click on Exit to return the Header 
Block of CHRF.
9 Proceed to confirm your receipt in the normal manner.
If you wish to assign the bond number in the Header Block to the receipt line:
If you wish to assign a bond number other than the number in the Header Block to the receipt line:
If you do NOT wish to place the receipt line on bond hold:
a) Click on Copy Bond Number. a) Use the pick list function to assign a bond number to the receipt line.
a) Delete the bond number by pressing the Delete key on your keyboard.

### Releasing a Bond Hold in BORL <a id="releasing-a-bond-hold-in-borl"></a>

You release a bond hold in BORL (Bond Release Adjustment). Once you release the bond hold, the product becomes regular inventory and can be adjusted and shipped like any other inventory in your warehouse.
1 Enter BORL.
2 Key in your bond number and click on Execute Query. If you do not know the bond number, you can press Enter to bypass the Bond Number field and query by customer code and inventory levels.
3 Click on Hold Block.
BORL screening showing two pallets of item A1, lot 102 on bond hold BON1
4 Press Enter twice to position your cursor in the Adjust field.

OPERATIONS 2 GUIDE 4.2* 105
5 Do one of the following:
6 Click on Process Hold.
BORL screen showing prompt for duty numbers
7 If required, key in your duty number and press Enter. If you do not wish to enter a duty number, press 
Enter to bypass this field.
8 Key in your release date and press Enter or press Enter to accept the current system date as your release date.
9 When the Remark Block appears, do one of the following:
If you wish to release all product identified in the Header Block of 
BORL:
If you wish to release a portion of the product identified in the 
Header Block of BORL:
a) Click on Delete. a) Key in the quantity that you are releasing from hold plus the SKU code that this quantity is expressed in and press Enter.
a) The quantity that you enter in this field must be a negative number; 
for example, if you are releasing 
20 cases, you would key in 
-20C.
If you wish to attach a remark to the adjustment:
If you do NOT wish to attach a remark to the adjustment:
a) Key in your remarks.
b) When you finish entering your remarks, click on Return to exit the Remark Block.
a) Click on Return to exit. 

10 Click on Exit to exit BORL.

### USING THE RELEASE ALL COMMAND <a id="using-the-release-all-command"></a>

The Release All command in BORL allows you to release all inventory assigned to a given bond number in a single step. Release All is only available when you are releasing all product on bond; you cannot release a portion of the product on bond.
1 Enter BORL.
2 Key in your bond number and click on Execute Query.
3 Click on Release All.
BORL screen showing release all confirmation message
4 When prompted to release all inventory, click on Yes.
5 If required, key in your duty number and press Enter. If you do not wish to enter a duty number, press 
Enter to bypass this field.
6 Key in your release date and press Enter or press Enter to accept the current system date as your release date.
7 When the Remark Block appears, do one of the following:
8 Click on Exit to exit BORL.

### Closing a Bond in BOND <a id="closing-a-bond-in-bond"></a>

You close a bond in BOND by entering a closing date in the Closing Date field. All product attached to the bond must be released before you can close it.
If you wish to attach a remark to the adjustment:
If you do NOT wish to attach a remark to the adjustment:
a) Key in your remarks.
b) When you finish entering your remarks, click on Return to exit the Remark Block.
a) Click on Return to exit. 

OPERATIONS 2 GUIDE 4.2* 107
1 Enter BOND.
2 Click on Enter Criteria.
3 Key in your bond number and click on Execute Query.
4 Press Enter until your cursor is positioned in the Closing Date field.
BOND screen showing cursor in Closing Date field
5 Key in your closing date and press Enter.
6 Press Enter to accept the value in the Hold Code field.
7 Click on Exit to exit.

### Shipping Product in Bond in ENOR <a id="shipping-product-in-bond-in-enor"></a>

You can ship product on bond hold to another bonded facility by entering the appropriate bond hold code and bond number in the Line Block of ENOR. Two conditions must be met before you can ship product on bond hold: 
 the order line must be a regular — not pending — line
 the bond hold code must be shippable (you define whether a bond hold code is shippable in the program 
HOLD)
1 Enter ENOR.
2 Enter the header information for the order in the normal manner.

3 In the Line Block, enter all the product’s inventory levels.
4 Press F9 (Previous Field) until your cursor is positioned in the Hold Code field.
ENOR screen showing cursor positioned in Hold Code field
5 Key in your bond hold code and press Enter.
6 Key in your bond number and press Enter.
7 Press Enter to position your cursor in the Ordered Quantity field and key in your order quantity.
8 Continue to enter your order line.
9 Confirm the order in CHOF or COOL in the normal manner.

### Looking Up Bond Information in LOBO <a id="looking-up-bond-information-in-lobo"></a>

You look up bond information in LOBO (Look Up Bonds). LOBO shows complete bond information (the bond number, customer and key dates for the bonded product such as the arrival date, received date, release date and closing date) as well as item information, history information and location information. 
LOBO also shows the following system-calculated dates:
 Due Date
 Variance Due Date
 Expiry Date

OPERATIONS 2 GUIDE 4.2* 109
There are four status’s for a bond in LOBO:
1 Enter LOBO.
2 If you wish to query by bond number, key in your bond number. If you wish to query by bond status, customer code, arrival date, etc., press Enter until your cursor is positioned in the appropriate field and key in the value that you are looking for.
3 Click on Execute Query.
new you have created the bond in BOND but no product has been assigned to it open you have assigned product to the bond that you created in BOND released you have released all product on the bond in BORL or you have shipped the product in bond in ENOR closed after releasing the bond in BORL or shipping the product in bond in 
ENOR, you have closed it in BOND
FIELD DESCRIPTIONS
Bond Number The bond number that you created in BOND.
Customer Code The customer whose product is on bond hold.
Bond Status See above
Arrival Date The arrival date that you entered in BOND.
Entry Date The entry date that you entered in BOND.
Received Date The date that the receipt was confirmed in CHRF.
Variance Due Date The received date plus two working days.
Due Date The final release date plus ten days.
Closing Date The closing date that you entered in BOND.
Final Release Date The date that you released the last product on the bond in BORL or you shipped the product in bond in ENOR.
Expiry Date The received date plus two years.

LOBO screen showing bond with open status
4 Click on Summary Block. The Summary Block shows the items attached to the bond number in the 
Header Block.
LOBO screen showing Summary Block
5 Position your cursor over the line that you wish to query on and click on History Block.

OPERATIONS 2 GUIDE 4.2* 111
LOBO screen showing History Block
6 Click on Location Block to enter the Location Block. The Location Block shows all locations for the bond number in the Header Block.
LOBO screen showing Location Block
7 When you finish looking up your bond information, click on Return to Main and Exit to exit.

### Bond Reports <a id="bond-reports"></a>

See the Standard Reports Guide.

OPERATIONS 2 GUIDE 4.2* 113

## Inventory Attributes <a id="inventory-attributes"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

Inventory attributes represents additional information that you wish to capture about an inventory entity such as the pallet type, country of origin, etc. Unlike item process values set up in IPRO/IPRP, inventory attributes can be attached to any inventory level from the item level on down to the pallet ID level. You can set up as many inventory attributes as you need for your facility and can define them as either mandatory or optional. 

### Setting Up Inventory Attributes <a id="setting-up-inventory-attributes"></a>

You set up your inventory attribute rules in IAPR (Inventory Attributes Profile Code). In the Header Block, you set up your inventory attribute profile code as well as a description. In the Detail Block, you set up one or more inventory attributes that you wish to capture for this profile code. Your then attach your IAPR profile code to the appropriate item(s) in ITEM.
When you receive that item in either ENRE or RFCH or create new inventory for that item in either ENAJ or 
RFAJ, you enter your inventory attributes. 
In the Attribute Name Block, you set up one or more inventory attributes that you wish to capture for this profile code. 
FIELD DESCRIPTIONS (HEADER BLOCK)
Inventory Attribute Profile CodeMandatory
Your inventory attribute profile code.
Description Mandatory
Your inventory attribute description.
FIELD DESCRIPTIONS (ATTRIBUTE NAME BLOCK)
Attribute Name Mandatory
The name of the attribute that you wish to capture.

OPERATIONS 2 GUIDE 4.2* 215
Description Mandatory
A description for the attribute that you wish to capture.
Required Whether or not the inventory attribute is mandatory. if you define an attribute as mandatory, a receipt line cannot be confirmed if a required attribute is missing.
Attached to Inventory 
Level
The inventory level that the inventory attribute is attached to.
Allow RF Merge If you select this option, you can merge the item in RFMI even if the attributes do not match.
If you do not select this option, you can only merge the item in RFMI if there is an exact match of attributes at the inventory level that you specify in the 
Attach to Inventory Level field.
Allow Allocation If you select Allow Allocation, you can specify inventory attribute names as well as restrictions in the Inventory Attributes Restriction Block of ENOR. If you do specify attribute names and/or restrictions, only product that satisfies these restrictions will be allocated to the order.
Allocation Sequence If allocation is activated, you can specify an allocation sequence for different inventory attributes. For example, if you set country code to 5 and establishment number to 10, allocation will attempt to allocate product assigned a country code before allocating product with an establishment number.
Attribute Entry Type Alphanumeric
Date
Integer
Money
Number
The type of attribute being entered.
Date Format The date format for date-type attributes.
Maximum Length Optional
The maximum length of the attribute.
Exclude From RF CheckInIf you select this option, attribute values cannot be entered in RFCH.
FIELD DESCRIPTIONS (ATTRIBUTE NAME BLOCK)

In the Attribute Values Block, you set up your attribute values for the attribute in the Attribute Block.
1 Enter IAPR.
2 Click on New .
3 Key in your inventory attribute profile code and press Enter.
4 Key in a description for your new inventory attribute profile code and click on Save 
5 Click in the Attribute Name field and click on New .
6 Key in your attribute name.
7 Key in a description for your attribute name and press Enter.
8 If the attribute is mandatory, click in the Required field.
9 Key in your inventory level for the attribute and press Enter.
10 If required, click on the Allow RF Merge and Allow Allocation checkboxes.
11 If required, key in an allocation sequence number and press Enter.
12 In the Attribute Entry Type field, select the appropriate value from the dropdown list: Alphanumeric, Date, 
Integer, Money or Number.
13 If required, key in date format and/or a maximum length.
14 When you finish setting up your attribute profile code, click on Save .
Override Attribute Value on Confirmation
If you select this option, you can override your attribute value at receipt/order 
FIELD DESCRIPTIONS (ATTRIBUTE VALUES BLOCK)
Sequence Mandatory
A sequence number for the attribute value.
Value Mandatory
The attribute value.
FIELD DESCRIPTIONS (ATTRIBUTE NAME BLOCK)

OPERATIONS 2 GUIDE 4.2* 217

IAPR screen 
15 Click anywhere in the Details Block, then click on Details .
16 Key in a sequence number for your first attribute value and press Enter.
17 Key in your first attribute value and press Enter.
18 Click on New and repeat the above two steps for your second and subsequent attribute values.
IAPR screen showing three countries attached to COO

19 When you finish entering your attribute values, click on Save . 
20 Click on Return then click on Exit to exit.

### ATTACHING YOUR INVENTORY ATTRIBUTE CODE TO YOUR ITEM(S) <a id="attaching-your-inventory-attribute-code-to-your-item-s"></a>

1 Enter ITEM.
2 Retrieve the item that you are going to attach the inventory attribute profile code to.
3 In the Inventory Attribute Profile Code field, key in the inventory attribute profile code that you created in 
IAPR and press Enter.

ITEM screen showing COO code attached to item A1
4 Click on Return to Main and Exit to exit ITEM.

### DEACTIVATING INVENTORY ATTRIBUTE CAPTURE BY SHIPPER <a id="deactivating-inventory-attribute-capture-by-shipper"></a>

If required, you can suppress inventory attribute capture for individual shippers by setting the Suppress 
Inventory Attributes flag in SHIP to Y for Yes.

OPERATIONS 2 GUIDE 4.2* 219
SHIP screen showing Suppress Inventory Attributes flag set to Yes

### Entering Inventory Attributes in ENRE <a id="entering-inventory-attributes-in-enre"></a>

If the Exclude from RF Check-In flag in IAPR is not selected, you can also enter inventory attributes in RFCH.
1 Enter ENRE.
2 Enter your header information in the normal manner.
3 In the Line Block, enter your inventory levels.
4 Enter your expected and received quantities.
5 Click on Inventory Attributes Screen.

ENRE screen showing prompt for COO (country of origin) attribute value
6 Key in your value and press Enter or select it from the pick list.
7 When you finish entering your attribute(s), click on Exit to exit the Inventory Attributes Block.
8 Continue to enter your receipt line in the normal manner.

### Looking Up Your Inventory Attributes in LOEN <a id="looking-up-your-inventory-attributes-in-loen"></a>

You look up an item’s inventory attributes in LOEN by clicking on the Look Up Inventory Attributes icon.
1 Enter LOEN.
2 Key in your customer code and press Enter.
3 Key in the required number of inventory levels and press F2 (Execute Query).
4 Click on Inventory Attributes Block.

OPERATIONS 2 GUIDE 4.2* 221

LOEN screen showing Look Up Inventory Attributes Block
5 When you finish looking up your inventory attributes, click on Exit to exit the Inventory Attributes 
Block.
6 Click on Inventory and Exit to exit LOEN.

### Changing Your Inventory Attributes in CHIA <a id="changing-your-inventory-attributes-in-chia"></a>

If the wrong attribute was attach to an inventory entity in either ENRE or RFCH, you can correct the error in 
CHIA (Change Inventory Attributes).
1 Enter CHIA.
2 Key in your customer code and press Enter.
3 Key in the required number of inventory levels and press F2 (Execute Query).
4 Click on Attribute Block.
5 Key in your new attribute value and press Enter or use the pick list to select it and press Enter.

CHIA screen showing new and existing attribute values
6 Click on Process Change.
7 If required, key in your remarks for the transaction.
8 Click on Exit to exit.

### Allocation by Inventory Attribute <a id="allocation-by-inventory-attribute"></a>

If allocation is activated for an inventory attribute, you can allocate by that attribute in the Inventory Attributes 
Restricction Block of ENOR.
1 Enter ENOR.
2 Retrieve the order that you wish to allocate.
3 Select the order line that you wish to allocate. Make sure that the order line type is set to P.
4 Click on Inventory Attributes Restriction .

OPERATIONS 2 GUIDE 4.2* 223
ENOR screen showing Inventory Attributes Restriction Block
5 Key in your attribute name and press Enter or select it from the pick list.
6 If required, key in your allocation sort sequence number and press Enter.
7 Enter your attribute restrictions using the standard set of AccellosOne 3PL operands: =, (=), >, >=, <, <=, 
-.
8 When you finish entering your restrictions, click on Save to save your changes.
9 Click on Exit .

OPERATIONS 2 GUIDE 4.2* 225

## Item Process Values <a id="item-process-values"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

Item process values allow you to create predefined messages and capture operator-entered values that can be attached to a particular item during order or receipt entry. You can choose to print these messages and values on the inbound or outbound document that you specify or you can store them on the system only. 
You use item process values when you wish to:
 capture item-specific information such as serial numbers, temperatures, catch weights or purchase order numbers for the purpose of printing them on an inbound or outbound document such as a bill of lading, label or other document 
 attach a standard predefined message to a document with no value to be captured (for example, “REPACK ITEM TO COMPANY X’S SPECS”)1
If you are capturing a value, you can specify whether you wish to store the value in inventory; if you store the value in inventory, you can look it up in LOIP (Look Up Item Process). If you do not store the value in inventory, it will be automatically deleted when you confirm the order or receipt or when you purge the order or receipt in PURG. 

### PROCESS VALUES VS. INVENTORY LEVELS <a id="process-values-vs-inventory-levels"></a>

You use item process values when you wish to attach a message or operator-entered value to a particular item or to a small group of items during order or receipt entry. If you wished to attach a message to all items belonging to a customer, you would use the programs MESS, DEME and DPME. 
If you wished to record and track serial numbers for all of a customer’s items, you would set up an inventory level in DILP. If you used item process values to record serial numbers instead of an inventory level, you could not assign a location to a particular serial number and no billing or allocation by serial number would be possible.

### Setting Up Your Item Process Code in IPRO <a id="setting-up-your-item-process-code-in-ipro"></a>

In this program, you set up your item process codes. Item process codes are attached to your item process profile (IPRP).
1. only available for documents that support item process values.
FIELD DESCRIPTIONS
Process Code Mandatory
Your item process code; for example, CW for Catch Weight.

OPERATIONS 2 GUIDE 4.2* 385
Description Mandatory
Your process code description
Type of Value CUBE = Cube
HGT = Height
LEN = Length
LEV2 = Inventory Level 2
OTHR = Other
SER = Serial Number in Weight Bar Code
SN = Serial Number
TARE = Tare Weight
TEMP = Temperature
WGTG = Gross Weight
WGTN = Net Weight
WID = Width
The type of value that you are capturing. If you are capturing a value during receipt or order entry, you can use any of the above types. If you are setting up a standard predefined message, use OTHR as your type of value.
Entry Value Y = Yes
N = No
If you set Entry to Yes, you can go to the Process Block and enter a value during order or receipt entry. If you set Entry to No, the predefined text will print on the document that you specify in the Detail Block and you can, if required, record the value manually on this document.
Inbound / Outbound / 
Both
Only available if you are capturing a value
I = Inbound
O = Outbound
B = Both
If you specify I for Inbound, you are capturing a value during an inbound process. If you specify O for Outbound, you are capturing a value during an outbound process. If you specify B for Both, you are capturing a value during both an inbound and outbound process.
FIELD DESCRIPTIONS

Per SKU Class (defined in SKCL)
Only available if you are capturing a value
The SKU class to which you wish to attach the message or value. For example, if you specify Pallets, you will be prompted to enter a value for each inbound or outbound pallet or for any other SKU type assigned to the SKU class of Pallets. If you specify Cases and the like, you will be prompted to enter a value for each inbound or outbound case or any other SKU type assigned to the class Cases and the like.
Use SKU class 6 (Other) when you wish to capture one value for each receipt/ order line rather one value based on the line quantity. For example, you want to capture one temperature or inbound dimension for each receipt line regardless of the line quantity.
Entry Length Only available if you are capturing a value
The length of the value to be entered. The maximum length permitted is 250 characters. If the item that IPRO is attached to is also attached to a SCPR (Scan Parameter Profile) record, the length in SCPR will override the length in 
IPRO.
Data Type Only available if you are capturing a value
CHAR = Character
DATE = Date
INT = Integer
MONY = Money
NUM = Number
This field controls the formatting of values that you capture. If you select 
DATE, the number that you enter will be formatted as a date. If you select 
MONY, the number that you enter will be formatted in dollars and cents (for example, $99.99).
Use CHAR for serial and purchase order numbers.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 387
Transfer Value to Inventory
Only available if you are capturing a value
Y = Yes
N = No
If you specify Yes, the following will occur:
 item process code values will be transferred to inventory when the order or receipt is confirmed and can be viewed in LOIP (Look Up Item Process)
 inbound process values, if any, will be transferred to outbound orders when you run ORPE (Order Process Entry) or RFOPS (RF Outbound Process 
Scanning)
If you specify No, there will be no transfer of item process code values to inventory and therefore you cannot view them in LOIP.
Create Automatic 
Records
Only available if you are capturing a value
Y = Yes
N = No
If you specify Yes, you can create one process code value per pallet (if you specify Pallets in the Per SKU Class field) or one process code value per case/carton (if you specify Cases and the like in the Per SKU Class field). If you specify No, no records will be created for each pallet or each case/carton and you will not be able to access the Process Block of ENRE/ENOR.
The No option is only available if you are capturing temperatures by means of the TEMP code or if you use RF to receive or ship product.
FIELD DESCRIPTIONS

Entry Validation Rules Only available if you are capturing a non-numeric value and there is no SCPR record attached to the item
Equal or greater
Equal or less
Match exactly
No validation
If you specify Equal or greater, the value that you capture can have a length greater than or equal to the value in the Entry Length field. If you specify Equal or less, the value that you capture can have a length less than or equal to the value in the Entry Length field.
If you specify Match Exactly, the length of the value that you capture must match the value that you enter in the Entry Length field. If you specify No validation, no validation will be performed on the entry length.
Allow Duplicates Only available if you are capturing a value
Y = Yes
N = No
If you specify Yes, duplicate entries within the same receipt or order line will be allowed. If you specify No, no duplicates will be allowed within the same receipt or order line.
Delete After Confirmation Only available if you are capturing a value
Y = Yes
N = No
If you specify Yes, the system will delete the item process code entries from the receipt or order once you confirm it. If you specify No, the item process code entries will remain on your system until you purge your orders and receipts in PURG.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 389
Mandatory Entry Only available if you are capturing a value
Y = Yes
N = No
If you specify Yes, you will not be able to confirm the receipt or order if all process values have not been entered. If you specify No, you can confirm the receipt or order even if there are missing process values.
Locate Weight in Bar 
Code Dynamically
See the section on RFOPS in the RF User’s Guide.
Use Only Exact Quantity 
From This SKU Class
Only available if you are performing a weight scan in RFPIC or RFOPS and you are capturing weights from two or more SKU classes
Y = Yes
N = No
EXAMPLE
Quantity breakdown = 25 cases per pallet order line 1 = 5 cases order line 2 = 25 cases (1 full pallet)
order line 3 = 30 cases ( 1 full pallet plus 5 cases)
Yes option (only one scan for a full SKU class)
order line 1 = 5 scans (1 per case)
order line 2 = 1 scan for the pallet order line 3 = 5 scans (1 per case) plus 1 scan for the pallet
No option order line 1 = same as Yes option order line 2 = 1 scan for the pallet plus 25 scans for each case order line 3 = 1 scan for the pallet plus 30 scans for each case
Prompt User to Select 
Weight Measure Code
Only available if you are performing a weight only scan in RFPIC or RFOPS
Y = Yes
N = No
If you specify Yes, the RF operator will be prompted to select a weight measure code in RFPIC and RFOPS. If you specify No, the RF operator cannot override the standard weight measure code defined in IPRO.
FIELD DESCRIPTIONS

### SETTING UP THE CAPTURE OF AN OPERATOR-ENTERED VALUE <a id="setting-up-the-capture-of-an-operator-entered-value"></a>

1 Enter IPRO.
2 Use your pick list function to select an appropriate type of value. To select a code using a pick list, press 
F10 to display the pick list, and click on Execute Query to display the list of codes. Then position your cursor over the appropriate code using your arrow keys and click on Select to select it.
3 In the Entry Value field, key in Y for Yes and press Enter.
4 In the Inbound / Outbound / Both field, key in the appropriate value (I for Inbound, O for Outbound or B for Both) and press Enter.
5 In the Per SKU Class field, use your pick list function to select an appropriate SKU class.
6 In the Entry Length field, key in the length of the value to be entered by the operator.
7 In the Data Type field, use your pick list function to select an appropriate data type.
8 In the Transfer Value to Inventory field, key in Y for Yes or N for No and press Enter.
9 In the Create Automatic Records field, key in Y for Yes or N for No and press Enter.
10 In the Validate Entry Value field, key in Y for Yes or N for No and press Enter.
11 In the Allow Duplicates field, key in Y for Yes or N for No and press Enter.
Weight Modifier Override Only available if you are performing a weight only scan in RFPIC or RFOPS
If required, you can specify a weight modifier and the scanned in weight will be multiplied by the modifer.
FIELD DESCRIPTIONS (DETAIL BLOCK)
Document Code (defined in DOCU)
Optional
The document to which you wish to attach the message or item process value. 
You can attach the same message or item process value to two or more documents.
NOTE Not all documents support process values. Contact your HighJump implementation consultant for further information.
Message Optional
The text of your message.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 391
12 In the Delete After Confirmation field, key in Y for Yes or N for No and press Enter.
13 In the Mandatory Entry field, key in Y for Yes or N for No and press Enter.
14 Press Enter to bypass the Locate Weight in Bar Code Dynamically field.
15 In the Use Only Exact Quantity From This SKU Class field, key in Y for Yes or N for No and press Enter.
16 In the Prompt User to Select Weight Measure Code, key in Y for Yes or N for No and press Enter.
17 If required, in the Detail Block key in the document code of the document to which the process value is attached and press Enter or click on Return to Main and Exit to exit IPRO if you do not require a document.
18 Click on Return to Main and Master Block to exit the Detail Block.

Item Process(es) screen showing a 20-digit inspection level to be entered by the operator
19 When you finish entering your item process codes, click on Exit to exit.

### SETTING UP A PREDEFINED MESSAGE ON A DOCUMENT <a id="setting-up-a-predefined-message-on-a-document"></a>

1 Enter IPRO.
2 Click on Create Record.
3 Key in an item process code and press Enter.
4 Key in a description for your code and press Enter.
5 Use your pick list function to select an appropriate type of value. To select a code using a pick list, press 
F10 to display the pick list, and click on Execute Query to display the list of codes. Then position your cursor over the appropriate code using your arrow keys and click on Select to select it.
6 In the Entry Value field, key in N for No and press Enter.

7 In the Detail Block, key in the document code of the document to which you wish to attach the message and press Enter.
8 Key in the text of your message and press Enter.
9 Click on Return to Main and Exit to exit the Detail Block.

Item Process(es) screen showing the message “Cube:________” that will print on the receiving tally
10 When you finish entering your item process code, click on Exit to exit.

### Setting Up Your Item Process Profile in IPRP <a id="setting-up-your-item-process-profile-in-iprp"></a>

In this program, you attach the item process code or codes that you created in IPRO to the item process profile. In ITEM you will attach this profile to the item to which it belongs. 
If you set the Transfer Value to Inventory flag in IPRO to Yes, you can assign dependencies to item process codes. You use dependencies when you are capturing weight or cube information and you want to attach this weight or cube process code to another process code.
For example, you set up a process code of BC to capture a bar coded label and assign this process code the dependency of Parent. Then you set up a second process code to capture the weight or cube that is encoded in the bar code label and assign this process code the dependency of Child. When you look up the item in 
LOIP (Look Up Item Process), the parent process code will appear in the header block of this program and the child process code of codes will appear in the detail block.

OPERATIONS 2 GUIDE 4.2* 393
You do not use dependencies when you are attaching a predefined message to a document or when you are capturing values like serial numbers or catch weights and these values do not contain weight or cube information that form part of another item process code. 
1 Enter IPRP.
2 If you need a new item process profile, click on Create Record.
3 Key in a process profile code and press Enter.
4 Key in a description for your code and press Enter.
5 In the Process Code field, key in your process code and press Enter or use your pick list function to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to display the list of codes. Then position your cursor over the appropriate code using your arrow keys and click on Select to select it.
FIELD DESCRIPTIONS
Process Profile Code Mandatory
Your process profile code; for example, PO for Purchase Order Number.
Description Mandatory
Your process profile code description.
Process Code (defined in IPRO)
Mandatory
Your item process code.
Dependency Only available if you set the Transfer Value to Inventory flag in IPRO to Yes.
P = Parent Code
C = Child Code
N = No Dependency (default)
The parent and child dependencies are only used when you have bar coded process codes containing weight or cube information. The bar coded process code is the parent code and the weight or cube values are the child codes. 
Item process codes assigned the dependency of child must have CUBE, 
WGTG or WGTN as their Type Description in IPRO.
Process values set up as parent codes will be appear in header block of LOIP. 
Process values set up as child codes will appear in the detail block of LOIP. 
You cannot query on child process values.

6 In the Dependency field, key in the appropriate value (P for Parent Code, C for Child code or N for No 
Dependency) and press Enter.
7 Press Enter to bypass the Correction field.
8 If you wish to add another process code to this profile, repeat steps 6 to 8 to add another line.

Item Process Profile screen showing two process codes
9 When you finish creating your item process profile, click on Return to Main and Master Block. Then click on Exit to exit.

### Setting Up Your Items in ITEM <a id="setting-up-your-items-in-item"></a>

In ITEM, you attach your IPRP code to the item.

OPERATIONS 2 GUIDE 4.2* 395

Item screen

### SETTING UP A FLOW IN DIFP <a id="setting-up-a-flow-in-difp"></a>

If you are setting up an item process code to capture an operator-entered value, you can add a flow to your flow profile in order to track the capture of the value. If you do not set up a flow and forget to enter your process values, you may not be able to confirm the receipt or order.
Process Code 
CW (Catch 
Weights) 
attached to item 
A1

Depositor Workflow Profile (DIFP) screen showing flow CAWE (Capture Weight)

### Setting Up Catch Weights <a id="setting-up-catch-weights"></a>

The entry of catch weights can be either mandatory or optional. If you define catch weights as optional, you will be able to confirm the receipt or order without entering all your catch weights. If you define catch weights as mandatory, you will not be able to advance to the next flow or confirm the receipt or order unless all your catch weights have been entered.
You define catch weights as mandatory by attaching the appropriate special verify program to your DIFP profile. There are two special verify programs:
 CREW (Check receipt weights from IPRO) for receipts
 CORW (Check order weights from IPRO) for orders
For inbound catch weights, the following setup is required:
FLOW
SET IN SPECIAL VERIFICATION 
BLOCK OF DIFP for any flow except CORE (Confirm 
Receipt)
Complete flag = Yes
Sequence flag = B (Before) or A (After)
for CORE (Confirm Receipt) Complete flag = Yes
Sequence flag = B (Before)

OPERATIONS 2 GUIDE 4.2* 397
For outbound catch weights, the following setup is required:
You can attach these special verify programs to any flow in DIFP. If you attach your special verify to CORE (Confirm Receipt) or COOR (Confirm Order), you will not be able to confirm the receipt or order until all your catch weights have been entered. If you attach your special verify to any other flow, you will be unable to advance to the next flow until all your catch weights have been entered.
There are two catch weight options: you can enter catch weights for reference purposes only or you can enter catch weights that override the system-defined gross or net weight of each receipt/order line.
FLOW
SET IN SPECIAL VERIFICATION 
BLOCK OF DIFP for any flow except COOR (Confirm Order) Complete flag = Yes
Sequence flag = B (Before) or A (After)
for COOR (Confirm Order) Complete flag = Yes
Sequence flag = B (Before)
OPTION DESCRIPTION SETUP
Reference purposes only Catch weight appears in the Process Block of ENRE/ENOR, but does not change the gross or net weight of the receipt/order line.
Set the Standard Weight field in ITEM to Y for Standard Weight.
Catch weight = actual weight of inventory being received or shipped
Catch weight overrides the system-defined gross or net weight of each receipt/order line.
Set the Standard Weight field in ITEM to any weight option other than Y for Standard 
Weight.

DIFP screen showing special verification program CORW (Check Order Weights from IPRO)

### Adding Process Values to a Receipt <a id="adding-process-values-to-a-receipt"></a>

You add process values to a receipt by entering the Process Value Block of ENRE.
1 Enter ENRE.
2 Enter the Header Block information for the receipt.
3 In the Line Block, enter your item code and any required inventory levels.
4 Enter your expected and received quantities.
5 If required, press Enter to bypass the Weight Code and any other weight-related fields.
6 If required, enter your location.
7 When a new line block is displayed, click on Return to Main to exit create mode and display the first line on the receipt.
8 Press Enter until your cursor is positioned on Process field. The value in this field should be Y for Yes to indicate that a process value is expected. 
9 Click on Process Data to enter the Process Value Block.
10 Key in your first process value and press Enter.

OPERATIONS 2 GUIDE 4.2* 399

ENRE screen showing prompt for serial numbers
11 Repeat the above step for each additional process value that you wish to add to the receipt. If you attempt to exit before entering all your values, a warning box will appear with the following message: “Not all values have been entered. Do you want to exit (Y/N)?” You can exit without entering all your values, but you must return to ENRE at a later time to enter the missing values. All values must be entered before you can confirm the receipt.
12 When you finish entering all your lines, click on Exit and Return to Main.
13 Continue to process the receipt normally.

### CAPTURING TEMPERATURES FOR INBOUND PRODUCT <a id="capturing-temperatures-for-inbound-product"></a>

If you wish to capture temperatures for inbound product and need only one temperature per receipt line, create an item process code called TEMP and set the flags in IPRO as follows: 
Entry Value = Y
Per SKU Class = Other
Transfer Value to Inventory = N
Create Automatic Records = N

IPRO screen for the capture of temperatures
Then attach your TEMP code to the appropriate item by means of the IPRP profile. When you enter the Line 
Block of ENRE, you will be prompted to enter a temperature in the Temperature field for the entire receipt line.

ENRE screen showing entry of a temperature

### MANUALLY ENTERING THE DIMENSIONS OF INBOUND PRODUCT <a id="manually-entering-the-dimensions-of-inbound-product"></a>

If you wish to manually enter the dimensions of inbound product because the standard dimensions defined in 
ITEM do not apply, create an item process code called RD and set the flags in IPRO as follows:
Entry Value = N

OPERATIONS 2 GUIDE 4.2* 401
Per SKU Class = Other
Then attach your RD code to the appropriate item by means of the IPRP profile. When you enter the Line 
Block of ENRE, you will be able to access the Length, Width and Height fields so as to change the default values.

IPRO screen for the capture of dimensions
NOTE If you receive the same inventory entity multiple times and enter different dimensions each time (for example, 10,000 cubic inches, 12,000 cubic inches and 
14,000 cubic inches), AccellosOne 3PL will use the average of these three values (12,000) when calculating the number of cubic inches that should be subtracted from a location’s capacity when you ship an order. 

ENRE screen showing access to Length, Width and Height fields
When you enter the Line Block of ENRE, you will have access to the Length, Width and Height fields. You can press Enter to accept the default values or you can key in new values and press Enter.

### Adding Process Values to an Order <a id="adding-process-values-to-an-order"></a>

You add process values to an order by entering the Process Value Block of ENOR.
1 Enter ENOR.
2 Enter the Header Block information for the order.
3 In the Line Block, enter your item code and any required inventory levels.
4 Enter your expected and received quantities.
5 If required, press Enter to bypass the Weight Code and any other weight-related fields.
6 If required, enter your location.
7 When a new line block is displayed, click on Return to Main to exit create mode and display the first line on the order.
8 Press Enter until your cursor is positioned on Process field. The value in this field should be Y for Yes to indicate that a process value is expected. 
9 Click on Process Data to enter the Process Value Block.
10 Key in your first process value and press Enter.

OPERATIONS 2 GUIDE 4.2* 403

ENOR screen showing entry of catch weights
11 Repeat the above step for each additional process value that you wish to add to the order. If you attempt to exit before entering all your values, a warning box will appear with the following message: “Not all values have been entered. Do you want to exit (Y/N)?” You can exit without entering all your values, but you must return to ENOR at a later time to enter the missing values. All values must be entered before you can confirm the order.
12 When you finish entering all your lines, click on Exit and Return to Main.
13 Continue to process the order normally.

### Looking Up Process Values in LOIP <a id="looking-up-process-values-in-loip"></a>

You can look up item process values in LOIP (Look Up Item Process) if the Transfer Value to Inventory flag of the process code has been set to Y for Yes and if the order or receipt has been confirmed. You can query on an item process code or on the value itself. For each code or value that you look up, LOIP shows the following:
 the date that the product was processed
 the flow at which the item entered inventory (CR = Confirmed Receipt or CO = Confirmed Order)
 the receipt or order number on which it was entered
 the line number in the receipt or order
 the line number in the Location Block
 the process quantity
 the gross weight, net weight or cube (only available for parent child dependencies defined in IPRP in which the Type Description of the child is set to CUBE, WGTG or WGTN)
1 Enter LOIP.

2 Key in your criteria and press Enter. You can query on customer code, level 1, 2, 3 and 4 value, process value or process code. 

To query by process code, you would press Enter until your cursor was positioned in the Process Code field and then you would enter your process code (for example, CW for Catch Weights). To query by process value, you would press Enter until your cursor was positioned in the Process Value field and then you would enter your value (for example, A-1234 for a serial number query).
3 When you finish entering your criteria, click on Execute Query.
AccellosOne 3PL will retrieve all process value records that meet the criteria that you specified.

Look Up Item Process (LOIP) screen showing a serial number for code SN
4 Use your arrow keys to scroll through the records in the header block of LOIP.
5 When you reach the record that you wish to query on, click on Detail Block to enter the Detail Block.

OPERATIONS 2 GUIDE 4.2* 405

Look Up Item Process (LOIP) screen showing confirmed receipt 147 processed on 05.05.08
6 When you finish viewing the Detail Block, click on Master Block and Exit to exit.

### Looking Up Process Values in LORE/LOOR <a id="looking-up-process-values-in-lore-loor"></a>

You can look up item process values attached to a receipt in LORE and you can look up item process values attached to an order in LOOR.
1 Enter LORE or LOOR.
2 Retrieve the receipt or order that you wish to look up.
3 Click on Line Block to enter the Line Block.
4 Use your arrow keys to scroll forward to the line that you wish to look up.

LORE screen showing Line Block
5 Press Enter until your cursor is positioned in the Process field. The value in this field should be Y for Yes to indicate that a process value is expected.
6 Click on Process Data to enter the Process Block.
Process field should be set to 
Y for Yes

OPERATIONS 2 GUIDE 4.2* 407

LORE screen showing catch weights and serial numbers in the Process Block
7 If required, use your arrow keys to scroll through the list of process values.
8 When you finish looking up your process values, click on Line Block and Master Block. Then click on Exit to exit.

### Modifying Process Values in ENRE/ENOR <a id="modifying-process-values-in-enre-enor"></a>

You can modify an item process value at any flow before CORE (Confirm Receipt) or COOR (Confirm Order).
1 Enter ENRE or ENOR.
2 Retrieve the receipt or order whose process values you wish to modify.
3 Click on Line Block to enter the Line Block.
4 Select the line whose process values you wish to modify.
5 Press Enter until your cursor is positioned in the Process field.
6 Click on Process Data.
7 Proceed to make the required changes to your process values.
8 When you finish making your changes, click on Exit to exit the Item Process Block.
9 Click on Return to Main and Master Block.
10 Click on Exit to exit ENRE/ENOR.

### TRANSFERRING PROCESS VALUES <a id="transferring-process-values"></a>

You can automatically transfer inbound process values such as catch weights and serial numbers to outbound orders if you set the Transfer Value to Inventory flag in IPRO to Y for Yes. For example, you receive item A, lot 101, pallet ID 123 and assign it a catch weight of 100 lbs. When you ship the same inventory in 
ENOR and run the program ORPE (Order Process Entry), AccellosOne 3PL will automatically transfer the catch weight of 100 lbs. to the order.
You can only transfer process values attached to full pallets or to whichever SKU type is assigned the highest 
SKU class. For example, if your quantity breakdown is 100 cases per pallet and you receive a partial pallet (say, 75 cases), you cannot transfer process values.
The process values can be attached to any SKU in the item’s quantity breakdown. For example, if your quantity breakdown is pallet/case/each, you can capture one process value per pallet, one process value for each case on the pallet or one process value for each each on the pallet.

### SETTING UP THE TRANSFER OF PROCESS VALUES <a id="setting-up-the-transfer-of-process-values"></a>

The following setup is required in IPRO:
 Type of Value = the type of value being captured
 Inbound / Outbound / Both = Both
 Per SKU class = any SKU class
 Create Automatic Records = Yes
 Transfer Value to Inventory = Yes
Example 1 — Setup for Catch Weights in IPRO

IPRO screen showing process code for catch weights called CW1
Example 2 — Setup for Serial Numbers in IPRO

OPERATIONS 2 GUIDE 4.2* 409

IPRO screen showing process code for serial numbers called SN1

### Performing the Transfer <a id="performing-the-transfer"></a>

There are five steps to follow in performing the transfer:
 you enter your receipt in ENRE
 you enter your process values in REPE (Receipt Process Entry)
 you print your receipt documents and confirm the receipt in the normal manner
 you enter your order in ENOR
 you transfer your process values in ORPE (Order Process Entry)

### ENTERING THE RECEIPT IN ENRE <a id="entering-the-receipt-in-enre"></a>

The quantity being received must always equal one full pallet (or one drum if drum is assigned to the highest 
SKU class). For example, if you receive in cases, the number of cases that you receive must equal one full pallet.

### ENTERING PROCESS VALUES IN REPE <a id="entering-process-values-in-repe"></a>

You enter your process values in REPE (Receipt Process Entry). You can enter your process values at any flow before CORE (Confirm Receipt).
1 Enter REPE.
2 Key in your receipt number and press Enter.
3 Key in your line number and press Enter.
4 Key in your process values.

REPE screen showing captured process values
5 When you finish entering your process values for the first receipt line, click on Exit to return to Header 
Block.
6 Repeat steps three to five for each additional line on the receipt.
7 When you finish entering all your process values for each line, click on Exit twice to exit REPE.

OPERATIONS 2 GUIDE 4.2* 411

### ENTERING YOUR ORDER IN ENOR <a id="entering-your-order-in-enor"></a>

The following conditions apply to your order in ENOR.

### TRANSFERRING INBOUND PROCESS VALUES TO OUTBOUND ORDERS IN ORPE <a id="transferring-inbound-process-values-to-outbound-orders-in-orpe"></a>

You transfer your process values to the order in ORPE (Order Process Entry). You can transfer your process values at any flow before COOR (Confirm Order) provided that you have either run allocation or you have entered an R-type line in ENOR with all inventory levels specified.
The following restrictions apply to the transfer of process values:
 You cannot transfer process values if you are missing one or more values. For example, if you have five cases on one full pallet and one of the cases is missing a process value, you cannot transfer the process values in ORPE. You must enter the missing catch weight(s) in ENOR and then return to ORPE to perform the transfer.
 You cannot transfer process values if you have two or more inventory entities that are identical. For example, you have two pallets with the same level 1/2/3 values and you wish to ship out a single pallet.
 Unless you are clearing out all inventory, the quantity being shipped must always equal one full pallet (or one drum if drum is assigned to the highest SKU class). For example, if you ship in cases, the number of cases that you ship must equal one full pallet.
1 Enter ORPE.
2 Key in your order number and press Enter.
3 Key in your line number and press Enter.
ORPE will display the Item Process Block showing the process values that were transferred to the order.
If you are clearing out all inventory:
If you are NOT clearing out all inventory:
Clearing out all inventory means shipping the last remaining inventory for a particular inventory entity. For example, if you have 
50 cases of item A, lot 101, pallet ID 001 and ship out all 50 cases, you are clearing out all inventory.
When clearing out all inventory, you can ship full pallets, partial pallets or individual cases.
NOTE You cannot clear out all inventory if the inventory that you are clearing out in 
ENOR is on another open order.
The quantity being shipped must always equal one full pallet (or one drum if drum is assigned to the highest SKU class). For example, if you ship in cases, the number of cases that you ship must equal one full pallet.

ORPE screen showing transferred process values
4 If you wish to change the process values, key in your new value and press Enter.
5 Click on Exit to return to the Header Block.
6 Repeat steps three to five for each additional line on the order.
7 When you finish transferring the process values for each line, click on Exit to exit ORPE.

OPERATIONS 2 GUIDE 4.2* 413
