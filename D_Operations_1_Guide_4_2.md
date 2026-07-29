# Manual D — Operations 1 Guide (Operações 1: Recebimento e Expedição)

> **ID do Manual:** D  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Fluxo operacional principal: recebimento (ENRE), confirmação (CHRF/CHOF), expedição de pedidos (ENOR), lookups (LORE/LOOR/LOEN), impressão de documentos, relocações (RELO), ajustes (ENAJ), holds, transferências, e processamento de inventory levels.

---

AccellosOne Enterprise 
3PL Operations 1 Guide
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

OPERATIONS 1 GUIDE 4.2 i
TABLE OF CONTENTS
INTRODUCTION ......................................................................... 1
About This Manual........................................................................................................................... 2
AccellosOne 3PL Documentation Set ............................................................................................ 2
THE OPERATIONS FLOW PROCESS ............................................. 5
Understanding the Flow Process ................................................................................................... 6
Flow Process Codes........................................................................................................................ 6
Looking Up Your System’s Flow Process Codes.......................................................................... 7
Flow Process Sequence.................................................................................................................. 7
Looking Up Your System’s Flow Process Sequence.................................................................... 8
Flow Process Summary ................................................................................................................ 10
RECEIVING ..............................................................................13
Overview of Receiving................................................................................................................... 14
Receiving Programs .......................................................................................................... 15
Entering a Regular Type Receipt — P (Post-Receiving)............................................................. 17
Overview............................................................................................................................ 17
Entering Header Information in ENRE............................................................................... 17
Entering Line Information in ENRE.................................................................................... 22
Entering Information in the Optional Blocks of ENRE ....................................................... 31
Understanding Warehouse Restrictions...................................................................................... 35
Preset Warehouse Restrictions .................................................................................................... 35
Operator-Selected Restrictions ......................................................................................... 36
Restricting Multiple Item Lines to a Common Warehouse................................................. 36
Restricting Individual Item Lines to a Specific Warehouse................................................ 38
Warehouse Restriction Summary...................................................................................... 39
Modifying a Receipt ....................................................................................................................... 40
Modifying Header Block Data ............................................................................................ 40
Modifying Line Block Data ................................................................................................. 42
Modifying Location Block Data .......................................................................................... 43
Modifying Optional Blocks Data......................................................................................... 44
Changing the Inventory Level on a Receipt Line............................................................... 46
Deleting a Receipt.......................................................................................................................... 46
Deleting an Entire Receipt................................................................................................. 47
Deleting an Entire Line Block Record................................................................................ 48
Deleting Location Block Data ............................................................................................ 50

ii 4.2 OPERATIONS 1 GUIDE
Receipt Header Types and Receipt Line Types........................................................................... 51
Receipt Line Types............................................................................................................ 51
Confirm-Type Receipts .................................................................................................................. 52
In-Transit Receipts......................................................................................................................... 53
Receiving an In-Transit Receipt When All Inventory Levels are Known............................ 53
Receipts With Unknown Inventory Levels................................................................................... 54
Looking Up Pending Receipts in LOPR............................................................................. 55
Entering the Missing Inventory Levels in an Unknown Receipt......................................... 56
Sequential Entry Receipts............................................................................................................. 57
Procedure .......................................................................................................................... 58
Receipts With System-Generated Inventory Levels ................................................................... 61
Receiving Variable Quantity Breakdown Inventory .................................................................... 63
Checking an Item’s Variable Quantity Breakdown in CVQB ............................................. 65
Automatically Updating an Item’s Variable Quantity Breakdown in URQB........................ 66
Look-Up Programs......................................................................................................................... 67
Viewing All Records........................................................................................................... 67
Viewing a Single Record ................................................................................................... 68
Viewing All Records with Common Selection Criteria ....................................................... 69
Looking Up Telephone Information in LOTE............................................................................... 70
Looking Up Receipts in LORE ...................................................................................................... 71
Receipt Block..................................................................................................................... 73
Time-Stamping Block ........................................................................................................ 75
Line Block .......................................................................................................................... 76
Optional Blocks.................................................................................................................. 77
Looking Up an Item Summary ........................................................................................... 77
Changing the Default Sort Sequence in LORE ................................................................. 77
Printing the Receiving Documents............................................................................................... 78
Printing a Document for Specific Receipts in PRRM......................................................... 78
Printing a Document for All Receipts in PRRE .................................................................. 80
Cancelling or Reprinting Receipt Documents.................................................................... 84
Cancelling Receipt Documents in RERE........................................................................... 85
Reprinting Receipt Documents in RERE ........................................................................... 86
Reprinting Receiving Labels in RELA................................................................................ 88
Confirming a Receipt..................................................................................................................... 89
Time-Stamping and Confirming Receipts in CHRF ........................................................... 90
Troubleshooting Help for Confirming a Receipt................................................................. 93
Confirming Receipts One Line at a Time in CORL............................................................ 94
Checking Confirmed Lines in LORE.................................................................................. 95
Rating a Receipt in RCRA ............................................................................................................. 96
Rating a Receipt with No Optional Charges ...................................................................... 96

OPERATIONS 1 GUIDE 4.2 iii
Rating a Receipt with Optional Charges............................................................................ 97
Requeuing a Receipt for Rating in RERA........................................................................ 100
Receipt Check-In Receiving........................................................................................................ 103
Setting Up Receipt Check-In Parameters in CICP .......................................................... 103
Setting Up Your Special Verify Program in DIFP ............................................................ 105
Activating Receipt Variances in MRFP............................................................................ 105
Looking Up Variances and Location Statuses in RCIS ................................................... 105
Printing the Receipt Check-In at Staging Summary Report ............................................ 107
Printing the Receipt Check-In at Staging Detail Report................................................... 108
Looking Up the Receipt Check-In at Staging Detail Report in LORE .............................. 109
Confirming Receipts With a Variance in CHRF ............................................................... 110
INVENTORY MAINTENANCE AND ADJUSTMENTS ...................... 113
Looking Up Inventory Information in LOEN ...............................................................................114
The Inventory Block and Querying in LOEN.................................................................... 116
Looking Up All Inventory Entities for a Specific Customer .............................................. 117
Looking Up All Inventory Entities for a Specific Item ....................................................... 118
Looking Up a Specific Entity............................................................................................ 119
Looking Up All Entities for a Specific Inventory Level ..................................................... 120
Looking Up All Inventory Level Codes Starting With a Prefix.......................................... 122
Drill Block......................................................................................................................... 122
Location Block ................................................................................................................. 124
History Block.................................................................................................................... 128
History Details Block........................................................................................................ 131
History Remarks Block .................................................................................................... 133
Renewal Block................................................................................................................. 133
Looking Up Inventory by Alternate Type Code and Alternate Item Code........................ 135
Looking Up Locations in LOLO .................................................................................................. 136
Location Block ................................................................................................................. 138
Inventory Block ................................................................................................................ 138
Entering Adjustments to Inventory Amounts............................................................................ 140
Querying in ENAJ ............................................................................................................ 140
Entering a Positive Adjustment in ENAJ.......................................................................... 142
Entering a Negative Adjustment in ENAJ ........................................................................ 146
Changing the Product’s Received Date........................................................................... 149
Entering a Transfer Adjustment in ENAJ......................................................................... 149
Creating New Inventory in ENAJ ..................................................................................... 153
Performing Massive Adjustments in MATR............................................................................... 154
Transferring Inventory — Process One Option ............................................................... 155
Transferring Inventory — Process All Option .................................................................. 157
Relocating Inventory ................................................................................................................... 159

iv 4.2 OPERATIONS 1 GUIDE
Relocating Inventory Not on Hold.................................................................................... 160
Relocating Inventory on Hold .......................................................................................... 162
Relocating Inventory on Item Hold .................................................................................. 163
Relocating Product on Location Hold .............................................................................. 164
Performing a Massive Relocation of Inventory in MARL ......................................................... 165
Entering Hold Adjustments......................................................................................................... 169
Placing Inventory on Hold in HOAD ................................................................................ 170
Removing Inventory from Hold in HOAD......................................................................... 173
Looking Up the Off Hold Date in LOEN ........................................................................... 175
Removing Auto Take-Off Holds in HATO ........................................................................ 176
Adjusting Only the Hold Code in HOAD .......................................................................... 177
Putting Inventory on a Massive Hold in POHO................................................................ 177
Removing Inventory from a Massive Hold in MAHO ....................................................... 181
Performing a Mass Transfer of Product on Hold in MOHO ............................................. 184
Adjusting Inventory Details......................................................................................................... 186
Adjusting the Expiry Date in CHEI................................................................................... 187
Adjusting the Descriptions for Inventory Level 2 and Higher in CHEI.............................. 188
Adjusting Weight Details.................................................................................................. 189
Clearing Weights in CLWE .............................................................................................. 196
Reversing a Document’s Flow in RVDF ..................................................................................... 197
SHIPPING .............................................................................. 199
Overview of Shipping .................................................................................................................. 200
Shipping Programs .......................................................................................................... 201
Shipping Operations Process .......................................................................................... 202
Entering a Regular (R-Type) Order............................................................................................. 203
Overview.......................................................................................................................... 203
Entering Header Information in ENOR ............................................................................ 203
Entering Line Information in ENOR ................................................................................. 210
Entering an R-Type Line.................................................................................................. 212
Entering a P-Type Line.................................................................................................... 218
Querying on Inventory Levels in ENOR........................................................................... 218
Assigning Multiple Locations to a Line Block Record ...................................................... 221
Optional Blocks of ENOR ................................................................................................ 224
Entering a Manual Order in MAOE ............................................................................................. 228
Modifying an Order ...................................................................................................................... 229
Modifying Header Block Data .......................................................................................... 229
Modifying Line Block Data ............................................................................................... 230
Modifying Location Block Data ........................................................................................ 232
Modifying Optional Blocks Data....................................................................................... 233

OPERATIONS 1 GUIDE 4.2 v
Updating the Carrier Details in UOCP ............................................................................. 234
Deleting an Order......................................................................................................................... 236
Deleting an Entire Order.................................................................................................. 237
Deleting an Entire Line Block Record.............................................................................. 238
Deleting Location Block Data .......................................................................................... 240
Order Header Types and Order Line Types ............................................................................... 241
Order Line Types............................................................................................................. 241
Looking Up Orders in LOOR....................................................................................................... 242
Order Block...................................................................................................................... 244
Time-Stamping Block ...................................................................................................... 247
Line Block ........................................................................................................................ 248
Optional Blocks................................................................................................................ 249
Looking Up an Item Summary ......................................................................................... 249
Changing the Default Sort Sequence in LOOR ............................................................... 249
Printing the Shipping Documents .............................................................................................. 250
Printing a Document for Specific Orders in PROM.......................................................... 250
Printing a Document for All Orders in PROR................................................................... 253
Printing a Document for a Specific Order Number .......................................................... 256
Confirming an Order.................................................................................................................... 257
Time-Stamping and Confirming Orders in CHOF............................................................ 257
Troubleshooting Help for Confirming an Order................................................................ 260
Confirming Orders One Line at a Time in COOL............................................................. 261
Checking Confirmed Lines in LOOR ............................................................................... 263
Changing the Confirmation Date in CHCD ...................................................................... 264
Generating the VICS Bill of Lading............................................................................................. 266
Creating a New Bill of Lading .......................................................................................... 266
Looking Up a Bill of Lading.............................................................................................. 270
Printing a Bill of Lading.................................................................................................... 272
Modifying the Orders on a Bill of Lading.......................................................................... 273
Confirming a Bill of Lading............................................................................................... 274
Deleting a Bill of Lading................................................................................................... 275
Confirming All Orders on a Bill of Lading in CHOF.......................................................... 275
Cancelling or Reprinting Order Documents .............................................................................. 276
Cancelling Order Documents in REOR ........................................................................... 277
Reprinting Order Documents in REOR............................................................................ 278
Requeuing a Range of Order Documents in RERO ........................................................ 280
Reprinting Shipping Labels in RELA ............................................................................... 281
Inspection Orders ........................................................................................................................ 282
Distribution Orders ...................................................................................................................... 284
Setting Up Distribution Orders......................................................................................... 285

vi 4.2 OPERATIONS 1 GUIDE
Entering a Distribution Order in ENOR............................................................................ 286
Confirming a Distribution Order ....................................................................................... 287
Looking Up a Distribution Order ...................................................................................... 288
Transfer Orders ............................................................................................................................ 290
Setting Up Transfer Orders ............................................................................................. 291
Entering a Transfer Order................................................................................................ 295
Confirming a Transfer Order............................................................................................ 297
Looking Up a Transfer Order........................................................................................... 298
Clearing a Transfer Order in CHAT ................................................................................. 299
Entering Freight Type or Non-Inventory Orders ....................................................................... 300
Picking to Clean ........................................................................................................................... 302
Broker Orders............................................................................................................................... 303
Setting Up a Broker Customer......................................................................................... 303
Shipping a Broker Order.................................................................................................. 305
Processing Proof of Delivery in POD......................................................................................... 306
Entering Proof of Delivery for an Order Delivered in Full................................................. 307
Entering Proof of Delivery for an Order Not Delivered in Full.......................................... 309
Looking Up a Proof of Delivery Transaction in LOOR ..................................................... 313
Looking Up a Proof of Delivery Transfer Receipt in LORE.............................................. 315
Looking Up a Proof of Delivery Record in LOEN............................................................. 317
INDEX ................................................................................... 321

OPERATIONS 1 GUIDE 4.2 1
INTRODUCTION
About This Manual .............................................................................................. 2
AccellosOne 3PL Documentation Set ............................................................... 2

INTRODUCTION
About This Manual
About This Manual
The Operations 1 Guide will assist you in applying the programs that are used most frequently during 
warehouse operations. This guide is designed for beginner and intermediate users of the AccellosOne 3PL 
operations programs. It is divided into four parts. 
Part I, The Operations Flow Process, describes the sequential process that the system uses to direct both 
the receiving and the shipping operations. 
Part II, Receiving, describes the AccellosOne 3PL programs that apply to the receiving process. It provides 
detailed procedures for entering, modifying and deleting data into these programs. This section also explains 
the specific look-up programs that will allow you to view data entered during the receiving process.
Part III, Inventory Maintenance, describes the AccellosOne 3PL programs that maintain accurate inventory 
records while the product is stored in the warehouse. It provides detailed procedures for adjusting inventory 
records, relocating inventory, and placing or removing inventory from holds. This section also explains the 
specific look-up programs that will allow you to view inventory-related data.
Part IV, Shipping, describes the AccellosOne 3PL programs that apply to the shipping process. It provides 
detailed procedures for entering, modifying and deleting data into these programs. This section also explains 
the specific look-up programs that will allow you to view data entered during the shipping process.
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
Guide to ActiveDesktop/A13PLlogging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your 
company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide
core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating 
product, entering hold adjustments

INTRODUCTION
AccellosOne 3PL Documentation Set
OPERATIONS 1 GUIDE 4.2 3
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

OPERATIONS 1 GUIDE 4.2 5
THE OPERATIONS FLOW PROCESS
Understanding the Flow Process ...................................................................... 6
Flow Process Codes ........................................................................................... 6
Looking Up Your System’s Flow Process Codes ............................................ 7
Flow Process Sequence ..................................................................................... 7
Looking Up Your System’s Flow Process Sequence ...................................... 8
Flow Process Summary.................................................................................... 10

THE OPERATIONS FLOW PROCESS
Understanding the Flow Process
Understanding the Flow Process
The two main functions of AccellosOne 3PL Operations are receiving inventory into the warehouse and 
shipping inventory out of the warehouse to fill orders. A flow process setup is used in AccellosOne 3PL to 
direct both of these procedures.
The flow process is the series of steps (flows) that the system requires you to perform when receiving and 
shipping product through AccellosOne 3PL. The code names for the steps were set up previously in the 
program Flow Process (FLPR). 
The sequence of the steps was defined in the program Depositor Workflow Profile (DIFP). The system 
controls the order of the steps and does not allow you to go out of sequence (although print jobs may be 
cancelled if necessary and flow processes that have been set up as Not Mandatory in DIFP can be bypassed 
in either CHRF or CHOF).
As the operator advances each flow, the system attaches the operator’s code and the current system time to 
the flow. This process is called time-stamping. Time-stamping is useful whenever a follow-up is needed since 
questions can be directed to the operator who made the entry. (Therefore, be sure to log in with your own 
operator code and do not allow anyone else to use it.)
Various documents such as tallies or pick sheets usually need to be printed as part of the receiving or 
shipping operation process. (However, a warehouse with a Radio Frequency environment may not need to 
print any documents.) In the program DIFP, each document type is attached to a particular flow process. 
Document types and flow processes are attached in DIFP to match the real workflow of performing actual 
warehouse tasks.
Flow Process Codes
All flow steps that are part of receiving are inbound processes. All flow steps that are part of shipping are 
outbound processes. 
There are two mandatory inbound processes: 
 ENRE (Enter Receipt)
 CORE (Confirm Receipt) 
 There are two mandatory outbound processes: 
 ENOR (Enter Order) 
 COOR (Confirm Order) 
AccellosOne 3PL has other pre-loaded optional inbound and outbound codes. The pre-loaded flow process 
codes are:
 CITR (Change In-Transit to Regular)
 EDI (Message Received by TradeLink)
In addition, your system setup may have additional codes for other flow processes that your company wishes 
to track. 

THE OPERATIONS FLOW PROCESS
Looking Up Your System’s Flow Process Codes
OPERATIONS 1 GUIDE 4.2 7
Looking Up Your System’s Flow Process Codes
If you have authorization to access the program Flow Process (FLPR), you may familiarize yourself with the 
flow process codes that are set up in your system. The following procedure allows you to check existing 
codes so you will recognize them as they display when processing a receipt or an order.
1 Enter FLPR.

FLPR screen showing the flow process codes used for shipping and receiving
2 Click on Enter Criteria and Execute Query to display the list of existing flow process codes. Use your 
arrow keys to scroll through the list. Be sure to scroll through to the end of the list as they may not all 
appear on the screen at one time if the list is long.
3 Click on Exit to exit the program.
For a full explanation of the program FLPR, refer to the Setup Guide. 
Flow Process Sequence
Flow codes and their related documents are each assigned a number to indicate their sequence in the flow. 
Sequence numbers usually are in multiples of five or ten (10, 15, 20, 25, 30, etc.) so that new flows can be 
added between existing ones if the need arises.
Regardless of how many codes there are, Enter Receipt (ENRE) and Confirm Receipt (CORE) are always 
sequence 1 and 90 respectively in the inbound flow sequence and Enter Order (ENOR) and Confirm Order 
(COOR) are always sequence 1 and 90 respectively in the outbound flow sequence. An example of a flow 
process in DIFP could be:

THE OPERATIONS FLOW PROCESS
Looking Up Your System’s Flow Process Sequence
INBOUND
 ENRE ENTER THE RECEIPT (with printing of the receiving tally document attached to this step)
 CORE CONFIRM THE RECEIPT (with printing of the warehouse receipt document attached to this 
step)
OUTBOUND
 ENOR ENTER THE ORDER (with printing of the pick document attached to this step)
 COOR CONFIRM THE ORDER (with printing of the bill of lading document attached to this step)
Looking Up Your System’s Flow Process Sequence
If you have authorization to access the program Depositor Workflow Profile (DIFP), you may familiarize 
yourself with the sequence of the flow process steps that are set up in your system. The following procedure 
allows you to check the existing workflow profiles so you will recognize them as they display when processing 
a receipt or an order.
The DIFP program screen consists of:
 the Header Block
 the In/Out Block 
 the Flow Block
 the Document Block
 the Special Verification Block
1 Enter DIFP.
2 Click on Enter Criteria then Execute Query to display the existing workflow profiles. 
Note that the bottom left-hand corner of the header box has a current record counter, e.g., 1 of 10. The 
first digit is the actual number of the record currently displayed on the screen and the second digit indicates how many records there are in total in the program. 1 of 10 means you are viewing the first of ten 
records.

THE OPERATIONS FLOW PROCESS
Looking Up Your System’s Flow Process Sequence
OPERATIONS 1 GUIDE 4.2 9

DIFP screen showing DIFP program blocks
3 With your cursor in the Header Block, use the up and down arrow keys to move from one DIFP record to 
another. Find a record that applies to a customer whose receipts you will be entering. 
4 Click on In/Out/Repi/Relo Block. Use your up and down arrow keys to toggle back and forth between 
Inbound and Outbound. 
When the In/Out/Repi/Relo Block is set at Inbound, the Flow Block below displays the inbound flow 
steps.
When the In/Out/Repi/Relo Block is set at Outbound, the Flow Block below displays the outbound flow 
steps.
5 Set the cursor on Inbound.
6 Click on Flow Block. The cursor is positioned on the first Sequence Flow Number field. Note the Document Block below, which now displays the documents (if any) that are attached to the first flow process. 
Check the current record counter at the bottom left-hand side of the screen. Only four documents display 
on the screen at a time. If there are more than four, click on Document Block. Use the down pointer key 
to move through to the last document. Once you have viewed all documents listed, click on Flow Block.
7 Use the up and down arrow keys to position your cursor on the second Sequence Flow Number field. 
Note the Document Block below, which now lists the documents (if any) that are attached to the second 
flow process. 
Check the current record counter at the bottom left-hand side of the screen. If there are more than four, 
click on Document Block. Use the down pointer key to move through to the last document. 
Place cursor 
here to toggle 
between 
inbound and 
outbound flow 
processes
Header 
Block

THE OPERATIONS FLOW PROCESS
Flow Process Summary

DIFP screen showing all DIFP program blocks
8 If there are more flow processes, position the cursor on the next Sequence Flow field number to view the 
attached documents in the Document Block. Repeat until you have viewed all flows and attached documents.
9 Click on Special Verification Block to check whether any customized functions have been set up for this 
Depositor Workflow Profile. Use the down pointer key to move through to the last function listed.
10 Click on Master Block and In/Out/Repi/Relo Block. 
11 Set the cursor on Outbound.
12 Repeat steps 6 to 10 to view the outbound DIFP details.
13 Click on Document Block, Flow Block and then In/Out/Repi/Relo Block. Then click on Master Block and 
Exit to exit the program.
For a full explanation of DIFP, refer to the Setup Guide. 
Flow Process Summary
FLPR and DIFP direct both the receiving and shipping processes.
When the cursor 
is on a sequence 
flow process 
code, the 
attached documents for that 
flow show in the 
Document Block

THE OPERATIONS FLOW PROCESS
Flow Process Summary
OPERATIONS 1 GUIDE 4.2 11
This program holds all of the system’s flow process codes. These codes are used to time-stamp and to track 
the steps that you follow during receiving and shipping. 
This program directs the receiving and shipping operations. DIFP does the following:
 sets the specific flow process codes and the flow process sequence that you must follow to receive a 
customer’s (depositor’s) shipment or to ship out an order 
 attaches receiving and shipping documents to corresponding flow process codes
 if your company uses directed put-away and directed picking, DIFP directs the system to perform allocation after a specific flow process 
FLPR
Flow Process
DIFP
Depositor Workflow Profile
Receiving Process Shipping Process

THE OPERATIONS FLOW PROCESS
Flow Process Summary

OPERATIONS 1 GUIDE 4.2 13
RECEIVING
Overview of Receiving...................................................................................... 14
Entering a Regular Type Receipt — P (Post-Receiving)................................ 17
Understanding Warehouse Restrictions......................................................... 35
Preset Warehouse Restrictions ....................................................................... 35
Modifying a Receipt .......................................................................................... 40
Deleting a Receipt ............................................................................................. 46
Receipt Header Types and Receipt Line Types ............................................. 51
Confirm-Type Receipts..................................................................................... 52
In-Transit Receipts............................................................................................ 53
Receipts With Unknown Inventory Levels...................................................... 54
Sequential Entry Receipts................................................................................ 57
Receipts With System-Generated Inventory Levels ...................................... 61
Receiving Variable Quantity Breakdown Inventory ....................................... 63
Look-Up Programs............................................................................................ 67
Looking Up Telephone Information in LOTE.................................................. 70
Looking Up Receipts in LORE ......................................................................... 71
Printing the Receiving Documents.................................................................. 78
Confirming a Receipt ........................................................................................ 89
Rating a Receipt in RCRA ................................................................................ 96
Receipt Check-In Receiving ........................................................................... 103

RECEIVING
Overview of Receiving
Overview of Receiving
The following is a simplified model of the receiving tasks that are performed each time that a customer sends 
product to the warehouse.
PUT-AWAY
THE INVENTORY
ALLOCATE
Select and assign the locations where the 
product will be put away for storage.
RECEIVE THE PRODUCT 
FROM THE CUSTOMER
CREATE PUT-AWAY 
 INSTRUCTIONS AND OTHER 
RECEIVING DOCUMENTS 
RECORD THE 
PRODUCT DETAILS 

RECEIVING
Overview of Receiving
OPERATIONS 1 GUIDE 4.2 15
RECEIVING PROGRAMS
In AccellosOne 3PL, several programs are involved in the process of receiving inventory into the warehouse. 
You record details for each different item that the customer sent. You record 
where each item will be stored in the warehouse (manual allocation) or you 
allow the system to perform automatic allocation later.
After each flow, you print any receiving document that is attached to that particular flow. Not 
all flows will have a document attached to them.
You use PRRM to print a document that is attached to the flow of a specific Receipt Number.
You use PRRE to print the same document (for example, a tally sheet) that is attached to a 
specific flow for all receipt numbers in the system that are at this same stage in their flow process.
If necessary, you cancel the need to print a document that is attached to a receiving flow. 
This will allow you to enter CHRF and advance the system to the next flow process without 
actually printing the document.
If the document for the current flow process has been printed before, you can make the system reprint an attached receiving document.
You time-stamp and advance each flow process.
You Execute Confirm. This will update inventory data and will rate the receipt if your system 
is set up to rate receipts automatically.
You time-stamp and advance each flow process for individual receipt (Line Block) lines.
You Execute Confirm for individual receipt lines, which will update inventory data accordingly 
and will also rate the line if your system is set up to rate receipts automatically.
ENRE
Enter Receipt
PRRM
Print Receiving Documents - Specific
PRRE
Print Receiving Documents - All
RERE
Requeue Receipt Documents
CHRF
Time-Stamp and Confirm Receipts
CORL
Confirm Receipts - One 
Line at a Time

RECEIVING
Overview of Receiving
RECEIVING OPERATIONS PROCESS
You return to CHRF or CORL and PRRM or PRRE as many times as necessary until all flow processes and 
all attached receiving documents are processed.
ENRE
PRRM or PRRE
CHRF or CORL
PRRM or PRRE
PRRM or PRRE
CHRF or CORL
Flow Process 2
Flow Process 1
Need to print
receiving
document?
Need to print
receiving
document?
Need to print
receiving
document?
Flow Process 3
No Yes
No Yes
No Yes
CHRF or CORL
Execute Confirm

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 17
Entering a Regular Type Receipt — P (Post-Receiving)
To begin the receiving process in AccellosOne 3PL, you enter a receipt in the program ENRE (Enter Receipt). 
You enter a separate receipt for each customer whose product arrives at the warehouse. 
OVERVIEW
The program ENRE records many details about the incoming product. The system uses these details later to 
automatically update inventory records and to bill the owners of the product for inbound handling charges and 
initial storage charges. ENRE also allows for the manual entry of any extra and accessorial charge details 
that may apply. 
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
A physical receipt has general information that applies to the whole shipment and specific information about 
the individual items that make up the shipment. To capture this in AccellosOne 3PL, ENRE has a Header 
Block and a Line Block. General information that applies to the whole transaction is entered in the Header 
Block. Particular information about each item is entered separately in the Line Block.
P (Post-receiving) is the normal ENRE receipt type. Rating of P (Post-receiving) receipts automatically 
generates inbound handling and initial storing charges according to the profiles that were set up in AccellosOne 3PL for your warehouse company.
The following procedure will lead you through the ENRE program, field by field. Information for completing the 
fields is obtained from the receiving documents that accompany or precede the goods or the fields fill in 
automatically (populate) with data that was preset in other AccellosOne 3PL programs.
Some fields are mandatory. The system will not allow you to continue until you complete a mandatory field. 
Other fields are optional and the system allows you to bypass them by pressing Enter without adding any 
information.
Some fields have pick lists that display the available options for that field. This is helpful when you do not 
remember the code that you need. 
ENTERING HEADER INFORMATION IN ENRE
The Header Block is also called the Master Block. Data in the Header Block will apply to all line records that 
you will create later in the Line Block.
1 Key in ENRE at the Enter Selection Prompt. Press Enter and the system displays the Enter Receipts 
(Inbounds) screen. The program is in the Create Record mode.
2 Leave the Receipt Number field blank. The system will automatically generate a number later.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
3 In the Customer Code field, key in the code of the product owner and press Enter. 
If you do not know your customer code, you can select it from the pick list. To select a code using a pick 
list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use 
your arrow keys to position your cursor over the appropriate code and click on Select.
4 The system automatically fills in the next seven customer-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 

 ENRE screen showing a P (Post-Receiving) type receipt
5 If required, enter the Shipper Code of the party that is sending the product to the warehouse and press 
Enter. If you do not know the code, use the pick list. If manual shippers are activated on your system, you 
can key in a forward slash (/) followed by the name and address of the shipper.
6 The system automatically fills in the next seven shipper-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 
7 The system automatically bypasses the Priority field, either filling it in or leaving it blank. This field is only 
functional when using the auto-print feature of AccellosOne 3PL and it refers to the priority in the printing 
queue. The priority range is from one to nine with one being the highest priority and nine being the lowest. The system default is 5. 
NOTE If the shipper is always the same as the customer (that is, the customer 
ships from its own facility), your system may have a profile set up in Shipper (SHIP) 
that uses S (for Same) as the Shipper Code. In this case, you can key in S in place of 
the Shipper Code and press Enter.
Receipt Type field

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 19
If you need to change the default value, press F9 (Previous Field) and then press Enter until the cursor is 
in the priority Field. Key in the correct number and press Enter.
The screen scrolls up. The system automatically fills in and skips over the (Priority) Description field.

ENRE screen after the screen scrolls upward for the first time
8 The Bill To Code field refers to the party that will be billed for the receiving charges. The system populates this field with the Customer Code. If the party to be billed for the receiving charges is not the Customer Code, key in the correct code and press Enter. If you do not know the code, use the pick list. 
9 The system automatically fills in the next seven Bill To Code related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 
10 Press Enter to accept the default date as the expected Receipt Date. If a different expected Receipt Date 
is required, key in the correct date using the same date format as shown in the field and press Enter. 
You can enter a Receipt Date that differs from the current system date by up to one month in the past or 
in the future.
11 Press Enter to accept the default time as the Receipt Time. If a different Receipt Time is required, key in 
the correct time using the same format as shown in the field and press Enter.
12 Key in the carrier’s probill reference number if the customer requires it and press Enter. Otherwise, press 
Enter to bypass the field. 
13 Key in any customer-defined Reference Number that applies to this receipt and press Enter. Otherwise, 
press Enter to bypass the field. The screen scrolls up.
14 Enter the Carrier Code of the firm that transported the product to the warehouse and press Enter. If not 
known, use the pick list. If manual carriers are activated on your system, you can key in \ followed by the 
name and address of the carrier.
Note that the pick list has an “unassigned” option if the carrier is not known at this point in time.
The system populates the Customer 
Code and Bill To 
Code fields with the 
same data. Change 
the bill-to code if necessary.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
15 Enter the Load Type Code and press Enter. If you do not know the code, use the pick list 
The system automatically fills in the Description field of the Load Type Code.
16 The Warehouse Code field is usually left blank. Press Enter to bypass the field.
For further information on this field, refer to the section, “Restricting Multiple Item Lines to a Common 
Warehouse” on page 36. 

ENRE screen after the screen scrolls upward for the second time
17 In the Total Units field, key in the number of units that arrived at the warehouse for the entire receipt and 
press Enter. Do this by adding together the units of each line on the receipt. 
You count the units of each line by using the line item’s lowest SKU level according to its item quantity 
breakdown. For example, count by cases for the line 1 item if its quantity breakdown is pallets/cases and 
count by feet for the line 2 item if its quantity break-down is yards/feet. Then add the units together for 
both lines: 10 cases plus 10 feet equal 20 units.
18 The default for the Remarks field is N (for No). If you do not need header remarks to appear on the warehouse receipt, press Enter to accept the default. If you do, key in Y (for Yes) and press Enter. A block will 
appear later in the program to enter the remarks.
19 In the Carrier Details field, key in the appropriate value.
N (No) Use when you do not need to track carrier details. 
E (Entry) Use to enter the carrier details during receipt entry. The Carrier 
Details Block will display later in ENRE for you to complete. The 
details will print on the attached inbound document that has been 
pre-selected by your company.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 21
20 Press Enter to bypass the Pallet Details field.
21 Press Enter twice to bypass the Accessorial Charges and Receipt Extra Charges fields.
22 Press Enter again to bypass the Material Handling Equipment Type Code field.
23 In the Extra Reference Number 1 and the Extra Reference Number 2 fields, enter the data defined by the 
customer and press Enter. 
If the customer does not require such reference data, press Enter to bypass each of the fields.

ENRE screen after the screen scrolls upward for the third time
24 Press Enter to bypass the Distribution Type Code field.
25 If you changed the default in any of the fields for Remarks, Accessorial Charges and Receipt Extra 
Charges, the corresponding blocks will display now on the screen in succession. 
Complete the applicable blocks by following the corresponding Optional Blocks procedures, which follow 
the Line Block procedure. Then return to the Line Block procedure, listed directly below, and complete it. 
If none of these optional blocks apply, proceed to the mandatory Line Block procedure directly below. 
C (Confirmation) Use to add carrier details during confirmation of this receipt. The 
Carrier Details Block will display during confirmation and the 
details will print on the attached inbound document that has been 
pre-selected by your company.
B (Both) Use to add carrier details twice — once during ENRE and again 
during confirmation. The details will print on the attached inbound 
document that has been pre-selected by your company.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
ENTERING LINE INFORMATION IN ENRE 
In AccellosOne 3PL, the term item means an entity made up of its inventory levels as defined in DILP 
(Depositor Inventory Level Profile). Inventory Level 1 is always the item itself and any other levels are further 
descriptions or variations of the item’s attributes. 
For example, if you are receiving Item: A, Lot Number: 1, Color: Grey as well as Item: A, Lot Number: 1, 
Color: Blue, you must enter two separate Line Block records. Each Line Block record has a line number 
assigned to it and each record contains specific details about an individual item at its time of arrival at the 
warehouse.
Warehouse charges can vary for each item. Therefore, there are different Line Block types to regulate the 
warehouse charges applied to each item. The following procedure is for a regular P (Post-receiving) Line 
Block type.
1 The system enters the Line Block in the Create Record mode. Leave the Line field with the 1 that is generated by the system.

ENRE Line Block screen ready to accept the details of the first inbound item
2 Leave the Type field with the P (Post-receiving) that is generated by the system. 
3 In the Remark field, if you need remarks to appear on the warehouse receipt for this line item, key in Y
(Yes) and press Enter. 
Otherwise, press Enter to accept the N (No) default.
4 In the Charge field, you can add charges for this line item (other than the automatic Inbound handling 
and Initial Storing charges). If you wish to add charges, key in Y and press Enter. An Accessorial Block 
screen will display later for entering the charge details.
If there are no additional charges, press Enter to accept N (No). 

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 23
5 The system may skip over the Warehouse Restriction field leaving it blank. This means that the field does 
not apply to this line and the system does not allow you access.
However, the cursor may enter the field and the Help Message Line indicates “Enter a warehouse restriction if required.” If storage of this item is to be restricted to a particular warehouse, key in the Warehouse 
Code and press Enter. If you do not know the code, use the pick list. If a restriction is not required, press 
Enter to bypass the field.
6 Key in the Item Code and press Enter. If you do not know the code, use the pick list. 
Note that Item Code is always Inventory Level 1.

ENRE Line Block screen
7 Under the Item Code field, there can be — depending on the customer’s setup — Inventory Level 2, 
Inventory Level 3 and Inventory Level 4. However, these fields will display with the correct terminology 
(for example, Lot Number, Production Date, Expiry Date, Pallet ID, etc.) that was preset for this customer. 
If this item has an Inventory Level 2, enter the information for this level and press Enter. Repeat for the 
other inventory levels, if applicable.
Inventory 
levels

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)

ENRE Line Block screen
8 Your setup may have a Description Entry field to the right of one or more of the fields for Inventory Level 
2 and higher levels. If this is the case, the cursor moves here prompting you to enter the specific data for 
this level as requested by the customer (for instance, an actual serial number or actual production date, 
etc.). The specific data is available in the receiving documents. 
Key in the required information and press Enter for each of the Description Entry fields attached to the 
inventory levels. 
The system may populate these fields. Check that the system-entered data matches the warehouse 
receiving documents. If it does, press Enter to accept. If it does not, press F11 (Clear Field), key in the 
correct data and press Enter.
9 In the Quantity Breakdown field, AccellosOne 3PL shows the SKU’s used to track and bill this item. For 
example, if the Quantity Breakdown field shows PLT: 50 (the largest SKU) and CASE: 1 (smallest SKU), 
you read it as one pallet has 50 cases.
10 In the Expected Quantity field, key in the item amount as declared on the receiving documents and press 
Enter. 
You can key in the amount in any SKU that is valid for receipt entry. The SKU’s that are valid for receipt 
entry are defined in IQBP (Item Quantity Breakdown Profile). For example, if the item’s quantity breakdown is 100 cases per pallet, you can enter an amount of 1,010 cases as follows:
1010 CASES or 10PLT 10 CASES or 9PLT 110 CASES
Embedded spaces are allowed but not required. The total number of characters including blank spaces 
cannot exceed 20 characters.
11 The system automatically fills in the Received Quantity field with the same amount as the Expected 
Quantity Field. If the amount received into the warehouse is the same as the amount declared on the 
Description 
Entry field 
for an 
inventory 
level

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 25
receiving documents, press Enter to accept the data. If it is not, key in the actual amount received and 
press Enter.
12 The system skips over the Expiry Date field. If this is an Expiry Date Item and you need to enter an expiry 
date or correct the system-entered date, press F9 (Previous Field). Key in the expiry date and press 
Enter.
13 If the item has a temperature requirement that needs to be tracked, key in the degrees in this field. If it 
does not, the system skips over the field.

ENRE Line Block screen with item details
14 The system automatically calculates and fills in the item’s Weight Code, Unit Weight, Total Gross Weight, 
Total Net Weight Linear Code, Length, Width and Height if the item was set up as a Standard Weight 
item.
If you need to change the data in any of these fields, press F9 (Previous Field) the required number of 
times until the cursor is in the field.
If the item has non-standard weights, key in the applicable weight data in each respective field and press 
Enter.
15 The Location Code field determines the put-away location for this item. If you wish to use automatic putaway, that is, you want the system to choose the location, press Enter to bypass the Location Code field. 
Later in the receiving process, during printing of the attached inbound document that was pre-assigned 
to trigger allocation, the system will select and assign the location.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
If you wish to make a manual put-away entry, that is, you wish to select the put-away location, do one of 
the following.
16 If your warehouse has automatic put-away, press Enter to bypass the Warehouse Code field. The active 
locator will choose the warehouse in which to store this item. 
If your warehouse uses manual put-away, the system fills in the Warehouse Code field based on the 
location code entered in the previous field or a pre-set warehouse restriction. Press Enter to accept it.
17 If you entered a location, choose the applicable option for the Hold Code field:
If the item does not need to be placed on hold, press Enter to leave this field blank. 
If the item needs to be placed on hold, key in the code and press Enter. If the code is not known, use the 
pick list. 
If the field is populated, this indicates that either this item or the location where the product will be stored 
has an automatic hold attached to it. Press Enter to accept the current code or use the pick list to select 
a new code. 
18 The Remark and Accessorial blocks for this line will now appear on the screen for completion if you 
requested them in the Line Block. If none of these blocks apply, proceed to the next step.
If you need to complete the Remarks Block and/or Accessorial Block, see the corresponding procedures 
in “Entering Information in the Optional Blocks of ENRE” on page 31. 
If this is a manual entry and … Then do the following …
You know the location Key in the location code of where the item 
will be stored and press Enter.
You know the location but the product for 
this line has to be stored in more than one 
location because it did not all fit into a single 
location
See the next section “Receiving a Single Item Line into Multiple Locations” on page 28.
You do not know the location yet Press Enter to bypass the field. Later, when 
you attempt to confirm the receipt, the system will prompt you that the location is 
missing. At that time, you must query this 
receipt in ENRE and key in the missing 
location in order to be able to confirm the 
receipt.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 27

ENRE Line Block screen
19 You are taken back to the Line field at the beginning of the Line Block. A new line (Line 2) displays for 
you to continue entering the next item line from the receiving documents. If a new line number does not 
display, click on Create Record.
Repeat the Line Block procedure for each line (entity). The upper right hand corner of the screen displays 
a current record counter for your reference. 
When you have completed entering all of the receipt lines, click on Return to Main and Master Block.
a new Line 
Block 
record displays for 
completion

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)

ENRE Header Block screen
20 You are now taken back to the beginning of ENRE where the system shows the receipt number it has 
generated.
21 If you wish to enter another receipt, click on Create Record. 
22 If you wish to exit the ENRE program, click on Exit. The following message may display on your screen: 
“The remaining Units are not 0, do you want to continue? (Yes) (No).” The system is alerting you to the 
fact that the number in the Total Units field of the Header Block does not equal the number of units that 
was entered in all of the Line Block records when they are added together. Key in Y.
Messages previously set up in Adjust Inventory Messages (ADIM) may appear in the Line Block. These 
messages are for display purposes only and do not print on any document or report.
RECEIVING A SINGLE ITEM LINE INTO MULTIPLE LOCATIONS
It may happen that the total amount of an item for a single receipt line does not fit into one warehouse location 
or that the item has to be split into more than one location for whatever reason. If this is the case, use the 
Location Block. This block allows you to store the receipt line in more than one location. 
1 Complete the ENRE Header Block. Complete the Line Block fields normally, but leave the Location field 
blank.
2 Click on Return to Main to exit create record mode.
system-generated 
receipt number

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 29

ENRE Line Block showing how to access the Location Block
3 Click on Location Block. The Location Block appears on the screen and the system fills in the Location 
Line Number.

ENRE Line Block showing the Location Block
Click on 
Location 
Block
Location 
Block lines 
for entering 
put-away 
instructions

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
4 Key in the location code of where the first portion of the product will be stored and press Enter.
The system populates the Warehouse Code field and skips over it.
5 Key in the quantity that will be stored in this location and press Enter.
6 Key in a hold code, if applicable, and press Enter. If you do not know the code, use the pick list.
If no hold code is necessary, press Enter. The cursor moves to the next Location Line Number (Line 2). 

Location Block showing Location Proof box
7 Note the Location Proof Box just above the Location Block on the right hand side, which indicates the following information:
When the balance indicates 0, it means that all units have been entered. 
8 In Line 2 of the Location Block, key in the location code, quantity and hold code for the next portion of the 
product that will be stored in this second location.
Repeat until the Location Proof Balance is 0. 
9 Click on Line Block.
10 If you need to enter another line in the Line Block, click on Create Record. To exit ENRE, click on Master 
Block and then Exit.
Total Total units received for this line
Entered Number of units entered into locations up to this point
Balance Number of remaining units that still need to be entered into locations. 

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 31
RE-RECEIVING INVENTORY
If you re-receive inventory, the following message may display “Caution, this entity is in the system, do you 
wish to re-receive? (Yes) (No).” The system is alerting you to the fact that this item — with these exact 
inventory levels — has been received into the warehouse before. You can click on Yes to re-receive the 
inventory or you can click on No to change one or more inventory levels.
The re-receive message only appears if the on-hand plus on-receipt quantity of the inventory being rereceived is greater than zero.
CREATING LOCATION CODES ON THE FLY
You can create new location codes while in ENRE without leaving the receipt entry program to enter LOCA 
(Locations).
1 Enter your receipt header information in the normal manner.
2 In the Line Block, enter your inventory levels for the item being received as well as the expected quantity.
3 Enter your new location code and press Enter.
4 Click on Create Code to enter LOCA (Locations).
LOCA screen in Create Record mode
5 In LOCA, enter your location information in the normal manner.
6 When the Line Block redisplays, continue to enter your receipt line in the normal manner.
ENTERING INFORMATION IN THE OPTIONAL BLOCKS OF ENRE
If you indicated in the Header Block that you need to enter details in any of the ENRE Optional Blocks, they 
will appear now in succession. The following procedures will assist you in completing these blocks.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
REMARKS BLOCK
The Remarks Block will appear on the screen if the Remarks field in either the Header Block or the Line Block 
is set to Y (for Yes). A remark can be any useful message that will appear on the screen. The remark will also 
print on the actual receipt document if this option was preset in your system.
1 Key in your remarks. 

Remarks Block screen showing two remark entries
2 When you finish entering all remarks for this receipt, click on Return. 
3 If you are in create record mode, the next optional block or the Line Block appears on the screen for completion. Continue to process the receipt in the usual manner.
EXTENDED REMARKS BLOCK
If activated in COMP (Company Code), the Extended Remarks screen allows you to attach one or more 
messages to a given receipt document. The message can be either a predefined message in MESS or a freetext message that you enter manually. Unlike the messages in DPME (Depositor Print Messages), these 
messages print for a specific receipt only.
NOTE No individual “word” can exceed 40 characters and no line can exceed 45 
characters.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
OPERATIONS 1 GUIDE 4.2 33
For example, if you select Customer Message and BF (Blast Freezing) as your message code, the text 
“Customer Message” and “BF (Blast Freezing)” will print on your selected document.
1 Select the checkboxes that apply to your remarks: Customer Message, Shipper Message or Carrier Message.
2 If required, select your document from the Document Code pick list.
3 Do one of the following:
Extended Remarks screen
4 Click on Save.
5 Click on Exit.
CARRIER BLOCK
The Carrier Block will appear on the screen if the Carrier Details field in the Header Block is set to E for Entry 
or B for Both. It records data concerning the transportation vehicle and the driver that brought the product to 
NOTE Adding the message to an actual document such as a bill of lading or receipt 
tally may require custom programming by HighJump.
If you are using a predefined 
message:
If you are entering a free-text 
message:
a) Select your message code from 
the Message Code pick list.
a) Key in a free-text message in the 
Message Text field.

RECEIVING
Entering a Regular Type Receipt — P (Post-Receiving)
the warehouse. You can capture information such as the power unit number, the trailer number, the seal 
numbers and the front, middle and back temperatures.
You can also capture your pallet in and pallet out quantities. Unlike pallets entered in the Pallet Block, pallets 
entered in the Carrier Block are not assigned a pallet type or an account and are not tracked in LOPC (Look 
Up Pallet Control).
Only the driver code is mandatory in the Carrier Details block. However, you must go through each field in this 
block before you can save a carrier record.
1 The Carrier Block is in the Create Record mode. Enter the Driver Code and press Enter. If you do not 
know the code, use the pick list. The system automatically fills in the Name field. 
If the driver’s name is not in the pick list, key in / and press Enter. Then enter the driver’s name in the 
Name field.
2 Enter the Power Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass 
the field.

Carrier Block screen
3 Enter the Carry Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
4 Enter the Vessel Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
5 Enter the Voyage Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
6 Enter the Seal 1 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
7 Enter the Seal 2 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.

RECEIVING
Understanding Warehouse Restrictions
OPERATIONS 1 GUIDE 4.2 35
8 Enter the temperature readings for the front, middle and back of the transportation vehicle, if applicable, 
and press Enter. If it does not apply, press Enter to bypass the three fields.
9 In the Setting field, if applicable, key in the temperature that the transportation vehicle’s thermostat control is set at and press Enter. If it does not apply, press Enter to bypass the field.
10 If required, key in your pallet in and/or pallet out quantities in the fields of the same name and press 
Enter.
11 If you are in create record mode, click on Exit to display the next optional block or the Line Block. Continue to process the receipt in the usual manner.
Understanding Warehouse Restrictions
This chapter only applies if your system uses more than one Warehouse Code for storing or putting away 
product and if your company performs manual put-away. 
The process of assigning where to put-away product can be done in either of two ways:
 automatically by AccellosOne 3PL (also called system-directed put-away)
 manually by warehouse personnel 
In ENRE, recording the put-away of an item involves three fields in the Line Block:
 Warehouse Code
 Location Code
 Hold Code
When completing ENRE in a system-directed put-away environment, you leave the Warehouse, Location and 
Hold fields blank for the Active Locator to complete. (The Active Locator is a software program that automatically assigns where to put away product when receiving and from where to pick product when shipping.)
When completing ENRE in a manual put-away environment, you record where the item has already been 
stored or leave it blank if the storage location is not yet known. Nonetheless, while recording the put-away 
location, the system may restrict you to certain warehouse and location codes. It is therefore helpful to be 
aware of the put-away options that are available and the restrictions that apply. Preset warehouse restrictions 
display as the system default. The system does allow you a few options, in specific circumstances, to override 
the system defaults.
Preset Warehouse Restrictions
A warehouse restriction code may have been previously attached to either the customer of an item in (CUST) 
or to the item itself in (ITEM). 
If there are two preset warehouse codes, one in ITEM and one in CUST, the ITEM restriction overrides the 
one in CUST. 
When there is a preset code, it will appear as the default in the ENRE Line Block. When entering a receipt for 
such an item, you will be restricted to this warehouse and its locations for storing or putting away the product.

RECEIVING
Preset Warehouse Restrictions
Preset warehouse restrictions apply to the whole receipt. If you have to enter fifty Line Block records for this 
receipt, this restriction will appear as the default every time.
OPERATOR-SELECTED RESTRICTIONS
Different items (different receipt lines) on the same receipt may have to be put away in different locations. 
Because the preset warehouse restrictions apply to the whole receipt, the system allows you two options to 
override these restrictions in the Line Block. You therefore have some flexibility in ENRE when recording the 
put-away information for different lines. 
The first option, which is always available, allows you to restrict multiple lines of a receipt to a common 
warehouse. See “Restricting Multiple Item Lines to a Common Warehouse” on page 36.
The second option, which is only available on systems that have a warehouse restriction set in the Depositor 
Shipping and Receiving Profile (DSRP), allows you to restrict individual item lines to a specific warehouse. 
See the section “Restricting Individual Item Lines to a Specific Warehouse” on page 38.
RESTRICTING MULTIPLE ITEM LINES TO A COMMON WAREHOUSE 
A warehouse restriction option is available in the ENRE Header Block in the Warehouse Code field. When 
you enter a code in this field, it automatically shows as the default in the Line Block’s Warehouse Code field. 
Also, only that warehouse’s locations will be available as put-away options in the Location Block. The 
Warehouse Code entered in this field will override any other preset warehouse restrictions attached to this 
item in (ITEM) or to this customer in (CUST).
This option is useful if you are entering a receipt with many line items and all or most of the receipt line items 
are to be stored in the same warehouse. For example, if you have a receipt with 100 line items and 90 are to 
be stored in the same warehouse, enter the Warehouse Code that applies to the 90 lines. This will save you 
keystrokes in the Line Block.
1 Enter ENRE. 
2 Complete the Header Block until you reach the Warehouse Code field. 
3 Key in the Warehouse Code that applies to the majority of the receipt item lines. If you do not know the 
code, use the pick list. 

RECEIVING
Preset Warehouse Restrictions
OPERATIONS 1 GUIDE 4.2 37


Warehouse code entered in header becomes warehouse restriction default in the Line Block
4 Complete the Line Block for all item lines that will be stored in the same warehouse. 
5 Click on Return to Main and then Master Block to return to the Header Block. Press Enter until the cursor 
is in the Warehouse Code field. 
If the remaining line items will be placed in different warehouses, Press F11 (Clear Field) to leave the 
field blank and press Enter. 
If, on the other hand, there is another large group of line items to be stored in a common warehouse, key 
in that Warehouse Code and press Enter. If you do not know the Warehouse Code, use the pick list.
6 Click on Line Block.
7 Click on Create Record. Continue entering the remaining item lines in the usual manner.
a warehouse 
code entered 
here becomes 
the warehouse 
restriction 
default in the 
Line Block

RECEIVING
Preset Warehouse Restrictions
8 When all line items of the receipt have been entered, click on Return to Main and then Master Block. 
9 If you wish to enter another receipt, click on Create Record. If you wish to exit ENRE, click on Exit.
RESTRICTING INDIVIDUAL ITEM LINES TO A SPECIFIC WAREHOUSE 
A warehouse restriction option may be available in the ENRE Line Block in the Warehouse Restriction field. 
However, this option is only available if this item has a warehouse restriction flag set up in its Depositor 
Shipping and Receiving Profile (DSRP). 
You will know whether this option is available if the cursor enters the Warehouse Restriction field. The Help 
Message Line will indicates “Enter a warehouse restriction if required.” If the cursor skips over the Warehouse 
Code field, then the option is not available for this receipt.
An entry in the Warehouse Restriction field will override all other warehouse restrictions previously applied to 
this item or line. That is, it will override any preset warehouse restrictions attached to this item or customer as 
well as any manually entered restriction in the ENRE Header Block, Warehouse Code field. When you enter a 
code in this field, it will automatically show as the default in the Line Block’s Warehouse Code field and only 
that warehouse’s locations will be available as options for storing the product.

ENRE Line Block with the Warehouse Restriction field set to 01
1 Enter ENRE. 
2 Complete the Header Block and the Line Block in the normal manner until you reach the Warehouse 
Code field. 
3 If the cursor enters the Warehouse Restriction field, choose the applicable option from the following:
If a warehouse restriction is not necessary, press Enter to leave the field blank.
If storage of this line item is to be restricted to a specific warehouse, key in the Warehouse Code and 
press Enter. If you do not know the code, use the pick list. 
If you enter 
a warehouse 
code in the 
Warehouse 
Restriction 
field, putaway is 
restricted to 
that warehouse 

RECEIVING
Preset Warehouse Restrictions
OPERATIONS 1 GUIDE 4.2 39
4 Continue completing the Line Block for this record in the normal manner. 
5 If necessary, enter other Line Block records for each different item. When all line items of the receipt 
have been entered, click on Return to Main and then Master Block. 
6 If you wish to enter another receipt, click on Create Record. If you wish to exit ENRE, click on Exit.
WAREHOUSE RESTRICTION SUMMARY
The following table shows how the setting of the various AccellosOne 3PL warehouse restriction options 
affects put-away of product. 
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
None None None The warehouse restriction set in CUST will display as the 
default.
Put-away of product is restricted to this warehouse and 
its locations.
None None None The warehouse restriction set in ITEM will display as the 
default.
Put-away of product is restricted to this warehouse and 
its locations. 
None None The warehouse restriction set in CUST will display as the 
default. 
The CUST restriction overrides the ITEM restriction. 
Put-away of product is restricted to this warehouse and 
its locations.
None The warehouse restriction that was manually entered in 
the ENRE Header Block will display as the default. 
This manually entered warehouse restriction overrides 
both the ITEM and the CUST restrictions. 
Put-away of product is restricted to this warehouse and 
its locations.

RECEIVING
Modifying a Receipt
Modifying a Receipt
You can re-open and modify receipts in ENRE as long as they have not been confirmed. Data in both the 
Header and Line Block fields can be changed.
You can check whether or not a receipt has been confirmed in the program LORE (Look Up Receipts). This 
program has a Status field, which will display “Confirm Receipt…” if the receipt has been confirmed. If the 
receipt has not been confirmed, the LORE Status field will show the name of the current flow process in the 
flow process sequence for this receipt.
MODIFYING HEADER BLOCK DATA
If you modify a receipt’s shipper and if that shipper has a workflow profile that differs from the customer’s 
workflow profile, AccellosOne 3PL will use the receipt’s original workflow profile, not the new workflow profile.
1 Enter ENRE. The program is in the Create Record mode.
2 Click on Enter Criteria.
The warehouse restriction that was manually entered in 
the ENRE Line Block Warehouse Restriction field will 
display as the default. 
This manually entered warehouse restriction overrides 
any other restriction in ITEM, CUST and the ENRE 
Header Block. 
Put-away of product is restricted to this warehouse and 
its locations.
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

RECEIVING
Modifying a Receipt
OPERATIONS 1 GUIDE 4.2 41

ENRE screen showing the method of calling up an unconfirmed receipt
3 Key in the system-generated number of the receipt that you want to modify. 
4 Click on Execute Query. The receipt will display on your screen. 
5 Press Enter to change from Main Mode to Modify Record mode.
6 Press Enter the required number of times until your cursor is in the field that you want to modify. Press 
F11 (Clear Field).
Set the program in the Enter 
Criteria mode.
Key in the number of the 
unconfirmed receipt that you 
wish to modify.
Press Execute Query.

RECEIVING
Modifying a Receipt

ENRE screen showing Modify Record mode
7 Key in the new data and press Enter.
8 If you need to make additional changes to other Header Block fields, repeat steps 6 and 7 until all of the 
necessary changes are entered.
9 If you need to make changes to data in the Line Block, click on Line Block and follow the procedure 
below. 
10 When no further changes are required, click on Return to Main and then Exit to exit ENRE.
MODIFYING LINE BLOCK DATA
The following procedure applies to all types of Line Block records except for U (Unknown), which always 
allows you to open the receipt and fill in missing data.
1 Enter ENRE. 
2 Click on Enter Criteria. 
3 Key in the system-generated number of the receipt that you want to modify and click on Execute Query. 
The receipt will display on your screen. 
4 Click on Line Block. 
5 If this receipt has more than one Line Block record, key in the number of the Line Block record that you 
wish to change and press Enter. If not known, use your up and down arrow keys to find the Line Block 
number needing modification.
Set the program in 
Modify 
Record 
mode.
Press Enter 
until your 
cursor is in 
the field 
that you 
wish to 
change.

RECEIVING
Modifying a Receipt
OPERATIONS 1 GUIDE 4.2 43

ENRE Line Block screen
6 If you need to change the Received Quantity and/or Location Code fields, press Enter until the cursor is 
in the desired field. Press F11 (Clear Field). Key in the new data and press Enter.
If you need to change the Product Code, Receive Date, Expiry Date or Expect Quantity fields, you will 
need to delete the entire Line Block record. Refer to“Deleting an Entire Line Block Record” on page 48. 
7 Click on Return to Main to return to the beginning of the Line Block. Repeat steps 7 and 8 if you need to 
change any other Line Block records for this receipt or click on Master Block and Exit to exit the program.
MODIFYING LOCATION BLOCK DATA
You must have multiple locations assigned to the same receipt line before you can enter the Location Block 
and make changes to it.
The following procedure applies to all types of Line Block records except for U (Unknown), which always 
allows you to open the receipt and fill in missing data.
1 Enter ENRE. 
2 Click on Enter Criteria. Key in the system-generated number of the receipt that you want to modify and 
click on Execute Query. The receipt will display on your screen. 
3 Click on Line Block. 
4 If this receipt has more than one Line Block record, key in the number of the Line Block record that you 
wish to change and press Enter. If this number is not known, use your up and down arrow keys to find the 
Line Block number needing modification.
5 Click on Location Block.
6 Press Enter. You are now in Modify Record mode.
Enter the 
line number 
of the record 
that you 
wish to modify

RECEIVING
Modifying a Receipt

ENRE Line Block screen showing the Location Block
7 Use the up and down arrow keys to move the cursor next to the Location Line that needs to be modified.
8 Press Enter the required number of times until the cursor is in the field that you need to modify. Key in the 
new data and press Enter.
If you want to move product from one location to another, you must reduce the quantity in the from location before you add to the quantity in the to location. You cannot add to the quantity in the to location first.
9 Click on Return to Main to return to the beginning of the Location Line Block. To enter a new line, click on 
Create Record. To exit, click on Line Block and Master Block. Then click on Exit.
MODIFYING OPTIONAL BLOCKS DATA
The procedure for modifying the Remarks, Carrier Details, Accessorial Charges and Receipt Extra Charges 
blocks is the same. The following procedure uses the Remarks Block as an example for the procedure.
1 Enter ENRE. 
2 Click on Enter Criteria. Key in the system-generated number of the receipt that you want to modify and 
click on Execute Query. The receipt will display on your screen. 
Use the arrow 
keys to move 
the cursor next 
to the line that 
you need to 
modify. 
Press Enter to 
the field that you 
need to modify.

RECEIVING
Modifying a Receipt
OPERATIONS 1 GUIDE 4.2 45

ENRE Header Block screen showing how to access the optional blocks
3 In the Header Block, press Enter until the cursor is on the Y of the Remark field.
4 Click on Remarks.

ENRE Remarks Block screen
5 Clear the existing data and key in the new remark.
6 When you finish making your corrections, click on Return. Then click on Return to Main and then Exit to 
exit.
Place the cursor 
in the field of the 
optional block 
that you wish to 
modify. 
Then click on the 
corresponding 
button.

RECEIVING
Deleting a Receipt
CHANGING THE INVENTORY LEVEL ON A RECEIPT LINE
You can change the inventory level on a receipt line in CHRL without the need to enter ENRE and enjoy full 
access to all the fields in that program.
1 Enter CHRL.
2 Key in your receipt number and press Enter.
CHRL screen
3 If the receipt has multiple lines, select the line whose inventory level you wish to change.
4 Key in your new level 2, 3 or 4 value and press Enter.
5 Click on Update Line.
6 Click on Exit.
Deleting a Receipt
Receipts may need to be deleted due to errors. You can delete receipts in ENRE as long as they have not 
been confirmed.
You can check whether or not a receipt has been confirmed in the program LORE (Look Up Receipts). This 
program has a Status field, which will display “Confirm Receipt…” if the receipt has been confirmed. If the 
receipt has not been confirmed, the LORE Status field will show the name of the current flow process in the 
flow process sequence for this receipt.

RECEIVING
Deleting a Receipt
OPERATIONS 1 GUIDE 4.2 47
You can view details of deleted receipts in LORE. Deleted receipts remain in LORE until they are purged in 
the program Purge Orders, Receipts, Inventory (PURG).
DELETING AN ENTIRE RECEIPT
1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in the system-generated number of the receipt that you want to delete and click on Execute Query. 
The receipt will display on your screen.
4 Press Enter. You are now in Modify Record mode and the Delete button will appear at the bottom of the 
screen.

ENRE Header Block showing the Delete entire receipt option
5 Click on Delete. 
Set the mode 
to Modify 
Record. 
Delete button displays 
as an option.

RECEIVING
Deleting a Receipt

ENRE Header Block showing Deletion message
6 A message block displays asking if you want to proceed with the deletion. On your keyboard, key in the 
letter of whichever of the following options applies to your situation and press Enter.
If you choose R (Remarks Block), the receipt will be deleted and the Remarks Block will display. Key in 
the reason for deleting the receipt and press Enter. A message block appears indicating the receipt is 
being deleted.
7 Click on Exit to exit the ENRE program.
DELETING AN ENTIRE LINE BLOCK RECORD 
There may be situations in which you need to delete an entire Line Block record. For instance, this would be 
necessary under the following circumstances:
 to cancel an item from an unconfirmed receipt that was previously entered in ENRE 
 to change the Product Code, Receive Date, Expiry Date or Quantity Expected fields on a receipt
When you delete a receipt line record and then create a new receipt line, the line number of the new line 
depends on the number of lines on the receipt and the line number that you deleted. Refer to the following 
table for the renumbering rules in AccellosOne 3PL:
Y (Yes) If you wish to delete without entering any remarks as to why this 
receipt is being deleted.
N (No) If you do not want to delete this receipt.
R (Remarks) If you want to delete this receipt and include remarks explaining 
why this receipt is being deleted. The remarks will be saved with 
the deleted receipt.
If … then …
you delete the first line of an receipt with a 
single receipt line
the next new line created will be line 1

RECEIVING
Deleting a Receipt
OPERATIONS 1 GUIDE 4.2 49
1 Enter ENRE. 
2 Click on Enter Criteria. 
3 Key in the system-generated number of the receipt you want to delete and click on Execute Query. The 
receipt will display on your screen. 
4 Click on Line Block.
5 Key in the number of the Line Block record that you wish to delete and press Enter. If not known, use 
your up and down arrow keys to find the line number needing deletion.

ENRE Line Block screen showing the Delete entire Line Block option
6 Press Enter until the Delete button appears at the bottom of the screen. 
you delete any line except the first line or 
the last line of an receipt with multiple 
receipt lines
the next new line created will be the last line 
+ 1
you delete the last line of an receipt with 
multiple receipt lines
the next new line created will be line number of the line that you just deleted
If … then …
Delete 
option

RECEIVING
Deleting a Receipt
7 Click on Delete. A message block displays asking if you want to proceed with the deletion. Click on the 
appropriate button.
The line that you were on will disappear and the previous line number and its details will be displayed.
8 If you wish to create a new line with new data, click on Create Record and complete the Line Block in the 
usual manner. If you wish to exit, click on Return to Main and Master Block. Then click on Exit.
DELETING LOCATION BLOCK DATA
You use the following procedure to delete records from the Location Block. Records in the Location Block are 
composed of lines. (These are different than Line Block lines.) When you delete in the Location Block, you 
delete the whole line record.
1 Enter the Line Block. Key in the line number of the record that you wish to delete and press Enter. If not 
known, use your up and down arrow keys to find the line number that you need to delete.
2 Click on Location Block.

ENRE Location Block showing two line entries
3 Use the up and down arrow keys to move the cursor next to the line that you wish to delete.
4 Press Enter until the Delete button appears. Then click on Delete.
Y (Yes) If you wish to delete the Line Block record without entering any 
remarks as to why this record is being deleted.
N (No) If you do not want to delete this Line Block record.
Set the cursor 
at the end of 
the line that 
needs to be 
deleted

RECEIVING
Receipt Header Types and Receipt Line Types
OPERATIONS 1 GUIDE 4.2 51
5 Click on Return to Main to return to the beginning of the Line Block. To Enter a new line, click on Create 
Record. To exit, click on Line Block and Master Block. Then click on Exit to exit.
Receipt Header Types and Receipt Line Types
There are six types of receipt headers in AccellosOne 3PL. The receipt header type indicates which of the 
automatic inbound handling and initial storage charges are to be applied to this receipt when it is rated. The 
profiles for these automatic charges were previously set up in AccellosOne 3PL for your warehouse company. 
P (Post Receiving) is the normal receipt type. It indicates to the system that the regular automatic charges for 
inbound handling and initial storage are to be applied to this receipt. You use the other five types in special 
circumstances when you need to override the normal charge setups.
RECEIPT LINE TYPES
Warehouse charges can vary for each item line of a receipt. Therefore, there are different receipt line types in 
AccellosOne 3PL to regulate the charges that are to be applied to each line. Be sure to select the correct 
receipt line type.
P (Post-receiving) Use if there are both inbound handling and initial storage charges 
to be applied to this item line. Also, all of the inventory levels must 
be known for the product. This is a regular receipt type line.
N (No Charge) Use if there are no charges to be applied to this item line.
H (Handling Only) Use if only the inbound handling charge is to be applied to this item 
line (that is, there will be no initial storage charge).
S (Storage Only) Use if only the initial storage is to be applied to this item line (that 
is, there will be no inbound handling charge).
I (In-transit) See “In-Transit Receipts” on page 53.
C (Confirm) Use if you wish to confirm the receipt when you exit ENRE. This 
option allows you to enter and confirm a receipt in a single step 
without going through the standard inbound flows defined in DIFP.
P (Post-receiving) Use if there are both inbound handling and initial storage charges 
to be applied to this line. Also, all of the inventory levels must be 
known for the product. This is a regular receipt type line.
N (No Charge) Use if there are no charges to be applied to this line.
H (Handling Only) Use if only the inbound handling charge is to be applied to this line 
(that is, there will be no initial storage charge).

RECEIVING
Confirm-Type Receipts
Confirm-Type Receipts
A confirm-type receipt is a receipt that you enter and confirm in a single step without going through the 
standard inbound flows defined in DIFP. When you exit ENRE after entering all your lines, AccellosOne 3PL 
will automatically confirm the receipt.
1 Enter ENRE.
2 In the Customer Code field, key in your customer code and press F9.
3 In the Receipt Type field, key in C for Confirm and press Enter. 
4 Complete the Header Block in the usual manner for the receipt.
S (Storage Only) Use if only the initial storage is to be applied to this line (that is, 
there will be no inbound handling charge).
O (Open Lot) See the Billing and Invoicing Guide for further information on 
this type of receipt.
X (Cross Dock) Use only for cross docking. If you enter this line type, you will be 
prompted to enter a cross dock profile in the Cross Dock field. Special inbound handling and initial storage charges will apply. See the 
Billing and Invoicing Guide for further information.
U (Unknown) See “Receipts With Unknown Inventory Levels” on page 
54.
I (In-transit) See “In-Transit Receipts” on page 53.
NOTE Confirm-type receipts do not support directed put-away or the printing of 
inbound documents. You must manually enter your locations in the Line Block of 
ENRE.

RECEIVING
In-Transit Receipts
OPERATIONS 1 GUIDE 4.2 53

ENRE screen showing confirm-type receipt
5 In the Line Block, enter all required information including the location code and warehouse code.
6 When you finish entering all your lines, press F4 the required number of times to exit.
In-Transit Receipts
An in-transit receipt is a receipt that has been shipped to the warehouse but has not yet arrived. This receipt 
type is typically used when you receive an advance shipment notice of product to be received. After the 
product arrives at the warehouse, the system will change this to a P-type receipt during the receiving process. 
When you create an in-transit receipt, the receipt line’s quantities will display in the Location Block of Look Up 
Entity Information (LOEN) under the In-Transit column. Once the product arrives at the warehouse, the 
system changes the receipt line type from In-transit (I) to Post-receiving (P) and moves the receipt line’s 
quantities from the In-Transit column to the On Receipt column in the Location Block of LOEN.
RECEIVING AN IN-TRANSIT RECEIPT WHEN ALL INVENTORY LEVELS ARE 
KNOWN
1 Enter ENRE.
2 In the Customer Code field, key in your customer code and press F9.
3 In the Type field, key in I for In-Transit and press Enter. 
4 Press Enter again to bypass the Customer Code field.
5 Complete the Header Block in the usual manner for the receipt.

RECEIVING
Receipts With Unknown Inventory Levels
6 Complete the Line Block in the usual manner for the receipt. Enter all inventory levels but do not enter 
locations.
7 When you finish entering your receipt lines, click on Return to Main and Master Block. Then click on Exit 
to exit.
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
8 When you finish entering your receipt lines, click on Return to Main and Master Block. Then click on Exit 
to exit.
9 Enter the missing inventory levels when known.
10 Advance the flow of the receipt in CHRF. 
11 Return to ENRE and enter your location information.
12 Confirm the receipt in the usual manner. A pop-up box will appear with the message “Change In-transit to 
Post Receiving”.
Receipts With Unknown Inventory Levels
A receipt line type of U for Unknown allows you to create a receipt for an item when there is missing data for 
some of the item’s inventory levels. A regular P (Post-receiving) type of receipt line would not allow you to 
bypass inventory level fields.
You must return to a U-type receipt line and complete the missing information before confirming the receipt in 
Time-Stamp and Confirm Receipts (CHRF).
Item quantities of U-type receipt lines do not show in LOEN because their inventory levels are missing. When 
the missing inventory levels are completed in ENRE, then they will appear in LOEN.
1 Enter ENRE.
2 Leave the Header Block’s Receipt Type field as P. Complete the Header Block in the usual manner.

RECEIVING
Receipts With Unknown Inventory Levels
OPERATIONS 1 GUIDE 4.2 55
3 When the screen displays the Line Block, press F9 (Previous Field) until the cursor is in the Type field. 
Key in U and press Enter.
4 Complete the Line Block fields until you reach Item Code.
5 Key in the Item Code and press Enter. If you do not know the code, use the pick list.

ENRE Line Block showing an Unknown receipt type
6 Press Enter to bypass any inventory level fields with missing information. Key in the information for 
inventory level fields with available data. Press Enter.
7 Continue completing the Line Block fields in the normal manner. The system will bypass the Location 
Code field as you cannot enter location information for a receipt line until the missing inventory levels are 
entered.
8 In the Hold Code field, key in your hold code and press Enter. If you do not require a hold code, press 
Enter with no code entered to bypass this field.
9 Enter any remaining receipt lines. When you finish, click on Return to Main and Master Block. Then click 
on Exit to exit ENRE. 
10 Do not confirm the U-type receipt line. You must return to this receipt and complete the missing inventory 
levels once you know them.
LOOKING UP PENDING RECEIPTS IN LOPR
You look up pending receipts in LOPR (Look Up Pending Receipts). A pending receipt is a receipt containing 
one or more U-type lines indicating missing inventory levels.
For each pending receipt that you look up in LOPR, AccellosOne 3PL shows the receipt number, the line 
number for the unknown inventory, the receipt date, the pending quantity, the pending weight and the pending 
cube.
In an 
Unknown 
receipt type, 
the system 
allows you to 
bypass 
inventory levels with missing data

RECEIVING
Receipts With Unknown Inventory Levels
1 Enter LOPR.
2 Key in your search criteria for each field and press Enter. You can query on customer code, any inventory 
level except the lowest level and receipt date. 
3 When you finish entering your search criteria, click on Execute Query.

LOPR screen
4 When you finish looking up your pending receipts, click on Exit to exit.
ENTERING THE MISSING INVENTORY LEVELS IN AN UNKNOWN RECEIPT
When you enter the missing inventory levels in ENRE, AccellosOne 3PL changes the line type from U for 
Unknown to P for Post-Receiving. 
1 Enter ENRE.
2 Click on Enter Criteria.
3 Key in the receipt number of the U-Line receipt and click on Execute Query.
4 Click on Line Block.
5 Key in the Line Block number of the U Line record that you need to complete and press Enter or use the 
up and down arrow keys to find it.

RECEIVING
Sequential Entry Receipts
OPERATIONS 1 GUIDE 4.2 57

ENRE Line Block screen showing an Unknown receipt type
6 Press Enter until the cursor is in the first Inventory Level with missing data. Key in the data and press 
Enter.
7 Key in the data for other Inventory Levels, if applicable, and press Enter.
8 If this is a manual put-away and the location code is missing, press Enter until the cursor is in the Location Code field, key in the Location Code and press Enter.
9 Key in the hold code, if applicable, or press Enter to bypass the field.
10 Repeat the procedure for any other U-type receipt lines. 
11 When you finish updating your U-type lines, click on Return to Main and Master Block. Then click on Exit 
to exit the program.
Sequential Entry Receipts
A sequential entry receipt is a receipt in which you enter your higher inventory levels (for example, levels 1 
and 2) once and these levels are automatically attached to lower levels (for example, level 3). Sequential 
entry allows you to avoid repetitive entry of the same data.
For example, suppose you have a three-level inventory profile consisting of item/lot/pallet ID and you are 
receiving a lot with 20 pallets on it. Sequential entry allows you to enter the item code and lot number once for 
all 20 pallets; when you key in your pallet ID’s, the system attaches them automatically to the same item code 
and lot.
Complete 
the missing inventory level 
data and 
the location code

RECEIVING
Sequential Entry Receipts
To set up sequential entry, enter the Level Block of DILP (Depositor Inventory Level Profile) and arrow down 
to the level of inventory that changes when receiving. Then use your pick list to select A for Receipt Entry 
from the Sequential Entry field.

DILP screen showing Sequential Entry field set to Receipt Entry for Level 3 (PID)
PROCEDURE
You enter a sequential entry receipt by entering all inventory levels for your first receipt line in the normal 
manner. Then you key in the number of times that you wish to repeat the same level 1/2/3 values for each 
new inventory entity for which sequential entry is activated.
If you wish to bypass sequential entry on a specific receipt line, you do not enter the number of times that you 
wish to repeat your higher inventory levels. When you bypass sequential entry, you will be required to enter all 
inventory levels for each receipt line.
In the following example, you are receiving a three-level item (item, lot, and pallet ID) and sequential entry is 
activated for level 3 (pallet ID).
1 Enter ENRE and key in your header information normally.
2 When the Line Block appears, key in all inventory levels for the first inventory entity that you are receiving. When you finish entering your last inventory level, your cursor will be positioned in a blank field on 
the right-hand side of your screen.

RECEIVING
Sequential Entry Receipts
OPERATIONS 1 GUIDE 4.2 59

ENRE screen showing cursor in blank field
3 Key in the number of times that you wish to repeat the same item, lot and date code for each new pallet 
ID and press Enter. If you wish to bypass sequential entry for this receipt line, leave the field on righthand side of the screen blank and press Enter.
You enter 
the number of times 
that you 
wish to 
repeat this 
item and lot 
here

RECEIVING
Sequential Entry Receipts

ENRE screen showing the number of lines for item D1, lot 102
4 Enter the expected and received quantities for this pallet ID plus any other required information until your 
line is complete. When you finish entering your first line, AccellosOne 3PL will create a second line showing inventory levels 1, 2 and 3 filled in with the values from the previous line.
Number of 
lines for item 
D1, lot 102

RECEIVING
Receipts With System-Generated Inventory Levels
OPERATIONS 1 GUIDE 4.2 61

ENRE screen showing values for levels 1 and 2 automatically entered by the system
5 Key in your lowest inventory level and press Enter. If required, make any necessary adjustments to the 
value showing the remaining number of lines for this item/lot. Then enter the remaining information in the 
Line Block normally.
6 Repeat the above steps for each additional pallet ID that you wish to receive under the same item/lot/
date code.
7 When you finish receiving all pallets for this item/lot/date code, AccellosOne 3PL will create a new line. 
All inventory levels will be blank and you will have to enter all levels manually.
8 Enter a new line or click on Return to Main, Master Block and Exit to exit.
Receipts With System-Generated Inventory Levels
If your system is set up to automatically create level 2, 3 or 4 values using system-generated numbers, you 
can leave the inventory level blank and AccellosOne 3PL will generate a number for it. Depending on your 
Second line 
shows item and 
lot information 
from previous 
line
Remaining 
number of lines 
for this item and 
lot

RECEIVING
Receipts With System-Generated Inventory Levels
system setup in DILP (Depositor Inventory Level Profile), your system-generated number may be generated 
immediately or may be generated when you create a new receipt line.
In the following example, you are receiving a three-level item (item/lot/pallet ID) and your third level — pallet 
ID — is system generated.
1 Enter ENRE and key in your header information in the normal manner.
2 Do one of the following:
3 When the Line Block appears, key in your item code and press Enter.
4 Key in your lot number and press Enter.

ENRE screen showing cursor positioned in the Pallet ID field
CAUTION Only one user can enter a receipt line with system-generated inventory 
levels at any given time. If multiple users enter receipts in your facility, you must make 
sure that you complete the receipt line as quickly as possible so as not to lock out 
other users. For example, if you enter your levels 1 and 2 as well as the expected and 
received quantities but do not complete the line, no other user will be able to create 
new receipt lines for that customer until you complete the line or exit.
If you want the system to 
generate your pallet ID:
If you want to enter your pallet ID 
manually:
a) You must enter a warehouse 
code in the receipt header.
a) You can leave the Warehouse 
Code field blank.

RECEIVING
Receiving Variable Quantity Breakdown Inventory
OPERATIONS 1 GUIDE 4.2 63
5 Do one of the following:

ENRE screen showing system-generated pallet ID
6 Enter the expected and received quantities for this pallet ID plus any other required information until your 
line is complete.
7 Enter another receipt line or click on Return to Main and Master Block to exit the Line Block. Then click 
on Exit to exit.
Receiving Variable Quantity Breakdown Inventory
A variable quantity breakdown item is an item whose quantity breakdown is not fixed. For example, lot 101 of 
a given item has 60 cases per pallet, while lot 102 of the same item has 80 cases per pallet.
If you want the system to 
generate your pallet ID:
If you want to enter your pallet ID 
manually:
a) Press Enter to bypass the Pallet 
ID field. Your system-generated 
pallet ID may or may not appear 
on your screen depending on the 
options that you selected in 
DILP.
a) Key in your pallet ID and press 
Enter.

RECEIVING
Receiving Variable Quantity Breakdown Inventory
When you receive a variable quantity item and the inventory entity that you are receiving is being received for 
the first time, you can change the inventory entity’s quantity breakdown. Once you change an inventory 
entity’s quantity breakdown, the new quantity breakdown is fixed and cannot be changed on future receipts 
for that inventory entity.
ITEM screen showing Variable Quantity Breakdown flag set to Y for Yes for item A2
1 In the Line Block of ENRE, press Enter the required number of times to bypass the Remark, Process, 
Charge and Warehouse Restriction fields.
2 Key in your item code and press Enter.
3 Key in your level 2, 3 and 4 values and press Enter.

RECEIVING
Receiving Variable Quantity Breakdown Inventory
OPERATIONS 1 GUIDE 4.2 65
ENRE screen showing PLT field highlighted (that is, an enterable field)
In the Quantity Breakdown field, AccellosOne 3PL will show the SKU’s used to track and bill the item. For 
example, if the Quantity Breakdown field shows PLT: 100 (the largest SKU) and CASE: 1 (the smallest 
SKU), you read it as one pallet has 100 cases.
4 Do one of the following:
5 Enter the expected quantity and received quantity of the new product and continue to enter your receipt 
line normally.
6 When you finish entering your receipt line, press F4 the required number of times to exit.
CHECKING AN ITEM’S VARIABLE QUANTITY BREAKDOWN IN CVQB
The special verify program CVQB (Check Qty Breakdown and Receipt Qty) allows you to check an item’s 
variable quantity breakdown and correct it if it is wrong. It can be attached to any inbound flow after ENRE 
(Enter Receipt).
1 Enter CHRF and advance the receipt’s inbound flow in the normal manner until you reach the flow to 
which CVQB is attached.
If you are receiving the 
inventory entity for the first 
time and wish to change the 
quantity breakdown:
If you are receiving the 
inventory entity for the first 
time and do NOT wish to 
change the quantity 
breakdown:
If you have already received 
the inventory entity:
a) Key in a new quantity breakdown and press Enter.a) Press Enter to accept the 
default quantity breakdown.
a) Proceed to next step.

RECEIVING
Receiving Variable Quantity Breakdown Inventory
CVQB screen showing receipt lines being checked
2 Use your arrow keys to scroll through the list of variable quantity breakdown inventory.
3 If you see a record that you wish to correct, press Enter to position your cursor in the Quantity Breakdown field.
4 Key in your new quantity breakdown and press Enter.
5 When you finish checking your inventory in CVQB, click on Exit to exit.
AUTOMATICALLY UPDATING AN ITEM’S VARIABLE QUANTITY BREAKDOWN IN 
URQB
The special verify program URQB (Update Receipt Quantity Breakdown) automatically updates an item’s 
quantity breakdown when the standard quantity breakdown in ITEM does not match the expected/received 
quantity in ENRE. For example, suppose an item’s standard quantity breakdown is 100 cases and you 
receive 105 cases in ENRE. AccellosOne 3PL will automatically update the inventory entity’s quantity 
breakdown to 105 cases per pallet.
URQB can be attached to any inbound flow after ENRE (Enter Receipt). It runs in the background and does 
not display on your screen.

RECEIVING
Look-Up Programs
OPERATIONS 1 GUIDE 4.2 67
ENRE Line Block showing mismatch between the standard quantity breakdown (100 cases) and 
receive quantity (105 cases)
Look-Up Programs
AccellosOne 3PL has programs that allow you to view data concerning receiving, shipping and inventory 
status. These look-up programs only allow you to view data — you cannot modify, add or delete data in these 
programs. The most commonly used look-up programs for operations are Looking Up Receipts (LORE), 
Looking Up Orders (LOOR), Look Up Entity Information (LOEN) and Look Up Location Information (LOLO).
In the look-up programs, you must first instruct the system to find the records you want to view. There are 
three ways of looking up records in look-up programs:
 you can view all records in the program
 you can view a single record
 you can view all records that meet common selection criteria
VIEWING ALL RECORDS
Leaving a look-up program screen blank (i.e., by not entering any selection criteria) and executing a query will 
retrieve all records in that program.
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Click on Execute Query.
3 The system retrieves all records in the program. Check the current record counter to know which record 
you are viewing currently and how many records there are in total.
4 Use the up and down arrow keys to scroll from one record to another.

RECEIVING
Look-Up Programs

Look-up screen for LORE program
5 When you find the record that you are looking for, view the Header Block and then click on the corresponding button of any record block that you wish to view. When you finish viewing the record, click on 
the appropriate button to exit the block.
6 Repeat the previous step for each additional block that you wish to view.
7 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
8 When you have finished viewing all records, click on Exit in the Master Block to exit the program.
VIEWING A SINGLE RECORD
To view a specific record when you know the system-generated record number, you use the following 
procedure.
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Key in the number of the record. 
3 Click on Execute Query.
The record will display on the screen. 
4 When you find the record that you are looking for, view the Header Block and then click on the corresponding button of any record block that you wish to view. When you finish viewing the record, click on 
the appropriate button to exit the block.
5 Repeat the previous step for each additional block that you wish to view.
6 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
Use the up 
and down 
arrow keys to 
scroll from 
record to 
record.
Press the 
appropriate 
buttons to 
view the block 
details of the 
record that 
you are currently viewing

RECEIVING
Look-Up Programs
OPERATIONS 1 GUIDE 4.2 69
7 When you have finished viewing all desired records, click on Exit in the Master Block to exit the program.
VIEWING ALL RECORDS WITH COMMON SELECTION CRITERIA
This method is useful when you do not know the specific record number of the record that you are looking for 
but you do know other detail(s) about the record. You use the detail(s) that you do know about the record as 
selection criteria. 
The system will only retrieve records with these criteria in common. This will be faster than having to scroll 
through all records in the program to find the one you need.
1 Enter the look-up program. You are in the Enter Criteria mode.
2 Key in the information that you do know about the record in the corresponding fields. For instance, if you 
know the Receipt Date of the record you are looking for and there is a Receipt Date field, key in the date.
The more fields you complete the more you restrict the search. The system will retrieve fewer records for 
you to search through.

Look-up screen for the program LORE
3 Click on Execute Query. The system retrieves all records that meet the selection criteria.
4 Use the up and down arrow keys to scroll from one record to another until you find the record that you are 
looking for. 
5 View the Header Block and then click on the corresponding button of any record block that you wish to 
view. When you finish viewing the record, click on the appropriate button to exit the block.
6 Repeat the previous step for each additional block that you wish to view.
7 When you have seen all of this record’s blocks and you wish to move to another record, click on Master 
Block. Use the up and down arrow keys to scroll to another record.
In this 
example, 
Execute 
Query will 
call up all 
records for 
customer D 
that 
involved 
carrier ABC 
and had a 
receipt date 
of 01.15.07

RECEIVING
Looking Up Telephone Information in LOTE
8 When you have finished viewing all desired records, click on Exit in the Master Block to exit the program.
Looking Up Telephone Information in LOTE
You can look up telephone information in LOTP (Look Up Telephone Numbers). For each number that you 
look up, LOTE shows the telephone number, telephone list code, account type, account name, contact name 
and contact position.
In LOTE you can query by telephone number, telephone list type and account type.
1 Enter LOTE.

LOTE screen
2 Key in your selection criteria. You can search by telephone number, telephone list type (FAX, CELL, 
MAIN or whatever other list types you have defined in TETP) or account type (CU for Customer, BR for 
Broker, CO for Consignee, FR for Freight, GE for General, SH for Shipper or SO for Sold-To).
3 When you finish entering your selection criteria, click on Execute Query.

RECEIVING
Looking Up Receipts in LORE
OPERATIONS 1 GUIDE 4.2 71

LOTE screen showing 10 telephone numbers whose list code is FAX
4 When you finish looking up your telephone numbers, click on Exit to exit.
Looking Up Receipts in LORE
The program Look Up Receipts (LORE) allows you to view all receipts that have been entered into AccellosOne 3PL and that have not been purged. In LORE, it is possible to view receipts of any status — whether 
entered, confirmed, rated or deleted. 
In LORE, you can see all of a receipt’s details. The Status field shows the current inbound flow process for 
this receipt. This lets you know where you are in the flow process sequence. LORE also indicates whether or 
not there are outstanding documents to print for this receipt. 

RECEIVING
Looking Up Receipts in LORE

LORE screen showing the Receipt Block details of receipt number 1209
LORE consists of the following sections:
 Receipt Block (Header Block)
 Time-Stamping Block
 Line Block
 Optional Detail Blocks (if applicable)
The following procedure allows you to view the details of a receipt in the various blocks of LORE. An explanation of the LORE fields and the data they contain follows this procedure.
1 Enter LORE. You are in the Enter Criteria Mode.
2 If you wish to view a specific receipt, key in the Receipt Number and click on Execute Query.
If you wish to view all ENRE receipts, click on Enter Criteria and click on Execute Query.
If you wish to view receipts that meet specific criteria, enter your selection criteria in the corresponding 
field(s) and click on Execute Query.
The Receipt Block details display for you to view.
3 Click on Time Block. The receipt’s time-stamping details display for you to consult.
4 Click on Master Block.
5 Click on Line Block and the Line Block details display for you to view. Use your up and down arrow keys 
to move from one Line Block record to another.
6 Click on Master Block.
receipt’s 
status in the 
flow process 
sequence
the next 
document 
in the flow 
process 
sequence 
that needs 
to be 
printed

RECEIVING
Looking Up Receipts in LORE
OPERATIONS 1 GUIDE 4.2 73

LORE screen showing the Optional Block fields
7 Check the optional blocks fields. If Y, E, C or B is entered next to any of these blocks, there are details. 
Press Enter until the cursor is in the optional field that you want to view. Then click on the appropriate 
button and the optional block details display for you to view. 
8 Click on Master Block. If you want to view another receipt’s details, check the current record counter. If 
there is more than one record, use the down arrow key to scroll to the next record. 
If there is only one record, click on Enter Criteria and key in the selection criteria for the next receipt that 
you wish to view.
9 If you want to exit the program, click on Exit in the Master Block.
RECEIPT BLOCK
The LORE Receipt Block contains basically the same information as the original ENRE receipt. It does, 
however, have some extra fields as described below: 
If Y, E, C or B displays next to any 
of the optional 
blocks, there are 
details. Move the 
cursor to the field 
and the button 
displays as the 
option for that 
block.

RECEIVING
Looking Up Receipts in LORE

LORE screen showing the Receipt Block details for receipt number 1209
FIELD DESCRIPTIONS
Rated Y = Yes
N = No
This flag indicates whether or not the receipt has been rated.
Status The current flow process of this receipt in terms of the flow process sequence. 
Also displays the date and time when the receipt received this status.
On Order The corresponding Order Number if this is a Transfer receipt type.
Receipt Date The date entered in the Receipt Date field of ENRE when the receipt was created.
Received Date The date entered in the Receive Date field of CHRF when the receipt was 
confirmed in Time-Stamp and Confirm a Receipt (CHRF). 

RECEIVING
Looking Up Receipts in LORE
OPERATIONS 1 GUIDE 4.2 75
TIME-STAMPING BLOCK
The Time-Stamping Block displays details regarding the flow processes that have been completed up to this 
point for this receipt. If there is a document attached to a flow and this document has been printed, you can 
click on the View icon to see a PDF version of the document.
If the Appointment Remarks button is enabled, you can look up remarks entered in APPL (Appointment 
Planner) for the appointment’s receipt.
Invoice Date The date when the invoice or warehouse receipt was rated. If your system 
rates the receipt automatically as it is confirmed, this date will always be the 
same as the Received Date. If you rate receipts manually in Receipt Rater 
(RCRA), the Received Date and the Invoice Date may be different if the two 
processes were performed on different dates. 
Location Status Indicates whether all of the receipt’s lines have been assigned a location yet 
(Entered) or whether they are still unassigned (Missing). 
O/S Receipt Reference 
Receipt Source Receipt 
Number
Applicable only to EDI users 
When a very large shipment is divided up and entered in ENRE as more than 
one receipt, the related receipt number displays in this field for reference purposes. (EDI generates the reference number.)
Remarks and Carrier 
Details
Y = Yes
N = No
C = Confirmation
B = Both
E = Entry
If Y, E, C or B is entered next to any of these fields, there are details entered in 
that block. To view the details, press Enter until the cursor is in the optional 
field that you want to view. Then click on the appropriate button and the 
optional block details will display.
Document Status Indicates whether there are any outstanding receiving documents to print for 
this receipt. Names the next document that requires printing according to the 
flow process sequence. 
FIELD DESCRIPTIONS

RECEIVING
Looking Up Receipts in LORE

LORE screen showing Time-Stamping Block
LINE BLOCK
The LORE Line Block shows basically the same fields and details that appear in the original receipt’s ENRE 
Line Block. There is one difference to note, however, which is in the Receive Date field. This field is blank if 
the receipt or the receipt line has not been confirmed. 
FIELD DESCRIPTIONS
Date The date when the flow displayed in the Flow Process column was performed.
Time The time when the flow displayed in the Flow Process column was performed.
Flow Process The flow processes that have been performed and advanced for this receipt at 
the time of viewing.
If the view icon is highlighted, you can click on the icon to view and print the 
document in PDF format.
If the e-File icon is highlighted, you can click on the icon to view and print the 
e-File or Signature Capture document.
Operator The operator who advanced the flow process.

RECEIVING
Looking Up Receipts in LORE
OPERATIONS 1 GUIDE 4.2 77
If the entire receipt was confirmed in Time-Stamp and Confirm a Receipt (CHRF), then all of the receipt’s Line 
Block lines will display the same Receive Date. This date is the same as was entered in the Receive Date 
field of CHRF when the receipt was confirmed.
If only individual lines of the receipt were confirmed in Confirm Receipts - One Line at a Time (CORL), then 
the confirmed lines will display a date in the Receive Date. This will be the same as was entered in the 
Receive Date field of CORL when the line was confirmed. The receipt lines that have not yet been confirmed 
will have a blank Receive Date field.
OPTIONAL BLOCKS
The LORE Optional Blocks show the same fields and details that appear in the original receipt’s ENRE 
Optional Blocks.
LOOKING UP AN ITEM SUMMARY
The item summary command allows you to look up a summary of all receipt lines by item rather than by 
receipt line. That is to say, if you have multiple receipt lines for the same item, the lines will be consolidated 
into a single line.
1 Retrieve the receipt that you wish to look up.
2 Click on Item Summary.
LORE screen showing item summary
3 When you finish looking up your item summary, click on Receipt Header and Exit to exit.
CHANGING THE DEFAULT SORT SEQUENCE IN LORE
The default sort sequence in LORE is oldest receipt first, then second oldest receipt, followed by third oldest 
receipt, etc. You can change the default sort sequence to show the newest receipts first by means of the Ctrl 
+ A command.
1 Enter LORE.
NOTE Line Block details do not display for deleted receipts.

RECEIVING
Printing the Receiving Documents
2 Query any receipt.
3 Press Ctrl + A. The message “Sequence will be descending” will display in the message area of your 
screen.
4 Perform your query. To retrieve all receipts, leave all query fields blank.
AccellosOne 3PL will retrieve your receipts in descending sequence; that is, newest receipt first, then 
second newest receipt, followed by third newest receipt, etc.
Printing the Receiving Documents
Receipts entered in ENRE may have documents attached to them. Each document is attached to a specific 
flow process that was set up in DIFP. These documents need to be printed before you can proceed to the next 
flow. You print these documents in PRRM (Print Receiving Documents - Specific) or in a batch print through 
PRRE (Print Receiving Documents - All).
PRINTING A DOCUMENT FOR SPECIFIC RECEIPTS IN PRRM
You use PRRM (Print Receiving Documents - Specific) to print the same document for specific receipt 
numbers that have been entered in ENRE. You can print for a single specific receipt (Receipt Number 5 
needs its Tally document printed) or for multiple specific receipts (Receipt Numbers 1, 25 and 46 each need 
their Tally document printed).
PRRM consists of the following sections:
 Header Block
 Receipt Block
 Print Block
The Header Block in PRRM lists all of the receiving documents. If you do not know which document to print at 
this point in the flow process sequence, you can check in LORE. The Document Status field in LORE 
specifies the next document that needs to be printed. The following example shows the steps required to 
process a receipt that has the inbound flow processes ENRE, UNLO and CORE:
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

RECEIVING
Printing the Receiving Documents
OPERATIONS 1 GUIDE 4.2 79
1 Enter PRRM.
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document 
that you wish to print.

PRRM screen showing Header Block with documents
3 Click on Receipt Block.
4 Click on Create Record.
5 Key in the number of the receipt whose attached document you need to print and press Enter.
6 If there are other ENRE receipts that need this same document printed, key in each receipt number and 
press Enter.

PRRM screen showing the Receipt Block
7 Click on Return to Main and then Print Block.
a) Execute Confirm
FLOW 
PROCESS
ATTACHED 
DOCUMENT REQUIRED ACTION
Place your 
cursor next to 
the document 
type that 
needs to be 
printed
The tally document attached to 
receipt numbers 
1149 and 1153 
will be printed

RECEIVING
Printing the Receiving Documents

PRRM screen showing the Printer Block
8 Key in the code of the printer where this document is to print and press Enter. If you do not know the 
code, use the dropdown list.
9 Click Ok. The document will print and the system returns to the Main Menu.
PRINTING A DOCUMENT FOR ALL RECEIPTS IN PRRE
You use PRRE (Print Receiving Documents - All) to print the same document for all ENRE receipts that are at 
the same stage in their flow process and that need this document printed. 
You can also use PRRE to print the same document for all ENRE receipts that meet common criteria and that 
are at the same stage in their flow process. In this case, you use the Query Block to enter the selection 
criteria that the receipts have in common. The system will then call up only these receipts for printing of the 
attached document. For example, if you need to print the tally document for all receipts that were entered on 
June 23rd for Customer A, you would fill in the date and the customer fields accordingly and instruct the 
system to execute the query for these restrictions.
PRRE consists of the following sections:
 Header Block
 Query (Restriction) Block
 Receipt Block
 Print Block
1 Enter PRRE.

RECEIVING
Printing the Receiving Documents
OPERATIONS 1 GUIDE 4.2 81

PRRE screen showing Header Block with documents
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document 
that you wish to print.
3 Click on Query Block.

PRRE screen showing the Query Restriction Block
4 In the Header Block, you selected a document for printing. The Query Restriction Block now provides 
you with two options to print this selected document:
you can instruct the system to retrieve all receipts that are at this step in their flow process
you can instruct the system to retrieve all receipts that are at this step in their flow process and that have 
common criteria
Place the 
cursor next to 
the document that 
needs to be 
printed
A blank Query 
Restriction 
Block and Execute Query 
causes all 
receipts that 
need the 
selected document printed to 
display in the 
Receipt Block. 

RECEIVING
Printing the Receiving Documents
5 Do one of the following:
If you wish to print the 
document in the Header Block 
for all receipts that are at this 
step in their flow process:
If you wish to print the 
document in the Header Block 
for a specific receipt:
If you wish to print the 
document in the Header Block 
for receipts that have common 
criteria:
a) Proceed to step 6. a) Key in the receipt number and 
press Enter.
a) Key in the common selection 
criteria in the corresponding 
field or fields. Use the following table as a guide:
Completing this field …
will print the document selected 
in the Header Block for …
Customer Code all receipts that belong to this customer. 
Shipper Code all receipts that belong to this shipper.
Carrier Code all receipts that belong to this carrier
Receipt Date - Start all receipts that were created in ENRE with 
a Receipt Date starting from the date you 
specify here.
Receipt Date - End all receipts that were created in ENRE with 
a Receipt Date up to the date you specify 
here
Received Date - Start all receipts that were confirmed starting 
from the date that you specify here
Received Date - End all receipts that were confirmed up to the 
date that you specify here
Appointment Date - Start all receipts that have an appointment date 
starting from the date that you specify here. 
This refers to appointments that are set up 
in the Appointment System — appointments scheduled at the warehouse doors 
for pick-up and delivery purposes.
Appointment Date - End all receipts that have an appointment date 
up to the date that you specify here. This 
refers to appointments that are set up in the 
Appointment System — appointments 
scheduled at the warehouse doors for 
pickup and delivery purposes.

RECEIVING
Printing the Receiving Documents
OPERATIONS 1 GUIDE 4.2 83
6 Click on Execute Query. The system displays the Receipt Block where it shows all receipts that meet the 
selection criteria that you specified.

PRRE screen showing the Receipt Block
7 Click on Print Block.
8 Key in the code of the printer where these document are to print and press Enter. If you do not know the 
code, use the dropdown list.
9 Click Ok. The documents will print and the system returns to the Main Menu.
Type all receipts that are of the ENRE Header 
Block receipt type
Priority all receipts that have this priority code
Operator Code all receipts that were entered by the operator that you specify here
EDI Group Value the selected document for all receipts that 
have the same EDI Group Value field that 
you specify here
Completing this field …
will print the document selected 
in the Header Block for …
In this example, clicking 
Print Block will 
print the tally 
document for all 
of the receipts 
that have been 
called up in the 
PRRE Receipt 
Block. 

RECEIVING
Printing the Receiving Documents
CANCELLING OR REPRINTING RECEIPT DOCUMENTS
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
Depending on the document print status, you have the option of cancelling the printing of the document or 
reprinting it as necessary. The following table shows the options that are available depending on the 
document status.
Receipt’s current 
flow process
Document 
attached to this 
flow process
Number of times 
this document has 
been printed
Print status of this 
document

RECEIVING
Printing the Receiving Documents
OPERATIONS 1 GUIDE 4.2 85
CANCELLING RECEIPT DOCUMENTS IN RERE
Cancelling the printing of a document that is attached to a flow process may be necessary if circumstances 
require you to advance to the next flow without printing the document attached to the current flow.
Use the following procedure when the RERE Print Status field indicates “To be printed” and you need to 
reprint the receipt.
1 Enter RERE.
2 Key in the receipt number and press Enter. The system displays the documents that are attached to this 
receipt’s current flow process. 
3 Check that the print status indicates “To be printed”. If there is more than one document, use the arrow 
keys to place the cursor beside the document that you wish to reprint. 
4 Click on Cancel key. Note that the print status indicates “Cancel”. 
PRINT STATUS DESCRIPTION OPTIONS 
All documents have been 
printed.
There are no more documents left to either 
requeue (reprint) or cancel. The receipt has 
been confirmed. All process flows have been 
completed and all documents attached to these 
process flows have been printed.
None. The Help Message Line displays “This 
receipt has no documents to be requeued or 
cancelled.”
To be printed The displayed document(s) has not been 
printed before. It needs to be printed now 
according to the flow process sequence.
To cancel printing of this document, click on 
Cancel. The system will now allow you, in 
CHRF, to proceed to the next flow of the flow 
process sequence.
To print the document, exit RERE. Enter PRRM 
and print the document.
Printed The displayed document has been printed 
before.
Click on Requeue to reprint this document. 

RECEIVING
Printing the Receiving Documents

RERE screen
5 Click on Receipt Number and Exit to exit the program
6 Enter CHRF. Continue confirming the receipt in the usual manner.
REPRINTING RECEIPT DOCUMENTS IN RERE
Reprinting of a document that is attached to a flow process may be necessary if the original was lost or 
destroyed or if a duplicate is required. The system only allows you to reprint document types that have been 
set up in DOCU to allow reprinting.
Use the following procedure when the RERE Print Status field indicates “Printed” and you need to reprint the 
receipt.
1 Enter RERE 
2 Key in the receipt number and press Enter. The system displays the documents that are attached to this 
receipt’s current flow process.
3 Check that the print status indicates “Printed.” If there is more than one document listed, use the up and 
down arrow keys to place the cursor beside the document that you wish to reprint.
Clicking on cancel changes the 
Print Status field 
to Cancel.
Printing of the 
receipt invoice 
document is no 
longer needed to 
advance to the 
next flow in 
CHRF.

RECEIVING
Printing the Receiving Documents
OPERATIONS 1 GUIDE 4.2 87

RERE screen
4 Click on Requeue. Note that the print status indicates “Requeue(d).” This means that you can now reprint 
the selected document.
The tally 
document 
has been 
printed.
Requeue is 
available as 
the reprinting option.

RECEIVING
Printing the Receiving Documents

RERE screen
5 Click on Receipt Number and Exit. 
6 Enter PRRM to reprint the document.
REPRINTING RECEIVING LABELS IN RELA
You use the program RELA (Reprint Labels) to reprint AccellosOne 3PL’s standard receiving label. RELA is a 
general purpose reprint program that is more flexible than PRRM or PRRE. It allows you to reprint labels for a 
specific line of a receipt, to specify the number of copies to be reprinted and to reprint at any flow.
RELA prints one label for each pallet; pallets are defined at the detail line level according to the item’s quantity 
breakdown profile. For example, if your standard quantity breakdown is 10 cases per pallet and your receipt 
line quantity is 35 cases, RELA will print four labels — one for each of the three full pallets and one for the 
partial pallet of five cases.
1 Enter RELA.
2 Key in your document code and press Enter or use your pick list to select it.
3 Key in R for Receipt as your document type.
4 Key in your receipt number and press Enter.
5 Key in your line number and press Enter.
Clicking on 
Requeue 
changes the 
print status 
and the 
receipt 
invoice document is set to 
requeue 
(reprint).

RECEIVING
Confirming a Receipt
OPERATIONS 1 GUIDE 4.2 89

RELA screen
6 In the Number of Labels field, key in the number of extra labels that you require and press Enter.
7 When the Printer Block appears, key in the code of the printer where these labels are to print and press 
Enter. If you do not know the code, use the dropdown list.
8 Click Ok. The labels will print and the system returns to the Main Menu.
Confirming a Receipt
Once a receipt has been entered successfully, the product appears in LOEN (Look Up Entity Information) as 
“On Receipt” In order for the product to be made “Available” — that is, ready to be shipped out of the 
warehouse as part of an order — the receipt must be confirmed 
This is done in the program Time-Stamp and Confirm Receipts (CHRF) where each of the receipt’s flow 
processes is selected and time-stamped individually. The flow processes were previously set up in DIFP as 
either mandatory or non-mandatory. Mandatory flows must be selected and time-stamped in CHRF whereas 
non-mandatory flows are optional and they can be bypassed in CHRF.
ENRE is always the first inbound flow process. The system automatically time-stamps the ENRE flow process 
when you finish entering the receipt. Then you select each of the receipt’s other flows individually in CHRF. As 
you do this, AccellosOne 3PL time-stamps the flow to verify completion of the action and then advances to 
the next flow.
Documents attached to any of the flow processes must also be printed in one of the printing programs before 
the system allows you to proceed to the next flow. Once all of the flows are processed, AccellosOne 3PL 
creates a permanent receipt record and the inventory is available for shipping when needed.

RECEIVING
Confirming a Receipt
The Time-Stamping Block in LORE shows the flows that have been selected, time-stamped and processed to 
date for a specific receipt.
TIME-STAMPING AND CONFIRMING RECEIPTS IN CHRF
Before you can confirm a receipt in CHRF, the following conditions must be met:
 all documents have been printed for the receipt
 all locations have been entered for each receipt line
1 Enter CHRF.
2 Do one of the following:
CHRF screen showing Query Block
NOTE Advancing the flow of a receipt in CHRF is only required in a manual paperbased environment. In RF receiving, the flow is automatically advanced after each 
receipt line is stage and/or put-away.
if you know your receipt number: If you wish to perform a query:
a) Key in your receipt number and 
press Enter.
a) Click on Query Block.
b) Key in your query criteria and 
click on Execute Query.
c) In the Receipts Queried Block, 
use your arrow keys to locate the 
receipt that you wish to confirm.
d) With your cursor positioned over 
the desired receipt, click on 
Accept Receipt.

RECEIVING
Confirming a Receipt
OPERATIONS 1 GUIDE 4.2 91
AccellosOne 3PL will populate the fields in CHRF with the appropriate values for the receipt that you 
entered or selected.
3 The cursor moves to the Next Flow Process Code field. Press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the 
appropriate code and click on Select. If there is only one option in the pick list, it is a mandatory flow process. Click on Select.
If there is more than one option in the pick list, the last selection — the one with the highest sequence 
number — is mandatory. The other options are non-mandatory. You can bypass a non-mandatory process flow by not selecting it in the pick list. Use the up and down arrow keys to move the cursor next to 
the flow process that you wish to select. Then click on Select.

CHRF screen showing the pick list for the Next Flow Process Code field
4 The Receive Date field is for entering the date when the product arrived at the warehouse. The field may 
be blank in which case the system bypasses it and does not allow you to enter the field. Proceed to step 
5.
Depending on your setup, the field may display MM.DD.YY or it may display an actual date. If the field 
displays MM.DD.YY and you do not move the cursor into the field, the field will automatically populate 
with the default date as you continue. The default is the Current Date in your system setup (usually, 
today’s date).
If you need a different Receive Date than the default, press F9 and then press Enter until the cursor is in 
the field. Key in the applicable date and press Enter.
Non-mandatory 
flow process 
option
Mandatory flow 
process option

RECEIVING
Confirming a Receipt
 CHRF screen
5 Click on Select Flow. The CHRF screen becomes blank. 
If the system does not advance to the next flow, see “Troubleshooting Help for Confirming a Receipt” on 
page 93.
Click on 
Select Flow 
will confirm 
the Next Flow 
Process Code 
and advance 
the system to 
the flow process that follows in the sequence. 

RECEIVING
Confirming a Receipt
OPERATIONS 1 GUIDE 4.2 93
6 Continue selecting the next flow and re-entering the receipt number by repeating steps 3 to 5 inclusive 
until you reach your CORE (Confirm Receipt) flow.
7 If you wish to change the receive date on the receipt, press Enter to position your cursor in the Receive 
Date field. Then key in a new date and press Enter.
8 Click on Select Flow.
9 Do one of the following:
TROUBLESHOOTING HELP FOR CONFIRMING A RECEIPT
If you receive any of the following messages in the Help Line, the following actions are required:
There are no more flow sequences for this receipt. 
The receipt has been either confirmed or deleted. Exit CHRF and, if you wish, you may enter LORE to check 
the receipt’s status. See “Looking Up Receipts in LORE” on page 71.
There is at least one more document to print for this receipt. 
1 Click on Exit to exit CHRF.
2 Enter into the program PRRM. Print the document(s) for this flow. See “Printing the Receiving Documents” on page 78.
3 Once the document(s) is printed, return to CHRF. Key in the receipt Number and press Enter. Click on 
Select Flow and continue the procedure for confirming the receipt in the usual manner.
You cannot select this flow since this receipt does not have all locations entered.
1 Click on Exit to exit CHRF. 
2 Enter ENRE.
3 Click on Enter Criteria.
4 Key in the receipt number and click on Execute Query.
5 Click on Line Block.
6 Press Enter until the cursor is in the Location Code field.
If you wish to confirm the 
receipt and exit CHRF:
If you wish to cancel the 
confirmation and exit CHRF 
If you wish to remain in CHRF 
to work on other receipts:
a) Click on Exit. A message will 
appear indicating that the 
receipt is being confirmed.
a) Key in the same receipt number and press Enter.
b) Click on Exit.
a) Key in your next receipt number and press Enter.
b) If required, change the Ship 
date.
c) Click on Select Flow.
d) Repeat the above three steps 
for each additional receipt that 
you wish to confirm.
e) When you finish processing 
your receipts, click on Confirm. A message will appear 
indicating that receipt 1 of xxx 
is being confirmed.

RECEIVING
Confirming a Receipt
7 Key in the Location Code and press Enter. Click on Exit.
8 Enter CHRF. Key in the receipt number and press Enter. Click on Select Flow and continue the procedure for confirming the receipt in the usual manner.
CONFIRMING RECEIPTS ONE LINE AT A TIME IN CORL
You use the program Confirm Receipts - One Line at a Time (CORL) in situations when it is necessary to 
confirm only a specific line(s) of the receipt and not the entire receipt.
The following conditions must be met before you can confirm a receipt line in CORL:
 the line or lines that you wish to confirm must be fully allocated
 the line or lines must be at the flow immediately preceding the flow CORE (Confirm Receipt) unless the 
flow immediately preceding CORE is defined as non-mandatory in DIFP
 all documents attached to any flow before CORE must be printed.
EXAMPLE
If your inbound flows are ENRE, FLOW1, FLOW2, FLOW3 and CORE and if FLOW3 is 
defined as mandatory in DIFP, the line or lines must be at FLOW3. If FLOW3 is not 
mandatory, the line or lines must be at FLOW2.
1 Enter CORL. 
2 Click on Create Record.
3 Key in the receipt number and press Enter.

CORL screen
4 Key in the line number and press Enter twice. “Confirm” displays under the receipt number. 
5 Click on Return to Main.
Confirm 
appears under 
the receipt 
number.
The Receipt 
Date Block displays.

RECEIVING
Confirming a Receipt
OPERATIONS 1 GUIDE 4.2 95
6 Click on Receive Date. The Receive Date is the date when this flow is being confirmed. Press Enter to 
accept the default date as the date you are confirming this flow. The default is the current date of your 
system setup (usually today’s date).
If you need a different Receive Date than the default (for example, you are confirming this flow on a different day than when the receipt was entered), key in the applicable date and press Enter. 

CORL screen showing the Receive Date Block
7 To enter another receipt line that needs to be confirmed, click on Master Block. Click on Create Record 
and repeat steps 3 to 6.
8 When you have finished entering all the lines that need to be confirmed, click on Confirm. A message will 
display on your screen indicating that the line(s) are being confirmed.
CHECKING CONFIRMED LINES IN LORE
You can check that individual lines entered in CORL have been confirmed. Although individual lines of the 
receipt have been confirmed, the receipt’s status will not display as confirmed in LORE. The receipt still has 
remaining lines that have not yet been confirmed. Once all lines are confirmed, then the receipt’s status will 
show as confirmed.
1 Enter LORE. 
2 Key in the receipt number and click on Execute Query.
To confirm 
the lines, you 
must click 
Confirm

RECEIVING
Rating a Receipt in RCRA

LORE screen showing a receipt with line confirmed in CORL
3 Click on Line Block. 
4 Use the up or down arrow keys to scroll to the line that you confirmed in CORL. 
5 If the Receive Date field is completed, you know the line is confirmed. Click on Header Block and Exit to 
exit the program.
If the Receive Date field is blank, the line was not confirmed. Click on Header Block and Exit to exit 
LORE. Enter CORL and re-enter the line.
Rating a Receipt in RCRA
You use the program Receipt Rater (RCRA) to manually rate a receipt. This program calculates all the 
automatic and optional charges that apply to a receipt. 
If your system has been set up to rate receipts automatically, you skip the procedure below. With automatic 
rating, the receipt was rated at the same time that it was confirmed. 
RATING A RECEIPT WITH NO OPTIONAL CHARGES
1 Enter RCRA.
2 Key in the receipt number and press Enter.
Receipt status
The Receive 
Date field 
shows when 
line 2 was confirmed

RECEIVING
Rating a Receipt in RCRA
OPERATIONS 1 GUIDE 4.2 97
3 The cursor will be positioned in the Invoice Date field. The Invoice Date will default to the date when this 
receipt was confirmed (that is, the date entered in the Received Date field in CHRF). If you are rating this 
receipt on the same date as it was confirmed, leave the existing date.
If you are rating this receipt on a different date than when it was confirmed, key in the correct date.
4 If applicable, press F9 (Previous Field) to position the cursor in the Reference Number field and key in 
the reference number.

RCRA screen
5 Click on Rate. The system will display a message indicating that it is rating the receipt.
6 Click on Exit. 
RATING A RECEIPT WITH OPTIONAL CHARGES
A receipt extra charge will appear on the warehouse receipt invoice if your company produces one. If more 
than one receipt extra charge is added to one specific receipt, all of the applied extra charges will be stamped 
with the same receipt number. Receipt extra charges are billed immediately on the warehouse receipt invoice.
NOTE You cannot click on Exit to cancel the rating of the receipt. The Exit command is equivalent to the Rate command.
If there are no other 
charges to add, click on 
Rate.

RECEIVING
Rating a Receipt in RCRA
An accessorial charge will not appear on the warehouse receipt invoice. These charges will be picked up by 
the system and applied as part of batch charges in BILB. Accessorial charges will be billed for later, separate 
from the warehouse receipt invoice.
1 Enter RCRA.
2 Key in the receipt number and press Enter.
3 The cursor is in the Invoice Date field. The Invoice Date will default to the date when this receipt was confirmed (that is, the date entered in the Received Date field in CHRF). If you are rating this receipt on the 
same date as it was confirmed, leave the existing date.
If you are rating this receipt on a different date than when it was confirmed, key in the correct date.
4 If applicable, press F9 (Previous Field) to position the cursor in the Reference Number field and key in 
the reference number.
5 Click on Add Extra Charge.

RCRA screen showing Receipt Extra Charge Flag and Accessorial Charge Flag

RECEIVING
Rating a Receipt in RCRA
OPERATIONS 1 GUIDE 4.2 99
6 Position your cursor over the appropriate field (Receipt Extra Charge Flag or Receipt Accessorial Flag), 
key in Y for Yes and press Enter.
If you wish to apply the charge 
to the receipt header:
If you wish to apply the charge 
to the receipt line:
a) Click on Extra Charge or 
Accessorial Charge.
b) When the Bill Later - Enter 
Charges Block appears, proceed to enter your accessorial 
or receipt extra charge(s). You 
add charges to this screen by 
following the instructions in 
the “Entering Receipt Accessorial Charges” section of the 
Billing and Invoicing Guide.
c) When you finish entering your 
charges, click on Return to 
Main and Exit to exit the Bill 
Later - Enter Charges Block.
a) Click on Receipt Details.
b) Position your cursor over the 
line to which you wish to apply 
the receipt extra charge.
c) Key in Y for Yes and press 
Enter.
d) Click on Extra Charge.
e) When the Bill Later - Enter 
Charges Block appears, proceed to enter your accessorial 
or receipt extra charge(s). You 
add charges to this screen by 
following the instructions in 
the “Entering Receipt Accessorial Charges” section of the 
Billing and Invoicing Guide.
f) When you finish entering your 
charges, click on Return to 
Main and Exit to exit the Bill 
Later - Enter Charges Block.
g) Repeat steps b to f for each 
additional line that you wish to 
apply the receipt extra charge.

RECEIVING
Rating a Receipt in RCRA

RCRA screen
7 If you applied charges to the receipt header in step 6 and now wish to apply charges to the receipt line, 
repeat step 6 for the receipt line charges. Likewise, if you applied charges to the receipt line and now 
wish to apply charges to the receipt header, repeat step 6 for the receipt header charges.
8 When you finish entering your receipt extra charges, click on Exit twice to exit.
You can enter the program Bill Later - Enter Charges (ENAC) to verify that the charges have been applied to 
the receipt.
REQUEUING A RECEIPT FOR RATING IN RERA
You use the program Requeue Receipt for Rating (RERA) if you need to remove the charges that were 
applied to a receipt when it was rated. RERA “un-rates” the receipt — that is, it removes the charges and 
returns the receipt to a status of “Confirm(ed) Receipt, not rated” in LORE. The last point in the invoicing 
process at which you can unrate a receipt depends upon your invoicing type:
 if the receipt charges are on an accessorial invoice, you can run RERA at any time before the accessorial batch is confirmed in ACIN
 if the receipt charges are not on an accessorial invoice, you can run RERA at any time before running 
DLRE (Daily Invoice Register) 
You also use RERA to change the Receipt Type designation that was assigned to a receipt that has already 
been rated and confirmed. For example, you can change the Receipt Type from S (Initial Storage charges 
only) to H (Inbound Handling charges only). See the section “Overriding Generated Charges on a Receipt” in 
the Billing and Invoicing Guide for further details on receipt type designation.
To add receipt 
extra charges to 
specific receipt 
lines, set the flag 
to Y in the 
Receipt Detail 
Block for the 
applicable lines
Accessorial 
Charge field

RECEIVING
Rating a Receipt in RCRA
OPERATIONS 1 GUIDE 4.2 101
The Receipt Type designation can be changed for either the receipt’s Header Block or any of its Line Block 
records. This function will also remove the charges that were applied to the receipt and return the receipt to a 
status of “Confirm(ed) Receipt, not rated” in LORE. 
RERA has two blocks: the Detail Block (the Header Block) and the Line Block.
1 Enter RERA. 
2 Key in the receipt number and press Enter.

RERA screen
3 The system completes the other fields and moves the cursor to the Receipt Type field. If it is necessary 
to change the Header Receipt Type, key in the new code and press Enter. If a change is not necessary to 
the Header Receipt Type, no further action is required for this field.
NOTE When you change the Receipt Type designation in RERA for either the 
Header or the Line Block, the system un-rates the entire receipt.
This Receipt 
Type field will 
change the 
receipt type 
designation of 
the receipt’s 
Header Block

RECEIVING
Rating a Receipt in RCRA
4 There are two command options available: Line Block and Rerate.

RERA screen showing the Line Block
5 If you need to rerate another receipt, key in the next Receipt Number and press Enter. Then repeat steps 
3 and 4.
6 When you finish rerating all applicable receipts, click on Exit.
After you perform the above procedure on a rated receipt, the receipt’s status will show in LORE as “Confirm, 
not rated.” This means that the receipt is confirmed and that the previously applied charges have been 
removed. It is now possible to rate the receipt again with the correct charges. You do this either manually in 
If you do not need to change the 
Receipt Type designation for any 
of the receipt’s Line Block 
records:
If you need to change the Receipt 
Type designation for any of the 
receipt’s Line Block records:
a) Click on Rerate. 
b) The Help Message Line indicates that the system is working. 
Wait while the system completes 
its task. 
c) The screen blanks out the fields, 
which indicates that the entire 
receipt has been un-rated.
a) Click on Line Block.
b) Use the up and down arrow keys 
to move the cursor next to the 
Line Block record that you need 
to change. Check the Current 
Record Counter to ensure that 
you are changing the correct line 
record.
c) Key in the new Receipt Type 
code over the existing one and 
press Enter.
d) Click on Details. The Help Message Line indicates that the system is working. Wait while the 
system completes its task. 
e) The screen blanks out the fields. 
This indicates that the entire 
receipt has been un-rated and 
that the Line Block Receipt Type 
change(s) have also been made.
This Receipt 
Type field will 
change the 
Receipt Type 
designation 
of the 
receipt’s Line 
Block 
records

RECEIVING
Receipt Check-In Receiving
OPERATIONS 1 GUIDE 4.2 103
RCRA or automatically in CHRF, depending on how rating is done for this customer. (In the latter case, 
although you will use the CHRF screen, the system will rate first since the receipt has already been 
confirmed.)
Receipt Check-In Receiving
The Receipt Check-In set of programs allows you to check whether the quantity received in RFCH or RFPU 
of a given receipt matches the quantity expected in ENRE and whether the product has been assigned to a 
final put-away location or has been left in a staging location.
If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE 
flow, AccellosOne 3PL will check for variances in CHRF. If the receipt contains a variance, you will be 
prompted to either accept the variance and confirm the receipt or leave the receipt unconfirmed until the 
variance can be resolved.
SETTING UP RECEIPT CHECK-IN PARAMETERS IN CICP
You set up your receipt check-in parameters in CICP (Check-In Configuration Parameters). In this program, 
you define the following:
 the flow at which you want AccellosOne 3PL to start checking for variances (flows before this flow will 
not be checked)
 the default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIS 
(Receipt Check-In at Staging)
 the default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIR 
(Receipt Check-In Report)
You can define a single set of check-in parameters for all customers by using the .ALL option or you can 
define different check-in parameters for each of your customers.
FIELD DESCRIPTIONS
Customer Code The customer that the receipt check-in parameters apply to or .ALL for all customers if your parameters apply to all customers.
Flow Process Code The flow at which you wish to start checking for variances.
Balance by Inventory 
Level
The default inventory level that you want AccellosOne 3PL to use for calculating variances in RCIS. For example, suppose you receive 10 cases of item A, 
lot 1 and 10 cases of item A, lot 2 in ENRE. When you process the receipt in 
RF, you record 15 cases of lot 1 and 5 cases of lot 2.
If you balance by inventory level 2, your receipt will be out of balance. However, if you balance by inventory level 1, your receipt will be considered balanced.

RECEIVING
Receipt Check-In Receiving
1 Enter CICP.
2 Click on Enter Criteria then Execute Query to see which receipt check-in parameters have been set up. If 
the receipt check-in parameters that you require have not been set up, click on Create Record.
3 In the Customer Code field, key in your customer code and press Enter. If you do not know the customer 
code, you can select it from the pick list. To select a code from a pick list, press F10 to display the pick list 
and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select.
4 In the Flow Process Code field, key in your flow process code and press Enter. If you do not know the 
code, use the pick list to select it.
5 In the Balance by Inventory Level field, key in the appropriate inventory level and press Enter.
6 In the Report by Inventory Level field, key in the appropriate inventory level and press Enter.
7 Add another record to CICP or click on Return to Main to exit create record mode.
CICP screen showing three records
8 Click on Exit to exit.
Report by Inventory Level The default inventory level that you want AccellosOne 3PL to use for reporting 
purposes in RCIR. This value need not be the same as your Balance by 
Inventory Level value.
For example, if you report by level 1, RCIR will show a single line for each 
receipt line. If, on the other hand, you report by level 3, RCIR will show three 
lines for each receipt line; an item total with variances, a lot total with variances (if level 2 = lot) and a pallet ID total with variances (if level 3 = pallet ID).
NOTE Your Report by Inventory Level value should always be less than 
the number of inventory levels used by the customer. For example, if you are 
reporting on a three-level account, you should set this field to 1 or 2. If you set 
this field to 3, the extra lines generated in RCIR will be redundent.
FIELD DESCRIPTIONS

RECEIVING
Receipt Check-In Receiving
OPERATIONS 1 GUIDE 4.2 105
SETTING UP YOUR SPECIAL VERIFY PROGRAM IN DIFP
If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE 
flow and set the Complete flag to Y for Yes, AccellosOne 3PL will check for quantity variances in CHRF. Refer 
to the System Administration Guide for instructions on setting up special verify programs.
DIFP screen showing special verify program RNSL attached to CORE flow with Complete flag set to Y 
for Yes
ACTIVATING RECEIPT VARIANCES IN MRFP
Make sure that the RFCH/RFPU Quantity Must Match the ENRE Quantity flag in MRFP is set to either “Match 
not required” or “Warn if mismatch with ENRE”.
LOOKING UP VARIANCES AND LOCATION STATUSES IN RCIS
You can look up the variance quantity and location status of receipts in RCIS (Receipt Check-In at Staging). 
For each receipt that you query on, RCIS shows the receipt number, customer code, flow code, receipt date, 
gross weight, net weight, expected quantity, received quantity, quantity variance and location status.
When the quantity received in RF matches the quantity expected in ENRE, the quantity variance will show B 
for Balanced followed by the inventory level used to calculate variances; for example, “B-L1”. When the 
quantity received does not match the quantity expected, the quantity variance will show U for Unbalanced 
followed by the inventory level used to calculate variances; for example, “U-L1”.
There are three possible location statuses for a receipt in RCIS: 
 M for missing locations
 S for staging locations assigned
 P for put-away locations assigned 

RECEIVING
Receipt Check-In Receiving
If even one receipt line on a receipt has not been assigned, the location status will be set to M for missing. If 
all receipt lines on a receipt have been assigned and at least one line has been assigned to a staging 
location, the location status will be set to S for staging locations assigned. If all receipt lines on a receipt have 
been assigned to a final put-away location, the location status will be set to P for put-away locations assigned.
There are three possible reporting options in RCIS:
 you can run the Receipt Check-In at Staging Summary report
 you can run the Receipt Check-In at Staging Detail report
 when you look up a receipt in RCIS, AccellosOne 3PL automatically generates a Receipt Check-In at 
Staging Detail Report for that receipt and attaches it to the Time-Stamping Block of LORE where you 
can look it up by clicking on the View icon.
1 Enter RCIS.
RCIS screen showing View Filter
2 Key in your search criteria such as customer code, receipt number range, receipt date range, receipt reference number and probill number.
3 If you wish to override the customer’s balance by inventory level value defined in CICP, key in an override value and press Enter in the Balance by Inventory Level field.
4 If you wish to override the customer’s report by inventory level value defined in CICP, key in an override 
value and press Enter in the Report by Inventory Level field.
5 If you wish to override the default value in the Display Weight in Lbs / Kilos field, key in L for pounds or K
for Kilos and press Enter.
6 When you finish entering your search criteria, click on Execute Query.

RECEIVING
Receipt Check-In Receiving
OPERATIONS 1 GUIDE 4.2 107
RCIS screen showing receipt details and receipt summary
7 If your query retrieves more than a page of records, use your up and down arrow keys to scroll through 
the list of receipts.
8 If you wish to scroll horizontally to see reference and probill number information, press Enter or tab to see 
the additional fields. Press Enter or tab again to suppress the display of reference and probill number 
information.
9 When you finish looking up your variances in RCIS, click on Return and Exit to exit.
PRINTING THE RECEIPT CHECK-IN AT STAGING SUMMARY REPORT
This report shows the receipt number, receipt date, customer code, reference number (if any), expected 
quantity, received quantity, variance quantity, variance status (Balanced or Unbalanced), the inventory level at 
which the variance calculation was made, the location status (Missing, Staging or Put-Away), probill number 
(if any) and flow process for each receipt reported on.

RECEIVING
Receipt Check-In Receiving
1 Enter RCIS.
2 Retrieve the receipts that you wish to report on.
3 Click on Receipt Check-In at Staging Summary Report.
4 Select your printer from the Printer Code dropdown list and click Ok.
PRINTING THE RECEIPT CHECK-IN AT STAGING DETAIL REPORT
In addition to the information shown in the summary version of the report, this report shows the level 1, level 
2, level 2 description, line number, expected quantity, received quantity, pending quantity, gross weight, net 
weight, location and flow process for each receipt line reported on.
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

RECEIVING
Receipt Check-In Receiving
OPERATIONS 1 GUIDE 4.2 109
1 Enter RCIS.
2 Retrieve the receipts that you wish to report on.
3 Click on Receipt Check-In at Staging Detail Report.
4 Select your printer from the Printer Code dropdown list and click Ok.
LOOKING UP THE RECEIPT CHECK-IN AT STAGING DETAIL REPORT IN LORE
This report is automatically generated and attached to the Time-Stamping Block of LORE in the following 
cases:
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

RECEIVING
Receipt Check-In Receiving
Time Stamping Block showing highlighted View icon
4 Click on View to view and, if required, print the document in PDF format.
5 When you finish looking up the document, click on Master Block and Exit to exit.
CONFIRMING RECEIPTS WITH A VARIANCE IN CHRF
If you attach the special verify program RNSL (Check Receipt Line is not in Staging Location) to your CORE 
flow, AccellosOne 3PL will check for variances in CHRF. If the receipt contains a variance, you will be 
prompted to either accept the variance and confirm the receipt or leave the receipt unconfirmed until the 
variance can be resolved.
When you confirm a receipt in RCIS, AccellosOne 3PL automatically generates the Receipt Check-In at 
Staging Detail Report for that receipt; this report is attached to the Time-Stamping Block of LORE where you 
can look it up by clicking on the View icon.
1 Enter CHRF.
2 Key in your receipt number and press Enter.
3 Press Enter to position your cursor in the Receive Date field. Then press Enter to accept the current date 
as your receive date or key in a new date and press Enter.
4 Click on Select Flow.

RECEIVING
Receipt Check-In Receiving
OPERATIONS 1 GUIDE 4.2 111
CHRF screen showing receipt check-in override options
5 If you wish to override the customer’s balance by inventory level value defined in CICP, key in an override value and press Enter in the Balance by Inventory Level field. If you do not wish to override this 
value, press Enter to bypass the field.
6 If you wish to override the customer’s report by inventory level value defined in CICP, key in an override 
value and press Enter in the Report by Inventory Level field. If you do not wish to override this value, 
press Enter to bypass the field.
7 In the Display Weight in Lbs / Kilos field, key in L for pounds or K for Kilos and press Enter.
CHRF screen showing prompt to accept or reject variance
8 Click on Yes to accept the variance or click on No to leave the receipt unconfirmed.
9 Click on Exit to exit.

RECEIVING
Receipt Check-In Receiving

OPERATIONS 1 GUIDE 4.2 113
INVENTORY MAINTENANCE AND 
ADJUSTMENTS
Looking Up Inventory Information in LOEN ................................................. 114
Looking Up Locations in LOLO ..................................................................... 136
Entering Adjustments to Inventory Amounts............................................... 140
Relocating Inventory....................................................................................... 159
Entering Hold Adjustments............................................................................ 169
Adjusting Inventory Details............................................................................ 186
Reversing a Document’s Flow in RVDF ........................................................ 197

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
Looking Up Inventory Information in LOEN
The program Look Up Entity Information (LOEN) allows you to view details of all inventory that is stored in the 
warehouse. LOEN allows you to view all transactions that have been processed for this product. You can also 
view the locations where the product is stored and the amounts in each location.
Inventory setup in AccellosOne 3PL uses levels to identify product. Inventory levels are the various identifiable characteristics of an item. Some examples of inventory levels are: Lot Number, Pallet Identification 
Number, Expiry Date and Color. Customers can be set up with up to four inventory levels and each level may 
also have an optional description field. 
An item together with any of its inventory level combinations is called an inventory entity. For example, Item A, 
Lot Number 100 is one entity and Item A, Lot Number 200 is another entity.
The following are examples of possible inventory level setups for an entity:
Entity Level Setup
Description 
(Optional)
The product item is all the same model and color. It therefore requires a one- level setup.Level 1: Item 123 AA Printer Model BB
The product item is all the same model but it has various 
colors. It therefore requires a two-level setup.
Level 1: Item 456
Level 2: Color 
BB Telephone Model C
The product item has different lot numbers and expiry 
dates. It therefore requires a three-level setup.
Level 1: Item 789
Level 2: Lot: 001
Level 3: Expiry Date:
 Mar.16.99
Sweet Peas

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 115

LOEN screen showing the Inventory Block
The LOEN program is made up of the following parts:
 Inventory Block
 Drill Block (only available for inventory with more than one inventory level)
 History Block
 History Details Block
 Location Block 
 Renewal Block
The LOEN program provides inventory entity details such as:
 product availability, that is the number of units that are available, on hand, on order, or on receipt for 
each inventory level for your customers
 the location where the inventory entity is stored
 the inventory entity’s history (which receipts, orders and adjustments have been performed on the 
entity)
 history time-stamping activity, i.e. who performed the stamped activity and when
 the last billing renewal date and the next renewal date
Once a receipt has been created in ENRE, the product shows in LOEN as inventory that is “On Receipt”.’ 
After the same receipt has been confirmed, the same product shows in LOEN as inventory that is “On Hand.”
The following diagram shows the various blocks in LOEN.
Inventory levels 1 and 2 and 
their attached 
optional 
descriptions

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
THE INVENTORY BLOCK AND QUERYING IN LOEN
In the Inventory Block of LOEN, you enter the selection criteria for the inventory records that you want to view. 
You can query by:
customer only Completing only the customer code will retrieve all items owned by this 
selected customer. All Inventory Level One (Item) products will display along 
with all of their other inventory level combinations — their related entities.
item Completing the customer code and the item code will retrieve the selected 
item and all of its related entities. The selected Level One plus all of its Level 
2, 3, and higher inventory level combinations will display.
Header Block
History Block
History
Details Block
Location
Block
Renewal
Block
This block shows the locations
where the inventory in the Header
Block is stored.
EXAMPLE
Location A100 15 CASES
Location A101 10 CASES
Location A102 0 CASES
This block shows the last
renewal date and the next
renewal date for the product in
the Header Block. For each
location billing code, the
Renewal Block shows the
location billing code, total
number of units, gross weight
and net weight.
EXAMPLE
LOCATION BILL CODE UNITS
ALL 10 PLT
COOL 4 PLT
This block shows each transaction
performed for the inventory in the
Header Block.
EXAMPLE
ER (Enter Receipt) 10 UNITS
CR (Confirm Receipt) 10 UNITS
A (Adjustment) 3 UNITS
EO (Enter Order) -5 UNITS
This block shows the
operator who performed
the transaction in the
History Block.
EXAMPLE
JOHN DOE 10:30AM
This block shows the
inventory that you are
looking up.
EXAMPLE
Item A1
Lot 101
Pallet ID 123

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 117
When you enter the customer code and any additional inventory levels that you wish to query on, the 
Inventory Block displays an entity broken down into its component inventory levels. All of the other LOEN 
blocks for this record refer to this entity. However, when you query on an inventory level (for example, Lot X) 
without specifying a customer, the system will display every entity or customer that has a Lot X. 

LOEN screen showing the Inventory Block
LOOKING UP ALL INVENTORY ENTITIES FOR A SPECIFIC CUSTOMER 
The following procedure allows you to view all inventory entities that a specific customer has in the system. 
All of the customer’s items 
(Level 1) will display along with any of their other inventory level combinations. LOEN will display a separate 
record for each entity.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
inventory level 
(level 2 and higher)
For product with more than one inventory level and with several entities under 
that level, you can query on its Inventory Level 2 and higher levels. Completing the customer code, item code and Inventory Level fields up to and including the one that you want to query on will display all entities for the selected 
inventory level. For example, if you query on a specific Inventory Level 3, all of 
its entities will display. The information will display in the Drill Block. 
specific entity Completing the customer code, item code and all displayed inventory level 
fields will retrieve only the record for the selected entity (for example, CUST1, 
ITEM1, Lot 100, Color: Blue).
All details provided 
in the other LOEN 
blocks apply to the 
entity displayed in 
the Inventory 
Block

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
2 To view all entities for this customer, key in the customer code. If you do not know the code, use the pick 
list. Click on Execute Query.
3 Click on Location Block to display the locations where this product is currently stored. If necessary, use 
the up and down arrow keys to scroll through the locations.

LOEN showing the Inventory and Location Blocks
4 Use the function key buttons to access and view this entity’s details in the History, History Details, 
Renewal and Drill Blocks. These blocks are explained later in this section.
5 Click on Inventory Block. If you want to view the details of another entity for this customer, check the current record counter. If there is more than one record, use the down arrow key to scroll to the next record. 
If you wish to view the inventory of another customer, click on Enter Criteria. Key in the customer code or 
use the pick list.
If you wish to exit the program, click on Return to Main.
LOOKING UP ALL INVENTORY ENTITIES FOR A SPECIFIC ITEM 
The following procedure allows you to view all inventory combinations (all entities) for one selected item.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
2 Key in the customer code and press Enter. If you do not know the customer code, use the pick list.
3 Key in the item code.
Use the buttons 
to access the 
other LOEN 
Blocks

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 119

LOEN showing the Inventory and Drill Blocks
4 Click on Execute Query.
5 If a Drill Block does not display, use the function key buttons to access and view the details in the Location, History, History Details and Renewal blocks. (These blocks are explained later in this section.) 
Then, click on Inventory Block and Exit and skip the remainder of the procedure.
If there is a Drill Block, continue with the remainder of the procedure.
6 You must view the detail blocks separately for each entity that is displayed in the Drill Block. In the Drill 
Block, use the up and down arrow keys to place the cursor next to the entity whose details you wish to 
view. 
Then use the function key buttons to access and view the details in the Location, History, History Details 
and Renewal blocks. These blocks are explained later in this section.
7 When you have finished viewing this entity’s details, click on Drill Block. 
If you wish to view another entity’s details, use the up and down arrow keys to place the cursor next to 
the entity whose details you wish to view and use the function key buttons to view its details.
8 When you have finished viewing all of the entities in the Drill Block that you needed to see, click on 
Inventory Block. 
If you wish to view another item or the inventory of another customer, click on Enter Criteria.
If you wish to exit the program, click on Return to Main.
LOOKING UP A SPECIFIC ENTITY
The following procedure will display the inventory for one selected entity.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
A query is made 
on Item D3
Item D3’s other 
inventory levels 
(lot and PID) display in the Drill 
Block

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
2 Key in the Customer Code and click on Enter. If you do not know the Customer Code, use the pick list.
3 Key in the Item Code and press Enter.
4 In each Inventory Level field that displays, key in the corresponding codes for the entity and press Enter.
5 Click on Execute Query.
6 Click on Location Block to display the locations where this product is currently stored. If necessary, use 
the up and down arrow keys to scroll through the locations.
7 Use the function key buttons to access and view this entity’s details in the History, History Details and 
Renewal and Blocks. These blocks are explained later in this section.
8 Click on Inventory Block. 
9 If you want to view another record, click on Enter Criteria.
10 If you wish to exit the program, click on Return to Main.
LOOKING UP ALL ENTITIES FOR A SPECIFIC INVENTORY LEVEL 
With the following procedure, you can query on any specific inventory level that is Level 2 or higher. The 
inventory level that you query on must also have several entities under that level. For example, if you are 
querying on Lot Number, there must be more than one lot number for this entity (Lot # 101, Lot # 102, Lot # 
103, etc.) 
The results of your query will display in the Drill Block. You can use the following procedure to restrict the 
records that are retrieved into the Drill Block.
1 Enter LOEN. You are in the Inventory Block.
2 Key in the item code and press Enter. The entity’s other inventory level fields will display for completion. 
3 Key in the applicable data for the inventory levels that you want to query on. 
To view details for all of an item’s inventory levels, key in the item code and click on Execute Query. The 
Drill Block will display details for all of the remaining levels. For example, an entity that has three inventory levels — Item, Lot Number and Color — would display all of the item’s entities with all Lot Number 
and Color combinations in the Drill Block.
To view details for an item’s specific Level 2 entities, key in the item code and the specific data that you 
want to query on in Inventory Level 2. Click on Execute Query. The Drill Block will display the specified 
Inventory Level 2’s details for all of the remaining levels. In our example, all of the item’s PID records will 
display in the Drill Block for the specific lot number that you queried on.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 121

LOEN screen showing the selection criteria in the Inventory Block

LOEN screen showing the Drill Block
4 Use the function key buttons to access and view the details in the History, History Details, Renewal and 
Drill Blocks. These blocks are explained later in this section.
5 Click on Inventory Block. If you wish to view another entity or customer, click on Enter Criteria. 
If you wish to exit the program, click on Return to Main.
Executing this 
query will display all Customer D’s Item 
D3’s entities
All level 2 (lot) 
and level 3 
(PID) entities 
display for item 
D3

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
LOOKING UP ALL INVENTORY LEVEL CODES STARTING WITH A PREFIX
The following procedure allows you to view all records of an item that start with the prefix that you are 
searching for.
1 Enter LOEN. The system will be in the Enter Criteria Mode.
2 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
3 Key in the inventory levels in the normal manner until you reach the Inventory Level field that you wish to 
search by. Key in the prefix you are looking for followed by % (e.g. 32%). 
4 Click on Execute Query. The system displays all of the codes that begin with 32 for the selected Inventory Level. If there is more than one record that meets this criteria, then the information will display in the 
Drill Block.
5 Use the function key options to access and view the details in the History, History Details and Renewal 
Blocks. These blocks are explained later in this section.
If there is a Drill Block, first use the up and down arrow keys to place the cursor next to the entity whose 
details you wish to view. Then use the function key options to access and view the details in the History, 
History Details and Renewal Blocks.
6 Click on Inventory Block. 
7 If you want to view other records, click on Enter Criteria. If you wish to exit the program, click on Return 
to Main.
DRILL BLOCK
The Drill Block only displays if all of the following criteria are met:
 the entity has more than one inventory level, that is, it has Inventory Level 2 and possibly more levels 
 the inventory level that you are querying on (Level 2 or higher) has more than one record. For example, 
if you are querying on the inventory level lot number, there must be more than one lot for this entity (Lot 
# 101, Lot # 102, Lot # 103, etc.).
Inventory records in the Drill Block are sequenced according to the value that you selected in the FIFO/LIFO 
Based on field in PIPR (Picking Profile). There are five possible options in this field: receipt date, expiry date, 
inventory level 2, inventory level 3 and inventory level 4.
When you have multiple records for the same receipt date/expiry date/level 2, etc., AccellosOne 3PL will sort 
the records in ascending alphanumeric sequence. This means that even if you enter numbers as your level 2 
value — for example, lot number — the system will treat these numbers as alphanumeric characters and sort 
them accordingly. As a result, your lots may appear to be out of sequence when you look up inventory in 
LOEN, perform allocation or run reports.
EXAMPLE
If you receive item A1, lot 1001 and item A1, lot 9, the two inventory entities will be sorted in ascending alphanumeric order as follows:
1001
9
Lot 1001 will be listed before lot 9 because 1 is less than 9.
In order to avoid this sort sequence, you must define a fixed length for all your lots numbers and add leading 
zeros to all lot numbers that are less than the fixed length. For example, if the fixed length of your lot number 
is five characters and you are receiving lot # 6, you must enter 00006 — not 6.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 123

LOEN screen showing lot 107 listed before lot 9
FIELD DESCRIPTIONS
Level 2 The item’s inventory level 2 data.
Level 3 The item’s inventory level 3 data.
Available Indicates the number of units of this entity that are in the warehouse for filling 
orders. See the “Available” field in the Location Block for the available formula. 
On Hand The total units of this entity that are Available, On Order and On Hold.
It would be necessary to remove units On Order from an unconfirmed order 
before they are actually available for shipping out. It would be necessary to 
remove the hold from units with non-shippable hold codes before they are 
actually available for shipping out.
On Order Indicates the number of units of this entity that are currently allocated to an 
unconfirmed order. Once the order is confirmed, the number will be subtracted 
from the On Hand Total.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
LOCATION BLOCK
The Location Block shows product availability. It lists the locations in which the entity is currently stored and it 
provides a breakdown of the amount stored in each location. It also shows if any of this entity is on hold, onorder, in-transit or being replenished.
On Receipt Indicates the number of units of this entity that have arrived at the warehouse 
and have had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the receipt is confirmed, the product amount will move from 
the “On Receipt” column to the “On Hand” and “Available” columns.
Quantity Breakdown 
Setup
The entity’s quantity breakdown.
Conveyance Reserved for future use.
In-Transit The amount of this entity that is on its way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. 
For example, the pick location will show -10 cases and the bulk location will 
show 10 cases. Once the replenishment request has been processed and this 
amount is moved from the bulk location to the pick location, the replenishment 
amount for both locations will be zero and the Available amounts for each 
location will adjust accordingly as in the example below.
Before processing of the replenishment request:
LocationAvailableReplenishment
Bulk A1000 Cases 10 Cases
Pick A1 Case-10 Cases
After processing of the replenishment request:
LocationAvailableReplenishment
Bulk A990 Cases0 Cases
Pick A11 Cases0 Cases
NOTE A negative quantity in the Replenishment column indicates that 
product is being added to the location.
NOTE If the amounts in the On Order and the Available fields do not equal the total 
in the On Hand field, this could mean that some units are on a non-shippable Hold. 
Therefore, they are On Hand in the warehouse but are not available to be allocated to 
an order for shipping. Units that are On Hold display in the Location Block.
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 125
If all quantities in a given location equal zero, this means that the product used to be in the location but no 
longer is. For example, if you move all product in location A100 to location A101, the available, on-hand, on 
order, on receipt, in-transit and replenishment quantities for location A100 will be set to zero.

LOEN showing the Location Block details
NOTE The fields in the Location Block continue to the right of what initially displays 
on the screen. Press Enter once to view the In-transit and Replenishment columns. 
Use the tab key to toggle between these columns and the On Order and On Receipt 
columns.
Totals for 
each of the 
corresponding 
columns 
above

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN

LOEN screen showing the Location Block details
In the Location Block, you can choose to view either all locations for the entity you have selected or only the 
non-zero locations. This is useful when you have a large number of locations and you need to see only those 
locations with a balance.
8 Enter the Location Block of LOEN. The block displays all of the locations for the entity that you are querying on. Press CTRL + A to toggle between the following messages at the bottom of your screen: “Will 
query all locations” and “Will query only non-zero locations.”
9 When the message “Will query only non-zero locations” displays, click on Drill Block to exit the Location 
Block.
10 Click on Location Block to return to the Location Block. The Location Block will display only non-zero 
locations for the selected entity.
FIELD DESCRIPTIONS
Warehouse The Warehouse Code where the entity is stored. 
An * in the Warehouse and Location Columns is a temporary repository where the system places units that have been assigned to an order or to a receipt but that have not 
yet been assigned a location. 
Press the tab 
key to toggle 
between the hidden columns 
and the On 
Order and On 
Receipt columns

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 127
Location The Location Code where the entity is stored.
A Location Code with zero units (for example, location A101 in the preceding screen 
capture) indicates that this entity was stored here before. The entity has since been 
removed because of relocation, filling an order or an adjustment. If you need further 
details about this location’s transactions, go into the History Block.
Hold Indicates the type of Hold Code.
Available Indicates the number of units of this entity that is available in the warehouse for filling 
orders. The formula for calculating this value is as follows:
Available = On Hand - On Order - On Hold
If the available quantity is a negative, the product belongs to a reserve logic customer.
On Hand The total number of units that are Available, On Order and On Hold. 
It would be necessary to remove units On Order from an unconfirmed order before they 
are actually available for shipping out. It would be necessary to remove the hold from 
units with non-shippable hold codes before they are actually available for shipping out.
On Order Indicates the number of units that are currently allocated to an unconfirmed order. 
Once the order is confirmed, the number will be subtracted from the Available Total.
On Receipt Indicates the number of units of this entity that have arrived at the warehouse and have 
had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the 
receipt is confirmed, the product will move from the “On Receipt” column to the “On 
Hand” column.
Conv. Reserved for future use.
In-Transit The number of units for this entity that are on their way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. For example, the pick location will show -10 cases and the bulk location will show 10 cases. 
Once the replenishment request has been processed and this amount is moved from 
the bulk location to the pick location, the replenishment amount for both locations will 
be zero and the Available amounts for each location will adjust accordingly as in the 
example below.
Before processing of the replenishment request:
Location
Bulk A
Pick A
Available
1000 Cases
1 Case
Replenishment
10 Cases
-10 Cases
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
HISTORY BLOCK
The History Block allows you to trace all inventory movement for a particular entity from when it was first 
entered into the system until the present. You can see everything that was done to the inventory. 
The first and second lines along the top of the History Block are headings. The other lines are individual transaction records.
Inventory transactions display as: 
 inventory received into the warehouse (a receipt) 
 inventory shipped out of the warehouse (an order) 
 inventory record that has been corrected (an adjustment)
 inventory placed on hold (a hold)
After processing of the replenishment request:
Location
Bulk A
Pick A
Available
990 Cases
11 Case
Replenishment
0 Cases
0 Cases
NOTE A negative quantity in the Replenishment column indicates that product is 
being added to the location.
Total The total inventory amount for the corresponding column above.
Quantity Breakdown 
Setup
The entity’s quantity breakdown.
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 129

LOEN screen showing History Block
When viewing all details in the History Block, you can arrange the data in either ascending or descending 
order by date by using the following procedure.
1 Press Ctrl + A. The Help Message Line will indicate “Sequence will be descending.” 
2 Click on Enter Criteria and Execute Query and the data will display in descending order by date.
3 Press Ctrl + A. The Help Message Line will indicate “Sequence will be ascending.” 
4 Click on Enter Criteria and Execute Query and the data will display in ascending order by date.
To query in the History Block for specific information use the following procedure.
5 Enter the History Block.
6 Click on Enter Criteria.
7 Press Enter until the cursor is in the field that you wish to query on and key in your query. For example, if 
you want to query on Document # 4, press Enter until the cursor is in the Document # field and key in 4.
NOTE The Weight column changes from Gross Weight to Net Weight or vice versa 
when the cursor is in the History Block and you press Enter.
A hold transaction
A confirmed 
receipt transaction

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
8 Click on Execute Query and the information for Document 4 will display. 
FIELD DESCRIPTIONS
Transaction Date The date that the activity took place.
(Transaction) Type The type of activity. The acronyms used stand for:
A (Adjustment)
the inventory was adjusted in ENAJ
BF (Brought Forward)
inventory balances were brought forward after inventory was purged in PURG
CO (Confirmed Order)
the inventory was shipped on a confirmed order
CR (Confirmed Receipt)
the inventory was received on a confirmed receipt
EO (Entered Order)
the inventory is on an open order
ER (Entered Receipt)
the inventory is on an open receipt
HL (Hold Adjustment)
the inventory was placed on hold
IF (Information Only)
the inventory’s weight was adjusted or the level 2 description, expiry date, 
item value, etc. was modified in CHEI
OM (Order Move)
The inventory was moved as a result of an order move. An order move is a 
manual movement of inventory that occurs when product on an outbound 
order is moved from an assigned picking location to any other location (usually 
but not always an outbound staging or dock location). Order moves typically 
require an RF program.
PD (Proof of Delivery)
the inventory was shipped and then returned to the warehouse using POD
RL (Relocation)
the inventory was relocated in RELO or MARL
Document # The receipt, order or adjustment number assigned to this transaction.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 131
HISTORY DETAILS BLOCK
If the History Details Block option appears at the bottom of your screen, you may enter this block for more 
information about the transaction. It provides new information about the transaction: the time it was 
completed, the operator who performed it and the number of item lines involved.
If the transaction is related to an order, you can click on LOOR Block to look up the order. If the transaction is 
related to a receipt, you can click on LORE Block to look up the receipt.
Units The number of units involved in this order, receipt or adjustment.
Weight Gross/ Weight 
Net
The total gross and net weight involved in the transaction.
Hold The hold code that has been placed on this entity. 
Carrier Name The name of the carrier.
Shipper/Consignee/ReasonThe name of the shipper or consignee involved in the transaction or the reason for the adjustment.
Audit # The audit number for this transaction.
EDI # The EDI number for this transaction.
Reference # 1 The first customer-defined reference number that refers to the inventory, if 
applicable.
Reference # 2 The second customer-defined reference number that refers to the inventory, if 
applicable.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN

LOEN screen showing the History Details Block
FIELD DESCRIPTIONS
Time The time the transaction was entered into the system.
Operator The operator who entered the transaction into the system.
Type The transaction type. See “History Block” on page 128.
Document # The receipt, order or adjustment number assigned to this transaction.
Line The Line Block Line Number from ENRE in which the item involved in the 
transaction was first entered.
Units The number of units involved in the transaction.
Conv. Reserved for future use.
Hold The type of hold code placed on the item.
Whse The warehouse where this item is stored.
Location The location where this item is stored.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 133
HISTORY REMARKS BLOCK 
If you are in the History Details Block and you see the History Remarks Block button displayed as an option in 
the Help Message Line at the bottom of your screen, click on the button to view the Remark entries. This 
shows internal warehouse remarks that were entered by you or other operators to explain various activities 
that were performed on the selected inventory.

LOEN screen showing the History Remarks Block
RENEWAL BLOCK
This block shows the history of renewal transactions for storage of the inventory items.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.
FIELD DESCRIPTIONS
The History 
Remarks 
Block contains explanatory 
information 
regarding a 
transaction 
that was performed on the 
selected item

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN

LOEN screen showing the Renewal Block
FIELD DESCRIPTIONS
Period Number The number of times the inventory has been renewed for storage.
Next Renewal Date The date when storage of this entity needs to be renewed and charged again.
Last Renewal Date The date when the current storage period began.
Loc. Bill The location billing code of the location where the inventory item is stored.
Units The number of inventory units for which renewal storage is being charged.
Gross Weight The gross weight of inventory units for which renewal storage is being 
charged.
Net Weight The net weight of inventory units for which renewal storage is being charged.
Conv. Qty Reserved for future use.
Quantity Breakdown 
Setup
The inventory item’s quantity breakdown setup.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Inventory Information in LOEN
OPERATIONS 1 GUIDE 4.2 135
LOOKING UP INVENTORY BY ALTERNATE TYPE CODE AND ALTERNATE ITEM 
CODE
You can look up inventory by alternate type code and/or alternate item code if these values have been 
defined in ALIT (Alternate Item and Language) for a particular item.
1 Enter LOEN.
2 Key in your customer code and press Enter.
3 In the Item field, key in ! followed by your alternate type code or alternate item code.
You can look up inventory by both alternate type code and alternate item code by entering both values. 
For example, if your alternate type code were BX1 and your alternate item code were ALT_ITEM, you 
would key in !BX1!ALT_ITEM.

LOEN screen showing alternate item code ALT_ITEM
4 Click on Execute Query.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Locations in LOLO

LOEN screen showing all inventory records for ALT_ITEM (equals D3)
5 When you finish looking up your inventory, click on Inventory and Exit to exit.
Looking Up Locations in LOLO
You use the program Look Up Location Information (LOLO) to view details of warehouse locations, the 
inventory that they contain and the amount of space that is still available for storing incoming product. 
LOLO has two blocks: the Location Block and the Inventory Block.
1 Enter LOLO.
2 If you want to view data for all locations, click on Enter Criteria and Execute Query. Use the up and down 
pointer keys to scroll through the locations. 
If you are looking for a specific location, key in the warehouse code and press Enter. Then key in the 
location code and click on Execute Query.
You can also query by capacity SKU code, % SKU utilized, maximum SKU capacity, isolator code and 
location type code.
3 Click on Inventory Block. The details of the inventory contained in this location will display. 

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Locations in LOLO
OPERATIONS 1 GUIDE 4.2 137

LOLO screen
4 If the current record indicator shows that there is more than one entity in this location, use the up and 
down pointer keys to scroll through the entities. 
5 Click on Location.
6 If you want to view another location and its details, click on Enter Criteria and repeat the procedure. To 
exit the program, click on Location and Exit.
NOTE When you are in the Location Block, the Inventory Block button will only 
appear if there is inventory in the location. If there is no inventory in the location, the 
Inventory Block button will be blank.
Location 
Code 
A103 contains four 
entities

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Locations in LOLO
LOCATION BLOCK
INVENTORY BLOCK
FIELD DESCRIPTIONS
Warehouse Code The Warehouse Code.
Location Code The Location Code.
Capacity SKU Code The SKU type that is used to measure the location’s capacity.
% SKU Utilized Percentage of the location that is full.
Maximum SKU Capacity The maximum number of SKU’s that can fit into this location.
Isolator Code The code that indicates the location’s isolation type for storing product that 
needs to be separated from other product. If it is not an isolation type of location, the code will be N/A (for Not Applicable).
Location Type Code The location type code assigned to the location.
FIELD DESCRIPTIONS
Customer Code The code of the product owner.
Item Code The code for the item.
Inventory Levels The inventory levels of the item.
Hold Code The hold type code attached to product in this location.
Available Indicates the number of units of this entity that is available in the warehouse for filling 
orders. 
On Hand Indicates the number of units of this entity that is in the warehouse. It is the total for this 
entity of all units that are Available, On Order and On Hold.
It would be necessary to remove units On Order from an unconfirmed order before they 
are actually available for shipping out. It would be necessary to remove the hold from 
units with non-shippable hold codes before they are actually available for shipping out.
On Order Indicates the number of units of this entity that is currently allocated to an unconfirmed 
order. Once the order is confirmed, the number will be subtracted from the Available 
Total.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Looking Up Locations in LOLO
OPERATIONS 1 GUIDE 4.2 139
On Receipt Indicates the number of units of this entity that has arrived at the warehouse and has 
had a receipt created in ENRE, but the receipt has not been confirmed yet. Once the 
receipt is confirmed, the product will move from the “On Receipt” column to the “On 
Hand” column.
In-Transit Indicates the number of units of this entity that is on its way to the warehouse.
Replenishment The amount of this entity that has been requested to replenish the pick line. For example, the pick location will show -10 cases and the bulk location will show 10 cases. 
Once the replenishment request has been processed and this amount is moved from 
the bulk location to the pick location, the replenishment amount for both locations will 
be zero and the Available amounts for each location will adjust accordingly as in the 
example below.
Before processing of the replenishment request:
Location
Bulk A
Pick A
Available
1000 Cases
1 Case
Replenishment
10 Cases
-10 cases
After processing of the replenishment request:
Location
Bulk A
Pick A
Available
990 Cases
11 Case
Replenishment
0 Cases
0 cases
NOTE A negative quantity in the Replenishment column indicates that product is 
being added to the location.
Quantity The total quantity corresponding to each of the above columns: On Hand, On Order, 
On Receipt, In-Transit and Replenishment.
SKU Capacity % The percentage of this location’s SKU capacity that is occupied for each of the above 
columns: On Hand, On Order, On Receipt, In-Transit and Replenishment.
Weight Capacity % Only displays if you press tab key
The percentage of this location’s weight capacity that is occupied for each of the above 
columns: On Hand, On Order, On Receipt, In-Transit and Replenishment. Weight 
capacity requires a value in the Weight Limit field of LOCA.
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
Entering Adjustments to Inventory Amounts
You use the program Inventory Adjustments (ENAJ) to correct errors in current warehouse inventory records. 
Transactions made in ENAJ are corrections to internal inventory records and therefore they do not involve 
any charges. In instances where the type of adjustment code does require a charge, the Bill Later - Enter 
Charges (ENAC) screen appears for completion during the procedure.
There are four types of inventory adjustments that you can perform in AccellosOne 3PL:
 positive adjustments in which you add inventory to the current recorded amount
 negative adjustments in which you subtract inventory from the current recorded amount
 transfer adjustments in which you subtract inventory currently recorded under one customer code/level 
1 value/level 2 value and add it to another customer code/level 1 value/level 2 value
 positive adjustments in which you create new inventory
QUERYING IN ENAJ
When you enter ENAJ, you need to instruct the system as to which entity you need to adjust. ENAJ allows 
you to do this by querying on customer and/or on the item’s inventory levels:
 if you complete the Customer field, all of the customer’s inventory records will display when you click on 
Execute Query
 if you complete the Inventory Level 1 field, all of this item’s records will display 
 if you complete the Customer field, the Inventory Level 1 field (ITEM) and the Inventory Level 2 field (for 
example Lot Number), all records with this lot number will display when you click on Execute Query
The more information that you enter, the fewer the records that you will have to search through.
Cube Capacity % Only displays if you press tab key
The percentage of this location’s cube capacity that is occupied for each of the above 
columns: On Hand, On Order, On Receipt, In-Transit and Replenishment.
FIELD DESCRIPTIONS

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 141

ENAJ screen
QUERYING IN ENAJ BY PROCESS VALUE
If the item that you are looking up has a process code (IPRO) attached to it, you can query by process code 
and process value.
1 Enter ENAJ.
2 Press Enter to bypass the Customer Code and Level 1/2/3/4 fields.
ENAJ screen showing prompt for process code and process value
Complete 
as many of 
the inventory levels 
as possible

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
3 When prompted for the process code and value, key in your process code and press Enter. Then key in 
your process value and click on Execute Query.
ENTERING A POSITIVE ADJUSTMENT IN ENAJ
You enter a positive adjustment in ENAJ to make inventory corrections that add product to the system 
records. 
1 Enter ENAJ. The program will be in the Enter Criteria Mode.
2 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels and press Enter. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the amount and the SKU of the entity that you wish to add and press Enter. If you do not enter a 
SKU, AccellosOne 3PL will use the item’s lowest SKU.
The system automatically updates the weight-related fields for standard weight items. For items of nonstandard weight, you will be required to key in the weight data in the corresponding fields.

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date 
field. 
If this entity has an expiry date or is part of an open lot, the system will automatically populate the corresponding fields.
Key in the 
amount that 
you are adding to inventory. Specify 
the SKU.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 143
9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know 
the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. Information 
from this field will print on the Adjustment Audit Report.

ENAJ screen
11 Click on Location Block. The Location Block displays the locations where this entity is currently stored 
and the amounts in each location.
Complete the 
adjustment 
code and 
adjustment 
reason fields.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts

ENAJ screen showing the Location Block
12 Use the up and down arrow keys to move the cursor next to the location where you will be adding the 
inventory. 
If you need to add the product to a location that is not listed, click on Create Record and then use the pick 
list to select a location.
Press Enter until the cursor is in the Adjust (From) Column. Key in the amount and SKU that you are adding to this location. Press Enter. 
If you are adding to more than one location, move your cursor to the next location where you will be adding inventory (for example, if you are adjusting ten cases and you place five cases in one location and the 
remaining five cases in a second location). Repeat until the proof is zero.
Check the Proof 
Box amount.
Set the cursor 
next to the 
Location Line 
where you will 
be adding the 
quantity that you 
are adjusting.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 145

ENAJ screen showing the Location Block
13 Click on Process Adjustment.

ENAJ screen showing the Remarks Block
14 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
15 When you finish entering your remarks, click on Return. A message will display providing the number of 
the adjustment record.
16 If prompted to enter a charge for the transaction, click on Exit.
Press Enter across 
the Location Line 
until you are in the 
Adjust Column. Key 
in the amount that 
you will be adding to 
this location.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
17 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit ENAJ.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the Adjustment 
record.
ENTERING A NEGATIVE ADJUSTMENT IN ENAJ
You enter a negative adjustment in ENAJ to make inventory corrections that subtract product from locations in 
the system records. The procedure is the same as for a positive adjustment except that instead of adding 
product to a location or locations you will be subtracting quantities. You must therefore enter a negative 
number in the Adjust Quantity field in ENAJ.
You can also use negative adjustments to correct product that was recorded under an incorrect lot number. 
First, you make a negative adjustment to subtract product from the incorrect lot number. Next, you make a 
positive adjustment to add product to the correct lot number.
1 Enter ENAJ. The program will be in the Enter Criteria Mode.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the negative amount and the SKU of the entity that you wish to remove from the system and press 
Enter (for example, -5CASE). If you do not enter a SKU, AccellosOne 3PL will use the item’s lowest 
SKU.
The system automatically updates the weight-related fields and fills in the Adjustment Date. If this entity 
has an expiry date or is part of an open lot, the system will automatically populate the corresponding 
fields.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 147

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date 
field. 
9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know 
the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. This information will print on the Adjustment Audit Report (ADJ01).
11 Click on Location Block. The Location Block displays the locations where this entity is currently stored 
and the amounts in each location. Use the up and down arrow keys to move the cursor next to the location from which you will be removing the inventory. 
Press Enter until the cursor is in the Adjust (From) Column. Key in the negative amount and SKU that 
you are removing from this location. Press Enter.
If you are removing product from more than one location, move your cursor to the next location where 
you will be removing inventory (for example if you are adjusting ten cases and you remove five cases 
from one location and the remaining five cases from a second location). Repeat until the proof is zero.
Key in the amount 
that you are removing from inventory. 
This must be a 
negative SKU 
amount.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts

ENAJ screen showing Location Block
12 Click on Process Adjustment.
13 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.

ENAJ screen showing the Remarks Block
14 When you finish entering your remarks, click on Return. A message will display indicating the number of 
the adjustment record.
15 If prompted to enter a charge for the transaction, click on Exit.
Check the Proof 
Box.
The negative 
value of the 
proof must be 
entered in the 
Location Block 
to bring the 
proof to zero.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 149
16 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit ENAJ.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the Adjustment 
record.
CHANGING THE PRODUCT’S RECEIVED DATE
The product’s received date is the date that the product was confirmed in CHRF. When you perform a transfer 
adjustment in ENAJ, you can retain the product’s original received date or you can overwrite this date with the 
current date. You define your received date option in ADJU (Adjustment Type Codes) and then attach the 
appropriate adjustment type code to your adjustment in ENAJ.
If you select Original as your option in the Date Used for Adjustments / Renewals field in ADJU, the product to 
which you are applying this adjustment type will retain its original received date and will renew on that date 
(anniversary monthly and anniversary weekly billing only). 
If you select Current, the product to which you are applying this adjustment type will be assigned the current 
date as its received date and will renew on the day that the adjustment was made (anniversary monthly and 
anniversary weekly billing only).
ENTERING A TRANSFER ADJUSTMENT IN ENAJ
A transfer adjustment in ENAJ allows you to transfer product within the system without creating an invoice. 
You can use this program to adjust inventory records that have incorrect:
 customer codes
 item codes
 inventory level codes
 expiry dates
For example, product that was recorded under an incorrect lot number will need to be subtracted from that lot 
number and added to the correct one; product that was assigned to the wrong customer will need to be 
subtracted from that customer and added to the correct one, etc. You begin with a negative quantity in ENAJ 
since you must first subtract product from the incorrect detail category and then add it to the correct one.
Transfer adjustments do not require that both items have the same quantity breakdown. You can transfer 
product from a pallet/case item to an each item and vice versa.
1 Enter ENAJ. The program will be in the Enter Criteria mode.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels. 
5 Click on Execute Query. 
6 Press Enter until the cursor is in the Adjustment Quantity field. 
7 Key in the negative amount and the SKU of the entity that you wish to remove from the system because 
it was entered incorrectly and press Enter. If you do not enter a SKU, AccellosOne 3PL will use the item’s 
lowest SKU.
The system automatically updates the weight-related fields and fills in the Adjustment Date. If this entity 
has an expiry date or is part of an open lot, the system will automatically populate the corresponding 
fields.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts

ENAJ screen
8 If your system has been configured to do so, you can change the default date in the Adjustment Date 
field. 
9 Press Enter until you reach the Adjustment Code field. Key in the adjustment code. If you do not know 
the code, use the pick list.
10 Key in the reason for the adjustment or press Enter to bypass the Adjustment Reason field. Information 
from this field will print on the Adjustment Audit Report.
11 Click on Transfer To Block. In this block, you will be entering the product’s correct details. 
12 Key in your customer code and press Enter. 
13 Key in your item code and press Enter. 
14 Key in all of the inventory levels and press Enter. 
Key in the negative 
amount that you are 
removing for the 
adjustment. Specify 
the SKU.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 151

ENAJ screen showing the Transfer Block
15 The Transfer Quantity field fills in with the amount that you are transferring and the Help Line displays the 
Message, “The Transfer From Quantity is …” Press Enter. 
The system automatically updates the weight-related fields for items with a standard weight. If the item is 
of non-standard weight, key in the weight details in the corresponding fields.
16 If your system allows the manual entry of expiry dates, you can change the expiry date.
17 Click on Location Block. The Location Block displays the locations where this entity is currently stored 
and the amounts in each location.
Key in the correct 
customer code 
and all inventory 
levels.
Transfer Quantity 
field.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts

ENAJ screen showing the Location Block and the From and To Proof boxes
18 Use your up and down arrow keys to move the cursor next to the location from where you will be subtracting the inventory. 
Press Enter until the cursor is in the Adjust (From) Column. Key in the negative amount and SKU that 
you are subtracting from this location. Press Enter. 
19 Do one of the following:
20 When you finish entering your from and to locations and quantities, both the From Proof Box and the To 
Proof Box should show a quantity of zero.
21 If you are in create record mode, click on Return to Main to exit create record mode.
If the location to which you wish 
to transfer the inventory is 
displayed:
If the location to which you wish 
to transfer the inventory is NOT 
displayed:
a) Move your cursor to the location 
where you want to transfer the 
inventory. If you wish to transfer 
inventory to the same location, 
you skip this step.
b) Press Enter until the cursor is in 
the Adjust (To) Column. Key in 
the positive amount and SKU 
and press Enter. 
a) Press Enter to position your cursor in the Location field.
b) Click on Create Record and key 
in your to location code.
c) Key in the positive amount and 
SKU and press Enter. 

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Adjustments to Inventory Amounts
OPERATIONS 1 GUIDE 4.2 153

ENAJ screen showing the Location Block
22 Click on Process Adjustment.
A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
23 When you finish entering your remarks, click on Return. A message will display indicating the number of 
the adjustment record.
24 If prompted to enter a charge for the transaction, click on Exit.
25 If you need to process another adjustment, click on Enter Criteria to begin the next transaction. Otherwise, click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who made the adjustment. The Document Number is the number of the adjustment 
record.
CREATING NEW INVENTORY IN ENAJ
1 Enter ENAJ.
2 Click on Return to Main.
3 Click on Create Record.
4 Key in your customer code and press Enter.
5 Key in all inventory levels for the new product and press Enter.
6 In the Adjustment Quantity field, key in the quantity and SKU code of the inventory that you wish to add 
and press Enter.
In the From 
Adjust Column 
field, key in the 
negative amount 
that you are 
removing.
In the To Adjust 
Column field, key 
in the amount 
that you are adding

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing Massive Adjustments in MATR
7 Press Enter until you reach the Adjustment Code field. Then key in your adjustment code and press 
Enter.
8 Click on Location Block to enter the Location Block.
9 Click on Create Record and enter the location for the new product.
10 Press Enter to bypass the Hold field.
11 Key in your adjustment quantity and press Enter.
12 When the proof equals zero, click on Process Adjustment.
13 If required, enter your remarks for the adjustment.
14 Click on Exit to exit.
Performing Massive Adjustments in MATR
A massive adjustment is an adjustment in which you transfer all product for a particular entity to another 
inventory entity. For example, you can:
 transfer all product from one item or inventory level to another item or inventory level
 transfer all product for one item from one customer to another 
Unlike ENAJ (Enter Adjustment), you do not specify any quantities in MATR because the adjustment applies 
to all product for up to the inventory level that you specify.
MATR is typically used when you want to rename an item or customer. You first create your new item or 
customer code and then you use MATR to transfer over the item(s)/customer. 
The following conditions apply to massive adjustments:
 If you are transferring product from one customer to another, the two customers must have similar 
inventory level profiles and quantity breakdowns. For example, you cannot transfer an item with two 
inventory levels to a customer with a single inventory level. Neither can you transfer a pallets/cases/
eaches item to a customer with a pallets/cases quantity breakdown.
 If you are transferring product from one item to another within the same customer, both items must have 
the same quantity breakdown (for example, both items must be pallet/case items).
 The product that you are adjusting may or may not be assigned a new received date depending on the 
option that you choose in ADJU (Adjustment Type Code). See “Changing the Product’s Received Date”
on page 149.
NOTE When transferring large numbers of inventory records, it is advisable to run 
an inventory or location report for the items that you are transferring so you can track 
the movement of each inventory entity.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing Massive Adjustments in MATR
OPERATIONS 1 GUIDE 4.2 155
When transferring inventory with multiple levels (for example, item/lot number), the following options are 
available:
TRANSFERRING INVENTORY — PROCESS ONE OPTION
You use the Process One option in the following cases:
 you are transferring item-only inventory
 you are performing a one-to-one transfer
1 Enter MATR.
2 Key in your customer code and press Enter.
3 Enter all inventory levels for the product that you wish to transfer. If you do not know your second level of 
inventory, you can perform your query with the Level 2 field blank. When the system retrieves all lots for 
the item that you specified, you can use your arrow keys to select the lot that you wish to transfer. 
Alternatively, you can transfer all product on a specific receipt by entering your item code and receipt 
number.
4 Click on Execute Query.
OPTION EXAMPLE PROCEDURE
One to One You wish to transfer item A, lot 1, to item 
B, lot 1.
Use the Process One command in MATR.
Many to One You wish to transfer all lots for item A (lots 
1, 2, 3, 4, etc.) to item B, lot 1.
Use the Process All command in MATR.
Many to Many You wish to transfer all lots for item A (lots 
1, 2, 3, 4, etc.) to equivalent lots for item 
B.
Use the Process All command in MATR.
Many to Many You wish to transfer a range of lots for item 
A (lots 101, 102, 103, 104, etc.) to equivalent lots for item B.
Retrieve the lots that you wish to transfer 
using the wildcard character (lot = 10%). 
Then use the Process All command in 
MATR.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing Massive Adjustments in MATR

MATR screen showing lot 101 for item ITEM01
5 Click on Relocate Block.
6 Key in your adjustment code and press Enter.
7 If required, key in an adjustment reason and press Enter.
8 Key in the customer code of the customer to which you are transferring the product and press Enter.
9 Key in all inventory levels for your “to” item. For example, if you are transferring a two-level item (item/
lot), you must specify both the item and lot number in the Relocate Block.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing Massive Adjustments in MATR
OPERATIONS 1 GUIDE 4.2 157

MATR screen showing Process One and Process All options
10 Click on Process One.
11 When the “STOP Do you want to proceed with UPDATE” message appears, key in Y for Yes.
12 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can 
enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
13 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
14 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.
TRANSFERRING INVENTORY — PROCESS ALL OPTION
You use the Process All option when you wish to perform a many-to-one transfer or a many-to-many transfer.
1 Enter MATR.
2 Key in your customer code and press Enter.
3 Enter your level 1 value only and then click on Execute Query.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing Massive Adjustments in MATR

MATR screen showing all lots for ITEM01
4 Click on Relocate Block.
5 Key in your adjustment code and press Enter.
6 If required, key in an adjustment reason and press Enter.
7 Key in the customer code of the customer to which you are transferring the product and press Enter.
8 Key in your level 1 value and press Enter.
9 Do one of the following:
If you are doing a many-to-one 
transfer:
If you are doing a many-to-many 
transfer:
a) Enter all your inventory levels. 
For example, if you are transferring a two-level item (item/lot), 
you must specify both the item 
and lot number in the Relocate 
Block.
a) Proceed to next step.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory
OPERATIONS 1 GUIDE 4.2 159

MATR screen showing Process One and Process All options
10 Click on Process All.
11 When the “STOP Do you want to proceed with UPDATE” message appears, key in Y for Yes.
12 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can 
enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
13 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
14 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.
Relocating Inventory
You use the program Relocate Inventory (RELO) to record changes that involve physical movement of 
inventory from one location to another in the warehouse. It is used most frequently to record consolidation or 
rearrangement of warehouse inventory. You can use RELO when the entire inventory amount has been 
moved from a location or when only a portion of it has been moved. 
The following restrictions apply to RELO:
 You cannot relocate product that is on an open order or receipt.
There are 
four lots for 
ITEM01

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory
 If the Location Capacity Validation Type field in COMP (Company Code) is set to “No validation for userinitiated transactions”, relocating inventory does not take into account the location’s capacity. You can 
move inventory into a location that is considered “full”.
 If the product is on non-breakable hold, you must relocate all product in the location; you cannot relocate 
partial quantities.
RELOCATING INVENTORY NOT ON HOLD
1 Enter RELO.
2 Key in the customer code. If you do not know the code, use the pick list to select it. 
3 Key in the inventory levels of the product that you wish to relocate.
4 Click on Execute Query.
5 Click on Location Block.

RELO screen showing the Location Block
6 Check the Available field in the Header Block to ensure that there is sufficient inventory to relocate. This 
is the total amount available for all locations.
7 The Location Block displays all locations that currently contain or have contained in the past the product 
to be relocated. Use the up and down arrow keys to move the cursor next to the location from which you 
will be removing product. 
The Available field in the Location Block shows the amount of inventory in this specific location. An 
amount of zero indicates that the location used to contain product but is currently empty.
8 Press Enter to move the cursor to the Adjust Quantity field. 
Displays total for 
all locations where 
this product is currently stored.
Displays amount 
in the specified 
location indicated 
by the amount.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory
OPERATIONS 1 GUIDE 4.2 161
If you are removing the entire amount of product that is available in this location, click on Delete while 
your cursor is in the Adjust Quantity field for this location.
If you are removing only part of the full amount that is available in this location, key in the negative value 
and SKU that you are removing (i.e., -15 CASE) and press Enter. The Proof field will show the number 
of units that are being removed.
9 Press Enter again to bypass the Conveyance field.
10 Use the up and down arrow keys to place the cursor next to the location where you will be moving the 
product. If you need to place the product in a location that is not displayed, use the pick list. Press Enter 
until the cursor is in the Adjust Quantity field. Key in the positive value that is being added here and press 
Enter. The proof indicates the number of remaining SKU’s that still need to be relocated.
If the location is not available in the pick list, click on Create Record. Then key in the location, the number 
and SKU that you are adding and press Enter. 

RELO screen showing the Location Block
11 Repeat until the proof is zero.
12 Click on Relocate.
13 A Remarks Block displays. If you wish to enter a remark for the relocation, key in your remark. You can 
enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
14 When you have finished entering all applicable remarks, click on Return to exit. 
A message box will display indicating the number of the adjustment record.
15 If you need to process another adjustment, begin the next transaction. Otherwise, click on Exit to exit.
Product is 
being 
removed 
(subtracted) 
from location 
A101
The same 
product is 
being relocated (added) 
to location 
A102

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory
You can now enter LOEN to check the adjustment. Enter LOEN. Key in the entity and go to its History Block. 
Here you can also check who recorded the relocation. The Document Number is the number of the 
adjustment record.
RELOCATING INVENTORY ON HOLD
When you relocate inventory on hold, the hold code may or may not “travel” with the inventory depending 
upon the type of hold. There are two types of holds in AccellosOne 3PL:
 item holds applied manually in HOAD/ENRE or attached automatically to inbound product through 
setup in IHOP
 location holds defined in LOCA (all product placed in a location with a pre-assigned hold code will be 
placed on that hold)
Item holds override all location holds and “travel” with the product
Location holds defined in LOCA are removed when the product leaves the location
FROM LOCATION TO LOCATION
Item Location Item Hold
Location Hold
Location Item Hold
Location Hold
EXAMPLE 1 A1 100 DMG 200 DMG
You move 10 units of item A1 from location 100 to location 200. Item A1 in location 100 is on DMG (Damaged) hold 
and that hold was applied in HOAD. When you relocate the inventory to location 200, the product remains on DMG 
hold.
EXAMPLE 2 A2 300 DMG 400 DMG QA
You move 10 units of item A2 from location 300 to location 400. Item A2 in location 300 is on DMG hold and that hold 
was applied in HOAD. When you relocate the inventory to location 400, the item hold of DMG applied in HOAD overrides the location hold of QA (Qualify Assurance) defined in LOCA.
FROM LOCATION TO LOCATION
Item Location Item Hold
Location Hold
Location Item Hold
Location Hold
EXAMPLE 3 A1 100 QA 200
You move 10 units of item A1 from location 100 to location 200. All inventory in location 100 is on QA hold and that 
hold is a location hold. When you relocate the inventory to location 200, the QA hold is removed.
EXAMPLE 4 A2 300 QA 400 DMG

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory
OPERATIONS 1 GUIDE 4.2 163
RELOCATING INVENTORY ON ITEM HOLD
When you relocate inventory on item hold, the from location hold code must match the to location hold code in 
the Location Block of RELO. A match means that both locations have no hold or have the same hold. You 
cannot move product from location A100 (hold code = DMG) to location A200 (no hold code).
Item holds in RELO have no check mark in the Loc. Hold column.
1 Enter RELO.
2 Key in the customer code and inventory levels of the product that needs to be relocated and press Execute Query.
3 Click on Location Block.
AccellosOne 3PL will show one line for each location/hold code combination. For example, if there are 10 
units on hold in location A100 and 10 units not on hold in the same location, the Location Block of RELO 
will contain two lines: one for the product on hold and another for the product not on hold.
4 Proceed to enter your from and to locations/quantities in the normal manner. The from location and to 
location hold codes, if any, must match when relocating inventory on manual hold.
You move 10 units of item A2 from location 300 to location 400. All inventory in location 300 is on QA hold and that 
hold is a location hold. When you relocate the inventory to location 400, which is on DMG hold, the QA hold is 
replaced by the DMG hold.
NOTE When you relocate inventory on hold, AccellosOne 3PL creates two records 
in the History Block of LOEN: an RL (Relocation) transaction type with a quantity of 
zero and a HL (Hold) transaction type with a quantity equal to the quantity that was 
relocated.
FROM LOCATION TO LOCATION

INVENTORY MAINTENANCE AND ADJUSTMENTS
Relocating Inventory

RELO screen showing inventory on item hold DMG in location A101
5 When the proof quantity is zero, click on Relocate and complete the relocation in the normal manner.
RELOCATING PRODUCT ON LOCATION HOLD
When you relocate inventory on location hold, no match is required between the from location hold code and 
the to location hold code in the Location Block of RELO. You can move product from any location to any 
location regardless of the location hold as location hold codes do not “travel” with the product.
Location holds in RELO are indicated by a check mark in the Loc. Hold column. 
1 Enter RELO.
2 Key in the customer code and inventory levels of the product that needs to be relocated and press Execute Query.
3 Click on Location Block.
AccellosOne 3PL will show all locations that currently contain or have contained in the past the product to 
be relocated.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing a Massive Relocation of Inventory in MARL
OPERATIONS 1 GUIDE 4.2 165

RELO screen showing inventory in location A105 on location hold of DMG
4 Proceed to enter your from and to locations/quantities in the normal manner.
5 When the proof quantity is zero, click on Relocate and complete the relocation in the normal manner.
Performing a Massive Relocation of Inventory in MARL
In MARL (Massive Relocate), you perform massive relocations. A massive relocation can involve the 
movement of any one of the following:
 all product belonging to a particular customer
 all product with a particular level 1, 2, 3 or 4 value
 all product stored in a particular warehouse
 all product stored in a particular location
 all product that has been placed on a particular hold

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing a Massive Relocation of Inventory in MARL
You can also relocate any combination of the above. For example, all product belonging to customer A, in 
warehouse 1 on the hold DMG.
There are two relocate options in MARL: you can move a specific inventory entity from one location to 
another (Process One) or you can move all inventory retrieved in your query to a single location (Process All). 
If the product to be relocated is on hold or if the from or to location is on hold, the rules described in 
“Relocating Inventory on Hold” on page 162 apply to each inventory entity. That is, item holds override all 
location holds and “travel” with the product while location holds defined in LOCA are removed when product 
leaves the location.
1 Enter MARL.
2 Key in your search criteria. You can query by customer code, any inventory level or combination of inventory levels, from location code, from warehouse code or from hold code. 
3 When you finish entering your query criteria, click on Execute Query. AccellosOne 3PL will display all 
inventory entities that meet your search criteria.
4 If your query retrieved multiple inventory entities, you can use up and down arrow keys to view each 
inventory entity.
NOTE You cannot move partial quantities of inventory in MARL. For example, if you 
have ten units of Item A in location 100, you cannot move five units of this inventory to 
location 200. If you want to move partial quantities, you must use RELO instead of 
MARL.
TIP When relocating inventory, it is advisable to use the Print function in MARL to 
print a listing of the inventory that you are relocating so you can track the movement 
of each inventory entity.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing a Massive Relocation of Inventory in MARL
OPERATIONS 1 GUIDE 4.2 167

MARL screen showing item A2, lot 101
5 Click on Location Block.
6 Check the Available to Relocate field in the Header Block to ensure that there is sufficient inventory to 
relocate. This amount is the total amount for the currently selected inventory in the Header Block.
7 Key in the warehouse code to which you are relocating the inventory and press Enter.
8 Key in the location code to which you are relocating the inventory and press Enter. If the to location has 
an automatic hold, the hold code will display in the Automatic Hold Code field.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Performing a Massive Relocation of Inventory in MARL

MARL screen showing Process One and Process All commands
9 Do one of the following:
10 When the “STOP Do you want to proceed with UPDATE” message appears, click on Yes. If you selected 
the Process All option, the number of records being relocated will be shown.
11 A Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You can 
enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
12 When you have finished entering all applicable remarks, click on Return to exit. 
If you wish to relocate only the 
currently selected inventory in 
the Header Block:
If you wish to relocate all 
inventory in the Header Block to 
a single location:
a) Click on Process One. a) Click on Process All.
Product is 
being relocated to this 
warehouse 
and location.
To location 
has been 
assigned a 
location hold 
of DMG

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 169

MARL screen showing the number of the adjustment record (200) and each inventory entity being 
relocated
13 If required, you can jot down the number of the adjustment record for future reference. You can also 
scroll down the External Messages window to view all inventory entities being relocated.
14 When you finish viewing the individual relocation records, do one of the following:
15 If you need to process another adjustment, begin the next transaction. Otherwise, click on Return to Main 
and Exit to exit.
Entering Hold Adjustments
In AccellosOne 3PL, product can be put on hold as it is received into the warehouse. Product can also be put 
on hold after it has been received into the warehouse as normal inventory. Product that is placed on hold 
must have the hold removed before it can be shipped (unless the hold is defined as shippable in HOLD). 
It is possible to place product on hold either automatically or manually. The following are various ways of 
putting a hold on product:
 The item always requires a hold to be put on it as it is received into the warehouse. A hold profile 
defined in IHOP was therefore attached to ITEM so that this product will automatically be placed on hold 
every time that it is received into the warehouse. The automatic hold code shows as the default in ENRE 
and is applied as the receipt is created in the program ENRE. 
 The item is stored in a hold-type location. When the receipt was created in ENRE, this item was placed 
into a hold-type location.
If you wish to print a listing of 
each relocation transaction:
If you do NOT wish to print a 
listing of each relocation 
transaction:
a) Click on Select Printer.
b) Key in your printer code and 
press Enter.
c) Click Ok.
d) Click on Exit to close the External Messages window.
a) Click on Exit to close the External Messages window.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
 The item needs to be placed on hold after it has been received into the warehouse as regular non-hold 
inventory. This requires a manual hold entry in the program Hold Adjustments (HOAD).
You use the program Hold Adjustments (HOAD) for the following transactions: 
 putting product on hold 
 removing product from hold 
 adjusting existing hold data records
PLACING INVENTORY ON HOLD IN HOAD
1 Enter HOAD.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the entity’s other inventory levels if applicable.
5 Click on Execute Query. 
6 Click on Hold Block. This block shows all locations for the product that you queried on in which the product is on hold. If the on hold quantity is zero, that means that the product in the location used to be on 
hold but is currently free of any hold.

HOAD screen showing the Hold Block
7 Check the Available to Hold field that is located just above the Hold block to verify whether there is 
enough product for the required hold adjustment. This block shows all locations for the product that you 
queried on in which the product is currently on hold or was on hold in the past. If the on hold quantity is 
zero, that means that the product in the location used to be on hold but is currently free of any hold.
Displays total 
for all locations 
where this product is currently 
stored.
Displays the 
amount in the 
specified location indicated by 
the cursor.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 171
There is one record in the Hold Block for each unique combination of location code/hold code. For example, if a given product used to be on hold BF (Blast Freezing) in location A100 and is now on hold DMG 
(Damaged) in the same location, you would see two records in the Hold Block:
A100BF0CASE
A100DMG5CASE
There are two ways of placing product on hold in HOAD:
if there is an existing record in the Hold Block for the location code/hold code, you modify the existing 
record
if there is no record in the Hold Block for the location code/hold code, you must enter create record mode 
8 Do one of the following:
9 Key in your hold code and press Enter.
10 Check the Available to Hold field at the bottom of the Hold Block to verify the amount of product that is 
available in this location for the hold adjustment. 
11 Key in the positive value and SKU that you wish to put on hold.
If the product’s location/hold 
code is shown in the Hold Block:
If the product’s location/hold 
code is NOT shown in the Hold 
Block:
a) Use your up and down arrow 
keys to move the cursor next to 
the location line with the location 
code and hold code that you 
need.
b) Press Enter to position your cursor in the Hold field.
a) Click on Create Record.
b) Use your pick list to select the 
product’s location.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments

HOAD screen showing the Hold Block
12 Press Enter to complete the line.
13 If the Return to Main button is available, click on Return to Main.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 173

HOAD screen showing the Hold Block
14 Click on Process Hold.
15 The Remarks Block will appear. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
16 When you finish entering your remarks, click on Return to exit.
17 A message will display on the screen showing the number of the adjustment record. Write it down for 
future reference. It will appear as the Document Number in the LOEN History Block.
18 The cursor will return to the Customer Code field for the next hold transaction. If more product needs to 
be put on hold, begin the next transaction or click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN, key in the entity and click on History Block) It 
will show as HL (Hold) Type. You can also check who recorded the adjustment. The document number is the 
number of the processing adjustment record.
REMOVING INVENTORY FROM HOLD IN HOAD
1 Enter HOAD.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the entity’s other inventory levels.
5 Click on Execute Query. 
The adjusted 
amount from 
the above 
screen capture 
now becomes 
part of the On 
Hold column.
Click on Process Hold.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
6 Click on Hold Block. This block shows all locations for the product that you queried on in which the product is on hold. If the on hold quantity is zero, that means that the product in the location used to be on 
hold but is currently free of any hold.

HOAD screen showing Hold Block
7 Use the up and down arrow keys to move the cursor next to the location line with the product that needs 
to be removed from hold.
8 Press Enter until you reach the Adjust column field and key in the negative value and SKU to be removed 
from hold. If you wish to remove all product in a given location from hold, click on Delete.
Location Column
On Hold Column
Place the cursor 
next to the location line with onhold product that 
needs to be 
adjusted.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 175

HOAD screen showing Hold Block
9 If you did not use the Delete function, press Enter to complete the line.
10 Click on Process Hold.
11 The Remarks Block will appear. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
12 When you finish entering your remarks, click on Return to exit.
13 A message will display on the screen showing the number of the hold adjustment record. Write it down 
for future reference. It will appear as the Document Number in the LOEN History Block.
14 The cursor will return to the Customer Code field for the next transaction. If more product needs to be put 
on hold, begin the next transaction. Otherwise, click on Exit to exit.
You can now enter LOEN to check the adjustment. Enter LOEN, key in the entity and click on History Block. It 
will show as HL (Hold) Type. You can also check who recorded the adjustment. The Document Number is the 
number of the Processing Adjustment record.
LOOKING UP THE OFF HOLD DATE IN LOEN
You can look up the off hold date for auto take-off holds in the Location Block of LOEN.
1 Enter LOEN.
2 Retrieve the inventory whose off hold date you wish to look up.
3 Press F3 to enter the Location Block.
4 Press the tab key to display the Off Hold Date column.
Key in the 
negative 
value of the 
amount that 
you want to 
take off.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
LOEN showing off hold date column
REMOVING AUTO TAKE-OFF HOLDS IN HATO
If a hold is defined as an auto take-off hold in HOLD (Hold Types), you must remove the hold by running 
HATO (Holds Auto Take-Off). When you run HATO, any auto holds applied to inventory are removed 
according to the auto-hold rules defined in HOLD.
The Holds Auto Take-Off Audit Trail shows the customer, up to three inventory levels, the product’s current 
location, the auto-hold code and the quantity that was removed from hold. HATO can only be run once for 
inventory on hold; if you attempt to rerun HATO a second time for the same hold inventory, the message 
“Report has no data” will print.
If you defined a specific number of 
days in HOLD:
if the number of days plus 1 has passed, the hold will be removed 
If you defined a specific date in HOLD: the hold will be removed if this date has passed

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 177
1 Enter HATO.

Holds Auto Take-Off prompt
2 Click OK to proceed.
3 Key in your printer code or select it from the dropdown list. Then click Ok to print.
ADJUSTING ONLY THE HOLD CODE IN HOAD
If you only need to change the type of hold code in a Hold Block location line but the amount remains the 
same, you must perform two transactions in HOAD.
1 Enter HOAD.
2 Remove the inventory from hold. 
3 Exit HOAD and then re-enter the program.
4 Place the same product on the new hold code in the normal manner. 
PUTTING INVENTORY ON A MASSIVE HOLD IN POHO
You use the program Put on Hold (POHO) to place one hold code type on all inventory that you specify. In 
POHO, first you select the customer, item or entity on which you need to place a hold. Then you choose the 
specific hold code. The system will place this hold on the entire selected inventory in all locations within your 
company. 
NOTE POHO applies a hold only on inventory that is currently free of any hold 
code. If you have 10 cases on DMG hold and 20 cases of the same product on no 
hold, the hold that you specify in POHO will apply only to the 20 cases that are not on 
hold.
ABC Warehousing Inc. Adjustment Number: 204 Page 1 of 1
Holds Auto Take-Off Audit Trail 03.09.07 10:50
------------------------------------------------------------------------------------------------------------------------------------
Customer Level 1 Level 2 Level 3 Location Whse Hold Adjust
---------- -------------------- -------------------- -------------------- ------------ ---- ---- --------------------
A A2 102 * A101 1 24HR -15CASE
D D1 101 GN000344 D100 1 24HR -60CASE

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
If you wish to place a hold on inventory that is stored in specific location(s), use HOAD. To place a hold on a 
specific pallet(s), case(s) or other SKU(s), you would also use HOAD.
POHO does not display the amounts and locations for the inventory entity or customer that you are querying 
on. To find out this information, you must look them up in LOEN.
PUTTING A HOLD ON ONE RETRIEVED RECORD (PROCESS ONE)
This procedure will place one specified hold code type on one record that is retrieved by the system for a 
selected customer, item or inventory entity.
1 Enter POHO.
2 Key in your inventory selection criteria. 
To retrieve all of a customer’s inventory records, key in the customer code and click on Execute Query. 
To retrieve all of an item’s inventory records, key in the customer code and press Enter. Then key in the 
item code and click on Execute Query. 
To retrieve all records for a specific entity key in the customer code, the item code and the applicable 
inventory levels of the entity. Press Enter after each entry. Then click on Execute Query. 
3 With the cursor anywhere in the Header Block screen, use the up and down arrow keys to scroll through 
the retrieved records. Stop when the record with the selection criteria that you need displays on the 
screen.

POHO screen
4 Click on Hold Block. 
5 The cursor moves to the Hold Block field. Key in the hold code that you wish to place on the selected 
inventory and press Enter. If you do not know the code, use the pick list. 
Querying on 
A retrieves 
four records.
Use the up 
and down 
arrow keys to 
scroll through 
the other 
records.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 179
6 Click on Process One.

POHO screen
7 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
8 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
9 When you finish entering your remarks, click on Return to exit.
10 A message block appears with the number of the adjustment record. Write it down for future reference. It 
will appear as the Document Number in the LOEN History Block.
11 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks 
and viewing the transaction details.
PUTTING A HOLD ON ALL RETRIEVED RECORDS (PROCESS ALL)
This procedure will place one specified hold code type on all records retrieved by the system for a selected 
customer, item or inventory entity.
1 Enter POHO.
2 If you want to place a hold code on all of a customer’s inventory, key in the Customer Code. click on Execute Query. 
If you want to place a hold code on a specific item or inventory entity, key in the customer code and the 
applicable inventory levels of the entity. click on Execute Query. 
Selected item.
Process One will apply 
the selected hold code 
to the displayed record 
(only record 1 and not 
records 2, 3 or 4 of the 
current record counter).

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
To view the retrieved records individually, use the up and down arrow keys while your cursor is in the 
Header Block.

POHO screen
3 Click on Hold Block. 
4 The cursor moves to the Hold Block field. Key in the hold code that you wish to place on all retrieved 
records for the selected inventory and press Enter. If you do not know the code, use the pick list. 
5 Click on Process All.
Querying on A 
retrieved four 
records.
Use the up and 
down arrow 
keys to scroll 
through the 
other records.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 181

POHO screen
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It 
will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks 
and viewing the transaction details.
REMOVING INVENTORY FROM A MASSIVE HOLD IN MAHO
You use the program Take Off Holds (MAHO) to remove one hold or all holds from large quantities of selected 
inventory — regardless of location. In MAHO, first you select the customer, item or entity from which you need 
to remove the hold(s). Then you choose:
 to remove one specific hold code from the selected inventory in your entire company or 
 to remove all hold codes from the selected inventory in your entire company
If you wish to remove a hold or holds from inventory stored in specific location(s), use HOAD. To remove a 
hold from a specific pallet(s), case(s) or other SKU(s), you would also use HOAD.
MAHO only displays the hold code types for the customer or entity that you are querying on. To find out the 
amounts and the locations of the entity with this specific hold code type, you must look them up in LOEN.
Selected item.
Process All will 
apply the 
selected hold 
code to all 
retrieved records 
(four in this 
example according to the current record 
counter).

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
REMOVING ONE HOLD CODE (PROCESS ONE)
This procedure will remove one hold code that is currently placed on the product of a selected customer, item 
or inventory entity.
1 Enter MAHO.
2 Choose from the following options:
3 With the cursor anywhere in the header block screen, use the up and down arrow keys to move from one 
hold code type to another for this customer or entity. Stop when the hold code that you need to remove 
displays on the screen.
4 Click on Remove Hold. 

MAHO screen
If you want to remove a specific 
hold code that is currently placed 
on all of a customer’s products:
If you want to remove a specific 
hold code that is currently placed 
on a specific item or inventory 
entity:
a) Key in the customer code. Then 
click on Execute Query. This 
retrieves all hold codes for the 
selected customer.
a) Key in the customer code and 
the applicable inventory levels of 
the entity. Then click on Execute 
Query. This retrieves all hold 
codes for the selected item or 
entity.
Selected item.
The hold code 
that applies to the 
Remove Hold 
Code Block.
Process One will 
removed the displayed hold code 
from the selected 
item (DMG in this 
example).

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 183
5 The cursor moves to the Remove Hold Block and the buttons Process One and Process All display on 
the screen. click on Process One.
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It 
will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks 
and viewing the transaction details. You can also verify by re-entering MAHO, keying in the same selection 
criteria that you used for this procedure. Then click on Execute Query. The system does not have any hold 
codes to retrieve because they were removed by the procedure.
REMOVING ALL HOLD CODES (PROCESS ALL)
This procedure will remove all hold codes that are currently placed on the product of a selected customer, 
item or inventory entity.
1 Enter MAHO.
2 If you want to remove all hold codes that are currently placed on a customer’s products, key in the customer code and click on Execute Query. This retrieves all hold codes for the selected customer.
If you want to remove all hold codes that are currently placed on a specific item or inventory entity, key in 
the customer code and the applicable inventory levels of the entity. click on Execute Query. This retrieves 
all hold codes for the selected item or entity.
If you wish to view the retrieved records individually, use the up and down arrow keys while your cursor is 
in the Header Block.
3 Click on Remove Hold. 
4 The cursor moves to the Remove Hold Block and the buttons Process One and Process All display on 
the screen.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments

MAHO screen
5 Click on Process All.
6 The following message will display: “Stop. Do you want to proceed with update? Yes. No.” Click on Yes.
7 The Remarks Block displays. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
8 When you finish entering your remarks, click on Return to exit.
9 A message block appears with the number of the adjustment record. Write it down for future reference. It 
will appear as the Document Number in the LOEN History Block.
10 If you need to perform a second transaction in this program, repeat the procedure. Otherwise, click on 
Return to Main and Exit.
You can verify that the above procedure was successful by going into the LOEN Location and History Blocks 
and viewing the transaction details. You can also verify by re-entering MAHO, keying in the same selection 
criteria that you used for this procedure. Then click on Execute Query. The system does not have any hold 
codes to retrieve because they were removed by the procedure.
PERFORMING A MASS TRANSFER OF PRODUCT ON HOLD IN MOHO
You can perform a mass transfer of product on hold in MOHO (Move Hold to Hold). For example, you want to 
transfer a large number of inventory entities from a non-shippable hold called DMG for Damaged to a 
shippable hold called RET for Return to customer.
Using MOHO to perform a mass transfer is equivalent to removing a hold from the inventory in MAHO (Take 
Off Holds) and then applying a new hold to the inventory in POHO (Put On Hold).
Selected item.
Process All will 
remove all hold 
codes that are 
currently 
applied to the 
selected item 
(one in this 
example).

INVENTORY MAINTENANCE AND ADJUSTMENTS
Entering Hold Adjustments
OPERATIONS 1 GUIDE 4.2 185
There are two transfer options in MOHO: one-to-one and many-to-one. With a one-to-one transfer, you apply 
a new hold code to the currently selected record in the header block. With a many-to-one transfer, you apply 
a new hold code to all records in the header block.
1 Enter MOHO.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the entity’s other inventory levels if applicable.
5 If required, key in your hold code.
6 Click on Execute Query.
MOHO screen showing four inventory records on hold
A1 Transport will retrieve all inventory that meet the search criteria that you specified. Inventory records 
not on hold will not be retrieved and cannot be processed in MOHO.
The Existing Hold Code field shows the hold code of the currently selected inventory record.
7 Click on Change Hold to position your cursor in the Hold Code field. The key in your to hold code and 
press Enter.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
MOHO screen showing new hold code SUSP
8 Do one of the following:
9 When prompted to proceed with the update, click on Yes.
10 Key in any required remarks and click on Return.
11 Click on Return to Main.
12 Click on Exit.
Adjusting Inventory Details
When items were first recorded in AccellosOne 3PL, the records included details about the item’s weight, 
inventory levels, expiry dates and other applicable features. AccellosOne 3PL uses these details for various 
calculations. If any of these details change, AccellosOne 3PL has programs to accommodate the changes. 
Three of the most commonly used programs are Change Entity Information (CHEI), Weight Adjustments 
(WEAD) and Recalculate Standard Weight (RESW). 
If you wish to apply the new hold 
code to the currently selected 
record (one-to-one transfer):
If you wish to apply the new hold 
code to all records retrieved in 
your query (many-to-one 
transfer):
a) Click on Process One. a) Click on Process All.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
OPERATIONS 1 GUIDE 4.2 187
ADJUSTING THE EXPIRY DATE IN CHEI
You use the program Change Entity Information (CHEI) to change the expiry date of inventory products. It 
may be necessary to change an item or entity’s expiry date due to incorrect data entry on the original 
receiving records or because the shelf life date has to be back-dated. The following procedure only applies to 
inventory items or entities that have expiry dates.
Once this procedure is processed, the system will update all existing inventory records for this selected item. 
The system will replace the currently recorded expiry date with the new one.
1 Enter CHEI.
2 Key in the customer code and press Enter. If you do not know the code, use the pick list.
3 Key in the item code and press Enter.
4 Key in the applicable Inventory Levels.
5 Click on Execute Query.
6 If you have retrieved more than one record, use the up and down arrow keys to find the record with the 
product details that you need.
7 Click on Change Block.
8 In the Expiry Date field the system displays the selected item or entity’s current expiry date. Key in the 
new expiry date over the existing one and press Enter.

CHEI screen showing the Change Block
9 Click on Process Change. 
10 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
11 When you have finished entering all remarks, click on Return to exit. 
A message will display to indicate that the system is processing the change.
Selected item
Expiry Date field

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
12 If you wish to perform another adjustment, key in the next inventory selection criteria. Otherwise, click on 
Exit to exit.
ADJUSTING THE DESCRIPTIONS FOR INVENTORY LEVEL 2 AND HIGHER IN 
CHEI 
You use the program Change Entity Information (CHEI) to change the descriptions of products with Inventory 
Levels 2 and higher. For example, it may be necessary to change the inventory level descriptions due to 
incorrect data entry on the original receiving records. The following procedure only applies to inventory levels 
that have the Assign Description to New Entity flag set to Y in DILP.
Once this procedure is processed, the system will update all existing inventory records for this selected item. 
The system will replace the currently recorded descriptions with the corrected one. 
1 Enter CHEI.
2 Key in your customer code and press Enter. If you do not know the code, use the pick list.
3 Key in your item code and press Enter.
4 Key in the applicable inventory levels.
5 Click on Execute Query.
6 If you have retrieved more than one record, use the up and down arrow keys to find the record with the 
product details that you need.
7 Click on Change Block. The Change Block will display the applicable Inventory Levels for this inventory 
product.
8 Press Enter the required number of times until the cursor is in the Inventory Level Description field that 
you need to change. The system displays the current description for this level. Press F11 (Clear Field) 
and key in the new description. Then press Enter. 
9 Repeat for any of the other levels that you need to change.

CHEI screen showing the Change Block
Selected inventory entity.
Inventory Level 2 
and higher field 
descriptions display here.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
OPERATIONS 1 GUIDE 4.2 189
10 Click on Process Change. 
11 A Remarks Block will display. If you wish to enter a remark for the adjustment, key in your remark. You 
can enter as many lines as you need, but no individual “word” can exceed 40 characters and no line can 
exceed 45 characters.
12 When you have finished entering all remarks, click on Return to Main to exit. 
A message will display to indicate that the system is processing the change.
13 If you wish to perform another adjustment, key in the next inventory selection criteria. Otherwise, click on 
Exit to exit.
ADJUSTING WEIGHT DETAILS
When you need to change the weight details of an item, there are two program options depending on whether 
the item is of standard or non-standard weight. The two programs are Weight Adjustments (WEAD) and 
Recalculate Standard Weight (RESW).
You use WEAD to adjust the weight of an inventory item or entity that is of non-standard weight. Nonstandard weight items do not have a constant weight. Weight changes in WEAD apply to the lowest inventory 
level; for example, if you track pallet ID’s, you must change the weight of each pallet ID individually.
You use the program RESW to adjust the weight or the cube of an inventory item or entity that is of standard 
weight. Standard weight items have a constant weight. Weight changes in RESW apply to all inventory 
belonging to an item regardless of the level 2, 3 or 4 values.
ENTERING WEIGHT ADJUSTMENTS FOR NON-STANDARD WEIGHTS IN WEAD
You use the program Weight Adjustments (WEAD) when the non-standard weight was entered incorrectly on 
the original receiving records. The system will then adjust the weight for this entity for all inventory currently in 
the warehouse. The weight change is effective immediately.
In WEAD you work with the total net and gross weights of the product at the product’s lowest inventory level. 
For example, if you track pallet ID’s for the product, you must change the weight of each pallet ID individually.
There are three weight adjustment options in WEAD:
 you can adjust the gross weight of each lot, pallet ID, roll, etc.
 you can adjust the net weight of each lot, pallet ID, roll, etc.
 you can adjust both
When you adjust the weight of an inventory entity, you have two options: you can enter the adjustment weight 
(that is, the current weight plus or minus the adjustment weight, which is the amount by which the total weight 
must be adjusted because of the change) or you can enter the new total weight.
EXAMPLE
You currently have 5 cases of item A, lot 7, in your warehouse and the weight of this lot is 10 lb. (2 lb. per 
case). If you wish to change the weight of each case to 3 lbs., you can enter an adjustment weight of 5 lb. (5 
X 1 = 5) or you can enter a new total weight of 15 (10 + 5 = 15).
CURRENT WEIGHT NEW WEIGHT
2 pounds per case 3 pounds per case

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
1 Enter LOEN and look up the total number of on-hand units of the inventory entity whose weight you wish 
to change. You will need this information to calculate the adjustment weight or the new total gross or net 
weight.
2 Enter WEAD.
3 Key in the customer code. If you do not know the code, use the pick list.
4 Key in your item code.
5 Key in the applicable inventory levels.
6 Click on Execute Query.
7 Click on Weight Block. The Weight Block displays the Gross Current Total Weight and the Net Current 
Total Weight. These are the weight details of this entity’s total inventory that is currently Available and On 
Hand. The Weight Measure Code field indicates the unit of measure being used.

WEAD screen showing the Weight Block
8 If the Adjustment Date field is activated on your system, you can key in a new date and press Enter. If the 
system date is correct, press Enter to accept it.
9 If the weight measure code you are using to record the change is the same as the one that displays in the 
Weight Measure Code field, press Enter. 
If the Weight Measure Code you are using to record the change is not the same as the one in the Weight 
Measure Code field, key in the code and press Enter. If you do not know the code, use the pick list.
Current Total Weight is 10 lbs.
(5 cases X 2 lbs.)
Adjustment Amount is 5 lbs.
(5 cases X 1 lbs.)
CURRENT WEIGHT NEW WEIGHT
Selected inventory 
entity
The gross and net 
weights for the total 
amount of this 
inventory entity that 
is currently stored in 
your company.
The Weight Measure Code field indicates the unit of 
measure for the 
weight.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
OPERATIONS 1 GUIDE 4.2 191

WEAD screen showing the Weight Block
10 If required, make any necessary changes to the inventory’s gross weight. If no change is required to the 
inventory’s gross weight, press Enter twice to bypass the Gross Adjustment Weight and Gross New Total 
Weight fields.
If you wish to enter the gross 
adjustment weight:
If you wish to enter the new total 
gross weight:
a) Key in your gross adjustment 
weight and press Enter. You key 
in a negative amount if the new 
weight is less than the currently 
recorded weight; you key in a 
positive amount if the new weight 
is more than the currently 
recorded weight. 
b) Press Enter to bypass the Gross 
New Total Weight field.
a) Press Enter to bypass the Gross 
Adjustment Weight field.
b) Key in your new total gross 
weight and press Enter.
Selected entity
The amount that you 
enter in the Gross 
Adjustment Weight 
and Net Adjustment 
Weight fields can be 
a positive or negative value.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
11 If required, make any necessary changes to the inventory’s net weight. If no change is required to the 
inventory’s net weight, leave the Net Adjustment Weight and Net New Total Weight fields blank.
12 Click on Process.
13 A Remarks Block will appear to enter any necessary remarks. If you wish to enter a remark for the adjustment, key in your remark. You can enter as many lines as you need, but no individual “word” can exceed 
40 characters and no line can exceed 45 characters.
14 When you finish entering your remarks, click on Return.
15 Click on Exit to exit.
You can verify weight adjustments in the History Details Block of LOEN. A weight adjustment made in WEAD 
will show in the inventory transaction’s history as a 0 (zero) quantity adjustment. The weight adjustment will 
only show the weight difference not the new total weight.
If you wish to enter the net 
adjustment weight:
If you wish to enter the new total 
net weight:
a) Key in your net adjustment 
weight and press Enter. You key 
in a negative amount if the new 
weight is less than the currently 
recorded weight; you key in a 
positive amount if the new weight 
is more than the currently 
recorded weight. 
b) Press Enter to bypass the Net 
New Total Weight field.
a) Press Enter to bypass the Net 
Adjustment Weight field.
b) Key in your new total net weight 
and press Enter.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
OPERATIONS 1 GUIDE 4.2 193

LOEN screen showing the weight adjustment from the above procedure
ENTERING WEIGHT ADJUSTMENTS FOR STANDARD WEIGHTS IN RESW
You use the program Recalculate Standard Weight (RESW) to adjust the standard weight or cube of an item. 
An item must be set up as a standard weight item in order to use RESW. If the item is not a standard weight 
item, you must adjust its weight in Weight Adjustments (WEAD).
A standard weight may need to be changed because the item’s weight details were keyed in incorrectly in the 
original ITEM record or because the manufacturer changes the size of the standard container. For example, a 
case of paint is currently recorded in the system as having a standard gross weight of 15 lbs. The system 
uses this data in all applicable calculations. However, the manufacturer has now changed the size of the paint 
container and a case of paint now weighs only 14 lbs. 
First, you record the change in the Item Quantity Breakdown Block of the program ITEM. Then you run 
RESW to update the weight or cube data on existing inventory records. The system will apply the change 
effective from the date that you enter as the Adjustment Date. 
There are two adjustment options in RESW:
 post adjustment
 reprocess history
The post adjustment option will create a separate line for the adjustment. For example, if the original standard 
weight of the item was 2 lbs. per case and you adjust it to 3 lbs. per case, the adjustment for 5 cases of 
available inventory would appear as follows:
A 0 cases 5 lbs. (difference between old weight of 10 lbs. and new weight of 
15 lbs.)
A weight adjustment shows as a 
0 quantity adjustment.
Only the weight 
adjustment displays — not the 
new total weight.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
If you select the reprocess option, the original lines in the History Block of LOEN will be adjusted to the new 
weight and there will be no separate adjustment line showing the difference between the original weight and 
the new standard weight.
1 Enter ITEM.
2 Click on Enter Criteria.
3 Key in the Customer Code and press Enter. If you do not know the code, use the pick list.
4 Click on Execute Query.
5 Click on Quantity Breakdown Block.
6 If necessary, use the up and down arrow keys to move to the SKU record with the weight and cube 
details. Press Enter until the cursor is in the cube or weight field that you need to change. Key in your 
new value and press Enter. 

ITEM screen showing the Item Quantity Breakdown Block
7 When you have finished changing all of the applicable fields, click on Master Block and Exit.
CO -5 cases -10 lbs. (you confirm the order of 5 cases)
CR 10 cases 20 lbs. (you confirm the receipt of 10 cases)
CO -5 cases -15 lbs. (you confirm the order of 5 cases)
CR 10 cases 30 lbs. (you confirm the receipt of 10 cases)
Cube fields of 
the selected 
item or entity.
Gross and Net 
Weight fields of 
the selected 
item or entity.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
OPERATIONS 1 GUIDE 4.2 195
8 Enter RESW.
9 Key in your customer code and press Enter. If you do not know the code, use the pick list.
10 Key in A (Post Adjustment) or R (Re-Process History) and press Enter. A will create a separate line in 
the History Block of LOEN so that you can see both the original record and the adjustment record. R will 
adjust all history records in the History Block of LOEN to show the new weight.
11 If the Adjustment Date field is activated, key in the date when the weight change became effective and 
press Enter. If the date when the weight change began is the same as the default date, press Enter to 
accept the default date.
12 Key in the item code of the item whose weight or cube is being changed and press Enter. If you do not 
know the code, use the pick list.

RESW screen
13 Click on Process. A message will display to inform you that the system is processing the adjustment.
14 Click on Exit to exit.
You can verify that the RESW transaction was successful by looking up this transaction in the History Block of 
LOEN.
Adjusting the Weight of Open Orders and Receipts
RESW will not adjust the weight of product on open orders and receipts. Refer to the following table for 
specific instructions:
open receipts Delete the receipt lines and then re-add them. When you create a 
new receipt line, AccellosOne 3PL will retrieve the new weights 
defined in ITEM.
Post Adjustment or Reprocess field.
Adjustment 
Date field.
Process button

INVENTORY MAINTENANCE AND ADJUSTMENTS
Adjusting Inventory Details
CLEARING WEIGHTS IN CLWE
This program allows you to clear the weights — that is, set to zero — of all items with a positive or negative 
weight but a quantity of zero. If you do not clear your weights, you may generate invoices and reports for 
product that is no longer in your warehouse.
CLWE will clear all weights for the customer or customers that you specify and post a weight adjustment to 
the item. The effective date of the weight adjustment will be either the last transaction date for the item or lot 
or the adjustment date that you enter in CLWE.
When you run CLWE, the first renewal billing after you clear your weights may be slower than usual. 
However, all subsequent renewal billings will be normal.
1 Enter CLWE.
2 Key in your customer code and press Enter.
3 Key in your item code and press Enter.

Clear Weights (CLWE) screen
pending order line AccellosOne 3PL will retrieve the new weights defined in ITEM during allocation.
regular order line with or without location enteredChange the to ship quantity of each order line to zero. Then reenter the correct to ship quantity. AccellosOne 3PL will retrieve the 
new weights defined in ITEM.
CAUTION Do not run CLWE while performing inventory activity for that customer. 
Inventory activity includes any transaction that affects inventory such as entering a 
receipt or order, confirming a receipt or order, making an adjustment or relocating 
product. If you run CLWE while performing any of these activities, your inventory 
could be out of balance.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Reversing a Document’s Flow in RVDF
OPERATIONS 1 GUIDE 4.2 197
4 In the Adjustment Date/Last Transaction Date field, key in A for Adjustment Date or L for Last Transaction Date and press Enter.
5 If you selected Adjustment Date in the previous field and if the Adjustment Date field is activated, you can 
press Enter to accept the current system date as your adjustment date or you can key in a new adjustment date and press Enter.
6 Click on Update Inventory. If the customer that you selected has non-zero weights for inventory whose 
quantity is zero, the message “Clearing out weights” will be displayed.
Reversing a Document’s Flow in RVDF
You can reverse an order or receipt’s flow for all new lines in the program RVDF (Reverse Document Flow). 
For example, you wish to add a new order line after picking or loading a given order. By reversing the order 
header to STPI (Start Picking) from FIPI (Finish Picking), you can allocate and pick the new order line. 
Existing order lines, however, will remain at the FIPI flow.
You can reverse a document’s flow to any flow that precedes the document’s current flow. However, you 
cannot reverse a flow back to ENRE (Enter Receipt) or ENOR (Enter Order).
The following restrictions apply if the order has been assigned to a load:
 you cannot reverse an order flow if the load is confirmed
 you cannot reverse an order flow if the order has been loaded in OLOP and is NOT the last stop (for 
example, if order 10 is assigned to stop 4 and order 11 is assigned to stop 3, you can reverse the order 
flow of order 11 because it is the last stop loaded but not order 10) 
 you cannot reverse the order flow if the load is locked
1 Enter RVDF.
2 Do one of the following:
If you wish to reverse the flow of 
an order:
If you wish to reverse the flow of 
a receipt:
a) Key in your order number and 
press Enter.
a) Key in your receipt number and 
press Enter.

INVENTORY MAINTENANCE AND ADJUSTMENTS
Reversing a Document’s Flow in RVDF

RVDF screen showing order header at the flow STLO (Start Loading)
3 In the Reset Flow Process Code field, select from the dropdown list the previous flow code that you wish 
to assign to all new receipt or order lines. If the dropdown list is deactivated, this means that the document is already at the flow immediately following ENRE (Enter Receipt) or ENOR (Enter Order) and cannot be reversed.
4 Click on Accept to save your changes.
5 Click on Exit to exit.

OPERATIONS 1 GUIDE 4.2 199
SHIPPING
Overview of Shipping ..................................................................................... 200
Entering a Regular (R-Type) Order................................................................ 203
Modifying an Order ......................................................................................... 229
Deleting an Order ............................................................................................ 236
Order Header Types and Order Line Types.................................................. 241
Looking Up Orders in LOOR .......................................................................... 242
Printing the Shipping Documents ................................................................. 250
Confirming an Order ....................................................................................... 257
Generating the VICS Bill of Lading................................................................ 266
Cancelling or Reprinting Order Documents ................................................. 276
Inspection Orders ........................................................................................... 282
Distribution Orders ......................................................................................... 284
Transfer Orders ............................................................................................... 290
Entering Freight Type or Non-Inventory Orders .......................................... 300
Picking to Clean .............................................................................................. 302
Broker Orders.................................................................................................. 303
Processing Proof of Delivery in POD ............................................................ 306

SHIPPING
Overview of Shipping
Overview of Shipping
The following is a simplified model of the shipping tasks that are involved in processing each order.
PICK
 ALLOCATE
Select and assign the locations from which 
the product will be picked.
PRODUCE PICKING 
INSTRUCTIONS AND OTHER
 SHIPPING DOCUMENTS
SHIP
RECEIVE 
THE
ORDER
RECORD THE 
PRODUCT DETAILS

SHIPPING
Overview of Shipping
OPERATIONS 1 GUIDE 4.2 201
SHIPPING PROGRAMS
Several warehouse tasks are involved in the process of filling order requests and shipping out the inventory. 
Shipping is also referred to as the outbound process. The outline below lists the shipping tasks and their main 
functions:
ENOR is the first flow in the shipping process. You enter the details that 
apply to the entire order in the Header Block and you enter the details for 
each separate item of the shipment in the Line Block. 
You can also add any outbound charges and special details that may apply 
to this order in the Optional Blocks. 
You time-stamp and advance each flow process for the entire order.
You Execute Confirm. This command accepts the details for the entire order into the system 
and updates inventory data accordingly. 
In the program CHOF, you have already time-stamped and advanced all of the order’s flow 
processes — up to COOR (Confirm Order).
You Execute Confirm for the last flow — COOR (Confirm Order) in the program COOL. You 
do this only for the individual order lines that you specify. The system updates inventory data 
accordingly.
After each flow, you print any document(s) attached to that particular flow. The system will do 
this for the order(s) that you specify.
Printing of the designated picking document will allocate the order — that is, assign the product and the location(s) to be used for picking.
You use PROR to print the document(s) attached to a specific flow. The system will do this 
for all order numbers that are currently in the system and that are at the same stage in their 
flow process.
If necessary, you cancel the requirement to print an attached shipping document. This 
advances the system to the next flow process without actually printing the document. 
If the document has been printed before, you can set REOR to reprint the attached order 
document.
ENOR
Enter Order
CHOF
Time-Stamp and Confirm 
COOL
Confirm Orders - One 
PROM
Print Shipping 
PROR
Print Shipping 
REOR
Requeue Order 

SHIPPING
Overview of Shipping
SHIPPING OPERATIONS PROCESS
You return to CHOF/COOL and PROM/PROR as many times as necessary until all flow processes and all 
attached shipping documents are processed.
CHOF or COOL
Flow Process 2
Flow Process 1
Flow Process 3
Execute Confirm
ENOR
CHOF or COOL
CHOF or COOL
PR0M or PROR
Need to print
shipping
document?
PROM or PROR
Need to print
shipping
document?
Yes
PROM or PROR
Need to print
shipping
document?
No
Yes
No
No
Yes

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 203
Entering a Regular (R-Type) Order
You begin the shipping process in AccellosOne 3PL by entering an order record in the program ENOR (Enter 
Order). In ENOR you record details of the product that the warehouse is shipping out to a specific consignee 
(the receiver of the goods). 
OVERVIEW
The ENOR program consists of the following sections:
 Order Block (also called the Header or Master Block)
 Remarks Block
 Carrier Block
 Accessorial Charges Block
 Line Block
The Header Block and Line Block are mandatory. The other blocks are optional.
The record created in ENOR has general information that applies to the whole shipment and specific information about the individual items that make up the shipment. To capture this in AccellosOne 3PL, ENOR has 
a Header Block and a Line Block. General information that applies to the whole transaction is entered in the 
Header Block. Particular information about each item is entered separately in the Line Block.
The following procedure will lead you through the ENOR program, field by field. You will obtain most of the 
information for completing the fields from the order request. Other fields will fill in automatically (populate) 
with data that was preset in other AccellosOne 3PL programs.
Some fields are mandatory. The system will not allow you to continue until you enter data into a mandatory 
field. Other fields are optional and the system will allow you to bypass them by pressing Enter without 
entering any information.
Certain fields have pick lists, which display the available options for that field. This is helpful when you do not 
remember the code that you need. 
There are various Header Block order types. R (Regular) is the usual type that you use when the product is 
available for filling the order. There are other Header Block order types for special circumstances when the 
ordered product is not available.
The procedure below is for an order that is R (Regular) type in the Header Block.
ENTERING HEADER INFORMATION IN ENOR
The Header Block is also called the Master Block. Data entered in the Header Block applies to all line records 
that will be created in the Line Block. 
1 Key in ENOR at the Enter Selection Prompt. Press Enter and the system displays the Enter Orders (Outbounds) screen. The program is in the Create Record mode.
2 Leave the Order Number field blank. The system will automatically generate a number later.
3 For a normal order type, leave the Order Type field with the R (Regular) that is generated by the system. 
4 The cursor is in the Customer Code field. Enter the code of the product owner and press Enter. 
If you do not know the code, press F10 and then click on Execute Query to display the pick list. Use the 
pointer (arrow) keys to move the cursor next to the applicable code. Click on Select Code. 

SHIPPING
Entering a Regular (R-Type) Order
5 The system automatically fills in the next seven customer-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. 

ENOR screen
6 Enter the Consignee Code of whomever will be receiving the product and press Enter. If you do not know 
the code, use the pick list. 
7 The system automatically fills in the next seven consignee-related fields: Name, Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code. If you used a forward slash to bypass the Consignee 
Code field, see the information note above.
8 The system either bypasses or automatically populates the Priority field. Priorities determine the printing 
sequence of this order’s documents over other orders that have documents in the printing queue at the 
same time (auto-printed documents only) and whether this order’s product can be de-allocated and 
assigned to another order with a higher priority.
The system default is 5. If you need to change the default value, press F9 (Previous Field) until the cursor is in the Priority field. Key in the correct number and press Enter or use the pick list, if necessary.
NOTE If the Consignee Code that you need does not exist in the pick list and manual consignees are activated on your system, key in / (a forward slash) in the Consignee Code field and press Enter. Then, in the Name field, key in the actual name 
and press Enter. This will allow you to bypass these mandatory fields. Key in the 
Address 1, Address 2, Address 3, City, State/Province and ZIP Code fields as applicable or press Enter to bypass these optional fields.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 205
9 The cursor is in the Sold To Code field, which refers to the party who will pay the product owner for the 
goods. The Consignee and the Sold to party may be different. For example, the head office of a department store chain will pay for the product but the product is being shipped to Store # 22. The head office is 
the Sold To and Store #22 is the Consignee.
If you do not need to capture Sold To information or if the Sold To and the Consignee are the same, key 
in S (for Same as Consignee).
If the Sold To and the Consignee are not the same, key in the Sold To Code and press Enter. If you do 
not know the code, use the pick list.
10 The system automatically fills in the next seven Sold To Code related fields: Name, Address 1, Address 
2, Address 3, City, State/Province and ZIP Code. If you used a forward slash to bypass the Sold To Code 
field, see the information note above.

ENOR screen
11 Press Enter to accept the default date as the order date. If a different order date is required, key in the 
correct date using the same date format as shown in the field and press Enter.
NOTE If the Sold To Code that you need is not in the pick list and manual Sold To’s 
are activated on your system, key in / (a forward slash) in the Sold To Code field and 
press Enter. Then, in the Name field, key in the actual name and press Enter. This will 
allow you to bypass these mandatory fields. Key in the Address 1, Address 2, 
Address 3, City, State/Province and ZIP Code fields as applicable or press Enter to 
bypass these optional fields.
Order Date, To Ship 
Date and To Arrive 
Date fields

SHIPPING
Entering a Regular (R-Type) Order
You can enter an order date that differs from the current system date by up to one month in the past or in 
the future.
12 If necessary, key in the order time based on a 24-hour clock (i.e. 14:00 for 2:00 p.m.) and press Enter. If 
the time is not required, press Enter to bypass the field. 
13 The default for the to ship date is the next working day based on the default date. If the default is correct 
as the date that the product is leaving the warehouse, press Enter. 
If you require a different to ship date, key in the correct date using the same date format as shown in the 
field and press Enter.
14 Key in the to ship time, if necessary, and press Enter. If the time is not required, press Enter to bypass 
the field.
15 The default for the to arrive date is the same as the to ship date. If the default is correct as the date that 
the product will arrive at its destination, press Enter. 
If you require a different to arrive date, key in the correct date using the same date format as shown in 
the field and press Enter.
16 Key in the to arrive time, if necessary, and press Enter. If the time is not required, press Enter to bypass 
the field.
17 If there is a number that references the order that you are creating, key it in the Customer Order Number 
field and press Enter. This is a free format field. If a reference number does not apply, press Enter to 
bypass the field. 
If you enter a customer order number that has already been used, you will be prompted to reuse it. Click 
on Yes to reuse or click on No to enter a new customer order number.
18 Key in the purchase order number that applies to this order and press Enter. This is a free format field. If 
a purchase order number is not used, press Enter to bypass the field.
If you enter a purchase order number that has already been used, you will be prompted to reuse it. Click 
on Yes to reuse or click on No to enter a new customer order number.
19 Enter the carrier code of the firm that will be transporting the product to the consignee and press Enter. If 
you do not know the code, use the pick list. 
If the pick list does not have a code set up for the required carrier and manual carriers are activated on 
your system, you can key in / and press Enter. Then key in the name of the carrier and press Enter. This 
option is referred to as a “manual carrier” because you, as the operator, keyed in the carrier name.
Note that the pick list has an “Unassigned” option if you do not know the carrier at this point in time.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 207

ENOR screen
20 The system either bypasses or automatically populates the Logistics Management field depending on 
whether or not your system setup includes SmartFreight. If your system does include SmartFreight and if 
previous setups establish that the carrier for this order is a freight-type carrier, the system will automatically place this order into SmartFreight. 
21 Key in the load type code and press Enter. This is a mandatory field and must be completed. Use the 
code NA (Not Applicable) if this order does not involve a Load Type Code. If you do not know the code, 
use the pick list. 
The system automatically fills in the Description field of the Load Type Code.
If a carrier has 
not been 
assigned yet to 
deliver this order, 
select the unassigned option 
from the pick list

SHIPPING
Entering a Regular (R-Type) Order

ENOR screen
22 The Freight Terms field refers to the type of freight charge payment that applies to the delivery of this 
order. 
Key in the applicable freight terms description and press Enter. This is a mandatory field and must be 
completed. Use the code NA (Not Applicable) if this order does not involve any freight charge payments. 
If you do not know the description, use the pick list to select it. 
23 If cash on delivery (COD) was chosen as the type of freight term for this order, the COD Amount field is 
mandatory. Key in the actual cash amount that is to be collected upon delivery of this order and press 
Enter. Do not use any monetary symbols.
If the freight term for this order is not cash on delivery, either press Enter to bypass the field or key in the 
amount that applies to the selected freight term. 
24 If the selected freight term requires the collection of payment upon delivery, the Payment Type field is 
mandatory. This field also uses the code description and not the code acronym (i.e. Post Dated Check 
and not PODS; Warehouse C.O.D. and not W.C.O.D.). 
Key in the code for the method of payment that will be used for the freight charges and press Enter. If you 
do not know the code, use the pick list.
If the freight term for this order does not require the collection of payment upon delivery, either press 
Enter to bypass the field or key in the amount that applies to the selected Freight Term.
25 The Message Code field will only apply if your company has standard messages that print on shipping 
documents. If this order requires a such a message to be printed on one of the shipping documents that 
is attached to this order, key in the appropriate code in the Message Code field. If you do not know the 
code, use the pick list. 
If your system does not have this option or if a message is not necessary, press Enter to bypass the field.
The Freight 
Terms field 
accepts the 
code description but not the 
code acronym. 
For example, it 
will accept “cash 
on delivery” but 
not “COD”.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 209
The system automatically populates the Description field for the message code.
26 The default for the Remarks field is N (for No). If you do not need Header Block remarks to appear on the 
warehouse order form, press Enter to accept the default. 
If you do need Header Block remarks to appear on the warehouse order form, key in Y (for Yes) and 
press Enter. A block will appear later in the program to enter the remarks. 
27 There are four options to choose from in the Carrier Details field.
If your selection is N, press Enter to accept the default. If your selection is any of the other choices, key in 
the applicable letter and press Enter. 
28 Press Enter to bypass the Pallet Details field.
29 Press Enter twice to bypass the EDI Details and Accessorial Charges fields.
N (No) Use when you do not need to track carrier details 
E (Entry) Use to add carrier details during order entry. The Carrier 
Details Block will display later in ENOR. If your warehousing firm purchased the additional system printing option, 
the details will also print on the attached outbound document that was selected by your company.
C (Confirmation) Use to add carrier details during confirmation of the order. 
The Carrier Details Block will display during confirmation. If 
your warehousing firm purchased the additional system 
printing option, the details will also print on the attached 
outbound document that was selected by your company.
B (Both) Use to add carrier details twice — once during ENOR and 
again during confirmation of the order. The Carrier Details 
Block will display in ENOR and during confirmation. If your 
warehousing firm purchased the additional system printing 
option, the details will also print on the attached outbound 
document that was selected by your company.

SHIPPING
Entering a Regular (R-Type) Order

ENOR screen
30 The Warehouse Code field is usually left blank. Press Enter to bypass the field. 
For further information on this field, refer to “Restricting Multiple Item Lines to a Common Warehouse” on 
page 36.
31 Press Enter to bypass the Material Handling Equipment Type Code field.
32 In the Extra Reference Number 1 and the Extra Reference Number 2 fields, key in the data defined by 
the customer and press Enter. 
If the customer does not require such reference data, press Enter to bypass each of the fields.
33 Press Enter to bypass the Distribution Type Code field.
34 If required, key in your account in the Parcel Shipping Account field and press Enter.
35 If you changed the default in any of the fields for Remarks, Carrier Details, EDI and Accessorial Charges, 
the corresponding blocks will display now on the screen in succession. 
Complete the applicable blocks by following the corresponding Optional Blocks procedures, which follow 
the Line Block procedure. Then return to the Line Block procedure listed directly below and complete it. 
If none of these optional blocks apply, proceed to the mandatory Line Block procedure directly below. 
ENTERING LINE INFORMATION IN ENOR 
In the ENOR Line Block, you enter the details of the item that you will use to fill the order request. There are 
two ways of selecting and assigning the specific inventory that is to be used for filling the order that you are 
creating:
 you select the item by completing all of the inventory level fields 
 you allow the system to select the inventory entity through the allocation routine
If there are miscellaneous 
charges 
attached to this 
order, key in Y
in the Accessorial Charges 
field.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 211
If you wish to select the inventory yourself, use the R (Regular) Line Block type. Then complete all of the 
Inventory Level fields in the ENOR Line Block; for example, Item: ABC, Lot Number: 123 and Color: Blue. 
If you want the system to automatically select the inventory through the allocation routine, you use a P 
(Pending) Line Block type. You complete the Inventory Level 1 field and the system will allow you to bypass 
Inventory Level 2 and any other higher inventory level fields that apply to the item. 
For example, suppose you have an item setup that uses two inventory levels:
You key in the information in the Item field but you leave the Expiry Date field blank. Later, when you print the 
designated picking document, this will trigger the allocation routine. The allocation process will select the 
inventory with either the oldest or the most recent expiry date, depending on the First In, First Out/Last In, 
Last Out rules that are set up in your system. The system will populate the Expiry Date field in ENOR and 
show this date in the picking document.
The following table shows the differences between R-type and P-type lines.
Item (Inventory Level One)
Expiry Date (Inventory Level Two)
R-TYPE LINE P-TYPE LINE
Manual Allocation (you assign the inventory) Automatic Allocation (the system assigns the inventory through the allocation routine)
Inventory is reserved for that order and cannot be 
assigned to another order. 
Inventory is NOT reserved for that order; if both an Rtype and P-type order call for the same inventory 
entity and there is insufficient product to fill both 
orders, allocation will fill the R-type order first. Only 
then will any remaining units be assigned to the Ptype order.
Status of inventory in LOEN = “On Order”. Status of inventory in LOEN = “Available”.
Line type does not change after allocation. After allocation, P-type line becomes a R-type line.
If you do not enter your level 2 and higher values in 
ENOR, the system selects these values during order 
entry according to the options that you select in PIPR 
(Picking Profile). AccellosOne 3PL will create as 
many additional R-type lines as are required to fulfil 
the order quantity.
If you do not enter your level 2 and higher values in 
ENOR, the system selects these values during allocation — not order entry — according to your PIPR 
parameters. For example, you can enter your order 
today but your level 2 and higher values will be determined tomorrow when you run allocation.
If you enter the location in ENOR, no selection of 
location by ILOP (Item Location Profile) during allocation will occur.
You cannot enter the location in ENOR. During allocation, the system will select the locations according 
to your ILOP parameters.
Immediate information is provided in ENOR about an 
item’s availability.
No information is provided in ENOR about an item’s 
availability.

SHIPPING
Entering a Regular (R-Type) Order
ENTERING AN R-TYPE LINE
With R-type lines, you can enter all inventory levels if they are known, level 1 only or up to inventory level 2 or 
3. If you do not enter all inventory levels, AccellosOne 3PL will automatically select the inventory when you 
create a new line or exit ENOR. 
1 The system enters the Line Block in Create Record mode. Leave the Line field with the 1 that is generated by the system.

ENOR Line Block screen
2 If you want to select the product that is to be used in filling this order line, press Enter to accept the system-generated R (Regular) as the line type. 
Allocation may run faster because the inventory was 
selected in ENOR, but the full power of AccellosOne 
3PL to select the best possible inventory to pick will 
not be harnessed.
Allocation may run slower because any selection of 
inventory in ENOR was not final, but you will take full 
advantage of AccellosOne 3PL’s allocation routine to 
pick the best possible inventory based on receipt 
date, expiry date, product already in location and 
many other factors.
Inventory must be received and confirmed before you 
can place it on an order.
Inventory not yet received into the warehouse can be 
placed on an order.
Item substitution is not available. You can perform item substitution.
R-TYPE LINE P-TYPE LINE
This screen 
is ready to 
create a 
record for 
line 1 of this 
order.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 213
3 If you need remarks to appear on the designated warehouse order form for this line item, key in Y (for 
Yes) in the Remark field and press Enter. 
Otherwise, press Enter to accept the N (for No) default.
4 If their completion is required, the cursor will enter the EDI, Charge, Warehouse Restriction, Customer 
Code and Hold Code fields. Otherwise, the system will skip over these fields. 
If the system skips over the field but you need to access it (for example, the Charge field), press F9 (Previous Field) the required number of times until the cursor is in the field. 
5 The system may skip over the Warehouse Restriction field leaving it blank. This means the field does not 
apply to this line and the system does not allow you access.
However, the cursor may enter the field and the Help Message Line indicates “Enter a warehouse restriction if required.” If picking of this item is to be restricted to a particular warehouse, key in the Warehouse 
Code and press Enter. If you do not know the code, use the pick list. 
If a restriction is not required, press Enter to bypass the field.
6 The Hold Code field applies to inventory entities that have a shippable hold code placed on them. 
If you wish to ship only product that has been placed on a specific hold, press F9 the required number of 
times until the cursor is in the Hold Code field. Key in the hold code that you wish to restrict the order line 
to and press Enter. If you do not know the code, use the pick list.
If the field is populated, this indicates that either this item or the location where the product has been 
stored has an automatic hold attached to it. Press Enter to accept the current code or use the pick list to 
select a new code. 
7 Key in the item code and press Enter. If you do not know the code, use the pick list. 
Note that item code is always Inventory Level 1.
8 Under the Item Code field, there can be — although none or not all may apply in your case — Inventory 
Level 2, Inventory Level 3 and Inventory Level 4. However, these fields will display with the correct terminology (for example, Lot Number, Production Date, Expiry Date, Pallet ID, etc.) that was preset for this 
customer. 
Complete all of the inventory level fields that display if you wish to select the product yourself. In Inventory Level 2, key in the code for this level and press Enter. If you do not know the code, use the pick list. 
Repeat for the other inventory levels, if applicable.
If you want the system to select the product that is to be shipped, enter the appropriate data up to the 
level that you want the system to select. For example, you need: 
Inventory Level 1 (Item) = One 
Inventory Level 2 (Lot) = 234 
Inventory Level 3 (Production Date) = oldest in stock
In order to allow the system to find and assign Item One, Lot 234 with the oldest production date, you 
would complete Inventory Level 1 and 2 but you would leave Inventory Level 3 blank. (The system would 

SHIPPING
Entering a Regular (R-Type) Order
fill in the blank field after it has completed the allocation routine and has found the correct Production 
Date.)

ENOR screen
9 The system skips over the Alternate Description field either leaving it blank or populating it with preset 
data. 
10 In the Ordered Quantity field, key in the amount and the SKU that was ordered — the number of units 
that you expect to ship to the consignee. Press Enter.
You can key in the amount in any SKU that is valid for order entry. For example, if the item’s quantity 
breakdown is 100 cases per pallet, you can enter an amount of 1,010 cases as follows:
1010 CASES or 10PLT 10 CASES or 9PLT 110 CASES
Embedded spaces are allowed but not required. The total number of characters including blank spaces 
cannot exceed 20 characters.
NOTE When you select an inventory level in an inventory level pick list, you are 
selecting all inventory levels including the lowest inventory level. You cannot manually 
enter a value or select another value from a lower inventory level. For example, if you 
use the pick list for level 2 to select your lot number, you will be forced to select your 
pallet ID at the same time. As as result, you will not be able to access the level 3 field.
If you wish to leave certain inventory levels blank in the Line Block of ENOR, you 
must manually enter your values instead of selecting them from a pick list.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 215
11 If there is enough inventory available, the system will populate the To Ship Quantity with the same 
amount as was entered in the Ordered Quantity field. Press Enter to accept the default entry.
If there is not enough inventory available, see the section “Shipping With Insufficient Inventory” in the 
Allocation Guide.
The system may now skip over the remaining fields and move you to the next Line Block record. If this 
occurs, proceed to step 19. 

ENOR screen showing the Line Block
12 The Quantity Breakdown field as completed by the system. This identifies the SKU that is used to track 
and bill this item. For example if the quantity breakdown field shows PLT: 50 (the largest SKU) and 
CASE: 1 (the smallest SKU), you read it as one pallet has 50 cases.
The system will only allow you to enter this field if the Variable Quantity Breakdown field was set to Y in 
the program ITEM for this product. If this product does have a variable quantity breakdown, key in the 
correct information and press Enter.
The system 
assumes that the 
amount ordered 
and the amount 
to be shipped will 
be the same.
For an R-type 
line, the system 
shows the quantity that is presently available for 
shipping.

SHIPPING
Entering a Regular (R-Type) Order

ENOR screen showing the Line Block
13 The system automatically calculates and fills in the item’s Weight Code, Unit Weight, Gross Weight and 
Net Weight.
F9 (Previous Field) will return you to any of these fields if you need to enter or change data in them. For 
instance, if the item has non-standard weights, you may be required to enter the Unit Weight.
14 The Location Code field assigns the location(s) from which the product is to be picked when filling this 
order. If you want the system to choose the location, leave the Location Code field blank. The allocation 
routine will assign the location according to the parameters set up in Item Location Profile (ILOP).
If you want to choose the location, 
If you wish to select the location 
from which this item is to be 
picked and . . . Then do the following . . .
You know the location Key in the location code of where the item 
is stored and press Enter. If you do not 
know the location code, use the pick list.
You do not know the location Press Enter to bypass the field. Once you 
do know the location, you can return to this 
order — as long as it has not been confirmed — and complete the location code 
field.
Weightrelated 
fields.
It may be 
necessary to 
enter the unit 
of an item 
that does not 
have a standard weight.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 217
15 The system automatically completes the Warehouse Code field based on the location code entered in 
the previous field or based on a pre-set warehouse restriction. See “Understanding Warehouse Restrictions” on page 35 for further information.
16 The Remark, Accessorial and EDI blocks for this line will now appear on the screen for completion if you 
requested them above. If none of these blocks apply, proceed to the next step.
If you need to complete the Remarks Block and/or Accessorial Block, see the corresponding procedures 
in “Optional Blocks of ENOR” on page 224. 

ENOR screen
17 A new line displays for you to enter the next item line from the order documents. If a new line number 
does not display, click on Create Record.
This line involves product that has a shippable holdThe pick list will restrict your options. It will 
only display locations that have inventory 
with the selected shippable hold attached. 
If this line has to be picked from more than 
one location because there is not enough 
product in a single location
See “Assigning Multiple Locations to 
a Line Block Record” on page 221.
If you wish to select the location 
from which this item is to be 
picked and . . . Then do the following . . .
Running total of 
the line details 
that have been 
entered up to this 
point. In this 
example, these 
details are for the 
totals of lines 1 
and 2.
Current record 
counter.

SHIPPING
Entering a Regular (R-Type) Order
Repeat the Line Block procedure for each line record (i.e., for each inventory entity). The upper right 
hand corner of the screen displays a current record counter for your reference. The Line Block also displays a running total of some key details for the line entries that have been entered up to this point.
When you have finished entering all of the order lines, click on Return to Main and Master Block. 
18 You are now taken back to the beginning of ENOR where the system shows the order number that it has 
generated.
19 If you wish to enter another order, click on Create Record. If you wish to exit the ENOR program, click on 
Exit.
ENTERING A P-TYPE LINE
The procedure for entering a P-type line is identical to the procedure for entering an R-type line with two 
exceptions. With P-type lines:
 you leave the inventory levels that you want the system to select blank
 you cannot specify a location
The Allow P-Type Lines in Order Entry flag in COMP (Company Parameters Block) must be set to Y for Yes 
before you can enter P-type lines.

ENOR screen showing the Line Block
When your run allocation, the allocation routine will select the inventory and location for the P-type line and 
then change its type to R for Regular.
QUERYING ON INVENTORY LEVELS IN ENOR
In the Line Block, you can query on any inventory level to see how much of that product is available. For 
example, the screen capture below has an inventory setup of two levels: 
With a P-type 
line, Show 
Totals displays 
as an option.
To view the 
amounts that 
are currently 
available, on 
hand and on 
order for the 
inventory entity, 
click on Show 
Totals.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 219
Inventory Level 1 = Item 
Inventory Level 2 = Lot Number

ENOR screen showing Line Block
TO VIEW ALL ITEMS (INVENTORY LEVEL 1) FOR THIS CUSTOMER 
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 With your cursor in the blank Inventory Level 1 (Item) field, press F10 and then click on Execute Query. 
This will display the pick list with all items for this customer.
4 Select the Inventory Level 1 entity that you need or click on Cancel to exit the pick list.
5 Continue with the Line Block in the normal manner.

ENOR screen showing the pick list for inventory level 1
In ENOR, you 
can query on 
the inventory 
levels to view 
their entities 
and available 
quantities.

SHIPPING
Entering a Regular (R-Type) Order
TO VIEW ALL LOT NUMBERS (INVENTORY LEVEL 2) FOR THIS CUSTOMER 
AND ITEM
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 Key in Inventory Level 1 (Item) and press Enter. If you do not know the code, use the pick list.
4 With your cursor in the blank Inventory Level 2 field (lot number, in this example), press F10 and then 
click on Execute Query. This will display the pick list with all Inventory Level 1 and Inventory Level 2 for 
this customer.

ENOR screen showing the pick list for inventory level 2
5 Select the Inventory Level 2 entity that you need or click on Cancel to exit the pick list.
6 Continue with the Line Block in the normal manner.
TO VIEW A SPECIFIC LOT NUMBER (INVENTORY LEVEL 2) FOR THIS 
CUSTOMER AND ITEM
1 Complete the ENOR Header Block.
2 Complete the ENOR Line Block until you reach the Inventory Level 1 (Item) field.
3 Key in inventory level 1 (Item) and press Enter. If you do not know the code, use the pick list.
4 Key in the inventory level 2 data (Lot Number, in this example.) With your cursor in this same field, press 
F10 and then click on Execute Query. This will display the pick list with only the details for the specific 
Inventory Level 2 that you queried on.
This pick list 
displays all lot 
numbers 
(inventory 
level 2) for the 
customer and 
item selected 
in ENOR.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 221

ENOR Line Block screen
5 Select the specific entity or click on Cancel to exit the pick list.
6 Continue with the Line Block in the normal manner.
ASSIGNING MULTIPLE LOCATIONS TO A LINE BLOCK RECORD
It may happen that you need more units of an item than there is available in a single location. For example, 
the order line is for 20 cases and there are 15 cases in Location 1 and 5 cases in Location 2. If this occurs, 
use the Location Block. This block allows you to record picking from more than one location for an individual 
Line Block record.
1 Complete the ENOR Header Block. 
Querying on 
all inventory 
levels.
This pick list 
displays the 
specific lot 
number for the 
customer and 
item selected 
in ENOR.

SHIPPING
Entering a Regular (R-Type) Order
2 Complete the Line Block fields until you reach the Location Code field.
3 Press Enter to bypass the Location Code field.
4 Click on Return to Main.
5 Click on Location Block. The Location Block appears on the screen and the system fills in the location 
line number.

ENOR screen showing the Location Block
6 Key in the location code from which the first portion of the product will be picked and press Enter. If you 
do not know the code, use the pick list. 
7 The system populates the Warehouse Code field and skips to the next field.
8 Key in the quantity that will be picked from this location and press Enter.
Location and 
amount that will 
be picked from 
the first location.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 223

ENOR screen showing the Location Block
9 Check the Location Proof Box, which indicates the following information:
When the balance indicates 0, it means that all units have had picking locations assigned. 
Total Total units ordered and that need to be picked from inventory locations to fill this order line
Entered Number of units that have had picking locations assigned up to this 
point
Remaining Number of remaining units that still need to have picking locations 
assigned 
Location 
Proof box

SHIPPING
Entering a Regular (R-Type) Order

ENOR screen showing the Location Block
10 In Line 2 of the Location Block, key in the location code and quantity for the next portion of the product 
that will be picked from this second location.
Repeat until the Location Proof Balance is zero. 
11 Click on Line Block.
12 If you need to enter another line in the Line Block, click on Create Record. To exit ENOR click on Master 
Block and Exit.
OPTIONAL BLOCKS OF ENOR
The Optional Blocks are the Remark, Carrier, EDI and Accessorial Charges Blocks. If you requested any of 
these in the Header Block of ENOR, they will display now in succession. Follow the procedures below to 
complete them.
REMARKS BLOCK
The Remarks Block will appear on the screen if the Remarks field in either the Header Block or the Line Block 
is set to Y (for Yes). A remark can be any useful message that will appear on the order. 
1 Key in your remarks. 
NOTE No individual “word” can exceed 40 characters and no line can exceed 45 
characters.
Location 
Proof box 
must be zero 
or the system 
will not allow 
you to confirm the order 
later.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 225

ENOR screen showing the Remarks Block
2 When you finish entering all remarks for this order, click on Return.
3 If you are in create record mode, the next optional block or the Line Block appears on the screen for completion. Continue to process the order in the usual manner.
EXTENDED REMARKS BLOCK
If activated in COMP (Company Code), the Extended Remarks screen allows you to attach one or more 
messages to a given order document. The message can be either a predefined message in MESS or a freetext message that you enter manually. Unlike the messages in DPME (Depositor Print Messages), these 
messages print for a specific order only.
For example, if you select Customer Message and BF (Blast Freezing) as your message code, the text 
“Customer Message” and “BF (Blast Freezing)” will print on your selected document.
1 Select the checkboxes that apply to your remarks: Customer Message, Consignee Message, Carrier 
Message, RF Picking/Voice Message.
2 If required, select your document from the Document Code pick list.
NOTE Adding the message to an actual document such as a bill of lading or receipt 
tally may require custom programming by HighJump.

SHIPPING
Entering a Regular (R-Type) Order
3 Do one of the following:
Extended Remarks screen
4 Click on Save.
5 Click on Exit.
CARRIER BLOCK
The Carrier Block will appear on the screen if the Carrier Details field in the Header Block is set to E (Entry) or 
B (Both). It records data concerning the transportation vehicle and the driver that picks up the product from 
the warehouse. This information is important for reference purposes. 
You can also capture your pallet in and pallet out quantities. Unlike pallets entered in the Pallet Block, pallets 
entered in the Carrier Block are not assigned a pallet type or an account and are not tracked in LOPC (Look 
Up Pallet Control).
1 When you enter the Carrier Block, it is in the Create Record mode. Key in the driver code and press 
Enter. If you do not know the code, use the pick list. The system automatically fills in the Name field.
If the driver’s name is not in the pick list, key in / and press Enter. Then enter the driver’s name in the 
Name field.
2 Enter the Power Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass 
the field.
3 Enter the Carry Unit Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
4 Enter the Vessel Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
If you are using a predefined 
message:
If you are entering a free-text 
message:
a) Select your message code from 
the Message Code pick list.
a) Key in a free-text message in the 
Message Text field.

SHIPPING
Entering a Regular (R-Type) Order
OPERATIONS 1 GUIDE 4.2 227
5 Enter the Voyage Number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
6 Enter the Seal 1 number, if applicable, and press Enter. If it does not apply, press Enter to bypass the 
field.
7 Repeat the above step for seal number 2.

ENOR screen showing the Carrier Block
8 Enter the temperature reading for the front, middle and back of the inside of the transportation vehicle, if 
applicable, and press Enter. If it does not apply, press Enter to bypass the three fields.
9 In the Setting field, if applicable, key in the temperature that the transportation vehicle’s thermostat control is set at and press Enter. If it does not apply, press Enter to bypass the field.
10 In the Ambient field, key in the temperature reading outside of the transportation vehicle, if applicable, 
and press Enter. If it does not apply, press Enter to bypass the field.
11 If required, key in your pallet in and/or pallet out quantities in the fields of the same name and press 
Enter.
12 When you finish, click on Return to Main. The next optional block or the Line Block appears on the 
screen for completion.
NOTE If your warehousing firm purchased the special printing option, information 
from the Carrier Block fields will print on the shipping document(s) that was selected 
by your warehousing firm.

SHIPPING
Entering a Manual Order in MAOE
Entering a Manual Order in MAOE
You can enter manual orders in MAOE. A manual order is a type of quick entry order restricted to P-type order 
lines consisting of just the item code and order quantity. Quick entry orders in MAOE are designed to speed 
up order line creation by eliminating the need to enter level 2/3/4 values, hold codes, a shelf life, etc. 
1 Enter MAOE.
MAOE screen
2 Click on New .
3 Enter your order header in the normal manner.
4 When the Manual Order Entry screen displays, select Pending from the Type dropdown list and press 
Enter.
5 Key in your item code or select it from the pick list.
6 Key in your order quantity and press Enter. 
MAOE screen
7 Repeat the above three steps for any additional order lines that you wish to enter.
8 When you finish entering your order lines, click on Process Order .
NOTE If you wish to edit an order that you created in MAOE, you must do so in 
ENOR. You cannot edit quick entry orders in MAOE.

SHIPPING
Modifying an Order
OPERATIONS 1 GUIDE 4.2 229
9 Click on Exit to exit.
Modifying an Order
You can access and modify orders in ENOR as long as they have not been confirmed. It is possible to change 
data in both the Header Block and the Line Block.
You can check whether or not an order has been confirmed in the program LOOR (Look Up Orders). This 
program has a Status field. An order that has been confirmed will display as “Confirm Order…” in the LOOR 
Status field.
MODIFYING HEADER BLOCK DATA
If you modify an order’s consignee and if that consignee has a workflow profile that differs from the 
customer’s workflow profile, AccellosOne 3PL will use the order’s original workflow profile, not the new 
workflow profile.
1 Enter ENOR. The program is in Create Record mode.
2 Click on Enter Criteria.
3 Key in the system-generated number of the order you want to modify. 

ENOR screen showing the method for calling up an unconfirmed order
4 Click on Execute Query. The order will display on your screen.
Key in the number 
of the unconfirmed order that 
needs to be modified.
Click on Execute 
Query.

SHIPPING
Modifying an Order
5 Press Enter to put the system in Modify Record mode.

ENOR screen showing Modify Record mode
6 Press Enter the required number of times until your cursor is in the field that you want to modify. Delete 
the existing data or press F11 (Clear Field).
7 Key in the new data and press Enter.
8 If you need to make additional changes to other Header Block fields, repeat steps 6 and 7 until all of the 
necessary changes are entered.
9 If you need to make changes to data in the Line Block, click on Line Block and follow the procedure 
below. 
When you have finished entering all necessary changes, click on Return to Main and Exit to exit ENOR.
MODIFYING LINE BLOCK DATA
The data that you can modify in the Line Block depends upon the order line type. If the line type is P for 
Pending, you can modify any field. If, on the other hand, the line type is R for Regular, you can modify the 
remarks, accessorial charges and locations only; if you wish to change the ordered quantity or inventory 
levels, you must delete the entire line. See “Deleting an Entire Line Block Record” on page 238.
1 Enter ENOR. click on Enter Criteria. 
2 Key in the system-generated number of the order you want to modify. click on Execute Query. The order 
will display on your screen. 
3 Click on Line Block. 
4 If this order has more than one Line Block record, key in the number of the Line Block record that you 
wish to change and press Enter or click on Execute Query. If you do not know the line number, use your 
Press Enter 
until your cursor is in the 
field that 
needs to be 
changed.

SHIPPING
Modifying an Order
OPERATIONS 1 GUIDE 4.2 231
up and down arrow keys to scroll through the Line Block records until you find the line needing modification.

ENOR Line Block screen showing the details for the Line 2 record
5 Press Enter until your cursor is positioned in the field that you wish to modify. Then press F11 (Clear Field 
and key in the new data and press Enter.
6 Click on Master Block. Repeat steps 6 and 7 if you need to change any other Line Block records for this 
order or click on Exit to exit the program.
CREATING A NEW ORDER LINE
If you need to add a new line to an order that has already been created but which has not yet been confirmed, 
follow the procedure below.
1 Enter ENOR. Click on Enter Criteria. 
2 Key in the system-generated number of the order you want to modify. click on Execute Query. The order 
will display on your screen. 
3 Click on Line Block. 
4 Click on Create Record.
5 Complete the Line Block in the normal manner.
6 When you finish entering your line, click on Return to Main and Master Block. Then click on Exit to exit 
the program.
Enter the line 
number of the 
line that you need 
to modify.

SHIPPING
Modifying an Order
MODIFYING LOCATION BLOCK DATA
The following procedure applies to all types of Line Block records except for U (Unknown), which always 
allows you to open the order and fill in missing data as long as it has not been confirmed.
1 Enter ENOR. Click on Enter Criteria. Key in the system-generated number of the order that you want to 
modify. Click on Execute Query. The order will display on your screen. 
2 Click on Line Block. 
3 If this order has more than one Line Block record, key in the number of the Line Block record that you 
wish to change and press Enter. If this number is not known, use the up and down arrow keys to scroll 
through the Line Block records until you find the one needing modification.
4 Click on Location Block.
5 Press Enter. You are now in Modify Record mode.

ENOR Line Block screen showing the Location Block
6 Use the up and down arrow keys to move the cursor next to the location line that you need to modify.
7 Press Enter the required number of times until the cursor is in the field that you need to modify. Delete 
the previous data or press F11 (Clear Field). Key in the new data and press Enter or use the pick list to 
select the correct data.
Repeat this step if it is necessary to modify other Location Block lines.
8 When you have finished making all necessary changes to the Line Block, click on Line Block. If you need 
to create a new line, click on Create Record. 
9 When you need to exit ENOR, click on Master Block and Exit to exit.
Use your arrow 
keys to move the 
cursor next to the 
line that you need 
to modify.
Press Enter the 
required number 
of times to move 
the cursor to the 
field that you need 
to modify.

SHIPPING
Modifying an Order
OPERATIONS 1 GUIDE 4.2 233
MODIFYING OPTIONAL BLOCKS DATA
The procedure for modifying the Remarks, Carrier Details and Accessorial Charges blocks is the same. The 
following procedure uses the Remarks Block as an example of the procedure.
1 Enter ENOR. Click on Enter Criteria. Key in the system-generated number of the order that you want to 
modify. Click on Execute Query. The order will display on your screen. 

ENOR Header Block showing how to access the Optional Blocks
2 In the Header Block, press Enter until the cursor is positioned on the Y of the Remarks field.
3 Click on Remarks.
Place the 
cursor in 
the field of 
the optional 
block that 
you need to 
modify.
Then press 
the corresponding 
button.

SHIPPING
Modifying an Order

ENOR Remarks Block screen
4 Delete the existing data and key in the new remark.
5 When you finish changing your remark, Click on Return to exit the Remarks Block. Then click on Return 
to Main and Exit to exit ENOR.
UPDATING THE CARRIER DETAILS IN UOCP
You can update an order’s carrier and/or carrier details in UOCP (Update Order Carrier/Pallet) without 
entering ENOR.
1 Enter UOCP.
UOCP screen

SHIPPING
Modifying an Order
OPERATIONS 1 GUIDE 4.2 235
2 Do one of the following:
UOCP screen showing a range of orders
3 If your query retrieved a range of orders, use your arrow keys to select the order whose carrier details 
you wish to update.
4 Do one of the following:
If you wish to update a specific 
order:
If you wish to update a range of 
orders:
a) Click on Create Record.
b) Key in your order number and 
press Enter.
c) Click on Return to Main.
a) Click on Query Block.
b) Key in your search criteria and 
click on Execute Query.
If you wish to update carrier only:
If you wish to update the carrier 
details:
a) Click on Carrier Update Block. a) Press Enter to position your cursor in the Carrier Details field.
b) Click on Carrier Details.
c) Proceed to step 8.

SHIPPING
Deleting an Order
UOCP screen showing Carrier Update Block
5 Key in your new carrier code and press Enter or select your carrier code from the pick list.
6 Click on Process Carrier Update.
7 Click on Exit.
UOCP screen showing Carrier Details
8 Proceed to enter or update your carrier details.
9 When you finish entering or updating your carrier details, click on Return to Main.
10 Click on Return to Main again and then on Exit.
Deleting an Order
Orders may need to be deleted due to errors. You can delete orders in ENOR as long as they have not been 
confirmed.

SHIPPING
Deleting an Order
OPERATIONS 1 GUIDE 4.2 237
In LOOR, you can view all details of deleted orders except for Line Block details. Deleted orders remain in 
LOOR until they are purged in the program Purge Orders, Receipts, Inventory (PURG).
DELETING AN ENTIRE ORDER
1 Enter ENOR.
2 Click on Enter Criteria.
3 Key in the system-generated number of the order you want to delete.
4 Click on Execute Query. The order will display on your screen. 
5 Press Enter. You are now in Modify Record mode and the Delete button will appear at the bottom of the 
screen.

ENOR Header Block screen showing the Delete entire order option
6 Click on Delete. 
NOTE If product is in a staging location when you delete the order, you must do a 
manual relocation in RELO to return the product to the original non-staging location.
Delete displays 
as an option.

SHIPPING
Deleting an Order

ENOR Header Block screen showing the Delete entire order option
7 A message block displays asking if you want to proceed with the deletion. Key in the letter of whichever 
of the following options applies to your situation and press Enter.
If you chose the R (Remarks Block), the order will be deleted and the Remarks Block will display. Key in 
the reason for deleting the order and press Enter. A message block appears indicating that the order is 
being deleted.
8 Click on Exit to exit the ENOR program.
DELETING AN ENTIRE LINE BLOCK RECORD 
There may be situations in which you need to delete an entire Line Block record from an unconfirmed order. 
For instance, this would be necessary under the following circumstances:
 to cancel the order for an item
 to change the Ordered Quantity or Weight Code fields on an order
 to change the inventory levels or locations
 to change the to ship quantity to zero
When you delete an order line record and then create a new order line, the line number of the new line 
depends on the number of lines on the order and the line number that you deleted. Refer to the following table 
for the renumbering rules in AccellosOne 3PL:
Y (Yes) If you wish to delete without entering any remarks as to why this 
order is being deleted.
N (No) If you do not want to delete this order.
R (Remarks) If you want to delete the order and include remarks explaining why 
this order is being deleted. The remarks will be saved with the 
deleted order.
If . . . then . . .
you delete the first line of an order with a 
single order line
the next new line created will be line 1

SHIPPING
Deleting an Order
OPERATIONS 1 GUIDE 4.2 239
1 Enter ENOR. Click on Return to Main then Enter Criteria. 
2 Key in the system-generated number of the order that you want to delete. Click on Execute Query and 
the order will display on your screen. 
3 Click on Line Block.
4 Key in the number of the Line Block record that you wish to delete and press Enter. If you do not know 
the line number, use your up and down arrow keys to scroll through the Line Block records until you find 
the one needing deletion. Then press Enter to switch to Modify Record mode.

ENOR Line Block screen showing the Delete entire line block option
5 Click on Delete. A message block displays asking if you want to proceed with the deletion. Click on the 
appropriate button.
you delete any line except the first line or 
the last line of an order with multiple order 
lines
the next new line created will be the last line 
+ 1
you delete the last line of an order with multiple order linesthe next new line created will be line number of the line that you just deleted
Y (Yes) If you wish to proceed with the deletion.
N (No) If you do not want to delete this Line Block record.
If . . . then . . .
Delete displays 
as an option.

SHIPPING
Deleting an Order
If you proceed with the deletion, the Line Block record that you were on will disappear and the previous 
line number and its details will be displayed.
6 If you wish to create a new line, click on Create Record and complete the Line Block in the usual manner. 
7 When you have finished making all necessary changes, click on Master Block to exit the Line Block. 
Then click on Exit to exit ENOR.
DELETING LOCATION BLOCK DATA
You use the following procedure to delete records from the Location Block. Records in the Location Block are 
composed of lines. When you delete in the Location Block, you delete the whole line record.
1 Enter ENOR.
2 Key in the order number.
3 Click on Line Block. 
4 Key in the line number of the record that you wish to modify and press Enter. If you do not know the number, use your up and down arrow keys to scroll through the Line Block records until you find the one that 
you need to change.
5 Click on Location Block.

ENOR screen showing the Location Block
6 Use the up and down arrow keys to move the cursor next to the line that you need to delete.
7 Press Enter until the Delete button appears. Then click on Delete.
8 If it is necessary to delete other lines in the Location Block, repeat steps 6 and 7.
Set the cursor at 
the beginning of 
the line that 
needs to be 
deleted.
Press Enter until 
the Delete button is available 
as an option.

SHIPPING
Order Header Types and Order Line Types
OPERATIONS 1 GUIDE 4.2 241
9 When you have finished making all changes that are necessary, click on Master Block and Exit to exit 
ENOR.
Order Header Types and Order Line Types
There are various types of orders in AccellosOne 3PL. The normal order type is R (Regular). It indicates to 
the system that there is sufficient inventory available to fill the order. As you enter the items into an R type 
order, the system removes the ordered quantities from the warehouse inventory records and the changes 
show up in Look Up Entity Information (LOEN).
You use the other Header Block types in special circumstances.
ORDER LINE TYPES
The Line Block types allow you to control the product selection process based on the inventory level fields.
R (Regular) A regular order. Use when there is sufficient inventory available to 
fill the order. The system will remove the ordered quantities from 
inventory records and the changes will show in LOEN.
T (Transfer) Use when you need to transfer product from one warehouse customer to another. See “Transfer Orders” on page 290 for further information.
I (Inspection) Use when you need to retrieve product from inventory for a government inspection. See “Inspection Orders” on page 282 for 
further information.
K (Kit) Refer to the Kitting section of the Operations 2 Guide for further 
information on kit-type orders.
P (Pending) Sets the default for the Line Block Type
D (Distribution) Use when you need to cross-dock and ship an item at the same 
time. See “Distribution Orders” on page 284 for further information.
R (Regular) Use when you wish to select the inventory levels yourself. You 
must know all of the inventory levels and there must be sufficient 
inventory available to fill the order request. The system will remove 
the product that is selected in an R type line from the warehouse 
inventory records. The change will display in LOEN.

SHIPPING
Looking Up Orders in LOOR
Looking Up Orders in LOOR
The program Look Up Orders (LOOR) allows you to view all orders that have been entered into AccellosOne 
3PL and that have not been purged. In LOOR, it is possible to view orders of any status — whether entered, 
confirmed or deleted. 
In LOOR, you can see all of an order’s details. The Status field shows the last outbound flow process that was 
completed for this order so you know where you are in the flow process sequence. LOOR also indicates 
whether or not there are outstanding documents to print for this order. 
P (Pending) Use when you want the allocation routine to select the inventory 
levels. The allocation routine will select the product based on the 
parameters that are preset in Picking Profile (PIPR).
K (Kit) Refer to the Kitting section of the Operations 2 Guide for further 
information on kit-type orders.
U (Unknown) Used for reserve logic customers only. See the Allocation Guide for 
further information.
W (Weight) Used to allocate product by weight. See the Allocation Guide for 
further information.

SHIPPING
Looking Up Orders in LOOR
OPERATIONS 1 GUIDE 4.2 243

LOOR screen showing the Order Block details of order number 1893
LOOR consists of the following sections:
 Order Block (Header Block)
 Time-Stamping Block
 CRM Block
 Line Block
 Optional Detail Blocks (if applicable)
The following procedure allows you to view the details of an order in the various blocks of LOOR. An explanation of the LOOR fields and the data that they contain follows this procedure.
1 Enter LOOR. You are in the Enter Criteria Mode.
2 Do one of the following:
3 When you finish entering your criteria, click on Execute Query.
The Order Block details display for you to view.
4 Click on Time Block. The order’s time-stamping details display for you to consult.
5 Click on CRM Block.
6 Click on CRM / Manual Block.
If you wish to view a specific 
order: If you wish to view all orders:
If you wish to view orders that 
meet specific criteria:
a) Key in your order number. a) Proceed to next step. a) Enter your selection criteria in 
the corresponding field(s).
Order’s status 
in the flow process sequence.
Next document 
in the flow process sequence 
that needs to be 
printed.

SHIPPING
Looking Up Orders in LOOR
7 Click on Master Block and then Line Block. The Line Block details display for you to view. Use your up 
and down arrow keys to move from one Line Block record to another.
8 Click on Master Block.

LOOR screen showing the Optional Blocks fields
9 Check the fields that apply to the optional blocks. If anything other than N (for No) has been entered in 
any of these fields, there are details. Press Enter until the cursor is in the optional block field that you 
wish to view. Then click on the appropriate button and the details of the optional block will display. 
10 Click on Return to exit the optional block. 
11 If you want to view another order’s details, click on Enter Criteria and key in the selection criteria for the 
next order that you wish to view.
12 When you have finished viewing the details, click on Exit. 
ORDER BLOCK
The LOOR Order Block contains basically the same information as the original ENOR record. It does, 
however, have some extra fields as described below: 
If anything other than 
No displays next to 
any of the optional 
blocks fields, there 
are details. Move 
your cursor to the 
field and click on the 
appropriate button 
for that field.

SHIPPING
Looking Up Orders in LOOR
OPERATIONS 1 GUIDE 4.2 245

LOOR screen showing the Order Block details for order number 1830
FIELD DESCRIPTIONS
Status The latest flow process that has been completed for the order. The field also 
indicates the date and time that the flow was processed. Also displays if the 
order has been deleted. (The flow processes and their sequence were defined 
in DIFP.)
Transfer Receipt Number The corresponding order number if this is a transfer order type.
On Load(s) The order’s load number for loads created in SELO (Set Up Load). 
On External Load(s) The order’s load number for loads created in an external system such as 
Freight Logix. 
Back Order Reference If there was not enough product to fill the order and your system is set up to 
allow a back order for this product, this is the corresponding back order number.
If the system had to create more than one back order, the number range is 
provided, for example Back Order Ref: 56 <…> 69 indicates that the back 
orders created are numbers 56 to 69.

SHIPPING
Looking Up Orders in LOOR
Freight Term The order’s freight terms code; for example, COD, collect, prepaid, etc.
Warehouse Code The warehouse that the order lines are restricted to. Only product in this warehouse can be allocated to the order lines.
Parcel Shipping Account The parcel shipping account (Canada Post, DHL, FedEx, etc.) for the order.
Document Status Indicates if there are any order documents that need to be printed for this 
order. Names the next document that requires printing according to the flow 
process sequence. 
Remarks and Carrier 
Details
Y = Yes
N = No
B = Both
C = Confirmed
E = Entry
If Y or E is displayed next to any of these fields, there are details entered in 
that block. To view the details, press Enter until the cursor is in the optional 
field that you want to view. Click on Return and the optional block details will 
display.
Quick Response Refer to the Quick Response Labels section in the Operations 2 Guide.
Order Date The date entered in the Order Date field of ENOR; the date when the order 
was created.
Shipped Date The date entered in the Ship Date field of CHOF (Time-Stamp and Confirm 
Orders). If you do not enter a date, the system will use the date that the order 
was confirmed in CHOF. 
Location Status Indicates whether all of the order’s lines have been assigned a location yet 
(Entered) or whether they are still unassigned (Missing). 
Shipped Weight Only available for confirmed orders
Refers to weights recorded on outbound labels. 
Pallets/Pieces Shipped Only available for confirmed orders
The total number of pallets/pieces shipped.
Total Units The total number of units for all of this order’s Line Block records. This is the 
total number of units entered in the To Ship field of the Line Block.
FIELD DESCRIPTIONS

SHIPPING
Looking Up Orders in LOOR
OPERATIONS 1 GUIDE 4.2 247
TIME-STAMPING BLOCK
The Time-Stamping Block displays the details of the flow processes that have been completed up to this point 
for this order. If there is a document attached to a flow and this document has been printed, you can click on 
the View icon to see a PDF version of the document.
If the Appointment Remarks button is enabled, you can look up remarks entered in APPL (Appointment 
Planner) for the appointment’s order.

LOOR screen showing the Time-Stamping Block
Gross Weight The total gross weight of all the lines added together. 
Net Weight The total net weight of all the lines added together.
Load Type Code The order’s load type.
Reference Number 1/2 The order’s reference number 1/2 information.
Wave Number The order’s wave number (if any).
FIELD DESCRIPTIONS
Date The date when the flow displayed in the Flow Process column was performed.
Time The time when the flow displayed in the Flow Process column was performed.
FIELD DESCRIPTIONS

SHIPPING
Looking Up Orders in LOOR
LINE BLOCK
The LOOR Line Block shows basically the same fields and details that appear in the original order’s ENOR 
Line Block. There are a few differences, however, which are noted below. 

LOOR screen showing the Line Block
This Shipped Date field is blank if the entire order has not been confirmed in Time-Stamp and Confirm Orders 
(CHOF) or the order line has not been confirmed individually in Confirm Orders - Lines (COOL). If the entire 
order was confirmed in CHOF, then all of the order’s Line Block records will have the same shipped date. This 
date is the same as in the Ship Date field of CHOF when the order was confirmed.
Flow Process The Flow Process column lists all of the flow processes that have been performed for this order at the time of viewing.
If the view icon is highlighted, you can click on the icon to view or print the 
document in PDF format.
If the e-File icon is highlighted, you can click on the icon to view and print the 
e-File or Signature Capture document.
Operator The operator who advanced the flow process.
FIELD DESCRIPTIONS
The date on which 
this line was confirmed.

SHIPPING
Looking Up Orders in LOOR
OPERATIONS 1 GUIDE 4.2 249
If only individual lines of the order were confirmed in COOL, then the confirmed lines will display a date in the 
Shipped Date field. This will be the same as in the Ship Date field of COOL when the line was confirmed. The 
order lines that have not yet been confirmed, will have a blank Shipped Date field.
OPTIONAL BLOCKS
The LOOR Optional Blocks show the same fields and details that appear in the original order’s ENOR 
Optional Blocks.
LOOKING UP AN ITEM SUMMARY
The item summary command allows you to look up a summary of all order lines by item rather than by order 
line. That is to say, if you have multiple order lines for the same item, the lines will be consolidated into a 
single line.
1 Retrieve the order that you wish to look up.
2 Click on Item Summary.
LOOR screen showing item summary
3 When you finish looking up your item summary, click on Order Header and Exit to exit.
CHANGING THE DEFAULT SORT SEQUENCE IN LOOR
The default sort sequence in LOOR is oldest order first, then second oldest order, followed by third oldest 
order, etc. You can change the default sort sequence to show the newest orders first by means of the Ctrl + A 
command.
1 Enter LOOR.
2 Query any order.
3 Press Ctrl + A. The message “Sequence will be descending” will display in the message area of your 
screen.
4 Perform your query. To retrieve all orders, leave all query fields blank.
NOTE Line Block details do not display for deleted orders.

SHIPPING
Printing the Shipping Documents
AccellosOne 3PL will retrieve your orders in descending sequence; that is, newest order first, then second newest order, followed by third newest order, etc.
Printing the Shipping Documents
Orders may have shipping documents attached to them. Each document is attached to a specific flow 
process that was set up in DIFP. After a flow process is selected and time-stamped in CHOF, the documents 
that are attached to this flow need to be printed before the system allows you to proceed to the next flow. You 
print these documents individually in PROM (Print Shipping Documents - Specific) or in a batch print through 
PROR (Print Shipping Documents - All).
Your company may have a system that is set up to start the allocation procedure when you print a specific 
document. (Allocation is the process of selecting and assigning specific inventory to the order.) You will need 
to consider whether you want to allocate at this point in time before you proceed with printing of the document 
that triggers allocation. Your system administrator will advise you in this matter.
PRINTING A DOCUMENT FOR SPECIFIC ORDERS IN PROM
You use PROM (Print Shipping Documents - Specific) to print the same document for specific order numbers 
that have been entered in ENOR. You can print for a single specific order (for example, Order Number 5 
needs its pick document printed) or for multiple specific orders (Order Numbers 1, 25 and 46 each need their 
pick document printed).
PROM consists of the following sections:
 Header Block
 Order Block
 Print Block
The Header Block in PROM lists all of the shipping documents. If you do not know which document to print at 
this point in the flow process sequence, you can check in LOOR. LOOR specifies the next document that 
needs to be printed in the field Document Status. 
The following example shows the steps required to process an order that has the outbound flow processes:
ENOR (Enter Order)
MANC (Manual Check)
PRBL (Print Bill of Lading)
COOR (Confirm Order)
FLOW 
PROCESS
ATTACHED 
DOCUMENTS REQUIRED ACTION
ENOR (Enter Order) Pick document a) Enter the order in ENOR
b) Print the Pick document in PROM
MANC (Manual Check) None Time stamp and confirm the MANC flow in CHOF 

SHIPPING
Printing the Shipping Documents
OPERATIONS 1 GUIDE 4.2 251
1 Enter PROM.
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document 
that you need to print — the document attached to the flow that was most recently processed in CHOF.

PROM screen showing the Header and Order Blocks
3 Click on Order Block.
4 Click on Create Record.
5 Key in the number of the order whose attached document you need to print and press Enter.
If there are other ENOR orders that need this same document printed, key in each order number and 
press Enter.
PRBL (Print Bill of Lading)Bill of Lading a) Time stamp and confirm the PRBL flow in 
CHOF
b) Print the Bill of Lading in PROM
COOR (Confirm Order) None a) Time stamp and confirm the COOR flow 
in CHOF
b) Execute Confirm
FLOW 
PROCESS
ATTACHED 
DOCUMENTS REQUIRED ACTION
List of shipping 
documents
Place the cursor 
next to the document that needs to 
be printed.

SHIPPING
Printing the Shipping Documents

PROM screen showing the Order Block
6 Click on Return to Main.
7 Click on Print Block.
8 Key in the code of the printer where this document is to print and press Enter. If you do not know the 
code, use the dropdown list.

PROM screen showing the Printer Block
9 Click Ok. The document will print and the system returns to the Main Menu.
The pick document that is 
attached to order 
numbers 4, 5 
and 6 will be 
printed.
Printer Code
Click on OK to 
print.

SHIPPING
Printing the Shipping Documents
OPERATIONS 1 GUIDE 4.2 253
PRINTING A DOCUMENT FOR ALL ORDERS IN PROR
You use PROR (Print Order Documents - All) to print the same document for all orders that are at the same 
stage in their flow process sequence and that need this document printed. 
You can also use PROR to print the same document for all orders that meet common criteria and that are at 
the same stage in their flow process. In this case, you use the Query Block to enter the selection criteria that 
the orders have in common. The system will then call up only these orders. For example, if you need to print 
the Pick document for all orders that were entered on June 23rd for Customer A, you would fill in the date and 
the customer fields accordingly and instruct the system to execute the query for these restrictions.
PROR consists of the following sections:
 Header Block
 Query Restriction Block
 Order Block
 Print Block
1 Enter PROR.

PROR screen showing the Header and Order Blocks
2 A list of documents appears. Use the up and down arrow keys to place the cursor next to the document 
that you need to print.
3 Click on Query Block.
List of shipping documents
Place the 
cursor next 
to the document that 
needs to be 
printed.

SHIPPING
Printing the Shipping Documents

PROR screen showing the Query Restriction Block
4 Do one of the following:
If you wish to print the document 
selected in the Header Block for 
all orders that are at this step in 
their flow process sequence: 
If you wish to only print the 
selected document in the Header 
Block for orders that are at this 
step in their flow process 
sequence and that also have 
common criteria:
a) Click on Execute Query.
b) Proceed to step 7.
a) Key in the common selection criteria.
In the Header 
Block, a document has 
already been 
selected for 
printing. Now 
you are in the 
Query 
Restriction 
Block.

SHIPPING
Printing the Shipping Documents
OPERATIONS 1 GUIDE 4.2 255

PROR screen showing the Order Block
5 Refer to the following table for further information on the common criteria that you can specify:
Completing this field . . .
will print the document selected in the 
Header Block for . . .
Customer Code all orders containing product belonging to this customer
Consignee Code all orders containing product to this consignee
Carrier Code all orders that were assigned this carrier for transporting 
product
Order Date - Start all orders that were created in ENOR with an Order Date 
starting from the date you specify here
Order Date - End all orders that were created in ENOR with an Order Date 
up to the date that you specify here
Ship Date - Start all orders that were shipped starting from the date that 
you specify here
Ship Date - End all orders that were shipped up to the date that you specify here
Arrive Date - Start all orders whose product is to arrive at the destination 
point starting from the date that you specify here
Arrive Date - End all orders whose product is to arrive at the destination 
point before the date that you specify here
If you click on Execute Query while you 
are in a blank Query 
Restriction Block, 
the system will display in the Order 
Block all orders that 
need the selected 
document printed 
according to their 
flow process 
sequence.

SHIPPING
Printing the Shipping Documents
6 Click on Execute Query. The system moves to the Order Block where it displays all orders that meet the 
selection criteria that you specified.
7 Click on Print Block.
8 Key in the code of the printer where these documents are to print and press Enter. If you do not know the 
code, use the dropdown list.
9 Click on Ok. The documents will print and the system returns to the Main Menu.
PRINTING A DOCUMENT FOR A SPECIFIC ORDER NUMBER 
You can also use PROR to produce the same result as PROM — that is, to print a shipping document for a 
specific order. If it is more convenient, you can use the following procedure rather than having to switch back 
and forth between the two programs.
1 In the Query Restriction Block, key in the specific order number in the Order Number field.
2 Click on Execute Query.
3 Click on Print Block.
4 Key in the printer code and press Enter.
Appointment Date - Start all orders that have an appointment date starting from the 
date that you specify here. This refers to appointments 
that are set up in the Appointment System — appointments scheduled at the warehouse doors for pick-up and 
delivery purposes.
Appointment Date - End all orders that have an appointment date up to the date 
that you specify here. This refers to appointments that 
are set up in the Appointment System — appointments 
scheduled at the warehouse doors for pickup and delivery purposes.
Type all orders that are of this ENOR Header Block order type
Priority all orders that have this priority code
Operator Code all orders that were entered by the operator that you 
specify here
Load Number the load number into which this order was grouped 
together for shipping
EDI Group Value the external group reference number used to group 
orders together for EDI tracking purposes. The field is 
automatically populated by EDI.
Batch Order Number the batch order number that you specify
Completing this field . . .
will print the document selected in the 
Header Block for . . .

SHIPPING
Confirming an Order
OPERATIONS 1 GUIDE 4.2 257
5 Click on Ok. The document will print and the system returns to the Main Menu.
Confirming an Order
After you successfully enter an order in ENOR, the ordered product still appears in LOEN (Look Up Inventory) 
as both “On Hand” and “On Order.” You must now confirm the order. Then the system will remove the ordered 
product from the inventory records in LOEN. 
Confirming an order will perform all of the following tasks:
 adds the name of the operator who performed the confirmation
 adds the time and date when confirmation was performed
 removes the order’s product units from inventory records
 may rate the order with any applicable outbound charges, if the system is set up to rate automatically
You confirm an order in the program Time-Stamp and Confirm Orders (CHOF). In this program, the system 
individually time-stamps and advances each of the order’s outbound flow processes. Documents that are 
attached to these flow processes must also be printed in a separate program before the system allows you to 
proceed to the next flow. 
TIME-STAMPING AND CONFIRMING ORDERS IN CHOF
Before you can confirm an order in CHOF, the following conditions must be met:
 all documents have been printed for the order
 all locations have been entered for each order line
1 Enter CHOF.
2 Key in the order number and press Enter. The system fills in the other fields as applicable. 
If the system does not populate any of the fields in the bottom half of the screen and there is a message 
in the Help Message Line, see “Troubleshooting Help for Confirming an Order” on page 260.
NOTE Advancing the flow of an order in CHOF is only required in a manual paperbased environment. In RF shipping, the flow is automatically advanced after each 
order line is picked, staged and loaded.

SHIPPING
Confirming an Order

CHOF screen
3 The cursor moves to the Next Flow Process Code field. Press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the 
appropriate code and click on Select. If there is only one option in the pick list, it is a mandatory flow process. Click on Select.
If there is more than one option in the pick list, the last selection — the one with the highest sequence 
number — is mandatory. The other options are non-mandatory. You can bypass a non-mandatory process flow by not selecting it in the pick list. Use the up and down arrow keys to move the cursor next to 
the flow process that you wish to select. Then click on Select.
4 Click on Select Flow. The data in the CHOF screen blanks out as the system advances to the next flow in 
the flow process sequence.
5 Do one of the following:
If the Next Flow Process Code 
field is COOR (Confirm Order):
If the Next Flow Process Code 
field is NOT COOR (Confirm 
Order):
a) Go to step 6. a) Key in the order number again 
and press Enter. 
b) Click on Select Flow. The data in 
the CHOF screen blanks out as 
the system advances to the next 
flow. 
c) Repeat until the Next Flow Process Code field displays COOR.
The current flow 
has already been 
time-stamped 
and advanced.
The next flow 
process will be 
time-stamped 
and advanced 
when you click on 
Select Flow.

SHIPPING
Confirming an Order
OPERATIONS 1 GUIDE 4.2 259

CHOF screen
6 When the Next Flow Process Code field displays COOR (Confirm Order), the system will populate the 
Ship Date field with the default date. Check that the default date is the correct date when the product for 
this order will be shipped. 
If you need a different date than the default, press Enter until the cursor is in the Ship Date field. Using 
the same date formatting, key in the applicable date over the existing one and press Enter.
7 Click on Select Flow.
Now that you 
have clicked 
on Select Flow 
the system 
advances 
again.
STPI becomes 
the current 
flow.
FIPI, the following flow 
process in the 
DIFP 

SHIPPING
Confirming an Order

CHOF screen
8 Do one of the following:
TROUBLESHOOTING HELP FOR CONFIRMING AN ORDER
If you receive any of the following messages in the Help Line, the following actions are required:
There are no more flow sequences for this order. 
The order has been either confirmed or deleted.
If you wish to confirm the 
order and exit CHOF:
If you wish to cancel the 
confirmation and exit CHOF 
If you wish to remain in CHOF 
to work on other orders:
a) Click on Exit. A message will 
appear indicating that the 
order is being confirmed.
a) Key in the same order number 
and press Enter.
b) Click on Order Number to exit.
a) Key in your next order number 
and press Enter.
b) If required, change the Ship 
date.
c) Click on Select Flow.
d) Repeat the above three steps 
for each additional order that 
you wish to confirm.
e) When you finish processing 
your orders, click on Confirm. 
A message will appear indicating that order 1 of xxx is being 
confirmed.
After you select 
the last flow, the 
CHOF screen 
becomes blank 
and the button 
Confirm displays 
as an option.

SHIPPING
Confirming an Order
OPERATIONS 1 GUIDE 4.2 261
1 Click on Exit to exit CHOF.
2 Enter LOOR. 
3 Key in the order number and click on Execute Query.
4 Check the Status field. 
5 Click on Exit.
There is at least one document to print for this order. 
1 Click on Exit to exit CHOF.
2 Enter PROM. Print the document(s) for this flow. See “Printing the Shipping Documents” on page 250 for 
further instructions.
3 Once the document(s) is printed, return to CHOF. Key in the order number and press Enter. Click on 
Select Flow and continue the procedure for confirming the order in the usual manner.
You cannot set this flow since this order does not have all locations entered.
1 Click on Exit to exit CHOF. 
2 Enter ENOR.
3 Click on Enter Criteria.
4 Key in the order number and click on Execute Query.
5 Click on Line Block.
6 Press Enter until the cursor is in the Location Code field.
7 Key in the location code and press Enter. Press the down arrow key to move to the next Line Block 
record. Repeat this step as many times as necessary until you have entered the Location Code into all of 
the Lines.
8 Click on Exit.
9 Enter CHOF. Key in the order number and press Enter. Click on Select Flow and continue the procedure 
for confirming the order.
CONFIRMING ORDERS ONE LINE AT A TIME IN COOL
As you are advancing and time-stamping the outbound flow processes of an order in the program CHOF, you 
have two choices when you reach the mandatory flow process COOR (Confirm Order). If you wish to confirm 
the entire order, select the COOR flow process in CHOF (see “Time-Stamping and Confirming Orders in 
CHOF” on page 257). If you wish to only confirm specific lines of the order, you use the program Confirm 
Orders - Lines (COOL).
The following conditions must be met before you can confirm an order line in COOL:
 the line or lines that you wish to confirm must be fully allocated
 the line or lines must be at the flow immediately preceding the flow COOR (Confirm Order) unless the 
flow immediately preceding COOR is defined as non-mandatory in DIFP
 all documents attached to any flow before COOR must be printed.
EXAMPLE
If your outbound flows are ENOR, FLOW1, FLOW2, FLOW3 and COOR and if FLOW3 is 
defined as mandatory in DIFP, the line or lines must be at FLOW3. If FLOW3 is not 
mandatory, the line or lines must be at FLOW2.
1 Enter COOL. 

SHIPPING
Confirming an Order
2 Click on Create Record.
3 Key in your order number and press Enter.
4 Key in the line number and press Enter twice. “Confirm” displays under the order number and the Ship 
Date Block appears at the bottom of the screen.

COOL screen
5 Click on Return to Main.
6 Click on Ship Date. In the Ship Date field, you enter the date on which this order line’s product will be 
shipped out of the warehouse. If the ship date is the same as the default, press Enter. (The default is the 
current company date of your system.)
If you need a different ship date than the default, key in the applicable date and press Enter. 
7 If you need to confirm another order line, click on Master Block. click on Create Record and repeat steps 
3 to 6.
Confirm appears 
under the order 
number.
The Ship Date 
Block displays.

SHIPPING
Confirming an Order
OPERATIONS 1 GUIDE 4.2 263

COOL screen
8 When you have finished entering all the lines that need to be confirmed, click on Confirm. A message will 
display on your screen indicating that the line(s) are being confirmed.
CHECKING CONFIRMED LINES IN LOOR
You can check that the individual lines entered in COOL have been confirmed. You do so in the program Look 
Up Orders (LOOR).
Although individual lines of the order have been confirmed, the order’s status will not display as confirmed in 
LOOR. The order still has remaining lines that have not yet been confirmed. Once all lines are confirmed, 
then the order’s status will show as confirmed.
1 Enter LOOR. 
2 Key in the order number and click on Execute Query.
3 Click on Line Block. 
4 Use the up or down arrow keys to scroll to the line record that you confirmed in COOL. 
Click on 
Confirm to 
confirm the 
line(s).

SHIPPING
Confirming an Order

LOOR screen showing an order with a line that was confirmed in COOL
5 If the Shipped Date field is completed, you know that the line is confirmed. Click on Master Block and Exit 
to exit the program.
If the Shipped Date field is blank, the line was not confirmed.
6 Click on Master Block and Exit to exit LOOR. Enter COOL and re-enter the line.
To print the documents attached to your system’s flow processes, proceed to “Printing the Shipping 
Documents” on page 250.
CHANGING THE CONFIRMATION DATE IN CHCD
You can change the confirmation date of a confirmed order in CHCD (Change Confirmation Date).
1 Enter CHCD.
Order status
The Shipped 
Date shows 
the date on 
which line 2 
was confirmed.

SHIPPING
Confirming an Order
OPERATIONS 1 GUIDE 4.2 265

CHCD screen
2 Press Enter to accept O (Order) as your document type.
3 Key in your order number and press Enter.
4 Click on Change Block.

CHCD screen showing prompt for new confirmation date
5 Key in your new confirmation date and press Enter.
6 Click on Process Change.
7 If required, key in any remarks for the change in confirmation date. When you finish entering your 
remarks (if any), click on Return.
8 Click on Exit.

SHIPPING
Generating the VICS Bill of Lading
Generating the VICS Bill of Lading
You generate the VICS bill of lading in VBOL (VICS Bill of Lading). This program allows you to consolidate 
one or more orders belonging to the same customer and generate a VICS bill of lading. There are a number 
of options for attaching orders to a VICS bill of lading: you can attach individual orders, a range of orders, a 
batch order created in GEBA or COPI, or all orders assigned a given load number. You can also specify order 
restrictions such as order date, ship date, arrive date and appointment date.
Once a VICS bill of lading is created, new orders can be added to it and existing orders removed from it at 
any time until the bill of lading is confirmed. Confirmed bills of lading are closed and cannot be modified.
The VICS bill of lading is restricted to orders belonging to the same customer.
CREATING A NEW BILL OF LADING
1 Enter VBOL

VBOL screen
2 Click on Create Record.
3 Key in your customer code and press Enter or select your customer code from the pick list.
4 In the Arrive Date field, press Enter to accept the current date as your arrive date or key in a new arrive 
date and press Enter.
5 Key in your consignee code and press Enter or select your consignee code from the pick list.
6 Key in your carrier code and press Enter or select your carrier code from the pick list.
7 If required, key in your SID reference information and press Enter. If you do not require SID reference 
information, press Enter without entering anything to bypass this field.

SHIPPING
Generating the VICS Bill of Lading
OPERATIONS 1 GUIDE 4.2 267
8 If required, key in your CID reference information and press Enter. If you do not require CID reference 
information, press Enter without entering anything in this field.
9 If required, key in your reference 1/2 information and press Enter.
10 In the Trailer Number field, key in your trailer number and press Enter. If you do not require a trailer number, press Enter without entering a number to bypass this field.
11 In the Seal Number field, key in your seal number and press Enter. If you do not require a seal number, 
press Enter without entering a number to bypass this field.
12 In the Probill Number field, key in your probill number and press Enter. If you do not require a probill number, press Enter without entering a number to bypass this field.
13 In the FOB field, press Enter to accept the default value of N for No or key in Y for Yes and press Enter.
14 Proceed to select the appropriate freight terms:
15 In the Remarks field, do one of the following:
If the shipment is prepaid: If the shipment is collect:
If the shipment is to be billed 
to a third party:
a) In the Prepaid field, key in Y
for Yes and press Enter.
a) Press Enter to bypass the Prepaid field.
b) In the Collect field, key in Y for 
Yes and press Enter.
a) Press Enter twice to bypass 
the Prepaid and Collect fields.
b) In the 3rd Party field, key in Y
for Yes and press Enter.
c) Key in the name of the third 
party.
d) Key in the street address of 
the third party.
e) Key in the city, state or province and ZIP/postal code of 
the third party.
If you wish to add remarks to the 
bill of lading:
If you do NOT wish to add 
remarks to the bill of lading:
a) Key in Y for Yes and press Enter. a) Key in N for No and press Enter.

SHIPPING
Generating the VICS Bill of Lading
16 In the Commodity field, do one of the following:
17 If you entered Y for Yes in the Remarks field, key in your remarks. When you finish entering your 
remarks, click on Master Block.

Commodity Block of VBOL
18 If you entered Y for Yes in the Commodity field, proceed to enter your commodity information. When you 
finish, click on Return to Main.
19 Click on Order Block.
20 Click on Query Block.
If you wish to add commodity 
information to the bill of lading:
If you do NOT wish to add 
commodity information to the bill 
of lading:
a) Key in Y for Yes and press Enter. a) Key in N for No and press Enter.

SHIPPING
Generating the VICS Bill of Lading
OPERATIONS 1 GUIDE 4.2 269

Query Restriction Block
21 Proceed to enter your query restrictions. You can query by order number range, batch order number, 
load number, customer order number, purchase order number or date range. When you finish entering 
your query restrictions, click on Execute Query.

SHIPPING
Generating the VICS Bill of Lading

Order Block of VBOL showing all orders attached to a given bill of lading
22 Click on Master Block to exit the Order Block.
23 Click on Exit to exit VBOL.
LOOKING UP A BILL OF LADING
1 Enter VBOL.
2 Click on Enter Criteria.
3 Key in your search criteria such as VICS bill of lading number, customer code, consignee code, carrier 
code, etc. When you finish entering your search criteria, click on Execute Query.
4 If you wish to look up a bill of lading’s remarks, 3rd party details or commodity information, press Enter 
until your cursor is positioned in the 3rd Party, Remarks or Commodity field and press F3. When you finish looking up your remarks, 3rd party details or commodity information, press F4 to exit.
5 When you finish looking up your bill of lading, click on Return to Main and Exit to exit.
FIELD DESCRIPTIONS
VICS Sequence Number The VICS sequence number. This number is generated in sequential order by 
AccellosOne 3PL.
VICS BOL Number The full VICS bill of lading number. This number consists of the VICS 
sequence number plus the EAN UCC prefix plus a check digit.
Counter in Order 
Block showing 
currently selected 
record plus total 
number of records

SHIPPING
Generating the VICS Bill of Lading
OPERATIONS 1 GUIDE 4.2 271
Customer Code The shipment’s customer.
EAN UCC Prefix The customer’s EAN UCC prefix.
To Arrive Date The shipment’s to arrive date.
Consignee Code The shipment’s consignee.
Carrier Code The shipment’s carrier.
SCAC Code The carrier’s SCAC code.
SID Reference The shipment’s SID reference information.
CID Reference The consignee’s CID reference information.
Reference 1/2 The shipment’s extra reference number 1/2.
Trailer Number The shipment’s trailer number.
Seal Number The shipment’s seal number.
Probill Number The shipment’s probill number.
Total Units The total number of units of all orders on the bill of lading.
Total Weight The total weight of all orders on the bill of lading.
Pallet/Slip The pallet/slip flag (either Yes or No). This feature requires a customized document from HighJump.
FOB If the shipment is “Free on Board”, this field will be set to Y for Yes.
Prepaid If the shipment is prepaid, this field will be set to Y for Yes.
Collect If the shipment is collect, this field will be set to Y for Yes.
3rd Party If the shipment is to be billed to a third party, this field will be set to Y for Yes.
Remarks If there are miscellaneous remarks attached to the bill of lading, this field will 
be set to Y for Yes.
Commodity If there is commodity information attached to the bill of lading, this field will be 
set to Y for Yes.
FIELD DESCRIPTIONS

SHIPPING
Generating the VICS Bill of Lading
PRINTING A BILL OF LADING
You can print a bill of lading as many times as required as long as the orders on it are active; that is, neither 
deleted nor confirmed.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to print.
3 Click on Print Block.
Status A = Active
C = Closed
The bill of lading’s status.
Date Created The date that the bill of lading was created.
Date Closed The date that the bill of lading was either confirmed or deleted.
Last Printed Date The date that the bill of lading was last printed.
Printed By The operator who last printed the bill of lading.
Print Count The total number of times that the bill of lading has been printed.
FIELD DESCRIPTIONS

SHIPPING
Generating the VICS Bill of Lading
OPERATIONS 1 GUIDE 4.2 273

VBOL screen showing Select Printer window
4 Key in the code of the printer where the bill of lading is to print and press Enter. If you do not know the 
code, use the dropdown list.
5 Click Ok to send the document to the printer.
6 Click on Exit to exit.
MODIFYING THE ORDERS ON A BILL OF LADING
You can add orders to and remove orders from a VICS bill of lading at any time as long as the following conditions are met:
 the order is unconfirmed
 the bill of lading itself is unconfirmed
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to modify.
3 Press Enter to position your cursor in the To Arrive Date field, then click on Order Block.

SHIPPING
Generating the VICS Bill of Lading

Order Block of VBOL
4 Do one of the following:
5 Click on Master Block and Exit to exit.
CONFIRMING A BILL OF LADING
When you confirm a bill of lading, the bill of lading is considered closed and cannot be modified. Confirming a 
bill of lading does not change the status of the orders on it; open orders remain open and confirmed orders 
remain confirmed.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to confirm.
3 Press Enter to position your cursor in the To Arrive Date field.
4 Click on Confirm/Delete.
5 When prompted to proceed with the confirmation, click on Yes.
6 Click on Exit to exit.
If you wish to delete all orders 
on the bill of lading:
If you wish to delete selected 
orders on the 
bill of lading:
If you wish to add orders to the 
bill of lading:
a) Click on Delete All.
b) When prompted to confirm the 
deletion, click on Yes.
a) Use your arrow keys to position your cursor over the order 
to be deleted and click on 
Delete One.
a) Click on Query Block.
b) Key in your query criteria and 
click on Execute Query.

SHIPPING
Generating the VICS Bill of Lading
OPERATIONS 1 GUIDE 4.2 275
DELETING A BILL OF LADING
If you wish to delete a bill of lading, you must first remove any orders attached to it. Then you use the Confirm/
Delete command in VBOL.
1 Enter VBOL.
2 Retrieve the bill of lading that you wish to delete.
3 Enter the Order Block and remove any orders attached to the bill of lading.
4 Proceed to confirm the bill of lading in the normal manner.
CONFIRMING ALL ORDERS ON A BILL OF LADING IN CHOF
You can confirm all orders on a bill of lading by specifying the VICS sequence number in the field of the same 
name in CHOF. When you confirm by VICS sequence number, all orders on the bill of lading are automatically 
confirmed. This option is not available if the order has been assigned to a load; orders assigned to a load can 
only be confirmed individually or by load number.
When you confirm orders by VICS sequence number in CHOF, the normal conditions for confirming an order 
must be met:
 all documents have been printed for each order
 all locations have been entered for each order line
1 Enter CHOF.
2 Press Enter to position your cursor in the VICS Sequence Number field.
3 Key in your VICS sequence number and press Enter.

CHOF screen showing confirmation by bill of lading number

SHIPPING
Cancelling or Reprinting Order Documents
4 Proceed to confirm the orders on the bill of lading normally in CHOF.
Cancelling or Reprinting Order Documents
Normally, order documents are printed according to the flow process sequence. The program Requeue Order 
Documents (REOR)) allows you to print an order document out of sequence under certain circumstances.
You use the program REOR when you have to:
 cancel the printing of a document that is attached to a flow process
 reprint a document that is attached to a flow process
When you enter an order number into REOR, the program indicates the following information:
 the orders’s current flow process status
 the document attached to this flow process
 the number of times that this document has been printed to date
 the print status of this document. 
REOR screen
In REOR, the print statuses for documents are:
 all documents have been printed
 to be printed
 printed
 cancel
 requeue
The last flow process that was 
completed for 
this order up to 
this time.
Document 
attached to this 
flow process
Number of times 
that this document has been 
printed.
Print status of 
this document

SHIPPING
Cancelling or Reprinting Order Documents
OPERATIONS 1 GUIDE 4.2 277
Depending on the document print status, you have the option of cancelling the printing of the document or 
reprinting it as necessary. The following table shows the options that are available depending on the 
document status.
CANCELLING ORDER DOCUMENTS IN REOR 
There may be times when you need to cancel the printing of a document that is attached to a flow process. 
This would occur, for example, if you need to advance to the next flow without printing the document that is 
attached to the current flow (the flow that was most recently confirmed in CHOF).
Use the following procedure when the REOR Print Status field indicates “To be printed” and you need to 
cancel the printing of that document.
1 Enter REOR.
2 Key in the order number and press Enter. The system displays the documents that are attached to this 
order’s current flow process.
3 Check that the print status indicates “To be printed.” If there is more than one document, use the up and 
down arrow keys to place the cursor beside the document that you wish to cancel.
4 Click on Cancel. 
Print Status Description Options 
All documents have been 
printed
The order has been confirmed. All process 
flows have been completed and all their 
attached documents have been printed. There 
are no remaining documents to either requeue 
(reprint) or cancel. 
None.
The Help Message Line displays “This order has no 
documents to be requeued or cancelled.”
To be printed The displayed document needs to be printed 
now according to the flow process sequence.
Click on Cancel to cancel printing of this document. 
This will allow the system to advance to the next flow 
process without printing of the displayed document.
If you want to print the document, exit REOR and 
Enter PROM to print the attached document.
Printed The displayed document has been printed 
before.
Click on Requeue to reprint this document. 

SHIPPING
Cancelling or Reprinting Order Documents

REOR screen
5 Click on Order Number and Exit to exit the program REOR.
6 Enter CHOF. In CHOF, the system will now allow you to select the next flow process in the sequence. 
Continue confirming the order in the usual manner.
REPRINTING ORDER DOCUMENTS IN REOR
You may need to reprint a document that is attached to a flow process. For example, you need to replace a 
lost or damaged document or you need a duplicate for whatever reason. 
Use the following procedure when the REOR Print Status field indicates “Printed” and you need to reprint the 
attached document.
1 Enter REOR 
2 Key in the order number and press Enter. The system displays the documents that are attached to this 
order’s current flow process.
3 Check that the print status indicates “Printed.” If there is more than one document listed, use the up and 
down arrow keys to place the cursor beside the document that you need to reprint.
NOTE Depending on your system setup, some documents cannot be reprinted. 
The system will only allow you to reprint documents that have the Flag Reprint field 
set up to Y in the program DOCU.
The second 
function key 
button toggles between 
the “Cancel” 
and 
“Requeue” 
options.
Set the print 
status to 
“Cancel”.
Printing of the 
PICK is no 
longer needed 
and the system will allow 
you to 
advance to 
the next flow.

SHIPPING
Cancelling or Reprinting Order Documents
OPERATIONS 1 GUIDE 4.2 279

REOR screen
4 Click on Requeue.
5 If the message “Print all order lines or new lines only” appears, do one of the following:
If you wish to print all order lines:
If you wish to print only order 
lines added after the last printing 
of the document:
a) Click on All Lines. a) Click on New Lines Only.
The pick 
document 
has been 
printed once 
before.
Requeue is 
available as 
a reprinting 
option.

SHIPPING
Cancelling or Reprinting Order Documents

REOR screen
6 Click on Order Number and Exit to exit the REOR program. 
7 Enter PROM and reprint the document.
REQUEUING A RANGE OF ORDER DOCUMENTS IN RERO
You can requeue a range of order documents in RERO (Requeue a Range of Orders). You requeue order 
documents when you wish to print or reprint order documents that have been cancelled.
1 Enter RERO.
2 Key in your starting order number and press Enter. If you wish to requeue all order documents, you can 
set your starting order number to zero.
3 Key in your ending order number and press Enter.
4 Key in your document code and press Enter or use the pick list function to select it.
Clicking on 
Requeue 
changes the print 
status and the 
pick document is 
now set to 
requeue 
(reprint).

SHIPPING
Cancelling or Reprinting Order Documents
OPERATIONS 1 GUIDE 4.2 281

RERO screen
5 Click on Process.
6 If auto-processing is activated for the document, you will be prompted to start auto-processing each 
order document. If you enter Y for Yes, the document will auto-print. If you enter N for No, no auto-printing will occur and you will have to print the document in PROM or PROR. 
REPRINTING SHIPPING LABELS IN RELA
You use the program RELA (Reprint Labels) to reprint AccellosOne 3PL’s standard shipping label. RELA is a 
general purpose reprint program that is more flexible than PROR or PROM. It allows you to reprint labels for 
a specific line of an order, to specify the number of copies to be reprinted and to reprint at any flow.
RELA prints one label for each pallet; pallets are defined at the detail line level according to the item’s quantity 
breakdown profile. For example, if your standard quantity breakdown is 10 cases per pallet and your order 
line quantity is 35 cases, RELA will print four labels — one for each of the three full pallets and one for the 
partial pallet of five cases.
1 Enter RELA.
2 Key in your document code and press Enter or use your pick list to select it.
3 Key in O for Order as your document type.
4 Key in your order number and press Enter.
5 If you are reprinting an outbound pallet ID label, select the appropriate pallet ID from the dropdown list.
6 If required, key in your line number and press Enter.

SHIPPING
Inspection Orders

RELA screen
7 In the Number of Labels field, key in the number of extra labels that you require and press Enter.
8 When the Printer Block appears, key in the code of the printer where these labels are to print and press 
Enter. If you do not know the code, use the dropdown list.
9 Click Ok. The labels will print and the system returns to the Main Menu.
Inspection Orders
You use inspection orders when you need to retrieve product from inventory for a government inspection. If all 
product passes the inspection, the inspection order is confirmed with a ship quantity of zero. If product is 
damaged and does not pass the inspection, the inspection order is confirmed with a shipped quantity equal to 
the quantity of product that was destroyed.
Inspection orders are similar to R-type order lines. That means that if you do not enter all inventory levels in 
ENOR, AccellosOne 3PL will automatically select the appropriate values during order entry.
1 Create a dummy consignee in CONS for government inspections. For example, create a code called 
INSP.

SHIPPING
Inspection Orders
OPERATIONS 1 GUIDE 4.2 283

Dummy consignee in CONS called INS
2 Enter ENOR
3 In the Customer Code field, key in the code of the customer whose product you are inspecting and press 
F9.
4 In the Order Type field, key in I for Inspection and press Enter.
5 Press Enter to bypass the Customer Code field.
6 Proceed to enter the order header in the normal manner. The consignee should be the dummy consignee that you created in CONS for inspection orders.
7 In the Line Block, enter the product that you wish to inspect. 

SHIPPING
Distribution Orders

Line Block of ENOR showing five cases of product A1 being inspected
8 Do one of the following: 
Distribution Orders
You use a D (Distribution) type order to cross dock and to ship an item at the same time. For example, you 
need to fill an order with product that has just arrived at the warehouse. However, this product has not been 
received into the system through ENRE. In this situation, you use a D type order, which allows you to receive 
and to ship out at the same time.
You create a D type order in which you record the details of the product that you are shipping out. The system 
takes the information from the order that you create and uses it to automatically generate a mirror image 
receipt.
If all the product passes the 
inspection:
If some of the product is 
damaged and does not pass the 
inspection:
a) Change the to ship quantity to 
zero and confirm the order in 
CHOF in the normal manner.
a) Change the to ship quantity to 
the quantity of product that must 
be destroyed and confirm the 
order in CHOF in the normal 
manner.

SHIPPING
Distribution Orders
OPERATIONS 1 GUIDE 4.2 285
You create only one record — a Distribution Order type but the system generates two records:
 a Distribution Order type recording the process of shipping the product out of the warehouse
 a receipt recording the process of receiving the product into the warehouse and the order records
SETTING UP DISTRIBUTION ORDERS
Distribution orders require shipping lanes and shipping lane assignments. You set up your shipping lanes in 
SHLA. Shipping lanes must be attached to a staging location.
SHLA screen
You set up your shipping lane assignments in SLAS. In SLAS you assign your consignees to shipping lanes. 
A consignee can be assigned to only one shipping lane, but the same shipping lane can contain multiple 
consignees.
NOTE You can only use a Distribution Order if the entity has been received into the 
system on previous occasions. For example, your system has previously received the 
entities Item A, Lot 1 and Item A, Lot 2. The system would allow you to create a Distribution Order for Lot 1 or Lot 2.
Now, a new entity Item A, Lot 3 has just arrived at the warehouse and you would like 
to ship it out as a Distribution Order. The system would not allow you to do this, as it 
does not recognize an entity that has never been entered into the system before.

SHIPPING
Distribution Orders
SLAS screen
You can override your shipping lane assignments in ENOR.
ENTERING A DISTRIBUTION ORDER IN ENOR
1 Enter ENOR.
2 Key in your customer code and press F9 (Previous Field) to move the cursor to the Type field. 
3 Key in D for Distribution and press Enter.
4 Complete the ENOR Header Block in the normal manner. In the Shipping Lane Code field, you can override your shipping lane assignment set up in SLAS.
5 In the Line Block, leave the Type field with the D that is generated by the system.

ENOR Line Block for a distribution order
You must complete all inventory 
levels for the 
entity.

SHIPPING
Distribution Orders
OPERATIONS 1 GUIDE 4.2 287
6 Complete the Line Block in the normal manner. You must enter all inventory level fields for the entity that 
you are shipping. A pick list is available for each of the inventory level fields, if you need to use it.
7 When you have completed all lines for this order, click on Master Block to return to the order’s Header 
Block screen.
8 Click on Exit to exit the program. A Message Block will appear on the screen listing the number of this 
distribution order and the number of the corresponding receipt that the system generated.

Transferring message
CONFIRMING A DISTRIBUTION ORDER
1 Enter CHOF.
2 Confirm the order in CHOF in the normal manner.
If necessary, enter REOR to cancel the printing of documents attached to the outbound flows of this order 
and then return to CHOF.
3 In CHOF, after you click Execute Confirm, a Message Block will appear on the screen requesting a location code and a warehouse code.

CHOF screen showing prompt for location and warehouse

SHIPPING
Distribution Orders
4 Key in your location code for the cross-dock product and press Enter. If you do not know the code, use 
the pick list and then press Enter. (This transaction will not affect Location Block inventory records in 
LOEN since the product was not actually received nor stored in a warehouse location — it was only cross 
docked.)

CHOF screen showing location and warehouse for cross-dock product
5 Press Enter to accept the system-generated Warehouse Code. If the Warehouse Code field is blank, key 
in the warehouse code for the location that you entered in the previous step and press Enter.
The confirmation Message Box appears on the screen. Both the distribution order and the corresponding 
receipt are being confirmed. The screen blanks out. 
6 Click on Exit to exit CHOF.
You can now go into LOOR to view the details of this Distribution Order and into LORE to view the details of 
the corresponding receipt. Both should be confirmed.
LOOKING UP A DISTRIBUTION ORDER
1 Enter LOOR.
2 In the Order Number field, key in the number of the Distribution Order.
3 Click on Execute Query. The order will display on the screen.

SHIPPING
Distribution Orders
OPERATIONS 1 GUIDE 4.2 289

LOOR screen showing details of a distribution order
4 Note the Transfer Receipt field. This displays the number of the mirror image receipt that the system created and that corresponds to the Distribution Order. 
5 Click on Exit to exit LOOR.
6 Enter LORE. In the Receipt Number field, key in the corresponding Receipt Number.
7 Click Execute Query.
corresponding 
receipt number
distribution 
order number

SHIPPING
Transfer Orders

LORE screen showing receipt that corresponds to a distribution order
8 Note the On Order(s) field, which displays the number of the distribution order.
9 Click on Exit to exit LORE.
Transfer Orders
You use a transfer order to transfer product from one warehouse customer to another. For example, two 
warehouse customers have an identical item in common. Customer A is running low on the product and asks 
Customer B for a specified amount. 
The product is not being shipped out; it is only having its ownership transferred from one customer to another. 
To record the change, you create a transfer order. When you confirm the transfer order, AccellosOne 3PL will 
automatically create a confirmed receipt in the name of the new owner.

SHIPPING
Transfer Orders
OPERATIONS 1 GUIDE 4.2 291
If the product being transferred has process values such as catch weights or serial numbers attached to it, the 
process values will be transferred as well provided that both the from item and the to item have the same item 
process code(s) defined in IPRO (the item process profiles defined in IPRP need not be the same).
SETTING UP TRANSFER ORDERS
You set up transfer orders by creating a transfer profile in TRPR (Transfer Profile). In this profile, you define 
the charges, if any, associated with the transfer, the renewal date for transferred product and the document, if 
any, that will be printed when product is transferred. The profile that you create in TRPR must be attached to 
all customers who wish to transfer product among each other.
In order to perform a transfer, several additional conditions apply at the customer level:
 both customers track product in the same way (i.e., they have the same number of SKU’s in their quantity breakdown profiles — pallets/cases, etc.)
 both customers have the same number of inventory levels defined in DILP though not necessarily the 
same inventory terminology code (for example, an item/lot/pallet ID customer can transfer product to an 
item/date/pallet ID customer)
Further conditions apply at the item level:
 both items have the same item code
 both items have the same weight type
 if customers calculate expiry dates by means of a formula in ITSH, both customers must use the same 
formula and the ITSH profile(s) containing this formula must be attached to the appropriate items
NOTE If you wish to transfer product from one customer to another to correct an 
error in your inventory records — that is, there is no change in ownership because 
customer A is transferring inventory to customer B — you enter a transfer adjustment 
in ENAJ.
FIELD DESCRIPTIONS
Transfer Profile Code Mandatory
Your transfer profile code.
Description Mandatory
Your description for this code.

SHIPPING
Transfer Orders
Receipt Charge Type N = None
H = Handling
S = Storage
R = Regular
If you set this flag to None, there are no charges. If you set this flag to Handling, transferee pays handling only (that is, charges set up in IHAP). If you set 
this flag to Storage, transferee pays initial storage only (that is, charges set up 
in IISP). If you set this flag to Regular, transferee pays all charges associated 
with a regular receipt (that is, charges set up in IHAP and IISP).
Renewal Type O = Original Date
R = Receipt Date
EXAMPLE
Customer A (transferor) received product on August 10. Product was transferred to Customer B (transferee) on August 20.
Scenario 1 (Both customers have anniversary monthly billing)
If you set this flag to O for Original Date, product renews on September 10 
and Customer B will pay all charges from this date on. The next renewal date 
will be October 10. If you set this flag to R for Receipt Date, Customer B will 
start paying on August 20 and product renews on September 20.
Scenario 2 (Customer A is on anniversary monthly billing and Customer B is 
on monthly first of month billing)
If you set this flag to O for Original Date, product renews on September 10 
and Customer B will pay all charges from this date on. The next renewal date 
will October 1. If you set this flag to R for Receipt Date, Customer B will start 
paying on September 1 and product renews on October 1.
Scenario 3 (Customer A is on anniversary monthly billing and Customer B is 
on anniversary weekly billing)
If you set this flag to O for Original Date, product renews on September 10 
and Customer B will pay all charges from this date on. The next renewal date 
will be September 17. If you set this flag to R for Receipt Date, Customer B will 
start paying on August 27 and product renews on September 3.
FIELD DESCRIPTIONS

SHIPPING
Transfer Orders
OPERATIONS 1 GUIDE 4.2 293
Scenario 4 (Customer A is on anniversary monthly billing and Customer B is 
on anniversary weekly billing for first period and then anniversary monthly billing for subsequent periods)
If you set this flag to O for Original Date, product renews on September 10 
and Customer B will pay all charges from this date on. The next renewal date 
will be October 10. If you set this flag to R for Receipt Date, Customer B will 
start paying on August 27 and product renews on September 27.
Document Code (DOCU) Optional
The document, if any, that you wish to print for each transfer. This document 
will print instead of any documents attached to the flow ENRE in the transferee’s workflow profile defined in DIFP. 
If you do not enter a document code in this field, AccellosOne 3PL will print 
the document or documents defined in the transferee’s DIFP profile for the 
flow CORE. Any documents attached to earlier flows such as ENRE will not 
be printable.
You enter a document code in this field when you wish to print an additional
receiving document that is not attached to the transferee’s workflow profile at 
the CORE flow.
Extra Charge Profile 
Code (ECHP)
Optional
The extra charge profile code for the charges, if any, for the transfer itself 
excluding any normal receipt, storage or handling charges. These charges 
can apply to either the transferor or transferee.
Free Storage for TransfereeIf you select this checkbox, you can define a free storage period for the transferee in a transfer order. That is, although the transferee now owns the product, the transferor pays renewal storage.
Free Days for Transferee Only available if Free Storage for Transferee checkbox is selected
The number of free days for the transferee paid for by the transferor.
FIELD DESCRIPTIONS

SHIPPING
Transfer Orders
1 Enter TRPR.
2 Click on New .
3 Key in a transfer profile code and press Enter. Then key in a meaningful description and press Enter 
again.
4 Key in the appropriate receipt charge type (N for None, H for Handling Only, S for Storage Only or R for 
Regular) and press Enter.
5 Key in the appropriate renewal type (O for Original Date or R for Receipt Date) and press Enter.
6 If you wish to print a particular document for each transfer, key in your document code and press Enter or 
select it using the pick list. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the 
appropriate code and click on Select.
7 In the Extra Charge Profile Code field, key in your extra charge code and press Enter or press Enter with 
the field blank to bypass this option.
8 If you wish to set up a free days storage period for the transferee, click on the Free Storage for Transferee checkbox and press Enter. Then key in the number of free days in the Free Days for Transferee 
field and press Enter. Next select the appropriate charge code from the Charge Code for Transferee Free 
Days pick list. Lastly, select the appropriate free days charge type from the dropdown list (Daily or Balance).
Charge Code for Transferee Free Days
Only available if Free Storage for Transferee checkbox is selected
The charge code used to calculate charges for the transferor during the free 
days period. The transferor’s rates will apply to this charge; not the transferee’s.
Free Days Charge Type Balance
Daily
If you select Balance, a single charge will be generated based on the balance 
of inventory still in the warehouse at the end of the free days period. If you 
select Daily, a charge will be created for each day in the free days period 
based on the balance of inventory at the end of each day.
FIELD DESCRIPTIONS

SHIPPING
Transfer Orders
OPERATIONS 1 GUIDE 4.2 295

Transfer Profile
9 When you finish setting up your transfer profile, click on Save to save your changes.
10 Click on Exit to exit TRPR.
11 Attach your new profile to all customers who wish to transfer product among each other.
ENTERING A TRANSFER ORDER
1 Enter ENOR
2 In the Customer Code field, key in the code of the customer from whom you are transferring product and 
press F9.
3 In the Order Type field, key in T for Transfer and press Enter.
4 Press Enter to bypass the Customer Code field.
5 In the Consignee Code field, key in the code of the customer to whom you are transferring product and 
press Enter.
6 Key in your same-type code for your sold-to code and press Enter.
7 Press Enter the required number of times to bypass the Order Date, To Ship Date and To Arrive Date 
fields.
8 If required, enter your customer order number or purchase order number.
9 In the Carrier Code field, key in your N/A code and press Enter.
10 In the Freight Term field, use your pick list to select the NA (Not Applicable) code.

SHIPPING
Transfer Orders
11 Complete the rest of the Header Block fields in the normal manner as if you were entering an R-type 
order.

ENOR screen showing a transfer order
12 In the Line Block, leave the Type field with the T that is generated by the system. 
13 Complete the rest of the Line Block fields in the normal manner as you would for an R type order until you 
reach the Inventory Level fields.
14 In the Inventory Level fields, do one of the following:
15 In the Ordered Quantity field, key in the amount and SKU that is being transferred and press Enter.
If you wish to transfer a specific 
inventory entity:
If you wish to transfer multiple 
inventory entities (for example all 
lots belonging to a specific item 
or all pallet ID’s belonging to a 
specific lot):
a) Enter all inventory levels. a) Enter your item code only and 
leave the lot field blank (scenario 
one) or enter your item code and 
lot number only and leave the 
pallet ID field blank (scenario 
two).
Order type = T for 
Transfer

SHIPPING
Transfer Orders
OPERATIONS 1 GUIDE 4.2 297

ENOR screen showing a transfer order
16 Complete the remaining Line Block fields in the normal manner. 
17 When you have finished entering all lines for this order, click on Return to Main. 
18 Note the order number and then click on Master Block and Exit.
19 Advance the flows of the order in CHOF and print any required documents.
You are now ready to confirm the transfer order and to print its attached documents.
CONFIRMING A TRANSFER ORDER
1 Enter CHOF.
2 Key in the transfer order number and press Enter.
3 Click on Select Flow for the flow COOR (Confirm Order).
4 Click on Exit to exit CHOF. 
A message box will appear on the screen to indicate that the order is being confirmed.
A second message box will then display indicating the corresponding receipt number.

CHOF screen showing the corresponding receipt number for the transfer order
Key in the amount 
that is to be transferred to another 
customer.

SHIPPING
Transfer Orders
The order has been confirmed and you can now look up the transfer order in LOOR.
LOOKING UP A TRANSFER ORDER 
1 Enter LOOR.
2 Key in the order number in the Order Number field.
3 Click on Execute Query.

LOOR screen showing a transfer type order
4 When you have finished viewing the details of this order, click on Exit to exit LOOR.
5 Enter LORE
6 Key in the number of the corresponding receipt in the Receipt Number field.
7 Click on Execute Query.
Transfer order 
number
Transfer receipt 
number

SHIPPING
Transfer Orders
OPERATIONS 1 GUIDE 4.2 299

LORE screen showing the receipt that corresponds to the transfer order
8 When you have finished viewing the details of this receipt, click on Exit to exit LORE.
CLEARING A TRANSFER ORDER IN CHAT
If a transfer order fails to create a transfer receipt, a warning message will appear in CHOF each time that you 
confirm an order. To clear the message, you must run CHAT (Change Auto Transfer Order to Regular). After 
the message is cleared, it will no longer appear in CHOF.
The transfer receipt must be manually entered in ENRE when it is not automatically generated in CHOF.
1 Enter CHAT.
2 Key in your order number and press Enter.
Transfer receipt 
number
The transfer 
order number 
displays in the 
Reference 
Number field.

SHIPPING
Entering Freight Type or Non-Inventory Orders

CHAT screen
3 Click on Clear Auto-Transfer.
4 Click on Exit to exit.
Entering Freight Type or Non-Inventory Orders
You use freight-type or non-inventory orders to track the shipping of non-inventory items such as containers 
or other equipment that are empty and do not contain product. For example, you receive product from a 
shipper in containers and you want to return the containers to the original shipper.
You can also use freight-type or non-inventory orders to enter an order that will be automatically transferred to 
AccellosOne Transport.
1 Enter ENOR.
2 Press F9 to position your cursor in Order Type field.
3 Key in F for Freight and press Enter.

SHIPPING
Entering Freight Type or Non-Inventory Orders
OPERATIONS 1 GUIDE 4.2 301

ENOR screen showing Order Type set to F for Freight 
4 Enter the order header in the normal manner by specifying your customer, consignee, carrier and other 
mandatory information.

ENOR screen showing the Class Block
5 When the Class Block appears, key in your freight class for the equipment that you are shipping and 
press Enter or select if from the pick list.
6 Key in the number of units and press Enter.
7 Key in the weight and press Enter.
8 If required, enter values in the Cube, Pallets and Amount fields.

SHIPPING
Picking to Clean

ENOR screen showing 10 units of the freight class FAK being shipped
9 When you finish entering your freight information, click on Return to Main to exit create mode.
10 If you wish to add remarks to your freight class, click on Remarks and proceed to enter any remarks.
11 Click on Master Block and Exit to exit.
12 Proceed to advance the flows of the freight order in CHOF in the normal manner and print any required 
order documents in PROM or PROR.
Picking to Clean
The pick to clean option allows you to pick all inventory for a particular item, level 2, level 3 or level 4 without 
entering a quantity in the Ordered Quantity field. AccellosOne 3PL will automatically populate the Ordered 
Quantity field with the total quantity of all available inventory for the inventory levels that you specify. 
Pick to clean supports both R-type and P-type order lines. However, you cannot pick to clean inventory on 
shippable or non-shippable hold.
1 Enter ENOR.
2 Enter the order header information normally.
3 In the Line Block, enter the required number of inventory levels. You can pick to clean at the lowest 
inventory, the highest inventory level or any inventory level in between.
4 In the Ordered Quantity field, key in C and press Enter.

SHIPPING
Broker Orders
OPERATIONS 1 GUIDE 4.2 303

ENOR screen showing C in Order Quantity field
5 Continue to enter your order lines.
6 When you finish entering your order lines, click on Return to Main. Then click on Master Block and Exit to 
exit.
Broker Orders
A broker order is an order shipped by a broker account. A broker account is a customer who is allowed to sell 
and ship inventory from other non-broker or “owner” customers. A single broker order can contain product 
from many different owner customers.
Broker accounts do not pay renewal storage because they do not own the inventory.
Any charges attached to the order header are billed to the broker, while charges attached to the order line are 
billed to the owner customer.
SETTING UP A BROKER CUSTOMER
To create a broker account, you set up a customer in CUST with an account type of B for Broker. In the Broker 
Block of the broker account, you enter all the customers whose products this broker is allowed to ship. You 
then set the Allow Replacement of Same Item flag to the appropriate value for each owner customer: Y for 
Yes or N for No.
You enter C in 
the Ordered 
Quantity field

SHIPPING
Broker Orders
When same item replacement is activated, AccellosOne 3PL will consider all items with the same item code 
as the same product and will allocate the order line according to the PIPR profile of the broker customer. For 
example, if you allocate product by absolute FIFO, AccellosOne 3PL will allocate the oldest product first 
regardless of ownership. Likewise, AccellosOne 3PL will ignore product ownership and pick to clean first, 
then pick from partial locations and lastly pick from full pallet locations according to your parameters in ILOP. 
The following restrictions apply to same item replacement:
 the two or more customers must share the same DILP profile
 the two or more items must have the same item code in ITEM and share the same ITSH profile
 the two or more items must share the same PIPR profile if a PIPR profile is attached to the item

CUST screen showing Account Type set to B for Broker
FIELD DESCRIPTIONS (BROKER BLOCK)
Customer Code The owner customer whose product the broker is authorized to ship.
Allow Replacement of 
Same Item
N = No
Y = Yes
If you set this flag to N for No, same item replacement is deactivated for the 
owner customer. That is, if you wish to ship product belonging to a specific 
owner customer when entering a broker order, you must key in that customer’s code in the Line Block of ENOR.
If you set this flag to Y for Yes, same item replacement is activated for the 
owner customer. That is, AccellosOne 3PL will ignore product ownership and 
allocate product based on the PIPR profile of the broker customer.

SHIPPING
Broker Orders
OPERATIONS 1 GUIDE 4.2 305

Broker Block with three customers shown
SHIPPING A BROKER ORDER
A single broker order can contain product from many different owner customers. If the broker account has its 
own inventory, a broker order can also contain product belonging to the broker account.
If the workflow profile set up in DIFP for the broker account differs from the workflow profile of the owner 
customer, the profile of the broker account will override the profile of the owner customer.
1 Enter ENOR and create an order for the broker customer.
2 Enter the rest of the header information in ENOR in the normal manner.
3 When the Line Block appears, enter your line type, remarks, etc. in the normal manner.
4 When your cursor is positioned in the Item field, do one of the following:
If you are shipping product 
belonging to the owner 
customer and same item 
replacement is activated:
If you are shipping product 
belonging to the owner 
customer and same item 
replacement is deactivated:
If you are shipping product 
belonging to the broker:
a) Proceed to next step. a) Press F9 until your cursor is 
positioned in the Customer 
Code field.
b) Key in the customer code of 
the owner customer — that is, 
the customer whose product 
you are actually shipping — 
and press Enter.
a) Proceed to next step.

SHIPPING
Processing Proof of Delivery in POD

ENOR screen showing order for broker 1 containing product from customer A
5 Enter the remaining Line Block information normally.
6 Add another line to your broker order or click on Exit to exit.
Processing Proof of Delivery in POD
The program Proof of Delivery (POD) validates the quantities of product that were actually delivered to the 
consignee and allows you to process product that is returned to the warehouse. 
Consignees may not accept all or some of the ordered quantities for various reasons. The following are two 
possible examples of undelivered product: 
EXAMPLE 1
Shipped Quantity = 10 cases to Consignee A
Delivered Quantity = 8 cases are accepted
Returned Quantity = 2 cases are returned due to damage
EXAMPLE 2
Shipped Quantity = 20 cases to Consignee B
Delivered Quantity = 0 cases
Returned Quantity = 20 cases as Consignee B cannot issue the COD payment
Once you have recorded the quantities that were delivered for an order, POD will also cause the system to 
perform the following functions: 
 update the Delivered field in LOOR

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 307
 create a new receipt to begin the process of re-receiving the undelivered product into the warehouse. 
(Later, you will need to confirm this receipt in order to update the inventory records.)
 show the transaction details in LOEN for the POD record, the transfer receipt and the original order 
There are two procedures in POD. You use one procedure when you need to validate that the order was 
delivered in full. You use the other procedure when the order has undelivered items that are returned to the 
warehouse.
ENTERING PROOF OF DELIVERY FOR AN ORDER DELIVERED IN FULL
This procedure will validate delivery of an entire order in full. The quantities that were shipped out were the 
same as the quantities that were delivered to and accepted by the consignee. If the order was made up of 
several products and therefore included multiple lines, the full quantity for each line was accepted by the 
consignee.
1 Enter POD.
2 Key in your order number and press Enter. The order must be confirmed before you can process it in 
POD.
3 Press Enter to accept the current date as your delivery date or key in a new delivery date and press 
Enter.
4 Key in your delivery time and press Enter or press Enter to accept the default value of 00:00 to indicate 
no delivery time.
NOTE You can only perform POD once for an order.

SHIPPING
Processing Proof of Delivery in POD

POD screen showing the Header Block details of order 1
5 Click on In Full. 
If the order was 
delivered in full, 
press F1 (In Full).

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 309

POD screen showing alert message
6 A message displays on the screen asking if you want to proceed with the update. Key in Y for Yes. You 
are taken out of POD.
ENTERING PROOF OF DELIVERY FOR AN ORDER NOT DELIVERED IN FULL
This procedure will process an order with undelivered product that was returned to the warehouse. If the 
order was made up of different items and therefore included multiple lines, each line will be validated individually. 
1 Enter POD.
2 Key in your order number and press Enter. The order must be confirmed before you can process it in 
POD.
3 Press Enter to accept the current date as your delivery date or key in a new delivery date and press 
Enter.
4 Key in your delivery time and press Enter or press Enter to accept the default value of 00:00 to indicate 
no delivery time.

SHIPPING
Processing Proof of Delivery in POD

POD screen showing the Header Block details of order 13
5 Click on Exceptions. The system populates the Line Block.
If the order was 
not delivered in 
full, press F3 
(Exceptions).

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 311

POD screen showing the details of order 13
6 The cursor moves to the Delivered field of the first line and prompts you to complete it. 
7 Do one of the following:
If the quantity delivered to and 
accepted by the consignee 
matches the shipped quantity:
If the delivered quantity does 
NOT match the shipped quantity:
a) Click on Set to Shipped. a) Key in the actual amount that 
was delivered and press Enter.
The Line Block displays the line 
details of the order: 
the item, the order 
quantity and the 
shipped quantity.

SHIPPING
Processing Proof of Delivery in POD

POD screen showing the details of order 13
8 Repeat step 7 of this procedure for each line. 
9 When you have finished setting the delivered amount in the Delivery field for all lines of this order, click 
on Return to Main.
F2 (Set to 
Shipped) will 
fill in the 
Delivered field 
with the same 
quantity as 
the Shipped 
field.
Key in any 
corrections.

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 313

POD screen showing Process button
10 F1 (Process) now appears as an option. Click on Process. You are taken out of POD.
You can now enter LOOR, and LOEN to check that the Proof of Delivery has been recorded into the system. 
You can also enter LORE to check the details of the corresponding receipt that the system created in order to 
re-receive the returned product. 
LOOKING UP A PROOF OF DELIVERY TRANSACTION IN LOOR
1 Enter LOOR.
2 Key in your order number.
3 Click on Execute Query and the order details will display on the screen.
NOTE You will need to finish processing the corresponding transfer receipt that the 
system has generated. You must enter the Location Code(s) in the transfer receipt, 
confirm it and print its attached documents. See “Looking Up a Proof of Delivery 
Transfer Receipt in LORE” on page 315.
You must press F1 
(Process) to enter the 
changes into the system; otherwise, the data 
will not be validated and 
processed.

SHIPPING
Processing Proof of Delivery in POD

LOOR screen showing transfer receipt for order 13
4 Note the Transfer Receipt Number and write it down for future reference.
5 Click on Line Block and the first line record will display.
6 Check the Deliver Quantity field. It shows the amount that was delivered and accepted by the Consignee. 
You can compare this to the data in the Ordered Quantity and Ship(ped) Quantity fields.
7 The difference between the Deliver(ed) Quantity and the Shipped Quantity is the quantity that was 
returned to the warehouse and it is the quantity that will show on the Transfer Receipt.
8 Use the up and down arrow keys to view all line records.
Transfer receipt 
number that the 
system created in 
order to re-receive 
the returned product.

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 315

LOOR screen showing the details of order 13
9 When you have finished viewing all line records, click on Order Block and Exit.
LOOKING UP A PROOF OF DELIVERY TRANSFER RECEIPT IN LORE
1 Enter LORE.
2 Key in your receipt number.
3 Click on Execute Query and the receipt details will display on the screen.
The Deliver 
Quantity field 
now shows the 
amount that 
was entered in 
POD.

SHIPPING
Processing Proof of Delivery in POD

LORE screen showing the Header Block details of transfer receipt 22
4 Note the Reference Number and write it down for future reference. It is the number of the corresponding 
order with returned product.
5 Also note that the Location Status, which will likely display as “Missing.”
6 Click on Line Block and the first line record will display.
The reference 
number is the 
number of the 
corresponding order with 
the returned 
product.
Location status

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 317

LORE screen showing the Line Block details of transfer receipt 22
7 The Expect Quantity and Receive Quantity fields show the amount of this item that is being received into 
the warehouse. (This is the same quantity as was returned for the corresponding order.)
8 If this receipt has more than one Line Block record, use the up and down arrow keys to view the other 
records.
9 When you have finished viewing all line records, click on Receipt Block and Exit.
LOOKING UP A PROOF OF DELIVERY RECORD IN LOEN
1 Enter LOEN.
2 Key in the customer code of the owner of the product and press Enter.
3 Key in the item code and press Enter. 
4 Key in the applicable Inventory Level fields.
5 Click on Execute Query and the details will display on the screen.
6 Click on History Block.
NOTE The Location Code will be missing for each Line Block record. Enter ENRE 
and key in the locations for each of the Line Block records of this order. 
You will also need to confirm the receipt in CHRF and to print the attached documents 
in PRRE or PRRM (or bypass the printing requirement in RERE).
The returned product is being rereceived into the 
warehouse.

SHIPPING
Processing Proof of Delivery in POD

LOEN screen showing the History Block
7 Use the up and down arrow keys to scroll down to the Proof of Delivery transaction that you are looking 
for. The transaction type will show as PD.
The corresponding transfer 
receipt and order 
numbers
The POD transaction
The original confirmed order 
transaction

SHIPPING
Processing Proof of Delivery in POD
OPERATIONS 1 GUIDE 4.2 319

LOEN screen showing the History Details Block
8 Click on History Detail Block. When you have finished viewing the details, Click on History Block.
9 If you wish to view the History Block details for the original order and the transfer receipt, use the up and 
down arrow keys to scroll down to the transaction that you are looking for. Then click on History Detail 
Block. When you have finished viewing the details, click on History Block. 
10 Repeat until you have finished viewing the details for all of the transactions that are related to this Proof 
of Delivery.
11 Click on History Block, Inventory Block and Exit.

SHIPPING
Processing Proof of Delivery in POD

OPERATIONS 1 GUIDE 4.2 321
A
adjustments
creating new inventory 153
to expiry dates 187
to holds 169
to inventory 140
to level 2 descriptions 188
to weights 189
transfer type 149
alternate type codes and alternate item codes, using in inventory queries 135
B
broker orders 303
C
cancelling order documents 277
cancelling receipt documents 85
Carrier Block (ENRE) 33
Change Auto Transfer Order to Regular (CHAT) 299
Change Confirmation Date (CHCD) 264
Change Entity Information (CHEI) 187, 188
CHAT (Change Auto Transfer Order to Regular) 299
CHCD (Change Confirmation Date) 264
Check Qty Breakdown and Receipt Qty (CVQB) 65
CHEI (Change Entity Information) 187, 188
CHOF (Time-Stamp and Confirm Orders) 257
CHRF (Time-Stamp and Confirm Receipt) 90
CHRL (Change Inventory Level on Receipt Line) 46
CICP (Check-In Configuration Parameters) 103
Clear Weights (CLWE) 196
clearing weights 196
CLWE (Clear Weights) 196
Confirm Orders - Line at a Time (COOL) 261
confirming
orders 257
receipts 89
confirm-type receipts 52
COOL (Confirm Orders - Line at a Time) 261
CORL (Confirm Receipts - Line at a Time) 94
cross-docking 284
CVQB (Check Qty Breakdown and Receipt Qty) 65
D
default sort sequence in LOOR, changing 249
default sort sequence in LORE, changing 77
descriptions for level 2, adjusting in CHEI 188
distribution-type orders 284
documents
for orders 250
for receipts 78
E
ENAJ (Enter Adjustment)
creating new inventory 153
negative 146
overview 140
positive 142
transfer 149
ENOR (Enter Orders) See orders
ENRE (Enter Receipts) See receipts
Enter Adjustment (ENAJ)
creating new inventory 153
negative 146
overview 140
positive 142
transfer 149
Entering 203
expiry dates, adjusting in CHEI 187
F
flow processes
looking up codes 7
overview 6
reversing 197
sequence 7
time-stamping in CHOF 257
time-stamping in CHRF 89
INDEX

INDEX
freight-type orders 300
H
HATO (Holds Auto Take-Off) 176
HOAD (Hold Adjustments)
adjusting hold code only 177
overview 169
placing inventory on hold 170
removing inventory from hold 173
Hold Adjustments (HOAD)
adjusting hold code only 177
overview 169
placing inventory on hold 170
removing inventory from hold 173
holds
looking up off hold date 175
massive 177
on selected inventory 169
overview 169
removing 173
Holds Auto Take-Off HATO) 176
I
inspection orders 282
in-transit receipts 53
L
location capacity, looking up in LOLO 139
location codes, entering on the fly in ENRE 31
LOEN (Look Up Entity Information)
alternate type code and alternate item code 135
Drill Block 122
Header Block 114
History Block 128
History Details Block 131
History Remark Block 133
Location Block 124
Renewal Block 133
LOLO (Look Up Location Information) 136
Look Up Entity Information (LOEN)
Drill Block 122
Header Block 114
History Block 128
History Details Block 131
History Remark Block 133
Location Block 124
Renewal Block 133
Look Up Location Information (LOLO) 136
Look Up Orders (LOOR) 245
Look Up Pending Receipts (LOPR) 55
Look Up Receipts (LORE) 71
Look Up Telephone Numbers (LOTE) 70
looking up inventory 114
looking up locations 136
look-up programs 67
LOOR (Look Up Orders) 245
LOPR (Look Up Pending Receipts) 55
LORE (Look Up Receipts) 71
LOTE (Look Up Telephone Numbers) 70
M
MAHO (Take Off Holds) 181
MAOE (Manual Order Entry) 228
MARL (Massive Relocate) 165
Massive Adjustment (MATR) 154
massive adjustments 154
massive holds 177
Massive Relocate (MARL) 165
MATR (Massive Adjustment) 154
MOHO (Move Hold to Hold) 184
N
non-inventory orders 300
non-standard weights, adjusting 189
O
operations flow process 6
order documents See printing order documents
orders
adding to the VICS bill of lading 273
assigning locations 216
assigning multiple locations to a line block record 221
broker type 303
Carrier Block 226
changing default sort sequence 249
clearing out all inventory 302
confirmation date, changing in CHCD 264
confirming in CHOF 257
confirming in COOL 261
deleting entire line 238
deleting entire order 237
deleting Location Block data 240
distribution-type 284
entering Header Block information 203
entering Line Block information 210
Extended Remarks Block 225
freight-type 300
header types 241
inspection type 282
line types 241
looking up in LOOR 242
looking up item summary 249
manual order entry in MAOE 228
modifying Header Block data 229
modifying Line Block data 230
modifying Location Block data 232
modifying optional blocks data 233
non-inventory 300
overview 200
pending versus regular 211
picking to clean 302
printing documents for See printing order documents
P-type lines vs. R-type lines 211
querying on inventory levels 218
Remark Block 224
removing from the VICS bill of lading 273
requeuing a range 280
R-type lines vs. P-type lines 211
transfer type 290

INDEX
OPERATIONS 1 GUIDE 4.2 323
troubleshooting confirmation of 260
updating carrier details 234
P
pending receipts, looking up 55
POD See proof of delivery
POHO (Put on Hold) 177
Print Order Documents - All (PROR) 253
Print Receiving Documents - All (PRRE) 80
Print Receiving Documents - Specific (PRRM) 78
Print Shipping Documents - Specific (PROM) 250
printing order documents
cancelling 277
for all orders 253
for specific orders 250
overview 250
reprinting 278
shipping labels 281
printing receipt documents
cancelling 85
for all receipts 80
for specific receipts 78
overview 78
receiving labels 88
reprinting 86
PROM (Print Shipping Documents - Specific) 250
proof of delivery
for orders delivered in full 307
for orders not delivered in full 309
looking up in LOEN 317
looking up in LOOR 313
looking up in LORE 315
overview 306
PROR (Print Order Documents - All) 253
PRRE (Print Receiving Documents - All) 80
PRRM (Print Receiving Documents - Specific) 78
Put on Hold (POHO) 177
Q
queries, basic 67
R
rating receipts 96
RCIS (Receipt Check-In at Staging) 105
RCRA (Receipt Rater) 96
Recalculate Standard Weight (RESW) 193
Receipt Check-In at Staging Detail Report 108
Receipt Check-In at Staging Summary Report 107
receipt check-in receiving 103
receipt documents See printing receipt documents
Receipt Rater (RCRA) 96
receipts
cancelling documents for 85
Carrier Block 33
changing default sort sequence 77
changing the inventory level on receipt line 46
confirming in CHRF 89
confirming in CORL 94
confirm-type 52
deleting entire line 48
deleting entire receipt 46
deleting Location Block data 50
entering Header Block information 17
entering Line Block information 22
entering location 26
Extended Remarks Block 32
header types 51
in-transit 53
line types 51
location codes, entering on the fly 31
looking up in LORE 67
looking up item summary 77
missing inventory levels, entering 56
modifying 40
modifying Location Block data 43
modifying optional blocks data 44
overview 14
printing documents for See printing receipt documents
rating in RCRA 96
receiving a single item line into multiple locations 28
Remark Block 32
removing charges from in RERA 100
reprinting documents for 86
requeuing for rating purposes 100
re-receiving inventory 31
sequential entry 57
system-generated inventory levels 61
troubleshooting confirmation of 93
unrating in RERA 100
U-type 54
variable quantity breakdown inventory 63
RELA (Reprint Labels) 88, 281
RELO (Relocate Inventory) 159
Relocate Inventory (RELO) 159
REOR (Requeue Order Documents) 276
Reprint Labels (RELA) 88, 281
reprinting order documents 278
reprinting receipt documents 86
Requeue Order Documents (REOR) 276
Requeue Receipt Documents (RERE) 84
Requeue Receipt for Rating (RERA) 100
requeuing a range of orders 280
RERA (Requeue Receipt for Rating) 100
RERE (Requeue Receipt Documents) 84
RERO (Requeue a Range of Orders) 280
restricting warehouses 35
RESW (Recalculate Standard Weight) 193
Reverse Document Flow (RVDF) 197
RVDF (Reverse Document Flow) 197
S
sequential entry receipts 57
standard weights, adjusting 193
T
Take Off Holds (MAHO) 181
telephone numbers, looking up 70
Time-Stamp and Confirm Orders (CHOF) 257

INDEX
Time-Stamp and Confirm Receipt (CHRF) 90
transaction types (LOEN) 130
transfer adjustments 149
transfer orders 290
Transfer Profile Code (TRPR) 290
TRPR (Transfer Profile Code) 290
U
unrating a receipt 100
UOCP (Update Order Carrier/Pallet) 234
Update Receipt Quantity Breakdown (URQB) 66
URQB (Update Receipt Quantity Breakdown) 66
U-type receipts 54
V
variable quantity breakdown inventory, receiving 63
VBOL (VICS Bill of Lading) 266
VICS Bill of Lading (VBOL) 266
W
warehouse restrictions 35
WEAD (Weight Adjustments) 189
Weight Adjustments (WEAD) 189
weights, adjusting 189
weights, clearing in CLWE 196
