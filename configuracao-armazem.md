---
title: "Configuração — Armazém, Locais e Mensagens"
description: "Setup inicial, formato de armazém e localizações, tipos de local, zonas e mensagens."
layout: default
---

# Configuração — Armazém, Locais e Mensagens

Setup inicial, formato de armazém e localizações, tipos de local, zonas e mensagens.

**Fluxo principal:** `COMP -> WARE/LOCA/LOTP -> WHZO -> MESS/DEME`

> Fonte: manuais N do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction <a id="introduction"></a>

*Manual N — Setup Guide*

# Manual N — Setup Guide (Guia de Configuração Inicial)
> **ID do Manual:** N  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Configuração inicial do sistema: SKU, documentos, impressoras, armazéns, localizações, clientes, perfis de depositor, tarifas, perfis de item, mensagens. Programas principais: SKCL, SKUS, DONU, PRIN, WARE, LOCA, CUST, RATE, ITEM, DIFP, DSRP, DBIP, DILP, DIAP, ILOP, e dezenas de outros perfis de configuração.
---

### About This Manual <a id="about-this-manual"></a>

This manual provides basic setup instructions for AccellosOne 3PL. It contains all the mandatory programs that you need to set up plus the majority of commonly used optional programs. When you finish setup, you will be able to receive and ship product and perform most of the commonly used functions in AccellosOne 
3PL.
This manual is divided into eight sections. Because each program or system code builds on previously set up codes or programs, it is important to follow the order of programs as they are presented in this manual. If you attempt to skip mandatory programs, you will be unable to set up a program or profile presented later in the manual. 
▪ INITIAL SETUP (SKU classes and codes, printer codes, etc.)
▪ WAREHOUSE AND LOCATION SETUP (warehouses, locations, isolator zones, etc.)
▪ CUSTOMER PROFILE SETUP (flow steps, inventory levels, billing profiles, customers, etc.)
▪ CHARGE AND RATE SETUP (general ledger information, revenue analysis, charges, rates, etc.)
▪ MESSAGE SETUP (custom messages that can be attached to a customer, item, etc.)
▪ ITEM PROFILE SETUP (initial storage, renewal storage, quantity breakdowns, hold codes, etc.)
▪ ITEM SETUP (the main item record)
▪ MISCELLANEOUS SETUP (carriers, shippers, consignees, telephone numbers, etc.)

### Building Your System <a id="building-your-system"></a>

System setup in AccellosOne 3PL is a gradual process in which you build your system from the lowest level (system codes such as SKU types, billing terms, charge types, flow codes, etc.) to the next level (depositor profiles, item profiles, flow profiles, etc.) to the highest level (customers and items), which are the main programs in AccellosOne 3PL. 
For example, you have a minimum renewal charge for a particular item in your warehouse. First, you define a charge code for your minimum renewal charge in CHAR, next you attach this charge code to your renewal storage profile, and then you attach the renewal storage profile to your item billing profile. Lastly, you attach the item billing profile to the appropriate item. 
CHAR IRSP IBIP ITEM
Create a charge code
Attach the charge code to a renewal storage billing profile
Attach the IRSP billing profile to the item billing profile
Attach the IBIP profile to the item

### Using Profiles <a id="using-profiles"></a>

AccellosOne 3PL uses profiles to group related information about billing, items, item location, shipping, quantity breakdown, etc. A profile is merely a series of options grouped under a profile code. When a given profile code is attached to a particular customer or item, all the options of that profile code automatically apply to the customer or item. 
Profiles make it easy to change large numbers of customers or items by means of a single change to one program. For example, if you set up a standard billing profile for all your customers, you can change your billing for all customers by making the change once in the profile rather than individually for each of your customers.
Although you can set up as many profiles as you want (for example, a separate profile for each of your customers), such an approach is seldom recommended. Generally, you want to minimize the number of your profiles as much as possible. If all your customers are billed in the same way, there is no need to set up more than one billing profile. 

### Global Versus Unique Programs <a id="global-versus-unique-programs"></a>

There are two types of programs in AccellosOne 3PL: global and unique. A global program is a program in which once you set up a system code or a profile, it can be shared across companies, warehouses, customers, etc. For example, SKUS (Stock Keeping Units) is a global program. If you set up a SKU in this program (for example, a SKU called CASES), you can use CASES in any warehouse, company or customer on your system. 
ITEM, on the other hand, is a unique program. Items created in ITEM are customer specific; they cannot be shared or accessed across companies or other customers.
To share global programs across companies, you must set the Global Code field in COMP (Company Code) 
to the same value for all companies whose codes and profiles you wish to share. For example, if you assign the global code of 00 to companies W1 and W2 and assign the global code 01 to companies W3 and W4, companies W1 and W2 will share one set of global codes and profiles while companies W3 and W4 will share a separate set of global codes and profiles. 
Global Code = 00
COMPANY 1
Global Code = 00
COMPANY 2
Global Code =
COMPANY 3 codes and profiles shared between companies no sharing of codes and profiles between companies

Company Code (COMP) screen for company W1 showing Global Code set to 00
 For your test or training company, you should always leave the Global Code field blank so that test codes and profiles do not get mixed up with your live customers and items. For your live companies, on the other hand, you can assign global codes to them if required so that your live codes and profiles are available for use in other live companies.
T1 (Sample Company 1)
Global Code = 00
T2 (Training Company 2)
Global Code = 
W1 (Live Company)
Global Code = 00
EXAMPLE 1
You create a SKU type of CASES in T1 using the program SKUS.
CASES set up in T1 are not available for use in any T2 program because global code in T2 does not match global code in T1.
CASES set up in T1 are available for use in all W1 programs because global code in W1 matches global code in T1.
EXAMPLE 2
You create an isolator code of FISH in T2 using the program ISOL.
FISH set up in T2 are not available for use in any T1 program because global code in T2 does not match global code in T1.
FISH set up in T2 are not available for use in any W1 program because global code in T2 does not match global code in W1.

### Status of Codes and Profiles <a id="status-of-codes-and-profiles"></a>

The majority of codes and profiles have a Status field used to indicate their status. There are two possible statuses for a code or profile:
▪ Active
▪ Deactivated
You deactivate an active code or profile by clicking on Delete. You activate a deactivated code or profile by entering A in the Status field and pressing Enter. You can activate and deactivate the same code as many times as you wish.

### Updating Records in the Database <a id="updating-records-in-the-database"></a>

When you create or modify a record in any setup program, the changes that you make only take effect when you click on Exit to exit the program. If you do not click on Exit to exit the program, other operators on your 
AccellosOne 3PL system will only have access to the old information.
For example, if you make a change to an item description in ITEM but do not click on Exit to exit, any other user receiving or shipping the item will receive or ship the item with its old description. 
NOTE Once you assign a global code in COMP to a particular company, you cannot change it. Should you make a mistake and need to reset the flag, contact your HighJump consultant for assistance.
Active An active code or profile is a normal code or profile that can be used in any setup or operational program. For example, an active item can be shipped, received and adjusted like normal inventory and can be attached to another profile. 
Deactivated A deactivated code or profile can be shipped and adjusted like normal inventory but cannot be received. Nor can it be attached to another profile. For example, if you deactivate an item, you cannot receive new inventory for this item, but existing inventory remains unchanged and can be shipped and adjusted like normal inventory.

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting reports
Introduction Guide logging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating product, entering hold adjustments
Operations 2 Guide appointment planner, back orders, batch picking, manual packing, customer relationship management, EDI, faxing and auto-printing, item substitution, kitting, labor tracking, Operational Board, pallet control, inventory attributes, item process values, outbound load building, quick response labels
Physical Inventory 
Guide setup and operational programs for physical inventory as well as the physical inventory reports
RF Guide setup programs for RF (Radio Frequency), RF receiving, RF picking, entering process values in RF, voice-activated picking, order assignment system, equipment tracking, tasking, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

## Initial Setup <a id="initial-setup"></a>

*Manual N — Setup Guide*

### Before You Begin <a id="before-you-begin"></a>

The following codes must be created in AccellosOne 3PL before you can perform setup:
▪ an “NA” (Not Applicable) invoice type in INTP 
▪ a “no charge” type charge code in CHAR
▪ an inventory terminology code of ITEM in INTE
▪ a dummy general ledger account in GLCH
▪ a currency in CURR
▪ a bank code in BANK
▪ six document types in DOTP
The above codes may or may not be available to the company that you are setting up depending on the type of company that you are creating (“global” or “unique”) and whether other companies have already been set up on your system. 
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
8 In the Trade GL Account field, key in the same dummy account that you created in the previous procedure and press Enter. 
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

### SKU Class (SKCL) <a id="sku-class-skcl"></a>

OVERVIEW
In this program, you review your SKU classes. SKU classes are required when you define your SKU types in 
SKUS (Stock Keeping Units). 
The purpose of SKU classes is to define the type and relative size of each SKU type. For example, suppose you have one SKU type called CARTONS for Customer 1, another SKU type called BOXES for Customer 2 and a third SKU type called CASES for Customer 3. Because all three SKU types are essentially the same thing, you assign them the SKU class of CASE (cases and the like) as a way of grouping them. This allows 
AccellosOne 3PL to differentiate these SKU types from pallets, which would have their own SKU class.
PREREQUISITES: None
ATTACHED TO: SKUS (Stock Keeping Units)
PIPR (Picking Profile)
LOAD (Load Type)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

SKU classes allow you to define in PIPR (Picking Profile) what constitutes a partial quantity. A partial quantity in AccellosOne 3PL is defined as a quantity that is less than a full SKU class and not the highest SKU class. 
For example, if you have a PALLETS/CASES account and your SKU classes are 1 for pallets and 3 for cases, then a partial quantity would be any number of cases not making up a full pallet. Partial quantities are used in the allocation routine when you specify whether or not you want AccellosOne 3PL to clean up locations containing partial quantities.
There are five predefined SKU classes in AccellosOne 3PL. These classes are ranked by size with the largest items (usually pallet) being assigned the lowest number. If you wish to change these predefined classes, you type over the information that you wish to change.
The sixth SKU class (Other) is used for SKU codes like LBS, KGS, HR and OCCURRENCE, which do not have a size.
PROCEDURE
1 Enter SKCL.
2 Review the predefined SKU classes.
FIELD DESCRIPTIONS
Class Number This number is set up by HighJump and cannot be altered. 
Description The long description of the SKU class. You can change the long description by keying in a new one over the old one and pressing Enter. 
Short Description The short description of the SKU class. The short description of the SKU class appears on certain screens and reports where there is insufficient space to show the long description.

3 If you wish to change either a long description or short description, press Enter until your cursor is positioned in the field that you wish to change. Then key in a new long or short description and press Enter.
4 When you finish making your changes, click on Exit. If you are in modify record mode, click on Return to 
Main and then Exit.

### Stock Keeping Units (SKUS) <a id="stock-keeping-units-skus"></a>

OVERVIEW
In this program, you define the SKU codes that you wish to use for tracking product and billing your customers. A SKU code is anything in your warehouse that you wish to track and/or charge for. SKU codes can be physical objects (such as bags, boxes, cases, units, pallets, drums, etc.), units of measure (such as pounds, hundredweights, tonnes, hours, meters, cubic inches, etc.) or a service that you wish to charge for (for example, a bill of lading).
There are four main functions in SKUS:
▪ you define the SKU code itself (bags, boxes, pounds, pallets, cases, etc.)
▪ you define how the SKU code is counted (by weight, number of units, etc.)
▪ you define the SKU class (how big is the SKU code compared to other SKU codes)
▪ if you are setting up a multiple SKU such as hundredweight, you must define the “divide by” value (for example, 1 hundredweight = 100 pounds) 
You can set up one SKU code for each non-pallet item in your warehouse (for example, bag, box, case, carton, etc.) or simply use pallets/cases as the standard quantity breakdown for all your customers. Separate 
SKU codes for each non-pallet item are only required if your customers need their own terminology on invoices and reports.
PREREQUISITES: SKCL
ATTACHED TO: CHAR (Charge Codes)
IQBP (Item Quantity Breakdown Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all your SKU codes

FIELD DESCRIPTIONS
SKU Code Mandatory
Your SKU code. For example, PLT for pallet or CSE for case.
CAUTION: AccellosOne 3PL does not support single-letter SKU codes such as C for Case or P for Pallet. Not does it support multi-letter codes in which one code can be embedded in another. For example, you cannot have 
CASE for Case and CA for Carton because CA can be embedded in CASE.
Description Mandatory
Your SKU code description. For example, “Pallets.”
Qualifier Code Mandatory
The way in which the SKU code is counted. If the SKU code is a physical object (for example, pallet, case, each, drum, bag, etc.), use UNIT. If the SKU code is a container that may hold partial quantities (for example, tote), you can use either UNIT or WGTG/WGTN. If the SKU code is weight based (for example, pounds, kilos, hundredweights, tons, etc.), use either WGTG or WGTN.
The following qualifier codes are supported in AccellosOne 3PL:
CUBE = Cubic Measure
HOUR = Hour*
OCCR = Occurrence*
UNIT = Unit
WGTG = Gross Weight
WGTN = Net Weight
* See the Billing and Invoicing Guide for further information on using these qualifier 
codes to set up one-time flat rate charges and hourly based charges.

PROCEDURE
1 Enter SKUS.
2 Click on Enter Criteria then Execute Query to view your existing SKU codes.
3 Using your arrow keys, go through each record to see which SKU codes have already been set up. If the 
SKU codes that you require have already been set up, click on Exit. There is no need to add any new codes to SKUS.
SKU Class Description (SKCL)
Mandatory
For SKU codes that are physical objects with a size, use your regular SKU classes (Eaches and the like, Cases and the like).
For all other SKU codes (that is, those based on weight, occurrence, hour, etc. 
that do not have a size) use Others. When you assigned a SKU class of Others to a SKU code, you cannot have AccellosOne 3PL pick partial quantities of this SKU code in ILOP (Item Location Profile).
Value Mandatory
The value is usually 1 with the following exceptions: 
▪ If you are using the following weight-based SKU Codes — CWT, CKGS, 
MTON and TON — you must specify the appropriate value to convert the 
SKU to either pounds or kilos. For example, for CWT the value will be 100 and for MTONS (metric tonnes) the value will be 2200.
▪ If you are using cubic inches, enter .000579 as your value.
▪ If you are using kilograms, enter 2.2045855 as your value.
Base SKU Code Optional
Refer to “Billing by Multiple Units of a SKU” in the Billing and Invoicing Guide.
FIELD DESCRIPTIONS

SKU Code for cases
4 If the SKU codes that you require have not been set up, click on Create Record.
5 Key in your new SKU code and press Enter.
6 Key in a meaningful description for the new code and press Enter.
7 Key in your qualifier code and press Enter.
To select other qualifier codes, you can use the pick list function. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
8 Key in your SKU class description and press Enter. If the SKU code is weight based, use Others as your class description.
To select a SKU class description, use your pick list.
For most physical objects: For weight-based SKU’s:
a) Use UNIT. a) Use the appropriate code for weight-based SKUS.

SKU Code for hundredweight
9 Key in your value and press Enter.
10 When you finish setting up your SKU code, click on Return to Main and then Exit.
For most UNIT-base SKU codes:
For weight-based or cube-based 
SKU codes:
a) Use 1 as your value. a) Enter the appropriate value.
CAUTION If you are creating a weight-based SKU code such as CWT, CKGS, 
MTON (metric tonne) or TON, you must have a SKU code on your system for pounds (in the case of CWT and TON) and/or kilograms (in the case of CKGS or MTON). If you fail to define your pounds or kilos, your system will not be able to rate or bill properly.

### Document Numbers (DONU) <a id="document-numbers-donu"></a>

OVERVIEW
In this program, you define the format of your document numbers for each document type set up in AccellosOne 3PL. Accessorial invoice, renewal invoice, order number and receipt number are some of the document types that you define in DONU. For each document type you must specify the prefix, starting number and ending number of your block of numbers. As an option, you can also define a suffix for your block of numbers. 
Once set up, blocks of numbers are final and cannot be changed. You can, however, change the prefix.
PREREQUISITES: None
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE When working with multiple companies, you cannot use the same number series and prefix for two or more companies. You must change either the number series or the prefix of your block of numbers to accommodate the second company.

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
Order, etc.), the current year or any other series of letters or numbers except the dash character (-). If you use the current year as your prefix, you must remember to change it every year.
If you are working with multiple companies, you cannot use the same number series and prefix for two or more companies. You must change either the number series or the prefix of your block of numbers to accommodate the second company.
Current Number Mandatory
Your current number.
Start Number/End Number
Mandatory
The starting and ending number for your block of numbers. When AccellosOne 3PL reaches the end of your block of numbers, it will restart at the value that you define in the Start Number field.
NOTE Small ranges (for example, a starting number of 100 and an ending number of 200) are not recommended. If you must use a small range, make sure that you purge your inventory on a regular basis. If you fail to do so, you might have two open receipts with the same receipt number.

PROCEDURE
1 Enter DONU.
2 If required, click on Detail Block.
3 Key in your prefix and press Enter. You can use a single letter as your prefix (for example, A for Accessorial, O for Order, etc.), the current year or any other series of letters or numbers. If you use the current year as your prefix, you should remember to change it every year.
4 Key in your current number (usually 1) and press Enter.
5 Key in your start number (usually 1) and press Enter. Your start number must always be less than or equal to your current number.
6 Key in your end number (usually the default of 999999) and press Enter.
7 Key in your suffix and press Enter or press Enter with the field blank for no suffix.
8 Click on Return to Main to return to the main block.
Document Numbers screen
9 To set the number series for another document type, arrow down to the document that you wish to set up and click on Detail Block.
10 Repeat steps 3 to 8 for each document type that you wish to set up.
Suffix Optional
Your suffix (up to four characters in length).
FIELD DESCRIPTIONS

11 When you finish setting up your document types, click on Exit to exit the program. If Exit is not available, click on Return to Main and then Exit.

### Printer Code (PRIN) <a id="printer-code-prin"></a>

OVERVIEW
In this program, you set up the printers that you will be using in AccellosOne 3PL to print your labels, documents, physical inventory tickets, reports, etc. There are seven predefined “printers” set up in AccellosOne 3PL: AFAX, BAR, EXCL, FAX, MAIL, SPL and VIEW. These printers are set up by HighJump and cannot be modified or deleted.
Before you set up your printers in AccellosOne 3PL, you must first set up the printers in Unix and use the same Unix printer codes in PRIN.
PREREQUISITES: None
ATTACHED TO: LPPR (Location Print Profile) --> (LOCA)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: Your printer code as defined in Unix
FIELD DESCRIPTIONS
Printer Code Mandatory
Your printer code in AccellosOne 3PL. Your AccellosOne 3PL printer code need not be the same as your Unix printer code.
Description Mandatory
Your printer code description.
System Printer Code Mandatory
Your printer code as defined in lpstat in Unix for raw drivers.

System Alternate Printer 
Code
Optional
An alternate system printer code. For example, your print queue for postscript/
PDF outputs.
Printer Size Only available for non-PDF printing
S = Small
R = Regular
If you select S for Small, any document that is wider than 80 characters will be compressed. If in fact the document that you are printing is less than 80 characters across, no compression will occur. Therefore, if there is any possibility of an item requiring compression, it is recommended that you select the Small option.
If you select R for Regular, no compression will occur and the document will be printed as is.
Command Type Optional p = Pipe (sends the print job to a printer)
c = Command (executes a Unix command)
d = Device (data sent to a defined device)
f = Fax (reserved for future use)
e = E-Mail (reserved for future use)
Your command type.
Command Optional
When you output to a printer using the command type of p, there are two command options:
lp -d $sys_prt_code..........................................................output to a printer dd of=/directorypath/filename .............................................. output to a file
FIELD DESCRIPTIONS

PROCEDURE
1 Enter PRIN.
2 Click on Enter Criteria then Execute Query to see which printers have already been set up.
Print Profile Code (PRPF) Optional
This code is set up by HighJump. It allows you to print document overlays using printer macros.
IP Address / Printer 
Name for BarTender Software
See the Core Documents Guide.
Compress Escape 
Sequence
Optional
You can specify any Unix lp command (for example, use font 123) that is valid for the printer that you are printing on.
Reset Escape Sequence Optional
You can specify any Unix lp command (for example, use font 123) that is valid for the printer that you are printing on.
Reference IP Address Optional
External information for reporting purposes.
Reference Model 
Description
Optional
External information for reporting purposes.
FIELD DESCRIPTIONS

3 Using your arrow keys, go through each record to see which printers have already been set up. If the printers that you require have already been set up, click on Exit. There is no need to add any new codes to PRIN.
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
13 In the Compress Escape Sequence and Reset Escape Sequence fields, key in your Unix lp option and press Enter or press Enter with the field blank to bypass the field. 
14 When you finish setting up your printer, click on Return to Main and Exit to exit the program.

### Country Codes (CNTY) <a id="country-codes-cnty"></a>

OVERVIEW
In this program, you set up your country codes. Country codes serve two purposes in AccellosOne 3PL. First, they allow you to record the country in which an item was manufactured. Second, they allow you to define the format of and the valid characters in your ZIP and postal codes for that country (Classic only).
AccellosOne 3PL supports both fixed length and variable length postal codes. It also supports multiple postal code formats when a country is switching from one format to another (for example, the five-digit and nine-digit 
ZIP codes in the US).
You define your postal code by means of “partitions”. A partition is a distinct part of a code that always contains a certain character or type of character. For example, if the first character of your code is always a letter and the second character is always a number, you would set up two partitions: partition 1 would be defined as letters only and partition 2 would be defined as numeric only.
AMERICAN ZIP CODE 
The American five-digit ZIP code is all numeric and consists of a single partition.
EXAMPLES
PREREQUISITES: None
ATTACHED TO: STPR (State(s)/Province(s))
ZIPO (Zip/Postal Codes)
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

02356
68734
CANADIAN POSTAL CODE 
The Canadian postal code is divided into seven fixed-length partitions. The space between the first and last three characters is defined as a partition and assigned the ^ character to indicate a blank space.
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
3 1 Y 0123456789
4 1 Y 0123456789^
5 1 Y 0123456789^
6 1 Y ABCDEFGHJKLMNPQRSTUVWXYZ0123456
7 2 N ABCDEFGHJKLMNPQRSTUVWXYZ

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
If the country has two ZIP or postal code formats (for example, the five-digit and nine-digit ZIP code in the US), you must create two breakdowns. If the country has a single ZIP or postal code format, create a single breakdown. 
Description Mandatory
Your breakdown description.
FIELD DESCRIPTIONS
Partition Number Mandatory 
If your postal code can be broken down into distinct parts (for example, 
AB1234), you can create multiple partitions and define each partition separately. If your codes are uniform (for example, always numbers), you need only define a single partition.

PROCEDURE
1 Enter CNTY.
2 Click Enter Criteria then Execute Query to retrieve your country codes. When the first country code is displayed, use your down arrow key to see which countries have already been set up.
Length of Partition Mandatory 
The number of characters in the partition that you want AccellosOne 3PL to do validation on. If you set the Exact Length field to No, you can create postal codes that exceed the Length of Partition value. However, no validation will occur on these extra characters.
Exact Length Y = Yes
N = No (only available for last partition in code)
If the partition is always the same length (for example, the first character of your code is always a letter), set this flag to Yes. If the partition is not always the same length (for example, your code can begin with one or two characters that are always a letter), set this flag to No.
If you set this flag to Yes, AccellosOne 3PL will perform validation on all characters in the code. If you set this flag to No, AccellosOne 3PL will perform validation on the number of characters that you entered in the Length of Partition field. You can add extra characters to a ZIP or postal code, but no validation on these extra characters will be performed.
Valid Characters Mandatory 
The characters that you can use in your ZIP or postal code. Valid characters can be numbers, letters or special characters.
FIELD DESCRIPTIONS

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
14 If you wish to create a second breakdown, click on Breakdown Block and then Create Record. Then repeat steps 7 to 13 for your second breakdown. If you do not need a second breakdown, click on Return to Main and then Exit.

Country Codes screen for the US

### States/Provinces (STPR) <a id="states-provinces-stpr"></a>

OVERVIEW
In this program, you set up your state and province codes. You use these codes to record the postal address of your companies, warehouses, customers, carriers, consignees, shippers and sold-to’s. State and province codes print on any AccellosOne 3PL document containing an address.
If you do not need states or provinces for a county because the country does not have them or they are unimportant to your business, create a single code like OS for Overseas.
PREREQUISITES: None
ATTACHED TO: ZIPO (Zip/Postal Codes)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

PROCEDURE
1 Enter STPR.
2 Click on Enter Criteria then Execute Query to retrieve your state and province codes. When the first code is displayed, use your down arrow key to see which states and provinces have already been set up.
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

6 Select your country from the dropdown list.
7 Key in a description for your state or province code and press Enter.
8 Repeat steps 5, 6 and 7 for each additional state or province that you wish to add.
9 When you finish adding your states and provinces, click on Save to save your changes.
10 Click on Exit to exit the program.

### ZIP/Postal Code (ZIPO) <a id="zip-postal-code-zipo"></a>

OVERVIEW
In this program, you set up your ZIP and postal codes. ZIP and postal codes are a mandatory field in all 
AccellosOne 3PL programs with an address such as WARE, CUST, CARR, etc. In ZIPO you attach your ZIP or postal codes to the city and state or province to which they belong. Because ZIP and postal codes are always linked to the appropriate city and state/province, you can enter the ZIP code of a customer in CUST and the city and state fields are automatically filled in by AccellosOne 3PL based on the information that you set up in ZIPO.
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

PROCEDURE
1 Enter ZIPO.
2 Click on Enter Criteria then Execute Query to retrieve all your ZIP/postal codes. To look up a specific code, first click Enter Criteria. Then key in your country code and press Enter. Lastly, key in your ZIP/ postal code and click Execute Query. 
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

9 When you finish adding your ZIP or postal codes, click on Return to Main and then Exit.

## Warehouse Setup <a id="warehouse-setup"></a>

*Manual N — Setup Guide*

### Warehouse & Location Format (WARE) <a id="warehouse-location-format-ware"></a>

OVERVIEW
In this program, you set up your warehouse (a warehouse code plus the address) as well as the format of your locations in that warehouse (the number of characters in the location code and the format of each character — letter, number, special character, etc.). 
A warehouse is a logical entity containing locations for the receiving, storage, picking and shipping of product. 
A warehouse can correspond to a single physical building and contain all of the locations in that building. 
Alternatively, a warehouse can correspond to a room, floor or special area within the same building and contain all of the locations within that part of the building. Multiple warehouses in the same building are recommended when you wish to generate reports showing the availability of product by room or area, which parts of your warehouse are full, etc.
PREREQUISITES: CNTY, ZIPO, STPR
ATTACHED TO: LOCA (Locations)
ILOP (Item Location Profile)
WHZO (Warehouse Zone Codes)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The address of the warehouse and the format of its locations
FIELD DESCRIPTIONS
Warehouse Code Mandatory
Your warehouse code. For example, W1 for warehouse 1. A warehouse code can consist of any combination of numbers or letters up to four characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” 
may cause problems in certain programs and are not recommended. Other special characters are generally supported.
Description Mandatory
Your warehouse code description.

Address 1/2/3/4 Mandatory
The address of the warehouse.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (ZIP/Postal Code), the city, state/province and country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
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
Warehouse Labor Capture Flag
Reserved for future use
FIELD DESCRIPTIONS

Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
External Reference Number
Optional
You can add any miscellaneous reference information about a warehouse in this field.
Establishment Number Reserved for future use
Country Code - Origin Reserved for future use
Location Codes Must 
Conform to Location Definition
Y = Yes
N = No
If you select Yes, locations created in LOCA must follow the format set up in the Location Definition Block for that warehouse. If you select No, you can override the format set up in the Location Definition Block for that warehouse.
Default Location Code (LOCA)
If you create a new location in ENRE, it will inherit the properties of the location code that you enter in this field.
Voice Check Digit Usage See the section on Voice Activated Picking and Order Assignment System in the RF Guide.
Days of the Week for 
Check Digit 1/2/3
See the section on Voice Activated Picking and Order Assignment System in the RF Guide.
LOCATION DEFINITION BLOCK
Character Position Mandatory
The position of the character whose valid characters you are defining.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter WARE.
2 Key in your warehouse code (for example, W1) and press Enter.
3 Key in the name and address of the warehouse, pressing Enter at the end of each line.
4 In the ZIP Code field, key in the warehouse’s ZIP code and press Enter. 
If the code that you enter is new and not yet on the system, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into WARE with the appropriate information filled in.
5 In the Length of Location Code field, key in the exact number of characters used in your warehouse’s locations and press Enter. For example, if the locations in your warehouse are set up as 1A123B, you would key in a field length of 6. If, on the other hand, the locations in your warehouse are set up as 
1A123, you would key in a field length of 5.
Valid Characters Mandatory
The valid characters for this character position. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.
LOCATION DEFINITION BLOCK

Warehouse and Location Format
6 Press Enter to bypass the Fax Cover Sheet field.
7 Press Enter twice to bypass the Building Code and Directed Move Profile Code fields.
8 Key in N for No in the Warehouse Labor Capture Flag and press Enter.
9 Press Enter to bypass the Labor Standard Modifier field.
10 If required, key in your external reference number and press Enter or press Enter with the field blank to bypass the External Reference Number field.
11 Press Enter the required number of times to bypass the remaining fields in WARE.
12 When the Location Definition Block is displayed, enter the valid characters for each character in your location. You press Enter at the end of each line to advance the cursor to the next line.

Location Definition Block with six characters
The above sample screen illustrates the following: 
Some valid locations based on the above definition are:
0AB-A8
8Z9-DC
If you tried to enter the code 0AB-A in LOCA (the program where location codes are set up), it would be rejected because it is only five characters long and this warehouse requires a six-character code. If you tried to enter AZ9-DC, it would be rejected because the first character is a letter and you have defined the first character as a number.
13 When you finish defining your locations, click on Master Block then Exit to exit the program.
CHARACTER 
POSITION VALID CHARACTERS
1 0-9 or any number
2 A-Z or any letter
3 0-9 + A-Z any number or letter
4 only the special character “-”
5 only the letters A, B, C, D, E and K
6 only 8 and C

LOCATION ATTRIBUTES BLOCK
In this block, you define the aisles, bays and odd/even positions of your warehouse. You define aisles, bays and odd/even positions by specifying which character(s) in your location codes define an aisle, bay or odd/ even position. For example, if your location codes are four characters in length and the first character indicates the aisle, locations A100, A101 and A200 will be considered part of aisle A, while locations B100, 
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
The starting position for your aisle, bay or odd/even position. For odd/even positions, the starting position must be numeric.
End Position Mandatory
The ending position for your aisle, bay or odd/even position. For odd/even positions, the ending position must be the same as the starting position.

WARE screen showing aisle defined as first character in location code and odd/even position defined as fourth character of location code

### Location Billing Codes (LODE) <a id="location-billing-codes-lode"></a>

OVERVIEW
In this program, you set up your location billing codes. Location billing codes are a means of grouping your warehouse locations for billing and revenue analysis purposes.
For example, you can set up location billing codes for all locations, dry storage, the cooler area, etc. By setting up these codes, you can set different rates of storage for different areas in your warehouse and you can track the revenue generated by each of these storage areas.
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
IISP (Item Initial Storage Profile) --> ITEM
IRSP (Item Renewal Storage Profile) --> ITEM 
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you wish to make changes to a location billing code after attaching the code to locations in LOCA, you must run ADLB (Adjust Location Bill 
Code). You cannot modify a location billing code in LOCA. 
See the System Administration Guide for further instructions on using 
ADLB.
OTHER REQUIREMENTS: A list of the different storage areas in your warehouse

In the program LOCA, each location billing code is attached to the specific location that it represents and any product stored in these areas will be billed accordingly.
EXAMPLE
Product stored in the cooler area such as film is charged $4.00 per case
Product stored in a high value area is charged $3.75 per case
Product stored in the general warehouse area is charged $3.00 per case
If you do not charge different storage rates based on the area in which the product is placed and do not track revenue by area, you do not need location billing codes.
FIELD DESCRIPTIONS
Code Mandatory
Your location billing code. For example, DRY for dry.
Description Mandatory
Your billing code description.
Renewal Calc. by OPID See the Billing and Invoicing Guide.
ITEM
IISP
LODE
When the location billing code of the item matches the location billing code of the location, the item is billed the appropriate initial and renewal storage rates.
IRSP
LODE
LOCA
LODE item being putaway into location
IBIP
CHAR CHAR

PROCEDURE
1 Enter LODE.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
Location Billing Codes
3 If you need to set up another code, click on Create Record.
4 Key in your code (for example, DRY) and press Enter.
5 Key in a description and press Enter.
6 Press Enter to bypass the G. L. Modifier Code field.
Refer to the program [General Ledger Modifier Code (GLMO)](faturamento-setup.html#general-ledger-modifier-code-glmo) for further information on general ledger modifiers.
7 Repeat steps 4 to 6 for your next location billing code or click on Return to Main and then Exit.

### Isolators (ISOL) <a id="isolators-isol"></a>

G. L. Modifier (defined in GLMO)
Optional
Refer to the program GLMO in Part 4 of this manual for information on general ledger modifiers.
Description Defined in GLMO.
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
ILOP (Item Location Profile) --> ITEM
PUPR (Put-Away Profile Code) --> DSRP 
FIELD DESCRIPTIONS

OVERVIEW
In this program, you set up your isolator zones. Isolator zones serve two key functions:
▪ They allow you to keep certain products separate from each other within the same area. For example, you keep both fish and cheese in your cooler area but for obvious reasons you do not want both products sitting side by side in the same location or adjacent locations. Isolator zones allow you to keep both products separate from each other.
▪ They allow you to keep similar product together. When similar product is kept together, you avoid a situation where product is dispersed in numerous locations in your warehouse and as a consequence is time-consuming and expensive to pick.
You attach isolator zone codes to your locations in the program LOCA (Locations) and to your products in the program ILOP (Item Location Profile).
ISOL is intended for systems set up with directed put-away. If you are performing your put-away manually, you do not need isolator zones and should set up one isolator on your system called N/A (Not Applicable).
ISSUES TO CONSIDER WHEN SETTING UP ISOLATORS
Before setting up your isolator zones, you should give serious thought to how you want to divide up the space in any given area of your warehouse. For example, you can break up an area by customer:
▪ Customer A
▪ Customer B
▪ All others
In this example, you have two major customers (Customer A and Customer B) and you wish to keep their products in separate areas of the warehouse. Your other customers are not major and you don’t care whether their products are all mixed up together.
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: You must know which items or customers you wish to keep separate and how you want to define your overflow areas location 1 fish location 4 fish location 7 cheese location 10 cheese location 13 other products location 16 other products location 2 fish location 5 fish location 8 cheese location 11 cheese location 14 other products location 17 other products location 3 fish location 6 fish location 9 cheese location 12 cheese location 15 other products location 18 other products
Isolator 1 Isolator 2 Isolator 3

You could also break up an area in your warehouse by product:
▪ Chemicals/Hazardous Goods
▪ Food Stuffs
▪ Other
This example illustrates a scenario whereby you wish to group certain products together regardless of the customer to whom they belong.
You could also break up an area in your warehouse by how fast a product moves:
▪ Fast-Moving Items
▪ Medium-Moving Items
▪ Slow-Moving Items
Three isolator zones for meat: fast-moving, medium moving and slow-moving
OVERFLOW ISOLATORS
Isolator zones can also have one or more designated overflow isolators assigned to them. When you receive product and all locations in the isolator zone for that product are full, AccellosOne 3PL will allocate the product to the first overflow isolator. If the first overflow isolator is full, AccellosOne 3PL will attempt to allocate product to the second overflow isolator (if any). You can define multiple overflow isolators for the same item and specify the sequence in which AccellosOne 3PL will query isolator zones in search of empty locations. 
location 1 meat fast-moving location 4 meat medium-moving location 7 meat slow-moving location 2 meat fast-moving location 5 meat medium-moving location 8 meat slow-moving location 3 meat fast-moving location 6 meat medium-moving location 9 meat slow-moving
Isolator 1 Isolator 2 Isolator 3

Three isolator zones for meat that progressively overflow into the fourth zone (Meat Overflow)
When the last overflow zone is filled, AccellosOne 3PL will prompt you to enter a location manually.
The number of isolator zones to set up will depend on the layout of your warehouse, the number of customers and items, the extent to which product must be kept separate and the types of overflow that you allow. It is necessary to strike a balance between too few isolators (AccellosOne 3PL has to search a large number of locations in directed put-away and consequently performance is poor) and too many isolators (similar product is unnecessarily separated into narrowly defined categories that are overly specific). 
ISOLATORS AND ILOP
The following graphic shows how AccellosOne 3PL uses isolators and ILOP parameters to assign locations to product.
location 1 meat fast-moving location 4 meat medium-moving location 7 meat slow-moving location 10 meat overflow location 2 meat fast-moving location 5 meat medium-moving location 8 meat slow-moving location 11 meat overflow location 3 meat fast-moving location 6 meat medium-moving location 9 meat slow-moving location 12 meat overflow
Isolator 1 Isolator 2 Isolator 3 Isolator 4
NOTE When two products with different isolator zones are assigned the same overflow location, the products may be stored in the same location and you lose the benefit of isolator zones. Therefore, if two products should never mix, you must set up separate overflow zones for each one.
OVERFLOW OVERFLOW OVERFLOW

PROCEDURE
1 Enter ISOL.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
FIELD DESCRIPTIONS
Isolator Code Mandatory
Your isolator code. For example, MTF for meat fast moving.
Description Mandatory
Your isolator code description.
Overflow Sequence Number
Optional
The sequence of the overflow isolator code.
Overflow Isolator Code Optional
The overflow isolator code.
ITEM
ILOP
ISOL
Depending on your parameters defined in
ILOP, AccellosOne 3PL will ignore, use an exact match or use an overflow isolator when picking or putting away product.
LOCA
ISOL item being put-away into or picked from location

3 If you need to set up another code, click on New.
4 Key in your isolator code and press Enter.
5 Key in a description for your code and press Enter.
6 Do one of the following:
7 Click in the Overflow Sequence field.
8 Key in your sequence number (1) and press Enter.
9 Key in your isolator code for sequence number 1 and press Enter.
10 Repeat the above three steps for each additional overflow area that you wish to add. Each additional overflow area must be assigned the next available sequence number.
Isolator MT1 with three overflow areas assigned to it
11 When you finish adding your overflow sequences, click on Save to save your new isolator.
12 Key in another isolator code and repeat the above steps or click on Exit twice to exit the program.
HAZARD CLASS TAB
In this tab, you set up your hazardous class restrictions. That is, which hazardous classes cannot be mixed together. 
When you put-away, relocate or adjust product into a location and the location’s hazardous class restrictions match the item’s hazardous class (for example, explosives 1.1 is mixed with explosives 1.2), AccellosOne 
If you wish to assign an overflow area to the isolator:
If you do NOT wish to assign an overflow area to the isolator:
a) Proceed to next step. a) Click on Save to save your new isolator.
b) Click on Exit to exit ISOL.

3PL will write a record to the hazardous restriction violation table in the database. Using d’Amigo, you can run queries and generate alerts to report on these violations.
Isolator A with three records in the Hazard Block

### Location Print Profile (LPPR) <a id="location-print-profile-lppr"></a>

OVERVIEW
This program allows you to “split” certain documents among two or more printers based on the location of the item. For example, if your warehouse has three different printers at different doors and you are processing an 
PREREQUISITES: DOCU (set up by HighJump), PRIN
ATTACHED TO: LOCA (Locations)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A list of all printers in your warehouse and the documents that can be “split” among these printers

order, LPPR allows you to print three separate pick documents at three different printers so that documents are always printed on the closest printer.
If you do not need to split documents among two or more printers, you do not use this program.
You need to set up one print profile for each printer that is to accept split documents. Each profile should contain the document code for all documents that you want to print on that printer. When you finish setting up your location print profiles, you attach them to the appropriate locations in the program LOCA (Locations).
PROCEDURE
1 Enter LPPR.
2 Click on Enter Criteria then Execute Query to see which profiles have already been set up.
3 If you need to set up another profile, click on Create Record.
4 Key in your location print profile code for your first printer and press Enter.
5 Key in a description (for example, Door 3) and press Enter.
NOTE If you are splitting your pick document into different documents, make sure that the document is set up to print a message telling the warehouse person that another pick must be performed to complete the order.
FIELD DESCRIPTIONS
Location Print Profile 
Code
Mandatory
Your location print profile code.
Description Mandatory
Your location print profile code description.
Document Code (defined in DOCU)
Mandatory
The document that you wish to print.
Printer Code (defined in PRIN)
Mandatory
The printer on which you wish to print the document.

Location Print Profile showing two documents to print on printer P1
6 In the Document Block, key in your document code and press Enter.
7 Key in your printer code for this location and press Enter.
8 Repeat steps 6 and 7 for each additional document that you wish to “split” based on location.
9 Repeat the above steps for your second location print profile. If you have a third printer in your warehouse, set up a third location print profile.
10 When you finish setting up all your profiles, click on Return to Main to exit create mode.
11 Click on Exit to exit the program.

### Location Type (LOTP) <a id="location-type-lotp"></a>

OVERVIEW
In this program, you define your location types (BULK, RACK, COOLER, PICK, DRY, etc.). Location types are attached to locations in the program LOCA (Locations). There are four types of locations that you can set up in LOTP:
▪ a regular rack location (that is, neither pick line nor staging)
▪ a pick line location (pick lines are set up in PIIT)
▪ a staging location
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of your location types

▪ a reserved area for partial pallets
A staging location is a temporary storage area for inbound or outbound product that has not been counted or confirmed. A typical staging area would be a dock or a door. When you receive the product in ENRE or through an EDI program, you assign it to a staging location. Once you confirm the receipt, the allocation routine will assign a regular location to the product.
For each location type that you set up in LOTP, you specify the following:
▪ whether or not you want the allocation routine to assign locations for inbound product
▪ whether or not you want the allocation routine to assign locations for outbound product
▪ which location type you want the allocation routine to pick from first, which location type you want the allocation routine to pick from second, third, etc., (outbound product only)
NOTE Do not confuse location types with isolator zones. Location types correspond to different physical areas within your warehouse (BULK, RACK, PICK, etc.). 
Isolator zones, on the other hand, are artificially created entities within the same area (for example, CUSTOMER A/CUSTOMER B or FAST-MOVING MEAT/SLOW-MOVING MEAT) whose purpose is to keep similar product together and hence improve the efficiency of directed put-away and picking.
FIELD DESCRIPTIONS
Location Type Mandatory
Your location type code. For example, OPEN for Open Area.
Description Mandatory
Your location type description.

Sequence Mandatory
The allocation routine will pick from location types based on the sequence number with lower numbers having a higher priority. Sequence number logic is only activated after all other factors have been evaluated. For example, if you are picking to clean and you set your BULK type to 1 and your RACK type to 3, the following will occur. Should the allocation routine select two locations with the same product and the same quantity, the location with the location type of BULK will be picked first then the location with the location type of 
RACK. 
If you do not want to sequence your location types, set the sequence number to 5 for all location types.
NOTE The Sequence field is ignored for directed put-away.
Not to Mix Inventory at 
Level
If you select an inventory level in this field, allocation will not mix inventory at the level that you specify. For example, if you select level 2 (lot), allocation will not put-away two different lots in the same location. This field applies to putaway, relocate and replenishment.
Enable Location Aliases See “Location Aliases” (ver [Locations (LOCA)](configuracao-armazem.html#locations-loca)).
Suppress Inventory 
Merge to Location
Y = Yes
N = No
If you set this flag to Yes for your pick line location type, inventory merging of the lowest inventory level with the pick line location code will be disabled during replenishments and relocations. That is, if you replenish item AB, lot 123, 
PID 001 to pick line location A00L, the PID will NOT change from 001 to A00L.
The Yes option will override your inventory merge settings in ITEM.
Directed Put-Away Y = Yes
N = No
If you specify Yes, the allocation routine will put product away in this location type. If you specify No, the allocation routine will bypass this location type when putting way product.
FIELD DESCRIPTIONS

Directed Picking Y = Yes
N = No
If you specify Yes, the allocation routine will pick from this location type. If you specify No, the allocation routine will bypass this location type when picking product.
Pick Line N = No
Y = Yes
If the location type is a pick line, set this flag to Yes.
Priority Picking N = No
Y = Yes
If you select this option, allocation will always pick from these locations first regardless of your FIFO/LIFO rules. Priority pick locations are typically used for product with a high volume of each picks for a particular item. Priority picking is only available for orders assigned to waves in Wave Manager.
Reserve for Partial Pallet N = No
Y = Yes
If you set this flag to Yes for a given location type, you can define a reserved area for partial pallets. When receiving partial pallets in RFCH/RFPU, directed put-away will select locations in this reserved area.
Partial pallet put-away to a reserved area must be activated in the Put-Away 
Partial Pallet to Reserved Area field in MRFP.
Staging N = No
Y = Yes
If the location type is a staging area, set this flag to Yes. 
Staging Type Pick and Drop
Wrapper
The type of staging area. If you leave this field blank, the staging area will be considered a general staging area located on the dock.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter LOTP.
2 Click on Enter Criteria then Execute Query to see which location types have been already set up. 
Allow Picking in Staging 
Location
N = No
Y = Yes
If you set this flag to N for No, you cannot pick product in an RF program from a staging location. If you set this flag to Y for Yes, you can pick product from a staging location in an RF program. 
Disable Three-Step PutAwayN = No
Y = Yes
If you set this flag to Yes for a given location type, you can disable three-step put-away for that location type even though it is defined as a default in MRFP in the Special Receiving Mode Types field (options 2 and 3).
Weight Restriction ValidationReserved for future use
Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
Exclude from RFPIC Pick 
List
N = No
Y = Yes
If you select No, locations belonging to this location type will not be excluded from the RFPIC pick list. If you select Yes, locations belonging to this location type will be excluded from the RF pick list; for example, order lines that are to be voice picked should not appear in RFPIC pick list.
Enable Pallet Attribute N = No
Y = Yes
The Yes option is only required if you put-away product by inventory attribute (INAT).
FIELD DESCRIPTIONS

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

### Locations (LOCA) <a id="locations-loca"></a>

OVERVIEW
In this program, you set up the locations in your warehouse. You can define your locations in AccellosOne 
3PL in any way that you choose — a location can be the floor space to hold a single pallet or it can be an entire area of your warehouse. You can also set up a dock area or door as a location. The way in which you define your locations in AccellosOne 3PL depends on a number of factors including the racking in your warehouse and the type and variety of product that you store. Generally speaking, small well-defined locations are recommended to take full advantage of AccellosOne 3PL’s active locator system.
The following examples show how locations might be defined in a typical warehouse. If your warehouse has special needs, you may wish to define your locations differently.
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

▪ MHE = Material Handling Equipment Locations
A static/stationary location is a standard rack or floor area that cannot be moved. An MHE (material handling equipment) location is a forklift, truck, pallet jack or other type of vehicle or equipment that may hold product for a brief period of time but is not considered a permanent location.
DEFINING THE SIZE/MAXIMUM CAPACITY OF A LOCATION
One of the most important functions in LOCA is the different options for defining the size/maximum capacity of a location. The size/maximum capacity of a location in AccellosOne 3PL serves two functions: it is used in directed put-away to tell AccellosOne 3PL when a particular location is full and it is needed in the Location 
Analysis Report (LOAN) to identify the amount of space occupied for each location.
There are four ways of specifying the size/maximum capacity of a location in AccellosOne 3PL:
SETTING UP A NEW LOCATION
When you set up a new location in LOCA, the following information is required:
▪ the warehouse to which the location belongs
▪ a code for the location
▪ the location bill code for the location (set up in LODE)
▪ the height, width and length of the location
▪ the location structure type (that is, a standard rack or floor location that cannot be moved or a piece of movable equipment such as a forklift or pallet jack)
▪ the location type (set up in LOTP)
▪ the isolator code (set up in ISOL)
linear measurements (cube)
You can specify the linear measurements for the location (height, width and length) and AccellosOne 3PL will calculate the cube for you automatically.
maximum capacity If you receive standard pallet sizes, you can defined the maximum number of pallets, cases or eaches per location.
location size code If you receive non-standard pallet sizes, you can assign location size codes to each location line in ENRE. See Allocation and Wave Manager for further information.
weight You can define a maximum weight for a location or range of locations.
NOTE If you use more than one method for calculating the size/maximum capacity of location (for example, a maximum cube, a maximum number of SKU’s and a maximum weight), all conditions must be satisfied before directed put-away will select the location.

▪ the maximum SKU capacity
FIELD DESCRIPTIONS
Warehouse Code (defined in WARE)
Mandatory
The warehouse to which the location belongs.
Location Code Mandatory
Your code for this location. The code that you enter in this field must match the format that you defined in the Format Block of WARE.
Description Optional
A meaningful description for this location.
Location Bill Code (LODE)
Mandatory
The location bill code for the location (that is, how the product in this location will be billed). You cannot change the location bill code for a location in modify mode. If you wish to change the location bill code for an existing location, you must do so in ADLB (Adjust Location Bill Code). See the System Administration Guide for further instructions.
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

Height Mandatory
The height of the location.
Width Mandatory
The width of the location.
Length Mandatory
The length of the location.
Weight Measure Code Mandatory
The unit of measure (pounds, kilograms, tonnes, etc.) you wish to use to record the weight limit of this location. You use the weight limit of a location in directed put-away/moves if you want AccellosOne 3PL to check the weight of product against the weight limit of a location.
This function requires further setup in ILOP (Item Location Profile).
Weight Limit Mandatory
The weight limit of the location. If you do not want AccellosOne 3PL to check the weight limit of a location during directed put-away, enter a weight of 0.
FIELD DESCRIPTIONS

Master Location for 
Weight
Optional
If you have a weight limit for an entire aisle or rack, you must specify a master location for weight and link each location to the master location.
For example, suppose you have three locations — A101, A102 and A103 — and each location has a weight limit of 100 pounds. If you specify a master location, the weight limit will apply to all three locations. For example, you could have 100 lbs. in one location and zero in the other two, you could have 
33 lbs. in each location or you could have any other weight combination that did not exceed the overall total of 100 lbs.
If you do not specify a master location for weight, the 100 lbs. limit applies to each location.
SAMPLE SETUP
You have three locations — A101, A102 and A103 — and a total weight for the rack of 100 pounds. For your A101 location, set you weight limit to 100 lbs. 
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
An MHE (material handling equipment) location is a forklift, truck, pallet jack or other type of vehicle or equipment that may hold product for a brief period of time but is not considered a permanent location.
A static/stationary location is a standard rack or floor area that cannot be moved.
Location Type Code (LOTP)
Mandatory
The type of location (RACK, DRY, COOLER, etc.).
FIELD DESCRIPTIONS

Isolator Code (ISOL) Mandatory
The isolator code (if any) of the location or NR for Not Required.
Hold Code (HOLD) Optional
If you attach a hold code to the location (for example, blast freezing), any product put in the location will be placed on automatic hold and cannot be shipped until it is released (unless product is on a shippable hold).
Attaching a hold to a location affects new inventory only. Product already in the location will not be placed on hold.
Cycle Count Profile Code (CYCP)
Optional
See the Cycle Counting Guide for further information.
Picking Path Sequence 
Number
Optional
See the RF Guide for further information on configuring the sort sequence for picking tasks in RFPIC. You set up the sort sequence for picking tasks in 
REGI (Task Profile).
Aisle Reference This field is used to identify aisles when the aisle cannot be extracted from the location code in the Location Attributes Block of WARE.
Facing Reference An additional field that can be used for sorting purposes.
Location Size Code (LOCS)
Optional
If you specify a size code for the location, AccellosOne 3PL will attempt to putaway product in a location whose location size code matches the product’s location size code.
Location Ship Unit ID Reserved for future use
FIELD DESCRIPTIONS

Track Last Location Used for Put-Away
F = Track at Level 4
H = Track at Level 3
N = Not Used
R = Track by Receipt
T = Track at Level 2
Y = Track at Level 1
If you select any option other than N (Not Used), you can put-away product into this location using the options in the Last Location Used group in ILOP (Put-Away). If you select Not Used, the options in the Last Location Used group in ILOP (Put-Away) are not available for this location.
For example, suppose you select Track at Level 1. Any lot for the same item will be considered the last location used. If, however, you select Track at Level 
2, any pallet ID belonging to the same lot will be considered the last location used.
Put-away/Directed Move 
Sort Sequence
See Allocation and Wave Manager.
Capacity SKU Code (SKUS)
Mandatory
The SKU type that is stored in the location.
Maximum Capacity Mandatory
The maximum capacity of the location in the units of measure defined in 
Capacity SKU Code field. If you are handling standard pallet sizes, AccellosOne 3PL’s active locator system uses this information to determine the best location for receiving any given product.
Labor Standard Modifier See section on Operational Board in the Operations 2 Guide.
Voice Check Digit 1/2/3 See the section on Voice Activated Picking and Order Assignment System in the RF Guide.
FIELD DESCRIPTIONS

LOCATION ALIASES
Location aliases serve two functions in AccelloOne 3PL:
▪ because RF operators cannot see location aliases, they prevent operators from cheating by typing in the code for a location that they are not actually working at
Location X/Y/Z CoordinatesThese three fields allow you to define the travel distance between a bulk location and the pick-face when performing replenishments. When searching for a suggested put-away location, inbound allocation will search for locations that are as close as possible to the item's pick line location set up in PIIT. The unit of measure in these three fields is defined in the Linear Measure Code field.
NOTE This proximity logic applies to fixed pick line locations only; floating pick line locations are not supported.
ILOP uses the following formula to calculate a put-away location's proximity to an item's pick line location:
absolute value (X_locEmpty - X_locPIIT) + absolute value (Y_locEmpty - 
Y_locPIIT) + absolute value (X_locEmpty - Z_locPIIT) = storage distance score
The lower the score, the closer the location is to the pick line.
Proximity logic must be activated in ILOP by selecting option I8360, M8360 or 
MS 8360 “Order by distance to fixed pick line by LOCA X, Y, Z coordinates, ware, loc”.
Exclude from Follow 
Order Rule for Directed 
Staging
N = No
Y = Yes
This flag allows you to define rules for staging product in RFPIC/RFITLV when the RF operator overrides the suggested directed staging location. If you select No, the new staging location becomes the default staging location for the remaining pallets on that order. 
If you select Yes, any override by the RF operator of the suggested directed staging location will have no effect on the suggested directed staging location for the remaining pallets on the order.
Status A = Active
D = Deactivated
If a location is active, you can receive product into the location and ship product out of the location. If a location is deactivated, you cannot receive new product into the location.
FIELD DESCRIPTIONS

▪ they allow you to split a location into two sections (for example, a carton live storage system) depending on your point of access: a front fill location alias for picking and a back fill location alias for put-away 
When putting away to locations with enabled aliases in RFCH, RFPU, RFPR, RFRL and RFITLV, the RF operator will either:
▪ see the location code but must scan in the back fill location alias and use the back fill check digits for validation (option Y in LOTP)
▪ see the alias and scan in the back fill location alias and use the back fill check digits for validation (option C in LOTP)
When picking or relocating from locations with enabled aliases in RFPIC/RFPK, RFST, RFITLV and RFRL, the RF operator will either:
▪ see the location code but must scan in the front fill location and use the front fill check digits for validation (option Y in LOTP)
▪ see the alias and scan in the front fill location alias and use the front fill check digits for validation (option 
C in LOTP)
PROCEDURE
1 Enter LOCA.
LOCATION ALIASES (LOTP)
Enable Location Aliases N = Not Used
Y = Use Aliases for Validation
C = Use Aliases to display and validation
If you specify Y or C, location aliases will be activated in LOCA. If you specify 
No, location aliases will NOT be activated in LOCA. Location aliases serve two functions in AccelloOne 3PL:
▪ because RF operators cannot see location aliases, they prevent operators from cheating by typing in the code for a location that they are not actually working at
▪ they allow you to split a location into two sections (for example, a carton live storage system) depending on your point of access: a front fill location alias for picking and a back fill location alias for put-away
If you select “Y - Use Aliases for validation”, the actual location code in LOCA will display, but the RF operator must enter or scan in the alias. If, on the other hand, you select “C - Use Aliases to display and validation”, the alias will display and the RF operator must enter or scan in this alias.
TIP It is best to create “like” locations all at the same time. For example, start by creating all your rack locations before you go on to create your bulk locations. By grouping your locations in this manner, you minimize changes to the “template” as you create new locations.

2 Click on Enter Criteria then Execute Query to see which locations have been already set up. 
3 If you need to set up another location, click on Create Record.
4 Key in the warehouse code for the location and press Enter.
5 Key in your first location code and press Enter.
If you receive an error message, then your location code does not match the parameters that you set up in WARE (Warehouse and Location Format). Go back to WARE and verify the format of your location codes.
6 If required, key in a meaningful description for your location code and press Enter.
7 Key in a location bill code and press Enter or use your pick list to choose the appropriate code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code.
8 If required, key in a location print profile code and press Enter.
9 Key in the linear measurement code for the location (IN = inches, FT = feet, etc.) and press Enter or use your pick list to select from a list of predefined codes.
10 Key in the height, width and length of the location, pressing Enter at the end of each line.
11 Key in the weight measurement code for the location (LBS = pounds, KG = kilograms, etc.) and press 
Enter or use your pick list to select from a list of predefined codes.
Locations
12 Key in your weight limit for the location and press Enter. If you do not require a weight limit for the location, key in 0.
13 If required, key in a location in the Master Location for Weight field and press Enter.
14 Press Enter to bypass the Vertical Height Factor Code field.
15 In the Location Structure Type Code field, use your pick list to choose the appropriate code.
16 Key in your location type code and press Enter or use your pick list to choose the appropriate code.

17 Key in your isolator code if any and press Enter or use your pick list to choose the appropriate code.
Locations
18 Press Enter to bypass the Hold Code field.
19 Press Enter to bypass the Cycle Count Profile Code fields.
20 If required, key in a location size code and press Enter.
21 In the Track Last Location Used for Put-Away field, key in the appropriate value and press Enter.
22 Press Enter until your cursor is positioned in the Capacity SKU Code (SKUS) field.
23 Key in your capacity SKU code and press Enter or use your pick list to choose the appropriate code.
24 Key in the location’s maximum capacity in the units of measure that you specified in the previous field and press Enter.
25 Press Enter to bypass the Labor Standard Modifier field.

26 Do one of the following:
27 When you finish adding your locations, click on Return to Main and then Exit to exit.
If you wish to create more locations based on the parameters of your first location: If you wish to exit:
a) Key in your new location code and press Enter.
b) If required, make any necessary changes to the parameters of the location (for example, the description, location type, isolation code, height, etc.).
c) Press F12 to add the new location.
d) Repeat the above steps for each additional location that you wish to add.
a) Proceed to next step.

## Message Setup <a id="message-setup"></a>

*Manual N — Setup Guide*

### Messages (MESS) <a id="messages-mess"></a>

OVERVIEW
This program allows you to set up standard messages on your system such as “Must maintain at above zero degrees Celsius”, “Remind driver to chock wheels”, etc. The messages that you create in this program can be attached to a specific customer, item, carrier or consignee. You can print these messages on specific shipping and receiving documents (DPME) or you can have them appear as pop-up messages for the operator at any flow step that you specify (DEME).
PROCEDURE
1 Enter MESS.
PREREQUISITES: None
ATTACHED TO: DEME (Depositor Messages)
DPME (Depositor Print Messages)
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

2 Click on Enter Criteria then Execute Query to view the message codes that have been already set up.

Messages
3 If you need to set up a new message code, click on Create Record.
4 Key in your message code and press Enter. Then key in a meaningful description and press Enter again.
5 Press Enter in the Text Block field to advance to the next field.
6 Key in the first line of your message and press Enter. If you want to create a multi-line message, you must press Enter at the end of each line in order to advance to the next line.
7 When you finish entering your message, press Enter to get a new line.
8 Click on Return to Main then Exit to exit.

### Depositor Messages (DEME) <a id="depositor-messages-deme"></a>

OVERVIEW
In this program, you attach the message that you created in MESS to the customer and flow to which it applies. When you set up a depositor message in DEME, the message appears in pop-up form to the operator at the flow that you specify.
PREREQUISITES: CUST, MESS, FLPR
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

For example, suppose you attach a specific message to inbound flow X and customer Y. Whenever you receive from customer Y and advance to flow X in CHRF (Time Stamp and Confirm Receipts), that message will appear in pop-up form.

Depositor message attached to COOR flow
PROCEDURE
1 Enter DEME.
FIELD DESCRIPTIONS
Customer Code (defined in CUST)
Mandatory
The customer to whom the message is attached or .ALL for all customers.
Flow Code (defined in FLPR)
Mandatory
The flow at which the message will appear.
Message Code (defined in MESS)
Mandatory
The message.

2 Click on Enter Criteria then Execute Query to see which messages have been attached to which customers.

Depositor Messages
3 If you need to set up a new depositor message, click on Create Record.
4 Key in your customer code and press Enter or select it using the pick list. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
5 Key in your flow code and press Enter or select it using the pick list.
6 Key in your message code and press Enter or select it using the pick list.
7 Repeat the above steps for each additional depositor message that you wish to set up.
8 When you finish setting up your codes, click on Return to Main and then Exit to exit.

### Depositor Print Messages (DPME) <a id="depositor-print-messages-dpme"></a>

OVERVIEW
In this program, you can attach the message that you created in MESS to a particular document such as the core bill of lading, pick document, receipt invoice and tally. You can also display the message in RFCH (RF 
Check/Unload) and RFPIC (RF Pick). DPME allows you to specify that a given message will print on a given document for either all customers or a specific customer. As well, you must specify one of the following as your message recipient:
PREREQUISITES: CUST, CARR, CONS, SHIP, MESS, DOCU (set up by HighJump)
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

▪ a specific carrier
▪ .ALL carriers
▪ a specific consignee
▪ a specific shipper
If you have not set up your carriers, consignees and shippers, you cannot create DPME messages. Return to this program after you have completed the setup procedures.
PROCEDURE
1 Enter DPME.
2 Click on Enter Criteria then Execute Query to see which documents and which messages have been attached to which customers.
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer to whom the message applies or .ALL for all customers.
Carrier (CARR) / Consignee (CONS) / Shipper (SHIP) Code
Mandatory
The carrier, consignee or shipper for whom the message is intended or .ALL for all carriers.
Document Code (DOCU) Mandatory
The document on which the message will be printed.
Message Code (MESS) Mandatory
The message code of the message.
Allow Display of Message in RF
Y = Yes
N = No
If you select N for No, the message will be suppressed in all RF programs that support messages.

Depositor Print Messages
3 If you need to set up a new customer/document/message, click on Create Record.
4 Key in your customer code and press Enter or use the pick list function to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. 
Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
If you want the message to appear for all customers using this document, select .ALL.
5 Use your pick list function to select a particular carrier/consignee/ shipper. You can also select .ALL carriers, consignees or shippers for this field. 
6 Key in your document code and press Enter or use the pick list function to select a document code.
7 Key in your message code and press Enter or use the pick list function to select a message code.
8 In the Allow Display of Message in RF field, key in Y for Yes or N for No and press Enter.
9 If required, enter another document and message for this customer and carrier/consignee/shipper or click on Return to Main and then Exit to exit this program.

### Hazardous Material Messages (HAZA) <a id="hazardous-material-messages-haza"></a>

PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 

OVERVIEW
In this program, you set up your hazardous material messages. These messages can be attached to a particular item and will print on the standard bill of lading 1 and 2 and the pick document.
For more advanced hazardous material tracking, see “Hazardous Material Block” (ver [Item (ITEM)](configuracao-itens.html#item-item)) in ITEM.
PROCEDURE
1 Enter HAZA.
2 Click on Enter Criteria then Execute Query to see which hazardous material messages have already been set up.
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Code Mandatory
Your hazardous code.
Description Mandatory
Your hazardous code description.
Text Block Mandatory
The message text for your hazardous code.

Hazardous Material Messages
3 If you need a new hazardous message, click on Create Record.
4 Key in a message code and press Enter.
5 Key in a description for your new code and press Enter.
6 Press Enter in the Text Block and begin typing in the text of your message. If you require more than one line of text, press Enter at the end of the line to generate a new line. You can enter as many lines as you need. When you finish entering your last line, press Enter. Then click on Master Block to exit the Text 
Block.
7 Repeat steps 3 to 6 for each additional hazardous message that you wish to enter.
8 When you finish entering your hazardous messages, click on Master Block and then Exit to exit.

### Inventory Messages (ADIM) <a id="inventory-messages-adim"></a>

OVERVIEW
In this program, you can create messages that can be attached to a particular item. The messages that you create in ADIM can be displayed in the Line Block during order entry (ENOR) and receipt entry (ENRE). As well, you can view them when you look the item up in LOEN. These messages are for display purposes only; 
they do not print on any AccellosOne 3PL document or report.
The messages that you create in this program must be attached to a unique inventory entity; that is, an item defined down to the lowest inventory level.
Multiple messages attached to the same item are allowed.
PREREQUISITES: MESS, CUST, ITEM
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: You must have at least one confirmed item in your warehouse.
FIELD DESCRIPTIONS
Customer Code (defined in CUST)
Mandatory
The customer to whom this item belongs.
Level 1 (defined in ITEM)
Mandatory
The item to which you wish to attach the message.
Level 2/3/4 The inventory level to which you wish to attach the message.
Message Code (defined in MESS)
Mandatory
The item’s message

PROCEDURE
1 Enter ADIM.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter.
4 If required, key in additional levels of inventory and press Enter.
5 When you have defined the item to which you wish to attach the message, click on Execute Query.
6 If your query retrieved more than one inventory entity, use your up and down arrow keys to select the inventory entity to which you wish to attach the message.
7 Click on Message Block.
8 Use your pick list to select the appropriate message that you wish to attach to the item.
9 In the Order Entry field, key in Y for Yes or N for No and press Enter.
10 In the Receipt Entry field, key in Y for Yes or N for No and press Enter.
11 In the Inventory Look-Up field, key in Y for Yes or N for No and press Enter.
Order Entry Y = Yes
N = No
If you set this field to Yes, the message will appear in ENOR. If you set this field to No, the message will not appear in ENOR.
Receipt Entry Y = Yes
N = No
If you set this field to Yes, the message will appear in ENRE. If you set this field to No, the message will not appear in ENRE.
Inventory Look-Up Y = Yes
N = No
If you set this field to Yes, the message will appear in LOEN. If you set this field to No, the message will not appear in LOEN.
FIELD DESCRIPTIONS

Adjust Inventory Messages showing two messages
12 Repeat steps 7 to 10 for each additional message that you wish to attach.
13 When you finish entering all your messages for this item, click on Return to Main to exit create mode. 
Then click on Inventory and Exit to exit.
