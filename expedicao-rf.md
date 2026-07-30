---
title: "Expedição via RF (Setup e Processamento)"
description: "Configuração e operação outbound no coletor: regras de saída, tasking e scanning."
layout: default
---

# Expedição via RF (Setup e Processamento)

Configuração e operação outbound no coletor: regras de saída, tasking e scanning.

**Fluxo principal:** `CCCC/CCOR/CCDU (regras) -> RFOPS/RFOLP (scanning) -> RFOT (tasking)`

> Fonte: manuais H do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Outbound Setup Programs <a id="outbound-setup-programs"></a>

*Manual H — RF Guide*

### About the Task Engine <a id="about-the-task-engine"></a>

The task engine offers a fully automated solution to outbound task assignment. Instead of allowing RF operators to pick orders at their own pace and in a sequence that does not take into account the tasks of other RF operators, AccellosOne 3PL consolidates all picking and replenishment tasks in a single centralized “bucket”.
When an RF operator logs into RFPIC, he or she is assigned the next available outbound task in the bucket. 
The next available task is based on a number of factors including:
▪ the RF operator’s equipment
▪ the RF operator’s proximity to the task’s location
▪ the RF operator’s task profile
▪ the location’s height restrictions
▪ the priority assigned to the task’s activity type
▪ the task’s pick method (full pallet pick vs. case pick)
▪ the level of congestion in a particular aisle
If an RF operator chooses to skip a pick or replenishment task, AccellosOne 3PL will record the skipped task as well as the operator who skipped it.
This purpose of tasking is to optimize the distribution of warehouse tasks such that travel times in the warehouse are reduced to a minimum, urgent tasks are performed first and congestion in warehouse aisles is avoided whenever possible.
Tasks are sorted in the following sequence:
▪ Task Priority Override if any
▪ Warehouse Activity Type Number 
▪ Ship To Date/Time 
▪ Order Priority Number
▪ Create Date/Time 
The task engine will not release pick tasks if there are pending replenishment tasks. For pre-build outbound pallets (pallets generated at the time of waving), the entire assignment will not be released if there is a single pending replenishment task. Each time that a pick task cannot be released because of a pending replenishment, the priority of the replenishment task will be increased.

### ACTIVATING THE TASK ENGINE <a id="activating-the-task-engine"></a>

You activate the task engine by setting up one or more task profiles in REGI and then attaching your RF operators to the appropriate task profile(s) in RFOT.

### Overview of Setup Programs <a id="overview-of-setup-programs"></a>

The following graphic shows the various setup programs for outbound processing.

### Customer Codes (CUST) <a id="customer-codes-cust"></a>

Make sure that the Consolidation Method for Allocated Lines field in CUST is set to Multiple Location Lines 
NOT Allowed.
MHET WATP
CTSZ
REGI
PKST
REGI CCCC
CCDU
RFOP
RF operators set up in RFOP are attached to material handling equipment types, task profiles and warehouse activity types.
Task profiles are attached to outbound process configurations. If required, OPID mix/no mix rule in 
WCCO overrides CCCC.
Document codes and pick methods are attached to various combinations of customer/consignee/carrier in 
CCDU.
ITEM
ICNP
In cartonization setup, packing stations are defined in 
PKST, carton size codes are attached to outbound process configurations and item cartonization profile codes are attached to items.
WCCO
CCOR
Outbound rules relating to allocation, manual pallet picking in RFPIC and SSCC/MCP labels are attached to various combinations of customer/consignee.

CUST (Customer Code) screen showing Consolidation Method for Allocated Lines set to Multiple 
Location Lines NOT Allowed
FIELD DESCRIPTIONS
Consolidation Method for 
Allocated Lines
Multiple Location Lines Allowed (default value)
Multiple Location Lines NOT Allowed
If you set this field to Multiple Location Lines Allowed, AccellosOne 3PL will not create additional order lines when an order line picks from more than one location. If you set this field to Multiple Location Lines NOT Allowed, AccellosOne 3PL will create additional order lines to ensure that no order line has more than one location line. 
For example, if an order line of 30 cases requires picks from three different locations, AccellosOne 3PL will create two additional order lines for a total of three: line 1 (10 cases), line 2 (15 cases) and line 3 (5 cases).
The Multiple Location Lines NOT Allowed option requires P-type order lines in 
ENOR.
The advantage of this feature is faster picking of large order lines by splitting the work into multiple tasks that can be performed by multiple operators. If you activate this feature, three operators could work on the same order line if that line picked from three different locations. If you deactivate this feature, the entire order line could only be picked by a single operator.

### Customer / Consignee Document Setup (CCDU) <a id="customer-consignee-document-setup-ccdu"></a>

In this program, you set up your label document(s) and pick methods for RFPIC, RFPK and RFSC. 
Documents set up in CCDU are not flow dependent and do not need to be attached to the appropriate outbound flow in DIFP.
You can set up a single label document for all customers/carriers/consignees or you can define a specific label document for certain customer/carrier/consignee combinations. For example, in RFPIC label 1 will print for customer A, label 2 will print for customer B and label 3 will print for all other customers.
You can also define different documents for different pick methods: for example, print label 1 when each picking and print label 2 when pallet picking.
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
The pick method that the label document applies to. If you leave this field blank (that is, no pick method), the pick method is CASE.
Document Code Your document code for the unique customer/consignee combination. This document code must be set up in DOCU.
Interface Flag If you are printing an actual document on a physical printer, leave this flag blank. If you are sending your CCDU information to another device for further processing, click on this flag to select it.

CCDU screen showing bill of lading document for customer A2, all carriers, all consignees and all picking methods

### Item Hazardous Material Violation (IHZV) <a id="item-hazardous-material-violation-ihzv"></a>

In this program, you define your segregation rules for outbound pallets and containers; for example, hazardous class 1.1 (Explosives) cannot be mixed with hazardous class 1.2 (Explosives). The segregation rules apply to RFPIC (RF Pick) and RFMG (RF Merge OPID). To activate hazmat segregations rules in these programs, you must set the Separate Hazmat by Item in Each Pick flag in MRFP (RFPIC 3 tab) to Yes.
If the rules in IHZV are violated, the RF operator will be not be able to pick the line in RFPIC or merge the 
OPID in RFMG.
IHZV screen showing classes 1.2, 1.3 and 1.4 as restricted classes for class 1.1

### Outbound Pallet Building With the Pallet Build Engine <a id="outbound-pallet-building-with-the-pallet-build-engine"></a>

The Pallet Build engine allows you to generate picking assignments (outbound pallets) based on predefined pallet building rules. Pallet building is only available for orders assigned to a wave in Wave Manager and picked in RFITLV (RF Interleaving).
There are two types of pallet building in AccellosOne Enterprise 3PL: pre-built pallets and dynamically built pallets. With pre-built pallet building, the pallet is built during waving and you can view and edit your pallet build assignments in PABU (Pallet Build). With dynamic pallet building, on the other hand, the pallet is built in real time by the Task Engine taking into account only the currently available tasks and you cannot view or edit your pallet build assignments in PABU.
Pre-built pallets are built when orders are waved. The pallet build engine will look at the entire order and then calculate the contents and pick sequence for your outbound pallets. The number of pallets generated is based on your picking path mode, your maximum cube and weight rules per pallet and whether or not a single pallet can contain mixed product. Dynamically built pallets, on the other hand, are built in real time as the RF operator moves through the warehouse performing his or her picks. Rather than looking at the entire order, the pallet build engine looks only at the currently available tasks facing a given RF operator.
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
In IPBR you set up your pallet build restrictions, defining which items can be placed together on the same pallet. For example, if you add the code R1 in the Header Block and the code R2 in the Detail Block, items assigned your R1 pallet restriction code can never be placed on the same pallet as items assigned your R2 pallet restriction code. 
If you select the Allow Only on Top checkbox, items assigned the pallet build restriction code in the Detail 
Block can be placed on top of but not underneath items assigned the pallet build restriction code in the 
Header Block. Your IPBR code is then attached to the appropriate items in ITEM.

IPBR screen
ITEM screen showing IPBR code of R1
In ITEM, you define the following:
Stackability Indicator Code In this field, you define how heavy or light the item is compared to other items. 
You can choose any value from Category 1 (base item or very heavy) to Category 5 (the lightest possible item). The Pallet Build engine will not allow you to place heavier items on top of lighter items.
Stackability Quantity in Highest SKU In this field, you define the maximum number of units that can be stacked on top of each other. For example, if the item’s highest SKU is cases and you enter 10 in this field, 

the maximum number of cases that can be stacked on top of each other is 10. This field is for reporting purposes only.
ITEM screen
In REGI you define the Maximum Pallet Height and Maximum Number of Cartons.
REGI screen
In CONS, you set the Single Item Per Outbound Pallet flag to the appropriate value. If you set this flag to 
Yes, the Pallet Build engine will check this flag and restrict outbound pallets to a single item.

CONS screen showing flag set to No
In COMP, you set the Use Assignment Parameter Tables for Pallet Build flag to the appropriate value. If you set this flag to Yes, you can rebuild pallets any number of times using the same REGI/CCCC configuration that was in effect when you first built the pallet for a given order line. If you set this flag to No and you rebuild a pallet, AccellosOne 3PL will use your default pallet build settings in REGI and CCCC.
COMP screen showing the Use Assignment Parameter Tables for Pallet Build flag 

### Task Profile (REGI) <a id="task-profile-regi"></a>

In this program, you set up your task profile(s). A task profile defines various picking options for RF operators. 
For each task profile that you set up, you can define the following options:
▪ the default staging location and warehouse
▪ the picking path mode or sequence in which locations are picked
▪ the sort sequence code (if any) and picking path mode
▪ the maximum pallet weight and/or cube for a pallet assignment when that pallet assignment contains mixed product
REGI is a mandatory setup program for the following programs/functions:
▪ voice-activated picking
▪ outbound pallet building
▪ picking by assignment in RFPV
▪ tasking in RFITLV
If you pick by order line in RFPIC and do not use assignments, task profiles are not required.
Task profiles are attached to operators in RFOP. They can also be attached to Outbound Process Configuration (CCCC). If required, you can set up different task profiles for different combinations of customer, consignee and carrier in CCCC.
FIELD DESCRIPTIONS
Task Profile Mandatory
Your task profile.
Description Mandatory
A description for your task profile.
Voice Profile Code (VOPR)
See [Setting Up Voice-Activated Picking](rf-setup.html#setting-up-voice-activated-picking).
Default Customer Voice 
Profile Code (VOPC)
See [Setting Up Voice-Activated Picking](rf-setup.html#setting-up-voice-activated-picking).

Staging Location Optional
The default staging location for the task profile. If you do not specify a default staging location, the RF operator will be required to specify a staging location during picking.
Warehouse Optional
The warehouse to which the default staging location belongs.
Sort Sequence Code (SOSE)
Optional
The sort sequence or “snaking” of your locations within the task profile. This sort sequence is applied to a picking path mode. If you do not enter a sort sequence code, the sequence of your pick locations will be based on the option that you select in the Picking Path Mode field.
Length of UI Check Digit See [Setting Up Voice-Activated Picking](rf-setup.html#setting-up-voice-activated-picking).
Picking Path Mode Pick in location sequence
With this option, work assignments will be sequenced in location code sequence and order line splitting will be allowed.
The remaining options in this field (“Pick in location sequence, do not split order lines”, etc.) are custom and are only to be used if you are so advised by your HighJump implementation consultant.
% Reserved for future use.
Alternate Reporting Type 
/ Code
Reserved for future use.
OPID Prefix Optional
The prefix for your OPID’s (outbound pallet ID’s).
Spoken Length See [Setting Up Voice-Activated Picking](rf-setup.html#setting-up-voice-activated-picking).
Spoken Value Numeric See [Setting Up Voice-Activated Picking](rf-setup.html#setting-up-voice-activated-picking).
FIELD DESCRIPTIONS

1 Enter REGI.
2 Key in your task profile and press Enter.
3 Key in a description for your new task profile and press Enter.
Maximum Pallet Weight Optional
The maximum weight for a full pallet. If the weight of the order line exceeds this maximum, AccellosOne 3PL will split the line into two or more work assignments.
Maximum Pallet Cube Optional
The maximum cube for a full pallet. If the cube of the order line exceeds this maximum, AccellosOne 3PL will split the line into two or more assignments.
Maximum Pallet Height The maximum height for a full pallet. If the height of the order line exceeds this maximum, AccellosOne 3PL will split the line into two or more assignments.
Pallet Base Length/Width Reserved for future use.
Maximum Half Pallet 
Cube
Optional
The maximum cube for a half pallet.
Max. Number of Cartons The maximum size of a pallet assignment for the Pallet Build engine.
Max. Number of OperatorsSee [OUTBOUND TASKING](expedicao-rf.html#outbound-tasking).
Max. Number of Operators per LocationSee [OUTBOUND TASKING](expedicao-rf.html#outbound-tasking).
Select Only Assignment 
With Both Pick Line/NonPick Line Locations
See [OUTBOUND TASKING](expedicao-rf.html#outbound-tasking).
Priority to Force ReplenishmentSee [OUTBOUND TASKING](expedicao-rf.html#outbound-tasking).
Weight Measure Code The weight measure code for the Maximum Pallet Weight field.
Linear Measure Code The linear measure code for the Maximum Pallet Cube field.
FIELD DESCRIPTIONS

4 Key in your voice profile code and press Enter.
5 If required, key in your staging location and press Enter. 
6 If required, key in your staging warehouse and press Enter.
7 If required, select the appropriate sort sequence code from the pick list.
8 Enter or select any other required parameters for your task profile.
9 When you finish setting up the general parameters for your task profile, click on Save.
REG screen showing task profile 1
10 Click on Exit to exit REGI.

### ADDING FILTERS TO REGI <a id="adding-filters-to-regi"></a>

If you create a saved filter in REGI, the filter column name fields will be populated with your filter values.

REG screen showing filters

### Item Consignee Configuration (ICOC) <a id="item-consignee-configuration-icoc"></a>

In this program, you can define the outbound pallet quantity by consignee when building outbound pallets (pallet build, case picking, OPID merge) for an outbound order. ICOC must be activated in CCOR by setting the Use Consignee Item Configuration flag to Yes for the appropriate consignee record.
ICOC screen

### Outbound Process Configuration (CCCC) <a id="outbound-process-configuration-cccc"></a>

In this program, you set up your pallet wrapping rules for different customer/carrier/consignee combinations. 
You can also override certain MRFP settings for a specific customer/carrier/consignee combination. For example, suppose your default picking mode is set to case picking in MRFP; however, based on your CCCC setting for a specific customer/carrier/ consignee combination, you can establish normal mode picking instead of case pick for that combination.
In CCCC you also specify your pallet building mode in the Task Profile (REGI) field: pre-built or dynamically built.
FIELD DESCRIPTIONS
Customer Code The customer that the outbound process configuration applies to or .ALL for all customers.
Carrier Code The carrier that the outbound process configuration applies to or .ALL for all carriers.
Consignee Code The consignee that the outbound process configuration applies to or .ALL for all consignees.
Number of Times Pallet 
Wrapping is Required
Only required for pallet wrapping
If pallet wrapping is required for a pallet being built in the warehouse, enter the number of times in this field.
Number of Times Pallet 
Wrapping is Required for 
Pallet Pick
Only required for pallet wrapping
If pallet rewrapping is required for a full pallet pick (that is, the pallet was already wrapped when it was received into the warehouse), enter the number of times in this field.
Number of Hours from 
Ship Date to Release Full 
Pallet Pick Task
Only available if tasking is activated
In this field, you specify the number of hours before the ship date that a full pallet pick task is created. 
Task Profile Code (REGI) If you populate this field with a task profile, pre-built pallet building will be activated. If you leave this field blank, dynamic pallet building will be activated.

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
If you select Per Item, a single OPID per item is required. That is to say, the same item cannot be assigned to two or more OPID’s. If you select Per Order, a single OPID per order is required. If you select Per Order Line, a single 
OPID per order line in case pick mode is required. If you select Per Order Line in NM Mode, a single OPID per order line in normal mode is required.
If you select Per OPID, OPID entered by user, QRS label by line, AccellosOne 
3PL will generate a QRS value for each OPID entered by the user. This option is only available for QRS orders in which the user enters an OPID for each order line.
If you select No Restriction, the same OPID can be assigned to any number of items, orders or order lines.
Allow Partial Picking in 
Normal Mode
Allow all, no restriction
Allow last remaining partial inventory and full pallets
Allow full pallets only
If you select an option in this field, it will override the option that you selected in MRFP.
Workflow Profile Code (DIFP)
If you enter a workflow profile code in this field, it will override the workflow profile code(s) attached to the customer and consignee.
FIELD DESCRIPTIONS

AccellosOne Ship Date Current Date
Ship to Date if you select Current Date, AccellosOne Ship will use the current date as the ship to date sent to the parcel carrier even if that date differs from the order ship to date in AccellosOne 3PL. If you select Ship to Date, AccellosOne Ship will use the order ship to date in AccellosOne 3PL as the ship to date sent to the parcel carrier.
UCC-128 Package Type Carton
Container
Pallet
The UCC-128 packaging type.
Maximum Gross Weight per OPID
The maximum gross weight for an OPID in RFPIC/RFMG (that is, pallet building, case picking and OPID merging).
Maximum Net Weight per 
OPID
The maximum net weight for an OPID in RFPIC/RFMG (that is, pallet building, case picking and OPID merging).
OPID Weight Measure 
Code
The unit of measure for the maximum weight.
OPID Alert Percentage The percentage of the maximum weight at which an alert will be generated for the RF operator in RFPIC. If the operator selects Yes at the Continue? prompt, he or she can pick the selected line even though it is overweight.
Parcel Carrier Notification 
Type
Reserved for future use
Number of Hours Before 
Ship Date to Force 
Replenishment Tasks
Only available if tasking is activated
In this field, you specify the number of hours before the ship date to “force” 
replenishment tasks. That is, create a replenishment task for a pick line location even if the pick line location is full and there is no room for the replenishment.
FIELD DESCRIPTIONS

CCCC screen

### DOCUMENT MESSAGES BLOCK <a id="document-messages-block"></a>

In this block, you can attach a message code to a document code for a specific combination of customer/ carrier/consignee. This block is a further refinement of the document print messages logic in DPME.
If there are multiple messages attached to the same document, you can specify the sequence of messages appearing on the document by entering a sequence number in the Seq. No field.
Priority Value for Forced 
Replenishments
Only available if tasking is activated
In this field, you specify the priority value for forced replenishment tasks. The default value for all replenishments is 100. You can change it to a lower value (say, 50) so that it has a lower priority.
FIELD DESCRIPTIONS

### Warehouse Customer Consignee OPID Rule (WCCO) <a id="warehouse-customer-consignee-opid-rule-wcco"></a>

In this program, you define your mix/no mix OPID rules for each warehouse/customer/consignee combination. The Allow Mixing Items in OPID flag in WCCO overrides your OPID Assignment Rules in CCCC. It also overrides your Single Item Per Outbound Pallet setting in CONS. Mix/no mix OPID rules apply to the programs RFPIC, RFPK, RFITLV and RFMG.
NOTE: If an order requires the generation of a SSCC label, item codes cannot be mixed.
WCCO screen

### Customer/Consignee Outbound Rules (CCOR) <a id="customer-consignee-outbound-rules-ccor"></a>

In this program, you define your outbound rules for various customer/consignee combinations. Outbound rules cover three major areas:
▪ allocation
▪ manual pallet building in RFPIC

▪ labeling requirements
CCOR is an optional program. If none of your customers and consignees use any of the options in this program, you do not need to set up any records in CCOR.
FIELD DESCRIPTIONS
Customer Code The customer for the outbound rules.
Consignee Code The consignee for the outbound rules.
Ship Newer Product Y = Yes
N = No
If you set this flag to Yes, allocation will only allocate product whose expiry date is greater than or equal to previously shipped inventory from that customer to that consignee.
OPID Inventory Level 
Optimization Type
Only available for manual pallet building in RFPIC
No Optimization (1)
Inventory Level 2 (2)
Inventory Level 3 (3)
Inventory Level 4 (4)
If you select 1, a single pallet can contain mixed product at all inventory levels; 
that is, different levels 1, 2, 3 and 4. If you select 2, all product on a single pallet must have the same level 2 value, but other inventory levels may differ. If you select 3, all product on a single pallet must have the same level 3 value, but other inventory levels may differ. If you select 4, all product on a single pallet must have the same level 4 value, but other inventory levels may differ.

OPID Expiry Date Optimization Type
Only available for manual pallet building in RFPIC
Not allow (1)
A single expiry date per OPID is allowed.
Allow based on specified dates (2)
You can specify a minimum number of shelf life days, a maximum number of shelf life days and/or a maximum number of days between your minimum and maximum number of shelf life days.
Allow based on number of shelf life days (3)
You can specify a minimum number of days to expiry.
Allow any dates (4)
Any expiry date is allowed on an OPID.
Minimum Number of 
Shelf Life Days
Only available if OPID Expiry Date Optimization Type = 2
If you enter a minimum number of shelf life days in this field (say, 10), all product on the same pallet must have a shelf life of at least 10 days.
Maximum Number of 
Shelf Life Days
Only available if OPID Expiry Date Optimization Type = 2
If you enter a maximum number of shelf life days in this field (say, 20), all product on the same pallet must have a shelf life of greater than 20 days.
Number of Days Between 
Min./Max. Dates
Only available if OPID Expiry Date Optimization Type = 2
In this field, you specify the maximum number of days between your minimum number of shelf life days and your maximum number of shelf life days. If there is a conflict between this value and your minimum/maximum number of shelf life days value, the more restrictive condition will apply.
Number of Days Between 
Multiple Expiry Dates in 
OPID
Only available if OPID Expiry Date Optimization Type = 3
If you enter a number in this field (say, 90), any product with an expiry date greater than 90 days can be mixed.
FIELD DESCRIPTIONS

Use Consignee Item 
Configuration
Y = Yes
N = No
If you set this flag to Yes, you can define outbound pallet quantity by consignee in ICOC. If you set this flag to No, outbound pallet quantity by consignee in ICOC is deactivated.
SSCC Label Required Y = Yes
N = No
If you set this flag to Yes, an SSCC label will be generated. If you set this flag to No, no SSCC label will be generated. This field overrides the Generate 
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
Number of SSCC Labels to Print
Only available if SSCC Label Required = Yes
The number of SSCC labels to print.
Retail Ready Reserved for future use.
SSCC Number Range Only available if SSCC Label Required = Yes
Your number series for SSCC labels in NUSE (Number Series)
Print Customer Name Y = Yes
N = No
If you set this flag to Yes, the customer name will print on the e label. If you set this flag to No, the customer name will not print on the label.
FIELD DESCRIPTIONS

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
If you set this flag to Yes, OPID’s will be restricted to product belonging to a single order. If you set this flag to No, an OPID can contain product from multiple orders.
The option that you select in this field overrides the option that you select in the OPID Assignment Rules field in CCCC.
MCP Label Required Y = Yes
N = No
If you select Yes, an MCP label is required. If you select No, an MCP label is not required.
Pick From Bulk if Order 
Qty. Over Set Percentage
Y = Yes
N = No
If you select Yes, allocation will pick from a non-pick line location when the order quantity is less than a full pallet but greater than the threshold percentage that you define. The remaining pallet quantity not needed to fill the order line will be relocated within bulk via a directed move.
If you select No, allocation will pick anything less than a full pallet from the pick line according to your rules in PIPR and PIIT.
Threshold Percentage Only available if Pick From Bulk … = Yes
The threshold percentage of a full pallet for picking from bulk. This calculation is based on the item's lowest SKU. If the item is a variable quantity breakdown item, the threshold percentage will be based on the variable quantity breakdown.
FIELD DESCRIPTIONS

Acceptable Range of 
Expiry Dates
Only available if Pick From Bulk … = Yes
The acceptable range of expiry dates between pick line stock and full pallet picks from bulk. A value of zero in this field means that the expiry date of the pick line stock must match exactly the expiry date of the full pallet stock in bulk.
For example, if you set this field to 15, allocation will only pick from bulk if the expiry date of product in bulk is within 15 days of the expiry date of product allocated from the pick line.
Pick Full Pallets Only Y = Yes
N = No
If you select Yes, allocation will pick from full pallet stock only and selection by 
FIFO will be deactivated if necessary. The definition of a full pallet is based on the following:
▪ if the Use Consignee Item Configuration flag is set to Yes, the quantity breakdown set up in ICOC (Item Consignee Configuration) will be used 
▪ if the Use Consignee Item Configuration flag is set to No, the quantity breakdown set up in ITEM will be used
CAUTION Because FIFO selection is deactivated, the Yes option may leave non-full pallet stock in the warehouse even if it is the oldest stock. And eventually this stock will expire.
FIELD DESCRIPTIONS

CCOR screen showing default values
In the Item Outbound Rules Block, you define the threshold percentage and full pallet picking only rules for specific items when shipped to the consignee in the header block.
CCOR screen showing Item Outbound Rules Block

GENERAL NAVIGATION AND LOOK-UP 
PROGRAMS

## Outbound Processing <a id="outbound-processing"></a>

*Manual H — RF Guide*

### Overview of Shipping <a id="overview-of-shipping"></a>

There are up to nine steps to follow in outbound RF processing:
RFOT
SELO
Depending on the flows in your workflow profile, you may have to confirm your orders in CHOF (Time-Stamp and Confirm Orders).
You assign buildings and doors to loads in SELO (Set Up Load). 
You pick your orders in RFPIC/RFPK/RFPV. If your system is set up for pallet building, you must enter the pallet ID of your new pallet.
CHOF
If required, you assign RF operators to order lines in RFOT (RF Operator Task Assign).
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
If required, you assign RF operators to orders/loads in RFOT (RF Operator Task Assign).
ENOR
You enter your order in ENOR (Enter, Modify and 
Delete Order).

### Understanding Outbound Flows in RF <a id="understanding-outbound-flows-in-rf"></a>

In non-RF shipping, you time-stamp and advance the flow of an order in CHOF (Time-Stamp and Confirm 
Orders). Advancing the flow of an order in CHOF advances the flow of all order lines and order location lines on the order. You cannot advance the flow of one order line and leave another order line remain at its original flow.
In RF shipping, on the other hand, AccellosOne 3PL automatically advances the flow of individual order lines and order location lines. For example, when you pick an order line in RFPIC, the order line’s flow is automatically advanced from STPI (Start Picking) to FIPI (Finish Picking). Because the flow of individual order lines is advanced as each order line is picked, not all lines on a given order will be at the same flow. When this happens, the order header will show the earliest flow on the order.
For example, suppose there are five order lines on a given order: two lines are at the flow STPI, two lines are at the flow FIPI and one line is at the flow STLO (Start Loading). If you look up the order in LOOR, the order’s flow will be set to STPI, which is the earliest flow.

### Understanding Pick Methods <a id="understanding-pick-methods"></a>

Pick methods allow you to split order lines into two or more pick method assignments. For example, if your order line quantity was two pallets and 10 cases, you might want to assign one RF operator with a forklift to pick the two pallets and another RF operator with a different piece of equipment to pick the 10 cases. Without pick methods, you would be forced to assign the entire order line quantity to a single RF operator using a single piece of equipment. This could be an inefficient use of resources.
Pick methods also allow you to define a sequence for your picking; for example, pick cases/eaches first because it is complex and time-consuming and pick full pallets last because it is simple and straightforward. 
Different pick methods can have different label printing requirements; you can attach different customer/ consignee/carrier combinations to a particular pick method/document in CCDU (Customer/Consignee 
Document Setup).
Pick methods are assigned to order lines in the Wave Manager based on the order line quantity and your item setup. For example, if your order line quantity is one pallet, the pick method will be set to PALL.
CAUTION Using CHOF to confirm orders in an RF environment is not recommended unless all order lines are at the same flow. If line 1 is at the STPI flow and line 2 is at the FIPI flow, advancing the order header to the STLO flow in CHOF will also advance line 1 to STLO. At which point, line 1 may no longer be pickable.

AccellosOne 3PL supports the following pick methods:
You can look up an order line’s pick method in LOOR.
NAME CODE DESCRIPTION
CASE A normal case pick in RFPIC. The Pick Method field in LOOR for this pick method is left blank to indicate that it is the system default.
Batch Label Pick BATP A case pick across multiple orders when two or more orders in the wave are being picked up by the same carrier and the carrier type = UPS, DHL or 
FEDEX. Labels are printed after each pick.
Batch Pallet Pick BPAL A batch pallet pick across multiple orders in the same wave when the following conditions are met:
▪ the picks consist of partial pallets
▪ the picks are for the same inventory entity in a single location
▪ the entire inventory entity in the location is picked
Labels are printed after the pallet is built.
Each Pick EACH A Pick & Pack by each (the smallest SKU in an item’s quantity breakdown).
Label Pick LABP An individual order pick when a single order is being picked up by a given carrier.
Non-RF Packing Station PKST Manual packing performed in EPSD (Enter Packing Details).
Packed via Packing StationPACK First level cartonization performed in RFSC (RF Sort to Carton) or RFPK (RF 
Wave Pick).
Pallet Pick PALL A full pallet pick. The order quantity of each order line must equal a full pallet quantity.
RF Merge RFMG A merge of two or more OPID’s in RFMG.
System-Driven Cartonization Each PickCART A Pick & Pack by each used in system-driven cartonization.

Order line assigned CART pick method

### Overview of RF Picking Programs <a id="overview-of-rf-picking-programs"></a>

There are four possible RF picking programs in AccellosOne 3PL: RFPIC, RFPK, RFPV and RFINVT.

### RFPIC (RF PICK) <a id="rfpic-rf-pick"></a>

This program is AccellosOne 3PL’s most basic picking program. it is a system-assisted environment in which the RF operator can select individual order lines to work on and enjoys considerable latitude in determining the sequence of picks.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ Picking is based on orders and order lines only; there is no support for task profiles and any order assignments must be created manually in RFOT. 
▪ Pallet building is performed manually by the RF operator.
▪ Any pick methods assigned to the order by the Wave Manager are ignored.
▪ Consolidated pick using wave number is supported but you cannot restrict by warehouse zone.

### RFPK (RF WAVE PICK) <a id="rfpk-rf-wave-pick"></a>

This program is AccellosOne 3PL’s most advanced picking program. Many of the tasks that are performed manually by the RF operator in RFPIC are automated in RFPK.
▪ Only orders that have been waved in the Wave Manager can be picked.

▪ Pick method assignment is performed by Wave Manager during allocation.
▪ System-driven cartonization is supported.

### RFPV (RF PICKING VOICE) <a id="rfpv-rf-picking-voice"></a>

This program is the RF equivalent of voice-activated picking. It allows you to pick certain orders or products using a standard RF gun rather than your voice-activated equipment.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ RF operator must be set up in RFOP and REGI must be configured.
▪ Pallet build assignment is performed dynamically in real time rather than through the Wave Manger.

### RFINVT (RF INTERLEAVING) <a id="rfinvt-rf-interleaving"></a>

This program supports tasking.
▪ Orders can be allocated through either Wave Manager or ASOR/PROR.
▪ RF operator must be set up in RFOP and REGI must be configured.
▪ Pallet build assignment is performed by Wave Manager during allocation.

### Picking Orders in RFPIC <a id="picking-orders-in-rfpic"></a>

RFPIC is AccellosOne 3PL’s most basic picking program. You can pick product by zone or by order number. 
Orders must be fully allocated before you can pick them in RFPIC. You cannot pick an order if some lines are allocated (R-type) and other lines are unallocated (P-type).
If you are picking full pallets from bulk, you scan in the original pallet ID of the pallet and use this pallet ID for the duration of the outbound process. If you are picking cases from either bulk or the pick line, you scan in the original pallet ID for each case pick. When you finish building your pallet, you have two options for the outbound pallet containing mixed product:
▪ if AccellosOne 3PL generates your pallet ID for outbound pallets, you generate your label and then send it to the appropriate printer
▪ if you use your own preprinted labels for outbound pallets, you enter or scan in the preprinted pallet ID
When you finish generating or scanning in your pallet ID label, you can look up your pallet ID in the 
Processing Block of LOOR for each item on the pallet.

If the product that you are picking is not in its assigned location, you have two options. If you know where the product is, you can go to that location and pick it. If you do not know where the product is, you can place the product on hold to indicate that it could not be picked.
REQUIREMENTS
FLOWS ENOR (Enter Order)
SUAL (Supervisor Allocated) — optional
STPI (Start Picking)
FIPI (Finish Picking)
STLO (Start Loading)
FNLO (Finish Loading)
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFPIC.
CASE PICKING There are three requirements for case picking:
▪ you need a pallet ID label defined in DOCU (Documents)
▪ this label must be attached to the appropriate customers/consignees in CCDU (Customer / Consignee Document Setup)
▪ you need an outbound item process code called CP (Case Pick) in IPRO (Item 
Processes)
NOTE Your CP code set up in IPRO must NOT be attached to the IPRP profile attached to ITEM.
If you want AccellosOne 3PL to generate a unique pallet ID for each pallet label, there are three additional requirements:
▪ you need to set up a code in NUSE (Number Series)
▪ you need to attach to your NUSE code to a DIAP (Depositor Inventory Assign 
Profile) called QRS
▪ you need to set the Outbound Pallet ID Label field on the RFPIC (2) tab in 
MRFP to either option 2 or option 3
NOTE Your QRS code set up in DIAP must NOT be attached to DILP (Depositor Inventory Level Profile).

DIAP screen showing sample setup for case pick label
IPRO screen showing setup for CP code
ITEM MESSAGES If you define a message in MESS (Messages) and attach the message to an item in ITEM, the message will display in a pop-up window when you process an order line for that item.
REQUIREMENTS

DEPOSITOR 
PRINT MESSAGES
If you wish to display a depositor print message set up in DPME, attach a document code of PICK to your message code in DPME. DPME messages for RFPIC require specific customer/carrier/consignee combinations; you cannot use the “.ALL” codes.
NOTE A DPME message for RFPIC does not actually print unless you set up a real pick document in DOCU and then attach this pick document to an outbound flow in DIFP.
PROCESS VALUES
Only required if you are scanning process values
See [Entering Process Values in RFOPS](expedicao-rf.html#entering-process-values-in-rfops) for further information.
SCAN PARAMETER CODE
Only required if you are scanning process values, inventory levels or UI values from a bar code label
See [Entering Process Values in RFOPS](expedicao-rf.html#entering-process-values-in-rfops) for further information.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code label
You must define a bar code profile in BAPR and attach to it the scan parameter code that you set up in SCPR.
PALLET BLOCK If you wish to ship, receive and exchange pallets, you must set the Display Pallet 
Screen field in MRFP (RFPIC tab) to the appropriate value: Display Before Picking or Display on Completion of Picking. 
CONSOLIDATED 
ORDERS
If you consolidate your orders in COPI (Consolidated Pick), you must set the 
Default Mode in MRFP (RFPIC tab) to Only Pallet Picking.
OTHER Picking locations must be attached to a warehouse zone in WHZO.
You need a hold type code of SUSP (Suspend) in HOLD (Hold Types). The Shippable flag must be set to N for No for this code.
FUNCTION KEYS
All Modes
REQUIREMENTS

F1 FN (Function) Allows you to access RFRL, RFPR, RFIT and RFLR without leaving RFPIC.
F2 Qu (Query) Displays the first unpicked order line of the current order being processed.
F2 CP (Case Pick Mode) Allows you to switch to case pick mode. 
This command is only available before selecting an order line.
F3 HD (Hold) Places product on hold.
F4 Ex (Exit) Exit program.
F9 Move cursor to previous field.
Exit Tag screen
F1 GL (Go to Location) Allows you to skip the PRT field and go directly to LOCTO field. OPID validation is also skipped.
Only used when you wish to print labels and validate the OPID in RFST.
Pick List of Order Lines
F1 L1 (Level 1) Changes the function key assignments for 
F1 and F2. If F1 = L1 (item code), pressing F1 will change F1 to L4 (level 4 or lowest) and F2 to LO (location). These new function key assignments will allow you to change the sequence of order lines to either level 4/lowest inventory level or location.
F2 L2 (Level 2) Changes the function key assignments for 
F1 and F2. If F2 = LO (location), pressing 
F2 will change F1 to L1 (level 1) and F2 to 
L4 (level 4 or lowest). These new function key assignments will allow you to change the sequence of order lines to either level 
1 or location.
F3 SL (Select) Selects the order line that the cursor is positioned over.
FUNCTION KEYS

### PICKING FULL PALLETS FROM BULK <a id="picking-full-pallets-from-bulk"></a>

1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.

RFPIC screen
3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.
5 Do one of the following:
F4 CN (Cancel) Exits the pick list without selecting an order line.
If you wish to pick by zone:
If you wish to pick by order number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order number and press Enter.
a) Press Enter to bypass the Zone field.
b) If required, key in your warehouse and press Enter.
c) Key in your order number and press Enter.
If the default mode for RFPIC has been set to Case:
If the default mode for RFPIC has been set to Pallet:
The message “You have selected CP 
Mode” will appear.
a) Key in N for No and press Enter.
The message “You have selected NM mode” will appear.
a) Press Enter to continue.
FUNCTION KEYS

RFPIC screen showing pick list of order lines, items and locations to pick
6 The pick list of order lines is initially shown in location code sequence. If you wish to display the list in 
Level 1 sequence, press F1 (L1). If you wish to display the list in Level 4 or lowest inventory level sequence, press F2 (L4). If the list is in Level 4 sequence, you can press F2 again to return to the location code sequence.
7 Use your arrow keys to position your cursor over the order line that you wish to pick, then press F3 (Select).

RFPIC screen showing prompt for from location
8 If required, enter or scan in your from location.

9 Enter or scan in your UI (Unique Identifier) as follows:
10 Key in your pick quantity and press Enter. If your pick quantity is less than your order quantity, see [Placing Product on Hold](expedicao-rf.html#placing-product-on-hold) for further instructions.
11 If prompted to do so, enter or scan in your staging location as well as the staging location’s warehouse.
If the order is on a load, the door’s staging location from the load will be shown.
12 When the pick list of unpicked order lines reappears, repeat the above steps for each additional line on the order.
13 When you finish entering your order lines, the message “ORDER COMPLETED” may appear. If it does, press Enter to acknowledge it.
14 Process another order or press F4 to exit.

### PICKING CASES <a id="picking-cases"></a>

When you pick cases, you must print a pallet ID label for each pallet that you build. You can place as many cases as you want on a pallet, but all cases must belong to the same order; you cannot place product from different orders on the same pallet.
If you are picking from a pick line, case pick mode is automatically activated in RFPIC unless the Default 
Mode field in MRFP set to Only Pallet Picking. 
1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.

RFPIC screen
If reserved logic is activated for this customer:
If reserve logic is NOT activated for this customer:
a) If the lowest inventory level is represented by a plus sign (+), you can enter any value for that level. If the lot number, pallet ID, etc. is represented by an actual value, you must enter that value; 
any other value will be rejected by the system.
a) All inventory levels for the product to be picked will be shown. 
The lot number, pallet ID, etc. 
that you enter must match the values displayed on your screen. 
If you attempt to enter different values, they will be rejected by the system. 

3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.

RFPIC screen prompt to continue in case pick mode
5 Do one of the following:
If you wish to pick by zone:
If you wish to pick by order number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order number and press Enter.
a) Press Enter to bypass the Zone field.
b) Key in your warehouse and press Enter.
c) Key in your order number and press Enter.
If the default mode for RFPIC has been set to Case:
If the default mode for RFPIC has been set to Pallet:
The message “You have selected CP 
Mode” will appear.
a) Press Enter to continue.
The message “You have selected normal mode” will appear.
a) Key in N for No and press Enter.

RFPIC screen showing list of order lines, items and locations to pick
6 The pick list of order lines is initially shown in location code sequence. If you wish to display the list in 
Level 1 sequence, press F1 (L1). If you wish to display the list in Level 4 or lowest inventory level sequence, press F2 (L4). If the list is in Level 4 sequence, you can press F2 again to return to the location code sequence.
7 Use your arrow keys to position your cursor over the order line that you wish to pick.
8 Press F3 (Select).

RFPIC screen showing prompt for from location
9 Enter or scan in your from location.

10 Enter or scan in your UI (Unique Identifier) as follows:
11 Key in your pick quantity and press Enter. If your pick quantity is less than your order quantity, see [Placing Product on Hold](expedicao-rf.html#placing-product-on-hold) for further instructions.
12 Do one of the following:

RFPIC screen showing Print Label (F1) option available
13 Press F1 (Print Label).
If reserved logic is activated for this customer:
If reserve logic is NOT activated for this customer:
a) If the lowest inventory level is represented by a plus sign (+), you can enter any value for that level. If the lot number, pallet ID, etc. is represented by an actual value, you must enter that value; 
any other value will be rejected by the system.
a) All inventory levels for the product to be picked will be shown. 
The lot number, pallet ID, etc. 
that you enter must match the values displayed on your screen. 
If you attempt to enter different values, they will be rejected by the system. 
If your order consists of a single order line:
If your order has multiple order lines and you wish to pick another line:
If your order has multiple order lines and you wish to close the pallet and print the pallet ID label:
a) Proceed to next step. AccellosOne 3PL will display the list of unpicked order lines.
a) Select the line that you wish to pick and repeat steps 6 to 12 for that line.
AccellosOne 3PL will display the list of unpicked order lines.
a) Press F4 to exit the list.
b) Proceed to next step.

RFPIC screen showing prompt for label ID
14 Do one of the following:

RFPIC screen showing prompt for to location
15 Enter or scan in your to location. Your to location must be a staging location. If prompted to do so, enter your to warehouse.
16 Process another order or press F4 to exit.
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that are not generated in 
AccellosOne 3PL: If the Label field is populated:
a) Press Enter to generate your pallet ID.
b) If required, key in your printer code* and press Enter.
c) If prompted to validate your pallet ID, enter or scan it in. 
a) Enter or scan in your pallet ID.
b) If required, key in your printer code* and press Enter.
a) If the PRT (Printer) field is not populated, key in your printer code* and press Enter.
* If you select either SPL or VIEW, no OPID validation will occur.

### PICKING PRODUCT WITH PROCESS VALUES <a id="picking-product-with-process-values"></a>

If you are picking cases from a pallet and if there is a balance remaining on the pallet, AccellosOne 3PL will prompt you to scan each case ID. If you are unable to scan in each case ID on the pallet for any reason, 
AccellosOne 3PL will present you with the following options:

RFPIC screen showing prompt for catch weight
1 Scan all cases that you are shipping for the pallet. The system will prompt you when you are complete.
2 If you are unable to scan all cases for any reason, press F4 after scanning the last scannable case.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned and remove unscanned quantities from the to ship quantity. 
You cannot process the order line again in RFPIC.
4 (Exit, New Line) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned, remove the unscanned quantities from the to ship quantity and will create a new line for the balance.
5 (Exit, Cancel Picking) Cease scanning and exit without saving any process values including those already scanned. The order line will revert to its original status before being picked in 
6 (Replace DAMG) Remove a damaged case from the order and replace it with an undamaged case.
7 (Exit Scan, Save) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned.

RFPIC screen showing “Scan incomplete” message
3 Do one of the following:
4 Continue to pick the order line normally in RFPIC.
If you wish to continue from where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the to ship quantity:
Key in 3 and press Enter.
When prompted to short the order line, key in Y for Yes and press Enter.
If you wish to exit, short the to ship quantity and create a new line for the balance:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values and you wish to restore the order line to its original state before processing in RFPIC:
Key in 5 and press Enter.
When prompted to confirm the cancellation, key in Y for Yes and press Enter.
If you wish to replace a damaged case:Key in 6 and press Enter.
Scan in the damaged case.
Scan in the replacement case.
If you have multiple damaged cases to replace, you must press F4 again and repeat the above steps.
If you wish to exit without saving the scanned process values:
Key in 7 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

### PICKING PARTIAL QUANTITIES OF PRODUCT WITH PROCESS VALUES <a id="picking-partial-quantities-of-product-with-process-values"></a>

When picking a partial quantity from a full pallet that has not been picked before and is in a single location, you can scan in the cases to be removed rather than the cases to be picked. A partial quantity is defined as 
60% or more of the total quantity in the location. For example, if there are 50 cases in a location and you need to pick 30, you can scan in the 20 cases to be removed rather than the 30 cases to be picked. 
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
If you wish to scan the cases to be removed:
If you wish to scan the order quantity:
a) Key in Y for Yes and press Enter.
b) Scan in the cases to be removed.
a) Key in N for No and press Enter.
b) Scan in the cases to be picked.

8 When all your cases are scanned, process another order line or press F4 to exit.

### PICKING RESERVE LOGIC ORDERS <a id="picking-reserve-logic-orders"></a>

Reserve logic allows you to reserve inventory during order allocation at a level other than the lowest level for a customer. By using this option, you allow the RF operator to make the final selection at the lot or pallet ID level based on which product is most accessible.
The lot or pallet ID to be selected by the RF operator is indicated by a plus sign (+) in RFPIC.
1 Enter RFPIC.
2 Do one of the following:
RFPIC screen showing + sign in PI (level 3) field
3 Go the location and scan in the from location.
RFPIC screen showing from location
If you wish to pick by zone:
If you wish to pick by order number:
a) Key in your zone code and press 
Enter.
b) If required, key in your order number and press Enter.
a) Press Enter to bypass the Zone field.
b) Key in your warehouse and press Enter.
c) Key in your order number and press Enter.

4 Scan in the pallet ID that you wish to pick.
RFPIC screen showing selected pallet ID
5 Enter your pick quantity.
6 Scan in your OPID and staging location.
RFPIC screen showing OPID and staging location
7 Press F4 the required number of times to exit.

### PLACING PRODUCT ON HOLD <a id="placing-product-on-hold"></a>

You place product on hold if the product that you wish to pick is damaged or missing. You can place a whole pallet on hold or you can place one or more individual cases on hold. When you place a hold on individual cases, the number of units placed on hold depends on whether the account is a regular account or a reserve logic account.
For regular accounts, the hold applies to the remaining number of units on the order line. For reserve logic accounts, the hold applies to the remaining number of units in the entire warehouse up to the inventory level that you are reserving at. For example, if you reserve at level 2 and place a partial hold on pallet ID 123, the hold will apply to all pallet ID’s in your warehouse for the same level 1 and 2 values.
When you place product on hold, AccellosOne 3PL creates a new line for the missing or damaged product and then attempts to allocate the line. For example, suppose you have two orders lines, one of which is missing 10 cases. AccellosOne 3PL will create a third order line for the order with a quantity of 10 cases and then attempt to allocate this line.

Product placed on hold in RFPIC will be assigned the hold code of SUSP (Suspend) in LOEN (Look Up 
Inventory).
1 Enter RFPIC.
2 Retrieve the order that you wish to process.
3 Use your arrow keys to position your cursor over the order line that you wish to pick and press F3 (Select).

RFPIC screen showing prompt for from location
REQUIREMENTS
MRFP Suspended holds are not available if the Allow Suspended Holds field in MRFP (RFPIC tab) is set to “Split Order Line, No Suspended Holds”.
Suspended holds may require the approval of a supervisor.

4 Do one of the following:
5 If a supervisor is required to approve the hold, the Supervisor Screen will appear.
RFPIC Supervisor screen
If you wish to place the whole pallet on hold:
If you wish to place one or more cases on hold (nonreserve logic account):
If you wish to place one or more cases on hold (reserve logic account):
a) Press F3 (Hold). 
RFPIC screen showing prompt to place pallet on hold
b) If you wish to accept the variance, key in Y for Yes and press Enter. If you do not accept the variance and wish to re-enter the pick quantity, key in N for No and press 
Enter.
a) Enter or scan in your from location.
b) Enter or scan in your UI.
c) Key in the number of units that are NOT on hold and press 
Enter. 
RFPIC screen showing an allocated quantity of 5 cases and a pick quantity of 3 cases
d) If you wish to accept the variance, key in Y for Yes and press Enter. If you do not accept the variance and wish to re-enter the pick quantity, key in N for No and press 
Enter.
▪ If you keyed in Y for Yes, AccellosOne 3PL will create a new line for the remaining number of units — that is, the number of units on hold. 
a) Enter or scan in your from location.
b) Enter or scan in your UI.
c) Key in the number of units that are NOT on hold and press 
Enter.
d) Press F3 (Hold) to place the remaining units in your warehouse on hold.
e) If you wish to accept the variance, key in Y for Yes and press Enter. If you do not accept the variance and wish to re-enter the pick quantity, key in N for No and press 
Enter.

After signing on, the supervisor will be prompted to accept or reject the hold.
RFPIC Supervisor screen showing mismatched quantity
6 If the supervisor approves the hold, enter or scan in your staging location.
7 When the pick list of unpicked order lines appears, do one of the following:

### ENTERING PALLET INFORMATION <a id="entering-pallet-information"></a>

If the Display Pallet Screen field in MRFP (RFPIC tab) is set to either Display Before Picking or Display on 
Completion of Picking, you will be prompted to enter pallet information for the order.
1 Enter RFPIC.
2 Enter your zone and/or warehouse and order number in the usual manner.
RFPIC screen showing Pallet Block
If you placed the entire pallet on hold in step 4:
If you placed one or more cases on hold in step 4:
a) Process the remaining order lines in the normal manner.
a) Select the new line created by 
AccellosOne 3PL for the remaining number of units.
b) Process this line in the normal manner.
c) Process the remaining order lines in the normal manner.

3 When the Pallet Block appears, do one of the following:
4 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
5 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
6 Key in your pallet code and press Enter or use your pick list to select it.
7 Key in the number of pallets that you are shipping or receiving and press Enter.

RFPIC screen showing prompt for reference information
8 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not require a remark, press Enter to bypass this field.
9 If required, repeat the above steps to add additional lines in the Pallet Block.
10 When you finish adding your lines, press F4 to exit Create Mode. AccellosOne 3PL will display the last pallet details record that you entered. If you have multiple pallet transactions for this order, you can use your up and down arrow keys to scroll through the list of records.
If you wish to record pallet information for the order:
If you do NOT wish to record pallet information for the order:
a) Proceed to next step. a) Press F4 twice to exit the Pallet 
Block.
b) Continue to process the order in the normal manner.
Received Received means that you are receiving pallets from the account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 of your own pallets so that there is no change to your pallet balances.

If you wish to delete a pallet transaction, select the transaction that you wish to delete with your arrow keys. Then press Enter until your cursor is positioned in the NUM PALL field and press F2 (DE).
11 Press F4 again to exit the Pallet Block.
12 Continue to process your order in the normal manner.

### EXCLUDING ORDERS FROM OVERPICKING IN EOSU <a id="excluding-orders-from-overpicking-in-eosu"></a>

If the overpicking of order lines is activated in PIPR for a given customer, item or consignee, you can override the flag — that is, exclude an individual order from overpicking — in EOSU (Exclude Orders from Substitution/Overpicking). When an order is excluded from overpicking, the to ship quantity cannot exceed the order quantity.
1 Enter EOSU.

EOSU screen
2 In the Mode field, select Over-Pick from the dropdown list.
3 Key in your search criteria for the orders that you wish to exclude and click on Execute Query to execute the query.

EOSU screen showing all open orders for carrier ABC
4 Proceed to select the orders that you wish to exclude from overpicking as follows:
5 When you finish selecting your orders, click on Enable RF Overpick . The Substitution Flag beside the selected order(s) will change from N or blank to Y. If you make a mistake and wish to reverse your action, select the orders that you enabled and click on Disable RF Over-Pick .
6 Click on Exit to exit EOSU.

### PICKING PICK LINE PRODUCT FROM A NON-PICK LINE LOCATION <a id="picking-pick-line-product-from-a-non-pick-line-location"></a>

You can allow operators to pick pick line product from a non-pick line location such as bulk or rack when multiple replenishments for the same product cause overcrowding in your pick line. This choice is available when the full order quantity is not available in the pick line location and a replenishment has been generated.
If you wish to: You:
select a single order click in the checkbox beside the order select all orders click on Select All deselect a single order click in the checkbox beside the selected order deselect all orders click on Deselect All 

For example, suppose your order quantity is 10 cases, there are only five cases in the pick line and the replenishment quantity is 60 cases. The operator can choose to pick the 10 cases from a bulk or non-pick line location instead of waiting for a replenishment and picking from the pick line. The 10 cases picked from bulk is subtracted from the replenishment quantity; 60 -10 = 50.
RFPIC screen showing prompt to pick from replenishment location rather than pick line location
To activate pick line picking from a non-pick line location, you must set the flag in MRFP called Allow Picking 
Outside of Pick Line to Yes.

### PERFORMING REPLENISHMENTS IN RFPIC <a id="performing-replenishments-in-rfpic"></a>

You can allow operators to perform replenishments in RFPIC if their equipment permits it; you can either allow it on a permanent basis or you can give each operator the choice each time that he or she logs on.
You define your RF pick line/replenishment rules in a field in MRFP called Replenishment Rules for Pick Line. 
There are three options in this field:
1) REPI is done inside of RFPIC
2) REPI is done separately (that is, in RFRP or RFPL)
3) Determined by the user

### LOOKING UP REMARKS AND MESSAGES IN RFPIC <a id="looking-up-remarks-and-messages-in-rfpic"></a>

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
1 Enter RFPIC and retrieve the order whose remarks/messages you wish to look up. The remark/message will display automatically when you retrieve the order.

RFPIC screen showing header and line remarks
2 If the remarks are more than six lines long, use your up and down arrow keys to scroll through the remark lines. 
3 If there are multiple remarks/messages attached to the order, press Enter or F4 to jump to the next message.

4 Continue to process the order normally.

### RECOVERING FROM A DROPPED CONNECTION <a id="recovering-from-a-dropped-connection"></a>

If equipment tracking is activated in your system and if your RF connection is dropped in the middle of a pick (that is, you have selected an order line to pick and validated the UI but have not yet assigned an OPID to it), you will be prompted to select one of the following two options:
▪ finish the pick using your existing material handling equipment code
▪ change your material handling equipment code and exit the order without completing the pick
1 When you re-enter RFPIC/RFOLP, the following screen will appear:
RFPICK screen showing prompt to continue
2 Press Enter to continue.

RFPICK screen showing prompt to stage or exit
3 Do one of the following:
If you wish to stage the product with your existing material handling equipment code:
If you wish to change your material handling equipment code and exit the order without completing the pick:
a) Press F3 (Stage).
RFPIC screen showing prompt for to location
b) Scan or manually enter your staging location.
a) If prompted to do so, perform any required equipment checks.
a) Press F4 (Exit).
RFPIC screen showing prompt for MHE code
b) Key in your new equipment type code and press Enter.
c) If prompted to do so, perform any required equipment checks.

### Performing Inventory Count Backs <a id="performing-inventory-count-backs"></a>

You can perform inventory counts while picking in RFPIC if the Activate Inventory Count flag in MRFP is set to a value other than Never and if the order has not been assigned to a load in ENOR whose load type excludes count backs.
If the count does not match the on hand quantity, an inventory discrepancy record will be created in the program ICIN (Inventory Count Investigation). Depending on the option that you choose in the Inventory 
Count Rules field in MRFP, a supervisor may be required to log on and flag the discrepancy as either resolved or unresolved before you can pick the order line.
There are six steps to follow in performing count backs:

### PERFORMING THE COUNT IN RFPIC <a id="performing-the-count-in-rfpic"></a>

1 Enter RFPIC.
Product is assigned to load.
Supervisor login
ICIN
If second count fails, supervisor must login to authorize.
Supervisor can resolve the discrepancy in 
ICIN, RFCI or RFCL.
SELO
RF operator prompted to enter quantity of remaining product in location.
Operator count matches system count?
End recount
Yes No
Resolved?
End
Yes No
Resolved?
End
Yes No
OLOP
If discrepancy is still unresolved, operator will not be allowed to load the product.
End
Discrepancy record created. 3

2 Retrieve the order that you wish to pick.

RFPIC screen showing pick list of order lines
3 Select the order line that you wish to pick.
4 Enter your from location.
5 Enter your UI value.
6 Key in your pick quantity and press Enter.

RFPIC screen showing prompt for remaining quantity
7 Key in the quantity of product remaining in the location and press Enter. If the location contains mixed product, count only the product that you are picking.

8 Do one of the following:
9 Continue to pick the order in the normal fashion.

### LOOKING UP INVENTORY DISCREPANCY RECORDS IN ICIN <a id="looking-up-inventory-discrepancy-records-in-icin"></a>

You look up inventory discrepancy records in ICIN (Inventory Count Investigation). Inventory discrepancy records remain in ICIN until you delete them or assign them to a work request in CRME (Enter CRM 
Request).
1 Enter ICIN.
2 Click on Enter Criteria.
If the quantity that you enter matches the on-hand quantity:
If the quantity that you enter does NOT match the on hand quantity:
a) Proceed to next step. The following message will appear:
a) Press Enter to acknowledge the message and re-enter your count.
b) Key in the remaining quantity again and press Enter.
c) If prompted to do so, press Enter again to acknowledge the “Incorrect 2nd Count” message.
d) If the Supervisor Screen appears, a supervisor must log on and enter either Y to flag the discrepancy as resolved or N to flag the discrepancy as unresolved.
e) Proceed to next step.

3 Do one of the following:
4 Click on Execute Query.

ICIN screen showing a discrepancy for item 11111
5 Use your arrow keys to scroll through the list of records. 
6 When you finish viewing your inventory discrepancy records in ICIN, click on Return to Main and Exit.

### LOOKING UP INVENTORY DISCREPANCY RECORDS IN RFCL <a id="looking-up-inventory-discrepancy-records-in-rfcl"></a>

You must have supervisor access in OPER (Operator Code) before you can look up inventory discrepancy records in RFCL (RF Count Log).
1 Enter RFCL.
If you wish to view all records in 
ICIN:
If you wish to restrict your query to certain records:
a) Proceed to next step. a) Enter the appropriate search criteria (order number, line number, operator code, etc.).

RFCL screen
2 Do one of the following:
3 Click on Execute Query.

RFCL screen showing discrepancy record for item D1
4 Use your arrow keys to scroll through the list of records. 
5 When you finish viewing your inventory discrepancy records in RFCL, press F4 to exit.

### REMOVING INVENTORY DISCREPANCY RECORDS FROM ICIN <a id="removing-inventory-discrepancy-records-from-icin"></a>

There are two methods of removing records from ICIN: you can delete the record using the Delete command or you can create a work request for the discrepancy in CRME and AccellosOne 3PL will delete the record automatically. Regardless of the option that you choose, AccellosOne 3PL will create an IF (Information Only) 
record in the History Block of LOEN.
If you wish to view all records in 
RFCL:
If you wish to restrict your query to certain records:
a) Proceed to next step. a) Enter the appropriate search criteria (UI number, order number, customer code, etc.).

1 Enter ICIN.
2 Retrieve the record that you wish to remove.
3 Do one of the following:
4 Click on Return to Main and Exit.

### REMOVING INVENTORY DISCREPANCY RECORDS IN RFCL <a id="removing-inventory-discrepancy-records-in-rfcl"></a>

You must have supervisor access in OPER (Operator Code) before you can remove inventory discrepancy records in RFCL (RF Count Log).
1 Enter RFCL.
2 Retrieve the record that you wish to remove.
3 Press F3 (Rm).
4 When the message “Record is Deleted Enter to Continue” appears, press Enter to continue.
5 Press F4 to exit.

### REMOVING INVENTORY DISCREPANCY RECORDS IN RFCI <a id="removing-inventory-discrepancy-records-in-rfci"></a>

This program allows RF supervisors to clear inventory investigations when there are multiple ICIN records for the same inventory entity. There are three different options in RFCI:
▪ you can clear the currently selected OPID
▪ you can clear all OPID's on open orders with the same inventory levels up to level 3
▪ you can exit out without clearing any OPID's (that is, the variance remains unresolved)
When you clear an ICIN record, any SUSP holds on the product are removed.
1 Enter RFCI.
If you wish to delete the record: 
If you wish to create a work request in CRME:
a) Click on Delete.
b) If required, enter your remarks for the transaction.
a) Click on CRM Entry.
b) Click on Create Record.
c) Proceed to enter your work request. Refer to the Operations 
2 Guide for further information on entering work requests in CRME.
d) When you finish entering your work request, click on Exit.

RFCI screen
2 Enter or scan the OPID that you wish to clear.
RFCI screen showing three options
3 If there are multiple records for a single OPID, use your arrow keys to select the record that you wish to clear.
4 Press Enter to position your cursor in the Option field.
5 Key in the appropriate option (1, 2 or 3) and press Enter.

### Entering Temperature and Trailer Information in RFTT <a id="entering-temperature-and-trailer-information-in-rftt"></a>

This program allows you to enter temperature, trailer/seal number and pallet information for a given receipt or order without working in RFCH or RFPIC. The information that you can enter in RFTT for a receipt — temperature only, trailer/seal number only, temperature and trailer/seal number, etc. — depends on which option you choose in the Show Temperature and Pallet Blocks field in MRFP.
1 Enter RFTT.

RFTT screen
2 Key in your order number and press Enter.
3 Enter your temperature, trailer/seal number and pallet information in the usual manner.

### Entering Pallet Information in RFOPE <a id="entering-pallet-information-in-rfope"></a>

If the Pallet Block is deactivated in RFPIC, you can use the stand-alone program RFOPE (RF Order Pallet 
Entry) to enter your pallet information.
1 Enter RFOPE.
RFOPE screen
2 Key in your order number and press Enter.

RFOPE screen showing prompt for account code
3 Key in your account code and press Enter or use your pick list to select it. To select a code using the pick list, press F10 to display the pick list and use your up and down arrow keys to select the appropriate code. Then press Enter to make your selection. The account is the party (customer, shipper or carrier) 
that you are receiving pallets from or shipping pallets to.
RFOPE screen showing prompt for transaction type
4 In the Type field, key in the appropriate value for your pallet transaction (R for Received, S for Shipped or 
E for Exchanged) and press Enter. 
5 Key in your pallet code and press Enter or use your pick list to select it.
Received Received means that you are receiving pallets from the account that you specified in the previous field.
Shipped Shipped means that you are shipping pallets to the account that you specified in the previous field.
Exchanged Exchanged means that you are performing an even exchange of pallets; for example, you receive 10 pallets from a given account and you give this account 10 of your own pallets so that there is no change to your pallet balances.

6 Key in the number of pallets that you are shipping or receiving and press Enter.

RFOPE screen showing prompt for reference information
7 If required, key in a remark for the pallet transaction in the Reference field and press Enter. If you do not require a remark, press Enter to bypass this field.
8 If required, repeat the above steps to add additional lines in the Pallet Block.
9 When you finish adding your lines, press F4 to exit Create Mode.
10 Press F4 again to exit RFOPE.

### EDITING A PALLET DETAILS RECORD IN RFOPE <a id="editing-a-pallet-details-record-in-rfope"></a>

If pallet details have already been entered for an order in RFPIC or ENOR, you can edit the pallet details in 
RFOPE.
1 Enter RFOPE.
2 Key in your order number and press Enter.
RFOPE screen showing existing pallet details record
3 Proceed to make any required changes to your pallet details.
4 When you finish making your changes, press F4 the required number of times to exit.

### DELETING A PALLET DETAILS RECORD IN RFOPE <a id="deleting-a-pallet-details-record-in-rfope"></a>

1 Enter RFOPE.
2 Key in your order number and press Enter.
3 Press Enter until your cursor is in the NUM PALL field.
RFOPE screen showing existing pallet details record
4 Press F2 (DE).
5 Press F4 the required number of times to exit.

### Adjusting Your Pallet Type in RFPA <a id="adjusting-your-pallet-type-in-rfpa"></a>

You can adjust your pallet type for an OPID (outbound pallet ID) in RFPA (RF Pallet Code Update). If the 
OPID has already been assigned a pallet type, the CUR PALL TYPE field will be populated with the current pallet type. If the OPID has never been assigned a pallet type, the CUR PALL TYPE field will be blank.
1 Enter RFPA.
RFPA screen

2 Enter or scan in your OPID.
RFPA screen showing current pallet type plus prompt for new pallet type
3 If you make a mistake, you can press F3 (CL) to clear the OPID and start over again.
4 Key in your new pallet type and press Enter or press F1 (PL) to select it from the pick list.
RFPA screen showing “Enter to continue” message
5 Press Enter to confirm the update.
6 Press F4 to exit.

### Looking Up Your OPID’s <a id="looking-up-your-opid-s"></a>

There are three ways of looking up your OPID’s (outbound pallet ID’s):
▪ from the desktop program LOCN (Look Up Carton)
▪ in the RF program RFNCO (OPID Look-Up)
▪ from the desktop program LOOR (Look Up Orders)

### LOOKING UP YOUR OPID’S IN LOCN <a id="looking-up-your-opid-s-in-locn"></a>

You can look up OPID’s (outbound pallet ID’s) in LOCN (Look Up Carton). OPID’s are created when you perform case picking in RFPIC. When you look up OPID’s, AccellosOne 3PL shows the customer code, level 
1 value, order number and line number for each inventory entity on the pallet.
1 Enter LOCN.
2 Click on Enter Query.
3 Enter or scan in your OPID and click on Execute Query.
LOCN screen showing three inventory entities on the pallet
4 When you finish looking up your OPID, click on Exit to exit.

### LOOKING UP YOUR OPID’S IN RFNCO <a id="looking-up-your-opid-s-in-rfnco"></a>

This RF program allows you to look up the product on an OPID (outbound pallet ID). It is similar to RFCO (RF 
Confirm OPID) but without the F3 (Process) command.
The Line Block shows each order line assigned to the OPID; that is, the order number, line number, customer, all inventory levels, the staging location and the quantity. Records in the Line Block are sorted by date and time stamp based on the STPI (Start Picking) flow with the oldest records shown first followed by the newer records.
1 Enter RFNCO.

RFNCO
2 Key or scan in your OPID.
RFNCO screen showing two order lines attached to OPID 00002240
3 If there are multiple records in the Line Block, you use your Up and Down arrow keys to scroll through the list.
4 When you finish looking up your OPID’s, press F4 the required number of times to exit.

### LOOKING UP AN ORDER’S OPID’S IN LOOR <a id="looking-up-an-order-s-opid-s-in-loor"></a>

You can look up an order’s OPID’s in the Location Block of LOOR.

LOOR screen showing OPID for order line 1

### Confirming Orders by OPID in RFCO <a id="confirming-orders-by-opid-in-rfco"></a>

This program allows you to confirm orders by OPID (outbound pallet ID) without the need to confirm the entire order in CHOF. If an OPID contains multiple order lines, you can confirm individual orders lines or you can confirm all order lines assigned to the OPID. If you choose to confirm individual order lines, the Shipped Date field in the Line Block of LOOR will be populated for each order line confirmed in RFCO.
1 Enter RFCO.
REQUIREMENTS
FLOWS The order must be picked.
DOCUMENTS You cannot use RFCO if you print one or more documents at your FIPI (Finish 
Picking) flow because the flow FIPI is bypassed in RFCO. To use RFCO, you must move your document(s) to the COOR (Confirm Order) flow.
OTHER See Miscellaneous 2 tab in MRFP.

RFCO screen
2 Press Enter to scan in your OPID.
RFCO screen showing F3 (Process command)

3 Do one of the following:
4 Repeat the above steps for another OPID or press F4 (EX) to exit.

### Confirming Individual Order Lines by UI in RFCU <a id="confirming-individual-order-lines-by-ui-in-rfcu"></a>

This program allows you to confirm individual order lines by UI. When you look up the order in LOOR, the 
Shipped Date field in the Line Block will be populated for each order line confirmed in RFCU.
1 Enter RFCU.
To confirm individual order lines:
To confirm all order lines assigned to the OPID:
a) Press F1 (LN) to enter the Detail 
Block of RFCO.
b) Use your arrow keys to scroll through the list of order lines.
c) When you reach the order line that you wish to confirm, press 
Enter to select it.
d) When prompted to confirm the order line, press Enter to accept the default value of Y(es).
a) Press F3 (PR) to process it.

RFCU
2 Key in your order number and press Enter.
3 Scan in your UI value.
RFCU screen showing prompt to continue
4 Press Enter to confirm the order line.
5 Press F4 to exit.

### Reprinting Outbound Labels in RFOLP <a id="reprinting-outbound-labels-in-rfolp"></a>

In this program, you can reprint outbound labels for orders that have already been picked in RFPIC. There are two reprint modes in RFOLP depending on the outcome of label printing in RFPIC.
If the original label printed correctly in RFPIC, you enter the UI value of the order line or the OPID of the original label in RFOLP. If label printing failed in RFPIC due to a lost connection or loss of power, AccellosOne 
3PL will generate an internal tag number and attach this tag number to all order lines that have been picked. 
The way that you process these order lines that have been picked depends upon how you create your 
OPID’s:

▪ if you manually create your OPID’s, you must enter ENOR and change the tag number in the Process 
Block to the desired OPID number and use this number as your OPID number (AccellosOne 3PL will replace the tag number for all order lines that have been picked by the new OPID number)
▪ if your OPID’s are system generated, you must enter LOOR and look up the tag number assigned to the order line in the Process Block and use this tag number as your OPID number (when you finish reprinting in RFOLP, AccellosOne 3PL will assign the new system-generated OPID number to all order lines that have been picked)

LOOR screen showing tag number generated in Process Block when label printing fails
1 Do one of the following:
2 Enter RFOLP.
REQUIREMENTS
CASE PICKING See RFPIC.
If you wish to reprint a previously printed label:
If you need to create a new label because label printing failed in 
RFPIC:
a) Proceed to next step. a) Enter LOOR.
b) Retrieve the order whose label printing failed.
c) Open the Process Block and look up the system-assigned tag number. Use this value as your 
OPID.

RFOLP screen
3 Key in your order number and press Enter.
4 Do one of the following:

RFOLP screen showing prompt for number of labels to print
5 Key in the number of labels that you wish to print/reprint and press Enter.
6 Do one of the following:
If you wish to scan in the UI value:
If you wish to scan in the outbound pallet ID:
a) Enter or scan in your UI value.
b) If a single UI value has multiple 
OPID’s, select the appropriate 
OPID from the pick list.
a) Press Enter to bypass the UI field.
b) Enter or scan in your OPID.
If the printer code is displayed:
If the printer code is NOT displayed:
a) Press Enter to accept it or key in a new printer code and press 
Enter.
a) Key in your printer code and press Enter.

### Picking Cases from a Pick Line in CASE <a id="picking-cases-from-a-pick-line-in-case"></a>

In this program, you can pick partial quantities (that is, less than a full pallet) from a pick line in Skip mode. In 
Skip mode, automatic replenishment is deactivated and the picker can select any pick line inventory from any pick line location whose level 1 value matches the level 1 value of the order line.
CASE is designed for fast-moving pick lines in which old product (that is, allocating in FIFO/LIFO sequence) 
is not an issue and manual procedures are in place to ensure that the pick line never runs out of product. If you activate Skip mode, you will not be able to pick partial quantities from a pick line in RFPIC.
When you allocate an order in Skip mode, the following events occur in AccellosOne 3PL:
▪ the P-type order line for the pick line quantity will not be changed to R for Regular
▪ the Location Status field of the order header will be updated to “Entered”, but no locations will be assigned to the order lines
▪ no replenishments will be generated
NOTE If the order quantity is such that both a bulk pick and a pick line pick are required (for example, order quantity = 110 cases or 1 pallet/10 cases), AccellosOne 
3PL will create a second order line for the pick line pick. However, the non-pick line pick will allocate normally; that is, the P-type line will change to R for Regular.
REQUIREMENTS
FLOWS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
CASE PICK LABEL See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
INVENTORY LEVELSCASE supports three-level accounts only.
OTHER You need a pick line for the product that you wish to pick in CASE. See the Allocation and Wave Manager for instructions on setting up a pick line.
In the DSRP (Depositor Shipping and Receiving) record attached to the customer that you are setting up for CASE picking, the Change Zero Pending Line to RType Line field must be set to N for No.
In the PIPR (Picking Profile) record attached to the customer that you are setting up for CASE picking, the following setups are required:
▪ Use FIFO/LIFO for Pick Line Picking or Skip = S for Skip
▪ Exclude Pick Line Stock When Bulk Picking = Y for Yes

PIPR screen showing required setup for CASE
REQUIREMENTS

1 Enter CASE.

CASE screen
2 Enter or scan in your order number.
PROCESS VALUESSee [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
SCAN PARAMETER CODEOnly required if you are scanning process values, inventory levels or UI values from a bar code label
See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
BAR CODE PROFILEOnly required if you are scanning a UI value or inventory levels from a bar code label
See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
HOLDS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
REQUIREMENTS

CASE screen showing pick list of possible pick locations for order line 1
AccellosOne 3PL will display all locations in the pick line containing the product whose level 1 value matches the level 1 of the order line. For each location, CASE will display the order line number, warehouse, level 1 value and pick quantity.
3 Use your arrow keys to position your cursor over the order line/location that you wish to pick, then press 
F3 (Select).

CASE screen showing prompt for UI value
4 If you make a mistake and wish to work on another order or order line, press F2 (QU for Quit) to position your cursor in the Ord# field. Then enter or scan in another order number or press Enter to work on the same order but a different order line.
5 Enter or scan in your UI value.
Record 1
Record 2

CASE screen showing prompt for pick quantity
6 Key in your quantity and press Enter. The quantity that you enter must be less than or equal to the available quantity in the location.
7 Repeat the above steps for each additional order line to be picked from the pick line.
8 When you finish picking all your order lines, the “Case pick completed” message will appear. Press F4 (Rt) to display the case pick label screen.

CASE screen showing case pick label screen
9 Do one of the following:
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that are not generated in AccellosOne 3PL: If the Label field is populated:
a) Press Enter to generate your pallet ID.
b) Key in your printer code and press Enter.
a) Enter or scan in your pallet ID. a) If the PRT (Printer) field is not populated, key in your printer code and press Enter.
Available quantity in location 

CASE screen showing completed case pick label screen
10 Press F4 (Rt) to close the case pick label screen.
11 Press F4 (EX) again to exit CASE.

### Merging OPID’s in RFOPB <a id="merging-opid-s-in-rfopb"></a>

In this program, you can merge two or more separate picks (a case pick and an each pick) into a single pallet under a new OPID. When you finish merging your picks, you will be prompted to print a label for the new 
OPID.
1 Enter RFOPB.
REQUIREMENTS
FLOWS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
CASE PICKING See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
ENOR Each pick must be a separate order line on the same order.
LABELS You need a label set up in DOCU and this label must be attached to the appropriate customers and consignees in CCDU (Customer / Consignee Document 
Setup). The pick method must be set to each.

RFOPB screen
2 Enter or scan your new OPID.
RFOBP screen showing prompt for carton ID
3 Enter or scan in your first OPID.
RFOBP screen showing prompt for carton ID

4 Enter or scan in your second OPID.
5 Enter or scan in any additional OPID’s that you wish to merge.
6 When you finish scanning in your from OPID’s, press F3 (Process).
RFOBP screen showing prompt for printer code
7 Key in your printer code and press Enter.
8 Press F4 to exit.

### LOOKING UP YOUR NEW OPID <a id="looking-up-your-new-opid"></a>

You can look up your new OPID in the Time Block of LOOR.
LOOR screen showing new OPID

### Picking Substitution <a id="picking-substitution"></a>

Picking substitution allows RF operators to pick product other than the allocated product on the order line. 
Depending on the options that you choose, the substitute product:
▪ may or may not be allocated to another order
▪ may or may not be from the same location
▪ may or may not have the same FIFO attributes
▪ may or may not have the same level 2/3/4 values 
Regardless of the option that you choose, if the original order line has a hold code, the substitute product must have the same hold.
Picking substitution is designed to achieve faster picking and increased productivity for the warehouse by allowing operators to pick the most accessible product in a given location or area without sacrificing FIFO or other picking requirements.
It is only available for RF picking in the program RFPIC. When the picker enters an inventory level value other than the value of the allocated line, AccellosOne 3PL will evaluate a) whether picking substitution is allowed and b) if it is allowed, whether the product picked as a substitute is acceptable.
If picking substitution is not activated, the picker can only pick product not on the order line if reserve logic is activated.

### SETTING UP PICKING SUBSTITUTION <a id="setting-up-picking-substitution"></a>

There are three steps to follow in setting up picking substitution.
▪ You set up your picking substitution rules in PSPR (RF Substitution Profile Code). 
▪ You attach your RF substitution profile code to PIPR (Picking Profile Code). 
▪ You attach your PIPR profile code to the appropriate records in ITEM, CONS, CCOP, HOLD or DSRP.
NOTE Picking substitution offers more flexibility at picking time than does reserve logic. You can pick product from a location other than the pick location, you can pick product whose level 2/3/4 value is not an exact match of the product on the order, you can pick product with a variable quantity breakdown and you can pick product on another open order.

### SETTING UP YOUR PICKING SUBSTITUTION RULES IN PSPR <a id="setting-up-your-picking-substitution-rules-in-pspr"></a>

You set up your picking substitution rules in PSPR. Picking substitution rules are always location type dependent; that means that you can set up one set of picking substitution rules for your rack locations and a completely different set of picking substitution rules for your pick line locations.
FIELD DESCRIPTIONS
Substitution Profile Code Mandatory
Your RF substitution profile code.
Description Mandatory
The description for your RF substitution profile code.
Enable Replenishment 
Substitution
Y = Yes
N = No
If you select Y for Yes, your picking substitution rules will apply to replenishments as well. If you select N for No, your picking substitution rules will apply to picking only.
LOCATION TYPE BLOCK
Location Type Code (defined in LOTP)
Mandatory
The location type code for your RF substitution profile code.
Sort Sequence Code (defined in SOSE)
Optional
If you attach a SOSE code to your location type, the substitution pick list in 
RFPIC will be sorted in the order that you specify.

Range in Days Mode A = Allocated Lot, allocation time (default)
O = Oldest Lot
If you select A for Allocated Lot, your range in days value will be based on the originally allocated product’s receipt/expiry date. If you select O for Oldest Lot, your range in days value will be based on the oldest lot at the time of allocation.
Range in Days from Originally Allocated EntityOnly available if Range in Days Mode = blank or A for Allocated Lot, if relative 
FIFO picking is activated in PIPR and if the PSPR rule “Substitute product must have equivalent FIFO attributes” is chosen
The number of days that the substitute product’s receipt/expiry date can exceed the originally allocated product’s receipt/expiry date. 
EXAMPLE
Suppose you set the Range in Days from Oldest Lot to 10 in PIPR and the 
Range in Days from Originally Allocated Entity in PSPR to 5. During allocation, AccellosOne 3PL selects Jan. 7 as the lot to pick even though the oldest lot is Jan. 1. If the picker elects to pick substitute product in RFPIC, any lot up to Jan 12 will be accepted.
If you leave this field blank, the value of zero will be assumed and the substitute product’s receipt/expiry date must match the original product’s receipt/ expiry date. 
NOTE If your customer has specific FIFO rules such as never ship anything with a date greater than 20 days from the oldest lot, you must make sure that the sum of the Range in Days from Oldest Lot value in PIPR and the 
Range in Days from Originally Allocated Entity value in PSPR does not exceed 20. 
For example, you could set both values to 10 (10 + 10 = 20) or your PIPR value could be 15 and your PSPR value could be 5. However, you could not set your PIPR value to 15 and your PSPR value to 10 because product with a date greater than 20 days from the oldest lot might be shipped.
Range in Days from Oldest Lot During AllocationOnly available if Range in Days Mode = O for Oldest Lot, if relative FIFO picking is activated in PIPR and if the PSPR rule “Substitute product must have equivalent FIFO attributes” is chosen
The number of days that the substitute product’s receipt/expiry date can exceed the oldest lot at the time of allocation. 
LOCATION TYPE BLOCK

There are five logical groups in PSPR. Each group has two or more mutually exclusive options. From each group, you select the appropriate option.
1 Enter PSPR.
2 Click on Create Record.
3 Key in your substitution profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 In the Enable Replenishment Substitution field, key in N for No or Y for Yes and press Enter.
6 In the Location Type Block, click on Return to Main.
7 Click on Create Record.
8 In the Location Type field, key in your location type code and press Enter or use the pick list function to select it.
Do not use stock allocated to other orders as substitute
Use stock allocated to other orders for same location only (not available if the picking substitution profile code attached to the customer differs from the picking substitution code attached to the consignee)
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
The traditional range in days mode option looks at a single order only. The extended range in days option, on the other hand, looks at all allocated order lines. For example, if your range in days value is 5, the substitute product’s receipt/expiry date can exceed the receipt / expiry date of any allocated product that has not been picked.
NOTE The picking substitution rules that you define in PSPR override any picking parameters that you define in ILOP. For example, if you select “pick to clean” in ILOP and if the operator decides to pick from another location, that location may not satisfy the pick to clean requirement. In other words, the operator may pick from a less desirable location according to ILOP.

9 If required, key in your sort sequence code and press Enter or use the pick list function to select it. If you do not require a sort sequence code, press Enter to bypass this field.
10 In the Range in Days Mode field, key in A for Allocated Lot or O for Oldest Lot and press Enter.
11 If required, key in the number of days in the Range in Days from Originally Allocated Entity field and press Enter.
12 In the Available Options Block, use your arrow keys to position your cursor beside the parameter that you wish to choose and then click on Add Option.
13 Repeat the previous step for each set of parameters.
14 When you finish selecting your parameters, click on Location Type Block.

PSPR screen showing picking rules for BULK options
15 Click on Master Block and Exit to exit.

### ATTACHING YOUR PSPR PROFILE CODE TO THE APPROPRIATE CODE <a id="attaching-your-pspr-profile-code-to-the-appropriate-code"></a>

First, attach your PSPR profile code to PIPR (Picking Profile Code). Next, attach your PIPR profile to the appropriate code (ITEM, CONS or DSRP). If you are attaching picking profiles to items and consignees as well to customers, the following logic will apply:
▪ the profile that you attach to DSRP is the default
▪ if you attach a picking profile to ITEM, it will override the profile in DSRP
▪ if you attach a picking profile to CONS, it will override the profiles in DSRP and ITEM (you cannot use the “Use stock allocated to other orders for same location” option in PSPR when attaching a picking profile to CONS)

### EXCLUDING ORDERS FROM PICKING SUBSTITUTION IN EOSU <a id="excluding-orders-from-picking-substitution-in-eosu"></a>

You can exclude open orders from picking substitution in EOSU (Exclude Orders from RF Substitution). When you exclude an order from picking substitution, the following restrictions apply:
▪ only product on that order can be picked (other product cannot be substituted for the product on the order)
▪ product on that order cannot serve as a substitute for product on another order
EOSU shows all open orders that can be excluded from picking substitution. The Substitution flag shows the current status of each order. A value of Y or blank indicates that picking substitution is enabled for the order. 
A value of N indicates that the order is excluded from picking substitution.
1 Enter EOSU.

EOSU screen
2 Key in your search criteria for the orders that you wish to exclude and click on Execute Query to execute the query.

EOSU screen showing all open orders for carrier ABC
3 Proceed to select the orders that you wish to exclude from RF substitution as follows:
4 When you finish selecting your orders, click on Enable RF Substitution . The Substitution Flag beside the selected order(s) will change from N or blank to Y. If you make a mistake and wish to reverse your action, select the orders that you enabled and click on Disable RF Substitution .
5 Click on Exit to exit EOSU.

### PERFORMING PICKING SUBSTITUTION IN RFPIC <a id="performing-picking-substitution-in-rfpic"></a>

If substitute product can come from a location other than the originally allocated location, you pick substitute product in RFPIC by entering the location of the substitute product followed by its UI value. If, however, 
If you wish to: You:
select a single order click in the checkbox beside the order select all orders click on Select All deselect a single order click in the checkbox beside the selected order deselect all orders click on Deselect All 

substitute product must come from the originally allocated location, the Location field will be filled in with the original location and you enter the UI value of the substitute product only.
If you enter a location other than the pick location and that location does not hold any substitute product, 
RFPIC will display a pick list showing all locations containing substitute product that is acceptable. After selecting the product/location that you wish to pick, you continue to process the order normally.
1 Make sure that your order is at the flow SUAL (Supervisor Allocated) or STPI (Start Picking).
2 Enter RFPIC.
3 Do one of the following:
4 If there is a remark attached to the order, press Enter twice to acknowledge it.
5 Do one of the following:
6 When the pick list of order lines is displayed, use your arrow keys to position your cursor over the order line that you wish to pick, then press F3 (Select).

RFPIC screen showing prompt for pick location
7 If prompted to enter your from location, enter or scan in the location of the substitute product.
If you wish to pick by zone:
If you wish to pick by order number:
a) Key in your zone code and press 
Enter.
a) Press Enter to bypass the Zone field.
b) Key in your warehouse and press Enter.
c) Key in your order number and press Enter.
If the default mode for RFPIC has been set to Case:
If the default mode for RFPIC has been set to Pallet:
The message “You have selected 
CP Mode” will appear.
a) Key in N for No and press Enter.
The message “You have selected 
NM mode” will appear.
a) Press Enter to continue.

8 Do one of the following:
9 Continue to pick the product normally in RFPIC. 
If there is NO substitute product in any location:
If there is NO substitute product in the location that you entered:
If there is substitute product in the location that you entered or the pre-filled in location:
a) The message “No subst. for all loc” will appear. You can only pick the product on the original order line.
a) The following message will appear: 
b) Key in Y for Yes and press 
Enter.
c) AccellosOne 3PL will display a pick list of acceptable substitutes. 
d) Use your up and down arrow keys to scroll through the list of substitute product.
e) When you find the product that you wish to pick, press F3 to select it.
a) Enter or scan in its UI value.

### Entering Process Values in RFOPS <a id="entering-process-values-in-rfops"></a>

You enter process values in RFOPS. There are two process values that you enter in this program: catch weight and serial number. You can scan a bar code that contains these two values or you can enter them manually.
RFOPS maintains a running total by both weight and number of pieces. The running total shows the weight and number of pieces that have been scanned in as well as the weight and number of pieces that have not been scanned in. 
If a label has been scanned in error, you can remove it by means of the Remove command. If a case has been scanned in error, you can remove it from the remaining number of cases to be scanned by means of the 
Reduce command.
REQUIREMENTS
FLOWS ENOR (Enter Order)
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFOPS. 
PROCESS VALUESFor the UCC-128 label, you require two process values in RFOPS: one for catch weights and one for serial numbers. These codes must be set up in IPRO (Item 
Process) with the Create Automatic Records flag set to Y for Yes and then attached to a profile in IPRP (Item Process Profile). The IPRP profile must in turn be attached to the item(s) requiring the process values.
Because you are capturing a weight, the item(s) should assigned the appropriate non-standard weight option in ITEM.
See the section “Item Process Values” in the Operations 2 Guide for further information about process values.
SCAN PARAMETER CODEYou need a scan parameter profile defined in SCPR (Scan Parameter Code)*. 
For the UCC-128 label, this profile must contain a minimum of two records in the 
Detail Block: one record for your scanned in weight and another record for your scanned in serial number. The SCPR profile must in turn be attached to the item requiring the process values.
If you wish to scan in your lowest inventory level as a unique identifier, you must define your scan parameters in SCPR and attach your scan parameter code to your bar code profile in BAPR (Bar Code Profile).
* not required for manual entry in RFOPS

BASE FOR CUBE/
WEIGHT
The Base for Cube/Weight flag for your case SKU in the Quantity Breakdown 
Block of ITEM must be set to Y for Yes for any product that you wish to process in 
RFOPS.
CATCH WEIGHT 
TOLRANCES
See [Setting Up Catch Weight Tolerances](expedicao-rf.html#setting-up-catch-weight-tolerances) for further information.
SORT SEQUENCE 
CODE (SOSE)
You can define a sort sequence for your process values in the RFOPS Sort 
Sequence Code (SOSE) field in MRFP.
OTHER If you pick product in RFPIC, you can only enter process values in RFOPS after picking in RFPIC. If you pick product in any other program, you can enter process values either before or after picking.
RFOPS supports alternate item codes set up in ALIT (Alternate Item and Language).
FUNCTION KEYS
All Modes
F1 ME (Manual Entry) Displays a separate window in which you can manually enter your catch weights, serial numbers and other process values.
F2 RC (Reduce Quantity) Remove a scanned case from an order line and reduce the order line quantity by one.
F3 RL (Remove Label) Remove a label that has been scanned from an order line.
F3 CM (Change Mode) Capture the weight of each case on a full pallet rather than a single weight for the full pallet. For example, the pallet contains damaged product and a single weight for the full pallet would not be accurate.
Only available after selecting F1 (ME) for manual entry.
F4 EX (Exit) Exit program or scan incomplete message.
REQUIREMENTS

1 Enter RFOPS.

RFOPS screen
2 Do one of the following:
AccellosOne 3PL will retrieve all order lines that match the criteria that you entered.
F9 Move cursor to previous field.
Pick List of Order Lines
F3 SL (Select) Selects the order line that the cursor is positioned over.
F4 CN (Cancel) Exits the pick list without selecting an order line.
If you wish to process a specific order:
If you wish to process a specific order and a specific UI/
OPID:
If you wish to process a specific UI/OPID:
a) Press F9 to position your cursor in the ORD field.
b) Key in your order number and press Enter.
a) Press F9 to position your cursor in the ORD field.
b) Key in your order number and press Enter.
c) Enter or scan in your UI/OPID value.
a) Enter or scan in your UI/OPID value.
FUNCTION KEYS

RFOPS screen showing two order lines available for processing
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 (SL) to select it.

RFOPS screen showing prompt for catch weight
Line 1
Line 2

4 Do one of the following:

RFOPS screen showing case one out of five scanned in
5 Continue to scan all pieces on the order line. If the same item is found on two or more order lines, AccellosOne 3PL will calculate a running total of the weight for all order lines containing that item.
If you wish to scan in your process values:
If you wish to enter your process values manually:
a) Scan in your label. a) Press F1 (Me). 
b) Key in your weight and press 
Enter.
c) Key in your serial number and press Enter.
Weight of first piece

RFOPS screen showing total weight by item
6 When you finish entering all your order lines, process another order line or press F4 to exit.

### CAPTURING THE WEIGHT DYNAMICALLY FROM A BAR CODE <a id="capturing-the-weight-dynamically-from-a-bar-code"></a>

The locate weight in bar code dynamically option allows you to scan in the weight from a bar coded label without knowing which numbers in the bar code represent the product’s weight. Because the format of the bar code is unknown, you cannot use SCPR (Scan Parameter Profile) to break up the code into its component parts.
The following requirements must be met before you can locate the weight in a bar code dynamically:
▪ All bar codes for a given order line must have the same length.
▪ The weight portion of the bar code for a given order line must all have the same length; if a weight is less than the full length, it must be padded with zeros.
▪ All weights for a given order line must fall within a range of 10 times heavier or lighter than the first case. 
For example, if case 1 weighs 100 lbs., case 2 cannot weigh more than 1,000 lbs. or less than 10 lbs.
▪ The locate weight option must be activated in IPRO by setting the Locate Weight in Bar Code Dynamically flag to Y for Yes for a given process code. This process code must be attached to an item process profile code in IPRP (Item Process Profile), which in turn must be attached to the appropriate item(s) in 
ITEM.
Total weight for all lines on order containing this item

IPRO screen showing Locate Weight in Bar Code Dynamically flag set to Y for Yes
The operator scans in the full bar code and then manually enters the weight for the first three cartons. If the manually entered weight matches the bar code weight in all three cartons on the same order line, AccellosOne 3PL “learns” the position of the weight in the bar code.
If the manually entered weight does not match the bar code weight, the operator will be prompted to either start over again or rescan the current carton.
EXAMPLE
9991234999 (Label 1)
9991356999 (Label 2)
9991426999 (Label 3)
Because the position of the weight in label one (positions 4 through 7) matches the position of the weight in labels two and three, AccellosOne 3PL will read the weight from these positions for all pieces on the order line.
If the same bar code is scanned twice, the operator will have two choices: accept the duplicate or enter a new bar code.
1 Enter RFOPS.
2 Do one of the following:
AccellosOne 3PL will retrieve all order lines that match the criteria that you entered.
If you wish to process a specific order:
If you wish to process a specific order and a specific OPID:If you wish to process a specific OPID:
a) Key in your order number and press Enter.
b) Press Enter to bypass the UI field.
a) Key in your order number and press Enter.
b) Enter or scan in your OPID value.
a) Press Enter to bypass the 
Order Number field.
b) Enter or scan in your OPID value.

RFOPS screen showing two order lines available for processing
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 (SL) to select it.

RFOPS screen showing prompt for weight measure code
4 Key in your weight unit of measure (1 for kilograms or 2 for pounds) and press Enter. If you made a mistake and wish to select another order line, key in 3 for Cancel and press Enter. 

RFOPS screen showing prompt to scan the bar code
5 Scan in your bar code.
Line 1
Line 2

RFOPS screen showing prompt to enter weight
6 Key in the weight and press Enter. The weight must include a decimal point. For example, to enter a weight of 20 pounds, you must key in either 20.0 or 20.00. You cannot key in 20.
7 Repeat steps 5 and 6 for your second piece.
8 Do one of the following:
If the position and weight of label 
1 matches label 2:
If the position and weight of label 
1 does NOT match label 2:
a) Repeat steps 5 and 6 for your third piece.
AccellosOne 3PL will offer you two options: you can either start over again from the first scan or repeat the second scan.
a) Press Enter to rescan or key in N for No to start over. 

9 Do one of the following:

RFOPS screen showing five pieces to scan for order line 1
10 Scan in your first piece.
If the position and weight of label 
3 matches labels 1/2:
If the position and weight of label 
3 does NOT match labels 1/2:
The following message may appear:
“Keep 3 Scans” message
a) Press Enter to start scanning or key in N for No and press Enter.
AccellosOne 3PL will offer you two options: you can either start over again from the first scan or repeat the third scan.
a) Press Enter to rescan or key in N for No to start over. 
Line #

RFOPS screen showing prompt for next piece
11 Continue to scan all pieces on the order line. If the same item is found on two or more order lines, AccellosOne 3PL will calculate a running total of the weight for all order lines containing that item.

RFOPS screen showing total weight by item
12 When you finish scanning all your pieces, process another order line or press F4 to exit.

### MANUALLY ENTERING THE WEIGHT <a id="manually-entering-the-weight"></a>

If AccellosOne 3PL is unable to locate the weight portion of the bar code, you must enter the weight of each piece manually.
1 The following message will display when there is no match between the manually entered weight and the bar code weight in two out of three labels:
Weight of first piece
Total weight for all lines on order containing this item

RFOPS screen showing “Weight positions not found” message
2 Key in 1 (Enter weight only) and press Enter.

RFOPS screen showing “Scan barcode” message
3 Manually key in the weight of the first piece and press Enter.
4 Repeat the previous step for each piece on the order line.
5 When you finish entering your weights manually, press F4 to exit.

### REMOVING LABELS THAT HAVE BEEN SCANNED <a id="removing-labels-that-have-been-scanned"></a>

You can remove labels that have been scanned in RFOPS by means of the RL (Remove) command. A removed label cannot be re-used.
1 Enter RFOPS.
2 Enter or scan in your order number and/or UI number.
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 (SL) to select it.

RFOPS screen showing order line with seven unscanned cases
4 Press F3 (RL).

RFOPS screen showing label remove prompt
5 Key in Y for Yes and press Enter.

RFOPS screen showing prompt to scan in the label to be removed
6 Enter or scan in the label to be removed.
7 When the “Barcode Removed” message appears, press Enter to confirm it.
8 Continue to process the next label on the order line in the normal manner.

### REMOVING CASES EITHER SCANNED OR UNSCANNED <a id="removing-cases-either-scanned-or-unscanned"></a>

You can remove cases either scanned or unscanned in RFOPS by means of the RC (Reduce) command. 
When you use the Reduce command, the number of cases removed is subtracted from the order line’s to ship quantity in ENOR as well as the remaining number of cases and weight in RFOPS.
1 Enter RFOPS.
2 Enter or scan in your order number and/or UI number.
3 Use your arrow keys to position your cursor over the order line that you wish to process and press F3 (SL) to select it.
4 Press F2 (RC).

RFOPS screen showing prompt to remove cases
5 When prompted to remove the case and reduce the line quantity, key in Y for Yes and press Enter.

RFOPS screen showing seven potential cases to be removed
6 Do one of the following:
To remove a scanned case: To remove an unscanned case:
a) Enter or scan in the case that you wish to remove.
a) Press Enter to position your cursor in the REDUCE QTY field.
b) Key in the quantity to remove and press Enter.

RFOPS screen showing “Unscanned quantity reduced” message
7 When the “Unit removed” or “Unscanned quantity reduced” message appears, press Enter to confirm it.

RFOPS screen showing “Scan bar code message”
8 Continue to scan in or remove cases in the normal manner or press F4 (EX) to exit.

### REMOVING CASES FROM A FULLY SCANNED ORDER <a id="removing-cases-from-a-fully-scanned-order"></a>

You can remove cases from a fully scanned order by selecting the Yes option when the “Scan Complete 
Remove Case <Y/N> to Continue” message appears.
This message will appear in RFOPS whenever you retrieve a fully scanned order that has not yet been confirmed. It is designed to deal with situations in which it is necessary to remove cases from a pallet during the loading stage because of space limitations on the truck.
Each case that you scan in RFOPS removes one case from the to ship quantity in ENOR. If you have duplicate label ID’s attached to the same UI value, AccellosOne 3PL will remove the case or cases from the lowest process line number.
1 Enter RFOPS.
2 Key in your order number and press Enter.
3 Enter or scan in your OPID value.

RFOPS screen showing prompt to remove case and reduce line quantity
4 Key in Y for Yes and press Enter.

RFOPS screen showing pick list of order lines
5 Use your arrow keys to position the cursor over the order line containing the case(s) that you wish to remove and press F3 (SL) to select it.

RFOPS screen showing prompt to scan in bar code to be removed
6 Enter or scan in the case that you wish to remove.

RFOPS screen showing “Unit removed” message
7 When the “Unit removed” message appears, press Enter to confirm it.
8 Do one of the following:
9 When you finish scanning the cases to be removed, press F4 (RT) and F4 (EX) to exit.

### PERFORMING AN INCOMPLETE SCAN <a id="performing-an-incomplete-scan"></a>

If you are unable to scan in all cases on the pallet for any reason, AccellosOne 3PL will present you with the following options:
If you wish to exit RFOPS:
If you wish to remove additional cases from the same OPID:
If you wish to remove cases from a different OPID:
a) Proceed to next step. a) Enter or scan in your label number.
a) Press F4 (Ex) to position your cursor in the Ord. field and press Enter.
b) Enter or scan in your new 
OPID value.
c) Enter or scan in your label number.
1 (Continue) Continue to scan the remaining cases on the pallet.
2 (Start Over) Rescan all cases starting from the beginning.
3 (Exit, Short) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned and remove unscanned quantities from the to ship quantity. 
You cannot process the order line again in RFPIC.
4 (Exit, New Line) Only available when locate weight in bar code logic is deactivated
Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned, remove the unscanned quantities from the to ship quantity and will create a new line for the balance.
5 (Exit, Cancel Picking) Only available in RFPIC.

1 Scan all cases that you are shipping for the pallet. The system will prompt you when you are complete.
2 If you are unable to scan all cases for any reason, press F4 after scanning the last scannable case.

RFOPS screen showing “Scan incomplete” message
3 Do one of the following:
4 Continue to enter your process values normally in RFOPS.

### TRANSFERRING INBOUND PROCESS VALUES TO OUTBOUND ORDERS <a id="transferring-inbound-process-values-to-outbound-orders"></a>

If the automatic transfer of inbound process values to outbound orders is activated on your system, the process values attached to the product will be automatically transferred to the order when you enter or scan in your order number in RFOPS.
The following restrictions apply to the transfer of process values:
6 (Replace DAMG) Only available in RFPIC.
7 (Exit Scan, Save) Cease scanning and exit. AccellosOne 3PL will save the process values of any cases already scanned.
If you wish to continue from where you left off:
Key in 1 and press Enter.
If you wish to rescan all cases: Key in 2 and press Enter.
If you wish to exit and short the to ship quantity:
Key in 3 and press Enter.
When prompted to short the order line, key in Y for Yes and press Enter.
If you wish to exit, short the to ship quantity and create a new line for the balance:
Key in 4 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.
If you wish to exit without saving the scanned process values:
Key in 7 and press Enter.
Press Enter to acknowledge the “Process Complete” 
message.

▪ You cannot transfer process values if one or more values is missing. For example, if you have five cases on one full pallet and one of the cases is missing a process value, you cannot transfer the process values in RFOPS. You must enter the missing catch weight(s) in ENOR and then return to RFOPS to perform the transfer.
▪ You cannot transfer process values if you have two or more inventory entities that are identical. For example, you have two pallets with the same level 1/2/3 values and you wish to ship out a single pallet.
▪ Unless you are clearing out all inventory, the quantity being shipped must always equal one full pallet (or one drum if drum is assigned to the highest SKU class). For example, if you ship in cases, the number of cases that you ship must equal one full pallet.
Refer to the section “Item Process Values” in the Operations 2 Guide for further information about setting up this feature.
1 Enter RFOPS.
2 Retrieve the order whose process values you wish to transfer.
The “Barcode values for this order have transferred” message will appear.

RFOPS screen showing “Barcode values for this order have transferred” message
3 Press Enter to acknowledge the message.
4 Press F4 to exit. Your process values are transferred.

### SETTING UP CATCH WEIGHT TOLERANCES <a id="setting-up-catch-weight-tolerances"></a>

You can define catch weight tolerances for each item in ITEM. If a catch weight for that item exceeds the allowed tolerance, the weight will be rejected and the receipt or order cannot be confirmed until a catch weight within the permissible range is entered. For example, if the net weight of a pallet is defined as 100 lbs. 
for a given item in ITEM and the weight tolerance percentage is 5% for that item, you cannot enter a catch weight of greater than 105 lbs. or less than 95 lbs. in any RF program.

RFIPS screen showing “Wgt tolerance failed” message
Catch weight tolerances apply to RFOPS (Outbound Process Scan) and RFIPS (Inbound Process Scan).
In addition to the normal setups for catch weights in IPRO and IPRP, you must enter a value in the Weight 
Tolerance Percent field in Quantity Breakdown Block of ITEM for the appropriate SKU.
ITEM screen showing a weight tolerance of 5% on a net weight of 50 lbs.

### Picking Waves in RFPK <a id="picking-waves-in-rfpk"></a>

You pick your waves in RFPK (RF Wave Pick). Depending on your pick method, you may or may not be prompted to for a carton size when you close your pallet and prepare to print your labels. You can look up your carton information in LOCN (Look Up Carton).
1 Enter RFPK.
RFPK screen
2 Key in your wave number and press Enter.
REQUIREMENTS
FLOWS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
CASE PICKING See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
PROCESS VALUES See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
SUSP HOLDS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information.
MRFP The Outbound Pallet ID Entry at Beginning field in MRFP (RFPIC 2 tab) must be set to Yes.
WAVE MANAGER You need to run a wave in the Wave Manager.
LABELS You need a wave label set up in DOCU and this label must be attached to the appropriate customers and consignees in CCDU (Customer / Consignee Document Setup).
OTHER See the Wave Manager documentation.

RFPK screen
3 Key in your equipment code and press Enter.
RFPK screen showing prompt for pick method
4 Key in the number corresponding to your pick method and press Enter.
RFPK screen showing prompt for outbound pallet ID
5 Enter or scan in your outbound pallet ID.

RFPK screen showing prompt for outbound pallet ID
6 Use your up and down arrow keys to scroll through the list of order lines assigned to your outbound pallet 
ID. When you find the order line that you wish to pick, press F3 (SL) to select it.
RFPK screen showing prompt for from location
7 Enter or scan in your from location.
8 Enter or scan in your UI.
9 Key in your pick quantity and press Enter.
10 Do one of the following:
11 Press F1 (Print Label).
If your order consists of a single order line:
If your order has multiple order lines and you wish to pick another line:
If your order has multiple order lines and you wish to close the pallet and print the pallet ID label:
a) Proceed to next step. AccellosOne 3PL will display the list of unpicked order lines.
a) Select the line that you wish to pick and repeat steps 6 to 12 for that line.
AccellosOne 3PL will display the list of unpicked order lines.
a) Press F4 to exit the list.
b) Proceed to next step.

RFPK screen showing prompt for printer
12 Do one of the following:
13 Enter or scan in your staging location.
14 Process another order or press F4 to exit.

### Relocating Product in RFST <a id="relocating-product-in-rfst"></a>

In this program, you can relocate product on an outbound order. The product must be picked and assigned an outbound pallet ID in an RF picking program before it can be moved.
If your labels are generated in 
AccellosOne 3PL:
If you use your own labels that are not generated in 
AccellosOne 3PL: If Label field is populated:
a) Press Enter to generate your pallet ID.
b) if required, key in your printer code and press Enter.
c) If prompted to validate your pallet ID, enter or scan it in. 
a) Enter or scan in your pallet ID.
b) If required, key in your printer code and press Enter.
a) If the PRT (Printer) field is not populated, key in your printer code and press Enter.
REQUIREMENTS
FLOWS See [Picking Orders in RFPIC](expedicao-rf.html#picking-orders-in-rfpic) for further information for your outbound flows and other RFPIC requirements.
The order line must be picked in an RF picking program using CASE pick mode before it can be relocated in RFST.

1 Enter RFST.
RFST screen
2 Enter or scan in your order number. Then enter or scan in your OPID number. If your OPID numbers are unique, you can bypass the order number and enter only the OPID number.
RFST screen showing prompt for quantity
3 If prompted to enter the quantity, key in the total quantity on the pallet and press Enter.
4 If prompted to enter the from location, enter or scan in the from location.
OTHER There are five possible configuration parameters for RFST that you set up in 
MRFP (Miscellaneous tab).
▪ in the Validate Quantity in Order Move field, you specify whether or not the operator must enter the quantity being moved
▪ in the Validate From Location in Order Move field, you specify whether or not the operator must enter the from location of the product being moved
▪ in the Location Type of To Location in Order Move field, you specify whether the to location must be a staging location, a pick location or any location
▪ in the Allow Multiple Pallet Moves in RFST field, you specify whether or not the operator can relocate multiple pallets in a single step 
▪ in the Suggested Location Rules in RFST field, you define the suggested or default to location 
REQUIREMENTS

RFST screen showing prompt for to location
5 Enter or scan in your to location.
RFST screen showing confirmation message
6 Key in Y for Yes and press Enter to move the pallet.
7 Press F4 (EX) to exit.

### Merging OPID’s in RFMG <a id="merging-opid-s-in-rfmg"></a>

You can merge two or more outbound pallets into a single pallet in RFMG. For example, suppose you pick 10 cases from a location and build an outbound pallet. Later, you pick 25 cases from the same location and build a second outbound pallet. You now have two partial pallets and wish to merge the two into a single pallet to save space.
If your order line does NOT have process values such as serial number or weight, you can merge the entire quantity of a pallet or a partial quantity. However, if your order line has process values such as serial number or weight, you cannot merge partial quantities. If you do so, all process values attached to the order line will be deleted.
The following conditions must be met before you can do a pallet merge:
▪ The product must be picked from the same location.
▪ If you attach orders to loads in SELO and warehouse attribute 333 is set to 1, the product being merged must be on the same load and assigned to the same stop and group.
▪ Hazardous products cannot be merged with non-hazardous products.
▪ The same item must be kept together whenever possible if the item quantities are partials. For example, suppose you have three OPID’s on the same order and each OPID represents a partial pallet. If OPID’s 
1 and 2 are the same item and OPID 3 is a different item, OPID’s 1 and 2 can be merged, but 1 and 3 (or 
2 and 3) cannot be merged because that would put two different items on the same pallet.

There are two merge options that are configurable in MRFP:

### MERGING TWO EXISTING OPID’S <a id="merging-two-existing-opid-s"></a>

1 Enter RFMG.

RF Merge OPID screen
2 Enter or scan in your from OPID.
FIELD DESCRIPTIONS (MISCELLANEOUS 2/5 TAB)
Allow Merging Orders/
Items to One OPID Within 
Load (RFMG)
Yes
No
If you select Yes, the RF operator can assign different orders/items to the same OPID within a given load in RFMG. If you select No, the RF operator cannot assign different orders/items to the same OPID within a given load in 
RFMG.
Retain OPID To in RFMG Yes
No
If you select Yes, the OPID to value remains displayed on the screen after the merge so that the RF operator can continue to merge into the same OPID.

RFMG screen showing from OPID
3 If there are multiple order lines attached to the same OPID, you can press F1 (LN) to position your cursor in the from OPID block. Then use your arrow keys to scroll through the orders lines of your from OPID. 
When you finish scrolling, press F4 (RT) to return to the to OPID field.
4 Press Enter to accept the full OPID quantity or key in a partial quantity and press Enter.
5 Enter or scan in your to OPID.

RFMG screen showing to OPID and prompt to update
6 Press F3 (UP) to perform the merge.
7 Press F4 (EX) to exit.

### CREATING A NEW OPID <a id="creating-a-new-opid"></a>

You can move the full quantity or a partial quantity of an existing OPID to a new OPID that you create in 
RFMG. AccellosOne 3PL will create a new order line for the new OPID.
1 Enter RFMG.

RF Merge OPID screen
2 Enter or scan in your from OPID.

RFMG screen showing from OPID
3 If there are multiple order lines attached to the same OPID, you can press F1 (LN) to position your cursor in the from OPID block. Then use your arrow keys to scroll through the orders lines of your from OPID. 
When you finish scrolling, press F4 (RT) to return to the to OPID field.
4 Press Enter to accept the full OPID quantity or key in a partial quantity and press Enter.
5 Enter or scan in your new OPID.

RFMG screen showing new OPID and prompt to update
6 Press F3 (UP) to perform the merge.
7 Press F4 (EX) to exit.

### Performing Outbound Audits in RFOA <a id="performing-outbound-audits-in-rfoa"></a>

This program allows you to perform an audit of staged product before it is loaded onto the truck. You define your inventory level for RFOA audits in MRFP. For example, if you select Level 1 in the RFOA Audit Level field, the RF operator will perform a count for each item on the order. If, on the other hand, you select Level 2, the RF operator will perform a count for each lot on the order.
If the count matches the order line quantity, the order line will be advanced to the next flow and a time-stamp will be created indicating that the audit was successful. If the count does not match the order line quantity, an error message will be displayed and the order line will not be advanced to the next flow.
1 Enter RFOA.
REQUIREMENTS
FLOWS ENOR (Enter Order)
SUAL (Supervisor Allocated) — optional
STPI (Start Picking)
FIPI (Finish Picking)
special flow for RFOA audit
STLO (Start Loading) — optional
COOR (Confirm Order)
INVENTORY LEVELSYou can process up to four inventory levels in RFOA.
OTHER You must define your inventory level for RFOA audits in the RFOA Audit Level field in MRFP. For example, if you select Level 1 in the RFOA Audit Level field, the RF operator will perform a count for each item on the order. If, on the other hand, you select Level 2, the RF operator will perform a count for each lot on the order.
If you select “Suspend Advancing Flow in Outbound Audit” in MRFP, the order will 
NOT be advanced to the next flow even if the operator count matches the order line quantity.

RFOA screen
2 Enter or scan in your staging location.
3 If there are multiple orders at your staging location, press F3 (SL) to select the order that you wish to audit.
RFOA screen showing prompt for OPID
4 Enter or scan in your OPID.
5 Enter or scan in the required number of inventory levels.

RFOA screen showing prompt for quantity
6 Key in your quantity and press Enter.
7 Do one of the following:
RFOA screen showing message for completed audit
8 Repeat the above steps for any additional order lines that you wish to audit or press F4 the required number of times to exit RFOA.
If your audit quantity is correct:
If your audit quantity is NOT correct:
a) Press Enter to acknowledge the message.
a) Press Enter to acknowledge the error message.
b) Re-enter your quantity. If your quantity is rejected again, press 
F4 (RT) to exit.
c) Press Enter to acknowledge the “Order Incomplete” message.

### Adjusting Cubic Dimensions in RFCC <a id="adjusting-cubic-dimensions-in-rfcc"></a>

You can adjust the cubic dimensions and gross weight of an OPID in RFCC (RF Carton Cube). If you do not adjust cubic dimensions of an OPID in this program, the dimensions will be automatically calculated based on the item setup and the product assigned to the OPID.
1 Enter RFCC.
RFCC screen
2 Enter or scan in your OPID.
RFCC screen showing linear measurement code set to M for Meters
3 Key in your length and press Enter.
4 Key in your width and press Enter.
5 Key in your height and press Enter.
6 Key in your gross weight and press Enter.

7 Press F4 to exit.
8 If you re-enter your OPID in RFCC, you can look up the cubic dimensions that you previously scanned.
RFCC screen showing cubic dimensions for OPID 000046

### Assigning Orders to Loads in SELO <a id="assigning-orders-to-loads-in-selo"></a>

Refer to the Operations 2 Guide for instructions on using SELO and OLOP.

### Replacing Damaged Product in RFRD <a id="replacing-damaged-product-in-rfrd"></a>

This program allows you to take picked product off an order, put it on SUSP hold and allocate replacement product. It is only available for product that has been picked and staged. Depending on the option that you choose in the Allow Suspended Holds field in MRFP, a supervisor login may be required. 
If there are process values attached to the picked and staged product, you will be prompted to scan those values.
1 Enter RFRD.

RFRD screen
2 Enter or scan in your UI value.
3 If there are multiple order lines with the same UI, use F3 (SL) to select the line that you wish to work on.
RFRD screen showing prompt for damaged quantity
4 Key in your damaged quantity and press Enter.
5 Press F3 to process.
RFRD screen showing prompt to proceed
6 Key in Y for Yes and press Enter.

RFRD screen showing confirmation message
7 Press Enter to continue.
8 Press F4 to exit.

### Working With Pallet Build Assignments in PABU <a id="working-with-pallet-build-assignments-in-pabu"></a>

This program allows you to look up and modify your pallet build assignments before they are released to RF or voice for picking. PABU supports the following functions:
▪ you can look up the Task Profile parameters used to generate assignments
▪ you can update your Task Profile parameters and re-process the pallet build
▪ you can update existing assignments by adding or removing order lines
▪ you can create new assignments
▪ you can run the Pallet Build Summary/Detail Reports
▪ you can assign a staging location to order lines
NOTE Pallet build assignments are only available in PABU for pre-built pallets. Pallets built dynamically by the Task Engine cannot be viewed or edited in PABU.

### SETTING UP YOUR PALLET BUILD PARAMETERS IN COMP <a id="setting-up-your-pallet-build-parameters-in-comp"></a>

The automatic suspension of picking tasks can be activated in COMP. If you do not wish to automatically suspend your picking tasks, you can manually suspend them in RFOT.
You release your pallet build assignment tasks to RF or voice.
REGI/
PABU
AccellosOne 3PL generates your pallet build assignments based on your setup in REGI and 
CCCC.
You review your pallet build assignments and make any necessary adjustments.
Allocation
PABU
You allocate your orders in Wave Manager. 1
RFPIC/
Voice
5 RF operator performs the picking tasks. 

### PERFORMING QUERIES <a id="performing-queries"></a>

You can query by suspended tasks, released tasks or all tasks.
At the load level, PABU shows the total number of pallets, the total number of pallet build assignments, the total quantity, the number of picked pallets, the number of pick assignments, the number of picked picks, the picked quantity, the gross weight, the net weight and the cube for each load.
At the order level, PABU shows the stop number, the wave number, the customer, the total number of pallets, the total number of pallet build assignments, the total quantity, the number of picked pallets, the number of pick assignments, the number of picked picks, the picked quantity, the gross weight, the net weight and the cube for each order.
At the assignment level, PABU shows the assignment number, quantity, total number of picks, net weight, height and cube or each pallet build assignment.
1 Enter PABU.
FIELD DESCRIPTIONS
Suspend Picking Tasks 
Upon Wave Execution
Yes
No
If you set this flag to Yes, picking tasks will be automatically suspended when you generate a wave in Wave Manager. This will allow you to manually adjust your pallet build assignments in PABU (Pallet Build) before they are released to RF or voice for picking.
If you set this flag to No, picking tasks will be automatically released to RF or voice for picking once the wave is generated.
This flag overrides the Suspend Task flag in Wave Manager, which allows you to suspend tasks for a specific Wave Manager template.
Use Assignment Parameter Tables for Pallet BuildYes
No
If you set this flag to Yes, you can rebuild pallets any number of times using the same REGI/CCCC configuration that was in effect when you first built the pallet for a given order line. If set this flag to No and you rebuild a pallet, 
AccellosOne 3PL will use your default pallet build settings in REGI and CCCC.

PABU screen showing query fields
2 Enter your wave, load, order and customer order parameters.
3 In the Task Options dropdown list, select Suspended, Released or All.
4 Click on Execute Query.
PABU screen showing query results for All option
5 In the Load Summary Block, select the load whose orders you wish to look up.
6 Click on Order / Assignment.
7 In the Order Details Block, select the order whose pallet build assignments you wish to look up.
8 If the order has header or line remarks, you can click on Order Header/Line Remarks to view them.

PABU screen showing order header and order line remarks
When you finish looking up your order remarks, click on Exit to return to the Order Details screen.
9 Click on Order / Assignment to see your pallet build assignments.
PABU screen showing pallet build assignments
If the Assignment column is blank, that means that the order line was not included in any pallet build assignment.
10 Click on Lines to see the order lines for those assignments.

PABU screen showing order lines
11 When you finish looking up your pallet build assignments, click on Exit the required number of times to exit. 

### RELEASING AND STAGING A SUSPENDED LOAD <a id="releasing-and-staging-a-suspended-load"></a>

Staging a suspended order or load in PABU will override the existing staging location if one has already been assigned.
1 Select the suspended order or load that you wish to release.
2 Click on Release Order Tasks.
PABU screen showing prompt for staging location
3 Select your staging location and warehouse from the pick list and press Enter twice to accept them.

### MERGING ASSIGNMENTS <a id="merging-assignments"></a>

1 Go the Assignments tab.

PABU screen showing assignments
2 Select the first of the two assignments to be merged.
3 Click on Assignment Merge dropdown list.
PABU screen showing Assignment Merge dropdown list
4 Select the second of the two assignments to be merged and click on Merge Assignment.
5 When prompted to confirm the merge, click on Yes. The screen will be refreshed and only one pallet assignment will be displayed.

### DELETING ASSIGNMENTS <a id="deleting-assignments"></a>

When you delete a pallet build assignment, the order line remains but the assignment number is deleted. The 
Task Engine will create a new pallet build assignment dynamically.
1 Go the Assignments tab.

PABU screen showing assignments
2 Select the line or lines that you wish to delete and click on Delete Assignment Lines.
3 When prompted to confirm the deletion, click on Yes.
PABU screen showing deleted assignment

### ADDING ASSIGNMENTS <a id="adding-assignments"></a>

If a pallet build assignment has been deleted, the line cannot be picked until you create a new assignment for the line.
1 Go to the Assignments tab.
PABU screen showing pick without assignment

2 Click on Add Assignment.
PABU screen showing Add Assignment
3 Select the line or lines that you wish to add and click on Add Assignment.
PABU screen showing new assignment

### DELETING LINES FROM AN ASSIGNMENT <a id="deleting-lines-from-an-assignment"></a>

If an assignment contains two or more lines, you can delete individual lines from the assignment.
1 Go to the Assignments tab.
PABU screen showing assignments
2 Click on Lines.

PABU screen showing order lines
3 Select the line that you wish to delete and click on Delete Assignment Lines.
4 When prompted to confirm the deletion, click on Yes.

### OVERRIDING ASSIGNMENTS <a id="overriding-assignments"></a>

You can move a line from one assignment to another by means of the Override command.
1 Go to the Assignments tab.
PABU screen showing assignments
2 Click on Lines.
PABU screen showing lines

3 Select the line that you wish to move and click on the Assignment Override dropdown list to select the to assignment. Then click on Assignment Override.
4 When prompted to confirm the assignment override, click on Yes.

### CHANGING YOUR ORDER PARAMETERS <a id="changing-your-order-parameters"></a>

If you change your order parameters, you can rebuild your pallet assignments using the new parameter(s).
1 Select the order that you wish to reprocess.
2 Click on Order Parameters.
Order Parameters screen
3 Proceed to make any necessary changes to your order parameters. Only fields and flags in boldface type can be modified.
4 Click on Save to save your changes and rebuild your pallet assignments.
5 When prompted to save your changes, click on Yes.

### RESTORING YOUR ORIGINAL ORDER PARAMETERS <a id="restoring-your-original-order-parameters"></a>

If you changed your order parameters and are not satisfied with the results, you can restore your order parameters to the original settings. You define what is meant by “original” settings in the Use Assignment 
Parameter Tables for Pallet Build field in COMP.
1 Select the order whose original parameters you wish to restore.

2 Click on Order Parameters.
3 Click on Copy Originals.
4 When prompted to confirm the restoration of your original parameters, click on Yes.

### PRINTING THE PALLET BUILD SUMMARY REPORT <a id="printing-the-pallet-build-summary-report"></a>

This report shows the assignment number, stop number, quantity, number of picks, number of items, height, cube, gross weight and net weight for each assignment reported on.
1 Select the load or order that you wish to report on.
2 Click on Run APBR Summary Report.
APBR report
3 Select your printer and click OK.
APBR Summary report
ABC FOODS

### PRINTING THE PALLET BUILD DETAIL REPORT <a id="printing-the-pallet-build-detail-report"></a>

This report shows the sequence number, order line number, item code, pick location, isolator code (ISOL), quantity, cube and net weight for each pick in a pallet build assignment.
1 Select the load or order that you wish to report on.
2 Click on Run APBR Detail Report.
3 Select your printer and click OK.
APBR Detail report

### SUSPENDING A TASK IN RFOT <a id="suspending-a-task-in-rfot"></a>

If automatic task suspension is deactivated in COMP, you can manually suspend a pallet build assignment task until you are ready to pick it.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
ABC Foods

RFOT screen showing unsuspended tasks
4 Click in the Suspend Tasks column of each task that you wish to suspend.
5 Click on Save to suspend the tasks.

### RELEASING A SUSPENDED TASK IN RFOT <a id="releasing-a-suspended-task-in-rfot"></a>

When you are ready to pick the task, you must release the suspension.
1 Enter RFOT.
2 Perform your query to retrieve the orders that you wish to work with.
3 Click on the Tasks tab.
RFOT screen showing suspended tasks
4 Click in the Suspend Tasks column of each task that you wish to release to deselect the checkbox.
5 Click on Save to release the task.

## Outbound Tasking <a id="outbound-tasking"></a>

*Manual H — RF Guide*

### Overview <a id="overview"></a>

Outbound tasking allows you to optimize the distribution of work in your warehouse such that urgent work is performed first, congestion in warehouse aisles and zones is avoided whenever possible and the discretion of individual RF operators to pick and choose their own work is reduced to a minimum.
Instead of RF operators entering individual RF programs such as RFPIC or RFRP to pick entire order lines and perform replenishments at their own pace and in a sequence that does not take into account the work of other RF operators, they enter a single program, RFITLV, to work on their first assigned task. The first assigned task and all subsequent tasks for an operator are based on the following factors:
▪ the RF operator’s equipment
▪ the RF operator’s “proximity” to the task’s location (that is, is the operator in the same location, aisle or zone)
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
If an RF operator chooses to skip a task, AccellosOne 3PL will record the skipped task as well as the operator who skipped it. The operator will not see the task again in his or her current RF session.
The RF operator performs outbound tasking in RFITLV (RF Interleaving). RFITLV supports all the standard functions performed in RFPIC (case pick mode), REPI, RFRP and RFCE.

### UNDERSTANDING ORDER LINES, PICK ASSIGNMENTS AND OUTBOUND TASKS <a id="understanding-order-lines-pick-assignments-and-outbound-tasks"></a>

An order line is a line entered in ENOR representing one item. 
A pick assignment is a single outbound pallet consisting of one or more order lines based on the weight and cube limits for a single pallet, whether or not item mixing is allowed on the same pallet and whether or not the product is stackable. 
Order line
Pick assignment
Pick assignment
Pick assignment
Task 1 Task 2 Task 3 Task 4 Task 5 full pallet picks case picks

A task is a pick assignment broken down by location, RF operator and pick method. In other words, the smallest possible unit of work in a warehouse. For example, if a pick assignment or outbound pallet of 20 cases consists of three picks from three different locations, each pick location/RF operator/pick method is considered a separate task.
1 — ORDER ENTRY You enter an order line of 80 cases (1 pallet, 20 cases)
2 — WAVE MANAGER Wave Manager creates two pick assignments for the order line. A full pallet pick for an RF operator working with a fork lift and a case pick for an RF operator working with a pallet jack.
Task engine assigns tasks to operators based on RFOP, MHEC, 
REGI and warehouse activity type exclusion settings. Tasks are sequenced by ship to date/time, order priority number and order create date/time.
If replenishments are required for a pick line location, the replenishment must be performed before the pick.
Task engine creates five pick tasks:
task 1 = full pallet pick by RF operator 1 task 2 = pick of 10 cases from location A by RF operator 2 task 3 = pick of 5 cases from location B by RF operator 2 task 4 = pick of 5 cases from location C by RF operator 2 task 5 = replenishment of location C by operator 3
4 — TASK ENGINE
Operator 1
Attached to forklift, can only perform picks
Operator 2
Attached to pallet jack, can only perform picks
Operator 3
Attached to forklift, can only perform replenishments
5 — RF PICKING/
 REPLENISHMENT
RF operators perform their assigned picks and replenishments. Case picking, which is slower, may be scheduled before full pallet picks.
Operator 3 replenishes location C using a forklift
Operator 2 picks 10 cases from location A, 5 cases from location B and 5 cases from location C using a pallet jack
Operator 1 picks a full pallet using a forklift
RFITLV
ENOR
3 — REVIEW PALLET BUILD
 ASSIGNMENTS (OPTIONAL)
If pre-built pallet building is activated in CCCC (that is, pallets are built during waving), supervisor can review and edit pallet build assignments.
PABU

### Company Parameters (COMP) <a id="company-parameters-comp"></a>

In this program, you activate tasking by setting the Enable Task Interleaving flag to the appropriate value: 
▪ Create All Tasks
▪ Create Tasks According to Zone Setting
▪ Create All Tasks, Exclude Orders not in Wave
▪ Create Tasks According to Zone Setting, Exclude Orders not in Wave
If you select “Create All Tasks”, tasking will be activated for all warehouse zones whose zone type is set to I for Interleaving in WHZO. If you select “Create Tasks According to Zone Setting”, tasking will be activated only for warehouse zones whose zone type has been set to I for Interleaving and whose Task Required flag has been set to Yes.
COMP screen showing Enable Task Interleaving set to Create All Tasks
The following options also require setup in COMP.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)
RFITLV First Check 
Same Location for Task
Yes
No (default)
If you set this flag to Yes, the task engine will not limit itself to available tasks at the current location. If you set this flag to No, the task engine will consider order and load priority before checking the same location for a task.

COMP screen showing Same Location/Aisle/Zone fields
RFITLV Second Check 
Same Aisle for Task
Yes
No
If you set this flag to Yes, the task engine will not limit itself to available tasks in the same aisle. If you set this flag to No, the task engine will consider order and load priority before checking the current aisle for a task.
RFITLV Third Check 
Same Zone for Task
Yes
No
If you set this flag to Yes, the task engine will not limit itself to available tasks in the same warehouse zone. If you set this flag to No, the task engine will consider order and load priority before checking the current warehouse zone for a task.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

### Wave Manager <a id="wave-manager"></a>

See the Wave Manager documentation for further information on the Suspend Task function. If you activate this function, tasks will be automatically suspended when you generate a wave in Wave Manager. This will allow you to manually adjust your pallet build assignments in PABU (Pallet Build) before they are released to 
RF or voice for picking.

### Material Handling Types (MHET) <a id="material-handling-types-mhet"></a>

See [Material Handling Types (MHET)](expedicao-rf.html#material-handling-types-mhet).

### Warehouse Zones (WHZO) <a id="warehouse-zones-whzo"></a>

Only locations attached to a warehouse zone whose zone type code has been set to I for Interleaving can be used for tasking. See [Warehouse Zones (WHZO)](expedicao-rf.html#warehouse-zones-whzo) for further information on WHZO.
If you selected the Create Tasks According to Zone Setting option in COMP, you must set the Task Required flag to Yes for each warehouse zone in WHZO that you wish to activate.
WHZO screen showing interleaving zone type code and Task Required flag

### Warehouse and Location Format (WARE) <a id="warehouse-and-location-format-ware"></a>

You must define your aisles in the Location Attributes Block of WARE. See the Setup Guide for further information on WARE.
WARE screen showing aisle defined as first character in location code

### Locations (LOCA) <a id="locations-loca"></a>

In this program, you define your location height restrictions for each location. Only equipment types whose vertical height factor code matches the location’s vertical height factor code can be assigned a task in this location.

LOCA screen showing location assigned a vertical height factor code of 3

### Task Profile (REGI) <a id="task-profile-regi"></a>

In this program, you define the following:
▪ the maximum number of RF operators allowed in a warehouse aisle at any one time
▪ the maximum number of RF operators allowed in a warehouse location at any one time
▪ the priority number for forced replenishments
▪ the pick method (full pallet pick or case pick)
▪ the warehouse activity type (picking or replenishment)
If picking and replenishment are performed by different teams in your warehouse, tasking requires two task profiles: one for the activity type of picking and one for the activity type of replenishment. If your pickers use different equipment based on the pick quantity, you will need a separate task profile for each equipment type. 

REGI screen showing five as the maximum number of operators per aisle when picking (activity type = 
26)
FIELD DESCRIPTIONS
Max. Number of OperatorsIn this field, you define “congestion” in a warehouse aisle; that is, if the number of operators in a task profile exceeds this number, the extra operators will not be assigned any tasks until one or more existing operators completes his or her task(s).
Max. Number of Operators per LocationIn this field, you define “congestion” in a warehouse location; that is, if the number of operators in a task profile exceeds this number, the extra operators will not be assigned any tasks until one or more existing operators completes his or her task(s).
Select Only Assignments 
With Both Pick Line/NonPick Line Locations
Reserved for future use.

### RF Outbound Tasking in RFITLV <a id="rf-outbound-tasking-in-rfitlv"></a>

You perform tasking in RFITLV (RF Interleaving). Depending on the next available task, RFITLV calls one of the following programs: RFPIC, RFRP and RFCE. Refer to the documentation on these programs for further information.
1 Enter RFITLV.
Force Replenishment PriorityAll replenishment tasks are assigned a default priority number of 100. This priority number is reduced by 1 each time that an order line cannot be picked because the pick location has not been replenished. The process continues until the location is replenished and the order line is picked. 
If a replenishment task is found with a priority number less than or equal to the number that you enter on this field, it will be released to the operator even if it may have other issues such as the quantity in the pick line location is still above the minimum quantity or the location is full.
If you leave this field blank, regardless of the task priority number the replenishment task will not be released to the operator when the quantity in the pick line location is still above the minimum quantity or the location is full.
REQUIREMENTS
COMP Task interleaving must be activated.
COMP The following fields must be configured: RFITLV First Check Same Location for Task, RFITLV Second Check Same Aisle for Task and RFITLV Third Check 
Same Zone for Task.
PALLET BUILDING If you wish to take advantage of the Pallet Build engine, setup is required in 
IPBR, ITEM, REGI and CONS.
OPERATOR RESTRICTIONSYou can deactivate tasking for some or all RF operators by setting up activity type exclusions in RFOP. For example, RF operator 1 can only pick, RF operator 2 can only put-away and RF operator 3 can only relocate.
FIELD DESCRIPTIONS

RFITLV screen showing prompt for MHE code
2 Key in your MHE code and press Enter.
RFITLV screen showing pick list for task profiles
3 If prompted to do so, select the appropriate task profile from the pick list. If you are restricted to a single task profile code, press Enter to acknowledge it.
RFITLV screen showing picking task

4 Do one of the following:
5 Repeat the above steps for each additional task assigned to your task profile.
6 When you finish performing all your tasks, press F4 (RT) to exit. Then key in N for Exit and press Enter.

### Looking Up Your Outbound Tasks in RFOT <a id="looking-up-your-outbound-tasks-in-rfot"></a>

You can look up your outbound tasks in RFOT and, if required, change their priority or suspend them.
1 Enter RFOT.
2 If required, click on the Pick/Interleave (2) tab.
To perform the task: To skip the task:
a) Press F3 (SL) to select the line that you wish to work on.
b) Proceed to perform the pick/ replenishment the task.
a) Press F4 (RT).
b) Key in Y for next task and press 
Enter or key in N for exit and press Enter.

RFOT screen showing Pick/Interleave (2) tab
3 Key in your filter criteria and click on Execute Query. AccellosOne 3PL will retrieve all order lines that meet your filter criteria.
4 Click on the Tasks tab. This tab shows the following information for each task:
▪ the order number
▪ the line number
▪ the order priority
▪ if the pallet is built from product in multiple locations, the sort sequence number for these locations
▪ if the pallet is built from product in multiple locations, the assignment number
▪ the release date (the release date is the order ship date on the order header)
▪ whether or not the task has been suspended
▪ the priority override value (if any)

RFOT screen showing Tasks tab (if Sort Sequence and Assignment Number fields are blank, the assignment is a full pallet pick)
5 If required, you can change the priority of an outbound task. The default value is 100. If you enter a lower value (say, 50), the outbound task will have a lower priority.
6 If required, you can suspend a task by selecting the Suspend Task checkbox.
7 If you made any changes in the previous two steps, click on Save to save your changes.
8 If you wish to look up your pick assignments in assignment sequence, click on Order Assignments.
RFOT screen showing Order Assignments tab

9 When you finish looking up your order line tasks, click on Exit the required number of times to exit.

A accessing RF 132 adjusting non-serial number inventory 346 adjusting serial number inventory 355 alternate item codes in RFCH 184 alternate item codes in RFPU 201 assignments, pick method 217 auto-confirming receipts in RFCH 157 auto-confirming receipts in RFPU 157, 193
B
BAPR (Bar Code Profile Code) 12 blind receiving in RFCH 154 cartonization 418
Cartonization tab (MRFP) 418 cartons, deleting in DCAR 451 cartons, looking up in LOCN 449
CASE (Case Picking) 267 case picking 227 catch weight tolerances 302
CCCC (Outbound Process Configuration) 120, 422
CCDU (Customer / Consignee Document Setup) 109
CCOR (Customer Consignee Outbound Rules) 124 changing your company 132
CONS (Consignees) 429
Consolidation Method for Allocated Lines field (CUST) 107 count backs, performing in RFPIC 246
CRM tasks, performing in RF 379
CTPA (Clear Terminal Pick Assignments) 415
CTSZ (Carton Size Setup) 420
CUST (Customer Codes) 107
Customer/Consignee Outbound Rules (CCOR) 124
D damaged product, replacing in RFRD 317
DCAR (Delete Carton) 451
E entry of expiry dates in RFCH 164
EOSU (Exclude Orders from RF Substitution) 280
EPSD (Enter Packing Details) 442 equipment tracking 454 excluding orders from overpicking in EOSU 241 extra charge setup 89 extra charges, adding to receipt/order in RFEC 370
F first level cartonization 418
H holds, placing product on in RFCH 186 holds, placing product on in RFPIC 236
ICIN (Inventory Count Investigation) 249
ICNP (Item Cartonization Profile Code) 427
ICOC (Item Consignee Configuration) 119
IHZV (Item Hazardous Material Violation) 110 inbound flows, understanding 153 inventory counting in RFPIC 246 inventory, merging 363
IPBR (Item Pallet Build Restrictions) 111
Item Consignee Configuration (ICOC) 119
Item Hazardous Material Violation (IHZV) 110
LOCN (Look Up Carton) 259, 449
LOENRF (RF Look Up Entity Information) 144
LOLORF (Look Up Location - RF) 142 looking up temperature and trailer information in LORE 189 look-up programs 131
LOORRF (Look Up Orders - RF) 147
LORERF (RF Look Up Receipts) 145

M
MCHK (RF Checklist) 455 merging inventory 363 merging OPID’s 309
MHEC (Material Handling Equipment Code) 401, 461
MHET (Material Handling Types) 458
MIRP (Item RF Profile) 84
Miscellaneous (2) tab (MRFP) 67
Miscellaneous (3) tab (MRFP) 71
Miscellaneous tab (MRFP) 64 mixed product, receiving in RFCH 187
MRFP (RF Profile Code) 16 multi-pallet moves 344
O one-step put-away 152
OPID’s, looking up in LOCN/LOOR 259
OPID’s, merging 309 outbound flows, understanding 217 outbound pallet building 111 overpicking, excluding orders from in EOSU 241 overriding the system-assigned location in RFCH 169 overriding the system-assigned location in RFPU 198
P
Pallet Build (PABU) 319
Pallet Build engine 111
Pick & Pack 418 pick and pack cartonization 434 pick methods 217 picking orders in RFPIC 220 picking pick line product from a non-pick line location in RFPIC 242 picking programs, overview of 219 picking substitution 275 process values entering in RFIPS 202 entering in RFOPS 284 entering in RFPIC 232
PSPR (RF Substitution Profile Code) 276 putting away to a pick line location in RFPU 202
Q queries, performing in RFCH 174
R
REAS (Reason Code) 400 receiving mixed product in RFCH 187
REGI (Task Profile) 113, 396 relocating inventory in RFRL 335 replenishments, performing in RFPIC 243 reserve logic orders, picking 235
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
adjusting in inventory 356 adjusting out cases 358 adjusting out full pallets 359 adjusting out using Remove command 360 overview 346 recovering from a lost connection 362
RFAJB (RF Adjustment)
overview 355
RFATT (RF Attributes) 387
RFBR (RF Bar Code Read) 381
RFCC (RF Carton Cube) 316
RFCD (RF Check Digit) 374
RFCE (RF CRM Entry) 379
RFCH (RF Check Unload)
creating a new line 183 entering expiry dates 164 entering partial U-type receipt lines in 175 entering process values 180 entering trailer and pallet information 170 looking up remarks in 190 overview 154 performing queries in 174 printing labels in 176 processing variances 177 receiving mixed product 187 receiving product on automatic hold 186 receiving product under an alternate item code 184 receiving product with a variable quantity breakdown validating process values in 182
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
capturing the weight dynamically from a bar code 204 overview 202 weight discovery 204
RFIT (RF Item Look-Up) 132
RFITLV (RF Interleaving) 476
RFLOIP (RF Look Up Item Process) 141
RFLR (RF Look Up Reserve Logic Customers) 148
