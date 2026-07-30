---
title: "Faturamento — Configuração de Tarifas e Cobranças"
description: "Invoice register, tarifas, mínimos e máximos, charge groups, renewal storage e tópicos avançados."
layout: default
---

# Faturamento — Configuração de Tarifas e Cobranças

Invoice register, tarifas, mínimos e máximos, charge groups, renewal storage e tópicos avançados.

**Fluxo principal:** `INRE (registro) -> RATE/CHAR (tarifas) -> CHGR (grupos) -> RENW (renewal)`

> Fonte: manuais A, N do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction <a id="introduction"></a>

*Manual A — Billing and Invoicing*

# Manual A — Billing and Invoicing Guide (Faturamento e Cobrança)
> **ID do Manual:** A  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Sistema completo de billing 3PL: receipt charges, renewal charges, accessorial charges. Setup de tarifas (RATE/CHAR), invoice register (INRE), extra charges (GEXC), invoicing cycles (BILB/BACO), credit invoices, cash posting (CHPO/ARCP), surcharges, taxes, open lots, cost tracking.
---

### Welcome <a id="welcome"></a>

Welcome to the Billing and Invoicing Guide, the complete reference guide to the billing and invoicing programs of AccellosOne 3PL. Designed for intermediate and advanced users of AccellosOne 3PL, this manual has been divided into four parts. 
Basics is essential reading for all users of this manual. It describes the types of charges and invoicing in 
AccellosOne 3PL and provides an overview of the billing/invoicing cycle.
Billing is a high-level look at billing issues. It is intended for advanced users who need to understand how charges are calculated in AccellosOne 3PL so that they can set up charge codes and profiles correctly to ensure that customers receive accurate and complete invoices.
Invoicing is intended for intermediate users who need a thorough knowledge of invoicing to do their job, but do not set up charge codes or billing profiles or need to understand how charges are calculated in AccellosOne 3PL. The information in this section does not require a knowledge of the high-level billing issues discussed in Part II.
Reference provides a listing of common billing and invoicing reports as well as field-by-field descriptions of all billing and invoicing programs. It can be referred to by users at any level on an as-required basis.

### Related Reading <a id="related-reading"></a>

This manual does not include setup procedures for the various AccellosOne 3PL billing setup programs such as CHAR, RATE, IISP, IRSP, etc. Refer to the Setup Guide for detailed instructions on these programs.
Refer to the Core Documents Guide for samples of various billing related documents such as the accessorial audit and accessorial invoice.

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting 

Guide to ActiveDesktop/A13PLlogging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating product, entering hold adjustments
Operations 2 Guide appointment planner, back orders, batch picking, manual packing, customer relationship management, EDI, faxing and auto-printing, item substitution, kitting, labor tracking, Operational Board, pallet control, inventory attributes, item process values, outbound load building, quick response labels
Physical Inventory 
Guide setup and operational programs for physical inventory as well as the physical inventory reports
RF Guide setup programs for RF (Radio Frequency), RF receiving, RF picking, entering process values in RF, voice-activated picking, order assignment system, equipment tracking, interleaving, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

## Basics <a id="basics"></a>

*Manual A — Billing and Invoicing*

### Billing and Invoicing Overview <a id="billing-and-invoicing-overview"></a>

There are essentially three types of charges in AccellosOne 3PL:
 receipt charges
 renewal charges
 accessorial charges

### RECEIPT CHARGES <a id="receipt-charges"></a>

Receipt charges are any charges that are incurred when product is received in the warehouse. Receipt charges come in two forms: automatic charges and manual charges.
Automatic receipt charges are set up in IISP (Initial Storage Profile) and IHAP (Item Handling Profile). They can also be set up in ECHP (Extra Charge Profile). Manual receipt charges are entered in the Header Block of ENRE by setting the Receipt Extra Charge flag to Yes. 
Receipt charges accumulate in ENAC (Enter Charges - Bill Later) and can be invoiced once the receipt has been confirmed. 

### RENEWAL CHARGES <a id="renewal-charges"></a>

Renewal charges are any charges that are incurred after the product has been received in the warehouse and any receipt charges calculated. There are no manual renewal charges. You set up automatic renewal charges in IRSP (Item Renewal Storage Profile). 
Renewal charges must be generated in a batch program. Once generated, they accumulate in ENAC (Enter 
Charges - Bill Later).

### ACCESSORIAL CHARGES <a id="accessorial-charges"></a>

Accessorial charges are any charges that you enter through the program ENAC (Enter Charges - Bill Later). 
Manual accessorial charges can be entered directly into ENAC or can be entered at either the header or line detail level in ENRE (Enter Receipts) or ENOR (Enter Orders). Automatic accessorial charges are set up in 
GEXC (General Extra Charges) and ECHP (Extra Charge Profile).
You use accessorial charges to bill for miscellaneous type charges such as a charge for blast freezing, palletization, a bill of lading, etc. that apply to a specific receipt or order. You can also use accessorial charges to bill for general or one-time miscellaneous charges that are not attached to a particular order or receipt; for example, rent, overtime, faxing and long distance charges.

### Types of Invoicing <a id="types-of-invoicing"></a>

There are four possible invoicing options available in AccellosOne 3PL for any given customer. The invoicing option that you choose determines the type of charges that will appear on an invoice. 
You define your invoicing options for a customer in the Invoice Printing Profile Code field in DBIP (Depositor 
Billing Profile). If you wish to invoice differently for certain customers, you must set up multiple depositor billing profiles in DBIP and then attach them to the appropriate customers.

Billing Profile STD in DBIP showing IND invoicing
IND three invoice types
 a warehouse receipt invoice containing receipt charges such as initial storage/handling and extra charges
 an accessorial invoice containing accessorial charges such as receipt/order accessorial charges and extra charges set up in GEXC and ECHP
 a renewal invoice containing renewal storage charges 
UALL an accessorial invoice containing all charges
UREC two invoice types
 an accessorial invoice containing receipt charges and accessorial charges
 a renewal invoice containing renewal storage charges 
UREN two invoice types
 a warehouse receipt invoice containing receipt charges
 an accessorial invoice containing accessorial charges and renewal storage charges

### Overview of Billing/Invoicing Cycle <a id="overview-of-billing-invoicing-cycle"></a>

There are seven basic steps in the billing/invoicing cycle.
BILB
ENAC
BILB
You generate your batch in BILB.
You print your audit report in BILB.
If required, you edit your charges.
You confirm your batch and print your invoice in 
BILB. 
You run the daily invoice register. This program posts the various charges to your management and sales reports. If your accounting software is linked to AccellosOne Enterprise 3PL, the daily invoice register will create your general ledger interface file.
CHRF, CHOF, 
RCRA
When you confirm a receipt in CHRF or confirm an order in CHOF, all charges — both automatic and manual — are generated. If you use the receipt rater program, receipt charges are generated when you run RCRA. 
BILB
BILB
ENRE, ENOR
You add any extra or accessorial charges to a receipt in ENRE or to an order in ENOR.

## Basic Billing Setup <a id="basic-billing-setup"></a>

*Manual A — Billing and Invoicing*

### Billing Setup <a id="billing-setup"></a>

AccellosOne 3PL uses charge codes to generate charges in the billing system. Charge codes are set up in 
CHAR (Charge Code) and RATE (Depositor Billing Rates). If there is no charge for a particular type of storage (for example, you have no receipt charges for inbound product), you can use a “No Charge” type charge code.
Charge codes are attached to profiles and it is by means of these profiles that most charges are generated.
There are eight mandatory setup programs in AccellosOne 3PL for billing and invoicing:
DILP (Depositor Inventory Level Profile) 
In this program, you define the inventory level you wish to bill at plus the default minimums for initial storage, renewal storage and handling.
DBIP (Depositor Billing Profile) 
In this program, you define the invoicing type plus minimums at the invoice level for receipt, renewal and accessorial charges.
IISP (Item Initial Storage Profile) 
In this program, you set up the charges for initial storage and the discount period, if any.
IRSP (Item Renewal Storage Profile) 
In this program, you set up the charges for renewal storage and your renewal dates.
IHAP (Item Handling Profile) 
In this program, you set up the charges for handling.
IBIP (Item Billing Profile)
In this program, you assign the initial storage, renewal storage, handling and date profiles to the item profile. You also define the local overrides, if any, for the initial storage, renewal storage and handling minimums set up in DILP.
LODE (Location Billing Codes) 
In this program, you set up location billing codes if you charge different rates of storage for different areas in your warehouse or you want to assign revenue to different GL accounts.
INRE (Invoice Register Definition)
In this program, you set up your invoice register. An invoice register is a listing of all invoices produced on a certain date or range of dates. For each invoice on the listing there is a total for the invoice plus a breakdown by type of charge (for example, Initial Storage, Handling, Blast Freezing, etc.). 

There are also two optional setup programs for extra charges:
The following flow chart shows the seven mandatory setup programs for billing and invoicing and how they are connected to customers and items.
GEXC (General Extra Charges) 
In this program, you set up charges that are automatically applied to a receipt or to an order when you run BILB.
ECHP (Extra Charge Profile) 
In this program, you set up charges that may or may not be related to a specific receipt or order and can be either manually or automatically applied by running BILB. 
CUST
DILP DBIP
ITEM
IBIP
IRSP renewal storage
IISP IHAP initial storage handling
LODE LODE
Location billing code Location billing code
ITEM BILLING PROFILE if required, local overrides of the minimums defined in DILP
DEPOSITOR BILLING PROFILE
- invoicing type
- minimums at the invoice level 
for receipt, renewal and 
DEPOSITOR INVENTORY LEVEL 
PROFILE
- inventory level you wish to bill at 
- default minimums at the customer 
level for initial storage, renewal storage and handling

### SETTING UP THE INVOICE REGISTER DEFINTION (INRE) <a id="setting-up-the-invoice-register-defintion-inre"></a>

An invoice register is a listing of all invoices produced on a certain date or range of dates. For each invoice on the listing there is a total for the invoice plus a breakdown by type of charge (for example, Initial Storage, 
Handling, Blast Freezing, etc.). 
You must set up your invoice register in INRE before you can run BILB (Daily Invoice Register). When you run 
BILB, AccellosOne 3PL accumulates all charges incurred since the last time that you ran the program and generates the invoice register and other financial reports. If AccellosOne 3PL is linked to your accounting system, DLRE also updates your accounts receivable and general ledger.
Daily Invoice Register showing section for renewal storage
You define three things in INRE:
 the invoice breakdown code or type (Accessorial, Freight, Receipt and Renewal)
 the column or columns on the invoice register (you need to define one column for each type of charge that you want to break out; for example, Initial Storage, Handling, etc.)
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

FIELD DESCRIPTIONS
Breakdown Number Mandatory
You set up one breakdown number for each invoice type you require. Valid types of invoices are Accessorial, Freight, Receipt and Renewal (see Invoice 
Breakdown Code field).
Description Mandatory
Your breakdown description
Invoice Breakdown Code ACC = Accessorial
FRT = Freight
RCPT = Receipt
RENW = Renewal
The type of invoice.
Column Mandatory
You can have up to eight columns on each invoice. Column 9 is reserved for miscellaneous charges.
Description Top Mandatory
The first line of your column description (for example, INITIAL).
Description Bottom Optional
The second line of your column description (for example, STORAGE).

1 Enter INRE.
2 Click on Enter Criteria then Execute Query to see whether the invoice register has already been set up. If the invoice register has not been set up, click on Create Record. If the invoice register has been set up, refer to the next procedure ([Setting Up Additional Invoice Types](faturamento-setup.html#setting-up-additional-invoice-types)) for instructions.
3 Key in 1 for your first breakdown number and press Enter.
4 Key in a description for your first breakdown number (for example, Warehouse Receipts) and press 
Enter.
5 Use your pick list to select the appropriate invoice breakdown. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
6 In the Column Number field, key in 1 and press Enter to set up your first column.
7 In the Description Top field, key in the first line of your description for this column (for example, INITIAL) 
and press Enter.
8 In the Description Bottom field, key in the second line of your description for this column if required (for example, STORAGE) and press Enter.
9 When the Revenue Analysis Block appears, click on Create Record. 
10 Use your pick list to select the appropriate revenue analysis code for your first column.
Revenue Analysis (REVA)
Mandatory
The revenue analysis codes attached to this column. When you run DLRE, 
AccellosOne 3PL will search for all charges whose charge codes are attached to the revenue analysis code(s) that you specify for each column. 
AccellosOne 3PL will accumulate the charges for each column and sort them by customer code. 
If AccellosOne 3PL finds any charges whose revenue analysis codes are not listed in the columns that you define, the charges will be listed in the Miscellaneous column of the Invoice Register.
FIELD DESCRIPTIONS

Invoice Register Definition showing a revenue analysis code of FE assigned to column 1
11 If you have further revenue analysis codes to add to this column, repeat the previous step.
12 When you finish entering your revenue analysis codes for the first column, click on Return to Main to exit create mode.
13 Click on Column Block.
14 Click on Create Record.
15 Key in 2 and press Enter to set up your second column.
16 In the Description Top and Description Bottom fields, key in the first and second lines of your description for this column and press Enter after each field.
17 Use your pick list to select the appropriate revenue analysis codes for your second column.
18 Repeat the previous step for each revenue analysis code that you wish to add to your second column.
19 Repeat the above steps for each additional column that you wish to add to this invoice type. When you finish setting up all your columns for your first invoice type, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit the program.

### SETTING UP ADDITIONAL INVOICE TYPES <a id="setting-up-additional-invoice-types"></a>

1 Enter INRE.
2 Click on Enter Criteria then Execute Query to display the invoice type that you set up in the main procedure.
3 Click on Create Record.
4 Key in 2 as your breakdown number and press Enter.
5 Key in a description for your second invoice type and press Enter.
6 Set up your column numbers, column headings and the revenue analysis codes that belong to each column.

7 When you finish all your columns and revenue analysis codes for your second invoice type, click on 
Return to Main to exit create mode. Then click on Master Block and Exit to exit the program.

### Working With Maximum and Minimum Charges <a id="working-with-maximum-and-minimum-charges"></a>

AccellosOne 3PL supports multiple maximum and minimum charges. You can apply maximum/minimum charges to a billing entity, receipt invoice line, receipt invoice, renewal invoice, charge code or individual receipt/order. When multiple maximum/minimum charges apply to the same item, the individual maximum/ minimum are calculated at each level — billing entity, receipt line, etc. — independently of the maximum or minimum charges at another level.
EXAMPLE
You charge by the PALLET and you receive 1 PALLET.
minimum charge in RATE = 5.00 rate = 2.50 per pallet initial storage minimum = 10.00 billing entity minimum = 25.00 receipt invoice minimum = 100.00
Because of the various minimums that apply, the total charge for the one pallet would be $100.00.
There are two ways in which minimums are shown in AccellosOne 3PL. If the minimum is set up in RATE, the minimum value replaces the actual value; for example, $5.00 (the minimum) replaces $2.50 (the actual charge). If the minimum is set up in any other program (for example, any minimum field in IBIP), two charges are generated whenever a minimum charge is activated: the actual charge plus whatever amount is needed to bump up the actual charge to the minimum charge. The sum of the two charges equals the minimum charge.
CHARGE 
QUANTITY RATE CHARGE EXPLANATION
5.00 5.00 added to meet initial storage minimum of 10.00
15.00 15.00 added to meet billing entity minimum of 25.00
75.00 75.00 added to meet receipt invoice minimum of 
100.00
100.00 Total

### DEFAULT MAXIMUM/MINIMUM CHARGES <a id="default-maximum-minimum-charges"></a>

You set up your default maximum/minimum charges in DILP. These defaults apply to all of a customer’s items. If this default does not apply to certain items, you must override the default by setting up a maximum/ minimum charge in IBIP (Item Billing Profile). 
There are four minimum charges set up in DILP:
 billing entity minimum
 renewal storage line minimum
 initial storage minimum
 handling minimum
NOTE Maximum/minimum charges are always calculated independently of any other charges that may be added to a receipt or to an order. For example, suppose you receive product from customer A and an initial storage minimum is invoked because of the quantity of product received. Then you add an accessorial charge to your receipt in ENRE for special handling.
Even if the sum of the initial storage charge and the accessorial charge exceeds the initial storage minimum, an initial storage minimum will still be triggered because the system will ignore accessorial charges when determining whether an initial storage minimum is required.
FIELD DESCRIPTIONS
Billing Entity Minimum 
Charge Code
See [Maximum/Minimum Charges for Billing Entities](faturamento-setup.html#maximum-minimum-charges-for-billing-entities).
Renewal Storage Line 
Minimum Charge Code
This minimum charge applies to each renewal storage entity on your invoice. 
A renewal storage entity consists of all product in which:
 the appropriate inventory level values are the same (if you bill at level 1, all level 1 values must be the same but levels 2 and 3 if any can differ; if you bill at level 2, all levels up to level 2 must be the same but level 3 if any can differ) 
 the renewal period is the same
 the location bill code is the same
If there is no minimum charge for renewal storage lines, set this field to NC for 
No Charge.
Initial Storage Minimum 
Charge Code
This minimum charge applies to initial storage charges on a particular receipt line. If there is no minimum charge for initial storage, set this field to NC for No 
Charge.

DILP screen showing minimum charges for billing entities and initial storage

### ITEM-SPECIFIC MAXIMUM/MINIMUM CHARGES <a id="item-specific-maximum-minimum-charges"></a>

You set up your item-specific maximum/minimum charges, if any, in IBIP. These maximum/minimum charges apply only to those items that your IBIP profile is attached to. IBIP maximum/minimums are local (that is, itemlevel) maximum/minimums that override the customer level defaults defined in DILP.
There are four item-specific maximum/minimum charges set up in IBIP:
 billing entity minimum
 renewal storage line minimum
 initial storage minimum
 handling minimum
Handling Minimum 
Charge Code
This minimum charge applies to the handling charges on a particular receipt line. If there is no minimum charge for handling, set this field to NC for No 
Charge.
FIELD DESCRIPTIONS

FIELD DESCRIPTIONS
Billing Entity Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the default billing entity maximum/minimum charge defined in DILP (Depositor 
Inventory Level Profile). 
Renewal Storage Line 
Minimum Charge Code
Optional
If you enter a charge code in this field, this charge code will override the default renewal storage line maximum/minimum charge defined in DILP (Depositor Inventory Level Profile).
Initial Storage Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the default initial storage maximum/minimum charge defined in DILP (Depositor 
Inventory Level Profile).
Handling Minimum 
Charge Code
Optional
If you enter a charge code in this field, this charge code will override the default handling maximum/minimum charge defined in DILP (Depositor Inventory Level Profile). 

IBIP screen showing minimum for renewal storage line

### MINIMUM CHARGES FOR A GIVEN INVOICE <a id="minimum-charges-for-a-given-invoice"></a>

You set minimum charges for a given invoice in DBIP. There are four minimum charges set up in this program:
 receipt charge
 renewal storage minimum
 accessorial minimum
 threshold accessorial minimum
FIELD DESCRIPTIONS
Minimum / Maximum 
Receipt Charge Code
Optional
If you have a minimum charge for receipt charges on an invoice, enter the appropriate charge code. If there is no minimum charge for receipt charges, leave this field blank.
NOTE Maximum charges for receipt charges are not supported in this release of AccellosOne 3PL.

Minimum / Maximum 
Renewal Charge Code 
Optional
If you have a minimum charge for renewal charges on an invoice, enter the appropriate charge code. If there is no minimum charge for renewal charges, leave this field blank.
NOTE Maximum charges for renewal charges are not supported in this release of AccellosOne 3PL.
Minimum / Maximum 
Accessorial Charge Code 
Optional
If you have a minimum charge for accessorial charges on an invoice, enter the appropriate charge code. If there is no minimum charge for accessorial charges, leave this field blank.
NOTE Maximum charges for accessorial charges are not supported in this release of AccellosOne 3PL.
Threshold Accessorial 
Charge Code
Optional
This field allows you to specify a minimum dollar value for an accessorial invoice. If you specify a minimum, no accessorial invoice will print if it has not reached the minimum value. The charges on the invoice will continue to accumulate until the threshold is met. 
If there is no minimum value for an accessorial invoice, leave this field blank.
FIELD DESCRIPTIONS

DBIP screen showing two minimum charges: one for receipt charges and one for an accessorial invoice

### MAXIMUM/MINIMUM CHARGES FOR BILLING ENTITIES <a id="maximum-minimum-charges-for-billing-entities"></a>

A billing entity is all product received on one receipt in which all the levels of inventory used in billing are identical.
For example, suppose you have a customer with two inventory levels — item and lot number — and you bill at the lot level. You are receiving product from this customer and because of the way in which the truck is loaded you receive the following:
Lines 1 and 3 — although on different receipt lines — represent identical product with the same item and lot numbers and are therefore considered a single billing entity. When the system calculates initial storage and handling, lines 1 and 3 will be consolidated into a single billing entity and if the total of this billing entity is less than the minimum charge, the actual charge will be replaced by the minimum charge.
EXAMPLE
LINE 
NUMBER ITEM
LOT 
NUMBER QUANTITY
1 item 1 101 100 cases
2 item 2 101 200 cases
3 item 1 101 5 cases
4 item 1 299 80 cases

line 1 --> initial storage: $10/ initial handling: $5 line 2 --> initial storage: $15/ initial handling: $7.50 line 3 --> initial storage: $2/ initial handling: $1.25 line 4 --> initial storage: $10/ initial handling: $5 billing entity minimum charge = $20.00
If you bill this customer at the item level, the totals for the three billing entities will be calculated as follows:
line 1 and 3 = 15 + 3.25 = 18.25 line 2 = 22.50 line 4 = 15
The charge for line 2 (item 2, lot 101) is above the minimum and therefore not affected by the minimum charge. However, the charges for lines 1 and 3 (item 1, lot 101) and line 4 (item 1, lot 299) are below the minimum charge and therefore the actual charge will be replaced by the minimum charge.

### MINIMUM CHARGES FOR A GIVEN RECEIPT/ORDER <a id="minimum-charges-for-a-given-receipt-order"></a>

You can define minimum charges for individual receipts and orders when invoicing through UALL. The minimum charge is based on the total number of charges regardless of type applied to a given receipt/order.
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
NOTE Billing entity minimums apply to initial storage and handling only. They are not required for renewal storage because the system automatically consolidates receipt lines containing identical product when it calculates renewal storage.

$10.00 (extra charge on item 3)
$90.00 total
The minimum charge does not apply as the order total ($90) exceeds the minimum charge ($80).
You set up minimum receipt charges by attaching the appropriate charge code to the Accessorial Invoice 
Receipt Minimum Charge Code field in DBIP (Depositor Billing Profile). Likewise, you set up minimum order charges by attaching the appropriate charge code to the Accessorial Invoice Order Minimum Charge Code field in DBIP.
DBIP screen showing Accessorial Invoice Receipt Minimum Charge and Accessorial Invoice Order 
Minimum Charge fields

### SETTING UP MAXIMUM/MINIMUM CHARGE CODES <a id="setting-up-maximum-minimum-charge-codes"></a>

Maximum/minimum charge codes should be set up with a charge type of SING, a charge definition of B for 
Break and a single break in RATE.
1 Enter CHAR and click on Create Record.
2 Key in your charge code and description.
3 Press Enter twice to bypass the Reference and External Reference fields.
4 In the Charge Type field, key in SING and press Enter.
5 In the Charge Definition field, key in B for Break and press Enter.

Charge Code (CHAR)
6 Key in your general ledger, revenue analysis and invoice type values.
7 Key in your charge on and qualify on SKU codes.
8 Press Enter to bypass the Default Rate Charge Code field.

Depositor Billing Rates (RATE)
9 In RATE, key in the customer to whom the charge applies and press Enter. If the charge applies to all customers, use .ALL as your customer code.
10 Key in your effective date and press Enter.
11 In the Number of Breaks field, key in 1 and press Enter.
12 In the Minimum Charge field, key in your minimum charge and press Enter. If there is no minimum charge, press Enter with this field set to the default value of 0.
13 In the Maximum Charge field, key in your maximum charge and press Enter. If there is no maximum charge, press Enter with this field set to the default value of 99999999999.99.
14 Press Enter to bypass the remaining fields in CHAR.
15 When the Detail Block appears, press Enter to accept the default value in the Quantity Break field.
16 In the Charge Amount field, key in 0 and press Enter.

Detail Block of RATE showing a single break with a charge amount = 0
17 Click on Master Block and Return to Main. Then click on Exit to exit.

### MONTHLY MINIMUM BILLING <a id="monthly-minimum-billing"></a>

This billing option allows you to define a minimum monthly charge when the total of all invoices for a given month is less than the minimum. For example, suppose you define a monthly minimum charge of $100. If the total of all invoices — warehouse receipt invoices, renewal invoices, accessorial invoices, etc. — is $55, 
AccellosOne 3PL will charge an additional $45 to reach the minimum. 
The following conditions apply to monthly minimum billing:
 The customer’s status must be A for Active in CUST.
 If the total invoice amount is zero or if no invoice is generated, the monthly minimum charge will apply if there is still inventory in the warehouse.
 All invoices created with an invoice date between the 1st of the month and the batch create date of the minimum invoice will be counted when calculating the minimum. For example, if the minimum invoice batch is created on Oct-15, AccellosOne 3PL will look at all receipt, renewal and accessorial invoices created between Oct-01 and Oct-15 when determining whether a monthly minimum invoice is required.
You set up monthly minimum billing in DBIP by entering a charge code in the Total Invoices Minimum Charge 
Code field.

DBIP screen showing monthly minimum billing
Monthly minimum billing requires a separate batch and invoice using the batch type “Minimum Total Invoices” 
in BILB (Billing Batch). This batch type should be run after the extra charge batch/invoice, accessorial batch/ invoice and renewal batch/invoice.

### Working With Charge Groups <a id="working-with-charge-groups"></a>

Charge groups allow you to group two or more charge codes in a single charge group and calculate a minimum/maximum value based on the sum of all charges in the charge group. It is designed to provide a substitute in a single, easy-to-maintain program for the various minimum/maximum charges scattered throughout DILP, DBIP and IBIP. 
If the minimum/maximum applies to two or more charge codes, the Detail Block must be populated with those charge codes. If, on the other hand, the minimum/maximum applies to a single charge group type, the Detail 
Block will be left empty. 
FIELD DESCRIPTIONS
Charge Group Code Mandatory
Your charge group code.

Description Mandatory
Your description for the charge group code.
Minimum / Maximum 
Charge Code
Mandatory
Your maximum/minimum charge for the charge group.
Charge Group Type Document Line This charge group type is used to create receipt or order charges with the minimum /maximum applied to all charges attached to each line of a receipt/order.
Document This charge group type is used to create receipt or order charges with the minimum/maximum applied to all the charges attached to an entire receipt or order.
Billing Entity This charge group type can be applied at the document, batch or invoice level. It will group the charges for the same billing entity and apply the minimum/maximum to that amount.
Invoice This charge group type applies the minimum/maximum to an entire invoice.
NOTE There are four charge group types, each of which is calculated independently. That means you can set up one minimum for each of the four types for a total of four minimums applied.
Charge Code If you enter two or more charge codes in this field, the maximum/minimum charge will apply to the sum of all charges in the charge group.
FIELD DESCRIPTIONS

CHGR screen showing charge group for Document Line

### Changing Your Rates <a id="changing-your-rates"></a>

You change your rates for a particular charge code in the program RATE (Depositor Billing Rates). You change a rate in this program by keying in a new effective date over the old effective date and then entering your new rates. AccellosOne 3PL will create a new record in RATE; the new record will be identical to old record — that is, the same charge code, customer code, charge type code, etc. — except for the effective date. The old rate remains in RATE under the old effective date. That means that you always have a complete listing of the current rate plus all previous and future rates.
You can change a rate in RATE effective immediately by entering the current date as your effective date or you can change a rate effective in the future by entering a future date as your effective date. 
TYPE OF CHARGE RATE CHANGE TAKES EFFECT receipt The rate change takes effect for any new product received from that point on (if you enter the current date as your effective date) or on or after the new effective date (if you enter a future date as your effective date).
accessorial The rate change takes effect for any new accessorial charges entered from that point on (if you enter the current date as your effective date) or on or after the new effective date (if you enter a future date as your effective date).

### ENTERING A RATE CHANGE <a id="entering-a-rate-change"></a>

1 Enter RATE.
2 Click on Enter Criteria
3 If you wish to query by customer code, key in your customer code and press Enter. If you do not wish to query by customer code, press Enter to bypass this field.
4 Key in your charge code and click on Execute Query. The system will display the current RATE record for the charge.

Depositor Billing Rates (RATE)
renewal The rate change takes effect for any new product charged for renewal from that point on (if you enter the current date as your effective date) or on or after the new effective date (if you enter a future date as your effective date).
For existing inventory, the rate change may or may not apply to existing inventory depending on the option that you selected in the Original or Current Rate on Renewals field in DBIP. 
C for Current The new rates will be applied to existing inventory as well; that is, the next time renewal charges are calculated for an item or lot of existing inventory, the system will use the current rate — not the original rate.
I for Initial Original or R for Renewal 
Original
The rates set up in IISP or IRSP when the product was received will apply to renewal storage charges for existing inventory.
TYPE OF CHARGE RATE CHANGE TAKES EFFECT

5 Key in your new effective date over the old effective date and press Enter. AccellosOne 3PL will create a new record in RATE; the new record will be identical to old record except for the effective date.
6 When you finish changing your rates, click on Return to Main and Exit to exit.

### CANCELLING A RATE CHANGE <a id="cancelling-a-rate-change"></a>

If the effective date of the rate change is in the future, you cancel a rate change by deleting the appropriate record in RATE.
1 Enter RATE.
2 Use your query commands to locate the RATE record containing the rates that you wish to cancel.
3 Press Enter until your cursor is positioned in the Minimum Charge field.
4 Click on Delete Record.
5 Click on Return to Main and Exit to exit.

### CHANGING YOUR RATES BY A FIXED PERCENTAGE IN IDRA <a id="changing-your-rates-by-a-fixed-percentage-in-idra"></a>

If you wish to change one or more of your rates by a fixed percentage, you use the program IDRA (Increase/
Decrease Rates). IDRA allows you to increase or decrease your rates as of an effective date that you specify. 
The effective date in IDRA must be a date in the future; that is, the current date plus one. When you run IDRA, 
If the charge that you are changing is a flat rate charge:
If the charge has breaks (that is, not a flat rate):
a) Press Enter until your cursor is positioned in the Flat Rate field.
b) In the Flat Rate field, key in your new flat rate and press Enter.
a) Press Enter until your cursor is positioned in the Number of 
Breaks field.
b) In the Number of Breaks field, key in your new number of breaks and press Enter. If the number of breaks is the same, key in the old number of breaks and press Enter.
c) In the Minimum Charge field, key in your minimum charge and press Enter. If there is no minimum charge, key in 0.
d) In the Maximum Charge field, key in your maximum charge and press Enter. If there is no maximum charge, key in 
999999999.99.
e) When the Detail Block is displayed, key in your quantity break and charge amount for each break. Press Enter after entering each value.
f) Click on Master Block to exit the 
Detail Block.

the system creates a second record in RATE for each charge code that you specify in IDRA. The second record has the same customer code and charge code as the first record but a different effective date and different rates.
IDRA applies to your break charges only; that is, the rates in the Detail Block of RATE. It does not apply to flat rate and maximum/minimum charges. If you wish to change flat rate and maximum/minimum charges, you must do so manually in RATE. If a charge code has both break and flat rate/maximum-minimum charges, 
IDRA will change the break charges but leave the other charges unchanged.
You can restrict rate increases and decreases by customer code and charge code or you can enter no restrictions in IDRA and change rates for all charge codes attached to the customer that you specify. 
1 Enter IDRA.

Increase/Decrease Rates (IDRA)
2 Key in your customer code and press Enter.
3 Key in your charge code and press Enter or press Enter with this field blank to change rates for all charge codes.
4 Key in your effective date and press Enter. The effective date must be in the future; that is, the current date plus one.
5 Key in your percentage change and press Enter. To enter a rate increase, you enter a positive number (for example, 5.7). To enter a rate decrease, you enter a negative number (for example, -10).
NOTE If you specify .ALL as your customer code, IDRA will change all rates attached to the customer code .ALL. It will not, however, change the rates of all customers. For example, if you have five charge codes attached to .ALL and three charge codes attached to ABCSUPP (ABC Supplies), a customer code of .ALL in 
IDRA will apply the rate change to your five .ALL charge codes but leave your three 
ABCSUPP charge codes unchanged.

6 Click on Process Change.

### CANCELLING AN IDRA RATE CHANGE <a id="cancelling-an-idra-rate-change"></a>

You cancel an IDRA rate change by deleting the appropriate record in RATE.
1 Enter RATE.
2 Use your query commands to locate the RATE record containing the rates that you wish to cancel.
3 Press Enter until your cursor is positioned on the Minimum Charge field.
4 Click on Delete.
5 Click on Return to Main and Exit to exit.

### Working With Renewal Storage <a id="working-with-renewal-storage"></a>

Renewal storage is any recurring storage charge that is charged after initial storage. Renewal storage is normally charged for as long as the product is in the warehouse.

### MAXIMUM DAILY BILLING <a id="maximum-daily-billing"></a>

In maximum daily billing, renewal storage charges are based on the highest daily quantity during the billing period just past. Maximum daily billing supports both single break and multi-break charges.
EXAMPLE USING FIRST OF MONTH BILLING
In this type of billing, the initial storage charge is zero. On the first of the month, your highest daily balance for the previous month is 1,000 cases and you charge on that amount. In the second renewal period, you receive an additional 300 cases on the 5th for a total quantity of 1,300 (1,000 + 300). On the 10th, you ship out 100 cases for a total quantity of 1,200 (1,000 + 300 -100). On the first of the following month, your new highest daily balance for the previous period is 1,300 cases and you charge renewal storage on this amount.
PERIOD 1
Inbounds: 1,000 cases received on 18th
Maximum: 1,000 cases
PERIOD 2
Initial maximum: 1000 cases
Inbounds: 300 cases received on 5th 
Outbounds: 100 cases shipped on 10th 
Maximum: 1,300 cases
18 05 01 01
+1000 CS renewal storage renewal storage
+300 CS
-100 CS =1200 CS

### SETTING UP MAXIMUM DAILY BILLING <a id="setting-up-maximum-daily-billing"></a>

1 Create a charge code in CHAR with a charge type code of MAXD (Maximum Daily Single Break) or 
MAXX (Maximum Daily Multi-Break).
2 Attach your charge code to your renewal storage profile in IRSP.
3 Attach your renewal storage profile to IBIP.
4 Attach your item billing profile to your items in ITEM.
5 Set up your rates for the charge code in RATE.

### CHECK-IN ONLY BILLING <a id="check-in-only-billing"></a>

With check-in only billing, renewal charges are based on the opening balance plus inbounds during the billing period just past. The opening balance does not include outbound shipments from the previous period. In this type of billing, the initial storage charge is usually zero.
EXAMPLE USING FIRST OF MONTH BILLING
On the first of May, your opening balance for the previous month is 0 cases and you received 1,000 cases during the month. Your billing amount for period 1 is therefore 1,000. In the second renewal period, your opening balance for the previous period is 1,000 cases and during the month you receive 300 cases; your billing amount for this period is 1,300 (1,000 + 300) and does not include any outbound shipments. 
On July 1 you look back at your third renewal period; your opening balance is 1,200 (1,000 + 300 - 100) 
cases. Since you have no inbounds in period 3, your billing amount (1,200) is the same as your opening balance.

### SETTING UP CHECK-IN ONLY BILLING <a id="setting-up-check-in-only-billing"></a>

1 Create a charge code in CHAR with a charge type code of either CIO (Check-In Only) for single break charges or MXCX (Max. Daily CIO - Multi-Break) for multi-break charges.
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
Opening balance: 1,200 cases (1,000 + 300 - 100)
Outbounds: 400 cases
Billing Amount: 1,200 cases
18 10 JUNE 01 JULY 01 
+1000 CS -100 CS
$ renewal storage renewal storage
-400 CS
=1000 CS = 800 CS
MAY 01 05
+300 CS =1200 CS
$ $ renewal storage

4 Attach your item billing profile to your items in ITEM.
5 Set up your rates for the charge code in RATE.

### DAILY AVERAGE BILLING <a id="daily-average-billing"></a>

With daily average billing, AccellosOne 3PL calculates a daily inventory balance for an item or group of items. 
When you generate your renewal or accessorial batch, the system adds up all the daily balances and then divides the total by the number of days on which there was inventory in the warehouse for the item or items.
Daily average billing is only available for unit-based SKU’s; you cannot use daily average billing if you bill by weight or cube.
EXAMPLE 
Suppose Customer A has the following balances:
If you run a batch on August 7, the system will calculate the daily average as follows:
11 + 15 + 5 + 3 + 8 (for Item A) + 3 + 5 + 5 + 4 +3 (for item B)/ 5 = 12.4 (or 13 pallets with rounding)
You divide the total by 5 rather than by 7 because there was no inventory on August 6 and 7.

### SETTING UP DAILY AVERAGE BILLING <a id="setting-up-daily-average-billing"></a>

1 Enter DBIP and retrieve the billing profile for the customer that you want to set up for daily average billing.
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
If daily average billing applies to all of a customer’s items:
If daily average billing applies to a single item or group of items:
a) Enter the code CDAV in the 
Renewal Summarization Code field.
a) Enter the code ISUM in the 
Renewal Summarization Code field.

DBIP screen showing Renewal Summarization Code field set to CDAV
3 Exit DBIP and enter CHAR.
4 Create one or more charge codes with a charge type of either DAVS (Daily Average Single Break) or 
DAVM (Daily Average Multi-Break). Make sure that the charge on and qualify on SKU is a unit-based 
SKU.

CHAR screen showing a charge type of DAVS (Daily Average Single Break)

5 Exit CHAR and enter IRSP.
6 Create a renewal storage profile with a single record in the Frequency Block. Set the Frequency Code to 
D for Daily and set the Cycle field to 1. 
7 In the Location Bill Block, attach the charge code or codes that you created in the previous step to the appropriate location billing codes. These charge codes must have a charge type of either DAVS or 
DAVM.

IRSP screen showing a frequency code of D for Daily, a cycle of 1 and a charge code whose charge type is set to DAVS or DAVM
8 Exit IRSP and enter IBIP. Attach your IRSP profile to your item billing profile.

IBIP screen showing DAVG as the renewal storage profile code
9 Do one of the following:
If you entered CDAV as your renewal summarization code in 
DBIP:
If you entered ISUM as your renewal summarization code in 
DBIP:
a) Leave the Renewal Summarization Code field blank since the option that you selected in DBIP applies to all of the customer’s items. 
a) Enter the code CDAV in the 
Renewal Summarization Code field.

IBIP screen showing CDAV as your renewal summarization code
10 Exit IBIP and enter ITEM. Attach your new IBIP profile to all items requiring daily average billing.

### EXCEED DAILY AVERAGE BILLING <a id="exceed-daily-average-billing"></a>

You can define a fixed number of pallet/case spaces that are “reserved” for a given customer and generate a charge whenever this number is exceeded. The charge is based on the daily average of the “over” quantity.
For example, suppose the reserved space or base quantity for a customer is 500 pallets. 
Calculation: 625/5 = 125 x rate (day 2 with zero quantity over is not counted)
DAY INVENTORY QUANTITY OVER
1 550 50
2 500 0
3 560 60
4 555 55
5 560 60
6 900 400

You set up exceed daily average billing in DBIP by entering EDAV (Exceed Daily Average) in the Renewal 
Summarization Code field. In the Reserved Quantity field, you enter your reserved quantity in your renewal storage charge on SKU. For example, if your charge on SKU for renewal storage in CHAR is cases and you enter 500 in the Reserved Quantity field, your reserved quantity will be 500 cases.
DBIP screen showing a reserved quantity of 500
Setup
1 In CHAR charge code type = DAVM or DAVS.
2 In DBIP renewal summarization code = EDAV (if exceed daily average billing applies to all of the customer’s items) or ISUM (if exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if exceed daily average billing applies to all of the customer’s items) or EDAV (if exceed daily average billing applies to a single item or group of items).

### TOTAL EXCEED DAILY AVERAGE BILLING <a id="total-exceed-daily-average-billing"></a>

You can define a fixed number of pallet/case spaces that are “reserved” for a given customer and generate a charge for the sum of exceeded quantities.
For example, suppose the reserved space or base quantity for a customer is 500 pallets. 
DAY INVENTORY QUANTITY OVER
1 550 50
2 500 0
3 560 60
4 555 55
5 560 60

Calculation: 625 x rate
You set up total exceed daily average billing in DBIP by entering EDTO (Total Exceed Daily) in the Renewal 
Summarization Code field. In the Reserved Quantity field, you enter your reserved quantity in your renewal storage charge on SKU. For example, if your charge on SKU for renewal storage in CHAR is cases and you enter 500 in the Reserved Quantity field, your reserved quantity will be 500 cases.
DBIP screen showing a reserved quantity of 500
Setup
1 In CHAR charge code type = DAVM or DAVS.
2 In DBIP renewal summarization code = EDTO (if total exceed daily average billing applies to all of the customer’s items) or ISUM (if total exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if total exceed daily average billing applies to all of the customer’s items) or EDTO (if total exceed daily average billing applies to a single item or group of items).

### DAILY AVERAGE BILLING BASED ON NUMBER OF PALLET POSITIONS <a id="daily-average-billing-based-on-number-of-pallet-positions"></a>

If you store pallets in bulk locations, you can have the system charge for the number of pallet positions versus the physical number of pallets in a location. 
For example, suppose you have a bulk location that can stack four pallets high, but you have three physical pallets in that location. With Customer Daily Maximum billing, the system will charge for four pallets instead of three. The reasoning is that because the space is unusable, you want to re-coup your costs for the entire bulk space versus what is actually being used.
This billing option is designed for product that is crushable, which limits the stacking height.
Setup
1 In CHAR charge code type = DAVM or DAVS.
6 900 400
DAY INVENTORY QUANTITY OVER

2 In DBIP renewal summarization code = CDMX (if daily average billing applies to all of the customer’s items) or ISUM (if total exceed daily average billing applies to a single item or group of items).
3 In IBIP renewal summarization code = blank (if daily average billing applies to all of the customer’s items) 
or CDMX (if total exceed daily average billing applies to a single item or group of items).

### SINGLE LEVEL BILLING <a id="single-level-billing"></a>

Single level billing allows you to generate a single charge for mixed product received on the same pallet. For example, suppose you bill at inventory level 2 or higher and you receive two different lots on the same pallet. 
AccellosOne 3PL would generate a single charge for the whole pallet. 
You set up single level billing by setting the Single Level Billing flag in DBIP to Y for Yes for the appropriate customers. 

### MONTHLY RENEWAL INVOICING <a id="monthly-renewal-invoicing"></a>

With monthly renewal invoicing, you can generate renewal invoices for each billing entity based on a predetermined scheduled such as every 30 days or every seven days. For example, suppose you charge renewal storage daily and have the following inventory in your warehouse:
 billing entity A received on July 1
 billing entity B received on July 15
If monthly renewal invoicing is deactivated and you generate a renewal batch on August 5, it would have an invoice date of August 5 and would contain the renewal storage charges from July 1 to August 5 for billing entity A as well as the renewal storage charges from July 15 to August 5 for billing entity B. 
With month renewal invoicing, a renewal storage batch generated on August 5 would contain only charges for billing entity A up to July 31. Charges for billing entity A incurred after July 31 could only invoiced the following month. And charges for billing entity B could only be invoiced on August 15 or later.
You activate monthly renewal storage invoicing by entering appropriate values in the following two fields in 
DBIP.
NOTE Monthly renewal invoicing is only available for IND and UREN invoicing.
FIELD DESCRIPTIONS
Number of Days Between 
Renewal Invoices
You activate monthly renewal storage invoicing by entering a value greater than zero (say, 30) in this field.
Create Renewal Invoice at Zero Inventory
Only available if Number of Days Between Renewal Invoices > 0
If you set this flag to Y for Yes, the billing entity will have its next renewal invoice date reset to the date that the inventory is zero out. If you set this field to N for No or leave it blank, the next renewal invoice date will not be reset.

DBIP screen showing monthly renewal invoicing activated
In DBIP you establish your customer-level defaults. You can override your customer-level defaults for individual items by entering different values in IBIP.

### RENEWAL INVOICING BY RECEIPT <a id="renewal-invoicing-by-receipt"></a>

With renewal invoicing by receipt, you can generate one renewal invoice for each receipt. For example, suppose you charge renewal storage daily and you receive and confirm five receipts on September 1. If you generate a renewal storage batch on September 2, AccellosOne 3PL will generate five different invoices; one for each receipt. If renewal invoicing by receipt is deactivated, AccellosOne 3PL would generate a single renewal invoice for all five receipts on September 2. 
You activate renewal invoicing by receipt by setting the Renewal Invoice by Receipt flag in DBIP to Y for Yes. 
Renewal invoicing by receipt is only available for IND and UREN invoicing.

DBIP screen showing renewal invoicing by receipt activated

### RENEWAL INVOICING BY OPID <a id="renewal-invoicing-by-opid"></a>

You can calculate renewal storage charges by outbound pallet ID rather than unique billing entity. That is, the renewal calculation will be based on the entire unshipped outbound pallet associated with the OPID and will not consider individual inventory entities.
An OPID can be composed of different billing entities. For example, item A, Lot 123, PID A-123 can be shipped out together with item B, Lot 123, PID B-123 in one OPID, say 0001. The renewal calculation will treat each unique OPID as a different billing entity and apply the correct renewal charge. Each OPID is considered as one pallet to bill.
In LODE, you set the Renewal Calc. by OPID flag to Yes for the appropriate location bill code(s). Depending on your requirements, renewal storage by OPID can be activated for some location bill codes, all location bill codes or none. 
LODE screen showing Renewal Calc. by OPID flag set to Yes
In DBIP, you set the Renewal Calculation by OPID flag to Yes.

DBIP screen showing Renewal Calculation by OPID flag set to Yes 

### LOOKING UP RENEWAL STORAGE INFORMATION <a id="looking-up-renewal-storage-information"></a>

You look up renewal storage information in the Renewal Block of LOEN. The Renewal Block shows the period number, next renewal date, last renewal date, number of units, gross/net weight of the item and the number of conveyances (if applicable). 
The period number refers to the product’s current renewal period. For example, if the period number is 3, that means that the product has been renewed twice and is currently in its third renewal period. If the period number is -1 and the next renewal date is 01.01.01, this means that the receipt was never rated. Use RCRA (Receipt Rater) or CHRF to rate the receipt.
1 Enter LOEN.
2 Key in your customer code and press Enter.
3 Key in your item code and level 2, 3 and 4 values (if any) and press Enter.
4 When the inventory entity whose renewal information you wish to look up is displayed, click on Location 
Block.
5 Click on Renewal Block.
NOTE Unlike the Location Block, the Renewal Block is not updated in real time and may show out-of-date information. For example, you have generated and confirmed a renewal batch but the next and last renewal dates remain unchanged or you shipped out one pallet a week ago and your current balance is three yet the Renewal Block shows a quantity of four pallets. 
In the majority of cases, you can update the information in the Renewal Block by running RENW. See the section [Running the Renewal Preprocessor (RENW) On 
Demand](faturamento-setup.html#running-the-renewal-preprocessor-renw-on-demand) for complete instructions.

Renewal Block in LOEN showing renewal period 7
In the sample screen shown above, the product is in its eighth renewal period. It last renewed on 
08.11.07 and will be renewed for the eighth time on 09.08.07.
6 When you finish viewing the renewal information, click on Drill Block and Inventory. Then click on Exit to exit.

### RUNNING THE RENEWAL PREPROCESSOR (RENW) ON DEMAND <a id="running-the-renewal-preprocessor-renw-on-demand"></a>

The renewal preprocessor (RENW) is a special program that updates the billing history of your inventory; any transaction that you enter in ENOR (orders and transfers), RELO and ENAJ potentially affects the billing history of an item.
The purpose of the renewal preprocessor is to shorten the processing time of a renewal batch by catching and correcting as many billing errors as possible before running your renewal batch. If you do not run RENW, the program will run “in the background” when you run BILB.
The frequency with which you should run RENW will depend on a number of factors including your billing frequency and the volume of transactions in your warehouse. You can run the program daily, weekly, at the end of each month or whenever required. Each time that you run it, RENW will update the billing history of all items that have had activity in ENOR (orders and transfers), RELO or ENAJ since the last time that you ran 
RENW. 
1 Key in RENW and press Enter. There is no screen or input parameters for this program and you cannot specify a customer.
NOTE RENW can be set up as a cron job in Unix to run automatically every night, every week or any other frequency that you require. If you set up RENW as a cron job, there is no need to run RENW on demand.

### Changing Renewal Storage Rates <a id="changing-renewal-storage-rates"></a>

When you change your renewal storage rates in IRSP, the new rates automatically apply to new inventory renewed after the change was entered. They may or may not apply to existing inventory depending on the option that you choose in DBIP (Depositor Billing Profile).
You can override your original vs. current rate on renewals logic at the customer level by setting the Original / 
Current Rate on Renewals flag in IBIP (Item Billing Profile) to the appropriate value. If the item-level value differs from the customer-level value, the item-level value will be used.

### CHANGING RENEWAL ORIGINAL RATES FOR EXISTING INVENTORY IN ADBD <a id="changing-renewal-original-rates-for-existing-inventory-in-adbd"></a>

If you wish to change the renewal original rates for existing inventory (for example, when the product was received the renewal rate was $2.00 per case but should have been $1.50 per case), you must use the program ADBD (Adjust Billing Data).
When entering your changes in ADBD, the number of inventory levels that you must enter depend upon the inventory level that you bill at in DILP. For example, if you have two levels of inventory — item and lot — and you bill at the item level, you enter your changes in ADBD once for that item. If, on the other hand, you bill at the lot level and you have 10 lots of item 1 in your warehouse, you must enter your changes in ADBD ten times — that is, once per lot. 
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
C for Current The new rates will be applied to existing inventory as well; that is, the next time renewal charges are calculated for an item or lot of existing inventory, the system will use the current rate — not the original rate.
R for Renewal Original The rates set up in IRSP when the product was received will apply to renewal storage charges for existing inventory. If you wish to change these rates for existing inventory, you must use the program ADBD (Adjust Billing Data).

Adjust Billing Data (ADBD) screen showing Billing Block
6 When you have reached your lowest level of inventory for billing purposes, click on Billing Block.
7 Click on Detail Block.

Adjust Billing Data (ADBD) screen showing Billing Detail Block
8 Key in your new rate and press Enter. For example, if your new rate is $2 per pallet, you would enter 2 in this field.
The new rate will take effect the next time that the product renews.
9 Press Enter to accept the system-calculated qualifier quantity displayed in the appropriate field (Qualifier 
Quantity, Qualifier Weight, Qualifier Net Weight or Qualifier Cube). 
10 When you finish making your changes, click on Process Adjustments.

11 When the Remark Block is displayed, key in 1 as your line number and press Enter. Then enter your remarks and press Enter again. When you finish entering your remarks, click on Return to Main and 
Return to exit.
12 Repeat the above steps for each inventory entity that you wish to change. 
13 When you finish changing your rates, click on Exit to exit.

### ADJUSTING BILLING DATA IN ADBD <a id="adjusting-billing-data-in-adbd"></a>

In ADBD, you can also make changes to the following renewal storage parameters for existing inventory:
 the next renewal date (only required if you are changing your billing frequency; for example, from anniversary monthly to monthly first of month)
 the base renewal date
 the item billing profile code set up in IBIP (for example, you attached the wrong IBIP code to an item and you wish to correct the error so that renewal storage will be properly calculated)
The base renewal date is the date that the product was originally received. If you have changed your renewal billing frequency from a fixed date renewal (weekly as of Monday, monthly first of the month, monthly last of the month) to an anniversary renewal (anniversary monthly, anniversary weekly, daily), you may have to adjust this date to make sure that the base renewal date matches the next renewal date.
EXAMPLE — Switch from monthly first of month to anniversary monthly on 06.10.09 (June 10, 2009)
Next Renewal Date = 06.10.09
Last Renewal Date = 05.01.09
Base Renewal Date = 01.25.09
In the above example, you must change your base renewal date from 01.25.09 (the date that the product was originally received) to 06.10.09 so that the next renewal date and the base renewal date match.
When entering your changes in ADBD, the number of inventory levels that you must enter depends upon the inventory level that you bill at in DILP. For example, if you have two levels of inventory — item and lot — and you bill at the item level, you enter your changes in ADBD once for that item. If, on the other hand, you bill at the lot level and you have 10 lots of item 1 in your warehouse, you must enter your changes in ADBD ten times — that is, once per lot.
1 Enter ADBD.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter. If your customer has a single inventory level, click on Execute 
Query instead of Enter after entering your item code.
4 If your customer has multiple inventory levels, key in your lot number, production date, etc. and click on 
Execute Query.

Adjust Billing Data (ADBD) screen showing Billing Block
5 When you have reached your lowest level of inventory, click on Billing Block.
6 Proceed to make any required changes to the following fields:
 Next Renewal Date
 Base Renewal Date (requires running RENW)
 Billing Profile Code
7 When you finish making your changes, click on Process Adjustments.
8 When the Remark Block is displayed, key in your remarks. When you finish entering your remarks, click on Return to exit.
9 Repeat the above steps for each inventory entity that you wish to change. 
10 When you finish all your changes, click on Exit to exit.
11 If you changed the base renewal date in step 6, you must run the renewal preprocessor in RENW.

## Billing Setup — Advanced Topics <a id="billing-setup-advanced-topics"></a>

*Manual A — Billing and Invoicing*

### Combination Type Charges <a id="combination-type-charges"></a>

A combination type charge consists of a flat rate charge together with a linear per unit charge. For example, for unloading a non-palletized trailer, you charge a flat rate of $75 plus 10 cents a case. Combination type charges can be defined as either single break or multi-break type charges. Consider the following examples:
Example 1
Charge Type = Single break
Charge Definition = Combination
RATE is set up with one flat rate break and one linear break for a total number of two breaks.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total of $51.00.
Example 2
Charge Type = Multi-break
Charge Definition = Combination
Rates are the same as those in example 1.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total of $101.00.
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

An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total of $150 and 101 cases will have a charge total of $101.
Example 4
Charge Type = Multi-break
Charge Definition = Combination
Rates are the same as those in example 3.
An amount of less than or equal to 50 cases will have a charge total of $100. 51 cases will have a charge total of $250 (100 + 150). 101 cases will have a charge total of $251 (100 for the first 50 cases, 150 for the next 50 cases and 1 for the last case).

### SETTING UP COMBINATION TYPE CHARGES <a id="setting-up-combination-type-charges"></a>

Combination type charge require a charge type of Single or Multi and a Charge Definition of C for Combination.
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

### Third Party Billing <a id="third-party-billing"></a>

Third party billing occurs when storage costs are paid by a third party — that is, by someone other than the owner of the goods. There are four ways of performing third party billing in AccellosOne 3PL:
 you can perform third party billing of initial storage and handling charges on a receipt-by-receipt basis
 you can create an accessorial charge and bill this charge to any customer on your system
 you can set up an invoice only customer so that all invoicing is automatically directed to the third party
 you can set up billing subscription in BTCS

### THIRD PARTY BILLING ON A RECEIPT-BY-RECEIPT BASIS <a id="third-party-billing-on-a-receipt-by-receipt-basis"></a>

By changing the default value in the Bill to Code field in ENRE, you can bill all initial storage and handling charges for that receipt to any other customer set up in AccellosOne 3PL.
1 Enter ENRE.
2 In the Customer Code field, key in the customer whose product you are receiving and press Enter.
3 In the Shipper Code field, key in your shipper code and press Enter.
In the Bill To Code field, the system will display the customer that you entered in step 2. 
4 Key in the customer you wish to bill for the receipt and press Enter or use your pick list (press F10 to enter the pick list, F2 to display the customer codes and F3 to select) to select the appropriate customer code.
5 Continue to enter your receipt in the normal manner. All charges will be billed to the customer that you specified in the Bill To Code field.

### CREATING AN ACCESSORIAL CHARGE <a id="creating-an-accessorial-charge"></a>

By changing the default value in the Bill to Code field in ENAC, you can bill an accessorial charge to any customer on your system. These charges can be either attached to a particular order or receipt or entered directly in ENAC. 

### SETTING UP AN INVOICE ONLY CUSTOMER <a id="setting-up-an-invoice-only-customer"></a>

An invoice only customer is a customer with no inventory. Typical examples of invoice only customers are carriers, shippers, consignees or any other party that you wish to invoice.
1 Set up one billing profile code in DBIP with the Send Invoice To flag set to P for Paying Office. You will use this profile for the customer with inventory in your warehouse whose storage charges will be paid by a third party.
NOTE Invoice only customers do not have their own rates. The rates used to generate the invoice only customer’s invoices are those of the inventory customer.

2 Set up a second billing profile in DBIP with the Send Invoice To flag set to C for Customer. You will use this profile for the customer with no inventory who will pay the storage charges for the other customer’s product.
3 Set up two customer profiles in CUST as follows:

### BILLING SUBSCRIPTION <a id="billing-subscription"></a>

Billing subscription allows you to perform 3PL/4PL billing in which you are outsourcing to other 3PL providers or you are performing warehouse services that are to be invoiced to parties other than the customer such as the consignee.
For example, suppose because of space limitations you have sub-contracted some of your warehousing to another 3PL provider. You would need to establish billing rules and rates for the customer whose inventory is being handled by another 3PL provider (normal billing) and you would also need to establish billing rules and rates for the 3PL provider that you have sub-contacted out to.
With billing subscription, the system generates two invoices: one for your customer (normal billing) and one for the 3PL operator you have sub-contracted out to. The first “invoice” is not actually a real invoice that you pay on receipt, but rather a statement of what you will pay the other 3PL provider or what they should be charging you.
You maintain third party billing rules in BTCS (Bill to Customer Subscription). BTCS allows you to link a virtual customer to a customer owning inventory with the same or different set of billing rules and rates.
In the Header Block, you define your billing subscription defaults: the actual customer who owns the inventory (Customer Code), the 3PL operator that you have contracted out to (Bill To Customer Code) and the default item billing profile used by the 3PL operator to bill for these services. 
CUSTOMER A (CUSTA) CUSTOMER B (CUSTB)
The inventory is in this customer’s name but all billing is sent to a third party (customer B)
This customer has no inventory but pays the bills for customer A’s inventory 
 Account Type = W for Warehouse
 Billing Profile Code = code that you set up in step 1 with Send Invoice To flag set to P
 Paying Office Code = CUSTB
 Account Type = I for Invoice Only
 Billing Profile Code = code that you set up in step 2 with Send Invoice To flag set to C for Customer
FIELD DESCRIPTIONS (HEADER)
Customer Code Mandatory
The actual customer who owns the inventory.

In the Detail Block, you define any overrides to the values in the Header Block. For example, for a particular item billing code used by the inventory customer, use a particular item billing code that is not defined in the 
Header Block. If there no overrides, you leave the Detail Block blank.
Bill To Customer Code Mandatory
The 3PL operator that you have contracted out to.
NOTE The bill to customer must be set up in CUST as either a regular or invoice only type customer.
Item Billing Profile Code (IBIP)
Mandatory
The default item billing profile used by the 3PL operator to bill for these services. 
Bill Event Type Receipt Rater Only receipt charges would apply to the Bill To Customer. It means once a receipt is rated for the customer, another set of receipt charges based on the Item Billing Profile will be created under the Bill to Customer 
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

BTCS screen

### Alternate Billing Groups <a id="alternate-billing-groups"></a>

Alternate billing groups allow you to group items for billing purposes; for example, all items belonging to the same product line can be treated as a single entity for billing purposes.
If you use alternate billing, you must apply it to all of a customer’s items. The same customer can have multiple alternate billing groups — for example, one group for baked goods, another group for candy and a third group for ice cream — but all items must be set up for alternate group billing and attached to a group.
Alternate billing applies to renewal storage only and overrides any renewal storage options that you set up in 
DILP. Alternate billing is not available for initial storage, handling or accessorial charges.
1 Set up a charge code for renewal storage in CHAR and RATE.
2 Set up your renewal storage profile in IRSP.
3 Set up your item billing profile in IBIP.
4 Create a single level or double level code in ITAS. If you do not know how to set up item alternate sort codes in ITAS, refer to the Setup Guide for complete instructions.

Item Alternate Sorts screen showing code for MEAT
5 Attach the IBIP profile that you created in step 3 to the appropriate alternate inventory reporting code in 
ITAS. 
6 Set up your depositor billing profile in DBIP and attach the ITAS code that you created in the previous step to this profile. You enter your ITAS code in the Alternate Billing Group Code field in DBIP.
7 Set up your customer and attach the DBIP profile that you created in the previous step to this customer.
8 Set up your items and attach your item billing code created in IBIP to these items. Then attach your ITAS code to the Alternate Reporting Block in ITEM for all items that are part of the alternate billing group.

### Load Type Charges <a id="load-type-charges"></a>

Load type charges are handling charges that apply to a particular load type. You specify your load type for inbound charges when receiving product in ENRE and you specify your load type for outbound charges when shipping product in ENOR. 
For inbound load type charges, AccellosOne 3PL will generate one charge for each receipt line. For outbound load type charges, AccellosOne 3PL will generate one charge for each order. 
To set up load type charges, first you define your load type in LOAD (Load Types). Then you attach the appropriate charge code to the load type in DELO (Depositor Load Type Charges). The charge code for a load type charge must be assigned a charge on and qualify on SKU that is based on net or gross weight, cube or number of units.

Load Type screen showing PLT for palletized load

Depositor Load Type Charges screen showing charge code of PLT1 attached to the load type code of 
PLT
If you use IND or UREN invoicing, inbound load type charges print on the warehouse receipt invoice. In all other cases, load type charges print on the accessorial invoice.

### Open Lot Receipts <a id="open-lot-receipts"></a>

Open lots are lots that remain open for one or more days and allow you to receive the same entity in multiple receipts. For example, if item A is defined as an open lot for three days, you can receive the following:
With open lots, the customer will be charged initial storage once for a receipt of 65,000 lbs. instead of three times for receipts of 10,000, 25,000 and 30,000 lbs. You use open lots when you wish to offer your customers a discount on large volumes of inventory.
Open “lots” need not be defined as actual lots in DILP. They can be any inventory terminology code set up in 
INTE — for example, date code, trailer number, etc. — provided that the following conditions are met:
 your open lot must be defined as inventory level 2 or higher
 you must bill at that inventory level (for example, if your open lot is defined as inventory level 3, you must bill at that level)
 all inventory levels must be the same for product to be received on the same open lot
If you produce a warehouse receipt invoice, handling charges for an open lot will appear on each warehouse receipt invoice. Initial storage, on the other hand, will always print on the accessorial invoice.

### SETTING UP OPEN LOTS IN ITEM <a id="setting-up-open-lots-in-item"></a>

You set up open lots by entering the appropriate number of days in the Number of Days for Open Lots field in 
ITEM. The number entered in this field determines for how many days this entity (the item with these specific inventory levels) can be received as an open lot.
If you enter 99 as your number of days, the number of days is set by the operator in ENRE when receiving the open lot and not in ITEM. That is, the Close Date in the Line Block of ENRE for the open lot will appear as 
DD.MM.YY or MM.DD.YY depending on your date format and must be manually entered by the operator.
1 Enter ITEM.
2 Retrieve the item that you wish to set up for open lots.
3 Press Enter until your cursor is positioned in the Number of Days for Open Lots field.
4 Key in the number of days that this item can remain open and press Enter.
June 16 item A/ lot 001 10,000
June 17 " 25,000
June 18 " 30,000
65,000

Item screen showing five as the number of days that a lot can remain open
5 Click on Return to Main and Exit to exit.

### ENTERING AN OPEN LOT IN ENRE <a id="entering-an-open-lot-in-enre"></a>

It is necessary to create a separate receipt each time that a shipment of this open lot arrives at the warehouse. 
1 Enter ENRE.
2 Complete the ENRE Header Block as a normal P (Post-receiving) type of receipt.
3 When you reach the Line Block, press F9 (Previous Field) until the cursor is in the Type field. Key in O for 
Open Lot and press Enter.

ENRE Line Block screen showing an open lot receipt type
4 Continue completing the Line Block until you reach the Close Date field. 
NOTE If you receive a Help Line Message “Inventory entity has been closed, cannot enter ’X’ or ’O’ lines,” this means that the number of days for open lots as defined in ITEM has expired. This item can no longer be received as part of an open lot.
Open lot type receipt line

ENRE Line Block screen showing an open lot receipt type
5 The system may automatically fill in the Close Date field according to the open entity number of days that was previously set up in ITEM. If the system-entered date is correct as the last day for receiving this entity as part of an open lot, press Enter.
If you need to override the system-entered date, key in the new date over the old one using the same date format. Then press Enter.
If DD.MM.YY appears in the Close Date field, key in the closing date using the same date format and then press Enter.
6 Complete the remaining Line Block fields in the usual manner.
7 Enter any remaining receipt lines. Then click on Return to Main to exit create mode and Master Block and Exit to exit.

### CLOSING AN OPEN LOT IN CLOL <a id="closing-an-open-lot-in-clol"></a>

When the close date arrives, you must run the program Close Open Lots (CLOL) to generate the charges.
1 Enter CLOL. No input is required in this program as AccellosOne 3PL closes the open lot automatically.
2 If you rate your receipts manually, enter RCRA (Receipt Rater) and proceed to rate the receipt.
The Close 
Date is the last day that this entity can be received as part of an open lot

### Overriding Generated Charges on a Receipt <a id="overriding-generated-charges-on-a-receipt"></a>

You can use the Receipt Type and Line Type fields in ENRE to override certain generated charges on a receipt. The following four options are available at both the header and line detail levels: 
 P for Post Receiving (default)
 N for No Charge
 H for Handling Only
 S for Initial Storage Only
However, certain options at the line detail level are not available if they conflict with options at the header level. For example, if you select H for Handling at the header level, your only options at the line detail level are 
Handling Only and No Charge; you cannot select Post Receiving because this would conflict with your selection at the header level.
Individual receipt lines on the same receipt can be assigned different options. For example, line 1 could be P (Post Receiving), line 2 could be N (No Charge) and lines 3 to 9 could be P. AccellosOne 3PL would generate normal initial storage and handling charges for lines 1 and 3 to 9 and no charges for line 2. 
RECEIPT 
LINE TYPE DESCRIPTION
P Post Receiving
All normal charges set up in IISP and IHAP for the item apply.
N No Charges
No charges will be generated for the receipt if you enter this option at the header level. No charges will be generated for the receipt line if you enter this option at the line detail level. This option is useful during implementations when you are adding inventory to a new system but do not wish to generate any receipt charges.
H Handling Only
Normal handling charges for the receipt will apply. However, no initial storage charges will be generated for the receipt if you enter this option at the header level and no initial storage charges will be generated for the receipt line if you enter this option at the line detail level.
S Initial Storage Only
Normal initial charges for the receipt will apply. However, no handling charges will be generated for the receipt if you enter this option at the header level and no handling charges will be generated for the receipt line if you enter this option at the line detail level.

### Seasonal or Special Billing <a id="seasonal-or-special-billing"></a>

You can attach multiple billing profiles to the same item in order to perform seasonal or special billing. For example, suppose you have an item that renews differently based on the demand for the product. You could set up two profiles: one that will renew weekly and one that will renew monthly. 
Each time that you receive a new billing entity in that product (for example, item 1, lot A), you will be prompted to select a billing profile. After selecting that profile (either weekly or monthly), you will not be prompted again for your billing profile code for the duration of the billing entity.
You can assign up to three item billing profile codes to an item.
1 Create the different types of profiles that you need in IBIP (Item Billing Information Profile). 
2 Attach the profile codes created in IBIP to the item in ITEM using your pick list.

Item A1 showing two billing profiles
3 When you receive that particular item and you are rating the receipt, AccellosOne 3PL will prompt you in 
CHRF or RCRA for which profile you wish to use. Select the appropriate profile for that receipt.
NOTE If you receive the same billing entity on a new receipt, you will not be prompted for a billing profile. AccellosOne 3PL will automatically use the billing profile that you selected when you first received the billing entity.

From then on the system will use the same profile for that item (that is, renewals and accessorial billing). 
The profile that you select will remain in effect throughout the duration of the billing entity.

### Taxes <a id="taxes"></a>

AccellosOne 3PL supports the following taxes: the GST (Goods and Services Tax), PST (Provincial Sales 
Tax) and HST (Harmonized Sales Tax). These taxes are defined as single break charge codes in CHAR (Charge Codes) and the tax rate is defined in RATE (Depositor Billing Rates).

Depositor Billing Rates screen showing rate for charge code HST
In DBIP you define the default tax for a given customer. In ITEM you define whether the default defined in 
DBIP applies to a particular item. For example, if you define the GST as the default tax code for customer A, you have two tax options for each of customer A’s items. You can tax them at the GST rate by assigning them the tax code of GST or you exempt them from taxes by assigning them the tax code of NONE.
If all of a customer’s items are taxable, you can use surcharges to calculate the tax. See the section [Surcharges](faturamento-setup.html#surcharges) for further information.
NOTE If you wish to change the renewal storage charged on an item during a billing entity (that is, after the item has been received), you would have to do so in Adjust 
Billing Data (ADBD). Refer to [Adjusting Billing Data in ADBD](faturamento-setup.html#adjusting-billing-data-in-adbd) for complete instructions.

### Billing by Multiple Units of a SKU <a id="billing-by-multiple-units-of-a-sku"></a>

AccellosOne 3PL allows you to track inventory in one SKU and bill by a multiple of that SKU. For example, suppose you want to track inventory by bags and bill by bags of four. In SKUS (Stock Keeping Units) you define a SKU called BGFR (Bags of Four). You set the Base SKU Code field to BAG (your inventory SKU) 
and set the Value field to 4 (the number of bags in a BGFR SKU). 
1 Enter SKUS and set the SKU Code, Value and Base SKU Code fields to the appropriate values.

SKUS screen showing SKU code for BGFR
2 Enter CHAR and set the charge on and qualify on SKU to BGFR (your billing SKU) instead of BAG (your inventory SKU). 

CHAR screen showing Charge on/Qualify on SKU Code fields set to BGFR
3 In the Quantity Breakdown Block of ITEM for the items that you wish to set up for billing by multiple units of a SKU, set the Whole/Prorate flag to P for Prorate.

### Discounts on Initial Storage and Handling Charges <a id="discounts-on-initial-storage-and-handling-charges"></a>

You can apply discounts to the initial storage and handling charges for a given item by setting up a discount profile code in DPRO. For example, if you define a charge percentage of 90 percent in DPRO, initial storage charges for the item defined in IISP and handling charges for the item defined in IHAP will by multiplied by .9 
— that is, a 10 percent discount — to arrive at the actual initial storage and handling charges for the item.
There are two ways of applying discounts. You can attach the discount profile code to a particular item in 
ITEM and the discount will be automatically applied whenever you receive that item. Alternatively, you can select the appropriate discount profile code when you confirm the receipt and the discount profile code that you select will be applied to all items on the receipt.
There are two steps to follow in setting up discounts on initial storage and handling:
 you set up your discount profile code(s) in DPRO
 you set the Item Discount Flag in ITEM to the appropriate value and, if required, attach your DPRO code to the item

### SETTING UP YOUR DISCOUNT PROFILE CODE IN DPRO <a id="setting-up-your-discount-profile-code-in-dpro"></a>

In DPRO you define the effective date and percentage for your discount. When you confirm your receipt, 
AccellosOne 3PL compares the confirmation date to the date in DPRO. If the confirmation date is greater 

than or equal to the date in DPRO, the percentage will be applied to initial storage and handling charges. If the confirmation date is less than the date in DPRO, no percentage will be applied to initial storage and handling charges.
You can set up multiple effective dates and percentages in DPRO. For example, your percentage for January 
1 could be 90, your percentage for March 1 could be 85 and your percentage for May 1 could be 80. When you confirm your receipt, AccellosOne 3PL will select the appropriate percentage.
1 Enter DPRO.
2 Click on Create Record.
3 Key in your discount profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 When the Percentage Block appears, key in your effective date and press Enter.
6 Key in your percentage for this effective date and press Enter.

Discount Profile Code screen showing Percentage Block with a charge percentage of 90
7 Repeat the above two steps for any additional dates and percentages that you required.
8 When you finish setting up your dates and percentages, click on Return to Main to exit create record mode.
9 Click on Master Block and Exit to exit DPRO.

### SETTING UP YOUR ITEM IN ITEM <a id="setting-up-your-item-in-item"></a>

In ITEM, you set the Item Discount Flag to the appropriate value and, if required, attach your DPRO code to the item.

10 Enter ITEM.
11 Retrieve the item that you wish to set up for discounting.
FIELD DESCRIPTIONS
Item Discount Flag A = Always
N = No
C = Choose
If you select A for Always, the discount profile code that you enter in the Discount Profile Code field will be automatically applied whenever you receive that item. If you select N for No, no item discounting will take place for the item.
If you select C for Choose, you will be prompted to select the appropriate discount profile code when you confirm the receipt and the discount profile code that you select will be applied to all items on the receipt. The choose option requires unique inventory entities. You cannot re-receive the same inventory entity; for example, if you receive item A, lot 001 on your first receipt, you cannot receive the same inventory entity on an other receipt and apply a discount profile code to it.
Discount Profile Code Only available if you specify A for Always in the Item Discount Flag field.
If you attach a DPRO profile to the item, the percentage specified in the Percent Block of DPRO will be applied to the initial storage charges for the item. 
For example, if you enter 10%, the default initial storage charges for the item defined in IISP will be multiplied by .1 to arrive at the actual initial storage charges for the item.

Item screen showing item A1 assigned discount profile code 1
12 In the Item Discount Flag field, key in A for Always or C for Choose and press Enter.
13 If you selected A for Always in the previous step, key in your discount profile code and press Enter or select it using the pick list.
14 Click on Return to Main to exit modify record mode. Then click on Exit to exit.
SELECTING YOUR DISCOUNT PROFILE CODE DURING RECEIPT 
CONFIRMATION
If your receipts are automatically rated, you select your discount profile code during receipt confirmation. If you manually rate your receipts in RCRA, you select your discount profile code in RCRA.
AccellosOne 3PL does not support multiple discount profiles applied to the same inventory entity. As a result of this restriction, if you re-receive the same inventory entity on two separate receipts, you will not be prompted to select a discount profile code; the discount profile code that you selected the first time will be applied to all subsequent receipts of the same inventory entity.
1 Do one of the following:
2 When the Discount Profile Code screen appears, click on Execute Query.
If your receipts are rated automatically:
If you manually rate your receipts in RCRA:
a) Enter CHRF.
b) Proceed to confirm your receipt in the normal manner.
a) Enter RCRA.
b) Proceed to rate your receipt in the normal manner.

RCRA screen showing pick list of discount profile codes
3 Position your cursor over the discount profile code that you wish to select.
4 Click on Select Code to select the code.

### Cross-Dock Billing <a id="cross-dock-billing"></a>

Cross-dock billing occurs when you enter a cross-dock receipt in ENRE. You use a cross dock receipt to record product that comes into the warehouse for a short period of time. Cross dock product will either be taken from the incoming transportation vehicle and be placed directly on the outgoing transportation vehicle or it will be placed on the cross dock area of the warehouse from which it will be shipped out within a few days. 
Because the product is at the warehouse for such a short time period, it will not be stored in a normal warehouse location. Special inbound handling and initial storage charges will apply. 
When you use cross-dock billing, you cannot re-receive the same inventory entity during the cross-dock period. For example, if your cross dock period is four days and you receive item A, lot 001 on day 1, you cannot receive the same inventory entity — that is, item A, lot 001 — on day 2, 3 or 4.

### SETTING UP CROSS-DOCK BILLING <a id="setting-up-cross-dock-billing"></a>

There are three setup programs for cross-dock billing:
 you set up your cross-dock profile in IXDP
 you set the Cross Dock flag to Yes in ITEM for each item that you wish to cross-dock
 you make sure that the Rate Receipt Automatically flag in DBIP is set to N for No

The cross dock profile defines the initial storage and handling charges for cross dock items, the number of days in the cross dock period, the type of storage charged if the product stays in the warehouse longer than the cross dock period and which date (receipt or cross dock) the system is to use for renewal storage.
FIELD DESCRIPTIONS
Cross Dock Profile Code Mandatory
Your cross-dock profile code. For example, STD for Standard.
Description Mandatory
Your cross-dock profile code description
Initial Storage Profile 
Code (IISP)
Mandatory
The initial storage profile for the items to which this profile is attached. This profile overrides the IISP profile in IBIP (Item Billing Profile).
Handling Profile Code (IHAP)
Mandatory
The handling storage profile for the items to which this profile is attached. This profile overrides the IHAP profile in IBIP (Item Billing Profile).
Number of Cross Dock 
Days
Mandatory
The number of days that the item will remain in cross-dock.
Type of Billing When 
Cross Dock Period Ends
I = Initial Storage
R = Renewal Storage
If you set to I for Initial Storage, the system will charge initial storage when the cross-dock period ends. Initial storage will be based on the initial storage profile attached to IXDP. If you set to R for Renewal Storage, the system will charge renewal storage when the cross-dock period ends. Renewal storage will be based on the renewal storage profile attached to IBIP (Item Billing Profile).

1 Enter IXDP.

Item X-Dock Profile
2 Click on Create Record.
3 Key in your cross-dock profile code and press Enter.
4 Key in a meaningful description and press Enter.
5 Use your pick list function to select the appropriate initial storage profile code. To select a code using a pick list, press F8 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on Select Code to select it.
6 Use your pick list function to select the appropriate handling profile code.
7 Key in the number of days that an item is allowed to remain in cross-dock before being charged regular storage.
8 In the After Cross Dock Period Process field, key in the appropriate value (I for Initial Storage or R for 
Renewal Storage) and press Enter.
9 In the Renewal Date Flag field, key in the appropriate value (R for Original Receipt Date or X for Dock 
Date) and press Enter.
10 Click on Return to Main.
Renewal Date Flag X = Dock Date
R = Receipt Date
If you set to X for Dock Date, the system will generate renewals based on the date the cross-dock period ended. If you set to R for Receipt Date, the system will generate renewals based on the original receipt date of the product.
FIELD DESCRIPTIONS

Item X-Dock Profile
11 Click on Exit.
12 Enter ITEM.
13 Retrieve the item that you wish to set up for cross-dock billing.
14 Press Enter until your cursor is positioned on the Cross Dock field.

ITEM screen showing Cross Dock flag set to Y for Yes
15 In the Cross Dock field, key in Y for Yes and press Enter.

16 Click on Return to Main and then Exit to exit.
17 Enter DBIP (Depositor Billing Profile) and make sure that the Rate Receipt Automatically flag is set to N for No.

### ENTERING A CROSS-DOCK RECEIPT <a id="entering-a-cross-dock-receipt"></a>

You enter a cross-dock receipt by entering X as your line type in ENRE. After entering your inventory levels and your expected and received quantities in the normal manner, you enter your cross dock profile code in the Cross Dock field and make any necessary changes to the Close Date field. 
1 Enter ENRE.
2 Complete the ENRE Header Block as a normal P (Post-receiving) type of receipt.
3 When you reach the Line Block, press F9 (Previous Field) until the cursor is in the Type field. Then key in 
X and press Enter.

ENRE Line Block screen showing a Cross-Dock receipt type
4 Continue completing the Line Block until you reach the Cross Dock field. 
5 In the Cross Dock field, key in the cross dock code and press Enter. 
NOTE You cannot re-receive the same inventory entity during the cross-dock period. For example, if your cross dock period is four days and you receive item A, lot 
001 on day 1, you cannot receive the same inventory entity — that is, item A, lot 001 
— on day 2, 3 or 4.
Cross 
Dock type receipt line

ENRE Line Block screen showing a Cross Dock receipt type
6 The system automatically populates the Close Date field. If the system-entered date is correct as the last day for billing this entity at the cross dock rate, press Enter to accept. (Regular storage rates will apply after this date.)
If you need to change the system-entered date, key in the new date over the old using the same date format and press Enter.
7 Complete the remaining Line Block fields in the usual manner.
8 Enter any remaining receipt lines. Then press click on Return to Main to exit create mode.
9 Click on Master Block and Exit to exit.

### RATING A CROSS-DOCK RECEIPT <a id="rating-a-cross-dock-receipt"></a>

1 Receive and confirm the receipt in the normal manner.
2 When the cross-dock period ends, rate the receipt manually in RCRA (Receipt Rater).

### Surcharges <a id="surcharges"></a>

A surcharge is an additional charge that is based on the invoice total. The invoice “total” can be the total weight of an invoice, the total cube of an invoice or the total dollar amount of an invoice.
EXAMPLE 1 — Surcharge based on total weight of invoice
Cross Dock 
Profile Code
Last day of cross dock period. Regular charges begin after this date.

Your invoice total is $100, your total weight is 42,500 lbs and your fuel surcharge is 5 percent. Your surcharge would be 42500 / 100 (CWT) X .05 = 21.25, which would be added to the $100.
EXAMPLE 2 — Surcharge based on total dollar amount of invoice
Your invoice total is $100 and your fuel surcharge is 5 percent. Your surcharge would be 100 X .05 = 5, which would be added to the $100.
Surcharges can be based on any SKU type with the following qualifier codes: gross weight, net weight, cube, occurrence and invoice total value. You cannot use surcharges for SKU types whose qualifier code is unit, hour or value index.
You can set up flat rate surcharges by using a SKU type based on the qualifier code of OCCR for occurrence. 
A flat rate surcharge would be a fixed amount — say, $10.00 — added to each invoice regardless of the invoice total.
There are three types of surcharges in AccellosOne 3PL: receipt surcharges, renewal surcharges and accessorial surcharges. The type(s) of surcharge that you can use depend on your invoicing option. 

### WORKING WITH MULTIPLE SURCHARGES <a id="working-with-multiple-surcharges"></a>

You can have up to three surcharges for each invoicing option. Each surcharge can, if necessary, be based on a different invoice total. For example, surcharge 1 can be based on the total weight, surcharge 2 can be based on the total cube and surcharge 3 can be based on the total dollar amount. 
If you have multiple surcharges and all surcharges are based on the total dollar amount of the invoice, the surcharges can be calculated independently of each other or can be based on the original total plus another surcharge — that is, a surcharge on a surcharge. If you have multiple surcharges that are NOT all based on the total value of the invoice — that is, one is based on weight and one is based on the total dollar value of the invoice — each surcharge will be calculated independently of each other.

### SETTING UP SURCHARGES <a id="setting-up-surcharges"></a>

There are three steps to follow in setting up a surcharge.
NOTE Surcharges need not be based on the same value used to calculate the original invoice without the surcharge. For example, you can charge renewal storage by the case or by the pallet and then add a fuel surcharge to the invoice total that is based on weight.
OPTION TYPE OF SURCHARGES ALLOWED
IND no restriction on type of surcharge
UALL accessorial surcharges only
UREC accessorial and renewal surcharges only
UREN receipt and accessorial surcharges only

1 Check your SKU type in SKUS to make sure that the qualify on value is correct.

SKUS screen showing SKU code for invoice total value

SKUS screen showing SKU code for hundredweight
2 Set up your charge code in CHAR. Your charge type must be either SING or MULT.

CHAR screen showing charge code of SUR1 with a charge on and qualify on SKU type of INVT for 
Invoice Total Value 
3 In RATE make sure that the Exclude from Surcharge Calculations flag is set to No.
4 Set up your depositor billing profile in DBIP. If you are adding two surcharges to the same invoicing option, you must set the Inclusive of Previous Surcharge flag to the appropriate value. 
5 If you are adding three surcharges to the same invoicing option, you must set the Inclusive of Previous 
Surcharges flag to the appropriate value. Make sure that the qualifier code of the SKU type attached to the charge code is set to Invoice Total Value for all charge codes.
Inclusive flag = No Surcharges are calculated independently of each other.
Inclusive flag = Yes Only available if both surcharges are based on the total dollar value of the invoice
Second surcharge is based on invoice total plus amount of first surcharge.
Inclusive flag = First Third surcharge is based on invoice total plus amount of first surcharge.
Inclusive flag = Second Third surcharge is based on invoice total plus amount of second surcharge.
Inclusive flag = Both Third surcharge is based on invoice total plus amount of first and second surcharges.

DBIP screen showing two mutually exclusive surcharges for accessorial invoicing

### USING SURCHARGES TO CALCULATE TAXES <a id="using-surcharges-to-calculate-taxes"></a>

You can use surcharges to calculate taxes such as the GST and PST provided that all of the customer’s items are subject to the tax. If some items are taxable and some items are non-taxable, you cannot use surcharges to calculate tax. Instead, you must attach the appropriate tax code to your depositor billing profile and to your items. See the section [Taxes](faturamento-setup.html#taxes) for further information.
When you use surcharges to calculate taxes, the tax is based on the total charges at the header level; that is, all charges on the invoice. If you wish to calculate charges at the line level (that is, taxes calculated separately for each line on the invoice), you must use AccellosOne 3PL’s predefined tax codes: GST, PST, GST1, etc.
1 Make sure that the qualifier code of your SKU type in SKUS is set to Invoice Total Value.
2 Create a charge code for the tax in CHAR and set the Charge on SKU Code and Qualify on SKU Code values to your invoice total value SKU code.
3 Create a record for your new charge code in RATE and set the rate to the appropriate percentage (for example, 6% for the GST).
4 Attach the charge code that you created in CHAR to your depositor billing profile in DBIP. The charge code must be attached to all three surcharge fields: Receipt Surcharge Charge Code, Renewal Surcharge Charge Code and Accessorial Surcharge Charge Code. 
If you are not already using surcharges, your new charge code for taxes should be attached to the first receipt, renewal and accessorial surcharge fields. If you are already using surcharges, your new charge 
Inclusive flag = None Third surcharge is calculated independently of first two surcharges.

code for taxes should be attached to the first unused surcharge field and the Inclusive flag for the previous field should be set to Y for Yes. 
For example, if you already have a fuel surcharge attached to the Accessorial Surcharge Charge Code 1 field, your new charge code for taxes must be attached to the Accessorial Surcharge Charge Code 2 field. 
5 Make sure that the Tax Code fields in DBIP and ITEM are set to NONE.

### Density Rating <a id="density-rating"></a>

The density rater allows you to rate an item based on its density; that is, use a different charge code depending on the density of the item. For example, if the density of the item is under 10 lbs. per cubic foot, use charge code CHAR-1; if the density of the item is between 10 and 20 lbs. per cubic foot, use CHAR-2, etc.
The density of the product is compared to the breaks set up in DECH (Density Charge Codes) and the appropriate charge code is selected. Density is calculated in pounds per cubic foot. The normal rating process then continues with the rate being calculated based on the weight breaks in RATE.
EXAMPLE
You receive 1,000 cases of boxed shrimp weighing 25 lbs per case. Case dimensions are 9.5 x 11.25 x 19.5 inches for a total volume of 1.206 cubic feet. The density is 20.73 lbs. per cubic foot.
When you receive the item shrimp and this item has a charge type of DENS (for density), the system looks up the item’s charge code in DECH. The item’s charge code in DECH contains the density weight breaks and the corresponding charge codes:
Because the item’s density is 20.73, the charge code of CHAR-2 applies. The system then looks up the 
CHAR-2 record in RATE and calculates the charges.
You can use density rating for any type of charge in AccellosOne 3PL — receipt charges, renewal charges, accessorial charges, etc.

### SETTING UP DENSITY CHARGES <a id="setting-up-density-charges"></a>

1 Enter CHAR and create your charge code for density rating. Set the Charge Type Code to DENS and then enter your Invoice Type Code. The remaining fields in CHAR are not required for a density charge code.
BREAK VALUE CHARGE CODE
10 CHAR-1
15 CHAR-2
25 CHAR-3

Charge Code screen showing density type charge code
2 If you have not already done so, create your regular, non-density charge codes for each density break.
3 Exit CHAR and enter DECH.
4 In DECH, key in your density charge code in the Density Charge Code field and press Enter.
5 In the Detail Block, click on Create Record. Then enter the density value and charge code for each density break.

Density Charge Codes screen showing three density breaks
6 When you finish entering your density breaks, click on Return to Main to exit create record mode.
7 Exit DECH and attach your density charge code to the appropriate profile (for example, IISP, IRSP, etc.).
8 Enter ITEM and make sure that the items that density rating applies to have the correct weight and cube.

### Flat Rate Charges <a id="flat-rate-charges"></a>

You can set up flat rate charges such as producing a bill of lading, loading/unloading a truck, cleaning up a spill, etc. by using the qualifier code of Occurrence. During invoicing, you add the special charge code that you created in CHAR to the invoice and the customer is billed for the one-time flat rate charge. 
1 Enter SKUS and create a SKU code called OCCR based on a qualifier code of OCCR (Occurrence).

Stock Keeping Units screen showing SKU type of OCCR for Occurrence
2 Enter CHAR and create your new charge code using OCCR as the SKU type that you will be charging on. Set the Charge Type Code to SING (Single Break) and the Charge Definition to F for Flat.

Charge Code screen showing charge code of BOL
3 When you finish setting up your new charge code, you can add it to an invoice as a regular accessorial charge.

### Hourly Based Charges <a id="hourly-based-charges"></a>

You can set up hourly based charges for extra labor, etc. by using the qualifier code of Hour. During invoicing, you add the charge code that you created in CHAR to the invoice and the customer is billed for the extra labor charges.
1 Enter SKUS and create a SKU code called HR based on a qualifier code of HOUR.
Charge on and Qualify on 
SKU’s set to OCCR

Stock Keeping Units screen showing SKU type of HR for Hours
2 Enter CHAR and create your new charge code using HR as the SKU type that you will be charging on. 
Set the Charge Type Code to SING (Single Break) and the Charge Definition to B for Break.

Charge Code screen showing charge code of LAB
3 When you finish setting up your new charge code, you can add it to an invoice as a regular accessorial charge.
Charge on and 
Qualify on SKU’s set to HR

### Customer Fixed Charges <a id="customer-fixed-charges"></a>

Customer fixed charges allow you to generate recurring accessorial charges for your customers to cover noninventory fixed rate charges such as rent, administration, labor, etc. For example, you rent out a facility to a customer but do not track that customer's inventory. Or you have an administration fee of $500 a week in addition to the usual initial, handling and renewal storage charges for a customer's inventory.
Recurring accessorial charges will be generated automatically whenever you create a new accessorial batch in BILB. (A cron job in Unix set up by HighJump is required to generate the accessorial charges.) 
You set up your recurring accessorial charges in the Fixed Charges Block of CUST. You can also set them up in the stand-alone program CUFC.
FIELD DESCRIPTIONS
Customer Code The customer being charged.
Charge Code Your occurrence-based charge code.
Charge Quantity Usually 1. If you enter a number greater than 1 (for example, 2), two charges will be generated instead of one.
Frequency Code Anniversary Weekly - Same Day Next Week
Anniversary Monthly
Daily
Monthly - 1st of Month
Monthly - Last Day of Month
Weekly as of Monday
If you have regular billing periods, the frequency of the charge.
Date Profile Code (DAPR)
Optional
Your date profile code if you have irregular billing periods.
Start Date Your start date for the charge.
End Date Optional
If you enter an end date for the charge, the charge will end on that date. If you leave this field blank, the charge will continue until you delete the record.

CUFC screen showing fixed charge for weekly RENT

### Multi-Currency Billing <a id="multi-currency-billing"></a>

Multi-currency billing allows you to work in two or more currencies. You define your base or home currency in 
COMP (Company Code) and the currency that you wish to invoice a customer in in DBIP (Depositor Billing 
Profile). In the program CURX (Currency Exchange Rates), you set up your exchange rates for each invoicing or non-base currency.
1 You activate multi-currency support by setting the Use Multiple Currencies flag on the Financial tab of 
COMP (Company Code) to Yes and selecting your base currency in the Home Currency Code field.
Remarks Optional
Your remarks for the charge.
FIELD DESCRIPTIONS

COMP screen showing multi-currency billing activated
2 In CURX (Currency Exchange Rates), you set up your exchange rates for each invoicing or non-base currency. 
CURX screen showing exchange rates and effective dates for euro
3 If you set the Update Rate flag to Y for Yes, AccellosOne 3PL will automatically update your rates in 
RATE whenever the exchange rate changes. For example, suppose your base currency in DBIP is Canadian and the Canadian dollar falls by 50% in relation to the US dollar; if you charge 1$ CDN a month for storage, a new record will be created in RATE in which the rate is now $1.50 per month.
LOIN (Look Up Invoices) shows two amounts: the amount invoiced to the customer in the customer’s currency and the base amount in your company’s currency.

LOIN screen showing invoice amount in US dollars and base amount in CDN dollars
Multi-currency billing requires a custom invoice document from HighJump.

### Billing Batch Automation <a id="billing-batch-automation"></a>

Billing batch automation allows you to generate and confirm billing batches in the background on a predetermined schedule. It eliminates the need to manually create and confirm extra charge, renewal, accessorial and immediate batches in BILB (Billing Batch).
Billing batch automation requires a cron job set up in Linux.
You activate billing batch automation in COMP by selecting the appropriate option from the Processing Billing 
Batch (BILB) Automatically field. If you leave this field blank, billing batch automation will be deactivated.

COMP screen showing Processing Billing Batch (BILB) Automatically field
Generate All Batches Except DLRE
AccellosOne 3PL will generate batches up to “Generated” status for all batch types except the Daily Invoice 
Register.
Generate All Batches Up To Confirmation
AccellosOne 3PL will generate batches all the way to “Confirmed” status.
Automate Billing Processes by IBIP Invoice Type
For custom use only.

### Automatic Pre-Renewal Billing <a id="automatic-pre-renewal-billing"></a>

Automatic pre-renewal billing allows you to automatically generate charge records for your renewal batch in the background on a predetermined schedule. Its purpose is to shorten the processing time of a renewal batch in BILB by catching and correcting as many billing errors as possible before generating your renewal batch at mid-month or at the end of the month.
Charges generated through automatic pre-renewal billing are added to the pre-renewal batch type PRNW. 
This batch type first executes the RENW (Renewal Preprocessor) process and then picks up all billing entities whose next renewal date is less than or equal to the current date and creates the necessary charge records in the charge table.
Automatic pre-renewal billing does not support the following billing options:
 renewal summarization
 splitting out invoices by alternate reporting type codes

If required, you can audit pre-renewal batch charges in a d’Amigo report. Should you find errors in the prerenewal batch, you cannot delete it in BILB. However, you can delete the renewal batch.
If you delete a renewal batch containing pre-renewal batch charges, you delete all the newly generated charges in the renewal batch plus any pre-renewal batch charges as well.That means that the next renewal batch could take longer to generate since the pre-renewal generated charges would need to be re-created.
You activate automatic pre-renewal billing in CUST by setting the Automatic Pre-Renewal Billing flag to Yes. 
You then define your pre-renewal schedule (every night at 11pm, every two days, every week, etc.) in a Linux cron job.
You generate your renewal batch normally in 
BILB and pick up all PRNW charges from days 
1, 2 and 3 as well as any new billing entities whose next renewal date is less than or equal to current system date.
Day 2
Day 3
Batch type PRNW is run again and picks up all new billing entities whose next renewal date is less than or equal to current system date.
Batch type PRNW is run again and picks up all new billing entities whose next renewal date is less than or equal to current system date.
Day 1
Day 30
Batch type PRNW is run and picks up all billing entities whose next renewal date is less than or equal to current system date.

CUST screen showing Automatic Pre-Renewal Billing field

## Charge And Rate Setup <a id="charge-and-rate-setup"></a>

*Manual N — Setup Guide*

### General Ledger Chart of Accounts (GLCH) <a id="general-ledger-chart-of-accounts-glch"></a>

OVERVIEW
In this program, you set up your general ledger accounts in AccellosOne 3PL. The accounts that you set up in 
GLCH should be identical to the accounts that you use or will be using in your accounting system to track warehouse revenue. You can set up accounts to capture revenue by various buckets such as division, customer, warehouse, etc. and within these buckets can record revenue by type of charge — for example, storage, handling, accessorial and renewals. If required, you can also set up accounts for taxes.
The accounts that you set up in GLCH are attached to specific charge codes in CHAR and these charge codes are then attached to specific divisions, customers, items, charges, etc. During the billing cycle in AccellosOne 3PL, the revenue generated is posted to the appropriate account.
Accounts set up in GLCH are not activated until they are linked to a particular charge code in CHAR. If you create an account in GLCH but do not link it to a charge code, the account will not be active and no revenue will be posted to it.
If you do not use AccellosOne 3PL to generate invoices or gather billing information, you do not need to set up a chart of accounts. 
PREREQUISITES: None
ATTACHED TO: CHAR (Charge Codes)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you use AccellosOne 3PL to gather billing information or generate invoices
OTHER REQUIREMENTS: You must have a list of your chart of accounts
NOTE If AccellosOne 3PL is linked to your accounting system, you can use your general ledger accounts to track revenue by company/division, customer and warehouse location. Refer to the program GLMO (General Ledger Modifier Code) for instructions before setting up your GL accounts.
FIELD DESCRIPTIONS
General Ledger Code Mandatory
Your general ledger account number.

PROCEDURE
1 Enter GLCH.
2 Key in your general ledger code and press Enter.
3 Key in your description and press Enter.
4 Press Enter three times to bypass the G/L External Reference 1, G/L External Reference 2 and Status fields.
5 Repeat the above three steps for each additional general ledger code that you wish to add.

General Ledger Chart of Accounts
6 When you finish adding your codes, click on Return to Main and then Exit to exit.
Description Mandatory
Your account description.
G/L External Reference 1 Special programming by HighJump required.
G/L External Reference 2 Special programming by HighJump required.
TIP You do not need to set up a separate general ledger account for each charge that you wish to track. Instead, you can use revenue analysis codes defined in REVA to track each charge at whatever level of detail you require. The advantage of using 
REVA for this function is its enhanced reporting capabilities, which allow you to generate reports for only those charges that interest you.
FIELD DESCRIPTIONS

### Currency Codes (CURR) <a id="currency-codes-curr"></a>

OVERVIEW
In this program, you set up your currency code(s). If multi-currency billing is NOT activated on your system, you set up a single currency code for all your customers and attach it to your depositor billing profile(s) in 
DBIP. The single currency code that you set up in CURR does not print on any AccellosOne 3PL invoice document or report.
If, on the other hand, multi-currency billing is activated on your system, you set up a record in CURR for each currency that you wish to use. As well, you define your exchange rates in CURX (Currency Exchange Rates). 
Currency codes in a multi-currency billing environment DO print on most invoice documents and sales reports.
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
Trade G. L. Account (defined in GLCH)
Mandatory
Enter the dummy account number that you created in GLCH.
Discount G. L. Account Reserved for future use
Interest G. L. Account Reserved for future use
Trade G. L. Account Reserved for future use
Discount G. L. Account Reserved for future use
Interest G. L. Account Reserved for future use
FIELD DESCRIPTIONS

Currency Codes
9 Press Enter to bypass the remaining G.L. account fields.
10 When you finish entering your currency code(s), click on Return to Main and then Exit to exit.

### Bank Code (BANK) <a id="bank-code-bank"></a>

OVERVIEW
In this program, you set up your bank account. If you use multi-currency billing, you must set up one record in 
BANK for each currency.
PREREQUISITES: GLCH, CURR
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Only required if you invoice your customers in AccellosOne 3PL
OTHER REQUIREMENTS:

PROCEDURE
1 Enter BANK.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
3 If you need to set up another code, click on Create Record.
4 Key in your bank code and press Enter.
5 Key in any number as your bank account number or use NA for Not Applicable and press Enter.
6 Key in your GL account for the bank account and press Enter or use the pick list function (F10) to select it.
7 Key in your currency code for the bank account and press Enter or use the pick list function (F10) to select it.
8 Click on Return to Main to exit Create Record mode.
FIELD DESCRIPTIONS
Bank Code Mandatory
Your bank code.
Description Mandatory
Your bank code description.
Bank Account Number Mandatory
Key in any number as your bank account number or use NA for Not Applicable.
Bank GL Account (defined in GLCH)
Mandatory
Enter the dummy account number that you created in GLCH.
Currency Code (defined in CURR)
Mandatory
The currency code for your bank account.

Bank Code
9 Click on Exit to exit.

### General Ledger Modifier Code (GLMO) <a id="general-ledger-modifier-code-glmo"></a>

OVERVIEW
This program allows you to use your general ledger accounts to track revenue by company/division, customer and location billing code. If you use this program, you avoid the need to create dozens of charge codes for each location billing code, customer, etc. whose revenue you wish to track.
PREREQUISITES: GLCH
ATTACHED TO: LODE (Location Billing Codes)
or
CUST (Customer Setup) 
or
COMP (Company Code)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: You must have a list of your chart of accounts

You use “wildcard” characters in your general ledger chart of accounts to indicate that certain digits in the account number are variables. AccellosOne 3PL supports the following wildcards:
* represents a customer defined in CUST
? represents a location billing code defined in LODE
= represents a company/division defined in COMP
For example, if you set up an account called Handling with the number ***11000, you are indicating that the first three digits of the account refer to any customer on your system. Likewise, an account called Renewal 
Storage with the number 100==300 would indicate that the fourth and fifth digits refer to any company or division in your warehouse.
The general ledger modifier in GLMO converts these wildcards to the appropriate digit(s) so that your chart of accounts shows your exact revenue by customer, company or location billing code.
EXAMPLE 1 — TRACKING INITIAL STORAGE BY COMPANY 
In this example, you wish to track initial storage by company and your GL account for initial storage is XX2100 where XX is the company number. You have three companies on your system: 01, 02 and 03.
1 In GLCH you create an initial storage GL account numbered ==2100.
2 In GLMO you set up your GL modifier code for each company:
Enter company 01 and create a 01 code in GLMO.
Enter company 02 and create a 02 code in GLMO.
Enter company 03 and create a 03 code in GLMO.
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of ==2100.
4 In COMP (Company Code) you attach the GL modifier code that you created in GLMO to your three companies.
Enter company 01 and attach your 01 GLMO code to it.
Enter company 02 and attach your 02 GLMO code to it.
Enter company 03 and attach your 03 GLMO code to it.
5 Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to the appropriate company. At the end of the day, AccellosOne 3PL will generate three Initial Storage accounts (012100, 022100 and 032100) showing all charges for that company.
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

5 Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to the appropriate customer. At the end of the day, AccellosOne 3PL will generate three Initial Storage accounts (310100, 310200 and 310300) showing all charges for that customer.
EXAMPLE 3 — TRACKING INITIAL STORAGE BY LOCATION BILLING CODE 
In this example, you wish to track initial storage by location billing code and your GL account for initial storage is 2100XX where XX is the location billing code.
1 In GLCH you create an initial storage GL account numbered 2100??.
2 In GLMO you set up your GL modifier code for each location billing code:
01 = Location Billing Code A
02 = Location Billing Code B
03 = Location Billing Code C
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of 2100??.
4 In LODE (Location Billing Code) you attach the GL modifier code that you created in GLMO (01, 02, 03, etc.) to the appropriate location billing code.
5 Whenever you put-away product into a particular location, the charges are calculated and assigned to the appropriate location billing code. At the end of the day, AccellosOne 3PL will generate three Initial 
Storage accounts (210001, 210002 and 210003) showing all charges for that location billing code.
6 If your system consists of two or more global companies, you must perform your GLCH and GLMO setup in each global company.
EXAMPLE 4 — TRACKING INITIAL STORAGE BY WAREHOUSE
In this example, you wish to track initial storage by warehouse and your GL account for initial storage is 
31XX00 where XX is the warehouse number.
1 In GLCH you create an initial storage GL account numbered 31**00.
2 In GLMO you set up your GL modifier code for each warehouse:
01 = Warehouse 1
02 = Warehouse 2
03 = Warehouse 3
3 In CHAR (Charges) you set up a charge code for initial storage and assign to it the GL code of 31**00.
NOTE If your system consists of two or more global companies, you must perform your GLCH and GLMO setup in each global company.
NOTE This method only works if your customers are restricted to a single warehouse. If customers can span warehouses, you may have to manually allocate a customer’s revenue to two or more warehouses.

4 In CUST (Customer) you attach the GL modifier code that you created in GLMO (01, 02, 03, etc.) to the appropriate customer. For example, if customer A’s product is stored in warehouse 01, you would enter 
01 in the G. L. Modifier field.
Whenever you confirm a receipt from one of your customers, the charges are calculated and assigned to the appropriate warehouse. At the end of the day, AccellosOne 3PL will generate three Initial Storage accounts (310100, 310200 and 310300) showing all charges for that warehouse.
FIELD DESCRIPTIONS
G.L. Modifier Mandatory
Your general ledger modifier number.
Description Mandatory
Your general ledger modifier description.
Substitution Modifier Optional
The substitution modifier allows users to set up new customers, companies and location billing codes without the need to know the general ledger chart of accounts. For example, suppose you have three facilities in three states (C for 
California, T for Texas and N for Nevada) and two types of customers (F for 
Freezer and D for Dry).
Your staff could use codes like CF for a California freezer customer and TD for a Texas dry customer when setting up new accounts. AccellosOne 3PL would convert these codes to the correct general ledger accounts during billing. If you changed your accounts, the same codes — CF, TD, etc. — could point to the new accounts, making the change transparent to your staff. 
GL Modifier
CF
TD
NF
Substitution Modifier
NOTE The number of characters in the substitution modifier must match the number of wildcard characters. For example, if your GL code is **123, the substitution modifier must also be two characters — AB, 01, XY, etc.
Company Reference 
Code
Special programming by HighJump required.

PROCEDURE
1 Enter GLCH and make the necessary changes to your chart of accounts.

GLCH showing the use of wildcards to designate a company
2 Enter GLMO.
3 Key in your GL code and press Enter.
4 Key in a description for your code and press Enter.
5 If required, key in your substitution modifier and press Enter or press Enter with the field blank to bypass this option.
6 Press Enter twice to bypass the Company Reference Code and Account Reference Code fields.
7 Repeat the above steps for each additional GL modifier that you wish to add.

General ledger modifier codes for three companies
8 When you finish adding your codes, click on Return to Main and then Exit to exit.
Account Reference Code Special programming by HighJump required.
FIELD DESCRIPTIONS

SETTING UP DESCRIPTIONS FOR WILDCARD ACCOUNTS
If you use wildcard characters in your general ledger accounts to track revenue by company/division, customer or location bill code, the description in the daily invoice register for any account containing a wildcard character will appear as UNKNOWN. If you wish to see a valid description for your accounts, you must set up a separate account in GLCH (GL Chart of Accounts) with the correct description for each company/division, customer or location bill code. 
EXAMPLE
In this example, you have two wildcard characters (==) for the company and one wildcard character (?) for the location bill code in your general ledger account for renewal storage (==?3010). There are two companies in your system (W7 and W8) and two location bill codes (code 3 and code 4). You must set up one record in GLCH for each company code/ location bill code combination in addition to your ==?3010 code.

GLMO screen showing four records for each company/location billing code combination

### Revenue Group Codes (REGR) <a id="revenue-group-codes-regr"></a>

OVERVIEW
In this program, you set up your revenue group codes. Revenue group codes allow you to consolidate two or more revenue analysis codes into a single group. Revenue group codes can be printed on invoices and audit reports to show all revenue from a group of revenue analysis codes.
PREREQUISITES: None
ATTACHED TO: REVA (Revenue Analysis) --> CHAR
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

PROCEDURE
1 Enter REGR.
2 Click on Create Record.
3 Key in your revenue group code and press Enter.
4 Key in your description and press Enter.
5 Repeat the above steps for each additional code that you wish to add.

Revenue Group Codes
6 When you finish adding your codes, click on Return to Main and Exit to exit.

### Revenue Analysis Codes (REVA) <a id="revenue-analysis-codes-reva"></a>

FIELD DESCRIPTIONS
Revenue Group Mandatory
Your revenue group code.
Description Mandatory
Your revenue group code description.
PREREQUISITES: REGR

OVERVIEW
In this program, you set up your revenue analysis codes. Revenue analysis codes allow you to group two or more charge codes in a single category for revenue reporting purposes. For example, you create a revenue analysis code of LA for Labor and attach it to the following four charge codes
▪ charge code 1 for miscellaneous labor
▪ charge code 2 for extra help
▪ charge code 3 for lumper rate
▪ charge code 4 for handling inbound damage
When you run the SALE (12-Month Sales Report) or some other sales report, you enter LA as your revenue analysis code restriction. AccellosOne 3PL will show only revenue generated through the four charge codes to which you have attached your LA revenue analysis code. 
If you do not wish to use revenue analysis in AccellosOne 3PL, you must create a single NA (Not Applicable) 
revenue analysis code. 
ATTACHED TO: CHAR (Charge Code) 
INRE (Invoice Register Definition)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE Revenue analysis codes are for management reporting purposes only; there is no need for a one-to-one relationship between these codes and your general ledger accounts. For example, you can have one general ledger account for initial storage and a number of revenue analysis codes to report on storage revenue by each of your customers.
FIELD DESCRIPTIONS
Revenue Analysis Code Mandatory
Your revenue analysis code. For example, HA for Handling.
Description Mandatory
Your revenue analysis description.

PROCEDURE
1 Enter REVA.
2 Click on Enter Criteria then Execute Query to view which revenue analysis codes have already been set up. A minimum of one code (for example, NR for Not Required) is mandatory. 
3 If the codes that you require have already been set up, click on Exit to exit. There is no need to add any new codes to REVA. If the codes that you require have not been set up, click on Create Record.

Revenue Analysis Code
4 Key in your revenue analysis code and press Enter.
5 Key in a meaningful description and press Enter.
6 If required, key in your revenue analysis group code in the Revenue Group Code field and press Enter. If you do not use revenue analysis groups, press Enter with the field blank to bypass this option.
Revenue Group Code (defined in REGR)
Optional
If you have set up revenue analysis group codes in REGR, you assign the appropriate revenue analysis group code to your revenue analysis code.
True Revenue Y = Yes
N = No
If you select Yes, the revenue will be considered true revenue (that is, money paid by your customer that goes to you) and included in your sales reports such as SALE (12-Month Sales Report) and BIRR (Billing Renewals Report).
If you select No, the revenue will be considered non-true revenue and will not be included in your sales reports. You use non-true revenue to record revenue such as a tax remitted to the government or a rebate from the government.
FIELD DESCRIPTIONS

7 In the True Revenue field, key in Y for Yes or N for No and press Enter.
8 Repeat steps 4 to 7 for each additional revenue analysis code that you wish to set up.
9 When you finish setting up your codes, click on Return to Main and then Exit to exit the program.

### Invoice Types (INTP) <a id="invoice-types-intp"></a>

OVERVIEW
In this program, you set up your invoice types. You use invoice types in the billing program BILB (Billing 
Batch) to restrict the types of charges that will appear on an accessorial invoice or to split out the charges on two or more invoices.
For example, you create an invoice type called LABOR CHARGES. Then you attach this invoice type to one or more charge codes in CHAR (Charge Codes). When you enter BILB (Billing Batch), you specify in the 
Select Block of this program that you want only charges whose invoice type is LABOR CHARGES to be included in the invoice. When generate your accessorial batch, the batch will be restricted to accessorial labor charges.
If you do not use AccellosOne 3PL for billing or do not need to restrict certain charges in BILB, you do not need invoice types. Create a single invoice type called NA for Not Applicable.
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

PROCEDURE
1 Enter INTP.
2 Click on Enter Criteria then Execute Query to see which, if any, invoice types have already been set up.

Invoice Types
3 Using your arrow keys, go through each record to see which invoice types have already been set up. If the types that you require have already been set up, click on Exit to exit. There is no need to add any new codes to INTP.
4 If the invoice types that you require have not been set up, click on Create Record. 
5 Key in your new invoice code and press Enter.
6 Key in a meaningful description for your new code and press Enter.
7 Repeat steps 5 and 6 for each additional invoice type that you wish to add.
8 When you finish entering your invoice types, click on Return to Main and then Exit to exit the program.

### Charge Codes (CHAR) <a id="charge-codes-char"></a>

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

OVERVIEW
In this program, you set up standard tariff charge codes for the various rates that you will be using for your initial storage, renewal storage, handling and accessorial charges. You should set up a separate charge code for each handling charge or additional service for which you have a standard rate (for example, stencilling cases, case picking, labelling, sorting, etc.).
CHAR defines four major parameters for your charges:
▪ the type of charge (single break, multiple break, no charge, etc.)
▪ the charge definition (break, flat or combination)
▪ the general ledger account for the charge
▪ the SKU type or unit of measure that the charge is based on (pallets, cases, pounds, etc.)
Once set up, the code that you create in CHAR is attached to RATE (Depositor Billing Rates), which specifies the actual rates — that is, the weight breaks, minimum charge, flat rate, the customer to whom the charge applies, etc.
You must set up at least one charge code to run AccellosOne 3PL. If you do not use AccellosOne 3PL to gather billing information or generate invoices, you use the NC (No Charge) charge code.
CUSTOMER LEVEL VERSUS ITEM LEVEL BILLING
You can set up charges at both the item level and the customer level. At the item level, you attach your charge code to IISP (Item Initial Storage Profile), IRSP (Item Renewal Storage Profile) and IHAP (Item Handling 
Profile). These profiles are attached to IBIP (Item Billing Profile), which is then attached to your items in ITEM. 
At the customer level, you can set up certain maximum and minimum charges that apply to an invoice. You attach these charge codes to DBIP (Depositor Billing Profile). DBIP is then attached to your customer in 
CUST. 
OTHER REQUIREMENTS: A list of all charges (handling, shrink wrapping, etc.) that can be applied to a customer.
NOTE Charge codes should not be customer specific. If you wish to give a special rate to a particular customer, you set up one charge code in CHAR (for example, HA for Handling) for all customers. Then you enter RATE (Depositor Billing Rates) and create two records. The first record contains your standard rates and is attached to the customer .ALL while the second record contains your special rates and is attached to the customer to whom the special rates apply.

FIELD DESCRIPTIONS
Charge Code Mandatory
Your charge code. For example, HIN for handling inbound. The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used in a charge code.
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

Description Mandatory
Your charge code description.
Reference Optional
If required, you can add reference information to your charge code; for example, all your handling charge codes could have “Handling” as their reference. 
Special programming by HighJump is required if you wish to print this information on a document or capture it for EDI purposes. 
External Reference Special programming by HighJump required.
Charge Type Code Refer to the Billing and Invoicing Guide for charge type codes other than Single, Multi and No Charge.
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
For a receipt of 12,000 lbs., AccellosOne 3PL will charge $0.07 per lb. (that is, a single rate will be applied to the entire weight).
FIELD DESCRIPTIONS

MULTIPLE (Charge on multiple breaks)
Multiple type rating selects the appropriate rate for each weight break and calculates the charge for that break. Then it adds up all the charges to arrive at the final charge.
EXAMPLE 3
For a receipt of 12,000 lbs., AccellosOne 3PL will rate as follows:
1st 5000 lbs. is charged $0.09 per lb.
next 4000 lbs. is charged $0.08 per lb.
next 3000 lbs. is charged $0.07 per lb.
NOTE Multi-break charge codes require that the charge on SKU code be the same as the qualify on SKU code. You cannot qualify on pounds and charge by hundredweight.
When you use multi-break charges, the rate appearing on the invoice will be averaged. For example, if your rate for the first 1,000 lbs. is .60 and for the next 500 lbs. is .50, the rate on an invoice for a receipt of 1,500 lbs. would be 
.57 (the total charges divided by the total weight).
NO CHARGE
This type is used when no billing is necessary. When you select no charge, the majority of fields in CHAR are bypassed when creating a new record.
This charge type is necessary because certain billing profiles such as Initial 
Storage require a valid charge code. If you don’t wish to charge Initial Storage for a particular customer, you must set up a billing profile for that customer with the charge code set to “No Charge.”
FIELD DESCRIPTIONS

Charge Definition Mandatory
The charge can be a flat rate, a linear charge multiplied by a quantity or a combination of the two. 
B = Break
F = Flat
C = Combination (See Billing and Invoicing Guide)
The Charge Definition field works in conjunction with the Charge Type Code field. There are two valid values for the Charge Definition:
BREAK
Use Break when you wish to multiply the charge by a particular quantity.
FLAT
Use Flat when you wish to charge the same amount regardless of quantity.
General Ledger Code (GLCH)
Mandatory
The GL account to which the revenues from this charge will be posted.
Revenue Analysis Code (REVA)
Mandatory
The revenue analysis code to which this charge is assigned.
Invoice Type Code (INTP)
Mandatory
The invoice on which the charge will appear. You use invoice types in the billing program BILB (Billing Batch) to restrict the types of charges that will appear on an accessorial invoice or to split out the charges on two or more invoices.
If you do not use AccellosOne 3PL for billing or do not need to restrict certain charges in BILB, use your NA for Not Applicable invoice type.
FIELD DESCRIPTIONS

Charge on SKU Code (SKUS)
Mandatory
The SKU code that you are charging on. For automatic charges such initial storage or renewal storage, the qualifier code of your SKU in SKUS should be 
UNIT, WGTG or WGTN. For manual charges such as bill of lading or labelling charges, the qualifier code of your SKU can be HOUR or OCCR.
See “Charge on SKU Code vs. Qualify on SKU Code” (ver [Charge Codes (CHAR)](faturamento-setup.html#charge-codes-char)) for further information.
Rounding Flag Rounding only applies to charges based on a unit-base SKU that is NOT the smallest SKU in the item’s quantity breakdown. For example, if your quantity breakdown is pallet/case/each, rounding only applies if you charge by pallet or case. If you charge by each, no rounding will occur.
U = Up
D = Down
N = No rounding
This flag is used when you are charging by one unit-based SKU type (for example, cases) and shipping or receiving partial quantities of this type (for example, pieces).
Suppose you charge for handling by the case but ship and receive in cases / pieces and your quantity breakdown is 10 pieces per case. Should you receive 5 cases and 4 pieces, you have to tell AccellosOne 3PL how to charge for this partial quantity. 
Round flag set to
Up
Down
No rounding
System will charge for
5.4
If you charge by either weight or the smallest unit-based SKU, set this flag to 
N for No Rounding.
Qualify on SKU Code (SKUS)
Mandatory
Usually the same as your charge on SKU code. See “Charge on SKU Code vs. Qualify on SKU Code” (ver [Charge Codes (CHAR)](faturamento-setup.html#charge-codes-char)) for further information.
Rounding Flag Rounding rules for partial quantities of Qualify on SKU code. See previous 
Rounding Flag field for an explanation.
FIELD DESCRIPTIONS

Default Rate Charge 
Code
Optional
If two charge codes have the same rates, you can set up two charge codes that have different general ledger and revenue analysis information but use the same rates. See the Billing and Invoicing Guide for further information.
Charge Formula Reserved for future use
Tax Code Optional
GST
GST1
GST2
HST1/2/3/4/5/6/7/8/9
NONE
PST
The tax code that you enter (if any) overrides the customer tax code in DBIP and the item’s tax code in ITEM. 
Tax codes defined at the charge code level are designed for facilities in which multiple warehouses in different states or provinces with different tax rules and/or rates are assigned to the same company in COMP. For example, product stored and shipped within Ontario could be charged an HST rate of 13% for renewal storage, while product stored and shipped within British Columbia could be charged an HST rate of 12% for renewal storage. 
In this scenario, you would need to set up two charge codes in CHAR: one for 
Ontario renewal storage (tax code = HST) and one for BC (British Columbia) 
renewal storage (tax code = HST1). You would then attach these charge codes to different renewal storage profiles in IRSP and different item billing profiles in IBIP. 
Alternatively, you could set up a single renewal storage profile in IRSP and assign different charge codes to different location bill codes; for example, HST for your ON (Ontario) location billing code and HST1 for your BC location billing code.
FIELD DESCRIPTIONS

CHARGE ON SKU CODE VS. QUALIFY ON SKU CODE
The Charge on SKU code refers to the SKU type or unit of measure that you wish to charge by or bill by. For example, if your customer receives product as cases/pieces, do you wish to charge by the case, by the piece or by weight.
The Qualify on SKU code refers to the SKU type or unit of measure that you wish to “qualify on” — that is, the 
SKU type or unit of measure that you will count to determine your per rate. In the majority of cases, your “qualify on” SKU type will be the same as your “Charge on” SKU type. 
In a small number of cases, your “qualify on” SKU type will differ from your “Charge on” SKU type. See the following example.
Tax Code Override Flag Y = Yes
N = No
If you set this flag to Y for Yes, the operator will be forced to select the appropriate tax code from a pick list when adding accessorial or immediate charges to an invoice in ENAC/ENIN. 
If you set this flag to N for No, the Tax Code field in ENAC/ENIN will be automatically populated with either the charge code’s tax code (if any) or the customer’s tax code set up in DBIP and the operator will not be able to change it.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter CHAR.
2 Click on Enter Criteria then Execute Query to see which charge codes have been already set up.
3 Using your arrow keys, go through each record to see which charges have already been set up. If the charges that you need have already been set up, click on Exit to exit. There is no need to add any new charge codes to CHAR.
4 If the charges that you require have not been set up, click on Create Record.
5 Key in a code to describe the charge and press Enter. 
6 Key in a meaningful description for the new charge and press Enter.
7 If required, key in your reference information and press Enter to press Enter with this field blank to bypass this option.
8 Press Enter to bypass the External Reference field.
9 Key in your charge type and press Enter or use the pick list function to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
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
In this example, you are qualifying on pounds (0 --> 5,000 lbs. is the SKU type you are counting when you look up your per rate) and you are also charging by the pound (the rate for the 0 --> 5,000 weight break is 
.09 per lb.). Therefore, your “qualify on” SKU type is the same as your “charge on” SKU type. 
EXAMPLE 2
Suppose your rates are:
0 --> 5,000 lbs.
5001 --> 9,000 lbs.
9,001 --> 15,000 lbs.
.09 per CWT
.08 per CWT
.07 per CWT
In this example, you are qualifying on pounds as in the previous example, but you are charging by the hundredweight (CWT). Therefore, your “qualify on” SKU type is not the same as your “charge on” SKU type. To set up a charge code for this type of rating, you would enter CWT as your Charge on SKU Code and would enter your SKU code for pounds (set up in SKUS) as your Qualify on SKU Code.

11 Key in the general ledger code to which the revenues from this charge are to be posted and press Enter or use the pick list function to select it.
▪ If your codes have not been fully defined yet, use your miscellaneous account 999999.
▪ If you are using the GL modifier code feature, key in your account code using your wildcard characters (for example, **120000).
12 Key in your revenue analysis code and press Enter or use the pick list function to select it.
13 Key in your invoice type and press Enter or use the pick list function to select it.

Charge Code for blast freezing
14 Key in the SKU type that you wish to charge on and press Enter or use the pick list function to select it.
If you are setting up a charge code for fax services or taxes, use EA as your SKU type. If you are setting up an hourly based labor charge, use HR as your SKU type.
15 Key in the appropriate value for the Rounding Flag for your Charge on SKU type (U for Round Up, D for 
Round Down or N for No Rounding) and press Enter.
16 Key in the SKU type that you wish to qualify on and press Enter or use the pick list function to select it.
17 Key in the appropriate value for the Rounding Flag for your Qualify on SKU type and press Enter.
CAUTION In the majority of cases, your “Qualify on” SKU type will be the same as your “Charge on” SKU type. However, if you use CWT (hundredweight) or CKG (hundred kilo) as your Charge on SKU type, you must qualify on either pounds or kilos and enter the appropriate code for your unit of measure.

Charge Code screen showing Charge on and Qualify on SKU values
18 Press Enter to skip the remaining fields and enter RATE.
19 Go to next section of this manual for instructions on RATE (Depositor Billing Rates).

### Depositor Billing Rates (RATE) <a id="depositor-billing-rates-rate"></a>

OVERVIEW
In this program, you set up your rates — that is, the flat rate or linear charge, the number of weight breaks, any maximum and minimum charges and the effective date. The rates that you create in this program are 
PREREQUISITES: CHAR, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: This program is mandatory if you use AccellosOne 3PL for billing
OTHER REQUIREMENTS: A list of all your tariffs.

attached to the specific charge codes that you created in CHAR as well as to specific customers that you created in CUST. 
If you are setting up a rate that applies to all customers (for example, your published rates), you can use .ALL as your customer code. If you are setting up a customer-specific rate, you would enter the code for that customer in the Customer Code field in RATE.
You can enter your rates in RATE when you create your charge code in CHAR or you can set up your charge code in CHAR first and enter your rates at a later date. However, you must have a valid RATE record attached to your charge code before you can perform any transactions involving that charge code; for example, you cannot enter a receipt if the item that you are receiving is attached to a charge code with no RATE record.
This program is not used for “no charge” type charge codes.
FIELD DESCRIPTIONS
Customer Code (defined in CUST)
Mandatory
Enter .ALL for all customers or a specific customer code if the rate applies to a single customer.
Charge Code (CHAR) Set up in CHAR.
Charge Type Code Determined by the charge type that you selected in CHAR.
Charge Definition Determined by the charge definition that you selected in CHAR.
Effective Date Mandatory
If you use 01.01.01, you can bill for anything in the past. If you enter a future date in this field, rates will take effect on the date that you specify. Rates with an effective date in the future can be deleted in RATE.
Percentage Value Reserved for future use
Flat Rate Only available if Charge Definition set to F for Flat
Your flat rate for the charge code.
Number of Flat Rate 
Breaks
Only available if Charge Definition set to C for Combination
The number of flat rate breaks.

Number of Breaks Only available if Charge Definition set to B for Break or C for Combination
The total number of breaks both flat and linear.
Minimum Charge Only available if Charge Definition set to B for Break or C for Combination
Your minimum charge for the charge code.
Maximum Charge Only available if Charge Definition set to B for Break or C for Combination
Your maximum charge for the charge code.
Charge on SKU Code If you enter a SKU code in this field, it will override the charge on SKU in 
CHAR. What this override means is that the same charge code can be used twice with different charge on and qualify on values: once for customer A with a charge on and qualify on SKU of PLT and once for customer B with a charge on and qualify on SKU of CS. 
Round Flag The rounding rules for your override charge on SKU code.
Qualify on SKU Code See Charge on SKU Code field.
Round Flag See Charge on SKU Code field.
Exclude From Surcharge 
Calculations
N = No (default)
Y = Yes
If you set this flag to N for No, the charge will be included in any surcharge calculations set up in DBIP for a given customer unless you set up individual exclusions in the following four fields. 
If you set this flag to Y for Yes, the charge will NOT be included in any surcharge calculations set up in DBIP.
FIELD DESCRIPTIONS

PROCEDURE
1 If you are not already in RATE, enter RATE. If you accessed this program through CHAR, proceed to step 2.
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
Exclude From Accessorial Surcharge
Only available if Exclude From Surcharge Calculations = No
Same as above.
Exclude From Immediate 
Invoice Surcharge
Only available if Exclude From Surcharge Calculations = No
Same as above.
FIELD DESCRIPTIONS

Depositor Billing Rates
2 Key in the customer code that this charge or rate is to be applied to and press Enter. If the charge or rate applies to all customers, use .ALL as your customer code.
3 If you have accessed this program through CHAR, the charge code field will be filled in with the code that you created in CHAR. If you have accessed this program outside of CHAR, you must enter a charge code yourself. 
Key in your charge code and press Enter or select it using the pick list. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
4 Once the charge code has been entered, the charge type and charge definition fields will be automatically filled in and cannot be changed.
5 Key in your effective date (01.01.01 is recommended if you are setting up a new system) and press 
Enter.

Depositor Billing Rates for a charge type of Break
6 Proceed to enter your rates and your breaks according to the charge definition that you have selected:
7 Key in your non-flat or linear breaks.
If you selected Flat: If you selected Break:
a) In the Flat Rate field, key in the flat rate and press Enter.
b) In the Exclude from Surcharge 
Calculations field, key in Y for 
Yes or N for No and press 
Enter.
c) When the Breaks window appears, Click on Master 
Block to exit create mode. 
Then click on Return to Main and Exit to exit.
a) In the Number of Breaks field, key in the number of breaks and press Enter.
b) Key in your minimum and maximum charges or press 
Enter to accept the system defaults.
c) In the Exclude from Surcharge 
Calculations field, key in Y for 
Yes or N for No and press 
Enter.
d) Proceed to next step.

Depositor Billing Rates screen showing Breaks Block with four breaks
In the above example, for up to 499 lbs., the rate is $1.00 per CWT. For weights between 499 and 999 lbs., the rate is $0.90 and so on and so forth. If you set up the first two breaks as a flat rate (number of flat rate breaks = 2), the rate for up 499 lbs. would be a flat rate of $1.00 and the rate for up to 999 lbs. would be a flat rate of $0.90. 
8 Click on Master Block to exit create mode. Then click on Return to Main and Exit to exit.
COPYING RATES
You can copy individual depositor billing rates from one company/customer to another company/customer. 
When copying rates, the Use Current Effective Date of From Customer checkbox allows you to specify which effective date AccellosOne 3PL uses for the new rate: the current effective date of the from customer or the current system date. Old rates that are no longer effective are NOT copied.
EXAMPLE: Customer A, charge = BOL (Bill of Lading)
The following example shows five different effective dates belonging to the from customer: two rates in the past, one current rate and two rates in the future. 
FROM RATES
TO RATES - CHECKBOX 
UNCHECKED
TO RATES - CHECKBOX 
CHECKED
01-JAN Past rate Not copied Not copied
20-MAR Past rate Not copied Not copied
05-JUN Current rate June 20 June 5
Today = June 20

If you wish to copy all rates from one company to another regardless of customer, you can do so in COCO (Copy Codes Between Companies).
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
