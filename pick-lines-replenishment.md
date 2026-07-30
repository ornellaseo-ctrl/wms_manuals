---
title: "Pick Lines, Replenishment, Wave Manager e Directed Moves"
description: "Linhas de picking, reabastecimento, gestão de waves e movimentações dirigidas."
layout: default
---

# Pick Lines, Replenishment, Wave Manager e Directed Moves

Linhas de picking, reabastecimento, gestão de waves e movimentações dirigidas.

**Fluxo principal:** `Pick line -> RFRP/TURE (replenish) | DOWA/PIIT (wave) | DMPA/DMPR (directed move)`

> Fonte: manuais K do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Pick Lines And Replenishment <a id="pick-lines-and-replenishment"></a>

*Manual K — Allocation and Wave Manager*

### Overview <a id="overview"></a>

A pick line is a special area within a warehouse used to store fast moving product in smaller than pallet-sized units for quick picking. Before you can pick from a pick line in AccellosOne 3PL, the following conditions must be met:
 you must set up and activate a pick line for the item that you wish to pick
 the order quantity must be a partial 
You can set up your system to perform replenishment automatically or you can manually replenish your pick line through a product relocation. If you activate automatic replenishment, the system will generate one or more replenishments whenever the quantity in the pick line falls below the minimum quantity for the location that you specify. Replenishment occurs during order allocation and is governed by the replenishment parameters that you define in PIIT (Pick Line Item Assignment) and ILOP (Replenish from Bulk).
You must confirm your replenishments in REPI (Relocate to Pick Line) or through an RF replenishment program.
The following examples show four scenarios: a pick from bulk rather than the pick line, a pick from the pick line with no replenishment, a pick from the pick line with a case replenishment and a pick from the pick line with a pallet replenishment.
Order quantity = 120 CS
EXAMPLE 1 — NO PICK LINE PICKING
Quantity breakdown of item: 100 CS/PALLET
Order quantity: 120 CS (1.2 PALLETS)
pick line system picks 120 CS from bulk rather than pick line because order quantity is not a partial bulk area no activity in pick line

There is a maximum of five steps to follow in picking from and replenishing a pick line:
EXAMPLE 2 — PICK LINE PICKING WITHOUT REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 50 CS
Minimum pick line quantity: 20 CS
Order quantity = 10 CS system picks 10 CS from pick line; no replenishment occurs because remaining quantity is greater than minimum (50 - 10 = 40, which is greater than minimum)
pick line bulk area
EXAMPLE 3 — PICK LINE PICKING WITH CASE REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 25 CS
Minimum pick line quantity: 20 CS
Replenish to quantity: 100 CS system picks 10 CS from pick line pick line
Order quantity = 10 CS replenishment is required because 25 -10 = 15 and 15 is less than minimum quanity;
system replenishes 85 CS from bulk (100 - 15)
bulk area
EXAMPLE 4 — PICK LINE PICKING WITH PALLET REPLENISHMENT
Order quantity: 10 CS
Available in pick line: 25 CS
Minimum pick line quantity: 20 CS
Replenish to quantity: 1 PLT system picks 10 CS from pick line pick line
Order quantity = 10 CS replenishment is required because 25 -10 = 15 and 15 is less than minimum quanity;
system replenishes 1 PLT from bulk bulk area

### TYPES OF PICK LINES <a id="types-of-pick-lines"></a>

AccellosOne 3PL supports two kinds of pick lines: fixed position pick lines and floating pick lines. A fixed position pick line is a pick line in which each item is assigned a fixed location. A floating pick line is a pick line in which the items on it are not assigned fixed locations. Any pick line location can contain any pick line item.

### WORKING WITH MULTIPLE PICK LINE LOCATIONS FOR THE SAME PRODUCT <a id="working-with-multiple-pick-line-locations-for-the-same-product"></a>

Multiple pick line locations (either fixed position or floating) for the same item is not recommended for product that falls within the same FIFO/LIFO range or product in which FIFO/LIFO picking is deactivated for the pick line (that is, allocation will pick the oldest product in the pick line even if there is older product in bulk). In 
ENOR
PROM/ 
PROR
RPAU
REPI
CHOF/
COOL
When you print your order documents in PROM or PROR, the system assigns locations to each order line. If the quantity in a pick line location falls below the minimum quantity, the system orders a replenishment and updates the quantity in the replenish from location.
You enter your P-type order lines in 
ENOR (not required if your orders are generated through EDI). 
If the picker performs replenishment, a message such as "Pick 1 pallet from bulk location X" will print on the pick sheet.*
If the picker does not perform replenishment, you can print RPAU (Relocate Pick Line Audit Report). This report, which generates an audit number, shows all your replenishments.*
* Printing the pick sheet and RPAU are optional in 
an all-RF environment.
You confirm your replenishments in 
REPI (Relocate to Pick Line) or RFRP (RF Replenish). AccellosOne 3PL updates the quantity in the replenish to location.
You confirm your orders in CHOF or 
COOL.
Picker does 
No replenishment Yes

these scenarios, allocation will tend to pick from and replenish to the first location only (“first” meaning first in location code sequence) and ignore the other pick line locations for the product.
For example, suppose you have three pick line locations for item A and each location contains product with a date code of November 1. Allocation will pick from the first location until the quantity falls below the minimum quantity; at that point, it will order a replenishment. 
No more pick line picking can take place from the first location until the replenishment is performed even though there is available and eligible product in the second and third locations. Only when all November 1 product in bulk has been moved to the first pick line location and picked from that location will allocation pick from the second and third pick line locations.
You can avoid the allocation problems that arise from multiple pick locations for the same product by defining one “super” location for the three slot positions on your pick line and activating picking substitution in PSPR (RF Substitution Profile Code). 

### Setting Up a Fixed Position Pick Line <a id="setting-up-a-fixed-position-pick-line"></a>

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

### 1 — SETTING THE ACTIVATE DIRECTED MOVE STOCK FLAG IN COMP <a id="1-setting-the-activate-directed-move-stock-flag-in-comp"></a>

The Activate Directed Move Stock flag must be set to Yes.

COMP screen showing Activate Directed Move Stock flag

### 2 — SETTING THE ASSIGN LOCATION FLAG IN DIFP <a id="2-setting-the-assign-location-flag-in-difp"></a>

In the DIFP record attached to the customer whose items you wish to pick from the pick line, make sure that the Assign Location flag has been set to Yes for at least one outbound flow code.

Depositor Workflow Profile (DIFP)

### 3 — SETTING UP YOUR PICKING PROFILE IN PIPR <a id="3-setting-up-your-picking-profile-in-pipr"></a>

In the PIPR record attached to the customer whose items you wish to pick from the pick line, there are five flags to be set:

 Break Quantity at SKU Class
 Use FIFO/LIFO for Pick Line Picking or Skip
 Exclude Pick Line Stock When Bulk Picking
 Replenishment Message on Pick Documents
 Break at SKU Class for Replenishment
FIELD DESCRIPTIONS
Break Quantity at SKU 
Class
Make sure that the Break Quantity at SKU Class field has been set to the appropriate value. For example, if your quantity breakdown is PALLETS/
CASES and you have two SKU classes (1 = pallets, 3 = cases and the like), you must select the “Break at SKU Class 1” option in PIPR so that the system will pick CASES (the next smaller SKU class) from your pick line.
For multiple pick line locations for the same item in different SKU’s, you must break at two SKU classes — for example, “1,2” or “1,3”. 
If you select the “Ignore SKU classes” option, the allocation routine will not pick from your pick line.
Use FIFO/LIFO for Pick 
Line Picking or Skip
N = No
Y = Yes
S = Skip
In this field, you specify whether or not you want allocation to follow a strict 
FIFO/LIFO sequence when pick line picking.
If you set this flag to N for No, the allocation routine will completely ignore 
FIFO/LIFO requirements when picking from the pick line. In other words, any stock that is found in a pick line location is considered acceptable no matter what the FIFO/LIFO setting is. 
If you set this flag to Y for Yes, the allocation routine will pick product in the pick line according to your FIFO/LIFO requirements.That means that product inside or outside of the pick line are all being allocated under the same FIFO/
LIFO requirement.
If you set this flag to S for Skip, skip mode will be activated. In skip mode, automatic replenishment is deactivated and the picker can select any pick line inventory from any pick line location whose level 1 value matches the level 1 value of the order line. See the section “Picking Cases from a Pick Line in 
CASE” in the RF User’s Guide.

Exclude Pick Line Stock 
When Bulk Picking blank = No
N = No
Y = Yes
In this field, you specify how you want allocation to handle situations in which a few cases of the oldest product are in the pick line and the order quantity consists of one or more full pallets. 
EXAMPLE order quantity = 2 pallets oldest product = 3 cases in pick line
If you set this flag to N for No, the allocation routine will pick the three cases in the pick line first. Then it will generate a replenishment and pick the remaining quantity from that replenishment. 
If you set this flag to Y for Yes, AccellosOne 3PL will pick the full order quantity from bulk even though the oldest product is in the pick line.
Replenishment Message on Pick Documents
N = No
Y = Yes
If you set this field to N for No, a message such as “Pick 1 pallet from bulk location X” will print on the document. You use the No option when the picker performs replenishment of the pick line.
If you set this field to Y for Yes, a message such as “If product not there, see replenishment staff” will print on the pick document. You use the Yes option when someone other than the picker performs replenishment of the pick line. 
If you do not use the core pick document, replenishment messages require a custom document from HighJump.
Break at SKU Class for 
Replenishment
This field allows you to define a sequence of SKU classes for replenishment. 
For example, you can replenish partial pallets first followed by full pallets or you can replenish full pallets first followed by partial pallets. You can also specify a combination of SKU classes for replenishment in a particular sequence such as Break at SKU Class 1, 2, 3.
If you leave this field blank, full pallets will be replenished first (assuming that the Replenish to SKU Code field in PIIT is set to PLT).
FIELD DESCRIPTIONS

Picking Profile (PIPR)
The picking profile that you define in PIPR can apply to all customers or to a particular customer. If required, it can apply to an item or series of items or it can apply to a consignee.
If you are attaching picking profiles to items and consignees as well to customers, the following logic will apply:
 the profile that you attach to DSRP is the default
 if you attach a picking profile to an item in ITEM, it will override the profile in DSRP
 if you attach a picking profile to a consignee in CONS, it will override the profiles in DSRP and ITEM

### 4 — SETTING UP YOUR REPLENISHMENT OPTIONS IN DSRP <a id="4-setting-up-your-replenishment-options-in-dsrp"></a>

If you use automatic replenishment, you must activate or deactivate replenishment optimization in DSRP. 
FIELD DESCRIPTIONS
Replenishment Optimizationblank = No
N = No
Y = Yes
In this field, you specify whether you want AccellosOne 3PL to pick directly from bulk when the replenishment quantity is less than or equal to the order quantity; that is, the replenishment quantity is fully allocated to a particular order/order line. It is recommended for customers that use absolute FIFO/
LIFO as an effective way of eliminating redundant replenishments.
NOTE Replenishment optimization is only available if the replenishment quantity is fully allocated to a particular order/order line at the time that the replenishment is generated. If you allocate line 1 of an order at 10:00 am and then allocate line 2 of the same order at 11:00 am and the replenishment quantity is fully allocated to the sum of the two order lines, no optimization will occur because the condition — replenishment quantity is fully allocated to an order — was not met at the time of the first replenishment.
If you set this field to N for No, AccellosOne 3PL will generate a replenishment from bulk to restore the pick line to its optimal quantity. Once the replenishment is confirmed, it will generate a pick from the pick line to fill the order line.
If you set this field to Y for Yes, AccellosOne 3PL will pick the replenishment quantity directly from bulk instead of replenishing the pick line and then picking it.
EXAMPLE
Quantity breakdown = 90 cases
Order quantity = 160 cases (one pallet and 70 cases)
Replenishment quantity = one pallet
Pick line location = A100 (50 cases) of oldest lot
Bulk location = BLK001 (120 cases) of the next newest lot

Depositor Shipping and Receiving Profile (DSRP)
Replenishment Optimization = N for No
Allocation will perform the following actions:
 pick 50 cases from the pick line location because this location contains the oldest product
 generate a replenishment of one pallet (90 cases) for the pick line 
 pick the full pallet of 90 cases from the pick line
 generate a second replenishment of 30 cases (the remaining product in location BLK001) for the pick line
 pick the balance of the order quantity (20 cases) from the pick line
Replenishment Optimization = Y for Yes
Allocation will perform the following actions:
 pick 50 cases from the pick line location because this location contains the oldest product
 pick one full pallet of 90 cases from bulk
 generate a replenishment of 30 cases (the remaining product in location 
BLK001) for the pick line
 pick the balance of the order quantity (20 cases) from the pick line
FIELD DESCRIPTIONS

### 5 — SETTING UP YOUR LOCATION TYPE IN LOTP <a id="5-setting-up-your-location-type-in-lotp"></a>

In the LOTP record attached to your pick line locations, make sure that the Directed Picking and Pick Line flags are both set to Y for Yes.

Location Type (LOTP)
6 — ASSIGNING YOUR LOCATION TYPE TO YOUR PICK LINE LOCATIONS IN 
LOCA
In this program, you attach the pick line location type that you set up in LOTP to your pick line locations in 
LOCA.

Locations (LOCA)

### 7 — DEFINING YOUR PICKING PARAMETERS FOR REPLENISHMENT IN ILOP <a id="7-defining-your-picking-parameters-for-replenishment-in-ilop"></a>

In this program, you define the picking parameters for your replenishments. You can have the system replenish product based on receipt date, isolator zone, quantity of product in the location and other criteria that you specify. 
The picking parameters for replenishments are defined in the Replenish from Bulk Block of ILOP. These parameters are identical to the picking parameters in the Picking Block of ILOP. If you do not define replenishment parameters in ILOP, the system will use the default parameters for picking. The default replenishment value is the first option in each group of your standard logical groups for picking. 
See [Setting Up the Item Location Profile for Picking (ILOP)](alocacao.html#setting-up-the-item-location-profile-for-picking-ilop) for complete information on the various replenishment options available. 
1 Enter ILOP.
2 Do one of the following:
If you are creating a new ILOP profile:
If you are attaching your replenishment parameters to an existing ILOP profile:
a) Key in an item location profile code and press Enter.
b) Key in a meaningful description for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to update.
b) Click on Type Block.
c) Proceed to step 5.

3 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
4 Use your pick list function to select any warehouse code for your overflow warehouse.
5 Use your pick list function to select any location code for your overflow location code.
6 Press your up or down arrow key in the Types Block until the Replenish from Bulk option is displayed.

Blank Replenishment screen
7 Proceed to enter your replenishment parameters. Refer to [Setting Up a New Profile in ILOP](alocacao.html#setting-up-a-new-profile-in-ilop) for instructions on how to assign parameters to sequences in ILOP.
8 When you finish entering all your sequences, click on Return to Main and then Type Block.
9 Click on Master Block and then Exit to exit the program.

### 8 — SETTING UP YOUR PICK LINE IN PIIT <a id="8-setting-up-your-pick-line-in-piit"></a>

You set up your pick lines in PIIT (Pick Line Item Assignment). In this program, the following parameters need to be defined:
 the location of the pick line (fixed or non-floating pick lines only)
 the item or items on the pick line
 the replenishment quantity
 the minimum quantity 
 the SKU code that you will be picking from the pick line
 the SKU code that you will be using to replenish the pick line
 whether replenishment occurs manually or automatically

You can have multiple items for multiple customers assigned to the same pick line location or you can set up one pick line location for each item/customer. As well, you can have multiple pick line locations for the same item; for example, you can have one pick line location for EACHES (item x) and another pick line location for 
CASES (item x). 
You need to set up one PIIT record for each unique combination of customer code, item code, warehouse/ location code and pick line SKU code. For example, if you wish to assign three items to the same pick line location, you would have to set up three PIIT records — one for each item.
You cannot change the customer code, item code, warehouse/location code or pick line SKU code of an existing PIIT record. If you wish to change any of these values, you must delete the record and then recreate it with the correct values.
NOTE Before changing or deleting a pick line location, you must delete or confirm any replenishments for that location.
FIELD DESCRIPTIONS
Customer Code Mandatory
The customer whose item(s) you wish to assign to a pick line.
Item Code Mandatory
The item that you wish to assign to a pick line.
Inventory Level 2 Optional
See [Setting Up a Pick Line With Replenishment by Inventory Level 2](pick-lines-replenishment.html#setting-up-a-pick-line-with-replenishment-by-inventory-level-2) for further information.
Warehouse Code Mandatory for fixed or non-floating pick lines
The warehouse in which the pick line is located.
Location Code Mandatory for fixed or non-floating pick lines
The pick line’s location. The location that you specify must be assigned a location type whose Pick Line flag has been set to Yes in LOTP (Location Types).

Use Floating Pick Line to 
Hold Demand REPI
Reserved for future use.
Pick Line SKU Code Mandatory
The SKU code of your pick line — that is, the SKU code that you will be picking from this pick line. The SKU codes that you can enter in this field depend upon the value you entered in the Break Quantity at SKU Class field in the 
PIPR (Picking Profile) record attached to this item; if no PIPR profile is attached to this item, the system will use the PIPR profile attached to the customer. 
If you are unable to enter the SKU code that you wish to pick from your pick line, return to PIPR and check that you have set up this profile correctly.
Replenish To Quantity Mandatory 
The optimal quantity allowed for the location. When the on-hand quantity in the location falls below the quantity that you specify in the Minimum Quantity field, the system will replenish whatever quantity is needed to restore the location to its optimal quantity — that is, the difference between the available quantity and the replenish to quantity.
For example, if you currently have 20 cases in your pick line and your replenish to quantity is 100 cases, the system will perform a replenishment of 80 cases.
If your replenish to SKU code is different from your pick line SKU code (for example, you pick cases from the pick line but replenish in pallets), then the system will round up to the nearest pallet and replenish that quantity.
CAUTION Do not set the replenish to quantity to the location’s maximum capacity as defined in LOCA (Locations). If you do, AccellosOne 3PL may appear to over-replenish the location. 
Replenish To SKU Code Mandatory 
The SKU code for the Replenish To Quantity field. This SKU code may differ from the SKU code in the Pick Line SKU Code field (for example, you can pick in CASES from the pick line but replenish in PALLETS).
FIELD DESCRIPTIONS

Minimum Quantity Mandatory 
If the available quantity in the pick line location falls below the minimum quantity that you specify in this field, the system will perform automatic replenishment. The number that you enter in this field is always in the SKU code that you specified in the Pick Line SKU Code field.
NOTE The minimum quantity must always be less than the replenish to quantity. If the minimum and replenish to quantities are expressed in different 
SKU codes (for example, your minimum is in CASES and your replenish to is in pallets), you must convert one of your quantities — pallets to cases or cases to pallets — to ensure that the replenish to quantity is greater than the minimum quantity.
Setting the Minimum Quantity to Zero
If you set the minimum quantity to zero and the Automatic Replenish to Pick 
Line flag to Y for Yes, no replenishment will take place when the available quantity in the pick line reaches zero unless a replenishment is required to fill a current order.
EXAMPLE 1
The quantity in the pick line is three cases and the order quantity is three cases. AccellosOne 3PL will pick three cases from the pick line but no replenishment will take place until another order requires a pick from the pick line.
EXAMPLE 2
The quantity in the pick line is three cases and the order quantity is four cases. 
AccellosOne 3PL will pick three cases from the pick line, perform a replenishment and them pick the remaining one case from the pick line.
CAUTION Automatic replenishment with a zero minimum quantity is only available for a single pick line location/item/SKU code combination. You cannot use this function with two or more pick line locations assigned the same item code and SKU code.
Critical Quantity in Pick 
Location
This field is used to establish a critical level of inventory in a pick line location requiring a high priority replenishment. The critical quantity can be either greater than or less than the minimum quantity.
If you specify a critical quantity and if the available quantity in the pick line location falls below the critical quantity, one of the following will occur:
 If you use system-assisted tasking, you can create an ActiveDesktop alert for the supervisor warning him or her of the situation.
 If you use system-driven tasking, the replenishment task will be re-assigned to a higher priority.
FIELD DESCRIPTIONS

Rounding Method for 
Replenish To Quantity
This field makes it possible to perform partial replenishments to a pick line location. Partial replenishments reduce the number of partial non-pick line locations and eliminate multiple replenishments for the same location. 
For example, suppose a given pick line location requires a 60-case replenishment. Depending on the option that you choose, AccellosOne 3PL will either increase the replenishment quantity to 65 or 70 cases to clean out a given location or reduce the replenishment quantity to 55 or 50 cases to clean out a given location.
There are four options in this field:
D for Down
Round down to the available quantity in a location and create a single REPI for each replenishment.
U for Up
Round up to the full available quantity in a location and create a single REPI for each replenishment.
R for Round Up or Down
Round up or down to the available quantity in a location and create a single 
REPI for each replenishment.
N for No Rounding
Pick the exact quantity required to make up the replenish to quantity and perform multiple replenishments if required.
Allow On-Demand 
Replenishment
N = No
Y = Yes
This field makes it possible to force AccellosOne 3PL to generate replenishments outside of normal order allocation processing. For example, your pick line is well stocked for the current day's orders and you wish to pick your orders first from the pick line and worry about replenishing your pick line on a later shift.
You activate on-demand replenishment by setting the Allow On-Demand 
Replenishment to Y for Yes. Then you write a background cron job in Unix to run according to a predefined schedule; depending on the command that you use, you can run replenishments for all customers of a given company, for a given customer of a given company or a specific item belonging to a specify customer.
You can also generate on-demand replenishments in TURE (Top Up Replenishments).
FIELD DESCRIPTIONS

1 Enter PIIT
Force Replenishment 
When Needed
Y = Yes
N = No
If you set this flag to Y for Yes, allocation will force a replenishment when the product on order cannot be picked from the pick line because of FIFO constraints and a replenishment cannot be generated because the pick line quantity is above the minimum. If you set this flag to N for No, allocation will generate a partial pick from bulk when the required product is not in the pick line. 
NOTE The Yes option (force a replenishment) must be used with extreme caution as it may cause over-crowding in your pick line.
Number of Days to Empty 
Out a Location if Not 
Used
Reserved for future use
Automatic Replenish to 
Pick Line
Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL will automatically generate a replenishment record for each pick line location whose quantity falls below the minimum quantity. You can either confirm or delete this record in REPI (Relocate to Pick Line). If you set this flag to N for No, automatic replenishment will not occur. You must manually replenish the pick line by means of RELO (Relocate Inventory).
Exclude Bulk When no 
Floating Locations Available
Reserved for future use
Release in Full Quantity Reserved for future use
FIELD DESCRIPTIONS

Pick Line Item Assignment
2 Click on Create Record.
3 Use your pick list (press F10 to enter the pick list, click on Execute Query then Select) to select the appropriate customer that you wish to attach to the pick line.
4 Use your pick list to select the item that you wish to attach to the pick line.
5 Press Enter to bypass the Inventory Level 2 field.
6 In the Pick Line SKU Code field, key in the SKU code that you will be picking from in this pick line and press Enter.
If you wish to set up a static pick line:
If you wish to set up a floating pick line:
a) Key in your warehouse code and press Enter
b) Use your pick list to select the appropriate location for your pick line.
c) If you are unable to access any locations for your pick line, make sure that you have assigned a location type to the location whose Pick Line flag has been set to Yes. You set up location types in LOTP (Maintain Location Types).
a) Press Enter to bypass the Warehouse Code and Location Code fields. Floating pick lines do not have defined locations in PIIT. 

7 In the Replenish to Quantity field, key in your “replenish to” quantity and press Enter.
8 In the Replenish To SKU Code field, key in the SKU code you want the system to use when it replenishes the pick line and press Enter.
9 In the Minimum Quantity field, key in the minimum quantity for this item and press Enter. Make sure that the minimum quantity is less than the “replenish to” quantity.
10 In the Rounding Method for Replenish to Quantity field, key in the appropriate value (D for Down, U for 
Up, R for Round Down or Up or N for No Rounding) and press Enter.
11 In the Allow On-Demand Replenishment field, key in N for No or Y for Yes and press Enter.
12 In the Force Replenishment When Needed field, key in N for No or Y for Yes and press Enter. 
13 Press Enter to bypass the Automatic Replenish to Pick Line field.
14 When you finish adding your pick line, click on Return to Main to exit create mode.

Pick Line Item Assignment (PIIT) screen showing a replenishment to quantity of 1 pallet when the quantity falls below 10 cases
15 Click on Exit to exit.

### 9 — ACTIVATING YOUR PICK LINE USING ENOR/REPI <a id="9-activating-your-pick-line-using-enor-repi"></a>

Pick line locations that are empty will not be replenished. To fill empty pick line locations with enough product to activate replenishments, follow the steps below:
1 Make sure that there is enough product in bulk to move to the pick line.
2 Create an order for one case of each item going into the pick line.
3 Allocate the order normally. AccellosOne 3PL will generate all the replenishments.
4 Perform your replenishments in REPI.

5 Delete the original order.

### Setting Up a Floating Pick Line <a id="setting-up-a-floating-pick-line"></a>

A floating pick line is a pick line in which the items on it are not assigned fixed locations. Any pick line location can contain any pick line item. You set up a floating pick line by creating a record in PIIT (Pick Line Item 
Assignment) with a customer code, item code, pick line SKU code, etc. but no warehouse code and location. 
Once you set up your PIIT pick line, any location in your warehouse whose location type in LOTP has the 
Directed Picking, Directed Put-Away and Pick Line flags set to Y for Yes is defined as a floating pick line.
In addition to the setup programs for fixed position pick lines, there are two additional steps for setting up a floating pick line:
 you define your put-away parameters in the Replenish to Floating Pick Line Block of ILOP (Item Location Profile)
 you define the way in which AccellosOne 3PL calculates the minimum quantity for a pick line location in 
PIPR (Picking Profile)
The put-away parameters for replenishing a floating pick line are defined in the Replenish to Floating Pick 
Line Block of ILOP. These parameters are identical to the put-away parameters in the Put-Away Block of 
ILOP. If you do not define replenishment parameters in ILOP, the system will use the default parameters for put-away.
Enter ILOP and select Replenish to Floating Pick Line as your type. Then refer to [Item Location Profile for 
Put-Away (ILOP)](alocacao.html#item-location-profile-for-put-away-ilop) for complete information on the various replenishment options available.
NOTE If you set up two or more pick line locations in PIIT for the same item and the same pick line SKU code, make sure that they both have inventory in them. If one of the locations is empty, the allocation routine will not replenish that location. To relocate inventory to an empty pick line, use RELO (Relocate Inventory) to move product from elsewhere in the warehouse.
NOTE Floating pick lines have two sets of replenishment parameters in ILOP. The 
Replenish from Bulk parameters define which locations in bulk you pick from in order to replenish the pick line. The Replenish to Floating Pick Line parameters define which pick line locations you put-away to when replenishing your floating pick line.

Item Location Profile Code (ILOP) screen showing Replenish to Floating Pick Line type
The way in which AccellosOne 3PL replenishes a floating pick line depends upon the value that you select in the Replenishment Based on Eligible Records field in PIPR (Picking Profile). If you set this flag to Y for Yes, 
AccellosOne 3PL will replenish a floating pick line location based on the minimum quantity of eligible records (for example, all inventory older than June 1). If you set this flag to N for No, AccellosOne 3PL will replenish a floating pick line location based on the minimum quantity of all inventory in the pick line.

Picking Profile (PIPR)

### Mixing Fixed Position and Floating Locations in the Same Pick Line <a id="mixing-fixed-position-and-floating-locations-in-the-same-pick-line"></a>

In order to mix floating and fixed position locations in the same pick line, you must set up at least two isolator codes for your warehouse: one for your floating locations and another (or a number of others) for your fixed locations.
1 Make sure that all your floating locations have the same isolator code and that this isolator code is not attached to any fixed position location or fixed position location item.
2 Set up your ILOP profile for your fixed position locations in the normal manner. In the Replenish From 
Bulk block, you can select any option that you wish from the Isolator group.
3 Set up a second ILOP profile for your floating locations. In the Replenish to Floating Pick Line block, select the “Use exact match isolator code” option from the Isolator group. You must use this option in each ILOP sequence in the Replenish to Floating Pick Line block.
If you do not attach the exact match parameter to your ILOP profile for floating locations, allocation could put-away floating location product to a fixed position location for a different product.
Replenishment Based on Eligible 
Records field

### Setting Up a Pick Line With Replenishment by Inventory Level 2 <a id="setting-up-a-pick-line-with-replenishment-by-inventory-level-2"></a>

Replenishment by inventory level allows you to define separate pick line locations for each level 1/level 2 combination in your warehouse. Each pick line location can be assigned a specific level 1/level 2 entity with its own minimum and replenishment quantities.
For example, suppose your level 1 value is Nike shoes and your level 2 value is shoe size and your minimum quantity is 25. If you deactivate replenishment by inventory level, AccellosOne 3PL will perform a replenishment whenever the quantity of a particular shoe regardless of size falls below the minimum quantity. The replenishment will consist of any size of that shoe.
If you activate replenishment by inventory level, AccellosOne 3PL will perform a replenishment whenever the quantity of a particular shoe and size falls below the minimum quantity. The replenishment will consist of the shoe and size whose quantity fell below the minimum quantity.
There are three requirements for pick lines with replenishment by inventory level 2:
 the Use FIFO/LIFO for Pick Line Picking flag in PIPR must be set to N for No
 the Replenish Pick Line up to Level flag in PIPR must be set to 2
 there must be one record in PIIT for each unique level 1/level 2 combination in your pick line
NOTE Replenishment by inventory level 2 is only available for fixed position pick lines. You cannot use this function with floating pick lines.
Replenish up to Level
Minimum 
Quantity in PIIT
Available Quantity in 
Pick Line Replenishment
1 25 size 8 (10 units), size 9 (10 units), size 10 (12 units)
No replenishment occurs because total quantity (10 + 10 + 12) is greater than the minimum quantity.
2 25 size 8 (10 units), size 9 (10 units), size 10 (12 units)
Replenishment takes place because the quantity for each size is less than the minimum quantity.

Picking Profile (PIPR)
CAUTION If you create a record in PIIT with the level 1 specified but no level 2 — for example, NIKE001 but no size — AccellosOne 3PL may generate unnecessary replenishments in REPI (Relocate to Pick Line).
Replenish 
Pick Line up to Level field set to 2

Pick Line Item Assignment (PIIT)

### ENTERING ORDERS IN ENOR <a id="entering-orders-in-enor"></a>

Replenishment by inventory level requires that you enter both level 1 and level 2 for each order line in ENOR. 
If you enter a single inventory level in ENOR, AccellosOne 3PL will use your item-level default in PIIT; that is, it will pick from the pick line and then replenish — if necessary — based on the minimum quantity defined for the item. The replenishment will consist of any level 2 value for that item — not necessarily the level 2 value on the order line that triggered the replenishment.
If there is no item-level default defined in PIIT, AccellosOne 3PL will pick orders from bulk and ignore the pick line.

### Putting Away to a Pick Line Using Directed Put-Away <a id="putting-away-to-a-pick-line-using-directed-put-away"></a>

You can put-away to a pick line using directed put-away by means of the program PUPR (Put-Away Profile 
Code). Putting away to a pick line works well in two cases: the pick line item has a single inventory level or the pick line item has multiple inventory levels but your picking is very relative — that is, your range in days value in PIPR is very high and there are a large number of eligible inventory records from which to pick. Putting away to a pick line is not recommended when you are picking absolute or when you are picking relative but the range of acceptable inventory records is very small. 
There are five setup programs for a pick line with directed put-away:
 You set the Directed Put-Away flag in LOTP to Yes for the location type attached to your pick line location
 You set up your put-away profile code in PUPR (Put-Away Profile Code). 
 You attach your PUPR profile to DSRP (Depositor Shipping & Receiving Profile). 
 You set up your overflow locations in PIIT (Pick Line Item Assignment). 
Inventory 
Level 2 must be defined

 You define your put-away rules in ILOP (Item Location Profile).

### 1 — SETTING UP YOUR LOCATION TYPE IN LOTP <a id="1-setting-up-your-location-type-in-lotp"></a>

Make sure that the Directed Put-Away, Directed Picking and Pick Line flags are all set to Yes for the pick line’s location type.

Location Type (LOTP)

### 2 — SETTING UP YOUR PUT-AWAY PROFILE CODE IN PUPR <a id="2-setting-up-your-put-away-profile-code-in-pupr"></a>

In PUPR you set up your directed put-away options for your pick line. There are two put-away options in this program:
 You can specify that product is to be always put away to the pick line or that only partial quantities are put away to the pick line. These options requires custom RF programming.
 You can specify an item receipt hold profile. You set up item receipt hold profiles in IRHP (Item Receipt 
Hold Profile). If you specify an item receipt hold profile, product with a hold attached to it will be put away to the location assigned to that hold in IRHP instead of to the pick line. 
PUPR is attached to DSRP (Depositor Shipping and Receiving Profile). If you attach a PUPR profile to ITEM, that profile will override the customer-level default in DSRP. For example, if you wish to put away to the pick line all product for a given customer with the exception of one item, you would create two PUPR profiles as follows: 
 you would set your first one to Always or Partial and attach it to your DSRP profile 
 you would set your second one to None and attach it to the item that you do not wish to put away to the pick line.

FIELD DESCRIPTIONS
Put-Away to Pick Line A = Always
P = Partial
N = None
If you select A for Always, the system will always attempt to put away to a pick line location. If you select P for Partial, the system will only attempt to put away partial quantities to the pick line. If you select N for None, the system will never attempt to put away to a pick line location and the item will be assigned a non-pick line location.
When you select either the Always and Partial options, the system will compare the size and weight of the item being received against the capacity and weight limitations of the pick line location and attempt to put away in a pick line location that satisfies your ILOP parameters. If the size or weight of the item exceeds the capacity of the pick line location, the system will attempt to put away to a pick line overflow location defined in PIIT.
If there are no pick line overflow locations or if the pick line overflow locations are full, the system will attempt to put away to a non-pick line location using your ILOP parameters.
Pick Line Isolator Code (ISOL)
Optional
The isolator code that you enter in this field applies only to your pick line and pick line overflow locations. It may differ from your ILOP isolator code that is attached to the item, which applies only to non-pick line locations.
If you enter an isolator code in this field, the following rules will apply:
 if putting away to non-pick line locations, the system will use the isolator code(s) for the ILOP profile attached to the item that you are putting away
 if putting away to pick line or pick line overflow locations and ILOP is set to “use only exact match isolator code,” the system will use your PUPR isolator code
 if putting away to pick line or pick line overflow locations and ILOP is set to “use any overflow isolator code,” the system will use your ISOL overflow isolator code 
If you do not enter an isolator code in this field, the system will use the isolator code(s) for the ILOP profile attached to the item that you are putting away.
Range in Days from Oldest LotSee [Put-Away Profile Code (PUPR)](alocacao.html#put-away-profile-code-pupr) for further information..

1 Enter PUPR.
2 Key in your put-away profile code and press Enter.
3 Key your put-away profile code description and press Enter.
4 In the Put-Away To Pick Line field, key in the appropriate value (A for Always, P for Partials or N for 
None) and press Enter.
5 In the Pick Line Isolator Code field, key in your isolator code and press Enter or press Enter with this field blank to bypass the option.
6 If required, enter your item receipt hold profile code and set the Item Receipt Hold Override flag to the appropriate value. If you do not require an item receipt hold profile code, press Enter to bypass this field.

Put-Away Profile Code (PUPR) screen showing a profile code for putting away partials only to the pick line
7 Click on Return to Main and Exit to exit.

### 3 — ATTACHING YOUR PUPR PROFILE TO DSRP <a id="3-attaching-your-pupr-profile-to-dsrp"></a>

In this program, you attach your PUPR profile to your Depositor Shipping & Receiving Profile (DSRP). The 
PUPR profile that you specify in a given DSRP profile will apply to all customers to which you have attached that DSRP profile. If you attach a PUPR profile to a given item in ITEM, that profile will override the customerlevel default in DSRP.
Range Based on See [Put-Away Profile Code (PUPR)](alocacao.html#put-away-profile-code-pupr) for further information..
FIELD DESCRIPTIONS

1 Enter DSRP.
2 Click on Enter Criteria and Execute Query to retrieve the profile that you wish to modify.
3 In the Put-Away Profile Code field, key in your put-away profile code and press Enter or use your pick list to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to display the list of codes. Then position your cursor over the appropriate code using your arrow keys and click on Select to select it. 

Depositor Shipping and Receiving Profile (DSRP) showing Put-Away Profile Code = P2
4 When you finish modifying your code, click on Return to Main and Exit to exit.

### 4 — SETTING UP YOUR OVERFLOW LOCATIONS IN PIIT (OPTIONAL) <a id="4-setting-up-your-overflow-locations-in-piit-optional"></a>

In PIIT, you can define overflow locations for a pick line into which you are putting away. If the pick line location is full, the system will attempt to put away inbound product to the first overflow location. If the first overflow location is full, the system will attempt to put away the product to the second overflow location (if any). If the second overflow location is full, the system will attempt to put away product to the third overflow location (if any). 
If all overflow locations are full or you do not specify any overflow locations, the product will be directed to normal ILOP processing.
Overflow locations must be defined as pick line locations.
1 Enter PIIT.
2 Click on Enter Criteria and Execute Query to retrieve the PIIT record that you wish to modify.

3 Click on Overflow Block.
4 Key in your first sequence number and press Enter.
5 Key in your warehouse code for your first overflow location and press Enter.
6 Key in the location code of your first overflow location and press Enter.
7 Repeat steps 4 to 6 for each additional overflow location.

Pick Line Item Assignment (PIIT) screen showing three overflow locations
8 When you finish adding all your overflow locations, click on Master Block and Exit to exit.

### 5 — DEFINING YOUR PUT-AWAY RULES IN ILOP <a id="5-defining-your-put-away-rules-in-ilop"></a>

You define your put-away rules in the PIIT Location Capacity group in ILOP. See “PIIT Location Capacity 
Group (I8500)” (ver [Standard Logical Groups for Put-Away](alocacao.html#standard-logical-groups-for-put-away)).

Item Location Profile screen showing PIIT Location Capacity group

### Performing Your Replenishments <a id="performing-your-replenishments"></a>

There are two steps to follow in performing a replenishment:
 you do one of the following: you run the Relocate Pick Line Audit Report (RPAU) or you use the pick document with the replenish from message
 you confirm the replenishment in either Relocate to Pick Line (REPI) or RFRP (RF Replenish) 

### RUNNING THE RELOCATE TO PICK LINE AUDIT (RPAU) <a id="running-the-relocate-to-pick-line-audit-rpau"></a>

Refer to the Standard Reports Guide. 
NOTE If the replenishment involves picking multiple inventory entities from a single location, AccellosOne 3PL will create one or more order lines with order and ship quantities of zero. These order lines are required to satisfy uniqueness constraints in the database and should be ignored. 

### CONFIRMING YOUR REPLENISHMENTS IN REPI <a id="confirming-your-replenishments-in-repi"></a>

You confirm your replenishments in REPI (Relocate to Pick Line). When you perform allocation through the printing of a shipping document or some other process, the system will generate a REPI screen or record for each replenishment with all fields (Order Number, From Warehouse Code, Relocate Units, etc.) fully filled in. 
If the replenishment involves picking one inventory entity from multiple locations or multiple inventory entities from a single location, a REPI screen will be generated for each unique location/entity combination. 
If required, you can manually override the “replenish from” locations in REPI. The system will then replenish from the location or locations that you specify rather from the system-selected location or locations.
1 Enter REPI.
2 Click on Execute Query. The system will retrieve a REPI record for each replenishment that met the criteria that you specified in the previous step. For example, if you have a single pick line location and the system replenishes it from two locations, you will have to two records in REPI — one for each “from” 
location.
CAUTION If you do not confirm your replenishments in REPI, the allocation routine will nevertheless assume that replenishment has taken place and the quantities in the “replenish from” locations will be adjusted accordingly. However, the “replenish to” locations — that is, the pick line — will not be replenished on the system. As a result, you may be unable to confirm an order if the system considers the pick line to be empty.
If you wish to confirm all your replenishments:
If you wish to restrict your confirmation to certain replenishments:
a) Proceed to next step. a) Press Enter to position your cursor in the field that you wish to restrict on. You can restrict on customer code, item code, level 
2, 3 and 4 values, order number, audit number*, from warehouse code/location and to warehouse code/location. 
b) Key in your restriction value; for example, your order number, customer code, etc.
c) If you wish to include a second field in your restriction, repeat the above two steps for your second value.
* Only available if you run RPAU (Relocate to Pick Line Audit Report).

Relocate to Pick Line (REPI) screen showing two replenishments
3 If you wish to manually override the “replenish from” location, press Enter to position your cursor in the 
From Location Code field. Then use your pick list (press F10 to enter the pick list, click on Execute Query to query and then Select) to select the appropriate from location code.
4 Click on Relocate Done.
5 Do one of the following:
6 When you finish confirming your replenishments, click on Exit to exit.

### LOOKING UP A REPLENISHMENT IN LOEN <a id="looking-up-a-replenishment-in-loen"></a>

Replenishments appear in the Replenishment column of the Location Block in LOEN. The replenish from quantity is shown as a positive quantity while the replenish to quantity is shown as a negative quantity. When you confirm your replenishments in REPI, all quantities in the Replenishment column revert to zero.
1 Enter LOEN.
2 Key in the customer code, item code and inventory levels of the product being moved to the pick list and click on Execute Query.
If reserve logic is activated on your system:
If reserve logic is NOT activated on your system:
a) Enter the missing inventory level(s) and click on Relocate 
Done.
a) Repeat the above step for each additional record in REPI that you wish to confirm.
a) Continue to click on Relocate 
Done for each record in REPI that you wish to confirm.

3 Click on Location Block.
4 If required, use your down arrow to scroll down in the Location Block.
5 Press Enter to display the Replenishment column.

Look Up Inventory (LOEN) screen showing a replenishment of 5 cases from FA001 to FA008
6 Continue to press Enter to scroll horizontally through the various columns in the Location Block.
7 When you finish looking up your replenishments, click on Inventory and Exit to exit.

### GENERATING TOP UP REPLENISHMENTS IN TURE <a id="generating-top-up-replenishments-in-ture"></a>

You can generate top up or on demand replenishments in TURE. Top up replenishments are governed by the replenishment rules set up in PIIT. They differ from regular replenishments in that they are not triggered by an order picking from a pick line location. If you run TURE and if the quantity in a pick line location is less than the minimum quantity, a replenishment will be generated.
On demand replenishment must be activated in PIIT (Pick Line Item Assignment) by setting the Allow On 
Demand Replenishment flag to Y for Yes.
1 Enter TURE.
2 Proceed to enter your top up restrictions. You can restrict top up replenishments to all product belonging to a specific customer or to a specific item.

TURE screen showing top up restrictions
3 If required, you can restrict your replenishments to a specific location. Key in your location code and press Enter. To restrict your replenishments to a range of locations, use one or more of the following operands:
4 Click on Process.

### DELETING A REPLENISHMENT <a id="deleting-a-replenishment"></a>

If you delete a replenishment in REPI, the system will remove the product from your pick line and restore it to its original location. However, the system will not undo the quantity that you picked from your pick line. As a result, your inventory may be out of balance and you may need to relocate inventory in RELO in order to correct it.
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

After the deletion, the quantity in the bulk location is restored to its original value (100 CS), but the pick line quantity is now -8 CS instead of 2 CS (the original value). Therefore, you will have to relocate some product from the bulk location to the pick line location in order to restore the pick line to its original value.

### DELETING AN ORDER THAT TRIGGERED A REPLENISHMENT <a id="deleting-an-order-that-triggered-a-replenishment"></a>

If you delete an order after performing and confirming the associated replenishments, there is no need to make any adjustments because your inventory will be in balance. If, on the other hand, you delete an order before picking the product and performing the replenishment, you may need to delete your replenishment. 
Refer to the previous section [Deleting a Replenishment](pick-lines-replenishment.html#deleting-a-replenishment) for complete instructions.

### CONFIRMING YOUR REPLENISHMENTS IN RFRP (RF ONLY) <a id="confirming-your-replenishments-in-rfrp-rf-only"></a>

If you confirm your replenishments in RF, you use the program RFRP (RF Replenish). Refer to [Confirming 
Your Replenishments in REPI](pick-lines-replenishment.html#confirming-your-replenishments-in-repi) for general information about replenishment logic in AccellosOne 
3PL. 
There are three replenishment modes to choose from in RFRP. These modes allow you to rank replenishments by urgency and perform urgent replenishments first, less urgent replenishments next and non-urgent replenishments last. They make it possible to improve the efficiency of your pick line picking and ship orders faster.
The three replenishment modes are:
The sort order of replenishment records in RFRP is as follows: order date/time, relocation date/time, customer code, level 1 value, to location code and quantity (lowest quantity first). The quantity calculation in 
RFRP depends upon the replenishment mode.
EXAMPLE OF REPLENISHMENT MODES
NOTE RFRP shows all replenishments; that is, both replenishments that are currently ready to be performed as well as those that will be performed in the future when there is space in the pick line location. Locations that are full and cannot be replenished immediately are indicated by the flag F for Full.
Active Demand Only replenishment records in which the on hand quantity in the pick line location is less than the order quantity for the location are displayed.
Threshold Minimum Only replenishment records in which on-hand quantity in the pick line location is less than the minimum quantity defined in PIIT are displayed.
All All replenishment records are displayed.

Suppose you have the following five replenishments:
Active Demand Mode rule: on hand quantity in location < order quantity for location (replenishment is urgent because there is a picking task for the location and not enough product to pick)
replenishment records displayed: 4, 5 sort order of replenishment records: 5, 4 (calculate on hand qty - on order qty and then display lowest records first)
Threshold Minimum Mode rule: on hand quantity in location < than minimum quantity (replenishment is less urgent because there is no picking task for the location)
replenishment records displayed: 1, 2 sort order of replenishment records: 1, 2 (calculate on hand qty - on minimum qty and then display lowest records first)
All Modes rule: none (display all replenishments)
sort order of replenishment records: same as Active Demand mode
RFRP also allows you to perform partial replenishments. For example, if your replenishment quantity is two pallets and your forklift can only carry one pallet at a time, you can replenish one pallet to the pick line and leave the remaining pallet to be replenished at a later time. Partial replenishments are useful whenever a full replenishment would be undesirable because of equipment limitations or lack of space in the pick line location.
1 Key in RFRP and press Enter.
Replenishment #Pick Line 
Location
Order Quantity for Location
On-Hand Quantity in 
Location
Minimum Quantity for 
Location (PIIT)
1 P1 0 10 25
2 P2 0 20 25
3 P3 30 30 25
4 P4 60 40 25
5 P5 80 50 25

RFRP screen
2 If required, you can restrict your replenishments to a particular warehouse by press F3 (EW) and entering your warehouse code.
3 If required, change your replenishment mode to D for Active Demand or I for Threshold Minimum and press Enter. If you press Enter without changing your replenishment mode, AccellosOne 3PL will use the default value of A for All.
AccellosOne 3PL will retrieve the appropriate replenishment records. 
RFRP screen showing a replenishment from A103 to B102 (B102 is not full)

4 Do one of the following:
5 If you wish to change the sequence of replenishments so as to perform certain replenishments first and postpone other replenishments to a later time, use your up and down arrow keys to scroll through the list.
6 Press F3 to position your cursor in the UI field.

RFRP screen showing prompt for UI value
If you wish to confirm all your replenishments:
If you wish to restrict your confirmation to certain replenishments:
a) Proceed to next step. a) Press F1 (Enter Criteria).
b) Press Enter to position your cursor in the field that you wish to restrict on. You can restrict on customer code, item code, level 
2, 3 and 4 values, UI value, order number, from warehouse code and to warehouse code.
c) Key in your restriction value; for example, your order number, customer code, etc.
d) If you wish to include a second field in your restriction, repeat the above two steps for your second value.
e) If you wish to see the number of replenishments that meet your restrictions, press F3 (Cq).
f) When you finish entering your query criteria, press F2 (Execute 
Query). AccellosOne 3PL will retrieve an RFRP record for each replenishment that meets the criteria that you specified.

7 Enter or scan in your UI value or lowest inventory value. 
RFRP screen showing prompt for quantity
8 Key in your quantity and press Enter. 
RFRP screen showing prompt for to location
9 Enter or scan in your to location and press Enter.
10 When you finish confirming your replenishments, press F4 the required number of times to exit.
CANCELLING A REPLENISHMENT
The Hold command in RFRP allows you to cancel a replenishment. When you cancel a replenishment, the following actions occur in AccellosOne 3PL: 
 all replenishments for the same inventory entity and from location are deleted
 a supervisor is prompted to log in and place the product on suspend hold
 the order lines for the inventory entity that triggered the replenishment is zeroed out, a P-type line is created and allocation is called 
 the RF operator is presented with an alternate replenishment task 

RFRP screen showing supervisor login message

### OVERRIDING REPLENISHMENT PRIORITIES IN RFRO <a id="overriding-replenishment-priorities-in-rfro"></a>

RFRO allows you to manually override the default sort sequence for replenishments in RFRP by means of a priority number override. For example, if you set the priority number override of replenishment 1 to 10 and the priority number override of replenishment 2 to 5, replenishment 2 will be listed before replenishment 1 in 
RFRP.
1 Enter RFRO.
2 Retrieve the replenishment whose priority you wish to override.
3 In the Priority Number Override field, key in your new priority number and press Enter.
4 Click on Save to save your changes.

RPRO screen showing replenishment with a priority number override value of 60
5 Click on Exit to exit.

### Troubleshooting Pick Lines and Replenishments <a id="troubleshooting-pick-lines-and-replenishments"></a>

Refer to the Allocation Troubleshooting Guide for instructions on troubleshooting your pick lines and replenishments. 

### Reports <a id="reports"></a>

Refer to the Standard Reports Guide.

## Directed Move System <a id="directed-move-system"></a>

*Manual K — Allocation and Wave Manager*

### Overview <a id="overview"></a>

The directed move system allows you to relocate confirmed product from a temporary inbound location to a final put-away location; the relocation occurs after any auto take-off holds placed on the product have expired and uses the directed move parameters defined in ILOP to select the best possible location for the product.
When you confirm the directed move in RELO or RFRL, AccellosOne 3PL will display the optimal location according to your ILOP parameters; you are free to accept this location or to override it with another location of your choice.
The directed move system is designed for facilities that store their inbound product in a blast freezing or paint shop location for a fixed number of days before moving it to a final put-away location. Because the inventory is confirmed while still in the temporary location, you can perform invoicing and EDI confirmation transactions on the actual receipt date while final put-way is deferred to a later date.
Directed moves can also be used to reverse or undo a relocation. For example, you move product to an outbound staging area after picking an order; the order is cancelled and you wish to return the product to a rack location using directed move to select the best location.
The directed move system can generate a report and labels showing both the inventory entities as well as the suggested locations for those entities.

### Setting Up the Directed Move System <a id="setting-up-the-directed-move-system"></a>

There are six setup programs for the directed move system:
 COMP (Company Code)
 HOLD (Hold Types)
 DMPA (Directed Move Profile)
 WARE (Warehouse and Location Format)
 ILOP (Item Location Profile)
DMPR
OFFICE/WAREHOUSE
If you use RF, you confirm the directed move in
RFRL. If you do not use RF, you confirm the directed move in RELO.
OFFICE
You assign suggested locations to the product in
DMPR (Directed Move Processing) and, if required, print labels or a report.
OFFICE
You time-stamp and confirm the receipt in CHRF (Time-Stamp and Confirm Receipt).
END
ENRE
CHRF
ENRE/RF
OFFICE
You enter the receipt in ENRE (Enter, Modify and
Delete Receipt).
OFFICE/WAREHOUSE
You assign a temporary location to the product manually in ENRE or you have the system assign the temporary location using directed put-away logic.
RF?
RELO RFRL
No Yes

 LOTP (Location Type)

### ACTIVATING DIRECTED MOVE IN COMP <a id="activating-directed-move-in-comp"></a>

You activate the directed move system in COMP by setting the Activate Directed Move Inbound flag to Yes.
COMP screen showing Activate Directed Move Inbound flag

### SETTING UP YOUR HOLD CODE(S) IN HOLD <a id="setting-up-your-hold-code-s-in-hold"></a>

If you use the directed move system to move product that has been on hold, you need at least one hold type in HOLD with the Auto Take-Off flag set to Y for Yes. 

HOLD screen showing a blast freezing hold code that will expire in five days

### SETTING UP YOUR DIRECTED MOVE PROFILE CODE IN DMPA <a id="setting-up-your-directed-move-profile-code-in-dmpa"></a>

You set up your directed move profile code in DMPA (Directed Move Profile). You then attach your directed move profile code(s) to the appropriate warehouses in WARE. If you have multiple warehouses on your system, you can create a unique directed move profile code for each warehouse or you can use the same directed move profile code for all warehouses.
In DMPA, you specify the following parameters:
 whether or not you want holds to be removed automatically when you generate suggested locations for your directed move in DMPR
 whether or not you want to require the authorization of a supervisor before an operator can override a suggested put-away location (RF only)
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
If you select Y for Yes, AccellosOne 3PL will automatically remove any expired auto take-off holds from product when you run DMPR. If you select N for No, you must run HATO (Holds Auto Take-Off) to remove expired auto take-off holds from product.
Supervisor Authorization 
Required to Override 
Location
Y = Yes
N = No
If you select Y for Yes, the operator can only override the system suggested location in RELO/RFRL if the change has been authorized by a supervisor. If you select N for No, the operator can override the system suggested location in RELO/RFRL without the authorization of a supervisor.
The Yes option requires at least one operator defined as a supervisor. A supervisor is an operator in OPER whose Supervisor Flag has been set to Y for Yes.

1 Enter DMPA.
2 Key in your directed move profile code and press Enter.
3 Key in a description for your new code and press Enter.
4 In the Automatically Remove Expired Hold Codes field, key in Y for Yes or N for No and press Enter.
5 In the Supervisor Authorization Required to Override Location field, key in Y for Yes or N for No and press Enter.
6 In the Document Code for Report field, key in your document code for the report and press Enter or press 
Enter with the field blank for no document code.
7 In the Document Code for Label field, key in your document code for the label and press Enter or press 
Enter with the field blank for no document code.
8 When you finish entering your directed move parameters, click on Return to Main.
Enable Automated Pallet 
Consolidation
See [Pallet Restacking](pick-lines-replenishment.html#pallet-restacking) for further information.
Staging Warehouse Code See [Pallet Restacking](pick-lines-replenishment.html#pallet-restacking) for further information.
Staging Location Code See [Pallet Restacking](pick-lines-replenishment.html#pallet-restacking) for further information.
Document Code for 
Report
Optional
The report printed for product on directed move. This report must be set up as a document in DOCU.
Document Code for Label Optional
The label printed for product on directed move. This label must be set up as a document in DOCU.
FIELD DESCRIPTIONS

DMPA screen showing document codes for printing labels and reports
9 Click on Exit.
ATTACHING YOUR DIRECTED MOVE PROFILE CODE TO A WAREHOUSE IN 
WARE
You attach your directed move profile code(s) to the appropriate warehouse(s) in WARE.

WARE screen showing directed move profile code 1 attached to warehouse 1

### SETTING UP YOUR DIRECTED MOVE PARAMETERS IN ILOP <a id="setting-up-your-directed-move-parameters-in-ilop"></a>

You set up your directed move parameters by selecting the Directed Move Stock option in the Type Block of 
ILOP (Item Location Profile) and then selecting the appropriate option from each logical group. After setting up your directed move stock ILOP profile, you attach this profile to the appropriate items in ITEM. The directed move stock options in AccellosOne 3PL are identical in every way to the put-away options described in [Standard Logical Groups for Put-Away](alocacao.html#standard-logical-groups-for-put-away). The same standard logical groups are used and each group contains the same options.
1 Enter ILOP.
2 Use your pick list function to select the isolator code for this profile. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
If you are creating a new ILOP profile:
If you are attaching your directed move parameters to an existing 
ILOP profile:
a) Key in an item location profile code and press Enter.
b) Key in a meaningful description for your new code and press 
Enter.
a) Click on Enter Criteria then Execute Query to search for the 
ILOP profile that you wish to update.
b) Click on Type Block.
c) Proceed to step 5.

3 Use your pick list function to select the warehouse code for your overflow warehouse. If you have a single warehouse, use this warehouse.
4 Use your pick list function to select the location code for your overflow location code.
5 Press your up or down arrow key in the Type Block until the Directed Move Stock option is displayed.

Blank Directed Move Stock screen
6 Proceed to enter your directed move parameters. Refer to [Setting Up a New Profile in ILOP for Directed 
Put-Away](alocacao.html#setting-up-a-new-profile-in-ilop-for-directed-put-away) for instructions on how to assign parameters to sequences in ILOP.
7 When you finish entering all your sequences, click on Sequence Block and Return to Main and then Type 
Block.

ILOP screen showing the selected parameters for the first pass
8 Click on Type Block.
9 Click on Master Block and then Exit to exit the program.

### SETTING THE DIRECTED PUT-AWAY AND STAGING FLAGS IN LOTP <a id="setting-the-directed-put-away-and-staging-flags-in-lotp"></a>

The final put-away locations for directed moves must be assigned a location type in LOTP whose Directed 
Put-Away flag has been set to Y for Yes and whose Staging flag has been set to N for No.

LOTP screen showing Directed Put-Away flag set to Y for Yes

### Assigning Suggested Locations for a Directed Move in DMPR <a id="assigning-suggested-locations-for-a-directed-move-in-dmpr"></a>

When you assign suggested locations for a directed move in DMPR, AccellosOne 3PL will automatically remove any expired auto take-off holds from the product being moved if the Automatically Remove Expired 
Holds flag in DMPA is set to Y for Yes. 
You can select the product to be moved by location (that is, one location at a time), by location type code, by isolator code, by zone code, by expiry date, by customer code, by level 1/2/3/4 value, by hold code and by audit number.
1 Make sure that the product is confirmed and that any auto take-off holds have expired. If you have set the 
Automatically Remove Expired Hold Codes flag in DMPA to No, you must run HATO to remove these holds.
2 Enter DMPR.

3 Key in your warehouse code and press Enter.

DMPR screen
4 If required, enter your location code, location type code, isolator code, zone code, expiry date, customer code, levels 1, 2, 3 or 4 values, hold code or audit number.
5 If the Enable Automated Pallet Consolidation flag is set to Yes, key in N for No and press Enter.
6 When you finish entering your search criteria, click on (Execute Query).
AccellosOne 3PL will display all confirmed product in the warehouse and location that you specified that is no longer on hold and meets any search criteria that you entered. 

DMPR screen showing selected product
7 Do one of the following:
AccellosOne 3PL will insert an asterisk to indicate that a particular inventory entity is selected. If you make a mistake and wish to undo your selection(s), click on Deselect All.
8 Click on (Move/Undo). AccellosOne 3PL will populate the To Whse & Loc. fields of selected inventory with a suggested location.
When you perform a move in DMPR, AccellosOne 3PL refreshes the screen by requerying with the original search criteria such as warehouse code, location code, customer code, level 1 value, etc. If your original query included a hold code and if you have activated the automatic removal of hold codes in 
DMPA, AccellosOne 3PL will requery without the original hold code.
If you wish to assign all locations:
If you wish to assign selected locations:
a) Click on Select All. a) Click on the lines that you wish to select.

DMPR screen showing to locations selected by system
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 

### Printing Labels for a Directed Move <a id="printing-labels-for-a-directed-move"></a>

If a suggested location has been assigned to an inventory entity, you can print a label for the product in 
DMPR. The label will show the level 3 value, the to location, the level 1 value and the quantity.
When you print a label for a particular inventory entity, the “N” in the Label column of DMPR is changed to “Y”.
1 Enter DMPR
2 Key in your warehouse code and press Enter.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Make sure that suggested locations have been assigned to the inventory entities whose labels you wish to print.
6 Click on (Print Label).

7 When the Printer Code Block appears, key in your printer code and press Enter.
8 Click on Execute Report.
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 

### Printing the Directed Move Report (DMVR) <a id="printing-the-directed-move-report-dmvr"></a>

The Directed Move Report shows the customer code, up to four inventory levels, the from and to locations, and the move quantity. DMVR shows only inventory that has been assigned a suggested location in DMPR; 
inventory without a suggested location will not print. 
When you run a report for a particular inventory entity, the “N” in the Report column of DMPR is changed to “Y”.
DMVR is an audit report. An audit report is a report that generates a unique audit number the first time that it is run for a given inventory entity. The audit number is assigned to each inventory entity included in the report. 
Once an audit number is assigned to inventory, it is fixed. New inventory will be assigned the next audit number in the series while existing inventory will retain the audit number that was originally assigned when the report was first run.
The purpose of audit numbers is to group a series of transactions that occurred at the same time into a single batch for audit and control purposes; for example, all directed moves for a particular customer or all directed moves performed on a specific date. If you know the audit number for a batch, you can easily assign and deassign suggested locations for all inventory in the batch.
1 Enter DMPR
2 Key in your warehouse and press Enter.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Make sure that suggested locations have been assigned to the inventory entities that you wish to report on.
6 Click on (Print Report).
7 When the Printer Code Block appears, key in your printer code and press Enter.
8 Click Ok.
9 Click on (Return) to exit Directed Move Details. 
10 Click on (Exit) to exit. 

Directed Move Report for audit 363

### Removing Suggested Locations for a Directed Move <a id="removing-suggested-locations-for-a-directed-move"></a>

You can remove suggested locations for a directed move in DMPR at any time before the directed move is confirmed in RELO or RFRL. When you remove suggested locations for a directed move, you can rerun 
DMPR at a later time to generate new suggested locations.
1 Enter DMPR.
2 Enter your warehouse.
3 If required, enter your location code, location type code, customer code, levels 1, 2, 3 or 4 values, hold code or audit number.
4 When you finish entering your search criteria, click on (Execute Query).
5 Select the inventory whose suggested locations you wish to deassign.
6 Click on Move/Undo. AccellosOne 3PL will remove the to location from the selected inventory entities.
7 Click on (Return) to exit Directed Move Details. 
8 Click on (Exit) to exit. 

### Confirming the Directed Move <a id="confirming-the-directed-move"></a>

You can confirm your directed move in either RELO (Relocate Inventory) or RFRL (RF Relocate). When you confirm a directed move, you have two choices: you can accept the location suggested by the system or you can select your own location.
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

If you ran the Directed Move Report in DMPR, the system-generated audit number assigned to the transactions will be used as the adjustment number for each inventory entity in the report. If you print labels rather than a report or do no printing, each move in RELO will be assigned a separate adjustment number.

### CONFIRMING THE DIRECTED MOVE IN RELO <a id="confirming-the-directed-move-in-relo"></a>

1 Enter RELO.
2 Enter any required search criteria.
3 Click on Move Mode.

RELO screen showing seven records that have been assigned directed move locations in DMPR
AccellosOne 3PL will automatically retrieve all records that were successfully assigned suggested locations in DMPR.
4 Use your arrow keys to select the inventory entity that you wish to confirm.
5 Click on Location Block.

RELO screen (Location Block) showing from location A101 with a negative quantity and to location 
A107 with a positive quantity
6 Do one of the following:
7 When the Remark Block appears, enter your remarks and press Enter or click on Return to Main to bypass remarks.
8 Click on Exit to exit.
If you accept the suggested location:
If you do NOT accept the suggested location:
a) Click on Relocate. a) Use your arrow keys to position your cursor over the suggested to location line.
b) Press Enter to position your cursor in the Adjust column of the suggested to location. Then click on Delete.
c) If the to location that you wish to put-away to is not displayed, click on Create Record. Then key in the location code and warehouse code (if required).
d) Key in the adjustment quantity and press Enter. The adjustment quantity should match the quantity in the Proof column.
e) Press Enter to bypass the Conveyance field.
f) Click on Relocate.

### CONFIRMING THE DIRECTED MOVE IN RFRL <a id="confirming-the-directed-move-in-rfrl"></a>

If the Supervisor Authorization Required to Override Location flag in DMPA has been set to Y for Yes and you attempt to override the suggested location in RFRL, the supervisor authorization pop-up window will appear. 
A supervisor must then log on to authorize the change in location.
1 Enter RFRL.
2 Enter any required search criteria.
3 Press F1 (Move Mode).

RFRL screen showing three records that has been assigned a directed move location in DMPR
4 If the quantity is not correct, press F9 to position your cursor in the Qty field. Then key in a new quantity and press Enter. 
5 Do one of the following:
If you accept the suggested location:
If you do NOT accept the suggested location:
a) Press Enter to accept the location.
b) Press F3 (PR) to confirm the move.
a) Key in the new location and press Enter.

RFRL screen showing prompt for supervisor authorization
b) If prompted to do so, key in the supervisor login and press Enter. 
Then key in the supervisor password and press Enter again.
c) Press F3 (PR) to confirm the move.

6 Repeat the above steps for each additional move that you wish to confirm.
7 When you finish processing your moves, press F4 twice to exit.

### Looking Up Directed Moves in LOEN <a id="looking-up-directed-moves-in-loen"></a>

When you run DMPR to assign suggested locations to a directed move, the following records are created in the Location Block of LOEN: the from location will show a positive quantity in both the On-Hand and Replenishment columns while to the to location will show a positive quantity in the Available column and a negative quantity in the Replenishment column.

LOEN screen showing A101 and A103 as the from location and A107 as the to location
When you confirm the directed move in RELO or RFRL, AccellosOne 3PL will create two records in the 
History Block: an IF (Information Only) record and an RL (Relocation) record. The IF record will show the from location and the suggested to location, while the RL record will show the from location and the actual to location selected in RELO or RFRL.

LOEN screen showing IF and RL records in History Block

### Pallet Restacking <a id="pallet-restacking"></a>

Directed Move processing supports automatic consolidation or re-stacking of partial pallets. For example, you have placed dividers in your pallets to improve the airflow during blast freezing and now wish to restack the pallet normally without dividers.
You define your pallet stacking rules in the Allow Merging Up To Level (RFMI) field in MRFP and you perform the actual restacking in RFMI (RF Merge Inventory). In DMPA, the following fields are required:
FIELD DESCRIPTIONS
Enable Automated Pallet 
Consolidation
If you enter Yes in this field, automated pallet consolidation will be activated.
Staging Warehouse Code Mandatory
The warehouse code where pallet restacking will take place.

In DMPR (Directed Move Processing), you can perform the following functions: 
 you can control the size of re-stacked pallets by entering values in the Maximum Height for Pallet, Linear Measure Code and Number of Layers on Pallet fields 
 you can override the staging location dynamically by changing default staging warehouse and location codes
 you can disable automated pallet re-stacking dynamically by turning off Enable Automated Pallet Consolidation
DMPR screen
Staging Location Code Mandatory
The staging location code where pallet restacking will take place.
FIELD DESCRIPTIONS

### Opportunistic Cross-Docking <a id="opportunistic-cross-docking"></a>

Opportunistic cross-docking allows you to put-away a receipt into a cross-dock location located on your receiving/shipping dock rather than into a bulk, rack or pick line location. Once the receipt is confirmed, the inventory can be allocated to a pending order in the usual way. Opportunistic cross-docking is designed to save labor and time by allocating inbound product to an outbound dock location.
AccellosOne 3PL will only assign inbound product to a cross-dock location if the following conditions have been met:
 there is a pending order with the same level 1 value and the same hold code (if any)
 the pending order has no level 2 or higher values entered and the to ship date is less than or equal to the current system date
 the cross-dock location has sufficient capacity to hold the entire receipt line (you cannot split a receipt line and sent part of the line to the cross-dock location and the remainder of the line to a non-cross-dock location)
 there is no inventory in a non-cross-dock location for the product being received (if the product being received is on hold, there is no inventory in a non-cross-dock location with a matching hold code)
Opportunistic cross-docking must be activated in ILOP (Directed Move Inbound). There are nine opportunistic cross-dock options:
CODE DESCRIPTION
M7010 enable OCD, put-away qty cannot exceed pending order qty with same ship date
The put-away quantity is less than or equal to the sum of all pending orders for the same item with the same ship date.
M7011 enable OCD option 7010 when pending order qty > on hand
1) The put-away quantity is less than or equal to the sum of all pending orders for the same item with the same ship date. 
2) The pending order quantity is greater than the on-hand quantity in the cross-dock location.
M7020 enable OCD, put-away qty can exceed pending order qty with same ship date
The put-away quantity can be greater than the sum of all pending orders for the same item with the same ship date.
M7021 enable OCD option 7020 when pending order qty > on hand
1) The put-away quantity can be greater than the sum of all pending orders for the same item with the same ship date.
2) The pending order quantity is greater than the on hand quantity in the cross-dock location.
M7030 enable OCD, distribute to orders with shipping lane, ignoring FIFO/LIFODistribute inbound product across multiple orders without running allocation. The priority of distribution will be based on order priority and ship to date. 
M7040 enable OCD, put-away qty cannot exceed pending order qty, ship in given hour
The put-away quantity is less than or equal to the sum of all pending orders for the same item with the same ship date that ship within the number of hours specified in the Hours field.

### “SHIP IN GIVEN HOUR” OPTION <a id="ship-in-given-hour-option"></a>

If you select either M7040 or M7042, you must specify the number of hours before the pending order's ship date/time that is acceptable for opportunistic cross docking. For example, the product is freezer product that cannot be left on the dock for more than a given number of hours. If, say, you specify a value of 6 hours and product is received at 12 noon, it cannot be assigned to a pending order with a ship date/time later than 6 pm on the same day.
ILOP screen showing Hours = 6 for M7040
M7041 enable OCD option 7040 when Pending 
Order Qty > On Hand
1) The put-away quantity is less than or equal to the sum of all pending orders for the same item with the same ship date that ship within the number of hours specified in the Hours field. 
2) The pending order quantity is greater than the on hand quantity in the cross-dock location.
M7042 enable OCD, put-away qty can exceed pending order qty, ship in given hour
The put-away quantity can exceed the sum of all pending orders for the same item with the same ship date that ship within the number of hours specified in the Hours field.
M7043 enable OCD option 7042 when Pending 
Order Qty > On Hand
1) The put-away quantity can exceed the sum of all pending orders for the same item with the same ship date that ship within the number of hours specified in the Hours field.
2) The pending order quantity is greater than the on hand quantity in the cross-dock location.
CODE DESCRIPTION

ILOP screen showing opportunistic cross-dock options

### SETTING UP OPPORTUNISTIC CROSS-DOCKING (M7010-21, M7040-43) <a id="setting-up-opportunistic-cross-docking-m7010-21-m7040-43"></a>

1 If you are only cross-docking certain product, create a new ILOP profile with cross-docking enabled. If you are cross-docking all your product, you can modify an existing profile instead of creating a new one.
2 Your cross-docking profile must contain only one put-away sequence in which cross-docking is enabled. 
The cross-dock sequence must be the first sequence in your profile.
3 For the put-away sequence in which cross-docking is enabled, you must define a cross-dock warehouse and location in the Sequence Block of ILOP. The location type set up in LOTP for the cross-dock location must have the Directed Put-Away and Directed Picking flags set to Y for Yes and the Staging flag set to N for No.
4 Create at least one non-cross-dock sequence after your first cross-dock sequence. In this non-crossdock sequence, you define a “next best” location should your cross-dock sequence fail.
5 If you are creating a new ILOP profile, attach the new profile to the items that you wish to cross dock.
6 Make sure that directed put-away is activated.
NOTE When you use any of “enable” options, they disable and override all other options in the sequence. For example, if you set up sequence 1 in ILOP with “use only exact match isolator code” and “enable OCD, put-away qty cannot exceed pending order qty with same ship date”, your exact match requirement for isolators codes will be ignored.

### SETTING UP OPPORTUNISTIC CROSS-DOCKING (M7030) <a id="setting-up-opportunistic-cross-docking-m7030"></a>

1 If you are only cross-docking certain product, create a new ILOP profile with cross-docking enabled. If you are cross-docking all your product, you can modify an existing profile instead of creating a new one.
2 Your cross-docking profile must contain only one directed move sequence in which cross-docking is enabled. The cross-dock sequence must be the first sequence in your profile.
ILOP screen showing option M7030
3 For the directed moved sequence in which cross-docking is enabled, you must define a cross-dock warehouse and location in the Sequence Block of ILOP. The location type set up in LOTP for the cross-dock location must have the Directed Put-Away and Directed Picking flags set to Y for Yes and the Staging flag set to N for No.
4 Create at least one non-cross-dock sequence after your first cross-dock sequence. In this non-crossdock sequence, you define a “next best” location should your cross-dock sequence fail.
5 If you are creating a new ILOP profile, attach the new profile to the items that you wish to cross dock.
6 Make sure that directed put-away is activated.
7 Create one or more shipping lanes in SHLA.

SHLA screen
Shipping lanes must be attached to a staging location in SHLA.
8 Assign your cross-dock consignees to shipping lanes in SLAS. A consignee can be assigned to only one shipping lane, but the same shipping lane can contain multiple consignees.
SLAS screen

### ATTACHING A SHIPPING LANE TO AN ORDER IN ENOR <a id="attaching-a-shipping-lane-to-an-order-in-enor"></a>

If you attach a shipping lane to an order in ENOR, it will override your shipping lane assignments in SLAS.
1 Enter ENOR.
2 Enter your order header information (customer, consignee, sold-to, etc.) in the normal manner.

ENOR screen showing prompt for shipping lane code
3 When you reach the Shipping Lane Code field, key in your shipping lane code and press Enter or use the picklist to select it.
4 Continue processing your order normally in ENOR.

## Wave Manager <a id="wave-manager"></a>

*Manual K — Allocation and Wave Manager*

### Overview <a id="overview"></a>

Wave Manager is a batch processing tool for orders that allows you to group orders by various criteria such as company code, allocated or unallocated status, flow process, customer, consignee, carrier, warehouse, load type, door, etc. and assign them to waves. You can define a date range for a wave using the ship date or arrive date and you can define a maximum size for a wave by the number of pieces, net or gross weight, cube or estimated number of hours of labor required.
When you process a wave using the Run Wave command, AccellosOne 3PL will allocate any unallocated orders in the wave and print the required number of carrier labels. The type and number of carrier labels printed is based on the order’s pick method. You configure your pick methods in CCDU (Customer / 
Consignee Document Setup).
Wave Manager supports label picking. With label picking, the AccellosOne 3PL-generated divider label shows the product’s location and number of cartons to pick, while the AccellosOne 3PL-generated carton label shows the consignee and carrier. The picker uses the divider label to pick the product. When applying the carton label to the picked product, only the first and last label is scanned. Label picking leads to improved speed and accuracy in picking and less sorting of product on the loading dock.
Divider label showing pick location and number of cartons to pick

You can save your wave parameters in one or more templates and schedule these templates to run automatically at a given time; for example, every 15 minutes, every day at 4:00 pm, every 30 minutes on Wednesday, etc.

### WAVES VS. TEMPLATES <a id="waves-vs-templates"></a>

A wave is a batch of orders whose selection is based on various selection criteria such as company code, customer code, allocation status, flow process, etc. A template is a reusable container holding the filters used to create waves containing only the orders that meet the criteria that you define.
NOTE A given template will retrieve a specific order only once. If you rerun the same template twice in the same day, only new orders meeting the template’s selection criteria will be retrieved; orders already retrieved the first time that the template was run will NOT be retrieved a second time.
Create Wave
You select your template and click on Run 
Wave From Template.
You select your wave parameters and click on Query. After Wave Manager retrieves your query results, you can run the wave “on demand” or save your template with a description and printer code.
If required, you print the Wave Summary 
Report.
If your orders allocated correctly, you pick 
RFPK them in RFPK.
Template 
Management
Run Wave 
From 
Template
If required, you select your printer code and disable label printing.
Wave 
Summary 
Report

### Setting Up Label Printing <a id="setting-up-label-printing"></a>

Labels printed from Wave Manager must be set up in BarTender Enterprise. They are not attached to flows in 
DIFP and are not governed by the reprint restrictions in DOCU.
The type and number of labels printed is based on the order’s pick method. There are nine possible pick methods supported in Wave Manager. The following pick methods do NOT support label picking:
The following pick methods DO support label picking and the generation of a label pick label: 
BATP requires setup in the Carrier Type Code field of CARR.
Pick Method Description
PALL A full pallet pick. The order quantity of each order line must equal a single pallet.
EACH A Pick & Pack by each (the smallest SKU in an item’s quantity breakdown).
blank A normal case pick in RFPIC/RFPK.
Pick Method Description
BATP A batch pick across multiple orders when two or more orders in the wave are being picked up by the same carrier and the carrier type = UPS, DHL or FEDEX.
For example, if order line 1 picks 10 cases from a given location and order line 2 picks 5 cases of the same product from the same location, Wave Manager will generate a consolidated pick of 15 cases from the location.
LABP An individual order pick when a single order is being picked up by a given carrier.
RFMG A merge of two or more OPID’s in RFMG.
PKST Manual packing performed in EPSD (Enter Packing Details).
PACK First level cartonization performed in RFSC (RF Sort to Carton) 
or RFPK (RF Wave Pick).
CART A Pick & Pack by each used in system-driven cartonization.

CARR screen showing carrier type code set to UPS
In CCDU (Customer/Consignee Document Setup), you specify which label and pick method applies to which customers/carriers/consignees. 
CCDU screen showing pallet label and pick method for customer A and consignee CONS
See the RF Guide for further information on CCDU (Customer/Consignee Document Setup).

### Setting Up Your Wave Deallocation Rule in CUST <a id="setting-up-your-wave-deallocation-rule-in-cust"></a>

In CUST you specify what the Wave Manager should do if an order cannot be fully allocated. There are two options to choose from:
 Deallocate All Orders and Delete Wave 
 Deallocate Pending Orders from Wave and Keep Wave
CUST screen showing Wave Deallocation Rule field
FIELD DESCRIPTIONS
Wave Deallocation Rule Deallocate All Orders and Delete Wave
Deallocate Pending Orders From Wave and Keep Wave
In this field, you define your wave de-allocation rules when using the Wave 
Manager. If you leave this field blank, unallocated order lines will remain as Ptype lines and no deallocation will occur.

### Launching Wave Manager <a id="launching-wave-manager"></a>

You launch Wave Manager from the ActiveDesktop. There are four main options in Wave Manager:
1 From ActiveDesktop click on Wave Manager.
Wave Manager screen
2 Click on Template Management to view your existing wave templates. Only templates created by yourself will display.
Create Wave Template Click on this option to create a new wave template. Any wave template that you create can only be viewed, edited and run by yourself. Wave templates are not shared; that means you do not have access to templates created by other AccellosOne 3PL operators and they do not have access to your templates.
Template Management Click on this option to manage your waves. You can update waves, run waves and schedule waves from this option. Only waves created by yourself will be accessible in Template Management.
Wave Management Click on this option to view and manage your waves. You can delete waves, view orders on a wave, reprint wave labels and generate wave reports. 
NOTE Wave Management shows all active waves in Wave 
Manager regardless of the operator who created them. You can delete waves and perform other wave operations on waves belonging to other operators.
Schedule Management Click on this option to view and manage your scheduled templates. 
You can search for scheduled templates and scheduled jobs, edit a scheduled template and look up the job status of a scheduled job. 

Template Management screen showing templates
3 If required, click on the appropriate filter. The Show All Templates filter shows templates only but no wave information, while the Show Templates That Have Waves filter shows only templates that have been used to generate a wave. If the same template has been used to generate multiple waves, a separate record is shown for each wave.
4 Click on Wave Management to manage your waves. Wave Management shows all waves created by all 
AccellosOne 3PL operators; you are not restricted to waves created by yourself.
Wave Manager screen showing Wave Search parameters
5 Enter or select your wave search parameters and click on Search.

Wave Results screen showing eight waves
6 Click on Exit to exit Wave Manager.

### Working With Pick Lists and the Column Manager <a id="working-with-pick-lists-and-the-column-manager"></a>

Wave Manager’s advanced navigation capabilities allow you to select multiple values from a pick list and turn on and off any column in your query results.

### SELECTING MULTIPLE VALUES IN A FILTER PICK LIST <a id="selecting-multiple-values-in-a-filter-pick-list"></a>

In this example, you select multiple orders from the order filter in Create Wave Template.
1 Click on the appropriate primary filter to display the various values that you can select for that filter.
Order Filter screen
2 Click on the field that you wish to select multiple values from.

Order Filter showing unselected order numbers
3 Select the individual records that you wish to add to your filter.
Order Filter showing three selected records
4 When you finish selecting your records, click on Add on the right side of your screen.
Order Filter showing selected records added to Order Number field
5 If your selection is correct, click on Add to add the records to the primary order filter. If your selection in incorrect, click on Clear and reselect your records.

Primary Wave Filters screen showing Order Filters field populated
6 To verify your selection, you can mouse over a populated field to see all selected records.
Primary Wave Filters screen showing pop-up window

### WORKING WITH THE COLUMN MANAGER <a id="working-with-the-column-manager"></a>

Column Manager allows you to select which columns you wish to see in your query results in Create 
Template, Template Management and Wave Management. Your Column Manager settings apply to the current session only; they are not saved when you exit Wave Manager.
1 Click on Cols to display the Column Manager.

Column Manager
2 Proceed to select or deselect the columns that you wish to display. If you make a mistake, you can click on the Check/Uncheck All Columns to undo your changes.
3 When you finish selecting your columns, do one of the following:

### Creating a New Template <a id="creating-a-new-template"></a>

There are two types in templates in Wave Manager: saved and unsaved. Saved templates are regular templates used on a daily basis in a production environment, while unsaved templates are intended for testing purposes only.
Both types of templates can be used to run waves and print labels, and both types of templates are stored in 
Template Management with the exception of unsaved templates that are created but not run. Unsaved templates that are not run are automatically deleted when you exit Create Template.
The only difference between a saved and unsaved but run template is the template’s description in Template 
Management. For an unsaved template, the system-created description will read “TEMPORARY - RUN 
If you wish to save your changes:
If you wish to exit without saving your changes:
a) Click on Refresh. Your updated columns will display after a few seconds.
a) Click on Close.

MODE ONLY TEMPLATE”. You can change an unsaved template into a saved template with a meaningful description by means of the Update Template command.
FIELD DESCRIPTIONS
Company Code Mandatory
The company code for the template. The value that you enter in this field determines many of the values in other filters such as Order Filters, Customer 
Filters and Consignee Filters.
Allocation Status All
Allocated
Unallocated
If you select All, all orders regardless of allocation status will be included in the wave. If you select Allocated, only allocated orders will be included in the wave. If you select Unallocated, only unallocated orders will be included in the wave.
Assigned to Load No
Yes
If you select No, only orders NOT attached to a load in SELO will be included in the wave. If you select Yes, only orders attached to a load in SELO will be included in the wave.
Advance Workflow No Advance Flow
Before Allocation
After Allocation
If you select No Advance Flow, the flow of orders in the wave will not be advanced when you run the wave. If you select Before Allocation, the flow of orders in the wave will be advanced before allocation occurs. If you select 
After Allocation, the flow of orders in the wave will be advanced after allocation.

Suspend Task Not Applicable
Yes
If you select Yes, picking tasks will be automatically suspended when you generate a wave in Wave Manager. This will allow you to manually adjust your pallet build assignments in PABU (Pallet Build) before they are released to RF or voice for picking.
If you select Not Applicable, picking tasks will be automatically released to RF or voice for picking once the wave is generated.
NOTE The suspension of picking tasks must be activated in COMP before you can use the Yes option in a template.
De-Allocate Rule Not Applicable
Unalloc. Orders
All Orders
In this field, you specify what the Wave Manager should do if an order cannot be fully allocated. If you select Unalloc. Orders, Wave Manager will deallocate pending orders from the wave and keep the wave. If you select All Orders, 
Wave Manager will deallocate all orders and delete the wave.
If you select Not Applicable, the option that you select in the Wave Deallocation Rule field in CUST will be used.
Banding Reserved for future use.
Flow Process Filters If you specify one or more flows, only orders at those flows will be included in the wave. 
Order Filters If you specify one or more orders, only those orders will be included in the wave. 
NOTE Filtering by specific orders is for testing purposes only. It is NOT recommended for saved templates as the template can only be used once before you must manually change the order restrictions.
Customer Filters If you specify one or more customers, only orders belonging to those customers will be included in the wave. 
FIELD DESCRIPTIONS

1 Click on Create Template.
Consignee Filters If you specify one or more consignees, only orders being shipped to those consignees will be included in the wave. 
You can specify consignees by consignee code, consignee name, consignee city, consignee state/province, consignee ZIP/postal code, consignee country code, consignee priority, freight destination code, load analysis code, consignee type (RETP) and special consignee status. 
Carrier Filters If you specify one or more carriers, only orders assigned to those carriers will be included in the wave. You can specify carriers by carrier code, standard alpha code, carrier type code and transport mode code.
Warehouse Filters If you specify one or more warehouses, only orders being picked from those warehouse will be included in the wave. You can specify warehouses by warehouse code and location type code. 
Freight Filters If you specify an AccellosOne 3PL load number, an external load number or a stop number, only orders assigned to the AccellosOne 3PL load number, external load number or stop number will be included in the wave.
Load Type Filters If you specify one or more load types, only orders assigned to those load types will be included in the wave.
Door Filters If you use APPL (Appointment Planner) to assign orders to buildings and doors, you can restrict your wave to orders assigned a particular building and door(s).
Item Filters If you specify one or more items, only order lines containing those items will be included in the wave. You can specify items by item code, hold code, alternate reporting type code, alternate reporting code and hazmat flag.
There are three possible values in the Hazmat Flag field: All, Inclusive or 
Exclusive. If you select All, all items regardless of hazmat status will be included in the wave. If you select Inclusive, any order containing at least one line with a hazmat item will be included in the wave. If you select Exclusive, only orders with NO hazmat items on any line will be included in the wave.
FIELD DESCRIPTIONS

Create Template screen
2 Proceed to enter or select the appropriate values in the various Create Template filters. If you do not know how to select multiple values in a filter, see [Selecting Multiple Values in a Filter Pick List](pick-lines-replenishment.html#selecting-multiple-values-in-a-filter-pick-list).
3 Click on Date Filters to view your date restrictions. If you do not want to enter date restrictions, click on 
Clear Date Filters.
Date Filters
4 If you wish to enter capacity parameters, click on Capacity Parameters.
NOTE Date restrictions are NOT recommended for saved templates.

Capacity Parameters
5 Key in any required capacity parameters.
6 Select the appropriate sort order (order number, ship to date or carrier) for your query results.
7 When you finish entering your wave parameters, click on Query.
Wave Results screen showing wave results
8 If you wish to exclude individual orders from the wave, click on the Select checkbox of the first order to be excluded. Then click on any part of the row except the checkbox of any additional orders that you wish to exclude from the wave.
If you make a mistake and wish to include any previously excluded orders, click on the Select checkbox in the header row to select all rows in the wave results.
9 If you excluded one or more individual orders from the wave in the previous step, click on Use Selected 
Rows to refresh your screen and show only the selected orders.
10 Do one of the following:
If you are creating a saved template:
If you are NOT creating a saved template:
a) Click on Save Template. End of Procedure.

Save Template screen
11 Key in a meaningful description for your new template.
12 Select your label printer code from the pick list.
13 Click on Save Template.

### SETTING YOUR WAVE PREFERENCES <a id="setting-your-wave-preferences"></a>

Wave preferences allow you to set the unit of measure, number of orders per page and the default value in the “Disable Label Printing for this run” checkbox in Run Wave From Template. Wave preferences apply to waves run in the current session only; once you exit Wave Manager, wave preferences are reset to the default values.
If you want to apply your own wave preferences to a given template, you must reset your wave preferences on the Preference screen and then use the Update Template command to save your wave preferences for that template.
FIELD DESCRIPTIONS
System of Measure Metric
Imperial
The unit of measure used in the wave results for gross weight, net weight and cube.
Orders Per Page 100
The number of orders per page in the wave results.

1 Click on Query Preferences.
Wave Manager showing Query Preferences window
2 Make any required changes to your preferences.
3 Click on Query Preferences to close the Query Preferences window and save your changes.

### MODIFYING A TEMPLATE <a id="modifying-a-template"></a>

The Modify Template command allows you to modify the template’s company code, allocation status, assigned to load flag as well as the various flow process, order and other filters.
1 Click on Template Management.
2 Select the template that you wish to modify.
3 Click on Modify Template.
4 Make any required changes to the Primary Wave and Date Filters as well as to the Capacity Parameters.
5 When you finish making your changes, click on Query.
6 Click on Update Template to save your changes.

### UPDATING A TEMPLATE <a id="updating-a-template"></a>

The Update Template command allows you to update the template description and label printer code. The 
Warehouse Code, Location Code and Printer Code fields are reserved for future use.
If you have reset your wave preferences in the current session, the Update Template command will attach those preferences to the template.
Run Wave Label Printing ON
OFF
If you select ON, the Disable Label Printing for this run checkbox in Run Wave 
From Template will NOT be selected. If you select OFF, the Disable Label 
Printing for this run checkbox will be selected.
Exclusion Rules Use ALL Exclusion Filters
Use Excluded Orders Only
Use Included Orders Only
No Exclusion
In this field, you define your exclusion rules. You can use all your exclusion filters (default value), only your excluded order filters, only your included order filters or no exclusions. If you select no exclusions, any exclusions in your template will be ignored.
FIELD DESCRIPTIONS

1 Click on Template Management.
2 Select the template that you wish to modify.
3 Click on Update Template.
Update Wave Template
4 Proceed to make your changes to the wave template.
5 When you finish making your changes, click on Update Template to save your changes.

### DELETING A TEMPLATE <a id="deleting-a-template"></a>

1 Click on Template Management.
2 Select the template that you wish to delete.
3 Click on Delete in the Action column.

### LOOKING UP THE GENERATED SQL FOR A QUERY <a id="looking-up-the-generated-sql-for-a-query"></a>

The SQL Inspector allows you to look up the generated SQL for queries in Create Template. It is used for debugging purposes when the actual results set does not match the expected results set.
1 Click on Create Template.
2 Proceed to enter or select the appropriate values in the various Create Template filters.
3 When you finish entering your wave parameters, click on Query.
4 Click on SQL.
SQL Inspector screen showing generated SQL for a Create Web Template query

5 When you finish looking up your generated SQL, click on SQL again to close the SQL Inspector.

### CREATING A CUSTOM SQL FILTER <a id="creating-a-custom-sql-filter"></a>

You can create custom SQL filters to complement your primary wave filters.
1 Click on Create Template.
2 Click on Custom SQL Filter.
3 Click on Edit/View Custom SQL Filter.
Custom SQL Filter
4 Enter your SQL commands in the box at the bottom of your screen.
5 When you finish entering your SQL parameters, click on Apply Custom SQL Changes.
6 Click on Test Parameters and SQL to test your new filter.
7 If your test is successful, click on Cancel to exit. If your test is unsuccessful, correct your filter and click on Test/Validate SQL.

### Running a Wave <a id="running-a-wave"></a>

When you process a wave using the Run Wave command, AccellosOne 3PL will allocate any unallocated orders in the wave and print the required number of carrier labels. 

1 Click on Template Management.
2 Select the template that you wish to run and click on Run Wave From Template.
Run Wave From Template screen
3 If the Label Printer Code field is not populated, select your printer code from the pick list.
4 If required, you can click on the Disable Label Printing for this run checkbox to select or deselect it.
5 Click on Run Wave From Template.
Wave Manager will display the Wave Manager Information screen showing the job number.
Wave Manager Information screen showing job number

### RUNNING A WAVE FROM AN UNSAVED TEMPLATE <a id="running-a-wave-from-an-unsaved-template"></a>

You can run a wave from an unsaved template in Create Template.
1 Click on Create Template.
2 Enter your wave parameters in the normal manner.
3 If required, clear your date filters. If you do not clear your date filters, the default ship date will be set to today’s date.
4 Click on Query.
5 When the wave results screen displays, click on Run Wave.
Run Wave screen
6 If the Label Printer Code field is not populated, select your printer code from the pick list.

7 If required, you can click on the Disable Label Printing for this run checkbox to select or deselect it.
8 Click on Run Wave.

### SEARCHING FOR A WAVE <a id="searching-for-a-wave"></a>

You can search for a wave by company code, wave status, label print status, order number, wave create date and wave ID. If you enter a comma between each value in Wave ID field, you can search for multiple wave 
ID’s.
1 Click on Wave Management.
Wave Search
2 Enter or select your wave search parameters and click on Search.
Wave Results screen

### LOOKING UP ORDERS ON A WAVE <a id="looking-up-orders-on-a-wave"></a>

1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.

3 Select the wave whose orders you wish to look up and click on View Wave Orders.
Wave Orders screen
4 Click on Close to return to the Waves screen.

### DELETING ORDERS FROM A WAVE <a id="deleting-orders-from-a-wave"></a>

1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave containing the order(s) that you wish to delete and click on View Wave Orders.
Wave Orders screen
4 Select the order(s) that you wish to delete and click on Delete in the Action column.
5 Click on Close to return to the Waves screen.

### DEALLOCATING ORDERS BY WAVE IN DOWA <a id="deallocating-orders-by-wave-in-dowa"></a>

You can deallocate all orders in a wave or selected orders in a wave in DOWA (Deallocate Orders by Wave).
1 Enter DOWA.
2 Key in your wave number and press Enter.
DOWA screen

3 Do one of the following:
The screen will clear.
4 Click on Exit.

### TIME-STAMPING AND CONFIRMING A WAVE IN CHOF <a id="time-stamping-and-confirming-a-wave-in-chof"></a>

You time-stamp and confirm waves in CHOF (Time Stamp and Confirm Orders) in the same way that you time-stamp and confirm individual orders. Advancing the flow of a wave will advance the flow of all orders on the wave.
1 Enter CHOF.
2 Press Enter until your cursor is positioned in the Batch Order Number / Wave Number field.
3 Key in your wave number and press Enter.
CHOF screen showing wave with next flow process code of STLO (Start Loading)
4 Proceed to advance the wave’s flow in the normal manner.
To deallocate all orders in the wave:
To deallocate selected orders in the wave:
a) Click on Deallocate All. a) Select the orders that you wish to deallocate.
b) Click on Deallocate 
Selected.

### DELETING A WAVE <a id="deleting-a-wave"></a>

Waves that run successfully should be deleted on a regular basis to maintain system performance and to avoid running out of disk storage space.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave that you wish to delete and click on Delete Wave.

### LOOKING UP A WAVE’S COMPLETION STATUS <a id="looking-up-a-wave-s-completion-status"></a>

You can look up a wave’s completion status by clicking on Status in the Action column. When you click on 
Status, Wave Manager displays Operational Board information showing completed vs. remaining quantities and percentages for the wave.
An order is considered completed when the entire order is confirmed in CHOF or the order line is confirmed in 
COOL.
If you have set up labor standards in AccellosOne 3PL, Wave Manager shows the estimated number of hours and minutes that it took to perform the completed work as well as the estimated number of hours and minutes to finish the remaining work.
See the Operational Board documentation in the Operations 2 Guide for further information on tracking completed vs. remaining work.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave whose status you wish to look up and click on Status in the Action column.
Order Summary screen showing partially complete wave
4 When you finish looking up the wave’s completion status, click on Close.

### LOOKING UP A WAVE’S JOB HISTORY <a id="looking-up-a-wave-s-job-history"></a>

To monitor your run jobs, you can use the Run Jobs tab to see the wave ID generated by the job as well as the job’s status (Success, No Wave, etc.). If the job failed and no wave was generated, you can look up the probable cause by clicking on Job Details.
1 Click on Run Jobs.

Wave Manager Job History window showing wave ID generated by the job, job status and job details
2 If required, click on the wave ID to see the wave details.

### LOOKING UP YOUR PRINT JOB DETAILS <a id="looking-up-your-print-job-details"></a>

The Print Jobs tab shows the status of your print jobs and printers. You use this command when your wave was successfully generated, but no labels printed.
1 Click on Print Jobs.

Print Job History screen

### GENERATING A WAVE SUMMARY REPORT <a id="generating-a-wave-summary-report"></a>

The Wave Summary Report is generated automatically whenever a wave is run. It shows the total units, gross weight, net weight, cube, pending or unallocated quantity, header flow, maximum line flow (which may be later than the header flow) and the to ship date for each order on the wave.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave that you wish to report on and click on Generate Wave Report.

Wave Summary Report
4 If you wish to print the report, right click anywhere on the report and select Print. When the Print window appears, select your printer and click on Print.
5 Select File > Exit to close the report window.

### GENERATING A WAVE DETAILS REPORT <a id="generating-a-wave-details-report"></a>

This report can only be run once immediately after running your wave. It is for support purposes if orders do not allocate and is not available after you exit the Wave Manager Information window.
Wave Details Report

### REPRINTING WAVE LABELS <a id="reprinting-wave-labels"></a>

When you reprint wave labels, you can reprint all wave labels or exception labels only. Exception labels are labels that failed to print in BarTender.
1 Click on Wave Management.
2 Enter or select your wave search parameters and click on Search.
3 Select the wave whose labels you wish to reprint and click on Reprint Wave Labels.
Reprint Wave Labels screen
4 Select the appropriate label type from the dropdown list (all labels or exception labels only).
5 If required, select a new label printer code.
6 Click on Reprint Wave Labels.

### LOOKING UP AN ORDER’S WAVE NUMBER IN LOOR <a id="looking-up-an-order-s-wave-number-in-loor"></a>

The order header in LOOR (Look Up Orders) shows the order’s wave number, while the order line shows the picking method for that order line.

LOOR screen showing wave number
Line Block of LOOR showing picking method for order line 1

### Scheduling a Template <a id="scheduling-a-template"></a>

You can schedule a template to run automatically at a given time; for example, the 15th minute of each hour, every day at 4:00 pm, the 30th minute of each hour on Wednesday, etc. You must specify a start date for a scheduled template. The end date field for a scheduled template is optional. 
You set up scheduling by selecting the appropriate values in the Minutes, Hour, Day, Month and Day of Week dropdown lists. The following chart shows some of various scheduling scenarios available in Wave Manager.
Wave scheduling must be activated by HighJump.
1 Click on Template Management.
2 Select the template that you wish to schedule and click on Schedule Wave From Template.
Wave Template Scheduler
3 Click on Start Date to select your start date from the pop-up calendar.
Frequency Minutes Hour Day Month
Day of 
Week the 20th minute of each hour 20 " " " " the 45th minute of each hour on Wednesdays
45 " " " Wednesday
9 am every day " 9 am " " "
9 am every Monday " 9 am " " Monday
9 am first of the month " 9 am 1 " "

4 If required, click on End Date to select your end date from the pop-up calendar.
5 Select your the appropriate values from the Minutes, Hour, Day, Month and Day of Week dropdown lists. 
6 When you finish setting up your schedule, click on Save.

### SEARCHING FOR A SCHEDULED TEMPLATE <a id="searching-for-a-scheduled-template"></a>

A scheduled template search allows you to search for all scheduled templates, active scheduled templates or inactive scheduled templates. Scheduled template searches retrieve all templates whether or not they have ever run; for example, a scheduled template with a start date in the future that has not run yet.
1 Click on Schedule Management.
Schedule Management screen
2 Select your schedule type from the dropdown list: All Scheduled Templates, Active Scheduled Templates or Inactive Scheduled Templates.
3 If required, enter a start date, end date or template ID.
4 Click on Search Scheduled Templates.
Search Results for Scheduled Templates pane
5 Click on the scheduled template that you wish to look up.

Wave Manager will display the scheduled start date, schedule end date (if any) and template ID in the fields of the same name.

### SEARCHING FOR A SCHEDULED JOB <a id="searching-for-a-scheduled-job"></a>

A scheduled job search allows you to search for jobs based on scheduled templates that have already run. 
You can search for all jobs, successful jobs, failed jobs or unprocessed or new jobs. An unprocessed or new job is a failed job that did not run to completion for any reason.
After performing your scheduled job query, you can click on any scheduled template in your query results and look up detailed processing information for each job run as part of the scheduled template.
1 Click on Schedule Management.
Schedule Management screen
2 Select your job status from the dropdown list: All Jobs, Successful Jobs, Failed Jobs or Unprocessed or 
New Jobs.
3 If required, enter the date that the job was processed.
4 Click on Search Scheduled Jobs.
Search Results for Scheduled Jobs pane showing the date processed, status and template ID
5 Click on the scheduled job that you wish to look up.

Wave Manager will display the scheduled start date, schedule end date (if any), template ID and date processed in the fields of the same name.
6 Click on View Scheduled Jobs. This command will show all jobs run for the currently selected scheduled template plus detailed processing information for each job.
History of Wave Batch Jobs showing each job run for the selected scheduled template (203754)
7 When you finish looking up your scheduled jobs for the currently selected template, click on Close.

### PERFORMING A SHORTCUT SEARCH <a id="performing-a-shortcut-search"></a>

Shortcut searches allow you to search for Today’s Jobs (jobs run today whether successful or not), Today’s 
Successful Jobs and Show All Successful Jobs (all successful jobs regardless of date).
1 Click on Schedule Management.
Schedule Management screen showing shortcuts
2 Click on the appropriate shortcut: Today’s Jobs, Today’s Successful Jobs or All Successful Jobs.

Search Results for Scheduled Jobs pane showing the date processed, status and template ID
3 Click on the scheduled job that you wish to look up.
Wave Manager will display the scheduled start date, schedule end date (if any), template ID and date processed in the fields of the same name.

### EDITING A SCHEDULED TEMPLATE <a id="editing-a-scheduled-template"></a>

1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Templates.
3 In the Search Results for Scheduled Templates pane, click on the template that you wish to edit.
4 Click on Edit Schedule.
Wave Template Scheduler screen
5 Click on Edit Schedule.
6 Proceed to make your changes to the schedule.
7 Click on Save to save your changes.

### DELETING A SCHEDULED TEMPLATE <a id="deleting-a-scheduled-template"></a>

You can delete a template’s schedule at any time.
1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Templates.
3 In the Search Results for Scheduled Templates pane, click on the template that you wish to delete.
4 Click on Edit Schedule.

5 Click on Delete Schedule.

### LOOKING UP A SCHEDULED TEMPLATE’S JOB HISTORY <a id="looking-up-a-scheduled-template-s-job-history"></a>

The job history of a scheduled template shows the date of the job, the job status (S for Successful, E for Error or N for New), the process code (if job status = S or E) and processing information.
1 Click on Schedule Management.
2 Enter your search criteria and click on Search Scheduled Jobs.
3 In the Search Results for Scheduled Jobs pane, click on the job that you wish to look up.
4 Click on View Scheduled Jobs.
History of Wave Batch Jobs
5 When you finish looking up your scheduled template’s job history, click on Close.

### Paper-Based Tracking <a id="paper-based-tracking"></a>

You can generate a document to support paper-based picking for product that is not properly labeled. Wave 
Manager will automatically break tasks down into the standard MHE capacity based on your configuration in 
REGI. You set up paper-based tracking in LTRE (Load Type/Task Profiles). In this program, you create a relationship between a load type code (LOAD) and a task profile (REGI).
Paper-based tracking requires a custom document from HighJump.
LTRE screen

A absolute FIFO/LIFO (PIPR) 55 allocation automatic de-allocation of an order 100 by minimum level 2, 3 and 4 values 119 by shelf life 102 by shelf life percentage 104 by weight 81 de-allocating an order in DEOR 96 inventory only 85 looking up order processed in ASOR 95 of fully filled orders only 117 of variable quantity breakdown product 80 overview 49 picking 67 put-away 4 reserving a minimum level of inventory 125 soft 111 using ASOR 87 wildcard characters and Boolean logic, using 116
ASOR (Assign Orders to Location) 87
Assign Orders to Location (ASOR) 87 automatic de-allocation 100 automatic replenishment 142
B
Boolean logic and wildcard characters, using in allocation
Breaking inventory into multiple to locations group (ILOP)
15, 16, 17, 18
Calculate capacity by lowest/highest SKU class group (ILOP) 14
Capacity group (ILOP) 15, 70
CCOP (Customer/Consignee Override of PIPR) 65 combining fixed position and floating positions in the same pick line 153 cross-docking (opportunistic) 197
Cube capacity group (ILOP) 12
Customer/Consignee Override of CCOP) 65
D deactivating directed put-away for selected receipts 34
De-Allocate Order (DEOR) 96 de-allocation (automatic) 100 de-allocation (manual) 96
DEOR (De-Allocate Order) 96
Directed Move (ILOP) 182
Directed Move Processing (DMPR) 185
Directed Move Profile (DMPA) 179
Directed Move Report (DMVR) 189 directed moves assigning suggested locations for in DMPR 185 confirming 190 looking up in LOEN 194 overview 176 printing labels for 188 printing the Directed Move Report 189 setting up 177 directed put-away 4
DMPA (Directed Move Profile) 179
DMPR (Directed Move Processing) 185
DMVR (Directed Move Report) 189 double stacking product in directed put-away 17
DOWA (Deallocate Orders by Wave) 227
E
Empty and/or partially filled location group (ILOP) 6
Entire Dock Quantity group (ILOP) 19
Evaluate Minimum flag in ORPR 125
F
FIFO group (ILOP) 73
FIFO/LIFO parameters in PIPR, setting 52
Fill location group (ILOP) 11 fully filled orders, shipping 117

H hard allocation, performing in OPLU 112
Hold code group (ILOP) 11, 71
Ignore/use in transit when calculating capacity by cube group (ILOP) 10
Ignore/use in transit when calculating capacity by quantity group (ILOP) 9
Ignore/use on order when calculating capacity by cube group (ILOP) 11
Ignore/use on order when calculating capacity by quantity group (ILOP) 10
Ignore/use on order when calculating capacity by weight group (ILOP) 10
Ignore/use on receipt when calculating capacity by cube group (ILOP) 9
Ignore/use on receipt when calculating capacity by quantity group (ILOP) 8
Ignore/use on receipt when calculating capacity by weight group (ILOP) 9
Ignore/use outstanding moves/relocates when calculating capacity by cube group (ILOP) 11
Ignore/use outstanding moves/relocates when calculating capacity by quantity group (ILOP) 11
ILOP (Directed Move) 182
ILOP (Picking) 67
ILOP (Put-Away) 4
ILOP (Put-Away), overriding for individual receipt lines 26
ILOP (Replenishment) 142
IMSL (Item Minimum Shipping Level) 119
INAT (Inventory Attribute Factors) 46 inventory only allocation 85
IPUP (Item Put-Away Parameters) 44
Isolator group (ILOP) 5, 69
Item Minimum Shipping Level (IMSL) 119 item-specific picking profiles 65
IVLP (Item Velocity Location Profile) 27
Last location used group (ILOP) 12
Location Height group (ILOP) 16
Location Size Codes (LOCS) 40
Location size group (ILOP) 12
Location type group (ILOP) 74
LOCS (Location Size Codes) 40
LTRE (Load Type / Regions) 240
M manual de-allocation 96 minimum level of inventory, reserving 125 minimum shipping levels for item in IMSL 119
Mixed product group (ILOP) 70 mixing fixed position and floating locations in the same pick line 153
O on demand replenishments 165
On receipt hold code group (ILOP) 71
On receipt mixed product group (ILOP) 71
On receipt partial quantity group (ILOP) 73
OPLU (Order Line Inventory/Location Update) 112 opportunistic cross-docking 197
Opportunistic cross-docking group (ILOP) 14 orders allocating in ASOR 87 automatically de-allocating 100 manually de-allocating 96 pending versus regular 49 shipping by weight 81 shipping only fully filled 117 shipping with insufficient inventory 50
ORPR (Order Priorities) 100
Overflow Location Size Code field (LOCS) 41
Overflow Sequence Number field (LOCS) 41 overpicking order lines 62
Override quantity breakdown group (ILOP) 74 overriding directed put-away zone code 39
P
Pallet Breakdown group (ILOP) 73 pallet restacking 195 pallet type, put-away by 46 paper-based tracking 240
Partial quantity group (ILOP) 72
Partially filled location group (ILOP) 6
Pick Line Item Assignment (PIIT) 144 mixing fixed position and floating locations in the same pick line 153 overview 131 setting up a fixed position pick line 134 setting up a floating pick line 151 troubleshooting 173 types of pick lines 133 picking (directed) 67
Picking Profile (PIPR) 52
PIIT (Pick Line Item Assignment) 144
PIIT Location Capacity group (ILOP) 18
PIPR (Picking Profile) 52
PND Location Capacity group (ILOP) 18
PnD Location group (ILOP) 18
Product Stacking group (ILOP) 17 proximity logic for last location used group 42
PUPR (Put-Away Profile Code) 31, 157 put-away (directed) 4 put-away by location size 40 put-away by pallet type 46 put-away by zone code 38
Put-Away Profile Code (PUPR) 31, 157
R
Receipt date group (ILOP) 69 relative FIFO/LIFO (PIPR) 55
Relocate to Pick Line (REPI) 163
