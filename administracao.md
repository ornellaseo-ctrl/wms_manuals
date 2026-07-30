---
title: "Administração — Empresas, Usuários e Acessos"
description: "Código de empresa, operadores, papéis, restrições de acesso e verificações especiais."
layout: default
---

# Administração — Empresas, Usuários e Acessos

Código de empresa, operadores, papéis, restrições de acesso e verificações especiais.

**Fluxo principal:** `COMP/COAC (empresas) -> OPER/OPAC/OPRS/ROMA (usuarios) -> MSVS (special verify)`

> Fonte: manuais L do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction <a id="introduction"></a>

*Manual L — System Administration*

# Manual L — System Administration Guide (Administração do Sistema)
> **ID do Manual:** L  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Administração: company setup (COMP), programas (EXJO/JOSE), acesso de empresa (COAC), usuários (OPER/OPAC/OPRS), roles (ROMA), ActiveDesktop security (ADSA), archiving/purging (ARPU/DEAR), conversões de dados (DEPC/PRCO).
---

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting 
Introduction Guide logging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your company, working with menus and programs, basic queries, Signature Capture
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

SYSTEM ADMINISTRATION GUIDE 4.2* 3
SETTING UP COMPANIES, PROGRAMS 
AND USERS

## Setting Up Companies, Programs And Users <a id="setting-up-companies-programs-and-users"></a>

*Manual L — System Administration*

SYSTEM ADMINISTRATION GUIDE 4.2* 5

### Overview <a id="overview"></a>

There are three types of setup in AccellosOne 3PL:
 company setup
 program setup
 operator setup
Before you can use AccellosOne 3PL, you must be set up as an operator in OPER and your operator must have access to a company set up in COMP. The programs that you wish to use must be set up in JOSE and be accessible to the company in which you are working. Lastly, your operator must have access to the programs that you wish to use.
If any of these conditions has not been met (for example, your operator does not have access to a company, your operator does not have access to a program or the program does not have access to a company), you will not be able to enter the program.
EXAMPLE
An operator called BOB wants to enter a receipt in the program ENRE while working in company W1.
The following system flowchart shows the relationships between companies, operators and programs.
Bob has access to W1
ENRE accessible to W1
Bob has access to ENRE Result
Yes Yes No No access
Yes No Yes No access
No Yes Yes No access
Yes Yes Yes Access granted

Generally speaking, all system administration programs are in company Z1 (AccellosOne 3PL Utilities).

### Setting Up Your Company Code in COMP <a id="setting-up-your-company-code-in-comp"></a>

AccellosOne 3PL is divided into one or more companies. Customers, shippers, consignees, items and inventory available in one company may or may not be available in another company. Multiple companies are useful when you wish to:
 separate one business unit from another operating out of the same facility
 separate two facilities located in different cities belonging to the same business unit 
COMPANY SETUP
In these programs, you set up your company information.
COPA COMP
OPERATOR SETUP
In this program, you set up your operators.
OPER
PROGRAM SETUP
In these programs, you set up your application programs.
EXJO
JOSE
OPRS
COAC OPAC COOA
In COAC (Company Access), you assign programs to companies.
In OPAC (Operator Access) or
COOA (Copy Operator Access), you assign programs to operators.
In OPRS (Operator Restrictions), you restrict operators to companies.
COPA (Company Parameters)
EXJO (Executable Job Code)
JOSE (Job Selection Code)
or

SYSTEM ADMINISTRATION GUIDE 4.2* 7
 separate test data from live data
You set up your company codes in COMP (Company Code). In COMP, you define the following:
 the company’s name and address
 the company’s date format
 whether the company’s date defaults to the master date
 the company’s global code
 the company’s customer description
NOTE Any changes that you make to COMP do not take effect until the next time that you log onto AccellosOne 3PL.
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

ZIP/Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (ZIP/Postal Code), the city, state/province and country will be filled in by the system.
If the ZIP code or postal code that you enter is not in the system, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by first entering the country and the code and then defining the city plus state/province to which it belongs.
Date Format Mandatory
The date format for your company. You can choose from MM.DD.YY, 
DD.MM.YY or MON.DD.YY
Default to Master Date Y = Yes
N = No
If you select Yes, the company date of this company will automatically change when you change your company dates in ALDA (Change Date for All Companies).
If you select No, the company date of this company will not change when you change your company dates in ALDA. 
G.L. Modifier Code Optional
If you are using general ledger modifier codes to track revenue by company, enter the GL modifier code that you created in GLMO for this company.
FIELD DESCRIPTIONS

SYSTEM ADMINISTRATION GUIDE 4.2* 9
Global Code The value that you enter in the Global Code field determines whether or not global codes and profiles created in other companies will be available for use in your new company.
To share global programs across companies, you must set the Global Code field to the same value for all companies whose codes and profiles you wish to share. For example, if you assign the global code of 00 to companies W1 and 
W2 and assign the global code 01 to companies W3 and W4, companies W1 and W2 will share one set of global codes and profiles while companies W3 and W4 will share a separate set of global codes and profiles. AccellosOne 
3PL supports up to five global codes: 00, 01, 02, 03 and 04.
If you leave the Global Code field blank, the company is local — that is, any global profile is only available to the company in which the profile was set up. 
NOTE Once you set up a global code for a particular company, you cannot change it. Should you make a mistake and need to delete or modify the global code, contact your HighJump consultant for assistance.
Printer Code Mandatory
The default printer to be used throughout the company for documents. 
Rollup Type N = Not Applicable
C = Child
R = Rollup
See “Rollup Invoicing” in the Billing and Invoicing Guide.
External Reference Number
Optional
An external reference number to be used where required.
Company Reference 
Code
Optional
An external reference number to be used where required.
FIELD DESCRIPTIONS

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
11 If you are using general ledger modifier codes to track revenue by company, key in your general ledger modifier code for this company and press Enter. If you are not using general ledger modifier codes to track revenue by company, leave this field blank.
Auto-Process Sequence 
Number
Optional
This field allows you to sequence the printing of auto-printed documents by company. For example, if you set company W1 to 1 and company W2 to 5, 
W1’s auto-printed documents will be printed before W2’s auto-printed documents.
FIELD DESCRIPTIONS

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

### SETTING UP YOUR COMPANY PARAMETERS <a id="setting-up-your-company-parameters"></a>

You open the Company Parameters window by clicking on Company Parameters.
If you wish to share global codes and profiles with another company:
If you do NOT wish to share global codes and profiles:
a) Key in your global code and press Enter.
a) Press Enter to bypass the Global 
Code field.

COMP screen showing Outbound tab
FIELD DESCRIPTIONS (OUTBOUND)
Activate Back Orders Yes
No
If you select Yes, the back order system is active and you can enter a value in the Back Orders at Level Number field in ITSH (Item Shipping 
Profile). If you select No, the back order system is deactivated.
Allow P-Type Lines in 
Order Entry
Yes
No
If you select Yes, you can enter P-type order lines in ENOR.
If you select No, you cannot enter P-type order lines in ENOR.

SYSTEM ADMINISTRATION GUIDE 4.2* 13
Allow Multiple Warehouses on Order Confirmation
Single
Multiple
If you select Single and you are shipping product from multiple warehouses, you cannot confirm the order in CHOF (Time Stamp and Confirm Orders). 
Instead, you must confirm individual order lines in COOL (Confirm Orders - 
Line at a Time).
If you select Multiple and you are shipping product from multiple warehouses, the above restriction does not apply. You can confirm such orders in CHOF (Time Stamp and Confirm Orders) and are not forced to confirm each order line individually in COOL.
Generate Order Alerts None
Ship
Order
Both
If you select None, no order alerts will be generated.
If you select Ship, an order alert will be generated whenever the shipped quantity is greater than the ordered quantity. If you select Order, an order alert will be generated whenever the ordered quantity is greater than the shipped quantity.
If you select Both, an order alert will be generated whenever the shipped quantity and ordered quantity do not match.
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
will update the carrier entered in ENOR. If you select No, the carrier code that you enter in VBOL will NOT update the carrier entered in ENOR.
FIELD DESCRIPTIONS (OUTBOUND)

COMP screen showing Financial tab
FIELD DESCRIPTIONS (FINANCIAL)
Number of Fiscal Periods Reserved for future use.
Use Multiple Currencies See the Billing and Invoicing Guide.
Home Currency Code (CURR)
See the Billing and Invoicing Guide.
Financial Interface Code The financial interface code used to link AccellosOne 3PL to your accounting system. This field must be set up by HighJump.

SYSTEM ADMINISTRATION GUIDE 4.2* 15
Verify Customer’s Credit 
Status
Only available if you use the cash posting system to track payments received from customers
Yes
No
If you set this field to Yes and enter a credit limit amount in DBIP for a given customer, you will not be able to create a new order for that customer in 
ENOR when the outstanding invoices for that customer exceed the customer’s credit limit.
If you set this field to No, credit status checking will be deactivated.
Number of Decimal 
Places for Billing Calculations
The number of decimal places for all database columns in AccellosOne 3PL relating to charges, invoice amounts and taxes. You can choose any value between two and six decimal places in this field.
For example, if you set the Charge Number of Decimal Places to ‘4’ and the calculated charge amount is 100.123456, the charge amount being stored in the database will become 100.123500. If you set the Charge Number of Decimal Places to ‘2’, this charge amount will become 100.120000.
Regardless of the option that you choose, invoice amounts that print on invoices will show only two decimal places.
Department Entry for 
Charges
None
Allow
Require
If you select Allow, you can assign a department code to a manual charge in 
ENAC. If you select Require, you must assign a department code to a manual charge in ENAC.
Process Billing Batch (BILB) Automatically
See the Billing and Invoicing Guide.
FIELD DESCRIPTIONS (FINANCIAL)

COMP screen showing Transport tab
FIELD DESCRIPTIONS (TRANSPORT)
Freight Terminal Code (TERL)
Your freight terminal code for 3PL-TMS integration. 
Activate Freight Reserved for future use.
Activate TMS Yes
No
If you set this flag to Yes, 3PL -TMS integration will be activated. If you set this flag to No, 3PL-TMS integration will not be activated.
Freight Interface Profile 
Code (FIPR)
Your freight interface profile code for 3PL-TMS integration.
External Freight Interface Profile Code (FIPR)Your freight interface profile code for an external non 3PL-TMS integration.
Parcel Interface Profile 
Code (FIPR)
Your freight interface profile code for an external parcel processing system.
Ignore Freight Version For HighJump use only.

SYSTEM ADMINISTRATION GUIDE 4.2* 17
COMP screen showing Allocation tab
FIELD DESCRIPTIONS (ALLOCATION)
Activate Directed PutAwayYes
No
If you select Yes, you can perform directed put-away. If you select No, directed put-away will be deactivated and you will have to assign locations to receipts manually. When you select the No option and bypass the Location field in 
ENRE, the Location Block will appear to remind you to enter a location.
Activate Directed Move 
Inbound
Yes
No
If you select Yes, you can perform directed moves in RFCH (RF Check/
Unload) and RFPU (RF Put-Away). If you select No, directed moves in RFCH and RFPU will be deactivated and you will have to assign locations to receipts manually.

Activate Directed Move 
Stock
Yes
No
If you select Yes, you can perform directed moves in DMPR (Directed Move 
Processing). If you select No, directed moves in DMPR will be deactivated and you will have to assign locations to receipts manually.
Allow Replenishment from Pick Line Location 
Type
Yes
No
If you select Yes, you can pick product from a staging location in RFPIC. If you select No, you cannot pick product from a staging location in RFPIC.
Activate Location Size Yes
No
If you select Yes, location size logic is activated for directed put-away. If you select No, location size logic is deactivated for directed put-away. 
Activate Weight Capacity Yes
No
If you select Yes, the put-away by weight options in ILOP are activated for directed put-away. If you select No, the put-away by weight options in ILOP are deactivated.
Activate Cube Capacity Yes
No
If you select Yes, the put-away by cube options in ILOP are activated for directed put-away. If you select No, the put-away by cube options in ILOP are deactivated.
Print Sequence Code for 
Auto-Printed Documents
PRI
MRPI
PSDT
PROM
PRI sorts documents to print by priority only. MRPI adds 10 days to the to ship date if to ship date is in the future. It adds 2 days if to ship date is current. It doesn’t add any days if to ship date has passed. Then the system prints according to the new modified ship date. PSDT sorts documents by order priority, to ship date and order number. PROM sorts by order entry. 
FIELD DESCRIPTIONS (ALLOCATION)

SYSTEM ADMINISTRATION GUIDE 4.2* 19
Assign Location Based on Header/Document 
Flow
Header
Document
If you set this field to Header (the default value), allocation will be triggered and locations assigned whenever an inbound or outbound document is assigned to a flow in DIFP in which the Assign Location flag is set to Y for Yes.
If you set this field to Document, allocation will only be triggered if the Print 
Document Without Assigning Location field in DOCU is not Y for Yes for the inbound or outbound document.
This option is useful when more than one document is attached to a flow and not all documents should trigger allocation. For example, suppose you have two documents attached to the STPI (Start Picking) flow:
document 1 = Print Document Without Assigning Location field in DOCU set to Y for Yes document 2 = Print Document Without Assigning Location field in DOCU set to N for No
Document 1 will print but no allocation will occur and locations will not be assigned. Then document 2 will print, allocation will run and pick locations for the order lines will be assigned in the normal manner.
Activate Consolidation of 
R-Type Location Lines
Yes
No
If you set this flag to Yes, allocation will automatically consolidate location lines for R-type orders when the location and inventory entity are the same. 
For example, suppose you have three location lines for the same inventory in the same location:
Line Number Location Inventory Entity Quantity
1 A100 A1/101 10C
2 A100 A1/101 25C
3 A100 A1/101 15C
If you set this flag to Yes, AccellosOne 3PL will consolidate the three lines into one line for location A100 with a quantity of 50 cases. If you set this flag to No, 
AccellosOne 3PL will NOT consolidate the three lines into one. 
FIELD DESCRIPTIONS (ALLOCATION)

COMP screen showing Manual Accounts tab
Limit Pick Line to 
Assigned Carriers Only
Yes
No
If you set this flag to Yes, pick line locations will be limited to assigned carriers only. If you set this flag to No, pick line locations will be available to all carriers. 
In PIPA (Allocation Pick Line for Parcel Carrier), you specify which SKU codes can be picked from the pick line for the assigned carriers.
NOTE The Yes option does not support FIFO/LIFO rules. Orders for nonselected carriers will never be allocated to the pick line even if the oldest product is in a pick line location.
Enable Pallet Attribute in 
LOTP
Yes
No
If you set this flag to Yes, you can put-away product by inventory attribute such as pallet size or pallet type rather than SKU quantity, weight or cube. For example, you receive both standard four-foot pallets as well seven-foot pallets in your warehouse and you need a way to assign your different pallet types to a location with sufficient capacity.
If you set this flag to No, put-away by inventory attribute will be deactivated.
FIELD DESCRIPTIONS (ALLOCATION)

SYSTEM ADMINISTRATION GUIDE 4.2* 21
FIELD DESCRIPTIONS (MANUAL ACCOUNT)
Allow Manual ConsigneesYes
No
If you select Yes, you can enter manual consignees in ENOR. If you select No, you cannot enter manual consignees in ENOR. 
A manual consignee is a consignee that is not set up in CONS (Consignees). 
You enter a manual consignee by keying in a forward slash (/) in the Consignee Code field of ENOR. Then you key in the name of your manual consignee in the Name field.
Allow Manual Shippers Yes
No
If you select Yes, you can enter manual shippers in ENRE. If you select No, you cannot enter manual shippers in ENRE. A manual shipper is a shipper that is not set up in SHIP (Shippers). 
You enter a manual shipper by keying in a forward slash (/) in the Shipper 
Code field of ENRE. Then you key in the name of your manual shipper in the 
Name field.
Allow Manual Carriers Yes
No
If you select Yes, you can enter manual carriers in ENRE and
ENOR. If you select No, you cannot enter manual carriers in
ENRE or ENOR. 
A manual carrier is a carrier that is not set up in CARR (Carriers). You enter a manual carrier by keying in a forward slash (/) in the Carrier Code field of 
ENRE or ENOR. Then you key in the name of your manual carrier in the 
Name field.
Allow Manual Sold-To’s Yes
No
If you select Yes, you can enter manual sold-to’s in ENOR. If you select No, you cannot enter manual sold-to’s in ENOR.
A manual sold-to is a sold-to that is not set up in SOLD (Sold-To Codes). You enter a manual sold-to by keying in a forward slash (/) in the Sold To Code field of ENOR. Then you key in the name of your manual sold-to in the Name field.

COMP screen showing Miscellaneous tab
FIELD DESCRIPTIONS (MISCELLANEOUS)
Allow Multiple Warehouses on Receipt Confirmation
Single
Multiple
If you select Single, multiple warehouses are not allowed on the same receipt; 
that is, you cannot put-away product on the same receipt in multiple warehouses. If you select Multiple, there is no restriction on the number of warehouses on a receipt.
Force Audit of Accessorial ChargesYes
No
If you set this field to Yes, you can force manual charges to be authorized before they can be placed on a batch and invoiced. If you set this field to No, you cannot force manual charges to be authorized.

SYSTEM ADMINISTRATION GUIDE 4.2* 23
Allow Override of Adjustment DateYes
No
If you set this field to Yes, users can override the adjustment date field in 
ENAJ. If you set this field to No, users cannot override the adjustment date in 
ENAJ.
Activate Pallet RestrictionsSee “PALLET CONTROL” in the Operations 2 Guide. 
Warehouse Code 
Optional for Invoicing by 
Warehouse
See “Invoicing by Warehouse” in the Billing and Invoicing Guide.
Warehouse Code mandatory for Invoicing by 
Warehouse
See “Invoicing by Warehouse” in the Billing and Invoicing Guide.
Use Line-by-Line Formatting for Remarks BlockYes
No
Extended
If you set this field to Yes, remarks that you enter in ENRE, ENOR, ENAJ, 
RELO and other programs require a line number and each line can hold up to 
40 characters. If you set this field to No, remarks that you enter in ENRE, 
ENOR, ENAJ, RELO and other programs do not require a line number and automatically wrap to the next line.
If you set this field to Extended, the following screen will display in the 
Remarks Block of ENRE/ENOR:
Extended Remarks screen
See the Operations 1 Guide for further information on extended remarks.
FIELD DESCRIPTIONS (MISCELLANEOUS)

RF Java Executable For HighJump use only.
Restrict Relocations to 
Same Warehouse
Yes
No
If you set this field to Yes, you cannot relocate inventory in RFRL (RF Relocate) from one warehouse to another. If you set this field to No, there are no restrictions on inter-warehouse moves and you can relocated product in RFRL from one warehouse to another.
Activate Background 
Printing
Yes
No
This flag applies to the following programs: PRRM (Print Receiving Documents - Specific), PROM (Print Shipping Documents - Specific), PROR (Print 
Shipping Documents - All) and PRRE (Print Receiving Documents - All).
When you activate this flag and print to a warehouse printer, SPL, FAX or 
MAIL, AccellosOne 3PL will execute the printing in the background. This will eliminate the delay on the screen and will allow you to continue working on your next task. However, any orders or receipts being printed in PRRE, 
PRRM, PROR and PROM will remain locked until printing is complete.
NOTE Background printing is not available for the VIEW printer (Adobe 
Acrobat).
Carrier Owns Transport 
Equipment Equipment/
Container
Yes
No
Whether or not the carrier owns the transport equipment/container or whether carrier leases the transport equipment/container from another company.
4PL Type For HighJump use only.
4PL Freight Update is 
Active
For HighJump use only.
FIELD DESCRIPTIONS (MISCELLANEOUS)

SYSTEM ADMINISTRATION GUIDE 4.2* 25
COMP screen showing Miscellaneous 2 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 2)
Pallet Code (PALL) This field allows you to add the weight of the pallet itself (that is, the block of wood on which the pallet contents rests) to a bill of lading or other outbound documents. It can also be used by EDI if required.
Customization by HighJump may be required.
Warehouse Required Yes
No
If you set this field to Yes, the user is required to enter a warehouse code in the Header Block of ENRE/ENOR. If you set this field to No, the entry of a warehouse code in the Header Block of ENRE/ENOR is not mandatory.
Default Receipt Type in 
ENRE
You can define a default receipt type (Post-receiving, No Charge, Handling, etc.) for ENRE in this field.

Only Display Customer 
Charges
Yes
No
If you select Yes, the pick list of charges in ENAC and ENIN will show only charges attached to the customer in RATE. That is, a charge attached to customer A in RATE cannot be applied to customer B. As well, a charge attached to the .ALL customer cannot be applied to either customer A or customer B.
If you select No, the pick list of charges in ENAC and ENIN will show all charges regardless of customer.
Allow Update to Charge 
Quantity and SKU
Yes
No
If you select Yes, the user can update the charge quantity and SKU in ENAC and ENIN. If you select No, the charge quantity and SKU in ENAC and ENIN are not editable fields.
Enable Reason Codes in 
ENRE/ENOR
Yes
No
If you select Yes, the user can attach a reason code to a receipt/order line in 
ENRE/ENOR. Reason codes, which are maintained in REAS, are used to flag exceptional conditions such as “wrong quantity”. 
Enable Equipment Tracking in RFYes
No
If you select Yes, equipment tracking is enabled. Each time that an RF operator logs onto RF, he or she will be required to enter a valid equipment type code.
Enable Task Generation for Interleaving
Yes
No
If you select Yes, task interleaving will be enabled in RFITLV.
Enable A1 Schedule IntegrationYes
No
If you select Yes, 3PL appointments can be set up and maintained in A1 
Schedule.
FIELD DESCRIPTIONS (MISCELLANEOUS 2)

SYSTEM ADMINISTRATION GUIDE 4.2* 27
External Labor System Yes
No
If you select Yes, AccellosOne 3PL will be integrated with West Monroe’s 
FLEXdls labor management software.
Single Pallet Per Order 
Line Flag
Yes
No
If you select Yes, an order line containing two or more pallets in the same location will be split into two or more pick assignments. For example, if the order line quantity is two pallets and both pallets are in the same location, 
AccellosOne 3PL will create two pick assignments, each for a single pallet. 
The Yes option may be required because of equipment restrictions.
If you select No, an order line containing two or more pallets in the same location will NOT be split into two or more pick assignments.
Validate Ship Date When 
Entering Appointment
Yes
No
If you set this flag to Yes, the user cannot enter a start date for an appointment in APPL that is greater than the order/load’s to ship date. If you set this flag to 
No, there is no validation in APPL that the appointment’s start date is less than or equal to the order/load’s to ship date.
FIELD DESCRIPTIONS (MISCELLANEOUS 2)

COMP screen showing Miscellaneous 3 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 3)
Prompt User to Run 
RESW When Changing 
Weight in ITEM
Yes
No
If you set this flag to Yes, the user will be prompted to run RESW if he or she changes the standard weight in ITEM.
Minimum Number of 
Months to Retain Data
See [ARCHIVING AND PURGING](administracao-manutencao.html#archiving-and-purging).
Allow Multiple Archive/
Purge Selections
See [ARCHIVING AND PURGING](administracao-manutencao.html#archiving-and-purging).

SYSTEM ADMINISTRATION GUIDE 4.2* 29
Special Sorting Process 
Type (RFSC)
Enter OPID from, select an order if more than one order in OPID
If you select “Enter OPID from, select an order if more than one order in 
OPID”, you will be prompted to enter the OPID in RFSC. If you leave this field blank, you will be prompted to enter the order number in RFSC.
Update Carrier Code on 
Orders/Receipts from 
Appointment
Yes
No
If you set this flag to Yes and the carrier attached to the appointment in APPL does not match the carrier attached to the order/receipt, AccellosOne 3PL will update the order/receipt carrier to match the appointment’s carrier. 
Update Load Type Code on Orders/Receipts from 
Appointment
Yes
No
If you set this flag to Yes and the load type attached to the appointment in 
APPL does not match the load type attached to the order/receipt, AccellosOne 
3PL will update the order/receipt load type to match the appointment’s load type. 
Allow Emails to be Generated Upon Batch Confirmation
Yes
No
If you set this flag to Yes and create a valid record in AECS (Automatic Email 
Setup), you can email confirmed invoices to customers in BILB (Billing Batch). 
If you set this flag to No, emailing of confirmed invoices to customers in BILB will be deactivated.
Enable RF Image Capture
Only available for Intermec CK71 ITE devices
Yes
No
If you set this flag to Yes, RF image capture will be activated. If you set this flag to No, RF image capture will be deactivated.
Enable Order Cancellation in ENORYes
No
If you set this flag to Yes and delete an order in ENOR, you will be prompted to either delete or cancel the order. If you select the Cancel option, your selection will be saved in the order header in a field used by EDI that is not accessible in LOOR. 
FIELD DESCRIPTIONS (MISCELLANEOUS 3)

Allow Skipping of From 
Warehouse in RFPIC
Yes
No
If you set this flag to Yes, you can bypass the WHSE field in RFPIC and enter your order directly. If you set this flag to No, the WHSE field is mandatory and cannot be bypassed.
Reason Code Required for Appointments
Reserved for future use.
Enable OPID Mixed Item 
Rule by Warehouse
Yes
No
In this field, you set up your default rule for mixing items on the same OPID. 
This rule defines whether or not you can mix different items on the same OPID when performing case picking (RFPIC, RFPK, RFITLV), pallet building and 
OPID merging (RFMG).
This flag is a default only. You can override it in both CCCC and WCCO.
FIELD DESCRIPTIONS (MISCELLANEOUS 3)

SYSTEM ADMINISTRATION GUIDE 4.2* 31
COMP screen showing Miscellaneous 4 tab
FIELD DESCRIPTIONS (MISCELLANEOUS 4)
Wave Pick Method 
Assignment Type
Enable Pick Method Generation
Enable Pick Method Generation, suppress LABP pick method
See your HighJump implementation consultant for further information on this field.
Skip Order Entry in RFOA Yes
No
If you set this flag to Yes, you can skip the ORDE field in RFOA and enter your 
OPID directly. If you set this flag to No, the ORDE field in RFOA is mandatory and cannot be skipped.

Event Cycle Count Limited by Warehouse CodeYes
No
If you set this flag to Yes, any event-driven cycle counts generated by a variance will be limited to the warehouse in which the variance occurred. If you set this flag to No, any event-driven cycle counts generated by a variance will apply to all warehouses.
Minimum Number of 
Days to Retain OPID
The minimum number of days to retain OPID’s. If you leave this field blank, you will not be able to reuse OPID’s in RFMG. If you enter a value in this field (say, 30 days), duplicate OPID’s will be allowed in RFMG after 30 days.
Default Receipt Line Type in ENRE
You can define a default line type in ENRE by entering the line type (P, U, etc.) 
in this field.
Hide Quantity in RFPR Yes
No
If you set this flag to Yes, the quantity fields in RFPR (RF Product Look-Up by 
Location) will be suppressed for non-supervisory users. If you set this flag to 
No, the quantity fields in RFPR will display for all users both supervisory and non-supervisory.
Suspend Picking Tasks 
Upon Wave Execution
See the “Building Pallets in PABU” section in the RF Guide for further information.
RFRP Requery Type Requery Scrolling in Pick List and Upon REPI Completion
Requery Upon REPI Completion
In this field, you specify your requery rules for RFRP. A requery occurs when you select a record in RFRP using your arrow keys, confirm the replenishment of that record and then query for a second record to confirm.
If you select “Requery Scrolling in Pick List and Upon REPI Completion”, the list of available replenishments in RFRP will display the full list starting with the first record when you perform a requery. If you select “Requery Upon REPI 
Completion”, the list of available replenishments in RFRP will display the full list starting with the record before the last record that you selected; to see records before that record, you must use your arrow keys to scroll to the beginning of the list.
RFITLV First Check 
Same Location for Task
See the “Task Interleaving” section in the RF Guide for further information.
RFITLV Second Check 
Same Aisle for Task
See the “Task Interleaving” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

SYSTEM ADMINISTRATION GUIDE 4.2* 33
COMP screen showing Miscellaneous 5 tab
RFITLV Third Check 
Same Zone for Task
See the “Task Interleaving” section in the RF Guide for further information.
Supervisor Notification 
Group Email Address
See the “Supervisor Notification” section in the RF Guide.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)
Ignore CCOR Validation in ICOC
No
Yes
If you set this flag to Yes, you can access ICOC even if the Use Consignee 
Item Configuration flag in CCOR is set to No. If you set this flag to No, you can only access ICOC if the Use Consignee Item Configuration flag in CCOR is set to Yes.
FIELD DESCRIPTIONS (MISCELLANEOUS 4)

Consignee Subscribed to 
Interface Processing Only
No
Yes
This field is only used if your consignees are set up and maintained in another system such as ERP software and imported into AccellosOne 3PL.
If you set this flag to Yes, you cannot create and delete consignees in CONS nor can you modify the consignee’s address. If you set this flag to No, normal create, delete and modify functions are available in CONS.
Customer Subscribed to 
Interface Processing Only
No
Yes
This field is only used if your customers are set up and maintained in another system such as ERP software and imported into AccellosOne 3PL.
If you set this flag to Yes, you cannot create and delete customers in CUST nor can you modify the customer’s address. If you set this flag to No, normal create, delete and modify functions are available in CUST.
Use Pallet Pick Method for Last Entity
Yes
No
In this field, you define the pick method for non-pick line locations when the order line does not have any pick method assigned to it by the Wave Manager.
If you set this flag to Yes, if the Wave Pick Method Assignment Type parameter in COMP is not blank and if the order line quantity equals the on-hand quantity of the entity in the location, the PALL pick method will be assigned to the order line.
If you set this flag to No and if the order line quantity is greater than or equal to a full pallet, the PALL pick method will be assigned to the order line.
Default Load Status Created by Freight Interface 1 Create
2 Ready to Load
In this field, you define the default load status when creating outbound loads for a TMS system or EDI.
Use Assignment Parameter Tables for Pallet BuildSee the “Building Pallets in PABU” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

SYSTEM ADMINISTRATION GUIDE 4.2* 35

### Setting Up Your Programs in EXJO, JOSE <a id="setting-up-your-programs-in-exjo-jose"></a>

There are two setup programs in AccellosOne 3PL for application programs:
 EXJO (Executable Job Code)
 JOSE (Job Selection Code)
The executable job code is the actual program name of a given program. The job selection code, on the other hand, is the code that the user types in to access the program. For example, the executable job code for the Enter Receipts program is rp_101 while the job selection code for the same program is ENRE (Enter Receipt).
Executable job codes are set up by HighJump and cannot be modified by system administrators. Job selection codes, on the other hand, can be user-defined by system administrators to meet company or language requirements.
There are two steps to follow in setting up a new program: first you set up your executable job code in EXJO and second you attach your executable job code to your job selection code in JOSE.
Location Capacity Validation TypeNo validation for user-initiated transactions (1)
Validate location capacity and generate warning message (2)
Validate location capacity and do not allow operator to continue (3)
If you select 1, no validation of location capacity will be performed for user-initiated transactions in ENRE, RELO, RFCH, RFPU and RFRL.
If you select 2, AccellosOne Enterprise 3PL will validate the location capacity for user-initiated transactions. If the location capacity is exceeded, the system will generate a warning message; as well, if the violation occurs in an RF program, an event-driven cycle count will be generated.
If you select 3, AccellosOne Enterprise 3PL will validate the location capacity for user-initiated transactions. If the location capacity is exceeded, the operator will not be allowed to proceed; as well, if the violation occurs in an RF program, an event-driven cycle count will be generated. 
RF Special Character See the “General Setup” section in the RF Guide for further information.
Set Default Values in RF 
Pallet Screen
See the “General Setup” section in the RF Guide for further information.
FIELD DESCRIPTIONS (MISCELLANEOUS 5)

### SETTING UP YOUR EXECUTABLE JOB CODES IN EXJO <a id="setting-up-your-executable-job-codes-in-exjo"></a>

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
If you select R for Report, the word “Report” will appear beside the program name and description when you view the submenu to which the program is attached. 
If you select N for None, the program name and description only will appear when you view the submenu to which the program is attached.
EXJO JOSE job code = rp_101 rp_101 = ENRE

SYSTEM ADMINISTRATION GUIDE 4.2* 37

### LOCK BLOCK <a id="lock-block"></a>

The Lock Block allows you to apply locks to programs. There are two kinds of program locks in AccellosOne 
3PL: 
 there are exclusive locks that allow you to restrict access to a program to a single user at any one time (for example, if operator A is using ENRE, no other operator can enter this program until operator A exits)
 there are conditional locks that allow you to lock one program when another program is being used (for example, if program A is running, program B is locked and cannot be accessed by any user until program A has finished)
You can combine both kinds of locks in EXJO for the same program. For example, you apply an exclusive lock to PHUP (Physical to Inventory Update) so that only one user can access this program at any given time. 
Then you apply a conditional lock to ENTI (Enter Tickets) so that no user — including the user working in 
PHUP — can enter tickets in ENTI for a physical while PHUP is running. 
Query Job Y = Yes
N = No
If you select Y for Yes, the program will appear on the Hot Query Selection menu. If you select N for No, the program will NOT appear on the Hot Query 
Selection menu.
Hot Queries allow you to enter a second program to look up information without closing the program that you are currently working in. For example, if you are entering a receipt in ENRE and receive a telephone call about a specific order, you can look up the order in LOOR without closing ENRE.
External Executable Reserved for future use.
NOTE Locks apply to the active company only. If you set up an exclusive lock for 
ENTI and are working in ENTI in company W1, no other operator in W1 will be able to access the program. However, a second operator working in company W2 will be able to access ENTI as well as a third operator working in company W3.
FIELD DESCRIPTIONS
Job Name The job name or names that you wish to lock. If you are setting up an exclusive lock, the job name in the Lock Block will be the same as the job name in the Header Block. If you are setting up a conditional lock, the job name in the 
Lock Block will not match the job name in the Header Block.
FIELD DESCRIPTIONS

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
If you select Y for Yes, the record is correct and you wish to accept it. If you select N for No, the record is not correct and you can change it.
FIELD DESCRIPTIONS

SYSTEM ADMINISTRATION GUIDE 4.2* 39
10 In the Lock Block, do one of the following.

Executable Job Code (EXJO) screen showing two locks: an exclusive lock (pi_105) and a conditional lock (pi_101)
11 When you finish setting up your executable job code, click on Return to Main and Master Block. Then click on Exit to exit.

### SETTING UP YOUR JOB SELECTION CODES IN JOSE <a id="setting-up-your-job-selection-codes-in-jose"></a>

In JOSE you attach the executable job code previously set up in EXJO to your job selection code. You define the following parameters in JOSE:
 the job selection code for the program
 the submenu to which the job selection code is attached
 the program’s position on the submenu
 the program’s executable job code
If you wish to set up locks for the program:
If you do NOT wish to set up locks for the program:
a) Click on Create Record.
b) Key in your job name and press 
Enter.
c) In the Correct field, press Enter to accept the value of Yes.
d) Repeat the above steps for each additional program that you wish to lock.
a) Proceed to step 10.

If required, you can attach multiple job selection codes to the same executable job.
FIELD DESCRIPTIONS
Selection Code Mandatory
The program’s job selection code. Job selection codes can consist of any combination of letters between four and six characters in length. 
Description Mandatory
A meaningful description for the job selection code.
Subsystem Code (JOSE) Mandatory
The submenu to which the program is attached.
Sort Sequence The program’s position on the submenu. For example, if you enter 5 for the program ENRE, ENRE will be the fifth program shown on the submenu RECE.
Executable Job Code (EXJO)
Optional
The program’s executable job code.
Help File For HighJump use only
Print Job N = No
R = Report
If the executable job code is defined as a report in EXJO, this field will automatically be set to R for Report. If the executable job code is not defined as a report in EXJO, this field will automatically be set to N for No. 
Form Code (FORM) Only available if the executable job is a standard report
The report’s paper size and orientation.
ISO Reference Code Only available if the executable job is a report
If you enter ISO reference information in this field, it will print in the bottom right-hand corner of each page of the report.

SYSTEM ADMINISTRATION GUIDE 4.2* 41
1 Enter JOSE.
2 Click on Create Record. 
3 Key in your job selection code and press Enter.
4 Key in a meaningful description for your job selection code and press Enter.
5 In the Subsystem Code field, key in the submenu to which the job selection is to be attached and press 
Enter or use your pick list to select the appropriate submenu.
6 Key in your sort sequence number and press Enter.
7 In the Executable Job Code field, key in your executable job code and press Enter or use your pick list to select the appropriate code.
8 Press Enter to bypass the Help File field.
9 If the executable job code that you entered in the previous field is defined as a report in EXJO, key in your form code in the Form Code field and press Enter or use your pick list to select it. Then press Enter in the Re-Align Forms Message field to accept the value of N for No.
10 If the executable job code that you entered in the Executable Job Code field is defined as a report in 
EXJO, you can enter an ISO reference code. If you do not require an ISO reference code, press Enter to bypass this field.

Job Selection Code (JOSE)
11 When you finish setting up your job selection code, click on Return to Main and Exit to exit.

### SETTING UP SUBMENUS IN JOSE <a id="setting-up-submenus-in-jose"></a>

The menu tree consists of two types of codes: job selection codes and submenus. A job selection code is a regular AccellosOne 3PL program that you use to look up information or to create or modify data. 
Re-Align Forms Message Reserved for future use.
FIELD DESCRIPTIONS

Job selection codes are always attached to submenus. A submenu, on the other hand, is merely a folder or directory used to group a number of similar programs under a single, meaningful name. For example, ITRE is a submenu used to group all item-related programs.
AccellosOne 3PL allows you to create your own submenus using your own terminology and attach these customized submenus to other submenus; in this way, you can create a completely customized menu structure. You set up a submenu in JOSE by creating a new job selection code. Unlike programs, submenus do not have executable job codes attached to them. 
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
NOTE Once you have created a new submenu, you must give your company access to it in COAC (Company Access) and your operators access to it in OPAC (Operator Access).

SYSTEM ADMINISTRATION GUIDE 4.2* 43

Job Selection Code (JOSE) screen showing the submenu RECE
10 Click on Exit to exit.

### DELETING A SUBMENU <a id="deleting-a-submenu"></a>

Before you can delete a submenu, you must remove any dependent selections. A dependent selection is a program or submenu that is attached to the submenu that you wish to delete.
1 If the submenu has dependent selections, you must remove them in JOSE. You remove dependent selections by retrieving the program or submenu in JOSE and deleting it.
2 Enter JOSE.
3 Click on Enter Criteria.
4 Press Enter to position your cursor in the Selection Code field.
5 Key in the code of the submenu that you wish to delete and click on Query.
6 When the record is retrieved, press Enter twice to position your cursor in the Description field.
7 Click on Delete.
8 Click on Exit to exit.

### LOOKING UP A PROGRAM’S PATH <a id="looking-up-a-program-s-path"></a>

You look up a program’s path in JOSE by performing a query on the job selection code. When the appropriate record is retrieved from the database, you note the selection code’s subsystem code and then perform a second query — this time entering the subsystem code in the Selection Code field. You continue to work back up from the first or lowest subsystem code, to the second or next higher subsystem code, to the third or next higher subsystem code until you reach MAIN or RFMN (for RF programs).
For example, if you wished to look up the path of CORL (Confirm Receipts - Line at a time), you would do the following.
1 Enter JOSE.

2 Click on Enter Criteria.
3 Press Enter to position your cursor in the Selection Code field.
4 Key in CORL and click on Execute Query.

Job Selection Code (JOSE) screen showing RECE as the subsystem code for CORL
5 Your first subsystem code for CORL is RECE (Receiving). You are now ready to query on RECE.
6 Click on Enter Criteria.
7 Press Enter to position your cursor in the Selection Code field.
8 Key in RECE and click on Execute Query.

Job Selection Code (JOSE) screen showing WO as the subsystem code for RECE

SYSTEM ADMINISTRATION GUIDE 4.2* 45
9 Your second subsystem code for CORL is WO (Warehouse Operations). You are now ready to query on 
WO.
10 Click on Enter Criteria.
11 Press Enter to position your cursor in the Selection Code field.
12 Key in WO and click on Execute Query.

Job Selection Code (JOSE) screen showing MAIN as the subsystem code for WO
13 Your third and final subsystem code for CORL is MAIN (Main Menu). You now know the complete path of 
CORL: MAIN\ WO\RECE\CORL.

### LOOKING UP A PROGRAM’S EXECUTABLE JOB CODE <a id="looking-up-a-program-s-executable-job-code"></a>

You look up the executable job code for a program by performing a query in JOSE on the job selection code.
1 Enter JOSE.
2 Click on Enter Criteria.
3 Press Enter to position your cursor in Selection Code field.
4 Key in the job selection code that you are querying on and click on Query.

Job Selection Code (JOSE) screen showing rp_101 as the executable job for ENRE
5 Click on Exit to exit.

### Assigning Programs to Companies in COAC <a id="assigning-programs-to-companies-in-coac"></a>

You give companies access to programs and submenus in COAC (Company Access). Company access means that a given program or submenu appears on your screen when you are working in that company. It is not the same as operator access set up in OPAC, which allows you to look up information, run reports and enter data. In order to use a given program, you need both company access and operator access. 
For example, in order for operator A to use ENRE (Enter Receipts) in W1, you must give W1 access to ENRE and you must give operator A access to ENRE. If either of these conditions is not met, operator A will not be able to enter receipts in W1.
NOTE In order to give a company access to a given program, you must give the company access to the program’s entire path; that is, all submenus to which the program is attached. If you do not know the submenus to which a program is attached, you must perform a query in JOSE. See [Looking Up a Program’s Path](administracao.html#looking-up-a-program-s-path) for further instructions.

SYSTEM ADMINISTRATION GUIDE 4.2* 47
1 Enter the appropriate company (usually Z1).
2 Enter COAC.
3 Key in your company code and press Enter.
4 Key in your subsystem code and press Enter or use your pick list to select it.
FIELD DESCRIPTIONS
Company Code Mandatory
The company to which you wish to give access.
Subsystem Code Mandatory
The subsystem code to which the program is attached. If you do not know to which submenu a program is attached, you must look it up in JOSE.
Selection Code A list of all selection codes that are attached to the submenu that you selected in the Subsystem Code field.
Dependent Selections If the selection code is a submenu, the number of programs and submenus that are attached to it.
Attach to Subsystem Y = Yes
N = No
If you select Y for Yes, the company will have access to that selection code plus any dependent selections. If you select N for No, the company will have no access to either the selection code or any dependent selections.

Company Access (COAC) showing WO subsystem
5 Use your arrow keys to position your cursor on the selection code that you wish to give access to.
6 In the Attach to Subsystem field, key in Y for Yes and press Enter.
7 If you entered Yes in the previous field and your selection code has dependent selections, click on 
Dependent Selections. Then repeat the above steps for each dependent selection. In order to give a company access to a given program, you must always drill down to the lowest level.
8 When you finish giving your company access to the required programs, click on Return to Main and then 
Exit to exit.

### REMOVING PROGRAMS FROM COMPANIES <a id="removing-programs-from-companies"></a>

1 Enter COAC. 
2 Key in your company code and press Enter.
3 Key in your subsystem code and press Enter or use your pick list to select it.
4 Use your arrow keys to position your cursor on the selection code that you wish to remove access to.
5 In the Attach to Subsystem field, key in N for No and press Enter.
6 When you finish removing the required programs, click on Return to Main and then Exit to exit.

SYSTEM ADMINISTRATION GUIDE 4.2* 49

### Overview of New User Setup <a id="overview-of-new-user-setup"></a>

There are four steps to follow in setting up a new user:

### Setting Up New Users in OPER <a id="setting-up-new-users-in-oper"></a>

You set up new users in OPER (Operator Code). There are two classes of users in AccellosOne 3PL: 
system administrators and regular users. System administrators can create other operators, give operators access to programs, remove access to programs and delete operators. Regular users, on the other hand, are not able to perform any of these functions. They are limited to changing their own password in the password change program.
When you set up a new user, that user’s password is preset to his or her operator code followed by the default password in INST (Installation Parameters). For example, if you set up a new user called Bob and the default password in INST is set to “CHANGEIT”, Bob’s initial password will be BOBCHANGEIT. The new user must change this password when he or she logs on to AccellosOne 3PL for the first time.
ActiveDesktop
OPAC/
COOA
The new user must log into ActiveDesktop and change his or her temporary password.
You assign program access to users in
OPAC or copy program access in COOA.
OPER
OPRS
You set up your new user in OPER as either a system administrator or regular user.
You enter your operator restrictions in
OPRS. You can restrict an operator to certain printers, companies, customers, consignees, shippers, carriers and documents.

FIELD DESCRIPTIONS
Operator/ Employee 
Code
The operator code. The code that you enter cannot start with a number and cannot exceed 20 characters in length. No embedded spaces or special characters are allowed.
Name The operator name.
Language Code Mandatory
The user’s language. This field determines the language of the screens, menus, hint lines, error messages and system codes for the user throughout the entire AccellosOne 3PL suite of products.
e-Mail Address Optional
The user’s e-mail address. 
Operator Flag O = Operator
B = Both (only used to give an operator supervisor privileges in certain RF program)
Set to O for Operator
Employee ID Reserved for future use
Show Inventory Access 
Code
Y = Yes
N = No
If you set this flag to Yes, the inventory access code will be displayed when the user looks up inventory in LOEN. The inventory access code is a fivecharacter system-generated code that refers to a specific inventory entity. For example, the code 01ABC could refer to item 1, lot 101, pallet ID 123.
If you set this flag to No, the inventory access code will not be displayed when the user looks up inventory in LOEN.
Show Archive Data in 
Look Ups
See [ARCHIVING AND PURGING](administracao-manutencao.html#archiving-and-purging).

SYSTEM ADMINISTRATION GUIDE 4.2* 51

### SETTING UP AN OPERATOR <a id="setting-up-an-operator"></a>

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
If you enter Y for Yes, the user will enjoy “system administrator” privileges and can create other operators, give operators access to programs, remove access to programs and delete operators. If you enter N for No, the user will not be able to perform any of these functions. Non-system administrators are limited to changing their own password in the password change program.
If you change this flag for an existing user, that user’s password will be set to his or her operator code plus the default password in INST (Installation 
Parameters). For example, if the user’s operator code is JOE and the default password in INST is set to “CHANGEIT”, Joe’s password will be set to 
JOECHANGEIT.
NOTE Before system administrators can give operators access to programs in OPAC (Operator Access), they must be given access to OPAC themselves. Likewise, before system administrators can set up job selection codes in JOSE, they must be given access to this program.
Authority Flag Reserved for future use
FIELD DESCRIPTIONS

Operator Code (OPER) screen showing an operator
15 Click on Exit to exit.

### SETTING UP AN OPERATOR WITH SUPERVISOR PRIVILEGES <a id="setting-up-an-operator-with-supervisor-privileges"></a>

Certain RF programs require supervisor privileges to access. You give an operator supervisor privileges by setting the Supervisor Flag to Y for Yes.
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
10 Press Enter to position your cursor in the Company Code field. Then key in your company code and press Enter.
11 Press Enter to position your cursor in the Warehouse Code field. Then use the pick list function to select any warehouse code from the pick list.
12 In the MHE Type Code field, use your pick list to select any MHE type code.
13 Press Enter until your cursor is positioned in the Employee Temporary Flag field. Then key in N for No and press Enter.

SYSTEM ADMINISTRATION GUIDE 4.2* 53
14 In the Supervisor Flag field, key in Y for Yes and press Enter.
15 Click on Return to Main and Exit to exit.

### DEACTIVATING AN OPERATOR <a id="deactivating-an-operator"></a>

If you deactivate an operator, the operator will not be able to log on to AccellosOne 3PL until he or she has been reactivated.
1 Enter OPER.
2 Retrieve the operator that you wish to deactivate.
3 Press Enter to position your cursor in the Name field.
4 Click on Delete.
5 Click on Exit to exit.

### REACTIVATING AN OPERATOR <a id="reactivating-an-operator"></a>

If an operator has been deactivated, he or she must be reactivated in order to access AccellosOne 3PL. 
There are two steps to follow in reactivating an operator: first you change the status of the operator in OPER from D to A and then you reset the operator’s password in ROPA (Reset Operator Password).
1 Enter OPER.
2 Retrieve the operator that you wish to reactivate.
3 Continue to press Enter until your cursor is positioned in the Status field.
4 Key in A for Activate and press Enter.
5 Click on Exit to exit.
6 Proceed to reset the operator’s password by following the instructions in [Resetting an Operator’s Password in ROPA](administracao.html#resetting-an-operator-s-password-in-ropa).

### RESETTING AN OPERATOR’S PASSWORD IN ROPA <a id="resetting-an-operator-s-password-in-ropa"></a>

Resetting an operator’s password is necessary in the three cases:
 you wish to reactivate a deactivated operator
 the operator has forgotten his or her password and cannot log on to AccellosOne 3PL
 an RF operator has no access to ActiveDesktop and has never logged on to AccellosOne 3PL through 
ActiveDesktop
When you reset an operator’s password, that user’s password is preset to his or her operator code plus the default password in INST (Installation Parameters). For example, if the user’s operator code is JOE and the default password in INST is set to “CHANGEIT”, Joe’s password will be set to JOECHANGEIT. The user must change this password when he or she logs on to AccellosOne 3PL for the first time.
1 Enter ROPA.
2 Key in the operator code that you wish to reset and press Enter.

Reset Operator Password (ROPA)
3 Click on Reset.
4 Click on Yes when prompted to reset the password.
5 Click on Exit to exit.

### Assigning Program Access to Users in OPAC <a id="assigning-program-access-to-users-in-opac"></a>

The AccellosOne 3PL menu structure has a tree formation consisting of a main menu, submenus and individual programs. The MAIN menu forms the trunk from which the submenus branch out. Many of the submenus have their own submenus and some of these have yet another submenu attached to them as well. 
Attached to submenus at any level are the programs themselves that you use to look up information and enter data. 
The following diagram shows a sample selection of programs that are attached to the submenu RECE.

SYSTEM ADMINISTRATION GUIDE 4.2* 55
In order to give a user access to any given program, you have to give access to MAIN as well as to all the submenus to which the program is attached.
For example, to give a user access to ENRE (Enter Receipts), you would first give access to MAIN, then give access to WO (Warehouse Operations), then give access to RECE (Receiving) and lastly give access to the program itself, ENRE. If you failed to give the user access to MAIN or any of the submenus, the user would be unable to enter ENRE. 
There are two possible levels of access for any given AccellosOne 3PL program: read only = Yes and read only = No. 
You assign program access to users in OPAC (Operator Access). OPAC gives users access to all companies on your system. If you wish to restrict users to certain companies, you must do so in OPRS (Operator Restrictions).

### RF MENU STRUCTURE <a id="rf-menu-structure"></a>

The Main Menu from which all RF programs branch out is called RFMN. There are four submenus attached to 
RFMN: RFLOOK for RF look-up programs, RFINB for RF receiving, RFOUTB for RF shipping and RFINVT for miscellaneous RF programs.
read only = Yes the user can look up information in the program but cannot change it read only = No the user can modify any information in the program; for example, create a record, change a record and delete a record
MAIN
WO (Warehouse
Operations)
SA (System
Administration)
CS (Customer
Service)
RECE (Receiving)
CHRF Time stamp and confirm receipts
CORL Confirm receipts - line at a time
ENRE Enter Receipts (inbounds)
PRRE Print receiving documents - all
PRRM Print receiving documents - specific
RERE Requeue receipt documents submenus attached to MAIN submenu RECE attached to submenu WO programs attached to submenu RECE

### LOOKING UP SUBMENUS <a id="looking-up-submenus"></a>

You look up submenus in OPAC (Operator Access).
1 Enter OPAC.
2 Key in your submenu code and press Enter or use your pick list to select it.

Operator Access (OPAC)
3 If the selection code has dependent selections, the code is a submenu. If the selection code has no dependent selections, the code is a program and you cannot drill down any further.
4 Click on Subsystem Code and Exit to exit.

### ASSIGNING PROGRAM ACCESS TO A USER <a id="assigning-program-access-to-a-user"></a>

You assign program access to users in OPAC (Operator Access). OPAC requires you to assign program access to individual users one program at a time. If you have multiple users that share the same access privileges, you can set up generic operators (for example, level 1 security, level 2 security, level 3 security, etc.) 
and copy the generic access to the individual operators in COOA (Copy Operator Access). 
CAUTION You cannot assign program access to a user until that user has logged into ActiveDesktop for the first time and changed his or her temporary password from 
JOEMUSTCHANGE to a permanent password. “JOEMUSTCHANGE” passwords are not valid in OPAC, COOA (Copy Operator Access) and OPRS (Operator Restrictions).
the name of the submenu this code has no dependent selections and is therefore a program this code has 14 dependent selections and is therefore a submenu

SYSTEM ADMINISTRATION GUIDE 4.2* 57
1 Enter OPAC.
2 Key in MAIN or RFMN and press Enter.
3 If you have multiple MAIN/RFMN menus on your system, select the MAIN/RFMN menu for the appropriate language.

Operator Access (OPAC) screen showing MAIN submenu
4 The system will display all submenus attached to MAIN (CL, CS, DA, etc.) or RFMN. In the screen shown above, there are a total of 16 submenus attached to MAIN. In the Dependent Selections column is shown the number of submenus and programs attached to each submenu attached to MAIN. For example, the 
CS submenu has two dependent selections.
5 Click on Operator Block. In this step you are going to give the user access to MAIN/RFMN.

Operator Access (OPAC) showing Operator Block
6 Click on Create Record.
7 Key in your operator code and press Enter or use your pick list to select your operator.
8 In the Read Only Flag field, key in Y for Yes or N for No and press Enter.
9 When you finish giving your user access to MAIN/RFMN, click on Return to Main to exit Create Mode and return to Main Mode.
10 Click on Master Block to display the programs and submenus attached to your first submenu.

SYSTEM ADMINISTRATION GUIDE 4.2* 59

Operator Access (OPAC) screen showing four programs attached to FX submenu
11 If you wish to give the user access to this program or submenu, click on Operator Block and repeat steps 
7 and 8. If you do not wish to give the user access to this program or submenu, click on Previous Subsystem.
12 Continue to assign access to the user. Remember to drill down from the MAIN/RFMN submenus to the program that you wish to give access to and then work your way back up to the submenus attached to 
MAIN/RFMN. 
13 When you finish giving your user access to the programs that he requires, press Exit to exit.

### REMOVING A USER’S PROGRAM ACCESS <a id="removing-a-user-s-program-access"></a>

1 Enter OPAC.
2 Key in MAIN or RFMN and press Enter.
3 If you have multiple MAIN/RFMN menus on your system, select the MAIN/RFMN menu for the appropriate language.
The system will display all submenus attached to MAIN (CL, CS, DA, etc.) or RFMN. 
NOTE You must enter the Operator Block and create a record for each submenu starting from MAIN /RFMN in a program’s path. If a single link is missing — that is, there is no access to a particular submenu in a program’s path — the user will be unable to access the program.

4 Continue to drill down from MAIN until you reach the program or submenu whose access you wish to remove.
5 Click on Operator Block. 

Operator Access (OPAC) showing Operator Block
6 Position your cursor over the operator whose access you wish to remove.
7 Press Enter to position your cursor in the Read Only Flag field.
8 Click on Delete.
9 Press F4 the required number of times to exit OPAC.

### COPYING AN OPERATOR’S ACCESS IN COOA <a id="copying-an-operator-s-access-in-cooa"></a>

You can copy access from one user to another user in the program COOA (Copy Operator Access). The copy function allows you to set up generic security levels such as Level 1, Level 2, Level 3, Level 4, etc. Once you have set up your generic operator codes and assigned them the appropriate program access in OPAC (Operator Access), you can copy their access and assign it to individual operators in a single step. 
The copy function makes it possible to set up standard levels of access for different classes of users, thereby eliminating the need to assign access to a user one program at a time in OPAC (Operator Access).
When you use the copy function, the “from” and “to” operators must have the same language code in OPER (Operator Code). You cannot copy operator 1’s access (language code = ENUS) to operator 2 (language code = ESCL).

SYSTEM ADMINISTRATION GUIDE 4.2* 61
There are two options in COOA: ALL or Missing. The All option gives the “from” and “to” operators identical access. The Missing option, on the other hand, adds the “from” operator’s access to the “to” operator’s access without making the two operators identical. 
1 Enter COOA.
2 Key in your from operator and press Enter.
3 When the list of operators is displayed, use your arrow keys to position your cursor on the operator code that is to receive the from operator’s program access.
4 Press Enter to position your cursor in the First Menu field. Then do one of the following:
5 Press Enter again to position your cursor in the All/Missing field.
6 Key in A for All or M for Missing and press Enter.
7 If required, you can copy operator restrictions set up in OPRS by keying in Y for Yes in the appropriate field(s) — CUST Restrictions, CONS restrictions, etc. — and pressing Enter.
A’s Access
B’s Access 
Before Copy 
B’s Access After Copy 
Using All Option Explanation
ENRE, ENOR CHRF, CHOF ENRE, ENOR The system deletes B’s original access and then copies A’s access to B.
A’s Access
B’s Access 
Before Copy
B’s Access After Copy 
Using Missing Option Explanation
ENRE, ENOR CHRF, CHOF ENRE, ENOR, CHRF, CHOF The system copies A’s access to B without deleting B’s original access.
If you wish to copy access for non-RF programs only:
If you wish to copy access for RF programs only:
a) Key in MAIN and press Enter. a) Key in RFMN and press Enter.

Copy Operator Access (COOA) showing the operator ABCFOOD-1 receiving the access of BOB
8 Repeat steps 3 to 7 for each additional operator that is to receive the from operator’s program access.
9 When you finish copying access, click on Operator Code and Exit to exit.

### Entering Operator Restrictions in OPRS <a id="entering-operator-restrictions-in-oprs"></a>

You can restrict an operator by printer, company, customer, consignee, shipper, carrier and document. A restriction can be either inclusive or exclusive. An inclusive restriction means that the user is limited to the printer, company, customer, consignee, shipper, carrier or document that you specify. An exclusive restriction means that the user can use any printer(s), company/companies, customer(s), consignee(s), shipper(s), carrier(s) or document(s) on your system except those that are specifically excluded.
For example, if an operator is restricted to customer ABC, only customer ABC can be accessed in CUST, only 
ABC’s inventory can be received in ENRE, only customer ABC’s inventory can be shipped in ENOR, only 
ABC’s inventory can be looked up in LOEN, only ABC’s inventory can be adjusted in ENAJ and only ABC’s inventory can be relocated in RELO.
If there are no restrictions for a particular operator in OPRS, that operator has access to all printers, companies, customers, consignees, shippers, carriers and documents.

SYSTEM ADMINISTRATION GUIDE 4.2* 63
You can only change the operator restrictions of operators other than yourself. If you need to change your own operator restrictions, another user must log on and perform the change for you.

### CUSTOMER/CONSIGNEE/SHIPPER/CARRIER/DOCUMENT TABS <a id="customer-consignee-shipper-carrier-document-tabs"></a>

These tabs are only available if you define an inclusive company restriction in the Company Block. Exclusive companies cannot be restricted by customer, consignee, shipper, carrier or document.
FIELD DESCRIPTIONS
Operator Code Your operator code. You cannot change the restrictions of an operator who is currently logged on.
Printer Code The printer or printers that the operator is restricted to. If you leave this field blank, the operator will have access to all printers.
Company Code The company or companies that the operator is restricted to. If you leave this field blank, the operator will have access to all companies.
Inclusive/Exclusive If you set the company to Inclusive, the operator is restricted to that company. 
If you set the company to Exclusive, the operator can use any company on your system except those that are specifically excluded.
You can enter multiple restrictions per company, but all restrictions must be of the same type; that is, either inclusive or exclusive.
FIELD DESCRIPTIONS
Customer Code The customer or customers that the operator is restricted to. If you leave this field blank, the operator will have access to all customers.
Inclusive/Exclusive If you set the customer to Inclusive, the operator is restricted to that customer. 
If you set the company to Exclusive, the operator can use any customer on your system except those that are specifically excluded.
You can enter multiple restrictions per customer, but all restrictions must be of the same type; that is, either inclusive or exclusive.
Consignee Code The consignee or consignees that the operator is restricted to. If you leave this field blank, the operator will have access to all consignees.
Consignee restrictions apply to the following programs: CONS, ENOR and 
LOOR.

1 Enter OPRS.
Inclusive/Exclusive If you set the consignee to Inclusive, the operator is restricted to that consignee. If you set the company to Exclusive, the operator can use any consignee on your system except those that are specifically excluded.
You can enter multiple restrictions per consignee, but all restrictions must be of the same type; that is, either inclusive or exclusive.
Shipper Code The shipper or shippers that the operator is restricted to. If you leave this field blank, the operator will have access to all shippers.
Shipper restrictions apply to the following programs: SHIP, ENRE and LORE.
Inclusive/Exclusive If you set the shipper to Inclusive, the operator is restricted to that shipper. If you set the company to Exclusive, the operator can use any shipper on your system except those that are specifically excluded.
You can enter multiple restrictions per shipper, but all restrictions must be of the same type; that is, either inclusive or exclusive.
Carrier Code The carrier or carriers that the operator is restricted to. If you leave this field blank, the operator will have access to all carriers.
Carrier restrictions apply to the following programs: CARR, ENRE, ENOR, 
LORE and LOOR.
Inclusive/Exclusive If you set the carrier to Inclusive, the operator is restricted to that carrier. If you set the company to Exclusive, the operator can use any carrier on your system except those that are specifically excluded.
You can enter multiple restrictions per carrier, but all restrictions must be of the same type; that is, either inclusive or exclusive.
Document Code The document or documents that the operator is restricted to. If you leave this field blank, the operator will have access to all documents.
Document restrictions apply to the following programs: DOCU, PRRE, PRRM, 
PROM and PROR. They also apply to e-Vista.
Inclusive/Exclusive If you set the document to Inclusive, the operator is restricted to that document. If you set the company to Exclusive, the operator can use any document on your system except those that are specifically excluded.
You can enter multiple restrictions per document, but all restrictions must be of the same type; that is, either inclusive or exclusive.
FIELD DESCRIPTIONS

SYSTEM ADMINISTRATION GUIDE 4.2* 65

Operator Restrictions (OPRS)
2 Key in the operator code whose restrictions you wish to change and press Enter.
3 Click on Company Block.
4 In the Company Block, click on Create Record.
5 Key in your company code restriction and press Enter.
If you wish to enter a printer restriction:
If you do not wish to enter a printer restriction:
a) Key in your printer code and press Enter.
b) Press Enter to bypass the Correct field.
c) Repeat the above two steps for each additional printer that you wish to add.
d) When you finishing adding your printers, click on Return to Main to exit Create Mode.
a) Proceed to next step. 

6 Do one of the following:

Operator Restrictions (OPRS) showing an operator limited to customer A in company V6
7 When you finish entering your restrictions, click on Return to Main and Company Block. Then click on 
Printer Block and Operator Block. Lastly, click on Exit to exit.

### REMOVING RESTRICTIONS <a id="removing-restrictions"></a>

You remove restrictions by deleting the appropriate code in the block or tab containing the restriction.
1 Enter OPRS.
2 Key in your operator code and press Enter.
3 Go to the block or tab containing the restriction that you wish to remove.
If you wish to enter a customer, consignee, shipper, carrier or document restriction:
If you do not wish to enter any further restrictions:
a) Click on the appropriate tab.
b) Click on Inclusive/Exclusive until the correct value is displayed.
c) Key in the appropriate customer, consignee, shipper, carrier or document code and press Enter.
d) Press Enter again to bypass the 
Correct field.
e) Repeat the above two steps for each additional code that you wish to add.
f) If you wish to define restrictions on another tab, click on the tab and then repeat the above steps.
a) Proceed to next step.

SYSTEM ADMINISTRATION GUIDE 4.2* 67
4 Press the tab key until the Delete command is displayed for the restriction that you wish to remove.
5 Click on Delete.
6 If you are in the Customer, Consignee, Shipper, Carrier or Document tab, click on Company Block.
7 Click on Printer Block and Operator Code. Then click on Exit to exit OPRS. 

### Setting Up Roles in ROMA <a id="setting-up-roles-in-roma"></a>

d’Amigo and e-Filing use role-based access control to determine which users have access to which functions. 
A role is a classification for security purposes that defines which functions a particular user has access to. For example, you could create a role called OFFICE and attach to this role all your office users. Office users would have access only to those d’Amigo menus and templates that office users need. 
Likewise, you could create a role called SUPERVISOR and attach to this role all your supervisors. Supervisors would have access only to those e-Filing document types and functions that supervisors need.
You set up your roles in the program ROMA (Role). ActiveDesktop supports role overlapping; that is, the same operator can be attached to as many roles as required.
1 Enter ROMA.

Role (ROMA) screen
2 Click on Create Record .
3 Key in your role code and press Enter.
4 Key in a description for your role code and press Enter.
5 Click on Save .
6 Click on Attach Operator .

Role (ROMA) screen showing Operator pick list
7 Click on the operators that you wish to select. If you wish to select all operators, you can click on Select 
All. If you wish to deselect all operators, click on Deselect All.
8 When you finish making your selections, click on Save .
9 Click on Return and then Exit .

### DELETING A ROLE <a id="deleting-a-role"></a>

If there are no dependencies such as operators, d’Amigo templates or e-Filing records attached to a role, deleting it will remove it from AccellosOne 3PL. If there are dependencies such as operators, d’Amigo templates or e-Filing records attached to a role, deleting a role will deactivate it only.
1 Enter ROMA.
2 Select the role that you wish to delete.
3 Click on Delete .
4 Click on Exit .

### MODIFYING A ROLE <a id="modifying-a-role"></a>

You can add operators to, and remove operators from, a role at any time.
1 Enter ROMA.
2 Select the role that you wish to modify.
3 Click on Edit.

SYSTEM ADMINISTRATION GUIDE 4.2* 69
4 Select the operators that you wish to add to the role and/or deselect the operators that you wish to remove from the role.
5 When you finish making your selections and deselections, click Ok.
6 Click on Exit .

### LOOKING UP AN OPERATOR’S ROLES <a id="looking-up-an-operator-s-roles"></a>

If an operator is attached to multiple roles, you can use the Look Up Roles command to see which roles the operator has access to.
1 Click on Look Up Roles .

Look Up Roles screen
2 Select your operator from the dropdown list.
3 Click on Execute Query .

ROMA screen showing operator attached to two roles
4 When you finish looking up your role information, click on Return to close the Look Up Roles window.

### Setting Up ActiveDesktop Security Administrators in ADSA <a id="setting-up-activedesktop-security-administrators-in-adsa"></a>

In this program, you set up your ActiveDesktop security administrator(s). An ActiveDesktop security administrator is an operator set up in OPER who has access to one or more d’Amigo security administration functions. If you do not set up an operator in ADSA, the operator cannot perform security administration functions and has access to only those templates assigned to the operator in ROMA (Roles). 
1 Enter ADSA.

ActiveDesktop Security Administrator (ADSA) screen showing D4SUPPORT as a security administrator
2 If the operator that you wish to set up for ActiveDesktop security is not shown in the list of operators on the left-side of the screen, click on Create Record .
3 Key in your operator code and press Enter or select the appropriate operator code from the pick list.
FIELD DESCRIPTIONS
Operator Code (OPER) The operator that you wish to set up for ActiveDesktop security. This operator must be defined as a system administrator in OPER.
Global Access Privilege If you check the Global Access checkbox, the operator is attached to a special role called Global and can view all d'Amigo templates and views. If you do 
NOT check the Global Access checkbox, the operator can only view those templates assigned to the operator in ROMA (Roles).
Alter Template Privilege If you check the Alter Template Privilege checkbox, the operator can create, modify and delete templates. If you do NOT check the Alter Template Privilege checkbox, the operator cannot create, modify and delete templates.
Alter View Privilege If you check the Alter View Privilege checkbox, the operator can modify and delete any view. If you do NOT check the Alter View Privilege checkbox, the operator can only modify and delete views created by him/herself.

SYSTEM ADMINISTRATION GUIDE 4.2* 71
4 Click on the appropriate checkboxes (Global Access Privilege, Alter Template Privilege, Alter View Privilege) to assign your operator the correct access.
5 When you finish setting up your ActiveDesktop security administrator, click on Save .
6 Click on Exit to exit ADSA.

### DELETING A SECURITY ADMINISTRATOR <a id="deleting-a-security-administrator"></a>

1 Enter ADSA.
2 Select the operator that you wish to delete.
3 Click on Delete .
4 Click on Exit .

### Setting Up e-Filing Security <a id="setting-up-e-filing-security"></a>

Access to e-Filing is governed by ActiveDesktop’s role-based security system. Users must be given access to the appropriate document types and functions in ROMA (Roles).
Document types refer to which indexes a user has access to. Valid values are any index, carrier, company, customer, invoice, item, no index, order, receipt and shipper. Functions refer to which function(s) a user attached to a particular role is allowed to perform. The list of available functions includes:
 purge document
 batch upload
 update document information
 upload document
1 Create a new role in ROMA for e-Filing security or retrieve an existing role.
2 Attach the appropriate operators to your new or existing role.
3 Click on the e-Filing tab.
NOTE Operators can be attached to multiple roles in ROMA. If the same operator is assigned to two or more roles and those roles have different e-Filing document types and functions, the operator will have access to all document types and functions for those two or more roles.

ROMA screen showing e-Filing tab
4 Click on Attach Operator .

ROMA screen showing no access for OFFICE
5 Select the document type that you wish to give access to.
6 Select the function that you wish to give access to.
7 Click on Save to add the document type/function to the left-hand column.
8 Repeat the above three steps for each additional document type and function that you wish to add.
If your role has access to some document types and not others (that is, it does not have access to “Any 
Index), you must set up document types and functions for each document type/function combination.
For example, if your role has access to consignee, customer and shipper document types and two functions (Purge document and Batch upload), you must create six records in ROMA:
consignee / Purge document consignee / Batch upload customer / Purge document customer / Batch upload shipper / Purge document

SYSTEM ADMINISTRATION GUIDE 4.2* 73 shipper / Batch upload

ROMA screen showing three functions attached to the customer and item document type
9 When you finish setting up your e-Filing security, click on Return .

ROMA screen showing access for OFFICE
10 Click on Exit .

### REMOVING DOCUMENT TYPES AND FUNCTIONS FROM A ROLE <a id="removing-document-types-and-functions-from-a-role"></a>

1 Retrieve the role whose access you wish to modify.
2 Click on the e-Filing tab.
3 Click on Attach e-Filing Codes .
4 Double click the document type/function that you wish to remove.

5 Click on Delete .
6 Click on Return .
7 Click on Exit .

### Activating the ActiveDesktop Icons <a id="activating-the-activedesktop-icons"></a>

All users are automatically given access to the AccellosOne 3PL and Password Change icons in ActiveDesktop. All other icons (for example, Alert Maintenance, Operational Board, d’Amigo, e-Filing, etc.) must be manually assigned to each user in OPAC (Operator Access). If a user does not have access to a ActiveDesktop icon, that icon will not appear when the user logs on and the user will have no access to the program.
System administrators are automatically given access to all ActiveDesktop icons; they do not need to be assigned to icons in OPAC.
ActiveDesktop icons are listed under the subsystem code ACTIVE in OPAC. There are nine possible icons that a user can have access to:
NOTE Access to an ActiveDesktop icon will display that icon when the user logs onto ActiveDesktop. However, all other security conditions must be satisfied before the user can enter the program and work in it. For example, to view documents in eFiling, the user must be assigned the appropriate document types and functions in 
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

SYSTEM ADMINISTRATION GUIDE 4.2* 75
1 Enter OPAC.
2 Key in ACTIVE as your subsystem code and press Enter.

OPAC screen showing the ACTIVE subsystem code
3 Click on Operator Block and proceed to add the appropriate operators to the appropriate selection codes.
4 When you finish adding your operators, click on Master Block, Subsystem Code and Exit.

### Modifying Your Installation Parameters in INST <a id="modifying-your-installation-parameters-in-inst"></a>

In this program, you set up your installation parameters. Installation parameters define the facility in which your computer is located and certain system-wide parameters such as the date delimiter and format, password expiry dates, etc. Currently, only password expiry dates and ActiveDesktop security are implemented in INST. 
ADVIST e-Vista
ADWAVE Wave Manager
FIELD DESCRIPTIONS
Installation Name The name of your installation.
SELECTION 
CODE DESCRIPTION

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
If you select Yes, ActiveDesktop security will be enabled. d’Amigo users can only access the menus and templates attached to their role in ROMA and eFiling users can only access the document types and functions attached to their roles in ROMA.
If you select No, ActiveDesktop security will be disabled. Any d’Amigo user will be able to access, modify and delete any template or view and any e-Filing user will have access to all document types and all functions. 
Print Restrictions on 
Reserved for future use.
Default Password The default password for your environment. For example. if the default password is set to “CHANGEIT” and a user called Tom wishes to log on for the first time, he must enter TOMCHANGEIT as his password.
Passwords Expire in (Days)
This field allows you to define an expiry date for all user passwords in your installation. You activate this feature by entering the appropriate number of days in the Passwords Expiry in (Days) field. A password is considered to be expired when the date that the password was last changed plus the number of days that you specify in the Passwords Expire in (Days) field is a date in the past.
EXAMPLE
You have three operators on your system and you enter a value of 30 days in this field. Operator 1, who was added to the system on the same day, will have to change his password in 30 days. Operator 2, who was added to the system six months ago, will have to change his password immediately. Operator 3, who was added to the system six months ago and had his password changed one week ago, will have to change his password in three weeks or 21 days.
FIELD DESCRIPTIONS

SYSTEM ADMINISTRATION GUIDE 4.2* 77
1 Enter INST.
If you leave this field blank, passwords will not expire until they are reset by a system administrator in ROPA (Reset Operator Password) or manually changed by the user using the Password Change function in ActiveDesktop.
Application Home DirectoryFor HighJump use only.
Document Archive DirectoryThe archive directory for order and receipt documents printed in PRRE, 
PRRM, PROM and PROR. If you set up an archive directory, any document that you print in these programs will be automatically moved to this directory after the number of months specified in the next field has passed.
Storing large numbers of old receipt and order documents in a directory other than the application home directory makes it possible to query for an old bill of lading, for example, without affecting the performance of day-to-day operations in AccellosOne 3PL.
Receipt and order documents stored in the archive directory can be viewed in 
LORE and LOOR like any other receipt or order document.
Number of Months to 
Retain Documents in 
Home Directory
The number of months that receipt or order documents will be kept in the application home directory before being move to the archive directory.
FIELD DESCRIPTIONS

Installation Parameters (INST) screen
2 When you finish modifying your installation parameters, click on Exit to exit.

SYSTEM ADMINISTRATION GUIDE 4.2* 79

## Special Verification Programs <a id="special-verification-programs"></a>

*Manual L — System Administration*

### Overview <a id="overview"></a>

A special verification program is a custom program or plug-in that is automatically run at some stage in your inbound receiving or outbound shipping process. Special verification programs perform a variety of functions some of which are visible to the user and some of which are not.
They can display the Pallet Details Block or the Bill Later - Enter Charges screen, update the Time-Stamping 
Block of LORE/LOOR for the appointment system, create back orders, cancel the printing of auto-printed documents, check for non-numeric values in the Extra Reference fields of ENOR/ENRE, create back receipts for product not received on the original receipt and perform many other functions.
Special verification programs are only executed via ENRE/ENOR, CHRF /CHOF and CORL/COOR.
You set up special verification programs in the Special Verification Block of DIFP (Depositor Workflow Profile). 
Special verification programs can be attached to any flow in your inbound or outbound flow profile. For example, the special verification CBOR (Create Back Order) allows you to create back orders at any outbound flow on your system except ENOR (Enter Order).
FIELD DESCRIPTIONS
Sequence Mandatory
If you have multiple special verification programs attached to the same flow, you specify their sequence by means of a sequence number. If you have a single special verification program, use the number 10.
Special Verification Code Mandatory
Your special verification code.
Complete Y = Yes
N = No
If you set this flag to Y for Yes, the special verification program must run successfully before you can advance to the next flow. For example, if you attach a special verification program for catch weights to FLOW2 and set this flag to Y, you will not be able to advance to FLOW3 if you fail to capture a catch weight.
If you set this flag to N for No, you can advance to the next flow even if the special verification program does not run successfully.
NOTE If you set this flag to Y for Yes, you must set the Sequence flag to B for Before.

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
9 Key in your special verification code and press Enter or use your pick list to select it. To select a code using a pick list, press F10 to display the pick list, position your cursor over the appropriate code using your arrow keys and click on Select to select it.
Sequence A = After
B = Before
If you set this flag to A for After, the special verification program will run after the flow to which it is attached. If you set this flag to B for Before, the special verification program will run before the flow to which it is attached.
Display Reserved for future use.
FIELD DESCRIPTIONS

10 In the Complete field, key in Y for Yes or N for No and press Enter.
11 In the Sequence field, key in A for After or B for Before and press Enter.
12 Press Enter to bypass the Display field.

Depositor Workflow Profile (DIFP) screen showing special verification MRAC attached to the flow 
DRAR
13 Click on Return to Main to exit create mode.
14 Click on Document Block, Flow Block, In/Out/Repi/Relo Block and then Master Block.
15 Click on Exit to exit.

### Looking Up Special Verification Programs in LOSV <a id="looking-up-special-verification-programs-in-losv"></a>

You can look up a complete list of all special verification programs in LOSV (Look Up Special Verification).
1 Enter LOSV.
2 Click on Execute Query.

SYSTEM ADMINISTRATION GUIDE 4.2* 197

Look Up Special Verification (LOSV) screen
3 When you finish looking up your special verification programs, click on Exit.

### Creating Your Own Special Verification Program in MSVS <a id="creating-your-own-special-verification-program-in-msvs"></a>

MSVS (Special Verifier SQL) allows you to create your own special verify programs to implement specific validation for an order or receipt. You can define a sequence of SQL statements and attach this sequence to a combination of customer, carrier, consignee/ shipper, return value, type of failure and error message. The resulting objects are attached to a workflow in DIFP.

MSVS screen showing sample special verification program

### Mandatory Order Accessorials (MOAC) <a id="mandatory-order-accessorials-moac"></a>

This special verify program prompts you to enter an accessorial charge when you exit ENOR or advance to the next flow in CHOF. You can enter an accessorial charge or you can click on Exit to exit without entering an accessorial charge.

SYSTEM ADMINISTRATION GUIDE 4.2* 199

MOAC screen showing Bill Later - Enter Charges program

### Mandatory Receipt Accessorials (MRAC) <a id="mandatory-receipt-accessorials-mrac"></a>

This special verify program prompts you to enter an accessorial charge when you exit ENRE or advance to the next flow in CHRF. You can enter an accessorial charge or you can click on Exit to exit without entering an accessorial charge.

MRAC screen showing Bill Later - Enter Charges program

### Mandatory Receipt Carrier Details (MRCA) <a id="mandatory-receipt-carrier-details-mrca"></a>

This special verify program displays the Carrier Details block when you exit ENRE or advance to the next flow in CHRF. You can enter your carrier details or you can click on Exit to exit without entering carrier details.
NOTE MRCA operates independently of the Carrier Details flag in ENRE. If you enter (C)onfirmation or (B)oth in the Carrier Details field in ENRE, the Carrier Details screen will appear twice during receipt confirmation. To see the pop-up screen only once during receipt confirmation, you must bypass the Carrier Details field.

SYSTEM ADMINISTRATION GUIDE 4.2* 201

MRCA screen showing Carrier Block

### Mandatory Order Carrier Details (MOCA) <a id="mandatory-order-carrier-details-moca"></a>

This special verify program displays the Carrier Details block when you exit ENOR or advance to the next flow in CHOF. You can enter your carrier details or you can click on Exit to exit without entering carrier details.
NOTE MOCA operates independently of the Carrier Details flag in ENOR. If you enter (C)onfirmation or (B)oth in the Carrier Details field in ENOR, the Carrier Details screen will appear twice during order confirmation. To see the pop-up screen only once during order confirmation, you must bypass the Carrier Details field.

MOCA screen showing Carrier Block

### Order Total Quantity Verification (OTQV) <a id="order-total-quantity-verification-otqv"></a>

This special verify program displays the total order quantity when you advance to the next flow in CHOF (Time Stamp and Confirm Orders). The total order quantity is shown in whichever SKU or SKU’S were entered in ENOR. For example, if line 1 is entered as one pallet, line 2 is entered as 60 cases, line 3 is entered as 10 cases and line four is entered as 5 eaches, the total order quantity shown in OTQV will be one pallet (line 1), 70 cases (lines 2 and 3) and 5 eaches (line 4).
The operator will be prompted to accept the total order quantity. If the operator accepts the total order quantity, the order’s flow will be advanced normally. If the operator does not accept the total order quantity, the order’s flow will not be advanced.
OTQV must be attached to an outbound flow before COOR (Confirm Order).

SYSTEM ADMINISTRATION GUIDE 4.2* 203

CHOF screen showing total quantity of 1 pallet, 70 cases and 5 eaches on order

### Create Receipt from Order (CRCU) <a id="create-receipt-from-order-crcu"></a>

This special verify allows you to re-receive product on an outbound order as a new receipt. It is similar to a transfer order with one important difference: the receipt customer is the same as the order customer.
CRCU is normally attached to the flow COOR (Confirm Order).

### Mandatory Order Line Carton ID (MOCI) <a id="mandatory-order-line-carton-id-moci"></a>

This special verify checks that each order line has been assigned a carton ID. It is normally attached to the flow COOR (Confirm Order).
CHOF screen showing missing carton ID message

### Update Order To Ship Date (UOTS) <a id="update-order-to-ship-date-uots"></a>

This special verify sets the to ship date to the order confirmation date. if you do not use this special verify, the default to ship date is the order confirmation date plus one day.
UOTS must be attached to the flow COOR (Confirm Order).

### Order Charges (ORCH) <a id="order-charges-orch"></a>

This special verify allows you to add accessorial charges to an order. It must be attached to the outbound flow 
COOR in DIFP. If there are previously entered charges for the order, they will be displayed in the Detail Block.
If there are extra charges on the order, running ORCH will automatically generate and confirm the extra charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra charge audit and confirm the extra charge batch. 
ORCH
NOTE Extra charge batches created through ORCH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra charges on the extra charge batch are fully editable in ENAC.

SYSTEM ADMINISTRATION GUIDE 4.2* 205

### Receipt Charges (RECH) <a id="receipt-charges-rech"></a>

This special verify allows you to add accessorial charges to a receipt. It must be attached to the inbound flow 
CORE in DIFP. If there are previously entered charges for the receipt, they will be displayed in the Detail 
Block.
If there are extra charges on the receipt, running RECH will automatically generate and confirm the extra charge batch. That is to say, there is no need to generate the extra charge batch in BILB, print the extra charge audit and confirm the extra charge batch. 
RECH
NOTE Extra charge batches created through RECH do not display in BILB (Extra 
Charge Rater) and are not editable in that program. However, individual extra charges on the extra charge batch are fully editable in ENAC.

SYSTEM ADMINISTRATION GUIDE 4.2* 207
A
ActiveDesktop icons, assigning to users 74
ActiveDesktop Security Administrator (ADSA) 70
Adjust Entity Quantity Breakdown (AEQB) 150
Adjust Location Billing Code (ADLB) 157
Adjust Location Type (ADLT) 159
ADLB (Adjust Location Billing Code) 157
ADLT (Adjust Location Type) 159
ADSA (ActiveDesktop Security Administrator) 70 advanced queries 163
AEQB (Adjust Entity Quantity Breakdown) 150
ALDA (Change Date For All Companies) 160
Archive/Purge Processing (ARPU) 83 accessorial and immediate charges 87 inventory 85 looking up inventory to be purged 90 orders to be purged 88 receipts to be purged 89 overview 80 receipts and orders 83 the spooler files 96 warnings and messages 97
ARPU (Archive/Purge Processing) 83
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
COMP (Company Code) 6 companies, assigning program access to 46 companies, removing program access from 48
Company Access (COAC) 46
Company Code (COMP) 6 company setup 6
Conversion Exception Report (COER) 143 conversions 139 carrier details 127
COER (Conversion Exception Report) 143 consignee details 122
Conversion Exception Report (COER) 143 creating your csv files 104
DEPC (Data Extraction Process for Conversion) 144 existing locations 122 from a non-AccellosOne 3PL system 102 from AccellosOne 3PL system 144 inventory balances 134 item details 108 location details 118
LOCO (Load Conversion) 139
MOCO (Modify Conversion Data) 140
Modify Conversion Data (MOCO) 140 overview 102 performing 139
PRCO (Process Conversion) 141
Process Conversion (PRCO) 141 report 143 revenue master details 132 shipper details 125 transaction history details 129
ZIP codes 133
COOA (Copy Operator Access) 60
Copy Codes Between Companies (COCO) 187
Copy Items From One to Another (COIT) 149
Copy Operator Access (COOA) 60
CRCU (Create Receipt from Order) 203
Create Receipt from Order (CRCU) 203
D
Data Extraction Process for Conversion (DEPC) 144

DATE (Change Company Date) 160
DEAR (Delete Archive/Purge) 94
Delete Archive/Purge (DEAR) 94
DEPC (Data Extraction Process for Conversion) 144
E
Executable Job Code (EXJO) 36 executable job codes, looking up 45
EXJO (Executable Job Code) 36 expiry dates, resetting in REEX 161
F fax information, looking up in LOSP 168
IFFI (Interface From File) 190
IMAS (Item Mass Update) 189
INST (Installation Parameters) 75
Installation Parameters (INST) 75 inventory access code 50 item codes, copying in COIT 149
Item Mass Update (IMAS) 189
J
Job Selection Code (JOSE) 39
JOSE (Job Selection Code) 39
Load Conversion (LOCO) 139 location billing codes, adjusting in ADLB 157 location types, adjusting in ADLT 159 locks on programs 37 locks, clearing 148
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
Mandatory Receipt Carrier Details (MRCA) 200 menu structure 54
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
Operator Restrictions (OPRS) 62 operator setup 49
OPRS (Operator Restrictions) 62
ORCH (Order Charges) 204
Order Charges (ORCH) 204
Order Total Quantity Validation (OTQV) 202
OTQV (Order Total Quantity Validation) 202
P passwords for initial sign-on 49 resetting 53
PRCO (Process Conversion) 141
Process Conversion (PRCO) 141 program access assigning to users 54 removing users from 59 program locks 37 program setup 35 programs paths, looking up 43 programs, assigning to companies 46
Purge Warnings/Messages (PUWM) 99 purging and archiving performing the purge 94
PUWM (Purge Warning/Messages) 99
Q quantity breakdowns, adjusting in AEQB 150 queries, advanced 163
R
RATE (special verify for rating receipts) 86
Receipt Charges (RECH) 205
RECH (Receipt Charges) 205
REEX (Reset Inventory Expiry Date) 161
Reset Inventory Expiry Date (REEX) 161
Reset Operator Password (ROPA) 53 restricting user access 62
RF supervisors, setting up 52
Role (ROMA) 67
ROMA (Role) 67
ROPA (Reset Operator Password) 53
S
SAM (Supervisory Activity Management) 173 setting up companies 6 company access 46 programs 35 submenus 41 users 49 setup programs, overview 5 show inventory access code 50
Sort Sequence Code (SOSE) 169
SOSE (Sort Sequence Code) 169 special verification programs 194
