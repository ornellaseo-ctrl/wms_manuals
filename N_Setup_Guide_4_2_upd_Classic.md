# Manual N — Setup Guide (Guia de Configuração Inicial)

> **ID do Manual:** N  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Configuração inicial do sistema: SKU, documentos, impressoras, armazéns, localizações, clientes, perfis de depositor, tarifas, perfis de item, mensagens. Programas principais: SKCL, SKUS, DONU, PRIN, WARE, LOCA, CUST, RATE, ITEM, DIFP, DSRP, DBIP, DILP, DIAP, ILOP, e dezenas de outros perfis de configuração.

---

AccellosOne Enterprise 
3PL Setup Guide 
(Classic)
May 2016
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

TABLE OF CONTENTS
INTRODUCTION ......................................................................... 1
About This Manual .............................................................................................. 2
Building Your System......................................................................................... 2
Using Profiles ...................................................................................................... 3
Global Versus Unique Programs ....................................................................... 3
Status of Codes and Profiles ............................................................................. 5
Updating Records in the Database.................................................................... 5
AccellosOne 3PL Documentation Set ............................................................... 6
INITIAL SETUP ......................................................................... 7
Before You Begin ................................................................................................ 8
SKU Class (SKCL)............................................................................................. 10
Stock Keeping Units (SKUS)............................................................................ 12
Document Numbers (DONU) ............................................................................ 17
Printer Code (PRIN)........................................................................................... 20
Country Codes (CNTY) ..................................................................................... 24
States/Provinces (STPR) .................................................................................. 29
ZIP/Postal Code (ZIPO) ..................................................................................... 31
WAREHOUSE SETUP .................................................................35
Warehouse & Location Format (WARE).......................................................... 36
Location Billing Codes (LODE)........................................................................ 43
Isolators (ISOL) ................................................................................................. 45
Location Print Profile (LPPR)........................................................................... 51
Location Type (LOTP)....................................................................................... 53
Locations (LOCA).............................................................................................. 59
CUSTOMER SETUP ...................................................................71
Salespersons (SAPE)........................................................................................ 72
Customer Service Representatives (CUSE) ................................................... 73
Flow Process (FLPR) ........................................................................................ 75
Depositor Workflow Profile (DIFP) .................................................................. 78
Number Series (NUSE) ..................................................................................... 86
Depositor Inventory Assign Profile (DIAP) ..................................................... 88
Depositor Level Validation Profile (DLVP)...................................................... 95
Inventory Terminology (INTE).......................................................................... 99
Depositor Inventory Level Profile (DILP) ...................................................... 101
Depositor Item Profile (DITP) ......................................................................... 112
Picking Profile (PIPR) ..................................................................................... 114

ii 4.2* SETUP GUIDE
Depositor Shipping & Receiving Profile (DSRP).......................................... 116
Telephone List Types (TETP)......................................................................... 120
Billing Terms (TERM)...................................................................................... 122
Holidays (HOLI) ............................................................................................... 126
Depositor Billing Profile (DBIP) ..................................................................... 127
Depositor Alternate Sorts (DEAS) ................................................................. 136
Customer Setup (CUST) — Basic .................................................................. 139
Customer Setup (CUST) — Advanced .......................................................... 151
CHARGE AND RATE SETUP ..................................................... 157
General Ledger Chart of Accounts (GLCH) .................................................. 158
Currency Codes (CURR)................................................................................. 160
Bank Code (BANK).......................................................................................... 162
General Ledger Modifier Code (GLMO)......................................................... 164
Revenue Group Codes (REGR)...................................................................... 169
Revenue Analysis Codes (REVA) .................................................................. 170
Invoice Types (INTP)....................................................................................... 173
Charge Codes (CHAR) .................................................................................... 174
Depositor Billing Rates (RATE) ..................................................................... 185
ITEM PROFILE SETUP ............................................................. 193
Item Information Profile (IINP) ....................................................................... 194
Item Initial Storage Profile (IISP).................................................................... 196
Item Renewal Storage Profile (IRSP)............................................................. 201
Item Handling Profile (IHAP) .......................................................................... 208
Date Profile (DAPR)......................................................................................... 210
Item Billing Profile (IBIP) ................................................................................ 212
Item Shipping Profile (ITSH)........................................................................... 217
Item Process Profile (IPRP)............................................................................ 224
Item Quantity Breakdown Profile (IQBP) ...................................................... 226
Item Alternate Sorts (ITAS) ............................................................................ 233
Hold Types (HOLD) ......................................................................................... 237
Hold Shipping Sequence Profile Code (HOSP) ............................................ 241
Item Hold Profile (IHOP) ................................................................................. 244
Item Incubation Hold Code (IIHO).................................................................. 247
Incubation Hold Profile (IIHP) ........................................................................ 249
Freight Class Codes (CLAS) .......................................................................... 252
Commodities (COMM)..................................................................................... 254
Item Location Profile (ILOP)........................................................................... 256
Item Tare Profile (ITAP) .................................................................................. 258

MESSAGE SETUP .................................................................... 263
Messages (MESS) ........................................................................................... 264
Depositor Messages (DEME) ......................................................................... 265
Depositor Print Messages (DPME) ................................................................ 267
Hazardous Material Messages (HAZA).......................................................... 269
Inventory Messages (ADIM) ........................................................................... 272
ITEM SETUP .......................................................................... 275
Item (ITEM)....................................................................................................... 276
MISCELLANEOUS SETUP ......................................................... 311
Adjustment Type Codes (ADJU).................................................................... 312
Load Type (LOAD)........................................................................................... 315
Transport Mode Codes (TRMO) ..................................................................... 318
Carriers (CARR)............................................................................................... 320
Load Analysis (LDAN) .................................................................................... 327
Shippers (SHIP) ............................................................................................... 328
Retail Profiles (RETP) ..................................................................................... 336
Consignees (CONS) ........................................................................................ 338
Sold-To Codes (SOLD) ................................................................................... 347
Drivers (DRIV).................................................................................................. 351
Language Code (LANG).................................................................................. 353
Alternate Item and Language (ALIT) ............................................................. 355
Telephone Numbers (TELE) ........................................................................... 359
INDEX ................................................................................... 363

iv 4.2* SETUP GUIDE

INTRODUCTION
About This Manual .............................................................................................. 2
Building Your System......................................................................................... 2
Using Profiles ...................................................................................................... 3
Global Versus Unique Programs ....................................................................... 3
Status of Codes and Profiles ............................................................................. 5
Updating Records in the Database.................................................................... 5
AccellosOne 3PL Documentation Set ............................................................... 6

INTRODUCTION
About This Manual
About This Manual
This manual provides basic setup instructions for AccellosOne 3PL. It contains all the mandatory programs 
that you need to set up plus the majority of commonly used optional programs. When you finish setup, you 
will be able to receive and ship product and perform most of the commonly used functions in AccellosOne 
3PL.
This manual is divided into eight sections. Because each program or system code builds on previously set up 
codes or programs, it is important to follow the order of programs as they are presented in this manual. If you 
attempt to skip mandatory programs, you will be unable to set up a program or profile presented later in the 
manual. 
▪ INITIAL SETUP (SKU classes and codes, printer codes, etc.)
▪ WAREHOUSE AND LOCATION SETUP (warehouses, locations, isolator zones, etc.)
▪ CUSTOMER PROFILE SETUP (flow steps, inventory levels, billing profiles, customers, etc.)
▪ CHARGE AND RATE SETUP (general ledger information, revenue analysis, charges, rates, etc.)
▪ MESSAGE SETUP (custom messages that can be attached to a customer, item, etc.)
▪ ITEM PROFILE SETUP (initial storage, renewal storage, quantity breakdowns, hold codes, etc.)
▪ ITEM SETUP (the main item record)
▪ MISCELLANEOUS SETUP (carriers, shippers, consignees, telephone numbers, etc.)
Building Your System
System setup in AccellosOne 3PL is a gradual process in which you build your system from the lowest level 
(system codes such as SKU types, billing terms, charge types, flow codes, etc.) to the next level (depositor 
profiles, item profiles, flow profiles, etc.) to the highest level (customers and items), which are the main 
programs in AccellosOne 3PL. 
For example, you have a minimum renewal charge for a particular item in your warehouse. First, you define a 
charge code for your minimum renewal charge in CHAR, next you attach this charge code to your renewal 
storage profile, and then you attach the renewal storage profile to your item billing profile. Lastly, you attach 
the item billing profile to the appropriate item. 
CHAR IRSP IBIP ITEM
Create a charge
code
Attach the charge
code to a renewal
storage billing
profile
Attach the IRSP
billing profile to the
item billing profile
Attach the IBIP
profile to the item

INTRODUCTION
Using Profiles
Using Profiles
AccellosOne 3PL uses profiles to group related information about billing, items, item location, shipping, 
quantity breakdown, etc. A profile is merely a series of options grouped under a profile code. When a given 
profile code is attached to a particular customer or item, all the options of that profile code automatically apply 
to the customer or item. 
Profiles make it easy to change large numbers of customers or items by means of a single change to one 
program. For example, if you set up a standard billing profile for all your customers, you can change your 
billing for all customers by making the change once in the profile rather than individually for each of your 
customers.
Although you can set up as many profiles as you want (for example, a separate profile for each of your 
customers), such an approach is seldom recommended. Generally, you want to minimize the number of your 
profiles as much as possible. If all your customers are billed in the same way, there is no need to set up more 
than one billing profile. 
Global Versus Unique Programs
There are two types of programs in AccellosOne 3PL: global and unique. A global program is a program in 
which once you set up a system code or a profile, it can be shared across companies, warehouses, 
customers, etc. For example, SKUS (Stock Keeping Units) is a global program. If you set up a SKU in this 
program (for example, a SKU called CASES), you can use CASES in any warehouse, company or customer 
on your system. 
ITEM, on the other hand, is a unique program. Items created in ITEM are customer specific; they cannot be 
shared or accessed across companies or other customers.
To share global programs across companies, you must set the Global Code field in COMP (Company Code) 
to the same value for all companies whose codes and profiles you wish to share. For example, if you assign 
the global code of 00 to companies W1 and W2 and assign the global code 01 to companies W3 and W4, 
companies W1 and W2 will share one set of global codes and profiles while companies W3 and W4 will share 
a separate set of global codes and profiles. 
Global Code = 00
COMPANY 1
Global Code = 00
COMPANY 2
Global Code =
COMPANY 3
codes and profiles
shared between
companies
no sharing of codes
and profiles between
companies

INTRODUCTION
Global Versus Unique Programs

Company Code (COMP) screen for company W1 showing Global Code set to 00
 For your test or training company, you should always leave the Global Code field blank so that test codes and 
profiles do not get mixed up with your live customers and items. For your live companies, on the other hand, 
you can assign global codes to them if required so that your live codes and profiles are available for use in 
other live companies.
T1 (Sample Company 1)
Global Code = 00
T2 (Training Company 2)
Global Code = 
W1 (Live Company)
Global Code = 00
EXAMPLE 1
You create a SKU type of CASES in T1 using the program SKUS.
CASES set up in T1 are not available for use in any T2 program 
because global code in T2 does 
not match global code in T1.
CASES set up in T1 are available 
for use in all W1 programs 
because global code in W1 
matches global code in T1.
EXAMPLE 2
You create an isolator code of FISH in T2 using the program ISOL.
FISH set up in T2 are not available for use in any T1 program 
because global code in T2 does 
not match global code in T1.
FISH set up in T2 are not available for use in any W1 program 
because global code in T2 does 
not match global code in W1.

INTRODUCTION
Status of Codes and Profiles
Status of Codes and Profiles
The majority of codes and profiles have a Status field used to indicate their status. There are two possible 
statuses for a code or profile:
▪ Active
▪ Deactivated
You deactivate an active code or profile by clicking on Delete. You activate a deactivated code or profile by 
entering A in the Status field and pressing Enter. You can activate and deactivate the same code as many 
times as you wish.
Updating Records in the Database
When you create or modify a record in any setup program, the changes that you make only take effect when 
you click on Exit to exit the program. If you do not click on Exit to exit the program, other operators on your 
AccellosOne 3PL system will only have access to the old information.
For example, if you make a change to an item description in ITEM but do not click on Exit to exit, any other 
user receiving or shipping the item will receive or ship the item with its old description. 
NOTE Once you assign a global code in COMP to a particular company, you cannot 
change it. Should you make a mistake and need to reset the flag, contact your HighJump 
consultant for assistance.
Active An active code or profile is a normal code or profile that can be used in any 
setup or operational program. For example, an active item can be shipped, 
received and adjusted like normal inventory and can be attached to another 
profile. 
Deactivated A deactivated code or profile can be shipped and adjusted like normal inventory but cannot be received. Nor can it be attached to another profile. For 
example, if you deactivate an item, you cannot receive new inventory for this 
item, but existing inventory remains unchanged and can be shipped and 
adjusted like normal inventory.

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
tracking, tasking, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory 
level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

INITIAL SETUP
Before You Begin ................................................................................................ 8
SKU Class (SKCL)............................................................................................. 10
Stock Keeping Units (SKUS)............................................................................ 12
Document Numbers (DONU) ............................................................................ 17
Country Codes (CNTY) ..................................................................................... 24
States/Provinces (STPR) .................................................................................. 29
ZIP/Postal Code (ZIPO) ..................................................................................... 31

INITIAL SETUP
Before You Begin
Before You Begin
The following codes must be created in AccellosOne 3PL before you can perform setup:
▪ an “NA” (Not Applicable) invoice type in INTP 
▪ a “no charge” type charge code in CHAR
▪ an inventory terminology code of ITEM in INTE
▪ a dummy general ledger account in GLCH
▪ a currency in CURR
▪ a bank code in BANK
▪ six document types in DOTP
The above codes may or may not be available to the company that you are setting up depending on the type 
of company that you are creating (“global” or “unique”) and whether other companies have already been set 
up on your system. 
TO SET UP YOUR INVOICE TYPE:
1 Enter INTP (Invoice Types).
2 Click on Enter Criteria then Execute Query to view your existing invoice types.
3 If there is no invoice type of NA for not applicable, click on Create Record.
4 In the Invoice Type field, key in NA for Not Applicable and press Enter.
5 In the Description field, key in Not Applicable and press Enter.
6 Click on Return to Main and Exit to exit.
TO SET UP YOUR “NO CHARGE” TYPE CHARGE CODE:
1 Enter CHAR (Charge Code).
2 Click on Enter Criteria then Execute Query to view your existing charge codes.
3 If there is no charge code of NC for no charge, click on Create Record.
4 In the Charge Code field, key in NC for No Charge and press Enter.
5 In the Description field, key in No Charge and press Enter.
6 Press Enter twice to bypass the Reference and External Reference fields.
7 In the Charge Type Code field, key in NC and press Enter.
8 In the Invoice Type Code field, use your pick list to select the NA invoice type.
9 Click on Return to Main and Exit to exit.
TO SET UP YOUR INVENTORY TERMINOLOGY CODE:
1 Enter INTE (Inventory Terminology). 
2 Click on Enter Criteria then Execute Query to view your existing inventory terminology codes.
3 If there is no inventory terminology code of ITEM, click on Create Record.
4 In the Code field, key in ITEM and press Enter.
5 In Description field, key in Item and press Enter.

INITIAL SETUP
Before You Begin
6 Press Enter to bypass the RF field.
7 Click on Return to Main and Exit to exit.
TO SET UP A DUMMY GENERAL LEDGER ACCOUNT:
1 Enter GLCH (G. L. Chart of Accounts). 
2 Click on Enter Criteria then Execute Query to view your existing general ledger accounts.
3 If there is no general ledger account, click on Create Record.
4 In the Code field, key in a dummy account number like 999999 or 100000 and press Enter.
5 In Description field, key in your description (“Miscellaneous”) and press Enter.
6 Press Enter twice to bypass the GL External Reference 1/2 fields.
7 Click on Return to Main and Exit to exit.
TO SET UP A CURRENCY:
1 Enter CURR.
2 Click on Enter Criteria then Execute Query to view your existing currencies.
3 If there is no currency set up, click on Create Record.
4 Key in your currency code and press Enter.
5 In the Description field, key in the description for your new currency and press Enter.
6 In the Value to Base Currency field, key in 1 and press Enter.
7 Press Enter to bypass the Realized Exchange G. L. Account field.
8 In the Trade GL Account field, key in the same dummy account that you created in the previous procedure and press Enter. 
9 Press Enter to bypass the remaining fields in CURR.
10 Click on Return to Main and Exit to exit.
TO SET UP A BANK CODE IN BANK:
1 Enter BANK.
2 Click on Enter Criteria then Execute Query to view your existing banks.
3 If there is no bank set up, click on Create Record.
4 Key in NA as your bank code and press Enter.
5 Key in Not Applicable as your description and press Enter.
6 In the Bank Account Number field, key in any number and press Enter.
7 In the Bank G. L. Account field, key in the dummy account number that you created in GLCH and press 
Enter. 
8 In the Currency Code field, key in any valid currency code that you created in CURR and press Enter.
9 When you finish entering your bank code, click on Return to Main and Exit to exit.

INITIAL SETUP
SKU Class (SKCL)
TO SET UP YOUR SIX DOCUMENT TYPES IN DOTP:
1 Enter DOTP (Document Types). 
2 Click on Enter Criteria then Execute Query to view your existing document types. 
3 If there are no document types on your system, you should set up the following types:
AD (Adjustment Audit)
IN (Inbound)
OU (Outbound)
BI (Billing)
PH (Physical)
LA (Label)
4 To set up a document type, click on Create Record.
5 In the Document Type Code field, key in your code and press Enter.
6 In the Description field, key in your description and press Enter.
7 In the Type field, key in the same code that you entered in the Document Type Code field and press 
Enter.
8 Repeat the above steps for each document type that you wish to add.
9 When you finish adding your document types, click on Return to Main and Exit to exit.
SKU Class (SKCL)
OVERVIEW
In this program, you review your SKU classes. SKU classes are required when you define your SKU types in 
SKUS (Stock Keeping Units). 
The purpose of SKU classes is to define the type and relative size of each SKU type. For example, suppose 
you have one SKU type called CARTONS for Customer 1, another SKU type called BOXES for Customer 2 
and a third SKU type called CASES for Customer 3. Because all three SKU types are essentially the same 
thing, you assign them the SKU class of CASE (cases and the like) as a way of grouping them. This allows 
AccellosOne 3PL to differentiate these SKU types from pallets, which would have their own SKU class.
PREREQUISITES: None
ATTACHED TO: SKUS (Stock Keeping Units)
PIPR (Picking Profile)
LOAD (Load Type)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

INITIAL SETUP
SKU Class (SKCL)
SKU classes allow you to define in PIPR (Picking Profile) what constitutes a partial quantity. A partial quantity 
in AccellosOne 3PL is defined as a quantity that is less than a full SKU class and not the highest SKU class. 
For example, if you have a PALLETS/CASES account and your SKU classes are 1 for pallets and 3 for cases, 
then a partial quantity would be any number of cases not making up a full pallet. Partial quantities are used in 
the allocation routine when you specify whether or not you want AccellosOne 3PL to clean up locations 
containing partial quantities.
There are five predefined SKU classes in AccellosOne 3PL. These classes are ranked by size with the largest 
items (usually pallet) being assigned the lowest number. If you wish to change these predefined classes, you 
type over the information that you wish to change.
The sixth SKU class (Other) is used for SKU codes like LBS, KGS, HR and OCCURRENCE, which do not 
have a size.
PROCEDURE
1 Enter SKCL.
SKU Class (SKCL)
2 Review the predefined SKU classes.
FIELD DESCRIPTIONS
Class Number This number is set up by HighJump and cannot be altered. 
Description The long description of the SKU class. You can change the long description by 
keying in a new one over the old one and pressing Enter. 
Short Description The short description of the SKU class. The short description of the SKU class 
appears on certain screens and reports where there is insufficient space to 
show the long description.

INITIAL SETUP
Stock Keeping Units (SKUS)
3 If you wish to change either a long description or short description, press Enter until your cursor is positioned in the field that you wish to change. Then key in a new long or short description and press Enter.
4 When you finish making your changes, click on Exit. If you are in modify record mode, click on Return to 
Main and then Exit.
Stock Keeping Units (SKUS)
OVERVIEW
In this program, you define the SKU codes that you wish to use for tracking product and billing your 
customers. A SKU code is anything in your warehouse that you wish to track and/or charge for. SKU codes 
can be physical objects (such as bags, boxes, cases, units, pallets, drums, etc.), units of measure (such as 
pounds, hundredweights, tonnes, hours, meters, cubic inches, etc.) or a service that you wish to charge for 
(for example, a bill of lading).
There are four main functions in SKUS:
▪ you define the SKU code itself (bags, boxes, pounds, pallets, cases, etc.)
▪ you define how the SKU code is counted (by weight, number of units, etc.)
▪ you define the SKU class (how big is the SKU code compared to other SKU codes)
▪ if you are setting up a multiple SKU such as hundredweight, you must define the “divide by” value (for 
example, 1 hundredweight = 100 pounds) 
You can set up one SKU code for each non-pallet item in your warehouse (for example, bag, box, case, 
carton, etc.) or simply use pallets/cases as the standard quantity breakdown for all your customers. Separate 
SKU codes for each non-pallet item are only required if your customers need their own terminology on 
invoices and reports.
PREREQUISITES: SKCL
ATTACHED TO: CHAR (Charge Codes)
IQBP (Item Quantity Breakdown Profile)
ITEM (Item) 
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all your SKU codes

INITIAL SETUP
Stock Keeping Units (SKUS)
FIELD DESCRIPTIONS
SKU Code Mandatory
Your SKU code. For example, PLT for pallet or CSE for case.
CAUTION: AccellosOne 3PL does not support single-letter SKU codes 
such as C for Case or P for Pallet. Not does it support multi-letter codes in 
which one code can be embedded in another. For example, you cannot have 
CASE for Case and CA for Carton because CA can be embedded in CASE.
Description Mandatory
Your SKU code description. For example, “Pallets.”
Qualifier Code Mandatory
The way in which the SKU code is counted. If the SKU code is a physical 
object (for example, pallet, case, each, drum, bag, etc.), use UNIT. If the SKU 
code is a container that may hold partial quantities (for example, tote), you can 
use either UNIT or WGTG/WGTN. If the SKU code is weight based (for example, pounds, kilos, hundredweights, tons, etc.), use either WGTG or WGTN.
The following qualifier codes are supported in AccellosOne 3PL:
CUBE = Cubic Measure
HOUR = Hour*
OCCR = Occurrence*
UNIT = Unit
WGTG = Gross Weight
WGTN = Net Weight
* See the Billing and Invoicing Guide for further information on using these qualifier 
codes to set up one-time flat rate charges and hourly based charges.

INITIAL SETUP
Stock Keeping Units (SKUS)
PROCEDURE
1 Enter SKUS.
2 Click on Enter Criteria then Execute Query to view your existing SKU codes.
3 Using your arrow keys, go through each record to see which SKU codes have already been set up. If the 
SKU codes that you require have already been set up, click on Exit. There is no need to add any new 
codes to SKUS.
SKU Class Description 
(SKCL)
Mandatory
For SKU codes that are physical objects with a size, use your regular SKU 
classes (Eaches and the like, Cases and the like).
For all other SKU codes (that is, those based on weight, occurrence, hour, etc. 
that do not have a size) use Others. When you assigned a SKU class of Others to a SKU code, you cannot have AccellosOne 3PL pick partial quantities of 
this SKU code in ILOP (Item Location Profile).
Value Mandatory
The value is usually 1 with the following exceptions: 
▪ If you are using the following weight-based SKU Codes — CWT, CKGS, 
MTON and TON — you must specify the appropriate value to convert the 
SKU to either pounds or kilos. For example, for CWT the value will be 100 
and for MTONS (metric tonnes) the value will be 2200.
▪ If you are using cubic inches, enter .000579 as your value.
▪ If you are using kilograms, enter 2.2045855 as your value.
Base SKU Code Optional
Refer to “Billing by Multiple Units of a SKU” in the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

INITIAL SETUP
Stock Keeping Units (SKUS)

SKU Code for cases
4 If the SKU codes that you require have not been set up, click on Create Record.
5 Key in your new SKU code and press Enter.
6 Key in a meaningful description for the new code and press Enter.
7 Key in your qualifier code and press Enter.
To select other qualifier codes, you can use the pick list function. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow 
keys to position your cursor over the appropriate code and click on Select Code.
8 Key in your SKU class description and press Enter. If the SKU code is weight based, use Others as your 
class description.
To select a SKU class description, use your pick list.
For most physical objects: For weight-based SKU’s:
a) Use UNIT. a) Use the appropriate code for 
weight-based SKUS.

INITIAL SETUP
Stock Keeping Units (SKUS)

SKU Code for hundredweight
9 Key in your value and press Enter.
10 When you finish setting up your SKU code, click on Return to Main and then Exit.
For most UNIT-base SKU 
codes:
For weight-based or cube-based 
SKU codes:
a) Use 1 as your value. a) Enter the appropriate value.
CAUTION If you are creating a weight-based SKU code such as CWT, CKGS, 
MTON (metric tonne) or TON, you must have a SKU code on your system for pounds 
(in the case of CWT and TON) and/or kilograms (in the case of CKGS or MTON). If 
you fail to define your pounds or kilos, your system will not be able to rate or bill properly.

INITIAL SETUP
Document Numbers (DONU)
Document Numbers (DONU)
OVERVIEW
In this program, you define the format of your document numbers for each document type set up in AccellosOne 3PL. Accessorial invoice, renewal invoice, order number and receipt number are some of the 
document types that you define in DONU. For each document type you must specify the prefix, starting 
number and ending number of your block of numbers. As an option, you can also define a suffix for your block 
of numbers. 
Once set up, blocks of numbers are final and cannot be changed. You can, however, change the prefix.
PREREQUISITES: None
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE When working with multiple companies, you cannot use the same number 
series and prefix for two or more companies. You must change either the number 
series or the prefix of your block of numbers to accommodate the second company.

INITIAL SETUP
Document Numbers (DONU)
FIELD DESCRIPTIONS
Number Type Description Accessorial Invoice Number
Freight Invoice Number*
Order Number
PO Number
Receipt Number
Rollup Accessorial Number
Renewal Invoice Number
Rollup Renewal Number
Shipment Number*
* Reserved for future use.
Prefix Mandatory
You can use a single letter as your prefix (for example, A for Accessorial, O for 
Order, etc.), the current year or any other series of letters or numbers except 
the dash character (-). If you use the current year as your prefix, you must 
remember to change it every year.
If you are working with multiple companies, you cannot use the same number 
series and prefix for two or more companies. You must change either the number series or the prefix of your block of numbers to accommodate the second 
company.
Current Number Mandatory
Your current number.
Start Number/End Number
Mandatory
The starting and ending number for your block of numbers. When AccellosOne 3PL reaches the end of your block of numbers, it will restart at the 
value that you define in the Start Number field.
NOTE Small ranges (for example, a starting number of 100 and an ending 
number of 200) are not recommended. If you must use a small range, make 
sure that you purge your inventory on a regular basis. If you fail to do so, you 
might have two open receipts with the same receipt number.

INITIAL SETUP
Document Numbers (DONU)
PROCEDURE
1 Enter DONU.
2 If required, click on Detail Block.
3 Key in your prefix and press Enter. You can use a single letter as your prefix (for example, A for Accessorial, O for Order, etc.), the current year or any other series of letters or numbers. If you use the current 
year as your prefix, you should remember to change it every year.
4 Key in your current number (usually 1) and press Enter.
5 Key in your start number (usually 1) and press Enter. Your start number must always be less than or 
equal to your current number.
6 Key in your end number (usually the default of 999999) and press Enter.
7 Key in your suffix and press Enter or press Enter with the field blank for no suffix.
8 Click on Return to Main to return to the main block.
Document Numbers screen
9 To set the number series for another document type, arrow down to the document that you wish to set up 
and click on Detail Block.
10 Repeat steps 3 to 8 for each document type that you wish to set up.
Suffix Optional
Your suffix (up to four characters in length).
FIELD DESCRIPTIONS

INITIAL SETUP
Printer Code (PRIN)
11 When you finish setting up your document types, click on Exit to exit the program. If Exit is not available, 
click on Return to Main and then Exit.
Printer Code (PRIN)
OVERVIEW
In this program, you set up the printers that you will be using in AccellosOne 3PL to print your labels, 
documents, physical inventory tickets, reports, etc. There are seven predefined “printers” set up in AccellosOne 3PL: AFAX, BAR, EXCL, FAX, MAIL, SPL and VIEW. These printers are set up by HighJump and 
cannot be modified or deleted.
Before you set up your printers in AccellosOne 3PL, you must first set up the printers in Unix and use the 
same Unix printer codes in PRIN.
PREREQUISITES: None
ATTACHED TO: LPPR (Location Print Profile) --> (LOCA)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: Your printer code as defined in Unix
FIELD DESCRIPTIONS
Printer Code Mandatory
Your printer code in AccellosOne 3PL. Your AccellosOne 3PL printer code 
need not be the same as your Unix printer code.
Description Mandatory
Your printer code description.
System Printer Code Mandatory
Your printer code as defined in lpstat in Unix for raw drivers.

INITIAL SETUP
Printer Code (PRIN)
System Alternate Printer 
Code
Optional
An alternate system printer code. For example, your print queue for postscript/
PDF outputs.
Printer Size Only available for non-PDF printing
S = Small
R = Regular
If you select S for Small, any document that is wider than 80 characters will be 
compressed. If in fact the document that you are printing is less than 80 characters across, no compression will occur. Therefore, if there is any possibility 
of an item requiring compression, it is recommended that you select the Small 
option.
If you select R for Regular, no compression will occur and the document will 
be printed as is.
Command Type Optional
p = Pipe (sends the print job to a printer)
c = Command (executes a Unix command)
d = Device (data sent to a defined device)
f = Fax (reserved for future use)
e = E-Mail (reserved for future use)
Your command type.
Command Optional
When you output to a printer using the command type of p, there are two command options:
lp -d $sys_prt_code..........................................................output to a printer
dd of=/directorypath/filename .............................................. output to a file
FIELD DESCRIPTIONS

INITIAL SETUP
Printer Code (PRIN)
PROCEDURE
1 Enter PRIN.
2 Click on Enter Criteria then Execute Query to see which printers have already been set up.
Print Profile Code (PRPF) Optional
This code is set up by HighJump. It allows you to print document overlays 
using printer macros.
IP Address / Printer 
Name for BarTender Software
See the Core Documents Guide.
Compress Escape 
Sequence
Optional
You can specify any Unix lp command (for example, use font 123) that is valid 
for the printer that you are printing on.
Reset Escape Sequence Optional
You can specify any Unix lp command (for example, use font 123) that is valid 
for the printer that you are printing on.
Reference IP Address Optional
External information for reporting purposes.
Reference Model 
Description
Optional
External information for reporting purposes.
FIELD DESCRIPTIONS

INITIAL SETUP
Printer Code (PRIN)
Printer Code (PRIN)
3 Using your arrow keys, go through each record to see which printers have already been set up. If the 
printers that you require have already been set up, click on Exit. There is no need to add any new codes 
to PRIN.
4 If the printers that you require have not been set up, click on Create Record.
5 Key in your printer code (up to four alphanumeric characters) and press Enter.
6 Key in a meaningful description for the new code and press Enter.
7 In the System Printer field, key in the name of the printer as defined in lpstat in Unix and press Enter.
8 In the Printer Size field, specify S for Small or R for Regular and press Enter.
9 In the Command Type field, key in p for Pipe, c for Command or d for Device and press Enter.
10 If required, key in your print command and press Enter. If you do not require a print command, press 
Enter to bypass this field.
11 Press Enter to bypass the Print Profile Code field.
12 Press Enter again to bypass the IP Address / Printer Name for BarTender Software field.
13 In the Compress Escape Sequence and Reset Escape Sequence fields, key in your Unix lp option and 
press Enter or press Enter with the field blank to bypass the field. 
14 When you finish setting up your printer, click on Return to Main and Exit to exit the program.

INITIAL SETUP
Country Codes (CNTY)
Country Codes (CNTY)
OVERVIEW
In this program, you set up your country codes. Country codes serve two purposes in AccellosOne 3PL. First, 
they allow you to record the country in which an item was manufactured. Second, they allow you to define the 
format of and the valid characters in your ZIP and postal codes for that country (Classic only).
AccellosOne 3PL supports both fixed length and variable length postal codes. It also supports multiple postal 
code formats when a country is switching from one format to another (for example, the five-digit and nine-digit 
ZIP codes in the US).
You define your postal code by means of “partitions”. A partition is a distinct part of a code that always 
contains a certain character or type of character. For example, if the first character of your code is always a 
letter and the second character is always a number, you would set up two partitions: partition 1 would be 
defined as letters only and partition 2 would be defined as numeric only.
AMERICAN ZIP CODE 
The American five-digit ZIP code is all numeric and consists of a single partition.
EXAMPLES
PREREQUISITES: None
ATTACHED TO: STPR (State(s)/Province(s))
ZIPO (Zip/Postal Codes)
ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
CAUTION Your system contains a country code of UNKN for Unknown Country. 
This code is required for internal system purposes and should never be deleted.
Partition 
Number
Length of 
Partition
Exact 
Length Valid Characters
1 5 Y 0123456789

INITIAL SETUP
Country Codes (CNTY)
02356
68734
CANADIAN POSTAL CODE 
The Canadian postal code is divided into seven fixed-length partitions. The space between the first and last 
three characters is defined as a partition and assigned the ^ character to indicate a blank space.
EXAMPLES
M5A 2V8
H2L 3C9
K7R 6B3
BRITISH POSTCODE 
The British postcode is divided into seven partitions, the last of which is of variable length.
EXAMPLES
Partition 
Number
Length of 
Partition
Exact 
Length Valid Characters
1 1 Y ABCDEFGHJKLMNPQRSTVWXYZ
2 1 Y 0123456789
3 1 Y ABCDEFGHJKLMNPQRSTVWXYZ
4 1 Y^
5 1 Y 0123456789
6 1 Y ABCDEFGHJKLMNPQRSTVWXYZ
7 1 Y 0123456789
Partition 
Number
Length of 
Partition
Exact 
Length Valid Characters
1 1 Y ABCDEFGHJKLMNPQRSTUVWXYZ
2 1 Y ABCDEFGHJKLMNPQRSTUVWXYZ0123456
789
3 1 Y 0123456789
4 1 Y 0123456789^
5 1 Y 0123456789^
6 1 Y ABCDEFGHJKLMNPQRSTUVWXYZ0123456
789
7 2 N ABCDEFGHJKLMNPQRSTUVWXYZ

INITIAL SETUP
Country Codes (CNTY)
MK4 1AR
A18 3QD
AB16 7FK
PARTITION BLOCK
FIELD DESCRIPTIONS
Country Code Mandatory
Your country code.
Name Mandatory
The name of your country.
Breakdown Number Mandatory
If the country has two ZIP or postal code formats (for example, the five-digit 
and nine-digit ZIP code in the US), you must create two breakdowns. If the 
country has a single ZIP or postal code format, create a single breakdown. 
Description Mandatory
Your breakdown description.
FIELD DESCRIPTIONS
Partition Number Mandatory 
If your postal code can be broken down into distinct parts (for example, 
AB1234), you can create multiple partitions and define each partition separately. If your codes are uniform (for example, always numbers), you need 
only define a single partition.

INITIAL SETUP
Country Codes (CNTY)
PROCEDURE
1 Enter CNTY.
2 Click Enter Criteria then Execute Query to retrieve your country codes. When the first country code is displayed, use your down arrow key to see which countries have already been set up.
Length of Partition Mandatory 
The number of characters in the partition that you want AccellosOne 3PL to do 
validation on. If you set the Exact Length field to No, you can create postal 
codes that exceed the Length of Partition value. However, no validation will 
occur on these extra characters.
Exact Length Y = Yes
N = No (only available for last partition in code)
If the partition is always the same length (for example, the first character of 
your code is always a letter), set this flag to Yes. If the partition is not always 
the same length (for example, your code can begin with one or two characters 
that are always a letter), set this flag to No.
If you set this flag to Yes, AccellosOne 3PL will perform validation on all characters in the code. If you set this flag to No, AccellosOne 3PL will perform validation on the number of characters that you entered in the Length of Partition 
field. You can add extra characters to a ZIP or postal code, but no validation 
on these extra characters will be performed.
Valid Characters Mandatory 
The characters that you can use in your ZIP or postal code. Valid characters 
can be numbers, letters or special characters.
FIELD DESCRIPTIONS

INITIAL SETUP
Country Codes (CNTY)
Country Codes screen for the US
3 If the country that you require has not been set up, click on Create Record.
4 Key in your country code (up to four alphanumeric characters) and press Enter.
5 Key in a meaningful description for the new code and press Enter.
6 When the Breakdowns window appears, key in 1 as your breakdown number and press Enter.
7 Key in your breakdown description and press Enter.
8 When the Partitions window appears, key in 1 as your first partition number and press Enter.
9 Key in the length of your partition and press Enter.
10 In the Exact Length field, key in Y for Yes or N for No and press Enter.
11 Key in the valid characters for this partition and press Enter.
12 If required, repeat the above steps for your second partition.
13 When you finish adding your partitions, click on Return to Main.
14 If you wish to create a second breakdown, click on Breakdown Block and then Create Record. Then 
repeat steps 7 to 13 for your second breakdown. If you do not need a second breakdown, click on Return 
to Main and then Exit.

INITIAL SETUP
States/Provinces (STPR)
Country Codes screen for the US
States/Provinces (STPR)
OVERVIEW
In this program, you set up your state and province codes. You use these codes to record the postal address 
of your companies, warehouses, customers, carriers, consignees, shippers and sold-to’s. State and province 
codes print on any AccellosOne 3PL document containing an address.
If you do not need states or provinces for a county because the country does not have them or they are 
unimportant to your business, create a single code like OS for Overseas.
PREREQUISITES: None
ATTACHED TO: ZIPO (Zip/Postal Codes)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

INITIAL SETUP
States/Provinces (STPR)
PROCEDURE
1 Enter STPR.
2 Click on Enter Criteria then Execute Query to retrieve your state and province codes. When the 
first code is displayed, use your down arrow key to see which states and provinces have already been 
set up.
3 If you need to set up another code, click on New.
State(s)/Province(s)
4 If the state or province that you require has not been set up, click on New.
5 Key in your state or province code (up to four alphanumeric characters) and press Enter.
FIELD DESCRIPTIONS
State or Province Mandatory
Your state or province code.
Country Code (CNTY) Mandatory
Your state or province’s country code.
Description Mandatory
The name of your state or province.

INITIAL SETUP
ZIP/Postal Code (ZIPO)
6 Select your country from the dropdown list.
7 Key in a description for your state or province code and press Enter.
8 Repeat steps 5, 6 and 7 for each additional state or province that you wish to add.
9 When you finish adding your states and provinces, click on Save to save your changes.
10 Click on Exit to exit the program.
ZIP/Postal Code (ZIPO)
OVERVIEW
In this program, you set up your ZIP and postal codes. ZIP and postal codes are a mandatory field in all 
AccellosOne 3PL programs with an address such as WARE, CUST, CARR, etc. In ZIPO you attach your ZIP 
or postal codes to the city and state or province to which they belong. Because ZIP and postal codes are 
always linked to the appropriate city and state/province, you can enter the ZIP code of a customer in CUST 
and the city and state fields are automatically filled in by AccellosOne 3PL based on the information that you 
set up in ZIPO.
PREREQUISITES: CNTY, STPR
ATTACHED TO: WARE (Warehouse & Location Format)
CUST (Customer Code)
CONS (Consignees)
CARR (Carriers)
SHIP (Shippers)
SOLD (Sold-To Codes)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Country Code Mandatory
Your country code.

INITIAL SETUP
ZIP/Postal Code (ZIPO)
PROCEDURE
1 Enter ZIPO.
2 Click on Enter Criteria then Execute Query to retrieve all your ZIP/postal codes. To look up a specific 
code, first click Enter Criteria. Then key in your country code and press Enter. Lastly, key in your ZIP/
postal code and click Execute Query. 
ZIP/Postal Code
3 If the ZIP or postal code that you require has not been set up, click on Create Record.
4 Key in your country code and press Enter.
5 Key in your ZIP or postal code and press Enter.
6 Key in the city or town that the code corresponds to and press Enter.
7 Key in your state or province code and press Enter.
8 Repeat steps 3 to 7 for each additional code that you wish to add.
ZIP/Postal Code Mandatory
Your ZIP or postal code.
City Mandatory
The city or town corresponding to the ZIP/postal code.
State or Province Mandatory
The state or province of the ZIP/postal code.
FIELD DESCRIPTIONS

INITIAL SETUP
ZIP/Postal Code (ZIPO)
9 When you finish adding your ZIP or postal codes, click on Return to Main and then Exit.

INITIAL SETUP
ZIP/Postal Code (ZIPO)

WAREHOUSE SETUP
Warehouse & Location Format (WARE).......................................................... 36
Location Billing Codes (LODE)........................................................................ 43
Isolators (ISOL) ................................................................................................. 45
Location Print Profile (LPPR)........................................................................... 51
Location Type (LOTP)....................................................................................... 53
Locations (LOCA).............................................................................................. 59

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
Warehouse & Location Format (WARE)
OVERVIEW
In this program, you set up your warehouse (a warehouse code plus the address) as well as the format of 
your locations in that warehouse (the number of characters in the location code and the format of each 
character — letter, number, special character, etc.). 
A warehouse is a logical entity containing locations for the receiving, storage, picking and shipping of product. 
A warehouse can correspond to a single physical building and contain all of the locations in that building. 
Alternatively, a warehouse can correspond to a room, floor or special area within the same building and 
contain all of the locations within that part of the building. Multiple warehouses in the same building are 
recommended when you wish to generate reports showing the availability of product by room or area, which 
parts of your warehouse are full, etc.
PREREQUISITES: CNTY, ZIPO, STPR
ATTACHED TO: LOCA (Locations)
ILOP (Item Location Profile)
WHZO (Warehouse Zone Codes)
ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The address of the warehouse and the format of its locations
FIELD DESCRIPTIONS
Warehouse Code Mandatory
Your warehouse code. For example, W1 for warehouse 1. A warehouse code 
can consist of any combination of numbers or letters up to four characters in 
length. The single quote (’) and double quote (“) special characters are not 
valid and should never be used. Special characters such as “&”, “%” and “_” 
may cause problems in certain programs and are not recommended. Other 
special characters are generally supported.
Description Mandatory
Your warehouse code description.

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
Address 1/2/3/4 Mandatory
The address of the warehouse.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (ZIP/Postal Code), the city, state/province and 
country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO. 
State Defined in STPR.
Country Code Defined in CNTY.
Length of Location Code Mandatory
The length of the location code for this warehouse.
Fax Cover Sheet (FXCS) Optional
Only required for faxing and auto-printing.
Building Code (BLDG) Optional
Only required for the appointment system and outbound load building.
Directed Move Profile 
Code (DMPA)
Optional
Only required for the directed move system.
Warehouse Labor Capture Flag
Reserved for future use
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
External Reference Number
Optional
You can add any miscellaneous reference information about a warehouse in 
this field.
Establishment Number Reserved for future use
Country Code - Origin Reserved for future use
Location Codes Must 
Conform to Location Definition
Y = Yes
N = No
If you select Yes, locations created in LOCA must follow the format set up in 
the Location Definition Block for that warehouse. If you select No, you can 
override the format set up in the Location Definition Block for that warehouse.
Default Location Code 
(LOCA)
If you create a new location in ENRE, it will inherit the properties of the location code that you enter in this field.
Voice Check Digit Usage See the section on Voice Activated Picking and Order Assignment System in 
the RF Guide.
Days of the Week for 
Check Digit 1/2/3
See the section on Voice Activated Picking and Order Assignment System in 
the RF Guide.
LOCATION DEFINITION BLOCK
Character Position Mandatory
The position of the character whose valid characters you are defining.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
PROCEDURE
1 Enter WARE.
2 Key in your warehouse code (for example, W1) and press Enter.
3 Key in the name and address of the warehouse, pressing Enter at the end of each line.
4 In the ZIP Code field, key in the warehouse’s ZIP code and press Enter. 
If the code that you enter is new and not yet on the system, your cursor will not advance to the next field 
and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and 
press Enter. You will be brought back into WARE with the appropriate information filled in.
5 In the Length of Location Code field, key in the exact number of characters used in your warehouse’s 
locations and press Enter. For example, if the locations in your warehouse are set up as 1A123B, you 
would key in a field length of 6. If, on the other hand, the locations in your warehouse are set up as 
1A123, you would key in a field length of 5.
Valid Characters Mandatory
The valid characters for this character position. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain 
programs and are not recommended. Other special characters are generally 
supported.
LOCATION DEFINITION BLOCK

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
Warehouse and Location Format
6 Press Enter to bypass the Fax Cover Sheet field.
7 Press Enter twice to bypass the Building Code and Directed Move Profile Code fields.
8 Key in N for No in the Warehouse Labor Capture Flag and press Enter.
9 Press Enter to bypass the Labor Standard Modifier field.
10 If required, key in your external reference number and press Enter or press Enter with the field blank to 
bypass the External Reference Number field.
11 Press Enter the required number of times to bypass the remaining fields in WARE.
12 When the Location Definition Block is displayed, enter the valid characters for each character in your 
location. You press Enter at the end of each line to advance the cursor to the next line.

WAREHOUSE SETUP
Warehouse & Location Format (WARE)

Location Definition Block with six characters
The above sample screen illustrates the following: 
Some valid locations based on the above definition are:
0AB-A8
8Z9-DC
If you tried to enter the code 0AB-A in LOCA (the program where location codes are set up), it would be 
rejected because it is only five characters long and this warehouse requires a six-character code. If you 
tried to enter AZ9-DC, it would be rejected because the first character is a letter and you have defined the 
first character as a number.
13 When you finish defining your locations, click on Master Block then Exit to exit the program.
CHARACTER 
POSITION VALID CHARACTERS
1 0-9 or any number
2 A-Z or any letter
3 0-9 + A-Z any number or letter
4 only the special character “-”
5 only the letters A, B, C, D, E and K
6 only 8 and C

WAREHOUSE SETUP
Warehouse & Location Format (WARE)
LOCATION ATTRIBUTES BLOCK
In this block, you define the aisles, bays and odd/even positions of your warehouse. You define aisles, bays 
and odd/even positions by specifying which character(s) in your location codes define an aisle, bay or odd/
even position. For example, if your location codes are four characters in length and the first character 
indicates the aisle, locations A100, A101 and A200 will be considered part of aisle A, while locations B100, 
B101 and B110 will be considered part of aisle B.
FIELD DESCRIPTIONS
Location Attribute Code Mandatory
AISL = Aisle
BAY = Bay (= one side of an aisle)
ODEV = Odd/Even position
Aisles are a requirement for RF interleaving in the program RFITLV. BAY and 
ODEV are requirements for certain display and order by options in the report 
LOCT (Location With Item Description Report).
Start Position Mandatory
The starting position for your aisle, bay or odd/even position. For odd/even 
positions, the starting position must be numeric.
End Position Mandatory
The ending position for your aisle, bay or odd/even position. For odd/even 
positions, the ending position must be the same as the starting position.

WAREHOUSE SETUP
Location Billing Codes (LODE)
WARE screen showing aisle defined as first character in location code and odd/even position defined 
as fourth character of location code
Location Billing Codes (LODE)
OVERVIEW
In this program, you set up your location billing codes. Location billing codes are a means of grouping your 
warehouse locations for billing and revenue analysis purposes.
For example, you can set up location billing codes for all locations, dry storage, the cooler area, etc. By 
setting up these codes, you can set different rates of storage for different areas in your warehouse and you 
can track the revenue generated by each of these storage areas.
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
IISP (Item Initial Storage Profile) --> ITEM
IRSP (Item Renewal Storage Profile) --> ITEM 
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you wish to make changes to a location billing code after attaching the 
code to locations in LOCA, you must run ADLB (Adjust Location Bill 
Code). You cannot modify a location billing code in LOCA. 
See the System Administration Guide for further instructions on using 
ADLB.
OTHER REQUIREMENTS: A list of the different storage areas in your warehouse

WAREHOUSE SETUP
Location Billing Codes (LODE)
In the program LOCA, each location billing code is attached to the specific location that it represents and any 
product stored in these areas will be billed accordingly.
EXAMPLE
Product stored in the cooler area such as film is charged $4.00 per case
Product stored in a high value area is charged $3.75 per case
Product stored in the general warehouse area is charged $3.00 per case
If you do not charge different storage rates based on the area in which the product is placed and do not track 
revenue by area, you do not need location billing codes.
FIELD DESCRIPTIONS
Code Mandatory
Your location billing code. For example, DRY for dry.
Description Mandatory
Your billing code description.
Renewal Calc. by OPID See the Billing and Invoicing Guide.
ITEM
IISP
LODE
When the location billing code of the
item matches the location billing
code of the location, the item is billed
the appropriate initial and renewal
storage rates.
IRSP
LODE
LOCA
LODE
item being putaway into location
IBIP
CHAR CHAR

WAREHOUSE SETUP
Isolators (ISOL)
PROCEDURE
1 Enter LODE.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
Location Billing Codes
3 If you need to set up another code, click on Create Record.
4 Key in your code (for example, DRY) and press Enter.
5 Key in a description and press Enter.
6 Press Enter to bypass the G. L. Modifier Code field.
Refer to the program “General Ledger Modifier Code (GLMO)” on page 164 for further information on 
general ledger modifiers.
7 Repeat steps 4 to 6 for your next location billing code or click on Return to Main and then Exit.
Isolators (ISOL)
G. L. Modifier
(defined in GLMO)
Optional
Refer to the program GLMO in Part 4 of this manual for information on general 
ledger modifiers.
Description Defined in GLMO.
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
ILOP (Item Location Profile) --> ITEM
PUPR (Put-Away Profile Code) --> DSRP 
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Isolators (ISOL)
OVERVIEW
In this program, you set up your isolator zones. Isolator zones serve two key functions:
▪ They allow you to keep certain products separate from each other within the same area. For example, 
you keep both fish and cheese in your cooler area but for obvious reasons you do not want both products sitting side by side in the same location or adjacent locations. Isolator zones allow you to keep both 
products separate from each other.
▪ They allow you to keep similar product together. When similar product is kept together, you avoid a situation where product is dispersed in numerous locations in your warehouse and as a consequence is 
time-consuming and expensive to pick.
You attach isolator zone codes to your locations in the program LOCA (Locations) and to your products in the 
program ILOP (Item Location Profile).
ISOL is intended for systems set up with directed put-away. If you are performing your put-away manually, 
you do not need isolator zones and should set up one isolator on your system called N/A (Not Applicable).
ISSUES TO CONSIDER WHEN SETTING UP ISOLATORS
Before setting up your isolator zones, you should give serious thought to how you want to divide up the space 
in any given area of your warehouse. For example, you can break up an area by customer:
▪ Customer A
▪ Customer B
▪ All others
In this example, you have two major customers (Customer A and Customer B) and you wish to keep their 
products in separate areas of the warehouse. Your other customers are not major and you don’t care whether 
their products are all mixed up together.
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You must know which items or customers you wish to keep separate and 
how you want to define your overflow areas
location 1
fish
location 4
fish
location 7
cheese
location 10
cheese
location 13
other 
products
location 16
other 
products
location 2
fish
location 5
fish
location 8
cheese
location 11
cheese
location 14
other 
products
location 17
other 
products
location 3
fish
location 6
fish
location 9
cheese
location 12
cheese
location 15
other 
products
location 18
other 
products
Isolator 1 Isolator 2 Isolator 3

WAREHOUSE SETUP
Isolators (ISOL)
You could also break up an area in your warehouse by product:
▪ Chemicals/Hazardous Goods
▪ Food Stuffs
▪ Other
This example illustrates a scenario whereby you wish to group certain products together regardless of the 
customer to whom they belong.
You could also break up an area in your warehouse by how fast a product moves:
▪ Fast-Moving Items
▪ Medium-Moving Items
▪ Slow-Moving Items
Three isolator zones for meat: fast-moving, medium moving and slow-moving
OVERFLOW ISOLATORS
Isolator zones can also have one or more designated overflow isolators assigned to them. When you receive 
product and all locations in the isolator zone for that product are full, AccellosOne 3PL will allocate the 
product to the first overflow isolator. If the first overflow isolator is full, AccellosOne 3PL will attempt to allocate 
product to the second overflow isolator (if any). You can define multiple overflow isolators for the same item 
and specify the sequence in which AccellosOne 3PL will query isolator zones in search of empty locations. 
location 1
meat fast-moving
location 4
meat medium-moving
location 7
meat slow-moving
location 2
meat fast-moving
location 5
meat medium-moving
location 8
meat slow-moving
location 3
meat fast-moving
location 6
meat medium-moving
location 9
meat slow-moving
Isolator 1 Isolator 2 Isolator 3

WAREHOUSE SETUP
Isolators (ISOL)
Three isolator zones for meat that progressively overflow into the fourth zone (Meat Overflow)
When the last overflow zone is filled, AccellosOne 3PL will prompt you to enter a location manually.
The number of isolator zones to set up will depend on the layout of your warehouse, the number of customers 
and items, the extent to which product must be kept separate and the types of overflow that you allow. It is 
necessary to strike a balance between too few isolators (AccellosOne 3PL has to search a large number of 
locations in directed put-away and consequently performance is poor) and too many isolators (similar product 
is unnecessarily separated into narrowly defined categories that are overly specific). 
ISOLATORS AND ILOP
The following graphic shows how AccellosOne 3PL uses isolators and ILOP parameters to assign locations to 
product.
location 1
meat fast-moving
location 4
meat medium-moving
location 7
meat slow-moving
location 10
meat overflow
location 2
meat fast-moving
location 5
meat medium-moving
location 8
meat slow-moving
location 11
meat overflow
location 3
meat fast-moving
location 6
meat medium-moving
location 9
meat slow-moving
location 12
meat overflow
Isolator 1 Isolator 2 Isolator 3 Isolator 4
NOTE When two products with different isolator zones are assigned the same 
overflow location, the products may be stored in the same location and you lose the 
benefit of isolator zones. Therefore, if two products should never mix, you must set up 
separate overflow zones for each one.
OVERFLOW OVERFLOW OVERFLOW

WAREHOUSE SETUP
Isolators (ISOL)
PROCEDURE
1 Enter ISOL.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
FIELD DESCRIPTIONS
Isolator Code Mandatory
Your isolator code. For example, MTF for meat fast moving.
Description Mandatory
Your isolator code description.
Overflow Sequence Number
Optional
The sequence of the overflow isolator code.
Overflow Isolator Code Optional
The overflow isolator code.
ITEM
ILOP
ISOL
Depending on your parameters defined in
ILOP, AccellosOne 3PL will ignore, use an
exact match or use an overflow isolator
when picking or putting away product.
LOCA
ISOL
item being put-away
into or picked from
location

WAREHOUSE SETUP
Isolators (ISOL)
3 If you need to set up another code, click on New.
4 Key in your isolator code and press Enter.
5 Key in a description for your code and press Enter.
6 Do one of the following:
7 Click in the Overflow Sequence field.
8 Key in your sequence number (1) and press Enter.
9 Key in your isolator code for sequence number 1 and press Enter.
10 Repeat the above three steps for each additional overflow area that you wish to add. Each additional 
overflow area must be assigned the next available sequence number.
Isolator MT1 with three overflow areas assigned to it
11 When you finish adding your overflow sequences, click on Save to save your new isolator.
12 Key in another isolator code and repeat the above steps or click on Exit twice to exit the program.
HAZARD CLASS TAB
In this tab, you set up your hazardous class restrictions. That is, which hazardous classes cannot be mixed 
together. 
When you put-away, relocate or adjust product into a location and the location’s hazardous class restrictions 
match the item’s hazardous class (for example, explosives 1.1 is mixed with explosives 1.2), AccellosOne 
If you wish to assign an overflow 
area to the isolator:
If you do NOT wish to assign an 
overflow area to the isolator:
a) Proceed to next step. a) Click on Save to save your 
new isolator.
b) Click on Exit to exit ISOL.

WAREHOUSE SETUP
Location Print Profile (LPPR)
3PL will write a record to the hazardous restriction violation table in the database. Using d’Amigo, you can run 
queries and generate alerts to report on these violations.
Isolator A with three records in the Hazard Block
Location Print Profile (LPPR)
OVERVIEW
This program allows you to “split” certain documents among two or more printers based on the location of the 
item. For example, if your warehouse has three different printers at different doors and you are processing an 
PREREQUISITES: DOCU (set up by HighJump), PRIN
ATTACHED TO: LOCA (Locations)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A list of all printers in your warehouse and the documents that can be 
“split” among these printers

WAREHOUSE SETUP
Location Print Profile (LPPR)
order, LPPR allows you to print three separate pick documents at three different printers so that documents 
are always printed on the closest printer.
If you do not need to split documents among two or more printers, you do not use this program.
You need to set up one print profile for each printer that is to accept split documents. Each profile should 
contain the document code for all documents that you want to print on that printer. When you finish setting up 
your location print profiles, you attach them to the appropriate locations in the program LOCA (Locations).
PROCEDURE
1 Enter LPPR.
2 Click on Enter Criteria then Execute Query to see which profiles have already been set up.
3 If you need to set up another profile, click on Create Record.
4 Key in your location print profile code for your first printer and press Enter.
5 Key in a description (for example, Door 3) and press Enter.
NOTE If you are splitting your pick document into different documents, make sure 
that the document is set up to print a message telling the warehouse person that 
another pick must be performed to complete the order.
FIELD DESCRIPTIONS
Location Print Profile 
Code
Mandatory
Your location print profile code.
Description Mandatory
Your location print profile code description.
Document Code
(defined in DOCU)
Mandatory
The document that you wish to print.
Printer Code 
(defined in PRIN)
Mandatory
The printer on which you wish to print the document.

WAREHOUSE SETUP
Location Type (LOTP)
Location Print Profile showing two documents to print on printer P1
6 In the Document Block, key in your document code and press Enter.
7 Key in your printer code for this location and press Enter.
8 Repeat steps 6 and 7 for each additional document that you wish to “split” based on location.
9 Repeat the above steps for your second location print profile. If you have a third printer in your warehouse, set up a third location print profile.
10 When you finish setting up all your profiles, click on Return to Main to exit create mode.
11 Click on Exit to exit the program.
Location Type (LOTP)
OVERVIEW
In this program, you define your location types (BULK, RACK, COOLER, PICK, DRY, etc.). Location types are 
attached to locations in the program LOCA (Locations). There are four types of locations that you can set up 
in LOTP:
▪ a regular rack location (that is, neither pick line nor staging)
▪ a pick line location (pick lines are set up in PIIT)
▪ a staging location
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of your location types

WAREHOUSE SETUP
Location Type (LOTP)
▪ a reserved area for partial pallets
A staging location is a temporary storage area for inbound or outbound product that has not been counted or 
confirmed. A typical staging area would be a dock or a door. When you receive the product in ENRE or 
through an EDI program, you assign it to a staging location. Once you confirm the receipt, the allocation 
routine will assign a regular location to the product.
For each location type that you set up in LOTP, you specify the following:
▪ whether or not you want the allocation routine to assign locations for inbound product
▪ whether or not you want the allocation routine to assign locations for outbound product
▪ which location type you want the allocation routine to pick from first, which location type you want the 
allocation routine to pick from second, third, etc., (outbound product only)
NOTE Do not confuse location types with isolator zones. Location types correspond to different physical areas within your warehouse (BULK, RACK, PICK, etc.). 
Isolator zones, on the other hand, are artificially created entities within the same area 
(for example, CUSTOMER A/CUSTOMER B or FAST-MOVING MEAT/SLOW-MOVING MEAT) whose purpose is to keep similar product together and hence improve the 
efficiency of directed put-away and picking.
FIELD DESCRIPTIONS
Location Type Mandatory
Your location type code. For example, OPEN for Open Area.
Description Mandatory
Your location type description.

WAREHOUSE SETUP
Location Type (LOTP)
Sequence Mandatory
The allocation routine will pick from location types based on the sequence 
number with lower numbers having a higher priority. Sequence number logic 
is only activated after all other factors have been evaluated. For example, if 
you are picking to clean and you set your BULK type to 1 and your RACK type 
to 3, the following will occur. Should the allocation routine select two locations 
with the same product and the same quantity, the location with the location 
type of BULK will be picked first then the location with the location type of 
RACK. 
If you do not want to sequence your location types, set the sequence number 
to 5 for all location types.
NOTE The Sequence field is ignored for directed put-away.
Not to Mix Inventory at 
Level
If you select an inventory level in this field, allocation will not mix inventory at 
the level that you specify. For example, if you select level 2 (lot), allocation will 
not put-away two different lots in the same location. This field applies to putaway, relocate and replenishment.
Enable Location Aliases See “Location Aliases” on page 66.
Suppress Inventory 
Merge to Location
Y = Yes
N = No
If you set this flag to Yes for your pick line location type, inventory merging of 
the lowest inventory level with the pick line location code will be disabled during replenishments and relocations. That is, if you replenish item AB, lot 123, 
PID 001 to pick line location A00L, the PID will NOT change from 001 to A00L.
The Yes option will override your inventory merge settings in ITEM.
Directed Put-Away Y = Yes
N = No
If you specify Yes, the allocation routine will put product away in this location 
type. If you specify No, the allocation routine will bypass this location type 
when putting way product.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Location Type (LOTP)
Directed Picking Y = Yes
N = No
If you specify Yes, the allocation routine will pick from this location type. If you 
specify No, the allocation routine will bypass this location type when picking 
product.
Pick Line N = No
Y = Yes
If the location type is a pick line, set this flag to Yes.
Priority Picking N = No
Y = Yes
If you select this option, allocation will always pick from these locations first 
regardless of your FIFO/LIFO rules. Priority pick locations are typically used 
for product with a high volume of each picks for a particular item. Priority picking is only available for orders assigned to waves in Wave Manager.
Reserve for Partial Pallet N = No
Y = Yes
If you set this flag to Yes for a given location type, you can define a reserved 
area for partial pallets. When receiving partial pallets in RFCH/RFPU, directed 
put-away will select locations in this reserved area.
Partial pallet put-away to a reserved area must be activated in the Put-Away 
Partial Pallet to Reserved Area field in MRFP.
Staging N = No
Y = Yes
If the location type is a staging area, set this flag to Yes. 
Staging Type Pick and Drop
Wrapper
The type of staging area. If you leave this field blank, the staging area will be 
considered a general staging area located on the dock.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Location Type (LOTP)
PROCEDURE
1 Enter LOTP.
2 Click on Enter Criteria then Execute Query to see which location types have been already set up. 
Allow Picking in Staging 
Location
N = No
Y = Yes
If you set this flag to N for No, you cannot pick product in an RF program from 
a staging location. If you set this flag to Y for Yes, you can pick product from a 
staging location in an RF program. 
Disable Three-Step PutAwayN = No
Y = Yes
If you set this flag to Yes for a given location type, you can disable three-step 
put-away for that location type even though it is defined as a default in MRFP 
in the Special Receiving Mode Types field (options 2 and 3).
Weight Restriction ValidationReserved for future use
Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
Exclude from RFPIC Pick 
List
N = No
Y = Yes
If you select No, locations belonging to this location type will not be excluded 
from the RFPIC pick list. If you select Yes, locations belonging to this location 
type will be excluded from the RF pick list; for example, order lines that are to 
be voice picked should not appear in RFPIC pick list.
Enable Pallet Attribute N = No
Y = Yes
The Yes option is only required if you put-away product by inventory attribute 
(INAT).
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Location Type (LOTP)
LOTP screen showing a location type of RACK
3 If you need to set up another type, click on Create Record.
4 Key in your location type code and press Enter.
5 Key in a description for your code and press Enter.
6 In the Sequence field, key in your sequence number and press Enter.
7 In the Not to Mix Inventory at Level field, key in Y for Yes or N for No and press Enter.
8 In the Enable Location Aliases field, key in Y for Yes or N for No and press Enter.
9 In the Suppress Inventory Merged to Location field, key in Y for Yes or N for No and press Enter.
10 In the Directed Put-Away field, key in Y for Yes or N for No and press Enter.
11 In the Directed Picking field, key in Y for Yes or N for No and press Enter.
12 In the Pick Line field, key in Y for Yes or N for No and press Enter.
13 In the Priority Picking field, key in Y for Yes or N for No and press Enter.
14 In the Reserve for Partial Pallet field, key in Y for Yes or N for No and press Enter.
15 In the Staging field, key in Y for Yes or N for No and press Enter.
16 In the Allow Picking in Staging Location field, key in Y for Yes or N for No and press Enter.
17 In the Disable 3 Step Put-Away field, key in Y for Yes or N for No and press Enter.
18 Press Enter twice to bypass the Weight Restriction Validation and Labor Standard Modifier fields.
19 In the Exclude From RFPIC Pick List field, key in Y for Yes or N for No and press Enter.
20 In the Enable Pallet Attribute field, key in Y for Yes or N for No and press Enter.
21 When you finish creating your location type, click on Return to Main and then Exit to exit the program.

WAREHOUSE SETUP
Locations (LOCA)
Locations (LOCA)
OVERVIEW
In this program, you set up the locations in your warehouse. You can define your locations in AccellosOne 
3PL in any way that you choose — a location can be the floor space to hold a single pallet or it can be an 
entire area of your warehouse. You can also set up a dock area or door as a location. The way in which you 
define your locations in AccellosOne 3PL depends on a number of factors including the racking in your 
warehouse and the type and variety of product that you store. Generally speaking, small well-defined 
locations are recommended to take full advantage of AccellosOne 3PL’s active locator system.
The following examples show how locations might be defined in a typical warehouse. If your warehouse has 
special needs, you may wish to define your locations differently.
There are two types of locations in AccellosOne 3PL:
▪ STIC = Static/Stationary Locations
PREREQUISITES: WARE, LODE, ISOL, LPPR, LOTP
ATTACHED TO: ILOP (Item Location Profile)
WHZO (Warehouse Zone Codes)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
Single face Define one location
Double deep Define one location
Drive-thru Define two locations (pallets 1 to 3, 4 to 5)
Drive-in Define one location
Bins Define three locations (one per bin)
Bulk area Define one location

WAREHOUSE SETUP
Locations (LOCA)
▪ MHE = Material Handling Equipment Locations
A static/stationary location is a standard rack or floor area that cannot be moved. An MHE (material handling 
equipment) location is a forklift, truck, pallet jack or other type of vehicle or equipment that may hold product 
for a brief period of time but is not considered a permanent location.
DEFINING THE SIZE/MAXIMUM CAPACITY OF A LOCATION
One of the most important functions in LOCA is the different options for defining the size/maximum capacity of 
a location. The size/maximum capacity of a location in AccellosOne 3PL serves two functions: it is used in 
directed put-away to tell AccellosOne 3PL when a particular location is full and it is needed in the Location 
Analysis Report (LOAN) to identify the amount of space occupied for each location.
There are four ways of specifying the size/maximum capacity of a location in AccellosOne 3PL:
SETTING UP A NEW LOCATION
When you set up a new location in LOCA, the following information is required:
▪ the warehouse to which the location belongs
▪ a code for the location
▪ the location bill code for the location (set up in LODE)
▪ the height, width and length of the location
▪ the location structure type (that is, a standard rack or floor location that cannot be moved or a piece of 
movable equipment such as a forklift or pallet jack)
▪ the location type (set up in LOTP)
▪ the isolator code (set up in ISOL)
linear measurements 
(cube)
You can specify the linear measurements for the location (height, width and 
length) and AccellosOne 3PL will calculate the cube for you automatically.
maximum capacity If you receive standard pallet sizes, you can defined the maximum number of 
pallets, cases or eaches per location.
location size code If you receive non-standard pallet sizes, you can assign location size codes to 
each location line in ENRE. See Allocation and Wave Manager for further 
information.
weight You can define a maximum weight for a location or range of locations.
NOTE If you use more than one method for calculating the size/maximum capacity of location (for example, a maximum cube, a maximum number of SKU’s and a maximum weight), all 
conditions must be satisfied before directed put-away will select the location.

WAREHOUSE SETUP
Locations (LOCA)
▪ the maximum SKU capacity
FIELD DESCRIPTIONS
Warehouse Code
 (defined in WARE)
Mandatory
The warehouse to which the location belongs.
Location Code Mandatory
Your code for this location. The code that you enter in this field must match the 
format that you defined in the Format Block of WARE.
Description Optional
A meaningful description for this location.
Location Bill Code 
(LODE)
Mandatory
The location bill code for the location (that is, how the product in this location 
will be billed). You cannot change the location bill code for a location in modify 
mode. If you wish to change the location bill code for an existing location, you 
must do so in ADLB (Adjust Location Bill Code). See the System Administration Guide for further instructions.
Location Print Profile 
Code (LPPR)
Optional
Only used if you are “splitting” your documents among two or more printers.
Linear Measurement 
Code
Mandatory
CM = Centimeters
FT = Feet
IN = Inches
KM = Kilometers
M = Meters
MILE = Miles
The unit of measure for the height, width and length of the location.

WAREHOUSE SETUP
Locations (LOCA)
Height Mandatory
The height of the location.
Width Mandatory
The width of the location.
Length Mandatory
The length of the location.
Weight Measure Code Mandatory
The unit of measure (pounds, kilograms, tonnes, etc.) you wish to use to 
record the weight limit of this location. You use the weight limit of a location in 
directed put-away/moves if you want AccellosOne 3PL to check the weight of 
product against the weight limit of a location.
This function requires further setup in ILOP (Item Location Profile).
Weight Limit Mandatory
The weight limit of the location. If you do not want AccellosOne 3PL to check 
the weight limit of a location during directed put-away, enter a weight of 0.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Locations (LOCA)
Master Location for 
Weight
Optional
If you have a weight limit for an entire aisle or rack, you must specify a master 
location for weight and link each location to the master location.
For example, suppose you have three locations — A101, A102 and A103 — 
and each location has a weight limit of 100 pounds. If you specify a master 
location, the weight limit will apply to all three locations. For example, you 
could have 100 lbs. in one location and zero in the other two, you could have 
33 lbs. in each location or you could have any other weight combination that 
did not exceed the overall total of 100 lbs.
If you do not specify a master location for weight, the 100 lbs. limit applies to 
each location.
SAMPLE SETUP
You have three locations — A101, A102 and A103 — and a total weight for the 
rack of 100 pounds. For your A101 location, set you weight limit to 100 lbs. 
and leave the Master Location for Weight field blank. For locations A102 and 
A103, set the weight limit to 0 and set the Master Location for Weight to A101.
Vertical Height Factor 
Code
Only available for RF interleaving
The vertical height of the location.
Location Structure Type 
Code
MHE = MHE (Material Handling Equipment) Locations
STIC = Static/Stationary Locations
An MHE (material handling equipment) location is a forklift, truck, pallet jack or 
other type of vehicle or equipment that may hold product for a brief period of 
time but is not considered a permanent location.
A static/stationary location is a standard rack or floor area that cannot be 
moved.
Location Type Code 
(LOTP)
Mandatory
The type of location (RACK, DRY, COOLER, etc.).
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Locations (LOCA)
Isolator Code (ISOL) Mandatory
The isolator code (if any) of the location or NR for Not Required.
Hold Code (HOLD) Optional
If you attach a hold code to the location (for example, blast freezing), any 
product put in the location will be placed on automatic hold and cannot be 
shipped until it is released (unless product is on a shippable hold).
Attaching a hold to a location affects new inventory only. Product already in 
the location will not be placed on hold.
Cycle Count Profile Code 
(CYCP)
Optional
See the Cycle Counting Guide for further information.
Picking Path Sequence 
Number
Optional
See the RF Guide for further information on configuring the sort sequence for 
picking tasks in RFPIC. You set up the sort sequence for picking tasks in 
REGI (Task Profile).
Aisle Reference This field is used to identify aisles when the aisle cannot be extracted from the 
location code in the Location Attributes Block of WARE.
Facing Reference An additional field that can be used for sorting purposes.
Location Size Code 
(LOCS)
Optional
If you specify a size code for the location, AccellosOne 3PL will attempt to putaway product in a location whose location size code matches the product’s 
location size code.
Location Ship Unit ID Reserved for future use
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Locations (LOCA)
Track Last Location Used 
for Put-Away
F = Track at Level 4
H = Track at Level 3
N = Not Used
R = Track by Receipt
T = Track at Level 2
Y = Track at Level 1
If you select any option other than N (Not Used), you can put-away product 
into this location using the options in the Last Location Used group in ILOP 
(Put-Away). If you select Not Used, the options in the Last Location Used 
group in ILOP (Put-Away) are not available for this location.
For example, suppose you select Track at Level 1. Any lot for the same item 
will be considered the last location used. If, however, you select Track at Level 
2, any pallet ID belonging to the same lot will be considered the last location 
used.
Put-away/Directed Move 
Sort Sequence
See Allocation and Wave Manager.
Capacity SKU Code 
(SKUS)
Mandatory
The SKU type that is stored in the location.
Maximum Capacity Mandatory
The maximum capacity of the location in the units of measure defined in 
Capacity SKU Code field. If you are handling standard pallet sizes, AccellosOne 3PL’s active locator system uses this information to determine the best 
location for receiving any given product.
Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
Voice Check Digit 1/2/3 See the section on Voice Activated Picking and Order Assignment System in 
the RF Guide.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Locations (LOCA)
LOCATION ALIASES
Location aliases serve two functions in AccelloOne 3PL:
▪ because RF operators cannot see location aliases, they prevent operators from cheating by typing in the 
code for a location that they are not actually working at
Location X/Y/Z CoordinatesThese three fields allow you to define the travel distance between a bulk location and the pick-face when performing replenishments. When searching for a 
suggested put-away location, inbound allocation will search for locations that 
are as close as possible to the item's pick line location set up in PIIT. The unit 
of measure in these three fields is defined in the Linear Measure Code field.
NOTE This proximity logic applies to fixed pick line locations only; floating 
pick line locations are not supported.
ILOP uses the following formula to calculate a put-away location's proximity to 
an item's pick line location:
absolute value (X_locEmpty - X_locPIIT) + absolute value (Y_locEmpty - 
Y_locPIIT) + absolute value (X_locEmpty - Z_locPIIT) = storage distance 
score
The lower the score, the closer the location is to the pick line.
Proximity logic must be activated in ILOP by selecting option I8360, M8360 or 
MS 8360 “Order by distance to fixed pick line by LOCA X, Y, Z coordinates, 
ware, loc”.
Exclude from Follow 
Order Rule for Directed 
Staging
N = No
Y = Yes
This flag allows you to define rules for staging product in RFPIC/RFITLV when 
the RF operator overrides the suggested directed staging location. If you 
select No, the new staging location becomes the default staging location for 
the remaining pallets on that order. 
If you select Yes, any override by the RF operator of the suggested directed 
staging location will have no effect on the suggested directed staging location 
for the remaining pallets on the order.
Status A = Active
D = Deactivated
If a location is active, you can receive product into the location and ship product out of the location. If a location is deactivated, you cannot receive new 
product into the location.
FIELD DESCRIPTIONS

WAREHOUSE SETUP
Locations (LOCA)
▪ they allow you to split a location into two sections (for example, a carton live storage system) depending 
on your point of access: a front fill location alias for picking and a back fill location alias for put-away 
When putting away to locations with enabled aliases in RFCH, RFPU, RFPR, RFRL and RFITLV, the RF 
operator will either:
▪ see the location code but must scan in the back fill location alias and use the back fill check digits for 
validation (option Y in LOTP)
▪ see the alias and scan in the back fill location alias and use the back fill check digits for validation 
(option C in LOTP)
When picking or relocating from locations with enabled aliases in RFPIC/RFPK, RFST, RFITLV and RFRL, 
the RF operator will either:
▪ see the location code but must scan in the front fill location and use the front fill check digits for validation (option Y in LOTP)
▪ see the alias and scan in the front fill location alias and use the front fill check digits for validation (option 
C in LOTP)
PROCEDURE
1 Enter LOCA.
LOCATION ALIASES (LOTP)
Enable Location Aliases N = Not Used
Y = Use Aliases for Validation
C = Use Aliases to display and validation
If you specify Y or C, location aliases will be activated in LOCA. If you specify 
No, location aliases will NOT be activated in LOCA. Location aliases serve 
two functions in AccelloOne 3PL:
▪ because RF operators cannot see location aliases, they prevent operators 
from cheating by typing in the code for a location that they are not actually 
working at
▪ they allow you to split a location into two sections (for example, a carton live 
storage system) depending on your point of access: a front fill location alias 
for picking and a back fill location alias for put-away
If you select “Y - Use Aliases for validation”, the actual location code in LOCA 
will display, but the RF operator must enter or scan in the alias. If, on the other 
hand, you select “C - Use Aliases to display and validation”, the alias will display and the RF operator must enter or scan in this alias.
TIP It is best to create “like” locations all at the same time. For example, start by 
creating all your rack locations before you go on to create your bulk locations. By 
grouping your locations in this manner, you minimize changes to the “template” as 
you create new locations.

WAREHOUSE SETUP
Locations (LOCA)
2 Click on Enter Criteria then Execute Query to see which locations have been already set up. 
3 If you need to set up another location, click on Create Record.
4 Key in the warehouse code for the location and press Enter.
5 Key in your first location code and press Enter.
If you receive an error message, then your location code does not match the parameters that you set up 
in WARE (Warehouse and Location Format). Go back to WARE and verify the format of your location 
codes.
6 If required, key in a meaningful description for your location code and press Enter.
7 Key in a location bill code and press Enter or use your pick list to choose the appropriate code. To select 
a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick 
list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code.
8 If required, key in a location print profile code and press Enter.
9 Key in the linear measurement code for the location (IN = inches, FT = feet, etc.) and press Enter or use 
your pick list to select from a list of predefined codes.
10 Key in the height, width and length of the location, pressing Enter at the end of each line.
11 Key in the weight measurement code for the location (LBS = pounds, KG = kilograms, etc.) and press 
Enter or use your pick list to select from a list of predefined codes.
Locations
12 Key in your weight limit for the location and press Enter. If you do not require a weight limit for the location, key in 0.
13 If required, key in a location in the Master Location for Weight field and press Enter.
14 Press Enter to bypass the Vertical Height Factor Code field.
15 In the Location Structure Type Code field, use your pick list to choose the appropriate code.
16 Key in your location type code and press Enter or use your pick list to choose the appropriate code.

WAREHOUSE SETUP
Locations (LOCA)
17 Key in your isolator code if any and press Enter or use your pick list to choose the appropriate code.
Locations
18 Press Enter to bypass the Hold Code field.
19 Press Enter to bypass the Cycle Count Profile Code fields.
20 If required, key in a location size code and press Enter.
21 In the Track Last Location Used for Put-Away field, key in the appropriate value and press Enter.
22 Press Enter until your cursor is positioned in the Capacity SKU Code (SKUS) field.
23 Key in your capacity SKU code and press Enter or use your pick list to choose the appropriate code.
24 Key in the location’s maximum capacity in the units of measure that you specified in the previous field 
and press Enter.
25 Press Enter to bypass the Labor Standard Modifier field.

WAREHOUSE SETUP
Locations (LOCA)
26 Do one of the following:
27 When you finish adding your locations, click on Return to Main and then Exit to exit.
If you wish to create more 
locations based on the 
parameters of your first location: If you wish to exit:
a) Key in your new location code 
and press Enter.
b) If required, make any necessary 
changes to the parameters of the 
location (for example, the 
description, location type, isolation code, height, etc.).
c) Press F12 to add the new location.
d) Repeat the above steps for each 
additional location that you wish 
to add.
a) Proceed to next step.

CUSTOMER SETUP
Salespersons (SAPE)........................................................................................ 72
Customer Service Representatives (CUSE) ................................................... 73
Flow Process (FLPR) ........................................................................................ 75
Depositor Workflow Profile (DIFP) .................................................................. 78
Number Series (NUSE) ..................................................................................... 86
Depositor Inventory Assign Profile (DIAP) ..................................................... 88
Depositor Level Validation Profile (DLVP)...................................................... 95
Inventory Terminology (INTE).......................................................................... 99
Depositor Inventory Level Profile (DILP) ...................................................... 101
Depositor Item Profile (DITP) ......................................................................... 112
Picking Profile (PIPR) ..................................................................................... 114
Depositor Shipping & Receiving Profile (DSRP).......................................... 116
Telephone List Types (TETP)......................................................................... 120
Billing Terms (TERM)...................................................................................... 122
Holidays (HOLI) ............................................................................................... 126
Depositor Billing Profile (DBIP) ..................................................................... 127
Depositor Alternate Sorts (DEAS) ................................................................. 136
Customer Setup (CUST) — Basic .................................................................. 139
Customer Setup (CUST) — Advanced .......................................................... 151

CUSTOMER SETUP
Salespersons (SAPE)
Salespersons (SAPE)
OVERVIEW
In this program, you set up your salespersons. A salesperson is the individual who established the contract 
with the customer or is responsible for the rates charged to the customer. By setting up the information in 
SAPE, you have a point of contact if there are any questions with regard to the account or the rates.
If you do not know the salesperson for a particular account or you do not have salespersons in your 
warehouse, you can use the code HA for House Account.
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

CUSTOMER SETUP
Customer Service Representatives (CUSE)
Salespersons
3 If the salespeople that you require have already been set up, click on Exit to exit. There is no need to add 
any new codes to SAPE.
If the salespeople that you require have not been set up, click on Create Record. 
4 Key in your salesperson’s initials or other code (up to four alphanumeric characters) and press Enter.
5 In the Name field, key in the salesperson’s first and last name and press Enter.
6 Repeat steps 4 and 5 for each additional salesperson that you wish to add. 
7 When you finish setting up your salespeople, click on Return to Main and then Exit to exit the program.
Customer Service Representatives (CUSE)
OVERVIEW
In this program, you set up your customer service representatives. A customer service representative is the 
individual responsible for any support issues involving a customer.
If you do not know the name of a particular representative or do not have customer service representatives in 
your warehouse, you can use the code HA for House Account.
You can also use CUSE to set up “Attention to” names. “Attention to” names print on the accessorial, renewal, 
extra charge and immediate accessorial invoices if they are specified in BILB (Billing Batch).
PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of your customer service representatives

CUSTOMER SETUP
Customer Service Representatives (CUSE)
PROCEDURE
1 Enter CUSE.
2 Click Enter Criteria then Execute Query to see which customer service representatives have already 
been set up.
Customer Service Reps
3 If the customer service representatives that you require have already been set up, click on Exit. There is 
no need to add any new codes to CUSE.
If, however, the customer service representatives that you require have not been set up, click on Create 
Record.
4 Key in your customer service representative’s initials or other code (up to four alphanumeric characters) 
and press Enter.
5 In the Description field, key in the customer service representative’s first and last name and press Enter.
6 Repeat steps 4 and 5 for each additional representative that you wish to add. 
7 When you finish setting up your representatives, click on Return to Main and then Exit to exit the program.
FIELD DESCRIPTIONS
Customer Service RepresentativeMandatory
Your code for this customer service representative. For example, KJ for Karen 
Jones.
Name Mandatory
The name of the customer service representative.

CUSTOMER SETUP
Flow Process (FLPR)
Flow Process (FLPR)
OVERVIEW
AccellosOne 3PL uses flow process codes to track and time-stamp inbound and outbound shipments. There 
are six codes that are preloaded into your system and cannot be modified or deleted. These six codes are:
CITR (Change In-Transit to Regular)
COOR (Confirm Order)
CORE (Confirm Receipt)
EDI (Message Received by TradeLink)
ENOR (Enter Order)
ENRE (Enter Receipt)
Flow process codes are attached to the depositor workflow profile in DIFP. A workflow profile is a sequence of 
steps or “flows” that must be taken for all inbound receiving and outbound shipping. The following codes are 
mandatory and must be included in any workflow profile:
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
NOTE Although there is a create record function in FLPR, custom flow codes that 
you create yourself are not supported in RF. 

CUSTOMER SETUP
Flow Process (FLPR)
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
Suppression Rules for eVista Client AccountsSee the e-Vista Setup Guide — Warehouse Only.
Inbound Sequence NumberSee the Operational Board section in the Operations 2 Guide.
Outbound Sequence 
Number
See the Operational Board section in the Operations 2 Guide.

CUSTOMER SETUP
Flow Process (FLPR)
Flow Process codes
3 Using your arrow keys, go through each record to see the list of standard flow process codes that have 
been preloaded into your system. If the codes that you require have already been set up, click on Exit. 
There is no need to add any new codes to FLPR.
If, however, the flow process codes that you require have not been set up, click on Create Record.
4 Key in your new flow code and press Enter.
5 Key in a meaningful description for the new code and press Enter. The description that you type in here 
will be the description that you want your customer to see on his reports and documents.
6 In the Priority field, key in 1 and press Enter.
7 Press Enter to bypass the remaining fields in FLPR.
8 Repeat steps 4 to 7 for each additional code that you wish to add.
9 When you finish setting up your flow codes, click on Return to Main and then exit to exit the program.

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
Depositor Workflow Profile (DIFP)
OVERVIEW
In this program, you set up your workflow profiles. A workflow profile is a sequence of steps or “flows” that 
must be taken for all inbound receiving and outbound shipping. Workflow profiles serve three functions in 
AccellosOne 3PL:
▪ They are a way of time-stamping a task or action (for example, recording the arrival time of a driver). 
▪ They allow you to attach a particular document to a particular step in the sequence and require the operator to print that document before proceeding to the next step.
▪ They allow you to specify after which flow you want AccellosOne 3PL to perform allocation and deallocation.
The workflow profile that you create in this program is attached to the program CUST (Customer Code). You 
can set up one workflow profile for all your customers or you can set up separate workflow profiles for certain 
customers as required. You can also attach workflow profiles to consignees and shippers. Workflow profiles 
attached to consignees and shippers will override the workflow profile attached to the customer.
For example, if you set up two workflow profile codes — STD and ABC — and attach your STD code to 
customer 1 and your ABC code to consignee 1, the following will occur. When shipping customer 1’s product 
to consignee 1, AccellosOne 3PL will use the flows defined in workflow profile ABC. When shipping customer 
1’s product to any other consignee, AccellosOne 3PL will use the STD workflow profile.
There are four mandatory flow codes that are preloaded into your system and must be included in any 
workflow profile:
Inbounds
TIP The more flow codes that you use, the better you will be able to track and timestamp your inbound and outbound shipments. However, numerous flow codes will 
require more input on the computer.
PREREQUISITES: FLPR, DOCU (set up by HighJump)
ATTACHED TO: CUST (Customer Code)
CONS (Consignees)
SHIP (Shippers)
CCCC (Outbound Process Configuration)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The steps that you follow for your inbound receiving and outbound shipping and the documents that are printed at each step

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
ENRE (Enter Receipt)
CORE (Confirm Receipt)
Outbounds
ENOR (Enter Order)
COOR (Confirm Order)
These codes are mandatory and cannot be changed or deleted. You must use ENRE and CORE in all your 
inbound workflow profiles and ENOR and COOR in all your outbound workflow sequences. In addition to the 
four basic flows, you can add any of the standard preloaded flow codes in FLPR to any point in your workflow 
sequences; for example, you can add new flows to your inbound workflow sequence after ENRE and before 
or after CORE.
Flow codes and documents are assigned a number to indicate their sequence in the flow. You can have a 
total of 99 flows and 99 documents for any given inbound workflow sequence as well as 99 flows and 99 
documents for any given outbound workflow sequence. When adding new sequence numbers to your profile, 
it is best to use multiples of five or ten (10, 15, 20, 30, etc.) so that you can insert new flows in your sequence 
at a later time.
OVERRIDING THE CUSTOMER DIFP PROFILE
The DIFP profile attached to the customer in CUST is the default DIFP profile for that customer. You can 
override this default in SHIP (Shippers), CONS (Consignees) and CCCC (Outbound Process Configuration). 
The override logic works as follows:
▪ for receipts, the DIFP profile in SHIP (if any) overrides the default profile in CUST
▪ for orders, the DIFP profile in CONS (if any) overrides the default profile in CUST and the DIFP profile in 
CCCC (if any) overrides the DIFP profile in CONS
FIELD DESCRIPTIONS
Workflow Profile Code Mandatory
Your code for this profile. For example, ABC for Customer ABC or STD for 
Standard.
If you click on the View Flow Chart icon , you can see a flow chart of your 
profile showing each flow, the documents if any attached to the flow as well as 
any special verify programs.
Description Mandatory
Your description for this workflow profile code.

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
Sequence Mandatory
The position of the flow code in your flow sequence.
Flow Code
(defined in FLPR)
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
If you specify Yes, the allocation routine will assign locations for a receipt or an 
order after you have completed that flow. If you specify No, no allocation will 
occur after that flow. The Yes option is available for any inbound flow except 
CORE and any outbound flow except COOR. 
The Yes option is mandatory for at least one inbound and one outbound flow. 
If required, you can use the Yes option for multiple flows. For example, you 
perform initial allocation for an order at Flow 3 and then wish to rerun allocation at Flow 5 because new product has been received that will enable you to 
fill an order line.
* See “Inventory Only Allocation” in Allocation and Wave Manager Guide.
Deassign Location Only available for outbound flows
Y = Yes (Only available if Assign Location = Yes)
N = No
This field allows you to specify the flow(s) at which you can perform manual 
de-allocation. If you specify Yes, you can manually de-allocate an order in 
DEOR after you have completed that flow. If you specify No, you cannot manually de-allocated an order after that flow. The Yes option is not available for 
COOR (Confirm Order).
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
DOCUMENT BLOCK
In this block, you define the document(s) that you want to print at a particular flow. If you do not want to print 
any documents at a particular flow, leave this block blank for the flow.
Labor Standard Code See the Operational Board section in the Operations 2 Guide.
UOM See the Operational Board section in the Operations 2 Guide.
Modifier See the Operational Board section in the Operations 2 Guide.
Alert Time See the Operational Board section in the Operations 2 Guide.
Create DRMS Reserved for future use
FIELD DESCRIPTIONS
Sequence Mandatory
The sequence of the document within the flow that you specify in the Flow 
Block.
Document Code
(defined in DOCU)
Mandatory
The document that you wish to print. If you are using directed put-away, you 
must specify at least one document in your inbound flow sequence. If you are 
using directed picking, you must specify at least one document in your outbound flow sequence (unless you assign locations to orders in ASOR).
These restrictions do not apply to RF put-away and picking.
Form Code (defined in 
FORM)
Mandatory
The document’s form code. The form code determines the paper size, the 
number of horizontal lines on a page before a page break and the page’s orientation.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
SPECIAL VERIFICATION BLOCK
This block contains advanced programs and customized functions that can be added to any stage in your 
inbound or outbound procedure. See the System Administration Guide for instructions on setting up special 
verify programs.
PROCEDURE
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to see which workflow profiles have been already set up. 
3 If the workflow profile that you need is already set up, click on Exit to exit the program.
If, however, the workflow profile that you need is not set up, click Create Record. Then key in a unique 
code and description for the profile (for example, STD for Standard) and press Enter.
Type R = Regular
If you specify Regular, AccellosOne 3PL requires you to print this document 
before proceeding to the next step. Regular is the default or preset value in 
this field. 
O = Optional
If you specify Optional, you can bypass the printing of this document.
A = Automatic
If you specify Automatic, the document will be printed automatically after a 
specific flow. See the “Faxing and Auto-Printing” section in the Operations 2 
Guide for further information on this option.
P = Printer (sequences 1 and 90 only)
If you specify Printer, you can select your printer from a pop-up menu when 
you exit ENRE, ENOR or any confirmation program. After you select your 
printer, the document will be printed automatically. This option requires special 
programming by HighJump. 
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
Depositor Workflow Profile showing two default flows for inbound receiving
You will see the two standard flows for inbound receiving: ENRE and CORE. These flows are mandatory 
and cannot be deleted.
4 If you are using the active locator system for inbounds, you must set the Assign Location flag to Y for one 
flow in your inbound profile. 
If you are using the default setup of ENRE and CORE, set the Assign Location flag to Yes for ENRE to 
specify that you want allocation to take place after ENRE and before CORE. You set this flag to Yes by 
pressing Enter until your cursor is positioned on the next line. AccellosOne 3PL will automatically change 
N to Y for the flow ENRE.

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
If you are adding additional flows to your profile, you can program the allocation routine to run after any of 
your new flows.
5 If you have one or more documents such as a receiving tally or a notice that require setup for your 
inbound flow sequence, position your cursor in the appropriate Sequence field. 
For example, if you wanted to attach a document to flow code ENRE, you would position your cursor in 
flow sequence 1; alternatively, if you wanted to attach a document to flow code CORE, you would position your cursor in flow sequence 90.
6 Click on Document Block to enter the Document Block.
7 Key in the sequence number of the document (for example, 10) and press Enter. 
8 Key in your document code and press Enter. If you do not know the code of the document that you wish 
to have printed, you can select it from the pick list. To select a code using a pick list, press F10 to display 
the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
9 In the Form Code field, key in your form code and press Enter or use the pick list function to select the 
appropriate form.
10 Key in your document type (R for Regular, O for Optional, A for Automatic or P for Printer) and press 
Enter.
Adding New Flows to the Flow Block
a) With your cursor in the Sequence field of the Flow Block, click on Create 
Record to create a blank line.
b) Key in a sequence number for the new flow that corresponds to where in the 
sequence you want the flow to take place and press Enter. 
c) Key in your flow code and press Enter or select your code using the pick list.
d) Set the Mandatory flag to Yes or No for your new code and press Enter. If you 
set it to Yes, the operator will be forced to perform the flow. If you set it to No, 
the operator can bypass the flow.
e) Set the Assign Location flag to the appropriate value and press Enter. If set to 
Yes, AccellosOne 3PL will perform allocation after this flow.
f) Set the Deassign Location flag to the appropriate value and press Enter. If 
set to Yes, AccellosOne 3PL will perform deallocation after this flow.
g) Press Enter three times to bypass the Labor Standard Code, Alert Time and 
Create DRMS fields.
h) Click on Return to Main to exit create mode or repeat the above steps to add 
another flow.

CUSTOMER SETUP
Depositor Workflow Profile (DIFP)
Depositor Workflow Profile showing one document requiring printing after DRAR
11 If you need to add a second document, repeat steps 8 to 11. When you finish attaching your documents 
to this flow code, click on Return to Main and then Flow Block to return to the Flow Block.
12 If you wish to attach documents to another flow code, position your cursor in the Sequence field corresponding to the desired flow code. Then click on Document Block for that flow code and enter your document codes.
13 When you finish defining your inbound flow sequence, click on Return to Main and then Exit exit the program.
See the next section for information on setting up your outbound flow sequence.
SETTING UP YOUR OUTBOUND FLOW SEQUENCE
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to display the first profile on your system.
3 Use your arrow keys to locate the profile that you set up for your inbound procedure.
4 When you find it, click on In/Out/Repi/Relo Block.
5 Press your down arrow key to display the outbound record.
6 Follow the steps described previously for your inbound flow sequence to set up flows and attach documents to your outbound procedure. If you are using AccellosOne 3PL’s active locator system for outbounds, you must set the Assign Location flag to Yes for one flow in your outbound sequence.
7 Click on Return to Main and then Exit to exit the program.

CUSTOMER SETUP
Number Series (NUSE)
Number Series (NUSE)
OVERVIEW
In this program, you define the series of numbers (lot numbers, pallet ID’s, etc.) to be used by the Depositor 
Inventory Assign Profile (DIAP), AccellosOne 3PL’s auto-lot assignment program. This profile is only required 
if you want AccellosOne 3PL to generate series of numbers for your lot numbers, pallet ID’s, etc. If you create 
these numbers yourself or if they are supplied by your customers, you do not use NUSE or DIAP.
You can set up as many different number series as necessary (one for each customer if required). If you 
assign unique lot numbers for each warehouse, you will need to set up a unique series for each warehouse.
PREREQUISITES: None
ATTACHED TO: DIAP (Depositor Inventory Assign Profile Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you are using the program DIAP
OTHER REQUIREMENTS: The list of numbers that you wish to use for your lot numbers, pallet ID’s, 
etc.
FIELD DESCRIPTIONS
Number Code Mandatory
Your code for the number series (for example, LOT, PID, BOX, etc.).
Description Mandatory
Your description for the number series.

CUSTOMER SETUP
Number Series (NUSE)
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
The starting and ending number for your block of numbers. When AccellosOne 3PL reaches the end of your block of numbers, it will restart at the 
value that you define in the Start Number field.
NOTE Small ranges (for example, a starting number of 100 and an ending 
number of 200) are not recommended. If you must use a small range, make 
sure that you purge your inventory on a regular basis. If you fail to do so, you 
might have two open receipts with the same lot or pallet ID.
Current Number Calculated by AccellosOne 3PL.
Number to Reserve Mandatory
You can exclude a block of numbers from your number series by entering the 
appropriate number in this field. For example, if your starting number is 1,000 
and you enter 1,050 as your number to reserve, AccellosOne 3PL will reserve 
the first 50 numbers and start numbering at 1,051.
If you are excluding a block of numbers in create mode, your number to 
reserve must be greater than your starting number. If you are excluding a 
block of numbers in modify mode, your number to reserve must be greater 
than your current number.
If you do not wish to exclude a block of numbers from your number series, you 
enter your starting number minus 1. For example, if your starting number = 1, 
key in 0; if your starting number is 150000, key in 149999.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
Number Series starting with 150,000
8 Click on Exit to exit.
Depositor Inventory Assign Profile (DIAP)
OVERVIEW
This program is only required if you want AccellosOne 3PL to generate series of numbers for your lot 
numbers, pallet ID’s, production dates or other inventory level 2 or higher value. If you create these numbers 
yourself or if they are supplied by your customers, you do not use DIAP.
PREREQUISITES: WARE, NUSE
ATTACHED TO: DILP (Depositor Inventory Level Profile) --> CUST
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
CHANGE STATUS: Any changes to a profile take effect at the end of the frequency period. If 
you wish to make changes to your number series that are effective immediately, you must create a new profile and attach it to DILP.
OTHER REQUIREMENTS:

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
For example, if you want AccellosOne 3PL to assign lot numbers automatically when you enter the receipt, 
you must set up the parameters for the lot number in this program.
DIAP defines the parameters of the number series that you created in NUSE. You tell AccellosOne 3PL how 
the numbers are assigned (each time you process a new receipt, each time you process a new receipt line, 
each time you receive from a new customer, etc.), whether there are any prefixes and suffixes and whether to 
pad out the numbers with leading zeroes.
The numbers generated by DIAP are always at the next lower level than the level at which you are generating. For example, if you are generating numbers based on item (level 1), the numbers that you generate will 
be level 2. Likewise, if you are generating numbers based on item (level 1) and production date (level 2), the 
numbers that you generate will be level 3.
DIAP is attached to the Depositor Inventory Level Profile (DILP). You can create a single DIAP profile for all 
your customers or create customer specific profiles for those customers with special numbering requirements.
There are a number of options for defining how your numbers are assigned: 
▪ by receipt
▪ by receipt and up to a specified level (1, 2 or 3)
▪ by receipt line
▪ by period of time
▪ by customer over a specified period of time
▪ by period of time up to a specified level (1, 2 or 3)
OPTION DESCRIPTION
Number valid for period 
of
All customers, all receipts and all product will be assigned the same number 
for a specified period of time — provided the same DIAP profile is attached to 
“all” customers.
Number valid for each 
Depositor for period of
Each customer will be assigned a separate number and that number will be 
assigned to all product received from that customer during a specified period 
of time. 
Number valid for up to 
each level 1 for period 
of
All product with the same level 1 value received over a specified period of time 
will be assigned the same number.
The number generated will be level 2.
Number valid for up to 
each level 2 for period 
of
All product with the same level 1 and level 2 values received over a specified 
period of time will be assigned the same number.
The number generated will be level 3.
Number valid for up to 
each level 3 for period 
of
All product with the same level 1, level 2 and level 3 values received over a 
specified period of time will be assigned the same number.
The number generated will be level 4.

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
EXAMPLE 1
Level 1 = Item
Level 2 = Lot Number (system generated based on level 1)
Number valid for = each receipt and up to level 1 
Number valid for each 
receipt
All product on the same receipt will get the same lot number regardless of 
level 1 or the customer.
Number valid for each 
receipt and up to level 1
All product on the same receipt with the same level 1 value will get the same 
number. When you change level 1 on the same receipt, a new number will be 
assigned. 
The number generated will be level 2.
Number valid for each 
receipt and up to level 2
All product on the same receipt with the same level 1 and level 2 values will 
get the same number. When you change level 1 or level 2 on the same 
receipt, a new number will be assigned. 
The number generated will be level 3.
Number valid for each 
receipt and up to level 3
All product on the same receipt with the same level 1, level 2 and level 3 will 
get the same number. When you change either level 1, level 2 or level 3 on the 
same receipt, a new number will be assigned.
The number generated will be level 4.
Number valid for each 
receipt line
Everything on the same receipt line regardless of its level 2 or 3 value will get 
the same number. When you change receipt lines, AccellosOne 3PL generates a new number.
Number valid for period 
of
All customers, all receipts and all product will be assigned the same number 
for a specified period of time — provided the same DIAP profile is attached to 
“all” customers.
Number valid for each 
Depositor for period of
Each customer will be assigned a separate number and that number will be 
assigned to all product received from that customer during a specified period 
of time. 
Receipt Item
Lot Number Generated 
by System Remarks
001 Item A1 1 new item and therefore new lot number generated
001 Item B2 2 level 1 changes and new lot number generated
OPTION DESCRIPTION

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
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
001 Item A1 1 more Item A received and original lot number for this item 
assigned
Receipt Item
Lot Number Generated 
by System Remarks
001 Item A1 1 new line and therefore new lot number generated
001 Item B2 2 new line and therefore new lot number generated
001 Item A1 3 even though more of item A1 is received, it is received on a 
new line and therefore a new lot number is generated
Receipt Item
Production 
Date
Value # Generated 
by System Remarks
01 (Jan 01) TV Dinner 1 040701 427 new item and production date
01 TV Dinner 1 040701 427 same item and production date
01 TV Dinner 1 040730 428 same item but new production date; therefore new value #
02 (Jan 15) TV Dinner 1 040730 428 new receipt but item and production date remain the 
same; therefore same value #
02 TV Dinner 2 040730 429 item changes but not production date; therefore new value 
#
Receipt Item
Lot Number Generated 
by System Remarks

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
03 (Jan 20) TV Dinner 1 040730 428 new receipt but item and production date previously 
received on Jan 15; therefore use previously assigned 
value #
FIELD DESCRIPTIONS
Inventory Assign Profile 
Code
Mandatory
Your code for the number series (for example, LOT, PID, BOX, etc.).
Description Mandatory
Your description for the number series.
Name of Function to Generate Lot Number
Optional
You can use PL/SQL to write custom functions to generate inventory 2 or 
higher values. If you define a function, it will override any setups in the Detail 
Block.
Number Valid for Mandatory
The way in which you wish to assign your lot numbers (by receipt or receipt 
line, by period of time, by customer, by inventory level, etc.).
Frequency Code Mandatory if you select a time-dependent value in the Number Valid for field
The frequency with which you wish to assign your number series (for example, 
daily, weekly, monthly, etc.).
Cycle Mandatory if you select a time-dependent value in the Number Valid for field
The number of the units of time defined in the Frequency field that must pass 
before a new period begins. Refer to the example below for a demonstration 
of how the Frequency and Cycle fields work.
Receipt Item
Production 
Date
Value # Generated 
by System Remarks

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
PROCEDURE
1 Enter DIAP.
2 Click on Enter Criteria then Execute Query to see which profiles have already been set up.
3 If you need to set up another profile, click on Create Record.
Frequency
weekly
daily
monthly
Cycle
1
3
2
Result
 every week
 every three days
 every two months
Whse
(defined in WARE)
Mandatory
The warehouse code that this number series applies to. If you wish it to apply 
to all warehouses, use .ALL.
Number Code
(defined in NUSE)
Mandatory
The number series code that you set up in NUSE.
Prefix Optional
A prefix, if any, that you wish to attach to your number series.
Prefix Date Format Optional
If you enter a date format (for example, YDDD, DDMMYY, MMDDYYYY, etc.), 
the current system date will print on the case pick label.
Suffix Optional
A suffix, if any, that you wish to attach to your number series.
Pad N = No
Y = Yes
If you specify No, the numbers will not be padded out with zeroes (for example, the number 99 will appear as 99 and not 000099). If you specify Yes, the 
number will be padded out with zeroes if it is less than the maximum number 
of characters that you defined in NUSE.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Inventory Assign Profile (DIAP)
4 Key in your profile code (for example, LOT or CUS1) and press Enter.
5 Key in a description for your code and press Enter.
6 In the Number Valid for field, use your pick list to choose the appropriate code. To select a code using a 
pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then 
use your arrow keys to position your cursor over the appropriate code and click on Select Code.
7 If you selected a time-dependent value in the previous field, you must enter a value in the Frequency 
field. Use your pick list to choose the appropriate code (daily, weekly, monthly, etc.).
Then enter a number in the Cycle field. The cycle value defines how many of these units of time must 
pass before a new period begins. Key in the number of days, weeks, months, etc. for the frequency that 
you selected and press Enter.
8 In the Detail Block, key in the warehouse code that this profile applies to and press Enter or use .ALL for 
all warehouses.
9 In the Number Code field, key in your number code and press Enter or use your pick list to select it.
10 If required, key in a prefix for the number and press Enter or press Enter with this field blank to bypass it.
11 If required, key in a prefix date format for the number and press Enter or press Enter with this field blank 
to bypass it.
12 If required, key in a suffix for the number and press Enter or press Enter with this field blank to bypass it.
13 In the Pad field, key in Y for Yes to pad or zero fill the number and press Enter or press Enter to accept 
the value of No.
14 If required, key in another line in the Detail Block for a second warehouse and repeat the above steps or 
click on Return to Main to exit create mode.
Depositor Inventory Assign Profile screen with the number valid for each receipt and up to level 2
15 Click on Master Block and Exit to exit the program.

CUSTOMER SETUP
Depositor Level Validation Profile (DLVP)
Depositor Inventory Assign Profile screen with the number valid for each receipt and up to level 1
Depositor Level Validation Profile (DLVP)
OVERVIEW
This program allows you to define acceptable values for any level 2, 3 and 4 entry (that is, those lot numbers, 
serial numbers, date codes, etc. that you want to accept). During receipt entry, AccellosOne 3PL will perform 
level validation and will reject any item whose lot number, serial number, date code, etc. does not match the 
acceptable values that you defined in DLVP. 
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

CUSTOMER SETUP
Depositor Level Validation Profile (DLVP)
entry, if the operator enters a lot number other than 111 or 999 for any item belonging to 
that customer, the receipt will be rejected.
The acceptable values that you set up in DLVP can apply to a single level of inventory or to a number of 
levels. You need to set up a separate profile for each level of inventory that you wish to verify; therefore, if you 
are verifying two levels of inventory, you must set up two different profiles. 
Level verification can apply to all of a customer’s items or to only certain of a customer’s items. If level verification is item specific, you must specify in DLVP the items to which level verification applies. Items must be 
set up in ITEM before you can attach them to DLVP.
In the Depositor Inventory Level Profile (DILP), you attach your DLVP profile to the level of inventory to which 
it applies.
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

CUSTOMER SETUP
Depositor Level Validation Profile (DLVP)
PROCEDURE
1 Enter DLVP.
2 Key in a meaningful level validation profile code and press Enter.
3 Key in a description for your code and press Enter.
4 In the Level Block, click on Create Record.
5 In the Level Code field, key in the lot number, serial number or date code that you wish to accept and 
press Enter.
6 Key in a description and press Enter.
Restrict N = No
Y = Yes
If you specify N for No, the restriction applies to all of a customer’s items and 
no further input is required. If you specify Y for Yes, the restriction applies to 
certain items only. The Yes option requires you to enter those items in the Item 
Block.
Customer Code Mandatory if you set the Restrict field to Yes
The customer of the item(s) that you wish to verify.
Item Code Mandatory if you set the Restrict field to Yes
The item(s) that you wish to verify.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Level Validation Profile (DLVP)
7 In the Restrict field, key in N for No if the restriction applies to all of a customer’s items or Y for Yes if the 
restriction applies only to certain items. Then press Enter.
Depositor Level Validation Profile with two items defined for level code 103
8 When you finish entering all the items that the restriction applies to, click on Return to Main to exit create 
mode.
9 Click on Master Block and Exit to exit the program.
If you enter N for No in the 
Restrict field:
If you enter Y for Yes in the 
Restrict field:
a) If required, key in another line in 
the Level Block for an additional 
lot number, serial number or date 
code that you wish to accept and 
press Enter.
b) When you finish entering all the 
lot numbers, serial numbers or 
date codes that you wish to 
accept, click on Return to Main to 
exit create mode. Then click on 
Master Block and Exit to exit.
a) In the Item Block, click on Create 
Record.
b) Key in your customer code and 
press Enter or use your pick list 
to select it. To select a code 
using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the 
pick list codes. Then use your 
arrow keys to position your cursor over the appropriate code 
and click on Select Code.
c) Key in your item code and press 
Enter or use your pick list to 
select it.
d) Press Enter to accept the value 
of Y in the Correct field.
e) Repeat the above steps for each 
item that the restriction applies 
to.

CUSTOMER SETUP
Inventory Terminology (INTE)
DELETING A LINE IN THE ITEM BLOCK
1 Enter DLVP.
2 Retrieve the profile containing the line that you wish to delete.
3 Position your cursor over the record that you wish to delete.
4 Cl.ick on Delete Record to delete the line.
5 Click on Return to Main to exit create mode.
6 Click on Master Block and Exit to exit the program.
Inventory Terminology (INTE)
OVERVIEW
In this program, you set up your inventory terminology for your levels of inventory. A level of inventory in 
AccellosOne 3PL refers to the ways in which you wish to identify an item for tracking and billing purposes. For 
example, lot number, serial number, expiry date, color, model #, pallet ID, etc. are considered inventory levels 
in AccellosOne 3PL.
In INTE you define your inventory terminology — that is, what you want to call your inventory levels. In DILP 
you actually set up the inventory levels themselves. The inventory terminology that you create in this program 
will appear on most reports, invoices and documents produced for your customers.
You must create one inventory terminology code for each level of inventory that you wish to track. Since 
different customers may have different tracking requirements, you may need to set up different codes for 
different customers. For example, if one of your customers uses the term “Pallet ID” while another customer 
uses the term “Pallet #”, you could set up two INTE codes to reflect the difference in terminology among your 
customers.
PREREQUISITES: None
ATTACHED TO: DILP (Depositor Inventory Level Profile) --> CUST
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE The INTE code “ITEM” is a system code and cannot be deleted, modified or 
translated. However, you can customize the description of item as required (for example, ITEM = Item Code or SKU Number, etc.). The description of ITEM that you specify in this program will apply to all customers on your system.

CUSTOMER SETUP
Inventory Terminology (INTE)
PROCEDURE
1 Enter INTE.
2 Click on Enter Criteria then Execute Query to view the inventory terms already set up.
Inventory Terminology
3 Using your arrow keys, go through each record to see which inventory terminology codes have already 
been set up. If the codes that you require have already been set up, click on Exit. There is no need to add 
any new codes to INTE.
4 If the inventory terminology codes that you require have not been set up, click on Create Record.
FIELD DESCRIPTIONS
Code Mandatory
Your inventory terminology code. For example, LOT for lot number or PID for 
pallet ID.
Description Mandatory
Your description for the code.
RF If you do not set up inventory terminology codes for RF (for example, LT for 
Lot instead of L2), AccellosOne 3PL will use the system defaults: L1 for Level 
1, L2 for Level 2, L3 for Level 3 and L4 for Level 4.
RF terminology applies to the following RF programs: RFCH, RFPU, RFPIC, 
OLOP and RFRL.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
5 Key in your new inventory code and press Enter.
6 Key in a meaningful description for the new code and press Enter.
7 If required, key in your custom RF terminology and press Enter or press Enter with the field blank to 
bypass the RF field.
8 Repeat steps 5 to 7 for each additional code that you wish to add.
9 When you finish entering your codes, click on Return to Main and then Exit to exit the program.
Depositor Inventory Level Profile (DILP)
OVERVIEW
In this program, you set up your inventory levels. Inventory levels are the different ways that you wish to use 
for identifying an item for tracking and billing purposes (for example, lot number, serial number, expiry date, 
color, etc.). The inventory level profile makes it possible to customize the number of levels for each customer.
You can have a maximum of four inventory levels in AccellosOne 3PL. Level 1 is always Item but levels 2, 3 
and 4 can be anything that you define. 
The chart below illustrates different setups for a customer depending on the way in which you want to track 
that customer’s product.
You can track product at one level and bill at another or you can track and bill at the same level. For example, 
consider the following customer:
PREREQUISITES: INTP, INTE, CHAR, NUSE, DIAP, DLVP
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you wish to make changes to an inventory level profile after attaching it 
to a customer, you must contact HighJump for assistance. This is a billable service if the customer has inventory and history records.
OTHER REQUIREMENTS: You must know how each of your customers is to be tracked and billed
Level 1 = Item
Level 2 = Serial Number
Level 1 = Item
Level 2 = Lot Number
Level 3 = Color
Level 1 = Item
Level 2 = Product Date Code
Level 1 = Item
two-level customer three-level customer two-level customer one-level customer

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
Customer A
Level 1 = Item (this is mandatory)
Level 2 = Lot Number
Level 3 = Pallet ID
In this example, you are tracking by three levels — item, lot number and pallet ID. If you bill at level 1 (Item), 
lot numbers and pallet ID will not be broken out on invoices and separate charges will not be generated for lot 
numbers or pallet ID’s. If, on the other hand, you bill by lot number, then item and lot number (but not pallet 
ID) will be broken out on all invoices and charges will be generated for different lots.
In DILP you can also set up:
▪ what you want to call a particular level (that is, the inventory terminology)
▪ the level at which you wish to perform level validation (if you have created a level validation profile in 
DLVP)
▪ the level at which you wish AccellosOne 3PL to generate lot numbers (if you have created a number 
series in NUSE and a profile for this number series in DIAP)
▪ the format of item codes, lot number, serial numbers, etc.
▪ the level at which you wish to charge initial and renewal storage
▪ your minimum charges for initial storage, renewal storage and handling
A customer can have only one depositor inventory level profile. If you need more than one profile for a 
customer, you must create two customers.
In DILP, you set the maximum number of levels for a particular profile. The profile is then attached to a 
customer in CUST. Individual items belonging to that customer can have fewer than the maximum number of 
levels defined in DILP but can never have more than the maximum.
NOTE Inventory levels are different ways of describing what a particular item is 
(item x, serial number y, lot z, expiry date whatever, etc.). They do not define the 
quantity of the item. The quantity of an item is given by the quantity breakdown (pallet/20 cases/50 eaches) defined in IQBP (Item Quantity Breakdown Profile).
For example, a given item has two levels: ITEM and PALLET ID. The quantity breakdown is PALLETS/CASES/EACHES. If you wanted to track the item, you would use 
the PALLET ID. If you wanted to count how much of the item you had in your warehouse, you would count the number of PALLETS (a SKU type), not the number of 
PALLET ID’s (an inventory level).
TIP If you have minimum charges for initial storage, renewal storage, handling, etc., 
do not attempt to set them up when you first create your DILP profile. Instead, use 
your No Charge charge code that you set up in CHAR. Later, when you set up other 
charge codes in Part IV of this manual, you can go back to DILP and adjust your minimum charges if required.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
FIELD DESCRIPTIONS
Inventory Level Profile 
Code
Your inventory level profile code.
Description Your description for the code.
Inventory Terminology 
Code (INTE)
Mandatory
The name of the inventory level as it will appear on reports, invoices and documents produced for your customers. For level 1, AccellosOne 3PL assigns 
the code ITEM automatically and this code must not be changed. For subsequent levels, you can select from a pick list.
Assign Description to 
New Entity
Only available for level 2 or higher
N = No
Y = Yes 
This field allows you to manually enter a description for each receipt line in the 
program ENRE. If you set this field to Y for Yes, you must enter a description 
for the receipt line at the level that you specify.
For example, if you are setting up a three-level customer with item, model 
number and serial number who also requires a meter read to be tracked, you 
can track the meter read by means of the this field.
You put in Y in the this field for your second level (model number). When 
receiving product, you will be prompted to enter not only the item and model 
number, but also a second level description (your meter read). Then you will 
be prompted to enter your third level (serial number).
Assign Value to New 
Entity
Reserved for future use

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
Sequential Entry Only available for level 2 or higher
A = Receipt Entry
B = Order Entry
C = Receipt/Order Entry
D = RF Receipt Entry
N = None
This field allows you to avoid repetitive entry of the same information when 
entering a receipt or order. You enter your highest inventory levels (for example, levels 1 and 2) once and these levels are automatically attached to lower 
inventory levels (for example, level 3).
For options A, B, and C, refer to “Sequential Entry Receipts” in the Operations 
1 Guide for further information on this field.
Singleton Entry Reserved for future use 
Item Minimum Shipping 
Level Flag
Only available for level 2 or higher
N = No
Y = Yes
If you specify No, this function is deactivated. If you specify Yes, IMSL (Item 
Minimum Shipping) will be activated. This program allows you to specify minimum level 2, 3 and 4 values (outbound picking only). Refer to Allocation and 
Wave Manager Guide for further information on IMSL.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
Method of Generating/
Validating Values
A = Arbitrary (default)
D = Depositor
W = Warehouse (level 2 or higher only)
V = Validate (level 2 or higher only)
This option allows you to define the valid format for any inventory level. For 
example, if you have a customer whose item codes always begin with the letters BA, you can define the item code format such that an item code that does 
not conform to this format is rejected. For example, should you try to create a 
new item code in ITEM starting with XY, AccellosOne 3PL will not allow you to 
do so.
If you use this option for other inventory levels such as lot numbers or pallet 
ID’s, validation will occur in ENRE (Enter Receipts). You define the format in 
the Assign Block of DILP.
A = Arbitrary
Validation for item codes and inventory levels is switched off.
D = Depositor
This option is used if you wish to define the valid format for any inventory level 
in the Assign Block of DILP. If you use Depositor for inventory level 1 or item, 
validation will occur when you set up a new item in ITEM. If you use Depositor 
for level 2 or higher, validation will occur during receipt entry.
W = Warehouse (level 2 or higher only)
This option is only used if you have set up NUSE (Set Up Number Series) and 
DIAP (Depositor Inventory Assign Profile). When you specify W for Warehouse, AccellosOne 3PL will automatically generate lot numbers, pallet ID’s, 
etc. upon receiving product. 
V = Validate (level 2 or higher only)
This option is only used if you have set up a profile in DLVP and wish to perform level validation.
Inventory Assign Profile 
Code (DIAP)
Mandatory if you set the Method of Generating/Validating Values field to W for 
Warehouse 
The profile that you defined in DIAP will be attached to the inventory level that 
you specify.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
BILLING RELATED FIELDS
The Charge Initial and Renewal Storage field must be set to Yes for one of your inventory levels even if you 
do not use AccellosOne 3PL for billing. 
For whichever level you set this field to Yes, you must enter valid charge codes in all the minimum charge 
code fields (Billing Entity, Renewal Storage, etc.). If there is no minimum charge for a field, use NC for No 
Charge in the field. If you are not using AccellosOne 3PL for billing, set all these fields to NC.
Point at Which Values 
Generated
Mandatory if you set the Method of Generating/Validating Values field to W for 
Warehouse 
L = Line
E = Entry
R = RF
If you specify Line, the numbers defined in NUSE and DIAP will be generated 
when you finish a given receipt line in ENRE and start entering the next line. 
If you specify Entry, the numbers will be generated immediately — that is, 
before proceeding to the Quantity field in ENRE for a given receipt.
If you specify RF, the numbers will be generated when you process a given 
receipt in RFCH. Numbers in RF can only be generated at the lowest inventory level.
Level Validation Profile 
Code (DLVP)
Mandatory if you set the Method of Generating/Validating Values field to V for 
Validate
You select an appropriate profile from DLVP by using your pick list.
NOTE If you do not have a charge code of NC for No Charge on your system, you 
must create one in CHAR before you set up your depositor inventory level profile in 
DILP.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
FIELD DESCRIPTIONS
Charge Initial and 
Renewal Storage
In this field, you specify the inventory level at which you want AccellosOne 
3PL to charge. One and only one of your inventory levels must have this field 
set to Yes.
For example, suppose you have a customer with two levels of inventory:
1) item 
2) lot
If you wanted to charge at the lot level, you would set this field to Yes when 
you set up level 2. If you wanted to charge at the item level, you would set this 
field to Yes when you set up level 1.
If you charge at the lot level, AccellosOne 3PL will show one charge for each 
lot on a given invoice. If you charge at the item level, AccellosOne 3PL will 
show one charge for each item on a given invoice.
Billing Entity Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for 
that level 
See the Billing and Invoicing Guide.
Renewal Storage Line 
Minimum Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for 
that level
See the Billing and Invoicing Guide.
Initial Storage Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for 
that level 
See the Billing and Invoicing Guide.
Handling Minimum 
Charge Code
Mandatory if you set the Charge Initial and Renewal Storage flag to Yes for 
that level 
See the Billing and Invoicing Guide.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
CREATING A LEVEL 1 PROFILE
1 Enter CHAR (Charge Codes) and make sure that you have a charge code of NC for No Charge.
2 Enter DILP.
3 Click on Create Record.
4 Key in a meaningful code for your profile (up to four alphanumeric characters) and press Enter. Then key 
a meaningful description and press Enter again.
5 When you finish entering your profile code and description, AccellosOne 3PL will automatically set up 
level 1 as ITEM and fill in the first seven fields of the Level Block. ITEM is a mandatory code for level 1 
and should not be changed.

Depositor Inventory Level Profile level 1
6 Select the appropriate value in the Method of Generating/Validating Values field (A for Arbitrary or D for 
Depositor) and press Enter. The Depositor option is only required if you wish to define the format of your 
item codes, serial numbers, lot numbers, etc.
7 Key in the appropriate Charge Initial and Renewal Storage value and press Enter. If you specify Y for 
Yes, AccellosOne 3PL will invoice at level 1 (Item). If you specify N for No, you must specify a Yes value 
at another level in the same profile.
8 Key in the appropriate minimum charge codes for the following fields and press Enter.
▪ Billing Entity Minimum Charge Code
▪ Renewal Storage Line Minimum Charge Code
▪ Initial Storage Minimum Charge Code
▪ Handling Minimum Charge Code
If you entered Y for Yes in the previous field (Charge Initial and Renewal Storage), you must enter a valid 
charge code or a code of NC for No Charge in the above fields.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
If you entered N for No in the previous field, you can press Enter to bypass all these fields.

Depositor Inventory Level Profile showing no invoicing at level 1 (ITEM)
9 If you selected Depositor as your method of generating/validating values (step 6), AccellosOne 3PL will 
now display the Assign Block. Refer to the instructions on the pages that follow for information on what to 
enter in this block.
If you selected Arbitrary as your method of generating/validating values, AccellosOne 3PL will now display your level 2 screen. Refer to the section below for instructions on creating your second level of 
inventory (if required). If you are setting up a single-level profile, click on Return to Main to exit create 
mode. Then click on Master Block and Exit to exit the program.
ADDING A SECOND LEVEL TO A PROFILE
If you are adding your second level at the same time as you are creating your first level of inventory, proceed 
to step 4.
1 Enter DILP and select the profile to which you wish to add a second inventory level.
2 Click on Level Block.
3 Click on Create Record. AccellosOne 3PL will display level 2.
4 Key in your inventory terminology code and press Enter or use your pick list to select it. To select a code 
using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list 
codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
The code that you enter in this field will be used on all customer-related reports, invoices and documents 
to describe the level that you are setting up.
5 Key in your Assign Description to New Entity value and press Enter. If you set this field to Yes, you can 
enter a description for this level on any receipt.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
6 Press Enter to bypass the Assign Value to New Entity field.
7 Press Enter to bypass the Sequential Entry field.
8 Press Enter to bypass the Singleton Entry field.
9 Press Enter to bypass the Item Minimum Shipping Level Flag field.
10 In the Method of Generating/Validating Values field, key in the appropriate value (A for Arbitrary, D for 
Depositor, W for Warehouse or V for Validate) and press Enter.
11 If you selected Warehouse in the previous field, key in your DIAP profile in the Inventory Assign Profile 
Code field and press Enter or use your pick list to select it.
Then key in L for Line or E for Entry in the Point at which Values Generated field and press Enter.
12 If you selected Validate in the Method of Generation/Validating Values field, key in your DLVP profile in 
the Level Validation Profile Code field and press Enter or use your pick list to select it.
13 Key in the appropriate Charge Initial and Renewal Storage value and press Enter. If you select Y for Yes, 
AccellosOne 3PL will invoice at level 2. If you specify N for No, you must specify a Yes value at another 
level in the same profile.
14 Key in the appropriate charge codes for the following fields and press Enter:
▪ Billing Entity Minimum Charge Code
▪ Renewal Storage Line Minimum Charge Code
▪ Initial Storage Minimum Charge Code
▪ Handling Minimum Charge Code 
15 When you finish entering all your charge codes, AccellosOne 3PL will display level 3. Repeat the above 
steps for level 3 or click on Return to Main, Master Block and Exit to exit the program.
ASSIGN BLOCK
You use the Assign Block to define the format of your inventory level codes for a particular customer. For 
example, if you have a customer whose item codes always begin with the letters BA, you can define the item 
code format such that an item code that does not conform to this format is rejected. 
If your customer tracks by item and serial number, you can define valid formats for both inventory levels. If 
you define a format at level 1 (item level), item codes that do not match the format will be rejected in ITEM 
when you try to add a new item. If you define a format at other inventory levels, validation will occur in the 
Enter Receipt program (ENRE) or RFCH.
FIELD DESCRIPTIONS
Partition Number If your item code or lot number can be broken down into distinct parts (for 
example, AB1234), you can create multiple partitions and define each partition 
separately. If your codes are uniform (for example, always numbers), you 
need only define a single partition.
Length of Partition The number of characters in the partition that you want AccellosOne 3PL to do 
validation on. If you set the Exact Length field to No, you can create item 
codes, lot number, etc. that exceed the Length of Partition value. However, no 
validation will occur on these extra characters.

CUSTOMER SETUP
Depositor Inventory Level Profile (DILP)
EXAMPLE
If you have an item code of AB1234, you could define your code as follows:
Partition 1
length = 2, valid characters = AB
Partition 2
length = 4, valid characters = 1234 
PROCEDURE
1 Enter DILP and retrieve the profile that you wish to work with.
2 Click on Level Block.
3 Select the level whose code you wish to define.
4 Set the Method of Generating/Validating Values field to D for Depositor and press Enter.
5 Click on Return to Main to refresh your screen.
6 Click on Assign Block.
Exact Length Y = Yes
N = No
If you set this field to Yes, AccellosOne 3PL will perform validation on all characters in the item code, lot number, etc.
If you set this field to No, AccellosOne 3PL will perform validation on the number of characters that you entered in the Length of Partition field. You can add 
extra characters to an item code, lot number, etc., but no validation on these 
extra characters will be performed.
NOTE If you have multiple partitions for a particular code, the Exact Length 
flag should not be set to N for No for partition 1 or 2 and then set to Y for Yes 
for a partition higher than 1 or 2. Consider the following examples:
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
Examples 1 and 2 are both valid. However, the value of N for No in the first 
partition of example 3 will be treated as a Yes.
Valid Characters The characters that you can use in your item code, lot number, etc. Valid characters can be numbers or letters. Special characters such as #, &, %, etc. are 
not valid. Nor can you use periods, commas or embedded spaces.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Item Profile (DITP)
7 Key in 1 for partition 1 and press Enter.
8 Key in the length of partition 1 and press Enter.
9 In the Exact Length field, key in Y for Yes or N for No and press Enter.
10 Key in the valid characters for this code and press Enter. 

Depositor Inventory Level Profile — Assign Block
11 If required, repeat the above steps to create a second partition.
12 When you finish defining your codes, click on Return to Main to exit create mode.
13 Click on Master Block and Exit to exit.
Depositor Item Profile (DITP)
PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

CUSTOMER SETUP
Depositor Item Profile (DITP)
OVERVIEW
In this program, you set up the weight measure that you wish to use when looking up the total weight shown 
on the receipt and order headers. The total weight of the receipt header is shown in the header block of LORE 
and in the running totals for the entire receipt in ENRE. The total weight of the order header is shown in the 
header block of LOOR and in the running totals for the entire order in ENOR. 
You also set up the default linear measure (feet, inches, centimeters, etc.) that you wish to use for cube 
reporting in the Wave Report and in other interfaces.
FIELD DESCRIPTIONS
Depositor Item Profile Mandatory
Your depositor item profile code.
Description Mandatory
Your description for this code.
Record Weight Measure 
Code
Mandatory 
The default weight measure (pounds, kilograms, tons, etc.) that you wish to 
use when looking up the total weight of the receipt and order headers.
NOTE The unit of measure that you define in DITP applies to the total 
gross and net weight shown in the order and receipt headers only. All other 
weights in AccellosOne 3PL (for example, the weight of order and receipt 
lines, weights shown in LOEN, etc.) are defined at the item level in ITEM.
Record Linear Measure 
Code
Mandatory 
The default linear measure (feet, inches, centimeters, etc.) that you wish to 
use for cube reporting in the Wave Report and in other interfaces. This linear 
measure code will override the linear measure code defined at the item level 
in ITEM.
Track Item Cost Reserved for future use
Number of Item Costing 
Buckets
Reserved for future use
Maintain Item Prices Reserved for future use

CUSTOMER SETUP
Picking Profile (PIPR)
PROCEDURE
1 Enter DITP.
2 Click on Enter Criteria then Execute Query to see whether a profile has already been set up. 

Depositor Item Profile
3 If you already have one profile on your system, no further action is required. Click on Exit to exit. If there 
is no profile on your system, proceed to create one.
4 Click on Create Record to enter create mode. Then in the Depositor Item Profile field, key in your depositor item profile code and press Enter.
5 In the Description field, key in your description and press Enter.
6 In the Record Weight Measure Code field, key in your weight measure and press Enter or select it using 
the pick list.
7 In the Record Linear Measure Code field, key in your linear measure and press Enter or select it using 
the pick list.
8 Click on Return to Main then Exit to exit the program.
Picking Profile (PIPR)
PREREQUISITES: None

CUSTOMER SETUP
Picking Profile (PIPR)
OVERVIEW
In this program, you define how product will be allocated to orders (if you use directed picking). In PIPR, you 
can specify:
▪ FIFO (First In First Out) or LIFO (Last In First Out)
▪ absolute FIFO/LIFO (that is, always pick from the oldest or newest lot, then the next oldest/newest lot, 
etc., etc. and attach relatively less importance to location and capacity factors defined in ILOP) 
▪ relative FIFO/LIFO (that is, pick from a group of the oldest or newest lots and use location and capacity 
parameters defined in ILOP to make selections within this batch)
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

CUSTOMER SETUP
Depositor Shipping & Receiving Profile (DSRP)

Picking Profile screen showing an NA code
19 Click on Exit to exit the program.
Depositor Shipping & Receiving Profile (DSRP)
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

CUSTOMER SETUP
Depositor Shipping & Receiving Profile (DSRP)
▪ your warehouse restriction options (you can restrict an order line or a receipt line to a specific warehouse) 
This profile is attached to your customers in CUST. If any of the above options differ for certain of your 
customers, you must set up multiple DSRP profiles.
FIELD DESCRIPTIONS
Shipping/Receiving ProfileMandatory
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
In this field, you define the type of order line created — Regular or Pending — 
when there is insufficient product to fill an order line.
EXAMPLE
You receive an order for 20 cases of product X but can only ship 10. 
Change Zero Pending Line to R-Type Line = Yes
If two lots were chosen during allocation, AccellosOne 3PL will generate two 
regular lines:
1) Lot A ordered = 10 shipped = 10 (Regular)
2) Lot B ordered = 10 shipped = 0 (Regular)
If one lot was chosen during allocation, AccellosOne 3PL will generate one 
regular line:
1) Lot A ordered = 20 shipped = 10 (Regular)
The order can be confirmed in CHOF or COOL.

CUSTOMER SETUP
Depositor Shipping & Receiving Profile (DSRP)
Change Zero Pending Line to R-Type Line = No
AccellosOne 3PL will generate one regular line and one pending line:
1) ordered = 10 shipped = 10 (Regular)
2) ordered = 10 shipped = 10 (Pending)
The order cannot be confirmed in CHOF or COOL until the product required is 
received or the pending line is deleted. 
P.O. Required on Orders Reserved for future use
Allow Back Orders See the back order section in the Operations 2 Guide for further information 
on this field.
Create Back Orders at 
Allocation
See the back order section in the Operations 2 Guide for further information 
on this field.
Ship Full Order Quantity See the back order section in the Operations 2 Guide for further information 
on this field.
Picking Profile Code 
(PIPR)
Mandatory
The default picking profile for the customer to which this DSRP profile is 
attached.
Put-Away Profile Code 
(PUPR)
Optional
The default put-away profile for the customer to which this DSRP profile is 
attached. The PUPR profile allows you to put-away product to a pick line.
Allow In-Transit Receipts Reserved for future use
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Shipping & Receiving Profile (DSRP)
PROCEDURE
1 Enter DSRP.
2 Click on Enter Criteria) then Execute Query to see which depositor shipping & receiving profiles have 
been already set up. 
3 If you need to set up another profile, click on Create Record.
4 Key in a depositor shipping & receiving profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 Press Enter to bypass the Ship Only Fully Filled Orders field.
7 In the Change Zero Pending Line to R-Type Line field, key in Y for Yes or N for No and press Enter.
8 Press Enter to bypass the P. O. Required on Orders field.
9 Press Enter three times to bypass the Allow Back Orders, Create Back Orders at Allocation and Ship Full 
Order Quantity fields.
10 In the Pick Profile Code field, key in your picking profile and press Enter or use your pick list to select it. 
To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve 
the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click 
on Select Code.
11 If required, key in your put-away profile code and press Enter.
Warehouse Restriction 
Flag
Optional
 = blank
I = Inbound
O = Outbound
B = Both
This field allows you to restrict receipt lines and order lines to a specific warehouse. For example, if you specify I for Inbound, you can enter a warehouse 
code for any receipt line in ENRE and only locations in that warehouse will be 
available for that receipt line. If you leave this field blank, no warehouse 
restrictions will apply at the receipt or order line level.
Order Statistics for 
Grouping
Reserved for future use
Replenishment OptimizationRefer to Allocation and Wave Manager Guide for further information on 
replenishment optimization.
Allocation of Variable 
Quantity Breakdown 
Items Based on Highest 
SKU Entered
See Allocation and Wave Manager Guide for further information on this field.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Telephone List Types (TETP)
12 Press Enter to bypass the Allow In-Transit Receipts field.
13 In the Warehouse Restriction Flag field, key in I for Inbound, O for Outbound or B for Both and press 
Enter or press Enter with the field blank for no warehouse restriction.
14 Press Enter the required number of times to bypass the remaining fields on this screen.

Depositor Shipping & Receiving Profile
15 Repeat the above steps to add another depositor shipping & receiving profile or click on Return to Main 
and then Exit to exit the program.
Telephone List Types (TETP)
PREREQUISITES: None
ATTACHED TO: TELE (Telephone Numbers)
CARR (Carriers)
CUST (Customer Code)
SHIP (Shippers)
CONS (Consignees)
SOLD (Sold-To Codes)

CUSTOMER SETUP
Telephone List Types (TETP)
OVERVIEW
In this program you set up your telephone types. A telephone type is any identifying information you wish to 
attach to one or more telephone numbers belonging to a carrier, customer, consignee or shipper. Telephone 
types can identify the type of number (for example, FAX, PAGE and MODM), the department to which they 
belong (for example, CS for Customer Service and TRAF for Traffic) or any other important information (for 
example, HOME, MAIN, etc.).
Once set up, telephone types allow you to identify at a glance any telephone number listed in the CUST, 
CARR, CONS and SHIP programs.
Telephone types can also be used to print the name of a designated individual on an invoice or bill of lading 
(for example, ATTN: JIM SMITH). This capability requires special programming by HighJump.
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

CUSTOMER SETUP
Billing Terms (TERM)

Telephone Types
3 If you need to set up another telephone type, click on Create Record.
4 Key in a telephone type code and press Enter.
5 Key in a meaningful description and press Enter.
6 Repeat steps 4 and 5 to add another telephone type or click on Return to Main and then Exit to exit.
Billing Terms (TERM)
OVERVIEW
In this program, you set up your different terms of payment for your customers. Your terms of payment will 
depend on the way in which you wish to invoice them (for example, the invoice is due on receipt, within x days 
of receipt, etc.). The billing terms that you create in TERM will be later attached to your billing profile(s) in 
DBIP. Billing terms will be printed on all AccellosOne 3PL invoices.
AccellosOne 3PL supports a number of different invoicing options:
PREREQUISITES: None
ATTACHED TO: DBIP (Depositor Billing Profile) --> CUST
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You must know the billing terms and the discount percentage (if any) that 
you offer your customers

CUSTOMER SETUP
Billing Terms (TERM)
▪ you can invoice in installments with each installment assigned a percentage of the total invoice
▪ if invoicing by installment, each installment can be the same percentage of the total invoice or a different 
percentage of the invoice
▪ you can set the number of days from the receipt date that the invoice is due
▪ you can offer a percentage discount on the total invoice if payment is received within a given number of 
days
If you do not use AccellosOne 3PL to generate invoices or gather billing information, you do not need billing 
terms. Set up one billing term code called NA (Not Applicable) and use the following values:
Installment = 1
Percentage of Invoice = 100
Invoice Due After X Days = 1
Discount Percentage = 0.00
Discount Good for X Days = 0
FIELD DESCRIPTIONS
Term Mandatory
Your billing term code. For example, REC for Upon Receipt or 30D for 30 
days.
Description Mandatory
Your description.
Installment Number Mandatory
The number of the installment. If there are no installments (that is, the full 
amount is due), create a single installment.
Percentage of Invoice Mandatory
The percentage of the invoice that you wish to assign to that installment. If you 
are setting up multiple installments, you can specify a different percentage for 
each installment. If you are setting up a single installment, use 100 as your 
percentage.

CUSTOMER SETUP
Billing Terms (TERM)
PROCEDURE
1 Enter TERM.
2 Click on Enter Criteria then Execute Query to see which billing terms have already been set up.
Invoice Due After X Days Mandatory
The number of days from the receipt date that the invoice is due. If you are 
setting up an NA billing term, use the number 1.
Discount Percentage Mandatory
The discount percentage (if any) for the installment if the customer pays within 
a specified time period. If there is no discount percentage, use the default 
value of 0.00.
Discount Good for X 
Days
Mandatory
The number of days that the discount is good for. If there is no discount percentage, use the value 0.
EXAMPLES
Installment Number Percentage of Invoice Invoice Due After X Days Discount Percentage Discount Good for X Days
1 100 5 0.00 0
Example 1 — a single invoice payable in 5 days with no discount
Installment Number Percentage of Invoice Invoice Due After X Days Discount Percentage Discount Good for X Days
1
2
60
40
5
15
0.00
0.00
0
0
Example 2 — 2 installments with the first one (60%) payable in 5 days and the second one (40%) payable in 15 
days
1
2
60
40
15
30
5.00
0.00
5
0
Example 3 — 2 installments with the first one (60%) payable in 15 days with a 5% discount if paid within 5 days and the second one 
(40%) payable in 30 days with no discount
FIELD DESCRIPTIONS

CUSTOMER SETUP
Billing Terms (TERM)
3 If the billing terms for your customers have already been set up, click on Exit to exit. There is no need to 
add any new billing terms to TERM. If the billing terms have not been set up, click on Create Record.
4 Key in a code to describe the billing term (for example, REC = Upon Receipt or 30D = 30 Days) and 
press Enter.
5 Key in a meaningful description for the new term and press Enter.
6 Key in your installment number and press Enter. If there is a single installment, use the number 1.
7 Key in a value for the percentage of invoice and press Enter. 
8 Key in the number of days and press Enter. The number of days is the number of days from the receipt 
date that the invoice is due.
9 If required, key in a discount percentage and press Enter or press Enter to accept the default value of 
0.00. 
10 If you entered a discount percentage in the previous step, you must specify the number of days that the 
discount is good for. Key in this value and press Enter. 
11 If you have a second installment to enter, repeat the above steps for installment 2. 

Billing Terms showing two installments
12 When you finish entering all your installments, click on Return to Main to exit create mode. Then click on 
Master Block and Exit to exit the program.

CUSTOMER SETUP
Holidays (HOLI)
Holidays (HOLI)
OVERVIEW
In this program, you set up your holidays for billing purposes. If you select the Skip Holidays option in DBIP, 
AccellosOne 3PL will automatically bypass renewal billing for the dates entered in this program and bill on the 
date following the holiday. Should you wish to renew inventory on the holiday, do not set up the date in HOLI.
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

CUSTOMER SETUP
Depositor Billing Profile (DBIP)

Holidays
3 If the holidays that you require have already been set up, click on Exit to exit. There is no need to add 
any new holidays to HOLI. If the holidays that you require have not been set up, click on Create Record.
4 Key in your holiday code and press Enter.
5 Key in the date and press Enter.
6 If you have a second holiday to enter, repeat the above steps for your second holiday.
7 When you finish entering all your holidays, click on Return to Main and then Exit to exit.
Depositor Billing Profile (DBIP)
PREREQUISITES: CURR, TERM
ATTACHED TO: CUST (Customer Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You will need to know how your customers are invoiced

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
OVERVIEW
In this program, you specify the type of invoicing you wish to set up for a customer. There are four invoicing 
options available depending on the number of invoices that you wish to generate and the charges that you 
wish to place on these invoices:
In DBIP you also specify:
▪ your billing terms for the customer
▪ your renewal day options
▪ the rate that you wish to charge on renewals
▪ your maximum or minimum charges per invoice, if any, for receipt, renewal and accessorial charges
If your billing is identical for all your customers, you can set up a single profile and attach this profile to each 
customer. However, if certain customers have special billing terms, you will need to set up multiple billing 
profiles. If you do not use AccellosOne 3PL for billing, set up one billing profile called NA.
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

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Term Code (TERM) Mandatory
The billing terms for this profile.
Cost Entry N = No
Y = Yes
If you select Yes, you can enter costing charges against an invoice in CTIN 
(Cost Tracking in Invoice).
Charge Interest N = No
Y = Yes
Set to No. Yes flag reserved for future use.
Check Credit Limit Only available if you use the cash posting system
N = No
Y = Yes
If you set this flag to N for No, no credit limit check will be performed in ENOR. 
If you set this flag to Y for Yes, AccellosOne 3PL will compare the total of all 
outstanding invoices for a given customer against the customer’s credit limit. If 
the total of all outstanding invoices is equal to or greater than the customer’s 
credit limit, you will not be able to create an order for that customer in ENOR.
Credit Limit Only available if Check Credit Limit flag is set to Y for Yes and if you use the 
cash posting system
The depositor billing profile’s credit limit.
Send Statement N = No
Y = Yes
Set to No. Yes flag reserved for future use.
Single Level Billing See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Include Day on Renewals N = No
Y = Yes
This flag governs whether transactions occurring on the renewal date are 
included in the current billing cycle or assigned to the next billing cycle.
If you set this flag to No, transactions that occur on the renewal date will NOT 
be included in the current billing cycle. You use the No option when you wish 
to bill on the opening balance of the billing cycle.
EXAMPLE (monthly first of month billing)
You receive 80 cases of product on March 15 and ship out 20 cases on April 
1. The April 1 transaction is NOT included in the current billing cycle and you 
bill your customer for 80 cases, which is the closing balance for March; the following month, if there are no more transactions, you will bill your customer for 
the 60 remaining cases (80 minus 20).
If you set this flag to Yes, transactions that occur on the renewal date (that is, 
up to 11:59 pm on that date) will be included in the current billing cycle. You 
use the Yes option when you wish to bill on closing balance of the billing cycle.
EXAMPLE (monthly first of month billing)
You receive 80 cases of product on March 15 and ship out 20 cases on April 
1. The April 1 transaction is included in the current billing cycle and you bill 
your customer for 60 cases (80 minus 20).
NOTE For this option, you should generate and confirm your renewal 
batch the day after the current billing cycle.
Renew on Day A = Any day
H = Skip holidays (requires setup in HOLI)
W = Skip weekends
S = Skip both
This field allows you to specify whether there are any holidays or special days 
to be skipped when determining the renewal day. For example, if a product is 
to renew on Saturday or Sunday and you specify the Skip Weekends option, 
the product will renew on the following Monday.
If you select the Any day option, product will renew on any day including 
weekends and holidays.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Original / Current Rate on 
Renewals
C = Current
I = Initial Original
R = Renewal Original
If you select Current, the current renewal storage rate will be charged for 
renewals even if the current rate differs from the rate in effect when the product was received. If you select Initial Original, the initial storage rate defined in 
IISP when the product was received will be charged for renewals. If you select 
Renewal Original, the renewal storage rate defined in IRSP when the product 
was received will be charged.
EXAMPLE
A billing entity was first received on Jan. 1 for 1,000 cases. The initial and 
renewal storage rates were as follows and no product was shipped out of the 
warehouse in January and February.
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
On Feb. 1, AccellosOne 3PL will charge $0.3 per case. On Mar. 1, AccellosOne 3PL will charge $0.5 per case, the current rate in IRSP.
Original / Current Rate on Renewals = Renewal Original
On Feb. 01, AccellosOne 3PL will charge $0.3 per case. On Mar. 1, AccellosOne 3PL will charge the same amount — $0.3 per case. The rate change in 
March has no effect on the rate charged.
Original / Current Rate on Renewals = Initial Original
The rate of $0.7 per case defined in charge code A attached to IISP will be 
charged on Feb. 1 and Mar. 1.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Rate Qualifier B = Balance (only available if previous field set to C for Current)
O = Original
In this field, you specify which amount — either the balance or the original — 
you wish to use to determine your per rate. If you select Balance, AccellosOne 
3PL will qualify on the balance as of the renewal date and apply the current 
rate to the balance. If you select Original, AccellosOne 3PL will qualify on the 
original amount received and apply the appropriate rate to the original 
amount.
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
You receive 35,000 pounds and on renewal day you have 6,000 pounds left. If 
you select Original, AccellosOne 3PL will qualify on the original amount 
(35,000 pounds) and apply the appropriate rate (.70 or .75 per CWT). If you 
select Balance, AccellosOne 3PL will qualify on the balance (6,000 pounds) 
and apply the rate for 6,000 pounds — either .90 per CWT or .95 per CWT.
NOTE If you do not have multiple weight breaks in your rates, AccellosOne 
3PL will always qualify on the original amount.
Send Invoices to C = Customer
P = Paying Office
In this field you specify where you want the invoice sent to. If the customer is 
paying for his own storage, set this field to C.
If a third party is paying for storage, set this field to P. Then refer to the 
Account Type field in CUST (Customer Code) for further instructions. 
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Tax Code Mandatory
GST (GST Only)
GST1 (GST and PST)
GST2 (PST on GST)
HST (HST Only)
None
PST (PST Only)
The taxes, if any, that apply to this profile. With GST1, the GST (Goods and 
Services Tax) and PST (Provincial Sales Tax) are calculated separately and 
added to the invoice total. With GST2, however, the GST is calculated first 
and added to the invoice total. Then the PST is calculated based on the 
invoice total including the GST.
Rate Receipt AutomaticallyY = Yes
N = No
If you set this field to Yes, when the receipt is confirmed AccellosOne 3PL will 
automatically generate any receipt charges that are applicable. If you set this 
field to No, confirmation of the receipt will not generate any receipt charges. 
You will be required to go into RCRA (Receipt Rater) and rate the receipt manually.
If you do not use AccellosOne 3PL to generate invoices and track revenue, 
set this field to N for No.
Invoice Printing Profile 
Code
IND generates a warehouse receipt invoice for initial storage and handing 
charges, an accessorial invoice for accessorial charges and a renewal invoice 
for renewal storage charges
UALL generates one accessorial invoice for all charges
UREC generates an accessorial invoice for initial storage, handling and 
accessorial charges and a renewal invoice for renewal storage charges
UREN generates a warehouse receipt invoice for initial storage and handling 
charges and an accessorial invoice for accessorial and renewal storage 
charges
Renewal Summarization 
Code
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
Reserved Quantity Optional
See “Exceed Daily Average Billing” in the Billing and Invoicing Guide.
Minimum / Maximum 
Receipt Charge Code 
(CHAR)
Optional
See the Billing and Invoicing Guide.
Minimum / Maximum 
Renewal Charge Code 
(CHAR)
Optional
See the Billing and Invoicing Guide.
Minimum / Maximum 
Accessorial Charge Code 
(CHAR)
Optional
See the Billing and Invoicing Guide.
Threshold Accessorial 
Charge Code (CHAR)
Optional
See the Billing and Invoicing Guide.
Alternate Billing Group 
Code (ITAS)
Optional
This field allows you to group items for billing purposes; that is, you can bill a 
customer for a number of items comprising an entire product line rather than 
each item individually. Alternate billing applies to renewal storage only. See 
“Alternate Billing Groups” in the Billing and Invoicing Guide for further information.
Surcharge fields Optional
See “Surcharges” in the Billing and Invoicing Guide.
Renewal Invoice by 
Receipt
Optional
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Billing Profile (DBIP)
PROCEDURE
1 Enter DBIP.
2 Click on Enter Criteria then Execute Query to see which billing profiles have already been set up.
3 If you need to set up another billing profile, click on Create Record.
4 Key in a billing profile code and press Enter.
5 Key in a meaningful description and press Enter.
6 If you wish to change the default currency code, use your pick list to select the appropriate currency. To 
select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the 
pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
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
Weekends or S for Skip Both) and press Enter. If you specify a value other than All, AccellosOne 3PL will 
skip weekends and/or holidays when calculating renewal storage.
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
Create Renewal Invoice 
at Zero Inventory
See “Monthly Renewal Invoicing” in the Billing and Invoicing Guide.
Renewal Calculation by 
OPID
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Depositor Alternate Sorts (DEAS)
17 If prompted to do so, key in the appropriate rate qualifier value (O for Original or B for Balance) in the 
Rate Qualifier field and press Enter.
18 In the Send Invoice to field, select either C for Customer (the most common) or P for Paying Office and 
press Enter.
19 Use your pick list to select the appropriate tax code.
20 In the Rate Receipt Automatically field, select Y for Yes or N for No and press Enter.
21 Select the appropriate invoice printing profile code (IND, UALL, UREC or UREN) and press Enter.

Depositor Billing Profile screen
22 Press Enter to bypass the Renewal Summarization Code field.
23 Press Enter four times to bypass the Minimum / Maximum Receipt Charge Code, the Minimum / Maximum Renewal Charge Code, the Minimum / Maximum Accessorial Charge Code and the Threshold 
Accessorial Charge Code fields.
24 If required, key in an alternate billing group code and press Enter or press Enter to bypass this field.
25 Press Enter to bypass the remaining fields in DBIP.
26 Click on Return to Main and then Exit to exit.
Depositor Alternate Sorts (DEAS)
PREREQUISITES: None
ATTACHED TO: CUST (Customer Code)

CUSTOMER SETUP
Depositor Alternate Sorts (DEAS)
OVERVIEW
In this program, you define your alternate reporting type codes. These codes are used by the program SALE 
(12-Month Sales Report) and certain custom reports to generate consolidated inventory reports showing all 
product of a specific type regardless of customer. For example, if you have seven meat customers and you 
want to run an inventory report for these seven customers, the report will tell you how much beef, pork and 
chicken you have in your warehouse.
The codes that you create in this program can be either single level or double level. For example, if you 
create a code for ICE CREAM, this is considered a single-level code. If, however, you want to track both ice 
cream in general and particular flavours of ice cream, you would have to break down your ICE CREAM code 
into VANILLA, CHOCOLATE and STRAWBERRY. This is considered a double-level code.
The codes that you create in this program are attached to the Reporting Block in CUST. When you run the 
appropriate inventory report and specify an alternate reporting type code, all items belonging to the 
customers to whom you have attached that code in CUST will be included in the report.
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
If you are creating a single-level code, this code will be identical to the code 
that you entered in the Alternate Customer Reporting Type field. If you are 
creating a double-level code (for example, ICE CREAM/ VANILLA), you enter 
your second level — VANILLA — in this field. 
Description Mandatory
Your description for the code.

CUSTOMER SETUP
Depositor Alternate Sorts (DEAS)
PROCEDURE
1 Enter DEAS.
2 Click on Enter Criteria then Execute Query to see which alternate reporting type codes have already 
been set up.
3 If you need to set up another code, click on Create Record.
4 Key in your alternate reporting type code and press Enter.
5 Key in a meaningful description and press Enter.
6 When the Reporting Codes window appears, do one of the following:

Depositor Alternate Sorts Detail Block showing double-level codes
7 When you finish entering your second-level codes for this reporting type, click on Return to Main and 
then Exit to exit.
If you are creating a single-level 
code:
If you are creating a double-level 
code:
a) Key in the same code and 
description that you entered in 
the Main Block and press Enter 
after each entry.
b) Click on Return to Main to exit 
create mode. Then click on Master Block and Exit to exit the program. 
c) The Main Block and the Detail 
Block will be identical.
a) Key in your second code and a 
meaningful description and press 
Enter after each entry.
b) Repeat the above step for each 
additional second-level code that 
you wish to add.

CUSTOMER SETUP
Customer Setup (CUST) — Basic
Customer Setup (CUST) — Basic
OVERVIEW
In this program, you set up your main customer record. A customer in AccellosOne 3PL is a company that 
owns the goods being stored in the warehouse and pays for their storage. 
In CUST you take the profiles and codes that you have set up in the previous programs and attach them to 
your customers. You can also set up certain options such as which inventory level you wish to reserve at 
during order allocation and which default unit of measure you wish to use for entering receipts, orders and 
adjustments.
The profile fields in CUST are mandatory and once you attach a particular profile to a customer, it can only be 
changed by HighJump. The optional fields, on the other hand, such as reserving inventory levels and setting 
default units of measure can be changed as required.
PREREQUISITES: ZIPO, GLCH, DBIP, DSRP, FLPR, SAPE, CUSE, DILP, DIFP, DITP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You will need complete information on your customer — full address, 
salesperson, customer service representative, etc.

CUSTOMER SETUP
Customer Setup (CUST) — Basic
FIELD DESCRIPTIONS
Customer Code Mandatory
Enter a unique code for your customer. For example, if your customer were 
ABC Supplies, you could use the first three characters of the first name and 
the first three characters of the last name to make up a code of ABCSUP.
A customer code can consist of any combination of numbers or letters up to 
ten characters in length. Please note the following restrictions on special characters:
▪ The single quote (’) and double quote (") special characters are not valid 
and should never be used. 
▪ Special characters such as “&”, “%” and “_” may cause problems in certain 
programs and are not recommended. 
▪ The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used.
▪ Other special characters are generally supported.
CAUTION If you are setting up a test customer, the test customer code 
should always be longer than any live customer codes that are similar. For 
example, if your live customer code is ABCSUP, you should use ABCSUPT1 
as your test company code. If you use ABC as your test customer code, you 
could purge old data by mistake for both ABC and ABCSUP.
Name Mandatory
The full name of the customer as you would like it to appear on invoices, bills 
of lading, etc.
Extendable Name This is an overflow field for the Name field when the customer name exceeds 
30 characters.
Address 1 Mandatory
The customer’s street address. This address will print on all documents unless 
you specify a Paying Office Code as explained further in this section.
Extendable Address 1 This is an overflow field for the Address 1 field when the address 1 exceeds 
30 characters.

CUSTOMER SETUP
Customer Setup (CUST) — Basic
Address 2/3/4 Optional
Additional lines for the customer’s street address. This address will print on all 
documents unless you specify a Paying Office Code as explained further in 
this section.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (Zip/Postal Code), the city, state/province and 
country will be filled in by the system.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Salesperson Code 
(SAPE)
Mandatory
The salesperson responsible for the account.
Customer Service Representative (CUSE)
Mandatory
The customer service representative responsible for the account.
Start Business Date Enter 01.01.01. This date will allow you to backdate any receipts for a customer in ENRE. If you enter the current date, you will not be able to backdate 
receipts.
G. L. Modifier Code 
(GLMO)
Optional
If you are using general ledger modifier codes to track revenue by customer, 
enter the GL modifier code for this customer that you created in GLMO.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
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
This account type is for customers that are billed only and have no inventory 
to be tracked (for example, a customer who is renting office space or is shipping and/or receiving goods belonging to another customer).
If you create an invoice only customer, you will not be able to proceed past the 
Billing Profile Code field.
Broker
See the “Broker Orders” section in the Operations 1 Guide for full instructions 
on setting up a broker.
Billing Profile Code 
(DBIP)
Mandatory
The billing profile specifying the type of invoicing for this customer.
Paying Office Code Only available if the Account Type = Warehouse and the Send Invoice To field 
in DBIP is set to P for Paying Office
This field is only used for customers with inventory but no billing because all 
billing is sent to a third party. See the Billing and Invoicing Guide for full 
instructions.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
UPC Prefix Optional
This field is used to attach a predefined UPC prefix (five digits followed by a 
hyphen) to all of a customer’s item codes. The use of the prefix eliminates the 
need to key in the same digits for all items and makes it possible to handle 
UPC codes that are too long for the item code field.
UPC prefixes are typically used for EDI, bar coded labels and special reports 
that are external to the warehouse. This option cannot be activated without 
special customization from HighJump.
Freight Paying Office 
Code (FPAY)
Optional
Only required if you wish to bill a customer’s freight charges to a third party 
when using AccellosOne Transport.
Shipping/Receiving Profile Code (DSRP)
Mandatory
This profile contains your picking profile (set up in PIPR if required) and 
defines how you want to process orders that cannot be fully filled.
Workflow Profile Code 
(DIFP)
Mandatory
This profile defines your inbound and outbound flows or steps for time-stamping and allocation/de-allocation purposes.
If you click on the View Flow Chart icon , you can see a flow chart of your 
profile showing each flow, the documents if any attached to the flow as well as 
any special verify programs.
Inventory Level Profile 
Code (DILP)
Mandatory
This profile defines the number of inventory levels and what these levels are 
called.
Reserve Orders at Level 
Number
RF only
See the reserve logic section in the Allocation and Wave Manager Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
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
This profile defines the weight measure that you wish to use when looking up 
the total weight shown on the receipt and order headers as well as the default 
linear measure code for cube reporting in the Wave Report and other interfaces.
EDI Profile Code Optional
See the EDI section in the Operations 2 Guide.
Freight Profile Code 
(FRCP)
AccellosOne Transport only
TMS Interchange QualifierFor HighJump use only
TMS Interchange ID For HighJump use only
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
Default SKU for Receipt 
Entry
H = High
L = Low
In this field, you define how you want AccellosOne 3PL to interpret quantities 
in ENRE when the SKU type is not specified. This flag works in conjunction 
with the Receipt Process field in IQBP for each SKU type in an item’s quantity 
breakdown.
Consider the following example: the item has a quantity breakdown of pallet/
case/each
Receipt Process flag in IQBP for pallets = Y for Yes
Receipt Process flag in IQBP for cases = Y for Yes
Receipt Process flag in IQBP for eaches = N for No
If you enter H for High in CUST and if you enter a quantity of 50 units in 
ENRE, the 50 units will be considered to be 50 pallets. If, on the other hand, 
you enter L for Low in CUST, the same receipt of 50 units would be recorded 
by the system as 50 cases. You cannot receive 50 eaches because the 
Receipt Process flag in IQBP for eaches has been deactivated.
You can manually override the default SKU type in ENRE.
Default SKU for Order 
Entry
H = High
L = Low
The same logic as the Default SKU Receipt Entry field but applies to order 
entry.
Default SKU for Adjustment EntryH = High
L = Low
The same logic as the Default SKU Receipt Entry field but applies to the entry 
of adjustments.
Extra Charge Profile 
Code (ECHP)
See the Billing and Invoicing Guide for further information.
Voice Profile Code 
(VOPC)
Only required for voice-activated picking
The customer’s voice profile (customer).
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
Warehouse Code 
(WARE)
Optional
The default warehouse code for the customer’s product when assigning locations to receipt lines in ENRE. If you specify a warehouse code in ILOP, the 
receipt header or a receipt line, that warehouse code will override the warehouse code in this field.
Conveyance Number Reserved for future use
Transfer Profile Code 
(TRPR)
Optional
This profile is used if you wish to transfer product from one customer to 
another within your warehouse.
RF Profile Code (MRFP) Optional
This profile is used to set up your RF options.
RFID Partition Reserved for future use
RFID Company Prefix Reserved for future use
Customer EDI Partner ID See the EDI section in the Operations 2 Guide.
EAN UCC Prefix Optional
The EAN UCC prefix for the VICS bill of lading and UCC-128 label.
EAN UCC Number Code 
(NUSE)
Optional
Your number series for generating UCC-128/SSCC-18 numbers. 
External Reference Number
Optional
You can add any miscellaneous reference information about a customer in this 
field.
Wave Deallocation Rule See Allocation and Wave Manager Guide.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic
PROCEDURE
1 Enter CUST.
2 Key in your customer code and press Enter.
3 Key in the full name of your customer and press Enter.
4 Press Enter to bypass the Extendable Name field.
5 Key in the full address of the customer, pressing Enter at the end of each line.
6 Key in your ZIP/postal code and press Enter. If the code is already in AccellosOne 3PL, the city, state or 
province and country will be filled in automatically. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next 
field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. First 
key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. Then 
key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press 
Enter. You will be brought back into CUST with the appropriate information filled in.
7 In the Salesperson Code field, key in your salesperson code and press Enter or use your pick list to 
select a code. To select a code using a pick list, press F10 to display the pick list and click on Execute 
Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
8 In the Customer Service Representative Code field, key in the code for your representative and press 
Enter or use your pick list to select a code.
9 Key in 01.01.01 as your start business date and press Enter.
Customer Reference 
Code
Special programming by HighJump required.
Unique Level for Pallet ID In this field, you can define which level is the primary conveyance for RFCH, 
RFPIC, RFRL and RFMG. For example, suppose a given item has four inventory levels with level 3 being Pallet ID and Level 4 being serial number. If you 
can scan level 3 (Pallet ID), all the serial numbers will be automatically associated with the level 3 that you scanned.
Automatic Billing PreRenewalSee the Billing and Invoicing Guide.
Employee ID Number Reserved for future use
Status A = Active
D = Deactivated
If a customer is active, you can ship and receive product from that customer. If 
a customer is deactivated, you can ship existing product from that customer 
but you cannot receive new product from the customer.
FIELD DESCRIPTIONS

CUSTOMER SETUP
Customer Setup (CUST) — Basic

Customer Code
10 If you are using the general ledger modifier function, use your pick list to select the code that you created 
in GLMO for this customer.
11 Press Enter to bypass the Labor Capture Job Level Flag field.
12 Press Enter again to bypass the Labor Standard Modifier field.
13 Key in your account type code (W for Warehouse or I for Invoice Only) and press Enter.
14 Use your pick list to select the billing profile code that you created in DBIP. If you selected an Invoice 
Only account type, you will not be able to proceed past this field and will have to click on Return to Main 
and Exit to exit.
15 Press Enter to bypass the UPC Prefix field.

CUSTOMER SETUP
Customer Setup (CUST) — Basic

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
CAUTION Make sure that you select your profiles carefully. Once you attach a 
profile to a customer, it cannot be removed without special programming by 
HighJump. 

CUSTOMER SETUP
Customer Setup (CUST) — Basic

Customer Code
24 Press Enter to bypass the EDI Profile Code field.
25 Press Enter to bypass the Freight Profile Code field.
26 Press Enter twice to bypass the TMS Interchange fields.
27 Press Enter to bypass the Extra Charge Profile field.
28 Press Enter again to bypass the Voice Profile Code field.
29 If required, key in a warehouse code in the Warehouse Code field and press Enter or press Enter to 
bypass this option.

CUSTOMER SETUP
Customer Setup (CUST) — Advanced

Customer Code screen showing prompt for default SKU for receipt entry
30 If required, change the default values in the Default SKU Receipt Entry, Order Entry and Adjustment 
Entry fields or press Enter to bypass these fields.
31 Press Enter to bypass the Conveyance Number field.
32 Press Enter the required number of times to bypass the Transfer Profile Code, RF Profile Code, RFID 
Partition, RFID Company Prefix, Customer EDI Partner ID and EAN UCC Prefix fields.
33 If required, key in miscellaneous reference information in the External Reference Number field and press 
Enter. If you do not require miscellaneous reference information, press Enter to bypass this field.
34 When the Receiving Block is displayed, click on Return to Main and then Exit to exit.
Customer Setup (CUST) — Advanced
PREREQUISITES: TETP, CARR, CUST, DEAS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional

CUSTOMER SETUP
Customer Setup (CUST) — Advanced
OVERVIEW
This chapter describes the more advanced features of CUST. 
▪ Receiving Block
▪ Shipping Block
▪ Reporting Block
▪ Telephone Block
▪ Carrier Block
RECEIVING BLOCK
The Receiving Block displays the inventory levels for your customer. The sequence in which the levels are 
displayed determines the sequence in which you will enter inventory in the receiving program (ENRE). 
For example, if your inventory levels are set up as follows:
Level 1 = Item
Level 2 = Lot
AccellosOne 3PL will prompt you to enter your item code first in ENRE and then your lot number.
You can change the order in which you receive inventory at any time by changing the order of your inventory 
levels in the Receiving Block.

Receiving Block
To change the order of your inventory levels:
1 Enter CUST.
2 Retrieve the customer whose inventory levels you wish to resequence.
3 Click on Receiving Block.
OTHER REQUIREMENTS:

CUSTOMER SETUP
Customer Setup (CUST) — Advanced
4 Change the numbers in the Level column to reflect the order in which you wish to receive your inventory 
and press Enter after changing each number.
For example, if your current order is:
Item = 1
Lot = 2
you would change Item to 2 and Lot to 1 in order to receive the lot before the item.
5 Click on Master Block and then Exit to exit.
SHIPPING BLOCK
The Shipping Block works in the same way as the Receiving Block. By changing the order of your inventory 
levels in this block, you change the order in which you enter inventory in ENOR. This feature is only available 
for P-type order lines.
REPORTING BLOCK
This block is used by the program SALE (12-Month Sales Report) and certain custom reports to group 
customers with similar product and generate consolidated inventory reports containing all products for a 
number of customers. For example, if you have seven meat customers and you want to run an inventory 
report for these seven customers, the report will tell you how much meat you have in your warehouse (a 
single-level code) or how much beef, pork and chicken you have in your warehouse (a double-level code).
When you run the appropriate inventory report and select an alternate reporting type code, all customers to 
whom you have attached that code in the Report Block in CUST will be included in the report.

Reporting Block showing two alternate reporting types — COOK (a single-level code) and MEAT (a 
double-level code)
To add an alternate reporting type code to the Reporting Block:
1 Enter CUST.
2 Retrieve the customer for whom you wish to add an alternate reporting type.
3 Click on Receive Block, Shipping Block and then Report Block.

CUSTOMER SETUP
Customer Setup (CUST) — Advanced
4 If you are not in Create Mode, click on Create Record.
5 In the Type field, use your pick list to select the appropriate alternate reporting type (first level) that you 
created in DEAS. Then press Enter to advance to the next field.
6 In the Code field, use your pick list to select the appropriate alternate reporting type (second level) that 
you created in DEAS and then press Enter to advance to the next line. If there is no second level code, 
key in the same code that you used in the previous step and press Enter.
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
5 In the Telephone List Code field, use your pick list to select the appropriate telephone type. To select a 
code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list 
codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
6 Key in the telephone number and press Enter.
7 Key in the name of the contact person and press Enter.

CUSTOMER SETUP
Customer Setup (CUST) — Advanced
8 If required, key in the person’s position and press Enter. If you do not need the person’s position, press 
Enter to bypass this field.
9 Key in another line or click on Return to Main to exit create mode. Then click on Report Block, Shipping 
Block, Receive Block, Master Block and Exit.
CARRIER BLOCK
This block allows you to list in order of preference the carriers that you wish to use for this particular customer. 
This listing is for reference purposes only; it does not modify the order of carriers during order or receipt entry. 
If you have not set up your carriers yet in CARR, you cannot enter a listing of preferred carriers at this time. 
When you set up your carriers in CARR, you can return to CUST and complete the Carrier Block.

CUSTOMER SETUP
Customer Setup (CUST) — Advanced

CHARGE AND RATE SETUP
General Ledger Chart of Accounts (GLCH) .................................................. 158
Currency Codes (CURR)................................................................................. 160
Bank Code (BANK).......................................................................................... 162
General Ledger Modifier Code (GLMO)......................................................... 164
Revenue Group Codes (REGR)...................................................................... 169
Revenue Analysis Codes (REVA) .................................................................. 170
Invoice Types (INTP)....................................................................................... 173
Charge Codes (CHAR) .................................................................................... 174
Depositor Billing Rates (RATE) ..................................................................... 185

CHARGE AND RATE SETUP
General Ledger Chart of Accounts (GLCH)
General Ledger Chart of Accounts (GLCH)
OVERVIEW
In this program, you set up your general ledger accounts in AccellosOne 3PL. The accounts that you set up in 
GLCH should be identical to the accounts that you use or will be using in your accounting system to track 
warehouse revenue. You can set up accounts to capture revenue by various buckets such as division, 
customer, warehouse, etc. and within these buckets can record revenue by type of charge — for example, 
storage, handling, accessorial and renewals. If required, you can also set up accounts for taxes.
The accounts that you set up in GLCH are attached to specific charge codes in CHAR and these charge 
codes are then attached to specific divisions, customers, items, charges, etc. During the billing cycle in AccellosOne 3PL, the revenue generated is posted to the appropriate account.
Accounts set up in GLCH are not activated until they are linked to a particular charge code in CHAR. If you 
create an account in GLCH but do not link it to a charge code, the account will not be active and no revenue 
will be posted to it.
If you do not use AccellosOne 3PL to generate invoices or gather billing information, you do not need to set 
up a chart of accounts. 
PREREQUISITES: None
ATTACHED TO: CHAR (Charge Codes)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you use AccellosOne 3PL to gather billing information or 
generate invoices
OTHER REQUIREMENTS: You must have a list of your chart of accounts
NOTE If AccellosOne 3PL is linked to your accounting system, you can use your 
general ledger accounts to track revenue by company/division, customer and warehouse location. Refer to the program GLMO (General Ledger Modifier Code) for 
instructions before setting up your GL accounts.
FIELD DESCRIPTIONS
General Ledger Code Mandatory
Your general ledger account number.

CHARGE AND RATE SETUP
General Ledger Chart of Accounts (GLCH)
PROCEDURE
1 Enter GLCH.
2 Key in your general ledger code and press Enter.
3 Key in your description and press Enter.
4 Press Enter three times to bypass the G/L External Reference 1, G/L External Reference 2 and Status 
fields.
5 Repeat the above three steps for each additional general ledger code that you wish to add.

General Ledger Chart of Accounts
6 When you finish adding your codes, click on Return to Main and then Exit to exit.
Description Mandatory
Your account description.
G/L External Reference 1 Special programming by HighJump required.
G/L External Reference 2 Special programming by HighJump required.
TIP You do not need to set up a separate general ledger account for each charge 
that you wish to track. Instead, you can use revenue analysis codes defined in REVA 
to track each charge at whatever level of detail you require. The advantage of using 
REVA for this function is its enhanced reporting capabilities, which allow you to generate reports for only those charges that interest you.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Currency Codes (CURR)
Currency Codes (CURR)
OVERVIEW
In this program, you set up your currency code(s). If multi-currency billing is NOT activated on your system, 
you set up a single currency code for all your customers and attach it to your depositor billing profile(s) in 
DBIP. The single currency code that you set up in CURR does not print on any AccellosOne 3PL invoice 
document or report.
If, on the other hand, multi-currency billing is activated on your system, you set up a record in CURR for each 
currency that you wish to use. As well, you define your exchange rates in CURX (Currency Exchange Rates). 
Currency codes in a multi-currency billing environment DO print on most invoice documents and sales 
reports.
PREREQUISITES: GLCH
ATTACHED TO: DBIP (Depositor Billing Profile)
CURX (Currency Exchange Rates)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Currency Code Mandatory
Your code for this currency.
Description Mandatory
Your description for this currency.
Value to Base Currency Mandatory
Set to 1.

CHARGE AND RATE SETUP
Currency Codes (CURR)
PROCEDURE
1 Enter CURR.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
3 If you need to set up another code, click on Create Record.
4 Key in your currency code and press Enter.
5 Key a description for your code and press Enter.
6 In the Value to Base Currency field, key in 1 and press Enter.
7 Press Enter to bypass the Realized Exchange G.L. Account field.
8 In the Trade G.L. Account field, key in the dummy account number that you created in GLCH and press 
Enter.
Realized Exchange G. L. 
Account
Reserved for future use
Trade G. L. Account
(defined in GLCH)
Mandatory
Enter the dummy account number that you created in GLCH.
Discount G. L. Account Reserved for future use
Interest G. L. Account Reserved for future use
Trade G. L. Account Reserved for future use
Discount G. L. Account Reserved for future use
Interest G. L. Account Reserved for future use
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Bank Code (BANK)

Currency Codes
9 Press Enter to bypass the remaining G.L. account fields.
10 When you finish entering your currency code(s), click on Return to Main and then Exit to exit.
Bank Code (BANK)
OVERVIEW
In this program, you set up your bank account. If you use multi-currency billing, you must set up one record in 
BANK for each currency.
PREREQUISITES: GLCH, CURR
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you invoice your customers in AccellosOne 3PL
OTHER REQUIREMENTS:

CHARGE AND RATE SETUP
Bank Code (BANK)
PROCEDURE
1 Enter BANK.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
3 If you need to set up another code, click on Create Record.
4 Key in your bank code and press Enter.
5 Key in any number as your bank account number or use NA for Not Applicable and press Enter.
6 Key in your GL account for the bank account and press Enter or use the pick list function (F10) to select 
it.
7 Key in your currency code for the bank account and press Enter or use the pick list function (F10) to 
select it.
8 Click on Return to Main to exit Create Record mode.
FIELD DESCRIPTIONS
Bank Code Mandatory
Your bank code.
Description Mandatory
Your bank code description.
Bank Account Number Mandatory
Key in any number as your bank account number or use NA for Not Applicable.
Bank GL Account 
(defined in GLCH)
Mandatory
Enter the dummy account number that you created in GLCH.
Currency Code (defined 
in CURR)
Mandatory
The currency code for your bank account.

CHARGE AND RATE SETUP
General Ledger Modifier Code (GLMO)

Bank Code
9 Click on Exit to exit.
General Ledger Modifier Code (GLMO)
OVERVIEW
This program allows you to use your general ledger accounts to track revenue by company/division, customer 
and location billing code. If you use this program, you avoid the need to create dozens of charge codes for 
each location billing code, customer, etc. whose revenue you wish to track.
PREREQUISITES: GLCH
ATTACHED TO: LODE (Location Billing Codes)
or
CUST (Customer Setup) 
or
COMP (Company Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: You must have a list of your chart of accounts

CHARGE AND RATE SETUP
General Ledger Modifier Code (GLMO)
You use “wildcard” characters in your general ledger chart of accounts to indicate that certain digits in the 
account number are variables. AccellosOne 3PL supports the following wildcards:
* represents a customer defined in CUST
? represents a location billing code defined in LODE
= represents a company/division defined in COMP
For example, if you set up an account called Handling with the number ***11000, you are indicating that the 
first three digits of the account refer to any customer on your system. Likewise, an account called Renewal 
Storage with the number 100==300 would indicate that the fourth and fifth digits refer to any company or 
division in your warehouse.
The general ledger modifier in GLMO converts these wildcards to the appropriate digit(s) so that your chart of 
accounts shows your exact revenue by customer, company or location billing code.
EXAMPLE 1 — TRACKING INITIAL STORAGE BY COMPANY 
In this example, you wish to track initial storage by company and your GL account for initial storage is XX2100 
where XX is the company number. You have three companies on your system: 01, 02 and 03.
1 In GLCH you create an initial storage GL account numbered ==2100.
2 In GLMO you set up your GL modifier code for each company:
Enter company 01 and create a 01 code in GLMO.
Enter company 02 and create a 02 code in GLMO.
Enter company 03 and create a 03 code in GLMO.
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of ==2100.
4 In COMP (Company Code) you attach the GL modifier code that you created in GLMO to your three companies.
Enter company 01 and attach your 01 GLMO code to it.
Enter company 02 and attach your 02 GLMO code to it.
Enter company 03 and attach your 03 GLMO code to it.
5 Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to 
the appropriate company. At the end of the day, AccellosOne 3PL will generate three Initial Storage 
accounts (012100, 022100 and 032100) showing all charges for that company.
EXAMPLE 2 — TRACKING INITIAL STORAGE BY CUSTOMER 
In this example, you wish to track initial storage by customer and your GL account for initial storage is 
31XX00 where XX is the customer number.
1 In GLCH you create an initial storage GL account numbered 31**00.
2 In GLMO you set up your GL modifier code for each customer:
01 = Customer 1
02 = Customer 2
03 = Customer 3
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of 31**00.
4 In CUST (Customer Setup) you attach the GL modifier code that you created in GLMO (01, 02, 03, etc.) 
to the appropriate customer.

CHARGE AND RATE SETUP
General Ledger Modifier Code (GLMO)
5 Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to 
the appropriate customer. At the end of the day, AccellosOne 3PL will generate three Initial Storage 
accounts (310100, 310200 and 310300) showing all charges for that customer.
EXAMPLE 3 — TRACKING INITIAL STORAGE BY LOCATION BILLING CODE 
In this example, you wish to track initial storage by location billing code and your GL account for initial storage 
is 2100XX where XX is the location billing code.
1 In GLCH you create an initial storage GL account numbered 2100??.
2 In GLMO you set up your GL modifier code for each location billing code:
01 = Location Billing Code A
02 = Location Billing Code B
03 = Location Billing Code C
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of 2100??.
4 In LODE (Location Billing Code) you attach the GL modifier code that you created in GLMO (01, 02, 03, 
etc.) to the appropriate location billing code.
5 Whenever you put-away product into a particular location, the charges are calculated and assigned to 
the appropriate location billing code. At the end of the day, AccellosOne 3PL will generate three Initial 
Storage accounts (210001, 210002 and 210003) showing all charges for that location billing code.
6 If your system consists of two or more global companies, you must perform your GLCH and GLMO setup 
in each global company.
EXAMPLE 4 — TRACKING INITIAL STORAGE BY WAREHOUSE
In this example, you wish to track initial storage by warehouse and your GL account for initial storage is 
31XX00 where XX is the warehouse number.
1 In GLCH you create an initial storage GL account numbered 31**00.
2 In GLMO you set up your GL modifier code for each warehouse:
01 = Warehouse 1
02 = Warehouse 2
03 = Warehouse 3
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of 31**00.
NOTE If your system consists of two or more global companies, you must perform 
your GLCH and GLMO setup in each global company.
NOTE This method only works if your customers are restricted to a single warehouse. If customers can span warehouses, you may have to manually allocate a customer’s revenue to two or more warehouses.

CHARGE AND RATE SETUP
General Ledger Modifier Code (GLMO)
4 In CUST (Customer) you attach the GL modifier code that you created in GLMO (01, 02, 03, etc.) to the 
appropriate customer. For example, if customer A’s product is stored in warehouse 01, you would enter 
01 in the G. L. Modifier field.
Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to the 
appropriate warehouse. At the end of the day, AccellosOne 3PL will generate three Initial Storage accounts 
(310100, 310200 and 310300) showing all charges for that warehouse.
FIELD DESCRIPTIONS
G.L. Modifier Mandatory
Your general ledger modifier number.
Description Mandatory
Your general ledger modifier description.
Substitution Modifier Optional
The substitution modifier allows users to set up new customers, companies 
and location billing codes without the need to know the general ledger chart of 
accounts. For example, suppose you have three facilities in three states (C for 
California, T for Texas and N for Nevada) and two types of customers (F for 
Freezer and D for Dry).
Your staff could use codes like CF for a California freezer customer and TD for 
a Texas dry customer when setting up new accounts. AccellosOne 3PL would 
convert these codes to the correct general ledger accounts during billing. If 
you changed your accounts, the same codes — CF, TD, etc. — could point to 
the new accounts, making the change transparent to your staff. 
GL Modifier
CF
TD
NF
Substitution Modifier
01
87
65
NOTE The number of characters in the substitution modifier must match 
the number of wildcard characters. For example, if your GL code is **123, the 
substitution modifier must also be two characters — AB, 01, XY, etc.
Company Reference 
Code
Special programming by HighJump required.

CHARGE AND RATE SETUP
General Ledger Modifier Code (GLMO)
PROCEDURE
1 Enter GLCH and make the necessary changes to your chart of accounts.

GLCH showing the use of wildcards to designate a company
2 Enter GLMO.
3 Key in your GL code and press Enter.
4 Key in a description for your code and press Enter.
5 If required, key in your substitution modifier and press Enter or press Enter with the field blank to bypass 
this option.
6 Press Enter twice to bypass the Company Reference Code and Account Reference Code fields.
7 Repeat the above steps for each additional GL modifier that you wish to add.

General ledger modifier codes for three companies
8 When you finish adding your codes, click on Return to Main and then Exit to exit.
Account Reference Code Special programming by HighJump required.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Revenue Group Codes (REGR)
SETTING UP DESCRIPTIONS FOR WILDCARD ACCOUNTS
If you use wildcard characters in your general ledger accounts to track revenue by company/division, 
customer or location bill code, the description in the daily invoice register for any account containing a 
wildcard character will appear as UNKNOWN. If you wish to see a valid description for your accounts, you 
must set up a separate account in GLCH (GL Chart of Accounts) with the correct description for each 
company/division, customer or location bill code. 
EXAMPLE
In this example, you have two wildcard characters (==) for the company and one wildcard 
character (?) for the location bill code in your general ledger account for renewal storage 
(==?3010). There are two companies in your system (W7 and W8) and two location bill 
codes (code 3 and code 4). You must set up one record in GLCH for each company code/
location bill code combination in addition to your ==?3010 code.

GLMO screen showing four records for each company/location billing code combination
Revenue Group Codes (REGR)
OVERVIEW
In this program, you set up your revenue group codes. Revenue group codes allow you to consolidate two or 
more revenue analysis codes into a single group. Revenue group codes can be printed on invoices and audit 
reports to show all revenue from a group of revenue analysis codes.
PREREQUISITES: None
ATTACHED TO: REVA (Revenue Analysis) --> CHAR
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

CHARGE AND RATE SETUP
Revenue Analysis Codes (REVA)
PROCEDURE
1 Enter REGR.
2 Click on Create Record.
3 Key in your revenue group code and press Enter.
4 Key in your description and press Enter.
5 Repeat the above steps for each additional code that you wish to add.

Revenue Group Codes
6 When you finish adding your codes, click on Return to Main and Exit to exit.
Revenue Analysis Codes (REVA)
FIELD DESCRIPTIONS
Revenue Group Mandatory
Your revenue group code.
Description Mandatory
Your revenue group code description.
PREREQUISITES: REGR

CHARGE AND RATE SETUP
Revenue Analysis Codes (REVA)
OVERVIEW
In this program, you set up your revenue analysis codes. Revenue analysis codes allow you to group two or 
more charge codes in a single category for revenue reporting purposes. For example, you create a revenue 
analysis code of LA for Labor and attach it to the following four charge codes
▪ charge code 1 for miscellaneous labor
▪ charge code 2 for extra help
▪ charge code 3 for lumper rate
▪ charge code 4 for handling inbound damage
When you run the SALE (12-Month Sales Report) or some other sales report, you enter LA as your revenue 
analysis code restriction. AccellosOne 3PL will show only revenue generated through the four charge codes 
to which you have attached your LA revenue analysis code. 
If you do not wish to use revenue analysis in AccellosOne 3PL, you must create a single NA (Not Applicable) 
revenue analysis code. 
ATTACHED TO: CHAR (Charge Code) 
INRE (Invoice Register Definition)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE Revenue analysis codes are for management reporting purposes only; there 
is no need for a one-to-one relationship between these codes and your general ledger accounts. For example, you can have one general ledger account for initial storage and a number of revenue analysis codes to report on storage revenue by each of 
your customers.
FIELD DESCRIPTIONS
Revenue Analysis Code Mandatory
Your revenue analysis code. For example, HA for Handling.
Description Mandatory
Your revenue analysis description.

CHARGE AND RATE SETUP
Revenue Analysis Codes (REVA)
PROCEDURE
1 Enter REVA.
2 Click on Enter Criteria then Execute Query to view which revenue analysis codes have already been set 
up. A minimum of one code (for example, NR for Not Required) is mandatory. 
3 If the codes that you require have already been set up, click on Exit to exit. There is no need to add any 
new codes to REVA. If the codes that you require have not been set up, click on Create Record.

Revenue Analysis Code
4 Key in your revenue analysis code and press Enter.
5 Key in a meaningful description and press Enter.
6 If required, key in your revenue analysis group code in the Revenue Group Code field and press Enter. If 
you do not use revenue analysis groups, press Enter with the field blank to bypass this option.
Revenue Group Code
(defined in REGR)
Optional
If you have set up revenue analysis group codes in REGR, you assign the 
appropriate revenue analysis group code to your revenue analysis code.
True Revenue Y = Yes
N = No
If you select Yes, the revenue will be considered true revenue (that is, money 
paid by your customer that goes to you) and included in your sales reports 
such as SALE (12-Month Sales Report) and BIRR (Billing Renewals Report).
If you select No, the revenue will be considered non-true revenue and will not 
be included in your sales reports. You use non-true revenue to record revenue 
such as a tax remitted to the government or a rebate from the government.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Invoice Types (INTP)
7 In the True Revenue field, key in Y for Yes or N for No and press Enter.
8 Repeat steps 4 to 7 for each additional revenue analysis code that you wish to set up.
9 When you finish setting up your codes, click on Return to Main and then Exit to exit the program.
Invoice Types (INTP)
OVERVIEW
In this program, you set up your invoice types. You use invoice types in the billing program BILB (Billing 
Batch) to restrict the types of charges that will appear on an accessorial invoice or to split out the charges on 
two or more invoices.
For example, you create an invoice type called LABOR CHARGES. Then you attach this invoice type to one 
or more charge codes in CHAR (Charge Codes). When you enter BILB (Billing Batch), you specify in the 
Select Block of this program that you want only charges whose invoice type is LABOR CHARGES to be 
included in the invoice. When generate your accessorial batch, the batch will be restricted to accessorial labor 
charges.
If you do not use AccellosOne 3PL for billing or do not need to restrict certain charges in BILB, you do not 
need invoice types. Create a single invoice type called NA for Not Applicable.
PREREQUISITES: None
ATTACHED TO: CHAR (Charge Code) 
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Invoice Type Mandatory
Your code for this invoice type.
Description Mandatory
Your description for this invoice type.

CHARGE AND RATE SETUP
Charge Codes (CHAR)
PROCEDURE
1 Enter INTP.
2 Click on Enter Criteria then Execute Query to see which, if any, invoice types have already been set up.

Invoice Types
3 Using your arrow keys, go through each record to see which invoice types have already been set up. If 
the types that you require have already been set up, click on Exit to exit. There is no need to add any 
new codes to INTP.
4 If the invoice types that you require have not been set up, click on Create Record. 
5 Key in your new invoice code and press Enter.
6 Key in a meaningful description for your new code and press Enter.
7 Repeat steps 5 and 6 for each additional invoice type that you wish to add.
8 When you finish entering your invoice types, click on Return to Main and then Exit to exit the program.
Charge Codes (CHAR)
PREREQUISITES: GLCH, GLMO, REVA, INTP, SKUS
ATTACHED TO: RATE (Depositor Billing Rates)
IISP (Item Initial Storage Profile)
IRSP (Item Renewal Storage Profile)
IHAP (Item Handling Profile)
DBIP (Depositor Billing Profile)
IBIP (Item Billing Profile)
DILP (Depositor Inventory Level Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory

CHARGE AND RATE SETUP
Charge Codes (CHAR)
OVERVIEW
In this program, you set up standard tariff charge codes for the various rates that you will be using for your 
initial storage, renewal storage, handling and accessorial charges. You should set up a separate charge code 
for each handling charge or additional service for which you have a standard rate (for example, stencilling 
cases, case picking, labelling, sorting, etc.).
CHAR defines four major parameters for your charges:
▪ the type of charge (single break, multiple break, no charge, etc.)
▪ the charge definition (break, flat or combination)
▪ the general ledger account for the charge
▪ the SKU type or unit of measure that the charge is based on (pallets, cases, pounds, etc.)
Once set up, the code that you create in CHAR is attached to RATE (Depositor Billing Rates), which specifies 
the actual rates — that is, the weight breaks, minimum charge, flat rate, the customer to whom the charge 
applies, etc.
You must set up at least one charge code to run AccellosOne 3PL. If you do not use AccellosOne 3PL to 
gather billing information or generate invoices, you use the NC (No Charge) charge code.
CUSTOMER LEVEL VERSUS ITEM LEVEL BILLING
You can set up charges at both the item level and the customer level. At the item level, you attach your charge 
code to IISP (Item Initial Storage Profile), IRSP (Item Renewal Storage Profile) and IHAP (Item Handling 
Profile). These profiles are attached to IBIP (Item Billing Profile), which is then attached to your items in ITEM. 
At the customer level, you can set up certain maximum and minimum charges that apply to an invoice. You 
attach these charge codes to DBIP (Depositor Billing Profile). DBIP is then attached to your customer in 
CUST. 
OTHER REQUIREMENTS: A list of all charges (handling, shrink wrapping, etc.) that can be applied to 
a customer.
NOTE Charge codes should not be customer specific. If you wish to give a special 
rate to a particular customer, you set up one charge code in CHAR (for example, HA 
for Handling) for all customers. Then you enter RATE (Depositor Billing Rates) and 
create two records. The first record contains your standard rates and is attached to 
the customer .ALL while the second record contains your special rates and is 
attached to the customer to whom the special rates apply.

CHARGE AND RATE SETUP
Charge Codes (CHAR)
FIELD DESCRIPTIONS
Charge Code Mandatory
Your charge code. For example, HIN for handling inbound. The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB 
(Billing Batch) and cannot be used in a charge code.
CHAR DBIP
RATE
Customer #1 attached to .ALL rates
Customer #2 attached to .ALL rates
Customer ABC Supplies attached to ABC
Supplies rates
RATE CHAR
CUST
RATE
Customer Code = ABC Supplies
Customer Code = .ALL
Billing at customer level showing two sets of rates
Charge Code = RS1 for Renewal Storage 1
Depositor Billing Rates
Billing at item level showing initial, renewal and handling charges
RATE CHAR
RATE CHAR
IISP
IRSP
IHAP
LODE
IBIP ITEM
Item Billing Profile
Initial Storage Profile
Renewal Storage Profile
Handling Profile

CHARGE AND RATE SETUP
Charge Codes (CHAR)
Description Mandatory
Your charge code description.
Reference Optional
If required, you can add reference information to your charge code; for example, all your handling charge codes could have “Handling” as their reference. 
Special programming by HighJump is required if you wish to print this information on a document or capture it for EDI purposes. 
External Reference Special programming by HighJump required.
Charge Type Code Refer to the Billing and Invoicing Guide for charge type codes other than Single, Multi and No Charge.
SINGLE (Charge on a single break)
Single type rating selects the appropriate rate and applies it to the total weight.
EXAMPLE 1
If the rate is 0 --> 999,999 lbs. (.09 lb.)
For a receipt of 12,000 lbs., AccellosOne 3PL will charge $0.09 per lb.
EXAMPLE 2
If the weight is:
0 --> 5,000 lbs.
5,001 --> 9,000 lbs.
9,001 --> 15,000 lbs.
15,001 --> 999,999 lbs.
the rate is:
.09 per lb.
.08 per lb.
.07 per lb.
.06 per lb. 
For a receipt of 12,000 lbs., AccellosOne 3PL will charge $0.07 per lb. (that is, 
a single rate will be applied to the entire weight).
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
MULTIPLE (Charge on multiple breaks)
Multiple type rating selects the appropriate rate for each weight break and calculates the charge for that break. Then it adds up all the charges to arrive at 
the final charge.
EXAMPLE 3
For a receipt of 12,000 lbs., AccellosOne 3PL will rate as follows:
1st 5000 lbs. is charged $0.09 per lb.
next 4000 lbs. is charged $0.08 per lb.
next 3000 lbs. is charged $0.07 per lb.
NOTE Multi-break charge codes require that the charge on SKU code be 
the same as the qualify on SKU code. You cannot qualify on pounds and 
charge by hundredweight.
When you use multi-break charges, the rate appearing on the invoice will be 
averaged. For example, if your rate for the first 1,000 lbs. is .60 and for the 
next 500 lbs. is .50, the rate on an invoice for a receipt of 1,500 lbs. would be 
.57 (the total charges divided by the total weight).
NO CHARGE
This type is used when no billing is necessary. When you select no charge, 
the majority of fields in CHAR are bypassed when creating a new record.
This charge type is necessary because certain billing profiles such as Initial 
Storage require a valid charge code. If you don’t wish to charge Initial Storage 
for a particular customer, you must set up a billing profile for that customer 
with the charge code set to “No Charge.”
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
Charge Definition Mandatory
The charge can be a flat rate, a linear charge multiplied by a quantity or a 
combination of the two. 
B = Break
F = Flat
C = Combination (See Billing and Invoicing Guide)
The Charge Definition field works in conjunction with the Charge Type Code 
field. There are two valid values for the Charge Definition:
BREAK
Use Break when you wish to multiply the charge by a particular quantity.
FLAT
Use Flat when you wish to charge the same amount regardless of quantity.
General Ledger Code 
(GLCH)
Mandatory
The GL account to which the revenues from this charge will be posted.
Revenue Analysis Code 
(REVA)
Mandatory
The revenue analysis code to which this charge is assigned.
Invoice Type Code 
(INTP)
Mandatory
The invoice on which the charge will appear. You use invoice types in the billing program BILB (Billing Batch) to restrict the types of charges that will 
appear on an accessorial invoice or to split out the charges on two or more 
invoices.
If you do not use AccellosOne 3PL for billing or do not need to restrict certain 
charges in BILB, use your NA for Not Applicable invoice type.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
Charge on SKU Code 
(SKUS)
Mandatory
The SKU code that you are charging on. For automatic charges such initial 
storage or renewal storage, the qualifier code of your SKU in SKUS should be 
UNIT, WGTG or WGTN. For manual charges such as bill of lading or labelling 
charges, the qualifier code of your SKU can be HOUR or OCCR.
See “Charge on SKU Code vs. Qualify on SKU Code” on page 182 for further 
information.
Rounding Flag Rounding only applies to charges based on a unit-base SKU that is NOT the 
smallest SKU in the item’s quantity breakdown. For example, if your quantity 
breakdown is pallet/case/each, rounding only applies if you charge by pallet or 
case. If you charge by each, no rounding will occur.
U = Up
D = Down
N = No rounding
This flag is used when you are charging by one unit-based SKU type (for 
example, cases) and shipping or receiving partial quantities of this type (for 
example, pieces).
Suppose you charge for handling by the case but ship and receive in cases / 
pieces and your quantity breakdown is 10 pieces per case. Should you 
receive 5 cases and 4 pieces, you have to tell AccellosOne 3PL how to charge 
for this partial quantity. 
Round flag set to
Up
Down
No rounding
System will charge for
6
5
5.4
If you charge by either weight or the smallest unit-based SKU, set this flag to 
N for No Rounding.
Qualify on SKU Code 
(SKUS)
Mandatory
Usually the same as your charge on SKU code. See “Charge on SKU Code 
vs. Qualify on SKU Code” on page 182 for further information.
Rounding Flag Rounding rules for partial quantities of Qualify on SKU code. See previous 
Rounding Flag field for an explanation.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
Default Rate Charge 
Code
Optional
If two charge codes have the same rates, you can set up two charge codes 
that have different general ledger and revenue analysis information but use 
the same rates. See the Billing and Invoicing Guide for further information.
Charge Formula Reserved for future use
Tax Code Optional
GST
GST1
GST2
HST1/2/3/4/5/6/7/8/9
NONE
PST
The tax code that you enter (if any) overrides the customer tax code in DBIP 
and the item’s tax code in ITEM. 
Tax codes defined at the charge code level are designed for facilities in which 
multiple warehouses in different states or provinces with different tax rules 
and/or rates are assigned to the same company in COMP. For example, product stored and shipped within Ontario could be charged an HST rate of 13% 
for renewal storage, while product stored and shipped within British Columbia 
could be charged an HST rate of 12% for renewal storage. 
In this scenario, you would need to set up two charge codes in CHAR: one for 
Ontario renewal storage (tax code = HST) and one for BC (British Columbia) 
renewal storage (tax code = HST1). You would then attach these charge 
codes to different renewal storage profiles in IRSP and different item billing 
profiles in IBIP. 
Alternatively, you could set up a single renewal storage profile in IRSP and 
assign different charge codes to different location bill codes; for example, HST 
for your ON (Ontario) location billing code and HST1 for your BC location billing code.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
CHARGE ON SKU CODE VS. QUALIFY ON SKU CODE
The Charge on SKU code refers to the SKU type or unit of measure that you wish to charge by or bill by. For 
example, if your customer receives product as cases/pieces, do you wish to charge by the case, by the piece 
or by weight.
The Qualify on SKU code refers to the SKU type or unit of measure that you wish to “qualify on” — that is, the 
SKU type or unit of measure that you will count to determine your per rate. In the majority of cases, your 
“qualify on” SKU type will be the same as your “Charge on” SKU type. 
In a small number of cases, your “qualify on” SKU type will differ from your “Charge on” SKU type. See the 
following example.
Tax Code Override Flag Y = Yes
N = No
If you set this flag to Y for Yes, the operator will be forced to select the appropriate tax code from a pick list when adding accessorial or immediate charges 
to an invoice in ENAC/ENIN. 
If you set this flag to N for No, the Tax Code field in ENAC/ENIN will be automatically populated with either the charge code’s tax code (if any) or the customer’s tax code set up in DBIP and the operator will not be able to change it.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Charge Codes (CHAR)
PROCEDURE
1 Enter CHAR.
2 Click on Enter Criteria then Execute Query to see which charge codes have been already set up.
3 Using your arrow keys, go through each record to see which charges have already been set up. If the 
charges that you need have already been set up, click on Exit to exit. There is no need to add any new 
charge codes to CHAR.
4 If the charges that you require have not been set up, click on Create Record.
5 Key in a code to describe the charge and press Enter. 
6 Key in a meaningful description for the new charge and press Enter.
7 If required, key in your reference information and press Enter to press Enter with this field blank to 
bypass this option.
8 Press Enter to bypass the External Reference field.
9 Key in your charge type and press Enter or use the pick list function to select it. To select a code using a 
pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then 
use your arrow keys to position your cursor over the appropriate code and click on Select Code.
10 Key in your charge definition (B for Break or F for Flat) and press Enter.
Example of Qualify on vs. Charge on
EXAMPLE 1
Suppose your rates are:
0 --> 5,000 lbs.
5,001 --> 9,000 lbs.
9,001 --> 15,000 lbs.
.09 per lb.
.08 per lb.
.07 per lb.
In this example, you are qualifying on pounds (0 --> 5,000 lbs. is the SKU type you are counting when you 
look up your per rate) and you are also charging by the pound (the rate for the 0 --> 5,000 weight break is 
.09 per lb.). Therefore, your “qualify on” SKU type is the same as your “charge on” SKU type. 
EXAMPLE 2
Suppose your rates are:
0 --> 5,000 lbs.
5001 --> 9,000 lbs.
9,001 --> 15,000 lbs.
.09 per CWT
.08 per CWT
.07 per CWT
In this example, you are qualifying on pounds as in the previous example, but you are charging by the 
hundredweight (CWT). Therefore, your “qualify on” SKU type is not the same as your “charge on” SKU 
type. To set up a charge code for this type of rating, you would enter CWT as your Charge on SKU Code 
and would enter your SKU code for pounds (set up in SKUS) as your Qualify on SKU Code.

CHARGE AND RATE SETUP
Charge Codes (CHAR)
11 Key in the general ledger code to which the revenues from this charge are to be posted and press Enter 
or use the pick list function to select it.
▪ If your codes have not been fully defined yet, use your miscellaneous account 999999.
▪ If you are using the GL modifier code feature, key in your account code using your wildcard characters 
(for example, **120000).
12 Key in your revenue analysis code and press Enter or use the pick list function to select it.
13 Key in your invoice type and press Enter or use the pick list function to select it.

Charge Code for blast freezing
14 Key in the SKU type that you wish to charge on and press Enter or use the pick list function to select it.
If you are setting up a charge code for fax services or taxes, use EA as your SKU type. If you are setting 
up an hourly based labor charge, use HR as your SKU type.
15 Key in the appropriate value for the Rounding Flag for your Charge on SKU type (U for Round Up, D for 
Round Down or N for No Rounding) and press Enter.
16 Key in the SKU type that you wish to qualify on and press Enter or use the pick list function to select it.
17 Key in the appropriate value for the Rounding Flag for your Qualify on SKU type and press Enter.
CAUTION In the majority of cases, your “Qualify on” SKU type will be the same as 
your “Charge on” SKU type. However, if you use CWT (hundredweight) or CKG (hundred kilo) as your Charge on SKU type, you must qualify on either pounds or kilos 
and enter the appropriate code for your unit of measure.

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)

Charge Code screen showing Charge on and Qualify on SKU values
18 Press Enter to skip the remaining fields and enter RATE.
19 Go to next section of this manual for instructions on RATE (Depositor Billing Rates).
Depositor Billing Rates (RATE)
OVERVIEW
In this program, you set up your rates — that is, the flat rate or linear charge, the number of weight breaks, 
any maximum and minimum charges and the effective date. The rates that you create in this program are 
PREREQUISITES: CHAR, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: This program is mandatory if you use AccellosOne 3PL for billing
OTHER REQUIREMENTS: A list of all your tariffs.

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)
attached to the specific charge codes that you created in CHAR as well as to specific customers that you 
created in CUST. 
If you are setting up a rate that applies to all customers (for example, your published rates), you can use .ALL 
as your customer code. If you are setting up a customer-specific rate, you would enter the code for that 
customer in the Customer Code field in RATE.
You can enter your rates in RATE when you create your charge code in CHAR or you can set up your charge 
code in CHAR first and enter your rates at a later date. However, you must have a valid RATE record attached 
to your charge code before you can perform any transactions involving that charge code; for example, you 
cannot enter a receipt if the item that you are receiving is attached to a charge code with no RATE record.
This program is not used for “no charge” type charge codes.
FIELD DESCRIPTIONS
Customer Code
(defined in CUST)
Mandatory
Enter .ALL for all customers or a specific customer code if the rate applies to a 
single customer.
Charge Code (CHAR) Set up in CHAR.
Charge Type Code Determined by the charge type that you selected in CHAR.
Charge Definition Determined by the charge definition that you selected in CHAR.
Effective Date Mandatory
If you use 01.01.01, you can bill for anything in the past. If you enter a future 
date in this field, rates will take effect on the date that you specify. Rates with 
an effective date in the future can be deleted in RATE.
Percentage Value Reserved for future use
Flat Rate Only available if Charge Definition set to F for Flat
Your flat rate for the charge code.
Number of Flat Rate 
Breaks
Only available if Charge Definition set to C for Combination
The number of flat rate breaks.

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)
Number of Breaks Only available if Charge Definition set to B for Break or C for Combination
The total number of breaks both flat and linear.
Minimum Charge Only available if Charge Definition set to B for Break or C for Combination
Your minimum charge for the charge code.
Maximum Charge Only available if Charge Definition set to B for Break or C for Combination
Your maximum charge for the charge code.
Charge on SKU Code If you enter a SKU code in this field, it will override the charge on SKU in 
CHAR. What this override means is that the same charge code can be used 
twice with different charge on and qualify on values: once for customer A with 
a charge on and qualify on SKU of PLT and once for customer B with a charge 
on and qualify on SKU of CS. 
Round Flag The rounding rules for your override charge on SKU code.
Qualify on SKU Code See Charge on SKU Code field.
Round Flag See Charge on SKU Code field.
Exclude From Surcharge 
Calculations
N = No (default)
Y = Yes
If you set this flag to N for No, the charge will be included in any surcharge calculations set up in DBIP for a given customer unless you set up individual 
exclusions in the following four fields. 
If you set this flag to Y for Yes, the charge will NOT be included in any surcharge calculations set up in DBIP.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)
PROCEDURE
1 If you are not already in RATE, enter RATE. If you accessed this program through CHAR, proceed to 
step 2.
Exclude From Receipt 
Surcharge
Only available if Exclude From Surcharge Calculations = No
Exclude from Surcharge 1
Exclude from Surcharge 1, 2
Exclude from Surcharge 1, 2, 3
Exclude from Surcharge 1, 3
Exclude from Surcharge 2
Exclude from Surcharge 2, 3
Exclude from Surcharge 3
You can exclude the charge from any combination of up three surcharges.
Exclude From Renewal 
Surcharge 
Only available if Exclude From Surcharge Calculations = No
Same as above.
Exclude From Accessorial Surcharge
Only available if Exclude From Surcharge Calculations = No
Same as above.
Exclude From Immediate 
Invoice Surcharge
Only available if Exclude From Surcharge Calculations = No
Same as above.
FIELD DESCRIPTIONS

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)

Depositor Billing Rates
2 Key in the customer code that this charge or rate is to be applied to and press Enter. If the charge or rate 
applies to all customers, use .ALL as your customer code.
3 If you have accessed this program through CHAR, the charge code field will be filled in with the code that 
you created in CHAR. If you have accessed this program outside of CHAR, you must enter a charge 
code yourself. 
Key in your charge code and press Enter or select it using the pick list. To select a code using a pick list, 
press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your 
arrow keys to position your cursor over the appropriate code and click on Select Code.
4 Once the charge code has been entered, the charge type and charge definition fields will be automatically filled in and cannot be changed.
5 Key in your effective date (01.01.01 is recommended if you are setting up a new system) and press 
Enter.

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)

Depositor Billing Rates for a charge type of Break
6 Proceed to enter your rates and your breaks according to the charge definition that you have selected:
7 Key in your non-flat or linear breaks.
If you selected Flat: If you selected Break:
a) In the Flat Rate field, key in 
the flat rate and press Enter.
b) In the Exclude from Surcharge 
Calculations field, key in Y for 
Yes or N for No and press 
Enter.
c) When the Breaks window 
appears, Click on Master 
Block to exit create mode. 
Then click on Return to Main 
and Exit to exit.
a) In the Number of Breaks field, 
key in the number of breaks 
and press Enter.
b) Key in your minimum and 
maximum charges or press 
Enter to accept the system 
defaults.
c) In the Exclude from Surcharge 
Calculations field, key in Y for 
Yes or N for No and press 
Enter.
d) Proceed to next step.

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)

Depositor Billing Rates screen showing Breaks Block with four breaks
In the above example, for up to 499 lbs., the rate is $1.00 per CWT. For weights between 499 and 999 
lbs., the rate is $0.90 and so on and so forth. If you set up the first two breaks as a flat rate (number of flat 
rate breaks = 2), the rate for up 499 lbs. would be a flat rate of $1.00 and the rate for up to 999 lbs. would 
be a flat rate of $0.90. 
8 Click on Master Block to exit create mode. Then click on Return to Main and Exit to exit.
COPYING RATES
You can copy individual depositor billing rates from one company/customer to another company/customer. 
When copying rates, the Use Current Effective Date of From Customer checkbox allows you to specify which 
effective date AccellosOne 3PL uses for the new rate: the current effective date of the from customer or the 
current system date. Old rates that are no longer effective are NOT copied.
EXAMPLE: Customer A, charge = BOL (Bill of Lading)
The following example shows five different effective dates belonging to the from customer: two rates in the 
past, one current rate and two rates in the future. 
FROM RATES
TO RATES - CHECKBOX 
UNCHECKED
TO RATES - CHECKBOX 
CHECKED
01-JAN Past rate Not copied Not copied
20-MAR Past rate Not copied Not copied
05-JUN Current rate June 20 June 5
Today = June 20

CHARGE AND RATE SETUP
Depositor Billing Rates (RATE)
If you wish to copy all rates from one company to another regardless of customer, you can do so in COCO 
(Copy Codes Between Companies).
1 Enter RATE.
2 Select the rate that you wish to copy.
3 Click on Copy Rate.
RATE screen showing from company/customer, to company/customer and checkbox
4 Select your to company from the dropdown list.
5 If your from customer is not .ALL, select your to customer from the dropdown list.
6 If required, click on the Use Current Effective Date of From Customer checkbox.
7 Click on Process.
8 When prompted to proceed, click on Yes.
9 Click on Yes to acknowledge the “Copy done” message. 
10 Click on Exit to close the Copy Rates window.
11 Click on Exit to exit RATE.
18-AUG Future rate Same as from date 18-AUG Same as from date
22-SEP Future rate Same as from date 22-SEP Same as from date
FROM RATES
TO RATES - CHECKBOX 
UNCHECKED
TO RATES - CHECKBOX 
CHECKED

ITEM PROFILE SETUP
Item Information Profile (IINP) ....................................................................... 194
Item Initial Storage Profile (IISP).................................................................... 196
Item Renewal Storage Profile (IRSP)............................................................. 201
Item Handling Profile (IHAP) .......................................................................... 208
Date Profile (DAPR)......................................................................................... 210
Item Billing Profile (IBIP) ................................................................................ 212
Item Shipping Profile (ITSH)........................................................................... 217
Item Process Profile (IPRP)............................................................................ 224
Item Quantity Breakdown Profile (IQBP) ...................................................... 226
Item Alternate Sorts (ITAS) ............................................................................ 233
Hold Types (HOLD) ......................................................................................... 237
Hold Shipping Sequence Profile Code (HOSP) ............................................ 241
Item Hold Profile (IHOP) ................................................................................. 244
Item Incubation Hold Code (IIHO).................................................................. 247
Incubation Hold Profile (IIHP) ........................................................................ 249
Freight Class Codes (CLAS) .......................................................................... 252
Commodities (COMM)..................................................................................... 254
Item Location Profile (ILOP)........................................................................... 256
Item Tare Profile (ITAP) .................................................................................. 258

ITEM PROFILE SETUP
Item Information Profile (IINP)
Item Information Profile (IINP)
OVERVIEW
In this program, you define your deferred handling percentages. That is, you wish to split your handling 
revenue into two portions: one portion that is earned when the product is received and another portion that is 
earned when the product is shipped. Because IINP is a mandatory profile in ITEM, you must create a profile 
in IINP even if you do not track deferred handling.
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
General Information Item 
Profile Code
Mandatory
Your general information profile code. For example, LBS or KILOS.
Description Mandatory
Your general information profile code description
Deferred Handling 
Inbound Percentage
Mandatory
Set the percentage to 100. For further information on deferred handling, refer 
to the Standard Reports Guide.
Deferred Handling Outbound PercentageMandatory
Set the percentage to 0.
Calculate Turns Reserved for future use
Calculate Tonnage Reserved for future use

ITEM PROFILE SETUP
Item Information Profile (IINP)
PROCEDURE
1 Enter IINP.
2 Click on Enter Criteria) then Execute Query to see whether the profile that you wish to use has already 
been set up. If no profile has been set up, click on Create Record.

Item Information Profile
3 In the General Information Item Profile Code field, key in the appropriate code (LBS, KGS, TONS, etc.) 
and press Enter.
4 Key in your description (for example, Standard) and press Enter.
5 In the Deferred Handling Inbound Percentage field, key in 100 and press Enter.
6 In the Record Weight Measure Code field, use your pick list to select the any unit of measure. To select a 
code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list 
codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
7 In the Record Cube Measure Code field, use your pick list to select the any unit of measure.
Record Weight Measure 
Code
Reserved for future use
Record Cube Measure 
Code
Reserved for future use
Part of Assembly Reserved for future use
Ship Alone Reserved for future use
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Initial Storage Profile (IISP)
8 Click on Return to Main and then Exit to exit the program.
Item Initial Storage Profile (IISP)
OVERVIEW
In this program, you set up your item initial storage profile(s). The item initial storage profile defines the onetime charges incurred for an item when that item is first received into the warehouse. This profile can be 
attached to a particular location billing code (for example, one charge for all locations assigned a location 
billing code of DRY, another charge for all locations assigned a location billing code of COOL, etc.) if you want 
to set up different charges for initial storage based on location. Alternatively, you can set up one profile that 
applies to all locations. 
You can also define special discounts on initial storage for product received a specified number of days 
before the end or after the beginning of your billing period. If you are not using the discount function, you can 
prorate initial storage based on the number of days that the product has been in your warehouse. 
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not 
charge for initial storage. 
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE You cannot use discounts or prorating for open lots. If you process open lots 
and wish to offer discounts or prorating on non-open lots, you must set up two profiles 
in IISP: one for open lots and another for non-open lots.
FIELD DESCRIPTIONS
Initial Storage Profile 
Code
Mandatory
Your initial storage profile code. For example, F1 for Freezer Group 1.

ITEM PROFILE SETUP
Item Initial Storage Profile (IISP)
Description Mandatory
Your initial storage profile code description
Location Bill Code 
(LODE)
Mandatory
The location billing code for this profile. If you have the same initial storage 
rates regardless of location billing code, use .ALL (not ALL without the preceding dot).
If you intend to store the same item in two different locations with two different 
location billing codes (for example, a product like chocolate that could be 
either a freezer item or a cooler item depending on its temperature when it 
was received), you can assign the same initial storage profile two or more 
location billing codes. This allows you to charge initial storage based on the 
location billing code. 
For example, if you receive a shipment of chocolate and place half the receipt 
in your freezer and the other half in your cooler, the freezer portion of the 
receipt will be charged freezer rates and the cooler portion of the receipt will 
be charged cooler rates.
TIP You can use the .ALL code to indicate “all other location billing codes.” 
For example, if you assign charge code 1 to your .ALL code and charge code 
2 to your DRY1 location billing code, all location billing codes except DRY1 will 
be charged the rates defined for charge code 1.
Charge Code (CHAR) Mandatory
The charge code for your initial storage. Make sure that the SKU code that the 
charge code is based on does not have a value of OCCURRENCE in the 
Qualifier Code field in SKUS (Stock Keeping Units).
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Initial Storage Profile (IISP)
Discount Day Optional
Defines the number of days in the billing period that the discount period 
applies to. If you enter a positive number, you count forward from the day after 
the day that you specify to the end of the billing period or to the next discount 
day — whichever comes first. For example, if you enter 15, the discount 
period will start on the 16th (the day after the day that you specify).
If you enter a negative number (for example, -3), you count backwards from 
the last day of the billing period to the day that you specify in order to define 
the discount period.
The billing period in AccellosOne 3PL is determined as follows. If you set up a 
date profile in DAPR, your billing periods will be determined by the starting 
dates that you enter in that program. If you do not set up a date profile in 
DAPR, your billing periods will be based on the calendar month in which the 
receipt was confirmed. For example, if your receipt is confirmed in August, 
your billing period is Aug. 1 to Aug. 31. If your receipt is confirmed in February, 
your billing period is Feb. 1 to Feb. 28.
Discount Percentage Optional
The percentage discount that applies to the discount period.
Prorate If you use prorating, you cannot set up discount days and discount percentages
Y = Yes
N = No
If you set this flag to Yes, AccellosOne 3PL will charge initial storage for only 
the portion of the billing period that the goods are in the warehouse. For example, if your billing period is 30 days and you receive on the 15th day (that is, 
midway through the period), the prorate function will charge for half the period 
only.
See the Discount Day field for further information on how the billing period is 
calculated by AccellosOne 3PL.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Initial Storage Profile (IISP)
EXAMPLES OF DISCOUNT DAYS
PROCEDURE
1 Enter IISP.
2 Click on Enter Criteria then Execute Query to see whether the profile that you wish to use has already 
been set up. If no profile has been set up, click on Create Record.
3 Key in your initial storage profile code and press Enter.
4 Key in a description for your initial storage profile code and press Enter.
5 If your profile applies to all locations, key in .ALL and press Enter. If your profile is location specific, use 
your pick list to select the appropriate location bill code. To select a code using a pick list, press F10 to 
Example 1 — split month billing
Discount Day Percentage Meaning
16 50 If product is received during first 16 days of the billing period, full initial 
storage charges apply. If product is received from the 17th day of the 
billing period to the last day of the billing period, there is a 50% discount off initial storage charges. 
Example 2
Discount Day Percentage Meaning
-3 60 60% off initial storage for product received during the last three days of 
the billing period. 
Example 3
Discount Day Percentage Meaning
0 0 No discount days.
Example 4
Discount Day Percentage Meaning
15 50 50% off initial storage on product received from the 16th day of the billing period to the third day before the end of the period.
-2 30 30% discount on product received during the last two days of the billing period.

ITEM PROFILE SETUP
Item Initial Storage Profile (IISP)
display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys 
to position your cursor over the appropriate code and click on Select Code. 
6 In the Charge Code field, key in your charge code and press Enter or use your pick list to select the 
appropriate charge code. If there is no charge for initial storage, select your NC charge code and click on 
Return to Main to exit create mode. Then click on Master Block and Exit to exit.
7 Key in the number of the discount day and press Enter or key in 0 and press Enter to bypass this field. 
8 Key in the discount percentage and press Enter or key in 0 and press Enter to bypass this field.
9 If you are setting up prorating, key in Y for Yes in the Prorate field and press Enter.
10 If required, repeat steps 7 to 9 to define another discount period and percentage in the Discount Block.
11 When you finish defining your discount period and percentage, click on Return to Main to exit create 
mode.

Item Initial Storage Profile showing discount days
12 Click on Master Block and Exit to exit the program.
Item Initial Storage Profile
If you wish to set up discount 
days or prorating:
If you do NOT wish to set up 
discount days or prorating:
a) Click on Return to Main to redisplay the Location Billing Block.
b) Click on Discount Block.
a) Click on Return to Main to exit 
create mode. Then click on Master Block and Exit to exit.

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
Item Renewal Storage Profile (IRSP)
OVERVIEW
In this program, you set up your renewal storage profile(s). Renewal storage is any recurring storage charge 
that is charged after initial storage. Renewal storage is normally charged for as long as the product remains in 
the warehouse.
IRSP supports the following types of renewal billing:
▪ Anniversary — Monthly
▪ Anniversary — Weekly 
▪ Daily
▪ Monthly — First of Month 
▪ Monthly — Last of Month 
▪ Weekly as of Monday
If you renew on a special day of each month that the above billing types cannot accommodate (for example, 
every 30 days, every second week, the 14th of each month, etc.), you must set up your start dates in DAPR 
(Date Profile).
EXAMPLE 1 — FIRST OF MONTH BILLING
Product gets renewed the first of the month regardless of the day it was originally received.
PERIOD 1
Inbounds: 1,000 cases received on 18th
Outbounds: 700 cases (25th)
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: Any changes to renewal storage take effect at the end of the frequency 
period. For example, if you change your frequency from anniversary 
monthly to anniversary weekly, the change will take place at the end of 
the current month.
OTHER REQUIREMENTS:
18 25 01 01
+1000 CS -700 CS
$ initial storage renewal storage
= 300 CS

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
Balance: 300 cases (1st)
You receive 1,000 cases of new product on the 18th of the month and your initial storage charge is based on 
this amount. On the 25th of the month, you ship out 700 cases. On the first of the following month, you have a 
balance of 300 cases and renewal storage is charged on this quantity.
EXAMPLE 2 — ANNIVERSARY MONTHLY BILLING
Product gets renewed each month on the day it was originally received.
In this type of billing, the initial storage period is zero. You receive 1,000 cases of new product on the 18th of 
the month and your renewal storage for the first month is based on this amount. On the 25th of the month, 
you ship out 700 cases. On the 18th of the following month, you have a balance of 300 cases and renewal 
storage is charged on this quantity.
A profile can consist of a single type of renewal billing or multiple types. If you set up multiple types, you 
define a period for each renewal whose billing frequency you wish to change. For example, period one could 
be anniversary monthly, period two could be daily, period three could be weekly as of Monday, etc. For each 
period that you define, you can set up different charges and rates if required.
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not 
charge for renewal storage or do not use AccellosOne 3PL to generate invoices or gather billing information. 
Set up a No Charge profile as follows:
Period Number = 1
Frequency Code = any frequency (daily, anniversary monthly, etc.)
Cycle = 1
Reset Date = N
Location Bill Code = .ALL
Charge Code = NC (No charge)
PERIOD 1
Inbounds: 1,000 cases received on 18th
Outbounds: 700 cases (25th)
Balance: 300 cases (1st)
PERIOD 2
Initial balance: 300 cases
Inbounds: 200 cases received on 20th
Balance: 500 cases
NOTE If you receive product on the 31st of a month, product will renew on the last 
day of the following month if that month does not have 31 days. For example, product 
received on Jan. 31 will renew on Feb. 28 or 29, March 31, April 30, etc.
18 25 18 18
+1000 CS -700 CS
$ renewal storage renewal storage
= 300 CS
20
+200 CS

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
FIELD DESRIPTIONS
FIELD DESCRIPTIONS
Renewal Storage Profile 
Code
Mandatory
Your renewal storage profile code. For example, 35A for 35-40 lb. Anniversary 
Monthly.
Description Mandatory
Your renewal storage profile code description
Period Number Mandatory
You need to set up a separate period for each time your type of billing 
changes.
Frequency Code AM = Anniversary — Monthly
product is renewed each month on the day it was originally received
AW = Anniversary — Weekly
product is renewed each week on the day it was originally received
D = Daily
product is renewed each day 
MF = Monthly — 1st of Month
product is renewed the first of the month regardless of which day it was originally received
ML = Monthly — Last of Month
product is renewed the last of the month regardless of which day it was originally received
W = Weekly as of Monday
product is renewed every Monday regardless of which day it was originally 
received

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
Cycle Mandatory
The number of times the type of billing specified in the Frequency Code field 
will occur in the current period before AccellosOne 3PL switches to the next 
period, if any. 
If there is only a single period, the cycle will repeat itself for as long as there is 
product in the warehouse.
EXAMPLES
Period
1
Frequency
Anniversary Monthly
Cycle
1
Product gets renewed each month on the day it was originally received for as 
long as there is product in the warehouse.
Period
1
Frequency
Daily
Cycle
1
Product gets renewed daily from the beginning of the renewal storage period 
for as long as there is product in the warehouse.
Period
1
2
Frequency
Daily
Anniversary Monthly
Cycle
7
1
There are two periods in this renewal storage profile. Period 1 lasts seven 
days starting from the beginning of the renewal storage period. In period 2, 
product gets renewed each month on the day it was originally received for as 
long as there is product in the warehouse.
Reset Date Y = Yes
N = No
This flag allows you to reset the original receipt date when you switch from 
one billing frequency to another. For example, you offer X number of days of 
free storage and then charge renewal storage based on either the original 
receipt date or the date that the free storage ended.
EXAMPLE 1
Period
1
2
Frequency
Daily
Anniversary Monthly
Cycle
10
1
Reset Date
Y
N
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
If product is received on Feb. 02, the first renewal date will be Feb. 12. At that 
time, the original receipt date will be reset to Feb. 12. Then the next renewal 
date will be Mar. 12 based on the new reset date followed by Apr 12, May 12 
and so on.
EXAMPLE 2
Period
1
2
Frequency
Daily
Anniversary Monthly
Cycle
10
1
Reset Date
N
N
If product is received on Feb. 02, the first renewal date will be Feb. 12 and the 
original receipt date will remain Feb. 02. The next renewal date will be Mar. 02 
followed by Apr 02, May 02 and so on.
Location Bill Code
(defined in LODE)
Mandatory
The location billing code for the period specified in the Period Number field. If 
you have the same renewal storage rates for all your locations, use .ALL (not 
ALL without the preceding dot).
If the same item can be stored in two or more locations with different location 
billing codes and hence different rates (for example, a product like lumber that 
could be stored either outside in a yard or inside in the warehouse), you must 
assign multiple location billing codes to the same renewal storage profile. This 
will allow you to charge different renewal storage rates based on the area in 
which the product is stored. 
For example, if you receive a shipment of lumber and place half the receipt in 
your yard and the other half in your warehouse, the yard portion of the receipt 
will be charged yard rates and the warehouse portion of the receipt will be 
charged warehouse rates.
TIP You can use the .ALL code to indicate “all other location billing codes.” 
For example, if you assign charge code 1 to your .ALL code and charge code 
2 to your DRY1 location billing code, all location billing codes except DRY1 will 
be charged the rates defined for charge code 1.
Charge Code
(defined in CHAR)
Mandatory
The charge code for the period specified in the Period Number field. Make 
sure that the SKU code that the charge code is based on does not have a 
value of OCCURRENCE in the Qualifier Code field in SKUS (Stock Keeping 
Units).
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
EXAMPLE 1
In this example, the customer’s products are renewed anniversary monthly.

Anniversary monthly billing
In the above example, AccellosOne 3PL will bill anniversary monthly using the charge code R15C. Since only 
a single period is defined, anniversary monthly billing will continue month after month. In other words, the 
period one cycle will repeat itself for as long as there is product in the warehouse.
EXAMPLE 2
In this example, there are two renewal storage periods: period 1 and period 2. Period 1 lasts seven days and 
is followed by period 2, which lasts as long as there is product in the warehouse. 

Two renewal storage periods

ITEM PROFILE SETUP
Item Renewal Storage Profile (IRSP)
In the above example, there are two billing periods. In period 1, AccellosOne 3PL will calculate renewal 
storage at the end of the seven-day period using charge code NC for no charge (not shown). In period 2, 
AccellosOne 3PL will apply charge code SCS for every month thereafter. Because the Reset Date flag is set 
to Yes for the first billing period, AccellosOne 3PL will reset the original receipt date to the original receipt date 
+ 7 days.
PROCEDURE
1 Enter IRSP.
2 Click on Enter Criteria then Execute Query to see which renewal storage profiles have been already set 
up.
3 If the profile that you require has not been set up, click on Create Record.
4 Key in a code to describe the renewal storage profile and press Enter. 
5 Key in a meaningful description for the new profile and press Enter.
6 Key in 1 for your period number and press Enter.
7 Use your pick list to select the appropriate billing frequency code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow 
keys to position your cursor over the appropriate code and click on Select Code.
If you will be setting up special billing dates in DAPR (Date Profile) and attaching this profile to all your 
items, you can enter any frequency that you wish. AccellosOne 3PL will ignore the frequency specified in 
IRSP and use the DAPR dates instead. 
8 Key in your cycle number (the number of times that you want period to repeat itself before it moves to the 
next period) and press Enter. If you are setting up a single period, you set the Cycle field to 1.
9 Key in your reset date value (Y for Yes or N for No) and press Enter.
10 If you require renewal billing with multiple billing frequencies, enter another line for period number 2.
11 When you finish entering all your billing periods, click on Return to Main to exit create mode.
12 Position the cursor over period number 1.
13 Click on Location Bill Block.
14 Key in your location bill code for period 1 and press Enter. You can use .ALL for all locations or you can 
use your pick list to select the appropriate location bill code.
15 Use your pick list to select the appropriate charge code for this period.
CAUTION If you are setting up two or more billing frequencies, make sure that 
your cursor is positioned over the correct period number before you enter the Location Bill Block. If you position your cursor by mistake over period 2 rather than period 
1, the location bill code and the charge code will be attached to the wrong period. 

ITEM PROFILE SETUP
Item Handling Profile (IHAP)

Renewal Storage profile showing anniversary monthly billing
16 If required, enter your second location billing record to the Location Bill Block.
17 When you finish entering your location billing records, click on Return to Main.
Item Handling Profile (IHAP)
If you wish to set up a second 
renewal billing period:
If you do NOT wish to set up 
a second renewal billing period:
a) Click on Create Record.
b) Repeat the above steps for your 
second billing period.
a) Click on Frequency Block.
b) Click on Master Block and then 
Exit to exit.
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory

ITEM PROFILE SETUP
Item Handling Profile (IHAP)
OVERVIEW
In this program, you set up your inbound handling charges for an item. Inbound handling charges are onetime charges that are automatically applied when you confirm a receipt. 
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not 
charge for handling or do not use AccellosOne 3PL to generate invoices or gather billing information. A no 
charge profile must contain a valid charge code for your inbound handling charges in order to be added to 
AccellosOne 3PL.
PROCEDURE
1 Enter IHAP.
2 Key in your handling profile code and press Enter.
3 Key in a meaningful description for your handling profile code and press Enter.
4 In the Inbound Charge Code field, use your pick list to select the appropriate charge code. To select a 
code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list 
codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
If you are setting up a no charge profile, use your NC charge code in this field.
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Handling Profile Code Mandatory
Your handling profile code. For example, H1 for Handling Charges 1.
Description Mandatory
Your handling profile code description
Inbound Charge Code 
(CHAR)
Mandatory
You charge code for inbound handling charges. If you are setting up a no 
charge profile, enter your NC charge code in this field. Make sure that the 
SKU code that the charge code is based on does not have a value of OCCURRENCE in the Qualifier Code field in SKUS (Stock Keeping Units). 

ITEM PROFILE SETUP
Date Profile (DAPR)

Item Handling Profile showing inbound handling charges
5 Click on Return to Main and then Exit to exit.
Date Profile (DAPR)
OVERVIEW
In this program, you set up the starting dates for each renewal period. This program is only required if you 
have irregular billing periods such as every 25 days, the 17th of each month, the third week of each month, 
etc. If you bill anniversary monthly, anniversary weekly, daily, first of the month, last of the month or weekly as 
of Monday, you use the standard frequency codes in IRSP.
In DAPR you key in manually the starting date (month, day and year or day, month and year) of each billing 
period. During setup you should enter all starting dates for the current year. At the end of the current year, you 
will have to enter the starting dates for the following year.
PREREQUISITES: None
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory only if you use AccellosOne 3PL to generate invoices or 
gather billing information and you have irregular billing periods
OTHER REQUIREMENTS: A list of your billing periods for the current year

ITEM PROFILE SETUP
Date Profile (DAPR)
PROCEDURE
1 Enter DAPR.
2 Click on Create Record.
3 Key in your date profile code and press Enter. 
4 Key in a meaningful description for your date profile and press Enter again.
5 In the Dates window, key in the starting date of your first renewal period using the correct date format and 
press Enter.
6 Press Enter in the Correct column to confirm the starting date and create a new blank line.
7 Repeat the above step for each starting date that you wish to enter. You should enter all dates for a minimum period of one year.
FIELD DESCRIPTIONS
Date Profile Code Mandatory
Your date profile code.
Description Mandatory
Your date profile code description
Starting Date Mandatory
Your starting date for each renewal period. The format of this date must match 
the date format in COMP (Company Code).
CAUTION Your first starting date should always be one month or billing period 
back from the current date. For example, if you bill on the 15th of each month and are 
performing your setup on July 12, 2013, your first starting date should be June 15, 
2013. If you were to make July 15 your first starting date, you would be unable to bill 
for items renewing before this date.

ITEM PROFILE SETUP
Item Billing Profile (IBIP)

Date Profile for late 08 and the first two quarters of 2009
8 When you finish entering all your dates, click on Return to Main to exit create mode. Then click on Master 
Block and Exit to exit.
Item Billing Profile (IBIP)
OVERVIEW
In this program, you attach your various billing-related profiles (IISP, IRSP, IHAP, etc.) to a new profile called 
IBIP. You then attach IBIP to your items in ITEM. You use IBIP to set up item-related billing only (for example, 
a minimum initial storage charge that applies to a particular item). If you wish to set up minimum charges that 
apply to an entire receipt — that is, all items from one customer — you do so in DILP (Depositor Inventory 
Level Profile).
PREREQUISITES: IISP, IRSP, IHAP, CHAR, DAPR
ATTACHED TO: ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Item Billing Profile (IBIP)
IBIP also allows you to set up “local overrides” for your billing entity minimum charge, renewal storage line 
minimum charge, initial storage minimum charge and handling minimum charge. A local override is a profile 
for a single item or a group of items whose billing entity minimum charge, renewal storage line minimum 
charge, etc. replaces the customer-wide defaults set up in DILP (Depositor Inventory Level Profile).
IBIP profiles can be customer specific or can apply to all customers. If you charge special rates for certain 
items, you will have to set up multiple item billing profiles for those items. If you do not use AccellosOne 3PL 
to generate invoices or gather billing information, set up one billing profile called NA (Not Applicable).
FIELD DESCRIPTIONS
Item Billing Profile Code Mandatory
Your item billing profile code. For example, CAS1 for Billing on Cases 1. The 
special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing 
batchs in BILB (Billing Batch) and cannot be used in an item billing profile.
Description Mandatory
Your item billing profile code description
Initial Storage Profile 
Code (IISP)
Mandatory
The initial storage profile for the items to which this profile is attached.
Renewal Storage Profile 
Code (IRSP)
Mandatory
The renewal storage profile for the items to which this profile is attached.
Handling Profile Code 
(IHAP)
Mandatory
The handling storage profile for the items to which this profile is attached.
Date Profile Code 
(DAPR)
Optional
If required, the date profile for the items to which this profile is attached. 

ITEM PROFILE SETUP
Item Billing Profile (IBIP)
Billing Entity Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Renewal Storage Line 
Minimum Charge Code 
(CHAR)
Optional
See Billing and Invoicing Guide.
Initial Storage Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Handling Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Create Renewal Invoice 
at Zero Inventory
This field is an override at the item level of the customer level default established in DBIP. See the Billing and Invoicing Guide.
Original / Current Rate on 
Renewals
C = Current
I = Initial Original
R = Renewal Original
See the field of the same name in Depositor Billing Profile (DBIP). If you enter 
a value in this field, it will override the customer-level default in DBIP for the 
items attached to this profile.
Number of Days Between 
Renewal Invoices
This field is an override at the item level of the customer level default established in DBIP. See the Billing and Invoicing Guide.
Rate Qualifier O = Original
B = Balance
See the field of the same name in Depositor Billing Profile (DBIP). If you enter 
a value in this field, it will override the customer-level default in DBIP for the 
items attached to this profile.
Invoice Type for AutoProcessingFor custom use only.
Reserve Quantity See Billing and Invoicing Guide.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Billing Profile (IBIP)
PROCEDURE
1 Enter IBIP.
2 Click on Enter Criteria then Execute Query to view the item billing profiles that have been already set up.
3 If you need to set up a new item billing profile, click on Create Record.
4 Key in an item billing profile code and press Enter. 
5 Key in a meaningful description for your item billing profile and press Enter again.
6 Use your pick list to select the appropriate profile code for initial storage. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select Code. 
7 Use your pick list to select the appropriate profile code for renewal storage.
Renewal Summarization 
Code
See Billing and Invoicing Guide.
Ignore Multiple Location 
Bill Codes for Same Billing Entity
Y = Yes
N = No
If the same billing entity is stored in multiple locations with multiple location 
billing codes, you can bill on a single location bill code or all location billing 
codes. 
If you set this field to Yes, the billing engine will select the location billing code 
with the largest quantity to be billed and ignore the other location billing codes. 
If you set this field to No, the billing engine will bill on all location billing codes.
Split Invoice by Alternate 
Reporting Code
N = No
Y = Yes
If you set this field to Yes, you can split invoices based on alternate reporting 
type and alternate reporting code. If the type and code that you enter in the 
Alternate Reporting Type and Alternate Reporting Code fields in IBIP matches 
the type and code attached to items in ITEM, AccellosOne 3PL will generate a 
separate invoice for each alternate reporting type. 
Alternate Reporting Type 
(ITAS)
Only available if Split Invoice by Alternate Reporting Type Code = Yes
Your alternate reporting type.
Alternate Reporting Code 
(ITAS)
Only available if Split Invoice by Alternate Reporting Type Code = Yes
Your alternate reporting code.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Billing Profile (IBIP)
8 Use your pick list to select the appropriate profile code for handling charges.
9 If required, use your pick list to select the appropriate date profile code.
10 If required, use your pick list to select the appropriate charge codes for the following:
▪ billing entity minimum 
▪ renewal storage minimum
▪ initial storage minimum 
▪ handling charge minimum
If you do not require minimums for these charges or the customer-wide defaults set up in DILP apply to 
all items, press Enter to bypass these fields.
11 If required, key in the appropriate value (C for Current, I for Initial Original or R for Renewal Original) in 
the Original /Current Rate on Renewals field and press Enter. If prompted to do so, key in your rate qualifier (O for Original or B for Balance) and press Enter.
12 Press Enter to bypass the remaining fields in IBIP.
13 When you finish setting up your item billing profile, click on Return to Main.

Item Billing Profile with no local overrides for minimum charges
14 Click on Exit to exit.

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
Item Shipping Profile (ITSH)
OVERVIEW
ITSH serves three main functions. It allows you to:
▪ specify your back order options at the item level (refer to the Operations 2 Guide for further information 
on back orders)
▪ generate expiry dates and assign them to inbound product
▪ activate allocation by weight for outbound product
ITSH is a mandatory profile for ITEM. If you do not need to use the above options, you must set up a single 
NA (Not Applicable) profile and set the Enter Expiry Dates field to No. If you intend to use one or more of the 
above options, you may have to set up multiple profiles; for example, one profile with the allocation by weight 
option switched on and another profile with the allocation by weight option switched off.
EXPIRY DATES
Expiry dates serve two functions in AccellosOne 3PL. You can use them to identify product that will expire as 
of a specified cut-off date in reports such as EXRE (Aging by Expy/Rcvd. Report). As well, you can specify 
expiry dates as the basis of your FIFO/LIFO selection when you set up directed picking in PIPR (Picking 
Profile). There are four different options for recording expiry dates for inbound product: 
▪ you can use the receipt date as your expiry or production date
▪ you can enter your expiry dates manually in ENRE or RFCH
▪ your customer supplies expiry dates in a regular date format (MMDDYY, DDYYMM or YYMMDD) or in 
an encoded production date or date code format
PREREQUISITES: DILP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you change the shelf life duration and/or frequency, the change affects 
new inventory only. If you wish to change existing inventory as well, you 
must run REEX (Reset Inventory Expiry Date).
OTHER REQUIREMENTS: If you are converting an inventory level into an expiry date, you will 
require a formula

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
▪ your customer supplies an encoded production date or date code and from this date you wish to calculate an expiry date
FORMULA 
REQUIRED
INVENTORY LEVEL 
REQUIRED ITSH SETUP
you do not use expiry dates None No inventory level required for 
expiry date.
Set the Enter Expiry Dates flag to 
No.
you use your receipt date or current 
system date as your expiry or production date
None No inventory level required for 
expiry date.
Set the Enter Expiry Dates flag to 
Yes and the Expiry Date Derived 
from field to CD (Company Date) 
and the Expiry Date Formula field 
to !CD.
you enter your expiry dates manually in ENRE or RFCHNone No inventory level required for 
expiry date.
Set the Enter Expiry Dates flag to 
Yes and bypass the Expiry Date 
Derived from field.
you enter a date or date code as an 
inventory level in ENRE or RFCH 
and wish to use this date as your 
expiry date
Formula required to convert 
code to a MMDDYY format.
Inventory level set up in DILP 
required for date or date code.
Set the Enter Expiry Dates flag to 
Yes and enter your inventory level 
and date conversion formula.
you enter a date or date code as an 
inventory level in ENRE or RFCH 
and wish to add a specified number 
of days or months to this date in 
order to arrive at your expiry date
Formula required to convert 
code to a MMDDYY format. 
Product’s shelf life added to this 
date to arrive at the expiry date.
Inventory level set up in DILP 
required for date or date code.
Set the Enter Expiry Dates flag to 
Yes and enter your inventory level 
and date conversion formula. Then 
enter your shelf life duration and 
frequency values.
FIELD DESCRIPTIONS
Item Shipping Profile 
Code
Mandatory
Your item shipping profile code. For example, EXP1 for Expiry Date 1 or NA 
for Not Applicable.
Description Mandatory
Your item shipping profile code description
Generate Back Orders at 
Inventory Level
See the back orders section of the Operations 2 Guide for further information 
on this field.
Allow Future Orders Reserved for future use

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
Use Substitute Item 
Codes
See the item substitution section in the Operations 2 Guide.
Dynamic Shelf Life Calculation MethodSee the allocating product by shelf life section of Allocation and Wave Manager for further information on this field.
Enter Expiry Dates N = No
Y = Yes
If you set this field to No, no expiry date will be assigned to a receipt line in 
ENRE. If you set this field to Yes, you can enter an expiry date for each receipt 
line in ENRE. 
Expiry Date Derived from Only available if you set the Enter Expiry Dates field to Yes
CD (Company Date)
LEV2
LEV3
LEV4
RD (Received Date)
If you are using the receipt date or current system date as your expiry date, 
select CD (Company Date). If your expiry dates are based on an inventory 
level, you must select the inventory level in this field. If you are using the 
receipt confirmation date in CHRF/CORL, use RD (Received Date).
NOTE If you rereceive inventory, the new inventory will have the same 
expiry date as the original inventory. For example, if you receive item A, lot 1, 
on Jan. 10 and assign it an expiry date of Jan. 30, any further inventory 
received for this item and lot — regardless of the date that it is received — will 
expire on Jan. 30.
Expiry Date Formula Only available if you select an option in the Expiry Date Derived from field
If your expiry dates are based on an inventory level that requires decoding, 
you enter the decoding formula in this field. This formula is normally provided 
by HighJump.
If you selected Company Date in the previous field, enter !CD as your expiry 
date formula. If you selected Received Date in the previous field, enter !RD as 
your expiry date formula.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
Expiry Date Format Only available if you select an option in the Expiry Date Derived from field
The format of your expiry dates expressed in Oracle date format (for example, 
YYDDMM, MMDDYYYY, YYDDD, etc.).
NOTE Single-digit year formats such as YDDD are not recommended.
Shelf Life Duration Only available if you select an inventory level in the Expiry Date Derived from 
field
If you are using production dates/date codes, you can enter a shelf life in days 
or months to allow AccellosOne 3PL to calculate the expiry date automatically. 
AccellosOne 3PL adds the value that you enter in this field to the production 
date to arrive at the expiry date.
For example, if a product was produced on July 1 and you set the shelf life to 
three months, the product will expire on October 1.
If you enter a negative value in this field, you can advance the expiry date to 
an earlier date. For example, if your customer does not want product shipped 
if it will expire within two months, you can enter -2 in this field to advance the 
expiry date. 
If you change your shelf live duration or shelf life frequency and you want the 
change to apply to existing inventory, you must run REEX (Reset Inventory 
Expiry Date).
Shelf Life Frequency Only available if you enter a shelf life duration
D = Days
M = Months
See Shelf Life Duration field above.
Ship by Weight D = Disallowed
G = Gross
N = Net
If you select either Gross or Net, you can allocate outbound product by weight 
instead of number of pieces. If you select D for Disallowed, no allocation by 
weight is allowed. See the section “Allocation by Weight” in Allocation and 
Wave Manager for further information on shipping by weight.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
Ship by Weight Rounding MethodD = Down
U = Up
If you select U for Up, allocation will ship one or more additional units of inventory to ensure that the weight to be shipped is always reached. If you select D 
for Down, allocation will stop allocating additional units of inventory just before 
the shipping weight is reached. 
For example, if each case weighs 8 lbs and you enter a ship weight of 50 lbs, 
allocation will ship 7 cases or 56 lbs if you round up. If you select the round 
down option, allocation will ship 6 cases or 48 lbs.
Automatic Hold Code for 
Expired Inventory
If you specify a hold code for expired product in this field, when inventory 
belonging to the item that your ITSH profile is attached to expires, AccellosOne 3PL will automatically place it on that hold code.
NOTE Hold codes for expired inventory require a cron job set up by 
HighJump.
Number of Days Identifying Stale ProductThe number of days before expiry that must be reached before a product is 
considered stale. When the number of days before expiry is reached, the 
inventory entity is automatically put on “stale” hold. If the inventory entity is still 
in the warehouse on the expiry date, the “stale” hold code is changed to your 
“expired” hold code.
NOTE Stale product holds require a cron job set up by HighJump.
Automatic Hold Code for 
Stale Product (HOLD)
The hold that you wish to use to identify stale product. 
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
The following fields allow you to define expiry/production date rules for product received in ENRE/RFCH 
and positive adjustments made in ENAJ and MATR. Inbound product that violates these rules (that is, an 
insufficient shelf life) will be rejected as outside the acceptable date range for this product.
ENRE screen showing out of range message
If you attach the special verify program MMSO (Min/Max Expiry/Prod. Date Supervisor Over.) to your 
CORE flow in DIFP, receipt lines that failed expiry/production date validation in RFCH will display in CHRF. 
If the supervisor override option has been activated, a supervisor will be prompted to logon and authorize 
the violation of expiry/production date rules.
Assign by Production 
Date or Expiry Date
E = Expiry Date
P = Production Date
The date that you wish to validate.
Shelf Life Duration Reserved for future use.
Supvr. Override Min./
Max. Expiry/Production 
Date
N = No
Y = Yes
If you set this flag to Yes, a supervisor can override violations to expiry date/
production date rules in RF and at receipt confirmation. If you set this flag to 
No, there is no override for violations to expiry date/production date rules.
Minimum Expiry Date 
Days
The minimum range in days to expiry.
Maximum Expiry Date 
Days
The maximum range in days to expiry.
Maximum Production 
Date Days
The maximum range in days from the production date. A value of zero is 
acceptable.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Shipping Profile (ITSH)
PROCEDURE
1 Enter ITSH.
2 Click on Enter Criteria then Execute Query to see which item shipping profiles have already been set up.
3 If you need a new item shipping profile, click on Create Record.
4 Key in an item shipping profile code and press Enter.
5 Key in a description for your profile and press Enter.
6 If your cursor is positioned in Generate Back Orders at Inventory Level field, press Enter to bypass this 
option.
7 Press Enter to bypass the Allow Future Orders field.
8 In the Use Substitute Item Codes field, key in N for No and press Enter.
9 Press Enter to bypass the Dynamic Shelf Life Calculation Method field.
10 In the Enter Expiry Dates field, key in Y for Yes or N for No and press Enter. If you select No, proceed to 
step 14.
11 In the Expiry Date Derived from field, use your pick list function to select an appropriate inventory level or 
press Enter to bypass this field if you are not using a formula to convert your date codes. 
To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve 
the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click 
on Select Code. 
12 If you selected an inventory level in the previous step, key in your expiry date formula provided by 
HighJump and press Enter. 
Then key in the format of your expiry dates in the Expiry Date Format field and press Enter.
13 If you need to add a specified number of days or months to your date in order to arrive at an expiry date, 
key in a shelf life duration and press Enter. If you do not need a shelf life duration, press Enter to bypass 
this field.
If you specified a shelf life duration, key in your shelf life frequency (D for Days or M for Months) and 
press Enter.
14 In the Ship by Weight field, key in D for Disallowed and press Enter.
15 In the Automatic Hold Code for Expired Inventory field, key in your hold code for expired product or press 
Enter to bypass this field.
16 if you wish to track stale product, enter the number of days for stale product and press Enter. Then enter 
your hold code for stale product.
17 Press Enter to bypass the remaining fields in ITSH.
18 When you finish entering your item shipping profile, click on Return to Main.

ITEM PROFILE SETUP
Item Process Profile (IPRP)

Item Shipping Profile screen showing expiry dates based on inventory level 3
19 Click on Exit to exit.
Item Process Profile (IPRP)
OVERVIEW
In this program, you set up an N/A (Not Applicable) item process profile code. An N/A code in IPRP is 
required because IPRP is a mandatory profile for ITEM. In ITEM you will attach this profile to all your items.
If you use item process codes to capture item-specific information such as serial numbers, catch weights or 
temperatures, refer to the item process values section of the Operations 2 Guide for complete setup instructions.
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Item Process Profile (IPRP)
PROCEDURE
1 Enter IPRP.
2 Click on Enter Criteria then Execute Query to see whether an N/A code has already been set up.
3 If you need a new item process profile, click on Create Record.
4 Key in N/A as your process profile code and press Enter.
5 Key in a description for your code and press Enter.
6 Click on Master Block to exit the Detail Block.

Item Process Profile Code screen
7 Click on Exit to exit.
FIELD DESCRIPTIONS
Process Profile Code Mandatory
Your process profile code. For example, N/A for Not Applicable.
Description Mandatory
Your process profile code description

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
Item Quantity Breakdown Profile (IQBP)
OVERVIEW
In this program, you set up the quantity breakdowns for your items. The quantity breakdown defines which 
SKU types (pallets, eaches, pieces, barrels, rolls, etc.) you wish to use to record the quantities of an item for 
tracking and billing purposes. You can define up to five different SKU types in a single quantity breakdown 
profile. 
Some typical quantity breakdowns are:
▪ pallets/cases
▪ pallets/cases/eaches
▪ cases/retail packs
▪ bales
A quantity breakdown can contain both unit-based SKU types and a unit of measure such as weight or a 
linear measurement. For example, the following quantity breakdowns are supported:
▪ rolls/meters
▪ totes/pounds
By using meters and pounds in your quantity breakdown, you can ship partial quantities of rolls and totes.
In IQBP you define the SKU types that an item’s quantity can be expressed in; for example, PALLETS/
CASES. In ITEM, you define the relationship between these SKU types or the actual quantities — that is, the 
number of cases to a pallet, the number of eaches in a box, the number of meters in a roll, etc.
You must set up one quantity breakdown profile for each item with a different quantity breakdown. For 
example, customer A receives item 123 in cases/pieces but item 456 in cases only. In this case, you would 
PREREQUISITES: SKUS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all SKU types used by your customers
NOTE Do not confuse the quantity breakdown with inventory levels. The quantity 
breakdown describes how much do I have of an item; for example, I have 3 pallets 
and 15 cases of item X. Inventory levels, on the other hand, describe what exactly 
item X is; for example, the color, size, production date, expiry date, serial number, etc. 
of item X.

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
need two quantity break-down profiles: one for item 123 (CASES/PIECES) and another for item 456 
(CASES). 
IQBP also defines the default SKU types for shipping, receiving, adjustments, etc. The defaults in this profile 
override any defaults that you set in CUST.
FIELD DESCRIPTIONS
Quantity Breakdown Profile CodeMandatory
Your quantity breakdown profile code. For example, PC for Pallets/Cases or 
CASE for Cases Only.
Description Mandatory
Your quantity breakdown profile code description
Qualifier Code Mandatory
The unit of measure for the SKU type. Use UNIT for SKU types consisting of a 
physical object such as case, pallet, each, drum, etc.

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
SKU Block
SKU Code (SKUS) Mandatory
CAUTION The SKU type for this quantity breakdown. The SKU type that 
you enter in this field (for example, pallets, eaches, cartons, boxes, etc.) must 
match your billing SKU type for the item IQBP is going to be attached to. If the 
two SKU types do not match, you may not be able to bill the item.
EXAMPLE
You set up a charge code in CHAR called ABC and your charge on SKU type 
in that charge code is CS (Cases). Cases are assigned to SKU class 3 (Cases 
and the like) in SKUS. Then you attach your ABC charge code to your item 
billing profiles: IISP, IRSP and IHAP. 
In order to be able to bill, one of the SKU types that you enter in IQBP must 
belonging to the same SKU class (that is, SKU class 3). If, for example, your 
item billing profiles are charging by pallet (SKU class 1) and your item quantity 
breakdown profile is defined as boxes (SKU class 3), AccellosOne 3PL will be 
unable to rate your receipt.
Receipt Process Y = Yes
N = No
If you set this field to Yes, you can receive in the SKU type that you specified 
in the previous field. If you set this field to No, you cannot receive in the SKU 
type that you specified in the previous field.
This field must be set to Yes for one SKU type in every profile. If your quantity 
breakdown is PALLETS/CASES and you set this flag to Yes for pallets and to 
No for cases, you will be able to receive in pallets only. If you wish to receive 
in pallets and cases, you must set this flag to Yes for both SKU types.
Shipment Process Y = Yes
N = No
If you set this field to Yes, you can ship in the SKU type that you specified in 
the SKU Code field. If you set this field to No, you cannot ship in the SKU type 
that you specified in the SKU Code field.
This field must be set to Yes for one SKU type in every profile. If your quantity 
breakdown is CASES/PIECES and you set this flag to Yes for cases and to No 
for pieces, you will be able to ship in cases only. If you wish to ship in cases 
and pieces, you must set this flag to Yes for both SKU types.

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
Report Process Y = Yes
N = No
If you set this field to Yes, AccellosOne 3PL will show quantities in LOEN in 
the SKU type that you specified in the SKU Code field. If you set this field to 
No, AccellosOne 3PL will show quantities in LOEN in another SKU type that 
you specify.
EXAMPLE
Suppose an item has a quantity breakdown of pallets/cases/eaches and there 
are 10 eaches in a case and 50 cases on a pallet. The available quantity is 
1,015 eaches.
Example 1
Report Process flag = N for Pallets
Report Process flag = N for Cases
Report Process flag = Y for Eaches
Available quantity in LOEN = 1,015 eaches
Example 2
Report Process flag = N for Pallets
Report Process flag = Y for Cases
Report Process flag = Y for Eaches
Available quantity in LOEN = 101 cases 5 eaches
This field must be set to Yes for one SKU type in every profile.
Invoice Report Process Y = Yes
N = No
This field determines which SKU type(s) that you wish to appear on your 
invoices. For example, if you set this field to Yes for pallets, the word “pallets” 
will appear on your invoices.
If you use non weight-based billing, you must set this field to Yes for whichever SKU type(s) you are billing on as defined in IISP, IRSP and IHAP. If you 
use weight-based billing, you can set this field to Yes for any SKU type.
SKU Block

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
Adjustment Process Y = Yes
N = No
This flag refers to the following programs:
ENAJ (Enter Inventory Adjustment)
RELO (Relocate Inventory)
HOAD (Inventory Hold Adjustments)
If you set this field to Yes, you will be able to make adjustments in the above 
programs in the SKU type that you specified in the SKU Code field. If you set 
this field to No, you will not be able to make adjustments in this SKU type.
This field must be set to Yes for one SKU type in every profile. 
Layer Configuration 
Required
Y = Yes
N = No
Layer configuration refers to the hi and the tie (that is, the number of layers on 
a pallet and the number of items per layer). If you set this field to Yes, AccellosOne 3PL will require this information to be entered when you set up an item 
in ITEM. If you set this field to No, this information will not be required in ITEM.
Layer configuration is not required for single level quantity breakdowns (for 
example, pallets only) or multi-level quantity breakdowns when one breakdown is a unit of measure rather than a physical object (for example, rolls/
meters).
In all other cases, layer configuration must be set to Yes if you wish to perform 
directed put-away.
SKU Block

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
PROCEDURE
1 Enter IQBP.
2 Click on Enter Criteria then Execute Query to see which item quantity breakdown profiles have already 
been set up.
3 If you need a new item quantity breakdown profile, click on Create Record.
4 Key in an item quantity breakdown code and press Enter.
Rounding Code The Round Up, Truncate and Round Down options are only available for a single SKU type. All other SKU types must be assigned the No Rounding rounding code.
This option is only available for customers with a single inventory level.
R = Round Down (round up if greater than 50%; otherwise round down)
T = Truncate
U = Round Up (always round up)*
N = No Rounding
This field allows you to define how you want to round the shipped quantity of 
an order so that you avoid the need to break a case, inner pack or some other 
SKU code. For example, suppose your quantity breakdown is as follows:
CASE = 1
INNER PACK = 10 (10 inner packs per case)
EACH = 12 (12 eaches per inner pack)
You receive an order for 100 eaches or 8.3 inner packs. If you select Round 
Down, AccellosOne 3PL will ship 8 inner packs or 96 eaches. If you select 
Truncate, AccellosOne 3PL will ship 8 inner packs or 96 eaches. If you select 
Round Up, AccellosOne 3PL will ship 9 inner packs or 108 eaches.
You set the Rounding Code flag to the appropriate value at the SKU level 
below the SKU level that you are rounding up or down to. In the example 
above, you would activate rounding for your eaches SKU — not for your inner 
pack SKU.
The following conditions must be met before rounding will take place:
▪ the order quantity of the order line must consist of a single SKU type (for 
example, 100EA not 10CS 5EA)
▪ the Break Quantity at SKU Class field in PIPR must be set to break at any 
SKU class
*Not available for highest SKU.
SKU Block

ITEM PROFILE SETUP
Item Quantity Breakdown Profile (IQBP)
5 Key in a meaningful description for your code (for example, “pallets and cases” or “pallets/cases/
eaches”) and press Enter.
6 Use your pick list function to select an appropriate qualifier code (usually UNIT). To select a code using a 
pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then 
use your arrow keys to position your cursor over the appropriate code and click on Select Code.
AccellosOne 3PL will assign level 1 to this SKU type and position your cursor in the SKU Code field.
7 Use your pick list function to select an appropriate SKU type.
8 In the Receipt Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to 
define which SKU types you wish to receive in.
9 In the Shipment Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to 
define which SKU types you wish to ship in.
10 In the Report Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define 
which SKU types you wish to report in.
11 In the Invoice Report Process field, key in the appropriate value (Y for Yes or N for No) and press Enter 
to define which SKU types you wish to appear on your invoices. 
12 In the Adjustment Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to 
define which SKU types you wish to make adjustments to in ENAJ, RELO and HOAD.
13 In the Layer Configuration Required field, key in the appropriate value (Y for Yes or N for No) and press 
Enter.
14 In the Rounding Code field, key in the appropriate value (R for Round Down, T for Truncate or U for 
Round Up) and press Enter.
CAUTION Make sure that the SKU type that you use for the Invoice Report 
matches the SKU type that you are charging on in your item billing profiles.

ITEM PROFILE SETUP
Item Alternate Sorts (ITAS)

Item Quantity Breakdown Profile showing prompt for second SKU type
15 If you are setting up a quantity breakdown profile consisting of a single SKU type, your profile is complete. Press Return to Main to exit create mode. Then click on Master Block and Exit to exit the program. 
If you are setting up a quantity breakdown profile consisting of multiple SKU types (for example, PALLETS/CASES/EACHES or CASES/RETAIL PACKS), you must set up the other SKU types. Enter your 
next SKU type following the steps outlined above. 
16 When you finish entering all your SKU types for this profile, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit.
Item Alternate Sorts (ITAS)
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Item Alternate Sorts (ITAS)
OVERVIEW
In this program, you define your alternate reporting type codes. Alternate reporting type codes serve three 
functions:
▪ you can use them in the programs INAS (Inventory Report by Alternate Sort) and INAI (Inventory by 
Alternate Sort - Item Level) to generate consolidated inventory reports showing all product of a specific 
type regardless of customer
▪ you can use them to rename an item in your inventory reports (for example, you receive an item called 
OFFICE DESK #1 and you wish to list it in an inventory report under another name — say, 497-4678-A)
▪ you can use them to group items for billing purposes (for example, all items belonging to the same product line can be treated as a single item for billing purposes)
The same item can be assigned multiple alternate reporting type codes.
CONSOLIDATED INVENTORY REPORTS
If you have a customer who deals in meat, dairy products and fish, and you want to know how much meat this 
customer has in your warehouse, you would use ITAS.
You would set up an ITAS code for meat and attach it to all this customer’s meat items. Then you would run 
an inventory report in INAS specifying the meat code as your alternate reporting type. The report would show 
all meat items for this customer.
ITAS is similar to DEAS (Depositor Alternate Sorts). ITAS defines alternate sorts at the item level while DEAS 
defines alternate sorts at the customer level. DEAS is always customer specific while ITAS can be attached to 
any item belonging to any customer.
The codes that you create in this program can be either single level or double level. For example, if you 
create a code for ICE CREAM, this is considered a single-level alternate sort. If, however, you want to track 
both ice cream in general and particular flavours of ice cream, you would have to break down your ICE 
CREAM code into VANILLA, CHOCOLATE and STRAWBERRY. This is considered a double-level alternate 
sort. 
If you wish to … setup required …
generate consolidated inventory reports▪ create a single level or double level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block 
in ITEM
▪ when you run inventory reports in INAS or INAI, specify the alternate reporting type that you created in ITAS
Item 1
meat
Item 2
fish
Item 3
dairy
Item 4
meat
Item 5
fish
Item 6
meat
MEAT

ITEM PROFILE SETUP
Item Alternate Sorts (ITAS)
rename an item in an inventory report▪ create a single level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block 
in ITEM
▪ when you run inventory reports in INAS or INAI, specify the alternate reporting type that you created in ITAS
group items for billing purposesAlternate billing applies to renewal storage only and 
overrides any renewal storage options that you set up in 
DILP. Alternate billing is not available for initial storage 
charges.
Alternate billing must be applied to all of a customer’s 
items. You cannot mix alternate billing and regular billing 
within the same customer.
▪ create a single level or double level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block 
in ITEM for all items in the group
▪ attach the same ITAS code to your DBIP profile
FIELD DESCRIPTIONS
Alternate Inventory 
Reporting Type
Mandatory
Your alternate inventory reporting type code. For example, USDA for USDA 
Tracking.
Description Mandatory
Your alternate inventory reporting type code description
Alternate Inventory 
Reporting Code
Mandatory
If you are setting up a single-level alternate sort, your code in this field will be 
the same as your code in the Alternate Inventory Reporting Type field. If you 
are setting up a double-level alternate sort, you would enter your second level 
alternate sort code in this field.
If you wish to … setup required …

ITEM PROFILE SETUP
Item Alternate Sorts (ITAS)
PROCEDURE
1 Enter ITAS.
2 Click on Enter Criteria then Execute Query to see which alternate reporting types have already been set 
up. 
3 If you need a new alternate reporting type, click on Create Record.
4 Key in an alternate reporting type code and press Enter.
5 Key in your description and press Enter.
6 Key in your second code and a meaningful description and press Enter after each entry.
7 Press Enter to bypass the Billing Code field.
8 Repeat the above steps for each additional second-level code that you wish to add.
Description Mandatory
If you are setting up a single-level alternate sort, your description in this field 
will be the same as your description for your alternate inventory reporting type 
code. If you are setting up a double-level alternate sort, you would enter your 
second level alternate sort description in this field.
Billing Profile Code
(defined in IBIP)
Optional
Refer to the section on alternate billing groups in the Billing and Invoicing 
Guide.
If you are creating a single-level 
alternate sort code:
If you are creating a double-level 
alternate sort code:
a) Key in the same code and 
description that you entered in 
the Main Block and press Enter 
after each entry. 
b) Press Enter to bypass the Billing 
Code field.
c) Click on Return to Main to exit 
create mode. Then click on Master Block and Exit to exit.
a) Proceed to next step.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Hold Types (HOLD)

Item Alternate Sorts showing double-level codes
9 When you finish entering your second-level codes for this reporting type, click on Return to Main to exit 
create mode. Then click on Master Block and Exit to exit.
Hold Types (HOLD)
OVERVIEW
In this program, you set up your hold codes. You use hold codes to put product on hold in programs like 
POHO and HOAD. You can also attach a hold code to a location in LOCA so that product placed in that 
location is automatically assigned that hold code. When a product is on hold, it can be either shippable like 
normal product or non-shippable (non-shippable product is product that cannot be shipped until the hold is 
removed).
You can use hold codes for product damaged in the warehouse, product damaged in transit, products that 
need a quality assurance inspection, etc. Some sample hold codes are:
Damaged Hold
Customer Hold
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
IHOP (Item Hold Profile)
HOSP (Hold Shipping Sequence Profile Code)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A list of all the reasons why you put product on hold in your warehouse

ITEM PROFILE SETUP
Hold Types (HOLD)
USDA Inspection
Repair Return
FIELD DESCRIPTIONS
Hold Type Mandatory
Your hold type code.
Description Mandatory
Your hold type description.
Ship If you define a hold type as shippable, the product is shippable despite the 
hold. If you define a hold type as non-shippable, you will have to remove the 
hold before you can ship the product.
Renew If you define a hold type as renewable, renewal storage will be charged on 
product to which this hold type has been attached. If you define a hold type as 
non-renewable, no renewal storage will be charged on product to which this 
hold type has been attached.
Bond If you define a hold type as a bond hold, the hold type can be used in the bond 
system to place product on bond hold. If you define a hold type as a non-bond 
hold, the hold type is a regular non-bond hold type.
Dmg Reserved for future use.
Breakable Inventory If you define a hold type as breakable, you can relocate and make hold adjustments to partial quantities. For example, if you have 10 cases of product (say, 
item A, lot 101) on a breakable hold called DMG, you can relocate a partial 
quantity such as 5 cases to another location in RELO and you can remove a 
partial quantity such as 3 cases from hold in HOAD.
If you define a hold type as non-breakable, the following will occur:
▪ When relocating a specific inventory entity in RELO, the entire entity on the 
non-breakable hold must be relocated; you cannot relocate partial quantities. 
▪ When placing a specific inventory entity on non-breakable hold in HOAD, 
you must place the entire entity on hold.
▪ When removing a specific inventory entity from non-breakable hold in 
HOLD, you must remove the entire entity.
QA Reserved for future use.

ITEM PROFILE SETUP
Hold Types (HOLD)
Res. Reserved for future use.
Disabled EDI Send If you select this option, the hold type will be excluded from EDI hold adjustment transactions. 
For example, if BL (Blast Hold) is checked, EDI transactions will not report on 
blast hold transactions for inbound or outbound product. So when the warehouse ABC Foods puts product received from customer A on blast hold, customer A will not be notified of the blast hold activity in its EDI transactions.
e-Vista Activation in e-Vista at both the account and user level required
If you select this option, your customers can place product on hold in the 
Inventory Balances tab of e-Vista using this hold type. If you do not select this 
option, the hold type will not be available in the Inventory Balances tab of eVista.
Auto Take-Off Only available for non-bond holds
If you define a hold type as non-auto take-off, the hold must be manually 
removed. If you define a hold type as auto take-off, the hold will be removed 
after the number of days specified in the Days field has passed or on the date 
that you specify in the Date field. To activate auto take-off, you must run the 
program HATO (Holds Auto Take-Off).
Days Only available if Auto Take-Off flag set to Yes
Specifies the number of days for auto take-off holds. AccellosOne 3PL calculates the date by adding the number of days plus one day to the current date. 
For example, if you place product on hold on January 1 and the number of 
days is 5, the hold will come off on January 7 (January 1 + 5 = January 6 + 
one day = January 7).
If you wish to set up a 24-hour hold, use zero as your number of days value. 
For example, product is placed on hold on March 10 and the hold is removed 
at midnight or on March 11.
If you enter a number of days value, you cannot enter a an auto take-off date.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Hold Types (HOLD)
PROCEDURE
1 Enter HOLD.
2 Click on Enter Criteria then Execute Query to see which hold types have already been set up.
Hours Only available if Auto Take-Off flag set to Yes
Specifies the number of hours for auto take-off holds.
Date Only available if Auto Take-Off flag set to Yes
Specifies the auto take-off date. You can change this date whenever required 
and the change will apply to existing inventory in your warehouse.
If you enter an auto take-off date, you cannot enter a number of days value.
RF Hold Excl From If you select RF Hold Excl From, you cannot remove this hold code from product in RFHO. If you leave this checkbox unselected, there are no restrictions 
related to this hold code in RFHO. 
RF Hold Excl To If you select RF Hold Excl To, you cannot attach this hold code to product in 
RFHO. If you leave this checkbox unselected, there are no restrictions related 
to this hold code in RFHO. 
Excl From Count Back If you select this checkbox, any product on this hold code will be excluded 
from the system count during a count back. If you leave this checkbox 
unselected, the system count will include all product in a given location 
regardless of its hold status.
Picking Profile If you attach a picking profile set up in PIPR to a hold type, any order lines 
placed on that hold type will be allocated according to the hold type’s picking 
profile; that is, the customer’s item’s or consignee’s picking profile will be overridden by the hold type’s picking profile.
This feature makes it possible to define special picking rules for expired product by creating a hold type for expired product, assigning it a unique picking 
profile and then attaching your new hold type to your expired inventory. When 
you run allocation, AccellosOne 3PL will use the hold type’s picking profile 
rather than the regular picking profile(s) attached to the customer, item or consignee
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Hold Shipping Sequence Profile Code (HOSP)

Hold Types
3 If you need a new hold type, click in the empty Hold field after your last hold type record. If there are no 
blank lines on your screen, click on New to create one.
4 Key in your hold code and press Enter.
5 Key in a description for your new hold code and press Enter.
6 Click on the appropriate checkboxes to select your hold type options.
7 If you selected the Auto Take-Off option, key in the number of days or the auto take-off date.
8 If required, select the RF Hold Excl From, the RF Hold Excl To and/or the Exclude From Count Back 
checkbox(es).
9 If required, select a picking profile from the pick list for your new hold type.
10 When you finish entering your hold types, click on Save to save your new hold type.
11 Click on Exit to exit HOLD.
Hold Shipping Sequence Profile Code (HOSP)
PREREQUISITES: HOLD
ATTACHED TO: IHOP (Item Hold Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Hold Shipping Sequence Profile Code (HOSP)
OVERVIEW
This program allows you to set up order allocation so that AccellosOne 3PL selects inventory entities based 
on hold codes. You specify in HOSP which hold codes you want to allocate first, which hold codes you want to 
allocate second and so on and so forth.
EXAMPLE
The allocation routine will attempt to fill the order line by selecting product to which you have assigned the 
Quality A hold. Once all the Quality A product has been allocated, if the order remains unfilled the allocation 
routine will look for product with a hold code of Quality B. Once all the Quality B product has been allocated, if 
further product is required the allocation routine will search for Quality C product.
If there remains product to be allocated and the allocation routine runs out of product on holds A, B and C, 
then the order line is left not fully allocated.
SEQUENCE HOLD CODE
1 Quality A
2 Quality B
3 Quality C
FIELD DESCRIPTIONS
Hold Shipping Sequence 
Profile Code
Mandatory
Your hold shipping sequence profile code.
Description Mandatory
Your hold shipping sequence profile description.
Sequence Number Mandatory
The sequence number for the hold code; for example, 1, 2, 3, 4, etc.

ITEM PROFILE SETUP
Hold Shipping Sequence Profile Code (HOSP)
PROCEDURE
1 Enter HOSP.
2 Click on Enter Criteria then Execute Query to see which hold shipping profiles have already been set up. 
If you need a new hold shipping profile, click on Create Record.
3 Key in a profile code and press Enter.
4 Key in a description for your new profile code and press Enter.
5 Starting at 1, key in your sequence number for the hold code and press Enter.
6 Key in your hold code for the sequence and press Enter or use your pick list function to select it. To select 
a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick 
list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code.
7 Repeat the above two steps for each additional hold code that you wish to add to the profile.

Hold Ship Profile Code
8 When you finish entering your hold codes for this profile, click on Return to Main to exit create mode. 
Then click on Exit to exit.
Hold Code (HOLD) Mandatory
The hold code for the sequence. Any holds that you enter in this field must be 
defined as shippable holds in HOLD. The hold code for the first sequence 
must be the same as the outbound hold code that you define in IHOP.
EXAMPLE 
Sequence in HOSP
1
2
3
Outbound Hold Code in IHOP
1
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Hold Profile (IHOP)
Item Hold Profile (IHOP)
OVERVIEW
In this program, you set up your item hold profiles. An item hold profile defines your inbound and outbound 
hold codes. You use an inbound hold code when you wish to place an item on automatic hold whenever it is 
received in ENRE. You use an outbound hold code when you wish to ship only product that has been 
assigned that hold code. If required, the same item can be assigned one inbound hold code and on another 
outbound hold code.
For example, if you have a product that requires blast freezing, you would create an item hold profile for blast 
freezing. In the profile you would assign your blast freezing hold code as the profile’s inbound hold code. 
Then you would attach the profile to the item in ITEM. 
PREREQUISITES: HOLD, HOSP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Hold Profile Code Mandatory
Your hold profile code.
Description Mandatory
Your hold profile code description.
Inbound Hold Code 
(HOLD)
Optional
The hold code that you wish to attach to an item when it is inbound. If you create new inventory in ENAJ (Enter Inventory Adjustment), the hold code will be 
automatically attached to it.

ITEM PROFILE SETUP
Item Hold Profile (IHOP)
INBOUND LOCATION TYPE BLOCK
This block allows you to define a relationship between an inbound hold code and location type code. The 
Inbound Location Type block is only available when the Inbound Hold Code field is not populated in the 
header.
When you confirm the receipt, the hold code defined in the Inbound Location Type Block will be applied to the 
receipt line/receipt location line if the put-away location's location type matches the location type in the 
Inbound Location Type Block. If a hold code has been assigned to a receipt line or receipt location line in 
ENRE, it will override the hold code defined in the Inbound Location Type Block.
Allow Override of Hold 
Code During Core RF 
Receiving
Only available for core RF receiving
Y = Yes
N = No
If you set this flag to Yes, you can override or remove automatic holds when 
receiving in RFCH or RFPU. If you set this flag to No, you cannot override or 
remove automatic holds in RFCH or RFPU.
Outbound Hold Code 
(HOLD)
Only mandatory if you wish to define a hold ship sequence in HOSP
The hold code that product must be attached to before it can be allocated in 
an outbound order. The hold code that you enter in this field must match the 
hold code in your first sequence in HOSP.
Hold Ship Sequence Profile Code (HOSP)
Optional
If you set up a hold ship sequence profile in HOSP, the allocation routine will 
select product based on hold code. For example, first allocate all product to 
which you have assigned your Quality A hold, then if the order remains unfulfilled allocate product assigned your Quality B hold. If the order still requires 
further product, allocate your Quality C hold, etc.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Hold Profile (IHOP)
Inbound Location Type Block (IHOP)
PROCEDURE
1 Enter IHOP.
2 Click on Enter Criteria then Execute Query to see which hold profiles have already been set up.
3 If you need a new hold profile, click on Create Record.
4 Key in a hold profile code and press Enter.
5 Key in a description for your new hold profile code and press Enter.
6 If you want the code to be applied to an item when it is inbound, use your pick list function to select the 
appropriate hold code. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the 
appropriate code and click on Select Code. 
If you do not want an inbound hold code, press Enter to bypass this field.
7 In the Allow Override of Hold Code During Core RF Receiving field, key in Y for Yes or N for No and 
press Enter.
8 If you want the code to be applied to an item when it is outbound, use your pick list function to select the 
appropriate hold code.
If you do not want an outbound hold code, press Enter to bypass this field.
9 If required, key in a hold ship profile code in the Hold Ship Sequence Profile Code field and press Enter 
or press Enter with the field blank to bypass this option.
10 Repeat steps 4 to 9 for each additional hold profile that you wish to add.
11 When you finish entering your hold profiles, click on Return to Main to exit create record mode.

ITEM PROFILE SETUP
Item Incubation Hold Code (IIHO)

Item Hold Profile
12 Click on Exit to exit.
Item Incubation Hold Code (IIHO)
OVERVIEW
In this program, you set up your incubation holds. Incubation holds allow you to define an “incubation” period 
for inbound product during which the product cannot be shipped because it is not yet considered ready. The 
incubation period is based on a fixed number of days from the manufacturing or slaughter date. The hold is 
automatically applied to the product when you confirm the receipt in CHRF. At the end of the incubation 
period, you must release the incubation hold by running HATO (Holds Auto Take-Off).
In order to use incubation holds, the manufacturing or slaughter date must be embedded in one or more 
inventory levels and an SQL statement must be written to extract this date.
PREREQUISITES: HOLD, ITEM, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: The special verify program PIIH (Put Item on Incubation Hold) must be 
attached to the inbound flow CORE (Confirm Receipt) in DIFP

ITEM PROFILE SETUP
Item Incubation Hold Code (IIHO)
You need to set up one record in IIHO for each item that you wish to place on incubation hold.
PROCEDURE
1 Enter IIHO.
2 Click on Enter Criteria then Execute Query to see which incubation holds have already been set up.
3 If you need a new incubation hold code, click on Create Record.
4 In the Customer Code field, key in your customer code and press Enter.
5 In the Item Code field, key in your item code and press Enter.
6 In the Incubation Hold Code field, key in your incubation hold code and press Enter.
7 In the Number of Days field, key in the number of days that the incubation period will last.
NOTE IIHO is used when each item in your warehouse has different incubation 
hold rules. If you have multiple items with the same incubation hold rules, IIHP (Incubation Hold Profile) is the recommended setup program to use.
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer whose product will be placed on incubation hold.
Item Code (ITEM) Mandatory
The product that will be placed on incubation hold.
Incubation Hold Code 
(HOLD)
Mandatory
The incubation hold code for the product. The Auto Take-Off flag in HOLD 
must be set to Y for Yes for this hold code.
Number of Days The number of days from the manufacturing or slaughter date that the incubation period will last.
Date Formula The SQL statement that will extract the manufacturing or slaughter date from 
one or more inventory levels.
Date Format The format of the date being extracted.

ITEM PROFILE SETUP
Incubation Hold Profile (IIHP)
8 In the Date Formula field, key in your SQL statement for extracting the date and press Enter.
9 In the Date Format field, key in your date format and press Enter.

Item Incubation Hold Code screen showing a three-day incubation period based on inventory level 2
10 Repeat the above steps for any additional items that you want placed on incubation hold.
11 When you finish entering your incubation hold, click on Return to Main and then Exit to exit.
12 Enter DIFP and retrieve the workflow profile code for the customer whose product you wish to place on 
incubation hold. Make sure that the special verify PIIH is attached to the inbound flow CORE (Confirm 
Receipt).
Incubation Hold Profile (IIHP)
PREREQUISITES: HOLD, ITEM, CUST
ATTACHED TO: ITEM
GLOBAL/UNIQUE: Unique
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: The special verify program PIIH (Put Item on Incubation Hold) must be 
attached to the inbound flow CORE (Confirm Receipt) in DIFP

ITEM PROFILE SETUP
Incubation Hold Profile (IIHP)
OVERVIEW
IIHP is an alternate version of IIHO. It is used when you have multiple items with the same incubation hold 
code rules. When you attach an incubation hold profile to an item in ITEM and click on Process, AccellosOne 
3PL will automatically create an IIHO record for that customer/item.
PROCEDURE
1 Enter IIHP.
2 Click on Enter Criteria then Execute Query to see which incubation hold profiles have already 
been set up.
3 If you need a new incubation hold profile, Click on New.
4 In the Incubation Hold Profile Code field, key in your incubation hold profile code and press Enter.
5 In the Incubation Hold Code (HOLD) field, key in your incubation hold code and press Enter.
6 In the Number of Days field, key in the number of days that the incubation period will last.
7 In the Date Formula field, key in your SQL statement for extracting the date and press Enter.
8 In the Date Format field, key in your date format and press Enter.
FIELD DESCRIPTIONS
Incubation Hold Profile Mandatory
Your incubation hold profile code.
Description Mandatory
Your incubation hold profile description.
Incubation Hold Code 
(HOLD)
Mandatory
The incubation hold code for the product. The Auto Take-Off flag in HOLD 
must be set to Y for Yes for this hold code.
Number of Days The number of days from the manufacturing or slaughter date that the incubation period will last.
Date Formula The SQL statement that will extract the manufacturing or slaughter date from 
one or more inventory levels.
Date Format The format of the date being extracted.

ITEM PROFILE SETUP
Incubation Hold Profile (IIHP)

Item Incubation Hold Profile screen showing a three-day incubation period based on inventory level 2
9 When you finish entering your incubation hold, click on Save to save your changes.
10 Click on Exit to exit.
11 Enter DIFP and retrieve the workflow profile code for the customer whose product you wish to place on 
incubation hold. Make sure that the special verify PIIH is attached to the inbound flow CORE (Confirm 
Receipt).
ATTACHING YOUR INCUBATION HOLD CODE TO AN ITEM
When you attach an incubation hold profile to an item in ITEM and click on Process, AccellosOne 3PL will 
automatically create an IIHO record for that customer/item.
1 Enter ITEM.
2 Retrieve the item that you wish to set up for incubation holds.
3 Click on IIHO Block.

ITEM PROFILE SETUP
Freight Class Codes (CLAS)
ITEM screen showing IIHO Block
4 Key in your incubation hold profile code and press Enter.
5 Click on Process.
6 Press F4 to exit.
Freight Class Codes (CLAS)
OVERVIEW
In this program, you set up your freight class codes. Freight class codes are required for the commodity code 
or National Motor Freight Class (NMFC) system of freight classification. Freight class and commodity codes 
are normally printed on your bill of lading.
If you use AccellosOne Transport and charge different rates based on the class of freight, you must set up 
one class code for each class of freight. If you do not use AccellosOne Transport and do not require 
commodity codes and class codes on your bill of lading, use AccellosOne 3PL class FAK (Freight All Kinds) 
for all your items. 
PREREQUISITES: None
ATTACHED TO: COMM (Commodity) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Freight Class Codes (CLAS)
PROCEDURE
1 Enter CLAS.
2 Click on Enter Criteria then Execute Query to see which freight class codes have already been set up.

Freight Class Codes
3 If you need a new freight class code, click on Create Record.
4 Key in a freight class code and press Enter.
5 Key a description for your new freight class code and press Enter.
6 Repeat steps 4 and 5 for each additional freight class that you wish to enter.
7 When you finish entering your freight class codes, click on Return to Main and then Exit to exit.
FIELD DESCRIPTIONS
Freight Class Code Mandatory
Your freight class code.
Description Mandatory
Your freight class code description.

ITEM PROFILE SETUP
Commodities (COMM)
Commodities (COMM)
OVERVIEW
In this program, you set up your commodity codes. Commodity codes are required for the National Motor 
Freight Class (NMFC) system of freight classification and are used primarily for freight rating purposes in 
AccellosOne Transport. Commodity codes are normally printed on your bill of lading; this requires special 
programming by HighJump. If required, you can attach message text to your commodity code and print it on 
your bill of lading.
If you do not need commodity codes on your bill of lading, use AccellosOne 3PL commodity code FAK 
(Freight All Kinds) for all your items.
PREREQUISITES: CLAS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Commodity Code Mandatory
Your commodity code.
Subcode Mandatory
Your commodity subcode. If you are setting up a single commodity code, use 
00 in this field.
Freight Class
(defined in CLAS)
Mandatory
Your freight class code.

ITEM PROFILE SETUP
Commodities (COMM)
PROCEDURE
1 Enter COMM.
2 Click on Enter Criteria then Execute Query to see which class codes have already been set up.

Commodity
3 If you need a new commodity code, click on Create Record.
4 Key in a commodity code (for example, FAK for Freight All Kinds) and press Enter.
5 Key in a subcode (for example, 00) and press Enter.
6 Use your pick list function to select the appropriate freight class code that you created in CLAS. To select 
a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick 
list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code. 
Text Block Optional
The message text for your commodity code.
FIELD DESCRIPTIONS

ITEM PROFILE SETUP
Item Location Profile (ILOP)
7 Do one of the following:
8 Repeat steps 3 to 7 for each additional commodity code that you wish to enter.
9 When you finish entering your commodity codes, click on Exit to exit.
Item Location Profile (ILOP)
OVERVIEW
In this program, you set up a single item location profile called NA for passive shipping and receiving. Passive 
shipping and receiving means that locations for inbound receipts and outbound orders will be manually 
assigned by the operator.
If you wish to set up active shipping or receiving (that is, AccellosOne 3PL assigns the locations), refer to the 
Allocation and Wave Manager Guide. 
If you wish to attach message 
text to your commodity 
code:
If you do NOT wish to attach 
message text to your commodity 
code:
a) Type in your text. If you require 
more than one line of text, press 
Enter at the end of the line to 
generate a new line. You can 
enter as many lines as you need. 
b) When you finish entering your 
last line, press Enter. Then click 
on Master Block.
a) Click on Master Block to exit the 
Text Block.
PREREQUISITES: ISOL, WARE, LOCA
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

ITEM PROFILE SETUP
Item Location Profile (ILOP)
PROCEDURE
1 Make sure that the Assign Location flags in DIFP are set to No for the customer to whom your passive 
ILOP profile will be attached.
2 Enter ILOP.
3 Click on Enter Criteria then Execute Query to see which item location profiles have already been set up. 
4 If you need a new item location profile, click on Create Record. If Create Record is not available, click on 
Return to Main to activate it.
5 Key in NA as your item location profile code and press Enter.
6 Key in PASSIVE LOCATOR as your description and press Enter.
7 Use your pick list function to select NA or ALL as your isolator code. To select a code using a pick list, 
press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code 
and click on Select Code to select it. 
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
Description Mandatory
Your item location profile code description.
Isolator Code (ISOL) Mandatory
Use ALL or NA as your isolator code. This field is not used in passive shipping 
or receiving.
Overflow Warehouse 
Code (WARE)
Mandatory
Enter any valid warehouse code. This field is not used in passive shipping or 
receiving.
Overflow Location Code 
(LOCA)
Mandatory
Enter any valid location code. This field is not used in passive shipping or 
receiving.

ITEM PROFILE SETUP
Item Tare Profile (ITAP)
8 Use your pick list function to select any warehouse on your system.
9 Use your pick list function to select any location code on your system.

Item Location Profile for passive locator system
No further input is required. AccellosOne 3PL will display the Type Block.
10 Click on Master Block to exit the Type Block.
11 Click on Exit to exit.
Item Tare Profile (ITAP)
OVERVIEW
In this program, you set up your tare weight profiles. You use tare weight profiles for items of non-standard 
weight when the tare weight of an item varies in a non-linear way depending on the weight of product 
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: Standard Weight field in ITEM is set to the appropriate tare weight option

ITEM PROFILE SETUP
Item Tare Profile (ITAP)
received. For example, the tare weight of one item is 5 lbs. while the tare weight of two items is a value other 
than 10 lbs.
EXAMPLE
In ITEM, you select “Enter Rcpt Gross Wgt, Calc Rcpt Net Wgt from Tare” as your weight option in the 
Standard Weight field. Then you set up the following ITAP profile and attach it to ITEM.

ITEM PROFILE SETUP
Item Tare Profile (ITAP)
You receive an item and enter 150 as its gross weight. AccellosOne 3PL will look up the appropriate weight 
break in ITAP — break 2 — and calculate the net weight from the tare weight (150 - 15 = 135).
BREAK VALUE TARE
1 100 10
2 200 15
3 300 20
FIELD DESCRIPTIONS
Item Tare Profile Code Mandatory
Your item tare profile code.
Description Mandatory
Your item tare profile description.
Weight Measure Code The weight measure code (pounds, kilos, tons, etc.) for your tare profile. This 
code must match the weight code attached to the item in the Quantity Breakdown Block of ITEM.
Number of Breaks The number of breaks for your tare profile.
Value Mandatory
The weight for this break expressed in terms of the weight measure code that 
you entered in the Weight Measure Code field. Depending on the standard 
weight option that you select in ITEM, your weight breaks will be based on 
either the item’s net weight or gross weight. 
Tare Mandatory
The tare weight for this weight break. 

ITEM PROFILE SETUP
Item Tare Profile (ITAP)
PROCEDURE
1 Enter ITAP.
2 Click on Create Record.
3 Key in your tare profile code and press Enter.
4 Key in a description for your new tare profile code and press Enter.
5 In the Weight Measure Code field, use your pick list to select the appropriate weight measure for your 
tare profile.
6 In the Number of Breaks field, key in the number of breaks for this tare profile and press Enter.
7 In the Break Block, key in the weight for your first break and press Enter.
8 In the Tare field, key in your tare weight for this break and press Enter.
9 Repeat the above two steps for each additional break for this profile.

ITAP screen showing four weight breaks for tare profile code 1
10 When you finish setting up your item tare profile code, click on Master Block and then Exit to exit.

ITEM PROFILE SETUP
Item Tare Profile (ITAP)

MESSAGE SETUP
Messages (MESS) ........................................................................................... 264
Depositor Messages (DEME) ......................................................................... 265
Depositor Print Messages (DPME) ................................................................ 267
Hazardous Material Messages (HAZA).......................................................... 269
Inventory Messages (ADIM) ........................................................................... 272

MESSAGE SETUP
Messages (MESS)
Messages (MESS)
OVERVIEW
This program allows you to set up standard messages on your system such as “Must maintain at above zero 
degrees Celsius”, “Remind driver to chock wheels”, etc. The messages that you create in this program can be 
attached to a specific customer, item, carrier or consignee. You can print these messages on specific shipping 
and receiving documents (DPME) or you can have them appear as pop-up messages for the operator at any 
flow step that you specify (DEME).
PROCEDURE
1 Enter MESS.
PREREQUISITES: None
ATTACHED TO: DEME (Depositor Messages)
DPME (Depositor Print Messages)
ITEM (Item)
CARR (Carrier)
CONS (Consignees)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Message Code Mandatory
Your code for this message.
Description Mandatory
The message description.
Text Block Mandatory
The text of your message.

MESSAGE SETUP
Depositor Messages (DEME)
2 Click on Enter Criteria then Execute Query to view the message codes that have been already set up.

Messages
3 If you need to set up a new message code, click on Create Record.
4 Key in your message code and press Enter. Then key in a meaningful description and press Enter again.
5 Press Enter in the Text Block field to advance to the next field.
6 Key in the first line of your message and press Enter. If you want to create a multi-line message, you 
must press Enter at the end of each line in order to advance to the next line.
7 When you finish entering your message, press Enter to get a new line.
8 Click on Return to Main then Exit to exit.
Depositor Messages (DEME)
OVERVIEW
In this program, you attach the message that you created in MESS to the customer and flow to which it 
applies. When you set up a depositor message in DEME, the message appears in pop-up form to the 
operator at the flow that you specify.
PREREQUISITES: CUST, MESS, FLPR
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

MESSAGE SETUP
Depositor Messages (DEME)
For example, suppose you attach a specific message to inbound flow X and customer Y. Whenever you 
receive from customer Y and advance to flow X in CHRF (Time Stamp and Confirm Receipts), that message 
will appear in pop-up form.

Depositor message attached to COOR flow
PROCEDURE
1 Enter DEME.
FIELD DESCRIPTIONS
Customer Code
(defined in CUST)
Mandatory
The customer to whom the message is attached or .ALL for all customers.
Flow Code
(defined in FLPR)
Mandatory
The flow at which the message will appear.
Message Code
(defined in MESS)
Mandatory
The message.

MESSAGE SETUP
Depositor Print Messages (DPME)
2 Click on Enter Criteria then Execute Query to see which messages have been attached to which customers.

Depositor Messages
3 If you need to set up a new depositor message, click on Create Record.
4 Key in your customer code and press Enter or select it using the pick list. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select Code.
5 Key in your flow code and press Enter or select it using the pick list.
6 Key in your message code and press Enter or select it using the pick list.
7 Repeat the above steps for each additional depositor message that you wish to set up.
8 When you finish setting up your codes, click on Return to Main and then Exit to exit.
Depositor Print Messages (DPME)
OVERVIEW
In this program, you can attach the message that you created in MESS to a particular document such as the 
core bill of lading, pick document, receipt invoice and tally. You can also display the message in RFCH (RF 
Check/Unload) and RFPIC (RF Pick). DPME allows you to specify that a given message will print on a given 
document for either all customers or a specific customer. As well, you must specify one of the following as 
your message recipient:
PREREQUISITES: CUST, CARR, CONS, SHIP, MESS, DOCU (set up by HighJump)
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

MESSAGE SETUP
Depositor Print Messages (DPME)
▪ a specific carrier
▪ .ALL carriers
▪ a specific consignee
▪ a specific shipper
If you have not set up your carriers, consignees and shippers, you cannot create DPME messages. Return to 
this program after you have completed the setup procedures.
PROCEDURE
1 Enter DPME.
2 Click on Enter Criteria then Execute Query to see which documents and which messages have been 
attached to which customers.
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer to whom the message applies or .ALL for all customers.
Carrier (CARR) / Consignee (CONS) / Shipper 
(SHIP) Code
Mandatory
The carrier, consignee or shipper for whom the message is intended or .ALL 
for all carriers.
Document Code (DOCU) Mandatory
The document on which the message will be printed.
Message Code (MESS) Mandatory
The message code of the message.
Allow Display of Message 
in RF
Y = Yes
N = No
If you select N for No, the message will be suppressed in all RF programs that 
support messages.

MESSAGE SETUP
Hazardous Material Messages (HAZA)

Depositor Print Messages
3 If you need to set up a new customer/document/message, click on Create Record.
4 Key in your customer code and press Enter or use the pick list function to select it. To select a code using 
a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. 
Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
If you want the message to appear for all customers using this document, select .ALL.
5 Use your pick list function to select a particular carrier/consignee/ shipper. You can also select .ALL carriers, consignees or shippers for this field. 
6 Key in your document code and press Enter or use the pick list function to select a document code.
7 Key in your message code and press Enter or use the pick list function to select a message code.
8 In the Allow Display of Message in RF field, key in Y for Yes or N for No and press Enter.
9 If required, enter another document and message for this customer and carrier/consignee/shipper or 
click on Return to Main and then Exit to exit this program.
Hazardous Material Messages (HAZA)
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 

MESSAGE SETUP
Hazardous Material Messages (HAZA)
OVERVIEW
In this program, you set up your hazardous material messages. These messages can be attached to a 
particular item and will print on the standard bill of lading 1 and 2 and the pick document.
For more advanced hazardous material tracking, see “Hazardous Material Block” on page 301 in ITEM.
PROCEDURE
1 Enter HAZA.
2 Click on Enter Criteria then Execute Query to see which hazardous material messages have already 
been set up.
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Code Mandatory
Your hazardous code.
Description Mandatory
Your hazardous code description.
Text Block Mandatory
The message text for your hazardous code.

MESSAGE SETUP
Hazardous Material Messages (HAZA)

Hazardous Material Messages
3 If you need a new hazardous message, click on Create Record.
4 Key in a message code and press Enter.
5 Key in a description for your new code and press Enter.
6 Press Enter in the Text Block and begin typing in the text of your message. If you require more than one 
line of text, press Enter at the end of the line to generate a new line. You can enter as many lines as you 
need. When you finish entering your last line, press Enter. Then click on Master Block to exit the Text 
Block.
7 Repeat steps 3 to 6 for each additional hazardous message that you wish to enter.
8 When you finish entering your hazardous messages, click on Master Block and then Exit to exit.

MESSAGE SETUP
Inventory Messages (ADIM)
Inventory Messages (ADIM)
OVERVIEW
In this program, you can create messages that can be attached to a particular item. The messages that you 
create in ADIM can be displayed in the Line Block during order entry (ENOR) and receipt entry (ENRE). As 
well, you can view them when you look the item up in LOEN. These messages are for display purposes only; 
they do not print on any AccellosOne 3PL document or report.
The messages that you create in this program must be attached to a unique inventory entity; that is, an item 
defined down to the lowest inventory level.
Multiple messages attached to the same item are allowed.
PREREQUISITES: MESS, CUST, ITEM
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: You must have at least one confirmed item in your warehouse.
FIELD DESCRIPTIONS
Customer Code
(defined in CUST)
Mandatory
The customer to whom this item belongs.
Level 1
(defined in ITEM)
Mandatory
The item to which you wish to attach the message.
Level 2/3/4 The inventory level to which you wish to attach the message.
Message Code
(defined in MESS)
Mandatory
The item’s message

MESSAGE SETUP
Inventory Messages (ADIM)
PROCEDURE
1 Enter ADIM.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter.
4 If required, key in additional levels of inventory and press Enter.
5 When you have defined the item to which you wish to attach the message, click on Execute Query.
6 If your query retrieved more than one inventory entity, use your up and down arrow keys to select the 
inventory entity to which you wish to attach the message.
7 Click on Message Block.
8 Use your pick list to select the appropriate message that you wish to attach to the item.
9 In the Order Entry field, key in Y for Yes or N for No and press Enter.
10 In the Receipt Entry field, key in Y for Yes or N for No and press Enter.
11 In the Inventory Look-Up field, key in Y for Yes or N for No and press Enter.
Order Entry Y = Yes
N = No
If you set this field to Yes, the message will appear in ENOR. If you set this 
field to No, the message will not appear in ENOR.
Receipt Entry Y = Yes
N = No
If you set this field to Yes, the message will appear in ENRE. If you set this 
field to No, the message will not appear in ENRE.
Inventory Look-Up Y = Yes
N = No
If you set this field to Yes, the message will appear in LOEN. If you set this 
field to No, the message will not appear in LOEN.
FIELD DESCRIPTIONS

MESSAGE SETUP
Inventory Messages (ADIM)

Adjust Inventory Messages showing two messages
12 Repeat steps 7 to 10 for each additional message that you wish to attach.
13 When you finish entering all your messages for this item, click on Return to Main to exit create mode. 
Then click on Inventory and Exit to exit.

ITEM SETUP
Item (ITEM)....................................................................................................... 276

ITEM SETUP
Item (ITEM)
Item (ITEM)
OVERVIEW
In this program, you take the codes and profiles that you set up in the previous steps and attach them to your 
items. You also define the quantity breakdown of the item (x number of eaches per case, y number of cases 
per pallet, etc.), the base SKU type for tracking the item’s size and weight, and the linear measurements and 
weight of this base SKU type.
Mandatory fields in this program are:
▪ Customer Code
▪ Item Code
▪ General Information Profile Code
▪ Item Billing Profile Code
▪ Shipping Profile Code
▪ Process Profile Code
▪ Quantity Breakdown Profile Code
▪ Location Profile Code
▪ Commodity Code
▪ Entry Required up to Level
▪ Variable Quantity Breakdown
▪ Standard Weight
▪ Tax Code
There are also a number of fields in the Quantity Breakdown Block that are mandatory.
PREREQUISITES: IINP, IBIP, ITSH, IPRP, IQBP, ILOP, COMM, SKUS, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The quantity breakdown of the item, the layer configuration (tie and hi), 
the linear measurements (height, width and length) and the weight
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer to whom this item belongs.

ITEM SETUP
Item (ITEM)
Item Code Mandatory
Your item code. An item code can consist of any combination of numbers or 
letters up to 20 characters in length. Please note the following restrictions on 
special characters:
▪ The single quote (’) and double quote (") special characters are not valid 
and should never be used. 
▪ Special characters such as “&”, “%” and “_” may cause problems in certain 
programs and are not recommended. 
▪ The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used.
▪ Other special characters are generally supported.
Description Mandatory
Your item code description. An item code description can consist of any combination of numbers or letters up to 20 characters in length. The special character restrictions for item codes apply equally to item descriptions.
Master Item N = No
Y = Yes
If you select Yes, the item is a master item and can have other non-master 
items attached to it. Master items are a way of grouping similar items.
Attached to (ITEM) Optional
The item’s master item.
General Information Profile Code (IINP)
Mandatory
This profile specifies the unit of measure that you wish to use for management 
reporting purposes.
Alternate Description Optional
If required, you can record a secondary description for the item in this field. 
This option can be used for bilingual product descriptions or technical data 
regarding the item.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Extended Description Optional
This field is an overflow field for the Description field when the description 
exceeds 40 characters.
Hazardous Material N = No
Y = Yes
If you select Yes, you can open the Hazardous Material Block and enter hazardous material information for the item.
Item Billing Profile Code 1 
(IBIP)
Mandatory
This profile controls the initial storage, renewal storage and handling charges 
for this item. If you wish to change this profile after receiving inventory, the 
change will apply to new inventory only unless you run ADBD (Adjust Billing 
Data). See the Billing and Invoicing Guide for further information.
Item Billing Profile Code 
2/3
Optional
Reserved for special or seasonal billing. See the Billing and Invoicing Guide
for further information.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Shipping Profile Code 
(ITSH)
Mandatory
This profile allows you to allocate product to an order based on an expiry date 
or date code. If you do not require this function for this item, use your NA (Not 
Applicable) profile. If you wish to change this profile after receiving inventory, 
the change will apply to new inventory only unless you run CHEI (Change 
Entity Information). See the Operations 1 Guide for further information.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Process Profile Code 
(IPRP)
Mandatory
This profile allows you to attach predefined messages and operator-entered 
values to an item. If you do not require this feature, use your NA (Not Applicable) profile.
Quantity Breakdown Profile Code (IQBP)
Mandatory
The quantity breakdown for this item (for example, PALLETS/CASES or PALLETS/ CASES/EACHES).
CAUTION Once you receive inventory in a particular item, you cannot 
change the item’s quantity breakdown profile in ITEM. Should you need to 
change the profile, you must do so in AEQB (Adjust Entity Quantity Breakdown).
Location Profile Code 
(ILOP)
Mandatory
This profile specifies the parameters that you wish AccellosOne 3PL to use for 
active shipping and receiving. If you do manual put-away and picking for this 
item, use your NA (Not Applicable) profile.
Warehouse Code 
(WARE)
Optional
If the item is restricted to one warehouse, enter the warehouse code in this 
field. If the item can be received in any warehouse, leave this field blank.
Hold Profile Code (IHOP) Optional
If you enter a hold profile code in this field, the item will be placed on automatic hold when it is received or shipped.
Commodity Code 
(COMM)
Mandatory
The item’s commodity code.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Entry Required up to 
Level
Mandatory
The number of inventory levels needed for this item. You can specify any number between the inventory level that you bill at (defined in DILP) and the maximum number of levels for the customer (defined in DILP) attached to this item.
For example, if you set up a customer with three inventory levels (ITEM, LOT 
and PALLET ID) and bill this customer at level 2, you can set this field to either 
2 (no pallet ID required for a particular item) or 3 (all inventory levels required 
for this item).
Number of Days for Open 
Lots
Optional
If you wish to process the item as an open lot, enter the number of days that 
the item can remain open. Open lots are lots that remain open for one or more 
days and allow you to receive the same entity in multiple receipts.
See “Open Lot Receipts” in the Billing and Invoicing Guide for further information on this field.
Variable Quantity BreakdownN = No
Y = Yes
This field allows you to specify whether you wish to allow non-standard quantity breakdowns for the item. If you set this flag to No, the quantity breakdown 
that you define in the Quantity Breakdown Block of this program is standard 
and cannot be changed for any particular receipt. If you set this flag to Yes, 
you can change the item’s quantity breakdown on a receipt.
EXAMPLE
Your standard quantity breakdown for a particular product is 25 pieces per 
case. 
If you set this field to No, each time you receive this product in ENRE, AccellosOne 3PL will automatically calculate the total number of pieces using the 
standard quantity breakdown. For example, if you receive 10 cases, you are 
receiving 250 pieces.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
If you set this field to Yes, each time you receive this product in ENRE, AccellosOne 3PL will prompt you to override the number of pieces per case. For 
example, you could enter 30 pieces per case (rather than 25) and AccellosOne 3PL would record 300 pieces received (not 250).
NOTE You can only change the quantity breakdown on a receipt if you are 
receiving the inventory entity for the first time. If the inventory entity has 
already been received by the warehouse, you cannot change its quantity 
breakdown. 
Renewal Options for Variable Quantity BreakdownH = High
L = Low
M = Most
S = Standard
In this field, you specify how you want AccellosOne 3PL to calculate renewal 
storage on variable quantity breakdown items in which the same billing entity 
has multiple quantity breakdowns. For example, you bill on level 2 or lot and 
you have four pallets in your warehouse with different quantity breakdowns 
but the same lot number: 
pallet 1 = 60 cases
pallet 2 = 75 cases
pallet 3 = 100 cases
pallet 4 = 75 cases.
If you select High, AccellosOne 3PL will use the highest quantity breakdown 
when doing a pallet count (100 cases). If you select Low, AccellosOne 3PL will 
use the lowest quantity breakdown when doing a pallet count (60 cases). If 
you select Most, AccellosOne 3PL will use the most common quantity breakdown when doing a pallet count (75 cases). 
If you select Standard, AccellosOne 3PL will use the standard quantity breakdown defined in ITEM.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Standard Weight Y = Standard Weight
F10 = Other Options
If you set this field to Standard Weight, AccellosOne 3PL will use the standard 
weight specified in the Quantity Breakdown Block of this program; you will not 
be able to modify this weight during receipt entry or order entry. If you wish to 
enter the weight manually on shipping or receiving or calculate the weight in a 
different manner, see “Non-Standard Weight Options” on page 305 for further 
information.
If you wish to change your weight option after receiving inventory, the change 
will apply to new inventory only unless you run WEAD (Weight Adjustments) 
or RESW (Recalculate Standard Weight). See “Adjusting Weight Details” in 
the Operations 1 Guide for further information.
Tare Profile Code (ITAP) Optional
Only required if you use tare weight profiles.
Cross Dock Y = Yes
N = No (default)
See “Cross-Dock Billing” in the Billing and Invoicing Guide for further information on this field.
Item Value Optional
For use in export documents. The value that you enter in this field will appear 
in export documents as the declared value. Also used in cycle counting if you 
track variances by the item’s value.
Value for SKU Code 
(SKUS)
Optional
The SKU code that the value applies to.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Hazard Code (HAZA) Optional
If required, the hazard code for this item. The hazard code will print on the 
standard bill of lading 1 and 2 and the pick document.
If you use AccellosOne Transport and attach a hazard code to an item, that 
item cannot be placed on the same load as an item with no hazard code 
attached to it.
Cycle Count Profile Code 
(CYCP)
Optional
See the Cycle Counting Guide for further information.
Picking Profile Code 
(PIPR)
Optional
If you attach a PIPR profile to this item, the item will be allocated according to 
the options that you defined in your PIPR profile. If you do not attach a PIPR 
profile to this item, the item will be allocated according to the default PIPR profile that you attached to DSRP (Depositor Shipping & Receiving).
Allow Overpick, Ignore 
Consignee
Only available if the Picking Profile Code (PIPR) field is populated with any 
PIPR profile (if this profile has overpick rules, the rules are ignored)
N = No
Y = Yes
If you set this flag to N for No, overpicking in RFPIC is deactivated for this 
item. If you set this flag to Y for Yes, the picker can overpick an order line in 
RFPIC up to the next full pallet quantity. 
For example, suppose the quantity breakdown of a given item is meters and 
pallets with a full pallet being defined as 800 meters. If the order quantity is 
500 meters, the picker is allowed to pick 800 meters, overpicking the order 
line by 300 meters. 
NOTE Overpicking at the item level with no consignee override is intended 
for facilities that ship to a single consignee. Hence, the need to ignore the consignee’s overpick rules, if any. Allowing the consignee override to take effect 
through a PIPR profile would force the same overpick rules on all of customer’s items.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Item Discount Flag A = Always
N = No
C = Choose
See the section “Discounts on Initial Storage and Handling” in the Billing and 
Invoicing Guide.
Discount Profile Code 
(DPRO)
See the section “Discounts on Initial Storage and Handling” in the Billing and 
Invoicing Guide.
Tax Code Mandatory
The tax that you wish to apply to the item. The item’s tax code can be either 
the same as the customer’s tax code defined in DBIP (Depositor Billing Profile) or can be set to None. For example, if the customer’s tax code is GST 
Only, the item’s tax code can only be GST Only or None for no tax; you cannot 
enter a tax code of PST Only for any item belonging to this customer.
If you enter a tax code in this field that differs from the tax code in DBIP 
(Depositor Billing Profile), the tax code at the item level will override the tax 
code at the customer level.
Message Code (MESS) Optional
If required, the message that you wish to attach to this item. These messages 
can be printed on any inbound or outbound document (requires special programming by HighJump).
Weight Tolerance Profile 
Code (IWTP)
Reserved for future use
Scan Parameter Code 
(SCPR)
Optional
If required, the scan parameter code used if you are scanning in your weights 
or some other process code value from bar coded labels (RF only). 
Location Size Code 
(LOCS)
Optional
The item’s location size. This field is only used if you are putting away product 
based on location size.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Put-Away Profile Code 
(PUPR)
Optional
If you attach a PUPR profile to this item, the item will be put-away according to 
the options that you defined in your PUPR profile. If you do not attach a PUPR 
profile to this item, the item will be allocated according to the default PUPR 
profile (if any) that you attached to DSRP (Depositor Shipping & Receiving).
Pallet Build Restriction 
Code (IPBR)
See Outbound Pallet Building section in the RF Guide.
Cartonization Profile 
Code (ICNP)
See RF Guide.
Country Code (CNTY) Optional
The country in which the item was manufactured. An entry in this field is only 
required if the item’s country differs from the customer’s country specified in 
CUST.
Kit N = No (default)
Y = Yes
See the kitting section in the Operations 2 Guide for further information.
Order Line Types for Kit 
Components
N = No (default)
Y = Yes
See the kitting section in the Operations 2 Guide for further information.
Processing Area Code 
(PROA)
Reserved for future use
UPC Optional
The item’s UPC code.
Allow Mixed Pallets in RF Custom use only
Allow Banding Reserved for future use
Banding SKU Class Reserved for future use
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Maximum Banding QuantityReserved for future use
Item Value Profile Code Reserved for future use
Item RF Profile Code 
(MIRP)
See the RF Guide for further information.
Inventory Attribute Profile Code (IAPR)
Optional
See the Inventory Attributes section in the Operations 2 Guide for further information.
Scan Parameter Code for 
Inventory Validation 
(SCPR)
If you enter a scan parameter code in this field, it will override the customer 
level default that you established in the Validate Inventory Level from Bar 
Code Using SCPR Code field in MRFP.
Scan Parameter Code for 
Voice (SCPR)
This field allows you to define two SCPR codes for the same item: one for RF 
scanning and a second one for voice. 
If this field is populated, voice will use this SCPR code rather than the SCPR 
code in the Scan Parameter Code (SCPR) field. If this field is not populated, 
voice will use the scan parameter profile in the Scan Parameter Code (SCPR) 
field.
Oversize Flag Only used in A1 Ship integration.
Stackability Indicator 
Code
See the Outbound Pallet Building section in the RF Guide. 
Stackablility Quantity in 
Highest SKU
For outbound stacking, see the Outbound Pallet Building section in the RF 
Guide. For inbound stacking, see the Product Stacking Group (ILOP) in the 
Allocation and Wave Manager Guide.
Pallet Type Height/
Spacer Height
The item’s standard pallet type height and spacer height. The unit of measure 
for these two fields is the linear measure code selected in the Quantity Breakdown Block for the base SKU. The put-away/directed move engine will consider the height of pallet types and spacers in the calculations for inbound 
moves, but ignore the height of spacers for inventory moves.
Allocate Pallet by Entity If you set this flag set to Y, when allocation is looking for pallets, all stock for 
one inventory entity (i.e. one unique inventory level 1, 2, 3, 4) in a location will 
be treated as a pallet even if the quantity is less than a full pallet or greater 
than a full pallet. When allocation is not looking for pallets, such stock will be 
treated as if the flag were set to N.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
PROCEDURE
1 Enter ITEM.
2 Click on Enter Criteria then Execute Query to see whether the item has already been set up. If the item 
has not been set up, click on Create Record.
3 Key in your customer code and press Enter.
4 Key in your item code and press Enter. An item code can consist of any combination of numbers or letters up to 20 characters in length.
5 Key in a description for your item code and press Enter.
6 Press Enter twice to bypass the Master Item and Attached to (ITEM) fields.
7 Use your pick list to select the appropriate general information profile code. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select Code. 
Velocity Code (IVLP) The item’s velocity code.
Directed Put-Away Zone 
Code (WHZO)
See Allocation and Wave Manager.
Merge Inventory to Location on Replenishment 
and RFRL
If you select this option, the lowest inventory level of an inventory entity being 
relocated or replenished to the pick line will be changed to the to location 
code. For example, if item 1, lot 101, pallet ID 123 is relocated to location 
ABC, it will become item 1, lot 101, pallet ID ABC.
Allow Supvr. Override of 
Min./Max. Expiry/Production Date
An override at the item level of the field of the same name in ITSH.
Minimum Range in Days 
to Expiry
An override at the item level of the field of the same name in ITSH.
Maximum Range in Days 
to Expiry
An override at the item level of the field of the same name in ITSH.
Maximum Range in Days 
from Production Date
An override at the item level of the field of the same name in ITSH.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Status A = Active
D = Deactivated
If an item is active, you can ship and receive it like any other item. If an item is 
deactivated, you can ship the item but you cannot receive new inventory for 
the item.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
8 Use your pick list to select the appropriate item billing profile code.
9 Press Enter to bypass the Billing Profile Code 2 and 3 fields.
10 Press Enter to bypass the Extra Charge Profile Code field.
11 Use your pick list to select the following profile codes:
▪ the shipping profile code
▪ the process profile code
▪ the quantity breakdown profile code
▪ the location profile code

Item
12 If you wish to restrict the item to a particular warehouse, enter this warehouse in the Warehouse Code 
field. If the item can be received in any warehouse or you only have a single warehouse on your system, 
press Enter to bypass this field.
13 If required, use your pick list to select the appropriate hold profile code. If you do not need a hold profile 
code, press Enter to bypass this field.
14 If required, key in an alternate description for your item and press Enter. If you do not need an alternate 
description, press Enter to bypass this field.
15 Use your pick list to select the appropriate commodity code.
16 Press Enter to accept the commodity subcode.
17 In the Entry Required up to Level field, key in the number of inventory levels required for this item and 
press Enter.
18 Press Enter to accept 0 as the number of days that you want the lot to remain open in the Number of 
Days for Open Lots field and press Enter.

ITEM SETUP
Item (ITEM)
19 Key in the appropriate value in the Variable Quantity Breakdown field (Y for Yes or N for No) and press 
Enter. If you select No, AccellosOne 3PL will use the standard quantity breakdown in ENRE. If you select 
Yes, AccellosOne 3PL will prompt you for the quantity breakdown in ENRE.
20 If you entered Y in the previous field, key in the appropriate value (H for High, L for Low, M for Most or S
for Standard) in the Renewal Option for Variable Quantity Breakdown field and press Enter.
21 In the Standard Weight field, key in Y for Yes and press Enter to use the standard weight as defined in 
Quantity Breakdown Block. If you do not want to use a standard weight, press F10 to access a pick list of 
other weight options.

Item screen showing prompt for tare profile code
22 If required, use your pick list to select the appropriate tare profile code. 
23 Key in the appropriate value in the Cross Dock field and press Enter. If you select No, you will not be able 
to cross dock the item. If you select Yes, AccellosOne 3PL will permit cross docking of the item.
24 If required, key in a declared value for the item and press Enter or press Enter with the field blank to 
bypass this option.
25 If you entered a declared value for the item, key in the SKU code that the value applies to and press 
Enter.
26 Use your pick list to select the appropriate hazard code or press Enter to bypass this field.
27 Press Enter to bypass the Cycle Count Profile Code field.
28 Use your pick list to select the appropriate picking profile code or press Enter to bypass this field.
29 In the Item Discount Flag field, key in N for Never and press Enter.

ITEM SETUP
Item (ITEM)

Item screen showing prompt for tax code
30 Use your pick list to select the appropriate tax code.
31 Use your pick list to select the message code or press Enter to bypass this field.
32 Press Enter to bypass the Weight Tolerance Profile Code field.

ITEM SETUP
Item (ITEM)

Item screen showing prompt for scan parameter code
33 If required, use your pick list to select the following optional codes:
▪ scan parameter code
▪ location size code
▪ put-away profile code
▪ country code
34 In the Kit field, key in the N for and press Enter.
35 Press Enter to bypass the Processing Area Code field.
36 If required, key in the item’s UPC code and press Enter.
37 Press Enter the required number of times to bypass the remaining fields in ITEM.
The Quantity Breakdown Block will be displayed. Refer to the section that follows for complete instructions.
QUANTITY BREAKDOWN BLOCK
In this block, you set up: 
▪ the quantity breakdown of the item (that is, the number of units of SKU type X that make up a full SKU 
type Y)
▪ the layer configuration or tie and hi (optional)
▪ the linear measurements 
▪ the weight 
If you selected a profile in the Quantity Breakdown Profile Code field consisting of a single SKU type (for 
example, CASES only), AccellosOne 3PL will create a single record in the Quantity Breakdown Block. 

ITEM SETUP
Item (ITEM)
If you selected a profile in the Quantity Breakdown Profile Code field consisting of multiple SKU types (for 
example, CASES/EACHES or PALLETS/CASES/ EACHES), AccellosOne 3PL will create one record in the 
Quantity Breakdown Block for each SKU type — that is, one for CASES and one for EACHES or one for 
PALLETS, one for CASES and one for EACHES.
When you select a quantity breakdown profile consisting of two or more SKU types, you must specify two 
things: the number of units of SKU type X that make up a full SKU type of Y and the SKU type that you wish 
to use to track the item’s weight and size.
CAUTION If you wish to change an item’s quantity breakdown after receiving 
inventory for that item, refer to “Adjusting an Item’s Quantity Breakdown in AEQB” in 
the System Administration Guide for further instructions.
FIELD DESCRIPTIONS
SKU Code (SKUS) This value is set by AccellosOne 3PL according to quantity breakdown profile 
that you defined in IQBP and attached to this item in the Quantity Breakdown 
Profile Code field in this program.
When you first enter the Quantity Breakdown Block, the SKU type of your 
highest quantity breakdown level is shown.
Quantity Mandatory
If you have a single level quantity breakdown (for example, CASES only), set 
this field to 1. If your quantity breakdown is CASES/EACHES, you would have 
two quantities. For your EACHES quantity breakdown, you would enter 1; for 
your CASES quantity breakdown, you would enter the number of eaches per 
case (for example, 20 if 20 eaches per case are standard for this item).
If your quantity breakdown were PALLETS/ CASES/EACHES, your quantities 
would be as follows (example only):
EACHES level = 1 (because lowest level)
CASES level = 10 (10 eaches per standard case)
PALLET level = 60 (60 cases per standard pallet)
NOTE If you are entering the number of layers and the quantity per layer 
for this quantity breakdown level, the product of the two values (number of layers times quantity per layer) must equal the value that you enter in the Quantity field.

ITEM SETUP
Item (ITEM)
Minimum Quantity Optional
If you enter a minimum quantity in this field, AccellosOne 3PL will not allocate 
product to an order if the on-hand quantity is less than the minimum quantity. 
You can override minimum quantities for high priority orders by setting the 
Evaluate Minimum flag in ORPR (Order Priorities) to the appropriate value.
A minimum quantity can include more than one SKU in an item’s quantity 
breakdown. For example, for a pallet/case item you can set up a minimum 
quantity of one pallet for your pallet SKU and 10 cases for your case SKU. 
AccellosOne 3PL will use the total minimum quantity of all SKU’s — that is, 1 
pallet, 10 cases — as the item’s minimum quantity.
Base for Cube/Weight Y = Yes
N = No
If you enter Yes, AccellosOne 3PL will track the item’s weight and cube at this 
quantity breakdown level. If you enter No, you must specify Yes for another 
quantity breakdown level.
For example, if the item has a single quantity breakdown level such as 
CASES, you must set this flag to Yes for CASES. If the item’s quantity breakdown is PALLETS/CASES, you must set this flag to Yes for either PALLETS or 
CASES.
If you are setting up a variable quantity breakdown item, you should set this 
flag to Yes for the lowest SKU.
Whole/Prorate W = Whole (default)
P = Prorate
If you set to Whole, AccellosOne 3PL will round up partial quantities (for 
example, 1.5 pallets would be billed as two pallets if you were charging by pallet). If you set to Prorate, AccellosOne 3PL will charge for actual quantities 
stored and will not round up.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Number of Layers Mandatory if you set the Layer Configuration Required Flag to Yes in IQBP
If you set the Layer Configuration Required flag in IQBP to Yes for this quantity breakdown level, you must enter the number of layers or hi for this quantity 
breakdown level as well as the quantity per layer or tie.
If you set the Layer Configuration Required flag in IQBP to No for this quantity 
breakdown level, you can press Enter to bypass the layer configuration fields.
NOTE The number of layers times the quantity per layer must always 
equal the number in the Quantity field.
If you are at your lowest quantity breakdown level or if you do not require layer 
configuration, set the number of layers and quantity per layer to 1.
Quantity Per Layer Optional
The number of entities or tie per layer.
Quantity Odd Layer Optional
If the number of layers times the quantity per layer does not equal the number 
in the Quantity field, you must enter the difference in this field so that the 
quantities balance.
Override Configuration on 
Receipt
Reserved for future use
Volume Measure Code Optional
You can track an item’s volume by entering a volume measure code in this 
field. 
Volume The item’s volume.
Carton Size Cube Only required if you perform cartonization
The number of units of this item that can fit into a carton.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Linear Measurement 
Code
Mandatory
Feet, inches, meters, etc.
Height Optional
The height of your base quantity breakdown level
Width Optional
The width of your base quantity breakdown level
Length Optional
The length of your base quantity breakdown level
Total Cube Mandatory
If you enter the item’s height, width and length, AccellosOne 3PL will automatically calculate the item’s cube. If you do not enter a height, width and length, 
enter 1 to bypass the Total Cube field.
Weight Measure Code Mandatory
Pounds, kilograms, tons, etc.
Gross Weight Mandatory
The item’s standard gross weight. If the item has no standard gross weight, 
enter 1.
Net Weight Mandatory
The item’s standard net weight. If the item has no standard net weight, enter 
1.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
PROCEDURE
When you first enter the Quantity Breakdown Block, the SKU type of your highest quantity breakdown level is 
shown. In the sample screen shown below, the highest quantity breakdown level is PALLET.

Quantity Breakdown Block showing PALLET as the first quantity breakdown level
1 In the Quantity field, key in the appropriate number and press Enter.
2 If required, key in a minimum quantity for this quantity breakdown level and press Enter.
Tare Weight Optional
The item’s tare weight. This weight is only required for non-standard weight 
options under which the gross or net receipt weight is calculated using the tare 
weight.
Weight Tolerance % See the RF Guide for further information on catch weight tolerances.
If the quantity breakdown is 
single level (for example, 
CASES only):
If the quantity breakdown is 
double-level (for example, 
CASES/EACHES):
If the quantity breakdown is 
triple level (for example, 
PALLETS/CASES/EACHES):
a) You enter 1. a) You enter the number of 
eaches per case.
a) You enter the number of cases 
per pallet.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
3 In the Base for Cube/Weight field, key in Y for Yes or N for No to specify whether you want AccellosOne 
3PL to track the item’s size and weight at this quantity breakdown level. If you are entering a single-level 
quantity breakdown (for example, UNITS), you must enter a Y in this field.
4 In the Whole/Prorate field, key in W for Whole or P for Prorate and press Enter. 
5 If required, key in the number of layers or hi of this quantity breakdown level and press Enter.
6 If required, key in the quantity per layer or tie of this quantity breakdown level and press Enter.
7 If the number of layers times the quantity per layer does not equal the value in the Quantity field, key in 
the difference in the Quantity Odd Layer field and press Enter.
8 Press Enter to bypass the Override Configuration at Receipt field.
9 If you select No in the Base for Cube/Weight field, AccellosOne 3PL will display the next quantity breakdown level. Repeat the previous steps for the next quantity breakdown level.
If you select Yes in the Base for Cube/Weight field, you must enter the linear and weight measurements 
for this quantity breakdown level.
10 If required, use your pick list to select the appropriate volume measurement code. Then key in your volume for this quantity breakdown and press Enter.
Quantity Breakdown Block showing PALLET as the base for cube and weight
11 Use your pick list to select the appropriate linear measurement (feet, inches, meters, etc.).
12 Key in the height of the SKU type and press Enter.
13 Key in the width of the SKU type and press Enter.
14 Key in the length of the SKU type and press Enter. AccellosOne 3PL will calculate the cube automatically.
15 Use your pick list to select the appropriate weight measure code (pounds, kilograms, tons, etc.).

ITEM SETUP
Item (ITEM)
16 If there is a standard weight for the item, key in the gross weight of the SKU type and press Enter. If there 
is no standard weight, you can use 1.
17 If there is a standard weight for the item, key in the net weight of the SKU type and press Enter. If there is 
no standard weight, you can use 1.
18 If required, key in the tare weight of the SKU type and press Enter.

Quantity Breakdown Block showing PALLET as the base for cube and weight
19 Press Enter to bypass the Weight Tolerance % field.
20 If you are entering a single-level quantity breakdown item, your item is complete. Click on Master Block 
and Exit to exit.
If you are entering a multi-level quantity breakdown item, AccellosOne 3PL will display the next highest 
quantity breakdown level. Refer to the table below for further instructions:
If the next highest quantity breakdown level is 
your last (for example, your breakdown is 
CASES/EACHES and you are at the EACHES 
level).
Quantity field = 1.
Number Layers and Quantity Per Layer = 1
If you are recording your weight and size at the 
CASE quantity breakdown, the weight and size 
fields will be bypassed for EACHES.
If the next highest quantity breakdown level is 
not your last (for example, your breakdown is 
PALLETS/CASES/EACHES and you are at the 
CASE level).
Quantity field = number of eaches per case.
Number Layers = number of layers of eaches in 
a case
Quantity Per Layer = number of eaches in a 
layer

ITEM SETUP
Item (ITEM)

Quantity Breakdown Block showing CASE breakdown level
21 Once you have entered all your quantity breakdown levels, click on Master Block and then Exit to exit the 
program.
CHANGING AN ITEM’S QUANTITY BREAKDOWN
If you wish to change an item’s quantity breakdown (for example, from 50 cases to a pallet to 60) and you 
want the change to apply to existing inventory, you must run AEQB (Adjust Entity Quantity Breakdown).
CHANGING AN ITEM’S WEIGHT
If you wish to change an item’s weight (for example, from 100 KGS to 90 KGS) and you want the change to 
apply to existing inventory, you must run RESW (Recalculate Standard Weight).
DELETING AN ITEM
You can delete an item if you have not received any inventory for the item in ENRE or created new inventory 
in ENAJ. If there are history records for the item, you can deactivate the item but not delete it.
1 Enter ITEM.
2 Retrieve the item that you wish to delete.
3 Press Enter until the Delete button appears.
4 Click on Delete.
5 Click on Exit.

ITEM SETUP
Item (ITEM)
ADDING ADDITIONAL ITEMS
You may use the first item that you set up for this customer as your template for all the other items of this 
customer.
1 Enter ITEM.
2 Locate the item that you previously set up.
3 Click in the Item Code field.
4 Key in your new item code over the existing item code and press Enter.
5 Key in your new description over the old description and press Enter.
6 Change any information that does not apply to the new item. Some of the profiles or fields that you may 
have to change are:
▪ Item Quantity Breakdown Profile
▪ Variable Quantity Breakdown
▪ Standard Weight
7 One you are satisfied that you have changed all the required fields and profiles and that the new item is 
correct, press F12 (Commit).
8 Click on Return to Main to display the new item that you have just committed.
9 Click on Quantity Breakdown to enter the Quantity Breakdown Block of the new item.
You will see the quantities, layer configuration, linear measurements and weight of the original item.
10 Change these quantities, layer configuration, linear measurements and weights for each SKU type as 
required.
11 Repeat the above steps for each additional item that you wish to add.
12 When you finish entering all your items, click on Master Block and Exit to exit.
ALTERNATE REPORTING BLOCK
In this block, you attach the alternate reporting type codes that you defined in ITAS to the item. When you 
attach an alternate reporting type code to an item (for example, MEAT), you can run the report program INAS 
(Inventory Report by Alternate Location). This report will generate a consolidated inventory report showing all 
meat items regardless of customer to which you have attached the MEAT alternate reporting type code.
You can also use alternate reporting type codes to rename an item and to group items for billing purposes 
(that is, bill for an entire product line rather than item by item).
1 Enter ITEM.
2 Retrieve the item to which you wish to add the alternate reporting code.
3 Click on Quantity Breakdown Block, Substitute Block and Alternate Reporting Block.
4 Click on Create Record.
5 Use your pick list to select your alternate reporting type code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow 
keys to position your cursor over the appropriate code and click on Select Code. 
6 Use your pick list to select your alternate reporting code. If you are attaching a single-level reporting type 
code, you will select the same code that you selected in step 5. If you are attaching a double-level code, 
you will select the second level of the code that you selected in step 5.

ITEM SETUP
Item (ITEM)

Alternate Reporting Block showing a double-level code — MEAT/PORK
7 If you have another reporting type code to add, repeat steps 5 and 6. 
8 When you finish entering your alternate reporting codes, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit ITEM.
HAZARDOUS MATERIAL BLOCK
In the Hazardous Material Block, you define the hazardous material properties of your items. You access the 
Hazardous Material Block by positioning your cursor in the Hazardous Material field, keying in Y for Yes and 
clicking on Hazardous Material.
AccellosOne 3PL supports the ADR, IATA, DOT and IMO classification systems for hazardous product.

ITEM SETUP
Item (ITEM)
Hazardous Material Block showing various hazmat properties
TRANSPORT MODE BLOCK
In the Transport Mode Block, you can attach a transport mode code — air, sea, ground or all modes — as well 
as transport mode hazardous properties such as inner packing code type and quantity to an item. The same 
item can have different transport mode hazardous properties depending on its transport mode code. For 
example, line 1 is “Sea”, Line 2 is “Air” and Line 3 is “Ground”.
You must save a record in the Hazardous Material Block before you can access the Transport Mode Block by 
clicking on Details.
FIELD DESCRIPTIONS
Line Number Mandatory
Your line number. You need one line number for each transport mode code.

ITEM SETUP
Item (ITEM)
Transport Mode Block showing item A1 as hazardous when shipped by air transportation
Transport Mode Code 
(TRMO)
Mandatory
All Modes
Ground
Air
Sea
Your transport mode code.
FIELD DESCRIPTIONS

ITEM SETUP
Item (ITEM)
Hazardous Material Transport block
LANGUAGE BLOCK
In the Language Block, you can define the ADR proper shipping name, hazard text 1, hazard text 2 and 
hazard text 3 in different languages. You must save a record in the Transport Mode Block before you can 
access the Language Block.
Language Block showing ENUS proper shipping name and hazard text 1/2/3

ITEM SETUP
Item (ITEM)
NON-STANDARD WEIGHT OPTIONS
AccellosOne 3PL supports a number of different weight options. When receiving product, you can manually 
enter the unit weight, gross weight or net weight or you can use the item’s tare weight to calculate either the 
gross weight or the net weight. When shipping product, you can manually enter the product’s gross weight, 
net weight or both.
You can also combine various inbound and outbound options. For example, you can enter the gross weight 
and calculate the net weight from the tare weight when receiving and enter the order’s gross weight when 
shipping.
ENRE Line Block showing all weight fields automatically populated for standard weight item (for nonstandard weight item some or all of these fields are blank and manually enterable)

ITEM SETUP
Item (ITEM)
WEIGHT CODES
A Enter Rcpt Unit Wgt
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will multiply the receipt unit weight by the number of units to arrive at the total gross 
weight of a receipt line.
This option is not suitable if you wish to track or bill product by net weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.
AT Enter Rcpt Unit Wgt, Calc Rcpt Net Wgt from Tare
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will multiply the receipt unit weight by the number of units to arrive at the total gross 
weight of a receipt line. The total net weight of the line will be calculated by subtracting the 
total tare weight from the total gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
B Enter Rcpt Gross Wgt 
With this option, you enter the weight of each receipt line in ENRE. AccellosOne 3PL will 
calculate the receipt unit weight by dividing the receipt’s gross weight by the number of 
units received.
This option is not suitable if you wish to track or bill product by net weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.

ITEM SETUP
Item (ITEM)
BT Enter Rcpt Gross Wgt, Calc Rcpt Net Wgt from Tare
With this option, you enter the gross weight of each receipt line in ENRE. AccellosOne 
3PL will calculate the total net weight of the line by subtracting the total tare weight from 
the total gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
C Enter Rcpt Net Wgt
With this option, you enter the net weight of each receipt line in ENRE. This option is not 
suitable if you wish to track or bill product by gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.
CT Enter Rcpt Net Wgt, Calc Rcpt Gross Wgt from Tare
With this option, you enter the net weight of each receipt line in ENRE. AccellosOne 3PL 
will calculate the total gross weight of the line by adding the tare weight to the total net 
weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
D Enter Rcpt Unit Wgt, Rcpt Net Wgt
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will calculate the total gross weight of the receipt line. You then enter the total net 
weight of the line; this weight must be less than or equal to the total gross weight of the 
line.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = N/A
WEIGHT CODES

ITEM SETUP
Item (ITEM)
E Enter Rcpt Gross Wgt, Rcpt Net Wgt
With this option, you enter the gross weight and net weight of each receipt line in ENRE. 
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = N/A
F Enter Ord Gross Wgt
With this option, you enter the gross weight of each order line in ENRE. AccellosOne 3PL 
will calculate the order unit weight by dividing the order’s gross weight by the number of 
units shipped.
G Enter Ord Net Wgt
With this option, you enter the net weight of each order line in ENOR. 
H Enter Ord Gross Wgt, Ord Net Wgt
With this option, you enter the gross weight and net weight of each order line in ENOR. 
AccellosOne 3PL will calculate the order unit weight by dividing the order’s gross weight 
by the number of units shipped.
I Enter Rcpt Unit Wgt, Ord Gross Wgt
See options A and F.
IT Enter Rcpt Unit Wgt, Ord Gross Wgt, Calc Rcpt Net Wgt from Tare
See options AT and F.
J Enter Rcpt Unit Wgt, Ord Net Wgt
See options A and G.
JT Enter Rcpt Unit Wgt, Ord Net Wgt, Calc Rcpt Net Wgt from Tare 
See options AT and G.
K Enter Rcpt Unit Wgt, Ord Gross Wgt, Ord Net Wgt
See options A and H.
WEIGHT CODES

ITEM SETUP
Item (ITEM)
KT Enter Rcpt Unit Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Net Wgt from Tare
See options AT and H.
L Enter Rcpt Gross Wgt, Ord Gross Wgt
See options B and F. 
LT Enter Rcpt Gross Wgt, Ord Gross Wgt, Calc Rcpt Net Wgt from Tare
See options BT and F. 
M Enter Rcpt Gross Wgt, Ord Net Wgt
See options B and G.
MT Enter Rcpt Gross Wgt, Ord Net Wgt, Calc Rcpt Net Wgt from Tare
See options BT and G.
N Enter Rcpt Gross Wgt, Ord Gross Wgt, Ord Net Wgt
See options B and H.
NT Enter Rcpt Gross Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Net Wgt from Tare
See options BT and H.
O Enter Rcpt Net Wgt, Ord Gross Wgt
See options C and F.
OT Enter Rcpt Net Wgt, Ord Gross Wgt, Calc Rcpt Gross Wgt from Tare
See options CT and F. 
P Enter Rcpt Net Wgt, Ord Net Wgt
See options C and G.
PT Enter Rcpt Net Wgt, Ord Net Wgt, Calc Rcpt -Ord Gross Wgt from Tare
See options CT and G.
WEIGHT CODES

ITEM SETUP
Item (ITEM)
Q Enter Rcpt Net Wgt, Ord Gross Wgt, Ord Net Wgt
See options C and H.
QT Enter Rcpt Net Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Gross Wgt from Tare
See options CT and H.
S Enter Rcpt Unit Wgt, Rcpt Net Wgt, Ord Gross Wgt
See options D and F.
U Enter Rcpt Unit Wgt, Rcpt Net Wgt, Ord Net Wgt, Ord Gross Wgt
See options D and H.
V Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Gross Wgt
See options E and F.
W Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Net Wgt
See options E and G.
X Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Gross Wgt, Ord Net Wgt
See options E and H.
WEIGHT CODES

MISCELLANEOUS SETUP
Adjustment Type Codes (ADJU).................................................................... 312
Load Type (LOAD)........................................................................................... 315
Transport Mode Codes (TRMO) ..................................................................... 318
Carriers (CARR)............................................................................................... 320
Load Analysis (LDAN) .................................................................................... 327
Shippers (SHIP) ............................................................................................... 328
Retail Profiles (RETP) ..................................................................................... 336
Consignees (CONS) ........................................................................................ 338
Sold-To Codes (SOLD) ................................................................................... 347
Drivers (DRIV).................................................................................................. 351
Language Code (LANG).................................................................................. 353
Alternate Item and Language (ALIT) ............................................................. 355
Telephone Numbers (TELE) ........................................................................... 359

MISCELLANEOUS SETUP
Adjustment Type Codes (ADJU)
Adjustment Type Codes (ADJU)
OVERVIEW
In this program, you set up your adjustment type codes. Adjustment type codes are required when you make 
adjustments to inventory in programs such as ENAJ (Enter Inventory Adjustment), MATR (Massive 
Adjustment) and ENPH (Enter Physical Parameters). These codes specify the type of adjustment; for 
example, aged product, damaged goods, lost inventory, customer returns, receipt correction, other, etc.
You will need one adjustment type code for each type of adjustment to inventory that you make in your 
warehouse.
In this program, the following items require definition:
▪ the adjustment code and its description
▪ the reason for the adjustment
▪ the document to be printed whenever an adjustment is made using this adjustment type
▪ whether there any charges associated with the adjustment and whether the current or original date is 
used for such charges
▪ whether a product’s receipt date changes during an adjustment
▪ the adjustment’s EDI status
The following adjustment type codes are system codes and cannot be modified or deleted: CY (Cycle Count 
Adjustment), HL (Hold Adjustment), IF (Information Only Adjustment), RL (Relocate) and WGT (Weight 
Adjustment).
PREREQUISITES: one document set up in DOCU with a document type of ADJ
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all the reasons why you make adjustments to your inventory
FIELD DESCRIPTIONS
Adjustment Code Mandatory
Your adjustment code. For example, AGED for Aged Product.

MISCELLANEOUS SETUP
Adjustment Type Codes (ADJU)
Description Mandatory
Your adjustment code description.
Adjustment Analysis 
Description
EXTRNL = External
The adjustment is the result of a customer-related error.
INTNL = Internal
The adjustment is the result of a warehouse-related error.
OTHER = Other
The adjustment is the result of neither a customer-related error nor a warehouse-related error.
Document Code (DOCU) Mandatory
This field allows you to specify a custom document or report that you can print 
to track your adjustments. Any document code that you enter requires a document type of ADJ in DOCU. If you do not have a custom document for adjustments, you must create a dummy document in DOCU to populate this field.
Enter Charges Y = Yes
N = No
If you select Yes, you will be prompted to enter charges when making an 
adjustment with this adjustment type. You must select Yes if you intend to 
charge for this adjustment type.
If there is no charge for this adjustment type, select No.
Effective Date for 
Charges
Only available if Enter Charges = Yes
C = Current
O = Original
If you select Original, the charges for this adjustment type that were in effect 
the day the product was received will apply. If you select Current, current 
charges for this adjustment type will apply. 
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Adjustment Type Codes (ADJU)
PROCEDURE
1 Enter ADJU.
2 Click on Enter Criteria then Execute Query to see whether the adjustment types that you require have 
already been set up. If you need to set up a new adjustment type, click on Create Record.
3 Key in your adjustment code and press Enter.
4 Key in a meaningful description for your adjustment code (for example, Damaged Goods or Lost Inventory) and press Enter.
5 Use your pick list to select the appropriate adjustment analysis description. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select Code.
6 Use your pick list to select the appropriate document code for the document or report that you wish to 
print whenever this adjustment type is made.
7 In the Enter Charges field, key in Y for Yes or N for No and press Enter.
8 In the Effective Date for Charges field, key in O for Original or C for Current and press Enter.
9 In the Date Used for Adjustments / Renewals field, key in O for Original or C for Current and press Enter.
10 In the Send via EDI field, key in Y for Yes or N for No and press Enter.
Date Used for Adjustments / RenewalsC = Current
O = Original
If you select Original, the product to which you are applying this adjustment 
type will retain its original received date and will renew on that date. If you 
select Current, the product to which you are applying this adjustment type will 
be assigned the current date as its received date and will renew on the day 
that the adjustment was made.
Send via EDI Y = Yes
N = No
Set to Yes if the customer has a need to see the adjustment, the adjustment is 
recorded on a document or report and the only way the customer can get that 
document or report is through EDI.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Load Type (LOAD)

Adjustment Type Codes
11 Repeat the above steps for each additional adjustment type that you wish to add to ADJU.
12 When you finish entering your adjustment codes, click on Return to Main and then Exit to exit.
Load Type (LOAD)
OVERVIEW
In this program, you set up your load types. Load types serve four functions in AccellosOne 3PL:
▪ you can use them to apply extra charges such as sorting, freezing, stencilling, unloading, etc. that you 
incur when receiving or shipping a load 
PREREQUISITES: SKCL
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Load Type (LOAD)
▪ you can use them for reporting purposes only to describe the types of loads entering and leaving your 
warehouse (for example, palletized load, floor-loaded product, slip-sheeted load, etc.)
▪ you can use them in the appointment system to define the number of minutes required to load or unload 
a given quantity of a given load type
▪ you can use them to define the number of temperatures readings required
You assign a load type to a load in ENRE (for inbounds) and ENOR (for outbounds). If you do not require load 
types for your warehouse, use AccellosOne 3PL load type called NA (Not Applicable).
FIELD DESCRIPTIONS
Load Type Code Mandatory
Your load type code. For example, FL for Floor Loading.
Description Mandatory
Your load type description.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Num of Temperatures In this field, you define the number of different temperatures readings by load 
type required for each receipt that you enter in RFCH. 
You can enter any number between 0 and 6 in this field. The number zero indicates no restrictions, while any number between 1 and 6 indicates the exact 
number of temperatures required in RFCH. 
If you specify a non-zero value in this field and the number of temperature 
readings that you enter in RFCH does not match this value, the temperature(s) will be rejected and an error message will display.
Inb. Fixed Minutes See the “Appointment Planner” section in the Operations 2 Guide.
Outb. Fixed Minutes See the “Appointment Planner” section in the Operations 2 Guide.
Override Pick Method to 
EACH
All Pick Methods
Case Pick Method Only
No CART Pick Method
Pallet Pick Method Only
In this field, you can override a pick method to EACH. 

MISCELLANEOUS SETUP
Load Type (LOAD)
PROCEDURE
1 Enter LOAD.
2 Click on Enter Criteria then Execute Query to see whether the load types that you require have already 
been set up. If you need to set up a new load type, click on Create Record.
3 Key in your load type code and press Enter.
4 Key in a meaningful description for your load type code and press Enter.
5 Press Enter to bypass the Labor Standard Modifier field.
6 If required, key in the number of temperatures required for this load type and press Enter. If you do not 
require an exact number of temperatures, leave this field blank.
7 If required, key in the number of fixed minutes for inbound appointments for this load type and press 
Enter. If you do not require a number of fixed minutes for inbound appointments, leave this field blank.
8 If required, key in the number of fixed minutes for outbound appointments for this load type and press 
Enter. If you do not require a number of fixed minutes for outbound appointments, leave this field blank.
9 If required, select a pick method from the Override PIck Method to EACH pick list or press Enter to 
bypass this field.
10 If required, key in Y for Yes in the Disable Item Subst. from PL field and press Enter or press Enter with 
the field blank to bypass this option.
11 If required, key in Y for Yes in the Disable Count Backs field and press Enter or press Enter with the field 
blank to bypass this option.
Your cursor will be positioned in the Weight Block.
Disable Item Subst. from 
PL
Y = Yes
N = No
If you enter Y for Yes in this field, allocation and item substitution from pickline type locations will be deactivated for orders assigned to this load type.
Disable Count Backs Y = Yes
N = No
If you enter Y for Yes in this field, count backs in RFPIC will be deactivated for 
orders assigned to this load type.
WEIGHT/QUANTITY BLOCK
The fields in this block are used to define the number of minutes required to load or unload a given quantity of a given load type. See the appointment system section in the Operations 2 Guide for further information.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Transport Mode Codes (TRMO)

Load Type for NA (Not Applicable)
12 Click on In/Out Block to exit create mode. Then click on Master Block and Exit to exit.
Transport Mode Codes (TRMO)
OVERVIEW
In this program, you set up your transport mode codes. Transport mode codes describe how freight is 
shipped from the warehouse: by air, sea, ground or by all modes. They must be attached to carriers in CARR 
if you use ShippingLIVE to ship and track your outbound orders. They are also a requirement in the Transport 
Mode Block of ITEM if you wish to capture hazmat information for a given item on an outbound order.
PREREQUISITES: None
ATTACHED TO: ITEM (Item Codes)
CARR (Carriers)
GLOBAL/UNIQUE: Global
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Transport Mode Codes (TRMO)
PROCEDURE
1 Enter TRMO.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
3 If you need to set up another code, click on New.
4 Key in your transport mode code and press Enter.
5 Key in a description for your new code and press Enter.
6 If required, key in a reference for your new code.
7 Select the appropriate transport mode type from the dropdown list.
8 Repeat the above four steps for each additional transport mode code that you wish to add.
FIELD DESCRIPTIONS
Code Mandatory
Your transport mode code.
Description Mandatory
Your transport mode description.
Reference Optional
Miscellaneous reference information about your transport mode.
Transport Mode Type All Modes
Ground
Air
Sea
Your transport mode type.

MISCELLANEOUS SETUP
Carriers (CARR)
Transport Mode Codes
9 When you finish adding your transport mode codes, click on Save to save your changes.
10 Click on Exit to exit the program.
Carriers (CARR)
OVERVIEW
In this program, you set up your commonly used carriers. You set up the name and address of the carrier, the 
carrier’s Standard Carrier Alpha Code, whether or not the carrier will be used to carry loads generated 
through AccellosOne Transport and the message (optional) that you want to print automatically on the 
carrier’s bill of lading.
The carriers that you create in CARR are attached to loads in ENRE (for inbound loads) and ENOR (for 
outbound loads). If you do not have any commonly used carriers, it is possible to bypass the Carrier fields in 
ENRE and ENOR.
PREREQUISITES: MESS, TETP
ATTACHED TO: CUST (Customer Setup)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all your commonly used carriers

MISCELLANEOUS SETUP
Carriers (CARR)
FIELD DESCRIPTIONS
Carrier Code Mandatory
Your carrier code. A carrier code can consist of any combination of numbers 
or letters up to 10 characters in length. The single quote (’) and double quote 
(“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are 
not recommended. Other special characters are generally supported.
Name Mandatory
The name of your carrier.
Address 1/2/3/4 Mandatory
The address of the carrier
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (Zip/Postal Code), the city, state/province and 
country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Standard Carrier Alpha 
Code
Mandatory
If the carrier has a predefined SCAC code, enter it in this field. If the carrier 
does not have a SCAC code, use X to bypass this field.

MISCELLANEOUS SETUP
Carriers (CARR)
Weight Measure I = Imperial
M = Metric
The carrier’s weight measure. This weight measure prints on the bill of lading 
or other shipping document and need not be the same as the item’s weight 
measure in ITEM. 
External Carrier Flag Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL orders assigned to this carrier will be accessible to a second freight interface. If you set this flag to N for 
No, AccellosOne 3PL orders assigned to this carrier will NOT be accessible to 
a second freight interface.
Freight Interface Type 
Code
FRT = Freight Interface 
A common carrier who picks up consolidated loads generated through AccellosOne Transport.
NFR = No Freight Interface
A common carrier who carries regular inbound and outbound loads processed 
in ENRE and ENOR.
Freight Pay Carrier Code 
(CARR)
Reserved for future use.
Freight Type Code 
(FRTY)
Only available if Carrier Type Code = FRT
The freight type as defined by US regulatory authorities.
Freight Mileage Rate Reserved for future use.
Freight Minimum PaymentReserved for future use.
Freight Discount PercentageReserved for future use.
Carrier Type Code CPU = Customer Pick-Up
The customer delivers and picks up his own product and does not use a common carrier.
This field is set up by HighJump.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Carriers (CARR)
Generated Number Profile CodeReserved for future use.
Transport Mode Code 
(TRMO)
A transport mode code is needed for ShippingLIVE. It is also a requirement in 
the Transport Mode Block of ITEM if you wish to capture hazmat information 
for a given item on an outbound order.
B/L Message Code 
(MESS)
Optional
The message that you enter here will print on the carrier’s bill of lading.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
SKU Class for Number of 
Labels
Only available for BarTender labels and ShippingLIVE
The SKU class that you enter here overrides the default SKU class defined in 
DOCU (Documents). 
Rounding Method for 
Number of Labels
Only available for BarTender labels and ShippingLIVE
U = Up
D = Down
The Rounding Method that you enter here overrides the default rounding 
method defined in DOCU (Documents). 
Isolator Code (ISOL) Reserved for future use
Allow Banding Reserved for future use
Compliant Label 
Required
Reserved for future use
EDI Required Flag Reserved for future use
A1 Ship Service The carrier’s A1 Ship service.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Carriers (CARR)
INSURANCE BLOCK
The information in this block is for informational purposes only and not used in any other AccellosOne 3PL 
program.
PROCEDURE
1 Enter CARR.
2 Click on Create Record.
3 Key in your carrier code and press Enter.
4 Key in the name of your new carrier and press Enter.
5 Key in the address of the carrier, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the carrier’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next 
field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and 
press Enter. You will be brought back into CARR with the appropriate information filled in.
7 If the carrier has a predefined SCAC code, enter it in this field and press Enter. If the carrier does not 
have a SCAC code, key in X and press Enter to bypass this field.
8 Key in your carrier’s weight measure (I for Imperial or M for Metric) and press Enter.
9 If required, key in Y for Yes or N for No in the External Carrier Required field and press Enter.
Yard Location Profile 
Code
Reserved for future use
FIELD DESCRIPTIONS
Policy Code The carrier’s policy number.
Description A description of this policy.
Deductible The policy’s deductible.
From Date The date that insurance coverage starts. The format of this date must match 
the date format in COMP (Company Code).
To Date The date that insurance coverage ends. The format of this date must match 
the date format in COMP (Company Code).
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Carriers (CARR)
10 Use your pick list to select the appropriate carrier type code for this carrier. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select Code. 

Carrier screen showing prompt for generated number profile
11 Press Enter to bypass the Generated Number Profile Code field.
12 If required, key in your transport mode code in the Transport Mode Code field and press Enter. If your 
carrier does not require a transport mode code, press Enter to bypass this field.
13 In the B/L Message Code field, you can specify a standard message to print on the carrier’s bill of lading. 
If such a message is required, use your pick list to select the appropriate message code.
14 Press Enter the required number of times to bypass the Extra Charge Profile Code, Labor Standard Modifier, SKU Class for Number of Labels, Isolator Code and Yard Location Profile Code fields.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax 
numbers and e-mail addresses for this carrier if you choose to do so or you can leave this block blank 
If you enter FRT for Freight: If you enter any other code:
a) Enter the appropriate values in 
the Freight Pay Carrier Code and 
Freight Type Code fields.
b) Enter the appropriate value in 
the Freight Type Code field.
c) Press Enter to bypass the 
Freight Mileage Rate, Freight 
Minimum Payment and Freight 
Discount Percentage fields.
a) Proceed to next step.

MISCELLANEOUS SETUP
Carriers (CARR)
and not use it. If you do not want to use the Telephone Block at this time, click on Return to Main. Then 
proceed to step 13. 
15 In the Code field, use your pick list to select the appropriate telephone type. Then key in the telephone 
number and press Enter. Next key in your contact name for this carrier and press Enter followed by the 
contact’s position (press Enter again).
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

Telephone Block in CARR
CARR also contains a Motor Carrier Block and an Insurance Block. The Motor Carrier Block is reserved 
for future use. The Insurance Block allows you to record a carrier’s policy number, deductible and period 
of coverage.
16 If you wish to record insurance information for the carrier, click on Motor Carrier Block and then Insurance Block to enter the Insurance Block. If you do not wish to set up these blocks at this time, proceed to 
step 20.
17 Key in the carrier’s policy number and press Enter.
18 Key in a description for this policy and press Enter.
19 Key in the amount of the deductible for the policy and press Enter.
20 Key in the date that insurance coverage starts and press Enter.
21 Key in the date that the insurance coverage ends and press Enter.

MISCELLANEOUS SETUP
Load Analysis (LDAN)

Carrier screen showing Insurance Block
22 When you finish entering your insurance information, click on Return to Main to exit create mode. 
23 Click on Master Block and Exit to exit.
Load Analysis (LDAN)
OVERVIEW
In this program, you set up your load analysis codes. You use these codes to track the types of loads that you 
receive from shippers (inbounds) and the types of loads that you ship to consignees (outbounds). For 
inbound loads, load analysis codes are reserved for future use and you should use the system load analysis 
code called NA (Not Applicable) for your shippers.
For outbound loads, load analysis codes are a restriction in Wave Manager; that is, you can filter the orders in 
a wave by load analysis code. For example, you could assign load analysis codes to consignees by region — 
NE for North-East, SW for South-West, MW for Mid-West, etc. — and filter your waves by consignee region.
PREREQUISITES: None
ATTACHED TO: SHIP (Shippers)
CONS (Consignees)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Shippers (SHIP)
PROCEDURE
1 Enter LDAN.
2 Click on Enter Criteria then Execute Query to view your NA (Not Applicable) code.

Load Analysis Codes
3 When you finish viewing your NA code, click on Exit to exit.
Shippers (SHIP)
FIELD DESCRIPTIONS
Load Analysis Code Mandatory
Your load analysis code.
Description Mandatory
Your load analysis description.
PREREQUISITES: LDAN, DIFP, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory

MISCELLANEOUS SETUP
Shippers (SHIP)
OVERVIEW
In this program, you set up your commonly used shippers. The shippers that you create in SHIP are attached 
to inbound loads in ENRE. If you do not have any commonly used shippers, it is possible to bypass the 
Shipper field in ENRE.
If the shipper is the same as the customer (that is, your customer is shipping inbound loads from his own 
facility), you have two options:
▪ you can set up a generic shipper called SAME for all your customers
▪ you can set up individual shippers for each customer in SHIP with the same code as the customer (with 
this option, the Shipper Code field in ENRE will be automatically populated when receiving product from 
the customer)
A generic SAME-type shipper requires the following setup in SHIP:
▪ a shipper code of SAME 
▪ a period or slash in the Address 1 field
▪ any valid ZIP code to bypass the ZIP Code field
▪ a customer code of .ALL
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
An individual shipper for each customer requires the following setup in SHIP:
▪ a shipper code that is the same as the customer code (for example, a customer code of ABC_SUP in 
CUST and a shipper code of ABC_SUP in SHIP)
▪ a complete address and valid ZIP code
▪ a customer code of .ALL
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
▪ a workflow profile code (optional)
If the shipper is not the same as the customer (that is, the inbound loads originate from a separate company), 
you must set up a complete SHIP record. A complete SHIP record requires the following:
▪ a valid shipper code and name
▪ a complete address and valid ZIP code
▪ the customer code 
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
▪ a workflow profile code (optional)
OTHER REQUIREMENTS: The names and addresses of your customers’ shippers
NOTE Do not confuse the term shipper with customer or depositor. A shipper in 
AccellosOne 3PL is always a company shipping to your warehouse — that is, the 
originator of an inbound shipment. The term shipper never refers to an outbound 
order.

MISCELLANEOUS SETUP
Shippers (SHIP)
FIELD DESCRIPTIONS
Shipper Code Mandatory
Your shipper code. A shipper code can consist of any combination of numbers 
or letters up to 10 characters in length. The single quote (’) and double quote 
(“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are 
not recommended. Other special characters are generally supported.
Name Mandatory
The name of your shipper.
Address 1/2/3/4 Mandatory
The address of the shipper.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (Zip/Postal Code), the city, state/province and 
country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.

MISCELLANEOUS SETUP
Shippers (SHIP)
Customer Code (CUST) Mandatory
If you are using the SAME option, use .ALL. If you are setting up real shippers 
with names and addresses, you can attach a particular customer to a particular shipper or you can use .ALL for all customers. If you attach a particular 
customer to a particular shipper, only that shipper will be available when 
receiving product from that customer. If you use .ALL as your customer, the 
shipper will be available to all customers.
The customer code restrictions that you define in SHIP are subject to the 
operator restrictions that you set up in OPRS (Operator Restrictions). For 
example, if a given shipper is available to all customers but a given operator is 
restricted to three shippers, the operator will only see those three shippers 
when he or she enters a receipt in ENRE.
Weight Measure Code for 
Receipts
Mandatory
The unit of measure for this shipper (pounds, kilograms, tons, etc.). If you 
receive a non-standard weight item from this shipper, the weight measure that 
you enter in this field will override the item’s weight measure (defined in ITEM) 
when you process a receipt in ENRE.
Load Analysis Code 
(LDAN)
Mandatory
The load analysis code for this shipper.
Shipper Type Set to W for Warehouse.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Shippers (SHIP)
Workflow Profile Code 
(DIFP)
Optional
If you enter a DIFP profile in this field, it will override the DIFP profile that you 
attached to the customer in CUST. If you do not enter a DIFP profile in this 
field, the system will use the default profile specified in CUST for this shipper /
customer. You use this field only if a particular shipper has unique flows or 
special documents that require printing.
Do not enter a DIFP profile in this field if you are setting up a SAME-type shipper.
If you click on the View Flow Chart icon , you can see a flow chart of your 
profile showing each flow, the documents if any attached to the flow as well as 
any special verify programs.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Item Location Profile 
Code (ILOP)
Optional
If you enter an ILOP profile in this field, product received from this shipper will 
use this ILOP profile for put-away instead of the ILOP profile attached to the 
item that you are receiving.
External Reference Number
Optional
You can add any miscellaneous reference information about a shipper in this 
field.
Establishment Number Reserved for future use.
Country Code - Origin Reserved for future use.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Shippers (SHIP)
PROCEDURE
1 Enter SHIP.
2 Click on Enter Criteria then Execute Query to see whether the shippers that you require have already 
been set up. If you need to set up a new shipper, click on Create Record.
3 Key in your shipper code and press Enter.
4 Key in the name of your shipper and press Enter.
5 Key in the address of the shipper, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the shipper’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next 
field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and 
press Enter. You will be brought back into SHIP with the appropriate information filled in.
7 Key in your customer code and press Enter or use .ALL for all your customers.
8 In the Weight Measurement Code for Receipts field, use your pick list to select the appropriate unit of 
measure for this shipper. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the 
appropriate code and click on Select Code.
Master Shipper Y = Yes
N = No
If you set this flag to for Yes, you can define the shipper as a master shipper 
and attach non-master shippers to the shipper. A master shipper is merely a 
way of grouping a number of related shippers. By setting up the appropriate 
query in d’Amigo for your master shipper(s), you can easily track inventory 
activity for a group of related shippers; for example, all plants in a certain geographical area belonging to the same customer.
If you set this flag to N for No, the shipper is not a master shipper.
Attached to (SHIP) Only available if the Master Shipper flag = N for No
The master shipper that this shipper is attached to.
Suppress Inventory Attributes
Y = Yes
N = No
If you select Yes, inventory attribute capture for this shipper will be deactivated.
Last Activity Date Reserved for future use.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Shippers (SHIP)

Shipper screen showing prompt for load analysis code
9 Key in your shipper’s load analysis code and press Enter.
10 Key in W for Warehouse as your shipper type and press Enter.
11 If required, use your pick list to select the appropriate workflow profile code for this shipper. If you do not 
require an workflow profile code, press Enter to bypass this field.
12 Press Enter to bypass the Extra Charge Profile Code field.
13 Press Enter to bypass the Labor Standard Modifier field.

MISCELLANEOUS SETUP
Shippers (SHIP)

Shipper screen showing prompt for item location profile code
14 If required, key in an item location profile code for this shipper and press Enter. If no item location profile 
is required, press Enter with the field blank to bypass this option.
15 If required, key in your external reference number for this shipper and press Enter. If no external reference number is required, press Enter with the field blank to bypass this option.
16 Press Enter twice to bypass the Establishment Number and Country Code - Origin fields.
17 In the Shipper Code Master field, key in the appropriate value (N for No or Y for Yes) and press Enter.
18 If you entered N for No in the previous field, you can specify a master shipper for the shipper. If you wish 
to attach a master shipper to the shipper, key in the shipper code for the master shipper and press Enter.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax 
numbers and e-mail addresses for this shipper if you choose to do so or you can leave this block blank 
and not use it. If you do not want to use the Telephone Block at this time, click on Master Block. Then 
proceed to step 16. 
19 In the List Code field, use your pick list to select the appropriate telephone type. Then key in the telephone number and press Enter. Next key in your contact name for this carrier and press Enter followed 
by the contact’s position (press Enter again). 
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

MISCELLANEOUS SETUP
Retail Profiles (RETP)

Telephone Block in SHIP
20 Click on Master Block and then Exit to exit.
Retail Profiles (RETP)
OVERVIEW
In this program, you set up your retail profiles. The retail profiles that you create in RETP are attached to 
consignees in CONS. Retail profiles serve two functions in AccellosOne 3PL:
▪ they allow you to restrict a wave in the Wave Manager by consignee type
▪ they make it possible to report by consignee type in d’Amigo
PREREQUISITES: NONE
ATTACHED TO: CONS (Consignees)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Retail Profiles (RETP)
PROCEDURE
1 Enter RETP.
2 Click on Enter Criteria then Execute Query to see which retail profiles have already been set 
up.
FIELD DESCRIPTIONS
Retail Profile Code Mandatory
Your retail profile code.
Description Mandatory
Your retail profile code description.
Type Other
Repair
Store
Vendor
Warehouse
Your consignee type.
Home Delivery Reserved for future use
Re-ticketing Reserved for future use

MISCELLANEOUS SETUP
Consignees (CONS)

Retail Profiles
3 If you need a new retail profile, click on New to create one.
4 Key in your retail profile code and press Enter.
5 Key in a description for your new retail profile code and press Enter.
6 Select the appropriate consignee type (Other, Repair, Store, Vendor, Warehouse) from the Type dropdown list.
7 Click on Save to save your new profile.
8 Click on Exit to exit RETP.
Consignees (CONS)
OVERVIEW
In this program, you set up your commonly used consignees. The consignees that you create in CONS are 
attached to outbound loads in ENOR. If your customers do not have any commonly used consignees, you do 
not need to set up consignees in this program.
PREREQUISITES: CUST, LDAN, MESS, DIFP, PIPR, DAPC, TETP, LANG
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The names and addresses of your customers’ consignees

MISCELLANEOUS SETUP
Consignees (CONS)
The main options in CONS are:
▪ the consignee’s name and address
▪ the consignee’s workflow profile (only required if the consignee has special flows or documents that differ from the customer’s flows and documents)
▪ the consignee’s picking profile (only required if the way in which you pick product for this consignee differs from the picking profile defaults; these defaults are set up at the customer level in DSRP and at the 
item level in ITEM)
▪ the consignee’s item location profile (only required if the way in which you pick product for this consignee differs from the default item location profile attached to the item) 
Consignees can be either customer specific or general. If a consignee is customer specific, only orders 
belonging to the customer that you specify can be shipped to the consignee. If a consignee is general, any 
order belonging to any customer can be shipped to the consignee. 
FIELD DESCRIPTIONS
Consignee Code Mandatory
Your consignee code. A consignee code can consist of any combination of 
numbers or letters up to 10 characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain 
programs and are not recommended. Other special characters are generally 
supported.
Name Mandatory
The name of your consignee.
Address 1/2/3/4 Mandatory
The address of your consignee.

MISCELLANEOUS SETUP
Consignees (CONS)
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal 
code is already defined in ZIPO (Zip/Postal Code), the city, state/province and 
country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Language Code (LANG) Mandatory
If you have an alternate item and description set up in ALIT (Alternate Item 
and Language) for an item, an alternate item and description will be captured 
when that item is being shipped to this consignee.
Customer Code (CUST) Mandatory
You can attach a particular customer to a particular consignee or you can use 
.ALL for all customers. If you attach a particular customer to a particular consignee, only that consignee will be available when shipping orders for that 
customer. If you use .ALL as your customer, the consignee will be available to 
all customers.
The customer code restrictions that you define in CONS are subject to the 
operator restrictions that you set up in OPRS (Operator Restrictions). For 
example, if a given consignee is available to all customers but a given operator is restricted to three consignees, the operator will only see those three consignees when he or she enters an order in ENOR.
B/L Message Code 
(MESS)
Optional
The message that you enter here will print on the carrier’s bill of lading.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Consignees (CONS)
Load Analysis Code 
(LDAN)
Mandatory
The load analysis code for this consignee.
Freight Destination Code Reserved for future use.
Freight Discount PercentageReserved for future use.
Workflow Profile Code 
(DIFP)
Optional
If you enter a DIFP profile in this field, it will override the DIFP profile that you 
attached to the customer in CUST. If you do not enter a DIFP profile in this 
field, AccellosOne 3PL will use the default profile specified in CUST for this 
consignee/customer. You use this field only if a particular consignee has 
unique flows or special documents that require printing.
If you click on the View Flow Chart icon , you can see a flow chart of your 
profile showing each flow, the documents if any attached to the flow as well as 
any special verify programs.
Picking Profile Code 
(PIPR)
Optional
If you enter a PIPR profile in this field, it will override the PIPR profiles that you 
attached to the consignee’s customer in DSRP and to the item in ITEM (PIPR 
is optional in ITEM). If you do not enter a PIPR profile in this field, AccellosOne 3PL will use the default profile specified in DSRP for this consignee/
customer — unless you specify a PIPR profile for an item and this item is 
being shipped to this consignee.
Priority You can filter waves in Wave Manager by consignee priority.
Day Profile Code (DAPC) Only available if you auto-print order documents
See the Operations 2 Guide for further information on day profile codes.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Consignees (CONS)
Retail Profile Code 
(RETP)
Optional
The consignee’s retail profile code.
Allow Back Orders See the back orders section in the Operations 2 Guide.
External Reference Number
Optional
You can add any miscellaneous reference information about a consignee in 
this field.
Item Location Profile 
Code (ILOP)
Optional
If you enter an ILOP profile code in this field, product shipped to this consignee will use this ILOP profile code for picking instead of the ILOP profile 
attached to the item that you are picking.
Ship Only Fully Filled 
Orders
See “Allocating Only Fully Filled Orders” in Allocation and Wave Manager.
Master Consignee Y = Yes
N = No
If you set this flag to for Yes, you can define the consignee as a master consignee and attach non-master consignees to the consignee. A master consignee is merely a way of grouping a number of related consignees. By setting 
up the appropriate query in d’Amigo for your master consignee(s), you can 
easily track inventory activity for a group of related consignees; for example, 
all stores in a certain geographical area belonging to the same customer.
If you set this flag to N for No, the consignee is not a master consignee.
Attached to (CONS) Only available if the Master Consignee flag = N for No
The master consignee that this consignee is attached to.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Consignees (CONS)
Appointment Required Y = Yes
N = No
If you set this flag to Yes, an appointment is required for this consignee. If you 
set this flag to No, no appointment is required for this consignee. The appointments referred to in this field are appointments at the consignee’s premises — 
not appointments at the warehouse set up in AccellosOne 3PL’s appointment 
system.
External Reference Number 2/3/4
Optional
You can add any miscellaneous reference information about a consignee in 
these fields.
Allow Banding Reserved for future use.
Banding SKU Class 
(SKCL)
Reserved for future use.
Consignee Consolidation 
Type
Reserved for future use.
Pallet Code If you specify a pallet code in this field, RFPICK will validate that any pallet 
code entered during order picking for that consignee will match the consignee's pallet code. Pallet code validation must be activated in MRFP by setting the Enter Pallet Type flag to Yes.
Special Consignee 
Requirement
Y = Yes
N = No
If you set this flag to Yes, the consignee is marked as having a special requirement. If you set this flag to No, the consignee is considered a normal consignee with no special requirements.
Outbound Type ASN 
Reporting
Reserved for future use.
MSDS Paperwork 
Required
Reserved for future use.
Single Item Per Outbound PalletIf you set this flag to Yes, the Pallet Build engine will check this flag and 
restrict outbound pallets to a single item. This flag is only supported in RFITLV.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Consignees (CONS)
CARRIER BLOCK
The Carrier Block allows you to specify your preferred carriers for each consignee. These carriers are for 
information purposes only and do not affect the carriers available for a particular consignee during order entry 
in ENOR.
SKU Class for Number of 
Labels
Only available for BarTender labels and ShippingLIVE
The SKU class that you enter here overrides the default SKU class defined in 
DOCU (Documents) and CARR (Carriers). 
Rounding Method for 
Number of Labels
Only available for BarTender labels and ShippingLIVE
U = Up
D = Down
The Rounding Method that you enter here overrides the default rounding 
method defined in DOCU (Documents) and CARR (Carriers). 
Maximum Weight RestrictionOnly available if weight restrictions are activated in WAPC (attribute 338)
If you enter a weight restriction and if this weight restriction is exceeded in 
OLOP for this consignee, the RF operator will not be allowed to continue loading.
Generate UCC-128 
Sequence Number
Only available for BarTender labels and ShippingLIVE
Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL will generate a UCC-128 
sequence number when printing case labels for this consignee. If you set this 
flag to N for No, no UCC-128 sequence number will be generated when printing case labels for this consignee.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Skip Cartonization Flag See the Cartonization section in the RF Guide.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Consignees (CONS)
PROCEDURE
1 Enter CONS.
2 Click on Enter Criteria then Execute Query to see whether the consignees you require have already been 
set up. If you need to set up a new consignee, click on Create Record.
3 Key in your consignee code and press Enter.
4 Key in the name of your consignee and press Enter.
5 Key in the address of the consignee, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the consignee’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet on AccellosOne 3PL, your cursor will not advance to the next 
field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and 
press Enter. You will be brought back into CONS with the appropriate information filled in.
7 In the Language Code field, use your pick list to select the appropriate language. To select a code using 
a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. 
Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
8 Key in your customer code and press Enter or use .ALL for all your customers.

Consignee screen showing prompt for B/L message code
9 In the B/L Message Code field, you can specify a standard message to print on the carrier’s bill of lading 
when shipping to this consignee. If such a message is required, use your pick list to select the appropriate message code. If you do not require such a message, press Enter to bypass this field.
10 Key in your load analysis code and press Enter or use your pick list to select it.

MISCELLANEOUS SETUP
Consignees (CONS)
11 In the Freight Destination Code field, AccellosOne 3PL will display the ZIP or postal code that you 
entered in the Zip Code field. Press Enter to accept it.
12 Press Enter to bypass the Freight Discount Percent field.
13 If required, use your pick list to select the appropriate workflow profile code for this consignee.
14 If required, use your pick list to select the appropriate picking profile code for this consignee.
15 Press Enter five times to bypass the following fields: Priority, Day Profile Code, Extra Charge Profile 
Code, Retail Profile Code and Allow Back Orders.

Consignees screen showing prompt for external reference number
16 If required, key in an external reference number and press Enter. If you do not need an external reference number, press Enter to bypass this field.
17 If required, use your pick list to select the appropriate item location profile code for this consignee.
18 Press Enter to bypass the Ship Only Fully Filled Orders Field.
19 In the Consignee Code Master field, key in the appropriate value (N for No or Y for Yes) and press Enter.
20 If you entered N for No in the previous field, you can specify a master consignee for the consignee. If you 
wish to attach a master consignee to the consignee, key in the consignee code for the master consignee 
and press Enter.
21 In the Appointment Required field, key in Y for Yes or N for No and press Enter.
22 Press Enter to bypass the SKU Class for Number of Labels field.
23 Press Enter to bypass the remaining fields on your screen.
AccellosOne 3PL will display the Carrier Block.
24 Click on Telephone Block to enter the Telephone Block. The Carrier Block is reserved for future use.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax 
numbers and e-mail addresses for this consignee if you choose to do so or you can leave this block blank 

MISCELLANEOUS SETUP
Sold-To Codes (SOLD)
and not use it. If you do not want to create a Telephone Block at this time, click on Return to Main. Then 
proceed to step 26. 
25 In the List Code field, use your pick list to select the appropriate telephone type. Then key in the telephone number and press Enter. Next key in your contact name for this consignee and press Enter followed by the contact’s position (press Enter again). 
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

Telephone Block in CONS
26 Click on Master Block and then Exit to exit.
Sold-To Codes (SOLD)
OVERVIEW
In this program, you set up your sold-to accounts. You use sold-to accounts if you wish to capture sold-to 
information when shipping an order to a consignee (set up in CONS). For example, if you are shipping 
product to a large department store, the individual store (for example, store #37) could be the consignee set 
up in CONS and head office, which is actually paying for the product, could be the sold-to account set up in 
SOLD. 
PREREQUISITES: CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Sold-To Codes (SOLD)
The sold-to accounts that you create in SOLD are attached to outbound orders in ENOR. If required, sold-to 
information can be printed on a bill of lading or other document; this capability must be programmed by 
HighJump.
If you do not need to capture sold-to information, create a single code on your system called SAME. For a 
SAME-type code, only the following is required:
▪ a sold-to code of SAME and a sold-to description
▪ a period or slash in the Address 1 field 
▪ any valid ZIP code to bypass the Zip Code field
▪ a customer code of .ALL
FIELD DESCRIPTIONS
Sold-To Code Mandatory
The name of your sold-to code. A sold-to code can consist of any combination 
of numbers or letters up to 10 characters in length. The single quote (’) and 
double quote (“) special characters are not valid and should never be used. 
Special characters such as “&”, “%” and “_” may cause problems in certain 
programs and are not recommended. Other special characters are generally 
supported.
Name Mandatory
The name of your sold-to code.
Address 1/2/3/4 Mandatory
The address of your sold-to account.

MISCELLANEOUS SETUP
Sold-To Codes (SOLD)
ZIP / Postal Code (ZIPO) Mandatory
If you are setting up a sold-to code of SAME, enter any valid ZIP code to 
bypass this field.
If you are setting up a real sold-to account, enter the ZIP code or postal code 
of the above address. If the ZIP code or postal code is already defined in ZIPO 
(Zip/Postal Code), the city, state or province and country will be filled in by 
AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you 
will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering 
the code and then defining the country code, city and state/province to which it 
belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Language Code (LANG) Optional
If you have an alternate item and description set up in ALIT (Alternate Item 
and Language) for an item, an alternate item and description will be captured 
when that item is being shipped to this sold-to account.
Customer Code (CUST) Mandatory
You can attach a particular customer to a particular sold-to account or you can 
use .ALL for all customers. Use .ALL if you are setting up a sold-to code of 
SAME. 
CAUTION If you are setting up a real sold-to account and if you have 
given your customers operations access to AccellosOne 3PL, do not use the 
.ALL option. Instead, assign a specific customer to each sold-to account. If 
you use the .ALL option, each of your customers will be able to see the sold-to 
accounts of all your other customers when entering an order in ENOR. 
Reference 1/2 Optional
You can record reference information about a sold-to account in this field.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Sold-To Codes (SOLD)
PROCEDURE
1 Enter SOLD.
2 Click on Create Record.
3 Key in your sold-to code and press Enter.
4 Key in your sold-to name and press Enter.
5 Key in the address of your sold-to, pressing Enter at the end of each line. For a SAME-type code, use a 
single period in the first address line to bypass this field.
6 In the ZIP / Postal Code field, key in the sold-to’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet on AccellosOne 3PL, your cursor will not advance to the next 
field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and 
press Enter. You will be brought back into CONS with the appropriate information filled in.
7 If required, key in your language code and press Enter. If no language code is required, press Enter to 
bypass this field.
8 Key in your customer code and press Enter or use .ALL for all your customers.
External Reference Number
Optional
You can add any miscellaneous reference information about a sold-to account 
in this field.
Last Activity Date Reserved for future use
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Drivers (DRIV)

Sold-To Codes screen showing SAME-type code
9 If required, key in reference information in the Reference 1/2 fields and press Enter or press Enter with 
these fields blank to bypass the reference option. 
10 If required, key in your external reference number and press Enter.
11 In the Telephone Block, enter any telephone numbers and contact names that you wish to attach to this 
sold-to account. When you finish entering your telephone numbers, click on Return to Main to exit create 
mode.
12 Click on Master Block and then Exit to exit.
Drivers (DRIV)
PREREQUISITES: None
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Drivers (DRIV)
OVERVIEW
In this program, you set up your drivers. You use drivers in the Carrier Block of ENRE and ENOR to identify 
the driver for a receipt or an order. For each driver that you set up, you can track the driver’s percentage, 
hourly rate and license number. This information is for look-up purposes only and is not used in any other 
AccellosOne 3PL program.
DRIV is intended for drivers who are employees of the warehouse — not drivers who work for outside 
carriers.
PROCEDURE
1 Enter DRIV.
2 Click on Create Record.
3 Key in your driver code and press Enter.
4 Key in your driver name and press Enter.
5 In the Percentage field, key in the percentage for this driver and press Enter. If there is no percentage for 
this driver, key in 0 as your percentage.
6 In the Hourly Rate field, key in the driver’s hourly rate and press Enter. 
FIELD DESCRIPTIONS
Code Mandatory
Your driver code.
Name Mandatory
The name of your driver.
Percentage Mandatory
The driver’s percentage. If the driver does not receive a percentage, enter 0.
Hourly Rate Mandatory
The driver’s hourly rate.
License Number Mandatory
The driver’s license number.

MISCELLANEOUS SETUP
Language Code (LANG)
7 If the License Number field, key in the driver’s license number and press Enter. 
8 Repeat the above steps for each additional driver that you wish to add to DRIV.

Drivers screen showing three drivers
9 When you finish setting up your drivers, click on Return to Main and then Exit to exit.
Language Code (LANG)
OVERVIEW
In this program, you set up your language codes. Language codes determine the language of field labels, hint 
lines, system codes, error messages, menu names, button text and any other text appearing in ActiveDesktop, AccellosOne 3PL, standard reports, e-Vista, d’Amigo and RF.
AccellosOne 3PL currently supports three base languages: English (ENUS), English (ENCA) and Spanish 
(ESMX). A base language is a language that has been fully translated by HighJump. You can create new nonbase languages if you wish to customize a base language. 
For example, if your base language is English (US) and you wish to change “item code” to “product code” in 
AccellosOne 3PL, you would create a language called ENG1 in LANG. Then you would enter TRMA (Translation Manger) and change “item code” to “product code” in the appropriate AccellosOne 3PL programs.
PREREQUISITES: None
ATTACHED TO: ALIT, CONS, SOLD, OPER
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

MISCELLANEOUS SETUP
Language Code (LANG)
Languages are operator-specific in AccellosOne 3PL. Different operators can work in different languages 
within the same system. For example, operator 1 could be defined as English, while operator 2 could be 
defined as Spanish. You assign languages to operators in OPER (Operator Code).
PROCEDURE
1 Enter LANG.
2 Click on Enter Criteria then Execute Query to see whether the languages that you require have 
already been set up. If you need to set up a new language, click on New.
FIELD DESCRIPTIONS
Language Code Mandatory
Your code for the language.
Description Mandatory
Your description for the language.
Base A base language is a language that has been fully translated by HighJump. 
Base languages can only be set up by HighJump.
Parent Language Code Mandatory for non-base languages
The base language that your non-base language will inherit from. That means 
that unless you explicitly change a field label, system code, error message, 
etc. in TRMA, your new language will inherit all field labels, system codes, 
error messages, etc. from the base language.

MISCELLANEOUS SETUP
Alternate Item and Language (ALIT)

Language Code
3 Key in your language code and press Enter. 
4 Key in your description and press Enter.
5 Select the appropriate base language from the Parent Language Code field.
6 When you finish entering your language, click on Save and then Exit to exit.
Alternate Item and Language (ALIT)
OVERVIEW
In this program, you set up your alternate items and descriptions or aliases. You use alternate items and 
descriptions when you wish to print foreign language item codes and descriptions on a bill of lading or other 
shipping document. You can also use this program to set up alternate spellings of an item or item description 
within the same language. 
For example, you could set up one language code for American English and another language code for 
British English. When you shipped to an American consignee, the item description could be “color blue” and 
when you shipped to a British consignee the item description could be “color blue.”
PREREQUISITES: LANG, ALTP, CUST, ITEM, SHIP, CONS, CARR, SOLD
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A custom document created by HighJump

MISCELLANEOUS SETUP
Alternate Item and Language (ALIT)
ALIT is a setup program for capturing alternate item and description information. If you want to print this information on a bill of lading or other document, you require a custom document programmed by HighJump.
Alternate items and descriptions consist of two elements: an “account to” value and an item. The “account to” 
value is a shipper, carrier, customer, consignee or sold to or any combination of these parties. An item is any 
item belonging to any customer. When you attach an “account to” value to an item, any order or receipt 
involving that item and that “account to” value will be assigned the alternate item and description. 
EXAMPLE 1
Account To = Consignee 1
Item = Item A
Language Code = SPANISH
Whenever you ship Item A to Consignee 1, a Spanish alternate item and description will be attached to an 
Item A document.
EXAMPLE 2
Account To = Shipper 2
Item = Item B
Language Code = GERMAN
Whenever you receive Item B from Shipper 2, a German alternate item and description will be attached to an 
Item B document.
NOTE The alternate language attached to an item in ALIT will always override the 
operator’s language. For example, an item can be attached to the language ENUS 
while the operator’s language is ENCA.
NOTE If you are setting up an alternate item and description for a consignee or 
sold to, the language code in ALIT for the consignee or sold-to must match the language code attached to the consignee in CONS or the sold-to in SOLD.
FIELD DESCRIPTIONS
Account To Code Mandatory
The party (customer, consignee, shipper, carrier, or sold-to) that is shipping 
the item (inbounds), carrying the item or receiving the item (outbounds). 

MISCELLANEOUS SETUP
Alternate Item and Language (ALIT)
Customer Code (CUST) Mandatory
The customer code of the item.
Item Code (ITEM) Mandatory
The item to which you wish to attach the alternate item and description.
Level 2/3/4 Optional
If you populate these fields with level 2/3/4 values, you can capture style, size 
and color information for apparel, furniture, bedding and similar products. For 
example, you scan in a level 2 or 3 value from a bar code in RFCH and the bar 
code value of 1234 (the supplier code) is automatically converted to blue shirt 
(L1), size medium (L2) based on your setup in ALIT.
Level 2/3/4 conversion from a bar code is supported in both RFCH and 
RFPIC.
Alternate Type Code 
(ALTP) 
Mandatory
The alternate type code for this item. You use alternate type codes to specify 
the type of bar coding on an item’s label.
Language Code (LANG) Mandatory
The language of the alternate item and description. 
Account Item Code Mandatory
The item’s alternate item code. The alternate item code can be the same as 
the main item code (for example, A1) or it can be different from the main item 
code (for example, A1 - SPANISH).
For single inventory level product only, you can receive under an alternate 
item code in the core RF receiving programs RFCH and RFPU.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Alternate Item and Language (ALIT)
PROCEDURE
1 Enter ALIT.
2 Click on Create Record
3 Key in your account to code and press Enter. If you account to value is a consignee or sold to, you must 
attach the language code that you set up in ALIT to either the consignee in CONS or the sold to in SOLD.
4 Key in the customer code of the item and press Enter.
5 Key in your item code and press Enter.
6 If required, enter your level 2/3/4 values.
7 Use your pick list to select the appropriate alternate type code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow 
keys to position your cursor over the appropriate code and click on Select Code.
8 Use your pick list to select the appropriate language code.
9 In the Account Item Code field, key in your alternate item code and press Enter.
Account Item Quantity Optional
This field allows you to specify the quantity for DUN-14 labels.
If you leave the Account Item Quantity field blank, the default value of 1 will be 
used. That is, one scan = a quantity of one. If you enter a value other than 
one, that value will be used to calculate the quantity received. For example, if 
the account item quantity is four and you perform two scans for that item, the 
quantity received will be eight (2 X 4).
Account Item UPC Optional
The UPC code for this item/lot/pallet ID.
Description Mandatory
The alternate description for the item in the language that you specified in the 
Language Code field. 
Alternate Description Optional
If required, you can enter a second alternate description for the item in this 
field.
FIELD DESCRIPTIONS

MISCELLANEOUS SETUP
Telephone Numbers (TELE)
10 If required, key in a quantity in the Account Item Quantity field and press Enter or press Enter with the 
field blank to bypass this function.
11 If required, key in the item’s UPC code in the Account Item UPC field and press Enter or press Enter with 
the field blank to bypass this function.
12 In the Description field, key in your alternate description for the item and press Enter.

Alternate Item & Language showing item A1 with a Spanish alternate description for Consignee 1
13 If required, key in a second alternate description in the Alternate Description field and press Enter or 
press Enter to bypass this field.
14 Click on Return to Main and then Exit to exit.
Telephone Numbers (TELE)
PREREQUISITES: TETP
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional

MISCELLANEOUS SETUP
Telephone Numbers (TELE)
OVERVIEW
In CUST, CARR, CONS and SHIP, you added your customer, carrier, consignee and shipper contact names 
and telephone numbers to the telephone blocks in these programs. In TELE you can add any additional 
numbers you need that are not related to customers, carriers, consignees and shippers. For example, you 
could enter the names and telephone numbers of your suppliers, other warehouse staff, etc. 
The telephone numbers that you add to TELE and to the telephone blocks in CUST, CARR, CONS and SHIP 
can be viewed in LOTE (Look Up Telephone Numbers).
PROCEDURE
1 Enter TELE.
2 Click on Enter Criteria then Execute Query to see whether the telephone numbers that you require have 
already been set up. If you need to set up a new number, click on Create Record.
3 Use your pick list to select the appropriate telephone type.
4 Key in the telephone number and press Enter. 
5 Key in your contact name for this number and press Enter.
6 If required, key in the contact’s position and press Enter or press Enter with the field blank to bypass this 
option. 
OTHER REQUIREMENTS: The names and telephone numbers of the people that you wish to add to 
your telephone list
FIELD DESCRIPTIONS
List Code (TETP) Mandatory
Your telephone list type for the number.
Telephone Mandatory
The telephone number.
Contact Mandatory
The name of the person or company.
Position Optional
The contact’s position.

MISCELLANEOUS SETUP
Telephone Numbers (TELE)
7 If you have additional numbers to enter, repeat the above steps for each additional number. 

Telephone Numbers
8 When you finish entering your telephone numbers, click on Return to Main and then Exit to exit.

MISCELLANEOUS SETUP
Telephone Numbers (TELE)

A
Account Item Code field (ALIT) 357
Account Item Quantity field (ALIT) 358
Account To Code field (ALIT) 356
Account Type field (CUST) 142
active status 5
ADIM (Inventory Messages) 272
ADJU (Adjustment Type Codes) 312
Adjustment Analysis Description field (ADJU) 313
Adjustment Process field (IQBP) 230
Adjustment Type Codes (ADJU) 312
ALIT (Alternate Item and Language) 355
allocation, by weight 220
Allow Overpick, Ignore Consignee field (ITEM) 283
Allow Override of Hold Code During Core RF Receiving 
field (IHOP) 245
Allow Picking in Staging Location field (LOTP) 57
Alternate Billing Group Code field (TERM) 134
Alternate Description field (ALIT) 358
Alternate Inventory Reporting Code field (ITAS) 235
Alternate Item and Language (ALIT) 355
Alternate Reporting Block (ITEM) 300
alternate sorts (depositor) 137
alternate sorts (item) 233
Alternate Type Code field (ALIT) 357
anniversary monthly frequency (IRSP) 203
anniversary weekly frequency (IRSP) 203
Appointment Required field (CONS) 343
Assign Block (DILP) 110
Assign Description to New Entity field (DILP) 103
Assign Location field (DIFP) 80
Assign Profile Code field (DILP) 105
Attached to field (CONS) 342
Attached to field (SHIP) 333
Auto Take-Off field (HOLD) 239
auto-generation of lot numbers 88
automatic printing (DIFP) 82
B
B/L Message Code field (CARR) 323
B/L Message Code field (CONS) 340
BANK (Bank Code) 162
Bank Code (BANK) 162
Base field (LANG) 354
Base for Cube/Weight field (ITEM) 293
Base SKU Code field (SKUS) 14
Billing Entity Minimum Charge Code field (DILP) 107
Billing Entity Minimum Charge Code field (IBIP) 214
billing overview 175
billing periods, non-standard 210
Billing Profile Code field (CUST) 142
Billing Profile Code field (ITAS) 236
Billing Terms (TERM) 122
Bond field (HOLD) 238
break type charge (CHAR) 179
Breakable Inventory field (HOLD) 238
Breakdown Number field (CNTY) 26
C
Capacity SKU Code field (LOCA) 65
CARR (Carriers) 320
Carrier / Consignee / Shipper Code field (DPME) 268
Carrier Block (CUST) 155
Carrier Type Code field (CARR) 322
Carriers (CARR) 320
Change Zero Pending Line to R-type Line field (DSRP) 117
CHAR (Charge Codes) 175
Character Position field (WARE) 38
Charge Code field
(IISP) 197
(IRSP) 205
Charge Definition field (CHAR) 179
Charge Initial and Renewal Storage field (DILP) 107
Charge on SKU Code field (CHAR) 180
Charge on SKU Code field (RATE) 187
charge on SKU code vs. qualify on SKU code, definition of
182
INDEX

INDEX
Charge Type Code field (CHAR) 177
Check Credit Limit field (DBIP) 129
City field (ZIPO) 32
CLAS (Class Codes) 252
CLAS (Freight Class Codes) 252
Class Codes (CLAS) 252
CNTY (Country Codes) 24
Code field (DEAS) 137
COMM (Commodity) 254
Command field (PRIN) 21
Command Type field (PRIN) 21
Commodity (COMM) 254
Commodity Code field (ITEM) 279
Compress Escape Sequence field (PRIN) 22
CONS (Consignees) 338
Consignees (CONS) 338
Consolidation Method for Allocated Lines field (CUST) 144
Contact field (TELE) 360
copying rates in RATE 191
Country Code field (ITEM) 285
country codes 24
Country Codes (CNTY) 24
Credit Limit field (DBIP) 129
Cross Dock field (ITEM) 282
CURR (Currency Codes) 160
Currency Code field (DBIP) 128
Currency Codes (CURR) 160
Current Number field (DONU) 18
CUSE (Customer Service Representatives) 73
CUST (Advanced) 152
CUST (Customer Setup) 139
Customer Code field
(CONS) 340
(DLVP) 97
(SHIP) 331
(SOLD) 349
Customer Service Representatives (CUSE) 73
Customer Setup (Advanced) 152
Customer Setup (CUST) 139
Cycle field (DIAP) 92
Cycle field (IRSP) 204
D
daily frequency (IRSP) 203
DAPR (Date Profile) 210
Date field (HOLD) 240
Date Format field (IIHO) 248
Date Formula field (IIHO) 248
Date Profile (DAPR) 210
Date Profile Code field (IBIP) 213
Date Used for Adjustments / Renewals field (ADJU) 314
DBIP (Depositor Billing Profile) 128
deactivated status 5
DEAS (Depositor Alternate Sorts) 137
Deassign Location field (DIFP) 80
Default Rate Charge Code field (CHAR) 181
Default SKU Adjustment Entry field (CUST) 145
Default SKU Order Entry field (CUST) 145
Default SKU Receipt Entry field (CUST) 145
Deferred Handling Inbound Percentage field (IINP) 194
DEME (Depositor Messages) 265
Depositor Alternate Sorts) 137
Depositor Billing Profile (DBIP) 128
Depositor Billing Rates (RATE) 185
Depositor Inventory Assign Profile (DIAP) 88
Depositor Inventory Level Profile (DILP) 101
Depositor Item Profile (DITP) 113
Depositor Item Profile Code field (CUST) 144
Depositor Level Validation Profile (DLVP) 95
Depositor Messages (DEME) 265
Depositor Print Messages (DPME) 267
Depositor Shipping and Receiving Profile (DSRP) 116
Depositor Workflow Profile (DIFP) 78
Description field
(ALIT) 358
(ITAS) 236
(SKCL) 11
DIAP (Depositor Inventory Assign Profile) 88
DIFP (Depositor Workflow Profile) 78
DILP (Depositor Inventory Level Profile) 101
Directed Picking field (LOTP) 56
Directed Put-Away field (LOTP) 55
Disabled EDI Send field (HOLD) 239
Discount Day field (IISP) 198
Discount Good for X Days field (TERM) 124
Discount Percentage field (IISP) 198
Discount Percentage field (TERM) 124
Discount Profile Code field (ITEM) 284
DITP (Depositor Item Profile) 113
DLVP (Depositor Level Validation Profile) 95
Document Code field
(ADJU) 313
(DIFP) 81
(DPME) 268
Document Numbers (DONU) 17
Document Types (DOTP) 10
DONU (Document Numbers) 17
DPME (Depositor Print Messages) 267
DRIV (Drivers) 351
Drivers (DRIV) 351
DSRP (Depositor Shipping and Receiving Profile) 116
E
EDI Profile Code field (CUST) 144
Effective Date field (RATE) 186
Effective Date for Charges field (ADJU) 313
Enable Location Aliases field (LOTP) 55, 67
End Number field (DONU) 18
Ending Number field (NUSE) 87
ending number in a number series (DONU) 17
Enter Charges field (ADJU) 313
Enter Expiry Dates field (ITSH) 219
Entry Required up to Level field (ITEM) 280
e-Vista field (HOLD) 239
Exact Length field (CNTY) 27
Exact Length field (DILP) 111
Exclude From Surcharge Calculations field (RATE) 187
expiry dates 217

INDEX
Expiry Selection Description field (ITSH) 219
Expiry Selection Formula (ITSH) 219
Expiry Selection Formula Format field (ITSH) 220
External Reference Number field
(CONS) 342
(CUST) 146
(SHIP) 332
(SOLD) 350
F
FIFO/LIFO parameters in PIPR, setting 115
Flat Rate field (RATE) 186
flat type charge (CHAR) 179
Flow Code field (DEME) 266
flow codes 75
Flow Process (FLPR) 75
flow profiles 78
FLPR (Flow Process) 75
Form Code field (DIFP) 81
Freight Class Codes (CLAS) 252
Freight Class field (COMM) 254
Freight Interface Type Code field (CARR) 322
Freight Paying Office Code field (CUST) 143
Freight Profile Code field (CUST) 144
Freight Type Code field (CARR) 322
Frequency Code field (DIAP) 92
Frequency Code field (IRSP) 203
G
G. L. Modifier Code field (CUST) 141
General Information Profile Code field (ITEM) 277
General Ledger Chart of Accounts (GLCH) 158
General Ledger Code field (CHAR) 179
General Ledger Modifier Codes (GLMO) 164
Generate UCC-128 Sequence Number field (CONS) 344
GLCH (General Ledger Chart of Accounts) 158
GLMO (General Ledger Modifier Codes) 164
global vs. unique programs 3
Gross Weight field (ITEM) 295
H
handling charges setup in IHAP 208
Handling Minimum Charge Code field (DILP) 107
Handling Minimum Charge Code field (IBIP) 214
Handling Profile Code field (IBIP) 213
HAZA (Hazardous Material Messages) 270
Hazard Code field (ITEM) 283
Hazardous Material Block (ITEM) 301
Hazardous Material Messages (HAZA) 270
Height field (ITEM) 295
HOLD (Hold Types) 237
Hold Code field (HOSP) 243
Hold Code field (LOCA) 64
Hold Profile Code field (ITEM) 279
hold profiles (IHOP) 244
Hold Ship Sequence Profile Code field (IHOP) 245
Hold Shipping Sequence Profile Code (HOSP) 241
Hold Types (HOLD) 237
HOLI (Holidays) 126
Holidays (HOLI) 126
HOSP (Hold Shipping Sequence Profile Code) 241
Hourly Rate field (DRIV) 352
I
IBIP (Item Billing Profile) 212
IHAP (Item Handling Profile) 208
IHOP (Item Hold Profile) 244
IIHO (Item Incubation Hold Code) 247
IIHP (Incubation Hold Profile) 250
IINP (Item Information Profile) 194
IISP (Item Initial Storage Profile) 196
ILOP (Item Location Profile) 256
Inbound Charge Code field (IHAP) 209
inbound handling charges (IHAP) 209
Inbound Hold Code field (IHOP) 244
Include Day on Renewals fields (DBIP) 130
Incubation Hold Code field (IIHO) 248
Incubation Hold Profile (IIHP) 250
IND invoicing 128
Initial Storage Minimum Charge Code field (DILP) 107
Initial Storage Minimum Charge Code field (IBIP) 214
Initial Storage Profile Code field (IBIP) 213
installment invoicing in TERM 123
Installment Number field (TERM) 123
INTE (Inventory Terminology) 99
INTP (Invoice Types) 173
Inventory Level Profile Code field (CUST) 143
inventory level profiles 101
Inventory Look-Up field (ADIM) 273
Inventory Messages (ADIM) 272
Inventory Terminology (INTE) 99
Inventory Terminology Code field (DILP) 103
Invoice Due After X Days field (TERM) 124
Invoice Printing Profile Code field (TERM) 133
Invoice Report Process field (IQBP) 229
Invoice Type Code field (CHAR) 179
Invoice Types (INTP) 173
invoicing, overview 133
IPRP (Item Process Profile) 224
IQBP (Item Quantity Breakdown Profile) 226
IRSP (Item Renewal Storage Profile) 201
ISOL (Isolators) 46
Isolator Code field (ILOP) 257
Isolators (ISOL) 46
ITAP (Item Tare Profile) 258
ITAS Item Alternate Sorts) 233
ITEM (Item) 276
Item (ITEM) 276
Item Alternate Sorts (ITAS) 233
Item Billing Profile (IBIP) 212
Item Billing Profile Code 1 field (ITEM) 278
Item Code field (DLVP) 97
Item Discount Flag field (ITEM) 284
Item Handling Profile (IHAP) 208
Item Hold Profile (IHOP) 244
Item Incubation Hold Code (IIHO) 247
Item Information Profile (IINP) 194
Item Initial Storage Profile (IISP) 196

INDEX
Item Location Profile (ILOP) 256
Item Location Profile Code field (CONS) 342
Item Location Profile Code field (SHIP) 332
Item Minimum Shipping Level Flag field (DILP) 104
Item Process Profile (IPRP) 224
item profile (DITP) 113
Item Quantity Breakdown Profile (IQBP) 226
Item Renewal Storage Profile (IRSP) 201
Item Shipping Profile (ITSH) 217
Item Tare Profile (ITAP) 258
Item Value field (ITEM) 282
Item Value Profile Code field (ITEM) 286
ITSH (Item Shipping Profile) 217
L
LANG (Language Code) 353
Language Code (LANG) 353
Language Code field
(ALIT) 357
(CONS) 340
(SOLD) 349
Layer Configuration Required field (IQBP) 230
LDAN (Load Analysis) 327
Length field (ITEM) 295
Length of Partition field (CNTY) 27
Length of Partition field (DILP) 110
Level Code field (DLVP) 96
level validation (DLVP) 95
Level Verify Profile Code field (DILP) 106
License Number (DRIV) 352
Linear Measurement Code field (ITEM) 295
LOAD (Load Type) 315
Load Analysis (LDAN) 327
Load Analysis Code field (CONS) 341
Load Analysis Code field (SHIP) 331
Load Type (LOAD) 315
LOCA (Locations) 59
location aliases 66
Location Attributes Block (WARE) 42
Location Bill Code field (IISP) 197
Location Bill Code field (IRSP) 205
Location Bill Code field (LOCA) 61
Location Billing Codes (LODE) 43
Location Print Profile (LPPR) 51
Location Profile Code field (ITEM) 279
Location Size Code field (ITEM) 284
Location Structure Type Code field (LOCA) 63
Location Types (LOTP) 53
Locations (LOCA) 59
LODE (Location Billing Codes) 43
lot numbers, auto-generation of 88
LOTP (Location Types) 53
LPPR (Location Print Profile) 51
M
management reporting, unit of measurement for 194
Mandatory field (DIFP) 80
Master Consignee field (CONS) 342
Master Location for Weight field (LOCA) 63
Master Shipper field (SHIP) 333
Maximum Capacity field (LOCA) 65
Maximum Charge field (RATE) 187
Merge Inventory to Location on Replenishment and RFRL 
field (ITEM) 287
MESS (Messages) 264
Message Code field
(ADIM) 272
(DEME) 266
(DPME) 268
(ITEM) 284
Messages (MESS) 264
Method of Generating/Validating Values field (DILP) 105
Minimum Charge field (RATE) 187
Minimum Quantity field (ITEM) 293
Minimum/Maximum Accessorial Charge Code field (DBIP)
134
Minimum/Maximum Receipt Charge Code field (DBIP) 134
Minimum/Maximum Renewal Charge Code field (DBIP)
134
monthly first of month frequency (IRSP) 203
monthly last of month frequency (IRSP) 203
multiple type charge (CHAR) 178
N
Net Weight field (ITEM) 295
no charge type charge code (CHAR) 8
non-standard weight options 305
Number of Breaks field (ITAP) 260
Number of Breaks field (RATE) 187
Number of Day field (IIHO) 248
Number of Days field (HOLD) 239
Number of Days for Open Lots field (ITEM) 280
Number of Flat Rate Breaks field (RATE) 186
Number of Layers field (ITEM) 294
Number of Temperatures field (LOAD) 316
Number Series (NUSE) 86
Number to Reserve field (NUSE) 87
Number valid for field (DIAP) 92
number valid for options (DIAP) 89
NUSE (Number Series) 86
O
optional printing 82
Order Entry field (ADIM) 273
Original / Current Rate on Renewals field (IBIP) 214
Original or Current Rate on Renewals field (DBIP) 131
outbound handling charges (IHAP) 209
Outbound Hold Code field (IHOP) 245
Overflow Location Code field (ILOP) 257
Overflow Warehouse Code field (ILOP) 257
P
Pad field (DIAP) 93
Parent Language Code field (LANG) 354
Partition Number field (CNTY) 26
Partition Number field (DILP) 110
Paying Office Code field (CUST) 142
pending lines with zero quantity 117

INDEX
Percentage field (DRIV) 352
Percentage of Invoice field (TERM) 123
Period Number field (IRSP) 203
Picking Profile (PIPR) 115
Picking Profile Code field
(CONS) 341
(DSRP) 118
(ITEM) 283
PIPR (Picking Profile) 115
Point at Which Values Generated field (DILP) 106
Position field (TELE) 360
postal codes, defining the format of 24
Prefix Date Format field (DIAP) 93
Prefix field (DIAP) 93
Prefix field (DONU) 18
PRIN (Printer Code) 20
Print Profile Code field (PRIN) 22
Printer Code (PRIN) 20
Printer Size field (PRIN) 21
Process Profile Code field (ITEM) 279
product lines, billing by 235
profiles, using 3
Prorate field (IISP) 198
Put-Away Profile Code field (DSRP) 118
Put-Away Profile Code field (ITEM) 285
Q
Qualifier Code field (IQBP) 227
Qualifier Code field (SKUS) 13
Qualify on SKU Code field (CHAR) 180
qualify on SKU code vs. charge on SKU code, definition of
182
Quantity Breakdown Block (ITEM) 291
Quantity Breakdown Profile Code field (ITEM) 279
quantity breakdown, definition of 226
Quantity field (ITEM) 292
Quantity Odd Layer field (ITEM) 294
Quantity Per Layer field (ITEM) 294
quarantine zones see Isolators
R
RATE (Depositor Billing Rates) 185
Rate Qualifier field (DBIP) 132
Rate Qualifier field (IBIP) 214
Rate Receipt Automatically field (DBIP) 133
Realized Exchange G. L. Account field (CURR) 161
Receipt Entry field (ADIM) 273
Receipt Process field (IQBP) 228
Receiving Block (CUST) 152
Record Linear Measure Code field (DITP) 113
Record Weight Measure Code field (DITP) 113
Reference 1/2 field (SOLD) 349
Reference field (CHAR) 177
REGR (Revenue Group Codes) 169
regular printing (DIFP) 82
Renew field (HOLD) 238
Renew on Day field (DBIP) 130
Renewal Options for Variable Quantity Breakdown field 
(ITEM) 281
Renewal Storage Line Minimum Charge Code field (DILP)
107
Renewal Storage Line Minimum Charge Code field (IBIP)
214
Renewal Storage Profile Code field (IBIP) 213
Report Process field (IQBP) 229
Reporting Block (CUST) 153
Reserve for Partial Pallet field (LOTP) 56
Reserve Orders at Level Number field (CUST) 143
Reset Date field (IRSP) 204
Reset Escape Sequence field (PRIN) 22
Restrict field (DLVP) 97
Retail Profiles (RETP) 336
RETP (Retail Profiles) 336
REVA (Revenue Analysis Codes) 171
Revenue Analysis Code field (CHAR) 179
Revenue Analysis Codes (REVA) 171
Revenue Group Code field (REVA) 172
Revenue Group Codes (REGR) 169
RF Company Prefix field (CUST) 146
RF Partition field (CUST) 146
RF Profile Code field (CUST) 146
Rounding Code field (IQBP) 231
Rounding Flag field (CHAR) 180
Rounding Method for Number of Labels field (CARR) 323
Rounding Method for Number of Labels field (CONS) 344
S
Salespersons (SAPE) 72
SAPE (Salespersons) 72
Scan Parameter Code field (ITEM) 284
Scan Parameter Code for Inventory Validation (SCPR) field 
(ITEM) 286
Send Invoices To field (DBIP) 132
Send via EDI field (ADJU) 314
Sequence field (DIFP) 80, 81
Sequence field (LOTP) 55
Sequence Number field (HOSP) 242
Sequential Entry field (DILP) 104
Shelf Life Duration field (ITSH) 220
Shelf Life Frequency field (ITSH) 220
SHIP (Shippers) 328
Ship by Weight field (ITSH) 220
Ship by Weight Rounding Method field (ITSH) 221
Ship field (HOLD) 238
Shipment Process field (IQBP) 228
Shipper Type field (SHIP) 331
Shippers (SHIP) 328
Shipping Block (CUST) 153
Shipping Profile Code field (ITEM) 278
Shipping/Receiving Profile Code field (CUST) 143
Short Description field (SKCL) 11
short shipping See Change Zero Pending Line to RType Line field (DSRP)
single type charge (CHAR) 177
SKCL (SKU Class) 10
SKU Class (SKCL) 10
SKU Class Description field (SKUS) 14
SKU Class for Number of Labels field (CARR) 323

INDEX
SKU Class for Number of Labels field (CONS) 344
SKU Code field
(IQBP) 228
(ITEM) 292
SKU codes, overview 12
SKUS (Stock Keeping Units) 12
SOLD (Sold-To Codes) 347
Sold-To Codes (SOLD) 347
Special Verification Block (DIFP) 82
Stackability Indicator Code field (ITEM) 286
Stackablility Quantity in Highest SKU field (ITEM) 286
Staging field (LOTP) 56
Standard Carrier Alpha Code field (CARR) 321
Standard Weight field (ITEM) 282
Start Business Date field (CUST) 141
Start Number field (DONU) 18
Starting Date field (DAPR) 211
starting dates for billing periods, setting 210
Starting Number field (NUSE) 87
starting/ending numbers in a number series (DONU) 17
State or Province field (ZIPO) 32
States/Provinces (STPR) 29
Status field
(CUST) 147
(ITEM) 287
(LOCA) 66
status of codes and profiles 5
Stock Keeping Units (SKUS) 12
STPR (States/Provinces) 29
Subcode field (COMM) 254
Substitution Modifier field (GLMO) 167
Suffix field (DIAP) 93
Suffix field (DONU) 19
Suppress Inventory Merge to Location field (LOTP) 55
System Printer field (PRIN) 20
T
Tare field (ITAP) 260
Tare Profile Code field (ITEM) 282
Tare Weight field (ITEM) 296
Tax Code field (CHAR) 181
Tax Code field (DBIP)) 133
Tax Code field (ITEM) 284
Tax Code Override Flag field (CHAR) 182
TELE (Telephone Numbers) 359
Telephone Block
(CARR) 326
(CONS) 346
(CUST) 154
(SHIP) 335
Telephone List Types (TETP) 121
Telephone Numbers (TELE) 359
TERM (Billing Terms) 122
Term Code field (TERM) 129
TETP (Telephone List Types) 121
Text Block field (COMM) 255
Threshold Accessorial Charge Code field (DBIP) 134
time-stamping receipts and orders 75
Total Cube field (ITEM) 295
Track Last Used for Put-Away field (LOCA) 65
Trade G. L. Account field (CURR) 161
Transfer Profile Code field (CUST) 146
Transport Mode Block (ITEM) 301
Transport Mode Code field (CARR) 323
Transport Mode Codes (TRMO) 318
Transport Mode Type field (TRMO) 319
TRMO (Transport Mode Codes) 318
True Revenue field (REVA) 172
Type field (DIFP) 82
U
UALL invoicing 128
Unique Level for Pallet ID field (CUST) 147
unique vs. global programs 3
UPC field (ITEM) 285
UPC Prefix field (CUST) 143
updated status 5
UREN invoicing 128
Use Substitute Item Codes field (ITSH) 219
V
Valid Characters field (CNTY) 27
Valid Characters field (DILP) 111
Valid Characters field (WARE) 39
validating lot numbers (DLVP) 95
Value field
(ITAP) 260
(SKUS) 14
Value to Base Currency field (CURR) 160
Variable Quantity Breakdown field (ITEM) 280
Volume field (ITEM) 294
Volume Measure Code field (ITEM) 294
W
WARE (Warehouse & Location Format) 36
Warehouse & Location Format (WARE) 36
Warehouse Code field
(CUST) 146
(ITEM) 279
Warehouse Restriction Flag field (DSRP) 119
weekly as of Monday frequency (IRSP) 203
Weight Limit field (LOCA) 62
Weight Measure Code field (ITAP) 260
Weight Measure Code field (ITEM) 295
Weight Measure Code field (LOCA) 62
Weight Measure field (CARR) 322
Weight Measure for Receipts Code field (SHIP) 331
weight options, non-standard 305
weight, allocation by 220
Whole/Prorate field (ITEM) 293
Whse field (DIAP) 93
Width field (ITEM) 295
wildcard characters for general ledger chart of accounts
165
Workflow Profile Code field
(CONS) 341
(CUST) 143
(SHIP) 332

INDEX
Z
zero pending lines 117
ZIP codes, defining the format of 24
ZIP/Postal Codes (ZIPO) 31
ZIPO (ZIP/Postal Codes) 31

INDEX
