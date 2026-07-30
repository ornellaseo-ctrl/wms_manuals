---
title: "RF — Setup, Navegação, Lookups e Equipamentos"
description: "Perfis de RF e scanner, tasking, navegação, consultas no coletor, voice e equipamentos."
layout: default
---

# RF — Setup, Navegação, Lookups e Equipamentos

Perfis de RF e scanner, tasking, navegação, consultas no coletor, voice e equipamentos.

**Fluxo principal:** `MRFP/SCPR/BAPR/MIRP (perfis) -> REGI (tasking) -> lookups RF`

> Fonte: manuais H do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction <a id="introduction"></a>

*Manual H — RF Guide*

# Manual H — RF Guide (Guia de Operações RF/Scanner)
> **ID do Manual:** H  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Operações via scanner RF: setup (SCPR/BAPR/MRFP/MIRP), check/unload (RFCH), put-away (RFPU), picking (RFPIC), wave pick (RFPK), relocação (RFRL), ajustes (RFAJ), cartonization, outbound pallet building, staging, weight discovery, voice picking, equipment tracking, tasking (REGI).
---

### Before You Begin <a id="before-you-begin"></a>

This manual contains the majority of core RF programs that are part of AccellosOne 3PL. The following core 
RF programs are not included: 
▪ RFCY (RF Cycle Count) — see Cycle Counting Guide
▪ RFPH (RF Entering Physical Inventory Tickets) — see Physical Inventory Guide
▪ RFPL/RFPR (Replenishment) see Allocation and Wave Manager 
▪ OLOP (Outbound Loading Process) see Operations 2 Guide

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
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

## General Setup Programs <a id="general-setup-programs"></a>

*Manual H — RF Guide*

### Scan Parameter Profile (SCPR) <a id="scan-parameter-profile-scpr"></a>

In this program, you define your scan parameters for bar coded labels. SCPR allows you to break up a bar code into its component parts and capture a separate value for each part. For example, the first four characters of the bar code could represent the lot number, characters 6 to 10 could represent the weight and characters 11 to 14 could represent the serial number.
In the Header Block of SCPR, you define your scan profile code, description and total length. In the Detail 
Block of SCPR, you define whether the bar code is inbound or outbound, its type (weight, serial number, etc.), starting and end position, the action required when it is scanned and its data type. You can have as many records in the Detail Block as you require. For example, if a bar code consists of three parts (one for the weight, one for the level 2 value and one for the serial number), you would set up three records in the Detail 
Block for that scan parameter profile.
If you are capturing weights, serial numbers or a temperature, the profiles that you set up in SCPR must be attached to the appropriate items in ITEM. If you are capturing inventory levels that were unknown at the time of receipt entry (that is, blind receiving), the SCPR profile(s) are NOT attached to the appropriate items in 
ITEM.
NOTE SCPR only supports bar code scanning of items with no more than two 
SKU’s in their quantity breakdown (for example, pallet/case). You cannot scan bar codes of items with three or more SKU’s in their quantity breakdown (for example, pallet/case/each).
FIELD DESCRIPTIONS
Scan Profile Code Mandatory
Your scan profile code.
Description Mandatory
The description for your scan profile code.
Scan Profile Industry 
Type
If you enter 128, your label will be defined as a UCC-128 label.

Variable Length Y = Yes
N = No
Set this flag to Yes if the bar code that you are attaching your scan parameter profile to is a variable length bar code. Otherwise, set the flag to No.
Scan Profile Code Length Mandatory
The total length of the bar code.
FIELD DESCRIPTIONS (DETAIL BLOCK)
Inbound/Outbound I = Inbound
O = Outbound
B = Both
If you specify I for Inbound, the portion of the bar code that you are capturing is restricted to an inbound RF process. If you specify O for Outbound, the portion of the bar code that you are capturing is restricted to an outbound RF process. If you specify B for Both, the portion of the bar code that you are capturing can be used in either an inbound or outbound RF process. 
Sequence Mandatory
In this field, you specify the sequence of each scanned in value. The sequence that you enter need not match the physical layout of the bar coded label.
You can extract an inventory level from multiple sequences in a bar code. For example, if your bar code is 0123456789, you can define two sequences for the level 3 value: sequence 1 for positions 1 to 2 and sequence 2 for positions 
9 to 10. Your level 3 value extracted from the bar code would be 0189.
The extraction of an inventory level from multiple sequences of a bar code is only available in RFCH blind receiving.
FIELD DESCRIPTIONS

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
The type of value that you are capturing. If a portion of the bar code that you are scanning contains information that you do not wish to capture, you can use the IGNO (Ignore Entry) option. Any part of a bar code assigned this type will not be captured by AccellosOne 3PL.
NOTE If you use two or more values such as CUBE, HGT, LEN and WID in the same scan parameter profile, each value must be captured on a separate label. Only the values of SER, LEV1/2/3/4, UI, WGTG and WGTN can be combined together and captured from a single label.
* The inventory level will be validated against the acceptable values that 
you defined in DLVP and any item whose lot number, serial number, date code, etc. does not match the acceptable values will be rejected. 
Start Position Mandatory for fixed position bar codes
The position of the start character of the value that you are capturing. For example, if the total length of your bar code is 10 characters and the portion of the bar code that you are capturing is position 3 through 7, you would enter 3 in this field.
FIELD DESCRIPTIONS (DETAIL BLOCK)

End Position Mandatory for fixed position bar codes
The position of the last character of the value that you are capturing. For example, if the total length of your bar code is 10 characters and the portion of the bar code that you are capturing is position 3 through 7, you would enter 7 in this field.
You can also define the end position by leaving this field blank and entering the appropriate value in the Length field.
Start Character Reserved for future use
The number, letter or special character indicating the start of the portion of the bar code that you wish to capture.
End Character Reserved for future use
The number, letter or special character indicating the end of the portion of the bar code that you wish to capture.
Length Only applicable to fixed position bar codes
The length of the portion of bar code that you are capturing If you are using the UCC-128 label, the length is usually 48.
Action The following actions are supported:
01 = Entry
02 = Validation
If you select Entry, validation may or may not occur depending on the value being captured. If you select Validation, AccellosOne 3PL validates the value against a list of valid values.
Date Format In this field you can specify the date format of any dates scanned in from a 
SSCC label and saved in AccellosOne 3PL as an inventory level. 
FIELD DESCRIPTIONS (DETAIL BLOCK)

Unit of Measure Code Only required if you enter a weight, cube or linear measurement in the Type field
The unit of measure for the captured value.
Data Type CHAR = Character
DATE = Date
INT = Integer
MONY = Money
NUM = Number
This field controls the formatting of values that you capture. If you select 
DATE, the number that you enter will be formatted as a date. If you select 
MONY, the number that you enter will be formatted in dollars and cents (for example, $99.99).
Use CHAR for serial and purchase order numbers.
Decimal Position Only applicable to scanned in values with a data type of MONY or NUM
The position of the decimal point. For example, if you specify 2 and your captured value is 12345, AccellosOne 3PL will record the value as 123.45. If you do not specify the position of the decimal point, all numbers will be captured as integers.
Weight Modifier Only applicable to scanned in values whose unit of measure code is a weight (KGS or LBS)
If required, you can specify a weight modifier and the scanned in weight will be multiplied by the modifier.
FIELD DESCRIPTIONS (DETAIL BLOCK)

Validate Item Code Only available for item code validation
P = Position-Based
L = Left Starting Position
R = Right Starting Position
Item code validation allows you to validate the item code in RFOPS when the item code in the bar code is shorter than the item code in ITEM. That is, the level 1 in the bar code is a subset of the full level 1 in ITEM.
In this field, you specify the position of the item code in the bar code.
Item Code Start Position Only available for position-based validation
The start position for the item code.
Item Code End Position Only available for position-based validation
The end position of the item code.
Item Code Length for 
Right/Left Starting Position
The number of characters from the right or left that comprise the item code.
FIELD DESCRIPTIONS (DETAIL BLOCK)

SCPR (Scan Parameter Profile) screen showing scan parameters for scan profile code L2

### APPLICATION IDENTIFICATION BLOCK <a id="application-identification-block"></a>

Used to set up the MARS bar code.

### Bar Code Profile Code (BAPR) <a id="bar-code-profile-code-bapr"></a>

In this program, you set up your bar code profile codes. Bar code profile codes are only required if you wish to scan in inventory levels or UI (Unique Identifier) values that are embedded in a bar code label. If the value that you are scanning is not embedded in another code (that is, the level 1 or 2 or 3 label contains no other value or extra characters), you do not need to set up a bar code profile in BAPR.
UI values can be scanned in RFCH, RFPIC and many other RF programs. Inventory levels, on the other hand, can only be scanned in RFCH. For each profile that you set up in BAPR, you define the value being scanned (LEV1, LEV2, LEV3, LEV4, UI), the scan parameter code to which it is attached, the bar code length and the bar code ID. 
If you are capturing two or more inventory levels in RFCH, you can do so from multiple bar code labels. For example, you could scan in levels 1 and 2 from bar code label A and level 3 from bar code label B.

Consider the following SCPR and BAPR setups for various bar coded labels. In the following examples, “---” 
represents an inventory level, UI, weight or serial number that you wish to capture, while “999” represents non-AccellosOne 3PL information in the bar code that you do not wish to capture.
BAR CODE(S) SCPR SETUP BAPR SETUP ITEM SETUP
---L1--- N/A N/A N/A
---L3--- N/A N/A N/A
999---L1--- A profile with one detail record whose type is set to LEV1.
The SCPR profile set up in the previous column must be attached to a bar code profile whose bar code type is set to 
LEV1.
N/A
---L2---999 A profile with one detail record 
whose type is set to LEV2.
The SCPR profile set up in the previous column must be attached to a bar code profile whose bar code type is set to 
LEV2.
N/A
---L1---L2---L3--- A profile with three detail 
records: one whose type is set to 
LEV1, another whose type is set to LEV2 and a third whose type is set to LEV3.
The SCPR profile set up in the previous column must be attached to a bar code profile whose bar code type is set to 
LEV1.
N/A
999---L1---
---L2---999
Two profiles required: one with a detail record set to LEV1 and one with a detail record set to 
LEV2.
Two records required: one for the level 1 label and one for the level 
2 label. The appropriate SCPR profile must be attached to each record.
N/A
999---L1---999---L2---999
999---L3---999
Two profiles required. The first profile will contain two detail records: one set to LEV1 and one set to LEV2. The second profile will contain a single record set to LEV3.
Two records required: one for the level 1/2 label and one for the level 3 label. The appropriate 
SCPR profile must be attached to each record.
N/A
---UI---999 A profile with one detail record 
whose type is set to UI.
The SCPR profile set up in the previous column must be attached to a bar code profile whose bar code type is set to UI.
N/A
999---WEIGHT--- A profile with one detail record whose type is set to WGTG or 
WGTN.
N/A The SCPR profile must be attached to the item.

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
SCPR, the bar code type is set to the lowest inventory level. For example, if your label format is 999---LEV2---LEV3, your bar code type would be set to 
LEV3, which is the lowest inventory level.
Scan Parameter Profile 
Code (SCPR)
Mandatory
The bar code profile’s scan parameter profile code. 
Bar Code ID Optional
The bar code’s ID. This ID identifies the manufacturer of the product. The number of characters in this field must equal the end position - the start position + 1.
NOTE Although bar code ID’s are optional in BAPR, they should be used whenever they are available. If you do not specify a bar code ID, operators will be confronted with a pick list whenever two bar codes have the same length. If the RF operator selects the wrong code from the pick list, he or she could capture bad data.

Start Position Mandatory if you enter a bar code ID
The starting position of the bar code ID.
End Position Mandatory if you enter a bar code ID
The ending position of the bar code ID.
Variable Length Only available for variable length bar codes based on the GS-1 standard.
The length of the variable portion of the bar code.
Bar Code Length Mandatory
The total length of the bar code. This length must match the length of the scan parameter profile code in SCPR.
Size of Fixed Part in Variable Length Bar Code
Only available for variable length bar codes based on the GS-1 standard.
See your HighJump implementation consultant for further information on this field.
ASCII Value of Separator in Variable Length Bar 
Code
Only available for variable length bar codes based on the GS-1 standard.
See your HighJump implementation consultant for further information on this field.
FIELD DESCRIPTIONS

BAPR (Bar Code Profile Code) screen showing setup for bar code L12

### RF Profile (MRFP) <a id="rf-profile-mrfp"></a>

In this program, you set up your RF profile code(s). The RF profile code defines the default values and available options in the core RF programs. Once you set up your RF profile code in MRFP, you must attach it to the appropriate customer(s) in CUST.

### RFCH QUERIES <a id="rfch-queries"></a>

This tab shows your RFCH query options.

RFCH Queries tab
FIELD DESCRIPTIONS (RFCH QUERIES)
Customize Query Results in RFCH
Yes
No
If you set this field to Yes, you can customize the RFCH pick list in query mode. For example, if you set the Receipt Number and Warehouse Code fields to Yes and all the other fields to No, only the receipt number and warehouse code will appear in the RFCH pick list when you perform a query.
If you set this field to No, you cannot customize the RFCH pick list and all values — customer code, receipt number, receipt line number, all inventory levels, etc — will display in this list. 

### RFCH ONLY <a id="rfch-only"></a>

This tab shows various RFCH options.
RFCH pick list screen showing customization
Receipt Number If you set this field to Yes, the receipt number will appear in the RFCH pick list when you perform a query.
Receipt Line Number If you set this field to Yes, the receipt line number will appear in the RFCH pick list when you perform a query.
Inventory Level 1 If you set this field to Yes, inventory level 1 will appear in the RFCH pick list when you perform a query.
Inventory Level 2 If you set this field to Yes, inventory level 2 will appear in the RFCH pick list when you perform a query.
Inventory Level 3 If you set this field to Yes, inventory level 3 will appear in the RFCH pick list when you perform a query.
Inventory Level 4 If you set this field to Yes, inventory level 4 will appear in the RFCH pick list when you perform a query.
Warehouse Code If you set this field to Yes, the warehouse code will appear in the RFCH pick list when you perform a query.
Quantity If you set this field to Yes, the quantity will appear in the RFCH pick list when you perform a query.
Hold Code If you set this field to Yes, the hold code will appear in the RFCH pick list when you perform a query.
FIELD DESCRIPTIONS (RFCH QUERIES)

RFCH Only tab
.
FIELD DESCRIPTIONS (RFCH ONLY)
Label Document Printed Optional
If you enter a document code in this field, the RF operator will be prompted to print the document in RFCH should he/she create a new receipt line. The document code that you enter in this field must have a document type of LA (Label) in DOCU.
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

In this field, you specify which information an RF operator can enter for each receipt: temperature only, pallet block only, trailer/seal number only, etc. The options in this field are not mandatory; that is, if temperature entry is activated, the RF operator can enter a temperature in RFCH, but is not required to do so.
RFCH screen showing prompt for temperature and trailer number information
Perform Trailer Checks Only available if the entry of trailer numbers is activated in the Show Temperature and Pallet Blocks field
Yes
No
If you set this flag to Yes, the RF operator will be prompted to perform a series of trailer checks. If you set this flag to No, the RF operator will NOT be prompted to perform any trailer checks.
RFCH screen showing trailer check
FIELD DESCRIPTIONS (RFCH ONLY)

Allow New Lines Yes (1)
No (2)
Stay in New Line Mode (3)
Allow New Line from Existing Entity on Receipt, Do Not Show New Line 
Message (4)
Allow New Line With Supervisor Approval
If you select option 1, the RF operator can create new receipt lines in RFCH with the CL (Create Lines) command and will be prompted to either mark a receipt as complete or create a new line when finishing the last line of a receipt. 
If you select option 2, the RF operator cannot create new receipt lines in 
RFCH and will not be prompted to do so when finishing the last line of a receipt.
If you select option 3, the RF operator will NOT be prompted to either mark a receipt as complete or create a new line and the header flow of the receipt will 
NOT be advanced.
If you select option 4, the RF operator can only add a new line if the new line consists of an existing inventory entity on the receipt. For example, the RF operator receives 20 cases for pallet ID 123 and later discovers an additional case for the same pallet ID. That case can be added, but a case for pallet ID 
456 (which is not on the receipt) cannot be added.
If you select option 5, the RF operator can only add a new line if a supervisor logs in to authorize the transaction.
FIELD DESCRIPTIONS (RFCH ONLY)

Allow Duplicate Inventory No Validation (1)
Disallow Duplicate Inventory Entities (2)
Disallow Duplicate Inventory UI’s (3)
Disallow Duplicate Inventory Entities, No User Override (4)
Disallow Duplicate Inventory UI’s, No User Override (5)
This flag allows the RF operator to check for duplicate inventory in RFCH when the line type is U for Unknown in ENRE. If you select option 1, no popup message will appear when the RF operator receives duplicate inventory in 
RFCH.
If you select option 2, a pop-up message will appear when the RF operator receives a duplicate inventory entity and he/she will be prompted to accept or reject the duplicate scan.
If you select option 3, a pop-up message will appear when the RF operator receives a duplicate inventory UI and he/she will be prompted to accept or reject the duplicate scan.
If you select option 4, the RF operator will not be allowed to receive a duplicate inventory entity.
If you select option 5, the RF operator will not be allowed to receive a duplicate inventory UI.
Default Staging Warehouse/Location CodeIf you enter a staging location and warehouse, the Loc and Whse fields will be populated with these values when you are performing two-step put-away with manual staging. You can either accept the defaults or enter a new staging location and warehouse. 
FIELD DESCRIPTIONS (RFCH ONLY)

Must Use Tie/Hi/Loose to 
Calculate Receiving 
Quantity
No
Yes
Yes With Variance Check in P-Type Lines
If you set this flag to No, the Tie, Hi and Loose fields in RFCH will be disabled and the RF operator can only enter the total quantity for a receipt line. 
If you set this flag to Yes, the RF operator will be required to enter the tie, hi and loose quantities for each receipt line and the Qty field in RFCH will be disabled. For example, a tie, hi and loose quantity of 5/10/03 would equal 53 cases, while a tie, hi and loose quantity of 5/10/-1 would equal 49 cases. The 
Yes option is designed to force RF operators to perform more accurate counts and reduce receiving errors.
If you set this flag to Yes With Variance Check in P-Type Lines, the following will occur. If the line quantity calculated from the tie/hi/loose quantities entered by the operator in RFCH does not match the expected quantity in ENRE, the operator will be allowed to enter the tie/hi/loose quantities a second time. If there is still no match, the variance must be processed by a supervisor in 
RFCV.
Variance Rules Variance screen for all users
Variance screen for supvr. only
Only allow if supvr. approved
This field determines whether or not the Variance screen is displayed when the quantity entered does not match the expected quantity. If you select the “Variance screen for all users” option, any user can process a variance. If you select the “Variance screen for supvr. only” option, non-supervisors will not be able to press F3 to zero out the line. 
If you select the “Only allow if supvr. approved” option, when non-supervisors press F3 to zero out the line a supervisor must sign on and approve the transaction.
NOTE Regardless of the option that you choose, the variance itself is always tracked in LORE even if the Variance screen does not display.
Tolerance Check for PO Reserved for future use.
FIELD DESCRIPTIONS (RFCH ONLY)

Enter Quantity Breakdown for U-Type LineNo
Yes
Set Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes
If you select No, the RF operator cannot change the quantity breakdown for a 
U-type line in RFCH. If you select Yes, the RF operator can change the quantity breakdown for a U-type line in RFCH; that is, override the quantity breakdown entered in ENRE. If you select “Set Quantity Breakdown to Line 
Quantity for IQBP With 2 SKU Classes”, the item’s quantity breakdown will be automatically set to the line quantity entered in RFCH.
The following requirements must be met for the Yes and “Set Quantity Breakdown to Line Quantity ...” options:
▪ the item is set up as a variable quantity breakdown item in ITEM
▪ the item has been received on a U-type line in ENRE
▪ the inventory entity is new (that is, it has not been previously received in the warehouse)
RFCH screen showing prompt for quantity breakdown
Expiry Date Rules Disable expiry date entry for U-type line
If you select this option, the expiry date entry screen will NOT display in RFCH even though manual entry of expiry dates has been activated for the item in 
ITSH.
If you leave this field blank, the expiry date entry screen will display in RFCH if manual entry of expiry dates has been activated for the item in ITSH.
FIELD DESCRIPTIONS (RFCH ONLY)

### RFCH ONLY (2) <a id="rfch-only-2"></a>

This tab shows additional RFCH options.

MRFP screen showing RFCH Only (2) tab
Enter/Change Hold Code Allow Entry/Change of Hold Code (default value)
Disallow Change of Hold Code. Allow New Hold Code.* 
Disallow Entry/Change of Hold Code*
Skip Hold Code
If you select “Allow Entry/Change of Hold Code“, the RF operator can enter new hold codes and change existing hold codes in RFCH. If you select “Disallow Change of Hold Code. Allow New Hold Code.’, the RF operator can enter new hold codes but cannot change existing hold codes in RFCH. 
If you select “Disallow Entry/Change of Hold Code”, the RF operator will have access to the Hold field in RFCH but cannot change a hold code. If you select “Skip Hold Code”, the RF operator will have no access to the Hold field and as a consequence will not be able to change the quantity.
* The two non-default options in this field are NOT available when an item hold profile is 
set up in IHOP and attached to an item in ITEM.
FIELD DESCRIPTIONS (RFCH ONLY)

FIELD DESCRIPTIONS (RFCH ONLY 2)
Validate Item Weight/
Cube Setup
Not Required
Check Weight and Cube
This field allows you to check whether the base SKU of the item being received has a weight and cube greater than zero.
If you select “Not Required”, no check will be made of the item’s base SKU weight and cube. 
If you select “Check Weight and Cube”, AccellosOne 3PL will perform the check. If the item fails the check, the RF operator will be forced to enter the missing values in RFCH before receiving the receipt line. RFCH in turn will update the missing values in the Quantity Breakdown Block of ITEM.
Extra Charge Entry Type See [Extra Charge Setup for RF](picking-rf.html#extra-charge-setup-for-rf) for further information.
Concatenate Inventory 
Level in U-Type Line
Only available for U-type lines in which the RF operator selects the receipt number from a pick list
Concatenate Level 2 to Beginning of Current Value
Concatenate Level 2 to End of Current Value
If you select either of these two options, a scanned in value such as a date code (for example, 101101) will be appended to either the beginning or end of the level 2 value. 
For example, office staff create a U-type receipt line in ENRE and enter the level 2 value normally. In RFCH the RF operator scans in a value and that value is concatenated to the level 2 value entered in ENRE.
Keep First Location Entry and Skip the Field
No
Yes
If you select Yes, the RF operator can skip the Location field after his or her first entry and put-away the remaining receipt lines in the same location.
Allow Change to Receiving ModeNo
Yes
If you select Yes, the RF operator can switch from one-step put-away to twostep put-away (or vice versa) in RFCH.

Special Receiving Mode 
Types
U Line Receiving, Enter UI, Scan Serial as Inventory Level
RFCH to Gen Stag Loc, RFPU to PnD Loc, Then to Final Loc*
RFCH to Gen Stag Loc, RFPU to PnD Loc, Then to Final Loc
RFCH Overrides*
In this field, you can select a special receiving type mode required for your facility. If you leave this field blank, special receiving type modes will be deactivated.
*These two special receiving mode types require special setup. See the section on 
three-step put-away in “Unloading Product in RFCH”.
Validate Inventory Level from Bar Code Using 
SCPR Code
Your scan parameter profile code for validating inventory levels in RFCH receiving. This code is a default scan parameter code at the customer level. In 
ITEM, you can override your customer default by entering an SCPR code in the Scan Parameter Code for Inventory Validation (SCPR) field.
If an invalid inventory level is scanned in RFCH, the RF operator will not be allowed to proceed.
Door Rules Door Not Used
Enter/Update Door in RFCH
If you select Door Not Used, the RF operator cannot select or change a door assignment. If you select Enter/Update Door in RFCH, the RF operator can enter/change a door assignment.
Display Quantity BreakdownNo
Yes
If you select No, the item’s quantity breakdown will be suppressed in RFCH. If you select Yes, the item’s quantity breakdown will be displayed in RFCH. 
RFCH showing quantity breakdown displayed
FIELD DESCRIPTIONS (RFCH ONLY 2)

Allow Put-Away of Multiple Pallets in RFCHNo
Yes
If you select Yes, the RF operator can put-away multiple pallets in a single step; that is, the RF operator scans two or more UI’s in RFCH but only enters the to location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
Enter Quantity Breakdown for P-Type LineNo
Yes
Set Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes
If you select No, the item’s quantity breakdown cannot be changed in RFCH. If you select Yes, the RF operator can change the quantity breakdown in RFCH; 
that is, override the quantity breakdown entered in ENRE. If you select “Set 
Quantity Breakdown to Line Quantity for IQBP With 2 SKU Classes”, the item’s quantity breakdown will be automatically set to the line quantity entered in RFCH.
The following requirements must be met for the Yes and “Set Quantity Breakdown to Line Quantity ...” options:
▪ the item is set up as a variable quantity breakdown item in ITEM
▪ the item has been received on a P-type line in ENRE
▪ the inventory entity is new (that is, it has not been previously received in the warehouse)
FIELD DESCRIPTIONS (RFCH ONLY 2)

### RFCH ONLY (3) <a id="rfch-only-3"></a>

This tab shows additional RFCH options.
RFCH screen showing prompt for quantity breakdown
Update Expiry Date for PType LineNo
Yes
If you select Yes, the RF operator can override the expiry date for P-type lines in RFCH. The item shipping profile (ITSH) attached to the item must have expiry date entry activated (Enter Expiry Dates = Yes).
RFCH screen showing prompt for expiry date
FIELD DESCRIPTIONS (RFCH ONLY 2)

MRFP screen showing RFCH Only (3) tab
FIELD DESCRIPTIONS (RFCH ONLY 3)
Capture Photo When 
Unloading First UI
Only available for Intermec CK71 devices
Yes
No
If you select Yes, you can capture images when unloading first UI. If you select No, image capture will be deactivated when unloading first UI.
Capture Photo When UI is Put On Hold
Only available for Intermec CK71 devices
Yes
No
If you select Yes, you can capture images when placing UI on hold. If you select No, image capture will be deactivated when placing UI on hold.

Duplicate Receiving 
Rules if Qty. Entered < 
Qty. Received
Create Second Line With Remainder (1)
Prompt User to Zero Out Second Line (2)
Zero Out Second Line Automatically (3)
In this field, you specify your receiving rules when the quantity entered in 
RFCH is less than the quantity received in ENRE.
EXAMPLE quantity entered (ENRE) = 100 CS quantity received (RFCH) = 99 CS
With option 1, AccellosOne 3PL will create a second line with a quantity of 1. 
With option 2, the RF operator will be prompted to zero out the second line. If the RF operator selects Yes, the result will be option 3; if the RF operator selects No, the result will be option 1.
With option 3, AccellosOne 3PL will automatically create a second line with a quantity of 0.
Allow Mixed Pallet for 
Items With Same ILOP
Yes
No
If you select Yes, you can receive mixed pallets in RFCH for items with the same ILOP code. If you select No, you cannot receive mixed pallets in RFCH.
Use Repetitive Scan With 
ALIT Starting With Inventory
Level 1
Level 2
Level 3
Level 4
In this field, you can activate grocery style scanning in RFCH. Grocery style scanning is used when receiving product such as clothing that does not come in a standard pallet/case quantity breakdown and therefore each piece received must be individually scanned.
One scan can represent a quantity of one for that item or any other quantity that you define. AccellosOne 3PL will calculate the count automatically based on the number of pieces scanned and your setup in ALIT.
Sort Sequence Code (SOSE)
This sort sequence code allows you to define a custom sort sequence for receipt lines in RFCH. When you enter RFCH and key in a receipt number, the receipt lines will be sorted according to your SOSE code. If you leave this field blank, receipt lines in RFCH will be sorted in receipt line number order.
FIELD DESCRIPTIONS (RFCH ONLY 3)

Receiving Qty. Must be 
Less Than or Equal to 
Item Pallet Qty.
No
Yes
If you set this flag to Yes, the RF operator cannot receive oversized non-standard pallets. For example, if an item's quantity breakdown is 50 cases per pallet and the ENRE quantity for a given receipt line is 1 pallet or 50 cases, the 
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
If you set this flag to Yes, the RF operator can continue to receive a receipt line in RFCH even if inventory level validation based on SCPR fails.
Special Item Process 
Capture Mode
Capture Item Processes Before Entering Location
If you select this option, the RF operator scans any process values before entering a staging location. If you leave this field blank, the RF operator scans process values after entering a staging location.
FIELD DESCRIPTIONS (RFCH ONLY 3)

### RFCH ONLY (4) <a id="rfch-only-4"></a>

This tab shows additional RFCH options.
MRFP screen showing RFCH Only (4) tab

### RFCH SHARED <a id="rfch-shared"></a>

This tab shows options available in both RFCH and RFPU.
Always Prompt to Enter a 
Staging Location
No
Yes
If you set this flag to No, the display of the suggested staging location in the L: 
field of RFCH will be suppressed and the RF operator will be required to scan in the staging location. If you set this flag to Yes, the L: field will be populated with the suggested staging location and the RF operator is only required to press Enter to accept it.
Zero Out Receipt Lines Not Allowed 
All Users Are Allowed
Supervisors Only Are Allowed
The rules for zeroing out receipt lines in RFCH.
FIELD DESCRIPTIONS (RFCH ONLY 4)
Keep Last Location for 
One-Step Manual PutAway
Yes
No
If you set this flag to Yes, the last location for one-step manual put-away will display in RFCH. If you set this flag to No, the Location field in RFCH will always be blank when performing one-step manual put-away.
FIELD DESCRIPTIONS (RFCH ONLY 3)

RFCH Shared tab
.
FIELD DESCRIPTIONS (RFCH SHARED)
Show Default Quantity in 
RFCH/RFPU
Yes
No
RFPU Only
Variance Screen Only
If you select Yes, AccellosOne 3PL will display the received quantity of the receipt line from ENRE as the default quantity in RFCH/RFPU. You can press 
Enter to confirm it in these programs or you can enter a new quantity.
If you select No, the received quantity from ENRE will not be displayed in 
RFCH/RFPU.
If you select RFPU Only, AccellosOne 3PL will display the received quantity of the receipt line from ENRE as the default quantity in RFPU.
If you select Variance Screen Only, AccellosOne 3PL will display the received quantity of the receipt line from ENRE only on the Variance screen.

RFCH/RFPU Quantity 
Must Match ENRE Quantity
Only available for P-type receipt lines
Must match ENRE (1)
Matching not required (2)
Warn if mismatch with ENRE (3)
No warning if mismatch with ENRE (4)
Receive no more than original lines expected quantity in RFPU (5)
Must match ENRE in RFCH. No more than original line expected quantity in RFPU (6)
If you select option 1, the entered quantity in RFCH/RFPU must match the expected quantity in ENRE. If the two quantities do not match, the RF operator will not be able to process the receipt line.
If you select option 2, the entered quantity in RFCH/RFPU need NOT match the expected quantity in ENRE and a warning message is only generated when the received quantity is greater than the expected quantity.
If you select option 3, a warning message will be generated when the entered quantity in RFCH/RFPU does not match the expected quantity in ENRE, but the RF operator will be allowed to proceed.
If you select option 4, no warning message will be generated when the entered quantity in RFCH/RFPU does not match the expected quantity in 
ENRE.
If you select option 5, matching is not required in RFCH. However, the entered quantity in RFPU cannot exceed the expected quantity in ENRE.
If you select option 6, the entered quantity in RFCH must match the expected quantity in ENRE and the entered quantity in RFPU cannot exceed the expected quantity in ENRE.
Supvr. Must Authorize 
Location Overrides in 
RFCH/RFPU/RFRL
Yes
No blank = No
If you select Yes, RF operators cannot override a system-assigned put-away location without the approval of a supervisor. If you select No, RF operators can override system-assigned locations without the approval of a supervisor.
NOTE The approval of a supervisor is NOT required to override a putaway location with a staging location.
FIELD DESCRIPTIONS (RFCH SHARED)

Validate One Process 
Value
Only available for P-type receipt lines
RFPIC Only
RFCH and RFPIC
RFCH Only in Supervr. Override Mode
None
This flag allows the RF operator to validate the serial number and other information such as level 1 and 2 values in bar code labels. Validation will only occur for P-type receipt lines when the full quantity is received and all process values have been entered or scanned in.
If you set this field to RFCH Only, RFPIC Only or RFCH and RFPIC, the RF operator will be prompted to scan in one label from each pallet for validation purposes in the appropriate program. Should the label be missing or not valid, the RF operator will not be able to complete the receipt in RFCH or the order in RFPIC. 
If you set this field to RFCH Only in Supervr. Override Mode, the RF operator will be prompted to scan in one label from each pallet for validation purposes in RFCH. Should the label be missing or not valid, the RF supervisor login screen is displayed. When the supervisor logs in, he or she will be prompted to select how long to turn off process value validation: either turn off for just that pallet or for all pallets on that receipt or all pallets of that item on that receipt. 
RFCH screen showing supervisor options
If you set this flag to None, no validation of the serial number or other information on a bar code label will occur.
FIELD DESCRIPTIONS (RFCH SHARED)

Advance Receipt Header 
When Last Line Confirmed
Yes (default)
No
If you select Yes, the receipt header will be automatically confirmed when the last receipt line is confirmed in RFCH/RFPU. If you select No, the receipt header will NOT be automatically confirmed when the last receipt line is confirmed in RFCH/RFPU.
The No option allows you to add new receipt lines after all receipt lines on a receipt have been confirmed.
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
If you select No, partial pallet put-away to a reserved area is deactivated and normal put-away rules to a non-reserved area apply.
If you select Yes, partial pallet put-away to a reserved area is activated and the following logic applies:
▪ if received quantity = zero or null, halt the receiving process and send a “SEE SUPERVISOR” message to RF operator
▪ if received quantity = standard quantity breakdown, pallet is deemed to be a full pallet
▪ if received quantity < standard quantity breakdown, pallet is deemed to be a partial pallet
▪ if received quantity > standard quantity breakdown, halt the receiving process and send a “SEE SUPERVISOR” message to RF operator
If you select Yes With Allowing Over a Pallet as Full Pallet, the same logic as 
Yes will apply with the following exception:
▪ if received quantity > standard quantity breakdown, no message is generated and normal put-away continues
Receipt Confirmation 
Date in RFCH/RFPU
Receipt Date
Actual Company Date
If you select “Receipt Date”, the receipt confirmation date in RFCH/RFPU will be the receipt creation date. If you select “Actual Company Date”, the receipt confirmation date in RFCH/RFPU will be the receipt confirmation date in 
CHRF.
FIELD DESCRIPTIONS (RFCH SHARED)

## General Navigation And Look-Up Programs <a id="general-navigation-and-look-up-programs"></a>

*Manual H — RF Guide*

### Accessing RF <a id="accessing-rf"></a>

You access RF through an RF device. To access RF through an RF device, log onto Tera Term or some other terminal emulation software.

### Changing Your Company <a id="changing-your-company"></a>

The company that you are currently working in is displayed on the RF Main Menu. If you wish to change this company, you key in your new company code and press Enter.
1 Enter the RF environment.

RF Main Menu
2 Check the company code in the top left-hand side of your screen.
3 If you wish to change companies, key in your new company code and press Enter. 
4 Proceed to enter the RF program that you wish to use.

### Looking Up Inventory in RFIT <a id="looking-up-inventory-in-rfit"></a>

You look up your inventory in RFIT. For the item or items that you specify, RFIT shows the level 2, 3 and 4 values, whether the item is on hold, the location in which the item is stored and the on-hand, on-order, onreceipt and available quantities.
You can enter up to six search criteria for any given query. For example, you can specify your customer code only and RFIT will show all product belonging to that customer. If you enter your customer code and item code, RFIT will show all product for the item that you specify. If you enter customer code, item code and level 
2 value, RFIT will show all product for the level 2 value that you specify.
current company

If you enter no search criteria, RFIT will show all product in your warehouse regardless of customer.
1 Enter RFIT.

RF — Item Look-Up
2 Enter or scan in the appropriate search criteria. You can query by one or more of the parameters shown below. If you do not want to enter a parameter (for example, you want to look up all items regardless of level 2 and 3 values), press Enter to bypass the appropriate fields. You can query by one or more of the following:
▪ customer code 
NOTE You can only look up records in RFIT that have positive inventory. If you wish to look up inventory with zero balances, you must use LOEN (Look Up Inventory).
FUNCTION KEYS
Criteria Mode
F2 Eq (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria mode.
F4 Rt (Return to Main) Switch to Main Mode.
Main Mode
F1 En (Enter Criteria) Switch to Criteria Mode.
F4 Ex (Exit) Exit program.

▪ item code
▪ level 2, 3 and 4 value
▪ hold code
3 When you finish entering your search criteria, press F2 to execute your query.

RFIT screen showing three records for item A1
4 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll forward and backward through the records that matched the criteria that you specified.
5 Press F1 to perform another query or press F4 to exit.

### Looking Up Inventory by Location in RFPR <a id="looking-up-inventory-by-location-in-rfpr"></a>

You can look up inventory by either item or by location in RFPR. For each item or location that you specify, 
RFPR shows the level 2, 3 and 4 values, whether the item is on hold, the location in which the item is stored and the available, on hand, on order and replenishment quantities.
There are two types of searches that you can do in RFPR: you can search for all inventory records including plus records or you can exclude plus records from your search results. A plus record is a temporary record generated by the system when you allocate an order for a reserve logic customer. The inventory levels that are unknown at the time of allocation are indicated by a plus sign.
If you query by location code and warehouse, the search results are sorted in customer code and levels 1/2/
3/4 sequence. If you query by any other criteria, the search results are sorted in location code, inventory access code sequence.
REQUIREMENTS
GENERAL If you set the Hide Quantity in RFPR flag in COMP to Yes, the quantity fields will be suppressed for non-supervisory users. If you set this flag to No, the quantity fields in RFPR will display for all users both supervisory and non-supervisory.
1 = current record displayed
3 = number of records that met the criteria that you specified 

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
F2 QU (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria mode. 
This query retrieves all eligible inventory records including plus records.
F3 QR (Query Reserve) Excludes plus records from your search results.
F4 EX (Exit) Exit program.
If you wish to look up all inventory including plus records:
If you wish to exclude plus records in your query results:
a) Press F2 (QU). a) Press F3 (QR).

RFPR screen (record 40) showing available, on-hand, on order and replenishment quantities for location A103
The AV.Q field shows the available quantity, the OH.Q field shows the on-hand quantity, the ORD field shows the on order quantity and the REPI field shows the replenishment quantity.
4 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll forward and backward through the records that matched the criteria that you specified.
5 Press F1 to perform another query or press F4 to exit.

### Looking Up Receipts in RFIL <a id="looking-up-receipts-in-rfil"></a>

You look up your allocated unconfirmed receipts in RFIL. If the receipt is confirmed or unallocated, you cannot look it up in RFIL. There are three options in RFIL:
▪ you can look up all allocated lines on an unconfirmed receipt
▪ you can look up all lines that have been staged but not put-away (if you do not stage your product, this option is not available) 
▪ you can look up all lines that have been put-away 
RFIL shows the quantity of each receipt line in the lowest SKU. For example, if your receipt line has a quantity of two pallets and there 60 cases to a pallet, the quantity in RFIL will read 120.
FUNCTION KEYS
Results Mode
F1 AL (All) Shows all staged/put-away receipt lines.
F2 RC (Received) Shows all receipt lines that have been staged but not put-away.
F3 PU (Put-Away) Shows all receipt lines that have been putaway but not confirmed.

1 Enter RFIL.

RF — RF Receipt Line Look-Up
2 Key in your receipt number and press Enter.
3 Press F1 (All) to display the first receipt line on the receipt.

Receipt 1204 showing line 1 of a five-line receipt
4 Use your arrow keys to scroll forward and backward to view each receipt line.
5 If you stage your product before you put it away, press F2 (Receiving) to view product that has been staged but not put-away.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F4 EX (Exit) Exit program.
FUNCTION KEYS
1 = current line displayed
5 = total number of lines on receipt

RFIL screen showing two lines of staged product
6 If you have multiple lines of staged product, use your arrow keys to scroll forward and backward to view each line.
7 Press F3 (Put-Away) to view product that has been put-away.

RFIL screen showing three lines of product that have been put away
8 If you have multiple lines of product that have been put-away, use your arrow keys to scroll forward and backward to view each line.
9 When you finish looking up your receipt, press F4 the required number of times to exit.

### Looking Up Allocated Order Lines in RFOL <a id="looking-up-allocated-order-lines-in-rfol"></a>

You look up your allocated unconfirmed order lines in RFOL. If the order line is confirmed, you cannot look it up in RFOL. For each order line that you look up, RFOL shows the order number, customer code, line number, warehouse code, location type, up to four inventory levels, hold code (if any), quantity, location and 
OPID (if any). Locations with a quantity of zero are not shown.
There are three options in RFOL:

▪ you can look up all unconfirmed order lines (that is, the order is either allocated or picked)
▪ you can look up unconfirmed order lines that have been allocated but not picked 
▪ you can look up unconfirmed order lines that have been picked
Order line records in RFOL are sorted by order number followed by location code.
1 Enter RFOL.

RF — Order Line Look-Up
NOTE The allocated and picked options in RFOL always show the allocated and picked lines for the currently selected order. If you wish to look up all allocated or picked lines regardless of order, you must start a new query. You cannot query on all allocated or picked lines if there is an order displayed on your screen.
FUNCTION KEYS
Results Mode
F1 AL (All) Shows all order lines that have been either allocated or picked.
F2 AO (Allocated) Shows all order lines that have been allocated but not picked.
F3 PI (Picked) Shows all order lines that have been picked but not confirmed.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F4 EX (Exit) Exit program.

2 Enter or scan in the appropriate search criteria. You can query by one or more of the parameters shown below. If you do not want to enter a parameter (for example, you want to look up all orders regardless of warehouse), press Enter to bypass the field.
▪ order number 
▪ warehouse code
▪ location type code
3 After pressing Enter in the Location Type field, press F1 (All) to display the first order line on the first order. 

Order Line Look-Up showing ALL option
4 Use your arrow keys to scroll forward and backward to view each order line on each unconfirmed order.
5 Press F2 (Allocated) to view the order lines for the currently selected order that have been allocated.

Order Line Look-Up showing allocated lines for order 1512
6 Use your arrow keys to scroll forward and backward to view each order line that has been allocated.
7 Press F3 (Picked) to view the order lines of the currently selected order that have been picked.
1 = current record displayed
133 = total number of order lines for all unconfirmed orders
There are two allocated lines for order 

Order Line Look-Up showing picked lines for order 1528
8 When you finish viewing your orders, press F4 the required number of times to exit.

### Looking Up Inventory in RFLOIP <a id="looking-up-inventory-in-rfloip"></a>

This program allows you to look up inventory information by scanning in a serial number from a bar code label. For each serial number, RFLOIP shows the customer code, up to four inventory levels, the warehouse and location, and the on-hand and available quantities. You can scan in the entire bar code label or you can manually key only the serial number portion of the bar code. 
You cannot look up serial numbers if the product is on a confirmed order.
1 Enter RFLOIP.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria mode.
F4 RT (Return to Main) Switch to Main Mode.
Main Mode
F1 EN (Enter Criteria) Switch to Criteria Mode.
F4 EX (Exit) Exit program.
There are three lines that have been picked for order 1528

RF — Look Up Item Process
2 Enter or scan in your serial number.

RF — Look Up Item Process showing inventory information for serial number 0001
3 If your query resulted in multiple records being retrieved from the database, use your arrow keys to scroll forward and backward through the records that matched the criteria that you specified.
4 Press F1 to perform another query or press F4 to exit.

### Looking Up Locations in LOLORF <a id="looking-up-locations-in-lolorf"></a>

This RF look-up program is similar to the non-RF program LOLO (Look Up Location Information). It is designed to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to AccellosOne 3PL’s location information. 
Refer to the Operations 1 Guide for detailed information on LOLO.
1 Enter LOLORF.

RF - Look Up Location
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the location(s) that you selected, press F3 (Inventory Block) to see the inventory in the location(s).

RF - Look Up Location
4 When you finish looking up; your location, press F4 (Location) and then F4 (Exit).

### Looking Up Inventory in LOENRF <a id="looking-up-inventory-in-loenrf"></a>

This RF look-up program is similar to the non-RF program LOEN (Look Up Entity Information). It is designed to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to AccellosOne 3PL’s location information. 
Refer to the Operations 1 Guide for detailed information on LOEN.
1 Enter LOENRF.

RF - Look Up Entity Information
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the inventory that you selected, press F3 (Location Block) to see the inventory in the location(s).

RF - Look Up Entity Information
4 When you finish looking up your inventory, press F4 (Inventory) and then F4 (Exit).

### Looking Up Receipts in LORERF <a id="looking-up-receipts-in-lorerf"></a>

This RF look-up program is similar to the non-RF program LORE (Look Up Receipts). It is designed to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to 
AccellosOne 3PL’s receipt information. 
Refer to the Operations 1 Guide for detailed information on LORE.
1 Enter LORERF.

RF - Look Up Receipts
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the receipts that you selected, press F3 (Line Block) to see the receipt lines.

RF - Look Up Receipts
4 When you finish looking up your receipts, press F4 (Receipt Block) and then F4 (Exit).

### Looking Up Orders in LOORRF <a id="looking-up-orders-in-loorrf"></a>

This RF look-up program is similar to the non-RF program LOOR (Look Up Orders). It is designed to be viewed on a truck-mounted RF device with a wider screen and allows warehouse personnel full access to 
AccellosOne 3PL’s order information. 
Refer to the Operations 1 Guide for detailed information on LOOR.
1 Enter LOORRF.

RF - Look Up Orders
2 Key in your search criteria and press F2 (Execute Query).
3 When AccellosOne 3PL retrieves the orders that you selected, press F3 (Line Block) to see the order lines.

RF - Look Up Orders
4 When you finish looking up orders, press F4 (Order Block) and then F4 (Exit).

### Looking Up Reserve Logic Customers in RFLR <a id="looking-up-reserve-logic-customers-in-rflr"></a>

You look up inventory by location for reserve logic customers in RFLR. For each location that you specify, 
RFLR shows the on-hand, on order replenishment and available quantities at the inventory level that the customer reserves at. For example, if a three-level customer reserves at level 2 (lot number), RFLR will show quantities for each unique lot in a given location.
Locations in which the available quantity is less than or equal to zero are not shown and inventory on hold is not included in the location quantities.
If your query retrieves multiple locations, locations are sorted by the expiry date of product in the location.
FUNCTION KEYS
Criteria Mode
F2 Eq (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria mode.
F4 Ex (Exit) Exit program.
Main Mode
F1 En (Enter Criteria) Switch to Criteria Mode.

1 Enter RFLR.
RF — Look Up Reserve Logic Customer
2 Key in your level 1 value and press Enter. If two customers have the same item code, a pick list will display. Use your arrow keys to position the cursor over the item code that you wish to look up and press 
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

## Miscellaneous Processing <a id="miscellaneous-processing"></a>

*Manual H — RF Guide*

### Relocating Inventory in RFRL <a id="relocating-inventory-in-rfrl"></a>

You relocate inventory from one location to another in RFRL. The locations that you specify in a relocate can be within the same warehouse or belong to different warehouses. You cannot relocate inventory if it is on order or on receipt.
The following restrictions apply to RFRL:
▪ You cannot relocate product that is on an open order or receipt.
▪ If the Location Capacity Validation Type field in COMP (Company Code) is set to “No validation for userinitiated transactions”, relocating inventory does not take into account the location’s capacity. You can move inventory into a location that is considered “full”.
▪ If the product is on non-breakable hold, you must relocate all product in the location; you cannot relocate partial quantities.
If you wish to relocate product to a pick line location, you must set the Validation Rules for Relocate to Pick 
Line flag in MRFP to either 2 (Allow operator to proceed) or 3 (Omit validation of location).
REQUIREMENTS
ALLOCATION If you want AccellosOne 3PL to select the best possible to location for a relocation based on your directed move stock parameters in ILOP, you must set the 
Allow Directed Move in RF Relocate flag in MRFP to Yes.
See the Allocation and Wave Manager Guide for further information on setting up directed moves.
OTHER If you want the operator to be forced to validate the from location in a relocation, you must set the Picklist Rules in RF Relocate flag in MRFP to the appropriate value.
If you want relocation quantity to be displayed, you must set the Display From 
Relocation Quantity in RF Relocate flag in MRFP to Yes.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria Mode.
F3 CQ (Count Query) Counts the number of records that meet the criteria that you specify in Criteria 
Mode.

### RELOCATING INVENTORY (OPERATOR SELECTS TO LOCATION) <a id="relocating-inventory-operator-selects-to-location"></a>

1 Enter RFRL.

RF — Relocate
F4 RM (Return to Main) Switch to Main Mode.
Results Mode
F1 EC (Enter Criteria) Switch to Criteria Mode.
F3 LB (Location Block) Positions your cursor in the From Location field after pressing F4 (IN) to position your cursor in the Customer field.
F3 PR (Process Relocate) Performs the relocation.
F4 IN (Inventory) Positions your cursor in the Customer field so that you can scroll through the list of records retrieved in your query.
F4 EX (Exit) Exit program.
F9 Move cursor to previous field.
FUNCTION KEYS

2 Do one of the following:
3 The system will display the number of inventory records that meet the level 1, 2, 3 and 4 criteria that you specified.

RFRL screen showing one record for item A2, lot 101
If you wish to query by UI value:
If you wish to query by inventory level:
a) Key in your UI value and press 
Enter.
a) Enter or scan in your customer code.
b) Enter or scan in your item code.
c) If required, enter or scan in your level 2, 3 and 4 values.
d) Press F2 to query.
Number of records for this inventory entity

RFRL screen showing prompt for quantity
If you know your from location:
If you do NOT know your from location:
a) Key in your from location and press Enter.
a) Press F10 to enter the pick list, then F2 to perform your query.
▪ AccellosOne 3PL will display all locations containing the product that you specified. 
RFRL screen showing available locations
b) Use your arrow keys to position your cursor beside the location containing the product that you wish to move.
c) Press F3 to select the location. 
The system will return you to the main RFRL screen.

4 Do one of the following:
5 Enter or scan in your to location.
6 If required, enter or scan in your to warehouse.
7 Press F3 to process the relocate.
8 Perform another relocate or press F4 the required number of times to exit. 

### RELOCATING INVENTORY (DIRECTED MOVE SYSTEM ACTIVATED) <a id="relocating-inventory-directed-move-system-activated"></a>

There are three options for overriding the system-assigned location for a relocation depending on your setup in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to No, an operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to Yes, changing a location must be approved by a supervisor
▪ if the Max. Number of F3 (NX) Allowed Per ILOP Sequence in RFRLflag in MRFP is activated, an operator can select an alternative suggested relocate location
1 Enter RFRL.

RF — Relocate
If the QTY field is populated: If the QTY field is blank:
a) If you wish to relocate all product in the location, proceed to the next step. If you wish to relocate a portion of the product in the location, press F9 to position your cursor in the QTY field. 
Then key in your relocation quantity and press Enter.
a) Key in the quantity that you wish to relocate and press Enter.

2 Do one of the following:
3 The system will display the number of inventory records that meet the level 1, 2, 3 and 4 criteria that you specified.

RFRL screen showing six records for item A2, lot 101
If you wish to query by UI value:
If you wish to query by inventory level:
a) Key in your UI value and press 
Enter.
a) Enter or scan in your customer code.
b) Enter or scan in your item code.
c) If required, enter or scan in your level 2, 3 and 4 values.
d) Press F2 to query.
Number of records for this inventory entity

RFRL screen showing prompt for quantity
If you know your from location:
If you do NOT know your from location:
a) Key in your from location and press Enter.
a) Press F10 to enter the pick list, then F2 to perform your query.
▪ AccellosOne 3PL will display all locations containing the product that you specified. 
RFRL screen showing available locations
b) Use your arrow keys to position your cursor beside the location containing the product that you wish to move.
c) Press F3 to select the location. 
The system will return you to the main RFRL screen.

4 Do one of the following:

RFRL screen showing location assigned by system
If the QTY field is populated: If the QTY field is blank:
a) If you wish to relocate all product in the location, proceed to the next step. If you wish to relocate a portion of the product in the location, press F9 to position your cursor in the QTY field. 
Then key in your relocation quantity and press Enter.
a) Key in the quantity that you wish to relocate and press Enter.

5 Do one of the following:
6 Press F3 to process the relocate.
7 Perform another relocate or press F4 the required number of times to exit. 
If you accept the systemassigned location:If you wish to change the system-assigned location:
If you wish to select an alternative system-assigned location:
a) Scan in your location to confirm it.a) Key in a new location for the relocated product and press 
Enter. The following message will appear: 
b) Key in Y for Yes and press 
Enter to proceed with the location override. If you do not wish to proceed with the override, key in N for No and press Enter to return to the main RFRL screen.
c) If you enter Y for Yes to proceed with the relocation and if a supervisor’s authorization is required to override the location, the following screen will appear:

d) Have a supervisor log in to approve the location override.
a) Press F3 (NX) to display a second suggested put-away location. If the second suggested put-away location is not acceptable, press F3 (NX) again to see a third suggested put-away location.
b) Press Enter again to accept the warehouse that the system-assigned location belongs to.

### Performing Multi-Pallet Moves <a id="performing-multi-pallet-moves"></a>

Multi-pallet moves allow you to stage, put-away, pick, relocate and replenish multiple pallets in a single step; 
that is, you scan two or more UI’s but only enter/scan the to location once. Multi-pallet moves are supported in the following programs: RFCH, RFPU, RFPIC, RFRL, RFRP and RFST.
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

RFPIC screen showing prompt to pick next pallet
7 When the pick next pallet prompt appears, do one of the following:
8 Repeat steps 2 to 5 for each additional pallet that you wish to move.
9 When the maximum capacity for the equipment type is reached, the following message will appear:
RFPIC screen showing prompt to go to staging (current count = maximum for equipment type)
10 Press Enter to continue.
11 Continue normal processing for RFCH, RFPU, RFPIC, etc.
To cancel multi-pallet move mode:
To continue in multi-pallet move mode:
a) Key in N (Go to Staging) and press Enter.
b) Stage, put-away or move the current pallet before working on the next pallet.
a) Key in Y (Pick Pallet) and press 
Enter.
b) Proceed to next step.
the maximum capacity for the equipment type = 2 pallets the current pallet being worked on

### Adjusting Non-Serial Number Inventory in RFAJ <a id="adjusting-non-serial-number-inventory-in-rfaj"></a>

You can adjust in and adjust out non-serial number inventory in RFAJ without the need to enter ENAJ (Enter 
Adjustment). In RFAJ you can perform most of the functions supported in ENAJ including: 
▪ querying by any inventory level
▪ entering positive and negative adjustments for existing inventory
▪ creating new inventory 
When adjusting existing inventory, you can enter either partial or full amounts of an inventory entity. When creating new inventory, you can specify a hold code, enter a variable quantity breakdown (if this feature is activated in ITEM) and enter an expiry date (if expiry date entry is activated in ITSH).
RFAJ does not support adjustment transfers, changes to an item’s quantity breakdown or changes to a level 
2/3/4 description. These functions must be performed in ENAJ.

### ADJUSTING OUT EXISTING INVENTORY <a id="adjusting-out-existing-inventory"></a>

1 Enter RFAJ.
FUNCTION KEYS
Main Mode
F2 QU (Query) Allows you to query inventory.
F4 EX (Exit) Exit program.
Results Mode
F1 HD (Hold) Places product on hold.
F2 CM (Change Mode) Allows you to switch modes; from adjust in to adjust out and vice versa.
F3 PR (Process) Processes the adjustment.
F4 RT (Return to Main) Switch to Main Mode.
F9 Move cursor to previous field.

RFAJ screen
2 Enter your UI or inventory levels and press Enter. If the same inventory is found in multiple locations, you must enter or scan in your location.
If you do not know the UI or inventory levels of the inventory that you wish to adjust out, press Enter twice to position your cursor in the L1 field. Then enter the inventory level(s) that you know and press F2 (QU). 
When AccellosOne 3PL retrieves the list of query results, use your up and down arrow keys to scroll through the list.
RFAJ screen showing adjust out mode
3 If the inventory has been assigned multiple locations, use your up and down arrow keys to find the location that you want to adjust out. The press Enter to accept it.
4 Enter or scan in your location.
5 Key in your adjust out quantity as a negative (for example, -1 or 
-1PLT) and press Enter. If the item has multiple SKU’s in its quantity breakdown and you do not specify 
a SKU, AccellosOne 3PL will use the item’s lowest SKU.

RFAJ screen showing adjust out quantity
6 Press F3 (PR) to process the adjustment.
7 Press F4 (EX) to exit.

### ADJUSTING IN NEW INVENTORY <a id="adjusting-in-new-inventory"></a>

New inventory is inventory that has never been received in the warehouse before. That is, at least one of the item’s inventory levels is new.
1 Enter RFAJ.
RFAJ screen
2 Press Enter to bypass the UI field.
3 Enter or scan in your location.
4 Enter or scan in your item. If the same item is attached to two or more customers, press F3 (SL) to select the appropriate customer/item from the pick list.

RFAJ screen showing prompt for level 2 value
5 Enter the remaining inventory levels of the inventory that you wish to adjust in.
RFAJ screen showing prompt to process
6 If you wish to place the adjust in inventory on hold, press F1 (HD). Then key in your hold code and press 
Enter.
7 Press F3 (PR) to process.
RFAJ screen showing prompt for location

8 Enter or scan in your location.
RFAJ screen showing prompt for adjustment quantity
9 Key in your adjust in quantity (for example, 1 or 1PLT) and press Enter. If the item has multiple SKU’s in its quantity breakdown and you do not specify a SKU, AccellosOne 3PL will use the item’s lowest SKU.
If the location that you enter does NOT match the location in step 3:
If the location that you enter does match the location in step 
3:
a) The following message will appear:
Prompt to accept change in location
b) If the location is correct, key in Y for Yes and press Enter to accept it. Otherwise, press Enter to reject it.
a) Proceed to next step.

RFAJ screen showing adjustment in quantity
10 Press F3 (PR) to process the adjustment.
11 Do one of the following:
12 Press F4 (RT) and F4 (EX).
If manual entry of expiry dates is activated for the item:
If manual entry of expiry dates is 
NOT activated for the item:
a) The following window will appear:
b) Key in your expiry date in the format displayed on your screen and press Enter.
c) If the expiry date is correct, key in Y for Yes and press Enter. 
Otherwise, press Enter to return to the date screen and re-enter it.
a) Proceed to next step.

### ADJUSTING IN EXISTING INVENTORY <a id="adjusting-in-existing-inventory"></a>

If the inventory that you wish to adjust in is already in the warehouse, you must change your mode from “adjust out” to “adjust in”.
1 Enter RFAJ.
RFAJ screen
2 Press Enter to bypass the UI field.
3 Enter or scan in your item. If the same item is attached to two or more customers, press F3 (SL) to select the appropriate customer/item from the pick list.
RFAJ screen showing prompt for level 2 value
4 Enter the remaining inventory levels of the inventory that you wish to adjust in.
RFAJ screen showing adjust out mode

5 Press F2 (CM).
RFAJ screen showing prompt to adjust in inventory
6 Key in Y for Yes and press Enter.
7 If you wish to place the adjust in inventory on hold, press F1 (HD). Then key in your hold code and press 
Enter.
8 Press F3 (PR) to process.
RFAJ screen showing prompt for location
9 Enter or scan in your location.
RFAJ screen showing prompt for adjustment quantity
10 If the location that you entered in the previous step does not match the location in step 3, the following message will display:

RFAJ screen showing prompt to accept change in location
If the location is correct, key in Y for Yes and press Enter to accept it. Otherwise, press Enter to reject it.
11 Key in your adjust in quantity (for example, 1 or 1PLT) and press Enter. If the item has multiple SKU’s in its quantity breakdown and you do not specify a SKU, AccellosOne 3PL will use the item’s lowest SKU.
RFAJ screen showing adjustment in quantity
12 Press F3 (PR) to process the adjustment.
13 Press F4 (RT) and F4 (EX).

### ADJUSTING IN INVENTORY WITH A VARIABLE QUANTITY BREAKDOWN <a id="adjusting-in-inventory-with-a-variable-quantity-breakdown"></a>

If you are adjusting in inventory with a variable quantity breakdown, you will be prompted to enter the quantity breakdown. You can either press Enter to accept the system default or key in a new quantity breakdown and press Enter.
RFAJ screen showing prompt for adjusting quantity breakdown

### Adjusting Serial Number Inventory in RFAJB <a id="adjusting-serial-number-inventory-in-rfajb"></a>

You can adjust in and adjust out serial number inventory in RFAJB. RFAJB performs the adjustment to inventory and the bar code validation at same time. It can only be used with unique serial numbers.
You can adjust in inventory when the serial number has never been received or is on a confirmed order. If required, adjusted in inventory can be placed on hold. You can adjust out inventory when the serial number has been received and is not picked. If a case is on a full pallet and all cases are available, you can adjust out a full pallet by scanning in a single case.
RFAJB can also recover from a lost connection. When a connection is dropped, you can either finish the current transaction or continue to adjust in or adjust out more cases.
REQUIREMENTS
INVENTORY LEVELSRFAJB requires a three-level account.
PROCESS VALUESYou require two process values: one for catch weights and one for serial numbers. These codes must be set up in IPRO (Item Process) as follows:
Transfer Value to Inventory = Yes
Create Automatic Records = Yes
Allow Duplicates = Yes for your catch weight value and No for your serial number value
Then attach your process values to a profile in IPRP (Item Process Profile). The 
IPRP profile must in turn be attached to the item(s) requiring the process values.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEYou need a scan parameter profile defined in SCPR (Scan Parameter Code). 
This profile must contain a minimum of three records in the Detail Block: one record for your scanned in weight, a second record for your scanned in serial number and a third record for your scanned in inventory level 1 value. The SCPR profile must in turn be attached to the item requiring the process values.
BAR CODE PROFILEYou must define a bar code profile in BAPR and attach to it the scan parameter code that you set up in SCPR.
OTHER You need a default adjustment code in ATMP (Action Template Setup) for each company/customer combination. If a single default adjustment code for all customers in all companies, you can use the .ALL codes for both customer and company.

### ADJUSTING IN INVENTORY <a id="adjusting-in-inventory"></a>

You can adjust in inventory when the serial number has never been received or the product is on a confirmed order.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in your bar code of the first case to adjust in.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile and press F3 (SL) to select it.
FUNCTION KEYS
All Modes
F1 PLT (Pallet) Allows you to adjust out a full pallet.
F2 RM (Remove) Allows you to remove a previously scanned case.
F2 HD (Hold) Places product on hold.
F3 PR (Process) Displays the quantity validation screen.
F4 EX (Exit) Exit program.
F4 RT (Return to Main) Switch to Main Mode.
F9 Move cursor to previous field.

RFAJB screen showing adjust in message
5 Repeat the above step for each additional case that you wish to adjust in.
6 If you make a mistake and wish to “unscan” a scanned case, press F2 (RM). Then rescan the case to be removed from the adjustment.
7 When you finish scanning the cases to be adjusted in, press F3 (PR).

RFAJB screen showing quantity validation 
8 Key in the number of cases to be adjusted in and press Enter.
9 Enter or scan in your level 2/3/4 values. If you wish to apply a hold code to the new inventory, press F2 (HL) before entering you lowest inventory level. Then key in your hold code and press Enter. Lastly, enter your remaining inventory levels.
10 If the adjusted in inventory has already been received, the following message will appear.

RFAJB screen showing warning that serial number has already been received 

11 Do one of the following:
12 Press F4 to exit.

### ADJUSTING OUT CASES <a id="adjusting-out-cases"></a>

You can adjust out cases if the serial number has been received and is not picked.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in your bar code of the first case to adjust out.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile and press F3 (SL) to select it.

RFAJB screen showing adjust out message
5 Repeat the above step for each additional case that you wish to adjust out.
If you accept the re-received inventory:
If you reject the re-received inventory:
a) Key in 1 and press Enter. a) Key in 2 and press Enter.
b) Re-enter the required inventory level.

6 If you make a mistake and wish to “unscan” a scanned case, press F2 (RM). Then rescan the case to be removed from the adjustment.
7 When you finish scanning the cases to be adjusted out, press F3 (PR).

RFAJB screen showing quantity validation
8 Key in the number of cases to be adjusted out and press Enter.
9 Press F4 to exit.

### ADJUSTING OUT FULL PALLETS <a id="adjusting-out-full-pallets"></a>

You can adjust out full pallets if the serial number has been received, all cases are available and no cases have been picked.
1 Enter RFAJB.

RFAJB screen
2 Enter or scan in your location.
3 Enter or scan in the bar code of any case on the pallet.
4 If there are multiple bar code profile codes for the inventory, position your cursor over the correct profile and press F3 (SL) to select it.

RFAJB screen showing adjust out message
5 Press F1 (PLT).

RFAJB screen showing confirmation prompt
6 Key in Y for Yes and press Enter.
7 Press F3 (PR).

RFAJB screen showing quantity validation
8 Key in the total number of cases on the pallet and press Enter.
9 Press F4 to exit.

### ADJUSTING OUT CASES USING THE REMOVE COMMAND <a id="adjusting-out-cases-using-the-remove-command"></a>

If you wish to adjust out the majority of cases on a pallet (for example, a pallet holds 50 cases and you wish to adjust out 45), you can use the Remove command. The Remove command allows you to scan in only the cases NOT to be adjusted out rather than each case to be adjusted out.
1 Enter RFAJB.

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

RFAJB screen showing quantity validation
10 Key in the total number of cases being adjusted out — that is, the number of cases on the pallet that you did NOT scan — and press Enter.
For example, if your pallet quantity breakdown is 20 cases per pallet and you use the Remove command to remove five cases, your adjust out quantity will be 15 (20 -5).
11 Press F4 to exit.

### RECOVERING FROM A LOST CONNECTION <a id="recovering-from-a-lost-connection"></a>

If you lose your RF connection and re-enter RFAJB, you will be prompted to either finish the existing adjustment or continue to add more cases to your adjustment in/adjustment out.
1 Enter RFAJB.

RFAJB screen showing lost connection message
2 Do one of the following:
If you wish to finish the existing adjustment:
If you wish to add more cases to your adjustment:
a) Key in 1 and press Enter.
b) Press F3 (PR) to confirm the count.
c) Complete the adjustment in the normal manner.
a) Key in 2 and press Enter.
b) Continue to add new cases.
c) Complete the adjustment in the normal manner.

### Merging Inventory in RFMI <a id="merging-inventory-in-rfmi"></a>

You can merge and transfer inventory entities in RFMI. You use RFMI when you wish to consolidate two partial pallets into a single PID or you wish to correct an incorrect inventory level. For example, you received product under lot number 101, which is wrong, and you want to transfer the product to lot number 102, which is the correct lot number. Lot 102 can be either an existing lot number or a new lot number created by the operator in RFMI.
The following requirements must be met before you can merge/transfer inventory in RFMI:
▪ the product belongs to the same customer
▪ the customer is billed at the lowest inventory level in DILP
▪ the product is NOT on an open order or receipt
If you have assigned process values to your product and if you are merging or transferring a full pallet, no scanning of process values is required as the values are transferred automatically. If, however, you are working with less than a full pallet, process values must be individually scanned.
REQUIREMENTS
SCAN PARAMETER CODEIf you use process values to capture catch weights and serial numbers, you need a scan parameter profile defined in SCPR (Scan Parameter Code). This profile must contain a minimum of three records in the Detail Block: one record for your scanned in weight, a second record for your scanned in serial number and a third record for your scanned in inventory level 1 value. The SCPR profile must in turn be attached to the item requiring the process values.
INVENTORY LEVELSYou can merge inventory entities at inventory levels other than the lowest (PID) 
by setting the Allow Merging Up To Level (RFMG) field in MRFP to the appropriate value: Level 1, Level 2 or Level 3.
INVENTORY 
ATTRIBUTES
If your inventory entities have inventory attributes set up in IAPR (Inventory Attributes Profile Code), you cannot perform a merge unless there is an exact match of attributes (you can deactivate this condition by selecting the Allow RF Merge flag in IAPR).
VARIABLE QUANTITY BREAKDOWN 
INVENTORY
The Base for Cube/Weight flag in ITEM must be set to Y for Yes for the lowest 
SKU.
OTHER You need a default adjustment code in ATMP (Action Template Setup) for each company/customer combination. If a single default adjustment code applies to all customers in all companies, you can use the .ALL codes for both customer and company.

### MERGING EXISTING INVENTORY ENTITIES <a id="merging-existing-inventory-entities"></a>

When you merge two existing inventory entities, AccellosOne 3PL will apply the following logic to renewal storage and expiry calculations:
▪ billing will use the oldest date as the next renewal date
▪ the oldest expiry date will be assumed for the merged inventory
1 Enter RFMI.
ATMP screen showing default adjustment code for all companies and customers
REQUIREMENTS

RFMI screen
2 Do one of the following:
RFMI screen showing adjust in inventory
3 Press F3 (PR) to display the adjust out screen.
If you know the UI of the adjust in inventory:
If you do NOT know the UI value of the adjust in inventory:
a) Enter or scan in the UI of your adjust in inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 101 will be your adjust in inventory.
c) If the UI that you entered exists in multiple locations, key in your location code and press Enter.
a) Press Enter to bypass the UI field.
b) Key in the location code and/or inventory levels of your adjust in inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 101 will be your adjust in inventory.
d) If AccellosOne 3PL retrieves multiple inventory records, use your arrow keys to select the inventory entity that you wish to transfer in.

RFMI screen showing adjust out screen
4 Do one of the following:
RFMI screen showing adjust out screen
5 If the inventory entity that you entered in the previous step is found in multiple locations, use your arrow keys to select the correct record.
6 Key in your adjustment quantity as a negative value and press Enter.
If you know the UI of the adjust out inventory:
If you do NOT know the UI value of the adjust out inventory:
a) Enter or scan in the UI of your adjust out inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 102 will be your adjust out inventory.
c) If the UI that you entered exists in multiple locations, key in your location code and press Enter.
a) Press Enter to bypass the UI field.
b) Key in the location code and/or inventory levels of your adjust out inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 102 will be your adjust out inventory.
d) If AccellosOne 3PL retrieves multiple inventory records, use your arrow keys to select the inventory entity that you wish to transfer out.

RFMI screen showing adjust out quantity of -3C
7 Press F3 (PR) to process the adjustment.
RFMI screen showing prompt for total number of cases
8 If you want to place the merged inventory on hold, press F9 to position your cursor in the H field. Then key in your hold code and press Enter.
9 Key in the total number of cases and press Enter. For example, if you are merging 5 cases of pallet ID 
101 with 10 cases of pallet ID, your total number of cases will be 15 (5 + 10). 
10 Press F4 (EX) to exit.

### CREATING NEW INVENTORY ENTITIES <a id="creating-new-inventory-entities"></a>

You can transfer an existing inventory entity to a new entity created in RFMI.
1 Enter RFMI.

RFMI screen
2 Enter or scan in the UI of your new inventory entity.
RFMI screen showing adjust in inventory
3 Press F3 (PR) to display the adjust out screen.
RFMI screen showing adjust out screen

4 Do one of the following:
RFMI screen showing adjust out screen
5 Key in your adjustment quantity as a negative value and press Enter.
RFMI screen showing adjust out quantity of -1 PLT 3 CASE
6 Press F3 (PR) to process the adjustment.
If you know the UI of the adjust out inventory:
If you do NOT know the UI value of the adjust out inventory:
a) Enter or scan in the UI of your adjust out inventory. 
b) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 102 will be your adjust out inventory.
c) If the UI that you entered exists in multiple locations, key in your location code and press Enter.
a) Press Enter to bypass the UI field.
b) Key in the location code and/or inventory levels of your adjust out inventory and press F2 (QU).
c) For example, if you are transferring pallet ID 102 to pallet ID 101, pallet ID 102 will be your adjust out inventory.
d) If AccellosOne 3PL retrieves multiple inventory records, use your arrow keys to select the inventory entity that you wish to transfer out.

RFMI screen showing prompt for total number of cases
7 If you want to place the new inventory on hold, press F9 to position your cursor in the H field. Then key in your hold code and press Enter.
8 Enter or scan in the location of the new inventory. 
9 Press F4 (EX) to exit.

### Adding Extra Charges to a Receipt/Order in RFEC <a id="adding-extra-charges-to-a-receipt-order-in-rfec"></a>

If RF entry of extra charges is activated in ECHP, you can add extra charges to receipts or orders in the standalone program RFEC. You can also add extra charges to receipts or order in RFCH (receipts only) or RFPIC (orders only).
The entry of extra charges in RFEC/RFCH/RFPIC is strictly optional. You can press F4 at any time to exit the program without entering an extra charge.
There are two possible scenarios for extra charge entry in RFEC: you can select your extra charge(s) from a predefined list or you can manually enter them. 
There are two flags in ECHP that govern extra charge entry in RF: Allow RF Entry and Allow Override of 
Charge Quantity in RF. If both flags are set to N for No, extra charge entry in RF is deactivated.

### SCENARIO 1 — RF OPERATOR ENTERS CHARGE QUANTITY ONLY <a id="scenario-1-rf-operator-enters-charge-quantity-only"></a>

Allow RF Entry (ECHP) = No
Allow Override of Charge Quantity in RF (ECHP) = Yes
REQUIREMENTS — GENERAL
FLOWS The receipt or order must be at the flow set up for extra charge entry in ECHP. If the Flow Process Code (FLPR) for RF field in ECHP is blank, you can add extra charges to a receipt or order at any flow.
OTHER See [Extra Charge Setup for RF](picking-rf.html#extra-charge-setup-for-rf)

In this scenario, the RF operator can select one or more extra charges from a predefined list and can enter any charge quantity for the selected charge(s).
1 Enter RFEC.
RFEC screen
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
RFEC screen showing two possible extra charges
4 If you change your mind and do not wish to add an extra charge to the receipt or order, press F4 (RT) and 
F4 (EX) to exit RFEC.
5 If there are multiple extra charges in RFEC, use your arrow keys to scroll up and down the list until you find the extra charge that you wish to add.
6 Key in your charge quantity and press Enter. A charge quantity of zero means no extra charge for the receipt or order.

RFEC screen showing prompt to confirm the change to the charge quantity
7 Do one of the following:
8 Repeat the previous steps for each additional extra charge that you wish to add to the receipt or order.
9 When you finish adding your extra charges, press F4 (RT) and F4 (EX) to exit.

### SCENARIO 2 — RF OPERATOR ENTERS CHARGE CODE AND QUANTITY <a id="scenario-2-rf-operator-enters-charge-code-and-quantity"></a>

Allow RF Entry (ECHP) = Yes
Allow Override of Charge Quantity in RF (ECHP) = Yes
In this scenario, the RF operator must manually enter his or her extra charges (if any) and can enter any charge quantity for the entered charges.
1 Enter RFEC.
RFEC screen
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
If you wish to confirm the change to the charge quantity:
If you wish to cancel your change:
a) Key in Y for Yes and press Enter. a) Press Enter to accept the default value of No.

RFEC screen showing prompt to enter RF extra charges
4 Do one of the following:
RFEC screen showing prompt to enter charge
5 Key in your charge code and press Enter.
If you wish to add an extra charge:
If you do NOT wish to add an extra charge:
a) Press Enter to continue.
b) Proceed to next step.
a) Key in N for No to exit.
b) END OF PROCEDURE

RFEC screen showing prompt to enter charge quantity
6 Key in your charge quantity and press Enter. If you press Enter to accept the default quantity of zero, no extra charge will be created for the receipt or order.
7 Repeat the previous steps for each additional extra charge that you wish to add to the receipt or order.
8 When “RF Charges Completed” message appears, press Enter to acknowledge it.
9 Press F4 (EX) to exit.

### DELETING AN EXTRA CHARGE <a id="deleting-an-extra-charge"></a>

You delete an extra charge in RFEC by setting its charge quantity to zero. The following conditions must be met before you can perform a deletion:
▪ the receipt or order’s flow has not been advanced
▪ the Allow Override of Charge Quantity in RF flag in ECHP has been set to Yes
1 Enter RFEC.
2 Key in I for Inbound or O for Outbound and press Enter.
3 Key in your document number and press Enter.
4 If there are multiple extra charges in RFEC, use your arrow keys to scroll up and down the list until you find the extra charge that you wish to delete.
5 In the QTY field, key in zero and press Enter.
6 When prompted to confirm the change to the charge quantity, key in Y for Yes and press Enter.
7 Press F4 (RT) and F4 (EX) to exit.

### Assigning Check Digits to Locations in RFCD <a id="assigning-check-digits-to-locations-in-rfcd"></a>

You can define check digits for your locations and require RF operators to scan in this check digit from a label attached to the location whenever they work in RFRL, RFPU, RFPIC and RFRP. The purpose of check digit scanning is to ensure that the RF operator physically went to the location to scan it rather than manually entering any location at the dock. 

You can use the program RFCD (RF Check Digit) to assign a check digit to an individual location or to a range of locations. If your locations already have check digits, you can use RFCD to update them.
You use the “%” character as a wildcard when you wish to update a range of locations.
1 Enter RFCD.
RFCD screen
2 Do one of the following:
TIP You can look up and update location check digits in LOCA (Locations). However, unlike RFCD LOCA does not allow you to update a range of locations in a single step.
REQUIREMENTS
WAREHOUSE AND 
LOCATION FORMAT
Check digit scanning must be activated in WARE by selecting the Manual Check 
Digit 1 option in the Voice Check Digit Usage field.
If you wish to assign a check digit to a single location:
If you wish to assign the same check digit to multiple locations:
a) Key in your location code and press Enter.
a) Use the %” character as a wildcard. For example, enter A1% to for all locations starting with the characters A1 or A1%1B for all locations starting with the characters A1 and ending with the characters 1B.

RFCD screen showing 12 records retrieved
AccellosOne 3PL will retrieve all locations whose code matches the search criteria that you entered. If there is currently a check digit assigned to the location(s) retrieved, it will display in the Check Digit field.
3 Do one of the following:
4 Key in your new check digit over the existing check digit (if any) and press Enter. When you press Enter, all records that you retrieved in RFCD are updated with the new check digit.
5 Press F4 twice to exit RFCD.
If your query retrieved a singe location:
If your query retrieved multiple locations:
If you used the wildcard “%” in your query:
a) Proceed to next step. a) If required, you can use your up and down arrow keys to scroll through the list of locations to be updated.
b) Press Enter to position your cursor in the Check Digit field.
a) If required, you can use your up and down arrow keys to scroll through the list of locations to be updated.
b) Press Enter to display the following message:
c) Press Enter to acknowledge the message and position your cursor in the Check Digit field.

### Entering Incidents in RFINC <a id="entering-incidents-in-rfinc"></a>

You can track ad-hoc labor activities that occur while working in RF in RFINC (RF Incidents). For example, a pallet is poorly stacked and falls over, a battery change is required for a forklift or a worker goes on break. If required, you can invoice the activity to a customer and add a free-text comment.
The elapsed time of the incident is tracked by comparing the start time to the end time; that is, the time that the incident was opened versus the time that you exit RFINC.
RFINC can be run directly from the menu or can be initiated from RFPIC, RFPU. RFCH and RFRL by pressing the F5 function key.
1 Enter RFINC.
RFINC screen
2 Press F3 (PL) to display the job type pick list.
REQUIREMENTS
CUSTOMER RELATIONSHIP MANAGEMENT
If the incident’s job type in JBTP is attached to a CRM code, RFINC will create a 
CRME record for the incident.
See the labor tracking section of the Operations 2 Guide for further information on job types.
BILLING If an incident’s job type in JBTP is attached to a charge code and you select the invoice to customer option, RFINC will create an accessorial charge for the incident.
See the labor tracking section of the Operations 2 Guide for further information on job types.
MESSAGES Message codes must be set up in MESS.

RFINC screen showing job type pick list
3 Use your up and down arrow keys to position the cursor over the job type that you wish to select. Then press F3 (SL) to select it.
4 Key in the quantity of product involved in the incident and press Enter.
5 Key in the quantity's SKU code and press Enter.
RFINC screen showing quantity of one pallet
6 Do one of the following:
7 Key in your message code for the incident and press Enter or use the pick list function to select your message code.
8 If your job type is attached to a CRM code, you can key in free-text comment in the Comment field. This comment will appear in the Description field of CRME.
9 When you finish entering your incident, press F1 (PR) to process.
If you wish to charge for the incident:
If you do NOT wish to charge for the incident:
a) Press F9 to position your cursor in the Invoice to Cust field.
b) Key in Y for Yes and press Enter.
c) Key in your customer code and press Enter or use the pick list function to select your customer.
a) Proceed to next step.

RFINC screen showing system-generated incident number
10 Press F4 (EX) to exit.

### Performing CRM Tasks in RFCE <a id="performing-crm-tasks-in-rfce"></a>

If a CRM (Customer Relationship Management) task has been assigned to you in CRME (CRM Entry), you will be prompted to perform the task whenever you log on to RF or exit an RF program. You can also access your CRM tasks directly in the program RFCE (RF CRM Entry).
CRM tasks remain assigned to you until you close them. When you close a CRM task, you can add a free-text comment to it or you can close the task without adding a comment.
CRM entry in RF does not support labor tracking.
1 Enter RFCE.
RFCE screen showing three CRM tasks assigned to RF operator

2 Do one of the following:
RFCE screen showing details for CRM
3 Do one of the following:
4 Press F4 (EX) to exit RFCE.
If you wish to scroll through the list of CRM tasks: If you wish to perform a query:
a) Using your arrow keys, select the 
CRM task that you wish to work on and press F3 (SL).
a) Press F1 (EQ).
b) Key in your query word or phrase and press Enter.
c) If your query retrieves more than one record, use your arrow keys to select the task that you wish to work on and press F3 (SL).
If you wish to add a comment before closing the CRM task:
If you wish to close the CRM task without adding a comment:
If you wish to exit without closing the CRM task:
a) Key in your comment and press Enter.
b) When prompted to close the task, key in Y for Yes and press Enter. 
c) Press Enter to continue when the CRM Closed message appears.
a) Press F3 (PR) to process the task.
b) When prompted to close the task, key in Y for Yes and press Enter. 
c) Press Enter to continue when the CRM Closed message appears.
a) Press F4 (EX) to exit without closing the CRM task.

### Checking Your Bar Codes in RFBR <a id="checking-your-bar-codes-in-rfbr"></a>

This program allows you to scan in any bar code to find out the number of empty spaces between each segment. Empty spaces are indicated by hyphens.
1 Enter RFBR.
RFBR screen
2 Scan in your bar code.
RFBR screen showing embedded spaces indicated by hyphen
3 Press F4 (RT)
4 Press F4 (EX) to exit.

### Entering Hold Adjustments in RFHO <a id="entering-hold-adjustments-in-rfho"></a>

This program allows you to make positive and negative hold adjustments in RF. It is similar to HOAD (Hold 
Adjustments), but only supports hold codes that have been activated for RF processing in HOLD (Hold 
Types).
There are two flags in HOLD that control the behavior of RFHO: RF Hold Excl From and RF Hold Excl To. If you select RF Hold Excl From, you cannot remove this hold code from product in RFHO. If you select RF 
Hold Excl To, you cannot attach this hold code to product in RFHO. If you leave both fields unchecked, there are no restrictions related to this hold code in RFHO.
HOLD screen showing flags RF Hold Excl From and RF Hold Excl to

### PLACING PRODUCT ON HOLD <a id="placing-product-on-hold"></a>

1 Enter RFHO.
2 Key in your UI value and press Enter.
RFHO screen showing prompt for Hold to
3 Key in your hold code and press Enter.

RFHO screen showing prompt for hold quantity
4 Key in your hold quantity and press Enter.
RFHO screen showing “F3 to process” message
5 Press F3 to process.
6 When prompted to proceed, key in Y for Yes and press Enter.
RFHO screen showing “<Enter> to continue” message
7 Press Enter to continue.

8 Press F4 to exit.

### REMOVING INVENTORY FROM HOLD <a id="removing-inventory-from-hold"></a>

1 Enter RFHO.
2 Key in your UI value and press Enter.
RFHO screen showing 10 cases on DMG Hold
3 Press Enter to bypass the HT (Hold To) field.
RFHO screen showing prompt for hold quantity
4 Key in your hold quantity as a positive number and press Enter.

RFHO screen showing “F3 to process” message
5 Press F3 to process.
6 When prompted to proceed, key in Y for Yes and press Enter.
RFHO screen showing “<Enter> to continue” message
7 Press Enter to continue.
8 Press F4 to exit.

### Processing Supervisor Overrides in RFSUN <a id="processing-supervisor-overrides-in-rfsun"></a>

This program allows supervisors to look up and accept overrides from the following programs: RFCH, RFPU, 
RFPIC, OLOP and RFRL. When an override is accepted in RFSUN, it is deleted and can no longer be accessed.
1 Enter RFSUN.

RFSUN screen
2 Press Enter to advance to the DOC field.
3 Key in your query criteria. You can query by document type, document number, document line, building, door, selection code, terminal code and operator code. There are five document types in RFSUN: I for 
Inbound, O for Outbound, M for Relocation, R for Replenishment and L for Load.
4 When you finish entering your query criteria, press F2 (PL) to execute your query.
RFSUN screen showing override in OLOP
5 Use your arrow keys to scroll through the list of override records. When you reach the record that you wish to process, press F3 to select it.
RFSUN screen showing prompt "F3 TO PROCESS"
6 Press F3 to process.

RFSUN screen showing prompt to confirm
7 To confirm acceptance of the override, key in Y for Yes and press Enter. To cancel your acceptance, key in N for No and press Enter.
8 Press F4 (EX) to exit.

### Entering Inventory Attributes in RFATT <a id="entering-inventory-attributes-in-rfatt"></a>

This program allows you to attach inventory attributes to existing inventory in your warehouse.
1 Enter RFATT.
RFATT screen
REQUIREMENTS
INVENTORY 
ATTRIBUTES
Inventory attributes must be set up in IAPR (Inventory Attributes) and your IAPR profile must be attached to the appropriate items.

2 Scan or manually enter your UI.
3 If there are multiple inventory entities with the same UI, press F3 to select the inventory entity that you wish to work with.
RFATT screen showing prompt for country of origin (1 inventory attribute required)
4 Scan or manually enter the required inventory attribute(s).
RFATT screen showing “Attributes not required or entered” message
5 Press Enter to acknowledge the “Attributes not required or entered” message.
6 Press F4 to exit.

VOICE-ACTIVATED PICKING AND ORDER 
ASSIGNMENT SYSTEM

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

### Overview <a id="overview"></a>

Voice-activated picking using Vocollect Voice allows you to perform easy, hands-free picking. You can set up voice profiles defining various Vocollect Voice options and attach these profiles to task profiles that define which customers, carriers, consignees, items, orders, locations and warehouses can be picked. If required, voice-directed picking can be combined with scanning when certain inventory levels are too long to be spoken.
You can also define voice operator overrides that temporarily override an operator’s standard task profiles in order to perform work that is particularly urgent.
The order assignment system allows you to assign specific orders and/or order lines to specific operators and define a picking sequence for each order. When the designated operator enters RFPIC, only orders assigned to that operator will display in the pick list. If required, an operator can cancel order assignments in RFPIC; 
when this happens, the order line appears in the pick list of all RF operators.
The order assignment system shares two voice-activated picking programs — RFOP and RFOT — but does not use voice profiles defined in VOPR and VOPC.

### Setting Up Voice-Activated Picking <a id="setting-up-voice-activated-picking"></a>

There are up to eight setup programs for voice-activated picking:
▪ VOPR (Voice Profile)
▪ VOPC (Voice Profile - Customer)
▪ REGI (Task Profile)
▪ RFOP (RF Operator)
▪ WARE (Warehouses and Location Format)
▪ LOCA (Locations)
▪ REAS (Reason Code)
▪ MHEC (Material Handling Equipment Code)
There are two voice profiles in voice-activated picking: VOPR and VOPC. VOPR defines properties that are specific to particular task profiles and operators, while VOPC defines properties that are specific to particular customers.

### SETTING UP YOUR VOICE PROFILE IN VOPR <a id="setting-up-your-voice-profile-in-vopr"></a>

In this program, you define your voice profiles. A voice profile is a user-defined code that identifies a number of Vocollect Voice options or properties. When you attach this code to a task profile in REGI and then attach the task profile to an operator in RFOP, the properties that you define in VOPR will be assigned to the operator.
You can create a single voice profile for all operators or you can create multiple voice profiles and assign them to the appropriate task profiles and operators.
In VOPR, you define the following properties:
▪ whether or not the operator requests work or the system assigns it automatically
▪ which inventory level(s) the operator will hear for each pick

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
▪ whether or not the operator will be prompted with the delivery location
▪ the number of digits in a work ID
FIELD DESCRIPTIONS
Voice Profile Code Mandatory
Your voice profile code.
Description Mandatory
The description for your voice profile code.
Auto-Assign Options Operator requests work
System assigns operator assignment
If you select Operator requests work, the operator will be prompted to read out the order number that he or she wishes to pick. If you select System assigns operator assignment, assignments are automatically assigned to operators and no order number is required.
Inventory Level Prompt No Inventory Levels
Level 1 Only
Level 2 Only
Level 3 Only
Level 4 Only
Level 1, 2, etc.
In this field, you specify which inventory levels (if any) the operator will hear from Vocollect Voice for each pick.
Delivery Location Prompt with delivery location
Prompt with and confirm delivery location
In this property, you specify whether or not you want AccellosOne 3PL to prompt the operator for the delivery or staging location and whether or not you want the operator to confirm the delivery or staging location.
If the order has been assigned an appointment, AccellosOne 3PL will use the appointment’s door/location as the delivery location. If the order has NOT been assigned an appointment, AccellosOne 3PL will use the staging location in the operator’s task profile.
The operator can override the delivery location by saying “override”. The system will ask him or her for a new location. From that time on, the new location will be used for the next delivery until the operator overrides it again.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
1 Enter VOPR.

VOPR screen
2 Click on Create.
3 Key in your voice profile code and press Enter.
4 Key in a description for your new code and press Enter.
Work ID Length The number of digits in a work ID. If an operator provides a work ID with fewer than this number of digits, it will be rejected by AccellosOne 3PL.
If you enter the value -1, the operator must provide the entire work ID number.
Assignment Message If populated, this field will be read out to the voice operator for each assignment that he or she is going to work on. This is the default message. It will not be read out if there are higher level assignment messages that replace the 
VOPR default message. There are four possible higher level assignment messages:
1) pallet code description will be read out if a pallet code is attached to the 
CONS record for the order
2) message code description will be read out or added to the above if a message code is attached to the CONS record for the order
3) message code description will be read out or added to the above if a message code is attached to the order header
4) appointment time and door number will be read out or added to the above if an appointment is attached to the load of the order
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
5 Click on Save.
6 Proceed to select the appropriate option for each property by either selecting the option from a dropdown list or by keying in a value.
7 When you finish selecting your properties, click on Save.
8 Click on Exit to exit VOPR.

### SETTING UP YOUR VOICE PROFILE (CUSTOMER) IN VOPC <a id="setting-up-your-voice-profile-customer-in-vopc"></a>

In this program, you define your customer-based voice profiles. A customer-based voice profile is a userdefined code that identifies a number of Vocollect Voice options or properties. When you attach this code to a customer in CUST, the properties that you define in VOPC will be assigned to that customer.
In VOPC, you define the following properties:
▪ whether or not you want AccellosOne 3PL to state a given inventory level before each pick
▪ whether or not you want the operator to read back the inventory level as confirmation
▪ whether or not cycle counting is activated and the rules to follow when the inventory count by the operator does not match the on hand quantity
FIELD DESCRIPTIONS
Voice Profile Code Mandatory
Your customer-based voice profile code.
Description Mandatory
The description for your customer-based voice profile code.
Data 1 Use Do not process data 1
Process data 1
In this property, you specify whether or not you want AccellosOne 3PL to process the data 1 value of product being picked. Data 1 can refer to any inventory level. If you select the “Do not process data 1” option, AccellosOne 3PL will specify a quantity and location for each pick, but no inventory levels.
Data 1 Heading None
Level 1
Level 2
Level 3
Level 4
The inventory level that data 1 refers to.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
Data 1 Confirmation Only available if Data 1 Use is set to “Process data 1”
Do not capture data 1 information
If you select this option, the data 1 value is spoken but the operator does not read it back.
Capture data 1 information
If you select this option, the data 1 value is spoken and the operator must read it back. The value read back must match the product being picked or must be a valid substitution product.
Do not speak the data 1 field but allow operator to enter confirmation value
If you select this option, the data 1 value is not spoken but the operator must confirm it. The value confirmed must match the product being picked or must be a valid substitution product.
Data 1 Minimum Capture 
Length
In this property, you specify the number of characters in the inventory level that the operator must read out. For example, if you set this property to two, the operator must read out the last two characters in the inventory level. 
This value is a minimum only; if the inventory level has five characters and this value is set to two, the operator can read out the last two characters, the three last characters, the four last characters or all five characters. However, he or she cannot read out the last character only as this value is less than the minimum.
If you leave this field blank, the operator must read out all characters in the inventory level.
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
In this field, you activate cycle count count backs for your voice customer. See [Performing Inventory Count Backs](expedicao-rf.html#performing-inventory-count-backs) for further information.
Cycle Count Rules Ignore investigation
Supervisor must override
Flow advancement not allowed
Supervisor override/No flow advance
See the Inventory Count Rules field in MRFP (RFPIC 2).
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

VOPC screen
2 Click on Create Record.
3 Key in your voice profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 Click on Save.
6 Proceed to select the appropriate option for each property by either selecting the option from a dropdown list or by keying in a value.
7 When you finish selecting your properties, click on Save.
8 Click on Exit to exit VOPR.
9 When you finish setting up your voice profile, open CUST and proceed to attach your voice profile to the appropriate customer by entering the voice profile code in the Voice Profile Code field.

### SETTING UP YOUR TASK PROFILE IN REGI <a id="setting-up-your-task-profile-in-regi"></a>

In this program, you attach your voice profile code set up in VOPC to your task profile. You also define the length of your UI check digit, the length of the spoken portion of the OPIC and whether the spoken value must be numeric. See [Task Profile (REGI)](expedicao-rf.html#task-profile-regi) for further information on this program.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
The following fields in REGI apply exclusively to voice-activated picking:

### SETTING UP YOUR RF OPERATORS IN RFOP <a id="setting-up-your-rf-operators-in-rfop"></a>

See [RF Operator (RFOP)](picking-rf.html#rf-operator-rfop).

### SETTING UP YOUR CHECK DIGIT PARAMETERS IN WARE (OPTIONAL) <a id="setting-up-your-check-digit-parameters-in-ware-optional"></a>

You can define up to three manual check digits for each location in AccellosOne 3PL. Check digits are alternate location codes that Vocollect Voice uses whenever the actual location code is too long to be read out by the operator for each pick.
You define the number of check digits as well as the days of the week that each check digit will be used in 
WARE (Warehouse and Location Format). Then you enter your manual check digits for each location in the 
Voice Check Digit 1/2/3 fields in LOCA (Locations).
1 Enter WARE.
2 Retrieve the warehouse that you wish to set up for manual check digits.
FIELD DESCRIPTIONS
Voice Profile Code (VOPR)
Mandatory
The task profile’s voice profile.
Default Customer Voice 
Profile Code (VOPC)
The default customer voice profile for the task profile. This profile is used if the customer has not been assigned a voice profile in CUST.
Length of UI Check Digit Optional
The length of the UI check digit. For example, if you enter 3 in this field, the operator must read out the last three digits belonging to the UI of the product to picked in the location that the product is to be picked from.
For example, suppose the order line is picking item ABC001, pallet ID PA987 from location LA001. The voice terminal will read out the location code to the operator. The operator will go to the location LA001, find pallet ID PA987 and read out “987” to confirm that he or she has arrived at the location.
Spoken Length The length of the spoken portion of the OPID. This value is added to the OPID prefix to form the full OPID for the order line being picked. AccellosOne 3PL will validate this number to ensure that it is unique and has not been used before.
Spoken Value Numeric If this field is checked, the value spoken by the operator must be numeric. If this field is NOT checked, the value spoken by the operator can be alphanumeric.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
3 Press Enter until your cursor is positioned in the Voice Check Digit Usage field. Then select the appropriate manual check digit option.
4 Depending on the option that you selected in the previous step, key in the days of week separated by commas for each check digit and then press Enter. For example, to enter Monday, Wednesday and Friday, you would key in MON,WED,FRI. 

WARE screen showing two check digits for warehouse 1
5 When you finish setting up your check digit parameters, click on Return to Main and Exit.

### ASSIGNING CHECK DIGITS TO LOCATIONS IN LOCA <a id="assigning-check-digits-to-locations-in-loca"></a>

If you specified one or more check digit days in WARE, you must add one check digit in LOCA for each check digit day in WARE.
1 Enter LOCA.
2 Retrieve the location that you wish to assign a check digit to.
3 Key in your check digits for the location.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
LOCA screen showing two check digits for location A100
4 Repeat the above steps for any additional locations in the warehouse that require check digits.
5 When you finish assigning check digits to your locations, click on Return to Main and Exit.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

### SETTING UP YOUR REASON CODES IN REAS <a id="setting-up-your-reason-codes-in-reas"></a>

In this program, you set up your reason codes for voice-activated picking. Pickers use these codes to record a reason when the pick quantity for a given order line does not match the order quantity.
1 Enter REAS.
FIELD DESCRIPTIONS
Reason The following reason codes are supported:
1 (Split-picking a Line)
This option is used for short picks; that is, the picker wishes to pick a partial quantity from the location and return for the remaining quantity at a later time. 
For example, if the pick quantity is five cases and the picker picks two cases, 
AccellosOne 3PL will split the line into two lines. Line 1 (two cases) will be marked as picked, while line 2 (three cases) will be marked as unpicked.
2 (Not Enough Product SUSP Hold)
3 (Location is Empty SUSP Hold)
With this option, the allocated product is put on a SUSP hold. The original order will be zeroed out and a new P-type line will be created and allocated. If allocation is successful, the new order line can be picked at a later time.
4 (Not enough Product LOST Hold)
5 (Location is Empty LOST Hold)
With this option, the allocated product is put on the hold code that you enter in the Hold Code field of REAS (and not on SUSP hold). The original order line will be zeroed out and a new P-type line will be created but NOT allocated. To allocate the new order line, you must either do so manually in ASOR (Assign 
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
2 Click on Create Record.
3 Key in your reason code (1, 2, 3, 4 or 5) and press Enter.
4 Key in an appropriate description for your reason code and press Enter.
5 In the Type field, key P for Pick and press Enter.
6 In the Attached To field, key in PICK and press Enter.
7 Repeat the above steps for each additional reason code that you wish to set up.
REAS screen showing standard reason code for voice-activated picking
8 When you finish setting up your reason codes, click on Return to Main to exit create record mode.
9 Click on Exit to exit.

### ACTIVATING YOUR VOICE TERMINALS IN MHEC <a id="activating-your-voice-terminals-in-mhec"></a>

Voice terminals need to be activated in MHEC before you can use them in AccellosOne 3PL.
FIELD DESCRIPTIONS
Equipment Code The terminal ID of your Talkman voice terminal.
Description A description for your Talkman voice terminal.
Type Set to TALK.
Hourly Cost Reserved for future use
Warehouse Code The warehouse code for your voice terminal.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
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
Location Code The location code of your voice terminal. The warehouse and location code that you attach to a voice terminal in MHEC will be assigned to any product picked using this voice terminal. 
For example, if you assign staging location S100 to a given voice terminal and then pick 10 cases of product using this terminal, AccellosOne 3PL will create a record in the Location Block of LOEN showing 10 cases of product in location S100.
In LOCA, the following setup is required for this location:
▪ its location type in LOTP must be staging
▪ its location structure type code in LOCA must be MHE
FIELD DESCRIPTIONS

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
If you do not want to pick certain orders using your voice-activated equipment, you can pick the orders in 
RFPV (RF Picking Voice) using standard RF guns.
1 Enter RFPV.
RFPV screen showing RF operator’s region
2 Press Enter to continue.
RFPV screen showing first order line to pick
3 Do one of the following:
If you wish to pick the order line:
If you do NOT want to pick the order line:
a) Press F3 (SL) to select it. a) Press F1 (SK) to skip it.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

### Picking Orders in RFPV <a id="picking-orders-in-rfpv"></a>

4 If an item message displays, press F4 (EX) to continue.
RFPV screen showing prompt for pick location
5 Key in or scan in your pick location.
RFPV screen showing prompt for UI
6 Key in or scan in your UI (Unique Identifier).

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
RFPV screen showing prompt for pick quantity
7 Key in your pick quantity and press Enter.
RFPV screen showing prompt for to location
8 If prompted to do so, key in or scan in the check digit for the location.
RFPV screen showing “Assignment Completed” message

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

### Assigning RF Operators to Orders in RFOT <a id="assigning-rf-operators-to-orders-in-rfot"></a>

9 Press Enter to acknowledge the “Assignment Completed” message.
RFPV screen showing “Assignment Completed” message
10 Press Enter to continue with the next pick or key in 2 and press Enter to exit RFPV.
If you use Vocollect Voice to pick your orders, you can temporarily override the orders in an operator’s standard task profile(s) in order to give priority to orders that are particularly urgent. You define overrides by selecting individual orders and order lines in RFOT and assigning them to the appropriate voice operator.
If you do not use Vocollect Voice and pick your orders in RFPIC, assigning operators to orders in RFOT will reserve those orders/order lines for the designated operator in RFPIC. When the designated operator enters 
RFPIC, only assigned orders for that operator will display in the pick list.
RFOT also allows you to define the picking sequence of orders assigned to a particular RF operator. If you do not define a picking sequence, orders will be sequenced by order priority followed by order number.

### ASSIGNING RF OPERATORS TO ORDERS AND ORDER LINES <a id="assigning-rf-operators-to-orders-and-order-lines"></a>

You can assign either order lines or entire orders to a given operator.
1 Enter RFOT.
2 If required, click on the Pick/Interleave (2) tab.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
RFOT screen showing Pick/Interleave (2) tab
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all order lines that meet your filter criteria.
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

RFOT screen showing orders that meet the filter criteria
4 If required, you can resort the order records in either ascending or descending sequence by clicking on the appropriate header buttons (Order #, Customer, Consignee, To Ship Date, Flow or Cust. Order #).
5 If there is a line remark attached to the order line, click on Remarks to view it.
6 If you wish to assign order lines to an operator, click on the Lines tab.
TODAY Only orders with a to ship date of today
TODAY +1, etc. On orders with a to ship date of tomorrow (+1) or the day before yesterday (-2)

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
7 Proceed to assign the orders/order lines that you want the operator to work on by one of the following methods:
8 If required, you can assign a sequence number to an order/order line and the order/order line must be picked in that sequence. If you do not specify a sequence number, orders will be sequenced by order priority followed by order number.
9 When you finish assigning your orders/order lines, click on Save.

RFOT screen showing three orders assigned to the operator D4SUPPORT
10 Click on Exit to exit RFOT.

### ASSIGNING RF OPERATORS TO LOADS <a id="assigning-rf-operators-to-loads"></a>

You can restrict RF operators to loads, buildings and doors. When you assign an operator to an entire load, the assignment is applied to all orders on the load. The restrictions that you enforce in RFOT apply to OLOP (Outbound Loading Process).
1 Enter RFOT.
2 Click on Outbound Loads.
If you wish to assign individual operators to individual orders/ order lines:
If you wish to assign all unassigned orders/order lines to a given operator:
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on the checkbox to the left of the operator code to complete the assignment.
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on Assign All.
c) If you make a mistake and wish to undo all assignments made in the current session, click on 
Unassign All.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

RFOT screen
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all loads that meet your filter criteria.
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
TODAY +1, etc. On orders with a to ship date of tomorrow (+1) or the day before yesterday (-2)

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

RFOT screen showing loads that meet the filter criteria
4 If required, you can resort the load records in either ascending or descending sequence by clicking on the appropriate header buttons (Load #, Ext. Load #, Building, Door or Operator).
5 Proceed to assign the loads that you want the operator to work on by one of the following methods:
6 If required, you can assign a sequence number to a load and the load will be picked in that sequence. If you do not specify a sequence number, loads will be sequenced by order priority followed by order number.
7 When you finish assigning your loads, click on Save.

RFOT screen showing three loads assigned to the operator DALLEN
If you wish to assign individual operators to individual loads:
If you wish to assign all unassigned loads to a given operator:
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on the checkbox to the left of the operator code to complete the assignment.
a) Select your operator from the 
Assign Operator dropdown list.
b) Click on Assign All.
c) If you make a mistake and wish to undo all assignments made in the current session, click on 
Unassign All.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
8 Click on Exit to exit RFOT.

### ASSIGNING RF OPERATORS TO PICK METHODS <a id="assigning-rf-operators-to-pick-methods"></a>

1 Enter RFOT.
2 Click on Pick/Interleave (2).
3 Select your pick method from the Pick Method pick list.
4 Click on Execute Query.
5 When RFOT retrieves all orders whose pick method matches the pick method that you specified in step 
3, select your operator from the Assign Operator dropdown list.
6 Click on the checkbox to the left of the operator code to complete the assignment.
7 Click on Save to save your changes.

### REMOVING AN OPERATOR ASSIGNMENT <a id="removing-an-operator-assignment"></a>

You can remove an operator assignment in RFOT if the operator has not already started it. Once an assignment is started in either RFPIC or Vocollect Voice, removing an operator assignment in RFOT will have no affect on the order currently being worked on.
1 Enter RFOT.
2 On the Filter window, key in the RF operator code of the operator whose assignments you wish to remove and click on click on Execute Query. You can query by multiple operators by separating each operator by a comma; for example, “BOB1,BOB2”.
RFOT screen showing three order lines assigned to the operator D4SUPPORT

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
3 Do one of the following:
4 When you finish removing your operator assignments, click on Save.
5 Click on Exit to exit RFOT.

### SUSPENDING A TASK <a id="suspending-a-task"></a>

You can temporarily suspend an order or task until you are ready to pick it.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
RFOT screen
3 Click in the Suspend Tasks column of each order that you wish to suspend.
4 Click on Save to suspend the order.

### RELEASING A SUSPENDED TASK <a id="releasing-a-suspended-task"></a>

When you are ready to pick the order, you must release the suspension.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
If you wish to remove an RF operator from an order:
If you wish to remove an RF operator from an order line:
a) Click on the Order tab to access your orders.
b) Click on the Operator dropdown list and select the operator “--
NONE--”.
a) Click on the Operator dropdown list and select the blank “operator” at the end of the list.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
RFOT screen
3 Click in the Suspend Tasks column of each order that you wish to release to deselect the checkbox.
4 Click on Save to release the order.

### CHANGING THE SYSTEM-ASSIGNED STAGING LOCATION <a id="changing-the-system-assigned-staging-location"></a>

1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
RFOT screen
3 Select your new staging location from the dropdown list for each affected order.
4 Click on Save to save your changes.

### CHANGING THE PRIORITY LEVEL OF A TASK <a id="changing-the-priority-level-of-a-task"></a>

The Tasks tab allows you to assign a priority override value to an order line task. The default value is 100. If you enter a lower value (say, 50), the order line task will have a lower priority.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM

### Clearing Work Assignments in CTPA <a id="clearing-work-assignments-in-ctpa"></a>

1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
RFOT screen
4 Enter your priority override value (must be less than 100).
5 Click on Save to save your changes.
You can look up the current work assignments of your Vocollect Voice operators in CTPA (Clear Terminal Pick 
Assignments). In the Detail Block of this program, you can clear all work assignments for a given voice operator and make these work assignments available to another voice operator.
1 Enter CTPA.
CTPA screen showing 3 work lines assigned to the operator E80568
NOTE The Execute Query command in this program is limited to a screen refresh only. It does not allow you to perform actual queries.

VOICE-ACTIVATED PICKING AND ORDER ASSIGNMENT SYSTEM
2 Select the operator whose work assignments you wish to look up or clear and click on Detail Block.
CTPA screen showing current work assignments for operator E80568
3 Do one of the following:
4 Click on Exit.
If you wish to look up the operator's work assignments only:
If you wish to clear the operator’s work assignments:
a) When you finish looking up the work assignments, click on Master Block.
a) Click on Clear All Assignments. 
All current work assignments for the operator that you selected will be released and made available to other Vocollect Voice operators.

## Equipment Tracking <a id="equipment-tracking"></a>

*Manual H — RF Guide*

### Overview <a id="overview"></a>

The equipment tracking system allows you to track the equipment used by each RF operator, restrict certain activity types such as picking, packing, etc. to certain types of equipment and restrict certain RF operators to certain activity types and equipment types. If you assign a location to a piece of equipment, you can track a product’s location as it is moved around the warehouse.
Equipment can be equipment that carries or holds product such as a forklift truck or pallet jack. It can also be any device used in the warehouse that you wish to track such as a voice headset or an RF scanner. 
When equipment tracking is enabled, the following screen will appear each time an RF operator logs on:
Prompt for MHE code
The RF operator must enter a valid material handling equipment code in order to proceed. If the RF operator enters a material handling equipment type code already in use, one of the following message will appear:
The REMOVE THE LOCK message means that there are no active sessions attached to the MHE code and thus the MHE code is empty. It is safe to remove the lock.
Prompt to remove lock or change MHE code
Prompt to take over the MHE or reenter MHE

The TAKE OVER THE MHE message means that the Oracle session is still active even though the Unix session has been dropped (for example, the RF operator switches off the device or removes the batteries). If you take over another user’s session, that person will lose all his or her work and the gun will be frozen. This option must be used with extreme caution.

### Company Code (COMP) <a id="company-code-comp"></a>

In this program, you activate equipment tracking by selecting Yes in the Enable Equipment Tracking in RF flag.
Company Parameters block in COMP showing equipment tracking activated

### RF Checklist (MCHK) <a id="rf-checklist-mchk"></a>

In this program, you set up your checklists for RF equipment types. In the checklist, you define one or more questions for the RF operator as well as possible answers to these questions. One of the answers is marked as failed. 
In the Header Block, you create a code and description for your new checklist. In the Question Block, you create a list of questions in the desired sequence. If the Information Only flag is turned on, an answer is not required for that question. In the Answer Block, you define possible answers.
The checklist code that you create in MCHK is attached to the Checklist tab in MHET for the appropriate equipment type. It can also be attached to loads in SELO. When an RF operator enters any equipment code belonging to that equipment type in any RF program, the following prompt appears:

Checklist prompt for forklift
If the RF operator enters 1 for Pass, he or she can proceed to pick the order, put-away the receipt, etc. If the 
RF operator enters 2 for Fail, he or she cannot proceed with that equipment code.
MCHK screen 

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
A unique sequence number for your question. Your checklist can contain as many questions as you require.
Question Mandatory
The question or instruction that will display to the RF operator in every RF program.
Information Only If you select this flag, the question or statement in the previous field does not require an answer.
Answer Sequence NumberMandatory if Information Only flag is not checked
A unique sequence number for your answer. You can have as many answers as you like for a given question.
Answer Mandatory if Information Only flag is not checked
Your answer text. For example, “Pass”, “Fail”, etc.
Fail Flag If you select this flag, the answer is a fail and the RF operator will not be able to proceed if he or she selects that answer. At least one answer for each question should be set up as a fail.

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
16 if you wish to add a second question to your checklist, click in Checklist Sequence Number field, key in 2 as your sequence number and press Enter. 
17 Repeat steps 7 to 10 for the first answer to your second checklist question.
18 Add your additional answers to the second checklist question.
19 When you finish setting up your checklist, Click on Exit to exit.

### Material Handling Types (MHET) <a id="material-handling-types-mhet"></a>

In this program, you attach the checklist code that you created in MCHK to the Checklist tab in MHET for the appropriate equipment type. If you perform RF tasking in RFITLV, you must specify the equipment type’s vertical height factor and excluded warehouse activity types (if any).

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

Location Required N = No
Y = Yes
If you select N for No, a staging location is not required in MHEC for material handling equipment codes assigned this equipment type. If you select Y for 
Yes, a staging location is required in MHEC for material handling equipment codes assigned this equipment type.
Staging locations are not mandatory for material handling equipment codes. 
However, they allow you to track product more effectively on an open order. 
For example, if you assign staging location S100 to a given forklift and then pick 10 cases of product using this forklift, AccellosOne 3PL will create a record in the Location Block of LOEN showing 10 cases of product in location 
S100.
Location Vertical Height Only supported in RFITLV
The height or vertical reach of this equipment type, The vertical height factor code in this field must match the vertical height factor code of the location before an RF operator assigned this equipment type can be assigned a task for the location.
Exclude Whse Activity 
Type
Only supported in RFITLV
If you enter one or more activity types in this field, the RF operator will not be able to use this equipment type for this activity type in RFITLV.
Checklist In this field, you enter the checklist code that you created in MCHK.
Pick Method Reserved for future use.
FIELD DESCRIPTIONS

MHET screen showing electric lift equipment type that can be assigned to locations whose vertical height factor = 1 to 5

### Material Handling Equipment Code (MHEC) <a id="material-handling-equipment-code-mhec"></a>

In this program, you set up your material handling equipment codes. RF operators must enter one of these equipment codes each time that they enter an RF program.
MHEC screen

FIELD DESCRIPTIONS
Equipment Code Mandatory
Your material handling equipment code.
Description Mandatory
Your description for this material handling equipment code.
Type (defined in MHET) Mandatory
The material handling type for this material handling equipment code.
Hourly Cost Reserved for future use
Warehouse Code Only available if Location Required flag set to Yes in MHET for the material handling type
The warehouse code for this material handling equipment code.
Location Code Only available if Location Required flag set to Yes in MHET for the material handling type
The staging location code for this material handling equipment code. In LOCA, the following setup is required for this location:
▪ its location type in LOTP must be staging
▪ its location structure type code in LOCA must be MHE
The location capacity in LOCA (for example, two pallets) determines the number of SKU’s that can be moved in a multi-pallet move.

### RF Operator (RFOP) <a id="rf-operator-rfop"></a>

In this program, you set up your activity type and material handling type exclusions for RF operators. If you specify one or more task profiles for the RF operator on the Task Profiles tab, the RF operator will be restricted to those task profiles. 
RFOP screen showing activity type restrictions for ALEX

### Locations (LOCA) <a id="locations-loca"></a>

In this program, you define your location height restrictions for each location. Only equipment types whose vertical height factor code matches the location’s vertical height factor code can be assigned a task in this location.
NOTE Activity type and material handling type exclusions are only supported in 
RFITLV.

LOCA screen showing location assigned a vertical height factor code of 3

### Warehouse Shift Setup (WASH) <a id="warehouse-shift-setup-wash"></a>

In this program, you set up your warehouse shifts. Warehouse shifts are optional in equipment tracking. If you set up warehouse shifts, the RF checklist will need to be performed by the RF operator only once per shift. If you do not set up warehouse shifts, the RF checklist will need to be performed each time that an RF operator logs on (that is, more than once per shift if the RF operator logs off during a shift).
WASH screen showing three shifts

### Operator Code (OPER) <a id="operator-code-oper"></a>

If you use warehouse shifts, you must assign the appropriate warehouse shift code to your operators in 
OPER.
FIELD DESCRIPTIONS
Shift Code Mandatory
Your warehouse shift code.
Description Mandatory
Your description for this warehouse shift code.
Warehouse Code Mandatory
The shift’s warehouse.
Shift ID in Time & Attendance
Reserved for future use
Start Time The start time in 24-hour format of the shift.
End Time The end time in 24-hour format of the shift.

OPER screen showing operator being assigned the warehouse shift code of DAY

### Looking Up Equipment Tracking Data <a id="looking-up-equipment-tracking-data"></a>

Equipment tracking data is stored in the Oracle database. If you wish to look this data up, you must write a d’Amigo query.
