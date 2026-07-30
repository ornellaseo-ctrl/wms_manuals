# Manual A — Billing and Invoicing Guide (Faturamento e Cobrança)

> **ID do Manual:** A  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Sistema completo de billing 3PL: receipt charges, renewal charges, accessorial charges. Setup de tarifas (RATE/CHAR), invoice register (INRE), extra charges (GEXC), invoicing cycles (BILB/BACO), credit invoices, cash posting (CHPO/ARCP), surcharges, taxes, open lots, cost tracking.

---

AccellosOne Enterprise 
3PL Billing and Invoicing 
Guide (Classic)
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

BILLING AND INVOICING GUIDE 4.2 iii
TABLE OF CONTENTS
INTRODUCTION.......................................................................... 1
Welcome ........................................................................................................................................... 2
Related Reading............................................................................................................................... 2
AccellosOne 3PL Documentation Set ............................................................................................ 2
BASICS ..................................................................................... 5
Billing and Invoicing Overview....................................................................................................... 6
Receipt Charges.................................................................................................................. 6
Renewal Charges ................................................................................................................ 6
Accessorial Charges............................................................................................................ 6
Types of Invoicing............................................................................................................................ 7
Overview of Billing/Invoicing Cycle ............................................................................................... 8
BASIC BILLING SETUP ............................................................... 9
Billing Setup ................................................................................................................................... 10
Setting Up the Invoice Register Defintion (INRE).............................................................. 12
Setting Up Additional Invoice Types ................................................................... 15
Working With Maximum and Minimum Charges......................................................................... 16
Default Maximum/Minimum Charges ................................................................................ 17
Item-Specific Maximum/Minimum Charges ....................................................................... 18
Minimum Charges for a Given Invoice .............................................................................. 20
Maximum/Minimum Charges for Billing Entities ................................................................ 22
Minimum Charges for a Given Receipt/Order ................................................................... 23
Setting Up Maximum/Minimum Charge Codes.................................................................. 24
Monthly Minimum Billing.................................................................................................... 27
Working With Charge Groups....................................................................................................... 28
Changing Your Rates..................................................................................................................... 30
Entering a Rate Change .................................................................................................... 31
Cancelling a Rate Change................................................................................................. 32
Changing Your Rates by a Fixed Percentage in IDRA...................................................... 32
Cancelling an IDRA Rate Change ..................................................................................... 34
Working With Renewal Storage .................................................................................................... 34
Maximum Daily Billing ....................................................................................................... 34
Setting Up Maximum Daily Billing ....................................................................... 35
Check-In Only Billing ......................................................................................................... 35
Setting Up Check-In Only Billing ......................................................................... 35

iv 4.2 BILLING AND INVOICING GUIDE
Daily Average Billing.......................................................................................................... 36
Setting Up Daily Average Billing ......................................................................... 36
Exceed Daily Average Billing .............................................................................. 40
Total Exceed Daily Average Billing ..................................................................... 41
Daily Average Billing Based on Number of Pallet Positions................................ 42
Single Level Billing ............................................................................................................ 43
Monthly Renewal Invoicing................................................................................................ 43
Renewal Invoicing by Receipt ........................................................................................... 44
Renewal Invoicing by OPID............................................................................................... 45
Looking Up Renewal Storage Information......................................................................... 46
Running the Renewal Preprocessor (RENW) On Demand ............................................... 47
Changing Renewal Storage Rates................................................................................................ 48
Changing Renewal Original Rates for Existing Inventory in ADBD ................................... 48
Adjusting Billing Data in ADBD.......................................................................................... 50
EXTRA CHARGE RATER .............................................................53
Overview ......................................................................................................................................... 54
General Extra Charges...................................................................................................... 54
Specific Extra Charges ...................................................................................................... 54
Understanding the Charge Per Options....................................................................................... 55
COD (Cash on Delivery) — can only be attached to CUST .............................................. 55
DHOC (Document Header for Occurrence) — can only be attached to CUST ................. 55
DOCH (Document Header) — can only be attached to CUST.......................................... 56
DOCL (Document Line) ..................................................................................................... 56
DOCT (Document Total) — can only be attached to CUST .............................................. 57
ICTL (Initial Charge Total) — can only be attached to CUST............................................ 57
IHTL (Initial Handling Total) — can only be attached to CUST ......................................... 57
ISTL (Initial Storage Total) — can only be attached to CUST ........................................... 57
ITCT (Item Count) — can only be attached to CUST ........................................................ 57
LCNT (Document Line Count) — can only be attached to CUST...................................... 57
LTCT (Lot Count)............................................................................................................... 58
ULV1 (Unique Level 1) ...................................................................................................... 58
ULV2 (Unique Level 2) ...................................................................................................... 58
ULV3 (Unique Level 3) ...................................................................................................... 58
ULV4 (Unique Level 4) ...................................................................................................... 58
SLV2 (Single Level 2)........................................................................................................ 59
SLV3 (Single Level 3)........................................................................................................ 59
SLV4 (Single Level 4)........................................................................................................ 59
Assigning Location Billing Codes to Inbound Extra Charges................................................... 59
DOCL (Document Line) ..................................................................................................... 59
Specifying Extra Charge Restrictions.......................................................................................... 60

BILLING AND INVOICING GUIDE 4.2 v
Charging for Partial Quantities of Unit-Based SKU’s ................................................................. 62
Ignore Last Quantity .......................................................................................................... 64
Setting Up an Extra Charge for Case Partials ................................................................... 64
Setting Up an Extra Charge for Case Partials and Each Partials...................................... 65
Setting Up an Extra Charge for Non-Partial Quantities ..................................................... 65
Setting Up General Extra Charges in GEXC................................................................................ 65
Procedure .......................................................................................................................... 68
Setting Up Specific Extra Charges in ECHP................................................................................ 70
Procedure .......................................................................................................................... 79
Charging by Physical Pallet.......................................................................................................... 81
Third Party Billing in ECHP........................................................................................................... 82
Activating Extra Charges for EDI.................................................................................................. 83
Confirming an Extra Charge ......................................................................................................... 84
BILLING SETUP — ADVANCED TOPICS ........................................87
Combination Type Charges........................................................................................................... 88
Setting Up Combination Type Charges ............................................................................. 89
Third Party Billing .......................................................................................................................... 90
Third Party Billing on a Receipt-by-Receipt Basis ............................................................. 90
Creating an Accessorial Charge........................................................................................ 90
Setting Up an Invoice Only Customer ............................................................................... 90
Billing Subscription ............................................................................................................ 91
Alternate Billing Groups................................................................................................................ 93
Load Type Charges........................................................................................................................ 94
Open Lot Receipts ......................................................................................................................... 96
Setting Up Open Lots in ITEM........................................................................................... 96
Entering an Open Lot in ENRE.......................................................................................... 97
Closing an Open Lot in CLOL............................................................................................ 99
Overriding Generated Charges on a Receipt ............................................................................ 100
Seasonal or Special Billing ......................................................................................................... 101
Taxes ............................................................................................................................................. 102
Billing by Multiple Units of a SKU .............................................................................................. 103
Discounts on Initial Storage and Handling Charges ................................................................ 104
Setting Up Your Discount Profile Code in DPRO ............................................................ 104
Setting Up Your Item in ITEM.......................................................................................... 105
Selecting Your Discount Profile Code During Receipt Confirmation ............................... 107
Cross-Dock Billing....................................................................................................................... 108
Setting Up Cross-Dock Billing ......................................................................................... 108

vi 4.2 BILLING AND INVOICING GUIDE
Entering a Cross-Dock Receipt ....................................................................................... 112
Rating a Cross-Dock Receipt .......................................................................................... 113
Surcharges ....................................................................................................................................113
Working with Multiple Surcharges ................................................................................... 114
Setting Up Surcharges .................................................................................................... 114
Using Surcharges to Calculate Taxes ............................................................................. 117
Density Rating...............................................................................................................................118
Setting Up Density Charges ............................................................................................ 118
Flat Rate Charges ........................................................................................................................ 120
Hourly Based Charges ................................................................................................................ 121
Customer Fixed Charges ............................................................................................................ 123
Multi-Currency Billing.................................................................................................................. 124
Billing Batch Automation ............................................................................................................ 126
Automatic Pre-Renewal Billing................................................................................................... 127
INVOICING ............................................................................. 131
IND Invoicing ................................................................................................................................ 132
Quick Steps ..................................................................................................................... 133
Detailed Steps ................................................................................................................. 133
IND Invoicing With Extra Charges on a Warehouse Receipt ................................................... 133
Quick Steps ..................................................................................................................... 134
Detailed Steps ................................................................................................................. 135
UALL Invoicing............................................................................................................................. 135
Quick Steps ..................................................................................................................... 136
Detailed Steps ................................................................................................................. 137
UREC Invoicing ............................................................................................................................ 137
Quick Steps ..................................................................................................................... 138
Detailed Steps ................................................................................................................. 139
UREN Invoicing ............................................................................................................................ 139
Quick Steps ..................................................................................................................... 140
Detailed Steps ................................................................................................................. 141
UREN Invoicing With Extra Charges on a Warehouse Receipt ............................................... 141
Quick Steps ..................................................................................................................... 142
Detailed Steps ................................................................................................................. 142
Generating and Printing the Warehouse Receipt Invoice ........................................................ 142
Generating and Printing the Accessorial Batch/Invoice .......................................................... 144
Generating the Accessorial Batch in BILB....................................................................... 144
Printing the Accessorial Audit.......................................................................................... 148
Confirming the Batch and Printing the Accessorial Invoice ............................................. 149

BILLING AND INVOICING GUIDE 4.2 vii
Generating and Printing the Renewal Batch/Invoice................................................................ 150
Before You Begin ............................................................................................................ 150
Generating a Renewal Batch in BILB .............................................................................. 151
Printing the Renewal Audit .............................................................................................. 153
Confirming the Batch and Printing the Renewal Invoice ................................................. 155
Generating and Printing the Extra Charge Batch ..................................................................... 155
Generating an Extra Charge Batch in BILB..................................................................... 156
Printing the Extra Charge Audit ....................................................................................... 158
Confirming the Batch and Printing to VIEW the Extra Charge Invoice ............................ 159
Troubleshooting Extra Charges....................................................................................... 160
Working With Audit Batch Restrictions ..................................................................................... 160
Reprinting an Audit Batch................................................................................................ 162
Running the Daily Invoice Register............................................................................................ 163
Printing the Daily Invoice Register Audit ......................................................................... 164
Confirming the Batch and Printing the Daily Invoice Register ......................................... 166
Reprocessing the Financial Interface .............................................................................. 167
Emailing of Invoices......................................................................................................... 168
Working With Batches and Invoices .......................................................................................... 168
Regenerating a Batch...................................................................................................... 169
Reprinting an Invoice....................................................................................................... 169
Deleting a Batch .............................................................................................................. 169
Looking Up a Charge on a Batch .................................................................................... 169
Deleting and Modifying Charges on a Confirmed Batch.................................................. 171
Deleting a Charge............................................................................................................ 171
Modifying a Charge ......................................................................................................... 172
Troubleshooting Renewal Invoicing................................................................................. 172
Looking Up an Invoice in LOIN........................................................................................ 173
Printing an Invoice in LOIN.............................................................................................. 174
Looking Up All Charges for a Given Item, Level 2/3/4 Value in LOAC............................ 175
Using Invoice Types to Split Out Accessorial Charges ................................................... 178
Backdating Open Orders and Receipts ........................................................................... 178
Entering Accessorial Bill Later Charges.................................................................................... 180
Entering Receipt Accessorial Charges ............................................................................ 180
Entering Receipt Extra Charges ...................................................................................... 183
Entering Order Accessorial Charges ............................................................................... 186
Entering Accessorial Charges in ENAC .......................................................................... 190
Adding Accessorial Charges to a Confirmed Order in OEXC.......................................... 192
Adding Accessorial or Receipt Extra Charges to a Confirmed Receipt in REXC ............ 194
Entering a Credit in ENAC............................................................................................... 196
Entering a Customer Department in ENAC ..................................................................... 198
Working With Accessorial Bill Immediately Charges............................................................... 198

viii 4.2 BILLING AND INVOICING GUIDE
Entering Your Charges in ENIN....................................................................................... 198
Entering a Credit in ENIN ................................................................................................ 201
Generating an Immediate Accessorial Batch .................................................................. 203
Printing the Immediate Accessorial Audit ........................................................................ 206
Confirming the Batch and Printing the Immediate Accessorial Invoice ........................... 207
Adding Charges to a Confirmed Receipt................................................................................... 208
Deleting a Charge............................................................................................................ 210
Adding Charges to a Confirmed Order ...................................................................................... 210
Deleting a Charge............................................................................................................ 212
Rollup Invoicing ........................................................................................................................... 212
Setting Up Rollup Invoicing ............................................................................................. 214
Setting Up Your Rollup Company.................................................................................... 214
Setting Up Your Child Companies .................................................................... 214
Attaching Your Child Companies to the Rollup Company ............................................... 215
Setting Up Your Customers............................................................................................. 216
Generating and Printing Rollup Invoices........................................................... 216
Billing Audit System .................................................................................................................... 216
Setting Up the Billing Audit System ................................................................................. 217
Activating the Billing Audit System .................................................................................. 217
Setting Up Your Reason Codes in REAS........................................................................ 218
Changing and Deleting Charges ..................................................................................... 219
Changing and Deleting Charges in ENAC....................................................................... 219
Changing and Deleting Charges in ENIN ........................................................................ 220
Tracking Changes to ENAC and ENIN Charges ............................................................. 221
Looking Up Changes in ACAL......................................................................................... 222
Running the Accessorial Charge Changes Report (ACCA)............................................. 222
Authorizing Your Charges ............................................................................................... 223
Running the Accessorial Charges Authorization Audit (OAUD) ...................................... 224
Authorizing the Charges in ACAU ................................................................................... 225
Purging Change Records in PACA.................................................................................. 226
Invoicing by Warehouse.............................................................................................................. 227
Activating Invoicing by Warehouse in COMP .................................................................. 228
Assigning Your Location Billing Codes to Warehouses in LODE .................................... 229
Setting Up Your Address Option in DOCU ...................................................................... 231
Entering Receipts and Orders in ENRE/ENOR ............................................................... 232
Entering Batch Restrictions in BILB................................................................................. 233
Entering Charges in ENAC/ENIN .................................................................................... 234
Invoicing by Inventory Level....................................................................................................... 234
Reversing Charges on Confirmed Invoices............................................................................... 236
Canceling the Reversal of a Charge................................................................................ 237
Allocating Costs to an Invoice.................................................................................................... 237

BILLING AND INVOICING GUIDE 4.2 ix
CASH POSTING SYSTEM .......................................................... 239
Overview ....................................................................................................................................... 240
Setting Up Your Bank in BANK................................................................................................... 240
Setting Up Customer Cross References in CUCR .................................................................... 241
Removing a Cross Reference ......................................................................................... 242
Entering a Payment in ARCP ...................................................................................................... 243
Deleting a Payment ......................................................................................................... 245
Removing an Invoice from a Payment............................................................................. 245
Understanding the Check, Posted and Remaining Amounts .......................................... 246
Looking Up Summary Information ................................................................................... 247
Posting a Payment in CHPO ....................................................................................................... 247
Removing Payments from a Batch .................................................................................. 249
Deleting a Batch .............................................................................................................. 250
Closing a Batch ............................................................................................................... 250
Printing the Batch Audit ................................................................................................... 251
Reports.......................................................................................................................................... 251
REPORTS AND REFERENCE ...................................................... 253
Reports.......................................................................................................................................... 254
BILB (Accessorial Invoicing) ...................................................................................................... 254
BILB (Renewal Invoicing)............................................................................................................ 256
BILB (Immediate Invoice Invoicing) ........................................................................................... 258
ENAC (Bill Later - Enter Charges) .............................................................................................. 260
ENIN (Enter Immediate Invoice).................................................................................................. 264
BILB (Extra Charge Invoicing) .................................................................................................... 266
ADBD (Adjust Billing Data) ......................................................................................................... 268
LOIN (Look Up Invoices) ............................................................................................................. 271
LOAC (Look Up Accessorial)...................................................................................................... 272
Troubleshooting Billing and Invoicing....................................................................................... 276
The renewal dates or quantities in the Renewal Block of LOEN are wrong .................... 276
The rates shown on my invoice are wrong ...................................................................... 276
The charges are wrong (weight-based billing only) ......................................................... 276
There are missing charges on my audit report or invoice................................................ 277
No charges generated for a confirmed receipt ................................................................ 277
INDEX .................................................................................... 279

x 4.2 BILLING AND INVOICING GUIDE

BILLING AND INVOICING GUIDE 4.2 1
INTRODUCTION
Welcome .............................................................................................................. 2
Related Reading .................................................................................................. 2
AccellosOne 3PL Documentation Set ............................................................... 2

INTRODUCTION
Welcome
Welcome
Welcome to the Billing and Invoicing Guide, the complete reference guide to the billing and invoicing 
programs of AccellosOne 3PL. Designed for intermediate and advanced users of AccellosOne 3PL, this 
manual has been divided into four parts. 
Basics is essential reading for all users of this manual. It describes the types of charges and invoicing in 
AccellosOne 3PL and provides an overview of the billing/invoicing cycle.
Billing is a high-level look at billing issues. It is intended for advanced users who need to understand how 
charges are calculated in AccellosOne 3PL so that they can set up charge codes and profiles correctly to 
ensure that customers receive accurate and complete invoices.
Invoicing is intended for intermediate users who need a thorough knowledge of invoicing to do their job, but 
do not set up charge codes or billing profiles or need to understand how charges are calculated in AccellosOne 3PL. The information in this section does not require a knowledge of the high-level billing issues 
discussed in Part II.
Reference provides a listing of common billing and invoicing reports as well as field-by-field descriptions of all 
billing and invoicing programs. It can be referred to by users at any level on an as-required basis.
Related Reading
This manual does not include setup procedures for the various AccellosOne 3PL billing setup programs such 
as CHAR, RATE, IISP, IRSP, etc. Refer to the Setup Guide for detailed instructions on these programs.
Refer to the Core Documents Guide for samples of various billing related documents such as the accessorial 
audit and accessorial invoice.
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

INTRODUCTION
AccellosOne 3PL Documentation Set
BILLING AND INVOICING GUIDE 4.2 3
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

INTRODUCTION
AccellosOne 3PL Documentation Set

BILLING AND INVOICING GUIDE 4.2 5
BASICS
Billing and Invoicing Overview .......................................................................... 6
Types of Invoicing............................................................................................... 7
Overview of Billing/Invoicing Cycle .................................................................. 8

BASICS
Billing and Invoicing Overview
Billing and Invoicing Overview
There are essentially three types of charges in AccellosOne 3PL:
 receipt charges
 renewal charges
 accessorial charges
RECEIPT CHARGES
Receipt charges are any charges that are incurred when product is received in the warehouse. Receipt 
charges come in two forms: automatic charges and manual charges.
Automatic receipt charges are set up in IISP (Initial Storage Profile) and IHAP (Item Handling Profile). They 
can also be set up in ECHP (Extra Charge Profile). Manual receipt charges are entered in the Header Block 
of ENRE by setting the Receipt Extra Charge flag to Yes. 
Receipt charges accumulate in ENAC (Enter Charges - Bill Later) and can be invoiced once the receipt has 
been confirmed. 
RENEWAL CHARGES
Renewal charges are any charges that are incurred after the product has been received in the warehouse 
and any receipt charges calculated. There are no manual renewal charges. You set up automatic renewal 
charges in IRSP (Item Renewal Storage Profile). 
Renewal charges must be generated in a batch program. Once generated, they accumulate in ENAC (Enter 
Charges - Bill Later).
ACCESSORIAL CHARGES
Accessorial charges are any charges that you enter through the program ENAC (Enter Charges - Bill Later). 
Manual accessorial charges can be entered directly into ENAC or can be entered at either the header or line 
detail level in ENRE (Enter Receipts) or ENOR (Enter Orders). Automatic accessorial charges are set up in 
GEXC (General Extra Charges) and ECHP (Extra Charge Profile).
You use accessorial charges to bill for miscellaneous type charges such as a charge for blast freezing, palletization, a bill of lading, etc. that apply to a specific receipt or order. You can also use accessorial charges to 
bill for general or one-time miscellaneous charges that are not attached to a particular order or receipt; for 
example, rent, overtime, faxing and long distance charges.

BASICS
Types of Invoicing
BILLING AND INVOICING GUIDE 4.2 7
Types of Invoicing
There are four possible invoicing options available in AccellosOne 3PL for any given customer. The invoicing 
option that you choose determines the type of charges that will appear on an invoice. 
You define your invoicing options for a customer in the Invoice Printing Profile Code field in DBIP (Depositor 
Billing Profile). If you wish to invoice differently for certain customers, you must set up multiple depositor 
billing profiles in DBIP and then attach them to the appropriate customers.

Billing Profile STD in DBIP showing IND invoicing
IND three invoice types
 a warehouse receipt invoice containing receipt charges such as initial storage/handling and extra charges
 an accessorial invoice containing accessorial charges such as receipt/order 
accessorial charges and extra charges set up in GEXC and ECHP
 a renewal invoice containing renewal storage charges 
UALL an accessorial invoice containing all charges
UREC two invoice types
 an accessorial invoice containing receipt charges and accessorial charges
 a renewal invoice containing renewal storage charges 
UREN two invoice types
 a warehouse receipt invoice containing receipt charges
 an accessorial invoice containing accessorial charges and renewal storage 
charges

BASICS
Overview of Billing/Invoicing Cycle
Overview of Billing/Invoicing Cycle
There are seven basic steps in the billing/invoicing cycle.
BILB
ENAC
BILB
You generate your batch in BILB.
You print your audit report in BILB.
If required, you edit your charges.
You confirm your batch and print your invoice in 
BILB. 
You run the daily invoice register. This program 
posts the various charges to your management 
and sales reports. If your accounting software is 
linked to AccellosOne Enterprise 3PL, the daily 
invoice register will create your general ledger 
interface file.
CHRF, CHOF, 
RCRA
When you confirm a receipt in CHRF or confirm 
an order in CHOF, all charges — both automatic 
and manual — are generated. If you use the 
receipt rater program, receipt charges are 
generated when you run RCRA. 
BILB
BILB
ENRE, ENOR
You add any extra or accessorial charges to a 
receipt in ENRE or to an order in ENOR.

BILLING AND INVOICING GUIDE 4.2 9
BASIC BILLING SETUP
Billing Setup ...................................................................................................... 10
Working With Maximum and Minimum Charges............................................ 16
Working With Charge Groups.......................................................................... 28
Changing Your Rates........................................................................................ 30
Working With Renewal Storage ....................................................................... 34
Changing Renewal Storage Rates................................................................... 48

BASIC BILLING SETUP
Billing Setup
Billing Setup
AccellosOne 3PL uses charge codes to generate charges in the billing system. Charge codes are set up in 
CHAR (Charge Code) and RATE (Depositor Billing Rates). If there is no charge for a particular type of storage 
(for example, you have no receipt charges for inbound product), you can use a “No Charge” type charge 
code.
Charge codes are attached to profiles and it is by means of these profiles that most charges are generated.
There are eight mandatory setup programs in AccellosOne 3PL for billing and invoicing:
DILP (Depositor Inventory Level Profile) 
In this program, you define the inventory level you wish to bill at plus the 
default minimums for initial storage, renewal storage and handling.
DBIP (Depositor Billing Profile) 
In this program, you define the invoicing type plus minimums at the invoice 
level for receipt, renewal and accessorial charges.
IISP (Item Initial Storage Profile) 
In this program, you set up the charges for initial storage and the discount 
period, if any.
IRSP (Item Renewal Storage Profile) 
In this program, you set up the charges for renewal storage and your renewal 
dates.
IHAP (Item Handling Profile) 
In this program, you set up the charges for handling.
IBIP (Item Billing Profile)
In this program, you assign the initial storage, renewal storage, handling and 
date profiles to the item profile. You also define the local overrides, if any, for 
the initial storage, renewal storage and handling minimums set up in DILP.
LODE (Location Billing Codes) 
In this program, you set up location billing codes if you charge different rates 
of storage for different areas in your warehouse or you want to assign revenue 
to different GL accounts.
INRE (Invoice Register Definition)
In this program, you set up your invoice register. An invoice register is a listing 
of all invoices produced on a certain date or range of dates. For each invoice 
on the listing there is a total for the invoice plus a breakdown by type of charge 
(for example, Initial Storage, Handling, Blast Freezing, etc.). 

BASIC BILLING SETUP
Billing Setup
BILLING AND INVOICING GUIDE 4.2 11
There are also two optional setup programs for extra charges:
The following flow chart shows the seven mandatory setup programs for billing and invoicing and how they 
are connected to customers and items.
GEXC (General Extra Charges) 
In this program, you set up charges that are automatically applied to a receipt 
or to an order when you run BILB.
ECHP (Extra Charge Profile) 
In this program, you set up charges that may or may not be related to a specific receipt or order and can be either manually or automatically applied by 
running BILB. 
CUST
DILP DBIP
ITEM
IBIP
IRSP
renewal
 storage
IISP IHAP
initial storage handling
LODE LODE
Location billing code Location billing code
ITEM BILLING PROFILE
if required, local overrides of 
the minimums defined in DILP
DEPOSITOR BILLING PROFILE
- invoicing type
- minimums at the invoice level 
for receipt, renewal and 
accessorial charges
DEPOSITOR INVENTORY LEVEL 
PROFILE
- inventory level you wish to bill at 
- default minimums at the customer 
level for initial storage, renewal 
storage and handling

BASIC BILLING SETUP
Billing Setup
SETTING UP THE INVOICE REGISTER DEFINTION (INRE)
An invoice register is a listing of all invoices produced on a certain date or range of dates. For each invoice on 
the listing there is a total for the invoice plus a breakdown by type of charge (for example, Initial Storage, 
Handling, Blast Freezing, etc.). 
You must set up your invoice register in INRE before you can run BILB (Daily Invoice Register). When you run 
BILB, AccellosOne 3PL accumulates all charges incurred since the last time that you ran the program and 
generates the invoice register and other financial reports. If AccellosOne 3PL is linked to your accounting 
system, DLRE also updates your accounts receivable and general ledger.
Daily Invoice Register showing section for renewal storage
You define three things in INRE:
 the invoice breakdown code or type (Accessorial, Freight, Receipt and Renewal)
 the column or columns on the invoice register (you need to define one column for each type of charge 
that you want to break out; for example, Initial Storage, Handling, etc.)
 the revenue analysis code(s) attached to each column
HighJump, INC. /usr1/del4/work/faxl Page 4 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 1 of 3
Print Date : 04-02-2000 Renewal Storage - Invoice List Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code & Name Total Charges
S-000111 19-01-2000 A Customer A 48643.16
S-000112 19-01-2000 B Customer B 757900.00
S-000113 19-01-2000 C Customer C 179559.64
S-000114 19-01-2000 D Customer D 107.00
S-000115 19-01-2000 E Customer E 2675.00
 ----------
Total Number of Invoices : 5 Total Charges : 988884.80
 ==========
HighJump, INC. /usr1/del4/work/faxl Page 5 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 2 of 3
Print Date : 04-02-2000 Renewal Storage - Revenue Analysis Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code Total Storage Miscell
S-000111 19-01-2000 A 48643.16 3182.36 0.00 0.00 0.00 0.00 0.00 45460.80
S-000112 19-01-2000 B 757900.00 757900.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000113 19-01-2000 C 179559.64 102879.64 0.00 0.00 0.00 0.00 0.00 76680.00
S-000114 19-01-2000 D 107.00 107.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000115 19-01-2000 E 2675.00 2675.00 0.00 0.00 0.00 0.00 0.00 0.00
 ---------- ---------- ------- ------- ------- ---------- ---------- --------
Totals 988884.80 866744.00 0.00 0.00 0.00 0.00 0.00 122140.80
 ========== ========== ======= ======= ======= ========== ========== =========
HighJump, INC. /usr1/del4/work/faxl Page 6 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 3 of 3
Print Date : 04-02-2000 Renewal Storage - G.L. Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
General Ledger Code & Description Total Charges
G.L. Posting Date : 19-01-2000
104200 Handling 122140.80
123456 General 851632.80HighJump
123457 Goods & Services Taxes 15111.20
 ----------
Total for Day 988884.80
 ----------
 ----------
Total for All Days 988884.80
 ==========

BASIC BILLING SETUP
Billing Setup
BILLING AND INVOICING GUIDE 4.2 13
FIELD DESCRIPTIONS
Breakdown Number Mandatory
You set up one breakdown number for each invoice type you require. Valid 
types of invoices are Accessorial, Freight, Receipt and Renewal (see Invoice 
Breakdown Code field).
Description Mandatory
Your breakdown description
Invoice Breakdown Code ACC = Accessorial
FRT = Freight
RCPT = Receipt
RENW = Renewal
The type of invoice.
Column Mandatory
You can have up to eight columns on each invoice. Column 9 is reserved for 
miscellaneous charges.
Description Top Mandatory
The first line of your column description (for example, INITIAL).
Description Bottom Optional
The second line of your column description (for example, STORAGE).

BASIC BILLING SETUP
Billing Setup
1 Enter INRE.
2 Click on Enter Criteria then Execute Query to see whether the invoice register has already been set up. If 
the invoice register has not been set up, click on Create Record. If the invoice register has been set up, 
refer to the next procedure (“Setting Up Additional Invoice Types” on page 15) for instructions.
3 Key in 1 for your first breakdown number and press Enter.
4 Key in a description for your first breakdown number (for example, Warehouse Receipts) and press 
Enter.
5 Use your pick list to select the appropriate invoice breakdown. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow 
keys to position your cursor over the appropriate code and click on Select Code. 
6 In the Column Number field, key in 1 and press Enter to set up your first column.
7 In the Description Top field, key in the first line of your description for this column (for example, INITIAL) 
and press Enter.
8 In the Description Bottom field, key in the second line of your description for this column if required (for 
example, STORAGE) and press Enter.
9 When the Revenue Analysis Block appears, click on Create Record. 
10 Use your pick list to select the appropriate revenue analysis code for your first column.
Revenue Analysis 
(REVA)
Mandatory
The revenue analysis codes attached to this column. When you run DLRE, 
AccellosOne 3PL will search for all charges whose charge codes are attached 
to the revenue analysis code(s) that you specify for each column. 
AccellosOne 3PL will accumulate the charges for each column and sort them 
by customer code. 
If AccellosOne 3PL finds any charges whose revenue analysis codes are not 
listed in the columns that you define, the charges will be listed in the Miscellaneous column of the Invoice Register.
FIELD DESCRIPTIONS

BASIC BILLING SETUP
Billing Setup
BILLING AND INVOICING GUIDE 4.2 15

Invoice Register Definition showing a revenue analysis code of FE assigned to column 1
11 If you have further revenue analysis codes to add to this column, repeat the previous step.
12 When you finish entering your revenue analysis codes for the first column, click on Return to Main to exit 
create mode.
13 Click on Column Block.
14 Click on Create Record.
15 Key in 2 and press Enter to set up your second column.
16 In the Description Top and Description Bottom fields, key in the first and second lines of your description 
for this column and press Enter after each field.
17 Use your pick list to select the appropriate revenue analysis codes for your second column.
18 Repeat the previous step for each revenue analysis code that you wish to add to your second column.
19 Repeat the above steps for each additional column that you wish to add to this invoice type. When you 
finish setting up all your columns for your first invoice type, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit the program.
SETTING UP ADDITIONAL INVOICE TYPES
1 Enter INRE.
2 Click on Enter Criteria then Execute Query to display the invoice type that you set up in the main procedure.
3 Click on Create Record.
4 Key in 2 as your breakdown number and press Enter.
5 Key in a description for your second invoice type and press Enter.
6 Set up your column numbers, column headings and the revenue analysis codes that belong to each column.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
7 When you finish all your columns and revenue analysis codes for your second invoice type, click on 
Return to Main to exit create mode. Then click on Master Block and Exit to exit the program.
Working With Maximum and Minimum Charges
AccellosOne 3PL supports multiple maximum and minimum charges. You can apply maximum/minimum 
charges to a billing entity, receipt invoice line, receipt invoice, renewal invoice, charge code or individual 
receipt/order. When multiple maximum/minimum charges apply to the same item, the individual maximum/
minimum are calculated at each level — billing entity, receipt line, etc. — independently of the maximum or 
minimum charges at another level.
EXAMPLE
You charge by the PALLET and you receive 1 PALLET.
minimum charge in RATE = 5.00
rate = 2.50 per pallet
initial storage minimum = 10.00 
billing entity minimum = 25.00
receipt invoice minimum = 100.00
Because of the various minimums that apply, the total charge for the one pallet would be $100.00.
There are two ways in which minimums are shown in AccellosOne 3PL. If the minimum is set up in RATE, the 
minimum value replaces the actual value; for example, $5.00 (the minimum) replaces $2.50 (the actual 
charge). If the minimum is set up in any other program (for example, any minimum field in IBIP), two charges 
are generated whenever a minimum charge is activated: the actual charge plus whatever amount is needed 
to bump up the actual charge to the minimum charge. The sum of the two charges equals the minimum 
charge.
CHARGE 
QUANTITY RATE CHARGE EXPLANATION
5.00 5.00 added to meet initial storage minimum of 10.00
15.00 15.00 added to meet billing entity minimum of 25.00
75.00 75.00 added to meet receipt invoice minimum of 
100.00
100.00 Total

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 17
DEFAULT MAXIMUM/MINIMUM CHARGES
You set up your default maximum/minimum charges in DILP. These defaults apply to all of a customer’s 
items. If this default does not apply to certain items, you must override the default by setting up a maximum/
minimum charge in IBIP (Item Billing Profile). 
There are four minimum charges set up in DILP:
 billing entity minimum
 renewal storage line minimum
 initial storage minimum
 handling minimum
NOTE Maximum/minimum charges are always calculated independently of any 
other charges that may be added to a receipt or to an order. For example, suppose 
you receive product from customer A and an initial storage minimum is invoked 
because of the quantity of product received. Then you add an accessorial charge to 
your receipt in ENRE for special handling.
Even if the sum of the initial storage charge and the accessorial charge exceeds the 
initial storage minimum, an initial storage minimum will still be triggered because the 
system will ignore accessorial charges when determining whether an initial storage 
minimum is required.
FIELD DESCRIPTIONS
Billing Entity Minimum 
Charge Code
See “Maximum/Minimum Charges for Billing Entities” on page 
22.
Renewal Storage Line 
Minimum Charge Code
This minimum charge applies to each renewal storage entity on your invoice. 
A renewal storage entity consists of all product in which:
 the appropriate inventory level values are the same (if you bill at level 1, all 
level 1 values must be the same but levels 2 and 3 if any can differ; if you 
bill at level 2, all levels up to level 2 must be the same but level 3 if any can 
differ) 
 the renewal period is the same
 the location bill code is the same
If there is no minimum charge for renewal storage lines, set this field to NC for 
No Charge.
Initial Storage Minimum 
Charge Code
This minimum charge applies to initial storage charges on a particular receipt 
line. If there is no minimum charge for initial storage, set this field to NC for No 
Charge.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges

DILP screen showing minimum charges for billing entities and initial storage
ITEM-SPECIFIC MAXIMUM/MINIMUM CHARGES
You set up your item-specific maximum/minimum charges, if any, in IBIP. These maximum/minimum charges 
apply only to those items that your IBIP profile is attached to. IBIP maximum/minimums are local (that is, itemlevel) maximum/minimums that override the customer level defaults defined in DILP.
There are four item-specific maximum/minimum charges set up in IBIP:
 billing entity minimum
 renewal storage line minimum
 initial storage minimum
 handling minimum
Handling Minimum 
Charge Code
This minimum charge applies to the handling charges on a particular receipt 
line. If there is no minimum charge for handling, set this field to NC for No 
Charge.
FIELD DESCRIPTIONS

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 19
FIELD DESCRIPTIONS
Billing Entity Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the 
default billing entity maximum/minimum charge defined in DILP (Depositor 
Inventory Level Profile). 
Renewal Storage Line 
Minimum Charge Code
Optional
If you enter a charge code in this field, this charge code will override the 
default renewal storage line maximum/minimum charge defined in DILP 
(Depositor Inventory Level Profile).
Initial Storage Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the 
default initial storage maximum/minimum charge defined in DILP (Depositor 
Inventory Level Profile).
Handling Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the 
default handling maximum/minimum charge defined in DILP (Depositor Inventory Level Profile). 

BASIC BILLING SETUP
Working With Maximum and Minimum Charges

IBIP screen showing minimum for renewal storage line
MINIMUM CHARGES FOR A GIVEN INVOICE
You set minimum charges for a given invoice in DBIP. There are four minimum charges set up in this program:
 receipt charge
 renewal storage minimum
 accessorial minimum
 threshold accessorial minimum
FIELD DESCRIPTIONS
Minimum / Maximum 
Receipt Charge Code
Optional
If you have a minimum charge for receipt charges on an invoice, enter the 
appropriate charge code. If there is no minimum charge for receipt charges, 
leave this field blank.
NOTE Maximum charges for receipt charges are not supported in this 
release of AccellosOne 3PL.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 21
Minimum / Maximum 
Renewal Charge Code 
Optional
If you have a minimum charge for renewal charges on an invoice, enter the 
appropriate charge code. If there is no minimum charge for renewal charges, 
leave this field blank.
NOTE Maximum charges for renewal charges are not supported in this 
release of AccellosOne 3PL.
Minimum / Maximum 
Accessorial Charge Code 
Optional
If you have a minimum charge for accessorial charges on an invoice, enter the 
appropriate charge code. If there is no minimum charge for accessorial 
charges, leave this field blank.
NOTE Maximum charges for accessorial charges are not supported in this 
release of AccellosOne 3PL.
Threshold Accessorial 
Charge Code
Optional
This field allows you to specify a minimum dollar value for an accessorial 
invoice. If you specify a minimum, no accessorial invoice will print if it has not 
reached the minimum value. The charges on the invoice will continue to accumulate until the threshold is met. 
If there is no minimum value for an accessorial invoice, leave this field blank.
FIELD DESCRIPTIONS

BASIC BILLING SETUP
Working With Maximum and Minimum Charges

DBIP screen showing two minimum charges: one for receipt charges and one for an accessorial 
invoice
MAXIMUM/MINIMUM CHARGES FOR BILLING ENTITIES
A billing entity is all product received on one receipt in which all the levels of inventory used in billing are 
identical.
For example, suppose you have a customer with two inventory levels — item and lot number — and you bill 
at the lot level. You are receiving product from this customer and because of the way in which the truck is 
loaded you receive the following:
Lines 1 and 3 — although on different receipt lines — represent identical product with the same item and lot 
numbers and are therefore considered a single billing entity. When the system calculates initial storage and 
handling, lines 1 and 3 will be consolidated into a single billing entity and if the total of this billing entity is less 
than the minimum charge, the actual charge will be replaced by the minimum charge.
EXAMPLE
LINE 
NUMBER ITEM
LOT 
NUMBER QUANTITY
1 item 1 101 100 cases
2 item 2 101 200 cases
3 item 1 101 5 cases
4 item 1 299 80 cases

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 23
line 1 --> initial storage: $10/ initial handling: $5
line 2 --> initial storage: $15/ initial handling: $7.50
line 3 --> initial storage: $2/ initial handling: $1.25
line 4 --> initial storage: $10/ initial handling: $5
billing entity minimum charge = $20.00
If you bill this customer at the item level, the totals for the three billing entities will be calculated as follows:
line 1 and 3 = 15 + 3.25 = 18.25
line 2 = 22.50
line 4 = 15
The charge for line 2 (item 2, lot 101) is above the minimum and therefore not affected by the minimum 
charge. However, the charges for lines 1 and 3 (item 1, lot 101) and line 4 (item 1, lot 299) are below the 
minimum charge and therefore the actual charge will be replaced by the minimum charge.
MINIMUM CHARGES FOR A GIVEN RECEIPT/ORDER
You can define minimum charges for individual receipts and orders when invoicing through UALL. The 
minimum charge is based on the total number of charges regardless of type applied to a given receipt/order.
Consider the following examples:
Example 1 
Minimum charge on each receipt = $100
$20.00 (initial storage on item 1)
$30.00 (initial storage on item 2)
$30.00 (initial storage on item 3)
$10.00 (initial handling on item 3)
$90.00 total
The total of $90 is less than the minimum charge for the receipt; therefore, the $100 minimum charge applies. 
Example 2 
Minimum charge on each order = $100
$20.00 (manual charge on order header)
$30.00 (manual charge for item 1)
$30.00 (manual charge for item 2)
$10.00 (extra charge on item 3)
$90.00 total
The total of $90 is less than the minimum charge for the order; therefore, the $100 minimum charge applies. 
Example 3 
Minimum charge on each order = $80
$20.00 (manual charge on order header)
$30.00 (manual charge for item 1)
$30.00 (manual charge for item 2)
NOTE Billing entity minimums apply to initial storage and handling only. They are 
not required for renewal storage because the system automatically consolidates 
receipt lines containing identical product when it calculates renewal storage.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
$10.00 (extra charge on item 3)
$90.00 total
The minimum charge does not apply as the order total ($90) exceeds the minimum charge ($80).
You set up minimum receipt charges by attaching the appropriate charge code to the Accessorial Invoice 
Receipt Minimum Charge Code field in DBIP (Depositor Billing Profile). Likewise, you set up minimum order 
charges by attaching the appropriate charge code to the Accessorial Invoice Order Minimum Charge Code 
field in DBIP.
DBIP screen showing Accessorial Invoice Receipt Minimum Charge and Accessorial Invoice Order 
Minimum Charge fields
SETTING UP MAXIMUM/MINIMUM CHARGE CODES
Maximum/minimum charge codes should be set up with a charge type of SING, a charge definition of B for 
Break and a single break in RATE.
1 Enter CHAR and click on Create Record.
2 Key in your charge code and description.
3 Press Enter twice to bypass the Reference and External Reference fields.
4 In the Charge Type field, key in SING and press Enter.
5 In the Charge Definition field, key in B for Break and press Enter.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 25

Charge Code (CHAR)
6 Key in your general ledger, revenue analysis and invoice type values.
7 Key in your charge on and qualify on SKU codes.
8 Press Enter to bypass the Default Rate Charge Code field.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges

Depositor Billing Rates (RATE)
9 In RATE, key in the customer to whom the charge applies and press Enter. If the charge applies to all 
customers, use .ALL as your customer code.
10 Key in your effective date and press Enter.
11 In the Number of Breaks field, key in 1 and press Enter.
12 In the Minimum Charge field, key in your minimum charge and press Enter. If there is no minimum 
charge, press Enter with this field set to the default value of 0.
13 In the Maximum Charge field, key in your maximum charge and press Enter. If there is no maximum 
charge, press Enter with this field set to the default value of 99999999999.99.
14 Press Enter to bypass the remaining fields in CHAR.
15 When the Detail Block appears, press Enter to accept the default value in the Quantity Break field.
16 In the Charge Amount field, key in 0 and press Enter.

BASIC BILLING SETUP
Working With Maximum and Minimum Charges
BILLING AND INVOICING GUIDE 4.2 27

Detail Block of RATE showing a single break with a charge amount = 0
17 Click on Master Block and Return to Main. Then click on Exit to exit.
MONTHLY MINIMUM BILLING
This billing option allows you to define a minimum monthly charge when the total of all invoices for a given 
month is less than the minimum. For example, suppose you define a monthly minimum charge of $100. If the 
total of all invoices — warehouse receipt invoices, renewal invoices, accessorial invoices, etc. — is $55, 
AccellosOne 3PL will charge an additional $45 to reach the minimum. 
The following conditions apply to monthly minimum billing:
 The customer’s status must be A for Active in CUST.
 If the total invoice amount is zero or if no invoice is generated, the monthly minimum charge will apply if 
there is still inventory in the warehouse.
 All invoices created with an invoice date between the 1st of the month and the batch create date of the 
minimum invoice will be counted when calculating the minimum. For example, if the minimum invoice 
batch is created on Oct-15, AccellosOne 3PL will look at all receipt, renewal and accessorial invoices 
created between Oct-01 and Oct-15 when determining whether a monthly minimum invoice is required.
You set up monthly minimum billing in DBIP by entering a charge code in the Total Invoices Minimum Charge 
Code field.

BASIC BILLING SETUP
Working With Charge Groups
DBIP screen showing monthly minimum billing
Monthly minimum billing requires a separate batch and invoice using the batch type “Minimum Total Invoices” 
in BILB (Billing Batch). This batch type should be run after the extra charge batch/invoice, accessorial batch/
invoice and renewal batch/invoice.
Working With Charge Groups
Charge groups allow you to group two or more charge codes in a single charge group and calculate a 
minimum/maximum value based on the sum of all charges in the charge group. It is designed to provide a 
substitute in a single, easy-to-maintain program for the various minimum/maximum charges scattered 
throughout DILP, DBIP and IBIP. 
If the minimum/maximum applies to two or more charge codes, the Detail Block must be populated with those 
charge codes. If, on the other hand, the minimum/maximum applies to a single charge group type, the Detail 
Block will be left empty. 
FIELD DESCRIPTIONS
Charge Group Code Mandatory
Your charge group code.

BASIC BILLING SETUP
Working With Charge Groups
BILLING AND INVOICING GUIDE 4.2 29
Description Mandatory
Your description for the charge group code.
Minimum / Maximum 
Charge Code
Mandatory
Your maximum/minimum charge for the charge group.
Charge Group Type Document Line This charge group type is used to create receipt or order 
charges with the minimum /maximum applied to all charges attached to each 
line of a receipt/order.
Document This charge group type is used to create receipt or order charges 
with the minimum/maximum applied to all the charges attached to an entire 
receipt or order.
Billing Entity This charge group type can be applied at the document, batch 
or invoice level. It will group the charges for the same billing entity and apply 
the minimum/maximum to that amount.
Invoice This charge group type applies the minimum/maximum to an entire 
invoice.
NOTE There are four charge group types, each of which is calculated independently. That means you can set up one minimum for each of the four types 
for a total of four minimums applied.
Charge Code If you enter two or more charge codes in this field, the maximum/minimum 
charge will apply to the sum of all charges in the charge group.
FIELD DESCRIPTIONS

BASIC BILLING SETUP
Changing Your Rates
CHGR screen showing charge group for Document Line
Changing Your Rates
You change your rates for a particular charge code in the program RATE (Depositor Billing Rates). You 
change a rate in this program by keying in a new effective date over the old effective date and then entering 
your new rates. AccellosOne 3PL will create a new record in RATE; the new record will be identical to old 
record — that is, the same charge code, customer code, charge type code, etc. — except for the effective 
date. The old rate remains in RATE under the old effective date. That means that you always have a complete 
listing of the current rate plus all previous and future rates.
You can change a rate in RATE effective immediately by entering the current date as your effective date or 
you can change a rate effective in the future by entering a future date as your effective date. 
TYPE OF CHARGE RATE CHANGE TAKES EFFECT
receipt The rate change takes effect for any new product received from that point on (if you enter the 
current date as your effective date) or on or after the new effective date (if you enter a future 
date as your effective date).
accessorial The rate change takes effect for any new accessorial charges entered from that point on (if 
you enter the current date as your effective date) or on or after the new effective date (if you 
enter a future date as your effective date).

BASIC BILLING SETUP
Changing Your Rates
BILLING AND INVOICING GUIDE 4.2 31
ENTERING A RATE CHANGE
1 Enter RATE.
2 Click on Enter Criteria
3 If you wish to query by customer code, key in your customer code and press Enter. If you do not wish to 
query by customer code, press Enter to bypass this field.
4 Key in your charge code and click on Execute Query. The system will display the current RATE record for 
the charge.

Depositor Billing Rates (RATE)
renewal The rate change takes effect for any new product charged for renewal from that point on (if 
you enter the current date as your effective date) or on or after the new effective date (if you 
enter a future date as your effective date).
For existing inventory, the rate change may or may not apply to existing inventory depending 
on the option that you selected in the Original or Current Rate on Renewals field in DBIP. 
C for Current The new rates will be applied to existing inventory as 
well; that is, the next time renewal charges are calculated for an item or lot of existing inventory, the system will use the current rate — not the original rate.
I for Initial Original or R for Renewal 
Original
The rates set up in IISP or IRSP when the product 
was received will apply to renewal storage charges 
for existing inventory.
TYPE OF CHARGE RATE CHANGE TAKES EFFECT

BASIC BILLING SETUP
Changing Your Rates
5 Key in your new effective date over the old effective date and press Enter. AccellosOne 3PL will create a 
new record in RATE; the new record will be identical to old record except for the effective date.
6 When you finish changing your rates, click on Return to Main and Exit to exit.
CANCELLING A RATE CHANGE
If the effective date of the rate change is in the future, you cancel a rate change by deleting the appropriate 
record in RATE.
1 Enter RATE.
2 Use your query commands to locate the RATE record containing the rates that you wish to cancel.
3 Press Enter until your cursor is positioned in the Minimum Charge field.
4 Click on Delete Record.
5 Click on Return to Main and Exit to exit.
CHANGING YOUR RATES BY A FIXED PERCENTAGE IN IDRA
If you wish to change one or more of your rates by a fixed percentage, you use the program IDRA (Increase/
Decrease Rates). IDRA allows you to increase or decrease your rates as of an effective date that you specify. 
The effective date in IDRA must be a date in the future; that is, the current date plus one. When you run IDRA, 
If the charge that you are 
changing is a flat rate charge:
If the charge has breaks (that is, 
not a flat rate):
a) Press Enter until your cursor is 
positioned in the Flat Rate field.
b) In the Flat Rate field, key in your 
new flat rate and press Enter.
a) Press Enter until your cursor is 
positioned in the Number of 
Breaks field.
b) In the Number of Breaks field, 
key in your new number of 
breaks and press Enter. If the 
number of breaks is the same, 
key in the old number of breaks 
and press Enter.
c) In the Minimum Charge field, key 
in your minimum charge and 
press Enter. If there is no minimum charge, key in 0.
d) In the Maximum Charge field, 
key in your maximum charge and 
press Enter. If there is no maximum charge, key in 
999999999.99.
e) When the Detail Block is displayed, key in your quantity 
break and charge amount for 
each break. Press Enter after 
entering each value.
f) Click on Master Block to exit the 
Detail Block.

BASIC BILLING SETUP
Changing Your Rates
BILLING AND INVOICING GUIDE 4.2 33
the system creates a second record in RATE for each charge code that you specify in IDRA. The second 
record has the same customer code and charge code as the first record but a different effective date and 
different rates.
IDRA applies to your break charges only; that is, the rates in the Detail Block of RATE. It does not apply to flat 
rate and maximum/minimum charges. If you wish to change flat rate and maximum/minimum charges, you 
must do so manually in RATE. If a charge code has both break and flat rate/maximum-minimum charges, 
IDRA will change the break charges but leave the other charges unchanged.
You can restrict rate increases and decreases by customer code and charge code or you can enter no restrictions in IDRA and change rates for all charge codes attached to the customer that you specify. 
1 Enter IDRA.

Increase/Decrease Rates (IDRA)
2 Key in your customer code and press Enter.
3 Key in your charge code and press Enter or press Enter with this field blank to change rates for all charge 
codes.
4 Key in your effective date and press Enter. The effective date must be in the future; that is, the current 
date plus one.
5 Key in your percentage change and press Enter. To enter a rate increase, you enter a positive number 
(for example, 5.7). To enter a rate decrease, you enter a negative number (for example, -10).
NOTE If you specify .ALL as your customer code, IDRA will change all rates 
attached to the customer code .ALL. It will not, however, change the rates of all customers. For example, if you have five charge codes attached to .ALL and three 
charge codes attached to ABCSUPP (ABC Supplies), a customer code of .ALL in 
IDRA will apply the rate change to your five .ALL charge codes but leave your three 
ABCSUPP charge codes unchanged.

BASIC BILLING SETUP
Working With Renewal Storage
6 Click on Process Change.
CANCELLING AN IDRA RATE CHANGE
You cancel an IDRA rate change by deleting the appropriate record in RATE.
1 Enter RATE.
2 Use your query commands to locate the RATE record containing the rates that you wish to cancel.
3 Press Enter until your cursor is positioned on the Minimum Charge field.
4 Click on Delete.
5 Click on Return to Main and Exit to exit.
Working With Renewal Storage
Renewal storage is any recurring storage charge that is charged after initial storage. Renewal storage is 
normally charged for as long as the product is in the warehouse.
MAXIMUM DAILY BILLING
In maximum daily billing, renewal storage charges are based on the highest daily quantity during the billing 
period just past. Maximum daily billing supports both single break and multi-break charges.
EXAMPLE USING FIRST OF MONTH BILLING
In this type of billing, the initial storage charge is zero. On the first of the month, your highest daily balance for 
the previous month is 1,000 cases and you charge on that amount. In the second renewal period, you receive 
an additional 300 cases on the 5th for a total quantity of 1,300 (1,000 + 300). On the 10th, you ship out 100 
cases for a total quantity of 1,200 (1,000 + 300 -100). On the first of the following month, your new highest 
daily balance for the previous period is 1,300 cases and you charge renewal storage on this amount.
PERIOD 1
Inbounds: 1,000 cases received on 18th
Maximum: 1,000 cases
PERIOD 2
Initial maximum: 1000 cases
Inbounds: 300 cases received on 5th 
Outbounds: 100 cases shipped on 10th 
Maximum: 1,300 cases
18 05 01 01
+1000 CS
renewal storage renewal storage
+300 CS
10
-100 CS =1200 CS

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 35
SETTING UP MAXIMUM DAILY BILLING
1 Create a charge code in CHAR with a charge type code of MAXD (Maximum Daily Single Break) or 
MAXX (Maximum Daily Multi-Break).
2 Attach your charge code to your renewal storage profile in IRSP.
3 Attach your renewal storage profile to IBIP.
4 Attach your item billing profile to your items in ITEM.
5 Set up your rates for the charge code in RATE.
CHECK-IN ONLY BILLING
With check-in only billing, renewal charges are based on the opening balance plus inbounds during the billing 
period just past. The opening balance does not include outbound shipments from the previous period. In this 
type of billing, the initial storage charge is usually zero.
EXAMPLE USING FIRST OF MONTH BILLING
On the first of May, your opening balance for the previous month is 0 cases and you received 1,000 cases 
during the month. Your billing amount for period 1 is therefore 1,000. In the second renewal period, your 
opening balance for the previous period is 1,000 cases and during the month you receive 300 cases; your 
billing amount for this period is 1,300 (1,000 + 300) and does not include any outbound shipments. 
On July 1 you look back at your third renewal period; your opening balance is 1,200 (1,000 + 300 - 100) 
cases. Since you have no inbounds in period 3, your billing amount (1,200) is the same as your opening 
balance.
SETTING UP CHECK-IN ONLY BILLING
1 Create a charge code in CHAR with a charge type code of either CIO (Check-In Only) for single break 
charges or MXCX (Max. Daily CIO - Multi-Break) for multi-break charges.
2 Attach your charge code to your renewal storage profile in IRSP.
3 Attach your renewal storage profile to IBIP.
PERIOD 1
Opening balance: 0
Inbounds: 1,000 cases received on 
18th
Billing Amount: 1,000 cases
PERIOD 2
Opening balance: 1,000 cases
Inbounds: 300 cases received on 5th 
Outbounds: 100 cases
Billing Amount: 1,300 cases (1,000 + 
300)
PERIOD 3
Opening balance: 1,200 cases 
(1,000 + 300 - 100)
Outbounds: 400 cases
Billing Amount: 1,200 cases
18 10 JUNE 01 JULY 01 
+1000 CS -100 CS
$ renewal storage renewal storage
-400 CS
15
=1000 CS = 800 CS
MAY 01 05
+300 CS =1200 CS
$ $
renewal storage

BASIC BILLING SETUP
Working With Renewal Storage
4 Attach your item billing profile to your items in ITEM.
5 Set up your rates for the charge code in RATE.
DAILY AVERAGE BILLING
With daily average billing, AccellosOne 3PL calculates a daily inventory balance for an item or group of items. 
When you generate your renewal or accessorial batch, the system adds up all the daily balances and then 
divides the total by the number of days on which there was inventory in the warehouse for the item or items.
Daily average billing is only available for unit-based SKU’s; you cannot use daily average billing if you bill by 
weight or cube.
EXAMPLE 
Suppose Customer A has the following balances:
If you run a batch on August 7, the system will calculate the daily average as follows:
11 + 15 + 5 + 3 + 8 (for Item A) + 3 + 5 + 5 + 4 +3 (for item B)/ 5 = 12.4 (or 13 pallets with rounding)
You divide the total by 5 rather than by 7 because there was no inventory on August 6 and 7.
SETTING UP DAILY AVERAGE BILLING
1 Enter DBIP and retrieve the billing profile for the customer that you want to set up for daily average billing.
2 Do one of the following:
DATE
DAILY BALANCE 
FOR ITEM 1
DAILY BALANCE 
FOR ITEM 2
August 1 11 PLT 3 PLT
August 2 15 PLT 5 PLT
August 3 5 PLT 5 PLT
August 4 3 PLT 4 PLT
August 5 8 PLT 3 PLT
August 6 0 PLT 0 PLT
August 7 0 PLT 0 PLT
If daily average billing applies to 
all of a customer’s items:
If daily average billing applies to 
a single item or group of items:
a) Enter the code CDAV in the 
Renewal Summarization Code 
field.
a) Enter the code ISUM in the 
Renewal Summarization Code 
field.

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 37

DBIP screen showing Renewal Summarization Code field set to CDAV
3 Exit DBIP and enter CHAR.
4 Create one or more charge codes with a charge type of either DAVS (Daily Average Single Break) or 
DAVM (Daily Average Multi-Break). Make sure that the charge on and qualify on SKU is a unit-based 
SKU.

CHAR screen showing a charge type of DAVS (Daily Average Single Break)

BASIC BILLING SETUP
Working With Renewal Storage
5 Exit CHAR and enter IRSP.
6 Create a renewal storage profile with a single record in the Frequency Block. Set the Frequency Code to 
D for Daily and set the Cycle field to 1. 
7 In the Location Bill Block, attach the charge code or codes that you created in the previous step to the 
appropriate location billing codes. These charge codes must have a charge type of either DAVS or 
DAVM.

IRSP screen showing a frequency code of D for Daily, a cycle of 1 and a charge code whose charge 
type is set to DAVS or DAVM
8 Exit IRSP and enter IBIP. Attach your IRSP profile to your item billing profile.

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 39

IBIP screen showing DAVG as the renewal storage profile code
9 Do one of the following:
If you entered CDAV as your 
renewal summarization code in 
DBIP:
If you entered ISUM as your 
renewal summarization code in 
DBIP:
a) Leave the Renewal Summarization Code field blank since the 
option that you selected in DBIP 
applies to all of the customer’s 
items. 
a) Enter the code CDAV in the 
Renewal Summarization Code 
field.

BASIC BILLING SETUP
Working With Renewal Storage
IBIP screen showing CDAV as your renewal summarization code
10 Exit IBIP and enter ITEM. Attach your new IBIP profile to all items requiring daily average billing.
EXCEED DAILY AVERAGE BILLING
You can define a fixed number of pallet/case spaces that are “reserved” for a given customer and generate a 
charge whenever this number is exceeded. The charge is based on the daily average of the “over” quantity.
For example, suppose the reserved space or base quantity for a customer is 500 pallets. 
Calculation: 625/5 = 125 x rate (day 2 with zero quantity over is not counted)
DAY INVENTORY QUANTITY OVER
1 550 50
2 500 0
3 560 60
4 555 55
5 560 60
6 900 400

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 41
You set up exceed daily average billing in DBIP by entering EDAV (Exceed Daily Average) in the Renewal 
Summarization Code field. In the Reserved Quantity field, you enter your reserved quantity in your renewal 
storage charge on SKU. For example, if your charge on SKU for renewal storage in CHAR is cases and you 
enter 500 in the Reserved Quantity field, your reserved quantity will be 500 cases.
DBIP screen showing a reserved quantity of 500
Setup
1 In CHAR charge code type = DAVM or DAVS.
2 In DBIP renewal summarization code = EDAV (if exceed daily average billing applies to all of the customer’s items) or ISUM (if exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if exceed daily average billing applies to all of the customer’s items) or EDAV (if exceed daily average billing applies to a single item or group of items).
TOTAL EXCEED DAILY AVERAGE BILLING
You can define a fixed number of pallet/case spaces that are “reserved” for a given customer and generate a 
charge for the sum of exceeded quantities.
For example, suppose the reserved space or base quantity for a customer is 500 pallets. 
DAY INVENTORY QUANTITY OVER
1 550 50
2 500 0
3 560 60
4 555 55
5 560 60

BASIC BILLING SETUP
Working With Renewal Storage
Calculation: 625 x rate
You set up total exceed daily average billing in DBIP by entering EDTO (Total Exceed Daily) in the Renewal 
Summarization Code field. In the Reserved Quantity field, you enter your reserved quantity in your renewal 
storage charge on SKU. For example, if your charge on SKU for renewal storage in CHAR is cases and you 
enter 500 in the Reserved Quantity field, your reserved quantity will be 500 cases.
DBIP screen showing a reserved quantity of 500
Setup
1 In CHAR charge code type = DAVM or DAVS.
2 In DBIP renewal summarization code = EDTO (if total exceed daily average billing applies to all of the 
customer’s items) or ISUM (if total exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if total exceed daily average billing applies to all of the customer’s items) or EDTO (if total exceed daily average billing applies to a single item or group of items).
DAILY AVERAGE BILLING BASED ON NUMBER OF PALLET POSITIONS
If you store pallets in bulk locations, you can have the system charge for the number of pallet positions versus 
the physical number of pallets in a location. 
For example, suppose you have a bulk location that can stack four pallets high, but you have three physical 
pallets in that location. With Customer Daily Maximum billing, the system will charge for four pallets instead of 
three. The reasoning is that because the space is unusable, you want to re-coup your costs for the entire bulk 
space versus what is actually being used.
This billing option is designed for product that is crushable, which limits the stacking height.
Setup
1 In CHAR charge code type = DAVM or DAVS.
6 900 400
DAY INVENTORY QUANTITY OVER

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 43
2 In DBIP renewal summarization code = CDMX (if daily average billing applies to all of the customer’s 
items) or ISUM (if total exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if daily average billing applies to all of the customer’s items) 
or CDMX (if total exceed daily average billing applies to a single item or group of items).
SINGLE LEVEL BILLING
Single level billing allows you to generate a single charge for mixed product received on the same pallet. For 
example, suppose you bill at inventory level 2 or higher and you receive two different lots on the same pallet. 
AccellosOne 3PL would generate a single charge for the whole pallet. 
You set up single level billing by setting the Single Level Billing flag in DBIP to Y for Yes for the appropriate 
customers. 
MONTHLY RENEWAL INVOICING
With monthly renewal invoicing, you can generate renewal invoices for each billing entity based on a predetermined scheduled such as every 30 days or every seven days. For example, suppose you charge renewal 
storage daily and have the following inventory in your warehouse:
 billing entity A received on July 1
 billing entity B received on July 15
If monthly renewal invoicing is deactivated and you generate a renewal batch on August 5, it would have an 
invoice date of August 5 and would contain the renewal storage charges from July 1 to August 5 for billing 
entity A as well as the renewal storage charges from July 15 to August 5 for billing entity B. 
With month renewal invoicing, a renewal storage batch generated on August 5 would contain only charges for 
billing entity A up to July 31. Charges for billing entity A incurred after July 31 could only invoiced the following 
month. And charges for billing entity B could only be invoiced on August 15 or later.
You activate monthly renewal storage invoicing by entering appropriate values in the following two fields in 
DBIP.
NOTE Monthly renewal invoicing is only available for IND and UREN invoicing.
FIELD DESCRIPTIONS
Number of Days Between 
Renewal Invoices
You activate monthly renewal storage invoicing by entering a value greater 
than zero (say, 30) in this field.
Create Renewal Invoice 
at Zero Inventory
Only available if Number of Days Between Renewal Invoices > 0
If you set this flag to Y for Yes, the billing entity will have its next renewal 
invoice date reset to the date that the inventory is zero out. If you set this field 
to N for No or leave it blank, the next renewal invoice date will not be reset.

BASIC BILLING SETUP
Working With Renewal Storage
DBIP screen showing monthly renewal invoicing activated
In DBIP you establish your customer-level defaults. You can override your customer-level defaults for 
individual items by entering different values in IBIP.
RENEWAL INVOICING BY RECEIPT
With renewal invoicing by receipt, you can generate one renewal invoice for each receipt. For example, 
suppose you charge renewal storage daily and you receive and confirm five receipts on September 1. If you 
generate a renewal storage batch on September 2, AccellosOne 3PL will generate five different invoices; one 
for each receipt. If renewal invoicing by receipt is deactivated, AccellosOne 3PL would generate a single 
renewal invoice for all five receipts on September 2. 
You activate renewal invoicing by receipt by setting the Renewal Invoice by Receipt flag in DBIP to Y for Yes. 
Renewal invoicing by receipt is only available for IND and UREN invoicing.

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 45
DBIP screen showing renewal invoicing by receipt activated
RENEWAL INVOICING BY OPID
You can calculate renewal storage charges by outbound pallet ID rather than unique billing entity. That is, the 
renewal calculation will be based on the entire unshipped outbound pallet associated with the OPID and will 
not consider individual inventory entities.
An OPID can be composed of different billing entities. For example, item A, Lot 123, PID A-123 can be 
shipped out together with item B, Lot 123, PID B-123 in one OPID, say 0001. The renewal calculation will 
treat each unique OPID as a different billing entity and apply the correct renewal charge. Each OPID is 
considered as one pallet to bill.
In LODE, you set the Renewal Calc. by OPID flag to Yes for the appropriate location bill code(s). Depending 
on your requirements, renewal storage by OPID can be activated for some location bill codes, all location bill 
codes or none. 
LODE screen showing Renewal Calc. by OPID flag set to Yes
In DBIP, you set the Renewal Calculation by OPID flag to Yes.

BASIC BILLING SETUP
Working With Renewal Storage
DBIP screen showing Renewal Calculation by OPID flag set to Yes 
LOOKING UP RENEWAL STORAGE INFORMATION
You look up renewal storage information in the Renewal Block of LOEN. The Renewal Block shows the 
period number, next renewal date, last renewal date, number of units, gross/net weight of the item and the 
number of conveyances (if applicable). 
The period number refers to the product’s current renewal period. For example, if the period number is 3, that 
means that the product has been renewed twice and is currently in its third renewal period. If the period 
number is -1 and the next renewal date is 01.01.01, this means that the receipt was never rated. Use RCRA 
(Receipt Rater) or CHRF to rate the receipt.
1 Enter LOEN.
2 Key in your customer code and press Enter.
3 Key in your item code and level 2, 3 and 4 values (if any) and press Enter.
4 When the inventory entity whose renewal information you wish to look up is displayed, click on Location 
Block.
5 Click on Renewal Block.
NOTE Unlike the Location Block, the Renewal Block is not updated in real time and 
may show out-of-date information. For example, you have generated and confirmed a 
renewal batch but the next and last renewal dates remain unchanged or you shipped 
out one pallet a week ago and your current balance is three yet the Renewal Block 
shows a quantity of four pallets. 
In the majority of cases, you can update the information in the Renewal Block by running RENW. See the section “Running the Renewal Preprocessor (RENW) On 
Demand” on page 42 for complete instructions.

BASIC BILLING SETUP
Working With Renewal Storage
BILLING AND INVOICING GUIDE 4.2 47

Renewal Block in LOEN showing renewal period 7
In the sample screen shown above, the product is in its eighth renewal period. It last renewed on 
08.11.07 and will be renewed for the eighth time on 09.08.07.
6 When you finish viewing the renewal information, click on Drill Block and Inventory. Then click on Exit to 
exit.
RUNNING THE RENEWAL PREPROCESSOR (RENW) ON DEMAND
The renewal preprocessor (RENW) is a special program that updates the billing history of your inventory; any 
transaction that you enter in ENOR (orders and transfers), RELO and ENAJ potentially affects the billing 
history of an item.
The purpose of the renewal preprocessor is to shorten the processing time of a renewal batch by catching 
and correcting as many billing errors as possible before running your renewal batch. If you do not run RENW, 
the program will run “in the background” when you run BILB.
The frequency with which you should run RENW will depend on a number of factors including your billing 
frequency and the volume of transactions in your warehouse. You can run the program daily, weekly, at the 
end of each month or whenever required. Each time that you run it, RENW will update the billing history of all 
items that have had activity in ENOR (orders and transfers), RELO or ENAJ since the last time that you ran 
RENW. 
1 Key in RENW and press Enter. There is no screen or input parameters for this program and you cannot 
specify a customer.
NOTE RENW can be set up as a cron job in Unix to run automatically every night, 
every week or any other frequency that you require. If you set up RENW as a cron 
job, there is no need to run RENW on demand.

BASIC BILLING SETUP
Changing Renewal Storage Rates
Changing Renewal Storage Rates
When you change your renewal storage rates in IRSP, the new rates automatically apply to new inventory 
renewed after the change was entered. They may or may not apply to existing inventory depending on the 
option that you choose in DBIP (Depositor Billing Profile).
You can override your original vs. current rate on renewals logic at the customer level by setting the Original / 
Current Rate on Renewals flag in IBIP (Item Billing Profile) to the appropriate value. If the item-level value 
differs from the customer-level value, the item-level value will be used.
CHANGING RENEWAL ORIGINAL RATES FOR EXISTING INVENTORY IN ADBD
If you wish to change the renewal original rates for existing inventory (for example, when the product was 
received the renewal rate was $2.00 per case but should have been $1.50 per case), you must use the 
program ADBD (Adjust Billing Data).
When entering your changes in ADBD, the number of inventory levels that you must enter depend upon the 
inventory level that you bill at in DILP. For example, if you have two levels of inventory — item and lot — and 
you bill at the item level, you enter your changes in ADBD once for that item. If, on the other hand, you bill at 
the lot level and you have 10 lots of item 1 in your warehouse, you must enter your changes in ADBD ten 
times — that is, once per lot. 
1 Make sure that the Original or Current Rate on Renewals field in DBIP is set to R for Renewal Original. 
You cannot change renewal storage for existing inventory if this flag has been set to C for Current.
2 Enter ADBD.
3 Key in your customer code and press Enter.
4 If required, key in your item code and press Enter. If your customer has a single inventory level, click on 
Execute Query instead of Enter after entering your item code.
5 If your customer has multiple inventory levels, key in your lot number, production date, etc. and click on 
Execute Query.
Original or Current Rate on 
Renewals field in DBIP Result
C for Current The new rates will be applied to existing inventory as well; that 
is, the next time renewal charges are calculated for an item or 
lot of existing inventory, the system will use the current rate — 
not the original rate.
R for Renewal Original The rates set up in IRSP when the product was received will 
apply to renewal storage charges for existing inventory. If you 
wish to change these rates for existing inventory, you must use 
the program ADBD (Adjust Billing Data).

BASIC BILLING SETUP
Changing Renewal Storage Rates
BILLING AND INVOICING GUIDE 4.2 49

Adjust Billing Data (ADBD) screen showing Billing Block
6 When you have reached your lowest level of inventory for billing purposes, click on Billing Block.
7 Click on Detail Block.

Adjust Billing Data (ADBD) screen showing Billing Detail Block
8 Key in your new rate and press Enter. For example, if your new rate is $2 per pallet, you would enter 2 in 
this field.
The new rate will take effect the next time that the product renews.
9 Press Enter to accept the system-calculated qualifier quantity displayed in the appropriate field (Qualifier 
Quantity, Qualifier Weight, Qualifier Net Weight or Qualifier Cube). 
10 When you finish making your changes, click on Process Adjustments.

BASIC BILLING SETUP
Changing Renewal Storage Rates
11 When the Remark Block is displayed, key in 1 as your line number and press Enter. Then enter your 
remarks and press Enter again. When you finish entering your remarks, click on Return to Main and 
Return to exit.
12 Repeat the above steps for each inventory entity that you wish to change. 
13 When you finish changing your rates, click on Exit to exit.
ADJUSTING BILLING DATA IN ADBD
In ADBD, you can also make changes to the following renewal storage parameters for existing inventory:
 the next renewal date (only required if you are changing your billing frequency; for example, from anniversary monthly to monthly first of month)
 the base renewal date
 the item billing profile code set up in IBIP (for example, you attached the wrong IBIP code to an item and 
you wish to correct the error so that renewal storage will be properly calculated)
The base renewal date is the date that the product was originally received. If you have changed your renewal 
billing frequency from a fixed date renewal (weekly as of Monday, monthly first of the month, monthly last of 
the month) to an anniversary renewal (anniversary monthly, anniversary weekly, daily), you may have to 
adjust this date to make sure that the base renewal date matches the next renewal date.
EXAMPLE — Switch from monthly first of month to anniversary monthly on 06.10.09 (June 10, 2009)
Next Renewal Date = 06.10.09
Last Renewal Date = 05.01.09
Base Renewal Date = 01.25.09
In the above example, you must change your base renewal date from 01.25.09 (the date that the product was 
originally received) to 06.10.09 so that the next renewal date and the base renewal date match.
When entering your changes in ADBD, the number of inventory levels that you must enter depends upon the 
inventory level that you bill at in DILP. For example, if you have two levels of inventory — item and lot — and 
you bill at the item level, you enter your changes in ADBD once for that item. If, on the other hand, you bill at 
the lot level and you have 10 lots of item 1 in your warehouse, you must enter your changes in ADBD ten 
times — that is, once per lot.
1 Enter ADBD.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter. If your customer has a single inventory level, click on Execute 
Query instead of Enter after entering your item code.
4 If your customer has multiple inventory levels, key in your lot number, production date, etc. and click on 
Execute Query.

BASIC BILLING SETUP
Changing Renewal Storage Rates
BILLING AND INVOICING GUIDE 4.2 51

Adjust Billing Data (ADBD) screen showing Billing Block
5 When you have reached your lowest level of inventory, click on Billing Block.
6 Proceed to make any required changes to the following fields:
 Next Renewal Date
 Base Renewal Date (requires running RENW)
 Billing Profile Code
7 When you finish making your changes, click on Process Adjustments.
8 When the Remark Block is displayed, key in your remarks. When you finish entering your remarks, click 
on Return to exit.
9 Repeat the above steps for each inventory entity that you wish to change. 
10 When you finish all your changes, click on Exit to exit.
11 If you changed the base renewal date in step 6, you must run the renewal preprocessor in RENW.

BASIC BILLING SETUP
Changing Renewal Storage Rates

BILLING AND INVOICING GUIDE 4.2 53
EXTRA CHARGE RATER
Overview ............................................................................................................ 54
Understanding the Charge Per Options.......................................................... 55
Assigning Location Billing Codes to Inbound Extra Charges...................... 59
Specifying Extra Charge Restrictions............................................................. 60
Charging for Partial Quantities of Unit-Based SKU’s .................................... 62
Setting Up General Extra Charges in GEXC ................................................... 65
Setting Up Specific Extra Charges in ECHP................................................... 69
Charging by Physical Pallet ............................................................................. 79
Third Party Billing in ECHP .............................................................................. 80
Activating Extra Charges for EDI..................................................................... 81
Confirming an Extra Charge ............................................................................ 82

EXTRA CHARGE RATER
Overview
Overview
Extra charges are miscellaneous type charges such as a bill of lading charge, per order line charge or partial 
pallet charge that apply to a specific receipt or order. Extra charges can be based on either inbound or 
outbound transactions and can apply to a customer, carrier, consignee or shipper or any combination of these 
parties. A charge can apply to one party and be billed to another party; for example, whenever you ship to 
consignee A, an extra charge is created and billed to the customer on the order.
Extra charges are cumulative. When multiple extra charges apply to the same receipt or order, each charge is 
calculated separately and added to the total. For example, if you have an extra charge of $1/pallet each time 
you ship to consignee A and an extra charge of 50 cents/pallet each time you use carrier B, an order of one 
pallet going to consignee A via carrier B would result in a charge of $1.50.
There are two types of extra charges:
 general extra charges set up in GEXC (General Extra Charges)
 specific extra charges set up in ECHP (Extra Charge Profile)
GENERAL EXTRA CHARGES
General extra charges are extra charges such as a bill of lading charge, per order line charge or partial pallet 
charge that are applied automatically to a receipt or order. General extra charges are always treated as 
accessorial charges and appear on the accessorial invoice. 
General extra charges are automatic charges that cannot be adjusted or overridden when processing receipts 
or orders. If you want the capability of manually entering or adjusting extra charges while entering a receipt or 
order, you cannot use general extra charges. Instead, you must set up an extra charge in ECHP (Extra 
Charge Profile).
SPECIFIC EXTRA CHARGES
Specific extra charges are similar to general extra charges in that you use them to generate charges such as 
a bill of lading charge, per order line charge or partial pallet charge. However, specific extra charges differ 
from general extra charges in four important respects:
 they are set up in a profile that is attached to a specific customer or item
 they can be “optional” — that is, require confirmation during receipt or order processing
 they can be manually entered in RF by the RF operator
 if they are inbound charges, they can be set up as either an accessorial charge appearing on the accessorial invoice or as a receipt charge appearing on the warehouse receipt invoice 
There are two factors that determine how the ECHP charge is applied: 
 the restrictions that you enter in ECHP 
 the entity that the ECHP profile is attached to (customer, item, shipper, consignee or carrier)
NOTE You cannot apply extra charges to manual shippers, carriers and consignees. Only shippers, carriers and consignees set up in their respective maintain program (SHIP, CARR, CONS) can trigger an extra charge.

EXTRA CHARGE RATER
Understanding the Charge Per Options
BILLING AND INVOICING GUIDE 4.2 55
During receipt or order processing, the system will look at the restrictions, if any, that you enter in ECHP and 
the entity to which your ECHP profile is attached. If the order or receipt meets all conditions, an extra charge 
will be generated when you create your extra charge batch. 
For example, if you restrict by carrier 1 in ECHP and attach your ECHP profile to all your customers, the 
following will occur. For an inbound charge, the charge will apply to all inbound product carried by carrier 1 
regardless of shipper or customer; for an outbound charge, the charge will apply to all outbound product 
carried by carrier 1 regardless of customer or consignee.
Understanding the Charge Per Options
The charge per defines the way in which an extra charge is applied (to an entire receipt or order, to an item, to 
a receipt or order line, etc.). There are 18 charge per options for extra charges:
COD = COD
DHOC = Document Header for Occurrence
DOCH = Document Header
DOCL = Document Line
DOCT = Document Total
ICTL = Initial Charge Total
IHTL = Initial Handling Total
ISTL = Initial Storage Total
ITCT = Item Count
LCNT = Document Line Count
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4
COD (CASH ON DELIVERY) — CAN ONLY BE ATTACHED TO CUST
With this option, the charge is applied to an entire order. COD has two requirements: first, a charge code 
whose “charge on” and “qualify on” SKU types are based on OCCURRENCE and second, the freight term of 
COD attached to the order header.
DHOC (DOCUMENT HEADER FOR OCCURRENCE) — CAN ONLY BE ATTACHED 
TO CUST
With this option, the charge is applied to an entire receipt or order even if the receipt/order quantity is zero. It 
requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

EXTRA CHARGE RATER
Understanding the Charge Per Options
DOCH (DOCUMENT HEADER) — CAN ONLY BE ATTACHED TO CUST
With this option, the charge is applied to an entire receipt or order. For unit-based SKU’s, the “charge on” 
SKU for the extra charge must match one of the SKU’s in the item’s quantity breakdown before a charge is 
created. For example, if your “charge on” SKU for the extra charge is pallets, AccellosOne 3PL will count the 
number of pallets on the receipt or order. If a particular item does not have pallets in its quantity breakdown 
(for example, it is set up as a CASE/EACH item), it will not be counted by the extra charge rater.
The item’s quantity breakdown must contain the SKU that the extra charge is charging on
EXAMPLE
You have a cased-based extra charge for outbound orders of $1.00 per case and you have the following 
items on your order:
 Item 1 (PALLET/CASE/EACH)
 Item 2 (PALLET)
 Item 3 (PALLET/CASE)
AccellosOne 3PL will charge $1.00 for each case of item 1 and item 3 on the order. There will be no extra 
charge for item 2 product because item 2 does not have cases in its quantity breakdown. 
DOCL (DOCUMENT LINE)
With this option, the charge is applied to each receipt or order line regardless of the product on the receipt or 
order line. For example, if you have 10 receipt lines containing identical product and that product is subject to 
an extra charge, the system will generate 10 extra charges, one for each line.
Item A2
quantity breakdown =
PLT/CASE/EACH
Item A1
quantity breakdown =
PLT/CASE
Item A3
quantity breakdown =
PLT/EACH
You charge on pallets You charge on cases You charge on eaches
No count for this item
because there are no
cases
No count for this item
because there are no
eaches

EXTRA CHARGE RATER
Understanding the Charge Per Options
BILLING AND INVOICING GUIDE 4.2 57
DOCT (DOCUMENT TOTAL) — CAN ONLY BE ATTACHED TO CUST
With this option, the charge is applied to all receipts or orders belonging to a particular customer on an extra 
charge batch. For unit-based SKU’s, the quantity breakdown for all of a customer’s items must be the same; 
that is, all items must have the same quantity breakdown (for example, PALLETS / CASES) and the number 
of units in the quantity breakdown must be identical (for example, 100 cases per pallet). For non-unit based 
SKU’s, this restriction does not apply.
Document total extra charges cannot be billed to a third party such as another customer, a carrier, a shipper 
or a consignee.
ICTL (INITIAL CHARGE TOTAL) — CAN ONLY BE ATTACHED TO CUST
With this option, a single charge is generated based on a percentage of the total initial storage charge plus 
the total initial handling charge of an entire receipt. For example, if the total of both initial storage and initial 
handling is $100 and the charge code has a rate of 0.5, the extra charge will $50 (that is, 50% of the total 
initial charge). ICTL requires a charge code whose “charge on” and “qualify on” SKU types are based on 
INTV.
IHTL (INITIAL HANDLING TOTAL) — CAN ONLY BE ATTACHED TO CUST
With this option, a single charge is generated based on a percentage of the total initial handling charge of an 
entire receipt. For example, if the initial handling total is $100 and the charge code has a rate of 0.5, the extra 
charge will $50 (that is, 50% of the initial handling total). IHTL requires a charge code whose “charge on” and 
“qualify on” SKU types are based on INTV.
ISTL (INITIAL STORAGE TOTAL) — CAN ONLY BE ATTACHED TO CUST
With this option, a single charge is generated based on a percentage of the total initial storage charge of an 
entire receipt. For example, if the initial storage total is $100 and the charge code has a rate of 0.5, the extra 
charge will $50 (that is, 50% of the initial storage total). ISTL requires a charge code whose “charge on” and 
“qualify on” SKU types are based on INTV.
ITCT (ITEM COUNT) — CAN ONLY BE ATTACHED TO CUST
With this option, a single charge is created based on the number of items on the receipt or order. If there are 
duplicate items on the same receipt or order, the item count is not incremented for the duplicates. For 
example, if you receive five items on ten lines, your extra charge will be based on the number of items (five) 
— not the number of lines. ITCT requires a charge code whose “charge on” and “qualify on” SKU types are 
based on OCCURRENCE.
LCNT (DOCUMENT LINE COUNT) — CAN ONLY BE ATTACHED TO CUST
With this option, a single charge is created based on the number of lines on the receipt or order regardless of 
the product on each line. The document line count does not consolidate duplicate items. For example, you 
can have two items on three lines — that is, two of your lines contain the same item — but your line count will 
remain three and the extra charge will be based on this line count.
LCNT requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.

EXTRA CHARGE RATER
Understanding the Charge Per Options
LTCT (LOT COUNT)
With this option, your rate is based on the number of unique level 1 and 2 entities on the receipt or order. In 
the following example, you have four lines but your lot count is three because lines 1 and 4 are identical.
One extra charge is generated and this charge is based on the rate defined in RATE for a quantity of 3. LTCT 
requires a charge code whose “charge on” and “qualify on” SKU types are based on OCCURRENCE.
ULV1 (UNIQUE LEVEL 1)
With this option, a single charge is generated for each unique level one value on a receipt or an order. If there 
are duplicate items on the same receipt or order, they are consolidated and the charge is applied to the 
consolidated item quantities — not the item quantities before consolidation. ULV1 is not available for variable 
quantity breakdown items if you are using a charge code whose SKU type is based on UNIT.
ULV2 (UNIQUE LEVEL 2)
With this option, a single charge is generated for each unique level 1/2 value on a receipt or an order. If there 
are duplicate level 1/2 entities on the same receipt or order, they are consolidated and the charge is applied to 
the consolidated quantities — not the quantities before consolidation. ULV2 is available for standard quantity 
breakdown items without restriction. However, ULV2 is only available for variable quantity breakdown items 
with the following restriction: if the charge code has a SKU type based on UNIT, all inventory entities with the 
same level 2 value must have the same quantity breakdown.
ULV3 (UNIQUE LEVEL 3)
With this option, a single charge is generated for each unique level 1/2/3 value on a receipt or an order. If 
there are duplicate level 1/2/3 entities on the same receipt or order, they are consolidated and the charge is 
applied to the consolidated quantities — not the quantities before consolidation. ULV3 is available for 
standard quantity breakdown items without restriction. However, ULV3 is only available for variable quantity 
breakdown items with the following restriction: if the charge code has a SKU type based on UNIT, all 
inventory entities with the same level 3 value must have the same quantity breakdown.
ULV4 (UNIQUE LEVEL 4)
With this option, a single charge is generated for each unique level 1/2/3/4 value on a receipt or an order. If 
there are duplicate level 1/2/3/4 entities on the same receipt or order, they are consolidated and the charge is 
applied to the consolidated quantities — not the quantities before consolidation. ULV4 is available for 
standard quantity breakdown items without restriction. However, ULV4 is only available for variable quantity 
breakdown items with the following restriction: if the charge code has a SKU type based on UNIT, all 
inventory entities with the same level 4 value must have the same quantity breakdown.
Line Item Lot Number
1. A 101
2. A 201
3. B 101
4. A 101

EXTRA CHARGE RATER
Assigning Location Billing Codes to Inbound Extra Charges
BILLING AND INVOICING GUIDE 4.2 59
SLV2 (SINGLE LEVEL 2)
With this option, a single charge is generated for mixed product received on the same pallet. To activate this 
option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at 
inventory level 2.
SLV3 (SINGLE LEVEL 3)
With this option, a single charge is generated for mixed product received on the same pallet. To activate this 
option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at 
inventory level 3.
SLV4 (SINGLE LEVEL 4)
With this option, a single charge is generated for mixed product received on the same pallet. To activate this 
option, you must set the Single Level Billing flag in DBIP to Y for Yes and you must bill the customer at 
inventory level 4.
Assigning Location Billing Codes to Inbound Extra Charges
For inbound extra charges, the way in which location billing codes are assigned to receipts differs according 
to the charge per. For all charge pers except DOCL (Document Line), if you put-away the same receipt in 
multiple locations and these locations have different location billing codes, the system will be forced to 
allocate the entire receipt to a given location billing code. For example, suppose you have the following 
receipt:
The system will pick the receipt line with the largest quantity (line 2) and assign its location billing code to the 
extra charge.
DOCL (DOCUMENT LINE)
If you put-away the same line in multiple locations and these locations have different location billing codes, 
the system will be forced to allocate the receipt line to a given location billing code. For example, suppose you 
have the following receipt:
Line
Location Billing Code of 
location Quantity
Location Billing Code 
assigned to receipt
1. ALL 20 CS ???????
2. COOL 30 CS ???????
3. BULK 15 CS ???????
Line
Location Billing Code of 
location Quantity
Location Billing Code assigned to 
receipt line
1. ALL ALL
2. COOL COOL
3. BULK 15 CS ???????

EXTRA CHARGE RATER
Specifying Extra Charge Restrictions
Line 1 is assigned exclusively to locations with the location billing code of ALL and poses no problem. 
Likewise, line 2 is assigned exclusively to locations with the location billing code of COOL and poses no 
problem. However, line 3 is split between locations with the location billing code of BULK and locations with 
the location billing code of FREZ. The system will pick the location with the largest quantity and assign its 
location billing code (FREZ) to the entire line.
Specifying Extra Charge Restrictions
You specify your extra charge restrictions by entering the appropriate operand and code in the Customer, 
Consignee, Shipper and Carrier Code fields in GEXC and ECHP. For example, if you specify customer A as 
your restriction, only orders or receipts for customer A will be charged the general extra charge. If you specify 
consignee B as your restriction, all orders going to consignee B regardless of customer will be charged the 
general extra charge.
You can specify restrictions in more than one field and an extra charge will be generated each time that a 
restriction is met. For example, if you attach an extra charge to customers A and B as well as to consignee C, 
the following will occur:
 when customers A or B ship to consignee D, the extra charge attached to the customer will be generated
 when customers A or B ship to consignee C, two extra charges will be generated — one for the extra 
charge attached to the customer and one for the extra charge attached to the consignee
If there is no restriction for a particular field (for example, the charge applies to all customers), leave the field 
blank.
3. FREZ 30 CS ???????
EXAMPLE 1 (OUTBOUND)
CUST =
CONS =
CARR =
Since there are no customer, consignee or carrier restrictions, one 
charge is generated for each order.
EXAMPLE 2 (OUTBOUND)
CUST = ABC
CONS =
CARR =
One charge is generated for each order belonging to customer 
ABC.
EXAMPLE 3 (OUTBOUND)
CUST = ABC
CONS = 1
CARR =
One charge is generated for each order belonging to customer 
ABC. If the consignee is consignee 1, a second charge is generated for that order.
EXAMPLE 4 (OUTBOUND)
CUST = ABC
CONS = 1
CARR = 999
One charge is generated for each order belonging to customer 
ABC. If the consignee is consignee 1, a second charge is generated for that order. If the carrier is carrier 999, a third charge is generated for that order.

EXTRA CHARGE RATER
Specifying Extra Charge Restrictions
BILLING AND INVOICING GUIDE 4.2 61
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 
(for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 
(for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 
(=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If 
you exceed this limit, AccellosOne 3PL will display an error message. Remove one or 
two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or 
“<“ and “>” in the same field.

EXTRA CHARGE RATER
Charging for Partial Quantities of Unit-Based SKU’s
Charging for Partial Quantities of Unit-Based SKU’s
If you have two or more unit-based SKU types in the item’s quantity breakdown (for example, PALLETS/
CASES or PALLETS/CASES/EACHES) and wish to charge for partial quantities, you have two options:
 you can charge for the Entered Quantity
 you can charge for the Actual Quantity Moved
The entered quantity is the actual number of remaining units. The actual quantity moved is the difference 
between the actual number of remaining units and the number of units that make up a full pallet, case, carton, 
etc. 
For example, if your quantity breakdown for the item is 36 cases per pallet and the order calls for 24 cases 
(.66 pallets), the partial quantity will be 24 if you select the entered quantity option and will be 12 (36 - 24) if 
you select the actual quantity moved option.
There are four pairs of options for defining which SKU’s can be partials and how you wish to count the 
number of units in the partial. 
Actual Quantity Moved
You need 24 cases and you remove 
12 cases from a pallet holding 36
Entered Quantity
You need 24 cases and you build 
the pallet from scratch
NOTE The actual quantity moved is only used if the number of remaining units is 
greater than half a pallet. If the number of remaining units is less than half a pallet, 
AccellosOne 3PL uses the entered quantity regardless of the option that you select.
 RM2A - Entered Qty (2nd SKU)
 RM2R - Actual Qty Moved (2nd SKU)
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/
cases/eaches, cases will be considered partials. 

EXTRA CHARGE RATER
Charging for Partial Quantities of Unit-Based SKU’s
BILLING AND INVOICING GUIDE 4.2 63
You can define multiple partials for the same item. For example, if your quantity breakdown is PALLETS/
CASES/EACHES, you can define a partial as eaches only, cases only or cases and eaches. Each partial SKU 
can have its own charge code and its own rates.
EXAMPLE
Suppose you have the following breakdown for an item:
1 pallet = 4 cases (or 12 eaches)
1 case = 3 eaches
1 each = 1 each
 RM2A - Entered Qty (2nd SKU)
 RM2R - Actual Qty Moved (2nd SKU)
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/
cases, cases will be considered a partial.
 RM3A - Entered Qty (3rd SKU)
 RM3R - Actual Qty Moved (3rd SKU)
Use one of these options if you wish to define a partial as the third SKU in an item’s quantity breakdown.
For example, if your quantity breakdown is pallets/
cases/eaches, eaches will be considered a partial.
 RM4A - Entered Qty (4th SKU)
 RM4R - Actual Qty Moved (4th SKU)
Use one of these options if you wish to define a partial as the fourth SKU in an item’s quantity breakdown. 
For example, if your quantity breakdown is pallets/
cases/cartons/packs, packs will be considered a partial.
 RM5A - Entered Qty (5th SKU)
 RM5R - Actual Qty Moved (5th SKU)
Use one of these options if you wish to define a partial as the fifth SKU in an item’s quantity breakdown. 
For example, if your quantity breakdown is pallets/
cases/cartons/packs/eaches, eaches will be considered a partial.
 RQ2A = Entered Qty (2nd SKU - Use Last Recd 
Qty Bkd)*
 RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty 
Bkd)*
Use one of these options if you wish to define a partial as the second SKU in an item’s quantity breakdown and the item is a variable quantity breakdown 
item.
With these two options, if the quantity received is 
greater than the item's standard quantity breakdown, 
the definition of a full pallet will be based on the 
received quantity from the last confirmed receipt plus 
any manual adjustments that occurred in RFMI since 
the last confirmed receipt.

EXTRA CHARGE RATER
Charging for Partial Quantities of Unit-Based SKU’s
You receive an order for 34 eaches and ship the order as follows:
2 pallets = 24 eaches
3 cases = 9 eaches
1 each = 1 eaches
total = 34 eaches
IGNORE LAST QUANTITY
The Ignore Last Qty option allows you to skip the generation of a charge for partial quantities when picking 
the last remaining inventory entity in a location. For example, suppose your quantity breakdown is 80 cases 
per pallet and you ship out the following orders:
This option is only available for RF picking.
SETTING UP AN EXTRA CHARGE FOR CASE PARTIALS
Your quantity breakdown is PALLETS/CASES and you wish to set up a handling charge that can deal with 
partial quantities of cases.
1 Create a charge code in CHAR for cases. Set the “charge on” and “qualify on” values to cases and set 
the Round Flag to N for No Rounding.
2 Create a record in ECHP for cases. Enter your charge code for cases and set the Value Interpretation 
Description to Entered Qty (2nd SKU) or Actual Qty Moved (2nd SKU).
If your partial SKU is case: If your partial SKU is each:
The extra charge will be based on the following number of 
units:
Entered Qty (2nd SKU) = 3 cases
Actual Qty Moved (2nd SKU) = 1 case (4 - 3)....................
The extra charge will be based on the following number of 
units:
Entered Qty (3rd SKU) = 1 each
Actual Qty Moved (3rd SKU) = 1 each*
*Because entered quantity (1) is less than half a case (3), 
entered quantity = actual quantity moved.
ORDER 
NUMBER
ORDER 
QTY
REMAINING 
QTY RESULT
1 40 40 partial quantity charge generated
2 25 15 partial quantity charge generated
3 10 5 partial quantity charge generated
4 5 0 no charge for this partial quantity

EXTRA CHARGE RATER
Setting Up General Extra Charges in GEXC
BILLING AND INVOICING GUIDE 4.2 65
SETTING UP AN EXTRA CHARGE FOR CASE PARTIALS AND EACH PARTIALS
Your quantity breakdown is PALLETS/CASES/EACHES and you wish to set up a handling charge that can 
deal with partial quantities of cases and eaches.
1 Create a charge code in CHAR for cases. Set the “charge on” and “qualify on” values to cases and set 
the Round Flag to N for No Rounding.
2 Create a charge code in CHAR for eaches. Set the “charge on” and “qualify on” values to eaches and set 
the Round Flag to N for No Rounding.
3 Create a record in ECHP for cases. Enter your charge code for cases and set the Value Interpretation 
Description to Entered Qty (2nd SKU) or Actual Qty Moved (2nd SKU).
4 Create a second record in ECHP for eaches. Make sure that this record is attached to the same extra 
charge profile code as the case record. Enter your charge code for eaches and set the Value Interpretation Description to Entered Qty (3rd SKU) or Actual Qty Moved (3rd SKU).
SETTING UP AN EXTRA CHARGE FOR NON-PARTIAL QUANTITIES
You can also set up an extra charge for non-partial quantities by means of the top SKU rounded down option. 
For example, suppose your quantity breakdown is PALLETS/CASES and you wish to set up a labelling 
charge for each pallet. If you select the top SKU rounded down option and ship 1.25 pallets, AccellosOne 3PL 
will charge for one pallet.
1 Create a charge code in CHAR for pallets. Set the “charge on” and “qualify on” values to pallets and set 
the Round Flag to N for No Rounding.
2 Create a record in ECHP for pallets. Enter your charge code for pallets and set the Value Interpretation 
Description to PRIS (Top SKU Rounded Down).
Setting Up General Extra Charges in GEXC
General extra charges apply to all orders or receipts that meet the criteria that you specify in the Customer 
Code, Carrier Code, Shipper Code and Consignee Code fields. If you leave these fields blank, the general 
extra charge will apply to all customers, carriers, shippers and consignees. As a result, an extra charge will be 
generated for each order or receipt that you process!
FIELD DESCRIPTIONS
Type I = Inbound
O = Outbound
Select I for an inbound extra charge or O for an outbound extra charge.

EXTRA CHARGE RATER
Setting Up General Extra Charges in GEXC
Sequence Number Mandatory
Each general extra charge that you create requires a unique sequence number (1, 2, 3, 4, etc.). 
Charge Code
(defined in CHAR)
Mandatory
Your charge code for the general extra charge.
CAUTION The SKU type that you qualify on and charge on in this charge 
code must match the SKU type of all items to which the general extra charge 
applies. For example, you cannot set up a pallet-based charge code in GEXC 
and apply it to a customer whose items are defined as cases.
Charge per COD = COD
DHOC = Document Header for Occurrence
DOCH = Document Header
DOCL = Document Line
DOCT = Document Total
ICTL = Initial Charge Total
IHTL = Initial Handling Total
ISTL = Initial Storage Total
ITCT = Item Count
LCNT = Document Line Count
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4
See “Understanding the Charge Per Options” on page 55 for further information.
FIELD DESCRIPTIONS

EXTRA CHARGE RATER
Setting Up General Extra Charges in GEXC
BILLING AND INVOICING GUIDE 4.2 67
Customer / Consignee / 
Shipper / Carrier Code
Optional but if no values are entered, the general extra charge will be generated for each receipt or order that you process
See “Specifying Extra Charge Restrictions” on page 60 for further information 
on restricting by customer, consignee, shipper, etc. 
NOTE If you bill shippers, consignees or carriers for certain charges and if 
on occasion you use manual shippers, consignees or carriers, you must enter 
the restriction “(=/)” in the Shipper/Consignee/Carrier Code field to exclude the 
manual account from the batch.
EXAMPLE
Suppose when shipping orders to consignee ABC, you charge a special handling fee. In the Consignee Code field, you must enter the following code: 
“=ABC,(=/)”. 
Bill to CARR = Carrier
CONS = Consignee
CUST = Customer
SHIP = Shipper
The party that will be billed for the charge. If you wish to bill the carrier, consignee or shipper for a charge, that carrier, consignee or shipper must be set 
up as an “invoice only” customer in CUST.
FIELD DESCRIPTIONS

EXTRA CHARGE RATER
Setting Up General Extra Charges in GEXC
PROCEDURE
1 Enter GEXC.
Quantity Based on OTOO = One to One 
OTOZ = One to One - include 0 qty line
PRIS = Top SKU Rounded Down*
RM2A = Entered Qty (2nd SKU) - Ignore Last Qty*
RM2R = Actual Qty Moved (2nd SKU) - Ignore Last Qty*
RM3A = Entered Qty (3rd SKU) - Ignore Last Qty*
RM3R = Actual Qty Moved (3rd SKU) - Ignore Last Qty*
RM4A = Entered Qty (4th SKU) - Ignore Last Qty*
RM4R = Actual Qty Moved (4th SKU) - Ignore Last Qty*
RM5A = Entered Qty (5th SKU) - Ignore Last Qty*
RM5R = Actual Qty Moved (5th SKU) - Ignore Last Qty*
RM2A = Entered Qty (2nd SKU)*
RM2R = Actual Qty Moved (2nd SKU)*
RM3A = Entered Qty (3rd SKU)*
RM3R = Actual Qty Moved (3rd SKU)*
RM4A = Entered Qty (4th SKU)*
RM4R = Actual Qty Moved (4th SKU)*
RM5A = Entered Qty (5th SKU)*
RM5R = Actual Qty Moved (5th SKU)*
RQ2A = Entered Qty (2nd SKU - Use Last Recd Qty Bkd)*
RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty Bkd)*
*DOCL, ULV1, ULV2, ULV3 and ULV4 only
This field allows you to specify the way in which you wish to charge for partial 
quantities. If there are no partial quantities (for example, a bill of lading charge 
that applies to an entire order), use One to One. 
One to One is the most common option and can be used for both unit-based 
SKU’s and weight-based SKU’s. If any partial quantities are involved, the system will round up, round down or perform no rounding depending on the 
option that you specify in the Round Flag field in CHAR (Charge Code). 
See “Charging for Partial Quantities of Unit-Based SKU’s” on page 62 for further information on the entered quantity and actual quantity moved options.
FIELD DESCRIPTIONS

EXTRA CHARGE RATER
Setting Up General Extra Charges in GEXC
BILLING AND INVOICING GUIDE 4.2 69

General Extra Charges (GEXC)
2 Click on Create Record.
3 Key in your type (I for Inbound or O for Outbound) and press Enter.
4 Key in your sequence number for the charge and press Enter.
5 Key in your charge code for the general extra charge and press Enter.
6 Use your pick list to select the appropriate charge per. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on 
Select to select it.
7 If required, key in a customer code in the Customer Code field and press Enter. If the charge is not specific to a particular customer, press Enter to bypass this field.
8 Repeat the above step for the Consignee Code, Shipper Code and Carrier Code fields.
9 In the Bill to field, use your pick list to select the appropriate value. A general extra charge can be billed 
to a customer, carrier, consignee or shipper.
10 In the Quantity Based on field, use your pick list to select the appropriate value.
11 Click on Return to Main to exit create record mode.

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP

General Extra Charges screen showing a BOL extra charge for customer A
12 Click on Exit to exit.
13 If you create your receipts or orders through EDI, refer to “Activating Extra Charges for EDI” on page 83 
for further setup instructions.
Setting Up Specific Extra Charges in ECHP
There are two factors that determine how the ECHP charge is applied: 
 the restrictions that you enter in ECHP 
 the entity that the ECHP profile is attached to (CUST, ITEM, CARR, SHIP, CONS)
Refer to the chart below for sample setups:
How you wish to charge Setup in ECHP ECHP profile attached to
You charge all your customers an extra 
charge when you ship their product via 
carrier A.
Create an extra charge profile and 
restrict on carrier A.
Attach the ECHP profile to all your customers.
You charge an extra charge for shipping 
item 1.
Create an extra charge profile with no 
restrictions.
Attach the ECHP profile to item 1.
You charge an extra charge for shipping 
item 1 to consignee A.
Create an extra charge profile and 
restrict on consignee A.
Attach the ECHP profile to item 1.

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 71
You charge customers A and B an extra 
charge when you ship their product to 
consignee C via carrier D.
Create an extra charge profile and 
restrict on consignee C and carrier D.
Attach the ECHP profile to customers A 
and B.
You charge customers A and B an outbound extra charge when you ship their 
product to consignee C via carrier D and 
an inbound extra charge with no restrictions.
Create an extra charge profile. In the 
Sequence Block, create an outbound 
charge and restrict on consignee C and 
carrier D and create an inbound charge 
with no restrictions.
Attach the ECHP profile to customers A 
and B.
FIELD DESCRIPTIONS
Extra Charge Profile 
Code
Mandatory
Your code for this extra charge profile.
Description Mandatory
Your description for this extra charge profile.
SEQUENCE BLOCK
Type I = Inbound
O = Outbound
Select I for an inbound extra charge or O for an outbound extra charge.
Sequence Number Mandatory
Each extra charge that you create requires a unique sequence number (1, 2, 
3, 4, etc.). 
How you wish to charge Setup in ECHP ECHP profile attached to

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
Charge Code
(defined in CHAR)
Mandatory
Your charge code for the extra charge.
CAUTION The SKU type that you qualify on and charge on in this charge 
code must match the SKU type of all items to which the extra charge applies. 
For example, you cannot set up a pallet-based charge code in ECHP and 
attach it to an item whose quantity breakdown is cases only.
Charge per Mandatory
COD = Cash on Delivery*
DHOC = Document Header for Occurrence*
DOCH = Document Header*
DOCL = Document Line
DOCT = Document Total*
ICTL = Initial Charge Total*
IHTL = Initial Handling Total*
ISTL = Initial Storage Total*
ITCT = Item Count*
LCNT = Document Line Count*
LTCT = Lot Count
ULV1 = Unique Inventory Level 1
ULV2 = Unique Inventory Level 2
ULV3 = Unique Inventory Level 3
ULV4 = Unique Inventory Level 4
SLV2 = Single Level 2
SLV3 = Single Level 3
SLV4 = Single Level 4
CAUTION Charge per options marked by an asterisk (*) can only be 
attached to CUST. If you attach these charge per options to ITEM, no charge 
will be generated. 
See “Understanding the Charge Per Options” on page 55 for further information on these options.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 73
Action Type O = Optional
A = Automatic
If you select O for Optional, the system will prompt you to confirm or cancel 
the charge. If you select A for Automatic, the charges will be generated automatically and you will not be able to cancel or override them. 
CAUTION The optional action type is not available for extra charges generated through a special verify program.
Entry Type Only available if Action Type = O for Optional
E = Entry
C = Confirmation
B = Both
N = None
The flow at which you are prompted to confirm the extra charge. If you select 
E for Entry, the system prompt will appear when you enter the receipt or order. 
If you select C for Confirmation, the system prompt will appear when you confirm the receipt or order. If you select B for Both, the system prompt will 
appear at both entry and confirmation time.
If you select N for None, no manual intervention will be allowed and the 
charge will be generated automatically.
Override Quantity Rules Only available if Action Type = O for Optional
E = Entry
C = Confirmation
B = Both
N = None
This field allows you to override the quantity on which the charge is based. If 
you select E for Entry, you can override the quantity when you enter the 
receipt or order. If you select C for Confirmation, you can override the quantity 
when you confirm the receipt or order. If you select B for Both, you can override the quantity at both entry and confirmation time.
If you do not wish to allow the quantity to be overridden, select N for None.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
ENRE screen showing Override Quantity field
Charge Date Based on B = Batch Creation Date
C = Document Confirmation Date
If you select B for Batch Creation Date, the charge date for the extra charge 
will the date that the extra charge batch was created in BILB. If you select C 
for Document Confirmation Date, the charge date for the extra charge will be 
the date that the receipt or order containing the extra charge was confirmed.
The charge date prints on the accessorial audit report.
Invoice Type E = Extra Billing (only available for inbound charges)
A = Accessorial
This fields allows you to specify the invoice on which the charge appears. If 
you select E for Extra Billing and if you generate a warehouse receipt for the 
customer, the charge will appear on the warehouse receipt. If you select A for 
Accessorial, the charge will appear on the accessorial invoice.
The Extra Billing option is invalid for outbound charges as all outbound 
charges are automatically placed on the accessorial invoice.
Allow RF Entry See “Extra Charge Setup for RF” in the RF Guide.
Allow Charge Profile 
Override in RF
See “Extra Charge Setup for RF” in the RF Guide.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 75
Split Order Charge N = No
Y = Yes
If you select Y for Yes, you can charge for split loads. That is, if an order is 
split into three loads, an extra charge based on three loads would be generated. The following setups are required in ECHP:
 Charge Code = occurrence-based charge set up in CHAR
 Type = Outbound
 Charge per = Document Header
 Split Order Charge = Yes
Flow Process Code 
(FLPR) for RF
See “Extra Charge Setup for RF” in the RF Guide.
Customer / Consignee / 
Shipper / Carrier Code
Optional
See “Specifying Extra Charge Restrictions” on page 60 for further information 
on restricting by customer, consignee, shipper, etc. 
NOTE If you bill shippers, consignees or carriers for certain charges and if 
on occasion you use manual shippers, consignees or carriers, you must enter 
the restriction “(=/)” in the Shipper/Consignee/Carrier Code field to exclude the 
manual account from the batch.
EXAMPLE
Suppose when shipping orders to consignee ABC, you charge a special handling fee. In the Consignee Code field, you must enter the following code: 
“=ABC,(=/)”. 
Hold Code If you specify a hold code in this field, the extra charge will apply only to 
receipt or order lines that have been placed on that hold code. 
For example, if you specify DMG as your hold code and attach your ECHP 
profile to the item 001, an extra charge will be generated for each receipt and/
or order line containing item 001 that has been placed on the DMG hold.
This field supports two operands for hold codes: “=” for an exact match of all 
characters and “= + %” for a match of characters entered. For example, “=QA” 
will pick up hold QA only, while “=QA%” will pick up holds QA and QA7.
If required, you can enter multiple hold codes in the Hold Code field. For 
example, if you enter “=QA,=24HR, =DMG”, any product shipped or received 
with any of these holds would be charged. 
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
Load Type Code Only available when charge per = DOCH (Document Header).
If you specify a load type code in this field, the extra charge will apply only to 
receipts or orders that have been assigned to that load type code. For example, if you attach a load type code to a profile, an extra charge will be generated only when the order or receipt has been assigned that load type.
Pallet Code See “Charging by Physical Pallet” on page 79 for further information.
Location Type Code If you enter a location type restriction in this field, the extra charge will apply 
only to receipt or order lines whose final put-away location (for inbounds) or 
final pick or staging location (for outbounds) has been assigned that location 
type.
Bill to CARR = Carrier
CONS = Consignee
CUST = Customer
SHIP = Shipper
The party that will be billed for the charge. If you wish to bill the carrier, consignee or shipper for a charge, that carrier, consignee or shipper must be set 
up as an “invoice only” customer in CUST.
If you wish to bill to an account other than the carrier, consignee, customer or 
shipper, see “Third Party Billing in ECHP” on page 80 for further information.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 77
Quantity Based on OTOO = One to One 
OTOZ = One to One - include 0 qty line
PRIS = Top SKU Rounded Down*
RM2A = Entered Qty (2nd SKU) - Ignore Last Qty*
RM2R = Actual Qty Moved (2nd SKU) - Ignore Last Qty*
RM3A = Entered Qty (3rd SKU) - Ignore Last Qty*
RM3R = Actual Qty Moved (3rd SKU) - Ignore Last Qty*
RM4A = Entered Qty (4th SKU) - Ignore Last Qty*
RM4R = Actual Qty Moved (4th SKU) - Ignore Last Qty*
RM5A = Entered Qty (5th SKU) - Ignore Last Qty*
RM5R = Actual Qty Moved (5th SKU) - Ignore Last Qty*
RM2A = Entered Qty (2nd SKU)*
RM2R = Actual Qty Moved (2nd SKU)*
RM3A = Entered Qty (3rd SKU)*
RM3R = Actual Qty Moved (3rd SKU)*
RM4A = Entered Qty (4th SKU)*
RM4R = Actual Qty Moved (4th SKU)*
RM5A = Entered Qty (5th SKU)*
RM5R = Actual Qty Moved (5th SKU)*
RQ2A = Entered Qty (2nd SKU - Use Last Recd Qty Bkd)*
RQ2B = Actual Qty (2nd SKU - Use Last Recd Qty Bkd)*
*DOCL, ULV1, ULV2, ULV3 and ULV4 only
This field allows you to specify the way in which you wish to charge for partial 
quantities. If there are no partial quantities (for example, a bill of lading charge 
that applies to an entire order), use One to One. 
One to One is the most common option and can be used for both unit-based 
SKU’s and weight-based SKU’s. If any partial quantities are involved, the system will round up, round down or perform no rounding depending on the 
option that you specify in the Rounding Flag field in CHAR (Charge Code). 
See “Charging for Partial Quantities of Unit-Based SKU’s” on page 62 for further information on the entered quantity and actual quantity moved options.
Process Code (IPRO) If you specify a process code in this field, the extra charge will apply only to 
receipt and order lines containing items that have been assigned to that process code.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
Type of Value If you specify a item process code type of value in this field (for example, 
CUBE, HGT, LEN, LEV2, SER, TEMP), the extra charge will apply only to 
receipt and order lines containing items that have been assigned to that process code with that type of value.
NOTE This restriction can be used in conjunction with a process code 
restriction or can be used in stand-alone mode; that is, if you specify CUBE, 
any process code whose type of value has been set to CUBE will generate an 
extra charge.
Exclude System-Populated Process ValuesN = No
Y = Yes
If set to Y for Yes, no catch weight charges will be generated for system-populated process values. If set to N for No, catch weight charges will be generated 
normally for system-populated process values.
A system-calculated process value is a process value created through either 
an EDI receipt creation process or an auto-transfer from inbound to outbound.
Some of the possible scenarios that you might need to deal with are as follows:
 If the customer transfers the process values on a receipt line via EDI, the 
catch weight charges should be excluded. However, if the expected quantities are incorrect forcing the operator to delete the EDI values and rescan, 
the catch weight charges should be included.
 If order allocation selects a full pallet that has not been touched and the 
weights are automatically transferred, the catch weight charges should be 
excluded.
 If a customer service representative is forced to manually enter weights in 
ENRE/ENOR, the catch weight charges should be included.
EDI Version Code These EDI fields allow you to set up an extra charge based on the number of 
occurrences of any EDI Data ID Code value. For example, suppose you set 
up an extra charge attached to the Customer EDI Line Number Data ID Code 
belonging to the 940 transaction set. AccellosOne 3PL will add up the number 
of occurrences of unique Customer EDI Line Number fields for the order or 
receipt and calculate an extra charges.
EDI Transaction Set 
Code (EDTS)
Only available if you enter an EDI version code.
Your EDI Transaction Set Code.
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 79
PROCEDURE
1 Enter ECHP.
EDI Data ID Code (EDDI) Only available if you enter an EDI version code.
Your EDI Data ID Code.
Label Count N = No
Y = Yes
If you select Y for Yes, you can charge by label count. For example, you cartonize your outbound shipments and a single carton can contain multiple 
items. Rather than charge by the item, you wish to generate a single charge 
per carton.
Label count charges are only available for cartonized product. Product is considered cartonized when:
 you perform manual cartonization in RFSC
 you perform system-directed or first level cartonization in RFPK (also known 
as "Pick & Pack")
 you perform second level cartonization for product that cannot be cartonized in RFPK
 you perform manual packing in EPSD
SEQUENCE BLOCK

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP

Extra Charge Profile (ECHP)
2 Click on Create Record.
3 Key in your extra charge profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 Key in your type (I for Inbound or O for Outbound) and press Enter.
6 Key in your sequence number for the charge and press Enter.
7 Key in your charge code for the extra charge profile and press Enter.
8 Use your pick list to select the appropriate charge per. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on 
Select to select it.
9 In the Action Type field, key in the appropriate option (O for Optional or A for Automatic) and press Enter.
10 In the Entry Type field, key in the appropriate option (E for Entry, C for Confirmation, B for Both or N for 
None) and press Enter.
11 In the Override Quantity Rules field, key in the appropriate option (E for Entry, C for Confirmation, B for 
Both or N for None) and press Enter.
12 In the Charge Date Based on field, key in B for Batch Creation Date or C for Document Confirmation 
Date.
13 In the Invoice Type field, key in A for Accessorial or E for Extra Billing and press Enter.
14 Press Enter the required number of times to position your cursor in the Customer Code field.
15 If required, key in a customer code in the Customer Code field and press Enter. If the charge is not specific to a particular customer, press Enter to bypass this field.
16 Repeat the above step for the Consignee Code, Shipper Code and Carrier Code fields.
17 If required, key in a hold code in the Hold Code field and press Enter. If a hold code is not required, press 
Enter to bypass this field.

EXTRA CHARGE RATER
Setting Up Specific Extra Charges in ECHP
BILLING AND INVOICING GUIDE 4.2 81
18 In the Bill To field, use your pick list to select the appropriate value. A general extra charge can be billed 
to a customer, carrier, consignee or shipper.
19 In the Quantity Based on field, use your pick list to select the appropriate value.
20 Do one of the following:
21 Click on Return to Main to exit create record mode.

Extra Charge Profile screen showing extra charge for each receipt line with an action type of Optional 
22 Click on Master Block. Then click on Exit to exit.
23 Attach your extra charge profile to the appropriate item, customer, shipper, consignee or carrier.
If you wish to set up an extra 
charge based on an EDI Data ID 
Code value:
If you do NOT wish to set up an 
extra charge based on an EDI 
Data ID Code value:
a) Key in your EDI version code 
and press Enter.
b) Key in your EDI transaction set 
code and press Enter.
c) Key in your EDI Data ID Code 
and press Enter.
a) Press Enter to bypass the EDI 
Version Code field.
CAUTION Make sure that the charge per for the extra charge is compatible with 
the entity to which it is attached. For example, document total extra charges can only 
be attached to customers; they cannot be attached to items.

EXTRA CHARGE RATER
Charging by Physical Pallet
24 If you create your receipts or orders through EDI, refer to “Activating Extra Charges for EDI” on page 83 
for further setup instructions.
Charging by Physical Pallet
You can generate an inbound/outbound extra charge based on the number of physical pallets entered in the 
Pallet Block of ENRE/ENOR. When you confirm the receipt or order, AccellosOne 3PL will calculate an 
accessorial charge based on the pallet type and the number of shipped pallets. The charge quantity is calculated as follows:
EXAMPLE 1 (OUTBOUND)
ship quantity = 3
receive quantity = 2
charge quantity = 1
EXAMPLE 2 (OUTBOUND)
exchange quantity = 2
charge quantity = 0
EXAMPLE 3 (INBOUND)
ship quantity = 3
receive quantity = 1
charge quantity = 2
You set up your physical pallet charge in ECHP as follows:
 Charge Code = charge code set up in CHAR/RATE for physical pallet charges
 Charge per = DOCUMENT HEADER
 Pallet Code = pallet code in PALL (Pallet Types) using the standard AccellosOne 3PL operands such as 
"=", "(=)", "<", ">", etc.
After setting up your extra charge profile for physical pallet charges, you attach the profile to the appropriate 
customers and/or items.

EXTRA CHARGE RATER
Third Party Billing in ECHP
BILLING AND INVOICING GUIDE 4.2 83
ECHP screen showing outbound pallet charge for CHEP and CPC pallets
Third Party Billing in ECHP
You can bill a third party customer in ECHP by selecting the OVRR (Customer Override) option in the Bill to 
field. A third party customer is a customer other than the standard three accounts on any receipt /order; that 
is, a customer who is not a customer (inventory owner), carrier or shipper/consignee. The third party 
customer must be set up in CUST in order to be charged and can be either a regular or invoice only type 
customer.

EXTRA CHARGE RATER
Activating Extra Charges for EDI
ECHP screen showing third party billing for customer A
Activating Extra Charges for EDI
In order to activate extra charges, you must attache the appropriate special verify program to your workflow 
profile defined in DIFP. For receipt extra charges, the EDEC (EDI Receipt Extra Charge) special verify must 
be attached to the appropriate inbound flow. For order extra charges, the OREC (EDI order Extra Charge) 
special verify must be attached to the appropriate outbound flow.
EDEC and OREC can be attached to any flow following the printing of the last document and receipt/order 
confirmation.
1 Enter DIFP.
2 Retrieve the workflow profile that you wish to modify.
3 Click on In/Out Block.
4 Use your arrow keys to select the appropriate option: Inbound or Outbound.
5 Click on Flow Block to enter the Flow Block.
6 User your arrow keys to select the appropriate inbound or outbound flow.
7 Click on Document Block and Special Verify Block to enter the Special Verification Block.
8 Click on Create Record.
9 Key in your sequence number for the special verify and press Enter.
10 Key in the appropriate special verify (OREC or EDEC) and press Enter.

EXTRA CHARGE RATER
Confirming an Extra Charge
BILLING AND INVOICING GUIDE 4.2 85
11 Press Enter three times to bypass the remaining fields.

Depositor Workflow Profile screen showing special verify OREC attached to the flow FIPI (Finish Picking)
12 Click on Return to Main and Document Block. Then click on Flow Block, In/Out Block, Master Block and 
Exit to exit DIFP.
Confirming an Extra Charge
If you set the Entry Type field in ECHP to E for Entry, C for Confirmation or B for Both, you will be prompted to 
confirm the extra charge at either the header or line level in ENRE or ENOR. During confirmation, you can 
override the quantity on which the charge is based if you set the Override Quantity Rules field in ECHP to E 
for Entry, C for Confirmation or B for Both.
1 Enter ENRE or ENOR and enter your receipt or order. When you finish entering the header or line information to which the extra charge is attached, the Extra Charge Block will be displayed.

EXTRA CHARGE RATER
Confirming an Extra Charge

ENOR showing Extra Charge Block
2 You have up to four options on this screen:
3 Continue entering your receipt or order in the normal manner.
To cancel an extra charge: Click on Cancel Charge
To restore an extra charge that you have cancelled:Click on Apply Charge
To override the quantity on which the extra 
charge is based: 
Press Enter to position your cursor in the 
Override Quantity field. Then key in your 
override quantity and press Enter. The override quantity is based on the charge on SKU 
code in CHAR (Charge Code).
NOTE If you enter a quantity in one or 
more lines and wish to undo the quantity in all 
lines, click on Clear All Lines. Then click on 
Yes when prompted to proceed with the 
update.
To accept the extra charge as is with no 
change:
Click on Exit to exit the Extra Charge Block.

BILLING AND INVOICING GUIDE 4.2 87
BILLING SETUP — ADVANCED TOPICS
Combination Type Charges ............................................................................. 88
Third Party Billing ............................................................................................. 89
Alternate Billing Groups................................................................................... 92
Load Type Charges........................................................................................... 93
Open Lot Receipts ............................................................................................ 94
Overriding Generated Charges on a Receipt ................................................. 98
Seasonal or Special Billing .............................................................................. 99
Taxes ................................................................................................................ 100
Billing by Multiple Units of a SKU ................................................................. 100
Discounts on Initial Storage and Handling Charges.................................... 101
Cross-Dock Billing .......................................................................................... 105
Surcharges ...................................................................................................... 110
Density Rating ................................................................................................. 114
Flat Rate Charges............................................................................................ 115
Hourly Based Charges.................................................................................... 116
Customer Fixed Charges................................................................................ 117
Multi-Currency Billing..................................................................................... 118
Billing Batch Automation ............................................................................... 120
Automatic Pre-Renewal Billing ...................................................................... 121

BILLING SETUP — ADVANCED TOPICS
Combination Type Charges
Combination Type Charges
A combination type charge consists of a flat rate charge together with a linear per unit charge. For example, 
for unloading a non-palletized trailer, you charge a flat rate of $75 plus 10 cents a case. Combination type 
charges can be defined as either single break or multi-break type charges. Consider the following examples:
Example 1
Charge Type = Single break
Charge Definition = Combination
RATE is set up with one flat rate break and one linear break for a total number of two breaks.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total 
of $51.00.
Example 2
Charge Type = Multi-break
Charge Definition = Combination
Rates are the same as those in example 1.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total 
of $101.00.
Example 3
Charge Type = Single break
Charge Definition = Combination
RATE is set up with two flat rate breaks and one linear break for a total number of three breaks.
BREAK 
NUMBER QUANTITY BREAK CHARGE AMOUNT
1 50 100
BREAK 
NUMBER
QUANTITY 
BREAK CHARGE AMOUNT
1 50 100
2 100 150

BILLING SETUP — ADVANCED TOPICS
Combination Type Charges
BILLING AND INVOICING GUIDE 4.2 89
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total 
of $150 and 101 cases will have a charge total of $101.
Example 4
Charge Type = Multi-break
Charge Definition = Combination
Rates are the same as those in example 3.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total 
of $250 (100 + 150). 101 cases will have a charge total of $251 (100 for the first 50 cases, 150 for the next 50 
cases and 1 for the last case).
SETTING UP COMBINATION TYPE CHARGES
Combination type charge require a charge type of Single or Multi and a Charge Definition of C for Combination.
1 Enter CHAR.
2 Create a charge code with a charge type of Single or Multi.
3 In the Charge Definition field, key in C for Combination.
4 Enter the remaining fields in CHAR in the normal manner.
5 When the RATE screen appears, key in your effective date and press Enter.
6 In the Number of Flat Rate Breaks field, key in the number of flat breaks and press Enter.
7 In the Number of Breaks field, key in the total number of breaks (both flat and linear) and press Enter.
For example, if you want two flat breaks and two linear breaks, you would key in 4 in the Number of 
Breaks field.
8 Key in your minimum and maximum charges or press Enter to accept the system defaults.

RATE screen showing example 2 
9 Click on Master Block to exit create mode. Then click on Return to Main and Exit to exit.

BILLING SETUP — ADVANCED TOPICS
Third Party Billing
Third Party Billing
Third party billing occurs when storage costs are paid by a third party — that is, by someone other than the 
owner of the goods. There are four ways of performing third party billing in AccellosOne 3PL:
 you can perform third party billing of initial storage and handling charges on a receipt-by-receipt basis
 you can create an accessorial charge and bill this charge to any customer on your system
 you can set up an invoice only customer so that all invoicing is automatically directed to the third party
 you can set up billing subscription in BTCS
THIRD PARTY BILLING ON A RECEIPT-BY-RECEIPT BASIS
By changing the default value in the Bill to Code field in ENRE, you can bill all initial storage and handling 
charges for that receipt to any other customer set up in AccellosOne 3PL.
1 Enter ENRE.
2 In the Customer Code field, key in the customer whose product you are receiving and press Enter.
3 In the Shipper Code field, key in your shipper code and press Enter.
In the Bill To Code field, the system will display the customer that you entered in step 2. 
4 Key in the customer you wish to bill for the receipt and press Enter or use your pick list (press F10 to 
enter the pick list, F2 to display the customer codes and F3 to select) to select the appropriate customer 
code.
5 Continue to enter your receipt in the normal manner. All charges will be billed to the customer that you 
specified in the Bill To Code field.
CREATING AN ACCESSORIAL CHARGE
By changing the default value in the Bill to Code field in ENAC, you can bill an accessorial charge to any 
customer on your system. These charges can be either attached to a particular order or receipt or entered 
directly in ENAC. 
SETTING UP AN INVOICE ONLY CUSTOMER
An invoice only customer is a customer with no inventory. Typical examples of invoice only customers are 
carriers, shippers, consignees or any other party that you wish to invoice.
1 Set up one billing profile code in DBIP with the Send Invoice To flag set to P for Paying Office. You will 
use this profile for the customer with inventory in your warehouse whose storage charges will be paid by 
a third party.
NOTE Invoice only customers do not have their own rates. The rates used to generate the invoice only customer’s invoices are those of the inventory customer.

BILLING SETUP — ADVANCED TOPICS
Third Party Billing
BILLING AND INVOICING GUIDE 4.2 91
2 Set up a second billing profile in DBIP with the Send Invoice To flag set to C for Customer. You will use 
this profile for the customer with no inventory who will pay the storage charges for the other customer’s 
product.
3 Set up two customer profiles in CUST as follows:
BILLING SUBSCRIPTION
Billing subscription allows you to perform 3PL/4PL billing in which you are outsourcing to other 3PL providers 
or you are performing warehouse services that are to be invoiced to parties other than the customer such as 
the consignee.
For example, suppose because of space limitations you have sub-contracted some of your warehousing to 
another 3PL provider. You would need to establish billing rules and rates for the customer whose inventory is 
being handled by another 3PL provider (normal billing) and you would also need to establish billing rules and 
rates for the 3PL provider that you have sub-contacted out to.
With billing subscription, the system generates two invoices: one for your customer (normal billing) and one 
for the 3PL operator you have sub-contracted out to. The first “invoice” is not actually a real invoice that you 
pay on receipt, but rather a statement of what you will pay the other 3PL provider or what they should be 
charging you.
You maintain third party billing rules in BTCS (Bill to Customer Subscription). BTCS allows you to link a virtual 
customer to a customer owning inventory with the same or different set of billing rules and rates.
In the Header Block, you define your billing subscription defaults: the actual customer who owns the inventory 
(Customer Code), the 3PL operator that you have contracted out to (Bill To Customer Code) and the default 
item billing profile used by the 3PL operator to bill for these services. 
CUSTOMER A (CUSTA) CUSTOMER B (CUSTB)
The inventory is in this customer’s name 
but all billing is sent to a third party (customer B)
This customer has no inventory but pays 
the bills for customer A’s inventory 
 Account Type = W for Warehouse
 Billing Profile Code = code that you set 
up in step 1 with Send Invoice To flag set 
to P
 Paying Office Code = CUSTB
 Account Type = I for Invoice Only
 Billing Profile Code = code that you set 
up in step 2 with Send Invoice To flag set 
to C for Customer
FIELD DESCRIPTIONS (HEADER)
Customer Code Mandatory
The actual customer who owns the inventory.

BILLING SETUP — ADVANCED TOPICS
Third Party Billing
In the Detail Block, you define any overrides to the values in the Header Block. For example, for a particular 
item billing code used by the inventory customer, use a particular item billing code that is not defined in the 
Header Block. If there no overrides, you leave the Detail Block blank.
Bill To Customer Code Mandatory
The 3PL operator that you have contracted out to.
NOTE The bill to customer must be set up in CUST as either a regular or 
invoice only type customer.
Item Billing Profile Code 
(IBIP)
Mandatory
The default item billing profile used by the 3PL operator to bill for these services. 
Bill Event Type Receipt Rater Only receipt charges would apply to the Bill To Customer. It 
means once a receipt is rated for the customer, another set of receipt charges 
based on the Item Billing Profile will be created under the Bill to Customer 
Code.
Renewal Only renewal charges would apply to the Bill to Customer.
Both Both receipt charges and renewal charges would apply to the Bill to 
Customer.
FIELD DESCRIPTIONS (DETAIL BLOCK)
Inventory Billing Profile 
Code
The item billing profile code used by the inventory customer.
Bill To Customer Profile 
Code
The matching item billing profile code used by the bill to customer.
FIELD DESCRIPTIONS (HEADER)

BILLING SETUP — ADVANCED TOPICS
Alternate Billing Groups
BILLING AND INVOICING GUIDE 4.2 93
BTCS screen
Alternate Billing Groups
Alternate billing groups allow you to group items for billing purposes; for example, all items belonging to the 
same product line can be treated as a single entity for billing purposes.
If you use alternate billing, you must apply it to all of a customer’s items. The same customer can have 
multiple alternate billing groups — for example, one group for baked goods, another group for candy and a 
third group for ice cream — but all items must be set up for alternate group billing and attached to a group.
Alternate billing applies to renewal storage only and overrides any renewal storage options that you set up in 
DILP. Alternate billing is not available for initial storage, handling or accessorial charges.
1 Set up a charge code for renewal storage in CHAR and RATE.
2 Set up your renewal storage profile in IRSP.
3 Set up your item billing profile in IBIP.
4 Create a single level or double level code in ITAS. If you do not know how to set up item alternate sort 
codes in ITAS, refer to the Setup Guide for complete instructions.

BILLING SETUP — ADVANCED TOPICS
Load Type Charges

Item Alternate Sorts screen showing code for MEAT
5 Attach the IBIP profile that you created in step 3 to the appropriate alternate inventory reporting code in 
ITAS. 
6 Set up your depositor billing profile in DBIP and attach the ITAS code that you created in the previous 
step to this profile. You enter your ITAS code in the Alternate Billing Group Code field in DBIP.
7 Set up your customer and attach the DBIP profile that you created in the previous step to this customer.
8 Set up your items and attach your item billing code created in IBIP to these items. Then attach your ITAS 
code to the Alternate Reporting Block in ITEM for all items that are part of the alternate billing group.
Load Type Charges
Load type charges are handling charges that apply to a particular load type. You specify your load type for 
inbound charges when receiving product in ENRE and you specify your load type for outbound charges when 
shipping product in ENOR. 
For inbound load type charges, AccellosOne 3PL will generate one charge for each receipt line. For outbound 
load type charges, AccellosOne 3PL will generate one charge for each order. 
To set up load type charges, first you define your load type in LOAD (Load Types). Then you attach the appropriate charge code to the load type in DELO (Depositor Load Type Charges). The charge code for a load type 
charge must be assigned a charge on and qualify on SKU that is based on net or gross weight, cube or 
number of units.

BILLING SETUP — ADVANCED TOPICS
Load Type Charges
BILLING AND INVOICING GUIDE 4.2 95

Load Type screen showing PLT for palletized load

Depositor Load Type Charges screen showing charge code of PLT1 attached to the load type code of 
PLT
If you use IND or UREN invoicing, inbound load type charges print on the warehouse receipt invoice. In all 
other cases, load type charges print on the accessorial invoice.

BILLING SETUP — ADVANCED TOPICS
Open Lot Receipts
Open Lot Receipts
Open lots are lots that remain open for one or more days and allow you to receive the same entity in multiple 
receipts. For example, if item A is defined as an open lot for three days, you can receive the following:
With open lots, the customer will be charged initial storage once for a receipt of 65,000 lbs. instead of three 
times for receipts of 10,000, 25,000 and 30,000 lbs. You use open lots when you wish to offer your customers 
a discount on large volumes of inventory.
Open “lots” need not be defined as actual lots in DILP. They can be any inventory terminology code set up in 
INTE — for example, date code, trailer number, etc. — provided that the following conditions are met:
 your open lot must be defined as inventory level 2 or higher
 you must bill at that inventory level (for example, if your open lot is defined as inventory level 3, you 
must bill at that level)
 all inventory levels must be the same for product to be received on the same open lot
If you produce a warehouse receipt invoice, handling charges for an open lot will appear on each warehouse 
receipt invoice. Initial storage, on the other hand, will always print on the accessorial invoice.
SETTING UP OPEN LOTS IN ITEM
You set up open lots by entering the appropriate number of days in the Number of Days for Open Lots field in 
ITEM. The number entered in this field determines for how many days this entity (the item with these specific 
inventory levels) can be received as an open lot.
If you enter 99 as your number of days, the number of days is set by the operator in ENRE when receiving the 
open lot and not in ITEM. That is, the Close Date in the Line Block of ENRE for the open lot will appear as 
DD.MM.YY or MM.DD.YY depending on your date format and must be manually entered by the operator.
1 Enter ITEM.
2 Retrieve the item that you wish to set up for open lots.
3 Press Enter until your cursor is positioned in the Number of Days for Open Lots field.
4 Key in the number of days that this item can remain open and press Enter.
June 16 item A/ lot 001 10,000
June 17 " 25,000
June 18 " 30,000
65,000

BILLING SETUP — ADVANCED TOPICS
Open Lot Receipts
BILLING AND INVOICING GUIDE 4.2 97

Item screen showing five as the number of days that a lot can remain open
5 Click on Return to Main and Exit to exit.
ENTERING AN OPEN LOT IN ENRE
It is necessary to create a separate receipt each time that a shipment of this open lot arrives at the 
warehouse. 
1 Enter ENRE.
2 Complete the ENRE Header Block as a normal P (Post-receiving) type of receipt.
3 When you reach the Line Block, press F9 (Previous Field) until the cursor is in the Type field. Key in O for 
Open Lot and press Enter.

BILLING SETUP — ADVANCED TOPICS
Open Lot Receipts

ENRE Line Block screen showing an open lot receipt type
4 Continue completing the Line Block until you reach the Close Date field. 
NOTE If you receive a Help Line Message “Inventory entity has been closed, cannot enter ’X’ or ’O’ lines,” this means that the number of days for open lots as defined 
in ITEM has expired. This item can no longer be received as part of an open lot.
Open lot 
type 
receipt line

BILLING SETUP — ADVANCED TOPICS
Open Lot Receipts
BILLING AND INVOICING GUIDE 4.2 99

ENRE Line Block screen showing an open lot receipt type
5 The system may automatically fill in the Close Date field according to the open entity number of days that 
was previously set up in ITEM. If the system-entered date is correct as the last day for receiving this 
entity as part of an open lot, press Enter.
If you need to override the system-entered date, key in the new date over the old one using the same 
date format. Then press Enter.
If DD.MM.YY appears in the Close Date field, key in the closing date using the same date format and 
then press Enter.
6 Complete the remaining Line Block fields in the usual manner.
7 Enter any remaining receipt lines. Then click on Return to Main to exit create mode and Master Block 
and Exit to exit.
CLOSING AN OPEN LOT IN CLOL
When the close date arrives, you must run the program Close Open Lots (CLOL) to generate the charges.
1 Enter CLOL. No input is required in this program as AccellosOne 3PL closes the open lot automatically.
2 If you rate your receipts manually, enter RCRA (Receipt Rater) and proceed to rate the receipt.
The Close 
Date is the 
last day that 
this entity 
can be 
received as 
part of an 
open lot

BILLING SETUP — ADVANCED TOPICS
Overriding Generated Charges on a Receipt
Overriding Generated Charges on a Receipt
You can use the Receipt Type and Line Type fields in ENRE to override certain generated charges on a 
receipt. The following four options are available at both the header and line detail levels: 
 P for Post Receiving (default)
 N for No Charge
 H for Handling Only
 S for Initial Storage Only
However, certain options at the line detail level are not available if they conflict with options at the header 
level. For example, if you select H for Handling at the header level, your only options at the line detail level are 
Handling Only and No Charge; you cannot select Post Receiving because this would conflict with your 
selection at the header level.
Individual receipt lines on the same receipt can be assigned different options. For example, line 1 could be P 
(Post Receiving), line 2 could be N (No Charge) and lines 3 to 9 could be P. AccellosOne 3PL would generate 
normal initial storage and handling charges for lines 1 and 3 to 9 and no charges for line 2. 
RECEIPT 
LINE TYPE DESCRIPTION
P Post Receiving
All normal charges set up in IISP and IHAP for the item apply.
N No Charges
No charges will be generated for the receipt if you enter this option at the 
header level. No charges will be generated for the receipt line if you enter this 
option at the line detail level. This option is useful during implementations 
when you are adding inventory to a new system but do not wish to generate 
any receipt charges.
H Handling Only
Normal handling charges for the receipt will apply. However, no initial storage 
charges will be generated for the receipt if you enter this option at the header 
level and no initial storage charges will be generated for the receipt line if you 
enter this option at the line detail level.
S Initial Storage Only
Normal initial charges for the receipt will apply. However, no handling charges 
will be generated for the receipt if you enter this option at the header level and 
no handling charges will be generated for the receipt line if you enter this 
option at the line detail level.

BILLING SETUP — ADVANCED TOPICS
Seasonal or Special Billing
BILLING AND INVOICING GUIDE 4.2 101
Seasonal or Special Billing
You can attach multiple billing profiles to the same item in order to perform seasonal or special billing. For 
example, suppose you have an item that renews differently based on the demand for the product. You could 
set up two profiles: one that will renew weekly and one that will renew monthly. 
Each time that you receive a new billing entity in that product (for example, item 1, lot A), you will be prompted 
to select a billing profile. After selecting that profile (either weekly or monthly), you will not be prompted again 
for your billing profile code for the duration of the billing entity.
You can assign up to three item billing profile codes to an item.
1 Create the different types of profiles that you need in IBIP (Item Billing Information Profile). 
2 Attach the profile codes created in IBIP to the item in ITEM using your pick list.

Item A1 showing two billing profiles
3 When you receive that particular item and you are rating the receipt, AccellosOne 3PL will prompt you in 
CHRF or RCRA for which profile you wish to use. Select the appropriate profile for that receipt.
NOTE If you receive the same billing entity on a new receipt, you will not be 
prompted for a billing profile. AccellosOne 3PL will automatically use the billing profile 
that you selected when you first received the billing entity.

BILLING SETUP — ADVANCED TOPICS
Taxes
From then on the system will use the same profile for that item (that is, renewals and accessorial billing). 
The profile that you select will remain in effect throughout the duration of the billing entity.
Taxes
AccellosOne 3PL supports the following taxes: the GST (Goods and Services Tax), PST (Provincial Sales 
Tax) and HST (Harmonized Sales Tax). These taxes are defined as single break charge codes in CHAR 
(Charge Codes) and the tax rate is defined in RATE (Depositor Billing Rates).

Depositor Billing Rates screen showing rate for charge code HST
In DBIP you define the default tax for a given customer. In ITEM you define whether the default defined in 
DBIP applies to a particular item. For example, if you define the GST as the default tax code for customer A, 
you have two tax options for each of customer A’s items. You can tax them at the GST rate by assigning them 
the tax code of GST or you exempt them from taxes by assigning them the tax code of NONE.
If all of a customer’s items are taxable, you can use surcharges to calculate the tax. See the section 
“Surcharges” on page 110 for further information.
NOTE If you wish to change the renewal storage charged on an item during a billing entity (that is, after the item has been received), you would have to do so in Adjust 
Billing Data (ADBD). Refer to “Adjusting Billing Data in ADBD” on page 45 for complete instructions.

BILLING SETUP — ADVANCED TOPICS
Billing by Multiple Units of a SKU
BILLING AND INVOICING GUIDE 4.2 103
Billing by Multiple Units of a SKU
AccellosOne 3PL allows you to track inventory in one SKU and bill by a multiple of that SKU. For example, 
suppose you want to track inventory by bags and bill by bags of four. In SKUS (Stock Keeping Units) you 
define a SKU called BGFR (Bags of Four). You set the Base SKU Code field to BAG (your inventory SKU) 
and set the Value field to 4 (the number of bags in a BGFR SKU). 
1 Enter SKUS and set the SKU Code, Value and Base SKU Code fields to the appropriate values.

SKUS screen showing SKU code for BGFR
2 Enter CHAR and set the charge on and qualify on SKU to BGFR (your billing SKU) instead of BAG (your 
inventory SKU). 

BILLING SETUP — ADVANCED TOPICS
Discounts on Initial Storage and Handling Charges

CHAR screen showing Charge on/Qualify on SKU Code fields set to BGFR
3 In the Quantity Breakdown Block of ITEM for the items that you wish to set up for billing by multiple units 
of a SKU, set the Whole/Prorate flag to P for Prorate.
Discounts on Initial Storage and Handling Charges
You can apply discounts to the initial storage and handling charges for a given item by setting up a discount 
profile code in DPRO. For example, if you define a charge percentage of 90 percent in DPRO, initial storage 
charges for the item defined in IISP and handling charges for the item defined in IHAP will by multiplied by .9 
— that is, a 10 percent discount — to arrive at the actual initial storage and handling charges for the item.
There are two ways of applying discounts. You can attach the discount profile code to a particular item in 
ITEM and the discount will be automatically applied whenever you receive that item. Alternatively, you can 
select the appropriate discount profile code when you confirm the receipt and the discount profile code that 
you select will be applied to all items on the receipt.
There are two steps to follow in setting up discounts on initial storage and handling:
 you set up your discount profile code(s) in DPRO
 you set the Item Discount Flag in ITEM to the appropriate value and, if required, attach your DPRO code 
to the item
SETTING UP YOUR DISCOUNT PROFILE CODE IN DPRO
In DPRO you define the effective date and percentage for your discount. When you confirm your receipt, 
AccellosOne 3PL compares the confirmation date to the date in DPRO. If the confirmation date is greater 

BILLING SETUP — ADVANCED TOPICS
Discounts on Initial Storage and Handling Charges
BILLING AND INVOICING GUIDE 4.2 105
than or equal to the date in DPRO, the percentage will be applied to initial storage and handling charges. If 
the confirmation date is less than the date in DPRO, no percentage will be applied to initial storage and 
handling charges.
You can set up multiple effective dates and percentages in DPRO. For example, your percentage for January 
1 could be 90, your percentage for March 1 could be 85 and your percentage for May 1 could be 80. When 
you confirm your receipt, AccellosOne 3PL will select the appropriate percentage.
1 Enter DPRO.
2 Click on Create Record.
3 Key in your discount profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 When the Percentage Block appears, key in your effective date and press Enter.
6 Key in your percentage for this effective date and press Enter.

Discount Profile Code screen showing Percentage Block with a charge percentage of 90
7 Repeat the above two steps for any additional dates and percentages that you required.
8 When you finish setting up your dates and percentages, click on Return to Main to exit create record 
mode.
9 Click on Master Block and Exit to exit DPRO.
SETTING UP YOUR ITEM IN ITEM
In ITEM, you set the Item Discount Flag to the appropriate value and, if required, attach your DPRO code to 
the item.

BILLING SETUP — ADVANCED TOPICS
Discounts on Initial Storage and Handling Charges
10 Enter ITEM.
11 Retrieve the item that you wish to set up for discounting.
FIELD DESCRIPTIONS
Item Discount Flag A = Always
N = No
C = Choose
If you select A for Always, the discount profile code that you enter in the Discount Profile Code field will be automatically applied whenever you receive 
that item. If you select N for No, no item discounting will take place for the 
item.
If you select C for Choose, you will be prompted to select the appropriate discount profile code when you confirm the receipt and the discount profile code 
that you select will be applied to all items on the receipt. The choose option 
requires unique inventory entities. You cannot re-receive the same inventory 
entity; for example, if you receive item A, lot 001 on your first receipt, you cannot receive the same inventory entity on an other receipt and apply a discount 
profile code to it.
Discount Profile Code Only available if you specify A for Always in the Item Discount Flag field.
If you attach a DPRO profile to the item, the percentage specified in the Percent Block of DPRO will be applied to the initial storage charges for the item. 
For example, if you enter 10%, the default initial storage charges for the item 
defined in IISP will be multiplied by .1 to arrive at the actual initial storage 
charges for the item.

BILLING SETUP — ADVANCED TOPICS
Discounts on Initial Storage and Handling Charges
BILLING AND INVOICING GUIDE 4.2 107

Item screen showing item A1 assigned discount profile code 1
12 In the Item Discount Flag field, key in A for Always or C for Choose and press Enter.
13 If you selected A for Always in the previous step, key in your discount profile code and press Enter or 
select it using the pick list.
14 Click on Return to Main to exit modify record mode. Then click on Exit to exit.
SELECTING YOUR DISCOUNT PROFILE CODE DURING RECEIPT 
CONFIRMATION
If your receipts are automatically rated, you select your discount profile code during receipt confirmation. If 
you manually rate your receipts in RCRA, you select your discount profile code in RCRA.
AccellosOne 3PL does not support multiple discount profiles applied to the same inventory entity. As a result 
of this restriction, if you re-receive the same inventory entity on two separate receipts, you will not be 
prompted to select a discount profile code; the discount profile code that you selected the first time will be 
applied to all subsequent receipts of the same inventory entity.
1 Do one of the following:
2 When the Discount Profile Code screen appears, click on Execute Query.
If your receipts are rated 
automatically:
If you manually rate your receipts 
in RCRA:
a) Enter CHRF.
b) Proceed to confirm your receipt 
in the normal manner.
a) Enter RCRA.
b) Proceed to rate your receipt in 
the normal manner.

BILLING SETUP — ADVANCED TOPICS
Cross-Dock Billing

RCRA screen showing pick list of discount profile codes
3 Position your cursor over the discount profile code that you wish to select.
4 Click on Select Code to select the code.
Cross-Dock Billing
Cross-dock billing occurs when you enter a cross-dock receipt in ENRE. You use a cross dock receipt to 
record product that comes into the warehouse for a short period of time. Cross dock product will either be 
taken from the incoming transportation vehicle and be placed directly on the outgoing transportation vehicle 
or it will be placed on the cross dock area of the warehouse from which it will be shipped out within a few 
days. 
Because the product is at the warehouse for such a short time period, it will not be stored in a normal 
warehouse location. Special inbound handling and initial storage charges will apply. 
When you use cross-dock billing, you cannot re-receive the same inventory entity during the cross-dock 
period. For example, if your cross dock period is four days and you receive item A, lot 001 on day 1, you 
cannot receive the same inventory entity — that is, item A, lot 001 — on day 2, 3 or 4.
SETTING UP CROSS-DOCK BILLING
There are three setup programs for cross-dock billing:
 you set up your cross-dock profile in IXDP
 you set the Cross Dock flag to Yes in ITEM for each item that you wish to cross-dock
 you make sure that the Rate Receipt Automatically flag in DBIP is set to N for No

BILLING SETUP — ADVANCED TOPICS
Cross-Dock Billing
BILLING AND INVOICING GUIDE 4.2 109
The cross dock profile defines the initial storage and handling charges for cross dock items, the number of 
days in the cross dock period, the type of storage charged if the product stays in the warehouse longer than 
the cross dock period and which date (receipt or cross dock) the system is to use for renewal storage.
FIELD DESCRIPTIONS
Cross Dock Profile Code Mandatory
Your cross-dock profile code. For example, STD for Standard.
Description Mandatory
Your cross-dock profile code description
Initial Storage Profile 
Code (IISP)
Mandatory
The initial storage profile for the items to which this profile is attached. This 
profile overrides the IISP profile in IBIP (Item Billing Profile).
Handling Profile Code 
(IHAP)
Mandatory
The handling storage profile for the items to which this profile is attached. This 
profile overrides the IHAP profile in IBIP (Item Billing Profile).
Number of Cross Dock 
Days
Mandatory
The number of days that the item will remain in cross-dock.
Type of Billing When 
Cross Dock Period Ends
I = Initial Storage
R = Renewal Storage
If you set to I for Initial Storage, the system will charge initial storage when the 
cross-dock period ends. Initial storage will be based on the initial storage profile attached to IXDP. If you set to R for Renewal Storage, the system will 
charge renewal storage when the cross-dock period ends. Renewal storage 
will be based on the renewal storage profile attached to IBIP (Item Billing Profile).

BILLING SETUP — ADVANCED TOPICS
Cross-Dock Billing
1 Enter IXDP.

Item X-Dock Profile
2 Click on Create Record.
3 Key in your cross-dock profile code and press Enter.
4 Key in a meaningful description and press Enter.
5 Use your pick list function to select the appropriate initial storage profile code. To select a code using a 
pick list, press F8 to display the pick list, use your arrow keys to position your cursor over the appropriate 
code and click on Select Code to select it.
6 Use your pick list function to select the appropriate handling profile code.
7 Key in the number of days that an item is allowed to remain in cross-dock before being charged regular 
storage.
8 In the After Cross Dock Period Process field, key in the appropriate value (I for Initial Storage or R for 
Renewal Storage) and press Enter.
9 In the Renewal Date Flag field, key in the appropriate value (R for Original Receipt Date or X for Dock 
Date) and press Enter.
10 Click on Return to Main.
Renewal Date Flag X = Dock Date
R = Receipt Date
If you set to X for Dock Date, the system will generate renewals based on the 
date the cross-dock period ended. If you set to R for Receipt Date, the system 
will generate renewals based on the original receipt date of the product.
FIELD DESCRIPTIONS

BILLING SETUP — ADVANCED TOPICS
Cross-Dock Billing
BILLING AND INVOICING GUIDE 4.2 111

Item X-Dock Profile
11 Click on Exit.
12 Enter ITEM.
13 Retrieve the item that you wish to set up for cross-dock billing.
14 Press Enter until your cursor is positioned on the Cross Dock field.

ITEM screen showing Cross Dock flag set to Y for Yes
15 In the Cross Dock field, key in Y for Yes and press Enter.

BILLING SETUP — ADVANCED TOPICS
Cross-Dock Billing
16 Click on Return to Main and then Exit to exit.
17 Enter DBIP (Depositor Billing Profile) and make sure that the Rate Receipt Automatically flag is set to N 
for No.
ENTERING A CROSS-DOCK RECEIPT
You enter a cross-dock receipt by entering X as your line type in ENRE. After entering your inventory levels 
and your expected and received quantities in the normal manner, you enter your cross dock profile code in 
the Cross Dock field and make any necessary changes to the Close Date field. 
1 Enter ENRE.
2 Complete the ENRE Header Block as a normal P (Post-receiving) type of receipt.
3 When you reach the Line Block, press F9 (Previous Field) until the cursor is in the Type field. Then key in 
X and press Enter.

ENRE Line Block screen showing a Cross-Dock receipt type
4 Continue completing the Line Block until you reach the Cross Dock field. 
5 In the Cross Dock field, key in the cross dock code and press Enter. 
NOTE You cannot re-receive the same inventory entity during the cross-dock 
period. For example, if your cross dock period is four days and you receive item A, lot 
001 on day 1, you cannot receive the same inventory entity — that is, item A, lot 001 
— on day 2, 3 or 4.
Cross 
Dock type 
receipt line

BILLING SETUP — ADVANCED TOPICS
Surcharges
BILLING AND INVOICING GUIDE 4.2 113

ENRE Line Block screen showing a Cross Dock receipt type
6 The system automatically populates the Close Date field. If the system-entered date is correct as the last 
day for billing this entity at the cross dock rate, press Enter to accept. (Regular storage rates will apply 
after this date.)
If you need to change the system-entered date, key in the new date over the old using the same date format and press Enter.
7 Complete the remaining Line Block fields in the usual manner.
8 Enter any remaining receipt lines. Then press click on Return to Main to exit create mode.
9 Click on Master Block and Exit to exit.
RATING A CROSS-DOCK RECEIPT
1 Receive and confirm the receipt in the normal manner.
2 When the cross-dock period ends, rate the receipt manually in RCRA (Receipt Rater).
Surcharges
A surcharge is an additional charge that is based on the invoice total. The invoice “total” can be the total 
weight of an invoice, the total cube of an invoice or the total dollar amount of an invoice.
EXAMPLE 1 — Surcharge based on total weight of invoice
Cross Dock 
Profile Code
Last day of 
cross dock 
period. Regular charges 
begin after 
this date.

BILLING SETUP — ADVANCED TOPICS
Surcharges
Your invoice total is $100, your total weight is 42,500 lbs and your fuel surcharge is 5 percent. Your surcharge 
would be 42500 / 100 (CWT) X .05 = 21.25, which would be added to the $100.
EXAMPLE 2 — Surcharge based on total dollar amount of invoice
Your invoice total is $100 and your fuel surcharge is 5 percent. Your surcharge would be 100 X .05 = 5, which 
would be added to the $100.
Surcharges can be based on any SKU type with the following qualifier codes: gross weight, net weight, cube, 
occurrence and invoice total value. You cannot use surcharges for SKU types whose qualifier code is unit, 
hour or value index.
You can set up flat rate surcharges by using a SKU type based on the qualifier code of OCCR for occurrence. 
A flat rate surcharge would be a fixed amount — say, $10.00 — added to each invoice regardless of the 
invoice total.
There are three types of surcharges in AccellosOne 3PL: receipt surcharges, renewal surcharges and accessorial surcharges. The type(s) of surcharge that you can use depend on your invoicing option. 
WORKING WITH MULTIPLE SURCHARGES
You can have up to three surcharges for each invoicing option. Each surcharge can, if necessary, be based 
on a different invoice total. For example, surcharge 1 can be based on the total weight, surcharge 2 can be 
based on the total cube and surcharge 3 can be based on the total dollar amount. 
If you have multiple surcharges and all surcharges are based on the total dollar amount of the invoice, the 
surcharges can be calculated independently of each other or can be based on the original total plus another 
surcharge — that is, a surcharge on a surcharge. If you have multiple surcharges that are NOT all based on 
the total value of the invoice — that is, one is based on weight and one is based on the total dollar value of the 
invoice — each surcharge will be calculated independently of each other.
SETTING UP SURCHARGES
There are three steps to follow in setting up a surcharge.
NOTE Surcharges need not be based on the same value used to calculate the original invoice without the surcharge. For example, you can charge renewal storage by 
the case or by the pallet and then add a fuel surcharge to the invoice total that is 
based on weight.
INVOICING 
OPTION TYPE OF SURCHARGES ALLOWED
IND no restriction on type of surcharge
UALL accessorial surcharges only
UREC accessorial and renewal surcharges only
UREN receipt and accessorial surcharges only

BILLING SETUP — ADVANCED TOPICS
Surcharges
BILLING AND INVOICING GUIDE 4.2 115
1 Check your SKU type in SKUS to make sure that the qualify on value is correct.

SKUS screen showing SKU code for invoice total value

SKUS screen showing SKU code for hundredweight
2 Set up your charge code in CHAR. Your charge type must be either SING or MULT.

BILLING SETUP — ADVANCED TOPICS
Surcharges

CHAR screen showing charge code of SUR1 with a charge on and qualify on SKU type of INVT for 
Invoice Total Value 
3 In RATE make sure that the Exclude from Surcharge Calculations flag is set to No.
4 Set up your depositor billing profile in DBIP. If you are adding two surcharges to the same invoicing 
option, you must set the Inclusive of Previous Surcharge flag to the appropriate value. 
5 If you are adding three surcharges to the same invoicing option, you must set the Inclusive of Previous 
Surcharges flag to the appropriate value. Make sure that the qualifier code of the SKU type attached to 
the charge code is set to Invoice Total Value for all charge codes.
Inclusive flag = No Surcharges are calculated independently of each other.
Inclusive flag = Yes Only available if both surcharges are based on the total dollar 
value of the invoice
Second surcharge is based on invoice total plus amount of first 
surcharge.
Inclusive flag = First Third surcharge is based on invoice total plus amount of first surcharge.
Inclusive flag = Second Third surcharge is based on invoice total plus amount of second 
surcharge.
Inclusive flag = Both Third surcharge is based on invoice total plus amount of first and 
second surcharges.

BILLING SETUP — ADVANCED TOPICS
Surcharges
BILLING AND INVOICING GUIDE 4.2 117

DBIP screen showing two mutually exclusive surcharges for accessorial invoicing
USING SURCHARGES TO CALCULATE TAXES
You can use surcharges to calculate taxes such as the GST and PST provided that all of the customer’s items 
are subject to the tax. If some items are taxable and some items are non-taxable, you cannot use surcharges 
to calculate tax. Instead, you must attach the appropriate tax code to your depositor billing profile and to your 
items. See the section “Taxes” on page 100 for further information.
When you use surcharges to calculate taxes, the tax is based on the total charges at the header level; that is, 
all charges on the invoice. If you wish to calculate charges at the line level (that is, taxes calculated separately 
for each line on the invoice), you must use AccellosOne 3PL’s predefined tax codes: GST, PST, GST1, etc.
1 Make sure that the qualifier code of your SKU type in SKUS is set to Invoice Total Value.
2 Create a charge code for the tax in CHAR and set the Charge on SKU Code and Qualify on SKU Code 
values to your invoice total value SKU code.
3 Create a record for your new charge code in RATE and set the rate to the appropriate percentage (for 
example, 6% for the GST).
4 Attach the charge code that you created in CHAR to your depositor billing profile in DBIP. The charge 
code must be attached to all three surcharge fields: Receipt Surcharge Charge Code, Renewal Surcharge Charge Code and Accessorial Surcharge Charge Code. 
If you are not already using surcharges, your new charge code for taxes should be attached to the first 
receipt, renewal and accessorial surcharge fields. If you are already using surcharges, your new charge 
Inclusive flag = None Third surcharge is calculated independently of first two surcharges.

BILLING SETUP — ADVANCED TOPICS
Density Rating
code for taxes should be attached to the first unused surcharge field and the Inclusive flag for the previous field should be set to Y for Yes. 
For example, if you already have a fuel surcharge attached to the Accessorial Surcharge Charge Code 1 
field, your new charge code for taxes must be attached to the Accessorial Surcharge Charge Code 2 
field. 
5 Make sure that the Tax Code fields in DBIP and ITEM are set to NONE.
Density Rating
The density rater allows you to rate an item based on its density; that is, use a different charge code 
depending on the density of the item. For example, if the density of the item is under 10 lbs. per cubic foot, 
use charge code CHAR-1; if the density of the item is between 10 and 20 lbs. per cubic foot, use CHAR-2, 
etc.
The density of the product is compared to the breaks set up in DECH (Density Charge Codes) and the appropriate charge code is selected. Density is calculated in pounds per cubic foot. The normal rating process then 
continues with the rate being calculated based on the weight breaks in RATE.
EXAMPLE
You receive 1,000 cases of boxed shrimp weighing 25 lbs per case. Case dimensions are 9.5 x 11.25 x 19.5 
inches for a total volume of 1.206 cubic feet. The density is 20.73 lbs. per cubic foot.
When you receive the item shrimp and this item has a charge type of DENS (for density), the system looks up 
the item’s charge code in DECH. The item’s charge code in DECH contains the density weight breaks and the 
corresponding charge codes:
Because the item’s density is 20.73, the charge code of CHAR-2 applies. The system then looks up the 
CHAR-2 record in RATE and calculates the charges.
You can use density rating for any type of charge in AccellosOne 3PL — receipt charges, renewal charges, 
accessorial charges, etc.
SETTING UP DENSITY CHARGES
1 Enter CHAR and create your charge code for density rating. Set the Charge Type Code to DENS and 
then enter your Invoice Type Code. The remaining fields in CHAR are not required for a density charge 
code.
BREAK VALUE CHARGE CODE
10 CHAR-1
15 CHAR-2
25 CHAR-3

BILLING SETUP — ADVANCED TOPICS
Density Rating
BILLING AND INVOICING GUIDE 4.2 119

Charge Code screen showing density type charge code
2 If you have not already done so, create your regular, non-density charge codes for each density break.
3 Exit CHAR and enter DECH.
4 In DECH, key in your density charge code in the Density Charge Code field and press Enter.
5 In the Detail Block, click on Create Record. Then enter the density value and charge code for each density break.

Density Charge Codes screen showing three density breaks
6 When you finish entering your density breaks, click on Return to Main to exit create record mode.
7 Exit DECH and attach your density charge code to the appropriate profile (for example, IISP, IRSP, etc.).
8 Enter ITEM and make sure that the items that density rating applies to have the correct weight and cube.

BILLING SETUP — ADVANCED TOPICS
Flat Rate Charges
Flat Rate Charges
You can set up flat rate charges such as producing a bill of lading, loading/unloading a truck, cleaning up a 
spill, etc. by using the qualifier code of Occurrence. During invoicing, you add the special charge code that 
you created in CHAR to the invoice and the customer is billed for the one-time flat rate charge. 
1 Enter SKUS and create a SKU code called OCCR based on a qualifier code of OCCR (Occurrence).

Stock Keeping Units screen showing SKU type of OCCR for Occurrence
2 Enter CHAR and create your new charge code using OCCR as the SKU type that you will be charging 
on. Set the Charge Type Code to SING (Single Break) and the Charge Definition to F for Flat.

BILLING SETUP — ADVANCED TOPICS
Hourly Based Charges
BILLING AND INVOICING GUIDE 4.2 121

Charge Code screen showing charge code of BOL
3 When you finish setting up your new charge code, you can add it to an invoice as a regular accessorial 
charge.
Hourly Based Charges
You can set up hourly based charges for extra labor, etc. by using the qualifier code of Hour. During invoicing, 
you add the charge code that you created in CHAR to the invoice and the customer is billed for the extra labor 
charges.
1 Enter SKUS and create a SKU code called HR based on a qualifier code of HOUR.
Charge on 
and Qualify on 
SKU’s set 
to OCCR

BILLING SETUP — ADVANCED TOPICS
Hourly Based Charges

Stock Keeping Units screen showing SKU type of HR for Hours
2 Enter CHAR and create your new charge code using HR as the SKU type that you will be charging on. 
Set the Charge Type Code to SING (Single Break) and the Charge Definition to B for Break.

Charge Code screen showing charge code of LAB
3 When you finish setting up your new charge code, you can add it to an invoice as a regular accessorial 
charge.
Charge on and 
Qualify on SKU’s 
set to HR

BILLING SETUP — ADVANCED TOPICS
Customer Fixed Charges
BILLING AND INVOICING GUIDE 4.2 123
Customer Fixed Charges
Customer fixed charges allow you to generate recurring accessorial charges for your customers to cover noninventory fixed rate charges such as rent, administration, labor, etc. For example, you rent out a facility to a 
customer but do not track that customer's inventory. Or you have an administration fee of $500 a week in 
addition to the usual initial, handling and renewal storage charges for a customer's inventory.
Recurring accessorial charges will be generated automatically whenever you create a new accessorial batch 
in BILB. (A cron job in Unix set up by HighJump is required to generate the accessorial charges.) 
You set up your recurring accessorial charges in the Fixed Charges Block of CUST. You can also set them up 
in the stand-alone program CUFC.
FIELD DESCRIPTIONS
Customer Code The customer being charged.
Charge Code Your occurrence-based charge code.
Charge Quantity Usually 1. If you enter a number greater than 1 (for example, 2), two charges 
will be generated instead of one.
Frequency Code Anniversary Weekly - Same Day Next Week
Anniversary Monthly
Daily
Monthly - 1st of Month
Monthly - Last Day of Month
Weekly as of Monday
If you have regular billing periods, the frequency of the charge.
Date Profile Code 
(DAPR)
Optional
Your date profile code if you have irregular billing periods.
Start Date Your start date for the charge.
End Date Optional
If you enter an end date for the charge, the charge will end on that date. If you 
leave this field blank, the charge will continue until you delete the record.

BILLING SETUP — ADVANCED TOPICS
Multi-Currency Billing
CUFC screen showing fixed charge for weekly RENT
Multi-Currency Billing
Multi-currency billing allows you to work in two or more currencies. You define your base or home currency in 
COMP (Company Code) and the currency that you wish to invoice a customer in in DBIP (Depositor Billing 
Profile). In the program CURX (Currency Exchange Rates), you set up your exchange rates for each 
invoicing or non-base currency.
1 You activate multi-currency support by setting the Use Multiple Currencies flag on the Financial tab of 
COMP (Company Code) to Yes and selecting your base currency in the Home Currency Code field.
Remarks Optional
Your remarks for the charge.
FIELD DESCRIPTIONS

BILLING SETUP — ADVANCED TOPICS
Multi-Currency Billing
BILLING AND INVOICING GUIDE 4.2 125
COMP screen showing multi-currency billing activated
2 In CURX (Currency Exchange Rates), you set up your exchange rates for each invoicing or non-base 
currency. 
CURX screen showing exchange rates and effective dates for euro
3 If you set the Update Rate flag to Y for Yes, AccellosOne 3PL will automatically update your rates in 
RATE whenever the exchange rate changes. For example, suppose your base currency in DBIP is Canadian and the Canadian dollar falls by 50% in relation to the US dollar; if you charge 1$ CDN a month for 
storage, a new record will be created in RATE in which the rate is now $1.50 per month.
LOIN (Look Up Invoices) shows two amounts: the amount invoiced to the customer in the customer’s 
currency and the base amount in your company’s currency.

BILLING SETUP — ADVANCED TOPICS
Billing Batch Automation
LOIN screen showing invoice amount in US dollars and base amount in CDN dollars
Multi-currency billing requires a custom invoice document from HighJump.
Billing Batch Automation
Billing batch automation allows you to generate and confirm billing batches in the background on a predetermined schedule. It eliminates the need to manually create and confirm extra charge, renewal, accessorial and 
immediate batches in BILB (Billing Batch).
Billing batch automation requires a cron job set up in Linux.
You activate billing batch automation in COMP by selecting the appropriate option from the Processing Billing 
Batch (BILB) Automatically field. If you leave this field blank, billing batch automation will be deactivated.

BILLING SETUP — ADVANCED TOPICS
Automatic Pre-Renewal Billing
BILLING AND INVOICING GUIDE 4.2 127
COMP screen showing Processing Billing Batch (BILB) Automatically field
Generate All Batches Except DLRE
AccellosOne 3PL will generate batches up to “Generated” status for all batch types except the Daily Invoice 
Register.
Generate All Batches Up To Confirmation
AccellosOne 3PL will generate batches all the way to “Confirmed” status.
Automate Billing Processes by IBIP Invoice Type
For custom use only.
Automatic Pre-Renewal Billing
Automatic pre-renewal billing allows you to automatically generate charge records for your renewal batch in 
the background on a predetermined schedule. Its purpose is to shorten the processing time of a renewal 
batch in BILB by catching and correcting as many billing errors as possible before generating your renewal 
batch at mid-month or at the end of the month.
Charges generated through automatic pre-renewal billing are added to the pre-renewal batch type PRNW. 
This batch type first executes the RENW (Renewal Preprocessor) process and then picks up all billing entities 
whose next renewal date is less than or equal to the current date and creates the necessary charge records 
in the charge table.
Automatic pre-renewal billing does not support the following billing options:
 renewal summarization
 splitting out invoices by alternate reporting type codes

BILLING SETUP — ADVANCED TOPICS
Automatic Pre-Renewal Billing
If required, you can audit pre-renewal batch charges in a d’Amigo report. Should you find errors in the prerenewal batch, you cannot delete it in BILB. However, you can delete the renewal batch.
If you delete a renewal batch containing pre-renewal batch charges, you delete all the newly generated 
charges in the renewal batch plus any pre-renewal batch charges as well.That means that the next renewal 
batch could take longer to generate since the pre-renewal generated charges would need to be re-created.
You activate automatic pre-renewal billing in CUST by setting the Automatic Pre-Renewal Billing flag to Yes. 
You then define your pre-renewal schedule (every night at 11pm, every two days, every week, etc.) in a Linux 
cron job.
You generate your renewal batch normally in 
BILB and pick up all PRNW charges from days 
1, 2 and 3 as well as any new billing entities 
whose next renewal date is less than or equal to 
current system date.
Day 2
Day 3
Batch type PRNW is run again and picks up all 
new billing entities whose next renewal date is 
less than or equal to current system date.
Batch type PRNW is run again and picks up all 
new billing entities whose next renewal date is 
less than or equal to current system date.
Day 1
Day 30
Batch type PRNW is run and picks up all billing 
entities whose next renewal date is less than or 
equal to current system date.
10
1
2
3
4

BILLING SETUP — ADVANCED TOPICS
Automatic Pre-Renewal Billing
BILLING AND INVOICING GUIDE 4.2 129
CUST screen showing Automatic Pre-Renewal Billing field

BILLING SETUP — ADVANCED TOPICS
Automatic Pre-Renewal Billing

BILLING AND INVOICING GUIDE 4.2 131
INVOICING
IND Invoicing ................................................................................................... 132
IND Invoicing With Extra Charges on a Warehouse Receipt ...................... 133
UALL Invoicing................................................................................................ 135
UREC Invoicing ............................................................................................... 137
UREN Invoicing ............................................................................................... 139
UREN Invoicing With Extra Charges on a Warehouse Receipt .................. 141
Generating and Printing the Warehouse Receipt Invoice ........................... 142
Generating and Printing the Accessorial Batch/Invoice ............................. 144
Generating and Printing the Renewal Batch/Invoice................................... 150
Generating and Printing the Extra Charge Batch......................................... 155
Working With Audit Batch Restrictions ........................................................ 160
Running the Daily Invoice Register............................................................... 163
Working With Batches and Invoices ............................................................. 168
Entering Accessorial Bill Later Charges....................................................... 180
Working With Accessorial Bill Immediately Charges .................................. 198
Adding Charges to a Confirmed Receipt ...................................................... 208
Adding Charges to a Confirmed Order ......................................................... 210
Rollup Invoicing .............................................................................................. 212
Billing Audit System ....................................................................................... 216
Invoicing by Warehouse................................................................................. 227
Invoicing by Inventory Level.......................................................................... 234
Reversing Charges on Confirmed Invoices.................................................. 236
Allocating Costs to an Invoice....................................................................... 237

INVOICING
IND Invoicing
IND Invoicing
IND invoicing generates three invoices:
 a warehouse receipt invoice containing receipt and extra charges
 an accessorial invoice containing receipt/order accessorial charges and other accessorial charges
 a renewal invoice containing renewal storage charges
Because IND invoicing generates three separate invoices, each invoice can be generated independently of 
the others. For example, you will generate your warehouse receipt invoice whenever you receive product, you 
can generate accessorial invoices each time that you run BILB (accessorial) and you can generate renewal 
invoices each time that you run BILB (renewal).
ENRE
CHRF
ENOR
CHOF BILB
(renewal)
ENAC
BILB
(accessorial)
Accessorial 
Invoice
receipt/order 
accessorial charges
receipt/order
accessorial and
extra charges
renewal charges
receipt charges such as 
initial storage and handling
handling charges
(outbound)
Renewal Invoice
print invoice
PRRE/PRRM
Warehouse 
Receipt Invoice
receipt and
extra charges
BILB (extra 
charge)
charges created in GEXC 
and ECHP

INVOICING
IND Invoicing With Extra Charges on a Warehouse Receipt
BILLING AND INVOICING GUIDE 4.2 133
QUICK STEPS
1 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the 
batch is correct, confirm it. 
4 Generate your accessorial batch in BILB. It will gather the receipt accessorial charges and extra charges 
that have already been generated and place them in an accessorial batch.
5 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes. 
6 Confirm the batch and print the accessorial invoice.
7 Generate your renewal batch in BILB.
8 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then 
delete the batch in BILB and create a new batch.
9 Confirm the batch and print the renewal invoice.
DETAILED STEPS
1 Refer to “Generating and Printing the Warehouse Receipt Invoice” on page 142 for complete instructions 
on the warehouse receipt.
2 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
3 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
4 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal invoice.
IND Invoicing With Extra Charges on a Warehouse Receipt
If you select a Invoice Type of E for Extra Billing in ECHP, the system will automatically generate the receipt 
extra charges when you confirm the receipt in CHRF (automatic rating) or when you rate the receipt in RCRA 
(manual rating). Therefore, there is no need to generate an extra charge batch in BILB for the receipt extra 
charges because the charges are automatically generated. If you look up the extra charge in ENAC, the 
receipt number for the extra charge preceded by a minus sign will appear in the Reference Description field.

INVOICING
IND Invoicing With Extra Charges on a Warehouse Receipt

ENAC (Bill Later - Enter Charges) screen
QUICK STEPS
1 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your accessorial batch in BILB.
4 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes. 
5 Confirm the batch and print the accessorial invoice.
6 Generate your renewal batch in BILB.
7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then 
delete the batch in BILB and create a new batch.
If your only extra charges are 
receipt extra charges that appear 
on a warehouse receipt:
If you have other extra charges 
as well:
a) Proceed to next step. a) Generate your extra charge 
batch in BILB. 
b) Print the audit report for your 
extra charge batch in BILB. If the 
batch is correct, confirm it. Once 
confirmed, you can no longer 
print the batch.
Negative 
number 
indicates a 
receipt 
extra 
charge

INVOICING
UALL Invoicing
BILLING AND INVOICING GUIDE 4.2 135
8 Confirm the batch and print the renewal invoice.
DETAILED STEPS
1 Refer to “Generating and Printing the Warehouse Receipt Invoice” on page 142 for complete instructions 
on the warehouse receipt.
2 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
3 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
4 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal invoice.
UALL Invoicing
UALL invoicing generates a single invoice for all charges. You normally perform UALL invoicing when you are 
ready to run your renewals. 

INVOICING
UALL Invoicing
QUICK STEPS
1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Generate your renewal batch in BILB.
3 Print the audit report.
4 Confirm and print to VIEW the renewal batch.
5 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the 
batch is correct, confirm it.
6 Generate your accessorial batch in BILB. It will gather the receipt, renewal and extra charges that have 
already been generated and place them in an accessorial batch.
7 Print the audit report and check it against the extra charge audit report (if any). If any charges are incorrect, enter ENAC and make the required changes.
ENRE
CHRF
ENOR
CHOF BILB
(renewal)
ENAC
BILB 
(accessorial)
Accessorial Invoice 
containing all 
charges
all charges
receipt/order
accessorial and
extra charges
receipt charges such as 
initial storage and handling
handling charges
(outbound)
renewal charges
BILB (extra 
charge)
charges created in GEXC 
and ECHP

INVOICING
UREC Invoicing
BILLING AND INVOICING GUIDE 4.2 137
8 Confirm the batch and print the accessorial invoice.
DETAILED STEPS
1 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal invoice.
2 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
3 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
UREC Invoicing
UREC invoicing generates two invoices:
 an accessorial invoice containing receipt, accessorial and extra charges
 a renewal invoice containing renewal storage charges 

INVOICING
UREC Invoicing
QUICK STEPS
1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the 
batch is correct, confirm it.
3 Generate your accessorial batch in BILB. The accessorial batch for UREC invoicing will contain accessorial and receipt charges but no renewal charges.
4 Print the audit report.
5 Confirm the batch and print the accessorial invoice.
6 Generate your renewal batch in BILB. The renewal batch will contain renewal charges only.
ENRE
CHRF
ENOR
CHOF BILB
(renewal)
ENAC
BILB 
(accessorial)
Accessorial Invoice 
containing receipt 
charges
receipt, receipt/
order accessorial and 
extra charges
receipt/order
accessorial and
extra charges
renewal charges
receipt charges such as 
initial storage and handling
handling charges
(outbound)
Renewal Invoice
print invoice
BILB (extra 
charge)
charges created in GEXC 
and ECHP

INVOICING
UREN Invoicing
BILLING AND INVOICING GUIDE 4.2 139
7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. Then 
reprint the batch.
8 Confirm the batch and print the renewal invoice.
DETAILED STEPS
1 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
2 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
3 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal invoice.
UREN Invoicing
UREN invoicing generates two invoices:
 a warehouse receipt invoice containing receipt and extra charges
 an accessorial invoice containing receipt/order accessorial charges and renewal storage charges

INVOICING
UREN Invoicing
QUICK STEPS
1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your renewal batch in BILB.
4 Print the audit report.
5 Confirm and print to VIEW the renewal batch.
6 If you have extra charges set up in GEXC or ECHP, generate your extra charge batch in BILB. If the 
batch is correct, confirm it.
7 Generate your accessorial batch in BILB. The accessorial batch for UREN invoicing will contain accessorial and renewal charges but no receipt charges.
8 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. 
9 Confirm the accessorial batch and print the accessorial invoice.
ENRE
CHRF
ENOR
CHOF BILB
(renewal)
receipt charges such as 
initial storage and 
handling
handling charges
(outbound)
generate renewal 
charges
ENAC
BILB
(accessorial)
Accessorial Invoice 
containing renewal 
charges
renewal and 
receipt/order 
accessorial charges
receipt/order
accessorial and
extra charges
PRRE/PRRM
Warehouse 
Receipt Invoice
receipt and
extra charges
BILB (extra 
charge)
charges created in GEXC 
and ECHP

INVOICING
UREN Invoicing With Extra Charges on a Warehouse Receipt
BILLING AND INVOICING GUIDE 4.2 141
DETAILED STEPS
1 Refer to “Generating and Printing the Warehouse Receipt Invoice” on page 142 for complete instructions 
on the warehouse receipt.
2 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal batch.
3 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
4 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
UREN Invoicing With Extra Charges on a Warehouse Receipt
If you select a Invoice Type of E for Extra Billing in ECHP, the system will automatically generate the receipt 
extra charges when you confirm the receipt in CHRF (automatic rating) or when you rate the receipt in RCRA 
(manual rating). Therefore, there is no need to generate an extra charge batch in BILB for the receipt extra 
charges because the charges are automatically generated. If you look up the extra charge in ENAC, the 
receipt number for the extra charge preceded by a minus sign will appear in the Reference Description field.
Negative 
number indicates a 
receipt extra 
charge

INVOICING
Generating and Printing the Warehouse Receipt Invoice
QUICK STEPS 
1 Confirm in CHRF any receipts that you wish to include in the invoice. If required, rate the receipts in 
RCRA after you confirm them.
2 Print the warehouse receipt invoice in PRRE or PRRM.
3 Generate your renewal batch in BILB.
4 Print the audit report.
5 Confirm and print to VIEW the renewal batch.
6 Generate your accessorial batch in BILB. The accessorial batch for UREN invoicing will contain accessorial and renewal charges but no receipt charges.
7 Print the audit report. If any charges are incorrect, enter ENAC and make the required changes. 
8 Confirm the accessorial batch and print the accessorial invoice.
DETAILED STEPS
1 Refer to “Generating and Printing the Warehouse Receipt Invoice” on page 142 for complete instructions 
on the warehouse receipt.
2 Refer to “Generating and Printing the Renewal Batch/Invoice” on page 150 for complete instructions on 
the renewal batch.
3 Refer to “Generating and Printing the Extra Charge Batch” on page 155 for complete instructions on generating an extra charge batch.
4 Refer to “Generating and Printing the Accessorial Batch/Invoice” on page 144 for complete instructions 
on the accessorial invoice.
Generating and Printing the Warehouse Receipt Invoice
You can print a warehouse receipt invoice from two programs: PRRM (Print Documents for Specific Receipts) 
or PRRE (Print Receiving Documents - All). You use PRRM if you know the receipt numbers of the receipts 
that you wish to invoice. You use PRRE if you wish to invoice multiple receipts that you will select based on 
certain criteria; for example, all receipts received on a certain date, all receipts from a specific customer, etc. 
If your only extra charges are 
receipt extra charges that appear 
on a warehouse receipt:
If you have other extra charges 
as well:
a) Proceed to next step. a) Generate your extra charge 
batch in BILB. 
b) Print the audit report for your 
extra charge batch in BILB. If the 
batch is correct, confirm it. Once 
confirmed, you can no longer 
print the batch.

INVOICING
Generating and Printing the Warehouse Receipt Invoice
BILLING AND INVOICING GUIDE 4.2 143
In this procedure, you will print the warehouse receipt invoice from PRRM. If you wish to print it from PRRE, 
refer to your Operations 1 Guide for complete instructions.
1 Enter your receipt in ENRE.
2 Add any accessorial or extra charges to the receipt if required.
3 Confirm the receipt in CHRF. If required, rate the receipt in RCRA.
When you confirm a receipt, all receipt charges are loaded into ENAC. In this program, you can modify or 
delete any charge as required.
4 Enter PRRM.

Print Documents for Specific Receipts (PRRM)
5 Position your cursor beside the document that you wish to print.
6 Click on Receipt Block.
7 Press Enter once to position your cursor in the Receipt Number field.
8 Key in your receipt number and press Enter.

Print Documents for Specific Receipts (PRRM) screen showing receipt 1149
9 If you have additional documents to print, key in their receipt numbers and press Enter.
10 Click on Execute Query.
11 Click on Print Block.

INVOICING
Generating and Printing the Accessorial Batch/Invoice
12 Key in your printer code and press Enter or select it using the pick list. To select a code using the pick list, 
press F10 and then click on Execute Query to display your pick list of available printers. Use your arrow 
keys to position the cursor beside the print that you wish to select and then click on Select Code to select 
it. If you use UALL or UREC invoicing, print to VIEW the warehouse receipt.
13 Click Ok. 
Generating and Printing the Accessorial Batch/Invoice
You can generate an accessorial batch at any time and as often as required — for example, daily, weekly, 
monthly, twice a day, whenever you receive or ship, etc. Each time you generate a batch, all accessorial 
charges that have accumulated in ENAC since the confirming and printing of your last invoice will be placed 
in a batch and assigned a batch number by the system. 
If you are performing UALL invoicing, the accessorial invoice may contain receipt and renewal charges as 
well. If you are performing UREC invoicing, the accessorial invoice may contain receipt charges but no 
renewal charges; if you are performing UREN invoicing, the accessorial invoice may contain renewal charges 
but no receipt charges. 
The following conditions must be met before you can place a charge on an accessorial batch:
 if the accessorial charge is attached to a particular receipt, the receipt must be confirmed and rated
 if the accessorial charge is attached to a particular order, the order must be confirmed
 If accessorial authorization is activated in your system, the accessorial charge must be authorized in 
OAUD (Accessorial Charges Authorization Audit) and ACAU (Accessorial Authorization)
GENERATING THE ACCESSORIAL BATCH IN BILB
1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing accessorial batches

INVOICING
Generating and Printing the Accessorial Batch/Invoice
BILLING AND INVOICING GUIDE 4.2 145
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line 
above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all accessorial charges that were entered up to and including the cut-off date will be 
included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be 
the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing accessorial batch restrictions
8 Proceed to specify restrictions on the charges you wish to place on your accessorial invoice. For example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in 
the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 

INVOICING
Generating and Printing the Accessorial Batch/Invoice
EXAMPLES
9 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this 
field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be 
included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
10 In the Bill Profile Code field, key in your billing profile code restrictions and press Enter or press Enter 
with this field blank for no restrictions. 
If you enter billing profile code restrictions in this field, only charges for items that meet the restriction will 
be included in the invoice. If you leave this field blank, your invoice will include all charges regardless of 
billing profile code.
Billing profile codes are set up in DBIP (Depositor Billing Profile) and assigned to the customer.
11 In the Accessorial Date field, key in your date restrictions and press Enter or press Enter with this field 
blank for no restrictions. You must enter your date restrictions in YYYY.MM.DD format.
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 
(for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 
(for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 
(=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If 
you exceed this limit, AccellosOne 3PL will display an error message. Remove one or 
two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or 
“<“ and “>” in the same field.

INVOICING
Generating and Printing the Accessorial Batch/Invoice
BILLING AND INVOICING GUIDE 4.2 147
If you enter a date in this field, only those accessorial charges with a Date to Charge date that meets the 
date restriction that you specify will be generated. If you leave this field blank, all accessorial charges 
regardless of their Date to Charge value will be generated.
12 In the Invoice Type field, key in your invoice type restrictions and press Enter or press Enter with this field 
blank for no restrictions.
If you enter invoice type restrictions in this field, only charges that meet the restriction will be included in 
the invoice. If you leave this field blank, your invoice will include all charge codes. In order to use this 
restriction, you must have invoice types set up in INTP (Invoice Types).
13 In the Charge Code field, key in your charge code restrictions and press Enter or press Enter with this 
field blank for no restrictions. 
If you enter charge code restrictions in this field, only charges that meet the restriction will be included in 
the invoice. If you leave this field blank, your invoice will include all charge codes.

Billing Batch (BILB) screen showing a batch being generated for BF (Blast Freezing) charges
14 In the Source Flag field, key in your source flag restrictions and press Enter or press Enter with this field 
blank for no restrictions. 
The Source Flag field allows you to specify the source or sources of the charges that you wish to include 
in the invoice. If you leave this field blank, your invoice will include all charges regardless of their source. 
BILB supports the following types of charges:
R Receipt charges entered in ENRE or generated automatically in IISP (Initial Storage Profile)
O Order charges entered in ENOR 
NOTE Any restrictions that you enter in this field will operate within the cut-off date 
that you defined in the Create Date field in the Main Block of BILB. For example, you 
can specify Jan 1/05 as your cut-off date — that is, no charges later than that date — 
and you can specify > Dec 1/04 as your Accessorial Date restriction. This would 
result in a batch of all charges created between Dec 1/04 and Jan 1/05.

INVOICING
Generating and Printing the Accessorial Batch/Invoice
E Extra charges generated automatically in GEXC (General Extra Charges) or ECHP (Extra Charge 
Profile)
X Renewal charges created when a renewal batch is generated
A Maximum/minimum charges charged when the actual charge is less than the minimum charge or 
greater than the maximum charge
S Accessorial charges entered through ENAC
F Freight charges created in A1 Transport
15 If invoicing by inventory level is activated in CUST, you can key in any inventory level restrictions in the 
Billing Level 1/2/3 fields and press Enter. For example, if you bill by level (lot number) and you wish to 
generate a batch for lot 123 that you received last week, key in =123 in the Billing Level 2 field.
16 Click on Generate Batch. 
PRINTING THE ACCESSORIAL AUDIT
The accessorial audit shows each charge that will appear on the invoice. The purpose of this report is to allow 
you to verify all charges before confirming and printing the final invoice.
Refer to “Working With Audit Batch Restrictions” on page 160 for further information on audit reports.
1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 116 with a status of Generated
5 Select Print Audit from the Action dropdown list.

INVOICING
Generating and Printing the Accessorial Batch/Invoice
BILLING AND INVOICING GUIDE 4.2 149

Billing Batch (BILB) screen showing print audit restrictions for accessorial audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your print audit restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will 
be displayed.
CONFIRMING THE BATCH AND PRINTING THE ACCESSORIAL INVOICE
If all the charges on the accessorial audit report are correct, you are ready to confirm the batch and print the 
invoice. If you wish to make changes to the batch before confirming it, see the section “Deleting and 
Modifying Charges on a Confirmed Batch” on page 171. 
1 Enter BILB.
2 Select Accessorial Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
NOTE If you specify a minimum dollar value in the Threshold Ancillary Charge 
Code field in DBIP (Depositor Billing Profile), no accessorial invoice will be printed if 
the minimum value for a particular customer has not been reached.

INVOICING
Generating and Printing the Renewal Batch/Invoice

Billing Batch (BILB) screen showing batch 116 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the 
pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.
Generating and Printing the Renewal Batch/Invoice
Each time that you generate a renewal batch, all renewal charges that have accumulated in ENAC since the 
confirming and printing of your last invoice will be placed in a batch and assigned a batch number by the 
system.
There are four steps to follow in generating and printing a renewal invoice:
 generate the batch
 print the audit report
 confirm the batch
 print or print to VIEW the invoice 
BEFORE YOU BEGIN
 Make sure that there are no open or incomplete renewal batches in BILB for the customer that you are 
going to invoice. If there are, delete or confirm the old batch before you generate a new batch.
 It is recommended that you run RENW (Renewal Preprocessor) at least once before generating your 
renewal batch. 
TIP For best results, it is recommended that you confirm any orders and receipts 
that have been received or shipped before the cut-off date, but are still open. For 
example, if your cut-off date is the third Friday of each month, make sure that any 
orders shipped or receipts received during the billing period have been confirmed. 
Then run a suitable inventory report. A suitable inventory report is any report showing 
all inventory levels used in billing, the product’s weight (if you bill by weight) or the 
product’s SKU (if you bill by pallet, case, etc.). By following these two steps, it is easy 
to resolve any renewal billing discrepancies.

INVOICING
Generating and Printing the Renewal Batch/Invoice
BILLING AND INVOICING GUIDE 4.2 151
GENERATING A RENEWAL BATCH IN BILB
1 Enter BILB.
2 Select Renewal Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing renewal batches
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line 
above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all inventory with a next renewal date that falls on or before this date will be included in 
the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting 
date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

INVOICING
Generating and Printing the Renewal Batch/Invoice

Billing Batch (BILB) screen showing renewal batch restrictions
8 Proceed to specify restrictions on the charges that you wish to place on your renewal invoice. For example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in 
the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 
(for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 
(for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 
(=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)

INVOICING
Generating and Printing the Renewal Batch/Invoice
BILLING AND INVOICING GUIDE 4.2 153
9 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this 
field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be 
included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
10 In the Bill Profile Code field, key in your billing profile code restrictions and press Enter or press Enter 
with this field blank for no restrictions. 
If you enter billing profile code restrictions in this field, only charges for items that meet the restriction will 
be included in the invoice. If you leave this field blank, your invoice will include all charges regardless of 
billing profile code.
Billing profile codes are set up in DBIP (Depositor Billing Profile) and attached to the customer.

Billing Batch (BILB) showing batch being generated for customer ABC
11 Click on Generate Batch. 
PRINTING THE RENEWAL AUDIT
The renewal audit shows each charge that will appear on the invoice. The purpose of this report is to allow 
you to verify all charges before confirming and printing the final invoice.
Refer to “Working With Audit Batch Restrictions” on page 160 for further information on audit reports.
1 Enter BILB.
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If 
you exceed this limit, AccellosOne 3PL will display an error message. Remove one or 
two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or 
“<“ and “>” in the same field.

INVOICING
Generating and Printing the Renewal Batch/Invoice
2 Click on Enter Criteria.
3 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing renewal batch 79 with a status of Generated
4 Select Print Audit from the Action dropdown list.

Billing Batch (BILB) screen showing print audit restrictions for renewal audit
5 Select the appropriate option in the Summary or Detail field.
6 Key in a description for your audit report.
7 Proceed to enter your print audit restrictions, if any.
8 When you finish entering your print audit restrictions, click on Print.
9 Key in your printer code and press Enter or select it using the pick list.
10 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will 
be displayed.

INVOICING
Generating and Printing the Extra Charge Batch
BILLING AND INVOICING GUIDE 4.2 155
CONFIRMING THE BATCH AND PRINTING THE RENEWAL INVOICE
If all the charges on the renewal audit report are correct, you are ready to confirm the batch and print the 
invoice. If you wish to make changes to the batch before confirming it, see the section “Deleting and 
Modifying Charges on a Confirmed Batch” on page 171.
1 Enter BILB.
2 Select Renewal Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing renewal batch 79 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the 
pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.
Generating and Printing the Extra Charge Batch
The extra charges discussed in this chapter are outbound extra charges set up in GEXC (General Extra 
Charges) and ECHP (Extra Charge Profile). If you have inbound extra charges set up in ECHP with an 
invoice type of E for Extra Billing or you have added inbound extra charges to a receipt in ENRE, CHRF or 
RCRA, you do not use the procedures in this chapter.

INVOICING
Generating and Printing the Extra Charge Batch
Extra charges print on the accessorial invoice. You must generate and confirm your extra charge batch in 
BILB before you generate and print the accessorial batch/invoice in BILB. As well, the order must be 
confirmed before any charges attached to it can be placed on a batch.
GENERATING AN EXTRA CHARGE BATCH IN BILB
1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch screen showing extra charge batches
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line 
above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all extra charges that have been incurred up to and including the cut-off date will be 
included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be 
the posting date for the charge.
NOTE You can automate the generation, printing and confirmation of extra charge 
batches by running RECH/ORCH as either a stand-alone program or a special verification program. This approach is recommended when all extra charges are automatically invoiced. However, if you use special extra charge logic based on all extra 
charges during a billing period — for example, the tenth and higher bill of lading per 
billing period is free — you cannot run RECH/ORCH. Instead, you must generate an 
extra charge batch in BILB and then manually adjust the charges to be invoiced.

INVOICING
Generating and Printing the Extra Charge Batch
BILLING AND INVOICING GUIDE 4.2 157
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing restrictions for extra charge batch
8 Proceed to enter your restrictions, if any, for the batch. If there are no restrictions for a particular field, 
press Enter with the field blank to bypass the restriction. For example, if you leave the Customer Code 
field blank, your batch will include charges for all customers.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
NOTE BILB supports the following extra charge restrictions: customer code, consignee code and carrier code. Restrictions apply to the selection of orders to be processed, not to the account that will be billed for the charges. For example, if you 
restrict your extra charge batch to customer ABC, any charges associated with customer ABC’s orders will be generated even if they are billed to the carrier or consignee.
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 
(for example, CUST1, CUST111, CUST199, CUST1ABC)

INVOICING
Generating and Printing the Extra Charge Batch
9 When you finish entering your restrictions, click on Generate Batch. 
PRINTING THE EXTRA CHARGE AUDIT
The extra charge audit shows each extra charge that will appear on the invoice. The purpose of this report is 
to allow you to verify all charges before confirming and printing the final invoice. 
Refer to “Working With Audit Batch Restrictions” on page 160 for further information on audit reports.
1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 
(for example, CUST1, CUST111, CUST299, CUST2ABC)
(=CUST1) All customers except customer 1 
(=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If 
you exceed this limit, AccellosOne 3PL will display an error message. Remove one or 
two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or 
“<“ and “>” in the same field.

INVOICING
Generating and Printing the Extra Charge Batch
BILLING AND INVOICING GUIDE 4.2 159

Billing Batch (BILB) screen showing batch 70 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch screen showing print audit restrictions for extra charge audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your print audit restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
When the batch finishes running, your report is printed.
CONFIRMING THE BATCH AND PRINTING TO VIEW THE EXTRA CHARGE 
INVOICE
If all the charges on the Extra Charge Audit report are correct, you are ready to confirm the batch and print the 
invoice. If you wish to make changes to the batch before confirming it, see the section “Deleting and 
Modifying Charges on a Confirmed Batch” on page 171.
1 Enter BILB.
2 Select Extra Charge Rater from the Batch Type dropdown list.

INVOICING
Working With Audit Batch Restrictions
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 70 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in VIEW as your printer code and press Enter.
7 Click Ok. When the batch finishes running, you are ready to generate your accessorial batch.
TROUBLESHOOTING EXTRA CHARGES
If you encounter an error message during batch generation, the status of the batch will read “Generated” even 
though the complete batch was not successfully generated. You can print a partial audit report to check that 
portion of the batch that was successfully generated, but you cannot confirm the batch until the entire batch is 
regenerated successfully.
Working With Audit Batch Restrictions
Audit batch restrictions apply to the accessorial, renewal, extra charge and immediate batches. They allow 
you to summarize the audit report by customer code, inventory level and charge code and make it possible to 
limit the report to a specific customer, inventory level and charge code.
Audit batches together with invoices are stored in the del4/archive directory in Unix. They should be deleted 
when no longer needed in order to save disk space.
Audit batches are stored in the format CC_TTTT_NNNNNN_NNN where CC = company code, TTTT = batch 
type, NNNNNN = batch number and NNN = audit number. For example, W1_RENW_456_12.
NOTE Audit batch restrictions are for reporting purposes only. Unlike the restrictions that you specify when generating a batch, audit batch restrictions do not affect 
the charges on a batch. For example, if you specify customer ABC as your print audit 
restriction, the audit report will show only charges for that customer. However, when 
you confirm the audit in BILB, the confirmed invoice will contain charges for all customers on the batch.

INVOICING
Working With Audit Batch Restrictions
BILLING AND INVOICING GUIDE 4.2 161
Invoices are stored in the format CC_PP_NNNNNN where CC = company code, PP = invoice prefix and 
NNNNNN = batch number. For example, W1_RC_100000827.
FIELD DESCRIPTIONS
Summary or Detail Details
The audit report will show one line for each charge on the batch.
Customer
The audit report will show one line for each customer on the batch.
Customer, Level 1
The audit report will show one line for each customer/level 1 value on the 
batch.
Customer, Level 1/2
The audit report will show one line for each customer/level 2 value on the 
batch.
Customer, Level 1/2/3
The audit report will show one line for each customer/level 3 value on the 
batch.
Customer, Charge Code
The audit report will show one line for each customer/charge code on the 
batch.
Audit Description This description serves to identify the audit when you use the Reprint Archive 
command.
Customer Code If you enter a customer restriction in this field, the audit report will be restricted 
to charges for that customer. If you do not enter a customer restriction in this 
field, the audit report will contain all charges on the batch regardless of customer.
Level 1 Only available if you specify a customer code restriction
If you enter a level 1 restriction in this field, the audit report will be restricted to 
charges for the level 1 value that you enter. If you leave this field blank, the 
audit report will contain all charges regardless of level 1 value.

INVOICING
Working With Audit Batch Restrictions
REPRINTING AN AUDIT BATCH
1 Enter BILB.
2 Retrieve the audit batch that you wish to reprint.
3 Click on Print Archive.
Level 2 If you have a customer code restriction, this field will only be available if the 
customer has two or more inventory levels.
If you enter a level 2 restriction in this field, the audit report will be restricted to 
charges for that level 2 value. If you leave this field blank, the audit report will 
contain all charges regardless of level 2 value.
Level 3 If you have a customer code restriction, this field will only be available if the 
customer has two or more inventory levels.
If you enter a level 3 restriction in this field, the audit report will be restricted to 
charges for that level 3 value. If you leave this field blank, the audit report will 
contain all charges regardless of level 3 value.
Charge Code If you enter a charge code in this field, the audit report will be restricted to 
charges for that charge code. If you leave this field blank, the audit report will 
contain all charges regardless of charge code.
FIELD DESCRIPTIONS

INVOICING
Running the Daily Invoice Register
BILLING AND INVOICING GUIDE 4.2 163

Batch audits window in BILB screen showing two batch audits for batch 82
Audit batches are listed in batch number order. If you wish to resort your query results in audit file 
description or audit number sequence, click on the appropriate button.
4 Double click on the audit batch that you wish to print.
5 When the Select Printer window displays, select your printer from the dropdown list and click Ok.
Running the Daily Invoice Register
The daily invoice register picks up all confirmed invoice revenue that has been generated since the last time 
that the register was run and posts it to the appropriate management and sales reports. If AccellosOne 3PL is 
linked to your accounting system, the daily invoice register will also create your general ledger interface file. 
When the register is run, all confirmed charges in ENAC and ENIN are removed and no longer available in 
these programs. If you wish to look up a charge that was removed from ENAC, you use the program LOAC 
(Look Up Accessorial).
The daily invoice register prints a report showing the following in three separate sections:
 a list of all invoices
 a breakdown of revenue by revenue analysis code — you define your breakdown in the program INRE 
(Invoice Register)
 a breakdown of revenue by general ledger account

INVOICING
Running the Daily Invoice Register
If you do not assign a revenue analysis code to a column in INRE (Invoice Register), any revenue from that 
revenue analysis code will be assigned to the Miscellaneous column in the daily invoice register.
1 Enter BILB.
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing daily invoice registers
4 In the Description field, key in a description for your batch and press Enter.
5 Press Enter to bypass the Attention field.
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all invoices that have been confirmed on or before the cut-off date will be included in the 
batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be the posting 
date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.
8 Click on Generate Batch. 
PRINTING THE DAILY INVOICE REGISTER AUDIT
The daily invoice register audit report shows the invoice number and total charges for each invoice on the 
daily invoice register. The purpose of this report is to allow you to verify all invoices before confirming and 
printing the final daily invoice register.
Refer to “Working With Audit Batch Restrictions” on page 160 for further information on audit reports.
CAUTION If you are unable to confirm the batch because of an error condition, 
that batch will have a status “Begun Generation” or “Begun Confirmation”. You must 
correct the error and then regenerate the batch. DO NOT ATTEMPT TO GENERATE 
A NEW BATCH IF THE CURRENT BATCH IS NOT CONFIRMED AND DO NOT 
ATTEMPT TO DELETE AN UNCONFIRMED BATCH.

INVOICING
Running the Daily Invoice Register
BILLING AND INVOICING GUIDE 4.2 165
1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Daily Invoice Register (BILB) screen showing batch 16 with a status of Generated
5 Select Print Audit from the Action dropdown list.

Billing Batch (BILB) screen showing restrictions for daily invoice register
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will 
be displayed.

INVOICING
Running the Daily Invoice Register
CONFIRMING THE BATCH AND PRINTING THE DAILY INVOICE REGISTER
Depending on your setup, confirming the batch in BILB will create your general ledger interface file or 
populate your database with the updated financial information. 
1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 16 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When prompted to confirm the batch, click on Yes.
7 Key in your printer code and press Enter or select it using the pick list.
8 Click Ok. When the batch finishes running, your daily invoice register is printed.

INVOICING
Running the Daily Invoice Register
BILLING AND INVOICING GUIDE 4.2 167
9 Click Ok.
Daily Invoice Register showing section for renewal storage
REPROCESSING THE FINANCIAL INTERFACE
If you confirm your batch but need to recreate the interface file or repopulate the database with the updated 
financial information, you can use the FINI option (Reprocess Financial Interface).
1 Enter BILB
2 Select Daily Register from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
HighJump, INC. /usr1/del4/work/faxl Page 4 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 1 of 3
Print Date : 04-02-2000 Renewal Storage - Invoice List Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code & Name Total Charges
S-000111 19-01-2000 A Customer A 48643.16
S-000112 19-01-2000 B Customer B 757900.00
S-000113 19-01-2000 C Customer C 179559.64
S-000114 19-01-2000 D Customer D 107.00
S-000115 19-01-2000 E Customer E 2675.00
 ----------
Total Number of Invoices : 5 Total Charges : 988884.80
 ==========
HighJump, INC. /usr1/del4/work/faxl Page 5 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 2 of 3
Print Date : 04-02-2000 Renewal Storage - Revenue Analysis Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
Invoice # Invoice Date Customer Code Total Storage Miscell
S-000111 19-01-2000 A 48643.16 3182.36 0.00 0.00 0.00 0.00 0.00 45460.80
S-000112 19-01-2000 B 757900.00 757900.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000113 19-01-2000 C 179559.64 102879.64 0.00 0.00 0.00 0.00 0.00 76680.00
S-000114 19-01-2000 D 107.00 107.00 0.00 0.00 0.00 0.00 0.00 0.00
S-000115 19-01-2000 E 2675.00 2675.00 0.00 0.00 0.00 0.00 0.00 0.00
 ---------- ---------- ------- ------- ------- ---------- ---------- --------
Totals 988884.80 866744.00 0.00 0.00 0.00 0.00 0.00 122140.80
 ========== ========== ======= ======= ======= ========== ========== 
HighJump, INC. /usr1/del4/work/faxl Page 6 of 13
Invoice Register # : 38 SECTION 2 of 5
 Section Page 3 of 3
Print Date : 04-02-2000 Renewal Storage - G.L. Breakdown Sub Section Page 1 of 1
--------------------------------------------------------------------------------------------------------------------
General Ledger Code & Description Total Charges
G.L. Posting Date : 19-01-2000
104200 Handling 122140.80
123456 General 851632.80
123457 Goods & Services Taxes 15111.20
 ----------
Total for Day 988884.80
 ----------
 ----------
Total for All Days 988884.80
 ==========

INVOICING
Working With Batches and Invoices
5 Select Reprocess Financial Interface from the Action dropdown list.
6 When prompted to confirm reprocessing of the financial interface, click on Yes.
EMAILING OF INVOICES
You can email confirmed invoices from BILB (Billing Batch). Emailing of confirmed invoices must be set up for 
each customer in the configuration program AECS (Automatic Email Setup). In this program, you define the 
directory where you want to store a copy of your emailed invoices, the subject line for your email message 
and your email body text.
Invoices are attached to the email in the form of a PDF file.
AECS screen showing sample setup
1 Enter BILB.
2 Select your batch type from the dropdown list.
3 Select the confirmed invoice that you wish to email.
4 In the Action field, select Email Invoice.
Working With Batches and Invoices
The procedures in this section apply to all batch types in BILB: accessorial invoice, daily invoice register, 
extra charge rater, immediate invoice and renewal invoice.

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 169
REGENERATING A BATCH
If a batch fails to generate successfully, the batch will have a status of BEGUN GENERATION. 
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Select Regenerate from the Action dropdown list.
6 When prompted to regenerate the batch, click on Yes.
REPRINTING AN INVOICE
You can reprint a confirmed invoice as many times as required.
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Select Final Reprint from the Action dropdown list.
6 Key in your printer code and click Ok.
DELETING A BATCH
If the status of a batch is GENERATED or PRINTED, you can delete it if required. When you delete a batch, 
all charges in the batch are released and will be picked up in the next batch that you generate. You use the 
Delete command when you have made a mistake in the generation of your batch and you wish to regenerate 
it.
1 Enter BILB.
2 Select the appropriate batch type from the dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.
5 Click on Delete.
6 When prompted to confirm the deletion, click on Yes.
LOOKING UP A CHARGE ON A BATCH
You look up a charge on a batch by performing a query in ENAC. You can query on the accessorial entry 
number, bill-to code, date to charge, charge code, batch number, renewal date and many other parameters. 
You can also query on a particular receipt or renewal. Receipt information is shown in the Source Reference 
Number field while the renewal date is shown in the Reference Description field.

INVOICING
Working With Batches and Invoices
For example, to query on all charges on receipt 25, you would enter 25 in the Source Reference Number 
field. To query on all renewal charges on a renewal batch, you could enter the date of the batch in the 
Reference Description field or you could enter the batch number in the Renewal Batch Number field. To query 
on all extra charges on a given extra charge batch, you would enter %EXIN Batch <xx> in the Reference 
Description field where xx equals the extra charge batch number.
If the batch has been confirmed and you have run DLRE (Daily Invoice Register), you cannot look up the 
charge in ENAC. Instead, you must look up the charge in LOAC (Look Up Accessorial). Refer to “Looking Up 
All Charges for a Given Item, Level 2/3/4 Value in LOAC” on page 175.
1 Enter ENAC.
2 Click on Enter Criteria.
3 Press Enter until you reach the field that you wish to query on. If you wish to query on the Source Reference Number to look up a particular receipt, you would press Enter to bypass all fields on the first page of 
ENAC. When the second page of ENAC is displayed, you would enter the receipt number in the Source 
Reference Number field. 

ENAC showing second page of this screen
4 Key in your query word or code and click on Execute Query.
ENAC will display all records that meet the criteria that you specify.

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 171

ENAC screen showing an initial storage on receipt 1417
5 When you finish your query, click on Exit to exit.
DELETING AND MODIFYING CHARGES ON A CONFIRMED BATCH
You can delete or modify a charge on a confirmed batch as long as the daily invoice has not been run in 
DLRE. You delete and modify charges by entering ENAC and making the required changes. After making 
your changes, you must reprint the batch by means of the RAUD Selection Code. 
DELETING A CHARGE
When you delete a charge in ENAC, the charge is permanently deleted and cannot be recreated when you 
generate a new batch. Should you delete a charge by mistake, you will have to re-enter it manually in ENAC.
1 Enter ENAC.
2 Look up the accessorial charge that you wish to delete. You can use your Enter Criteria and Execute 
Query buttons to query on the Accessorial Entry Number, Bill To Code, Date to Charge, Reference Number or Charge Code fields.
For example, if you wish to modify all charges on receipt 25, you would enter 25 in the Source Reference 
Number field and click on Execute Query to query.
3 When you find the charge that you wish to delete, press Enter to position your cursor in the Reference 
Description field
4 Click on Delete.
5 Click on Exit.

INVOICING
Working With Batches and Invoices
MODIFYING A CHARGE
1 Enter ENAC. 
2 Look up the accessorial charge that you wish to modify. You can use your Enter Criteria and Execute 
Query buttons to query on the Accessorial Entry Number, Bill To Code, Date to Charge, Reference Number or Charge Code fields.
For example, if you wish to modify all charges on receipt 61, you would enter 61 in the Source Reference 
Number field and click on Execute Query to query.
3 Press Enter until your cursor is positioned on the field that you wish to change.
4 Key in your new value over the old value and press Enter.
5 Click on Return to Main and Exit to exit.
TROUBLESHOOTING RENEWAL INVOICING
The following chart shows some of the more common problems encountered with renewal invoicing.
batch cannot be confirmed Make sure that there are no previous unconfirmed 
batches in BILB. If there are, delete or confirm the previous batch and then confirm the current batch.
missing charges on a 
renewal batch
Check LORE or LOEN to ensure that the product was 
confirmed and rated. 
Make sure that you did not enter restrictions when generating the batch such as all charges later than June 1 or all 
charges except those incurred by Customer X.
Check LOEN to ensure that product should renew.
Check CHAR and RATE to ensure that the charge code 
has been properly set up. If your charge code is correct 
and has been attached to the proper profiles but there 
are no rates in RATE for the charge code, no charges will 
be generated. 
If you are still unable to identify the cause of the missing 
charge, delete the renewal batch in BILB. Then run 
RENW (Renewal Recalculations) to gather any renewal 
charges that were missed. Lastly, regenerate the batch in 
BILB.

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 173
LOOKING UP AN INVOICE IN LOIN
You look up invoices in the program LOIN (Look Up Invoices). For non-receipt charges, a batch must have a 
status of CONFIRMED before you can look up an invoice generated from that batch in LOIN. For receipt 
charges, the receipt must be confirmed and rated before you can look it up in LOIN.
1 Enter LOIN. 
2 Key in your invoice number or receipt number and click on Execute Query. If you do not know the invoice 
number or receipt number, use your Enter Criteria and Execute Query functions to perform a query on 
the values that you know (for example, the batch number, customer code, etc.).

Look Up Invoices (LOIN) screen showing invoice 20
3 Click on Revenue Block to display the revenue breakdown of the invoice.
batch takes too long to run Run RENW (Renewal Recalculations) on a regular basis 
or at least once before you run your renewals.
If you have made a change to a billing profile, the system 
may have to recalculate the billing history of the item and 
this may take much longer than usual. However, the next 
time you run renewals, the batch should take the usual 
amount of time.
If you have made weight adjustments to older lots, the 
system may take longer than usual to run.

INVOICING
Working With Batches and Invoices

Look Up Invoices (LOIN) screen showing Revenue Analysis Block
4 If required, click on G.L. Block to view the revenue by general ledger account.
5 Click on Invoice Block and Exit to exit.
PRINTING AN INVOICE IN LOIN
1 Enter LOIN.
2 Retrieve the invoice that you wish to print.
3 Press Enter. AccellosOne 3PL will display the message “Searching for File.”

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 175

Look Up Invoices screen showing the message “Found Invoice”
4 When the “Found invoice” message appears, key in your printer code and press Enter or use your pick 
list to select it.
5 Click Ok to print.
6 Click on Exit to exit.
LOOKING UP ALL CHARGES FOR A GIVEN ITEM, LEVEL 2/3/4 VALUE IN LOAC
You look up all charges for a given item or level 2/3/4 value in the program LOAC (Look Up Accessorial). This 
program shows the following information about a charge:
 the accessorial entry number and date
 the charge code and amount
 if applicable, the receipt or order number and the line number
 the location billing code, qualifying quantity and SKU, charge on quantity and SKU as well as the rate
For each inventory record retrieved, LOAC shows the total invoiced, the total unbilled and the grand total — 
that is, both invoiced and unbilled.
Records in LOAC are permanent and cannot be deleted except through the program PURA (Purge Accessorial Batch). Refer to “LOAC (Look Up Accessorial)” on page 272 for detailed information on each field in 
LOAC.
1 Enter LOAC.

INVOICING
Working With Batches and Invoices

Look Up Accessorial (LOAC)
2 Key in your customer code and press Enter.
If you wish to look up charges 
not attached to a given item or 
level 2/3/4 value:
If you wish to look up all charges 
for a given item or level 2/3/4 
value:
a) Click on Execute Query.
b) Use your down arrow key to 
scroll to the last record in LOAC. 
c) In the last record, the level 2/3/4 
fields will be blank to indicate 
that the charge is not linked to a 
particular item.
a) Key in the item code and inventory levels that you wish to query 
and click on Execute Query.

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 177

Look Up Accessorial (LOAC) screen showing two charges for item A1, lot 108
3 Click on Accessorial Block to enter the Accessorial Block.
4 Use your arrow keys to position the cursor over the accessorial entry number that you wish to query.
5 Click on Detail Block.

INVOICING
Working With Batches and Invoices

Look Up Accessorial (LOAC) screen showing a receipt charge of 16.00
6 When you finish your query in LOAC, click on Accessl Block and Inventory. Then click on Exit to exit.
USING INVOICE TYPES TO SPLIT OUT ACCESSORIAL CHARGES
You use invoice types in the accessorial billing program BILB (Accessorial Invoicing) to restrict the types of 
charges that will appear on an invoice or to split out the charges on two or more invoices.
For example, you create an invoice type called LAB for Labor Charges in the program INTP (Invoice Type). 
Then you attach this invoice type to one or more charge codes in CHAR (Charge Code). When you enter 
BILB, you specify in the Select Block of this program that you want only charges whose invoice type is LAB to 
be included in the invoice. When you run the program, you will have an invoice restricted to accessorial labor 
charges.
If you do not need to split out your accessorial charges, you create a single invoice type in INTP called NA 
(Not Applicable).
BACKDATING OPEN ORDERS AND RECEIPTS
Backdating open receipts and orders serves two functions in AccellosOne 3PL. First, it allows you to charge 
renewal storage immediately instead of waiting for the next month or billing period. Second, it can simplify 
your accounting and financial reporting by ensuring that orders and receipts are always entered and 
confirmed within the same month or billing period.
For example, suppose a customer has monthly first of month renewal storage billing and you receive product 
for that customer on November 30 but only confirm it on December 1. If you backdate your receipt to 
November 30, you can charge renewal storage for the month of December. If you do not backdate your 
receipt to November 30, no renewal storage would be charged for the product until January 1.

INVOICING
Working With Batches and Invoices
BILLING AND INVOICING GUIDE 4.2 179
To backdate an open receipt or order, you confirm the receipt or order with a ship or receive date equal to the 
last day of the previous billing period. Then you run your renewal batch with a create date equal to the end of 
the previous billing period.
1 Do one of the following:

CHOF screen showing cursor in Ship Date field
2 Generate your renewal batch with a create date that equals the ship date or receive date that you 
entered in the previous step.
3 Print and confirm the renewal batch in the usual manner.
If you have open orders: If you have open receipts:
a) Enter CHOF.
b) Advance the order’s flow to 
COOR.
c) Position your cursor in the Ship 
Date field.
d) Enter the last day of the previous 
billing period as your ship date.
e) Confirm the order in the usual 
manner.
a) Enter CHRF.
b) Advance the receipt’s flow to 
CORE.
c) Position your cursor in the 
Receive Date field.
d) Enter the last day of the previous 
billing period as your receive 
date.
e) Confirm the receipt in the usual 
manner.

INVOICING
Entering Accessorial Bill Later Charges
Entering Accessorial Bill Later Charges
Accessorial bill later charges are miscellaneous type charges such as blast freezing, shrink wrapping, palletization, etc. They accumulate in ENAC (Bill Later - Enter Charges) and can be either attached to a particular 
receipt or order or entered independently of any given receipt or order.
ENTERING RECEIPT ACCESSORIAL CHARGES
You enter this type of charge in ENRE (Enter Receipts). You can enter receipt accessorial charges at either 
the header level or the line detail level.
1 Enter ENRE.
2 Key in your customer code and press Enter.
3 Key in your shipper code and press Enter.
4 Key in your bill-to code and press Enter.
5 If required, key in values in the various ENRE fields (Receipt Date, Receipt Time, Probill Number and 
Reference Number). If you wish to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 If required, key in a warehouse code and press Enter or press Enter with this field blank to bypass this 
option.
9 Key in your total number of units and press Enter.
10 Press Enter to bypass the remaining fields until your reach the Accessorial Charges field.
11 AccellosOne 3PL will display the Bill Later - Enter Charges (ENAC) screen.
If you are entering your 
accessorial charges at the 
header level:
If you are entering your 
accessorial charges at the line 
detail level:
a) In the Accessorial Charges field, 
key in Y for Yes and press Enter.
b) Continue to press Enter to 
bypass the Receipt Extra 
Charges and Extra Reference 
Number fields.
a) In the Accessorial Charges field, 
key in N for No and press Enter.
b) Continue to press Enter to 
bypass the Extra Charges and 
Extra Reference Number fields.
c) In the Line Detail Block, press 
Enter until your cursor is positioned in the Charge field.
d) In the Charge field, key in Y for 
Yes and press Enter.
e) Key in your item code, quantities, 
location and any other requested 
information for your line.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 181

Bill Later - Enter Charges (ENAC)
12 Click on Create Record.
The system will display the customer information of the customer you entered in step 2. If you wish to bill 
to a party other than the customer who owns the goods, press F9 until your cursor is positioned in the Bill 
To Code field. Then key in the customer code of the bill-to party and press Enter.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges (ENAC) screen showing prompt for charge code
13 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then 
key in Y for Yes and press Enter.
14 In the Charge Code field, key in your charge code and press Enter.
15 If prompted to do so, select the appropriate tax code from the tax code pick list.
16 If prompted to do so, key in your location bill code and press Enter.
17 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based 
labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one 
hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45. 

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 183

Bill Later - Enter Charges (ENAC) screen showing prompt for rate
18 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the 
standard rate, key in a new rate and press Enter.
19 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override 
the system-calculated total, key in a new total and press Enter.
20 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and 
press Enter.
21 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line 
number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, 
click on Return to Main and Master Block to exit the Remark Block.
22 If required, repeat steps 13 to 20 for any additional charges that you wish to assign to the header or line 
detail blocks.
23 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
24 When you finish entering all your line details, click on Return to Main and Master Block. Then click on 
Exit to exit.
ENTERING RECEIPT EXTRA CHARGES
You enter this type of charge in the header block of ENRE (Enter Receipts) only. You cannot enter receipt 
extra charges at the line detail level. Unlike receipt accessorial charges, receipt extra charges cannot be 
billed to a third party; that is, the bill-to party must equal the customer.

INVOICING
Entering Accessorial Bill Later Charges
If you do not produce a separate warehouse receipt invoice — that is, you include receipt charges with your 
accessorial charges on an accessorial invoice — there is no need to create receipt extra charges. Instead, 
create a receipt accessorial charge.
1 Enter ENRE.
2 Key in your customer code and press Enter.
3 Key in your shipper code and press Enter.
4 Key in your bill-to code and press Enter.
5 If required, key in values in the various ENRE fields (Receipt Date, Receipt Time, Probill Number and 
Reference Number). If you wish to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 If required, key in a warehouse code and press Enter or press Enter with this field blank to bypass this 
option.
9 Key in your total number of units and press Enter.
10 Press Enter to bypass the remaining fields until your reach the Receipt Extra Charges field. Key in Y for 
Yes in this field and press Enter.
11 Press Enter to bypass the Extra Reference Number fields until AccellosOne 3PL displays the Bill Later - 
Enter Charges (ENAC) screen.

Bill Later - Enter Charges (ENAC)
12 Click on Create Record.
The system will display the customer information of the customer that you entered in step 2. 

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 185

Bill Later - Enter Charges (ENAC) screen showing prompt for charge code
13 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then 
key in Y for Yes and press Enter.
14 In the Charge Code field, key in your charge code and press Enter.
15 If prompted to do so, select the appropriate tax code from the tax code pick list.
16 If prompted to do so, key in your location bill code and press Enter.
17 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based 
labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one 
hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges (ENAC) screen showing prompt for rate
18 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the 
standard rate, key in a new rate and press Enter.
19 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override 
the system-calculated total, key in a new total and press Enter.
20 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and 
press Enter.
21 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line 
number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, 
click on Return to Main and Master Block to exit the Remark Block.
22 If required, repeat steps 13 to 20 for any additional charges that you wish to assign to the header block.
23 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
24 Enter your line details in the normal way and then click on Return to Main and Master Block. Then click 
on Exit to exit.
ENTERING ORDER ACCESSORIAL CHARGES
You enter this type of charge in ENOR (Enter Orders). You can enter order accessorial charges at the header 
level, at the line detail level or both. 
1 Enter ENOR.
2 Key in your customer code and press Enter.
3 Key in your consignee code and press Enter.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 187
4 Key in your sold-to code and press Enter.
5 If required, key in values in the various ENOR fields (Order Date, Order Time, To Ship Date, To Ship 
Time, To Arrive Date, To Arrive Time, Customer Order Number and Purchase Order Number). If you wish 
to skip a field, press Enter with the field blank to bypass the option. 
6 Key in your carrier code and press Enter.
7 Key in your load type code and press Enter.
8 Key in your freight term and press Enter. If required, key in your COD amount, payment type and message code. 
9 Key in Y for Yes or N for No in the Remarks, Carrier Details, Pallet Details and EDI Details fields and 
press Enter.
10 AccellosOne 3PL will display the Bill Later - Enter Charges (ENAC) screen.
If you are entering your 
accessorial charges at the 
header level:
If you are entering your 
accessorial charges at the line 
detail level:
a) In the Accessorial Charges field, 
key in Y for Yes and press Enter.
b) Continue to press Enter to 
bypass the Warehouse Code 
and Extra Reference Number 
fields.
a) In the Accessorial Charges field, 
key in N for No and press Enter.
b) Continue to press Enter to 
bypass the Extra Charges and 
Extra Reference Number fields.
c) In the Line Detail Block, press 
Enter until your cursor is positioned in the Charge field.
d) In the Charge field, key in Y for 
Yes and press Enter.
e) Key in your item code, quantities, 
location and any other requested 
information for your line.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges (ENAC)
11 Click on Create Record.
The system will display the customer information of the customer that you entered in step 2. If you wish 
to bill to a party other than the customer who owns the goods, press F9 until your cursor is positioned in 
the Bill To Code field. Then key in the customer code of the bill-to party and press Enter.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 189

Bill Later - Enter Charges (ENAC) showing prompt for charge code
12 If you wish to attach a remark to your charge, press F9 to position your cursor in the Remark field. Then 
key in Y for Yes and press Enter.
13 In the Charge Code field, key in your charge code and press Enter.
14 If prompted to do so, select the appropriate tax code from the tax code pick list.
15 If prompted to do so, key in your location bill code and press Enter.
16 In the Qualifying Quantity field, key in your quantity and press Enter. If you are entering an hourly based 
labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one 
hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges (ENAC) showing prompt for rate
17 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the 
standard rate, key in a new rate and press Enter.
18 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override 
the system-calculated total, key in a new total and press Enter.
19 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and 
press Enter.
20 If you entered Y for Yes in the Remark field, the Remark Block will be displayed. Key in 1 as your line 
number and press Enter. Then key in your remarks and press Enter again. When you finish your last line, 
click on Return to Main and Master Block to exit the Remark Block.
21 If required, repeat steps 13 to 19 for any additional charges that you wish to assign to the header or line 
detail blocks.
22 When you have added all your charges, click on Return to Main and Exit to return to the Line Detail 
Block.
23 Enter your line details in the normal way and then click on Return to Main and Master Block. Then click 
on Exit to exit.
ENTERING ACCESSORIAL CHARGES IN ENAC
You can enter accessorial bill later charges directly in ENAC without creating a receipt in ENRE or an order in 
ENOR. This procedure is useful when you wish to add an accessorial charge to a receipt or order that is 
already confirmed or you wish create a one-time accessorial charge that is not connected to a particular 
receipt or order.
1 Enter ENAC.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 191
2 Click on Create Record.
3 In the Bill To Code field, key in the customer that you wish to bill and press Enter.

Bill Later - Enter Charges (ENAC) showing prompt for date
4 In the Date to Charge field, key in your date to charge and press Enter. This date is only used if you enter 
a date restriction in the Accessorial Date field in BILB. For example, if you enter 25.01.05 in the Date to 
Charge field and (=25.01.05) in the Accessorial Date field, the charge will be excluded from the batch.
If you press Enter in the field without entering a date, ENAC will use the current system date.
5 If required, key in a reference description and/or reference number and press Enter. If the charge is 
related to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in Y or Yes or N for No and press Enter. Unlike reference descriptions, remarks
are for internal purposes only and do not print on the invoice.
7 In the Charge Code field, key in your charge code and press Enter.
8 If prompted to do so, select the appropriate tax code from the tax code pick list.
9 If prompted to do so, key in your location bill code and press Enter.
10 In the Qualifying Quantity field, key in the quantity and press Enter. If you are entering an hourly based 
labor charge, you enter partial hours by specifying the number of minutes. For example, to enter one 
hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges (ENAC) showing prompt for rate
11 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter.
12 In the Total field, press Enter to accept the system total or key in a new total and press Enter.
13 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and 
press Enter.
14 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your 
remarks, click on Return to Main and Master Block to return to the Main Block.
15 Repeat steps 7 to 13 for each additional charge for this customer.
16 When you finish entering all your charges, click on Return to Main to exit create mode.
The system will assign an Accessorial Entry Number to the charges. You may wish to write this number 
down for future reference. It will allow you to access the charge in ENAC directly without the need to 
scroll through records or query by customer or charge code.
17 Click on Exit to exit.
ADDING ACCESSORIAL CHARGES TO A CONFIRMED ORDER IN OEXC
You can add an accessorial charge to a confirmed order in OEXC (Add Accessorial Charge to Order). You 
can add this charge at either the header level or the line detail level.
1 Enter OEXC.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 193
2 Key in your order number and press Enter.

Add Accessorial Charge to Order (OEXC) screen showing two order lines on order 1908
3 Position your cursor over the line to which you wish to apply the accessorial charge.
4 Key in Y for Yes and press Enter.
5 Click on Extra Charge.
If you wish to apply the charge to 
the order header:
If you wish to apply the charge to 
the order line:
a) In the Order Extra Charge Flag 
field, key in Y for Yes and press 
Enter.
b) Click on Extra Charge.
c) Proceed to step 6.
a) Click on Order Details.
b) Proceed to next step.

INVOICING
Entering Accessorial Bill Later Charges

Bill Later - Enter Charges Block
6 When the Bill Later - Enter Charges Block appears, proceed to enter your accessorial charge(s). You add 
charges to this screen by following the instructions in “Entering Accessorial Charges in ENAC” on page 
190.
7 When you finish entering your charges, click on Return to Main and Exit to exit. 
ADDING ACCESSORIAL OR RECEIPT EXTRA CHARGES TO A CONFIRMED 
RECEIPT IN REXC
You can add an accessorial or receipt extra charge to a confirmed receipt in REXC (Enter Receipt Extra 
Charges). You can add receipt extra charges at either the header level or the line detail level. You can add 
accessorial extra charges at the header level only.
If you do not produce a separate warehouse receipt invoice — that is, you include receipt charges with your 
accessorial charges on an accessorial invoice — there is no need to create receipt extra charges in REXC. 
Instead, create a receipt accessorial charge.
1 Do one of the following:
If you rate your receipts 
automatically:
If you rate your receipts manually 
in RCRA (Receipt Rater):
a) Run RERA (Requeue Receipt for 
Rating) to “unrate” the receipt.
a) If you rated your receipt in 
RCRA, you cannot add further 
charges to it in REXC unless you 
first “unrate” the receipt in RERA 
(Requeue Receipt for Rating).

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 195
2 Enter REXC.
3 Key in your receipt number and press Enter.

Enter Receipt Extra Charges (REXC) screen showing receipt 1434
4 Position your cursor over the appropriate field (Receipt Extra Charge Flag or Receipt Accessorial Flag), 
key in Y for Yes and press Enter.

Enter Receipt Extra Charges (REXC) screen showing three receipt lines on receipt 1434
5 Position your cursor over the line to which you wish to apply the receipt extra charge.
If you wish to apply the charge to 
the receipt header:
If you wish to apply the receipt 
extra charge to the receipt line:
a) Click on Extra Charge or Accessorial Charge.
b) Proceed to step 7.
a) Click on Receipt Details.
b) Proceed to next step.

INVOICING
Entering Accessorial Bill Later Charges
6 Key in Y for Yes and press Enter.
7 Click on Extra Charge.

Bill Later - Enter Charges Block
8 When the Bill Later - Enter Charges Block appears, proceed to enter your accessorial or receipt extra 
charge(s). You add charges to this screen by following the instructions in “Entering Accessorial Charges 
in ENAC” on page 190.
9 When you finish entering your charges, click on Return to Main and Exit to exit. 
10 Do one of the following:
ENTERING A CREDIT IN ENAC
Credits are similar to regular charges except that the quantity is entered as a negative value. If you wish the 
credit to appear on a separate invoice, you can use the immediate charge program (ENIN) instead of ENAC. 
If the charge code that you use for the credit has a minimum charge, you must enter the credit in ENIN. See 
“Entering a Credit in ENIN” on page 201 for instructions.
1 Enter ENAC.
2 Click on Create Record.
If you rate your receipts 
automatically:
If you rate your receipts manually 
in RCRA (Receipt Rater):
a) Run CHRF (Time Stamp and 
Confirm Receipt) to rerate the 
receipt.
a) Run RCRA to rerate the receipt.

INVOICING
Entering Accessorial Bill Later Charges
BILLING AND INVOICING GUIDE 4.2 197
3 In the Bill To Code field, key in the customer that you wish to credit and press Enter.

Bill Later - Enter Charges (ENAC) showing prompt for date
4 In the Date to Charge field, press Enter to accept the current date. 
5 If required, key in a reference description and/or reference number and press Enter. If the credit is related 
to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in Y or Yes or N for No and press Enter. Unlike reference descriptions, remarks
are for internal purposes only and do not print on the invoice.
7 In the Charge Code field, key in your charge code and press Enter.
8 If prompted to do so, select the appropriate tax code from the tax code pick list.
9 If prompted to do so, key in your location bill code and press Enter.
10 In the Qualifying Quantity field, key in the quantity and press Enter. Because you are entering a credit, 
you must enter the quantity as a negative.
11 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter. 
12 In the Total field, press Enter to accept the system total or key in a new total and press Enter.
13 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your 
remarks, click on Return to Main and Master Block to return to the Main Block.
14 When you finish entering all your charges, click on Return to Main and Exit.

INVOICING
Working With Accessorial Bill Immediately Charges
ENTERING A CUSTOMER DEPARTMENT IN ENAC
You can assign a department code to a manual charge entered in ENAC. Department codes are used solely 
for reporting purposes and financial integration and serve no other function in AccelosOne 3PL. You maintain 
your customer/department relationships in CUDE and you activate customer department codes in COMP 
(Company Parameters) by selecting the appropriate option - None, Allow, Required - in the new field 
Department Entry for Charges.
CUDE screen
When customer departments are activated, the Department dropdown list in ENAC is populated with the 
departments that you set up in CUDE.
Working With Accessorial Bill Immediately Charges
These charges are one-time miscellaneous charges that are not attached to a particular order or receipt — for 
example, overtime, faxing and long distance charges — and that you wish to invoice immediately. You enter 
this type of charge in ENIN (Enter Charges - Bill Immediately). Unlike bill later accessorial charges, 
immediate accessorial charges do not accumulate in ENAC. 
There are five main steps in billing and invoicing immediate accessorial charges:
 you enter your charges in ENIN
 you generate the batch in BILB
 you print the audit
 you confirm the batch
 you print the invoice
ENTERING YOUR CHARGES IN ENIN
1 Enter ENIN.
2 Click on Create Record.
3 In the Bill-To Code field, key in the customer that you wish to bill and press Enter.

INVOICING
Working With Accessorial Bill Immediately Charges
BILLING AND INVOICING GUIDE 4.2 199

Bill Immediate - Enter Charges (ENIN)
4 In the Invoice Date field, press Enter to accept the current system date as your invoice date or key in a 
new date and press Enter. This date is only used if you enter a date restriction in the Invoice Date field in 
BILB. For example, if you enter 25.01.01 as your invoice date in ENIN and (=25.01.01) in the Invoice 
Date field in BILB, the charge will be excluded from the batch.
5 If required, key in a description in the Reference Description field and press Enter or press Enter with this 
field blank to bypass this option. This reference description is for internal purposes only and does not 
print on the invoice.
6 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field 
apply to the entire invoice. If you wish to enter remarks for each charge, you do so in the Charge Block, 
not the Main Block.
Unlike reference descriptions, remarks print on the invoice.
7 Do one of the following:
If you entered N for No: If you entered Y for Yes:
a) Proceed to next step. a) Key in your first line of your 
remarks and press Enter.
b) If required, key in your second 
and any additional lines that you 
require and press Enter at the 
end of each line. To exit the 
Remark Block, click on Return to 
Main and Master Block.
c) Click on Charge Block.

INVOICING
Working With Accessorial Bill Immediately Charges
8 In the Charge Code field, key in your charge code and press Enter.
9 In the Reference Description field, key in a reference description and press Enter or press Enter with this 
field blank to bypass this option.
10 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field 
apply to each charge in the Charge Block.
11 If prompted to do so, key in your location bill code and press Enter.
12 In the Qualifying Quantity field, key in the quantity to be charged for and press Enter. If you are entering 
an hourly based labor charge, you enter partial hours by specifying the number of minutes. For example, 
to enter one hour and 15 minutes, you key in 1.15; to enter two hours and 45 minutes, you key in 2.45.
13 In the Rate field, press Enter to accept the standard rate for this charge code. If you wish to override the 
standard rate, key in a new rate and press Enter.
14 In the Total field, press Enter to accept the system-calculated total for the charge. If you wish to override 
the system-calculated total, key in a new total and press Enter.
15 If a tax field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount and 
press Enter.
If you entered N for No in the 
Remarks field:
If you entered Y for Yes in the 
Remarks field:
a) Proceed to next step. a) Key in your first line of your 
remarks and press Enter.
b) If required, key in your second 
and any additional lines that you 
require and press Enter at the 
end of each line. To exit the 
Remark Block, click on Return to 
Main and Exit.
c) To add an additional charge, 
click on Charge Block then Create Record.

INVOICING
Working With Accessorial Bill Immediately Charges
BILLING AND INVOICING GUIDE 4.2 201

Bill Immediate - Enter Charges (ENIN) showing Charge Block
16 If required, repeat the above steps for any additional charges that you wish to assign to the invoice.
17 When you finish adding all your charges, click on Return to Main and, if required, Remark Block. Then 
click on Master Block and Exit.
Note the system-generated invoice number at the top of your screen. You will need this number if you 
wish to look up the invoice in LOIN (Look Up Invoices).
ENTERING A CREDIT IN ENIN
Credits are similar to regular charges except that the quantity is entered as a negative value. If the charge 
code that you use for the credit has a minimum charge and the quantity that you enter triggers that minimum 
charge, the system will display the minimum charge (a positive number) rather than the credit amount (a 
negative number) as the charge total. When this happens, you must enter the credit amount manually in the 
Total field (for example, -15 for a credit amount of 15 currency units).
1 Enter ENIN.
2 Click on Create Record.
3 In the Bill To Code field, key in the customer that you wish to credit and press Enter.

INVOICING
Working With Accessorial Bill Immediately Charges

Bill Immediate - Enter Charges (ENIN) showing prompt for date
4 In the Invoice Date field, press Enter to accept the current date. 
5 If required, key in a reference description and/or reference number and press Enter. If the credit is related 
to a specific receipt or order, you should note the order or receipt number in one of these fields.
Reference descriptions are for internal purposes only and do not print on your invoice.
6 In the Remarks field, key in N for No or Y for Yes and press Enter. The remarks that you enter in this field 
apply to the entire invoice. If you wish to enter remarks for each charge, you do so in the Charge Block, 
not the Main Block.
Unlike reference descriptions, remarks do print on the invoice.
7 If prompted to do so, key in your location bill code and press Enter.
8 In the Charge Code field, key in your charge code and press Enter.
If you entered N for No: If you entered Y for Yes:
a) Proceed to next step. a) Key in your first line of your 
remarks and press Enter.
b) If required, key in your second 
and any additional lines that you 
require and press Enter at the 
end of each line. To exit the 
Remark Block, click on Return to 
Main and Master Block.
c) Click on Charge Block.

INVOICING
Working With Accessorial Bill Immediately Charges
BILLING AND INVOICING GUIDE 4.2 203
9 In the Qualifying Quantity field, key in the quantity and press Enter. Because you are entering a credit, 
you must enter the quantity as a negative.
10 In the Rate field, press Enter to accept the system rate or key in a new rate and press Enter. 
11 In the Total field, press Enter to accept the system total or key in a new total and press Enter. If the 
charge code that you use has a minimum charge, you may need to override the total amount (a positive 
number representing the minimum charge) by the credit amount (a negative number).
12 If the GST field is displayed, press Enter to accept the system-calculated tax or key in a new tax amount 
and press Enter.
13 If you entered a Yes in the Remarks field, the Remark Block will be displayed. Key in 1 as your line number and press Enter. Then key in your remarks and press Enter again. When you finish entering your 
remarks, When you finish entering your remarks, click on Return to Main and Master Block to return to 
the Main Block.
14 When you finish entering all your charges, click on Return to Main and Exit.
GENERATING AN IMMEDIATE ACCESSORIAL BATCH
Each time you generate an immediate accessorial batch, all immediate accessorial charges that have 
accumulated in ENIN since the confirming and printing of your last invoice will be placed in a batch and 
assigned a batch number by the system.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Create Record.

Billing Batch (BILB) screen showing immediate invoices
4 In the Description field, key in a description for your batch and press Enter. Possible descriptions are: 
ALL CUSTOMERS
CUSTOMER 1
CAUTION Do not generate an immediate accessorial batch if another operator is 
entering a charge in ENIN. Wait until the operator has finished entering the charge 
before you begin working in BILB.

INVOICING
Working With Accessorial Bill Immediately Charges
5 If you select a name from the Attention dropdown list, it will print on the invoice as an Attention To line 
above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
6 In the Create Date field, select your cut-off date for your batch from the pop-up calendar. When you specify a cut-off date, all immediate charges that were entered up to and including the cut-off date will be 
included in the batch. If AccellosOne 3PL is linked to your accounting system, the cut-off date will also be 
the posting date for the charge.
If you do not select a date from the pop-up calendar, BILB will use the current date as your cut-off date.
7 Click on Save or press Enter to confirm your create date.

Billing Batch (BILB) screen showing immediate accessorial restrictions
8 Proceed to specify restrictions on the charges that you wish to place on your accessorial invoice. For 
example, if you wanted to generate an invoice for Customer 1 only, you would enter the code for Customer 1 in the Customer Code field. Only charges incurred by Customer 1 would appear on the invoice.
You enter restrictions by means of the following operands:
= (exact match of all characters)
= + % (match of characters entered)
(=) (not equal to)
> (greater than)
>= (greater than or equal to)
< (less than)
<= (less than or equal to)
- (from X to Y (a range)) 
EXAMPLES
=CUST1 Customer 1 only
=CUST1% Any customer code beginning with CUST1 
(for example, CUST1, CUST111, CUST199, CUST1ABC)
=CUST1%,=CUST2% Any customer code beginning with CUST1 or CUST2 
(for example, CUST1, CUST111, CUST299, CUST2ABC)

INVOICING
Working With Accessorial Bill Immediately Charges
BILLING AND INVOICING GUIDE 4.2 205
9 In the Invoice Number field, key in your invoice number restrictions and press Enter or press Enter with 
this field blank for no restrictions. 
If you enter invoice number restrictions in this field, only charges for those invoices that meet the restriction will be included in the batch. If you leave this field blank, your invoice will include all charges regardless of invoice number.
10 In the Customer Code field, key in your customer restrictions and press Enter or press Enter with this 
field blank for no restrictions. 
If you enter customer restrictions in this field, only charges for customers that meet the restriction will be 
included in the invoice. If you leave this field blank, your invoice will include charges for all customers.
11 In the Invoice Date field, key in your date restrictions and press Enter or press Enter with this field blank 
for no restrictions. You must enter your date restrictions in YYYY.MM.DD format.
If you enter a date in this field, only those immediate accessorial charges with a invoice date that meets 
the date restriction that you specify will be generated. If you leave this field blank, all accessorial charges 
regardless of their invoice value will be generated.
(=CUST1) All customers except customer 1 
(=CUST1),(=CUST2) All customers except customers 1 and 2 
>CUST1 All customers greater than or equal to customer 1
(for example, CUST1, CUST2, D4, S7, etc.)
<CUST1 All customers less than or equal to customer 1 
(for example, CUST0, CUST1, A4, B7, etc.)
CUST1-CUST4 Customer 1 through Customer 4
NOTE There is a maximum of 250 characters that you can enter in a restriction. If 
you exceed this limit, AccellosOne 3PL will display an error message. Remove one or 
two of the customer, consignee, shipper or carriers in the restriction causing the problem and try again.
Only one operand can be used in any given field. You cannot use both “=” and “(=)” or 
“<“ and “>” in the same field.
NOTE Any restrictions that you enter in this field will operate within the cut-off date 
that you defined in the Create Date field in the Main Block of BILB. For example, you 
can specify Jan 1/05 as your cut-off date — that is, no charges later than that date — 
and you can specify > Dec 1/04 as your Invoice Date restriction. This would result in a 
batch of all charges created between Dec 1/04 and Jan 1/05.

INVOICING
Working With Accessorial Bill Immediately Charges

Immediate Invoice Invoicing (BILB) screen showing a batch being generated for all charges with an 
invoice date later than 06.08.07
12 Click on Generate Batch. 
PRINTING THE IMMEDIATE ACCESSORIAL AUDIT
The immediate accessorial audit shows each charge that will appear on the invoice. The purpose of this 
report is to allow you to verify all charges before confirming and printing the final invoice.
Refer to “Working With Audit Batch Restrictions” on page 160 for further information on audit reports.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

Billing Batch (BILB) screen showing batch 79 with a status of Generated
5 Select Print Audit from the Action dropdown list.

INVOICING
Working With Accessorial Bill Immediately Charges
BILLING AND INVOICING GUIDE 4.2 207

Billing Batch screen showing restrictions for immediate audit
6 Select the appropriate option in the Summary or Detail field.
7 Key in a description for your audit report.
8 Proceed to enter your print audit restrictions, if any.
9 When you finish entering your restrictions, click on Print.
10 Key in your printer code and press Enter or select it using the pick list.
11 Click Ok.
In a few moments, your report will begin to print. Once the report is finished printing, the BILB screen will 
be displayed.
CONFIRMING THE BATCH AND PRINTING THE IMMEDIATE ACCESSORIAL 
INVOICE
If all the charges on the Immediate Invoice Audit report are correct, you are ready to confirm the batch and 
print the invoice. If the batch or any charge on it is not correct, you must delete the batch and generate a new 
one.
1 Enter BILB.
2 Select Immediate Invoice from the Batch Type dropdown list.
3 Click on Enter Criteria.
4 Key in your batch number and click on Execute Query.

INVOICING
Adding Charges to a Confirmed Receipt

Billing Batch (BILB) screen showing batch 79 with a status of Printed
5 Select Confirm from the Action dropdown list.
6 When the Select Printer window appears, key in your printer code and press Enter or select it using the 
pick list.
7 Click Ok. When the batch finishes running, your invoice is printed.
Adding Charges to a Confirmed Receipt
If a receipt has been confirmed but not invoiced, you can add new accessorial charges to the receipt in RECH 
(Receipt Charges) as well as modify/delete existing charges. RECH also allows you to look up existing 
charges for the receipt without adding any new charges.
If there are extra charges on the receipt, running RECH will automatically generate and confirm the extra 
charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra 
charge audit and confirm the extra charge batch. 
1 Enter RECH.
2 Key in your receipt number and press Enter.
NOTE Extra charge batches created through RECH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra 
charges on the extra charge batch are fully editable in ENAC.

INVOICING
Adding Charges to a Confirmed Receipt
BILLING AND INVOICING GUIDE 4.2 209
RECH screen showing previously entered charges for receipt
RECH displays all previously entered charges for the receipt. The A/O flag shows whether the charge is 
automatic or optional (that is, whether or not you can override the charge at receipt/order confirmation). 
3 If you click on Detail/Summary Records , you can toggle between detail view (all charges listed 
individually) and summary view (charges summarized by charge code).
4 Do one of the following:
If you wish to add an accessorial 
charge to the receipt:
If you wish to modify an existing 
charge on the receipt:
a) In the Header Block, click on All 
Charges/ENAC . 
b) Enter your accessorial charge(s) 
in the normal manner.
a) In the Detail Block, click on This 
Charge/ENAC beside the 
charge that you wish to modify. 
b) Proceed to modify the charge in 
the normal manner.

INVOICING
Adding Charges to a Confirmed Order
RECH screen showing existing charge
5 When you finish entering, modifying or deleting your charge(s), click on Exit .
DELETING A CHARGE
1 In the Detail Block, click on the charge that you wish to delete and click on Delete All Charges/ENAC
. 
2 When prompted to confirm the deletion, click on Yes.
Adding Charges to a Confirmed Order
If an order has been confirmed but not invoiced, you can add new accessorial charges to an order in ORCH 
(Order Charges) as well modify/delete existing charges. ORCH also allows you to look up existing charges for 
the order without adding any new charges. 

INVOICING
Adding Charges to a Confirmed Order
BILLING AND INVOICING GUIDE 4.2 211
If there are extra charges on the order, running ORCH will automatically generate and confirm the extra 
charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra 
charge audit and confirm the extra charge batch. 
1 Enter ORCH.
2 Key in your order number and press Enter.
ORCH screen showing previously entered charge for order
ORCH displays all previously entered charges for the order. The A/O flag shows whether the charge is 
automatic or optional (that is, whether or not you can override the charge at receipt/order confirmation).
3 If you click on Detail/Summary Records , you can toggle between detail view (all charges listed 
individually) and summary view (charges summarized by charge code).
4 Do one of the following:
NOTE Extra charge batches created through ORCH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra 
charges on the extra charge batch are fully editable in ENAC.
If you wish to add an accessorial 
charge to the order:
If you wish to modify an existing 
charge on the order:
a) In the Header Block, click on All 
Charges/ENAC . 
b) Enter your accessorial charge(s) 
in the normal manner.
a) In the Detail Block, click on This 
Charge/ENAC beside the 
charge that you wish to modify. 
b) Proceed to modify the charge in 
the normal manner.

INVOICING
Rollup Invoicing
ORCH screen showing existing charge
5 When you finish entering, modifying or deleting your charge(s), click on Exit .
DELETING A CHARGE
1 In the Detail Block, click on the charge that you wish to delete and click on Delete All Charges/ENAC
. 
2 When prompted to confirm the deletion, click on Yes.
Rollup Invoicing
Rollup invoicing allows you to generate a single invoice for a customer across multiple companies based on 
the charges for that customer in each of the companies.
The charges need not be the same across companies. For example, you can charge for handling by the piece 
in company 1 and charge handling by weight in company 2. AccellosOne 3PL will calculate the correct 
charges in both companies and produce a single invoice in the rollup company showing the total handling for 
both companies. 
Rollup invoicing is only available for renewal and accessorial invoices and consequently should only be used 
with the UREC and UALL invoicing types. Receipt and immediate charges will be correctly calculated and 

INVOICING
Rollup Invoicing
BILLING AND INVOICING GUIDE 4.2 213
invoiced in your separate companies for each customer; however, when you generate your rollup invoice, 
receipt and immediate charges will not be rolled up.
Rollup invoicing requires a minimum of three companies:
 a rollup company for creating a single cross-company invoice for the customers requiring such an 
invoice
 two or more child companies — a child company is the company in which the actual charges are generated
The customers in your child companies should all have the same invoicing type. It is not recommended to mix 
invoicing types for the same customer across multiple child companies.
The following diagram shows invoice processing for a renewal invoice (UREC) customer.
child receipt 
charges
child renewal 
charges
child daily invoice 
register
rollup customer 
charges
child accessorial 
invoice
child extra
 charges
child accessorial 
charges
non-rollup 
customers posted 
to GL
child renewal 
invoice
rollup accessorial 
invoice
rollup renewal 
invoice
rollup daily invoice 
register
rollup customers 
posted to GL
all charges except receipt 
and immediate charges 
passed to rollup company

INVOICING
Rollup Invoicing
SETTING UP ROLLUP INVOICING
You define your rollup and child companies in COMP (Company Code) be entering the appropriate value in 
the Rollup Type field. There are three possible values for the Rollup Type field:
C = Child
N = Not Applicable
R = Rollup
SETTING UP YOUR ROLLUP COMPANY
1 Enter COMP.
2 Click on Create Record.
3 Enter your company code, company description and the other requested information.
4 When you reach the Rollup Type field, key in R for Rollup and press Enter.
5 When you finish setting up your company, click on Return to Main to exit create record mode. Then click 
on Exit to exit.

Company Code (COMP) screen showing roll-up company R1
SETTING UP YOUR CHILD COMPANIES
1 Enter COMP.
2 Click on Create Record.
NOTE If your company is already set up, you cannot adjust its rollup type. Contact 
your HighJump consultant for assistance.

INVOICING
Rollup Invoicing
BILLING AND INVOICING GUIDE 4.2 215
3 Enter your company code, company description and the other requested information.
4 When you reach the Rollup Type field, key in C for Child and press Enter.
5 When you finish setting up your company, click on Return to Main to exit create record mode. Then click 
on Exit to exit.
6 Repeat the above steps for each additional child company that you wish to set up.

Company Code (COMP) screen showing child company C1
ATTACHING YOUR CHILD COMPANIES TO THE ROLLUP COMPANY
You attach your child companies to your rollup company in the Rollup Block of your rollup company. 
1 Enter COMP.
2 Key the company code for your rollup company and press Enter.
3 Click on Rollup Block.
4 If you are not in Create Record mode, click on Create Record.
5 Key in your child company code and press Enter.
6 Press Enter to bypass the Report field.
7 In the Invoice field, key in Y for Yes and press Enter.
8 Repeat the above steps for each additional child company that you wish to add to your rollup company.
9 When you finish adding your child companies, click on Return to Main.

INVOICING
Billing Audit System

Company Code (COMP) screen showing Rollup Block
10 Click on Master Block and Exit to exit.
SETTING UP YOUR CUSTOMERS
1 In the child companies, set up your customer(s) in the normal manner. These customers can have receipt 
invoices but the receipt charges on such invoices will NOT be rolled up to the rollup company’s accessorial invoice.
2 In the rollup company, set up the same customer or customers that you defined in your child companies. 
Your rollup customer must have the same customer code as your child customers and be defined as an 
invoice only customer — that is, a customer with no inventory.
The invoicing type that you define in DBIP for your rollup customer must be the same as the invoicing 
type defined in your child companies.
GENERATING AND PRINTING ROLLUP INVOICES
When generating and printing rollup invoices, you follow the same procedures that you use for accessorial 
(UALL) or renewal (UREC) invoicing.
1 For each child company, generate and print the appropriate batches according to the normal procedures 
for accessorial or renewal invoicing.
2 Run the daily invoice register (BILB) for each child company.
3 In your rollup company, generate and print the appropriate batches. If your child companies have accessorial invoicing, follow the normal procedures for accessorial invoicing. If your child companies have 
renewal invoicing, follow the normal procedures for renewal invoicing.
4 Run the daily invoice register (BILB) for your rollup company.
Billing Audit System
The billing audit system allows you to track changes to and deletions of any charge in ENAC or ENIN. For 
example, if an operator changes the charge code, qualifying quantity, rate or total of a charge in ENAC, AccellosOne 3PL will create a complete record of the change, showing the date and time of the change, the 
operator code, the accessorial number and what was changed.

INVOICING
Billing Audit System
BILLING AND INVOICING GUIDE 4.2 217
When changing or deleting a charge in ENAC or ENIN, the operator will be required to enter a reason code 
describing the rationale for the change. Reason codes are user-defined in the setup program REAS.
You can look up your changes and deletions in ACAL (Look Up Changes to Accss. Charges) and you can 
print them in the report ACCA (Accessorial Charge Changes Report). Changes and deletions remain on your 
system until you purge them in PACA (Purge Changes to Accss. Charges).
If you activate the authorization component of the billing audit system, changes to any charge in ENAC must 
be individually approved in a separate program before it can be placed on a batch and invoiced. Likewise, 
manual charges1 created in ENAC will be subject to the same approval process.
SETTING UP THE BILLING AUDIT SYSTEM
There are two steps to follow in setting up the billing audit system:
 you activate the billing audit system
 you set up your reason codes
ACTIVATING THE BILLING AUDIT SYSTEM
The billing audit system must be activated by selecting the appropriate option in the Force Audit of Accessorial Charges field in COMP (Company Code). There are three options available for the billing audit system:
1 Enter COMP.
2 Retrieve the company that you wish to set up for the billing audit system.
3 Click on Company Parameters.
4 Click on the Miscellaneous tab.
5 Select the appropriate option from the Force Audit of Accessorial Charges dropdown list.
1. A manual charge is any charge that is not automatically generated by the system. For example, extra charges added 
to a receipt or order and accessorial charges entered through ENAC or ENIN are all considered to be manual charges.
OPTION DESCRIPTION
Neither Tracking nor 
Authorization
The billing audit system is deactivated. There is no tracking of changes, additions and deletions in ENAC or ENIN and no authorization is required.
Tracking Only The following logic applies:
 any changes made to existing charges in either ENAC or ENIN are tracked
 deletions of existing charges in either ENAC or ENIN are tracked
 manual charges added to ENAC are NOT tracked
 no authorization is required
Tracking and AuthorizationThe tracking options of A (Tracking Only) plus the following logic:
 authorization is required to add manual charges to ENAC
 authorization is required to make changes to existing charges in ENAC 

INVOICING
Billing Audit System
COMP screen showing three options in Force Audit of Accessorial Charges field
6 When you finish making your charges, click on Save.
7 Click on Return to exit the Company Parameters Block.
8 Click on Exit.
SETTING UP YOUR REASON CODES IN REAS
Reason codes are required whenever you modify or delete a charge in either ENAC or ENIN. They describe 
the reason why the record is being modified or deleted. You set up your reason codes in REAS (Reason 
Code). If you do not require reason codes, set up a single code called NA (Not Applicable). 
1 Enter REAS.
2 Click on Enter Criteria then Execute Query to see which reason codes have already been set up.
3 If the code that you require has not been set up, click on Create Record.
4 Key in your reason code and press Enter.
5 Key in a description for your new reason code and press Enter.
6 Key in I for Internal and press Enter.
7 Repeat the above steps for each additional reason code that you wish to set up.
8 When you finish adding your reason codes, click on Return to Main.

INVOICING
Billing Audit System
BILLING AND INVOICING GUIDE 4.2 219

REAS screen showing two internal reason codes
9 Click on Exit to exit.
CHANGING AND DELETING CHARGES
You can change or delete any charge in ENAC or ENIN as long as the charge has not been posted to the 
daily invoice register in the program DLRE. When you change or delete a charge, you must enter a reason 
code explaining the rationale for the change.
CHANGING AND DELETING CHARGES IN ENAC
1 Enter ENAC.
2 Retrieve the charge that you wish to modify or delete.

INVOICING
Billing Audit System

ENAC screen showing blast freezing charge
3 Do one of the following:
4 Click on Return to Main and Exit to exit.
CHANGING AND DELETING CHARGES IN ENIN
1 Enter ENIN.
2 Retrieve the invoice containing the charge that you wish to modify or delete.
3 Click on the Charge Block.
If you wish to modify the charge: If you wish to delete the charge:
a) Press Enter until your cursor is 
positioned in the field that you 
wish to change. You can change 
the Qualifying Quantity, the Rate 
and/or the Total.
b) Proceed to make your changes.
c) Key in your reason code and 
press Enter.
a) Press Enter to display the Delete 
button.
b) Click on Delete.
c) Key in your reason code and 
press Enter.
d) Click on Delete again.

INVOICING
Billing Audit System
BILLING AND INVOICING GUIDE 4.2 221

ENIN screen showing three charges on invoice 57
4 If there is more than one charge on the invoice, use your arrow keys to select the appropriate charge.
5 Do one of the following:
6 Click on Return to Main and Master Block.
7 Click on Exit to exit.
TRACKING CHANGES TO ENAC AND ENIN CHARGES
There are two programs that you can use for tracking changes to ENAC and ENIN charges: a look-up 
program called ACAL (Look Up Changes to Accss. Charges) and a report called ACCA (Accessorial Charge 
Changes Report). Both programs show the same information.
If you wish to modify the charge: If you wish to delete the charge:
a) Press Enter until your cursor is 
positioned in the field that you 
wish to change. You can change 
the Qualifying Quantity, the Rate 
and/or the Total.
b) Proceed to make your changes.
c) Key in your reason code and 
press Enter.
a) Press Enter once to position your 
cursor in the Charge field.
b) Click on Delete.
c) Key in your reason code and 
press Enter.
d) Make sure that your cursor is 
positioned on the charge that 
you just deleted.
e) Press Enter once to position your 
cursor in the Charge field.
f) Click on Delete again. The 
record will disappear from your 
screen.

INVOICING
Billing Audit System
If a charge has been modified in either ENAC or ENIN, the Action field will be set to UPD and the original and 
current values will be shown. One record in ACAL/ACCA will be created for each value that was changed.
If a charge has been deleted in either ENAC or ENIN, the Action field will be set to DEL and one record in 
ACAL/ACCA will be created for each enterable field in ENAC or ENIN (for example, Customer Code, Date to 
Charge, Reference Number, Remark Flag, Charge Code, etc.).
LOOKING UP CHANGES IN ACAL
1 Enter ACAL.
2 Key in your search criteria and click on Execute Query.

ACAL screen showing eight updated records for ENAC
3 When you finish looking up your charges, click on Exit to exit.
RUNNING THE ACCESSORIAL CHARGE CHANGES REPORT (ACCA)
1 Enter ACCA.
2 Do one of the following:
If you wish to report on ENAC 
records only:
If you wish to report on ENIN 
records only:
a) Key in ENAC as your program 
name and press Enter.
a) Key in ENIN as your program 
name and press Enter.

INVOICING
Billing Audit System
BILLING AND INVOICING GUIDE 4.2 223

ACCA screen showing ENAC option selected
3 Key in your start date and press Enter. Then key in your end date and press Enter. Only charges that 
were modified or deleted between the start and end dates that you specify will be reported on.
4 Key in your printer code and press Enter.
5 Click Ok.
ACCA report showing five changes
AUTHORIZING YOUR CHARGES
If the authorization component of the billing audit system is activated, you must authorize the following:
 any new manual charges added to ENAC
 any changes to existing charges in ENAC 
You authorize your charges in two steps: first you run the report OAUD (Accessorial Charges Authorization 
Audit) and second you individually approve each charge in ACAU (Accessorial Authorization). If you make a 
change to a charge in ENAC after performing these two steps, you must rerun OAUD and reauthorize the 
charge in ACAU.
ABC Warehousing, Inc. Page 1 of 1
Accessorial Charge Changes Report 02.24.06 09:49
------------------------------------------------------------------------------------------------------------------------------------
Accessorial Charges (ENAC)
 Accss Column Original Current
Update Date Operator Actn Number Name Value Value
------------------ -------- ---- --------- ---------------------- ------------------------------ ------------------------------
02.24.06 09:43:31 LORNE UPD 44012 Charge Rate 20 15
 UPD 44012 Charge Total 20 30
02.24.06 09:45:30 LORNE UPD 44015 Charge Code C1 CHAR-1
 UPD 44015 Loc Bill Code COOL
 UPD 44015 Charge Rate .825 1
 UPD 44015 Charge Total 20.63 25

INVOICING
Billing Audit System
RUNNING THE ACCESSORIAL CHARGES AUTHORIZATION AUDIT (OAUD)
OAUD is an audit report. Each time that you run OAUD, AccellosOne 3PL will group all ENAC charges that 
meet the criteria that you specified on the parameter screen and assign those charges an audit number. The 
audit number that the system will assign is simply the next number in the audit number sequence. This audit 
number will also show on the report.
Each time that you run OAUD, only charges modified or added since the last time that you ran the report are 
included. You cannot generate the same report twice in OAUD. If you wish to report on charges assigned to a 
previous audit, you must set the Reprint flag to Y for Yes and enter your audit number in the Reprint Audit 
Number field.
1 Make sure that you have at least one manual charge to bill. If the manual charge is attached to a particular receipt or order, the receipt or order must be confirmed.
2 Enter OAUD.

OAUD screen
3 In the Customer Code field, key in your customer code and press Enter or press Enter with this field 
blank to include all customers.
4 In the Operator Code field, press Enter to accept your own operator code or key in another operator code 
and press Enter.
5 In the Location Bill Code field, key in your location billing code and press Enter or press Enter with this 
field blank to include all location billing codes.
6 Do one of the following:
If you are printing the report for 
the first time: If you are reprinting the report:
a) Proceed to next step. a) In the Reprint field, key in Y for 
Yes and press Enter.
b) Key in your audit number and 
press Enter.

INVOICING
Billing Audit System
BILLING AND INVOICING GUIDE 4.2 225
7 Key in your printer code and press Enter.
8 Click Ok.
OAUD report showing a blast freezing charge for Customer A
AUTHORIZING THE CHARGES IN ACAU
Once you have reviewed the ENAC charges on the report and approved them, you are ready to authorize 
them in ACAU.
1 Enter ACAU.
2 Click on Enter Criteria then Execute Query to retrieve all charges that require authorization.
ABC Warehousing, Inc. Page 1 of 1
Customer : A Operator : BJONES Location Billing : All
 Accessorial Charges Authorization Audit (OAUD) 02.16.09 15:45
 Accessorial Entry Number 47581 Audit Number 4
 Bill To Code A
 Name Customer A
 Address 1 100 Renfrew Drive, Suite 100
 Address 2
 Address 3
 City Markham State ON
 Zip Code L3R 9R6
 Date To Charge FEB.16.09
 Reference Description
 Reference Number
 Charge Code BF1
 Description Blast Freezing 1
Loc --Qualifying-- ----Charge----
Bill Quantity Sku Quantity Sku Rate Total
 20000 LBS 200 CWT .700 140.00
Remarks

INVOICING
Billing Audit System

Accessorial Authorization (ACAU)
3 Click on Authorize to authorize the first charge.
4 Press your down arrow key to display the next record and click on Authorize to authorize it.
5 Repeat the above step for each charge that you wish to authorize.
6 When you finish authorizing all your charges, click on Exit to exit.
The charges that you authorized can now be placed on a batch and invoiced. 
PURGING CHANGE RECORDS IN PACA
Change records are automatically created by AccellosOne 3PL in ACAL and ACCA whenever you change or 
delete an existing charge in either ENAC or ENIN. They remain on your system until you purge them in 
PACA.
When you purge change records in PACA, the records are permanently removed from the database and 
cannot be restored. You can no longer view the records in ACAL or print them in the report ACCA.
1 Enter PACA.
NOTE PACA should be run on a regular basis to remove old records from the database. Failure to purge these records could eventually lead to slower system performance and a lack of disk storage space.

INVOICING
Invoicing by Warehouse
BILLING AND INVOICING GUIDE 4.2 227
2 Do one of the following:

PACA screen showing ENAC option selected
3 In the All Changes Before field, key in your cut-off date and press Enter.
4 Click on Process Purge.
5 When the “Do you want to proceed with DELETE” message appears, click on Yes.
Invoicing by Warehouse
Invoicing by warehouse allows you to generate separate batches and invoices in BILB by warehouse. For 
example, you could generate one renewal batch for product stored in warehouse 1 and a second renewal 
batch for product stored in warehouse 2. 
There are three setup programs for invoicing by warehouse:
 COMP (Company Parameters Block)
 LODE (Location Billing Code)
 DOCU (Documents)
If you wish to purge ENAC 
records only:
If you wish to purge ENIN 
records only:
If you wish to purge all 
records:
a) Key in ENAC as your program name and press Enter.a) Key in ENIN as your program 
name and press Enter.
a) Press Enter to bypass the Program Name field.

INVOICING
Invoicing by Warehouse
ACTIVATING INVOICING BY WAREHOUSE IN COMP
Invoicing by warehouse must be activated in COMP (Company Code). There are two possible configurations 
for invoicing by warehouse:
1 Enter COMP.
2 Key in your company code and press Enter.
3 Click on Company Parameters.
4 Click on the Miscellaneous tab.
FIELD DESCRIPTIONS (MISCELLANEOUS TAB)
Warehouse Code 
Optional for Invoicing by 
Warehouse
No
Yes
If you select Yes, the Warehouse Code field in BILB is optional. That is, you do 
not need to specify a warehouse when generating your accessorial, extra 
charge, renewal and immediate batches. If you select No, the Warehouse 
Code field in BILB is mandatory.
If you leave this field blank, invoicing by warehouse is deactivated.
Warehouse Code Mandatory for Invoicing by 
Warehouse
No
Yes
If you select Yes, the Warehouse Code field in BILB is mandatory. That is, you 
will not be able to generate a batch without specifying a warehouse restriction.If you select No, the Warehouse Code field in BILB is optional.
If you leave this field blank, invoicing by warehouse is deactivated.

INVOICING
Invoicing by Warehouse
BILLING AND INVOICING GUIDE 4.2 229
COMP screen showing invoicing by warehouse deactivated
5 Select the appropriate value (Yes or No) in the two invoicing by warehouse fields.
6 When you finish making your changes, click on Save to save your changes.
7 Click on Return to exit the Company Parameters Block.
8 Click on Exit to exit.
ASSIGNING YOUR LOCATION BILLING CODES TO WAREHOUSES IN LODE
In LODE you must assign each location billing code to the appropriate warehouse(s). For example, suppose 
you had two location billing codes (COOL and DRY) in your company and three warehouses (1, 2 and 3). If 
COOL and DRY applied to all three warehouses, for each LODE record you would have to set up three detail 
records in the Warehouse Restriction Block: one for warehouse 1, a second for warehouse 2 and a third for 
warehouse 3.
If you had only two warehouses (1 and 2) and warehouse 1 was your COOL warehouse while warehouse 2 
was your DRY warehouse, each LODE record would contain a single record in the Warehouse Restriction 
Block. 
1 Enter LODE.
2 Click on Enter Criteria and Execute Query to retrieve your location billing codes.
3 Select your first location billing code and press Enter.
4 Click on Warehouse Restriction.

INVOICING
Invoicing by Warehouse

LODE screen showing Location Billing Warehouse Restriction block
5 Click on Create Record.
6 Key in your warehouse code and press Enter.
7 Repeat the above steps for each additional warehouse that you wish to link to the location billing code.
8 When you finish assigning warehouse codes to location billing codes, click on Return to Main.

INVOICING
Invoicing by Warehouse
BILLING AND INVOICING GUIDE 4.2 231

LODE screen showing location billing code COOL assigned to two warehouses
9 Click on Master Block and Exit to exit.
SETTING UP YOUR ADDRESS OPTION IN DOCU
In DOCU you must set the Print Company/Warehouse Address flag to the appropriate value for each invoice 
document. If you set this field to C for Company, the company’s address will print on the invoice. If you set this 
field to W for Warehouse, the warehouse address will print on the invoice. 
1 Enter DOCU.
2 Retrieve the invoice document or documents — ACCE, IINV and RENW — that you wish to set up for 
invoicing by warehouse.
3 In the Print Company/Warehouse Address field, key in C for Company or W for Warehouse and press 
Enter.

INVOICING
Invoicing by Warehouse

DOCU screen showing Print Company/Warehouse Address to C for Company
4 Click on Return to Main and Exit to exit.
ENTERING RECEIPTS AND ORDERS IN ENRE/ENOR
When invoicing by warehouse is activated, the Warehouse Code field in the Header Block of ENRE and 
ENOR is a mandatory field.

INVOICING
Invoicing by Warehouse
BILLING AND INVOICING GUIDE 4.2 233

ENRE screen showing Warehouse Code field
ENTERING BATCH RESTRICTIONS IN BILB
If the Warehouse Code Mandatory for Invoicing by Warehouse flag in COMP (Company Parameters) is set to 
No, the warehouse code restriction in BILB is not mandatory. If the Warehouse Code Mandatory for Invoicing 
by Warehouse is set to Yes, the warehouse code restriction in BILB is a mandatory field.

Billing Batch (BILB) screen showing dropdown list for warehouse code

INVOICING
Invoicing by Inventory Level
ENTERING CHARGES IN ENAC/ENIN
When invoicing by warehouse is activated, the Location Billing Code field in ENAC and ENIN is a mandatory 
field.

Bill Later Enter Charges (ENAC) showing Location Billing Code field
Invoicing by Inventory Level
Invoicing by inventory level allows you to generate renewal and accessorial invoices for individual items, lots 
and pallet ID’s in BILB. You activate invoicing by inventory level in CUST by entering the inventory level that 
you wish to invoice by in the Invoices at Inventory Level field.

INVOICING
Invoicing by Inventory Level
BILLING AND INVOICING GUIDE 4.2 235
CUST screen showing invoicing by level 2
In BILB you enter your inventory level restrictions in the Billing Level 1, 2 or 3 fields when you create a new 
accessorial or renewal batch.
BILB screen showing new accessorial batch restricted to lots 101, 105 and 104 through 105

INVOICING
Reversing Charges on Confirmed Invoices
Reversing Charges on Confirmed Invoices
CRIN (Credit Invoice) allows you to reverse charges on accessorial, receipt, renewal and immediate invoice 
after they have been confirmed. When you run the daily invoice register, the reversed charges are listed in the 
register. If AccellosOne 3PL is linked to your accounting system, the reversed charges are also added to your 
general ledger interface file and posted to the appropriate account in your accounting system.
1 Enter CRIN.
2 Key in your search criteria: invoice number, prefix, type (RCPT, RENW, ACCE or IINV), date, customer 
code or amount.
3 When you finish entering your query values, click on Execute Query.
Credit Invoice (CRIN) showing accessorial invoices for customer RF009
AccellosOne 3PL will display the Accessorial tab showing all your accessorial charges. If you wish to 
reverse charges on an immediate invoice, click on the Immediate tab to display your immediate invoices.
4 Click on the charge(s) that you wish to reverse. If you wish to reverse all charges on an invoice, click on 
 Select All.
5 When you finish selecting your charge(s), click on Save.
Prompt to reprocess invoice
6 When prompted to reprocess the invoice through the Accounting Interface, click on Yes.

INVOICING
Allocating Costs to an Invoice
BILLING AND INVOICING GUIDE 4.2 237
AccellosOne 3PL will create a negative charge in CRIN for the reversed charge. For example, if you 
reverse a bill of lading charge of $20 dated June 1, AccellosOne 3PL will create a bill of lading charge of 
-$20 dated with the current date.
7 Click on Exit to exit.
CANCELING THE REVERSAL OF A CHARGE
When you cancel the reversal of a charge, AccellosOne 3PL creates a positive charge offsetting the negative 
charge created when you reversed the original charge.
1 Enter CRIN.
2 Retrieve the invoice containing the reversed charge(s) that you wish to cancel.
3 Select the reversed charge(s) that you wish to cancel and click on Save.
AccellosOne 3PL will create a positive charge offsetting the negative charge created when you reversed 
the charge.
4 Click on Exit to exit.
Allocating Costs to an Invoice
You can manually allocate a cost against an invoice. The cost could for third party services, internal costs or 
for whatever else you determine is relevant. The cost is entered against an invoice and is reported to the 
financial system through the Daily Register Update.
You set up your costs in CHAR as normal charge codes with GL account codes. You activate costing by 
setting the Cost Entry flag in DBIP (Depositor Billing Profile) to Yes. When costing is activated, you must enter 
at least one cost for each invoice in CTIN (Cost Tracking in Invoice). Invoices without a cost cannot be added 
to the daily invoice register.
DBIP screen showing Cost Entry = Yes
1 Enter CTIN.

INVOICING
Allocating Costs to an Invoice
2 Click on Enter Criteria.
3 Key in your invoice number and click on Execute Query.
4 Click on Charge Block.
5 Click on Create Record.
6 Enter your cost (charge code) in the normal manner.
CTIN screen showing cost for BOL printing
7 When you finish entering your cost(s), click on Return to Main and Master Block.
8 Click on Return to Main and Exit to exit.
9 Click on Release Invoice to DLRE.

BILLING AND INVOICING GUIDE 4.2 239
CASH POSTING SYSTEM
Overview .......................................................................................................... 240
Setting Up Your Bank in BANK...................................................................... 240
Setting Up Customer Cross References in CUCR ....................................... 241
Removing a Cross Reference.................................................................... 242
Entering a Payment in ARCP ......................................................................... 243
Deleting a Payment.................................................................................... 245
Removing an Invoice from a Payment ....................................................... 245
Understanding the Check, Posted and Remaining Amounts..................... 246
Looking Up Summary Information ............................................................. 247
Posting a Payment in CHPO .......................................................................... 247
Removing Payments from a Batch ............................................................ 249
Deleting a Batch......................................................................................... 250
Closing a Batch.......................................................................................... 250
Printing the Batch Audit ............................................................................. 251
Reports............................................................................................................. 251

CASH POSTING SYSTEM
Overview
Overview
The cash posting system allows you to track payments received from your customers and apply these 
payments to specific invoices. You can apply a payment to one or more invoices, you can receive payment 
from one customer and apply the payment to another customer and you can run aging reports to show the 
age of various outstanding accounts.
The cash posting system is linked to the Credit Limit field in DBIP. If you set the Check Credit Limit field to Y 
for Yes and if the total of all outstanding invoices for a given customer exceeds the customer’s credit limit, you 
will not be able to create an order for that customer in ENOR.
There are a maximum of four steps to follow when processing a cash payment:
Setting Up Your Bank in BANK
If you wish to track the bank and account number when posting payments in CHPO, you must set up a bank 
and account number in BANK. You need one record in BANK for each bank account that you post to in 
CHPO.
1 Enter BANK.
2 Click on Create Record.
3 Key in your bank code and press Enter.
ARCP
CHPO
CHPO
REPORTS
In CHPO (Check Posting), you assign the 
payment to a batch.
When you close the batch in CHPO, all the 
payments on the batch are final and cannot 
be modified or reversed.
If required, you can run various reports to 
track your cash payments: CRPR (Cash/
Check Posting Report), ARAR (Accounts 
Receivable Aging Report) and INPR 
(Invoice Payment Report). 
You enter your payments in ARCP (Check/
Cash Entry). 

CASH POSTING SYSTEM
Setting Up Customer Cross References in CUCR
BILLING AND INVOICING GUIDE 4.2 241
4 Key in a description for your new bank code and press Enter.
5 Key in your bank account number and press Enter.
6 Select the appropriate GL account from the dropdown list.
7 Select the appropriate currency from the dropdown list.
8 When you finish setting up your bank, click on Return to Main to exit create record mode.

BANK screen
9 Click on Exit to exit.
Setting Up Customer Cross References in CUCR
Customer cross references allow you to apply a payment to a customer other than the customer issuing the 
check. For example, suppose you have four accounts: COLA_1, COLA_2, COLA_3 and COLA_4. You 
receive a check from COLA_1 and you wish to apply a portion of the check to an invoice from COLA_2, a 
second portion of the check to an invoice from COLA_3 and the remainder of the check to an invoice from 
COLA_4.
You set up customer cross references in CUCR by creating one record for each cross reference. For 
example, if COLA_1 can pay invoices belonging to COLA_2, COLA_3 and COLA_4, you would set up three 
records in CUCR:
COLA_1 --> COLA_2 (invoice customer)
COLA_1 --> COLA_3 (invoice customer)
COLA_1 --> COLA_4 (invoice customer)
If the payment customer in your warehouse always equals the invoice customer (that is, you do not apply a 
payment from one customer to another customer), you do NOT set up customer cross references in CUCR.

CASH POSTING SYSTEM
Setting Up Customer Cross References in CUCR
1 Enter CUCR.

CUCR screen
2 Click on New.
3 Select your payment customer from the Customer Code pick list.
4 Select the corresponding invoice customer from the Invoice Customer Code pick list.
5 Repeat the above two steps for each additional payment customer/invoice customer relationship that you 
wish to set up.
6 When you finish setting up your customer cross references, click on Save to save your changes.

CUCR screen showing five customer cross references
7 Click on Exit to exit.
REMOVING A CROSS REFERENCE
1 Enter CUCR.
2 Select the record in CUCR that you wish to delete.
3 Click on Delete.
4 When prompted to confirm the deletion, click on Yes.
5 Click on Exit to exit.

CASH POSTING SYSTEM
Entering a Payment in ARCP
BILLING AND INVOICING GUIDE 4.2 243
Entering a Payment in ARCP
You enter your payments in ARCP (Cash/Check Entry). You can enter both invoice payments and non-invoice 
payments in ARCP. An invoice payment is a payment related to a specific invoice, while a non-invoice 
payment is money unrelated to a specific invoice that is placed into an account for future use.
There is a one-to-many relationship between payments and checks. That means that you can apply a single 
check to as many invoices that the check will pay. You can also enter partial payments; for example, instead 
of paying one invoice in full, you can partially pay three invoices from one check.
1 Enter ARCP.

ARCP screen
2 Click on New.
3 Key in your customer code and press Enter.
4 Key in the check number and press Enter.
5 Key in your posting date and press Enter or select your posting date from the pop-up calendar.
6 Key in the amount of the check being received and press Enter.
7 If required, select a new currency from the Currency dropdown list.
8 If required, you can add miscellaneous remarks to the payment by clicking on Remarks. After entering your remarks, click on Save to save them or click on Return to exit without saving.

CASH POSTING SYSTEM
Entering a Payment in ARCP

ARCP screen showing check for $100 from customer A
9 In the Detail Block, key in your invoice number and press Enter or select your invoice from pick list. You 
select an invoice from the pick list by clicking on pick list or pressing F10. When the pick list displays, click on invoice(s) that you wish to select. You can click on Select All to select all invoices or 
 Deselect All to deselect all your selections. When you finish making your selections, click on 
Accept to save them.
AccellosOne 3PL will populate the Entered Amount field with the invoice amount — if the check amount 
matches or exceeds the invoice amount. You can enter a partial payment by manually keying an amount 
less than the full invoice amount.
10 If required, you can add miscellaneous remarks to the invoice by clicking on Remarks. After entering your remarks, click on Save to save them or click on Return to exit without saving.
11 If a portion of the check is not being applied to an invoice, key in the non-invoice amount in the NonInvoice Amount field.

CASH POSTING SYSTEM
Entering a Payment in ARCP
BILLING AND INVOICING GUIDE 4.2 245

ARCP screen showing payments applies to three invoices
12 Repeat the above steps for each additional invoice that you want to pay.
13 When you finish adding your invoices, click on Save to save your changes.
14 Click on Exit to exit.
DELETING A PAYMENT
When you delete a payment in ARCP, any invoices linked to the payment are removed from the Invoice Detail 
Block and the payment is deactivated. Deleting a payment is final and cannot be reversed.
1 Enter ARCP.
2 Retrieve the payment that you wish to reverse.
3 Click on Delete.
4 When prompted to confirm the deletion, click on Yes.
5 Click on Exit to exit.
REMOVING AN INVOICE FROM A PAYMENT
When you remove an invoice from a payment, the invoice is considered to be unpaid and once again will 
appear in the pick list of unpaid invoices in the Invoice Detail Block of ARCP.
1 Enter ARCP.
2 Retrieve the payment that you wish to modify.
3 Select the invoice that you wish to remove.

CASH POSTING SYSTEM
Entering a Payment in ARCP
4 Click on Delete.
5 When prompted to confirm the deletion, click on Yes.
6 Click on Exit to exit.
UNDERSTANDING THE CHECK, POSTED AND REMAINING AMOUNTS
There are four amounts in the Header Block of ARCP: the check amount, the non-invoice amount, the posted 
amount and the remaining amount. The check amount and the non-invoice amount are entered by the 
operator, while the posted and remaining amounts are system-calculated.
A payment is considered balanced if the check amount equals the invoice amount plus the non-invoice 
amount.

ARCP screen showing unbalanced payment
Check Amount the amount of the payment as entered by the operator
Non-Invoice Amount the portion of the payment as entered by the operator that is not applied to any 
invoice
Posted Amount the sum of all entered amounts in the Invoice Detail Block; that is, the total 
amount applied to all invoices
Remaining Amount the difference between the check amount and posted amount; that is, check 
amount - non-invoice amount - posted amount = remaining amount 

CASH POSTING SYSTEM
Posting a Payment in CHPO
BILLING AND INVOICING GUIDE 4.2 247
LOOKING UP SUMMARY INFORMATION
The Summary box in ARCP shows the total number of checks entered on a given date, the total check 
amount, the total posted amount and the difference (if any). The Summary as of date used in ARCP is the 
system date when the checks were entered — not the check entry date.

ARCP screen showing Summary box
Posting a Payment in CHPO
You post a payment in CHPO by assigning the payment to a batch containing similar payments; for example, 
all payments received from a certain customer or all payments received between a certain date range. As 
long as the batch remains active, you can add payments to it and remove payments from it. However, once 
the batch is closed, all payments in the batch are final and cannot be modified or reversed.
There are two tabs in CHPO: the Posted Checks tab and the Unposted Checks tab. The Posted Checks tab 
shows all payments assigned to a particular batch. The Unposted Checks tab shows all unposted payments 
that meet the customer and from/to date selection criteria that you enter in the Batch Block of CHPO.
When you post a payment, the check is moved from the Unposted Checks tab to the Posted Checks tab of 
the appropriate batch.
1 Enter CHPO.
TIP Before posting your payments, it is advisable to run the CRPR report to make 
sure that all payments have been correctly entered.

CASH POSTING SYSTEM
Posting a Payment in CHPO

CHPO screen
2 Select the customer whose payments you wish to post from the dropdown list or select .ALL for all customers.
3 If required, select your bank from the dropdown list.
4 If required, key in your batch date and press Enter. If you do not enter a batch date, AccellosOne 3PL will 
use the current date. 
5 Click on Save. AccellosOne 3PL will create a batch number for the new batch and populate the 
Batch Date field with the current date (if you did not manually enter a batch date in the previous step).

CHPO screen showing new batch number for .ALL customer
6 Select your from and to dates from the pop-up calendars. Only payments received between these two 
dates will be included in the batch.
7 When you finish entering your selection criteria, click on Execute Query. If prompted to save your 
changes, click on Yes. AccellosOne 3PL will retrieve all unposted checks that meet the criteria that you 
specified.

CASH POSTING SYSTEM
Posting a Payment in CHPO
BILLING AND INVOICING GUIDE 4.2 249

CHPO screen showing all unposted checks received between the from and to dates that you specified
8 Proceed to select the checks from the Unposted Checks tab that you wish to post to the batch. You can 
select checks manually by clicking in the checkbox beside each check or you can click on Select All 
to select all checks or Deselect All to deselect all your selections. You can also manually deselect a 
selected check by clicking on the appropriate checkbox.
9 When you finish selecting your checks, click on Save. AccellosOne 3PL will move the selected 
checks from the Unposted Checks tab to the Posted Checks tab.
10 Click on Exit twice to exit.
REMOVING PAYMENTS FROM A BATCH
When you remove payments from a batch, AccellosOne 3PL moves the payments from the Posted Checks 
tab to the Unposted Checks tab.
1 Enter CHPO.
2 Retrieve the batch containing the payments that you wish to remove.
3 Click on the Posted Checks tab.

CASH POSTING SYSTEM
Posting a Payment in CHPO

CHPO screen showing Posted Checks tab
4 Proceed to select the checks that you wish to remove. You can select checks manually by clicking in the 
checkbox beside each check or you can click on Select All to select all checks or Deselect All 
to deselect all your selections. You can also manually deselect a selected check by clicking on the appropriate checkbox.
5 Click on Save to move the payments from the Posted Checks tab to the Unposted Checks tab.
6 Click on Exit twice to exit.
DELETING A BATCH
All posted checks on a batch must be removed before you can delete the batch.
1 Enter CHPO.
2 Retrieve the batch that you wish to delete.
3 Make sure that there are no posted checks on the batch.
4 Click on Delete. The status of the batch will change to “Deleted”.
5 Click on Exit twice to exit.
CLOSING A BATCH
When you close a batch in CHPO, all the payments on the batch are final and cannot be modified or reversed. 
Posted payments can no longer be accessed in ARCP.
1 Enter CHPO.
2 Retrieve the batch that you wish to close.

CASH POSTING SYSTEM
Reports
BILLING AND INVOICING GUIDE 4.2 251
3 Click on the Close Batch checkbox to select it.
4 Click on Save.
PRINTING THE BATCH AUDIT
For each check reported on, the batch audit shows the customer code, check number, entry date, check 
amount, batch date, batch status, remarks and the AccellosOne 3PL operator who entered the check.
For each invoice that the check was applied to, the Cash/Check Posting Report shows the invoice prefix, 
invoice number, the invoice type, the invoice amount, the paid amount and remarks.
1 Enter CHPO.
2 Retrieve the batch that you wish to print.
3 Click on Print Report.
Reports
See the Standard Reports Guide.
Accellos, Inc. Cash Posting Batch Audit 03.12.08 14:05 Page 1 of 3
------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------
 Customer: NIK01 Nikolaus Shoes Batch : 19 Bank : BA
 Check Reference Entry Date Check Amount Batch Date Batch Status Remarks Operator
 -------------------- ---------- -------------- ---------- ------------ --------------------------------------------- ----------
 11427A 01.18.08 455.56 03.07.08 Confirmed Wrong date entered on original check DALLEN
 Prefix Invoice # Type Invoice Amount Paid Amount Remarks
 ------ --------- ---- -------------- -------------- --------------------------------------------------
 RC 100000124 RCPT 61.09 61.09
 RN 300000006 RENW 262.25 262.25
 AC 400000052 ACCE 3,985.74 132.22 Partial to blance check
 -------------- -------------- -------------- --------------
 Customer Total : 4309.08 455.56 .00 455.56 * Check Amount Total
------------------------------------------------------------------------------------------------------------------------------------
 Customer: PW005 Pat's Test Transfer Cust Batch : 19 Bank : BA
 Check Reference Entry Date Check Amount Batch Date Batch Status Remarks Operator
 -------------------- ---------- -------------- ---------- ------------ --------------------------------------------- ----------
 DTI123 01.18.08 64.00 03.07.08 Confirmed DALLEN
 Prefix Invoice # Type Invoice Amount Paid Amount Remarks
 ------ --------- ---- -------------- -------------- --------------------------------------------------
 RC 100000031 RCPT 16.00 16.00
 RC 100000042 RCPT 48.00 48.00
 -------------- -------------- -------------- --------------
 Customer Total : 64.00 64.00 .00 64.00 Check Amount Total

CASH POSTING SYSTEM
Reports

BILLING AND INVOICING GUIDE 4.2 253
REPORTS AND REFERENCE
Reports............................................................................................................. 254
BILB (Accessorial Invoicing) ......................................................................... 254
BILB (Renewal Invoicing) ............................................................................... 256
BILB (Immediate Invoice Invoicing) .............................................................. 258
ENAC (Bill Later - Enter Charges) ................................................................. 260
ENIN (Enter Immediate Invoice)..................................................................... 264
BILB (Extra Charge Invoicing) ....................................................................... 266
ADBD (Adjust Billing Data) ............................................................................ 268
LOIN (Look Up Invoices) ................................................................................ 271
LOAC (Look Up Accessorial) ......................................................................... 272
Troubleshooting Billing and Invoicing.......................................................... 276

REPORTS AND REFERENCE
Reports
Reports
See the Standard Reports Guide.
BILB (Accessorial Invoicing)
You use this program to generate and print accessorial bill later invoices. The type of charges that appear on 
these invoices depend on the invoicing option — IND, UALL, UREC or UREN — that you specify in DBIP 
(Depositor Billing Profile).

FIELD DESCRIPTIONS
Batch Type Accessorial
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up 
in CUSE (Customer Service Representatives).

REPORTS AND REFERENCE
BILB (Accessorial Invoicing)
BILLING AND INVOICING GUIDE 4.2 255
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are 
released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Generation
The batch failed to generate successfully or was changed and will have to be 
regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been 
printed.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, 
etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, 
no charge created after this date will be included. Second, if AccellosOne 3PL 
is linked to your accounting system, the Create Date will be the posting date 
for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
BILB (Renewal Invoicing)
BILB (Renewal Invoicing)
You use this program to generate and print renewal batches and invoices. 

Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to 
generate successfully. 
PRNT (Print Audit)
You use this command to print an audit report of a batch.
CONF (Confirm)
You use this command to confirm a batch.
RAUD (Reprint Audit)
You use this command to reprint the audit report of a batch.
FPRT (Final Reprint)
You use this command to reprint an invoice.
Printer Code The printer on which you wish to print the batch.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
BILB (Renewal Invoicing)
BILLING AND INVOICING GUIDE 4.2 257
FIELD DESCRIPTIONS
Batch Type Renewal
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up 
in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are 
released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Confirmation
The batch failed to generate successfully or was changed and will have to be 
regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been 
printed to a printer or to screen.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, 
etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, 
no charge created after this date will be included. Second, if AccellosOne 3PL 
is linked to your accounting system, the Create Date will be the posting date 
for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.

REPORTS AND REFERENCE
BILB (Immediate Invoice Invoicing)
BILB (Immediate Invoice Invoicing)
You use this program to generate and print accessorial bill immediate invoices. 

Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to 
generate successfully. 
PRNT (Print Audit)
You use this command to print an audit report of a batch.
CONF (Confirm)
You use this command to confirm a batch.
RAUD (Reprint Audit)
You use this command to reprint the audit report of a batch.
FPRT (Final Reprint)
You use this command to reprint an invoice.
Printer Code The printer on which you wish to print the batch.
FIELD DESCRIPTIONS
Batch Type Immediate Invoice
Batch Number This number is system generated.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
BILB (Immediate Invoice Invoicing)
BILLING AND INVOICING GUIDE 4.2 259
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up 
in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are 
released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Generation
The batch failed to generate successfully or was changed and will have to be 
regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been 
printed.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, 
etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, 
no charge created after this date will be included. Second, if AccellosOne 3PL 
is linked to your accounting system, the Create Date will be the posting date 
for your warehouse revenue.
Last Audit Number The number of times that the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ENAC (Bill Later - Enter Charges)
ENAC (Bill Later - Enter Charges)
The program is used as a bucket to hold charges generated or entered in ENRE, ENOR and BILB. It holds all 
charges except immediate accessorial charges. You use ENAC to modify or delete charges before confirming 
and printing your invoice. You can also enter charges directly in ENAC if the receipt or order is already 
confirmed or if the charge is unrelated to a specific receipt or order.
Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to 
generate successfully. 
PRNT (Print Audit)
You use this command to print an audit report of a batch.
CONF (Confirm)
You use this command to confirm a batch.
RAUD (Reprint Audit)
You use this command to reprint the audit report of a batch.
FPRT (Final Reprint)
You use this command to reprint an invoice.
Printer Code The printer on which you wish to print the batch.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ENAC (Bill Later - Enter Charges)
BILLING AND INVOICING GUIDE 4.2 261

FIELD DESCRIPTIONS
Accessorial Entry NumberThis number is system generated.
Bill-To Code The customer who is to be billed for the charge
Department Code Only available if activated in COMP (Company Parameters)
Address 1/2/3 Address information retrieved from customer record set up in CUST.
City/ZIP Code City and ZIP code information retrieved from customer record set up in CUST.

REPORTS AND REFERENCE
ENAC (Bill Later - Enter Charges)
Date to Charge If you enter ENAC through ENRE or ENOR, this field displays the system date 
and cannot be edited. If you enter ENAC in stand-alone mode, you can modify 
this field.
For renewal charges, this field shows the date the product renews.
If you enter a date restriction in the Select Block of BILB, a charge may be 
dropped from the batch based on its Date to Charge date.
If AccellosOne 3PL is linked to your accounting system, the Date to Charge 
date does not determine the posting date of the charge in your accounting 
system. The system uses the date the batch was created (the Create Date in 
BILB) as the posting date. 
Reference Description A free format field for internal purposes that does not print on the invoice. If 
the charge is a renewal storage charge, the renewal date will be shown. If the 
charge is an extra charge, the following will appear:
EXIN Batch <999>
where the number in brackets is the extra charge batch number. If the number 
in brackets is negative, this indicates that the extra charge was entered 
through the receipt rater.
Reference Number If you enter ENAC through ENRE or ENOR, the reference number is generated by the system based on the receipt or order number plus type of charge. 
EXAMPLES
Receipt WR - 15 (Initial storage for receipt 15)
Rec 18 (accessorial charge at the header level for receipt 18)
Rec 20 line 3 (accessorial charge for line 3 of receipt 20)
EXIN on WR:190 (extra charge on receipt 190)
Remarks Y = Yes
N = No
If you enter Y for Yes, the Remark Block will be displayed and you can add a 
remark to the charge. 
Charge Code The charge code for the charge.
Tax Code The tax code for the charge code. This field is only enterable if tax code overrides are activated for the charge code in CHAR.
Location Bill Code The location billing code for the charge.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ENAC (Bill Later - Enter Charges)
BILLING AND INVOICING GUIDE 4.2 263
The following fields are query fields only and do not display when you retrieve a record. 
Qualifying Quantity The quantity you are charging for.
Charge Quantity Display field only.
Rate The rate for this charge.
Total The total for this charge.
FIELD DESCRIPTIONS
Accessorial Batch NumberThe accessorial batch on which the charge was placed. If the charge was 
deleted, never placed on a batch or is a renewal charge, the value in this field 
will be zero.
Renewal Batch Number The renewal batch on which the charge was generated. If the charge was 
deleted, never placed on a batch or is an accessorial charge, the value in this 
field will be zero.
Source Reference Flag A = Maximum/minimum charges charged when the actual charge is less than 
the minimum charge or greater than the maximum charge.
E = Extra charges generated automatically in GEXC or ECHP.
F = Freight charges created in A1 Transport.
I = Insurance charges attached to BILB.
O = Order charges entered in ENOR.
R = Receipt charges entered in ENRE or generated automatically in IISP or 
IHAP.
S = Accessorial charges entered through ENAC.
X = Renewal charges created when a renewal batch is generated.
Source Reference NumberThe receipt or order number for the charge (if any).
Source Reference Line 
Number
The line number of the receipt or order for the charge (if any).
Inventory Customer Code The “bill-to” customer code for the charge.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ENIN (Enter Immediate Invoice)
ENIN (Enter Immediate Invoice)
You use this program to enter immediate accessorial charges.
Inventory Level 1/2/3 If the charge is related to a specific receipt or order, the level 1 and 2 values 
for the item.
Current Renewal Date For renewal charges only, the product’s last renewal date.
Next Renewal Date For renewal charges only, the product’s next renewal date.
Entered Quantity For unit-based SKU’s, the quantity expressed in the largest SKU type (for 
example, 1 pallet 40 cases).
Quantity For unit-based SKU’s, the quantity expressed in the smallest SKU type (for 
example, 100 cases).
Weight Measure Code For unit-based SKU’s, the unit of measure for the weight of the product.
Weight The gross weight of the product.
Net Weight The net weight of product.
Linear Measurement 
Code
For unit-based SKU’s, the unit of measure for the cube of the product.
Cube The cube of the product.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ENIN (Enter Immediate Invoice)
BILLING AND INVOICING GUIDE 4.2 265

FIELD DESCRIPTIONS
Invoice Number This number is system generated.
Bill-To Code The customer who is to be billed for the charge
Address 1/2/3 Address information retrieved from customer record set up in CUST.
City/ZIP Code City and ZIP code information retrieved from customer record set up in CUST.
Invoice Date If you enter a date restriction in the Select Block of BILB, a charge may be 
dropped from the batch based on its invoice date.
If AccellosOne 3PL is linked to your accounting system, the invoice date does 
not determine the posting date of the charge in your accounting system. The 
system uses the date the batch was created (Create Date in BILB) as the 
posting date. 
Charge Code The charge code for this charge.
Reference Description A free format field for internal purposes that does not print on the invoice. 

REPORTS AND REFERENCE
BILB (Extra Charge Invoicing)
BILB (Extra Charge Invoicing)
You use this program to generate accessorial extra charges that have been set up in ECHP (Extra Charge 
Profile) or GEXC (General Extra Charges) and attached to a customer, item, consignee or carrier. If you enter 
a receipt extra charge manually in ENRE, you do not use this program.

Tax Code The customer’s tax code. This field is only enterable if tax code overrides are 
activated in CHAR.
Rmk. Y = Yes
N = No
If you enter Y for Yes, the Remark Block will be displayed and you can add a 
remark to the charge. Remarks are for internal purposes only and do not print 
on any invoice.
Qualifying Quantity The quantity that you are charging for.
Charge Quantity Display field only.
Rate The rate for this charge.
Total The total for this charge.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
BILB (Extra Charge Invoicing)
BILLING AND INVOICING GUIDE 4.2 267
FIELD DESCRIPTIONS
Batch Type Extra Order/Receipt Rater
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up 
in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are 
released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated. If you encounter a status message during 
generation, the status of the batch will read “Generated” but in reality the 
batch will not be completely generated and you will have to regenerate it 
before you can confirm it. The purpose of the “Generated” status is to allow 
you to print a partial audit report.
Begun Generation
The batch failed to generate successfully or was changed and will have to be 
regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been 
printed to a printer or to screen.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, 
etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, 
no charge created after this date will be included. Second, if AccellosOne 3PL 
is linked to your accounting system, the Create Date will be the posting date 
for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.

REPORTS AND REFERENCE
ADBD (Adjust Billing Data)
ADBD (Adjust Billing Data)
You use this adjustment program to make changes to your renewal storage charges for existing inventory in 
your warehouse. You can change the next and last renewal dates, the billing profile code set up in IBIP and 
the rate for renewal storage.
Batch The batch number.
Total Entries The number of charges on the batch.
Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to 
generate successfully.
PRNT (Print Audit)
You use this command to print an audit report of a batch.
CONF (Confirm)
You use this command to confirm a batch.
RAUD (Reprint Audit)
You use this command to reprint the audit report of a batch.
FPRT (Final Reprint)
You use this command to reprint an invoice.
Printer Code The printer on which you wish to print the batch.
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
ADBD (Adjust Billing Data)
BILLING AND INVOICING GUIDE 4.2 269

FIELD DESCRIPTIONS
Customer Code The customer whose billing date you wish to adjust.
Item The item whose billing data you wish to adjust.
Period Number The current renewal period.
Alternate Billing Group The customer’s alternate billing group (if any).
Inventory Customer Code The inventory customer when billing subscription is set up and billing records 
have been created.
Next Renewal Date The product’s next renewal date.
Last Renewal Date The product’s last renewal date.

REPORTS AND REFERENCE
ADBD (Adjust Billing Data)
Base Renewal Date Only used when switching from fixed date renewals to anniversary date 
renewals
The date that the product was originally received. If you have changed your 
renewal billing frequency from a fixed date renewal (weekly as of Monday, 
monthly first of the month, monthly last of the month) to an anniversary 
renewal (anniversary monthly, anniversary weekly, daily), you may have to 
adjust this date to make sure that the base renewal date matches the next 
renewal date.
EXAMPLE — Switch from monthly first of month to anniversary monthly on 
06.10.09 (June 10, 2009)
Next Renewal Date = 06.10.09
Last Renewal Date = 05.01.09
Base Renewal Date = 01.25.09
In the above example, you must change your base renewal date from 
01.25.09 (the date that the product was originally received) to 06.10.09 so that 
the next renewal date and the base renewal date match.
Discount Profile Code The product’s discount profile code, if any.
Billing Profile Code The product’s billing profile code.
Next Renewal Invoice 
Date
The system-calculated next renewal invoice date. This field is only populated 
if Number of Days Between Renewal Invoices field in DBIP is set to a value 
greater than zero.
You should consult with your HighJump 3PL support before you manually 
override this date as it could affect the future renewal invoice date.
Last Renewal Invoice 
Date
The last renewal invoice date. This field is only populated if Number of Days 
Between Renewal Invoices field in DBIP is set to a value greater than zero.
BILLING DETAIL BLOCK
Location Bill Code The product’s location billing code (display field only).
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
LOIN (Look Up Invoices)
BILLING AND INVOICING GUIDE 4.2 271
LOIN (Look Up Invoices)
You use this program to look up your invoices. A batch must have a status of confirmed before you can look 
up the invoice in LOIN.

Rate The new rate for renewal storage that will be charged the next time the product renews.
This option is only available if you selected the option R for Renewal Original 
in the Original or Current Rate on Renewals field in DBIP.
Qualifier Quantity/Weight/
Net Weight/Cube
The qualifier quantity for the new rate. This value is generated by the system.
FIELD DESCRIPTIONS
Invoice Number The invoice number or receipt number.
Invoice Prefix Defined in DONU (Document Numbers).
BILLING DETAIL BLOCK

REPORTS AND REFERENCE
LOAC (Look Up Accessorial)
LOAC (Look Up Accessorial)
You use this program to look up all accessorial bill later charges for a given item or level 2/3/4 value. LOAC 
shows the following information about a charge:
 the accessorial entry number and date
 the charge code and amount
 the charge’s invoice (if applicable)
 the receipt or order number and the line number (if applicable)
 the location billing code, qualifying quantity and SKU, charge on quantity and SKU as well as the rate
Invoice Type ACCE = Accessorial
RCPT = Receipt
RENW = Renewal
Customer Code The customer to whom the invoice was sent.
Invoice Date The date that the invoice was created.
Invoice Amount The amount of the invoice in the customer’s currency.
Base Amount Only available if multi-currency billing is activated
The amount of the invoice in your home currency defined in COMP (Company 
Code).
Invoice Register Number The number of the invoice register on which this invoice was placed.
Invoice Register Date The date that the invoice was posted to the invoice register.
Batch Number The batch that the invoice was generated from. If the invoice type is RCPT for 
Receipt, no batch is generated and therefore there is no batch number. 
Payment Amount If you use the cash posting system, the total of all payments made for this 
invoice.
Rollup Company Code If you use rollup invoicing, the rollup company code.
Rollup Invoice Number If you use rollup invoicing, the rollup invoice number.
Rollup Invoice Prefix Defined in DONU (Document Numbers).
FIELD DESCRIPTIONS

REPORTS AND REFERENCE
LOAC (Look Up Accessorial)
BILLING AND INVOICING GUIDE 4.2 273
Records in LOAC are permanent and cannot be deleted except through the program PURA (Purge Accessorial Batch).

FIELD DESCRIPTIONS (HEADER BLOCK)
Customer Code The customer whose charges you wish to look up.
Level 1 The item whose charges you wish to look up.
Level 2/3/4 The level 2/3/4 entity that you wish to look up.
ACCESSORIAL BLOCK
Accessorial Number The accessorial entry number for the charge.
Date The date that the charge was created.

REPORTS AND REFERENCE
LOAC (Look Up Accessorial)
Remarks N = No
Y = Yes
If you entered a remark when you created the accessorial charge, this flag will 
be set to Y for Yes. If you did not enter a remark when you created the accessorial charge, this flag will be set to N for No.
You can view remarks in LOAC by positioning your cursor in the Remark field 
and pressing F3 to view the Remarks Block.
Charge Code The charge code for the charge.
Amount The amount of the charge.
Invoice Prefix Invoice prefixes are defined in DONU (Document Numbers).
Invoice Number If the charge has been invoiced, the number of the invoice will appear in this 
field. If the charge has NOT been invoiced, the following will occur:
 if the charge is associated with a confirmed receipt or order, the receipt or 
order number will appear
 if the charge is associated with an unconfirmed receipt or order, this field will 
be blank
 if the charge is confirmed but is not associated with a specific receipt or 
order (for example, a renewal charge), the number 1 will appear
Total Invoiced The total for invoiced charges. A charge is considered invoiced if the receipt or 
order associated with the charge has been confirmed.
Total Unbilled The total for unbilled charges. A charge is considered unbilled if the receipt or 
order associated with the charge has NOT been confirmed.
Total The total invoiced plus the total unbilled.
ACCESSORIAL BLOCK

REPORTS AND REFERENCE
LOAC (Look Up Accessorial)
BILLING AND INVOICING GUIDE 4.2 275

DETAIL BLOCK
Entered by For manual charges, the operator who entered the charge. For automatic 
charges, the operator who confirmed the receipt or order.
Audited by If you use accessorial authorization, the operator who authorized the charge.
Source Type Accessorial Entry
Extra Charge Rater
Freight
Order
Receipt
Renewal
The type of charge.
Document Number The charge’s receipt or order number. If there is no receipt or order associated 
with the charge, the document number will be zero. 
Line Number The charge’s receipt or order line number. The line number will be zero in the 
following cases:
 there is no receipt or order associated with the charge
 the charge was applied to the order or receipt header — not the line

REPORTS AND REFERENCE
Troubleshooting Billing and Invoicing
Troubleshooting Billing and Invoicing
THE RENEWAL DATES OR QUANTITIES IN THE RENEWAL BLOCK OF LOEN ARE 
WRONG
The information in the Renewal Block is not updated in real-time and may show out-of-date information. In the 
majority of cases, running the renewal preprocessor (RENW) will update the billing information in LOEN. 
THE RATES SHOWN ON MY INVOICE ARE WRONG
If you are using a multi-break charge code, the rate of the charge appearing on the invoice will be averaged. 
For example, if your rate for the first 1,000 lbs. is .60 and for the next 500 lbs. is .50, the rate on an invoice for 
a receipt of 1,500 lbs. would be .57 (the total charges divided by the total weight).
If you enter a charge code in the Default Rate Charge Code field in CHAR (for example, charge code X has 
charge code Y as its default rate charge code), charge code X will use charge code Y’s rates. Any rates that 
you enter for charge code X in RATE will be ignored by the system. 
THE CHARGES ARE WRONG (WEIGHT-BASED BILLING ONLY)
If the charges are wrong for weight-based billing, check the item’s weight. An incorrect weight will lead to 
incorrect charges. You can correct the weight of an item in RESW (Recalculate Standard Weight) or WEAD 
(Weight Adjustment).
Confirmed N = No
Y = Yes
If the charge was entered when processing a receipt or order and this receipt 
or order has not been confirmed, this flag will be set to No. In all other cases, 
this flag will be set to Yes.
Location Bill Code The location billing code for the charge.
SKU Code Qualifier The qualifying SKU code for the charge.
Qualifying Quantity The quantity for qualifying purposes.
SKU Code Charge The charging SKU code for the charge.
Charge Quantity The quantity for charging purposes.
Rate The charge’s rate.
Amount The total amount of the charge.
DETAIL BLOCK

REPORTS AND REFERENCE
Troubleshooting Billing and Invoicing
BILLING AND INVOICING GUIDE 4.2 277
THERE ARE MISSING CHARGES ON MY AUDIT REPORT OR INVOICE
Zero charges do not appear on audit reports and invoices. Look up the quantity and rate for the charge in 
ENAC. If either the quantity or rate of the charge is zero, the charge total will be zero too.
The SKU type that you qualify on and charge on in CHAR must match the SKU type of all items to which the 
charge applies. For example, you cannot set up a pallet-based charge code in CHAR and attach it to an item 
whose quantity breakdown is cases only. If you do, the charge quantity will be zero and no charge will be 
generated.
NO CHARGES GENERATED FOR A CONFIRMED RECEIPT
The receipt is confirmed but not rated. Rate the receipt in RCRA (Receipt Rater).

REPORTS AND REFERENCE
Troubleshooting Billing and Invoicing

BILLING AND INVOICING GUIDE 4.2 279
A
ACAL (Accessorial Charges Audit Look-Up) 222
ACAU (Accessorial Authorization) 225
ACCA (Accessorial Charge Changes Report) 222
accessorial audit, printing 148
accessorial batches
confirming 149
entering restrictions 61, 145, 152, 157, 204
accessorial bill immediate charges 198
accessorial bill later charges 180
accessorial charges
adding to a confirmed order 192
entering in ENAC 190
overview 6
splitting out by means of invoice types 178
accessorial invoice, generating and printing 144
ADBD (Adjust Billing Data)
changing other parameters 50
changing renewal storage dates 50
changing renewal storage rates 48
overview and field descriptions 268
allocating costs to an invoice 237
alternate billing groups 93
ARCP (Cash/Check Entry) 243
audit batch restrictions in BILB 160
automatic pre-renewal billing 127
B
backdating open orders and receipts 178
BANK (Bank Code) 240
batches
deleting 169
looking up charges on 169
modifying a charge on 172
regenerating 169
reprinting 169
troubleshooting 172
BILB (Accessorial Invoicing)
overview and field descriptions 254
using 144
BILB (Daily Invoice Register) 163
BILB (Extra Charge Invoicing)
overview and field descriptions 266
using 155
BILB (Immediate Invoice Invoicing)
overview and field descriptions 258
using 203
BILB (Renewal Invoicing)
overview and field descriptions 256
using 150
billing audit system
authorizing your charges 223
changing and deleting charges 219
overview 216
purging change records in PACA 226
setting up 217
tracking changes to ENAC and ENIN charges 221
billing by warehouse 227
billing entities, overview 22
Billing Entity Minimum Charge Code field (IBIP) 19
billing setup programs 10
billing subscription 91
billing/invoicing cycle, overview 8
Bill-To Code field, using 90
Breakdown Number field (INRE) 13
BTCS (Billing Subscription) 91
C
cancelling a rate change 32
cash posting system
closing a batch in CHPO 250
entering a payment in ARCP 243
overview 240
posting a payment in CHPO 247
printing the audit batch 251
setup 240
CDAV (Daily Average for Customer) 36
CDMX (Customer Daily Maximum) 42
INDEX

INDEX
changing renewal storage rates 48
charges
deleting from a batch 171
looking up on a batch 169
missing 172
modifying on a batch 172
splitting out 178
charging by physical pallet 81
check-in only billing 35
CHGR (Charge Group) 28
CHPO (Check Posting) 247
CLOL (Close Open Lots) 99
closing open lots 99
COD extra charge 55
Column field (INRE) 13
combination type charges 88
confirming
accessorial batches 149
extra charges 84, 159
renewal batches 155
costs, allocating to an invoice 237
credits, entering in ENAC 196
credits, entering in ENIN 201
CRIN (Credit Invoice) 236
cross-docking billing 108
CUCR (Customer Cross Reference) 241
CUDE (Customer Departments) 198
CUFC (Customer Fixed Charges) 123
CURX (Currency Exchange Rates) 124, 125
customer departments 198
customer fixed charges 123
D
daily average billing 36
Daily Invoice Register (BILB) 163
DECH (Density Charge Codes) 118
deleting batches 169
deleting charges from a batch 171
DELO (Depositor Load Type Charges) 94
Density Charge Codes (DECH) 118
density rating 118
Description Bottom field (INRE) 13
Description field
(INRE) 13
Description Top field (INRE) 13
discounts on initial storage and handling 104
DPRO (Discount Profile Code) 104
E
ECHP (Extra Charge Profile)
field descriptions 71
overview 54
EDEC (EDI Receipt Extra Charge) 83
emailing of confirmed invoices 168
ENAC (Bill Later - Enter Charges)
entering a credit in 196
entering charges in 190
entering customer department in 198
looking up charges in 169
overview and field descriptions 260
ENIN (Bill Immediate - Enter Charges)
entering a credit in 201
overview and field descriptions 264
using 198
exceed daily average billing (renewal storage) 40
extra charge audit, printing 158
extra charges
activating 83
assigning location billing codes to 59
charging for partial quantities 62
confirming 84, 159
for third party billing 82
generating a batch for 155
group descriptions 55
printing 158
receipt 183
specifying restrictions for 60
F
flat rate charges 120
G
generating
a renewal batch 150
a warehouse receipt invoice 142
accessorial bill immediate charges 198
an accessorial batch 144
an extra charge batch 155
GEXC (General Extra Charges)
field descriptions 65
overview 54
H
Handling Minimum Charge Code field (IBIP) 19
hourly based charges 121
I
IDRA (Increase/Decrease Rates) 32
immediate accessorial audit, printing 206
immediate accessorial batch, confirming 207
immediate accessorial batch, generating 203
IND invoicing 132, 133
Initial Storage Minimum Charge Code field (IBIP) 19
INRE (Invoice Register Definition) 12
inventory levels, invoicing by 234
Invoice Breakdown Code field (INRE) 13
invoice only customer 90
invoice register definition (INRE), setting up 12
invoice types in BILB 178
invoices
allocating costs to 237
emailing 168
looking up 173
printing 174
reprinting 169
invoicing by inventory level 234
invoicing by warehouse 227

INDEX
BILLING AND INVOICING GUIDE 4.2 281
invoicing types, overview 7
ITAS (Item Alternate Sorts) 93
IXDP (Item X-Dock Profile) 108
L
labor charges 121
line types for receipts 100
LOAC (Look Up Accessorial)
field descriptions 272
overview and using 175
load type charges 94
LOIN (Look Up Invoices)
overview and field descriptions 271
using 173
looking up
charges on a batch 169
invoices 173
renewal storage 46
M
maximum daily billing 34
maximum/minimum charges
defaults 17
for a given receipt/order 23
for billing entities 22
item-specific 18
overview 16
Minimum / Maximum Accessorial Charge Code field (DBIP)
21
Minimum / Maximum Receipt Charge Code field (DBIP) 20
Minimum / Maximum Renewal Charge Code field (DBIP)
21
minimum charges for a given receipt/order 23
minimum total invoices 27
missing charges 172
monthly minimum billing 27
monthly renewal invoicing 43
multi-currency billing 124
multiple units of a SKU, billing by 103
N
number of pallet positions billing 42
O
OAUD (Accessorial Charges Authorization Audit) 224
occurrence as a qualifier code 120
OEXC (Add Accessorial Charge to Order) 192
OPAU (Accessorial Charges by Operator) 223
open lots 96
OPID, calculating renewal storage by 45
ORCH (Order Charges) 210
order accessorial charges 186
order minimum charge 23
OREC (EDI order Extra Charge) 83
overriding quantity for extra charge 84
overriding receipt charges 100
P
PACA (Purge Accessorial Charge Audit) 226
partial quantities, charging for 62
physical pallet, charging by 81
pre-renewal billing 127
printing
accessorial audit 148
extra charge audit 158
invoice 174
renewal audit 153
R
rates
cancelling 32
changing 30
REAS (Entry Reason Code) 218
receipt accessorial charges 180
receipt charges
overriding 100
overview 6
receipt extra charges
adding to a confirmed receipt 194
entering 183
generating for IND customers 133
generating for UREN customers 141
receipt line types 100
receipt minimum charge 23
RECH (Receipt Charges) 208
regenerating batches 169
renewal audit, printing 153
renewal batches
confirming 155
generating 150
renewal charges 6
renewal dates, changing 50
renewal invoices, troubleshooting 172
renewal invoicing by receipt 44
renewal preprocessor (RENW) 47
renewal storage
backdating open orders and receipt 178
by OPID 45
changing rates of 48
looking up 46
Renewal Storage Line Minimum Charge Code field (IBIP)
19
RENW See renewal preprocessor
reports
OPAU (Accessorial Charges by Operator) 223
reprint archive function in BILB 162
reprinting invoices 169
restrictions in batch programs 61, 145, 152, 157, 204
Revenue Analysis field (INRE) 14
reversing charges on confirmed invoices 236
REXC (Enter Receipt Extra Charges) 194
rollup invoicing 212
S
seasonal or special billing 101
setup, billing 10

INDEX
single level billing (extra charge rater) 59
single level billing (renewal storage) 43
SKU, billing by multiple units of 103
Source Flag field (BILB) 147
surcharges 113
T
taxes 102
third party billing 90
third party billing in ECHP 82
Threshold Accessorial Charge Code field (DBIP) 21
total exceed daily average billing (renewal storage) 41
transferring charges to a third party 90
troubleshooting
extra charge batches 160
general 276
renewal invoices 172
types of charges 6
U
UALL invoicing 135
UREC invoicing 137
UREN invoicing 139, 141
W
warehouse receipt invoices, generating and printing 142
X
X-dock billing 108
