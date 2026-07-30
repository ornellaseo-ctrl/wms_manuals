---
title: "Alocação de Entrada e Saída"
description: "Directed put-away, perfis de localização, alocação de pedidos e prioridades."
layout: default
---

# Alocação de Entrada e Saída

Directed put-away, perfis de localização, alocação de pedidos e prioridades.

**Fluxo principal:** `Entrada: ILOP/PUPR/IPUP | Saida: PIPR/CCOP -> ASOR/DEOR -> ORPR`

> Fonte: manuais K do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Inbound Allocation <a id="inbound-allocation"></a>

*Manual K — Allocation and Wave Manager*

# Manual K — Allocation and Wave Manager Guide (Alocação e Wave Manager)
> **ID do Manual:** K  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Alocação inbound (put-away dirigido via ILOP/PUPR/IPUP) e outbound (picking via PIPR/ASOR/DEOR). Wave Manager para agrupamento e priorização de ordens. Replenishment (RFRO/RFRP). Directed moves (DMPA/DMPR). Reserve logic. Pick lines.
---

### Overview <a id="overview"></a>

There are two main put-away programs in AccellosOne 3PL: ILOP (Item Location Profile) and IRHP (Item 
Receipt Hold Profile Code).
ILOP is the most flexible option for putting away product. You can select from a number of logical groups when defining your put-away rules. You can have AccellosOne 3PL assign locations based on isolator zones, the size of the location, the location’s hold code, whether the location is empty or partially filled, whether the location was the last location used for a particular item, etc.
IRHP is a much more limited put-away program. If there is an exact match between the item’s hold code and the location’s hold code, AccellosOne 3PL will assign the item to that location and normal ILOP processing will be bypassed.

### Item Location Profile for Put-Away (ILOP) <a id="item-location-profile-for-put-away-ilop"></a>

In this program, you define the algorithms that you want AccellosOne 3PL to use when it performs directed put-away. You can have the system assign locations based on isolator zones, the size of the location, whether the location is empty or partially filled and other criteria that you specify. In ILOP you define the following:
 the isolator zone to which the product belongs
 the overflow warehouse for the product
 the overflow location for the product in the overflow warehouse
 the algorithms that you want the system to use for the put-away of this product 
You can set up as many different profiles as you need. Generally speaking, however, you would set up one profile for each isolator zone. Depending on how you defined your isolator zones, you would have one ILOP profile for each group of products, each group of customers, a specific product, a specific customer, etc. If you have an isolator zone (for example, MEAT OVERFLOW) that is used strictly as an overflow area, no profile would be required for this isolator zone.
The profile that you create in ILOP is attached to ITEM.

### UNDERSTANDING DIRECTED PUT-AWAY <a id="understanding-directed-put-away"></a>

In directed put-away, you want to place product in the best possible location. If the best possible location is not available, you want to place it in the next best location and so on and so forth. In ILOP, you tell the system the criteria that you wish it to use for the purpose of identifying the best and the next best locations.
You define your criteria by means of sequences. Each sequence contains a number of parameters for selecting a location. The following example shows five sequences that progressively define increasingly less desirable locations.
Sample Sequences for Selecting Locations
Sequence 1 (ideal)
Use only exact match isolator code
Use only empty locations
Fill location to maximum capacity

In sequence 1, which contains the strictest selection criteria, the system searches for a location that satisfies all the parameters. If it finds such a location, the product is allocated and the other sequences are never run. 
If the system is unable to find a location, it proceeds to sequence 2.
In sequence 2, which is less strict, the system searches for a location that satisfies all the parameters. If it finds such a location, the product is allocated and the other sequences are never run. If the system is unable to find a location, it proceeds to sequence 3.
In sequences 3, 4 and 5, the system continues to search for a location that satisfies all the parameters. If the system is unable to find a location in any of these sequences, it will allocate the product to the overflow location designated in ILOP.

### STANDARD LOGICAL GROUPS FOR PUT-AWAY <a id="standard-logical-groups-for-put-away"></a>

There are 24 logical groups in ILOP. Each group has two or more mutually exclusive options. From each group, you select the appropriate option. If you do not wish to use a particular group, select the first option in the group to deactivate it. For example, if you do not wish to use the Hold codes group, you would select the first option, “Ignore hold codes in location”.
ISOLATOR GROUP (I0500)
Sequence 2 (next best)
Use only exact match isolator code
Use any empty or partially filled location
Fill location to maximum capacity
Sequence 3 (next best)
Use any overflow isolator code
Use only empty locations
Fill location to maximum capacity
Sequence 4 (next best)
Use any overflow isolator
Use any empty and/or partially filled location
Fill location to maximum capacity
Sequence 5 (worst)
Ignore isolator codes
Use any empty and/or partially filled location
Fill location to maximum capacity
TIP You can define up to nine passes or sequences in any given profile. It is important to bear in mind, however, that each sequence requires time to perform the specified searches to validate locations. Therefore, you must strike a balance between the requirement to place product in the best possible location using many sequences and the requirement to put product away in a reasonable time.
ignore isolator codes Do not use isolator codes for determining a put-away location.
use only exact match isolator code Match the item isolator with the location isolator. This is a method for keeping similar product together and dissimilar product apart.
Sample Sequences for Selecting Locations

ZONE CODE GROUP (I0600)
EMPTY AND/OR PARTIALLY FILLED LOCATION GROUP (I1000)
PARTIALLY FILLED LOCATION GROUP (I1500)
use any overflow isolator code Place product in the overflow isolators which have been attached to the product isolator. A product may have many overflow isolators. The system will try to place the product in the first overflow isolator and then move on to other isolators if necessary.
ignore zone codes Do not use zone codes for determining a put-away location.
use only exact match zone code Match the item zone code with the location zone code. 
use first overflow zone code Place product in the first overflow zone that has been attached to the product’s warehouse zone. 
use first & second overflow zone code Place product in either the first or second overflow zone that has been attached to the product’s warehouse zone. 
use first, second & third zone code Place product in either the first, second or third overflow zone that has been attached to the product’s warehouse zone. 
use any overflow zone code Place product in any overflow zone that has been attached to the product’s warehouse zone. A product may have many overflow zones. The system will try to place the product in the first overflow zone and then move on to other zones if necessary.
use any empty and/or partially filled location
Place product in an empty or partially filled location. If inventory is placed in a partially filled location, the system will only place inventory if the inventory meets the criteria that you select in the next group (Partially Filled Location Group).
use only empty locations Place product only in locations that are empty. If you select this option, you must select “use any partially filled location regardless of what is there” from the Partially Filled Location Group.
use only partially filled locations Place product only in locations that are partially filled — provided that the criteria in the next group (Partially Filled Location Group) 
are also met.
use any partially filled location regardless of what is there
For those items that are being placed in partially filled locations, place inventory in locations regardless of what inventory is already being stored in the location.
use partial locations which have only the same entity of level 1
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same item and no other item (customer may differ).

partial locations, only the same level 1 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same entity of level 2
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same level 2 and no other level 2 (customer and level 1 may differ).
partial locations, only the same level 1/
2 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same entity of level 3
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same level 3 and no other level 3 (customer and other levels may differ).
partial locations, only the same level 1/
2/3 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same entity of level 4
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same level 4 and no other level 4 (customer and other levels may differ).
partial locations, only the same level 1/
2/3/4 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same depositor code 
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer and no other customer.
use partial locations which have only the same entity up to level 1
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer and item and no other customer or item.
partial locations, at least same level 1 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same entity up to level 2
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item and level 2 (lot number, date code, etc.) and no other customer/item/level 2.
partial locations, at least same level 1/2 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only the same entity up to level 3
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item, level 2 and level 3 (pallet ID, etc.) and no other customer/item/level 2/3.
partial locations, at least same level 1/
2/3 and match PUPR date range
Same as previous but must also match PUPR date range.

IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I2000)
use partial locations which have only the same entity up to level 4
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item, level 2, level 3 and level 4 and no other customer/item/level 2/3/4.
partial locations, at least same level 1/
2/3/4 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have at least the same depositor code
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer.
use partial locations which have at least the same entity up to level 1
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer and item.
use partial locations which have at least the same entity up to level 2
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item and level 2 (lot number, date code, etc.).
use partial locations which have at least the same entity up to level 3
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item, level 2 and level 3 (pallet ID, etc.).
use partial locations, at least same level 1/2/3 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have at least the same entity up to level 4
For those items that are being placed in partially filled locations, place inventory in locations that already have inventory for the same customer, item, level 2, level 3 and level 4.
use partial locations, at least same level 1/2/3/4 and match PUPR date range
Same as previous but must also match PUPR date range.
ignore on receipt when calculating capacity by quantity
When calculating capacity by quantity, do not take into account inventory on receipt (that is unconfirmed receipts). 
EXAMPLE
You put unconfirmed product in location x, which was previously empty (on-hand = 0). If you specify the ignore on receipt option, the system will not add the on-receipt quantities to the on-hand quantities when evaluating the location’s capacity; as a result, location x will be considered empty and the system will either assign this location (if empty locations were specified) or assign another location (if partially filled locations were specified and other criteria are met).

IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY WEIGHT 
GROUP (I2200)
Put-away by weight must be activated in the Company Parameters Block of COMP (Company Code). 
IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY CUBE GROUP (I2300)
IGNORE/USE IN TRANSIT WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I2500)
use on receipt when calculating capacity by quantityWhen calculating capacity by quantity, do take into account unconfirmed receipts. 
EXAMPLE
You put unconfirmed product in location x, which was previously empty (on-hand = 0). If you specify the use on receipt option, the system will add the on-receipt quantities to the on-hand quantities when evaluating the location’s capacity; as a result, location x will be considered filled or partially filled and the system will start assigning product to another locations (if empty locations were specified) or assign product to this location (if partially filled locations were specified and other criteria are met).
ignore on receipt when calculating capacity by weight
When calculating capacity by weight, do not take into account inventory on receipt (that is unconfirmed receipts). 
use on receipt when calculating capacity by weightWhen calculating capacity by weight, do take into account unconfirmed receipts. 
ignore on receipt when calculating capacity by cube
When calculating capacity by cube, do not take into account inventory on receipt (that is unconfirmed receipts). 
use on receipt when calculating capacity by cubeWhen calculating capacity by cube, do take into account unconfirmed receipts. 
ignore in transit when calculating capacity by quantity
When calculating capacity by quantity, do not take into account inventory in transit (that is, being transported to the warehouse). 
use in transit when calculating capacity by quantity
When calculating capacity by quantity, do take into account inventory in transit (being transported to the warehouse). 

IGNORE/USE IN TRANSIT WHEN CALCULATING CAPACITY BY CUBE GROUP (I2700)
IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I300)
IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY WEIGHT 
GROUP (I3200)
Put-away by weight must be activated in the Company Parameters Block of COMP (Company Code). 
ignore in transit when calculating capacity by cube
When calculating capacity by cube, do not take into account inventory in transit (that is, being transported to the warehouse). 
use in transit when calculating capacity by cube
When calculating capacity by cube, do take into account inventory in transit (being transported to the warehouse). 
ignore on order when calculating capacity by quantity
When calculating capacity by quantity, do not take into account inventory on order.
EXAMPLE
You have 10 cases in location x which are on order but not picked or confirmed. If you specify the ignore on order option, the system will ignore the product’s on-order status when evaluating the location’s capacity. As a result, it will consider location x to be full and will place product in another location.
use on order when calculating capacity by quantity
When calculating capacity by quantity, do take into account inventory on order. 
EXAMPLE
You have 10 cases in location x which are on order but not picked or confirmed. If you specify the use on order option, the system will subtract the on-order quantity from the on-hand quantity when evaluating the location’s capacity. As a result, it will consider location x to be empty and will allocate product to that location.
ignore on order when calculating capacity by weight
When calculating capacity by weight, do not take into account inventory on order (that is unconfirmed orders). 
use on order when calculating capacity by weight
When calculating capacity by weight, do take into account unconfirmed orders. 

IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY CUBE GROUP (I3300)
IGNORE/USE OUTSTANDING MOVES/RELOCATES WHEN CALCULATING 
CAPACITY BY QUANTITY GROUP (I3500)
Outstanding moves/relocates refers to product that has been moved by means of a directed move.
IGNORE/USE OUTSTANDING MOVES/RELOCATES WHEN CALCULATING 
CAPACITY BY CUBE GROUP (I3600)
Outstanding moves/relocates refers to product that has been moved by means of a directed move.
FILL LOCATION GROUP (I3800)
HOLD CODE GROUP (I4000)
ignore on order when calculating capacity by cube
When calculating capacity by cube, do not take into account inventory on order (that is unconfirmed orders). 
use on order when calculating capacity by cube
When calculating capacity by cube, do take into account unconfirmed orders. 
ignore outstanding moves/ relocates when calculating capacity by quantity
When calculating capacity by quantity, do not take into account inventory that is part of an outstanding move or relocate.
use outstanding moves/ relocates when calculating capacity by quantity
When calculating capacity by quantity, do take into account inventory that is part of an outstanding move or relocate.
ignore outstanding moves/ relocates when calculating capacity by cube
When calculating capacity by cube, do not take into account inventory that is part of an outstanding move or relocate. 
use outstanding moves/ relocates when calculating capacity by cube
When calculating capacity by cube, do take into account inventory that is part of an outstanding move or relocate.
fill location to maximum capacity Place inventory based on the cube capacity of the location regardless of the standard pallet stack. If activated, this option may require you to break a pallet in order to achieve maximum location usage.
fill location to full pallet maximum capacity only
Place inventory based on the standard pallet stack pattern. Do not break a pallet in order to achieve maximum space usage.
ignore location/inventory hold codes Do not use hold codes for determining a put-away location.

LOCATION SIZE GROUP (I4500)
This option is only available if you have set up location size codes in LOCS (Location Size Codes) and you have assigned a location size code to inbound product during receipt entry. Location size codes must be activated by HighJump.
In the Empty and/or partially filled location group, you must select “Use only empty locations”.
CUBE CAPACITY GROUP (I5000)
LAST LOCATION USED GROUP (I6000)
The options in this group allow you to give priority to the last location used for a particular item. A location is considered to be the “last used” if you have put away, relocated or adjusted a given item into that location before or you have assigned that location to the item on a receipt.
use any location with an exact match of hold code
Place product in a location only if the hold code on the product being put-away matches the location’s hold code and there are no other holds in the location. If neither the product being put-away nor the location have a hold code and other product already in the location is not on hold either, AccellosOne 3PL considers the “exact match” condition to be satisfied.
NOTE
Product that is not on hold is not considered an “exact match” for this parameter. Therefore, if a location has one pallet on hold ABC and one pallet not on any hold, the system will not allocate product with hold ABC to this location because the existing product is considered to have mixed hold types.
use any location with a hold code Place product in a location only if the product being put-away and the product already stored in the location are both on hold (no exact match of hold code required).
ignore location size codes On receipt of inventory, do not use location size codes for determining a put-away location.
use only exact match location size codes
On receipt of inventory, match the location size code entered on the receipt location line with the location’s location size code. 
use any overflow location size codes On receipt of inventory, place product in any location where the location size code assigned to the receipt matches the location’s overflow location size code. The system will assign such product in the order specified in the Overflow Sequence Number field in 
LOCS.
ignore cube capacity On receipt of inventory, do not use cube capacity for determining a put-away location.
fill to 10, 20, 30%, etc. by cube capacity On receipt of inventory, place product in any location in which the quantity already in the location is such that that quantity plus the new inventory fills the location to the desired capacity. 

In order to activate this group, you must set the Track Last Used for Put-Away field in LOCA to the appropriate value (F, H, R T or Y) for all locations to which this option applies.
Do not give priority to the last location used 
When assigning locations to inventory, do not take into account the last location used for the item.
Give priority to the last used location for the item
When assigning locations to inventory, give priority to the last location used for the item.
Give priority to the last used location for the master item
When assigning locations to inventory, give priority to the last location used for the master item to which the item belongs. A master item’s location is the location of the last non-master item received. 
For example, suppose your master item is A and your non-master items are A1, A2 and A3. You receive A1 into location 100 and this sets the master item’s location to 100 as well. Then you receive A2. 
The last location used for the master item is location 100 and A2 will be assigned this location as well.
Give priority to the last used location for the item then master item
When assigning locations to inventory, give priority to the last location used for the item. If this location is full, give priority to the last location used for the master item.
Give priority to the last used location for the master item then item
When assigning locations to inventory, give priority to the last location used for the master item. If this location is full, give priority to the last location used for the item.
Use last used location for the item regardless of capacity
When assigning locations to inventory, give priority to the last location used for the item even if this location is full.
Use last used location for Level 1/2 regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2 even if this location is full.
Use last used location for Level 1/2/3 regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3 even if this location is full.
Use last used location for Level 1/2/3/4 regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4 even if this location is full.
Use last used location for master item regardless of capacity
When assigning locations to inventory, give priority to the last location used for the master item even if this location is full.
Use last used location for the item then the master item regardless of capacity
When assigning locations to inventory, give priority to the last used location for the item even if the location is full. If there is no last location for the item, give priority to the last used location for the master item even if the location is full.
Use last used location for the master item then the item regardless of capacity
When assigning locations to inventory, give priority to the last used location for the master item even if the location is full. If there is no last location for the master item, give priority to the last used location for the item even if the location is full.
Use last used location for the same receipt
When assigning locations to inventory, give priority to the last location used for any item on the same receipt.

CALCULATE CAPACITY BY LOWEST/HIGHEST SKU CLASS GROUP (I6500)
OPPORTUNISTIC CROSS-DOCKING GROUP (I7000)
Opportunistic cross-docking allows you to put-away a receipt into a cross-dock location located on your receiving/shipping dock rather than into a bulk, rack or pick line location. See [Opportunistic Cross-Docking](pick-lines-replenishment.html#opportunistic-cross-docking) for further information on setting up opportunistic cross-docking.
Use last used location for the inventory level 1,2
When assigning locations to inventory, give priority to the last location used for inventory level 1,2.
Use last used location for the inventory level 1,2,3
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3.
Use last used location for the inventory level 1,2,3,4
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4.
Try last used location, aisle, zone for the item
When assigning locations to inventory, give priority to the last location used for the item, then the same aisle and then the same zone.
Try last used location, aisle, zone for the master item
When assigning locations to inventory, give priority to the last location used for the master item, then the same aisle and then the same zone.
Try last used location, aisle, zone for inventory level 1,2
When assigning locations to inventory, give priority to the last location used for inventory level 1,2, then the same aisle and then the same zone.
Try last used location, aisle, zone for inventory level 1,2,3
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3, then the same aisle and then the same zone.
Try last used location, aisle, zone for inventory level 1,2,3,4
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4, then the same aisle and then the same zone.
Try last used location, aisle, zone for the receipt
When assigning locations to inventory, give priority to the last location used for the receipt, then the same aisle and then the same zone.
calculate capacity by lowest SKU class When calculating capacity by cube, use lowest SKU class and do not round up. For example, if there are 10 cases in a pallet and a given location contains 22 cases, the quantity in the location will be 
2 pallets and 2 cases.
calculate capacity by highest SKU class
When calculating capacity by cube, round up the quantity to the highest SKU. For example, if a given location contains 2.1 pallets, the quantity will be rounded up to 3 full pallets.
NOTE Each pallet consists of a single inventory entity. If there are two lots or pallet ID’s in the same location, each lot or pallet ID will be rounded up separately.

BREAK INVENTORY INTO MULTIPLE TO LOCATIONS GROUP (I7500)
This parameter allows you to specify whether or not allocation should split a receipt line (for directed putaway) or a location line (for directed move) into multiple to locations.
CAPACITY GROUP (I8000)
This parameter looks at the total put-away quantity of a receipt line and compares it to the location’s available capacity. For example, you have a receipt line of 14 pallets and you want allocation to select a location that can hold all 14 pallets.
Allow inventory to break into multiple to locations
Ignore the fact that the quantity to be put-away or moved may have to be split into multiple to locations.
NOTE
If the inventory that you are putting away or moving is on a hold whose Breakable Inventory flag set to N for No, allocation will ignore the option that you select in the “Allow inventory to break into multiple to locations” group. It will treat the inventory as nonbreakable and search for a location in which the entire quantity can be put-away or moved without splitting it into multiple location lines.
Disallow the breaking of inventory into multiple to locations
Place product on a location only if the entire quantity can be putaway or moved without splitting the product into multiple location lines.
For example, if the quantity to be put-away or moved is 200 cases, allocation will search for a location in which the entire 200 cases can be put-away or moved. It will not allow the 200 cases to be split into two or more location lines. 
put-away to any location that has the capacity
Place product in a location if there is any available capacity at all. 
For example, the receipt line is 10 pallets and a given location has an available capacity of 2 cases, allocation will assign two cases to this location and then look for other locations for the remaining pallets and cases.
put-away to location with matching capacity
Place product in a location only if the total put-away quantity is an exact match of the location’s available capacity.
put-away to location with matching or more capacity
Place product in a location only if the total put-away quantity is less than or equal to the location’s available capacity.
put-away to location with matching or less capacity
Place product in a location only if the total put-away quantity is greater than or equal to the location’s available capacity.
put-away to location starting with the highest capacity
Place product in a location starting with the locations with the highest available capacity.
put-away to location starting with lowest capacityPlace product in a location starting with the locations with the lowest available capacity.

LOCATION HEIGHT GROUP (I8200)
ORDER BY GROUP (I8300)
This group allows you to define the sort sequence for your last used locations/aisle/zone so that closer locations are tried first followed by less close locations.
Ignore location height Do not use location height for determining a put-away location.
Use location height, ascending order Place product in a location with the lowest possible height that is still high enough to hold the product.
Use location height, descending order Place product in a location with the highest possible height as long as it is high enough to hold the product.
Order by Warehouse Code, Location 
Code
The default sort order in AccellosOne 3PL: warehouse code followed by location code.
Order by LOCA Put Sequence Number, 
Warehouse Code, Location Code
Sort by put-away/directed move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Warehouse Attribute Proximity Sequence, Warehouse Code, Location CodeSort by proximity sequence number in WARE, then warehouse code followed by location code.
Order by Warehouse Attribute Proximity Sequence, LOCA Put Sequence 
Number, Warehouse Code, Location 
Code
Sort by proximity sequence number in WARE, then put-away/ directed move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Location Cube Ascending, 
Warehouse Code, Location Code
Sort by location with the smallest cube, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Code, Location Code
Sort by location with the largest cube, then warehouse code followed by location code.
Order by Location Cube Ascending, 
LOCA Put-Away Sequence Number, 
Warehouse Code, Location Code
Sort by location with the smallest cube, then put-away/directed move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Location Cube Descending, 
LOCA Put- Away Sequence Number, 
Warehouse Code, Location Code
Sort by location with the largest cube, then put-away/directed move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Location Cube Ascending, 
Warehouse Attribute Proximity 
Sequence, Warehouse Code, Location 
Code
Sort by location with the smallest cube, then proximity sequence number in WARE, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Attribute Proximity 
Sequence, Warehouse Code, Location 
Code
Sort by location with the largest cube, then proximity sequence number in WARE, then warehouse code followed by location code.

PRODUCT STACKING GROUP (I8400)
The options in this group allow you to define your product stacking rules. 
You define your stacking rules in ITEM by entering your stackability factor in the Stackability Quantity in 
Highest SKU field. In this field, you define how many layers of the highest SKU code can be stacked up.
For put-away purposes, the stackability factor will be applied to the location capacity. For example, if the location capacity is defined as four pallets and the item code has a stackability factor of 2, then the put-away/ directed move engine will consider 8 pallets as the location capacity for this item code. 
Order by Location Cube Ascending, 
Warehouse Attribute Proximity 
Sequence, LOCA Put- Away Sequence 
Number, Warehouse Code, Location 
Code
Sort by location with the smallest cube, then proximity sequence number in WARE, then put-away/directed move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Attribute Proximity 
Sequence, LOCA Put-Away Sequence 
Number, Warehouse Code, Location 
Code
Sort by location with the largest cube, then proximity sequence number in WARE, then put-away/directed move sort sequence number in LOCA, then warehouse code followed by location code.
Do not stack product Do not allow product stacking.
Stack product according to largest 
ITEM stackable setting
If a location contains multiple items, stack product according to the stackability settings of the largest item.
Stack product according to smallest 
ITEM stackable setting
If a location contains multiple items, stack product according to the stackability settings of the smallest item.

ITEM screen showing stackability factor field
PND LOCATION CAPACITY GROUP (I8700)
This group allows you to skip the final location if the associated PND does not have capacity.
PIIT LOCATION CAPACITY GROUP (I8500)
This group allows you to specify rules for putting away product into pick line locations if and when there is capacity for receiving new product. The rules apply to fixed position pick line locations only.
NOTE: The PIIT Location Capacity group looks at the available capacity in the location only. Unlike replenishment, it does not check whether the location’s minimum quantity has been reached.
Ignore PND location capacity Do not check the capacity of the PND location.
Skip final location if associated PND does not have capacity
In three-step put-away, if the PND location is full, do not consider any final put-away locations attached to that PND location.
Do not give priority to PIIT locations No priority will be given to pick line locations.
Give priority to PIIT locations, no need to check FIFO
Priority will be given to pick line locations and FIFO/LIFO rules will be ignored.
Give priority to PIIT locations, validate 
FIFO (DSRP, ITEM) requirements
Priority will be given to pick line locations and FIFO/LIFO rules will be followed.

ENTIRE DOCK QUANTITY GROUP (I8900)
This group allows you to consider the entire quantity for a given item on the dock when assigning put-away locations rather than the quantities of individual receipt lines. For example, you receive multiple receipts containing the same item or items at the same time and you wish to group your items on the receiving dock for more efficient put-away into a single large location if one is available.
Entire dock quantity receiving must be activated in FLPR by attaching the activity type 89 (Entire Dock 
Quantity Directed Move Inbound) to the appropriate inbound flow. Only receipts at this flow can be grouped for entire dock receiving purposes.
FLPR screen showing activity type 89 assigned to inbound flow INST (Inbound Staged)
In the Sequence Block of ITEM in the Entire Dock Quantity field, you specify the maximum number of pallets that can be grouped together for entire dock receiving purposes. For example, if you set this maximum to 20 pallets for your first ILOP sequence and there are 25 pallets of item A on the dock at your entire dock receiving flow, the ILOP sequence will fail and directed put-away will attempt to put-away using your second 
ILOP sequence.

ILOP screen showing a maximum quantity of 20 pallets

### FIELD DESCRIPTIONS (ILOP) <a id="field-descriptions-ilop"></a>

Ignore Entire Dock Quantity Directed 
Move Inbound
Do not use the entire dock quantity of an item for determining a put-away location.
Match Entire Dock Quantity against location capacity and go up
Place entire dock quantity product in a location with available capacity or greater.
Match Entire Dock Quantity against location capacity and go down
Place entire dock quantity product in a location with available capacity or less.
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each sequence as well as the put-away options for that sequence.

Description Mandatory
Your item location profile code description.
Isolator Code (ISOL) Mandatory
The default isolator zone attached to the profile. You can override this default in the Sequence Block.
Overflow Warehouse 
Code (WARE)
Mandatory
If you have set up an overflow warehouse in WARE, you enter its code in this field. If you have not set up an overflow warehouse, enter your main warehouse code.
Overflow Location Code (LOCA)
Mandatory
The overflow location in the warehouse that you specified in the previous field. 
You can specify a location such as an aisle, dock space, etc. or you can set up a dummy location called 99999 or ASKSUP in LOCA and use this for all your 
ILOP profiles.
SEQUENCE BLOCK
Sequence Number Mandatory
1, 2, 3, 4, etc.
Each sequence or pass contains the parameters that you specify for selecting a location. The sequence numbers that you enter in this field determine the order in which sequences are run.
Description Mandatory
Your sequence number description.
FIELD DESCRIPTIONS

Warehouse Code Optional
If you specify one or more warehouses in this field, the system will restrict its search for a location to the warehouse(s) that you specify. If you leave this field blank, the system will search all warehouses.
If required, each sequence can have a different warehouse. For example, sequence 1 could search for locations in warehouse 1, sequence 2 could search for locations in warehouse 2, sequence 3 could have no warehouse assigned, etc.
You can use the following symbols (=, <, >, etc.) to define one or more warehouses:
=1
1-2
>2
<5
1-3,=7
Any warehouse beginning with the number 1
Warehouses 1 through 2
Warehouses greater than or equal to 2
Warehouses less than or equal to 5
Warehouses 1 through 3 plus Warehouse 7
Location Code Optional
If you specify one or more locations in this field, the system will restrict its search for a location to the location(s) you specify. If you leave this field blank, the system will search all locations.
You can use the following symbols (=, <, >, etc.) to define one or more locations:
=100
100-200
>200
<500
100-300,=700
A100-E999
Any location beginning with 100 
Locations 100 through 200
Locations greater than or equal to 200
Locations less than or equal to 500
Locations 100 through 300 + 700
Aisles A through E
This field allows you to temporarily restrict put-away to certain locations or aisles when you are reracking your warehouse.
Acceptable Gap Height / 
UOM
The Acceptable Gap Height and UOM fields represent the gap between the product height and location height. If the gap between the product height and the location height for a given location exceeds the acceptable gap, that location will be rejected as a suitable put-away location.
SEQUENCE BLOCK

### SETTING UP A NEW PROFILE IN ILOP FOR DIRECTED PUT-AWAY <a id="setting-up-a-new-profile-in-ilop-for-directed-put-away"></a>

If you are setting up allocation for non-RF programs, you select your put-away parameters from the Put-Away option in the Type Block. If you are setting up allocation for RF programs such as RFCH/RFPU, refer to the 
RF Guide to find out which put-away parameters to use.
1 Enter ILOP.
2 Click on Create Record.
3 Key in an item location profile code and press Enter.
4 Key in a meaningful description for your new code and press Enter.
5 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
6 Use your pick list function to select the warehouse code for your overflow warehouse. If you have a single warehouse, use this warehouse.
Quantity Range The Quantity Range field defines an acceptable quantity range between the putaway quantity and the location capacity. The unit of measure is the SKU code entered in the Capacity SKU Code field in LOCA. This field works in conjunction with the I8000 series of options (“Put-away to any location that has capacity”). 
EXAMPLE 1
Suppose you enter 4 in the Quantity Range field and select I8020 (“Put-away to any location with matching or more capacity”). If you are putting 1 pallet of product away, the put-away/directed move engine would look for locations with a capacity starting with 1 and moving up to 5 (i.e. 1 + 4 = 5). 
EXAMPLE 2
Suppose you enter 2 in the Quantity Range field and select I8030 (“Put-away to any location with matching or less capacity”). If you are putting 6 pallets of product away, the put-away/directed move engine would look for locations with a capacity starting with 6 and moving down to 4 (i.e. 6 - 2 = 4).
Hours See [Opportunistic Cross-Docking](pick-lines-replenishment.html#opportunistic-cross-docking) for further information.
Entire Dock Quantity See “Entire Dock Quantity Group (I8900)” (ver [Standard Logical Groups for Put-Away](alocacao.html#standard-logical-groups-for-put-away)) for further information..
Isolator Code If you specify an isolator code in this field, it will override the isolator code in the header record.
SEQUENCE BLOCK

7 Use your pick list function to select the location code for your overflow location code.
The Type Block will appear. 
Blank Put-Away screen
8 Do one of the following:
9 Click on Sequence Block.
10 When the Selected Options Block appears, key in 1 for your first sequence and press Enter.
11 Key in a description for your first sequence (for example, FIRST PASS) and press Enter.
12 If you wish to restrict the search for locations in this sequence to a particular warehouse, key in the warehouse code and press Enter. If you want to search locations in all warehouses, press Enter to bypass this field.
TIP Create a location code in LOCA of 999 or ZZZZZZ and use this as your overflow location (the format of this code must conform to the format that you set up for this warehouse in WARE). When the system starts allocating to this location, you know that your warehouse is full.
If you are setting up allocation for non-RF programs:
If you are setting up allocation for RF programs:
a) Use your arrow keys to select the 
Put-Away option in the Type 
Block.
a) Refer to the RF Guide to find out which option — Put-Away or 
Directed Move Inbound — to select in the Type Block.

13 If you wish to restrict the search for locations in this sequence to particular locations or a range of locations, key in the location codes and press Enter. If you want to search all locations in this sequence, press Enter to bypass this field.
You will see the first set of parameters appear in the Available Options Block.
14 If required, enter your acceptable gap height and press Enter. Then key in your UOM and press Enter again.
15 If required, enter your quantity range and press Enter.
16 If you wish to override the isolator code in the header for a given sequence, key in your override isolator code and press Enter. If you do not wish to override the isolator code in the header, press Enter to bypass this field.
17 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you wish to choose and then click on Select Option. If you do not wish to use a particular group (for example, the Hold code group), select the first option in the group (“Ignore hold codes in location”) to deactivate the group.
18 Repeat the previous step for each set of parameters.
19 When you finish entering all your parameters for your first sequence, your cursor will be positioned over the last line in the Selected Options Block. Click on Sequence Block.

Sample Put-Away screen after entering sequence 1
20 Repeat steps 10 to 19 for each additional sequence that you wish to set up for your put-away profile.
21 When you finish entering all your sequences, click on Return to Main and then Type Block.
22 Click on Master Block.

Item Location Profile
23 Click on Exit to exit the program.

### OVERRIDING THE ILOP PROFILE FOR INDIVIDUAL RECEIPT LINES IN ENRE <a id="overriding-the-ilop-profile-for-individual-receipt-lines-in-enre"></a>

The operator can override the ILOP profile for an individual receipt line in ENRE. This functionality is available in both ENRE and EDI receipts.

ENRE screen showing Location Profile Code field
If there are multiple ILOP profiles that apply to a given receipt line, AccellosOne 3PL will use the following override sequence:
 item in ITEM (default and lowest priority)
 shipper (SHIP)
 velocity (IVLP)
 receipt line in ENRE (highest and to be used first when it exists)

### ATTACHING A VELOCITY CODE TO THE ILOP PROFILE <a id="attaching-a-velocity-code-to-the-ilop-profile"></a>

You can assign velocity codes to item location profile codes (ILOP) to indicate whether a particular item is fast moving or slow moving. For example, you assign the fast moving velocity code to the ILOP profile ABC and the slow moving velocity code to the ILOP profile DEF. You then attach your velocity codes to the appropriate items in ITEM.
The purpose of velocity codes is to handle seasonal product whose velocity may change depending on the time of year. For example, turkey is a fast-moving product at Thanksgiving and a slow-moving product at other times of the year.
Rather than enter the ITEM program and change the ILOP profile for dozens or more items, the system administrator can enter IVLP and change the ILOP profile once for all items assigned that velocity.

1 Enter IVLP.
2 Click on New.
3 Select your velocity code from the dropdown list.
4 Use your pick list to select the appropriate item location profile.
5 Repeat the above three steps for each additional velocity code that you wish to assign to an item location profile.
IVLP screen showing velocity codes assigned to ILOP profiles
FIELD DESCRIPTIONS
Velocity Code Mandatory
Your velocity code. You set up your velocity codes in VELO (Velocity Codes).
Item Location Profile (ILOP)
Mandatory
The ILOP profile being assigned a velocity. This profile will override the ILOP profile attached directly to the item.

6 When you finish assigning velocity codes to item location profiles, click on Save to your changes.
7 Click on Exit to exit IVLP.

### Item Receipt Hold Profile Code (IRHP) <a id="item-receipt-hold-profile-code-irhp"></a>

In this program, you set up your item receipt hold profile codes. These profile codes allow you to put away product based on its hold code. When you receive an item with a hold code attached to it and that hold code matches the hold code that you specify in IRHP, the system will put-away that item in the location assigned to it in IRHP and bypass normal ILOP processing.
You can attach as many items as you wish to the same receipt hold profile code, but you can only assign a single location to any given item/hold code combination. For example, you can assign one location to ITEM 1 
/ HOLD CODE A and another location to ITEM 1 / HOLD CODE B, but you cannot assign two locations to the same item/hold code combination.
IRHP is attached to PUPR (Put-Away Profile Code).
FIELD DESCRIPTIONS
Item Receipt Profile Code Mandatory
Your item receipt hold profile code.
Description Mandatory
Your item receipt hold profile description.
Customer Code (defined in CUST)
Mandatory
The customer code for the item.
Item Code (defined in ITEM)
Mandatory
Your item code or .ALL for all items belonging to a given customer.
Hold Code (defined in HOLD)
Mandatory
Your hold code.

1 Enter IRHP.
2 Key in an item receipt hold profile code and press Enter.
3 Key a description for your new item receipt hold profile code and press Enter.
4 Key in your customer code and press Enter.
5 Key in your item code and press Enter.
6 Key in your hold code and press Enter.
7 Key in your warehouse code and press Enter.
8 Key in your location code and press Enter.

Item Receipt Hold Profile Code showing item A1 with hold QC to be put-away to location A100 and the same item with hold BL assigned to location A103
9 Repeat steps 4 to 8 for each additional item that you wish to add to IRHP.
10 When you finish adding your items to the profile, click on Return to Main to exit create mode. Then click on Master Block and Exit to exit.
Warehouse Code (defined in WARE)
Mandatory
The warehouse in which you wish to put-away the item.
Location Code (defined in LOCA)
Mandatory
The location in which you wish to put-away the item.
FIELD DESCRIPTIONS

### Put-Away Profile Code (PUPR) <a id="put-away-profile-code-pupr"></a>

In this program, you set up your pick line options for directed put-away and specify whether product with a hold attached to it should be diverted to a special location reserved for the hold.
You can specify that product is to be always put-away to the pick line or that only partial quantities are putaway to the pick line. If you select either of these options, the allocation routine will search for pick line locations that satisfy the sequences that you set up in ILOP (Put-Away). If this search fails, the allocation routine will search for pick line overflow locations that satisfy your ILOP (Put-Away) sequences. If this search fails, the allocation routine will search for non-pick line locations that satisfy your ILOP (Put-Away) 
sequences.
If you specify an item receipt hold profile, product with a hold attached to it will be put-away to the location assigned to that hold in IRHP instead of to the pick line. 
PUPR is attached to DSRP (Depositor Shipping and Receiving Profile). If you attach a PUPR profile to ITEM, that profile will override the customer-level default in DSRP.
FIELD DESCRIPTIONS
Put-Away Profile Code Mandatory
Your put-away profile code.
Description Mandatory
Your put-away profile description.
Put-Away to Pick Line A = Always
P = Partial
N = None
See [Putting Away to a Pick Line Using Directed Put-Away](pick-lines-replenishment.html#putting-away-to-a-pick-line-using-directed-put-away) for further information..
Pick Line Isolator Code (ISOL)
Optional
See [Putting Away to a Pick Line Using Directed Put-Away](pick-lines-replenishment.html#putting-away-to-a-pick-line-using-directed-put-away) for further information..

Range in Days from Oldest Lot
Optional
This range in days applies to those options in the Partially Filled Locations group in ILOP that contain a “match PUPR date range” restriction. For example, if you select “Partial locations, at least same level 1 and match PUPR date range”, directed put-away will only select a location if both the inventory level requirements (“same level 1”) and the PUPR date range requirements are satisfied.
Range Based on Only available if the Range in Days from Oldest Lot field is populated
EXDT = Expiry Date
EXMO = Expiry Date Within 1 Month
RCDT = Receipt Date
The type of date that your range in days is based on.
Sort Sequence Code (SOSE)
Optional
This field allows you to specify how you want the allocation routine to resolve tie-breaking situations. For example, suppose you specify the following three put-away parameters in ILOP:
 use only exact match isolator code
 use only empty location
 fill location to maximum capacity
When you run allocation, the system finds three locations that meet the above criteria: A2, C6 and F4. A sort sequence code allows you to specify which of these three locations you wish to pick from. You set up sort sequence codes in 
SOSE in the form of SQL order by statements.
If you do not specify a sort sequence code for your picking profile, the allocation routine will select the “lowest” location — in the example above, A2.
FIELD DESCRIPTIONS

1 Enter PUPR.
2 Click on Create Record.
3 Key in your put-away profile code and press Enter.
4 Key in a description for your new put-away profile code and press Enter.
5 In the Put-Away to Pick Line field, press Enter to accept the default value of N for None.
6 If required, key in an isolator profile code and press Enter or press Enter with the field blank to bypass this option.
7 If required, key in a range in days from oldest lot value and then select the appropriate range based on code: EXDT for Expiry Date, EXMO for Expiry Date Within 1 Month or RCDT for Receipt Date.
8 If required, key in a sort sequence code and press Enter or press Enter with the field blank to bypass this option.
9 If required, key in an item receipt hold profile code and press Enter or press Enter with the field blank to bypass this option.
10 If you entered an item receipt hold profile code in the previous field, key in the appropriate override option (Y for Yes or N for No) and press Enter.
Item Receipt Hold Profile 
Code (IRHP)
Optional
If you enter an item receipt hold profile code, the system will check each receipt line for a hold code. If the receipt line has a hold code and if the receipt line hold code matches a hold code in IRHP, the system will attempt to putaway the receipt line in the location assigned that hold in IRHP.
This field overrides the pick line options that you specify in the Put-Away to 
Pick Line field.
Item Receipt Hold Override
Only available if you enter an item receipt hold profile code
Y = Yes
N = No
This field governs the way in which the system will put-away product with a hold that cannot be put-away in the location specified in IRHP. If you select Y for Yes, the system will allocate the item to the overflow locations that you specify in ILOP. If you select N for No, the item will undergo normal ILOP processing and will be assigned a location by that program.
FIELD DESCRIPTIONS

PUPR screen showing put-away profile P1 that will put-away product according to the location and hold code defined in IRHP
11 When you finish setting up your put-away profile code, click on Return to Main and then Exit to exit.

### Activating Directed Put-Away <a id="activating-directed-put-away"></a>

Four conditions must be met before directed put-away is activated:
 the Assign Location flag must be set to Yes for an inbound flow code in DIFP
 an inbound document must be set up to print in DIFP (unless you put-away using an RF program)
 the Activate Directed Put-Away flag in the Company Parameters Block of COMP must be set to Yes
 your put-away locations must be assigned a location type in LOTP whose Directed Put-Away flag has been set to Yes

### Deactivating Directed Put-Away for Selected Receipts <a id="deactivating-directed-put-away-for-selected-receipts"></a>

You can deactivate directed put-away for selected receipts by means of the special verify program SSDP (Skip Directed Put-Away). Deactivating directed put-away for selected receipts is useful when some products in your warehouse require special handling before final put-away. 

For example, suppose certain items require blast freezing before putting away to the normal freezer storage area of your warehouse. You would deactivate directed put-away for these items and place them directly in the blast freezing locations. Once blast freezing was complete, you could move them manually to the normal freezer storage area or you could perform a directed move.

### SETTING UP DIRECTED PUT-AWAY DEACTIVATION <a id="setting-up-directed-put-away-deactivation"></a>

You set up directed put-away deactivation by attaching the specify verify program SSDP to the flow before directed put-away is called in your inbound workflow profile.
1 Enter DIFP.
2 Retrieve the workflow profile code that you wish to set up.
3 Click on In/Out/Repi/Relo Block.
4 Click on Flow Block.
5 Use the arrow keys to position your cursor over the flow before directed put-away is called.
6 Click on Document Block then click on Special Verify Block.

DIFP screen
7 Click on Create Record.
8 Key in your sequence number (for example, 1) and press Enter.
9 Key in SSDP and press Enter.
10 In the Complete field, key in N for No and press Enter.
11 In the Sequence field, key in B for Before and press Enter.
12 In the Display field, key in Y for Yes and press Enter.

DIFP screen showing specify verify SSDP attached to the flow STUN
13 Click on Return to Main to exit create record mode.
14 Press F4 the required number of times to exit DIFP.
PROCESSING RECEIPTS WITH DIRECTED PUT-AWAY DEACTIVATION TURNED 
ON
You have three options when processing receipts:
 you can skip all lines on a receipt (that is, bypass directed put-away for all lines)
 you can skip some lines on a receipt and not skip others
 you can perform no skipping (that is, perform directed put-away for all receipt lines)
1 Enter your receipt in ENRE in the normal manner.
2 Advance the flow of the receipt in CHRF and print any required receipt documents.
3 When you reach the flow to which you attached the specify verify program SSDP, the following screen will appear.
NOTE When putting away a load in RFPU containing mixed lines (that is, some lines were skipped while others were put-away using directed put-away), skipped lines may show a system-assigned location. If this happens, exit RFPU and then reenter the program. The Location field will now be blank for all skipped lines.

CHRF screen showing receipt with three lines
4 Do one of the following:

CHRF screen showing two lines to be skipped
5 Continue to process the receipt normally in CHRF.
To skip all lines: To skip individual lines:
To perform no skipping (that is, put-away all lines):
a) Click on Skip All. a) Key in Y for Yes for each line that you wish to skip and press Enter. If you enter N for 
No or leave the field blank, the line will NOT be skipped.
b) When you finish skipping individual lines, click on Exit.
a) Click on Exit.

### LOOKING UP SKIPPED RECEIPT LINES IN LORE <a id="looking-up-skipped-receipt-lines-in-lore"></a>

A record is created in the Time Stamping Block of LORE whenever you skip a receipt line in CHRF. The record is attached to the flow before your SSDP special verify program.
If you skip individual lines in CHRF, a record will be created for each line skipped; for example, “Driver at Door 
# 1”, “Driver at Door # 2”, etc. If you skip all lines in CHRF, a single record will be created in the Time 
Stamping Block with a line number of zero; for example, “Driver at Door # 0”.
1 Enter LORE.
2 Retrieve the receipt that you wish to look up.
3 Click on Time Block.

LORE screen showing two skipped lines on receipt 1459 (lines 1 and 3)
4 If required, use your arrow keys to scroll through the records in the Time Stamping Block.
5 When you finish looking up your receipt, click on Master Block and Exit to exit.

### Put-Away by Warehouse Zone <a id="put-away-by-warehouse-zone"></a>

There are three setup programs for put-away by warehouse zone: WHZO, ITEM and ILOP. 

### WHZO (WAREHOUSE ZONE CODES) <a id="whzo-warehouse-zone-codes"></a>

If product cannot be put-away in a given warehouse zone, you can define an overflow sequence for warehouse zones in the Overflow Sequence Block. The overflow zones must have the same zone type code as the header zone.
Warehouse zones used in directed put-away require a zone type code of D (for Directed Put-Away).

WHZO screen showing overflow zone codes

### ITEM (ITEM CODE) <a id="item-item-code"></a>

The Zone Code field in ITEM defines the exact match zone code for an item. You can override this exact match warehouse zone for a given item by entering records in the Override ISOL Zone Block. In this block, you define specific warehouse zones for specific isolator codes and hold codes.
For example, if product is on QA hold, it is directed to locations in warehouse zone TDRY assigned the isolator code DRY.
ITEM screen showing Override Block

### ZONE CODE GROUP (ILOP) <a id="zone-code-group-ilop"></a>

The following options in the zone code group allow you to define your zone code rules in the same way that you define your isolator rules.
 Ignore zone codes
 Use only exact match zone code
 Use first overflow zone code
 Use first & second overflow zone code
 Use first & second and third overflow zone code
 Use any overflow zone code
ILOP screen showing zone code group

### Put-Away by Location Size <a id="put-away-by-location-size"></a>

You can put-away by location size when you receive pallets whose size (that is, the number of cases on the pallet) is unknown. You use location size codes to define the relative size of a location (large, medium, small, etc.). When you receive product, you attach the appropriate location size code to each location line in ENRE. 
During directed put-away, AccellosOne 3PL will attempt to place the product in a location whose location size code matches the location size code assigned to the receipt line.
You can define overflow sequences for your location size codes. If AccellosOne 3PL is unable to find a location whose location size code is an exact match of the product’s location size code, it will search for locations assigned the location size code or codes specified as overflow sizes. 

Location sizes must be activated on your system by HighJump and require setup of the appropriate put-away parameter in ILOP (Item Location Profile).

### SETUP IN LOCS <a id="setup-in-locs"></a>

You set up your location size codes in LOCS.
1 Enter LOCS.
2 Click on Enter Criteria then Execute Query to see which location size codes have been already set up. 
3 If you need to set up another code, click on Create Record.
4 Key in your location size code and press Enter.
5 Key in a description for your code and press Enter.
FIELD DESCRIPTIONS
Location Size Code Mandatory
Your location size code. 
Description Mandatory
Your location size description.
Overflow Sequence Number
Optional
The sequence number for your overflow location size code.
Overflow Location Size 
Code
The overflow location size code for the sequence number that you entered in the Overflow Sequence Number field.
If you wish to set up an overflow location size code for your new code:
If you do NOT wish to set up an overflow location size code for your new code:
a) Key in a sequence number and press Enter.
b) Key in a location size code for the sequence and press Enter.
c) Repeat the above steps for each additional sequence that you wish to set up.
d) Click on Master Block.
a) Click on Master Block.

LOCS screen showing two overflow location sizes for Small locations
6 If you wish to create another location size code, click on Create Record and repeat the above steps for each additional code that you wish to add. When you finish adding all your codes, click on Return to Main to exit create record mode.
7 When you finish creating your location size codes, click on Exit to exit the program.

### SETUP IN LOCA <a id="setup-in-loca"></a>

Your location size codes set up in LOCS must be attached to the appropriate locations in LOCA.

### SETUP IN ILOP <a id="setup-in-ilop"></a>

See “Location size group (I4500)” (ver [Standard Logical Groups for Put-Away](alocacao.html#standard-logical-groups-for-put-away)).

### Sort Sequences and Proximity Logic for Last Location Used Group <a id="sort-sequences-and-proximity-logic-for-last-location-used-group"></a>

If you put-away by last location used (ILOP) for a given level 1/level 2, you can extend the last location used logic to include the last bay used and then the last aisle used. For example, try the last location used first; if that location is full, try locations in the last bay used. If no location in the last bay used is available, try locations in the last aisle used.
When searching for locations in the last bay used and the last aisle used, you can define specific sort sequences for these locations so that the RF operator will try closer locations first and then try locations that are further and further away from the last location used. Ideally, you wish to put-away product in the last location used for that item/level 1/level 2. However, if that is not possible, you wish to put-away in the same bay, aisle and warehouse zone.

### LOCA (LOCATIONS) <a id="loca-locations"></a>

The Put-Away/Directed Move Sort Sequence field allows you to maintain specific sort sequences for putaway and directed move sorting. These sort sequences offer greater flexibility than the default alphanumeric sort sequence by location code. The Put-Away Directed Move Sort Sequence field is referenced in those options in the Order By group in ILOP that contain the LOCA Put-Away Sequence Number. 

For example, suppose you select “Order by LOCA Put-Away Sequence Number, Warehouse Code, Location 
Code” in ILOP and you have three locations: 
 A100 (sequence number = 2) 
 B100 (sequence number = 3) 
 C100 (sequence number = 1)
Allocation will attempt to put-away to location C100 first, then location A100 and last location B100. 
LOCA screen showing location A100 assigned a sequence number of 10

### WARE (WAREHOUSE AND LOCATION FORMAT) <a id="ware-warehouse-and-location-format"></a>

The Proximity Sequence # field and the Exclude/Include flag in the Location Attribute Block allow you to define how close any given location is to the last location used for put-away (ILOP options 6010 to 6095). 
Proximity logic is only activated if you select an option in the Order By group in ILOP containing the parameter 
Warehouse Attribute Proximity Sequence. For example, “Order by Location Cube Ascending, Warehouse 
Attribute Proximity Sequence, Warehouse Code, Location Code”.
FIRST PASS: PROXIMITY SEQUENCE NUMBER = 1 FOR BAY
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Exclude FA105, FA205, FA305, … FAX05, FAY05, FAZ05, etc.
DESCRIPTION: In the first pass, directed put-away searches for locations whose first two characters are “FA” (aisle) and last two characters are “05” (slot). The third character (bay) can be any character; that is, search for any bay in the current aisle and current slot.

WARE screen showing Location Attributes Block

### Item Put-Away Parameters (IPUP) <a id="item-put-away-parameters-ipup"></a>

This program is a simplified version of ITEM. It allows you to update the following for a given customer/item without entering ITEM:
SECOND PASS: PROXIMITY SEQUENCE NUMBER = 2 FOR SLOT
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Exclude FA105, FA205, FA305, … FAX05, FAY05, FAZ05, etc.
DESCRIPTION: In the second pass, directed put-away searches for locations whose first two characters are “FA” (aisle) and third character is “0” (bay). The last two characters (slot) can be any character; that is, search for any slot in the current aisle and bay.
THIRD PASS: PROXIMITY SEQUENCE NUMBER = 3 FOR AISLE
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Include FA000, FA001 ... FA101, FA102 ... FA971 … FA9A0 
… FA9X4 … FAC00, FAC01 … FAH77, FAH78 … 
FAZZ1 … FAZZZ, etc.
DESCRIPTION: In the third pass, directed put-away searches for locations whose first two characters are “FA” (aisle). The last three characters (bay and slot) can be any character; that is, search for any bay or slot in the current aisle.

 your put-away by warehouse zone rules
 your stackability rules for inbound put-away and outbound pallet building
In the Detail Block, you can define specific warehouse zones for specific isolator codes.
1 Enter IPUP.
2 Click on Enter Criteria.
3 Key in the customer code and item code that you wish to set up and click on Execute Query.
4 Press Enter twice to position your cursor in the Directed Put-Away Zone Code (WHZO) field.
5 Key in your put-away zone code and press Enter or select it from the pick list.
6 If you require stackability rules for outbound pallet building, select a stackability indicator code from the pick list.
7 In the Stackability Quantity in Highest SKU field, you define how many layers of the highest SKU code can be stacked up.
For put-away purposes, the stackability factor will be applied to the location capacity. For example, if the location capacity is defined as four pallets and the item code has a stackability factor of 2, then the putaway/directed move engine will consider 8 pallets as the location capacity for this item code. 
IPUP screen showing put-away setup
8 If you require specific warehouse zones for specific isolator codes, click in the Detail Block and then click on New. Then enter your isolator codes and the corresponding warehouse zone codes.
9 When you finish setting up your put-away parameters, click on Save to save your new record.
10 Click on Exit to exit IPUP.

### Put-Away by Pallet Type <a id="put-away-by-pallet-type"></a>

You can put-away product by pallet size or pallet type rather than SKU quantity, weight or cube. For example, you receive both standard four-foot pallets as well seven-foot pallets in your warehouse and you need a way to assign your different pallet types to a location with sufficient capacity.
In the program INAT (Inventory Attribute Factors), you define the number of standard pallet positions for each pallet type. For example, suppose a four-foot pallet has a factor of 1 and a seven-foot pallet has a factor of 2. 
This means that a four-foot pallet can be stored in location with a capacity of one or more pallets while a seven-foot pallet can only be stored in a location with a capacity of two or more pallets.
INAT screen showing 7-foot pallet with a location capacity standard factor of 2.00
The following setups are required for put-away by pallet type:
 in LOTP the Enable Pallet Attribute flag must be set to Yes for the appropriate location type(s)
 in COMP the Enable Pallet Attribute in LOTP flag must be set to Yes
 in IAPR you must create an inventory attribute profile code for pallet types
 in ITEM you must attached your IAPR profile for pallet types to the appropriate items
See the Operations 2 Guide for further information on inventory attributes.

## Outbound Allocation <a id="outbound-allocation"></a>

*Manual K — Allocation and Wave Manager*

Entering Orders With a Shelf Life Based on a Date Other Than the System 

### Understanding Allocation <a id="understanding-allocation"></a>

Outbound allocation is the process of selecting and assigning specific inventory to fill an order. It also involves selecting and assigning the specific location or locations from which the product is to be taken when filling the order. In other words, it prepares the information for the picking instructions.
In ENOR, there are two ways of performing allocation: 
 manually, in which you perform allocation yourself
 automatically, in which the system performs allocation

### MANUAL ALLOCATION <a id="manual-allocation"></a>

You must know all of the inventory levels in order to perform manual allocation. In the ENOR Line Block, you use an R (Regular) line type. Next you complete all of the Inventory Level fields, which selects and assigns specific product to the order line. 
If you also need to select the location from which the product is to be picked, you complete the Location Code field. Otherwise, you can leave the field blank for the system to choose the location through the allocation routine.

### AUTOMATIC ALLOCATION <a id="automatic-allocation"></a>

When you want the system to direct allocation, you use a P (Pending) line type in the Line Block and leave the Inventory Level 2 and higher inventory level fields blank. You also leave the Location Code field blank. 
Later, when you run the allocation routine, the system will automatically fill in these fields.
The allocation routine performs two functions:
 selects and assigns the inventory that is to be used when filling the order line. This is based on the parameters in the program Picking Profile (PIPR) and the setup in the program Depositor Shipping and 
Receiving (DSRP)
 selects and assigns the locations from which this product is to be picked according to the parameters that are set up in the program Item Location Profile (ILOP)

### SELECTION OF PRODUCT <a id="selection-of-product"></a>

The allocation routine follows preset rules (parameters) when selecting the specific inventory to use for this ordered item. For example, depending on whether the product has a LIFO or FIFO Picking Profile setup, the system will select the oldest or the newest inventory entity for dated product. 
LIFO is Last In and First Out meaning that the inventory that arrived at the warehouse last for this item must be shipped out first; FIFO is First In and First Out meaning that the inventory that arrived first to the warehouse for this item must be shipped out first.
Outbound Allocation = Selection of a specific product to fill an order
Selection of a specific location from which to pick the product
 +

### SELECTION OF LOCATION <a id="selection-of-location"></a>

When the selected product is stored in more than one location, the ILOP parameters direct the allocation routine to select the location that is preferable in terms of warehouse organizational priorities. For example, these could include picking first from a location to clean it out, picking first from an overflow location rather than from normal storage locations or picking first from locations that contain multiple Hold Code types rather than from locations that contain only one Hold Code type. 
The criteria for the parameters are set sequentially so that if the best option is not possible the system proceeds on the second best option and if the second option is not available it will proceed to the third best option, etc. until it finds a location.

### SHIPPING WITH INSUFFICIENT INVENTORY <a id="shipping-with-insufficient-inventory"></a>

An order may require more product than there is presently available in the warehouse. For example, suppose you need to ship twenty cases and there are only ten cases available as inventory. What happens next will depend on your system setup:
Setup 1
If your system is set up in DSRP so that the Change Zero Pending Line to R-Type Line flag is set to Yes and two lots were chosen during allocation, the system will generate two R type lines in the Line Block:
If one lot was chosen during allocation, the system will generate one R type line in the Line Block:
The order can be confirmed in CHOF or COOL so that you can ship out the portion that is available.
Setup 2
If your system is set up in DSRP so that it will not change the zero pending line to an r-type line, the system will generate one R type line and one P type line in the Line Block:
The order cannot be confirmed in CHOF or COOL. You will not be able to ship out any product until the missing product is received or the pending line is deleted.
Line 1 R Ordered Quantity = 10 cases
To Ship Quantity = 10 cases
Line 2 R Ordered Quantity = 10 cases
To Ship Quantity = 0 
Line 1 R Ordered Quantity = 20 cases
To Ship Quantity = 10 cases
Line 1 R Ordered Quantity = 10 cases
To Ship Quantity = 10 cases
Line 2 P Ordered Quantity = 10 cases
To Ship Quantity = 10 cases

### PRINTING YOUR PICK DOCUMENT <a id="printing-your-pick-document"></a>

If you used an R line type and you completed the Inventory Level 2 and higher fields as well as the Location 
Code field, you have performed allocation in ENOR. The data that you put into ENOR will be copied to the designated picking document as you print it. If you left the Location Code field blank, the allocation routine will select a location and it will populate this field accordingly as you print the designated picking document.
If you used a P line type, the system will perform allocation. Printing of the designated pick document will trigger the allocation routine to run. The allocation routine will select the entity and the location and it will enter the data into both ENOR and the designated picking document.
You complete the
Inventory Level 2 and higher fields in ENOR to select the specific product that you need.
You can complete the
Location Code field or you can leave it blank for the system to choose the location.
OUTBOUND
ALLOCATION
R (REGULAR)
LINE BLOCK TYPE
IN ENOR
P (PENDING)
LINE BLOCK TYPE
IN ENOR
 SELECTION OF
PRODUCT
 SELECTION OF
PRODUCT
SELECTION OF PICKING
LOCATION
SELECTION OF PICKING
LOCATION
Automatic
System-directed
Allocation
You leave the
Location Code field blank for the system to select.
You leave the
Inventory Level 2 and higher fields blank for the system to select.
PICKING
INSTRUCTIONS
PICKING
INSTRUCTIONS
You completed them in ENOR. They only need to be copied into the designated picking document when you print it.
The allocation routine will complete the instructions when you print the designated picking document.

### Setting Up Outbound Allocation <a id="setting-up-outbound-allocation"></a>

In AccellosOne 3PL, there are two programs used to set up directed picking: PIPR (Picking Profile) and ILOP (Item Location Profile). In PIPR you define the FIFO/LIFO sequence that you wish to use for the purpose of selecting a batch of inventory records. In ILOP you define location and capacity parameters that you want the system to use when selecting locations from the batch of records generated by PIPR.
Directed picking in AccellosOne 3PL

### Setting Up the Picking Profile (PIPR) <a id="setting-up-the-picking-profile-pipr"></a>

In this program, you define how product will be allocated to orders (if you use directed picking). In PIPR, you can specify:
 FIFO (First In First Out) or LIFO (Last In First Out)
 absolute FIFO/LIFO (that is, always pick from the oldest or newest lot, then the next oldest/newest lot, etc., and attach relatively less importance to location and capacity factors defined in ILOP) 
 relative FIFO/LIFO (that is, pick from a group of the oldest or newest lots and use location and capacity parameters defined in ILOP to make selections within this batch)
 the SKU class that you want the system to break at when picking partial quantities in ILOP
The picking profile that you define in PIPR can apply to all customers or to a particular customer. If required, it can apply to an item or series of items or it can apply to a consignee (that is all items being sent to a particular consignee).
If you are attaching picking profiles to items and consignees as well to customers, the following logic will apply:
 the profile that you attach to DSRP is the default
 if you attach a picking profile to ITEM, it will override the profile in DSRP
 if you attach a picking profile to CONS, it will override the profiles in DSRP and ITEM
 if you set up an item/consignee combination in CCOP, it will override the profiles in DSRP, ITEM and 
CONS (see [Setting Up Item-Specific Picking Profiles in CCOP](alocacao.html#setting-up-item-specific-picking-profiles-in-ccop) for further information)
 if you attach a picking profile set up in PIPR to a hold type in HOLD, any order lines placed on that hold type will be allocated according to the hold type’s picking profile (that is, the customer’s, item’s or consignee’s picking profile will be overridden by the hold type’s picking profile)

### CHANGING YOUR PICKING PROFILE <a id="changing-your-picking-profile"></a>

If you change your PIPR profile, the change takes effect immediately and applies to both existing orders as well as new orders. That is, PIPR settings are not saved when you create a new order. You can deallocate an existing order, change your PIPR profile and then re-allocate the order using your new picking rules.
ENOR PIPR ILOP

FIELD DESCRIPTIONS
Picking Profile Code Mandatory
Your picking profile code. For example, FIFO.
Description Mandatory
Your description.
Break Quantity at SKU 
Class (defined in SKCL)
Mandatory
In this field, you specify how you want the system to pick partial quantities — that is, whether or not to break a pallet or some other SKU type when an order requires a partial quantity. 
A partial quantity in AccellosOne 3PL is defined as a quantity that is less than a full SKU class and not the highest SKU class. For example, if you have a 
PALLETS/CASES account and your SKU classes are 1 for pallets and 3 for cases, then a partial quantity would be any number of cases not making up a full pallet.
EXAMPLE 1
Quantity Breakdown
Pallets
Cases
Eaches
SKU Class
1 (Pallets and the like)
2 (Cases and the like)
5 (eaches and the like)
If you specify the Break at SKU Class 1 option, the system will try to keep pallets together and will consider cases (SKU class 3) as the only valid SKU class for picking partials. If you specify the Break at SKU Class 3 option, the system will ignore pallets and try to keep cases together. Eaches or SKU class 
5 will be considered as the only valid SKU class for picking partials. 

EXAMPLE 2
If you specify “Ignore SKU Classes” in the above example, the system will ignore SKU classes during allocation and pick from any class (that is, break pallets, cases, etc. in order to fill the order). For example, if your quantity breakdown were 50 cases to a pallet, the following could occur during directed picking. If the order called for 60 cases, the system might pick 30 cases from two pallets (that is, breaking the two pallets) instead of picking one full pallet and one partial (10 cases).
The “Ignore” option is reserved for single-level accounts with no partials — for example, CASES only. You cannot use the “Ignore” option for:
 pick line items
 items whose ILOP profile contains any option in the Partial Quantity Group (for example, “pick partial from bulk”, “if picking from bulk and location has partial …”, etc.).
NOTE The system will override your break quantity at SKU class option if you select any “Pick to match” option in ILOP and a match is found.
Picking Based on FIFO/
LIFO
F = FIFO (First In First Out)
L = LIFO (Last In First Out)
FIFO/LIFO Based on EXDT = Expiry Date*
LEV2 = Inventory Level 2
LEV3 = Inventory Level 3
LEV4 = Inventory Level 4
RCDT = Receipt Date*
Defines what the FIFO/LIFO sequence is based on. If you select inventory level (for example, a lot number or date code), you may need to specify a selection formula (see next field).
The value that you enter in this field determines the sort order of inventory records in the Drill Block of LOEN.
* Sort order by date in the Drill Block of LOEN is only supported for all numeric dates 
such as 01.01.2005. If you use dates such as DEC-05 and FEB-05, records will be sorted in alphanumeric order: APR-05, DEC-05, FEB-05, etc.
FIELD DESCRIPTIONS

FIFO/LIFO Formula Optional
If you selected an inventory level in the previous field, you may require a formula to convert your inventory level values into a form that the system can use when it performs allocation. Consult your HighJump representative for the appropriate formula.
FIFO/LIFO Custom Program
Optional
This field is reserved for those cases when a special program — not merely a selection formula — is required to convert inventory levels. Must be set up by a HighJump consultant.
Picking Type A = Absolute
R = Relative
L = Location Sequence
If you select Absolute, the allocation routine will always pick the oldest product (if you are using FIFO) or the newest product (if you are using LIFO) regardless of location. The range in days fields are not available when absolute 
FIFO/LIFO is chosen.
If you select Relative, the allocation routine will pick from a batch of the oldest (or newest) lots and use location parameters defined in ILOP to make selections within this batch. With this option, you can select one or both of the following fields — Range in Days From Oldest Lot and/or the Minimum/
Maximum Range in Days to Expiry — to specify a range.
The Number of Inventory Records not to Exceed is a mandatory field for relative allocation. 
If you select Location Sequence, the available stock will be sorted by the 
FIFO/LIFO criteria defined in the following PIPR fields: Picking Based on 
FIFO/LIFO, FIFO/LIFO Based on and FIFO/LIFO Formula. Then the FIFO/
LIFO records will be sorted by location code sequence.
FIELD DESCRIPTIONS

For example, if FIFO/LIFO is based on receipt date (RCDT), inventory will allocated by receipt date then by location code. Likewise, if FIFO/LIFO is based on expiry date (EXDT), inventory will allocated by expiry date then by location code. And if FIFO/LIFO is based on an inventory level (LEV2, LEV3 or LEV4), inventory will be allocated by that inventory level value then by location code.
The following restrictions apply to allocation by absolute FIFO/LIFO then location code sequence:
 Your ILOP settings will not be checked.
 Your pick line settings will not be checked. All locations will be sorted by the location code and allocated accordingly.
 Full pallet or SKU class will not be checked. All stock will be sorted by FIFO/
LIFO criteria and location code only and allocated accordingly.
Range in Days from Oldest LotOnly available for relative picking.
In this field, you indicate to the allocation routine how many days from the oldest lot (or newest lot if you are using LIFO) it should look at — that is, how relative you want to pick. 
For example, if your oldest lot is dated June 1 and you enter 20 in this field, the system will look at all lots dated June 20 or older.
If you enter a small number in this field, the system will select a small number of lots and location will play a minor role in allocating product to orders. If you enter a large number in this field, the pick will be very relative — that is, the system will select a large number of lots to look at and location will play a major role in product allocation. 
FIELD DESCRIPTIONS system looks at all lots dated June 20 or later
April May June 1 20 July
Oldest lot dated June 1
Range in days from oldest lot set to 20

Range Based on Only available for relative picking. Mandatory if you are using a range in days field.
EXDT = Expiry Date
FIED = FIFO plus Expiry Date
FIRD = FIFO plus Receipt Date
RCDT = Receipt Date
SLPC = Shelf Life Percentage
If your FIFO or LIFO is based on the product’s receipt or expiry date, use 
EXDT or RCDT. If your FIFO or LIFO is based on a formula or custom program instead of your receipt or expiry date, select FIED or FIRD. 
Range in Days From Oldest Lot field
 if you select EXDT or FIED as your range based on value, the oldest/newest lot will be defined in terms of the expiry date
 if you select RCDT or FIRD as your range based on value, the oldest/newest lot will be defined in terms of the receipt date
Minimum/Maximum Range in Days to Expiry fields 
 if you select EXDT or FIED as your range based on value, the oldest/newest lot will be defined in terms of the expiry date
 if you select RCDT or FIRD as your range based on value, the oldest/newest lot will be defined in terms of the receipt date and AccellosOne 3PL will only pick product whose receipt date is newer than X days (that is, your range in days to expiry value) before the current system date
FIED and FIRD
These options use both the inventory level and receipt/expiry date to select the batch of inventory records. 
EXAMPLE
Suppose you set the Range in Days from Oldest Lot to 45 days and your oldest lot is dated February 1, 2000.
Lot
Level 2
Receipt Date
March 1, 2000
February 1, 2000
April 4, 2000
March 5, 2000
March 10, 2000
Days from Oldest Lot
FIELD DESCRIPTIONS

AccellosOne 3PL sorts all records in the batch by inventory level 2. Then it looks at the receipt date for each lot. When it reaches a lot with a receipt date that is out of range such as record 3 with a receipt date of April 4, it rejects that lot plus all subsequent lots such as lots 010 and 102. Only lots 001 and 002 will be included in the batch of eligible records.
Range in Days Starting 
From
Only available for relative picking
ARDT = To Arrive Date
ORDT = Order Date
SHDT = To Ship Date
SYDT = System Date (the date that the order is allocated)
The starting point for your range in days value. If you set the Range in Days to 
Expiry to 10 and select Order Date in this field, allocation will select product with a shelf life of at least 10 days as of the order date. If, on the other hand, you select To Arrive Date, allocation will select product with a shelf life of at least 10 days as of the to arrive date that you enter in ENOR.
If you leave this field blank, allocation will use SYSDT, the system default.
Number of Inventory 
Records not to Exceed
Mandatory for relative picking
In this field, you define the maximum number of inventory records that the allocation routine should process at a time. When you specify a maximum number of inventory records and a range in days from oldest lot or a range in days to expiry, the system will take the lessor of the two. 
EXAMPLE
You set the Range in Days From Oldest Lot field to 30 and this results in the selection of 15 inventory records. Then you set the Number of Inventory 
Records not to Exceed field to 20. The system will use the lessor value — 15 
— as the size of the batch. 
If you set this field to the maximum (99), your picking will be very relative; that is, the allocation routine will select records from many different lots and ILOP will make the final selection based on location. As a result, some older product may remain in your warehouse longer than desirable. 
If you set this field to a low value, your picking will be close to absolute FIFO/
LIFO and location factors defined in ILOP will play less of a role. Absolute or near absolute allocation can mean that you are taking less than full advantage of the system’s allocation capabilities. 
FIELD DESCRIPTIONS

Minimum Remaining 
Shelf Life Percentage
Only available if Range Based on = Shelf Life Percentage
See [Allocating by Shelf Life Percentage](alocacao.html#allocating-by-shelf-life-percentage) for further information..
Minimum / Maximum 
Range in Days to Expiry
Optional
You use these fields if you want to select product that will not expire until a certain date (that is, newer lots); this option is a way of guaranteeing a longer shelf life for the product that you pick. When you enter a positive number in one or both of these fields, the allocation routine counts forward from the current date to arrive at a date in the future. The system will then look at all product with expiry dates from the future date or later.
When you enter a negative value in one or more of these fields, your range will fall in the past.
EXAMPLE 1
Range Based on = Expiry Date
Range in Days Starting From = Order Date = June 1
Minimum Range in Days to Expiry = 10
Maximum Range in Days to Expiry = blank
FIELD DESCRIPTIONS

EXAMPLE 2
Range Based on = Expiry Date
Range in Days Starting From = Order Date
Minimum Range in Days to Expiry = 10
Maximum Range in Days to Expiry = 20
EXAMPLE 3
Range Based on = Expiry Date
Range in Days Starting From = System Date = June 25
Minimum Range in Days to Expiry = -10
Maximum Range in Days to Expiry = blank
NOTE An expiry date in AccellosOne 3PL need not be the date that product actually expires. It can be any date in your warehouse such as a production date or a packing date that you use to allocate product for an outbound order.
FIELD DESCRIPTIONS
June 1 = order date June 11 June 15 June 20 June 25 June 30 = expiry 
This product has a This product will ship shelf life less than the 
June 1 = order date June 11 June 15 June 21 June 25 June 30 = expiry 
This product has a This product will ship shelf life less than the 
This product has a shelf life greater than the maxiJune 1 June 10 June 15 = expiry June 20 June 25 = current June 30
This product has a shelf life less than This product will ship the minimum 

Sort Sequence Code (SOSE)
Optional
This field allows you to specify how you want the allocation routine to resolve tie-breaking situations. For example, suppose you specify the following three picking parameters in ILOP:
 use any isolator other than exact match or overflow 
 pick to match 
 ignore partials in bulk
When you run allocation, the system finds three locations that meet the above criteria: A2, C6 and F4. A sort sequence code allows you to specify which of these three locations you wish to pick from. You set up sort sequence codes in 
SOSE in the form of SQL order by statements.
If you do not specify a sort sequence code for your picking profile, the allocation routine will select the “lowest” location — in the example above, A2. 
Replenishment Message on Pick Documents
See [3 — Setting Up Your Picking Profile in PIPR](pick-lines-replenishment.html#3-setting-up-your-picking-profile-in-pipr) for further information.
Use FIFO/LIFO for Pick 
Line Picking or Skip
See [3 — Setting Up Your Picking Profile in PIPR](pick-lines-replenishment.html#3-setting-up-your-picking-profile-in-pipr) for further information.
Exclude Pick Line Stock 
When Bulk Picking
See [3 — Setting Up Your Picking Profile in PIPR](pick-lines-replenishment.html#3-setting-up-your-picking-profile-in-pipr) for further information.
Replenishment Based on 
Eligible Records
Only applicable to floating pick lines
See [Setting Up a Floating Pick Line](pick-lines-replenishment.html#setting-up-a-floating-pick-line) for further information. 
Replenish Pick Line up to 
Level
See [Setting Up a Pick Line With Replenishment by Inventory Level 2](pick-lines-replenishment.html#setting-up-a-pick-line-with-replenishment-by-inventory-level-2) for further information.
FIELD DESCRIPTIONS

Allow Overpicking of 
Order Lines
Y = Yes (Clean Out Location)
N = No
P = Partial
If you enter Y for Yes (Clean Out Location), the operator can overpick/ship an order line in RFPIC. Overpicking means picking all product in a given location so that it is left empty. For example, if the order quantity is 10 cases and there are 20 cases of the same inventory entity in the location, the operator can either pick 10 cases or 20 cases (the total quantity in that location), but no other quantity. If there are 5 cases on hold in the location, the overpick quantity will be 15 cases (20 - 5).
If you enter N for No, the operator cannot overpick/ship an order line.
If you select P for Partial, the operator can pick any quantity between the pick quantity and the location quantity. For example, if your pick quantity = 5 cases and your location quantity = 10 cases, the operator can pick 5, 6, 7, 8, 9 or 10 cases.
Picking Substitution Profile Code (PSPR)Your picking substitution profile code.
Break at SKU Class for 
Replenishment
See [3 — Setting Up Your Picking Profile in PIPR](pick-lines-replenishment.html#3-setting-up-your-picking-profile-in-pipr) for further information..
Carton Active Flag Special programming by HighJump required
Y = Yes
N = No
If you set this flag to Yes, cartonization will be activated on your system. If you set this flag to No, cartonization will be deactivated on your system. 
EDI Version Code Special programming by HighJump required
Used to allocate product by price.
EDI Transaction Set 
Code (EDTS)
Special programming by HighJump required
Used to allocate product by price.
FIELD DESCRIPTIONS

### PROCEDURE <a id="procedure"></a>

1 Enter PIPR.
2 Click on Enter Criteria then Execute Query to see which picking profiles have been already set up. 
3 If you need to set up another profile, click on Create Record.
4 Key in a picking profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 In the Break Quantity at SKU Class field, use your pick list to select the appropriate code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
7 Key in F for FIFO or L for LIFO and press Enter.
8 In the FIFO/LIFO Based on field, use your pick list to select what you want FIFO/LIFO to be based on — expiry date, receipt date or a particular inventory level.
9 If you selected an inventory level in the previous step, key in your FIFO/LIFO Formula and press Enter or press Enter to bypass this field. 
10 If required, key in a FIFO/LIFO Custom Program and press Enter.
EDI Data ID Code (EDDI) Special programming by HighJump required
Used to allocate product by price.
FIELD DESCRIPTIONS

11 Do one of the following:
12 If required, key in a sort sequence code in the Sort Sequence Code field and press Enter. If you do not require a sort sequence code, press Enter to bypass the field.
13 In the Replenishment Message on Pick Documents field, key in N for No and press Enter.
14 In the Use FIFO/LIFO for Pick Line Picking or Skip field, key in N for No and press Enter.
15 In the Exclude Pick Line Stock When Bulk Picking field, key in N for No or Y for Yes and press Enter.
16 In the Replenishment Based on Eligible Records field, key in N for No and press Enter. 
17 In the Replenish Pick Line up to Level field, key in 1 and press Enter.
18 In the Allow Overpicking of Order Lines field, key in N for No and press Enter.
19 Press Enter twice to bypass the Picking Substitution Profile Code and Break at SKU Class for Replenishment fields.
20 In the Carton Active field, key in N for No and press Enter.
If you wish to perform absolute picking:
If you wish to perform relative picking:
a) Key in A for Absolute and press 
Enter.
a) Key in R for Relative and press 
Enter.
b) In the Range in Days from Oldest 
Lot field, key in zero or a positive integer and press Enter.
c) In the Range Based on field, select the appropriate value from the pick list — EXDT, FIED, 
RCDT or FIRD.
d) If required, select the appropriate value from the Range in Days 
Starting From pick list.
e) In the Number of Records not to 
Exceed field, key in a positive integer and press Enter.
f) If required, key in a value in the 
Minimum Range in Days to 
Expiry field and press Enter.
g) If required, key in a value in the 
Maximum Range in Days to 
Expiry field and press Enter.

Picking Profile with relative option based on expiry date selected
21 Repeat the above steps to add another picking profile or click on Return to Main and then Exit to exit the program.

### Setting Up Item-Specific Picking Profiles in CCOP <a id="setting-up-item-specific-picking-profiles-in-ccop"></a>

If you are shipping to a consignee that has been assigned a picking profile and you want the shelf life of the items on the order to override the shelf life defined for the consignee, you must set up the appropriate consignee/item combinations in CCOP (Customer/Consignee Override of PIPR). 
If you do not set up the appropriate consignee/item combinations in CCOP, the shelf life of the consignee will override the shelf life of the items on the order. For example, the shelf of 15 days for the consignee will override the shelf life values for all items on the order (say, 10 days for item A, 12 days for item B, 20 days for item C, etc.).
You have two options in CCOP: 
 you can assign a picking profile to a given item
 alternatively, you can assign a picking profile to a given commodity code and commodity sub code, and that picking profile will apply to all items with that commodity and commodity sub code.
During allocation, AccellosOne 3PL will follow the sequence below to determine the applicable picking profile for a given order line:
a) if the product is on hold, the PIPR profile, if any, attached to the hold in HOLD
b) the PIPR profile, if any, attached to the item in CCOP
c) the PIPR profile, if any, attached to the commodity code/commodity sub code in CCOP

d) the PIPR profile, if any, attached to the consignee
e) the PIPR profile, if any, attached to the item
f) the PIPR record attached to DSRP and the customer
1 Enter CCOP.

Customer/Consignee Override of PIPR screen
2 Click on Create Record.
3 Key in your customer code and press Enter.
4 Key in your consignee code and press Enter.
5 Do one of the following:
6 Key in your picking profile and press Enter.
7 Repeat the above steps for each additional consignee/item override that you wish to set up.
8 When you finish setting up your consignee/item overrides, click on Return to Main.
If you are assigning a picking profile to an individual item:
If you are assigning a picking profile to a group of items through the use of commodity codes and commodity sub codes:
a) Key in your item code and press 
Enter.
a) Press Enter to bypass the Item 
Code field.
b) Key in your commodity code and press Enter.
c) Key in your commodity sub code and press Enter.

Customer/Consignee Override of PIPR screen showing three records
9 Click on Exit to exit.

### DELETING A RECORD IN CCOP <a id="deleting-a-record-in-ccop"></a>

1 Enter CCOP.
2 Retrieve the record that you wish to delete.
3 Press Enter until your cursor is positioned in the Picking Profile Code field.
4 Click on Delete.
5 Click on Return to Main and Exit to exit.

### Setting Up the Item Location Profile for Picking (ILOP) <a id="setting-up-the-item-location-profile-for-picking-ilop"></a>

In this program, you define the algorithms that you want AccellosOne 3PL to use when it performs picking. 
You can have the system pick product based on receipt date, isolator zone, quantity of product in the location and other criteria that you specify.
When you set up picking in AccellosOne 3PL, orders are channelled first through PIPR (Picking Profile), which selects product in FIFO/LIFO sequence based on receipt date or expiry date. The batch of inventory records selected by PIPR is then sent to ILOP, which selects locations based on the criteria that you specify.
There are three processes in directed picking in AccellosOne 3PL:
You can set up as many different profiles as you need. If you intend to use the same picking parameters for all product belonging to all customers, you would set up a single picking profile. If you intend to pick differently 
ENOR PIPR ILOP
Enter an order Pick product based on 
FIFO/LIFO
Pick product based on location

based on customer, you would set up a separate profile for each customer. And if certain items require special picking logic, you would have to set up separate profiles for those items that require non-standard picking. 
The profile that you create in ILOP is attached to ITEM. 

### UNDERSTANDING DIRECTED PICKING <a id="understanding-directed-picking"></a>

In picking, you want to pick product from the least desirable location first. If the least desirable location is not available, you want to pick from the next least desirable location and so on and so forth. In ILOP, you tell the system the criteria that you wish it to use for the purpose of identifying the least desirable and next least desirable locations.
You define your criteria by means of sequences. Each sequence contains a number of parameters for selecting a location. The following example shows five sequences that progressively define increasingly desirable locations.
Sample Sequences for Selecting Locations
In this example, the priorities of the warehouse are as follows:
 product should be kept in its isolator as much as possible
 full pallets should be shipped wherever possible (Break Quantity at SKU Class field in PIPR = 1 for pallets)
 high efficiency in picking takes precedence over a “clean” warehouse
If any of the priorities of your warehouse differs from the above, you would have to create different sequences.
Sequence 1 (worst)
Use any isolator other than exact match or overflow
Pick to match
Ignore partials in bulk
In this sequence, which contains the strictest selection criteria, the system searches for a location whose isolator is not an exact match or overflow and whose quantity is an exact match of the quantity needed (full pallets only).
Sequence 2 (next worst)
Use any overflow isolator
Pick to clean
If picking from bulk and location has partial and partial less than needed then pick it
In this sequence, which is less strict, the system searches for overflow locations with the least amount of product and picks from them. If it encounters a partial quantity in bulk (that is, less than a full pallet) and the partial quantity is less than the quantity needed, it picks the partial quantity.
Sequence 3 (next worst)
Use any overflow isolator 
Pick to match
Ignore partials in bulk
In sequence 3, which is less strict, the system continues to search overflow locations. This time it picks full pallets if the quantity needed is an exact match of the quantity on hand.
Sequence 4 (next worst)
Use any overflow isolator
Pick to clean
Pick partial quantity from bulk where ITEM partial in location is eliminated
The system continues to search overflow locations. This time it picks full pallets from locations with the least amount of product first. If it encounters a partial quantity in bulk (that is, less than a full pallet) and the partial quantity matches the quantity needed, it picks the partial quantity.
Last Sequence (performed by system if required)
Ignore isolator codes
Pick to clean
Ignore partials in bulk
In the last sequence, which is only performed if all the other sequences fail, the system turns all options off and uses the default in each group. 
In this example, the defaults are pick to clean from any location in the warehouse including exact match isolators.

### STANDARD LOGICAL GROUPS FOR PICKING <a id="standard-logical-groups-for-picking"></a>

There are 13 logical groups in ILOP. Each group has two or more mutually exclusive options. From each group, you select the appropriate option. If you do not wish to use a particular group, select the first option in the group to deactivate it. For example, if you do not wish to use the Hold codes group, you would select the first option, “Ignore hold codes in location”.
RECEIPT DATE GROUP (O0300)
In this group, you specify whether you want the system to pick product based on the date the product was received into a location — not the global receipt date of the item. This option is used when you receive open lots within the same item over a period of time. 
ISOLATOR GROUP (O0500)
TIP You can define up to nine passes or sequences in any given profile. It is important to bear in mind, however, that each sequence requires time to perform the specified searches to validate locations. Therefore, you must strike a balance between the requirement to pick product from the best possible location using many sequences and the requirement to process orders in a reasonable time.
ignore original receipt date of product in location (default)
Do not take into account the date the product was received into a location.
Sequence by original receipt date of product in location 
Sort all locations by the date that the product was originally received into that location. If FIFO or LIFO is needed within an entity, then this option must be turned on.
ignore isolator codes (default) Do not use isolator codes for the purposes of determining locations from which to pick.
use only exact match isolator code Pick from locations where item isolator matches the location isolator. 
use any overflow isolator code Pick from locations whose overflow isolator matches one of the overflow isolators of the item. If an item has multiple overflows, the system will pick from the last overflow first. 
use any isolator code other than exact match or overflows
Pick from locations that are outside of all isolator overflows and exact match isolators.

CAPACITY GROUP (O1000)
MIXED PRODUCT GROUP (O1500)
In this group, you specify how you want the allocation routine to clean up product from mixed locations.
pick to clean (default) Pick from locations with the least amount of product first and then pick from locations with the next most.
pick to match Pick from locations that have the exact quantity needed.
go from highest to lowest in quantities Pick from locations that have the most amount of product in them.
match order quantity and go upward Pick from locations that have the exact quantity needed. If no such locations are found, then pick from locations with the next highest quantity.
match order quantity and go downward Pick from locations that have the exact quantity needed. If no such locations are found, then pick from locations with the next lowest quantity.
match order quantity and go upward and then downward
Pick from locations that have the exact quantity needed. If no location is found, the system will search for the location with the next highest quantity. If there are no locations with the next highest quantity, the system will search for the next lowest quantity and use it. Then it will continue looking at locations with smaller and smaller quantities.
match order quantity and go downward and then upward
Pick from locations that have the exact quantity needed. If no location is found, the system will search for the location with the next lowest quantity. If there are no locations with the next lowest quantity, the system will search for the next highest quantity and use it. 
use any location (default) Pick from any location regardless of what other product may or may not be there.
use only locations where depositor code is different
Pick from locations with product belonging to more than one customer.
use only locations where up to level 1 is different
Pick from locations with product where customer or level 1 is different.
use only locations where up to level 2 is different
Pick from locations with product where customer or level 1 or level 
2 is different.
use only locations where up to level 3 is different
Pick from locations with product where customer or level 1 or level 
2 or level 3 is different.
use only locations where up to level 4 is different
Pick from locations with product where customer or level 1 or level 
2 or level 3 or level 4 is different.

ON RECEIPT MIXED PRODUCT GROUP (O2000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting locations in the Mixed Product Group. This does not mean that the allocation routine will pick product that has not been confirmed; it simply means that the system will take into account unconfirmed receipts and their locations when selecting locations from which to pick.
EXAMPLE
You receive 10 cases from customer X and assign it a given location. Because it has not been confirmed, its status remains “on-receipt.” This location already has 15 cases (confirmed) belonging to customer Y. If you select the “Use only locations where depositor code is different” option in the Mixed Product Group, the system will follow one of two scenarios: it can consider this location to have multiple customers and will attempt to pick from it (that is, on-receipt product is considered regular inventory) or it can consider this location to be a single customer location and not attempt to pick from it. 
HOLD CODES GROUP (O2500)
In this group, you specify whether you want the system to attempt to clean up locations containing multiple hold codes. The allocation routine will always pick product with the same hold code as the hold code on the order.
ON RECEIPT HOLD CODE GROUP (O3000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting locations in the Hold Code Group. This does not mean that the allocation routine will pick product that has not been confirmed; it simply means that the system will take into account unconfirmed receipts and their locations when selecting locations from which to pick.
EXAMPLE
You receive 10 cases and assign it a given location that already has 15 cases in it. The on-receipt product has a given hold code assigned to it while the confirmed product has a different hold code applied to it. If you select the “Use any location with multiple hold codes” option in the Hold Code Group, the system will follow one of two scenarios: it can consider this location to have multiple holds and will attempt to pick from it (that ignore on receipt in uniqueness calculations (default)Do not use on-receipt quantities when selecting locations in the 
Mixed Product Group.
use on receipt in uniqueness calculations Use on-receipt quantities when selecting locations in the Mixed 
Product Group — that is, treat these quantities like regular inventory.
ignore hold codes in location (default) Select locations regardless of the hold codes of the other product in that location.
use any location with only that hold code
Select locations that have only that product on that hold in that location.
use any location with multiple hold codes
Select locations that have other hold codes in that location regardless of the product the hold codes are attached to.

is, on-receipt product is considered regular inventory) or it can consider this location to have a single hold and not attempt to pick from it.
PARTIAL QUANTITY GROUP (O3500)
In this group, you specify whether you want the system to attempt to clean up locations containing partial quantities. A partial quantity is a quantity that is less than a full SKU class and not the highest SKU class. For example, if an item has a quantity breakdown of PALLETS/CASES/EACHES, then any combination of cases not forming a full pallet is considered a partial and any combination of eaches not forming a full case is considered a partial.
You define in the Break Quantity at SKU Class field in PIPR (Picking Profile) which SKU class(es) you want the system to break for the purpose of picking partials. The system will use the SKU class immediately below the SKU class you specify in PIPR. For example, suppose your quantity breakdown is PALLETS/CASES/
EACHES and your SKU classes for this quantity breakdown are 1, 3 and 5. If you specify Break Quantity at 
SKU Class 1 in PIPR, the system will consider CASES (SKU class 3) as the only valid SKU class for picking partials.
If the Break Quantity at SKU Class field in PIPR is set to “Ignore SKU classes”, then this group is ignored. 
In this group, bulk is defined as any location type set up in LOTP that is neither a pick line nor staging location type.
ignore on receipt in hold code calculations (default)Do not use on-receipt quantities when selecting locations in the 
Hold Code Group.
use on receipt in hold code calculations Use on-receipt quantities when selecting locations in the Hold 
Code Group — that is, treat on-receipt product like regular inventory.
ignore partials in bulk (default) Do not use partials in bulk for the purpose of determining locations from which to pick.
pick partials from bulk where ALL partials in location are eliminatedPick partials from bulk if all partials in the location will be eliminated. This means there cannot be partials from another item or from the same item but not in the current batch.
pick partials from bulk where ITEM partial in location is eliminatedPick from location if the partial quantity in the location is less than the partial quantity needed to fulfill the order line.
pick partials from bulk where partial is exact match and empties location
Pick from location if the partial quantity in the location matches the partial quantity needed to fulfill the order line and empties the location.
NOTE: Do not use this option in any sequence containing a Mixed 
Product Group option.
if picking from bulk and location has partial and partial less than needed pick it
If you are already picking from a bulk location as a result of an option selected in another logical group, pick from the bulk location you’re already looking at if the partial quantity in the location is less than the partial quantity of the order needed.

ON RECEIPT PARTIAL QUANTITY GROUP (O4000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting locations in the Partial Quantity Group. This does not mean that the allocation routine will pick product that is not on a confirmed receipt; it simply means that the system will take into account unconfirmed receipts and their locations when selecting locations from which to pick.
EXAMPLE
You receive a full pallet and assign it a given location, but the receipt remains unconfirmed. The location to which you assigned the pallet already has 15 cases (confirmed) in it. Therefore, you now have 1 pallet/15 cases in the location. If you select the “Pick partial quantity from bulk where partial is exact match and empties location” option in the Partial Quantity Group and enter an order for 1 pallet/15 cases, the system will follow one of two scenarios: it can consider this location to have an exact match and will attempt to pick from it (that is, on-receipt product is considered regular inventory) or it can consider this location to have only 15 cases and not attempt to pick from it.
FIFO GROUP (O4500)
In this group, which is only available if you pick relative in PIPR, you specify whether you want the system to sequence the locations to be picked by the FIFO of their inventory records within the batch.
PALLET BREAKDOWN GROUP (O5000)
In this group, you specify whether you want the system to pick from locations containing pallets with a standard quantity breakdown — that is, the quantity breakdown of the pallet matches the quantity breakdown of the item in IQBP.
ignore on receipt in partial calculations (default)
Do not use on-receipt quantities when selecting locations in the 
Partial Quantity Group.
use on receipt in partial calculations Use on-receipt quantities when selecting locations in the Partial 
Quantity Group — that is, treat on-receipt product like regular inventory.
ignore FIFO of inventory records within batch (default)
Do not use FIFO to sequence records within the inventory batch.
sequence locations by the FIFO of their inventory records within the batch
Use FIFO to sequence records within the batch from the oldest product to the newest product. If there are multiple eligible lots within the same location, the system will pick all lots in the location even if this violates the FIFO sequence.
For example, if location A has lot Jan. 5 and location B has lots 
Jan. 1 and Jan. 10, the system will pick in the following order: location B (lots Jan. 1 and Jan. 10) then location A (lot Jan. 5).
ignore matching of pallet breakdown with quantity breakdown set up in ITEM (default)
Select locations regardless of the quantity breakdown of the pallets in that location.

LOCATION TYPE GROUP (O5500)
In this group, you specify whether you want the system to pick full pallets from the pick line or from bulk.
OVERRIDE QUANTITY BREAKDOWN GROUP (O6000)
In this group, you specify whether you want the system to define a full pallet as all stock in a single location; 
that is, ignore the item’s standard quantity breakdown set up in ITEM. For example, if an item’s quantity breakdown is 60 cases per pallet and there are 50 remaining cases in a single location and all 50 cases have identical inventory levels (that is no mixed stock), AccellosOne 3PL will consider the 50 cases as a full pallet when performing full pallet picking and full pallet replenishment.

### FIELD DESCRIPTIONS (ILOP) <a id="field-descriptions-ilop"></a>

use location where pallet breakdown equal to quantity breakdown set up in 
ITEM
Select only locations in which the quantity breakdown of the pallet matches the standard quantity breakdown of the item in ITEM.
pick from all location types (default) Select locations regardless of the location type.
exclude pick line type locations when picking for SKU class 1
When picking full pallets, select only locations with a location type other than pick line.
do not override quantity breakdown (default)
Use the item’s standard quantity breakdown set up in ITEM to define a full pallet.
override quantity breakdown, treat all stock in 1 location as 1 pallet
If all product in a given location has the same inventory levels (that is, no mixed stock), consider the product a full pallet even if the number of cases is less than a full pallet.
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each sequence as well as the picking options for that sequence.
Description Mandatory
Your item location profile code description.

Isolator Code (defined in ISOL)
Mandatory
If you are using exact match or overflow isolator zones to define your picking algorithm, you will need to set up one ILOP profile for each isolator zone that you defined in ISOL.
If you do not use exact match or overflow isolator zones in your picking, use your N/A (Not Applicable) isolator.
Overflow Warehouse 
Code (defined in WARE)
Mandatory
Use any warehouse code.
Overflow Location Code (defined in LOCA)
Mandatory
Use any location code.
SEQUENCE BLOCK
Sequence Number Mandatory
1, 2, 3, 4, etc.
Each sequence or pass contains the parameters that you specify for selecting a location. The sequence numbers that you enter in this field determine the order in which sequences are run.
Description Mandatory
Your sequence number description.
FIELD DESCRIPTIONS

Warehouse Code (defined in WARE)
Optional
If you specify one or more warehouses in this field, the system will restrict its search for a location to the warehouse(s) you specify. If you leave this field blank, the system will search all warehouses.
If required, each sequence can have a different warehouse. For example, sequence 1 could search for locations in warehouse 1, sequence 2 could search for locations in warehouse 2, sequence 3 could have no warehouse assigned, etc.
You can use the following symbols (=, <, >, etc.) to define one or more warehouses:
=1
1-2
>2
<5
1-3,=7
Any warehouse beginning with the number 1 
Warehouses 1 through 2
Warehouses greater than or equal to 2
Warehouses less than or equal to 5
Warehouses 1 through 3 plus Warehouse 7
Location Code (defined in LOCA)
Optional
If you specify one or more locations in this field, the system will restrict its search for a location to the location(s) you specify. If you leave this field blank, the system will search all locations.
You can use the following symbols (=, <, >, etc.) to define one or more locations:
=100
100-200
>200
<500
100-300,=700
A100-E999
Any location beginning with 100 
Locations 100 through 200
Locations greater than or equal to 200
Locations less than or equal to 500
Locations 100 through 300 + 700
Aisles A through E
This field allows you to temporarily restrict put-away to certain locations or aisles when you are reracking your warehouse.
Acceptable Gap Height Reserved for future use.
UOM Reserved for future use.
Quantity Range Reserved for future use.
SEQUENCE BLOCK

### SETTING UP A NEW PROFILE IN ILOP <a id="setting-up-a-new-profile-in-ilop"></a>

1 Enter ILOP.
2 Do one of the following:
3 Use your pick list function to select your code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
4 Use your pick list function to select any warehouse code for your overflow warehouse.
5 Use your pick list function to select any location code for your overflow location code.
Isolator Code (defined in ISOL)
If you enter an isolator code in this field, it will override the isolator code in the 
Header Block for a particular sequence.
If you are creating a new ILOP profile:
If you are attaching your picking parameters to an existing ILOP profile:
a) Click on Create Record.
b) Key in an item location profile code and press Enter.
c) Key in a meaningful description for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to update.
b) Click on Type Block.
c) Proceed to step 5.
SEQUENCE BLOCK

Item Location Profile
6 Press your up or down arrow key in the Type Block until the Picking option is displayed.
The Sequence, Selected Options and Available Options Blocks for Picking will be displayed.
7 Click on Sequence Block.
8 Key in 1 for your first sequence and press Enter.
9 Key in a description for your first sequence (for example, FIRST PASS) and press Enter.
10 If you wish to restrict the search for locations in this sequence to a particular warehouse, key in the warehouse code and press Enter. If you want to search locations in all warehouses, press Enter to bypass this field.
11 If you wish to restrict the search for locations in this sequence to particular locations, key in the location codes and press Enter. If you want to search all locations in this sequence, press Enter to bypass this field.
You will see the first set of parameters appear in the Available Options Block.
12 Press Enter three times to bypass the Acceptable Gap Height, UOM and Quantity Range fields.
13 If you wish to override the isolator code in the header for a given sequence, key in your override isolator code and press Enter. If you do not wish to override the isolator code in the header, press Enter to bypass this field.
14 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you wish to choose and then click on Select Option. If you do not wish to use a particular group (for example, the Hold code group), select the first option in the group (“Ignore hold codes in location”) to deactivate the group.
You will see the second set of parameters appear in the Available Options Block.

15 Repeat the previous step for each set of parameters.
16 When you finish entering all your parameters for your first sequence, your cursor will be positioned in the 
Selected Options Block.

Sample Picking screen after entering sequence 1
17 Click on Sequence Block.
18 Repeat steps 7 to 16 for each additional sequence that you wish to set up for your picking profile.
19 When you finish entering all your sequences, click on Return to Main and then Type Block.
20 Click on Master Block and then Exit to exit the program.

### ASSIGNING A VELOCITY CODE TO THE ILOP PROFILE <a id="assigning-a-velocity-code-to-the-ilop-profile"></a>

You can assign velocity codes to item location profile codes (ILOP) to indicate whether a particular item is fast moving or slow moving. For example, you assign the fast moving velocity code to the ILOP profile ABC and the slow moving velocity code to the ILOP profile DEF. You then attach your velocity codes to the appropriate items in ITEM.
The purpose of velocity codes is to handle seasonal product whose velocity may change depending on the time of year. For example, turkey is a fast-moving product at Thanksgiving and a slow-moving product at other times of the year.
See [Attaching a Velocity Code to the ILOP Profile](alocacao.html#attaching-a-velocity-code-to-the-ilop-profile).

### Activating Directed Picking <a id="activating-directed-picking"></a>

Three conditions must be met before directed picking is activated:
 the Assign Location flag must be set to Yes for an outbound flow code in DIFP
 an outbound document must be set up to print in DIFP (unless you run ASOR or pick using RF)
 the locations from which you wish to pick must be assigned a location type in LOTP whose Directed 
Picking flag has been set to Yes

### Allocating Variable Quantity Breakdown Product <a id="allocating-variable-quantity-breakdown-product"></a>

If you receive variable quantity breakdown product, you must specify how you want AccellosOne 3PL to handle scenarios where the total quantity picked may not match the order quantity.
For example, suppose the quantity breakdown of a variable quantity breakdown item is 100 cases per pallet and your order quantity is 5 PLT 10 cases or 510 cases. Allocation will attempt to pick 5 whole pallets. 
However, because some of the pallets may in fact contain 90 cases or 110 cases, the total quantity picked may not match the order quantity.
You specify your allocation option in the Allocation of Variable Quantity Breakdown Items Based on Highest 
SKU Entered field in DSRP.
This field is only used for variable quantity breakdown items in which at least one SKU class is defined as a partial in the Break Quantity at SKU Class field in PIPR. As well, the item’s ILOP parameter cannot use any of the Match Quantity options.
NOTE If you activate directed picking and do not set up any picking parameters in 
ILOP, the allocation routine will use the default value for each logical group. The default value is the first option in each group.
FIELD DESCRIPTIONS
Allocation of Variable 
Quantity Breakdown 
Items Based on Highest 
SKU Entered
N = No
Y = Yes
If you set this field to N for No or leave it blank, allocation will convert the order quantity to the lowest SKU and attempt to allocate that. If you set this field to Y for Yes, allocation will attempt to allocate according to the highest SKU and the quantity shipped may exceed the order quantity if some of the pallets picked are “oversized”.

DSRP screen showing Allocation of Variable Quantity Breakdown Items Based on Highest SKU 
Entered flag set to N for No

### Allocation by Weight <a id="allocation-by-weight"></a>

You can allocate by weight by entering a W-type line in ENOR. When you allocate by weight, you enter the weight that you wish to ship rather than the number of units. During allocation, AccellosOne 3PL will change the W-type line to a R-type line and calculate the number of units that the entered weight represents. If you use reserve logic, the W-type line will be changed to a U-type line containing the number of units that the entered weight represents.
If there is insufficient inventory in your warehouse to fully fill a W-type line, the way in which AccellosOne 3PL treats the remaining unallocated weights depends upon the option that you choose in the Change Zero 
Pending Line to R-Type Line field in DSRP (Depositor Shipping & Receiving Profile) and whether or not 
Reserve Logic is activated. 
Reserve 
Logic 
Activated
Change Zero 
Pending Line 
Status Result
Y Y The remaining weight will be converted to the appropriate number of units and will appear in the Order Quantity field of a U-type line.
Y N The remaining weight will be left as a W-type line.

The only ILOP parameters available for W-type lines is the default option for each logical group. For example, in the Capacity Group of ILOP (Picking), pick to clean (the default) is the only option available. The other options in this group such as Pick to Match and Match Order Quantity and Go Upward are not available for Wtype lines. 
W-type lines are similar to P (Pending) type lines in that inventory is not reserved for the order.

### SETTING UP ALLOCATION BY WEIGHT <a id="setting-up-allocation-by-weight"></a>

In order to allocate by weight, you must set the Ship by Weight and Ship by Weight Rounding Method fields in 
ITSH (Item Shipping Profile) to the appropriate values. You then attach your ITSH profile to the appropriate items.
N Y The remaining weight will be converted to the appropriate number of units and will appear in the Order Quantity field of an R-type line.
N N The remaining weight will be left as a W-type line.
FIELD DESCRIPTIONS
Ship by Weight D = Disallowed
N = Net Weight
G = Gross Weight
If you select D for Disallowed, allocation by weight is not allowed. If you select 
N for Net Weight, you can allocate by net weight. If you select G for Gross weight, you can allocate by gross weight.
NOTE The Net Weight and Gross Weight options allow allocation by weight, but do not require it. You can still allocate by number of units if you enter a P-type line in ENOR.
Ship by Weight Rounding MethodU = Up
D = Down
If you select U for Up and the weight that you entered does not correspond to a specific number of units, AccellosOne 3PL will round up the number of units shipped. If you select D for Down and the weight that you entered does not correspond to a specific number of units, AccellosOne 3PL will round down the number of units shipped.
For example, if your shipping weight is 1,000 lbs. and you select the Down option, AccellosOne 3PL could allocate 49 units with a total weight of 990 lbs. 
If, on the other hand, you select the Up option, AccellosOne 3PL could allocate 50 units with a total weight of 1,100 lbs.
Reserve 
Logic 
Activated
Change Zero 
Pending Line 
Status Result

ITSH screen showing Ship by Weight field set to G for Gross Weight

### ENTERING A W-TYPE LINE IN ENOR <a id="entering-a-w-type-line-in-enor"></a>

1 Enter ENOR.
2 Enter your order header information in the normal manner.
3 In the Line Block, key in W for Weight in the Type field and press Enter.
4 Key in your item code and press Enter.
5 If required, key in any level 2 or higher values that you wish to select and press Enter.
6 Key in your order weight and press Enter.

ENOR screen showing a W-type line for 100 lbs.
7 Press Enter to accept the To Ship Weight.
8 When you finish entering your W-type lines, click on Master Block and Exit to exit.
Line Type = W for 
Weight

ENOR screen showing the same order after allocation (the W-type line has been converted to a Rtype line and the 100 lbs. has been converted to pallets and cases)

### Inventory Only Allocation <a id="inventory-only-allocation"></a>

Inventory only allocation allows you to reserve inventory for a given set of orders without assigning locations. 
It is equivalent to an R-type line in ENOR in which neither the level 2 or higher values nor the location has been entered. After you perform inventory only allocation, you have two options: you can enter your locations manually in ENOR or an RF program or you can run a full allocation by printing a document or by running 
ASOR (Assign Orders to Locations).
Inventory only allocation is designed for situations in which you wish to reserve inventory without assigning locations. For example, you receive your P-type orders through EDI for a particular customer and you wish to reserve inventory for those orders so that the inventory cannot be assigned to other less important orders.

### SETTING UP INVENTORY ONLY ALLOCATION <a id="setting-up-inventory-only-allocation"></a>

1 Enter DIFP.
2 Select the outbound flow at which you wish to perform inventory only allocation.
3 Set the Assign Location flag to I for Inventory Only.

DIFP screen showing inventory only allocation activated for the flow STPI
4 Exit DIFP. 

### PERFORMING INVENTORY ONLY ALLOCATION <a id="performing-inventory-only-allocation"></a>

1 Enter your order in ENOR using P-type lines. If your orders are created automatically through EDI, you can skip this step.
2 Advance the flow of the order in CHOF until you reach your inventory only allocation flow.
3 Run ASOR (Assign Locations to Orders) to perform inventory only allocation. AccellosOne 3PL will assign the inventory levels but no locations to each order line and will change the line type from P to R.
4 Advance the flow of the order in CHOF to your full allocation flow.
5 Allocate the order by printing an order document, picking the order in an RF program or running ASOR.
6 Confirm the order in the normal manner. 

### PERFORMING INVENTORY ONLY ALLOCATION IN ENOR <a id="performing-inventory-only-allocation-in-enor"></a>

If you wish to perform inventory only allocation in ENOR, no setup is required in DIFP. 
1 Enter the order header in ENOR in the normal manner. 
2 In the Line Block, enter a R-type line and key in your level 1 value.
3 Press Enter to bypass the lower inventory levels that you want AccellosOne 3PL to select.
4 Key in your quantity and press Enter.
5 Do one of the following:
AccellosOne 3PL will create as many additional R-type lines as are required to fulfil the order quantity.
6 Advance the flow of the order in CHOF in the normal manner.
7 Allocate the order by printing an order document, picking the order in an RF program or running ASOR.
If you wish to create another line: If you wish to exit:
a) Click on Create Record. a) Click on Exit.

8 Confirm the order in the normal manner. 

### Allocating Orders in ASOR <a id="allocating-orders-in-asor"></a>

The normal sequence for shipping operations in AccellosOne 3PL is first to key in the order in ENOR and then to run the allocation routine. The allocation routine is automatically triggered when you print the designated pick document, when you perform an RF function or when you run a batch program, depending on your system setup. Automatic allocation will select and assign the location(s) from which the ordered product is to be picked.
Whenever it is necessary to assign locations to an order without printing the pick document or without performing any of the other functions that would normally trigger automatic allocation, you use the program 
Assign Orders to Locations (ASOR). ASOR causes the allocation routine to run before its normal sequence. 
As ASOR assigns the locations to an order, the order lines automatically change from P to R type lines.
ASOR applies to orders that are:
 unallocated (unassigned) — they did not have a Location Code(s) assigned in ENOR 
 unconfirmed — they have not been confirmed in CHOF
 at a flow whose Assign Location flag in DIFP has been set to Y for Yes
In ASOR you can instruct the system to:
 assign locations to a specific order
 assign locations to two or more specific orders
 simultaneously assign locations to a specific order and all orders that were created after it (for example, order number 125 and all sequentially higher order numbers that are currently in the system — order number 126, 127, 128, etc.)
 simultaneously assign locations to all orders that are currently in the system

### QUERYING IN ASOR <a id="querying-in-asor"></a>

You can query ASOR to find and display orders. ASOR will only display orders that are unallocated, unconfirmed and active. Depending on your query, the system will display:
 a specific order number and all other unconfirmed orders that have a higher sequential number
 all order numbers that are currently in the system

ASOR screen
No query restrictions
Number on File will display in the Help Message 
Line how many records will be retrieved for these restrictions.
Execute Query will then display all six records.

ASOR screen showing all six records
To view all orders for all customers that are currently in the system and that are unconfirmed, active and unallocated, enter the program ASOR. Then click on Execute Query. 

ASOR screen
To view all orders for all customers that were created after a specific order number that you specify . . .
Key in the order number that you want the system to start with and click on Execute Query. For example, if you key in order number 
123, the system will display all orders for all customers that have a sequential number of 123 or higher.
To view all orders that apply to only one customer . . .
Leave the Order Number field blank and press Enter. The cursor is in the Customer Code field. Key in the customer code and click on 
Execute Query. 
To view all orders that apply to only one carrier . . .
Press Enter three times (once to bypass the Order Number field, second to bypass the Customer Code field and third to move the cursor to the Carrier Code field). Key in the carrier code and click on Execute Query.
To view all orders that are of only one order type . . .
Press Enter the required number of times to move the cursor to the 
Type field. Key in the Type Code (i.e. R for Regular, P for Pending, etc.) and click on Execute Query. 
To view all orders that have a specific order date . . .
Press Enter the required number of times to move the cursor to the 
Order Date field. Key in the date and click on Execute Query.
Clicking on Execute Query will display the selected order number (1435) 
and all subsequent order numbers that are unconfirmed, unallocated and active.

ASOR screen
You can complete more than one field at a time. For example, if you key in 123 in the Order Number field, 
CUST1 in the Customer Code field and CARR2 in the Carrier field, the system will call up and display all orders for Customer One that used Carrier Two and have an order number of 123 and higher. The more fields you are able to restrict; the fewer the number of records that will be retrieved and the simpler your search.

### ASSIGNING LOCATION(S) TO AN INDIVIDUAL ORDER <a id="assigning-location-s-to-an-individual-order"></a>

1 Enter ASOR.
2 Key in the number of the order to which you need to assign a location(s).
3 Click on Execute Query. This will display the order number that you are querying on as well as all other unconfirmed orders with subsequent order numbers.
This query will retrieve all orders that are for customer A, use carrier ABC, are of R type and have an order date of 
01.01.06.

ASOR screen
4 The cursor should be next to the order number that you are querying on. If it is not, use the up and down arrow keys to move your cursor next to the order number to which you need to assign locations.
5 Click on Select. The word “Assign” will display under the order number that you selected.
NOTE If “UNASSIGNED Not yet assigned” appears under an order, this means that the order does not have a carrier assigned to it yet. It does not refer to unassigned locations.
When you query on a specific order number (order number 1485 in this example), it will display along with all subsequent unconfirmed orders that do not yet have a location assigned to them.

ASOR screen
6 Click on Assign. The system will indicate that it is running the allocation routine to assign a location to the selected order. 
You are taken out of the ASOR program. If it is necessary to refresh the screen, press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has assigned one or more locations to the order. See the section [Looking Up an Order Processed in ASOR](alocacao.html#looking-up-an-order-processed-in-asor).
ASSIGNING LOCATIONS TO A SPECIFIC ORDER AND ALL SUBSEQUENT 
ORDERS 
1 Enter ASOR.
2 Key in the lowest order number to which you want to assign locations. 
3 Click on Execute Query. The system will call up and display the order number that you keyed in along with all other order numbers that are sequentially higher and that do not yet have a location assigned to them.
NOTE If you make a mistake and assign the wrong order number, click on Deselect. This will cancel the selection.
“Assign” displays under the selected order number.
Now click on 
Assign. The system will perform allocation and will assign a location or locations to the selected order.

ASOR screen
4 Click on Assign All. A message appears at the bottom of the screen indicating that the system is running the allocation routine. You are taken out of the ASOR program. If it is necessary to refresh your screen, press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has assigned locations to the orders. See the section [Looking Up an Order Processed in ASOR](alocacao.html#looking-up-an-order-processed-in-asor).

### ASSIGNING LOCATIONS TO ALL ORDERS <a id="assigning-locations-to-all-orders"></a>

1 Enter ASOR.
2 Click on Execute Query. This will display all unconfirmed orders that are currently in the system and that do not yet have a location assigned to them.
When you query on a specific order number (order number 1485 in this example), it will display along with all subsequent unconfirmed orders that do not yet have a location assigned to them.

ASOR screen showing details of all unconfirmed orders that are currently in the system and do not have locations assigned to them
3 Click on Assign All. 
The system will indicate that it is running the allocation routine and you are taken out of the ASOR program. If it is necessary to refresh your screen, press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has assigned locations to the orders. See the section [Looking Up an Order Processed in ASOR](alocacao.html#looking-up-an-order-processed-in-asor).

### LOOKING UP AN ORDER PROCESSED IN ASOR <a id="looking-up-an-order-processed-in-asor"></a>

1 Enter LOOR.
2 In the Order Number field, key in the number of the order that was processed in ASOR.
3 Click on Execute Query. 

LOOR screen
The order will display on the screen. Note that the Location Status field indicates that the locations have been entered.
4 Click on Line Block.
5 Note that the Location Code and Warehouse Code fields have been populated by the system. If necessary, jot their data down for future reference.
6 If the Line Block has more than one line record, use the up and down arrow keys to view the details of the other lines.
7 When you have finished viewing all of the lines, click on Master Block and Exit to exit LOOR.

### Manually De-Allocating Orders in DEOR <a id="manually-de-allocating-orders-in-deor"></a>

You use the program De-Allocate Order (DEOR) whenever it is necessary to manually remove previously assigned locations from an unconfirmed order. This program will remove the locations from either the entire order or only from the particular order lines that you specify. DEOR is restricted to orders that were allocated by the system; if you manually assigned locations to order lines in ENOR, you cannot de-allocate in DEOR.
When you remove the location from an order or order line, the location and its product is no longer attached to this order. The location and the product are now available to fill other orders. As DEOR removes the locations from an order, the order lines automatically change from R (Regular) to P (Pending) type lines.
The system has assigned locations to order number 
1573.
Click on 
Line Block to view the specific locations details.

With DEOR, the system will de-allocate the specific order or order lines that you specify regardless of other orders and their priority. If you wish to de-allocate orders based on their priority, you must define your order priorities in ORPR (Order Priorities). 

### SETTING UP MANUAL DE-ALLOCATION <a id="setting-up-manual-de-allocation"></a>

Orders can only be de-allocated if they are at a flow at which the Deassign Location flag in DIFP is set to Y for 
Yes. 

DIFP screen showing de-allocation activated for the flow FIPI (Finish Picking)

### DE-ALLOCATING AN ENTIRE ORDER <a id="de-allocating-an-entire-order"></a>

The following procedure will de-allocate an entire order. The system will remove previously assigned locations from all of the order lines.
1 Enter DEOR.
2 Key in your order number and press Enter. The system displays the details for this order, including the line details.

DEOR screen
3 Click on De-Allocate All. A message appears on the screen asking, “Do you want to de-allocate all of the lines for this order?” 

DEOR screen showing warning message
4 Key in Y (for Yes). 
At the bottom of the screen, a message will now indicate that the system is de-allocating this order. You will know that the system has completed the process when the cursor returns to the top of the screen.
5 Key in the next order that you need to de-allocate or click on Exit to exit DEOR.
You have completed the procedure. You can enter LOOR to verify that the locations have been removed from this order. The LOOR Header Block will indicate “Missing” in the Location Status field. In the LOOR Line 
Block, the Location Code and Warehouse Code fields will be blank for all of the order lines.
Key in the order number and press Enter.
The Line 
Details 
Block.

### DE-ALLOCATING INDIVIDUAL ORDER LINES <a id="de-allocating-individual-order-lines"></a>

The following procedure will de-allocate one or more specific lines of an unconfirmed order. The system will only remove previously assigned locations from the lines that you specify.
1 Enter DEOR.
2 Key in the order number and press Enter. The system displays the details for this order, including the line details.

DEOR screen
3 Use the up and down arrow keys to move the cursor next to the line that you need to de-allocate. Click on 
Select Line. The system populates the De-Allocate Status field with the term “De-Allocate.”
4 If you need to de-allocate another line, move your cursor to that line and click on Select Line. 
5 If you make a mistake and de-allocate the wrong line, use the up and down arrow keys to move the cursor back to that line. The function key button will now display as Skip Line. 
Key in the order number and press Enter.
The Line 
Details Block will show allocated lines for the order that you specified.

DEOR screen
Click on Skip Line and “De-Allocate” will disappear from the De-Allocate Status field column for this line.
6 When you have finished selecting all of the lines, click on De-Allocate Line. A warning message appears on the screen. If the message indicates the correct number of lines, key in Y (for Yes). 
Another message, at the bottom of the screen, will now indicate that the system is de-allocating this order. You will know that the system has completed the process when the cursor returns to the top of the screen.
7 Key in the next order that you need to de-allocate or click on Exit to exit DEOR.
You have completed the procedure. You can enter LOOR to verify that the locations have been removed from this order. The LOOR Header Block will indicate “Missing” in the Location Status field. In the LOOR Line 
Block, the Location Code and Warehouse Code fields will be blank for the order lines that you specified.

### Automatic De-Allocation of Orders Based on Order Priority <a id="automatic-de-allocation-of-orders-based-on-order-priority"></a>

You can have AccellosOne 3PL perform automatic de-allocation based on the order’s priority level by setting the Allow Deallocate flag in ORPR (Order Priorities) to the appropriate value. If there is insufficient stock to fill a given order, the system will look at other orders with different priority levels to see which of these orders can be de-allocated in favour of the current order.
If you use RF, only orders that have not been picked will be de-allocated to fill an order with a higher priority level; if even a single line on an order has been picked, the entire order is disqualified from de-allocation. If 
Column for the DeAllocate 
Status field.
Lines 2 and 
3 will be de-allocated.
Skip Line option

you do not use RF, the system will not check an order to see whether it has been picked and de-allocation can occur at any flow up to but not including order confirmation (COOR).

### SETTING UP AUTOMATIC DE-ALLOCATION <a id="setting-up-automatic-de-allocation"></a>

You set up automatic de-allocation by setting the Allow Deallocate flag in ORPR to the appropriate value. If you set this flag to Yes and there is insufficient stock to fill the order, the system will look at other orders with different priority levels to see which of these orders can be de-allocated in favour of the current order.
Only those orders assigned a priority level whose Allow Deallocate flag is set to No will be de-allocated to fill the order whose flag is set to Yes. Normally, you would set this flag to Yes for the higher priority levels and set this flag to No for the lower priority levels.
When de-allocation occurs, AccellosOne 3PL will remove the locations from the order lines to be de-allocated and change the status of these order lines from Regular to Pending. As well, the de-allocated order will appear on the pending orders report.
1 Enter ORPR.
2 Click on Enter Criteria then Execute Query to retrieve your order priorities.
3 Use your arrow keys to position the cursor on the priority level that you wish to modify.
4 Press Enter until your cursor is positioned in the Allow Deallocate field.
5 In the Allow Deallocate field, key in the appropriate value (Y for Yes or N for No) and press Enter.
6 Repeat the above steps for each additional priority level that you wish to modify.

ORPR screen showing Allow Deallocate flag set to Y for Yes for priorities 1, 2 and 3
7 When you finish setting up your priority levels, click on Exit to exit. If Exit is not available, click on Return to Main and Exit.

### ASSIGNING PRIORITY LEVELS TO ORDERS IN ENOR <a id="assigning-priority-levels-to-orders-in-enor"></a>

You assign a priority level to an order by changing the value in the Priority field during order entry in ENOR. If you do not change the priority value in ENOR, AccellosOne 3PL will use the default value of five.

### Allocating Product Based on Shelf Life <a id="allocating-product-based-on-shelf-life"></a>

You have two options for defining the minimum shelf life of a given product:
 you can use your standard picking profiles defined in PIPR
 you can define at the order line level the minimum shelf life 
ENTERING ORDERS WITH A SHELF LIFE BASED ON A DATE OTHER THAN THE 
SYSTEM DATE
If you select Order Date, To Ship Date or To Arrive Date as your option in the Range in Days Starting From field in PIPR, you must enter these dates accurately in the Header Block of ENOR.
1 Enter ENOR.
2 Enter your customer code, consignee code and sold-to code in the normal manner.

ENOR screen showing prompt for Order Date
3 Make sure that you enter the correct dates in the Order Date, To Ship Date and To Arrive Date fields.
4 Process the rest of the order in the normal manner.

### OVERRIDING THE SHELF LIFE OF INDIVIDUAL ORDER LINES IN ENOR <a id="overriding-the-shelf-life-of-individual-order-lines-in-enor"></a>

You can define at the order line level the minimum shelf life for product being shipped out. Only inventory with that minimum shelf life (that is, a production date or expiry date equal to a specific date or later) will be selected during allocation. 
You activate the shelf life override feature by setting the Dynamic Shelf Life Calculation Method flag in ITSH to the appropriate value: E for Expiry Date or P for Production Date.

ITSH screen showing Dynamic Shelf Life Calculation Method flag set to E for Expiry
You override a product’s shelf life by entering the appropriate value in the Number of Days for Shelf Life 
Override field in the Line Block of ENOR. During allocation, the following calculations will occur:
1 AccellosOne 3PL will recalculate the product’s production date/expiry date from the product’s expiry date using the ITSH formula and shelf life duration values.
2 t will check the appropriate PIPR record to determine the Range in Days Starting From value (to arrive, order, to ship or system date) for the order.
3 It will subtract the number in days that you enter in the Number of Days for Shelf Life Override field from the appropriate date (to arrive, order, to ship, etc.) in the order header to arrive at a new date, the earliest acceptable production date/expiry date. 
4 It will compare the earliest acceptable production date/expiry date (step 3) with the production date/ expiry date of product in inventory (step 1). Only inventory with a production date/expiry date equal to or later than this date will be selected during allocation.
NOTE When you define the minimum shelf life at the order line level, you override the minimum shelf life defined in all your PIPR profiles whether attached to the customer in DSRP, the item in ITEM, the consignee in CONS or the item/consignee in 
CCOP.

EXAMPLE
To arrive date in order header = May 15
Number of Days for Shelf Life Override = 10
Lots in inventory = lot A (production date of May 1), lot B (production date of May 5) and lot C (production date of May 7)
AccellosOne 3PL will subtract 10 from 15 to arrive at May 5. Only inventory with a production date of May 5 or later will be selected during allocation (that is, lots B and C). If you do not enter a value in this field, the allocation routine will search for inventory whose expiry dates satisfy the expiry date criteria that you define in 
PIPR (Picking Profile).

ENOR screen showing Number of Days for Shelf Life Override field set to 10
The following requirements must be met before you can override the shelf life for individual order lines:
 the order line type is either P for Pending or W for Weight
 the product’s expiry date is calculated from an inventory level containing the production date using an expiry date formula and shelf life duration defined in ITSH (Item Shipping Profile)
 the picking profile that applies to the order has a Range Based on value of expiry date and a Range in 
Days Starting From value of to ship date, to arrive date, order date or system date (that is, allocation date)

### ALLOCATING BY SHELF LIFE PERCENTAGE <a id="allocating-by-shelf-life-percentage"></a>

You can allocate product by a percentage of the shelf life remaining rather than a fixed number of days; that is, only ship product if it has a shelf life of at least say 25, 50 or 75% of the product’s total shelf life.

EXAMPLE 1 customer’s minimum shelf life percentage (PIPR) = 50% item A’s shelf life duration and frequency in ITSH = 100 days item B’s shelf life duration and frequency in ITSH = 200 days on day of allocation, item A has 40 days shelf life left item B has 101 days shelf life left
Item A will not allocate because it has only 40% shelf life remaining. Item B, on the other hand, will allocate because it has more than 50% shelf life remaining.
EXAMPLE 2
If a consignee’s minimum shelf life percentage is 30% and the product being shipped is same as that in 
Example 1, both items would allocate because there is more than 30% of the total shelf life remaining on both items.
You set up allocation by shelf life percentage in PIPR by selecting “Shelf Life Percentage” in the Range Based on field. In the Minimum Remaining Shelf Life Percentage field, you enter your percentage. In ITSH you set up your shelf life duration and frequency for your items.
PIPR screen showing minimum remaining shelf life percentage of 40%

### Allocating Orders With Reserve Logic <a id="allocating-orders-with-reserve-logic"></a>

Reserve logic allows you to reserve inventory during order allocation at a level other than the lowest level for a customer. By using this option, you allow the picker to make the final selection at the lot or pallet ID level based on which product is most accessible. Reserve logic is designed for warehouses with bulk locations.

For example, suppose you have a three-level account — Item / Lot / Pallet ID — and you wish to reserve inventory at level 2. When you allocate orders for this account, AccellosOne 3PL will select the lot and the location but not the pallet ID. The line type for the order line will be set to U for Unknown and the pallet ID will be shown as a plus sign (+) to indicate that it has not been selected. Once the product has been picked, the operator will enter the pallet ID (level 3) manually or scan it in using an RF device. At this point, the U-type lines will be changed to R for Regular.
In the above example, because the system has not selected a pallet ID, the operator can pick the pallet that is most accessible — that is, pallet 11.

### SETTING UP RESERVE LOGIC <a id="setting-up-reserve-logic"></a>

You set up reserve logic in CUST (Customer Codes) by entering the appropriate value in the Reserve Orders at Level Number field. 
1 Enter CUST.
2 Retrieve the customer that you wish to set up for reserve logic.
3 Press Enter until your cursor is positioned in the Reserve Orders at Level Number field.
4 In the Reserve Orders at Level Number field, key in the inventory level that you wish to reserve at and press Enter.
If you leave this field blank, reserve logic will be switched off and the system will select down to the lowest level of inventory.
NOTE Reserve logic is not available for items with a variable quantity breakdown. 
After allocation, AccellosOne 3PL may create multiple U-type lines from a single Ptype line in ENOR. Each U-type line will contain the same inventory entity in the same location and the sum of all the U-type lines will equal the total number of units of the 
P-type line. This is a normal occurrence in reserve logic and no cause for concern.
11 06

CUST (Customer Codes) screen showing Reserve Orders at Level Number field set to 2
5 Click on Return to Main and Exit to exit CUST.

### ENTERING ORDERS IN ENOR <a id="entering-orders-in-enor"></a>

Reserve logic requires a line type of P for Pending in ENOR.
1 Enter ENOR.
2 Enter the header information for the order in the normal manner.
3 In the Line Block, set the line type to P for Pending.
4 Key in your item code/level 1 value and press Enter.

ENOR screen showing the line type set to P for Pending
5 Press Enter to bypass your remain inventory levels. 
6 Key in your order quantity and press Enter. 
7 When you finish entering your order lines, click on Return to Main and Master Block. Then click on Exit to exit.
8 Allocate the order in the normal manner. When you allocate an order using reserve logic, AccellosOne 
3PL will change the line type from P to U for Unknown with a plus sign (+) indicating the unknown inventory levels.
CAUTION Do not enter inventory levels lower than the level 1. If you do, AccellosOne 3PL may be unable to allocate the order correctly.

Look Up Orders (LOOR) screen showing U-type line with a plus sign for pallet ID

### USING RESERVE LOGIC IN A NON-RF ENVIRONMENT <a id="using-reserve-logic-in-a-non-rf-environment"></a>

If you wish to use reserve logic in a non-RF environment, you must enter ENOR after the product has been picked and manually change the U-type order lines to R-type order lines. You change a U-type line to R-type line by deleting the U-type line and creating a new R-type line.
1 Enter ENOR.
2 Retrieve the order whose line types you wish to manually change.
3 Select the first order line. Note the inventory levels, order and to ship quantities and location for this line. 
You will need this information when you create a new R-type line for the product.
4 Press Enter to position your cursor in Remark field. Then click on Delete to delete the line.
5 Click on Create Record.
6 If required, change the line type of your new line to R for Regular.
7 Enter your R-type line. You must enter all inventory levels shown on the original U-type line, the inventory level or levels selected by the picker, the original order line’s order and to ship quantities as well as the original order line’s location information.
8 Repeat the above steps for each additional order line.
9 When you finish changing all your order lines, exit ENOR and advance the order’s flows normally in 
CHOF.

### LOOKING UP INVENTORY IN LOEN <a id="looking-up-inventory-in-loen"></a>

When you use reserve logic, AccellosOne 3PL creates a plus record in LOEN for the product on order whose inventory level or levels is unknown. A plus record is a temporary record in which the unknown inventory level is indicated by a plus sign. 
AccellosOne 3PL creates plus records at all inventory levels below the level at which you reserve inventory. 
For example, if you reserve at level 2, AccellosOne 3PL will create plus records for your level 3 values and level 4 values. If you reserve at level 3, AccellosOne 3PL will create plus records for your level 4 values.
The plus record for an unpicked order will show a negative available quantity and a positive on order quantity for the same amount. Once the product has been picked, all quantities of the plus record will be set to zero. 
Plus records for picked orders will remain on your system until you purge your inventory. They have no further affect on your inventory and should be ignored.
EXAMPLE
You enter an order for 10 cases with reserve logic activated for level 3 (pallet ID). The plus record for lot 101 shows -10 cases as available and 10 cases as on order.
When you pick the 10 cases, the plus record is set to zero and the order is assigned to one of the non-plus records (in this example, lot 101/pallet ID 001).
Lot Pallet ID Available On Hand On Order
101 001 100 100 0
101 002 50 50 0
101 + -10 0 10
102 007 75 75 0
102 + 0 0 0
Lot Pallet ID Available On Hand On Order
101 001 90 100 10
101 002 50 50 0
101 + 0 0 0
102 007 75 75 0
102 + 0 0 0

Look Up Inventory (LOEN) screen showing query at level 2 with “+” record indicating 25 cases on order whose pallet ID is unknown

### Performing Soft Allocation <a id="performing-soft-allocation"></a>

Soft allocation allows you to reserve inventory for a given set of orders without assigning locations. It is designed for facilities that wish to reserve inventory for an order as soon as the order is received, but only perform final allocation for the order much later when they are ready to ship. 
Soft allocation must be activated in CUST by setting the flag Allocate U Line (No Location) to R Line field to Y for Yes. The flag is only available if the Reserve Order at Level Number field is set to 1, 2 or 3.
NOTE When reserve logic is activated on your system, the available quantity for a given inventory entity is reserved when there is a plus record for that entity with a non-zero quantity. Do not attempt to ship or relocate the full available quantity for that inventory; only the available quantity as shown in LOEN minus the quantity of any plus records can be shipped or relocated.

CUST screen showing soft allocation activated
Soft allocation works as follows. First, you enter a P-type order line in ENOR. When you run allocation for the first time by printing a document or running ASOR, AccellosOne 3PL will convert the P-type lines to U-type lines and create + records for inventory levels 2, 3 and 4. When you are ready to ship a particular order, you run allocation for the second time. AccellosOne 3PL will convert the U-type lines to R-type lines, assign all inventory levels and locations and generate any required replenishments.

### Performing Hard Allocation in OPLU <a id="performing-hard-allocation-in-oplu"></a>

You can perform hard allocation in OPLU (Order Line Inventory/Location Update). It offers a simpler, easierto-use alternative to performing hard allocation in ENOR by means of an R-type order line.
1 Enter OPLU.
2 Key in your order number and press Enter.

OPLU screen showing one P-type line
3 Key in your level 2/3/4 values for each order line that you wish to hard allocate. Alternatively, you can select your level 2/3/4 values from the inventory pick list.
OPLU screen showing inventory pick list and available quantity
Alternatively, you can select your level 2/3/4 values from the location pick list, which shows locations as well as quantities and all inventory levels.

OPLU screen showing inventory location pick list and available quantity
4 When you finish entering/selecting your inventory levels, OPLU will show all inventory levels fully populated.
OPLU screen showing inventory levels fully populated
5 When you finish selecting your inventory levels for the hard allocation, click on Save.
6 When prompted to save your changes, click on Yes. OPLU will refresh showing a blank screen with no data.
7 Click on Exit to exit OPLU.

### CHANGING THE ORDER QUANTITY OF AN ORDER LINE <a id="changing-the-order-quantity-of-an-order-line"></a>

If you change the quantity of an order line in OPLU, AccellosOne 3PL will split the order line into two: one order line for the new quantity that you typed in and a second order line for the difference between the original quantity and the new quantity.

1 Enter OPLU.
2 Retrieve the order that you wish to hard allocate.
3 Select the order line whose quantity you wish to change.
OPLU screen
4 In the New Quantity field, key in your new quantity and click on Change Quantity.
5 When prompted to confirm the change in quantity, click on Yes.
AccellosOne 3PL will split the order line into two: one order line for the new quantity that you typed in and a second order line for the difference between the original quantity and the new quantity.
OPLU screen showing two order lines: 7 cases (new quantity) and 3 cases (difference between new quantity and original quantity)
6 Click on Exit to exit OPLU.

### Using Wildcards and Boolean Logic in Allocation <a id="using-wildcards-and-boolean-logic-in-allocation"></a>

You can use wildcard characters and Boolean logic when entering your inventory level 2/3/4 values in ENOR. 
This feature, which is only available for P-type and W-type order lines, allows you precise control over which lots or pallet ID’s allocation should look at or not look at when selecting the best product to ship. With wildcard characters and Boolean logic, you can
 exclude a specific lot or a range of lots when shipping to a particular consignee
 include all lots starting with or ending with a particular value or set of values 
 define complex conditions using AND/OR logic in math-like statements with brackets to specify the order of operations
The following wildcard characters/Boolean operators are supported in ENOR:
 ! = NOT EQUAL TO
 % = LIKE
 ~ = AND
 | = OR
LEVEL 2 VALUE DESCRIPTION
!123456 Not equal to 123456
23% Any string starting with 23
!23456~23% Not equal to 123456 and starting with 23
!23456|23% Not equal to 123456 or starting with 23
!23456|(23%~!23456) Not equal to 123456 or starting with 23 but not equal to 23456
123456|98765 Equal to 123456 or 98765
123%|987% Any string starting with either 123 or 987 (12%345|((98776%~%334)|!34
9%))
Any string starting with 12 and ending with 345 or (any string starting with 
98776 and ending with 334 or not equal to any string starting with 349)
NOTE Special characters such as !, % or ~ should not be used in inventory levels when receiving product in ENRE. If you do, allocation could ignore the meaning of the special character and allocate the inventory entity itself.

ENOR screen showing wildcard character in lot number (23%)

### Allocating Only Fully Filled Orders <a id="allocating-only-fully-filled-orders"></a>

You can set up AccellosOne 3PL so that only orders that can be fully filled will be allocated; an order is considered to be fully filled when there is enough product in the warehouse to fill all lines on the order. If a single line on a given order cannot be fully filled, the system will automatically de-allocate the entire order. 
The location status of the de-allocated order in LOOR will be “Missing” and the location and warehouse code fields will be blank for all order lines.
Allocating only fully filled orders requires P-type or W-type lines in ENOR.
If you do not activate allocation of only fully filled orders, order lines that cannot be fully allocated will be processed according to the option that you select in the Change Zero Pending Line to R-Type Line field in 
DSRP.

### SETTING UP ALLOCATION OF ONLY FULLY FILLED ORDERS <a id="setting-up-allocation-of-only-fully-filled-orders"></a>

There are two setup programs for allocating only fully filled orders: DSRP (Depositor Shipping & Receiving 
Profile) and CONS (Consignees). The Ship Only Fully Filled Orders flag must be set to Y for Yes in both programs for a given customer and consignee before you can restrict allocation to fully filled orders. 

DSRP screen showing Ship Only Fully Filled Orders flag set to Y for Yes

CONS screen showing Ship Only Fully Filled Orders flag set to Y for Yes for consignee A

MANUALLY DEACTIVATING ALLOCATION OF ONLY FULLY FILLED ORDERS IN 
ENOR
You can manually deactivate the allocation of only fully filled orders for a specific customer or consignee by entering N for No in the Ship Only Fully Filled Orders field in ENOR. 
1 Enter ENOR.
2 Enter your order header information in the normal manner.
3 When your cursor is positioned in the Distribution Type Code field, press F9 (Previous field).
4 In the Ship Only Fully Filled Orders field, key in N for No and press Enter.

ENOR screen showing Ship Only Fully Filled Orders flag set to N for No
5 Enter your order lines in the normal manner.
6 When you finish entering your order lines, click on Return to Main and Master Block. Then click on Exit to exit.

### Allocating by Minimum Level 2, 3 and 4 Values <a id="allocating-by-minimum-level-2-3-and-4-values"></a>

Minimum shipping level values in IMSL allow you to pick product based on minimum level 2, 3 and 4 values. 
For example, you can specify that you want the system to only pick product whose level 2 value is greater than or equal to A01. Minimum shipping level values are intended for computer products like motherboards 

with revision levels such as A01, B, B99, C00, etc. As older revision levels become out of date, IMSL allows you to set a minimum level for shipping — that is, only ship product that is revision level 7.1 or later.
The records selected will be processed in normal FIFO/LIFO sequence according to the rules laid out in PIPR (Picking Profile).
You can use IMSL to specify:
 a global minimum value
 a range (greater than or equal to the minimum value and less than another value)
 a series of ranges (greater than or equal to the minimum value 1 and less than value 1.1, greater than or equal to the minimum value 2 and less than value 2.1, etc.)
There are four fields used in IMSL to set a minimum value:
 Starting Position and Length fields (used to determine the “less than” value for ranges)
 Value field (used to determine the minimum value)
 Exception field (reserved for future use)
Allocation will select all inventory records with a level 2 value that is:
 greater than or equal to B 
REMARK: Because there is only a single value in the Exception Block, IMSL will ignore any values that you enter in the Starting Position and Length fields.
Allocation will select all inventory records with a level 2 value that is:
 greater than or equal to B01 and less than C (because the Starting Position and Length fields are both 1, the “less than” value is C — not C02) 
 greater than or equal to C02
REMARK: Because there are two entries in the Exception Block, IMSL will treat the pair as a range. The first entry will be the minimum value and the second entry will be the “less than” value.
EXAMPLE 1
Item Minimum Shipping Level Flag (DILP) = Yes for the second level of inventory
Values in Exception Block
B
Starting Position = 1
Length = 1
EXAMPLE 2
Item Minimum Shipping Level Flag (DILP) = Yes for the second level of inventory
Values in Exception Block
B01
C02
Starting Position = 1
Length = 1

Allocation will select the inventory records whose level 3 value is:
 greater than or equal to A99 and less than B (no values)
 greater than or equal to B09 and less than C (for example, B09, B10, B11, etc.)
 greater than or equal to C99 and less than D (no values)
 greater than or equal to D00 (for example, D00, D01, D05, E10, F12, etc.)

### SETTING UP YOUR ITEM MINIMUM SHIPPING LEVEL PARAMETERS <a id="setting-up-your-item-minimum-shipping-level-parameters"></a>

You set up your item minimum shipping level parameters in IMSL.
EXAMPLE 3
Item Minimum Shipping Level Flag (DILP) = Yes for the third level of inventory
Values in Exception Block
A99
B09
C99
D00
Starting Position = 1
Length = 1
NOTE Because there are multiple entries in the Exception Block, IMSL will pair each entry with the entry that follows and treat the two entries as a range. The first entry will be the minimum value and the second entry will be the “less than” value.
FIELD DESCRIPTIONS
Customer Code Mandatory
Your customer code.
Item Code Mandatory
Your item code.

Starting Position Mandatory
If you are defining a range or series of ranges, you must specify in the Starting 
Position and Length fields which characters in your IMSL value your inventory level value should be less than. For example, if you set the starting position to 
1 and the length to 1, then your inventory level value must be less than the first character of your IMSL value(s). Alternatively, if you set the starting position to 3 and the length to 2, then your inventory level value must be less than the third and fourth characters of your IMSL value(s).
If you are not defining a range, you do not need a starting position and length. 
Set both these fields to 1.
Length Mandatory
See Starting Position field.
Value Mandatory
If you add a single entry to the Exception Block in IMSL, the single entry will be your minimum value and only product greater than or equal to it will be allocated. Any values that you enter in the Starting Position and Length fields (for example, 1 and 1) will be ignored because there is no “less than” value.
If you add multiple entries to the Exception Block in IMSL, the program will treat each two entries as a pair. The first entry in the pair (entry 1) will be the minimum value and the second entry in the pair (entry 2) will be the “less than” 
value. The system will use the starting position and length values to determine which part of the IMSL value the item’s inventory level should be less than.
EXAMPLES starting position = 1 length = 1
Your inventory level value must be less than the first character of your IMSL value(s). 
FIELD DESCRIPTIONS

1 Enter DILP and set the Item Minimum Shipping Level Flag to Yes for the inventory level that the minimum value applies to.

DILP screen showing Item Minimum Shipping Level Flag set to Yes for level 2
2 Enter IMSL.
starting position = 3 length = 2
Your inventory level value must be less than the third and fourth characters of your IMSL value(s).
After evaluating entries 1 and 2, the allocation routine will evaluate entries 2 and 3. This time entry 2 will be the minimum value and entry 3 will be the “less than” value. When entries 2 and 3 are evaluated, the allocation routine will look at entries 3 and 4. This process will continue until the last entry in the 
Exception Block is reached and there is no longer a “less than” value.
Exception Mandatory
The Exception field in IMSL is reserved for future use. You must enter an operand (for example, =) in order to add an entry to the Exception Block, but the operand that you enter is ignored by IMSL.
FIELD DESCRIPTIONS

Item Minimum Shipping Level
3 Key in your customer code and press Enter.
4 Key in your item code and press Enter.
5 In the Starting Position field, key in the starting position of the characters in your IMSL value that your inventory level should be less than and press Enter.
6 In the Length field, key in the length of your IMSL value and press Enter. 
7 In the Value field, key in your level 2, 3 or 4 value and press Enter. 
8 In the Exception field, key in = as your operand and press Enter.
9 Repeat the above two steps for each additional value that you wish to add to the Exception Block.

IMSL screen showing five values in the Exception Block
10 When you finish setting up your minimum shipping values, click on Return to Main and Master Block. 
Then click on Exit to exit.

### PERFORMING ITEM MINIMUM SHIPPING LEVEL ALLOCATION <a id="performing-item-minimum-shipping-level-allocation"></a>

1 Enter a P-type order line in ENOR. Make sure that no value is entered for the inventory level that the minimum value applies to in either ENOR or any EDI program.

### Reserving a Minimum Level of Inventory for High Priority Orders <a id="reserving-a-minimum-level-of-inventory-for-high-priority-orders"></a>

You can reserve a certain level of inventory for high priority orders by setting the Evaluate Minimum flag in 
ORPR (Order Priorities) to the appropriate value and defining an item’s minimum quantity in ITEM.
For example, suppose you stock motherboards and you wish to keep five motherboards in stock at all times in order to handle rush orders. First you set the value in the Minimum Quantity field in the Quantity 
Breakdown Block of ITEM to five. Then you set the Evaluate Minimum flag to Y for Yes for all priorities except the highest. For the highest priorities — say priorities 1 and 2 — you would set the Evaluate Minimum flag to 
N for No.
When a regular order is received for motherboards (say, priority 5 or 6), the system will evaluate the minimum; that is, check whether the order can be filled without reducing the on-hand quantity to less than five. If there are only five motherboards in stock, they will be “locked” and the regular order will not be allowed to allocate them.
When a high priority order is received for motherboards (say priority 1 or 2), the minimum will not be evaluated because the Evaluate Minimum flag has been set to N for No. The high priority order will ignore the minimum quantity defined in ITEM and will allocate however many of the remaining five motherboards that it needs.

### SETTING UP A MINIMUM LEVEL OF INVENTORY <a id="setting-up-a-minimum-level-of-inventory"></a>

1 Enter ITEM.
2 Retrieve the item that you wish to set up for a minimum level of inventory.
3 Click on Quantity Breakdown Block.
4 Enter your minimum quantity in the Minimum Quantity field.

ITEM screen showing a minimum quantity of ten
5 Click on Master Block and Exit to exit.
6 Enter ORPR.
7 Click on Enter Criteria then Execute Query to retrieve your order priorities.
8 Use your arrow keys to position the cursor on the priority level that you wish to modify.
9 Press Enter until your cursor is positioned in the Evaluate Minimum field.
10 In the Evaluate Minimum field, key in the appropriate value (Y for Yes or N for No) and press Enter. 
Higher priorities should have the flag set to N for No while lower priorities should have the flag set to Y for 
Yes.
11 Repeat the above steps for each additional priority level that you wish to modify.

ORPR screen showing Evaluate Minimum flag set to N for No for priorities 1 and 2
12 When you finish setting up your priority levels, click on Exit to exit. If Exit is not available, click on Return to Main and Exit. 

### ASSIGNING PRIORITY LEVELS TO ORDERS IN ENOR <a id="assigning-priority-levels-to-orders-in-enor"></a>

See [Assigning Priority Levels to Orders in ENOR](alocacao.html#assigning-priority-levels-to-orders-in-enor).

6 — Assigning Your Location Type to Your Pick Line Locations in LOCA 141
