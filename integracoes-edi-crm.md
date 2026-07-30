---
title: "EDI e CRM"
description: "Perfis EDI, transaction sets, faturamento EDI 811 e registro de ocorrências CRM."
layout: default
---

# EDI e CRM

Perfis EDI, transaction sets, faturamento EDI 811 e registro de ocorrências CRM.

**Fluxo principal:** `DEDP/CEDI (perfil) -> EDTS/EDDI (transaction sets) -> EDIV (811) | CRMC/CRME`

> Fonte: manuais E do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Customer Relationship Management <a id="customer-relationship-management"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

The Customer Relationship Management system allows you to enter work requests and problems into the system for tracking and resolution purposes. Each work request shows complete time stamping information for all status changes. You can reopen completed requests, reassign responsibility for the request and enter as many charges as needed via a direct link to ENAC. You can also access the CRM module from both LORE and LOOR. 
The CRM system is designed for internal maintenance management as well as claims and damages management — both internal and external. It can track any event — whether planned or unplanned — that is beyond the scope of normal receiving/shipping.
A work request in CRM goes through the following statuses:

### Setting Up Your CRM Codes in CRMC <a id="setting-up-your-crm-codes-in-crmc"></a>

You set up your CRM codes in CRMC (CRM Code). CRM codes describe the nature of the work request and are used for internal tracking purposes.
The work request is completed by the person assigned primary responsibility for it. If required, completed work requests can be reopened.
The work request is opened in
CRME. Open requests can be assigned, deleted or resolved.
The work request is assigned to the person actually doing the work. Assigned work requests can be reassigned, deleted or resolved.
The work request is resolved by the person actually doing the work. Resolved work requests can be completed.
OPEN
ASSIGNED
RESOLVED
COMPLETED

OPERATIONS 2 GUIDE 4.2* 143
1 Enter CRMC.
2 Click on Create Record.
3 Key in your CRM code and press Enter.
4 Key in a description for your code and press Enter.
5 Press Enter to bypass the Job Type Code field.
6 Repeat the above steps for each additional code that you wish to set up.

CRMC screen showing CRM codes
7 When you finish setting up your CRM codes, click on Return to Main and Exit to exit.

### Entering Work Requests in CRME <a id="entering-work-requests-in-crme"></a>

When you enter a work request in CRME, you specify the following pieces of information:
 the customer for whom you are performing the work request
 the name and telephone number of the contact person for the work request
 the operator who has primary responsibility for the work request
 the operator who is assigned the work request
 whether the work request is billable or not
 the work request’s CRM code
FIELD DESCRIPTIONS
CRM Number This number is system generated.

Customer Mandatory
The customer for whom you are performing the work request. If you are creating an internal work request, you should create a dummy customer for your own company in CUST with an account type of I for Invoice Only.
Caller’s Name Mandatory
The person for whom the work request is being performed.
Telephone Mandatory
The telephone number of the caller.
Transaction Type Inventory
Miscellaneous
Order
Receipt
The type of transaction.
Reference Number Optional
The work request’s reference number. If you are adding a work request to an order or receipt in LOOR or LORE, this field is automatically populated with the order or receipt number.
Description Mandatory
The work request’s description.
Primary Responsibility (defined in OPER)
Optional
The operator in AccellosOne 3PL who has overall responsibility for the work request. If you do not specify an operator, the status of the work request will remain open until you assign an operator primary responsibility for the task or you advance the status to “Resolved”.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 145
1 Enter CRME.

2 Click on Create Record.
3 Key in your customer code and press Enter or use the pick list function to select it (press F10 to enter the pick list, then click on Execute Query and Select to select the appropriate code).
4 Key in the caller’s name and press Enter.
5 Key in the caller’s telephone number and press Enter.
6 If required, key in the caller’s extension number and press Enter. If there is no extension number, press 
Enter to bypass this field.
Assigned To (defined in OPER)
Optional
The operator in AccellosOne 3PL who will actually perform the work. If you do not specify an operator, the status of the work request will remain open until you assign an operator to the task or you advance the status to “Resolved”.
Charge Y = Yes
N = No
If you select Y for Yes, you can add one or more accessorial charges to the work request in ENAC. If you select N for No, you cannot add accessorial charges to the work request in ENAC
Hourly Rate Optional
The hourly rate for the work request.
Total Estimated Optional
The total estimated time for the work request.
CRM Code (defined in CRMC)
Mandatory
The CRM code for the work request.
Source I = Internal
E = External
If you select I for Internal, the work request is internal and unrelated to any customer or account. If you select E for External, the work request is being performed for an outside party.
FIELD DESCRIPTIONS

7 Select the appropriate transaction type from the dropdown list and press Enter.
8 If prompted to do so, key in your order number, receipt number or inventory levels and press Enter.
9 If required, key in a reference number and press Enter. If there is no reference number, press Enter to bypass this field.
10 Key in a description for the work request and press Enter.
11 If required, key in the person with primary responsibility for the task and press Enter or use the pick list function to select this person.
12 If required, key in the person that you are assigning to the work request and press Enter. If you do not enter a person in this field, the status of the work request will remain “Open” until it is assigned.
13 In the Charge field, key in N for No and press Enter.
14 If required, key in an hourly rate and press Enter.
15 If required, key in the total estimated time in hours and minutes and press Enter.
16 Key in your CRM code and press Enter or use the pick list function to select it.
17 In the Source field, key in I for Internal or E for External and press Enter.

CRME screen showing a non-billable POD work request
18 If you wish to record your time for setting up the work request, you must enter your time in the Detail 
Block. See [Entering Your Time in the Detail Block](integracoes-edi-crm.html#entering-your-time-in-the-detail-block) for further instructions.
19 When you finish entering your work request, click on Return to Main and Master Block. Then click on Exit to exit.

OPERATIONS 2 GUIDE 4.2* 147

### ENTERING YOUR TIME IN THE DETAIL BLOCK <a id="entering-your-time-in-the-detail-block"></a>

You enter your time for a given work request in the Details Block of CRME. Any operator in AccellosOne 3PL with access to CRME can enter his or her time for the request in the Detail Block of any CRM record. Any time recorded will be recorded under the operator code of the operator signed on to AccellosOne 3PL when the entry is made. The operator entering his or her time need not be the same as the primary responsibility operator or the assigned to operator. 
There are four codes used to track time in the Detail Block: CLAR (Clarification), FOLL (Follow-Up), ISSU (Issue) and RESO (Resolution).
1 Enter CRME.
2 Retrieve the CRM number whose Detail Block you wish to update.
3 Click on Details Block.
4 Do one of the following:
5 Key in your type code and press Enter or use the pick list function to select it (press F10 to enter the pick list, then click on Execute Query and Select to select the appropriate code).
6 Key in a description for your time and press Enter.
7 Key in your time in hours and press Enter. If you are entering your time in minutes only or not entering time, press Enter to bypass this field.
8 Key in your time in minutes and press Enter. If you are entering your time in hours only or not entering time, press Enter to bypass this field.
NOTE The Details Block in CRME is optional. If you do not enter any records in the 
Detail Block, the work request remains valid but you will not be able to track the total elapsed time of the request or the request details. If you enter records in the Details 
Block without entering any time, you will be able to track details of the request — for example, the action taken, the operator and date and time — but no total elapsed time for the request.
If there is already a record in the 
Detail Block: If the Detail Block is blank:
a) Click on Create Record. a) Click on Return to Main to return to Main then click on Create 
Record.

CRME screen showing entry in Detail Block by operator LORNE
9 If you wish to enter multiple description lines, you must repeat the type (for example, “FOLL” for Follow 
Up) and then enter your second description line.
10 When you finish entering your time, click on Return to Main and Master Block. Then click on Exit to exit.

### UPDATING THE STATUS OF A WORK REQUEST <a id="updating-the-status-of-a-work-request"></a>

You update the status of a work request by selecting the appropriate value in the Status field. The following table shows the valid statuses for each step in a work request.
Current Status is . . . Available statuses are . . .
Open Deleted, Resolved, Assigned
Assigned Deleted, Resolved, Reassigned
Reassigned Deleted, Resolved
Reopened Deleted, Resolved
Resolved Completed
Completed Reopened

OPERATIONS 2 GUIDE 4.2* 149
Whenever you update the status of a work request, AccellosOne 3PL creates a new line in the Time Stamping 
Block of CRME. This line shows the date and time that the status was changed, the status itself and the operator who changed the status. 
1 Enter CRME.
2 Retrieve the CRM number whose status you wish to updated.
3 Press Enter until your cursor is positioned in the Status field.
4 Use your pick list to select the appropriate status.
5 When you finish updating your status, click on Exit to exit.

### PRINTING A WORK REQUEST <a id="printing-a-work-request"></a>

You have two print options in CRME: you can either print the current work request in PDF format or you can run the CRMR report and select the work requests that you wish to print.
1 Enter CRME.
2 Retrieve the CRM number that you wish to reassign.
3 Press Enter once to position your cursor in the Caller’s Name field.
4 Click on Print Details.
5 When prompted to select the report parameters, do one of the following:
If you wish to print the current work request only:
If you wish to select your report parameters and run the CRMR report:
a) Click on No. a) Click on Yes.
b) Proceed to enter your report parameters.
c) When you finish entering your report parameters, click on 
Select Printer.
d) Select your printer and click Ok.
ABC Warehousing, Inc. WORK ORDER 05.27.08 11:20
--------------------------------------------------------------------------------
CRM Number : 81 Status : OPEN Opened
Customer : A Customer A Date : 05.27.08 11:10
Caller Name : Consignee (Harry's Computers) Chargeable: N
Telephone : 905-695-9999 Ext. Rate : Per Hour
Reference : Order 2 CRM Code : CLM Claims
Primary Resp. : PBRAD Source : E
Assigned To : Unassigned ORDER : 2
Total Estimated : H M
Total Elapsed : H 35 M
Description : computer not received, must do POD, requested toda y from FEDEX
 Elapsed
Type Operator Description (H) (M)
---- ----------------- --------------------------------------------- ---- ---
ISSU LORNE Customer has not received computer 35

### REASSIGNING A WORK REQUEST <a id="reassigning-a-work-request"></a>

If a work request has a status of Assigned, you can re-assign it to another operator.
1 Enter CRME.
2 Retrieve the CRM number that you wish to reassign.
3 Press Enter until your cursor is positioned in the Assign To field.
4 Key in your new operator or use the pick list function to select it.
5 Click on Return to Main and Master Block. Then click on Exit to exit.

### DELETING A WORK REQUEST <a id="deleting-a-work-request"></a>

If a work request has a status of Open, Assigned, Reassigned or Reopened, you can delete it. If the work request that you delete has a charge attached to it, the charge will be deleted as well.
1 Enter CRME.
2 Retrieve the CRM request that you wish to delete.
3 Press Enter until your cursor is positioned in the Status field.
4 Use your pick list to select the status of Deleted.
5 Click on Exit to exit.

### Adding a Work Request to an Order or Receipt <a id="adding-a-work-request-to-an-order-or-receipt"></a>

You can attach a work request to a specific order or receipt by entering the Time Block of LORE (Look Up 
Receipts) or LOOR (Look Up Orders). When you enter a work request in LORE or LOOR, the Reference 
Number field in CRME will show the work request’s receipt or order number.
1 Enter LORE or LOOR.
2 Retrieve the receipt or order that you wish to add the work request to.
3 Click on Time Block.
4 Click on CRM Block.
5 Click on Create Record.

OPERATIONS 2 GUIDE 4.2* 151
CRME screen showing new work request for receipt 2
6 Proceed to add your work request in the normal manner. If required, you can change the system-generated value in the Reference Number fields.
7 When you finish adding your work request, click on Return to Main and Master Block. Then click on Exit to exit.

### LOOKING UP A WORK REQUEST ATTACHED TO AN ORDER OR RECEIPT <a id="looking-up-a-work-request-attached-to-an-order-or-receipt"></a>

1 Enter LORE or LOOR.
2 Retrieve the receipt or order that the work request is attached to.
3 Click on Time Block.
4 Click on CRM Block.
5 Click on Enter Criteria then Execute Query to retrieve your work request or requests.
6 If there are multiple work requests attached to the same receipt or order, use your arrow keys to scroll through the list.
7 When you reach the work request that you wish to look up, you can modify it, change its status or delete it.
8 When you finish looking up your work request, click on Exit and Master Block. Then click on Exit to exit.
Reference 
Number field automatically populated with receipt or order 

### Adding a Work Request to Inventory in LOEN <a id="adding-a-work-request-to-inventory-in-loen"></a>

You can add a work request to an individual inventory entity in LOEN.
1 Enter LOEN.
2 Retrieve the inventory that you wish to add the work request to.
3 Click on CRM Screen .
CRME screen showing transaction type of inventory
4 Click on Create Record and add your work request in the normal manner.
5 When you finish adding your work request, click on Return to Main and Exit.
6 Click on Exit again to exit LOEN.

### Looking Up Work Requests in CRME <a id="looking-up-work-requests-in-crme"></a>

You can query a work request by CRM number, customer, reference number or any other field in the Master 
Block of CRME. If you have attached a work request to a receipt or order, the Reference # field in CRME will show the work request’s receipt or order number and you can query by this number as well.

OPERATIONS 2 GUIDE 4.2* 153
The Time Stamping Block of CRME shows one line for each change of status that the work request has undergone. This line shows the date and time that the status was changed, the status itself and the operator who changed the status. 
1 Enter CRME.
2 Click on Enter Criteria.
3 Proceed to enter your search criteria. You can search by CRM number, customer, reference number or any other field in the Master Block of CRME.
4 When you finish entering your search criteria, click on Execute Query.
CRME screen showing a completed work request
5 Click on Detail Block.
6 Click on Time Block.

CRME screen showing Time Stamping Block
7 Click on Detail Block to return to the Detail Block then click on Master Block to return to the Master Block.
8 Look up another work request in CRME or click on Exit to exit.

### Reports <a id="reports"></a>

See the Standard Reports Guide.

### Charging for a Work Request <a id="charging-for-a-work-request"></a>

If you set the Charge field in CRME to Y for Yes, you can add one or more accessorial charges to a work request. Adding a charge code to a work request requires a normal charge code set up in CHAR (Charge 
Code). You can bill any customer on your system for the charge; the customer that you bill need not be the customer attached to the work request in CRME.
No billing will occur for the charge until the work request has a status of “Completed”. You can look up the charge in ENAC by performing a query on the Reference Number field. Charges created while working in 
CRME will have a reference number of CRM followed by the CRM number. 

OPERATIONS 2 GUIDE 4.2* 155
ENAC screen showing Reference Number field
1 Enter CRME.
2 Retrieve the CRM number that you wish to charge for.
3 Press Enter until your cursor is positioned in the Charge field. The value in this field must by Y for Yes before you can enter a charge.
This charge is attached to 
CRM 2547

CRME screen showing cursor positioned in the Charge field
4 Click on Accessorial.
ENAC screen

OPERATIONS 2 GUIDE 4.2* 157
5 Click on Create Record.
6 Proceed to enter your charge or charges. Refer to the section “Entering Accessorial Charges Directly in 
ENAC” in the Billing and Invoicing Guide for further instructions on entering accessorial charges.
7 When you finish entering your accessorial charges, click on Return to Main and Exit to return to CRME. 
Then click on Return to Main and Exit to exit.
BILLING A CUSTOMER OTHER THAN THE CUSTOMER ATTACHED TO THE 
WORK REQUEST
If you wish to bill a customer other than the customer attached to the work request, you must do so in modify record mode.
1 Enter your charge in ENAC in the normal manner. The charge will be automatically billed to the customer attached to the work request in CRME.
2 Click on Return to Main to exit create record mode.
3 Press Enter to position your cursor in the Bill To Code field.
4 Key in your new customer code and press Enter.

OPERATIONS 2 GUIDE 4.2* 159

## EDI <a id="edi"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

AccellosOne 3PL’s EDI system consists of EDI translation and management software such as Softcare 
TradeLink, Nexus, ACom EZConnect, etc. together with various interfaces to AccellosOne 3PL. The EDI translation and management software is responsible for EDI (X12 and EDIFACT) and XML data translation, data management and communication. The AccellosOne 3PL interfaces are responsible for creating order, receipt and inventory transactions and extracting the information required for these transactions from the 
AccellosOne 3PL database. You can communicate via EDI and XML with any customer, carrier, shipper and consignee on your system.
EDI information can be defined as either mandatory or optional. If it is mandatory, you cannot confirm a receipt or order if the EDI data is missing. If it is optional, orders and receipts can be confirmed without the 
EDI data.

### Setting Up EDI <a id="setting-up-edi"></a>

There are up to seven steps to follow in setting up EDI in AccellosOne 3PL:
 you set up your EDI document in DOCU and attach it to the appropriate flow in DIFP (performed by 
HighJump)
 you set up your EDI transaction sets in EDTS
 you set up your data ID codes in EDDI
 you set up your case codes in EDCA (performed by HighJump)
 you set up your EDI profile codes in DEDP
 you set up your EDI customers in CUST
 you set up your EDI 810 Invoice in ECID (optional)

### 1 — SETTING UP YOUR EDI TRANSACTION SETS IN EDTS <a id="1-setting-up-your-edi-transaction-sets-in-edts"></a>

You set up your EDI transaction sets in EDTS. EDI transaction sets are linked to data segments in EDDI and attached to EDI profiles in DEDP. 
FIELD DESCRIPTIONS
EDI Version Code Mandatory
Your EDI version. Versions are supplied by HighJump.
EDI Transaction Set 
Code
Mandatory
Your EDI transaction set.

OPERATIONS 2 GUIDE 4.2* 161
1 Enter EDTS.
2 Click on Create Record.
3 Use your pick list to select the appropriate EDI version. Refer to the version description to ensure that you have selected the correct EDI code.
4 Key in your EDI transaction set and press Enter.
5 Key in a description for your EDI transaction set and press Enter.
6 In the EDI Transaction Type field, use your pick list to select the appropriate code. 

EDI Transaction Set Codes (EDTS)
7 Repeat the above steps to add another EDI transaction set or click on Return to Main and Exit to exit.

### 2 — SETTING UP YOUR DATA ID CODES IN EDDI <a id="2-setting-up-your-data-id-codes-in-eddi"></a>

In this program, you define the data segments for your transaction sets. A data segment consists of a data ID code, the starting position of the code and its length. 
EDI Type Description Ship
Receive
Other
Use Ship for outbound transactions. Use Receive for inbound transactions. 
Use Other when the transaction is both inbound and outbound.
FIELD DESCRIPTIONS
EDI Version Code Mandatory
The EDI version code for the data segment.
FIELD DESCRIPTIONS

1 Enter EDDI.
2 Click on Create Record.
3 Key in your EDI version code and press Enter or use your pick list to select the appropriate EDI version.
4 Key in your EDI transaction set code and press Enter or use your pick list to select the appropriate EDI transaction set.
5 Key in your EDI data ID code and press Enter.
6 Key in a description for your EDI data ID code and press Enter.
7 Key in a starting position for your EDI data ID code and press Enter.
8 Key in a length for your EDI data ID code and press Enter. Repeat the above steps for your next data segment or click on Return to Main and Exit to exit.
EDI Transaction Set 
Code (EDTS)
Mandatory
The EDI transaction set code for the data segment.
EDI Data ID Code Mandatory
The EDI/TradeLink code for the data segment.
Starting Position Mandatory
The starting position of the data segment as defined by TradeLink.
Length Mandatory
The length of the data segment as defined by TradeLink.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 163

EDI Data ID Codes (EDDI) screen showing unit of measurement code for the warehouse shipping advice

### 3 — SETTING UP YOUR CASE CODES IN EDCA <a id="3-setting-up-your-case-codes-in-edca"></a>

In this program, you set up your case codes. Case codes link a data element within a transaction set to the appropriate column in the AccellosOne 3PL database. Case codes are attached to EDI profile codes in 
DEDP. 
Case codes must be set up by HighJump.

EDI Program/Routine/Case Codes (EDCA) screen

### 4 — SETTING UP YOUR EDI PROFILE CODES IN DEDP <a id="4-setting-up-your-edi-profile-codes-in-dedp"></a>

In this program, you set up your EDI profile codes. An EDI profile code consists of an EDI version code, an 
EDI transaction set and the appropriate data ID codes and case codes. You can attach as many EDI transaction sets as you require to the same EDI profile code.
For each data ID code, you define:
 whether it can be manually entered or modified in ENRE or ENOR
 whether it is part of the order/receipt header or the order/receipt line
 whether it is mandatory or optional
 its length and data type
The EDI profile code that you set up in DEDP is attached to the appropriate customer in CUST (Customer 
Setup).
FIELD DESCRIPTIONS
EDI Profile Code Mandatory
Your EDI profile code.

OPERATIONS 2 GUIDE 4.2* 165
Description Mandatory
A description for your EDI profile code.
EDI Version Code Mandatory
The EDI version code for the transaction set.
TRANSACTION SET BLOCK
Transaction Set Code (defined in EDTS)
Mandatory
The EDI profile code’s transaction set.
DATA ID BLOCK
Data ID Code (defined in EDDI)
Mandatory
This transaction set’s data ID code.
Case Code (defined in EDCA)
Mandatory
The data ID code’s case code.
Send Reserved for future use
Type N = Never
E = At Entry
This field governs manual modifications to EDI data in the EDI Blocks in 
ENOR and ENRE. If you enter N for Never, the data ID code can never be modified in ENOR and ENRE. If you enter E for Entry, the data ID code can be modified at any time before order or receipt confirmation.
FIELD DESCRIPTIONS

Line Y = Yes
N = No
If you enter Y for Yes, the data ID code is defined as a line record. If you enter 
N for No, the data ID code is defined as a header record.
Mand. Y = Yes
N = No
If you enter Y for Yes, the data ID code is mandatory. If you define a data ID code as mandatory, you must manually enter the value in ENOR or ENRE before confirmation should this value be missing for any reason.
If you enter N for No, the data ID code is not mandatory.
Length Mandatory
The length of the column in the AccellosOne 3PL database corresponding to the data ID code. This length may differ from the length of the data ID code in 
EDDI (EDI Data ID Codes).
Type CHAR = Character
DATE = Date
INT = Integer
MONY = Money
NUM = Number
The data type of the data ID code.
OUTBOUND BLOCK
If an inbound EDI transaction set has a corresponding outbound transaction set, you define the outbound transaction set and data ID codes in this block.
Transaction Set Code (defined in EDTS)
Mandatory
The transaction set for the outbound transaction.
DATA ID BLOCK

OPERATIONS 2 GUIDE 4.2* 167
1 Enter DEDP.
2 Key in your EDI profile code and press Enter.
3 Key in a description for your EDI profile code and press Enter.
4 Key in your EDI version code and press Enter or use the pick list function to select it.
5 In the Transaction Set Block, key in your transaction set and press Enter or use the pick list function to select it.
6 Click on Data ID Block to enter the Data ID Block.
7 Key in your data ID code and press Enter.
8 Key in your case code and press Enter or use your pick list to select it.
9 Press Enter to bypass the Send field.
10 In the Type field, key in N for Never or E for Entry and press Enter.
11 In the Line field, key in Y for Yes or N for No and press Enter.
12 In the Mand. field, key in Y for Yes or N for No and press Enter.
13 In the Length field, key in the length of the data ID code and press Enter.
14 In the Type field, key in your column type and press Enter or use your pick list to select it.
15 Repeat steps 7 to 14 for each additional data ID code that you wish to add to the Data ID Code Block.
16 When you finish entering all your data ID codes, click on Return to Main and Trans Set Block. Then click on Master Block and Exit to exit DEDP.
Data ID Code (defined in EDDI)
Mandatory
The data ID code for the outbound transaction set.
OUTBOUND BLOCK

EDI Profile Code (DEDP) screen showing the Data ID Block

### 5 — SETTING UP YOUR EDI CUSTOMER IN CUST <a id="5-setting-up-your-edi-customer-in-cust"></a>

In this program, you set up your EDI customer. You set up an EDI customer by attaching the EDI profile code that you set up in DEDP to that customer. Then you add that customer’s EDI partner ID in the Customer EDI 
Partner ID field.
If you wish to set up a shipper or consignee as an EDI partner, you attach the appropriate EDI transaction set to a unique DIFP profile. You then attach that profile to the appropriate shipper or consignee.
1 Enter CUST.
2 Retrieve the customer that you wish to set up for EDI.
3 Press Enter until your cursor is positioned in the EDI Profile field.
4 In the EDI Profile field, key in your EDI profile code and press Enter.
5 In the Customer EDI Partner ID field, key in your EDI partner ID and press Enter.
6 Click on Return to Main and Exit to exit.

OPERATIONS 2 GUIDE 4.2* 169

Customer Codes (CUST) screen showing customer A assigned EDI profile DEMO

### 6 — SETTING UP THE EDI 810 INVOICE IN ECID (OPTIONAL) <a id="6-setting-up-the-edi-810-invoice-in-ecid-optional"></a>

In this program, you set up your EDI 810 electronic invoice for accessorial and renewal invoicing. For each customer that you invoice through EDI, you define the customer code, invoice type and document code (always 810A). You must set up one record in ECID for each unique combination of customer code/invoice type.
FIELD DESCRIPTIONS
Customer Code Mandatory
Your customer code or .ALL for all customers.
Invoice Type ACCE
RCPT
RENW
Your invoice type.

1 Enter ECID.
2 Click on Enter Criteria and Execute Query to see which customer/invoice type combinations have already been set up. If the customer/invoice type combination that you require has not been set up, click on Create Record.
3 Key in your customer code or use the pick list function to select it.
4 Key in your invoice type (ACCE, RCPT or RENW) and press Enter.
5 Key in 810A your document code and press Enter.
6 Repeat the above steps for each additional customer/invoice type combination that you wish to add.
ECID screen showing two invoice types set up
7 When you finish setting up your customer/invoice type combinations, click on Return to Main to exit create record mode then click on Exit to exit.

### COPYING EDI PROFILES IN CEDI <a id="copying-edi-profiles-in-cedi"></a>

You can copy EDI profiles from one company to another in CEDI (Copy EDI Profile). The profile that you copy can be copied under its original code or under a new code.
1 Enter CEDI.
2 Key in your from EDI profile code and press Enter or use your pick list to select the appropriate code.
3 Key in your to company code and press Enter.
4 Key in the code that this profile will use in your to company. You can choose the same code that you used in your from company or you can choose a new code.
Document Code Mandatory
Set to 810A. This document is set up in DOCU by HighJump.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 171

Copy EDI Profile Codes (CEDI) screen
5 Click on Process.

### Working With Orders and Receipts <a id="working-with-orders-and-receipts"></a>

If you set the Entry Type flag in DEDP (Depositor EDI Profile Code) to E for Entry, you can enter and modify 
EDI data at order or receipt creation. If you set the Entry Type flag in DEDP to C for Confirmation, you can enter and modify EDI data at order or receipt confirmation. If you set the Entry Type flag in DEDP to N for 
Never, you can look up EDI data in LOOR and LORE but you cannot modify it.

### ENTERING AND MODIFYING EDI DATA IN ENOR AT ORDER CREATION <a id="entering-and-modifying-edi-data-in-enor-at-order-creation"></a>

If you set the Entry Type flag in DEDP (Depositor EDI Profile Code) to E for Entry, you can enter and modify 
EDI data at order creation.
1 Enter ENOR.
2 Enter your header block information normally.

3 When you finish entering your header information, do one of the following:

ENOR screen showing prompt for depositor order number
4 When the Line Block appears, enter your line block information normally.
5 When you finish entering your line information, do one of the following:
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Key in your EDI value or values and press Enter. If the EDI values are filled in by the system, you can change them as required.
b) When you finish entering or modifying your EDI values, click on 
Exit to exit the EDI Block.
a) Proceed to step 4.
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Proceed to next step. a) Key in your EDI value or values and press Enter. If the EDI values are filled in by the system, you can change them as required.
b) When you finish entering or modifying your EDI values, click on 
Exit to exit the EDI Block.

OPERATIONS 2 GUIDE 4.2* 173

ENOR screen showing prompt for quantity ordered
6 When you finish entering your lines, click on Return to Main to exit create mode. Then click on Master 
Block and Exit to exit ENOR.

### MODIFYING EDI DATA IN ENOR AFTER ORDER CREATION <a id="modifying-edi-data-in-enor-after-order-creation"></a>

1 Enter ENOR.
2 Retrieve the order that you wish to modify.
3 Click on EDI Data.
4 Make your changes to the EDI values or values.
5 Click on Exit to exit the EDI Block.

### ENTERING AND MODIFYING EDI DATA IN ENRE AT RECEIPT CREATION <a id="entering-and-modifying-edi-data-in-enre-at-receipt-creation"></a>

If you set the Entry Type flag in DEDP (Depositor EDI Profile Code) to E for Entry, you can enter and modify 
EDI data at receipt creation.
1 Enter ENRE.
2 Enter your header block information normally.
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Press Enter until your cursor is positioned in the EDI Details field.
a) Click on Line Block.
b) Retrieve the line that you wish to modify.
c) Make sure that the EDI flag is set to Y for Yes.
d) Press Enter until your cursor is positioned in the EDI field.

3 When you finish entering your header information, do one of the following:

ENRE screen showing prompt for shipment date
4 When the Line Block appears, enter your line block information normally.
5 When you finish entering your line information, do one of the following:
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Key in your EDI value or values and press Enter. If the EDI values are filled in by the system, you can change them as required.
b) When you finish entering or modifying your EDI values, click on 
Exit to exit the EDI Block.
a) Proceed to step 4.
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Proceed to next step. a) Key in your EDI value or values and press Enter. If the EDI values are filled in by the system, you can change them as required.
b) When you finish entering or modifying your EDI values, click on 
Exit to exit the EDI Block.

OPERATIONS 2 GUIDE 4.2* 175

ENRE screen showing prompt for ID code
6 When you finish entering your lines, click on Return to Main to exit create mode. Then click on Master 
Block and Exit to exit ENRE.

### MODIFYING EDI DATA IN ENRE AFTER RECEIPT CREATION <a id="modifying-edi-data-in-enre-after-receipt-creation"></a>

1 Enter ENRE.
2 Retrieve the receipt that you wish to modify.
3 Click on EDI Data.
4 Make your changes to the EDI values or values.
5 Click on Exit to exit the EDI Block.

### LOOKING UP EDI DATA FOR ORDERS AND RECEIPTS <a id="looking-up-edi-data-for-orders-and-receipts"></a>

You look up EDI data for orders in LOOR (Look Up Orders). You look up EDI data for receipts in LORE (Look 
Up Receipts). The EDI flags in these programs must be set to Y for Yes before you can look up EDI information in them.
1 Enter LOOR or LORE.
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Press Enter until your cursor is positioned in the EDI Details field.
a) Click on Line Block.
b) Retrieve the line that you wish to look up.
c) Make sure that the EDI flag is set to Y for Yes.
d) Press Enter until your cursor is positioned in the EDI field.

2 Retrieve the order or receipt whose EDI information you wish to look up.
3 Click on EDI Data.

Look Up Orders (LOOR) screen showing prompt for depositor order number
4 Click on Exit to exit the EDI Block. Then click on Master Block (if available) and Exit to exit.

### RESUBMITTING AN OUTBOUND EDI TRANSACTION <a id="resubmitting-an-outbound-edi-transaction"></a>

If an outbound EDI transaction failed for any reason, you can resend it by reprinting the EDI document.
1 Enter REOR and requeue the EDI document.
2 Enter PROM or PROR and reprint the EDI document.

### Running EDI Programs from the Menu <a id="running-edi-programs-from-the-menu"></a>

There are four EDI programs that you can run from the menu:
 EDIA (EDI Adjustment Report)
 INEDI (EDI Inventory Report)
If the EDI transaction occurs at the header level:
If the EDI transaction occurs at the line level:
a) Make sure that the EDI flag is set to Y for Yes.
b) Press Enter until your cursor is positioned in the EDI field.
a) Click on Line Block.
b) Retrieve the line that you wish to look up.
c) Make sure that the EDI flag is set to Y for Yes.
d) Press Enter until your cursor is positioned in the EDI field.

OPERATIONS 2 GUIDE 4.2* 177
 UEDI (Update EDI Info for Confirmed Order)
 EDIV (EDI 811 Transaction Processing)

### REPORTING ADJUSTMENTS TO INVENTORY IN EDIA <a id="reporting-adjustments-to-inventory-in-edia"></a>

In this program, you report adjustments to inventory to your EDI partners. An adjustment to inventory is any adjustment processed in ENAJ (Inventory Adjustment), HOAD (Hold Adjustments), POHO (Put On Hold), 
MAHO (Take Off Holds) and HATO (Holds Auto Take-Off). You can restrict EDIA by customer code, adjustment number and adjustment code.
EDIA requires a document code set up in DOCU by HighJump and an adjustment type code set up in ADJU with the Send via EDI flag set to Yes. 
1 Enter EDIA.
2 Key in your customer code and press Enter or press Enter with this field blank to report on all customers.
3 Key in your adjustment number and press Enter or press Enter with this field blank to report on all adjustment numbers.
4 Key in your adjustment code and press Enter or press Enter with this field blank to report on all adjustment codes.
5 In the Document Code field, key in your document code and press Enter.

EDI Adjustment Audit (EDIA) screen showing report for customer A
6 Press Enter to bypass the Reprint Only field.
7 Key in NONE as your printer code and press Enter.
8 Click Ok to print.

### RESENDING A REPORT IN EDIA <a id="resending-a-report-in-edia"></a>

You can resend a previously reported EDI adjustment in EDIA by means of the Reprint Only flag.

1 Enter EDIA.
2 Press Enter three times to bypass the Customer Code, Adjustment Number and Adjustment Code fields.
3 In the Document Code field, key in your document code and press Enter.
4 In the Reprint Only field key in Y for Yes and press Enter.
5 Key in the audit number for the previously printed report and press Enter.
6 Key in your printer code and press Enter.
7 Click on Execute Report.

### REPORTING ON INVENTORY IN INEDI <a id="reporting-on-inventory-in-inedi"></a>

This inventory report is sent automatically to your trading partner through Nexus or other EDI software. You cannot print INEDI. INEDI supports the following transaction sets:
 846 (Inventory Report)
 852 (Product Activity Data)
1 Enter INEDI.

EDI Inventory Report (INEDI)
2 Key in your customer code and press Enter.
3 Key in your start date and press Enter.
4 Key in your end date and press Enter.
5 Key in your EDI transaction set and press Enter or use the pick list function to select it.
6 Click on Execute Report.

### UPDATING EDI DATA FOR CONFIRMED ORDERS IN UEDI <a id="updating-edi-data-for-confirmed-orders-in-uedi"></a>

You can update EDI data at the order line level for confirmed orders in UEDI. 
1 Enter UEDI.
2 Key in your order number and press Enter.

OPERATIONS 2 GUIDE 4.2* 179
3 Key in your order line number and press Enter.

Update EDI Info for Confirmed Order (UEDI)
4 Key in your new EDI value(s) over the existing value(s) and press Enter.
5 When you finish making your changes, click on Exit twice to exit.

### TRANSMITTING YOUR INVOICES IN EDIV <a id="transmitting-your-invoices-in-ediv"></a>

This function is only available if you have set up your EDI 810 invoice in ECID.
1 Enter EDIV.
2 Key in your register number and press Enter.
3 Key in your customer code and press Enter.
4 Key in your invoice type (ACCE, RENW or RCPT) and press Enter.

EDIV screen
5 If required, key in your invoice number and press Enter. If you do not enter an invoice number, the transmission will include all invoices for the customer and invoice type that you specify.
6 Click on Execute Report.

### Outputting EDI Reports in Text Format <a id="outputting-edi-reports-in-text-format"></a>

You can output EDI reports in text format rather than PDF format when sending the report to an e-mail recipient. This new feature requires setup by HighJump.

OPERATIONS 2 GUIDE 4.2* 181
