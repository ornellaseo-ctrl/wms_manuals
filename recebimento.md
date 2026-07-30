---
title: "Recebimento (Inbound)"
description: "Entrada de mercadoria no WMS: digitação, confirmação, rateio e impressão de documentos."
layout: default
---

# Recebimento (Inbound)

Entrada de mercadoria no WMS: digitação, confirmação, rateio e impressão de documentos.

**Fluxo principal:** `ENRE -> CHRF (confirma) -> RCRA (rateia) -> PRRE/PRRM (imprime)`

> Fonte: manuais D do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction <a id="introduction"></a>

*Manual D — Operations 1*

# Manual D — Operations 1 Guide (Operações 1: Recebimento e Expedição)
> **ID do Manual:** D  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Fluxo operacional principal: recebimento (ENRE), confirmação (CHRF/CHOF), expedição de pedidos (ENOR), lookups (LORE/LOOR/LOEN), impressão de documentos, relocações (RELO), ajustes (ENAJ), holds, transferências, e processamento de inventory levels.
---

### About This Manual <a id="about-this-manual"></a>

The Operations 1 Guide will assist you in applying the programs that are used most frequently during warehouse operations. This guide is designed for beginner and intermediate users of the AccellosOne 3PL operations programs. It is divided into four parts. 
Part I, The Operations Flow Process, describes the sequential process that the system uses to direct both the receiving and the shipping operations. 
Part II, Receiving, describes the AccellosOne 3PL programs that apply to the receiving process. It provides detailed procedures for entering, modifying and deleting data into these programs. This section also explains the specific look-up programs that will allow you to view data entered during the receiving process.
Part III, Inventory Maintenance, describes the AccellosOne 3PL programs that maintain accurate inventory records while the product is stored in the warehouse. It provides detailed procedures for adjusting inventory records, relocating inventory, and placing or removing inventory from holds. This section also explains the specific look-up programs that will allow you to view inventory-related data.
Part IV, Shipping, describes the AccellosOne 3PL programs that apply to the shipping process. It provides detailed procedures for entering, modifying and deleting data into these programs. This section also explains the specific look-up programs that will allow you to view data entered during the shipping process.

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting reports
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

## The Operations Flow Process <a id="the-operations-flow-process"></a>

*Manual D — Operations 1*

### Understanding the Flow Process <a id="understanding-the-flow-process"></a>

The two main functions of AccellosOne 3PL Operations are receiving inventory into the warehouse and shipping inventory out of the warehouse to fill orders. A flow process setup is used in AccellosOne 3PL to direct both of these procedures.
The flow process is the series of steps (flows) that the system requires you to perform when receiving and shipping product through AccellosOne 3PL. The code names for the steps were set up previously in the program Flow Process (FLPR). 
The sequence of the steps was defined in the program Depositor Workflow Profile (DIFP). The system controls the order of the steps and does not allow you to go out of sequence (although print jobs may be cancelled if necessary and flow processes that have been set up as Not Mandatory in DIFP can be bypassed in either CHRF or CHOF).
As the operator advances each flow, the system attaches the operator’s code and the current system time to the flow. This process is called time-stamping. Time-stamping is useful whenever a follow-up is needed since questions can be directed to the operator who made the entry. (Therefore, be sure to log in with your own operator code and do not allow anyone else to use it.)
Various documents such as tallies or pick sheets usually need to be printed as part of the receiving or shipping operation process. (However, a warehouse with a Radio Frequency environment may not need to print any documents.) In the program DIFP, each document type is attached to a particular flow process. 
Document types and flow processes are attached in DIFP to match the real workflow of performing actual warehouse tasks.

### Flow Process Codes <a id="flow-process-codes"></a>

All flow steps that are part of receiving are inbound processes. All flow steps that are part of shipping are outbound processes. 
There are two mandatory inbound processes: 
 ENRE (Enter Receipt)
 CORE (Confirm Receipt) 
 There are two mandatory outbound processes: 
 ENOR (Enter Order) 
 COOR (Confirm Order) 
AccellosOne 3PL has other pre-loaded optional inbound and outbound codes. The pre-loaded flow process codes are:
 CITR (Change In-Transit to Regular)
 EDI (Message Received by TradeLink)
In addition, your system setup may have additional codes for other flow processes that your company wishes to track. 

### Looking Up Your System’s Flow Process Codes <a id="looking-up-your-system-s-flow-process-codes"></a>

If you have authorization to access the program Flow Process (FLPR), you may familiarize yourself with the flow process codes that are set up in your system. The following procedure allows you to check existing codes so you will recognize them as they display when processing a receipt or an order.
1 Enter FLPR.

FLPR screen showing the flow process codes used for shipping and receiving
2 Click on Enter Criteria and Execute Query to display the list of existing flow process codes. Use your arrow keys to scroll through the list. Be sure to scroll through to the end of the list as they may not all appear on the screen at one time if the list is long.
3 Click on Exit to exit the program.
For a full explanation of the program FLPR, refer to the Setup Guide. 

### Flow Process Sequence <a id="flow-process-sequence"></a>

Flow codes and their related documents are each assigned a number to indicate their sequence in the flow. 
Sequence numbers usually are in multiples of five or ten (10, 15, 20, 25, 30, etc.) so that new flows can be added between existing ones if the need arises.
Regardless of how many codes there are, Enter Receipt (ENRE) and Confirm Receipt (CORE) are always sequence 1 and 90 respectively in the inbound flow sequence and Enter Order (ENOR) and Confirm Order (COOR) are always sequence 1 and 90 respectively in the outbound flow sequence. An example of a flow process in DIFP could be:

INBOUND
 ENRE ENTER THE RECEIPT (with printing of the receiving tally document attached to this step)
 CORE CONFIRM THE RECEIPT (with printing of the warehouse receipt document attached to this step)
OUTBOUND
 ENOR ENTER THE ORDER (with printing of the pick document attached to this step)
 COOR CONFIRM THE ORDER (with printing of the bill of lading document attached to this step)

### Looking Up Your System’s Flow Process Sequence <a id="looking-up-your-system-s-flow-process-sequence"></a>

If you have authorization to access the program Depositor Workflow Profile (DIFP), you may familiarize yourself with the sequence of the flow process steps that are set up in your system. The following procedure allows you to check the existing workflow profiles so you will recognize them as they display when processing a receipt or an order.
The DIFP program screen consists of:
 the Header Block
 the In/Out Block 
 the Flow Block
 the Document Block
 the Special Verification Block
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to display the existing workflow profiles. 
Note that the bottom left-hand corner of the header box has a current record counter, e.g., 1 of 10. The first digit is the actual number of the record currently displayed on the screen and the second digit indicates how many records there are in total in the program. 1 of 10 means you are viewing the first of ten records.

DIFP screen showing DIFP program blocks
3 With your cursor in the Header Block, use the up and down arrow keys to move from one DIFP record to another. Find a record that applies to a customer whose receipts you will be entering. 
4 Click on In/Out/Repi/Relo Block. Use your up and down arrow keys to toggle back and forth between 
Inbound and Outbound. 
When the In/Out/Repi/Relo Block is set at Inbound, the Flow Block below displays the inbound flow steps.
When the In/Out/Repi/Relo Block is set at Outbound, the Flow Block below displays the outbound flow steps.
5 Set the cursor on Inbound.
6 Click on Flow Block. The cursor is positioned on the first Sequence Flow Number field. Note the Document Block below, which now displays the documents (if any) that are attached to the first flow process. 
Check the current record counter at the bottom left-hand side of the screen. Only four documents display on the screen at a time. If there are more than four, click on Document Block. Use the down pointer key to move through to the last document. Once you have viewed all documents listed, click on Flow Block.
7 Use the up and down arrow keys to position your cursor on the second Sequence Flow Number field. 
Note the Document Block below, which now lists the documents (if any) that are attached to the second flow process. 
Check the current record counter at the bottom left-hand side of the screen. If there are more than four, click on Document Block. Use the down pointer key to move through to the last document. 
Place cursor here to toggle between inbound and outbound flow processes
Header 
Block

DIFP screen showing all DIFP program blocks
8 If there are more flow processes, position the cursor on the next Sequence Flow field number to view the attached documents in the Document Block. Repeat until you have viewed all flows and attached documents.
9 Click on Special Verification Block to check whether any customized functions have been set up for this 
Depositor Workflow Profile. Use the down pointer key to move through to the last function listed.
10 Click on Master Block and In/Out/Repi/Relo Block. 
11 Set the cursor on Outbound.
12 Repeat steps 6 to 10 to view the outbound DIFP details.
13 Click on Document Block, Flow Block and then In/Out/Repi/Relo Block. Then click on Master Block and 
Exit to exit the program.
For a full explanation of DIFP, refer to the Setup Guide. 

### Flow Process Summary <a id="flow-process-summary"></a>

FLPR and DIFP direct both the receiving and shipping processes.
When the cursor is on a sequence flow process code, the attached documents for that flow show in the 
Document Block

This program holds all of the system’s flow process codes. These codes are used to time-stamp and to track the steps that you follow during receiving and shipping. 
This program directs the receiving and shipping operations. DIFP does the following:
 sets the specific flow process codes and the flow process sequence that you must follow to receive a customer’s (depositor’s) shipment or to ship out an order 
 attaches receiving and shipping documents to corresponding flow process codes
 if your company uses directed put-away and directed picking, DIFP directs the system to perform allocation after a specific flow process 
FLPR
Flow Process
DIFP
Depositor Workflow Profile
Receiving Process Shipping Process

## Receiving <a id="receiving"></a>

*Manual D — Operations 1*

### Overview of Receiving <a id="overview-of-receiving"></a>

The following is a simplified model of the receiving tasks that are performed each time that a customer sends product to the warehouse.
PUT-AWAY
THE INVENTORY
ALLOCATE
Select and assign the locations where the product will be put away for storage.
RECEIVE THE PRODUCT 
FROM THE CUSTOMER
CREATE PUT-AWAY 
 INSTRUCTIONS AND OTHER 
RECEIVING DOCUMENTS 
RECORD THE 
PRODUCT DETAILS 

### RECEIVING PROGRAMS <a id="receiving-programs"></a>

In AccellosOne 3PL, several programs are involved in the process of receiving inventory into the warehouse. 
You record details for each different item that the customer sent. You record where each item will be stored in the warehouse (manual allocation) or you allow the system to perform automatic allocation later.
After each flow, you print any receiving document that is attached to that particular flow. Not all flows will have a document attached to them.
You use PRRM to print a document that is attached to the flow of a specific Receipt Number.
You use PRRE to print the same document (for example, a tally sheet) that is attached to a specific flow for all receipt numbers in the system that are at this same stage in their flow process.
If necessary, you cancel the need to print a document that is attached to a receiving flow. 
This will allow you to enter CHRF and advance the system to the next flow process without actually printing the document.
If the document for the current flow process has been printed before, you can make the system reprint an attached receiving document.
You time-stamp and advance each flow process.
You Execute Confirm. This will update inventory data and will rate the receipt if your system is set up to rate receipts automatically.
You time-stamp and advance each flow process for individual receipt (Line Block) lines.
You Execute Confirm for individual receipt lines, which will update inventory data accordingly and will also rate the line if your system is set up to rate receipts automatically.
ENRE
Enter Receipt
PRRM
Print Receiving Documents - Specific
PRRE
Print Receiving Documents - All
RERE
Requeue Receipt Documents
CHRF
Time-Stamp and Confirm Receipts
CORL
Confirm Receipts - One 
Line at a Time

RECEIVING OPERATIONS PROCESS
You return to CHRF or CORL and PRRM or PRRE as many times as necessary until all flow processes and all attached receiving documents are processed.
ENRE
PRRM or PRRE
CHRF or CORL
PRRM or PRRE
PRRM or PRRE
CHRF or CORL
Flow Process 2
Flow Process 1
Need to print document?
Need to print document?
Need to print document?
Flow Process 3
No Yes
No Yes
No Yes
CHRF or CORL
Execute Confirm

### Entering a Regular Type Receipt — P (Post-Receiving) <a id="entering-a-regular-type-receipt-p-post-receiving"></a>

To begin the receiving process in AccellosOne 3PL, you enter a receipt in the program ENRE (Enter Receipt). 
You enter a separate receipt for each customer whose product arrives at the warehouse. 

### OVERVIEW <a id="overview"></a>

The program ENRE records many details about the incoming product. The system uses these details later to automatically update inventory records and to bill the owners of the product for inbound handling charges and initial storage charges. ENRE also allows for the manual entry of any extra and accessorial charge details that may apply. 
The ENRE program consists of the following sections:
 Header Block (also called the Master Block)
 Remarks Block
 Carrier Block
 Pallet Block
 Accessorial Charges Block
 Extra Charges Block
 Line Block
 Location Block
The Header Block and Line Block are mandatory. The other blocks are optional.
A physical receipt has general information that applies to the whole shipment and specific information about the individual items that make up the shipment. To capture this in AccellosOne 3PL, ENRE has a Header 
Block and a Line Block. General information that applies to the whole transaction is entered in the Header 
Block. Particular information about each item is entered separately in the Line Block.
P (Post-receiving) is the normal ENRE receipt type. Rating of P (Post-receiving) receipts automatically generates inbound handling and initial storing charges according to the profiles that were set up in AccellosOne 3PL for your warehouse company.
The following procedure will lead you through the ENRE program, field by field. Information for completing the fields is obtained from the receiving documents that accompany or precede the goods or the fields fill in automatically (populate) with data that was preset in other AccellosOne 3PL programs.
Some fields are mandatory. The system will not allow you to continue until you complete a mandatory field. 
Other fields are optional and the system allows you to bypass them by pressing Enter without adding any information.
Some fields have pick lists that display the available options for that field. This is helpful when you do not remember the code that you need. 

### ENTERING HEADER INFORMATION IN ENRE <a id="entering-header-information-in-enre"></a>

The Header Block is also called the Master Block. Data in the Header Block will apply to all line records that you will create later in the Line Block.
1 Key in ENRE at the Enter Selection Prompt. Press Enter and the system displays the Enter Receipts (Inbounds) screen. The program is in the Create Record mode.
2 Leave the Receipt Number field blank. The system will automatically generate a number later.

3 In the Customer Code field, key in the code of the product owner and press Enter. 
If you do not know your customer code, you can select it from the pick list. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select.
4 The system automatically fills in the next seven customer-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 

 ENRE screen showing a P (Post-Receiving) type receipt
5 If required, enter the Shipper Code of the party that is sending the product to the warehouse and press 
Enter. If you do not know the code, use the pick list. If manual shippers are activated on your system, you can key in a forward slash (/) followed by the name and address of the shipper.
6 The system automatically fills in the next seven shipper-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 
7 The system automatically bypasses the Priority field, either filling it in or leaving it blank. This field is only functional when using the auto-print feature of AccellosOne 3PL and it refers to the priority in the printing queue. The priority range is from one to nine with one being the highest priority and nine being the lowest. The system default is 5. 
NOTE If the shipper is always the same as the customer (that is, the customer ships from its own facility), your system may have a profile set up in Shipper (SHIP) 
that uses S (for Same) as the Shipper Code. In this case, you can key in S in place of the Shipper Code and press Enter.
Receipt Type field

If you need to change the default value, press F9 (Previous Field) and then press Enter until the cursor is in the priority Field. Key in the correct number and press Enter.
The screen scrolls up. The system automatically fills in and skips over the (Priority) Description field.

ENRE screen after the screen scrolls upward for the first time
8 The Bill To Code field refers to the party that will be billed for the receiving charges. The system populates this field with the Customer Code. If the party to be billed for the receiving charges is not the Customer Code, key in the correct code and press Enter. If you do not know the code, use the pick list. 
9 The system automatically fills in the next seven Bill To Code related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 
10 Press Enter to accept the default date as the expected Receipt Date. If a different expected Receipt Date is required, key in the correct date using the same date format as shown in the field and press Enter. 
You can enter a Receipt Date that differs from the current system date by up to one month in the past or in the future.
11 Press Enter to accept the default time as the Receipt Time. If a different Receipt Time is required, key in the correct time using the same format as shown in the field and press Enter.
12 Key in the carrier’s probill reference number if the customer requires it and press Enter. Otherwise, press 
Enter to bypass the field. 
13 Key in any customer-defined Reference Number that applies to this receipt and press Enter. Otherwise, press Enter to bypass the field. The screen scrolls up.
14 Enter the Carrier Code of the firm that transported the product to the warehouse and press Enter. If not known, use the pick list. If manual carriers are activated on your system, you can key in \ followed by the name and address of the carrier.
Note that the pick list has an “unassigned” option if the carrier is not known at this point in time.
The system populates the Customer 
Code and Bill To 
Code fields with the same data. Change the bill-to code if necessary.

15 Enter the Load Type Code and press Enter. If you do not know the code, use the pick list 
The system automatically fills in the Description field of the Load Type Code.
16 The Warehouse Code field is usually left blank. Press Enter to bypass the field.
For further information on this field, refer to the section, [Restricting Multiple Item Lines to a Common 
Warehouse](recebimento.html#restricting-multiple-item-lines-to-a-common-warehouse). 

ENRE screen after the screen scrolls upward for the second time
17 In the Total Units field, key in the number of units that arrived at the warehouse for the entire receipt and press Enter. Do this by adding together the units of each line on the receipt. 
You count the units of each line by using the line item’s lowest SKU level according to its item quantity breakdown. For example, count by cases for the line 1 item if its quantity breakdown is pallets/cases and count by feet for the line 2 item if its quantity break-down is yards/feet. Then add the units together for both lines: 10 cases plus 10 feet equal 20 units.
18 The default for the Remarks field is N (for No). If you do not need header remarks to appear on the warehouse receipt, press Enter to accept the default. If you do, key in Y (for Yes) and press Enter. A block will appear later in the program to enter the remarks.
19 In the Carrier Details field, key in the appropriate value.
N (No) Use when you do not need to track carrier details. 
E (Entry) Use to enter the carrier details during receipt entry. The Carrier 
Details Block will display later in ENRE for you to complete. The details will print on the attached inbound document that has been pre-selected by your company.

20 Press Enter to bypass the Pallet Details field.
21 Press Enter twice to bypass the Accessorial Charges and Receipt Extra Charges fields.
22 Press Enter again to bypass the Material Handling Equipment Type Code field.
23 In the Extra Reference Number 1 and the Extra Reference Number 2 fields, enter the data defined by the customer and press Enter. 
If the customer does not require such reference data, press Enter to bypass each of the fields.

ENRE screen after the screen scrolls upward for the third time
24 Press Enter to bypass the Distribution Type Code field.
25 If you changed the default in any of the fields for Remarks, Accessorial Charges and Receipt Extra 
Charges, the corresponding blocks will display now on the screen in succession. 
Complete the applicable blocks by following the corresponding Optional Blocks procedures, which follow the Line Block procedure. Then return to the Line Block procedure, listed directly below, and complete it. 
If none of these optional blocks apply, proceed to the mandatory Line Block procedure directly below. 
C (Confirmation) Use to add carrier details during confirmation of this receipt. The 
Carrier Details Block will display during confirmation and the details will print on the attached inbound document that has been pre-selected by your company.
B (Both) Use to add carrier details twice — once during ENRE and again during confirmation. The details will print on the attached inbound document that has been pre-selected by your company.

### ENTERING LINE INFORMATION IN ENRE <a id="entering-line-information-in-enre"></a>

In AccellosOne 3PL, the term item means an entity made up of its inventory levels as defined in DILP (Depositor Inventory Level Profile). Inventory Level 1 is always the item itself and any other levels are further descriptions or variations of the item’s attributes. 
For example, if you are receiving Item: A, Lot Number: 1, Color: Grey as well as Item: A, Lot Number: 1, 
Color: Blue, you must enter two separate Line Block records. Each Line Block record has a line number assigned to it and each record contains specific details about an individual item at its time of arrival at the warehouse.
Warehouse charges can vary for each item. Therefore, there are different Line Block types to regulate the warehouse charges applied to each item. The following procedure is for a regular P (Post-receiving) Line 
Block type.
1 The system enters the Line Block in the Create Record mode. Leave the Line field with the 1 that is generated by the system.

ENRE Line Block screen ready to accept the details of the first inbound item
2 Leave the Type field with the P (Post-receiving) that is generated by the system. 
3 In the Remark field, if you need remarks to appear on the warehouse receipt for this line item, key in Y (Yes) and press Enter. 
Otherwise, press Enter to accept the N (No) default.
4 In the Charge field, you can add charges for this line item (other than the automatic Inbound handling and Initial Storing charges). If you wish to add charges, key in Y and press Enter. An Accessorial Block screen will display later for entering the charge details.
If there are no additional charges, press Enter to accept N (No). 

5 The system may skip over the Warehouse Restriction field leaving it blank. This means that the field does not apply to this line and the system does not allow you access.
However, the cursor may enter the field and the Help Message Line indicates “Enter a warehouse restriction if required.” If storage of this item is to be restricted to a particular warehouse, key in the Warehouse 
Code and press Enter. If you do not know the code, use the pick list. If a restriction is not required, press 
Enter to bypass the field.
6 Key in the Item Code and press Enter. If you do not know the code, use the pick list. 
Note that Item Code is always Inventory Level 1.

ENRE Line Block screen
7 Under the Item Code field, there can be — depending on the customer’s setup — Inventory Level 2, 
Inventory Level 3 and Inventory Level 4. However, these fields will display with the correct terminology (for example, Lot Number, Production Date, Expiry Date, Pallet ID, etc.) that was preset for this customer. 
If this item has an Inventory Level 2, enter the information for this level and press Enter. Repeat for the other inventory levels, if applicable.
Inventory levels

ENRE Line Block screen
8 Your setup may have a Description Entry field to the right of one or more of the fields for Inventory Level 
2 and higher levels. If this is the case, the cursor moves here prompting you to enter the specific data for this level as requested by the customer (for instance, an actual serial number or actual production date, etc.). The specific data is available in the receiving documents. 
Key in the required information and press Enter for each of the Description Entry fields attached to the inventory levels. 
The system may populate these fields. Check that the system-entered data matches the warehouse receiving documents. If it does, press Enter to accept. If it does not, press F11 (Clear Field), key in the correct data and press Enter.
9 In the Quantity Breakdown field, AccellosOne 3PL shows the SKU’s used to track and bill this item. For example, if the Quantity Breakdown field shows PLT: 50 (the largest SKU) and CASE: 1 (smallest SKU), you read it as one pallet has 50 cases.
10 In the Expected Quantity field, key in the item amount as declared on the receiving documents and press 
Enter. 
You can key in the amount in any SKU that is valid for receipt entry. The SKU’s that are valid for receipt entry are defined in IQBP (Item Quantity Breakdown Profile). For example, if the item’s quantity breakdown is 100 cases per pallet, you can enter an amount of 1,010 cases as follows:
1010 CASES or 10PLT 10 CASES or 9PLT 110 CASES
Embedded spaces are allowed but not required. The total number of characters including blank spaces cannot exceed 20 characters.
11 The system automatically fills in the Received Quantity field with the same amount as the Expected 
Quantity Field. If the amount received into the warehouse is the same as the amount declared on the 
Description 
Entry field for an inventory level

receiving documents, press Enter to accept the data. If it is not, key in the actual amount received and press Enter.
12 The system skips over the Expiry Date field. If this is an Expiry Date Item and you need to enter an expiry date or correct the system-entered date, press F9 (Previous Field). Key in the expiry date and press 
Enter.
13 If the item has a temperature requirement that needs to be tracked, key in the degrees in this field. If it does not, the system skips over the field.

ENRE Line Block screen with item details
14 The system automatically calculates and fills in the item’s Weight Code, Unit Weight, Total Gross Weight, 
Total Net Weight Linear Code, Length, Width and Height if the item was set up as a Standard Weight item.
If you need to change the data in any of these fields, press F9 (Previous Field) the required number of times until the cursor is in the field.
If the item has non-standard weights, key in the applicable weight data in each respective field and press 
Enter.
15 The Location Code field determines the put-away location for this item. If you wish to use automatic putaway, that is, you want the system to choose the location, press Enter to bypass the Location Code field. 
Later in the receiving process, during printing of the attached inbound document that was pre-assigned to trigger allocation, the system will select and assign the location.

If you wish to make a manual put-away entry, that is, you wish to select the put-away location, do one of the following.
16 If your warehouse has automatic put-away, press Enter to bypass the Warehouse Code field. The active locator will choose the warehouse in which to store this item. 
If your warehouse uses manual put-away, the system fills in the Warehouse Code field based on the location code entered in the previous field or a pre-set warehouse restriction. Press Enter to accept it.
17 If you entered a location, choose the applicable option for the Hold Code field:
If the item does not need to be placed on hold, press Enter to leave this field blank. 
If the item needs to be placed on hold, key in the code and press Enter. If the code is not known, use the pick list. 
If the field is populated, this indicates that either this item or the location where the product will be stored has an automatic hold attached to it. Press Enter to accept the current code or use the pick list to select a new code. 
18 The Remark and Accessorial blocks for this line will now appear on the screen for completion if you requested them in the Line Block. If none of these blocks apply, proceed to the next step.
If you need to complete the Remarks Block and/or Accessorial Block, see the corresponding procedures in [Entering Information in the Optional Blocks of ENRE](recebimento.html#entering-information-in-the-optional-blocks-of-enre). 
If this is a manual entry and … Then do the following …
You know the location Key in the location code of where the item will be stored and press Enter.
You know the location but the product for this line has to be stored in more than one location because it did not all fit into a single location
See the next section “Receiving a Single Item Line into Multiple Locations” (ver [Entering Line Information in ENRE](recebimento.html#entering-line-information-in-enre)).
You do not know the location yet Press Enter to bypass the field. Later, when you attempt to confirm the receipt, the system will prompt you that the location is missing. At that time, you must query this receipt in ENRE and key in the missing location in order to be able to confirm the receipt.

ENRE Line Block screen
19 You are taken back to the Line field at the beginning of the Line Block. A new line (Line 2) displays for you to continue entering the next item line from the receiving documents. If a new line number does not display, click on Create Record.
Repeat the Line Block procedure for each line (entity). The upper right hand corner of the screen displays a current record counter for your reference. 
When you have completed entering all of the receipt lines, click on Return to Main and Master Block.
a new Line 
Block record displays for completion

ENRE Header Block screen
20 You are now taken back to the beginning of ENRE where the system shows the receipt number it has generated.
21 If you wish to enter another receipt, click on Create Record. 
22 If you wish to exit the ENRE program, click on Exit. The following message may display on your screen: 
“The remaining Units are not 0, do you want to continue? (Yes) (No).” The system is alerting you to the fact that the number in the Total Units field of the Header Block does not equal the number of units that was entered in all of the Line Block records when they are added together. Key in Y.
Messages previously set up in Adjust Inventory Messages (ADIM) may appear in the Line Block. These messages are for display purposes only and do not print on any document or report.
RECEIVING A SINGLE ITEM LINE INTO MULTIPLE LOCATIONS
It may happen that the total amount of an item for a single receipt line does not fit into one warehouse location or that the item has to be split into more than one location for whatever reason. If this is the case, use the 
Location Block. This block allows you to store the receipt line in more than one location. 
1 Complete the ENRE Header Block. Complete the Line Block fields normally, but leave the Location field blank.
2 Click on Return to Main to exit create record mode.
system-generated receipt number

ENRE Line Block showing how to access the Location Block
3 Click on Location Block. The Location Block appears on the screen and the system fills in the Location 
Line Number.

ENRE Line Block showing the Location Block
Click on 
Location 
Block
Location 
Block lines for entering put-away instructions

4 Key in the location code of where the first portion of the product will be stored and press Enter.
The system populates the Warehouse Code field and skips over it.
5 Key in the quantity that will be stored in this location and press Enter.
6 Key in a hold code, if applicable, and press Enter. If you do not know the code, use the pick list.
If no hold code is necessary, press Enter. The cursor moves to the next Location Line Number (Line 2). 

Location Block showing Location Proof box
7 Note the Location Proof Box just above the Location Block on the right hand side, which indicates the following information:
When the balance indicates 0, it means that all units have been entered. 
8 In Line 2 of the Location Block, key in the location code, quantity and hold code for the next portion of the product that will be stored in this second location.
Repeat until the Location Proof Balance is 0. 
9 Click on Line Block.
10 If you need to enter another line in the Line Block, click on Create Record. To exit ENRE, click on Master 
Block and then Exit.
Total Total units received for this line
Entered Number of units entered into locations up to this point
Balance Number of remaining units that still need to be entered into locations. 

RE-RECEIVING INVENTORY
If you re-receive inventory, the following message may display “Caution, this entity is in the system, do you wish to re-receive? (Yes) (No).” The system is alerting you to the fact that this item — with these exact inventory levels — has been received into the warehouse before. You can click on Yes to re-receive the inventory or you can click on No to change one or more inventory levels.
The re-receive message only appears if the on-hand plus on-receipt quantity of the inventory being rereceived is greater than zero.
CREATING LOCATION CODES ON THE FLY
You can create new location codes while in ENRE without leaving the receipt entry program to enter LOCA (Locations).
1 Enter your receipt header information in the normal manner.
2 In the Line Block, enter your inventory levels for the item being received as well as the expected quantity.
3 Enter your new location code and press Enter.
4 Click on Create Code to enter LOCA (Locations).
LOCA screen in Create Record mode
5 In LOCA, enter your location information in the normal manner.
6 When the Line Block redisplays, continue to enter your receipt line in the normal manner.

### ENTERING INFORMATION IN THE OPTIONAL BLOCKS OF ENRE <a id="entering-information-in-the-optional-blocks-of-enre"></a>

If you indicated in the Header Block that you need to enter details in any of the ENRE Optional Blocks, they will appear now in succession. The following procedures will assist you in completing these blocks.

REMARKS BLOCK
The Remarks Block will appear on the screen if the Remarks field in either the Header Block or the Line Block is set to Y (for Yes). A remark can be any useful message that will appear on the screen. The remark will also print on the actual receipt document if this option was preset in your system.
1 Key in your remarks. 

Remarks Block screen showing two remark entries
2 When you finish entering all remarks for this receipt, click on Return. 
3 If you are in create record mode, the next optional block or the Line Block appears on the screen for completion. Continue to process the receipt in the usual manner.
EXTENDED REMARKS BLOCK
If activated in COMP (Company Code), the Extended Remarks screen allows you to attach one or more messages to a given receipt document. The message can be either a predefined message in MESS or a freetext message that you enter manually. Unlike the messages in DPME (Depositor Print Messages), these messages print for a specific receipt only.
NOTE No individual “word” can exceed 40 characters and no line can exceed 45 characters.

For example, if you select Customer Message and BF (Blast Freezing) as your message code, the text “Customer Message” and “BF (Blast Freezing)” will print on your selected document.
1 Select the checkboxes that apply to your remarks: Customer Message, Shipper Message or Carrier Message.
2 If required, select your document from the Document Code pick list.
3 Do one of the following:
Extended Remarks screen
4 Click on Save.
5 Click on Exit.
CARRIER BLOCK
The Carrier Block will appear on the screen if the Carrier Details field in the Header Block is set to E for Entry or B for Both. It records data concerning the transportation vehicle and the driver that brought the product to 
NOTE Adding the message to an actual document such as a bill of lading or receipt tally may require custom programming by HighJump.
If you are using a predefined message:
If you are entering a free-text message:
a) Select your message code from the Message Code pick list.
a) Key in a free-text message in the 
Message Text field.

the warehouse. You can capture information such as the power unit number, the trailer number, the seal numbers and the front, middle and back temperatures.
You can also capture your pallet in and pallet out quantities. Unlike pallets entered in the Pallet Block, pallets entered in the Carrier Block are not assigned a pallet type or an account and are not tracked in LOPC (Look 
Up Pallet Control).
Only the driver code is mandatory in the Carrier Details block. However, you must go through each field in this block before you can save a carrier record.
1 The Carrier Block is in the Create Record mode. Enter the Driver Code and press Enter. If you do not know the code, use the pick list. The system automatically fills in the Name field. 
If the driver’s name is not in the pick list, key in / and press Enter. Then enter the driver’s name in the 
Name field.
2 Enter the Power Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.

Carrier Block screen
3 Enter the Carry Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
4 Enter the Vessel Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
5 Enter the Voyage Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
6 Enter the Seal 1 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.
7 Enter the Seal 2 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the field.

8 Enter the temperature readings for the front, middle and back of the transportation vehicle, if applicable, and press Enter. If it does not apply, press Enter to bypass the three fields.
9 In the Setting field, if applicable, key in the temperature that the transportation vehicle’s thermostat control is set at and press Enter. If it does not apply, press Enter to bypass the field.
10 If required, key in your pallet in and/or pallet out quantities in the fields of the same name and press 
Enter.
11 If you are in create record mode, click on Exit to display the next optional block or the Line Block. Continue to process the receipt in the usual manner.

### Understanding Warehouse Restrictions <a id="understanding-warehouse-restrictions"></a>

This chapter only applies if your system uses more than one Warehouse Code for storing or putting away product and if your company performs manual put-away. 
The process of assigning where to put-away product can be done in either of two ways:
 automatically by AccellosOne 3PL (also called system-directed put-away)
 manually by warehouse personnel 
In ENRE, recording the put-away of an item involves three fields in the Line Block:
 Warehouse Code
 Location Code
 Hold Code
When completing ENRE in a system-directed put-away environment, you leave the Warehouse, Location and 
Hold fields blank for the Active Locator to complete. (The Active Locator is a software program that automatically assigns where to put away product when receiving and from where to pick product when shipping.)
When completing ENRE in a manual put-away environment, you record where the item has already been stored or leave it blank if the storage location is not yet known. Nonetheless, while recording the put-away location, the system may restrict you to certain warehouse and location codes. It is therefore helpful to be aware of the put-away options that are available and the restrictions that apply. Preset warehouse restrictions display as the system default. The system does allow you a few options, in specific circumstances, to override the system defaults.

### Preset Warehouse Restrictions <a id="preset-warehouse-restrictions"></a>

A warehouse restriction code may have been previously attached to either the customer of an item in (CUST) 
or to the item itself in (ITEM). 
If there are two preset warehouse codes, one in ITEM and one in CUST, the ITEM restriction overrides the one in CUST. 
When there is a preset code, it will appear as the default in the ENRE Line Block. When entering a receipt for such an item, you will be restricted to this warehouse and its locations for storing or putting away the product.

Preset warehouse restrictions apply to the whole receipt. If you have to enter fifty Line Block records for this receipt, this restriction will appear as the default every time.

### OPERATOR-SELECTED RESTRICTIONS <a id="operator-selected-restrictions"></a>

Different items (different receipt lines) on the same receipt may have to be put away in different locations. 
Because the preset warehouse restrictions apply to the whole receipt, the system allows you two options to override these restrictions in the Line Block. You therefore have some flexibility in ENRE when recording the put-away information for different lines. 
The first option, which is always available, allows you to restrict multiple lines of a receipt to a common warehouse. See [Restricting Multiple Item Lines to a Common Warehouse](recebimento.html#restricting-multiple-item-lines-to-a-common-warehouse).
The second option, which is only available on systems that have a warehouse restriction set in the Depositor 
Shipping and Receiving Profile (DSRP), allows you to restrict individual item lines to a specific warehouse. 
See the section [Restricting Individual Item Lines to a Specific Warehouse](recebimento.html#restricting-individual-item-lines-to-a-specific-warehouse).

### RESTRICTING MULTIPLE ITEM LINES TO A COMMON WAREHOUSE <a id="restricting-multiple-item-lines-to-a-common-warehouse"></a>

A warehouse restriction option is available in the ENRE Header Block in the Warehouse Code field. When you enter a code in this field, it automatically shows as the default in the Line Block’s Warehouse Code field. 
Also, only that warehouse’s locations will be available as put-away options in the Location Block. The 
Warehouse Code entered in this field will override any other preset warehouse restrictions attached to this item in (ITEM) or to this customer in (CUST).
This option is useful if you are entering a receipt with many line items and all or most of the receipt line items are to be stored in the same warehouse. For example, if you have a receipt with 100 line items and 90 are to be stored in the same warehouse, enter the Warehouse Code that applies to the 90 lines. This will save you keystrokes in the Line Block.
1 Enter ENRE. 
2 Complete the Header Block until you reach the Warehouse Code field. 
3 Key in the Warehouse Code that applies to the majority of the receipt item lines. If you do not know the code, use the pick list. 

Warehouse code entered in header becomes warehouse restriction default in the Line Block
4 Complete the Line Block for all item lines that will be stored in the same warehouse. 
5 Click on Return to Main and then Master Block to return to the Header Block. Press Enter until the cursor is in the Warehouse Code field. 
If the remaining line items will be placed in different warehouses, Press F11 (Clear Field) to leave the field blank and press Enter. 
If, on the other hand, there is another large group of line items to be stored in a common warehouse, key in that Warehouse Code and press Enter. If you do not know the Warehouse Code, use the pick list.
6 Click on Line Block.
7 Click on Create Record. Continue entering the remaining item lines in the usual manner.
a warehouse code entered here becomes the warehouse restriction default in the 

8 When all line items of the receipt have been entered, click on Return to Main and then Master Block. 
9 If you wish to enter another receipt, click on Create Record. If you wish to exit ENRE, click on Exit.

### RESTRICTING INDIVIDUAL ITEM LINES TO A SPECIFIC WAREHOUSE <a id="restricting-individual-item-lines-to-a-specific-warehouse"></a>

A warehouse restriction option may be available in the ENRE Line Block in the Warehouse Restriction field. 
However, this option is only available if this item has a warehouse restriction flag set up in its Depositor 
Shipping and Receiving Profile (DSRP). 
You will know whether this option is available if the cursor enters the Warehouse Restriction field. The Help 
Message Line will indicates “Enter a warehouse restriction if required.” If the cursor skips over the Warehouse 
Code field, then the option is not available for this receipt.
An entry in the Warehouse Restriction field will override all other warehouse restrictions previously applied to this item or line. That is, it will override any preset warehouse restrictions attached to this item or customer as well as any manually entered restriction in the ENRE Header Block, Warehouse Code field. When you enter a code in this field, it will automatically show as the default in the Line Block’s Warehouse Code field and only that warehouse’s locations will be available as options for storing the product.

ENRE Line Block with the Warehouse Restriction field set to 01
1 Enter ENRE. 
2 Complete the Header Block and the Line Block in the normal manner until you reach the Warehouse 
Code field. 
3 If the cursor enters the Warehouse Restriction field, choose the applicable option from the following:
If a warehouse restriction is not necessary, press Enter to leave the field blank.
If storage of this line item is to be restricted to a specific warehouse, key in the Warehouse Code and press Enter. If you do not know the code, use the pick list. 
If you enter a warehouse code in the 
Warehouse 
Restriction field, putaway is restricted to that warehouse 

4 Continue completing the Line Block for this record in the normal manner. 
5 If necessary, enter other Line Block records for each different item. When all line items of the receipt have been entered, click on Return to Main and then Master Block. 
6 If you wish to enter another receipt, click on Create Record. If you wish to exit ENRE, click on Exit.

### WAREHOUSE RESTRICTION SUMMARY <a id="warehouse-restriction-summary"></a>

The following table shows how the setting of the various AccellosOne 3PL warehouse restriction options affects put-away of product. 
CUST 
Warehouse 
Code Field
ITEM 
Warehouse 
Code Field
ENRE 
HEADER 
Warehouse 
Code Field
ENRE LINE 
Warehouse 
Restriction 
Field
RESULT IN ENRE LINE BLOCK
Warehouse Code Field
None None None None None. There are no warehouse restrictions.
None None None The warehouse restriction set in CUST will display as the default.
Put-away of product is restricted to this warehouse and its locations.
None None None The warehouse restriction set in ITEM will display as the default.
Put-away of product is restricted to this warehouse and its locations. 
None None The warehouse restriction set in CUST will display as the default. 
The CUST restriction overrides the ITEM restriction. 
Put-away of product is restricted to this warehouse and its locations.
None The warehouse restriction that was manually entered in the ENRE Header Block will display as the default. 
This manually entered warehouse restriction overrides both the ITEM and the CUST restrictions. 
Put-away of product is restricted to this warehouse and its locations.

### Modifying a Receipt <a id="modifying-a-receipt"></a>

You can re-open and modify receipts in ENRE as long as they have not been confirmed. Data in both the 
Header and Line Block fields can be changed.
You can check whether or not a receipt has been confirmed in the program LORE (Look Up Receipts). This program has a Status field, which will display “Confirm Receipt…” if the receipt has been confirmed. If the receipt has not been confirmed, the LORE Status field will show the name of the current flow process in the flow process sequence for this receipt.

### MODIFYING HEADER BLOCK DATA <a id="modifying-header-block-data"></a>

If you modify a receipt’s shipper and if that shipper has a workflow profile that differs from the customer’s workflow profile, AccellosOne 3PL will use the receipt’s original workflow profile, not the new workflow profile.
1 Enter ENRE. The program is in the Create Record mode.
2 Click on Enter Criteria.
The warehouse restriction that was manually entered in the ENRE Line Block Warehouse Restriction field will display as the default. 
This manually entered warehouse restriction overrides any other restriction in ITEM, CUST and the ENRE 
Header Block. 
Put-away of product is restricted to this warehouse and its locations.
CUST 
Warehouse 
Code Field
ITEM 
Warehouse 
Code Field
ENRE 
HEADER 
Warehouse 
Code Field
ENRE LINE 
Warehouse 
Restriction 
Field
RESULT IN ENRE LINE BLOCK
Warehouse Code Field

ENRE screen showing the method of calling up an unconfirmed receipt
3 Key in the system-generated number of the receipt that you want to modify. 
4 Click on Execute Query. The receipt will display on your screen. 
5 Press Enter to change from Main Mode to Modify Record mode.
6 Press Enter the required number of times until your cursor is in the field that you want to modify. Press 
F11 (Clear Field).
Set the program in the Enter 
Criteria mode.
Key in the number of the unconfirmed receipt that you wish to modify.
Press Execute Query.

ENRE screen showing Modify Record mode
7 Key in the new data and press Enter.
8 If you need to make additional changes to other Header Block fields, repeat steps 6 and 7 until all of the necessary changes are entered.
9 If you need to make changes to data in the Line Block, click on Line Block and follow the procedure below. 
10 When no further changes are required, click on Return to Main and then Exit to exit ENRE.

### MODIFYING LINE BLOCK DATA <a id="modifying-line-block-data"></a>

The following procedure applies to all types of Line Block records except for U (Unknown), which always allows you to open the receipt and fill in missing data.
1 Enter ENRE. 
2 Click on Enter Criteria. 
3 Key in the system-generated number of the receipt that you want to modify and click on Execute Query. 
The receipt will display on your screen. 
4 Click on Line Block. 
5 If this receipt has more than one Line Block record, key in the number of the Line Block record that you wish to change and press Enter. If not known, use your up and down arrow keys to find the Line Block number needing modification.
Set the program in 
Modify 
Record mode.
Press Enter until your cursor is in the field that you wish to change.

ENRE Line Block screen
6 If you need to change the Received Quantity and/or Location Code fields, press Enter until the cursor is in the desired field. Press F11 (Clear Field). Key in the new data and press Enter.
If you need to change the Product Code, Receive Date, Expiry Date or Expect Quantity fields, you will need to delete the entire Line Block record. Refer to[Deleting an Entire Line Block Record](expedicao.html#deleting-an-entire-line-block-record). 
7 Click on Return to Main to return to the beginning of the Line Block. Repeat steps 7 and 8 if you need to change any other Line Block records for this receipt or click on Master Block and Exit to exit the program.

### MODIFYING LOCATION BLOCK DATA <a id="modifying-location-block-data"></a>

You must have multiple locations assigned to the same receipt line before you can enter the Location Block and make changes to it.
The following procedure applies to all types of Line Block records except for U (Unknown), which always allows you to open the receipt and fill in missing data.
1 Enter ENRE. 
2 Click on Enter Criteria. Key in the system-generated number of the receipt that you want to modify and click on Execute Query. The receipt will display on your screen. 
3 Click on Line Block. 
4 If this receipt has more than one Line Block record, key in the number of the Line Block record that you wish to change and press Enter. If this number is not known, use your up and down arrow keys to find the 
Line Block number needing modification.
5 Click on Location Block.
6 Press Enter. You are now in Modify Record mode.
Enter the line number of the record that you wish to modify

ENRE Line Block screen showing the Location Block
7 Use the up and down arrow keys to move the cursor next to the Location Line that needs to be modified.
8 Press Enter the required number of times until the cursor is in the field that you need to modify. Key in the new data and press Enter.
If you want to move product from one location to another, you must reduce the quantity in the from location before you add to the quantity in the to location. You cannot add to the quantity in the to location first.
9 Click on Return to Main to return to the beginning of the Location Line Block. To enter a new line, click on 
Create Record. To exit, click on Line Block and Master Block. Then click on Exit.

### MODIFYING OPTIONAL BLOCKS DATA <a id="modifying-optional-blocks-data"></a>

The procedure for modifying the Remarks, Carrier Details, Accessorial Charges and Receipt Extra Charges blocks is the same. The following procedure uses the Remarks Block as an example for the procedure.
1 Enter ENRE. 
2 Click on Enter Criteria. Key in the system-generated number of the receipt that you want to modify and click on Execute Query. The receipt will display on your screen. 
Use the arrow keys to move the cursor next to the line that you need to modify. 
Press Enter to the field that you need to modify.

ENRE Header Block screen showing how to access the optional blocks
3 In the Header Block, press Enter until the cursor is on the Y of the Remark field.
4 Click on Remarks.

ENRE Remarks Block screen
5 Clear the existing data and key in the new remark.
6 When you finish making your corrections, click on Return. Then click on Return to Main and then Exit to exit.
Place the cursor in the field of the optional block that you wish to modify. 
Then click on the corresponding button.

### CHANGING THE INVENTORY LEVEL ON A RECEIPT LINE <a id="changing-the-inventory-level-on-a-receipt-line"></a>

You can change the inventory level on a receipt line in CHRL without the need to enter ENRE and enjoy full access to all the fields in that program.
1 Enter CHRL.
2 Key in your receipt number and press Enter.
CHRL screen
3 If the receipt has multiple lines, select the line whose inventory level you wish to change.
4 Key in your new level 2, 3 or 4 value and press Enter.
5 Click on Update Line.
6 Click on Exit.

### Deleting a Receipt <a id="deleting-a-receipt"></a>

Receipts may need to be deleted due to errors. You can delete receipts in ENRE as long as they have not been confirmed.
You can check whether or not a receipt has been confirmed in the program LORE (Look Up Receipts). This program has a Status field, which will display “Confirm Receipt…” if the receipt has been confirmed. If the receipt has not been confirmed, the LORE Status field will show the name of the current flow process in the flow process sequence for this receipt.

You can view details of deleted receipts in LORE. Deleted receipts remain in LORE until they are purged in the program Purge Orders, Receipts, Inventory (PURG).

### DELETING AN ENTIRE RECEIPT <a id="deleting-an-entire-receipt"></a>

1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in the system-generated number of the receipt that you want to delete and click on Execute Query. 
The receipt will display on your screen.
4 Press Enter. You are now in Modify Record mode and the Delete button will appear at the bottom of the screen.

ENRE Header Block showing the Delete entire receipt option
5 Click on Delete. 
Set the mode to Modify 
Record. 
Delete button displays as an option.

ENRE Header Block showing Deletion message
6 A message block displays asking if you want to proceed with the deletion. On your keyboard, key in the letter of whichever of the following options applies to your situation and press Enter.
If you choose R (Remarks Block), the receipt will be deleted and the Remarks Block will display. Key in the reason for deleting the receipt and press Enter. A message block appears indicating the receipt is being deleted.
7 Click on Exit to exit the ENRE program.

### DELETING AN ENTIRE LINE BLOCK RECORD <a id="deleting-an-entire-line-block-record"></a>

There may be situations in which you need to delete an entire Line Block record. For instance, this would be necessary under the following circumstances:
 to cancel an item from an unconfirmed receipt that was previously entered in ENRE 
 to change the Product Code, Receive Date, Expiry Date or Quantity Expected fields on a receipt
When you delete a receipt line record and then create a new receipt line, the line number of the new line depends on the number of lines on the receipt and the line number that you deleted. Refer to the following table for the renumbering rules in AccellosOne 3PL:
Y (Yes) If you wish to delete without entering any remarks as to why this receipt is being deleted.
N (No) If you do not want to delete this receipt.
R (Remarks) If you want to delete this receipt and include remarks explaining why this receipt is being deleted. The remarks will be saved with the deleted receipt.
If … then … you delete the first line of an receipt with a single receipt line the next new line created will be line 1

1 Enter ENRE. 
2 Click on Enter Criteria. 
3 Key in the system-generated number of the receipt you want to delete and click on Execute Query. The receipt will display on your screen. 
4 Click on Line Block.
5 Key in the number of the Line Block record that you wish to delete and press Enter. If not known, use your up and down arrow keys to find the line number needing deletion.

ENRE Line Block screen showing the Delete entire Line Block option
6 Press Enter until the Delete button appears at the bottom of the screen. 
you delete any line except the first line or the last line of an receipt with multiple receipt lines the next new line created will be the last line 
+ 1 you delete the last line of an receipt with multiple receipt lines the next new line created will be line number of the line that you just deleted
If … then …
Delete option

7 Click on Delete. A message block displays asking if you want to proceed with the deletion. Click on the appropriate button.
The line that you were on will disappear and the previous line number and its details will be displayed.
8 If you wish to create a new line with new data, click on Create Record and complete the Line Block in the usual manner. If you wish to exit, click on Return to Main and Master Block. Then click on Exit.

### DELETING LOCATION BLOCK DATA <a id="deleting-location-block-data"></a>

You use the following procedure to delete records from the Location Block. Records in the Location Block are composed of lines. (These are different than Line Block lines.) When you delete in the Location Block, you delete the whole line record.
1 Enter the Line Block. Key in the line number of the record that you wish to delete and press Enter. If not known, use your up and down arrow keys to find the line number that you need to delete.
2 Click on Location Block.

ENRE Location Block showing two line entries
3 Use the up and down arrow keys to move the cursor next to the line that you wish to delete.
4 Press Enter until the Delete button appears. Then click on Delete.
Y (Yes) If you wish to delete the Line Block record without entering any remarks as to why this record is being deleted.
N (No) If you do not want to delete this Line Block record.
Set the cursor at the end of the line that needs to be deleted

5 Click on Return to Main to return to the beginning of the Line Block. To Enter a new line, click on Create 
Record. To exit, click on Line Block and Master Block. Then click on Exit to exit.

### Receipt Header Types and Receipt Line Types <a id="receipt-header-types-and-receipt-line-types"></a>

There are six types of receipt headers in AccellosOne 3PL. The receipt header type indicates which of the automatic inbound handling and initial storage charges are to be applied to this receipt when it is rated. The profiles for these automatic charges were previously set up in AccellosOne 3PL for your warehouse company. 
P (Post Receiving) is the normal receipt type. It indicates to the system that the regular automatic charges for inbound handling and initial storage are to be applied to this receipt. You use the other five types in special circumstances when you need to override the normal charge setups.

### RECEIPT LINE TYPES <a id="receipt-line-types"></a>

Warehouse charges can vary for each item line of a receipt. Therefore, there are different receipt line types in 
AccellosOne 3PL to regulate the charges that are to be applied to each line. Be sure to select the correct receipt line type.
P (Post-receiving) Use if there are both inbound handling and initial storage charges to be applied to this item line. Also, all of the inventory levels must be known for the product. This is a regular receipt type line.
N (No Charge) Use if there are no charges to be applied to this item line.
H (Handling Only) Use if only the inbound handling charge is to be applied to this item line (that is, there will be no initial storage charge).
S (Storage Only) Use if only the initial storage is to be applied to this item line (that is, there will be no inbound handling charge).
I (In-transit) See [In-Transit Receipts](recebimento.html#in-transit-receipts).
C (Confirm) Use if you wish to confirm the receipt when you exit ENRE. This option allows you to enter and confirm a receipt in a single step without going through the standard inbound flows defined in DIFP.
P (Post-receiving) Use if there are both inbound handling and initial storage charges to be applied to this line. Also, all of the inventory levels must be known for the product. This is a regular receipt type line.
N (No Charge) Use if there are no charges to be applied to this line.
H (Handling Only) Use if only the inbound handling charge is to be applied to this line (that is, there will be no initial storage charge).

### Confirm-Type Receipts <a id="confirm-type-receipts"></a>

A confirm-type receipt is a receipt that you enter and confirm in a single step without going through the standard inbound flows defined in DIFP. When you exit ENRE after entering all your lines, AccellosOne 3PL will automatically confirm the receipt.
1 Enter ENRE.
2 In the Customer Code field, key in your customer code and press F9.
3 In the Receipt Type field, key in C for Confirm and press Enter. 
4 Complete the Header Block in the usual manner for the receipt.
S (Storage Only) Use if only the initial storage is to be applied to this line (that is, there will be no inbound handling charge).
O (Open Lot) See the Billing and Invoicing Guide for further information on this type of receipt.
X (Cross Dock) Use only for cross docking. If you enter this line type, you will be prompted to enter a cross dock profile in the Cross Dock field. Special inbound handling and initial storage charges will apply. See the 
Billing and Invoicing Guide for further information.
U (Unknown) See [Receipts With Unknown Inventory Levels](recebimento.html#receipts-with-unknown-inventory-levels).
I (In-transit) See [In-Transit Receipts](recebimento.html#in-transit-receipts).
NOTE Confirm-type receipts do not support directed put-away or the printing of inbound documents. You must manually enter your locations in the Line Block of 
ENRE.

ENRE screen showing confirm-type receipt
5 In the Line Block, enter all required information including the location code and warehouse code.
6 When you finish entering all your lines, press F4 the required number of times to exit.

### In-Transit Receipts <a id="in-transit-receipts"></a>

An in-transit receipt is a receipt that has been shipped to the warehouse but has not yet arrived. This receipt type is typically used when you receive an advance shipment notice of product to be received. After the product arrives at the warehouse, the system will change this to a P-type receipt during the receiving process. 
When you create an in-transit receipt, the receipt line’s quantities will display in the Location Block of Look Up 
Entity Information (LOEN) under the In-Transit column. Once the product arrives at the warehouse, the system changes the receipt line type from In-transit (I) to Post-receiving (P) and moves the receipt line’s quantities from the In-Transit column to the On Receipt column in the Location Block of LOEN.
RECEIVING AN IN-TRANSIT RECEIPT WHEN ALL INVENTORY LEVELS ARE 
KNOWN
1 Enter ENRE.
2 In the Customer Code field, key in your customer code and press F9.
3 In the Type field, key in I for In-Transit and press Enter. 
4 Press Enter again to bypass the Customer Code field.
5 Complete the Header Block in the usual manner for the receipt.

6 Complete the Line Block in the usual manner for the receipt. Enter all inventory levels but do not enter locations.
7 When you finish entering your receipt lines, click on Return to Main and Master Block. Then click on Exit to exit.
8 Advance the flow of the receipt in CHRF. 
9 Return to ENRE and enter your location information.
10 Confirm the receipt in the usual manner. A pop-up box will appear with the message “Change In-transit to 
Post Receiving”.
RECEIVING AN IN-TRANSIT RECEIPT WHEN ALL INVENTORY LEVELS ARE 
NOT KNOWN
1 Enter ENRE.
2 In the Customer Code field, key in your customer code and press F9.
3 In the Receipt Type field, key in I for In-Transit and press Enter. 
4 Press Enter again to bypass the Customer Code field.
5 Complete the Header Block in the usual manner for the receipt.
6 In the Line Block, press F9 (Previous Field) to position your cursor in the Type field. Then key in U for 
Unknown and press Enter. 
7 Enter the inventory levels that are known and bypass any levels that are not known. 
8 When you finish entering your receipt lines, click on Return to Main and Master Block. Then click on Exit to exit.
9 Enter the missing inventory levels when known.
10 Advance the flow of the receipt in CHRF. 
11 Return to ENRE and enter your location information.
12 Confirm the receipt in the usual manner. A pop-up box will appear with the message “Change In-transit to 
Post Receiving”.

### Receipts With Unknown Inventory Levels <a id="receipts-with-unknown-inventory-levels"></a>

A receipt line type of U for Unknown allows you to create a receipt for an item when there is missing data for some of the item’s inventory levels. A regular P (Post-receiving) type of receipt line would not allow you to bypass inventory level fields.
You must return to a U-type receipt line and complete the missing information before confirming the receipt in 
Time-Stamp and Confirm Receipts (CHRF).
Item quantities of U-type receipt lines do not show in LOEN because their inventory levels are missing. When the missing inventory levels are completed in ENRE, then they will appear in LOEN.
1 Enter ENRE.
2 Leave the Header Block’s Receipt Type field as P. Complete the Header Block in the usual manner.

3 When the screen displays the Line Block, press F9 (Previous Field) until the cursor is in the Type field. 
Key in U and press Enter.
4 Complete the Line Block fields until you reach Item Code.
5 Key in the Item Code and press Enter. If you do not know the code, use the pick list.

ENRE Line Block showing an Unknown receipt type
6 Press Enter to bypass any inventory level fields with missing information. Key in the information for inventory level fields with available data. Press Enter.
7 Continue completing the Line Block fields in the normal manner. The system will bypass the Location 
Code field as you cannot enter location information for a receipt line until the missing inventory levels are entered.
8 In the Hold Code field, key in your hold code and press Enter. If you do not require a hold code, press 
Enter with no code entered to bypass this field.
9 Enter any remaining receipt lines. When you finish, click on Return to Main and Master Block. Then click on Exit to exit ENRE. 
10 Do not confirm the U-type receipt line. You must return to this receipt and complete the missing inventory levels once you know them.

### LOOKING UP PENDING RECEIPTS IN LOPR <a id="looking-up-pending-receipts-in-lopr"></a>

You look up pending receipts in LOPR (Look Up Pending Receipts). A pending receipt is a receipt containing one or more U-type lines indicating missing inventory levels.
For each pending receipt that you look up in LOPR, AccellosOne 3PL shows the receipt number, the line number for the unknown inventory, the receipt date, the pending quantity, the pending weight and the pending cube.
In an 
Unknown receipt type, the system allows you to bypass inventory levels with missing data

1 Enter LOPR.
2 Key in your search criteria for each field and press Enter. You can query on customer code, any inventory level except the lowest level and receipt date. 
3 When you finish entering your search criteria, click on Execute Query.

LOPR screen
4 When you finish looking up your pending receipts, click on Exit to exit.

### ENTERING THE MISSING INVENTORY LEVELS IN AN UNKNOWN RECEIPT <a id="entering-the-missing-inventory-levels-in-an-unknown-receipt"></a>

When you enter the missing inventory levels in ENRE, AccellosOne 3PL changes the line type from U for 
Unknown to P for Post-Receiving. 
1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in the receipt number of the U-Line receipt and click on Execute Query.
4 Click on Line Block.
5 Key in the Line Block number of the U Line record that you need to complete and press Enter or use the up and down arrow keys to find it.

ENRE Line Block screen showing an Unknown receipt type
6 Press Enter until the cursor is in the first Inventory Level with missing data. Key in the data and press 
Enter.
7 Key in the data for other Inventory Levels, if applicable, and press Enter.
8 If this is a manual put-away and the location code is missing, press Enter until the cursor is in the Location Code field, key in the Location Code and press Enter.
9 Key in the hold code, if applicable, or press Enter to bypass the field.
10 Repeat the procedure for any other U-type receipt lines. 
11 When you finish updating your U-type lines, click on Return to Main and Master Block. Then click on Exit to exit the program.

### Sequential Entry Receipts <a id="sequential-entry-receipts"></a>

A sequential entry receipt is a receipt in which you enter your higher inventory levels (for example, levels 1 and 2) once and these levels are automatically attached to lower levels (for example, level 3). Sequential entry allows you to avoid repetitive entry of the same data.
For example, suppose you have a three-level inventory profile consisting of item/lot/pallet ID and you are receiving a lot with 20 pallets on it. Sequential entry allows you to enter the item code and lot number once for all 20 pallets; when you key in your pallet ID’s, the system attaches them automatically to the same item code and lot.
Complete the missing inventory level data and the location code

To set up sequential entry, enter the Level Block of DILP (Depositor Inventory Level Profile) and arrow down to the level of inventory that changes when receiving. Then use your pick list to select A for Receipt Entry from the Sequential Entry field.

DILP screen showing Sequential Entry field set to Receipt Entry for Level 3 (PID)

### PROCEDURE <a id="procedure"></a>

You enter a sequential entry receipt by entering all inventory levels for your first receipt line in the normal manner. Then you key in the number of times that you wish to repeat the same level 1/2/3 values for each new inventory entity for which sequential entry is activated.
If you wish to bypass sequential entry on a specific receipt line, you do not enter the number of times that you wish to repeat your higher inventory levels. When you bypass sequential entry, you will be required to enter all inventory levels for each receipt line.
In the following example, you are receiving a three-level item (item, lot, and pallet ID) and sequential entry is activated for level 3 (pallet ID).
1 Enter ENRE and key in your header information normally.
2 When the Line Block appears, key in all inventory levels for the first inventory entity that you are receiving. When you finish entering your last inventory level, your cursor will be positioned in a blank field on the right-hand side of your screen.

ENRE screen showing cursor in blank field
3 Key in the number of times that you wish to repeat the same item, lot and date code for each new pallet 
ID and press Enter. If you wish to bypass sequential entry for this receipt line, leave the field on righthand side of the screen blank and press Enter.
You enter the number of times that you wish to repeat this item and lot here

ENRE screen showing the number of lines for item D1, lot 102
4 Enter the expected and received quantities for this pallet ID plus any other required information until your line is complete. When you finish entering your first line, AccellosOne 3PL will create a second line showing inventory levels 1, 2 and 3 filled in with the values from the previous line.
Number of lines for item 
D1, lot 102

ENRE screen showing values for levels 1 and 2 automatically entered by the system
5 Key in your lowest inventory level and press Enter. If required, make any necessary adjustments to the value showing the remaining number of lines for this item/lot. Then enter the remaining information in the 
Line Block normally.
6 Repeat the above steps for each additional pallet ID that you wish to receive under the same item/lot/ date code.
7 When you finish receiving all pallets for this item/lot/date code, AccellosOne 3PL will create a new line. 
All inventory levels will be blank and you will have to enter all levels manually.
8 Enter a new line or click on Return to Main, Master Block and Exit to exit.

### Receipts With System-Generated Inventory Levels <a id="receipts-with-system-generated-inventory-levels"></a>

If your system is set up to automatically create level 2, 3 or 4 values using system-generated numbers, you can leave the inventory level blank and AccellosOne 3PL will generate a number for it. Depending on your 
Second line shows item and lot information from previous line
Remaining number of lines for this item and lot

system setup in DILP (Depositor Inventory Level Profile), your system-generated number may be generated immediately or may be generated when you create a new receipt line.
In the following example, you are receiving a three-level item (item/lot/pallet ID) and your third level — pallet 
ID — is system generated.
1 Enter ENRE and key in your header information in the normal manner.
2 Do one of the following:
3 When the Line Block appears, key in your item code and press Enter.
4 Key in your lot number and press Enter.

ENRE screen showing cursor positioned in the Pallet ID field
CAUTION Only one user can enter a receipt line with system-generated inventory levels at any given time. If multiple users enter receipts in your facility, you must make sure that you complete the receipt line as quickly as possible so as not to lock out other users. For example, if you enter your levels 1 and 2 as well as the expected and received quantities but do not complete the line, no other user will be able to create new receipt lines for that customer until you complete the line or exit.
If you want the system to generate your pallet ID:
If you want to enter your pallet ID manually:
a) You must enter a warehouse code in the receipt header.
a) You can leave the Warehouse 
Code field blank.

5 Do one of the following:

ENRE screen showing system-generated pallet ID
6 Enter the expected and received quantities for this pallet ID plus any other required information until your line is complete.
7 Enter another receipt line or click on Return to Main and Master Block to exit the Line Block. Then click on Exit to exit.

### Receiving Variable Quantity Breakdown Inventory <a id="receiving-variable-quantity-breakdown-inventory"></a>

A variable quantity breakdown item is an item whose quantity breakdown is not fixed. For example, lot 101 of a given item has 60 cases per pallet, while lot 102 of the same item has 80 cases per pallet.
If you want the system to generate your pallet ID:
If you want to enter your pallet ID manually:
a) Press Enter to bypass the Pallet 
ID field. Your system-generated pallet ID may or may not appear on your screen depending on the options that you selected in 
DILP.
a) Key in your pallet ID and press 
Enter.

When you receive a variable quantity item and the inventory entity that you are receiving is being received for the first time, you can change the inventory entity’s quantity breakdown. Once you change an inventory entity’s quantity breakdown, the new quantity breakdown is fixed and cannot be changed on future receipts for that inventory entity.
ITEM screen showing Variable Quantity Breakdown flag set to Y for Yes for item A2
1 In the Line Block of ENRE, press Enter the required number of times to bypass the Remark, Process, 
Charge and Warehouse Restriction fields.
2 Key in your item code and press Enter.
3 Key in your level 2, 3 and 4 values and press Enter.

ENRE screen showing PLT field highlighted (that is, an enterable field)
In the Quantity Breakdown field, AccellosOne 3PL will show the SKU’s used to track and bill the item. For example, if the Quantity Breakdown field shows PLT: 100 (the largest SKU) and CASE: 1 (the smallest 
SKU), you read it as one pallet has 100 cases.
4 Do one of the following:
5 Enter the expected quantity and received quantity of the new product and continue to enter your receipt line normally.
6 When you finish entering your receipt line, press F4 the required number of times to exit.

### CHECKING AN ITEM’S VARIABLE QUANTITY BREAKDOWN IN CVQB <a id="checking-an-item-s-variable-quantity-breakdown-in-cvqb"></a>

The special verify program CVQB (Check Qty Breakdown and Receipt Qty) allows you to check an item’s variable quantity breakdown and correct it if it is wrong. It can be attached to any inbound flow after ENRE (Enter Receipt).
1 Enter CHRF and advance the receipt’s inbound flow in the normal manner until you reach the flow to which CVQB is attached.
If you are receiving the inventory entity for the first time and wish to change the quantity breakdown:
If you are receiving the inventory entity for the first time and do NOT wish to change the quantity breakdown:
If you have already received the inventory entity:
a) Key in a new quantity breakdown and press Enter.a) Press Enter to accept the default quantity breakdown.
a) Proceed to next step.

CVQB screen showing receipt lines being checked
2 Use your arrow keys to scroll through the list of variable quantity breakdown inventory.
3 If you see a record that you wish to correct, press Enter to position your cursor in the Quantity Breakdown field.
4 Key in your new quantity breakdown and press Enter.
5 When you finish checking your inventory in CVQB, click on Exit to exit.
AUTOMATICALLY UPDATING AN ITEM’S VARIABLE QUANTITY BREAKDOWN IN 
URQB
The special verify program URQB (Update Receipt Quantity Breakdown) automatically updates an item’s quantity breakdown when the standard quantity breakdown in ITEM does not match the expected/received quantity in ENRE. For example, suppose an item’s standard quantity breakdown is 100 cases and you receive 105 cases in ENRE. AccellosOne 3PL will automatically update the inventory entity’s quantity breakdown to 105 cases per pallet.
URQB can be attached to any inbound flow after ENRE (Enter Receipt). It runs in the background and does not display on your screen.

ENRE Line Block showing mismatch between the standard quantity breakdown (100 cases) and receive quantity (105 cases)

### Look-Up Programs <a id="look-up-programs"></a>

AccellosOne 3PL has programs that allow you to view data concerning receiving, shipping and inventory status. These look-up programs only allow you to view data — you cannot modify, add or delete data in these programs. The most commonly used look-up programs for operations are Looking Up Receipts (LORE), 
Looking Up Orders (LOOR), Look Up Entity Information (LOEN) and Look Up Location Information (LOLO).
In the look-up programs, you must first instruct the system to find the records you want to view. There are three ways of looking up records in look-up programs:
 you can view all records in the program
 you can view a single record
 you can view all records that meet common selection criteria

### VIEWING ALL RECORDS <a id="viewing-all-records"></a>

Leaving a look-up program screen blank (i.e., by not entering any selection criteria) and executing a query will retrieve all records in that program.
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Click on Execute Query.
3 The system retrieves all records in the program. Check the current record counter to know which record you are viewing currently and how many records there are in total.
4 Use the up and down arrow keys to scroll from one record to another.

Look-up screen for LORE program
5 When you find the record that you are looking for, view the Header Block and then click on the corresponding button of any record block that you wish to view. When you finish viewing the record, click on the appropriate button to exit the block.
6 Repeat the previous step for each additional block that you wish to view.
7 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
8 When you have finished viewing all records, click on Exit in the Master Block to exit the program.

### VIEWING A SINGLE RECORD <a id="viewing-a-single-record"></a>

To view a specific record when you know the system-generated record number, you use the following 
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Key in the number of the record. 
3 Click on Execute Query.
The record will display on the screen. 
4 When you find the record that you are looking for, view the Header Block and then click on the corresponding button of any record block that you wish to view. When you finish viewing the record, click on the appropriate button to exit the block.
5 Repeat the previous step for each additional block that you wish to view.
6 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
Use the up and down arrow keys to scroll from record to record.
Press the appropriate buttons to view the block details of the record that you are currently viewing

7 When you have finished viewing all desired records, click on Exit in the Master Block to exit the program.

### VIEWING ALL RECORDS WITH COMMON SELECTION CRITERIA <a id="viewing-all-records-with-common-selection-criteria"></a>

This method is useful when you do not know the specific record number of the record that you are looking for but you do know other detail(s) about the record. You use the detail(s) that you do know about the record as selection criteria. 
The system will only retrieve records with these criteria in common. This will be faster than having to scroll through all records in the program to find the one you need.
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Key in the information that you do know about the record in the corresponding fields. For instance, if you know the Receipt Date of the record you are looking for and there is a Receipt Date field, key in the date.
The more fields you complete the more you restrict the search. The system will retrieve fewer records for you to search through.

Look-up screen for the program LORE
3 Click on Execute Query. The system retrieves all records that meet the selection criteria.
4 Use the up and down arrow keys to scroll from one record to another until you find the record that you are looking for. 
5 View the Header Block and then click on the corresponding button of any record block that you wish to view. When you finish viewing the record, click on the appropriate button to exit the block.
6 Repeat the previous step for each additional block that you wish to view.
7 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
In this example, 
Execute 
Query will call up all records for customer D that involved carrier ABC and had a receipt date of 01.15.07

8 When you have finished viewing all desired records, click on Exit in the Master Block to exit the program.

### Looking Up Telephone Information in LOTE <a id="looking-up-telephone-information-in-lote"></a>

You can look up telephone information in LOTP (Look Up Telephone Numbers). For each number that you look up, LOTE shows the telephone number, telephone list code, account type, account name, contact name and contact position.
In LOTE you can query by telephone number, telephone list type and account type.
1 Enter LOTE.

LOTE screen
2 Key in your selection criteria. You can search by telephone number, telephone list type (FAX, CELL, 
MAIN or whatever other list types you have defined in TETP) or account type (CU for Customer, BR for 
Broker, CO for Consignee, FR for Freight, GE for General, SH for Shipper or SO for Sold-To).
3 When you finish entering your selection criteria, click on Execute Query.

LOTE screen showing 10 telephone numbers whose list code is FAX
4 When you finish looking up your telephone numbers, click on Exit to exit.

### Looking Up Receipts in LORE <a id="looking-up-receipts-in-lore"></a>

The program Look Up Receipts (LORE) allows you to view all receipts that have been entered into AccellosOne 3PL and that have not been purged. In LORE, it is possible to view receipts of any status — whether entered, confirmed, rated or deleted. 
In LORE, you can see all of a receipt’s details. The Status field shows the current inbound flow process for this receipt. This lets you know where you are in the flow process sequence. LORE also indicates whether or not there are outstanding documents to print for this receipt. 

LORE screen showing the Receipt Block details of receipt number 1209
LORE consists of the following sections:
 Receipt Block (Header Block)
 Time-Stamping Block
 Line Block
 Optional Detail Blocks (if applicable)
The following procedure allows you to view the details of a receipt in the various blocks of LORE. An explanation of the LORE fields and the data they contain follows this procedure.
1 Enter LORE. You are in the Enter Criteria Mode.
2 If you wish to view a specific receipt, key in the Receipt Number and click on Execute Query.
If you wish to view all ENRE receipts, click on Enter Criteria and click on Execute Query.
If you wish to view receipts that meet specific criteria, enter your selection criteria in the corresponding field(s) and click on Execute Query.
The Receipt Block details display for you to view.
3 Click on Time Block. The receipt’s time-stamping details display for you to consult.
4 Click on Master Block.
5 Click on Line Block and the Line Block details display for you to view. Use your up and down arrow keys to move from one Line Block record to another.
6 Click on Master Block.
receipt’s status in the flow process sequence the next document in the flow process sequence that needs to be printed

LORE screen showing the Optional Block fields
7 Check the optional blocks fields. If Y, E, C or B is entered next to any of these blocks, there are details. 
Press Enter until the cursor is in the optional field that you want to view. Then click on the appropriate button and the optional block details display for you to view. 
8 Click on Master Block. If you want to view another receipt’s details, check the current record counter. If there is more than one record, use the down arrow key to scroll to the next record. 
If there is only one record, click on Enter Criteria and key in the selection criteria for the next receipt that you wish to view.
9 If you want to exit the program, click on Exit in the Master Block.

### RECEIPT BLOCK <a id="receipt-block"></a>

The LORE Receipt Block contains basically the same information as the original ENRE receipt. It does, however, have some extra fields as described below: 
If Y, E, C or B displays next to any of the optional blocks, there are details. Move the cursor to the field and the button displays as the option for that block.

LORE screen showing the Receipt Block details for receipt number 1209
FIELD DESCRIPTIONS
Rated Y = Yes
N = No
This flag indicates whether or not the receipt has been rated.
Status The current flow process of this receipt in terms of the flow process sequence. 
Also displays the date and time when the receipt received this status.
On Order The corresponding Order Number if this is a Transfer receipt type.
Receipt Date The date entered in the Receipt Date field of ENRE when the receipt was created.
Received Date The date entered in the Receive Date field of CHRF when the receipt was confirmed in Time-Stamp and Confirm a Receipt (CHRF). 

### TIME-STAMPING BLOCK <a id="time-stamping-block"></a>

The Time-Stamping Block displays details regarding the flow processes that have been completed up to this point for this receipt. If there is a document attached to a flow and this document has been printed, you can click on the View icon to see a PDF version of the document.
If the Appointment Remarks button is enabled, you can look up remarks entered in APPL (Appointment 
Planner) for the appointment’s receipt.
Invoice Date The date when the invoice or warehouse receipt was rated. If your system rates the receipt automatically as it is confirmed, this date will always be the same as the Received Date. If you rate receipts manually in Receipt Rater (RCRA), the Received Date and the Invoice Date may be different if the two processes were performed on different dates. 
Location Status Indicates whether all of the receipt’s lines have been assigned a location yet (Entered) or whether they are still unassigned (Missing). 
O/S Receipt Reference 
Receipt Source Receipt 
Number
Applicable only to EDI users 
When a very large shipment is divided up and entered in ENRE as more than one receipt, the related receipt number displays in this field for reference purposes. (EDI generates the reference number.)
Remarks and Carrier 
Details
Y = Yes
N = No
C = Confirmation
B = Both
E = Entry
If Y, E, C or B is entered next to any of these fields, there are details entered in that block. To view the details, press Enter until the cursor is in the optional field that you want to view. Then click on the appropriate button and the optional block details will display.
Document Status Indicates whether there are any outstanding receiving documents to print for this receipt. Names the next document that requires printing according to the 
FIELD DESCRIPTIONS

LORE screen showing Time-Stamping Block

### LINE BLOCK <a id="line-block"></a>

The LORE Line Block shows basically the same fields and details that appear in the original receipt’s ENRE 
Line Block. There is one difference to note, however, which is in the Receive Date field. This field is blank if the receipt or the receipt line has not been confirmed. 
FIELD DESCRIPTIONS
Date The date when the flow displayed in the Flow Process column was performed.
Time The time when the flow displayed in the Flow Process column was performed.
Flow Process The flow processes that have been performed and advanced for this receipt at the time of viewing.
If the view icon is highlighted, you can click on the icon to view and print the document in PDF format.
If the e-File icon is highlighted, you can click on the icon to view and print the e-File or Signature Capture document.
Operator The operator who advanced the flow process.

If the entire receipt was confirmed in Time-Stamp and Confirm a Receipt (CHRF), then all of the receipt’s Line 
Block lines will display the same Receive Date. This date is the same as was entered in the Receive Date field of CHRF when the receipt was confirmed.
If only individual lines of the receipt were confirmed in Confirm Receipts - One Line at a Time (CORL), then the confirmed lines will display a date in the Receive Date. This will be the same as was entered in the 
Receive Date field of CORL when the line was confirmed. The receipt lines that have not yet been confirmed will have a blank Receive Date field.

### OPTIONAL BLOCKS <a id="optional-blocks"></a>

The LORE Optional Blocks show the same fields and details that appear in the original receipt’s ENRE 

### LOOKING UP AN ITEM SUMMARY <a id="looking-up-an-item-summary"></a>

The item summary command allows you to look up a summary of all receipt lines by item rather than by receipt line. That is to say, if you have multiple receipt lines for the same item, the lines will be consolidated into a single line.
1 Retrieve the receipt that you wish to look up.
2 Click on Item Summary.
LORE screen showing item summary
3 When you finish looking up your item summary, click on Receipt Header and Exit to exit.

### CHANGING THE DEFAULT SORT SEQUENCE IN LORE <a id="changing-the-default-sort-sequence-in-lore"></a>

The default sort sequence in LORE is oldest receipt first, then second oldest receipt, followed by third oldest receipt, etc. You can change the default sort sequence to show the newest receipts first by means of the Ctrl 
+ A command.
1 Enter LORE.
NOTE Line Block details do not display for deleted receipts.

2 Query any receipt.
3 Press Ctrl + A. The message “Sequence will be descending” will display in the message area of your screen.
4 Perform your query. To retrieve all receipts, leave all query fields blank.
AccellosOne 3PL will retrieve your receipts in descending sequence; that is, newest receipt first, then second newest receipt, followed by third newest receipt, etc.

### Printing the Receiving Documents <a id="printing-the-receiving-documents"></a>

Receipts entered in ENRE may have documents attached to them. Each document is attached to a specific flow process that was set up in DIFP. These documents need to be printed before you can proceed to the next flow. You print these documents in PRRM (Print Receiving Documents - Specific) or in a batch print through 
PRRE (Print Receiving Documents - All).

### PRINTING A DOCUMENT FOR SPECIFIC RECEIPTS IN PRRM <a id="printing-a-document-for-specific-receipts-in-prrm"></a>

You use PRRM (Print Receiving Documents - Specific) to print the same document for specific receipt numbers that have been entered in ENRE. You can print for a single specific receipt (Receipt Number 5 needs its Tally document printed) or for multiple specific receipts (Receipt Numbers 1, 25 and 46 each need their Tally document printed).
PRRM consists of the following sections:
 Header Block
 Receipt Block
 Print Block
The Header Block in PRRM lists all of the receiving documents. If you do not know which document to print at this point in the flow process sequence, you can check in LORE. The Document Status field in LORE specifies the next document that needs to be printed. The following example shows the steps required to process a receipt that has the inbound flow processes ENRE, UNLO and CORE:
FLOW 
PROCESS
ATTACHED 
DOCUMENT REQUIRED ACTION
ENRE (Enter 
Receipt)
Tally document a) Enter PRRM and print the Tally
UNLO (Unload) None a) Enter CHRF. Select and time-stamp the 
UNLO flow.
CORE (Confirm 
Receipt)
Warehouse Receipt a) Select and time-stamp the CORE flow in 
CHRF
b) Enter PRRM and print the Warehouse 
Receipt

1 Enter PRRM.
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document that you wish to print.

PRRM screen showing Header Block with documents
3 Click on Receipt Block.
4 Click on Create Record.
5 Key in the number of the receipt whose attached document you need to print and press Enter.
6 If there are other ENRE receipts that need this same document printed, key in each receipt number and press Enter.

PRRM screen showing the Receipt Block
7 Click on Return to Main and then Print Block.
a) Execute Confirm
FLOW 
PROCESS
ATTACHED 
DOCUMENT REQUIRED ACTION
Place your cursor next to the document type that needs to be printed
The tally document attached to receipt numbers 
1149 and 1153 will be printed

PRRM screen showing the Printer Block
8 Key in the code of the printer where this document is to print and press Enter. If you do not know the code, use the dropdown list.
9 Click Ok. The document will print and the system returns to the Main Menu.

### PRINTING A DOCUMENT FOR ALL RECEIPTS IN PRRE <a id="printing-a-document-for-all-receipts-in-prre"></a>

You use PRRE (Print Receiving Documents - All) to print the same document for all ENRE receipts that are at the same stage in their flow process and that need this document printed. 
You can also use PRRE to print the same document for all ENRE receipts that meet common criteria and that are at the same stage in their flow process. In this case, you use the Query Block to enter the selection criteria that the receipts have in common. The system will then call up only these receipts for printing of the attached document. For example, if you need to print the tally document for all receipts that were entered on 
June 23rd for Customer A, you would fill in the date and the customer fields accordingly and instruct the system to execute the query for these restrictions.
PRRE consists of the following sections:
 Header Block
 Query (Restriction) Block
 Receipt Block
 Print Block
1 Enter PRRE.

PRRE screen showing Header Block with documents
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document that you wish to print.
3 Click on Query Block.

PRRE screen showing the Query Restriction Block
4 In the Header Block, you selected a document for printing. The Query Restriction Block now provides you with two options to print this selected document:
you can instruct the system to retrieve all receipts that are at this step in their flow process you can instruct the system to retrieve all receipts that are at this step in their flow process and that have common criteria
Place the cursor next to the document that needs to be printed
A blank Query 
Restriction 
Block and Execute Query causes all receipts that need the selected document printed to display in the 

5 Do one of the following:
If you wish to print the document in the Header Block for all receipts that are at this step in their flow process:
If you wish to print the document in the Header Block for a specific receipt:
If you wish to print the document in the Header Block for receipts that have common criteria:
a) Proceed to step 6. a) Key in the receipt number and press Enter.
a) Key in the common selection criteria in the corresponding field or fields. Use the following table as a guide:
Completing this field … will print the document selected in the Header Block for …
Customer Code all receipts that belong to this customer. 
Shipper Code all receipts that belong to this shipper.
Carrier Code all receipts that belong to this carrier
Receipt Date - Start all receipts that were created in ENRE with a Receipt Date starting from the date you specify here.
Receipt Date - End all receipts that were created in ENRE with a Receipt Date up to the date you specify here
Received Date - Start all receipts that were confirmed starting from the date that you specify here
Received Date - End all receipts that were confirmed up to the date that you specify here
Appointment Date - Start all receipts that have an appointment date starting from the date that you specify here. 
This refers to appointments that are set up in the Appointment System — appointments scheduled at the warehouse doors for pick-up and delivery purposes.
Appointment Date - End all receipts that have an appointment date up to the date that you specify here. This refers to appointments that are set up in the 
Appointment System — appointments scheduled at the warehouse doors for pickup and delivery purposes.

6 Click on Execute Query. The system displays the Receipt Block where it shows all receipts that meet the selection criteria that you specified.

PRRE screen showing the Receipt Block
7 Click on Print Block.
8 Key in the code of the printer where these document are to print and press Enter. If you do not know the code, use the dropdown list.
9 Click Ok. The documents will print and the system returns to the Main Menu.
Type all receipts that are of the ENRE Header 
Block receipt type
Priority all receipts that have this priority code
Operator Code all receipts that were entered by the operator that you specify here
EDI Group Value the selected document for all receipts that have the same EDI Group Value field that you specify here
Completing this field … will print the document selected in the Header Block for …
In this example, clicking 
Print Block will print the tally document for all of the receipts that have been called up in the 
PRRE Receipt 
Block. 

### CANCELLING OR REPRINTING RECEIPT DOCUMENTS <a id="cancelling-or-reprinting-receipt-documents"></a>

Normally, receipt documents must be printed according to the flow process sequence. RERE (Requeue 
Receipt Documents) allows you to print a document out of sequence under certain circumstances.
You use the program RERE when you have to:
 cancel the printing of a document that is attached to a flow process
 reprint a document that is attached to a flow process
When you enter a receipt number into RERE, the program indicates the following information:
 the receipt’s current flow process
 the document attached to this flow process
 the number of times that this document has been printed to date
 the print status of this document.

RERE screen
The document print statuses in RERE are:
 all documents have been printed
 to be printed
 printed
 cancel
 requeue
Depending on the document print status, you have the option of cancelling the printing of the document or reprinting it as necessary. The following table shows the options that are available depending on the document status.
Receipt’s current flow process
Document attached to this flow process
Number of times this document has been printed
Print status of this document

### CANCELLING RECEIPT DOCUMENTS IN RERE <a id="cancelling-receipt-documents-in-rere"></a>

Cancelling the printing of a document that is attached to a flow process may be necessary if circumstances require you to advance to the next flow without printing the document attached to the current flow.
Use the following procedure when the RERE Print Status field indicates “To be printed” and you need to reprint the receipt.
1 Enter RERE.
2 Key in the receipt number and press Enter. The system displays the documents that are attached to this receipt’s current flow process. 
3 Check that the print status indicates “To be printed”. If there is more than one document, use the arrow keys to place the cursor beside the document that you wish to reprint. 
4 Click on Cancel key. Note that the print status indicates “Cancel”. 
PRINT STATUS DESCRIPTION OPTIONS 
All documents have been printed.
There are no more documents left to either requeue (reprint) or cancel. The receipt has been confirmed. All process flows have been completed and all documents attached to these process flows have been printed.
None. The Help Message Line displays “This receipt has no documents to be requeued or cancelled.”
To be printed The displayed document(s) has not been printed before. It needs to be printed now according to the flow process sequence.
To cancel printing of this document, click on 
Cancel. The system will now allow you, in 
CHRF, to proceed to the next flow of the flow process sequence.
To print the document, exit RERE. Enter PRRM and print the document.
Printed The displayed document has been printed before.
Click on Requeue to reprint this document. 

RERE screen
5 Click on Receipt Number and Exit to exit the program
6 Enter CHRF. Continue confirming the receipt in the usual manner.

### REPRINTING RECEIPT DOCUMENTS IN RERE <a id="reprinting-receipt-documents-in-rere"></a>

Reprinting of a document that is attached to a flow process may be necessary if the original was lost or destroyed or if a duplicate is required. The system only allows you to reprint document types that have been set up in DOCU to allow reprinting.
Use the following procedure when the RERE Print Status field indicates “Printed” and you need to reprint the receipt.
1 Enter RERE 
2 Key in the receipt number and press Enter. The system displays the documents that are attached to this receipt’s current flow process.
3 Check that the print status indicates “Printed.” If there is more than one document listed, use the up and down arrow keys to place the cursor beside the document that you wish to reprint.
Clicking on cancel changes the 
Print Status field to Cancel.
Printing of the receipt invoice document is no longer needed to advance to the next flow in 
CHRF.

RERE screen
4 Click on Requeue. Note that the print status indicates “Requeue(d).” This means that you can now reprint the selected document.
The tally document has been printed.
Requeue is available as the reprinting option.

RERE screen
5 Click on Receipt Number and Exit. 
6 Enter PRRM to reprint the document.

### REPRINTING RECEIVING LABELS IN RELA <a id="reprinting-receiving-labels-in-rela"></a>

You use the program RELA (Reprint Labels) to reprint AccellosOne 3PL’s standard receiving label. RELA is a general purpose reprint program that is more flexible than PRRM or PRRE. It allows you to reprint labels for a specific line of a receipt, to specify the number of copies to be reprinted and to reprint at any flow.
RELA prints one label for each pallet; pallets are defined at the detail line level according to the item’s quantity breakdown profile. For example, if your standard quantity breakdown is 10 cases per pallet and your receipt line quantity is 35 cases, RELA will print four labels — one for each of the three full pallets and one for the partial pallet of five cases.
1 Enter RELA.
2 Key in your document code and press Enter or use your pick list to select it.
3 Key in R for Receipt as your document type.
4 Key in your receipt number and press Enter.
5 Key in your line number and press Enter.
Clicking on 
Requeue changes the print status and the receipt invoice document is set to requeue (reprint).

RELA screen
6 In the Number of Labels field, key in the number of extra labels that you require and press Enter.
7 When the Printer Block appears, key in the code of the printer where these labels are to print and press 
Enter. If you do not know the code, use the dropdown list.
8 Click Ok. The labels will print and the system returns to the Main Menu.

### Confirming a Receipt <a id="confirming-a-receipt"></a>

Once a receipt has been entered successfully, the product appears in LOEN (Look Up Entity Information) as “On Receipt” In order for the product to be made “Available” — that is, ready to be shipped out of the warehouse as part of an order — the receipt must be confirmed 
This is done in the program Time-Stamp and Confirm Receipts (CHRF) where each of the receipt’s flow processes is selected and time-stamped individually. The flow processes were previously set up in DIFP as either mandatory or non-mandatory. Mandatory flows must be selected and time-stamped in CHRF whereas non-mandatory flows are optional and they can be bypassed in CHRF.
ENRE is always the first inbound flow process. The system automatically time-stamps the ENRE flow process when you finish entering the receipt. Then you select each of the receipt’s other flows individually in CHRF. As you do this, AccellosOne 3PL time-stamps the flow to verify completion of the action and then advances to the next flow.
Documents attached to any of the flow processes must also be printed in one of the printing programs before the system allows you to proceed to the next flow. Once all of the flows are processed, AccellosOne 3PL creates a permanent receipt record and the inventory is available for shipping when needed.

The Time-Stamping Block in LORE shows the flows that have been selected, time-stamped and processed to date for a specific receipt.

### TIME-STAMPING AND CONFIRMING RECEIPTS IN CHRF <a id="time-stamping-and-confirming-receipts-in-chrf"></a>

Before you can confirm a receipt in CHRF, the following conditions must be met:
 all documents have been printed for the receipt
 all locations have been entered for each receipt line
1 Enter CHRF.
2 Do one of the following:
CHRF screen showing Query Block
NOTE Advancing the flow of a receipt in CHRF is only required in a manual paperbased environment. In RF receiving, the flow is automatically advanced after each receipt line is stage and/or put-away.
if you know your receipt number: If you wish to perform a query:
a) Key in your receipt number and press Enter.
a) Click on Query Block.
b) Key in your query criteria and click on Execute Query.
c) In the Receipts Queried Block, use your arrow keys to locate the receipt that you wish to confirm.
d) With your cursor positioned over the desired receipt, click on 
Accept Receipt.

AccellosOne 3PL will populate the fields in CHRF with the appropriate values for the receipt that you entered or selected.
3 The cursor moves to the Next Flow Process Code field. Press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select. If there is only one option in the pick list, it is a mandatory flow process. Click on Select.
If there is more than one option in the pick list, the last selection — the one with the highest sequence number — is mandatory. The other options are non-mandatory. You can bypass a non-mandatory process flow by not selecting it in the pick list. Use the up and down arrow keys to move the cursor next to the flow process that you wish to select. Then click on Select.

CHRF screen showing the pick list for the Next Flow Process Code field
4 The Receive Date field is for entering the date when the product arrived at the warehouse. The field may be blank in which case the system bypasses it and does not allow you to enter the field. Proceed to step 
5.
Depending on your setup, the field may display MM.DD.YY or it may display an actual date. If the field displays MM.DD.YY and you do not move the cursor into the field, the field will automatically populate with the default date as you continue. The default is the Current Date in your system setup (usually, today’s date).
If you need a different Receive Date than the default, press F9 and then press Enter until the cursor is in the field. Key in the applicable date and press Enter.
Non-mandatory flow process option
Mandatory flow process option

 CHRF screen
5 Click on Select Flow. The CHRF screen becomes blank. 
If the system does not advance to the next flow, see [Troubleshooting Help for Confirming a Receipt](recebimento.html#troubleshooting-help-for-confirming-a-receipt).
Click on 
Select Flow will confirm the Next Flow 
Process Code and advance the system to the flow process that follows in the sequence. 

6 Continue selecting the next flow and re-entering the receipt number by repeating steps 3 to 5 inclusive until you reach your CORE (Confirm Receipt) flow.
7 If you wish to change the receive date on the receipt, press Enter to position your cursor in the Receive 
Date field. Then key in a new date and press Enter.
8 Click on Select Flow.
9 Do one of the following:

### TROUBLESHOOTING HELP FOR CONFIRMING A RECEIPT <a id="troubleshooting-help-for-confirming-a-receipt"></a>

If you receive any of the following messages in the Help Line, the following actions are required:
There are no more flow sequences for this receipt. 
The receipt has been either confirmed or deleted. Exit CHRF and, if you wish, you may enter LORE to check the receipt’s status. See [Looking Up Receipts in LORE](recebimento.html#looking-up-receipts-in-lore).
There is at least one more document to print for this receipt. 
1 Click on Exit to exit CHRF.
2 Enter into the program PRRM. Print the document(s) for this flow. See [Printing the Receiving Documents](recebimento.html#printing-the-receiving-documents).
3 Once the document(s) is printed, return to CHRF. Key in the receipt Number and press Enter. Click on 
Select Flow and continue the procedure for confirming the receipt in the usual manner.
You cannot select this flow since this receipt does not have all locations entered.
1 Click on Exit to exit CHRF. 
2 Enter ENRE.
3 Click on Enter Criteria.
4 Key in the receipt number and click on Execute Query.
5 Click on Line Block.
6 Press Enter until the cursor is in the Location Code field.
If you wish to confirm the receipt and exit CHRF:
If you wish to cancel the confirmation and exit CHRF 
If you wish to remain in CHRF to work on other receipts:
a) Click on Exit. A message will appear indicating that the receipt is being confirmed.
a) Key in the same receipt number and press Enter.
b) Click on Exit.
a) Key in your next receipt number and press Enter.
b) If required, change the Ship date.
c) Click on Select Flow.
d) Repeat the above three steps for each additional receipt that you wish to confirm.
e) When you finish processing your receipts, click on Confirm. A message will appear indicating that receipt 1 of xxx is being confirmed.

7 Key in the Location Code and press Enter. Click on Exit.
8 Enter CHRF. Key in the receipt number and press Enter. Click on Select Flow and continue the procedure for confirming the receipt in the usual manner.

### CONFIRMING RECEIPTS ONE LINE AT A TIME IN CORL <a id="confirming-receipts-one-line-at-a-time-in-corl"></a>

You use the program Confirm Receipts - One Line at a Time (CORL) in situations when it is necessary to confirm only a specific line(s) of the receipt and not the entire receipt.
The following conditions must be met before you can confirm a receipt line in CORL:
 the line or lines that you wish to confirm must be fully allocated
 the line or lines must be at the flow immediately preceding the flow CORE (Confirm Receipt) unless the flow immediately preceding CORE is defined as non-mandatory in DIFP
 all documents attached to any flow before CORE must be printed.
EXAMPLE
If your inbound flows are ENRE, FLOW1, FLOW2, FLOW3 and CORE and if FLOW3 is defined as mandatory in DIFP, the line or lines must be at FLOW3. If FLOW3 is not mandatory, the line or lines must be at FLOW2.
1 Enter CORL. 
2 Click on Create Record.
3 Key in the receipt number and press Enter.

CORL screen
4 Key in the line number and press Enter twice. “Confirm” displays under the receipt number. 
5 Click on Return to Main.
Confirm appears under the receipt number.
The Receipt 
Date Block displays.

6 Click on Receive Date. The Receive Date is the date when this flow is being confirmed. Press Enter to accept the default date as the date you are confirming this flow. The default is the current date of your system setup (usually today’s date).
If you need a different Receive Date than the default (for example, you are confirming this flow on a different day than when the receipt was entered), key in the applicable date and press Enter. 

CORL screen showing the Receive Date Block
7 To enter another receipt line that needs to be confirmed, click on Master Block. Click on Create Record and repeat steps 3 to 6.
8 When you have finished entering all the lines that need to be confirmed, click on Confirm. A message will display on your screen indicating that the line(s) are being confirmed.

### CHECKING CONFIRMED LINES IN LORE <a id="checking-confirmed-lines-in-lore"></a>

You can check that individual lines entered in CORL have been confirmed. Although individual lines of the receipt have been confirmed, the receipt’s status will not display as confirmed in LORE. The receipt still has remaining lines that have not yet been confirmed. Once all lines are confirmed, then the receipt’s status will show as confirmed.
1 Enter LORE. 
2 Key in the receipt number and click on Execute Query.
To confirm the lines, you must click 
Confirm

LORE screen showing a receipt with line confirmed in CORL
3 Click on Line Block. 
4 Use the up or down arrow keys to scroll to the line that you confirmed in CORL. 
5 If the Receive Date field is completed, you know the line is confirmed. Click on Header Block and Exit to exit the program.
If the Receive Date field is blank, the line was not confirmed. Click on Header Block and Exit to exit 
LORE. Enter CORL and re-enter the line.

### Rating a Receipt in RCRA <a id="rating-a-receipt-in-rcra"></a>

You use the program Receipt Rater (RCRA) to manually rate a receipt. This program calculates all the automatic and optional charges that apply to a receipt. 
If your system has been set up to rate receipts automatically, you skip the procedure below. With automatic rating, the receipt was rated at the same time that it was confirmed. 

### RATING A RECEIPT WITH NO OPTIONAL CHARGES <a id="rating-a-receipt-with-no-optional-charges"></a>

1 Enter RCRA.
2 Key in the receipt number and press Enter.
Receipt status
The Receive 
Date field shows when line 2 was confirmed

3 The cursor will be positioned in the Invoice Date field. The Invoice Date will default to the date when this receipt was confirmed (that is, the date entered in the Received Date field in CHRF). If you are rating this receipt on the same date as it was confirmed, leave the existing date.
If you are rating this receipt on a different date than when it was confirmed, key in the correct date.
4 If applicable, press F9 (Previous Field) to position the cursor in the Reference Number field and key in the reference number.

RCRA screen
5 Click on Rate. The system will display a message indicating that it is rating the receipt.
6 Click on Exit. 

### RATING A RECEIPT WITH OPTIONAL CHARGES <a id="rating-a-receipt-with-optional-charges"></a>

A receipt extra charge will appear on the warehouse receipt invoice if your company produces one. If more than one receipt extra charge is added to one specific receipt, all of the applied extra charges will be stamped with the same receipt number. Receipt extra charges are billed immediately on the warehouse receipt invoice.
NOTE You cannot click on Exit to cancel the rating of the receipt. The Exit command is equivalent to the Rate command.
If there are no other charges to add, click on 
Rate.

An accessorial charge will not appear on the warehouse receipt invoice. These charges will be picked up by the system and applied as part of batch charges in BILB. Accessorial charges will be billed for later, separate from the warehouse receipt invoice.
1 Enter RCRA.
2 Key in the receipt number and press Enter.
3 The cursor is in the Invoice Date field. The Invoice Date will default to the date when this receipt was confirmed (that is, the date entered in the Received Date field in CHRF). If you are rating this receipt on the same date as it was confirmed, leave the existing date.
If you are rating this receipt on a different date than when it was confirmed, key in the correct date.
4 If applicable, press F9 (Previous Field) to position the cursor in the Reference Number field and key in the reference number.
5 Click on Add Extra Charge.

RCRA screen showing Receipt Extra Charge Flag and Accessorial Charge Flag

6 Position your cursor over the appropriate field (Receipt Extra Charge Flag or Receipt Accessorial Flag), key in Y for Yes and press Enter.
If you wish to apply the charge to the receipt header:
If you wish to apply the charge to the receipt line:
a) Click on Extra Charge or 
Accessorial Charge.
b) When the Bill Later - Enter 
Charges Block appears, proceed to enter your accessorial or receipt extra charge(s). You add charges to this screen by following the instructions in the “Entering Receipt Accessorial Charges” section of the 
Billing and Invoicing Guide.
c) When you finish entering your charges, click on Return to 
Main and Exit to exit the Bill 
Later - Enter Charges Block.
a) Click on Receipt Details.
b) Position your cursor over the line to which you wish to apply the receipt extra charge.
c) Key in Y for Yes and press 
Enter.
d) Click on Extra Charge.
e) When the Bill Later - Enter 
Charges Block appears, proceed to enter your accessorial or receipt extra charge(s). You add charges to this screen by following the instructions in the “Entering Receipt Accessorial Charges” section of the 
Billing and Invoicing Guide.
f) When you finish entering your charges, click on Return to 
Main and Exit to exit the Bill 
Later - Enter Charges Block.
g) Repeat steps b to f for each additional line that you wish to apply the receipt extra charge.

RCRA screen
7 If you applied charges to the receipt header in step 6 and now wish to apply charges to the receipt line, repeat step 6 for the receipt line charges. Likewise, if you applied charges to the receipt line and now wish to apply charges to the receipt header, repeat step 6 for the receipt header charges.
8 When you finish entering your receipt extra charges, click on Exit twice to exit.
You can enter the program Bill Later - Enter Charges (ENAC) to verify that the charges have been applied to the receipt.

### REQUEUING A RECEIPT FOR RATING IN RERA <a id="requeuing-a-receipt-for-rating-in-rera"></a>

You use the program Requeue Receipt for Rating (RERA) if you need to remove the charges that were applied to a receipt when it was rated. RERA “un-rates” the receipt — that is, it removes the charges and returns the receipt to a status of “Confirm(ed) Receipt, not rated” in LORE. The last point in the invoicing process at which you can unrate a receipt depends upon your invoicing type:
 if the receipt charges are on an accessorial invoice, you can run RERA at any time before the accessorial batch is confirmed in ACIN
 if the receipt charges are not on an accessorial invoice, you can run RERA at any time before running 
DLRE (Daily Invoice Register) 
You also use RERA to change the Receipt Type designation that was assigned to a receipt that has already been rated and confirmed. For example, you can change the Receipt Type from S (Initial Storage charges only) to H (Inbound Handling charges only). See the section “Overriding Generated Charges on a Receipt” in the Billing and Invoicing Guide for further details on receipt type designation.
To add receipt extra charges to specific receipt lines, set the flag to Y in the 
Receipt Detail 
Block for the applicable lines
Accessorial 
Charge field

The Receipt Type designation can be changed for either the receipt’s Header Block or any of its Line Block records. This function will also remove the charges that were applied to the receipt and return the receipt to a status of “Confirm(ed) Receipt, not rated” in LORE. 
RERA has two blocks: the Detail Block (the Header Block) and the Line Block.
1 Enter RERA. 
2 Key in the receipt number and press Enter.

RERA screen
3 The system completes the other fields and moves the cursor to the Receipt Type field. If it is necessary to change the Header Receipt Type, key in the new code and press Enter. If a change is not necessary to the Header Receipt Type, no further action is required for this field.
NOTE When you change the Receipt Type designation in RERA for either the 
Header or the Line Block, the system un-rates the entire receipt.
This Receipt 
Type field will change the receipt type designation of the receipt’s 
Header Block

4 There are two command options available: Line Block and Rerate.

RERA screen showing the Line Block
5 If you need to rerate another receipt, key in the next Receipt Number and press Enter. Then repeat steps 
3 and 4.
6 When you finish rerating all applicable receipts, click on Exit.
After you perform the above procedure on a rated receipt, the receipt’s status will show in LORE as “Confirm, not rated.” This means that the receipt is confirmed and that the previously applied charges have been removed. It is now possible to rate the receipt again with the correct charges. You do this either manually in 
If you do not need to change the 
Receipt Type designation for any of the receipt’s Line Block records:
If you need to change the Receipt 
Type designation for any of the receipt’s Line Block records:
a) Click on Rerate. 
b) The Help Message Line indicates that the system is working. 
Wait while the system completes its task. 
c) The screen blanks out the fields, which indicates that the entire receipt has been un-rated.
a) Click on Line Block.
b) Use the up and down arrow keys to move the cursor next to the 
Line Block record that you need to change. Check the Current 
Record Counter to ensure that you are changing the correct line record.
c) Key in the new Receipt Type code over the existing one and press Enter.
d) Click on Details. The Help Message Line indicates that the system is working. Wait while the system completes its task. 
e) The screen blanks out the fields. 
This indicates that the entire receipt has been un-rated and that the Line Block Receipt Type change(s) have also been made.
This Receipt 
Type field will change the 
Receipt Type designation of the receipt’s Line 
Block records

RCRA or automatically in CHRF, depending on how rating is done for this customer. (In the latter case, although you will use the CHRF screen, the system will rate first since the receipt has already been confirmed.)

### Receipt Check-In Receiving <a id="receipt-check-in-receiving"></a>

The Receipt Check-In set of programs allows you to check whether the quantity received in RFCH or RFPU of a given receipt matches the quantity expected in ENRE and whether the product has been assigned to a final put-away location or has been left in a staging location.
If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE flow, AccellosOne 3PL will check for variances in CHRF. If the receipt contains a variance, you will be prompted to either accept the variance and confirm the receipt or leave the receipt unconfirmed until the variance can be resolved.

### SETTING UP RECEIPT CHECK-IN PARAMETERS IN CICP <a id="setting-up-receipt-check-in-parameters-in-cicp"></a>

You set up your receipt check-in parameters in CICP (Check-In Configuration Parameters). In this program, you define the following:
 the flow at which you want AccellosOne 3PL to start checking for variances (flows before this flow will not be checked)
 the default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIS (Receipt Check-In at Staging)
 the default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIR (Receipt Check-In Report)
You can define a single set of check-in parameters for all customers by using the .ALL option or you can define different check-in parameters for each of your customers.
FIELD DESCRIPTIONS
Customer Code The customer that the receipt check-in parameters apply to or .ALL for all customers if your parameters apply to all customers.
Flow Process Code The flow at which you wish to start checking for variances.
Balance by Inventory 
Level
The default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIS. For example, suppose you receive 10 cases of item A, lot 1 and 10 cases of item A, lot 2 in ENRE. When you process the receipt in 
RF, you record 15 cases of lot 1 and 5 cases of lot 2.
If you balance by inventory level 2, your receipt will be out of balance. However, if you balance by inventory level 1, your receipt will be considered balanced.

1 Enter CICP.
2 Click on Enter Criteria then Execute Query to see which receipt check-in parameters have been set up. If the receipt check-in parameters that you require have not been set up, click on Create Record.
3 In the Customer Code field, key in your customer code and press Enter. If you do not know the customer code, you can select it from the pick list. To select a code from a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select.
4 In the Flow Process Code field, key in your flow process code and press Enter. If you do not know the code, use the pick list to select it.
5 In the Balance by Inventory Level field, key in the appropriate inventory level and press Enter.
6 In the Report by Inventory Level field, key in the appropriate inventory level and press Enter.
7 Add another record to CICP or click on Return to Main to exit create record mode.
CICP screen showing three records
8 Click on Exit to exit.
Report by Inventory Level The default inventory level that you want AccellosOne 3PL to use for reporting purposes in RCIR. This value need not be the same as your Balance by 
Inventory Level value.
For example, if you report by level 1, RCIR will show a single line for each receipt line. If, on the other hand, you report by level 3, RCIR will show three lines for each receipt line; an item total with variances, a lot total with variances (if level 2 = lot) and a pallet ID total with variances (if level 3 = pallet ID).
NOTE Your Report by Inventory Level value should always be less than the number of inventory levels used by the customer. For example, if you are reporting on a three-level account, you should set this field to 1 or 2. If you set this field to 3, the extra lines generated in RCIR will be redundent.
FIELD DESCRIPTIONS

### SETTING UP YOUR SPECIAL VERIFY PROGRAM IN DIFP <a id="setting-up-your-special-verify-program-in-difp"></a>

If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE flow and set the Complete flag to Y for Yes, AccellosOne 3PL will check for quantity variances in CHRF. Refer to the System Administration Guide for instructions on setting up special verify programs.
DIFP screen showing special verify program RNSL attached to CORE flow with Complete flag set to Y for Yes

### ACTIVATING RECEIPT VARIANCES IN MRFP <a id="activating-receipt-variances-in-mrfp"></a>

Make sure that the RFCH/RFPU Quantity Must Match the ENRE Quantity flag in MRFP is set to either “Match not required” or “Warn if mismatch with ENRE”.

### LOOKING UP VARIANCES AND LOCATION STATUSES IN RCIS <a id="looking-up-variances-and-location-statuses-in-rcis"></a>

You can look up the variance quantity and location status of receipts in RCIS (Receipt Check-In at Staging). 
For each receipt that you query on, RCIS shows the receipt number, customer code, flow code, receipt date, gross weight, net weight, expected quantity, received quantity, quantity variance and location status.
When the quantity received in RF matches the quantity expected in ENRE, the quantity variance will show B for Balanced followed by the inventory level used to calculate variances; for example, “B-L1”. When the quantity received does not match the quantity expected, the quantity variance will show U for Unbalanced followed by the inventory level used to calculate variances; for example, “U-L1”.
There are three possible location statuses for a receipt in RCIS: 
 M for missing locations
 S for staging locations assigned
 P for put-away locations assigned 

If even one receipt line on a receipt has not been assigned, the location status will be set to M for missing. If all receipt lines on a receipt have been assigned and at least one line has been assigned to a staging location, the location status will be set to S for staging locations assigned. If all receipt lines on a receipt have been assigned to a final put-away location, the location status will be set to P for put-away locations assigned.
There are three possible reporting options in RCIS:
 you can run the Receipt Check-In at Staging Summary report
 you can run the Receipt Check-In at Staging Detail report
 when you look up a receipt in RCIS, AccellosOne 3PL automatically generates a Receipt Check-In at 
Staging Detail Report for that receipt and attaches it to the Time-Stamping Block of LORE where you can look it up by clicking on the View icon.
1 Enter RCIS.
RCIS screen showing View Filter
2 Key in your search criteria such as customer code, receipt number range, receipt date range, receipt reference number and probill number.
3 If you wish to override the customer’s balance by inventory level value defined in CICP, key in an override value and press Enter in the Balance by Inventory Level field.
4 If you wish to override the customer’s report by inventory level value defined in CICP, key in an override value and press Enter in the Report by Inventory Level field.
5 If you wish to override the default value in the Display Weight in Lbs / Kilos field, key in L for pounds or K for Kilos and press Enter.
6 When you finish entering your search criteria, click on Execute Query.

RCIS screen showing receipt details and receipt summary
7 If your query retrieves more than a page of records, use your up and down arrow keys to scroll through the list of receipts.
8 If you wish to scroll horizontally to see reference and probill number information, press Enter or tab to see the additional fields. Press Enter or tab again to suppress the display of reference and probill number information.
9 When you finish looking up your variances in RCIS, click on Return and Exit to exit.

### PRINTING THE RECEIPT CHECK-IN AT STAGING SUMMARY REPORT <a id="printing-the-receipt-check-in-at-staging-summary-report"></a>

This report shows the receipt number, receipt date, customer code, reference number (if any), expected quantity, received quantity, variance quantity, variance status (Balanced or Unbalanced), the inventory level at which the variance calculation was made, the location status (Missing, Staging or Put-Away), probill number (if any) and flow process for each receipt reported on.

1 Enter RCIS.
2 Retrieve the receipts that you wish to report on.
3 Click on Receipt Check-In at Staging Summary Report.
4 Select your printer from the Printer Code dropdown list and click Ok.

### PRINTING THE RECEIPT CHECK-IN AT STAGING DETAIL REPORT <a id="printing-the-receipt-check-in-at-staging-detail-report"></a>

In addition to the information shown in the summary version of the report, this report shows the level 1, level 
2, level 2 description, line number, expected quantity, received quantity, pending quantity, gross weight, net weight, location and flow process for each receipt line reported on.
ABC Warehousing, Inc. Date From : Page 1 of 1
Receipt Check-In at Staging (RCIS) Date To : SUMMARY 07-09-09 15:50
------------------------------------------------------------------------------------------------------------------------------------
 Receipt# Rcpt.Date Customer Reference Number Expected Received V.Q. Loc. Probill Number Flow
--------- --------- ---------- ------------------- -------- -------- ---- ---- -------------------- ----
 1425 09-16-08 A 300 220 0 U-L2 S INST
 1430 09-18-08 A 5 5 0 B-L2 S INST
 1444 10-20-08 A 200 200 0 B-L2 P PUCO
 1489 11-28-08 A 100 0 100 U-L2 M INST
 1517 12-16-08 A 100 100 0 B-L2 S INST
 1542 01-30-09 A 100 0 100 U-L2 M STPU
 1562 05-11-09 A 100 100 0 B-L2 S INST
 1565 05-14-09 A 100 100 0 B-L2 S INST
 -------- -------- ------- ------------ ------------
 Report Total : 1005 725 200 1345.35 1278.67
 Gross Weight Net Weight

1 Enter RCIS.
2 Retrieve the receipts that you wish to report on.
3 Click on Receipt Check-In at Staging Detail Report.
4 Select your printer from the Printer Code dropdown list and click Ok.

### LOOKING UP THE RECEIPT CHECK-IN AT STAGING DETAIL REPORT IN LORE <a id="looking-up-the-receipt-check-in-at-staging-detail-report-in-lore"></a>

This report is automatically generated and attached to the Time-Stamping Block of LORE in the following cases:
 you look up a receipt with a variance in RCIS
 you confirm a receipt with a variance in CHRF
1 Enter LORE.
2 Retrieve the receipt whose report you wish to look up.
3 Click on Time Block.
ABC Warehousing, Inc. Date From : Page 1 of 3
Receipt Check-In at Staging (RCIS) Date To : DETAIL 07-09-09 15:53
------------------------------------------------------------------------------------------------------------------------------------
Customer : A Customer A
....................................................................................................................................
 Receipt# Rcpt.Date Customer Reference Number Expected Received V.Q. Loc. Probill Number Flow
--------- --------- ---------- ------------------- -------- -------- ---- ---- -------------------- ----
 1425 09-16-08 A 300 220 U-L2 S INST
Item Lot Number Line Expected Received Pending Gross LBS Net LBS Location Flow
-------------------- ------------------ -------------------- ---- -------- -------- ------- ------------ ------------ -------- ----
A1 106 * 1 200 20 0 37.48 35.27 S100 INST
A1 106 * 4 0 0 0 .00 .00
 -------- -------- ------- ------------ ------------
 Lot Number Total : 200 20 0 37.48 35.27
A1 107 * 2 100 100 0 187.39 176.37 S100 INST
 -------- -------- ------- ------------ ------------
 Lot Number Total : 100 100 0 187.39 176.37
A1 108 * 3 100 100 0 187.39 176.37 S100 INST
 -------- -------- ------- ------------ ------------
 Lot Number Total : 100 100 0 187.39 176.37
 -------- -------- ------- ------------ ------------
 Item Total : 400 220 0 412.26 388.01
 -------- -------- ------- ------------ ------------
 Receipt Total : 300 220 0 412.26 388.01
....................................................................................................................................

Time Stamping Block showing highlighted View icon
4 Click on View to view and, if required, print the document in PDF format.
5 When you finish looking up the document, click on Master Block and Exit to exit.

### CONFIRMING RECEIPTS WITH A VARIANCE IN CHRF <a id="confirming-receipts-with-a-variance-in-chrf"></a>

If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE flow, AccellosOne 3PL will check for variances in CHRF. If the receipt contains a variance, you will be prompted to either accept the variance and confirm the receipt or leave the receipt unconfirmed until the variance can be resolved.
When you confirm a receipt in RCIS, AccellosOne 3PL automatically generates the Receipt Check-In at 
Staging Detail Report for that receipt; this report is attached to the Time-Stamping Block of LORE where you can look it up by clicking on the View icon.
1 Enter CHRF.
2 Key in your receipt number and press Enter.
3 Press Enter to position your cursor in the Receive Date field. Then press Enter to accept the current date as your receive date or key in a new date and press Enter.
4 Click on Select Flow.

CHRF screen showing receipt check-in override options
5 If you wish to override the customer’s balance by inventory level value defined in CICP, key in an override value and press Enter in the Balance by Inventory Level field. If you do not wish to override this value, press Enter to bypass the field.
6 If you wish to override the customer’s report by inventory level value defined in CICP, key in an override value and press Enter in the Report by Inventory Level field. If you do not wish to override this value, press Enter to bypass the field.
7 In the Display Weight in Lbs / Kilos field, key in L for pounds or K for Kilos and press Enter.
CHRF screen showing prompt to accept or reject variance
8 Click on Yes to accept the variance or click on No to leave the receipt unconfirmed.
9 Click on Exit to exit.

INVENTORY MAINTENANCE AND 
ADJUSTMENTS
