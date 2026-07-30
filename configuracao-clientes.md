---
title: "Configuração — Clientes e Consignatários"
description: "Códigos de cliente (CUST), consignatários, sold-to, shippers e perfis de cliente."
layout: default
---

# Configuração — Clientes e Consignatários

Códigos de cliente (CUST), consignatários, sold-to, shippers e perfis de cliente.

**Fluxo principal:** `CUST -> CONS/SOLD/SHIP -> DBIP/DSRP/DIFP (perfis do depositante)`

> Fonte: manuais N do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Customer Setup <a id="customer-setup"></a>

*Manual N — Setup Guide*

### Salespersons (SAPE) <a id="salespersons-sape"></a>

OVERVIEW
In this program, you set up your salespersons. A salesperson is the individual who established the contract with the customer or is responsible for the rates charged to the customer. By setting up the information in 
SAPE, you have a point of contact if there are any questions with regard to the account or the rates.
If you do not know the salesperson for a particular account or you do not have salespersons in your warehouse, you can use the code HA for House Account.
PROCEDURE
1 Enter SAPE.
2 Click on Enter Criteria then Execute Query to see which salespeople are already set up.
PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of your salespersons
FIELD DESCRIPTIONS
Salesperson Mandatory
Your code for this salesperson. For example, JS for John Smith.
Name Mandatory
The name of the salesperson.

Salespersons
3 If the salespeople that you require have already been set up, click on Exit to exit. There is no need to add any new codes to SAPE.
If the salespeople that you require have not been set up, click on Create Record. 
4 Key in your salesperson’s initials or other code (up to four alphanumeric characters) and press Enter.
5 In the Name field, key in the salesperson’s first and last name and press Enter.
6 Repeat steps 4 and 5 for each additional salesperson that you wish to add. 
7 When you finish setting up your salespeople, click on Return to Main and then Exit to exit the program.

### Customer Service Representatives (CUSE) <a id="customer-service-representatives-cuse"></a>

OVERVIEW
In this program, you set up your customer service representatives. A customer service representative is the individual responsible for any support issues involving a customer.
If you do not know the name of a particular representative or do not have customer service representatives in your warehouse, you can use the code HA for House Account.
You can also use CUSE to set up “Attention to” names. “Attention to” names print on the accessorial, renewal, extra charge and immediate accessorial invoices if they are specified in BILB (Billing Batch).
PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of your customer service representatives

PROCEDURE
1 Enter CUSE.
2 Click Enter Criteria then Execute Query to see which customer service representatives have already been set up.
Customer Service Reps
3 If the customer service representatives that you require have already been set up, click on Exit. There is no need to add any new codes to CUSE.
If, however, the customer service representatives that you require have not been set up, click on Create 
Record.
4 Key in your customer service representative’s initials or other code (up to four alphanumeric characters) 
and press Enter.
5 In the Description field, key in the customer service representative’s first and last name and press Enter.
6 Repeat steps 4 and 5 for each additional representative that you wish to add. 
7 When you finish setting up your representatives, click on Return to Main and then Exit to exit the program.
FIELD DESCRIPTIONS
Customer Service RepresentativeMandatory
Your code for this customer service representative. For example, KJ for Karen 
Jones.
Name Mandatory
The name of the customer service representative.

### Flow Process (FLPR) <a id="flow-process-flpr"></a>

OVERVIEW
AccellosOne 3PL uses flow process codes to track and time-stamp inbound and outbound shipments. There are six codes that are preloaded into your system and cannot be modified or deleted. These six codes are:
CITR (Change In-Transit to Regular)
COOR (Confirm Order)
CORE (Confirm Receipt)
EDI (Message Received by TradeLink)
ENOR (Enter Order)
ENRE (Enter Receipt)
Flow process codes are attached to the depositor workflow profile in DIFP. A workflow profile is a sequence of steps or “flows” that must be taken for all inbound receiving and outbound shipping. The following codes are mandatory and must be included in any workflow profile:
ENRE (Enter Receipt)
CORE (Confirm Receipt)
ENOR (Enter Order)
COOR (Confirm Order)
Additional flow codes, which are optional, have been preloaded into AccellosOne 3PL. Some examples are 
DRDO (Driver Arrived at Door), STPI (Start Picking), FIPI (Finish Picking) and STLO (Start Loading). 
PREREQUISITES: None
ATTACHED TO: DIFP (Depositor Workflow Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE Although there is a create record function in FLPR, custom flow codes that you create yourself are not supported in RF. 

PROCEDURE
1 Enter FLPR.
2 Click on Enter Criteria then Execute Query.
FIELD DESCRIPTIONS
Flow Process Code Mandatory
Your code for this flow. For example, DOCK for dock check-in.
Description Mandatory
The description of your flow.
Priority Reserved for future use
Labor Standard Profile 
Code (LSOA)
See the Operational Board section in the Operations 2 Guide.
Unit of Measure See the Operational Board section in the Operations 2 Guide.
Labor Standard Modifier 
Profile Code (LSMP)
See the Operational Board section in the Operations 2 Guide.
Alert Time See the Operational Board section in the Operations 2 Guide.
Suppression Rules for eVista Client AccountsSee the e-Vista Setup Guide — Warehouse Only.
Inbound Sequence NumberSee the Operational Board section in the Operations 2 Guide.
Outbound Sequence 
Number
See the Operational Board section in the Operations 2 Guide.

Flow Process codes
3 Using your arrow keys, go through each record to see the list of standard flow process codes that have been preloaded into your system. If the codes that you require have already been set up, click on Exit. 
There is no need to add any new codes to FLPR.
If, however, the flow process codes that you require have not been set up, click on Create Record.
4 Key in your new flow code and press Enter.
5 Key in a meaningful description for the new code and press Enter. The description that you type in here will be the description that you want your customer to see on his reports and documents.
6 In the Priority field, key in 1 and press Enter.
7 Press Enter to bypass the remaining fields in FLPR.
8 Repeat steps 4 to 7 for each additional code that you wish to add.
9 When you finish setting up your flow codes, click on Return to Main and then exit to exit the program.

### Depositor Workflow Profile (DIFP) <a id="depositor-workflow-profile-difp"></a>

OVERVIEW
In this program, you set up your workflow profiles. A workflow profile is a sequence of steps or “flows” that must be taken for all inbound receiving and outbound shipping. Workflow profiles serve three functions in 
AccellosOne 3PL:
▪ They are a way of time-stamping a task or action (for example, recording the arrival time of a driver). 
▪ They allow you to attach a particular document to a particular step in the sequence and require the operator to print that document before proceeding to the next step.
▪ They allow you to specify after which flow you want AccellosOne 3PL to perform allocation and deallocation.
The workflow profile that you create in this program is attached to the program CUST (Customer Code). You can set up one workflow profile for all your customers or you can set up separate workflow profiles for certain customers as required. You can also attach workflow profiles to consignees and shippers. Workflow profiles attached to consignees and shippers will override the workflow profile attached to the customer.
For example, if you set up two workflow profile codes — STD and ABC — and attach your STD code to customer 1 and your ABC code to consignee 1, the following will occur. When shipping customer 1’s product to consignee 1, AccellosOne 3PL will use the flows defined in workflow profile ABC. When shipping customer 
1’s product to any other consignee, AccellosOne 3PL will use the STD workflow profile.
There are four mandatory flow codes that are preloaded into your system and must be included in any workflow profile:
Inbounds
TIP The more flow codes that you use, the better you will be able to track and timestamp your inbound and outbound shipments. However, numerous flow codes will require more input on the computer.
PREREQUISITES: FLPR, DOCU (set up by HighJump)
ATTACHED TO: CUST (Customer Code)
CONS (Consignees)
SHIP (Shippers)
CCCC (Outbound Process Configuration)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The steps that you follow for your inbound receiving and outbound shipping and the documents that are printed at each step

ENRE (Enter Receipt)
CORE (Confirm Receipt)
Outbounds
ENOR (Enter Order)
COOR (Confirm Order)
These codes are mandatory and cannot be changed or deleted. You must use ENRE and CORE in all your inbound workflow profiles and ENOR and COOR in all your outbound workflow sequences. In addition to the four basic flows, you can add any of the standard preloaded flow codes in FLPR to any point in your workflow sequences; for example, you can add new flows to your inbound workflow sequence after ENRE and before or after CORE.
Flow codes and documents are assigned a number to indicate their sequence in the flow. You can have a total of 99 flows and 99 documents for any given inbound workflow sequence as well as 99 flows and 99 documents for any given outbound workflow sequence. When adding new sequence numbers to your profile, it is best to use multiples of five or ten (10, 15, 20, 30, etc.) so that you can insert new flows in your sequence at a later time.
OVERRIDING THE CUSTOMER DIFP PROFILE
The DIFP profile attached to the customer in CUST is the default DIFP profile for that customer. You can override this default in SHIP (Shippers), CONS (Consignees) and CCCC (Outbound Process Configuration). 
The override logic works as follows:
▪ for receipts, the DIFP profile in SHIP (if any) overrides the default profile in CUST
▪ for orders, the DIFP profile in CONS (if any) overrides the default profile in CUST and the DIFP profile in 
CCCC (if any) overrides the DIFP profile in CONS
FIELD DESCRIPTIONS
Workflow Profile Code Mandatory
Your code for this profile. For example, ABC for Customer ABC or STD for 
Standard.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each flow, the documents if any attached to the flow as well as any special verify programs.
Description Mandatory
Your description for this workflow profile code.

Sequence Mandatory
The position of the flow code in your flow sequence.
Flow Code (defined in FLPR)
Mandatory
The flow code.
Mandatory Y = Yes
N = No
If you specify Y for Yes, you must perform the flow in CHRF (Time Stamp and 
Confirm Receipt) or CHOF (Time Stamp and Confirm Orders). If you specify 
No, you can bypass the flow.
Assign Location Y = Yes
N = No
I = Inventory Only (outbound)*
If you specify Yes, the allocation routine will assign locations for a receipt or an order after you have completed that flow. If you specify No, no allocation will occur after that flow. The Yes option is available for any inbound flow except 
CORE and any outbound flow except COOR. 
The Yes option is mandatory for at least one inbound and one outbound flow. 
If required, you can use the Yes option for multiple flows. For example, you perform initial allocation for an order at Flow 3 and then wish to rerun allocation at Flow 5 because new product has been received that will enable you to fill an order line.
* See “Inventory Only Allocation” in Allocation and Wave Manager Guide.
Deassign Location Only available for outbound flows
Y = Yes (Only available if Assign Location = Yes)
N = No
This field allows you to specify the flow(s) at which you can perform manual de-allocation. If you specify Yes, you can manually de-allocate an order in 
DEOR after you have completed that flow. If you specify No, you cannot manually de-allocated an order after that flow. The Yes option is not available for 
COOR (Confirm Order).
FIELD DESCRIPTIONS

DOCUMENT BLOCK
In this block, you define the document(s) that you want to print at a particular flow. If you do not want to print any documents at a particular flow, leave this block blank for the flow.
Labor Standard Code See the Operational Board section in the Operations 2 Guide.
UOM See the Operational Board section in the Operations 2 Guide.
Modifier See the Operational Board section in the Operations 2 Guide.
Alert Time See the Operational Board section in the Operations 2 Guide.
Create DRMS Reserved for future use
FIELD DESCRIPTIONS
Sequence Mandatory
The sequence of the document within the flow that you specify in the Flow 
Block.
Document Code (defined in DOCU)
Mandatory
The document that you wish to print. If you are using directed put-away, you must specify at least one document in your inbound flow sequence. If you are using directed picking, you must specify at least one document in your outbound flow sequence (unless you assign locations to orders in ASOR).
These restrictions do not apply to RF put-away and picking.
Form Code (defined in 
FORM)
Mandatory
The document’s form code. The form code determines the paper size, the number of horizontal lines on a page before a page break and the page’s orientation.
FIELD DESCRIPTIONS

SPECIAL VERIFICATION BLOCK
This block contains advanced programs and customized functions that can be added to any stage in your inbound or outbound procedure. See the System Administration Guide for instructions on setting up special verify programs.
PROCEDURE
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to see which workflow profiles have been already set up. 
3 If the workflow profile that you need is already set up, click on Exit to exit the program.
If, however, the workflow profile that you need is not set up, click Create Record. Then key in a unique code and description for the profile (for example, STD for Standard) and press Enter.
Type R = Regular
If you specify Regular, AccellosOne 3PL requires you to print this document before proceeding to the next step. Regular is the default or preset value in this field. 
O = Optional
If you specify Optional, you can bypass the printing of this document.
A = Automatic
If you specify Automatic, the document will be printed automatically after a specific flow. See the “Faxing and Auto-Printing” section in the Operations 2 
Guide for further information on this option.
P = Printer (sequences 1 and 90 only)
If you specify Printer, you can select your printer from a pop-up menu when you exit ENRE, ENOR or any confirmation program. After you select your printer, the document will be printed automatically. This option requires special programming by HighJump. 
FIELD DESCRIPTIONS

Depositor Workflow Profile showing two default flows for inbound receiving
You will see the two standard flows for inbound receiving: ENRE and CORE. These flows are mandatory and cannot be deleted.
4 If you are using the active locator system for inbounds, you must set the Assign Location flag to Y for one flow in your inbound profile. 
If you are using the default setup of ENRE and CORE, set the Assign Location flag to Yes for ENRE to specify that you want allocation to take place after ENRE and before CORE. You set this flag to Yes by pressing Enter until your cursor is positioned on the next line. AccellosOne 3PL will automatically change 
N to Y for the flow ENRE.

If you are adding additional flows to your profile, you can program the allocation routine to run after any of your new flows.
5 If you have one or more documents such as a receiving tally or a notice that require setup for your inbound flow sequence, position your cursor in the appropriate Sequence field. 
For example, if you wanted to attach a document to flow code ENRE, you would position your cursor in flow sequence 1; alternatively, if you wanted to attach a document to flow code CORE, you would position your cursor in flow sequence 90.
6 Click on Document Block to enter the Document Block.
7 Key in the sequence number of the document (for example, 10) and press Enter. 
8 Key in your document code and press Enter. If you do not know the code of the document that you wish to have printed, you can select it from the pick list. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
9 In the Form Code field, key in your form code and press Enter or use the pick list function to select the appropriate form.
10 Key in your document type (R for Regular, O for Optional, A for Automatic or P for Printer) and press 
Enter.
Adding New Flows to the Flow Block
a) With your cursor in the Sequence field of the Flow Block, click on Create 
Record to create a blank line.
b) Key in a sequence number for the new flow that corresponds to where in the sequence you want the flow to take place and press Enter. 
c) Key in your flow code and press Enter or select your code using the pick list.
d) Set the Mandatory flag to Yes or No for your new code and press Enter. If you set it to Yes, the operator will be forced to perform the flow. If you set it to No, the operator can bypass the flow.
e) Set the Assign Location flag to the appropriate value and press Enter. If set to 
Yes, AccellosOne 3PL will perform allocation after this flow.
f) Set the Deassign Location flag to the appropriate value and press Enter. If set to Yes, AccellosOne 3PL will perform deallocation after this flow.
g) Press Enter three times to bypass the Labor Standard Code, Alert Time and 
Create DRMS fields.
h) Click on Return to Main to exit create mode or repeat the above steps to add another flow.

Depositor Workflow Profile showing one document requiring printing after DRAR
11 If you need to add a second document, repeat steps 8 to 11. When you finish attaching your documents to this flow code, click on Return to Main and then Flow Block to return to the Flow Block.
12 If you wish to attach documents to another flow code, position your cursor in the Sequence field corresponding to the desired flow code. Then click on Document Block for that flow code and enter your document codes.
13 When you finish defining your inbound flow sequence, click on Return to Main and then Exit exit the program.
See the next section for information on setting up your outbound flow sequence.
SETTING UP YOUR OUTBOUND FLOW SEQUENCE
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to display the first profile on your system.
3 Use your arrow keys to locate the profile that you set up for your inbound procedure.
4 When you find it, click on In/Out/Repi/Relo Block.
5 Press your down arrow key to display the outbound record.
6 Follow the steps described previously for your inbound flow sequence to set up flows and attach documents to your outbound procedure. If you are using AccellosOne 3PL’s active locator system for outbounds, you must set the Assign Location flag to Yes for one flow in your outbound sequence.
7 Click on Return to Main and then Exit to exit the program.

### Number Series (NUSE) <a id="number-series-nuse"></a>

OVERVIEW
In this program, you define the series of numbers (lot numbers, pallet ID’s, etc.) to be used by the Depositor 
Inventory Assign Profile (DIAP), AccellosOne 3PL’s auto-lot assignment program. This profile is only required if you want AccellosOne 3PL to generate series of numbers for your lot numbers, pallet ID’s, etc. If you create these numbers yourself or if they are supplied by your customers, you do not use NUSE or DIAP.
You can set up as many different number series as necessary (one for each customer if required). If you assign unique lot numbers for each warehouse, you will need to set up a unique series for each warehouse.
PREREQUISITES: None
ATTACHED TO: DIAP (Depositor Inventory Assign Profile Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you are using the program DIAP
OTHER REQUIREMENTS: The list of numbers that you wish to use for your lot numbers, pallet ID’s, etc.
FIELD DESCRIPTIONS
Number Code Mandatory
Your code for the number series (for example, LOT, PID, BOX, etc.).
Description Mandatory
Your description for the number series.

PROCEDURE
1 Enter NUSE.
2 Key in a number code (for example, LOT, PID or BOX) and press Enter.
3 Key in a meaningful description and press Enter.
4 Key in your starting number and press Enter. 
5 Key in your ending number and press Enter.
6 In the Number to Reserve field, key in your starting number minus 1 and press Enter.
If your starting number = 1, key in 0
If your starting number = 150000, key in 149999
7 Click on Return to Main to exit create mode. AccellosOne 3PL will display the updated record.
Starting Number/Ending 
Number
Mandatory
The starting and ending number for your block of numbers. When AccellosOne 3PL reaches the end of your block of numbers, it will restart at the value that you define in the Start Number field.
NOTE Small ranges (for example, a starting number of 100 and an ending number of 200) are not recommended. If you must use a small range, make sure that you purge your inventory on a regular basis. If you fail to do so, you might have two open receipts with the same lot or pallet ID.
Current Number Calculated by AccellosOne 3PL.
Number to Reserve Mandatory
You can exclude a block of numbers from your number series by entering the appropriate number in this field. For example, if your starting number is 1,000 and you enter 1,050 as your number to reserve, AccellosOne 3PL will reserve the first 50 numbers and start numbering at 1,051.
If you are excluding a block of numbers in create mode, your number to reserve must be greater than your starting number. If you are excluding a block of numbers in modify mode, your number to reserve must be greater than your current number.
If you do not wish to exclude a block of numbers from your number series, you enter your starting number minus 1. For example, if your starting number = 1, key in 0; if your starting number is 150000, key in 149999.
FIELD DESCRIPTIONS

Number Series starting with 150,000
8 Click on Exit to exit.

### Depositor Inventory Assign Profile (DIAP) <a id="depositor-inventory-assign-profile-diap"></a>

OVERVIEW
This program is only required if you want AccellosOne 3PL to generate series of numbers for your lot numbers, pallet ID’s, production dates or other inventory level 2 or higher value. If you create these numbers yourself or if they are supplied by your customers, you do not use DIAP.
PREREQUISITES: WARE, NUSE
ATTACHED TO: DILP (Depositor Inventory Level Profile) --> CUST
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
CHANGE STATUS: Any changes to a profile take effect at the end of the frequency period. If you wish to make changes to your number series that are effective immediately, you must create a new profile and attach it to DILP.
OTHER REQUIREMENTS:

For example, if you want AccellosOne 3PL to assign lot numbers automatically when you enter the receipt, you must set up the parameters for the lot number in this program.
DIAP defines the parameters of the number series that you created in NUSE. You tell AccellosOne 3PL how the numbers are assigned (each time you process a new receipt, each time you process a new receipt line, each time you receive from a new customer, etc.), whether there are any prefixes and suffixes and whether to pad out the numbers with leading zeroes.
The numbers generated by DIAP are always at the next lower level than the level at which you are generating. For example, if you are generating numbers based on item (level 1), the numbers that you generate will be level 2. Likewise, if you are generating numbers based on item (level 1) and production date (level 2), the numbers that you generate will be level 3.
DIAP is attached to the Depositor Inventory Level Profile (DILP). You can create a single DIAP profile for all your customers or create customer specific profiles for those customers with special numbering requirements.
There are a number of options for defining how your numbers are assigned: 
▪ by receipt
▪ by receipt and up to a specified level (1, 2 or 3)
▪ by receipt line
▪ by period of time
▪ by customer over a specified period of time
▪ by period of time up to a specified level (1, 2 or 3)
OPTION DESCRIPTION
Number valid for period of
All customers, all receipts and all product will be assigned the same number for a specified period of time — provided the same DIAP profile is attached to “all” customers.
Number valid for each 
Depositor for period of
Each customer will be assigned a separate number and that number will be assigned to all product received from that customer during a specified period of time. 
Number valid for up to each level 1 for period of
All product with the same level 1 value received over a specified period of time will be assigned the same number.
The number generated will be level 2.
Number valid for up to each level 2 for period of
All product with the same level 1 and level 2 values received over a specified period of time will be assigned the same number.
The number generated will be level 3.
Number valid for up to each level 3 for period of
All product with the same level 1, level 2 and level 3 values received over a specified period of time will be assigned the same number.
The number generated will be level 4.

EXAMPLE 1
Level 1 = Item
Level 2 = Lot Number (system generated based on level 1)
Number valid for = each receipt and up to level 1 
Number valid for each receipt
All product on the same receipt will get the same lot number regardless of level 1 or the customer.
Number valid for each receipt and up to level 1
All product on the same receipt with the same level 1 value will get the same number. When you change level 1 on the same receipt, a new number will be assigned. 
The number generated will be level 2.
Number valid for each receipt and up to level 2
All product on the same receipt with the same level 1 and level 2 values will get the same number. When you change level 1 or level 2 on the same receipt, a new number will be assigned. 
The number generated will be level 3.
Number valid for each receipt and up to level 3
All product on the same receipt with the same level 1, level 2 and level 3 will get the same number. When you change either level 1, level 2 or level 3 on the same receipt, a new number will be assigned.
The number generated will be level 4.
Number valid for each receipt line
Everything on the same receipt line regardless of its level 2 or 3 value will get the same number. When you change receipt lines, AccellosOne 3PL generates a new number.
Number valid for period of
All customers, all receipts and all product will be assigned the same number for a specified period of time — provided the same DIAP profile is attached to “all” customers.
Number valid for each 
Depositor for period of
Each customer will be assigned a separate number and that number will be assigned to all product received from that customer during a specified period of time. 
Receipt Item
Lot Number Generated by System Remarks
001 Item A1 1 new item and therefore new lot number generated
001 Item B2 2 level 1 changes and new lot number generated
OPTION DESCRIPTION

EXAMPLE 2
Level 1 = Item
Level 2 = Lot Number (system generated based on level 1)
Number valid for = each receipt line 
EXAMPLE 3
Level 1 = Item
Level 2 = Production Date
Level 3 = Value # (system generated based on levels 1 and 2)
Number valid for = each level 2 for a period of one month 
001 Item C 3 level 1 changes again and new lot number generated again
001 Item A1 1 more Item A received and original lot number for this item assigned
Receipt Item
Lot Number Generated by System Remarks
001 Item A1 1 new line and therefore new lot number generated
001 Item B2 2 new line and therefore new lot number generated
001 Item A1 3 even though more of item A1 is received, it is received on a new line and therefore a new lot number is generated
Receipt Item
Production 
Date
Value # Generated by System Remarks
01 (Jan 01) TV Dinner 1 040701 427 new item and production date
01 TV Dinner 1 040701 427 same item and production date
01 TV Dinner 1 040730 428 same item but new production date; therefore new value #
02 (Jan 15) TV Dinner 1 040730 428 new receipt but item and production date remain the same; therefore same value #
02 TV Dinner 2 040730 429 item changes but not production date; therefore new value 
#
Receipt Item
Lot Number Generated by System Remarks

03 (Jan 20) TV Dinner 1 040730 428 new receipt but item and production date previously received on Jan 15; therefore use previously assigned value #
FIELD DESCRIPTIONS
Inventory Assign Profile 
Code
Mandatory
Your code for the number series (for example, LOT, PID, BOX, etc.).
Description Mandatory
Your description for the number series.
Name of Function to Generate Lot Number
Optional
You can use PL/SQL to write custom functions to generate inventory 2 or higher values. If you define a function, it will override any setups in the Detail 
Block.
Number Valid for Mandatory
The way in which you wish to assign your lot numbers (by receipt or receipt line, by period of time, by customer, by inventory level, etc.).
Frequency Code Mandatory if you select a time-dependent value in the Number Valid for field
The frequency with which you wish to assign your number series (for example, daily, weekly, monthly, etc.).
Cycle Mandatory if you select a time-dependent value in the Number Valid for field
The number of the units of time defined in the Frequency field that must pass before a new period begins. Refer to the example below for a demonstration of how the Frequency and Cycle fields work.
Receipt Item
Production 
Date
Value # Generated by System Remarks

PROCEDURE
1 Enter DIAP.
2 Click on Enter Criteria then Execute Query to see which profiles have already been set up.
3 If you need to set up another profile, click on Create Record.
Frequency weekly daily monthly
Cycle
Result every week every three days every two months
Whse (defined in WARE)
Mandatory
The warehouse code that this number series applies to. If you wish it to apply to all warehouses, use .ALL.
Number Code (defined in NUSE)
Mandatory
The number series code that you set up in NUSE.
Prefix Optional
A prefix, if any, that you wish to attach to your number series.
Prefix Date Format Optional
If you enter a date format (for example, YDDD, DDMMYY, MMDDYYYY, etc.), the current system date will print on the case pick label.
Suffix Optional
A suffix, if any, that you wish to attach to your number series.
Pad N = No
Y = Yes
If you specify No, the numbers will not be padded out with zeroes (for example, the number 99 will appear as 99 and not 000099). If you specify Yes, the number will be padded out with zeroes if it is less than the maximum number of characters that you defined in NUSE.
FIELD DESCRIPTIONS

4 Key in your profile code (for example, LOT or CUS1) and press Enter.
5 Key in a description for your code and press Enter.
6 In the Number Valid for field, use your pick list to choose the appropriate code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
7 If you selected a time-dependent value in the previous field, you must enter a value in the Frequency field. Use your pick list to choose the appropriate code (daily, weekly, monthly, etc.).
Then enter a number in the Cycle field. The cycle value defines how many of these units of time must pass before a new period begins. Key in the number of days, weeks, months, etc. for the frequency that you selected and press Enter.
8 In the Detail Block, key in the warehouse code that this profile applies to and press Enter or use .ALL for all warehouses.
9 In the Number Code field, key in your number code and press Enter or use your pick list to select it.
10 If required, key in a prefix for the number and press Enter or press Enter with this field blank to bypass it.
11 If required, key in a prefix date format for the number and press Enter or press Enter with this field blank to bypass it.
12 If required, key in a suffix for the number and press Enter or press Enter with this field blank to bypass it.
13 In the Pad field, key in Y for Yes to pad or zero fill the number and press Enter or press Enter to accept the value of No.
14 If required, key in another line in the Detail Block for a second warehouse and repeat the above steps or click on Return to Main to exit create mode.
Depositor Inventory Assign Profile screen with the number valid for each receipt and up to level 2
15 Click on Master Block and Exit to exit the program.

Depositor Inventory Assign Profile screen with the number valid for each receipt and up to level 1

### Depositor Level Validation Profile (DLVP) <a id="depositor-level-validation-profile-dlvp"></a>

OVERVIEW
This program allows you to define acceptable values for any level 2, 3 and 4 entry (that is, those lot numbers, serial numbers, date codes, etc. that you want to accept). During receipt entry, AccellosOne 3PL will perform level validation and will reject any item whose lot number, serial number, date code, etc. does not match the acceptable values that you defined in DLVP. 
EXAMPLE
You define a two-level customer as follows:
Level 1 = ITEM
Level 2 = LOT
In DLVP you specify that the only valid values for LOT are 111 and 999. During receipt 
PREREQUISITES: CUST, ITEM
ATTACHED TO: DILP (Depositor Inventory Level Profile) --> CUST
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

entry, if the operator enters a lot number other than 111 or 999 for any item belonging to that customer, the receipt will be rejected.
The acceptable values that you set up in DLVP can apply to a single level of inventory or to a number of levels. You need to set up a separate profile for each level of inventory that you wish to verify; therefore, if you are verifying two levels of inventory, you must set up two different profiles. 
Level verification can apply to all of a customer’s items or to only certain of a customer’s items. If level verification is item specific, you must specify in DLVP the items to which level verification applies. Items must be set up in ITEM before you can attach them to DLVP.
In the Depositor Inventory Level Profile (DILP), you attach your DLVP profile to the level of inventory to which it applies.
NOTE You can also perform level verification in the Partition Block in ITEM.
FIELD DESCRIPTIONS
Level Validation Profile 
Code
Mandatory
Your code for this profile.
Description Mandatory
Your description for the profile.
Level Code Mandatory
The lot number, serial number or date code that you wish to accept.
Description Mandatory
A description for your level code.

PROCEDURE
1 Enter DLVP.
2 Key in a meaningful level validation profile code and press Enter.
3 Key in a description for your code and press Enter.
4 In the Level Block, click on Create Record.
5 In the Level Code field, key in the lot number, serial number or date code that you wish to accept and press Enter.
6 Key in a description and press Enter.
Restrict N = No
Y = Yes
If you specify N for No, the restriction applies to all of a customer’s items and no further input is required. If you specify Y for Yes, the restriction applies to certain items only. The Yes option requires you to enter those items in the Item 
Block.
Customer Code Mandatory if you set the Restrict field to Yes
The customer of the item(s) that you wish to verify.
Item Code Mandatory if you set the Restrict field to Yes
The item(s) that you wish to verify.
FIELD DESCRIPTIONS

7 In the Restrict field, key in N for No if the restriction applies to all of a customer’s items or Y for Yes if the restriction applies only to certain items. Then press Enter.
Depositor Level Validation Profile with two items defined for level code 103
8 When you finish entering all the items that the restriction applies to, click on Return to Main to exit create mode.
9 Click on Master Block and Exit to exit the program.
If you enter N for No in the 
Restrict field:
If you enter Y for Yes in the 
Restrict field:
a) If required, key in another line in the Level Block for an additional lot number, serial number or date code that you wish to accept and press Enter.
b) When you finish entering all the lot numbers, serial numbers or date codes that you wish to accept, click on Return to Main to exit create mode. Then click on 
Master Block and Exit to exit.
a) In the Item Block, click on Create 
Record.
b) Key in your customer code and press Enter or use your pick list to select it. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
c) Key in your item code and press 
Enter or use your pick list to select it.
d) Press Enter to accept the value of Y in the Correct field.
e) Repeat the above steps for each item that the restriction applies to.

DELETING A LINE IN THE ITEM BLOCK
1 Enter DLVP.
2 Retrieve the profile containing the line that you wish to delete.
3 Position your cursor over the record that you wish to delete.
4 Cl.ick on Delete Record to delete the line.
5 Click on Return to Main to exit create mode.
6 Click on Master Block and Exit to exit the program.

### Inventory Terminology (INTE) <a id="inventory-terminology-inte"></a>

OVERVIEW
In this program, you set up your inventory terminology for your levels of inventory. A level of inventory in 
AccellosOne 3PL refers to the ways in which you wish to identify an item for tracking and billing purposes. For example, lot number, serial number, expiry date, color, model #, pallet ID, etc. are considered inventory levels in AccellosOne 3PL.
In INTE you define your inventory terminology — that is, what you want to call your inventory levels. In DILP you actually set up the inventory levels themselves. The inventory terminology that you create in this program will appear on most reports, invoices and documents produced for your customers.
You must create one inventory terminology code for each level of inventory that you wish to track. Since different customers may have different tracking requirements, you may need to set up different codes for different customers. For example, if one of your customers uses the term “Pallet ID” while another customer uses the term “Pallet #”, you could set up two INTE codes to reflect the difference in terminology among your customers.
PREREQUISITES: None
ATTACHED TO: DILP (Depositor Inventory Level Profile) --> CUST
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE The INTE code “ITEM” is a system code and cannot be deleted, modified or translated. However, you can customize the description of item as required (for example, ITEM = Item Code or SKU Number, etc.). The description of ITEM that you specify in this program will apply to all customers on your system.

PROCEDURE
1 Enter INTE.
2 Click on Enter Criteria then Execute Query to view the inventory terms already set up.
Inventory Terminology
3 Using your arrow keys, go through each record to see which inventory terminology codes have already been set up. If the codes that you require have already been set up, click on Exit. There is no need to add any new codes to INTE.
4 If the inventory terminology codes that you require have not been set up, click on Create Record.
FIELD DESCRIPTIONS
Code Mandatory
Your inventory terminology code. For example, LOT for lot number or PID for pallet ID.
Description Mandatory
Your description for the code.
RF If you do not set up inventory terminology codes for RF (for example, LT for 
Lot instead of L2), AccellosOne 3PL will use the system defaults: L1 for Level 
1, L2 for Level 2, L3 for Level 3 and L4 for Level 4.
RF terminology applies to the following RF programs: RFCH, RFPU, RFPIC, 
OLOP and RFRL.

5 Key in your new inventory code and press Enter.
6 Key in a meaningful description for the new code and press Enter.
7 If required, key in your custom RF terminology and press Enter or press Enter with the field blank to bypass the RF field.
8 Repeat steps 5 to 7 for each additional code that you wish to add.
9 When you finish entering your codes, click on Return to Main and then Exit to exit the program.

### Depositor Inventory Level Profile (DILP) <a id="depositor-inventory-level-profile-dilp"></a>

OVERVIEW
In this program, you set up your inventory levels. Inventory levels are the different ways that you wish to use for identifying an item for tracking and billing purposes (for example, lot number, serial number, expiry date, color, etc.). The inventory level profile makes it possible to customize the number of levels for each customer.
You can have a maximum of four inventory levels in AccellosOne 3PL. Level 1 is always Item but levels 2, 3 and 4 can be anything that you define. 
The chart below illustrates different setups for a customer depending on the way in which you want to track that customer’s product.
You can track product at one level and bill at another or you can track and bill at the same level. For example, consider the following customer:
PREREQUISITES: INTP, INTE, CHAR, NUSE, DIAP, DLVP
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you wish to make changes to an inventory level profile after attaching it to a customer, you must contact HighJump for assistance. This is a billable service if the customer has inventory and history records.
OTHER REQUIREMENTS: You must know how each of your customers is to be tracked and billed
Level 1 = Item
Level 2 = Serial Number
Level 1 = Item
Level 2 = Lot Number
Level 3 = Color
Level 1 = Item
Level 2 = Product Date Code
Level 1 = Item two-level customer three-level customer two-level customer one-level customer

Customer A
Level 1 = Item (this is mandatory)
Level 2 = Lot Number
Level 3 = Pallet ID
In this example, you are tracking by three levels — item, lot number and pallet ID. If you bill at level 1 (Item), lot numbers and pallet ID will not be broken out on invoices and separate charges will not be generated for lot numbers or pallet ID’s. If, on the other hand, you bill by lot number, then item and lot number (but not pallet 
ID) will be broken out on all invoices and charges will be generated for different lots.
In DILP you can also set up:
▪ what you want to call a particular level (that is, the inventory terminology)
▪ the level at which you wish to perform level validation (if you have created a level validation profile in 
DLVP)
▪ the level at which you wish AccellosOne 3PL to generate lot numbers (if you have created a number series in NUSE and a profile for this number series in DIAP)
▪ the format of item codes, lot number, serial numbers, etc.
▪ the level at which you wish to charge initial and renewal storage
▪ your minimum charges for initial storage, renewal storage and handling
A customer can have only one depositor inventory level profile. If you need more than one profile for a customer, you must create two customers.
In DILP, you set the maximum number of levels for a particular profile. The profile is then attached to a customer in CUST. Individual items belonging to that customer can have fewer than the maximum number of levels defined in DILP but can never have more than the maximum.
NOTE Inventory levels are different ways of describing what a particular item is (item x, serial number y, lot z, expiry date whatever, etc.). They do not define the quantity of the item. The quantity of an item is given by the quantity breakdown (pallet/20 cases/50 eaches) defined in IQBP (Item Quantity Breakdown Profile).
For example, a given item has two levels: ITEM and PALLET ID. The quantity breakdown is PALLETS/CASES/EACHES. If you wanted to track the item, you would use the PALLET ID. If you wanted to count how much of the item you had in your warehouse, you would count the number of PALLETS (a SKU type), not the number of 
PALLET ID’s (an inventory level).
TIP If you have minimum charges for initial storage, renewal storage, handling, etc., do not attempt to set them up when you first create your DILP profile. Instead, use your No Charge charge code that you set up in CHAR. Later, when you set up other charge codes in Part IV of this manual, you can go back to DILP and adjust your minimum charges if required.

FIELD DESCRIPTIONS
Inventory Level Profile 
Code
Your inventory level profile code.
Description Your description for the code.
Inventory Terminology 
Code (INTE)
Mandatory
The name of the inventory level as it will appear on reports, invoices and documents produced for your customers. For level 1, AccellosOne 3PL assigns the code ITEM automatically and this code must not be changed. For subsequent levels, you can select from a pick list.
Assign Description to 
New Entity
Only available for level 2 or higher
N = No
Y = Yes 
This field allows you to manually enter a description for each receipt line in the program ENRE. If you set this field to Y for Yes, you must enter a description for the receipt line at the level that you specify.
For example, if you are setting up a three-level customer with item, model number and serial number who also requires a meter read to be tracked, you can track the meter read by means of the this field.
You put in Y in the this field for your second level (model number). When receiving product, you will be prompted to enter not only the item and model number, but also a second level description (your meter read). Then you will be prompted to enter your third level (serial number).
Assign Value to New 
Entity
Reserved for future use

Sequential Entry Only available for level 2 or higher
A = Receipt Entry
B = Order Entry
C = Receipt/Order Entry
D = RF Receipt Entry
N = None
This field allows you to avoid repetitive entry of the same information when entering a receipt or order. You enter your highest inventory levels (for example, levels 1 and 2) once and these levels are automatically attached to lower inventory levels (for example, level 3).
For options A, B, and C, refer to “Sequential Entry Receipts” in the Operations 
1 Guide for further information on this field.
Singleton Entry Reserved for future use 
Item Minimum Shipping 
Level Flag
Only available for level 2 or higher
N = No
Y = Yes
If you specify No, this function is deactivated. If you specify Yes, IMSL (Item 
Minimum Shipping) will be activated. This program allows you to specify minimum level 2, 3 and 4 values (outbound picking only). Refer to Allocation and 
Wave Manager Guide for further information on IMSL.
FIELD DESCRIPTIONS

Method of Generating/
Validating Values
A = Arbitrary (default)
D = Depositor
W = Warehouse (level 2 or higher only)
V = Validate (level 2 or higher only)
This option allows you to define the valid format for any inventory level. For example, if you have a customer whose item codes always begin with the letters BA, you can define the item code format such that an item code that does not conform to this format is rejected. For example, should you try to create a new item code in ITEM starting with XY, AccellosOne 3PL will not allow you to do so.
If you use this option for other inventory levels such as lot numbers or pallet 
ID’s, validation will occur in ENRE (Enter Receipts). You define the format in the Assign Block of DILP.
A = Arbitrary
Validation for item codes and inventory levels is switched off.
D = Depositor
This option is used if you wish to define the valid format for any inventory level in the Assign Block of DILP. If you use Depositor for inventory level 1 or item, validation will occur when you set up a new item in ITEM. If you use Depositor for level 2 or higher, validation will occur during receipt entry.
W = Warehouse (level 2 or higher only)
This option is only used if you have set up NUSE (Set Up Number Series) and 
DIAP (Depositor Inventory Assign Profile). When you specify W for Warehouse, AccellosOne 3PL will automatically generate lot numbers, pallet ID’s, etc. upon receiving product. 
V = Validate (level 2 or higher only)
This option is only used if you have set up a profile in DLVP and wish to perform level validation.
Inventory Assign Profile 
Code (DIAP)
Mandatory if you set the Method of Generating/Validating Values field to W for 
Warehouse 
The profile that you defined in DIAP will be attached to the inventory level that you specify.
FIELD DESCRIPTIONS

BILLING RELATED FIELDS
The Charge Initial and Renewal Storage field must be set to Yes for one of your inventory levels even if you do not use AccellosOne 3PL for billing. 
For whichever level you set this field to Yes, you must enter valid charge codes in all the minimum charge code fields (Billing Entity, Renewal Storage, etc.). If there is no minimum charge for a field, use NC for No 
Charge in the field. If you are not using AccellosOne 3PL for billing, set all these fields to NC.
Point at Which Values 
Generated
Mandatory if you set the Method of Generating/Validating Values field to W for 
Warehouse 
L = Line
E = Entry
R = RF
If you specify Line, the numbers defined in NUSE and DIAP will be generated when you finish a given receipt line in ENRE and start entering the next line. 
If you specify Entry, the numbers will be generated immediately — that is, before proceeding to the Quantity field in ENRE for a given receipt.
If you specify RF, the numbers will be generated when you process a given receipt in RFCH. Numbers in RF can only be generated at the lowest inventory level.
Level Validation Profile 
Code (DLVP)
Mandatory if you set the Method of Generating/Validating Values field to V for 
Validate
You select an appropriate profile from DLVP by using your pick list.
NOTE If you do not have a charge code of NC for No Charge on your system, you must create one in CHAR before you set up your depositor inventory level profile in 
DILP.
FIELD DESCRIPTIONS

FIELD DESCRIPTIONS
Charge Initial and 
Renewal Storage
In this field, you specify the inventory level at which you want AccellosOne 
3PL to charge. One and only one of your inventory levels must have this field set to Yes.
For example, suppose you have a customer with two levels of inventory:
1) item 
2) lot
If you wanted to charge at the lot level, you would set this field to Yes when you set up level 2. If you wanted to charge at the item level, you would set this field to Yes when you set up level 1.
If you charge at the lot level, AccellosOne 3PL will show one charge for each lot on a given invoice. If you charge at the item level, AccellosOne 3PL will show one charge for each item on a given invoice.
Billing Entity Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for that level 
See the Billing and Invoicing Guide.
Renewal Storage Line 
Minimum Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for that level
See the Billing and Invoicing Guide.
Initial Storage Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for that level 
See the Billing and Invoicing Guide.
Handling Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for that level 
See the Billing and Invoicing Guide.

CREATING A LEVEL 1 PROFILE
1 Enter CHAR (Charge Codes) and make sure that you have a charge code of NC for No Charge.
2 Enter DILP.
3 Click on Create Record.
4 Key in a meaningful code for your profile (up to four alphanumeric characters) and press Enter. Then key a meaningful description and press Enter again.
5 When you finish entering your profile code and description, AccellosOne 3PL will automatically set up level 1 as ITEM and fill in the first seven fields of the Level Block. ITEM is a mandatory code for level 1 and should not be changed.

Depositor Inventory Level Profile level 1
6 Select the appropriate value in the Method of Generating/Validating Values field (A for Arbitrary or D for 
Depositor) and press Enter. The Depositor option is only required if you wish to define the format of your item codes, serial numbers, lot numbers, etc.
7 Key in the appropriate Charge Initial and Renewal Storage value and press Enter. If you specify Y for 
Yes, AccellosOne 3PL will invoice at level 1 (Item). If you specify N for No, you must specify a Yes value at another level in the same profile.
8 Key in the appropriate minimum charge codes for the following fields and press Enter.
▪ Billing Entity Minimum Charge Code
▪ Renewal Storage Line Minimum Charge Code
▪ Initial Storage Minimum Charge Code
▪ Handling Minimum Charge Code
If you entered Y for Yes in the previous field (Charge Initial and Renewal Storage), you must enter a valid charge code or a code of NC for No Charge in the above fields.

If you entered N for No in the previous field, you can press Enter to bypass all these fields.

Depositor Inventory Level Profile showing no invoicing at level 1 (ITEM)
9 If you selected Depositor as your method of generating/validating values (step 6), AccellosOne 3PL will now display the Assign Block. Refer to the instructions on the pages that follow for information on what to enter in this block.
If you selected Arbitrary as your method of generating/validating values, AccellosOne 3PL will now display your level 2 screen. Refer to the section below for instructions on creating your second level of inventory (if required). If you are setting up a single-level profile, click on Return to Main to exit create mode. Then click on Master Block and Exit to exit the program.
ADDING A SECOND LEVEL TO A PROFILE
If you are adding your second level at the same time as you are creating your first level of inventory, proceed to step 4.
1 Enter DILP and select the profile to which you wish to add a second inventory level.
2 Click on Level Block.
3 Click on Create Record. AccellosOne 3PL will display level 2.
4 Key in your inventory terminology code and press Enter or use your pick list to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
The code that you enter in this field will be used on all customer-related reports, invoices and documents to describe the level that you are setting up.
5 Key in your Assign Description to New Entity value and press Enter. If you set this field to Yes, you can enter a description for this level on any receipt.

6 Press Enter to bypass the Assign Value to New Entity field.
7 Press Enter to bypass the Sequential Entry field.
8 Press Enter to bypass the Singleton Entry field.
9 Press Enter to bypass the Item Minimum Shipping Level Flag field.
10 In the Method of Generating/Validating Values field, key in the appropriate value (A for Arbitrary, D for 
Depositor, W for Warehouse or V for Validate) and press Enter.
11 If you selected Warehouse in the previous field, key in your DIAP profile in the Inventory Assign Profile 
Code field and press Enter or use your pick list to select it.
Then key in L for Line or E for Entry in the Point at which Values Generated field and press Enter.
12 If you selected Validate in the Method of Generation/Validating Values field, key in your DLVP profile in the Level Validation Profile Code field and press Enter or use your pick list to select it.
13 Key in the appropriate Charge Initial and Renewal Storage value and press Enter. If you select Y for Yes, 
AccellosOne 3PL will invoice at level 2. If you specify N for No, you must specify a Yes value at another level in the same profile.
14 Key in the appropriate charge codes for the following fields and press Enter:
▪ Billing Entity Minimum Charge Code
▪ Renewal Storage Line Minimum Charge Code
▪ Initial Storage Minimum Charge Code
▪ Handling Minimum Charge Code 
15 When you finish entering all your charge codes, AccellosOne 3PL will display level 3. Repeat the above steps for level 3 or click on Return to Main, Master Block and Exit to exit the program.
ASSIGN BLOCK
You use the Assign Block to define the format of your inventory level codes for a particular customer. For example, if you have a customer whose item codes always begin with the letters BA, you can define the item code format such that an item code that does not conform to this format is rejected. 
If your customer tracks by item and serial number, you can define valid formats for both inventory levels. If you define a format at level 1 (item level), item codes that do not match the format will be rejected in ITEM when you try to add a new item. If you define a format at other inventory levels, validation will occur in the 
Enter Receipt program (ENRE) or RFCH.
FIELD DESCRIPTIONS
Partition Number If your item code or lot number can be broken down into distinct parts (for example, AB1234), you can create multiple partitions and define each partition separately. If your codes are uniform (for example, always numbers), you need only define a single partition.
Length of Partition The number of characters in the partition that you want AccellosOne 3PL to do validation on. If you set the Exact Length field to No, you can create item codes, lot number, etc. that exceed the Length of Partition value. However, no validation will occur on these extra characters.

EXAMPLE
If you have an item code of AB1234, you could define your code as follows:
Partition 1 length = 2, valid characters = AB
Partition 2 length = 4, valid characters = 1234 
PROCEDURE
1 Enter DILP and retrieve the profile that you wish to work with.
2 Click on Level Block.
3 Select the level whose code you wish to define.
4 Set the Method of Generating/Validating Values field to D for Depositor and press Enter.
5 Click on Return to Main to refresh your screen.
6 Click on Assign Block.
Exact Length Y = Yes
N = No
If you set this field to Yes, AccellosOne 3PL will perform validation on all characters in the item code, lot number, etc.
If you set this field to No, AccellosOne 3PL will perform validation on the number of characters that you entered in the Length of Partition field. You can add extra characters to an item code, lot number, etc., but no validation on these extra characters will be performed.
NOTE If you have multiple partitions for a particular code, the Exact Length flag should not be set to N for No for partition 1 or 2 and then set to Y for Yes for a partition higher than 1 or 2. Consider the following examples:
Example 1
N
N
N
Example 2
Y
Y
N
Example 3
N
Y
N
Examples 1 and 2 are both valid. However, the value of N for No in the first partition of example 3 will be treated as a Yes.
Valid Characters The characters that you can use in your item code, lot number, etc. Valid characters can be numbers or letters. Special characters such as #, &, %, etc. are not valid. Nor can you use periods, commas or embedded spaces.
FIELD DESCRIPTIONS

7 Key in 1 for partition 1 and press Enter.
8 Key in the length of partition 1 and press Enter.
9 In the Exact Length field, key in Y for Yes or N for No and press Enter.
10 Key in the valid characters for this code and press Enter. 

Depositor Inventory Level Profile — Assign Block
11 If required, repeat the above steps to create a second partition.
12 When you finish defining your codes, click on Return to Main to exit create mode.
13 Click on Master Block and Exit to exit.

### Depositor Item Profile (DITP) <a id="depositor-item-profile-ditp"></a>

PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

OVERVIEW
In this program, you set up the weight measure that you wish to use when looking up the total weight shown on the receipt and order headers. The total weight of the receipt header is shown in the header block of LORE and in the running totals for the entire receipt in ENRE. The total weight of the order header is shown in the header block of LOOR and in the running totals for the entire order in ENOR. 
You also set up the default linear measure (feet, inches, centimeters, etc.) that you wish to use for cube reporting in the Wave Report and in other interfaces.
FIELD DESCRIPTIONS
Depositor Item Profile Mandatory
Your depositor item profile code.
Description Mandatory
Your description for this code.
Record Weight Measure 
Code
Mandatory 
The default weight measure (pounds, kilograms, tons, etc.) that you wish to use when looking up the total weight of the receipt and order headers.
NOTE The unit of measure that you define in DITP applies to the total gross and net weight shown in the order and receipt headers only. All other weights in AccellosOne 3PL (for example, the weight of order and receipt lines, weights shown in LOEN, etc.) are defined at the item level in ITEM.
Record Linear Measure 
Code
Mandatory 
The default linear measure (feet, inches, centimeters, etc.) that you wish to use for cube reporting in the Wave Report and in other interfaces. This linear measure code will override the linear measure code defined at the item level in ITEM.
Track Item Cost Reserved for future use
Number of Item Costing 
Buckets
Reserved for future use
Maintain Item Prices Reserved for future use

PROCEDURE
1 Enter DITP.
2 Click on Enter Criteria then Execute Query to see whether a profile has already been set up. 

Depositor Item Profile
3 If you already have one profile on your system, no further action is required. Click on Exit to exit. If there is no profile on your system, proceed to create one.
4 Click on Create Record to enter create mode. Then in the Depositor Item Profile field, key in your depositor item profile code and press Enter.
5 In the Description field, key in your description and press Enter.
6 In the Record Weight Measure Code field, key in your weight measure and press Enter or select it using the pick list.
7 In the Record Linear Measure Code field, key in your linear measure and press Enter or select it using the pick list.
8 Click on Return to Main then Exit to exit the program.

### Picking Profile (PIPR) <a id="picking-profile-pipr"></a>

PREREQUISITES: None

OVERVIEW
In this program, you define how product will be allocated to orders (if you use directed picking). In PIPR, you can specify:
▪ FIFO (First In First Out) or LIFO (Last In First Out)
▪ absolute FIFO/LIFO (that is, always pick from the oldest or newest lot, then the next oldest/newest lot, etc., etc. and attach relatively less importance to location and capacity factors defined in ILOP) 
▪ relative FIFO/LIFO (that is, pick from a group of the oldest or newest lots and use location and capacity parameters defined in ILOP to make selections within this batch)
▪ the SKU class that you want AccellosOne 3PL to break at when picking partial quantities in ILOP
Refer to the Allocation and Wave Manager Guide for a complete explanation of each picking option in PIPR. 
In the procedure below, you will create an NA (“Not applicable”) code with all the default options.
PROCEDURE
1 Enter PIPR.
2 Click on Create Record.
3 Key in NA as your picking profile code and press Enter.
4 Key in “Not Applicable” as the description of your new code and press Enter.
5 In the Break Quantity at SKU Class field, select the “Ignore SKU classes” option.
6 In the Picking Based on FIFO/LIFO field, key in F for FIFO and press Enter.
7 In the FIFO/LIFO Based on field, use your pick list to select receipt date as your option.
8 Press Enter twice to position your cursor in the Picking Type field.
9 Key in A for Absolute as your picking type and press Enter.
10 Press Enter to bypass the Sort Sequence Code field.
11 In the Replenishment Message on Pick Documents field, key in N for No and press Enter.
12 In the Use FIFO/LIFO for Pick Line Picking or Skip field, key in N for No and press Enter.
13 Press Enter to bypass the Exclude Pick Line Stock When Bulk Picking field.
14 In the Replenishment Based on Eligible Records field, key in N for No and press Enter. 
15 In the Replenish Pick Line up to Level field, key in 1 and press Enter.
16 Press Enter three times to bypass the next three fields.
17 In the Carton Active field, key in N for No and press Enter.
18 Click on Return to Main to exit create record mode.
ATTACHED TO: DSRP (Depositor Shipping & Receiving) --> CUST
ITEM (Item) — optional
CONS (Consignee) — optional
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

Picking Profile screen showing an NA code
19 Click on Exit to exit the program.

### Depositor Shipping & Receiving Profile (DSRP) <a id="depositor-shipping-receiving-profile-dsrp"></a>

OVERVIEW
In this program, you set up the following:
▪ your order line options for an incomplete shipment (regular line vs. pending line)
▪ your default options for processing back orders (if you have insufficient product to fill an order line in 
ENOR, AccellosOne 3PL can create a back order for the missing product)
▪ your default picking profile (PIPR) 
▪ your default put-away profile (PUPR)
PREREQUISITES: PIPR
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

▪ your warehouse restriction options (you can restrict an order line or a receipt line to a specific warehouse) 
This profile is attached to your customers in CUST. If any of the above options differ for certain of your customers, you must set up multiple DSRP profiles.
FIELD DESCRIPTIONS
Shipping/Receiving ProfileMandatory
Your shipping/receiving profile code.
Description Mandatory
Your description.
Ship Only Fully Filled 
Orders
See “Allocating Only Fully Filled Orders” in the Allocation and Wave Manager 
Guide.
Change Zero Pending 
Line to R-Type Line
Only available for P-type order lines in ENOR
Y = Yes
N = No
In this field, you define the type of order line created — Regular or Pending — when there is insufficient product to fill an order line.
EXAMPLE
You receive an order for 20 cases of product X but can only ship 10. 
Change Zero Pending Line to R-Type Line = Yes
If two lots were chosen during allocation, AccellosOne 3PL will generate two regular lines:
1) Lot A ordered = 10 shipped = 10 (Regular)
2) Lot B ordered = 10 shipped = 0 (Regular)
If one lot was chosen during allocation, AccellosOne 3PL will generate one regular line:
1) Lot A ordered = 20 shipped = 10 (Regular)
The order can be confirmed in CHOF or COOL.

Change Zero Pending Line to R-Type Line = No
AccellosOne 3PL will generate one regular line and one pending line:
1) ordered = 10 shipped = 10 (Regular)
2) ordered = 10 shipped = 10 (Pending)
The order cannot be confirmed in CHOF or COOL until the product required is received or the pending line is deleted. 
P.O. Required on Orders Reserved for future use
Allow Back Orders See the back order section in the Operations 2 Guide for further information on this field.
Create Back Orders at 
Allocation
See the back order section in the Operations 2 Guide for further information on this field.
Ship Full Order Quantity See the back order section in the Operations 2 Guide for further information on this field.
Picking Profile Code (PIPR)
Mandatory
The default picking profile for the customer to which this DSRP profile is attached.
Put-Away Profile Code (PUPR)
Optional
The default put-away profile for the customer to which this DSRP profile is attached. The PUPR profile allows you to put-away product to a pick line.
Allow In-Transit Receipts Reserved for future use
FIELD DESCRIPTIONS

PROCEDURE
1 Enter DSRP.
2 Click on Enter Criteria) then Execute Query to see which depositor shipping & receiving profiles have been already set up. 
3 If you need to set up another profile, click on Create Record.
4 Key in a depositor shipping & receiving profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 Press Enter to bypass the Ship Only Fully Filled Orders field.
7 In the Change Zero Pending Line to R-Type Line field, key in Y for Yes or N for No and press Enter.
8 Press Enter to bypass the P. O. Required on Orders field.
9 Press Enter three times to bypass the Allow Back Orders, Create Back Orders at Allocation and Ship Full 
Order Quantity fields.
10 In the Pick Profile Code field, key in your picking profile and press Enter or use your pick list to select it. 
To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
11 If required, key in your put-away profile code and press Enter.
Warehouse Restriction 
Flag
Optional
 = blank
I = Inbound
O = Outbound
B = Both
This field allows you to restrict receipt lines and order lines to a specific warehouse. For example, if you specify I for Inbound, you can enter a warehouse code for any receipt line in ENRE and only locations in that warehouse will be available for that receipt line. If you leave this field blank, no warehouse restrictions will apply at the receipt or order line level.
Order Statistics for 
Grouping
Reserved for future use
Replenishment OptimizationRefer to Allocation and Wave Manager Guide for further information on replenishment optimization.
Allocation of Variable 
Quantity Breakdown 
Items Based on Highest 
SKU Entered
See Allocation and Wave Manager Guide for further information on this field.
FIELD DESCRIPTIONS

12 Press Enter to bypass the Allow In-Transit Receipts field.
13 In the Warehouse Restriction Flag field, key in I for Inbound, O for Outbound or B for Both and press 
Enter or press Enter with the field blank for no warehouse restriction.
14 Press Enter the required number of times to bypass the remaining fields on this screen.

Depositor Shipping & Receiving Profile
15 Repeat the above steps to add another depositor shipping & receiving profile or click on Return to Main and then Exit to exit the program.

### Telephone List Types (TETP) <a id="telephone-list-types-tetp"></a>

PREREQUISITES: None
ATTACHED TO: TELE (Telephone Numbers)
CARR (Carriers)
CUST (Customer Code)
SHIP (Shippers)
CONS (Consignees)
SOLD (Sold-To Codes)

OVERVIEW
In this program you set up your telephone types. A telephone type is any identifying information you wish to attach to one or more telephone numbers belonging to a carrier, customer, consignee or shipper. Telephone types can identify the type of number (for example, FAX, PAGE and MODM), the department to which they belong (for example, CS for Customer Service and TRAF for Traffic) or any other important information (for example, HOME, MAIN, etc.).
Once set up, telephone types allow you to identify at a glance any telephone number listed in the CUST, 
CARR, CONS and SHIP programs.
Telephone types can also be used to print the name of a designated individual on an invoice or bill of lading (for example, ATTN: JIM SMITH). This capability requires special programming by HighJump.
Telephone types are required in all programs in which you enter a telephone number.
PROCEDURE
1 Enter TETP.
2 Click on Enter Criteria then Execute Query to see which telephone types have already been set up.
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Code Mandatory
Your telephone type code.
Description Mandatory
Your description.

Telephone Types
3 If you need to set up another telephone type, click on Create Record.
4 Key in a telephone type code and press Enter.
5 Key in a meaningful description and press Enter.
6 Repeat steps 4 and 5 to add another telephone type or click on Return to Main and then Exit to exit.

### Billing Terms (TERM) <a id="billing-terms-term"></a>

OVERVIEW
In this program, you set up your different terms of payment for your customers. Your terms of payment will depend on the way in which you wish to invoice them (for example, the invoice is due on receipt, within x days of receipt, etc.). The billing terms that you create in TERM will be later attached to your billing profile(s) in 
DBIP. Billing terms will be printed on all AccellosOne 3PL invoices.
AccellosOne 3PL supports a number of different invoicing options:
PREREQUISITES: None
ATTACHED TO: DBIP (Depositor Billing Profile) --> CUST
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You must know the billing terms and the discount percentage (if any) that you offer your customers

▪ you can invoice in installments with each installment assigned a percentage of the total invoice
▪ if invoicing by installment, each installment can be the same percentage of the total invoice or a different percentage of the invoice
▪ you can set the number of days from the receipt date that the invoice is due
▪ you can offer a percentage discount on the total invoice if payment is received within a given number of days
If you do not use AccellosOne 3PL to generate invoices or gather billing information, you do not need billing terms. Set up one billing term code called NA (Not Applicable) and use the following values:
Installment = 1
Percentage of Invoice = 100
Invoice Due After X Days = 1
Discount Percentage = 0.00
Discount Good for X Days = 0
FIELD DESCRIPTIONS
Term Mandatory
Your billing term code. For example, REC for Upon Receipt or 30D for 30 days.
Description Mandatory
Your description.
Installment Number Mandatory
The number of the installment. If there are no installments (that is, the full amount is due), create a single installment.
Percentage of Invoice Mandatory
The percentage of the invoice that you wish to assign to that installment. If you are setting up multiple installments, you can specify a different percentage for each installment. If you are setting up a single installment, use 100 as your percentage.

PROCEDURE
1 Enter TERM.
2 Click on Enter Criteria then Execute Query to see which billing terms have already been set up.
Invoice Due After X Days Mandatory
The number of days from the receipt date that the invoice is due. If you are setting up an NA billing term, use the number 1.
Discount Percentage Mandatory
The discount percentage (if any) for the installment if the customer pays within a specified time period. If there is no discount percentage, use the default value of 0.00.
Discount Good for X 
Days
Mandatory
The number of days that the discount is good for. If there is no discount percentage, use the value 0.
EXAMPLES
Installment Number Percentage of Invoice Invoice Due After X Days Discount Percentage Discount Good for X Days
1 100 5 0.00 0
Example 1 — a single invoice payable in 5 days with no discount
Installment Number Percentage of Invoice Invoice Due After X Days Discount Percentage Discount Good for X Days
0.00
0.00
Example 2 — 2 installments with the first one (60%) payable in 5 days and the second one (40%) payable in 15 days
5.00
0.00
Example 3 — 2 installments with the first one (60%) payable in 15 days with a 5% discount if paid within 5 days and the second one (40%) payable in 30 days with no discount
FIELD DESCRIPTIONS

3 If the billing terms for your customers have already been set up, click on Exit to exit. There is no need to add any new billing terms to TERM. If the billing terms have not been set up, click on Create Record.
4 Key in a code to describe the billing term (for example, REC = Upon Receipt or 30D = 30 Days) and press Enter.
5 Key in a meaningful description for the new term and press Enter.
6 Key in your installment number and press Enter. If there is a single installment, use the number 1.
7 Key in a value for the percentage of invoice and press Enter. 
8 Key in the number of days and press Enter. The number of days is the number of days from the receipt date that the invoice is due.
9 If required, key in a discount percentage and press Enter or press Enter to accept the default value of 
0.00. 
10 If you entered a discount percentage in the previous step, you must specify the number of days that the discount is good for. Key in this value and press Enter. 
11 If you have a second installment to enter, repeat the above steps for installment 2. 

Billing Terms showing two installments
12 When you finish entering all your installments, click on Return to Main to exit create mode. Then click on 
Master Block and Exit to exit the program.

### Holidays (HOLI) <a id="holidays-holi"></a>

OVERVIEW
In this program, you set up your holidays for billing purposes. If you select the Skip Holidays option in DBIP, 
AccellosOne 3PL will automatically bypass renewal billing for the dates entered in this program and bill on the date following the holiday. Should you wish to renew inventory on the holiday, do not set up the date in HOLI.
The dates that you enter in this program must be manually updated each year. 
PROCEDURE
1 Enter HOLI.
2 Click on Enter Criteria then Execute Query to see which holidays have already been set up.
PREREQUISITES: None
ATTACHED TO: DBIP (Depositor Billing Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory if you use the Skip Holidays option for renewal billing in DBIP
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Holiday Code Mandatory
Your holiday.
Date Mandatory
The date of your holiday. The format of this date must match the date format in 
COMP (Company Code).

Holidays
3 If the holidays that you require have already been set up, click on Exit to exit. There is no need to add any new holidays to HOLI. If the holidays that you require have not been set up, click on Create Record.
4 Key in your holiday code and press Enter.
5 Key in the date and press Enter.
6 If you have a second holiday to enter, repeat the above steps for your second holiday.
7 When you finish entering all your holidays, click on Return to Main and then Exit to exit.

### Depositor Billing Profile (DBIP) <a id="depositor-billing-profile-dbip"></a>

PREREQUISITES: CURR, TERM
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You will need to know how your customers are invoiced

OVERVIEW
In this program, you specify the type of invoicing you wish to set up for a customer. There are four invoicing options available depending on the number of invoices that you wish to generate and the charges that you wish to place on these invoices:
In DBIP you also specify:
▪ your billing terms for the customer
▪ your renewal day options
▪ the rate that you wish to charge on renewals
▪ your maximum or minimum charges per invoice, if any, for receipt, renewal and accessorial charges
If your billing is identical for all your customers, you can set up a single profile and attach this profile to each customer. However, if certain customers have special billing terms, you will need to set up multiple billing profiles. If you do not use AccellosOne 3PL for billing, set up one billing profile called NA.
IND three invoices
▪ one for initial storage and handling charges
▪ one for accessorial charges
▪ one for renewal storage charges
UALL one invoice for all charges
UREC two invoices 
▪ one for initial storage, handling and accessorial charges
▪ one for renewal storage charges
UREN two invoices
▪ one for initial storage and handling charges
▪ one for accessorial and renewal storage charges
FIELD DESCRIPTIONS
Billing Profile Code Mandatory
Your billing profile code. For example, IND, UALL, UREC or UREN.
Description Mandatory
Your description.
Currency Code (CURR) Mandatory
The currency code for this profile.

Term Code (TERM) Mandatory
The billing terms for this profile.
Cost Entry N = No
Y = Yes
If you select Yes, you can enter costing charges against an invoice in CTIN (Cost Tracking in Invoice).
Charge Interest N = No
Y = Yes
Set to No. Yes flag reserved for future use.
Check Credit Limit Only available if you use the cash posting system
N = No
Y = Yes
If you set this flag to N for No, no credit limit check will be performed in ENOR. 
If you set this flag to Y for Yes, AccellosOne 3PL will compare the total of all outstanding invoices for a given customer against the customer’s credit limit. If the total of all outstanding invoices is equal to or greater than the customer’s credit limit, you will not be able to create an order for that customer in ENOR.
Credit Limit Only available if Check Credit Limit flag is set to Y for Yes and if you use the cash posting system
The depositor billing profile’s credit limit.
Send Statement N = No
Y = Yes
Set to No. Yes flag reserved for future use.
Single Level Billing See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

Include Day on Renewals N = No
Y = Yes
This flag governs whether transactions occurring on the renewal date are included in the current billing cycle or assigned to the next billing cycle.
If you set this flag to No, transactions that occur on the renewal date will NOT be included in the current billing cycle. You use the No option when you wish to bill on the opening balance of the billing cycle.
EXAMPLE (monthly first of month billing)
You receive 80 cases of product on March 15 and ship out 20 cases on April 
1. The April 1 transaction is NOT included in the current billing cycle and you bill your customer for 80 cases, which is the closing balance for March; the following month, if there are no more transactions, you will bill your customer for the 60 remaining cases (80 minus 20).
If you set this flag to Yes, transactions that occur on the renewal date (that is, up to 11:59 pm on that date) will be included in the current billing cycle. You use the Yes option when you wish to bill on closing balance of the billing cycle.
EXAMPLE (monthly first of month billing)
You receive 80 cases of product on March 15 and ship out 20 cases on April 
1. The April 1 transaction is included in the current billing cycle and you bill your customer for 60 cases (80 minus 20).
NOTE For this option, you should generate and confirm your renewal batch the day after the current billing cycle.
Renew on Day A = Any day
H = Skip holidays (requires setup in HOLI)
W = Skip weekends
S = Skip both
This field allows you to specify whether there are any holidays or special days to be skipped when determining the renewal day. For example, if a product is to renew on Saturday or Sunday and you specify the Skip Weekends option, the product will renew on the following Monday.
If you select the Any day option, product will renew on any day including weekends and holidays.
FIELD DESCRIPTIONS

Original / Current Rate on 
Renewals
C = Current
I = Initial Original
R = Renewal Original
If you select Current, the current renewal storage rate will be charged for renewals even if the current rate differs from the rate in effect when the product was received. If you select Initial Original, the initial storage rate defined in 
IISP when the product was received will be charged for renewals. If you select 
Renewal Original, the renewal storage rate defined in IRSP when the product was received will be charged.
EXAMPLE
A billing entity was first received on Jan. 1 for 1,000 cases. The initial and renewal storage rates were as follows and no product was shipped out of the warehouse in January and February.
IISP charge code = A in RATE
Charge Effective Date = Jan. 1
0 --> 500 cases
501 --> 5000 cases
5001 --> 20000 cases
0001 --> 999999 cases
0.8
0.7
0.6
0.5
IRSP charge code = B in RATE
Charge Effective Date = Mar. 1
0 --> 500 cases
501 --> 5000 cases
5001 --> 20000 cases
20001 --> 999999 cases
0.4
0.3
0.2
0.1
0.6
0.5
0.4
0.3
Original / Current Rate on Renewals = Current
On Feb. 1, AccellosOne 3PL will charge $0.3 per case. On Mar. 1, AccellosOne 3PL will charge $0.5 per case, the current rate in IRSP.
Original / Current Rate on Renewals = Renewal Original
On Feb. 01, AccellosOne 3PL will charge $0.3 per case. On Mar. 1, AccellosOne 3PL will charge the same amount — $0.3 per case. The rate change in 
March has no effect on the rate charged.
Original / Current Rate on Renewals = Initial Original
The rate of $0.7 per case defined in charge code A attached to IISP will be charged on Feb. 1 and Mar. 1.
FIELD DESCRIPTIONS

Rate Qualifier B = Balance (only available if previous field set to C for Current)
O = Original
In this field, you specify which amount — either the balance or the original — you wish to use to determine your per rate. If you select Balance, AccellosOne 
3PL will qualify on the balance as of the renewal date and apply the current rate to the balance. If you select Original, AccellosOne 3PL will qualify on the original amount received and apply the appropriate rate to the original amount.
EXAMPLE
0 --> 5000 lbs
5001 --> 9000 lbs
9001 --> 15000 lbs
15001 --> 999999 lbs
Jan 01
1.00 CWT
.90 CWT
.80 CWT
.70 CWT
Mar 01
1.05 CWT
.95 CWT
.85 CWT
.75 CWT
You receive 35,000 pounds and on renewal day you have 6,000 pounds left. If you select Original, AccellosOne 3PL will qualify on the original amount (35,000 pounds) and apply the appropriate rate (.70 or .75 per CWT). If you select Balance, AccellosOne 3PL will qualify on the balance (6,000 pounds) 
and apply the rate for 6,000 pounds — either .90 per CWT or .95 per CWT.
NOTE If you do not have multiple weight breaks in your rates, AccellosOne 
3PL will always qualify on the original amount.
Send Invoices to C = Customer
P = Paying Office
In this field you specify where you want the invoice sent to. If the customer is paying for his own storage, set this field to C.
If a third party is paying for storage, set this field to P. Then refer to the 
Account Type field in CUST (Customer Code) for further instructions. 
FIELD DESCRIPTIONS

Tax Code Mandatory
GST (GST Only)
GST1 (GST and PST)
GST2 (PST on GST)
HST (HST Only)
None
PST (PST Only)
The taxes, if any, that apply to this profile. With GST1, the GST (Goods and 
Services Tax) and PST (Provincial Sales Tax) are calculated separately and added to the invoice total. With GST2, however, the GST is calculated first and added to the invoice total. Then the PST is calculated based on the invoice total including the GST.
Rate Receipt AutomaticallyY = Yes
N = No
If you set this field to Yes, when the receipt is confirmed AccellosOne 3PL will automatically generate any receipt charges that are applicable. If you set this field to No, confirmation of the receipt will not generate any receipt charges. 
You will be required to go into RCRA (Receipt Rater) and rate the receipt manually.
If you do not use AccellosOne 3PL to generate invoices and track revenue, set this field to N for No.
Invoice Printing Profile 
Code
IND generates a warehouse receipt invoice for initial storage and handing charges, an accessorial invoice for accessorial charges and a renewal invoice for renewal storage charges
UALL generates one accessorial invoice for all charges
UREC generates an accessorial invoice for initial storage, handling and accessorial charges and a renewal invoice for renewal storage charges
UREN generates a warehouse receipt invoice for initial storage and handling charges and an accessorial invoice for accessorial and renewal storage charges
Renewal Summarization 
Code
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

Reserved Quantity Optional
See “Exceed Daily Average Billing” in the Billing and Invoicing Guide.
Minimum / Maximum 
Receipt Charge Code (CHAR)
Optional
See the Billing and Invoicing Guide.
Minimum / Maximum 
Renewal Charge Code (CHAR)
Optional
See the Billing and Invoicing Guide.
Minimum / Maximum 
Accessorial Charge Code (CHAR)
Optional
See the Billing and Invoicing Guide.
Threshold Accessorial 
Charge Code (CHAR)
Optional
See the Billing and Invoicing Guide.
Alternate Billing Group 
Code (ITAS)
Optional
This field allows you to group items for billing purposes; that is, you can bill a customer for a number of items comprising an entire product line rather than each item individually. Alternate billing applies to renewal storage only. See “Alternate Billing Groups” in the Billing and Invoicing Guide for further information.
Surcharge fields Optional
See “Surcharges” in the Billing and Invoicing Guide.
Renewal Invoice by 
Receipt
Optional
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter DBIP.
2 Click on Enter Criteria then Execute Query to see which billing profiles have already been set up.
3 If you need to set up another billing profile, click on Create Record.
4 Key in a billing profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 If you wish to change the default currency code, use your pick list to select the appropriate currency. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code.
7 Use your pick list to select a term code. 
8 Press Enter to bypass the Charge Interest field.
9 Press Enter again to bypass the Cost Entry field.
10 In the Check Credit Limit field, key in N for No or Y for Yes and press Enter.
11 If you enter Y for Yes in the previous field, key in your credit limit and press Enter. 
12 Press Enter to bypass the Send Statement field.
13 In the Single Level Billing field, key in N for No and press Enter.
14 In the Include Day on Renewals field, key in N for No or Y for Yes and press Enter.
15 Select the appropriate value in the Renew on Day field (A for Any Day, H for Skip Holidays, W for Skip 
Weekends or S for Skip Both) and press Enter. If you specify a value other than All, AccellosOne 3PL will skip weekends and/or holidays when calculating renewal storage.
16 In the Original or Current Rate on Renewals field, key in C for Current, I for Initial Original or R for 
Renewal Original and press Enter.
Total Invoices Minimum 
Charge Code
See “Monthly Minimum Billing” in the Billing and Invoicing Guide.
Accessorial Invoice 
Receipt Minimum Charge 
Code
See the Billing and Invoicing Guide.
Accessorial Invoice order 
Minimum Charge Code
See the Billing and Invoicing Guide.
Number of Days Between 
Renewal Invoices
See “Monthly Renewal Invoicing” in the Billing and Invoicing Guide.
Create Renewal Invoice at Zero Inventory
See “Monthly Renewal Invoicing” in the Billing and Invoicing Guide.
Renewal Calculation by 
OPID
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

17 If prompted to do so, key in the appropriate rate qualifier value (O for Original or B for Balance) in the 
Rate Qualifier field and press Enter.
18 In the Send Invoice to field, select either C for Customer (the most common) or P for Paying Office and press Enter.
19 Use your pick list to select the appropriate tax code.
20 In the Rate Receipt Automatically field, select Y for Yes or N for No and press Enter.
21 Select the appropriate invoice printing profile code (IND, UALL, UREC or UREN) and press Enter.

Depositor Billing Profile screen
22 Press Enter to bypass the Renewal Summarization Code field.
23 Press Enter four times to bypass the Minimum / Maximum Receipt Charge Code, the Minimum / Maximum Renewal Charge Code, the Minimum / Maximum Accessorial Charge Code and the Threshold 
Accessorial Charge Code fields.
24 If required, key in an alternate billing group code and press Enter or press Enter to bypass this field.
25 Press Enter to bypass the remaining fields in DBIP.
26 Click on Return to Main and then Exit to exit.

### Depositor Alternate Sorts (DEAS) <a id="depositor-alternate-sorts-deas"></a>

PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)

OVERVIEW
In this program, you define your alternate reporting type codes. These codes are used by the program SALE (12-Month Sales Report) and certain custom reports to generate consolidated inventory reports showing all product of a specific type regardless of customer. For example, if you have seven meat customers and you want to run an inventory report for these seven customers, the report will tell you how much beef, pork and chicken you have in your warehouse.
The codes that you create in this program can be either single level or double level. For example, if you create a code for ICE CREAM, this is considered a single-level code. If, however, you want to track both ice cream in general and particular flavours of ice cream, you would have to break down your ICE CREAM code into VANILLA, CHOCOLATE and STRAWBERRY. This is considered a double-level code.
The codes that you create in this program are attached to the Reporting Block in CUST. When you run the appropriate inventory report and specify an alternate reporting type code, all items belonging to the customers to whom you have attached that code in CUST will be included in the report.
GLOBAL/UNIQUE: Global
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: Custom programming by HighJump
FIELD DESCRIPTIONS
Customer Alternate 
Reporting Type
Mandatory
Your alternate reporting type code.
Description Mandatory
Your description for this code.
Code (Detail Block) Mandatory
If you are creating a single-level code, this code will be identical to the code that you entered in the Alternate Customer Reporting Type field. If you are creating a double-level code (for example, ICE CREAM/ VANILLA), you enter your second level — VANILLA — in this field. 
Description Mandatory
Your description for the code.

PROCEDURE
1 Enter DEAS.
2 Click on Enter Criteria then Execute Query to see which alternate reporting type codes have already been set up.
3 If you need to set up another code, click on Create Record.
4 Key in your alternate reporting type code and press Enter.
5 Key in a meaningful description and press Enter.
6 When the Reporting Codes window appears, do one of the following:

Depositor Alternate Sorts Detail Block showing double-level codes
7 When you finish entering your second-level codes for this reporting type, click on Return to Main and then Exit to exit.
If you are creating a single-level code:
If you are creating a double-level code:
a) Key in the same code and description that you entered in the Main Block and press Enter after each entry.
b) Click on Return to Main to exit create mode. Then click on Master Block and Exit to exit the program. 
c) The Main Block and the Detail 
Block will be identical.
a) Key in your second code and a meaningful description and press 
Enter after each entry.
b) Repeat the above step for each additional second-level code that you wish to add.

### Customer Setup (CUST) — Basic <a id="customer-setup-cust-basic"></a>

OVERVIEW
In this program, you set up your main customer record. A customer in AccellosOne 3PL is a company that owns the goods being stored in the warehouse and pays for their storage. 
In CUST you take the profiles and codes that you have set up in the previous programs and attach them to your customers. You can also set up certain options such as which inventory level you wish to reserve at during order allocation and which default unit of measure you wish to use for entering receipts, orders and adjustments.
The profile fields in CUST are mandatory and once you attach a particular profile to a customer, it can only be changed by HighJump. The optional fields, on the other hand, such as reserving inventory levels and setting default units of measure can be changed as required.
PREREQUISITES: ZIPO, GLCH, DBIP, DSRP, FLPR, SAPE, CUSE, DILP, DIFP, DITP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You will need complete information on your customer — full address, salesperson, customer service representative, etc.

FIELD DESCRIPTIONS
Customer Code Mandatory
Enter a unique code for your customer. For example, if your customer were 
ABC Supplies, you could use the first three characters of the first name and the first three characters of the last name to make up a code of ABCSUP.
A customer code can consist of any combination of numbers or letters up to ten characters in length. Please note the following restrictions on special characters:
▪ The single quote (’) and double quote (") special characters are not valid and should never be used. 
▪ Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. 
▪ The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used.
▪ Other special characters are generally supported.
CAUTION If you are setting up a test customer, the test customer code should always be longer than any live customer codes that are similar. For example, if your live customer code is ABCSUP, you should use ABCSUPT1 as your test company code. If you use ABC as your test customer code, you could purge old data by mistake for both ABC and ABCSUP.
Name Mandatory
The full name of the customer as you would like it to appear on invoices, bills of lading, etc.
Extendable Name This is an overflow field for the Name field when the customer name exceeds 
30 characters.
Address 1 Mandatory
The customer’s street address. This address will print on all documents unless you specify a Paying Office Code as explained further in this section.
Extendable Address 1 This is an overflow field for the Address 1 field when the address 1 exceeds 
30 characters.

Address 2/3/4 Optional
Additional lines for the customer’s street address. This address will print on all documents unless you specify a Paying Office Code as explained further in this section.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (Zip/Postal Code), the city, state/province and country will be filled in by the system.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Salesperson Code (SAPE)
Mandatory
The salesperson responsible for the account.
Customer Service Representative (CUSE)
Mandatory
The customer service representative responsible for the account.
Start Business Date Enter 01.01.01. This date will allow you to backdate any receipts for a customer in ENRE. If you enter the current date, you will not be able to backdate receipts.
G. L. Modifier Code (GLMO)
Optional
If you are using general ledger modifier codes to track revenue by customer, enter the GL modifier code for this customer that you created in GLMO.
FIELD DESCRIPTIONS

Labor Capture Job Level 
Flag
Reserved for future use
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Account Type W = Warehouse
I = Invoice Only
B = Broker
Warehouse
The standard account type for most customers.
Invoice Only
This account type is for customers that are billed only and have no inventory to be tracked (for example, a customer who is renting office space or is shipping and/or receiving goods belonging to another customer).
If you create an invoice only customer, you will not be able to proceed past the 
Billing Profile Code field.
Broker
See the “Broker Orders” section in the Operations 1 Guide for full instructions on setting up a broker.
Billing Profile Code (DBIP)
Mandatory
The billing profile specifying the type of invoicing for this customer.
Paying Office Code Only available if the Account Type = Warehouse and the Send Invoice To field in DBIP is set to P for Paying Office
This field is only used for customers with inventory but no billing because all billing is sent to a third party. See the Billing and Invoicing Guide for full instructions.
FIELD DESCRIPTIONS

UPC Prefix Optional
This field is used to attach a predefined UPC prefix (five digits followed by a hyphen) to all of a customer’s item codes. The use of the prefix eliminates the need to key in the same digits for all items and makes it possible to handle 
UPC codes that are too long for the item code field.
UPC prefixes are typically used for EDI, bar coded labels and special reports that are external to the warehouse. This option cannot be activated without special customization from HighJump.
Freight Paying Office 
Code (FPAY)
Optional
Only required if you wish to bill a customer’s freight charges to a third party when using AccellosOne Transport.
Shipping/Receiving Profile Code (DSRP)
Mandatory
This profile contains your picking profile (set up in PIPR if required) and defines how you want to process orders that cannot be fully filled.
Workflow Profile Code (DIFP)
Mandatory
This profile defines your inbound and outbound flows or steps for time-stamping and allocation/de-allocation purposes.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each flow, the documents if any attached to the flow as well as any special verify programs.
Inventory Level Profile 
Code (DILP)
Mandatory
This profile defines the number of inventory levels and what these levels are called.
Reserve Orders at Level 
Number
RF only
See the reserve logic section in the Allocation and Wave Manager Guide.
FIELD DESCRIPTIONS

Allocate U-Type Line (No 
Location) to R-Type Line
See the reserve logic section in the Allocation and Wave Manager Guide.
Invoices at Inventory 
Level Number
See “Invoicing by Inventory Level” in the Billing and Invoicing Guide.
Consolidation Method for 
Allocated Lines
Optional
See the RF Guide.
Depositor Item Profile 
Code (DITP)
Mandatory
This profile defines the weight measure that you wish to use when looking up the total weight shown on the receipt and order headers as well as the default linear measure code for cube reporting in the Wave Report and other interfaces.
EDI Profile Code Optional
See the EDI section in the Operations 2 Guide.
Freight Profile Code (FRCP)
AccellosOne Transport only
TMS Interchange QualifierFor HighJump use only
TMS Interchange ID For HighJump use only
FIELD DESCRIPTIONS

Default SKU for Receipt 
Entry
H = High
L = Low
In this field, you define how you want AccellosOne 3PL to interpret quantities in ENRE when the SKU type is not specified. This flag works in conjunction with the Receipt Process field in IQBP for each SKU type in an item’s quantity breakdown.
Consider the following example: the item has a quantity breakdown of pallet/ case/each
Receipt Process flag in IQBP for pallets = Y for Yes
Receipt Process flag in IQBP for cases = Y for Yes
Receipt Process flag in IQBP for eaches = N for No
If you enter H for High in CUST and if you enter a quantity of 50 units in 
ENRE, the 50 units will be considered to be 50 pallets. If, on the other hand, you enter L for Low in CUST, the same receipt of 50 units would be recorded by the system as 50 cases. You cannot receive 50 eaches because the 
Receipt Process flag in IQBP for eaches has been deactivated.
You can manually override the default SKU type in ENRE.
Default SKU for Order 
Entry
H = High
L = Low
The same logic as the Default SKU Receipt Entry field but applies to order entry.
Default SKU for Adjustment EntryH = High
L = Low
The same logic as the Default SKU Receipt Entry field but applies to the entry of adjustments.
Extra Charge Profile 
Code (ECHP)
See the Billing and Invoicing Guide for further information.
Voice Profile Code (VOPC)
Only required for voice-activated picking
The customer’s voice profile (customer).
FIELD DESCRIPTIONS

Warehouse Code (WARE)
Optional
The default warehouse code for the customer’s product when assigning locations to receipt lines in ENRE. If you specify a warehouse code in ILOP, the receipt header or a receipt line, that warehouse code will override the warehouse code in this field.
Conveyance Number Reserved for future use
Transfer Profile Code (TRPR)
Optional
This profile is used if you wish to transfer product from one customer to another within your warehouse.
RF Profile Code (MRFP) Optional
This profile is used to set up your RF options.
RFID Partition Reserved for future use
RFID Company Prefix Reserved for future use
Customer EDI Partner ID See the EDI section in the Operations 2 Guide.
EAN UCC Prefix Optional
The EAN UCC prefix for the VICS bill of lading and UCC-128 label.
EAN UCC Number Code (NUSE)
Optional
Your number series for generating UCC-128/SSCC-18 numbers. 
External Reference Number
Optional
You can add any miscellaneous reference information about a customer in this field.
Wave Deallocation Rule See Allocation and Wave Manager Guide.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter CUST.
2 Key in your customer code and press Enter.
3 Key in the full name of your customer and press Enter.
4 Press Enter to bypass the Extendable Name field.
5 Key in the full address of the customer, pressing Enter at the end of each line.
6 Key in your ZIP/postal code and press Enter. If the code is already in AccellosOne 3PL, the city, state or province and country will be filled in automatically. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press 
Enter. You will be brought back into CUST with the appropriate information filled in.
7 In the Salesperson Code field, key in your salesperson code and press Enter or use your pick list to select a code. To select a code using a pick list, press F10 to display the pick list and click on Execute 
Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
8 In the Customer Service Representative Code field, key in the code for your representative and press 
Enter or use your pick list to select a code.
9 Key in 01.01.01 as your start business date and press Enter.
Customer Reference 
Code
Special programming by HighJump required.
Unique Level for Pallet ID In this field, you can define which level is the primary conveyance for RFCH, 
RFPIC, RFRL and RFMG. For example, suppose a given item has four inventory levels with level 3 being Pallet ID and Level 4 being serial number. If you can scan level 3 (Pallet ID), all the serial numbers will be automatically associated with the level 3 that you scanned.
Automatic Billing PreRenewalSee the Billing and Invoicing Guide.
Employee ID Number Reserved for future use
Status A = Active
D = Deactivated
If a customer is active, you can ship and receive product from that customer. If a customer is deactivated, you can ship existing product from that customer but you cannot receive new product from the customer.
FIELD DESCRIPTIONS

Customer Code
10 If you are using the general ledger modifier function, use your pick list to select the code that you created in GLMO for this customer.
11 Press Enter to bypass the Labor Capture Job Level Flag field.
12 Press Enter again to bypass the Labor Standard Modifier field.
13 Key in your account type code (W for Warehouse or I for Invoice Only) and press Enter.
14 Use your pick list to select the billing profile code that you created in DBIP. If you selected an Invoice 
Only account type, you will not be able to proceed past this field and will have to click on Return to Main and Exit to exit.
15 Press Enter to bypass the UPC Prefix field.

Customer Code
16 Press Enter to bypass the Paying Office Code field.
17 If required, key in your freight paying office code and press Enter. If you do not use this feature, press 
Enter to bypass this field.
18 Use your pick list to select the shipping & receiving profile code that you created in DSRP.
19 Use your pick list to select the workflow profile code that you created in DIFP.
20 Use your pick list to select the inventory level profile code that you created in DILP.
21 Press Enter to bypass the Reserve Orders at Level Number field.
22 Press Enter again to bypass the Consolidation Method for Allocated Lines field.
23 Use your pick list to select the depositor item profile code that you created in DITP.
CAUTION Make sure that you select your profiles carefully. Once you attach a profile to a customer, it cannot be removed without special programming by 
HighJump. 

Customer Code
24 Press Enter to bypass the EDI Profile Code field.
25 Press Enter to bypass the Freight Profile Code field.
26 Press Enter twice to bypass the TMS Interchange fields.
27 Press Enter to bypass the Extra Charge Profile field.
28 Press Enter again to bypass the Voice Profile Code field.
29 If required, key in a warehouse code in the Warehouse Code field and press Enter or press Enter to bypass this option.

Customer Code screen showing prompt for default SKU for receipt entry
30 If required, change the default values in the Default SKU Receipt Entry, Order Entry and Adjustment 
Entry fields or press Enter to bypass these fields.
31 Press Enter to bypass the Conveyance Number field.
32 Press Enter the required number of times to bypass the Transfer Profile Code, RF Profile Code, RFID 
Partition, RFID Company Prefix, Customer EDI Partner ID and EAN UCC Prefix fields.
33 If required, key in miscellaneous reference information in the External Reference Number field and press 
Enter. If you do not require miscellaneous reference information, press Enter to bypass this field.
34 When the Receiving Block is displayed, click on Return to Main and then Exit to exit.

### Customer Setup (CUST) — Advanced <a id="customer-setup-cust-advanced"></a>

PREREQUISITES: TETP, CARR, CUST, DEAS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional

OVERVIEW
This chapter describes the more advanced features of CUST. 
▪ Receiving Block
▪ Shipping Block
▪ Reporting Block
▪ Telephone Block
▪ Carrier Block
RECEIVING BLOCK
The Receiving Block displays the inventory levels for your customer. The sequence in which the levels are displayed determines the sequence in which you will enter inventory in the receiving program (ENRE). 
For example, if your inventory levels are set up as follows:
Level 1 = Item
Level 2 = Lot
AccellosOne 3PL will prompt you to enter your item code first in ENRE and then your lot number.
You can change the order in which you receive inventory at any time by changing the order of your inventory levels in the Receiving Block.

Receiving Block
To change the order of your inventory levels:
1 Enter CUST.
2 Retrieve the customer whose inventory levels you wish to resequence.
3 Click on Receiving Block.
OTHER REQUIREMENTS:

4 Change the numbers in the Level column to reflect the order in which you wish to receive your inventory and press Enter after changing each number.
For example, if your current order is:
Item = 1
Lot = 2 you would change Item to 2 and Lot to 1 in order to receive the lot before the item.
5 Click on Master Block and then Exit to exit.
SHIPPING BLOCK
The Shipping Block works in the same way as the Receiving Block. By changing the order of your inventory levels in this block, you change the order in which you enter inventory in ENOR. This feature is only available for P-type order lines.
REPORTING BLOCK
This block is used by the program SALE (12-Month Sales Report) and certain custom reports to group customers with similar product and generate consolidated inventory reports containing all products for a number of customers. For example, if you have seven meat customers and you want to run an inventory report for these seven customers, the report will tell you how much meat you have in your warehouse (a single-level code) or how much beef, pork and chicken you have in your warehouse (a double-level code).
When you run the appropriate inventory report and select an alternate reporting type code, all customers to whom you have attached that code in the Report Block in CUST will be included in the report.

Reporting Block showing two alternate reporting types — COOK (a single-level code) and MEAT (a double-level code)
To add an alternate reporting type code to the Reporting Block:
1 Enter CUST.
2 Retrieve the customer for whom you wish to add an alternate reporting type.
3 Click on Receive Block, Shipping Block and then Report Block.

4 If you are not in Create Mode, click on Create Record.
5 In the Type field, use your pick list to select the appropriate alternate reporting type (first level) that you created in DEAS. Then press Enter to advance to the next field.
6 In the Code field, use your pick list to select the appropriate alternate reporting type (second level) that you created in DEAS and then press Enter to advance to the next line. If there is no second level code, key in the same code that you used in the previous step and press Enter.
7 Key in another line or click on Return to Main to exit create mode. Then click on Shipping Block, Receive 
Block, Master Block and Exit.
TELEPHONE BLOCK
This block allows you to look up the telephone numbers and e-mail addresses for a particular customer. 

Telephone Block
 To add a number to the Telephone Block:
1 Enter CUST.
2 Retrieve the customer for whom you wish to add a telephone number.
3 Click on Receive Block, Shipping Block, Report Block and then Telephone Block.
4 If you are not in Create Mode, click on Create Record.
5 In the Telephone List Code field, use your pick list to select the appropriate telephone type. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
6 Key in the telephone number and press Enter.
7 Key in the name of the contact person and press Enter.

8 If required, key in the person’s position and press Enter. If you do not need the person’s position, press 
Enter to bypass this field.
9 Key in another line or click on Return to Main to exit create mode. Then click on Report Block, Shipping 
Block, Receive Block, Master Block and Exit.
CARRIER BLOCK
This block allows you to list in order of preference the carriers that you wish to use for this particular customer. 
This listing is for reference purposes only; it does not modify the order of carriers during order or receipt entry. 
If you have not set up your carriers yet in CARR, you cannot enter a listing of preferred carriers at this time. 
When you set up your carriers in CARR, you can return to CUST and complete the Carrier Block.
