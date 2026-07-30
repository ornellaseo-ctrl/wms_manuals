---
title: "Recebimento via RF (Check-in e Put-Away)"
description: "Operação de entrada no coletor: RFCH check/unload, RFPU put-away, variâncias e temperatura."
layout: default
---

# Recebimento via RF (Check-in e Put-Away)

Operação de entrada no coletor: RFCH check/unload, RFPU put-away, variâncias e temperatura.

**Fluxo principal:** `RFCH (check/unload) -> RFPU (put-away) -> RFCV (tie/hi/loose)`

> Fonte: manuais H do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## RFPU <a id="rfpu"></a>

*Manual H — RF Guide*

This tab shows various RFPU options.
RFPU tab
.
FIELD DESCRIPTIONS (RFPU)
Validation Rules for PutAway to Pick LineStop operator from proceeding
Allow operator to proceed (reserved for future use)
Omit validation of location
If you select “Stop operator from proceeding”, the RF operator will not be able to put-away product in RFPU to a pick line location that is not set up for that product in PIIT. If you select “Omit validation of location”, the RF operator will able to put-away product to any pick line location without restriction.
Allow Put-Away to Staging LocationYes
No
If you select No, the RF operator cannot put-away product to a staging location in RFPU. If you select Yes, the RF operator can perform three-step putaway; that is, put-away product to a staging location in RFPU. When product is assigned to a staging location, the receipt’s flow remains at STPU (Start 
Put-Away) and is not advanced to PUCO (Put-Away Complete) until a nonstaging location is eventually entered. 

Variance Handling Variance screen deactivated
Variance screen no sup. override
Variance screen with sup. override
Variance screen for sup. only
If you select “Variance screen deactivated”, the Variance screen does not display for any user. If you select “Variance screen no sup. override”, the Variance screen displays for all users and no supervisor override is required to enter a variance. If you select “Variance screen with sup. override”, the Variance screen displays for all users and a supervisor override is required to enter a variance. If you select “Variance screen for sup. only”, the Variance screen displays for supervisors only and no supervisor override is required to enter a variance. 
NOTE Regardless of the option that you choose, the variance itself is always tracked in LORE even if the Variance screen does not display.
Validation Rules for System-Assigned LocationsNo validation for system-assigned locations and overrides allowed
Validation required WHEN system assigns location and overrides allowed
Validation required ONLY for system-assigned locations and overrides allowed
If you select “No validation”, the RF operator can press Enter in RFPU to accept a system-assigned location without the need to re-enter it. If you select “Validation required WHEN ...”, the RF operator must re-enter or scan in your put-away location in RFPU to confirm it.
If you select “Validation required ONLY ...”, the RF operator must re-enter or scan in your put-away location in RFPU to confirm it only when the location is assigned a location type in LOTP whose Directed Put-Away flag has been set to Yes.
Event-Driven Cycle 
Count Profile (CYCP)
See the Cycle Counting Guide for further information on event-driven cycle counts.
Allow Quantity to be 
Updated
No
Yes
If you select Yes, the RF operator can enter or modify the quantity of a receipt line in RFPU. If you select No, the cursor will skip over the Qty field and the quantity cannot be entered or modified.
FIELD DESCRIPTIONS (RFPU)

Enter/Change Hold Code Allow Entry/Change of Hold Code
Disallow Change of Hold Code. Allow New Hold Code
Disallow Entry/Change of Hold Code f you select “Allow Entry/Change of Hold Code“, the RF operator can enter new hold codes and change existing hold codes in RFCPU. If you select “Disallow Change of Hold Code. Allow New Hold Code.’, the RF operator can enter new hold codes but cannot change existing hold codes in RFPU. If you select “Disallow Entry/Change of Hold Code”, the RF operator will have no access to the hold code field in RFPU.
Maximum Number of F3 (NX) Allowed Per ILOP 
Sequence
In this field, you specify the maximum number of times that the RF operator can press F3 (NX) in RFPU to display a suggested put-away location.
Allow Put-Away of Multiple Pallets in RFPUNo
Yes*
If you select Yes, the RF operator can put-away multiple pallets in a single step; that is, the RF operator scans two or more UI’s but only enters the to location once. If you select No, the RF operator must put-away each pallet individually.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
* Does not support directed put-away. That is, only the flows INST and STPU can have 
the Assign Location flag set to Yes.
FIELD DESCRIPTIONS (RFPU)

## Inbound Processing <a id="inbound-processing"></a>

*Manual H — RF Guide*

### Overview of Put-Away <a id="overview-of-put-away"></a>

There are two ways of putting away product in AccellosOne 3PL:
▪ In two-step put-away, you unload the receipt and use RFCH to place the product in a staging location and then perform final put-away in RFPU. If auto-confirmation is activated in DIFP, no confirmation of the receipt is required in CHRF (Time-Stamp and Confirm Receipt).
▪ In one-step put-away, you unload the receipt and use RFCH to put-away the product in a final nonstaging location with no processing in RFPU. After final put-away in RFCH, you must confirm the receipt in CHRF (Time-Stamp and Confirm Receipt).
If your flows are correctly defined in DIFP, you can switch from one-step put-away to two-step put-away or from two-step put-away to one-step put-away as often as required within the same account. 
If you are performing two-step put-away, you put away the product in RFPU (RF PutAway).
WAREHOUSE
If you are performing one-step put-away, you put away the product in a final nonstaging location. If you are performing twostep put-away, you put away the product in a staging location.
RFCH
OFFICE
You enter the receipt in ENRE (Enter,
Modify and Delete Receipt).
CHRF
One-step putaway? No Yes
CHRF
ENRE
OFFICE
You confirm the receipt in CHRF (TimeStamp and Confirm Receipt).
OFFICE
You advance the receipt's flow to DRDO (driver arrived at door) in CHRF (TimeStamp and Confirm Receipt).
WAREHOUSE
You unload the receipt in RFCH (RF
Check/Unload).

### Understanding Inbound Flows in RF <a id="understanding-inbound-flows-in-rf"></a>

In non-RF receiving, you time-stamp and advance the flow of a receipt in CHRF (Time-Stamp and Confirm 
Receipts). Advancing the flow of a receipt in CHRF advances the flow of all receipt lines and receipt location lines on the receipt. You cannot advance the flow of one receipt line and leave another receipt line remain at its original flow.
In RF receiving, on the other hand, AccellosOne 3PL automatically advances the flow of individual receipt lines and receipt location lines. For example, when you unload product in RFCH, the receipt line’s flow is automatically advanced from STUN (Start Unloading) to INST (Inbound Staged). Because the flow of individual receipt lines is advanced as each receipt line is unloaded, not all lines on a given receipt will be at the same flow. When this happens, the receipt header will show the earliest flow on the receipt.
For example, suppose there are five receipt lines on a given receipt: two lines are at the flow STUN, two lines are at the flow INST and one line is at the flow STPU (Start Put-Away). If you look up the receipt in LORE, the receipt’s flow will be set to STUN, which is the earliest flow.

### Overview of the Unique Identifier (UI) <a id="overview-of-the-unique-identifier-ui"></a>

The unique identifier (UI) is a single value that represents an inventory entity defined down to the lowest inventory level. For example, the UI value of ABC001 could represent item A1, lot 101, pallet ID 10 belonging to customer A.
Unique Identifiers make it possible to enter a single value in the core RF program such as RFCH, RFPU, 
RFRL, RFRP and RFPIC that identifies the product that you are working with. When you enter this value, 
AccellosOne 3PL automatically populates the customer code and inventory level fields with the correct values.
AccellosOne 3PL can automatically generate these values when you receive inventory in ENRE or you can manually create the values yourself.

RFCH screen showing UI value of GN000286 that identifies three inventory levels

### Unloading Product in RFCH <a id="unloading-product-in-rfch"></a>

In this program, you unload your receipt and place it either in a staging location (if you are going to perform final put-away in RFPU) or in a non-staging location (if you are performing one-step put-away with no processing in RFPU). Your receipt must be at the flow DRDO (Driver Arrived) before you can unload it. If the product that you are receiving is not on the original receipt, you can create a new line for the product in 
RFCH.
RFCH supports two types of receipt lines:
▪ P type in which AccellosOne 3PL generates your pallet ID or you enter your pallet ID’s manually during receipt entry in ENRE (for the purposes of RF, P type includes the following line types in ENRE: I for InTransit, H for Handling Only and S for Storage Only)
▪ U type in which inventory level 2 or higher is unknown at the time of receipt entry (also known as blind receiving)
With P-type lines (that is, all inventory levels have been entered in ENRE), you can enter your lowest inventory level and RFCH will retrieve the receipt number and all other inventory levels. With U-type lines (that is, one or more inventory levels have not been entered in ENRE), you must enter your receipt number and all inventory levels. 
NOTE Depending on how you track your customers’ inventory, the unique identifier may or may not be unique across customers. For example, suppose you have two customers: customer A whose inventory is tracked by item code/lot number/pallet ID and customer B whose inventory is tracked by item code and lot number. Customer A could have “001” as the unique identifier representing a particular pallet ID and customer B could have “001” as the unique identifier representing a particular lot number.
When this happens, if both inventory entities are on open receipts at the appropriate flow, entering “001” in the UI field of RFCH will result in pick list from which the RF operator must select the appropriate inventory. 
CAUTION RFCH does not support multiple operators working on the same receipt when these operators are working in different modes. If you allow multiple operators to work on the same receipt, make sure that all operators are working in the same mode — either unload mode or put-away mode.

REQUIREMENTS — GENERAL
FLOWS DRDO (Driver Arrived at Door)
STUN (Start Unloading)
INST (Inbound Staged)
STPU (Start Put-Away)
PUCO (Put-Away Complete)
INVENTORY LEVELSYou can process up to four inventory levels in RFCH.
PROCESS VALUESIf you wish to scan in a catch weight and serial number, you require two process values: one for catch weights and one for serial numbers. These codes must be set up in IPRO (Item Process) with the Create Automatic Records flag set to Y for 
Yes and then attached to a profile in IPRP (Item Process Profile). The IPRP profile must in turn be attached to the item(s) requiring the process values.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEOnly required if you are scanning process values, inventory levels or UI values from a bar code label
You need a scan parameter profile defined in SCPR (Scan Parameter Code). 
This profile must contain a minimum of two records in the Detail Block: one record for your scanned in weight and another record for your scanned in serial number. 
The SCPR profile must in turn be attached to the item requiring the process values.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code label
You must define a bar code profile in BAPR and attach to it the scan parameter code that you set up in SCPR.
DOCUMENTS The Print Document Without Assigning Locations flag in DOCU (Documents) 
must be set to Yes for all receipt-related documents such as the tally.

OTHER If you want AccellosOne 3PL to generate your pallet ID’s or other inventory levels, you must set the Method of Generating/Validating Values flag in DILP (Depositor 
Inventory Level Profile) to W for Warehouse for that level. As well, the Warehouse 
Code field in the receipt header must be populated. See the Setup Guide for further information on DILP and DIAP.
If you wish to define a default staging and put-away warehouse, you can enter a warehouse code in either the header block of ENRE (for a given receipt) or in 
CUST (for all receipts for a given customer). If you enter a default warehouse code in both ENRE and CUST, the ENRE code will override the CUST code.
If you wish to display a depositor print message set up in DPME, attach a document code of TALY to your message code in DPME. DPME messages for RFCH require specific customer/carrier/shipper combinations; you cannot use the “.ALL” 
codes.
NOTE A DPME message for RFCH does not actually print unless you set up a real tally document in DOCU and then attach this tally document to an inbound flow in DIFP.
RESTRICTIONS RFCH does not support lines that have been partially received in ENRE. A line is considered partially received if you add a location line record in ENRE to a receipt line and the quantity of the location line is less than the full number of units for the receipt line.
REQUIREMENTS — One-Step Manual Put-Away (1)
In one-step manual put-away, you unload your receipt and place it in a final non-staging location with no processing in RFPU. The mode for one-step put-away in RFCH is P for Put-Away and the non-staging location is manually selected by the operator.
FLOWS For one-step manual put-away, the Assign Location flag in DIFP must be set as follows:
ENRE = Y
DRDO = N
STUN = N/A
INST = N/A
STPU = N
PUCO = N
CORE = N/A
NOTE If you wish to perform two-step put-away for some receipts and onestep put-away for other receipts, use the flow settings for two-step put-away.
REQUIREMENTS — GENERAL

AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a new flow and attach it to your inbound flow profile. This flow must be placed before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must be set to Y for Yes.
REQUIREMENTS — One-Step Directed Put-Away (2)
In one-step directed put-away, you unload your receipt and place it in a final non-staging location with no processing in RFPU. The mode for one-step put-away in RFCH is P for Put-Away and the non-staging location is selected by the system. Directed put-away requires special setup in ILOP (Item Location 
Profile) and other programs. See the Allocation and Wave Manager for further information.
FLOWS For one-step directed put-away, the Assign Location flag in DIFP must be set as follows:
ENRE = Y
DRDO = Y
STUN = N/A
INST = N/A
STPU = Y
PUCO = Y
CORE = N/A
NOTE If you wish to perform two-step put-away for some receipts and onestep put-away for other receipts, use the flow settings for two-step put-away.
AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a new flow and attach it to your inbound flow profile. This flow must be placed before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must be set to Y for Yes.
OTHER Put-away parameters must be defined in ILOP (Put-Away).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Manual PutAway (3)
In two-step put-away, you unload your receipt and place it in a staging location before performing final put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and both the staging and non-staging locations are manually selected by the operator. 
REQUIREMENTS — One-Step Manual Put-Away (1)

FLOWS For two-step put-away with manual staging, the Assign Location flag in DIFP must be set as follows:
ENRE = N
DRDO = N
STUN = N
INST = N
STPU = N
PUCO = N
CORE = N/A
REQUIREMENTS — Two-Step Put-Away with Directed Staging and Manual PutAway(4)
In two-step put-away, you unload your receipt and place it in a staging location before performing final put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and the staging location is selected by the system while the final non-staging location is selected by the operator. Directed staging requires special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave 
Manager Guide for further information.
FLOWS For two-step put-away with directed staging, the Assign Location flag in DIFP must be set as follows:
ENRE = N
DRDO = Y
STUN = Y
INST = N
STPU = N
PUCO = N
CORE = N/A
ALLOCATION Directed staging requires warehouse zones set up in WHZO (Warehouse Zone 
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER Directed Move Inbound parameters must be defined in ILOP (Directed Move 
Inbound).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Manual PutAway (3)

REQUIREMENTS — Two-Step Put-Away with Directed Staging and Directed 
Put-Away (5)
In two-step put-away, you unload your receipt and place it in a staging location before performing final put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and both the staging and final locations are selected by the system. Directed put-away requires special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave Manager Guide for further information.
If you switch from two-step put-away to one-step put-away in RFCH and if you are processing a P-type line, AccellosOne 3PL will use your directed move parameters rather than your directed put-away parameters.
FLOWS For two-step put-away with directed staging and put-away, the Assign Location flag in DIFP must be set as follows:
ENRE = N
DRDO = Y
STUN = Y
INST = Y
STPU = Y
PUCO = Y
CORE = N/A
ALLOCATION Directed put-away requires warehouse zones set up in WHZO (Warehouse Zone 
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER The following parameters must be defined: Directed Move Inbound in ILOP (Directed Moved Inbound) and Put-Away in ILOP (Put-Away).
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Directed PutAway (6)
In two-step put-away, you unload your receipt and place it in a staging location before performing final put-away in RFPU. The mode for two-step put-away in RFCH is U for Unload and the staging location is selected by the operator while the final location is selected by the system. Directed put-away requires special setup in ILOP (Item Location Profile) and other programs. See the Allocation and Wave Manager Guide for further information.

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
Codes). The zone type code must be set to P (P & D) or S (Sorting) and the staging location must be defined in the Header Block of WHZO.
OTHER Put-Away parameters must be defined in ILOP (Directed Move Inbound).
REQUIREMENTS — Three-Step Put-Away (7)
In three-step put-away, the product is received and staged on the dock, moved to a PnD location by a forklift operator and then moved to a final put-away location by a narrow aisle equipment (VNA) operator.
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
REQUIREMENTS — Two-Step Put-Away with Manual Staging and Directed PutAway (6)

LOTP The PnD location’s location type must be set up in LOTP as follows:
.
OTHER Put-Away parameters must be defined in ILOP (Directed Move Inbound).
MRFP In the Special Receiving Mode Types field in MRFP, you select from the following three-step put-away options:
▪ RFCH to General Staging Location, RFPU to a PnD Location, then to Final 
Location
▪ RFCH to Gen Stag Loc, RFPU to PnD Loc, then to Final Loc, RFCH Overrides
If you select the first option, three-step put-away is mandatory in RFCH. If you select the second option, the RF operator can select either two-step or three-step put-away in RFCH.
In the Picking Rules for PnD Locations field in MRFP, you define your pick methods for these types of locations: full pallet picks only or all pick methods.
FUNCTION KEYS
Criteria Mode
F2 EQ (Execute Query) Searches for the record(s) that meet the criteria that you specify in Criteria mode.
F4 EX (Return to Main) Switch to Main Mode.
REQUIREMENTS — Three-Step Put-Away (7)

1 Make sure that your receipt is at the flow DRDO or STUN.
2 Enter RFCH.

RFCH screen
Results Mode
F1 CL (Create Line) Create a new line.
F1 RM (Remark) Show remark(s) entered in ENRE.
F2 PL (Print Label) Print labels.
F3 CM (Change Mode) Switch between put-away mode and unload mode.
F3 CR (Close Receipt) Close a receipt with unprocessed lines. 
Supervisor access required.
F4 RT (Exit) Switch to Main Mode.
F9 Move cursor to previous field.
Main Mode
F1 PL (Print Label) Print labels.
F2 QS (Query) Query receipts.
F4 EX (Exit) Exit program.
FUNCTION KEYS

3 Do one of the following:
If you are processing a P-type line:
You have two options: 
a) You can enter or scan in your UI (Unique Identifier) 
value and AccellosOne 3PL will retrieve the receipt number and up to four inventory levels for that UI value. If you have the same UI value on multiple receipts, a pick list will appear showing the receipt number and level 1/2/3/4 values. Use your arrow keys to position the cursor over the receipt that you wish to process and press F3 to select it.
b) You can bypass the UI field and enter the receipt number and level 1, 2, 3 and 4 values yourself. 
If you are processing a U-type line from ENRE with no systemgenerated inventory levels:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Key in your level 1 value for the first product that you wish to receive and press Enter.
d) Key in your level 2 value and press Enter.
e) Key in your level 3 value and press Enter.
f) If required, key in your level 4 value and press Enter.
If you are processing a U-type line from ENRE with the lowest inventory level system generated:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Key in your level 1 value for the first product that you wish to receive and press Enter.
d) Repeat the above step for each additional inventory level until you reach your lowest level.
e) When you reach your lowest inventory level, you have two options: you can manually enter it and press Enter as you did with your higher inventory levels or you can press Enter with the field blank and AccellosOne 3PL will generate a number for you.
If you are processing a U-type line from ENRE and you are scanning in your inventory levels from one or more bar code labels:
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Scan in your level 1, 2 and 3 values from the appropriate label. If RFCH displays a pick list of bar code labels, select the appropriate label from the pick list.
If you do not know the UI number or receipt number:a) See [Performing Queries](expedicao-rf.html#performing-queries).

4 Do one of the following:
RFCH screen showing prompt for tie and hi
5 Depending on your system setup, RFCH will be preset to either put-away mode or unload mode. If required, you can press F3 (CM) to toggle between the two modes.
Once you process a receipt line, the mode is set for all remaining lines on the receipt and cannot be altered until you start a new receipt.
If manual entry of expiry dates is activated for the item and you are receiving a U-type line:
If manual entry of expiry dates is 
NOT activated for the item:
a) The following screen will appear:
b) Key in your expiry date in the format displayed on your screen and press Enter.
a) Proceed to next step.
NOTE If you have manually entered a location in ENRE for one receipt line belonging to a multi-line receipt, the mode for the remaining receipt lines will be preset to put-away and cannot be changed. To switch to unload mode, you will have to remove the location from the receipt line in ENRE and then return to RFCH.
MODE field shows current mode: 
P = Put-Away (one-step)
U = Unload (two-step)

6 Do one of the following:
7 If the quantity entered does not match the expected quantity, a warning message will appear (“Qty 
Entered Does Not Match Expected Qty. Do You Want to Continue (Y/N)”) and you will be prompted to either continue with the current receipt or work on another receipt.
8 Do one of the following: 
9 If F1 (Rm) is available, the receipt has remarks. You can press F1 to view the remarks and then press F4 to exit the Remarks Block.
If you wish to enter your tie, hi and loose values and let 
AccellosOne 3PL calculate the quantity:
If you wish to enter the total quantity directly:
a) Key in your tie and press Enter.
b) Key in your hi and press Enter again.
c) If you have loose quantities, key in your loose quantity and press 
Enter. If you do not have loose quantities, press Enter with the 
L(oose) field blank to bypass this option.
Depending on your setup in MRFP, the quantity may or may not be displayed in the Qty field.
a) Press Enter to bypass the T(ie) 
field.
b) Key in your quantity and press 
Enter. You can enter your quantity in pallets, eaches or any other SKU type that is activated in the item’s quantity breakdown. 
If your default SKU type is eaches and you wish to enter a quantity of 10 pallets, you would key in 10P for 10 pallets.
c) If the quantity is already displayed, press Enter to accept it or key in a new quantity and press Enter.
If the item that you are receiving requires the entry of a process code value:
If the item that you are receiving does NOT require the entry of a process code value:
a) Refer to the section [Entering 
Process Values](recebimento-rf.html#entering-process-values) for further instructions.
a) Proceed to next step.

10 Do one of the following:
11 Proceed to assign a location to the product as follows. If you are working in unload mode, the product must be placed in a staging location. A staging location is a location whose location type in LOTP is called STAG. This STAG code must have the Staging flag set to Y for Yes. 
If you are working in put-away mode, the product must be placed in a non-staging location. A non-staging location is a location whose location type in LOTP has the Staging flag set to N for No.
If there is no automatic hold placed on the item:
If there is an automatic hold placed on the item and manual overrides of holds are activated:
If there is an automatic hold placed on the item and manual overrides of holds are NOT activated:
a) If required, key in your manual hold code and press Enter. If you do not want to place the product on hold, press Enter to bypass this field.
a) If required, you can manually override or remove the hold code. Make any necessary changes and press Enter or press Enter without making any changes to accept the automatic hold.
a) The cursor will skip past the 
Hold field and you will not be able to override or remove the hold code.

If directed staging/put-away is activated on your system:
If directed staging/put-away is 
NOT activated on your system:
AccellosOne 3PL will display the system-assigned warehouse and location. You can accept the system-assigned warehouse and location or you can enter a different warehouse and location
If you wish to override the systemassigned location, see [Overriding the System-Assigned Location](recebimento-rf.html#overriding-the-system-assigned-location).
RFCH screen showing systemassigned warehouse and location
a) Press Enter to accept the system-assigned location.
b) Press Enter again to accept the warehouse that the systemassigned location belongs to.
a) Key in your location and press 
Enter.
b) If required, key in your warehouse and press Enter.
c) If you wish to change your location code, press F9 to return to the L(oc) field. Then repeat steps a and b. 

RFCH screen showing prompt for next UI
12 If required, you can press F9 to return to the Hold field and place the product on hold.
13 Repeat the above steps for any additional UI’s or receipt lines.
14 When you finish entering all the lines on the receipt, do one of the following:
If you have fully entered all lines on the receipt:
If you are an operator (or nonsupervisor) and you have NOT fully entered all lines on the receipt:
If you are a supervisor, if you have NOT entered all lines on the receipt and if you press F3 (CR):
a) Proceed to next step. The following message will appear: 
RFCH screen showing prompt to complete process
a) Press Enter to exit the receipt line. You can return to RFCH at any time and resume processing the receipt line.
The following message will appear: 
RFCH screen showing warning for not all lines processed
a) If you key in Y for Yes to proceed, the system will zero out any lines not unloaded or putaway, advance to the next flow and check for variances. If you key in N for No, proceed to enter the missing lines.

RFCH screen showing “Receipt completed?” message
15 Key in the appropriate option (1 to mark the receipt as complete, 2 to add a new line or 3 to exit and return at a later time to add a new line) and press Enter.
16 Process another receipt or press F4 to exit.

### OVERRIDING THE SYSTEM-ASSIGNED LOCATION <a id="overriding-the-system-assigned-location"></a>

There are three options for overriding the system-assigned location for a receipt line depending on your setup in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to No, an operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Override in RFCH/RFPU/RFRL flag in MRFP is set to Yes, changing a location must be approved by a supervisor
▪ if the Reason Code Required to Override System-Assigned Location flag in MRFP is set to Yes, the RF operator will be required to enter a reason code
1 Enter your receipt in RFCH in the normal manner.

RFCH screen showing system-assigned location
2 Key in your new location and press Enter.

3 Do one of the following:
4 Proceed to process the receipt normally in RFCH.

### ENTERING TRAILER AND PALLET INFORMATION <a id="entering-trailer-and-pallet-information"></a>

If trailer and pallet information entry is activated in MRFP (RFCH Only tab) by setting the Show Temperature and Pallet Blocks flag to the appropriate option, you will be prompted to enter trailer and pallet information for the receipt. If the Perform Trailer Checks flag in MRFP is set to Yes, you will be prompted to perform a series of trailer checks.
Any trailer and temperature information that you enter in RFCH for a given receipt can be viewed in the 
Carrier Details Block of ENRE and LORE. Likewise, any pallet information that you enter in RFCH can be viewed in Pallet Details Block of ENRE and LORE.
1 When you finish processing all UI’s or receipt lines, the following screen will appear:
If supervisor authorization is activated:
If supervisor authorization is 
NOT activated:
The following screen will appear:

a) Key in Y for Yes and press Enter to proceed with the location override. If you do not wish to proceed with the override, key in N for No and press Enter to return to the main RFCH screen.
b) Have a supervisor log in to approve the location override.
The following screen will appear:

a) Key in Y for Yes and press Enter to proceed with the location override. If you do not wish to proceed with the override, key in N for No and press Enter to return to the main RFCH screen.
b) Press Enter again to accept the warehouse that the systemassigned location belongs to.

RFCH screen showing prompt for temperature
2 Do one of the following:
3 If the entry of trailer checks is activated in MRFP, you will be prompted to perform a series of trailer checks.

RFCH screen showing trailer check
4 Proceed to respond with either a Yes or a No to each trailer check.
If you wish to record the temperatures and trailer number for the load:
If you do NOT wish to record the temperature and trailer number for the load:
a) Key in the required number of temperatures for your trailer and press Enter. You can skip a particular temperature by pressing 
Enter with the field blank.
b) If required, key in your trailer number and press Enter. If you do not wish to enter a trailer number, press Enter to exit the 
Temperature/Trailer prompt.
c) If required, key in your seal number and press Enter.
a) Press F4 to exit.
b) Proceed to step 15. You will not be prompted to enter pallet information.

5 If the Pallet Block appears, do one of the following:

RFCH screen showing the Pallet Block
6 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
7 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
8 Key in your pallet code and press Enter or use your pick list to select it.
9 Key in the number of pallets that you are shipping or receiving and press Enter.
If you wish to record pallet information for the load:
If you do NOT wish to record pallet information for the load:
a) Proceed to next step. a) Press F4 the required number of times to exit the Pallet Block.
b) When the temperature and trailer number prompts redisplay, press 
F4 to exit. Then proceed to step 
15.
Received Received means that you are receiving pallets from the account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 of your own pallets so that there is no change to your pallet balances.

RFCH screen showing prompt for reference information
10 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not require a remark, press Enter to bypass this field.
11 If required, repeat the above steps to add additional lines in the Pallet Block.
12 When you finish adding your lines, press F4 to exit Create Mode. AccellosOne 3PL will display the last pallet details record that you entered. If you have multiple pallet transactions for this receipt, you can use your up and down arrow keys to scroll through the list of records.
If you wish to delete a pallet transaction, select the transaction that you wish to delete with your arrow keys. Then press Enter until your cursor is positioned in the NUM PALL field and press F2 (DE).
13 Press F4 again to exit the Pallet Block.
AccellosOne 3PL will redisplay the prompt for the temperature and trailer number.
14 Press F4 to exit this screen.

RFCH screen showing message that receipt has been processed
15 Press Enter to close the “Process Complete” message. If prompted to mark the receipt as completed or to create a new line, key in Y for Yes to complete the receipt and press Enter.
16 Press F4 to exit.

### PERFORMING QUERIES <a id="performing-queries"></a>

The query function in RFCH allows you to query by receipt number, receipt line number, customer, inventory level, warehouse, hold code and shipper. In order to query a receipt in RFCH, the receipt must be at the flow 
DRDO (Driver Arrived at Door) without being fully staged or put-away. 
You can customize the values that appear in the query results screen by setting the appropriate flags in 
MRFP (RF Profile Code) to Yes. For example, if you wish to see the customer code and level 1 value only in the query results, you would set the Show Customer Code in RFCH Query and Show Inventory Level 1 in 
RFCH Query fields to Yes.
1 Enter RFCH.
2 Press F2 (QS).

RFCH screen showing Enter Criteria screen
3 Key in your search criteria and press F2 (Execute Query).

RFCH screen showing six records in pick list
4 Use your arrow keys to scroll through the list of records retrieved. If you wish to jump forward by ten records, press F1 (JF). If you wish to jump backwards by ten records, press F2 (JB).
5 When you find the line that you wish to select, press F3 to select it.
6 Continue to process the receipt normally.

### ENTERING PARTIAL U-TYPE RECEIPT LINES <a id="entering-partial-u-type-receipt-lines"></a>

You can enter partial U-type receipt lines in RFCH by entering the partial quantity (for example, 10 cases) and then keying in N for No when prompted to complete the process. You use partial receipt lines when product on a trailer is dispersed and you are not sure whether you have processed all product belonging to a particular inventory entity. You also use partial receipt lines when you wish to place part of a receipt on hold; 
for example, you receive a pallet of 100 cases and 20 cases are damaged.
When you enter partial receipt lines in RFCH, two lines are created in ENRE/LORE. The first line shows the number of units actually received and the second line shows the remaining number of units. For example, if your expected quantity is 100 and your received quantity is 10, the following receipt lines will be created:
▪ line 1: expected qty = 100, received qty = 10
▪ line 2: expected qty = 0, received qty = 90
If you receive additional units of the same product, line 2 will show the new quantity received and line 3 will show the new remaining number of units.
EXAMPLE
1) You received 10 units out of an expected quantity of 100.
2) You receive 20 more units of the same product.
3) You receive 50 more units.
Expected Received Location line 1 100 10 STAG line 2 0 90
Expected Received Location line 1 100 10 STAG line 2 0 20 STAG line 3 0 70
Expected Received Location line 1 100 10 STAG line 2 0 20 STAG line 3 0 50 STAG line 4 0 20

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

### PRINTING LABELS <a id="printing-labels"></a>

Printing labels requires a document set up by HighJump in DOCU (Documents).
1 Enter RFCH.
2 Press F1 (PL).

RFCH screen showing Print Label Block
3 Key in your receipt number and press Enter.
4 Enter or scan in your level 1 value.
5 If required, enter or scan in your level 2, level 3 and level 4 values.
Expected Received Location line 1 100 10 STAG line 2 0 20 STAG line 3 0 50 STAG line 4 0 20 STAG

RFCH screen prompt for quantity
6 Key in the number of labels that you wish to print for this inventory entity and press Enter.
7 Key in your printer code and press Enter.
8 Repeat the above steps for each additional label that you wish to print or press F4 the required number of times to exit.

### UNDERSTANDING VARIANCES IN RFCH <a id="understanding-variances-in-rfch"></a>

A variance occurs when the quantity actually received does not match the quantity on the receipt. There are two ways of calculating variances depending on the type of line:
▪ If all inventory levels are entered during receipt entry (that is, a P-type line), variances are calculated at the line level (that is, the lowest inventory level).
▪ If not all inventory levels are entered during receipt entry (that is, a U-type line), variances are calculated at the next highest level that is known. For example, if levels 1 and 2 are known and level 3 is unknown, the variance will be calculated for inventory level 2. If, however, level 1 is known and levels 2 and 3 are unknown, the variance will be calculated for inventory level 1.
For example, suppose you received the following product on the same receipt and level three (pallet ID) is system-generated:
If you enter a quantity of 85 for line 1 and a quantity of 65 for line 2, no variance will occur in RFCH because the total (85 + 65 = 150) equals the total in ENRE for item A1, lot 101.
If you enter a quantity of 120 for line 1 and a quantity of 45 for line 2, a variance will occur in RFCH because the total (120 + 45 = 165) does not equal 150. If you accept the variance of 15 units, the extra 15 units will be 
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

applied to line 1; you cannot split an overage or adjustment between two pallet ID’s belonging to the same lot number.

### PROCESSING VARIANCES <a id="processing-variances"></a>

If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Must Match ENRE”, you cannot enter variances in RFCH. When the quantity received does not match the quantity on the receipt, the following message will appear and you must either enter the correct quantity or exit the receipt line.

RFCH screen showing “Qty entered does not match expected qty” message
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching not required”, you can enter variances in RFCH. Variance processing in RFCH is dependent on whether or not the operator has supervisory privileges.
1 Make sure that the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching not required”.
NOTE All variances in RFCH are shown in the lowest SKU. For example, if your item is a pallet/case/each item, any variances will be shown in eaches — not pallets or cases.
Operator is NOT a Supervisor Operator is a Supervisor variance is a shortage “Receipt not completed yet” message appears when you exit the receipt and 
AccellosOne 3PL creates a second line in 
ENRE for the missing product. Operator can return to the receipt at any time to enter the missing product or office staff can delete the second line.
“Complete Process” message appears and supervisor is prompted to zero out the lines. 
If the supervisor selects Yes, Variance screen appears and supervisor is prompted to accept the shortage. No second line is created in ENRE for the missing product. 
variance is an overage If you enter all your inventory levels manually, Variance screen appears when you enter your quantity. If you do not enter all your inventory levels manually (that is, a Utype lines), Variance screen appears when you exit the receipt. In the Variance screen, operator is prompted to accept the overage. 
In ENRE, received quantity is greater than expected quantity.
Same as operator or non-supervisor.

2 Enter RFCH.
3 Enter or scan in your UI value or enter your receipt number and all known inventory levels of the product that you are receiving.
4 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and press Enter to bypass these fields.
5 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in a new quantity and press Enter.
6 Do one of the following:
7 Proceed to enter your hold code (if any) and location information for the receipt and then perform the remaining steps in RFCH normally.
8 When you finish processing all your receipt lines, press F4 to switch to main mode.
If the variance is a shortage: If the variance is an overage:
a) Proceed to next step. a) The following screen will appear: 
RFCH screen showing Variance screen
b) Key in Y for Yes to accept the variance or key in N for No to reenter a new received quantity.

9 Do one of the following:

### ENTERING PROCESS VALUES <a id="entering-process-values"></a>

If the capture of process values is activated for the product that you are receiving, you will be prompted to enter process values under the following conditions:
If you have supervisor privileges:
If you do NOT have supervisor privileges:
The following screen will appear:

a) Key in Y for Yes and press Enter to zero out all lines.
b) When prompted to confirm the zero out, key Y for Yes and press 
Enter.
c) If the variance is a shortage, the following screen will appear.

d) Press F3 (ZO) to accept the shortage.
e) Press Enter to continue.
The following screen will appear:

a) Press Enter to acknowledge the incomplete receipt messsage.

▪ there are no process values for the receipt line that you are processing
▪ there are missing process values for the receipt line that you are processing
▪ the quantity received in RFCH does not match the quantity recorded in ENRE (any existing process values will be erased and new values must be entered)
If you are unable to scan in each case ID on the pallet for any reason, AccellosOne 3PL will present you with the following options:
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all inventory levels of the product that you are receiving.
3 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and press Enter to bypass these fields.
4 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in a new quantity and press Enter.

RFCH screen showing prompt for process value
5 Key in your first value and press Enter or scan it in using your RF gun.
6 If you are capturing multiple process values, repeat the above step for each additional process value.
7 If you wish to interrupt your scanning for any reason, press F4.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will remove unscanned quantities from the receive quantity. You cannot process the receipt line again in RFCH.
4 (Exit, Save) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned. You cannot process the receipt line again in RFCH.
5 (Exit, No Save) Cease scanning and exit without saving any process values including those already scanned. You cannot process the receipt line again in RFCH.

RFCH screen showing incomplete scan message
8 Do one of the following:
9 Continue to process the receipt normally.

### VALIDATING PROCESS VALUES <a id="validating-process-values"></a>

If you set the Validate One Process Value flag to Y for Yes, you will be prompted to validate the serial number and other information such as level 1 and 2 values in bar code labels. You validate process values by scanning in one label from each pallet; if the label is not valid, you will not be allowed to complete the receipt in RFCH.
Validation will only occur for P-type receipt lines when the full quantity is received and all process values have been entered or scanned in. 
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all inventory levels of the product that you are receiving.
If you wish to continue from where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the received quantity:
Key in 3 and press Enter.
When prompted to short the receipt line, key in Y for 
Yes and press Enter.
If you wish to exit and save the scanned process values:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values:
Key in 5 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

3 Key in your tie, hi and loose values. If you do not wish to record these values, leave the tie field blank and press Enter to bypass these fields.
4 Key in your quantity and press Enter. If the quantity is already displayed, press Enter to accept it or key in a new quantity and press Enter.

RFCH screen showing prompt to scan any case
5 Scan in any case on the pallet.
6 Continue to process the receipt line normally in RFCH.

### CREATING A NEW LINE <a id="creating-a-new-line"></a>

If the product that you are receiving is not on the original receipt, you can create a new line for the product in 
RFCH. When you create a new line in RFCH, AccellosOne 3PL creates a new line for the receipt in ENRE in which the expected quantity and received quantity equal the quantity that you entered in RFCH. If an inventory level is system-generated, AccellosOne 3PL will generate the appropriate value for that inventory level.
Creating a new line is only allowed if the Allow New Lines flag in MRFP is set to Yes for the customer whose product you are receiving.
1 Enter RFCH.
2 Press Enter to bypass the UI field.
3 Key in your receipt number and press Enter.
4 Key in your level 1 value for the item that you wish to receive and press Enter. 

5 Do one of the following:
6 With your cursor positioned in the field for your lowest inventory level, press F1 (CL). AccellosOne 3PL will display the following message. 

RFCH screen showing prompt to create a new line
7 Do one of the following:
8 Proceed to enter the receipt normally.

### RECEIVING PRODUCT UNDER AN ALTERNATE ITEM CODE <a id="receiving-product-under-an-alternate-item-code"></a>

An alternate item code is a second or alternate name for an item. For example, you receive product under the code ABC and then you store it and ship it in AccellosOne 3PL under the code 001. 
Alternate item codes must be set up in ALIT (Alternate Item and Language). Refer to the Setup Guide for further instructions on setting up ALIT.
If you enter all inventory levels during receipt entry:
If your lowest inventory level is system generated:
a) Key in all inventory levels for the item.
a) Key in all inventory levels for the item except the last level. For example, if you are receiving a three-level item, you would enter the second inventory level but not the third. If you are receiving a four-level item, you would enter the second and third inventory levels but not the fourth.
If you wish to create a new line:
If you do NOT wish to create a new line:
a) Key in Y for Yes and press Enter.
b) Key in your quantity and press 
Enter.
a) Key in N for No and press Enter.
b) Re-enter the inventory level that triggered the “Create a New 
Line?” prompt.

ALIT screen showing ALT_ITEM as an alternate item code for item D1
1 Make sure that your receipt is at the flow DRDO (Driver Arrived at Door).
2 Enter RFCH.

RFCH screen

3 Do one of the following:

RFCH screen showing prompt for tie and hi
4 Proceed to process your receipt in the normal manner.

### RECEIVING PRODUCT ON AUTOMATIC HOLD <a id="receiving-product-on-automatic-hold"></a>

If you are receiving product on automatic hold, you can override or remove the automatic hold if the Allow 
Override of Hold Code During Core RF Receiving field in IHOP (Item Hold Profile) is set to Yes. If you set this flag to No, you will not be able to override or remove automatic holds. The profile that you set up in IHOP must be attached to the appropriate item in ITEM.
If you are receiving an item with a single inventory level:
If you are processing a P-type line containing an item with multiple inventory levels:
If you are processing a U-type line containing an item with multiple inventory levels:
a) Enter or scan in your alternate item code in the UI field. The system will convert the alternate item code to the regular 
AccellosOne 3PL item code. 
a) Enter or scan in your UI value. 
The system will retrieve the receipt number and three inventory levels for that UI value. The alternate item code will be converted to the regular 
AccellosOne 3PL item code.
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Enter or scan in your alternate item code. The system will convert the alternate item code to the regular AccellosOne 3PL item code.
d) Enter or scan in your remaining inventory levels.

IHOP screen showing Allow Override of Hold Code During Core RF Receiving field set to Y for Yes

### RECEIVING PRODUCT WITH A VARIABLE PRODUCT BREAKDOWN <a id="receiving-product-with-a-variable-product-breakdown"></a>

If you are receiving product with a variable quantity breakdown in RFCH, you must enter your quantity in the lowest SKU.
1 Enter RFCH.
2 Press Enter to bypass the UI (Unique Identifier) field. 
3 Key in your receipt number and press Enter.
4 Enter or scan your level 1 value for the first product that you wish to receive.
5 Enter or scan in your level 2 value. If required, enter or scan in your level 3 and level 4 values.
6 Depending on your system setup, RFCH will be preset to either put-away mode or unload mode. If required, you can press F3 (CM) to toggle between the two modes.
Once you process a receipt line, the mode is set for all remaining lines on the receipt and cannot be altered until you start a new receipt.
7 Key in your tie, hi and loose values. If you do not wish to record these values, press Enter three times to bypass these fields.
8 Key in your quantity in the lowest SKU and press Enter.
9 Continue to process the receipt normally in RFCH.

### RECEIVING MIXED PRODUCT <a id="receiving-mixed-product"></a>

You can receive mixed product on a single pallet without the need to scan in each unique inventory entity. For example, you have two receipt lines in ENRE with the same level 1 and 3 values (item code and pallet ID), but different level 2 values (date code). When you scan in the level 3 value in RFCH, you will be prompted to choose between full pallet receiving (process the pallet once as if the product was not mixed) or regular receiving (process each receipt line separately).

Receiving mixed product on a single pallet requires that the Receipt Reference Number field in ENRE be populated with the level 3 or 4 value that you scan in RFCH.
1 Enter RFCH.
2 Enter or scan in your UI value or enter your receipt number and all known inventory levels of the product that you are receiving.

RFCH screen showing three inventory entities on the same pallet
3 Press F3 (Sl) to select the first line.

RFCH screen showing mixed pallet message
4 Do one of the following:
If you wish to perform full pallet receiving:
If you wish to perform regular receiving:
a) Key in Y for Yes and press Enter.
b) Proceed to enter the quantity and location for the full pallet.
c) If prompted to do so, enter your trailer and pallet information in the normal manner.
a) Key in N for No and press Enter.
b) Proceed to enter the quantity and location for the first inventory entity on the pallet.
c) Repeat the previous step for each additional inventory entity on the pallet.
d) If prompted to do so, enter your trailer and pallet information in the normal manner.

### LOOKING UP TEMPERATURE AND TRAILER INFORMATION IN LORE <a id="looking-up-temperature-and-trailer-information-in-lore"></a>

If you entered a temperature and trailer number in RFCH, you can look up this information in the Carrier Block of LORE.
1 Enter LORE.
2 Retrieve the receipt whose temperature and trailer information you wish to look up.

LORE screen showing receipt number 4
3 Make sure that the value in the Carrier Details field is E for Entered.
4 Press Enter to position your cursor in the Carrier Details field.
5 Click on Carrier Details.

Carrier Details block of LORE showing trailer number and temperature
6 Click on Return to exit the Carrier Details Block. Then click on Exit to exit.

### LOOKING UP REMARKS AND MESSAGES IN RFCH <a id="looking-up-remarks-and-messages-in-rfch"></a>

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
1 Enter RFCH and retrieve the receipt whose remarks/messages you wish to look up. The remark/message will display automatically when you retrieve the receipt.

RFCH screen showing header and line remarks
2 If the remarks are more than six lines long, use your up and down arrow keys to scroll through the remark lines.
3 If there are multiple remarks/messages attached to the receipt, press Enter or F4 to jump to the next message.
4 Continue to process the receipt normally.

### Entering Temperature and Trailer Information in RFTT <a id="entering-temperature-and-trailer-information-in-rftt"></a>

This program allows you to enter temperature, trailer/seal number and pallet information for a given receipt or order without working in RFCH or RFPIC. The information that you can enter in RFTT — temperature only, trailer/seal number only, temperature and trailer/seal number, etc. — depends on which option you choose in the Show Temperature and Pallet Blocks field in MRFP and which value if any you enter in the Num of Temp. 
field in LOAD.
1 Enter RFTT.
RFTT screen
2 Key in your receipt number and press Enter.

3 Enter your temperature, trailer/seal number and pallet information in the usual manner.

### Putting Away Product in RFPU <a id="putting-away-product-in-rfpu"></a>

You put away your product in RFPU. RFPU can only be used after unloading the product in RFCH. If you wish to put-away product without unloading it, you must perform one-step put-away in RFCH.
When putting away product, you can enter the exact quantity (that is, the expected quantity equals the received quantity), an overage or a shortage and, if required, you can place product on a manual hold. You can also split a line; that is, if your receipt line has 50 units, you can put-away 30 units today in one location and put-away the remaining 20 units at a later time in the same location or in another location.
There are four different hold options in RFPU:
If directed put-away is activated on your system, the system-assigned warehouse and location will be displayed. You can accept the system-assigned warehouse and location or you can enter a new warehouse and location. If directed put-away is not activated on your system, you must enter your put-away location and warehouse manually. You can eliminate the need to enter a warehouse in RFPU by defining a default warehouse in the header block ENRE (for a given receipt) or in CUST (for all receipts from a given customer). 
If automatic confirmation is activated, RFPU advances the receipt’s flow to CORE. Therefore, you cannot work on or make adjustments to the receipt after processing it in RFPU.
If you enter a shortage … You can place a manual hold on the difference between the expected quantity and the received quantity. For example, if the quantity staged in RFCH is 100 units and you enter 80 for the same receipt line in RFPU, AccellosOne 3PL will place 20 units on the hold that you specify.
If the entire receipt line is damaged or requires special processing …
You can place an entire receipt line on a manual hold.
If you enter a shortage and the non-shortage part of the receipt line is damaged or requires special processing …
You can place two manual holds on the same receipt line: one hold for the variance quantity and a second hold for the non-variance quantity.
If automatic holds are activated for the product …
If manual overriding of holds is activated in IHOP, you can manually override or remove the hold code. If manual overriding of holds is 
NOT activated in IHOP, you cannot override or remove the hold code.
REQUIREMENTS
FLOWS See [Unloading Product in RFCH](recebimento-rf.html#unloading-product-in-rfch) for further information.

1 Make sure that your receipt in ENRE is at one of the following flows: DRDO (Driver at Door), STUN (Start 
Unloading), INST (Inbound Staged) or STPU (Start Put-Away).
2 Enter RFPU.
LINE TYPES RFPU requires P-type lines unless U-type lines have been received with a quantity of zero.
AUTO-CONFIRMATIONIf you wish to deactivate automatic confirmation of receipts, you must create a new flow and attach it to your inbound flow profile. This flow must be placed before CORE (Confirm Receipt) and the Mandatory flag for this flow in DIFP must be set to Y for Yes.
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

RFPU screen
3 Do one of the following:

RFPU screen showing receipt 5
If you know the UI value of the product that you are putting away:
If you do NOT know the UI value of the product that you are putting away:
a) Enter or scan in your UI value. 
You can also select your UI value using the pick list function. If there are multiple receipts attached to the same UI, receipts will display in location order not receipt number order.
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Key in your level 1 value for the first product that you wish to receive and press Enter.
d) Key in your level 2 value and press Enter.
e) Key in your level 3 value and press Enter.
f) If required, key in your level 4 value and press Enter.

4 If F1 (Rm) is available, the receipt has remarks. You can press F1 to view the remarks and then press F4 to exit the Remarks Block.
5 Key in the quantity that you are receiving and press Enter. You can enter your quantity in pallets, eaches or any other SKU type that is activated in the item’s quantity breakdown. If your default SKU type is eaches and you wish to enter a quantity of 10 pallets, you would key in 10P for 10 pallets.
6 Do one of the following:

RFPU screen showing variance options
7 Do one of the following:
If the quantity matches the quantity of the receipt line in 
RFCH:
If the quantity does NOT match the quantity of the receipt line in 
RFCH:
a) Proceed to step 9. The message “This receipt line has a variance. Accept? (Y/N/H/V)” will appear.
a) Proceed to next step.
If the variance is a shortage and you wish to ignore it for now because you expect to receive more product:
▪ Key in Y for Yes and press Enter.
AccellosOne 3PL will create a new receipt line for the difference.
If you wish to reject the variance and re-enter the quantity:
▪ Key in N for No and press Enter.
▪ Re-enter your quantity.
If the variance is a shortage and you wish to place the variance quantity on hold:
▪ Key in the H for Hold and press Enter.
▪ Key in your hold code and press Enter.
AccellosOne 3PL will place the variance quantity on the hold type that you specify.
If you wish to accept the variance:
▪ Key in V for Variance and press Enter.
AccellosOne 3PL will short the line without creating a new receipt line.

RFPU screen showing prompt for hold code
8 Do one of the following:
If there is no automatic hold placed on the item:
If there is an automatic hold placed on the item and manual overriding of holds is activated:
If there is an automatic hold placed on the item and manual overriding of holds is NOT activated:
a) If you wish to place the product on manual hold, press F9 to position your cursor in the 
Hold field. Then key in your manual hold code and press 
Enter.
▪ The hold that you enter in this field applies to the entire receipt line — if you did not record a variance in the 
Quantity field — or the difference between the variance and the expected quantity — if you did record a variance in the Quantity field.
a) If required, you can manually override or remove the hold code. Make any necessary changes and press Enter or press Enter without making any changes to accept the automatic hold.
a) The cursor will skip past the 
Hold field and you will not be able to override or remove the hold code.
current staging location for product

9 Do one of the following:
10 Repeat the above steps for the each additional receipt line that you wish to put away.
11 When all your lines have been put-away, the following message will appear:
If directed put-away is activated on your system:
If directed put-away is NOT activated on your system:
AccellosOne 3PL will display the system-assigned warehouse and location. You can accept the system-assigned warehouse and location or you can enter a different warehouse and location.
If you wish to override the systemassigned location, see [Overriding the System-Assigned Location](recebimento-rf.html#overriding-the-system-assigned-location).

RFPU screen showing systemassigned warehouse and location
a) Press Enter to accept the system-assigned location or press 
F3 (NX) to display a second suggested put-away location. If the second suggested put-away location is not acceptable, press 
F3 (NX) again to see a third suggested put-away location.
b) Press Enter again to accept the warehouse that the systemassigned location belongs to.
a) Key in your location and press 
Enter.
b) If required, key in your warehouse and press Enter. You will not need to enter a warehouse if you defined a default warehouse in either ENRE or CUST.
F = from location
S = system location
T = to location

 RFPU screen showing the “Receipt Put-Away” message
12 Press Enter to accept the message then process another receipt or press F4 to exit.

### OVERRIDING THE SYSTEM-ASSIGNED LOCATION <a id="overriding-the-system-assigned-location"></a>

There are three options for overriding the system-assigned location for a receipt line depending on your setup in MRFP (RF Profile): 
▪ if the Supvr. Must Authorize Location Overrides in RFCH/RFPU/RFRL flag in MRFP is set to No, an operator can change a location without authorization of a supervisor
▪ if the Supvr. Must Authorize Location Overrides in RFCH/RFPU/RFRL flag in MRFP is set to Yes, changing a location must be approved by a supervisor
▪ if the Reason Code Required to Override System-Assigned Location flag in MRFP is set to Yes, the RF operator will be required to enter a reason code
1 Enter your receipt in RFPU in the normal manner.

RFPU screen showing system-assigned location
2 Key in your new location and press Enter.

3 Do one of the following:
4 Proceed to process the receipt normally in RFPU.

### ENTERING VARIANCES <a id="entering-variances"></a>

If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Must match ENRE”, you cannot enter variances in RFPU. When the quantity received does not match the quantity on the receipt, the following message will appear and you must either enter the correct quantity or exit the receipt line.
If supervisor authorization is activated:
If supervisor authorization is 
NOT activated:
The following screen will appear:

a) Key in Y for Yes and press Enter to proceed with the location override. If you do not wish to proceed with the override, key in N for No and press Enter to return to the main RFPU screen.

b) Have a supervisor log in to approve the location override.
The following screen will appear:
a) Key in Y for Yes and press Enter to proceed with the location override. If you do not wish to proceed with the override, key in N for No and press Enter to return to the main RFPU screen.
b) Press Enter again to accept the warehouse that the systemassigned location belongs to.

RFPU screen showing “Qty entered does not match expected qty” message
If the RFCH/RFPU Quantity Must Match ENRE Quantity flag in MRFP is set to “Matching not required”, you have four options:
▪ you can ignore the variance for now because you expect to receive more product
▪ you can reject the variance and re-enter the quantity
▪ you can place the variance quantity on hold
▪ you can accept the variance
If you accept the variance, AccellosOne 3PL will create one line in the Location Block of ENRE for the flow 
CORE (Confirm Receipt) showing the actual quantity received. If you place the variance quantity on hold, 
AccellosOne 3PL will create two lines in the Location Block of ENRE for the flow CORE (Confirm Receipt): 
one line showing the actual quantity received with no hold code and a second line showing the variance quantity with the hold code that you specified in RFPU.

LORE screen showing 80 cases with no hold in location A101 and 20 cases on damaged hold in the same location

### PUTTING AWAY PRODUCT UNDER AN ALTERNATE ITEM CODE <a id="putting-away-product-under-an-alternate-item-code"></a>

See [Receiving Product Under an Alternate Item Code](recebimento-rf.html#receiving-product-under-an-alternate-item-code) for further information on setting up alternate item codes.
1 Make sure that your receipt in ENRE is at one of the following flows: STUN (Start Unloading), INST (Inbound Staged) or STPU (Start Put-Away).
2 Enter RFPU.

RFPU screen
3 Do one of the following:
If you are receiving an item with a single inventory level:
If you are receiving an item with multiple inventory levels and you know the UI value of the product that you are putting away:
If you are receiving an item with multiple inventory levels and you do NOT know the UI value of the product that you are putting away:
a) Enter or scan in your alternate item code in the UI field. The system will convert the alternate item code to the regular 
AccellosOne 3PL item code. 
a) Enter or scan in your UI value. 
The system will retrieve the receipt number and three inventory levels for that UI value. The alternate item code will be converted to the regular 
AccellosOne 3PL item code.
a) Press Enter to bypass the UI field.
b) Key in your receipt number and press Enter.
c) Enter or scan in your alternate item code. The system will convert the alternate item code to the regular AccellosOne 3PL item code.
d) Enter or scan in your remaining inventory levels.

RFPU screen showing prompt for quantity
4 Proceed to process your receipt in the normal manner.

### PUTTING AWAY IN A PICK LINE LOCATION <a id="putting-away-in-a-pick-line-location"></a>

If you wish to put-away product in a pick line location, you must set the Validation Rules for Put-Away to Pick 
Line flag in MRFP to either 2 (Allow operator to proceed) or 3 (Omit validation of location).

### Entering Process Values in RFIPS <a id="entering-process-values-in-rfips"></a>

RFIPS is a stand-alone version of the process value module in RFCH. It allows you to scan in process values without assigning the product to a final put-away location.
1 Enter RFIPS.
REQUIREMENTS
LOCATION STATUSIf there is an MRFP profile attached to the customer in CUST, the receipt line must be assigned a location. If there is no MRFP profile attached to the customer in CUST, a location for the receipt line is not required.
CATCH WEIGHT 
TOLERANCES
See [Setting Up Catch Weight Tolerances](expedicao-rf.html#setting-up-catch-weight-tolerances) for further information.

RFIPS screen
2 Enter your receipt number.
3 Enter or scan in your UI value. If you do not have a UI value, enter all inventory levels.

RFIPS screen
4 Key in your first value and press Enter or scan it in using your RF gun.
5 If you are capturing multiple process values, repeat the above step for each additional process value.
6 If you wish to interrupt your scanning for any reason, press F4.

RFIPS screen showing incomplete scan message
7 Do one of the following:
8 Scan in another receipt line or press F4 to exit.

### CAPTURING THE WEIGHT DYNAMICALLY FROM A BAR CODE <a id="capturing-the-weight-dynamically-from-a-bar-code"></a>

The locate weight in bar code dynamically option allows you to scan in the weight from a bar coded label without knowing which numbers in the bar code represent the product’s weight. Because the format of the bar code is unknown, you cannot use SCPR (Scan Parameter Profile) to break up the code into its component parts.
The following requirements must be met before you can locate the weight in a bar code dynamically:
▪ All bar codes for a given order line must have the same length.
▪ The weight portion of the bar code for a given order line must all have the same length; if a weight is less than the full length, it must be padded with zeros.
▪ All weights for a given order line must fall within a range of 10 times heavier or lighter than the first case. 
For example, if case 1 weighs 100 lbs., case 2 cannot weigh more than 1,000 lbs. or less than 10 lbs.
▪ The locate weight option must be activated in IPRO by setting the Locate Weight in Bar Code Dynamically flag to Y for Yes for a given process code. This process code must be attached to an item process 
If you wish to continue from where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the received quantity:
Key in 3 and press Enter.
When prompted to short the receipt line, key in Y for Yes and press 
Enter.
If you wish to exit and save the scanned process values:
Key in 4 and press Enter.
If you wish to exit without saving the scanned process values:
Key in 5 and press Enter.

profile code in IPRP (Item Process Profile), which in turn must be attached to the appropriate item(s) in 
ITEM.

IPRO screen showing Locate Weight in Bar Code Dynamically flag set to Y for Yes
The operator scans in the full bar code and then manually enters the weight for the first three cartons. If the manually entered weight matches the bar code weight in all three cartons on the same order line, AccellosOne 3PL “learns” the position of the weight in the bar code.
If the manually entered weight does not match the bar code weight, the operator will be prompted to either start over again or rescan the current carton.
EXAMPLE
9991234999 (Label 1)
9991356999 (Label 2)
9991426999 (Label 3)
Because the position of the weight in label one (positions 4 through 7) matches the position of the weight in labels two and three, AccellosOne 3PL will read the weight from these positions for all pieces on the receipt line.
If the same bar code is scanned twice, the operator will have two choices: accept the duplicate or enter a new bar code.
1 Enter RFIPS.
2 Enter your receipt number.
3 Enter or scan in your UI value. If you do not have a UI value, enter all inventory levels.

RFIPS screen showing prompt to use weight discovery
4 Key in Y for Yes and press Enter.
RFIPS screen showing prompt for weight measure code
5 Key in your weight unit of measure (1 for kilograms or 2 for pounds) and press Enter. If you made a mistake and wish to select another order line, key in 3 for Cancel and press Enter. 

RFIPS screen showing prompt to scan the bar code
6 Scan in your bar code.

RFIPS screen showing prompt to enter weight
7 Key in the weight and press Enter. The weight must include a decimal point. For example, to enter a weight of 20 pounds, you must key in either 20.0 or 20.00. You cannot key in 20.
8 Repeat steps 5 and 6 for your second piece.
9 Do one of the following:
If the position and weight of label 
1 matches label 2:
If the position and weight of label 
1 does NOT match label 2:
a) Repeat steps 5 and 6 for your third piece.
AccellosOne 3PL will offer you two options: you can either start over again from the first scan or repeat the second scan.
a) Press Enter to rescan or key in N for No to start over. 

10 Do one of the following:
11 Scan in your first piece.
12 Continue to scan all pieces on the receipt line. If the same item is found on two or more receipt lines, 
AccellosOne 3PL will calculate a running total of the weight for all receipt lines containing that item.
13 When you finish scanning all your pieces, process another receipt line or press F4 to exit.

### Deleting a Receipt Line in RFDL <a id="deleting-a-receipt-line-in-rfdl"></a>

You can delete a receipt line in RFDL if the receipt line has not been confirmed.
1 Enter RFDL.
RFDL
If the position and weight of label 
3 matches labels 1/2:
If the position and weight of label 
3 does NOT match labels 1/2:
The following message may appear:
“Keep 3 Scans” message
a) Press Enter to start scanning or key in N for No and press Enter.
AccellosOne 3PL will offer you two options: you can either start over again from the first scan or repeat the third scan.
a) Press Enter to rescan or key in N for No to start over. 

2 Key in your receipt number and press Enter.
RFDL screen showing prompt for unique UI
3 Key in your UI for the receipt line and press Enter.
RFDL screen showing prompt to continue
4 Press Enter to continue.
RFCH screen showing prompt to delete receipt line

5 Key in Y for Yes and press Enter.
6 When you finish deleting your receipt line, press F4 to exit.

### Clearing Tie/Hi/Loose Variances in RFCV <a id="clearing-tie-hi-loose-variances-in-rfcv"></a>

This program allows supervisors to clear receipt variances that occur when the tie/hi/loose quantity entered in 
RFCH does not match the expected quantity in ENRE. When a supervisor clears a pallet, it becomes available for final put-away in RFPU. There are two options in this program:
If the received quantity was adjusted and if the product is a catch weight product, the supervisor will be prompted to capture the weights.
1 Enter RFCV.
2 Enter or scan in your UI.
RFCV screen showing variance (three cases expected and four cases received)
RFCV screen showing variance (three cases expected and four cases received)
3 When the receipt line is retrieved, press Enter to continue.
update the received quantity the RFCH operator made a mistake, there is no variance and the expected and received quantities in fact match accept the variance The supervisor has confirmed the variance

RFCV screen showing variance options
4 Do one of the following:
To reject the variance: To accept the variance:
a) Key in 1 and press Enter.
b) Enter the correct quantity and press Enter.
c) If the product is a catch weight product, enter your catch weights.
a) Key in 2 and press Enter.
