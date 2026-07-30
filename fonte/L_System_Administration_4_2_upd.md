# Manual L — System Administration Guide (Administração do Sistema)

> **ID do Manual:** L  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Administração: company setup (COMP), programas (EXJO/JOSE), acesso de empresa (COAC), usuários (OPER/OPAC/OPRS), roles (ROMA), ActiveDesktop security (ADSA), archiving/purging (ARPU/DEAR), conversões de dados (DEPC/PRCO).

---

AccellosOne Enterprise 
3PL System 
Administration Guide
June 2016
Release 4.2*

Copyright © HighJump
All rights reserved
This manual is reserved for licensed users of AccellosOne Enterprise 3PL and e-Vista. If you are not a 
licensed user of AccellosOne Enterprise 3PL and e-Vista, no part of this publication may be reproduced, 
stored in a retrieval system or transmitted in any form or by any means electronic, mechanical, recording or 
otherwise, without the prior written consent of HighJump.
The information in this manual is furnished for informational use only, is subject to change without notice and 
should not be construed as a commitment of HighJump. HighJump assumes no responsibility or liability for 
any errors or inaccuracies that may appear in this manual.

SYSTEM ADMINISTRATION GUIDE 4.2* i
TABLE OF CONTENTS
INTRODUCTION ......................................................................... 1
AccellosOne 3PL Documentation Set ............................................................................................ 2
SETTING UP COMPANIES, PROGRAMS AND USERS ...................... 3
Overview ........................................................................................................................................... 5
Setting Up Your Company Code in COMP..................................................................................... 6
Setting Up Your Company Parameters ............................................................................. 11
Setting Up Your Programs in EXJO, JOSE.................................................................................. 35
Setting Up Your Executable Job Codes in EXJO .............................................................. 36
Lock Block ......................................................................................................................... 37
Setting Up Your Job Selection Codes in JOSE ................................................................. 39
Setting Up Submenus in JOSE ......................................................................................... 41
Deleting a Submenu .......................................................................................................... 43
Looking Up a Program’s Path............................................................................................ 43
Looking Up a Program’s Executable Job Code................................................................. 45
Assigning Programs to Companies in COAC ............................................................................. 46
Removing Programs from Companies .............................................................................. 48
Overview of New User Setup ........................................................................................................ 49
Setting Up New Users in OPER .................................................................................................... 49
Setting Up an Operator...................................................................................................... 51
Setting Up an Operator with Supervisor Privileges ........................................................... 52
Deactivating an Operator................................................................................................... 53
Reactivating an Operator................................................................................................... 53
Resetting an Operator’s Password in ROPA..................................................................... 53
Assigning Program Access to Users in OPAC............................................................................ 54
RF Menu Structure ............................................................................................................ 55
Looking Up Submenus ...................................................................................................... 56
Assigning Program Access to a User ................................................................................ 56
Removing a User’s Program Access................................................................................. 59
Copying an Operator’s Access in COOA........................................................................... 60
Entering Operator Restrictions in OPRS ..................................................................................... 62
Customer/Consignee/Shipper/Carrier/Document Tabs ..................................................... 63
Removing Restrictions....................................................................................................... 66
Setting Up Roles in ROMA ............................................................................................................ 67
Deleting a Role .................................................................................................................. 68
Modifying a Role................................................................................................................ 68
Looking Up an Operator’s Roles ....................................................................................... 69

ii 4.2* SYSTEM ADMINISTRATION GUIDE
Setting Up ActiveDesktop Security Administrators in ADSA.................................................... 70
Deleting a Security Administrator ...................................................................................... 71
Setting Up e-Filing Security .......................................................................................................... 71
Removing Document Types and Functions from a Role ................................................... 73
Activating the ActiveDesktop Icons............................................................................................. 74
Modifying Your Installation Parameters in INST ......................................................................... 75
ARCHIVING AND PURGING ........................................................79
Overview ......................................................................................................................................... 80
Setting Up Archiving and Purging................................................................................................ 82
COMP (Company Code) ................................................................................................... 82
OPER (Operator Code) ..................................................................................................... 82
Archiving Receipts, Orders, Inventory and Charges in ARPU .................................................. 83
Archiving Receipts and Orders.......................................................................................... 83
Archiving Inventory ............................................................................................................ 85
Archiving Accessorial and Immediate Charges ................................................................. 87
Looking Up Archived Records...................................................................................................... 88
Looking Up Archived Orders in LOOR .............................................................................. 88
Looking Up Archived Receipts in LORE............................................................................ 89
Looking Up Archived Inventory in LOEN ........................................................................... 90
Looking Up Archived Billing Records in LOEN.................................................................. 91
Looking Up Archive Registers in ARPU ............................................................................ 92
Deleting the Archive in DEAR....................................................................................................... 94
Miscellaneous Purging.................................................................................................................. 96
Purging the Spooler Files in SPPA.................................................................................... 96
Purging Warnings and Messages...................................................................................... 97
Looking Up Warning Messages (WAME)............................................................ 97
Purging Warning Messages (PUWM) ................................................................. 99
CONVERSIONS ....................................................................... 101
Overview ....................................................................................................................................... 102
Creating Your Excel Spreadsheets............................................................................................. 103
Creating Your Flat Files............................................................................................................... 103
Converting Customer Details...................................................................................................... 104
Converting Item Details............................................................................................................... 108
Entering the Quantity Breakdown.................................................................................... 108
Converting Location Details ........................................................................................................118
Converting Existing Locations ................................................................................................... 122

SYSTEM ADMINISTRATION GUIDE 4.2* iii
Converting Consignee Details.................................................................................................... 122
Converting Shipper Details......................................................................................................... 125
Converting Carrier Details........................................................................................................... 127
Converting Transaction History Details..................................................................................... 129
Converting Revenue Master Details........................................................................................... 132
Converting ZIP Codes ................................................................................................................. 133
Converting Inventory Balances .................................................................................................. 134
Converting Billing Information.......................................................................................... 135
Miscellaneous Conversions........................................................................................................ 139
Performing the Conversion......................................................................................................... 139
Step 1 — Loading the Conversion in LOCO.................................................................... 139
Step 2 — Viewing and Modifying the Conversion Data in MOCO................................... 140
Step 3 — Processing the Conversion in PRCO .............................................................. 141
Step 4 — Modifying Conversion Data in MOCO ............................................................. 142
Step 5 — Running COER (Conversion Exception Report).............................................. 143
Step 6 — Verifying the Converted Data .......................................................................... 144
 Transferring Data from One Company to Another................................................................... 144
MISCELLANEOUS PROGRAMS .................................................. 147
Clearing Terminal Locks in CLTL ............................................................................................... 148
Copying Item Codes in COIT....................................................................................................... 149
Adjusting an Item’s Quantity Breakdown in AEQB .................................................................. 150
Reports ............................................................................................................................ 151
Changing the Quantity Breakdown of a Standard Quantity Breakdown Item.................. 151
Changing the Quantity Breakdown of a Variable Quantity Breakdown Item ................... 154
Adjusting Location Billing Codes in ADLB ............................................................................... 157
Adjusting Location Types in ADLT............................................................................................. 159
Changing the Company Date in DATE or ALDA........................................................................ 160
Recalculating Inventory Expiry Dates in REEX......................................................................... 161
Performing Advanced Queries with SQL Statements............................................................... 163
Performing Queries on Multiple Fields ............................................................................ 165
Looking Up Spooler Activity in LOSP........................................................................................ 167
Looking Up Fax Information ............................................................................................ 168
Setting Up Sort Sequence Codes in SOSE................................................................................ 169
Looking Up Your Warehouse Utilization in LOWU.................................................................... 170
Looking Up Your Warehouse Activity in SAM........................................................................... 173
Looking Up Summary Information in SAM ...................................................................... 180

iv 4.2* SYSTEM ADMINISTRATION GUIDE
Working With the Translation Manager in TRMA ...................................................................... 181
Updating a Single Entity .................................................................................................. 183
Performing a Mass Update.............................................................................................. 186
Copying Codes Between Companies in COCO......................................................................... 187
Performing a Mass Update of an Item Value in IMAS ............................................................... 189
Importing Orders and Receipts in IFFI....................................................................................... 190
SPECIAL VERIFICATION PROGRAMS ........................................ 193
Overview ....................................................................................................................................... 194
Looking Up Special Verification Programs in LOSV................................................................. 196
Creating Your Own Special Verification Program in MSVS...................................................... 197
Mandatory Order Accessorials (MOAC)..................................................................................... 198
Mandatory Receipt Accessorials (MRAC).................................................................................. 199
Mandatory Receipt Carrier Details (MRCA) ............................................................................... 200
Mandatory Order Carrier Details (MOCA) .................................................................................. 201
Order Total Quantity Verification (OTQV) .................................................................................. 202
Create Receipt from Order (CRCU) ............................................................................................ 203
Mandatory Order Line Carton ID (MOCI).................................................................................... 203
Update Order To Ship Date (UOTS) ............................................................................................ 204
Order Charges (ORCH)................................................................................................................ 204
Receipt Charges (RECH) ............................................................................................................. 205
INDEX ................................................................................... 207

SYSTEM ADMINISTRATION GUIDE 4.2* 1
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
tracking, interleaving, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory 
level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

SYSTEM ADMINISTRATION GUIDE 4.2* 3
SETTING UP COMPANIES, PROGRAMS 
AND USERS
Overview .............................................................................................................. 5
Setting Up Your Company Code in COMP........................................................ 6
Setting Up Your Company Parameters........................................................ 11
Setting Up Your Programs in EXJO, JOSE..................................................... 35
Setting Up Your Executable Job Codes in EXJO ........................................ 36
Lock Block.................................................................................................... 37
Setting Up Your Job Selection Codes in JOSE ........................................... 39
Setting Up Submenus in JOSE.................................................................... 41
Deleting a Submenu .................................................................................... 43
Looking Up a Program’s Path ...................................................................... 43
Looking Up a Program’s Executable Job Code ........................................... 45
Assigning Programs to Companies in COAC................................................. 46
Removing Programs from Companies......................................................... 48
Overview of New User Setup ........................................................................... 49
Overview of New User Setup ........................................................................... 49
Setting Up an Operator ................................................................................ 51
Setting Up an Operator with Supervisor Privileges...................................... 52
Deactivating an Operator ............................................................................. 53
Reactivating an Operator ............................................................................. 53
Resetting an Operator’s Password in ROPA ............................................... 53
Assigning Program Access to Users in OPAC .............................................. 54
RF Menu Structure....................................................................................... 55
Looking Up Submenus................................................................................. 56
Assigning Program Access to a User .......................................................... 56
Removing a User’s Program Access ........................................................... 59
Copying an Operator’s Access in COOA ..................................................... 60
Entering Operator Restrictions in OPRS ........................................................ 62
Removing Restrictions ................................................................................. 66

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Roles in ROMA ............................................................................... 67
Deleting a Role ............................................................................................ 68
Modifying a Role .......................................................................................... 68
Looking Up an Operator’s Roles.................................................................. 69
Setting Up ActiveDesktop Security Administrators in ADSA ....................... 70
Setting Up e-Filing Security ............................................................................. 71
Activating the ActiveDesktop Icons ................................................................ 74
Modifying Your Installation Parameters in INST ............................................ 75

SETTING UP COMPANIES, PROGRAMS AND USERS
Overview
SYSTEM ADMINISTRATION GUIDE 4.2* 5
Overview
There are three types of setup in AccellosOne 3PL:
 company setup
 program setup
 operator setup
Before you can use AccellosOne 3PL, you must be set up as an operator in OPER and your operator must 
have access to a company set up in COMP. The programs that you wish to use must be set up in JOSE and 
be accessible to the company in which you are working. Lastly, your operator must have access to the 
programs that you wish to use.
If any of these conditions has not been met (for example, your operator does not have access to a company, 
your operator does not have access to a program or the program does not have access to a company), you 
will not be able to enter the program.
EXAMPLE
An operator called BOB wants to enter a receipt in the program ENRE while working in company W1.
The following system flowchart shows the relationships between companies, operators and programs.
Bob has access 
to W1
ENRE accessible 
to W1
Bob has access 
to ENRE Result
Yes Yes No No access
Yes No Yes No access
No Yes Yes No access
Yes Yes Yes Access granted

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Generally speaking, all system administration programs are in company Z1 (AccellosOne 3PL Utilities).
Setting Up Your Company Code in COMP
AccellosOne 3PL is divided into one or more companies. Customers, shippers, consignees, items and 
inventory available in one company may or may not be available in another company. Multiple companies are 
useful when you wish to:
 separate one business unit from another operating out of the same facility
 separate two facilities located in different cities belonging to the same business unit 
COMPANY SETUP
In these programs, you set up your
company information.
COPA COMP
OPERATOR SETUP
In this program, you set up your
operators.
OPER
PROGRAM SETUP
In these programs, you set up your
application programs.
EXJO
JOSE
OPRS
COAC OPAC COOA
In COAC (Company Access), you
assign programs to companies.
In OPAC (Operator Access) or
COOA (Copy Operator Access), you
assign programs to operators.
In OPRS (Operator Restrictions),
you restrict operators to companies.
COPA (Company Parameters)
COMP (Company Code)
OPER (Operator Code)
EXJO (Executable Job Code)
JOSE (Job Selection Code)
or

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 7
 separate test data from live data
You set up your company codes in COMP (Company Code). In COMP, you define the following:
 the company’s name and address
 the company’s date format
 whether the company’s date defaults to the master date
 the company’s global code
 the company’s customer description
NOTE Any changes that you make to COMP do not take effect until the next time 
that you log onto AccellosOne 3PL.
FIELD DESCRIPTIONS
Company Code Mandatory
Company codes consist of a letter followed by a number; for example, W1, 
W2, A4, T6, etc.
Name Mandatory
The name of the company. This name will appear across the top of every 
AccellosOne 3PL screen to identify the company in which you are working.
Address Line 1 Mandatory
The company’s first address line.
Address Line 2/3/ 4 The company’s second/third/fourth address line.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
ZIP/Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (ZIP/Postal Code), the city, state/province and 
country will be filled in by the system.
If the ZIP code or postal code that you enter is not in the system, you will have 
to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by first entering the 
country and the code and then defining the city plus state/province to which it 
belongs.
Date Format Mandatory
The date format for your company. You can choose from MM.DD.YY, 
DD.MM.YY or MON.DD.YY
Default to Master Date Y = Yes
N = No
If you select Yes, the company date of this company will automatically change 
when you change your company dates in ALDA (Change Date for All Companies).
If you select No, the company date of this company will not change when you 
change your company dates in ALDA. 
G.L. Modifier Code Optional
If you are using general ledger modifier codes to track revenue by company, 
enter the GL modifier code that you created in GLMO for this company.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 9
Global Code The value that you enter in the Global Code field determines whether or not 
global codes and profiles created in other companies will be available for use 
in your new company.
To share global programs across companies, you must set the Global Code 
field to the same value for all companies whose codes and profiles you wish to 
share. For example, if you assign the global code of 00 to companies W1 and 
W2 and assign the global code 01 to companies W3 and W4, companies W1 
and W2 will share one set of global codes and profiles while companies W3 
and W4 will share a separate set of global codes and profiles. AccellosOne 
3PL supports up to five global codes: 00, 01, 02, 03 and 04.
If you leave the Global Code field blank, the company is local — that is, any 
global profile is only available to the company in which the profile was set up. 
NOTE Once you set up a global code for a particular company, you cannot 
change it. Should you make a mistake and need to delete or modify the global 
code, contact your HighJump consultant for assistance.
Printer Code Mandatory
The default printer to be used throughout the company for documents. 
Rollup Type N = Not Applicable
C = Child
R = Rollup
See “Rollup Invoicing” in the Billing and Invoicing Guide.
External Reference Number
Optional
An external reference number to be used where required.
Company Reference 
Code
Optional
An external reference number to be used where required.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
1 Enter the appropriate company (usually Z1).
2 Enter COMP.

Company Code (COMP)
3 Click on Create Record.
4 Key in your company code and press Enter.
5 Key in your company name and press Enter.
6 Key in your first address line and press Enter.
7 If required, key in your second, third and fourth address lines.
8 Key in or select from the pick list your zip/postal code. 
9 In the Date Format field, key in your date format and press Enter.
10 In the Default to Master Date field, key in Y for Yes or N for No and press Enter.
11 If you are using general ledger modifier codes to track revenue by company, key in your general ledger 
modifier code for this company and press Enter. If you are not using general ledger modifier codes to 
track revenue by company, leave this field blank.
Auto-Process Sequence 
Number
Optional
This field allows you to sequence the printing of auto-printed documents by 
company. For example, if you set company W1 to 1 and company W2 to 5, 
W1’s auto-printed documents will be printed before W2’s auto-printed documents.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 11
12 Do one of the following:
13 In the Printer Code field, key in your printer code and press Enter.
14 Press Enter to bypass the Rollup Type field.
15 If required, key in an external reference number and press Enter.
16 If required, key in a company reference code and press Enter.
17 If required, key in an auto-process sequence number and press Enter.
18 When you finish entering your company, click on Return to Main.

Company Code (COMP)
19 Click on Exit to exit.
SETTING UP YOUR COMPANY PARAMETERS
You open the Company Parameters window by clicking on Company Parameters.
If you wish to share global codes 
and profiles with another 
company:
If you do NOT wish to share 
global codes and profiles:
a) Key in your global code and 
press Enter.
a) Press Enter to bypass the Global 
Code field.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Outbound tab
FIELD DESCRIPTIONS (OUTBOUND)
Activate Back Orders Yes
No
If you select Yes, the back order system is active and you can
enter a value in the Back Orders at Level Number field in ITSH (Item Shipping 
Profile). If you select No, the back order system is deactivated.
Allow P-Type Lines in 
Order Entry
Yes
No
If you select Yes, you can enter P-type order lines in ENOR.
If you select No, you cannot enter P-type order lines in ENOR.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 13
Allow Multiple Warehouses on Order Confirmation
Single
Multiple
If you select Single and you are shipping product from multiple warehouses, 
you cannot confirm the order in CHOF (Time Stamp and Confirm Orders). 
Instead, you must confirm individual order lines in COOL (Confirm Orders - 
Line
at a Time).
If you select Multiple and you are shipping product from multiple warehouses, 
the above restriction does not apply. You can confirm such orders in CHOF 
(Time Stamp and Confirm Orders) and are not forced to confirm each order 
line individually in COOL.
Generate Order Alerts None
Ship
Order
Both
If you select None, no order alerts will be generated.
If you select Ship, an order alert will be generated whenever the shipped 
quantity is greater than the ordered quantity. If you select Order, an order alert 
will be generated whenever the ordered quantity is greater than the shipped 
quantity.
If you select Both, an order alert will be generated whenever the shipped 
quantity and ordered quantity do not match.
Maximum Number of 
Orders in Batch
The maximum number of consolidated orders in a GEBA batch.
Default Order Type in 
ENOR
The default order type (Regular, Pending, Kit, etc.) for ENOR.
Update Carrier from VICS 
BOL
Yes
No
If you select Yes, the carrier code that you enter in VBOL (VICS Bill of Lading) 
will update the carrier entered in ENOR. If you select No, the carrier code that 
you enter in VBOL will NOT update the carrier entered in ENOR.
FIELD DESCRIPTIONS (OUTBOUND)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Financial tab
FIELD DESCRIPTIONS (FINANCIAL)
Number of Fiscal Periods Reserved for future use.
Use Multiple Currencies See the Billing and Invoicing Guide.
Home Currency Code 
(CURR)
See the Billing and Invoicing Guide.
Financial Interface Code The financial interface code used to link AccellosOne 3PL to your accounting 
system. This field must be set up by HighJump.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 15
Verify Customer’s Credit 
Status
Only available if you use the cash posting system to track payments received 
from customers
Yes
No
If you set this field to Yes and enter a credit limit amount in DBIP for a given 
customer, you will not be able to create a new order for that customer in 
ENOR when the outstanding invoices for that customer exceed the customer’s credit limit.
If you set this field to No, credit status checking will be deactivated.
Number of Decimal 
Places for Billing Calculations
2
3
3
5
6
The number of decimal places for all database columns in AccellosOne 3PL 
relating to charges, invoice amounts and taxes. You can choose any value 
between two and six decimal places in this field.
For example, if you set the Charge Number of Decimal Places to ‘4’ and the 
calculated charge amount is 100.123456, the charge amount being stored in 
the database will become 100.123500. If you set the Charge Number of Decimal Places to ‘2’, this charge amount will become 100.120000.
Regardless of the option that you choose, invoice amounts that print on 
invoices will show only two decimal places.
Department Entry for 
Charges
None
Allow
Require
If you select Allow, you can assign a department code to a manual charge in 
ENAC. If you select Require, you must assign a department code to a manual 
charge in ENAC.
Process Billing Batch 
(BILB) Automatically
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS (FINANCIAL)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Transport tab
FIELD DESCRIPTIONS (TRANSPORT)
Freight Terminal Code 
(TERL)
Your freight terminal code for 3PL-TMS integration. 
Activate Freight Reserved for future use.
Activate TMS Yes
No
If you set this flag to Yes, 3PL -TMS integration will be activated. If you set this 
flag to No, 3PL-TMS integration will not be activated.
Freight Interface Profile 
Code (FIPR)
Your freight interface profile code for 3PL-TMS integration.
External Freight Interface Profile Code (FIPR)Your freight interface profile code for an external non 3PL-TMS integration.
Parcel Interface Profile 
Code (FIPR)
Your freight interface profile code for an external parcel processing system.
Ignore Freight Version For HighJump use only.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 17
COMP screen showing Allocation tab
FIELD DESCRIPTIONS (ALLOCATION)
Activate Directed PutAwayYes
No
If you select Yes, you can perform directed put-away. If you select No, directed 
put-away will be deactivated and you will have to assign locations to receipts 
manually. When you select the No option and bypass the Location field in 
ENRE, the Location Block will appear to remind you to enter a location.
Activate Directed Move 
Inbound
Yes
No
If you select Yes, you can perform directed moves in RFCH (RF Check/
Unload) and RFPU (RF Put-Away). If you select No, directed moves in RFCH 
and RFPU will be deactivated and you will have to assign locations to receipts 
manually.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Activate Directed Move 
Stock
Yes
No
If you select Yes, you can perform directed moves in DMPR (Directed Move 
Processing). If you select No, directed moves in DMPR will be deactivated 
and you will have to assign locations to receipts manually.
Allow Replenishment 
from Pick Line Location 
Type
Yes
No
If you select Yes, you can pick product from a staging location in RFPIC. If you 
select No, you cannot pick product from a staging location in RFPIC.
Activate Location Size Yes
No
If you select Yes, location size logic is activated for directed put-away. If you 
select No, location size logic is deactivated for directed put-away. 
Activate Weight Capacity Yes
No
If you select Yes, the put-away by weight options in ILOP are activated for 
directed put-away. If you select No, the put-away by weight options in ILOP 
are deactivated.
Activate Cube Capacity Yes
No
If you select Yes, the put-away by cube options in ILOP are activated for 
directed put-away. If you select No, the put-away by cube options in ILOP are 
deactivated.
Print Sequence Code for 
Auto-Printed Documents
PRI
MRPI
PSDT
PROM
PRI sorts documents to print by priority only. MRPI adds 10 days to the to ship 
date if to ship date is in the future. It adds 2 days if to ship date is current. It 
doesn’t add any days if to ship date has passed. Then the system prints 
according to the new modified ship date. PSDT sorts documents by order priority, to ship date and order number. PROM sorts by order entry. 
FIELD DESCRIPTIONS (ALLOCATION)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 19
Assign Location Based 
on Header/Document 
Flow
Header
Document
If you set this field to Header (the default value), allocation will be triggered 
and locations assigned whenever an inbound or outbound document is 
assigned to a flow in DIFP in which the Assign Location flag is set to Y for Yes.
If you set this field to Document, allocation will only be triggered if the Print 
Document Without Assigning Location field in DOCU is not Y for Yes for the 
inbound or outbound document.
This option is useful when more than one document is attached to a flow and 
not all documents should trigger allocation. For example, suppose you have 
two documents attached to the STPI (Start Picking) flow:
document 1 = Print Document Without Assigning Location field in DOCU set 
to Y for Yes
document 2 = Print Document Without Assigning Location field in DOCU set 
to N for No
Document 1 will print but no allocation will occur and locations will not be 
assigned. Then document 2 will print, allocation will run and pick locations for 
the order lines will be assigned in the normal manner.
Activate Consolidation of 
R-Type Location Lines
Yes
No
If you set this flag to Yes, allocation will automatically consolidate location 
lines for R-type orders when the location and inventory entity are the same. 
For example, suppose you have three location lines for the same inventory in 
the same location:
Line Number Location Inventory Entity Quantity
1 A100 A1/101 10C
2 A100 A1/101 25C
3 A100 A1/101 15C
If you set this flag to Yes, AccellosOne 3PL will consolidate the three lines into 
one line for location A100 with a quantity of 50 cases. If you set this flag to No, 
AccellosOne 3PL will NOT consolidate the three lines into one. 
FIELD DESCRIPTIONS (ALLOCATION)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Manual Accounts tab
Limit Pick Line to 
Assigned Carriers Only
Yes
No
If you set this flag to Yes, pick line locations will be limited to assigned carriers 
only. If you set this flag to No, pick line locations will be available to all carriers. 
In PIPA (Allocation Pick Line for Parcel Carrier), you specify which SKU codes 
can be picked from the pick line for the assigned carriers.
NOTE The Yes option does not support FIFO/LIFO rules. Orders for nonselected carriers will never be allocated to the pick line even if the oldest product is in a pick line location.
Enable Pallet Attribute in 
LOTP
Yes
No
If you set this flag to Yes, you can put-away product by inventory attribute 
such as pallet size or pallet type rather than SKU quantity, weight or cube. For 
example, you receive both standard four-foot pallets as well seven-foot pallets 
in your warehouse and you need a way to assign your different pallet types to 
a location with sufficient capacity.
If you set this flag to No, put-away by inventory attribute will be deactivated.
FIELD DESCRIPTIONS (ALLOCATION)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 21
FIELD DESCRIPTIONS (MANUAL ACCOUNT)
Allow Manual ConsigneesYes
No
If you select Yes, you can enter manual consignees in ENOR. If you select No, 
you cannot enter manual consignees in ENOR. 
A manual consignee is a consignee that is not set up in CONS (Consignees). 
You enter a manual consignee by keying in a forward slash (/) in the Consignee Code field of ENOR. Then you key in the name of your manual consignee in the Name field.
Allow Manual Shippers Yes
No
If you select Yes, you can enter manual shippers in ENRE. If
you select No, you cannot enter manual shippers in ENRE. A manual shipper 
is a shipper that is not set up in SHIP (Shippers). 
You enter a manual shipper by keying in a forward slash (/) in the Shipper 
Code field of ENRE. Then you key in the name of your manual shipper in the 
Name field.
Allow Manual Carriers Yes
No
If you select Yes, you can enter manual carriers in ENRE and
ENOR. If you select No, you cannot enter manual carriers in
ENRE or ENOR. 
A manual carrier is a carrier that is not set up in CARR (Carriers). You enter a 
manual carrier by keying in a forward slash (/) in the Carrier Code field of 
ENRE or ENOR. Then you key in the name of your manual carrier in the 
Name
field.
Allow Manual Sold-To’s Yes
No
If you select Yes, you can enter manual sold-to’s in ENOR. If
you select No, you cannot enter manual sold-to’s in ENOR.
A manual sold-to is a sold-to that is not set up in SOLD (Sold-To Codes). You 
enter a manual sold-to by keying in a forward slash (/) in the Sold To Code 
field of ENOR. Then you key in the name of your manual sold-to in the Name 
field.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Miscellaneous tab
FIELD DESCRIPTIONS (MISCELLANEOUS)
Allow Multiple Warehouses on Receipt Confirmation
Single
Multiple
If you select Single, multiple warehouses are not allowed on the same receipt; 
that is, you cannot put-away product on the same receipt in multiple warehouses. If you select Multiple, there is no restriction on the number of warehouses on a receipt.
Force Audit of Accessorial ChargesYes
No
If you set this field to Yes, you can force manual charges to be authorized 
before they can be placed on a batch and invoiced. If you set this field to No, 
you cannot force manual
charges to be authorized.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 23
Allow Override of Adjustment DateYes
No
If you set this field to Yes, users can override the adjustment date field in 
ENAJ. If you set this field to No, users cannot override the adjustment date in 
ENAJ.
Activate Pallet RestrictionsSee “PALLET CONTROL” in the Operations 2 Guide. 
Warehouse Code 
Optional for Invoicing by 
Warehouse
See “Invoicing by Warehouse” in the Billing and Invoicing Guide.
Warehouse Code mandatory for Invoicing by 
Warehouse
See “Invoicing by Warehouse” in the Billing and Invoicing Guide.
Use Line-by-Line Formatting for Remarks BlockYes
No
Extended
If you set this field to Yes, remarks that you enter in ENRE, ENOR, ENAJ, 
RELO and other programs require a line number and each line can hold up to 
40 characters. If you set this field to No, remarks that you enter in ENRE, 
ENOR, ENAJ, RELO and other programs do not require a line number and 
automatically wrap to the next line.
If you set this field to Extended, the following screen will display in the 
Remarks Block of ENRE/ENOR:
Extended Remarks screen
See the Operations 1 Guide for further information on extended remarks.
FIELD DESCRIPTIONS (MISCELLANEOUS)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
RF Java Executable For HighJump use only.
Restrict Relocations to 
Same Warehouse
Yes
No
If you set this field to Yes, you cannot relocate inventory in RFRL (RF Relocate) from one warehouse to another. If you set this field to No, there are no 
restrictions on inter-warehouse moves and you can relocated product in RFRL 
from one warehouse to another.
Activate Background 
Printing
Yes
No
This flag applies to the following programs: PRRM (Print Receiving Documents - Specific), PROM (Print Shipping Documents - Specific), PROR (Print 
Shipping Documents - All) and PRRE (Print Receiving Documents - All).
When you activate this flag and print to a warehouse printer, SPL, FAX or 
MAIL, AccellosOne 3PL will execute the printing in the background. This will 
eliminate the delay on the screen and will allow you to continue working on 
your next task. However, any orders or receipts being printed in PRRE, 
PRRM, PROR and PROM will remain locked until printing is complete.
NOTE Background printing is not available for the VIEW printer (Adobe 
Acrobat).
Carrier Owns Transport 
Equipment Equipment/
Container
Yes
No
Whether or not the carrier owns the transport equipment/container or whether 
carrier leases the transport equipment/container from another company.
4PL Type For HighJump use only.
4PL Freight Update is 
Active
For HighJump use only.
FIELD DESCRIPTIONS (MISCELLANEOUS)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 25
COMP screen showing Miscellaneous 2 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 2)
Pallet Code (PALL) This field allows you to add the weight of the pallet itself (that is, the block of 
wood on which the pallet contents rests) to a bill of lading or other outbound 
documents. It can also be used by EDI if required.
Customization by HighJump may be required.
Warehouse Required Yes
No
If you set this field to Yes, the user is required to enter a warehouse code in 
the Header Block of ENRE/ENOR. If you set this field to No, the entry of a 
warehouse code in the Header Block of ENRE/ENOR is not mandatory.
Default Receipt Type in 
ENRE
You can define a default receipt type (Post-receiving, No Charge, Handling, 
etc.) for ENRE in this field.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Only Display Customer 
Charges
Yes
No
If you select Yes, the pick list of charges in ENAC and ENIN will show only 
charges attached to the customer in RATE. That is, a charge attached to customer A in RATE cannot be applied to customer B. As well, a charge attached 
to the .ALL customer cannot be applied to either customer A or customer B.
If you select No, the pick list of charges in ENAC and ENIN will show all 
charges regardless of customer.
Allow Update to Charge 
Quantity and SKU
Yes
No
If you select Yes, the user can update the charge quantity and SKU in ENAC 
and ENIN. If you select No, the charge quantity and SKU in ENAC and ENIN 
are not editable fields.
Enable Reason Codes in 
ENRE/ENOR
Yes
No
If you select Yes, the user can attach a reason code to a receipt/order line in 
ENRE/ENOR. Reason codes, which are maintained in REAS, are used to flag 
exceptional conditions such as “wrong quantity”. 
Enable Equipment Tracking in RFYes
No
If you select Yes, equipment tracking is enabled. Each time that an RF operator logs onto RF, he or she will be required to enter a valid equipment type 
code.
Enable Task Generation 
for Interleaving
Yes
No
If you select Yes, task interleaving will be enabled in RFITLV.
Enable A1 Schedule IntegrationYes
No
If you select Yes, 3PL appointments can be set up and maintained in A1 
Schedule.
FIELD DESCRIPTIONS (MISCELLANEOUS 2)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 27
External Labor System Yes
No
If you select Yes, AccellosOne 3PL will be integrated with West Monroe’s 
FLEXdls labor management software.
Single Pallet Per Order 
Line Flag
Yes
No
If you select Yes, an order line containing two or more pallets in the same 
location will be split into two or more pick assignments. For example, if the 
order line quantity is two pallets and both pallets are in the same location, 
AccellosOne 3PL will create two pick assignments, each for a single pallet. 
The Yes option may be required because of equipment restrictions.
If you select No, an order line containing two or more pallets in the same location will NOT be split into two or more pick assignments.
Validate Ship Date When 
Entering Appointment
Yes
No
If you set this flag to Yes, the user cannot enter a start date for an appointment 
in APPL that is greater than the order/load’s to ship date. If you set this flag to 
No, there is no validation in APPL that the appointment’s start date is less than 
or equal to the order/load’s to ship date.
FIELD DESCRIPTIONS (MISCELLANEOUS 2)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
COMP screen showing Miscellaneous 3 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 3)
Prompt User to Run 
RESW When Changing 
Weight in ITEM
Yes
No
If you set this flag to Yes, the user will be prompted to run RESW if he or she 
changes the standard weight in ITEM.
Minimum Number of 
Months to Retain Data
See “ARCHIVING AND PURGING” on page 79.
Allow Multiple Archive/
Purge Selections
See “ARCHIVING AND PURGING” on page 79.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 29
Special Sorting Process 
Type (RFSC)
Enter OPID from, select an order if more than one order in OPID
If you select “Enter OPID from, select an order if more than one order in 
OPID”, you will be prompted to enter the OPID in RFSC. If you leave this field 
blank, you will be prompted to enter the order number in RFSC.
Update Carrier Code on 
Orders/Receipts from 
Appointment
Yes
No
If you set this flag to Yes and the carrier attached to the appointment in APPL 
does not match the carrier attached to the order/receipt, AccellosOne 3PL will 
update the order/receipt carrier to match the appointment’s carrier. 
Update Load Type Code 
on Orders/Receipts from 
Appointment
Yes
No
If you set this flag to Yes and the load type attached to the appointment in 
APPL does not match the load type attached to the order/receipt, AccellosOne 
3PL will update the order/receipt load type to match the appointment’s load 
type. 
Allow Emails to be Generated Upon Batch Confirmation
Yes
No
If you set this flag to Yes and create a valid record in AECS (Automatic Email 
Setup), you can email confirmed invoices to customers in BILB (Billing Batch). 
If you set this flag to No, emailing of confirmed invoices to customers in BILB 
will be deactivated.
Enable RF Image Capture
Only available for Intermec CK71 ITE devices
Yes
No
If you set this flag to Yes, RF image capture will be activated. If you set this 
flag to No, RF image capture will be deactivated.
Enable Order Cancellation in ENORYes
No
If you set this flag to Yes and delete an order in ENOR, you will be prompted to 
either delete or cancel the order. If you select the Cancel option, your selection will be saved in the order header in a field used by EDI that is not accessible in LOOR. 
FIELD DESCRIPTIONS (MISCELLANEOUS 3)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Allow Skipping of From 
Warehouse in RFPIC
Yes
No
If you set this flag to Yes, you can bypass the WHSE field in RFPIC and enter 
your order directly. If you set this flag to No, the WHSE field is mandatory and 
cannot be bypassed.
Reason Code Required 
for Appointments
Reserved for future use.
Enable OPID Mixed Item 
Rule by Warehouse
Yes
No
In this field, you set up your default rule for mixing items on the same OPID. 
This rule defines whether or not you can mix different items on the same OPID 
when performing case picking (RFPIC, RFPK, RFITLV), pallet building and 
OPID merging (RFMG).
This flag is a default only. You can override it in both CCCC and WCCO.
FIELD DESCRIPTIONS (MISCELLANEOUS 3)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 31
COMP screen showing Miscellaneous 4 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 4)
Wave Pick Method 
Assignment Type
Enable Pick Method Generation
Enable Pick Method Generation, suppress LABP pick method
See your HighJump implementation consultant for further information on this 
field.
Skip Order Entry in RFOA Yes
No
If you set this flag to Yes, you can skip the ORDE field in RFOA and enter your 
OPID directly. If you set this flag to No, the ORDE field in RFOA is mandatory 
and cannot be skipped.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Event Cycle Count Limited by Warehouse CodeYes
No
If you set this flag to Yes, any event-driven cycle counts generated by a variance will be limited to the warehouse in which the variance occurred. If you set 
this flag to No, any event-driven cycle counts generated by a variance will 
apply to all warehouses.
Minimum Number of 
Days to Retain OPID
The minimum number of days to retain OPID’s. If you leave this field blank, 
you will not be able to reuse OPID’s in RFMG. If you enter a value in this field 
(say, 30 days), duplicate OPID’s will be allowed in RFMG after 30 days.
Default Receipt Line Type 
in ENRE
You can define a default line type in ENRE by entering the line type (P, U, etc.) 
in this field.
Hide Quantity in RFPR Yes
No
If you set this flag to Yes, the quantity fields in RFPR (RF Product Look-Up by 
Location) will be suppressed for non-supervisory users. If you set this flag to 
No, the quantity fields in RFPR will display for all users both supervisory and 
non-supervisory.
Suspend Picking Tasks 
Upon Wave Execution
See the “Building Pallets in PABU” section in the RF Guide for further information.
RFRP Requery Type Requery Scrolling in Pick List and Upon REPI Completion
Requery Upon REPI Completion
In this field, you specify your requery rules for RFRP. A requery occurs when 
you select a record in RFRP using your arrow keys, confirm the replenishment 
of that record and then query for a second record to confirm.
If you select “Requery Scrolling in Pick List and Upon REPI Completion”, the 
list of available replenishments in RFRP will display the full list starting with 
the first record when you perform a requery. If you select “Requery Upon REPI 
Completion”, the list of available replenishments in RFRP will display the full 
list starting with the record before the last record that you selected; to see 
records before that record, you must use your arrow keys to scroll to the 
beginning of the list.
RFITLV First Check 
Same Location for Task
See the “Task Interleaving” section in the RF Guide for further information.
RFITLV Second Check 
Same Aisle for Task
See the “Task Interleaving” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
SYSTEM ADMINISTRATION GUIDE 4.2* 33
COMP screen showing Miscellaneous 5 tab
RFITLV Third Check 
Same Zone for Task
See the “Task Interleaving” section in the RF Guide for further information.
Supervisor Notification 
Group Email Address
See the “Supervisor Notification” section in the RF Guide.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)
Ignore CCOR Validation 
in ICOC
No
Yes
If you set this flag to Yes, you can access ICOC even if the Use Consignee 
Item Configuration flag in CCOR is set to No. If you set this flag to No, you can 
only access ICOC if the Use Consignee Item Configuration flag in CCOR is 
set to Yes.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Company Code in COMP
Consignee Subscribed to 
Interface Processing Only
No
Yes
This field is only used if your consignees are set up and maintained in another 
system such as ERP software and imported into AccellosOne 3PL.
If you set this flag to Yes, you cannot create and delete consignees in CONS 
nor can you modify the consignee’s address. If you set this flag to No, normal 
create, delete and modify functions are available in CONS.
Customer Subscribed to 
Interface Processing Only
No
Yes
This field is only used if your customers are set up and maintained in another 
system such as ERP software and imported into AccellosOne 3PL.
If you set this flag to Yes, you cannot create and delete customers in CUST 
nor can you modify the customer’s address. If you set this flag to No, normal 
create, delete and modify functions are available in CUST.
Use Pallet Pick Method 
for Last Entity
Yes
No
In this field, you define the pick method for non-pick line locations when the 
order line does not have any pick method assigned to it by the Wave Manager.
If you set this flag to Yes, if the Wave Pick Method Assignment Type parameter in COMP is not blank and if the order line quantity equals the on-hand 
quantity of the entity in the location, the PALL pick method will be assigned to 
the order line.
If you set this flag to No and if the order line quantity is greater than or equal to 
a full pallet, the PALL pick method will be assigned to the order line.
Default Load Status Created by Freight Interface 1 Create
2 Ready to Load
In this field, you define the default load status when creating outbound loads 
for a TMS system or EDI.
Use Assignment Parameter Tables for Pallet BuildSee the “Building Pallets in PABU” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 35
Setting Up Your Programs in EXJO, JOSE
There are two setup programs in AccellosOne 3PL for application programs:
 EXJO (Executable Job Code)
 JOSE (Job Selection Code)
The executable job code is the actual program name of a given program. The job selection code, on 
the other hand, is the code that the user types in to access the program. For example, the executable job 
code for the Enter Receipts program is rp_101 while the job selection code for the same program is ENRE 
(Enter Receipt).
Executable job codes are set up by HighJump and cannot be modified by system administrators. Job 
selection codes, on the other hand, can be user-defined by system administrators to meet company or 
language requirements.
There are two steps to follow in setting up a new program: first you set up your executable job code in EXJO 
and second you attach your executable job code to your job selection code in JOSE.
Location Capacity Validation TypeNo validation for user-initiated transactions (1)
Validate location capacity and generate warning message (2)
Validate location capacity and do not allow operator to continue (3)
If you select 1, no validation of location capacity will be performed for user-initiated transactions in ENRE, RELO, RFCH, RFPU and RFRL.
If you select 2, AccellosOne Enterprise 3PL will validate the location capacity 
for user-initiated transactions. If the location capacity is exceeded, the system 
will generate a warning message; as well, if the violation occurs in an RF program, an event-driven cycle count will be generated.
If you select 3, AccellosOne Enterprise 3PL will validate the location capacity 
for user-initiated transactions. If the location capacity is exceeded, the operator will not be allowed to proceed; as well, if the violation occurs in an RF program, an event-driven cycle count will be generated. 
RF Special Character See the “General Setup” section in the RF Guide for further information.
Set Default Values in RF 
Pallet Screen
See the “General Setup” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SETTING UP YOUR EXECUTABLE JOB CODES IN EXJO
You set up your executable job codes in EXJO. Executable job codes are attached to job selection codes in 
JOSE (Job Selection Code).
FIELD DESCRIPTIONS
Job Name Mandatory
The job name. Job names must be set up by HighJump.
Description Mandatory
The job description.
Type JAVA
NET
ORAR
Set up by HighJump.
Operator Required Reserved for future use.
Print Job R = Report
N = None
If you select R for Report, the word “Report” will appear beside the program 
name and description when you view the submenu to which the program is 
attached. 
If you select N for None, the program name and description only will appear 
when you view the submenu to which the program is attached.
EXJO JOSE
job code = rp_101 rp_101 = ENRE

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 37
LOCK BLOCK
The Lock Block allows you to apply locks to programs. There are two kinds of program locks in AccellosOne 
3PL: 
 there are exclusive locks that allow you to restrict access to a program to a single user at any one 
time (for example, if operator A is using ENRE, no other operator can enter this program until operator A 
exits)
 there are conditional locks that allow you to lock one program when another program is being used 
(for example, if program A is running, program B is locked and cannot be accessed by any user until 
program A has finished)
You can combine both kinds of locks in EXJO for the same program. For example, you apply an exclusive 
lock to PHUP (Physical to Inventory Update) so that only one user can access this program at any given time. 
Then you apply a conditional lock to ENTI (Enter Tickets) so that no user — including the user working in 
PHUP — can enter tickets in ENTI for a physical while PHUP is running. 
Query Job Y = Yes
N = No
If you select Y for Yes, the program will appear on the Hot Query Selection 
menu. If you select N for No, the program will NOT appear on the Hot Query 
Selection menu.
Hot Queries allow you to enter a second program to look up information without closing the program that you are currently working in. For example, if you 
are entering a receipt in ENRE and receive a telephone call about a specific 
order, you can look up the order in LOOR without closing ENRE.
External Executable Reserved for future use.
NOTE Locks apply to the active company only. If you set up an exclusive lock for 
ENTI and are working in ENTI in company W1, no other operator in W1 will be able to 
access the program. However, a second operator working in company W2 will be 
able to access ENTI as well as a third operator working in company W3.
FIELD DESCRIPTIONS
Job Name The job name or names that you wish to lock. If you are setting up an exclusive lock, the job name in the Lock Block will be the same as the job name in 
the Header Block. If you are setting up a conditional lock, the job name in the 
Lock Block will not match the job name in the Header Block.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
1 Enter EXJO.
2 Click on Create Record.
3 Key in your job name and press Enter.
4 Key in your description and press Enter.
5 Press Enter to bypass the Type field.
6 In the Operator Required field, key in N for No and press Enter.
7 In the Print Job field, key in R for Report or N for None and press Enter.
8 In the Query Job field, key in Y for Yes or N for No and press Enter.

Executable Job Code (EXJO)
9 Press Enter to bypass the External Executable field.
Correct Y = Yes
N = No
If you select Y for Yes, the record is correct and you wish to accept it. If you 
select N for No, the record is not correct and you can change it.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 39
10 In the Lock Block, do one of the following.

Executable Job Code (EXJO) screen showing two locks: an exclusive lock (pi_105) and a conditional 
lock (pi_101)
11 When you finish setting up your executable job code, click on Return to Main and Master Block. Then 
click on Exit to exit.
SETTING UP YOUR JOB SELECTION CODES IN JOSE
In JOSE you attach the executable job code previously set up in EXJO to your job selection code. You define 
the following parameters in JOSE:
 the job selection code for the program
 the submenu to which the job selection code is attached
 the program’s position on the submenu
 the program’s executable job code
If you wish to set up locks for the 
program:
If you do NOT wish to set up 
locks for the program:
a) Click on Create Record.
b) Key in your job name and press 
Enter.
c) In the Correct field, press Enter 
to accept the value of Yes.
d) Repeat the above steps for each 
additional program that you wish 
to lock.
a) Proceed to step 10.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
If required, you can attach multiple job selection codes to the same executable job.
FIELD DESCRIPTIONS
Selection Code Mandatory
The program’s job selection code. Job selection codes can consist of any 
combination of letters between four and six characters in length. 
Description Mandatory
A meaningful description for the job selection code.
Subsystem Code (JOSE) Mandatory
The submenu to which the program is attached.
Sort Sequence The program’s position on the submenu. For example, if you enter 5 for the 
program ENRE, ENRE will be the fifth program shown on the submenu RECE.
Executable Job Code 
(EXJO)
Optional
The program’s executable job code.
Help File For HighJump use only
Print Job N = No
R = Report
If the executable job code is defined as a report in EXJO, this field will automatically be set to R for Report. If the executable job code is not defined as a 
report in EXJO, this field will automatically be set to N for No. 
Form Code (FORM) Only available if the executable job is a standard report
The report’s paper size and orientation.
ISO Reference Code Only available if the executable job is a report
If you enter ISO reference information in this field, it will print in the bottom 
right-hand corner of each page of the report.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 41
1 Enter JOSE.
2 Click on Create Record. 
3 Key in your job selection code and press Enter.
4 Key in a meaningful description for your job selection code and press Enter.
5 In the Subsystem Code field, key in the submenu to which the job selection is to be attached and press 
Enter or use your pick list to select the appropriate submenu.
6 Key in your sort sequence number and press Enter.
7 In the Executable Job Code field, key in your executable job code and press Enter or use your pick list to 
select the appropriate code.
8 Press Enter to bypass the Help File field.
9 If the executable job code that you entered in the previous field is defined as a report in EXJO, key in 
your form code in the Form Code field and press Enter or use your pick list to select it. Then press Enter 
in the Re-Align Forms Message field to accept the value of N for No.
10 If the executable job code that you entered in the Executable Job Code field is defined as a report in 
EXJO, you can enter an ISO reference code. If you do not require an ISO reference code, press Enter to 
bypass this field.

Job Selection Code (JOSE)
11 When you finish setting up your job selection code, click on Return to Main and Exit to exit.
SETTING UP SUBMENUS IN JOSE
The menu tree consists of two types of codes: job selection codes and submenus. A job selection 
code is a regular AccellosOne 3PL program that you use to look up information or to create or modify data. 
Re-Align Forms Message Reserved for future use.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
Job selection codes are always attached to submenus. A submenu, on the other hand, is merely a folder or 
directory used to group a number of similar programs under a single, meaningful name. For example, ITRE is 
a submenu used to group all item-related programs.
AccellosOne 3PL allows you to create your own submenus using your own terminology and attach these 
customized submenus to other submenus; in this way, you can create a completely customized menu 
structure. You set up a submenu in JOSE by creating a new job selection code. Unlike programs, submenus 
do not have executable job codes attached to them. 
1 Enter JOSE.

Job Selection Code (JOSE)
2 Click on Create Record. 
3 Key in your submenu code and press Enter.
4 Key in a meaningful description for your job selection code and press Enter.
5 In the Subsystem Code field, key in the submenu to which the job selection is to be attached and press 
Enter or use your pick list to select the appropriate submenu.
6 In the Visible field, key in Y for Yes and press Enter.
7 Key in your sort sequence number and press Enter.
8 Press Enter to bypass the Executable Job Code field.
9 Click on Return to Main.
NOTE Once you have created a new submenu, you must give your company 
access to it in COAC (Company Access) and your operators access to it in OPAC 
(Operator Access).

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 43

Job Selection Code (JOSE) screen showing the submenu RECE
10 Click on Exit to exit.
DELETING A SUBMENU
Before you can delete a submenu, you must remove any dependent selections. A dependent selection is a 
program or submenu that is attached to the submenu that you wish to delete.
1 If the submenu has dependent selections, you must remove them in JOSE. You remove dependent 
selections by retrieving the program or submenu in JOSE and deleting it.
2 Enter JOSE.
3 Click on Enter Criteria.
4 Press Enter to position your cursor in the Selection Code field.
5 Key in the code of the submenu that you wish to delete and click on Query.
6 When the record is retrieved, press Enter twice to position your cursor in the Description field.
7 Click on Delete.
8 Click on Exit to exit.
LOOKING UP A PROGRAM’S PATH 
You look up a program’s path in JOSE by performing a query on the job selection code. When the appropriate 
record is retrieved from the database, you note the selection code’s subsystem code and then perform a 
second query — this time entering the subsystem code in the Selection Code field. You continue to work back 
up from the first or lowest subsystem code, to the second or next higher subsystem code, to the third or next 
higher subsystem code until you reach MAIN or RFMN (for RF programs).
For example, if you wished to look up the path of CORL (Confirm Receipts - Line at a time), you would do the 
following.
1 Enter JOSE.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
2 Click on Enter Criteria.
3 Press Enter to position your cursor in the Selection Code field.
4 Key in CORL and click on Execute Query.

Job Selection Code (JOSE) screen showing RECE as the subsystem code for CORL
5 Your first subsystem code for CORL is RECE (Receiving). You are now ready to query on RECE.
6 Click on Enter Criteria.
7 Press Enter to position your cursor in the Selection Code field.
8 Key in RECE and click on Execute Query.

Job Selection Code (JOSE) screen showing WO as the subsystem code for RECE

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Your Programs in EXJO, JOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 45
9 Your second subsystem code for CORL is WO (Warehouse Operations). You are now ready to query on 
WO.
10 Click on Enter Criteria.
11 Press Enter to position your cursor in the Selection Code field.
12 Key in WO and click on Execute Query.

Job Selection Code (JOSE) screen showing MAIN as the subsystem code for WO
13 Your third and final subsystem code for CORL is MAIN (Main Menu). You now know the complete path of 
CORL: MAIN\ WO\RECE\CORL.
LOOKING UP A PROGRAM’S EXECUTABLE JOB CODE
You look up the executable job code for a program by performing a query in JOSE on the job selection code.
1 Enter JOSE.
2 Click on Enter Criteria.
3 Press Enter to position your cursor in Selection Code field.
4 Key in the job selection code that you are querying on and click on Query.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Programs to Companies in COAC

Job Selection Code (JOSE) screen showing rp_101 as the executable job for ENRE
5 Click on Exit to exit.
Assigning Programs to Companies in COAC
You give companies access to programs and submenus in COAC (Company Access). Company access 
means that a given program or submenu appears on your screen when you are working in that company. It is 
not the same as operator access set up in OPAC, which allows you to look up information, run reports and 
enter data. In order to use a given program, you need both company access and operator access. 
For example, in order for operator A to use ENRE (Enter Receipts) in W1, you must give W1 access to ENRE 
and you must give operator A access to ENRE. If either of these conditions is not met, operator A will not be 
able to enter receipts in W1.
NOTE In order to give a company access to a given program, you must give the 
company access to the program’s entire path; that is, all submenus to which the program is attached. If you do not know the submenus to which a program is attached, 
you must perform a query in JOSE. See “Looking Up a Program’s Path” on page 33 
for further instructions.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Programs to Companies in COAC
SYSTEM ADMINISTRATION GUIDE 4.2* 47
1 Enter the appropriate company (usually Z1).
2 Enter COAC.
3 Key in your company code and press Enter.
4 Key in your subsystem code and press Enter or use your pick list to select it.
FIELD DESCRIPTIONS
Company Code Mandatory
The company to which you wish to give access.
Subsystem Code Mandatory
The subsystem code to which the program is attached. If you do not know to 
which submenu a program is attached, you must look it up in JOSE.
Selection Code A list of all selection codes that are attached to the submenu that you selected 
in the Subsystem Code field.
Dependent Selections If the selection code is a submenu, the number of programs and submenus 
that are attached to it.
Attach to Subsystem Y = Yes
N = No
If you select Y for Yes, the company will have access to that selection code 
plus any dependent selections. If you select N for No, the company will have 
no access to either the selection code or any dependent selections.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Programs to Companies in COAC

Company Access (COAC) showing WO subsystem
5 Use your arrow keys to position your cursor on the selection code that you wish to give access to.
6 In the Attach to Subsystem field, key in Y for Yes and press Enter.
7 If you entered Yes in the previous field and your selection code has dependent selections, click on 
Dependent Selections. Then repeat the above steps for each dependent selection. In order to give a 
company access to a given program, you must always drill down to the lowest level.
8 When you finish giving your company access to the required programs, click on Return to Main and then 
Exit to exit.
REMOVING PROGRAMS FROM COMPANIES
1 Enter COAC. 
2 Key in your company code and press Enter.
3 Key in your subsystem code and press Enter or use your pick list to select it.
4 Use your arrow keys to position your cursor on the selection code that you wish to remove access to.
5 In the Attach to Subsystem field, key in N for No and press Enter.
6 When you finish removing the required programs, click on Return to Main and then Exit to exit.

SETTING UP COMPANIES, PROGRAMS AND USERS
Overview of New User Setup
SYSTEM ADMINISTRATION GUIDE 4.2* 49
Overview of New User Setup
There are four steps to follow in setting up a new user:
Setting Up New Users in OPER
You set up new users in OPER (Operator Code). There are two classes of users in AccellosOne 3PL: 
system administrators and regular users. System administrators can create other operators, give 
operators access to programs, remove access to programs and delete operators. Regular users, on the other 
hand, are not able to perform any of these functions. They are limited to changing their own password in the 
password change program.
When you set up a new user, that user’s password is preset to his or her operator code followed by the default 
password in INST (Installation Parameters). For example, if you set up a new user called Bob and the default 
password in INST is set to “CHANGEIT”, Bob’s initial password will be BOBCHANGEIT. The new user must 
change this password when he or she logs on to AccellosOne 3PL for the first time.
ActiveDesktop
OPAC/
COOA
The new user must log into ActiveDesktop
and change his or her temporary password.
You assign program access to users in
OPAC or copy program access in COOA.
OPER
OPRS
You set up your new user in OPER as
either a system administrator or regular
user.
You enter your operator restrictions in
OPRS. You can restrict an operator to
certain printers, companies, customers,
consignees, shippers, carriers and
documents.
2
3
4
1

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up New Users in OPER
FIELD DESCRIPTIONS
Operator/ Employee 
Code
The operator code. The code that you enter cannot start with a number and 
cannot exceed 20 characters in length. No embedded spaces or special characters are allowed.
Name The operator name.
Language Code Mandatory
The user’s language. This field determines the language of the screens, 
menus, hint lines, error messages and system codes for the user throughout 
the entire AccellosOne 3PL suite of products.
e-Mail Address Optional
The user’s e-mail address. 
Operator Flag O = Operator
B = Both (only used to give an operator supervisor privileges in certain RF 
program)
Set to O for Operator
Employee ID Reserved for future use
Show Inventory Access 
Code
Y = Yes
N = No
If you set this flag to Yes, the inventory access code will be displayed when 
the user looks up inventory in LOEN. The inventory access code is a fivecharacter system-generated code that refers to a specific inventory entity. For 
example, the code 01ABC could refer to item 1, lot 101, pallet ID 123.
If you set this flag to No, the inventory access code will not be displayed when 
the user looks up inventory in LOEN.
Show Archive Data in 
Look Ups
See “ARCHIVING AND PURGING” on page 79.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up New Users in OPER
SYSTEM ADMINISTRATION GUIDE 4.2* 51
SETTING UP AN OPERATOR
1 Enter the appropriate company (usually Z1).
2 Enter OPER.
3 Click on Create Record.
4 Key in your operator or employee code and press Enter.
5 Key in your operator or employee name and press Enter.
6 In the Language Code field, use your pick list to select the appropriate language for the user.
7 If required, key in the user’s e-mail address and press Enter.
8 In the Operator Flag field, key in O for Operator and press Enter.
9 Press Enter to bypass the Employee ID field.
10 In the Show Inventory Access Code field, key in Y for Yes or N for No and press Enter.
11 In the Show Archive Data in Look Ups field, key in Y for Yes or N for No and press Enter.
12 In the System Administrator field, key in Y for Yes or N for No and press Enter.
13 In the Authority Flag field, key in N for No and press Enter.
14 Click on Return to Main to exit Create Mode.
System Administrator Not available for employees
Y = Yes
N = No
If you enter Y for Yes, the user will enjoy “system administrator” privileges and 
can create other operators, give operators access to programs, remove 
access to programs and delete operators. If you enter N for No, the user will 
not be able to perform any of these functions. Non-system administrators are 
limited to changing their own password in the password change program.
If you change this flag for an existing user, that user’s password will be set to 
his or her operator code plus the default password in INST (Installation 
Parameters). For example, if the user’s operator code is JOE and the default 
password in INST is set to “CHANGEIT”, Joe’s password will be set to 
JOECHANGEIT.
NOTE Before system administrators can give operators access to programs in OPAC (Operator Access), they must be given access to OPAC themselves. Likewise, before system administrators can set up job selection codes 
in JOSE, they must be given access to this program.
Authority Flag Reserved for future use
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up New Users in OPER

Operator Code (OPER) screen showing an operator
15 Click on Exit to exit.
SETTING UP AN OPERATOR WITH SUPERVISOR PRIVILEGES
Certain RF programs require supervisor privileges to access. You give an operator supervisor privileges by 
setting the Supervisor Flag to Y for Yes.
1 Enter OPER.
2 Retrieve the operator whose privileges you wish to change.
3 Press Enter until your cursor is positioned in the Operator Flag field. Then key in B for Both and press 
Enter.
4 Press Enter to bypass the Employee ID field.
5 In the Show Inventory Access Code field, key in Y for Yes or N for No and press Enter.
6 In the Show Archive Data in Look Ups field, key in Y for Yes or N for No and press Enter.
7 In the System Administrator field, key in Y for Yes or N for No and press Enter.
8 In the Authority Flag field, key in N for No and press Enter.
9 In the Labor Capture Flag field, key in N and press Enter.
10 Press Enter to position your cursor in the Company Code field. Then key in your company code and 
press Enter.
11 Press Enter to position your cursor in the Warehouse Code field. Then use the pick list function to select 
any warehouse code from the pick list.
12 In the MHE Type Code field, use your pick list to select any MHE type code.
13 Press Enter until your cursor is positioned in the Employee Temporary Flag field. Then key in N for No 
and press Enter.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up New Users in OPER
SYSTEM ADMINISTRATION GUIDE 4.2* 53
14 In the Supervisor Flag field, key in Y for Yes and press Enter.
15 Click on Return to Main and Exit to exit.
DEACTIVATING AN OPERATOR
If you deactivate an operator, the operator will not be able to log on to AccellosOne 3PL until he or she has 
been reactivated.
1 Enter OPER.
2 Retrieve the operator that you wish to deactivate.
3 Press Enter to position your cursor in the Name field.
4 Click on Delete.
5 Click on Exit to exit.
REACTIVATING AN OPERATOR
If an operator has been deactivated, he or she must be reactivated in order to access AccellosOne 3PL. 
There are two steps to follow in reactivating an operator: first you change the status of the operator in OPER 
from D to A and then you reset the operator’s password in ROPA (Reset Operator Password).
1 Enter OPER.
2 Retrieve the operator that you wish to reactivate.
3 Continue to press Enter until your cursor is positioned in the Status field.
4 Key in A for Activate and press Enter.
5 Click on Exit to exit.
6 Proceed to reset the operator’s password by following the instructions in “Resetting an Operator’s Password in ROPA” on page 53.
RESETTING AN OPERATOR’S PASSWORD IN ROPA
Resetting an operator’s password is necessary in the three cases:
 you wish to reactivate a deactivated operator
 the operator has forgotten his or her password and cannot log on to AccellosOne 3PL
 an RF operator has no access to ActiveDesktop and has never logged on to AccellosOne 3PL through 
ActiveDesktop
When you reset an operator’s password, that user’s password is preset to his or her operator code plus the 
default password in INST (Installation Parameters). For example, if the user’s operator code is JOE and the 
default password in INST is set to “CHANGEIT”, Joe’s password will be set to JOECHANGEIT. The user must 
change this password when he or she logs on to AccellosOne 3PL for the first time.
1 Enter ROPA.
2 Key in the operator code that you wish to reset and press Enter.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC

Reset Operator Password (ROPA)
3 Click on Reset.
4 Click on Yes when prompted to reset the password.
5 Click on Exit to exit.
Assigning Program Access to Users in OPAC
The AccellosOne 3PL menu structure has a tree formation consisting of a main menu, submenus and 
individual programs. The MAIN menu forms the trunk from which the submenus branch out. Many of the 
submenus have their own submenus and some of these have yet another submenu attached to them as well. 
Attached to submenus at any level are the programs themselves that you use to look up information and enter 
data. 
The following diagram shows a sample selection of programs that are attached to the submenu RECE.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
SYSTEM ADMINISTRATION GUIDE 4.2* 55
In order to give a user access to any given program, you have to give access to MAIN as well as to all the 
submenus to which the program is attached.
For example, to give a user access to ENRE (Enter Receipts), you would first give access to MAIN, then give 
access to WO (Warehouse Operations), then give access to RECE (Receiving) and lastly give access to the 
program itself, ENRE. If you failed to give the user access to MAIN or any of the submenus, the user would be 
unable to enter ENRE. 
There are two possible levels of access for any given AccellosOne 3PL program: read only = Yes and read 
only = No. 
You assign program access to users in OPAC (Operator Access). OPAC gives users access to all companies 
on your system. If you wish to restrict users to certain companies, you must do so in OPRS (Operator Restrictions).
RF MENU STRUCTURE
The Main Menu from which all RF programs branch out is called RFMN. There are four submenus attached to 
RFMN: RFLOOK for RF look-up programs, RFINB for RF receiving, RFOUTB for RF shipping and RFINVT 
for miscellaneous RF programs.
read only = Yes the user can look up information in the program but cannot change it
read only = No the user can modify any information in the program; for example, create a 
record, change a record and delete a record
MAIN
WO
(Warehouse
Operations)
SA (System
Administration)
CS (Customer
Service)
RECE
(Receiving)
CHRF Time stamp and confirm receipts
CORL Confirm receipts - line at a time
ENRE Enter Receipts (inbounds)
PRRE Print receiving documents - all
PRRM Print receiving documents - specific
RERE Requeue receipt documents
submenus attached
to MAIN
submenu RECE attached
to submenu WO
programs attached
to submenu RECE

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
LOOKING UP SUBMENUS
You look up submenus in OPAC (Operator Access).
1 Enter OPAC.
2 Key in your submenu code and press Enter or use your pick list to select it.

Operator Access (OPAC)
3 If the selection code has dependent selections, the code is a submenu. If the selection code has no 
dependent selections, the code is a program and you cannot drill down any further.
4 Click on Subsystem Code and Exit to exit.
ASSIGNING PROGRAM ACCESS TO A USER
You assign program access to users in OPAC (Operator Access). OPAC requires you to assign program 
access to individual users one program at a time. If you have multiple users that share the same access privileges, you can set up generic operators (for example, level 1 security, level 2 security, level 3 security, etc.) 
and copy the generic access to the individual operators in COOA (Copy Operator Access). 
CAUTION You cannot assign program access to a user until that user has logged 
into ActiveDesktop for the first time and changed his or her temporary password from 
JOEMUSTCHANGE to a permanent password. “JOEMUSTCHANGE” passwords are 
not valid in OPAC, COOA (Copy Operator Access) and OPRS (Operator Restrictions).
the name of the 
submenu
this code has no 
dependent 
selections and is 
therefore a program
this code has 14 
dependent 
selections and is 
therefore a submenu

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
SYSTEM ADMINISTRATION GUIDE 4.2* 57
1 Enter OPAC.
2 Key in MAIN or RFMN and press Enter.
3 If you have multiple MAIN/RFMN menus on your system, select the MAIN/RFMN menu for the appropriate language.

Operator Access (OPAC) screen showing MAIN submenu
4 The system will display all submenus attached to MAIN (CL, CS, DA, etc.) or RFMN. In the screen shown 
above, there are a total of 16 submenus attached to MAIN. In the Dependent Selections column is shown 
the number of submenus and programs attached to each submenu attached to MAIN. For example, the 
CS submenu has two dependent selections.
5 Click on Operator Block. In this step you are going to give the user access to MAIN/RFMN.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC

Operator Access (OPAC) showing Operator Block
6 Click on Create Record.
7 Key in your operator code and press Enter or use your pick list to select your operator.
8 In the Read Only Flag field, key in Y for Yes or N for No and press Enter.
9 When you finish giving your user access to MAIN/RFMN, click on Return to Main to exit Create Mode 
and return to Main Mode.
10 Click on Master Block to display the programs and submenus attached to your first submenu.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
SYSTEM ADMINISTRATION GUIDE 4.2* 59

Operator Access (OPAC) screen showing four programs attached to FX submenu
11 If you wish to give the user access to this program or submenu, click on Operator Block and repeat steps 
7 and 8. If you do not wish to give the user access to this program or submenu, click on Previous Subsystem.
12 Continue to assign access to the user. Remember to drill down from the MAIN/RFMN submenus to the 
program that you wish to give access to and then work your way back up to the submenus attached to 
MAIN/RFMN. 
13 When you finish giving your user access to the programs that he requires, press Exit to exit.
REMOVING A USER’S PROGRAM ACCESS
1 Enter OPAC.
2 Key in MAIN or RFMN and press Enter.
3 If you have multiple MAIN/RFMN menus on your system, select the MAIN/RFMN menu for the appropriate language.
The system will display all submenus attached to MAIN (CL, CS, DA, etc.) or RFMN. 
NOTE You must enter the Operator Block and create a record for each submenu 
starting from MAIN /RFMN in a program’s path. If a single link is missing — that is, 
there is no access to a particular submenu in a program’s path — the user will be 
unable to access the program.

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
4 Continue to drill down from MAIN until you reach the program or submenu whose access you wish to 
remove.
5 Click on Operator Block. 

Operator Access (OPAC) showing Operator Block
6 Position your cursor over the operator whose access you wish to remove.
7 Press Enter to position your cursor in the Read Only Flag field.
8 Click on Delete.
9 Press F4 the required number of times to exit OPAC.
COPYING AN OPERATOR’S ACCESS IN COOA
You can copy access from one user to another user in the program COOA (Copy Operator Access). The copy 
function allows you to set up generic security levels such as Level 1, Level 2, Level 3, Level 4, etc. Once you 
have set up your generic operator codes and assigned them the appropriate program access in OPAC 
(Operator Access), you can copy their access and assign it to individual operators in a single step. 
The copy function makes it possible to set up standard levels of access for different classes of users, thereby 
eliminating the need to assign access to a user one program at a time in OPAC (Operator Access).
When you use the copy function, the “from” and “to” operators must have the same language code in OPER 
(Operator Code). You cannot copy operator 1’s access (language code = ENUS) to operator 2 (language 
code = ESCL).

SETTING UP COMPANIES, PROGRAMS AND USERS
Assigning Program Access to Users in OPAC
SYSTEM ADMINISTRATION GUIDE 4.2* 61
There are two options in COOA: ALL or Missing. The All option gives the “from” and “to” operators identical 
access. The Missing option, on the other hand, adds the “from” operator’s access to the “to” operator’s 
access without making the two operators identical. 
1 Enter COOA.
2 Key in your from operator and press Enter.
3 When the list of operators is displayed, use your arrow keys to position your cursor on the operator code 
that is to receive the from operator’s program access.
4 Press Enter to position your cursor in the First Menu field. Then do one of the following:
5 Press Enter again to position your cursor in the All/Missing field.
6 Key in A for All or M for Missing and press Enter.
7 If required, you can copy operator restrictions set up in OPRS by keying in Y for Yes in the appropriate 
field(s) — CUST Restrictions, CONS restrictions, etc. — and pressing Enter.
A’s Access
B’s Access 
Before Copy 
B’s Access After Copy 
Using All Option Explanation
ENRE, ENOR CHRF, CHOF ENRE, ENOR The system deletes B’s original access 
and then copies A’s access to B.
A’s Access
B’s Access 
Before Copy
B’s Access After Copy 
Using Missing Option Explanation
ENRE, ENOR CHRF, CHOF ENRE, ENOR, CHRF, CHOF The system copies A’s access to B without deleting B’s original access.
If you wish to copy access for 
non-RF programs only:
If you wish to copy access for RF 
programs only:
a) Key in MAIN and press Enter. a) Key in RFMN and press Enter.

SETTING UP COMPANIES, PROGRAMS AND USERS
Entering Operator Restrictions in OPRS

Copy Operator Access (COOA) showing the operator ABCFOOD-1 receiving the access of BOB
8 Repeat steps 3 to 7 for each additional operator that is to receive the from operator’s program access.
9 When you finish copying access, click on Operator Code and Exit to exit.
Entering Operator Restrictions in OPRS
You can restrict an operator by printer, company, customer, consignee, shipper, carrier and document. A 
restriction can be either inclusive or exclusive. An inclusive restriction means that the user is limited to 
the printer, company, customer, consignee, shipper, carrier or document that you specify. An exclusive 
restriction means that the user can use any printer(s), company/companies, customer(s), consignee(s), 
shipper(s), carrier(s) or document(s) on your system except those that are specifically excluded.
For example, if an operator is restricted to customer ABC, only customer ABC can be accessed in CUST, only 
ABC’s inventory can be received in ENRE, only customer ABC’s inventory can be shipped in ENOR, only 
ABC’s inventory can be looked up in LOEN, only ABC’s inventory can be adjusted in ENAJ and only ABC’s 
inventory can be relocated in RELO.
If there are no restrictions for a particular operator in OPRS, that operator has access to all printers, 
companies, customers, consignees, shippers, carriers and documents.

SETTING UP COMPANIES, PROGRAMS AND USERS
Entering Operator Restrictions in OPRS
SYSTEM ADMINISTRATION GUIDE 4.2* 63
You can only change the operator restrictions of operators other than yourself. If you need to change your 
own operator restrictions, another user must log on and perform the change for you.
CUSTOMER/CONSIGNEE/SHIPPER/CARRIER/DOCUMENT TABS
These tabs are only available if you define an inclusive company restriction in the Company Block. Exclusive 
companies cannot be restricted by customer, consignee, shipper, carrier or document.
FIELD DESCRIPTIONS
Operator Code Your operator code. You cannot change the restrictions of an operator who is 
currently logged on.
Printer Code The printer or printers that the operator is restricted to. If you leave this field 
blank, the operator will have access to all printers.
Company Code The company or companies that the operator is restricted to. If you leave this 
field blank, the operator will have access to all companies.
Inclusive/Exclusive If you set the company to Inclusive, the operator is restricted to that company. 
If you set the company to Exclusive, the operator can use any company on 
your system except those that are specifically excluded.
You can enter multiple restrictions per company, but all restrictions must be of 
the same type; that is, either inclusive or exclusive.
FIELD DESCRIPTIONS
Customer Code The customer or customers that the operator is restricted to. If you leave this 
field blank, the operator will have access to all customers.
Inclusive/Exclusive If you set the customer to Inclusive, the operator is restricted to that customer. 
If you set the company to Exclusive, the operator can use any customer on 
your system except those that are specifically excluded.
You can enter multiple restrictions per customer, but all restrictions must be of 
the same type; that is, either inclusive or exclusive.
Consignee Code The consignee or consignees that the operator is restricted to. If you leave this 
field blank, the operator will have access to all consignees.
Consignee restrictions apply to the following programs: CONS, ENOR and 
LOOR.

SETTING UP COMPANIES, PROGRAMS AND USERS
Entering Operator Restrictions in OPRS
1 Enter OPRS.
Inclusive/Exclusive If you set the consignee to Inclusive, the operator is restricted to that consignee. If you set the company to Exclusive, the operator can use any consignee on your system except those that are specifically excluded.
You can enter multiple restrictions per consignee, but all restrictions must be 
of the same type; that is, either inclusive or exclusive.
Shipper Code The shipper or shippers that the operator is restricted to. If you leave this field 
blank, the operator will have access to all shippers.
Shipper restrictions apply to the following programs: SHIP, ENRE and LORE.
Inclusive/Exclusive If you set the shipper to Inclusive, the operator is restricted to that shipper. If 
you set the company to Exclusive, the operator can use any shipper on your 
system except those that are specifically excluded.
You can enter multiple restrictions per shipper, but all restrictions must be of 
the same type; that is, either inclusive or exclusive.
Carrier Code The carrier or carriers that the operator is restricted to. If you leave this field 
blank, the operator will have access to all carriers.
Carrier restrictions apply to the following programs: CARR, ENRE, ENOR, 
LORE and LOOR.
Inclusive/Exclusive If you set the carrier to Inclusive, the operator is restricted to that carrier. If you 
set the company to Exclusive, the operator can use any carrier on your system except those that are specifically excluded.
You can enter multiple restrictions per carrier, but all restrictions must be of the 
same type; that is, either inclusive or exclusive.
Document Code The document or documents that the operator is restricted to. If you leave this 
field blank, the operator will have access to all documents.
Document restrictions apply to the following programs: DOCU, PRRE, PRRM, 
PROM and PROR. They also apply to e-Vista.
Inclusive/Exclusive If you set the document to Inclusive, the operator is restricted to that document. If you set the company to Exclusive, the operator can use any document on your system except those that are specifically excluded.
You can enter multiple restrictions per document, but all restrictions must be of 
the same type; that is, either inclusive or exclusive.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Entering Operator Restrictions in OPRS
SYSTEM ADMINISTRATION GUIDE 4.2* 65

Operator Restrictions (OPRS)
2 Key in the operator code whose restrictions you wish to change and press Enter.
3 Click on Company Block.
4 In the Company Block, click on Create Record.
5 Key in your company code restriction and press Enter.
If you wish to enter a printer 
restriction:
If you do not wish to enter a 
printer restriction:
a) Key in your printer code and 
press Enter.
b) Press Enter to bypass the Correct field.
c) Repeat the above two steps for 
each additional printer that you 
wish to add.
d) When you finishing adding your 
printers, click on Return to Main 
to exit Create Mode.
a) Proceed to next step. 

SETTING UP COMPANIES, PROGRAMS AND USERS
Entering Operator Restrictions in OPRS
6 Do one of the following:

Operator Restrictions (OPRS) showing an operator limited to customer A in company V6
7 When you finish entering your restrictions, click on Return to Main and Company Block. Then click on 
Printer Block and Operator Block. Lastly, click on Exit to exit.
REMOVING RESTRICTIONS
You remove restrictions by deleting the appropriate code in the block or tab containing the restriction.
1 Enter OPRS.
2 Key in your operator code and press Enter.
3 Go to the block or tab containing the restriction that you wish to remove.
If you wish to enter a customer, 
consignee, shipper, carrier or 
document restriction:
If you do not wish to enter any 
further restrictions:
a) Click on the appropriate tab.
b) Click on Inclusive/Exclusive until 
the correct value is displayed.
c) Key in the appropriate customer, 
consignee, shipper, carrier or 
document code and press Enter.
d) Press Enter again to bypass the 
Correct field.
e) Repeat the above two steps for 
each additional code that you 
wish to add.
f) If you wish to define restrictions 
on another tab, click on the tab 
and then repeat the above steps.
a) Proceed to next step.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Roles in ROMA
SYSTEM ADMINISTRATION GUIDE 4.2* 67
4 Press the tab key until the Delete command is displayed for the restriction that you wish to remove.
5 Click on Delete.
6 If you are in the Customer, Consignee, Shipper, Carrier or Document tab, click on Company Block.
7 Click on Printer Block and Operator Code. Then click on Exit to exit OPRS. 
Setting Up Roles in ROMA
d’Amigo and e-Filing use role-based access control to determine which users have access to which functions. 
A role is a classification for security purposes that defines which functions a particular user has access to. For 
example, you could create a role called OFFICE and attach to this role all your office users. Office users 
would have access only to those d’Amigo menus and templates that office users need. 
Likewise, you could create a role called SUPERVISOR and attach to this role all your supervisors. Supervisors would have access only to those e-Filing document types and functions that supervisors need.
You set up your roles in the program ROMA (Role). ActiveDesktop supports role overlapping; that is, the 
same operator can be attached to as many roles as required.
1 Enter ROMA.

Role (ROMA) screen
2 Click on Create Record .
3 Key in your role code and press Enter.
4 Key in a description for your role code and press Enter.
5 Click on Save .
6 Click on Attach Operator .

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Roles in ROMA

Role (ROMA) screen showing Operator pick list
7 Click on the operators that you wish to select. If you wish to select all operators, you can click on Select 
All. If you wish to deselect all operators, click on Deselect All.
8 When you finish making your selections, click on Save .
9 Click on Return and then Exit .
DELETING A ROLE
If there are no dependencies such as operators, d’Amigo templates or e-Filing records attached to a role, 
deleting it will remove it from AccellosOne 3PL. If there are dependencies such as operators, d’Amigo 
templates or e-Filing records attached to a role, deleting a role will deactivate it only.
1 Enter ROMA.
2 Select the role that you wish to delete.
3 Click on Delete .
4 Click on Exit .
MODIFYING A ROLE
You can add operators to, and remove operators from, a role at any time.
1 Enter ROMA.
2 Select the role that you wish to modify.
3 Click on Edit.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up Roles in ROMA
SYSTEM ADMINISTRATION GUIDE 4.2* 69
4 Select the operators that you wish to add to the role and/or deselect the operators that you wish to 
remove from the role.
5 When you finish making your selections and deselections, click Ok.
6 Click on Exit .
LOOKING UP AN OPERATOR’S ROLES
If an operator is attached to multiple roles, you can use the Look Up Roles command to see which roles the 
operator has access to.
1 Click on Look Up Roles .

Look Up Roles screen
2 Select your operator from the dropdown list.
3 Click on Execute Query .

ROMA screen showing operator attached to two roles
4 When you finish looking up your role information, click on Return to close the Look Up Roles window.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up ActiveDesktop Security Administrators in ADSA
Setting Up ActiveDesktop Security Administrators in ADSA
In this program, you set up your ActiveDesktop security administrator(s). An ActiveDesktop security administrator is an operator set up in OPER who has access to one or more d’Amigo security administration 
functions. If you do not set up an operator in ADSA, the operator cannot perform security administration 
functions and has access to only those templates assigned to the operator in ROMA (Roles). 
1 Enter ADSA.

ActiveDesktop Security Administrator (ADSA) screen showing D4SUPPORT as a security administrator
2 If the operator that you wish to set up for ActiveDesktop security is not shown in the list of operators on 
the left-side of the screen, click on Create Record .
3 Key in your operator code and press Enter or select the appropriate operator code from the pick list.
FIELD DESCRIPTIONS
Operator Code (OPER) The operator that you wish to set up for ActiveDesktop security. This operator 
must be defined as a system administrator in OPER.
Global Access Privilege If you check the Global Access checkbox, the operator is attached to a special 
role called Global and can view all d'Amigo templates and views. If you do 
NOT check the Global Access checkbox, the operator can only view those 
templates assigned to the operator in ROMA (Roles).
Alter Template Privilege If you check the Alter Template Privilege checkbox, the operator can create, 
modify and delete templates. If you do NOT check the Alter Template Privilege 
checkbox, the operator cannot create, modify and delete templates.
Alter View Privilege If you check the Alter View Privilege checkbox, the operator can modify and 
delete any view. If you do NOT check the Alter View Privilege checkbox, the 
operator can only modify and delete views created by him/herself.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up e-Filing Security
SYSTEM ADMINISTRATION GUIDE 4.2* 71
4 Click on the appropriate checkboxes (Global Access Privilege, Alter Template Privilege, Alter View Privilege) to assign your operator the correct access.
5 When you finish setting up your ActiveDesktop security administrator, click on Save .
6 Click on Exit to exit ADSA.
DELETING A SECURITY ADMINISTRATOR
1 Enter ADSA.
2 Select the operator that you wish to delete.
3 Click on Delete .
4 Click on Exit .
Setting Up e-Filing Security
Access to e-Filing is governed by ActiveDesktop’s role-based security system. Users must be given access to 
the appropriate document types and functions in ROMA (Roles).
Document types refer to which indexes a user has access to. Valid values are any index, carrier, company, 
customer, invoice, item, no index, order, receipt and shipper. Functions refer to which function(s) a user 
attached to a particular role is allowed to perform. The list of available functions includes:
 purge document
 batch upload
 update document information
 upload document
1 Create a new role in ROMA for e-Filing security or retrieve an existing role.
2 Attach the appropriate operators to your new or existing role.
3 Click on the e-Filing tab.
NOTE Operators can be attached to multiple roles in ROMA. If the same operator 
is assigned to two or more roles and those roles have different e-Filing document 
types and functions, the operator will have access to all document types and functions for those two or more roles.

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up e-Filing Security

ROMA screen showing e-Filing tab
4 Click on Attach Operator .

ROMA screen showing no access for OFFICE
5 Select the document type that you wish to give access to.
6 Select the function that you wish to give access to.
7 Click on Save to add the document type/function to the left-hand column.
8 Repeat the above three steps for each additional document type and function that you wish to add.
If your role has access to some document types and not others (that is, it does not have access to “Any 
Index), you must set up document types and functions for each document type/function combination.
For example, if your role has access to consignee, customer and shipper document types and two functions (Purge document and Batch upload), you must create six records in ROMA:
consignee / Purge document
consignee / Batch upload
customer / Purge document
customer / Batch upload
shipper / Purge document

SETTING UP COMPANIES, PROGRAMS AND USERS
Setting Up e-Filing Security
SYSTEM ADMINISTRATION GUIDE 4.2* 73
shipper / Batch upload

ROMA screen showing three functions attached to the customer and item document type
9 When you finish setting up your e-Filing security, click on Return .

ROMA screen showing access for OFFICE
10 Click on Exit .
REMOVING DOCUMENT TYPES AND FUNCTIONS FROM A ROLE
1 Retrieve the role whose access you wish to modify.
2 Click on the e-Filing tab.
3 Click on Attach e-Filing Codes .
4 Double click the document type/function that you wish to remove.

SETTING UP COMPANIES, PROGRAMS AND USERS
Activating the ActiveDesktop Icons
5 Click on Delete .
6 Click on Return .
7 Click on Exit .
Activating the ActiveDesktop Icons
All users are automatically given access to the AccellosOne 3PL and Password Change icons in ActiveDesktop. All other icons (for example, Alert Maintenance, Operational Board, d’Amigo, e-Filing, etc.) must be 
manually assigned to each user in OPAC (Operator Access). If a user does not have access to a ActiveDesktop icon, that icon will not appear when the user logs on and the user will have no access to the 
program.
System administrators are automatically given access to all ActiveDesktop icons; they do not need to be 
assigned to icons in OPAC.
ActiveDesktop icons are listed under the subsystem code ACTIVE in OPAC. There are nine possible icons 
that a user can have access to:
NOTE Access to an ActiveDesktop icon will display that icon when the user logs 
onto ActiveDesktop. However, all other security conditions must be satisfied before 
the user can enter the program and work in it. For example, to view documents in eFiling, the user must be assigned the appropriate document types and functions in 
ROMA (Role).
SELECTION 
CODE DESCRIPTION
ADBART BarTender Label Printing
ADDASH Operational Board
ADEFIL e-Filing
ADLERT Alert Maintenance
ADMIGO d’Amigo
ADSIGN Signature Capture
ADSQL SQL Pad

SETTING UP COMPANIES, PROGRAMS AND USERS
Modifying Your Installation Parameters in INST
SYSTEM ADMINISTRATION GUIDE 4.2* 75
1 Enter OPAC.
2 Key in ACTIVE as your subsystem code and press Enter.

OPAC screen showing the ACTIVE subsystem code
3 Click on Operator Block and proceed to add the appropriate operators to the appropriate selection codes.
4 When you finish adding your operators, click on Master Block, Subsystem Code and Exit.
Modifying Your Installation Parameters in INST
In this program, you set up your installation parameters. Installation parameters define the facility in which 
your computer is located and certain system-wide parameters such as the date delimiter and format, 
password expiry dates, etc. Currently, only password expiry dates and ActiveDesktop security are implemented in INST. 
ADVIST e-Vista
ADWAVE Wave Manager
FIELD DESCRIPTIONS
Installation Name The name of your installation.
SELECTION 
CODE DESCRIPTION

SETTING UP COMPANIES, PROGRAMS AND USERS
Modifying Your Installation Parameters in INST
Address Line 1/2/3 The address of your installation.
ZIP/Postal Code (ZIPO) The ZIP or postal code of your installation.
Date Delimiter Reserved for future use.
Date Format Reserved for future use.
Allowable Selection Entry 
Errors
Reserved for future use.
Enable ActiveDesktop 
Security
Y = Yes
N = No
If you select Yes, ActiveDesktop security will be enabled. d’Amigo users can 
only access the menus and templates attached to their role in ROMA and eFiling users can only access the document types and functions attached to 
their roles in ROMA.
If you select No, ActiveDesktop security will be disabled. Any d’Amigo user will 
be able to access, modify and delete any template or view and any e-Filing 
user will have access to all document types and all functions. 
Print Restrictions on 
Reports
Reserved for future use.
Default Password The default password for your environment. For example. if the default password is set to “CHANGEIT” and a user called Tom wishes to log on for the first 
time, he must enter TOMCHANGEIT as his password.
Passwords Expire in 
(Days)
This field allows you to define an expiry date for all user passwords in your 
installation. You activate this feature by entering the appropriate number of 
days in the Passwords Expiry in (Days) field. A password is considered to be 
expired when the date that the password was last changed plus the number of 
days that you specify in the Passwords Expire in (Days) field is a date in the 
past.
EXAMPLE
You have three operators on your system and you enter a value of 30 days in 
this field. Operator 1, who was added to the system on the same day, will have 
to change his password in 30 days. Operator 2, who was added to the system 
six months ago, will have to change his password immediately. Operator 3, 
who was added to the system six months ago and had his password changed 
one week ago, will have to change his password in three weeks or 21 days.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Modifying Your Installation Parameters in INST
SYSTEM ADMINISTRATION GUIDE 4.2* 77
1 Enter INST.
If you leave this field blank, passwords will not expire until they are reset by a 
system administrator in ROPA (Reset Operator Password) or manually 
changed by the user using the Password Change function in ActiveDesktop.
Application Home DirectoryFor HighJump use only.
Document Archive DirectoryThe archive directory for order and receipt documents printed in PRRE, 
PRRM, PROM and PROR. If you set up an archive directory, any document 
that you print in these programs will be automatically moved to this directory 
after the number of months specified in the next field has passed.
Storing large numbers of old receipt and order documents in a directory other 
than the application home directory makes it possible to query for an old bill of 
lading, for example, without affecting the performance of day-to-day operations in AccellosOne 3PL.
Receipt and order documents stored in the archive directory can be viewed in 
LORE and LOOR like any other receipt or order document.
Number of Months to 
Retain Documents in 
Home Directory
The number of months that receipt or order documents will be kept in the 
application home directory before being move to the archive directory.
FIELD DESCRIPTIONS

SETTING UP COMPANIES, PROGRAMS AND USERS
Modifying Your Installation Parameters in INST

Installation Parameters (INST) screen
2 When you finish modifying your installation parameters, click on Exit to exit.

SYSTEM ADMINISTRATION GUIDE 4.2* 79
ARCHIVING AND PURGING
Overview ............................................................................................................ 80
Setting Up Archiving and Purging................................................................... 82
COMP (Company Code).............................................................................. 82
OPER (Operator Code)................................................................................ 82
Archiving Receipts, Orders, Inventory and Charges in ARPU...................... 83
Archiving Receipts and Orders .................................................................... 83
Archiving Inventory ...................................................................................... 85
Archiving Accessorial and Immediate Charges ........................................... 87
Looking Up Archived Records......................................................................... 88
Looking Up Archived Orders in LOOR......................................................... 88
Looking Up Archived Receipts in LORE ...................................................... 89
Looking Up Archived Inventory in LOEN ..................................................... 90
Looking Up Archive Registers in ARPU....................................................... 92
Deleting the Archive in DEAR .......................................................................... 94
Miscellaneous Purging ..................................................................................... 96
Purging the Spooler Files in SPPA .............................................................. 96
Purging Warnings and Messages ................................................................ 97

ARCHIVING AND PURGING
Overview
Overview
Purging your system of old data is an essential element of system maintenance and must be done on a 
regular basis to maintain system performance and to avoid running out of disk storage space. For example, 
every month you remove all records older than one year. If you do not perform a purge on a regular basis, 
your system performance will suffer considerably.
Archiving and purging in AccellosOne 3PL is a two-step process:
Archiving and purging can be done during normal business hours. However, because system performance 
may be affected, it is best done during weekends and off hours.
ARPU (Archive/Purge 
Processing)
First, you run ARPU. This program moves the selected data from the regular 
system tables to the corresponding archive tables. For example, order headers in E_ORD_H are moved to the archive table H_ORD_H.
DEAR (Delete Archive 
Purge)
Second, you run DEAR. This program removes the records physically from 
the database and deletes the archive file.

ARCHIVING AND PURGING
Overview
SYSTEM ADMINISTRATION GUIDE 4.2* 81
There is a maximum of four steps to follow in archiving and purging:
ARPU
LOOR
LORE
LOEN
DEAR
Look up 
archived 
records?
Yes No
The system creates a register for the 
data and moves the archived data to 
the appropriate archive table. For 
example, order header data is moved 
from E_ORD_H to H_ORD_H.
You archive your receipts, orders, 
inventory and charge records in ARPU 
(Archive/Purge Processing). 
If you wish to look up the orders, 
receipts and inventory records that 
have been archived, you use the 
regular look-up programs (LOOR, 
LORE, LOEN).
You purge the records that you 
archived in step 1 in DEAR (Delete 
Archive Purge). This step is final and 
cannot be reversed.
Minimum number of 
months to retain archive 
data has passed?
Yes
No

ARCHIVING AND PURGING
Setting Up Archiving and Purging
Setting Up Archiving and Purging
There are two setup programs for archiving and purging: COMP (Company Code) and OPER (Operator 
Code).
COMP (COMPANY CODE)
In COMP you define the following:
 the minimum number of months to retain archived data before the data can be purged in DEAR
 whether or not to allow multiple archive/purge selections in ARPU (multiple selections could affect system performance)
COMP screen
OPER (OPERATOR CODE)
In OPER you give operators permission to look up archived data in LOOR, LORE and LOEN.

ARCHIVING AND PURGING
Archiving Receipts, Orders, Inventory and Charges in ARPU
SYSTEM ADMINISTRATION GUIDE 4.2* 83
OPER screen
Archiving Receipts, Orders, Inventory and Charges in ARPU
You archive receipts, orders, inventory, accessorial charges and immediate charges in ARPU (Archive/Purge 
Processing). In this program you specify the customer, if any, whose records you wish to archive and your 
cut-off date for the archive.
Depending on the option that you selected in the Allow Multiple Archive/Purge Selections field in COMP, you 
can archive all five types in one operation or you can run ARPU separately for each type of archiving.
ARCHIVING RECEIPTS AND ORDERS
There are three conditions that must be met before you can archive a receipt or order:
 the receipt or order must have a status of confirmed or deleted; if you manually rate receipts, the confirmed receipt must also be rated
 for confirmed receipts and orders, the confirmation date must be less than or equal to the archive’s cutoff date 
 for deleted receipts and orders, the order or receipt date must be less than the archive’s cut-off date 
1 Enter ARPU.

ARCHIVING AND PURGING
Archiving Receipts, Orders, Inventory and Charges in ARPU

Archive/Purge Processing (ARPU)
2 Click on New to create a new archive.
3 Key in your cut-off date in the To Date field and press Enter. When you enter your date, AccellosOne 3PL 
will archive all orders or receipts as follows:
for confirmed orders the order confirmation date is less than the cut-off date
for deleted orders the order date is less than the cut-off date
for confirmed receipts the receipt confirmation date is less than the cut-off date
for deleted receipts the receipt date is less than the cut-off date
TIP If you have a lot of data to archive or have not created an archive for a long 
time, it is recommended that you start with an early date range; for example, one 
month after the start of business date or one month after the last purge, etc. When 
you finish your first archive, increment the cut-off date by one month and perform the 
second archive. By splitting your archives into multiple jobs, you can reduce the affect 
on system performance.

ARCHIVING AND PURGING
Archiving Receipts, Orders, Inventory and Charges in ARPU
SYSTEM ADMINISTRATION GUIDE 4.2* 85
4 Key in your customer code and press Enter. Only data for the customer or customers that you enter in 
this field will be archived. If you leave this field blank, the archive will include data for all customers.
5 Click in the Process Orders or Process Receipts checkbox.
6 Click on Save . AccellosOne 3PL will generate a register number for the archive.

Archive/Purge Processing (ARPU) screen showing register number and status
7 Click on Process .
8 When all records have been archived, ARPU will close and you will be returned to the main menu.
ARCHIVING INVENTORY
The way in which the archives inventory option works depends upon the number of inventory levels of your 
inventory. If your inventory is item-level only, the system archives history records only. A history record is any 
record in the History Block or History Details Block of LOEN. If your inventory has two or more inventory 
levels, the system archives the entire entity.
NOTE Inventory attributes and inventory level descriptions are excluded from 
archiving and purging.

ARCHIVING AND PURGING
Archiving Receipts, Orders, Inventory and Charges in ARPU
See the following for the rules governing item only inventory versus inventory with two or more levels:
When history records are archived, you can no longer run transaction history reports like THIC (Transaction 
History) and THIS (Transaction History Report) for the purged level 2 and higher entities.
Archiving inventory is a two-step process. First you run CNBC (Clear Non-Billing Customer). Then you run 
ARPU (Process Inventory option).
1 Make sure that billing has run for the inventory that you wish to purge. You run billing by generating and 
confirming a renewal batch in BILB or by running RENW.
2 Enter CNBC.
3 Key in your customer code and press Enter.
For item-only inventory For inventory with two or more levels
The system will evaluate the following conditions:
 there are no open orders or receipts containing the item
 billing has run for all transactions for this item
If all conditions are met for a given item, the system will calculate the brought-forward balances for the available, on-hand, 
on order, etc. quantities as of the cut-off date and then delete 
all history records up until this date. If the new brought-forward 
balance is not zero, the system will create a new history record 
in LOEN with a type of BF (Brought Forward Balance). If the 
new brought-forward balance is zero, no new record is created 
in LOEN.
The system will evaluate the following conditions:
 the inventory balances for the entity are zero
 there are no transactions after the cut-off date
 there are no open orders or receipts containing that inventory entity
 billing has run for all transactions for this entity
If all conditions are met for a given entity, the system will 
archive the entire entity (for example, item A, lot 10) and all 
associated records (that is, the Location Block, History Block 
and Renewal Block).
TIP If you do not use AccellosOne 3PL to generate invoices and track revenue and 
if you have set the Rate Receipt Automatically flag in DBIP to N for No, you can use 
the special verification program RATE to “rate” your receipts. When attached to the 
flow CORE with the Sequence flag is set to A for After, RATE marks confirmed 
receipts as “rated”, thereby allowing them to be archived in ARPU without running 
CNBC (Clear Non-Billing Customer).
See “SPECIAL VERIFICATION PROGRAMS” on page 193 for further information on setting 
up special verification programs.

ARCHIVING AND PURGING
Archiving Receipts, Orders, Inventory and Charges in ARPU
SYSTEM ADMINISTRATION GUIDE 4.2* 87

Clear Non-Billing Customer (CNBC)
4 Click on Process.
5 If the customer has active billing records, a message will appear. Press Enter to acknowledge the message. An active billing record is a charge in ENAC with a status of Active for Active and a charge total 
that does not equal zero. If there is an active billing record for inventory included in the purge, that inventory cannot be purged. You must delete the record and then rerun CNBC.
6 Enter ARPU.
7 Click on New to create a new archive.
8 Key in your cut-off date in the To Date field and press Enter. For item-only inventory, the system will 
purge all history records up until this date; for level 2 and higher entities, the system will purge all records 
in LOEN for the entity (Location Block, History Block and Renewal Block).
9 Key in your customer code and press Enter. Only data for the customer or customers that you enter in 
this field will be purged. If you leave this field blank, the purge will include data for all customers.
10 Click on the Process Inventory checkbox to select it.
11 Click on Save . AccellosOne 3PL will generate a register number for the new archive.
12 Click on Process .
13 When all records have been archived, ARPU will close and you will be returned to the main menu.
ARCHIVING ACCESSORIAL AND IMMEDIATE CHARGES
The charge must be invoiced and posted to the Daily Invoice Register through BILB (Billing Batch) before you 
can archive it in ARPU. For manual charges, the cut-off date in ARPU is based on the date that the charge 
was created in ENAC or ENIN. For automatic charges, the cut-off date in ARPU is based on the date that the 
receipt or order to which the charge is attached was confirmed.
1 Enter ARPU.
2 Click on New to create a new archive.

ARCHIVING AND PURGING
Looking Up Archived Records
3 Key in your cut-off date and press Enter.
4 Key in your customer code and press Enter. Only data for the customer or customers that you enter in 
this field will be purged. If you leave this field blank, the purge will include data for all customers.
5 Click on the Process Accessorial and Process Immediate Invoices checkboxes to select them.
6 Click on Save . AccellosOne 3PL will generate a register number for the new archive.
7 Click on Process .
8 When all records have been archived, ARPU will close and you will be returned to the main menu.
Looking Up Archived Records
You look up your archived data for orders, receipts and inventory in the normal look-up programs; that is, 
LOOR (Look Up Orders), LORE (Look Up Receipts) and LOEN (Look Up Inventory). For orders, receipts and 
inventory, the archive number will display in the Header Block of LOOR, LORE and LOEN respectively.
Archived accessorial and immediate charges do not display an archive message in ENAC or ENIN.
LOOKING UP ARCHIVED ORDERS IN LOOR
You look up orders that have been archived in LOOR.
1 Enter LOOR.
2 Key in your search criteria and click on Execute Query.

ARCHIVING AND PURGING
Looking Up Archived Records
SYSTEM ADMINISTRATION GUIDE 4.2* 89

Look Up Orders (LOOR) screen showing archive 102
3 When you finish looking up your archived orders, click on Exit to exit.
LOOKING UP ARCHIVED RECEIPTS IN LORE
You look up receipts that have been archived in LORE.
1 Enter LORE.
2 Key in your search criteria and click on Execute Query.

ARCHIVING AND PURGING
Looking Up Archived Records

Look Up Receipts (LORE) screen showing archive 103
3 When you finish looking up your archived receipts, click on Exit to exit.
LOOKING UP ARCHIVED INVENTORY IN LOEN
You look up inventory records that have been archived in LOEN. 
1 Enter LOEN.
2 Key in your search criteria and click on Execute Query.

ARCHIVING AND PURGING
Looking Up Archived Records
SYSTEM ADMINISTRATION GUIDE 4.2* 91

Look Up Inventory (LOEN) screen showing archive 2
3 Use your arrow keys to scroll forward and backward through your inventory records.
4 When you finish looking up your archived inventory, click on Exit to exit.
LOOKING UP ARCHIVE REGISTERS IN ARPU
After creating a new archive register, you can look up the register to find out the run date, the total number of 
records purged as well as the total number of records purged by individual table.
1 Enter ARPU.
2 Click on Enter Criteria.
3 Key in your register number, cut-off date or customer restriction and click on Execute Query.

ARCHIVING AND PURGING
Looking Up Archived Records

Archive/Purge Processing (ARPU) screen showing register number, run date and total number of 
records archived
4 Click on Table Details to see all tables included in the archive as well as the actual number of 
records purged from each table.

ARCHIVING AND PURGING
Deleting the Archive in DEAR
SYSTEM ADMINISTRATION GUIDE 4.2* 93
ARPU screen showing table details
5 When you finish looking up your archive registers, click on Exit twice to exit.
Deleting the Archive in DEAR
You perform the actual purge in DEAR (Delete Archive/Purge). This program removes from the database all 
the records that you archived in ARPU.
You can delete archives in one of two ways: by register number or by cut-off date.
When you delete by register number, DEAR calculates all the possible records in that register that meet the 
minimum number of months to retain archived data value that you defined in COMP. If all records in the 
register meet the minimum number of months condition (that is, less than or equal to the current date minus 
the number of months that you specified in COMP), the records are purged and the register is deleted. If there 
are newer records in the register, the newer records will not be purged and the register will remain open.
CAUTION This step is final and cannot be reversed. You cannot retrieve the 
purged records and restore them to the database.

ARCHIVING AND PURGING
Deleting the Archive in DEAR
When you delete by cut-off date, DEAR validates that your cut-off date is less than or equal the current date 
minus the number of months that you specified in COMP. If this condition is met, DEAR performs the following 
tasks:
 if all records in a given open register meet the minimum number of months condition, the records are 
purged and the register is delete
 if there are newer records in a given open register, the newer records will not be purged and the register 
will remain open
1 Enter DEAR.
2 Do one of the following:

Delete Archive/Purge (DEAR)
3 Click on Process .
To delete by register number: To delete by cut-off date:
a) Key in your purge register number and press Enter.a) Press Enter to bypass the Purge 
Register Number field.
b) Key in your cut-off date and 
press Enter.
c) If your cut-off date is not acceptable, an error message will display in the hint line. Press Delete 
to clear the date and enter a new 
cut-off date.

ARCHIVING AND PURGING
Miscellaneous Purging
SYSTEM ADMINISTRATION GUIDE 4.2* 95
Miscellaneous Purging
PURGING THE SPOOLER FILES IN SPPA
Every time that you print a document or report to a printer other than NONE or VIEW, the system creates a file 
in the print spooler. It is necessary to purge these files on a regular basis in order to ensure that you do not 
run out of disk space.
You set up your purge parameters in SPPA (Spool Parameters). Based on the parameters that you enter in 
this program, the system will automatically purge your reports and documents after a given number of days.
In SPPA you set up two things:
 your default purge parameters 
 any exceptions to your defaults; an exception can apply to a particular document or to a particular document printed for a particular customer 
For example, suppose your system default is set up to purge all reports and documents after three days. An 
exception could be made, however, for your bill of lading document, which would be retained for five days 
rather than three. A further exception could be made for bill of lading documents produced for ABC 
SUPPLIES, which would be retained for ten days. 
1 Enter SPPA.
2 In the Automatic Purge of Spool Files field, key in Y for Yes and press Enter.
3 In the Number of Days for Purge Retention field, key in the number of days that you wish to keep your 
spooler files and press Enter. The value that you enter in this field is your system default.
If you wish to add exceptions to 
your spooler parameters:
If you do NOT wish to add 
exceptions to your spooler 
parameters:
a) In the Customer field of the Document Block, key in the customer 
code for your exception or use 
.ALL for all customers and press 
Enter.
b) In the Type field, key in S for 
Report or D for Document and 
press Enter.
c) In the Code field, key in your 
document or report code and 
press Enter or use your pick list 
to select it.
d) In the Days to Retain field, key in 
the number of days that you wish 
to retain this document or report 
and press Enter.
e) Repeat the above steps for each 
additional exception that you 
wish to add.
a) Proceed to next step.

ARCHIVING AND PURGING
Miscellaneous Purging

Spool Parameters showing three exceptions — one for all customers and one for customer A
4 When you finish setting up your spooler parameters, click on Master Block and Exit to exit.
PURGING WARNINGS AND MESSAGES
Whenever a warning message is generated in AccellosOne 3PL, the system creates a record in WAME (Look 
Up Warnings/Messages) that allows you to look up this message at any time. Messages remain in WAME 
until you purge them in PUWM (Purge Warnings/Messages).
LOOKING UP WARNING MESSAGES (WAME)
You look up your warning messages in WAME (Look Up Warnings/Messages). For each warning message, 
WAME shows:
 the sequence number (a system-generated number that you can use to track a particular message)
 the routine code (the program that was running when the problem was encountered)
 the date and time that the message occurred
 the operator code of the operator who viewed the message
 the date and time that the operator viewed the message
 the message text
There are two look-up options in this program. You can view either new messages or old messages. A new 
message is a message that has not been previously viewed. An old message is a message that has been 
previously viewed by any operator. 

ARCHIVING AND PURGING
Miscellaneous Purging
SYSTEM ADMINISTRATION GUIDE 4.2* 97
A message is flagged as viewed when you position your cursor beside the sequence number of the message. 
For example, if you use your arrow keys to cursor down through the first five records in WAME, these five 
records will all be flagged as viewed; however, any remaining records will have a status of unviewed. 
1 Enter WAME.
2 Click on Enter Criteria.
3 Click Execute Query.
TIP If you wish to scroll through your records without flagging them as viewed, use 
your page up and page down keys — not your arrow keys. When you use your page 
up and page down keys, only the first message of each page is flagged as viewed.
If … then …
you wish to look up all new messages Proceed to next step.
you wish to look up all messages that have 
been previously viewed
Press Enter until your cursor is positioned 
in the Viewed by field. Then key in the code 
ALL.
you wish to query on a particular warning 
message that has NOT been previously 
viewed
Key in the sequence number (if known), 
routine code or message date of the message.
you wish to query on a particular warning 
message that HAS been previously viewed
Key in the sequence number, routine code 
or message date of the message. Then key 
in one of the following: a value in the 
Viewed by field (ALL or the code of the 
actual operator who viewed the message) 
or the date that the message was viewed.

ARCHIVING AND PURGING
Miscellaneous Purging

Look Up Warnings/Messages (WAME) screen showing details for sequence number 558168
4 Click on Text Block to enter the Text Block.
5 If the number of lines in the Text Block exceeds 7, use your arrow keys to view the entire message. 
6 When you finish looking up your warning messages, click on Master Block and Exit to exit.
PURGING WARNING MESSAGES (PUWM)
You purge your warning messages in PUWM (Purge Warnings/ Messages). Purging warning messages is a 
one-step process; no archive file is created and you cannot reverse PUWM and restore the warning 
messages to the database.
You can only purge previously viewed messages; if the message has not been previously viewed, it will not 
be purged.
PUWM allows you to specify the number of records that Oracle will process before committing the purge. This 
option makes it possible to split up a large job into smaller segments. Each segment is performed separately 
and should your system fail in the middle of a segment, only that segment will have to be rerun — not 
previous segments.

ARCHIVING AND PURGING
Miscellaneous Purging
SYSTEM ADMINISTRATION GUIDE 4.2* 99
Consider the following examples in which you have a total of 1,000 records to purge:
If you specify a small number (say, 50), the purge will take longer but fewer system resources will be 
consumed and other programs will run faster. If you specify a large number (say, 1,000), the purge will be 
completely more quickly but more system resources will be consumed and other programs might be affected. 
The default number of record is 100.
1 Enter PUWM.

Purge Warnings/Messages (PUWM)
2 If required, change the value in the Records to Commit field and press Enter.
3 Click on Execute Purge.
EXAMPLE 1 EXAMPLE 2
Total records to process = 1,000
Records to commit = 100
Job fails at record = 940
Records 1 to 899 will already be committed. 
When you rerun PURB, only records 900 to 
1,000 will have to be reprocessed.
Total records to process = 1,000
Records to commit = 1,000
Job fails at record = 940
No records will be committed. When you 
rerun PURB, all 1,000 records will have to 
be reprocessed.

ARCHIVING AND PURGING
Miscellaneous Purging

SYSTEM ADMINISTRATION GUIDE 4.2* 101
CONVERSIONS
Overview .......................................................................................................... 102
Creating Your Excel Spreadsheets............................................................ 103
Creating Your Flat Files ............................................................................. 103
Converting Customer Details ..................................................................... 104
Converting Item Details.............................................................................. 108
Entering the Quantity Breakdown ................................................................. 108
Converting Location Details ....................................................................... 118
Converting Existing Locations.................................................................... 122
Converting Shipper Details ........................................................................ 125
Converting Carrier Details.......................................................................... 127
Converting Transaction History Details...................................................... 129
Converting Revenue Master Details .......................................................... 132
Converting ZIP Codes................................................................................ 133
Converting Inventory Balances .................................................................. 134
Converting Billing Information .................................................................... 135
Miscellaneous Conversions ....................................................................... 139
Performing the Conversion............................................................................ 139
Step 1 — Loading the Conversion in LOCO .............................................. 139
Step 2 — Viewing and Modifying the Conversion Data in MOCO ............. 140
Step 3 — Processing the Conversion in PRCO......................................... 141
Step 4 — Modifying Conversion Data in MOCO........................................ 142
Step 5 — Running COER (Conversion Exception Report) ........................ 143
Step 6 — Verifying the Converted Data..................................................... 144
Transferring Data from One Company to Another....................................... 144

CONVERSIONS
Overview
Overview
AccellosOne 3PL’s conversion programs allow you to convert data on customers, items, locations, existing 
locations, inventory balances, transaction history, consignees, shippers, carriers, ZIP codes and sales 
revenue from non-AccellosOne 3PL systems. There are nine steps to follow in performing a conversion:
EXCEL
LOCO
MOCO
PRCO
MOCO
A13PL
COER
In LOCO (Load Conversion), you load the 
appropriate file into A13PL from a csv file. 
This is a temporary table.
You view and if required modify the data in 
MOCO (Modify Conversion Data).
When you are satisfied that the information 
in MOCO is correct, you process the conversion in PRCO (Process Conversion). 
PRCO loads the information into the A13PL
tables so that it is available in the standard 
menu programs. 
You query all records in MOCO. 
You run COER (Conversion Exception 
Report) to look up the records that were not 
loaded. Any unloaded records must be 
corrected in MOCO. 
You verify the converted data by running a 
A13PL report or by looking up the converted 
data in ITEM, CONS, LOCA, etc. 
Records 
remain in 
MOCO?
No Yes
You transfer the csv file to the appropriate 
directory. 
CSV
You create an Excel spreadsheet based on 
column layouts defined in the control files.
You save your Excel spreadsheet as a csv 
file. 
FTP

CONVERSIONS
Creating Your Excel Spreadsheets
SYSTEM ADMINISTRATION GUIDE 4.2* 103
Creating Your Excel Spreadsheets
The following requirements must be met performing a conversion:
 All mandatory fields must be entered.
 Commas and apostrophes are not allowed in any column.
 The lower case “f” is not allowed in any column. Convert “f” to “F” wherever required.
 Columns must not exceed the prescribed length in any circumstances.
 Date columns should be entered in YYMMDD format.
 All columns should be formatted as text and left justified.
 No columns should have any spaces at the end; that is, padded with spaces.
 When entering numbers, no decimal is required unless you are entering a fraction and decimals must 
not be padded out with zeroes. For example, you can enter 1.07 in one field, 2 in another field, 145.6 in 
a third field, etc.
The following restrictions apply to code fields. A code field is a field like customer code, consignee code, 
shipper code, item code, location code, item billing profile code, quantity breakdown code, etc. that is created 
in an AccellosOne 3PL maintain program like CUST, ITEM, LOCA, SHIP, DBIP, etc.
 Code fields must be converted in uppercase letters. Lowercase or mixed case code fields are not valid. 
All codes should be created and available in AccellosOne 3PL before running LOCO.
 Code fields in AccellosOne 3PL do not support the single quote (’) and double quote (“) special characters. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not 
recommended. Other special characters are generally supported.
Creating Your Flat Files
AccellosOne 3PL conversion programs require csv (comma-separated values) files. You create your csv files 
using the Save As command in Excel. You can save the file to your local hard drive or to the Desktop. After 
saving your file, open it with Notepad and save it under the appropriate name. The naming convention for 
each csv file that the system looks for during a conversion is shown below:
CAUTION It is essential to carefully check your data before running PRCO. AccellosOne 3PL’s conversion utility provides only limited validation of converted data; for 
example, the item conversion does not validate that all the profiles required for a 
given item have been set up correctly in AccellosOne 3PL. If you convert bad data 
into AccellosOne 3PL, the data must be manually corrected one record at a time.
DESCRIPTION NAMING CONVENTION
Customer Master Details custcsv.dat
Item Master Details itemcsv.dat

CONVERSIONS
Converting Customer Details
Once you have created your csv file, you must move it into your DEL4 directory ($DEL4_HOME/del4/loader/
data). If you are not sure of the location of your DEL4 directory, contact the Platform Group or your HighJump 
consultant.
You cannot change these file names. All conversion files must be copied to the appropriate file name listed 
above for conversion.Once data has been copied to a .dat file, the conversion programs in AccellosOne 3PL 
can be used to complete the conversion.
Converting Customer Details
In this conversion file, you set up your customer details. The following codes and profiles must be set up 
before you can perform a customer conversion:
 ZIP/Postal Code (ZIPO)
 Depositor Billing Profile (DBIP)
 Country Code (CNTY)
 G/L Modifier Code (GLMO)
 Depositor Shipping and Receiving Profile (DSRP)
 Depositor Workflow Profile (DIFP)
 Depositor Inventory Level Profile (DILP)
 Depositor Item Profile (DITP)
Location Master Details loccsv.dat
Inventory Balances balcsv.dat
Consignee Master Details concsv.dat
Shipper Master Details shipcsv.dat
Carrier Master Details carrcsv.dat
ZIP Codes zipcsv.dat
Transaction History Conversion histcsv.dat
Revenue Master Details revncsv.dat
FIELD LENGTH MANDATORY NOTES
CUST_CODE 10 Y the customer code
CUST_NAME 30 Y the customer name
DESCRIPTION NAMING CONVENTION

CONVERSIONS
Converting Customer Details
SYSTEM ADMINISTRATION GUIDE 4.2* 105
CUST_ADD1 30 Y address line 1
CUST_ADD2 30 address line 2
CUST_ADD3 30 address line 3
ZIP_CODE 10 Y the customer’s ZIP code or postal code 
(must be set up in ZIPO)
SMAN_CODE 4 Y the salesperson code for the customer
CUST_REPS_CODE 4 Y the customer service representative for the 
customer
CUST_TP_FLAG 1 Y W = Warehouse (default)
I = Invoice Only
B = Broker
the customer’s account type
GL_MODY_CODE 10 the customer’s general ledger modifier 
code
CUST_CODE_PAY_OFFC 10 Y the customer’s paying office code
CUST_BILL_PROF_CODE 4 Y the customer’s billing profile (must be set 
up in DBIP)
CUST_OPS_PROF_CODE 4 Y the customer’s shipping and receiving profile code (must be set up in DSRP)
INFO_FLOW_PROF_CODE 4 Y the customer’s workflow profile code (must 
be set up in DIFP)
CUST_INVT_PROF_CODE 4 Y the customer’s inventory level profile code 
(must be set up in DILP)
CUST_ITEM_PROF_CODE 4 Y the customer’s item information profile 
code (must be set up in DITP)
WHSE_CODE 4 the warehouse to which the customer’s 
product is restricted (must be set up in 
WARE)
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Customer Details
CUST_START_BUS_DATE 6 Enter 010101 (YYMMDD). This date will 
allow you to backdate any receipts for the 
customer in ENRE.
CUST_LAST_ACT_DATE 6 Reserved for future use
EDI_PROF_CODE 4 the customer’s EDI profile code (must be 
set up in DEDP)
FRT_PAY_OFFC_CODE 10 Reserved for future use
CUST_FRT_PROF_CODE 4 Reserved for future use
CUST_UPC_PREX 6 this field is used to attach a predefined 
UPC prefix (five digits followed by a 
hyphen) to all of a customer’s item codes
CUST_TRF_PROF_CODE 4 the transfer profile code is used if you wish 
to transfer product from one customer to 
another within your warehouse (must be 
set up in TRPR)
CUST_DEF_RCPT_SKU_FLAG 1 Y H = High
L = Low
in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENRE when the SKU type is not specified
CUST_DEF_ORD_SKU_FLAG 1 Y H = High
L = Low
in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENOR when the SKU type is not specified
CUST_DEF_ADJ_SKU_FLAG 1 Y H = High
L = Low
in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENAJ when the SKU type is not specified
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Customer Details
SYSTEM ADMINISTRATION GUIDE 4.2* 107
CUST_LAB_CAPT_JOB_LEV_FLAG 1 Y N = No
Y = Yes
Set to N for No.
CUST_ORD_LEV_RES_NUM 1 the inventory level at which reserve logic is 
activated
CUST_CNVC_NUM 1 Reserved for future use
CUST_LAB_STD_MODY_NUM 5 the customer’s labor standard modifier 
(may have up to two decimals)
EXTRA_CHG_PROF_CODE 4 the customer’s extra charge profile code 
(must be set up in ECHP)
CUST_ADD4 30 address line 4
COUNTRY_CODE 4 Y the customer’s country code (must be set 
up in CNTY)
RF_PROF_CODE 4 the customer’s RF profile code (must be set 
up in MRFP)
INVT_TERMGY_CODE_I1 1 the first inventory terminology code to 
appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I2 1 the second inventory terminology code to 
appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I3 1 the third inventory terminology code to 
appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I4 1 the fourth inventory terminology code to 
appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I5 1 Reserved for future use.
INVT_TERMGY_CODE_O1 1 the first inventory terminology code to 
appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O2 1 the second inventory terminology code to 
appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O3 1 the third inventory terminology code to 
appear in ENOR (must be set in INTE)
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Item Details
Converting Item Details
In this conversion file, you set up your item details. The following codes and profiles must be set up before 
you can perform an item conversion:
 Customer Code (CUST)
 Class Code (CLAS)
 Commodity Code (COMM)
 General Information Profile Code (IINP)
 Item Billing Profile Code (IBIP)
 Quantity Breakdown Profile Code (IQBP)
 Item Shipping Profile Code (ITSH)
 Item Process Profile Code (IPRP)
ENTERING THE QUANTITY BREAKDOWN
You enter an item’s quantity breakdown in the VAR_QTY_BKD-_QTY1/2/3/4/5 fields. If your item has a single 
quantity breakdown (for example, cases only), you enter a 1 in the ITEM_QTY_BKD_BASE_NUM field and a 
1 in the VAR_QTY_BKD_QTY1 field. If your item has multiple SKU types in its quantity breakdown, you set 
the smallest SKU type to 1 and the next highest SKU type to the number of units of the smaller SKU type that 
fit in the next highest SKU type.
For example, if your quantity breakdown were 10 eaches per case and 60 cases per pallet, you would enter 
the following:
INVT_TERMGY_CODE_O4 1 the four inventory terminology code to 
appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O5 1 Reserved for future use.
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program to indicate records that 
have been processed versus those that 
may have failed and are still pending.
TEL_LIST_CODE 4 the telephone list code (must be set up in 
TETP)
TEL_NUM 20 the telephone number
TEL_CONTACT 30 the contact name
TEL_CONTACT_DES 20 the contact’s position
CUST_STAT 1 Y Set to A for Active
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Item Details
SYSTEM ADMINISTRATION GUIDE 4.2* 109
Quantity Breakdown Level 1 = 60
Quantity Breakdown Level 2 = 10 
Quantity Breakdown Level 3 = 1
CAUTION The value in the Quantity Breakdown Level 1 field must equal the product of the number of layers and the quantity per layer plus the odd layer quantity (if 
any). For example, if your Quantity Breakdown Level 1 is 60, your number of layers 
and quantity per layer must equal 5/12, 6/10 or some other combination of numbers 
whose product is 60.
FIELD LENGTH
MANDA
TORY NOTES
CUST_CODE 10 Y the customer code
ITEM_CODE 20 Y the item code
ITEM_DES1 40 Y item description
ITEM_DES2 60 your alternate description
GENR_INFO_PROF_CODE 4 Y must be set up in IINP
ITEM_BILL_PROF_CODE1 4 Y must be set up in IBIP
COMD_CODE 6 Y must be set up in COMM
COMD_SUB_CODE 2 Y "
WHSE_CODE 4 your warehouse restriction if any (must be set 
up in WARE)

CONVERSIONS
Converting Item Details
ITEM_VAR_QTY_BKD_FLAG 1 Y Y = Yes
N = No (default)
This field allows you to specify whether you 
wish to allow non-standard quantity breakdowns for the item. If you set this flag to No, 
the quantity breakdown that you define in the 
Quantity Breakdown Block of this program is 
standard and cannot be changed for any particular receipt. If you set this flag to Yes, you 
can change the item’s quantity breakdown on 
a receipt.
ITEM_WGT_TP_CODE 4 Y Y = Standard Weight
If you set this field to Standard Weight, the 
system will use the standard weight specified 
in the Quantity Breakdown Block of this program; you will not be able to modify this 
weight during receipt entry or order entry. If 
you wish to enter the weight manually on 
shipping or receiving or calculate the weight 
in a different manner, see “Non-Standard 
Weight Options” in the Setup Guide for further information.
ITEM_CODE_SUB 20 your substitute item if any
ITEM_VALUE NUM 13 the item’s value (may have up to four decimals)
PROS_PROF_CODE 4 Y the item’s process profile code (must be set 
up in IPRP)
SHIP_PROF_CODE 4 Y the item’s shipping profile code (must be set 
up in ITSH)
ITEM_LOC_PROF_CODE 4 the item’s item location profile code (must be 
set up in ILOP)
ALT_INVT_REP_TP_CODE 4 the item’s alternate inventory report type 
(must be set up in ITAS)
ALT_INVT_REP_CODE 20 the item’s alternate reporting type code (must 
be set up in ITAS)
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
SYSTEM ADMINISTRATION GUIDE 4.2* 111
ALT_INVT_REP_UPC_CODE 20 the item’s UPC code
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program to indicate records that have 
been processed versus those that may have 
failed and are still pending.
NUM_OPEN_DAY NUM 3 Y The number of days that an open lot item can 
remain open. If you do not use open lots, set 
this field to 0.
ITEM_BILL_PROF_CODE2 4 item billing profile code 2
ITEM_BILL_PROF_CODE3 4 item billing profile code 3
ALLOW_ENTRY_LEV_NUM NUM 1 The number of inventory levels needed for 
this item. You can enter any number between 
one and the maximum number of levels for 
the customer defined in DILP.
COUNTRY_CODE 4 the item’s country code (must be set up in 
CNTY)
TAX_CODE 4 the item’s tax code
PICK_PROF_CODE 4 the item’s picking profile code (must be set up 
in PIPR)
HAZ_CODE 4 the item’s hazard code (must be set up in 
HAZA)
ITEM_HOLD_PROF_CODE 4 the items’ hold profile code (must be set up in 
IHOP)
EXTRA_CHG_PROF_CODE 4 the items’ extra charge profile code (must be 
set up in ECHP)
ITEM_CRS_DOCK_FLAG 1 Y = Yes
N = No
the item’s cross dock flag
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
ITEM_KIT_FLAG 1 Y Y = Yes
N = No (default)
the item’s kit flag
ITEM_KIT_TP_FLAG 1 Y if 
ITEM_KIT_
FLAG = Y
P = Pending
W = Weight
the order line type for kit components
QTY_BKD_PROF_CODE 4 Y must be set up in IQBP
ITEM_QTY_BKD_BASE_NUM NUM 1 Y the quantity breakdown level at which you 
wish to track an item’s weight and size (for 
example, if your item’s quantity breakdown is 
pallet/case/each and you wish to track the 
item’s weight and size at the each level, you 
would enter 3 in this column)
VAR_QTY_BKD_QTY1 NUM 4 Y VAR_QTY_BKD_QTY1 is for your largest 
SKU type (for example, pallets), 
VAR_QTY_BKD_ QTY2 is for your next largest SKU type (for example, cases), etc. The 
number for the larger SKU type indicates how 
many of the smaller SKU types make up one 
unit of the larger SKU type.
For example, if your quantity breakdown were 
10 eaches per case and 60 cases per pallet, 
you would enter the following:
Quantity Breakdown Level 1 = 60
Quantity Breakdown Level 2 = 10
Quantity Breakdown Level 3 = 1
VAR_QTY_BKD_QTY2 NUM 4 Y
VAR_QTY_BKD_QTY3 NUM 4 Y
VAR_QTY_BKD_QTY4 NUM 4 Y
VAR_QTY_BKD_QTY5 NUM 4 Y
ITEM_QTY_BKD_QTY_PER_LAY NUM 3 Y the quantity per layer or tie (use 1 if layer configuration is set to No)
ITEM_QTY_BKD_NUM_LAY 3 Y the number of layers or hi (use 1 if layer configuration is set to No)
ITEM_QTY_BKD_QTY_ODD_LAY 3 the quantity, if any, of your odd layer
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
SYSTEM ADMINISTRATION GUIDE 4.2* 113
ITEM_QTY_BKD_WHOLE_FLAG 1 Y W = Whole (default)
P = Prorate
whether to round up partial quantities like 1.5 
pallets or whether to charge for the actual 
quantity stored
WGT_MEAS_CODE 4 Y the item’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
MT = Metric Tonne
LT = Long Tonne
LBS = Imperial Pounds
KG = Kilogram
GM = Grams
OZ = Ounces
TN = Imperial Tons
ITEM_QTY_BKD_WGT_GROSS NUM 15 Y the item’s gross weight (may have up to six 
decimals)
ITEM_QTY_BKD_WGT_NET NUM 15 Y the item’s net weight (may have up to six decimals)
LINEAR_MEAS_CODE 4 Y your linear measurement code (FT, CM, IN, 
M, etc.) 
ITEM_QTY_BKD_LEN NUM 8 the item’s length (may have up to three decimals)
ITEM_QTY_BKD_WID NUM 8 the item’s width (may have up to three decimals)
ITEM_QTY_BKD_HGT NUM 8 the item’s height (may have up to three decimals)
VOL_MEAS_CODE 4 your volume measurement code (CL, FLOZ, 
GAL, GALI, etc.)
ITEM_QTY_BKD_VOL NUM 15 the item’s volume (may have up to six decimals)
The following columns are all optional and apply to an item’s second SKU when this SKU is not defined as the base SKU for the 
item’s cube and weight. See the column description for the base SKU for further information. For example, for 
WGT_MEAS_CODE_2, see WGT_MEAS_CODE.
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
ITEM_QTY_BKD_QTY_PER_LAY_2 NUM 3
ITEM_QTY_BKD_QTY_NUM_LAY_2 3
ITEM_QTY_BKD_QTY_ODD_LAY_2 3
ITEM_QTY_BKD_WHOLE_FLAG_2 1
WGT_MEAS_CODE_2 4
ITEM_QTY_BKD_WGT_GROSS_2 NUM 15
ITEM_QTY_BKD_WGT_NET_2 NUM 15
LINEAR_MEAS_CODE_2 4
ITEM_QTY_BKD_LEN_2 NUM 8
ITEM_QTY_BKD_WID_2 NUM 8
ITEM_QTY_BKD_HGT_2 NUM 8
VOL_MEAS_CODE_2 4
ITEM_QTY_BKD_VOL_2 NUM 15
The following columns are all optional and apply to an item’s third SKU when this SKU is not defined as the base SKU for the item’s 
cube and weight. See the column description for the base SKU for further information. For example, for WGT_MEAS_CODE_3, see 
WGT_MEAS_CODE.
ITEM_QTY_BKD_QTY_PER_LAY_3 NUM 3
ITEM_QTY_BKD_QTY_NUM_LAY_3 3
ITEM_QTY_BKD_NUM_LAY_3 3
ITEM_QTY_BKD_QTY_ODD_LAY_3 3
ITEM_QTY_BKD_WHOLE_FLAG_3 1
WGT_MEAS_CODE_3 4
ITEM_QTY_BKD_WGT_GROSS_3 NUM 15
ITEM_QTY_BKD_WGT_NET_3 NUM 15
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
SYSTEM ADMINISTRATION GUIDE 4.2* 115
LINEAR_MEAS_CODE_3 4
ITEM_QTY_BKD_LEN_3 NUM 8
ITEM_QTY_BKD_WID_3 NUM 8
ITEM_QTY_BKD_HGT_3 NUM 8
VOL_MEAS_CODE_3 4
ITEM_QTY_BKD_VOL_3 NUM 15
The following columns are all optional and apply to an item’s fourth SKU when this SKU is not defined as the base SKU for the 
item’s cube and weight. See the column description for the base SKU for further information. For example, for 
WGT_MEAS_CODE_4, see WGT_MEAS_CODE.
ITEM_QTY_BKD_QTY_PER_LAY_4 NUM 3
ITEM_QTY_BKD_NUM_LAY_4 3
ITEM_QTY_BKD_QTY_ODD_LAY_4 3
 ITEM_QTY_BKD_WHOLE_FLAG_4 1
WGT_MEAS_CODE_4 4
ITEM_QTY_BKD_WGT_GROSS_4 NUM 15
ITEM_QTY_BKD_WGT_NET_4 NUM 15
LINEAR_MEAS_CODE_4 4
ITEM_QTY_BKD_LEN_4 NUM 8
ITEM_QTY_BKD_WID_4 NUM 8
ITEM_QTY_BKD_HGT_4 NUM 8
VOL_MEAS_CODE_4 4
ITEM_QTY_BKD_VOL_4 NUM 15
The following columns are all optional and apply to an item’s fifth SKU when this SKU is not defined as the base SKU for the item’s 
cube and weight. See the column description for the base SKU for further information. For example, for WGT_MEAS_CODE_5, see 
WGT_MEAS_CODE.
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
ITEM_QTY_BKD_QTY_PER_LAY_5 NUM 3
ITEM_QTY_BKD_NUM_LAY_5 3
ITEM_QTY_BKD_QTY_ODD_LAY_5 3
ITEM_QTY_BKD_WHOLE_FLAG_5 1
WGT_MEAS_CODE_5 4
ITEM_QTY_BKD_WGT_GROSS_5 NUM 15
ITEM_QTY_BKD_WGT_NET_5 NUM 15
LINEAR_MEAS_CODE_5 4
ITEM_QTY_BKD_LEN_5 NUM 8
ITEM_QTY_BKD_WID_5 NUM 8
ITEM_QTY_BKD_HGT_5 NUM 8
VOL_MEAS_CODE_5 4
ITEM_QTY_BKD_VOL_5 NUM 15
LANG_CODE 4 the item’s language code (only required if you 
use alternate items and descriptions in ALIT)
ACC_ITEM_DES1 40 an alternate description for the item (only 
required if you use alternate items and 
descriptions in ALIT)
ITEM_ALLOW_BAND_FLAG 1 Reserved for future use
ITEM_BAND_SKU_CLASS_NUM 1 Reserved for future use
ITEM_BAND_MAX_QTY 9 Reserved for future use
ITEM_ALLOW_MIX_PLT_FLAG 1 Reserved for future use
SCAN_PARAM_CODE 4 the item’s scan parameter code (must be set 
up in SCPR)
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Item Details
SYSTEM ADMINISTRATION GUIDE 4.2* 117

MOCO screen for pass name of ITEM
ITEM_CODE_MASTER_FLAG 1 Y N = No (default)
Y = Yes
Set to N for No.
FIELD LENGTH
MANDA
TORY NOTES

CONVERSIONS
Converting Location Details

MOCO screen for pass name of ITEM
Converting Location Details
In this conversion file, you set up your location details. The following codes and profiles must be set up before 
you can perform a location conversion:
 Company Code (CNTY)
 Warehouse Code (WARE)
 Location Billing Code (LODE)
 Location Type Code (LOTP)
 Isolator Type Code (ISOL)
 SKU Code (SKUS)
 the location’s location structure type code
A location details conversion inserts new records in the database. Existing location records are not touched.
FIELD LENGTH
MANDATORY NOTES
COMP_CODE 2 Y the company code (must be set up in COMP)
WHSE_CODE 4 Y the warehouse code (must be set up in 
WARE)

CONVERSIONS
Converting Location Details
SYSTEM ADMINISTRATION GUIDE 4.2* 119
LOC_CODE 12 Y the location code
LOC_DES 30 the location description
LOC_STAT 1 Y A = Active or D = Deactivated
LOC_BILL_CODE 4 Y the location’s location billing code (must be 
set up in LODE)
LINEAR_MEAS_CODE 4 Y the linear measurement code (FT, CM, IN, M, 
etc.)
LOC_HGT NUM 8 Y the location’s height (may have up to three 
decimals)
LOC_WID NUM 8 Y the location’s width (may have up to three 
decimals)
LOC_LEN NUM 8 Y the location’s length (may have up to three 
decimals)
LOC_CUBE NUM 11 the location’s cube (may have up to three 
decimals)
LOC_TP_CODE 4 Y the location’s location type (must be set up in 
LOTP)
ISOL_CODE 4 Y the location’s isolator code (must be set up in 
ISOL)
SKU_CODE 4 Y the location’s SKU code (must be set up in 
SKUS)
LOC_MAX_SKU_CAPC NUM 4 Y the maximum capacity for the location
SKU_CAPC_PCENT NUM 6 Reserved for future use
SPACE_CAPC_PCENT NUM 6 Reserved for future use
LOC_PRT_PROF_CODE 4 the location’s location print profile code (must 
be set up in LPPR)
CYC_CNT_PROF_CODE 4 the location’s cycle count profile code (must 
be set up in CYCP)
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Converting Location Details
HOLD_CODE 4 the location’s hold code (must be set up in 
HOLD)
LOC_SIZE_CODE 4 the location’s location size code (must be set 
up in LOCS)
LOC_LAB_STD_MODY
_NUM
NUM 5 the location’s labor standard modifier (may 
have up to two decimals)
WGT_MEAS_CODE 4 Y the location’s weight measurement code 
(LBS, KILO, GRAM, TON, etc.)
LOC_WGT NUM 15 Y the location’s weight limit or 0 if there is no 
weight limit (may have up to six decimals)
LOC_CODE_WGT_
MAST
12 the location’s master location for weight
LOC_STRUCT_TP_
CODE 
4 Y the location’s location structure type:
MHE = MHE Code
STIC = Static/Stationary Locations (default)
LOC_SHIP_UNIT_ID 20 Reserved for future use
PICK_SEQ_NUM 9 See the RF User Guide for further information 
on configuring the sort sequence for picking 
tasks in RFPIC.
LOC_VOICE_CHK_DIGIT1 5 the first location check digit for voice picking
LOC_VOICE_CHK_DIGIT2 5 the second location check digit for voice picking
LOC_VOICE_CHK_DIGIT3 5 the third location check digit for voice picking
LOC_VERT_HGT_FACT_CODE 4 the vertical height of the location
LOC_AISLE_REF 4 used to identify aisles when the aisle cannot 
be extracted from the location code in the 
Location Attributes Block of WARE
LOC_FACING_REF 4 an additional field that can be used for sorting 
purposes
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Converting Location Details
SYSTEM ADMINISTRATION GUIDE 4.2* 121

MOCO screen for pass name of LOC
LOC_FRONT_ALIAS 12 the front location alias
LOC_FRONT_ALIAS_CHK_DIGIT 5 the check digit for the front location alias
LOC_BACK_ALIAS 12 the back location alias
LOC_BACK_ALIAS_CHK_DIGIT 5 the check digit for the back location alias
PUT_SEQ_NUM 9 the put-away/directed move sort sequence 
number
LOC_USE_LAST_PUT_FLAG 1 Y Y =Yes
N = No (default)
whether or not you can put-away product into 
this location using the options in the Last 
Location Used group in ILOP
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Converting Existing Locations
Converting Existing Locations
An existing locations conversion is similar to a location details conversion. However, unlike a location details 
conversion, an existing locations conversion deletes all existing location records in the database before 
performing an insert based on your new csv file.
The only restriction to an existing locations conversion is location bill code: if you delete and recreate a 
location record, the original location bill code attached to that location will be retained. Your new location bill 
code attached to the location will be ignored.
Converting Consignee Details
In this conversion, you convert your consignees. The following codes and profiles must be set up before you 
can perform a consignee conversion:
 the consignee’s ZIP code (ZIPO)
 the consignee’s load analysis code (LDAN)
 the customer code for the consignee (CUST)
FIELD LENGTH
MANDATORY NOTES
LOC_STAT 1 Y U = Update or D = Deactivated
FIELD LENGTH MANDATORY NOTES
CON_CODE 10 Y the consignee code
CON_NAME 30 Y the consignee name
CON_STAT 1 Y Set to A for Active
CON_ADD1 30 Y Address line 1
CON_ADD2 30 Address line 2
CON_ADD3 30 Address line 3
ZIP_CODE 10 Y the consignee’s ZIP code or postal code 
(must be set up in ZIPO)
MES_CODE 4 the consignee’s bill of lading message code 
(must be set up in MESS)

CONVERSIONS
Converting Consignee Details
SYSTEM ADMINISTRATION GUIDE 4.2* 123
CON_LAST_ACT_DATE 6 Reserved for future use
LOAD_ANAL_CODE 4 Y the consignee’s load analysis code (must be 
set up in LDAN)
CON_FRT_APPO_FLAG 1 Y Set to N for No
CON_FRT_DISC_PCENT NUM 10 Y Set to zero
FRT_DEST_CODE 10 Y the consignee’s ZIP code or postal code 
(must be set up in ZIPO)
CUST_CODE 10 the consignee’s customer code (must be set 
up in CUST) or .ALL for all customers
PICK_PROF_CODE 4 the consignee’s pick profile code (must be set 
up in PIPR)
INFO_FLOW_PROF_
CODE
4 the consignee’s workflow profile code (must 
be set up in DIFP)
TEL_LIST_CODE 4 the consignee’s telephone list code (must be 
set up in TETP)
TEL_NUM 20 the telephone number for the telephone list 
code (must be set up in TELE)
TEL_CONTACT 30 Y* the contact name
* Only mandatory if you enter a telephone 
number.
TEL_CONTACT_DES 20 the contact’s position
CON_BORD_FLAG 1 Y A = Always
N = Never (default)
whether or not back orders are activated for 
this consignee
EXT_REF_NUM1 20 miscellaneous reference information about a 
consignee
EXT_REF_NUM2 20 miscellaneous reference information about a 
consignee
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Consignee Details
EXT_REF_NUM3 20 miscellaneous reference information about a 
consignee
EXT_REF_NUM4 20 miscellaneous reference information about a 
consignee
CON_ALLOW_BANDING_FLAG 1 Reserved for future use
CON_BANDING_SKU_CLASS_NU
M
1 Reserved for future use
CON_CONSL_TP 1 Reserved for future use
PALL_CODE Reserved for future use
CON_SPS_REQ_FLAG 1 whether or not the consignee is marked as 
having a special requirement
CON_ASN_REP_TP 1 Reserved for future use
CON_MSDS_REQ_FLAG 1 Reserved for future use
LANG_CODE 4 if you have an alternate item and description 
set up in ALIT (Alternate Item and Language) 
for an item, an alternate item and description 
will be captured when that item is being 
shipped to this consignee
SKU_CLASS_NUM 4 the SKU class that AccellosOne 3PL uses to 
calculate the number of labels to print in BarTender or ShippingLive
SKU_CLASS_NUM_RND_FLAG 1 U = Up
D = Down
the rounding method that you want AccellosOne 3PL to use for partial quantities when 
deciding how many labels to generate
CON_UCC128_LABEL_REQ_FLAG 1 Reserved for future use
CON_COMPL_ORD_FLAG 1 Y N = No (default)
Y = Yes
whether or not allocation of fully filled orders 
only is activated
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Shipper Details
SYSTEM ADMINISTRATION GUIDE 4.2* 125

MOCO screen for pass name of CON
Converting Shipper Details
In this conversion, you convert your shippers. The following codes and profiles must be set up before you can 
perform a shipper conversion:
 the shipper’s ZIP code (ZIPO)
 the shipper’s load analysis code (LDAN)
 the country code (CNTY)
FIELD LENGTH MANDATORY NOTES
SHIP_CODE 10 Y the shipper code
SHIP_NAME 30 Y the shipper name
SHIP_STAT 1 Y Set to A for Active
SHIP_ADD1 30 Y address line 1
SHIP_ADD2 30 address line 2

CONVERSIONS
Converting Shipper Details
SHIP_ADD3 30 address line 3
ZIP_CODE 10 Y the shipper’s ZIP code or postal code (must 
be set up in ZIPO)
WGT_MEAS_CODE 4 Y the shipper’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
SHIP_LAST_ACT_DATE 6 Reserved for future use
LOAD_ANAL_CODE 4 Y the shipper’s load analysis code (must be set 
up in LDAN)
FRT_DEST_CODE 10 Reserved for future use
INFO_FLOW_PROF_CODE 4 the shipper’s workflow profile code (must be 
set up in DIFP)
SHIP_LAB_STD_MODY_NUM 7 the shipper’s labor standard modifier (may 
have up to two decimals)
EXTRA_CHG_PROF_CODE 4 Reserved for future use
SHIP_ADD4 30 address line 4
COUNTRY_CODE 4 Y the shipper’s country code (must be set up in 
CNTY)
EXT_REF_NUM1 4 miscellaneous information about a shipper
EDI_PROF_CODE 4 the shipper’s EDI profile code (must be set up 
in DEDP); this profile overrides the default 
EDI profile attached to CUST - Customer 
Setup
SHIP_ESTAB_NUM 20 the shipper’s establishment number
SHIP_TP_CODE 1 Y O = Other
R = Repair
S = Store
V = Vendor
W = Warehouse
Unless otherwise instructed by your 
HighJump consultant, set to W for Warehouse.
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Carrier Details
SYSTEM ADMINISTRATION GUIDE 4.2* 127

MOCO screen for pass name of SHIP
Converting Carrier Details
In this conversion, you convert your carriers. The following codes and profiles must be set up before you can 
perform a carrier conversion:
 the carrier’s ZIP code
 the carrier’s country code
FIELD LENGTH MANDATORY NOTES
CARR_CODE 10 Y the carrier code
CARR_NAME 30 Y the carrier name
CARR_STAT 1 Y Set to A for Active
CARR_ADD1 30 Y address line 1
CARR_ADD2 30 address line 2
CARR_ADD3 30 address line 3

CONVERSIONS
Converting Carrier Details
ZIP_CODE 10 Y the carrier’s ZIP code or postal code (must be 
set up in ZIPO)
CARR_WGT_MEAS_FLAG 1 Y the carrier’s weight measure (I for Imperial or M 
for Metric)
MES_CODE 4 the message that will print on the carrier’s bill 
of lading (must be set up in MESS)
CARR_CODE_PAY 10 Y set to the carrier code in the CARR_CODE column
FRT_TP_CODE 4 Y set to .ALL
CARR_LAST_ACT_DATE 6 Reserved for future use
CARR_STD_ALPHA_CODE 4 Y the carrier’s predefined SCAC code or “X” if the 
carrier does not have such a code
CARR_TP_CODE 3 Y the freight interface type code (FRT for freight 
interface or NFR for no freight interface)
EXTRA_CHG_PROF_CODE 4 Reserved for future use
CARR_LAB_STD_MODY_NUM 7 the carrier’s labor standard modifier (may have 
up to two decimals)
CARR_ADD4 30 address line 4
COUNTRY_CODE 4 Y the carrier’s country code (must be set up in 
CNTY)
EDI_PROF_CODE 4 the carrier’s EDI profile code (must be set up in 
DEDP); this profile overrides the default EDI 
profile attached to CUST - Customer Setup
TRSPT_MODE_CODE 4 the carrier’s transport mode code (must be set 
up in TRMO)
CARR_EXT_FRT_FLAG 1 whether or not the carrier’s orders will be available in A1 Transport
GEN_NUM_PROF_CODE 4 Reserved for future use
ISOL_CODE 4 Reserved for future use
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Transaction History Details
SYSTEM ADMINISTRATION GUIDE 4.2* 129
MOCO screen for pass name of CARR
Converting Transaction History Details
In this conversion, you convert your transaction history records. The following codes and profiles must be set 
up before you can perform a transaction history conversion:
 Customer Code (CUST)
 Item Code (ITEM)
 Warehouse Code (WARE)
 Location Code (LOCA)
CARR_ALLOW_BANDING_FLAG 1 Reserved for future use
CARR_COMPL_LABEL_FLAG 1 Reserved for future use
CARR_REQ_EDI_FLAG 1 Reserved for future use
TRSPT_UNIT_VAL_HIST_FLAG 1 Reserved for future use
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Transaction History Details
 Adjustment Code (ADJU)
These transactions will be created as IF (Information Only) transaction types. They will have no impact on 
inventory balances.
NOTE You cannot look up transaction history details in MOCO.
FIELD LENGTH MANDATORY NOTES
CUST_CODE VARCHAR2(10) Y the customer code for the transaction
INVT_LEV1 VARCHAR2(40) Y the product’s item code
INVT_LEV2 VARCHAR2(40) Y the item’s level 2 value
INVT_LEV3 VARCHAR2(40) Y the item’s level 3 value
INVT_LEV4 VARCHAR2(40) Y the item’s level 4 value
INVT_LEV5 VARCHAR2(40) Reserved for future use
HOLD_CODE VARCHAR2(4) Y Use an asterisk (“*”) if there is no hold on the 
product.
WHSE_CODE VARCHAR2(4) Y the product’s warehouse code
LOC_CODE VARCHAR2(12) Y the product’s location code
MVT_EFF_TRANS_DATE DATE Y the date that the transaction took place
MVT_UNIT NUM 9 Y the number of units involved in the transaction 
MVT_CNVC_QTY NUM 6 the number of conveyances involved in the 
transaction
WGT_MEAS_CODE VARCHAR2(4) Y the product’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
TRANS_WGT NUM 17 Y the product’s gross weight (up to six decimal 
places)
TRANS_WGT_NET NUM 17 Y the product’s net weight (up to six decimal 
places)

CONVERSIONS
Converting Transaction History Details
SYSTEM ADMINISTRATION GUIDE 4.2* 131
LINEAR_MEAS_CODE VARCHAR2(4) Y the product’s linear measurement code (FT, 
CM, IN, M, etc.) 
TRANS_CUBE NUM 17 Y the product’s total cube (up to six decimal 
places)
DOC_NUM NUM 9 Y the order, receipt or adjustment number
DOC_LINE_NUM NUMBER(4) Y the line number
DOC_LOC_LINE_NUM NUMBER(4) Y the location line number
OP_CODE NUMBER(20) Y the operator who entered the transaction 
(must be set up in OPER)
MVT_REF1 VARCHAR2(10) Y the consignee (for orders), the shipper (for 
receipts) or the adjustment code (for adjustments)
CARR_CODE VARCHAR2(10) the transaction’s carrier (orders or receipts 
only)
LOAD_TP_CODE VARCHAR2(4) the transaction’s load type (orders or receipts 
only)
DOC_REF1 VARCHAR2(20) the customer order number (for orders) or the 
reference number (for receipts)
DOC_REF2 VARCHAR2(20) the PO number (for orders) or the probill 
number (for receipts)
DOC_REF3 VARCHAR2(20) Extra Reference Number 1 (orders and 
receipts only)
DOC_REF4 VARCHAR2(20) Extra Reference Number 2 (orders and 
receipts only)
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting Revenue Master Details
Converting Revenue Master Details
In this conversion file, you convert your sales revenue. The conversion program loads your revenue by 
revenue analysis code into AccellosOne 3PL. Once loaded you can run any AccellosOne 3PL sales report 
and look up the revenue that you converted. For example, suppose you had $1,500 in freight revenue in 
January 1999 and you performed a revenue master conversion. When you ran SALE (Sales Report), you 
would see the amount of 1,500 in the January 1999 column of the report for freight revenue. The columns in 
this table are separated by tildes. 
The following codes and profiles must be set up before you can perform a revenue master conversion: 
 Customer Code (COMP)
 Revenue Analysis Code (REVA)
MVT_TRANS_TP VARCHAR2(2) Y A = Adjustment
BF = Bring Forward
CO = Confirmed Order
CR = Confirmed Receipt
EO = Entered Order
ER = Entered Receipt
HL = Hold Adjustment
IF = Information Only
OM = Order Move
PD = Proof of Delivery
RL = Relocation
CONV_UPD_FLAG VARCHAR2(1) Leave this field blank. It is used by the conversion program to indicate records that have 
been processed versus those that may have 
failed and are still pending.
FIELD LENGTH MANDATORY NOTES
CUST_CODE VARCHAR2(10) Y the customer code for the revenue (must be 
set up in CUST)
REVN_ANAL_CODE VARCHAR2(4) Y the revenue analysis code for the revenue 
(must be set up in REVA)
REVN_DATE DATE Y The date that the revenue was earned. Must 
be in YYMMDD format.
REVN_AMT VARCHAR2(10) Y the revenue amount
FIELD LENGTH MANDATORY NOTES

CONVERSIONS
Converting ZIP Codes
SYSTEM ADMINISTRATION GUIDE 4.2* 133

MOCO screen for pass name of REVN
Converting ZIP Codes
In this conversion, you convert your ZIP codes for countries other than the US and Canada. The following 
codes and profiles must be set up before you can perform a ZIP code conversion: 
 Country Code (CNTRY)
 State/Province Code (STPR)

CONVERSIONS
Converting Inventory Balances

MOCO screen for pass name of ZIP
Converting Inventory Balances
In this conversion, you convert your inventory balances. Inventory balances consist of the item code, 
inventory levels, the weight, on-hand quantity, renewal dates, the original receipt date and the warehouse 
code/location code. Inventory balances are posted as an adjustment in AccellosOne 3PL and the adjustment 
date is the date that you processed the conversion in PRCO.
When converting item balances, you must define all items down to the lowest inventory level. For example, if 
you identify product by item, by lot number and by pallet ID, you must specify an item code, lot number and 
pallet ID number for each record that you wish to convert. 
The following codes and profiles must be set up before you can perform an inventory balance conversion:
 Warehouse Code (WARE)
 Location Code (LOCA)
NOTE You cannot process multiple records containing the same inventory entity 
and location; for example, you cannot have in balcsv.dat two records for item A, lot 1, 
expiry date = June 1 in which the warehouse code and location are the same. You 
must sum up the inventory balances for the two records and create a single record for 
that item/level 2/level 3 combination and that location.

CONVERSIONS
Converting Inventory Balances
SYSTEM ADMINISTRATION GUIDE 4.2* 135
CONVERTING BILLING INFORMATION
If you are converting billing information, the following pieces of information may be required:
 the item’s next renewal date 
 the item’s last renewal date (for historical data only)
 the item’s original qualifying quantity
 the item’s original qualifying weight
 the number of renewal days (only required if the renewal dates on your old system do not match your 
AccellosOne 3PL renewal dates)
 the item’s location billing profile code (for historical data only)
FIELD LENGTH
MANDATORY NOTES
CUST_CODE 10 Y your customer code (must be set up in CUST)
INVT_LEV1 20 Y your item code (must be set up in ITEM)
INVT_LEV2 40 Y your level 2 value
CONV_UNIT NUM 10 Y The item’s on-hand quantity in the lowest SKU code 
(for example, if your quantity breakdown is pallets/
cases and you enter 10 in this field, your inventory balance will be recorded as 10 cases). Decimal values 
are not accepted.
CONV_WGT NUM 17 Y The item’s on-hand gross weight in the weight measure code defined for the item in ITEM (may have up 
to six decimals).
If you do not know the item’s exact gross weight, enter 
zero (0) as your weight. AccellosOne 3PL will calculate the weight based on your setup in ITEM. That is, 
gross weight X CONV_UNIT or on-hand quantity in 
lowest SKU.
RENW_QTY NUM 10 Reserved for future use 
RENW_WGT NUM 17 Reserved for future use
DATE_NXT 6 Y The item’s next renewal date in YYMMDD format (if 
you do not use AccellosOne 3PL for billing, enter 
700101). This date cannot be earlier than the conversion processing date in PRCO.
DATE_LAST 6 The item’s last renewal date in YYMMDD format (used 
for historical data only). This date cannot be later than 
the conversion processing date in PRCO.

CONVERSIONS
Converting Inventory Balances
INVT_ORG_RECD_DATE 6 Y The item’s original receipt date in YYMMDD format. 
This date cannot be later than the conversion processing date in PRCO.
INVT_EXPY_DATE 6 The item’s expiry date in YYMMDD format. This date 
cannot be earlier than the conversion processing date 
in PRCO.
INVT_LEV3 40 the item’s level 3 value
INVT_LEV4 40 the item’s level 4 value
INVT_LEV5 40 Reserved for future use
WHSE_CODE 4 Y the item’s warehouse code (must be set up in WARE)
LOC_CODE 12 Y the item’s location (must be set up in LOCA)
HOLD_CODE 4 the item’s hold code (must be set up in HOLD)
INVT_LEV2_DES 40 level 2 description
ORG_RCPT_NUM 9 the original receipt number
INVT_LEV3_DES 40 the item’s level 3 description
INVT_LEV4_DES 40 the item’s level 4 description
INVT_LEV5_DES 40 reserved for future use
INVT_CLS_DATE 6 the lot closing date for open lots in YYMMDD format
INVT_CLS_FLAG 1 If the lot is open, set this field to N for No. If the lot is 
closed or if the item cannot be processed as an open 
lot, leave this field blank.
NUM_CASE_STOR_CALC 6 The item’s original qualifying quantity for renewal storage charges — that is, the number of units that the 
system uses to look up the per rate. If you do not enter 
a quantity in this field, the system will use the on-hand 
quantity.
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Converting Inventory Balances
SYSTEM ADMINISTRATION GUIDE 4.2* 137
CONV_WGT_NET 17 Y the item’s on-hand net weight in the weight measure 
code defined for the item in ITEM (may have up to six 
decimals)
If you do not know the item’s exact net weight, enter 
zero (0) as your weight. AccellosOne 3PL will calculate the weight based on your setup in ITEM. That is, 
net weight X CONV_UNIT or on-hand quantity in lowest SKU.
VAR_QTY_BKD_FACT 30 If the item is a variable quantity breakdown item, you 
enter its quantity breakdown factor in this field. The 
factor is always expressed in terms of the lowest SKU 
type; for example, if your quantity breakdown is 60 
cases per pallet and 12 eaches per case, you would 
enter the following:
000720000012000001
Each breakdown is six characters in length and must 
be padded out with leading zeroes.
NOTE Entering a value in this field will overwrite 
the default setup in ITEM and is only required if the 
item is a variable quantity breakdown.
RENW_ORG_RATE NUM 10 If you set the Original or Current Rate on Renewals 
flag in DBIP to R for Renewal Original, you must enter 
your original renewal rate in this field. You can enter 
up to four decimal places.
ORG_CHG_CODE 4 Reserved for future use.
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program.
NUM_RENW_DAY 1 Y If the renewal date on the system that you are converting from differs from the renewal date in AccellosOne 
3PL, you must adjust the date in this field. For example, if your system uses June 30 for product that actually renews on July 1, you would enter 1 in this field 
(June 30 + 1 day). 
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Converting Inventory Balances

MOCO screen for pass name of BAL
WGT_STOR_CALC 17 The item’s original qualifying weight for renewal storage charges — that is, the weight that the system 
uses to look up the per rate. If you do not enter a 
weight in this field, the system will use the on-hand 
weight. You can enter up to six decimal places.
ITEM_BILL_PROF_CODE 4 The item billing profile code for this item (used for historical data only). If you do not enter a code in this 
field, the system will use the item billing profile code 
attached to ITEM.
CNVC_QTY NUM 6 Reserved for future use
HOLD_SHIP_FLAG 1 Y N = No (default)
Y = Yes
If the product is on hold, whether or not the hold is 
shippable.
FIELD LENGTH
MANDATORY NOTES

CONVERSIONS
Miscellaneous Conversions
SYSTEM ADMINISTRATION GUIDE 4.2* 139
Miscellaneous Conversions
The following data can be converted using the AccellosOne 3PL conversion programs:
 alternate items (ALIT)
 alternate reporting types (ALTP)
 last expiry date (CCID)
 depositor level verification profiles (DLVP)
 fax/e-mail setup
 item kits 
 hazard details
 inventory attributes (IAPR)
 process values (IPRO, IPRP)
 pick line locations (PIIT)
Contact HighJump customer support for the appropriate csv file.
Performing the Conversion
After you have created your csv files, you are ready to perform the conversion.
STEP 1 — LOADING THE CONVERSION IN LOCO
In this step, you load the appropriate .dat file into a temporary AccellosOne 3PL table. You can only run 
LOCO once for any given record; if the record that you are loading is already in the conversion table, you will 
not be able to update it by rerunning LOCO.
LOCO loads the records in a staging table. It does not flag or delete the records in the .dat file. As such, if you 
rerun LOCO on the same dat file, it will create bad data in the table. LOCO creates records in the table first 
and at the end it updates the records with the company code from the company in which LOCO was run. As 
such, if the same record already exists, it will fail as a unique index error.
There are three error conditions that can occur when running LOCO:
 LOCO encounters a duplicate record and stops running
 LOCO encounters a field that exceeds its prescribed length and stops running
 the number of columns in the csv file does not match the number of columns in the control file
If you know Unix and the vi editor, you can easily identify the issue and fix the problem. The error file 
PASScsv.dat.log can be found in the del4/work/faxlp directory where PASS is the LOCO PASS name; for 
example, bal, item, loc, con, etc. 
Open the appropriate log file in the vi editor to find out what the issue is. Then exit the log file and go to del4/
loader/data and open the appropriate pass.dat file. Go to the specific record causing the problem and fix it. 
Next delete all records before the problem record as these records have already been loaded and cannot be 
reloaded. Lastly, save file and then rerun LOCO.
1 Make sure that you are in the correct company.
2 Enter LOCO.

CONVERSIONS
Performing the Conversion
3 Select the pass name corresponding to the type of data that you wish to convert and press Enter.
4 Press Enter to display the Begin Loading button.
5 Click on Begin Loading to load the flat file.

Load Conversion (LOCO) screen
6 When you finish loading your records, click on Exit to exit.
STEP 2 — VIEWING AND MODIFYING THE CONVERSION DATA IN MOCO
In this step, you view the information that was loaded in the previous step. If required, you can modify the 
information to correct any errors that occurred during the loading process as well as any values that you have 
identified as incorrect.
1 Enter MOCO.
2 Key in the pass name of the loaded data from step 1 and press Enter. 
3 Click on Execute Query.
NOTE If the loader encounters any errors in LOCO, the program will abort. Investigate the problem and then attempt to rerun LOCO.

CONVERSIONS
Performing the Conversion
SYSTEM ADMINISTRATION GUIDE 4.2* 141

Modify Conversion screen for pass name of LOC
Depending on the pass name that you entered, the appropriate MOCO screen will appear. MOCO is a 
query screen that allows you to view and modify the data loaded in the AccellosOne 3PL tables. You may 
use this screen to view all data or you can perform a query on specific criteria. The total number of 
records for the query can be seen in the top right hand corner.
4 Check the data in MOCO. If any data is incorrect, you can correct it by overtyping. Then press Enter or 
F12 to commit your changes. Alternatively, you can delete the record in MOCO and manually create the 
record in the appropriate AccellosOne 3PL program such as ITEM, CONS, CUST or SHIP.
You cannot create new records in MOCO.
STEP 3 — PROCESSING THE CONVERSION IN PRCO
Once you have checked the data in MOCO and made any necessary modifications, you are ready to perform 
the conversion in PRCO. This program loads the information into the AccellosOne 3PL tables so that it is 
available in the standard menu programs. For example, if you have loaded an item file, the items will be 
CAUTION Code fields in AccellosOne 3PL do not support the single quote (’) and 
double quote (“) special characters. Special characters such as “&”, “%” and “_” may 
cause problems in certain programs and are not recommended. Other special characters are generally supported. A code field is a field like customer code, consignee 
code, shipper code, item code, location code, item billing profile code, quantity breakdown code, etc. that is created in a AccellosOne 3PL maintain program like CUST, 
ITEM, LOCA, SHIP, DBIP, etc.

CONVERSIONS
Performing the Conversion
available in ITEM after PRCO has been run. No AccellosOne 3PL tables are updated or changed until PRCO 
is run. 
In addition to the pass name, this program requires a run date. This date will be the conversion date for the 
data in the specified pass file. For example, if inventory balances are being converted, the run date in PRCO 
will be the date that the inventory is available in AccellosOne 3PL.
1 Enter PRCO.

Process Conversion (PRCO)
2 Select your pass name from the dropdown list and press Enter.
3 If required, make any necessary changes to your run date and press Enter.
4 Click on Process.
STEP 4 — MODIFYING CONVERSION DATA IN MOCO
In this step, you return to MOCO and query all records. If any records remain in MOCO, this means that some 
records were not converted due to incorrect values or because they already existed in AccellosOne 3PL. Go 
to Step 5 and run COER (Conversion Exception Report) to find out which records were not converted. If no 
records remain in MOCO after performing Step 3, then the conversion was successful and you can skip Step 
5 and go directly to Step 6.
CAUTION If you are converting billing data, it is essential that the run date in 
PRCO matches the extraction date — that is, the date that you loaded the conversion 
in LOCO from your flat files. If the run date in PRCO does not match the extraction 
date, renewal storage charges may not be calculated correctly.
If you are doing an inventory balance conversion, make sure that your run date is 
consistent with your DATE_NXT, DATE_LAST and INVT_ORG_RECD_DATE values 
in balcsv.dat.

CONVERSIONS
Performing the Conversion
SYSTEM ADMINISTRATION GUIDE 4.2* 143
STEP 5 — RUNNING COER (CONVERSION EXCEPTION REPORT)
In this step, you run COER to look up records that were not converted in step 3. COER will generate a report 
describing the problem with each record remaining in MOCO. You should modify the records in MOCO to 
rectify the problem and then rerun PRCO and COER to ensure that all problems have been rectified. Repeat 
the process until no records remain in MOCO or COER.
1 Enter COER.
2 Key in your pass name and press Enter.

Conversion Exception Report (COER)
3 Key in your printer code and press Enter.
4 Click Ok to print.
Conversion Exception Report (COER) screen for pass name of BAL
5 Click on Exit to exit COER.
ABC Warehousing, Inc. Page 1 of 1
Conversion Exception Reporting (COER) Pass Name : BAL 03.24.08 12:27
------------------------------------------------------------------------------------------------------------------------------------
 Customer Level 1 Level 2 Level 3 Level 4 Whse Location Message
 ---------- -------------------- --------------- ---------- ---------- ---- ------------ ----------------------------------------
 BPLUBE 06450 06450 367794 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12092 12092 367797 1 155001 Location (whse=1 loc=155001) does not ex
 BPSCAN M077-021-00 M077-021-00 000148423 1 S1022 Location (whse=1 loc=S1022) does not exi
 BPLUBE 06062 06062 367790 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 06067 06067 367788 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12473 12473 100007783 1 4014 Location (whse=1 loc=4014) does not exis
 BPLUBE 03113 03113 000044832 1 4014 Location (whse=1 loc=4014) does not exis
 BPLUBE 06067 06067 367787 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12082 12082 367786 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12473 12473 100007788 1 4014 Location (whse=1 loc=4014) does not exis
 BPLUBE 06460 06460 367791 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12092 12092 367798 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 06450 06450 367793 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12112 12112 367795 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12112 12112 367796 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 06460 06460 367792 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12082 12082 367785 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 12092 12092 367799 1 155001 Location (whse=1 loc=155001) does not ex
 BPLUBE 06062 06062 367789 1 155001 Location (whse=1 loc=155001) does not ex

CONVERSIONS
Transferring Data from One Company to Another
STEP 6 — VERIFYING THE CONVERTED DATA
Once data has been converted and no records remain in MOCO or on the COER report, the data that has 
been converted may need to be verified in the AccellosOne 3PL programs. 
You can do this in one to two ways: you can run the applicable reports in AccellosOne 3PL and comparing 
these reports to reports from the converted system or you can perform a spot check in the applicable look-up 
programs. 
Refer to the table below for the appropriate look-up programs and reports:
Transferring Data from One Company to Another
You can transfer item details and inventory balances from one AccellosOne 3PL company to another in the 
program DEPC (Data Extraction Process for Conversion). DEPC is ideal for moving company-specific data 
from one company to another for testing or other purposes.
The following restrictions apply to an item master extraction in DEPC:
 the item must have a status of Active in ITEM
 mandatory profiles like the location code, warehouse code, item billing profile code, quantity breakdown 
profile code, etc. must be set up manually in the target system or moved there through COCO (Copy 
Codes Between Companies) before you can run DEPC
The following restrictions apply to an inventory balance extraction in DEPC:
 no inventory history is extracted
 the inventory must have an on-hand quantity greater than zero
 the inventory must be confirmed (inventory on open orders and receipts is not extracted)
 mandatory profiles like the location code, warehouse code, item billing profile code, quantity breakdown 
profile code, etc. must be set up manually in the target system or moved there through COCO (Copy 
Codes Between Companies) before you can run DEPC
csv File Look-Up Program Report
itemcsv.dat ITEM ITLI
loccsv.dat LOCA EMLO
concsv.dat CONS CONL
shipcsv.dat SHIP SHIL
custcsv.dat CUST CUPR
carrcsv.dat CARR CARL
zipcsv.dat ZIPO
balcsv.dat LOEN INHR, LOCT

CONVERSIONS
Transferring Data from One Company to Another
SYSTEM ADMINISTRATION GUIDE 4.2* 145
DEPC is restricted to the company that you currently working in. If you run DEPC in company W1, only 
company W1 data will be extracted. If you wish to extract W2 data as well, you must switch to company W2 
and then rerun DEPC for the second company.
1 Make sure that all required codes and profiles are set up in your target AccellosOne 3PL system. 
2 Enter the from company; that is, the company whose data you wish to extract.
3 Enter DEPC.
4 Key in ITEM or BAL and press Enter.
5 If required, key in a customer code restriction and press Enter. If you do not need a customer code 
restriction, press Enter to bypass this field.
FIELD DESCRIPTIONS
Extract ITEM / BAL ITEM
BAL
The type of data being extracted.
From Customer Optional
If you enter a customer code restriction in this field, only item details and 
inventory balances for that customer will be extracted.
<C>sv Flat File or Conversion <T>ableC = csv
T = table
The destination for the extracted data. If you select C for csv, the data will be 
extracted into a csv file and you must run LOCO to load the extracted data. If 
you select T for Table, the data will loaded directly into a table and will be 
immediately available in MOCO without the need to run LOCO.
Transfer to Company Only required for a conversion table extraction
Your to company.

CONVERSIONS
Transferring Data from One Company to Another
6 Do one of the following:

DEPC (Data Extraction Process for Conversion)
7 Click on Process.
8 If you are extracting both item and inventory balance information, repeat steps 2 to 7 for either ITEM or 
BAL.
9 Proceed to “Performing the Conversion” on page 139.
If you wish to extract the data 
to a flat file:
If you wish to extract the data 
to a database table:
a) Key in C for csv and press 
Enter.
a) Key in T for Table and press 
Enter.
b) Key in your to company code 
and press Enter. Your to company is the company where 
you want to copy the extracted 
data to.

SYSTEM ADMINISTRATION GUIDE 4.2* 147
MISCELLANEOUS PROGRAMS
Clearing Terminal Locks in CLTL .................................................................. 148
Copying Item Codes in COIT.......................................................................... 149
Adjusting an Item’s Quantity Breakdown in AEQB...................................... 150
Adjusting Location Billing Codes in ADLB................................................... 157
Adjusting Location Types in ADLT ............................................................... 159
Changing the Company Date in DATE or ALDA........................................... 160
Recalculating Inventory Expiry Dates in REEX............................................ 161
Performing Advanced Queries with SQL Statements.................................. 163
Performing Queries on Multiple Fields ......................................................... 165
Looking Up Spooler Activity in LOSP ........................................................... 167
Setting Up Sort Sequence Codes in SOSE................................................... 169
Looking Up Your Warehouse Utilization in LOWU....................................... 170
Looking Up Your Warehouse Activity in SAM.............................................. 173
Working With the Translation Manager in TRMA......................................... 181
Copying Codes Between Companies in COCO............................................ 187
Performing a Mass Update of an Item Value in IMAS .................................. 189
Importing Orders and Receipts in IFFI.......................................................... 190

MISCELLANEOUS PROGRAMS
Clearing Terminal Locks in CLTL
Clearing Terminal Locks in CLTL
AccellosOne 3PL uses a system of table locks to ensure that only one user at a time is altering a given table. 
For example, if user 1 is entering an order, then user 2 cannot allocate the same order. Sometimes a system 
failure will occur when a user is modifying an order and as a result the lock will remain in place instead of 
being automatically removed. When this happens, AccellosOne 3PL will automatically clear the lock when the 
Oracle session expires and a login event occurs (that is, a user logs in to or logs off from AccellosOne 3PL).
Should you wish to clear the lock manually before the Oracle session expires, you must do so in CLTL. 
CLTL shows the active sessions for all operators currently signed on including any locked sessions. For each 
session, CLTL shows the terminal ID, the operator code, the company code and the program in which the 
operator is currently working. If the program field is blank, the operator is currently in the main menu and not 
using any program.
When you clear a lock, the program name is removed but the terminal ID, operator code and company code 
remain in CLTL.
The following conditions apply to the clearing of locks in CLTL:
 You must be defined as a system administrator in OPER (Operator Code) before you can clear a terminal lock in CLTL.
 If you wish to clear yourself, you must open a new session.
1 Enter CLTL.
2 Click on Enter Criteria.
3 Key in your terminal ID and/or your operator code and click on Execute Query.

Clear Terminal Locks screen showing four active sessions
4 Position your cursor over the terminal that you wish to clear.
5 Click on Clear Locks. 
CAUTION When clearing terminal locks in CLTL for a user, make sure that the 
user exits the program being cleared before he or she resumes work in the program. 
Failure to do so could lead to out of balance inventory. 

MISCELLANEOUS PROGRAMS
Copying Item Codes in COIT
SYSTEM ADMINISTRATION GUIDE 4.2* 149
6 When the message “User still logged on. Are you sure?” appears, click on Yes to proceed. AccellosOne 
3PL will remove the name of the program from the Current Selection column. However, the terminal ID, 
operator code and company code will remain in CLTL.
7 Repeat the above two steps for each additional terminal lock that you wish to remove.
8 When you finish removing your terminal locks, click on Exit to exit.
Copying Item Codes in COIT
You can copy all active items from one customer to another in COIT. For example, suppose you have two 
customers: CUST1 and CUST2. CUST1 has three items (A, B and C) and CUST2 has two items (D and E). If 
you copy CUST1’s items to CUST2 using COIT, CUST2 will have five items — A, B, C, D and E.
The following requirements must be met before you can copy items:
 customers cannot be invoice type only
 customers cannot be the same
 customers must have the same inventory level profile
COIT is typically used in warehouses in which multiple customers share the same item codes.
1 Enter COIT.
2 Key in your from customer and press Enter.
3 Key in your to customer and press Enter.
NOTE COIT copies item information only such as the item code, description, quantity breakdown, billing profile code, weight, etc. It does not copy lot numbers, inventory balances or transaction history information. If you want to transfer inventory from 
one customer to another, you must perform a transfer adjustment in ENAJ, ENOR 
(Transfer type order) or MATR.

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB

Copy Items From One to Another
4 Click on Process.
Adjusting an Item’s Quantity Breakdown in AEQB
AEQB allows you to change the quantity breakdown of an item for all product currently in your warehouse. If 
you change an item’s quantity breakdown in the Quantity Breakdown Block of ITEM, your change will affect 
new inventory only; that is, only inventory received after you make the change. AEQB, on the other hand, 
allows you to change the quantity breakdown of product currently in your warehouse.
For example, suppose your original quantity breakdown for a particular item is 10 cases per pallet and you 
have two pallets (20 cases) in your warehouse. If you change the item’s quantity breakdown to 20 cases per 
pallet in AEQB, looking up your inventory in LOEN after the change will show one pallet containing a total of 
20 cases in your warehouse.
If an item is defined as a standard quantity breakdown item, you must apply the change to all existing 
inventory in your warehouse. If, however, an item is defined as a variable quantity breakdown item, 
you can individually change the quantity breakdown of each inventory entity. For example, lot 101 can have 
10 cases per pallet, lot 102 can have 20 cases per pallet and lot 103 can have 30 cases per pallet.
If you wish to add a breakdown level (for example, from pallets only to pallets/cases) or remove a breakdown 
level (for example, from pallets/cases to pallets only), you cannot run AEQB. You must contact HighJump for 
assistance and fill out an authorization form.

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB
SYSTEM ADMINISTRATION GUIDE 4.2* 151
REPORTS
If the report shows totals in the lowest SKU (for example, cases), changing an item’s quantity breakdown will 
have no affect on the report's totals. If, on the other hand, the report shows totals in a higher SKU such as 
pallets, the way in which AccellosOne 3PL calculates totals will depend on the type of report — inventory or 
history.
Inventory reports will calculate totals based on the current setup in the ITEM master. For example, if you 
change your quantity breakdown from 100 cases per pallet to 80 cases per pallet, your pallet total in any 
inventory report will be based on the new quantity breakdown. Your case total, on the other hand, will not be 
affected.
History reports will calculate totals on a transaction by transaction basis using the quantity breakdown in 
effect when the transaction was performed.
CHANGING THE QUANTITY BREAKDOWN OF A STANDARD QUANTITY 
BREAKDOWN ITEM
1 Enter AEQB.

Adjust Entity Quantity Breakdown (AEQB)
2 Key in your customer code and press Enter.
3 Do one of the following:
4 Click on Execute Query.
If you are changing the quantity 
breakdown of a single item:
If you are changing the quantity 
breakdown of multiple items:
a) Key in your level 1 value or 
select if from the item pick list.
a) Proceed to next step.

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB
5 If you did not enter a level 1 value in step 3, click on the appropriate customer/item combination to select 
the item that you wish to work with. AccellosOne 3PL will populate the Detail Block with all inventory entities for the selected item. 
If you have a large number of records for a given customer and are concerned about performance, you 
can deselect the Auto Display Inventory Details check box to suppress the display of the inventory 
details. When you find the item that you wish to work with, click on the Auto Display Inventory Details 
check box again to select it.

Adjust Entity Quantity Breakdown (AEQB)
6 Click on Update Quantity Breakdown.
Click on the 
appropriate customer/item combination to select 
the item that you 
wish to work with

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB
SYSTEM ADMINISTRATION GUIDE 4.2* 153

Item Quantity Breakdown Details screen
7 Proceed to change the item’s quantity breakdown by entering new values in the Quantity, Number of Layers, Quantity Per Layer and Quantity Odd Layer fields.
8 When you finish making your changes, click on Apply Changes to return to AEQB.

AEQB showing query on level 2 value (lot 102)
9 Click on Select All.
10 Click on Update Selected Records.
11 Check the Update Status message to ensure that your change was successful. If it was, the message 
“Entity Successfully Updated” will display.
12 Click on Exit to exit AEQB.

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB
CHANGING THE QUANTITY BREAKDOWN OF A VARIABLE QUANTITY 
BREAKDOWN ITEM
1 Enter AEQB.

Adjust Entity Quantity Breakdown (AEQB)
2 Key in your customer code and press Enter.
3 Do one of the following:
4 Click on Execute Query.
5 If you did not enter a level 1 value in step 3, click on the appropriate customer/item combination to select 
the item that you wish to work with. AccellosOne 3PL will populate the Detail Block with all inventory entities for the selected item. 
If you have a large number of records for a given customer and are concerned about performance, you 
can deselect the Auto Display Inventory Details check box to suppress the display of the inventory 
details. When you find the item that you wish to work with, click on the Auto Display Inventory Details 
check box again to select it.
NOTE You cannot update the quantity breakdown of a specific inventory entity if 
that inventory entity is on an open order or receipt or is locked by another user.
If you are changing the quantity 
breakdown of a single item:
If you are changing the quantity 
breakdown of multiple items:
a) Key in your level 1 value or 
select if from the item pick list.
a) Proceed to next step.

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB
SYSTEM ADMINISTRATION GUIDE 4.2* 155

Adjust Entity Quantity Breakdown (AEQB)
6 Do one of the following:
If you wish to change the 
quantity breakdown of new 
product and existing product:
If you wish to change the 
quantity breakdown of existing 
product only:
a) Click on Update Quantity 
Breakdown.
b) Proceed to change the item’s 
quantity breakdown by entering 
new values in the Quantity, Number of Layers, Quantity Per Layer 
and Quantity Odd Layer fields.
c) When you finish making your 
changes, click on Apply 
Changes to return to AEQB.
a) Proceed to next step.
Click on the 
appropriate customer/item combination to select 
the item that you 
wish to work with

MISCELLANEOUS PROGRAMS
Adjusting an Item’s Quantity Breakdown in AEQB

Item Quantity Breakdown Details screen

Adjust Entity Quantity Breakdown (AEQB)
7 Proceed to select the inventory records in the Detail Block that the new quantity breakdown will apply to. 
You individually select records by clicking on them or you can use the Select All and Deselect 
All commands. You can also query on individual level 2, 3 and 4 values by means of the Level 2, Level 3 
and Level 4 “Refine Your Query” fields.

MISCELLANEOUS PROGRAMS
Adjusting Location Billing Codes in ADLB
SYSTEM ADMINISTRATION GUIDE 4.2* 157

AEQB showing query on level 2 value (lot 102)
8 When you finish selecting your inventory records, click in the PLT field and key in your new quantity 
breakdown.
9 Click on Update Selected Records.
10 Check the Update Status message to ensure that your change was successful. If it was, the message 
“Entity Successfully Updated” will display.
11 Click on Exit to exit AEQB.
Adjusting Location Billing Codes in ADLB
This program allows you to change a location’s location billing code. For example, you assigned the location 
billing code of FREZ to location 101 in warehouse A and you want to change this code to COOL. Changes in 
ADLB are effective immediately; the next time that you generate your batch in the appropriate program, 
AccellosOne 3PL will generate the applicable charges according to the charge code attached to your new 
location billing code.
You can change the location billing code of a single location, all locations in a single warehouse or all 
locations assigned to a particular location billing code.
You cannot change a location’s location billing code in LOCA (Locations).
1 Enter ADLB.
2 Proceed to query the appropriate records:
To retrieve all locations in a given 
warehouse …
Key in your warehouse code and click on Execute Query.

MISCELLANEOUS PROGRAMS
Adjusting Location Billing Codes in ADLB
3 Click on Location Bill Block.
4 Key in your new location billing code and press Enter.

Adjust Location Billing Code (ADLB) screen showing change from general to dry
5 Do one of the following:
To retrieve a specific 
location …
Key in your warehouse code and press Enter. Then key in your 
location code and click on Execute Query.
To retrieve all locations belonging to a 
given location billing code …
Press Enter twice to bypass the Warehouse Code and Location 
Code fields. Then key in your location billing code and click on Execute Query.
If you wish to change the 
location billing code of the 
currently selected location:
If you wish to change the 
location billing code of all 
locations in the header block of 
ADLB:
a) Click on Process One. a) Click on Process All.

MISCELLANEOUS PROGRAMS
Adjusting Location Types in ADLT
SYSTEM ADMINISTRATION GUIDE 4.2* 159

Adjust Location Billing Code (ADLB) screen showing Remarks Block
6 Do one of the following:
7 Click on Exit to exit.
Adjusting Location Types in ADLT
You can change your location type for a single location or for a range of locations in ADLT. There are three 
location restrictions in this program: you can change a location type for all locations in a warehouse, for a 
given location or for all locations belonging to a given location type.
There are two options in this program: Process One and Process All. Process One will change the location type 
of the currently selected record only while Process All will change the location type of all records in the 
Header Block. For example, suppose you retrieve ten locations from Warehouse 1. You will have ten records 
in the Header Block and the record counter will read “1 of 10.” If you select Process One, AccellosOne 3PL 
will change the location type of record one only; if you select Process All, AccellosOne 3PL will change the 
location type of all ten records in the Header Block.
1 Enter ADLT.
2 Click on Location Type Block to enter the Location Type Block.
3 Key in your new location type and press Enter.
If you wish to enter a 
remark:
If you do NOT wish to enter a 
remark:
a) Enter your remarks.
b) When you finish entering your 
remarks, click on Return to exit 
the Remark Block.
a) Click on Return to exit the 
Remark Block.
NOTE If you wish to see your new location billing codes in the Renewal Block of 
LOEN, you must run the renewal preprocessor (RENW).

MISCELLANEOUS PROGRAMS
Changing the Company Date in DATE or ALDA

Adjust Location Type (ADLT) screen showing location type RACK being changed to BULK
4 Do one of the following:
5 Click on Exit to exit ADLT.
Changing the Company Date in DATE or ALDA
You can change the application system date for your company or companies in either DATE or ALDA. You 
use DATE (Change Company Date) when you wish to change the date in the company in which you are 
currently working; you use ALDA (Change Date for All Companies) when you wish to change the date for all 
companies on your system whose Default to Master Date flag in COMP has been set to Yes.
Changing the date in DATE or ALDA does not affect the Unix system date. The Unix system date is used to 
track the date and time of all time-stamping transactions in the Time Block of LOEN.
1 Enter DATE or ALDA.
If you wish to change the 
location type of the currently 
selected record in the Header 
Block:
If you wish to change the 
location type of ALL records in 
the Header Block:
a) Click on Process One. a) Click on Process All.

MISCELLANEOUS PROGRAMS
Recalculating Inventory Expiry Dates in REEX
SYSTEM ADMINISTRATION GUIDE 4.2* 161

Change Company Date (DATE) screen
2 In the Next Business Day field, key in your new company date and press Enter.
3 Click on Commit.
4 Click on Exit to exit.
Recalculating Inventory Expiry Dates in REEX
This program allows you to recalculate the expiry dates of existing inventory after changing your shelf life 
duration and/or frequency in ITSH (Item Shipping Profile). For example, if you currently calculate the expiry 
date by adding six months to the production date (inventory level 3) and wish to change this formula to the 
production date plus eight months, you must run REEX if you wish to apply the change to existing inventory. 
If you change your shelf life duration and/or frequency in ITSH but do not run REEX, your new formula will 
apply to new inventory only — not existing inventory — and allocation may not pick in correct FIFO/LIFO 
sequence. 
When recalculating expiry dates, you can exempt from recalculation those items using the current company 
date as their expiry date in ITSH. You do so by setting the For Items Using Company Date Recalculate the 
Expiry Date with New Company Date (Y/N) field to N for No. If you set this field to Y for Yes, all items including 
those using the current company date as their expiry date will have their expiry dates recalculated.
When you run REEX, AccellosOne 3PL creates an IF (Information Only) record in the History Block of LOEN 
for inventory whose expiry date formula was changed. The IF record shows both the original expiry date and 
the recalculated expiry date.

MISCELLANEOUS PROGRAMS
Recalculating Inventory Expiry Dates in REEX
1 Enter REEX.

Reset Inventory Expiry Date (REEX) screen
2 Key in your customer code and press Enter.
3 If required, key in your item code and press Enter.
4 In the For Items Using Company Date Recalculate the Expiry Date With New Company Date (Y/N) field, 
press Enter to accept the default value of N for No (recommended) or key in Y for Yes and press Enter.

Reset Inventory Expiry Date (REEX) screen
5 Click on Update Date.
6 Click on Yes when prompted to proceed with update.
7 Do one of the following:
If you wish to add a remark:
If you do NOT wish to add a 
remark:
a) Key in your remarks.
b) When you finish entering your 
remarks, click on Return.
a) Click on Return.

MISCELLANEOUS PROGRAMS
Performing Advanced Queries with SQL Statements
SYSTEM ADMINISTRATION GUIDE 4.2* 163
8 Click on Exit to exit.
Performing Advanced Queries with SQL Statements
The bind variable “:A” allows you to perform advanced queries on most query fields in AccellosOne 3PL. An 
advanced query makes it possible to use parameters such as greater than, less than, not equal to, like or any 
other SQL command in your queries. 
The following list shows some of the more common SQL commands that you can use in a query. If you are 
querying in an alphanumeric field, you must use single quotes for the query value.
Advanced queries can only be performed on unformatted database fields. An unformatted database field is a 
field whose value directly corresponds to a column in a database table. For example, the Customer Code field 
in LORE (Look Up Receipts) is a database field because CUST_CODE is a column in the E_RCPT_H table.
If you wish to perform an advanced query on a date field, the following requirements must be met:
COMMAND DESCRIPTION
> Greater than
< Less than 
!= Not equal to 
= Equal to 
BETWEEN Between
Example
Enter “BETWEEN 123 and 456” to show all receipts in LORE between 
receipts 123 and 456.
LIKE When used with the wildcard (%) character, this command allows you to query 
on individual characters in a code or value. For example, if you enter %A, 
AccellosOne 3PL will retrieve all codes ending in the letter A. If you enter A%, 
AccellosOne 3PL will retrieve all codes starting with the letter A. 
Example
Enter “LIKE ‘A&’” to show all codes starting with the letter ‘A’.
NOT LIKE Similar to the “LIKE” command.
Example
Enter “NOT LIKE ‘&01’” to show all codes that do not end with the numbers 
‘01’.

MISCELLANEOUS PROGRAMS
Performing Advanced Queries with SQL Statements
 you must enter the date in the Oracle date format (the AccellosOne 3PL date format is not valid
 you must enter your query in a non-date field and you must use the actual database column name (for 
example, ORD_CONF_DATE)
1 Enter the program in which you wish to perform the query.
2 Make sure that you are in query mode.
3 Key in :A in the field that you wish to query.

LORE screen showing the bind variable in the Customer Code field
4 Click on Execute Query.
5 In the Query Where window, key in :A followed by your query statement.

MISCELLANEOUS PROGRAMS
Performing Advanced Queries with SQL Statements
SYSTEM ADMINISTRATION GUIDE 4.2* 165

LORE screen showing a receipt query for all receipts in which the customer code does not equal A 
6 Click OK to execute it.
7 When you finish performing your query, click on Exit to exit.
PERFORMING QUERIES ON MULTIPLE FIELDS
If you wish to perform SQL queries on two or more fields, use :A for the first field, :B for the second field and 
so on and so forth.

MISCELLANEOUS PROGRAMS
Performing Advanced Queries with SQL Statements

LOOR screen showing a query on two fields: Customer and Carrier

LOOR screen showing query for customer code equals A and carrier code equals ABC

MISCELLANEOUS PROGRAMS
Looking Up Spooler Activity in LOSP
SYSTEM ADMINISTRATION GUIDE 4.2* 167
Looking Up Spooler Activity in LOSP
Every time that you print or auto-print a document or report, AccellosOne 3PL creates a file in the print 
spooler. You can look up these files in LOSP (Look Up Spooler Activity) and print them to a PC printer at any 
time.
Each file in the print spooler is assigned a five-digit system-generated sequence number. Unless you 
manually delete them, files remain in the print spooler for the number of days for purge retention that you 
define in SPPA (Spool Parameters).
1 Enter LOSP. 
2 When you finish entering your search criteria, click on Execute Query to query the report or document 
that you wish to access. 

Look Up Spooler Activity (LOSP) screen showing files in the print spooler
3 Use your arrow keys to locate the report or document that you wish to access, then press Enter to position your cursor in the Action column. 
4 Key in V for View and press Enter. 
5 Click on Process to process.
NOTE If you set your printer to NONE or VIEW, the report or document will not be 
sent to the spooler and you will be unable to access it in LOSP.

MISCELLANEOUS PROGRAMS
Looking Up Spooler Activity in LOSP
AccellosOne 3PL will display the document or report that you selected in step 5. You can use the Edit/
Find on this page command to search for the information that you require.
6 If you wish to print the report or document, select File/Print and select the appropriate PC printer. Then 
click on Print to print.
7 When you finish viewing and/or printing the file, select File/Close to close the window. 
8 Click on Return to Main and Exit to exit.
LOOKING UP FAX INFORMATION
If a file has been faxed, you can look up the faxing information in the Process Block.
1 Enter LOSP.
2 Key in your search criteria and press Enter.
3 Click on Execute Query to query the reports or documents that you wish to look up.
4 Use your arrow keys to locate the report or document that you wish to access, then press Enter to position your cursor in the Action column. 
5 Click on Fax Information.

Look Up Spooler Activity (LOSP) screen showing fax information in Process Block
6 When you finish looking up your fax information, click on Exit and Return to Main. Then click on Exit 
again to exit.

MISCELLANEOUS PROGRAMS
Setting Up Sort Sequence Codes in SOSE
SYSTEM ADMINISTRATION GUIDE 4.2* 169
Setting Up Sort Sequence Codes in SOSE
Sort sequence codes allow you to customize the sort sequence of certain lists in AccellosOne 3PL such as 
the physical inventory tickets that you create in PHTI and the cycle count tickets that you create in CYGT. 
They are currently used a number of programs including ENPH (Enter Physical Parameters), CYEN (Create 
Cycle Count), MRFP (RF Profile Code) and PSPR (RF Substitution Profile Code).
If you do not use sort sequence codes, these lists will be sorted in ascending alphanumeric order; for 
example, 101, 102, 103, 104.
SOSE supports any valid SQL statement that can follow an “order by” command; since the “order by” clause 
is automatically added to your statement, it should not be entered in SOSE.
If you know SQL, you can create your own sort sequence codes and attach them to the appropriate program. 
If you do not know SQL, you can contact HighJump for assistance.
1 Enter SOSE.
2 Click on Create Record.
3 Key in your sort sequence code and press Enter.
4 Key in a description for your new code and press Enter.
5 Key in your sequence formula and press tab.
6 Click on Return to Main to exit create record mode.
NOTE SOSE does not check the validity of your SQL statement. If your statement 
is invalid, you will get an error message when running the program that your sort 
sequence code is attached to.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Utilization in LOWU

SOSE screen showing sort sequence code for sorting location codes in descending order
7 Click on Exit to exit SOSE.
8 Attach your new SOSE code to the appropriate program.
Looking Up Your Warehouse Utilization in LOWU
This program shows the total capacity of each warehouse, the actual number of pallets, cases or other SKU 
type in the warehouse and the amount of free space as a percentage of the total capacity. Also shown are 
utilization values for “Today”, “Tomorrow” and “Next Day”.
For each warehouse, you can enter LOLO (Look Up Location Information) and look up capacity information 
for each location.
The utilization values are calculated as follows:
Utilization % the total on-hand quantity grouped by SKU class for all locations in 
the warehouse/the total capacity for all locations in the warehouse 
* 100

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Utilization in LOWU
SYSTEM ADMINISTRATION GUIDE 4.2* 171
1 Enter LOWU.

Enter Query screen
2 Key in your search criteria. You can query by building code, warehouse code, isolator code, location type 
code or any combination of these search criteria. 
3 When you finish entering your search criteria, click on Execute Query .
Today the actual capacity for “Today” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt 
date = today
 the total of all non-confirmed R-type order location lines with a to 
ship date = today
This sum is divided by total capacity of the warehouse and then 
multiplied by 100 to arrive at today’s utilization.
Tomorrow the actual capacity for “Tomorrow” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt 
date = today + 1
 the total of all non-confirmed R-type order location lines with a to 
ship date = today + 1
This sum is divided by total capacity of the warehouse and then 
multiplied by 100 to arrive at tomorrow’s utilization.
Next Day the actual capacity for “Next Day” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt 
date = today + 2
 the total of all non-confirmed R-type order location lines with a to 
ship date = today + 2
This sum is divided by total capacity of the warehouse and then 
multiplied by 100 to arrive at the next day’s utilization.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Utilization in LOWU

Look Up Warehouse Utilization screen showing utilization information for warehouse 1
4 If you wish to look up capacity information for individual locations within a warehouse, use your arrow 
keys to position the cursor beside the warehouse that you wish to look up and click on Drill Down to 
Locations .

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
SYSTEM ADMINISTRATION GUIDE 4.2* 173

Look Up Warehouse Utilization screen showing LOLO
5 Proceed to look up your location in LOLO in the normal manner.
6 When you finish looking up your location information, click on Exit to exit LOLO.
7 Click on Exit to exit LOWU.
Looking Up Your Warehouse Activity in SAM
This program allows you to look up all activity in your warehouse. It shows all inbound receipts, outbound 
orders, relocations, CRM’s, appointments and outbound loads for the date range that you specify. For 
outbound and appointment activity, you can specify which date to use (to ship date, to arrive date, etc.) when 
specifying a date range. For inbound and outbound load activity, the date used in the date range fields cannot 
be changed.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
SAM also shows all current operator activity: that is, each operator currently signed on to AccellosOne 3PL.
TAB DESCRIPTION
Inbound Activity For each receipt, SAM shows the receipt number, level 1 value, number of units, weight, number of pallets, priority number, flow code, 
warehouse/location, operator code and receipt date.
If the receipt has been deleted, the number of units will be shown as 
zero.
You can restrict your inbound activity query to show only late or in process receipts. A receipt is considered “late” if the receipt date is less 
than the current date. A receipt is considered “in process” if the receipt 
date equals the current date or falls in the future.
Outbound Activity For each order, SAM shows the order number, level 1 value, number of 
units, weight, number of pallets, priority number, flow code, warehouse/location, operator code and to ship date.
If the order has been deleted, the number of units will be shown as 
zero.
You can restrict your outbound activity query to show only late or in 
process orders. An order is considered “late” if the to ship date is less 
than the current date. An order is considered “in process” if the to ship 
date equals the current date or falls in the future.
Outbound Loads For each load, SAM shows the load number, the date and time that the 
load was created, the load’s status, the carrier, the external load number, the building and door, the number of units, the gross and net 
weight, and the percentage loaded.
If the load has been deleted, the number of units will be shown as zero.
You can restrict your outbound load activity query to show only late or 
in process loads. A load is considered “late” if the load creation date is 
less than the current date. A load is considered “in process” if the load 
creation date equals the current date or falls in the future.
Inventory Activity For each relocation, SAM shows the adjustment number, level 1 value, 
number of units, number of pallets, status, warehouse/location, operator code and transaction date.
CRM For each CRM, SAM shows the CRM number, customer code, 
assigned to operator, status, CRM code, date, type and operator.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
SYSTEM ADMINISTRATION GUIDE 4.2* 175
1 Enter SAM.

Query window
Appointment For each appointment, SAM shows the appointment number, date, 
building and door, carrier, whether the appointment is inbound or outbound, document number, load type, number of units, number of pallets and gross weight.
You can restrict your appointment query to show only late appointments. An appointment is considered “late” if the appointment arrival 
date is later than the appointment start date.
Operator Activity SAM shows each operator currently working in AccellosOne 3PL, the 
program that the operator is working in and whether or not the program 
is an RF program.
TAB DESCRIPTION

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
2 Do one of the following:
3 When you finish entering your search criteria, click on Execute Query .

Supervisory Activity Management screen (SAM) showing inbound activity
4 If you wish to see activity for each line of a given receipt, click on the Receipt/Lines button of the 
receipt that you wish to look up. When you finish looking up your receipt lines, you can click this button 
again to toggle back to receipt summary view.
If you wish to enter your search 
criteria manually:
If you wish to run a personal 
query:
a) Key in your search criteria. You 
can query by date range, receipt 
number, order number, appointment number, CRM number, customer code, item code, operator 
code, consignee code, carrier 
code and shipper code. 
b) If you wish to restrict your query 
to inbound activity, outbound 
activity, relocation activity, etc., 
deselect the appropriate check 
boxes to exclude the activities 
that you do not wish to see. 
When you deselect an activity, 
the corresponding tab on query 
results screen is greyed out.
a) Select your personal query from 
the My Queries dropdown list.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
SYSTEM ADMINISTRATION GUIDE 4.2* 177
You can also perform queries within the Inbound tab by means of the Enter Query and Execute 
Query commands.
5 If the Appointment tab is active, click on it to see your appointment activity.

SAM screen showing appointment activity
6 You can perform queries within the Appointment tab by means of the Enter Query and Execute Query commands.
7 If the CRM tab is active, click on it to see your CRM activity.

SAM screen showing CRM activity

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
8 You can perform queries within the CRM tab by means of the Enter Query and Execute Query 
commands.
9 If the Outbound tab is active, click on it to see your outbound activity.

SAM screen showing outbound activity
10 If you wish to see activity for each line of a given order, click on the Order/Lines button of the order 
that you wish to look up. When you finish looking up your order lines, you can click this button again to 
toggle back to order summary view.
You can also perform queries within the Outbound tab by means of the Enter Query and Execute Query commands.
11 If the Inventory tab is active, click on it to see your relocation activity.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM
SYSTEM ADMINISTRATION GUIDE 4.2* 179

SAM screen showing relocation activity
12 If the Outbound Loads tab is activated, click on it to see your outbound load activity.

SAM screen showing outbound load activity
13 You can perform queries within the Outbound Loads tab by means of the Enter Query and 
Execute Query commands.
14 If the Operator Activity tab is active, click on it to see your operator activity.

MISCELLANEOUS PROGRAMS
Looking Up Your Warehouse Activity in SAM

SAM screen showing operators activity
15 You can perform queries within the Operator Activity tab by means of the Enter Query and 
Execute Query commands.
16 When you finish looking up your warehouse activity, click on Exit to exit SAM.
LOOKING UP SUMMARY INFORMATION IN SAM
The Summary window in SAM shows summary information for receipts, orders, CRM’s, relocations and 
replenishments. The summary information shown is always based on the main or non-summary query.
1 Enter SAM.
2 Enter your search criteria and click on Execute Query.
3 When AccellosOne 3PL retrieves your query results, click on Summary.

SAM screen showing Summary window
4 Click on Return to exit.

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
SYSTEM ADMINISTRATION GUIDE 4.2* 181
Working With the Translation Manager in TRMA
The Translation Manager is a powerful field label and message management system that allows you to 
customize field labels, hint lines, system codes, error messages, menu names, button text and any other text 
appearing in the AccellosOne 3PL suite of products. The field labels, system codes and error messages that 
you manage in the Translation Manager apply to ActiveDesktop, AccellosOne 3PL, Standard Reports, eVista, d’Amigo and RF.
There are two update modes in TRMA: single entity update and mass update. In single entity mode, you 
update individual field labels, system code, button text, etc. one record at a time. In mass update mode, you 
update all instances of a field label, system code, button text, etc. in a single step.

TRMA query screen
FIELD DESCRIPTIONS (QUERY MODE)
Language Code The language that you wish to update. The update language need not be the 
same as the query language. For example, you can query by standard text 
(that is, English) and update Spanish.
Mass Update If you select this option, AccellosOne 3PL will retrieve a single record representing all instances of your search term and any changes that you make will 
apply to all instances. If you leave this option blank, AccellosOne 3PL will 
retrieve one record for each instance of your search term and you will have to 
update each record individually.

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
Application Code ActiveDesktop
All field labels and error messages used in ActiveDesktop.
Documents
Order and receipt documents set up in DOCU and printed from PROM, 
PROR, PRRE and PRRM.
Dynamic Forms
A dynamic form is a form in which all the field names and dropdown lists are 
stored in the database rather than in the program. Dynamic forms are used in 
a small number of maintain programs such MRFP, VOPC and VOPR.
Menus
The name of your menus as set up in JOSE (Job Selection Code).
Messages
All hint lines, pop-up messages, button text and block names used in static 
forms.
RF
All field labels, system prompts and error messages used in RF.
RF Loading Programs
All field labels, system prompts and error messages used in the RF loading 
programs.
Static Forms
All field labels used in static forms and standard reports. Static forms represent the vast majority of forms in AccellosOne 3PL. Also includes the output of 
standard reports.
System Codes
The codes that users select from dropdown and pick lists.
d’Amigo
All field labels, system prompts and error messages used in d’Amigo.
e-Vista
All field labels, system prompts and error messages used in e-Vista. Any 
changes to e-Vista field labels, system prompts and error messages must be 
activated in e-Vista before you can see them on your screen.
FIELD DESCRIPTIONS (QUERY MODE)

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
SYSTEM ADMINISTRATION GUIDE 4.2* 183
UPDATING A SINGLE ENTITY
You update a single entity by leaving the Mass Update checkbox blank. if a single entity has multiple records 
in TRMA, you will have to update each record individually.
1 Enter TRMA.
2 Select your language code from the dropdown list.
3 If required, select your application code from the dropdown list.
4 If you selected Dynamic Forms, Static Forms or RF as your application code, you can select the appropriate entity code from the dropdown list. If you selected Menus as your application code, you can enter 
the appropriate JOSE code or message number in the Label Code field.
Entity Code Only useful for Static and Dynamic Forms and RF
The name of the program containing the field label. For example, ENRE, 
CUST, ITEM, etc.
Label Code Only useful when the application code = Menus or Messages. For example, if 
you enter ENRE, you can change ENRE’s description.
Label Sub-Code For HighJump use only.
Standard Text The standard text word or phrase that you are searching for. If you do not 
know the full word or phrase, you can use the wildcard character (“%”) to represent the unknown letters or words.
Standard text is in English only and is set up and maintained by HighJump. 
You cannot change standard text. However, you can query by standard text 
and them make your change to the corresponding language text.
Match Case If you select this option, the case of each letter must match in query. If you do 
not select this option, the Translation Manager ignores case when performing 
a query.
Language Text The language text word or phrase that you are searching for. If you do not 
know the full word or phrase, you can use the wildcard character (“%”) to represent the unknown letters or words.
Language text belongs to a language set up in LANG. You can modify language text at any time and your changes will be seen by all users assigned 
that language in OPER.
Match Case If you select this option, the case of each letter must match in query. If you do 
not select this option, the Translation Manager ignores case when performing 
a query.
FIELD DESCRIPTIONS (QUERY MODE)

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
5 Do one of the following:
6 If your query is case sensitive, click on the appropriate Match Case checkbox.

TRMA screen showing query for “item code”
7 Click on Execute Query.

TRMA screen showing 78 records in the Header Block containing the word “Item Code”
If you are searching for standard 
text:
If you are searching for language 
text:
a) In the Standard Text field, key in 
the word or phrase that you are 
searching for.* 
a) In the Language Text field, key in 
the word or phrase that you are 
searching for.* 
* If you are not sure of the exact word or phrase, you can use the wildcard character 
(“%”) to represent unknown or missing letters or words.

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
SYSTEM ADMINISTRATION GUIDE 4.2* 185
8 Click in the Header Block.
9 Use your Up and Down arrow keys to scroll through the list of records in the Header Block.
10 When you reach the record that you wish to change, click in the blank field below and key in your 
change. If the message is a multi-line message, click on Ctrl + E to enter the Text Editor. Then key in your 
changes and click Ok to confirm or Cancel to exit without saving your changes.

TRMA screen showing the editing of a multi-line message

TRMA screen showing “Product Code” as the new label for “Item Code” in the program PIIT
11 When you finish making your changes, click on Save.
12 Click on Exit to exit.

MISCELLANEOUS PROGRAMS
Working With the Translation Manager in TRMA
PERFORMING A MASS UPDATE
The Mass Update function allows you to update all instances of a field label, system code, button text, etc. in 
a single step. For example, if you wish to change “Item Code” to “Product Code” in the dozens of programs 
that this label appears in, you would use the Mass Update function.
When you perform a mass update, TRMA displays the number of labels that will be updated. Also displayed 
is the Multiple Labels checkbox. If this checkbox is selected, there have been manual overrides to the label 
that you wish to change and your changes will overwrite them. For example, “Item Code” has already been 
changed to “Product Code” or some other value in one or more programs and these changes will be lost 
when you perform your mass update.
1 Enter TRMA.
2 Select your language code from the dropdown list.
3 Click on Mass Update.
4 If required, select your application code from the dropdown list.
5 If you selected Dynamic Forms, Static Forms or RF as your application code, you can select the appropriate entity code from the dropdown list. If you selected Menus as your application code, you can enter 
the appropriate JOSE code in the Label Code field.
6 Do one of the following:
7 If your query is case sensitive, click on the appropriate Match Case checkbox.
8 Click on Execute Query.

TRMA screen showing seven records for “ITEM CODE” and 79 records for “Item Code”
9 Click in the blank field below the record that you wish to change and key in your changes.
10 When you finish making your changes, click on Save.
11 Click on Exit to exit.
If you are searching for standard 
text:
If you are searching for language 
text:
a) In the Standard Text field, key in 
the word or phrase that you are 
searching for.* 
a) In the Language Text field, key in 
the word or phrase that you are 
searching for.* 
* If you are not sure of the exact word or phrase, you can use the wildcard character 
(“%”) to represent unknown or missing letters or words.

MISCELLANEOUS PROGRAMS
Copying Codes Between Companies in COCO
SYSTEM ADMINISTRATION GUIDE 4.2* 187
Copying Codes Between Companies in COCO
This program allows you to copy setup codes and profiles from one company to another. Using COCO it is 
easy to duplicate your setups for testing purposes and to set up new companies/facilities with the assurance 
that a given customer in a new facility will have the same billing, allocation and item setup that the customer 
had in the old facility. 
When you copy a code or profile, any dependencies for that code or profile are automatically copied as well 
even if you did not select them in COCO. For example, if you copy CUST, all the dependencies of CUST such 
as DBIP, FLPR, DILP, etc. will be copied as well even if you did not select them and even if they are deactivated profiles.
If you explicitly select a code or profile in COCO, it will only be copied if it is active. The following restrictions 
apply to COCO:
1 Enter COCO.
PROGRAM RESTRICTIONS
DLVP customer and item details are not copied
DOOR warehouse and locations are not copied
ILOP Mandatory warehouse and locations codes defined in LOCA are copied to the 
new company. If the location format in the new company differs from the location format in the old company, these copied location codes will require manual adjustment.
IRHP customer and item details are not copied
MRFP warehouse and locations are not copied
LOCA Mandatory warehouse and locations codes defined in LOCA are copied to the 
new company. If the location format in the new company differs from the location format in the old company, these copied location codes will require manual adjustment.
RATE All rates are copied. If there are any non-.ALL rates in your from company, the 
customers attached to those non-.ALL rates as well as all the customer’s 
items and any other dependencies are copied too.
See the Billing and Invoicing Guide for further information on the Use Current 
Effective Date of From Customer (RATE) checkbox.

MISCELLANEOUS PROGRAMS
Copying Codes Between Companies in COCO

COCO screen
2 Select your from company from the dropdown list.
3 Select your to company from the dropdown list.
4 Click on the code and profile that you wish to copy. To select multiple codes and profiles, press and hold 
the Ctrl key while you make your selection. To select a range of codes and profiles, click on the first item 
in the range. Then press and hold the shift key before clicking on the last item in the range.

MISCELLANEOUS PROGRAMS
Performing a Mass Update of an Item Value in IMAS
SYSTEM ADMINISTRATION GUIDE 4.2* 189

COCO screen showing six selections
5 When you finish making your selections, click on Process.
6 When prompted to confirm the copy, click on Yes.
7 Click on Yes again to acknowledge the “Copy done” message.
8 Click on Exit to exit.
Performing a Mass Update of an Item Value in IMAS
You can perform a mass update of an item’s item value in IMAS. You select the items to be updated by 
alternate inventory reporting type and alternate inventory reporting code defined in ITAS (Item Alternate 
Sorts).
1 Enter IMAS.

MISCELLANEOUS PROGRAMS
Importing Orders and Receipts in IFFI
IMAS screen
2 Select your alternate inventory reporting type from the dropdown list.
3 Select your alternate inventory reporting code from the dropdown list.
4 Key in your new item value.
IMAS screen showing all items assigned the alternate inventory reporting type/code of MEAT/BEEF
5 Click on Process .
6 When prompted to proceed with the update, click on Yes.
7 Click on Exit to exit.
Importing Orders and Receipts in IFFI
You can import orders and receipts from CSV files in IFFI.
1 Place the files to be uploaded into the $DEL4_HOME/del4/work/faxlp directory on the Linux server.
2 Enter IFFI.

MISCELLANEOUS PROGRAMS
Importing Orders and Receipts in IFFI
SYSTEM ADMINISTRATION GUIDE 4.2* 191
IFFI screen
3 Select your file conversion type from the dropdown list.
4 Select your customer from the dropdown list.
5 Key in your file name and click on Process .
6 If the import fails for any reason, click on Yes to acknowledge the error message.

MISCELLANEOUS PROGRAMS
Importing Orders and Receipts in IFFI

SYSTEM ADMINISTRATION GUIDE 4.2* 193
SPECIAL VERIFICATION PROGRAMS
Overview .......................................................................................................... 194
Looking Up Special Verification Programs in LOSV ................................... 196
Creating Your Own Special Verification Program in MSVS ........................ 197
Mandatory Order Accessorials (MOAC)........................................................ 198
Mandatory Receipt Accessorials (MRAC)..................................................... 199
Mandatory Receipt Carrier Details (MRCA) .................................................. 200
Mandatory Order Carrier Details (MOCA) ..................................................... 201
Order Total Quantity Verification (OTQV) ..................................................... 202
Create Receipt from Order (CRCU) ............................................................... 203
Mandatory Order Line Carton ID (MOCI)....................................................... 203
Update Order To Ship Date (UOTS)............................................................... 204
Order Charges (ORCH) ................................................................................... 204
Receipt Charges (RECH) ................................................................................ 205

SPECIAL VERIFICATION PROGRAMS
Overview
Overview
A special verification program is a custom program or plug-in that is automatically run at some stage in your 
inbound receiving or outbound shipping process. Special verification programs perform a variety of functions 
some of which are visible to the user and some of which are not.
They can display the Pallet Details Block or the Bill Later - Enter Charges screen, update the Time-Stamping 
Block of LORE/LOOR for the appointment system, create back orders, cancel the printing of auto-printed 
documents, check for non-numeric values in the Extra Reference fields of ENOR/ENRE, create back receipts 
for product not received on the original receipt and perform many other functions.
Special verification programs are only executed via ENRE/ENOR, CHRF /CHOF and CORL/COOR.
You set up special verification programs in the Special Verification Block of DIFP (Depositor Workflow Profile). 
Special verification programs can be attached to any flow in your inbound or outbound flow profile. For 
example, the special verification CBOR (Create Back Order) allows you to create back orders at any 
outbound flow on your system except ENOR (Enter Order).
FIELD DESCRIPTIONS
Sequence Mandatory
If you have multiple special verification programs attached to the same flow, 
you specify their sequence by means of a sequence number. If you have a 
single special verification program, use the number 10.
Special Verification Code Mandatory
Your special verification code.
Complete Y = Yes
N = No
If you set this flag to Y for Yes, the special verification program must run successfully before you can advance to the next flow. For example, if you attach a 
special verification program for catch weights to FLOW2 and set this flag to Y, 
you will not be able to advance to FLOW3 if you fail to capture a catch weight.
If you set this flag to N for No, you can advance to the next flow even if the 
special verification program does not run successfully.
NOTE If you set this flag to Y for Yes, you must set the Sequence flag to B 
for Before.

SPECIAL VERIFICATION PROGRAMS
Overview
SYSTEM ADMINISTRATION GUIDE 4.2* 195
1 Enter DIFP.
2 Select the flow profile to which you wish to attach the special verification program.
3 Click on In/Out/Repi/Relo Block.
4 Use your arrow keys to select Inbound or Outbound and click on Flow Block.
5 In the Flow Block, select the appropriate flow.
6 Click on Document Block.
7 Click on Special Verify Block.

Depositor Workflow Profile (DIFP) screen showing Special Verification Block
8 Key in your sequence number (for example, 10) and press Enter.
9 Key in your special verification code and press Enter or use your pick list to select it. To select a code 
using a pick list, press F10 to display the pick list, position your cursor over the appropriate code using 
your arrow keys and click on Select to select it.
Sequence A = After
B = Before
If you set this flag to A for After, the special verification program will run after
the flow to which it is attached. If you set this flag to B for Before, the special 
verification program will run before the flow to which it is attached.
Display Reserved for future use.
FIELD DESCRIPTIONS

SPECIAL VERIFICATION PROGRAMS
Looking Up Special Verification Programs in LOSV
10 In the Complete field, key in Y for Yes or N for No and press Enter.
11 In the Sequence field, key in A for After or B for Before and press Enter.
12 Press Enter to bypass the Display field.

Depositor Workflow Profile (DIFP) screen showing special verification MRAC attached to the flow 
DRAR
13 Click on Return to Main to exit create mode.
14 Click on Document Block, Flow Block, In/Out/Repi/Relo Block and then Master Block.
15 Click on Exit to exit.
Looking Up Special Verification Programs in LOSV
You can look up a complete list of all special verification programs in LOSV (Look Up Special Verification).
1 Enter LOSV.
2 Click on Execute Query.

SPECIAL VERIFICATION PROGRAMS
Creating Your Own Special Verification Program in MSVS
SYSTEM ADMINISTRATION GUIDE 4.2* 197

Look Up Special Verification (LOSV) screen
3 When you finish looking up your special verification programs, click on Exit.
Creating Your Own Special Verification Program in MSVS
MSVS (Special Verifier SQL) allows you to create your own special verify programs to implement specific 
validation for an order or receipt. You can define a sequence of SQL statements and attach this sequence to 
a combination of customer, carrier, consignee/ shipper, return value, type of failure and error message. The 
resulting objects are attached to a workflow in DIFP.

SPECIAL VERIFICATION PROGRAMS
Mandatory Order Accessorials (MOAC)
MSVS screen showing sample special verification program
Mandatory Order Accessorials (MOAC)
This special verify program prompts you to enter an accessorial charge when you exit ENOR or advance to 
the next flow in CHOF. You can enter an accessorial charge or you can click on Exit to exit without entering an 
accessorial charge.

SPECIAL VERIFICATION PROGRAMS
Mandatory Receipt Accessorials (MRAC)
SYSTEM ADMINISTRATION GUIDE 4.2* 199

MOAC screen showing Bill Later - Enter Charges program
Mandatory Receipt Accessorials (MRAC)
This special verify program prompts you to enter an accessorial charge when you exit ENRE or advance to 
the next flow in CHRF. You can enter an accessorial charge or you can click on Exit to exit without entering an 
accessorial charge.

SPECIAL VERIFICATION PROGRAMS
Mandatory Receipt Carrier Details (MRCA)

MRAC screen showing Bill Later - Enter Charges program
Mandatory Receipt Carrier Details (MRCA)
This special verify program displays the Carrier Details block when you exit ENRE or advance to the next flow 
in CHRF. You can enter your carrier details or you can click on Exit to exit without entering carrier details.
NOTE MRCA operates independently of the Carrier Details flag in ENRE. If you 
enter (C)onfirmation or (B)oth in the Carrier Details field in ENRE, the Carrier Details 
screen will appear twice during receipt confirmation. To see the pop-up screen only 
once during receipt confirmation, you must bypass the Carrier Details field.

SPECIAL VERIFICATION PROGRAMS
Mandatory Order Carrier Details (MOCA)
SYSTEM ADMINISTRATION GUIDE 4.2* 201

MRCA screen showing Carrier Block
Mandatory Order Carrier Details (MOCA)
This special verify program displays the Carrier Details block when you exit ENOR or advance to the next flow 
in CHOF. You can enter your carrier details or you can click on Exit to exit without entering carrier details.
NOTE MOCA operates independently of the Carrier Details flag in ENOR. If you 
enter (C)onfirmation or (B)oth in the Carrier Details field in ENOR, the Carrier Details 
screen will appear twice during order confirmation. To see the pop-up screen only 
once during order confirmation, you must bypass the Carrier Details field.

SPECIAL VERIFICATION PROGRAMS
Order Total Quantity Verification (OTQV)

MOCA screen showing Carrier Block
Order Total Quantity Verification (OTQV)
This special verify program displays the total order quantity when you advance to the next flow in CHOF 
(Time Stamp and Confirm Orders). The total order quantity is shown in whichever SKU or SKU’S were 
entered in ENOR. For example, if line 1 is entered as one pallet, line 2 is entered as 60 cases, line 3 is 
entered as 10 cases and line four is entered as 5 eaches, the total order quantity shown in OTQV will be one 
pallet (line 1), 70 cases (lines 2 and 3) and 5 eaches (line 4).
The operator will be prompted to accept the total order quantity. If the operator accepts the total order 
quantity, the order’s flow will be advanced normally. If the operator does not accept the total order quantity, 
the order’s flow will not be advanced.
OTQV must be attached to an outbound flow before COOR (Confirm Order).

SPECIAL VERIFICATION PROGRAMS
Create Receipt from Order (CRCU)
SYSTEM ADMINISTRATION GUIDE 4.2* 203

CHOF screen showing total quantity of 1 pallet, 70 cases and 5 eaches on order
Create Receipt from Order (CRCU)
This special verify allows you to re-receive product on an outbound order as a new receipt. It is similar to a 
transfer order with one important difference: the receipt customer is the same as the order customer.
CRCU is normally attached to the flow COOR (Confirm Order).
Mandatory Order Line Carton ID (MOCI)
This special verify checks that each order line has been assigned a carton ID. It is normally attached to the 
flow COOR (Confirm Order).
CHOF screen showing missing carton ID message

SPECIAL VERIFICATION PROGRAMS
Update Order To Ship Date (UOTS)
Update Order To Ship Date (UOTS)
This special verify sets the to ship date to the order confirmation date. if you do not use this special verify, the 
default to ship date is the order confirmation date plus one day.
UOTS must be attached to the flow COOR (Confirm Order).
Order Charges (ORCH)
This special verify allows you to add accessorial charges to an order. It must be attached to the outbound flow 
COOR in DIFP. If there are previously entered charges for the order, they will be displayed in the Detail Block.
If there are extra charges on the order, running ORCH will automatically generate and confirm the extra 
charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra 
charge audit and confirm the extra charge batch. 
ORCH
NOTE Extra charge batches created through ORCH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra 
charges on the extra charge batch are fully editable in ENAC.

SPECIAL VERIFICATION PROGRAMS
Receipt Charges (RECH)
SYSTEM ADMINISTRATION GUIDE 4.2* 205
Receipt Charges (RECH)
This special verify allows you to add accessorial charges to a receipt. It must be attached to the inbound flow 
CORE in DIFP. If there are previously entered charges for the receipt, they will be displayed in the Detail 
Block.
If there are extra charges on the receipt, running RECH will automatically generate and confirm the extra 
charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra 
charge audit and confirm the extra charge batch. 
RECH
NOTE Extra charge batches created through RECH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra 
charges on the extra charge batch are fully editable in ENAC.

SPECIAL VERIFICATION PROGRAMS
Receipt Charges (RECH)

SYSTEM ADMINISTRATION GUIDE 4.2* 207
A
ActiveDesktop icons, assigning to users 74
ActiveDesktop Security Administrator (ADSA) 70
Adjust Entity Quantity Breakdown (AEQB) 150
Adjust Location Billing Code (ADLB) 157
Adjust Location Type (ADLT) 159
ADLB (Adjust Location Billing Code) 157
ADLT (Adjust Location Type) 159
ADSA (ActiveDesktop Security Administrator) 70
advanced queries 163
AEQB (Adjust Entity Quantity Breakdown) 150
ALDA (Change Date For All Companies) 160
Archive/Purge Processing (ARPU) 83
archiving and purging
accessorial and immediate charges 87
inventory 85
looking up
inventory to be purged 90
orders to be purged 88
receipts to be purged 89
overview 80
receipts and orders 83
the spooler files 96
warnings and messages 97
ARPU (Archive/Purge Processing) 83
C
Change Company Date (DATE) 160
Change Date for All Companies (ALDA) 160
Clear Non-Billing Customer (CNBC) 86
Clear Terminal Locks (CLTL) 148
CLTL (Clear Terminal Locks) 148
CNBC (Clear Non-Billing Customer) 86
COAC (Company Access) 46
COCO (Copy Codes Between Companies) 187
COER (Conversion Exception Report) 143
COIT (Copy Items From One to Another) 149
COMP (Company Code) 6
companies, assigning program access to 46
companies, removing program access from 48
Company Access (COAC) 46
Company Code (COMP) 6
company setup 6
Conversion Exception Report (COER) 143
conversions 139
carrier details 127
COER (Conversion Exception Report) 143
consignee details 122
Conversion Exception Report (COER) 143
creating your csv files 104
DEPC (Data Extraction Process for Conversion) 144
existing locations 122
from a non-AccellosOne 3PL system 102
from AccellosOne 3PL system 144
inventory balances 134
item details 108
location details 118
LOCO (Load Conversion) 139
MOCO (Modify Conversion Data) 140
Modify Conversion Data (MOCO) 140
overview 102
performing 139
PRCO (Process Conversion) 141
Process Conversion (PRCO) 141
report 143
revenue master details 132
shipper details 125
transaction history details 129
ZIP codes 133
COOA (Copy Operator Access) 60
Copy Codes Between Companies (COCO) 187
Copy Items From One to Another (COIT) 149
Copy Operator Access (COOA) 60
CRCU (Create Receipt from Order) 203
Create Receipt from Order (CRCU) 203
D
Data Extraction Process for Conversion (DEPC) 144
INDEX

INDEX
DATE (Change Company Date) 160
DEAR (Delete Archive/Purge) 94
Delete Archive/Purge (DEAR) 94
DEPC (Data Extraction Process for Conversion) 144
E
Executable Job Code (EXJO) 36
executable job codes, looking up 45
EXJO (Executable Job Code) 36
expiry dates, resetting in REEX 161
F
fax information, looking up in LOSP 168
I
IFFI (Interface From File) 190
IMAS (Item Mass Update) 189
INST (Installation Parameters) 75
Installation Parameters (INST) 75
inventory access code 50
item codes, copying in COIT 149
Item Mass Update (IMAS) 189
J
Job Selection Code (JOSE) 39
JOSE (Job Selection Code) 39
L
Load Conversion (LOCO) 139
location billing codes, adjusting in ADLB 157
location types, adjusting in ADLT 159
locks on programs 37
locks, clearing 148
LOCO (Load Conversion) 139
Look Up Special Verification (LOSV) 196
Look Up Spooler Activity (LOSP) 167
Look Up Warehouse Utilization (LOWU) 170
LOSP (Look Up Spooler Activity) 167
LOSV (Look Up Special Verification) 196
LOWU (Look Up Warehouse Utilization) 170
M
Mandatory Order Accessorials (MOAC) 198
Mandatory Order Line Carton ID (MOCI) 203
Mandatory Receipt Accessorials (MRAC) 199
Mandatory Receipt Carrier Details (MRCA) 200
menu structure 54
MOAC (Mandatory Order Accessorials) 198
MOCI (Mandatory Order Line Carton ID) 203
MOCO (Modify Conversion Data) 140
Modify Conversion Data (MOCO) 140
MRAC (Mandatory Receipt Accessorials) 199
MRCA (Mandatory Receipt Carrier Details) 200
MSVS (Special Verifier SQL) 197
O
OPAC (Operator Access) 54
OPER (Operator Code) 49
Operator Access (OPAC) 54
Operator Code (OPER) 49
Operator Restrictions (OPRS) 62
operator setup 49
OPRS (Operator Restrictions) 62
ORCH (Order Charges) 204
Order Charges (ORCH) 204
Order Total Quantity Validation (OTQV) 202
OTQV (Order Total Quantity Validation) 202
P
passwords
for initial sign-on 49
resetting 53
PRCO (Process Conversion) 141
Process Conversion (PRCO) 141
program access
assigning to users 54
removing users from 59
program locks 37
program setup 35
programs paths, looking up 43
programs, assigning to companies 46
Purge Warnings/Messages (PUWM) 99
purging and archiving
performing the purge 94
PUWM (Purge Warning/Messages) 99
Q
quantity breakdowns, adjusting in AEQB 150
queries, advanced 163
R
RATE (special verify for rating receipts) 86
Receipt Charges (RECH) 205
RECH (Receipt Charges) 205
REEX (Reset Inventory Expiry Date) 161
Reset Inventory Expiry Date (REEX) 161
Reset Operator Password (ROPA) 53
restricting user access 62
RF supervisors, setting up 52
Role (ROMA) 67
ROMA (Role) 67
ROPA (Reset Operator Password) 53
S
SAM (Supervisory Activity Management) 173
setting up
companies 6
company access 46
programs 35
submenus 41
users 49
setup programs, overview 5
show inventory access code 50
Sort Sequence Code (SOSE) 169
SOSE (Sort Sequence Code) 169
special verification programs 194

INDEX
SYSTEM ADMINISTRATION GUIDE 4.2* 209
Spool Parameters (SPPA) 96
spooler activity, looking up in LOSP 167
SPPA (Spool Parameters) 96
SQL statements in advanced queries 163
submenus
deleting 43
looking up 56
setting up 41
supervisors, setting up 52
Supervisory Activity Management (SAM) 173
system administrator setup 49
T
terminal locks, clearing 148
Translation Manager (TRMA) 181
TRMA (Translation Manager) 181
U
UOTS (Update Order To Ship Date) 204
Update Order To Ship Date (UOTS) 204
user access, copying 60
user access, restricting 62
users
deactivating 53
giving program access to 54
giving supervisor privileges to 52
reactivating 53
removing program access from 59
resetting passwords for 53
setting up 49
W
WAME (Warnings/Messages) 97
Warnings/Messages (WAME) 97

INDEX
