# Manual K — Allocation and Wave Manager Guide (Alocação e Wave Manager)

> **ID do Manual:** K  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Alocação inbound (put-away dirigido via ILOP/PUPR/IPUP) e outbound (picking via PIPR/ASOR/DEOR). Wave Manager para agrupamento e priorização de ordens. Replenishment (RFRO/RFRP). Directed moves (DMPA/DMPR). Reserve logic. Pick lines.

---

AccellosOne Enterprise 
3PL Allocation and 
Wave Manager Guide 
(Classic)
May 2016
Release 4.2

Copyright © HighJump
All rights reserved
This manual is reserved for licensed users of AccellosOne Enterprise 3PL and e-Vista. If you are not a 
licensed user of AccellosOne Enterprise 3PL and e-Vista, no part of this publication may be reproduced, 
stored in a retrieval system or transmitted in any form or by any means electronic, mechanical, recording or 
otherwise, without the prior written consent of HighJump.
The information in this manual is furnished for informational use only, is subject to change without notice and 
should not be construed as a commitment of HighJump. HighJump assumes no responsibility or liability for 
any errors or inaccuracies that may appear in this manual.

ALLOCATION AND WAVE MANAGER 4.2 i
TABLE OF CONTENTS
INTRODUCTION ......................................................................... 1
AccellosOne 3PL Documentation Set ............................................................... 2
INBOUND ALLOCATION .............................................................. 3
Overview .............................................................................................................. 4
Item Location Profile for Put-Away (ILOP)........................................................ 4
Understanding Directed Put-Away................................................................. 4
Standard Logical Groups for Put-Away.......................................................... 5
Field Descriptions (ILOP)............................................................................. 20
Setting Up a New Profile in ILOP for Directed Put-Away............................. 23
Overriding the ILOP Profile for Individual Receipt Lines in ENRE ............... 26
Attaching a Velocity Code to the ILOP Profile ............................................. 27
Item Receipt Hold Profile Code (IRHP)............................................................ 29
Put-Away Profile Code (PUPR) ........................................................................ 31
Activating Directed Put-Away .......................................................................... 34
Deactivating Directed Put-Away for Selected Receipts................................. 34
Setting Up Directed Put-Away Deactivation................................................. 35
Processing Receipts With Directed Put-Away Deactivation Turned On ...... 36
Looking Up Skipped Receipt Lines in LORE ............................................... 38
Put-Away by Warehouse Zone......................................................................... 38
WHZO (Warehouse Zone Codes)................................................................ 38
ITEM (Item Code) ........................................................................................ 39
Zone Code Group (ILOP)............................................................................. 40
Put-Away by Location Size .............................................................................. 40
Setup in LOCS ............................................................................................. 41
Setup in LOCA ............................................................................................. 42
Setup in ILOP............................................................................................... 42
Sort Sequences and Proximity Logic for Last Location Used Group.......... 42
LOCA (Locations) ........................................................................................ 42
WARE (Warehouse and Location Format) .................................................. 43
Item Put-Away Parameters (IPUP) ................................................................... 44
Put-Away by Pallet Type................................................................................... 46
OUTBOUND ALLOCATION ..........................................................47
Understanding Allocation ................................................................................ 49
Manual Allocation......................................................................................... 49
Automatic Allocation .................................................................................... 49
Selection of Product..................................................................................... 49
Selection of Location.................................................................................... 50

ii 4.2 ALLOCATION AND WAVE MANAGER
Shipping With Insufficient Inventory............................................................. 50
Printing Your Pick Document ....................................................................... 51
Setting Up Outbound Allocation...................................................................... 52
Setting Up the Picking Profile (PIPR) .............................................................. 52
Changing Your Picking Profile ..................................................................... 52
Procedure .................................................................................................... 63
Setting Up Item-Specific Picking Profiles in CCOP ....................................... 65
Deleting a Record in CCOP ......................................................................... 67
Setting Up the Item Location Profile for Picking (ILOP)................................ 67
Understanding Directed Picking................................................................... 68
Standard Logical Groups for Picking ........................................................... 69
Field Descriptions (ILOP)............................................................................. 74
Setting Up a New Profile in ILOP................................................................. 77
Assigning a Velocity Code to the ILOP Profile............................................. 79
Activating Directed Picking.............................................................................. 80
Allocating Variable Quantity Breakdown Product ......................................... 80
Allocation by Weight......................................................................................... 81
Setting Up Allocation by Weight................................................................... 82
Entering a W-type Line in ENOR ................................................................. 83
Inventory Only Allocation................................................................................. 85
Setting Up Inventory Only Allocation ........................................................... 85
Performing Inventory Only Allocation........................................................... 86
Performing Inventory Only Allocation in ENOR ........................................... 86
Allocating Orders in ASOR .............................................................................. 87
Querying in ASOR ....................................................................................... 87
Assigning Location(s) to an Individual Order ............................................... 91
Assigning Locations to a Specific Order and all Subsequent Orders .......... 93
Assigning Locations to All Orders ................................................................ 94
Looking Up an Order Processed in ASOR................................................... 95
Manually De-Allocating Orders in DEOR ........................................................ 96
Setting Up Manual De-Allocation ................................................................. 97
 De-Allocating an Entire Order ..................................................................... 97
De-Allocating Individual Order Lines............................................................ 99
Automatic De-Allocation of Orders Based on Order Priority...................... 100
Setting Up Automatic De-Allocation........................................................... 101
Assigning Priority Levels to Orders in ENOR............................................. 101
Allocating Product Based on Shelf Life........................................................ 102
Entering Orders With a Shelf Life Based on a Date Other Than the System 
Date ........................................................................................................... 102
Overriding the Shelf Life of Individual Order Lines in ENOR ..................... 103
Allocating by Shelf Life Percentage ........................................................... 104
Allocating Orders With Reserve Logic.......................................................... 105
Setting Up Reserve Logic .......................................................................... 106

ALLOCATION AND WAVE MANAGER 4.2 iii
Entering Orders in ENOR .......................................................................... 107
Using Reserve Logic in a Non-RF Environment ........................................ 109
Looking Up Inventory in LOEN .................................................................. 110
Performing Soft Allocation............................................................................. 111
Performing Hard Allocation in OPLU ............................................................ 112
Changing the Order Quantity of an Order Line .......................................... 114
Using Wildcards and Boolean Logic in Allocation ...................................... 116
Allocating Only Fully Filled Orders ............................................................... 117
Setting Up Allocation of Only Fully Filled Orders ....................................... 117
 Manually Deactivating Allocation of Only Fully Filled Orders in ENOR..... 119
Allocating by Minimum Level 2, 3 and 4 Values........................................... 119
Setting Up Your Item Minimum Shipping Level Parameters...................... 121
Performing Item Minimum Shipping Level Allocation................................. 125
Reserving a Minimum Level of Inventory for High Priority Orders ............ 125
Setting Up a Minimum Level of Inventory .................................................. 125
Assigning Priority Levels to Orders in ENOR............................................. 127
PICK LINES AND REPLENISHMENT .......................................... 129
Overview .......................................................................................................... 131
Types of Pick Lines.................................................................................... 133
Working With Multiple Pick Line Locations for the Same Product ............. 133
Setting Up a Fixed Position Pick Line........................................................... 134
1 — Setting the Activate Directed Move Stock Flag in COMP................... 134
2 — Setting the Assign Location Flag in DIFP........................................... 135
3 — Setting Up Your Picking Profile in PIPR ............................................. 135
4 — Setting Up Your Replenishment Options in DSRP............................. 139
5 — Setting Up Your Location Type in LOTP ............................................ 141
6 — Assigning Your Location Type to Your Pick Line Locations in LOCA 141
7 — Defining Your Picking Parameters for Replenishment in ILOP .......... 142
8 — Setting Up Your Pick Line in PIIT ....................................................... 143
9 — Activating Your Pick Line Using ENOR/REPI..................................... 150
Setting Up a Floating Pick Line ..................................................................... 151
Mixing Fixed Position and Floating Locations in the Same Pick Line....... 153
Setting Up a Pick Line With Replenishment by Inventory Level 2 ............. 154
 Entering Orders in ENOR ......................................................................... 156
Putting Away to a Pick Line Using Directed Put-Away................................ 156
1 — Setting Up Your Location Type in LOTP ............................................ 157
2 — Setting Up Your Put-Away Profile Code in PUPR .............................. 157
3 — Attaching Your PUPR Profile to DSRP............................................... 159
4 — Setting Up Your Overflow Locations in PIIT (Optional) ...................... 160
5 — Defining Your Put-Away Rules in ILOP .............................................. 161
Performing Your Replenishments ................................................................. 162

iv 4.2 ALLOCATION AND WAVE MANAGER
Running the Relocate to Pick Line Audit (RPAU) ...................................... 162
Confirming Your Replenishments in REPI ................................................. 163
Looking Up a Replenishment in LOEN ...................................................... 164
Generating Top Up Replenishments in TURE ........................................... 165
Deleting a Replenishment.......................................................................... 166
Deleting an Order that Triggered a Replenishment ................................... 167
Confirming Your Replenishments in RFRP (RF Only) ............................... 167
Overriding Replenishment Priorities in RFRO ........................................... 172
Troubleshooting Pick Lines and Replenishments....................................... 173
Reports............................................................................................................. 173
DIRECTED MOVE SYSTEM ....................................................... 175
Overview .......................................................................................................... 176
Setting Up the Directed Move System .......................................................... 177
Activating Directed Move in COMP............................................................ 178
Setting Up Your Hold Code(s) in HOLD..................................................... 178
Setting Up Your Directed Move Profile Code in DMPA ............................. 179
Attaching Your Directed Move Profile Code to a Warehouse in WARE .... 181
Setting Up Your Directed Move Parameters in ILOP................................. 182
Setting the Directed Put-Away and Staging Flags in LOTP....................... 184
Assigning Suggested Locations for a Directed Move in DMPR ................. 185
Printing Labels for a Directed Move.............................................................. 188
Printing the Directed Move Report (DMVR) .................................................. 189
Removing Suggested Locations for a Directed Move ................................. 190
Confirming the Directed Move ....................................................................... 190
Confirming the Directed Move in RELO..................................................... 191
Confirming the Directed Move in RFRL ..................................................... 193
Looking Up Directed Moves in LOEN............................................................ 194
Pallet Restacking ............................................................................................ 195
Opportunistic Cross-Docking ........................................................................ 197
“Ship In Given Hour” Option....................................................................... 198
Setting Up Opportunistic Cross-Docking (M7010-21, M7040-43).............. 199
Setting Up Opportunistic Cross-Docking (M7030) ..................................... 200
Attaching a Shipping Lane to an Order in ENOR....................................... 201
WAVE MANAGER .................................................................... 203
Overview .......................................................................................................... 205
Waves vs. Templates................................................................................. 206
Setting Up Label Printing ............................................................................... 207
Setting Up Your Wave Deallocation Rule in CUST....................................... 209
Launching Wave Manager.............................................................................. 210
Working With Pick Lists and the Column Manager ..................................... 212

ALLOCATION AND WAVE MANAGER 4.2 v
Selecting Multiple Values in a Filter Pick List............................................. 212
Working With the Column Manager ........................................................... 214
Creating a New Template ............................................................................... 215
Setting Your Wave Preferences................................................................. 221
Modifying a Template................................................................................. 222
Updating a Template.................................................................................. 222
Deleting a Template................................................................................... 223
Looking Up the Generated SQL for a Query.............................................. 223
Creating a Custom SQL Filter.................................................................... 224
Running a Wave .............................................................................................. 224
Running a Wave From an Unsaved Template........................................... 225
Searching for a Wave ................................................................................ 226
Looking Up Orders on a Wave................................................................... 226
Deleting Orders From a Wave ................................................................... 227
Deallocating Orders by Wave in DOWA .................................................... 227
Time-Stamping and Confirming a Wave in CHOF ..................................... 228
Deleting a Wave......................................................................................... 229
Looking Up a Wave’s Completion Status................................................... 229
Looking Up a Wave’s Job History .............................................................. 229
Looking Up Your Print Job Details ............................................................. 230
Generating a Wave Summary Report........................................................ 231
Generating a Wave Details Report ............................................................ 232
Reprinting Wave Labels............................................................................. 233
Looking Up an Order’s Wave Number in LOOR ........................................ 233
Scheduling a Template ................................................................................... 235
Searching for a Scheduled Template......................................................... 236
Searching for a Scheduled Job.................................................................. 237
Performing a Shortcut Search.................................................................... 238
Editing a Scheduled Template ................................................................... 239
Deleting a Scheduled Template................................................................. 239
Looking Up a Scheduled Template’s Job History ...................................... 240
Paper-Based Tracking .................................................................................... 240
INDEX ................................................................................... 241

vi 4.2 ALLOCATION AND WAVE MANAGER

ALLOCATION AND WAVE MANAGER 4.2 1
INTRODUCTION
AccellosOne 3PL Documentation Set ............................................................... 2

INTRODUCTION
AccellosOne 3PL Documentation Set
AccellosOne 3PL Documentation Set
The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide
allocation setup, inbound and outbound allocation, pick lines and replenishment, 
reserve logic and Wave Manager
Billing and Invoicing 
Guide
billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup 
invoicing and billing/invoicing reports
Core Documents 
Guide
core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting 
reports
Guide to ActiveDesktop/A13PLlogging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your 
company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide
core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating 
product, entering hold adjustments
Operations 2 Guide appointment planner, back orders, batch picking, manual packing, customer relationship management, EDI, faxing and auto-printing, item substitution, kitting, labor tracking, Operational Board, pallet control, inventory attributes, item process values, 
outbound load building, quick response labels
Physical Inventory 
Guide
setup and operational programs for physical inventory as well as the physical inventory reports
RF Guide setup programs for RF (Radio Frequency), RF receiving, RF picking, entering process values in RF, voice-activated picking, order assignment system, equipment 
tracking, interleaving, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory 
level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

ALLOCATION AND WAVE MANAGER 4.2 3
INBOUND ALLOCATION
Overview .............................................................................................................. 4
Item Location Profile for Put-Away (ILOP)........................................................ 4
Understanding Directed Put-Away................................................................. 4
Standard Logical Groups for Put-Away.......................................................... 5
Field Descriptions (ILOP)............................................................................. 20
Setting Up a New Profile in ILOP for Directed Put-Away............................. 23
Overriding the ILOP Profile for Individual Receipt Lines in ENRE ............... 26
Attaching a Velocity Code to the ILOP Profile ............................................. 27
Item Receipt Hold Profile Code (IRHP)............................................................ 29
Put-Away Profile Code (PUPR) ........................................................................ 31
Activating Directed Put-Away .......................................................................... 34
Deactivating Directed Put-Away for Selected Receipts................................. 34
Setting Up Directed Put-Away Deactivation................................................. 35
Processing Receipts With Directed Put-Away Deactivation Turned On ...... 36
Looking Up Skipped Receipt Lines in LORE ............................................... 38
Put-Away by Warehouse Zone......................................................................... 38
WHZO (Warehouse Zone Codes)................................................................ 38
ITEM (Item Code) ........................................................................................ 39
Zone Code Group (ILOP)............................................................................. 40
Put-Away by Location Size .............................................................................. 40
Setup in LOCS ............................................................................................. 41
Setup in LOCA ............................................................................................. 42
Setup in ILOP............................................................................................... 42
Sort Sequences and Proximity Logic for Last Location Used Group.......... 42
LOCA (Locations) ........................................................................................ 42
WARE (Warehouse and Location Format) .................................................. 43
Item Put-Away Parameters (IPUP) ................................................................... 44

INBOUND ALLOCATION
Overview
Overview
There are two main put-away programs in AccellosOne 3PL: ILOP (Item Location Profile) and IRHP (Item 
Receipt Hold Profile Code).
ILOP is the most flexible option for putting away product. You can select from a number of logical groups 
when defining your put-away rules. You can have AccellosOne 3PL assign locations based on isolator zones, 
the size of the location, the location’s hold code, whether the location is empty or partially filled, whether the 
location was the last location used for a particular item, etc.
IRHP is a much more limited put-away program. If there is an exact match between the item’s hold code and 
the location’s hold code, AccellosOne 3PL will assign the item to that location and normal ILOP processing 
will be bypassed.
Item Location Profile for Put-Away (ILOP)
In this program, you define the algorithms that you want AccellosOne 3PL to use when it performs directed 
put-away. You can have the system assign locations based on isolator zones, the size of the location, whether 
the location is empty or partially filled and other criteria that you specify. In ILOP you define the following:
 the isolator zone to which the product belongs
 the overflow warehouse for the product
 the overflow location for the product in the overflow warehouse
 the algorithms that you want the system to use for the put-away of this product 
You can set up as many different profiles as you need. Generally speaking, however, you would set up one 
profile for each isolator zone. Depending on how you defined your isolator zones, you would have one ILOP 
profile for each group of products, each group of customers, a specific product, a specific customer, etc. If you 
have an isolator zone (for example, MEAT OVERFLOW) that is used strictly as an overflow area, no profile 
would be required for this isolator zone.
The profile that you create in ILOP is attached to ITEM.
UNDERSTANDING DIRECTED PUT-AWAY
In directed put-away, you want to place product in the best possible location. If the best possible location is 
not available, you want to place it in the next best location and so on and so forth. In ILOP, you tell the system 
the criteria that you wish it to use for the purpose of identifying the best and the next best locations.
You define your criteria by means of sequences. Each sequence contains a number of parameters for 
selecting a location. The following example shows five sequences that progressively define increasingly less 
desirable locations.
Sample Sequences for Selecting Locations
Sequence 1
(ideal)
Use only exact match isolator code
Use only empty locations
Fill location to maximum capacity

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 5
In sequence 1, which contains the strictest selection criteria, the system searches for a location that satisfies 
all the parameters. If it finds such a location, the product is allocated and the other sequences are never run. 
If the system is unable to find a location, it proceeds to sequence 2.
In sequence 2, which is less strict, the system searches for a location that satisfies all the parameters. If it 
finds such a location, the product is allocated and the other sequences are never run. If the system is unable 
to find a location, it proceeds to sequence 3.
In sequences 3, 4 and 5, the system continues to search for a location that satisfies all the parameters. If the 
system is unable to find a location in any of these sequences, it will allocate the product to the overflow 
location designated in ILOP.
STANDARD LOGICAL GROUPS FOR PUT-AWAY
There are 24 logical groups in ILOP. Each group has two or more mutually exclusive options. From each 
group, you select the appropriate option. If you do not wish to use a particular group, select the first option in 
the group to deactivate it. For example, if you do not wish to use the Hold codes group, you would select the 
first option, “Ignore hold codes in location”.
ISOLATOR GROUP (I0500)
Sequence 2
(next best)
Use only exact match isolator code
Use any empty or partially filled location
Fill location to maximum capacity
Sequence 3
(next best)
Use any overflow isolator code
Use only empty locations
Fill location to maximum capacity
Sequence 4
(next best)
Use any overflow isolator
Use any empty and/or partially filled location
Fill location to maximum capacity
Sequence 5
(worst)
Ignore isolator codes
Use any empty and/or partially filled location
Fill location to maximum capacity
TIP You can define up to nine passes or sequences in any given profile. It is important to bear in mind, however, that each sequence requires time to perform the specified searches to validate locations. Therefore, you must strike a balance between the 
requirement to place product in the best possible location using many sequences and 
the requirement to put product away in a reasonable time.
ignore isolator codes Do not use isolator codes for determining a put-away location.
use only exact match isolator code Match the item isolator with the location isolator. This is a method 
for keeping similar product together and dissimilar product apart.
Sample Sequences for Selecting Locations

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ZONE CODE GROUP (I0600)
EMPTY AND/OR PARTIALLY FILLED LOCATION GROUP (I1000)
PARTIALLY FILLED LOCATION GROUP (I1500)
use any overflow isolator code Place product in the overflow isolators which have been attached 
to the product isolator. A product may have many overflow isolators. The system will try to place the product in the first overflow 
isolator and then move on to other isolators if necessary.
ignore zone codes Do not use zone codes for determining a put-away location.
use only exact match zone code Match the item zone code with the location zone code. 
use first overflow zone code Place product in the first overflow zone that has been attached to 
the product’s warehouse zone. 
use first & second overflow zone code Place product in either the first or second overflow zone that has 
been attached to the product’s warehouse zone. 
use first, second & third zone code Place product in either the first, second or third overflow zone that 
has been attached to the product’s warehouse zone. 
use any overflow zone code Place product in any overflow zone that has been attached to the 
product’s warehouse zone. A product may have many overflow 
zones. The system will try to place the product in the first overflow 
zone and then move on to other zones if necessary.
use any empty and/or partially filled 
location
Place product in an empty or partially filled location. If inventory is 
placed in a partially filled location, the system will only place inventory if the inventory meets the criteria that you select in the next 
group (Partially Filled Location Group).
use only empty locations Place product only in locations that are empty. If you select this 
option, you must select “use any partially filled location regardless 
of what is there” from the Partially Filled Location Group.
use only partially filled locations Place product only in locations that are partially filled — provided 
that the criteria in the next group (Partially Filled Location Group) 
are also met.
use any partially filled location regardless of what is there
For those items that are being placed in partially filled locations, 
place inventory in locations regardless of what inventory is already 
being stored in the location.
use partial locations which have only 
the same entity of level 1
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same item and no other item (customer may differ).

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 7
partial locations, only the same level 1 
and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same entity of level 2
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same level 2 and no other level 2 (customer and level 1 may differ).
partial locations, only the same level 1/
2 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same entity of level 3
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same level 3 and no other level 3 (customer and other levels may 
differ).
partial locations, only the same level 1/
2/3 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same entity of level 4
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same level 4 and no other level 4 (customer and other levels may 
differ).
partial locations, only the same level 1/
2/3/4 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same depositor code 
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer and no other customer.
use partial locations which have only 
the same entity up to level 1
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer and item and no other customer or item.
partial locations, at least same level 1 
and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same entity up to level 2
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item and level 2 (lot number, date code, etc.) and 
no other customer/item/level 2.
partial locations, at least same level 1/2 
and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have only 
the same entity up to level 3
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item, level 2 and level 3 (pallet ID, etc.) and no 
other customer/item/level 2/3.
partial locations, at least same level 1/
2/3 and match PUPR date range
Same as previous but must also match PUPR date range.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I2000)
use partial locations which have only 
the same entity up to level 4
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item, level 2, level 3 and level 4 and no other customer/item/level 2/3/4.
partial locations, at least same level 1/
2/3/4 and match PUPR date range
Same as previous but must also match PUPR date range.
use partial locations which have at 
least the same depositor code
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer.
use partial locations which have at 
least the same entity up to level 1
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer and item.
use partial locations which have at 
least the same entity up to level 2
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item and level 2 (lot number, date code, etc.).
use partial locations which have at 
least the same entity up to level 3
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item, level 2 and level 3 (pallet ID, etc.).
use partial locations, at least same 
level 1/2/3 and match PUPR date 
range
Same as previous but must also match PUPR date range.
use partial locations which have at 
least the same entity up to level 4
For those items that are being placed in partially filled locations, 
place inventory in locations that already have inventory for the 
same customer, item, level 2, level 3 and level 4.
use partial locations, at least same 
level 1/2/3/4 and match PUPR date 
range
Same as previous but must also match PUPR date range.
ignore on receipt when calculating 
capacity by quantity
When calculating capacity by quantity, do not take into account 
inventory on receipt (that is unconfirmed receipts). 
EXAMPLE
You put unconfirmed product in location x, which was previously 
empty (on-hand = 0). If you specify the ignore on receipt option, the 
system will not add the on-receipt quantities to the on-hand quantities when evaluating the location’s capacity; as a result, location x 
will be considered empty and the system will either assign this 
location (if empty locations were specified) or assign another location (if partially filled locations were specified and other criteria are 
met).

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 9
IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY WEIGHT 
GROUP (I2200)
Put-away by weight must be activated in the Company Parameters Block of COMP (Company Code). 
IGNORE/USE ON RECEIPT WHEN CALCULATING CAPACITY BY CUBE GROUP 
(I2300)
IGNORE/USE IN TRANSIT WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I2500)
use on receipt when calculating capacity by quantityWhen calculating capacity by quantity, do take into account unconfirmed receipts. 
EXAMPLE
You put unconfirmed product in location x, which was previously 
empty (on-hand = 0). If you specify the use on receipt option, the 
system will add the on-receipt quantities to the on-hand quantities 
when evaluating the location’s capacity; as a result, location x will 
be considered filled or partially filled and the system will start 
assigning product to another locations (if empty locations were 
specified) or assign product to this location (if partially filled locations were specified and other criteria are met).
ignore on receipt when calculating 
capacity by weight
When calculating capacity by weight, do not take into account 
inventory on receipt (that is unconfirmed receipts). 
use on receipt when calculating capacity by weightWhen calculating capacity by weight, do take into account unconfirmed receipts. 
ignore on receipt when calculating 
capacity by cube
When calculating capacity by cube, do not take into account inventory on receipt (that is unconfirmed receipts). 
use on receipt when calculating capacity by cubeWhen calculating capacity by cube, do take into account unconfirmed receipts. 
ignore in transit when calculating 
capacity by quantity
When calculating capacity by quantity, do not take into account 
inventory in transit (that is, being transported to the warehouse). 
use in transit when calculating capacity 
by quantity
When calculating capacity by quantity, do take into account inventory in transit (being transported to the warehouse). 

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
IGNORE/USE IN TRANSIT WHEN CALCULATING CAPACITY BY CUBE GROUP 
(I2700)
IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY QUANTITY 
GROUP (I300)
IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY WEIGHT 
GROUP (I3200)
Put-away by weight must be activated in the Company Parameters Block of COMP (Company Code). 
ignore in transit when calculating 
capacity by cube
When calculating capacity by cube, do not take into account inventory in transit (that is, being transported to the warehouse). 
use in transit when calculating capacity 
by cube
When calculating capacity by cube, do take into account inventory 
in transit (being transported to the warehouse). 
ignore on order when calculating 
capacity by quantity
When calculating capacity by quantity, do not take into account 
inventory on order.
EXAMPLE
You have 10 cases in location x which are on order but not picked 
or confirmed. If you specify the ignore on order option, the system 
will ignore the product’s on-order status when evaluating the location’s capacity. As a result, it will consider location x to be full and 
will place product in another location.
use on order when calculating capacity 
by quantity
When calculating capacity by quantity, do take into account inventory on order. 
EXAMPLE
You have 10 cases in location x which are on order but not picked 
or confirmed. If you specify the use on order option, the system will 
subtract the on-order quantity from the on-hand quantity when 
evaluating the location’s capacity. As a result, it will consider location x to be empty and will allocate product to that location.
ignore on order when calculating 
capacity by weight
When calculating capacity by weight, do not take into account 
inventory on order (that is unconfirmed orders). 
use on order when calculating capacity 
by weight
When calculating capacity by weight, do take into account unconfirmed orders. 

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 11
IGNORE/USE ON ORDER WHEN CALCULATING CAPACITY BY CUBE GROUP 
(I3300)
IGNORE/USE OUTSTANDING MOVES/RELOCATES WHEN CALCULATING 
CAPACITY BY QUANTITY GROUP (I3500)
Outstanding moves/relocates refers to product that has been moved by means of a directed move.
IGNORE/USE OUTSTANDING MOVES/RELOCATES WHEN CALCULATING 
CAPACITY BY CUBE GROUP (I3600)
Outstanding moves/relocates refers to product that has been moved by means of a directed move.
FILL LOCATION GROUP (I3800)
HOLD CODE GROUP (I4000)
ignore on order when calculating 
capacity by cube
When calculating capacity by cube, do not take into account inventory on order (that is unconfirmed orders). 
use on order when calculating capacity 
by cube
When calculating capacity by cube, do take into account unconfirmed orders. 
ignore outstanding moves/ relocates 
when calculating capacity by quantity
When calculating capacity by quantity, do not take into account 
inventory that is part of an outstanding move or relocate.
use outstanding moves/ relocates 
when calculating capacity by quantity
When calculating capacity by quantity, do take into account inventory that is part of an outstanding move or relocate.
ignore outstanding moves/ relocates 
when calculating capacity by cube
When calculating capacity by cube, do not take into account inventory that is part of an outstanding move or relocate. 
use outstanding moves/ relocates 
when calculating capacity by cube
When calculating capacity by cube, do take into account inventory 
that is part of an outstanding move or relocate.
fill location to maximum capacity Place inventory based on the cube capacity of the location regardless of the standard pallet stack. If activated, this option may 
require you to break a pallet in order to achieve maximum location 
usage.
fill location to full pallet maximum 
capacity only
Place inventory based on the standard pallet stack pattern. Do not 
break a pallet in order to achieve maximum space usage.
ignore location/inventory hold codes Do not use hold codes for determining a put-away location.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
LOCATION SIZE GROUP (I4500)
This option is only available if you have set up location size codes in LOCS (Location Size Codes) and you 
have assigned a location size code to inbound product during receipt entry. Location size codes must be 
activated by HighJump.
In the Empty and/or partially filled location group, you must select “Use only empty locations”.
CUBE CAPACITY GROUP (I5000)
LAST LOCATION USED GROUP (I6000)
The options in this group allow you to give priority to the last location used for a particular item. A location is 
considered to be the “last used” if you have put away, relocated or adjusted a given item into that location 
before or you have assigned that location to the item on a receipt.
use any location with an exact match of 
hold code
Place product in a location only if the hold code on the product 
being put-away matches the location’s hold code and there are no 
other holds in the location. If neither the product being put-away 
nor the location have a hold code and other product already in the 
location is not on hold either, AccellosOne 3PL considers the 
“exact match” condition to be satisfied.
NOTE
Product that is not on hold is not considered an “exact match” for 
this parameter. Therefore, if a location has one pallet on hold ABC 
and one pallet not on any hold, the system will not allocate product 
with hold ABC to this location because the existing product is considered to have mixed hold types.
use any location with a hold code Place product in a location only if the product being put-away and 
the product already stored in the location are both on hold (no 
exact match of hold code required).
ignore location size codes On receipt of inventory, do not use location size codes for determining a put-away location.
use only exact match location size 
codes
On receipt of inventory, match the location size code entered on 
the receipt location line with the location’s location size code. 
use any overflow location size codes On receipt of inventory, place product in any location where the 
location size code assigned to the receipt matches the location’s 
overflow location size code. The system will assign such product in 
the order specified in the Overflow Sequence Number field in 
LOCS.
ignore cube capacity On receipt of inventory, do not use cube capacity for determining a 
put-away location.
fill to 10, 20, 30%, etc. by cube capacity On receipt of inventory, place product in any location in which the 
quantity already in the location is such that that quantity plus the 
new inventory fills the location to the desired capacity. 

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 13
In order to activate this group, you must set the Track Last Used for Put-Away field in LOCA to the appropriate value (F, H, R T or Y) for all locations to which this option applies.
Do not give priority to the last location 
used 
When assigning locations to inventory, do not take into account the 
last location used for the item.
Give priority to the last used location for 
the item
When assigning locations to inventory, give priority to the last location used for the item.
Give priority to the last used location for 
the master item
When assigning locations to inventory, give priority to the last location used for the master item to which the item belongs. A master 
item’s location is the location of the last non-master item received. 
For example, suppose your master item is A and your non-master 
items are A1, A2 and A3. You receive A1 into location 100 and this 
sets the master item’s location to 100 as well. Then you receive A2. 
The last location used for the master item is location 100 and A2 
will be assigned this location as well.
Give priority to the last used location for 
the item then master item
When assigning locations to inventory, give priority to the last location used for the item. If this location is full, give priority to the last 
location used for the master item.
Give priority to the last used location for 
the master item then item
When assigning locations to inventory, give priority to the last location used for the master item. If this location is full, give priority to 
the last location used for the item.
Use last used location for the item 
regardless of capacity
When assigning locations to inventory, give priority to the last location used for the item even if this location is full.
Use last used location for Level 1/2 
regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2 even if this location is full.
Use last used location for Level 1/2/3 
regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3 even if this location is full.
Use last used location for Level 1/2/3/4 
regardless of capacity
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4 even if this location is full.
Use last used location for master item 
regardless of capacity
When assigning locations to inventory, give priority to the last location used for the master item even if this location is full.
Use last used location for the item then 
the master item regardless of capacity
When assigning locations to inventory, give priority to the last used 
location for the item even if the location is full. If there is no last 
location for the item, give priority to the last used location for the 
master item even if the location is full.
Use last used location for the master 
item then the item regardless of capacity
When assigning locations to inventory, give priority to the last used 
location for the master item even if the location is full. If there is no 
last location for the master item, give priority to the last used location for the item even if the location is full.
Use last used location for the same 
receipt
When assigning locations to inventory, give priority to the last location used for any item on the same receipt.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
CALCULATE CAPACITY BY LOWEST/HIGHEST SKU CLASS GROUP (I6500)
OPPORTUNISTIC CROSS-DOCKING GROUP (I7000)
Opportunistic cross-docking allows you to put-away a receipt into a cross-dock location located on your 
receiving/shipping dock rather than into a bulk, rack or pick line location. See “Opportunistic Cross-Docking”
on page 197 for further information on setting up opportunistic cross-docking.
Use last used location for the inventory 
level 1,2
When assigning locations to inventory, give priority to the last location used for inventory level 1,2.
Use last used location for the inventory 
level 1,2,3
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3.
Use last used location for the inventory 
level 1,2,3,4
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4.
Try last used location, aisle, zone for 
the item
When assigning locations to inventory, give priority to the last location used for the item, then the same aisle and then the same zone.
Try last used location, aisle, zone for 
the master item
When assigning locations to inventory, give priority to the last location used for the master item, then the same aisle and then the 
same zone.
Try last used location, aisle, zone for 
inventory level 1,2
When assigning locations to inventory, give priority to the last location used for inventory level 1,2, then the same aisle and then the 
same zone.
Try last used location, aisle, zone for 
inventory level 1,2,3
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3, then the same aisle and then the 
same zone.
Try last used location, aisle, zone for 
inventory level 1,2,3,4
When assigning locations to inventory, give priority to the last location used for inventory level 1,2,3,4, then the same aisle and then 
the same zone.
Try last used location, aisle, zone for 
the receipt
When assigning locations to inventory, give priority to the last location used for the receipt, then the same aisle and then the same 
zone.
calculate capacity by lowest SKU class When calculating capacity by cube, use lowest SKU class and do 
not round up. For example, if there are 10 cases in a pallet and a 
given location contains 22 cases, the quantity in the location will be 
2 pallets and 2 cases.
calculate capacity by highest SKU 
class
When calculating capacity by cube, round up the quantity to the 
highest SKU. For example, if a given location contains 2.1 pallets, 
the quantity will be rounded up to 3 full pallets.
NOTE Each pallet consists of a single inventory entity. If there 
are two lots or pallet ID’s in the same location, each lot or pallet ID 
will be rounded up separately.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 15
BREAK INVENTORY INTO MULTIPLE TO LOCATIONS GROUP (I7500)
This parameter allows you to specify whether or not allocation should split a receipt line (for directed putaway) or a location line (for directed move) into multiple to locations.
CAPACITY GROUP (I8000)
This parameter looks at the total put-away quantity of a receipt line and compares it to the location’s available 
capacity. For example, you have a receipt line of 14 pallets and you want allocation to select a location that 
can hold all 14 pallets.
Allow inventory to break into multiple to 
locations
Ignore the fact that the quantity to be put-away or moved may have 
to be split into multiple to locations.
NOTE
If the inventory that you are putting away or moving is on a hold 
whose Breakable Inventory flag set to N for No, allocation will 
ignore the option that you select in the “Allow inventory to break 
into multiple to locations” group. It will treat the inventory as nonbreakable and search for a location in which the entire quantity can 
be put-away or moved without splitting it into multiple location lines.
Disallow the breaking of inventory into 
multiple to locations
Place product on a location only if the entire quantity can be putaway or moved without splitting the product into multiple location 
lines.
For example, if the quantity to be put-away or moved is 200 cases, 
allocation will search for a location in which the entire 200 cases 
can be put-away or moved. It will not allow the 200 cases to be split 
into two or more location lines. 
put-away to any location that has the 
capacity
Place product in a location if there is any available capacity at all. 
For example, the receipt line is 10 pallets and a given location has 
an available capacity of 2 cases, allocation will assign two cases to 
this location and then look for other locations for the remaining pallets and cases.
put-away to location with matching 
capacity
Place product in a location only if the total put-away quantity is an 
exact match of the location’s available capacity.
put-away to location with matching or 
more capacity
Place product in a location only if the total put-away quantity is less 
than or equal to the location’s available capacity.
put-away to location with matching or 
less capacity
Place product in a location only if the total put-away quantity is 
greater than or equal to the location’s available capacity.
put-away to location starting with the 
highest capacity
Place product in a location starting with the locations with the highest available capacity.
put-away to location starting with lowest capacityPlace product in a location starting with the locations with the lowest available capacity.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
LOCATION HEIGHT GROUP (I8200)
ORDER BY GROUP (I8300)
This group allows you to define the sort sequence for your last used locations/aisle/zone so that closer 
locations are tried first followed by less close locations.
Ignore location height Do not use location height for determining a put-away location.
Use location height, ascending order Place product in a location with the lowest possible height that is 
still high enough to hold the product.
Use location height, descending order Place product in a location with the highest possible height as long 
as it is high enough to hold the product.
Order by Warehouse Code, Location 
Code
The default sort order in AccellosOne 3PL: warehouse code followed by location code.
Order by LOCA Put Sequence Number, 
Warehouse Code, Location Code
Sort by put-away/directed move sort sequence number in LOCA, 
then warehouse code followed by location code.
Order by Warehouse Attribute Proximity Sequence, Warehouse Code, Location CodeSort by proximity sequence number in WARE, then warehouse 
code followed by location code.
Order by Warehouse Attribute Proximity Sequence, LOCA Put Sequence 
Number, Warehouse Code, Location 
Code
Sort by proximity sequence number in WARE, then put-away/
directed move sort sequence number in LOCA, then warehouse 
code followed by location code.
Order by Location Cube Ascending, 
Warehouse Code, Location Code
Sort by location with the smallest cube, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Code, Location Code
Sort by location with the largest cube, then warehouse code followed by location code.
Order by Location Cube Ascending, 
LOCA Put-Away Sequence Number, 
Warehouse Code, Location Code
Sort by location with the smallest cube, then put-away/directed 
move sort sequence number in LOCA, then warehouse code followed by location code.
Order by Location Cube Descending, 
LOCA Put- Away Sequence Number, 
Warehouse Code, Location Code
Sort by location with the largest cube, then put-away/directed move 
sort sequence number in LOCA, then warehouse code followed by 
location code.
Order by Location Cube Ascending, 
Warehouse Attribute Proximity 
Sequence, Warehouse Code, Location 
Code
Sort by location with the smallest cube, then proximity sequence 
number in WARE, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Attribute Proximity 
Sequence, Warehouse Code, Location 
Code
Sort by location with the largest cube, then proximity sequence 
number in WARE, then warehouse code followed by location code.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 17
PRODUCT STACKING GROUP (I8400)
The options in this group allow you to define your product stacking rules. 
You define your stacking rules in ITEM by entering your stackability factor in the Stackability Quantity in 
Highest SKU field. In this field, you define how many layers of the highest SKU code can be stacked up.
For put-away purposes, the stackability factor will be applied to the location capacity. For example, if the 
location capacity is defined as four pallets and the item code has a stackability factor of 2, then the put-away/
directed move engine will consider 8 pallets as the location capacity for this item code. 
Order by Location Cube Ascending, 
Warehouse Attribute Proximity 
Sequence, LOCA Put- Away Sequence 
Number, Warehouse Code, Location 
Code
Sort by location with the smallest cube, then proximity sequence 
number in WARE, then put-away/directed move sort sequence 
number in LOCA, then warehouse code followed by location code.
Order by Location Cube Descending, 
Warehouse Attribute Proximity 
Sequence, LOCA Put-Away Sequence 
Number, Warehouse Code, Location 
Code
Sort by location with the largest cube, then proximity sequence 
number in WARE, then put-away/directed move sort sequence 
number in LOCA, then warehouse code followed by location code.
Do not stack product Do not allow product stacking.
Stack product according to largest 
ITEM stackable setting
If a location contains multiple items, stack product according to the 
stackability settings of the largest item.
Stack product according to smallest 
ITEM stackable setting
If a location contains multiple items, stack product according to the 
stackability settings of the smallest item.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ITEM screen showing stackability factor field
PND LOCATION CAPACITY GROUP (I8700)
This group allows you to skip the final location if the associated PND does not have capacity.
PIIT LOCATION CAPACITY GROUP (I8500)
This group allows you to specify rules for putting away product into pick line locations if and when there is 
capacity for receiving new product. The rules apply to fixed position pick line locations only.
NOTE: The PIIT Location Capacity group looks at the available capacity in the location only. Unlike replenishment, it does not check whether the location’s minimum quantity has been reached.
Ignore PND location capacity Do not check the capacity of the PND location.
Skip final location if associated PND 
does not have capacity
In three-step put-away, if the PND location is full, do not consider 
any final put-away locations attached to that PND location.
Do not give priority to PIIT locations No priority will be given to pick line locations.
Give priority to PIIT locations, no need 
to check FIFO
Priority will be given to pick line locations and FIFO/LIFO rules will 
be ignored.
Give priority to PIIT locations, validate 
FIFO (DSRP, ITEM) requirements
Priority will be given to pick line locations and FIFO/LIFO rules will 
be followed.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 19
ENTIRE DOCK QUANTITY GROUP (I8900)
This group allows you to consider the entire quantity for a given item on the dock when assigning put-away 
locations rather than the quantities of individual receipt lines. For example, you receive multiple receipts 
containing the same item or items at the same time and you wish to group your items on the receiving dock 
for more efficient put-away into a single large location if one is available.
Entire dock quantity receiving must be activated in FLPR by attaching the activity type 89 (Entire Dock 
Quantity Directed Move Inbound) to the appropriate inbound flow. Only receipts at this flow can be grouped 
for entire dock receiving purposes.
FLPR screen showing activity type 89 assigned to inbound flow INST (Inbound Staged)
In the Sequence Block of ITEM in the Entire Dock Quantity field, you specify the maximum number of pallets 
that can be grouped together for entire dock receiving purposes. For example, if you set this maximum to 20 
pallets for your first ILOP sequence and there are 25 pallets of item A on the dock at your entire dock 
receiving flow, the ILOP sequence will fail and directed put-away will attempt to put-away using your second 
ILOP sequence.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ILOP screen showing a maximum quantity of 20 pallets
FIELD DESCRIPTIONS (ILOP)
Ignore Entire Dock Quantity Directed 
Move Inbound
Do not use the entire dock quantity of an item for determining a 
put-away location.
Match Entire Dock Quantity against 
location capacity and go up
Place entire dock quantity product in a location with available 
capacity or greater.
Match Entire Dock Quantity against 
location capacity and go down
Place entire dock quantity product in a location with available 
capacity or less.
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
If you click on the View Flow Chart icon , you can see a flow chart of 
your profile showing each sequence as well as the put-away options for that 
sequence.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 21
Description Mandatory
Your item location profile code description.
Isolator Code (ISOL) Mandatory
The default isolator zone attached to the profile. You can override this default 
in the Sequence Block.
Overflow Warehouse 
Code (WARE)
Mandatory
If you have set up an overflow warehouse in WARE, you enter its code in this 
field. If you have not set up an overflow warehouse, enter your main warehouse code.
Overflow Location Code 
(LOCA)
Mandatory
The overflow location in the warehouse that you specified in the previous field. 
You can specify a location such as an aisle, dock space, etc. or you can set up 
a dummy location called 99999 or ASKSUP in LOCA and use this for all your 
ILOP profiles.
SEQUENCE BLOCK
Sequence Number Mandatory
1, 2, 3, 4, etc.
Each sequence or pass contains the parameters that you specify for selecting a 
location. The sequence numbers that you enter in this field determine the order in 
which sequences are run.
Description Mandatory
Your sequence number description.
FIELD DESCRIPTIONS

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
Warehouse Code Optional
If you specify one or more warehouses in this field, the system will restrict its 
search for a location to the warehouse(s) that you specify. If you leave this field 
blank, the system will search all warehouses.
If required, each sequence can have a different warehouse. For example, 
sequence 1 could search for locations in warehouse 1, sequence 2 could search 
for locations in warehouse 2, sequence 3 could have no warehouse assigned, etc.
You can use the following symbols (=, <, >, etc.) to define one or more warehouses:
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
If you specify one or more locations in this field, the system will restrict its search 
for a location to the location(s) you specify. If you leave this field blank, the system 
will search all locations.
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
This field allows you to temporarily restrict put-away to certain locations or aisles 
when you are reracking your warehouse.
Acceptable Gap Height / 
UOM
The Acceptable Gap Height and UOM fields represent the gap between the product height and location height. If the gap between the product height and the location height for a given location exceeds the acceptable gap, that location will be 
rejected as a suitable put-away location.
SEQUENCE BLOCK

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 23
SETTING UP A NEW PROFILE IN ILOP FOR DIRECTED PUT-AWAY
If you are setting up allocation for non-RF programs, you select your put-away parameters from the Put-Away 
option in the Type Block. If you are setting up allocation for RF programs such as RFCH/RFPU, refer to the 
RF Guide to find out which put-away parameters to use.
1 Enter ILOP.
2 Click on Create Record.
3 Key in an item location profile code and press Enter.
4 Key in a meaningful description for your new code and press Enter.
5 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, 
press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your 
arrow keys to position your cursor over the appropriate code and click on Select Code. 
6 Use your pick list function to select the warehouse code for your overflow warehouse. If you have a single warehouse, use this warehouse.
Quantity Range The Quantity Range field defines an acceptable quantity range between the putaway quantity and the location capacity. The unit of measure is the SKU code 
entered in the Capacity SKU Code field in LOCA. This field works in conjunction 
with the I8000 series of options (“Put-away to any location that has capacity”). 
EXAMPLE 1
Suppose you enter 4 in the Quantity Range field and select I8020 (“Put-away to 
any location with matching or more capacity”). If you are putting 1 pallet of product 
away, the put-away/directed move engine would look for locations with a capacity 
starting with 1 and moving up to 5 (i.e. 1 + 4 = 5). 
EXAMPLE 2
Suppose you enter 2 in the Quantity Range field and select I8030 (“Put-away to 
any location with matching or less capacity”). If you are putting 6 pallets of product 
away, the put-away/directed move engine would look for locations with a capacity 
starting with 6 and moving down to 4 (i.e. 6 - 2 = 4).
Hours See “Opportunistic Cross-Docking” on page 197 for further information.
Entire Dock Quantity See “Entire Dock Quantity Group (I8900)” on page 19 for further information..
Isolator Code If you specify an isolator code in this field, it will override the isolator code in the 
header record.
SEQUENCE BLOCK

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
7 Use your pick list function to select the location code for your overflow location code.
The Type Block will appear. 
Blank Put-Away screen
8 Do one of the following:
9 Click on Sequence Block.
10 When the Selected Options Block appears, key in 1 for your first sequence and press Enter.
11 Key in a description for your first sequence (for example, FIRST PASS) and press Enter.
12 If you wish to restrict the search for locations in this sequence to a particular warehouse, key in the warehouse code and press Enter. If you want to search locations in all warehouses, press Enter to bypass this 
field.
TIP Create a location code in LOCA of 999 or ZZZZZZ and use this as your overflow location (the format of this code must conform to the format that you set up for 
this warehouse in WARE). When the system starts allocating to this location, you 
know that your warehouse is full.
If you are setting up allocation 
for non-RF programs:
If you are setting up allocation 
for RF programs:
a) Use your arrow keys to select the 
Put-Away option in the Type 
Block.
a) Refer to the RF Guide to find out 
which option — Put-Away or 
Directed Move Inbound — to 
select in the Type Block.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 25
13 If you wish to restrict the search for locations in this sequence to particular locations or a range of locations, key in the location codes and press Enter. If you want to search all locations in this sequence, 
press Enter to bypass this field.
You will see the first set of parameters appear in the Available Options Block.
14 If required, enter your acceptable gap height and press Enter. Then key in your UOM and press Enter 
again.
15 If required, enter your quantity range and press Enter.
16 If you wish to override the isolator code in the header for a given sequence, key in your override isolator 
code and press Enter. If you do not wish to override the isolator code in the header, press Enter to 
bypass this field.
17 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you 
wish to choose and then click on Select Option. If you do not wish to use a particular group (for example, 
the Hold code group), select the first option in the group (“Ignore hold codes in location”) to deactivate 
the group.
18 Repeat the previous step for each set of parameters.
19 When you finish entering all your parameters for your first sequence, your cursor will be positioned over 
the last line in the Selected Options Block. Click on Sequence Block.

Sample Put-Away screen after entering sequence 1
20 Repeat steps 10 to 19 for each additional sequence that you wish to set up for your put-away profile.
21 When you finish entering all your sequences, click on Return to Main and then Type Block.
22 Click on Master Block.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)

Item Location Profile
23 Click on Exit to exit the program.
OVERRIDING THE ILOP PROFILE FOR INDIVIDUAL RECEIPT LINES IN ENRE
The operator can override the ILOP profile for an individual receipt line in ENRE. This functionality is available 
in both ENRE and EDI receipts.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 27
ENRE screen showing Location Profile Code field
If there are multiple ILOP profiles that apply to a given receipt line, AccellosOne 3PL will use the following 
override sequence:
 item in ITEM (default and lowest priority)
 shipper (SHIP)
 velocity (IVLP)
 receipt line in ENRE (highest and to be used first when it exists)
ATTACHING A VELOCITY CODE TO THE ILOP PROFILE
You can assign velocity codes to item location profile codes (ILOP) to indicate whether a particular item is fast 
moving or slow moving. For example, you assign the fast moving velocity code to the ILOP profile ABC and 
the slow moving velocity code to the ILOP profile DEF. You then attach your velocity codes to the appropriate 
items in ITEM.
The purpose of velocity codes is to handle seasonal product whose velocity may change depending on the 
time of year. For example, turkey is a fast-moving product at Thanksgiving and a slow-moving product at 
other times of the year.
Rather than enter the ITEM program and change the ILOP profile for dozens or more items, the system 
administrator can enter IVLP and change the ILOP profile once for all items assigned that velocity.

INBOUND ALLOCATION
Item Location Profile for Put-Away (ILOP)
1 Enter IVLP.
2 Click on New.
3 Select your velocity code from the dropdown list.
4 Use your pick list to select the appropriate item location profile.
5 Repeat the above three steps for each additional velocity code that you wish to assign to an item location 
profile.
IVLP screen showing velocity codes assigned to ILOP profiles
FIELD DESCRIPTIONS
Velocity Code Mandatory
Your velocity code. You set up your velocity codes in VELO (Velocity Codes).
Item Location Profile 
(ILOP)
Mandatory
The ILOP profile being assigned a velocity. This profile will override the ILOP 
profile attached directly to the item.

INBOUND ALLOCATION
Item Receipt Hold Profile Code (IRHP)
ALLOCATION AND WAVE MANAGER 4.2 29
6 When you finish assigning velocity codes to item location profiles, click on Save to your changes.
7 Click on Exit to exit IVLP.
Item Receipt Hold Profile Code (IRHP)
In this program, you set up your item receipt hold profile codes. These profile codes allow you to put away 
product based on its hold code. When you receive an item with a hold code attached to it and that hold code 
matches the hold code that you specify in IRHP, the system will put-away that item in the location assigned to 
it in IRHP and bypass normal ILOP processing.
You can attach as many items as you wish to the same receipt hold profile code, but you can only assign a 
single location to any given item/hold code combination. For example, you can assign one location to ITEM 1 
/ HOLD CODE A and another location to ITEM 1 / HOLD CODE B, but you cannot assign two locations to the 
same item/hold code combination.
IRHP is attached to PUPR (Put-Away Profile Code).
FIELD DESCRIPTIONS
Item Receipt Profile Code Mandatory
Your item receipt hold profile code.
Description Mandatory
Your item receipt hold profile description.
Customer Code
(defined in CUST)
Mandatory
The customer code for the item.
Item Code
(defined in ITEM)
Mandatory
Your item code or .ALL for all items belonging to a given customer.
Hold Code
(defined in HOLD)
Mandatory
Your hold code.

INBOUND ALLOCATION
Item Receipt Hold Profile Code (IRHP)
1 Enter IRHP.
2 Key in an item receipt hold profile code and press Enter.
3 Key a description for your new item receipt hold profile code and press Enter.
4 Key in your customer code and press Enter.
5 Key in your item code and press Enter.
6 Key in your hold code and press Enter.
7 Key in your warehouse code and press Enter.
8 Key in your location code and press Enter.

Item Receipt Hold Profile Code showing item A1 with hold QC to be put-away to location A100 and the 
same item with hold BL assigned to location A103
9 Repeat steps 4 to 8 for each additional item that you wish to add to IRHP.
10 When you finish adding your items to the profile, click on Return to Main to exit create mode. Then click 
on Master Block and Exit to exit.
Warehouse Code
(defined in WARE)
Mandatory
The warehouse in which you wish to put-away the item.
Location Code
(defined in LOCA)
Mandatory
The location in which you wish to put-away the item.
FIELD DESCRIPTIONS

INBOUND ALLOCATION
Put-Away Profile Code (PUPR)
ALLOCATION AND WAVE MANAGER 4.2 31
Put-Away Profile Code (PUPR)
In this program, you set up your pick line options for directed put-away and specify whether product with a 
hold attached to it should be diverted to a special location reserved for the hold.
You can specify that product is to be always put-away to the pick line or that only partial quantities are putaway to the pick line. If you select either of these options, the allocation routine will search for pick line 
locations that satisfy the sequences that you set up in ILOP (Put-Away). If this search fails, the allocation 
routine will search for pick line overflow locations that satisfy your ILOP (Put-Away) sequences. If this search 
fails, the allocation routine will search for non-pick line locations that satisfy your ILOP (Put-Away) 
sequences.
If you specify an item receipt hold profile, product with a hold attached to it will be put-away to the location 
assigned to that hold in IRHP instead of to the pick line. 
PUPR is attached to DSRP (Depositor Shipping and Receiving Profile). If you attach a PUPR profile to ITEM, 
that profile will override the customer-level default in DSRP.
FIELD DESCRIPTIONS
Put-Away Profile Code Mandatory
Your put-away profile code.
Description Mandatory
Your put-away profile description.
Put-Away to Pick Line A = Always
P = Partial
N = None
See “Putting Away to a Pick Line Using Directed Put-Away” on page 156 for 
further information..
Pick Line Isolator Code 
(ISOL)
Optional
See “Putting Away to a Pick Line Using Directed Put-Away” on page 156 for 
further information..

INBOUND ALLOCATION
Put-Away Profile Code (PUPR)
Range in Days from Oldest Lot
Optional
This range in days applies to those options in the Partially Filled Locations 
group in ILOP that contain a “match PUPR date range” restriction. For example, if you select “Partial locations, at least same level 1 and match PUPR date 
range”, directed put-away will only select a location if both the inventory level 
requirements (“same level 1”) and the PUPR date range requirements are satisfied.
Range Based on Only available if the Range in Days from Oldest Lot field is populated
EXDT = Expiry Date
EXMO = Expiry Date Within 1 Month
RCDT = Receipt Date
The type of date that your range in days is based on.
Sort Sequence Code 
(SOSE)
Optional
This field allows you to specify how you want the allocation routine to resolve 
tie-breaking situations. For example, suppose you specify the following three 
put-away parameters in ILOP:
 use only exact match isolator code
 use only empty location
 fill location to maximum capacity
When you run allocation, the system finds three locations that meet the above 
criteria: A2, C6 and F4. A sort sequence code allows you to specify which of 
these three locations you wish to pick from. You set up sort sequence codes in 
SOSE in the form of SQL order by statements.
If you do not specify a sort sequence code for your picking profile, the allocation routine will select the “lowest” location — in the example above, A2.
FIELD DESCRIPTIONS

INBOUND ALLOCATION
Put-Away Profile Code (PUPR)
ALLOCATION AND WAVE MANAGER 4.2 33
1 Enter PUPR.
2 Click on Create Record.
3 Key in your put-away profile code and press Enter.
4 Key in a description for your new put-away profile code and press Enter.
5 In the Put-Away to Pick Line field, press Enter to accept the default value of N for None.
6 If required, key in an isolator profile code and press Enter or press Enter with the field blank to bypass 
this option.
7 If required, key in a range in days from oldest lot value and then select the appropriate range based on 
code: EXDT for Expiry Date, EXMO for Expiry Date Within 1 Month or RCDT for Receipt Date.
8 If required, key in a sort sequence code and press Enter or press Enter with the field blank to bypass this 
option.
9 If required, key in an item receipt hold profile code and press Enter or press Enter with the field blank to 
bypass this option.
10 If you entered an item receipt hold profile code in the previous field, key in the appropriate override option 
(Y for Yes or N for No) and press Enter.
Item Receipt Hold Profile 
Code (IRHP)
Optional
If you enter an item receipt hold profile code, the system will check each 
receipt line for a hold code. If the receipt line has a hold code and if the receipt 
line hold code matches a hold code in IRHP, the system will attempt to putaway the receipt line in the location assigned that hold in IRHP.
This field overrides the pick line options that you specify in the Put-Away to 
Pick Line field.
Item Receipt Hold Override
Only available if you enter an item receipt hold profile code
Y = Yes
N = No
This field governs the way in which the system will put-away product with a 
hold that cannot be put-away in the location specified in IRHP. If you select Y 
for Yes, the system will allocate the item to the overflow locations that you 
specify in ILOP. If you select N for No, the item will undergo normal ILOP processing and will be assigned a location by that program.
FIELD DESCRIPTIONS

INBOUND ALLOCATION
Activating Directed Put-Away

PUPR screen showing put-away profile P1 that will put-away product according to the location and 
hold code defined in IRHP
11 When you finish setting up your put-away profile code, click on Return to Main and then Exit to exit.
Activating Directed Put-Away
Four conditions must be met before directed put-away is activated:
 the Assign Location flag must be set to Yes for an inbound flow code in DIFP
 an inbound document must be set up to print in DIFP (unless you put-away using an RF program)
 the Activate Directed Put-Away flag in the Company Parameters Block of COMP must be set to Yes
 your put-away locations must be assigned a location type in LOTP whose Directed Put-Away flag has 
been set to Yes
Deactivating Directed Put-Away for Selected Receipts
You can deactivate directed put-away for selected receipts by means of the special verify program SSDP 
(Skip Directed Put-Away). Deactivating directed put-away for selected receipts is useful when some products 
in your warehouse require special handling before final put-away. 

INBOUND ALLOCATION
Deactivating Directed Put-Away for Selected Receipts
ALLOCATION AND WAVE MANAGER 4.2 35
For example, suppose certain items require blast freezing before putting away to the normal freezer storage 
area of your warehouse. You would deactivate directed put-away for these items and place them directly in 
the blast freezing locations. Once blast freezing was complete, you could move them manually to the normal 
freezer storage area or you could perform a directed move.
SETTING UP DIRECTED PUT-AWAY DEACTIVATION
You set up directed put-away deactivation by attaching the specify verify program SSDP to the flow before 
directed put-away is called in your inbound workflow profile.
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

INBOUND ALLOCATION
Deactivating Directed Put-Away for Selected Receipts

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
3 When you reach the flow to which you attached the specify verify program SSDP, the following screen 
will appear.
NOTE When putting away a load in RFPU containing mixed lines (that is, some 
lines were skipped while others were put-away using directed put-away), skipped 
lines may show a system-assigned location. If this happens, exit RFPU and then reenter the program. The Location field will now be blank for all skipped lines.

INBOUND ALLOCATION
Deactivating Directed Put-Away for Selected Receipts
ALLOCATION AND WAVE MANAGER 4.2 37

CHRF screen showing receipt with three lines
4 Do one of the following:

CHRF screen showing two lines to be skipped
5 Continue to process the receipt normally in CHRF.
To skip all lines: To skip individual lines:
To perform no skipping (that 
is, put-away all lines):
a) Click on Skip All. a) Key in Y for Yes for each line 
that you wish to skip and 
press Enter. If you enter N for 
No or leave the field blank, the 
line will NOT be skipped.
b) When you finish skipping individual lines, click on Exit.
a) Click on Exit.

INBOUND ALLOCATION
Put-Away by Warehouse Zone
LOOKING UP SKIPPED RECEIPT LINES IN LORE
A record is created in the Time Stamping Block of LORE whenever you skip a receipt line in CHRF. The 
record is attached to the flow before your SSDP special verify program.
If you skip individual lines in CHRF, a record will be created for each line skipped; for example, “Driver at Door 
# 1”, “Driver at Door # 2”, etc. If you skip all lines in CHRF, a single record will be created in the Time 
Stamping Block with a line number of zero; for example, “Driver at Door # 0”.
1 Enter LORE.
2 Retrieve the receipt that you wish to look up.
3 Click on Time Block.

LORE screen showing two skipped lines on receipt 1459 (lines 1 and 3)
4 If required, use your arrow keys to scroll through the records in the Time Stamping Block.
5 When you finish looking up your receipt, click on Master Block and Exit to exit.
Put-Away by Warehouse Zone
There are three setup programs for put-away by warehouse zone: WHZO, ITEM and ILOP. 
WHZO (WAREHOUSE ZONE CODES)
If product cannot be put-away in a given warehouse zone, you can define an overflow sequence for 
warehouse zones in the Overflow Sequence Block. The overflow zones must have the same zone type code 
as the header zone.
Warehouse zones used in directed put-away require a zone type code of D (for Directed Put-Away).

INBOUND ALLOCATION
Put-Away by Warehouse Zone
ALLOCATION AND WAVE MANAGER 4.2 39
WHZO screen showing overflow zone codes
ITEM (ITEM CODE)
The Zone Code field in ITEM defines the exact match zone code for an item. You can override this exact 
match warehouse zone for a given item by entering records in the Override ISOL Zone Block. In this block, 
you define specific warehouse zones for specific isolator codes and hold codes.
For example, if product is on QA hold, it is directed to locations in warehouse zone TDRY assigned the 
isolator code DRY.
ITEM screen showing Override Block

INBOUND ALLOCATION
Put-Away by Location Size
ZONE CODE GROUP (ILOP)
The following options in the zone code group allow you to define your zone code rules in the same way that 
you define your isolator rules.
 Ignore zone codes
 Use only exact match zone code
 Use first overflow zone code
 Use first & second overflow zone code
 Use first & second and third overflow zone code
 Use any overflow zone code
ILOP screen showing zone code group
Put-Away by Location Size
You can put-away by location size when you receive pallets whose size (that is, the number of cases on the 
pallet) is unknown. You use location size codes to define the relative size of a location (large, medium, small, 
etc.). When you receive product, you attach the appropriate location size code to each location line in ENRE. 
During directed put-away, AccellosOne 3PL will attempt to place the product in a location whose location size 
code matches the location size code assigned to the receipt line.
You can define overflow sequences for your location size codes. If AccellosOne 3PL is unable to find a 
location whose location size code is an exact match of the product’s location size code, it will search for 
locations assigned the location size code or codes specified as overflow sizes. 

INBOUND ALLOCATION
Put-Away by Location Size
ALLOCATION AND WAVE MANAGER 4.2 41
Location sizes must be activated on your system by HighJump and require setup of the appropriate put-away 
parameter in ILOP (Item Location Profile).
SETUP IN LOCS
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
Overflow Sequence Number
Optional
The sequence number for your overflow location size code.
Overflow Location Size 
Code
The overflow location size code for the sequence number that you entered in 
the Overflow Sequence Number field.
If you wish to set up an overflow 
location size code for your new 
code:
If you do NOT wish to set up an 
overflow location size code for 
your new code:
a) Key in a sequence number and 
press Enter.
b) Key in a location size code for 
the sequence and press Enter.
c) Repeat the above steps for each 
additional sequence that you 
wish to set up.
d) Click on Master Block.
a) Click on Master Block.

INBOUND ALLOCATION
Sort Sequences and Proximity Logic for Last Location Used Group
LOCS screen showing two overflow location sizes for Small locations
6 If you wish to create another location size code, click on Create Record and repeat the above steps for 
each additional code that you wish to add. When you finish adding all your codes, click on Return to Main 
to exit create record mode.
7 When you finish creating your location size codes, click on Exit to exit the program.
SETUP IN LOCA
Your location size codes set up in LOCS must be attached to the appropriate locations in LOCA.
SETUP IN ILOP
See “Location size group (I4500)” on page 12.
Sort Sequences and Proximity Logic for Last Location Used Group
If you put-away by last location used (ILOP) for a given level 1/level 2, you can extend the last location used 
logic to include the last bay used and then the last aisle used. For example, try the last location used first; if 
that location is full, try locations in the last bay used. If no location in the last bay used is available, try 
locations in the last aisle used.
When searching for locations in the last bay used and the last aisle used, you can define specific sort 
sequences for these locations so that the RF operator will try closer locations first and then try locations that 
are further and further away from the last location used. Ideally, you wish to put-away product in the last 
location used for that item/level 1/level 2. However, if that is not possible, you wish to put-away in the same 
bay, aisle and warehouse zone.
LOCA (LOCATIONS)
The Put-Away/Directed Move Sort Sequence field allows you to maintain specific sort sequences for putaway and directed move sorting. These sort sequences offer greater flexibility than the default alphanumeric 
sort sequence by location code. The Put-Away Directed Move Sort Sequence field is referenced in those 
options in the Order By group in ILOP that contain the LOCA Put-Away Sequence Number. 

INBOUND ALLOCATION
Sort Sequences and Proximity Logic for Last Location Used Group
ALLOCATION AND WAVE MANAGER 4.2 43
For example, suppose you select “Order by LOCA Put-Away Sequence Number, Warehouse Code, Location 
Code” in ILOP and you have three locations: 
 A100 (sequence number = 2) 
 B100 (sequence number = 3) 
 C100 (sequence number = 1)
Allocation will attempt to put-away to location C100 first, then location A100 and last location B100. 
LOCA screen showing location A100 assigned a sequence number of 10
WARE (WAREHOUSE AND LOCATION FORMAT)
The Proximity Sequence # field and the Exclude/Include flag in the Location Attribute Block allow you to 
define how close any given location is to the last location used for put-away (ILOP options 6010 to 6095). 
Proximity logic is only activated if you select an option in the Order By group in ILOP containing the parameter 
Warehouse Attribute Proximity Sequence. For example, “Order by Location Cube Ascending, Warehouse 
Attribute Proximity Sequence, Warehouse Code, Location Code”.
FIRST PASS: PROXIMITY SEQUENCE NUMBER = 1 FOR BAY
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Exclude FA105, FA205, FA305, … FAX05, FAY05, FAZ05, 
etc.
DESCRIPTION: In the first pass, directed put-away searches for locations whose first two characters are “FA” (aisle) and last two 
characters are “05” (slot). The third character (bay) can be any character; that is, search for any bay in the current aisle and current 
slot.

INBOUND ALLOCATION
Item Put-Away Parameters (IPUP)
WARE screen showing Location Attributes Block
Item Put-Away Parameters (IPUP)
This program is a simplified version of ITEM. It allows you to update the following for a given customer/item 
without entering ITEM:
SECOND PASS: PROXIMITY SEQUENCE NUMBER = 2 FOR SLOT
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Exclude FA105, FA205, FA305, … FAX05, FAY05, FAZ05, 
etc.
DESCRIPTION: In the second pass, directed put-away searches for locations whose first two characters are “FA” (aisle) and third 
character is “0” (bay). The last two characters (slot) can be any character; that is, search for any slot in the current aisle and bay.
THIRD PASS: PROXIMITY SEQUENCE NUMBER = 3 FOR AISLE
LAST USED LOCATION FOR ITEM EXCLUDE/INCLUDE ACCEPTABLE LOCATIONS
FA005 (“FA” = aisle, “0” = bay and “05” = slot) Include FA000, FA001 ... FA101, FA102 ... FA971 … FA9A0 
… FA9X4 … FAC00, FAC01 … FAH77, FAH78 … 
FAZZ1 … FAZZZ, etc.
DESCRIPTION: In the third pass, directed put-away searches for locations whose first two characters are “FA” (aisle). The last three 
characters (bay and slot) can be any character; that is, search for any bay or slot in the current aisle.

INBOUND ALLOCATION
Item Put-Away Parameters (IPUP)
ALLOCATION AND WAVE MANAGER 4.2 45
 your put-away by warehouse zone rules
 your stackability rules for inbound put-away and outbound pallet building
In the Detail Block, you can define specific warehouse zones for specific isolator codes.
1 Enter IPUP.
2 Click on Enter Criteria.
3 Key in the customer code and item code that you wish to set up and click on Execute Query.
4 Press Enter twice to position your cursor in the Directed Put-Away Zone Code (WHZO) field.
5 Key in your put-away zone code and press Enter or select it from the pick list.
6 If you require stackability rules for outbound pallet building, select a stackability indicator code from the 
pick list.
7 In the Stackability Quantity in Highest SKU field, you define how many layers of the highest SKU code 
can be stacked up.
For put-away purposes, the stackability factor will be applied to the location capacity. For example, if the 
location capacity is defined as four pallets and the item code has a stackability factor of 2, then the putaway/directed move engine will consider 8 pallets as the location capacity for this item code. 
IPUP screen showing put-away setup
8 If you require specific warehouse zones for specific isolator codes, click in the Detail Block and then click 
on New. Then enter your isolator codes and the corresponding warehouse zone codes.
9 When you finish setting up your put-away parameters, click on Save to save your new record.
10 Click on Exit to exit IPUP.

INBOUND ALLOCATION
Put-Away by Pallet Type
Put-Away by Pallet Type
You can put-away product by pallet size or pallet type rather than SKU quantity, weight or cube. For example, 
you receive both standard four-foot pallets as well seven-foot pallets in your warehouse and you need a way 
to assign your different pallet types to a location with sufficient capacity.
In the program INAT (Inventory Attribute Factors), you define the number of standard pallet positions for each 
pallet type. For example, suppose a four-foot pallet has a factor of 1 and a seven-foot pallet has a factor of 2. 
This means that a four-foot pallet can be stored in location with a capacity of one or more pallets while a 
seven-foot pallet can only be stored in a location with a capacity of two or more pallets.
INAT screen showing 7-foot pallet with a location capacity standard factor of 2.00
The following setups are required for put-away by pallet type:
 in LOTP the Enable Pallet Attribute flag must be set to Yes for the appropriate location type(s)
 in COMP the Enable Pallet Attribute in LOTP flag must be set to Yes
 in IAPR you must create an inventory attribute profile code for pallet types
 in ITEM you must attached your IAPR profile for pallet types to the appropriate items
See the Operations 2 Guide for further information on inventory attributes.

ALLOCATION AND WAVE MANAGER 4.2 47
OUTBOUND ALLOCATION
Understanding Allocation ................................................................................ 49
Manual Allocation......................................................................................... 49
Automatic Allocation .................................................................................... 49
Selection of Product..................................................................................... 49
Selection of Location.................................................................................... 50
Shipping With Insufficient Inventory............................................................. 50
Printing Your Pick Document ....................................................................... 51
Setting Up Outbound Allocation...................................................................... 52
Setting Up the Picking Profile (PIPR) .............................................................. 52
Procedure .................................................................................................... 63
Setting Up Item-Specific Picking Profiles in CCOP ....................................... 65
Deleting a Record in CCOP ......................................................................... 67
Setting Up the Item Location Profile for Picking (ILOP)................................ 67
Understanding Directed Picking................................................................... 68
Standard Logical Groups for Picking ........................................................... 69
Field Descriptions (ILOP)............................................................................. 74
Setting Up a New Profile in ILOP................................................................. 77
Assigning a Velocity Code to the ILOP Profile............................................. 79
Activating Directed Picking.............................................................................. 80
Allocating Variable Quantity Breakdown Product ......................................... 80
Allocation by Weight......................................................................................... 81
Setting Up Allocation by Weight................................................................... 82
Entering a W-type Line in ENOR ................................................................. 83
Inventory Only Allocation................................................................................. 85
Setting Up Inventory Only Allocation ........................................................... 85
Performing Inventory Only Allocation........................................................... 86
Performing Inventory Only Allocation in ENOR ........................................... 86
Allocating Orders in ASOR .............................................................................. 87
Querying in ASOR ....................................................................................... 87
Assigning Location(s) to an Individual Order ............................................... 91

OUTBOUND ALLOCATION
Assigning Locations to a Specific Order and all Subsequent Orders .......... 93
Assigning Locations to All Orders ................................................................ 94
Looking Up an Order Processed in ASOR................................................... 95
Manually De-Allocating Orders in DEOR ........................................................ 96
Setting Up Manual De-Allocation ................................................................. 97
De-Allocating an Entire Order ...................................................................... 97
De-Allocating Individual Order Lines............................................................ 99
Automatic De-Allocation of Orders Based on Order Priority...................... 100
Setting Up Automatic De-Allocation........................................................... 101
Assigning Priority Levels to Orders in ENOR............................................. 101
Allocating Product Based on Shelf Life........................................................ 102
Entering Orders With a Shelf Life Based on a Date Other Than the System 
Date ........................................................................................................... 102
Overriding the Shelf Life of Individual Order Lines in ENOR ..................... 103
Allocating Orders With Reserve Logic.......................................................... 105
Setting Up Reserve Logic .......................................................................... 106
Entering Orders in ENOR .......................................................................... 107
Using Reserve Logic in a Non-RF Environment ........................................ 109
Looking Up Inventory in LOEN .................................................................. 110
Performing Soft Allocation............................................................................. 111
Performing Hard Allocation in OPLU ............................................................ 112
Changing the Order Quantity of an Order Line .......................................... 114
Using Wildcards and Boolean Logic in Allocation ...................................... 116
Allocating Only Fully Filled Orders ............................................................... 117
Setting Up Allocation of Only Fully Filled Orders ....................................... 117
Manually Deactivating Allocation of Only Fully Filled Orders in ENOR...... 119
Allocating by Minimum Level 2, 3 and 4 Values........................................... 119
Setting Up Your Item Minimum Shipping Level Parameters...................... 121
Performing Item Minimum Shipping Level Allocation................................. 125
Reserving a Minimum Level of Inventory for High Priority Orders ............ 125
Setting Up a Minimum Level of Inventory .................................................. 125
Assigning Priority Levels to Orders in ENOR............................................. 127

OUTBOUND ALLOCATION
Understanding Allocation
ALLOCATION AND WAVE MANAGER 4.2 49
Understanding Allocation
Outbound allocation is the process of selecting and assigning specific inventory to fill an order. It also involves 
selecting and assigning the specific location or locations from which the product is to be taken when filling the 
order. In other words, it prepares the information for the picking instructions.
In ENOR, there are two ways of performing allocation: 
 manually, in which you perform allocation yourself
 automatically, in which the system performs allocation
MANUAL ALLOCATION
You must know all of the inventory levels in order to perform manual allocation. In the ENOR Line Block, you 
use an R (Regular) line type. Next you complete all of the Inventory Level fields, which selects and assigns 
specific product to the order line. 
If you also need to select the location from which the product is to be picked, you complete the Location Code 
field. Otherwise, you can leave the field blank for the system to choose the location through the allocation 
routine.
AUTOMATIC ALLOCATION
When you want the system to direct allocation, you use a P (Pending) line type in the Line Block and leave 
the Inventory Level 2 and higher inventory level fields blank. You also leave the Location Code field blank. 
Later, when you run the allocation routine, the system will automatically fill in these fields.
The allocation routine performs two functions:
 selects and assigns the inventory that is to be used when filling the order line. This is based on the 
parameters in the program Picking Profile (PIPR) and the setup in the program Depositor Shipping and 
Receiving (DSRP)
 selects and assigns the locations from which this product is to be picked according to the parameters 
that are set up in the program Item Location Profile (ILOP)
SELECTION OF PRODUCT
The allocation routine follows preset rules (parameters) when selecting the specific inventory to use for this 
ordered item. For example, depending on whether the product has a LIFO or FIFO Picking Profile setup, the 
system will select the oldest or the newest inventory entity for dated product. 
LIFO is Last In and First Out meaning that the inventory that arrived at the warehouse last for this item must 
be shipped out first; FIFO is First In and First Out meaning that the inventory that arrived first to the 
warehouse for this item must be shipped out first.
Outbound Allocation = Selection of a specific product 
to fill an order
Selection of a specific location from which to pick the 
product
 +

OUTBOUND ALLOCATION
Understanding Allocation
SELECTION OF LOCATION
When the selected product is stored in more than one location, the ILOP parameters direct the allocation 
routine to select the location that is preferable in terms of warehouse organizational priorities. For example, 
these could include picking first from a location to clean it out, picking first from an overflow location rather 
than from normal storage locations or picking first from locations that contain multiple Hold Code types rather 
than from locations that contain only one Hold Code type. 
The criteria for the parameters are set sequentially so that if the best option is not possible the system 
proceeds on the second best option and if the second option is not available it will proceed to the third best 
option, etc. until it finds a location.
SHIPPING WITH INSUFFICIENT INVENTORY
An order may require more product than there is presently available in the warehouse. For example, suppose 
you need to ship twenty cases and there are only ten cases available as inventory. What happens next will 
depend on your system setup:
Setup 1
If your system is set up in DSRP so that the Change Zero Pending Line to R-Type Line flag is set to Yes and 
two lots were chosen during allocation, the system will generate two R type lines in the Line Block:
If one lot was chosen during allocation, the system will generate one R type line in the Line Block:
The order can be confirmed in CHOF or COOL so that you can ship out the portion that is available.
Setup 2
If your system is set up in DSRP so that it will not change the zero pending line to an r-type line, the system 
will generate one R type line and one P type line in the Line Block:
The order cannot be confirmed in CHOF or COOL. You will not be able to ship out any product until the 
missing product is received or the pending line is deleted.
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

OUTBOUND ALLOCATION
Understanding Allocation
ALLOCATION AND WAVE MANAGER 4.2 51
PRINTING YOUR PICK DOCUMENT
If you used an R line type and you completed the Inventory Level 2 and higher fields as well as the Location 
Code field, you have performed allocation in ENOR. The data that you put into ENOR will be copied to the 
designated picking document as you print it. If you left the Location Code field blank, the allocation routine will 
select a location and it will populate this field accordingly as you print the designated picking document.
If you used a P line type, the system will perform allocation. Printing of the designated pick document will 
trigger the allocation routine to run. The allocation routine will select the entity and the location and it will enter 
the data into both ENOR and the designated picking document.
You complete the
Inventory Level 2 and
higher fields in ENOR
to select the specific
product that you
need.
You can complete the
Location Code field or
you can leave it blank
for the system to
choose the location.
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
Manual Allocation
Automatic
System-directed
Allocation
You leave the
Location Code
field blank for the
system to select.
You leave the
Inventory Level 2
and higher fields
blank for the
system to select.
PICKING
INSTRUCTIONS
PICKING
INSTRUCTIONS
You completed them
in ENOR. They only
need to be copied into
the designated picking
document when you
print it.
The allocation routine
will complete the
instructions when you
print the designated
picking document.

OUTBOUND ALLOCATION
Setting Up Outbound Allocation
Setting Up Outbound Allocation
In AccellosOne 3PL, there are two programs used to set up directed picking: PIPR (Picking Profile) and ILOP 
(Item Location Profile). In PIPR you define the FIFO/LIFO sequence that you wish to use for the purpose of 
selecting a batch of inventory records. In ILOP you define location and capacity parameters that you want the 
system to use when selecting locations from the batch of records generated by PIPR.
Directed picking in AccellosOne 3PL
Setting Up the Picking Profile (PIPR)
In this program, you define how product will be allocated to orders (if you use directed picking). In PIPR, you 
can specify:
 FIFO (First In First Out) or LIFO (Last In First Out)
 absolute FIFO/LIFO (that is, always pick from the oldest or newest lot, then the next oldest/newest lot, 
etc., and attach relatively less importance to location and capacity factors defined in ILOP) 
 relative FIFO/LIFO (that is, pick from a group of the oldest or newest lots and use location and capacity 
parameters defined in ILOP to make selections within this batch)
 the SKU class that you want the system to break at when picking partial quantities in ILOP
The picking profile that you define in PIPR can apply to all customers or to a particular customer. If required, it 
can apply to an item or series of items or it can apply to a consignee (that is all items being sent to a particular 
consignee).
If you are attaching picking profiles to items and consignees as well to customers, the following logic will 
apply:
 the profile that you attach to DSRP is the default
 if you attach a picking profile to ITEM, it will override the profile in DSRP
 if you attach a picking profile to CONS, it will override the profiles in DSRP and ITEM
 if you set up an item/consignee combination in CCOP, it will override the profiles in DSRP, ITEM and 
CONS (see “Setting Up Item-Specific Picking Profiles in CCOP” on page 65 for further information)
 if you attach a picking profile set up in PIPR to a hold type in HOLD, any order lines placed on that hold 
type will be allocated according to the hold type’s picking profile (that is, the customer’s, item’s or consignee’s picking profile will be overridden by the hold type’s picking profile)
CHANGING YOUR PICKING PROFILE
If you change your PIPR profile, the change takes effect immediately and applies to both existing orders as 
well as new orders. That is, PIPR settings are not saved when you create a new order. You can deallocate an 
existing order, change your PIPR profile and then re-allocate the order using your new picking rules.
ENOR PIPR ILOP

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 53
FIELD DESCRIPTIONS
Picking Profile Code Mandatory
Your picking profile code. For example, FIFO.
Description Mandatory
Your description.
Break Quantity at SKU 
Class
(defined in SKCL)
Mandatory
In this field, you specify how you want the system to pick partial quantities — 
that is, whether or not to break a pallet or some other SKU type when an order 
requires a partial quantity. 
A partial quantity in AccellosOne 3PL is defined as a quantity that is less than 
a full SKU class and not the highest SKU class. For example, if you have a 
PALLETS/CASES account and your SKU classes are 1 for pallets and 3 for 
cases, then a partial quantity would be any number of cases not making up a 
full pallet.
EXAMPLE 1
Quantity Breakdown
Pallets
Cases
Eaches
SKU Class
1 (Pallets and the like)
2 (Cases and the like)
5 (eaches and the like)
If you specify the Break at SKU Class 1 option, the system will try to keep pallets together and will consider cases (SKU class 3) as the only valid SKU 
class for picking partials. If you specify the Break at SKU Class 3 option, the 
system will ignore pallets and try to keep cases together. Eaches or SKU class 
5 will be considered as the only valid SKU class for picking partials. 

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
EXAMPLE 2
If you specify “Ignore SKU Classes” in the above example, the system will 
ignore SKU classes during allocation and pick from any class (that is, break 
pallets, cases, etc. in order to fill the order). For example, if your quantity 
breakdown were 50 cases to a pallet, the following could occur during directed 
picking. If the order called for 60 cases, the system might pick 30 cases from 
two pallets (that is, breaking the two pallets) instead of picking one full pallet 
and one partial (10 cases).
The “Ignore” option is reserved for single-level accounts with no partials — for 
example, CASES only. You cannot use the “Ignore” option for:
 pick line items
 items whose ILOP profile contains any option in the Partial Quantity Group 
(for example, “pick partial from bulk”, “if picking from bulk and location has 
partial …”, etc.).
NOTE The system will override your break quantity at SKU class option if 
you select any “Pick to match” option in ILOP and a match is found.
Picking Based on FIFO/
LIFO
F = FIFO (First In First Out)
L = LIFO (Last In First Out)
FIFO/LIFO Based on EXDT = Expiry Date*
LEV2 = Inventory Level 2
LEV3 = Inventory Level 3
LEV4 = Inventory Level 4
RCDT = Receipt Date*
Defines what the FIFO/LIFO sequence is based on. If you select inventory 
level (for example, a lot number or date code), you may need to specify a 
selection formula (see next field).
The value that you enter in this field determines the sort order of inventory 
records in the Drill Block of LOEN.
* Sort order by date in the Drill Block of LOEN is only supported for all numeric dates 
such as 01.01.2005. If you use dates such as DEC-05 and FEB-05, records will be 
sorted in alphanumeric order: APR-05, DEC-05, FEB-05, etc.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 55
FIFO/LIFO Formula Optional
If you selected an inventory level in the previous field, you may require a formula to convert your inventory level values into a form that the system can use 
when it performs allocation. Consult your HighJump representative for the 
appropriate formula.
FIFO/LIFO Custom Program
Optional
This field is reserved for those cases when a special program — not merely a 
selection formula — is required to convert inventory levels. Must be set up by 
a HighJump consultant.
Picking Type A = Absolute
R = Relative
L = Location Sequence
If you select Absolute, the allocation routine will always pick the oldest product 
(if you are using FIFO) or the newest product (if you are using LIFO) regardless of location. The range in days fields are not available when absolute 
FIFO/LIFO is chosen.
If you select Relative, the allocation routine will pick from a batch of the oldest 
(or newest) lots and use location parameters defined in ILOP to make selections within this batch. With this option, you can select one or both of the following fields — Range in Days From Oldest Lot and/or the Minimum/
Maximum Range in Days to Expiry — to specify a range.
The Number of Inventory Records not to Exceed is a mandatory field for relative allocation. 
If you select Location Sequence, the available stock will be sorted by the 
FIFO/LIFO criteria defined in the following PIPR fields: Picking Based on 
FIFO/LIFO, FIFO/LIFO Based on and FIFO/LIFO Formula. Then the FIFO/
LIFO records will be sorted by location code sequence.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
For example, if FIFO/LIFO is based on receipt date (RCDT), inventory will 
allocated by receipt date then by location code. Likewise, if FIFO/LIFO is 
based on expiry date (EXDT), inventory will allocated by expiry date then by 
location code. And if FIFO/LIFO is based on an inventory level (LEV2, LEV3 
or LEV4), inventory will be allocated by that inventory level value then by location code.
The following restrictions apply to allocation by absolute FIFO/LIFO then location code sequence:
 Your ILOP settings will not be checked.
 Your pick line settings will not be checked. All locations will be sorted by the 
location code and allocated accordingly.
 Full pallet or SKU class will not be checked. All stock will be sorted by FIFO/
LIFO criteria and location code only and allocated accordingly.
Range in Days from Oldest LotOnly available for relative picking.
In this field, you indicate to the allocation routine how many days from the oldest lot (or newest lot if you are using LIFO) it should look at — that is, how relative you want to pick. 
For example, if your oldest lot is dated June 1 and you enter 20 in this field, 
the system will look at all lots dated June 20 or older.
If you enter a small number in this field, the system will select a small number 
of lots and location will play a minor role in allocating product to orders. If you 
enter a large number in this field, the pick will be very relative — that is, the 
system will select a large number of lots to look at and location will play a 
major role in product allocation. 
FIELD DESCRIPTIONS
system looks at all lots dated June 20 or later
April May June 1 20 July
Oldest lot 
dated June 1
Range in days from
oldest lot set to 20

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 57
Range Based on Only available for relative picking. Mandatory if you are using a range in days 
field.
EXDT = Expiry Date
FIED = FIFO plus Expiry Date
FIRD = FIFO plus Receipt Date
RCDT = Receipt Date
SLPC = Shelf Life Percentage
If your FIFO or LIFO is based on the product’s receipt or expiry date, use 
EXDT or RCDT. If your FIFO or LIFO is based on a formula or custom program instead of your receipt or expiry date, select FIED or FIRD. 
Range in Days From Oldest Lot field
 if you select EXDT or FIED as your range based on value, the oldest/newest 
lot will be defined in terms of the expiry date
 if you select RCDT or FIRD as your range based on value, the oldest/newest lot will be defined in terms of the receipt date
Minimum/Maximum Range in Days to Expiry fields 
 if you select EXDT or FIED as your range based on value, the oldest/newest 
lot will be defined in terms of the expiry date
 if you select RCDT or FIRD as your range based on value, the oldest/newest lot will be defined in terms of the receipt date and AccellosOne 3PL will 
only pick product whose receipt date is newer than X days (that is, your 
range in days to expiry value) before the current system date
FIED and FIRD
These options use both the inventory level and receipt/expiry date to select 
the batch of inventory records. 
EXAMPLE
Suppose you set the Range in Days from Oldest Lot to 45 days and your oldest lot is dated February 1, 2000.
Lot
1
2
3
4
5
Level 2
001
002
007
010
102
Receipt Date
March 1, 2000
February 1, 2000
April 4, 2000
March 5, 2000
March 10, 2000
Days from Oldest Lot
29
0
63
34
39
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
AccellosOne 3PL sorts all records in the batch by inventory level 2. Then it 
looks at the receipt date for each lot. When it reaches a lot with a receipt date 
that is out of range such as record 3 with a receipt date of April 4, it rejects that 
lot plus all subsequent lots such as lots 010 and 102. Only lots 001 and 002 
will be included in the batch of eligible records.
Range in Days Starting 
From
Only available for relative picking
ARDT = To Arrive Date
ORDT = Order Date
SHDT = To Ship Date
SYDT = System Date (the date that the order is allocated)
The starting point for your range in days value. If you set the Range in Days to 
Expiry to 10 and select Order Date in this field, allocation will select product 
with a shelf life of at least 10 days as of the order date. If, on the other hand, 
you select To Arrive Date, allocation will select product with a shelf life of at 
least 10 days as of the to arrive date that you enter in ENOR.
If you leave this field blank, allocation will use SYSDT, the system default.
Number of Inventory 
Records not to Exceed
Mandatory for relative picking
In this field, you define the maximum number of inventory records that the 
allocation routine should process at a time. When you specify a maximum 
number of inventory records and a range in days from oldest lot or a range in 
days to expiry, the system will take the lessor of the two. 
EXAMPLE
You set the Range in Days From Oldest Lot field to 30 and this results in the 
selection of 15 inventory records. Then you set the Number of Inventory 
Records not to Exceed field to 20. The system will use the lessor value — 15 
— as the size of the batch. 
If you set this field to the maximum (99), your picking will be very relative; that 
is, the allocation routine will select records from many different lots and ILOP 
will make the final selection based on location. As a result, some older product 
may remain in your warehouse longer than desirable. 
If you set this field to a low value, your picking will be close to absolute FIFO/
LIFO and location factors defined in ILOP will play less of a role. Absolute or 
near absolute allocation can mean that you are taking less than full advantage 
of the system’s allocation capabilities. 
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 59
Minimum Remaining 
Shelf Life Percentage
Only available if Range Based on = Shelf Life Percentage
See “Allocating by Shelf Life Percentage” on page 104 for further information..
Minimum / Maximum 
Range in Days to Expiry
Optional
You use these fields if you want to select product that will not expire until a 
certain date (that is, newer lots); this option is a way of guaranteeing a longer 
shelf life for the product that you pick. When you enter a positive number in 
one or both of these fields, the allocation routine counts forward from the current date to arrive at a date in the future. The system will then look at all product with expiry dates from the future date or later.
When you enter a negative value in one or more of these fields, your range 
will fall in the past.
EXAMPLE 1
Range Based on = Expiry Date
Range in Days Starting From = Order Date = June 1
Minimum Range in Days to Expiry = 10
Maximum Range in Days to Expiry = blank
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
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
NOTE An expiry date in AccellosOne 3PL need not be the date that product actually expires. It can be any date in your warehouse such as a production date or a packing date that you use to allocate product for an outbound 
order.
FIELD DESCRIPTIONS
June 1 = order date June 11 June 15 June 20 June 25 June 30 = expiry 
This product has a This product will ship
shelf life less than the 
June 1 = order date June 11 June 15 June 21 June 25 June 30 = expiry 
This product has a This product will ship
shelf life less than the 
This product has a shelf 
life greater than the maxiJune 1 June 10 June 15 = expiry June 20 June 25 = current June 30
This product has a shelf life less than This product will ship
the minimum 

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 61
Sort Sequence Code 
(SOSE)
Optional
This field allows you to specify how you want the allocation routine to resolve 
tie-breaking situations. For example, suppose you specify the following three 
picking parameters in ILOP:
 use any isolator other than exact match or overflow 
 pick to match 
 ignore partials in bulk
When you run allocation, the system finds three locations that meet the above 
criteria: A2, C6 and F4. A sort sequence code allows you to specify which of 
these three locations you wish to pick from. You set up sort sequence codes in 
SOSE in the form of SQL order by statements.
If you do not specify a sort sequence code for your picking profile, the allocation routine will select the “lowest” location — in the example above, A2. 
Replenishment Message 
on Pick Documents
See “3 — Setting Up Your Picking Profile in PIPR” on page 135 for further 
information.
Use FIFO/LIFO for Pick 
Line Picking or Skip
See “3 — Setting Up Your Picking Profile in PIPR” on page 135 for further 
information.
Exclude Pick Line Stock 
When Bulk Picking
See “3 — Setting Up Your Picking Profile in PIPR” on page 135 for further 
information.
Replenishment Based on 
Eligible Records
Only applicable to floating pick lines
See “Setting Up a Floating Pick Line” on page 151 for further information. 
Replenish Pick Line up to 
Level
See “Setting Up a Pick Line With Replenishment by Inventory Level 2” on 
page 154 for further information.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
Allow Overpicking of 
Order Lines
Y = Yes (Clean Out Location)
N = No
P = Partial
If you enter Y for Yes (Clean Out Location), the operator can overpick/ship an 
order line in RFPIC. Overpicking means picking all product in a given location 
so that it is left empty. For example, if the order quantity is 10 cases and there 
are 20 cases of the same inventory entity in the location, the operator can 
either pick 10 cases or 20 cases (the total quantity in that location), but no 
other quantity. If there are 5 cases on hold in the location, the overpick quantity will be 15 cases (20 - 5).
If you enter N for No, the operator cannot overpick/ship an order line.
If you select P for Partial, the operator can pick any quantity between the pick 
quantity and the location quantity. For example, if your pick quantity = 5 cases 
and your location quantity = 10 cases, the operator can pick 5, 6, 7, 8, 9 or 10 
cases.
Picking Substitution Profile Code (PSPR)Your picking substitution profile code.
Break at SKU Class for 
Replenishment
See “3 — Setting Up Your Picking Profile in PIPR” on page 135 for further 
information..
Carton Active Flag Special programming by HighJump required
Y = Yes
N = No
If you set this flag to Yes, cartonization will be activated on your system. If you 
set this flag to No, cartonization will be deactivated on your system. 
EDI Version Code Special programming by HighJump required
Used to allocate product by price.
EDI Transaction Set 
Code (EDTS)
Special programming by HighJump required
Used to allocate product by price.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
ALLOCATION AND WAVE MANAGER 4.2 63
PROCEDURE
1 Enter PIPR.
2 Click on Enter Criteria then Execute Query to see which picking profiles have been already set up. 
3 If you need to set up another profile, click on Create Record.
4 Key in a picking profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 In the Break Quantity at SKU Class field, use your pick list to select the appropriate code. To select a 
code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list 
codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
7 Key in F for FIFO or L for LIFO and press Enter.
8 In the FIFO/LIFO Based on field, use your pick list to select what you want FIFO/LIFO to be based on — 
expiry date, receipt date or a particular inventory level.
9 If you selected an inventory level in the previous step, key in your FIFO/LIFO Formula and press Enter or 
press Enter to bypass this field. 
10 If required, key in a FIFO/LIFO Custom Program and press Enter.
EDI Data ID Code (EDDI) Special programming by HighJump required
Used to allocate product by price.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Picking Profile (PIPR)
11 Do one of the following:
12 If required, key in a sort sequence code in the Sort Sequence Code field and press Enter. If you do not 
require a sort sequence code, press Enter to bypass the field.
13 In the Replenishment Message on Pick Documents field, key in N for No and press Enter.
14 In the Use FIFO/LIFO for Pick Line Picking or Skip field, key in N for No and press Enter.
15 In the Exclude Pick Line Stock When Bulk Picking field, key in N for No or Y for Yes and press Enter.
16 In the Replenishment Based on Eligible Records field, key in N for No and press Enter. 
17 In the Replenish Pick Line up to Level field, key in 1 and press Enter.
18 In the Allow Overpicking of Order Lines field, key in N for No and press Enter.
19 Press Enter twice to bypass the Picking Substitution Profile Code and Break at SKU Class for Replenishment fields.
20 In the Carton Active field, key in N for No and press Enter.
If you wish to perform absolute 
picking:
If you wish to perform relative 
picking:
a) Key in A for Absolute and press 
Enter.
a) Key in R for Relative and press 
Enter.
b) In the Range in Days from Oldest 
Lot field, key in zero or a positive 
integer and press Enter.
c) In the Range Based on field, 
select the appropriate value from 
the pick list — EXDT, FIED, 
RCDT or FIRD.
d) If required, select the appropriate 
value from the Range in Days 
Starting From pick list.
e) In the Number of Records not to 
Exceed field, key in a positive 
integer and press Enter.
f) If required, key in a value in the 
Minimum Range in Days to 
Expiry field and press Enter.
g) If required, key in a value in the 
Maximum Range in Days to 
Expiry field and press Enter.

OUTBOUND ALLOCATION
Setting Up Item-Specific Picking Profiles in CCOP
ALLOCATION AND WAVE MANAGER 4.2 65

Picking Profile with relative option based on expiry date selected
21 Repeat the above steps to add another picking profile or click on Return to Main and then Exit to exit the 
program.
Setting Up Item-Specific Picking Profiles in CCOP
If you are shipping to a consignee that has been assigned a picking profile and you want the shelf life of the 
items on the order to override the shelf life defined for the consignee, you must set up the appropriate 
consignee/item combinations in CCOP (Customer/Consignee Override of PIPR). 
If you do not set up the appropriate consignee/item combinations in CCOP, the shelf life of the consignee will 
override the shelf life of the items on the order. For example, the shelf of 15 days for the consignee will 
override the shelf life values for all items on the order (say, 10 days for item A, 12 days for item B, 20 days for 
item C, etc.).
You have two options in CCOP: 
 you can assign a picking profile to a given item
 alternatively, you can assign a picking profile to a given commodity code and commodity sub code, and 
that picking profile will apply to all items with that commodity and commodity sub code.
During allocation, AccellosOne 3PL will follow the sequence below to determine the applicable picking profile 
for a given order line:
a) if the product is on hold, the PIPR profile, if any, attached to the hold in HOLD
b) the PIPR profile, if any, attached to the item in CCOP
c) the PIPR profile, if any, attached to the commodity code/commodity sub code in CCOP

OUTBOUND ALLOCATION
Setting Up Item-Specific Picking Profiles in CCOP
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
If you are assigning a picking 
profile to an individual item:
If you are assigning a picking 
profile to a group of items 
through the use of commodity 
codes and commodity sub 
codes:
a) Key in your item code and press 
Enter.
a) Press Enter to bypass the Item 
Code field.
b) Key in your commodity code and 
press Enter.
c) Key in your commodity sub code 
and press Enter.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 67

Customer/Consignee Override of PIPR screen showing three records
9 Click on Exit to exit.
DELETING A RECORD IN CCOP
1 Enter CCOP.
2 Retrieve the record that you wish to delete.
3 Press Enter until your cursor is positioned in the Picking Profile Code field.
4 Click on Delete.
5 Click on Return to Main and Exit to exit.
Setting Up the Item Location Profile for Picking (ILOP)
In this program, you define the algorithms that you want AccellosOne 3PL to use when it performs picking. 
You can have the system pick product based on receipt date, isolator zone, quantity of product in the location 
and other criteria that you specify.
When you set up picking in AccellosOne 3PL, orders are channelled first through PIPR (Picking Profile), 
which selects product in FIFO/LIFO sequence based on receipt date or expiry date. The batch of inventory 
records selected by PIPR is then sent to ILOP, which selects locations based on the criteria that you specify.
There are three processes in directed picking in AccellosOne 3PL:
You can set up as many different profiles as you need. If you intend to use the same picking parameters for all 
product belonging to all customers, you would set up a single picking profile. If you intend to pick differently 
ENOR PIPR ILOP
Enter an order Pick product based on 
FIFO/LIFO
Pick product based on 
location

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
based on customer, you would set up a separate profile for each customer. And if certain items require special 
picking logic, you would have to set up separate profiles for those items that require non-standard picking. 
The profile that you create in ILOP is attached to ITEM. 
UNDERSTANDING DIRECTED PICKING
In picking, you want to pick product from the least desirable location first. If the least desirable location is not 
available, you want to pick from the next least desirable location and so on and so forth. In ILOP, you tell the 
system the criteria that you wish it to use for the purpose of identifying the least desirable and next least 
desirable locations.
You define your criteria by means of sequences. Each sequence contains a number of parameters for 
selecting a location. The following example shows five sequences that progressively define increasingly 
desirable locations.
Sample Sequences for Selecting Locations
In this example, the priorities of the warehouse are as follows:
 product should be kept in its isolator as much as possible
 full pallets should be shipped wherever possible (Break Quantity at SKU Class field in PIPR = 1 for pallets)
 high efficiency in picking takes precedence over a “clean” warehouse
If any of the priorities of your warehouse differs from the above, you would have to create different sequences.
Sequence 1
(worst)
Use any isolator other than exact match or 
overflow
Pick to match
Ignore partials in bulk
In this sequence, which contains the strictest selection criteria, the system searches for a location whose isolator is not an exact match or 
overflow and whose quantity is an exact match of the quantity needed 
(full pallets only).
Sequence 2
(next worst)
Use any overflow isolator
Pick to clean
If picking from bulk and location has partial 
and partial less than needed then pick it
In this sequence, which is less strict, the system searches for overflow 
locations with the least amount of product and picks from them. If it 
encounters a partial quantity in bulk (that is, less than a full pallet) and 
the partial quantity is less than the quantity needed, it picks the partial 
quantity.
Sequence 3
(next worst)
Use any overflow isolator 
Pick to match
Ignore partials in bulk
In sequence 3, which is less strict, the system continues to search overflow locations. This time it picks full pallets if the quantity needed is an 
exact match of the quantity on hand.
Sequence 4
(next worst)
Use any overflow isolator
Pick to clean
Pick partial quantity from bulk where ITEM 
partial in location is eliminated
The system continues to search overflow locations. This time it picks full 
pallets from locations with the least amount of product first. If it encounters a partial quantity in bulk (that is, less than a full pallet) and the partial quantity matches the quantity needed, it picks the partial quantity.
Last Sequence (performed by system if 
required)
Ignore isolator codes
Pick to clean
Ignore partials in bulk
In the last sequence, which is only performed if all the other sequences 
fail, the system turns all options off and uses the default in each group. 
In this example, the defaults are pick to clean from any location in the 
warehouse including exact match isolators.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 69
STANDARD LOGICAL GROUPS FOR PICKING
There are 13 logical groups in ILOP. Each group has two or more mutually exclusive options. From each 
group, you select the appropriate option. If you do not wish to use a particular group, select the first option in 
the group to deactivate it. For example, if you do not wish to use the Hold codes group, you would select the 
first option, “Ignore hold codes in location”.
RECEIPT DATE GROUP (O0300)
In this group, you specify whether you want the system to pick product based on the date the product was 
received into a location — not the global receipt date of the item. This option is used when you receive open 
lots within the same item over a period of time. 
ISOLATOR GROUP (O0500)
TIP You can define up to nine passes or sequences in any given profile. It is important to bear in mind, however, that each sequence requires time to perform the specified searches to validate locations. Therefore, you must strike a balance between the 
requirement to pick product from the best possible location using many sequences 
and the requirement to process orders in a reasonable time.
ignore original receipt date of product in 
location (default)
Do not take into account the date the product was received into a 
location.
Sequence by original receipt date of 
product in location 
Sort all locations by the date that the product was originally 
received into that location. If FIFO or LIFO is needed within an 
entity, then this option must be turned on.
ignore isolator codes (default) Do not use isolator codes for the purposes of determining locations 
from which to pick.
use only exact match isolator code Pick from locations where item isolator matches the location isolator. 
use any overflow isolator code Pick from locations whose overflow isolator matches one of the 
overflow isolators of the item. If an item has multiple overflows, the 
system will pick from the last overflow first. 
use any isolator code other than exact 
match or overflows
Pick from locations that are outside of all isolator overflows and 
exact match isolators.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
CAPACITY GROUP (O1000)
MIXED PRODUCT GROUP (O1500)
In this group, you specify how you want the allocation routine to clean up product from mixed locations.
pick to clean (default) Pick from locations with the least amount of product first and then 
pick from locations with the next most.
pick to match Pick from locations that have the exact quantity needed.
go from highest to lowest in quantities Pick from locations that have the most amount of product in them.
match order quantity and go upward Pick from locations that have the exact quantity needed. If no such 
locations are found, then pick from locations with the next highest 
quantity.
match order quantity and go downward Pick from locations that have the exact quantity needed. If no such 
locations are found, then pick from locations with the next lowest 
quantity.
match order quantity and go upward 
and then downward
Pick from locations that have the exact quantity needed. If no location is found, the system will search for the location with the next 
highest quantity. If there are no locations with the next highest 
quantity, the system will search for the next lowest quantity and use 
it. Then it will continue looking at locations with smaller and smaller 
quantities.
match order quantity and go downward 
and then upward
Pick from locations that have the exact quantity needed. If no location is found, the system will search for the location with the next 
lowest quantity. If there are no locations with the next lowest quantity, the system will search for the next highest quantity and use it. 
use any location (default) Pick from any location regardless of what other product may or 
may not be there.
use only locations where depositor 
code is different
Pick from locations with product belonging to more than one customer.
use only locations where up to level 1 is 
different
Pick from locations with product where customer or level 1 is different.
use only locations where up to level 2 is 
different
Pick from locations with product where customer or level 1 or level 
2 is different.
use only locations where up to level 3 is 
different
Pick from locations with product where customer or level 1 or level 
2 or level 3 is different.
use only locations where up to level 4 is 
different
Pick from locations with product where customer or level 1 or level 
2 or level 3 or level 4 is different.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 71
ON RECEIPT MIXED PRODUCT GROUP (O2000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting 
locations in the Mixed Product Group. This does not mean that the allocation routine will pick product that has 
not been confirmed; it simply means that the system will take into account unconfirmed receipts and their 
locations when selecting locations from which to pick.
EXAMPLE
You receive 10 cases from customer X and assign it a given location. Because it has not been confirmed, its 
status remains “on-receipt.” This location already has 15 cases (confirmed) belonging to customer Y. If you 
select the “Use only locations where depositor code is different” option in the Mixed Product Group, the 
system will follow one of two scenarios: it can consider this location to have multiple customers and will 
attempt to pick from it (that is, on-receipt product is considered regular inventory) or it can consider this 
location to be a single customer location and not attempt to pick from it. 
HOLD CODES GROUP (O2500)
In this group, you specify whether you want the system to attempt to clean up locations containing multiple 
hold codes. The allocation routine will always pick product with the same hold code as the hold code on the 
order.
ON RECEIPT HOLD CODE GROUP (O3000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting 
locations in the Hold Code Group. This does not mean that the allocation routine will pick product that has not 
been confirmed; it simply means that the system will take into account unconfirmed receipts and their 
locations when selecting locations from which to pick.
EXAMPLE
You receive 10 cases and assign it a given location that already has 15 cases in it. The on-receipt product has 
a given hold code assigned to it while the confirmed product has a different hold code applied to it. If you 
select the “Use any location with multiple hold codes” option in the Hold Code Group, the system will follow 
one of two scenarios: it can consider this location to have multiple holds and will attempt to pick from it (that 
ignore on receipt in uniqueness calculations (default)Do not use on-receipt quantities when selecting locations in the 
Mixed Product Group.
use on receipt in uniqueness calculations Use on-receipt quantities when selecting locations in the Mixed 
Product Group — that is, treat these quantities like regular inventory.
ignore hold codes in location (default) Select locations regardless of the hold codes of the other product 
in that location.
use any location with only that hold 
code
Select locations that have only that product on that hold in that 
location.
use any location with multiple hold 
codes
Select locations that have other hold codes in that location regardless of the product the hold codes are attached to.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
is, on-receipt product is considered regular inventory) or it can consider this location to have a single hold and 
not attempt to pick from it.
PARTIAL QUANTITY GROUP (O3500)
In this group, you specify whether you want the system to attempt to clean up locations containing partial 
quantities. A partial quantity is a quantity that is less than a full SKU class and not the highest SKU class. For 
example, if an item has a quantity breakdown of PALLETS/CASES/EACHES, then any combination of cases 
not forming a full pallet is considered a partial and any combination of eaches not forming a full case is 
considered a partial.
You define in the Break Quantity at SKU Class field in PIPR (Picking Profile) which SKU class(es) you want 
the system to break for the purpose of picking partials. The system will use the SKU class immediately below 
the SKU class you specify in PIPR. For example, suppose your quantity breakdown is PALLETS/CASES/
EACHES and your SKU classes for this quantity breakdown are 1, 3 and 5. If you specify Break Quantity at 
SKU Class 1 in PIPR, the system will consider CASES (SKU class 3) as the only valid SKU class for picking 
partials.
If the Break Quantity at SKU Class field in PIPR is set to “Ignore SKU classes”, then this group is ignored. 
In this group, bulk is defined as any location type set up in LOTP that is neither a pick line nor staging location 
type.
ignore on receipt in hold code calculations (default)Do not use on-receipt quantities when selecting locations in the 
Hold Code Group.
use on receipt in hold code calculations Use on-receipt quantities when selecting locations in the Hold 
Code Group — that is, treat on-receipt product like regular inventory.
ignore partials in bulk (default) Do not use partials in bulk for the purpose of determining locations 
from which to pick.
pick partials from bulk where ALL partials in location are eliminatedPick partials from bulk if all partials in the location will be eliminated. This means there cannot be partials from another item or 
from the same item but not in the current batch.
pick partials from bulk where ITEM partial in location is eliminatedPick from location if the partial quantity in the location is less than 
the partial quantity needed to fulfill the order line.
pick partials from bulk where partial is 
exact match and empties location
Pick from location if the partial quantity in the location matches the 
partial quantity needed to fulfill the order line and empties the location.
NOTE: Do not use this option in any sequence containing a Mixed 
Product Group option.
if picking from bulk and location has 
partial and partial less than needed 
pick it
If you are already picking from a bulk location as a result of an 
option selected in another logical group, pick from the bulk location 
you’re already looking at if the partial quantity in the location is less 
than the partial quantity of the order needed.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 73
ON RECEIPT PARTIAL QUANTITY GROUP (O4000)
In this group, you specify whether you want the system to ignore or use on-receipt quantities when selecting 
locations in the Partial Quantity Group. This does not mean that the allocation routine will pick product that is 
not on a confirmed receipt; it simply means that the system will take into account unconfirmed receipts and 
their locations when selecting locations from which to pick.
EXAMPLE
You receive a full pallet and assign it a given location, but the receipt remains unconfirmed. The location to 
which you assigned the pallet already has 15 cases (confirmed) in it. Therefore, you now have 1 pallet/15 
cases in the location. If you select the “Pick partial quantity from bulk where partial is exact match and 
empties location” option in the Partial Quantity Group and enter an order for 1 pallet/15 cases, the system will 
follow one of two scenarios: it can consider this location to have an exact match and will attempt to pick from 
it (that is, on-receipt product is considered regular inventory) or it can consider this location to have only 15 
cases and not attempt to pick from it.
FIFO GROUP (O4500)
In this group, which is only available if you pick relative in PIPR, you specify whether you want the system to 
sequence the locations to be picked by the FIFO of their inventory records within the batch.
PALLET BREAKDOWN GROUP (O5000)
In this group, you specify whether you want the system to pick from locations containing pallets with a 
standard quantity breakdown — that is, the quantity breakdown of the pallet matches the quantity breakdown 
of the item in IQBP.
ignore on receipt in partial calculations 
(default)
Do not use on-receipt quantities when selecting locations in the 
Partial Quantity Group.
use on receipt in partial calculations Use on-receipt quantities when selecting locations in the Partial 
Quantity Group — that is, treat on-receipt product like regular 
inventory.
ignore FIFO of inventory records within 
batch (default)
Do not use FIFO to sequence records within the inventory batch.
sequence locations by the FIFO of their 
inventory records within the batch
Use FIFO to sequence records within the batch from the oldest 
product to the newest product. If there are multiple eligible lots 
within the same location, the system will pick all lots in the location 
even if this violates the FIFO sequence.
For example, if location A has lot Jan. 5 and location B has lots 
Jan. 1 and Jan. 10, the system will pick in the following order: location B (lots Jan. 1 and Jan. 10) then location A (lot Jan. 5).
ignore matching of pallet breakdown 
with quantity breakdown set up in ITEM 
(default)
Select locations regardless of the quantity breakdown of the pallets 
in that location.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
LOCATION TYPE GROUP (O5500)
In this group, you specify whether you want the system to pick full pallets from the pick line or from bulk.
OVERRIDE QUANTITY BREAKDOWN GROUP (O6000)
In this group, you specify whether you want the system to define a full pallet as all stock in a single location; 
that is, ignore the item’s standard quantity breakdown set up in ITEM. For example, if an item’s quantity 
breakdown is 60 cases per pallet and there are 50 remaining cases in a single location and all 50 cases have 
identical inventory levels (that is no mixed stock), AccellosOne 3PL will consider the 50 cases as a full pallet 
when performing full pallet picking and full pallet replenishment.
FIELD DESCRIPTIONS (ILOP)
use location where pallet breakdown 
equal to quantity breakdown set up in 
ITEM
Select only locations in which the quantity breakdown of the pallet 
matches the standard quantity breakdown of the item in ITEM.
pick from all location types (default) Select locations regardless of the location type.
exclude pick line type locations when 
picking for SKU class 1
When picking full pallets, select only locations with a location type 
other than pick line.
do not override quantity breakdown 
(default)
Use the item’s standard quantity breakdown set up in ITEM to 
define a full pallet.
override quantity breakdown, treat all 
stock in 1 location as 1 pallet
If all product in a given location has the same inventory levels (that 
is, no mixed stock), consider the product a full pallet even if the 
number of cases is less than a full pallet.
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
If you click on the View Flow Chart icon , you can see a flow chart of 
your profile showing each sequence as well as the picking options for that 
sequence.
Description Mandatory
Your item location profile code description.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 75
Isolator Code
(defined in ISOL)
Mandatory
If you are using exact match or overflow isolator zones to define your picking 
algorithm, you will need to set up one ILOP profile for each isolator zone that 
you defined in ISOL.
If you do not use exact match or overflow isolator zones in your picking, use 
your N/A (Not Applicable) isolator.
Overflow Warehouse 
Code
(defined in WARE)
Mandatory
Use any warehouse code.
Overflow Location Code
(defined in LOCA)
Mandatory
Use any location code.
SEQUENCE BLOCK
Sequence Number Mandatory
1, 2, 3, 4, etc.
Each sequence or pass contains the parameters that you specify for selecting a 
location. The sequence numbers that you enter in this field determine the order in 
which sequences are run.
Description Mandatory
Your sequence number description.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
Warehouse Code
(defined in WARE)
Optional
If you specify one or more warehouses in this field, the system will restrict its 
search for a location to the warehouse(s) you specify. If you leave this field blank, 
the system will search all warehouses.
If required, each sequence can have a different warehouse. For example, 
sequence 1 could search for locations in warehouse 1, sequence 2 could search 
for locations in warehouse 2, sequence 3 could have no warehouse assigned, 
etc.
You can use the following symbols (=, <, >, etc.) to define one or more warehouses:
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
Location Code
(defined in LOCA)
Optional
If you specify one or more locations in this field, the system will restrict its search 
for a location to the location(s) you specify. If you leave this field blank, the system will search all locations.
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
This field allows you to temporarily restrict put-away to certain locations or aisles 
when you are reracking your warehouse.
Acceptable Gap Height Reserved for future use.
UOM Reserved for future use.
Quantity Range Reserved for future use.
SEQUENCE BLOCK

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 77
SETTING UP A NEW PROFILE IN ILOP
1 Enter ILOP.
2 Do one of the following:
3 Use your pick list function to select your code. To select a code using a pick list, press F10 to display the 
pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position 
your cursor over the appropriate code and click on Select Code.
4 Use your pick list function to select any warehouse code for your overflow warehouse.
5 Use your pick list function to select any location code for your overflow location code.
Isolator Code
(defined in ISOL)
If you enter an isolator code in this field, it will override the isolator code in the 
Header Block for a particular sequence.
If you are creating a new ILOP 
profile:
If you are attaching your picking 
parameters to an existing ILOP 
profile:
a) Click on Create Record.
b) Key in an item location profile 
code and press Enter.
c) Key in a meaningful description 
for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to 
update.
b) Click on Type Block.
c) Proceed to step 5.
SEQUENCE BLOCK

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)

Item Location Profile
6 Press your up or down arrow key in the Type Block until the Picking option is displayed.
The Sequence, Selected Options and Available Options Blocks for Picking will be displayed.
7 Click on Sequence Block.
8 Key in 1 for your first sequence and press Enter.
9 Key in a description for your first sequence (for example, FIRST PASS) and press Enter.
10 If you wish to restrict the search for locations in this sequence to a particular warehouse, key in the warehouse code and press Enter. If you want to search locations in all warehouses, press Enter to bypass this 
field.
11 If you wish to restrict the search for locations in this sequence to particular locations, key in the location 
codes and press Enter. If you want to search all locations in this sequence, press Enter to bypass this 
field.
You will see the first set of parameters appear in the Available Options Block.
12 Press Enter three times to bypass the Acceptable Gap Height, UOM and Quantity Range fields.
13 If you wish to override the isolator code in the header for a given sequence, key in your override isolator 
code and press Enter. If you do not wish to override the isolator code in the header, press Enter to 
bypass this field.
14 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you 
wish to choose and then click on Select Option. If you do not wish to use a particular group (for example, 
the Hold code group), select the first option in the group (“Ignore hold codes in location”) to deactivate 
the group.
You will see the second set of parameters appear in the Available Options Block.

OUTBOUND ALLOCATION
Setting Up the Item Location Profile for Picking (ILOP)
ALLOCATION AND WAVE MANAGER 4.2 79
15 Repeat the previous step for each set of parameters.
16 When you finish entering all your parameters for your first sequence, your cursor will be positioned in the 
Selected Options Block.

Sample Picking screen after entering sequence 1
17 Click on Sequence Block.
18 Repeat steps 7 to 16 for each additional sequence that you wish to set up for your picking profile.
19 When you finish entering all your sequences, click on Return to Main and then Type Block.
20 Click on Master Block and then Exit to exit the program.
ASSIGNING A VELOCITY CODE TO THE ILOP PROFILE
You can assign velocity codes to item location profile codes (ILOP) to indicate whether a particular item is fast 
moving or slow moving. For example, you assign the fast moving velocity code to the ILOP profile ABC and 
the slow moving velocity code to the ILOP profile DEF. You then attach your velocity codes to the appropriate 
items in ITEM.
The purpose of velocity codes is to handle seasonal product whose velocity may change depending on the 
time of year. For example, turkey is a fast-moving product at Thanksgiving and a slow-moving product at 
other times of the year.
See “Attaching a Velocity Code to the ILOP Profile” on page 27.

OUTBOUND ALLOCATION
Activating Directed Picking
Activating Directed Picking
Three conditions must be met before directed picking is activated:
 the Assign Location flag must be set to Yes for an outbound flow code in DIFP
 an outbound document must be set up to print in DIFP (unless you run ASOR or pick using RF)
 the locations from which you wish to pick must be assigned a location type in LOTP whose Directed 
Picking flag has been set to Yes
Allocating Variable Quantity Breakdown Product
If you receive variable quantity breakdown product, you must specify how you want AccellosOne 3PL to 
handle scenarios where the total quantity picked may not match the order quantity.
For example, suppose the quantity breakdown of a variable quantity breakdown item is 100 cases per pallet 
and your order quantity is 5 PLT 10 cases or 510 cases. Allocation will attempt to pick 5 whole pallets. 
However, because some of the pallets may in fact contain 90 cases or 110 cases, the total quantity picked 
may not match the order quantity.
You specify your allocation option in the Allocation of Variable Quantity Breakdown Items Based on Highest 
SKU Entered field in DSRP.
This field is only used for variable quantity breakdown items in which at least one SKU class is defined as a 
partial in the Break Quantity at SKU Class field in PIPR. As well, the item’s ILOP parameter cannot use any of 
the Match Quantity options.
NOTE If you activate directed picking and do not set up any picking parameters in 
ILOP, the allocation routine will use the default value for each logical group. The 
default value is the first option in each group.
FIELD DESCRIPTIONS
Allocation of Variable 
Quantity Breakdown 
Items Based on Highest 
SKU Entered
N = No
Y = Yes
If you set this field to N for No or leave it blank, allocation will convert the order 
quantity to the lowest SKU and attempt to allocate that. If you set this field to Y 
for Yes, allocation will attempt to allocate according to the highest SKU and 
the quantity shipped may exceed the order quantity if some of the pallets 
picked are “oversized”.

OUTBOUND ALLOCATION
Allocation by Weight
ALLOCATION AND WAVE MANAGER 4.2 81

DSRP screen showing Allocation of Variable Quantity Breakdown Items Based on Highest SKU 
Entered flag set to N for No
Allocation by Weight
You can allocate by weight by entering a W-type line in ENOR. When you allocate by weight, you enter the 
weight that you wish to ship rather than the number of units. During allocation, AccellosOne 3PL will change 
the W-type line to a R-type line and calculate the number of units that the entered weight represents. If you 
use reserve logic, the W-type line will be changed to a U-type line containing the number of units that the 
entered weight represents.
If there is insufficient inventory in your warehouse to fully fill a W-type line, the way in which AccellosOne 3PL 
treats the remaining unallocated weights depends upon the option that you choose in the Change Zero 
Pending Line to R-Type Line field in DSRP (Depositor Shipping & Receiving Profile) and whether or not 
Reserve Logic is activated. 
Reserve 
Logic 
Activated
Change Zero 
Pending Line 
Status Result
Y Y The remaining weight will be converted to the appropriate number of 
units and will appear in the Order Quantity field of a U-type line.
Y N The remaining weight will be left as a W-type line.

OUTBOUND ALLOCATION
Allocation by Weight
The only ILOP parameters available for W-type lines is the default option for each logical group. For example, 
in the Capacity Group of ILOP (Picking), pick to clean (the default) is the only option available. The other 
options in this group such as Pick to Match and Match Order Quantity and Go Upward are not available for Wtype lines. 
W-type lines are similar to P (Pending) type lines in that inventory is not reserved for the order.
SETTING UP ALLOCATION BY WEIGHT
In order to allocate by weight, you must set the Ship by Weight and Ship by Weight Rounding Method fields in 
ITSH (Item Shipping Profile) to the appropriate values. You then attach your ITSH profile to the appropriate 
items.
N Y The remaining weight will be converted to the appropriate number of 
units and will appear in the Order Quantity field of an R-type line.
N N The remaining weight will be left as a W-type line.
FIELD DESCRIPTIONS
Ship by Weight D = Disallowed
N = Net Weight
G = Gross Weight
If you select D for Disallowed, allocation by weight is not allowed. If you select 
N for Net Weight, you can allocate by net weight. If you select G for Gross 
weight, you can allocate by gross weight.
NOTE The Net Weight and Gross Weight options allow allocation by 
weight, but do not require it. You can still allocate by number of units if you 
enter a P-type line in ENOR.
Ship by Weight Rounding MethodU = Up
D = Down
If you select U for Up and the weight that you entered does not correspond to 
a specific number of units, AccellosOne 3PL will round up the number of units 
shipped. If you select D for Down and the weight that you entered does not 
correspond to a specific number of units, AccellosOne 3PL will round down 
the number of units shipped.
For example, if your shipping weight is 1,000 lbs. and you select the Down 
option, AccellosOne 3PL could allocate 49 units with a total weight of 990 lbs. 
If, on the other hand, you select the Up option, AccellosOne 3PL could allocate 50 units with a total weight of 1,100 lbs.
Reserve 
Logic 
Activated
Change Zero 
Pending Line 
Status Result

OUTBOUND ALLOCATION
Allocation by Weight
ALLOCATION AND WAVE MANAGER 4.2 83

ITSH screen showing Ship by Weight field set to G for Gross Weight
ENTERING A W-TYPE LINE IN ENOR
1 Enter ENOR.
2 Enter your order header information in the normal manner.
3 In the Line Block, key in W for Weight in the Type field and press Enter.
4 Key in your item code and press Enter.
5 If required, key in any level 2 or higher values that you wish to select and press Enter.
6 Key in your order weight and press Enter.

OUTBOUND ALLOCATION
Allocation by Weight

ENOR screen showing a W-type line for 100 lbs.
7 Press Enter to accept the To Ship Weight.
8 When you finish entering your W-type lines, click on Master Block and Exit to exit.
Line Type = W for 
Weight

OUTBOUND ALLOCATION
Inventory Only Allocation
ALLOCATION AND WAVE MANAGER 4.2 85

ENOR screen showing the same order after allocation (the W-type line has been converted to a Rtype line and the 100 lbs. has been converted to pallets and cases)
Inventory Only Allocation
Inventory only allocation allows you to reserve inventory for a given set of orders without assigning locations. 
It is equivalent to an R-type line in ENOR in which neither the level 2 or higher values nor the location has 
been entered. After you perform inventory only allocation, you have two options: you can enter your locations 
manually in ENOR or an RF program or you can run a full allocation by printing a document or by running 
ASOR (Assign Orders to Locations).
Inventory only allocation is designed for situations in which you wish to reserve inventory without assigning 
locations. For example, you receive your P-type orders through EDI for a particular customer and you wish to 
reserve inventory for those orders so that the inventory cannot be assigned to other less important orders.
SETTING UP INVENTORY ONLY ALLOCATION
1 Enter DIFP.
2 Select the outbound flow at which you wish to perform inventory only allocation.
3 Set the Assign Location flag to I for Inventory Only.

OUTBOUND ALLOCATION
Inventory Only Allocation

DIFP screen showing inventory only allocation activated for the flow STPI
4 Exit DIFP. 
PERFORMING INVENTORY ONLY ALLOCATION
1 Enter your order in ENOR using P-type lines. If your orders are created automatically through EDI, you 
can skip this step.
2 Advance the flow of the order in CHOF until you reach your inventory only allocation flow.
3 Run ASOR (Assign Locations to Orders) to perform inventory only allocation. AccellosOne 3PL will 
assign the inventory levels but no locations to each order line and will change the line type from P to R.
4 Advance the flow of the order in CHOF to your full allocation flow.
5 Allocate the order by printing an order document, picking the order in an RF program or running ASOR.
6 Confirm the order in the normal manner. 
PERFORMING INVENTORY ONLY ALLOCATION IN ENOR
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

OUTBOUND ALLOCATION
Allocating Orders in ASOR
ALLOCATION AND WAVE MANAGER 4.2 87
8 Confirm the order in the normal manner. 
Allocating Orders in ASOR
The normal sequence for shipping operations in AccellosOne 3PL is first to key in the order in ENOR and 
then to run the allocation routine. The allocation routine is automatically triggered when you print the designated pick document, when you perform an RF function or when you run a batch program, depending on your 
system setup. Automatic allocation will select and assign the location(s) from which the ordered product is to 
be picked.
Whenever it is necessary to assign locations to an order without printing the pick document or without 
performing any of the other functions that would normally trigger automatic allocation, you use the program 
Assign Orders to Locations (ASOR). ASOR causes the allocation routine to run before its normal sequence. 
As ASOR assigns the locations to an order, the order lines automatically change from P to R type lines.
ASOR applies to orders that are:
 unallocated (unassigned) — they did not have a Location Code(s) assigned in ENOR 
 unconfirmed — they have not been confirmed in CHOF
 at a flow whose Assign Location flag in DIFP has been set to Y for Yes
In ASOR you can instruct the system to:
 assign locations to a specific order
 assign locations to two or more specific orders
 simultaneously assign locations to a specific order and all orders that were created after it (for example, 
order number 125 and all sequentially higher order numbers that are currently in the system — order 
number 126, 127, 128, etc.)
 simultaneously assign locations to all orders that are currently in the system
QUERYING IN ASOR
You can query ASOR to find and display orders. ASOR will only display orders that are unallocated, unconfirmed and active. Depending on your query, the system will display:
 a specific order number and all other unconfirmed orders that have a higher sequential number
 all order numbers that are currently in the system

OUTBOUND ALLOCATION
Allocating Orders in ASOR

ASOR screen
No query restrictions
Number on File will display in the Help Message 
Line how many records 
will be retrieved for these 
restrictions.
Execute Query will then 
display all six records.

OUTBOUND ALLOCATION
Allocating Orders in ASOR
ALLOCATION AND WAVE MANAGER 4.2 89

ASOR screen showing all six records
To view all orders for all customers that are currently in the system and that are unconfirmed, active and 
unallocated, enter the program ASOR. Then click on Execute Query. 

OUTBOUND ALLOCATION
Allocating Orders in ASOR

ASOR screen
To view all orders for all customers 
that were created after a specific order 
number that you specify . . .
Key in the order number that you want the system to start with and 
click on Execute Query. For example, if you key in order number 
123, the system will display all orders for all customers that have a 
sequential number of 123 or higher.
To view all orders that apply to only 
one customer . . .
Leave the Order Number field blank and press Enter. The cursor is 
in the Customer Code field. Key in the customer code and click on 
Execute Query. 
To view all orders that apply to only 
one carrier . . .
Press Enter three times (once to bypass the Order Number field, 
second to bypass the Customer Code field and third to move the 
cursor to the Carrier Code field). Key in the carrier code and click 
on Execute Query.
To view all orders that are of only one 
order type . . .
Press Enter the required number of times to move the cursor to the 
Type field. Key in the Type Code (i.e. R for Regular, P for Pending, 
etc.) and click on Execute Query. 
To view all orders that have a specific 
order date . . .
Press Enter the required number of times to move the cursor to the 
Order Date field. Key in the date and click on Execute Query.
Clicking on Execute Query will 
display the 
selected order 
number (1435) 
and all subsequent order numbers that are 
unconfirmed, 
unallocated and 
active.

OUTBOUND ALLOCATION
Allocating Orders in ASOR
ALLOCATION AND WAVE MANAGER 4.2 91

ASOR screen
You can complete more than one field at a time. For example, if you key in 123 in the Order Number field, 
CUST1 in the Customer Code field and CARR2 in the Carrier field, the system will call up and display all 
orders for Customer One that used Carrier Two and have an order number of 123 and higher. The more fields 
you are able to restrict; the fewer the number of records that will be retrieved and the simpler your search.
ASSIGNING LOCATION(S) TO AN INDIVIDUAL ORDER
1 Enter ASOR.
2 Key in the number of the order to which you need to assign a location(s).
3 Click on Execute Query. This will display the order number that you are querying on as well as all other 
unconfirmed orders with subsequent order numbers.
This query will 
retrieve all 
orders that 
are for customer A, use 
carrier ABC, 
are of R type 
and have an 
order date of 
01.01.06.

OUTBOUND ALLOCATION
Allocating Orders in ASOR

ASOR screen
4 The cursor should be next to the order number that you are querying on. If it is not, use the up and down 
arrow keys to move your cursor next to the order number to which you need to assign locations.
5 Click on Select. The word “Assign” will display under the order number that you selected.
NOTE If “UNASSIGNED Not yet assigned” appears under an order, this means 
that the order does not have a carrier assigned to it yet. It does not refer to unassigned locations.
When you 
query on a 
specific order 
number (order 
number 1485 
in this example), it will display along with 
all subsequent unconfirmed orders 
that do not yet 
have a location assigned 
to them.

OUTBOUND ALLOCATION
Allocating Orders in ASOR
ALLOCATION AND WAVE MANAGER 4.2 93

ASOR screen
6 Click on Assign. The system will indicate that it is running the allocation routine to assign a location to the 
selected order. 
You are taken out of the ASOR program. If it is necessary to refresh the screen, press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has 
assigned one or more locations to the order. See the section “Looking Up an Order Processed in ASOR” on 
page 95.
ASSIGNING LOCATIONS TO A SPECIFIC ORDER AND ALL SUBSEQUENT 
ORDERS 
1 Enter ASOR.
2 Key in the lowest order number to which you want to assign locations. 
3 Click on Execute Query. The system will call up and display the order number that you keyed in along 
with all other order numbers that are sequentially higher and that do not yet have a location assigned to 
them.
NOTE If you make a mistake and assign the wrong order number, click on Deselect. This will cancel the selection.
“Assign” displays under the 
selected order 
number.
Now click on 
Assign. The 
system will perform allocation 
and will assign 
a location or 
locations to the 
selected order.

OUTBOUND ALLOCATION
Allocating Orders in ASOR

ASOR screen
4 Click on Assign All. A message appears at the bottom of the screen indicating that the system is running 
the allocation routine. You are taken out of the ASOR program. If it is necessary to refresh your screen, 
press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has 
assigned locations to the orders. See the section “Looking Up an Order Processed in ASOR” on page 95.
ASSIGNING LOCATIONS TO ALL ORDERS
1 Enter ASOR.
2 Click on Execute Query. This will display all unconfirmed orders that are currently in the system and that 
do not yet have a location assigned to them.
When you 
query on a 
specific order 
number (order 
number 1485 
in this example), it will display along with 
all subsequent 
unconfirmed 
orders that do 
not yet have a 
location 
assigned to 
them.

OUTBOUND ALLOCATION
Allocating Orders in ASOR
ALLOCATION AND WAVE MANAGER 4.2 95

ASOR screen showing details of all unconfirmed orders that are currently in the system and do not 
have locations assigned to them
3 Click on Assign All. 
The system will indicate that it is running the allocation routine and you are taken out of the ASOR program. If 
it is necessary to refresh your screen, press the Home key.
You have completed the procedure. You can now go into the program LOOR to verify that the system has 
assigned locations to the orders. See the section “Looking Up an Order Processed in ASOR” on page 95.
LOOKING UP AN ORDER PROCESSED IN ASOR
1 Enter LOOR.
2 In the Order Number field, key in the number of the order that was processed in ASOR.
3 Click on Execute Query. 

OUTBOUND ALLOCATION
Manually De-Allocating Orders in DEOR

LOOR screen
The order will display on the screen. Note that the Location Status field indicates that the locations have 
been entered.
4 Click on Line Block.
5 Note that the Location Code and Warehouse Code fields have been populated by the system. If necessary, jot their data down for future reference.
6 If the Line Block has more than one line record, use the up and down arrow keys to view the details of the 
other lines.
7 When you have finished viewing all of the lines, click on Master Block and Exit to exit LOOR.
Manually De-Allocating Orders in DEOR
You use the program De-Allocate Order (DEOR) whenever it is necessary to manually remove previously 
assigned locations from an unconfirmed order. This program will remove the locations from either the entire 
order or only from the particular order lines that you specify. DEOR is restricted to orders that were allocated 
by the system; if you manually assigned locations to order lines in ENOR, you cannot de-allocate in DEOR.
When you remove the location from an order or order line, the location and its product is no longer attached to 
this order. The location and the product are now available to fill other orders. As DEOR removes the locations 
from an order, the order lines automatically change from R (Regular) to P (Pending) type lines.
The system has 
assigned 
locations 
to order 
number 
1573.
Click on 
Line Block 
to view the 
specific 
locations 
details.

OUTBOUND ALLOCATION
Manually De-Allocating Orders in DEOR
ALLOCATION AND WAVE MANAGER 4.2 97
With DEOR, the system will de-allocate the specific order or order lines that you specify regardless of other 
orders and their priority. If you wish to de-allocate orders based on their priority, you must define your order 
priorities in ORPR (Order Priorities). 
SETTING UP MANUAL DE-ALLOCATION
Orders can only be de-allocated if they are at a flow at which the Deassign Location flag in DIFP is set to Y for 
Yes. 

DIFP screen showing de-allocation activated for the flow FIPI (Finish Picking)
DE-ALLOCATING AN ENTIRE ORDER 
The following procedure will de-allocate an entire order. The system will remove previously assigned 
locations from all of the order lines.
1 Enter DEOR.
2 Key in your order number and press Enter. The system displays the details for this order, including the 
line details.

OUTBOUND ALLOCATION
Manually De-Allocating Orders in DEOR

DEOR screen
3 Click on De-Allocate All. A message appears on the screen asking, “Do you want to de-allocate all of the 
lines for this order?” 

DEOR screen showing warning message
4 Key in Y (for Yes). 
At the bottom of the screen, a message will now indicate that the system is de-allocating this order. You 
will know that the system has completed the process when the cursor returns to the top of the screen.
5 Key in the next order that you need to de-allocate or click on Exit to exit DEOR.
You have completed the procedure. You can enter LOOR to verify that the locations have been removed from 
this order. The LOOR Header Block will indicate “Missing” in the Location Status field. In the LOOR Line 
Block, the Location Code and Warehouse Code fields will be blank for all of the order lines.
Key in the 
order number and 
press Enter.
The Line 
Details 
Block.

OUTBOUND ALLOCATION
Manually De-Allocating Orders in DEOR
ALLOCATION AND WAVE MANAGER 4.2 99
DE-ALLOCATING INDIVIDUAL ORDER LINES
The following procedure will de-allocate one or more specific lines of an unconfirmed order. The system will 
only remove previously assigned locations from the lines that you specify.
1 Enter DEOR.
2 Key in the order number and press Enter. The system displays the details for this order, including the line 
details.

DEOR screen
3 Use the up and down arrow keys to move the cursor next to the line that you need to de-allocate. Click on 
Select Line. The system populates the De-Allocate Status field with the term “De-Allocate.”
4 If you need to de-allocate another line, move your cursor to that line and click on Select Line. 
5 If you make a mistake and de-allocate the wrong line, use the up and down arrow keys to move the cursor back to that line. The function key button will now display as Skip Line. 
Key in the 
order number and 
press Enter.
The Line 
Details Block 
will show 
allocated 
lines for the 
order that 
you specified.

OUTBOUND ALLOCATION
Automatic De-Allocation of Orders Based on Order Priority

DEOR screen
Click on Skip Line and “De-Allocate” will disappear from the De-Allocate Status field column for this line.
6 When you have finished selecting all of the lines, click on De-Allocate Line. A warning message appears 
on the screen. If the message indicates the correct number of lines, key in Y (for Yes). 
Another message, at the bottom of the screen, will now indicate that the system is de-allocating this 
order. You will know that the system has completed the process when the cursor returns to the top of the 
screen.
7 Key in the next order that you need to de-allocate or click on Exit to exit DEOR.
You have completed the procedure. You can enter LOOR to verify that the locations have been removed from 
this order. The LOOR Header Block will indicate “Missing” in the Location Status field. In the LOOR Line 
Block, the Location Code and Warehouse Code fields will be blank for the order lines that you specified.
Automatic De-Allocation of Orders Based on Order Priority
You can have AccellosOne 3PL perform automatic de-allocation based on the order’s priority level by setting 
the Allow Deallocate flag in ORPR (Order Priorities) to the appropriate value. If there is insufficient stock to fill 
a given order, the system will look at other orders with different priority levels to see which of these orders can 
be de-allocated in favour of the current order.
If you use RF, only orders that have not been picked will be de-allocated to fill an order with a higher priority 
level; if even a single line on an order has been picked, the entire order is disqualified from de-allocation. If 
Column for 
the DeAllocate 
Status field.
Lines 2 and 
3 will be 
de-allocated.
Skip Line 
option

OUTBOUND ALLOCATION
Automatic De-Allocation of Orders Based on Order Priority
ALLOCATION AND WAVE MANAGER 4.2 101
you do not use RF, the system will not check an order to see whether it has been picked and de-allocation can 
occur at any flow up to but not including order confirmation (COOR).
SETTING UP AUTOMATIC DE-ALLOCATION
You set up automatic de-allocation by setting the Allow Deallocate flag in ORPR to the appropriate value. If 
you set this flag to Yes and there is insufficient stock to fill the order, the system will look at other orders with 
different priority levels to see which of these orders can be de-allocated in favour of the current order.
Only those orders assigned a priority level whose Allow Deallocate flag is set to No will be de-allocated to fill 
the order whose flag is set to Yes. Normally, you would set this flag to Yes for the higher priority levels and set 
this flag to No for the lower priority levels.
When de-allocation occurs, AccellosOne 3PL will remove the locations from the order lines to be de-allocated 
and change the status of these order lines from Regular to Pending. As well, the de-allocated order will 
appear on the pending orders report.
1 Enter ORPR.
2 Click on Enter Criteria then Execute Query to retrieve your order priorities.
3 Use your arrow keys to position the cursor on the priority level that you wish to modify.
4 Press Enter until your cursor is positioned in the Allow Deallocate field.
5 In the Allow Deallocate field, key in the appropriate value (Y for Yes or N for No) and press Enter.
6 Repeat the above steps for each additional priority level that you wish to modify.

ORPR screen showing Allow Deallocate flag set to Y for Yes for priorities 1, 2 and 3
7 When you finish setting up your priority levels, click on Exit to exit. If Exit is not available, click on Return 
to Main and Exit.
ASSIGNING PRIORITY LEVELS TO ORDERS IN ENOR
You assign a priority level to an order by changing the value in the Priority field during order entry in ENOR. If 
you do not change the priority value in ENOR, AccellosOne 3PL will use the default value of five.

OUTBOUND ALLOCATION
Allocating Product Based on Shelf Life
Allocating Product Based on Shelf Life
You have two options for defining the minimum shelf life of a given product:
 you can use your standard picking profiles defined in PIPR
 you can define at the order line level the minimum shelf life 
ENTERING ORDERS WITH A SHELF LIFE BASED ON A DATE OTHER THAN THE 
SYSTEM DATE
If you select Order Date, To Ship Date or To Arrive Date as your option in the Range in Days Starting From 
field in PIPR, you must enter these dates accurately in the Header Block of ENOR.
1 Enter ENOR.
2 Enter your customer code, consignee code and sold-to code in the normal manner.

ENOR screen showing prompt for Order Date
3 Make sure that you enter the correct dates in the Order Date, To Ship Date and To Arrive Date fields.
4 Process the rest of the order in the normal manner.

OUTBOUND ALLOCATION
Allocating Product Based on Shelf Life
ALLOCATION AND WAVE MANAGER 4.2 103
OVERRIDING THE SHELF LIFE OF INDIVIDUAL ORDER LINES IN ENOR
You can define at the order line level the minimum shelf life for product being shipped out. Only inventory with 
that minimum shelf life (that is, a production date or expiry date equal to a specific date or later) will be 
selected during allocation. 
You activate the shelf life override feature by setting the Dynamic Shelf Life Calculation Method flag in ITSH 
to the appropriate value: E for Expiry Date or P for Production Date.

ITSH screen showing Dynamic Shelf Life Calculation Method flag set to E for Expiry
You override a product’s shelf life by entering the appropriate value in the Number of Days for Shelf Life 
Override field in the Line Block of ENOR. During allocation, the following calculations will occur:
1 AccellosOne 3PL will recalculate the product’s production date/expiry date from the product’s expiry date 
using the ITSH formula and shelf life duration values.
2 t will check the appropriate PIPR record to determine the Range in Days Starting From value (to arrive, 
order, to ship or system date) for the order.
3 It will subtract the number in days that you enter in the Number of Days for Shelf Life Override field from 
the appropriate date (to arrive, order, to ship, etc.) in the order header to arrive at a new date, the earliest 
acceptable production date/expiry date. 
4 It will compare the earliest acceptable production date/expiry date (step 3) with the production date/
expiry date of product in inventory (step 1). Only inventory with a production date/expiry date equal to or 
later than this date will be selected during allocation.
NOTE When you define the minimum shelf life at the order line level, you override 
the minimum shelf life defined in all your PIPR profiles whether attached to the customer in DSRP, the item in ITEM, the consignee in CONS or the item/consignee in 
CCOP.

OUTBOUND ALLOCATION
Allocating Product Based on Shelf Life
EXAMPLE
To arrive date in order header = May 15
Number of Days for Shelf Life Override = 10
Lots in inventory = lot A (production date of May 1), lot B (production date of May 5) and lot C (production 
date of May 7)
AccellosOne 3PL will subtract 10 from 15 to arrive at May 5. Only inventory with a production date of May 5 or 
later will be selected during allocation (that is, lots B and C). If you do not enter a value in this field, the 
allocation routine will search for inventory whose expiry dates satisfy the expiry date criteria that you define in 
PIPR (Picking Profile).

ENOR screen showing Number of Days for Shelf Life Override field set to 10
The following requirements must be met before you can override the shelf life for individual order lines:
 the order line type is either P for Pending or W for Weight
 the product’s expiry date is calculated from an inventory level containing the production date using an 
expiry date formula and shelf life duration defined in ITSH (Item Shipping Profile)
 the picking profile that applies to the order has a Range Based on value of expiry date and a Range in 
Days Starting From value of to ship date, to arrive date, order date or system date (that is, allocation 
date)
ALLOCATING BY SHELF LIFE PERCENTAGE
You can allocate product by a percentage of the shelf life remaining rather than a fixed number of days; that 
is, only ship product if it has a shelf life of at least say 25, 50 or 75% of the product’s total shelf life.

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic
ALLOCATION AND WAVE MANAGER 4.2 105
EXAMPLE 1
customer’s minimum shelf life percentage (PIPR) = 50%
item A’s shelf life duration and frequency in ITSH = 100 days
item B’s shelf life duration and frequency in ITSH = 200 days
on day of allocation,
item A has 40 days shelf life left
item B has 101 days shelf life left
Item A will not allocate because it has only 40% shelf life remaining. Item B, on the other hand, will allocate 
because it has more than 50% shelf life remaining.
EXAMPLE 2
If a consignee’s minimum shelf life percentage is 30% and the product being shipped is same as that in 
Example 1, both items would allocate because there is more than 30% of the total shelf life remaining on both 
items.
You set up allocation by shelf life percentage in PIPR by selecting “Shelf Life Percentage” in the Range Based 
on field. In the Minimum Remaining Shelf Life Percentage field, you enter your percentage. In ITSH you set 
up your shelf life duration and frequency for your items.
PIPR screen showing minimum remaining shelf life percentage of 40%
Allocating Orders With Reserve Logic
Reserve logic allows you to reserve inventory during order allocation at a level other than the lowest level for 
a customer. By using this option, you allow the picker to make the final selection at the lot or pallet ID level 
based on which product is most accessible. Reserve logic is designed for warehouses with bulk locations.

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic
For example, suppose you have a three-level account — Item / Lot / Pallet ID — and you wish to reserve 
inventory at level 2. When you allocate orders for this account, AccellosOne 3PL will select the lot and the 
location but not the pallet ID. The line type for the order line will be set to U for Unknown and the pallet ID will 
be shown as a plus sign (+) to indicate that it has not been selected. Once the product has been picked, the 
operator will enter the pallet ID (level 3) manually or scan it in using an RF device. At this point, the U-type 
lines will be changed to R for Regular.
In the above example, because the system has not selected a pallet ID, the operator can pick the pallet that is 
most accessible — that is, pallet 11.
SETTING UP RESERVE LOGIC
You set up reserve logic in CUST (Customer Codes) by entering the appropriate value in the Reserve Orders 
at Level Number field. 
1 Enter CUST.
2 Retrieve the customer that you wish to set up for reserve logic.
3 Press Enter until your cursor is positioned in the Reserve Orders at Level Number field.
4 In the Reserve Orders at Level Number field, key in the inventory level that you wish to reserve at and 
press Enter.
If you leave this field blank, reserve logic will be switched off and the system will select down to the lowest level of inventory.
NOTE Reserve logic is not available for items with a variable quantity breakdown. 
After allocation, AccellosOne 3PL may create multiple U-type lines from a single Ptype line in ENOR. Each U-type line will contain the same inventory entity in the same 
location and the sum of all the U-type lines will equal the total number of units of the 
P-type line. This is a normal occurrence in reserve logic and no cause for concern.
01
12
11 06
07
12

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic
ALLOCATION AND WAVE MANAGER 4.2 107

CUST (Customer Codes) screen showing Reserve Orders at Level Number field set to 2
5 Click on Return to Main and Exit to exit CUST.
ENTERING ORDERS IN ENOR
Reserve logic requires a line type of P for Pending in ENOR.
1 Enter ENOR.
2 Enter the header information for the order in the normal manner.
3 In the Line Block, set the line type to P for Pending.
4 Key in your item code/level 1 value and press Enter.

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic

ENOR screen showing the line type set to P for Pending
5 Press Enter to bypass your remain inventory levels. 
6 Key in your order quantity and press Enter. 
7 When you finish entering your order lines, click on Return to Main and Master Block. Then click on Exit to 
exit.
8 Allocate the order in the normal manner. When you allocate an order using reserve logic, AccellosOne 
3PL will change the line type from P to U for Unknown with a plus sign (+) indicating the unknown inventory levels.
CAUTION Do not enter inventory levels lower than the level 1. If you do, AccellosOne 3PL may be unable to allocate the order correctly.

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic
ALLOCATION AND WAVE MANAGER 4.2 109

Look Up Orders (LOOR) screen showing U-type line with a plus sign for pallet ID
USING RESERVE LOGIC IN A NON-RF ENVIRONMENT
If you wish to use reserve logic in a non-RF environment, you must enter ENOR after the product has been 
picked and manually change the U-type order lines to R-type order lines. You change a U-type line to R-type 
line by deleting the U-type line and creating a new R-type line.
1 Enter ENOR.
2 Retrieve the order whose line types you wish to manually change.
3 Select the first order line. Note the inventory levels, order and to ship quantities and location for this line. 
You will need this information when you create a new R-type line for the product.
4 Press Enter to position your cursor in Remark field. Then click on Delete to delete the line.
5 Click on Create Record.
6 If required, change the line type of your new line to R for Regular.
7 Enter your R-type line. You must enter all inventory levels shown on the original U-type line, the inventory 
level or levels selected by the picker, the original order line’s order and to ship quantities as well as the 
original order line’s location information.
8 Repeat the above steps for each additional order line.
9 When you finish changing all your order lines, exit ENOR and advance the order’s flows normally in 
CHOF.

OUTBOUND ALLOCATION
Allocating Orders With Reserve Logic
LOOKING UP INVENTORY IN LOEN
When you use reserve logic, AccellosOne 3PL creates a plus record in LOEN for the product on order whose 
inventory level or levels is unknown. A plus record is a temporary record in which the unknown inventory level 
is indicated by a plus sign. 
AccellosOne 3PL creates plus records at all inventory levels below the level at which you reserve inventory. 
For example, if you reserve at level 2, AccellosOne 3PL will create plus records for your level 3 values and 
level 4 values. If you reserve at level 3, AccellosOne 3PL will create plus records for your level 4 values.
The plus record for an unpicked order will show a negative available quantity and a positive on order quantity 
for the same amount. Once the product has been picked, all quantities of the plus record will be set to zero. 
Plus records for picked orders will remain on your system until you purge your inventory. They have no further 
affect on your inventory and should be ignored.
EXAMPLE
You enter an order for 10 cases with reserve logic activated for level 3 (pallet ID). The plus record for lot 101 
shows -10 cases as available and 10 cases as on order.
When you pick the 10 cases, the plus record is set to zero and the order is assigned to one of the non-plus 
records (in this example, lot 101/pallet ID 001).
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

OUTBOUND ALLOCATION
Performing Soft Allocation
ALLOCATION AND WAVE MANAGER 4.2 111

Look Up Inventory (LOEN) screen showing query at level 2 with “+” record indicating 25 cases on 
order whose pallet ID is unknown
Performing Soft Allocation
Soft allocation allows you to reserve inventory for a given set of orders without assigning locations. It is 
designed for facilities that wish to reserve inventory for an order as soon as the order is received, but only 
perform final allocation for the order much later when they are ready to ship. 
Soft allocation must be activated in CUST by setting the flag Allocate U Line (No Location) to R Line field to Y 
for Yes. The flag is only available if the Reserve Order at Level Number field is set to 1, 2 or 3.
NOTE When reserve logic is activated on your system, the available quantity for a 
given inventory entity is reserved when there is a plus record for that entity with a 
non-zero quantity. Do not attempt to ship or relocate the full available quantity for that 
inventory; only the available quantity as shown in LOEN minus the quantity of any 
plus records can be shipped or relocated.

OUTBOUND ALLOCATION
Performing Hard Allocation in OPLU
CUST screen showing soft allocation activated
Soft allocation works as follows. First, you enter a P-type order line in ENOR. When you run allocation for the 
first time by printing a document or running ASOR, AccellosOne 3PL will convert the P-type lines to U-type 
lines and create + records for inventory levels 2, 3 and 4. When you are ready to ship a particular order, you 
run allocation for the second time. AccellosOne 3PL will convert the U-type lines to R-type lines, assign all 
inventory levels and locations and generate any required replenishments.
Performing Hard Allocation in OPLU
You can perform hard allocation in OPLU (Order Line Inventory/Location Update). It offers a simpler, easierto-use alternative to performing hard allocation in ENOR by means of an R-type order line.
1 Enter OPLU.
2 Key in your order number and press Enter.

OUTBOUND ALLOCATION
Performing Hard Allocation in OPLU
ALLOCATION AND WAVE MANAGER 4.2 113
OPLU screen showing one P-type line
3 Key in your level 2/3/4 values for each order line that you wish to hard allocate. Alternatively, you can 
select your level 2/3/4 values from the inventory pick list.
OPLU screen showing inventory pick list and available quantity
Alternatively, you can select your level 2/3/4 values from the location pick list, which shows locations as 
well as quantities and all inventory levels.

OUTBOUND ALLOCATION
Performing Hard Allocation in OPLU
OPLU screen showing inventory location pick list and available quantity
4 When you finish entering/selecting your inventory levels, OPLU will show all inventory levels fully populated.
OPLU screen showing inventory levels fully populated
5 When you finish selecting your inventory levels for the hard allocation, click on Save.
6 When prompted to save your changes, click on Yes. OPLU will refresh showing a blank screen with no 
data.
7 Click on Exit to exit OPLU.
CHANGING THE ORDER QUANTITY OF AN ORDER LINE
If you change the quantity of an order line in OPLU, AccellosOne 3PL will split the order line into two: one 
order line for the new quantity that you typed in and a second order line for the difference between the original 
quantity and the new quantity.

OUTBOUND ALLOCATION
Performing Hard Allocation in OPLU
ALLOCATION AND WAVE MANAGER 4.2 115
1 Enter OPLU.
2 Retrieve the order that you wish to hard allocate.
3 Select the order line whose quantity you wish to change.
OPLU screen
4 In the New Quantity field, key in your new quantity and click on Change Quantity.
5 When prompted to confirm the change in quantity, click on Yes.
AccellosOne 3PL will split the order line into two: one order line for the new quantity that you typed in and 
a second order line for the difference between the original quantity and the new quantity.
OPLU screen showing two order lines: 7 cases (new quantity) and 3 cases (difference between new 
quantity and original quantity)
6 Click on Exit to exit OPLU.

OUTBOUND ALLOCATION
Using Wildcards and Boolean Logic in Allocation
Using Wildcards and Boolean Logic in Allocation
You can use wildcard characters and Boolean logic when entering your inventory level 2/3/4 values in ENOR. 
This feature, which is only available for P-type and W-type order lines, allows you precise control over which 
lots or pallet ID’s allocation should look at or not look at when selecting the best product to ship. With wildcard 
characters and Boolean logic, you can
 exclude a specific lot or a range of lots when shipping to a particular consignee
 include all lots starting with or ending with a particular value or set of values 
 define complex conditions using AND/OR logic in math-like statements with brackets to specify the 
order of operations
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
123%|987% Any string starting with either 123 or 987
(12%345|((98776%~%334)|!34
9%))
Any string starting with 12 and ending with 345 or (any string starting with 
98776 and ending with 334 or not equal to any string starting with 349)
NOTE Special characters such as !, % or ~ should not be used in inventory levels 
when receiving product in ENRE. If you do, allocation could ignore the meaning of the 
special character and allocate the inventory entity itself.

OUTBOUND ALLOCATION
Allocating Only Fully Filled Orders
ALLOCATION AND WAVE MANAGER 4.2 117
ENOR screen showing wildcard character in lot number (23%)
Allocating Only Fully Filled Orders
You can set up AccellosOne 3PL so that only orders that can be fully filled will be allocated; an order is 
considered to be fully filled when there is enough product in the warehouse to fill all lines on the order. If a 
single line on a given order cannot be fully filled, the system will automatically de-allocate the entire order. 
The location status of the de-allocated order in LOOR will be “Missing” and the location and warehouse code 
fields will be blank for all order lines.
Allocating only fully filled orders requires P-type or W-type lines in ENOR.
If you do not activate allocation of only fully filled orders, order lines that cannot be fully allocated will be 
processed according to the option that you select in the Change Zero Pending Line to R-Type Line field in 
DSRP.
SETTING UP ALLOCATION OF ONLY FULLY FILLED ORDERS
There are two setup programs for allocating only fully filled orders: DSRP (Depositor Shipping & Receiving 
Profile) and CONS (Consignees). The Ship Only Fully Filled Orders flag must be set to Y for Yes in both 
programs for a given customer and consignee before you can restrict allocation to fully filled orders. 

OUTBOUND ALLOCATION
Allocating Only Fully Filled Orders

DSRP screen showing Ship Only Fully Filled Orders flag set to Y for Yes

CONS screen showing Ship Only Fully Filled Orders flag set to Y for Yes for consignee A

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values
ALLOCATION AND WAVE MANAGER 4.2 119
MANUALLY DEACTIVATING ALLOCATION OF ONLY FULLY FILLED ORDERS IN 
ENOR
You can manually deactivate the allocation of only fully filled orders for a specific customer or consignee by 
entering N for No in the Ship Only Fully Filled Orders field in ENOR. 
1 Enter ENOR.
2 Enter your order header information in the normal manner.
3 When your cursor is positioned in the Distribution Type Code field, press F9 (Previous field).
4 In the Ship Only Fully Filled Orders field, key in N for No and press Enter.

ENOR screen showing Ship Only Fully Filled Orders flag set to N for No
5 Enter your order lines in the normal manner.
6 When you finish entering your order lines, click on Return to Main and Master Block. Then click on Exit to 
exit.
Allocating by Minimum Level 2, 3 and 4 Values
Minimum shipping level values in IMSL allow you to pick product based on minimum level 2, 3 and 4 values. 
For example, you can specify that you want the system to only pick product whose level 2 value is greater 
than or equal to A01. Minimum shipping level values are intended for computer products like motherboards 

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values
with revision levels such as A01, B, B99, C00, etc. As older revision levels become out of date, IMSL allows 
you to set a minimum level for shipping — that is, only ship product that is revision level 7.1 or later.
The records selected will be processed in normal FIFO/LIFO sequence according to the rules laid out in PIPR 
(Picking Profile).
You can use IMSL to specify:
 a global minimum value
 a range (greater than or equal to the minimum value and less than another value)
 a series of ranges (greater than or equal to the minimum value 1 and less than value 1.1, greater than or 
equal to the minimum value 2 and less than value 2.1, etc.)
There are four fields used in IMSL to set a minimum value:
 Starting Position and Length fields (used to determine the “less than” value for ranges)
 Value field (used to determine the minimum value)
 Exception field (reserved for future use)
Allocation will select all inventory records with a level 2 value that is:
 greater than or equal to B 
REMARK: Because there is only a single value in the Exception Block, IMSL will ignore any values that you 
enter in the Starting Position and Length fields.
Allocation will select all inventory records with a level 2 value that is:
 greater than or equal to B01 and less than C (because the Starting Position and Length fields are both 1, 
the “less than” value is C — not C02) 
 greater than or equal to C02
REMARK: Because there are two entries in the Exception Block, IMSL will treat the pair as a range. The first 
entry will be the minimum value and the second entry will be the “less than” value.
EXAMPLE 1
Item Minimum Shipping Level Flag (DILP) = Yes for the second 
level of inventory
Values in Exception Block
B
Starting Position = 1
Length = 1
EXAMPLE 2
Item Minimum Shipping Level Flag (DILP) = Yes for the second 
level of inventory
Values in Exception Block
B01
C02
Starting Position = 1
Length = 1

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values
ALLOCATION AND WAVE MANAGER 4.2 121
Allocation will select the inventory records whose level 3 value is:
 greater than or equal to A99 and less than B (no values)
 greater than or equal to B09 and less than C (for example, B09, B10, B11, etc.)
 greater than or equal to C99 and less than D (no values)
 greater than or equal to D00 (for example, D00, D01, D05, E10, F12, etc.)
SETTING UP YOUR ITEM MINIMUM SHIPPING LEVEL PARAMETERS
You set up your item minimum shipping level parameters in IMSL.
EXAMPLE 3
Item Minimum Shipping Level Flag (DILP) = Yes for the third 
level of inventory
Values in Exception Block
A99
B09
C99
D00
Starting Position = 1
Length = 1
NOTE Because there are multiple entries in the Exception Block, IMSL will pair 
each entry with the entry that follows and treat the two entries as a range. The first 
entry will be the minimum value and the second entry will be the “less than” value.
FIELD DESCRIPTIONS
Customer Code Mandatory
Your customer code.
Item Code Mandatory
Your item code.

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values
Starting Position Mandatory
If you are defining a range or series of ranges, you must specify in the Starting 
Position and Length fields which characters in your IMSL value your inventory 
level value should be less than. For example, if you set the starting position to 
1 and the length to 1, then your inventory level value must be less than the 
first character of your IMSL value(s). Alternatively, if you set the starting position to 3 and the length to 2, then your inventory level value must be less than 
the third and fourth characters of your IMSL value(s).
If you are not defining a range, you do not need a starting position and length. 
Set both these fields to 1.
Length Mandatory
See Starting Position field.
Value Mandatory
If you add a single entry to the Exception Block in IMSL, the single entry will 
be your minimum value and only product greater than or equal to it will be allocated. Any values that you enter in the Starting Position and Length fields (for 
example, 1 and 1) will be ignored because there is no “less than” value.
If you add multiple entries to the Exception Block in IMSL, the program will 
treat each two entries as a pair. The first entry in the pair (entry 1) will be the 
minimum value and the second entry in the pair (entry 2) will be the “less than” 
value. The system will use the starting position and length values to determine 
which part of the IMSL value the item’s inventory level should be less than.
EXAMPLES
starting position = 1
length = 1
Your inventory level value must be less than the first character of your IMSL 
value(s). 
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values
ALLOCATION AND WAVE MANAGER 4.2 123
1 Enter DILP and set the Item Minimum Shipping Level Flag to Yes for the inventory level that the minimum 
value applies to.

DILP screen showing Item Minimum Shipping Level Flag set to Yes for level 2
2 Enter IMSL.
starting position = 3
length = 2
Your inventory level value must be less than the third and fourth characters of 
your IMSL value(s).
After evaluating entries 1 and 2, the allocation routine will evaluate entries 2 
and 3. This time entry 2 will be the minimum value and entry 3 will be the “less 
than” value. When entries 2 and 3 are evaluated, the allocation routine will 
look at entries 3 and 4. This process will continue until the last entry in the 
Exception Block is reached and there is no longer a “less than” value.
Exception Mandatory
The Exception field in IMSL is reserved for future use. You must enter an 
operand (for example, =) in order to add an entry to the Exception Block, but 
the operand that you enter is ignored by IMSL.
FIELD DESCRIPTIONS

OUTBOUND ALLOCATION
Allocating by Minimum Level 2, 3 and 4 Values

Item Minimum Shipping Level
3 Key in your customer code and press Enter.
4 Key in your item code and press Enter.
5 In the Starting Position field, key in the starting position of the characters in your IMSL value that your 
inventory level should be less than and press Enter.
6 In the Length field, key in the length of your IMSL value and press Enter. 
7 In the Value field, key in your level 2, 3 or 4 value and press Enter. 
8 In the Exception field, key in = as your operand and press Enter.
9 Repeat the above two steps for each additional value that you wish to add to the Exception Block.

IMSL screen showing five values in the Exception Block
10 When you finish setting up your minimum shipping values, click on Return to Main and Master Block. 
Then click on Exit to exit.

OUTBOUND ALLOCATION
Reserving a Minimum Level of Inventory for High Priority Orders
ALLOCATION AND WAVE MANAGER 4.2 125
PERFORMING ITEM MINIMUM SHIPPING LEVEL ALLOCATION
1 Enter a P-type order line in ENOR. Make sure that no value is entered for the inventory level that the minimum value applies to in either ENOR or any EDI program.
Reserving a Minimum Level of Inventory for High Priority Orders
You can reserve a certain level of inventory for high priority orders by setting the Evaluate Minimum flag in 
ORPR (Order Priorities) to the appropriate value and defining an item’s minimum quantity in ITEM.
For example, suppose you stock motherboards and you wish to keep five motherboards in stock at all times 
in order to handle rush orders. First you set the value in the Minimum Quantity field in the Quantity 
Breakdown Block of ITEM to five. Then you set the Evaluate Minimum flag to Y for Yes for all priorities except 
the highest. For the highest priorities — say priorities 1 and 2 — you would set the Evaluate Minimum flag to 
N for No.
When a regular order is received for motherboards (say, priority 5 or 6), the system will evaluate the 
minimum; that is, check whether the order can be filled without reducing the on-hand quantity to less than 
five. If there are only five motherboards in stock, they will be “locked” and the regular order will not be allowed 
to allocate them.
When a high priority order is received for motherboards (say priority 1 or 2), the minimum will not be 
evaluated because the Evaluate Minimum flag has been set to N for No. The high priority order will ignore the 
minimum quantity defined in ITEM and will allocate however many of the remaining five motherboards that it 
needs.
SETTING UP A MINIMUM LEVEL OF INVENTORY
1 Enter ITEM.
2 Retrieve the item that you wish to set up for a minimum level of inventory.
3 Click on Quantity Breakdown Block.
4 Enter your minimum quantity in the Minimum Quantity field.

OUTBOUND ALLOCATION
Reserving a Minimum Level of Inventory for High Priority Orders

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

OUTBOUND ALLOCATION
Reserving a Minimum Level of Inventory for High Priority Orders
ALLOCATION AND WAVE MANAGER 4.2 127

ORPR screen showing Evaluate Minimum flag set to N for No for priorities 1 and 2
12 When you finish setting up your priority levels, click on Exit to exit. If Exit is not available, click on Return 
to Main and Exit. 
ASSIGNING PRIORITY LEVELS TO ORDERS IN ENOR
See “Assigning Priority Levels to Orders in ENOR” on page 101.

OUTBOUND ALLOCATION
Reserving a Minimum Level of Inventory for High Priority Orders

ALLOCATION AND WAVE MANAGER 4.2 129
PICK LINES AND REPLENISHMENT
Overview .......................................................................................................... 131
Types of Pick Lines.................................................................................... 133
Working With Multiple Pick Line Locations for the Same Product ............. 133
Setting Up a Fixed Position Pick Line........................................................... 134
1 — Setting the Activate Directed Move Stock Flag in COMP................... 134
2 — Setting the Assign Location Flag in DIFP........................................... 135
3 — Setting Up Your Picking Profile in PIPR ............................................. 135
4 — Setting Up Your Replenishment Options in DSRP............................. 139
5 — Setting Up Your Location Type in LOTP ............................................ 141
6 — Assigning Your Location Type to Your Pick Line Locations in LOCA 141
7 — Defining Your Picking Parameters for Replenishment in ILOP .......... 142
8 — Setting Up Your Pick Line in PIIT ....................................................... 143
9 — Activating Your Pick Line Using ENOR/REPI..................................... 150
Setting Up a Floating Pick Line ..................................................................... 151
Mixing Fixed Position and Floating Locations in the Same Pick Line....... 153
Setting Up a Pick Line With Replenishment by Inventory Level 2 ............. 154
Putting Away to a Pick Line Using Directed Put-Away................................ 156
1 — Setting Up Your Location Type in LOTP ............................................ 157
2 — Setting Up Your Put-Away Profile Code in PUPR .............................. 157
3 — Attaching Your PUPR Profile to DSRP............................................... 159
4 — Setting Up Your Overflow Locations in PIIT (Optional) ...................... 160
5 — Defining Your Put-Away Rules in ILOP .............................................. 161
Performing Your Replenishments ................................................................. 162
Running the Relocate to Pick Line Audit (RPAU) ...................................... 162
Confirming Your Replenishments in REPI ................................................. 163
Looking Up a Replenishment in LOEN ...................................................... 164
Generating Top Up Replenishments in TURE ........................................... 165
Deleting a Replenishment.......................................................................... 166
Deleting an Order that Triggered a Replenishment ................................... 167
Confirming Your Replenishments in RFRP (RF Only) ............................... 167

PICK LINES AND REPLENISHMENT
Overriding Replenishment Priorities in RFRO ........................................... 172
Troubleshooting Pick Lines and Replenishments....................................... 173
Reports............................................................................................................. 173

PICK LINES AND REPLENISHMENT
Overview
ALLOCATION AND WAVE MANAGER 4.2 131
Overview
A pick line is a special area within a warehouse used to store fast moving product in smaller than pallet-sized 
units for quick picking. Before you can pick from a pick line in AccellosOne 3PL, the following conditions must 
be met:
 you must set up and activate a pick line for the item that you wish to pick
 the order quantity must be a partial 
You can set up your system to perform replenishment automatically or you can manually replenish your pick 
line through a product relocation. If you activate automatic replenishment, the system will generate one or 
more replenishments whenever the quantity in the pick line falls below the minimum quantity for the location 
that you specify. Replenishment occurs during order allocation and is governed by the replenishment parameters that you define in PIIT (Pick Line Item Assignment) and ILOP (Replenish from Bulk).
You must confirm your replenishments in REPI (Relocate to Pick Line) or through an RF replenishment 
program.
The following examples show four scenarios: a pick from bulk rather than the pick line, a pick from the pick 
line with no replenishment, a pick from the pick line with a case replenishment and a pick from the pick line 
with a pallet replenishment.
Order quantity = 120 CS
EXAMPLE 1 — NO PICK LINE PICKING
Quantity breakdown of item: 100 CS/PALLET
Order quantity: 120 CS (1.2 PALLETS)
pick line
system picks 120 CS from bulk
rather than pick line because
order quantity is not a partial
bulk area
no activity in pick line

PICK LINES AND REPLENISHMENT
Overview
There is a maximum of five steps to follow in picking from and replenishing a pick line:
EXAMPLE 2 — PICK LINE PICKING WITHOUT REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 50 CS
Minimum pick line quantity: 20 CS
Order quantity = 10 CS
system picks 10 CS from pick line; no
replenishment occurs because remaining
quantity is greater than minimum (50 - 10 = 40,
which is greater than minimum)
pick line
bulk area
EXAMPLE 3 — PICK LINE PICKING WITH CASE REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 25 CS
Minimum pick line quantity: 20 CS
Replenish to quantity: 100 CS
system picks 10 CS from pick line pick line
Order quantity = 10 CS replenishment is required because 25 -10 = 15
and 15 is less than minimum quanity;
system replenishes 85 CS from bulk (100 - 15)
bulk area
EXAMPLE 4 — PICK LINE PICKING WITH PALLET REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 25 CS
Minimum pick line quantity: 20 CS
Replenish to quantity: 1 PLT
system picks 10 CS from pick line pick line
Order quantity = 10 CS replenishment is required because 25 -10 = 15
and 15 is less than minimum quanity;
system replenishes 1 PLT from bulk
bulk area

PICK LINES AND REPLENISHMENT
Overview
ALLOCATION AND WAVE MANAGER 4.2 133
TYPES OF PICK LINES
AccellosOne 3PL supports two kinds of pick lines: fixed position pick lines and floating pick lines. A fixed 
position pick line is a pick line in which each item is assigned a fixed location. A floating pick line is a pick line 
in which the items on it are not assigned fixed locations. Any pick line location can contain any pick line item.
WORKING WITH MULTIPLE PICK LINE LOCATIONS FOR THE SAME PRODUCT
Multiple pick line locations (either fixed position or floating) for the same item is not recommended for product 
that falls within the same FIFO/LIFO range or product in which FIFO/LIFO picking is deactivated for the pick 
line (that is, allocation will pick the oldest product in the pick line even if there is older product in bulk). In 
ENOR
PROM/ 
PROR
RPAU
REPI
CHOF/
COOL
When you print your order documents 
in PROM or PROR, the system assigns 
locations to each order line. If the 
quantity in a pick line location falls 
below the minimum quantity, the 
system orders a replenishment and 
updates the quantity in the replenish 
from location.
You enter your P-type order lines in 
ENOR (not required if your orders are 
generated through EDI). 
If the picker performs replenishment, a 
message such as "Pick 1 pallet from 
bulk location X" will print on the pick 
sheet.*
If the picker does not perform 
replenishment, you can print RPAU 
(Relocate Pick Line Audit Report). This 
report, which generates an audit 
number, shows all your replenishments.*
* Printing the pick sheet and RPAU are optional in 
an all-RF environment.
You confirm your replenishments in 
REPI (Relocate to Pick Line) or RFRP 
(RF Replenish). AccellosOne 3PL 
updates the quantity in the replenish to 
location.
You confirm your orders in CHOF or 
COOL.
Picker does 
No replenishment Yes

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
these scenarios, allocation will tend to pick from and replenish to the first location only (“first” meaning first in 
location code sequence) and ignore the other pick line locations for the product.
For example, suppose you have three pick line locations for item A and each location contains product with a 
date code of November 1. Allocation will pick from the first location until the quantity falls below the minimum 
quantity; at that point, it will order a replenishment. 
No more pick line picking can take place from the first location until the replenishment is performed even 
though there is available and eligible product in the second and third locations. Only when all November 1 
product in bulk has been moved to the first pick line location and picked from that location will allocation pick 
from the second and third pick line locations.
You can avoid the allocation problems that arise from multiple pick locations for the same product by defining 
one “super” location for the three slot positions on your pick line and activating picking substitution in PSPR 
(RF Substitution Profile Code). 
Setting Up a Fixed Position Pick Line
There are eight setup programs and two operational programs for setting up a fixed position pick line:
 COMP (Company Parameters)
 DIFP (Depositor Workflow Profile)
 PIPR (Picking Profile)
 DSRP (Depositor Shipping and Receiving Profile)
 LOTP (Location Type)
 LOCA (Locations)
 ILOP (Item Location Profile - Replenish from Bulk)
 PIIT (Pick Line Item Assignment)
 ENOR (Enter Order)/REPI (Relocate to Pick Line Location)
1 — SETTING THE ACTIVATE DIRECTED MOVE STOCK FLAG IN COMP
The Activate Directed Move Stock flag must be set to Yes.

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 135
COMP screen showing Activate Directed Move Stock flag
2 — SETTING THE ASSIGN LOCATION FLAG IN DIFP
In the DIFP record attached to the customer whose items you wish to pick from the pick line, make sure that 
the Assign Location flag has been set to Yes for at least one outbound flow code.

Depositor Workflow Profile (DIFP)
3 — SETTING UP YOUR PICKING PROFILE IN PIPR
In the PIPR record attached to the customer whose items you wish to pick from the pick line, there are five 
flags to be set:

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
 Break Quantity at SKU Class
 Use FIFO/LIFO for Pick Line Picking or Skip
 Exclude Pick Line Stock When Bulk Picking
 Replenishment Message on Pick Documents
 Break at SKU Class for Replenishment
FIELD DESCRIPTIONS
Break Quantity at SKU 
Class
Make sure that the Break Quantity at SKU Class field has been set to the 
appropriate value. For example, if your quantity breakdown is PALLETS/
CASES and you have two SKU classes (1 = pallets, 3 = cases and the like), 
you must select the “Break at SKU Class 1” option in PIPR so that the system 
will pick CASES (the next smaller SKU class) from your pick line.
For multiple pick line locations for the same item in different SKU’s, you must 
break at two SKU classes — for example, “1,2” or “1,3”. 
If you select the “Ignore SKU classes” option, the allocation routine will not 
pick from your pick line.
Use FIFO/LIFO for Pick 
Line Picking or Skip
N = No
Y = Yes
S = Skip
In this field, you specify whether or not you want allocation to follow a strict 
FIFO/LIFO sequence when pick line picking.
If you set this flag to N for No, the allocation routine will completely ignore 
FIFO/LIFO requirements when picking from the pick line. In other words, any 
stock that is found in a pick line location is considered acceptable no matter 
what the FIFO/LIFO setting is. 
If you set this flag to Y for Yes, the allocation routine will pick product in the 
pick line according to your FIFO/LIFO requirements.That means that product 
inside or outside of the pick line are all being allocated under the same FIFO/
LIFO requirement.
If you set this flag to S for Skip, skip mode will be activated. In skip mode, 
automatic replenishment is deactivated and the picker can select any pick line 
inventory from any pick line location whose level 1 value matches the level 1 
value of the order line. See the section “Picking Cases from a Pick Line in 
CASE” in the RF User’s Guide.

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 137
Exclude Pick Line Stock 
When Bulk Picking
blank = No
N = No
Y = Yes
In this field, you specify how you want allocation to handle situations in which 
a few cases of the oldest product are in the pick line and the order quantity 
consists of one or more full pallets. 
EXAMPLE
order quantity = 2 pallets
oldest product = 3 cases in pick line
If you set this flag to N for No, the allocation routine will pick the three cases in 
the pick line first. Then it will generate a replenishment and pick the remaining 
quantity from that replenishment. 
If you set this flag to Y for Yes, AccellosOne 3PL will pick the full order quantity 
from bulk even though the oldest product is in the pick line.
Replenishment Message 
on Pick Documents
N = No
Y = Yes
If you set this field to N for No, a message such as “Pick 1 pallet from bulk 
location X” will print on the document. You use the No option when the picker 
performs replenishment of the pick line.
If you set this field to Y for Yes, a message such as “If product not there, see 
replenishment staff” will print on the pick document. You use the Yes option 
when someone other than the picker performs replenishment of the pick line. 
If you do not use the core pick document, replenishment messages require a 
custom document from HighJump.
Break at SKU Class for 
Replenishment
This field allows you to define a sequence of SKU classes for replenishment. 
For example, you can replenish partial pallets first followed by full pallets or 
you can replenish full pallets first followed by partial pallets. You can also 
specify a combination of SKU classes for replenishment in a particular 
sequence such as Break at SKU Class 1, 2, 3.
If you leave this field blank, full pallets will be replenished first (assuming that 
the Replenish to SKU Code field in PIIT is set to PLT).
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line

Picking Profile (PIPR)
The picking profile that you define in PIPR can apply to all customers or to a particular customer. If required, it 
can apply to an item or series of items or it can apply to a consignee.
If you are attaching picking profiles to items and consignees as well to customers, the following logic will 
apply:
 the profile that you attach to DSRP is the default
 if you attach a picking profile to an item in ITEM, it will override the profile in DSRP
 if you attach a picking profile to a consignee in CONS, it will override the profiles in DSRP and ITEM

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 139
4 — SETTING UP YOUR REPLENISHMENT OPTIONS IN DSRP
If you use automatic replenishment, you must activate or deactivate replenishment optimization in DSRP. 
FIELD DESCRIPTIONS
Replenishment Optimizationblank = No
N = No
Y = Yes
In this field, you specify whether you want AccellosOne 3PL to pick directly 
from bulk when the replenishment quantity is less than or equal to the order 
quantity; that is, the replenishment quantity is fully allocated to a particular 
order/order line. It is recommended for customers that use absolute FIFO/
LIFO as an effective way of eliminating redundant replenishments.
NOTE Replenishment optimization is only available if the replenishment 
quantity is fully allocated to a particular order/order line at the time that the 
replenishment is generated. If you allocate line 1 of an order at 10:00 am and 
then allocate line 2 of the same order at 11:00 am and the replenishment 
quantity is fully allocated to the sum of the two order lines, no optimization will 
occur because the condition — replenishment quantity is fully allocated to an 
order — was not met at the time of the first replenishment.
If you set this field to N for No, AccellosOne 3PL will generate a replenishment 
from bulk to restore the pick line to its optimal quantity. Once the replenishment is confirmed, it will generate a pick from the pick line to fill the order line.
If you set this field to Y for Yes, AccellosOne 3PL will pick the replenishment 
quantity directly from bulk instead of replenishing the pick line and then picking it.
EXAMPLE
Quantity breakdown = 90 cases
Order quantity = 160 cases (one pallet and 70 cases)
Replenishment quantity = one pallet
Pick line location = A100 (50 cases) of oldest lot
Bulk location = BLK001 (120 cases) of the next newest lot

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line

Depositor Shipping and Receiving Profile (DSRP)
Replenishment Optimization = N for No
Allocation will perform the following actions:
 pick 50 cases from the pick line location because this location contains the 
oldest product
 generate a replenishment of one pallet (90 cases) for the pick line 
 pick the full pallet of 90 cases from the pick line
 generate a second replenishment of 30 cases (the remaining product in 
location BLK001) for the pick line
 pick the balance of the order quantity (20 cases) from the pick line
Replenishment Optimization = Y for Yes
Allocation will perform the following actions:
 pick 50 cases from the pick line location because this location contains the 
oldest product
 pick one full pallet of 90 cases from bulk
 generate a replenishment of 30 cases (the remaining product in location 
BLK001) for the pick line
 pick the balance of the order quantity (20 cases) from the pick line
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 141
5 — SETTING UP YOUR LOCATION TYPE IN LOTP
In the LOTP record attached to your pick line locations, make sure that the Directed Picking and Pick Line 
flags are both set to Y for Yes.

Location Type (LOTP)
6 — ASSIGNING YOUR LOCATION TYPE TO YOUR PICK LINE LOCATIONS IN 
LOCA
In this program, you attach the pick line location type that you set up in LOTP to your pick line locations in 
LOCA.

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line

Locations (LOCA)
7 — DEFINING YOUR PICKING PARAMETERS FOR REPLENISHMENT IN ILOP
In this program, you define the picking parameters for your replenishments. You can have the system 
replenish product based on receipt date, isolator zone, quantity of product in the location and other criteria 
that you specify. 
The picking parameters for replenishments are defined in the Replenish from Bulk Block of ILOP. These 
parameters are identical to the picking parameters in the Picking Block of ILOP. If you do not define replenishment parameters in ILOP, the system will use the default parameters for picking. The default replenishment 
value is the first option in each group of your standard logical groups for picking. 
See “Setting Up the Item Location Profile for Picking (ILOP)” on page 67 for complete information on the 
various replenishment options available. 
1 Enter ILOP.
2 Do one of the following:
If you are creating a new ILOP 
profile:
If you are attaching your 
replenishment parameters to an 
existing ILOP profile:
a) Key in an item location profile 
code and press Enter.
b) Key in a meaningful description 
for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to 
update.
b) Click on Type Block.
c) Proceed to step 5.

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 143
3 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, 
press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your 
arrow keys to position your cursor over the appropriate code and click on Select Code. 
4 Use your pick list function to select any warehouse code for your overflow warehouse.
5 Use your pick list function to select any location code for your overflow location code.
6 Press your up or down arrow key in the Types Block until the Replenish from Bulk option is displayed.

Blank Replenishment screen
7 Proceed to enter your replenishment parameters. Refer to “Setting Up a New Profile in ILOP” on page 77 
for instructions on how to assign parameters to sequences in ILOP.
8 When you finish entering all your sequences, click on Return to Main and then Type Block.
9 Click on Master Block and then Exit to exit the program.
8 — SETTING UP YOUR PICK LINE IN PIIT
You set up your pick lines in PIIT (Pick Line Item Assignment). In this program, the following parameters need 
to be defined:
 the location of the pick line (fixed or non-floating pick lines only)
 the item or items on the pick line
 the replenishment quantity
 the minimum quantity 
 the SKU code that you will be picking from the pick line
 the SKU code that you will be using to replenish the pick line
 whether replenishment occurs manually or automatically

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
You can have multiple items for multiple customers assigned to the same pick line location or you can set up 
one pick line location for each item/customer. As well, you can have multiple pick line locations for the same 
item; for example, you can have one pick line location for EACHES (item x) and another pick line location for 
CASES (item x). 
You need to set up one PIIT record for each unique combination of customer code, item code, warehouse/
location code and pick line SKU code. For example, if you wish to assign three items to the same pick line 
location, you would have to set up three PIIT records — one for each item.
You cannot change the customer code, item code, warehouse/location code or pick line SKU code of an 
existing PIIT record. If you wish to change any of these values, you must delete the record and then recreate 
it with the correct values.
NOTE Before changing or deleting a pick line location, you must delete or confirm 
any replenishments for that location.
FIELD DESCRIPTIONS
Customer Code Mandatory
The customer whose item(s) you wish to assign to a pick line.
Item Code Mandatory
The item that you wish to assign to a pick line.
Inventory Level 2 Optional
See “Setting Up a Pick Line With Replenishment by Inventory Level 2” on 
page 154 for further information.
Warehouse Code Mandatory for fixed or non-floating pick lines
The warehouse in which the pick line is located.
Location Code Mandatory for fixed or non-floating pick lines
The pick line’s location. The location that you specify must be assigned a location type whose Pick Line flag has been set to Yes in LOTP (Location Types).

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 145
Use Floating Pick Line to 
Hold Demand REPI
Reserved for future use.
Pick Line SKU Code Mandatory
The SKU code of your pick line — that is, the SKU code that you will be picking from this pick line. The SKU codes that you can enter in this field depend 
upon the value you entered in the Break Quantity at SKU Class field in the 
PIPR (Picking Profile) record attached to this item; if no PIPR profile is 
attached to this item, the system will use the PIPR profile attached to the customer. 
If you are unable to enter the SKU code that you wish to pick from your pick 
line, return to PIPR and check that you have set up this profile correctly.
Replenish To Quantity Mandatory 
The optimal quantity allowed for the location. When the on-hand quantity in 
the location falls below the quantity that you specify in the Minimum Quantity 
field, the system will replenish whatever quantity is needed to restore the location to its optimal quantity — that is, the difference between the available 
quantity and the replenish to quantity.
For example, if you currently have 20 cases in your pick line and your replenish to quantity is 100 cases, the system will perform a replenishment of 80 
cases.
If your replenish to SKU code is different from your pick line SKU code (for 
example, you pick cases from the pick line but replenish in pallets), then the 
system will round up to the nearest pallet and replenish that quantity.
CAUTION Do not set the replenish to quantity to the location’s maximum 
capacity as defined in LOCA (Locations). If you do, AccellosOne 3PL may 
appear to over-replenish the location. 
Replenish To SKU Code Mandatory 
The SKU code for the Replenish To Quantity field. This SKU code may differ 
from the SKU code in the Pick Line SKU Code field (for example, you can pick 
in CASES from the pick line but replenish in PALLETS).
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
Minimum Quantity Mandatory 
If the available quantity in the pick line location falls below the minimum quantity that you specify in this field, the system will perform automatic replenishment. The number that you enter in this field is always in the SKU code that 
you specified in the Pick Line SKU Code field.
NOTE The minimum quantity must always be less than the replenish to 
quantity. If the minimum and replenish to quantities are expressed in different 
SKU codes (for example, your minimum is in CASES and your replenish to is 
in pallets), you must convert one of your quantities — pallets to cases or 
cases to pallets — to ensure that the replenish to quantity is greater than the 
minimum quantity.
Setting the Minimum Quantity to Zero
If you set the minimum quantity to zero and the Automatic Replenish to Pick 
Line flag to Y for Yes, no replenishment will take place when the available 
quantity in the pick line reaches zero unless a replenishment is required to fill 
a current order.
EXAMPLE 1
The quantity in the pick line is three cases and the order quantity is three 
cases. AccellosOne 3PL will pick three cases from the pick line but no replenishment will take place until another order requires a pick from the pick line.
EXAMPLE 2
The quantity in the pick line is three cases and the order quantity is four cases. 
AccellosOne 3PL will pick three cases from the pick line, perform a replenishment and them pick the remaining one case from the pick line.
CAUTION Automatic replenishment with a zero minimum quantity is only 
available for a single pick line location/item/SKU code combination. You cannot use this function with two or more pick line locations assigned the same 
item code and SKU code.
Critical Quantity in Pick 
Location
This field is used to establish a critical level of inventory in a pick line location 
requiring a high priority replenishment. The critical quantity can be either 
greater than or less than the minimum quantity.
If you specify a critical quantity and if the available quantity in the pick line 
location falls below the critical quantity, one of the following will occur:
 If you use system-assisted tasking, you can create an ActiveDesktop alert 
for the supervisor warning him or her of the situation.
 If you use system-driven tasking, the replenishment task will be re-assigned 
to a higher priority.
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 147
Rounding Method for 
Replenish To Quantity
This field makes it possible to perform partial replenishments to a pick line 
location. Partial replenishments reduce the number of partial non-pick line 
locations and eliminate multiple replenishments for the same location. 
For example, suppose a given pick line location requires a 60-case replenishment. Depending on the option that you choose, AccellosOne 3PL will either 
increase the replenishment quantity to 65 or 70 cases to clean out a given 
location or reduce the replenishment quantity to 55 or 50 cases to clean out a 
given location.
There are four options in this field:
D for Down
Round down to the available quantity in a location and create a single REPI 
for each replenishment.
U for Up
Round up to the full available quantity in a location and create a single REPI 
for each replenishment.
R for Round Up or Down
Round up or down to the available quantity in a location and create a single 
REPI for each replenishment.
N for No Rounding
Pick the exact quantity required to make up the replenish to quantity and perform multiple replenishments if required.
Allow On-Demand 
Replenishment
N = No
Y = Yes
This field makes it possible to force AccellosOne 3PL to generate replenishments outside of normal order allocation processing. For example, your pick 
line is well stocked for the current day's orders and you wish to pick your 
orders first from the pick line and worry about replenishing your pick line on a 
later shift.
You activate on-demand replenishment by setting the Allow On-Demand 
Replenishment to Y for Yes. Then you write a background cron job in Unix to 
run according to a predefined schedule; depending on the command that you 
use, you can run replenishments for all customers of a given company, for a 
given customer of a given company or a specific item belonging to a specify 
customer.
You can also generate on-demand replenishments in TURE (Top Up Replenishments).
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
1 Enter PIIT
Force Replenishment 
When Needed
Y = Yes
N = No
If you set this flag to Y for Yes, allocation will force a replenishment when the 
product on order cannot be picked from the pick line because of FIFO constraints and a replenishment cannot be generated because the pick line quantity is above the minimum. If you set this flag to N for No, allocation will 
generate a partial pick from bulk when the required product is not in the pick 
line. 
NOTE The Yes option (force a replenishment) must be used with extreme 
caution as it may cause over-crowding in your pick line.
Number of Days to Empty 
Out a Location if Not 
Used
Reserved for future use
Automatic Replenish to 
Pick Line
Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL will automatically generate a 
replenishment record for each pick line location whose quantity falls below the 
minimum quantity. You can either confirm or delete this record in REPI (Relocate to Pick Line). If you set this flag to N for No, automatic replenishment will 
not occur. You must manually replenish the pick line by means of RELO (Relocate Inventory).
Exclude Bulk When no 
Floating Locations Available
Reserved for future use
Release in Full Quantity Reserved for future use
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
ALLOCATION AND WAVE MANAGER 4.2 149

Pick Line Item Assignment
2 Click on Create Record.
3 Use your pick list (press F10 to enter the pick list, click on Execute Query then Select) to select the 
appropriate customer that you wish to attach to the pick line.
4 Use your pick list to select the item that you wish to attach to the pick line.
5 Press Enter to bypass the Inventory Level 2 field.
6 In the Pick Line SKU Code field, key in the SKU code that you will be picking from in this pick line and 
press Enter.
If you wish to set up a static pick 
line:
If you wish to set up a floating 
pick line:
a) Key in your warehouse code and 
press Enter
b) Use your pick list to select the 
appropriate location for your pick 
line.
c) If you are unable to access any 
locations for your pick line, make 
sure that you have assigned a 
location type to the location 
whose Pick Line flag has been 
set to Yes. You set up location 
types in LOTP (Maintain Location Types).
a) Press Enter to bypass the Warehouse Code and Location Code 
fields. Floating pick lines do not 
have defined locations in PIIT. 

PICK LINES AND REPLENISHMENT
Setting Up a Fixed Position Pick Line
7 In the Replenish to Quantity field, key in your “replenish to” quantity and press Enter.
8 In the Replenish To SKU Code field, key in the SKU code you want the system to use when it replenishes 
the pick line and press Enter.
9 In the Minimum Quantity field, key in the minimum quantity for this item and press Enter. Make sure that 
the minimum quantity is less than the “replenish to” quantity.
10 In the Rounding Method for Replenish to Quantity field, key in the appropriate value (D for Down, U for 
Up, R for Round Down or Up or N for No Rounding) and press Enter.
11 In the Allow On-Demand Replenishment field, key in N for No or Y for Yes and press Enter.
12 In the Force Replenishment When Needed field, key in N for No or Y for Yes and press Enter. 
13 Press Enter to bypass the Automatic Replenish to Pick Line field.
14 When you finish adding your pick line, click on Return to Main to exit create mode.

Pick Line Item Assignment (PIIT) screen showing a replenishment to quantity of 1 pallet when the 
quantity falls below 10 cases
15 Click on Exit to exit.
9 — ACTIVATING YOUR PICK LINE USING ENOR/REPI
Pick line locations that are empty will not be replenished. To fill empty pick line locations with enough product 
to activate replenishments, follow the steps below:
1 Make sure that there is enough product in bulk to move to the pick line.
2 Create an order for one case of each item going into the pick line.
3 Allocate the order normally. AccellosOne 3PL will generate all the replenishments.
4 Perform your replenishments in REPI.

PICK LINES AND REPLENISHMENT
Setting Up a Floating Pick Line
ALLOCATION AND WAVE MANAGER 4.2 151
5 Delete the original order.
Setting Up a Floating Pick Line
A floating pick line is a pick line in which the items on it are not assigned fixed locations. Any pick line location 
can contain any pick line item. You set up a floating pick line by creating a record in PIIT (Pick Line Item 
Assignment) with a customer code, item code, pick line SKU code, etc. but no warehouse code and location. 
Once you set up your PIIT pick line, any location in your warehouse whose location type in LOTP has the 
Directed Picking, Directed Put-Away and Pick Line flags set to Y for Yes is defined as a floating pick line.
In addition to the setup programs for fixed position pick lines, there are two additional steps for setting up a 
floating pick line:
 you define your put-away parameters in the Replenish to Floating Pick Line Block of ILOP (Item Location Profile)
 you define the way in which AccellosOne 3PL calculates the minimum quantity for a pick line location in 
PIPR (Picking Profile)
The put-away parameters for replenishing a floating pick line are defined in the Replenish to Floating Pick 
Line Block of ILOP. These parameters are identical to the put-away parameters in the Put-Away Block of 
ILOP. If you do not define replenishment parameters in ILOP, the system will use the default parameters for 
put-away.
Enter ILOP and select Replenish to Floating Pick Line as your type. Then refer to “Item Location Profile for 
Put-Away (ILOP)” on page 4 for complete information on the various replenishment options available.
NOTE If you set up two or more pick line locations in PIIT for the same item and the 
same pick line SKU code, make sure that they both have inventory in them. If one of 
the locations is empty, the allocation routine will not replenish that location. To relocate inventory to an empty pick line, use RELO (Relocate Inventory) to move product 
from elsewhere in the warehouse.
NOTE Floating pick lines have two sets of replenishment parameters in ILOP. The 
Replenish from Bulk parameters define which locations in bulk you pick from in order 
to replenish the pick line. The Replenish to Floating Pick Line parameters define 
which pick line locations you put-away to when replenishing your floating pick line.

PICK LINES AND REPLENISHMENT
Setting Up a Floating Pick Line

Item Location Profile Code (ILOP) screen showing Replenish to Floating Pick Line type
The way in which AccellosOne 3PL replenishes a floating pick line depends upon the value that you select in 
the Replenishment Based on Eligible Records field in PIPR (Picking Profile). If you set this flag to Y for Yes, 
AccellosOne 3PL will replenish a floating pick line location based on the minimum quantity of eligible records
(for example, all inventory older than June 1). If you set this flag to N for No, AccellosOne 3PL will replenish a 
floating pick line location based on the minimum quantity of all inventory in the pick line.

PICK LINES AND REPLENISHMENT
Mixing Fixed Position and Floating Locations in the Same Pick Line
ALLOCATION AND WAVE MANAGER 4.2 153

Picking Profile (PIPR)
Mixing Fixed Position and Floating Locations in the Same Pick Line
In order to mix floating and fixed position locations in the same pick line, you must set up at least two isolator 
codes for your warehouse: one for your floating locations and another (or a number of others) for your fixed 
locations.
1 Make sure that all your floating locations have the same isolator code and that this isolator code is not 
attached to any fixed position location or fixed position location item.
2 Set up your ILOP profile for your fixed position locations in the normal manner. In the Replenish From 
Bulk block, you can select any option that you wish from the Isolator group.
3 Set up a second ILOP profile for your floating locations. In the Replenish to Floating Pick Line block, 
select the “Use exact match isolator code” option from the Isolator group. You must use this option in 
each ILOP sequence in the Replenish to Floating Pick Line block.
If you do not attach the exact match parameter to your ILOP profile for floating locations, allocation could 
put-away floating location product to a fixed position location for a different product.
Replenishment Based 
on Eligible 
Records field

PICK LINES AND REPLENISHMENT
Setting Up a Pick Line With Replenishment by Inventory Level 2
Setting Up a Pick Line With Replenishment by Inventory Level 2
Replenishment by inventory level allows you to define separate pick line locations for each level 1/level 2 
combination in your warehouse. Each pick line location can be assigned a specific level 1/level 2 entity with 
its own minimum and replenishment quantities.
For example, suppose your level 1 value is Nike shoes and your level 2 value is shoe size and your minimum 
quantity is 25. If you deactivate replenishment by inventory level, AccellosOne 3PL will perform a replenishment whenever the quantity of a particular shoe regardless of size falls below the minimum quantity. The 
replenishment will consist of any size of that shoe.
If you activate replenishment by inventory level, AccellosOne 3PL will perform a replenishment whenever the 
quantity of a particular shoe and size falls below the minimum quantity. The replenishment will consist of the 
shoe and size whose quantity fell below the minimum quantity.
There are three requirements for pick lines with replenishment by inventory level 2:
 the Use FIFO/LIFO for Pick Line Picking flag in PIPR must be set to N for No
 the Replenish Pick Line up to Level flag in PIPR must be set to 2
 there must be one record in PIIT for each unique level 1/level 2 combination in your pick line
NOTE Replenishment by inventory level 2 is only available for fixed position pick 
lines. You cannot use this function with floating pick lines.
Replenish 
up to Level
Minimum 
Quantity in PIIT
Available Quantity in 
Pick Line Replenishment
1 25 size 8 (10 units), size 9 (10 units), 
size 10 (12 units)
No replenishment occurs because 
total quantity (10 + 10 + 12) is 
greater than the minimum quantity.
2 25 size 8 (10 units), size 9 (10 units), 
size 10 (12 units)
Replenishment takes place 
because the quantity for each size 
is less than the minimum quantity.

PICK LINES AND REPLENISHMENT
Setting Up a Pick Line With Replenishment by Inventory Level 2
ALLOCATION AND WAVE MANAGER 4.2 155

Picking Profile (PIPR)
CAUTION If you create a record in PIIT with the level 1 specified but no level 2 — 
for example, NIKE001 but no size — AccellosOne 3PL may generate unnecessary 
replenishments in REPI (Relocate to Pick Line).
Replenish 
Pick Line up 
to Level 
field set to 2

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away

Pick Line Item Assignment (PIIT)
ENTERING ORDERS IN ENOR
Replenishment by inventory level requires that you enter both level 1 and level 2 for each order line in ENOR. 
If you enter a single inventory level in ENOR, AccellosOne 3PL will use your item-level default in PIIT; that is, 
it will pick from the pick line and then replenish — if necessary — based on the minimum quantity defined for 
the item. The replenishment will consist of any level 2 value for that item — not necessarily the level 2 value 
on the order line that triggered the replenishment.
If there is no item-level default defined in PIIT, AccellosOne 3PL will pick orders from bulk and ignore the pick 
line.
Putting Away to a Pick Line Using Directed Put-Away 
You can put-away to a pick line using directed put-away by means of the program PUPR (Put-Away Profile 
Code). Putting away to a pick line works well in two cases: the pick line item has a single inventory level or the 
pick line item has multiple inventory levels but your picking is very relative — that is, your range in days value 
in PIPR is very high and there are a large number of eligible inventory records from which to pick. Putting 
away to a pick line is not recommended when you are picking absolute or when you are picking relative but 
the range of acceptable inventory records is very small. 
There are five setup programs for a pick line with directed put-away:
 You set the Directed Put-Away flag in LOTP to Yes for the location type attached to your pick line location
 You set up your put-away profile code in PUPR (Put-Away Profile Code). 
 You attach your PUPR profile to DSRP (Depositor Shipping & Receiving Profile). 
 You set up your overflow locations in PIIT (Pick Line Item Assignment). 
Inventory 
Level 2 
must be 
defined

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away
ALLOCATION AND WAVE MANAGER 4.2 157
 You define your put-away rules in ILOP (Item Location Profile).
1 — SETTING UP YOUR LOCATION TYPE IN LOTP
Make sure that the Directed Put-Away, Directed Picking and Pick Line flags are all set to Yes for the pick 
line’s location type.

Location Type (LOTP)
2 — SETTING UP YOUR PUT-AWAY PROFILE CODE IN PUPR
In PUPR you set up your directed put-away options for your pick line. There are two put-away options in this 
program:
 You can specify that product is to be always put away to the pick line or that only partial quantities are 
put away to the pick line. These options requires custom RF programming.
 You can specify an item receipt hold profile. You set up item receipt hold profiles in IRHP (Item Receipt 
Hold Profile). If you specify an item receipt hold profile, product with a hold attached to it will be put away 
to the location assigned to that hold in IRHP instead of to the pick line. 
PUPR is attached to DSRP (Depositor Shipping and Receiving Profile). If you attach a PUPR profile to ITEM, 
that profile will override the customer-level default in DSRP. For example, if you wish to put away to the pick 
line all product for a given customer with the exception of one item, you would create two PUPR profiles as 
follows: 
 you would set your first one to Always or Partial and attach it to your DSRP profile 
 you would set your second one to None and attach it to the item that you do not wish to put away to the 
pick line.

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away
FIELD DESCRIPTIONS
Put-Away to Pick Line A = Always
P = Partial
N = None
If you select A for Always, the system will always attempt to put away to a pick 
line location. If you select P for Partial, the system will only attempt to put 
away partial quantities to the pick line. If you select N for None, the system will 
never attempt to put away to a pick line location and the item will be assigned 
a non-pick line location.
When you select either the Always and Partial options, the system will compare the size and weight of the item being received against the capacity and 
weight limitations of the pick line location and attempt to put away in a pick line 
location that satisfies your ILOP parameters. If the size or weight of the item 
exceeds the capacity of the pick line location, the system will attempt to put 
away to a pick line overflow location defined in PIIT.
If there are no pick line overflow locations or if the pick line overflow locations 
are full, the system will attempt to put away to a non-pick line location using 
your ILOP parameters.
Pick Line Isolator Code 
(ISOL)
Optional
The isolator code that you enter in this field applies only to your pick line and 
pick line overflow locations. It may differ from your ILOP isolator code that is 
attached to the item, which applies only to non-pick line locations.
If you enter an isolator code in this field, the following rules will apply:
 if putting away to non-pick line locations, the system will use the isolator 
code(s) for the ILOP profile attached to the item that you are putting away
 if putting away to pick line or pick line overflow locations and ILOP is set to 
“use only exact match isolator code,” the system will use your PUPR isolator code
 if putting away to pick line or pick line overflow locations and ILOP is set to 
“use any overflow isolator code,” the system will use your ISOL overflow 
isolator code 
If you do not enter an isolator code in this field, the system will use the isolator 
code(s) for the ILOP profile attached to the item that you are putting away.
Range in Days from Oldest LotSee “Put-Away Profile Code (PUPR)” on page 31 for further information..

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away
ALLOCATION AND WAVE MANAGER 4.2 159
1 Enter PUPR.
2 Key in your put-away profile code and press Enter.
3 Key your put-away profile code description and press Enter.
4 In the Put-Away To Pick Line field, key in the appropriate value (A for Always, P for Partials or N for 
None) and press Enter.
5 In the Pick Line Isolator Code field, key in your isolator code and press Enter or press Enter with this field 
blank to bypass the option.
6 If required, enter your item receipt hold profile code and set the Item Receipt Hold Override flag to the 
appropriate value. If you do not require an item receipt hold profile code, press Enter to bypass this field.

Put-Away Profile Code (PUPR) screen showing a profile code for putting away partials only to the pick 
line
7 Click on Return to Main and Exit to exit.
3 — ATTACHING YOUR PUPR PROFILE TO DSRP
In this program, you attach your PUPR profile to your Depositor Shipping & Receiving Profile (DSRP). The 
PUPR profile that you specify in a given DSRP profile will apply to all customers to which you have attached 
that DSRP profile. If you attach a PUPR profile to a given item in ITEM, that profile will override the customerlevel default in DSRP.
Range Based on See “Put-Away Profile Code (PUPR)” on page 31 for further information..
FIELD DESCRIPTIONS

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away
1 Enter DSRP.
2 Click on Enter Criteria and Execute Query to retrieve the profile that you wish to modify.
3 In the Put-Away Profile Code field, key in your put-away profile code and press Enter or use your pick list 
to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query 
to display the list of codes. Then position your cursor over the appropriate code using your arrow keys 
and click on Select to select it. 

Depositor Shipping and Receiving Profile (DSRP) showing Put-Away Profile Code = P2
4 When you finish modifying your code, click on Return to Main and Exit to exit.
4 — SETTING UP YOUR OVERFLOW LOCATIONS IN PIIT (OPTIONAL)
In PIIT, you can define overflow locations for a pick line into which you are putting away. If the pick line 
location is full, the system will attempt to put away inbound product to the first overflow location. If the first 
overflow location is full, the system will attempt to put away the product to the second overflow location (if 
any). If the second overflow location is full, the system will attempt to put away product to the third overflow 
location (if any). 
If all overflow locations are full or you do not specify any overflow locations, the product will be directed to 
normal ILOP processing.
Overflow locations must be defined as pick line locations.
1 Enter PIIT.
2 Click on Enter Criteria and Execute Query to retrieve the PIIT record that you wish to modify.

PICK LINES AND REPLENISHMENT
Putting Away to a Pick Line Using Directed Put-Away
ALLOCATION AND WAVE MANAGER 4.2 161
3 Click on Overflow Block.
4 Key in your first sequence number and press Enter.
5 Key in your warehouse code for your first overflow location and press Enter.
6 Key in the location code of your first overflow location and press Enter.
7 Repeat steps 4 to 6 for each additional overflow location.

Pick Line Item Assignment (PIIT) screen showing three overflow locations
8 When you finish adding all your overflow locations, click on Master Block and Exit to exit.
5 — DEFINING YOUR PUT-AWAY RULES IN ILOP
You define your put-away rules in the PIIT Location Capacity group in ILOP. See “PIIT Location Capacity 
Group (I8500)” on page 18.

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
Item Location Profile screen showing PIIT Location Capacity group
Performing Your Replenishments
There are two steps to follow in performing a replenishment:
 you do one of the following: you run the Relocate Pick Line Audit Report (RPAU) or you use the pick 
document with the replenish from message
 you confirm the replenishment in either Relocate to Pick Line (REPI) or RFRP (RF Replenish) 
RUNNING THE RELOCATE TO PICK LINE AUDIT (RPAU)
Refer to the Standard Reports Guide. 
NOTE If the replenishment involves picking multiple inventory entities from a single 
location, AccellosOne 3PL will create one or more order lines with order and ship 
quantities of zero. These order lines are required to satisfy uniqueness constraints in 
the database and should be ignored. 

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
ALLOCATION AND WAVE MANAGER 4.2 163
CONFIRMING YOUR REPLENISHMENTS IN REPI
You confirm your replenishments in REPI (Relocate to Pick Line). When you perform allocation through the 
printing of a shipping document or some other process, the system will generate a REPI screen or record for 
each replenishment with all fields (Order Number, From Warehouse Code, Relocate Units, etc.) fully filled in. 
If the replenishment involves picking one inventory entity from multiple locations or multiple inventory entities 
from a single location, a REPI screen will be generated for each unique location/entity combination. 
If required, you can manually override the “replenish from” locations in REPI. The system will then replenish 
from the location or locations that you specify rather from the system-selected location or locations.
1 Enter REPI.
2 Click on Execute Query. The system will retrieve a REPI record for each replenishment that met the criteria that you specified in the previous step. For example, if you have a single pick line location and the 
system replenishes it from two locations, you will have to two records in REPI — one for each “from” 
location.
CAUTION If you do not confirm your replenishments in REPI, the allocation routine will nevertheless assume that replenishment has taken place and the quantities 
in the “replenish from” locations will be adjusted accordingly. However, the “replenish 
to” locations — that is, the pick line — will not be replenished on the system. As a 
result, you may be unable to confirm an order if the system considers the pick line to 
be empty.
If you wish to confirm all your 
replenishments:
If you wish to restrict your 
confirmation to certain 
replenishments:
a) Proceed to next step. a) Press Enter to position your cursor in the field that you wish to 
restrict on. You can restrict on 
customer code, item code, level 
2, 3 and 4 values, order number, 
audit number*, from warehouse 
code/location and to warehouse 
code/location. 
b) Key in your restriction value; for 
example, your order number, 
customer code, etc.
c) If you wish to include a second 
field in your restriction, repeat 
the above two steps for your second value.
* Only available if you run RPAU (Relocate to Pick Line Audit Report).

PICK LINES AND REPLENISHMENT
Performing Your Replenishments

Relocate to Pick Line (REPI) screen showing two replenishments
3 If you wish to manually override the “replenish from” location, press Enter to position your cursor in the 
From Location Code field. Then use your pick list (press F10 to enter the pick list, click on Execute Query 
to query and then Select) to select the appropriate from location code.
4 Click on Relocate Done.
5 Do one of the following:
6 When you finish confirming your replenishments, click on Exit to exit.
LOOKING UP A REPLENISHMENT IN LOEN
Replenishments appear in the Replenishment column of the Location Block in LOEN. The replenish from 
quantity is shown as a positive quantity while the replenish to quantity is shown as a negative quantity. When 
you confirm your replenishments in REPI, all quantities in the Replenishment column revert to zero.
1 Enter LOEN.
2 Key in the customer code, item code and inventory levels of the product being moved to the pick list and 
click on Execute Query.
If reserve logic is activated on 
your system:
If reserve logic is NOT activated 
on your system:
a) Enter the missing inventory 
level(s) and click on Relocate 
Done.
a) Repeat the above step for each 
additional record in REPI that 
you wish to confirm.
a) Continue to click on Relocate 
Done for each record in REPI 
that you wish to confirm.

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
ALLOCATION AND WAVE MANAGER 4.2 165
3 Click on Location Block.
4 If required, use your down arrow to scroll down in the Location Block.
5 Press Enter to display the Replenishment column.

Look Up Inventory (LOEN) screen showing a replenishment of 5 cases from FA001 to FA008
6 Continue to press Enter to scroll horizontally through the various columns in the Location Block.
7 When you finish looking up your replenishments, click on Inventory and Exit to exit.
GENERATING TOP UP REPLENISHMENTS IN TURE
You can generate top up or on demand replenishments in TURE. Top up replenishments are governed by the 
replenishment rules set up in PIIT. They differ from regular replenishments in that they are not triggered by an 
order picking from a pick line location. If you run TURE and if the quantity in a pick line location is less than 
the minimum quantity, a replenishment will be generated.
On demand replenishment must be activated in PIIT (Pick Line Item Assignment) by setting the Allow On 
Demand Replenishment flag to Y for Yes.
1 Enter TURE.
2 Proceed to enter your top up restrictions. You can restrict top up replenishments to all product belonging 
to a specific customer or to a specific item.

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
TURE screen showing top up restrictions
3 If required, you can restrict your replenishments to a specific location. Key in your location code and 
press Enter. To restrict your replenishments to a range of locations, use one or more of the following 
operands:
4 Click on Process.
DELETING A REPLENISHMENT 
If you delete a replenishment in REPI, the system will remove the product from your pick line and restore it to 
its original location. However, the system will not undo the quantity that you picked from your pick line. As a 
result, your inventory may be out of balance and you may need to relocate inventory in RELO in order to 
correct it.
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
Location 1 (BULK) Location 2 (PICK LINE)
Original Quantity
Replenishment
Balance
Order picks 10 CS
New Balance
Delete Replenishment
Final Balance
10 CS
-50 CS
50 CS
N/A
50 CS
+100 CS
50 CS
2 CS
+50 CS
52 CS
-10 CS
42 CS
-50 CS
-8 CS

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
ALLOCATION AND WAVE MANAGER 4.2 167
After the deletion, the quantity in the bulk location is restored to its original value (100 CS), but the pick line 
quantity is now -8 CS instead of 2 CS (the original value). Therefore, you will have to relocate some product 
from the bulk location to the pick line location in order to restore the pick line to its original value.
DELETING AN ORDER THAT TRIGGERED A REPLENISHMENT
If you delete an order after performing and confirming the associated replenishments, there is no need to 
make any adjustments because your inventory will be in balance. If, on the other hand, you delete an order 
before picking the product and performing the replenishment, you may need to delete your replenishment. 
Refer to the previous section “Deleting a Replenishment” on page 166 for complete instructions.
CONFIRMING YOUR REPLENISHMENTS IN RFRP (RF ONLY)
If you confirm your replenishments in RF, you use the program RFRP (RF Replenish). Refer to “Confirming 
Your Replenishments in REPI” on page 163 for general information about replenishment logic in AccellosOne 
3PL. 
There are three replenishment modes to choose from in RFRP. These modes allow you to rank replenishments by urgency and perform urgent replenishments first, less urgent replenishments next and non-urgent 
replenishments last. They make it possible to improve the efficiency of your pick line picking and ship orders 
faster.
The three replenishment modes are:
The sort order of replenishment records in RFRP is as follows: order date/time, relocation date/time, 
customer code, level 1 value, to location code and quantity (lowest quantity first). The quantity calculation in 
RFRP depends upon the replenishment mode.
EXAMPLE OF REPLENISHMENT MODES
NOTE RFRP shows all replenishments; that is, both replenishments that are currently ready to be performed as well as those that will be performed in the future 
when there is space in the pick line location. Locations that are full and cannot be 
replenished immediately are indicated by the flag F for Full.
Active Demand Only replenishment records in which the on hand quantity in the 
pick line location is less than the order quantity for the location are 
displayed.
Threshold Minimum Only replenishment records in which on-hand quantity in the pick 
line location is less than the minimum quantity defined in PIIT are 
displayed.
All All replenishment records are displayed.

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
Suppose you have the following five replenishments:
Active Demand Mode
rule: on hand quantity in location < order quantity for location (replenishment is urgent because there is a 
picking task for the location and not enough product to pick)
replenishment records displayed: 4, 5
sort order of replenishment records: 5, 4 (calculate on hand qty - on order qty and then display lowest records 
first)
Threshold Minimum Mode
rule: on hand quantity in location < than minimum quantity (replenishment is less urgent because there is no 
picking task for the location)
replenishment records displayed: 1, 2
sort order of replenishment records: 1, 2 (calculate on hand qty - on minimum qty and then display lowest 
records first)
All Modes
rule: none (display all replenishments)
sort order of replenishment records: same as Active Demand mode
RFRP also allows you to perform partial replenishments. For example, if your replenishment quantity is two 
pallets and your forklift can only carry one pallet at a time, you can replenish one pallet to the pick line and 
leave the remaining pallet to be replenished at a later time. Partial replenishments are useful whenever a full 
replenishment would be undesirable because of equipment limitations or lack of space in the pick line 
location.
1 Key in RFRP and press Enter.
Replenishment #Pick Line 
Location
Order Quantity 
for Location
On-Hand Quantity in 
Location
Minimum Quantity for 
Location (PIIT)
1 P1 0 10 25
2 P2 0 20 25
3 P3 30 30 25
4 P4 60 40 25
5 P5 80 50 25

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
ALLOCATION AND WAVE MANAGER 4.2 169

RFRP screen
2 If required, you can restrict your replenishments to a particular warehouse by press F3 (EW) and entering 
your warehouse code.
3 If required, change your replenishment mode to D for Active Demand or I for Threshold Minimum and 
press Enter. If you press Enter without changing your replenishment mode, AccellosOne 3PL will use the 
default value of A for All.
AccellosOne 3PL will retrieve the appropriate replenishment records. 
RFRP screen showing a replenishment from A103 to B102 (B102 is not full)

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
4 Do one of the following:
5 If you wish to change the sequence of replenishments so as to perform certain replenishments first and 
postpone other replenishments to a later time, use your up and down arrow keys to scroll through the list.
6 Press F3 to position your cursor in the UI field.

RFRP screen showing prompt for UI value
If you wish to confirm all your 
replenishments:
If you wish to restrict your 
confirmation to certain 
replenishments:
a) Proceed to next step. a) Press F1 (Enter Criteria).
b) Press Enter to position your cursor in the field that you wish to 
restrict on. You can restrict on 
customer code, item code, level 
2, 3 and 4 values, UI value, order 
number, from warehouse code 
and to warehouse code.
c) Key in your restriction value; for 
example, your order number, 
customer code, etc.
d) If you wish to include a second 
field in your restriction, repeat 
the above two steps for your second value.
e) If you wish to see the number of 
replenishments that meet your 
restrictions, press F3 (Cq).
f) When you finish entering your 
query criteria, press F2 (Execute 
Query). AccellosOne 3PL will 
retrieve an RFRP record for each 
replenishment that meets the criteria that you specified.

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
ALLOCATION AND WAVE MANAGER 4.2 171
7 Enter or scan in your UI value or lowest inventory value. 
RFRP screen showing prompt for quantity
8 Key in your quantity and press Enter. 
RFRP screen showing prompt for to location
9 Enter or scan in your to location and press Enter.
10 When you finish confirming your replenishments, press F4 the required number of times to exit.
CANCELLING A REPLENISHMENT
The Hold command in RFRP allows you to cancel a replenishment. When you cancel a replenishment, the 
following actions occur in AccellosOne 3PL: 
 all replenishments for the same inventory entity and from location are deleted
 a supervisor is prompted to log in and place the product on suspend hold
 the order lines for the inventory entity that triggered the replenishment is zeroed out, a P-type line is created and allocation is called 
 the RF operator is presented with an alternate replenishment task 

PICK LINES AND REPLENISHMENT
Performing Your Replenishments
RFRP screen showing supervisor login message
OVERRIDING REPLENISHMENT PRIORITIES IN RFRO
RFRO allows you to manually override the default sort sequence for replenishments in RFRP by means of a 
priority number override. For example, if you set the priority number override of replenishment 1 to 10 and the 
priority number override of replenishment 2 to 5, replenishment 2 will be listed before replenishment 1 in 
RFRP.
1 Enter RFRO.
2 Retrieve the replenishment whose priority you wish to override.
3 In the Priority Number Override field, key in your new priority number and press Enter.
4 Click on Save to save your changes.

PICK LINES AND REPLENISHMENT
Troubleshooting Pick Lines and Replenishments
ALLOCATION AND WAVE MANAGER 4.2 173
RPRO screen showing replenishment with a priority number override value of 60
5 Click on Exit to exit.
Troubleshooting Pick Lines and Replenishments
Refer to the Allocation Troubleshooting Guide for instructions on troubleshooting your pick lines and replenishments. 
Reports
Refer to the Standard Reports Guide.

PICK LINES AND REPLENISHMENT
Reports

ALLOCATION AND WAVE MANAGER 4.2 175
DIRECTED MOVE SYSTEM
Overview .......................................................................................................... 176
Setting Up the Directed Move System .......................................................... 177
Activating Directed Move in COMP............................................................ 178
Setting Up Your Hold Code(s) in HOLD..................................................... 178
Setting Up Your Directed Move Profile Code in DMPA ............................. 179
Attaching Your Directed Move Profile Code to a Warehouse in WARE .... 181
Setting Up Your Directed Move Parameters in ILOP................................. 182
Setting the Directed Put-Away and Staging Flags in LOTP....................... 184
Assigning Suggested Locations for a Directed Move in DMPR ................. 185
Printing Labels for a Directed Move.............................................................. 188
Printing the Directed Move Report (DMVR) .................................................. 189
Removing Suggested Locations for a Directed Move ................................. 190
Confirming the Directed Move ....................................................................... 190
Confirming the Directed Move in RELO..................................................... 191
Confirming the Directed Move in RFRL ..................................................... 193
Looking Up Directed Moves in LOEN............................................................ 194
Pallet Restacking ............................................................................................ 195
Opportunistic Cross-Docking ........................................................................ 197
“Ship In Given Hour” Option....................................................................... 198
Setting Up Opportunistic Cross-Docking (M7010-21, M7040-43).............. 199
Setting Up Opportunistic Cross-Docking (M7030) ..................................... 200
Attaching a Shipping Lane to an Order in ENOR....................................... 201

DIRECTED MOVE SYSTEM
Overview
Overview
The directed move system allows you to relocate confirmed product from a temporary inbound location to a 
final put-away location; the relocation occurs after any auto take-off holds placed on the product have expired 
and uses the directed move parameters defined in ILOP to select the best possible location for the product.
When you confirm the directed move in RELO or RFRL, AccellosOne 3PL will display the optimal location 
according to your ILOP parameters; you are free to accept this location or to override it with another location 
of your choice.
The directed move system is designed for facilities that store their inbound product in a blast freezing or paint 
shop location for a fixed number of days before moving it to a final put-away location. Because the inventory 
is confirmed while still in the temporary location, you can perform invoicing and EDI confirmation transactions 
on the actual receipt date while final put-way is deferred to a later date.
Directed moves can also be used to reverse or undo a relocation. For example, you move product to an 
outbound staging area after picking an order; the order is cancelled and you wish to return the product to a 
rack location using directed move to select the best location.
The directed move system can generate a report and labels showing both the inventory entities as well as the 
suggested locations for those entities.

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
ALLOCATION AND WAVE MANAGER 4.2 177
Setting Up the Directed Move System
There are six setup programs for the directed move system:
 COMP (Company Code)
 HOLD (Hold Types)
 DMPA (Directed Move Profile)
 WARE (Warehouse and Location Format)
 ILOP (Item Location Profile)
DMPR
OFFICE/WAREHOUSE
If you use RF, you confirm the directed move in
RFRL. If you do not use RF, you confirm the
directed move in RELO.
OFFICE
You assign suggested locations to the product in
DMPR (Directed Move Processing) and, if
required, print labels or a report.
OFFICE
You time-stamp and confirm the receipt in CHRF
(Time-Stamp and Confirm Receipt).
3
END
4
ENRE
CHRF
ENRE/RF
OFFICE
You enter the receipt in ENRE (Enter, Modify and
Delete Receipt).
1
OFFICE/WAREHOUSE
You assign a temporary location to the product
manually in ENRE or you have the system assign
the temporary location using directed put-away
logic.
2
RF?
RELO RFRL
No Yes

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
 LOTP (Location Type)
ACTIVATING DIRECTED MOVE IN COMP
You activate the directed move system in COMP by setting the Activate Directed Move Inbound flag to Yes.
COMP screen showing Activate Directed Move Inbound flag
SETTING UP YOUR HOLD CODE(S) IN HOLD
If you use the directed move system to move product that has been on hold, you need at least one hold type 
in HOLD with the Auto Take-Off flag set to Y for Yes. 

HOLD screen showing a blast freezing hold code that will expire in five days

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
ALLOCATION AND WAVE MANAGER 4.2 179
SETTING UP YOUR DIRECTED MOVE PROFILE CODE IN DMPA
You set up your directed move profile code in DMPA (Directed Move Profile). You then attach your directed 
move profile code(s) to the appropriate warehouses in WARE. If you have multiple warehouses on your 
system, you can create a unique directed move profile code for each warehouse or you can use the same 
directed move profile code for all warehouses.
In DMPA, you specify the following parameters:
 whether or not you want holds to be removed automatically when you generate suggested locations for 
your directed move in DMPR
 whether or not you want to require the authorization of a supervisor before an operator can override a 
suggested put-away location (RF only)
 the report and label documents that you can print in DMPR
FIELD DESCRIPTIONS
Directed Move Profile 
Code
Mandatory
Your directed move profile code.
Description Mandatory
The description for your directed move profile code.
Automatically Remove 
Expired Hold Codes
Y = Yes
N = No
If you select Y for Yes, AccellosOne 3PL will automatically remove any 
expired auto take-off holds from product when you run DMPR. If you select N 
for No, you must run HATO (Holds Auto Take-Off) to remove expired auto 
take-off holds from product.
Supervisor Authorization 
Required to Override 
Location
Y = Yes
N = No
If you select Y for Yes, the operator can only override the system suggested 
location in RELO/RFRL if the change has been authorized by a supervisor. If 
you select N for No, the operator can override the system suggested location 
in RELO/RFRL without the authorization of a supervisor.
The Yes option requires at least one operator defined as a supervisor. A 
supervisor is an operator in OPER whose Supervisor Flag has been set to Y 
for Yes.

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
1 Enter DMPA.
2 Key in your directed move profile code and press Enter.
3 Key in a description for your new code and press Enter.
4 In the Automatically Remove Expired Hold Codes field, key in Y for Yes or N for No and press Enter.
5 In the Supervisor Authorization Required to Override Location field, key in Y for Yes or N for No and 
press Enter.
6 In the Document Code for Report field, key in your document code for the report and press Enter or press 
Enter with the field blank for no document code.
7 In the Document Code for Label field, key in your document code for the label and press Enter or press 
Enter with the field blank for no document code.
8 When you finish entering your directed move parameters, click on Return to Main.
Enable Automated Pallet 
Consolidation
See “Pallet Restacking” on page 195 for further information.
Staging Warehouse Code See “Pallet Restacking” on page 195 for further information.
Staging Location Code See “Pallet Restacking” on page 195 for further information.
Document Code for 
Report
Optional
The report printed for product on directed move. This report must be set up as 
a document in DOCU.
Document Code for Label Optional
The label printed for product on directed move. This label must be set up as a 
document in DOCU.
FIELD DESCRIPTIONS

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
ALLOCATION AND WAVE MANAGER 4.2 181

DMPA screen showing document codes for printing labels and reports
9 Click on Exit.
ATTACHING YOUR DIRECTED MOVE PROFILE CODE TO A WAREHOUSE IN 
WARE
You attach your directed move profile code(s) to the appropriate warehouse(s) in WARE.

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System

WARE screen showing directed move profile code 1 attached to warehouse 1
SETTING UP YOUR DIRECTED MOVE PARAMETERS IN ILOP
You set up your directed move parameters by selecting the Directed Move Stock option in the Type Block of 
ILOP (Item Location Profile) and then selecting the appropriate option from each logical group. After setting 
up your directed move stock ILOP profile, you attach this profile to the appropriate items in ITEM. The 
directed move stock options in AccellosOne 3PL are identical in every way to the put-away options described 
in “Standard Logical Groups for Put-Away” on page 5. The same standard logical groups are used and each 
group contains the same options.
1 Enter ILOP.
2 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, 
press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your 
arrow keys to position your cursor over the appropriate code and click on Select Code. 
If you are creating a new ILOP 
profile:
If you are attaching your directed 
move parameters to an existing 
ILOP profile:
a) Key in an item location profile 
code and press Enter.
b) Key in a meaningful description 
for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to 
update.
b) Click on Type Block.
c) Proceed to step 5.

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System
ALLOCATION AND WAVE MANAGER 4.2 183
3 Use your pick list function to select the warehouse code for your overflow warehouse. If you have a single warehouse, use this warehouse.
4 Use your pick list function to select the location code for your overflow location code.
5 Press your up or down arrow key in the Type Block until the Directed Move Stock option is displayed.

Blank Directed Move Stock screen
6 Proceed to enter your directed move parameters. Refer to “Setting Up a New Profile in ILOP for Directed 
Put-Away” on page 23 for instructions on how to assign parameters to sequences in ILOP.
7 When you finish entering all your sequences, click on Sequence Block and Return to Main and then Type 
Block.

DIRECTED MOVE SYSTEM
Setting Up the Directed Move System

ILOP screen showing the selected parameters for the first pass
8 Click on Type Block.
9 Click on Master Block and then Exit to exit the program.
SETTING THE DIRECTED PUT-AWAY AND STAGING FLAGS IN LOTP
The final put-away locations for directed moves must be assigned a location type in LOTP whose Directed 
Put-Away flag has been set to Y for Yes and whose Staging flag has been set to N for No.

DIRECTED MOVE SYSTEM
Assigning Suggested Locations for a Directed Move in DMPR
ALLOCATION AND WAVE MANAGER 4.2 185

LOTP screen showing Directed Put-Away flag set to Y for Yes
Assigning Suggested Locations for a Directed Move in DMPR
When you assign suggested locations for a directed move in DMPR, AccellosOne 3PL will automatically 
remove any expired auto take-off holds from the product being moved if the Automatically Remove Expired 
Holds flag in DMPA is set to Y for Yes. 
You can select the product to be moved by location (that is, one location at a time), by location type code, by 
isolator code, by zone code, by expiry date, by customer code, by level 1/2/3/4 value, by hold code and by 
audit number.
1 Make sure that the product is confirmed and that any auto take-off holds have expired. If you have set the 
Automatically Remove Expired Hold Codes flag in DMPA to No, you must run HATO to remove these 
holds.
2 Enter DMPR.

3 Key in your warehouse code and press Enter.

DIRECTED MOVE SYSTEM
Assigning Suggested Locations for a Directed Move in DMPR
DMPR screen
4 If required, enter your location code, location type code, isolator code, zone code, expiry date, customer 
code, levels 1, 2, 3 or 4 values, hold code or audit number.
5 If the Enable Automated Pallet Consolidation flag is set to Yes, key in N for No and press Enter.
6 When you finish entering your search criteria, click on (Execute Query).
AccellosOne 3PL will display all confirmed product in the warehouse and location that you specified that 
is no longer on hold and meets any search criteria that you entered. 

DIRECTED MOVE SYSTEM
Assigning Suggested Locations for a Directed Move in DMPR
ALLOCATION AND WAVE MANAGER 4.2 187

DMPR screen showing selected product
7 Do one of the following:
AccellosOne 3PL will insert an asterisk to indicate that a particular inventory entity is selected. If you 
make a mistake and wish to undo your selection(s), click on Deselect All.
8 Click on (Move/Undo). AccellosOne 3PL will populate the To Whse & Loc. fields of selected inventory with a suggested location.
When you perform a move in DMPR, AccellosOne 3PL refreshes the screen by requerying with the original search criteria such as warehouse code, location code, customer code, level 1 value, etc. If your 
original query included a hold code and if you have activated the automatic removal of hold codes in 
DMPA, AccellosOne 3PL will requery without the original hold code.
If you wish to assign all 
locations:
If you wish to assign selected 
locations:
a) Click on Select All. a) Click on the lines that you wish to 
select.

DIRECTED MOVE SYSTEM
Printing Labels for a Directed Move

DMPR screen showing to locations selected by system
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 
Printing Labels for a Directed Move
If a suggested location has been assigned to an inventory entity, you can print a label for the product in 
DMPR. The label will show the level 3 value, the to location, the level 1 value and the quantity.
When you print a label for a particular inventory entity, the “N” in the Label column of DMPR is changed to “Y”.
1 Enter DMPR
2 Key in your warehouse code and press Enter.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold 
code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Make sure that suggested locations have been assigned to the inventory entities whose labels you wish 
to print.
6 Click on (Print Label).

DIRECTED MOVE SYSTEM
Printing the Directed Move Report (DMVR)
ALLOCATION AND WAVE MANAGER 4.2 189
7 When the Printer Code Block appears, key in your printer code and press Enter.
8 Click on Execute Report.
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 
Printing the Directed Move Report (DMVR)
The Directed Move Report shows the customer code, up to four inventory levels, the from and to locations, 
and the move quantity. DMVR shows only inventory that has been assigned a suggested location in DMPR; 
inventory without a suggested location will not print. 
When you run a report for a particular inventory entity, the “N” in the Report column of DMPR is changed to 
“Y”.
DMVR is an audit report. An audit report is a report that generates a unique audit number the first time that it 
is run for a given inventory entity. The audit number is assigned to each inventory entity included in the report. 
Once an audit number is assigned to inventory, it is fixed. New inventory will be assigned the next audit 
number in the series while existing inventory will retain the audit number that was originally assigned when 
the report was first run.
The purpose of audit numbers is to group a series of transactions that occurred at the same time into a single 
batch for audit and control purposes; for example, all directed moves for a particular customer or all directed 
moves performed on a specific date. If you know the audit number for a batch, you can easily assign and 
deassign suggested locations for all inventory in the batch.
1 Enter DMPR
2 Key in your warehouse and press Enter.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold 
code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Make sure that suggested locations have been assigned to the inventory entities that you wish to report 
on.
6 Click on (Print Report).
7 When the Printer Code Block appears, key in your printer code and press Enter.
8 Click Ok.
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 

DIRECTED MOVE SYSTEM
Removing Suggested Locations for a Directed Move
Directed Move Report for audit 363
Removing Suggested Locations for a Directed Move
You can remove suggested locations for a directed move in DMPR at any time before the directed move is 
confirmed in RELO or RFRL. When you remove suggested locations for a directed move, you can rerun 
DMPR at a later time to generate new suggested locations.
1 Enter DMPR.
2 Enter your warehouse.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold 
code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Select the inventory whose suggested locations you wish to deassign.
6 Click on Move/Undo. AccellosOne 3PL will remove the to location from the selected inventory entities.
7 Click on (Return) to exit Directed Move Details. 
8 Click on (Exit) to exit. 
Confirming the Directed Move
You can confirm your directed move in either RELO (Relocate Inventory) or RFRL (RF Relocate). When you 
confirm a directed move, you have two choices: you can accept the location suggested by the system or you 
can select your own location.
 Directed Move Report - Suggested Locations
ABC Warehousing, Inc.(V6) 
19-Aug-05
Directed Move Report (DMVR)
Audit # 363 FROM SUGGESTED
Customer Level 1 Whse Location Whse Location Move Qty
 Level 2 Level 3 Level 4
-----------------------------------------------------------------------------
---
E E1 1 A101 1 B100 160
 106 JUNE 06 001
E E1 1 A101 1 B101 160
 101 JUNE 15 003
E E1 1 A101 1 B102 160

DIRECTED MOVE SYSTEM
Confirming the Directed Move
ALLOCATION AND WAVE MANAGER 4.2 191
If you ran the Directed Move Report in DMPR, the system-generated audit number assigned to the transactions will be used as the adjustment number for each inventory entity in the report. If you print labels rather 
than a report or do no printing, each move in RELO will be assigned a separate adjustment number.
CONFIRMING THE DIRECTED MOVE IN RELO
1 Enter RELO.
2 Enter any required search criteria.
3 Click on Move Mode.

RELO screen showing seven records that have been assigned directed move locations in DMPR
AccellosOne 3PL will automatically retrieve all records that were successfully assigned suggested locations in DMPR.
4 Use your arrow keys to select the inventory entity that you wish to confirm.
5 Click on Location Block.

DIRECTED MOVE SYSTEM
Confirming the Directed Move

RELO screen (Location Block) showing from location A101 with a negative quantity and to location 
A107 with a positive quantity
6 Do one of the following:
7 When the Remark Block appears, enter your remarks and press Enter or click on Return to Main to 
bypass remarks.
8 Click on Exit to exit.
If you accept the suggested 
location:
If you do NOT accept the 
suggested location:
a) Click on Relocate. a) Use your arrow keys to position 
your cursor over the suggested 
to location line.
b) Press Enter to position your cursor in the Adjust column of the 
suggested to location. Then click 
on Delete.
c) If the to location that you wish to 
put-away to is not displayed, 
click on Create Record. Then 
key in the location code and 
warehouse code (if required).
d) Key in the adjustment quantity 
and press Enter. The adjustment 
quantity should match the quantity in the Proof column.
e) Press Enter to bypass the Conveyance field.
f) Click on Relocate.

DIRECTED MOVE SYSTEM
Confirming the Directed Move
ALLOCATION AND WAVE MANAGER 4.2 193
CONFIRMING THE DIRECTED MOVE IN RFRL
If the Supervisor Authorization Required to Override Location flag in DMPA has been set to Y for Yes and you 
attempt to override the suggested location in RFRL, the supervisor authorization pop-up window will appear. 
A supervisor must then log on to authorize the change in location.
1 Enter RFRL.
2 Enter any required search criteria.
3 Press F1 (Move Mode).

RFRL screen showing three records that has been assigned a directed move location in DMPR
4 If the quantity is not correct, press F9 to position your cursor in the Qty field. Then key in a new quantity 
and press Enter. 
5 Do one of the following:
If you accept the suggested 
location:
If you do NOT accept the 
suggested location:
a) Press Enter to accept the location.
b) Press F3 (PR) to confirm the 
move.
a) Key in the new location and 
press Enter.

RFRL screen showing prompt 
for supervisor authorization
b) If prompted to do so, key in the 
supervisor login and press Enter. 
Then key in the supervisor password and press Enter again.
c) Press F3 (PR) to confirm the 
move.

DIRECTED MOVE SYSTEM
Looking Up Directed Moves in LOEN
6 Repeat the above steps for each additional move that you wish to confirm.
7 When you finish processing your moves, press F4 twice to exit.
Looking Up Directed Moves in LOEN
When you run DMPR to assign suggested locations to a directed move, the following records are created in 
the Location Block of LOEN: the from location will show a positive quantity in both the On-Hand and Replenishment columns while to the to location will show a positive quantity in the Available column and a negative 
quantity in the Replenishment column.

LOEN screen showing A101 and A103 as the from location and A107 as the to location
When you confirm the directed move in RELO or RFRL, AccellosOne 3PL will create two records in the 
History Block: an IF (Information Only) record and an RL (Relocation) record. The IF record will show the from 
location and the suggested to location, while the RL record will show the from location and the actual to 
location selected in RELO or RFRL.

DIRECTED MOVE SYSTEM
Pallet Restacking
ALLOCATION AND WAVE MANAGER 4.2 195

LOEN screen showing IF and RL records in History Block
Pallet Restacking
Directed Move processing supports automatic consolidation or re-stacking of partial pallets. For example, you 
have placed dividers in your pallets to improve the airflow during blast freezing and now wish to restack the 
pallet normally without dividers.
You define your pallet stacking rules in the Allow Merging Up To Level (RFMI) field in MRFP and you perform 
the actual restacking in RFMI (RF Merge Inventory). In DMPA, the following fields are required:
FIELD DESCRIPTIONS
Enable Automated Pallet 
Consolidation
If you enter Yes in this field, automated pallet consolidation will be activated.
Staging Warehouse Code Mandatory
The warehouse code where pallet restacking will take place.

DIRECTED MOVE SYSTEM
Pallet Restacking
In DMPR (Directed Move Processing), you can perform the following functions: 
 you can control the size of re-stacked pallets by entering values in the Maximum Height for Pallet, Linear Measure Code and Number of Layers on Pallet fields 
 you can override the staging location dynamically by changing default staging warehouse and location 
codes
 you can disable automated pallet re-stacking dynamically by turning off Enable Automated Pallet Consolidation
DMPR screen
Staging Location Code Mandatory
The staging location code where pallet restacking will take place.
FIELD DESCRIPTIONS

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
ALLOCATION AND WAVE MANAGER 4.2 197
Opportunistic Cross-Docking
Opportunistic cross-docking allows you to put-away a receipt into a cross-dock location located on your 
receiving/shipping dock rather than into a bulk, rack or pick line location. Once the receipt is confirmed, the 
inventory can be allocated to a pending order in the usual way. Opportunistic cross-docking is designed to 
save labor and time by allocating inbound product to an outbound dock location.
AccellosOne 3PL will only assign inbound product to a cross-dock location if the following conditions have 
been met:
 there is a pending order with the same level 1 value and the same hold code (if any)
 the pending order has no level 2 or higher values entered and the to ship date is less than or equal to 
the current system date
 the cross-dock location has sufficient capacity to hold the entire receipt line (you cannot split a receipt 
line and sent part of the line to the cross-dock location and the remainder of the line to a non-cross-dock 
location)
 there is no inventory in a non-cross-dock location for the product being received (if the product being 
received is on hold, there is no inventory in a non-cross-dock location with a matching hold code)
Opportunistic cross-docking must be activated in ILOP (Directed Move Inbound). There are nine opportunistic 
cross-dock options:
CODE DESCRIPTION
M7010 enable OCD, put-away qty cannot exceed 
pending order qty with same ship date
The put-away quantity is less than or equal to the sum of all pending 
orders for the same item with the same ship date.
M7011 enable OCD option 7010 when pending 
order qty > on hand
1) The put-away quantity is less than or equal to the sum of all pending 
orders for the same item with the same ship date. 
2) The pending order quantity is greater than the on-hand quantity in 
the cross-dock location.
M7020 enable OCD, put-away qty can exceed 
pending order qty with same ship date
The put-away quantity can be greater than the sum of all pending 
orders for the same item with the same ship date.
M7021 enable OCD option 7020 when pending 
order qty > on hand
1) The put-away quantity can be greater than the sum of all pending 
orders for the same item with the same ship date.
2) The pending order quantity is greater than the on hand quantity in the 
cross-dock location.
M7030 enable OCD, distribute to orders with shipping lane, ignoring FIFO/LIFODistribute inbound product across multiple orders without running allocation. The priority of distribution will be based on order priority and 
ship to date. 
M7040 enable OCD, put-away qty cannot exceed 
pending order qty, ship in given hour
The put-away quantity is less than or equal to the sum of all pending 
orders for the same item with the same ship date that ship within the 
number of hours specified in the Hours field.

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
“SHIP IN GIVEN HOUR” OPTION
If you select either M7040 or M7042, you must specify the number of hours before the pending order's ship 
date/time that is acceptable for opportunistic cross docking. For example, the product is freezer product that 
cannot be left on the dock for more than a given number of hours. If, say, you specify a value of 6 hours and 
product is received at 12 noon, it cannot be assigned to a pending order with a ship date/time later than 6 pm 
on the same day.
ILOP screen showing Hours = 6 for M7040
M7041 enable OCD option 7040 when Pending 
Order Qty > On Hand
1) The put-away quantity is less than or equal to the sum of all pending 
orders for the same item with the same ship date that ship within the 
number of hours specified in the Hours field. 
2) The pending order quantity is greater than the on hand quantity in the 
cross-dock location.
M7042 enable OCD, put-away qty can exceed 
pending order qty, ship in given hour
The put-away quantity can exceed the sum of all pending orders for the 
same item with the same ship date that ship within the number of hours 
specified in the Hours field.
M7043 enable OCD option 7042 when Pending 
Order Qty > On Hand
1) The put-away quantity can exceed the sum of all pending orders for 
the same item with the same ship date that ship within the number of 
hours specified in the Hours field.
2) The pending order quantity is greater than the on hand quantity in the 
cross-dock location.
CODE DESCRIPTION

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
ALLOCATION AND WAVE MANAGER 4.2 199

ILOP screen showing opportunistic cross-dock options
SETTING UP OPPORTUNISTIC CROSS-DOCKING (M7010-21, M7040-43)
1 If you are only cross-docking certain product, create a new ILOP profile with cross-docking enabled. If 
you are cross-docking all your product, you can modify an existing profile instead of creating a new one.
2 Your cross-docking profile must contain only one put-away sequence in which cross-docking is enabled. 
The cross-dock sequence must be the first sequence in your profile.
3 For the put-away sequence in which cross-docking is enabled, you must define a cross-dock warehouse 
and location in the Sequence Block of ILOP. The location type set up in LOTP for the cross-dock location 
must have the Directed Put-Away and Directed Picking flags set to Y for Yes and the Staging flag set to N 
for No.
4 Create at least one non-cross-dock sequence after your first cross-dock sequence. In this non-crossdock sequence, you define a “next best” location should your cross-dock sequence fail.
5 If you are creating a new ILOP profile, attach the new profile to the items that you wish to cross dock.
6 Make sure that directed put-away is activated.
NOTE When you use any of “enable” options, they disable and override all other 
options in the sequence. For example, if you set up sequence 1 in ILOP with “use 
only exact match isolator code” and “enable OCD, put-away qty cannot exceed pending order qty with same ship date”, your exact match requirement for isolators codes 
will be ignored.

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
SETTING UP OPPORTUNISTIC CROSS-DOCKING (M7030)
1 If you are only cross-docking certain product, create a new ILOP profile with cross-docking enabled. If 
you are cross-docking all your product, you can modify an existing profile instead of creating a new one.
2 Your cross-docking profile must contain only one directed move sequence in which cross-docking is 
enabled. The cross-dock sequence must be the first sequence in your profile.
ILOP screen showing option M7030
3 For the directed moved sequence in which cross-docking is enabled, you must define a cross-dock warehouse and location in the Sequence Block of ILOP. The location type set up in LOTP for the cross-dock 
location must have the Directed Put-Away and Directed Picking flags set to Y for Yes and the Staging flag 
set to N for No.
4 Create at least one non-cross-dock sequence after your first cross-dock sequence. In this non-crossdock sequence, you define a “next best” location should your cross-dock sequence fail.
5 If you are creating a new ILOP profile, attach the new profile to the items that you wish to cross dock.
6 Make sure that directed put-away is activated.
7 Create one or more shipping lanes in SHLA.

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
ALLOCATION AND WAVE MANAGER 4.2 201
SHLA screen
Shipping lanes must be attached to a staging location in SHLA.
8 Assign your cross-dock consignees to shipping lanes in SLAS. A consignee can be assigned to only one 
shipping lane, but the same shipping lane can contain multiple consignees.
SLAS screen
ATTACHING A SHIPPING LANE TO AN ORDER IN ENOR
If you attach a shipping lane to an order in ENOR, it will override your shipping lane assignments in SLAS.
1 Enter ENOR.
2 Enter your order header information (customer, consignee, sold-to, etc.) in the normal manner.

DIRECTED MOVE SYSTEM
Opportunistic Cross-Docking
ENOR screen showing prompt for shipping lane code
3 When you reach the Shipping Lane Code field, key in your shipping lane code and press Enter or use the 
picklist to select it.
4 Continue processing your order normally in ENOR.

ALLOCATION AND WAVE MANAGER 4.2 203
WAVE MANAGER
Overview .......................................................................................................... 205
Waves vs. Templates................................................................................. 206
Setting Up Label Printing ............................................................................... 207
Setting Up Your Wave Deallocation Rule in CUST....................................... 209
Launching Wave Manager.............................................................................. 210
Working With Pick Lists and the Column Manager ..................................... 212
Selecting Multiple Values in a Filter Pick List............................................. 212
Working With the Column Manager ........................................................... 214
Creating a New Template ............................................................................... 215
Setting Your Wave Preferences................................................................. 221
Modifying a Template................................................................................. 222
Updating a Template.................................................................................. 222
Deleting a Template................................................................................... 223
Looking Up the Generated SQL for a Query.............................................. 223
Creating a Custom SQL Filter.................................................................... 224
Running a Wave .............................................................................................. 224
Running a Wave From an Unsaved Template........................................... 225
Searching for a Wave ................................................................................ 226
Looking Up Orders on a Wave................................................................... 226
Deleting Orders From a Wave ................................................................... 227
Deallocating Orders by Wave in DOWA .................................................... 227
Time-Stamping and Confirming a Wave in CHOF ..................................... 228
Deleting a Wave......................................................................................... 229
Looking Up a Wave’s Completion Status................................................... 229
Looking Up a Wave’s Job History .............................................................. 229
Looking Up Your Print Job Details ............................................................. 230
Generating a Wave Summary Report........................................................ 231
Generating a Wave Details Report ............................................................ 232
Reprinting Wave Labels............................................................................. 233
Looking Up an Order’s Wave Number in LOOR ........................................ 233

WAVE MANAGER
Scheduling a Template ................................................................................... 235
Searching for a Scheduled Template......................................................... 236
Searching for a Scheduled Job.................................................................. 237
Performing a Shortcut Search.................................................................... 238
Editing a Scheduled Template ................................................................... 239
Deleting a Scheduled Template................................................................. 239
Looking Up a Scheduled Template’s Job History ...................................... 240
Paper-Based Tracking .................................................................................... 240

WAVE MANAGER
Overview
ALLOCATION AND WAVE MANAGER 4.2 205
Overview
Wave Manager is a batch processing tool for orders that allows you to group orders by various criteria such 
as company code, allocated or unallocated status, flow process, customer, consignee, carrier, warehouse, 
load type, door, etc. and assign them to waves. You can define a date range for a wave using the ship date or 
arrive date and you can define a maximum size for a wave by the number of pieces, net or gross weight, cube 
or estimated number of hours of labor required.
When you process a wave using the Run Wave command, AccellosOne 3PL will allocate any unallocated 
orders in the wave and print the required number of carrier labels. The type and number of carrier labels 
printed is based on the order’s pick method. You configure your pick methods in CCDU (Customer / 
Consignee Document Setup).
Wave Manager supports label picking. With label picking, the AccellosOne 3PL-generated divider label shows 
the product’s location and number of cartons to pick, while the AccellosOne 3PL-generated carton label 
shows the consignee and carrier. The picker uses the divider label to pick the product. When applying the 
carton label to the picked product, only the first and last label is scanned. Label picking leads to improved 
speed and accuracy in picking and less sorting of product on the loading dock.
Divider label showing pick location and number of cartons to pick

WAVE MANAGER
Overview
You can save your wave parameters in one or more templates and schedule these templates to run automatically at a given time; for example, every 15 minutes, every day at 4:00 pm, every 30 minutes on Wednesday, 
etc.
WAVES VS. TEMPLATES
A wave is a batch of orders whose selection is based on various selection criteria such as company code, 
customer code, allocation status, flow process, etc. A template is a reusable container holding the filters used 
to create waves containing only the orders that meet the criteria that you define.
NOTE A given template will retrieve a specific order only once. If you rerun the 
same template twice in the same day, only new orders meeting the template’s selection criteria will be retrieved; orders already retrieved the first time that the template 
was run will NOT be retrieved a second time.
Create Wave
You select your template and click on Run 
Wave From Template.
You select your wave parameters and click 
on Query. After Wave Manager retrieves 
your query results, you can run the wave 
“on demand” or save your template with a 
description and printer code.
If required, you print the Wave Summary 
Report.
If your orders allocated correctly, you pick 
RFPK them in RFPK.
Template 
Management
Run Wave 
From 
Template
If required, you select your printer code and 
disable label printing.
Wave 
Summary 
Report

WAVE MANAGER
Setting Up Label Printing
ALLOCATION AND WAVE MANAGER 4.2 207
Setting Up Label Printing
Labels printed from Wave Manager must be set up in BarTender Enterprise. They are not attached to flows in 
DIFP and are not governed by the reprint restrictions in DOCU.
The type and number of labels printed is based on the order’s pick method. There are nine possible pick 
methods supported in Wave Manager. The following pick methods do NOT support label picking:
The following pick methods DO support label picking and the generation of a label pick label: 
BATP requires setup in the Carrier Type Code field of CARR.
Pick Method Description
PALL A full pallet pick. The order quantity of each order line must 
equal a single pallet.
EACH A Pick & Pack by each (the smallest SKU in an item’s quantity 
breakdown).
blank A normal case pick in RFPIC/RFPK.
Pick Method Description
BATP A batch pick across multiple orders when two or more orders in 
the wave are being picked up by the same carrier and the carrier type = UPS, DHL or FEDEX.
For example, if order line 1 picks 10 cases from a given location and order line 2 picks 5 cases of the same product from 
the same location, Wave Manager will generate a consolidated 
pick of 15 cases from the location.
LABP An individual order pick when a single order is being picked up 
by a given carrier.
RFMG A merge of two or more OPID’s in RFMG.
PKST Manual packing performed in EPSD (Enter Packing Details).
PACK First level cartonization performed in RFSC (RF Sort to Carton) 
or RFPK (RF Wave Pick).
CART A Pick & Pack by each used in system-driven cartonization.

WAVE MANAGER
Setting Up Label Printing
CARR screen showing carrier type code set to UPS
In CCDU (Customer/Consignee Document Setup), you specify which label and pick method applies to which 
customers/carriers/consignees. 
CCDU screen showing pallet label and pick method for customer A and consignee CONS
See the RF Guide for further information on CCDU (Customer/Consignee Document Setup).

WAVE MANAGER
Setting Up Your Wave Deallocation Rule in CUST
ALLOCATION AND WAVE MANAGER 4.2 209
Setting Up Your Wave Deallocation Rule in CUST
In CUST you specify what the Wave Manager should do if an order cannot be fully allocated. There are two 
options to choose from:
 Deallocate All Orders and Delete Wave 
 Deallocate Pending Orders from Wave and Keep Wave
CUST screen showing Wave Deallocation Rule field
FIELD DESCRIPTIONS
Wave Deallocation Rule Deallocate All Orders and Delete Wave
Deallocate Pending Orders From Wave and Keep Wave
In this field, you define your wave de-allocation rules when using the Wave 
Manager. If you leave this field blank, unallocated order lines will remain as Ptype lines and no deallocation will occur.

WAVE MANAGER
Launching Wave Manager
Launching Wave Manager
You launch Wave Manager from the ActiveDesktop. There are four main options in Wave Manager:
1 From ActiveDesktop click on Wave Manager.
Wave Manager screen
2 Click on Template Management to view your existing wave templates. Only templates created by yourself will display.
Create Wave Template Click on this option to create a new wave template. Any wave template that you create can only be viewed, edited and run by yourself. Wave templates are not shared; that means you do not have 
access to templates created by other AccellosOne 3PL operators 
and they do not have access to your templates.
Template Management Click on this option to manage your waves. You can update waves, 
run waves and schedule waves from this option. Only waves created by yourself will be accessible in Template Management.
Wave Management Click on this option to view and manage your waves. You can 
delete waves, view orders on a wave, reprint wave labels and generate wave reports. 
NOTE Wave Management shows all active waves in Wave 
Manager regardless of the operator who created them. You can 
delete waves and perform other wave operations on waves belonging to other operators.
Schedule Management Click on this option to view and manage your scheduled templates. 
You can search for scheduled templates and scheduled jobs, edit a 
scheduled template and look up the job status of a scheduled job. 

WAVE MANAGER
Launching Wave Manager
ALLOCATION AND WAVE MANAGER 4.2 211
Template Management screen showing templates
3 If required, click on the appropriate filter. The Show All Templates filter shows templates only but no wave 
information, while the Show Templates That Have Waves filter shows only templates that have been 
used to generate a wave. If the same template has been used to generate multiple waves, a separate 
record is shown for each wave.
4 Click on Wave Management to manage your waves. Wave Management shows all waves created by all 
AccellosOne 3PL operators; you are not restricted to waves created by yourself.
Wave Manager screen showing Wave Search parameters
5 Enter or select your wave search parameters and click on Search.

WAVE MANAGER
Working With Pick Lists and the Column Manager
Wave Results screen showing eight waves
6 Click on Exit to exit Wave Manager.
Working With Pick Lists and the Column Manager
Wave Manager’s advanced navigation capabilities allow you to select multiple values from a pick list and turn 
on and off any column in your query results.
SELECTING MULTIPLE VALUES IN A FILTER PICK LIST
In this example, you select multiple orders from the order filter in Create Wave Template.
1 Click on the appropriate primary filter to display the various values that you can select for that filter.
Order Filter screen
2 Click on the field that you wish to select multiple values from.

WAVE MANAGER
Working With Pick Lists and the Column Manager
ALLOCATION AND WAVE MANAGER 4.2 213
Order Filter showing unselected order numbers
3 Select the individual records that you wish to add to your filter.
Order Filter showing three selected records
4 When you finish selecting your records, click on Add on the right side of your screen.
Order Filter showing selected records added to Order Number field
5 If your selection is correct, click on Add to add the records to the primary order filter. If your selection in 
incorrect, click on Clear and reselect your records.

WAVE MANAGER
Working With Pick Lists and the Column Manager
Primary Wave Filters screen showing Order Filters field populated
6 To verify your selection, you can mouse over a populated field to see all selected records.
Primary Wave Filters screen showing pop-up window
WORKING WITH THE COLUMN MANAGER
Column Manager allows you to select which columns you wish to see in your query results in Create 
Template, Template Management and Wave Management. Your Column Manager settings apply to the 
current session only; they are not saved when you exit Wave Manager.
1 Click on Cols to display the Column Manager.

WAVE MANAGER
Creating a New Template
ALLOCATION AND WAVE MANAGER 4.2 215
Column Manager
2 Proceed to select or deselect the columns that you wish to display. If you make a mistake, you can click 
on the Check/Uncheck All Columns to undo your changes.
3 When you finish selecting your columns, do one of the following:
Creating a New Template
There are two types in templates in Wave Manager: saved and unsaved. Saved templates are regular 
templates used on a daily basis in a production environment, while unsaved templates are intended for 
testing purposes only.
Both types of templates can be used to run waves and print labels, and both types of templates are stored in 
Template Management with the exception of unsaved templates that are created but not run. Unsaved 
templates that are not run are automatically deleted when you exit Create Template.
The only difference between a saved and unsaved but run template is the template’s description in Template 
Management. For an unsaved template, the system-created description will read “TEMPORARY - RUN 
If you wish to save your 
changes:
If you wish to exit without saving 
your changes:
a) Click on Refresh. Your updated 
columns will display after a few 
seconds.
a) Click on Close.

WAVE MANAGER
Creating a New Template
MODE ONLY TEMPLATE”. You can change an unsaved template into a saved template with a meaningful 
description by means of the Update Template command.
FIELD DESCRIPTIONS
Company Code Mandatory
The company code for the template. The value that you enter in this field 
determines many of the values in other filters such as Order Filters, Customer 
Filters and Consignee Filters.
Allocation Status All
Allocated
Unallocated
If you select All, all orders regardless of allocation status will be included in the 
wave. If you select Allocated, only allocated orders will be included in the 
wave. If you select Unallocated, only unallocated orders will be included in the 
wave.
Assigned to Load No
Yes
If you select No, only orders NOT attached to a load in SELO will be included 
in the wave. If you select Yes, only orders attached to a load in SELO will be 
included in the wave.
Advance Workflow No Advance Flow
Before Allocation
After Allocation
If you select No Advance Flow, the flow of orders in the wave will not be 
advanced when you run the wave. If you select Before Allocation, the flow of 
orders in the wave will be advanced before allocation occurs. If you select 
After Allocation, the flow of orders in the wave will be advanced after allocation.

WAVE MANAGER
Creating a New Template
ALLOCATION AND WAVE MANAGER 4.2 217
Suspend Task Not Applicable
Yes
If you select Yes, picking tasks will be automatically suspended when you 
generate a wave in Wave Manager. This will allow you to manually adjust your 
pallet build assignments in PABU (Pallet Build) before they are released to RF 
or voice for picking.
If you select Not Applicable, picking tasks will be automatically released to RF 
or voice for picking once the wave is generated.
NOTE The suspension of picking tasks must be activated in COMP before 
you can use the Yes option in a template.
De-Allocate Rule Not Applicable
Unalloc. Orders
All Orders
In this field, you specify what the Wave Manager should do if an order cannot 
be fully allocated. If you select Unalloc. Orders, Wave Manager will deallocate 
pending orders from the wave and keep the wave. If you select All Orders, 
Wave Manager will deallocate all orders and delete the wave.
If you select Not Applicable, the option that you select in the Wave Deallocation Rule field in CUST will be used.
Banding Reserved for future use.
Flow Process Filters If you specify one or more flows, only orders at those flows will be included in 
the wave. 
Order Filters If you specify one or more orders, only those orders will be included in the 
wave. 
NOTE Filtering by specific orders is for testing purposes only. It is NOT 
recommended for saved templates as the template can only be used once 
before you must manually change the order restrictions.
Customer Filters If you specify one or more customers, only orders belonging to those customers will be included in the wave. 
FIELD DESCRIPTIONS

WAVE MANAGER
Creating a New Template
1 Click on Create Template.
Consignee Filters If you specify one or more consignees, only orders being shipped to those 
consignees will be included in the wave. 
You can specify consignees by consignee code, consignee name, consignee 
city, consignee state/province, consignee ZIP/postal code, consignee country 
code, consignee priority, freight destination code, load analysis code, consignee type (RETP) and special consignee status. 
Carrier Filters If you specify one or more carriers, only orders assigned to those carriers will 
be included in the wave. You can specify carriers by carrier code, standard 
alpha code, carrier type code and transport mode code.
Warehouse Filters If you specify one or more warehouses, only orders being picked from those 
warehouse will be included in the wave. You can specify warehouses by warehouse code and location type code. 
Freight Filters If you specify an AccellosOne 3PL load number, an external load number or a 
stop number, only orders assigned to the AccellosOne 3PL load number, 
external load number or stop number will be included in the wave.
Load Type Filters If you specify one or more load types, only orders assigned to those load 
types will be included in the wave.
Door Filters If you use APPL (Appointment Planner) to assign orders to buildings and 
doors, you can restrict your wave to orders assigned a particular building and 
door(s).
Item Filters If you specify one or more items, only order lines containing those items will 
be included in the wave. You can specify items by item code, hold code, alternate reporting type code, alternate reporting code and hazmat flag.
There are three possible values in the Hazmat Flag field: All, Inclusive or 
Exclusive. If you select All, all items regardless of hazmat status will be 
included in the wave. If you select Inclusive, any order containing at least one 
line with a hazmat item will be included in the wave. If you select Exclusive, 
only orders with NO hazmat items on any line will be included in the wave.
FIELD DESCRIPTIONS

WAVE MANAGER
Creating a New Template
ALLOCATION AND WAVE MANAGER 4.2 219
Create Template screen
2 Proceed to enter or select the appropriate values in the various Create Template filters. If you do not 
know how to select multiple values in a filter, see “Selecting Multiple Values in a Filter Pick List” on page 
212.
3 Click on Date Filters to view your date restrictions. If you do not want to enter date restrictions, click on 
Clear Date Filters.
Date Filters
4 If you wish to enter capacity parameters, click on Capacity Parameters.
NOTE Date restrictions are NOT recommended for saved templates.

WAVE MANAGER
Creating a New Template
Capacity Parameters
5 Key in any required capacity parameters.
6 Select the appropriate sort order (order number, ship to date or carrier) for your query results.
7 When you finish entering your wave parameters, click on Query.
Wave Results screen showing wave results
8 If you wish to exclude individual orders from the wave, click on the Select checkbox of the first order to be 
excluded. Then click on any part of the row except the checkbox of any additional orders that you wish to 
exclude from the wave.
If you make a mistake and wish to include any previously excluded orders, click on the Select checkbox 
in the header row to select all rows in the wave results.
9 If you excluded one or more individual orders from the wave in the previous step, click on Use Selected 
Rows to refresh your screen and show only the selected orders.
10 Do one of the following:
If you are creating a saved 
template:
If you are NOT creating a saved 
template:
a) Click on Save Template. End of Procedure.

WAVE MANAGER
Creating a New Template
ALLOCATION AND WAVE MANAGER 4.2 221
Save Template screen
11 Key in a meaningful description for your new template.
12 Select your label printer code from the pick list.
13 Click on Save Template.
SETTING YOUR WAVE PREFERENCES
Wave preferences allow you to set the unit of measure, number of orders per page and the default value in 
the “Disable Label Printing for this run” checkbox in Run Wave From Template. Wave preferences apply to 
waves run in the current session only; once you exit Wave Manager, wave preferences are reset to the 
default values.
If you want to apply your own wave preferences to a given template, you must reset your wave preferences 
on the Preference screen and then use the Update Template command to save your wave preferences for 
that template.
FIELD DESCRIPTIONS
System of Measure Metric
Imperial
The unit of measure used in the wave results for gross weight, net weight and 
cube.
Orders Per Page 100
500
1000
The number of orders per page in the wave results.

WAVE MANAGER
Creating a New Template
1 Click on Query Preferences.
Wave Manager showing Query Preferences window
2 Make any required changes to your preferences.
3 Click on Query Preferences to close the Query Preferences window and save your changes.
MODIFYING A TEMPLATE
The Modify Template command allows you to modify the template’s company code, allocation status, 
assigned to load flag as well as the various flow process, order and other filters.
1 Click on Template Management.
2 Select the template that you wish to modify.
3 Click on Modify Template.
4 Make any required changes to the Primary Wave and Date Filters as well as to the Capacity Parameters.
5 When you finish making your changes, click on Query.
6 Click on Update Template to save your changes.
UPDATING A TEMPLATE
The Update Template command allows you to update the template description and label printer code. The 
Warehouse Code, Location Code and Printer Code fields are reserved for future use.
If you have reset your wave preferences in the current session, the Update Template command will attach 
those preferences to the template.
Run Wave Label Printing ON
OFF
If you select ON, the Disable Label Printing for this run checkbox in Run Wave 
From Template will NOT be selected. If you select OFF, the Disable Label 
Printing for this run checkbox will be selected.
Exclusion Rules Use ALL Exclusion Filters
Use Excluded Orders Only
Use Included Orders Only
No Exclusion
In this field, you define your exclusion rules. You can use all your exclusion filters (default value), only your excluded order filters, only your included order 
filters or no exclusions. If you select no exclusions, any exclusions in your 
template will be ignored.
FIELD DESCRIPTIONS

WAVE MANAGER
Creating a New Template
ALLOCATION AND WAVE MANAGER 4.2 223
1 Click on Template Management.
2 Select the template that you wish to modify.
3 Click on Update Template.
Update Wave Template
4 Proceed to make your changes to the wave template.
5 When you finish making your changes, click on Update Template to save your changes.
DELETING A TEMPLATE
1 Click on Template Management.
2 Select the template that you wish to delete.
3 Click on Delete in the Action column.
4
LOOKING UP THE GENERATED SQL FOR A QUERY
The SQL Inspector allows you to look up the generated SQL for queries in Create Template. It is used for 
debugging purposes when the actual results set does not match the expected results set.
1 Click on Create Template.
2 Proceed to enter or select the appropriate values in the various Create Template filters.
3 When you finish entering your wave parameters, click on Query.
4 Click on SQL.
SQL Inspector screen showing generated SQL for a Create Web Template query

WAVE MANAGER
Running a Wave
5 When you finish looking up your generated SQL, click on SQL again to close the SQL Inspector.
6
CREATING A CUSTOM SQL FILTER
You can create custom SQL filters to complement your primary wave filters.
1 Click on Create Template.
2 Click on Custom SQL Filter.
3 Click on Edit/View Custom SQL Filter.
Custom SQL Filter
4 Enter your SQL commands in the box at the bottom of your screen.
5 When you finish entering your SQL parameters, click on Apply Custom SQL Changes.
6 Click on Test Parameters and SQL to test your new filter.
7 If your test is successful, click on Cancel to exit. If your test is unsuccessful, correct your filter and click 
on Test/Validate SQL.
Running a Wave
When you process a wave using the Run Wave command, AccellosOne 3PL will allocate any unallocated 
orders in the wave and print the required number of carrier labels. 

WAVE MANAGER
Running a Wave
ALLOCATION AND WAVE MANAGER 4.2 225
1 Click on Template Management.
2 Select the template that you wish to run and click on Run Wave From Template.
Run Wave From Template screen
3 If the Label Printer Code field is not populated, select your printer code from the pick list.
4 If required, you can click on the Disable Label Printing for this run checkbox to select or deselect it.
5 Click on Run Wave From Template.
Wave Manager will display the Wave Manager Information screen showing the job number.
Wave Manager Information screen showing job number
RUNNING A WAVE FROM AN UNSAVED TEMPLATE
You can run a wave from an unsaved template in Create Template.
1 Click on Create Template.
2 Enter your wave parameters in the normal manner.
3 If required, clear your date filters. If you do not clear your date filters, the default ship date will be set to 
today’s date.
4 Click on Query.
5 When the wave results screen displays, click on Run Wave.
Run Wave screen
6 If the Label Printer Code field is not populated, select your printer code from the pick list.

WAVE MANAGER
Running a Wave
7 If required, you can click on the Disable Label Printing for this run checkbox to select or deselect it.
8 Click on Run Wave.
SEARCHING FOR A WAVE
You can search for a wave by company code, wave status, label print status, order number, wave create date 
and wave ID. If you enter a comma between each value in Wave ID field, you can search for multiple wave 
ID’s.
1 Click on Wave Management.
Wave Search
2 Enter or select your wave search parameters and click on Search.
Wave Results screen
LOOKING UP ORDERS ON A WAVE
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.

WAVE MANAGER
Running a Wave
ALLOCATION AND WAVE MANAGER 4.2 227
3 Select the wave whose orders you wish to look up and click on View Wave Orders.
Wave Orders screen
4 Click on Close to return to the Waves screen.
DELETING ORDERS FROM A WAVE
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave containing the order(s) that you wish to delete and click on View Wave Orders.
Wave Orders screen
4 Select the order(s) that you wish to delete and click on Delete in the Action column.
5 Click on Close to return to the Waves screen.
DEALLOCATING ORDERS BY WAVE IN DOWA
You can deallocate all orders in a wave or selected orders in a wave in DOWA (Deallocate Orders by Wave).
1 Enter DOWA.
2 Key in your wave number and press Enter.
DOWA screen

WAVE MANAGER
Running a Wave
3 Do one of the following:
The screen will clear.
4 Click on Exit.
TIME-STAMPING AND CONFIRMING A WAVE IN CHOF
You time-stamp and confirm waves in CHOF (Time Stamp and Confirm Orders) in the same way that you 
time-stamp and confirm individual orders. Advancing the flow of a wave will advance the flow of all orders on 
the wave.
1 Enter CHOF.
2 Press Enter until your cursor is positioned in the Batch Order Number / Wave Number field.
3 Key in your wave number and press Enter.
CHOF screen showing wave with next flow process code of STLO (Start Loading)
4 Proceed to advance the wave’s flow in the normal manner.
To deallocate all orders in the 
wave:
To deallocate selected orders in 
the wave:
a) Click on Deallocate All. a) Select the orders that you wish to 
deallocate.
b) Click on Deallocate 
Selected.

WAVE MANAGER
Running a Wave
ALLOCATION AND WAVE MANAGER 4.2 229
DELETING A WAVE
Waves that run successfully should be deleted on a regular basis to maintain system performance and to 
avoid running out of disk storage space.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave that you wish to delete and click on Delete Wave.
LOOKING UP A WAVE’S COMPLETION STATUS
You can look up a wave’s completion status by clicking on Status in the Action column. When you click on 
Status, Wave Manager displays Operational Board information showing completed vs. remaining quantities 
and percentages for the wave.
An order is considered completed when the entire order is confirmed in CHOF or the order line is confirmed in 
COOL.
If you have set up labor standards in AccellosOne 3PL, Wave Manager shows the estimated number of hours 
and minutes that it took to perform the completed work as well as the estimated number of hours and minutes 
to finish the remaining work.
See the Operational Board documentation in the Operations 2 Guide for further information on tracking 
completed vs. remaining work.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave whose status you wish to look up and click on Status in the Action column.
Order Summary screen showing partially complete wave
4 When you finish looking up the wave’s completion status, click on Close.
LOOKING UP A WAVE’S JOB HISTORY
To monitor your run jobs, you can use the Run Jobs tab to see the wave ID generated by the job as well as 
the job’s status (Success, No Wave, etc.). If the job failed and no wave was generated, you can look up the 
probable cause by clicking on Job Details.
1 Click on Run Jobs.

WAVE MANAGER
Running a Wave
Wave Manager Job History window showing wave ID generated by the job, job status and job details
2 If required, click on the wave ID to see the wave details.
LOOKING UP YOUR PRINT JOB DETAILS
The Print Jobs tab shows the status of your print jobs and printers. You use this command when your wave 
was successfully generated, but no labels printed.
1 Click on Print Jobs.

WAVE MANAGER
Running a Wave
ALLOCATION AND WAVE MANAGER 4.2 231
Print Job History screen
GENERATING A WAVE SUMMARY REPORT
The Wave Summary Report is generated automatically whenever a wave is run. It shows the total units, gross 
weight, net weight, cube, pending or unallocated quantity, header flow, maximum line flow (which may be later 
than the header flow) and the to ship date for each order on the wave.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave that you wish to report on and click on Generate Wave Report.

WAVE MANAGER
Running a Wave
Wave Summary Report
4 If you wish to print the report, right click anywhere on the report and select Print. When the Print window 
appears, select your printer and click on Print.
5 Select File > Exit to close the report window.
GENERATING A WAVE DETAILS REPORT
This report can only be run once immediately after running your wave. It is for support purposes if orders do 
not allocate and is not available after you exit the Wave Manager Information window.
Wave Details Report

WAVE MANAGER
Running a Wave
ALLOCATION AND WAVE MANAGER 4.2 233
REPRINTING WAVE LABELS
When you reprint wave labels, you can reprint all wave labels or exception labels only. Exception labels are 
labels that failed to print in BarTender.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave whose labels you wish to reprint and click on Reprint Wave Labels.
Reprint Wave Labels screen
4 Select the appropriate label type from the dropdown list (all labels or exception labels only).
5 If required, select a new label printer code.
6 Click on Reprint Wave Labels.
LOOKING UP AN ORDER’S WAVE NUMBER IN LOOR
The order header in LOOR (Look Up Orders) shows the order’s wave number, while the order line shows the 
picking method for that order line.

WAVE MANAGER
Running a Wave
LOOR screen showing wave number
Line Block of LOOR showing picking method for order line 1

WAVE MANAGER
Scheduling a Template
ALLOCATION AND WAVE MANAGER 4.2 235
Scheduling a Template
You can schedule a template to run automatically at a given time; for example, the 15th minute of each hour, 
every day at 4:00 pm, the 30th minute of each hour on Wednesday, etc. You must specify a start date for a 
scheduled template. The end date field for a scheduled template is optional. 
You set up scheduling by selecting the appropriate values in the Minutes, Hour, Day, Month and Day of Week 
dropdown lists. The following chart shows some of various scheduling scenarios available in Wave Manager.
Wave scheduling must be activated by HighJump.
1 Click on Template Management.
2 Select the template that you wish to schedule and click on Schedule Wave From Template.
Wave Template Scheduler
3 Click on Start Date to select your start date from the pop-up calendar.
Frequency Minutes Hour Day Month
Day of 
Week
the 20th minute of each hour 20 " " " "
the 45th minute of each hour 
on Wednesdays
45 " " " Wednesday
9 am every day " 9 am " " "
9 am every Monday " 9 am " " Monday
9 am first of the month " 9 am 1 " "

WAVE MANAGER
Scheduling a Template
4 If required, click on End Date to select your end date from the pop-up calendar.
5 Select your the appropriate values from the Minutes, Hour, Day, Month and Day of Week dropdown lists. 
6 When you finish setting up your schedule, click on Save.
SEARCHING FOR A SCHEDULED TEMPLATE
A scheduled template search allows you to search for all scheduled templates, active scheduled templates or 
inactive scheduled templates. Scheduled template searches retrieve all templates whether or not they have 
ever run; for example, a scheduled template with a start date in the future that has not run yet.
1 Click on Schedule Management.
Schedule Management screen
2 Select your schedule type from the dropdown list: All Scheduled Templates, Active Scheduled Templates 
or Inactive Scheduled Templates.
3 If required, enter a start date, end date or template ID.
4 Click on Search Scheduled Templates.
Search Results for Scheduled Templates pane
5 Click on the scheduled template that you wish to look up.

WAVE MANAGER
Scheduling a Template
ALLOCATION AND WAVE MANAGER 4.2 237
Wave Manager will display the scheduled start date, schedule end date (if any) and template ID in the 
fields of the same name.
SEARCHING FOR A SCHEDULED JOB
A scheduled job search allows you to search for jobs based on scheduled templates that have already run. 
You can search for all jobs, successful jobs, failed jobs or unprocessed or new jobs. An unprocessed or new 
job is a failed job that did not run to completion for any reason.
After performing your scheduled job query, you can click on any scheduled template in your query results and 
look up detailed processing information for each job run as part of the scheduled template.
1 Click on Schedule Management.
Schedule Management screen
2 Select your job status from the dropdown list: All Jobs, Successful Jobs, Failed Jobs or Unprocessed or 
New Jobs.
3 If required, enter the date that the job was processed.
4 Click on Search Scheduled Jobs.
Search Results for Scheduled Jobs pane showing the date processed, status and template ID
5 Click on the scheduled job that you wish to look up.

WAVE MANAGER
Scheduling a Template
Wave Manager will display the scheduled start date, schedule end date (if any), template ID and date 
processed in the fields of the same name.
6 Click on View Scheduled Jobs. This command will show all jobs run for the currently selected scheduled 
template plus detailed processing information for each job.
History of Wave Batch Jobs showing each job run for the selected scheduled template (203754)
7 When you finish looking up your scheduled jobs for the currently selected template, click on Close.
PERFORMING A SHORTCUT SEARCH
Shortcut searches allow you to search for Today’s Jobs (jobs run today whether successful or not), Today’s 
Successful Jobs and Show All Successful Jobs (all successful jobs regardless of date).
1 Click on Schedule Management.
Schedule Management screen showing shortcuts
2 Click on the appropriate shortcut: Today’s Jobs, Today’s Successful Jobs or All Successful Jobs.

WAVE MANAGER
Scheduling a Template
ALLOCATION AND WAVE MANAGER 4.2 239
Search Results for Scheduled Jobs pane showing the date processed, status and template ID
3 Click on the scheduled job that you wish to look up.
Wave Manager will display the scheduled start date, schedule end date (if any), template ID and date 
processed in the fields of the same name.
EDITING A SCHEDULED TEMPLATE
1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Templates.
3 In the Search Results for Scheduled Templates pane, click on the template that you wish to edit.
4 Click on Edit Schedule.
Wave Template Scheduler screen
5 Click on Edit Schedule.
6 Proceed to make your changes to the schedule.
7 Click on Save to save your changes.
DELETING A SCHEDULED TEMPLATE
You can delete a template’s schedule at any time.
1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Templates.
3 In the Search Results for Scheduled Templates pane, click on the template that you wish to delete.
4 Click on Edit Schedule.

WAVE MANAGER
Paper-Based Tracking
5 Click on Delete Schedule.
LOOKING UP A SCHEDULED TEMPLATE’S JOB HISTORY
The job history of a scheduled template shows the date of the job, the job status (S for Successful, E for Error 
or N for New), the process code (if job status = S or E) and processing information.
1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Jobs.
3 In the Search Results for Scheduled Jobs pane, click on the job that you wish to look up.
4 Click on View Scheduled Jobs.
History of Wave Batch Jobs
5 When you finish looking up your scheduled template’s job history, click on Close.
Paper-Based Tracking
You can generate a document to support paper-based picking for product that is not properly labeled. Wave 
Manager will automatically break tasks down into the standard MHE capacity based on your configuration in 
REGI. You set up paper-based tracking in LTRE (Load Type/Task Profiles). In this program, you create a 
relationship between a load type code (LOAD) and a task profile (REGI).
Paper-based tracking requires a custom document from HighJump.
LTRE screen

ALLOCATION AND WAVE MANAGER 4.2 241
A
absolute FIFO/LIFO (PIPR) 55
allocation
automatic de-allocation of an order 100
by minimum level 2, 3 and 4 values 119
by shelf life 102
by shelf life percentage 104
by weight 81
de-allocating an order in DEOR 96
inventory only 85
looking up order processed in ASOR 95
of fully filled orders only 117
of variable quantity breakdown product 80
overview 49
picking 67
put-away 4
reserving a minimum level of inventory 125
soft 111
using ASOR 87
wildcard characters and Boolean logic, using 116
ASOR (Assign Orders to Location) 87
Assign Orders to Location (ASOR) 87
automatic de-allocation 100
automatic replenishment 142
B
Boolean logic and wildcard characters, using in allocation
116
Breaking inventory into multiple to locations group (ILOP)
15, 16, 17, 18
C
Calculate capacity by lowest/highest SKU class group 
(ILOP) 14
Capacity group (ILOP) 15, 70
CCOP (Customer/Consignee Override of PIPR) 65
combining fixed position and floating positions in the same 
pick line 153
cross-docking (opportunistic) 197
Cube capacity group (ILOP) 12
Customer/Consignee Override of CCOP) 65
D
deactivating directed put-away for selected receipts 34
De-Allocate Order (DEOR) 96
de-allocation (automatic) 100
de-allocation (manual) 96
DEOR (De-Allocate Order) 96
Directed Move (ILOP) 182
Directed Move Processing (DMPR) 185
Directed Move Profile (DMPA) 179
Directed Move Report (DMVR) 189
directed moves
assigning suggested locations for in DMPR 185
confirming 190
looking up in LOEN 194
overview 176
printing labels for 188
printing the Directed Move Report 189
setting up 177
directed put-away 4
DMPA (Directed Move Profile) 179
DMPR (Directed Move Processing) 185
DMVR (Directed Move Report) 189
double stacking product in directed put-away 17
DOWA (Deallocate Orders by Wave) 227
E
Empty and/or partially filled location group (ILOP) 6
Entire Dock Quantity group (ILOP) 19
Evaluate Minimum flag in ORPR 125
F
FIFO group (ILOP) 73
FIFO/LIFO parameters in PIPR, setting 52
Fill location group (ILOP) 11
fully filled orders, shipping 117
INDEX

INDEX
H
hard allocation, performing in OPLU 112
Hold code group (ILOP) 11, 71
I
Ignore/use in transit when calculating capacity by cube 
group (ILOP) 10
Ignore/use in transit when calculating capacity by quantity 
group (ILOP) 9
Ignore/use on order when calculating capacity by cube 
group (ILOP) 11
Ignore/use on order when calculating capacity by quantity 
group (ILOP) 10
Ignore/use on order when calculating capacity by weight 
group (ILOP) 10
Ignore/use on receipt when calculating capacity by cube 
group (ILOP) 9
Ignore/use on receipt when calculating capacity by quantity 
group (ILOP) 8
Ignore/use on receipt when calculating capacity by weight 
group (ILOP) 9
Ignore/use outstanding moves/relocates when calculating 
capacity by cube group (ILOP) 11
Ignore/use outstanding moves/relocates when calculating 
capacity by quantity group (ILOP) 11
ILOP (Directed Move) 182
ILOP (Picking) 67
ILOP (Put-Away) 4
ILOP (Put-Away), overriding for individual receipt lines 26
ILOP (Replenishment) 142
IMSL (Item Minimum Shipping Level) 119
INAT (Inventory Attribute Factors) 46
inventory only allocation 85
IPUP (Item Put-Away Parameters) 44
Isolator group (ILOP) 5, 69
Item Minimum Shipping Level (IMSL) 119
item-specific picking profiles 65
IVLP (Item Velocity Location Profile) 27
L
Last location used group (ILOP) 12
Location Height group (ILOP) 16
Location Size Codes (LOCS) 40
Location size group (ILOP) 12
Location type group (ILOP) 74
LOCS (Location Size Codes) 40
LTRE (Load Type / Regions) 240
M
manual de-allocation 96
minimum level of inventory, reserving 125
minimum shipping levels for item in IMSL 119
Mixed product group (ILOP) 70
mixing fixed position and floating locations in the same pick 
line 153
O
on demand replenishments 165
On receipt hold code group (ILOP) 71
On receipt mixed product group (ILOP) 71
On receipt partial quantity group (ILOP) 73
OPLU (Order Line Inventory/Location Update) 112
opportunistic cross-docking 197
Opportunistic cross-docking group (ILOP) 14
orders
allocating in ASOR 87
automatically de-allocating 100
manually de-allocating 96
pending versus regular 49
shipping by weight 81
shipping only fully filled 117
shipping with insufficient inventory 50
ORPR (Order Priorities) 100
Overflow Location Size Code field (LOCS) 41
Overflow Sequence Number field (LOCS) 41
overpicking order lines 62
Override quantity breakdown group (ILOP) 74
overriding directed put-away zone code 39
P
Pallet Breakdown group (ILOP) 73
pallet restacking 195
pallet type, put-away by 46
paper-based tracking 240
Partial quantity group (ILOP) 72
Partially filled location group (ILOP) 6
Pick Line Item Assignment (PIIT) 144
pick lines and replenishment
mixing fixed position and floating locations in the same 
pick line 153
overview 131
putting away to a pick line using directed put-away
156
setting up a fixed position pick line 134
setting up a floating pick line 151
troubleshooting 173
types of pick lines 133
picking (directed) 67
Picking Profile (PIPR) 52
PIIT (Pick Line Item Assignment) 144
PIIT Location Capacity group (ILOP) 18
PIPR (Picking Profile) 52
PND Location Capacity group (ILOP) 18
PnD Location group (ILOP) 18
Product Stacking group (ILOP) 17
proximity logic for last location used group 42
PUPR (Put-Away Profile Code) 31, 157
put-away (directed) 4
put-away by location size 40
put-away by pallet type 46
put-away by zone code 38
Put-Away Profile Code (PUPR) 31, 157
R
Receipt date group (ILOP) 69
relative FIFO/LIFO (PIPR) 55
Relocate to Pick Line (REPI) 163

INDEX
ALLOCATION AND WAVE MANAGER 4.2 243
REPI (Relocate to Pick Line) 163
replenishment (automatic) 142
replenishment by inventory level 2 pick line 154
replenishments
confirming in REPI 163
confirming in RFRP 167
defining parameters for in ILOP (Replenish from Bulk)
142
deleting 166
looking up in LOEN 164
on demand 165
overriding the priority of in RFRO 172
performing 162
top up 165
reserve logic
entering orders in ENOR 107
looking up inventory in LOEN 110
overview 105
setting up 106
using in a non-RF environment 109
reserving a minimum level of inventory 125
restacking of pallets 195
RF Relocate (RFRL) 193
RF Replenish (RFRP) 167
RFRL (RF Relocate) 193
RFRO (Replenishment Priority Override) 172
RFRP (RF Replenish) 167
S
shelf life percentage, allocating product by 104
shelf life, allocating product by 102
shipping by weight 81
shipping only fully filled orders 117
soft allocation 111
sort sequences for last location used group 42
SSDP (Skip Directed Put-Away) 34
stacking rules (ILOP) 17
standard logical groups for directed picking 69
standard logical groups for directed put-away 5
T
top up replenishments 165
V
variable quantity breakdown product, allocating 80
VELO (Velocity Codes) 28
velocity codes, attaching to ILOP profile 27
W
Wave Manager
confirming waves in CHOF 228
creating a new template 215
custom SQL filters 224
deallocating orders by wave (DOWA) 227
deleting a template 223
deleting a wave 229
deleting orders from a wave 227
generating wave summary report 231
label picking, setting up 207
launching 210
looking up a wave’s completion status 229
looking up a wave’s job history 229
looking up orders on a wave 226
looking up print job details 230
modifying a template 222
overview 205
paper-based tracking 240
pick methods 207
reprinting wave labels 233
running a wave 224
scheduling a wave 235
setting up wave preferences 221
SQL Inspector 223
updating a template 222
Wave Deallocation Rule field (CUST) 209
working with pick lists and the column manager 212
weight, allocating by 81
wildcard characters and Boolean logic, using in allocation
116
Z
Zone code group (ILOP) 6
zone code, putting away by 38

INDEX
