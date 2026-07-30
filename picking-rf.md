---
title: "Picking via RF e Cartonização"
description: "RFPIC em todas as variantes, wave pick, voice picking e montagem de caixas."
layout: default
---

# Picking via RF e Cartonização

RFPIC em todas as variantes, wave pick, voice picking e montagem de caixas.

**Fluxo principal:** `RFPIC (pick) / RFPK (wave pick) -> RFSC (sort carton) -> RFOPB (pallet build)`

> Fonte: manuais H do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## RFPIC <a id="rfpic"></a>

*Manual H — RF Guide*

This tab show various RFPIC/RFPK options.
Allow Receiving of Multiple Lines TogetherDisallow Receiving Multiple Lines Together
Allow Receiving of Multiple Lines Together
If you select “Allow Receiving of Multiple Lines Together”, the RF operator can put-away multiple receipt lines in a single step if the following conditions are met:
▪ all lines have the same UI
▪ all lines are in the same location with the same hold code (if any)
▪ all items have three or four inventory levels
▪ the quantity entered is the total quantity and it is entered in the lowest SKU
NOTE If you used Directed Move Inbound to assign locations and the pallet has mixed items, the ILOP profile from the item with the largest quantity in the pallet is used to produce a to location.
Change of Warehouse 
Rules
Confirmation Required
Allow Change of Warehouse Code, No Confirmation Required
Do Not Allow Change of Warehouse Code
If you select “Conformation Required”, the RF operator will be prompted to confirm the change in warehouse code. If you select “Allow Change of Warehouse Code, No Confirmation Required”, the RF operator will not be prompted to confirm the change in warehouse code. If you select “Do Not Allow Change of Warehouse Code”, the RF operator will not be able to change the warehouse code.
Confirm Receipt Line for 
Opportunistic Cross-Dock in RFPU
No
Yes*
If you select No, a receipt line put-away to a cross-dock location must be manually confirmed in CHRF. If you select Yes, a receipt line put-away to a crossdock location will be automatically confirmed when the RF operator completes the put-away in RFPU.
FIELD DESCRIPTIONS (RFPU)

RFPIC tab
.
FIELD DESCRIPTIONS (RFPIC)
Default Mode Only Case Picking
Only Pallet Picking
Case Picking
Pallet Picking
If you select “Only Case Picking”, the RF operator cannot select pallet or normal mode (NM) in RFPIC. If you select “Only Pallet Picking”, the RF operator cannot select case pick mode (CP) in RFPIC (unless he or she is picking from a pick line location). If you select “Pallet Picking”, the RF operator will be prompted to confirm pallet or normal mode (NM) as the default picking mode in RFPIC. If you select “Case Picking (CP)”, the RF operator will be prompted to confirm case pick mode as the default picking mode in RFPIC. 
Once the RF operator selects a mode in RFPIC, that mode remains in effect for all orders until the RF operator exits RFPIC or changes his or her mode by pressing F2.

If the RF operator is picking from a pick line location, the mode is automatically set to Case Picking regardless of the option that the RF operator selects in this field.
Allow Loading Before 
Completion of Picking 
Process
Yes
No
If you select Yes, the RF operator can start loading in OLOP before picking all product on the order in RFPI/RFPIC. If you select No, the RF operator must pick all product on the order in RFPI/RFPIC before loading in OLOP.
Duplicate Pallet Label 
Rules
Allow Duplicate Pallet ID’s (1)
Disallow Duplicate Pallet ID’s (2)
Operator Decision in all Orders (3)
Disallow Duplicate Pallet ID’s in Open Orders (4)
Operator Decision in Open Orders (5)
Allow Duplicate Pallet ID’s in Its Own Order Only (6)
If you select 1, duplicate pallet ID’s will be allowed without restriction. If you select 2, duplicate pallet ID’s will never be allowed. 
If you select 3, the RF operator will be prompted to accept or reject a duplicate pallet ID for all orders. If you select 4, duplicate pallet ID’s will not be allowed in open orders. If you select 5, RF operator will be prompted to accept or reject a duplicate pallet ID for open orders only. If you select 6, duplicate pallet 
ID’s will be allowed only within an individual order.
FIELD DESCRIPTIONS (RFPIC)

Allow Partial Picking in 
Normal Mode
Allow all, no restriction (1)
Allow last remaining partial inventory and full pallets (2)
Allow full pallets only (3)
Allow PALL pick method only (4)
This flag governs which order lines appear in the RFPIC pick list when working in normal mode.
If you select 1, all order lines regardless of pick quantity appear in the RFPIC pick list. If you select 2, only full pallet picks and partial quantities representing the last remaining inventory in a location appear in the RFPIC pick list.
If you select 3, only full pallet picks appear in the RFPIC pick list. The RF operator must switch to case pick mode to pick partial order lines.
A partial quantity is defined as 60% or more of the total quantity in the location. For example, if there are 50 cases in a location and you need to pick 30, you can scan in the 20 cases to be removed rather than the 30 cases to be picked. This option is designed to save time by reducing the number of cases scanned.
If you select 4, only full pallet picks generated by the Wave Manager appear in the RFPIC pick list.
Assign PID on Full Pallets or Last Inventory
In NM Mode (1)
No (2)
In CP Mode as the first pick (3)
RFPIC CP Mode Full Pallet (INVT QTY Break) or RFITLV PALL Pick 
Method (4)
If you select 1, the lowest level or pallet ID will be added to the Process Block of the order under the code CP for case pick when picking full pallets or picking the last entity in a location in normal mode.
If you select 2, the lowest level or pallet ID will NOT be added to the Process 
Block of the order under the code CP for case pick.
If you select 3, the lowest level or pallet ID will be added to the Process Block of the order under the code CP for case pick after the first pick in case pick mode.
If you select 4, the lowest level or pallet ID will be added to the Process Block of the order under the code CP for case pick when picking full pallets based on the item’s standard quantity breakdown while in case pick mode in RFPIC.
FIELD DESCRIPTIONS (RFPIC)

Number of Days for Label 
Validation
The “value greater than zero” option requires a custom label from HighJump.
If you enter a value greater than zero in this field, AccellosOne 3PL will validate a case’s date in RFPIC. Should the Number of Days for Label Validation value be less than the order to arrive date minus the date embedded in the case's bar code label, the message “Too old for order” will display and you will not be able to pick the case. 
If you enter zero or leave this field blank, the RF operator can scan in the cases to be removed from a full pallet rather than the cases to be picked when picking a partial quantity. 
Allow Suspended Holds Split Order Line, No Suspended Hold
If you select “Split Order Line, No Suspended Hold” and place product on hold in RFPIC, the order line will be split but no suspended hold will be placed on the product that is not picked and the new order line can be picked at any time. With this option, the F3 (HD) command in RFPIC is not available. 
Allow Suspended Holds
Only Allow if Supervisor Approved
If you select “Allow Suspended Holds”, non-supervisory operators can place product on suspended hold in RFPIC. If you select “Only allow if Supervisor approved”, the following rules will apply:
▪ non-supervisory operators can place product on suspended hold in RFPIC if approved by a supervisor (HD command)
▪ a partial pick will require the approval of a supervisor
With both these options, the order line will be split into two: line 1 will contain the pick quantity and line 2 will contain the remaining quantity that could not be picked. Line 2 will be placed on suspended hold and AccellosOne 3PL will attempt to reallocate the line 2 quantity.
Split Order Line, Allow Suspended Hold
Split Order Line, Supervisor Approved
If you select option “Split Order Line, Allow Suspended Hold”, non-supervisory operators can place product on suspended hold in RFPIC. If you select “Split 
Order Line, Supervisor approved”, the following rules will apply:
▪ non-supervisory operators can place product on suspended hold in RFPIC if approved by a supervisor (HD command)
▪ a partial pick will NOT require the approval of a supervisor
FIELD DESCRIPTIONS (RFPIC)

With both these options, the order line will be split into two: line 1 will contain the pick quantity and line 2 will contain the remaining quantity that could not be picked. Line 2 will NOT be placed on suspended hold and AccellosOne 
3PL will NOT attempt to reallocate the line 2 quantity.
NOTE The option that you select in this field can be overridden at the item level in the program MIRP (Item RF Profile Code) by selecting a different option for a given item.
Disallow Process Value 
Scanning
Yes
No
If you select Yes, the RF operator cannot scan process values in RFPIC. 
Instead, he/she must scan these values in RFOPS. If you select No, the RF operator can scan process values in either program.
Allow Picking Outside 
Pick Line
Yes
No
This flag allows you to pick pick line product from a non-pick line location such as bulk or rack when multiple replenishments for the same product cause overcrowding in your pick line. This choice is available when the full order quantity is not available in the pick line location and a replenishment has been generated.
For example, suppose your order quantity is 10 cases, there are only five cases in the pick line and the replenishment quantity is 60 cases. The RF operator can choose to pick the 10 cases from a bulk or non-pick line location instead of waiting for a replenishment and picking from the pick line. The 10 cases picked from bulk is subtracted from the replenishment quantity; 60 -10 = 
50. 
If you select Yes, pick line picking from a non-pick line location is activated. If you select No, pick line picking from a non-pick line location is not allowed.
Replenishment Rules for 
Pick Line
REPI done inside of RFPIC
REPI done separately (default)
Determined by the user
If you select “REPI is done inside of RFPIC”, the RF operator can perform replenishments in RFPIC. If you select “REPI is done separately”, the RF operator can only perform replenishments in RFRP or RFPL. If you select “Determined by the user”, each time that the RF operator logs in, he/she will be prompted to select a replenishment mode.
FIELD DESCRIPTIONS (RFPIC)

Display Original Order 
Number/Quantity for Consolidated Picks
Only available for consolidated picking after consolidating your orders in COPI (Consolidated Picking)
No Display
Display at UI Field
If you select No Display, the original order number and quantity will not be displayed when the RF operator selects a consolidated line. If you select Display at UI Field, RFPIC will display the original order number, quantity and SKU in a pop-up window after the RF operator selects the UI value.
RFPIC screen showing display of original order number and quantity
Display Pallet Screen Do not display
Display before Picking
Display on completion of Picking
Display after RFSC
If you select “Do not display”, the Pallet Block will not display in RFPIC and the 
RF operator will not be able to ship, receive or exchange pallets in this program. If you select “Display before Picking”, the Pallet Block will display before picking in RFPIC. If you select “Display on Completion of Picking”, the Pallet 
Block will display after picking in RFPIC.
If you select “Display after RFSC”, the Pallet Block will display after performing manual cartonization in RFSC.
FIELD DESCRIPTIONS (RFPIC)

## RFPIC (2) <a id="rfpic-2"></a>

*Manual H — RF Guide*

This tab shows additional RFPIC/RFPK options.
RFPIC (2) tab
RFPIC screen showing Pallet Block
FIELD DESCRIPTIONS (RFPIC)

.
FIELD DESCRIPTIONS (RFPIC 2)
Activate Inventory Count Always
Never
If Quantity Reaches or Falls Below Threshold Quantity
Every 2nd / 3rd / 4th / 5th / 6th / 7th / 8th / 9th Line
CP mode options
If you select “Always”, the RF operator will be required to enter an inventory count for each pick location in RFPIC. If you select “Never”, inventory counting in RFPIC will be deactivated. If you select “If Quantity Reaches or Falls Below 
Threshold Quantity”, a count will be required only if the on-hand quantity reaches or falls below the threshold quantity. 
If you select one of the line options (every 2nd, 3rd, 4th, etc. line), a count will be required only for every 2nd, 3rd, 4th, etc. pick.
Inventory Count Rules Only available if Activate Inventory Count is set to a value other than Never
These rules govern what happens in RFPIC when the inventory count for the location that is entered by the RF operator does not match the on hand system quantity.
Ignore investigations
No record will be created in ICIN (Inventory Count Investigation) and the RF operator can pick the order line.
Supervisor must override
The RF operator cannot pick an order line unless a supervisor logs in and either accepts or rejects the discrepancy. If the supervisor accepts the discrepancy, no record will be created in ICIN (Inventory Count Investigation). If the supervisor rejects the discrepancy, a record is created in ICIN.
Flow advancement not allowed
Super. override/No flow adv.
Reserved for future use.
Threshold Quantity to Initiate CountOnly available if you select If Quantity Reaches or Falls Below Threshold 
Quantity in the Activate Inventory Count / Hold field
Your threshold quantity for initiating an inventory count.

Automatically Assign Pallet IDYes
No
Use SSCC-18 Pallet Sequence Number
If you select Yes, a unique pallet ID will be generated in RFPIC while in CP (case pick) mode and the cursor will automatically advance to the Printer field. 
The system-generated pallet ID cannot be changed by the RF operator. 
If you select No, the RF operator has two choices when prompted for a pallet 
ID in RFPIC while in case pick mode: 
▪ he or she can press Enter to have AccellosOne 3PL generate a unique pallet ID
▪ he or she can enter or scan in a pallet ID not generated in AccellosOne 3PL.
The Yes option requires a label document in either the Label Document or 
Quick Response Label Document fields. If all your consignees use quick response labels, a label document is not required in the Label Document for 
RF Picking field. If some consignees use quick response labels while others do not, you must enter a label document in both fields. 
If you do not use quick response labels, a label document is not required in the Quick Response Label Document field.
If you select Use SSCC-18 Pallet Sequence Number, the unique pallet ID generated in RFPIC will be a valid SSCC-18 pallet sequence number.
Label Document Only available if Automatically Assign Pallet ID = Yes
If you enter a label document in this field, the Label field in RFPIC when working in CP (case pick) mode will be populated with the label document number. 
If you set up a detail record in DOCU for this document specifying both the printer and operator, the Printer field in RFPIC will be populated with the RF operator’s printer. 
Quick Response Label 
Document
Only available if Automatically Assign Pallet ID = Yes
If you enter a label document in this field, the Label field in RFPIC when working in CP (case pick) mode will be populated with the quick response number. 
If you set up a detail record in DOCU for this document specifying both the printer and operator, the Printer field in RFPIC will be populated with the RF operator’s printer. 
FIELD DESCRIPTIONS (RFPIC 2)

Sort Sequence Code (SOSE)
Optional
The sort sequence code used to sequence or “snake” the pick list of picking tasks in RFPIC. You can apply these advanced SQL statements to either item codes, location codes or inventory entities.
When you activate sort sequencing, the RF operator can initially pick any item, location or inventory entity from the sorted list, but once this initial choice is made the RF operator must finish picking the item, location or inventory entity in RFPIC before proceeding to another item, location or inventory entity. 
For example, suppose you set up a sort sequence based on item and there are three different items on a given order: item A, item B and item C. When the 
RF operator enters RFPIC and selects any item on the order — say item B — he or she must pick all order lines containing item B before picking another item. The same logic applies to the remaining items on the order; once a given item is selected, all order lines containing that item must be picked before proceeding to another item.
Pick list in RFPIC shown in location code sequence (A107, A107, B102)
NOTE The table name (c_invt, e_ord_d5d1 or m_loc) is required in your 
SQL statement.
If you do not specify a sort sequence code, picking tasks in the pick list will be sequenced in location code sequence.
FIELD DESCRIPTIONS (RFPIC 2)

Sort Sequence Based on Item
Location
Inventory Entity
The value that the sort sequence is based on.
Event-Driven Cycle 
Count Profile (CYCP)
See the Cycle Counting Guide for further information on event-driven cycle counts.
Enter Outbound Pallet ID 
Before Picking
Only available for case pick mode in RFPIC/RFITLV
No
Yes
If you select No, the RF operator must enter label parameters after picking his/ her order line(s). If you select Yes, the RF operator must enter label parameters before picking his/her order lines.
FIELD DESCRIPTIONS (RFPIC 2)

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
In this field, you set your label printing options for the outbound pallet ID label in RFPIC and RFPK. 
If you select 1, no label will print and the PRT field will be bypassed. 
If you select 2, the RF operator must press Enter in the L(abel) field to generate an AccellosOne 3PL OPID. Then he/she scans in this OPID to validate it. 
If you select 3, the RF operator must press Enter in the L(abel) field to generate an AccellosOne 3PL OPID, but does not perform a scan to validate it. 
If you select 4, the RF operator must manually enter or scan in your own nonAccellosOne 3PL OPID. If you select 5, the RF operator must manually enter or scan in your own non-AccellosOne 3PL OPID twice.
If you select 6, the RF operator must manually enter or scan in your own nonAccellosOne 3PL OPID. After printing the label, the RF operator must scan the printed label to ensure that its OPID matches the original OPID in the 
L(abel) field.
Option 7 is custom.
Extra Charge Entry Type See [Extra Charge Setup for RF](picking-rf.html#extra-charge-setup-for-rf) for further information.
FIELD DESCRIPTIONS (RFPIC 2)

## RFPIC (3) <a id="rfpic-3"></a>

*Manual H — RF Guide*

This tab shows additional RFPIC/RFPK options.
REPIC (3) tab
FIELD DESCRIPTIONS RFPIC (3) 
Display Rules for Location/UI/QuantityDisplay Location/UI When Picking from Pick Line
Display Location/UI for All Locations
Display and Bypass Location/Qty in NM Mode
Display and Bypass UI (non-reserve)
Display and Bypass UI When Picking from Pick Line
Skip Location-From and Go to UI; Show Line Qty and Skip Qty field in 
NM Mode
Depending on the option that you choose, you can speed up picking by eliminating certain key strokes and validations in RFPIC.

Separate Hazmat by Item in Each Pick
No
Yes
If you define segregation rules for hazardous product in IHZV (Item Hazardous Material Validation) and set this flag to Yes, your segregation rules will apply to RFPIC and RFMG. If you set this flag to No, any segregation rules defined in IHZV will be ignored in RFPIC and RFMG.
Warehouse/Location for 
Kit Lines
Reserved for future use.
Rules for Picking by Item/
UPC
Validate Item/UPC for All Locations (1)
Validate Item/UPC in Pick Line Locations (2)
No (3)
If you select option 1 or 2, the UPC code scanned by the operator will be checked against the UPC code set up in ALIT. If the inventory levels linked to the UPC code in ALIT match the inventory levels of the pick order line, the pick will be accepted as valid. If, on the other hand, the inventory levels linked to the UPC code in ALIT do NOT match the inventory levels of the pick order line, the pick will be rejected. 
Option 1 performs the validation for all locations, while option 2 performs the validation for pick line locations only.
If you select option 3, no validation of the level 2/3/4 values in ALIT will occur. 
For one-level accounts only, the operator can scan in either the item code (level 1) or the UPC code. 
Capture OPID Cube and 
Dimension
For custom use only
In RF Pick
In RF Sorting
If you select In RF Pick, the RF operator can capture in RFPIC the cubic dimensions in meters and the gross weight in kilograms for each carton/pallet. 
If you select In RF Sorting, the RF operator can capture in RFSC the cubic dimensions in meters and the gross weight in kilograms for each carton/pallet.
If you leave this field blank, the capture of cubic dimensions and gross weight will be deactivated in RFPIC and RFSC.
Disable Last Label Scan in RFPK
Reserved for future use.
FIELD DESCRIPTIONS RFPIC (3) 

Use Bookmark in Picklist Yes option not available if Sort Sequence Code (SOSE) field populated
No
Yes
If you select Yes, the first order line in the picklist selected by the RF operator will be bookmarked. When the RF operator finishes picking that line and returns to the pick list, the pick list will display the next order line after the bookmark rather than the first order line in the pick list.
Allow Case Pick While in 
CART Mode in RFPK
No
Yes
If you select Yes, pick method 7 (Less Than Full Pallet) will be activated in 
RFPK. 
Allow Reusable Cartons in RFPK
Reserved for future use.
Supervisor Override 
Required for BATP in 
RFPK
Override Required for Reduce Order Qty Only
Override Required for Short of Inventory Only
Override Required for Both Reduce Order Qty and Short of Inventory
Override Not Required for Exceptions
In this field, you specify under which circumstances a supervisor override is required when the RF operator is wave picking in RFPK in batch label pick mode. 
If you select “Override Required for Reduce Order Qty Only”, a supervisor override is required when the RF operator reduces the order quantity. For example, the order quantity is 10 eaches, there are 10 eaches in the location and RF operator picks five eaches.
If you select “Override Required for Short of Inventory Only”, a supervisor override is required when the RF operator shorts an order line. For example, the order quantity is 10 eaches, there are 10 eaches in the location but five are damaged. The RF operator picks five eaches and shorts the remaining five.
If you select “Not Required for Exceptions”, the RF operator can reduce the order quantity and/or short an order line without a supervisor override.
FIELD DESCRIPTIONS RFPIC (3) 

## RFPIC (4) <a id="rfpic-4"></a>

*Manual H — RF Guide*

This tab shows additional RFPIC/RFPK options.
MRFP (RF Profile Code) screen showing RFPIC (4) tab
Automatically Confirm 
Order After Last Pick
No
Yes
If you select Yes, the order will be automatically confirmed when the RF operator picks the last line. If you select No, the order must be manually confirmed in CHOF.
NOTE The Yes option does not allow any flows between FIPI (Finish Picking) and COOR (Confirm Order).
Enter Pallet Type No
Yes
If you select Yes, the RF operator must enter a valid pallet type defined in 
PALL in RFPIC. If you specify a pallet code for a consignee in the Pallet Code field in CONS, RFPICK will validate that any pallet code entered during order picking for that consignee will match the consignee's pallet code. 
FIELD DESCRIPTIONS RFPIC (3) 

FIELD DESCRIPTIONS RFPIC (4)
Allow Relocation if Allocated Product BlockedNo
Yes
If you select Yes, RFRL (RF Relocate) will display whenever the RF operator enters an “invalid UI”; that is, the UI is in the correct location, but is not allocated to the order. If you select No, an error message will display whenever the RF operator enters an “invalid UI” and RFRL will not be available.
The purpose of this flag is to make it possible to move product when it is directly in front of and therefore blocking product allocated to an order. 
Display and Pick SKU Display and PIck in Lowest SKU
Display in Order Line SKU, Pick in Lowest
If you select “Display and Pick in Lowest SKU”, pick quantities will always display in the lowest SKU even if this SKU differs from the SKU quantity in 
ENOR. Likewise, the pick SKU entered by the RF operator will always be the item’s lowest SKU.
If you select “Display in Order Line SKU, Pick in Lowest”, the display SKU will be that of the order line in ENOR while the pick SKU entered by the RF operator must be the item’s lowest SKU.

Allow Pick of Multiple 
OPID’s in RFPIC
No
Yes
Yes Plus Unconsolidated COPI Orders Only With Full Pallet Pick in NM 
Mode
If you select Yes, the RF operator in RF picking programs can pick multiple 
OPID’s and deliver them to a staging location in a single step. The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
If you select No, the RF operator is restricted to a single OPID per pick. 
Display Rules for Default 
Staging Location
Last Staging Location in Previous Pick, Scan not Required
Display Last Staging Location from Order, Scan Required
Display Last Order Staging Location and Load Staging Location, Scan 
Required
Display Last Staging Location from Order, Scan not Required
Do Not Display Staging Location in Normal Mode
In this field, you specify your display and scanning rules for the default staging location.
Picking Methods for PnD 
Location
Full Pallet Only
All Pick Modes
The pick mode(s) allowed for PnD locations.
Display Order of Items and Descriptions in Pick 
List
Item, Description
Description, Item
The display order of items/descriptions in the RFPIC pick list.
Display Pick Quantity in 
Higher UOM
No
Yes
If you select Yes, the pick quantity will display in the highest UOM or SKU type (usually PLT).
FIELD DESCRIPTIONS RFPIC (4)

Validate OPID Using 
MSVS Code
If you set up a special verifier SQL record in MSVS, you can perform custom validation of your OPID’s.
Capture Pallet Spots For custom use only.
Scan From Location in 
No
Yes
If you select No, the From Location field is automatically populated by AccellosOne 3PL and no scan by the operator is required. If you select Yes, the from location must be scanned by the operator for each pick.
Apply Mask to UI in 
Left 01 to Left 25
Right 01 to Right 25
You can mask up to 25 characters of the UI from either the left or the right to prevent RF operators from cheating by typing in rather than scanning the UI.
FIELD DESCRIPTIONS RFPIC (4)

Inventory Count Investigation TypeInvestigation for Every Picked Unconfirmed Order and OPID
If you select “Investigation for Every Picked Unconfirmed Order and OPID”, an 
ICIN record will be created for all on order inventory in the warehouse whose inventory levels match the inventory levels of a single picked pallet with a countback variance.
If you leave this field blank, an ICIN record will be created for the current pallet being picked only should that pallet have a variance during an RFPIC countback. All other pallets for unconfirmed orders containing the same inventory will NOT be assigned an ICIN record.
When a supervisor logs into RFPIC to investigate a variance, the following screen will appear:
If the supervisor enters Y for Resolved, no ICIN record will be created for the current pallet being picked if there is a variance. However, ICIN records will be created for all other pallets on open orders whose first three inventory levels match the inventory levels of the current pallet.
When selecting the resolved option, the supervisor will be prompted to confirm the quantity. If the supervisor quantity matches the system quantity, no ICIN record is created. If the supervisor quantity does not match the system quantity, one of the following will occur: 
▪ if the quantity entered is less than the system quantity, the difference will be placed on SUSP hold and the required number of ICIN records will be generated 
▪ if the quantity entered is greater than the system quantity, the prompt “Move excess to designated location with label” will display and the required number of ICIN records will be generated
FIELD DESCRIPTIONS RFPIC (4)

## RFPIC (5) <a id="rfpic-5"></a>

*Manual H — RF Guide*

This tab shows additional RFPIC/RFPK options
RFPIC (5) tab
If the supervisor enters N for Not Resolved, no ICIN records will be created and the RF operator will be prompted to re-pick the order line.
FIELD DESCRIPTIONS RFPIC (5)
Inventory Count Display 
Type
Ignore Count When Outbound Qty = Inbound Qty = Item Setup Qty
If you select this option, no inventory counts will be required when the standard quantity breakdown (say, 50 cases per pallet) is the same as both the inbound quantity and the outbound quantity. That is, a full pallet was received and is now being shipped in its entirety.
For variable quantity breakdown product, no inventory counts will be required if the outbound quantity breakdown matches the inbound quantity breakdown.
FIELD DESCRIPTIONS RFPIC (4)

Use Tie/Hi/Loose to Calculate Inventory Count 
Quantity
No
Yes
If you select No, the RF operator must enter the total quantity of product in a location when performing a count back. If you select Yes, the RF operator will be prompted to enter the tie, hi and loose quantities; AccellosOne 3PL will then calculate the total quantity.
Inventory Count for Pallet Pick in RFITLVNo
Yes
If you select No, count backs will be deactivated for full pallet picks in RFITLV. 
If you select Yes, count backs for full pallet picks will be generated according to normal count back rules.
Pick Mode in RFITLV Use Pick List
One Task at a Time
If you select Use Pick List, the normal pick list will display and the RF operator can choose the task that he or she wishes to work on. If you select “One Task at a Time, the RF operator will see a single task in the pick list and will not be able to select a specific task from a list or skip a task.
Validate Item and Other 
Levels Special Mode
Read Qty From Bar Code, Validate Item/Lot if exists in the bar code by 
BAPR setting (1)
Validate Item After Location Field (2)
If you select 1, you can extract the quantity from a GS1 bar code and validate levels 1/2 against the scanned bar code. If the pick quantity is manually entered rather than scanned from the bar code and does not match the order line quantity, an error message is displayed and supervisor approval is required to complete the pick.
RFPIC screen showing incorrect quantity message
If you select 2, validation of levels 1/2 against the scanned bar code occurs after the RF operator has entered the to location.
FIELD DESCRIPTIONS RFPIC (5)

### MISCELLANEOUS <a id="miscellaneous"></a>

This tab shows various miscellaneous options.
Pick Background Substitution RulesReserved for future use.
Location Validation in 
RFPK - CART Pick
No
Yes
If you select No, a location scan of the pick location will NOT be required in 
RFPK while working in cart pick mode. If you select Yes, a location scan of the pick location will be required in RFPK while working in cart pick mode.
Override SystemAssigned OPIDAllow
Disallow
Warning
If you select Allow, the RF operator can override the assigned OPID by typing/ scanning over. If you select Disallow, the OPID field is protected and cannot be changed. If you select Warning, a warning is presented: "OPID has been changed. Y = Continue. No = Reverse the Value". "Yes" allows the change; 
"No" cancels the change and leaves the original OPID.
RFPIC screen showing “Update not Allowed” message
RFPIC screen showing “OPID has been changed” message
FIELD DESCRIPTIONS RFPIC (5)

FIELD DESCRIPTIONS MISCELLANEOUS
Display Order Lines by 
Item/Location in RFPI
Item
Location
If you select Item, order lines will be sorted in item code order in RFPI. If you select Location, order lines will be sorted in location code order.
Picklist Rules in RF RelocatePicklist and validation
Picklist. No validation (default)
No picklist. Must validate
If you select “Picklist and validation”, the RF operator can select the from location from a picklist and must scan in the from location to validate. If you select “Picklist. No validation”, the RF operator can select the from location from a picklist, but does not scan in the from location. If you select “No picklist. Must validate”, the RF operator cannot select the from location from a picklist, but must scan in the from location to validate.

Validation Rules for Relocate to Pick LineStop operator from proceeding
Allow operator to proceed
Omit validation of location
If you select “Stop operator from proceeding”, the RF operator will not be able to put-away product in RFPU to a pick line location that is not set up for that product in PIIT. If you select “Allow operator to proceed”, a warning message will display when the RF operator attempts to put-away product to a pick line location not set up for the product. However, the RF operator can bypass the warning message by pressing F3 to process. If you select “Omit validation of location”, the RF operator will be able to put-away product to any pick line location without restriction.
Validate Level Number in 
Physical
Optional
Refer to the Physical Inventory Guide.
Validate Quantity in Order 
Move
Yes
No
If you set this flag to Yes, the RF operator must enter the quantity being moved when relocating product in RFST. The quantity being moved is the number of cases/eaches or other SKU that has been assigned to an outbound pallet ID in RFPIC. If you set this flag to No, the quantity being moved is not entered when relocating product in RFST.
Validate From Location in 
Order Move
Yes
No
If you set this flag to Yes, the RF operator must enter the from location when relocating product in RFST. If you set this flag to No, the from location is not required.
Location Type of To Location in Order MoveAny Location
Staging Location Only
Pick Location Only
Staging Location Excluding Door Location
The required location type of your to location when relocating product in 
RFST.
FIELD DESCRIPTIONS MISCELLANEOUS

### MISCELLANEOUS (2) <a id="miscellaneous-2"></a>

This tab shows additional miscellaneous options.
Allow Directed Move in 
RF Relocate
Yes
No
If you set this flag to Yes, the RF operator can perform directed moves in 
RFRL. AccellosOne 3PL will select the best possible to location for a relocation based on your directed move stock parameters set up in ILOP. If you set this flag to No, the RF operator cannot perform directed moves in RFRL.
Display From Relocation 
Quantity in RF Relocate
Yes
No
If you select Yes, AccellosOne 3PL will display the from relocation quantity in the QTY field in RFRL and position the cursor in the LOC TO field. The RF operator can either proceed to relocate all product in the location or can press 
F9 and change the quantity. 
The from relocation quantity will be displayed in “cooked” format; that is, 1 pallet/25 cases instead of 125 cases or 5 cases/10 eaches instead of 110 eaches. This option is designed for facilities where relocating all inventory in a location is the rule rather than the exception.
The following conditions must be met before the from relocation quantity will display:
▪ all product in a given location belongs to the same inventory entity
▪ the quantity contains more than one SKU type; for example, there are two pallets, 20 cases in a location or 30 cases plus 10 eaches in a location. 
If you select No, the from relocation quantity will not be displayed in RFRL.
Allow RFCY Supervisor 
Count
Reserved for future use.
Print Inventory Access/
REPI Quantity Label
Reserved for future use.
Document Code for 
Quantity Labels
This field allows you to specify a document code for replenishment labels. A custom document from HighJump is required.
FIELD DESCRIPTIONS MISCELLANEOUS

Miscellaneous (2) tab
FIELD DESCRIPTIONS MISCELLANEOUS (2)
Use Pick Ticket Instead of RF Pick
Yes
No
If you select Yes, RF operators picking in RFPK will not have access to order lines assigned to either the CART or EACH pick method. These order lines must be picked manually outside of RFPK.
If you select No, RF operators picking in RFPK will enjoy full access to all order lines regardless of pick method.

Rules for Uniqueness of 
Serial Number
Per Document
Per Item for a Document
Per Entity for a Document blank
This field allows you to define how AccellosOne 3PL checks for duplicates in the following RF programs: RFIPS and RFOPS.
If you select Per Document, no duplicate serial numbers will be allowed within the same receipt/order. If you select Per Item for a Document, no duplicate serial numbers within will be allowed for the same item on a single receipt/ order. If you select Per Entity for a Document, no duplicate serial numbers will be allowed within the same inventory entity on a single receipt/order. If you leave this field blank, duplicate serial numbers will be allowed without restriction.
If the MRFP rule is violated, the RF operator will not be allowed to proceed.
Allow Merging Orders/
Items to One OPID Within 
Load (RFMG)
See [Merging OPID’s in RFMG](expedicao-rf.html#merging-opid-s-in-rfmg)
Allow Merging Up To 
Level (RFMG)
Level 1
Level 2
Level 3
You can merge inventory entities at inventory levels other than the lowest. For example, suppose you select Level 1 and merge two pallets with different lot numbers and pallet ID's. The adjusted out lot number and pallet ID will be lost and the adjusted in lot number and pallet ID quantity will be adjusted accordingly.
Refresh Screen After 
Each Relocation (RFRL)
Yes
No
If you select Yes, a blank RFRL screen will display for the RF operator after each relocation. If you select No, RFRL will not refresh after each relocation.
Confirm OPID for Pick 
Method in RFCO 
CART
If you select CART, order lines assigned the pick method of CART can have their OPID’s confirmed in RFCO. If you leave this field blank, order lines assigned the pick method of CART can only be confirmed in CHOF (that is, they cannot be confirmed in RFCO).
FIELD DESCRIPTIONS MISCELLANEOUS (2)

RF Relocation Executed by
Scan Location to Execute Relocation
UI Scan Only
Scan Location to Execute Relocation; UI Scan Only
In this field, you select how you want to execute a relocation. If you select “Scan Location to Execute Relocation”, the RF operator must scan the from location to execute the relocation and pressing F3 (Process) is not required. If you select “UI Scan Only” in this field, the RF operator must scan the UI to execute the relocation. If you select “Scan Location to Execute Relocation; UI 
Scan Only”, the RF operator must scan both the from location and the UI to execute the relocation.
Allow Mixed Pallet Allow Relocation of Mixed Pallets in RFRL
If you select this option, you can relocate a mixed pallet (multiple items, lots, date codes, etc.) in a single relocate action. A pallet license relocate will move all inventory records associated with the pallet. 
Show RF Confirm OPID 
Summary
Yes
No
If you select Yes, a pop-up screen displays in RFCO showing an order summary for each OPID. The summary shows the pick method as well as the total number of units in the OPID. 
Create RF Confirm OPID 
Audit
Yes
No
If you select Yes, a time-stamp message is inserted in the Time Block of 
LOOR indicating that the OPID was confirmed in RFCO. If you select No, no time-stamp message is inserted in the Time Block of LOOR.
FIELD DESCRIPTIONS MISCELLANEOUS (2)

### MISCELLANEOUS (3) <a id="miscellaneous-3"></a>

This tab shows additional miscellaneous options.
RFOA Audit Level Level 1
Level 2
Level 3
Level 4
RFOA allows you to perform an audit of staged product before it is loaded onto the truck. In this field, you define your inventory level for such audits. 
For example, if you select Level 1, the RF operator will perform a count for each item on the order. If, on the other hand, you select Level 2, the RF operator will perform a count for each lot on the order.
RFOPS Sort Sequence 
Code (SOSE)
In this field, you can define a sort sequence for your process values in 
RFOPS. For example, an unsorted list of process values might appear as follows:
▪ carton ID
▪ carton ID
▪ carton ID
▪ weight
▪ weight
▪ weight
After sorting, the same list of process values could appear in a more logical order:
▪ carton ID
▪ weight
▪ carton ID
▪ weight
▪ carton ID
▪ weight
FIELD DESCRIPTIONS MISCELLANEOUS (2)

Miscellaneous (3) tab
FIELD DESCRIPTIONS MISCELLANEOUS (3)
Other Inventory Count 
Programs
In this field, you select the RF program(s) in which you wish to perform count backs.
Activate Inventory Count Always
Never
If Quantity Reaches or Falls Below Threshold Quantity
If you select “Always”, a count back is required each time the RF operator puts away/relocates/replenishes product. For put-away activities, the location counted is always the to location. For relocation and replenishment activities, the RF operator counts the inventory in the from location.
If you select “If Quantity Reaches or Falls Below Threshold Quantity”, a count back is only required if the quantity in the to location (for RF receiving) or the from location (for RF relocation and replenishment) falls below the threshold quantity that you define in the Threshold Quantity to Initiate Count field.

Inventory Count Rules Require Supervisor Override
Ignore Investigation But Lock the Entity (reserved for future use)
Ignore Investigation
These rules govern what happens when the inventory count for the location that is entered by the RF operator does not match the on hand quantity. If you select “Require Supervisor Override”, a supervisor will be required to log in and approve the discrepancy. If you select “Ignore Investigation”, the RF operator can proceed normally to the next pick/relocation/put-away, etc.
Threshold Quantity to Initiate CountOnly available if you select If Quantity Reaches or Falls Below Threshold 
Quantity in the Activate Inventory Count field
Your threshold quantity for initiating an inventory count.
Inventory Count for All RF 
Based On
Item
Item Count for Pick Line Locations, Entity Count for Rest of Locations
If you select “Item”, the RF operator will count each item in a given location. If you leave this field blank, the RF operator will count each inventory entity in a given location. If you select “Item Count for Pick Line Locations, Entity Count for Rest of Locations”, the RF operator will count each item for pick line location types and each inventory entity for all other location types.
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
In this field, you define the suggested or default to location in RFST. If you select “Follow Order”, the suggested location will be the to location where the last OPID was staged. In other words, the suggested to location is always the to location chosen in the previous order line.
If you select Follow “Assigned Staging Location”, the suggested location will be the staging location assigned to the order line in either SELO or the Wave 
Manager. It will not change for a given order even if the RF operator overrides the suggested to location.
FIELD DESCRIPTIONS MISCELLANEOUS (3)

### MISCELLANEOUS (4) <a id="miscellaneous-4"></a>

This tab shows additional miscellaneous options.
Display To-Location in 
RFST
Yes option only available if Suggested Location Rules in RFST is activated
Yes
No
If you select Yes, the suggested to location is displayed. If you select No, the suggested to location is not displayed.
Default Staging Warehouse/Location Code in 
CASE
Custom use only.
Enter Adjustment InformationYes
No
If you set this flag to Yes and enter an adjustment in RFAJ, you will be prompted to enter an adjustment code (ADJU), a reason code (REAS) and remarks for each adjustment. If you set this flag to No, you will not be prompted for an adjustment code, reason code and remarks.
Allow Relocation of Multiple Pallets in RFRLYes
No
If you select Yes, the RF operator can relocate multiple pallets in a single step; 
that is, the RF operator scans two or more UI’s but only enters the to location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
FIELD DESCRIPTIONS MISCELLANEOUS (3)

Miscellaneous (4) tab
FIELD DESCRIPTIONS MISCELLANEOUS (4)
Allow Replenishment of 
Multiple Pallets in RFRP
Yes
No
If you select Yes, the RF operator can replenish multiple pallets in a single step; that is, the RF operator scans two or more UI’s but only enters the to location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type

Allow Mixed Put-Away, 
Move up to Inventory 
Level
Up to level 1
Up to level 2
Up to level 3
If you select “Up to level 1/2/3”, the RF operator can put-away and move multiple pallets in the same location in a single step. The multiple pallets can contain mixed inventory up to the inventory level selected. For example, pallets from different receipts, appointments and inbound loads containing different level 2’s and 3’s can be placed on the same forklift and put-away together if you select “Up to level 1”.
This field applies to the following programs: RFCH, RFPU, RFST, RFRL, 
RFRP and OLOP.
If you leave this field blank, the RF operator cannot put-away/move mixed product in a single step.
Reason Code Required to Override SystemAssigned Location
Yes
No
Yes with Location Overridden (reserved for future use)
If you select Yes, the RF operator will be required to enter a reason code in 
RFCH/RFPU/RFRL if he or she overrides the system-assigned location code or requests an alternate location. For RFCH/RFPU overrides only, the reason code will be stored on the receipt line and a time stamp will be created.
RFCH screen showing pick list for reason code
Max. Number of F3 (NX) 
Allowed Per ILOP 
Sequence in RFRL
In this field, you specify the maximum number of times that the RF operator can press F3 (NX) in RFRL to display a suggested relocate location.
FIELD DESCRIPTIONS MISCELLANEOUS (4)

Allow Multiple Pallet 
Moves in RFST
Yes
No
If you select Yes, the RF operator can relocate multiple pallets in a single step; 
that is, the RF operator scans two or more UI’s in RFST but only enters the to location once.
The following restrictions apply:
▪ all product has the same level 1
▪ equipment tracking must be activated in COMP
▪ the Location Required flag in MHET must be activated 
▪ the pallets do not contain mixed hold codes
▪ the number of pallets moved does not exceed the maximum capacity for the equipment type
Show Quantity Breakdown ScreenYes
No
If you select Yes, the item quantity breakdown will display as a pop-up message in the following programs: RFPIC, RFPK, RFRL, RFPR, RFRP, RFCH and RFPU.
Allow Skipping of 
Inbound Serial Number 
Validation in RFOPS
Yes
No
If you set this flag to Yes, you can skip the validation of inbound serial numbers when shipping serial number product in RFOPS. AccellosOne 3PL will create a new system-generated outbound serial number for the product being shipped. This feature is designed to save time and improve efficiency by eliminating the need to perform a validation scan for each case. 
For example, you are entering a transfer order to transfer serial number product from one account to another.
RFOPS screen showing F1 (SE) command
FIELD DESCRIPTIONS MISCELLANEOUS (4)

The RF operator selects ME (Manual Entry). After entering the weight, the RF operator can press F1 (SE) to create a new system-generated serial number.
Allow Weight Reduction for Standard Weight Item in RFOPS
Yes
No
If you set this flag to Yes, you can reduce standard weight product by entering a quantity; for example, 5CS. The quantity entered by the RF operator must be less than or equal to the order quantity. When the RF operator presses F2 (RC), the following prompt will appear:
RFOPS screen showing option 2
Enter Gross Weight in 
RFSC
Yes
No
If set to Yes, the RF operator will be required to enter the gross weight when closing a carton in RFSC. The weight measure code for the carton will be defined in DITP (Depositor Item Profile).
FIELD DESCRIPTIONS MISCELLANEOUS (4)

### MISCELLANEOUS (5) <a id="miscellaneous-5"></a>

This tab shows additional miscellaneous options.
Allow Put-Back of Outstanding REPI QuantityIn this field, you define put-back rules when the RF operator performs a partial replenishment (for example, less than a full pallet) because blocked or damaged product is preventing a full replenishment.
EXAMPLE
Item quantity breakdown: 50 cases per pallet replenishment quantity from bulk: 45 cases (less than a full replenishment)
order quantity: 10 cases
No
A second replenishment of five cases is created (50 - 45 = 5) for the original pick line location.
Yes
RF operator is prompted to perform a second replenishment of 5 cases to either the original pick line location or to another pick line location.
Cancel REPI Task
If the on-hand quantity in the pick line location is greater than the on order quantity, the second replenishment is deleted. If the on-hand quantity in the pick line location is NOT greater than the on order quantity, a second replenishment is created for the original pick line location (same as No option).
Enable UI Scanning in 
Cycle Counts
Custom use only.
Suspend Flow Advancement in Outbound AuditYes
No
If you select Yes, the order line will NOT be advanced to the next flow even though your count matches the order line quantity when you perform an outbound audit in RFOA. If you select No, the order line will be advanced to the next flow when your count matches the order line quantity in RFOA. 
FIELD DESCRIPTIONS MISCELLANEOUS (4)

Miscellaneous (5) tab
FIELD DESCRIPTIONS MISCELLANEOUS (5)
Retain OPID to in RFMG Yes
No
If you select Yes, the OPID to value remains displayed on the screen after the merge so that the RF operator can continue to merge into the same OPID.

Validate Manual Entry 
Process in RFOPS
Yes
No
If you select Yes, the following validations will occur when manually entering catch weights and serial numbers in RFOPS:
▪ the entry length and data type must match your setup in IPRO
▪ the outbound weight/serial number must match the inbound weight/serial number
▪ if the outbound weight does not match the inbound weight, it must be within the weight tolerance percent defined in ITEM
If you select No, only the entry length and data type must match your setup in 
IPRO.
Disallow REPI When 
Location Reaches Maximum Capacity
Yes
No
If you select Yes, replenishments will be canceled when the replenishment quantity plus the on-hand quantity in the pick line location exceeds the location's capacity. If you select No, replenishments will NOT be canceled when the replenishment quantity plus the on-hand quantity in the pick line location exceeds the location's capacity.
NOTES 
▪ Product on SUSP hold is not included in the pick line location’s on-hand quantity.
▪ The Yes option in MRFP will be ignored if you have shelf live overrides in 
CCOP (Customer/Consignee Override of PIPR) for an order triggering a replenishment.
Validate Serial Number (SN) From Picking Process
Yes
No
If you select No, serial number validation will be deactivated in RFSC. If you select Yes, serial number validation will be activated in RFSC and a valid serial number must be scanned for all product being packed in RFSC.
The purpose of the additional scan in RFSC to make sure that the serial number scanned during RFPIC is the same serial number going in the box during packing.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

Display Minimum Number of REPI Records in 
Demand Mode
Yes
No
If you select Yes and there are multiple replenishment records for the same item, AccellosOne 3PL will show only the replenishments that are needed to satisfy the order quantity. Other replenishments that are required to satisfy the minimum quantity for the location will not appear in active demand mode.
For example, suppose there are 255 cases in a pick location with 305 on order. Although there are three replenishments for a total of 144 cases, only 
60 cases are needed to meet the order quantity and therefore only one replenishment (the one for 60 cases) will show in demand mode.
Override Quantity Breakdown - Actual (if > Std) or 
Std
Override Quantity Breakdown Type
If you select Override Quantity Breakdown Types, the following rules will apply to RFCH and RFMI:
▪ if the pallet quantity associated with the UI is less than the standard item quantity breakdown, use the standard quantity breakdown
▪ if the pallet quantity associated with the UI is greater than or equal to the item quantity breakdown, use the actual quantity breakdown
▪ for a pallet/case/each breakdown, the standard case/each configuration will not change
NOTE 
The quantity breakdown entered in RFCH will overwrite the quantity breakdown entered/set up in ENRE and EDI.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

Display Process Description in RFOPSYes
No
If you select Yes, the item process code description will display in RFOPS. If you select No, the item process code only with no description will display.
RFOPS screen showing process code description
Allow Entry of Adjustment 
Code in RFMI
Yes
No
If you select Yes, the RF operator will be prompted to enter an adjustment code for the merge. If you select No, the default adjustment code set up in 
ATMP (Action Template Setup) will be used.
REPI Pick Location 
Capacity Based on UI
Yes
No
If you select Yes, the pick line location capacity will be based on the number of 
UI’s in the location and not on the number of units in the location. For example, if a location’s capacity is defined as two pallets and there are two UI’s in the location, the location will be considered full even if the two UI’s consist of partial pallets. When a pick line location is considered full, no replenishments will occur.
If you select No, the pick line location capacity will be based on the actual number of units in the location and not on the number of UI’s in the location.
FIELD DESCRIPTIONS MISCELLANEOUS (5)

### Item RF Profile (MIRP) <a id="item-rf-profile-mirp"></a>

In this program, you set up your suspended hold and inventory count rules at the item level. If you define a profile in MIRP and attach it to an item in ITEM, the suspended hold/inventory count rules in MIRP will override your suspended hold/inventory count defaults for a given customer defined in MRFP.
Location Scan Required for Count Backs and Suspend Holds
Yes
No
If you select Yes, the supervisor will be forced to scan in the current location when clearing a count back discrepancy or approving a suspended hold. If you leave this flag blank or set it to No, the supervisor will not be forced to scan in the current location when clearing a count back discrepancy or approving a suspended hold.
Allow Override of Receipt 
Line ILOP in RFCH
Yes
No
This flag allows you to manually remove an ILOP override attached to a receipt line in ENRE. If you select Yes, a pop-up will appear in RFCH allowing the RF operator to accept or remove the ILOP profile for the item being received. If you select No or leave this field blank, no pop-up will appear in 
RFCH allowing the RF operator to accept or remove the ILOP profile attached to the receipt line.
RFCH pop-up screen showing two options
FIELD DESCRIPTIONS MISCELLANEOUS (5)

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
The various zero out remaining quantity options allow the picker to pick any quantity up to the order line quantity. For example, if the order line quantity is 5 cases, the picker can pick 0, 1, 2, 3, 4 or 5 cases. AccellosOne 3PL will automatically zero out the remaining lines so that the order will ship without the need to reallocate the missing product or manually delete the lines in ENOR. 

### MISCELLANEOUS TAB <a id="miscellaneous-tab"></a>

If you select any options in these fields, they override the option(s) that you selected in MRFP.

### Warehouse/Customer/Location Config (WCLC) <a id="warehouse-customer-location-config-wclc"></a>

This program allows you to activate/deactivate UI scanning in RFPIC by warehouse code and customer code. 
It overrides the Display Rules for Location/UI/Quantity field in MRFP (RFPIC 3 tab). If you activate UI scanning for a given warehouse code/customer code combination, RFPICK will display the UI and the RF operator will need to press Enter to enter the QTY field. If required, the RF operator can overtype the UI.
Show Full Item Description in RFCHYes
No
If you select Yes, a pop-up box will display showing both the main item description and the alternate description in RFCH. if you select No, no pop-up box will display in the program.
Show Full Item Description in RFPICYes
No
If you select Yes, a pop-up box will display showing both the main item description and the alternate description in RFPIC. if you select No, no pop-up box will display in the program.
Activate Event-Driven 
Cycle Count in RFPIC
See the Cycle Counting Guide for further information on event-driven cycle counts.
Activate Inventory Count If you select an option in this field, it overrides the option that you selected in 
MRFP.
Inventory Count Rules If you select an option in this field, it overrides the option that you selected in 
MRFP.
Threshold Quantity to Initiate Count BackIf you select an option in this field, it overrides the option that you selected in 
MRFP.
Assign Pallet ID on Full 
Pallets of Last Inventory
If you select an option in this field, it overrides the option that you selected in 
MRFP.
FIELD DESCRIPTIONS (RFPIC TAB)

WCLC screen
In the Detail Block, you can switch on or off UI scanning for individual locations within the warehouse that you specified in the Header Block.
WCLC screen showing Detail Block

### Depositor Workflow Profile (DIFP) <a id="depositor-workflow-profile-difp"></a>

Certain flows are mandatory for inbound and outbound processing in DIFP. Refer to the appropriate program (RFCH, RFPI, RFPIC, etc.) to see which flows are required for a given program.

### RF Operator (RFOP) <a id="rf-operator-rfop"></a>

In this program, you set up your RF operators and define their default company and Vocollect Voice password. In the Detail Block, you define which task profiles they are allowed to work in as well as their material handling type and activity type exclusions.
RF operators in RFOP are required in the following cases:
▪ you perform voice-activated picking using Vocollect Voice
▪ you pick by assignment in RFVP (RF Voice Pick)

▪ you assign tasks to operators in RFOT (RF Operator Task Assign)
▪ you wish to track the equipment used by each RF operator and restrict certain RF operators to certain activity types and equipment types
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
Operator (defined in OPER)
Mandatory
Your operator code.
Default Company Mandatory
The company in which the RF operator will work. If you use Vocollect Voice and the operator has to switch companies, you must manually change the operator’s company in RFOP. If you pick your orders in RFPIC, you do not need to manually change the operator’s company in RFOP as the operator can perform this task in RFPIC.
Password Only required if you do voice-activated picking
The operator’s Vocollect Voice password.
MHET Types Exclusions See [RF Operator (RFOP)](picking-rf.html#rf-operator-rfop) for further information.
Activity Type Exclusions See [RF Operator (RFOP)](picking-rf.html#rf-operator-rfop) for further information.
Task Profile Enter the RF operator’s task profile.

RFOP screen showing operator PAUL assigned to task profile 1
8 Click on Exit to exit.
9 When prompted to save your changes, click on Yes.

### ACTIVATING AN RF OPERATOR IN ACTIVEDESKTOP <a id="activating-an-rf-operator-in-activedesktop"></a>

If the RF operator is a new AccellosOne 3PL operator who has never logged on to ActiveDesktop, he or she must log on to ActiveDesktop to change his or her password. You cannot log on to a RF device with the default password defined in INST (Installation Parameters).
1 Log on to ActiveDesktop and proceed to change your password. Once your new password is accepted, you can log on to a RF device using this password.

### Extra Charge Setup for RF <a id="extra-charge-setup-for-rf"></a>

You can add extra charges to a receipt or order in RF using the program RFEC (RF Extra Charge). You can also enter extra charges directly in RFPIC (for outbound orders) and in RFCH (for inbound receipts). You activate extra charge entry in RF by making the appropriate changes to your extra charge profile in ECHP (Extra Charge Profile).

Extra charge entry in RF is only available for customer-based extra charges; that is your ECHP profile is attached to a customer. AccellosOne 3PL does not support RF extra charges attached to an item.
FIELD DESCRIPTIONS (ECHP)
Charge Code (CHAR) The charge code that you enter must be unique in ECHP within a given inbound or outbound workflow. You cannot use the same charge code under a different sequence for a given inbound or outbound workflow. 
Allow RF Entry / Allow 
Override of Charge 
Quantity in RF
There are three possible scenarios for these two fields:
Allow RF Entry = No
Allow Override of Charge Quantity in RF = No
In this scenario, the RF operator cannot add extra charges in RF.
Allow RF Entry = No
Allow Override of Charge Quantity in RF = Yes
In this scenario, the RF operator can select one or more extra charges from a predefined list and can enter any charge quantity for the selected charge(s).
Allow RF Entry = Yes
Allow Override of Charge Quantity in RF = Yes
In this scenario, the RF operator must manually enter his or her extra charges (if any) and can enter any charge quantity for the entered charges.
Flow Process Code (FLPR) for RF
Optional
If you enter a flow, the extra charge can only be added at this inbound or outbound flow. If you leave this field blank, the extra charge can be added at any inbound or outbound flow.
Other fields Refer to the Billing and Invoicing Guide for further information.

ECHP screen showing fields for extra charge entry in RF
For inbound extra charges, you must set the Extra Charge Entry Type flag on the RFCH Only 2 tab in MRFP to the appropriate value.
FIELD DESCRIPTIONS (RFCH ONLY 2)
Extra Charge Entry Type Allow Extra Charge Entry When Completed
Allow Extra Charge Entry When Exiting
If you select “Allow Extra Charge Entry When Completed”, the extra charge screen will display when you finish checking/unloading the receipt line. If you select “Allow Extra Charge Entry When Exiting”, the extra charge screen will display when you exit RFCH.

For outbound extra charges, you must set the Extra Charge Entry Type flag on the RFPIC tab in MRFP to the appropriate value.

### Warehouse Zones (WHZO) <a id="warehouse-zones-whzo"></a>

In this program, you subdivide your warehouse into separate zones. Each zone can be considered a separate work area and the same order or receipt can be assigned to multiple RF operators working in different zones. 
A zone can be a section of your warehouse or a set of racks (for example, all floor-level racks could be zone 
1, all second-level racks could be zone 2, etc.).
There are seven zone types in WHZO:
FIELD DESCRIPTIONS (RFPIC 2)
Extra Charge Entry Type Allow Extra Charge Entry When Completed
Allow Extra Charge Entry When Exiting
If you select “Allow Extra Charge Entry When Completed”, the extra charge screen will display when you finish picking the order line. If you select “Allow 
Extra Charge Entry When Exiting”, the extra charge screen will display when you exit RFPIC.
Directed Put-Away Directed put-away zones allow you to define overflow sequences for directed put-away in the Overflow Sequence Block. For example, if no locations are available in put-away zone 1, try put-away zone 2 then put-away zone 3.
General General zones have no collection or drop off points assigned to them.
Sorting Area Sorting Area zones types have a drop off point assigned to them; that is, they require a location code in the header block of WHZO.
Material Handling Type This zone type is used for material handling type integration.
P & D P & D zones types have a collection point assigned to them; that is, they require a location code in the header block of WHZO.
Interleaving Interleaving zone types are used in RFITLV.
Voice Voice zone types are used for voice-activated picking.

P & D zone consisting of 12 locations in aisle A with a P & D location (A100)

### HEADER BLOCK <a id="header-block"></a>

In this block, you define your warehouse zone code and description, your zone type code and your warehouse/location code for sorting or P & D zones types.
A100 (P & D location)
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
Communication ReferenceReserved for future use

### FORMULA BLOCK <a id="formula-block"></a>

The Formula Block allows you to specify warehouse and location restrictions (for example, a range of locations) for the zone. When you exit the Formula Block, the system will automatically add the locations that you specify to the zone. If you use the Formula Block in modify record mode, any existing locations assigned to the warehouse zone will be removed and new locations will be assigned based on your formula.
Zone Type Code D = Directed Put-Away
G = General
M = Material Handling Type
S = Sorting Area
P = P & D
I = Interleaving
V = Voice
The zone type field allows you to define collection and drop off points for a zone and to assign to it a specific material handling equipment type.
If you select General, the zone will have no collection or drop off points. If you select Sorting Area, the zone will have a collection point for outbound product. 
If you select P & D, the zone will have a drop off or pick-up point for product.
Task Required Only available if Enable Task Interleaving in COMP = Create Tasks According to Zone Setting
See [Warehouse Zones (WHZO)](expedicao-rf.html#warehouse-zones-whzo).
Warehouse Code (defined in WARE)
Mandatory if zone type = S or P
The warehouse code of the location that you wish to attach to the zone.
Location Code (defined in LOCA)
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

If your location codes contain spaces or hyphens (-), you must use the caret character (^) before the space or hyphen.
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
If you specify Inbound, the locations added by the system will all be flagged as inbound locations. If you specify Outbound, the locations added by the system will all be flagged as outbound locations. If you specify Both, the locations added by the system will all be flagged as both inbound and outbound locations.
If you are setting up a P, S or M zone type, the value that you enter in this field is ignored because the zone type is either self-defined or defined in other programs.
Warehouse Code (defined in WARE)
Mandatory
Only locations belonging to the warehouse(s) that you specify can be added to the zone. See the following paragraph for a list of the operands that you use to specify one or more warehouses. 
Location Code (defined in LOCA)
Mandatory
Your location restrictions for the zone. See the following paragraph for a list of the operands that you use to specify one or more locations.

The following operands can be entered in the Warehouse Code and Location Code fields:
EXAMPLES
= match of characters entered (=) not equal to
> greater than or equal to
< less than or equal to
- from X to Y (a range)
=1 Any location code beginning with 1 (for example, 1, 111, 199, 1ABC)
=1,=2 Any location code beginning with 1 or 2 (for example, 1, 111, 299, 2ABC)
(=1) All warehouses except warehouse 1 (=1),(=2) All warehouses except warehouses 1 and 2 
>F101 All locations greater than or equal to location F101
(for example, F102, F199, F4, G99, etc.)
<D101 All locations less than or equal to location D101
(for example, A101, B999, D100, etc.)
A101-C999 Locations A101 through C999

Warehouse Zone Codes showing Formula Block

### PROCEDURE <a id="procedure"></a>

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
a) Proceed to next step. a) Key in your warehouse code and press Enter.
b) Key in your location code and press Enter.
c) Press Enter the required number of times to bypass the material handling type fields.

Warehouse Zone Codes showing Formula Block
10 When the Formula Block appears, do one of the following:
11 In the Warehouse Code field, key in your warehouse code restriction (for example, “=”) and press Enter. 
12 In the Location Code field, key in your location restrictions (for example, “>”) and press Enter. AccellosOne 3PL will retrieve all locations that meet the criteria that you specify and display the Locations 
Block. If there are no location restrictions, leave this field blank.
Warehouse Zone Codes showing External Messages
13 If you wish to print, fax or e-mail your External Messages, click on Select Printer. Then key in the appropriate printer code or use the pick list function to select it. Next click on Execute Report. If you selected either fax or mail as your printer, the Fax/Mail Entry pop-up window will appear. Enter your fax number or e-mail address and any other required information and then click on Send e-mail or Send fax.
For G or I type zones: For P or S type zones:
a) Key in I for Inbound, O for Outbound or B for Both in the 
Inbound/Outbound field and press Enter.
a) Key in B for Both in the Inbound/
Outbound field and press Enter.

14 Click on Exit to close the External Messages window. The locations that you specified in the Formula 
Block will be added to your zone.
15 Click on Location Block.
Warehouse Zone Codes showing 28 locations assigned to Zone 2
16 If required, you can manually add or remove a location in the Location Block. To add a location, click on 
Create Record and key in your warehouse code, your location code, your inbound/outbound value and your zone type.
If you wish to remove a location from the Location Block, move your arrow key to the appropriate location and press Enter until your cursor is positioned in the Inbound/Outbound column. Then click on Delete. 
If you wish to change the Inbound/Outbound flag, key over the default value of B for Both with either I for 
Inbound or O for Outbound.
When you finish making your changes, click on Return to Main.
17 When you finish setting up your zone, click on Master Block and then Exit to exit.

### OVERFLOW SEQUENCE BLOCK <a id="overflow-sequence-block"></a>

If product cannot be put-away in a given warehouse zone, you can define an overflow sequence for warehouse zones in the Overflow Sequence Block. The overflow zones must have the same zone type code as the header zone.
Warehouse zones used in directed put-away require a zone type code of D (for Directed Put-Away).

WHZO screen showing overflow zone codes

### Company Code (COMP) <a id="company-code-comp"></a>

The following fields in COMP may require setup:
FIELD DESCRIPTIONS (MISCELLANEOUS 5)
RF Special Character You can define a special character (for example, $) or a string of special characters as an RF check digit for your location codes. If you deactivate the special characters on your RF guns, RF operators will be forced to scan in the location code rather than typing it in manually.
RF special character logic allows up to five special characters and applies to 
RFCH, RFRL, RFPIC and RFRP.

### RF Supervisors <a id="rf-supervisors"></a>

RF supervisors have certain privileges that are denied to non-supervisory RF operators; for example, they can zero out receipts lines in RFCH when a variance is encountered. See the System Administration Guide for further information on setting up an RF supervisor.

### Supervisor Notification <a id="supervisor-notification"></a>

The supervisor notification system is triggered whenever a non-supervisory RF performs an action that requires supervisor approval. For example, the RF operator creates a new receipt line in RFCH, changes a suggested put-away location in RFPU, places product on hold in RFPIC, etc. The specific actions that require supervisor approval are defined in MRFP (RF Profile).
When supervisor notification is activated, an automatic email notification is generated and sent to a group email address for supervisors. The email would summarize the problem and identify the location.
Email notification message showing operator code, RF program, type of override and location
This allows the supervisor to go the location causing the problem and approve or reject the override in the usual manner. It eliminates the need for the RF operator to leave his or her current location in search of a supervisor to have the issue resolved.
Set Default Values in RF 
Pallet Screen
Yes
No
If you set this flag to Yes, the RF operator will see default values for the account code, account type and transaction type fields in the Pallet Entry screen for RFPIC, RFPK, RFVP, RFCH and RFPU. 
The default account code will be the customer for the order/receipt and the default account type will be the customer. For inbound receiving, the default transaction type will be R for Receiving; for outbound shipping, the default transaction type will be S for Shipping.
If you set this flag to No, the account code, account type and transaction type fields will be blank when the RF operator first accesses the Pallet Entry screen.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

The following actions trigger an automatic email notification and the creation of an override record in RFSUN:
▪ a non-supervisory RF operator creates a new receipt line in RFCH
▪ a non-supervisory RF operator overrides a suggested put-away location in RFPU 
▪ a non-supervisory RF operator records a variance for the put-away quantity in RFPU
▪ a non-supervisory RF operator places product on suspend hold in RFPIC
▪ a non-supervisory RF operator enters a countback quantity in RFPIC that does not match the system quantity
▪ a non-supervisory RF operator enters a loading quantity in OLOP that does not match the system quantity
▪ a non-supervisory RF operator places product on hold in RFRL
There are three setup programs for supervisor notification: COMP (Company Code), WARE (Warehouse and 
Location Format) and MRFP (RF Profile).
In the Supervisor Notification Group Email Address field in COMP, you enter the default group email address for supervisor notification.
Supervisor goes to the location, logs in to the appropriate program and approves the override (existing logic). 
email
RFSUN
Email message containing a description of the problem and the location where it occurred is created and sent to group email address for supervisors.
Override record is created in RFSUN. 
RFCH/
RFPU, etc.
RFCH/
RFPU, etc.
Non-supervisory RF operator encounters a supervisor override event (new receipt line in 
RFCH, override of suggested put-away location in RFPU, etc.).
RFSUN
At a later time, supervisor reviews the override records and individually approves them. Approved override records no longer appear in RFSUN.

COMP screen showing field
In the Supervisor Notification Group Email Address field in WARE, you enter the group email address for a specific warehouse. If this field is populated with a valid email address, it will override the group email address at the company level.

WARE screen showing field
In MRFP supervisor approval must be activated for creating new receipt lines in RFCH, changing a suggested put-away location in RFPU, placing product on suspend hold in RFPIC, etc.
RFSUN allows supervisors to look up and accept overrides from the following programs: RFCH, RFPU, 
RFPIC, OLOP and RFRL. When an override is accepted in RFSUN, it is deleted and can no longer be accessed.

## Cartonization <a id="cartonization"></a>

*Manual H — RF Guide*

### Overview <a id="overview"></a>

There are four cartonization options in AccellosOne 3PL:
▪ manual cartonization in RFSC
▪ system-directed or first level cartonization in RFPK (also known as “Pick & Pack”)
▪ second level cartonization for product that cannot be cartonized in RFPK
▪ manual packing in EPSD

### Cartonization Tab (MRFP) <a id="cartonization-tab-mrfp"></a>

On this tab, you configure your cartonization options.
Cartonization tab

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
System-Driven Cartonization
Keep items together as much as possible
Pick in Location Sequence
Pick in Location Sequence, do not split order lines
Pick in Wine Sequence (custom use only)
Cartons for one item all one pallet
Your picking path mode for the BATP and LABL pick methods in RFPK. See [Task Profile (REGI)](expedicao-rf.html#task-profile-regi) for a complete descriptions of picking path modes.
Cartonization Sort 
Sequence Code (SOSE)
The sort sequence or “snaking” of your pick locations for cartonization.
Validate Inventory Level in RFPK Cartonization
Validate Item Only
Validate Item and Level 2
The inventory level(s) that must be validated in RFPK.
Picking Style in RFPK 
Pick by Carton ID
Pick by Carton Position
If you select “Pick by Carton ID”, the RF operator will scan in the carton ID as a confirmation step in RFPK. If you select “Pick by Carton Position”, the RF operator will scan in the carton position on a cart or trolley as a confirmation step in RFPK.

### Carton Size Setup (CTSZ) <a id="carton-size-setup-ctsz"></a>

In this program, you set up your carton size codes. Carton size codes are attached to customer/carrier/ consignee combinations in CCCC. For each carton size code, you define the following:
▪ a carton size code and description
▪ whether or not the carton’s dimensions/weight are inherited from the item’s dimensions and weight
▪ if required, the linear measure code and the length/width and height
▪ if required, the weight measure code, the maximum weight and the weight of an empty carton
▪ the usable percentage of the cube
RFSC Carton Sorted by Sorted by Item
Sorted by Item/Level 2
Sorted by Item/Level 3
If you select “Sorted by Item”, the RF operator must scan in the item code in 
RFSC. If you select “Sorted by Item/Level 2”, the RF operator must scan in the item code plus level 2 value in RFSC. If you select “Sorted by Item/Level 3”, the RF operator must scan in the item code plus level 3 value in RFSC.
FIELD DESCRIPTIONS
Carton Size Code Mandatory
Your carton size code.
Description Mandatory
A description for your carton size code.
Utilize Standard ConfigurationIf you select this option, the carton dimensions/weight are inherited from the item’s dimensions/weight in ITEM. If you do not select this option, you must enter the carton’s dimensions/weight manually.
Linear Measure Code Only available if Utilize Standard Configuration is not selected
Your linear measure code for the carton size code.
FIELD DESCRIPTIONS (CARTONIZATION)

Length / Width / Height Only available if Utilize Standard Configuration is not selected
The length, width and height of your carton size code.
Total Cube Only available if Utilize Standard Configuration is not selected
The carton’s actual cube calculated by multiplying the carton’s length, width and height.
Carton Size Cube Only available if Utilize Standard Configuration is not selected
In this field, you can define an override cube for a carton. For example, suppose carton A has dimensions of 24 x 16 x 5 for a total of 1920 cubic inches. If you define an override cube of 2500, you can place any number of items whose total cube does not exceed 2500 cubic inches in this carton size.
Weight Measure Code Only available if Utilize Standard Configuration is not selected
Your weight measure code for the carton size code.
Maximum Weight Only available if Utilize Standard Configuration is not selected
The maximum weight allowed in the carton.
Weight of Empty Carton Only available if Utilize Standard Configuration is not selected
The tare weight or weight of an empty carton.
SKU Class (SKCL) Only available if Utilize Standard Configuration is selected
The SKU class that the standard configuration applies to.
Usable Percentage The usable percentage of the cube. The non-usable percentage is reserved for packing materials.
Variable Dimensions If you select this option, the user will be prompted to enter the carton dimension in EPSD.
FIELD DESCRIPTIONS

CTSZ screen

### Outbound Process Configuration (CCCC) <a id="outbound-process-configuration-cccc"></a>

In this program, you set up your cartonization rules for different customer/carrier/consignee combinations. 
UCC-128 Package Type Carton
Pallet
The UCC-128 package type.
FIELD DESCRIPTIONS

FIELD DESCRIPTIONS
Customer Code The customer that the outbound process configuration applies to or.ALL for all customers.
Carrier Code The carrier that the outbound process configuration applies to or.ALL for all carriers.
Consignee Code The consignee that the outbound process configuration applies to or.ALL for all consignees.
Follow System Cartonization at PackingReserved for future use.
Maximum Cube/Weight In these fields, you specify the maximum cube and weight for second level cartonization. Second-level cartonization applies to product that cannot be cartonized by the cartonization engine because it is oversized, has no ICNP profile attached to it or has missing dimensions in ITEM.
Default Carton Size Code (CTSZ)
Your default carton size code in RFSC and second level cartonization.
Cartonization Sort Rules Give Priority to Carton Size Cube
Give Priority to Carton Size Dimensions
If you select Give Priority to Carton Size Cube, the cube will be considered first then the weight for second level cartonization. If, on the other hand, you select Give Priority to Carton Size Dimensions, the weight will be considered first then the cube.

CCCC screen
Cartonization Break by 
Zone Type Code
Only available for first level cartonization in RFPK
Location Grouping
Material Handling Type Groups
Pickup and Delivery Groupings
Voice
In this field, you specify which zone type (if any) AccellosOne 3PL should look at when comparing warehouse zones codes for the purposes of determining the next pick location. 
Suppose two adjacent locations — location A and location B — are both attached to the following three zone types: Interleaving, PnD and Grouping. If you select Pick and Delivery Groupings as your Cartonization Break by Zone 
Code value, the system will compare location A’s PnD warehouse zone code to location B’s warehouse zone code. If there is a match, the picker can pick from A and then B. If there is no match, the picker can pick from A but not B.
FIELD DESCRIPTIONS

### CARTON SIZE CODE BLOCK <a id="carton-size-code-block"></a>

In this block, you define which carton size codes are valid for different customer/carrier/consignee combinations.

### Packing Station Code (PKST) <a id="packing-station-code-pkst"></a>

In this program, you set up your packing stations. Packing stations are only required for manual packing in 
EPSD. For each packing station, you define:
▪ a packing station code and description
▪ a material handling equipment code
▪ the labels that will be printed at the packing station and the printers that they will be printed on
FIELD DESCRIPTIONS
Packing Station Code Mandatory
Your packing station code. 

In the Documents Block, you assign your labels to packing station printers.
Description Mandatory
The description for your packing station code.
MHE Code (MHEC) Mandatory
Your material handling equipment code for the packing station. The material handling equipment code that you enter must be attached to a material handling equipment type whose Location Required flag has been set to Y for Yes because packing stations require a warehouse code and location code.
The location attached to the material handling equipment code in MHEC must be a staging location.
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

Documents Block showing printer code for shipping label

### Item Cartonization Profile Code (ICNP) <a id="item-cartonization-profile-code-icnp"></a>

In this program, you set up your item cartonization profile codes. Each profile code defines the factor to be applied to a given set of items. For example, for your standard weight items, you set the factor to 1 for your 
STD code in ICNP and attach STD to all standard weight items in ITEM. As for your non-standard weight items, for each weight or cube category such as 1.15, 1.25, 1.35 times the standard weight or cube, you attach the appropriate factor to a profile code.
For example, a fragile item like a teapot requiring a lot of extra packing materials might have a cube factor of.85 meaning that 15% of each carton would be reserved for packing materials. On the other hand, a “squishy” item like a stuffed animal might have a cube factor 1.25 meaning that a carton designed to hold four stuffed animals could in fact hold five.
Item Cartonization Profile Codes are only required for system-driven cartonization in RFPK.
FIELD DESCRIPTIONS
Include Case Pick 
Method
When this field is not checked, cartonization will only be activated for EACH picks. When this field is checked, cartonization will be activated for both CASE and EACH picks.

ICNP screen showing factors for standard weight and cube as well as factors for deviations from the standard weight and cube
After setting up your item cartonization profile codes in ICNP, you attach them to the appropriate items in 
ITEM.
ITEM screen showing cartonization profile code

### Consignees (CONS) <a id="consignees-cons"></a>

You can deactivate system-directed cartonization for individual consignees by setting the Skip Cartonization 
Flag in CONS to Y for Yes.
CONS screen showing Skip Cartonization Flag set to Y for Yes

### Performing Manual Cartonization in RFSC <a id="performing-manual-cartonization-in-rfsc"></a>

You perform manual cartonization in the program RFSC (RF Sort Carton). With manual cartonization, you sort the product on an outbound order and manually assign a carton ID to the inventory in the carton. The carton 
ID’s that you manually assign are not validated by AccellosOne 3PL.
A carton is restricted to product from a single order only.
FIELD DESCRIPTIONS
RFPIC The order must be case picked and assigned an outbound pallet ID in RFPIC/
RFPK.

1 Enter RFSC.
RFSC screen
2 Key in your order number and press Enter.
LABELS You need a carton label set up in DOCU and this label must be attached to the appropriate customers and consignees in CCDU (Customer / Consignee Document Setup).
PARCEL PROCESSING Closing a carton in RFSC can trigger a special parcel processing process.
CARTON SIZES Carton sizes must be set up in CTSZ (Carton Size Setup). However, there is no validation of your carton sizes in CTSZ to ensure that the total weight or cube has been exceeded. 
FUNCTION KEYS
Results Mode
F1 RM (Remove) Removes product from a carton.
F2 QR (Query) Displays the first unpicked order line of the current order being processed.
F3 CL (Close) Closes a carton.
F4 EX (Exit) Exits program.
FIELD DESCRIPTIONS

RFSC screen showing carton size prompt
3 Press Enter to accept the default carton size or key in a new carton size and press Enter.
4 Enter or scan in your carton ID.
RFSC screen showing item prompt
5 Enter or scan in your item code or UPC code.
6 If required, enter or scan in your level 2 or 3 value.

RFSC screen showing quantity prompt
7 Key in the quantity of product that you wish to place in the carton and press Enter.
8 If the quantity that you entered completes the order, the “Order completed” message will appear. Press 
Enter to acknowledge it.
RFSC screen showing RM, CL and RT commands remaining number of units of this item on this order to be sorted/packed

9 Do one of the following:
10 When you finish manual cartonization in RFSC, press F4 (RT) and F4 (EX) to exit.

### WORKING WITH CLOSED CARTONS <a id="working-with-closed-cartons"></a>

When a carton is closed, you have three options: you can re-open the carton to make adjustments to it, you can delete the carton or you can enter a new carton.
1 When you enter or scan in the carton ID of a closed carton, the following message will appear:
If you wish to close the carton:
If you wish to remove the product from the carton:
If you wish to leave the carton open and work on another carton:
a) Press F3 (CL). a) Press F1 (RM).
b) Key in Y to continue with the removal and press Enter.
c) Enter or scan in your item to be removed.
d) When the removal confirmation message appears, press 
Enter to accept it.
a) Press F4 (RT).
b) Key in your order number and press Enter.

RFSC screen showing options for closed carton
2 Do one of the following:

### Performing System-Driven Cartonization in RFPK <a id="performing-system-driven-cartonization-in-rfpk"></a>

You perform system-driven cartonization in the program RFPK (RF Wave Pick). With system-driven cartonization, you scan in your carton ID’s first and then pick the product to be placed in these newly scanned cartons.
During allocation in Wave Manager, AccellosOne 3PL performs the following tasks:
▪ calculates the number and size of cartons required for each order in the wave based on the item dimensions and your carton sizes in CTSZ
▪ generates a unique UCC-128 number or carton ID for each carton
In RFPK, you scan in your carton ID and slot number for each carton and then scan in the level 1/2 values of the product that you are packing in the carton.
To re-open the carton: To delete the carton: To enter a new carton:
a) Key in 1 and press Enter.
b) Proceed to add new product to the carton or removing existing product from the carton.
a) Key in 2 and press Enter.
b) Enter or scan in a new carton 
ID or press F4 twice to exit 
RFSC.
a) Key in 3 and press Enter.
b) Enter or scan in a new carton 
ID and continue processing in 
RFSC.

Pick & Pack trolley
REQUIREMENTS
QUANTITY BREAKDOWNOnly items with a quantity breakdown of pallet/case/each can be cartonized.
LABELS You need a carton label set up in DOCU and this label must be attached to the appropriate customers/carriers/consignees in CCDU (Customer / Consignee 
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

1 Enter RFPK.
2 Key in your wave number and press Enter.
3 If prompted to do so, key in your material equipment type code and press Enter.
RFPK screen showing prompt for pick method
4 Key in 6 (Carton Pick) and press Enter.
FUNCTION KEYS
Results Mode
F1 RM (Remove) Deletes a scanned in carton ID/slot.
F2 QR (Query) Displays the first unpicked order line of the current order being processed.
F3 SP (Start Picking) Prompts you to start picking.
F3 SK (Skip) Skips the current pick.
F3 SQ (Short Quantity) Moves cursor to the QTYP field.
F4 EX (Exit) Exits program.

RFPK screen showing prompt for carton ID
5 Key in or scan in your carton ID.
RFPK screen showing prompt for slot number
6 Key in or scan in your slot number.
RFPK screen showing prompt for carton ID

7 Do one of the following:
8 Repeat the above steps for each additional carton ID/slot that you wish to add to your trolley.
9 When you have added all your carton ID’s/slots and are ready to pick, use your arrow keys to position your cursor over the carton ID that you wish to pack and F3 (SP) to start picking.
RFPK screen showing prompt for level 1
10 Do one of the following:
11 Key in or scan in your level 1 value.
12 If prompted to do so, key in or scan in your level 2 value.
If your carton ID and slot number are correct:
If your carton ID or slot number is incorrect and you wish to rescan:
a) Proceed to next step. a) Use your arrow keys to position your cursor over the carton ID that you wish to delete.
b) Press F2 (RM).
c) Re-enter or rescan your carton 
ID and slot.
To select the current pick:
To skip the current pick and display your next pick:
a) Proceed to next step. a) Press F3 (SK).
b) Proceed to next step to pick this pick or press F3 (SK) to advance to the following pick.

RFPK screen showing prompt for quantity
13 Key in your quantity and press Enter.
RFPK screen showing prompt for carton ID/slot number
14 If the quantity that you enter is less than the pick quantity, the following screen will appear:
RFPK screen showing “Short Pick” message

15 Key in 1 and press Enter to accept the short pick or key in 3 and press Enter to re-enter the full quantity.
16 Do one of the following:
RFPK screen showing prompt for staging location
17 Key in or scan in your staging location.
RFPK screen showing “Move Completed” message
18 Press Enter to acknowledge the “Move Completed” message.
19 If you picked all orders on the wave, press Enter to acknowledge the “All Orders Completed” message. 
Then press F4 to exit.
If you did not pick the entire wave, the following screen will appear:
If your picking style is set to “Pick by Carton ID”:
If your picking style is set to “Pick by Carton Position”:
a) Key in or scan in your carton ID a second time to confirm the pick and pack.
a) Key in or scan in your slot number a second time to confirm the pick and pack.

RFPK screen showing “Wave Not Completed” message
20 Do one of the following:

### Performing Second Level Cartonization <a id="performing-second-level-cartonization"></a>

Second-level cartonization applies to product that cannot be cartonized by the cartonization engine because it is oversized, has no ICNP profile attached to it or has missing dimensions in ITEM. 
You pick the order normally in RFPK and then manually pack it using a special pick sheet. The pick sheet will assign system-generated carton ID’s to the product on the order based on the maximum weight and cube values that you define in CCCC (Outbound Process Configuration) for second-level cartonization.
If you wish to continue with the same wave:
If you wish to start a new wave: If you wish to exit the wave:
a) Key in 1 and press Enter.
b) Go to step 4.
a) Key in 2 and press Enter.
b) Key in your new wave number and press Enter.
a) Key in 3 and press Enter.

### Performing Manual Packing in EPSD <a id="performing-manual-packing-in-epsd"></a>

You perform manual packing in the program EPSD (Enter Packing Details). In this program, you can create your own carton ID’s or you can use system-generated carton ID’s based on the order number.
1 Enter EPSD.
REQUIREMENTS
RFPIC The order must be case picked and assigned an outbound pallet ID in RFPIC/
RFPK.
LABELS You need a carton label set up in DOCU and this label must be attached to the appropriate customers/carriers/consignees in CCDU (Customer / Consignee 
Document Setup).
PARCEL PROCESSING Closing a carton in EPSD will trigger a special parcel processing process.
CARTON SIZES Carton sizes must be set up in CTSZ (Carton Size Setup). 
PACKING STATION Packing stations are required in PKST.
AUTO-CONFIRMATION EPSD can be configured to automatically confirm order lines upon successful completion of packing. Contact HighJump for assistance.
PICK METHOD Pick method in LOOR = PKST.
FULL CASE QUANTITIESInstead of scanning a case label for each full case, you can simply scan the item and enter the total number of cases. Weights and dimensions are automatically pulled from the item master and AccellosOne 3PL prints the required number of shipping labels.
Processing full case quantities requires special setup by HighJump.
OTHER Many options in EPSD are not configurable by end-users. Contact HighJump for further information on these options.

EPSD screen
2 Key in your packing station code and press Enter or select it from the pick list.
3 Do one of the following:
If you are packing product from a full pallet picked in Normal mode:
If you are repacking product from a pallet with an OPID (outbound pallet ID):
a) Key in your order number and press Enter.
a) Key in your OPID and press 
Enter.

EPSD screen showing prompt for carton ID
4 Key in your carton ID and press Enter or click on Carton ID based on Order for a system-generated carton ID.
5 Scan in your item code.
6 If required, scan in your level 2 value.

EPSD screen showing prompt for pack quantity
7 Key in your pack quantity and press Enter.
8 Repeat the above two/three steps for each additional item that you wish to pack.
9 If you wish to look up order carton details, click on Order Carton Details . When you finish looking up your order carton details, click on Return to exit.

EPSD screen showing Order Carton Details
If the Confirmed flag is selected, it means that the order line has been confirmed.
10 If you wish to look up your carton details, click on Carton Details . When you finish looking up your carton details, click on Return to exit.
EPSD screen showing Carton Details
11 When you are ready to close your carton, click on Close Carton .
12 Key in your carton size code and press Enter or select it from the pick list.

EPSD screen showing prompt for length
13 If prompted to do so, enter the carton’s dimensions.
14 If required, enter or make a manual adjustment to the total carton weight.
15 Key in your label printer code and press Enter or select it from the pick list.
16 When the Enter Packing Details window appears showing that your label is printing, press Enter to acknowledge it.
17 Click on Exit to exit.

### TRACKING YOUR PROGRESS IN EPSD <a id="tracking-your-progress-in-epsd"></a>

The following fields allow you to track your progress in EPSD to find out what percentage of an order has been packed and what percentage of an order remains to be packed.

EPSD screen showing tracking fields

### DELETING A CARTON’S CONTENTS <a id="deleting-a-carton-s-contents"></a>

If a carton is not closed, you can delete the carton’s contents and re-use the carton for other product.
1 Enter EPSD.
2 Key in your packing station code and press Enter.
3 Key in your order number or OPID number and press Enter.
4 Key in the carton ID of the carton that you wish to delete and press Enter.
5 Click on Delete .
6 Click on Yes when prompted to confirm your deletion.

### WORKING WITH UNCLOSED CARTONS <a id="working-with-unclosed-cartons"></a>

Unclosed cartons remain in EPSD until you either close the carton or delete the carton’s contents.
FIELD DESCRIPTIONS
Units to Repack Only available if you are repacking a pallet with an OPID
The remaining number of units on the current order to be repacked.
Cartons Packed The total number of cartons on the current order that have been packed.
Units Packed The total number of units on the current order that have been packed.
Units to Pick The remaining number of units on the current order to be picked.
Cartons to Pick The remaining number of cartons on the current order to be picked.

### Looking Up Cartons in LOCN <a id="looking-up-cartons-in-locn"></a>

You can look up cartons in LOCN to find out which orders shipped in which cartons. The Header Block shows the carton ID, order number, the carrier tracking number (if any), the carton size code, UCC number and status.
The Detail Block shows the customer code, item code, order number, line number and current flow. If the checkbox after the Flow field is selected, the order line has been fully picked.
If you perform an extended query, you can search for carton information by customer code and item code.
1 Enter LOCN.
LOCN screen
2 Press Enter until your cursor is positioned in the field that you wish to query. Then key in your search criteria and click on Execute Query.

LOCN screen showing carton for order 3072
3 If you wish to query by customer code or item code, click on Extended Query.
Extended Query screen
4 Key in or select your customer/item code and click on Execute Query.
5 When you finish looking up your carton information, click on Exit to exit.

### Deleting Closed Cartons in DCAR <a id="deleting-closed-cartons-in-dcar"></a>

If you are a desktop user, you can delete a closed carton in the program DCAR. When you delete a closed carton, you can choose to reduce the order line quantity accordingly (the carton did not ship) or you can leave the order line quantity unchanged (the original carton was damaged and had to be replaced).
1 Enter DCAR.
2 Key in your order number and press Enter.
DCAR screen showing cartons for order 2096
3 If required, click on the Reduce Order Line Quantity checkbox to deselect it.
4 In the Detail Block, click on Delete Carton for each carton that you wish to delete. Alternatively, you can click on Select All or Deselect All to select/deselect all cartons.
5 When you finish selecting your cartons, click on Process .
6 Click on Exit twice to exit.
