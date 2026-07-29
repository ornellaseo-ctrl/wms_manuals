# Manual H — RF Guide (Guia de Operações RF/Scanner)

> **ID do Manual:** H  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Operações via scanner RF: setup (SCPR/BAPR/MRFP/MIRP), check/unload (RFCH), put-away (RFPU), picking (RFPIC), wave pick (RFPK), relocação (RFRL), ajustes (RFAJ), cartonization, outbound pallet building, staging, weight discovery, voice picking, equipment tracking, tasking (REGI).

---

AccellosOne Enterprise 
3PL RF Guide (Classic)
January 2017
Release 4.2***

Copyright © HighJump
All rights reserved
This manual is reserved for licensed users of AccellosOne Enterprise 3PL and e-Vista. If you are not a 
licensed user of AccellosOne Enterprise 3PL and e-Vista, no part of this publication may be reproduced, 
stored in a retrieval system or transmitted in any form or by any means electronic, mechanical, recording or 
otherwise, without the prior written consent of HighJump.
The information in this manual is furnished for informational use only, is subject to change without notice and 
should not be construed as a commitment of HighJump. HighJump assumes no responsibility or liability for 
any errors or inaccuracies that may appear in this manual.

TABLE OF CONTENTS
INTRODUCTION ......................................................................... 1
Before You Begin ................................................................................................ 2
AccellosOne 3PL Documentation Set ............................................................... 2
GENERAL SETUP PROGRAMS ..................................................... 5
Scan Parameter Profile (SCPR) ......................................................................... 6
Application Identification Block .................................................................... 12
Bar Code Profile Code (BAPR) ........................................................................ 12
RF Profile (MRFP).............................................................................................. 16
RFCH Queries ............................................................................................. 16
RFCH Only................................................................................................... 18
RFCH Only (2) ............................................................................................. 25
RFCH Only (3) ............................................................................................. 29
RFCH Only (4) ............................................................................................. 33
RFCH Shared .............................................................................................. 33
RFPU ........................................................................................................... 38
RFPIC .......................................................................................................... 41
RFPIC (2)..................................................................................................... 48
RFPIC (3)..................................................................................................... 54
RFPIC (4)..................................................................................................... 57
RFPIC (5)..................................................................................................... 62
Miscellaneous .............................................................................................. 64
Miscellaneous (2)......................................................................................... 67
Miscellaneous (3)......................................................................................... 71
Miscellaneous (4)......................................................................................... 74
Miscellaneous (5)......................................................................................... 79
Item RF Profile (MIRP) ...................................................................................... 84
Miscellaneous Tab ....................................................................................... 86
Warehouse/Customer/Location Config (WCLC)............................................. 86
Depositor Workflow Profile (DIFP) .................................................................. 87
RF Operator (RFOP).......................................................................................... 87
Activating an RF Operator in ActiveDesktop................................................ 89
Extra Charge Setup for RF ............................................................................... 89
Warehouse Zones (WHZO)............................................................................... 92
Header Block ............................................................................................... 93
Formula Block .............................................................................................. 94
Procedure .................................................................................................... 97
Overflow Sequence Block............................................................................ 99
Company Code (COMP).................................................................................. 100
RF Supervisors................................................................................................ 101

ii 4.2*** RF GUIDE
Supervisor Notification................................................................................... 101
OUTBOUND SETUP PROGRAMS ............................................... 105
About the Task Engine ................................................................................... 106
Activating the Task Engine ........................................................................ 106
Overview of Setup Programs ......................................................................... 106
Customer Codes (CUST) ................................................................................ 107
Customer / Consignee Document Setup (CCDU)......................................... 109
Item Hazardous Material Violation (IHZV) ..................................................... 110
Outbound Pallet Building With the Pallet Build Engine .............................. 111
Task Profile (REGI).......................................................................................... 115
Adding Filters to REGI ............................................................................... 118
Item Consignee Configuration (ICOC)........................................................... 119
Outbound Process Configuration (CCCC).................................................... 120
Document Messages Block ....................................................................... 123
Warehouse Customer Consignee OPID Rule (WCCO) ................................ 124
Customer/Consignee Outbound Rules (CCOR) ........................................... 124
GENERAL NAVIGATION AND LOOK-UP PROGRAMS .................... 131
Accessing RF .................................................................................................. 132
Changing Your Company ............................................................................... 132
Looking Up Inventory in RFIT ........................................................................ 132
Looking Up Inventory by Location in RFPR ................................................. 134
Looking Up Receipts in RFIL ......................................................................... 136
Looking Up Allocated Order Lines in RFOL ................................................. 138
Looking Up Inventory in RFLOIP................................................................... 141
Looking Up Locations in LOLORF ................................................................ 142
Looking Up Inventory in LOENRF ................................................................. 144
Looking Up Receipts in LORERF .................................................................. 145
Looking Up Orders in LOORRF ..................................................................... 147
Looking Up Reserve Logic Customers in RFLR .......................................... 148
INBOUND PROCESSING .......................................................... 151
Overview of Put-Away .................................................................................... 152
Understanding Inbound Flows in RF ............................................................ 153
Overview of the Unique Identifier (UI) ........................................................... 153
Unloading Product in RFCH........................................................................... 154
Overriding the System-Assigned Location................................................. 169
Entering Trailer and Pallet Information ...................................................... 170
Performing Queries.................................................................................... 174
Entering Partial U-Type Receipt Lines....................................................... 175

Printing Labels ........................................................................................... 176
Understanding Variances in RFCH............................................................ 177
Processing Variances ................................................................................ 178
Entering Process Values............................................................................ 180
Validating Process Values ......................................................................... 182
Creating a New Line .................................................................................. 183
Receiving Product Under an Alternate Item Code ..................................... 184
Receiving Product on Automatic Hold ....................................................... 186
Receiving Product with a Variable Product Breakdown............................. 187
Receiving Mixed Product ........................................................................... 187
Looking Up Temperature and Trailer Information in LORE ....................... 189
Looking Up Remarks and Messages in RFCH .......................................... 190
Entering Temperature and Trailer Information in RFTT .............................. 191
Putting Away Product in RFPU...................................................................... 192
Overriding the System-Assigned Location................................................. 198
Entering Variances..................................................................................... 199
Putting Away Product Under an Alternate Item Code................................ 201
Putting Away in a Pick Line Location ......................................................... 202
Entering Process Values in RFIPS ................................................................ 202
Capturing the Weight Dynamically from a Bar Code ................................. 204
Deleting a Receipt Line in RFDL.................................................................... 208
Clearing Tie/Hi/Loose Variances in RFCV .................................................... 210
OUTBOUND PROCESSING ........................................................ 213
Overview of Shipping ..................................................................................... 216
Understanding Outbound Flows in RF.......................................................... 217
Understanding Pick Methods......................................................................... 217
Overview of RF Picking Programs ................................................................ 219
RFPIC (RF Pick) ........................................................................................ 219
RFPK (RF Wave Pick) ............................................................................... 219
RFPV (RF Picking Voice)........................................................................... 220
RFINVT (RF Interleaving) .......................................................................... 220
Picking Orders in RFPIC................................................................................. 220
Picking Full Pallets from Bulk..................................................................... 225
Picking Cases ............................................................................................ 227
Picking Product With Process Values........................................................ 232
Picking Partial Quantities of Product With Process Values ....................... 234
Picking Reserve Logic Orders ................................................................... 235
Placing Product on Hold ............................................................................ 236
Entering Pallet Information......................................................................... 239
Excluding Orders from Overpicking in EOSU ............................................ 241
Picking Pick Line Product from a Non-Pick Line Location ......................... 242

iv 4.2*** RF GUIDE
Performing Replenishments in RFPIC ....................................................... 243
Looking Up Remarks and Messages in RFPIC ......................................... 243
Recovering From a Dropped Connection .................................................. 244
Performing Inventory Count Backs............................................................... 246
Performing the Count in RFPIC ................................................................. 247
Looking Up Inventory Discrepancy Records in ICIN.................................. 249
Looking Up Inventory Discrepancy Records in RFCL................................ 250
Removing Inventory Discrepancy Records from ICIN ............................... 251
Removing Inventory Discrepancy Records in RFCL.................................. 252
Removing Inventory Discrepancy Records in RFCI................................... 252
Entering Temperature and Trailer Information in RFTT .............................. 253
Entering Pallet Information in RFOPE........................................................... 254
Editing a Pallet Details Record in RFOPE ................................................. 256
Deleting a Pallet Details Record in RFOPE ............................................... 257
Adjusting Your Pallet Type in RFPA ............................................................. 257
Looking Up Your OPID’s ................................................................................ 258
Looking Up Your OPID’s in LOCN ............................................................. 259
Looking Up Your OPID’s in RFNCO .......................................................... 259
Looking Up an Order’s OPID’s in LOOR.................................................... 260
Confirming Orders by OPID in RFCO............................................................ 261
Confirming Individual Order Lines by UI in RFCU ....................................... 263
Reprinting Outbound Labels in RFOLP ........................................................ 264
Picking Cases from a Pick Line in CASE...................................................... 267
Merging OPID’s in RFOPB.............................................................................. 272
Looking Up Your New OPID ...................................................................... 274
Picking Substitution ....................................................................................... 275
Setting Up Picking Substitution.................................................................. 275
Setting Up Your Picking Substitution Rules in PSPR ................................ 276
Attaching Your PSPR Profile Code to the Appropriate Code..................... 279
Excluding Orders from Picking Substitution in EOSU................................ 280
Performing Picking Substitution in RFPIC ................................................. 281
Entering Process Values in RFOPS .............................................................. 284
Capturing the Weight Dynamically from a Bar Code ................................. 289
Manually Entering the Weight .................................................................... 294
Removing Labels That Have Been Scanned ............................................. 295
Removing Cases Either Scanned or Unscanned....................................... 297
Removing Cases From a Fully Scanned Order ......................................... 298
Performing an Incomplete Scan................................................................. 300
Transferring Inbound Process Values to Outbound Orders....................... 301
Setting Up Catch Weight Tolerances......................................................... 302
Picking Waves in RFPK .................................................................................. 304
Relocating Product in RFST........................................................................... 307

Merging OPID’s in RFMG................................................................................ 309
Merging Two Existing OPID’s .................................................................... 310
Creating a New OPID ................................................................................ 311
Performing Outbound Audits in RFOA ......................................................... 313
Adjusting Cubic Dimensions in RFCC .......................................................... 316
Assigning Orders to Loads in SELO ............................................................. 317
Replacing Damaged Product in RFRD .......................................................... 317
Working With Pallet Build Assignments in PABU........................................ 319
Setting Up Your Pallet Build Parameters in COMP ................................... 320
Performing Queries.................................................................................... 321
Releasing and Staging a Suspended Load................................................ 324
Merging Assignments ................................................................................ 324
Deleting Assignments ................................................................................ 325
Adding Assignments .................................................................................. 326
Deleting Lines From an Assignment .......................................................... 327
Overriding Assignments............................................................................. 328
Changing Your Order Parameters ............................................................. 329
Restoring Your Original Order Parameters................................................ 329
Printing the Pallet Build Summary Report.................................................. 330
Printing the Pallet Build Detail Report........................................................ 331
Suspending a Task in RFOT...................................................................... 331
Releasing a Suspended Task in RFOT ..................................................... 332
MISCELLANEOUS PROCESSING ............................................... 333
Relocating Inventory in RFRL........................................................................ 335
Relocating Inventory (Operator Selects To Location) ................................ 336
Relocating Inventory (Directed Move System Activated)........................... 339
Performing Multi-Pallet Moves....................................................................... 344
Adjusting Non-Serial Number Inventory in RFAJ ........................................ 346
Adjusting Out Existing Inventory ................................................................ 346
Adjusting In New Inventory ........................................................................ 348
Adjusting In Existing Inventory................................................................... 352
Adjusting In Inventory With a Variable Quantity Breakdown...................... 354
Adjusting Serial Number Inventory in RFAJB.............................................. 355
Adjusting in Inventory................................................................................. 356
Adjusting Out Cases .................................................................................. 358
Adjusting Out Full Pallets........................................................................... 359
Adjusting Out Cases Using the Remove Command .................................. 360
Recovering From a Lost Connection ......................................................... 362
Merging Inventory in RFMI ............................................................................. 363
Merging Existing Inventory Entities............................................................ 364
Creating New Inventory Entities................................................................. 367

vi 4.2*** RF GUIDE
Adding Extra Charges to a Receipt/Order in RFEC ..................................... 370
Scenario 1 — RF Operator Enters Charge Quantity Only ......................... 370
Scenario 2 — RF Operator Enters Charge Code and Quantity ................. 372
Deleting an Extra Charge........................................................................... 374
Assigning Check Digits to Locations in RFCD............................................. 374
Entering Incidents in RFINC........................................................................... 377
Performing CRM Tasks in RFCE.................................................................... 379
Checking Your Bar Codes in RFBR............................................................... 381
Entering Hold Adjustments in RFHO ............................................................ 382
Placing Product on Hold ............................................................................ 382
Removing Inventory from Hold .................................................................. 384
Processing Supervisor Overrides in RFSUN................................................ 385
Entering Inventory Attributes in RFATT........................................................ 387
VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM 389
Overview .......................................................................................................... 390
Setting Up Voice-Activated Picking .............................................................. 390
Setting Up Your Voice Profile in VOPR ..................................................... 390
Setting Up Your Voice Profile (Customer) in VOPC .................................. 393
Setting Up Your Task Profile in REGI ........................................................ 396
Setting Up Your RF Operators in RFOP .................................................... 397
Setting Up Your Check Digit Parameters in WARE (Optional) .................. 397
Assigning Check Digits to Locations in LOCA ........................................... 398
Setting Up Your Reason Codes in REAS .................................................. 400
Activating Your Voice Terminals in MHEC................................................. 401
Picking Orders in RFPV.................................................................................. 403
Assigning RF Operators to Orders in RFOT................................................. 406
Assigning RF Operators to Orders and Order Lines.................................. 406
Assigning RF Operators to Loads.............................................................. 409
Assigning RF Operators to Pick Methods .................................................. 412
Removing an Operator Assignment........................................................... 412
Suspending a Task .................................................................................... 413
Releasing a Suspended Task .................................................................... 413
Changing the System-Assigned Staging Location..................................... 414
Changing the Priority Level of a Task ........................................................ 414
Clearing Work Assignments in CTPA ........................................................... 415
CARTONIZATION .................................................................... 417
Overview .......................................................................................................... 418
Cartonization Tab (MRFP) .............................................................................. 418
Carton Size Setup (CTSZ)............................................................................... 420
Outbound Process Configuration (CCCC).................................................... 422

Carton Size Code Block............................................................................. 425
Packing Station Code (PKST) ........................................................................ 425
Item Cartonization Profile Code (ICNP)......................................................... 427
Consignees (CONS) ........................................................................................ 429
Performing Manual Cartonization in RFSC................................................... 429
Working With Closed Cartons.................................................................... 433
Performing System-Driven Cartonization in RFPK...................................... 434
Performing Second Level Cartonization....................................................... 441
Performing Manual Packing in EPSD............................................................ 442
Tracking Your Progress in EPSD............................................................... 447
Deleting a Carton’s Contents ..................................................................... 448
Working With Unclosed Cartons ................................................................ 448
Looking Up Cartons in LOCN ........................................................................ 449
Deleting Closed Cartons in DCAR................................................................. 451
EQUIPMENT TRACKING .......................................................... 453
Overview .......................................................................................................... 454
Company Code (COMP).................................................................................. 455
RF Checklist (MCHK) ...................................................................................... 455
Material Handling Types (MHET) ................................................................... 458
Material Handling Equipment Code (MHEC)................................................. 461
RF Operator (RFOP)........................................................................................ 463
Locations (LOCA)............................................................................................ 463
Warehouse Shift Setup (WASH) .................................................................... 464
Operator Code (OPER) ................................................................................... 465
Looking Up Equipment Tracking Data .......................................................... 466
OUTBOUND TASKING ............................................................. 467
Overview .......................................................................................................... 468
Understanding Order Lines, Pick Assignments and Outbound Tasks ....... 468
Company Parameters (COMP) ....................................................................... 470
Wave Manager ................................................................................................. 472
Material Handling Types (MHET) ................................................................... 472
Warehouse Zones (WHZO)............................................................................. 472
Warehouse and Location Format (WARE).................................................... 473
Locations (LOCA)............................................................................................ 473
Task Profile (REGI).......................................................................................... 474
RF Outbound Tasking in RFITLV................................................................... 476
Looking Up Your Outbound Tasks in RFOT................................................. 478
INDEX ................................................................................... 483

viii 4.2*** RF GUIDE

INTRODUCTION
Before You Begin ................................................................................................ 2
AccellosOne 3PL Documentation Set ............................................................... 2

INTRODUCTION
Before You Begin
Before You Begin
This manual contains the majority of core RF programs that are part of AccellosOne 3PL. The following core 
RF programs are not included: 
▪ RFCY (RF Cycle Count) — see Cycle Counting Guide
▪ RFPH (RF Entering Physical Inventory Tickets) — see Physical Inventory Guide
▪ RFPL/RFPR (Replenishment) see Allocation and Wave Manager 
▪ OLOP (Outbound Loading Process) see Operations 2 Guide
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
Introduction Guide logging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your 
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
tracking, tasking, cartonization, outbound pallet building

INTRODUCTION
AccellosOne 3PL Documentation Set
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory 
level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

INTRODUCTION
AccellosOne 3PL Documentation Set

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR) ......................................................................... 6
Bar Code Profile Code (BAPR) ........................................................................ 12
RF Profile (MRFP).............................................................................................. 16
Item RF Profile (MIRP) ...................................................................................... 84
Warehouse/Customer/Location Config (WCLC)............................................. 86
Depositor Workflow Profile (DIFP) .................................................................. 87
RF Operator (RFOP).......................................................................................... 87
Extra Charge Setup for RF ............................................................................... 89
Warehouse Zones (WHZO)............................................................................... 92
Company Code (COMP).................................................................................. 100
RF Supervisors................................................................................................ 101
Supervisor Notification................................................................................... 101

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
Scan Parameter Profile (SCPR)
In this program, you define your scan parameters for bar coded labels. SCPR allows you to break up a bar 
code into its component parts and capture a separate value for each part. For example, the first four 
characters of the bar code could represent the lot number, characters 6 to 10 could represent the weight and 
characters 11 to 14 could represent the serial number.
In the Header Block of SCPR, you define your scan profile code, description and total length. In the Detail 
Block of SCPR, you define whether the bar code is inbound or outbound, its type (weight, serial number, etc.), 
starting and end position, the action required when it is scanned and its data type. You can have as many 
records in the Detail Block as you require. For example, if a bar code consists of three parts (one for the 
weight, one for the level 2 value and one for the serial number), you would set up three records in the Detail 
Block for that scan parameter profile.
If you are capturing weights, serial numbers or a temperature, the profiles that you set up in SCPR must be 
attached to the appropriate items in ITEM. If you are capturing inventory levels that were unknown at the time 
of receipt entry (that is, blind receiving), the SCPR profile(s) are NOT attached to the appropriate items in 
ITEM.
NOTE SCPR only supports bar code scanning of items with no more than two 
SKU’s in their quantity breakdown (for example, pallet/case). You cannot scan bar 
codes of items with three or more SKU’s in their quantity breakdown (for example, 
pallet/case/each).
FIELD DESCRIPTIONS
Scan Profile Code Mandatory
Your scan profile code.
Description Mandatory
The description for your scan profile code.
Scan Profile Industry 
Type
If you enter 128, your label will be defined as a UCC-128 label.

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
Variable Length Y = Yes
N = No
Set this flag to Yes if the bar code that you are attaching your scan parameter 
profile to is a variable length bar code. Otherwise, set the flag to No.
Scan Profile Code Length Mandatory
The total length of the bar code.
FIELD DESCRIPTIONS (DETAIL BLOCK)
Inbound/Outbound I = Inbound
O = Outbound
B = Both
If you specify I for Inbound, the portion of the bar code that you are capturing 
is restricted to an inbound RF process. If you specify O for Outbound, the portion of the bar code that you are capturing is restricted to an outbound RF process. If you specify B for Both, the portion of the bar code that you are 
capturing can be used in either an inbound or outbound RF process. 
Sequence Mandatory
In this field, you specify the sequence of each scanned in value. The 
sequence that you enter need not match the physical layout of the bar coded 
label.
You can extract an inventory level from multiple sequences in a bar code. For 
example, if your bar code is 0123456789, you can define two sequences for 
the level 3 value: sequence 1 for positions 1 to 2 and sequence 2 for positions 
9 to 10. Your level 3 value extracted from the bar code would be 0189.
The extraction of an inventory level from multiple sequences of a bar code is 
only available in RFCH blind receiving.
FIELD DESCRIPTIONS

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
Type CUBE = Cube
EDT1 = YYMMDD
EDT2 = MMDDYYYY
EDT3 = MMDDY
EDT4 = MMDDYY
EXPY = Expiry Date
HGT = Height
IGNO = Ignore Entry
LEN = Length
LEV1/2/3/4 = Inventory Level 1/2/3/4
LV1V/LV2V/LV3V/LV4V = Level 1/2/3/4 Validation*
LV2D/LV3D/LV4D = Inventory Level 2/3/4 Description
OTHR = Other
PLTQ/PLTW = Pallet Quantity/Weight (custom code required)
SER = Serial Number in Weight Bar Code
SN = Serial Number
TARE = Tare Weight
TEMP = Temperature
UI = Unique Identifier
WGTG/WGTN = Weight Gross/Weight Net
WID = Width
The type of value that you are capturing. If a portion of the bar code that you 
are scanning contains information that you do not wish to capture, you can 
use the IGNO (Ignore Entry) option. Any part of a bar code assigned this type 
will not be captured by AccellosOne 3PL.
NOTE If you use two or more values such as CUBE, HGT, LEN and WID in 
the same scan parameter profile, each value must be captured on a separate 
label. Only the values of SER, LEV1/2/3/4, UI, WGTG and WGTN can be 
combined together and captured from a single label.
* The inventory level will be validated against the acceptable values that 
you defined in DLVP and any item whose lot number, serial number, 
date code, etc. does not match the acceptable values will be rejected. 
Start Position Mandatory for fixed position bar codes
The position of the start character of the value that you are capturing. For 
example, if the total length of your bar code is 10 characters and the portion of 
the bar code that you are capturing is position 3 through 7, you would enter 3 
in this field.
FIELD DESCRIPTIONS (DETAIL BLOCK)

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
End Position Mandatory for fixed position bar codes
The position of the last character of the value that you are capturing. For 
example, if the total length of your bar code is 10 characters and the portion of 
the bar code that you are capturing is position 3 through 7, you would enter 7 
in this field.
You can also define the end position by leaving this field blank and entering 
the appropriate value in the Length field.
Start Character Reserved for future use
The number, letter or special character indicating the start of the portion of the 
bar code that you wish to capture.
End Character Reserved for future use
The number, letter or special character indicating the end of the portion of the 
bar code that you wish to capture.
Length Only applicable to fixed position bar codes
The length of the portion of bar code that you are capturing If you are using 
the UCC-128 label, the length is usually 48.
Action The following actions are supported:
01 = Entry
02 = Validation
If you select Entry, validation may or may not occur depending on the value 
being captured. If you select Validation, AccellosOne 3PL validates the value 
against a list of valid values.
Date Format In this field you can specify the date format of any dates scanned in from a 
SSCC label and saved in AccellosOne 3PL as an inventory level. 
FIELD DESCRIPTIONS (DETAIL BLOCK)

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
Unit of Measure Code Only required if you enter a weight, cube or linear measurement in the Type 
field
The unit of measure for the captured value.
Data Type CHAR = Character
DATE = Date
INT = Integer
MONY = Money
NUM = Number
This field controls the formatting of values that you capture. If you select 
DATE, the number that you enter will be formatted as a date. If you select 
MONY, the number that you enter will be formatted in dollars and cents (for 
example, $99.99).
Use CHAR for serial and purchase order numbers.
Decimal Position Only applicable to scanned in values with a data type of MONY or NUM
The position of the decimal point. For example, if you specify 2 and your captured value is 12345, AccellosOne 3PL will record the value as 123.45. If you 
do not specify the position of the decimal point, all numbers will be captured 
as integers.
Weight Modifier Only applicable to scanned in values whose unit of measure code is a weight 
(KGS or LBS)
If required, you can specify a weight modifier and the scanned in weight will be 
multiplied by the modifier.
FIELD DESCRIPTIONS (DETAIL BLOCK)

GENERAL SETUP PROGRAMS
Scan Parameter Profile (SCPR)
Validate Item Code Only available for item code validation
P = Position-Based
L = Left Starting Position
R = Right Starting Position
Item code validation allows you to validate the item code in RFOPS when the 
item code in the bar code is shorter than the item code in ITEM. That is, the 
level 1 in the bar code is a subset of the full level 1 in ITEM.
In this field, you specify the position of the item code in the bar code.
Item Code Start Position Only available for position-based validation
The start position for the item code.
Item Code End Position Only available for position-based validation
The end position of the item code.
Item Code Length for 
Right/Left Starting Position
The number of characters from the right or left that comprise the item code.
FIELD DESCRIPTIONS (DETAIL BLOCK)

GENERAL SETUP PROGRAMS
Bar Code Profile Code (BAPR)

SCPR (Scan Parameter Profile) screen showing scan parameters for scan profile code L2
APPLICATION IDENTIFICATION BLOCK
Used to set up the MARS bar code.
Bar Code Profile Code (BAPR)
In this program, you set up your bar code profile codes. Bar code profile codes are only required if you wish to 
scan in inventory levels or UI (Unique Identifier) values that are embedded in a bar code label. If the value 
that you are scanning is not embedded in another code (that is, the level 1 or 2 or 3 label contains no other 
value or extra characters), you do not need to set up a bar code profile in BAPR.
UI values can be scanned in RFCH, RFPIC and many other RF programs. Inventory levels, on the other 
hand, can only be scanned in RFCH. For each profile that you set up in BAPR, you define the value being 
scanned (LEV1, LEV2, LEV3, LEV4, UI), the scan parameter code to which it is attached, the bar code length 
and the bar code ID. 
If you are capturing two or more inventory levels in RFCH, you can do so from multiple bar code labels. For 
example, you could scan in levels 1 and 2 from bar code label A and level 3 from bar code label B.

GENERAL SETUP PROGRAMS
Bar Code Profile Code (BAPR)
Consider the following SCPR and BAPR setups for various bar coded labels. In the following examples, “---” 
represents an inventory level, UI, weight or serial number that you wish to capture, while “999” represents 
non-AccellosOne 3PL information in the bar code that you do not wish to capture.
BAR CODE(S) SCPR SETUP BAPR SETUP ITEM SETUP
---L1--- N/A N/A N/A
---L3--- N/A N/A N/A
999---L1--- A profile with one detail record 
whose type is set to LEV1.
The SCPR profile set up in the 
previous column must be 
attached to a bar code profile 
whose bar code type is set to 
LEV1.
N/A
---L2---999 A profile with one detail record 
whose type is set to LEV2.
The SCPR profile set up in the 
previous column must be 
attached to a bar code profile 
whose bar code type is set to 
LEV2.
N/A
---L1---L2---L3--- A profile with three detail 
records: one whose type is set to 
LEV1, another whose type is set 
to LEV2 and a third whose type 
is set to LEV3.
The SCPR profile set up in the 
previous column must be 
attached to a bar code profile 
whose bar code type is set to 
LEV1.
N/A
999---L1---
---L2---999
Two profiles required: one with a 
detail record set to LEV1 and 
one with a detail record set to 
LEV2.
Two records required: one for the 
level 1 label and one for the level 
2 label. The appropriate SCPR 
profile must be attached to each 
record.
N/A
999---L1---999---L2---999
999---L3---999
Two profiles required. The first 
profile will contain two detail 
records: one set to LEV1 and 
one set to LEV2. The second 
profile will contain a single record 
set to LEV3.
Two records required: one for the 
level 1/2 label and one for the 
level 3 label. The appropriate 
SCPR profile must be attached 
to each record.
N/A
---UI---999 A profile with one detail record 
whose type is set to UI.
The SCPR profile set up in the 
previous column must be 
attached to a bar code profile 
whose bar code type is set to UI.
N/A
999---WEIGHT--- A profile with one detail record 
whose type is set to WGTG or 
WGTN.
N/A The SCPR profile must 
be attached to the item.

GENERAL SETUP PROGRAMS
Bar Code Profile Code (BAPR)
FIELD DESCRIPTIONS
Bar Code Profile Code Mandatory
Your bar code profile code.
Description Mandatory
The description for your bar code profile code.
Bar Code Type The following bar code types are supported:
LEV1 (Inventory Level 1)
LEV2 (Inventory Level 2)
LEV3 (Inventory Level 3)
LEV4 (Inventory Level 4)
UI (Unique Identifier)
SER (Serial Number)
YYMMDD
NOTE When the same label contains two or more inventory levels in 
SCPR, the bar code type is set to the lowest inventory level. For example, if 
your label format is 999---LEV2---LEV3, your bar code type would be set to 
LEV3, which is the lowest inventory level.
Scan Parameter Profile 
Code (SCPR)
Mandatory
The bar code profile’s scan parameter profile code. 
Bar Code ID Optional
The bar code’s ID. This ID identifies the manufacturer of the product. The 
number of characters in this field must equal the end position - the start position + 1.
NOTE Although bar code ID’s are optional in BAPR, they should be used 
whenever they are available. If you do not specify a bar code ID, operators will 
be confronted with a pick list whenever two bar codes have the same length. If 
the RF operator selects the wrong code from the pick list, he or she could capture bad data.

GENERAL SETUP PROGRAMS
Bar Code Profile Code (BAPR)
Start Position Mandatory if you enter a bar code ID
The starting position of the bar code ID.
End Position Mandatory if you enter a bar code ID
The ending position of the bar code ID.
Variable Length Only available for variable length bar codes based on the GS-1 standard.
The length of the variable portion of the bar code.
Bar Code Length Mandatory
The total length of the bar code. This length must match the length of the scan 
parameter profile code in SCPR.
Size of Fixed Part in Variable Length Bar Code
Only available for variable length bar codes based on the GS-1 standard.
See your HighJump implementation consultant for further information on this 
field.
ASCII Value of Separator 
in Variable Length Bar 
Code
Only available for variable length bar codes based on the GS-1 standard.
See your HighJump implementation consultant for further information on this 
field.
FIELD DESCRIPTIONS

GENERAL SETUP PROGRAMS
RF Profile (MRFP)

BAPR (Bar Code Profile Code) screen showing setup for bar code L12
RF Profile (MRFP)
In this program, you set up your RF profile code(s). The RF profile code defines the default values and 
available options in the core RF programs. Once you set up your RF profile code in MRFP, you must attach it 
to the appropriate customer(s) in CUST.
RFCH QUERIES
This tab shows your RFCH query options.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH Queries tab
FIELD DESCRIPTIONS (RFCH QUERIES)
Customize Query Results 
in RFCH
Yes
No
If you set this field to Yes, you can customize the RFCH pick list in query 
mode. For example, if you set the Receipt Number and Warehouse Code 
fields to Yes and all the other fields to No, only the receipt number and warehouse code will appear in the RFCH pick list when you perform a query.
If you set this field to No, you cannot customize the RFCH pick list and all values — customer code, receipt number, receipt line number, all inventory levels, etc — will display in this list. 

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH ONLY
This tab shows various RFCH options.
RFCH pick list screen showing customization
Receipt Number If you set this field to Yes, the receipt number will appear in the RFCH pick list 
when you perform a query.
Receipt Line Number If you set this field to Yes, the receipt line number will appear in the RFCH pick 
list when you perform a query.
Inventory Level 1 If you set this field to Yes, inventory level 1 will appear in the RFCH pick list 
when you perform a query.
Inventory Level 2 If you set this field to Yes, inventory level 2 will appear in the RFCH pick list 
when you perform a query.
Inventory Level 3 If you set this field to Yes, inventory level 3 will appear in the RFCH pick list 
when you perform a query.
Inventory Level 4 If you set this field to Yes, inventory level 4 will appear in the RFCH pick list 
when you perform a query.
Warehouse Code If you set this field to Yes, the warehouse code will appear in the RFCH pick 
list when you perform a query.
Quantity If you set this field to Yes, the quantity will appear in the RFCH pick list when 
you perform a query.
Hold Code If you set this field to Yes, the hold code will appear in the RFCH pick list when 
you perform a query.
FIELD DESCRIPTIONS (RFCH QUERIES)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)

RFCH Only tab
.
FIELD DESCRIPTIONS (RFCH ONLY)
Label Document Printed Optional
If you enter a document code in this field, the RF operator will be prompted to 
print the document in RFCH should he/she create a new receipt line. The document code that you enter in this field must have a document type of LA 
(Label) in DOCU.
Show Temperature and 
Pallet Blocks
Not required
Enter temperature, trailer/seal number and pallet block
Enter pallet block only
Enter trailer/seal number only
Enter temperature only
Enter trailer/seal number and pallet block
Enter temperature and trailer/seal number
Enter temperature and pallet block

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
In this field, you specify which information an RF operator can enter for each 
receipt: temperature only, pallet block only, trailer/seal number only, etc. The 
options in this field are not mandatory; that is, if temperature entry is activated, 
the RF operator can enter a temperature in RFCH, but is not required to do so.
RFCH screen showing prompt for temperature and trailer number information
Perform Trailer Checks Only available if the entry of trailer numbers is activated in the Show Temperature and Pallet Blocks field
Yes
No
If you set this flag to Yes, the RF operator will be prompted to perform a series 
of trailer checks. If you set this flag to No, the RF operator will NOT be 
prompted to perform any trailer checks.
RFCH screen showing trailer check
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow New Lines Yes (1)
No (2)
Stay in New Line Mode (3)
Allow New Line from Existing Entity on Receipt, Do Not Show New Line 
Message (4)
Allow New Line With Supervisor Approval
If you select option 1, the RF operator can create new receipt lines in RFCH 
with the CL (Create Lines) command and will be prompted to either mark a 
receipt as complete or create a new line when finishing the last line of a 
receipt. 
If you select option 2, the RF operator cannot create new receipt lines in 
RFCH and will not be prompted to do so when finishing the last line of a 
receipt.
If you select option 3, the RF operator will NOT be prompted to either mark a 
receipt as complete or create a new line and the header flow of the receipt will 
NOT be advanced.
If you select option 4, the RF operator can only add a new line if the new line 
consists of an existing inventory entity on the receipt. For example, the RF 
operator receives 20 cases for pallet ID 123 and later discovers an additional 
case for the same pallet ID. That case can be added, but a case for pallet ID 
456 (which is not on the receipt) cannot be added.
If you select option 5, the RF operator can only add a new line if a supervisor 
logs in to authorize the transaction.
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Duplicate Inventory No Validation (1)
Disallow Duplicate Inventory Entities (2)
Disallow Duplicate Inventory UI’s (3)
Disallow Duplicate Inventory Entities, No User Override (4)
Disallow Duplicate Inventory UI’s, No User Override (5)
This flag allows the RF operator to check for duplicate inventory in RFCH 
when the line type is U for Unknown in ENRE. If you select option 1, no popup message will appear when the RF operator receives duplicate inventory in 
RFCH.
If you select option 2, a pop-up message will appear when the RF operator 
receives a duplicate inventory entity and he/she will be prompted to accept or 
reject the duplicate scan.
If you select option 3, a pop-up message will appear when the RF operator 
receives a duplicate inventory UI and he/she will be prompted to accept or 
reject the duplicate scan.
If you select option 4, the RF operator will not be allowed to receive a duplicate inventory entity.
If you select option 5, the RF operator will not be allowed to receive a duplicate inventory UI.
Default Staging Warehouse/Location CodeIf you enter a staging location and warehouse, the Loc and Whse fields will be 
populated with these values when you are performing two-step put-away with 
manual staging. You can either accept the defaults or enter a new staging 
location and warehouse. 
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Must Use Tie/Hi/Loose to 
Calculate Receiving 
Quantity
No
Yes
Yes With Variance Check in P-Type Lines
If you set this flag to No, the Tie, Hi and Loose fields in RFCH will be disabled 
and the RF operator can only enter the total quantity for a receipt line. 
If you set this flag to Yes, the RF operator will be required to enter the tie, hi 
and loose quantities for each receipt line and the Qty field in RFCH will be disabled. For example, a tie, hi and loose quantity of 5/10/03 would equal 53 
cases, while a tie, hi and loose quantity of 5/10/-1 would equal 49 cases. The 
Yes option is designed to force RF operators to perform more accurate counts 
and reduce receiving errors.
If you set this flag to Yes With Variance Check in P-Type Lines, the following 
will occur. If the line quantity calculated from the tie/hi/loose quantities entered 
by the operator in RFCH does not match the expected quantity in ENRE, the 
operator will be allowed to enter the tie/hi/loose quantities a second time. If 
there is still no match, the variance must be processed by a supervisor in 
RFCV.
Variance Rules Variance screen for all users
Variance screen for supvr. only
Only allow if supvr. approved
This field determines whether or not the Variance screen is displayed when 
the quantity entered does not match the expected quantity. If you select the 
“Variance screen for all users” option, any user can process a variance. If you 
select the “Variance screen for supvr. only” option, non-supervisors will not be 
able to press F3 to zero out the line. 
If you select the “Only allow if supvr. approved” option, when non-supervisors 
press F3 to zero out the line a supervisor must sign on and approve the transaction.
NOTE Regardless of the option that you choose, the variance itself is 
always tracked in LORE even if the Variance screen does not display.
Tolerance Check for PO Reserved for future use.
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Enter Quantity Breakdown for U-Type LineNo
Yes
Set Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes
If you select No, the RF operator cannot change the quantity breakdown for a 
U-type line in RFCH. If you select Yes, the RF operator can change the quantity breakdown for a U-type line in RFCH; that is, override the quantity breakdown entered in ENRE. If you select “Set Quantity Breakdown to Line 
Quantity for IQBP With 2 SKU Classes”, the item’s quantity breakdown will be 
automatically set to the line quantity entered in RFCH.
The following requirements must be met for the Yes and “Set Quantity Breakdown to Line Quantity ...” options:
▪ the item is set up as a variable quantity breakdown item in ITEM
▪ the item has been received on a U-type line in ENRE
▪ the inventory entity is new (that is, it has not been previously received in the 
warehouse)
RFCH screen showing prompt for quantity breakdown
Expiry Date Rules Disable expiry date entry for U-type line
If you select this option, the expiry date entry screen will NOT display in RFCH 
even though manual entry of expiry dates has been activated for the item in 
ITSH.
If you leave this field blank, the expiry date entry screen will display in RFCH if 
manual entry of expiry dates has been activated for the item in ITSH.
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH ONLY (2)
This tab shows additional RFCH options.

MRFP screen showing RFCH Only (2) tab
Enter/Change Hold Code Allow Entry/Change of Hold Code (default value)
Disallow Change of Hold Code. Allow New Hold Code.* 
Disallow Entry/Change of Hold Code*
Skip Hold Code
If you select “Allow Entry/Change of Hold Code“, the RF operator can enter 
new hold codes and change existing hold codes in RFCH. If you select “Disallow Change of Hold Code. Allow New Hold Code.’, the RF operator can enter 
new hold codes but cannot change existing hold codes in RFCH. 
If you select “Disallow Entry/Change of Hold Code”, the RF operator will have 
access to the Hold field in RFCH but cannot change a hold code. If you select 
“Skip Hold Code”, the RF operator will have no access to the Hold field and as 
a consequence will not be able to change the quantity.
* The two non-default options in this field are NOT available when an item hold profile is 
set up in IHOP and attached to an item in ITEM.
FIELD DESCRIPTIONS (RFCH ONLY)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
FIELD DESCRIPTIONS (RFCH ONLY 2)
Validate Item Weight/
Cube Setup
Not Required
Check Weight and Cube
This field allows you to check whether the base SKU of the item being 
received has a weight and cube greater than zero.
If you select “Not Required”, no check will be made of the item’s base SKU 
weight and cube. 
If you select “Check Weight and Cube”, AccellosOne 3PL will perform the 
check. If the item fails the check, the RF operator will be forced to enter the 
missing values in RFCH before receiving the receipt line. RFCH in turn will 
update the missing values in the Quantity Breakdown Block of ITEM.
Extra Charge Entry Type See “Extra Charge Setup for RF” on page 89 for further information.
Concatenate Inventory 
Level in U-Type Line
Only available for U-type lines in which the RF operator selects the receipt 
number from a pick list
Concatenate Level 2 to Beginning of Current Value
Concatenate Level 2 to End of Current Value
If you select either of these two options, a scanned in value such as a date 
code (for example, 101101) will be appended to either the beginning or end of 
the level 2 value. 
For example, office staff create a U-type receipt line in ENRE and enter the 
level 2 value normally. In RFCH the RF operator scans in a value and that 
value is concatenated to the level 2 value entered in ENRE.
Keep First Location Entry 
and Skip the Field
No
Yes
If you select Yes, the RF operator can skip the Location field after his or her 
first entry and put-away the remaining receipt lines in the same location.
Allow Change to Receiving ModeNo
Yes
If you select Yes, the RF operator can switch from one-step put-away to twostep put-away (or vice versa) in RFCH.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Special Receiving Mode 
Types
U Line Receiving, Enter UI, Scan Serial as Inventory Level
RFCH to Gen Stag Loc, RFPU to PnD Loc, Then to Final Loc*
RFCH to Gen Stag Loc, RFPU to PnD Loc, Then to Final Loc
RFCH Overrides*
In this field, you can select a special receiving type mode required for your 
facility. If you leave this field blank, special receiving type modes will be deactivated.
*These two special receiving mode types require special setup. See the section on 
three-step put-away in “Unloading Product in RFCH”.
Validate Inventory Level 
from Bar Code Using 
SCPR Code
Your scan parameter profile code for validating inventory levels in RFCH 
receiving. This code is a default scan parameter code at the customer level. In 
ITEM, you can override your customer default by entering an SCPR code in 
the Scan Parameter Code for Inventory Validation (SCPR) field.
If an invalid inventory level is scanned in RFCH, the RF operator will not be 
allowed to proceed.
Door Rules Door Not Used
Enter/Update Door in RFCH
If you select Door Not Used, the RF operator cannot select or change a door 
assignment. If you select Enter/Update Door in RFCH, the RF operator can 
enter/change a door assignment.
Display Quantity BreakdownNo
Yes
If you select No, the item’s quantity breakdown will be suppressed in RFCH. If 
you select Yes, the item’s quantity breakdown will be displayed in RFCH. 
RFCH showing quantity breakdown displayed
FIELD DESCRIPTIONS (RFCH ONLY 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Put-Away of Multiple Pallets in RFCHNo
Yes
If you select Yes, the RF operator can put-away multiple pallets in a single 
step; that is, the RF operator scans two or more UI’s in RFCH but only enters 
the to location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type
Enter Quantity Breakdown for P-Type LineNo
Yes
Set Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes
If you select No, the item’s quantity breakdown cannot be changed in RFCH. If 
you select Yes, the RF operator can change the quantity breakdown in RFCH; 
that is, override the quantity breakdown entered in ENRE. If you select “Set 
Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes”, the 
item’s quantity breakdown will be automatically set to the line quantity entered 
in RFCH.
The following requirements must be met for the Yes and “Set Quantity Breakdown to Line Quantity ...” options:
▪ the item is set up as a variable quantity breakdown item in ITEM
▪ the item has been received on a P-type line in ENRE
▪ the inventory entity is new (that is, it has not been previously received in the 
warehouse)
FIELD DESCRIPTIONS (RFCH ONLY 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH ONLY (3)
This tab shows additional RFCH options.
RFCH screen showing prompt for quantity breakdown
Update Expiry Date for PType LineNo
Yes
If you select Yes, the RF operator can override the expiry date for P-type lines 
in RFCH. The item shipping profile (ITSH) attached to the item must have 
expiry date entry activated (Enter Expiry Dates = Yes).
RFCH screen showing prompt for expiry date
FIELD DESCRIPTIONS (RFCH ONLY 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MRFP screen showing RFCH Only (3) tab
FIELD DESCRIPTIONS (RFCH ONLY 3)
Capture Photo When 
Unloading First UI
Only available for Intermec CK71 devices
Yes
No
If you select Yes, you can capture images when unloading first UI. If you 
select No, image capture will be deactivated when unloading first UI.
Capture Photo When UI 
is Put On Hold
Only available for Intermec CK71 devices
Yes
No
If you select Yes, you can capture images when placing UI on hold. If you 
select No, image capture will be deactivated when placing UI on hold.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Duplicate Receiving 
Rules if Qty. Entered < 
Qty. Received
Create Second Line With Remainder (1)
Prompt User to Zero Out Second Line (2)
Zero Out Second Line Automatically (3)
In this field, you specify your receiving rules when the quantity entered in 
RFCH is less than the quantity received in ENRE.
EXAMPLE
quantity entered (ENRE) = 100 CS
quantity received (RFCH) = 99 CS
With option 1, AccellosOne 3PL will create a second line with a quantity of 1. 
With option 2, the RF operator will be prompted to zero out the second line. If 
the RF operator selects Yes, the result will be option 3; if the RF operator 
selects No, the result will be option 1.
With option 3, AccellosOne 3PL will automatically create a second line with a 
quantity of 0.
Allow Mixed Pallet for 
Items With Same ILOP
Yes
No
If you select Yes, you can receive mixed pallets in RFCH for items with the 
same ILOP code. If you select No, you cannot receive mixed pallets in RFCH.
Use Repetitive Scan With 
ALIT Starting With Inventory
Level 1
Level 2
Level 3
Level 4
In this field, you can activate grocery style scanning in RFCH. Grocery style 
scanning is used when receiving product such as clothing that does not come 
in a standard pallet/case quantity breakdown and therefore each piece 
received must be individually scanned.
One scan can represent a quantity of one for that item or any other quantity 
that you define. AccellosOne 3PL will calculate the count automatically based 
on the number of pieces scanned and your setup in ALIT.
Sort Sequence Code 
(SOSE)
This sort sequence code allows you to define a custom sort sequence for 
receipt lines in RFCH. When you enter RFCH and key in a receipt number, the 
receipt lines will be sorted according to your SOSE code. If you leave this field 
blank, receipt lines in RFCH will be sorted in receipt line number order.
FIELD DESCRIPTIONS (RFCH ONLY 3)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Receiving Qty. Must be 
Less Than or Equal to 
Item Pallet Qty.
No
Yes
If you set this flag to Yes, the RF operator cannot receive oversized non-standard pallets. For example, if an item's quantity breakdown is 50 cases per pallet and the ENRE quantity for a given receipt line is 1 pallet or 50 cases, the 
RF operator cannot enter a quantity greater than 50 cases. 
EXAMPLES: (quantity breakdown of 50 cases per pallet)
ENRE quantity: 1PLT RESULT: normal processing
RFCH quantity: 1 PLT
ENRE quantity: 1 PLT RESULT: normal processing
RFCH quantity: 2 PLT
ENRE quantity: 1 PLT RESULT: normal processing
RFCH quantity: 50 CS
ENRE quantity: 1 PLT RESULT: receipt quantity rejected
RFCH quantity: 51 CS
ENRE quantity: 1 PLT 30 CS RESULT: normal processing
RFCH quantity: 1 PLT 31 CS
ENRE quantity: 51 CS RESULT: receipt quantity rejected
RFCH quantity: 51 CS
Allow Skipping of Level 
Validation
Only applicable if the Validate Inventory Level from Bar Code Using SCPR 
Code field is activated.
No
Yes
If you set this flag to Yes, the RF operator can continue to receive a receipt 
line in RFCH even if inventory level validation based on SCPR fails.
Special Item Process 
Capture Mode
Capture Item Processes Before Entering Location
If you select this option, the RF operator scans any process values before 
entering a staging location. If you leave this field blank, the RF operator scans 
process values after entering a staging location.
FIELD DESCRIPTIONS (RFCH ONLY 3)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH ONLY (4)
This tab shows additional RFCH options.
MRFP screen showing RFCH Only (4) tab
RFCH SHARED
This tab shows options available in both RFCH and RFPU.
Always Prompt to Enter a 
Staging Location
No
Yes
If you set this flag to No, the display of the suggested staging location in the L: 
field of RFCH will be suppressed and the RF operator will be required to scan 
in the staging location. If you set this flag to Yes, the L: field will be populated 
with the suggested staging location and the RF operator is only required to 
press Enter to accept it.
Zero Out Receipt Lines Not Allowed 
All Users Are Allowed
Supervisors Only Are Allowed
The rules for zeroing out receipt lines in RFCH.
FIELD DESCRIPTIONS (RFCH ONLY 4)
Keep Last Location for 
One-Step Manual PutAway
Yes
No
If you set this flag to Yes, the last location for one-step manual put-away will 
display in RFCH. If you set this flag to No, the Location field in RFCH will 
always be blank when performing one-step manual put-away.
FIELD DESCRIPTIONS (RFCH ONLY 3)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH Shared tab
.
FIELD DESCRIPTIONS (RFCH SHARED)
Show Default Quantity in 
RFCH/RFPU
Yes
No
RFPU Only
Variance Screen Only
If you select Yes, AccellosOne 3PL will display the received quantity of the 
receipt line from ENRE as the default quantity in RFCH/RFPU. You can press 
Enter to confirm it in these programs or you can enter a new quantity.
If you select No, the received quantity from ENRE will not be displayed in 
RFCH/RFPU.
If you select RFPU Only, AccellosOne 3PL will display the received quantity of 
the receipt line from ENRE as the default quantity in RFPU.
If you select Variance Screen Only, AccellosOne 3PL will display the received 
quantity of the receipt line from ENRE only on the Variance screen.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFCH/RFPU Quantity 
Must Match ENRE Quantity
Only available for P-type receipt lines
Must match ENRE (1)
Matching not required (2)
Warn if mismatch with ENRE (3)
No warning if mismatch with ENRE (4)
Receive no more than original lines expected quantity in RFPU (5)
Must match ENRE in RFCH. No more than original line expected quantity 
in RFPU (6)
If you select option 1, the entered quantity in RFCH/RFPU must match the 
expected quantity in ENRE. If the two quantities do not match, the RF operator will not be able to process the receipt line.
If you select option 2, the entered quantity in RFCH/RFPU need NOT match 
the expected quantity in ENRE and a warning message is only generated 
when the received quantity is greater than the expected quantity.
If you select option 3, a warning message will be generated when the entered 
quantity in RFCH/RFPU does not match the expected quantity in ENRE, but 
the RF operator will be allowed to proceed.
If you select option 4, no warning message will be generated when the 
entered quantity in RFCH/RFPU does not match the expected quantity in 
ENRE.
If you select option 5, matching is not required in RFCH. However, the entered 
quantity in RFPU cannot exceed the expected quantity in ENRE.
If you select option 6, the entered quantity in RFCH must match the expected 
quantity in ENRE and the entered quantity in RFPU cannot exceed the 
expected quantity in ENRE.
Supvr. Must Authorize 
Location Overrides in 
RFCH/RFPU/RFRL
Yes
No
blank = No
If you select Yes, RF operators cannot override a system-assigned put-away 
location without the approval of a supervisor. If you select No, RF operators 
can override system-assigned locations without the approval of a supervisor.
NOTE The approval of a supervisor is NOT required to override a putaway location with a staging location.
FIELD DESCRIPTIONS (RFCH SHARED)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Validate One Process 
Value
Only available for P-type receipt lines
RFCH Only
RFPIC Only
RFCH and RFPIC
RFCH Only in Supervr. Override Mode
None
This flag allows the RF operator to validate the serial number and other information such as level 1 and 2 values in bar code labels. Validation will only 
occur for P-type receipt lines when the full quantity is received and all process 
values have been entered or scanned in.
If you set this field to RFCH Only, RFPIC Only or RFCH and RFPIC, the RF 
operator will be prompted to scan in one label from each pallet for validation 
purposes in the appropriate program. Should the label be missing or not valid, 
the RF operator will not be able to complete the receipt in RFCH or the order 
in RFPIC. 
If you set this field to RFCH Only in Supervr. Override Mode, the RF operator 
will be prompted to scan in one label from each pallet for validation purposes 
in RFCH. Should the label be missing or not valid, the RF supervisor login 
screen is displayed. When the supervisor logs in, he or she will be prompted 
to select how long to turn off process value validation: either turn off for just 
that pallet or for all pallets on that receipt or all pallets of that item on that 
receipt. 
RFCH screen showing supervisor options
If you set this flag to None, no validation of the serial number or other information on a bar code label will occur.
FIELD DESCRIPTIONS (RFCH SHARED)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Advance Receipt Header 
When Last Line Confirmed
Yes (default)
No
If you select Yes, the receipt header will be automatically confirmed when the 
last receipt line is confirmed in RFCH/RFPU. If you select No, the receipt 
header will NOT be automatically confirmed when the last receipt line is confirmed in RFCH/RFPU.
The No option allows you to add new receipt lines after all receipt lines on a 
receipt have been confirmed.
Maximum Quantity 
Allowed in RFCH/RFPU
In this field, you specify the maximum quantity for any given receipt line in 
RFCH/RFPU. If you do not enter a number, the maximum quantity allowed in 
RF receiving for a receipt line is 9999.
Put Away Partial Pallet to 
Reserved Area
Yes
No
Yes, With Allowing Over a Pallet as a Full Pallet
If you select No, partial pallet put-away to a reserved area is deactivated and 
normal put-away rules to a non-reserved area apply.
If you select Yes, partial pallet put-away to a reserved area is activated and 
the following logic applies:
▪ if received quantity = zero or null, halt the receiving process and send a 
“SEE SUPERVISOR” message to RF operator
▪ if received quantity = standard quantity breakdown, pallet is deemed to be a 
full pallet
▪ if received quantity < standard quantity breakdown, pallet is deemed to be a 
partial pallet
▪ if received quantity > standard quantity breakdown, halt the receiving process and send a “SEE SUPERVISOR” message to RF operator
If you select Yes With Allowing Over a Pallet as Full Pallet, the same logic as 
Yes will apply with the following exception:
▪ if received quantity > standard quantity breakdown, no message is generated and normal put-away continues
Receipt Confirmation 
Date in RFCH/RFPU
Receipt Date
Actual Company Date
If you select “Receipt Date”, the receipt confirmation date in RFCH/RFPU will 
be the receipt creation date. If you select “Actual Company Date”, the receipt 
confirmation date in RFCH/RFPU will be the receipt confirmation date in 
CHRF.
FIELD DESCRIPTIONS (RFCH SHARED)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPU
This tab shows various RFPU options.
x 
RFPU tab
.
FIELD DESCRIPTIONS (RFPU)
Validation Rules for PutAway to Pick LineStop operator from proceeding
Allow operator to proceed (reserved for future use)
Omit validation of location
If you select “Stop operator from proceeding”, the RF operator will not be able 
to put-away product in RFPU to a pick line location that is not set up for that 
product in PIIT. If you select “Omit validation of location”, the RF operator will 
able to put-away product to any pick line location without restriction.
Allow Put-Away to Staging LocationYes
No
If you select No, the RF operator cannot put-away product to a staging location in RFPU. If you select Yes, the RF operator can perform three-step putaway; that is, put-away product to a staging location in RFPU. When product 
is assigned to a staging location, the receipt’s flow remains at STPU (Start 
Put-Away) and is not advanced to PUCO (Put-Away Complete) until a nonstaging location is eventually entered. 

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Variance Handling Variance screen deactivated
Variance screen no sup. override
Variance screen with sup. override
Variance screen for sup. only
If you select “Variance screen deactivated”, the Variance screen does not display for any user. If you select “Variance screen no sup. override”, the Variance screen displays for all users and no supervisor override is required to 
enter a variance. If you select “Variance screen with sup. override”, the Variance screen displays for all users and a supervisor override is required to 
enter a variance. If you select “Variance screen for sup. only”, the Variance 
screen displays for supervisors only and no supervisor override is required to 
enter a variance. 
NOTE Regardless of the option that you choose, the variance itself is 
always tracked in LORE even if the Variance screen does not display.
Validation Rules for System-Assigned LocationsNo validation for system-assigned locations and overrides allowed
Validation required WHEN system assigns location and overrides 
allowed
Validation required ONLY for system-assigned locations and overrides 
allowed
If you select “No validation”, the RF operator can press Enter in RFPU to 
accept a system-assigned location without the need to re-enter it. If you select 
“Validation required WHEN ...”, the RF operator must re-enter or scan in your 
put-away location in RFPU to confirm it.
If you select “Validation required ONLY ...”, the RF operator must re-enter or 
scan in your put-away location in RFPU to confirm it only when the location is 
assigned a location type in LOTP whose Directed Put-Away flag has been set 
to Yes.
Event-Driven Cycle 
Count Profile (CYCP)
See the Cycle Counting Guide for further information on event-driven cycle 
counts.
Allow Quantity to be 
Updated
No
Yes
If you select Yes, the RF operator can enter or modify the quantity of a receipt 
line in RFPU. If you select No, the cursor will skip over the Qty field and the 
quantity cannot be entered or modified.
FIELD DESCRIPTIONS (RFPU)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Enter/Change Hold Code Allow Entry/Change of Hold Code
Disallow Change of Hold Code. Allow New Hold Code
Disallow Entry/Change of Hold Code
f you select “Allow Entry/Change of Hold Code“, the RF operator can enter 
new hold codes and change existing hold codes in RFCPU. If you select “Disallow Change of Hold Code. Allow New Hold Code.’, the RF operator can 
enter new hold codes but cannot change existing hold codes in RFPU. If you 
select “Disallow Entry/Change of Hold Code”, the RF operator will have no 
access to the hold code field in RFPU.
Maximum Number of F3 
(NX) Allowed Per ILOP 
Sequence
In this field, you specify the maximum number of times that the RF operator 
can press F3 (NX) in RFPU to display a suggested put-away location.
Allow Put-Away of Multiple Pallets in RFPUNo
Yes*
If you select Yes, the RF operator can put-away multiple pallets in a single 
step; that is, the RF operator scans two or more UI’s but only enters the to 
location once. If you select No, the RF operator must put-away each pallet 
individually.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type
* Does not support directed put-away. That is, only the flows INST and STPU can have 
the Assign Location flag set to Yes.
FIELD DESCRIPTIONS (RFPU)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC
This tab show various RFPIC/RFPK options.
Allow Receiving of Multiple Lines TogetherDisallow Receiving Multiple Lines Together
Allow Receiving of Multiple Lines Together
If you select “Allow Receiving of Multiple Lines Together”, the RF operator can 
put-away multiple receipt lines in a single step if the following conditions are 
met:
▪ all lines have the same UI
▪ all lines are in the same location with the same hold code (if any)
▪ all items have three or four inventory levels
▪ the quantity entered is the total quantity and it is entered in the lowest SKU
NOTE If you used Directed Move Inbound to assign locations and the pallet has mixed items, the ILOP profile from the item with the largest quantity in 
the pallet is used to produce a to location.
Change of Warehouse 
Rules
Confirmation Required
Allow Change of Warehouse Code, No Confirmation Required
Do Not Allow Change of Warehouse Code
If you select “Conformation Required”, the RF operator will be prompted to 
confirm the change in warehouse code. If you select “Allow Change of Warehouse Code, No Confirmation Required”, the RF operator will not be prompted 
to confirm the change in warehouse code. If you select “Do Not Allow Change 
of Warehouse Code”, the RF operator will not be able to change the warehouse code.
Confirm Receipt Line for 
Opportunistic Cross-Dock 
in RFPU
No
Yes*
If you select No, a receipt line put-away to a cross-dock location must be manually confirmed in CHRF. If you select Yes, a receipt line put-away to a crossdock location will be automatically confirmed when the RF operator completes 
the put-away in RFPU.
FIELD DESCRIPTIONS (RFPU)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC tab
.
FIELD DESCRIPTIONS (RFPIC)
Default Mode Only Case Picking
Only Pallet Picking
Case Picking
Pallet Picking
If you select “Only Case Picking”, the RF operator cannot select pallet or normal mode (NM) in RFPIC. If you select “Only Pallet Picking”, the RF operator 
cannot select case pick mode (CP) in RFPIC (unless he or she is picking from 
a pick line location). If you select “Pallet Picking”, the RF operator will be 
prompted to confirm pallet or normal mode (NM) as the default picking mode 
in RFPIC. If you select “Case Picking (CP)”, the RF operator will be prompted 
to confirm case pick mode as the default picking mode in RFPIC. 
Once the RF operator selects a mode in RFPIC, that mode remains in effect 
for all orders until the RF operator exits RFPIC or changes his or her mode by 
pressing F2.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
If the RF operator is picking from a pick line location, the mode is automatically set to Case Picking regardless of the option that the RF operator selects 
in this field.
Allow Loading Before 
Completion of Picking 
Process
Yes
No
If you select Yes, the RF operator can start loading in OLOP before picking all 
product on the order in RFPI/RFPIC. If you select No, the RF operator must 
pick all product on the order in RFPI/RFPIC before loading in OLOP.
Duplicate Pallet Label 
Rules
Allow Duplicate Pallet ID’s (1)
Disallow Duplicate Pallet ID’s (2)
Operator Decision in all Orders (3)
Disallow Duplicate Pallet ID’s in Open Orders (4)
Operator Decision in Open Orders (5)
Allow Duplicate Pallet ID’s in Its Own Order Only (6)
If you select 1, duplicate pallet ID’s will be allowed without restriction. If you 
select 2, duplicate pallet ID’s will never be allowed. 
If you select 3, the RF operator will be prompted to accept or reject a duplicate 
pallet ID for all orders. If you select 4, duplicate pallet ID’s will not be allowed 
in open orders. If you select 5, RF operator will be prompted to accept or 
reject a duplicate pallet ID for open orders only. If you select 6, duplicate pallet 
ID’s will be allowed only within an individual order.
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Partial Picking in 
Normal Mode
Allow all, no restriction (1)
Allow last remaining partial inventory and full pallets (2)
Allow full pallets only (3)
Allow PALL pick method only (4)
This flag governs which order lines appear in the RFPIC pick list when working in normal mode.
If you select 1, all order lines regardless of pick quantity appear in the RFPIC 
pick list. If you select 2, only full pallet picks and partial quantities representing 
the last remaining inventory in a location appear in the RFPIC pick list.
If you select 3, only full pallet picks appear in the RFPIC pick list. The RF operator must switch to case pick mode to pick partial order lines.
A partial quantity is defined as 60% or more of the total quantity in the location. For example, if there are 50 cases in a location and you need to pick 30, 
you can scan in the 20 cases to be removed rather than the 30 cases to be 
picked. This option is designed to save time by reducing the number of cases 
scanned.
If you select 4, only full pallet picks generated by the Wave Manager appear in 
the RFPIC pick list.
Assign PID on Full Pallets 
or Last Inventory
In NM Mode (1)
No (2)
In CP Mode as the first pick (3)
RFPIC CP Mode Full Pallet (INVT QTY Break) or RFITLV PALL Pick 
Method (4)
If you select 1, the lowest level or pallet ID will be added to the Process Block 
of the order under the code CP for case pick when picking full pallets or picking the last entity in a location in normal mode.
If you select 2, the lowest level or pallet ID will NOT be added to the Process 
Block of the order under the code CP for case pick.
If you select 3, the lowest level or pallet ID will be added to the Process Block 
of the order under the code CP for case pick after the first pick in case pick 
mode.
If you select 4, the lowest level or pallet ID will be added to the Process Block 
of the order under the code CP for case pick when picking full pallets based 
on the item’s standard quantity breakdown while in case pick mode in RFPIC.
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Number of Days for Label 
Validation
The “value greater than zero” option requires a custom label from HighJump.
If you enter a value greater than zero in this field, AccellosOne 3PL will validate a case’s date in RFPIC. Should the Number of Days for Label Validation 
value be less than the order to arrive date minus the date embedded in the 
case's bar code label, the message “Too old for order” will display and you will 
not be able to pick the case. 
If you enter zero or leave this field blank, the RF operator can scan in the 
cases to be removed from a full pallet rather than the cases to be picked when 
picking a partial quantity. 
Allow Suspended Holds Split Order Line, No Suspended Hold
If you select “Split Order Line, No Suspended Hold” and place product on hold 
in RFPIC, the order line will be split but no suspended hold will be placed on 
the product that is not picked and the new order line can be picked at any 
time. With this option, the F3 (HD) command in RFPIC is not available. 
Allow Suspended Holds
Only Allow if Supervisor Approved
If you select “Allow Suspended Holds”, non-supervisory operators can place 
product on suspended hold in RFPIC. If you select “Only allow if Supervisor 
approved”, the following rules will apply:
▪ non-supervisory operators can place product on suspended hold in RFPIC if 
approved by a supervisor (HD command)
▪ a partial pick will require the approval of a supervisor
With both these options, the order line will be split into two: line 1 will contain 
the pick quantity and line 2 will contain the remaining quantity that could not 
be picked. Line 2 will be placed on suspended hold and AccellosOne 3PL will 
attempt to reallocate the line 2 quantity.
Split Order Line, Allow Suspended Hold
Split Order Line, Supervisor Approved
If you select option “Split Order Line, Allow Suspended Hold”, non-supervisory 
operators can place product on suspended hold in RFPIC. If you select “Split 
Order Line, Supervisor approved”, the following rules will apply:
▪ non-supervisory operators can place product on suspended hold in RFPIC if 
approved by a supervisor (HD command)
▪ a partial pick will NOT require the approval of a supervisor
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
With both these options, the order line will be split into two: line 1 will contain 
the pick quantity and line 2 will contain the remaining quantity that could not 
be picked. Line 2 will NOT be placed on suspended hold and AccellosOne 
3PL will NOT attempt to reallocate the line 2 quantity.
NOTE The option that you select in this field can be overridden at the item 
level in the program MIRP (Item RF Profile Code) by selecting a different 
option for a given item.
Disallow Process Value 
Scanning
Yes
No
If you select Yes, the RF operator cannot scan process values in RFPIC. 
Instead, he/she must scan these values in RFOPS. If you select No, the RF 
operator can scan process values in either program.
Allow Picking Outside 
Pick Line
Yes
No
This flag allows you to pick pick line product from a non-pick line location such 
as bulk or rack when multiple replenishments for the same product cause 
overcrowding in your pick line. This choice is available when the full order 
quantity is not available in the pick line location and a replenishment has been 
generated.
For example, suppose your order quantity is 10 cases, there are only five 
cases in the pick line and the replenishment quantity is 60 cases. The RF 
operator can choose to pick the 10 cases from a bulk or non-pick line location 
instead of waiting for a replenishment and picking from the pick line. The 10 
cases picked from bulk is subtracted from the replenishment quantity; 60 -10 = 
50. 
If you select Yes, pick line picking from a non-pick line location is activated. If 
you select No, pick line picking from a non-pick line location is not allowed.
Replenishment Rules for 
Pick Line
REPI done inside of RFPIC
REPI done separately (default)
Determined by the user
If you select “REPI is done inside of RFPIC”, the RF operator can perform 
replenishments in RFPIC. If you select “REPI is done separately”, the RF 
operator can only perform replenishments in RFRP or RFPL. If you select 
“Determined by the user”, each time that the RF operator logs in, he/she will 
be prompted to select a replenishment mode.
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Display Original Order 
Number/Quantity for Consolidated Picks
Only available for consolidated picking after consolidating your orders in COPI 
(Consolidated Picking)
No Display
Display at UI Field
If you select No Display, the original order number and quantity will not be displayed when the RF operator selects a consolidated line. If you select Display 
at UI Field, RFPIC will display the original order number, quantity and SKU in 
a pop-up window after the RF operator selects the UI value.
RFPIC screen showing display of original order number and 
quantity
Display Pallet Screen Do not display
Display before Picking
Display on completion of Picking
Display after RFSC
If you select “Do not display”, the Pallet Block will not display in RFPIC and the 
RF operator will not be able to ship, receive or exchange pallets in this program. If you select “Display before Picking”, the Pallet Block will display before 
picking in RFPIC. If you select “Display on Completion of Picking”, the Pallet 
Block will display after picking in RFPIC.
If you select “Display after RFSC”, the Pallet Block will display after performing 
manual cartonization in RFSC.
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC (2)
This tab shows additional RFPIC/RFPK options.
RFPIC (2) tab
RFPIC screen showing Pallet Block
FIELD DESCRIPTIONS (RFPIC)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
.
FIELD DESCRIPTIONS (RFPIC 2)
Activate Inventory Count Always
Never
If Quantity Reaches or Falls Below Threshold Quantity
Every 2nd / 3rd / 4th / 5th / 6th / 7th / 8th / 9th Line
CP mode options
If you select “Always”, the RF operator will be required to enter an inventory 
count for each pick location in RFPIC. If you select “Never”, inventory counting 
in RFPIC will be deactivated. If you select “If Quantity Reaches or Falls Below 
Threshold Quantity”, a count will be required only if the on-hand quantity 
reaches or falls below the threshold quantity. 
If you select one of the line options (every 2nd, 3rd, 4th, etc. line), a count will 
be required only for every 2nd, 3rd, 4th, etc. pick.
Inventory Count Rules Only available if Activate Inventory Count is set to a value other than Never
These rules govern what happens in RFPIC when the inventory count for the 
location that is entered by the RF operator does not match the on hand system quantity.
Ignore investigations
No record will be created in ICIN (Inventory Count Investigation) and the RF 
operator can pick the order line.
Supervisor must override
The RF operator cannot pick an order line unless a supervisor logs in and 
either accepts or rejects the discrepancy. If the supervisor accepts the discrepancy, no record will be created in ICIN (Inventory Count Investigation). If 
the supervisor rejects the discrepancy, a record is created in ICIN.
Flow advancement not allowed
Super. override/No flow adv.
Reserved for future use.
Threshold Quantity to Initiate CountOnly available if you select If Quantity Reaches or Falls Below Threshold 
Quantity in the Activate Inventory Count / Hold field
Your threshold quantity for initiating an inventory count.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Automatically Assign Pallet IDYes
No
Use SSCC-18 Pallet Sequence Number
If you select Yes, a unique pallet ID will be generated in RFPIC while in CP 
(case pick) mode and the cursor will automatically advance to the Printer field. 
The system-generated pallet ID cannot be changed by the RF operator. 
If you select No, the RF operator has two choices when prompted for a pallet 
ID in RFPIC while in case pick mode: 
▪ he or she can press Enter to have AccellosOne 3PL generate a unique pallet ID
▪ he or she can enter or scan in a pallet ID not generated in AccellosOne 3PL.
The Yes option requires a label document in either the Label Document or 
Quick Response Label Document fields. If all your consignees use quick 
response labels, a label document is not required in the Label Document for 
RF Picking field. If some consignees use quick response labels while others 
do not, you must enter a label document in both fields. 
If you do not use quick response labels, a label document is not required in 
the Quick Response Label Document field.
If you select Use SSCC-18 Pallet Sequence Number, the unique pallet ID generated in RFPIC will be a valid SSCC-18 pallet sequence number.
Label Document Only available if Automatically Assign Pallet ID = Yes
If you enter a label document in this field, the Label field in RFPIC when working in CP (case pick) mode will be populated with the label document number. 
If you set up a detail record in DOCU for this document specifying both the 
printer and operator, the Printer field in RFPIC will be populated with the RF 
operator’s printer. 
Quick Response Label 
Document
Only available if Automatically Assign Pallet ID = Yes
If you enter a label document in this field, the Label field in RFPIC when working in CP (case pick) mode will be populated with the quick response number. 
If you set up a detail record in DOCU for this document specifying both the 
printer and operator, the Printer field in RFPIC will be populated with the RF 
operator’s printer. 
FIELD DESCRIPTIONS (RFPIC 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Sort Sequence Code 
(SOSE)
Optional
The sort sequence code used to sequence or “snake” the pick list of picking 
tasks in RFPIC. You can apply these advanced SQL statements to either item 
codes, location codes or inventory entities.
When you activate sort sequencing, the RF operator can initially pick any item, 
location or inventory entity from the sorted list, but once this initial choice is 
made the RF operator must finish picking the item, location or inventory entity 
in RFPIC before proceeding to another item, location or inventory entity. 
For example, suppose you set up a sort sequence based on item and there 
are three different items on a given order: item A, item B and item C. When the 
RF operator enters RFPIC and selects any item on the order — say item B — 
he or she must pick all order lines containing item B before picking another 
item. The same logic applies to the remaining items on the order; once a given 
item is selected, all order lines containing that item must be picked before proceeding to another item.
Pick list in RFPIC shown in location code sequence (A107, A107, B102)
NOTE The table name (c_invt, e_ord_d5d1 or m_loc) is required in your 
SQL statement.
If you do not specify a sort sequence code, picking tasks in the pick list will be 
sequenced in location code sequence.
FIELD DESCRIPTIONS (RFPIC 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Sort Sequence Based on Item
Location
Inventory Entity
The value that the sort sequence is based on.
Event-Driven Cycle 
Count Profile (CYCP)
See the Cycle Counting Guide for further information on event-driven cycle 
counts.
Enter Outbound Pallet ID 
Before Picking
Only available for case pick mode in RFPIC/RFITLV
No
Yes
If you select No, the RF operator must enter label parameters after picking his/
her order line(s). If you select Yes, the RF operator must enter label parameters before picking his/her order lines.
FIELD DESCRIPTIONS (RFPIC 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Generation of Outbound 
Pallet ID Label
Not Required (1)
OPID Generated by System - Validation Required (2)
OPID Generated by System - No Validation (3)
OPID Generated by Users - No Validation (4)
OPID Generated by Users - Validation Required (5)
OPID generated by System - Hide Partial OPID, Print & Validate before 
Staging (6)
After printing, OPID generated by the User (7)
In this field, you set your label printing options for the outbound pallet ID label 
in RFPIC and RFPK. 
If you select 1, no label will print and the PRT field will be bypassed. 
If you select 2, the RF operator must press Enter in the L(abel) field to generate an AccellosOne 3PL OPID. Then he/she scans in this OPID to validate it. 
If you select 3, the RF operator must press Enter in the L(abel) field to generate an AccellosOne 3PL OPID, but does not perform a scan to validate it. 
If you select 4, the RF operator must manually enter or scan in your own nonAccellosOne 3PL OPID. If you select 5, the RF operator must manually enter 
or scan in your own non-AccellosOne 3PL OPID twice.
If you select 6, the RF operator must manually enter or scan in your own nonAccellosOne 3PL OPID. After printing the label, the RF operator must scan 
the printed label to ensure that its OPID matches the original OPID in the 
L(abel) field.
Option 7 is custom.
Extra Charge Entry Type See “Extra Charge Setup for RF” on page 89 for further information.
FIELD DESCRIPTIONS (RFPIC 2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC (3)
This tab shows additional RFPIC/RFPK options.
REPIC (3) tab
FIELD DESCRIPTIONS RFPIC (3) 
Display Rules for Location/UI/QuantityDisplay Location/UI When Picking from Pick Line
Display Location/UI for All Locations
Display and Bypass Location/Qty in NM Mode
Display and Bypass UI (non-reserve)
Display and Bypass UI When Picking from Pick Line
Skip Location-From and Go to UI; Show Line Qty and Skip Qty field in 
NM Mode
Depending on the option that you choose, you can speed up picking by eliminating certain key strokes and validations in RFPIC.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Separate Hazmat by Item 
in Each Pick
No
Yes
If you define segregation rules for hazardous product in IHZV (Item Hazardous Material Validation) and set this flag to Yes, your segregation rules will 
apply to RFPIC and RFMG. If you set this flag to No, any segregation rules 
defined in IHZV will be ignored in RFPIC and RFMG.
Warehouse/Location for 
Kit Lines
Reserved for future use.
Rules for Picking by Item/
UPC
Validate Item/UPC for All Locations (1)
Validate Item/UPC in Pick Line Locations (2)
No (3)
If you select option 1 or 2, the UPC code scanned by the operator will be 
checked against the UPC code set up in ALIT. If the inventory levels linked to 
the UPC code in ALIT match the inventory levels of the pick order line, the 
pick will be accepted as valid. If, on the other hand, the inventory levels linked 
to the UPC code in ALIT do NOT match the inventory levels of the pick order 
line, the pick will be rejected. 
Option 1 performs the validation for all locations, while option 2 performs the 
validation for pick line locations only.
If you select option 3, no validation of the level 2/3/4 values in ALIT will occur. 
For one-level accounts only, the operator can scan in either the item code 
(level 1) or the UPC code. 
Capture OPID Cube and 
Dimension
For custom use only
In RF Pick
In RF Sorting
If you select In RF Pick, the RF operator can capture in RFPIC the cubic 
dimensions in meters and the gross weight in kilograms for each carton/pallet. 
If you select In RF Sorting, the RF operator can capture in RFSC the cubic 
dimensions in meters and the gross weight in kilograms for each carton/pallet.
If you leave this field blank, the capture of cubic dimensions and gross weight 
will be deactivated in RFPIC and RFSC.
Disable Last Label Scan 
in RFPK
Reserved for future use.
FIELD DESCRIPTIONS RFPIC (3) 

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Use Bookmark in Picklist Yes option not available if Sort Sequence Code (SOSE) field populated
No
Yes
If you select Yes, the first order line in the picklist selected by the RF operator 
will be bookmarked. When the RF operator finishes picking that line and 
returns to the pick list, the pick list will display the next order line after the 
bookmark rather than the first order line in the pick list.
Allow Case Pick While in 
CART Mode in RFPK
No
Yes
If you select Yes, pick method 7 (Less Than Full Pallet) will be activated in 
RFPK. 
Allow Reusable Cartons 
in RFPK
Reserved for future use.
Supervisor Override 
Required for BATP in 
RFPK
Override Required for Reduce Order Qty Only
Override Required for Short of Inventory Only
Override Required for Both Reduce Order Qty and Short of Inventory
Override Not Required for Exceptions
In this field, you specify under which circumstances a supervisor override is 
required when the RF operator is wave picking in RFPK in batch label pick 
mode. 
If you select “Override Required for Reduce Order Qty Only”, a supervisor 
override is required when the RF operator reduces the order quantity. For 
example, the order quantity is 10 eaches, there are 10 eaches in the location 
and RF operator picks five eaches.
If you select “Override Required for Short of Inventory Only”, a supervisor 
override is required when the RF operator shorts an order line. For example, 
the order quantity is 10 eaches, there are 10 eaches in the location but five 
are damaged. The RF operator picks five eaches and shorts the remaining 
five.
If you select “Not Required for Exceptions”, the RF operator can reduce the 
order quantity and/or short an order line without a supervisor override.
FIELD DESCRIPTIONS RFPIC (3) 

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC (4)
This tab shows additional RFPIC/RFPK options.
MRFP (RF Profile Code) screen showing RFPIC (4) tab
Automatically Confirm 
Order After Last Pick
No
Yes
If you select Yes, the order will be automatically confirmed when the RF operator picks the last line. If you select No, the order must be manually confirmed 
in CHOF.
NOTE The Yes option does not allow any flows between FIPI (Finish Picking) and COOR (Confirm Order).
Enter Pallet Type No
Yes
If you select Yes, the RF operator must enter a valid pallet type defined in 
PALL in RFPIC. If you specify a pallet code for a consignee in the Pallet Code 
field in CONS, RFPICK will validate that any pallet code entered during order 
picking for that consignee will match the consignee's pallet code. 
FIELD DESCRIPTIONS RFPIC (3) 

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
FIELD DESCRIPTIONS RFPIC (4)
Allow Relocation if Allocated Product BlockedNo
Yes
If you select Yes, RFRL (RF Relocate) will display whenever the RF operator 
enters an “invalid UI”; that is, the UI is in the correct location, but is not allocated to the order. If you select No, an error message will display whenever 
the RF operator enters an “invalid UI” and RFRL will not be available.
The purpose of this flag is to make it possible to move product when it is 
directly in front of and therefore blocking product allocated to an order. 
Display and Pick SKU Display and PIck in Lowest SKU
Display in Order Line SKU, Pick in Lowest
If you select “Display and Pick in Lowest SKU”, pick quantities will always display in the lowest SKU even if this SKU differs from the SKU quantity in 
ENOR. Likewise, the pick SKU entered by the RF operator will always be the 
item’s lowest SKU.
If you select “Display in Order Line SKU, Pick in Lowest”, the display SKU will 
be that of the order line in ENOR while the pick SKU entered by the RF operator must be the item’s lowest SKU.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Pick of Multiple 
OPID’s in RFPIC
No
Yes
Yes Plus Unconsolidated COPI Orders Only With Full Pallet Pick in NM 
Mode
If you select Yes, the RF operator in RF picking programs can pick multiple 
OPID’s and deliver them to a staging location in a single step. The following 
restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type
If you select No, the RF operator is restricted to a single OPID per pick. 
Display Rules for Default 
Staging Location
Last Staging Location in Previous Pick, Scan not Required
Display Last Staging Location from Order, Scan Required
Display Last Order Staging Location and Load Staging Location, Scan 
Required
Display Last Staging Location from Order, Scan not Required
Do Not Display Staging Location in Normal Mode
In this field, you specify your display and scanning rules for the default staging 
location.
Picking Methods for PnD 
Location
Full Pallet Only
All Pick Modes
The pick mode(s) allowed for PnD locations.
Display Order of Items 
and Descriptions in Pick 
List
Item, Description
Description, Item
The display order of items/descriptions in the RFPIC pick list.
Display Pick Quantity in 
Higher UOM
No
Yes
If you select Yes, the pick quantity will display in the highest UOM or SKU type 
(usually PLT).
FIELD DESCRIPTIONS RFPIC (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Validate OPID Using 
MSVS Code
If you set up a special verifier SQL record in MSVS, you can perform custom 
validation of your OPID’s.
Capture Pallet Spots For custom use only.
Scan From Location in 
RFPIC
No
Yes
If you select No, the From Location field is automatically populated by AccellosOne 3PL and no scan by the operator is required. If you select Yes, the 
from location must be scanned by the operator for each pick.
Apply Mask to UI in 
RFPIC
Left 01 to Left 25
Right 01 to Right 25
You can mask up to 25 characters of the UI from either the left or the right to 
prevent RF operators from cheating by typing in rather than scanning the UI.
FIELD DESCRIPTIONS RFPIC (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Inventory Count Investigation TypeInvestigation for Every Picked Unconfirmed Order and OPID
If you select “Investigation for Every Picked Unconfirmed Order and OPID”, an 
ICIN record will be created for all on order inventory in the warehouse whose 
inventory levels match the inventory levels of a single picked pallet with a 
countback variance.
If you leave this field blank, an ICIN record will be created for the current pallet 
being picked only should that pallet have a variance during an RFPIC countback. All other pallets for unconfirmed orders containing the same inventory 
will NOT be assigned an ICIN record.
When a supervisor logs into RFPIC to investigate a variance, the following 
screen will appear:
If the supervisor enters Y for Resolved, no ICIN record will be created for the 
current pallet being picked if there is a variance. However, ICIN records will be 
created for all other pallets on open orders whose first three inventory levels 
match the inventory levels of the current pallet.
When selecting the resolved option, the supervisor will be prompted to confirm 
the quantity. If the supervisor quantity matches the system quantity, no ICIN 
record is created. If the supervisor quantity does not match the system quantity, one of the following will occur: 
▪ if the quantity entered is less than the system quantity, the difference will be 
placed on SUSP hold and the required number of ICIN records will be generated 
▪ if the quantity entered is greater than the system quantity, the prompt “Move 
excess to designated location with label” will display and the required number of ICIN records will be generated
FIELD DESCRIPTIONS RFPIC (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RFPIC (5)
This tab shows additional RFPIC/RFPK options
RFPIC (5) tab
If the supervisor enters N for Not Resolved, no ICIN records will be created 
and the RF operator will be prompted to re-pick the order line.
FIELD DESCRIPTIONS RFPIC (5)
Inventory Count Display 
Type
Ignore Count When Outbound Qty = Inbound Qty = Item Setup Qty
If you select this option, no inventory counts will be required when the standard quantity breakdown (say, 50 cases per pallet) is the same as both the 
inbound quantity and the outbound quantity. That is, a full pallet was received 
and is now being shipped in its entirety.
For variable quantity breakdown product, no inventory counts will be required 
if the outbound quantity breakdown matches the inbound quantity breakdown.
FIELD DESCRIPTIONS RFPIC (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Use Tie/Hi/Loose to Calculate Inventory Count 
Quantity
No
Yes
If you select No, the RF operator must enter the total quantity of product in a 
location when performing a count back. If you select Yes, the RF operator will 
be prompted to enter the tie, hi and loose quantities; AccellosOne 3PL will 
then calculate the total quantity.
Inventory Count for Pallet Pick in RFITLVNo
Yes
If you select No, count backs will be deactivated for full pallet picks in RFITLV. 
If you select Yes, count backs for full pallet picks will be generated according 
to normal count back rules.
Pick Mode in RFITLV Use Pick List
One Task at a Time
If you select Use Pick List, the normal pick list will display and the RF operator 
can choose the task that he or she wishes to work on. If you select “One Task 
at a Time, the RF operator will see a single task in the pick list and will not be 
able to select a specific task from a list or skip a task.
Validate Item and Other 
Levels Special Mode
Read Qty From Bar Code, Validate Item/Lot if exists in the bar code by 
BAPR setting (1)
Validate Item After Location Field (2)
If you select 1, you can extract the quantity from a GS1 bar code and validate 
levels 1/2 against the scanned bar code. If the pick quantity is manually 
entered rather than scanned from the bar code and does not match the order 
line quantity, an error message is displayed and supervisor approval is 
required to complete the pick.
RFPIC screen showing incorrect quantity message
If you select 2, validation of levels 1/2 against the scanned bar code occurs 
after the RF operator has entered the to location.
FIELD DESCRIPTIONS RFPIC (5)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MISCELLANEOUS
This tab shows various miscellaneous options.
Pick Background Substitution RulesReserved for future use.
Location Validation in 
RFPK - CART Pick
No
Yes
If you select No, a location scan of the pick location will NOT be required in 
RFPK while working in cart pick mode. If you select Yes, a location scan of the 
pick location will be required in RFPK while working in cart pick mode.
Override SystemAssigned OPIDAllow
Disallow
Warning
If you select Allow, the RF operator can override the assigned OPID by typing/
scanning over. If you select Disallow, the OPID field is protected and cannot 
be changed. If you select Warning, a warning is presented: "OPID has been 
changed. Y = Continue. No = Reverse the Value". "Yes" allows the change; 
"No" cancels the change and leaves the original OPID.
RFPIC screen showing “Update not Allowed” message
RFPIC screen showing “OPID has been changed” message
FIELD DESCRIPTIONS RFPIC (5)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Miscellaneous tab
FIELD DESCRIPTIONS MISCELLANEOUS
Display Order Lines by 
Item/Location in RFPI
Item
Location
If you select Item, order lines will be sorted in item code order in RFPI. If you 
select Location, order lines will be sorted in location code order.
Picklist Rules in RF RelocatePicklist and validation
Picklist. No validation (default)
No picklist. Must validate
If you select “Picklist and validation”, the RF operator can select the from location from a picklist and must scan in the from location to validate. If you select 
“Picklist. No validation”, the RF operator can select the from location from a 
picklist, but does not scan in the from location. If you select “No picklist. Must 
validate”, the RF operator cannot select the from location from a picklist, but 
must scan in the from location to validate.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Validation Rules for Relocate to Pick LineStop operator from proceeding
Allow operator to proceed
Omit validation of location
If you select “Stop operator from proceeding”, the RF operator will not be able 
to put-away product in RFPU to a pick line location that is not set up for that 
product in PIIT. If you select “Allow operator to proceed”, a warning message 
will display when the RF operator attempts to put-away product to a pick line 
location not set up for the product. However, the RF operator can bypass the 
warning message by pressing F3 to process. If you select “Omit validation of 
location”, the RF operator will be able to put-away product to any pick line 
location without restriction.
Validate Level Number in 
Physical
Optional
Refer to the Physical Inventory Guide.
Validate Quantity in Order 
Move
Yes
No
If you set this flag to Yes, the RF operator must enter the quantity being 
moved when relocating product in RFST. The quantity being moved is the 
number of cases/eaches or other SKU that has been assigned to an outbound 
pallet ID in RFPIC. If you set this flag to No, the quantity being moved is not 
entered when relocating product in RFST.
Validate From Location in 
Order Move
Yes
No
If you set this flag to Yes, the RF operator must enter the from location when 
relocating product in RFST. If you set this flag to No, the from location is not 
required.
Location Type of To Location in Order MoveAny Location
Staging Location Only
Pick Location Only
Staging Location Excluding Door Location
The required location type of your to location when relocating product in 
RFST.
FIELD DESCRIPTIONS MISCELLANEOUS

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MISCELLANEOUS (2)
This tab shows additional miscellaneous options.
Allow Directed Move in 
RF Relocate
Yes
No
If you set this flag to Yes, the RF operator can perform directed moves in 
RFRL. AccellosOne 3PL will select the best possible to location for a relocation based on your directed move stock parameters set up in ILOP. If you set 
this flag to No, the RF operator cannot perform directed moves in RFRL.
Display From Relocation 
Quantity in RF Relocate
Yes
No
If you select Yes, AccellosOne 3PL will display the from relocation quantity in 
the QTY field in RFRL and position the cursor in the LOC TO field. The RF 
operator can either proceed to relocate all product in the location or can press 
F9 and change the quantity. 
The from relocation quantity will be displayed in “cooked” format; that is, 1 pallet/25 cases instead of 125 cases or 5 cases/10 eaches instead of 110 
eaches. This option is designed for facilities where relocating all inventory in a 
location is the rule rather than the exception.
The following conditions must be met before the from relocation quantity will 
display:
▪ all product in a given location belongs to the same inventory entity
▪ the quantity contains more than one SKU type; for example, there are two 
pallets, 20 cases in a location or 30 cases plus 10 eaches in a location. 
If you select No, the from relocation quantity will not be displayed in RFRL.
Allow RFCY Supervisor 
Count
Reserved for future use.
Print Inventory Access/
REPI Quantity Label
Reserved for future use.
Document Code for 
Quantity Labels
This field allows you to specify a document code for replenishment labels. A 
custom document from HighJump is required.
FIELD DESCRIPTIONS MISCELLANEOUS

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Miscellaneous (2) tab
FIELD DESCRIPTIONS MISCELLANEOUS (2)
Use Pick Ticket Instead 
of RF Pick
Yes
No
If you select Yes, RF operators picking in RFPK will not have access to order 
lines assigned to either the CART or EACH pick method. These order lines 
must be picked manually outside of RFPK.
If you select No, RF operators picking in RFPK will enjoy full access to all 
order lines regardless of pick method.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Rules for Uniqueness of 
Serial Number
Per Document
Per Item for a Document
Per Entity for a Document
blank
This field allows you to define how AccellosOne 3PL checks for duplicates in 
the following RF programs: RFIPS and RFOPS.
If you select Per Document, no duplicate serial numbers will be allowed within 
the same receipt/order. If you select Per Item for a Document, no duplicate 
serial numbers within will be allowed for the same item on a single receipt/
order. If you select Per Entity for a Document, no duplicate serial numbers will 
be allowed within the same inventory entity on a single receipt/order. If you 
leave this field blank, duplicate serial numbers will be allowed without restriction.
If the MRFP rule is violated, the RF operator will not be allowed to proceed.
Allow Merging Orders/
Items to One OPID Within 
Load (RFMG)
See “Merging OPID’s in RFMG” on page 309
Allow Merging Up To 
Level (RFMG)
Level 1
Level 2
Level 3
You can merge inventory entities at inventory levels other than the lowest. For 
example, suppose you select Level 1 and merge two pallets with different lot 
numbers and pallet ID's. The adjusted out lot number and pallet ID will be lost 
and the adjusted in lot number and pallet ID quantity will be adjusted accordingly.
Refresh Screen After 
Each Relocation (RFRL)
Yes
No
If you select Yes, a blank RFRL screen will display for the RF operator after 
each relocation. If you select No, RFRL will not refresh after each relocation.
Confirm OPID for Pick 
Method in RFCO 
CART
If you select CART, order lines assigned the pick method of CART can have 
their OPID’s confirmed in RFCO. If you leave this field blank, order lines 
assigned the pick method of CART can only be confirmed in CHOF (that is, 
they cannot be confirmed in RFCO).
FIELD DESCRIPTIONS MISCELLANEOUS (2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
RF Relocation Executed 
by
Scan Location to Execute Relocation
UI Scan Only
Scan Location to Execute Relocation; UI Scan Only
In this field, you select how you want to execute a relocation. If you select 
“Scan Location to Execute Relocation”, the RF operator must scan the from 
location to execute the relocation and pressing F3 (Process) is not required. If 
you select “UI Scan Only” in this field, the RF operator must scan the UI to 
execute the relocation. If you select “Scan Location to Execute Relocation; UI 
Scan Only”, the RF operator must scan both the from location and the UI to 
execute the relocation.
Allow Mixed Pallet Allow Relocation of Mixed Pallets in RFRL
If you select this option, you can relocate a mixed pallet (multiple items, lots, 
date codes, etc.) in a single relocate action. A pallet license relocate will move 
all inventory records associated with the pallet. 
Show RF Confirm OPID 
Summary
Yes
No
If you select Yes, a pop-up screen displays in RFCO showing an order summary for each OPID. The summary shows the pick method as well as the total 
number of units in the OPID. 
Create RF Confirm OPID 
Audit
Yes
No
If you select Yes, a time-stamp message is inserted in the Time Block of 
LOOR indicating that the OPID was confirmed in RFCO. If you select No, no 
time-stamp message is inserted in the Time Block of LOOR.
FIELD DESCRIPTIONS MISCELLANEOUS (2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MISCELLANEOUS (3)
This tab shows additional miscellaneous options.
RFOA Audit Level Level 1
Level 2
Level 3
Level 4
RFOA allows you to perform an audit of staged product before it is loaded 
onto the truck. In this field, you define your inventory level for such audits. 
For example, if you select Level 1, the RF operator will perform a count for 
each item on the order. If, on the other hand, you select Level 2, the RF operator will perform a count for each lot on the order.
RFOPS Sort Sequence 
Code (SOSE)
In this field, you can define a sort sequence for your process values in 
RFOPS. For example, an unsorted list of process values might appear as follows:
▪ carton ID
▪ carton ID
▪ carton ID
▪ weight
▪ weight
▪ weight
After sorting, the same list of process values could appear in a more logical 
order:
▪ carton ID
▪ weight
▪ carton ID
▪ weight
▪ carton ID
▪ weight
FIELD DESCRIPTIONS MISCELLANEOUS (2)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Miscellaneous (3) tab
FIELD DESCRIPTIONS MISCELLANEOUS (3)
Other Inventory Count 
Programs
In this field, you select the RF program(s) in which you wish to perform count 
backs.
Activate Inventory Count Always
Never
If Quantity Reaches or Falls Below Threshold Quantity
If you select “Always”, a count back is required each time the RF operator puts 
away/relocates/replenishes product. For put-away activities, the location 
counted is always the to location. For relocation and replenishment activities, 
the RF operator counts the inventory in the from location.
If you select “If Quantity Reaches or Falls Below Threshold Quantity”, a count 
back is only required if the quantity in the to location (for RF receiving) or the 
from location (for RF relocation and replenishment) falls below the threshold 
quantity that you define in the Threshold Quantity to Initiate Count field.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Inventory Count Rules Require Supervisor Override
Ignore Investigation But Lock the Entity (reserved for future use)
Ignore Investigation
These rules govern what happens when the inventory count for the location 
that is entered by the RF operator does not match the on hand quantity. If you 
select “Require Supervisor Override”, a supervisor will be required to log in 
and approve the discrepancy. If you select “Ignore Investigation”, the RF operator can proceed normally to the next pick/relocation/put-away, etc.
Threshold Quantity to Initiate CountOnly available if you select If Quantity Reaches or Falls Below Threshold 
Quantity in the Activate Inventory Count field
Your threshold quantity for initiating an inventory count.
Inventory Count for All RF 
Based On
Item
Item Count for Pick Line Locations, Entity Count for Rest of Locations
If you select “Item”, the RF operator will count each item in a given location. If 
you leave this field blank, the RF operator will count each inventory entity in a 
given location. If you select “Item Count for Pick Line Locations, Entity Count 
for Rest of Locations”, the RF operator will count each item for pick line location types and each inventory entity for all other location types.
Rules to Allow Short / 
Delete Line in RFIPS
Disallow Short / Delete Line
Allow Short / Delete Line
In this field, you activate/deactivate the shorting/deleting of receipt lines in 
RFIPS.
Suggested Location 
Rules in RFST
Follow Order
Follow Assigned Staging Location
In this field, you define the suggested or default to location in RFST. If you 
select “Follow Order”, the suggested location will be the to location where the 
last OPID was staged. In other words, the suggested to location is always the 
to location chosen in the previous order line.
If you select Follow “Assigned Staging Location”, the suggested location will 
be the staging location assigned to the order line in either SELO or the Wave 
Manager. It will not change for a given order even if the RF operator overrides 
the suggested to location.
FIELD DESCRIPTIONS MISCELLANEOUS (3)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MISCELLANEOUS (4)
This tab shows additional miscellaneous options.
Display To-Location in 
RFST
Yes option only available if Suggested Location Rules in RFST is activated
Yes
No
If you select Yes, the suggested to location is displayed. If you select No, the 
suggested to location is not displayed.
Default Staging Warehouse/Location Code in 
CASE
Custom use only.
Enter Adjustment InformationYes
No
If you set this flag to Yes and enter an adjustment in RFAJ, you will be 
prompted to enter an adjustment code (ADJU), a reason code (REAS) and 
remarks for each adjustment. If you set this flag to No, you will not be 
prompted for an adjustment code, reason code and remarks.
Allow Relocation of Multiple Pallets in RFRLYes
No
If you select Yes, the RF operator can relocate multiple pallets in a single step; 
that is, the RF operator scans two or more UI’s but only enters the to location 
once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type
FIELD DESCRIPTIONS MISCELLANEOUS (3)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Miscellaneous (4) tab
FIELD DESCRIPTIONS MISCELLANEOUS (4)
Allow Replenishment of 
Multiple Pallets in RFRP
Yes
No
If you select Yes, the RF operator can replenish multiple pallets in a single 
step; that is, the RF operator scans two or more UI’s but only enters the to 
location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Mixed Put-Away, 
Move up to Inventory 
Level
Up to level 1
Up to level 2
Up to level 3
If you select “Up to level 1/2/3”, the RF operator can put-away and move multiple pallets in the same location in a single step. The multiple pallets can contain mixed inventory up to the inventory level selected. For example, pallets 
from different receipts, appointments and inbound loads containing different 
level 2’s and 3’s can be placed on the same forklift and put-away together if 
you select “Up to level 1”.
This field applies to the following programs: RFCH, RFPU, RFST, RFRL, 
RFRP and OLOP.
If you leave this field blank, the RF operator cannot put-away/move mixed 
product in a single step.
Reason Code Required 
to Override SystemAssigned Location
Yes
No
Yes with Location Overridden (reserved for future use)
If you select Yes, the RF operator will be required to enter a reason code in 
RFCH/RFPU/RFRL if he or she overrides the system-assigned location code 
or requests an alternate location. For RFCH/RFPU overrides only, the reason 
code will be stored on the receipt line and a time stamp will be created.
RFCH screen showing pick list for reason code
Max. Number of F3 (NX) 
Allowed Per ILOP 
Sequence in RFRL
In this field, you specify the maximum number of times that the RF operator 
can press F3 (NX) in RFRL to display a suggested relocate location.
FIELD DESCRIPTIONS MISCELLANEOUS (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Allow Multiple Pallet 
Moves in RFST
Yes
No
If you select Yes, the RF operator can relocate multiple pallets in a single step; 
that is, the RF operator scans two or more UI’s in RFST but only enters the to 
location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the 
equipment type
Show Quantity Breakdown ScreenYes
No
If you select Yes, the item quantity breakdown will display as a pop-up message in the following programs: RFPIC, RFPK, RFRL, RFPR, RFRP, RFCH 
and RFPU.
Allow Skipping of 
Inbound Serial Number 
Validation in RFOPS
Yes
No
If you set this flag to Yes, you can skip the validation of inbound serial numbers when shipping serial number product in RFOPS. AccellosOne 3PL will 
create a new system-generated outbound serial number for the product being 
shipped. This feature is designed to save time and improve efficiency by eliminating the need to perform a validation scan for each case. 
For example, you are entering a transfer order to transfer serial number product from one account to another.
RFOPS screen showing F1 (SE) command
FIELD DESCRIPTIONS MISCELLANEOUS (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
The RF operator selects ME (Manual Entry). After entering the weight, the RF 
operator can press F1 (SE) to create a new system-generated serial number.
Allow Weight Reduction 
for Standard Weight Item 
in RFOPS
Yes
No
If you set this flag to Yes, you can reduce standard weight product by entering 
a quantity; for example, 5CS. The quantity entered by the RF operator must 
be less than or equal to the order quantity. When the RF operator presses F2 
(RC), the following prompt will appear:
RFOPS screen showing option 2
Enter Gross Weight in 
RFSC
Yes
No
If set to Yes, the RF operator will be required to enter the gross weight when 
closing a carton in RFSC. The weight measure code for the carton will be 
defined in DITP (Depositor Item Profile).
FIELD DESCRIPTIONS MISCELLANEOUS (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
MISCELLANEOUS (5)
This tab shows additional miscellaneous options.
Allow Put-Back of Outstanding REPI QuantityIn this field, you define put-back rules when the RF operator performs a partial 
replenishment (for example, less than a full pallet) because blocked or damaged product is preventing a full replenishment.
EXAMPLE
Item quantity breakdown: 50 cases per pallet
replenishment quantity from bulk: 45 cases (less than a full replenishment)
order quantity: 10 cases
No
A second replenishment of five cases is created (50 - 45 = 5) for the original 
pick line location.
Yes
RF operator is prompted to perform a second replenishment of 5 cases to 
either the original pick line location or to another pick line location.
Cancel REPI Task
If the on-hand quantity in the pick line location is greater than the on order 
quantity, the second replenishment is deleted. If the on-hand quantity in the 
pick line location is NOT greater than the on order quantity, a second replenishment is created for the original pick line location (same as No option).
Enable UI Scanning in 
Cycle Counts
Custom use only.
Suspend Flow Advancement in Outbound AuditYes
No
If you select Yes, the order line will NOT be advanced to the next flow even 
though your count matches the order line quantity when you perform an outbound audit in RFOA. If you select No, the order line will be advanced to the 
next flow when your count matches the order line quantity in RFOA. 
FIELD DESCRIPTIONS MISCELLANEOUS (4)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Miscellaneous (5) tab
FIELD DESCRIPTIONS MISCELLANEOUS (5)
Retain OPID to in RFMG Yes
No
If you select Yes, the OPID to value remains displayed on the screen after the 
merge so that the RF operator can continue to merge into the same OPID.

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Validate Manual Entry 
Process in RFOPS
Yes
No
If you select Yes, the following validations will occur when manually entering 
catch weights and serial numbers in RFOPS:
▪ the entry length and data type must match your setup in IPRO
▪ the outbound weight/serial number must match the inbound weight/serial 
number
▪ if the outbound weight does not match the inbound weight, it must be within 
the weight tolerance percent defined in ITEM
If you select No, only the entry length and data type must match your setup in 
IPRO.
Disallow REPI When 
Location Reaches Maximum Capacity
Yes
No
If you select Yes, replenishments will be canceled when the replenishment 
quantity plus the on-hand quantity in the pick line location exceeds the location's capacity. If you select No, replenishments will NOT be canceled when 
the replenishment quantity plus the on-hand quantity in the pick line location 
exceeds the location's capacity.
NOTES 
▪ Product on SUSP hold is not included in the pick line location’s on-hand 
quantity.
▪ The Yes option in MRFP will be ignored if you have shelf live overrides in 
CCOP (Customer/Consignee Override of PIPR) for an order triggering a 
replenishment.
Validate Serial Number 
(SN) From Picking Process
Yes
No
If you select No, serial number validation will be deactivated in RFSC. If you 
select Yes, serial number validation will be activated in RFSC and a valid 
serial number must be scanned for all product being packed in RFSC.
The purpose of the additional scan in RFSC to make sure that the serial number scanned during RFPIC is the same serial number going in the box during 
packing.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Display Minimum Number 
of REPI Records in 
Demand Mode
Yes
No
If you select Yes and there are multiple replenishment records for the same 
item, AccellosOne 3PL will show only the replenishments that are needed to 
satisfy the order quantity. Other replenishments that are required to satisfy the 
minimum quantity for the location will not appear in active demand mode.
For example, suppose there are 255 cases in a pick location with 305 on 
order. Although there are three replenishments for a total of 144 cases, only 
60 cases are needed to meet the order quantity and therefore only one replenishment (the one for 60 cases) will show in demand mode.
Override Quantity Breakdown - Actual (if > Std) or 
Std
Override Quantity Breakdown Type
If you select Override Quantity Breakdown Types, the following rules will apply 
to RFCH and RFMI:
▪ if the pallet quantity associated with the UI is less than the standard item 
quantity breakdown, use the standard quantity breakdown
▪ if the pallet quantity associated with the UI is greater than or equal to the 
item quantity breakdown, use the actual quantity breakdown
▪ for a pallet/case/each breakdown, the standard case/each configuration will 
not change
NOTE 
The quantity breakdown entered in RFCH will overwrite the quantity breakdown entered/set up in ENRE and EDI.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

GENERAL SETUP PROGRAMS
RF Profile (MRFP)
Display Process Description in RFOPSYes
No
If you select Yes, the item process code description will display in RFOPS. If 
you select No, the item process code only with no description will display.
RFOPS screen showing process code description
Allow Entry of Adjustment 
Code in RFMI
Yes
No
If you select Yes, the RF operator will be prompted to enter an adjustment 
code for the merge. If you select No, the default adjustment code set up in 
ATMP (Action Template Setup) will be used.
REPI Pick Location 
Capacity Based on UI
Yes
No
If you select Yes, the pick line location capacity will be based on the number of 
UI’s in the location and not on the number of units in the location. For example, if a location’s capacity is defined as two pallets and there are two UI’s in 
the location, the location will be considered full even if the two UI’s consist of 
partial pallets. When a pick line location is considered full, no replenishments 
will occur.
If you select No, the pick line location capacity will be based on the actual 
number of units in the location and not on the number of UI’s in the location.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

GENERAL SETUP PROGRAMS
Item RF Profile (MIRP)
Item RF Profile (MIRP)
In this program, you set up your suspended hold and inventory count rules at the item level. If you define a 
profile in MIRP and attach it to an item in ITEM, the suspended hold/inventory count rules in MIRP will 
override your suspended hold/inventory count defaults for a given customer defined in MRFP.
Location Scan Required 
for Count Backs and Suspend Holds
Yes
No
If you select Yes, the supervisor will be forced to scan in the current location 
when clearing a count back discrepancy or approving a suspended hold. If 
you leave this flag blank or set it to No, the supervisor will not be forced to 
scan in the current location when clearing a count back discrepancy or 
approving a suspended hold.
Allow Override of Receipt 
Line ILOP in RFCH
Yes
No
This flag allows you to manually remove an ILOP override attached to a 
receipt line in ENRE. If you select Yes, a pop-up will appear in RFCH allowing 
the RF operator to accept or remove the ILOP profile for the item being 
received. If you select No or leave this field blank, no pop-up will appear in 
RFCH allowing the RF operator to accept or remove the ILOP profile attached 
to the receipt line.
RFCH pop-up screen showing two options
FIELD DESCRIPTIONS MISCELLANEOUS (5)

GENERAL SETUP PROGRAMS
Item RF Profile (MIRP)
MIRP screen
FIELD DESCRIPTIONS (RFPIC TAB)
Code Your item RF profile code.
Description The description for your item RF profile code.
Allow Suspended Holds The following options are identical to the options in the Allow Suspended 
Holds field in MRFP:
Split Order Line, No Suspended Holds
Allow Suspended Holds
Only Allow if Supervisor Approved
Split Order Line, Allow Suspended Hold
Split Order Line, Supervisor Approved
The following options are only available in MIRP:
Split Order Line, Zero Out Remaining Quantity, No Suspended Hold
Split Order Line, Zero Out Remaining Quantity, Allow Suspended Hold
Split Order Line, Zero Out Remaining Quantity, Supervisor Approved
The various zero out remaining quantity options allow the picker to pick any 
quantity up to the order line quantity. For example, if the order line quantity is 5 
cases, the picker can pick 0, 1, 2, 3, 4 or 5 cases. AccellosOne 3PL will automatically zero out the remaining lines so that the order will ship without the 
need to reallocate the missing product or manually delete the lines in ENOR. 

GENERAL SETUP PROGRAMS
Warehouse/Customer/Location Config (WCLC)
MISCELLANEOUS TAB
If you select any options in these fields, they override the option(s) that you selected in MRFP.
Warehouse/Customer/Location Config (WCLC)
This program allows you to activate/deactivate UI scanning in RFPIC by warehouse code and customer code. 
It overrides the Display Rules for Location/UI/Quantity field in MRFP (RFPIC 3 tab). If you activate UI 
scanning for a given warehouse code/customer code combination, RFPICK will display the UI and the RF 
operator will need to press Enter to enter the QTY field. If required, the RF operator can overtype the UI.
Show Full Item Description in RFCHYes
No
If you select Yes, a pop-up box will display showing both the main item 
description and the alternate description in RFCH. if you select No, no pop-up 
box will display in the program.
Show Full Item Description in RFPICYes
No
If you select Yes, a pop-up box will display showing both the main item 
description and the alternate description in RFPIC. if you select No, no pop-up 
box will display in the program.
Activate Event-Driven 
Cycle Count in RFPIC
See the Cycle Counting Guide for further information on event-driven cycle 
counts.
Activate Inventory Count If you select an option in this field, it overrides the option that you selected in 
MRFP.
Inventory Count Rules If you select an option in this field, it overrides the option that you selected in 
MRFP.
Threshold Quantity to Initiate Count BackIf you select an option in this field, it overrides the option that you selected in 
MRFP.
Assign Pallet ID on Full 
Pallets of Last Inventory
If you select an option in this field, it overrides the option that you selected in 
MRFP.
FIELD DESCRIPTIONS (RFPIC TAB)

GENERAL SETUP PROGRAMS
Depositor Workflow Profile (DIFP)
WCLC screen
In the Detail Block, you can switch on or off UI scanning for individual locations within the warehouse that you 
specified in the Header Block.
WCLC screen showing Detail Block
Depositor Workflow Profile (DIFP)
Certain flows are mandatory for inbound and outbound processing in DIFP. Refer to the appropriate program 
(RFCH, RFPI, RFPIC, etc.) to see which flows are required for a given program.
RF Operator (RFOP)
In this program, you set up your RF operators and define their default company and Vocollect Voice 
password. In the Detail Block, you define which task profiles they are allowed to work in as well as their 
material handling type and activity type exclusions.
RF operators in RFOP are required in the following cases:
▪ you perform voice-activated picking using Vocollect Voice
▪ you pick by assignment in RFVP (RF Voice Pick)

GENERAL SETUP PROGRAMS
RF Operator (RFOP)
▪ you assign tasks to operators in RFOT (RF Operator Task Assign)
▪ you wish to track the equipment used by each RF operator and restrict certain RF operators to certain 
activity types and equipment types
▪ you perform tasking in RFITLV (RF Interleaving)
RF operators must be set up in OPER (Operator Code) before they can be set up in RFOP.
1 Enter RFOP.
2 Click on Create.
3 Key in your operator code and press Enter or press F10 to select it from the pick list.
4 Key in the operator’s default company and press Enter or press F10 to select if from the pick list.
5 If required, key in the operator’s voice password and press Enter.
6 In the Task Profile Block, key in your task profile and press Enter or select it from the pick list.
7 Repeat the above step for each additional task profile that you wish to assign to the operator.
FIELD DESCRIPTIONS
Operator
(defined in OPER)
Mandatory
Your operator code.
Default Company Mandatory
The company in which the RF operator will work. If you use Vocollect Voice 
and the operator has to switch companies, you must manually change the 
operator’s company in RFOP. If you pick your orders in RFPIC, you do not 
need to manually change the operator’s company in RFOP as the operator 
can perform this task in RFPIC.
Password Only required if you do voice-activated picking
The operator’s Vocollect Voice password.
MHET Types Exclusions See “RF Operator (RFOP)” on page 463 for further information.
Activity Type Exclusions See “RF Operator (RFOP)” on page 463 for further information.
Task Profile Enter the RF operator’s task profile.

GENERAL SETUP PROGRAMS
Extra Charge Setup for RF

RFOP screen showing operator PAUL assigned to task profile 1
8 Click on Exit to exit.
9 When prompted to save your changes, click on Yes.
ACTIVATING AN RF OPERATOR IN ACTIVEDESKTOP
If the RF operator is a new AccellosOne 3PL operator who has never logged on to ActiveDesktop, he or she 
must log on to ActiveDesktop to change his or her password. You cannot log on to a RF device with the 
default password defined in INST (Installation Parameters).
1 Log on to ActiveDesktop and proceed to change your password. Once your new password is accepted, 
you can log on to a RF device using this password.
Extra Charge Setup for RF
You can add extra charges to a receipt or order in RF using the program RFEC (RF Extra Charge). You can 
also enter extra charges directly in RFPIC (for outbound orders) and in RFCH (for inbound receipts). You 
activate extra charge entry in RF by making the appropriate changes to your extra charge profile in ECHP 
(Extra Charge Profile).

GENERAL SETUP PROGRAMS
Extra Charge Setup for RF
Extra charge entry in RF is only available for customer-based extra charges; that is your ECHP profile is 
attached to a customer. AccellosOne 3PL does not support RF extra charges attached to an item.
FIELD DESCRIPTIONS (ECHP)
Charge Code (CHAR) The charge code that you enter must be unique in ECHP within a given 
inbound or outbound workflow. You cannot use the same charge code under a 
different sequence for a given inbound or outbound workflow. 
Allow RF Entry / Allow 
Override of Charge 
Quantity in RF
There are three possible scenarios for these two fields:
Allow RF Entry = No
Allow Override of Charge Quantity in RF = No
In this scenario, the RF operator cannot add extra charges in RF.
Allow RF Entry = No
Allow Override of Charge Quantity in RF = Yes
In this scenario, the RF operator can select one or more extra charges from a 
predefined list and can enter any charge quantity for the selected charge(s).
Allow RF Entry = Yes
Allow Override of Charge Quantity in RF = Yes
In this scenario, the RF operator must manually enter his or her extra charges 
(if any) and can enter any charge quantity for the entered charges.
Flow Process Code 
(FLPR) for RF
Optional
If you enter a flow, the extra charge can only be added at this inbound or outbound flow. If you leave this field blank, the extra charge can be added at any 
inbound or outbound flow.
Other fields Refer to the Billing and Invoicing Guide for further information.

GENERAL SETUP PROGRAMS
Extra Charge Setup for RF
ECHP screen showing fields for extra charge entry in RF
For inbound extra charges, you must set the Extra Charge Entry Type flag on the RFCH Only 2 tab in MRFP 
to the appropriate value.
FIELD DESCRIPTIONS (RFCH ONLY 2)
Extra Charge Entry Type Allow Extra Charge Entry When Completed
Allow Extra Charge Entry When Exiting
If you select “Allow Extra Charge Entry When Completed”, the extra charge 
screen will display when you finish checking/unloading the receipt line. If you 
select “Allow Extra Charge Entry When Exiting”, the extra charge screen will 
display when you exit RFCH.

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
For outbound extra charges, you must set the Extra Charge Entry Type flag on the RFPIC tab in MRFP to the 
appropriate value.
Warehouse Zones (WHZO)
In this program, you subdivide your warehouse into separate zones. Each zone can be considered a separate 
work area and the same order or receipt can be assigned to multiple RF operators working in different zones. 
A zone can be a section of your warehouse or a set of racks (for example, all floor-level racks could be zone 
1, all second-level racks could be zone 2, etc.).
There are seven zone types in WHZO:
FIELD DESCRIPTIONS (RFPIC 2)
Extra Charge Entry Type Allow Extra Charge Entry When Completed
Allow Extra Charge Entry When Exiting
If you select “Allow Extra Charge Entry When Completed”, the extra charge 
screen will display when you finish picking the order line. If you select “Allow 
Extra Charge Entry When Exiting”, the extra charge screen will display when 
you exit RFPIC.
Directed Put-Away Directed put-away zones allow you to define overflow sequences for directed 
put-away in the Overflow Sequence Block. For example, if no locations are 
available in put-away zone 1, try put-away zone 2 then put-away zone 3.
General General zones have no collection or drop off points assigned to them.
Sorting Area Sorting Area zones types have a drop off point assigned to them; that is, they 
require a location code in the header block of WHZO.
Material Handling Type This zone type is used for material handling type integration.
P & D P & D zones types have a collection point assigned to them; that is, they 
require a location code in the header block of WHZO.
Interleaving Interleaving zone types are used in RFITLV.
Voice Voice zone types are used for voice-activated picking.

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
P & D zone consisting of 12 locations in aisle A with a P & D location (A100)
HEADER BLOCK
In this block, you define your warehouse zone code and description, your zone type code and your 
warehouse/location code for sorting or P & D zones types.
A100
(P & D location)
A101 A102 A103 A104 A105 A106
A107 A108 A109 A110 A111 A112
FIELD DESCRIPTIONS
Warehouse Zone Code Mandatory
Your code for this zone.
Description Mandatory
A meaningful description for this zone.
Zone Sort Value Mandatory
Set this field to 1 for all zones.
Labor Standard Modifier See the section on Operational Board in the Operations 2 Guide.
Communication ReferenceReserved for future use

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
FORMULA BLOCK
The Formula Block allows you to specify warehouse and location restrictions (for example, a range of 
locations) for the zone. When you exit the Formula Block, the system will automatically add the locations that 
you specify to the zone. If you use the Formula Block in modify record mode, any existing locations assigned 
to the warehouse zone will be removed and new locations will be assigned based on your formula.
Zone Type Code D = Directed Put-Away
G = General
M = Material Handling Type
S = Sorting Area
P = P & D
I = Interleaving
V = Voice
The zone type field allows you to define collection and drop off points for a 
zone and to assign to it a specific material handling equipment type.
If you select General, the zone will have no collection or drop off points. If you 
select Sorting Area, the zone will have a collection point for outbound product. 
If you select P & D, the zone will have a drop off or pick-up point for product.
Task Required Only available if Enable Task Interleaving in COMP = Create Tasks According 
to Zone Setting
See “Warehouse Zones (WHZO)” on page 472.
Warehouse Code 
(defined in WARE)
Mandatory if zone type = S or P
The warehouse code of the location that you wish to attach to the zone.
Location Code
(defined in LOCA)
Mandatory if zone type = S or P
The sorting or P & D location that you wish to attach to the zone.
Material Handling Type 
Inbound Code 
For HighJump use only.
Material Handling Type 
Outbound Empty Code 
For HighJump use only.
Material Handling Type 
Outbound Partial Code 
For HighJump use only.
FIELD DESCRIPTIONS

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
If your location codes contain spaces or hyphens (-), you must use the caret character (^) before the space or 
hyphen.
EXAMPLE 1
EXAMPLE 2
If your range is … You enter …
R 0K 001 1 to R 0K 044 5 R^ 0K^ 001^ 1-R^ 0K^ 044^ 5
If your range is … You enter …
P-OA-001-1 to P-OA-099-2 P^-OA^-001^-1-P^-OA^-099^-2
FIELD DESCRIPTIONS
Inbound/Outbound Only available for zone types of G
I = Inbound
O = Outbound
B = Both
If you specify Inbound, the locations added by the system will all be flagged as 
inbound locations. If you specify Outbound, the locations added by the system 
will all be flagged as outbound locations. If you specify Both, the locations 
added by the system will all be flagged as both inbound and outbound locations.
If you are setting up a P, S or M zone type, the value that you enter in this field 
is ignored because the zone type is either self-defined or defined in other programs.
Warehouse Code
(defined in WARE)
Mandatory
Only locations belonging to the warehouse(s) that you specify can be added to 
the zone. See the following paragraph for a list of the operands that you use to 
specify one or more warehouses. 
Location Code
(defined in LOCA)
Mandatory
Your location restrictions for the zone. See the following paragraph for a list of 
the operands that you use to specify one or more locations.

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
The following operands can be entered in the Warehouse Code and Location Code fields:
EXAMPLES
= match of characters entered
(=) not equal to
> greater than or equal to
< less than or equal to
- from X to Y (a range)
=1 Any location code beginning with 1
(for example, 1, 111, 199, 1ABC)
=1,=2 Any location code beginning with 1 or 2
(for example, 1, 111, 299, 2ABC)
(=1) All warehouses except warehouse 1 
(=1),(=2) All warehouses except warehouses 1 and 2 
>F101 All locations greater than or equal to location F101
(for example, F102, F199, F4, G99, etc.)
<D101 All locations less than or equal to location D101
(for example, A101, B999, D100, etc.)
A101-C999 Locations A101 through C999

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
Warehouse Zone Codes showing Formula Block
PROCEDURE
1 Enter WHZO.
2 Click on Create Record.
3 Key in your zone code and press Enter.
4 Key in your description for the zone code and press Enter.
5 Key in 1 as your zone sort value and press Enter.
6 Press Enter to bypass the Labor Standard Modifier field.
7 Press Enter to bypass the Communication Reference field.
8 In the Zone Type Code field, key in the appropriate value (G for General, I for Interleaving, S for Sorting 
Area, P for P & D or I for Interleaving) and press Enter.
9 Press Enter to bypass the Task Interleaving field.
If you enter G or I: If you enter P or S:
a) Proceed to next step. a) Key in your warehouse code 
and press Enter.
b) Key in your location code and 
press Enter.
c) Press Enter the required number of times to bypass the 
material handling type fields.

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
Warehouse Zone Codes showing Formula Block
10 When the Formula Block appears, do one of the following:
11 In the Warehouse Code field, key in your warehouse code restriction (for example, “=”) and press Enter. 
12 In the Location Code field, key in your location restrictions (for example, “>”) and press Enter. AccellosOne 3PL will retrieve all locations that meet the criteria that you specify and display the Locations 
Block. If there are no location restrictions, leave this field blank.
Warehouse Zone Codes showing External Messages
13 If you wish to print, fax or e-mail your External Messages, click on Select Printer. Then key in the appropriate printer code or use the pick list function to select it. Next click on Execute Report. If you selected 
either fax or mail as your printer, the Fax/Mail Entry pop-up window will appear. Enter your fax number or 
e-mail address and any other required information and then click on Send e-mail or Send fax.
For G or I type zones: For P or S type zones:
a) Key in I for Inbound, O for Outbound or B for Both in the 
Inbound/Outbound field and 
press Enter.
a) Key in B for Both in the Inbound/
Outbound field and press Enter.

GENERAL SETUP PROGRAMS
Warehouse Zones (WHZO)
14 Click on Exit to close the External Messages window. The locations that you specified in the Formula 
Block will be added to your zone.
15 Click on Location Block.
Warehouse Zone Codes showing 28 locations assigned to Zone 2
16 If required, you can manually add or remove a location in the Location Block. To add a location, click on 
Create Record and key in your warehouse code, your location code, your inbound/outbound value and 
your zone type.
If you wish to remove a location from the Location Block, move your arrow key to the appropriate location 
and press Enter until your cursor is positioned in the Inbound/Outbound column. Then click on Delete. 
If you wish to change the Inbound/Outbound flag, key over the default value of B for Both with either I for 
Inbound or O for Outbound.
When you finish making your changes, click on Return to Main.
17 When you finish setting up your zone, click on Master Block and then Exit to exit.
OVERFLOW SEQUENCE BLOCK
If product cannot be put-away in a given warehouse zone, you can define an overflow sequence for 
warehouse zones in the Overflow Sequence Block. The overflow zones must have the same zone type code 
as the header zone.
Warehouse zones used in directed put-away require a zone type code of D (for Directed Put-Away).

GENERAL SETUP PROGRAMS
Company Code (COMP)
x
WHZO screen showing overflow zone codes
Company Code (COMP)
The following fields in COMP may require setup:
FIELD DESCRIPTIONS (MISCELLANEOUS 5)
RF Special Character You can define a special character (for example, $) or a string of special characters as an RF check digit for your location codes. If you deactivate the special characters on your RF guns, RF operators will be forced to scan in the 
location code rather than typing it in manually.
RF special character logic allows up to five special characters and applies to 
RFCH, RFRL, RFPIC and RFRP.

GENERAL SETUP PROGRAMS
RF Supervisors
RF Supervisors
RF supervisors have certain privileges that are denied to non-supervisory RF operators; for example, they 
can zero out receipts lines in RFCH when a variance is encountered. See the System Administration Guide
for further information on setting up an RF supervisor.
Supervisor Notification
The supervisor notification system is triggered whenever a non-supervisory RF performs an action that 
requires supervisor approval. For example, the RF operator creates a new receipt line in RFCH, changes a 
suggested put-away location in RFPU, places product on hold in RFPIC, etc. The specific actions that require 
supervisor approval are defined in MRFP (RF Profile).
When supervisor notification is activated, an automatic email notification is generated and sent to a group 
email address for supervisors. The email would summarize the problem and identify the location.
Email notification message showing operator code, RF program, type of override and location
This allows the supervisor to go the location causing the problem and approve or reject the override in the 
usual manner. It eliminates the need for the RF operator to leave his or her current location in search of a 
supervisor to have the issue resolved.
Set Default Values in RF 
Pallet Screen
Yes
No
If you set this flag to Yes, the RF operator will see default values for the 
account code, account type and transaction type fields in the Pallet Entry 
screen for RFPIC, RFPK, RFVP, RFCH and RFPU. 
The default account code will be the customer for the order/receipt and the 
default account type will be the customer. For inbound receiving, the default 
transaction type will be R for Receiving; for outbound shipping, the default 
transaction type will be S for Shipping.
If you set this flag to No, the account code, account type and transaction type 
fields will be blank when the RF operator first accesses the Pallet Entry 
screen.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

GENERAL SETUP PROGRAMS
Supervisor Notification
The following actions trigger an automatic email notification and the creation of an override record in RFSUN:
▪ a non-supervisory RF operator creates a new receipt line in RFCH
▪ a non-supervisory RF operator overrides a suggested put-away location in RFPU 
▪ a non-supervisory RF operator records a variance for the put-away quantity in RFPU
▪ a non-supervisory RF operator places product on suspend hold in RFPIC
▪ a non-supervisory RF operator enters a countback quantity in RFPIC that does not match the system 
quantity
▪ a non-supervisory RF operator enters a loading quantity in OLOP that does not match the system quantity
▪ a non-supervisory RF operator places product on hold in RFRL
There are three setup programs for supervisor notification: COMP (Company Code), WARE (Warehouse and 
Location Format) and MRFP (RF Profile).
In the Supervisor Notification Group Email Address field in COMP, you enter the default group email address 
for supervisor notification.
Supervisor goes to the location, logs in to the 
appropriate program and approves the 
override (existing logic). 
email
RFSUN
Email message containing a description of 
the problem and the location where it 
occurred is created and sent to group email 
address for supervisors.
Override record is created in RFSUN. 
RFCH/
RFPU, etc.
RFCH/
RFPU, etc.
Non-supervisory RF operator encounters a 
supervisor override event (new receipt line in 
RFCH, override of suggested put-away 
location in RFPU, etc.).
1
2
3
4
RFSUN
At a later time, supervisor reviews the 
override records and individually approves 
them. Approved override records no longer 
appear in RFSUN.
5

GENERAL SETUP PROGRAMS
Supervisor Notification
COMP screen showing field
In the Supervisor Notification Group Email Address field in WARE, you enter the group email address for a 
specific warehouse. If this field is populated with a valid email address, it will override the group email 
address at the company level.

GENERAL SETUP PROGRAMS
Supervisor Notification
WARE screen showing field
In MRFP supervisor approval must be activated for creating new receipt lines in RFCH, changing a 
suggested put-away location in RFPU, placing product on suspend hold in RFPIC, etc.
RFSUN allows supervisors to look up and accept overrides from the following programs: RFCH, RFPU, 
RFPIC, OLOP and RFRL. When an override is accepted in RFSUN, it is deleted and can no longer be 
accessed.

OUTBOUND SETUP PROGRAMS
About the Task Engine ................................................................................... 106
Overview of Setup Programs ......................................................................... 106
Customer Codes (CUST) ................................................................................ 107
Customer / Consignee Document Setup (CCDU)......................................... 109
Item Hazardous Material Violation (IHZV) ..................................................... 110
Outbound Pallet Building With the Pallet Build Engine .............................. 111
Task Profile (REGI).......................................................................................... 115
Adding Filters to REGI ............................................................................... 118
Item Consignee Configuration (ICOC)........................................................... 119
Document Messages Block ....................................................................... 123
Outbound Process Configuration (CCCC).................................................... 120
Warehouse Customer Consignee OPID Rule (WCCO) ................................ 124
Customer/Consignee Outbound Rules (CCOR) ........................................... 124

OUTBOUND SETUP PROGRAMS
About the Task Engine
About the Task Engine
The task engine offers a fully automated solution to outbound task assignment. Instead of allowing RF 
operators to pick orders at their own pace and in a sequence that does not take into account the tasks of 
other RF operators, AccellosOne 3PL consolidates all picking and replenishment tasks in a single centralized 
“bucket”.
When an RF operator logs into RFPIC, he or she is assigned the next available outbound task in the bucket. 
The next available task is based on a number of factors including:
▪ the RF operator’s equipment
▪ the RF operator’s proximity to the task’s location
▪ the RF operator’s task profile
▪ the location’s height restrictions
▪ the priority assigned to the task’s activity type
▪ the task’s pick method (full pallet pick vs. case pick)
▪ the level of congestion in a particular aisle
If an RF operator chooses to skip a pick or replenishment task, AccellosOne 3PL will record the skipped task 
as well as the operator who skipped it.
This purpose of tasking is to optimize the distribution of warehouse tasks such that travel times in the 
warehouse are reduced to a minimum, urgent tasks are performed first and congestion in warehouse aisles is 
avoided whenever possible.
Tasks are sorted in the following sequence:
▪ Task Priority Override if any
▪ Warehouse Activity Type Number 
▪ Ship To Date/Time 
▪ Order Priority Number
▪ Create Date/Time 
The task engine will not release pick tasks if there are pending replenishment tasks. For pre-build outbound 
pallets (pallets generated at the time of waving), the entire assignment will not be released if there is a single 
pending replenishment task. Each time that a pick task cannot be released because of a pending replenishment, the priority of the replenishment task will be increased.
ACTIVATING THE TASK ENGINE
You activate the task engine by setting up one or more task profiles in REGI and then attaching your RF 
operators to the appropriate task profile(s) in RFOT.
Overview of Setup Programs
The following graphic shows the various setup programs for outbound processing.

OUTBOUND SETUP PROGRAMS
Customer Codes (CUST)
Customer Codes (CUST)
Make sure that the Consolidation Method for Allocated Lines field in CUST is set to Multiple Location Lines 
NOT Allowed.
MHET WATP
CCCC
CTSZ
REGI
PKST
REGI CCCC
CCDU
RFOP
RF operators set up in RFOP are attached to material 
handling equipment types, task profiles and warehouse 
activity types.
Task profiles are attached to outbound process 
configurations. If required, OPID mix/no mix rule in 
WCCO overrides CCCC.
Document codes and pick methods are attached to 
various combinations of customer/consignee/carrier in 
CCDU.
ITEM
ICNP
In cartonization setup, packing stations are defined in 
PKST, carton size codes are attached to outbound 
process configurations and item cartonization profile 
codes are attached to items.
WCCO
CCOR
Outbound rules relating to allocation, manual pallet 
picking in RFPIC and SSCC/MCP labels are attached to 
various combinations of customer/consignee.

OUTBOUND SETUP PROGRAMS
Customer Codes (CUST)

CUST (Customer Code) screen showing Consolidation Method for Allocated Lines set to Multiple 
Location Lines NOT Allowed
FIELD DESCRIPTIONS
Consolidation Method for 
Allocated Lines
Multiple Location Lines Allowed (default value)
Multiple Location Lines NOT Allowed
If you set this field to Multiple Location Lines Allowed, AccellosOne 3PL will 
not create additional order lines when an order line picks from more than one 
location. If you set this field to Multiple Location Lines NOT Allowed, AccellosOne 3PL will create additional order lines to ensure that no order line has 
more than one location line. 
For example, if an order line of 30 cases requires picks from three different 
locations, AccellosOne 3PL will create two additional order lines for a total of 
three: line 1 (10 cases), line 2 (15 cases) and line 3 (5 cases).
The Multiple Location Lines NOT Allowed option requires P-type order lines in 
ENOR.
The advantage of this feature is faster picking of large order lines by splitting 
the work into multiple tasks that can be performed by multiple operators. If you 
activate this feature, three operators could work on the same order line if that 
line picked from three different locations. If you deactivate this feature, the 
entire order line could only be picked by a single operator.

OUTBOUND SETUP PROGRAMS
Customer / Consignee Document Setup (CCDU)
Customer / Consignee Document Setup (CCDU)
In this program, you set up your label document(s) and pick methods for RFPIC, RFPK and RFSC. 
Documents set up in CCDU are not flow dependent and do not need to be attached to the appropriate 
outbound flow in DIFP.
You can set up a single label document for all customers/carriers/consignees or you can define a specific 
label document for certain customer/carrier/consignee combinations. For example, in RFPIC label 1 will print 
for customer A, label 2 will print for customer B and label 3 will print for all other customers.
You can also define different documents for different pick methods: for example, print label 1 when each 
picking and print label 2 when pallet picking.
FIELD DESCRIPTIONS
Customer Code The customer that the label document applies to or .ALL for all customers.
Consignee Code The consignee that the label document applies to or .ALL for all consignees.
Carrier Code The carrier that the label document applies to or .ALL for all carriers.
Pick Method Batch Label Pick
Each Pick
Label Pick
Non-RF Packing Station
Packed via Packing Station
Pallet Pick
RF Merge
System-Driven Cartonization Each Pick
The pick method that the label document applies to. If you leave this field 
blank (that is, no pick method), the pick method is CASE.
Document Code Your document code for the unique customer/consignee combination. This 
document code must be set up in DOCU.
Interface Flag If you are printing an actual document on a physical printer, leave this flag 
blank. If you are sending your CCDU information to another device for further 
processing, click on this flag to select it.

OUTBOUND SETUP PROGRAMS
Item Hazardous Material Violation (IHZV)
CCDU screen showing bill of lading document for customer A2, all carriers, all consignees and all 
picking methods
Item Hazardous Material Violation (IHZV)
In this program, you define your segregation rules for outbound pallets and containers; for example, 
hazardous class 1.1 (Explosives) cannot be mixed with hazardous class 1.2 (Explosives). The segregation 
rules apply to RFPIC (RF Pick) and RFMG (RF Merge OPID). To activate hazmat segregations rules in these 
programs, you must set the Separate Hazmat by Item in Each Pick flag in MRFP (RFPIC 3 tab) to Yes.
If the rules in IHZV are violated, the RF operator will be not be able to pick the line in RFPIC or merge the 
OPID in RFMG.
IHZV screen showing classes 1.2, 1.3 and 1.4 as restricted classes for class 1.1

OUTBOUND SETUP PROGRAMS
Outbound Pallet Building With the Pallet Build Engine
Outbound Pallet Building With the Pallet Build Engine
The Pallet Build engine allows you to generate picking assignments (outbound pallets) based on predefined 
pallet building rules. Pallet building is only available for orders assigned to a wave in Wave Manager and 
picked in RFITLV (RF Interleaving).
There are two types of pallet building in AccellosOne Enterprise 3PL: pre-built pallets and dynamically
built pallets. With pre-built pallet building, the pallet is built during waving and you can view and edit your 
pallet build assignments in PABU (Pallet Build). With dynamic pallet building, on the other hand, the pallet is 
built in real time by the Task Engine taking into account only the currently available tasks and you cannot view 
or edit your pallet build assignments in PABU.
Pre-built pallets are built when orders are waved. The pallet build engine will look at the entire order and then 
calculate the contents and pick sequence for your outbound pallets. The number of pallets generated is based 
on your picking path mode, your maximum cube and weight rules per pallet and whether or not a single pallet 
can contain mixed product. Dynamically built pallets, on the other hand, are built in real time as the RF 
operator moves through the warehouse performing his or her picks. Rather than looking at the entire order, 
the pallet build engine looks only at the currently available tasks facing a given RF operator.
The Pallet Build engine will automatically generate pallet build assignments based on the following rules: 
▪ all product must be on the same order
▪ the maximum cube for full pallet/half pallet (REGI) cannot be exceeded
▪ the maximum weight (REGI) cannot be exceeded
▪ “like” product (that is, the same alternate reporting type/code) will be kept together (ITEM)
▪ the pallet build restrictions defined in IPBR must be respected
There are six setup programs for the Pallet Build engine:
▪ IPBR (Item Pallet Build Restrictions)
▪ ITEM (Item Codes)
▪ REGI (Task Profile)
▪ CCCC (Outbound Process Configuration)
▪ CONS (Consignees)
▪ COMP (Company Code)
In IPBR you set up your pallet build restrictions, defining which items can be placed together on the same 
pallet. For example, if you add the code R1 in the Header Block and the code R2 in the Detail Block, items 
assigned your R1 pallet restriction code can never be placed on the same pallet as items assigned your R2 
pallet restriction code. 
If you select the Allow Only on Top checkbox, items assigned the pallet build restriction code in the Detail 
Block can be placed on top of but not underneath items assigned the pallet build restriction code in the 
Header Block. Your IPBR code is then attached to the appropriate items in ITEM.

OUTBOUND SETUP PROGRAMS
Outbound Pallet Building With the Pallet Build Engine
IPBR screen
ITEM screen showing IPBR code of R1
In ITEM, you define the following:
Stackability Indicator Code In this field, you define how heavy or light the item is compared to other items. 
You can choose any value from Category 1 (base item or very heavy) to Category 5 (the lightest possible 
item). The Pallet Build engine will not allow you to place heavier items on top of lighter items.
Stackability Quantity in Highest SKU In this field, you define the maximum number of units that can be 
stacked on top of each other. For example, if the item’s highest SKU is cases and you enter 10 in this field, 

OUTBOUND SETUP PROGRAMS
Outbound Pallet Building With the Pallet Build Engine
the maximum number of cases that can be stacked on top of each other is 10. This field is for reporting 
purposes only.
ITEM screen
In REGI you define the Maximum Pallet Height and Maximum Number of Cartons.
REGI screen
In CONS, you set the Single Item Per Outbound Pallet flag to the appropriate value. If you set this flag to 
Yes, the Pallet Build engine will check this flag and restrict outbound pallets to a single item.

OUTBOUND SETUP PROGRAMS
Outbound Pallet Building With the Pallet Build Engine
CONS screen showing flag set to No
In COMP, you set the Use Assignment Parameter Tables for Pallet Build flag to the appropriate value. If 
you set this flag to Yes, you can rebuild pallets any number of times using the same REGI/CCCC configuration that was in effect when you first built the pallet for a given order line. If you set this flag to No and you 
rebuild a pallet, AccellosOne 3PL will use your default pallet build settings in REGI and CCCC.
COMP screen showing the Use Assignment Parameter Tables for Pallet Build flag 

OUTBOUND SETUP PROGRAMS
Task Profile (REGI)
Task Profile (REGI)
In this program, you set up your task profile(s). A task profile defines various picking options for RF operators. 
For each task profile that you set up, you can define the following options:
▪ the default staging location and warehouse
▪ the picking path mode or sequence in which locations are picked
▪ the sort sequence code (if any) and picking path mode
▪ the maximum pallet weight and/or cube for a pallet assignment when that pallet assignment contains 
mixed product
REGI is a mandatory setup program for the following programs/functions:
▪ voice-activated picking
▪ outbound pallet building
▪ picking by assignment in RFPV
▪ tasking in RFITLV
If you pick by order line in RFPIC and do not use assignments, task profiles are not required.
Task profiles are attached to operators in RFOP. They can also be attached to Outbound Process Configuration (CCCC). If required, you can set up different task profiles for different combinations of customer, 
consignee and carrier in CCCC.
FIELD DESCRIPTIONS
Task Profile Mandatory
Your task profile.
Description Mandatory
A description for your task profile.
Voice Profile Code 
(VOPR)
See “Setting Up Voice-Activated Picking” on page 390.
Default Customer Voice 
Profile Code (VOPC)
See “Setting Up Voice-Activated Picking” on page 390.

OUTBOUND SETUP PROGRAMS
Task Profile (REGI)
Staging Location Optional
The default staging location for the task profile. If you do not specify a default 
staging location, the RF operator will be required to specify a staging location 
during picking.
Warehouse Optional
The warehouse to which the default staging location belongs.
Sort Sequence Code 
(SOSE)
Optional
The sort sequence or “snaking” of your locations within the task profile. This 
sort sequence is applied to a picking path mode. If you do not enter a sort 
sequence code, the sequence of your pick locations will be based on the 
option that you select in the Picking Path Mode field.
Length of UI Check Digit See “Setting Up Voice-Activated Picking” on page 390.
Picking Path Mode Pick in location sequence
With this option, work assignments will be sequenced in location code 
sequence and order line splitting will be allowed.
The remaining options in this field (“Pick in location sequence, do not split 
order lines”, etc.) are custom and are only to be used if you are so advised by 
your HighJump implementation consultant.
% Reserved for future use.
Alternate Reporting Type 
/ Code
Reserved for future use.
OPID Prefix Optional
The prefix for your OPID’s (outbound pallet ID’s).
Spoken Length See “Setting Up Voice-Activated Picking” on page 390.
Spoken Value Numeric See “Setting Up Voice-Activated Picking” on page 390.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Task Profile (REGI)
1 Enter REGI.
2 Key in your task profile and press Enter.
3 Key in a description for your new task profile and press Enter.
Maximum Pallet Weight Optional
The maximum weight for a full pallet. If the weight of the order line exceeds 
this maximum, AccellosOne 3PL will split the line into two or more work 
assignments.
Maximum Pallet Cube Optional
The maximum cube for a full pallet. If the cube of the order line exceeds this 
maximum, AccellosOne 3PL will split the line into two or more assignments.
Maximum Pallet Height The maximum height for a full pallet. If the height of the order line exceeds this 
maximum, AccellosOne 3PL will split the line into two or more assignments.
Pallet Base Length/Width Reserved for future use.
Maximum Half Pallet 
Cube
Optional
The maximum cube for a half pallet.
Max. Number of Cartons The maximum size of a pallet assignment for the Pallet Build engine.
Max. Number of OperatorsSee “OUTBOUND TASKING” on page 467.
Max. Number of Operators per LocationSee “OUTBOUND TASKING” on page 467.
Select Only Assignment 
With Both Pick Line/NonPick Line Locations
See “OUTBOUND TASKING” on page 467.
Priority to Force ReplenishmentSee “OUTBOUND TASKING” on page 467.
Weight Measure Code The weight measure code for the Maximum Pallet Weight field.
Linear Measure Code The linear measure code for the Maximum Pallet Cube field.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Task Profile (REGI)
4 Key in your voice profile code and press Enter.
5 If required, key in your staging location and press Enter. 
6 If required, key in your staging warehouse and press Enter.
7 If required, select the appropriate sort sequence code from the pick list.
8 Enter or select any other required parameters for your task profile.
9 When you finish setting up the general parameters for your task profile, click on Save.
REG screen showing task profile 1
10 Click on Exit to exit REGI.
ADDING FILTERS TO REGI
If you create a saved filter in REGI, the filter column name fields will be populated with your filter values.

OUTBOUND SETUP PROGRAMS
Item Consignee Configuration (ICOC)
REG screen showing filters
Item Consignee Configuration (ICOC)
In this program, you can define the outbound pallet quantity by consignee when building outbound pallets 
(pallet build, case picking, OPID merge) for an outbound order. ICOC must be activated in CCOR by setting 
the Use Consignee Item Configuration flag to Yes for the appropriate consignee record.
ICOC screen

OUTBOUND SETUP PROGRAMS
Outbound Process Configuration (CCCC)
Outbound Process Configuration (CCCC)
In this program, you set up your pallet wrapping rules for different customer/carrier/consignee combinations. 
You can also override certain MRFP settings for a specific customer/carrier/consignee combination. For 
example, suppose your default picking mode is set to case picking in MRFP; however, based on your CCCC 
setting for a specific customer/carrier/ consignee combination, you can establish normal mode picking instead 
of case pick for that combination.
In CCCC you also specify your pallet building mode in the Task Profile (REGI) field: pre-built or dynamically 
built.
FIELD DESCRIPTIONS
Customer Code The customer that the outbound process configuration applies to or .ALL for 
all customers.
Carrier Code The carrier that the outbound process configuration applies to or .ALL for all 
carriers.
Consignee Code The consignee that the outbound process configuration applies to or .ALL for 
all consignees.
Number of Times Pallet 
Wrapping is Required
Only required for pallet wrapping
If pallet wrapping is required for a pallet being built in the warehouse, enter the 
number of times in this field.
Number of Times Pallet 
Wrapping is Required for 
Pallet Pick
Only required for pallet wrapping
If pallet rewrapping is required for a full pallet pick (that is, the pallet was 
already wrapped when it was received into the warehouse), enter the number 
of times in this field.
Number of Hours from 
Ship Date to Release Full 
Pallet Pick Task
Only available if tasking is activated
In this field, you specify the number of hours before the ship date that a full 
pallet pick task is created. 
Task Profile Code (REGI) If you populate this field with a task profile, pre-built pallet building will be activated. If you leave this field blank, dynamic pallet building will be activated.

OUTBOUND SETUP PROGRAMS
Outbound Process Configuration (CCCC)
Default Mode in RFPIC Only required if you pick in RFPIC
If you select a mode in this field, it will override your default picking mode in 
MRFP.
OPID Assignment Rules Only required if you pick in RFPIC
No Restriction
Per Item
Per OPID, OPID entered by user, QRS label by line
Per Order
Per Order Line
Per Order Line in NM Mode
In this field, you define your OPID assignment rules for case pick mode in 
RFPIC.
If you select Per Item, a single OPID per item is required. That is to say, the 
same item cannot be assigned to two or more OPID’s. If you select Per Order, 
a single OPID per order is required. If you select Per Order Line, a single 
OPID per order line in case pick mode is required. If you select Per Order Line 
in NM Mode, a single OPID per order line in normal mode is required.
If you select Per OPID, OPID entered by user, QRS label by line, AccellosOne 
3PL will generate a QRS value for each OPID entered by the user. This option 
is only available for QRS orders in which the user enters an OPID for each 
order line.
If you select No Restriction, the same OPID can be assigned to any number of 
items, orders or order lines.
Allow Partial Picking in 
Normal Mode
Allow all, no restriction
Allow last remaining partial inventory and full pallets
Allow full pallets only
If you select an option in this field, it will override the option that you selected 
in MRFP.
Workflow Profile Code 
(DIFP)
If you enter a workflow profile code in this field, it will override the workflow 
profile code(s) attached to the customer and consignee.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Outbound Process Configuration (CCCC)
AccellosOne Ship Date Current Date
Ship to Date
if you select Current Date, AccellosOne Ship will use the current date as the 
ship to date sent to the parcel carrier even if that date differs from the order 
ship to date in AccellosOne 3PL. If you select Ship to Date, AccellosOne Ship 
will use the order ship to date in AccellosOne 3PL as the ship to date sent to 
the parcel carrier.
UCC-128 Package Type Carton
Container
Pallet
The UCC-128 packaging type.
Maximum Gross Weight 
per OPID
The maximum gross weight for an OPID in RFPIC/RFMG (that is, pallet building, case picking and OPID merging).
Maximum Net Weight per 
OPID
The maximum net weight for an OPID in RFPIC/RFMG (that is, pallet building, 
case picking and OPID merging).
OPID Weight Measure 
Code
The unit of measure for the maximum weight.
OPID Alert Percentage The percentage of the maximum weight at which an alert will be generated for 
the RF operator in RFPIC. If the operator selects Yes at the Continue? prompt, 
he or she can pick the selected line even though it is overweight.
Parcel Carrier Notification 
Type
Reserved for future use
Number of Hours Before 
Ship Date to Force 
Replenishment Tasks
Only available if tasking is activated
In this field, you specify the number of hours before the ship date to “force” 
replenishment tasks. That is, create a replenishment task for a pick line location even if the pick line location is full and there is no room for the replenishment.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Outbound Process Configuration (CCCC)
CCCC screen
DOCUMENT MESSAGES BLOCK
In this block, you can attach a message code to a document code for a specific combination of customer/
carrier/consignee. This block is a further refinement of the document print messages logic in DPME.
If there are multiple messages attached to the same document, you can specify the sequence of messages 
appearing on the document by entering a sequence number in the Seq. No field.
Priority Value for Forced 
Replenishments
Only available if tasking is activated
In this field, you specify the priority value for forced replenishment tasks. The 
default value for all replenishments is 100. You can change it to a lower value 
(say, 50) so that it has a lower priority.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Warehouse Customer Consignee OPID Rule (WCCO)
Document Messages Block
Warehouse Customer Consignee OPID Rule (WCCO) 
In this program, you define your mix/no mix OPID rules for each warehouse/customer/consignee combination. The Allow Mixing Items in OPID flag in WCCO overrides your OPID Assignment Rules in CCCC. It 
also overrides your Single Item Per Outbound Pallet setting in CONS. Mix/no mix OPID rules apply to the 
programs RFPIC, RFPK, RFITLV and RFMG.
NOTE: If an order requires the generation of a SSCC label, item codes cannot be mixed.
WCCO screen
Customer/Consignee Outbound Rules (CCOR)
In this program, you define your outbound rules for various customer/consignee combinations. Outbound 
rules cover three major areas:
▪ allocation
▪ manual pallet building in RFPIC

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
▪ labeling requirements
CCOR is an optional program. If none of your customers and consignees use any of the options in this 
program, you do not need to set up any records in CCOR.
FIELD DESCRIPTIONS
Customer Code The customer for the outbound rules.
Consignee Code The consignee for the outbound rules.
Ship Newer Product Y = Yes
N = No
If you set this flag to Yes, allocation will only allocate product whose expiry 
date is greater than or equal to previously shipped inventory from that customer to that consignee.
OPID Inventory Level 
Optimization Type
Only available for manual pallet building in RFPIC
No Optimization (1)
Inventory Level 2 (2)
Inventory Level 3 (3)
Inventory Level 4 (4)
If you select 1, a single pallet can contain mixed product at all inventory levels; 
that is, different levels 1, 2, 3 and 4. If you select 2, all product on a single pallet must have the same level 2 value, but other inventory levels may differ. If 
you select 3, all product on a single pallet must have the same level 3 value, 
but other inventory levels may differ. If you select 4, all product on a single pallet must have the same level 4 value, but other inventory levels may differ.

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
OPID Expiry Date Optimization Type
Only available for manual pallet building in RFPIC
Not allow (1)
A single expiry date per OPID is allowed.
Allow based on specified dates (2)
You can specify a minimum number of shelf life days, a maximum number of 
shelf life days and/or a maximum number of days between your minimum and 
maximum number of shelf life days.
Allow based on number of shelf life days (3)
You can specify a minimum number of days to expiry.
Allow any dates (4)
Any expiry date is allowed on an OPID.
Minimum Number of 
Shelf Life Days
Only available if OPID Expiry Date Optimization Type = 2
If you enter a minimum number of shelf life days in this field (say, 10), all product on the same pallet must have a shelf life of at least 10 days.
Maximum Number of 
Shelf Life Days
Only available if OPID Expiry Date Optimization Type = 2
If you enter a maximum number of shelf life days in this field (say, 20), all 
product on the same pallet must have a shelf life of greater than 20 days.
Number of Days Between 
Min./Max. Dates
Only available if OPID Expiry Date Optimization Type = 2
In this field, you specify the maximum number of days between your minimum 
number of shelf life days and your maximum number of shelf life days. If there 
is a conflict between this value and your minimum/maximum number of shelf 
life days value, the more restrictive condition will apply.
Number of Days Between 
Multiple Expiry Dates in 
OPID
Only available if OPID Expiry Date Optimization Type = 3
If you enter a number in this field (say, 90), any product with an expiry date 
greater than 90 days can be mixed.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
Use Consignee Item 
Configuration
Y = Yes
N = No
If you set this flag to Yes, you can define outbound pallet quantity by consignee in ICOC. If you set this flag to No, outbound pallet quantity by consignee in ICOC is deactivated.
SSCC Label Required Y = Yes
N = No
If you set this flag to Yes, an SSCC label will be generated. If you set this flag 
to No, no SSCC label will be generated. This field overrides the Generate 
UCC-128 Sequence Number flag in CONS (Consignees).
Use Client SSCC Only available if SSCC Label Required = Yes
Y = Yes
N = No
If you set this flag to Yes, the following requirements must be met:
▪ the SSCC number is received via EDI
▪ it is assigned to an LPN
▪ a full pallet is picked
If you set this flag to No, the SSCC label will be generated by AccellosOne 
3PL.
Number of SSCC Labels 
to Print
Only available if SSCC Label Required = Yes
The number of SSCC labels to print.
Retail Ready Reserved for future use.
SSCC Number Range Only available if SSCC Label Required = Yes
Your number series for SSCC labels in NUSE (Number Series)
Print Customer Name Y = Yes
N = No
If you set this flag to Yes, the customer name will print on the e label. If you set 
this flag to No, the customer name will not print on the label.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
Print Inventory Level on 
Labels
No Printing (1)
Inventory Level 2 (2)
Inventory Level 3 (3)
Inventory Level 4 (4)
The inventory level to be printed on the label or No Printing.
Single Order per OPID Only available for manual pallet building in RFPIC
Y = Yes
N = No
If you set this flag to Yes, OPID’s will be restricted to product belonging to a 
single order. If you set this flag to No, an OPID can contain product from multiple orders.
The option that you select in this field overrides the option that you select in 
the OPID Assignment Rules field in CCCC.
MCP Label Required Y = Yes
N = No
If you select Yes, an MCP label is required. If you select No, an MCP label is 
not required.
Pick From Bulk if Order 
Qty. Over Set Percentage
Y = Yes
N = No
If you select Yes, allocation will pick from a non-pick line location when the 
order quantity is less than a full pallet but greater than the threshold percentage that you define. The remaining pallet quantity not needed to fill the order 
line will be relocated within bulk via a directed move.
If you select No, allocation will pick anything less than a full pallet from the 
pick line according to your rules in PIPR and PIIT.
Threshold Percentage Only available if Pick From Bulk … = Yes
The threshold percentage of a full pallet for picking from bulk. This calculation 
is based on the item's lowest SKU. If the item is a variable quantity breakdown 
item, the threshold percentage will be based on the variable quantity breakdown.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
Acceptable Range of 
Expiry Dates
Only available if Pick From Bulk … = Yes
The acceptable range of expiry dates between pick line stock and full pallet 
picks from bulk. A value of zero in this field means that the expiry date of the 
pick line stock must match exactly the expiry date of the full pallet stock in 
bulk.
For example, if you set this field to 15, allocation will only pick from bulk if the 
expiry date of product in bulk is within 15 days of the expiry date of product 
allocated from the pick line.
Pick Full Pallets Only Y = Yes
N = No
If you select Yes, allocation will pick from full pallet stock only and selection by 
FIFO will be deactivated if necessary. The definition of a full pallet is based on 
the following:
▪ if the Use Consignee Item Configuration flag is set to Yes, the quantity 
breakdown set up in ICOC (Item Consignee Configuration) will be used 
▪ if the Use Consignee Item Configuration flag is set to No, the quantity breakdown set up in ITEM will be used
CAUTION Because FIFO selection is deactivated, the Yes option may 
leave non-full pallet stock in the warehouse even if it is the oldest stock. And 
eventually this stock will expire.
FIELD DESCRIPTIONS

OUTBOUND SETUP PROGRAMS
Customer/Consignee Outbound Rules (CCOR)
CCOR screen showing default values
In the Item Outbound Rules Block, you define the threshold percentage and full pallet picking only rules for 
specific items when shipped to the consignee in the header block.
CCOR screen showing Item Outbound Rules Block

GENERAL NAVIGATION AND LOOK-UP 
PROGRAMS
Accessing RF .................................................................................................. 132
Changing Your Company ............................................................................... 132
Looking Up Inventory in RFIT ........................................................................ 132
Looking Up Inventory by Location in RFPR ................................................. 134
Looking Up Receipts in RFIL ......................................................................... 136
Looking Up Allocated Order Lines in RFOL ................................................. 138
Looking Up Inventory in RFLOIP................................................................... 141
Looking Up Locations in LOLORF ................................................................ 142
Looking Up Inventory in LOENRF ................................................................. 144
Looking Up Receipts in LORERF .................................................................. 145
Looking Up Orders in LOORRF ..................................................................... 147
Looking Up Reserve Logic Customers in RFLR .......................................... 148

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Accessing RF
Accessing RF
You access RF through an RF device. To access RF through an RF device, log onto Tera Term or some other 
terminal emulation software.
Changing Your Company
The company that you are currently working in is displayed on the RF Main Menu. If you wish to change this 
company, you key in your new company code and press Enter.
1 Enter the RF environment.

RF Main Menu
2 Check the company code in the top left-hand side of your screen.
3 If you wish to change companies, key in your new company code and press Enter. 
4 Proceed to enter the RF program that you wish to use.
Looking Up Inventory in RFIT
You look up your inventory in RFIT. For the item or items that you specify, RFIT shows the level 2, 3 and 4 
values, whether the item is on hold, the location in which the item is stored and the on-hand, on-order, onreceipt and available quantities.
You can enter up to six search criteria for any given query. For example, you can specify your customer code 
only and RFIT will show all product belonging to that customer. If you enter your customer code and item 
code, RFIT will show all product for the item that you specify. If you enter customer code, item code and level 
2 value, RFIT will show all product for the level 2 value that you specify.
current company

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Inventory in RFIT
If you enter no search criteria, RFIT will show all product in your warehouse regardless of customer.
1 Enter RFIT.

RF — Item Look-Up
2 Enter or scan in the appropriate search criteria. You can query by one or more of the parameters shown 
below. If you do not want to enter a parameter (for example, you want to look up all items regardless of 
level 2 and 3 values), press Enter to bypass the appropriate fields. You can query by one or more of the 
following:
▪ customer code 
NOTE You can only look up records in RFIT that have positive inventory. If you 
wish to look up inventory with zero balances, you must use LOEN (Look Up Inventory).
FUNCTION KEYS
Criteria Mode
F2 Eq (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria mode.
F4 Rt (Return to Main) Switch to Main Mode.
Main Mode
F1 En (Enter Criteria) Switch to Criteria Mode.
F4 Ex (Exit) Exit program.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Inventory by Location in RFPR
▪ item code
▪ level 2, 3 and 4 value
▪ hold code
3 When you finish entering your search criteria, press F2 to execute your query.

RFIT screen showing three records for item A1
4 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll 
forward and backward through the records that matched the criteria that you specified.
5 Press F1 to perform another query or press F4 to exit.
Looking Up Inventory by Location in RFPR
You can look up inventory by either item or by location in RFPR. For each item or location that you specify, 
RFPR shows the level 2, 3 and 4 values, whether the item is on hold, the location in which the item is stored 
and the available, on hand, on order and replenishment quantities.
There are two types of searches that you can do in RFPR: you can search for all inventory records including 
plus records or you can exclude plus records from your search results. A plus record is a temporary record 
generated by the system when you allocate an order for a reserve logic customer. The inventory levels that 
are unknown at the time of allocation are indicated by a plus sign.
If you query by location code and warehouse, the search results are sorted in customer code and levels 1/2/
3/4 sequence. If you query by any other criteria, the search results are sorted in location code, inventory 
access code sequence.
REQUIREMENTS
GENERAL If you set the Hide Quantity in RFPR flag in COMP to Yes, the quantity fields will 
be suppressed for non-supervisory users. If you set this flag to No, the quantity 
fields in RFPR will display for all users both supervisory and non-supervisory.
1 = current record 
displayed
3 = number of 
records that met the 
criteria that you 
specified 

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Inventory by Location in RFPR
1 Enter RFPR.

RF — Look Up Product and Location
2 Enter or scan in the appropriate search criteria. You can query by one or more of the following:
▪ customer code 
▪ item code
▪ level 2 and 3 value
▪ location and warehouse code
▪ hold code
3 When you finish entering your search criteria, do one of the following:
FUNCTION KEYS
All Modes
F1 EN (Enter Criteria) Switch to Criteria Mode.
F2 QU (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria mode. 
This query retrieves all eligible inventory 
records including plus records.
F3 QR (Query Reserve) Excludes plus records from your search 
results.
F4 EX (Exit) Exit program.
If you wish to look up all 
inventory including plus records:
If you wish to exclude plus 
records in your query results:
a) Press F2 (QU). a) Press F3 (QR).

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Receipts in RFIL

RFPR screen (record 40) showing available, on-hand, on order and replenishment quantities for location A103
The AV.Q field shows the available quantity, the OH.Q field shows the on-hand quantity, the ORD field 
shows the on order quantity and the REPI field shows the replenishment quantity.
4 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll 
forward and backward through the records that matched the criteria that you specified.
5 Press F1 to perform another query or press F4 to exit.
Looking Up Receipts in RFIL
You look up your allocated unconfirmed receipts in RFIL. If the receipt is confirmed or unallocated, you cannot 
look it up in RFIL. There are three options in RFIL:
▪ you can look up all allocated lines on an unconfirmed receipt
▪ you can look up all lines that have been staged but not put-away (if you do not stage your product, this 
option is not available) 
▪ you can look up all lines that have been put-away 
RFIL shows the quantity of each receipt line in the lowest SKU. For example, if your receipt line has a quantity 
of two pallets and there 60 cases to a pallet, the quantity in RFIL will read 120.
FUNCTION KEYS
Results Mode
F1 AL (All) Shows all staged/put-away receipt lines.
F2 RC (Received) Shows all receipt lines that have been 
staged but not put-away.
F3 PU (Put-Away) Shows all receipt lines that have been putaway but not confirmed.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Receipts in RFIL
1 Enter RFIL.

RF — RF Receipt Line Look-Up
2 Key in your receipt number and press Enter.
3 Press F1 (All) to display the first receipt line on the receipt.

Receipt 1204 showing line 1 of a five-line receipt
4 Use your arrow keys to scroll forward and backward to view each receipt line.
5 If you stage your product before you put it away, press F2 (Receiving) to view product that has been 
staged but not put-away.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F4 EX (Exit) Exit program.
FUNCTION KEYS
1 = current line 
displayed
5 = total number 
of lines on receipt

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Allocated Order Lines in RFOL

RFIL screen showing two lines of staged product
6 If you have multiple lines of staged product, use your arrow keys to scroll forward and backward to view 
each line.
7 Press F3 (Put-Away) to view product that has been put-away.

RFIL screen showing three lines of product that have been put away
8 If you have multiple lines of product that have been put-away, use your arrow keys to scroll forward and 
backward to view each line.
9 When you finish looking up your receipt, press F4 the required number of times to exit.
Looking Up Allocated Order Lines in RFOL
You look up your allocated unconfirmed order lines in RFOL. If the order line is confirmed, you cannot look it 
up in RFOL. For each order line that you look up, RFOL shows the order number, customer code, line 
number, warehouse code, location type, up to four inventory levels, hold code (if any), quantity, location and 
OPID (if any). Locations with a quantity of zero are not shown.
There are three options in RFOL:

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Allocated Order Lines in RFOL
▪ you can look up all unconfirmed order lines (that is, the order is either allocated or picked)
▪ you can look up unconfirmed order lines that have been allocated but not picked 
▪ you can look up unconfirmed order lines that have been picked
Order line records in RFOL are sorted by order number followed by location code.
1 Enter RFOL.

RF — Order Line Look-Up
NOTE The allocated and picked options in RFOL always show the allocated and 
picked lines for the currently selected order. If you wish to look up all allocated or 
picked lines regardless of order, you must start a new query. You cannot query on all 
allocated or picked lines if there is an order displayed on your screen.
FUNCTION KEYS
Results Mode
F1 AL (All) Shows all order lines that have been either 
allocated or picked.
F2 AO (Allocated) Shows all order lines that have been allocated but not picked.
F3 PI (Picked) Shows all order lines that have been 
picked but not confirmed.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F4 EX (Exit) Exit program.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Allocated Order Lines in RFOL
2 Enter or scan in the appropriate search criteria. You can query by one or more of the parameters shown 
below. If you do not want to enter a parameter (for example, you want to look up all orders regardless of 
warehouse), press Enter to bypass the field.
▪ order number 
▪ warehouse code
▪ location type code
3 After pressing Enter in the Location Type field, press F1 (All) to display the first order line on the first 
order. 

Order Line Look-Up showing ALL option
4 Use your arrow keys to scroll forward and backward to view each order line on each unconfirmed order.
5 Press F2 (Allocated) to view the order lines for the currently selected order that have been allocated.

Order Line Look-Up showing allocated lines for order 1512
6 Use your arrow keys to scroll forward and backward to view each order line that has been allocated.
7 Press F3 (Picked) to view the order lines of the currently selected order that have been picked.
1 = current record 
displayed
133 = total number of order lines 
for all unconfirmed orders
There are two allocated lines for order 
1512

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Inventory in RFLOIP

Order Line Look-Up showing picked lines for order 1528
8 When you finish viewing your orders, press F4 the required number of times to exit.
Looking Up Inventory in RFLOIP
This program allows you to look up inventory information by scanning in a serial number from a bar code 
label. For each serial number, RFLOIP shows the customer code, up to four inventory levels, the warehouse 
and location, and the on-hand and available quantities. You can scan in the entire bar code label or you can 
manually key only the serial number portion of the bar code. 
You cannot look up serial numbers if the product is on a confirmed order.
1 Enter RFLOIP.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria mode.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F1 EN (Enter Criteria) Switch to Criteria Mode.
F4 EX (Exit) Exit program.
There are three lines 
that have been picked 
for order 1528

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Locations in LOLORF

RF — Look Up Item Process
2 Enter or scan in your serial number.

RF — Look Up Item Process showing inventory information for serial number 0001
3 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll 
forward and backward through the records that matched the criteria that you specified.
4 Press F1 to perform another query or press F4 to exit.
Looking Up Locations in LOLORF
This RF look-up program is similar to the non-RF program LOLO (Look Up Location Information). It is 
designed to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel 
full access to AccellosOne 3PL’s location information. 
Refer to the Operations 1 Guide for detailed information on LOLO.
1 Enter LOLORF.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Locations in LOLORF

RF - Look Up Location
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the location(s) that you selected, press F3 (Inventory Block) to see the 
inventory in the location(s).

RF - Look Up Location
4 When you finish looking up; your location, press F4 (Location) and then F4 (Exit).

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Inventory in LOENRF
Looking Up Inventory in LOENRF
This RF look-up program is similar to the non-RF program LOEN (Look Up Entity Information). It is designed 
to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access 
to AccellosOne 3PL’s location information. 
Refer to the Operations 1 Guide for detailed information on LOEN.
1 Enter LOENRF.

RF - Look Up Entity Information
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the inventory that you selected, press F3 (Location Block) to see the 
inventory in the location(s).

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Receipts in LORERF

RF - Look Up Entity Information
4 When you finish looking up your inventory, press F4 (Inventory) and then F4 (Exit).
Looking Up Receipts in LORERF
This RF look-up program is similar to the non-RF program LORE (Look Up Receipts). It is designed to be 
viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to 
AccellosOne 3PL’s receipt information. 
Refer to the Operations 1 Guide for detailed information on LORE.
1 Enter LORERF.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Receipts in LORERF

RF - Look Up Receipts
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the receipts that you selected, press F3 (Line Block) to see the receipt 
lines.

RF - Look Up Receipts
4 When you finish looking up your receipts, press F4 (Receipt Block) and then F4 (Exit).

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Orders in LOORRF
Looking Up Orders in LOORRF
This RF look-up program is similar to the non-RF program LOOR (Look Up Orders). It is designed to be 
viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to 
AccellosOne 3PL’s order information. 
Refer to the Operations 1 Guide for detailed information on LOOR.
1 Enter LOORRF.

RF - Look Up Orders
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the orders that you selected, press F3 (Line Block) to see the order 
lines.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Reserve Logic Customers in RFLR

RF - Look Up Orders
4 When you finish looking up orders, press F4 (Order Block) and then F4 (Exit).
Looking Up Reserve Logic Customers in RFLR
You look up inventory by location for reserve logic customers in RFLR. For each location that you specify, 
RFLR shows the on-hand, on order replenishment and available quantities at the inventory level that the 
customer reserves at. For example, if a three-level customer reserves at level 2 (lot number), RFLR will show 
quantities for each unique lot in a given location.
Locations in which the available quantity is less than or equal to zero are not shown and inventory on hold is 
not included in the location quantities.
If your query retrieves multiple locations, locations are sorted by the expiry date of product in the location.
FUNCTION KEYS
Criteria Mode
F2 Eq (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria mode.
F4 Ex (Exit) Exit program.
Main Mode
F1 En (Enter Criteria) Switch to Criteria Mode.

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Reserve Logic Customers in RFLR
1 Enter RFLR.
RF — Look Up Reserve Logic Customer
2 Key in your level 1 value and press Enter. If two customers have the same item code, a pick list will display. Use your arrow keys to position the cursor over the item code that you wish to look up and press 
Enter to select it.
3 If required, key in your level 2 value and press Enter.
4 If you have four inventory levels and reserve at level 3, you can key in a level 3 value and press Enter.
5 If required, key in your location code and press Enter.
6 If required, key in your warehouse code and press Enter.
7 When you finish entering your search criteria, press F2 (Qu) to query.

RF — Look Up Reserve Logic Customer showing level 2 quantities for location S100
8 If your query retrieves multiple locations, use your arrow keys to scroll through the list of locations.
9 When you finish looking up your reserve logic inventory by location, press F4 twice to exit.
F3 RL (Relocate) Enter RFRL to perform a relocate.
F4 Rt (Return to Main) Switch to Main Mode.
FUNCTION KEYS

GENERAL NAVIGATION AND LOOK-UP PROGRAMS
Looking Up Reserve Logic Customers in RFLR

INBOUND PROCESSING
Overview of Put-Away .................................................................................... 152
Understanding Inbound Flows in RF ............................................................ 153
Overview of the Unique Identifier (UI) ........................................................... 153
Unloading Product in RFCH........................................................................... 154
Entering Trailer and Pallet Information ...................................................... 170
Performing Queries.................................................................................... 174
Overriding the System-Assigned Location................................................. 169
Entering Partial U-Type Receipt Lines....................................................... 175
Printing Labels ........................................................................................... 176
Understanding Variances in RFCH............................................................ 177
Processing Variances ................................................................................ 178
Entering Process Values............................................................................ 180
Validating Process Values ......................................................................... 182
Creating a New Line .................................................................................. 183
Receiving Product Under an Alternate Item Code ..................................... 184
Receiving Product on Automatic Hold ....................................................... 186
Receiving Product with a Variable Product Breakdown............................. 187
Receiving Mixed Product ........................................................................... 187
Looking Up Temperature and Trailer Information in LORE ....................... 189
Looking Up Remarks and Messages in RFCH .......................................... 190
Entering Temperature and Trailer Information in RFTT .............................. 191
Putting Away Product in RFPU...................................................................... 192
Overriding the System-Assigned Location................................................. 198
Entering Variances..................................................................................... 199
Putting Away Product Under an Alternate Item Code................................ 201
Putting Away in a Pick Line Location ......................................................... 202
Entering Process Values in RFIPS ................................................................ 202
Capturing the Weight Dynamically from a Bar Code ................................. 204
Deleting a Receipt Line in RFDL.................................................................... 208
Clearing Tie/Hi/Loose Variances in RFCV .................................................... 210

INBOUND PROCESSING
Overview of Put-Away
Overview of Put-Away
There are two ways of putting away product in AccellosOne 3PL:
▪ In two-step put-away, you unload the receipt and use RFCH to place the product in a staging location and then perform final put-away in RFPU. If auto-confirmation is activated in DIFP, no confirmation 
of the receipt is required in CHRF (Time-Stamp and Confirm Receipt).
▪ In one-step put-away, you unload the receipt and use RFCH to put-away the product in a final nonstaging location with no processing in RFPU. After final put-away in RFCH, you must confirm the receipt 
in CHRF (Time-Stamp and Confirm Receipt).
If your flows are correctly defined in DIFP, you can switch from one-step put-away to two-step put-away or 
from two-step put-away to one-step put-away as often as required within the same account. 
If you are performing two-step put-away,
you put away the product in RFPU (RF PutAway).
WAREHOUSE
If you are performing one-step put-away,
you put away the product in a final nonstaging location. If you are performing twostep put-away, you put away the product in
a staging location.
RFCH
OFFICE
You enter the receipt in ENRE (Enter,
Modify and Delete Receipt).
CHRF
One-step putaway? No Yes
RFPU
CHRF
ENRE
OFFICE
You confirm the receipt in CHRF (TimeStamp and Confirm Receipt).
OFFICE
You advance the receipt's flow to DRDO
(driver arrived at door) in CHRF (TimeStamp and Confirm Receipt).
WAREHOUSE
You unload the receipt in RFCH (RF
Check/Unload).
1
2
3
4
5

INBOUND PROCESSING
Understanding Inbound Flows in RF
Understanding Inbound Flows in RF
In non-RF receiving, you time-stamp and advance the flow of a receipt in CHRF (Time-Stamp and Confirm 
Receipts). Advancing the flow of a receipt in CHRF advances the flow of all receipt lines and receipt location 
lines on the receipt. You cannot advance the flow of one receipt line and leave another receipt line remain at 
its original flow.
In RF receiving, on the other hand, AccellosOne 3PL automatically advances the flow of individual receipt 
lines and receipt location lines. For example, when you unload product in RFCH, the receipt line’s flow is 
automatically advanced from STUN (Start Unloading) to INST (Inbound Staged). Because the flow of 
individual receipt lines is advanced as each receipt line is unloaded, not all lines on a given receipt will be at 
the same flow. When this happens, the receipt header will show the earliest flow on the receipt.
For example, suppose there are five receipt lines on a given receipt: two lines are at the flow STUN, two lines 
are at the flow INST and one line is at the flow STPU (Start Put-Away). If you look up the receipt in LORE, the 
receipt’s flow will be set to STUN, which is the earliest flow.
Overview of the Unique Identifier (UI)
The unique identifier (UI) is a single value that represents an inventory entity defined down to the lowest 
inventory level. For example, the UI value of ABC001 could represent item A1, lot 101, pallet ID 10 belonging 
to customer A.
Unique Identifiers make it possible to enter a single value in the core RF program such as RFCH, RFPU, 
RFRL, RFRP and RFPIC that identifies the product that you are working with. When you enter this value, 
AccellosOne 3PL automatically populates the customer code and inventory level fields with the correct 
values.
AccellosOne 3PL can automatically generate these values when you receive inventory in ENRE or you can 
manually create the values yourself.

RFCH screen showing UI value of GN000286 that identifies three inventory levels

INBOUND PROCESSING
Unloading Product in RFCH
Unloading Product in RFCH
In this program, you unload your receipt and place it either in a staging location (if you are going to perform 
final put-away in RFPU) or in a non-staging location (if you are performing one-step put-away with no 
processing in RFPU). Your receipt must be at the flow DRDO (Driver Arrived) before you can unload it. If the 
product that you are receiving is not on the original receipt, you can create a new line for the product in 
RFCH.
RFCH supports two types of receipt lines:
▪ P type in which AccellosOne 3PL generates your pallet ID or you enter your pallet ID’s manually during 
receipt entry in ENRE (for the purposes of RF, P type includes the following line types in ENRE: I for InTransit, H for Handling Only and S for Storage Only)
▪ U type in which inventory level 2 or higher is unknown at the time of receipt entry (also known as blind 
receiving)
With P-type lines (that is, all inventory levels have been entered in ENRE), you can enter your lowest 
inventory level and RFCH will retrieve the receipt number and all other inventory levels. With U-type lines 
(that is, one or more inventory levels have not been entered in ENRE), you must enter your receipt number 
and all inventory levels. 
NOTE Depending on how you track your customers’ inventory, the unique identifier 
may or may not be unique across customers. For example, suppose you have two 
customers: customer A whose inventory is tracked by item code/lot number/pallet ID 
and customer B whose inventory is tracked by item code and lot number. Customer A 
could have “001” as the unique identifier representing a particular pallet ID and customer B could have “001” as the unique identifier representing a particular lot number.
When this happens, if both inventory entities are on open receipts at the appropriate 
flow, entering “001” in the UI field of RFCH will result in pick list from which the RF 
operator must select the appropriate inventory. 
CAUTION RFCH does not support multiple operators working on the same receipt 
when these operators are working in different modes. If you allow multiple operators 
to work on the same receipt, make sure that all operators are working in the same 
mode — either unload mode or put-away mode.

INBOUND PROCESSING
Unloading Product in RFCH
REQUIREMENTS — GENERAL
FLOWS DRDO (Driver Arrived at Door)
STUN (Start Unloading)
INST (Inbound Staged)
STPU (Start Put-Away)
PUCO (Put-Away Complete)
INVENTORY LEVELSYou can process up to four inventory levels in RFCH.
PROCESS VALUESIf you wish to scan in a catch weight and serial number, you require two process 
values: one for catch weights and one for serial numbers. These codes must be 
set up in IPRO (Item Process) with the Create Automatic Records flag set to Y for 
Yes and then attached to a profile in IPRP (Item Process Profile). The IPRP profile must in turn be attached to the item(s) requiring the process values.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEOnly required if you are scanning process values, inventory levels or UI values 
from a bar code label
You need a scan parameter profile defined in SCPR (Scan Parameter Code). 
This profile must contain a minimum of two records in the Detail Block: one record 
for your scanned in weight and another record for your scanned in serial number. 
The SCPR profile must in turn be attached to the item requiring the process values.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code 
label
You must define a bar code profile in BAPR and attach to it the scan parameter 
code that you set up in SCPR.
DOCUMENTS The Print Document Without Assigning Locations flag in DOCU (Documents) 
must be set to Yes for all receipt-related documents such as the tally.

INBOUND PROCESSING
Unloading Product in RFCH
OTHER If you want AccellosOne 3PL to generate your pallet ID’s or other inventory levels, 
you must set the Method of Generating/Validating Values flag in DILP (Depositor 
Inventory Level Profile) to W for Warehouse for that level. As well, the Warehouse 
Code field in the receipt header must be populated. See the Setup Guide for 
further information on DILP and DIAP.
If you wish to define a default staging and put-away warehouse, you can enter a 
warehouse code in either the header block of ENRE (for a given receipt) or in 
CUST (for all receipts for a given customer). If you enter a default warehouse 
code in both ENRE and CUST, the ENRE code will override the CUST code.
If you wish to display a depositor print message set up in DPME, attach a document code of TALY to your message code in DPME. DPME messages for RFCH 
require specific customer/carrier/shipper combinations; you cannot use the “.ALL” 
codes.
NOTE A DPME message for RFCH does not actually print unless you set up a 
real tally document in DOCU and then attach this tally document to an inbound 
flow in DIFP.
RESTRICTIONS RFCH does not support lines that have been partially received in ENRE. A line is 
considered partially received if you add a location line record in ENRE to a receipt 
line and the quantity of the location line is less than the full number of units for the 
receipt line.
REQUIREMENTS — One-Step Manual Put-Away (1)
In one-step manual put-away, you unload your receipt and place it in a final non-staging location with no 
processing in RFPU. The mode for one-step put-away in RFCH is P for Put-Away and the non-staging 
location is manually selected by the operator.
FLOWS For one-step manual put-away, the Assign Location flag in DIFP must be set as 
follows:
ENRE = Y
DRDO = N
STUN = N/A
INST = N/A
STPU = N
PUCO = N
CORE = N/A
NOTE If you wish to perform two-step put-away for some receipts and onestep put-away for other receipts, use the flow settings for two-step put-away.
REQUIREMENTS — GENERAL

INBOUND PROCESSING
Unloading Product in RFCH
AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a 
new flow and attach it to your inbound flow profile. This flow must be placed 
before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must 
be set to Y for Yes.
REQUIREMENTS — One-Step Directed Put-Away (2)
In one-step directed put-away, you unload your receipt and place it in a final non-staging location with 
no processing in RFPU. The mode for one-step put-away in RFCH is P for Put-Away and the non-staging location is selected by the system. Directed put-away requires special setup in ILOP (Item Location 
Profile) and other programs. See the Allocation and Wave Manager for further information.
FLOWS For one-step directed put-away, the Assign Location flag in DIFP must be set as 
follows:
ENRE = Y
DRDO = Y
STUN = N/A
INST = N/A
STPU = Y
PUCO = Y
CORE = N/A
NOTE If you wish to perform two-step put-away for some receipts and onestep put-away for other receipts, use the flow settings for two-step put-away.
AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a 
new flow and attach it to your inbound flow profile. This flow must be placed 
before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must 
be set to Y for Yes.
OTHER Put-away parameters must be defined in ILOP (Put-Away).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Manual PutAway (3)
In two-step put-away, you unload your receipt and place it in a staging location before performing final 
put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and both the staging and 
non-staging locations are manually selected by the operator. 
REQUIREMENTS — One-Step Manual Put-Away (1)

INBOUND PROCESSING
Unloading Product in RFCH
FLOWS For two-step put-away with manual staging, the Assign Location flag in DIFP 
must be set as follows:
ENRE = N
DRDO = N
STUN = N
INST = N
STPU = N
PUCO = N
CORE = N/A
REQUIREMENTS — Two-Step Put-Away with Directed Staging and Manual PutAway(4)
In two-step put-away, you unload your receipt and place it in a staging location before performing final 
put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and the staging location is 
selected by the system while the final non-staging location is selected by the operator. Directed staging 
requires special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave 
Manager Guide for further information.
FLOWS For two-step put-away with directed staging, the Assign Location flag in DIFP 
must be set as follows:
ENRE = N
DRDO = Y
STUN = Y
INST = N
STPU = N
PUCO = N
CORE = N/A
ALLOCATION Directed staging requires warehouse zones set up in WHZO (Warehouse Zone 
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER Directed Move Inbound parameters must be defined in ILOP (Directed Move 
Inbound).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Manual PutAway (3)

INBOUND PROCESSING
Unloading Product in RFCH
REQUIREMENTS — Two-Step Put-Away with Directed Staging and Directed 
Put-Away (5)
In two-step put-away, you unload your receipt and place it in a staging location before performing final 
put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and both the staging and 
final locations are selected by the system. Directed put-away requires special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave Manager Guide for further information.
If you switch from two-step put-away to one-step put-away in RFCH and if you are processing a P-type 
line, AccellosOne 3PL will use your directed move parameters rather than your directed put-away 
parameters.
FLOWS For two-step put-away with directed staging and put-away, the Assign Location 
flag in DIFP must be set as follows:
ENRE = N
DRDO = Y
STUN = Y
INST = Y
STPU = Y
PUCO = Y
CORE = N/A
ALLOCATION Directed put-away requires warehouse zones set up in WHZO (Warehouse Zone 
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER The following parameters must be defined: Directed Move Inbound in ILOP 
(Directed Moved Inbound) and Put-Away in ILOP (Put-Away).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Directed PutAway (6)
In two-step put-away, you unload your receipt and place it in a staging location before performing final 
put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and the staging location is 
selected by the operator while the final location is selected by the system. Directed put-away requires 
special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave Manager Guide for further information.

INBOUND PROCESSING
Unloading Product in RFCH
FLOWS For two-step put-away with manual staging and directed put-away, the Assign 
Location flag in DIFP must be set as follows:
ENRE = N
DRDO = N
STUN = N
INST = Y
STPU = Y
PUCO = Y
CORE = N/A
ALLOCATION Directed put-away requires warehouse zones set up in WHZO (Warehouse Zone 
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER Put-Away parameters must be defined in ILOP (Directed Move Inbound).
REQUIREMENTS — Three-Step Put-Away (7)
In three-step put-away, the product is received and staged on the dock, moved to a PnD location by a 
forklift operator and then moved to a final put-away location by a narrow aisle equipment (VNA) operator.
You set up your final put-away locations in the Location Block of WHZO (Warehouse Zones).
FLOWS For three-step put-away with manual staging and directed put-away, the Assign 
Location flag in DIFP must be set as follows:
ENRE = N
DRDO = N
STUN = N
INST = Y
STPU = Y
PUCO = Y
CORE = N/A
ALLOCATION Three-step put-away requires warehouse zones set up in WHZO (Warehouse 
Zone Codes). The zone type code must be set to P (PnD) or S (Sorting) and the 
PnD location must be defined in the Header Block of WHZO.
An initial staging location on the dock is also required.
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Directed PutAway (6)

INBOUND PROCESSING
Unloading Product in RFCH
LOTP The PnD location’s location type must be set up in LOTP as follows:
.
OTHER Put-Away parameters must be defined in ILOP (Directed Move Inbound).
MRFP In the Special Receiving Mode Types field in MRFP, you select from the following 
three-step put-away options:
▪ RFCH to General Staging Location, RFPU to a PnD Location, then to Final 
Location
▪ RFCH to Gen Stag Loc, RFPU to PnD Loc, then to Final Loc, RFCH Overrides
If you select the first option, three-step put-away is mandatory in RFCH. If you 
select the second option, the RF operator can select either two-step or three-step 
put-away in RFCH.
In the Picking Rules for PnD Locations field in MRFP, you define your pick methods for these types of locations: full pallet picks only or all pick methods.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria mode.
F4 EX (Return to Main) Switch to Main Mode.
REQUIREMENTS — Three-Step Put-Away (7)

INBOUND PROCESSING
Unloading Product in RFCH
1 Make sure that your receipt is at the flow DRDO or STUN.
2 Enter RFCH.

RFCH screen
Results Mode
F1 CL (Create Line) Create a new line.
F1 RM (Remark) Show remark(s) entered in ENRE.
F2 PL (Print Label) Print labels.
F3 CM (Change Mode) Switch between put-away mode and 
unload mode.
F3 CR (Close Receipt) Close a receipt with unprocessed lines. 
Supervisor access required.
F4 RT (Exit) Switch to Main Mode.
F9 Move cursor to previous field.
Main Mode
F1 PL (Print Label) Print labels.
F2 QS (Query) Query receipts.
F4 EX (Exit) Exit program.
FUNCTION KEYS

INBOUND PROCESSING
Unloading Product in RFCH
3 Do one of the following:
If you are processing a P-type 
line:
You have two options: 
a) You can enter or scan in your UI (Unique Identifier) 
value and AccellosOne 3PL will retrieve the receipt 
number and up to four inventory levels for that UI 
value. If you have the same UI value on multiple 
receipts, a pick list will appear showing the receipt 
number and level 1/2/3/4 values. Use your arrow 
keys to position the cursor over the receipt that you 
wish to process and press F3 to select it.
b) You can bypass the UI field and enter the receipt 
number and level 1, 2, 3 and 4 values yourself. 
If you are processing a U-type 
line from ENRE with no systemgenerated inventory levels:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Key in your level 1 value for the first product that you 
wish to receive and press Enter.
d) Key in your level 2 value and press Enter.
e) Key in your level 3 value and press Enter.
f) If required, key in your level 4 value and press Enter.
If you are processing a U-type 
line from ENRE with the lowest 
inventory level system generated:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Key in your level 1 value for the first product that you 
wish to receive and press Enter.
d) Repeat the above step for each additional inventory 
level until you reach your lowest level.
e) When you reach your lowest inventory level, you 
have two options: you can manually enter it and 
press Enter as you did with your higher inventory 
levels or you can press Enter with the field blank 
and AccellosOne 3PL will generate a number for 
you.
If you are processing a U-type 
line from ENRE and you are 
scanning in your inventory levels from one or more bar code 
labels:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Scan in your level 1, 2 and 3 values from the appropriate label. If RFCH displays a pick list of bar code 
labels, select the appropriate label from the pick list.
If you do not know the UI number or receipt number:a) See “Performing Queries” on page 174.

INBOUND PROCESSING
Unloading Product in RFCH
4 Do one of the following:
RFCH screen showing prompt for tie and hi
5 Depending on your system setup, RFCH will be preset to either put-away mode or unload mode. If 
required, you can press F3 (CM) to toggle between the two modes.
Once you process a receipt line, the mode is set for all remaining lines on the receipt and cannot be 
altered until you start a new receipt.
If manual entry of expiry dates is 
activated for the item and you are 
receiving a U-type line:
If manual entry of expiry dates is 
NOT activated for the item:
a) The following screen will appear:
b) Key in your expiry date in the format displayed on your screen 
and press Enter.
a) Proceed to next step.
NOTE If you have manually entered a location in ENRE for one receipt line belonging to a multi-line receipt, the mode for the remaining receipt lines will be preset to 
put-away and cannot be changed. To switch to unload mode, you will have to remove 
the location from the receipt line in ENRE and then return to RFCH.
MODE field shows current 
mode: 
P = Put-Away (one-step)
U = Unload (two-step)

INBOUND PROCESSING
Unloading Product in RFCH
6 Do one of the following:
7 If the quantity entered does not match the expected quantity, a warning message will appear (“Qty 
Entered Does Not Match Expected Qty. Do You Want to Continue (Y/N)”) and you will be prompted to 
either continue with the current receipt or work on another receipt.
8 Do one of the following: 
9 If F1 (Rm) is available, the receipt has remarks. You can press F1 to view the remarks and then press F4 
to exit the Remarks Block.
If you wish to enter your tie, hi 
and loose values and let 
AccellosOne 3PL calculate the 
quantity:
If you wish to enter the total 
quantity directly:
a) Key in your tie and press Enter.
b) Key in your hi and press Enter 
again.
c) If you have loose quantities, key 
in your loose quantity and press 
Enter. If you do not have loose 
quantities, press Enter with the 
L(oose) field blank to bypass this 
option.
Depending on your setup in MRFP, 
the quantity may or may not be displayed in the Qty field.
a) Press Enter to bypass the T(ie) 
field.
b) Key in your quantity and press 
Enter. You can enter your quantity in pallets, eaches or any 
other SKU type that is activated 
in the item’s quantity breakdown. 
If your default SKU type is 
eaches and you wish to enter a 
quantity of 10 pallets, you would 
key in 10P for 10 pallets.
c) If the quantity is already displayed, press Enter to accept it 
or key in a new quantity and 
press Enter.
If the item that you are receiving 
requires the entry of a process 
code value:
If the item that you are receiving 
does NOT require the entry of a 
process code value:
a) Refer to the section “Entering 
Process Values” on page 180 for 
further instructions.
a) Proceed to next step.

INBOUND PROCESSING
Unloading Product in RFCH
10 Do one of the following:
11 Proceed to assign a location to the product as follows. If you are working in unload mode, the product 
must be placed in a staging location. A staging location is a location whose location type in LOTP is 
called STAG. This STAG code must have the Staging flag set to Y for Yes. 
If you are working in put-away mode, the product must be placed in a non-staging location. A non-staging 
location is a location whose location type in LOTP has the Staging flag set to N for No.
If there is no automatic hold 
placed on the item:
If there is an automatic hold 
placed on the item and manual 
overrides of holds are 
activated:
If there is an automatic hold 
placed on the item and manual 
overrides of holds are NOT 
activated:
a) If required, key in your manual 
hold code and press Enter. If 
you do not want to place the 
product on hold, press Enter 
to bypass this field.
a) If required, you can manually 
override or remove the hold 
code. Make any necessary 
changes and press Enter or 
press Enter without making 
any changes to accept the 
automatic hold.
a) The cursor will skip past the 
Hold field and you will not be 
able to override or remove the 
hold code.

INBOUND PROCESSING
Unloading Product in RFCH
If directed staging/put-away is 
activated on your system:
If directed staging/put-away is 
NOT activated on your system:
AccellosOne 3PL will display the 
system-assigned warehouse and 
location. You can accept the system-assigned warehouse and location or you can enter a different 
warehouse and location
If you wish to override the systemassigned location, see “Overriding 
the System-Assigned Location” on 
page 169.
RFCH screen showing systemassigned warehouse and location
a) Press Enter to accept the system-assigned location.
b) Press Enter again to accept the 
warehouse that the systemassigned location belongs to.
a) Key in your location and press 
Enter.
b) If required, key in your warehouse and press Enter.
c) If you wish to change your location code, press F9 to return to 
the L(oc) field. Then repeat steps 
a and b. 

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen showing prompt for next UI
12 If required, you can press F9 to return to the Hold field and place the product on hold.
13 Repeat the above steps for any additional UI’s or receipt lines.
14 When you finish entering all the lines on the receipt, do one of the following:
If you have fully entered all 
lines on the receipt:
If you are an operator (or nonsupervisor) and you have NOT 
fully entered all lines on the 
receipt:
If you are a supervisor, if you 
have NOT entered all lines on 
the receipt and if you press F3 
(CR):
a) Proceed to next step. The following message will appear: 
RFCH screen showing prompt to 
complete process
a) Press Enter to exit the receipt 
line. You can return to RFCH 
at any time and resume processing the receipt line.
The following message will appear: 
RFCH screen showing warning 
for not all lines processed
a) If you key in Y for Yes to proceed, the system will zero out 
any lines not unloaded or putaway, advance to the next flow 
and check for variances. If you 
key in N for No, proceed to 
enter the missing lines.

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen showing “Receipt completed?” message
15 Key in the appropriate option (1 to mark the receipt as complete, 2 to add a new line or 3 to exit and 
return at a later time to add a new line) and press Enter.
16 Process another receipt or press F4 to exit.
OVERRIDING THE SYSTEM-ASSIGNED LOCATION
There are three options for overriding the system-assigned location for a receipt line depending on your setup 
in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to No, an operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to Yes, changing a location must be approved by a supervisor
▪ if the Reason Code Required to Override System-Assigned Location flag in MRFP is set to Yes, the RF 
operator will be required to enter a reason code
1 Enter your receipt in RFCH in the normal manner.

RFCH screen showing system-assigned location
2 Key in your new location and press Enter.

INBOUND PROCESSING
Unloading Product in RFCH
3 Do one of the following:
4 Proceed to process the receipt normally in RFCH.
ENTERING TRAILER AND PALLET INFORMATION
If trailer and pallet information entry is activated in MRFP (RFCH Only tab) by setting the Show Temperature 
and Pallet Blocks flag to the appropriate option, you will be prompted to enter trailer and pallet information for 
the receipt. If the Perform Trailer Checks flag in MRFP is set to Yes, you will be prompted to perform a series 
of trailer checks.
Any trailer and temperature information that you enter in RFCH for a given receipt can be viewed in the 
Carrier Details Block of ENRE and LORE. Likewise, any pallet information that you enter in RFCH can be 
viewed in Pallet Details Block of ENRE and LORE.
1 When you finish processing all UI’s or receipt lines, the following screen will appear:
If supervisor authorization is 
activated:
If supervisor authorization is 
NOT activated:
The following screen will appear:

a) Key in Y for Yes and press Enter 
to proceed with the location override. If you do not wish to proceed with the override, key in N
for No and press Enter to return 
to the main RFCH screen.
b) Have a supervisor log in to 
approve the location override.
The following screen will appear:

a) Key in Y for Yes and press Enter 
to proceed with the location override. If you do not wish to proceed with the override, key in N
for No and press Enter to return 
to the main RFCH screen.
b) Press Enter again to accept the 
warehouse that the systemassigned location belongs to.

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen showing prompt for temperature
2 Do one of the following:
3 If the entry of trailer checks is activated in MRFP, you will be prompted to perform a series of trailer 
checks.

RFCH screen showing trailer check
4 Proceed to respond with either a Yes or a No to each trailer check.
If you wish to record the 
temperatures and trailer number 
for the load:
If you do NOT wish to record the 
temperature and trailer number 
for the load:
a) Key in the required number of 
temperatures for your trailer and 
press Enter. You can skip a particular temperature by pressing 
Enter with the field blank.
b) If required, key in your trailer 
number and press Enter. If you 
do not wish to enter a trailer 
number, press Enter to exit the 
Temperature/Trailer prompt.
c) If required, key in your seal number and press Enter.
a) Press F4 to exit.
b) Proceed to step 15. You will not 
be prompted to enter pallet information.

INBOUND PROCESSING
Unloading Product in RFCH
5 If the Pallet Block appears, do one of the following:

RFCH screen showing the Pallet Block
6 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick 
list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate 
code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
7 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
8 Key in your pallet code and press Enter or use your pick list to select it.
9 Key in the number of pallets that you are shipping or receiving and press Enter.
If you wish to record pallet 
information for the load:
If you do NOT wish to record 
pallet information for the load:
a) Proceed to next step. a) Press F4 the required number of 
times to exit the Pallet Block.
b) When the temperature and trailer 
number prompts redisplay, press 
F4 to exit. Then proceed to step 
15.
Received Received means that you are receiving pallets from the 
account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the 
account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even 
exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 
of your own pallets so that there is no change to your 
pallet balances.

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen showing prompt for reference information
10 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not 
require a remark, press Enter to bypass this field.
11 If required, repeat the above steps to add additional lines in the Pallet Block.
12 When you finish adding your lines, press F4 to exit Create Mode. AccellosOne 3PL will display the last 
pallet details record that you entered. If you have multiple pallet transactions for this receipt, you can use 
your up and down arrow keys to scroll through the list of records.
If you wish to delete a pallet transaction, select the transaction that you wish to delete with your arrow 
keys. Then press Enter until your cursor is positioned in the NUM PALL field and press F2 (DE).
13 Press F4 again to exit the Pallet Block.
AccellosOne 3PL will redisplay the prompt for the temperature and trailer number.
14 Press F4 to exit this screen.

RFCH screen showing message that receipt has been processed
15 Press Enter to close the “Process Complete” message. If prompted to mark the receipt as completed or 
to create a new line, key in Y for Yes to complete the receipt and press Enter.
16 Press F4 to exit.

INBOUND PROCESSING
Unloading Product in RFCH
PERFORMING QUERIES
The query function in RFCH allows you to query by receipt number, receipt line number, customer, inventory 
level, warehouse, hold code and shipper. In order to query a receipt in RFCH, the receipt must be at the flow 
DRDO (Driver Arrived at Door) without being fully staged or put-away. 
You can customize the values that appear in the query results screen by setting the appropriate flags in 
MRFP (RF Profile Code) to Yes. For example, if you wish to see the customer code and level 1 value only in 
the query results, you would set the Show Customer Code in RFCH Query and Show Inventory Level 1 in 
RFCH Query fields to Yes.
1 Enter RFCH.
2 Press F2 (QS).

RFCH screen showing Enter Criteria screen
3 Key in your search criteria and press F2 (Execute Query).

RFCH screen showing six records in pick list
4 Use your arrow keys to scroll through the list of records retrieved. If you wish to jump forward by ten 
records, press F1 (JF). If you wish to jump backwards by ten records, press F2 (JB).
5 When you find the line that you wish to select, press F3 to select it.
6 Continue to process the receipt normally.

INBOUND PROCESSING
Unloading Product in RFCH
ENTERING PARTIAL U-TYPE RECEIPT LINES
You can enter partial U-type receipt lines in RFCH by entering the partial quantity (for example, 10 cases) and 
then keying in N for No when prompted to complete the process. You use partial receipt lines when product 
on a trailer is dispersed and you are not sure whether you have processed all product belonging to a 
particular inventory entity. You also use partial receipt lines when you wish to place part of a receipt on hold; 
for example, you receive a pallet of 100 cases and 20 cases are damaged.
When you enter partial receipt lines in RFCH, two lines are created in ENRE/LORE. The first line shows the 
number of units actually received and the second line shows the remaining number of units. For example, if 
your expected quantity is 100 and your received quantity is 10, the following receipt lines will be created:
▪ line 1: expected qty = 100, received qty = 10
▪ line 2: expected qty = 0, received qty = 90
If you receive additional units of the same product, line 2 will show the new quantity received and line 3 will 
show the new remaining number of units.
EXAMPLE
1) You received 10 units out of an expected quantity of 100.
2) You receive 20 more units of the same product.
3) You receive 50 more units.
Expected Received Location
line 1 100 10 STAG
line 2 0 90
Expected Received Location
line 1 100 10 STAG
line 2 0 20 STAG
line 3 0 70
Expected Received Location
line 1 100 10 STAG
line 2 0 20 STAG
line 3 0 50 STAG
line 4 0 20

INBOUND PROCESSING
Unloading Product in RFCH
4) You receive the final 20 units.
1 Enter RFCH.
2 Retrieve the inventory entity that you wish to process. 
3 If required, change your mode to either put-away or unload.
4 Key in your partial quantity and press Enter.
5 If required, place the product on hold.
6 Assign the product a location.
7 Press F4 to close the receipt.
8 When the Process Complete? message appears, key in Y for Yes and press Enter.
9 Exit RFCH.
PRINTING LABELS
Printing labels requires a document set up by HighJump in DOCU (Documents).
1 Enter RFCH.
2 Press F1 (PL).

RFCH screen showing Print Label Block
3 Key in your receipt number and press Enter.
4 Enter or scan in your level 1 value.
5 If required, enter or scan in your level 2, level 3 and level 4 values.
Expected Received Location
line 1 100 10 STAG
line 2 0 20 STAG
line 3 0 50 STAG
line 4 0 20 STAG

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen prompt for quantity
6 Key in the number of labels that you wish to print for this inventory entity and press Enter.
7 Key in your printer code and press Enter.
8 Repeat the above steps for each additional label that you wish to print or press F4 the required number of 
times to exit.
UNDERSTANDING VARIANCES IN RFCH
A variance occurs when the quantity actually received does not match the quantity on the receipt. There are 
two ways of calculating variances depending on the type of line:
▪ If all inventory levels are entered during receipt entry (that is, a P-type line), variances are calculated at 
the line level (that is, the lowest inventory level).
▪ If not all inventory levels are entered during receipt entry (that is, a U-type line), variances are calculated 
at the next highest level that is known. For example, if levels 1 and 2 are known and level 3 is unknown, 
the variance will be calculated for inventory level 2. If, however, level 1 is known and levels 2 and 3 are 
unknown, the variance will be calculated for inventory level 1.
For example, suppose you received the following product on the same receipt and level three (pallet ID) is 
system-generated:
If you enter a quantity of 85 for line 1 and a quantity of 65 for line 2, no variance will occur in RFCH because 
the total (85 + 65 = 150) equals the total in ENRE for item A1, lot 101.
If you enter a quantity of 120 for line 1 and a quantity of 45 for line 2, a variance will occur in RFCH because 
the total (120 + 45 = 165) does not equal 150. If you accept the variance of 15 units, the extra 15 units will be 
LINE 1
Item = A1
Lot = 101
Pallet ID = 001
Quantity = 100
LINE 2
Item = A1
Lot = 101
Pallet ID = 002
Quantity = 50

INBOUND PROCESSING
Unloading Product in RFCH
applied to line 1; you cannot split an overage or adjustment between two pallet ID’s belonging to the same lot 
number.
PROCESSING VARIANCES
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Must Match ENRE”, you 
cannot enter variances in RFCH. When the quantity received does not match the quantity on the receipt, the 
following message will appear and you must either enter the correct quantity or exit the receipt line.

RFCH screen showing “Qty entered does not match expected qty” message
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching not required”, you 
can enter variances in RFCH. Variance processing in RFCH is dependent on whether or not the operator has 
supervisory privileges.
1 Make sure that the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching 
not required”.
NOTE All variances in RFCH are shown in the lowest SKU. For example, if your 
item is a pallet/case/each item, any variances will be shown in eaches — not pallets 
or cases.
Operator is NOT a Supervisor Operator is a Supervisor
variance is a shortage “Receipt not completed yet” message 
appears when you exit the receipt and 
AccellosOne 3PL creates a second line in 
ENRE for the missing product. Operator 
can return to the receipt at any time to enter 
the missing product or office staff can 
delete the second line.
“Complete Process” message appears and 
supervisor is prompted to zero out the lines. 
If the supervisor selects Yes, Variance 
screen appears and supervisor is prompted 
to accept the shortage. No second line is 
created in ENRE for the missing product. 
variance is an overage If you enter all your inventory levels manually, Variance screen appears when you 
enter your quantity. If you do not enter all 
your inventory levels manually (that is, a Utype lines), Variance screen appears when 
you exit the receipt. In the Variance screen, 
operator is prompted to accept the overage. 
In ENRE, received quantity is greater than 
expected quantity.
Same as operator or non-supervisor.

INBOUND PROCESSING
Unloading Product in RFCH
2 Enter RFCH.
3 Enter or scan in your UI value or enter your receipt number and all known inventory levels of the product 
that you are receiving.
4 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and 
press Enter to bypass these fields.
5 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in 
a new quantity and press Enter.
6 Do one of the following:
7 Proceed to enter your hold code (if any) and location information for the receipt and then perform the 
remaining steps in RFCH normally.
8 When you finish processing all your receipt lines, press F4 to switch to main mode.
If the variance is a shortage: If the variance is an overage:
a) Proceed to next step. a) The following screen will appear: 
RFCH screen showing Variance 
screen
b) Key in Y for Yes to accept the 
variance or key in N for No to reenter a new received quantity.

INBOUND PROCESSING
Unloading Product in RFCH
9 Do one of the following:
ENTERING PROCESS VALUES
If the capture of process values is activated for the product that you are receiving, you will be prompted to 
enter process values under the following conditions:
If you have supervisor privileges:
If you do NOT have supervisor 
privileges:
The following screen will appear:

a) Key in Y for Yes and press Enter 
to zero out all lines.
b) When prompted to confirm the 
zero out, key Y for Yes and press 
Enter.
c) If the variance is a shortage, the 
following screen will appear.

d) Press F3 (ZO) to accept the 
shortage.
e) Press Enter to continue.
The following screen will appear:

a) Press Enter to acknowledge the 
incomplete receipt messsage.

INBOUND PROCESSING
Unloading Product in RFCH
▪ there are no process values for the receipt line that you are processing
▪ there are missing process values for the receipt line that you are processing
▪ the quantity received in RFCH does not match the quantity recorded in ENRE (any existing process values will be erased and new values must be entered)
If you are unable to scan in each case ID on the pallet for any reason, AccellosOne 3PL will present you with 
the following options:
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all inventory levels of the product that 
you are receiving.
3 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and 
press Enter to bypass these fields.
4 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in 
a new quantity and press Enter.

RFCH screen showing prompt for process value
5 Key in your first value and press Enter or scan it in using your RF gun.
6 If you are capturing multiple process values, repeat the above step for each additional process value.
7 If you wish to interrupt your scanning for any reason, press F4.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will 
remove unscanned quantities from the receive quantity. You cannot process the receipt line again in RFCH.
4 (Exit, Save) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned. You 
cannot process the receipt line again in RFCH.
5 (Exit, No Save) Cease scanning and exit without saving any process 
values including those already scanned. You cannot 
process the receipt line again in RFCH.

INBOUND PROCESSING
Unloading Product in RFCH

RFCH screen showing incomplete scan message
8 Do one of the following:
9 Continue to process the receipt normally.
VALIDATING PROCESS VALUES
If you set the Validate One Process Value flag to Y for Yes, you will be prompted to validate the serial number 
and other information such as level 1 and 2 values in bar code labels. You validate process values by 
scanning in one label from each pallet; if the label is not valid, you will not be allowed to complete the receipt 
in RFCH.
Validation will only occur for P-type receipt lines when the full quantity is received and all process values have 
been entered or scanned in. 
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all inventory levels of the product that 
you are receiving.
If you wish to continue from 
where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the 
received quantity:
Key in 3 and press Enter.
When prompted to short the receipt line, key in Y for 
Yes and press Enter.
If you wish to exit and save the 
scanned process values:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values:
Key in 5 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

INBOUND PROCESSING
Unloading Product in RFCH
3 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and 
press Enter to bypass these fields.
4 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in 
a new quantity and press Enter.

RFCH screen showing prompt to scan any case
5 Scan in any case on the pallet.
6 Continue to process the receipt line normally in RFCH.
CREATING A NEW LINE
If the product that you are receiving is not on the original receipt, you can create a new line for the product in 
RFCH. When you create a new line in RFCH, AccellosOne 3PL creates a new line for the receipt in ENRE in 
which the expected quantity and received quantity equal the quantity that you entered in RFCH. If an 
inventory level is system-generated, AccellosOne 3PL will generate the appropriate value for that inventory 
level.
Creating a new line is only allowed if the Allow New Lines flag in MRFP is set to Yes for the customer whose 
product you are receiving.
1 Enter RFCH.
2 Press Enter to bypass the UI field.
3 Key in your receipt number and press Enter.
4 Key in your level 1 value for the item that you wish to receive and press Enter. 

INBOUND PROCESSING
Unloading Product in RFCH
5 Do one of the following:
6 With your cursor positioned in the field for your lowest inventory level, press F1 (CL). AccellosOne 3PL 
will display the following message. 

RFCH screen showing prompt to create a new line
7 Do one of the following:
8 Proceed to enter the receipt normally.
RECEIVING PRODUCT UNDER AN ALTERNATE ITEM CODE
An alternate item code is a second or alternate name for an item. For example, you receive product under the 
code ABC and then you store it and ship it in AccellosOne 3PL under the code 001. 
Alternate item codes must be set up in ALIT (Alternate Item and Language). Refer to the Setup Guide for 
further instructions on setting up ALIT.
If you enter all inventory levels 
during receipt entry:
If your lowest inventory level is 
system generated:
a) Key in all inventory levels for the 
item.
a) Key in all inventory levels for the 
item except the last level. For 
example, if you are receiving a 
three-level item, you would enter 
the second inventory level but 
not the third. If you are receiving 
a four-level item, you would enter 
the second and third inventory 
levels but not the fourth.
If you wish to create a new line:
If you do NOT wish to create a 
new line:
a) Key in Y for Yes and press Enter.
b) Key in your quantity and press 
Enter.
a) Key in N for No and press Enter.
b) Re-enter the inventory level that 
triggered the “Create a New 
Line?” prompt.

INBOUND PROCESSING
Unloading Product in RFCH

ALIT screen showing ALT_ITEM as an alternate item code for item D1
1 Make sure that your receipt is at the flow DRDO (Driver Arrived at Door).
2 Enter RFCH.

RFCH screen

INBOUND PROCESSING
Unloading Product in RFCH
3 Do one of the following:

RFCH screen showing prompt for tie and hi
4 Proceed to process your receipt in the normal manner.
RECEIVING PRODUCT ON AUTOMATIC HOLD
If you are receiving product on automatic hold, you can override or remove the automatic hold if the Allow 
Override of Hold Code During Core RF Receiving field in IHOP (Item Hold Profile) is set to Yes. If you set this 
flag to No, you will not be able to override or remove automatic holds. The profile that you set up in IHOP 
must be attached to the appropriate item in ITEM.
If you are receiving an item 
with a single inventory level:
If you are processing a P-type 
line containing an item with 
multiple inventory levels:
If you are processing a U-type 
line containing an item with 
multiple inventory levels:
a) Enter or scan in your alternate 
item code in the UI field. The 
system will convert the alternate item code to the regular 
AccellosOne 3PL item code. 
a) Enter or scan in your UI value. 
The system will retrieve the 
receipt number and three 
inventory levels for that UI 
value. The alternate item code 
will be converted to the regular 
AccellosOne 3PL item code.
a) Press Enter to bypass the UI 
field.
b) Key in your receipt number 
and press Enter.
c) Enter or scan in your alternate 
item code. The system will 
convert the alternate item 
code to the regular AccellosOne 3PL item code.
d) Enter or scan in your remaining inventory levels.

INBOUND PROCESSING
Unloading Product in RFCH

IHOP screen showing Allow Override of Hold Code During Core RF Receiving field set to Y for Yes
RECEIVING PRODUCT WITH A VARIABLE PRODUCT BREAKDOWN
If you are receiving product with a variable quantity breakdown in RFCH, you must enter your quantity in the 
lowest SKU.
1 Enter RFCH.
2 Press Enter to bypass the UI (Unique Identifier) field. 
3 Key in your receipt number and press Enter.
4 Enter or scan your level 1 value for the first product that you wish to receive.
5 Enter or scan in your level 2 value. If required, enter or scan in your level 3 and level 4 values.
6 Depending on your system setup, RFCH will be preset to either put-away mode or unload mode. If 
required, you can press F3 (CM) to toggle between the two modes.
Once you process a receipt line, the mode is set for all remaining lines on the receipt and cannot be 
altered until you start a new receipt.
7 Key in your tie, hi and loose values. If you do not wish to record these values, press Enter three times to 
bypass these fields.
8 Key in your quantity in the lowest SKU and press Enter.
9 Continue to process the receipt normally in RFCH.
RECEIVING MIXED PRODUCT
You can receive mixed product on a single pallet without the need to scan in each unique inventory entity. For 
example, you have two receipt lines in ENRE with the same level 1 and 3 values (item code and pallet ID), but 
different level 2 values (date code). When you scan in the level 3 value in RFCH, you will be prompted to 
choose between full pallet receiving (process the pallet once as if the product was not mixed) or regular 
receiving (process each receipt line separately).

INBOUND PROCESSING
Unloading Product in RFCH
Receiving mixed product on a single pallet requires that the Receipt Reference Number field in ENRE be 
populated with the level 3 or 4 value that you scan in RFCH.
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all known inventory levels of the product 
that you are receiving.

RFCH screen showing three inventory entities on the same pallet
3 Press F3 (Sl) to select the first line.

RFCH screen showing mixed pallet message
4 Do one of the following:
If you wish to perform full pallet 
receiving:
If you wish to perform regular 
receiving:
a) Key in Y for Yes and press Enter.
b) Proceed to enter the quantity 
and location for the full pallet.
c) If prompted to do so, enter your 
trailer and pallet information in 
the normal manner.
a) Key in N for No and press Enter.
b) Proceed to enter the quantity 
and location for the first inventory 
entity on the pallet.
c) Repeat the previous step for 
each additional inventory entity 
on the pallet.
d) If prompted to do so, enter your 
trailer and pallet information in 
the normal manner.

INBOUND PROCESSING
Unloading Product in RFCH
LOOKING UP TEMPERATURE AND TRAILER INFORMATION IN LORE
If you entered a temperature and trailer number in RFCH, you can look up this information in the Carrier Block 
of LORE.
1 Enter LORE.
2 Retrieve the receipt whose temperature and trailer information you wish to look up.

LORE screen showing receipt number 4
3 Make sure that the value in the Carrier Details field is E for Entered.
4 Press Enter to position your cursor in the Carrier Details field.
5 Click on Carrier Details.

INBOUND PROCESSING
Unloading Product in RFCH

Carrier Details block of LORE showing trailer number and temperature
6 Click on Return to exit the Carrier Details Block. Then click on Exit to exit.
LOOKING UP REMARKS AND MESSAGES IN RFCH
There are four types of remarks/messages in RFCH:
▪ receipt header remarks prefixed by the number 0
▪ receipt line remarks prefixed by the line number (for example, 1, 2, 3)
▪ item messages set up in ITEM
▪ depositor print messages set up in DPME 
When you enter the receipt header in RFCH, all remarks/message are displayed in the following order:
▪ receipt header remarks
▪ line remarks
▪ item messages set up in ITEM
▪ depositor print messages set up in DPME
1 Enter RFCH and retrieve the receipt whose remarks/messages you wish to look up. The remark/message will display automatically when you retrieve the receipt.

INBOUND PROCESSING
Entering Temperature and Trailer Information in RFTT

RFCH screen showing header and line remarks
2 If the remarks are more than six lines long, use your up and down arrow keys to scroll through the remark 
lines.
3 If there are multiple remarks/messages attached to the receipt, press Enter or F4 to jump to the next 
message.
4 Continue to process the receipt normally.
Entering Temperature and Trailer Information in RFTT
This program allows you to enter temperature, trailer/seal number and pallet information for a given receipt or 
order without working in RFCH or RFPIC. The information that you can enter in RFTT — temperature only, 
trailer/seal number only, temperature and trailer/seal number, etc. — depends on which option you choose in 
the Show Temperature and Pallet Blocks field in MRFP and which value if any you enter in the Num of Temp. 
field in LOAD.
1 Enter RFTT.
RFTT screen
2 Key in your receipt number and press Enter.

INBOUND PROCESSING
Putting Away Product in RFPU
3 Enter your temperature, trailer/seal number and pallet information in the usual manner.
Putting Away Product in RFPU
You put away your product in RFPU. RFPU can only be used after unloading the product in RFCH. If you wish 
to put-away product without unloading it, you must perform one-step put-away in RFCH.
When putting away product, you can enter the exact quantity (that is, the expected quantity equals the 
received quantity), an overage or a shortage and, if required, you can place product on a manual hold. You 
can also split a line; that is, if your receipt line has 50 units, you can put-away 30 units today in one location 
and put-away the remaining 20 units at a later time in the same location or in another location.
There are four different hold options in RFPU:
If directed put-away is activated on your system, the system-assigned warehouse and location will be 
displayed. You can accept the system-assigned warehouse and location or you can enter a new warehouse 
and location. If directed put-away is not activated on your system, you must enter your put-away location and 
warehouse manually. You can eliminate the need to enter a warehouse in RFPU by defining a default 
warehouse in the header block ENRE (for a given receipt) or in CUST (for all receipts from a given customer). 
If automatic confirmation is activated, RFPU advances the receipt’s flow to CORE. Therefore, you cannot 
work on or make adjustments to the receipt after processing it in RFPU.
If you enter a shortage … You can place a manual hold on the difference between the 
expected quantity and the received quantity. For example, if the 
quantity staged in RFCH is 100 units and you enter 80 for the same 
receipt line in RFPU, AccellosOne 3PL will place 20 units on the 
hold that you specify.
If the entire receipt line is damaged or 
requires special processing …
You can place an entire receipt line on a manual hold.
If you enter a shortage and the non-shortage part of the receipt line is damaged or 
requires special processing …
You can place two manual holds on the same receipt line: one hold 
for the variance quantity and a second hold for the non-variance 
quantity.
If automatic holds are activated for the 
product …
If manual overriding of holds is activated in IHOP, you can manually 
override or remove the hold code. If manual overriding of holds is 
NOT activated in IHOP, you cannot override or remove the hold 
code.
REQUIREMENTS
FLOWS See “Unloading Product in RFCH” on page 154 for further information.

INBOUND PROCESSING
Putting Away Product in RFPU
1 Make sure that your receipt in ENRE is at one of the following flows: DRDO (Driver at Door), STUN (Start 
Unloading), INST (Inbound Staged) or STPU (Start Put-Away).
2 Enter RFPU.
LINE TYPES RFPU requires P-type lines unless U-type lines have been received with a quantity of zero.
AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a 
new flow and attach it to your inbound flow profile. This flow must be placed 
before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must 
be set to Y for Yes.
DOCUMENTS The Print Document Without Assigning Locations flag in DOCU (Documents) 
must be set to Yes for all receipt-related documents such as the tally.
OTHER The product must have been placed in a staging location in RFCH.
FUNCTION KEYS
Main Mode
F4 EX (Exit) Exit program.
Results Mode
F1 RM (Remark) Show remark(s) entered in ENRE.
F4 RT (Return to Main) Switch to Main Mode.
F9 Move cursor to previous field.
REQUIREMENTS

INBOUND PROCESSING
Putting Away Product in RFPU

RFPU screen
3 Do one of the following:

RFPU screen showing receipt 5
If you know the UI value of the 
product that you are putting 
away:
If you do NOT know the UI value 
of the product that you are 
putting away:
a) Enter or scan in your UI value. 
You can also select your UI value 
using the pick list function. If 
there are multiple receipts 
attached to the same UI, receipts 
will display in location order not 
receipt number order.
a) Press Enter to bypass the UI 
field.
b) Key in your receipt number and 
press Enter.
c) Key in your level 1 value for the 
first product that you wish to 
receive and press Enter.
d) Key in your level 2 value and 
press Enter.
e) Key in your level 3 value and 
press Enter.
f) If required, key in your level 4 
value and press Enter.

INBOUND PROCESSING
Putting Away Product in RFPU
4 If F1 (Rm) is available, the receipt has remarks. You can press F1 to view the remarks and then press F4 
to exit the Remarks Block.
5 Key in the quantity that you are receiving and press Enter. You can enter your quantity in pallets, eaches 
or any other SKU type that is activated in the item’s quantity breakdown. If your default SKU type is 
eaches and you wish to enter a quantity of 10 pallets, you would key in 10P for 10 pallets.
6 Do one of the following:

RFPU screen showing variance options
7 Do one of the following:
If the quantity matches the 
quantity of the receipt line in 
RFCH:
If the quantity does NOT match 
the quantity of the receipt line in 
RFCH:
a) Proceed to step 9. The message “This receipt line has a variance. Accept? (Y/N/H/V)” will appear.
a) Proceed to next step.
If the variance is a shortage 
and you wish to ignore it for 
now because you expect to 
receive more product:
▪ Key in Y for Yes and press Enter.
AccellosOne 3PL will create a new receipt line for the 
difference.
If you wish to reject the variance and re-enter the quantity:
▪ Key in N for No and press Enter.
▪ Re-enter your quantity.
If the variance is a shortage 
and you wish to place the variance quantity on hold:
▪ Key in the H for Hold and press Enter.
▪ Key in your hold code and press Enter.
AccellosOne 3PL will place the variance quantity on 
the hold type that you specify.
If you wish to accept the variance:
▪ Key in V for Variance and press Enter.
AccellosOne 3PL will short the line without creating a 
new receipt line.

INBOUND PROCESSING
Putting Away Product in RFPU

RFPU screen showing prompt for hold code
8 Do one of the following:
If there is no automatic hold 
placed on the item:
If there is an automatic hold 
placed on the item and manual 
overriding of holds is 
activated:
If there is an automatic hold 
placed on the item and manual 
overriding of holds is NOT 
activated:
a) If you wish to place the product on manual hold, press F9 
to position your cursor in the 
Hold field. Then key in your 
manual hold code and press 
Enter.
▪ The hold that you enter in this field 
applies to the entire receipt line — if 
you did not record a variance in the 
Quantity field — or the difference 
between the variance and the 
expected quantity — if you did record 
a variance in the Quantity field.
a) If required, you can manually 
override or remove the hold 
code. Make any necessary 
changes and press Enter or 
press Enter without making 
any changes to accept the 
automatic hold.
a) The cursor will skip past the 
Hold field and you will not be 
able to override or remove the 
hold code.
current staging location for product

INBOUND PROCESSING
Putting Away Product in RFPU
9 Do one of the following:
10 Repeat the above steps for the each additional receipt line that you wish to put away.
11 When all your lines have been put-away, the following message will appear:
If directed put-away is activated 
on your system:
If directed put-away is NOT 
activated on your system:
AccellosOne 3PL will display the 
system-assigned warehouse and 
location. You can accept the system-assigned warehouse and location or you can enter a different 
warehouse and location.
If you wish to override the systemassigned location, see “Overriding 
the System-Assigned Location” on 
page 198.

RFPU screen showing systemassigned warehouse and location
a) Press Enter to accept the system-assigned location or press 
F3 (NX) to display a second suggested put-away location. If the 
second suggested put-away 
location is not acceptable, press 
F3 (NX) again to see a third suggested put-away location.
b) Press Enter again to accept the 
warehouse that the systemassigned location belongs to.
a) Key in your location and press 
Enter.
b) If required, key in your warehouse and press Enter. You will 
not need to enter a warehouse if 
you defined a default warehouse 
in either ENRE or CUST.
F = from location
S = system location
T = to location

INBOUND PROCESSING
Putting Away Product in RFPU

 RFPU screen showing the “Receipt Put-Away” message
12 Press Enter to accept the message then process another receipt or press F4 to exit.
OVERRIDING THE SYSTEM-ASSIGNED LOCATION
There are three options for overriding the system-assigned location for a receipt line depending on your setup 
in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Overrides in RFCH/RFPU/RFRL flag in MRFP is set to No, an 
operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Overrides in RFCH/RFPU/RFRL flag in MRFP is set to Yes, 
changing a location must be approved by a supervisor
▪ if the Reason Code Required to Override System-Assigned Location flag in MRFP is set to Yes, the RF 
operator will be required to enter a reason code
1 Enter your receipt in RFPU in the normal manner.

RFPU screen showing system-assigned location
2 Key in your new location and press Enter.

INBOUND PROCESSING
Putting Away Product in RFPU
3 Do one of the following:
4 Proceed to process the receipt normally in RFPU.
ENTERING VARIANCES
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Must match ENRE”, you 
cannot enter variances in RFPU. When the quantity received does not match the quantity on the receipt, the 
following message will appear and you must either enter the correct quantity or exit the receipt line.
If supervisor authorization is 
activated:
If supervisor authorization is 
NOT activated:
The following screen will appear:

a) Key in Y for Yes and press Enter 
to proceed with the location override. If you do not wish to proceed with the override, key in N
for No and press Enter to return 
to the main RFPU screen.

b) Have a supervisor log in to 
approve the location override.
The following screen will appear:
a) Key in Y for Yes and press Enter 
to proceed with the location override. If you do not wish to proceed with the override, key in N
for No and press Enter to return 
to the main RFPU screen.
b) Press Enter again to accept the 
warehouse that the systemassigned location belongs to.

INBOUND PROCESSING
Putting Away Product in RFPU

RFPU screen showing “Qty entered does not match expected qty” message
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching not required”, you 
have four options:
▪ you can ignore the variance for now because you expect to receive more product
▪ you can reject the variance and re-enter the quantity
▪ you can place the variance quantity on hold
▪ you can accept the variance
If you accept the variance, AccellosOne 3PL will create one line in the Location Block of ENRE for the flow 
CORE (Confirm Receipt) showing the actual quantity received. If you place the variance quantity on hold, 
AccellosOne 3PL will create two lines in the Location Block of ENRE for the flow CORE (Confirm Receipt): 
one line showing the actual quantity received with no hold code and a second line showing the variance 
quantity with the hold code that you specified in RFPU.

LORE screen showing 80 cases with no hold in location A101 and 20 cases on damaged hold in the 
same location

INBOUND PROCESSING
Putting Away Product in RFPU
PUTTING AWAY PRODUCT UNDER AN ALTERNATE ITEM CODE
See “Receiving Product Under an Alternate Item Code” on page 184 for further information on setting up 
alternate item codes.
1 Make sure that your receipt in ENRE is at one of the following flows: STUN (Start Unloading), INST 
(Inbound Staged) or STPU (Start Put-Away).
2 Enter RFPU.

RFPU screen
3 Do one of the following:
If you are receiving an item 
with a single inventory level:
If you are receiving an item 
with multiple inventory levels 
and you know the UI value of 
the product that you are 
putting away:
If you are receiving an item 
with multiple inventory levels 
and you do NOT know the UI 
value of the product that you 
are putting away:
a) Enter or scan in your alternate 
item code in the UI field. The 
system will convert the alternate item code to the regular 
AccellosOne 3PL item code. 
a) Enter or scan in your UI value. 
The system will retrieve the 
receipt number and three 
inventory levels for that UI 
value. The alternate item code 
will be converted to the regular 
AccellosOne 3PL item code.
a) Press Enter to bypass the UI 
field.
b) Key in your receipt number 
and press Enter.
c) Enter or scan in your alternate 
item code. The system will 
convert the alternate item 
code to the regular AccellosOne 3PL item code.
d) Enter or scan in your remaining inventory levels.

INBOUND PROCESSING
Entering Process Values in RFIPS

RFPU screen showing prompt for quantity
4 Proceed to process your receipt in the normal manner.
PUTTING AWAY IN A PICK LINE LOCATION
If you wish to put-away product in a pick line location, you must set the Validation Rules for Put-Away to Pick 
Line flag in MRFP to either 2 (Allow operator to proceed) or 3 (Omit validation of location).
Entering Process Values in RFIPS
RFIPS is a stand-alone version of the process value module in RFCH. It allows you to scan in process values 
without assigning the product to a final put-away location.
1 Enter RFIPS.
REQUIREMENTS
LOCATION STATUSIf there is an MRFP profile attached to the customer in CUST, the receipt line 
must be assigned a location. If there is no MRFP profile attached to the customer 
in CUST, a location for the receipt line is not required.
CATCH WEIGHT 
TOLERANCES
See “Setting Up Catch Weight Tolerances” on page 302 for further information.

INBOUND PROCESSING
Entering Process Values in RFIPS

RFIPS screen
2 Enter your receipt number.
3 Enter or scan in your UI value. If you do not have a UI value, enter all inventory levels.

RFIPS screen
4 Key in your first value and press Enter or scan it in using your RF gun.
5 If you are capturing multiple process values, repeat the above step for each additional process value.
6 If you wish to interrupt your scanning for any reason, press F4.

INBOUND PROCESSING
Entering Process Values in RFIPS

RFIPS screen showing incomplete scan message
7 Do one of the following:
8 Scan in another receipt line or press F4 to exit.
CAPTURING THE WEIGHT DYNAMICALLY FROM A BAR CODE
The locate weight in bar code dynamically option allows you to scan in the weight from a bar coded label 
without knowing which numbers in the bar code represent the product’s weight. Because the format of the bar 
code is unknown, you cannot use SCPR (Scan Parameter Profile) to break up the code into its component 
parts.
The following requirements must be met before you can locate the weight in a bar code dynamically:
▪ All bar codes for a given order line must have the same length.
▪ The weight portion of the bar code for a given order line must all have the same length; if a weight is less 
than the full length, it must be padded with zeros.
▪ All weights for a given order line must fall within a range of 10 times heavier or lighter than the first case. 
For example, if case 1 weighs 100 lbs., case 2 cannot weigh more than 1,000 lbs. or less than 10 lbs.
▪ The locate weight option must be activated in IPRO by setting the Locate Weight in Bar Code Dynamically flag to Y for Yes for a given process code. This process code must be attached to an item process 
If you wish to continue from where you 
left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the 
received quantity:
Key in 3 and press Enter.
When prompted to short the receipt line, key in Y for Yes and press 
Enter.
If you wish to exit and save the 
scanned process values:
Key in 4 and press Enter.
If you wish to exit without saving the 
scanned process values:
Key in 5 and press Enter.

INBOUND PROCESSING
Entering Process Values in RFIPS
profile code in IPRP (Item Process Profile), which in turn must be attached to the appropriate item(s) in 
ITEM.

IPRO screen showing Locate Weight in Bar Code Dynamically flag set to Y for Yes
The operator scans in the full bar code and then manually enters the weight for the first three cartons. If the 
manually entered weight matches the bar code weight in all three cartons on the same order line, AccellosOne 3PL “learns” the position of the weight in the bar code.
If the manually entered weight does not match the bar code weight, the operator will be prompted to either 
start over again or rescan the current carton.
EXAMPLE
9991234999 (Label 1)
9991356999 (Label 2)
9991426999 (Label 3)
Because the position of the weight in label one (positions 4 through 7) matches the position of the weight in 
labels two and three, AccellosOne 3PL will read the weight from these positions for all pieces on the receipt 
line.
If the same bar code is scanned twice, the operator will have two choices: accept the duplicate or enter a new 
bar code.
1 Enter RFIPS.
2 Enter your receipt number.
3 Enter or scan in your UI value. If you do not have a UI value, enter all inventory levels.

INBOUND PROCESSING
Entering Process Values in RFIPS

RFIPS screen showing prompt to use weight discovery
4 Key in Y for Yes and press Enter.
RFIPS screen showing prompt for weight measure code
5 Key in your weight unit of measure (1 for kilograms or 2 for pounds) and press Enter. If you made a mistake and wish to select another order line, key in 3 for Cancel and press Enter. 

RFIPS screen showing prompt to scan the bar code
6 Scan in your bar code.

INBOUND PROCESSING
Entering Process Values in RFIPS

RFIPS screen showing prompt to enter weight
7 Key in the weight and press Enter. The weight must include a decimal point. For example, to enter a 
weight of 20 pounds, you must key in either 20.0 or 20.00. You cannot key in 20.
8 Repeat steps 5 and 6 for your second piece.
9 Do one of the following:
If the position and weight of label 
1 matches label 2:
If the position and weight of label 
1 does NOT match label 2:
a) Repeat steps 5 and 6 for your 
third piece.
AccellosOne 3PL will offer you two 
options: you can either start over 
again from the first scan or repeat 
the second scan.
a) Press Enter to rescan or key in N
for No to start over. 

INBOUND PROCESSING
Deleting a Receipt Line in RFDL
10 Do one of the following:
11 Scan in your first piece.
12 Continue to scan all pieces on the receipt line. If the same item is found on two or more receipt lines, 
AccellosOne 3PL will calculate a running total of the weight for all receipt lines containing that item.
13 When you finish scanning all your pieces, process another receipt line or press F4 to exit.
Deleting a Receipt Line in RFDL
You can delete a receipt line in RFDL if the receipt line has not been confirmed.
1 Enter RFDL.
RFDL
If the position and weight of label 
3 matches labels 1/2:
If the position and weight of label 
3 does NOT match labels 1/2:
The following message may 
appear:
“Keep 3 Scans” message
a) Press Enter to start scanning or 
key in N for No and press Enter.
AccellosOne 3PL will offer you two 
options: you can either start over 
again from the first scan or repeat 
the third scan.
a) Press Enter to rescan or key in N
for No to start over. 

INBOUND PROCESSING
Deleting a Receipt Line in RFDL
2 Key in your receipt number and press Enter.
RFDL screen showing prompt for unique UI
3 Key in your UI for the receipt line and press Enter.
RFDL screen showing prompt to continue
4 Press Enter to continue.
RFCH screen showing prompt to delete receipt line

INBOUND PROCESSING
Clearing Tie/Hi/Loose Variances in RFCV
5 Key in Y for Yes and press Enter.
6 When you finish deleting your receipt line, press F4 to exit.
Clearing Tie/Hi/Loose Variances in RFCV
This program allows supervisors to clear receipt variances that occur when the tie/hi/loose quantity entered in 
RFCH does not match the expected quantity in ENRE. When a supervisor clears a pallet, it becomes 
available for final put-away in RFPU. There are two options in this program:
If the received quantity was adjusted and if the product is a catch weight product, the supervisor will be 
prompted to capture the weights.
1 Enter RFCV.
2 Enter or scan in your UI.
RFCV screen showing variance (three cases expected and four cases received)
RFCV screen showing variance (three cases expected and four cases received)
3 When the receipt line is retrieved, press Enter to continue.
update the received 
quantity
the RFCH operator made a mistake, there is no variance and the expected and received quantities in fact 
match
accept the variance The supervisor has confirmed the variance

INBOUND PROCESSING
Clearing Tie/Hi/Loose Variances in RFCV
RFCV screen showing variance options
4 Do one of the following:
To reject the variance: To accept the variance:
a) Key in 1 and press Enter.
b) Enter the correct quantity and 
press Enter.
c) If the product is a catch weight 
product, enter your catch 
weights.
a) Key in 2 and press Enter.

INBOUND PROCESSING
Clearing Tie/Hi/Loose Variances in RFCV

OUTBOUND PROCESSING
Overview of Shipping ..................................................................................... 216
Understanding Outbound Flows in RF.......................................................... 217
Understanding Pick Methods......................................................................... 217
Overview of RF Picking Programs ................................................................ 219
Picking Orders in RFPIC................................................................................. 220
Picking Full Pallets from Bulk..................................................................... 225
Picking Cases ............................................................................................ 227
Picking Product With Process Values........................................................ 232
Picking Partial Quantities of Product With Process Values ....................... 234
Picking Reserve Logic Orders ................................................................... 235
Placing Product on Hold ............................................................................ 236
Excluding Orders from Overpicking in EOSU ............................................ 241
Picking Pick Line Product from a Non-Pick Line Location ......................... 242
Performing Replenishments in RFPIC ....................................................... 243
Looking Up Remarks and Messages in RFPIC ......................................... 243
Recovering From a Dropped Connection .................................................. 244
Performing Inventory Count Backs............................................................... 246
Performing the Count in RFPIC ................................................................. 247
Looking Up Inventory Discrepancy Records in ICIN.................................. 249
Looking Up Inventory Discrepancy Records in RFCL................................ 250
Removing Inventory Discrepancy Records in RFCL.................................. 252
Removing Inventory Discrepancy Records in RFCL.................................. 252
Removing Inventory Discrepancy Records in RFCI................................... 252
Entering Temperature and Trailer Information in RFTT .............................. 253
Entering Pallet Information in RFOPE........................................................... 254
Editing a Pallet Details Record in RFOPE ................................................. 256
Deleting a Pallet Details Record in RFOPE ............................................... 257
Adjusting Your Pallet Type in RFPA ............................................................. 257
Looking Up Your OPID’s ................................................................................ 258
Looking Up Your OPID’s in LOCN ............................................................. 259

OUTBOUND PROCESSING
Looking Up Your OPID’s in RFNCO .......................................................... 259
Looking Up an Order’s OPID’s in LOOR.................................................... 260
Confirming Orders by OPID in RFCO............................................................ 261
Confirming Individual Order Lines by UI in RFCU ....................................... 263
Reprinting Outbound Labels in RFOLP ........................................................ 264
Picking Cases from a Pick Line in CASE...................................................... 267
Merging OPID’s in RFOPB.............................................................................. 272
Picking Substitution ....................................................................................... 275
Setting Up Picking Substitution.................................................................. 275
Excluding Orders from Picking Substitution in EOSU................................ 280
Performing Picking Substitution in RFPIC ................................................. 281
Entering Process Values in RFOPS .............................................................. 284
Capturing the Weight Dynamically from a Bar Code ................................. 289
Manually Entering the Weight .................................................................... 294
Removing Labels That Have Been Scanned ............................................. 295
Removing Cases Either Scanned or Unscanned....................................... 297
Removing Cases From a Fully Scanned Order ......................................... 298
Performing an Incomplete Scan................................................................. 300
Transferring Inbound Process Values to Outbound Orders....................... 301
Setting Up Catch Weight Tolerances......................................................... 302
Picking Waves in RFPK .................................................................................. 304
Relocating Product in RFST........................................................................... 307
Merging OPID’s in RFMG................................................................................ 309
Merging Two Existing OPID’s .................................................................... 310
Creating a New OPID ................................................................................ 311
Performing Outbound Audits in RFOA ......................................................... 313
Adjusting Cubic Dimensions in RFCC .......................................................... 316
Assigning Orders to Loads in SELO ............................................................. 317
Replacing Damaged Product in RFRD .......................................................... 317
Working With Pallet Build Assignments in PABU........................................ 319
Performing Queries.................................................................................... 321
Releasing and Staging a Suspended Load................................................ 324
Merging Assignments ................................................................................ 324
Deleting Assignments ................................................................................ 325
Adding Assignments .................................................................................. 326
Deleting Lines From an Assignment .......................................................... 327
Overriding Assignments............................................................................. 328
Changing Your Order Parameters ............................................................. 329
Restoring Your Original Order Parameters................................................ 329
Printing the Pallet Build Summary Report.................................................. 330
Printing the Pallet Build Detail Report........................................................ 331
Suspending a Task in RFOT...................................................................... 331

OUTBOUND PROCESSING
Releasing a Suspended Task in RFOT ..................................................... 332

OUTBOUND PROCESSING
Overview of Shipping
Overview of Shipping
There are up to nine steps to follow in outbound RF processing:
RFOT
SELO
Depending on the flows in your workflow profile, 
you may have to confirm your orders in CHOF 
(Time-Stamp and Confirm Orders).
You assign buildings and doors to loads in SELO 
(Set Up Load). 
You pick your orders in RFPIC/RFPK/RFPV. If your 
system is set up for pallet building, you must enter 
the pallet ID of your new pallet.
CHOF
If required, you assign RF operators to order lines 
in RFOT (RF Operator Task Assign).
1
2
3
4
5
If required, you set up your loads in SELO (Set Up 
Load). 
Allocation
OLOP
You load your orders in OLOP (Outbound Loading 
Process).
You allocate your orders either in the Wave 
Manager or in PROR/ASOR.
RFPIC/
RFPK/RFPV
SELO
RFOT
If required, you assign RF operators to orders/loads 
in RFOT (RF Operator Task Assign).
6
7
8
9
ENOR
You enter your order in ENOR (Enter, Modify and 
Delete Order).

OUTBOUND PROCESSING
Understanding Outbound Flows in RF
Understanding Outbound Flows in RF
In non-RF shipping, you time-stamp and advance the flow of an order in CHOF (Time-Stamp and Confirm 
Orders). Advancing the flow of an order in CHOF advances the flow of all order lines and order location lines 
on the order. You cannot advance the flow of one order line and leave another order line remain at its original 
flow.
In RF shipping, on the other hand, AccellosOne 3PL automatically advances the flow of individual order lines 
and order location lines. For example, when you pick an order line in RFPIC, the order line’s flow is automatically advanced from STPI (Start Picking) to FIPI (Finish Picking). Because the flow of individual order lines is 
advanced as each order line is picked, not all lines on a given order will be at the same flow. When this 
happens, the order header will show the earliest flow on the order.
For example, suppose there are five order lines on a given order: two lines are at the flow STPI, two lines are 
at the flow FIPI and one line is at the flow STLO (Start Loading). If you look up the order in LOOR, the order’s 
flow will be set to STPI, which is the earliest flow.
Understanding Pick Methods
Pick methods allow you to split order lines into two or more pick method assignments. For example, if your 
order line quantity was two pallets and 10 cases, you might want to assign one RF operator with a forklift to 
pick the two pallets and another RF operator with a different piece of equipment to pick the 10 cases. Without 
pick methods, you would be forced to assign the entire order line quantity to a single RF operator using a 
single piece of equipment. This could be an inefficient use of resources.
Pick methods also allow you to define a sequence for your picking; for example, pick cases/eaches first 
because it is complex and time-consuming and pick full pallets last because it is simple and straightforward. 
Different pick methods can have different label printing requirements; you can attach different customer/
consignee/carrier combinations to a particular pick method/document in CCDU (Customer/Consignee 
Document Setup).
Pick methods are assigned to order lines in the Wave Manager based on the order line quantity and your item 
setup. For example, if your order line quantity is one pallet, the pick method will be set to PALL.
CAUTION Using CHOF to confirm orders in an RF environment is not recommended unless all order lines are at the same flow. If line 1 is at the STPI flow and 
line 2 is at the FIPI flow, advancing the order header to the STLO flow in CHOF will 
also advance line 1 to STLO. At which point, line 1 may no longer be pickable.

OUTBOUND PROCESSING
Understanding Pick Methods
AccellosOne 3PL supports the following pick methods:
You can look up an order line’s pick method in LOOR.
NAME CODE DESCRIPTION
CASE A normal case pick in RFPIC. The Pick Method field in LOOR for this pick 
method is left blank to indicate that it is the system default.
Batch Label Pick BATP A case pick across multiple orders when two or more orders in the wave are 
being picked up by the same carrier and the carrier type = UPS, DHL or 
FEDEX. Labels are printed after each pick.
Batch Pallet Pick BPAL A batch pallet pick across multiple orders in the same wave when the following conditions are met:
▪ the picks consist of partial pallets
▪ the picks are for the same inventory entity in a single location
▪ the entire inventory entity in the location is picked
Labels are printed after the pallet is built.
Each Pick EACH A Pick & Pack by each (the smallest SKU in an item’s quantity breakdown).
Label Pick LABP An individual order pick when a single order is being picked up by a given carrier.
Non-RF Packing Station PKST Manual packing performed in EPSD (Enter Packing Details).
Packed via Packing StationPACK First level cartonization performed in RFSC (RF Sort to Carton) or RFPK (RF 
Wave Pick).
Pallet Pick PALL A full pallet pick. The order quantity of each order line must equal a full pallet 
quantity.
RF Merge RFMG A merge of two or more OPID’s in RFMG.
System-Driven Cartonization Each PickCART A Pick & Pack by each used in system-driven cartonization.

OUTBOUND PROCESSING
Overview of RF Picking Programs
Order line assigned CART pick method
Overview of RF Picking Programs
There are four possible RF picking programs in AccellosOne 3PL: RFPIC, RFPK, RFPV and RFINVT.
RFPIC (RF PICK)
This program is AccellosOne 3PL’s most basic picking program. it is a system-assisted environment in which 
the RF operator can select individual order lines to work on and enjoys considerable latitude in determining 
the sequence of picks.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ Picking is based on orders and order lines only; there is no support for task profiles and any order 
assignments must be created manually in RFOT. 
▪ Pallet building is performed manually by the RF operator.
▪ Any pick methods assigned to the order by the Wave Manager are ignored.
▪ Consolidated pick using wave number is supported but you cannot restrict by warehouse zone.
RFPK (RF WAVE PICK)
This program is AccellosOne 3PL’s most advanced picking program. Many of the tasks that are performed 
manually by the RF operator in RFPIC are automated in RFPK.
▪ Only orders that have been waved in the Wave Manager can be picked.

OUTBOUND PROCESSING
Picking Orders in RFPIC
▪ Pick method assignment is performed by Wave Manager during allocation.
▪ System-driven cartonization is supported.
RFPV (RF PICKING VOICE)
This program is the RF equivalent of voice-activated picking. It allows you to pick certain orders or products 
using a standard RF gun rather than your voice-activated equipment.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ RF operator must be set up in RFOP and REGI must be configured.
▪ Pallet build assignment is performed dynamically in real time rather than through the Wave Manger.
RFINVT (RF INTERLEAVING)
This program supports tasking.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ RF operator must be set up in RFOP and REGI must be configured.
▪ Pallet build assignment is performed by Wave Manager during allocation.
Picking Orders in RFPIC
RFPIC is AccellosOne 3PL’s most basic picking program. You can pick product by zone or by order number. 
Orders must be fully allocated before you can pick them in RFPIC. You cannot pick an order if some lines are 
allocated (R-type) and other lines are unallocated (P-type).
If you are picking full pallets from bulk, you scan in the original pallet ID of the pallet and use this pallet ID for 
the duration of the outbound process. If you are picking cases from either bulk or the pick line, you scan in the 
original pallet ID for each case pick. When you finish building your pallet, you have two options for the 
outbound pallet containing mixed product:
▪ if AccellosOne 3PL generates your pallet ID for outbound pallets, you generate your label and then send 
it to the appropriate printer
▪ if you use your own preprinted labels for outbound pallets, you enter or scan in the preprinted pallet ID
When you finish generating or scanning in your pallet ID label, you can look up your pallet ID in the 
Processing Block of LOOR for each item on the pallet.

OUTBOUND PROCESSING
Picking Orders in RFPIC
If the product that you are picking is not in its assigned location, you have two options. If you know where the 
product is, you can go to that location and pick it. If you do not know where the product is, you can place the 
product on hold to indicate that it could not be picked.
REQUIREMENTS
FLOWS ENOR (Enter Order)
SUAL (Supervisor Allocated) — optional
STPI (Start Picking)
FIPI (Finish Picking)
STLO (Start Loading)
FNLO (Finish Loading)
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFPIC.
CASE PICKING There are three requirements for case picking:
▪ you need a pallet ID label defined in DOCU (Documents)
▪ this label must be attached to the appropriate customers/consignees in CCDU 
(Customer / Consignee Document Setup)
▪ you need an outbound item process code called CP (Case Pick) in IPRO (Item 
Processes)
NOTE Your CP code set up in IPRO must NOT be attached to the IPRP profile 
attached to ITEM.
If you want AccellosOne 3PL to generate a unique pallet ID for each pallet label, 
there are three additional requirements:
▪ you need to set up a code in NUSE (Number Series)
▪ you need to attach to your NUSE code to a DIAP (Depositor Inventory Assign 
Profile) called QRS
▪ you need to set the Outbound Pallet ID Label field on the RFPIC (2) tab in 
MRFP to either option 2 or option 3
NOTE Your QRS code set up in DIAP must NOT be attached to DILP (Depositor Inventory Level Profile).

OUTBOUND PROCESSING
Picking Orders in RFPIC
DIAP screen showing sample setup for case pick label
IPRO screen showing setup for CP code
ITEM MESSAGES If you define a message in MESS (Messages) and attach the message to an item 
in ITEM, the message will display in a pop-up window when you process an order 
line for that item.
REQUIREMENTS

OUTBOUND PROCESSING
Picking Orders in RFPIC
DEPOSITOR 
PRINT MESSAGES
If you wish to display a depositor print message set up in DPME, attach a document code of PICK to your message code in DPME. DPME messages for RFPIC 
require specific customer/carrier/consignee combinations; you cannot use the 
“.ALL” codes.
NOTE A DPME message for RFPIC does not actually print unless you set up 
a real pick document in DOCU and then attach this pick document to an outbound 
flow in DIFP.
PROCESS VALUES
Only required if you are scanning process values
See “Entering Process Values in RFOPS” on page 284 for further information.
SCAN PARAMETER CODE
Only required if you are scanning process values, inventory levels or UI values 
from a bar code label
See “Entering Process Values in RFOPS” on page 284 for further information.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code 
label
You must define a bar code profile in BAPR and attach to it the scan parameter 
code that you set up in SCPR.
PALLET BLOCK If you wish to ship, receive and exchange pallets, you must set the Display Pallet 
Screen field in MRFP (RFPIC tab) to the appropriate value: Display Before Picking or Display on Completion of Picking. 
CONSOLIDATED 
ORDERS
If you consolidate your orders in COPI (Consolidated Pick), you must set the 
Default Mode in MRFP (RFPIC tab) to Only Pallet Picking.
OTHER Picking locations must be attached to a warehouse zone in WHZO.
You need a hold type code of SUSP (Suspend) in HOLD (Hold Types). The Shippable flag must be set to N for No for this code.
FUNCTION KEYS
All Modes
REQUIREMENTS

OUTBOUND PROCESSING
Picking Orders in RFPIC
F1 FN (Function) Allows you to access RFRL, RFPR, RFIT 
and RFLR without leaving RFPIC.
F2 Qu (Query) Displays the first unpicked order line of the 
current order being processed.
F2 CP (Case Pick Mode) Allows you to switch to case pick mode. 
This command is only available before 
selecting an order line.
F3 HD (Hold) Places product on hold.
F4 Ex (Exit) Exit program.
F9 Move cursor to previous field.
Exit Tag screen
F1 GL (Go to Location) Allows you to skip the PRT field and go 
directly to LOCTO field. OPID validation is 
also skipped.
Only used when you wish to print labels 
and validate the OPID in RFST.
Pick List of Order Lines
F1 L1 (Level 1) Changes the function key assignments for 
F1 and F2. If F1 = L1 (item code), pressing F1 will change F1 to L4 (level 4 or lowest) and F2 to LO (location). These new 
function key assignments will allow you to 
change the sequence of order lines to 
either level 4/lowest inventory level or 
location.
F2 L2 (Level 2) Changes the function key assignments for 
F1 and F2. If F2 = LO (location), pressing 
F2 will change F1 to L1 (level 1) and F2 to 
L4 (level 4 or lowest). These new function 
key assignments will allow you to change 
the sequence of order lines to either level 
1 or location.
F3 SL (Select) Selects the order line that the cursor is 
positioned over.
FUNCTION KEYS

OUTBOUND PROCESSING
Picking Orders in RFPIC
PICKING FULL PALLETS FROM BULK
1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.

RFPIC screen
3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.
5 Do one of the following:
F4 CN (Cancel) Exits the pick list without selecting an 
order line.
If you wish to pick by zone:
If you wish to pick by order 
number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order 
number and press Enter.
a) Press Enter to bypass the Zone 
field.
b) If required, key in your warehouse and press Enter.
c) Key in your order number and 
press Enter.
If the default mode for RFPIC has 
been set to Case:
If the default mode for RFPIC has 
been set to Pallet:
The message “You have selected CP 
Mode” will appear.
a) Key in N for No and press Enter.
The message “You have selected NM 
mode” will appear.
a) Press Enter to continue.
FUNCTION KEYS

OUTBOUND PROCESSING
Picking Orders in RFPIC

RFPIC screen showing pick list of order lines, items and locations to pick
6 The pick list of order lines is initially shown in location code sequence. If you wish to display the list in 
Level 1 sequence, press F1 (L1). If you wish to display the list in Level 4 or lowest inventory level 
sequence, press F2 (L4). If the list is in Level 4 sequence, you can press F2 again to return to the location code sequence.
7 Use your arrow keys to position your cursor over the order line that you wish to pick, then press F3 
(Select).

RFPIC screen showing prompt for from location
8 If required, enter or scan in your from location.

OUTBOUND PROCESSING
Picking Orders in RFPIC
9 Enter or scan in your UI (Unique Identifier) as follows:
10 Key in your pick quantity and press Enter. If your pick quantity is less than your order quantity, see “Placing Product on Hold” on page 236 for further instructions.
11 If prompted to do so, enter or scan in your staging location as well as the staging location’s warehouse.
If the order is on a load, the door’s staging location from the load will be shown.
12 When the pick list of unpicked order lines reappears, repeat the above steps for each additional line on 
the order.
13 When you finish entering your order lines, the message “ORDER COMPLETED” may appear. If it does, 
press Enter to acknowledge it.
14 Process another order or press F4 to exit.
PICKING CASES
When you pick cases, you must print a pallet ID label for each pallet that you build. You can place as many 
cases as you want on a pallet, but all cases must belong to the same order; you cannot place product from 
different orders on the same pallet.
If you are picking from a pick line, case pick mode is automatically activated in RFPIC unless the Default 
Mode field in MRFP set to Only Pallet Picking. 
1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.

RFPIC screen
If reserved logic is activated for 
this customer:
If reserve logic is NOT activated 
for this customer:
a) If the lowest inventory level is 
represented by a plus sign (+), 
you can enter any value for that 
level. If the lot number, pallet ID, 
etc. is represented by an actual 
value, you must enter that value; 
any other value will be rejected 
by the system.
a) All inventory levels for the product to be picked will be shown. 
The lot number, pallet ID, etc. 
that you enter must match the 
values displayed on your screen. 
If you attempt to enter different 
values, they will be rejected by 
the system. 

OUTBOUND PROCESSING
Picking Orders in RFPIC
3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.

RFPIC screen prompt to continue in case pick mode
5 Do one of the following:
If you wish to pick by zone:
If you wish to pick by order 
number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order 
number and press Enter.
a) Press Enter to bypass the Zone 
field.
b) Key in your warehouse and 
press Enter.
c) Key in your order number and 
press Enter.
If the default mode for RFPIC has 
been set to Case:
If the default mode for RFPIC has 
been set to Pallet:
The message “You have selected CP 
Mode” will appear.
a) Press Enter to continue.
The message “You have selected normal 
mode” will appear.
a) Key in N for No and press Enter.

OUTBOUND PROCESSING
Picking Orders in RFPIC

RFPIC screen showing list of order lines, items and locations to pick
6 The pick list of order lines is initially shown in location code sequence. If you wish to display the list in 
Level 1 sequence, press F1 (L1). If you wish to display the list in Level 4 or lowest inventory level 
sequence, press F2 (L4). If the list is in Level 4 sequence, you can press F2 again to return to the location code sequence.
7 Use your arrow keys to position your cursor over the order line that you wish to pick.
8 Press F3 (Select).

RFPIC screen showing prompt for from location
9 Enter or scan in your from location.

OUTBOUND PROCESSING
Picking Orders in RFPIC
10 Enter or scan in your UI (Unique Identifier) as follows:
11 Key in your pick quantity and press Enter. If your pick quantity is less than your order quantity, see “Placing Product on Hold” on page 236 for further instructions.
12 Do one of the following:

RFPIC screen showing Print Label (F1) option available
13 Press F1 (Print Label).
If reserved logic is activated for 
this customer:
If reserve logic is NOT activated 
for this customer:
a) If the lowest inventory level is 
represented by a plus sign (+), 
you can enter any value for that 
level. If the lot number, pallet ID, 
etc. is represented by an actual 
value, you must enter that value; 
any other value will be rejected 
by the system.
a) All inventory levels for the product to be picked will be shown. 
The lot number, pallet ID, etc. 
that you enter must match the 
values displayed on your screen. 
If you attempt to enter different 
values, they will be rejected by 
the system. 
If your order consists of a 
single order line:
If your order has multiple 
order lines and you wish to 
pick another line:
If your order has multiple 
order lines and you wish to 
close the pallet and print the 
pallet ID label:
a) Proceed to next step. AccellosOne 3PL will display the 
list of unpicked order lines.
a) Select the line that you wish to 
pick and repeat steps 6 to 12 
for that line.
AccellosOne 3PL will display the 
list of unpicked order lines.
a) Press F4 to exit the list.
b) Proceed to next step.

OUTBOUND PROCESSING
Picking Orders in RFPIC

RFPIC screen showing prompt for label ID
14 Do one of the following:

RFPIC screen showing prompt for to location
15 Enter or scan in your to location. Your to location must be a staging location. If prompted to do so, enter 
your to warehouse.
16 Process another order or press F4 to exit.
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that 
are not generated in 
AccellosOne 3PL: If the Label field is populated:
a) Press Enter to generate your 
pallet ID.
b) If required, key in your printer 
code* and press Enter.
c) If prompted to validate your 
pallet ID, enter or scan it in. 
a) Enter or scan in your pallet ID.
b) If required, key in your printer 
code* and press Enter.
a) If the PRT (Printer) field is not 
populated, key in your printer 
code* and press Enter.
* If you select either SPL or VIEW, no OPID validation will occur.

OUTBOUND PROCESSING
Picking Orders in RFPIC
PICKING PRODUCT WITH PROCESS VALUES
If you are picking cases from a pallet and if there is a balance remaining on the pallet, AccellosOne 3PL will 
prompt you to scan each case ID. If you are unable to scan in each case ID on the pallet for any reason, 
AccellosOne 3PL will present you with the following options:

RFPIC screen showing prompt for catch weight
1 Scan all cases that you are shipping for the pallet. The system will prompt you when you are complete.
2 If you are unable to scan all cases for any reason, press F4 after scanning the last scannable case.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned and 
remove unscanned quantities from the to ship quantity. 
You cannot process the order line again in RFPIC.
4 (Exit, New Line) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned, 
remove the unscanned quantities from the to ship 
quantity and will create a new line for the balance.
5 (Exit, Cancel Picking) Cease scanning and exit without saving any process 
values including those already scanned. The order line 
will revert to its original status before being picked in 
RFPIC.
6 (Replace DAMG) Remove a damaged case from the order and replace it 
with an undamaged case.
7 (Exit Scan, Save) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned.

OUTBOUND PROCESSING
Picking Orders in RFPIC

RFPIC screen showing “Scan incomplete” message
3 Do one of the following:
4 Continue to pick the order line normally in RFPIC.
If you wish to continue from 
where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the 
to ship quantity:
Key in 3 and press Enter.
When prompted to short the order line, key in Y for Yes 
and press Enter.
If you wish to exit, short the to 
ship quantity and create a new 
line for the balance:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values 
and you wish to restore the 
order line to its original state 
before processing in RFPIC:
Key in 5 and press Enter.
When prompted to confirm the cancellation, key in Y
for Yes and press Enter.
If you wish to replace a damaged case:Key in 6 and press Enter.
Scan in the damaged case.
Scan in the replacement case.
If you have multiple damaged cases to replace, you 
must press F4 again and repeat the above steps.
If you wish to exit without saving the scanned process values:
Key in 7 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

OUTBOUND PROCESSING
Picking Orders in RFPIC
PICKING PARTIAL QUANTITIES OF PRODUCT WITH PROCESS VALUES
When picking a partial quantity from a full pallet that has not been picked before and is in a single location, 
you can scan in the cases to be removed rather than the cases to be picked. A partial quantity is defined as 
60% or more of the total quantity in the location. For example, if there are 50 cases in a location and you need 
to pick 30, you can scan in the 20 cases to be removed rather than the 30 cases to be picked. 
This option is designed to save time by reducing the number of cases scanned. It is only available if the 
Number of Days for Label Validation in RF Picking field in MRFP is blank or set to zero.
1 Enter RFPIC.
2 Select the product that you wish to pick from the pick list of order lines.
3 Enter or scan in your from location.
4 Enter or scan in your UI value.
5 Key in your pick quantity and press Enter.
6 If prompted to do so, enter or scan in your staging location as well as the staging location’s warehouse.

RFPIC screen showing prompt to scan cases to be removed
7 Do one of the following:

RFPIC screen showing cases to be removed
If you wish to scan the cases to 
be removed:
If you wish to scan the order 
quantity:
a) Key in Y for Yes and press Enter.
b) Scan in the cases to be 
removed.
a) Key in N for No and press Enter.
b) Scan in the cases to be picked.

OUTBOUND PROCESSING
Picking Orders in RFPIC
8 When all your cases are scanned, process another order line or press F4 to exit.
PICKING RESERVE LOGIC ORDERS
Reserve logic allows you to reserve inventory during order allocation at a level other than the lowest level for 
a customer. By using this option, you allow the RF operator to make the final selection at the lot or pallet ID 
level based on which product is most accessible.
The lot or pallet ID to be selected by the RF operator is indicated by a plus sign (+) in RFPIC.
1 Enter RFPIC.
2 Do one of the following:
RFPIC screen showing + sign in PI (level 3) field
3 Go the location and scan in the from location.
RFPIC screen showing from location
If you wish to pick by zone:
If you wish to pick by order 
number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order 
number and press Enter.
a) Press Enter to bypass the Zone 
field.
b) Key in your warehouse and 
press Enter.
c) Key in your order number and 
press Enter.

OUTBOUND PROCESSING
Picking Orders in RFPIC
4 Scan in the pallet ID that you wish to pick.
RFPIC screen showing selected pallet ID
5 Enter your pick quantity.
6 Scan in your OPID and staging location.
RFPIC screen showing OPID and staging location
7 Press F4 the required number of times to exit.
PLACING PRODUCT ON HOLD
You place product on hold if the product that you wish to pick is damaged or missing. You can place a whole 
pallet on hold or you can place one or more individual cases on hold. When you place a hold on individual 
cases, the number of units placed on hold depends on whether the account is a regular account or a reserve 
logic account.
For regular accounts, the hold applies to the remaining number of units on the order line. For reserve logic 
accounts, the hold applies to the remaining number of units in the entire warehouse up to the inventory level 
that you are reserving at. For example, if you reserve at level 2 and place a partial hold on pallet ID 123, the 
hold will apply to all pallet ID’s in your warehouse for the same level 1 and 2 values.
When you place product on hold, AccellosOne 3PL creates a new line for the missing or damaged product 
and then attempts to allocate the line. For example, suppose you have two orders lines, one of which is 
missing 10 cases. AccellosOne 3PL will create a third order line for the order with a quantity of 10 cases and 
then attempt to allocate this line.

OUTBOUND PROCESSING
Picking Orders in RFPIC
Product placed on hold in RFPIC will be assigned the hold code of SUSP (Suspend) in LOEN (Look Up 
Inventory).
1 Enter RFPIC.
2 Retrieve the order that you wish to process.
3 Use your arrow keys to position your cursor over the order line that you wish to pick and press F3 
(Select).

RFPIC screen showing prompt for from location
REQUIREMENTS
MRFP Suspended holds are not available if the Allow Suspended Holds field in MRFP 
(RFPIC tab) is set to “Split Order Line, No Suspended Holds”.
Suspended holds may require the approval of a supervisor.

OUTBOUND PROCESSING
Picking Orders in RFPIC
4 Do one of the following:
5 If a supervisor is required to approve the hold, the Supervisor Screen will appear.
RFPIC Supervisor screen
If you wish to place the whole 
pallet on hold:
If you wish to place one or 
more cases on hold (nonreserve logic account):
If you wish to place one or 
more cases on hold (reserve 
logic account):
a) Press F3 (Hold). 
RFPIC screen showing 
prompt to place pallet on 
hold
b) If you wish to accept the variance, key in Y for Yes and 
press Enter. If you do not 
accept the variance and wish 
to re-enter the pick quantity, 
key in N for No and press 
Enter.
a) Enter or scan in your from 
location.
b) Enter or scan in your UI.
c) Key in the number of units that 
are NOT on hold and press 
Enter. 
RFPIC screen showing 
an allocated quantity of 5 
cases and a pick quantity 
of 3 cases
d) If you wish to accept the variance, key in Y for Yes and 
press Enter. If you do not 
accept the variance and wish 
to re-enter the pick quantity, 
key in N for No and press 
Enter.
▪ If you keyed in Y for Yes, AccellosOne 3PL will create a new line for 
the remaining number of units — that 
is, the number of units on hold. 
a) Enter or scan in your from 
location.
b) Enter or scan in your UI.
c) Key in the number of units that 
are NOT on hold and press 
Enter.
d) Press F3 (Hold) to place the 
remaining units in your warehouse on hold.
e) If you wish to accept the variance, key in Y for Yes and 
press Enter. If you do not 
accept the variance and wish 
to re-enter the pick quantity, 
key in N for No and press 
Enter.

OUTBOUND PROCESSING
Picking Orders in RFPIC
After signing on, the supervisor will be prompted to accept or reject the hold.
RFPIC Supervisor screen showing mismatched quantity
6 If the supervisor approves the hold, enter or scan in your staging location.
7 When the pick list of unpicked order lines appears, do one of the following:
ENTERING PALLET INFORMATION
If the Display Pallet Screen field in MRFP (RFPIC tab) is set to either Display Before Picking or Display on 
Completion of Picking, you will be prompted to enter pallet information for the order.
1 Enter RFPIC.
2 Enter your zone and/or warehouse and order number in the usual manner.
RFPIC screen showing Pallet Block
If you placed the entire pallet on 
hold in step 4:
If you placed one or more cases 
on hold in step 4:
a) Process the remaining order 
lines in the normal manner.
a) Select the new line created by 
AccellosOne 3PL for the remaining number of units.
b) Process this line in the normal 
manner.
c) Process the remaining order 
lines in the normal manner.

OUTBOUND PROCESSING
Picking Orders in RFPIC
3 When the Pallet Block appears, do one of the following:
4 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick 
list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate 
code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
5 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
6 Key in your pallet code and press Enter or use your pick list to select it.
7 Key in the number of pallets that you are shipping or receiving and press Enter.

RFPIC screen showing prompt for reference information
8 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not 
require a remark, press Enter to bypass this field.
9 If required, repeat the above steps to add additional lines in the Pallet Block.
10 When you finish adding your lines, press F4 to exit Create Mode. AccellosOne 3PL will display the last 
pallet details record that you entered. If you have multiple pallet transactions for this order, you can use 
your up and down arrow keys to scroll through the list of records.
If you wish to record pallet 
information for the order:
If you do NOT wish to record 
pallet information for the order:
a) Proceed to next step. a) Press F4 twice to exit the Pallet 
Block.
b) Continue to process the order in 
the normal manner.
Received Received means that you are receiving pallets from the 
account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the 
account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even 
exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 
of your own pallets so that there is no change to your 
pallet balances.

OUTBOUND PROCESSING
Picking Orders in RFPIC
If you wish to delete a pallet transaction, select the transaction that you wish to delete with your arrow 
keys. Then press Enter until your cursor is positioned in the NUM PALL field and press F2 (DE).
11 Press F4 again to exit the Pallet Block.
12 Continue to process your order in the normal manner.
EXCLUDING ORDERS FROM OVERPICKING IN EOSU
If the overpicking of order lines is activated in PIPR for a given customer, item or consignee, you can override 
the flag — that is, exclude an individual order from overpicking — in EOSU (Exclude Orders from Substitution/Overpicking). When an order is excluded from overpicking, the to ship quantity cannot exceed the order 
quantity.
1 Enter EOSU.

EOSU screen
2 In the Mode field, select Over-Pick from the dropdown list.
3 Key in your search criteria for the orders that you wish to exclude and click on Execute Query to 
execute the query.

OUTBOUND PROCESSING
Picking Orders in RFPIC

EOSU screen showing all open orders for carrier ABC
4 Proceed to select the orders that you wish to exclude from overpicking as follows:
5 When you finish selecting your orders, click on Enable RF Overpick . The Substitution Flag beside 
the selected order(s) will change from N or blank to Y. If you make a mistake and wish to reverse your 
action, select the orders that you enabled and click on Disable RF Over-Pick .
6 Click on Exit to exit EOSU.
PICKING PICK LINE PRODUCT FROM A NON-PICK LINE LOCATION
You can allow operators to pick pick line product from a non-pick line location such as bulk or rack when 
multiple replenishments for the same product cause overcrowding in your pick line. This choice is available 
when the full order quantity is not available in the pick line location and a replenishment has been generated.
If you wish to: You:
select a single order click in the checkbox beside the 
order
select all orders
click on Select All 
deselect a single order click in the checkbox beside the 
selected order
deselect all orders
click on Deselect All 

OUTBOUND PROCESSING
Picking Orders in RFPIC
For example, suppose your order quantity is 10 cases, there are only five cases in the pick line and the 
replenishment quantity is 60 cases. The operator can choose to pick the 10 cases from a bulk or non-pick line 
location instead of waiting for a replenishment and picking from the pick line. The 10 cases picked from bulk 
is subtracted from the replenishment quantity; 60 -10 = 50.
RFPIC screen showing prompt to pick from replenishment location rather than pick line location
To activate pick line picking from a non-pick line location, you must set the flag in MRFP called Allow Picking 
Outside of Pick Line to Yes.
PERFORMING REPLENISHMENTS IN RFPIC
You can allow operators to perform replenishments in RFPIC if their equipment permits it; you can either allow 
it on a permanent basis or you can give each operator the choice each time that he or she logs on.
You define your RF pick line/replenishment rules in a field in MRFP called Replenishment Rules for Pick Line. 
There are three options in this field:
1) REPI is done inside of RFPIC
2) REPI is done separately (that is, in RFRP or RFPL)
3) Determined by the user
LOOKING UP REMARKS AND MESSAGES IN RFPIC
There are four types of remarks/messages in RFPIC:
▪ order header remarks prefixed by the number 0
▪ order line remarks prefixed by the line number (for example, 1, 2, 3)
▪ item messages set up in ITEM
▪ depositor print messages set up in DPME 
When you enter the order header in RFPIC, all remarks/message are displayed in the following order:
▪ order header remarks
▪ line remarks
▪ item messages set up in ITEM
▪ depositor print messages set up in DPME
1 Enter RFPIC and retrieve the order whose remarks/messages you wish to look up. The remark/message 
will display automatically when you retrieve the order.

OUTBOUND PROCESSING
Picking Orders in RFPIC

RFPIC screen showing header and line remarks
2 If the remarks are more than six lines long, use your up and down arrow keys to scroll through the remark 
lines. 
3 If there are multiple remarks/messages attached to the order, press Enter or F4 to jump to the next message.

4 Continue to process the order normally.
RECOVERING FROM A DROPPED CONNECTION
If equipment tracking is activated in your system and if your RF connection is dropped in the middle of a pick 
(that is, you have selected an order line to pick and validated the UI but have not yet assigned an OPID to it), 
you will be prompted to select one of the following two options:
▪ finish the pick using your existing material handling equipment code
▪ change your material handling equipment code and exit the order without completing the pick
1 When you re-enter RFPIC/RFOLP, the following screen will appear:
RFPICK screen showing prompt to continue
2 Press Enter to continue.

OUTBOUND PROCESSING
Picking Orders in RFPIC
RFPICK screen showing prompt to stage or exit
3 Do one of the following:
If you wish to stage the product 
with your existing material 
handling equipment code:
If you wish to change your 
material handling equipment 
code and exit the order without 
completing the pick:
a) Press F3 (Stage).
RFPIC screen showing 
prompt for to location
b) Scan or manually enter your 
staging location.
a) If prompted to do so, perform any 
required equipment checks.
a) Press F4 (Exit).
RFPIC screen showing 
prompt for MHE code
b) Key in your new equipment type 
code and press Enter.
c) If prompted to do so, perform any 
required equipment checks.

OUTBOUND PROCESSING
Performing Inventory Count Backs
Performing Inventory Count Backs
You can perform inventory counts while picking in RFPIC if the Activate Inventory Count flag in MRFP is set to 
a value other than Never and if the order has not been assigned to a load in ENOR whose load type excludes 
count backs.
If the count does not match the on hand quantity, an inventory discrepancy record will be created in the 
program ICIN (Inventory Count Investigation). Depending on the option that you choose in the Inventory 
Count Rules field in MRFP, a supervisor may be required to log on and flag the discrepancy as either resolved 
or unresolved before you can pick the order line.
There are six steps to follow in performing count backs:

OUTBOUND PROCESSING
Performing Inventory Count Backs
PERFORMING THE COUNT IN RFPIC
1 Enter RFPIC.
Product is assigned to load.
Supervisor 
login
ICIN
If second count fails, supervisor must login to 
authorize.
Supervisor can resolve the discrepancy in 
ICIN, RFCI or RFCL.
RFPIC
SELO
RF operator prompted to enter quantity of 
remaining product in location.
5
1
2
4
Operator 
count matches 
system count?
End recount
Yes No
Resolved?
End
Yes No
Resolved?
End
Yes No
OLOP
If discrepancy is still unresolved, operator 
will not be allowed to load the product.
End
Discrepancy record created. 3
6

OUTBOUND PROCESSING
Performing Inventory Count Backs
2 Retrieve the order that you wish to pick.

RFPIC screen showing pick list of order lines
3 Select the order line that you wish to pick.
4 Enter your from location.
5 Enter your UI value.
6 Key in your pick quantity and press Enter.

RFPIC screen showing prompt for remaining quantity
7 Key in the quantity of product remaining in the location and press Enter. If the location contains mixed 
product, count only the product that you are picking.

OUTBOUND PROCESSING
Performing Inventory Count Backs
8 Do one of the following:
9 Continue to pick the order in the normal fashion.
LOOKING UP INVENTORY DISCREPANCY RECORDS IN ICIN
You look up inventory discrepancy records in ICIN (Inventory Count Investigation). Inventory discrepancy 
records remain in ICIN until you delete them or assign them to a work request in CRME (Enter CRM 
Request).
1 Enter ICIN.
2 Click on Enter Criteria.
If the quantity that you enter 
matches the on-hand quantity:
If the quantity that you enter 
does NOT match the on hand 
quantity:
a) Proceed to next step. The following message will appear:
a) Press Enter to acknowledge the 
message and re-enter your 
count.
b) Key in the remaining quantity 
again and press Enter.
c) If prompted to do so, press Enter 
again to acknowledge the “Incorrect 2nd Count” message.
d) If the Supervisor Screen 
appears, a supervisor must log 
on and enter either Y to flag the 
discrepancy as resolved or N to 
flag the discrepancy as unresolved.
e) Proceed to next step.

OUTBOUND PROCESSING
Performing Inventory Count Backs
3 Do one of the following:
4 Click on Execute Query.

ICIN screen showing a discrepancy for item 11111
5 Use your arrow keys to scroll through the list of records. 
6 When you finish viewing your inventory discrepancy records in ICIN, click on Return to Main and Exit.
LOOKING UP INVENTORY DISCREPANCY RECORDS IN RFCL
You must have supervisor access in OPER (Operator Code) before you can look up inventory discrepancy 
records in RFCL (RF Count Log).
1 Enter RFCL.
If you wish to view all records in 
ICIN:
If you wish to restrict your query 
to certain records:
a) Proceed to next step. a) Enter the appropriate search criteria (order number, line number, operator code, etc.).

OUTBOUND PROCESSING
Performing Inventory Count Backs

RFCL screen
2 Do one of the following:
3 Click on Execute Query.

RFCL screen showing discrepancy record for item D1
4 Use your arrow keys to scroll through the list of records. 
5 When you finish viewing your inventory discrepancy records in RFCL, press F4 to exit.
REMOVING INVENTORY DISCREPANCY RECORDS FROM ICIN
There are two methods of removing records from ICIN: you can delete the record using the Delete command 
or you can create a work request for the discrepancy in CRME and AccellosOne 3PL will delete the record 
automatically. Regardless of the option that you choose, AccellosOne 3PL will create an IF (Information Only) 
record in the History Block of LOEN.
If you wish to view all records in 
RFCL:
If you wish to restrict your query 
to certain records:
a) Proceed to next step. a) Enter the appropriate search criteria (UI number, order number, 
customer code, etc.).

OUTBOUND PROCESSING
Performing Inventory Count Backs
1 Enter ICIN.
2 Retrieve the record that you wish to remove.
3 Do one of the following:
4 Click on Return to Main and Exit.
REMOVING INVENTORY DISCREPANCY RECORDS IN RFCL
You must have supervisor access in OPER (Operator Code) before you can remove inventory discrepancy 
records in RFCL (RF Count Log).
1 Enter RFCL.
2 Retrieve the record that you wish to remove.
3 Press F3 (Rm).
4 When the message “Record is Deleted Enter to Continue” appears, press Enter to continue.
5 Press F4 to exit.
REMOVING INVENTORY DISCREPANCY RECORDS IN RFCI
This program allows RF supervisors to clear inventory investigations when there are multiple ICIN records for 
the same inventory entity. There are three different options in RFCI:
▪ you can clear the currently selected OPID
▪ you can clear all OPID's on open orders with the same inventory levels up to level 3
▪ you can exit out without clearing any OPID's (that is, the variance remains unresolved)
When you clear an ICIN record, any SUSP holds on the product are removed.
1 Enter RFCI.
If you wish to delete the record: 
If you wish to create a work 
request in CRME:
a) Click on Delete.
b) If required, enter your remarks 
for the transaction.
a) Click on CRM Entry.
b) Click on Create Record.
c) Proceed to enter your work 
request. Refer to the Operations 
2 Guide for further information on 
entering work requests in CRME.
d) When you finish entering your 
work request, click on Exit.

OUTBOUND PROCESSING
Entering Temperature and Trailer Information in RFTT
RFCI screen
2 Enter or scan the OPID that you wish to clear.
RFCI screen showing three options
3 If there are multiple records for a single OPID, use your arrow keys to select the record that you wish to 
clear.
4 Press Enter to position your cursor in the Option field.
5 Key in the appropriate option (1, 2 or 3) and press Enter.
Entering Temperature and Trailer Information in RFTT
This program allows you to enter temperature, trailer/seal number and pallet information for a given receipt or 
order without working in RFCH or RFPIC. The information that you can enter in RFTT for a receipt — temperature only, trailer/seal number only, temperature and trailer/seal number, etc. — depends on which option you 
choose in the Show Temperature and Pallet Blocks field in MRFP.
1 Enter RFTT.

OUTBOUND PROCESSING
Entering Pallet Information in RFOPE
RFTT screen
2 Key in your order number and press Enter.
3 Enter your temperature, trailer/seal number and pallet information in the usual manner.
Entering Pallet Information in RFOPE
If the Pallet Block is deactivated in RFPIC, you can use the stand-alone program RFOPE (RF Order Pallet 
Entry) to enter your pallet information.
1 Enter RFOPE.
RFOPE screen
2 Key in your order number and press Enter.

OUTBOUND PROCESSING
Entering Pallet Information in RFOPE
RFOPE screen showing prompt for account code
3 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick 
list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate 
code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
RFOPE screen showing prompt for transaction type
4 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
5 Key in your pallet code and press Enter or use your pick list to select it.
Received Received means that you are receiving pallets from the 
account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the 
account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even 
exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 
of your own pallets so that there is no change to your 
pallet balances.

OUTBOUND PROCESSING
Entering Pallet Information in RFOPE
6 Key in the number of pallets that you are shipping or receiving and press Enter.

RFOPE screen showing prompt for reference information
7 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not 
require a remark, press Enter to bypass this field.
8 If required, repeat the above steps to add additional lines in the Pallet Block.
9 When you finish adding your lines, press F4 to exit Create Mode.
10 Press F4 again to exit RFOPE.
EDITING A PALLET DETAILS RECORD IN RFOPE
If pallet details have already been entered for an order in RFPIC or ENOR, you can edit the pallet details in 
RFOPE.
1 Enter RFOPE.
2 Key in your order number and press Enter.
RFOPE screen showing existing pallet details record
3 Proceed to make any required changes to your pallet details.
4 When you finish making your changes, press F4 the required number of times to exit.

OUTBOUND PROCESSING
Adjusting Your Pallet Type in RFPA
DELETING A PALLET DETAILS RECORD IN RFOPE
1 Enter RFOPE.
2 Key in your order number and press Enter.
3 Press Enter until your cursor is in the NUM PALL field.
RFOPE screen showing existing pallet details record
4 Press F2 (DE).
5 Press F4 the required number of times to exit.
Adjusting Your Pallet Type in RFPA
You can adjust your pallet type for an OPID (outbound pallet ID) in RFPA (RF Pallet Code Update). If the 
OPID has already been assigned a pallet type, the CUR PALL TYPE field will be populated with the current 
pallet type. If the OPID has never been assigned a pallet type, the CUR PALL TYPE field will be blank.
1 Enter RFPA.
RFPA screen

OUTBOUND PROCESSING
Looking Up Your OPID’s
2 Enter or scan in your OPID.
RFPA screen showing current pallet type plus prompt for new pallet type
3 If you make a mistake, you can press F3 (CL) to clear the OPID and start over again.
4 Key in your new pallet type and press Enter or press F1 (PL) to select it from the pick list.
RFPA screen showing “Enter to continue” message
5 Press Enter to confirm the update.
6 Press F4 to exit.
Looking Up Your OPID’s
There are three ways of looking up your OPID’s (outbound pallet ID’s):
▪ from the desktop program LOCN (Look Up Carton)
▪ in the RF program RFNCO (OPID Look-Up)
▪ from the desktop program LOOR (Look Up Orders)

OUTBOUND PROCESSING
Looking Up Your OPID’s
LOOKING UP YOUR OPID’S IN LOCN
You can look up OPID’s (outbound pallet ID’s) in LOCN (Look Up Carton). OPID’s are created when you 
perform case picking in RFPIC. When you look up OPID’s, AccellosOne 3PL shows the customer code, level 
1 value, order number and line number for each inventory entity on the pallet.
1 Enter LOCN.
2 Click on Enter Query.
3 Enter or scan in your OPID and click on Execute Query.
LOCN screen showing three inventory entities on the pallet
4 When you finish looking up your OPID, click on Exit to exit.
LOOKING UP YOUR OPID’S IN RFNCO
This RF program allows you to look up the product on an OPID (outbound pallet ID). It is similar to RFCO (RF 
Confirm OPID) but without the F3 (Process) command.
The Line Block shows each order line assigned to the OPID; that is, the order number, line number, customer, 
all inventory levels, the staging location and the quantity. Records in the Line Block are sorted by date and 
time stamp based on the STPI (Start Picking) flow with the oldest records shown first followed by the newer 
records.
1 Enter RFNCO.

OUTBOUND PROCESSING
Looking Up Your OPID’s
RFNCO
2 Key or scan in your OPID.
RFNCO screen showing two order lines attached to OPID 00002240
3 If there are multiple records in the Line Block, you use your Up and Down arrow keys to scroll through the 
list.
4 When you finish looking up your OPID’s, press F4 the required number of times to exit.
LOOKING UP AN ORDER’S OPID’S IN LOOR
You can look up an order’s OPID’s in the Location Block of LOOR.

OUTBOUND PROCESSING
Confirming Orders by OPID in RFCO
LOOR screen showing OPID for order line 1
Confirming Orders by OPID in RFCO
This program allows you to confirm orders by OPID (outbound pallet ID) without the need to confirm the entire 
order in CHOF. If an OPID contains multiple order lines, you can confirm individual orders lines or you can 
confirm all order lines assigned to the OPID. If you choose to confirm individual order lines, the Shipped Date 
field in the Line Block of LOOR will be populated for each order line confirmed in RFCO.
1 Enter RFCO.
REQUIREMENTS
FLOWS The order must be picked.
DOCUMENTS You cannot use RFCO if you print one or more documents at your FIPI (Finish 
Picking) flow because the flow FIPI is bypassed in RFCO. To use RFCO, you 
must move your document(s) to the COOR (Confirm Order) flow.
OTHER See Miscellaneous 2 tab in MRFP.

OUTBOUND PROCESSING
Confirming Orders by OPID in RFCO
RFCO screen
2 Press Enter to scan in your OPID.
RFCO screen showing F3 (Process command)

OUTBOUND PROCESSING
Confirming Individual Order Lines by UI in RFCU
3 Do one of the following:
4 Repeat the above steps for another OPID or press F4 (EX) to exit.
Confirming Individual Order Lines by UI in RFCU
This program allows you to confirm individual order lines by UI. When you look up the order in LOOR, the 
Shipped Date field in the Line Block will be populated for each order line confirmed in RFCU.
1 Enter RFCU.
To confirm individual order lines:
To confirm all order lines 
assigned to the OPID:
a) Press F1 (LN) to enter the Detail 
Block of RFCO.
b) Use your arrow keys to scroll 
through the list of order lines.
c) When you reach the order line 
that you wish to confirm, press 
Enter to select it.
d) When prompted to confirm the 
order line, press Enter to accept 
the default value of Y(es).
a) Press F3 (PR) to process it.

OUTBOUND PROCESSING
Reprinting Outbound Labels in RFOLP
RFCU
2 Key in your order number and press Enter.
3 Scan in your UI value.
RFCU screen showing prompt to continue
4 Press Enter to confirm the order line.
5 Press F4 to exit.
Reprinting Outbound Labels in RFOLP
In this program, you can reprint outbound labels for orders that have already been picked in RFPIC. There 
are two reprint modes in RFOLP depending on the outcome of label printing in RFPIC.
If the original label printed correctly in RFPIC, you enter the UI value of the order line or the OPID of the 
original label in RFOLP. If label printing failed in RFPIC due to a lost connection or loss of power, AccellosOne 
3PL will generate an internal tag number and attach this tag number to all order lines that have been picked. 
The way that you process these order lines that have been picked depends upon how you create your 
OPID’s:

OUTBOUND PROCESSING
Reprinting Outbound Labels in RFOLP
▪ if you manually create your OPID’s, you must enter ENOR and change the tag number in the Process 
Block to the desired OPID number and use this number as your OPID number (AccellosOne 3PL will 
replace the tag number for all order lines that have been picked by the new OPID number)
▪ if your OPID’s are system generated, you must enter LOOR and look up the tag number assigned to the 
order line in the Process Block and use this tag number as your OPID number (when you finish reprinting in RFOLP, AccellosOne 3PL will assign the new system-generated OPID number to all order lines 
that have been picked)

LOOR screen showing tag number generated in Process Block when label printing fails
1 Do one of the following:
2 Enter RFOLP.
REQUIREMENTS
CASE PICKING See RFPIC.
If you wish to reprint a previously 
printed label:
If you need to create a new label 
because label printing failed in 
RFPIC:
a) Proceed to next step. a) Enter LOOR.
b) Retrieve the order whose label 
printing failed.
c) Open the Process Block and 
look up the system-assigned tag 
number. Use this value as your 
OPID.

OUTBOUND PROCESSING
Reprinting Outbound Labels in RFOLP

RFOLP screen
3 Key in your order number and press Enter.
4 Do one of the following:

RFOLP screen showing prompt for number of labels to print
5 Key in the number of labels that you wish to print/reprint and press Enter.
6 Do one of the following:
If you wish to scan in the UI 
value:
If you wish to scan in the 
outbound pallet ID:
a) Enter or scan in your UI value.
b) If a single UI value has multiple 
OPID’s, select the appropriate 
OPID from the pick list.
a) Press Enter to bypass the UI 
field.
b) Enter or scan in your OPID.
If the printer code is displayed:
If the printer code is NOT 
displayed:
a) Press Enter to accept it or key in 
a new printer code and press 
Enter.
a) Key in your printer code and 
press Enter.

OUTBOUND PROCESSING
Picking Cases from a Pick Line in CASE
Picking Cases from a Pick Line in CASE
In this program, you can pick partial quantities (that is, less than a full pallet) from a pick line in Skip mode. In 
Skip mode, automatic replenishment is deactivated and the picker can select any pick line inventory from any 
pick line location whose level 1 value matches the level 1 value of the order line.
CASE is designed for fast-moving pick lines in which old product (that is, allocating in FIFO/LIFO sequence) 
is not an issue and manual procedures are in place to ensure that the pick line never runs out of product. If 
you activate Skip mode, you will not be able to pick partial quantities from a pick line in RFPIC.
When you allocate an order in Skip mode, the following events occur in AccellosOne 3PL:
▪ the P-type order line for the pick line quantity will not be changed to R for Regular
▪ the Location Status field of the order header will be updated to “Entered”, but no locations will be 
assigned to the order lines
▪ no replenishments will be generated
NOTE If the order quantity is such that both a bulk pick and a pick line pick are 
required (for example, order quantity = 110 cases or 1 pallet/10 cases), AccellosOne 
3PL will create a second order line for the pick line pick. However, the non-pick line 
pick will allocate normally; that is, the P-type line will change to R for Regular.
REQUIREMENTS
FLOWS See “Picking Orders in RFPIC” on page 220 for further information.
CASE PICK LABEL See “Picking Orders in RFPIC” on page 220 for further information.
INVENTORY LEVELSCASE supports three-level accounts only.
OTHER You need a pick line for the product that you wish to pick in CASE. See the Allocation and Wave Manager for instructions on setting up a pick line.
In the DSRP (Depositor Shipping and Receiving) record attached to the customer 
that you are setting up for CASE picking, the Change Zero Pending Line to RType Line field must be set to N for No.
In the PIPR (Picking Profile) record attached to the customer that you are setting 
up for CASE picking, the following setups are required:
▪ Use FIFO/LIFO for Pick Line Picking or Skip = S for Skip
▪ Exclude Pick Line Stock When Bulk Picking = Y for Yes

OUTBOUND PROCESSING
Picking Cases from a Pick Line in CASE
PIPR screen showing required setup for CASE
REQUIREMENTS

OUTBOUND PROCESSING
Picking Cases from a Pick Line in CASE
1 Enter CASE.

CASE screen
2 Enter or scan in your order number.
PROCESS VALUESSee “Picking Orders in RFPIC” on page 220 for further information.
SCAN PARAMETER CODEOnly required if you are scanning process values, inventory levels or UI values 
from a bar code label
See “Picking Orders in RFPIC” on page 220 for further information.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code 
label
See “Picking Orders in RFPIC” on page 220 for further information.
HOLDS See “Picking Orders in RFPIC” on page 220 for further information.
REQUIREMENTS

OUTBOUND PROCESSING
Picking Cases from a Pick Line in CASE

CASE screen showing pick list of possible pick locations for order line 1
AccellosOne 3PL will display all locations in the pick line containing the product whose level 1 value 
matches the level 1 of the order line. For each location, CASE will display the order line number, warehouse, level 1 value and pick quantity.
3 Use your arrow keys to position your cursor over the order line/location that you wish to pick, then press 
F3 (Select).

CASE screen showing prompt for UI value
4 If you make a mistake and wish to work on another order or order line, press F2 (QU for Quit) to position 
your cursor in the Ord# field. Then enter or scan in another order number or press Enter to work on the 
same order but a different order line.
5 Enter or scan in your UI value.
Record 1
Record 2

OUTBOUND PROCESSING
Picking Cases from a Pick Line in CASE

CASE screen showing prompt for pick quantity
6 Key in your quantity and press Enter. The quantity that you enter must be less than or equal to the available quantity in the location.
7 Repeat the above steps for each additional order line to be picked from the pick line.
8 When you finish picking all your order lines, the “Case pick completed” message will appear. Press F4 
(Rt) to display the case pick label screen.

CASE screen showing case pick label screen
9 Do one of the following:
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that 
are not generated in AccellosOne 3PL: If the Label field is populated:
a) Press Enter to generate your 
pallet ID.
b) Key in your printer code and 
press Enter.
a) Enter or scan in your pallet ID. a) If the PRT (Printer) field is not 
populated, key in your printer 
code and press Enter.
Available quantity in location 

OUTBOUND PROCESSING
Merging OPID’s in RFOPB

CASE screen showing completed case pick label screen
10 Press F4 (Rt) to close the case pick label screen.
11 Press F4 (EX) again to exit CASE.
Merging OPID’s in RFOPB
In this program, you can merge two or more separate picks (a case pick and an each pick) into a single pallet 
under a new OPID. When you finish merging your picks, you will be prompted to print a label for the new 
OPID.
1 Enter RFOPB.
REQUIREMENTS
FLOWS See “Picking Orders in RFPIC” on page 220 for further information.
CASE PICKING See “Picking Orders in RFPIC” on page 220 for further information.
ENOR Each pick must be a separate order line on the same order.
LABELS You need a label set up in DOCU and this label must be attached to the appropriate customers and consignees in CCDU (Customer / Consignee Document 
Setup). The pick method must be set to each.

OUTBOUND PROCESSING
Merging OPID’s in RFOPB
RFOPB screen
2 Enter or scan your new OPID.
RFOBP screen showing prompt for carton ID
3 Enter or scan in your first OPID.
RFOBP screen showing prompt for carton ID

OUTBOUND PROCESSING
Merging OPID’s in RFOPB
4 Enter or scan in your second OPID.
5 Enter or scan in any additional OPID’s that you wish to merge.
6 When you finish scanning in your from OPID’s, press F3 (Process).
RFOBP screen showing prompt for printer code
7 Key in your printer code and press Enter.
8 Press F4 to exit.
LOOKING UP YOUR NEW OPID
You can look up your new OPID in the Time Block of LOOR.
LOOR screen showing new OPID

OUTBOUND PROCESSING
Picking Substitution
Picking Substitution
Picking substitution allows RF operators to pick product other than the allocated product on the order line. 
Depending on the options that you choose, the substitute product:
▪ may or may not be allocated to another order
▪ may or may not be from the same location
▪ may or may not have the same FIFO attributes
▪ may or may not have the same level 2/3/4 values 
Regardless of the option that you choose, if the original order line has a hold code, the substitute product 
must have the same hold.
Picking substitution is designed to achieve faster picking and increased productivity for the warehouse by 
allowing operators to pick the most accessible product in a given location or area without sacrificing FIFO or 
other picking requirements.
It is only available for RF picking in the program RFPIC. When the picker enters an inventory level value other 
than the value of the allocated line, AccellosOne 3PL will evaluate a) whether picking substitution is allowed 
and b) if it is allowed, whether the product picked as a substitute is acceptable.
If picking substitution is not activated, the picker can only pick product not on the order line if reserve logic is 
activated.
SETTING UP PICKING SUBSTITUTION
There are three steps to follow in setting up picking substitution.
▪ You set up your picking substitution rules in PSPR (RF Substitution Profile Code). 
▪ You attach your RF substitution profile code to PIPR (Picking Profile Code). 
▪ You attach your PIPR profile code to the appropriate records in ITEM, CONS, CCOP, HOLD or DSRP.
NOTE Picking substitution offers more flexibility at picking time than does reserve 
logic. You can pick product from a location other than the pick location, you can pick 
product whose level 2/3/4 value is not an exact match of the product on the order, you 
can pick product with a variable quantity breakdown and you can pick product on 
another open order.

OUTBOUND PROCESSING
Picking Substitution
SETTING UP YOUR PICKING SUBSTITUTION RULES IN PSPR
You set up your picking substitution rules in PSPR. Picking substitution rules are always location type 
dependent; that means that you can set up one set of picking substitution rules for your rack locations and a 
completely different set of picking substitution rules for your pick line locations.
FIELD DESCRIPTIONS
Substitution Profile Code Mandatory
Your RF substitution profile code.
Description Mandatory
The description for your RF substitution profile code.
Enable Replenishment 
Substitution
Y = Yes
N = No
If you select Y for Yes, your picking substitution rules will apply to replenishments as well. If you select N for No, your picking substitution rules will apply 
to picking only.
LOCATION TYPE BLOCK
Location Type Code
(defined in LOTP)
Mandatory
The location type code for your RF substitution profile code.
Sort Sequence Code
(defined in SOSE)
Optional
If you attach a SOSE code to your location type, the substitution pick list in 
RFPIC will be sorted in the order that you specify.

OUTBOUND PROCESSING
Picking Substitution
Range in Days Mode A = Allocated Lot, allocation time (default)
O = Oldest Lot
If you select A for Allocated Lot, your range in days value will be based on the 
originally allocated product’s receipt/expiry date. If you select O for Oldest Lot, 
your range in days value will be based on the oldest lot at the time of allocation.
Range in Days from Originally Allocated EntityOnly available if Range in Days Mode = blank or A for Allocated Lot, if relative 
FIFO picking is activated in PIPR and if the PSPR rule “Substitute product 
must have equivalent FIFO attributes” is chosen
The number of days that the substitute product’s receipt/expiry date can 
exceed the originally allocated product’s receipt/expiry date. 
EXAMPLE
Suppose you set the Range in Days from Oldest Lot to 10 in PIPR and the 
Range in Days from Originally Allocated Entity in PSPR to 5. During allocation, AccellosOne 3PL selects Jan. 7 as the lot to pick even though the oldest 
lot is Jan. 1. If the picker elects to pick substitute product in RFPIC, any lot up 
to Jan 12 will be accepted.
If you leave this field blank, the value of zero will be assumed and the substitute product’s receipt/expiry date must match the original product’s receipt/
expiry date. 
NOTE If your customer has specific FIFO rules such as never ship anything with a date greater than 20 days from the oldest lot, you must make sure 
that the sum of the Range in Days from Oldest Lot value in PIPR and the 
Range in Days from Originally Allocated Entity value in PSPR does not 
exceed 20. 
For example, you could set both values to 10 (10 + 10 = 20) or your PIPR 
value could be 15 and your PSPR value could be 5. However, you could not 
set your PIPR value to 15 and your PSPR value to 10 because product with a 
date greater than 20 days from the oldest lot might be shipped.
Range in Days from Oldest Lot During AllocationOnly available if Range in Days Mode = O for Oldest Lot, if relative FIFO picking is activated in PIPR and if the PSPR rule “Substitute product must have 
equivalent FIFO attributes” is chosen
The number of days that the substitute product’s receipt/expiry date can 
exceed the oldest lot at the time of allocation. 
LOCATION TYPE BLOCK

OUTBOUND PROCESSING
Picking Substitution
There are five logical groups in PSPR. Each group has two or more mutually exclusive options. From each 
group, you select the appropriate option.
1 Enter PSPR.
2 Click on Create Record.
3 Key in your substitution profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 In the Enable Replenishment Substitution field, key in N for No or Y for Yes and press Enter.
6 In the Location Type Block, click on Return to Main.
7 Click on Create Record.
8 In the Location Type field, key in your location type code and press Enter or use the pick list function to 
select it.
Do not use stock allocated to other orders as substitute
Use stock allocated to other orders for same location only (not available if the picking substitution profile code attached to the customer differs from the picking substitution code 
attached to the consignee)
Substitute product must come from same location only
Substitute product must come from same type of locations (LOTP)
Substitute product can come from any location (not available for pick line locations)
Substitute product must have equivalent FIFO attributes
Ignore FIFO requirement for substitute product
Substitute product must be same inventory up to level 1
Substitute product must be same inventory up to level 2
Substitute product must be same inventory up to level 3
Substitute product must be same inventory up to level 4
Use traditional range in days mode
Use extended range in days mode based on all allocated order lines
The traditional range in days mode option looks at a single order only. The extended range in 
days option, on the other hand, looks at all allocated order lines. For example, if your range 
in days value is 5, the substitute product’s receipt/expiry date can exceed the receipt / expiry 
date of any allocated product that has not been picked.
NOTE The picking substitution rules that you define in PSPR override any picking 
parameters that you define in ILOP. For example, if you select “pick to clean” in ILOP 
and if the operator decides to pick from another location, that location may not satisfy 
the pick to clean requirement. In other words, the operator may pick from a less desirable location according to ILOP.

OUTBOUND PROCESSING
Picking Substitution
9 If required, key in your sort sequence code and press Enter or use the pick list function to select it. If you 
do not require a sort sequence code, press Enter to bypass this field.
10 In the Range in Days Mode field, key in A for Allocated Lot or O for Oldest Lot and press Enter.
11 If required, key in the number of days in the Range in Days from Originally Allocated Entity field and 
press Enter.
12 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you 
wish to choose and then click on Add Option.
13 Repeat the previous step for each set of parameters.
14 When you finish selecting your parameters, click on Location Type Block.

PSPR screen showing picking rules for BULK options
15 Click on Master Block and Exit to exit.
ATTACHING YOUR PSPR PROFILE CODE TO THE APPROPRIATE CODE
First, attach your PSPR profile code to PIPR (Picking Profile Code). Next, attach your PIPR profile to the 
appropriate code (ITEM, CONS or DSRP). If you are attaching picking profiles to items and consignees as 
well to customers, the following logic will apply:
▪ the profile that you attach to DSRP is the default
▪ if you attach a picking profile to ITEM, it will override the profile in DSRP
▪ if you attach a picking profile to CONS, it will override the profiles in DSRP and ITEM (you cannot use 
the “Use stock allocated to other orders for same location” option in PSPR when attaching a picking profile to CONS)

OUTBOUND PROCESSING
Picking Substitution
EXCLUDING ORDERS FROM PICKING SUBSTITUTION IN EOSU
You can exclude open orders from picking substitution in EOSU (Exclude Orders from RF Substitution). When 
you exclude an order from picking substitution, the following restrictions apply:
▪ only product on that order can be picked (other product cannot be substituted for the product on the 
order)
▪ product on that order cannot serve as a substitute for product on another order
EOSU shows all open orders that can be excluded from picking substitution. The Substitution flag shows the 
current status of each order. A value of Y or blank indicates that picking substitution is enabled for the order. 
A value of N indicates that the order is excluded from picking substitution.
1 Enter EOSU.

EOSU screen
2 Key in your search criteria for the orders that you wish to exclude and click on Execute Query to 
execute the query.

OUTBOUND PROCESSING
Picking Substitution

EOSU screen showing all open orders for carrier ABC
3 Proceed to select the orders that you wish to exclude from RF substitution as follows:
4 When you finish selecting your orders, click on Enable RF Substitution . The Substitution Flag 
beside the selected order(s) will change from N or blank to Y. If you make a mistake and wish to reverse 
your action, select the orders that you enabled and click on Disable RF Substitution .
5 Click on Exit to exit EOSU.
PERFORMING PICKING SUBSTITUTION IN RFPIC
If substitute product can come from a location other than the originally allocated location, you pick substitute 
product in RFPIC by entering the location of the substitute product followed by its UI value. If, however, 
If you wish to: You:
select a single order click in the checkbox beside the 
order
select all orders
click on Select All 
deselect a single order click in the checkbox beside the 
selected order
deselect all orders
click on Deselect All 

OUTBOUND PROCESSING
Picking Substitution
substitute product must come from the originally allocated location, the Location field will be filled in with the 
original location and you enter the UI value of the substitute product only.
If you enter a location other than the pick location and that location does not hold any substitute product, 
RFPIC will display a pick list showing all locations containing substitute product that is acceptable. After 
selecting the product/location that you wish to pick, you continue to process the order normally.
1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.
3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.
5 Do one of the following:
6 When the pick list of order lines is displayed, use your arrow keys to position your cursor over the order 
line that you wish to pick, then press F3 (Select).

RFPIC screen showing prompt for pick location
7 If prompted to enter your from location, enter or scan in the location of the substitute product.
If you wish to pick by zone:
If you wish to pick by order 
number:
a) Key in your zone code and press 
Enter.
a) Press Enter to bypass the Zone 
field.
b) Key in your warehouse and 
press Enter.
c) Key in your order number and 
press Enter.
If the default mode for RFPIC has 
been set to Case:
If the default mode for RFPIC has 
been set to Pallet:
The message “You have selected 
CP Mode” will appear.
a) Key in N for No and press Enter.
The message “You have selected 
NM mode” will appear.
a) Press Enter to continue.

OUTBOUND PROCESSING
Picking Substitution
8 Do one of the following:
9 Continue to pick the product normally in RFPIC. 
If there is NO substitute 
product in any location:
If there is NO substitute 
product in the location that 
you entered:
If there is substitute product in 
the location that you entered 
or the pre-filled in location:
a) The message “No subst. for all 
loc” will appear. You can only 
pick the product on the original 
order line.
a) The following message will 
appear: 
b) Key in Y for Yes and press 
Enter.
c) AccellosOne 3PL will display a 
pick list of acceptable substitutes. 
d) Use your up and down arrow 
keys to scroll through the list 
of substitute product.
e) When you find the product that 
you wish to pick, press F3 to 
select it.
a) Enter or scan in its UI value.

OUTBOUND PROCESSING
Entering Process Values in RFOPS
Entering Process Values in RFOPS
You enter process values in RFOPS. There are two process values that you enter in this program: catch 
weight and serial number. You can scan a bar code that contains these two values or you can enter them 
manually.
RFOPS maintains a running total by both weight and number of pieces. The running total shows the weight 
and number of pieces that have been scanned in as well as the weight and number of pieces that have not 
been scanned in. 
If a label has been scanned in error, you can remove it by means of the Remove command. If a case has 
been scanned in error, you can remove it from the remaining number of cases to be scanned by means of the 
Reduce command.
REQUIREMENTS
FLOWS ENOR (Enter Order)
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFOPS. 
PROCESS VALUESFor the UCC-128 label, you require two process values in RFOPS: one for catch 
weights and one for serial numbers. These codes must be set up in IPRO (Item 
Process) with the Create Automatic Records flag set to Y for Yes and then 
attached to a profile in IPRP (Item Process Profile). The IPRP profile must in turn 
be attached to the item(s) requiring the process values.
Because you are capturing a weight, the item(s) should assigned the appropriate 
non-standard weight option in ITEM.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEYou need a scan parameter profile defined in SCPR (Scan Parameter Code)*. 
For the UCC-128 label, this profile must contain a minimum of two records in the 
Detail Block: one record for your scanned in weight and another record for your 
scanned in serial number. The SCPR profile must in turn be attached to the item 
requiring the process values.
If you wish to scan in your lowest inventory level as a unique identifier, you must 
define your scan parameters in SCPR and attach your scan parameter code to 
your bar code profile in BAPR (Bar Code Profile).
* not required for manual entry in RFOPS

OUTBOUND PROCESSING
Entering Process Values in RFOPS
BASE FOR CUBE/
WEIGHT
The Base for Cube/Weight flag for your case SKU in the Quantity Breakdown 
Block of ITEM must be set to Y for Yes for any product that you wish to process in 
RFOPS.
CATCH WEIGHT 
TOLRANCES
See “Setting Up Catch Weight Tolerances” on page 302 for further information.
SORT SEQUENCE 
CODE (SOSE)
You can define a sort sequence for your process values in the RFOPS Sort 
Sequence Code (SOSE) field in MRFP.
OTHER If you pick product in RFPIC, you can only enter process values in RFOPS after 
picking in RFPIC. If you pick product in any other program, you can enter process 
values either before or after picking.
RFOPS supports alternate item codes set up in ALIT (Alternate Item and Language).
FUNCTION KEYS
All Modes
F1 ME (Manual Entry) Displays a separate window in which you 
can manually enter your catch weights, 
serial numbers and other process values.
F2 RC (Reduce Quantity) Remove a scanned case from an order 
line and reduce the order line quantity by 
one.
F3 RL (Remove Label) Remove a label that has been scanned 
from an order line.
F3 CM (Change Mode) Capture the weight of each case on a full 
pallet rather than a single weight for the 
full pallet. For example, the pallet contains 
damaged product and a single weight for 
the full pallet would not be accurate.
Only available after selecting F1 (ME) for 
manual entry.
F4 EX (Exit) Exit program or scan incomplete message.
REQUIREMENTS

OUTBOUND PROCESSING
Entering Process Values in RFOPS
1 Enter RFOPS.

RFOPS screen
2 Do one of the following:
AccellosOne 3PL will retrieve all order lines that match the criteria that you entered.
F9 Move cursor to previous field.
Pick List of Order Lines
F3 SL (Select) Selects the order line that the cursor is 
positioned over.
F4 CN (Cancel) Exits the pick list without selecting an 
order line.
If you wish to process a 
specific order:
If you wish to process a specific order and a specific UI/
OPID:
If you wish to process a 
specific UI/OPID:
a) Press F9 to position your cursor in the ORD field.
b) Key in your order number and 
press Enter.
a) Press F9 to position your cursor in the ORD field.
b) Key in your order number and 
press Enter.
c) Enter or scan in your UI/OPID 
value.
a) Enter or scan in your UI/OPID 
value.
FUNCTION KEYS

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing two order lines available for processing
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 
(SL) to select it.

RFOPS screen showing prompt for catch weight
Line 1
Line 2

OUTBOUND PROCESSING
Entering Process Values in RFOPS
4 Do one of the following:

RFOPS screen showing case one out of five scanned in
5 Continue to scan all pieces on the order line. If the same item is found on two or more order lines, AccellosOne 3PL will calculate a running total of the weight for all order lines containing that item.
If you wish to scan in your 
process values:
If you wish to enter your process 
values manually:
a) Scan in your label. a) Press F1 (Me). 
b) Key in your weight and press 
Enter.
c) Key in your serial number and 
press Enter.
Weight of first piece

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing total weight by item
6 When you finish entering all your order lines, process another order line or press F4 to exit.
CAPTURING THE WEIGHT DYNAMICALLY FROM A BAR CODE
The locate weight in bar code dynamically option allows you to scan in the weight from a bar coded label 
without knowing which numbers in the bar code represent the product’s weight. Because the format of the bar 
code is unknown, you cannot use SCPR (Scan Parameter Profile) to break up the code into its component 
parts.
The following requirements must be met before you can locate the weight in a bar code dynamically:
▪ All bar codes for a given order line must have the same length.
▪ The weight portion of the bar code for a given order line must all have the same length; if a weight is less 
than the full length, it must be padded with zeros.
▪ All weights for a given order line must fall within a range of 10 times heavier or lighter than the first case. 
For example, if case 1 weighs 100 lbs., case 2 cannot weigh more than 1,000 lbs. or less than 10 lbs.
▪ The locate weight option must be activated in IPRO by setting the Locate Weight in Bar Code Dynamically flag to Y for Yes for a given process code. This process code must be attached to an item process 
profile code in IPRP (Item Process Profile), which in turn must be attached to the appropriate item(s) in 
ITEM.
Total weight for all lines on 
order containing this item

OUTBOUND PROCESSING
Entering Process Values in RFOPS

IPRO screen showing Locate Weight in Bar Code Dynamically flag set to Y for Yes
The operator scans in the full bar code and then manually enters the weight for the first three cartons. If the 
manually entered weight matches the bar code weight in all three cartons on the same order line, AccellosOne 3PL “learns” the position of the weight in the bar code.
If the manually entered weight does not match the bar code weight, the operator will be prompted to either 
start over again or rescan the current carton.
EXAMPLE
9991234999 (Label 1)
9991356999 (Label 2)
9991426999 (Label 3)
Because the position of the weight in label one (positions 4 through 7) matches the position of the weight in 
labels two and three, AccellosOne 3PL will read the weight from these positions for all pieces on the order 
line.
If the same bar code is scanned twice, the operator will have two choices: accept the duplicate or enter a new 
bar code.
1 Enter RFOPS.
2 Do one of the following:
AccellosOne 3PL will retrieve all order lines that match the criteria that you entered.
If you wish to process a 
specific order:
If you wish to process a specific order and a specific OPID:If you wish to process a 
specific OPID:
a) Key in your order number and 
press Enter.
b) Press Enter to bypass the UI 
field.
a) Key in your order number and 
press Enter.
b) Enter or scan in your OPID 
value.
a) Press Enter to bypass the 
Order Number field.
b) Enter or scan in your OPID 
value.

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing two order lines available for processing
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 
(SL) to select it.

RFOPS screen showing prompt for weight measure code
4 Key in your weight unit of measure (1 for kilograms or 2 for pounds) and press Enter. If you made a mistake and wish to select another order line, key in 3 for Cancel and press Enter. 

RFOPS screen showing prompt to scan the bar code
5 Scan in your bar code.
Line 1
Line 2

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing prompt to enter weight
6 Key in the weight and press Enter. The weight must include a decimal point. For example, to enter a 
weight of 20 pounds, you must key in either 20.0 or 20.00. You cannot key in 20.
7 Repeat steps 5 and 6 for your second piece.
8 Do one of the following:
If the position and weight of label 
1 matches label 2:
If the position and weight of label 
1 does NOT match label 2:
a) Repeat steps 5 and 6 for your 
third piece.
AccellosOne 3PL will offer you two 
options: you can either start over 
again from the first scan or repeat 
the second scan.
a) Press Enter to rescan or key in N
for No to start over. 

OUTBOUND PROCESSING
Entering Process Values in RFOPS
9 Do one of the following:

RFOPS screen showing five pieces to scan for order line 1
10 Scan in your first piece.
If the position and weight of label 
3 matches labels 1/2:
If the position and weight of label 
3 does NOT match labels 1/2:
The following message may 
appear:
“Keep 3 Scans” message
a) Press Enter to start scanning or 
key in N for No and press Enter.
AccellosOne 3PL will offer you two 
options: you can either start over 
again from the first scan or repeat 
the third scan.
a) Press Enter to rescan or key in N
for No to start over. 
Line #

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing prompt for next piece
11 Continue to scan all pieces on the order line. If the same item is found on two or more order lines, AccellosOne 3PL will calculate a running total of the weight for all order lines containing that item.

RFOPS screen showing total weight by item
12 When you finish scanning all your pieces, process another order line or press F4 to exit.
MANUALLY ENTERING THE WEIGHT
If AccellosOne 3PL is unable to locate the weight portion of the bar code, you must enter the weight of each 
piece manually.
1 The following message will display when there is no match between the manually entered weight and the 
bar code weight in two out of three labels:
Weight of first piece
Total weight for all lines on 
order containing this item

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing “Weight positions not found” message
2 Key in 1 (Enter weight only) and press Enter.

RFOPS screen showing “Scan barcode” message
3 Manually key in the weight of the first piece and press Enter.
4 Repeat the previous step for each piece on the order line.
5 When you finish entering your weights manually, press F4 to exit.
REMOVING LABELS THAT HAVE BEEN SCANNED
You can remove labels that have been scanned in RFOPS by means of the RL (Remove) command. A 
removed label cannot be re-used.
1 Enter RFOPS.
2 Enter or scan in your order number and/or UI number.
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 
(SL) to select it.

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing order line with seven unscanned cases
4 Press F3 (RL).

RFOPS screen showing label remove prompt
5 Key in Y for Yes and press Enter.

RFOPS screen showing prompt to scan in the label to be removed
6 Enter or scan in the label to be removed.
7 When the “Barcode Removed” message appears, press Enter to confirm it.
8 Continue to process the next label on the order line in the normal manner.

OUTBOUND PROCESSING
Entering Process Values in RFOPS
REMOVING CASES EITHER SCANNED OR UNSCANNED
You can remove cases either scanned or unscanned in RFOPS by means of the RC (Reduce) command. 
When you use the Reduce command, the number of cases removed is subtracted from the order line’s to ship 
quantity in ENOR as well as the remaining number of cases and weight in RFOPS.
1 Enter RFOPS.
2 Enter or scan in your order number and/or UI number.
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 
(SL) to select it.
4 Press F2 (RC).

RFOPS screen showing prompt to remove cases
5 When prompted to remove the case and reduce the line quantity, key in Y for Yes and press Enter.

RFOPS screen showing seven potential cases to be removed
6 Do one of the following:
To remove a scanned case: To remove an unscanned case:
a) Enter or scan in the case that 
you wish to remove.
a) Press Enter to position your cursor in the REDUCE QTY field.
b) Key in the quantity to remove 
and press Enter.

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing “Unscanned quantity reduced” message
7 When the “Unit removed” or “Unscanned quantity reduced” message appears, press Enter to confirm it.

RFOPS screen showing “Scan bar code message”
8 Continue to scan in or remove cases in the normal manner or press F4 (EX) to exit.
REMOVING CASES FROM A FULLY SCANNED ORDER
You can remove cases from a fully scanned order by selecting the Yes option when the “Scan Complete 
Remove Case <Y/N> to Continue” message appears.
This message will appear in RFOPS whenever you retrieve a fully scanned order that has not yet been 
confirmed. It is designed to deal with situations in which it is necessary to remove cases from a pallet during 
the loading stage because of space limitations on the truck.
Each case that you scan in RFOPS removes one case from the to ship quantity in ENOR. If you have 
duplicate label ID’s attached to the same UI value, AccellosOne 3PL will remove the case or cases from the 
lowest process line number.
1 Enter RFOPS.
2 Key in your order number and press Enter.
3 Enter or scan in your OPID value.

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing prompt to remove case and reduce line quantity
4 Key in Y for Yes and press Enter.

RFOPS screen showing pick list of order lines
5 Use your arrow keys to position the cursor over the order line containing the case(s) that you wish to 
remove and press F3 (SL) to select it.

RFOPS screen showing prompt to scan in bar code to be removed
6 Enter or scan in the case that you wish to remove.

OUTBOUND PROCESSING
Entering Process Values in RFOPS

RFOPS screen showing “Unit removed” message
7 When the “Unit removed” message appears, press Enter to confirm it.
8 Do one of the following:
9 When you finish scanning the cases to be removed, press F4 (RT) and F4 (EX) to exit.
PERFORMING AN INCOMPLETE SCAN
If you are unable to scan in all cases on the pallet for any reason, AccellosOne 3PL will present you with the 
following options:
If you wish to exit RFOPS:
If you wish to remove 
additional cases from the 
same OPID:
If you wish to remove cases 
from a different OPID:
a) Proceed to next step. a) Enter or scan in your label 
number.
a) Press F4 (Ex) to position your 
cursor in the Ord. field and 
press Enter.
b) Enter or scan in your new 
OPID value.
c) Enter or scan in your label 
number.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned and 
remove unscanned quantities from the to ship quantity. 
You cannot process the order line again in RFPIC.
4 (Exit, New Line) Only available when locate weight in bar code logic is 
deactivated
Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned, 
remove the unscanned quantities from the to ship 
quantity and will create a new line for the balance.
5 (Exit, Cancel Picking) Only available in RFPIC.

OUTBOUND PROCESSING
Entering Process Values in RFOPS
1 Scan all cases that you are shipping for the pallet. The system will prompt you when you are complete.
2 If you are unable to scan all cases for any reason, press F4 after scanning the last scannable case.

RFOPS screen showing “Scan incomplete” message
3 Do one of the following:
4 Continue to enter your process values normally in RFOPS.
TRANSFERRING INBOUND PROCESS VALUES TO OUTBOUND ORDERS
If the automatic transfer of inbound process values to outbound orders is activated on your system, the 
process values attached to the product will be automatically transferred to the order when you enter or scan in 
your order number in RFOPS.
The following restrictions apply to the transfer of process values:
6 (Replace DAMG) Only available in RFPIC.
7 (Exit Scan, Save) Cease scanning and exit. AccellosOne 3PL will save 
the process values of any cases already scanned.
If you wish to continue from 
where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the 
to ship quantity:
Key in 3 and press Enter.
When prompted to short the order line, key in Y for Yes 
and press Enter.
If you wish to exit, short the to 
ship quantity and create a new 
line for the balance:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values:
Key in 7 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

OUTBOUND PROCESSING
Entering Process Values in RFOPS
▪ You cannot transfer process values if one or more values is missing. For example, if you have five cases 
on one full pallet and one of the cases is missing a process value, you cannot transfer the process values in RFOPS. You must enter the missing catch weight(s) in ENOR and then return to RFOPS to perform the transfer.
▪ You cannot transfer process values if you have two or more inventory entities that are identical. For 
example, you have two pallets with the same level 1/2/3 values and you wish to ship out a single pallet.
▪ Unless you are clearing out all inventory, the quantity being shipped must always equal one full pallet (or 
one drum if drum is assigned to the highest SKU class). For example, if you ship in cases, the number of 
cases that you ship must equal one full pallet.
Refer to the section “Item Process Values” in the Operations 2 Guide for further information about setting up 
this feature.
1 Enter RFOPS.
2 Retrieve the order whose process values you wish to transfer.
The “Barcode values for this order have transferred” message will appear.

RFOPS screen showing “Barcode values for this order have transferred” message
3 Press Enter to acknowledge the message.
4 Press F4 to exit. Your process values are transferred.
SETTING UP CATCH WEIGHT TOLERANCES
You can define catch weight tolerances for each item in ITEM. If a catch weight for that item exceeds the 
allowed tolerance, the weight will be rejected and the receipt or order cannot be confirmed until a catch 
weight within the permissible range is entered. For example, if the net weight of a pallet is defined as 100 lbs. 
for a given item in ITEM and the weight tolerance percentage is 5% for that item, you cannot enter a catch 
weight of greater than 105 lbs. or less than 95 lbs. in any RF program.

OUTBOUND PROCESSING
Entering Process Values in RFOPS
RFIPS screen showing “Wgt tolerance failed” message
Catch weight tolerances apply to RFOPS (Outbound Process Scan) and RFIPS (Inbound Process Scan).
In addition to the normal setups for catch weights in IPRO and IPRP, you must enter a value in the Weight 
Tolerance Percent field in Quantity Breakdown Block of ITEM for the appropriate SKU.
ITEM screen showing a weight tolerance of 5% on a net weight of 50 lbs.

OUTBOUND PROCESSING
Picking Waves in RFPK
Picking Waves in RFPK
You pick your waves in RFPK (RF Wave Pick). Depending on your pick method, you may or may not be 
prompted to for a carton size when you close your pallet and prepare to print your labels. You can look up 
your carton information in LOCN (Look Up Carton).
1 Enter RFPK.
RFPK screen
2 Key in your wave number and press Enter.
REQUIREMENTS
FLOWS See “Picking Orders in RFPIC” on page 220 for further information.
CASE PICKING See “Picking Orders in RFPIC” on page 220 for further information.
PROCESS VALUES See “Picking Orders in RFPIC” on page 220 for further information.
SUSP HOLDS See “Picking Orders in RFPIC” on page 220 for further information.
MRFP The Outbound Pallet ID Entry at Beginning field in MRFP (RFPIC 2 tab) must 
be set to Yes.
WAVE MANAGER You need to run a wave in the Wave Manager.
LABELS You need a wave label set up in DOCU and this label must be attached to the 
appropriate customers and consignees in CCDU (Customer / Consignee Document Setup).
OTHER See the Wave Manager documentation.

OUTBOUND PROCESSING
Picking Waves in RFPK
RFPK screen
3 Key in your equipment code and press Enter.
RFPK screen showing prompt for pick method
4 Key in the number corresponding to your pick method and press Enter.
RFPK screen showing prompt for outbound pallet ID
5 Enter or scan in your outbound pallet ID.

OUTBOUND PROCESSING
Picking Waves in RFPK
RFPK screen showing prompt for outbound pallet ID
6 Use your up and down arrow keys to scroll through the list of order lines assigned to your outbound pallet 
ID. When you find the order line that you wish to pick, press F3 (SL) to select it.
RFPK screen showing prompt for from location
7 Enter or scan in your from location.
8 Enter or scan in your UI.
9 Key in your pick quantity and press Enter.
10 Do one of the following:
11 Press F1 (Print Label).
If your order consists of a 
single order line:
If your order has multiple 
order lines and you wish to 
pick another line:
If your order has multiple 
order lines and you wish to 
close the pallet and print the 
pallet ID label:
a) Proceed to next step. AccellosOne 3PL will display the 
list of unpicked order lines.
a) Select the line that you wish to 
pick and repeat steps 6 to 12 
for that line.
AccellosOne 3PL will display the 
list of unpicked order lines.
a) Press F4 to exit the list.
b) Proceed to next step.

OUTBOUND PROCESSING
Relocating Product in RFST
RFPK screen showing prompt for printer
12 Do one of the following:
13 Enter or scan in your staging location.
14 Process another order or press F4 to exit.
Relocating Product in RFST
In this program, you can relocate product on an outbound order. The product must be picked and assigned an 
outbound pallet ID in an RF picking program before it can be moved.
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that 
are not generated in 
AccellosOne 3PL: If Label field is populated:
a) Press Enter to generate your 
pallet ID.
b) if required, key in your printer 
code and press Enter.
c) If prompted to validate your 
pallet ID, enter or scan it in. 
a) Enter or scan in your pallet ID.
b) If required, key in your printer 
code and press Enter.
a) If the PRT (Printer) field is not 
populated, key in your printer 
code and press Enter.
REQUIREMENTS
FLOWS See “Picking Orders in RFPIC” on page 220 for further information for your 
outbound flows and other RFPIC requirements.
The order line must be picked in an RF picking program using CASE pick 
mode before it can be relocated in RFST.

OUTBOUND PROCESSING
Relocating Product in RFST
1 Enter RFST.
RFST screen
2 Enter or scan in your order number. Then enter or scan in your OPID number. If your OPID numbers are 
unique, you can bypass the order number and enter only the OPID number.
RFST screen showing prompt for quantity
3 If prompted to enter the quantity, key in the total quantity on the pallet and press Enter.
4 If prompted to enter the from location, enter or scan in the from location.
OTHER There are five possible configuration parameters for RFST that you set up in 
MRFP (Miscellaneous tab).
▪ in the Validate Quantity in Order Move field, you specify whether or not the 
operator must enter the quantity being moved
▪ in the Validate From Location in Order Move field, you specify whether or 
not the operator must enter the from location of the product being moved
▪ in the Location Type of To Location in Order Move field, you specify whether 
the to location must be a staging location, a pick location or any location
▪ in the Allow Multiple Pallet Moves in RFST field, you specify whether or not 
the operator can relocate multiple pallets in a single step 
▪ in the Suggested Location Rules in RFST field, you define the suggested or 
default to location 
REQUIREMENTS

OUTBOUND PROCESSING
Merging OPID’s in RFMG
RFST screen showing prompt for to location
5 Enter or scan in your to location.
RFST screen showing confirmation message
6 Key in Y for Yes and press Enter to move the pallet.
7 Press F4 (EX) to exit.
Merging OPID’s in RFMG
You can merge two or more outbound pallets into a single pallet in RFMG. For example, suppose you pick 10 
cases from a location and build an outbound pallet. Later, you pick 25 cases from the same location and build 
a second outbound pallet. You now have two partial pallets and wish to merge the two into a single pallet to 
save space.
If your order line does NOT have process values such as serial number or weight, you can merge the entire 
quantity of a pallet or a partial quantity. However, if your order line has process values such as serial number 
or weight, you cannot merge partial quantities. If you do so, all process values attached to the order line will 
be deleted.
The following conditions must be met before you can do a pallet merge:
▪ The product must be picked from the same location.
▪ If you attach orders to loads in SELO and warehouse attribute 333 is set to 1, the product being merged 
must be on the same load and assigned to the same stop and group.
▪ Hazardous products cannot be merged with non-hazardous products.
▪ The same item must be kept together whenever possible if the item quantities are partials. For example, 
suppose you have three OPID’s on the same order and each OPID represents a partial pallet. If OPID’s 
1 and 2 are the same item and OPID 3 is a different item, OPID’s 1 and 2 can be merged, but 1 and 3 (or 
2 and 3) cannot be merged because that would put two different items on the same pallet.

OUTBOUND PROCESSING
Merging OPID’s in RFMG
There are two merge options that are configurable in MRFP:
MERGING TWO EXISTING OPID’S
1 Enter RFMG.

RF Merge OPID screen
2 Enter or scan in your from OPID.
FIELD DESCRIPTIONS (MISCELLANEOUS 2/5 TAB)
Allow Merging Orders/
Items to One OPID Within 
Load (RFMG)
Yes
No
If you select Yes, the RF operator can assign different orders/items to the 
same OPID within a given load in RFMG. If you select No, the RF operator 
cannot assign different orders/items to the same OPID within a given load in 
RFMG.
Retain OPID To in RFMG Yes
No
If you select Yes, the OPID to value remains displayed on the screen after the 
merge so that the RF operator can continue to merge into the same OPID.

OUTBOUND PROCESSING
Merging OPID’s in RFMG

RFMG screen showing from OPID
3 If there are multiple order lines attached to the same OPID, you can press F1 (LN) to position your cursor 
in the from OPID block. Then use your arrow keys to scroll through the orders lines of your from OPID. 
When you finish scrolling, press F4 (RT) to return to the to OPID field.
4 Press Enter to accept the full OPID quantity or key in a partial quantity and press Enter.
5 Enter or scan in your to OPID.

RFMG screen showing to OPID and prompt to update
6 Press F3 (UP) to perform the merge.
7 Press F4 (EX) to exit.
CREATING A NEW OPID
You can move the full quantity or a partial quantity of an existing OPID to a new OPID that you create in 
RFMG. AccellosOne 3PL will create a new order line for the new OPID.
1 Enter RFMG.

OUTBOUND PROCESSING
Merging OPID’s in RFMG

RF Merge OPID screen
2 Enter or scan in your from OPID.

RFMG screen showing from OPID
3 If there are multiple order lines attached to the same OPID, you can press F1 (LN) to position your cursor 
in the from OPID block. Then use your arrow keys to scroll through the orders lines of your from OPID. 
When you finish scrolling, press F4 (RT) to return to the to OPID field.
4 Press Enter to accept the full OPID quantity or key in a partial quantity and press Enter.
5 Enter or scan in your new OPID.

RFMG screen showing new OPID and prompt to update
6 Press F3 (UP) to perform the merge.
7 Press F4 (EX) to exit.

OUTBOUND PROCESSING
Performing Outbound Audits in RFOA
Performing Outbound Audits in RFOA
This program allows you to perform an audit of staged product before it is loaded onto the truck. You define 
your inventory level for RFOA audits in MRFP. For example, if you select Level 1 in the RFOA Audit Level 
field, the RF operator will perform a count for each item on the order. If, on the other hand, you select Level 2, 
the RF operator will perform a count for each lot on the order.
If the count matches the order line quantity, the order line will be advanced to the next flow and a time-stamp 
will be created indicating that the audit was successful. If the count does not match the order line quantity, an 
error message will be displayed and the order line will not be advanced to the next flow.
1 Enter RFOA.
REQUIREMENTS
FLOWS ENOR (Enter Order)
SUAL (Supervisor Allocated) — optional
STPI (Start Picking)
FIPI (Finish Picking)
special flow for RFOA audit
STLO (Start Loading) — optional
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFOA.
OTHER You must define your inventory level for RFOA audits in the RFOA Audit Level 
field in MRFP. For example, if you select Level 1 in the RFOA Audit Level field, 
the RF operator will perform a count for each item on the order. If, on the other 
hand, you select Level 2, the RF operator will perform a count for each lot on the 
order.
If you select “Suspend Advancing Flow in Outbound Audit” in MRFP, the order will 
NOT be advanced to the next flow even if the operator count matches the order 
line quantity.

OUTBOUND PROCESSING
Performing Outbound Audits in RFOA
RFOA screen
2 Enter or scan in your staging location.
3 If there are multiple orders at your staging location, press F3 (SL) to select the order that you wish to 
audit.
RFOA screen showing prompt for OPID
4 Enter or scan in your OPID.
5 Enter or scan in the required number of inventory levels.

OUTBOUND PROCESSING
Performing Outbound Audits in RFOA
RFOA screen showing prompt for quantity
6 Key in your quantity and press Enter.
7 Do one of the following:
RFOA screen showing message for completed audit
8 Repeat the above steps for any additional order lines that you wish to audit or press F4 the required number of times to exit RFOA.
If your audit quantity is correct:
If your audit quantity is NOT 
correct:
a) Press Enter to acknowledge the 
message.
a) Press Enter to acknowledge the 
error message.
b) Re-enter your quantity. If your 
quantity is rejected again, press 
F4 (RT) to exit.
c) Press Enter to acknowledge the 
“Order Incomplete” message.

OUTBOUND PROCESSING
Adjusting Cubic Dimensions in RFCC
Adjusting Cubic Dimensions in RFCC
You can adjust the cubic dimensions and gross weight of an OPID in RFCC (RF Carton Cube). If you do not 
adjust cubic dimensions of an OPID in this program, the dimensions will be automatically calculated based on 
the item setup and the product assigned to the OPID.
1 Enter RFCC.
RFCC screen
2 Enter or scan in your OPID.
RFCC screen showing linear measurement code set to M for Meters
3 Key in your length and press Enter.
4 Key in your width and press Enter.
5 Key in your height and press Enter.
6 Key in your gross weight and press Enter.

OUTBOUND PROCESSING
Assigning Orders to Loads in SELO
7 Press F4 to exit.
8 If you re-enter your OPID in RFCC, you can look up the cubic dimensions that you previously scanned.
RFCC screen showing cubic dimensions for OPID 000046
Assigning Orders to Loads in SELO
Refer to the Operations 2 Guide for instructions on using SELO and OLOP.
Replacing Damaged Product in RFRD
This program allows you to take picked product off an order, put it on SUSP hold and allocate replacement 
product. It is only available for product that has been picked and staged. Depending on the option that you 
choose in the Allow Suspended Holds field in MRFP, a supervisor login may be required. 
If there are process values attached to the picked and staged product, you will be prompted to scan those 
values.
1 Enter RFRD.

OUTBOUND PROCESSING
Replacing Damaged Product in RFRD
RFRD screen
2 Enter or scan in your UI value.
3 If there are multiple order lines with the same UI, use F3 (SL) to select the line that you wish to work on.
RFRD screen showing prompt for damaged quantity
4 Key in your damaged quantity and press Enter.
5 Press F3 to process.
RFRD screen showing prompt to proceed
6 Key in Y for Yes and press Enter.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
RFRD screen showing confirmation message
7 Press Enter to continue.
8 Press F4 to exit.
Working With Pallet Build Assignments in PABU
This program allows you to look up and modify your pallet build assignments before they are released to RF 
or voice for picking. PABU supports the following functions:
▪ you can look up the Task Profile parameters used to generate assignments
▪ you can update your Task Profile parameters and re-process the pallet build
▪ you can update existing assignments by adding or removing order lines
▪ you can create new assignments
▪ you can run the Pallet Build Summary/Detail Reports
▪ you can assign a staging location to order lines
NOTE Pallet build assignments are only available in PABU for pre-built pallets. Pallets built dynamically by the Task Engine cannot be viewed or edited in PABU.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
SETTING UP YOUR PALLET BUILD PARAMETERS IN COMP
The automatic suspension of picking tasks can be activated in COMP. If you do not wish to automatically 
suspend your picking tasks, you can manually suspend them in RFOT.
You release your pallet build assignment 
tasks to RF or voice.
REGI/
CCCC
PABU
AccellosOne 3PL generates your pallet build 
assignments based on your setup in REGI and 
CCCC.
You review your pallet build assignments and 
make any necessary adjustments.
Allocation
PABU
You allocate your orders in Wave Manager. 1
2
3
4
RFPIC/
Voice
5 RF operator performs the picking tasks. 

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PERFORMING QUERIES
You can query by suspended tasks, released tasks or all tasks.
At the load level, PABU shows the total number of pallets, the total number of pallet build assignments, the 
total quantity, the number of picked pallets, the number of pick assignments, the number of picked picks, the 
picked quantity, the gross weight, the net weight and the cube for each load.
At the order level, PABU shows the stop number, the wave number, the customer, the total number of pallets, 
the total number of pallet build assignments, the total quantity, the number of picked pallets, the number of 
pick assignments, the number of picked picks, the picked quantity, the gross weight, the net weight and the 
cube for each order.
At the assignment level, PABU shows the assignment number, quantity, total number of picks, net weight, 
height and cube or each pallet build assignment.
1 Enter PABU.
FIELD DESCRIPTIONS
Suspend Picking Tasks 
Upon Wave Execution
Yes
No
If you set this flag to Yes, picking tasks will be automatically suspended when 
you generate a wave in Wave Manager. This will allow you to manually adjust 
your pallet build assignments in PABU (Pallet Build) before they are released 
to RF or voice for picking.
If you set this flag to No, picking tasks will be automatically released to RF or 
voice for picking once the wave is generated.
This flag overrides the Suspend Task flag in Wave Manager, which allows you 
to suspend tasks for a specific Wave Manager template.
Use Assignment Parameter Tables for Pallet BuildYes
No
If you set this flag to Yes, you can rebuild pallets any number of times using 
the same REGI/CCCC configuration that was in effect when you first built the 
pallet for a given order line. If set this flag to No and you rebuild a pallet, 
AccellosOne 3PL will use your default pallet build settings in REGI and CCCC.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing query fields
2 Enter your wave, load, order and customer order parameters.
3 In the Task Options dropdown list, select Suspended, Released or All.
4 Click on Execute Query.
PABU screen showing query results for All option
5 In the Load Summary Block, select the load whose orders you wish to look up.
6 Click on Order / Assignment.
7 In the Order Details Block, select the order whose pallet build assignments you wish to look up.
8 If the order has header or line remarks, you can click on Order Header/Line Remarks to view 
them.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing order header and order line remarks
When you finish looking up your order remarks, click on Exit to return to the Order Details screen.
9 Click on Order / Assignment to see your pallet build assignments.
PABU screen showing pallet build assignments
If the Assignment column is blank, that means that the order line was not included in any pallet build 
assignment.
10 Click on Lines to see the order lines for those assignments.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing order lines
11 When you finish looking up your pallet build assignments, click on Exit the required number of times 
to exit. 
RELEASING AND STAGING A SUSPENDED LOAD
Staging a suspended order or load in PABU will override the existing staging location if one has already been 
assigned.
1 Select the suspended order or load that you wish to release.
2 Click on Release Order Tasks.
PABU screen showing prompt for staging location
3 Select your staging location and warehouse from the pick list and press Enter twice to accept them.
MERGING ASSIGNMENTS
1 Go the Assignments tab.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing assignments
2 Select the first of the two assignments to be merged.
3 Click on Assignment Merge dropdown list.
PABU screen showing Assignment Merge dropdown list
4 Select the second of the two assignments to be merged and click on Merge Assignment.
5 When prompted to confirm the merge, click on Yes. The screen will be refreshed and only one pallet 
assignment will be displayed.
DELETING ASSIGNMENTS
When you delete a pallet build assignment, the order line remains but the assignment number is deleted. The 
Task Engine will create a new pallet build assignment dynamically.
1 Go the Assignments tab.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing assignments
2 Select the line or lines that you wish to delete and click on Delete Assignment Lines.
3 When prompted to confirm the deletion, click on Yes.
PABU screen showing deleted assignment
ADDING ASSIGNMENTS
If a pallet build assignment has been deleted, the line cannot be picked until you create a new assignment for 
the line.
1 Go to the Assignments tab.
PABU screen showing pick without assignment

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
2 Click on Add Assignment.
PABU screen showing Add Assignment
3 Select the line or lines that you wish to add and click on Add Assignment.
PABU screen showing new assignment
DELETING LINES FROM AN ASSIGNMENT
If an assignment contains two or more lines, you can delete individual lines from the assignment.
1 Go to the Assignments tab.
PABU screen showing assignments
2 Click on Lines.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PABU screen showing order lines
3 Select the line that you wish to delete and click on Delete Assignment Lines.
4 When prompted to confirm the deletion, click on Yes.
OVERRIDING ASSIGNMENTS
You can move a line from one assignment to another by means of the Override command.
1 Go to the Assignments tab.
PABU screen showing assignments
2 Click on Lines.
PABU screen showing lines

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
3 Select the line that you wish to move and click on the Assignment Override dropdown list to select the to 
assignment. Then click on Assignment Override.
4 When prompted to confirm the assignment override, click on Yes.
CHANGING YOUR ORDER PARAMETERS
If you change your order parameters, you can rebuild your pallet assignments using the new parameter(s).
1 Select the order that you wish to reprocess.
2 Click on Order Parameters.
Order Parameters screen
3 Proceed to make any necessary changes to your order parameters. Only fields and flags in boldface type 
can be modified.
4 Click on Save to save your changes and rebuild your pallet assignments.
5 When prompted to save your changes, click on Yes.
RESTORING YOUR ORIGINAL ORDER PARAMETERS
If you changed your order parameters and are not satisfied with the results, you can restore your order 
parameters to the original settings. You define what is meant by “original” settings in the Use Assignment 
Parameter Tables for Pallet Build field in COMP.
1 Select the order whose original parameters you wish to restore.

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
2 Click on Order Parameters.
3 Click on Copy Originals.
4 When prompted to confirm the restoration of your original parameters, click on Yes.
PRINTING THE PALLET BUILD SUMMARY REPORT
This report shows the assignment number, stop number, quantity, number of picks, number of items, height, 
cube, gross weight and net weight for each assignment reported on.
1 Select the load or order that you wish to report on.
2 Click on Run APBR Summary Report.
APBR report
3 Select your printer and click OK.
APBR Summary report
ABC FOODS

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
PRINTING THE PALLET BUILD DETAIL REPORT
This report shows the sequence number, order line number, item code, pick location, isolator code (ISOL), 
quantity, cube and net weight for each pick in a pallet build assignment.
1 Select the load or order that you wish to report on.
2 Click on Run APBR Detail Report.
3 Select your printer and click OK.
APBR Detail report
SUSPENDING A TASK IN RFOT
If automatic task suspension is deactivated in COMP, you can manually suspend a pallet build assignment 
task until you are ready to pick it.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
ABC Foods

OUTBOUND PROCESSING
Working With Pallet Build Assignments in PABU
RFOT screen showing unsuspended tasks
4 Click in the Suspend Tasks column of each task that you wish to suspend.
5 Click on Save to suspend the tasks.
RELEASING A SUSPENDED TASK IN RFOT
When you are ready to pick the task, you must release the suspension.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
RFOT screen showing suspended tasks
4 Click in the Suspend Tasks column of each task that you wish to release to deselect the checkbox.
5 Click on Save to release the task.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL........................................................................ 335
Relocating Inventory (Operator Selects To Location) ................................ 336
Relocating Inventory (Directed Move System Activated)........................... 339
Performing Multi-Pallet Moves....................................................................... 344
Adjusting Non-Serial Number Inventory in RFAJ ........................................ 346
Adjusting Out Existing Inventory ................................................................ 346
Adjusting In New Inventory ........................................................................ 348
Adjusting In Existing Inventory................................................................... 352
Adjusting In Inventory With a Variable Quantity Breakdown...................... 354
Adjusting Serial Number Inventory in RFAJB.............................................. 355
Adjusting in Inventory................................................................................. 356
Adjusting Out Cases .................................................................................. 358
Adjusting Out Full Pallets........................................................................... 359
Adjusting Out Cases Using the Remove Command .................................. 360
Recovering From a Lost Connection ......................................................... 362
Merging Inventory in RFMI ............................................................................. 363
Merging Existing Inventory Entities............................................................ 364
Creating New Inventory Entities................................................................. 367
Adding Extra Charges to a Receipt/Order in RFEC ..................................... 370
Scenario 1 — RF Operator Enters Charge Quantity Only ......................... 370
Scenario 2 — RF Operator Enters Charge Code and Quantity ................. 372
Deleting an Extra Charge........................................................................... 374
Assigning Check Digits to Locations in RFCD............................................. 374
Entering Incidents in RFINC........................................................................... 377
Performing CRM Tasks in RFCE.................................................................... 379
Checking Your Bar Codes in RFBR............................................................... 381
Entering Hold Adjustments in RFHO ............................................................ 382
Placing Product on Hold ............................................................................ 382
Removing Inventory from Hold .................................................................. 384
Processing Supervisor Overrides in RFSUN................................................ 385

MISCELLANEOUS PROCESSING
Entering Inventory Attributes in RFATT........................................................ 387

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
Relocating Inventory in RFRL
You relocate inventory from one location to another in RFRL. The locations that you specify in a relocate can 
be within the same warehouse or belong to different warehouses. You cannot relocate inventory if it is on 
order or on receipt.
The following restrictions apply to RFRL:
▪ You cannot relocate product that is on an open order or receipt.
▪ If the Location Capacity Validation Type field in COMP (Company Code) is set to “No validation for userinitiated transactions”, relocating inventory does not take into account the location’s capacity. You can 
move inventory into a location that is considered “full”.
▪ If the product is on non-breakable hold, you must relocate all product in the location; you cannot relocate 
partial quantities.
If you wish to relocate product to a pick line location, you must set the Validation Rules for Relocate to Pick 
Line flag in MRFP to either 2 (Allow operator to proceed) or 3 (Omit validation of location).
REQUIREMENTS
ALLOCATION If you want AccellosOne 3PL to select the best possible to location for a relocation based on your directed move stock parameters in ILOP, you must set the 
Allow Directed Move in RF Relocate flag in MRFP to Yes.
See the Allocation and Wave Manager Guide for further information on setting up 
directed moves.
OTHER If you want the operator to be forced to validate the from location in a relocation, 
you must set the Picklist Rules in RF Relocate flag in MRFP to the appropriate 
value.
If you want relocation quantity to be displayed, you must set the Display From 
Relocation Quantity in RF Relocate flag in MRFP to Yes.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the 
criteria that you specify in Criteria Mode.
F3 CQ (Count Query) Counts the number of records that meet 
the criteria that you specify in Criteria 
Mode.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
RELOCATING INVENTORY (OPERATOR SELECTS TO LOCATION)
1 Enter RFRL.

RF — Relocate
F4 RM (Return to Main) Switch to Main Mode.
Results Mode
F1 EC (Enter Criteria) Switch to Criteria Mode.
F3 LB (Location Block) Positions your cursor in the From Location 
field after pressing F4 (IN) to position your 
cursor in the Customer field.
F3 PR (Process Relocate) Performs the relocation.
F4 IN (Inventory) Positions your cursor in the Customer field 
so that you can scroll through the list of 
records retrieved in your query.
F4 EX (Exit) Exit program.
F9 Move cursor to previous field.
FUNCTION KEYS

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
2 Do one of the following:
3 The system will display the number of inventory records that meet the level 1, 2, 3 and 4 criteria that you 
specified.

RFRL screen showing one record for item A2, lot 101
If you wish to query by UI value:
If you wish to query by inventory 
level:
a) Key in your UI value and press 
Enter.
a) Enter or scan in your customer 
code.
b) Enter or scan in your item code.
c) If required, enter or scan in your 
level 2, 3 and 4 values.
d) Press F2 to query.
Number of records 
for this inventory 
entity

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL

RFRL screen showing prompt for quantity
If you know your from location:
If you do NOT know your from 
location:
a) Key in your from location and 
press Enter.
a) Press F10 to enter the pick list, 
then F2 to perform your query.
▪ AccellosOne 3PL will display all locations 
containing the product that you specified. 
RFRL screen showing available locations
b) Use your arrow keys to position 
your cursor beside the location 
containing the product that you 
wish to move.
c) Press F3 to select the location. 
The system will return you to the 
main RFRL screen.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
4 Do one of the following:
5 Enter or scan in your to location.
6 If required, enter or scan in your to warehouse.
7 Press F3 to process the relocate.
8 Perform another relocate or press F4 the required number of times to exit. 
RELOCATING INVENTORY (DIRECTED MOVE SYSTEM ACTIVATED)
There are three options for overriding the system-assigned location for a relocation depending on your setup 
in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to No, an operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to Yes, changing a location must be approved by a supervisor
▪ if the Max. Number of F3 (NX) Allowed Per ILOP Sequence in RFRLflag in MRFP is activated, an operator can select an alternative suggested relocate location
1 Enter RFRL.

RF — Relocate
If the QTY field is populated: If the QTY field is blank:
a) If you wish to relocate all product 
in the location, proceed to the 
next step. If you wish to relocate 
a portion of the product in the 
location, press F9 to position 
your cursor in the QTY field. 
Then key in your relocation 
quantity and press Enter.
a) Key in the quantity that you wish 
to relocate and press Enter.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
2 Do one of the following:
3 The system will display the number of inventory records that meet the level 1, 2, 3 and 4 criteria that you 
specified.

RFRL screen showing six records for item A2, lot 101
If you wish to query by UI value:
If you wish to query by inventory 
level:
a) Key in your UI value and press 
Enter.
a) Enter or scan in your customer 
code.
b) Enter or scan in your item code.
c) If required, enter or scan in your 
level 2, 3 and 4 values.
d) Press F2 to query.
Number of records 
for this inventory 
entity

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL

RFRL screen showing prompt for quantity
If you know your from location:
If you do NOT know your from 
location:
a) Key in your from location and 
press Enter.
a) Press F10 to enter the pick list, 
then F2 to perform your query.
▪ AccellosOne 3PL will display all locations 
containing the product that you specified. 
RFRL screen showing available locations
b) Use your arrow keys to position 
your cursor beside the location 
containing the product that you 
wish to move.
c) Press F3 to select the location. 
The system will return you to the 
main RFRL screen.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
4 Do one of the following:

RFRL screen showing location assigned by system
If the QTY field is populated: If the QTY field is blank:
a) If you wish to relocate all product 
in the location, proceed to the 
next step. If you wish to relocate 
a portion of the product in the 
location, press F9 to position 
your cursor in the QTY field. 
Then key in your relocation 
quantity and press Enter.
a) Key in the quantity that you wish 
to relocate and press Enter.

MISCELLANEOUS PROCESSING
Relocating Inventory in RFRL
5 Do one of the following:
6 Press F3 to process the relocate.
7 Perform another relocate or press F4 the required number of times to exit. 
If you accept the systemassigned location:If you wish to change the 
system-assigned location:
If you wish to select an 
alternative system-assigned 
location:
a) Scan in your location to confirm it.a) Key in a new location for the 
relocated product and press 
Enter. The following message 
will appear: 
b) Key in Y for Yes and press 
Enter to proceed with the 
location override. If you do 
not wish to proceed with the 
override, key in N for No and 
press Enter to return to the 
main RFRL screen.
c) If you enter Y for Yes to proceed with the relocation and 
if a supervisor’s authorization is required to override 
the location, the following 
screen will appear:

d) Have a supervisor log in to 
approve the location override.
a) Press F3 (NX) to display a 
second suggested put-away 
location. If the second suggested put-away location is 
not acceptable, press F3 
(NX) again to see a third suggested put-away location.
b) Press Enter again to accept 
the warehouse that the system-assigned location 
belongs to.

MISCELLANEOUS PROCESSING
Performing Multi-Pallet Moves
Performing Multi-Pallet Moves
Multi-pallet moves allow you to stage, put-away, pick, relocate and replenish multiple pallets in a single step; 
that is, you scan two or more UI’s but only enter/scan the to location once. Multi-pallet moves are supported in 
the following programs: RFCH, RFPU, RFPIC, RFRL, RFRP and RFST.
The following restrictions apply to multi-pallet moves:
▪ all product has the same level 1
▪ multi-pallet moves must be activated in MRFP
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
1 Enter the appropriate program (RFCH, RFPU, RFPIC, etc.).
2 Select the line that you wish to pick, put-away, move, etc.
3 If the item is not defined as stackable in ITEM, the following message will appear:
RFPIC screen showing non-stackable message
4 Press Enter to acknowledge the message and proceed.
5 Enter/scan in your UI value.
6 If prompted to do so, enter the quantity.

MISCELLANEOUS PROCESSING
Performing Multi-Pallet Moves
RFPIC screen showing prompt to pick next pallet
7 When the pick next pallet prompt appears, do one of the following:
8 Repeat steps 2 to 5 for each additional pallet that you wish to move.
9 When the maximum capacity for the equipment type is reached, the following message will appear:
RFPIC screen showing prompt to go to staging (current count = maximum for equipment type)
10 Press Enter to continue.
11 Continue normal processing for RFCH, RFPU, RFPIC, etc.
To cancel multi-pallet move 
mode:
To continue in multi-pallet move 
mode:
a) Key in N (Go to Staging) and 
press Enter.
b) Stage, put-away or move the current pallet before working on the 
next pallet.
a) Key in Y (Pick Pallet) and press 
Enter.
b) Proceed to next step.
the maximum capacity for the 
equipment type = 2 pallets
the current pallet being 
worked on

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
Adjusting Non-Serial Number Inventory in RFAJ
You can adjust in and adjust out non-serial number inventory in RFAJ without the need to enter ENAJ (Enter 
Adjustment). In RFAJ you can perform most of the functions supported in ENAJ including: 
▪ querying by any inventory level
▪ entering positive and negative adjustments for existing inventory
▪ creating new inventory 
When adjusting existing inventory, you can enter either partial or full amounts of an inventory entity. When 
creating new inventory, you can specify a hold code, enter a variable quantity breakdown (if this feature is 
activated in ITEM) and enter an expiry date (if expiry date entry is activated in ITSH).
RFAJ does not support adjustment transfers, changes to an item’s quantity breakdown or changes to a level 
2/3/4 description. These functions must be performed in ENAJ.
ADJUSTING OUT EXISTING INVENTORY
1 Enter RFAJ.
FUNCTION KEYS
Main Mode
F2 QU (Query) Allows you to query inventory.
F4 EX (Exit) Exit program.
Results Mode
F1 HD (Hold) Places product on hold.
F2 CM (Change Mode) Allows you to switch modes; from adjust in 
to adjust out and vice versa.
F3 PR (Process) Processes the adjustment.
F4 RT (Return to Main) Switch to Main Mode.
F9 Move cursor to previous field.

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
RFAJ screen
2 Enter your UI or inventory levels and press Enter. If the same inventory is found in multiple locations, you 
must enter or scan in your location.
If you do not know the UI or inventory levels of the inventory that you wish to adjust out, press Enter twice 
to position your cursor in the L1 field. Then enter the inventory level(s) that you know and press F2 (QU). 
When AccellosOne 3PL retrieves the list of query results, use your up and down arrow keys to scroll 
through the list.
RFAJ screen showing adjust out mode
3 If the inventory has been assigned multiple locations, use your up and down arrow keys to find the location that you want to adjust out. The press Enter to accept it.
4 Enter or scan in your location.
5 Key in your adjust out quantity as a negative (for example, -1 or 
-1PLT) and press Enter. If the item has multiple SKU’s in its quantity breakdown and you do not specify 
a SKU, AccellosOne 3PL will use the item’s lowest SKU.

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
RFAJ screen showing adjust out quantity
6 Press F3 (PR) to process the adjustment.
7 Press F4 (EX) to exit.
ADJUSTING IN NEW INVENTORY
New inventory is inventory that has never been received in the warehouse before. That is, at least one of the 
item’s inventory levels is new.
1 Enter RFAJ.
RFAJ screen
2 Press Enter to bypass the UI field.
3 Enter or scan in your location.
4 Enter or scan in your item. If the same item is attached to two or more customers, press F3 (SL) to select 
the appropriate customer/item from the pick list.

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
RFAJ screen showing prompt for level 2 value
5 Enter the remaining inventory levels of the inventory that you wish to adjust in.
RFAJ screen showing prompt to process
6 If you wish to place the adjust in inventory on hold, press F1 (HD). Then key in your hold code and press 
Enter.
7 Press F3 (PR) to process.
RFAJ screen showing prompt for location

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
8 Enter or scan in your location.
RFAJ screen showing prompt for adjustment quantity
9 Key in your adjust in quantity (for example, 1 or 1PLT) and press Enter. If the item has multiple SKU’s in 
its quantity breakdown and you do not specify a SKU, AccellosOne 3PL will use the item’s lowest SKU.
If the location that you enter 
does NOT match the location in 
step 3:
If the location that you enter 
does match the location in step 
3:
a) The following message will 
appear:
Prompt to accept change in 
location
b) If the location is correct, key in Y
for Yes and press Enter to accept 
it. Otherwise, press Enter to 
reject it.
a) Proceed to next step.

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
RFAJ screen showing adjustment in quantity
10 Press F3 (PR) to process the adjustment.
11 Do one of the following:
12 Press F4 (RT) and F4 (EX).
If manual entry of expiry dates is 
activated for the item:
If manual entry of expiry dates is 
NOT activated for the item:
a) The following window will 
appear:
b) Key in your expiry date in the format displayed on your screen 
and press Enter.
c) If the expiry date is correct, key 
in Y for Yes and press Enter. 
Otherwise, press Enter to return 
to the date screen and re-enter it.
a) Proceed to next step.

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
ADJUSTING IN EXISTING INVENTORY
If the inventory that you wish to adjust in is already in the warehouse, you must change your mode from 
“adjust out” to “adjust in”.
1 Enter RFAJ.
RFAJ screen
2 Press Enter to bypass the UI field.
3 Enter or scan in your item. If the same item is attached to two or more customers, press F3 (SL) to select 
the appropriate customer/item from the pick list.
RFAJ screen showing prompt for level 2 value
4 Enter the remaining inventory levels of the inventory that you wish to adjust in.
RFAJ screen showing adjust out mode

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
5 Press F2 (CM).
RFAJ screen showing prompt to adjust in inventory
6 Key in Y for Yes and press Enter.
7 If you wish to place the adjust in inventory on hold, press F1 (HD). Then key in your hold code and press 
Enter.
8 Press F3 (PR) to process.
RFAJ screen showing prompt for location
9 Enter or scan in your location.
RFAJ screen showing prompt for adjustment quantity
10 If the location that you entered in the previous step does not match the location in step 3, the following 
message will display:

MISCELLANEOUS PROCESSING
Adjusting Non-Serial Number Inventory in RFAJ
RFAJ screen showing prompt to accept change in location
If the location is correct, key in Y for Yes and press Enter to accept it. Otherwise, press Enter to reject it.
11 Key in your adjust in quantity (for example, 1 or 1PLT) and press Enter. If the item has multiple SKU’s in 
its quantity breakdown and you do not specify a SKU, AccellosOne 3PL will use the item’s lowest SKU.
RFAJ screen showing adjustment in quantity
12 Press F3 (PR) to process the adjustment.
13 Press F4 (RT) and F4 (EX).
ADJUSTING IN INVENTORY WITH A VARIABLE QUANTITY BREAKDOWN
If you are adjusting in inventory with a variable quantity breakdown, you will be prompted to enter the quantity 
breakdown. You can either press Enter to accept the system default or key in a new quantity breakdown and 
press Enter.
RFAJ screen showing prompt for adjusting quantity breakdown

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB
Adjusting Serial Number Inventory in RFAJB
You can adjust in and adjust out serial number inventory in RFAJB. RFAJB performs the adjustment to 
inventory and the bar code validation at same time. It can only be used with unique serial numbers.
You can adjust in inventory when the serial number has never been received or is on a confirmed order. If 
required, adjusted in inventory can be placed on hold. You can adjust out inventory when the serial number 
has been received and is not picked. If a case is on a full pallet and all cases are available, you can adjust out 
a full pallet by scanning in a single case.
RFAJB can also recover from a lost connection. When a connection is dropped, you can either finish the 
current transaction or continue to adjust in or adjust out more cases.
REQUIREMENTS
INVENTORY LEVELSRFAJB requires a three-level account.
PROCESS VALUESYou require two process values: one for catch weights and one for serial numbers. These codes must be set up in IPRO (Item Process) as follows:
Transfer Value to Inventory = Yes
Create Automatic Records = Yes
Allow Duplicates = Yes for your catch weight value and No for your serial number value
Then attach your process values to a profile in IPRP (Item Process Profile). The 
IPRP profile must in turn be attached to the item(s) requiring the process values.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEYou need a scan parameter profile defined in SCPR (Scan Parameter Code). 
This profile must contain a minimum of three records in the Detail Block: one 
record for your scanned in weight, a second record for your scanned in serial 
number and a third record for your scanned in inventory level 1 value. The SCPR 
profile must in turn be attached to the item requiring the process values.
BAR CODE PROFILEYou must define a bar code profile in BAPR and attach to it the scan parameter 
code that you set up in SCPR.
OTHER You need a default adjustment code in ATMP (Action Template Setup) for each 
company/customer combination. If a single default adjustment code for all customers in all companies, you can use the .ALL codes for both customer and company.

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB
ADJUSTING IN INVENTORY
You can adjust in inventory when the serial number has never been received or the product is on a confirmed 
order.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in your bar code of the first case to adjust in.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile 
and press F3 (SL) to select it.
FUNCTION KEYS
All Modes
F1 PLT (Pallet) Allows you to adjust out a full pallet.
F2 RM (Remove) Allows you to remove a previously 
scanned case.
F2 HD (Hold) Places product on hold.
F3 PR (Process) Displays the quantity validation screen.
F4 EX (Exit) Exit program.
F4 RT (Return to Main) Switch to Main Mode.
F9 Move cursor to previous field.

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB

RFAJB screen showing adjust in message
5 Repeat the above step for each additional case that you wish to adjust in.
6 If you make a mistake and wish to “unscan” a scanned case, press F2 (RM). Then rescan the case to be 
removed from the adjustment.
7 When you finish scanning the cases to be adjusted in, press F3 (PR).

RFAJB screen showing quantity validation 
8 Key in the number of cases to be adjusted in and press Enter.
9 Enter or scan in your level 2/3/4 values. If you wish to apply a hold code to the new inventory, press F2 
(HL) before entering you lowest inventory level. Then key in your hold code and press Enter. Lastly, enter 
your remaining inventory levels.
10 If the adjusted in inventory has already been received, the following message will appear.

RFAJB screen showing warning that serial number has already been received 

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB
11 Do one of the following:
12 Press F4 to exit.
ADJUSTING OUT CASES
You can adjust out cases if the serial number has been received and is not picked.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in your bar code of the first case to adjust out.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile 
and press F3 (SL) to select it.

RFAJB screen showing adjust out message
5 Repeat the above step for each additional case that you wish to adjust out.
If you accept the re-received 
inventory:
If you reject the re-received 
inventory:
a) Key in 1 and press Enter. a) Key in 2 and press Enter.
b) Re-enter the required inventory 
level.

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB
6 If you make a mistake and wish to “unscan” a scanned case, press F2 (RM). Then rescan the case to be 
removed from the adjustment.
7 When you finish scanning the cases to be adjusted out, press F3 (PR).

RFAJB screen showing quantity validation
8 Key in the number of cases to be adjusted out and press Enter.
9 Press F4 to exit.
ADJUSTING OUT FULL PALLETS
You can adjust out full pallets if the serial number has been received, all cases are available and no cases 
have been picked.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in the bar code of any case on the pallet.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile 
and press F3 (SL) to select it.

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB

RFAJB screen showing adjust out message
5 Press F1 (PLT).

RFAJB screen showing confirmation prompt
6 Key in Y for Yes and press Enter.
7 Press F3 (PR).

RFAJB screen showing quantity validation
8 Key in the total number of cases on the pallet and press Enter.
9 Press F4 to exit.
ADJUSTING OUT CASES USING THE REMOVE COMMAND
If you wish to adjust out the majority of cases on a pallet (for example, a pallet holds 50 cases and you wish to 
adjust out 45), you can use the Remove command. The Remove command allows you to scan in only the 
cases NOT to be adjusted out rather than each case to be adjusted out.
1 Enter RFAJB.

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB
2 Enter or scan in your location.
3 Enter or scan in the bar code of any case on the pallet.

RFAJB screen showing adjust out message
4 Press F1 (PLT).

RFAJB screen showing confirmation prompt
5 Key in Y for Yes and press Enter.
6 Press F2 (RM).

RFAJB screen showing remove prompt
7 Enter or scan in the case that you wish to remove.
8 Repeat the above two steps for each additional case that you wish to remove.
9 When you finish removing your cases, press F3 (PR).

MISCELLANEOUS PROCESSING
Adjusting Serial Number Inventory in RFAJB

RFAJB screen showing quantity validation
10 Key in the total number of cases being adjusted out — that is, the number of cases on the pallet that you 
did NOT scan — and press Enter.
For example, if your pallet quantity breakdown is 20 cases per pallet and you use the Remove command 
to remove five cases, your adjust out quantity will be 15 (20 -5).
11 Press F4 to exit.
RECOVERING FROM A LOST CONNECTION
If you lose your RF connection and re-enter RFAJB, you will be prompted to either finish the existing 
adjustment or continue to add more cases to your adjustment in/adjustment out.
1 Enter RFAJB.

RFAJB screen showing lost connection message
2 Do one of the following:
If you wish to finish the existing 
adjustment:
If you wish to add more cases to 
your adjustment:
a) Key in 1 and press Enter.
b) Press F3 (PR) to confirm the 
count.
c) Complete the adjustment in the 
normal manner.
a) Key in 2 and press Enter.
b) Continue to add new cases.
c) Complete the adjustment in the 
normal manner.

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
Merging Inventory in RFMI
You can merge and transfer inventory entities in RFMI. You use RFMI when you wish to consolidate two 
partial pallets into a single PID or you wish to correct an incorrect inventory level. For example, you received 
product under lot number 101, which is wrong, and you want to transfer the product to lot number 102, which 
is the correct lot number. Lot 102 can be either an existing lot number or a new lot number created by the 
operator in RFMI.
The following requirements must be met before you can merge/transfer inventory in RFMI:
▪ the product belongs to the same customer
▪ the customer is billed at the lowest inventory level in DILP
▪ the product is NOT on an open order or receipt
If you have assigned process values to your product and if you are merging or transferring a full pallet, no 
scanning of process values is required as the values are transferred automatically. If, however, you are 
working with less than a full pallet, process values must be individually scanned.
REQUIREMENTS
SCAN PARAMETER CODEIf you use process values to capture catch weights and serial numbers, you need 
a scan parameter profile defined in SCPR (Scan Parameter Code). This profile 
must contain a minimum of three records in the Detail Block: one record for your 
scanned in weight, a second record for your scanned in serial number and a third 
record for your scanned in inventory level 1 value. The SCPR profile must in turn 
be attached to the item requiring the process values.
INVENTORY LEVELSYou can merge inventory entities at inventory levels other than the lowest (PID) 
by setting the Allow Merging Up To Level (RFMG) field in MRFP to the appropriate value: Level 1, Level 2 or Level 3.
INVENTORY 
ATTRIBUTES
If your inventory entities have inventory attributes set up in IAPR (Inventory Attributes Profile Code), you cannot perform a merge unless there is an exact match 
of attributes (you can deactivate this condition by selecting the Allow RF Merge 
flag in IAPR).
VARIABLE QUANTITY BREAKDOWN 
INVENTORY
The Base for Cube/Weight flag in ITEM must be set to Y for Yes for the lowest 
SKU.
OTHER You need a default adjustment code in ATMP (Action Template Setup) for each 
company/customer combination. If a single default adjustment code applies to all 
customers in all companies, you can use the .ALL codes for both customer and 
company.

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
MERGING EXISTING INVENTORY ENTITIES
When you merge two existing inventory entities, AccellosOne 3PL will apply the following logic to renewal 
storage and expiry calculations:
▪ billing will use the oldest date as the next renewal date
▪ the oldest expiry date will be assumed for the merged inventory
1 Enter RFMI.
ATMP screen showing default adjustment code for all companies and customers
REQUIREMENTS

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
RFMI screen
2 Do one of the following:
RFMI screen showing adjust in inventory
3 Press F3 (PR) to display the adjust out screen.
If you know the UI of the adjust in 
inventory:
If you do NOT know the UI value 
of the adjust in inventory:
a) Enter or scan in the UI of your 
adjust in inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 101 will be your adjust 
in inventory.
c) If the UI that you entered exists 
in multiple locations, key in your 
location code and press Enter.
a) Press Enter to bypass the UI 
field.
b) Key in the location code and/or 
inventory levels of your adjust in 
inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 101 will be your adjust 
in inventory.
d) If AccellosOne 3PL retrieves 
multiple inventory records, use 
your arrow keys to select the 
inventory entity that you wish to 
transfer in.

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
RFMI screen showing adjust out screen
4 Do one of the following:
RFMI screen showing adjust out screen
5 If the inventory entity that you entered in the previous step is found in multiple locations, use your arrow 
keys to select the correct record.
6 Key in your adjustment quantity as a negative value and press Enter.
If you know the UI of the adjust 
out inventory:
If you do NOT know the UI value 
of the adjust out inventory:
a) Enter or scan in the UI of your 
adjust out inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 102 will be your adjust 
out inventory.
c) If the UI that you entered exists 
in multiple locations, key in your 
location code and press Enter.
a) Press Enter to bypass the UI 
field.
b) Key in the location code and/or 
inventory levels of your adjust 
out inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 102 will be your adjust 
out inventory.
d) If AccellosOne 3PL retrieves 
multiple inventory records, use 
your arrow keys to select the 
inventory entity that you wish to 
transfer out.

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
RFMI screen showing adjust out quantity of -3C
7 Press F3 (PR) to process the adjustment.
RFMI screen showing prompt for total number of cases
8 If you want to place the merged inventory on hold, press F9 to position your cursor in the H field. Then 
key in your hold code and press Enter.
9 Key in the total number of cases and press Enter. For example, if you are merging 5 cases of pallet ID 
101 with 10 cases of pallet ID, your total number of cases will be 15 (5 + 10). 
10 Press F4 (EX) to exit.
CREATING NEW INVENTORY ENTITIES
You can transfer an existing inventory entity to a new entity created in RFMI.
1 Enter RFMI.

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
RFMI screen
2 Enter or scan in the UI of your new inventory entity.
RFMI screen showing adjust in inventory
3 Press F3 (PR) to display the adjust out screen.
RFMI screen showing adjust out screen

MISCELLANEOUS PROCESSING
Merging Inventory in RFMI
4 Do one of the following:
RFMI screen showing adjust out screen
5 Key in your adjustment quantity as a negative value and press Enter.
RFMI screen showing adjust out quantity of -1 PLT 3 CASE
6 Press F3 (PR) to process the adjustment.
If you know the UI of the adjust 
out inventory:
If you do NOT know the UI value 
of the adjust out inventory:
a) Enter or scan in the UI of your 
adjust out inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 102 will be your adjust 
out inventory.
c) If the UI that you entered exists 
in multiple locations, key in your 
location code and press Enter.
a) Press Enter to bypass the UI 
field.
b) Key in the location code and/or 
inventory levels of your adjust 
out inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, 
pallet ID 102 will be your adjust 
out inventory.
d) If AccellosOne 3PL retrieves 
multiple inventory records, use 
your arrow keys to select the 
inventory entity that you wish to 
transfer out.

MISCELLANEOUS PROCESSING
Adding Extra Charges to a Receipt/Order in RFEC
RFMI screen showing prompt for total number of cases
7 If you want to place the new inventory on hold, press F9 to position your cursor in the H field. Then key in 
your hold code and press Enter.
8 Enter or scan in the location of the new inventory. 
9 Press F4 (EX) to exit.
Adding Extra Charges to a Receipt/Order in RFEC
If RF entry of extra charges is activated in ECHP, you can add extra charges to receipts or orders in the standalone program RFEC. You can also add extra charges to receipts or order in RFCH (receipts only) or RFPIC 
(orders only).
The entry of extra charges in RFEC/RFCH/RFPIC is strictly optional. You can press F4 at any time to exit the 
program without entering an extra charge.
There are two possible scenarios for extra charge entry in RFEC: you can select your extra charge(s) from a 
predefined list or you can manually enter them. 
There are two flags in ECHP that govern extra charge entry in RF: Allow RF Entry and Allow Override of 
Charge Quantity in RF. If both flags are set to N for No, extra charge entry in RF is deactivated.
SCENARIO 1 — RF OPERATOR ENTERS CHARGE QUANTITY ONLY
Allow RF Entry (ECHP) = No
Allow Override of Charge Quantity in RF (ECHP) = Yes
REQUIREMENTS — GENERAL
FLOWS The receipt or order must be at the flow set up for extra charge entry in ECHP. If 
the Flow Process Code (FLPR) for RF field in ECHP is blank, you can add extra 
charges to a receipt or order at any flow.
OTHER See “Extra Charge Setup for RF” on page 89

MISCELLANEOUS PROCESSING
Adding Extra Charges to a Receipt/Order in RFEC
In this scenario, the RF operator can select one or more extra charges from a predefined list and can enter 
any charge quantity for the selected charge(s).
1 Enter RFEC.
RFEC screen
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
RFEC screen showing two possible extra charges
4 If you change your mind and do not wish to add an extra charge to the receipt or order, press F4 (RT) and 
F4 (EX) to exit RFEC.
5 If there are multiple extra charges in RFEC, use your arrow keys to scroll up and down the list until you 
find the extra charge that you wish to add.
6 Key in your charge quantity and press Enter. A charge quantity of zero means no extra charge for the 
receipt or order.

MISCELLANEOUS PROCESSING
Adding Extra Charges to a Receipt/Order in RFEC
RFEC screen showing prompt to confirm the change to the charge quantity
7 Do one of the following:
8 Repeat the previous steps for each additional extra charge that you wish to add to the receipt or order.
9 When you finish adding your extra charges, press F4 (RT) and F4 (EX) to exit.
SCENARIO 2 — RF OPERATOR ENTERS CHARGE CODE AND QUANTITY
Allow RF Entry (ECHP) = Yes
Allow Override of Charge Quantity in RF (ECHP) = Yes
In this scenario, the RF operator must manually enter his or her extra charges (if any) and can enter any 
charge quantity for the entered charges.
1 Enter RFEC.
RFEC screen
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
If you wish to confirm the change 
to the charge quantity:
If you wish to cancel your 
change:
a) Key in Y for Yes and press Enter. a) Press Enter to accept the default 
value of No.

MISCELLANEOUS PROCESSING
Adding Extra Charges to a Receipt/Order in RFEC
RFEC screen showing prompt to enter RF extra charges
4 Do one of the following:
RFEC screen showing prompt to enter charge
5 Key in your charge code and press Enter.
If you wish to add an extra 
charge:
If you do NOT wish to add an 
extra charge:
a) Press Enter to continue.
b) Proceed to next step.
a) Key in N for No to exit.
b) END OF PROCEDURE

MISCELLANEOUS PROCESSING
Assigning Check Digits to Locations in RFCD
RFEC screen showing prompt to enter charge quantity
6 Key in your charge quantity and press Enter. If you press Enter to accept the default quantity of zero, no 
extra charge will be created for the receipt or order.
7 Repeat the previous steps for each additional extra charge that you wish to add to the receipt or order.
8 When “RF Charges Completed” message appears, press Enter to acknowledge it.
9 Press F4 (EX) to exit.
DELETING AN EXTRA CHARGE
You delete an extra charge in RFEC by setting its charge quantity to zero. The following conditions must be 
met before you can perform a deletion:
▪ the receipt or order’s flow has not been advanced
▪ the Allow Override of Charge Quantity in RF flag in ECHP has been set to Yes
1 Enter RFEC.
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
4 If there are multiple extra charges in RFEC, use your arrow keys to scroll up and down the list until you 
find the extra charge that you wish to delete.
5 In the QTY field, key in zero and press Enter.
6 When prompted to confirm the change to the charge quantity, key in Y for Yes and press Enter.
7 Press F4 (RT) and F4 (EX) to exit.
Assigning Check Digits to Locations in RFCD
You can define check digits for your locations and require RF operators to scan in this check digit from a label 
attached to the location whenever they work in RFRL, RFPU, RFPIC and RFRP. The purpose of check digit 
scanning is to ensure that the RF operator physically went to the location to scan it rather than manually 
entering any location at the dock. 

MISCELLANEOUS PROCESSING
Assigning Check Digits to Locations in RFCD
You can use the program RFCD (RF Check Digit) to assign a check digit to an individual location or to a range 
of locations. If your locations already have check digits, you can use RFCD to update them.
You use the “%” character as a wildcard when you wish to update a range of locations.
1 Enter RFCD.
RFCD screen
2 Do one of the following:
TIP You can look up and update location check digits in LOCA (Locations). However, unlike RFCD LOCA does not allow you to update a range of locations in a single 
step.
REQUIREMENTS
WAREHOUSE AND 
LOCATION FORMAT
Check digit scanning must be activated in WARE by selecting the Manual Check 
Digit 1 option in the Voice Check Digit Usage field.
If you wish to assign a check 
digit to a single location:
If you wish to assign the same 
check digit to multiple locations:
a) Key in your location code and 
press Enter.
a) Use the %” character as a wildcard. For example, enter A1% to 
for all locations starting with the 
characters A1 or A1%1B for all 
locations starting with the characters A1 and ending with the 
characters 1B.

MISCELLANEOUS PROCESSING
Assigning Check Digits to Locations in RFCD
RFCD screen showing 12 records retrieved
AccellosOne 3PL will retrieve all locations whose code matches the search criteria that you entered. If 
there is currently a check digit assigned to the location(s) retrieved, it will display in the Check Digit field.
3 Do one of the following:
4 Key in your new check digit over the existing check digit (if any) and press Enter. When you press Enter, 
all records that you retrieved in RFCD are updated with the new check digit.
5 Press F4 twice to exit RFCD.
If your query retrieved a singe 
location:
If your query retrieved multiple 
locations:
If you used the wildcard “%” in 
your query:
a) Proceed to next step. a) If required, you can use your 
up and down arrow keys to 
scroll through the list of locations to be updated.
b) Press Enter to position your 
cursor in the Check Digit field.
a) If required, you can use your 
up and down arrow keys to 
scroll through the list of locations to be updated.
b) Press Enter to display the following message:
c) Press Enter to acknowledge 
the message and position 
your cursor in the Check Digit 
field.

MISCELLANEOUS PROCESSING
Entering Incidents in RFINC
Entering Incidents in RFINC
You can track ad-hoc labor activities that occur while working in RF in RFINC (RF Incidents). For example, a 
pallet is poorly stacked and falls over, a battery change is required for a forklift or a worker goes on break. If 
required, you can invoice the activity to a customer and add a free-text comment.
The elapsed time of the incident is tracked by comparing the start time to the end time; that is, the time that 
the incident was opened versus the time that you exit RFINC.
RFINC can be run directly from the menu or can be initiated from RFPIC, RFPU. RFCH and RFRL by 
pressing the F5 function key.
1 Enter RFINC.
RFINC screen
2 Press F3 (PL) to display the job type pick list.
REQUIREMENTS
CUSTOMER RELATIONSHIP MANAGEMENT
If the incident’s job type in JBTP is attached to a CRM code, RFINC will create a 
CRME record for the incident.
See the labor tracking section of the Operations 2 Guide for further information on job types.
BILLING If an incident’s job type in JBTP is attached to a charge code and you select the 
invoice to customer option, RFINC will create an accessorial charge for the incident.
See the labor tracking section of the Operations 2 Guide for further information on job types.
MESSAGES Message codes must be set up in MESS.

MISCELLANEOUS PROCESSING
Entering Incidents in RFINC
RFINC screen showing job type pick list
3 Use your up and down arrow keys to position the cursor over the job type that you wish to select. Then 
press F3 (SL) to select it.
4 Key in the quantity of product involved in the incident and press Enter.
5 Key in the quantity's SKU code and press Enter.
RFINC screen showing quantity of one pallet
6 Do one of the following:
7 Key in your message code for the incident and press Enter or use the pick list function to select your 
message code.
8 If your job type is attached to a CRM code, you can key in free-text comment in the Comment field. This 
comment will appear in the Description field of CRME.
9 When you finish entering your incident, press F1 (PR) to process.
If you wish to charge for the 
incident:
If you do NOT wish to charge for 
the incident:
a) Press F9 to position your cursor 
in the Invoice to Cust field.
b) Key in Y for Yes and press Enter.
c) Key in your customer code and 
press Enter or use the pick list 
function to select your customer.
a) Proceed to next step.

MISCELLANEOUS PROCESSING
Performing CRM Tasks in RFCE
RFINC screen showing system-generated incident number
10 Press F4 (EX) to exit.
Performing CRM Tasks in RFCE
If a CRM (Customer Relationship Management) task has been assigned to you in CRME (CRM Entry), you 
will be prompted to perform the task whenever you log on to RF or exit an RF program. You can also access 
your CRM tasks directly in the program RFCE (RF CRM Entry).
CRM tasks remain assigned to you until you close them. When you close a CRM task, you can add a free-text 
comment to it or you can close the task without adding a comment.
CRM entry in RF does not support labor tracking.
1 Enter RFCE.
RFCE screen showing three CRM tasks assigned to RF operator

MISCELLANEOUS PROCESSING
Performing CRM Tasks in RFCE
2 Do one of the following:
RFCE screen showing details for CRM
3 Do one of the following:
4 Press F4 (EX) to exit RFCE.
If you wish to scroll through the 
list of CRM tasks: If you wish to perform a query:
a) Using your arrow keys, select the 
CRM task that you wish to work 
on and press F3 (SL).
a) Press F1 (EQ).
b) Key in your query word or phrase 
and press Enter.
c) If your query retrieves more than 
one record, use your arrow keys 
to select the task that you wish to 
work on and press F3 (SL).
If you wish to add a comment 
before closing the CRM task:
If you wish to close the CRM 
task without adding a 
comment:
If you wish to exit without 
closing the CRM task:
a) Key in your comment and 
press Enter.
b) When prompted to close the 
task, key in Y for Yes and 
press Enter. 
c) Press Enter to continue when 
the CRM Closed message 
appears.
a) Press F3 (PR) to process the 
task.
b) When prompted to close the 
task, key in Y for Yes and 
press Enter. 
c) Press Enter to continue when 
the CRM Closed message 
appears.
a) Press F4 (EX) to exit without 
closing the CRM task.

MISCELLANEOUS PROCESSING
Checking Your Bar Codes in RFBR
Checking Your Bar Codes in RFBR
This program allows you to scan in any bar code to find out the number of empty spaces between each 
segment. Empty spaces are indicated by hyphens.
1 Enter RFBR.
RFBR screen
2 Scan in your bar code.
RFBR screen showing embedded spaces indicated by hyphen
3 Press F4 (RT)
4 Press F4 (EX) to exit.

MISCELLANEOUS PROCESSING
Entering Hold Adjustments in RFHO
Entering Hold Adjustments in RFHO
This program allows you to make positive and negative hold adjustments in RF. It is similar to HOAD (Hold 
Adjustments), but only supports hold codes that have been activated for RF processing in HOLD (Hold 
Types).
There are two flags in HOLD that control the behavior of RFHO: RF Hold Excl From and RF Hold Excl To. If 
you select RF Hold Excl From, you cannot remove this hold code from product in RFHO. If you select RF 
Hold Excl To, you cannot attach this hold code to product in RFHO. If you leave both fields unchecked, there 
are no restrictions related to this hold code in RFHO.
HOLD screen showing flags RF Hold Excl From and RF Hold Excl to
PLACING PRODUCT ON HOLD
1 Enter RFHO.
2 Key in your UI value and press Enter.
RFHO screen showing prompt for Hold to
3 Key in your hold code and press Enter.

MISCELLANEOUS PROCESSING
Entering Hold Adjustments in RFHO
RFHO screen showing prompt for hold quantity
4 Key in your hold quantity and press Enter.
RFHO screen showing “F3 to process” message
5 Press F3 to process.
6 When prompted to proceed, key in Y for Yes and press Enter.
RFHO screen showing “<Enter> to continue” message
7 Press Enter to continue.

MISCELLANEOUS PROCESSING
Entering Hold Adjustments in RFHO
8 Press F4 to exit.
REMOVING INVENTORY FROM HOLD
1 Enter RFHO.
2 Key in your UI value and press Enter.
RFHO screen showing 10 cases on DMG Hold
3 Press Enter to bypass the HT (Hold To) field.
RFHO screen showing prompt for hold quantity
4 Key in your hold quantity as a positive number and press Enter.

MISCELLANEOUS PROCESSING
Processing Supervisor Overrides in RFSUN
RFHO screen showing “F3 to process” message
5 Press F3 to process.
6 When prompted to proceed, key in Y for Yes and press Enter.
RFHO screen showing “<Enter> to continue” message
7 Press Enter to continue.
8 Press F4 to exit.
Processing Supervisor Overrides in RFSUN
This program allows supervisors to look up and accept overrides from the following programs: RFCH, RFPU, 
RFPIC, OLOP and RFRL. When an override is accepted in RFSUN, it is deleted and can no longer be 
accessed.
1 Enter RFSUN.

MISCELLANEOUS PROCESSING
Processing Supervisor Overrides in RFSUN
RFSUN screen
2 Press Enter to advance to the DOC field.
3 Key in your query criteria. You can query by document type, document number, document line, building, 
door, selection code, terminal code and operator code. There are five document types in RFSUN: I for 
Inbound, O for Outbound, M for Relocation, R for Replenishment and L for Load.
4 When you finish entering your query criteria, press F2 (PL) to execute your query.
RFSUN screen showing override in OLOP
5 Use your arrow keys to scroll through the list of override records. When you reach the record that you 
wish to process, press F3 to select it.
RFSUN screen showing prompt "F3 TO PROCESS"
6 Press F3 to process.

MISCELLANEOUS PROCESSING
Entering Inventory Attributes in RFATT
RFSUN screen showing prompt to confirm
7 To confirm acceptance of the override, key in Y for Yes and press Enter. To cancel your acceptance, key 
in N for No and press Enter.
8 Press F4 (EX) to exit.
Entering Inventory Attributes in RFATT
This program allows you to attach inventory attributes to existing inventory in your warehouse.
1 Enter RFATT.
RFATT screen
REQUIREMENTS
INVENTORY 
ATTRIBUTES
Inventory attributes must be set up in IAPR (Inventory Attributes) and your IAPR 
profile must be attached to the appropriate items.

MISCELLANEOUS PROCESSING
Entering Inventory Attributes in RFATT
2 Scan or manually enter your UI.
3 If there are multiple inventory entities with the same UI, press F3 to select the inventory entity that you 
wish to work with.
RFATT screen showing prompt for country of origin (1 inventory attribute required)
4 Scan or manually enter the required inventory attribute(s).
RFATT screen showing “Attributes not required or entered” message
5 Press Enter to acknowledge the “Attributes not required or entered” message.
6 Press F4 to exit.

VOICE-ACTIVATED PICKING AND ORDER 
ASSIGNMENT SYSTEM
Overview .......................................................................................................... 390
Setting Up Voice-Activated Picking .............................................................. 390
Setting Up Your Voice Profile in VOPR ..................................................... 390
Setting Up Your Voice Profile (Customer) in VOPC .................................. 393
Setting Up Your Task Profile in REGI ........................................................ 396
Setting Up Your RF Operators in RFOP .................................................... 397
Setting Up Your Check Digit Parameters in WARE (Optional) .................. 397
Setting Up Your Check Digit Parameters in WARE (Optional) .................. 397
Assigning Check Digits to Locations in LOCA ........................................... 398
Setting Up Your Reason Codes in REAS .................................................. 400
Activating Your Voice Terminals in MHEC................................................. 401
Picking Orders in RFPV.................................................................................. 403
Assigning RF Operators to Orders in RFOT................................................. 406
Assigning RF Operators to Orders and Order Lines.................................. 406
Assigning RF Operators to Loads.............................................................. 409
Assigning RF Operators to Pick Methods .................................................. 412
Removing an Operator Assignment........................................................... 412
Suspending a Task .................................................................................... 413
Releasing a Suspended Task .................................................................... 413
Changing the System-Assigned Staging Location..................................... 414
Clearing Work Assignments in CTPA ........................................................... 415

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Overview
Overview
Voice-activated picking using Vocollect Voice allows you to perform easy, hands-free picking. You can set up 
voice profiles defining various Vocollect Voice options and attach these profiles to task profiles that define 
which customers, carriers, consignees, items, orders, locations and warehouses can be picked. If required, 
voice-directed picking can be combined with scanning when certain inventory levels are too long to be 
spoken.
You can also define voice operator overrides that temporarily override an operator’s standard task profiles in 
order to perform work that is particularly urgent.
The order assignment system allows you to assign specific orders and/or order lines to specific operators and 
define a picking sequence for each order. When the designated operator enters RFPIC, only orders assigned 
to that operator will display in the pick list. If required, an operator can cancel order assignments in RFPIC; 
when this happens, the order line appears in the pick list of all RF operators.
The order assignment system shares two voice-activated picking programs — RFOP and RFOT — but does 
not use voice profiles defined in VOPR and VOPC.
Setting Up Voice-Activated Picking
There are up to eight setup programs for voice-activated picking:
▪ VOPR (Voice Profile)
▪ VOPC (Voice Profile - Customer)
▪ REGI (Task Profile)
▪ RFOP (RF Operator)
▪ WARE (Warehouses and Location Format)
▪ LOCA (Locations)
▪ REAS (Reason Code)
▪ MHEC (Material Handling Equipment Code)
There are two voice profiles in voice-activated picking: VOPR and VOPC. VOPR defines properties that are 
specific to particular task profiles and operators, while VOPC defines properties that are specific to particular 
customers.
SETTING UP YOUR VOICE PROFILE IN VOPR
In this program, you define your voice profiles. A voice profile is a user-defined code that identifies a number 
of Vocollect Voice options or properties. When you attach this code to a task profile in REGI and then attach 
the task profile to an operator in RFOP, the properties that you define in VOPR will be assigned to the 
operator.
You can create a single voice profile for all operators or you can create multiple voice profiles and assign 
them to the appropriate task profiles and operators.
In VOPR, you define the following properties:
▪ whether or not the operator requests work or the system assigns it automatically
▪ which inventory level(s) the operator will hear for each pick

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
▪ whether or not the operator will be prompted with the delivery location
▪ the number of digits in a work ID
FIELD DESCRIPTIONS
Voice Profile Code Mandatory
Your voice profile code.
Description Mandatory
The description for your voice profile code.
Auto-Assign Options Operator requests work
System assigns operator assignment
If you select Operator requests work, the operator will be prompted to read out 
the order number that he or she wishes to pick. If you select System assigns 
operator assignment, assignments are automatically assigned to operators 
and no order number is required.
Inventory Level Prompt No Inventory Levels
Level 1 Only
Level 2 Only
Level 3 Only
Level 4 Only
Level 1, 2, etc.
In this field, you specify which inventory levels (if any) the operator will hear 
from Vocollect Voice for each pick.
Delivery Location Prompt with delivery location
Prompt with and confirm delivery location
In this property, you specify whether or not you want AccellosOne 3PL to 
prompt the operator for the delivery or staging location and whether or not you 
want the operator to confirm the delivery or staging location.
If the order has been assigned an appointment, AccellosOne 3PL will use the 
appointment’s door/location as the delivery location. If the order has NOT 
been assigned an appointment, AccellosOne 3PL will use the staging location 
in the operator’s task profile.
The operator can override the delivery location by saying “override”. The system will ask him or her for a new location. From that time on, the new location 
will be used for the next delivery until the operator overrides it again.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
1 Enter VOPR.

VOPR screen
2 Click on Create.
3 Key in your voice profile code and press Enter.
4 Key in a description for your new code and press Enter.
Work ID Length The number of digits in a work ID. If an operator provides a work ID with fewer 
than this number of digits, it will be rejected by AccellosOne 3PL.
If you enter the value -1, the operator must provide the entire work ID number.
Assignment Message If populated, this field will be read out to the voice operator for each assignment that he or she is going to work on. This is the default message. It will not 
be read out if there are higher level assignment messages that replace the 
VOPR default message. There are four possible higher level assignment messages:
1) pallet code description will be read out if a pallet code is attached to the 
CONS record for the order
2) message code description will be read out or added to the above if a message code is attached to the CONS record for the order
3) message code description will be read out or added to the above if a message code is attached to the order header
4) appointment time and door number will be read out or added to the above 
if an appointment is attached to the load of the order
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
5 Click on Save.
6 Proceed to select the appropriate option for each property by either selecting the option from a dropdown 
list or by keying in a value.
7 When you finish selecting your properties, click on Save.
8 Click on Exit to exit VOPR.
SETTING UP YOUR VOICE PROFILE (CUSTOMER) IN VOPC
In this program, you define your customer-based voice profiles. A customer-based voice profile is a userdefined code that identifies a number of Vocollect Voice options or properties. When you attach this code to a 
customer in CUST, the properties that you define in VOPC will be assigned to that customer.
In VOPC, you define the following properties:
▪ whether or not you want AccellosOne 3PL to state a given inventory level before each pick
▪ whether or not you want the operator to read back the inventory level as confirmation
▪ whether or not cycle counting is activated and the rules to follow when the inventory count by the operator does not match the on hand quantity
FIELD DESCRIPTIONS
Voice Profile Code Mandatory
Your customer-based voice profile code.
Description Mandatory
The description for your customer-based voice profile code.
Data 1 Use Do not process data 1
Process data 1
In this property, you specify whether or not you want AccellosOne 3PL to process the data 1 value of product being picked. Data 1 can refer to any inventory level. If you select the “Do not process data 1” option, AccellosOne 3PL 
will specify a quantity and location for each pick, but no inventory levels.
Data 1 Heading None
Level 1
Level 2
Level 3
Level 4
The inventory level that data 1 refers to.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
Data 1 Confirmation Only available if Data 1 Use is set to “Process data 1”
Do not capture data 1 information
If you select this option, the data 1 value is spoken but the operator does not 
read it back.
Capture data 1 information
If you select this option, the data 1 value is spoken and the operator must read 
it back. The value read back must match the product being picked or must be 
a valid substitution product.
Do not speak the data 1 field but allow operator to enter confirmation 
value
If you select this option, the data 1 value is not spoken but the operator must 
confirm it. The value confirmed must match the product being picked or must 
be a valid substitution product.
Data 1 Minimum Capture 
Length
In this property, you specify the number of characters in the inventory level 
that the operator must read out. For example, if you set this property to two, 
the operator must read out the last two characters in the inventory level. 
This value is a minimum only; if the inventory level has five characters and this 
value is set to two, the operator can read out the last two characters, the three 
last characters, the four last characters or all five characters. However, he or 
she cannot read out the last character only as this value is less than the minimum.
If you leave this field blank, the operator must read out all characters in the 
inventory level.
Data 2 Use See Data 1 Use
Data 2 Heading See Data 1 Heading
Data 2 Confirmation See Data 1 Confirmation
Data 2 Minimum Capture 
Length
See Data 1 Minimum Capture Length
Data 3 Use See Data 1 Use
Data 3 Heading See Data 1 Heading
Data 3 Confirmation See Data 1 Confirmation
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
1 Enter VOPC.
Data 3 Minimum Capture 
Length
See Data 1 Minimum Capture Length
Data 4 Use See Data 1 Use
Data 4 Heading See Data 1 Heading
Data 4 Confirmation See Data 1 Confirmation
Data 4 Minimum Capture 
Length
See Data 1 Minimum Capture Length
Cycle Count Active Flag Do not cycle count this location
Cycle count this location - Blind
Cycle count this location - Known
In this field, you activate cycle count count backs for your voice customer. See 
“Performing Inventory Count Backs” on page 246 for further information.
Cycle Count Rules Ignore investigation
Supervisor must override
Flow advancement not allowed
Supervisor override/No flow advance
See the Inventory Count Rules field in MRFP (RFPIC 2).
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking

VOPC screen
2 Click on Create Record.
3 Key in your voice profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 Click on Save.
6 Proceed to select the appropriate option for each property by either selecting the option from a dropdown 
list or by keying in a value.
7 When you finish selecting your properties, click on Save.
8 Click on Exit to exit VOPR.
9 When you finish setting up your voice profile, open CUST and proceed to attach your voice profile to the 
appropriate customer by entering the voice profile code in the Voice Profile Code field.
SETTING UP YOUR TASK PROFILE IN REGI
In this program, you attach your voice profile code set up in VOPC to your task profile. You also define the 
length of your UI check digit, the length of the spoken portion of the OPIC and whether the spoken value must 
be numeric. See “Task Profile (REGI)” on page 115 for further information on this program.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
The following fields in REGI apply exclusively to voice-activated picking:
SETTING UP YOUR RF OPERATORS IN RFOP
See “RF Operator (RFOP)” on page 87.
SETTING UP YOUR CHECK DIGIT PARAMETERS IN WARE (OPTIONAL)
You can define up to three manual check digits for each location in AccellosOne 3PL. Check digits are 
alternate location codes that Vocollect Voice uses whenever the actual location code is too long to be read 
out by the operator for each pick.
You define the number of check digits as well as the days of the week that each check digit will be used in 
WARE (Warehouse and Location Format). Then you enter your manual check digits for each location in the 
Voice Check Digit 1/2/3 fields in LOCA (Locations).
1 Enter WARE.
2 Retrieve the warehouse that you wish to set up for manual check digits.
FIELD DESCRIPTIONS
Voice Profile Code 
(VOPR)
Mandatory
The task profile’s voice profile.
Default Customer Voice 
Profile Code (VOPC)
The default customer voice profile for the task profile. This profile is used if the 
customer has not been assigned a voice profile in CUST.
Length of UI Check Digit Optional
The length of the UI check digit. For example, if you enter 3 in this field, the 
operator must read out the last three digits belonging to the UI of the product 
to picked in the location that the product is to be picked from.
For example, suppose the order line is picking item ABC001, pallet ID PA987 
from location LA001. The voice terminal will read out the location code to the 
operator. The operator will go to the location LA001, find pallet ID PA987 and 
read out “987” to confirm that he or she has arrived at the location.
Spoken Length The length of the spoken portion of the OPID. This value is added to the OPID 
prefix to form the full OPID for the order line being picked. AccellosOne 3PL 
will validate this number to ensure that it is unique and has not been used 
before.
Spoken Value Numeric If this field is checked, the value spoken by the operator must be numeric. If 
this field is NOT checked, the value spoken by the operator can be alphanumeric.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
3 Press Enter until your cursor is positioned in the Voice Check Digit Usage field. Then select the appropriate manual check digit option.
4 Depending on the option that you selected in the previous step, key in the days of week separated by 
commas for each check digit and then press Enter. For example, to enter Monday, Wednesday and Friday, you would key in MON,WED,FRI. 

WARE screen showing two check digits for warehouse 1
5 When you finish setting up your check digit parameters, click on Return to Main and Exit.
ASSIGNING CHECK DIGITS TO LOCATIONS IN LOCA
If you specified one or more check digit days in WARE, you must add one check digit in LOCA for each check 
digit day in WARE.
1 Enter LOCA.
2 Retrieve the location that you wish to assign a check digit to.
3 Key in your check digits for the location.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
LOCA screen showing two check digits for location A100
4 Repeat the above steps for any additional locations in the warehouse that require check digits.
5 When you finish assigning check digits to your locations, click on Return to Main and Exit.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
SETTING UP YOUR REASON CODES IN REAS
In this program, you set up your reason codes for voice-activated picking. Pickers use these codes to record 
a reason when the pick quantity for a given order line does not match the order quantity.
1 Enter REAS.
FIELD DESCRIPTIONS
Reason The following reason codes are supported:
1 (Split-picking a Line)
This option is used for short picks; that is, the picker wishes to pick a partial 
quantity from the location and return for the remaining quantity at a later time. 
For example, if the pick quantity is five cases and the picker picks two cases, 
AccellosOne 3PL will split the line into two lines. Line 1 (two cases) will be 
marked as picked, while line 2 (three cases) will be marked as unpicked.
2 (Not Enough Product SUSP Hold)
3 (Location is Empty SUSP Hold)
With this option, the allocated product is put on a SUSP hold. The original 
order will be zeroed out and a new P-type line will be created and allocated. If 
allocation is successful, the new order line can be picked at a later time.
4 (Not enough Product LOST Hold)
5 (Location is Empty LOST Hold)
With this option, the allocated product is put on the hold code that you enter in 
the Hold Code field of REAS (and not on SUSP hold). The original order line 
will be zeroed out and a new P-type line will be created but NOT allocated. To 
allocate the new order line, you must either do so manually in ASOR (Assign 
Locations to Orders) or print a document.
You must set up at least one reason code in order to voice pick in Vocollect 
Voice.
Description Your description for the reason code. See Reason field.
Type Set to P for Pick.
External Reference Reserved for future use.
Attached To Set to PICK.
Hold Code Only available for reason code 4 and 5.
The hold code that product is placed on when an order line cannot be picked.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
2 Click on Create Record.
3 Key in your reason code (1, 2, 3, 4 or 5) and press Enter.
4 Key in an appropriate description for your reason code and press Enter.
5 In the Type field, key P for Pick and press Enter.
6 In the Attached To field, key in PICK and press Enter.
7 Repeat the above steps for each additional reason code that you wish to set up.
REAS screen showing standard reason code for voice-activated picking
8 When you finish setting up your reason codes, click on Return to Main to exit create record mode.
9 Click on Exit to exit.
ACTIVATING YOUR VOICE TERMINALS IN MHEC
Voice terminals need to be activated in MHEC before you can use them in AccellosOne 3PL.
FIELD DESCRIPTIONS
Equipment Code The terminal ID of your Talkman voice terminal.
Description A description for your Talkman voice terminal.
Type Set to TALK.
Hourly Cost Reserved for future use
Warehouse Code The warehouse code for your voice terminal.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Setting Up Voice-Activated Picking
1 Enter MHEC.
2 Click on New .
3 In the Equipment Code field, key in your Talkman terminal ID and press Enter.
4 Key in a description for your new terminal ID and press Enter.
5 In the Type field, key in TALK and press Enter.
6 Press Enter to bypass the Hourly Cost field.
7 Key in your warehouse code and press Enter or select it from the pick list.
8 Key in your staging type location code and press Enter or select it from the pick list.
9 Repeat the above steps for each additional voice terminal that you wish to activate.
MHEC screen showing three voice terminals
10 When you finish adding your voice terminal(s), click on Save to save your changes.
11 Click on Exit to exit.
Location Code The location code of your voice terminal. The warehouse and location code 
that you attach to a voice terminal in MHEC will be assigned to any product 
picked using this voice terminal. 
For example, if you assign staging location S100 to a given voice terminal and 
then pick 10 cases of product using this terminal, AccellosOne 3PL will create 
a record in the Location Block of LOEN showing 10 cases of product in location S100.
In LOCA, the following setup is required for this location:
▪ its location type in LOTP must be staging
▪ its location structure type code in LOCA must be MHE
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Picking Orders in RFPV
Picking Orders in RFPV
If you do not want to pick certain orders using your voice-activated equipment, you can pick the orders in 
RFPV (RF Picking Voice) using standard RF guns.
1 Enter RFPV.
RFPV screen showing RF operator’s region
2 Press Enter to continue.
RFPV screen showing first order line to pick
3 Do one of the following:
If you wish to pick the order line:
If you do NOT want to pick the 
order line:
a) Press F3 (SL) to select it. a) Press F1 (SK) to skip it.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Picking Orders in RFPV
4 If an item message displays, press F4 (EX) to continue.
RFPV screen showing prompt for pick location
5 Key in or scan in your pick location.
RFPV screen showing prompt for UI
6 Key in or scan in your UI (Unique Identifier).

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Picking Orders in RFPV
RFPV screen showing prompt for pick quantity
7 Key in your pick quantity and press Enter.
RFPV screen showing prompt for to location
8 If prompted to do so, key in or scan in the check digit for the location.
RFPV screen showing “Assignment Completed” message

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
9 Press Enter to acknowledge the “Assignment Completed” message.
RFPV screen showing “Assignment Completed” message
10 Press Enter to continue with the next pick or key in 2 and press Enter to exit RFPV.
Assigning RF Operators to Orders in RFOT
If you use Vocollect Voice to pick your orders, you can temporarily override the orders in an operator’s 
standard task profile(s) in order to give priority to orders that are particularly urgent. You define overrides by 
selecting individual orders and order lines in RFOT and assigning them to the appropriate voice operator.
If you do not use Vocollect Voice and pick your orders in RFPIC, assigning operators to orders in RFOT will 
reserve those orders/order lines for the designated operator in RFPIC. When the designated operator enters 
RFPIC, only assigned orders for that operator will display in the pick list.
RFOT also allows you to define the picking sequence of orders assigned to a particular RF operator. If you do 
not define a picking sequence, orders will be sequenced by order priority followed by order number.
ASSIGNING RF OPERATORS TO ORDERS AND ORDER LINES
You can assign either order lines or entire orders to a given operator.
1 Enter RFOT.
2 If required, click on the Pick/Interleave (2) tab.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
RFOT screen showing Pick/Interleave (2) tab
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all order lines 
that meet your filter criteria.
RFOT supports the following search criteria:
ABC = code ABC
!ABC does not = code ABC
>ABC is greater than code ABC
>=ABC is greater than or equal to code ABC
<ABC is less than code ABC
<=ABC is less than or equal to code ABC
ABC,DEF,GHI = codes ABC, DEF, GHI
!ABC,!DEF,!GHI does not equal codes ABC, DEF, GHI
ABC~DEF a range of codes falling between ABC and DEF

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT

RFOT screen showing orders that meet the filter criteria
4 If required, you can resort the order records in either ascending or descending sequence by clicking on 
the appropriate header buttons (Order #, Customer, Consignee, To Ship Date, Flow or Cust. Order #).
5 If there is a line remark attached to the order line, click on Remarks to view it.
6 If you wish to assign order lines to an operator, click on the Lines tab.
TODAY Only orders with a to ship date of today
TODAY +1, etc. On orders with a to ship date of tomorrow (+1) or the day 
before yesterday (-2)

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
7 Proceed to assign the orders/order lines that you want the operator to work on by one of the following 
methods:
8 If required, you can assign a sequence number to an order/order line and the order/order line must be 
picked in that sequence. If you do not specify a sequence number, orders will be sequenced by order priority followed by order number.
9 When you finish assigning your orders/order lines, click on Save.

RFOT screen showing three orders assigned to the operator D4SUPPORT
10 Click on Exit to exit RFOT.
ASSIGNING RF OPERATORS TO LOADS
You can restrict RF operators to loads, buildings and doors. When you assign an operator to an entire load, 
the assignment is applied to all orders on the load. The restrictions that you enforce in RFOT apply to OLOP 
(Outbound Loading Process).
1 Enter RFOT.
2 Click on Outbound Loads.
If you wish to assign individual 
operators to individual orders/
order lines:
If you wish to assign all 
unassigned orders/order lines to 
a given operator:
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on the checkbox to the left 
of the operator code to complete 
the assignment.
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on Assign All.
c) If you make a mistake and wish 
to undo all assignments made in 
the current session, click on 
Unassign All.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT

RFOT screen
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all loads that 
meet your filter criteria.
RFOT supports the following search criteria:
ABC = code ABC
!ABC does not = code ABC
>ABC is greater than code ABC
>=ABC is greater than or equal to code ABC
<ABC is less than code ABC
<=ABC is less than or equal to code ABC
ABC,DEF,GHI = codes ABC, DEF, GHI
!ABC,!DEF,!GHI does not equal codes ABC, DEF, GHI
ABC~DEF a range of codes falling between ABC and DEF
TODAY Only orders with a to ship date of today
TODAY +1, etc. On orders with a to ship date of tomorrow (+1) or the day 
before yesterday (-2)

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT

RFOT screen showing loads that meet the filter criteria
4 If required, you can resort the load records in either ascending or descending sequence by clicking on 
the appropriate header buttons (Load #, Ext. Load #, Building, Door or Operator).
5 Proceed to assign the loads that you want the operator to work on by one of the following methods:
6 If required, you can assign a sequence number to a load and the load will be picked in that sequence. If 
you do not specify a sequence number, loads will be sequenced by order priority followed by order number.
7 When you finish assigning your loads, click on Save.

RFOT screen showing three loads assigned to the operator DALLEN
If you wish to assign individual 
operators to individual loads:
If you wish to assign all 
unassigned loads to a given 
operator:
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on the checkbox to the left 
of the operator code to complete 
the assignment.
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on Assign All.
c) If you make a mistake and wish 
to undo all assignments made in 
the current session, click on 
Unassign All.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
8 Click on Exit to exit RFOT.
ASSIGNING RF OPERATORS TO PICK METHODS
1 Enter RFOT.
2 Click on Pick/Interleave (2).
3 Select your pick method from the Pick Method pick list.
4 Click on Execute Query.
5 When RFOT retrieves all orders whose pick method matches the pick method that you specified in step 
3, select your operator from the Assign Operator dropdown list.
6 Click on the checkbox to the left of the operator code to complete the assignment.
7 Click on Save to save your changes.
REMOVING AN OPERATOR ASSIGNMENT
You can remove an operator assignment in RFOT if the operator has not already started it. Once an 
assignment is started in either RFPIC or Vocollect Voice, removing an operator assignment in RFOT will have 
no affect on the order currently being worked on.
1 Enter RFOT.
2 On the Filter window, key in the RF operator code of the operator whose assignments you wish to 
remove and click on click on Execute Query. You can query by multiple operators by separating 
each operator by a comma; for example, “BOB1,BOB2”.
RFOT screen showing three order lines assigned to the operator D4SUPPORT

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
3 Do one of the following:
4 When you finish removing your operator assignments, click on Save.
5 Click on Exit to exit RFOT.
SUSPENDING A TASK
You can temporarily suspend an order or task until you are ready to pick it.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
RFOT screen
3 Click in the Suspend Tasks column of each order that you wish to suspend.
4 Click on Save to suspend the order.
RELEASING A SUSPENDED TASK
When you are ready to pick the order, you must release the suspension.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
If you wish to remove an RF 
operator from an order:
If you wish to remove an RF 
operator from an order line:
a) Click on the Order tab to access 
your orders.
b) Click on the Operator dropdown 
list and select the operator “--
NONE--”.
a) Click on the Operator dropdown 
list and select the blank “operator” at the end of the list.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Assigning RF Operators to Orders in RFOT
RFOT screen
3 Click in the Suspend Tasks column of each order that you wish to release to deselect the checkbox.
4 Click on Save to release the order.
CHANGING THE SYSTEM-ASSIGNED STAGING LOCATION
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
RFOT screen
3 Select your new staging location from the dropdown list for each affected order.
4 Click on Save to save your changes.
CHANGING THE PRIORITY LEVEL OF A TASK
The Tasks tab allows you to assign a priority override value to an order line task. The default value is 100. If 
you enter a lower value (say, 50), the order line task will have a lower priority.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Clearing Work Assignments in CTPA
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
RFOT screen
4 Enter your priority override value (must be less than 100).
5 Click on Save to save your changes.
Clearing Work Assignments in CTPA
You can look up the current work assignments of your Vocollect Voice operators in CTPA (Clear Terminal Pick 
Assignments). In the Detail Block of this program, you can clear all work assignments for a given voice 
operator and make these work assignments available to another voice operator.
1 Enter CTPA.
CTPA screen showing 3 work lines assigned to the operator E80568
NOTE The Execute Query command in this program is limited to a screen refresh 
only. It does not allow you to perform actual queries.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Clearing Work Assignments in CTPA
2 Select the operator whose work assignments you wish to look up or clear and click on Detail Block.
CTPA screen showing current work assignments for operator E80568
3 Do one of the following:
4 Click on Exit.
If you wish to look up the 
operator's work assignments 
only:
If you wish to clear the operator’s 
work assignments:
a) When you finish looking up the 
work assignments, click on Master Block.
a) Click on Clear All Assignments. 
All current work assignments for 
the operator that you selected 
will be released and made available to other Vocollect Voice 
operators.

CARTONIZATION
Overview .......................................................................................................... 418
Cartonization Tab (MRFP) .............................................................................. 418
Carton Size Setup (CTSZ)............................................................................... 420
Outbound Process Configuration (CCCC).................................................... 422
Packing Station Code (PKST) ........................................................................ 425
Item Cartonization Profile Code (ICNP)......................................................... 427
Consignees (CONS) ........................................................................................ 429
Performing Manual Cartonization in RFSC................................................... 429
Performing System-Driven Cartonization in RFPK...................................... 434
Performing Second Level Cartonization....................................................... 441
Performing Manual Packing in EPSD............................................................ 442
Looking Up Cartons in LOCN ........................................................................ 449
Deleting Closed Cartons in DCAR................................................................. 451

CARTONIZATION
Overview
Overview
There are four cartonization options in AccellosOne 3PL:
▪ manual cartonization in RFSC
▪ system-directed or first level cartonization in RFPK (also known as “Pick & Pack”)
▪ second level cartonization for product that cannot be cartonized in RFPK
▪ manual packing in EPSD
Cartonization Tab (MRFP)
On this tab, you configure your cartonization options.
Cartonization tab

CARTONIZATION
Cartonization Tab (MRFP)
FIELD DESCRIPTIONS (CARTONIZATION)
Requirement for Item 
Scanning
Scan Item Code and Enter Quantity
Scan Item Code for Each Case
Reserved for future use.
Default Container Size 
Code
Prompt Entering Carton Size Code
Prompt Entering Pallet Size Code (reserved for future use)
Your default carton size code in RFSC.
Default Sorting Location Your default sorting location in RFSC.
Picking Path Mode for 
System-Driven Cartonization
Keep items together as much as possible
Pick in Location Sequence
Pick in Location Sequence, do not split order lines
Pick in Wine Sequence (custom use only)
Cartons for one item all one pallet
Your picking path mode for the BATP and LABL pick methods in RFPK. See 
“Task Profile (REGI)” on page 115 for a complete descriptions of picking path 
modes.
Cartonization Sort 
Sequence Code (SOSE)
The sort sequence or “snaking” of your pick locations for cartonization.
Validate Inventory Level 
in RFPK Cartonization
Validate Item Only
Validate Item and Level 2
The inventory level(s) that must be validated in RFPK.
Picking Style in RFPK 
Cartonization
Pick by Carton ID
Pick by Carton Position
If you select “Pick by Carton ID”, the RF operator will scan in the carton ID as 
a confirmation step in RFPK. If you select “Pick by Carton Position”, the RF 
operator will scan in the carton position on a cart or trolley as a confirmation 
step in RFPK.

CARTONIZATION
Carton Size Setup (CTSZ)
Carton Size Setup (CTSZ)
In this program, you set up your carton size codes. Carton size codes are attached to customer/carrier/
consignee combinations in CCCC. For each carton size code, you define the following:
▪ a carton size code and description
▪ whether or not the carton’s dimensions/weight are inherited from the item’s dimensions and weight
▪ if required, the linear measure code and the length/width and height
▪ if required, the weight measure code, the maximum weight and the weight of an empty carton
▪ the usable percentage of the cube
RFSC Carton Sorted by Sorted by Item
Sorted by Item/Level 2
Sorted by Item/Level 3
If you select “Sorted by Item”, the RF operator must scan in the item code in 
RFSC. If you select “Sorted by Item/Level 2”, the RF operator must scan in the 
item code plus level 2 value in RFSC. If you select “Sorted by Item/Level 3”, 
the RF operator must scan in the item code plus level 3 value in RFSC.
FIELD DESCRIPTIONS
Carton Size Code Mandatory
Your carton size code.
Description Mandatory
A description for your carton size code.
Utilize Standard ConfigurationIf you select this option, the carton dimensions/weight are inherited from the 
item’s dimensions/weight in ITEM. If you do not select this option, you must 
enter the carton’s dimensions/weight manually.
Linear Measure Code Only available if Utilize Standard Configuration is not selected
Your linear measure code for the carton size code.
FIELD DESCRIPTIONS (CARTONIZATION)

CARTONIZATION
Carton Size Setup (CTSZ)
Length / Width / Height Only available if Utilize Standard Configuration is not selected
The length, width and height of your carton size code.
Total Cube Only available if Utilize Standard Configuration is not selected
The carton’s actual cube calculated by multiplying the carton’s length, width 
and height.
Carton Size Cube Only available if Utilize Standard Configuration is not selected
In this field, you can define an override cube for a carton. For example, suppose carton A has dimensions of 24 x 16 x 5 for a total of 1920 cubic inches. If 
you define an override cube of 2500, you can place any number of items 
whose total cube does not exceed 2500 cubic inches in this carton size.
Weight Measure Code Only available if Utilize Standard Configuration is not selected
Your weight measure code for the carton size code.
Maximum Weight Only available if Utilize Standard Configuration is not selected
The maximum weight allowed in the carton.
Weight of Empty Carton Only available if Utilize Standard Configuration is not selected
The tare weight or weight of an empty carton.
SKU Class (SKCL) Only available if Utilize Standard Configuration is selected
The SKU class that the standard configuration applies to.
Usable Percentage The usable percentage of the cube. The non-usable percentage is reserved 
for packing materials.
Variable Dimensions If you select this option, the user will be prompted to enter the carton dimension in EPSD.
FIELD DESCRIPTIONS

CARTONIZATION
Outbound Process Configuration (CCCC)
CTSZ screen
Outbound Process Configuration (CCCC)
In this program, you set up your cartonization rules for different customer/carrier/consignee combinations. 
UCC-128 Package Type Carton
Pallet
The UCC-128 package type.
FIELD DESCRIPTIONS

CARTONIZATION
Outbound Process Configuration (CCCC)
FIELD DESCRIPTIONS
Customer Code The customer that the outbound process configuration applies to or.ALL for all 
customers.
Carrier Code The carrier that the outbound process configuration applies to or.ALL for all 
carriers.
Consignee Code The consignee that the outbound process configuration applies to or.ALL for 
all consignees.
Follow System Cartonization at PackingReserved for future use.
Maximum Cube/Weight In these fields, you specify the maximum cube and weight for second level 
cartonization. Second-level cartonization applies to product that cannot be 
cartonized by the cartonization engine because it is oversized, has no ICNP 
profile attached to it or has missing dimensions in ITEM.
Default Carton Size Code 
(CTSZ)
Your default carton size code in RFSC and second level cartonization.
Cartonization Sort Rules Give Priority to Carton Size Cube
Give Priority to Carton Size Dimensions
If you select Give Priority to Carton Size Cube, the cube will be considered 
first then the weight for second level cartonization. If, on the other hand, you 
select Give Priority to Carton Size Dimensions, the weight will be considered 
first then the cube.

CARTONIZATION
Outbound Process Configuration (CCCC)
CCCC screen
Cartonization Break by 
Zone Type Code
Only available for first level cartonization in RFPK
Location Grouping
Material Handling Type Groups
Pickup and Delivery Groupings
Voice
In this field, you specify which zone type (if any) AccellosOne 3PL should look 
at when comparing warehouse zones codes for the purposes of determining 
the next pick location. 
Suppose two adjacent locations — location A and location B — are both 
attached to the following three zone types: Interleaving, PnD and Grouping. If 
you select Pick and Delivery Groupings as your Cartonization Break by Zone 
Code value, the system will compare location A’s PnD warehouse zone code 
to location B’s warehouse zone code. If there is a match, the picker can pick 
from A and then B. If there is no match, the picker can pick from A but not B.
FIELD DESCRIPTIONS

CARTONIZATION
Packing Station Code (PKST)
CARTON SIZE CODE BLOCK
In this block, you define which carton size codes are valid for different customer/carrier/consignee combinations.
Carton Size Code Block
Packing Station Code (PKST)
In this program, you set up your packing stations. Packing stations are only required for manual packing in 
EPSD. For each packing station, you define:
▪ a packing station code and description
▪ a material handling equipment code
▪ the labels that will be printed at the packing station and the printers that they will be printed on
FIELD DESCRIPTIONS
Packing Station Code Mandatory
Your packing station code. 

CARTONIZATION
Packing Station Code (PKST)
In the Documents Block, you assign your labels to packing station printers.
Description Mandatory
The description for your packing station code.
MHE Code (MHEC) Mandatory
Your material handling equipment code for the packing station. The material 
handling equipment code that you enter must be attached to a material handling equipment type whose Location Required flag has been set to Y for Yes 
because packing stations require a warehouse code and location code.
The location attached to the material handling equipment code in MHEC must 
be a staging location.
Auto-Weight Reserved for future use
Device Name Reserved for future use
Executable Reserved for future use
Wave Duration Set to 999.
Wave Margin Set to 1.
Wave Release Sequence 
Number
Set to 1.
Start / End Time Use the system defaults.
Order Unit Capacity Reserved for future use
Single/Multiple Order 
Lines
Reserved for future use
Overflow Shift Flag Reserved for future use
Overflow Day Flag Reserved for future use
FIELD DESCRIPTIONS

CARTONIZATION
Item Cartonization Profile Code (ICNP)
Documents Block showing printer code for shipping label
Item Cartonization Profile Code (ICNP)
In this program, you set up your item cartonization profile codes. Each profile code defines the factor to be 
applied to a given set of items. For example, for your standard weight items, you set the factor to 1 for your 
STD code in ICNP and attach STD to all standard weight items in ITEM. As for your non-standard weight 
items, for each weight or cube category such as 1.15, 1.25, 1.35 times the standard weight or cube, you 
attach the appropriate factor to a profile code.
For example, a fragile item like a teapot requiring a lot of extra packing materials might have a cube factor 
of.85 meaning that 15% of each carton would be reserved for packing materials. On the other hand, a 
“squishy” item like a stuffed animal might have a cube factor 1.25 meaning that a carton designed to hold four 
stuffed animals could in fact hold five.
Item Cartonization Profile Codes are only required for system-driven cartonization in RFPK.
FIELD DESCRIPTIONS
Include Case Pick 
Method
When this field is not checked, cartonization will only be activated for EACH 
picks. When this field is checked, cartonization will be activated for both CASE 
and EACH picks.

CARTONIZATION
Item Cartonization Profile Code (ICNP)
ICNP screen showing factors for standard weight and cube as well as factors for deviations from the 
standard weight and cube
After setting up your item cartonization profile codes in ICNP, you attach them to the appropriate items in 
ITEM.
ITEM screen showing cartonization profile code

CARTONIZATION
Consignees (CONS)
Consignees (CONS)
You can deactivate system-directed cartonization for individual consignees by setting the Skip Cartonization 
Flag in CONS to Y for Yes.
CONS screen showing Skip Cartonization Flag set to Y for Yes
Performing Manual Cartonization in RFSC
You perform manual cartonization in the program RFSC (RF Sort Carton). With manual cartonization, you sort 
the product on an outbound order and manually assign a carton ID to the inventory in the carton. The carton 
ID’s that you manually assign are not validated by AccellosOne 3PL.
A carton is restricted to product from a single order only.
FIELD DESCRIPTIONS
RFPIC The order must be case picked and assigned an outbound pallet ID in RFPIC/
RFPK.

CARTONIZATION
Performing Manual Cartonization in RFSC
1 Enter RFSC.
RFSC screen
2 Key in your order number and press Enter.
LABELS You need a carton label set up in DOCU and this label must be attached to the 
appropriate customers and consignees in CCDU (Customer / Consignee Document Setup).
PARCEL PROCESSING Closing a carton in RFSC can trigger a special parcel processing process.
CARTON SIZES Carton sizes must be set up in CTSZ (Carton Size Setup). However, there is 
no validation of your carton sizes in CTSZ to ensure that the total weight or 
cube has been exceeded. 
FUNCTION KEYS
Results Mode
F1 RM (Remove) Removes product from a carton.
F2 QR (Query) Displays the first unpicked order line of the 
current order being processed.
F3 CL (Close) Closes a carton.
F4 EX (Exit) Exits program.
FIELD DESCRIPTIONS

CARTONIZATION
Performing Manual Cartonization in RFSC
RFSC screen showing carton size prompt
3 Press Enter to accept the default carton size or key in a new carton size and press Enter.
4 Enter or scan in your carton ID.
RFSC screen showing item prompt
5 Enter or scan in your item code or UPC code.
6 If required, enter or scan in your level 2 or 3 value.

CARTONIZATION
Performing Manual Cartonization in RFSC
RFSC screen showing quantity prompt
7 Key in the quantity of product that you wish to place in the carton and press Enter.
8 If the quantity that you entered completes the order, the “Order completed” message will appear. Press 
Enter to acknowledge it.
RFSC screen showing RM, CL and RT commands
remaining number of units 
of this item on this order to 
be sorted/packed

CARTONIZATION
Performing Manual Cartonization in RFSC
9 Do one of the following:
10 When you finish manual cartonization in RFSC, press F4 (RT) and F4 (EX) to exit.
WORKING WITH CLOSED CARTONS
When a carton is closed, you have three options: you can re-open the carton to make adjustments to it, you 
can delete the carton or you can enter a new carton.
1 When you enter or scan in the carton ID of a closed carton, the following message will appear:
If you wish to close the carton:
If you wish to remove the 
product from the carton:
If you wish to leave the carton 
open and work on another 
carton:
a) Press F3 (CL). a) Press F1 (RM).
b) Key in Y to continue with the 
removal and press Enter.
c) Enter or scan in your item to 
be removed.
d) When the removal confirmation message appears, press 
Enter to accept it.
a) Press F4 (RT).
b) Key in your order number and 
press Enter.

CARTONIZATION
Performing System-Driven Cartonization in RFPK
RFSC screen showing options for closed carton
2 Do one of the following:
Performing System-Driven Cartonization in RFPK
You perform system-driven cartonization in the program RFPK (RF Wave Pick). With system-driven cartonization, you scan in your carton ID’s first and then pick the product to be placed in these newly scanned 
cartons.
During allocation in Wave Manager, AccellosOne 3PL performs the following tasks:
▪ calculates the number and size of cartons required for each order in the wave based on the item dimensions and your carton sizes in CTSZ
▪ generates a unique UCC-128 number or carton ID for each carton
In RFPK, you scan in your carton ID and slot number for each carton and then scan in the level 1/2 values of 
the product that you are packing in the carton.
To re-open the carton: To delete the carton: To enter a new carton:
a) Key in 1 and press Enter.
b) Proceed to add new product to 
the carton or removing existing product from the carton.
a) Key in 2 and press Enter.
b) Enter or scan in a new carton 
ID or press F4 twice to exit 
RFSC.
a) Key in 3 and press Enter.
b) Enter or scan in a new carton 
ID and continue processing in 
RFSC.

CARTONIZATION
Performing System-Driven Cartonization in RFPK
Pick & Pack trolley
REQUIREMENTS
QUANTITY BREAKDOWNOnly items with a quantity breakdown of pallet/case/each can be cartonized.
LABELS You need a carton label set up in DOCU and this label must be attached to the 
appropriate customers/carriers/consignees in CCDU (Customer / Consignee 
Document Setup).
WAVE MANAGER Only orders that have been waved in the Wave Manager can be cartonized in 
RFPK.
CARTON SIZES Carton sizes must be set up in CTSZ (Carton Size Setup). 
ITEM Accurate item dimensions (that is, the weights and cube) are required. 
CARTON ID’S A UCC-128 label is generated for each carton based on the value in the EAN 
UCC Prefix field in CUST. You can customize the serial number portion of the 
UCC-128 label by setting up a number series in NUSE (Number Series).
PICK METHOD 6 (Carton Pick)
COMP System-driven cartonization must be activated at the company level by 
HighJump.

CARTONIZATION
Performing System-Driven Cartonization in RFPK
1 Enter RFPK.
2 Key in your wave number and press Enter.
3 If prompted to do so, key in your material equipment type code and press Enter.
RFPK screen showing prompt for pick method
4 Key in 6 (Carton Pick) and press Enter.
FUNCTION KEYS
Results Mode
F1 RM (Remove) Deletes a scanned in carton ID/slot.
F2 QR (Query) Displays the first unpicked order line of the 
current order being processed.
F3 SP (Start Picking) Prompts you to start picking.
F3 SK (Skip) Skips the current pick.
F3 SQ (Short Quantity) Moves cursor to the QTYP field.
F4 EX (Exit) Exits program.

CARTONIZATION
Performing System-Driven Cartonization in RFPK
RFPK screen showing prompt for carton ID
5 Key in or scan in your carton ID.
RFPK screen showing prompt for slot number
6 Key in or scan in your slot number.
RFPK screen showing prompt for carton ID

CARTONIZATION
Performing System-Driven Cartonization in RFPK
7 Do one of the following:
8 Repeat the above steps for each additional carton ID/slot that you wish to add to your trolley.
9 When you have added all your carton ID’s/slots and are ready to pick, use your arrow keys to position 
your cursor over the carton ID that you wish to pack and F3 (SP) to start picking.
RFPK screen showing prompt for level 1
10 Do one of the following:
11 Key in or scan in your level 1 value.
12 If prompted to do so, key in or scan in your level 2 value.
If your carton ID and slot number 
are correct:
If your carton ID or slot number 
is incorrect and you wish to 
rescan:
a) Proceed to next step. a) Use your arrow keys to position 
your cursor over the carton ID 
that you wish to delete.
b) Press F2 (RM).
c) Re-enter or rescan your carton 
ID and slot.
To select the current pick:
To skip the current pick and 
display your next pick:
a) Proceed to next step. a) Press F3 (SK).
b) Proceed to next step to pick this 
pick or press F3 (SK) to advance 
to the following pick.

CARTONIZATION
Performing System-Driven Cartonization in RFPK
RFPK screen showing prompt for quantity
13 Key in your quantity and press Enter.
RFPK screen showing prompt for carton ID/slot number
14 If the quantity that you enter is less than the pick quantity, the following screen will appear:
RFPK screen showing “Short Pick” message

CARTONIZATION
Performing System-Driven Cartonization in RFPK
15 Key in 1 and press Enter to accept the short pick or key in 3 and press Enter to re-enter the full quantity.
16 Do one of the following:
RFPK screen showing prompt for staging location
17 Key in or scan in your staging location.
RFPK screen showing “Move Completed” message
18 Press Enter to acknowledge the “Move Completed” message.
19 If you picked all orders on the wave, press Enter to acknowledge the “All Orders Completed” message. 
Then press F4 to exit.
If you did not pick the entire wave, the following screen will appear:
If your picking style is set to 
“Pick by Carton ID”:
If your picking style is set to 
“Pick by Carton Position”:
a) Key in or scan in your carton ID a 
second time to confirm the pick 
and pack.
a) Key in or scan in your slot number a second time to confirm the 
pick and pack.

CARTONIZATION
Performing Second Level Cartonization
RFPK screen showing “Wave Not Completed” message
20 Do one of the following:
Performing Second Level Cartonization
Second-level cartonization applies to product that cannot be cartonized by the cartonization engine because 
it is oversized, has no ICNP profile attached to it or has missing dimensions in ITEM. 
You pick the order normally in RFPK and then manually pack it using a special pick sheet. The pick sheet will 
assign system-generated carton ID’s to the product on the order based on the maximum weight and cube 
values that you define in CCCC (Outbound Process Configuration) for second-level cartonization.
If you wish to continue with 
the same wave:
If you wish to start a new 
wave: If you wish to exit the wave:
a) Key in 1 and press Enter.
b) Go to step 4.
a) Key in 2 and press Enter.
b) Key in your new wave number 
and press Enter.
a) Key in 3 and press Enter.

CARTONIZATION
Performing Manual Packing in EPSD
Performing Manual Packing in EPSD
You perform manual packing in the program EPSD (Enter Packing Details). In this program, you can create 
your own carton ID’s or you can use system-generated carton ID’s based on the order number.
1 Enter EPSD.
REQUIREMENTS
RFPIC The order must be case picked and assigned an outbound pallet ID in RFPIC/
RFPK.
LABELS You need a carton label set up in DOCU and this label must be attached to the 
appropriate customers/carriers/consignees in CCDU (Customer / Consignee 
Document Setup).
PARCEL PROCESSING Closing a carton in EPSD will trigger a special parcel processing process.
CARTON SIZES Carton sizes must be set up in CTSZ (Carton Size Setup). 
PACKING STATION Packing stations are required in PKST.
AUTO-CONFIRMATION EPSD can be configured to automatically confirm order lines upon successful 
completion of packing. Contact HighJump for assistance.
PICK METHOD Pick method in LOOR = PKST.
FULL CASE QUANTITIESInstead of scanning a case label for each full case, you can simply scan the 
item and enter the total number of cases. Weights and dimensions are automatically pulled from the item master and AccellosOne 3PL prints the required 
number of shipping labels.
Processing full case quantities requires special setup by HighJump.
OTHER Many options in EPSD are not configurable by end-users. Contact HighJump 
for further information on these options.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen
2 Key in your packing station code and press Enter or select it from the pick list.
3 Do one of the following:
If you are packing product from a 
full pallet picked in Normal 
mode:
If you are repacking product from 
a pallet with an OPID (outbound 
pallet ID):
a) Key in your order number and 
press Enter.
a) Key in your OPID and press 
Enter.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen showing prompt for carton ID
4 Key in your carton ID and press Enter or click on Carton ID based on Order for a system-generated carton ID.
5 Scan in your item code.
6 If required, scan in your level 2 value.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen showing prompt for pack quantity
7 Key in your pack quantity and press Enter.
8 Repeat the above two/three steps for each additional item that you wish to pack.
9 If you wish to look up order carton details, click on Order Carton Details . When you finish looking 
up your order carton details, click on Return to exit.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen showing Order Carton Details
If the Confirmed flag is selected, it means that the order line has been confirmed.
10 If you wish to look up your carton details, click on Carton Details . When you finish looking up your 
carton details, click on Return to exit.
EPSD screen showing Carton Details
11 When you are ready to close your carton, click on Close Carton .
12 Key in your carton size code and press Enter or select it from the pick list.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen showing prompt for length
13 If prompted to do so, enter the carton’s dimensions.
14 If required, enter or make a manual adjustment to the total carton weight.
15 Key in your label printer code and press Enter or select it from the pick list.
16 When the Enter Packing Details window appears showing that your label is printing, press Enter to 
acknowledge it.
17 Click on Exit to exit.
TRACKING YOUR PROGRESS IN EPSD
The following fields allow you to track your progress in EPSD to find out what percentage of an order has 
been packed and what percentage of an order remains to be packed.

CARTONIZATION
Performing Manual Packing in EPSD
EPSD screen showing tracking fields
DELETING A CARTON’S CONTENTS
If a carton is not closed, you can delete the carton’s contents and re-use the carton for other product.
1 Enter EPSD.
2 Key in your packing station code and press Enter.
3 Key in your order number or OPID number and press Enter.
4 Key in the carton ID of the carton that you wish to delete and press Enter.
5 Click on Delete .
6 Click on Yes when prompted to confirm your deletion.
WORKING WITH UNCLOSED CARTONS
Unclosed cartons remain in EPSD until you either close the carton or delete the carton’s contents.
FIELD DESCRIPTIONS
Units to Repack Only available if you are repacking a pallet with an OPID
The remaining number of units on the current order to be repacked.
Cartons Packed The total number of cartons on the current order that have been packed.
Units Packed The total number of units on the current order that have been packed.
Units to Pick The remaining number of units on the current order to be picked.
Cartons to Pick The remaining number of cartons on the current order to be picked.

CARTONIZATION
Looking Up Cartons in LOCN
Looking Up Cartons in LOCN
You can look up cartons in LOCN to find out which orders shipped in which cartons. The Header Block shows 
the carton ID, order number, the carrier tracking number (if any), the carton size code, UCC number and 
status.
The Detail Block shows the customer code, item code, order number, line number and current flow. If the 
checkbox after the Flow field is selected, the order line has been fully picked.
If you perform an extended query, you can search for carton information by customer code and item code.
1 Enter LOCN.
LOCN screen
2 Press Enter until your cursor is positioned in the field that you wish to query. Then key in your search criteria and click on Execute Query.

CARTONIZATION
Looking Up Cartons in LOCN
LOCN screen showing carton for order 3072
3 If you wish to query by customer code or item code, click on Extended Query.
Extended Query screen
4 Key in or select your customer/item code and click on Execute Query.
5 When you finish looking up your carton information, click on Exit to exit.

CARTONIZATION
Deleting Closed Cartons in DCAR
Deleting Closed Cartons in DCAR
If you are a desktop user, you can delete a closed carton in the program DCAR. When you delete a closed 
carton, you can choose to reduce the order line quantity accordingly (the carton did not ship) or you can leave 
the order line quantity unchanged (the original carton was damaged and had to be replaced).
1 Enter DCAR.
2 Key in your order number and press Enter.
DCAR screen showing cartons for order 2096
3 If required, click on the Reduce Order Line Quantity checkbox to deselect it.
4 In the Detail Block, click on Delete Carton for each carton that you wish to delete. Alternatively, you can 
click on Select All or Deselect All to select/deselect all cartons.
5 When you finish selecting your cartons, click on Process .
6 Click on Exit twice to exit.

CARTONIZATION
Deleting Closed Cartons in DCAR

EQUIPMENT TRACKING
Overview .......................................................................................................... 454
Company Code (COMP).................................................................................. 455
RF Checklist (MCHK) ...................................................................................... 455
Material Handling Types (MHET) ................................................................... 458
Material Handling Equipment Code (MHEC)................................................. 461
RF Operator (RFOP)........................................................................................ 463
Locations (LOCA)............................................................................................ 463
Warehouse Shift Setup (WASH) .................................................................... 464
Operator Code (OPER) ................................................................................... 465
Looking Up Equipment Tracking Data .......................................................... 466

EQUIPMENT TRACKING
Overview
Overview
The equipment tracking system allows you to track the equipment used by each RF operator, restrict certain 
activity types such as picking, packing, etc. to certain types of equipment and restrict certain RF operators to 
certain activity types and equipment types. If you assign a location to a piece of equipment, you can track a 
product’s location as it is moved around the warehouse.
Equipment can be equipment that carries or holds product such as a forklift truck or pallet jack. It can also be 
any device used in the warehouse that you wish to track such as a voice headset or an RF scanner. 
When equipment tracking is enabled, the following screen will appear each time an RF operator logs on:
Prompt for MHE code
The RF operator must enter a valid material handling equipment code in order to proceed. If the RF operator 
enters a material handling equipment type code already in use, one of the following message will appear:
The REMOVE THE LOCK message means that there are no active sessions attached to the MHE code and 
thus the MHE code is empty. It is safe to remove the lock.
Prompt to remove lock or change MHE 
code
Prompt to take over the MHE or reenter MHE

EQUIPMENT TRACKING
Company Code (COMP)
The TAKE OVER THE MHE message means that the Oracle session is still active even though the Unix 
session has been dropped (for example, the RF operator switches off the device or removes the batteries). If 
you take over another user’s session, that person will lose all his or her work and the gun will be frozen. This 
option must be used with extreme caution.
Company Code (COMP)
In this program, you activate equipment tracking by selecting Yes in the Enable Equipment Tracking in RF 
flag.
Company Parameters block in COMP showing equipment tracking activated
RF Checklist (MCHK)
In this program, you set up your checklists for RF equipment types. In the checklist, you define one or more 
questions for the RF operator as well as possible answers to these questions. One of the answers is marked 
as failed. 
In the Header Block, you create a code and description for your new checklist. In the Question Block, you 
create a list of questions in the desired sequence. If the Information Only flag is turned on, an answer is not 
required for that question. In the Answer Block, you define possible answers.
The checklist code that you create in MCHK is attached to the Checklist tab in MHET for the appropriate 
equipment type. It can also be attached to loads in SELO. When an RF operator enters any equipment code 
belonging to that equipment type in any RF program, the following prompt appears:

EQUIPMENT TRACKING
RF Checklist (MCHK)
Checklist prompt for forklift
If the RF operator enters 1 for Pass, he or she can proceed to pick the order, put-away the receipt, etc. If the 
RF operator enters 2 for Fail, he or she cannot proceed with that equipment code.
MCHK screen 

EQUIPMENT TRACKING
RF Checklist (MCHK)
1 Enter MCHK.
2 Click on New .
FIELD DESCRIPTIONS
Checklist Code Mandatory
Your checklist code.
Description Mandatory
The description of your checklist code.
Checklist Sequence 
Number
Mandatory
A unique sequence number for your question. Your checklist can contain as 
many questions as you require.
Question Mandatory
The question or instruction that will display to the RF operator in every RF program.
Information Only If you select this flag, the question or statement in the previous field does not 
require an answer.
Answer Sequence NumberMandatory if Information Only flag is not checked
A unique sequence number for your answer. You can have as many answers 
as you like for a given question.
Answer Mandatory if Information Only flag is not checked
Your answer text. For example, “Pass”, “Fail”, etc.
Fail Flag If you select this flag, the answer is a fail and the RF operator 
will not be able to proceed if he or she selects that answer. At 
least one answer for each question should be set up as a fail.

EQUIPMENT TRACKING
Material Handling Types (MHET)
3 Key in your checklist code and press Enter.
4 Key in a description for your checklist code and press Enter.
5 Click on the Checklist Sequence Number field, key in 1 as your sequence number and press Enter. 
6 Key in your first question.
7 Click in the Answer Sequence Number field, key in 1 as your sequence number and press Enter.
8 Key in your answer.
9 If required, click on the Fail Flag if the answer is a fail.
10 Click on Save .
11 Click in the Answer Sequence Number field, key in 2 as your sequence number and press Enter.
12 Key in your answer.
13 If required, click on the Fail Flag if the answer is a fail.
14 Click on Save .
15 Repeat the above three steps for each additional answer to your first question.
16 if you wish to add a second question to your checklist, click in Checklist Sequence Number field, key in 2
as your sequence number and press Enter. 
17 Repeat steps 7 to 10 for the first answer to your second checklist question.
18 Add your additional answers to the second checklist question.
19 When you finish setting up your checklist, Click on Exit to exit.
Material Handling Types (MHET)
In this program, you attach the checklist code that you created in MCHK to the Checklist tab in MHET for the 
appropriate equipment type. If you perform RF tasking in RFITLV, you must specify the equipment type’s 
vertical height factor and excluded warehouse activity types (if any).

EQUIPMENT TRACKING
Material Handling Types (MHET)
MHET screen
FIELD DESCRIPTIONS
Material Handling Type 
Code
Mandatory
Your material handling type code.
Description Mandatory
The description for your material handling type code.
Hourly Cost Reserved for future use.
Labor Standard Modifier See the “Operational Board” section in the Operations 2 Guide.
Unit Pack Reserved for future use.
Outer Pack Reserved for future use.

EQUIPMENT TRACKING
Material Handling Types (MHET)
Location Required N = No
Y = Yes
If you select N for No, a staging location is not required in MHEC for material 
handling equipment codes assigned this equipment type. If you select Y for 
Yes, a staging location is required in MHEC for material handling equipment 
codes assigned this equipment type.
Staging locations are not mandatory for material handling equipment codes. 
However, they allow you to track product more effectively on an open order. 
For example, if you assign staging location S100 to a given forklift and then 
pick 10 cases of product using this forklift, AccellosOne 3PL will create a 
record in the Location Block of LOEN showing 10 cases of product in location 
S100.
Location Vertical Height Only supported in RFITLV
The height or vertical reach of this equipment type, The vertical height factor 
code in this field must match the vertical height factor code of the location 
before an RF operator assigned this equipment type can be assigned a task 
for the location.
Exclude Whse Activity 
Type
Only supported in RFITLV
If you enter one or more activity types in this field, the RF operator will not be 
able to use this equipment type for this activity type in RFITLV.
Checklist In this field, you enter the checklist code that you created in MCHK.
Pick Method Reserved for future use.
FIELD DESCRIPTIONS

EQUIPMENT TRACKING
Material Handling Equipment Code (MHEC)
MHET screen showing electric lift equipment type that can be assigned to locations whose vertical 
height factor = 1 to 5
Material Handling Equipment Code (MHEC)
In this program, you set up your material handling equipment codes. RF operators must enter one of these 
equipment codes each time that they enter an RF program.
MHEC screen

EQUIPMENT TRACKING
Material Handling Equipment Code (MHEC)
FIELD DESCRIPTIONS
Equipment Code Mandatory
Your material handling equipment code.
Description Mandatory
Your description for this material handling equipment code.
Type (defined in MHET) Mandatory
The material handling type for this material handling equipment code.
Hourly Cost Reserved for future use
Warehouse Code Only available if Location Required flag set to Yes in MHET for the material 
handling type
The warehouse code for this material handling equipment code.
Location Code Only available if Location Required flag set to Yes in MHET for the material 
handling type
The staging location code for this material handling equipment code. In LOCA, 
the following setup is required for this location:
▪ its location type in LOTP must be staging
▪ its location structure type code in LOCA must be MHE
The location capacity in LOCA (for example, two pallets) determines the number of SKU’s that can be moved in a multi-pallet move.

EQUIPMENT TRACKING
RF Operator (RFOP)
RF Operator (RFOP)
In this program, you set up your activity type and material handling type exclusions for RF operators. If you 
specify one or more task profiles for the RF operator on the Task Profiles tab, the RF operator will be 
restricted to those task profiles. 
RFOP screen showing activity type restrictions for ALEX
Locations (LOCA)
In this program, you define your location height restrictions for each location. Only equipment types whose 
vertical height factor code matches the location’s vertical height factor code can be assigned a task in this 
location.
NOTE Activity type and material handling type exclusions are only supported in 
RFITLV.

EQUIPMENT TRACKING
Warehouse Shift Setup (WASH)
LOCA screen showing location assigned a vertical height factor code of 3
Warehouse Shift Setup (WASH)
In this program, you set up your warehouse shifts. Warehouse shifts are optional in equipment tracking. If you 
set up warehouse shifts, the RF checklist will need to be performed by the RF operator only once per shift. If 
you do not set up warehouse shifts, the RF checklist will need to be performed each time that an RF operator 
logs on (that is, more than once per shift if the RF operator logs off during a shift).
WASH screen showing three shifts

EQUIPMENT TRACKING
Operator Code (OPER)
Operator Code (OPER)
If you use warehouse shifts, you must assign the appropriate warehouse shift code to your operators in 
OPER.
FIELD DESCRIPTIONS
Shift Code Mandatory
Your warehouse shift code.
Description Mandatory
Your description for this warehouse shift code.
Warehouse Code Mandatory
The shift’s warehouse.
Shift ID in Time & Attendance
Reserved for future use
Start Time The start time in 24-hour format of the shift.
End Time The end time in 24-hour format of the shift.

EQUIPMENT TRACKING
Looking Up Equipment Tracking Data
OPER screen showing operator being assigned the warehouse shift code of DAY
Looking Up Equipment Tracking Data
Equipment tracking data is stored in the Oracle database. If you wish to look this data up, you must write a 
d’Amigo query.

OUTBOUND TASKING
Overview .......................................................................................................... 468
Understanding Order Lines, Pick Assignments and Outbound Tasks ....... 468
Company Parameters (COMP) ....................................................................... 470
Wave Manager ................................................................................................. 472
Material Handling Types (MHET) ................................................................... 472
Warehouse Zones (WHZO)............................................................................. 472
Warehouse and Location Format (WARE).................................................... 473
Locations (LOCA)............................................................................................ 473
Task Profile (REGI).......................................................................................... 474
RF Outbound Tasking in RFITLV................................................................... 476
Looking Up Your Outbound Tasks in RFOT................................................. 478

OUTBOUND TASKING
Overview
Overview
Outbound tasking allows you to optimize the distribution of work in your warehouse such that urgent work is 
performed first, congestion in warehouse aisles and zones is avoided whenever possible and the discretion of 
individual RF operators to pick and choose their own work is reduced to a minimum.
Instead of RF operators entering individual RF programs such as RFPIC or RFRP to pick entire order lines 
and perform replenishments at their own pace and in a sequence that does not take into account the work of 
other RF operators, they enter a single program, RFITLV, to work on their first assigned task. The first 
assigned task and all subsequent tasks for an operator are based on the following factors:
▪ the RF operator’s equipment
▪ the RF operator’s “proximity” to the task’s location (that is, is the operator in the same location, aisle or 
zone)
▪ the RF operator’s task profile
▪ the RF operator’s warehouse activity type exclusions (picking only or replenishment only)
▪ the task’s pick method (full pallet pick vs. case pick) 
▪ the location’s height restrictions
▪ the level of congestion allowed in a particular aisle/location
Tasks in the RF operator’s queue are sorted in the following sequence:
▪ task priority override value if any
▪ ship to date/time
▪ order priority/order number
▪ create date/time
▪ sort sequences (SOSE)
If an RF operator chooses to skip a task, AccellosOne 3PL will record the skipped task as well as the operator 
who skipped it. The operator will not see the task again in his or her current RF session.
The RF operator performs outbound tasking in RFITLV (RF Interleaving). RFITLV supports all the standard 
functions performed in RFPIC (case pick mode), REPI, RFRP and RFCE.
UNDERSTANDING ORDER LINES, PICK ASSIGNMENTS AND OUTBOUND TASKS
An order line is a line entered in ENOR representing one item. 
A pick assignment is a single outbound pallet consisting of one or more order lines based on the weight 
and cube limits for a single pallet, whether or not item mixing is allowed on the same pallet and whether or not 
the product is stackable. 
Order line
Pick 
assignment
Pick 
assignment
Pick 
assignment
Task 1 Task 2 Task 3 Task 4 Task 5
full pallet picks case picks

OUTBOUND TASKING
Overview
A task is a pick assignment broken down by location, RF operator and pick method. In other words, the 
smallest possible unit of work in a warehouse. For example, if a pick assignment or outbound pallet of 20 
cases consists of three picks from three different locations, each pick location/RF operator/pick method is 
considered a separate task.
1 — ORDER ENTRY You enter an order line of 80 cases (1 pallet, 20 cases)
2 — WAVE MANAGER Wave Manager creates two pick assignments for the order 
line. A full pallet pick for an RF operator working with a fork 
lift and a case pick for an RF operator working with a pallet 
jack.
Task engine assigns tasks to operators based on RFOP, MHEC, 
REGI and warehouse activity type exclusion settings. Tasks 
are sequenced by ship to date/time, order priority number 
and order create date/time.
If replenishments are required for a pick line location, the 
replenishment must be performed before the pick.
Task engine creates five pick tasks:
task 1 = full pallet pick by RF operator 1
task 2 = pick of 10 cases from location A by RF operator 2
task 3 = pick of 5 cases from location B by RF operator 2
task 4 = pick of 5 cases from location C by RF operator 2
task 5 = replenishment of location C by operator 3
4 — TASK ENGINE
Operator 1
Attached to forklift, can only perform picks
Operator 2
Attached to pallet jack, can only perform picks
Operator 3
Attached to forklift, can only perform replenishments
5 — RF PICKING/
 REPLENISHMENT
RF operators perform their assigned picks and 
replenishments. Case picking, which is slower, may be 
scheduled before full pallet picks.
Operator 3 replenishes location C using a forklift
Operator 2 picks 10 cases from location A, 5 cases from 
location B and 5 cases from location C using a pallet jack
Operator 1 picks a full pallet using a forklift
RFITLV
ENOR
3 — REVIEW PALLET BUILD
 ASSIGNMENTS (OPTIONAL)
If pre-built pallet building is activated in CCCC (that is, pallets 
are built during waving), supervisor can review and edit pallet 
build assignments.
PABU

OUTBOUND TASKING
Company Parameters (COMP)
Company Parameters (COMP)
In this program, you activate tasking by setting the Enable Task Interleaving flag to the appropriate value: 
▪ Create All Tasks
▪ Create Tasks According to Zone Setting
▪ Create All Tasks, Exclude Orders not in Wave
▪ Create Tasks According to Zone Setting, Exclude Orders not in Wave
If you select “Create All Tasks”, tasking will be activated for all warehouse zones whose zone type is set to I 
for Interleaving in WHZO. If you select “Create Tasks According to Zone Setting”, tasking will be activated 
only for warehouse zones whose zone type has been set to I for Interleaving and whose Task Required flag 
has been set to Yes.
COMP screen showing Enable Task Interleaving set to Create All Tasks
The following options also require setup in COMP.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)
RFITLV First Check 
Same Location for Task
Yes
No (default)
If you set this flag to Yes, the task engine will not limit itself to available tasks 
at the current location. If you set this flag to No, the task engine will consider 
order and load priority before checking the same location for a task.

OUTBOUND TASKING
Company Parameters (COMP)
COMP screen showing Same Location/Aisle/Zone fields
RFITLV Second Check 
Same Aisle for Task
Yes
No
If you set this flag to Yes, the task engine will not limit itself to available tasks 
in the same aisle. If you set this flag to No, the task engine will consider order 
and load priority before checking the current aisle for a task.
RFITLV Third Check 
Same Zone for Task
Yes
No
If you set this flag to Yes, the task engine will not limit itself to available tasks 
in the same warehouse zone. If you set this flag to No, the task engine will 
consider order and load priority before checking the current warehouse zone 
for a task.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

OUTBOUND TASKING
Wave Manager
Wave Manager
See the Wave Manager documentation for further information on the Suspend Task function. If you activate 
this function, tasks will be automatically suspended when you generate a wave in Wave Manager. This will 
allow you to manually adjust your pallet build assignments in PABU (Pallet Build) before they are released to 
RF or voice for picking.
Material Handling Types (MHET)
See “Material Handling Types (MHET)” on page 458.
Warehouse Zones (WHZO)
Only locations attached to a warehouse zone whose zone type code has been set to I for Interleaving can be 
used for tasking. See “Warehouse Zones (WHZO)” on page 92 for further information on WHZO.
If you selected the Create Tasks According to Zone Setting option in COMP, you must set the Task Required 
flag to Yes for each warehouse zone in WHZO that you wish to activate.
WHZO screen showing interleaving zone type code and Task Required flag

OUTBOUND TASKING
Warehouse and Location Format (WARE)
Warehouse and Location Format (WARE)
You must define your aisles in the Location Attributes Block of WARE. See the Setup Guide for further information on WARE.
WARE screen showing aisle defined as first character in location code
Locations (LOCA)
In this program, you define your location height restrictions for each location. Only equipment types whose 
vertical height factor code matches the location’s vertical height factor code can be assigned a task in this 
location.

OUTBOUND TASKING
Task Profile (REGI)
LOCA screen showing location assigned a vertical height factor code of 3
Task Profile (REGI)
In this program, you define the following:
▪ the maximum number of RF operators allowed in a warehouse aisle at any one time
▪ the maximum number of RF operators allowed in a warehouse location at any one time
▪ the priority number for forced replenishments
▪ the pick method (full pallet pick or case pick)
▪ the warehouse activity type (picking or replenishment)
If picking and replenishment are performed by different teams in your warehouse, tasking requires two task 
profiles: one for the activity type of picking and one for the activity type of replenishment. If your pickers use 
different equipment based on the pick quantity, you will need a separate task profile for each equipment type. 

OUTBOUND TASKING
Task Profile (REGI)
REGI screen showing five as the maximum number of operators per aisle when picking (activity type = 
26)
FIELD DESCRIPTIONS
Max. Number of OperatorsIn this field, you define “congestion” in a warehouse aisle; that is, if the number 
of operators in a task profile exceeds this number, the extra operators will not 
be assigned any tasks until one or more existing operators completes his or 
her task(s).
Max. Number of Operators per LocationIn this field, you define “congestion” in a warehouse location; that is, if the 
number of operators in a task profile exceeds this number, the extra operators 
will not be assigned any tasks until one or more existing operators completes 
his or her task(s).
Select Only Assignments 
With Both Pick Line/NonPick Line Locations
Reserved for future use.

OUTBOUND TASKING
RF Outbound Tasking in RFITLV
RF Outbound Tasking in RFITLV
You perform tasking in RFITLV (RF Interleaving). Depending on the next available task, RFITLV calls one of 
the following programs: RFPIC, RFRP and RFCE. Refer to the documentation on these programs for further 
information.
1 Enter RFITLV.
Force Replenishment PriorityAll replenishment tasks are assigned a default priority number of 100. This priority number is reduced by 1 each time that an order line cannot be picked 
because the pick location has not been replenished. The process continues 
until the location is replenished and the order line is picked. 
If a replenishment task is found with a priority number less than or equal to the 
number that you enter on this field, it will be released to the operator even if it 
may have other issues such as the quantity in the pick line location is still 
above the minimum quantity or the location is full.
If you leave this field blank, regardless of the task priority number the replenishment task will not be released to the operator when the quantity in the pick 
line location is still above the minimum quantity or the location is full.
REQUIREMENTS
COMP Task interleaving must be activated.
COMP The following fields must be configured: RFITLV First Check Same Location 
for Task, RFITLV Second Check Same Aisle for Task and RFITLV Third Check 
Same Zone for Task.
PALLET BUILDING If you wish to take advantage of the Pallet Build engine, setup is required in 
IPBR, ITEM, REGI and CONS.
OPERATOR RESTRICTIONSYou can deactivate tasking for some or all RF operators by setting up activity 
type exclusions in RFOP. For example, RF operator 1 can only pick, RF operator 2 can only put-away and RF operator 3 can only relocate.
FIELD DESCRIPTIONS

OUTBOUND TASKING
RF Outbound Tasking in RFITLV
RFITLV screen showing prompt for MHE code
2 Key in your MHE code and press Enter.
RFITLV screen showing pick list for task profiles
3 If prompted to do so, select the appropriate task profile from the pick list. If you are restricted to a single 
task profile code, press Enter to acknowledge it.
RFITLV screen showing picking task

OUTBOUND TASKING
Looking Up Your Outbound Tasks in RFOT
4 Do one of the following:
5 Repeat the above steps for each additional task assigned to your task profile.
6 When you finish performing all your tasks, press F4 (RT) to exit. Then key in N for Exit and press Enter.
Looking Up Your Outbound Tasks in RFOT
You can look up your outbound tasks in RFOT and, if required, change their priority or suspend them.
1 Enter RFOT.
2 If required, click on the Pick/Interleave (2) tab.
To perform the task: To skip the task:
a) Press F3 (SL) to select the line 
that you wish to work on.
b) Proceed to perform the pick/
replenishment the task.
a) Press F4 (RT).
b) Key in Y for next task and press 
Enter or key in N for exit and 
press Enter.

OUTBOUND TASKING
Looking Up Your Outbound Tasks in RFOT
RFOT screen showing Pick/Interleave (2) tab
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all order lines 
that meet your filter criteria.
4 Click on the Tasks tab. This tab shows the following information for each task:
▪ the order number
▪ the line number
▪ the order priority
▪ if the pallet is built from product in multiple locations, the sort sequence number for these locations
▪ if the pallet is built from product in multiple locations, the assignment number
▪ the release date (the release date is the order ship date on the order header)
▪ whether or not the task has been suspended
▪ the priority override value (if any)

OUTBOUND TASKING
Looking Up Your Outbound Tasks in RFOT
RFOT screen showing Tasks tab (if Sort Sequence and Assignment Number fields are blank, the 
assignment is a full pallet pick)
5 If required, you can change the priority of an outbound task. The default value is 100. If you enter a lower 
value (say, 50), the outbound task will have a lower priority.
6 If required, you can suspend a task by selecting the Suspend Task checkbox.
7 If you made any changes in the previous two steps, click on Save to save your changes.
8 If you wish to look up your pick assignments in assignment sequence, click on Order Assignments.
RFOT screen showing Order Assignments tab

OUTBOUND TASKING
Looking Up Your Outbound Tasks in RFOT
9 When you finish looking up your order line tasks, click on Exit the required number of times to exit.

OUTBOUND TASKING
Looking Up Your Outbound Tasks in RFOT

INDEX
A
accessing RF 132
adjusting non-serial number inventory 346
adjusting serial number inventory 355
alternate item codes in RFCH 184
alternate item codes in RFPU 201
assignments, pick method 217
auto-confirming receipts in RFCH 157
auto-confirming receipts in RFPU 157, 193
B
BAPR (Bar Code Profile Code) 12
blind receiving in RFCH 154
C
cartonization 418
Cartonization tab (MRFP) 418
cartons, deleting in DCAR 451
cartons, looking up in LOCN 449
CASE (Case Picking) 267
case picking 227
catch weight tolerances 302
CCCC (Outbound Process Configuration) 120, 422
CCDU (Customer / Consignee Document Setup) 109
CCOR (Customer Consignee Outbound Rules) 124
changing your company 132
CONS (Consignees) 429
Consolidation Method for Allocated Lines field (CUST) 107
count backs, performing in RFPIC 246
CRM tasks, performing in RF 379
CTPA (Clear Terminal Pick Assignments) 415
CTSZ (Carton Size Setup) 420
CUST (Customer Codes) 107
Customer/Consignee Outbound Rules (CCOR) 124
D
damaged product, replacing in RFRD 317
DCAR (Delete Carton) 451
E
entry of expiry dates in RFCH 164
EOSU (Exclude Orders from RF Substitution) 280
EPSD (Enter Packing Details) 442
equipment tracking 454
excluding orders from overpicking in EOSU 241
extra charge setup 89
extra charges, adding to receipt/order in RFEC 370
F
first level cartonization 418
H
holds, placing product on in RFCH 186
holds, placing product on in RFPIC 236
I
ICIN (Inventory Count Investigation) 249
ICNP (Item Cartonization Profile Code) 427
ICOC (Item Consignee Configuration) 119
IHZV (Item Hazardous Material Violation) 110
inbound flows, understanding 153
inventory counting in RFPIC 246
inventory, merging 363
IPBR (Item Pallet Build Restrictions) 111
Item Consignee Configuration (ICOC) 119
Item Hazardous Material Violation (IHZV) 110
L
LOCN (Look Up Carton) 259, 449
LOENRF (RF Look Up Entity Information) 144
LOLORF (Look Up Location - RF) 142
looking up temperature and trailer information in LORE 189
look-up programs 131
LOORRF (Look Up Orders - RF) 147
LORERF (RF Look Up Receipts) 145
INDEX

INDEX
M
MCHK (RF Checklist) 455
merging inventory 363
merging OPID’s 309
MHEC (Material Handling Equipment Code) 401, 461
MHET (Material Handling Types) 458
MIRP (Item RF Profile) 84
Miscellaneous (2) tab (MRFP) 67
Miscellaneous (3) tab (MRFP) 71
Miscellaneous tab (MRFP) 64
mixed product, receiving in RFCH 187
MRFP (RF Profile Code) 16
multi-pallet moves 344
O
one-step put-away 152
OPID’s, looking up in LOCN/LOOR 259
OPID’s, merging 309
outbound flows, understanding 217
outbound pallet building 111
overpicking, excluding orders from in EOSU 241
overriding the system-assigned location in RFCH 169
overriding the system-assigned location in RFPU 198
P
Pallet Build (PABU) 319
Pallet Build engine 111
Pick & Pack 418
pick and pack cartonization 434
pick methods 217
picking orders in RFPIC 220
picking pick line product from a non-pick line location in RFPIC 242
picking programs, overview of 219
picking substitution 275
process values
entering in RFIPS 202
entering in RFOPS 284
entering in RFPIC 232
PSPR (RF Substitution Profile Code) 276
putting away to a pick line location in RFPU 202
Q
queries, performing in RFCH 174
R
REAS (Reason Code) 400
receiving mixed product in RFCH 187
REGI (Task Profile) 113, 396
relocating inventory in RFRL 335
replenishments, performing in RFPIC 243
reserve logic orders, picking 235
RF Bar Code Read (RFBR) 381
RF Confirm OPID (RFCO) 261
RF Confirm UI (RFCU) 263
RF CRM Entry (RFCE) 379
RF Delete Line (RFDL) 208
RF Extra Charge (RFEC) 370
RF Merge Inventory (RFMI) 363
RF Merge OPID (RFMG) 309
RF Operator (RFOP) 87
RF Operator Task Assign (RFOT) 406
RF Substitution Profile Code (PSPR) 276
RF supervisors 101
RFAJ (RF Adjustment)
adjusting in inventory 356
adjusting out cases 358
adjusting out full pallets 359
adjusting out using Remove command 360
overview 346
recovering from a lost connection 362
RFAJB (RF Adjustment)
overview 355
RFATT (RF Attributes) 387
RFBR (RF Bar Code Read) 381
RFCC (RF Carton Cube) 316
RFCD (RF Check Digit) 374
RFCE (RF CRM Entry) 379
RFCH (RF Check Unload)
creating a new line 183
entering expiry dates 164
entering partial U-type receipt lines in 175
entering process values 180
entering trailer and pallet information 170
looking up remarks in 190
overview 154
performing queries in 174
printing labels in 176
processing variances 177
receiving mixed product 187
receiving product on automatic hold 186
receiving product under an alternate item code 184
receiving product with a variable quantity breakdown
187
validating process values in 182
RFCH Only (2) tab (MRFP) 25
RFCH Only tab (MRFP) 18
RFCH Queries tab (MRFP) 16
RFCH Shared tab (MRFP) 29
RFCI (Clear Inventory Count Investigation) 252
RFCL (RF Count Log) 250, 252
RFCO (RF Confirm OPID) 261
RFCU (RF Confirm UI) 263
RFCV (Clear Receipt Tie/Hi/Loose) 210
RFDL (RF Delete Line) 208
RFEC (RF Extra Charge) 370
RFHO (RF Hold Adjustment) 382
RFIL (RF Receipt Line Look-Up) 136
RFINC (RF Incidents) 377
RFIPS (RF Inbound Process Scanning)
capturing the weight dynamically from a bar code 204
overview 202
weight discovery 204
RFIT (RF Item Look-Up) 132
RFITLV (RF Interleaving) 476
RFLOIP (RF Look Up Item Process) 141
RFLR (RF Look Up Reserve Logic Customers) 148

INDEX
RFMG (RF Merge OPID) 309
RFMI (RF Merge Inventory) 363
RFNCO (OPID Look-Up) 259
RFOA (RF Outbound Audit) 313
RFOL (RF Order Line Look-Up) 138
RFOLP (Outbound Label Printing) 264
RFOP (RF Operator) 87, 463
RFOPB (RF Outbound Pallet Build) 272
RFOPE (Order Pallet Entry) 254
RFOPS (RF Outbound Process Scanning)
capturing the weight dynamically from a bar code 289
incomplete scans 300
manually entering weight when weight cannot be captured 294
overview 284
removing cases from a fully scanned order 298
removing cases that have been scanned 297
removing labels that have been scanned 295
transferring inbound process values to outbound orders 301
weight discovery 289
RFOT (RF Operator Task Assign) 406
RFPA (RF Pallet Code Update) 257
RFPIC (2) tab (MRFP) 48
RFPIC (3) tab (MRFP) 54
RFPIC (RF Pick)
case picking 227
entering pallet information 239
entering process values 232
excluding orders from overpicking 241
looking up remarks in 243
overview 220
performing countbacks in 246
performing picking substitution in 281
performing replenishments in 243
picking full pallets from bulk 225
picking partial quantities of product with process values 234
picking pick line product from a non-pick line location
242
placing product on hold 236
reserve logic orders 235
RFPIC tab (MRFP) 41
RFPK (RF Wave Pick) 304
RFPR (RF Product Look-Up by Location) 134
RFPU (RF Put-Away) 192
RFPU tab (MRFP) 38
RFPV (RF Picking Voice) 220, 403
RFRD (Replace Damage) 317
RFRL (RF Relocate) 335
RFSC (RF Sort Carton) 429
RFST (RF Staging) 307
RFSUN (RF Supervisor Notification) 385
RFTT (RF Temperature and Trailer) 191, 253
S
SCPR (Scan Parameter Profile) 6
second-level cartonization 441
substitution (picking) 275
supervisor notification 101
supervisors (RF) 101
suspended hold options 45
system-driven cartonization 418, 434
T
task engine, about 106
Task Profile (REGI) 396
tasking 468
tasks, looking up in RFOT 478
temperature and trailer information, looking up in LORE
189
three-step put-away 160
two-step put-away 152
U
unique identifier, overview 153
V
validating process values in RFCH 182
variances in RFCH, overview 177
variances, entering in RFCH 178
variances, entering in RFPU 199
Voice Profile - Customer (VOPC) 393
Voice Profile (VOPR) 390
voice-activated picking, overview 390
VOPC (Voice Profile - Customer) 393
VOPR (Voice Profile) 390
W
Warehouse Customer Consignee OPID Rule (WCCO) 124
Warehouse Zones (WHZO) 92
WASH (Warehouse Shift Setup) 464
WCCO (Warehouse Customer Consignee OPID Rule) 124
WCLC (Warehouse/Customer/Location Config) 86
weight discovery in RFIPS 204
weight discovery in RFOPS 289
WHZO (Warehouse Zones) 92

INDEX
