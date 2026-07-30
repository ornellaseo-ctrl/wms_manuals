---
title: "Documentos, Impressão e Etiquetas"
description: "BOL, pick sheets, invoices, labels, manutenção via DOCU/DOTP/FORM, BarTender, fax e auto-print."
layout: default
---

# Documentos, Impressão e Etiquetas

BOL, pick sheets, invoices, labels, manutenção via DOCU/DOTP/FORM, BarTender, fax e auto-print.

**Fluxo principal:** `FORM/DOTP/DOCU (define) -> PRPF/ADOP (perfil e impressora) -> BarTender (etiquetas)`

> Fonte: manuais E, O do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Faxing And Auto-Printing <a id="faxing-and-auto-printing"></a>

*Manual E — Operations 2*

### Overview <a id="overview"></a>

AccellosOne 3PL’s faxing and auto-printing functions offer a number of options.

### FAX NOTES <a id="fax-notes"></a>

A fax note consists of a fax cover sheet only with no document attached to it. You can send fax notes from your workstation using the program SEFX (Send Faxes).

### MANUAL FAXING <a id="manual-faxing"></a>

You can manually fax most AccellosOne 3PL documents from your workstation by entering FAX as your printer code.

### MANUAL E-MAILING <a id="manual-e-mailing"></a>

You can manually e-mail most AccellosOne 3PL documents from your workstation by entering MAIL as your printer code.

### SEMI-AUTOMATIC FAXING <a id="semi-automatic-faxing"></a>

Semi-automatic faxing allows you to fax according to a pre-established schedule any document that you have manually printed to the spooler. You can batch semi-automatic faxes so that all documents for the same customer, consignee, carrier, etc. are consolidated and sent as a single fax.

### FULLY AUTOMATIC E-MAILING, FAXING AND PRINTING <a id="fully-automatic-e-mailing-faxing-and-printing"></a>

In fully automatic e-mailing, faxing and printing, the document is programmed to print automatically to either a regular printer or to a “fax” printer. If you print to a fax printer, the document can be faxed or e-mailed either immediately or according to a pre-established schedule. 
Fax meets criteria in Faxing 
Block (CUST)
fax is transmitted 
No fax remains in spooler
Yes no transmission
Print Spooler you print to 
AFAX fax placed in print spooler

OPERATIONS 2 GUIDE 4.2* 183
The following chart shows the various faxing, e-mailing and auto-printing options in AccellosOne 3PL.
FUNCTION DESCRIPTION SETUP
MANUAL 
Fax Notes A fax note consists of a fax cover sheet only with no document attached to it. 
None You send fax notes from the program SEFX (Send 
Faxes).
Manual Faxing You can manually fax most AccellosOne 
3PL documents.
None You enter FAX as your printer code.
Manual E-Mailing You can manually e-mail most AccellosOne 3PL documents.None You enter MAIL as your printer code.
Semi-Automatic 
Faxing
After you manually print the document to the spooler, the fax will be transmitted according to the schedule that you set up in the Faxing Block of CUST. 
You set up a record in the 
Faxing Block of CUST.
You enter AFAX as your printer code.
Auto-Faxing and 
E-Mailing of Documents
When the document prints, it is sent to the print spooler. At the time and on the day that you specify in the Faxing Block of CUST, the system will fax or e-mail the document.
You set up a record in the 
Faxing Block of CUST.
You set the printer code field in DOCU to AFAX.
You set the Type field in DIFP to A for Auto-Print.
You set the Auto-Allocate/
Print flag in ORPR or RCPR to Y for Yes.
None
You set up autoprinting of documents in DOCU.
DOCU
Fax/e-mail meets criteria in Faxing 
Block (CUST)
fax/e-mail is transmitted 
No
Yes no transmission
Print Spooler fax/e-mail placed in print spooler fax/e-mail remains in spooler

### REQUIREMENTS <a id="requirements"></a>

There are two external requirements for faxing:
 The VSI-FAX software must be installed on your system. Certain faxing parameters such as the maximum number of tries, the frequency of faxing, etc. are set up in VSI-FAX.
 Your spooler must be activated.

### Setting Up Cover Sheet Codes and Fax Overlay Codes <a id="setting-up-cover-sheet-codes-and-fax-overlay-codes"></a>

The faxing system in AccellosOne 3PL supports both fax cover sheets and fax overlays.
A fax overlay is an overlay of lines, column headings and other graphic elements that appear on the fax. 
When combined with the variable data in the report or document, the resulting document resembles a paperbased bill of lading, warehouse receipt, etc. If you do not use an overlay, the document or report will be sent in its standard printed format.
In AccellosOne 3PL you create the codes for fax cover sheets and overlays, but not the cover sheets and overlays themselves. The actual fax cover sheets and fax overlays are custom documents and require special programming by HighJump.

### SETTING UP A COVER SHEET IN FXCS <a id="setting-up-a-cover-sheet-in-fxcs"></a>

You set up fax cover sheet codes in FXCS (Fax Cover Sheet). 
1 Enter FXCS.
2 Key in your cover sheet code and press Enter.
3 Key in your fax cover sheet description and press Enter.
Auto-Printing of 
Documents
When you time-stamp the flow to which the document is attached, the document will automatically print on the printer that you specify in DOCU.
HighJump creates a cron job in Unix.
You set the printer code field in DOCU to the appropriate printer.
You set the Type field in DIFP to A for Auto-Print.
You set the Auto Allocate/
Print flag in ORPR or RCPR to Y for Yes.
None
FUNCTION DESCRIPTION SETUP
MANUAL 

OPERATIONS 2 GUIDE 4.2* 185

Fax Cover Sheet (FXCS)
4 Repeat steps 3 and 4 for each additional fax cover sheet that you wish to add.
5 When you finish adding your fax cover sheets, click on Return to Main and Exit to exit.

### ATTACHING YOUR COVER SHEET TO YOUR WAREHOUSE IN WARE <a id="attaching-your-cover-sheet-to-your-warehouse-in-ware"></a>

If you use semi-automatic or automatic faxing, you can attach your cover sheet to your warehouse in WARE and AccellosOne 3PL will automatically transmit the cover sheet with the report or document that you are faxing.
NOTE Attaching a fax cover sheet to a warehouse is only possible if you maintain separate warehouses for each customer. If the same warehouse can contain product for multiple customers, you must attach your fax cover sheet to each customer in the 
Faxing Block of CUST.

Warehouse and Location (WARE) screen showing fax cover sheet B

### SETTING UP A FAX OVERLAY IN FXOL <a id="setting-up-a-fax-overlay-in-fxol"></a>

You set up your fax overlay codes in FXOL (Document Overlay).
1 Enter FXOL.
2 Key in your fax overlay code and press Enter.
3 Key in your fax overlay code description and press Enter.
4 In the Overlay Side field, key in F for Front and press Enter.

Document Overlay (FXOL)
5 Repeat steps 3 and 4 for each additional fax overlay code that you wish to add.
6 When you finish adding your fax overlay codes, click on Return to Main and Exit to exit.

OPERATIONS 2 GUIDE 4.2* 187

### Sending a Fax Note in SEFX <a id="sending-a-fax-note-in-sefx"></a>

A fax note consists of a fax cover sheet only with no report or document attached to it. You send fax notes from the program SEFX (Fax/Mail Entry). 
1 Enter SEFX.

Send Faxes (SEFX)
2 In the Send To Code field, key in the account code that you are sending to and press Enter. If you are sending to a non-account recipient, key in a forward slash (/) and press Enter. Then enter the name of your recipient in the Name field and press Enter.
3 In the Fax Number field, key in your fax number and press Enter. If you have set up a fax number in the 
Telephone Block of the account that you are sending to, that number will appear in the Fax Number field. 
Press Enter to accept the number or key in a new fax number and press Enter.
When entering fax numbers, do not use hyphens to separate 1 from the area code or the area code from the fax number; for example, you enter 19054159778 not 1-905-415-9778.
4 If required, key in a name in the Attention field and press Enter.
5 If required, change the Send Time and From Name values.
6 If you have a fax cover sheet, key in your fax cover code and press Enter. If you do not have a fax cover sheet, press Enter to bypass this field.
7 If required, enter your comments and press Enter. Comments print on the fax cover sheet.
8 Press Enter until your cursor is positioned in the Text field.

Send Faxes (SEFX)
9 Key in the text of your fax note and press Enter.
10 If required, key in a second line and press Enter again. You can enter as many lines as you wish. 
11 When you finish adding your lines of text, click on Return to Main to exit create mode.
12 Click on Send Fax.

### Manually Faxing a Document <a id="manually-faxing-a-document"></a>

You can manually fax most AccellosOne 3PL documents. Manual faxes do not require setup in CUST or any other program.
1 Enter the program in which you print the document.
2 Enter any required parameters for the document.
3 Click on Print Block.
4 Key in FAX and press Enter. 
5 Click Ok. The Fax Setup Block will appear.

OPERATIONS 2 GUIDE 4.2* 189

Faxing Block for document
6 In the Send To Code field, key in the account code that you are sending to and press Enter. If you are sending to a non-account recipient, key in a forward slash (/) and press Enter. Then enter the name of your recipient in the Name field and press Enter.
7 In the Fax Number field, key in your fax number and press Enter. If you have set up a fax number in the 
Telephone Block of the account that you are sending to, that number will appear in the Fax Number field. 
Press Enter to accept the number or key in a new fax number and press Enter.
When entering fax numbers, do not use hyphens to separate 1 from the area code or the area code from the fax number; for example, you enter 19054159778 not 1-905-415-9778.
8 If required, key in a name in the Attention field and press Enter.
9 If required, change the Send Time and From Name values.
Faxing Block for document
10 If you have a fax cover sheet, key in your fax cover code and press Enter. If you do not have a fax cover sheet, press Enter to bypass this field.
11 If required, enter your comments and press Enter. Comments print on the fax cover sheet.
12 Click on Send Fax.

### Sending an E-Mail Message in SEFX <a id="sending-an-e-mail-message-in-sefx"></a>

E-mailing in AccellosOne 3PL requires special setup by HighJump.
1 Enter SEFX.
Send Faxes (SEFX)
2 In the Send To Code field, key in the account code that you are sending to and press Enter. If you are sending to a non-account recipient, key in a forward slash (/) and press Enter. Then enter the name of your recipient in the Name field and press Enter.
3 In the Fax Number field, key in your e-mail address and press Enter. You can send to multiple addresses by separating each e-mail recipient by a semi-colon; for example, jdoe@HighJump.com; 
bsmith@HighJump.com
4 If required, key in an e-mail address in the Cc field and press Enter.
5 If required, key in your subject line and press Enter.

OPERATIONS 2 GUIDE 4.2* 191

SEFX screen for e-mail
6 In the Text field, key in the text of your e-mail message and press Enter.
7 If required, key in a second line and press Enter again. You can enter as many lines as you wish. 
8 When you finish adding your lines of text, click on Return to Main to exit create mode.
9 Click on Send e-Mail.

### Manually E-Mailing a Document <a id="manually-e-mailing-a-document"></a>

You can e-mail most AccellosOne 3PL documents to any valid e-mail address. Your document will be sent in either PDF or WRI format and can be printed by your recipient on any printer as an attachment. 
1 Enter the program in which you print the document.
2 Enter any required parameters for the document.
3 Click on Print Block.
4 Key in MAIL and press Enter.
5 Click Ok. The Fax/Mail Entry Block will appear.

Faxing Block for document
6 In the e-mail To field, key in your e-mail address and press Enter. You can send to multiple addresses by separating each e-mail recipient by a semi-colon; for example, jdoe@HighJump.com; 
bsmith@HighJump.com
7 If required, key in an e-mail address in the Cc field and press Enter.
8 If required, key in your subject line and press Enter.

Faxing Block for e-mail
9 Click on Send e-Mail.

OPERATIONS 2 GUIDE 4.2* 193

### Semi-Automatic Faxing <a id="semi-automatic-faxing"></a>

With semi-automatic faxing, the system will fax out a document at a specified time on a specified day after it has been printed to the spooler. There are two requirements for semi-automatic faxing: you must set up your fax recipient in the Faxing Block of CUST and you must print to the AFAX printer code.
The AFAX printer code must be set up as follows in PRIN: the system printer assigned to AFAX must be in all uppercase letters (for example, FAX) and this printer must be defined in PRIN as a regular non-system printer.
The fax recipient of a semi-automatic fax must be an account in AccellosOne 3PL; that is, a customer, carrier, shipper, consignee or sold-to. If you wish to fax the document to multiple accounts or to multiple numbers belonging to the same account, you must set up multiple records in the Faxing Block of CUST.
NOTE You cannot modify the document type, document code, account code or fax number of an existing record in the Faxing Block of CUST. If you wish to make changes to any of these fields, you must delete the record and create a new record with the correct values.
FIELD DESCRIPTIONS
Document Type S = Selection (Signature Capture documents only)
D = Document (used for documents)
The selection that you make in this field determines which codes you can select in the Document Code field.
Document Code Mandatory
The document that you wish to fax. Only documents attached to a flow in DIFP and printable in PROM/PROR/PRRM/PRRE can be faxed.

Account Code Mandatory
The customer, carrier, shipper, consignee or sold-to that the fax is to be sent to.
For receipt documents, the account code can be a customer, carrier or shipper. The consignee and sold-to are not available for receipt documents.
For order documents, the account code can be a customer, carrier, consignee or sold-to. The shipper is not available for order documents.
Fax Number/e-Mail Mandatory
The fax number of your recipient.
Effective Date Mandatory
The date that you want automatic faxing to begin.
Fax Type B = Batch
O = One at a time
If you select batch, the system will group all documents going to the same customer, carrier, shipper, consignee or sold-to in a batch and send the batch as one fax.
If you select one at a time, the system will send individual faxes out one at a time. No batching will occur. 
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 195
Weekday Only available for Fax Type of Batch
D = Daily
FRI = Friday
M = Monthly
MON = Monday
SAT = Saturday
SUN = Sunday
THUR = Thursday
TUES = Tuesday
WED = Wednesday
WEEK = Weekdays
The day of the week or frequency that the fax should be sent.
Occurrence Only available for Fax Type of Batch
The number of times a day that you would like the system to check the print spooler for any faxes to be sent. If there are faxes to be sent, the system will send them.
EXAMPLES
0000 = once a day
0100 = every hour
1200 = every 12 hours
Start Time Mandatory
The time that you would like the system to start checking for and sending faxes. The format is HHMM using the 24-hour clock (for example, to start faxing at 8:00 pm, enter 2000).
If you do not want to specify a starting time, enter 0001 for one minute after midnight.
NOTE Make sure that your system is operational at your starting time. You cannot enter a starting time of 10:00 pm if you are performing a system backup at this time. 
Attention Mandatory
The name of the person that the fax will be going to.
FIELD DESCRIPTIONS

### SETTING UP NON-BATCH FAXING <a id="setting-up-non-batch-faxing"></a>

In non-batch faxing, the system will send individual faxes out one at a time. Faxes will not be grouped by customer, carrier, shipper, etc. and sent out as a single fax.
1 Enter CUST.
2 Retrieve the customer that you wish to set up for faxing.
3 Continue to press F3 until you reach the Fax/E-Mail Block. If there is already a record set up in this block, click on Create Record.
4 In the Document Type field, key in D for Document and press Enter.
5 In the Document Code field, use your pick list to select the report or document that you wish to fax.
6 In the Account Code field, use your pick list to select the appropriate account (carrier, shipper, consignee, customer or sold-to) to which the fax is to be sent.
7 Key in your fax telephone number and press Enter. When entering fax numbers, do not use hyphens to separate 1 from the area code or the area code from the fax number; for example, you enter 
19054159778 not 1-905-415-9778.
8 In the Effective Date field, key in the date that you want semi-automatic faxing to start.
9 In the Fax Type field, key in O for One at a time and press Enter.
10 Key in your starting time and press Enter.
11 In the Attention field, key in the name of the recipient of the fax and press Enter. If the name is already filled in, press Enter to accept it or key in a new name and press Enter.
12 Press Enter to bypass the From field.
From The sender of the fax. The system will automatically enter your operator code in this field.
Comments Optional
Any comments that you enter here will appear on the fax cover sheet.
Cover Code Optional
The fax cover sheet code. Fax cover sheets require special programming by 
HighJump.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 197

Faxing Block (CUST)
13 Key in your comments and press Enter or press Enter to bypass this field.
14 Use your pick list to select the appropriate cover sheet code or press Enter to bypass this field.
15 If you want to fax the same document to another account or another number belonging to the same account, repeat the above steps for the second account/number.
16 When you finish setting up the Faxing Block, click on Return to Main to exit create mode. Then click on 
F4 the required number of times to exit.

### SETTING UP BATCH FAXING <a id="setting-up-batch-faxing"></a>

In batch faxing, the system will group all documents or reports going to the same customer, carrier, shipper, consignee or sold-to in a batch and send the batch as one fax.
1 Enter CUST.
2 Retrieve the customer that you wish to set up for faxing.
3 Click on F3 until you reach the Fax/E-Mail Block. If there is already a record set up in this block, click on 
Create Record.
4 In the Document Type field, key in D for Document and press Enter.
5 In the Document Code field, use your pick list to select the report or document that you wish to fax.
6 In the Account Code field, use your pick list to select the appropriate account (carrier, shipper, consignee, customer or sold-to) to which the fax is to be sent.

7 Key in your fax telephone number and press Enter. When entering fax numbers, do not use hyphens to separate 1 from the area code or the area code from the fax number; for example, you enter 
19054159778 not 1-905-415-9778.
8 In the Effective Date field, key in the date that you want automatic faxing to start.
9 In the Start Time field, press F9 to position your cursor in the Fax Type field.
10 Key in B for Batch and press Enter.
11 Use your pick list to select the appropriate weekday option (daily, monthly, each Monday, etc.).
12 In the Occurrence field, key in the number of times a day that you want the system to check for and send faxes and press Enter.
13 Key in your starting time and press Enter.
14 In the Attention field, key in the name of the recipient of the fax and press Enter. If the name is already filled in, press Enter to accept it or key in a new name and press Enter.
15 Press Enter to bypass the From field.

Faxing Block (CUST) showing a setup in which the system will check every hour for faxes to be sent
16 Key in your comments and press Enter or press Enter to bypass this field.
17 Use your pick list to select the appropriate cover sheet code or press Enter to bypass this field.
18 If you want to fax the same document to another account, repeat the above steps for the second account. 
19 When you finish setting up the Faxing Block, press F4 the required number of times to exit.

OPERATIONS 2 GUIDE 4.2* 199

### USING VARIABLES IN THE ATTENTION LINE OF A FAX <a id="using-variables-in-the-attention-line-of-a-fax"></a>

You can generate an attention line for auto-faxes containing a variable. For example, “Order Number: 
123456” or “Order Reference #: 999999”.
You set up an attention line for auto-faxes by entering “YOUR TEXT <TABLE_NAME.COLUMN_NAME>” in the Attention field. The table name must be an order and receipt table; other tables in AccellosOne 3PL are not supported.
This feature is supported in the following core documents:
 d301n (Standard Bill of Lading 2)
 d303an (Receipt Invoice)
 d303n (Receipt Notice)
 d2000 (Pick Sheet)
 d2001 (Standard Bill of Lading 1)
 d100od (interface that calls outbound core documents)
 d100id (interface that calls inbound core documents)
Fax / e-Mail Block of CUST screen showing attention line for faxes
If you make a mistake in syntax, the fax will be sent with the text that you entered in CUST rather than the order/receipt variable from the table.

### SENDING A SEMI-AUTOMATIC FAX <a id="sending-a-semi-automatic-fax"></a>

You send a semi-automatic fax by printing to the printer code AFAX. AFAX places the report or document in the print spooler.
1 Enter the program in which you print the report or document.
2 Enter the parameters for the desired report or document and click on Print Block to display the Printer 
Block.
3 Key in AFAX as your printer code and press Enter.

When you print to AFAX, the document will be sent to the spooler. At the time that you specified in the Faxing 
Block in CUST, the system will retrieve the document from the spooler and fax it to the recipient that you selected in CUST.

### Auto-Printing of Documents <a id="auto-printing-of-documents"></a>

There are two output options for an auto-printed document:
 you can print it to a regular printer
 you can print it to the printer AFAX (the document will be sent to the spooler and then faxed or e-mailed according to the parameters that you specify in the Faxing Block of CUST)
If required, you can print one document to the printer and fax a copy of the same document to the customer. 
In order to do so, you must set up two separate documents in DOCU.
There are six setup programs required for auto-printed documents:
 a cron job in Unix (set up by HighJump)
 DOCU (Documents)
 DIFP (Depositor Workflow Profile)
 ORPR (Order Priorities) or RCPR (Receipt Priorities)
 COMP (Company Code)
 Faxing Block of CUST (Customer Setup) — only required if you are printing to AFAX

### SETTING UP YOUR DOCUMENT IN DOCU <a id="setting-up-your-document-in-docu"></a>

In DOCU you set up the document that you wish to auto-fax, e-mail or auto-print. If you wish to set up two documents — one for regular printing and one for auto-faxing — the document for faxing should be identical to the non-faxing document except for the printer code. You set the printer code of the document to be faxed to AFAX.
If you wish to add auto-fax capability to an existing document, retrieve the existing document and note the values in each field. You will need to know these values when you set up your new auto-faxing document.
1 Enter DOCU.
2 Key in your new document code (for example, TAL2 for Tally Sheet 2) and press Enter.
3 In the remaining DOCU fields, enter the appropriate values. If you are setting up an auto-fax document for an existing print document, make sure that all values for both documents are the same except for the printer code.
4 In the Printer Code field, key in the appropriate code (AFAX for faxing/e-mailing or a printer code for printing to a printer) and press Enter. 
5 If required, enter a document directory, document file prefix and document file suffix. If you do not need this information, press Enter to bypass these fields.
6 Click on Return to Main to return to Main Mode.

OPERATIONS 2 GUIDE 4.2* 201

Documents (DOCU) showing a receiving tally whose printer code has been set to AFAX
7 When you finish adding your document, click on Exit to exit.
ATTACHING YOUR DOCUMENT TO YOUR DEPOSITOR WORKFLOW PROFILE IN 
In DIFP you attach the document that you set up in DOCU to the flow at which you want the document to be faxed. The Type field in the Document Block must be set to A for Auto-Print.
If you are faxing the document to a shipper or consignee and if that shipper or consignee has a DIFP profile that differs from the customer’s DIFP profile, you must attach the document to the shipper or consignee’s 
DIFP profile — not the customer’s DIFP profile.
1 Enter DIFP.
2 Retrieve the profile that you wish to modify for auto-printing.
3 Click on In/Out Block.
4 In the In/Out Block, use your up and down arrow keys to select the appropriate option.
5 Click on Flow Block.
6 Select the flow at which you wish to attach the document.
7 Click on Document Block.
8 If there is already a document attached to the flow, click on Create Record.
9 Key in a sequence number and press Enter.
10 In the Document Code field, key in the code of the document that you created in DOCU and press Enter.
11 Key in your form code and press Enter.

12 In the Type field, key in A for Auto-Print and press Enter.

Depositor Workflow Profile screen showing the document TALF set up for auto-faxing
13 When you finish setting up your document, click on F4 the required number of times to exit.

### SETTING UP YOUR ORDER/RECEIPT PRIORITIES IN ORPR OR RCPR <a id="setting-up-your-order-receipt-priorities-in-orpr-or-rcpr"></a>

For order documents, you must set the Auto-Allocate/Print flag in ORPR to Y for Yes for all order priorities that require auto-printing of documents. For receipt documents, you must set the Auto-Allocate/Print flag in RCPR to Y for Yes for all receipt priorities that require auto-printing of documents.
1 Enter ORPR or RCPR.
2 Click on Enter Criteria then Execute Query to display your order or receipt priorities.
3 Make sure that the Auto-Allocate/Print flag is set to Y for Yes for all order or receipt priorities that require 
Type field set to 
A for Auto-Print

OPERATIONS 2 GUIDE 4.2* 203

Order Priorities (ORPR) screen showing Auto-Allocate/Print flag set to Yes

Receipt Priorities (RCPR) screen showing Auto-Allocate/Print flag set to Yes
4 When you finish setting up your order or receipt priorities, click on Exit to exit.

### DEFINING THE PRINT SEQUENCE OF YOUR DOCUMENTS IN COMP <a id="defining-the-print-sequence-of-your-documents-in-comp"></a>

If required, you can sequence the printing of auto-printing documents by company code. For example, if you set company W1 to 1 and company W2 to 5, W1’s auto-printed documents will be printed before W2’s autoprinted documents.
If you do not define an auto-process sequence number in COMP, auto-printed documents will be printed in company code sequence.
1 Enter COMP.

2 Retrieve the company whose auto-print documents you wish to sequence.
3 Press Enter until your cursor is positioned in the Auto-Process Sequence Number field.
4 Key in your sequence number and press Enter.

Company Code (COMP) showing company V6 assigned a sequence number of 1
5 Repeat the above steps for each additional company that you wish to set up.
6 When you finish setting up your companies, click on Return to Main and Exit to exit. 

### SETTING UP THE FAXING BLOCK IN CUST FOR AUTOMATIC FAXING <a id="setting-up-the-faxing-block-in-cust-for-automatic-faxing"></a>

This step is only required if you specified AFAX as your printer code in the program DOCU (Documents). See [Semi-Automatic Faxing](documentos-impressao.html#semi-automatic-faxing) for complete setup instructions.

### SETTING UP THE FAXING BLOCK IN CUST FOR AUTOMATIC E-MAILING <a id="setting-up-the-faxing-block-in-cust-for-automatic-e-mailing"></a>

With automatic e-mailing, the system will e-mail out a document in PDF format that can be printed by your recipient on any printer as an attachment. There are two requirements for automatic e-mailing in addition to the special e-mail setup by HighJump: you must set up your e-mail recipient in the Faxing Block of CUST and you must print to the AFAX printer code.

OPERATIONS 2 GUIDE 4.2* 205
The recipient of a semi-automatic e-mail message must be an account in AccellosOne 3PL; that is, a customer, carrier, shipper, consignee or sold-to. If you wish to e-mail the document to multiple accounts, you must set up multiple records in the Faxing Block of CUST.
FIELD DESCRIPTIONS
Document Type S = Selection (Signature Capture documents only)
D = Document (used for documents)
The selection that you make in this field determines which codes you can select in the Document Code field.
Document Code Mandatory
The document that you wish to e-mail. Only documents attached to a flow in 
DIFP and printable in PROM/PROR/PRRM/PRRE can be e-mailed.
Account Code Mandatory
The customer, carrier, shipper, consignee or sold-to that the e-mail message is to be sent to.
For receipt documents, the account code can be a customer, carrier or shipper. The consignee and sold-to are not available for receipt documents.
For order documents, the account code can be a customer, carrier, consignee or sold-to. The shipper is not available for order documents.
Fax Number/e-Mail To Mandatory
The e-mail address of your recipient. You can send to multiple addresses by separating each e-mail recipient by a semi-colon.
Cc Optional
The e-mail address of your cc recipient.
Effective Date Mandatory
The date that you want automatic e-mailing to begin.

1 Enter CUST.
2 Retrieve the customer that you wish to set up for automatic e-mailing.
3 Continue to press F3 until you reach the Faxing Block. If there is already a record set up in the Faxing 
Block, click on Create Record.
4 In the Document Type field, key in D for Document and press Enter.
5 In the Document Code field, use your pick list to select the report or document that you wish to e-mail.
6 In the Account Code field, use your pick list to select the appropriate account (carrier, shipper, consignee, customer or sold-to) to which the e-mail message is to be sent.
7 Key in your e-mail address and press Enter. You can send to multiple addresses by separating each email recipient by a semi-colon; for example, jdoe@HighJump.com;bsmith@HighJump.com
8 If required, key in a Cc address for the e-mail and press Enter. If you do not need a Cc address, press 
Enter to bypass this field.
9 In the Effective Date field, key in the date that you want semi-automatic e-mailing to start.
10 Key in 0000 as your starting time and press Enter.
11 In the Attention field, key in the name of the recipient of the document and press Enter. If the name is already filled in, press Enter to accept it or key in a new name and press Enter.
12 Make any necessary changes to the value in the From field. If there is an embedded space in your from name, you must change the name or remove the embedded space.
Start Time Mandatory
Set to 0000.
Attention Mandatory
The name of the person that the e-mail message will be going to.
From The sender of the e-mail message. The system will automatically enter your operator name in this field. If your operator name has embedded spaces, you must remove the embedded spaces or change the name.
Comments Optional
Any comments that you enter here will appear on the subject line of the e-mail message.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 207

Faxing Block (CUST)
13 Key in your comments and press Enter or press Enter to bypass this field.
14 If you want to e-mail the same document to another account, repeat the above steps for the second account.
15 When you finish setting up the Faxing Block, click on Master Block and Exit to exit.

### USING VARIABLES IN THE SUBJECT LINE OF AN E-MAIL <a id="using-variables-in-the-subject-line-of-an-e-mail"></a>

You can generate a subject line for automatic e-mails containing a variable. For example, “Order Number: 
123456” or “Order Reference #: 999999”.
You set up a subject line for automatic e-mails by entering “YOUR TEXT <TABLE_NAME.COLUMN_NAME>” 
in the Comments field. The table name must be an order and receipt table; other tables in AccellosOne 3PL are not supported. 
This feature is supported in the following core documents:
 d301n (Standard Bill of Lading 2)
 d303an (Receipt Invoice)
 d303n (Receipt Notice)
 d2000 (Pick Sheet)
 d2001 (Standard Bill of Lading 1)
 d100od (interface that calls outbound core documents)
 d100id (interface that calls inbound core documents)

Fax / e-Mail Block of CUST screen showing subject line for e-mails
If you make a mistake in syntax, the e-mail will be sent with the text that you entered in CUST rather than the order/receipt variable from the table.

### Scheduling Auto-Printed Documents for a Consignee <a id="scheduling-auto-printed-documents-for-a-consignee"></a>

You can schedule auto-printed documents for a given consignee by setting up a day profile code in DAPC. 
You use day profile codes when you wish to schedule order allocation for a particular consignee. For example, you can specify that you only want to ship product to Store A on Mondays between noon and 9:00 pm. For store B, on the other hand, you will ship product on Tuesdays and Thursdays between 8:00 am and 
4:00 pm.
If you do not specify a day profile code for a consignee, this means that you want to ship to that consignee whenever an order is processed.
The day profile code that you set up DAPC is attached to a consignee in CONS. To activate a day profile code, you must set the Allocate Days flag in ORPR (Order Priorities) to C for Consignee.
When you start allocation, the system checks the current time and date to determine whether they fall within the limits set up in DAPC. If they do, a location is attached to the order (that is, pick from location x) and the order proceeds normally.
If the current time and date do not fall within DAPC limits, no allocation takes place (that is, no location is assigned to the order). The order remains on the system unallocated until the allocation routine is run again. 
The allocation routine is run each time that you print a pick sheet or other document for the order that requires allocation. Allocation is also triggered by certain RF programs.

OPERATIONS 2 GUIDE 4.2* 209
EXAMPLE
You set up a consignee and specify that you only want to ship to this consignee on 
Thursday mornings. If you print a pick document for this consignee on Thursday afternoon, no allocation will take place because this order is outside of the DAPC limits. The order will remain on the system until the following Thursday.
If you print a pick document for this order on the following Thursday, the order will be allocated. If you do not print a pick document for the order on the following Thursday, the order will remain on the system for another week. And so on and so forth.

### TIME BLOCK <a id="time-block"></a>

If you activate the day of the week flag but do not set a start and end time in this block, order allocation can occur at any time over the course of the day.
FIELD DESCRIPTIONS
Day Profile Code Mandatory
Your day profile code.
Description Mandatory
Your description for the day profile code.
Monday/Tuesday /
Wednesday, etc. Active 
Flag
Y = Yes
N = No
If you set this flag to Yes, order allocation will be activated for that day of the week and you can specify a time range in the Time Block. If you do not enter a time range, order allocation can occur around the clock on that day.
If you set this flag to No, no order allocation will occur on that day for the consignee to which this profile is attached. 
Start Time The starting time for the day of the week that you specified in the header block. You enter your starting time in HH:MM format followed by either am or pm; for example, to specify 8:30 am you would enter 08:30am and to specify 
4:00 pm you would enter 04:00pm.
End Time The ending time for the day of the week that you specified in the header block.

### PROCEDURE <a id="procedure"></a>

1 Enter DAPC.
2 Click on Create Record.
3 Key in your day profile code and press Enter.
4 Key in your day profile code description and press Enter.
5 In the Monday Active Flag field, key in the appropriate value (Y for Yes or N for No) and press Enter.
6 Repeat the above steps for each additional day of the week that you wish to set up.
If you enter Yes: If you enter No:
Your cursor will be positioned in the Start 
Time field in the Time Block. 
a) If you require a start and end time, key in your start time and press Enter. If you do not require a start and end time, click on 
Master Block to exit the Time 
Block. Then press Enter to position your cursor over the appropriate day of the week and repeat step 5 for that day.
b) Key in your end time and press 
Enter.
c) If you wish to define a second time period for the same day, repeat the above steps. 
d) When you finish entering your times, click on Return to Main and Master Block to return to the header block.
a) Repeat the previous step for the next day of the week.

OPERATIONS 2 GUIDE 4.2* 211

Day Profile Code screen showing order allocation activated on weekdays with a time range of 12 noon to 6:30 pm on Tuesdays
7 When you finish setting up your day profile code, click on Exit to exit. 

### Defining the Print Sequence of Auto-Printed Documents <a id="defining-the-print-sequence-of-auto-printed-documents"></a>

You can define the sequence in which order documents in the print queue are processed by activating the appropriate print sequence value in COMP (Company Parameters Block). 
By specifying the sequence in which order documents are printed (typically a pick sheet or other allocation type document), you can ensure that higher priority orders are allocated first followed by lower priority orders. 
Depending on the option that you choose, AccellosOne 3PL will look at the order priority, order number, to ship date and the sequence in which order numbers are entered in PROM when deciding which order documents to print and allocate first.
NOTE Defining the print sequence of auto-printed documents works best when orders are batched (for example, you confirm entire loads in CHOF) and your cron job in Unix is set up to run at longer intervals such as every half hour. If you print individual order documents in short succession and if your cron job runs every two minutes, you will derive little benefit from print sequences.

You define the priority of an order by entering a value in the Priority field in ENOR.
AccellosOne 3PL supports four different print sequence options. If you do not specify an option, AccellosOne 
3PL will use PRI, the system default.
COMP screen showing Print Sequence Code for Auto-Printed Documents set to MPRI
CODE DESCRIPTION
PRI The sequence is order priority and order number.
MPRI The sequence is modified order priority, To Ship date in ENOR and order number. The order priority is modified as follows: 
 for orders with a To Ship date in the future, 10 is added to the order priority
 for orders with a To Ship date that equals the current system date, 2 is added to the order priority
 for orders with a To Ship date in the past, no change is made to the order priority
PSDT The sequence is order priority, To Ship date in ENOR and order number.
PROM The sequence is the order in which order numbers are entered in PROM (Print Shipping 
Documents - Specific).

OPERATIONS 2 GUIDE 4.2* 213

## Listing Of Core Documents <a id="listing-of-core-documents"></a>

*Manual O — Core Documents*

# Manual O — Core Documents Guide (Documentos e Impressão)
> **ID do Manual:** O  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Gestão de documentos do sistema: BOL, packing slips, pick sheets, invoices, labels (receiving/shipping/MH10/UCC-128), tallies. Setup em FORM/DOTP/DOCU/BATP. Overlays, Oracle Reports, SSRS. BarTender label printing integration.
---

### Accessorial Audit Report <a id="accessorial-audit-report"></a>

This document shows charge codes plus the inventory to which the charge codes apply. Charge codes are sorted in customer code/level 2 value/accessorial number order. If there are multiple customers in the report, the document shows the total charges for each customer plus the total charges for the report.
You can restrict this audit report in BILB (Billing Batch) by customer code, level 1/2/3 values and charge code. 
As well, you can summarize the report by customer, customer/level 1, customer level 1/2, customer level 1/2/
3 and customer/charge code.
PRINT FORM NAME: 6000
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
ABC Warehousing Inc. /u02/app/develop/del4/work/faxlp/04291550g00443 Page 2 of 2
Accessorial Audit Report SECTION 1 of 1
 BATCH # : 98 - Audit # : 2 - Batch Date : 02.06.07
Print Date : 04.29.08 Batch Description : All Customers Section Page 2 of 2
------------------------------------------------------------------------------------------------------------------------------------
Accessorial Number Date Reference Number Reference Description
 Charge Code & Description Quantity Rate Total Amount
A Customer A
=========================
 45417 09-JAN-06
 BF1 Blast Freezing 1 20.00 1.2500 25.00
 45418 09-JAN-06
 C1 Case Rate 25.00 0.7500 18.75
 45419 09-JAN-06
 BOL Bill of Lading Charge 2.00 25.0000 50.00
 47593 17-FEB-06
 BOL Bill of Lading Charge 1.00 100.0000 75.00
 47783 21-FEB-06
 BOL Bill of Lading Charge 1.00 85.0000 85.00
 44185 11-DEC-05 CRM 1306
 LAB Extra Labour Charges 2.00 60.0000 120.00
 ----------
 Total Charges : 900.53
 Audit Charges : 900.53
 ==========
End of Section # 1

### Accessorial Invoice <a id="accessorial-invoice"></a>

This document shows all charges on the accessorial invoice. Depending on your invoicing type (IND, UALL, 
UREC or UREN), charges will be broken down by charge type (accessorial charges, receipt charges, renewal charges, etc.).
There are three possible summary options for this invoice: print summary after invoice details (default), print summary on new page and print summary only (that is, no invoice details). You define the summary on new page and summary only options in DEAS by attaching the appropriate code (SUMMARY-ON-NEW-PAGE or 
SUMMARY-ONLY) to the DEAS code “ACIN”. Then you attach your DEAS code to the appropriate customers in CUST.
If you do not set up summary options in DEAS, the summary default — print summary immediately following invoice details without a page break — will be used.
DEAS screen showing ACIN code with summary on new page option
PRINT FORM NAME: ba_203
OVERLAYS SUPPORTED: HUAL (front page only)
ADDITIONAL PRINTS SUPPORTED: Y

ABC Warehousing, Inc.
 100 Renfrew Drive
 Suite 100 12.06.05 A-000036
 Markham ON L3R 9R6
 Two Installments 1
 INVOICE
 Customer D
 100 Renfrew Drive
 Markham ON L3R 6B3
 Canada
Receipt WR - 1160 Dtd: 11.01.05
 D1 Item D1
 GN000260
 4 PLT 108 5600.00
 400 CASE GN000261 4800.00
 4.00 PLT Initial Storage 2.000 8.00
 D2 Item D2
 2 PLT 105 200.00
 200 CASE GN000262 200.00
 2.00 PLT Initial Storage 2.000 4.00
Receipt WR - 1161 Dtd: 11.11.05
 D1 Item D1
 2 PLT 108 2800.00
 200 CASE GN000263 2400.00
 2.00 PLT Initial Storage 2.000 4.00
Misc. Dtd: 12.06.05
 20.00 CWT Blast Freezing 0.250 5.00
 1.00 OCCR Bill of Lading Charge 10.000 10.00
 3.00 HR Extra Labour Charges 35.000 105.00
 Summary Of Charges
 20.00 CWT Blast Freezing 0.250 5.00
 1.00 OCCR Bill of Lading Charge 10.000 10.00
 3.00 HR Extra Labour Charges 35.000 105.00
 8.00 PLT Initial Storage 2.000 16.00
 136.00

### Standard Bill of Lading 1 <a id="standard-bill-of-lading-1"></a>

This document supports NMFC classes, order remarks and depositor/ carrier/consignee messages. If printed in PROR (Print Shipping Documents - All) or PROM (Print Shipping Documents - Specific), it does not consolidate order lines containing the same product. If printed in COPI (Consolidated Pick), it does consolidate order lines containing the same product.
If you enter information such as the driver code, power unit number, trailer number, seal number, temperature, etc. in the Carrier Block of ENOR, the information that you enter will print on the document.
PRINT FORM NAME: d2001
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

### Standard Bill of Lading 2 <a id="standard-bill-of-lading-2"></a>

This document is an alternate version of d2001. If multiple order lines contain the same product, the lines will be consolidated at the appropriate inventory level. It includes the standard document overlay for the bill of lading.
If you enter information such as the driver code, power unit number, trailer number, seal number, temperature, etc. in the Carrier Block of ENOR, the information that you enter will print on the document.
 !!"#
$%& '&&& (	)*& '&% "+,-!"	"	" ".	%#*/*&
 0"-	1))	
234*
5 (%*%/"	14*
5
6(2.7/"	*		-##
$("$$ "*#*(&*

 08$
#%	3		9
"76/"	*		#

*

$:8;"$88"$ "*#*
;*3)/$
 08$

(%*%#%	3	
6(2.7/"	*		"76/"	*		
8(8+(8+8$";(
5(.8:(4($$<4

"$8
=##>'&0<$
>'&<$
??(8++8$$8??

## Amostras dos Documentos Core <a id="amostras-dos-documentos-core"></a>

*Manual O — Core Documents*

????????????????????

 0"$8
=##> &20<
> &<

6 0"$8
=##>60&7 <
>66&66<
&+&&"
0<%
	9*# !&!

(
	$<4@#0"$8(
=##>02&!2<$
=
>07&66<$

If you enter GROSS or gross in the Bar Code Directory field in DOCU, the gross weight will print for each line. 
If you enter NET or net in the Bar Code Directory field in DOCU, the net weight will print for each line.
The order’s load type will print on this document if the load type is a type other than NA (Not Applicable).
The standard bill of lading 2 supports the following form codes:
PRINT FORM NAME: d301n
OVERLAYS SUPPORTED: HBOL (front page only)
ADDITIONAL PRINTS SUPPORTED: Y
FORM CODE DESCRIPTION
BOLD (Bill of Lading 1,2,3) The bill of lading details will be sorted and grouped by up to four inventory levels. If two or more order lines are identical (that is, the same level 1, 2, 3 and 
4), the lines will be consolidated into a single line.
BLDR (Bill of Lading with Line 
Remarks)
Same as BOLD but with line remarks. If there are duplicate line remarks for the same inventory entity, only one line remark will print.
BLL1 (Bill of Lading Level 1) The bill of lading details will be sorted and grouped by item code.
BLL2 (Bill of Lading Level 2) The bill of lading details will be sorted and grouped by level 2 value.
BLL3 (Bill of Lading Level 3) The bill of lading details will be sorted and grouped by level 3 value.
DLT2 (Details at Level 2) The quantity and weight will print by level 2 value.
DLT3 (Details at Level 3) The quantity and weight will print by level 3 value.

 0-1792
 Carrier ABC SCAC: X
 125 Commerce Valley Drive, Markham, ON L3T 7W4 Page 1 of 1
 Customer A Consignee 1
 100 Renfrew Drive, Suite 100 25 Elm Street
 Markham Oshawa, ON L1C 4D3
 ON L3R 9R6
 Trailer #: 001
 Seal 1 : 0012345
 05.01.08
 05.02.08
 10 CASE A1 Item A1 14.17 FAK 00
 102 13.33
 15 CASE A2 Item A2 21.25 FAK 00
 101 20.00
 25 CASE A3 Item A3 35.42 FAK 00
 110 33.33
 Not Applicable
*************************************TOTALS*************************************
 50 G: 70.83 KGS
 N: 66.67 KGS
 ABC Warehousing, Inc.
 125 Commerce Valley Drive
 Suite 700
 Markham ON, L3T 7W4

### Bill of Lading by Broker Customer <a id="bill-of-lading-by-broker-customer"></a>

This document is designed for shipping broker orders. There are two parts to this bill of lading: the unconsolidated part and the consolidated part. The unconsolidated section has a separate page for each broker. The consolidated section shows the shipper code and name for each broker with no page break before each broker.
PRINT FORM NAME: d2011
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y
 Order # : 0-001180
 05:03PM
 Operator:Jack Rober
 Page 1 of 1
 BROKER CONS1
 Broker 1 Consignee 1
 100 Renfrew Drive, Suite 100 100 Renfrew Drive, Suite 100
 Markham, ON Markham, ON
 L3R 9R6 L3R 6B3
 0-001180
Order Date : 08.16.04 Shipped Date : 08.17.04
Cust. Ord. Num : Freight Term :
P.O. Number : Carrier : ABC Transport
LOT Code Description Unit Wgt.
(ITEM Code) Units SKU Pallets in_____ Pallets out_____
--------------------------------------------------------------------------------
SHIPPER : A - Customer A
========================
102 25 CASE Item A1 85.00 (Item : A1)
 1-A101 25 CASE
--------------------------------------------------------------------------------
Broker Total Units 25 CASE Broker Total 35.42 LBS
SHIPPER : B - Customer B
========================
101 10 CASE . 70.00 (Item : B1)
 1-C100 10 CASE
--------------------------------------------------------------------------------
Broker Total Units 10 CASE Broker Total 11.67 LBS
SHIPPER : D - Customer D
========================
101 15 CASE Item D1
 GN000091 (Item : D1)
 1-C100 15 CASE
 *************** ITEM MESSAGE ****************
 * Must maintain at above zero degrees Celsius *
 ***********************************************
Broker Total Units 15 CASE Broker Total 0.00 LBS
--------------------------------------------------------------------------------

### Case Pick Label <a id="case-pick-label"></a>

This label shows the customer name and address, the order number, customer order number, consignee name and address, and the pallet ID number. It is only generated in RFPIC when the automatic assignment of pallet ID’s is activated in MRFP and the picker is working in case pick mode. The case pick label prints only on a Zebra bar code printer.

### Cycle Count Tickets <a id="cycle-count-tickets"></a>

For blind counts this document will show the ticket number and location code. The customer code will also be shown unless you select .ALL as your customer. For non-blind counts, this document will show the ticket number, customer code and location code. As well, the item code and/or inventory levels and quantities will be shown depending on the options that you select when setting up your cycle count. 
PRINT FORM NAME: d2012
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
PRINT FORM NAME: DP220

### Extra Charge Audit Report <a id="extra-charge-audit-report"></a>

This document shows all outbound extra charges set up in GEXC and ECHP. You can restrict this audit report in BILB (Billing Batch) by customer code, level 1/2/3 values and charge code. As well, you can summarize the report by customer, customer/level 1, customer level 1/2, customer level 1/2/3 and customer/charge code.
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
PRINT FORM NAME: 4100
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

### FedEx Shipping Label (d2015) <a id="fedex-shipping-label-d2015"></a>

You can generate a CSV interface file containing the information required to print FedEx labels using FedEx’s label generation software. You create the file by printing the appropriate document in PROM/PROR or through auto-processing. The document for the shipping label requires the CSVH form code. The FedEx 
ABC Warehousing, Inc. /u02/app/develop/del4/work/faxlp/12061334g002b2 Page 1 of 1
Extra Charge Audit Report SECTION 1 of 1
 BATCH # : 66 - Audit # : 1 - Batch Date : 12.06.05
Print Date : 12.06.05 Batch Description : Customer A Section Page 1 of 1
------------------------------------------------------------------------------------------------------------------------------------
Accessorial Number Date Reference Number Reference Description
 Charge Code & Description Quantity Rate Total Amount
A Customer A
=========================
 44008 06-DEC-05 Order: 1473 Ord: 1473
 R3 flat rate 1.00 20.0000 20.00
 ITEM : * ** Unknown **
 44009 06-DEC-05 Order: 1473 Ord: 1473
 R3 flat rate 1473.00 20.0000 20.00
 ITEM : * ** Unknown **
 44010 06-DEC-05 Order: 1474 Ord: 1474
 R3 flat rate 1.00 20.0000 20.00
 ITEM : * ** Unknown **
 44011 06-DEC-05 Order: 1474 Ord: 1474
 R3 flat rate 1474.00 20.0000 20.00
 ITEM : * ** Unknown **
 44012 06-DEC-05 Order: 1478 Ord: 1478
 R3 flat rate 2.00 20.0000 20.00
 ITEM : * ** Unknown **
 44013 06-DEC-05 Order: 1478 Ord: 1478
 R3 flat rate 1478.00 20.0000 20.00
 ITEM : * ** Unknown **
 44014 06-DEC-05 Order: 1480 Ord: 1480
 R3 flat rate 1.00 20.0000 20.00
 ITEM : * ** Unknown **
 44015 06-DEC-05 WR: 1167 Rcp: 1167
 C1 Case Rate 25.00 0.8250 20.63
 ITEM : A1 Item A1
 LOT : 114
 ----------
 Audit Charges : 160.63
 GST : 0.00
 Total Charges : 160.63
 ==========

document “label” is for file generation purposes only; you cannot print a FedEx label within AccellosOne 3PL to a printer or view it on-screen in a PDF document.
A single FedEx label is printed for each AccellosOne 3PL order. If there are multiple order lines for a given order, the FedEx label will show the total weight and quantity for all orders lines. The quantity will be in the item’s lowest SKU.
CSV file for FedEx label

### Immediate Audit Report <a id="immediate-audit-report"></a>

This document shows all charges on the immediate invoice as well as remarks for the entire invoice plus remarks for each charge code. You can restrict this audit report in BILB (Billing Batch) by customer code, level 1/2/3 values and charge code. As well, you can summarize the report by customer, customer/level 1, customer level 1/2, customer level 1/2/3 and customer/charge code.
PRINT FORM NAME: 4000
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

### Immediate Invoice 1 <a id="immediate-invoice-1"></a>

This document shows all charges on the immediate invoice and includes the standard document overlay for this document.
PRINT FORM NAME: ba_204
OVERLAYS SUPPORTED: HIMM (front page only)
ADDITIONAL PRINTS SUPPORTED: Y

### Immediate Invoice 2 <a id="immediate-invoice-2"></a>

This document is identical to the immediate invoice (ba_204), but does not include the standard document overlay.
PRINT FORM NAME: ba_202
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

### Inbound Pallet Label <a id="inbound-pallet-label"></a>

This label shows up to four inventory levels. AccellosOne 3PL will print one label for each pallet; pallets are defined at the detail line level. The shipping label prints on an Intermec, Zebra or Datamax bar code printer.
The inbound pallet label supports the following form codes:
PRINT FORM NAME: d2007
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
FORM CODE DESCRIPTION
FMT2 200 DPI Zebra format.
FMT3 300 DPI Zebra format.
FMT4 200 DPI Zebra format for RF.
FMT5 300 DPI Zebra format with no customer code and date on the same line as the quantity.
FMT6 200 DPI Zebra format with the following parameters:
 prints inventory level 1/2/3 plus product description
 levels 1/2/3 are each bar coded
 quantity is besides level 2 bar code
 prints only one label per receipt line
FMT7 Intermec label format with the following parameters:
 first line prints receipt number and quantity with SKU
 second line prints level 1 inventory terminology (“item code”) plus description
 third line prints level 2 in bold approximately 2" high
 fourth line prints level 4 inventory terminology
 fifth line prints level 4 bar code
FMT8 Same format as FMT6 with the following differences:
 shorter bar codes, but human readable value under bar code is as large as the ITEM, LOT and PID labels
 description is restricted to 38 characters
 quantity prints on the same line as description (i.e. last line)

This document is similar to the shipping weight sheet (outbound). It shows catch weights, serial numbers and date codes for inbound product. The process values shown (catch weights only, catch weights and serial numbers only or catch weights, serial numbers and date codes) as well as which inventory level the weight sheet will group by is determined by your form code attached to the document in DOCU.
The form code for the inbound weight sheet is WS##. The first number indicates the number of Process Block values to be printed:
 1 = print catch weight only (for example, WS1#)
 2 = print catch weight and serial number (for example, WS2#)
 3 = print catch weight, serial number and date code (for example, WS3#)
The second number indicates the inventory levels to report on. For example, WS11 will print one detail line showing the quantity and weight for each unique level 1 value, while WS12 will print one detail line showing the quantity and weight for each unique level 1/2 value.
FMT9 Datamax format.
FMT10 Same as FMT9 but without the receipt number bar code. Larger bar codes for levels 3 and 4.
FMT2 200 DPI Zebra format.
FORM CODE DESCRIPTION

The load plan sheet shows the pallet position, UI or OPID value, up to four inventory levels and the number of units. AccellosOne 3PL generates pallet positions in the following sequence: LS001/LN001 (left stacked/left non-stacked), CS001/CN001 (Center stacked/center non-stacked), RS001/RN001 (right stacked/right nonstacked), LS002/LN002 (left stacked/left non-stacked), etc.
You can print the load plan sheet in either SELO or LOLD.
PRINT FORM NAME: d2019
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
OTHER REQUIREMENTS:  item process codes for catch weights and serials numbers set up in IPRO
 a process profile code set up in IPRP that is attached to the item 
 a scan parameter code set up in SCPR that is attached to the item
 if you wish print date codes, the type in 
SCPR must be set to EDT1 (AAMMDD)

### INBOUND WEIGHT SHEET <a id="inbound-weight-sheet"></a>

ABC Warehousing, Inc.
03.09.09 PAGE 1 of 1
CUSTOMER: CARRIER: Carrier ABC
 Customer A
SHIPPER: RECEIPT #: 1553
 Company A DATE: 03.09.09
 105 Commerce Valley Drive PRO #:
 Richmond Hill, ON CUST REF. #: 135172651
 L3T 7W3
--------------------------------------------------------------------------------
SUMMARY OF TAKE WEIGHT ITEMS: SUB-TOTAL
ITEM/LOT DESCRIPTION AND WEIGHTS QTY NET WT.KGS
A1 Item A1 5 58.00
 ------------------
 5 58.00
--------------------------------------------------------------------------------
RANDOM WEIGHT FOR : Item A1 / A1
 : 151
 10.00 0002 11.00 0003 12.00 0004 12.00 0001 13.00 0005
TOTAL LOT WEIGHT: 58.00
 TOTAL CASES: 5
--------------------------------------------------------------------------------

### Master Bill of Lading <a id="master-bill-of-lading"></a>

This document is a consolidated version of the standard bill of lading. It shows one line for each order. Each line shows the customer name, the consignee name and the consignee’s city, state/province and postal/zip code. Consignee messages are also shown.
This document must be printed from COPI (Consolidated Pick).
PRINT FORM NAME: DP253
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
PRINT FORM NAME: d2010
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

 Page 1 of 1
 LOAD#: 0
 Carrier ABC
 12.21.05
 Carrier ABC
 VARIOUS CONSIGNEES
 Load Contains: Freight All Kinds
 15 Customer A 20.00 21.25 C:28800.00
FAK Consignee 1 ARR : 12.23.05 00:00
 Markham, ON L3R 6B3
 25 Customer D 300.00 350.00 C:302400.00
FAK Consignee 1 ARR : 12.21.05 00:00
 Markham, ON L3R 6B3
 5 Customer A 6.67 7.08 C:9600.00
FAK Consignee 2 ARR : 12.21.05 00:00
 Calgary, AB T2J 4B4
 45 THIS IS A MASTER BILL OF LADING 326.67 378.33 C:340800.00
ABC Warehousing, Inc.
 100 Renfrew Drive
 Suite 100
 Markham, ON L3R 9R6

### MH10 and UCC-128 Labels <a id="mh10-and-ucc-128-labels"></a>

These labels fully support the industry standards for MH10 or UCC-128 labels. They print on either an 
Intermec or Zebra bar code printer.
PRINT FORM NAME: DP255
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N the check digit the twodigit prefix the type of shipping container the sevendigit member number the nine-digit serial number

### Packing Slip <a id="packing-slip"></a>

This document shows the shipper, consignee, order number and date. For each order line, the packing slip shows the ordered quantity, the shipped quantity, the item code, the gross weight and the net weight. The total number of units and the total gross and net weight print at the end of the packing slip.
There are seven possible form codes for the packing slip: PS01, PS02, PS03, PSO4, PS05, PS06 and PS07.
PRINT FORM NAME: d2016
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y
FORM CODE DESCRIPTION
PS01 For each detail line, the level 1 value only is shown. If an item being shipped has a depositor print message, the depositor print message will also be shown. This form prints the totals on a single line without any SKU code. For example, if one line has a quantity of 10 cases and a second line has a quantity of 2 pallets, the total will be 12 with no breakdown by SKU code.
PS02 For each detail line, the level 1 value only is shown. If an item being shipped has a depositor print message, the depositor print message will also be shown. This form prints the totals by SKU code. For example, if one line has a quantity of 10 cases and a second line has a quantity of 2 pallets, two totals will print: one for cases and one for pallets.
PS03 For each detail line, level 2 and 3 values are printed but no alternate description. If an item being shipped has a depositor print message, the depositor print message will also be shown.Totals are calculated by SKU codes as in 
PS02.
PS04 For each detail line, level 1 only plus the alternate description (if any) is printed and any depositor print messages are suppressed. If there are multiple order lines with the same level 1 value, they are consolidated as a single line.Totals are calculated by SKU codes as in PS02. 
PS05 PS05 is an alternate version of PS03. Unlike PSO3, PS05 does not print the system-generated weights for each order line. Instead of weights for each order line, PS05 prints a blank space for the weight to be manually entered by an operator.
No totals are printed.

### Physical Inventory Tickets <a id="physical-inventory-tickets"></a>

For blind counts this document will show the ticket number and location code. The customer code will also be shown unless you select .ALL as your customer. For non-blind counts, this document will show the ticket number, customer code and location code. As well, the item code and/or inventory levels and quantities will be shown depending on the options that you select when setting up your physical. 
PS06 PS06 is an alternate version of PS05. It prints the total quantity, total gross weight and total net weight for each order. Detail lines are the same as PS05.
PS07 PS07 is an alternate version of PS02. It supports the printing of P- type order lines. For P-type lines, the ship quantity is shown as zero and the weight is not added to the grand totals.
FORM CODE DESCRIPTION

### Pick Sheet <a id="pick-sheet"></a>

This document supports batch processing, split printing (requires location print profiles codes set up in 
LPPR), header and line remarks as well as a wide variety of messages such depositor, carrier, consignee, item hazard, item and replenishment.
If you attach the form code PBPL (Page Break by Pick Line Locations) to the document, all unallocated lines and pick line locations will print first and be separated from the other lines by a page break.
PRINT FORM NAME: DP210
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
PRINT FORM NAME: d2000
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

If you attach the form code PITE (Pick – Sort by Item) to the document, the document will print in item code sequence. If you do not specify the form code PITE for the document, the default print sequence of location code will be used.
If you attach the form code PI3D (Print Invt. Level 3 Description) to the document, the level 3 inventory description and the gross weight for each pick will print.
If you enter “SUMMARY” in the Bar Code Directory field in DOCU, only the summary section of the pick document will print. If you leave this field blank, the full version — both detail and summary — will print.
1BHFPG
1*$,4)&&5
0SEFS/VNCFS$PNQBOZ"#$8BSFIPVTJOH*OD
$"33*&3$BSSJFS"#$
1PXFS6OJU
5PCFTIJQQFEPO$BSSZ6OJU
$VTU0SEFS/VNCFS4FBM
10/VNCFS4FBM
$6450.&3%$0/4*(/&&$0/4
$VTUPNFS%$POTJHOFF
3FOGSFX%SJWF&MN4USFFU
.BSLIBN0/0TIBXB0/
-3#-$%
 -*/&*5&.*5&.%&4$3*15*0/25:4,6
-058)4&-0$"5*0/
1*%
 %*UFN%$"4& "$"4& (/5JF5JFS1-5$"4&  %*UFN%$"4& "$"4& (/5JF5JFS1-5$"4&
*5&..&44"(&
.VTUNBJOUBJOBUBCPWF[FSPEFHSFFT$FMTJVT
 %*UFN%$"4& "$"4& (/5JF5JFS1-5$"4&  1*$,505"-4
5PUBM4,6hT$"4&5PUBM8FJHIU	(SPTT
-#4
5PUBM8FJHIU	/FU
-#4
5PUBM$VCF*/
 03%&3*5&.505"-4
 *5&.$0%&*5&.%&4$3*15*0/6/*546/*54 03%&3&%4)*11&%  %*UFN%
%*UFN%
%*UFN%  5PUBM  5PUBM8FJHIU	(SPTT
-#4
5PUBM8FJHIU	/FU
-#4
5PUBM$VCF*/

DOCU screen for PICK document

### Cold Storage Pick Sheet <a id="cold-storage-pick-sheet"></a>

This pick document is similar to the regular pick sheet (d2000). If you attach the form code PITE (Print in Item 
Sequence) to this document, pick records will print in item code sequence rather than location code sequence.
For each order line, the cold storage pick sheet prints a box for manual entry of miscellaneous date. At the bottom of the pick sheet is printed a check list of items to be checked: Stretch Wrap Y/N, Label/Sticker Cases 
Y/N, etc.
PRINT FORM NAME: d2000cs
OVERLAYS SUPPORTED: N/A

ADDITIONAL PRINTS SUPPORTED: Y

 PICK SHEET Page 1 of 1
Order#: 0-2061 Company: ABC Warehousing, Inc.
To Be Shipped On: 06.05.09 CARRIER: Carrier ABC
Customer Order #: Carrier Unit #:
 P.O. Number: Seal 1:
 Seal 2:
 TRAILER INSPECTION:
 Temp Setting _______ Clean Y/N
 Good Condition Y/N Pre-Cooled Y/N
CUSTOMER: A CONSIGNEE: CONS1
Customer A Consignee 1
100 Renfrew Drive, Suite 100 25 Elm Street
Markham ON L3R 9R6 Oshawa ON L1C 4D3
LINE ITEM ITEM DESCRIPTION QTY SKU
 LOT LOT DESCRIPTION WHSE-LOCATION NET WGT. GROSS WGT.
================================================================================
 1 A1 Item A1 15 CASE CW
 1-A106 ==> 15 CASE
 Tie/Tier = 10/10 => PLT 100 / CASE 1
 ** ITEM MESSAGE **
 * Item message *
 ********************
----------------
| |
----------------
--------------------------------------------------------------------------------
 2 A2 Item A2 5 CASE CO
 1-S100 ==> 5 CASE
 Tie/Tier = 10/10 => PLT 100 / CASE 1
----------------
| |
----------------
--------------------------------------------------------------------------------
--------------------------------------------------------------------------------
PICK TOTALS Total Weight: (Gross) 16.70 KGS
Total Units: 20 Total Weight: (Net) 16.00 KGS
 Total Cube: 22809.60 IN
Stretch Wrap Y/N Stamping dates Y/N Restock(Cancelled) Y/N
Catch Weights Y/N Exporting Y/N Additional Labor Hrs. ____
Picking Cases Y/N Weight Conversions Y/N Other ___________________
Cut Straps/Boxes Y/N Dividers Worked In/Out Y/N PRODUCT TEMPERATURE
Label/Sticker Cases Y/N Floor Load Y/N Front ________
Revised Order Y/N Slip Sheeting Y/N Middle ________
 Tail ________
 Staged By _______
 PALLETS/DIVIDERS In Out Loaded By _______
Comments: __________________ Pallets Wood ______ ______ Approved By: _______
____________________________ Pallets Chep ______ ______
____________________________ Dividers Wood ______ ______ Arrival Time _______
____________________________ Dividers Plastic______ ______ Start Time _______
____________________________ Other _________ ______ ______ Finish Time _______

### Receipt Invoice 1 <a id="receipt-invoice-1"></a>

This document supports surcharges and accessorial charges and shows up to three inventory levels. It includes the standard document overlay for the receipt invoice.
If you need to see quantity specific details because you charge by quantity, create a document in DOCU ending in CS (for example, WRCS). Any document code not ending in CS will report quantity by weight (for customers who charge by weight).
PRINT FORM NAME: d303an
OVERLAYS SUPPORTED: HRIN (front page only)
ADDITIONAL PRINTS SUPPORTED: Y

### Receipt Invoice 2 <a id="receipt-invoice-2"></a>

This document shows up to four inventory levels, but does not include the standard document overlay for this document.
PRINT FORM NAME: d2003

### Receipt Notice 1 <a id="receipt-notice-1"></a>

This document shows up to three inventory levels as well as header remarks. It includes the standard document overlay for this document.
If you set the form code in DOCU to RCL3, the receipt notice details will be sorted and grouped by up to three inventory levels. If two or more order lines are identical (that is, the same level 1, 2 and 3), the lines will be consolidated into a single line.
If you set the form code in DOCU to RCL2, the receipt notice details will be sorted and grouped by up to two inventory levels. If two or more order lines are identical (that is, the same level 1 and 2), the lines will be consolidated into a single line.
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

PRINT FORM NAME: d303n
OVERLAYS SUPPORTED: HRNO (front page), TRMS (back page)
ADDITIONAL PRINTS SUPPORTED: Y

### Receipt Notice 2 <a id="receipt-notice-2"></a>

This document shows up to four inventory levels, but does not include the standard document overlay.
PRINT FORM NAME: d2004
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

### Receiving Label <a id="receiving-label"></a>

This label shows up to four inventory levels. AccellosOne 3PL will print one label for each pallet; pallets are defined at the detail line level. The receiving label prints on either an Intermec or Zebra bar code printer.

### Renewal Audit Report — Details <a id="renewal-audit-report-details"></a>

This document shows one line for each billing entity being renewed. You can restrict this audit report in BILB (Billing Batch) by customer code, level 1/2/3 values and charge code. As well, you can summarize the report by customer, customer/level 1, customer level 1/2, customer level 1/2/3 and customer/charge code.
PRINT FORM NAME: d2007
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
PRINT FORM NAME: 4001
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

### Renewal Audit Report — Single Line <a id="renewal-audit-report-single-line"></a>

This document shows one line for each customer giving the number of billing entities renewed as well as the total charges for each customer.
PRINT FORM NAME: _402
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
ABC Warehousing, Inc. /u02/app/develop/del4/work/faxlp/01091413300bb1 Page 1 of 3
Renewal Audit Report SECTION 1 of 2
 BATCH # : 69 - Audit # : 1 - Batch Date : 12.07.05
Print Date : 01.09.06 Batch Description : Customer D Section Page 1 of 2
------------------------------------------------------------------------------------------------------------------------------------
Customer Code & Name Number of Lots Renewed Total Charges Num. of Min. Charges Num. of Max. Charges
D Customer D 2 275.00 0 0
 D1 11.28.05 12.28.05
 3PLT
 1905.12 KGS 2100.000000 C1 0.5500 165.00
 D2 12.01.05 01.01.06
 2PLT
 200.00 KGS 128.000000 C1 0.5500 110.00
 Surcharge 0.00
ABC Warehousing, Inc. /u02/app/develop/del4/work/faxlp/01091427n0166f Page 3 of 3
Renewal Audit Report SECTION 2 of 2
 BATCH # : 69 - Audit # : 2 - Batch Date : 12.07.05
Print Date : 01.09.06 Batch Description : Customer D Section Page 1 of 1
------------------------------------------------------------------------------------------------------------------------------------
Customer Code & Name Number of Lots Renewed Total Charges Num. of Min. Charges Num. of Max. Charges
D Customer D 2 275.00 0 0
 ------ --------- ------ ------
Totals 2 275.00 0 0
 ====== ========= ====== ======
End of Section # 2
END OF REPORT. 

### Renewal Invoice 1 <a id="renewal-invoice-1"></a>

This document shows up to four inventory levels and includes the standard document overlay for the renewal invoice. 
There are three possible summary options for this invoice: print summary after invoice details (default), print summary on new page and print summary only (that is, no invoice details). You define the summary on new page and summary only options in DEAS by attaching the appropriate code (SUMMARY-ON-NEW-PAGE or 
SUMMARY-ONLY) to the DEAS code “ACIN”. Then you attach your DEAS code to the appropriate customers in CUST.
If you do not set up summary options in DEAS, the summary default — print summary immediately following invoice details without a page break — will be used.
DEAS screen showing ACIN code with summary on new page option
PRINT FORM NAME: ba_203
OVERLAYS SUPPORTED: HUAL (front page only)
ADDITIONAL PRINTS SUPPORTED: Y

### Renewal Invoice 2 <a id="renewal-invoice-2"></a>

This document shows charge codes only with no inventory information. It does not include the standard document overlay for the renewal invoice.
PRINT FORM NAME: ba_200
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

### Shipping Label <a id="shipping-label"></a>

This label shows up to four inventory levels. AccellosOne 3PL will print one label for each pallet; pallets are defined at the detail line level. The shipping label prints on either an Intermec or Zebra bar code printer.
PRINT FORM NAME: d2006
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N

### Shipping Weight Sheet <a id="shipping-weight-sheet"></a>

This document shows catch weights for outbound shipping. In the summary section of the weight sheet, the total weight for each inventory entity is shown. In the detail section of the weight sheet, the individual weights for each piece/pallet/case are shown.
You can configure this document to group by any inventory level. For example, suppose you have a threelevel account consisting of item/lot/pallet ID. If you group by level 1, the document will show the catch weights for each item. If you group by level 2, the document will show the catch weights for each lot. If you group by level 3, the document will show the catch weights for each pallet ID.
You define your group by value by creating a form code in FORM. The last character of your form code should be a number indicating the inventory level that you wish to group by. For example, a form code of “L1” would group by level 1, a form code of “L2” would group by level 2, etc. You then attach the appropriate form code to your shipping weight sheet document in DOCU.
The line details of the shipping weight sheet will print in two easy-to-read columns if you attach one of the following form codes to your weight sheet document:
 if you track pallet ID’s at level 3, use the form code PID3
 if you track pallet ID’s at level 4, use the form code PID4
PRINT FORM NAME: d2009

### Tally <a id="tally"></a>

This document shows up to four inventory levels and includes remarks as well as depositor, item hazard and item messages.
If the product is allocated, the tally will show one line for each location line on the receipt. If the product is not allocated, the tally will show one blank line for each unit of the lowest SKU on the receipt.
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: N
OTHER REQUIREMENTS:  an item process code for catch weights set up in IPRO
 a process profile code set up in IPRP that is attached to the item 
 a scan parameter code set up in SCPR that is attached to the item
 WEIGHT SHEET
ABC Warehousing
08.13.04 PAGE 1 of 1
SHIPPER: CARRIER: ABC Transport
 Customer D RUN :
CONSIGNEE: ORDER #: 1179
 Consignee 1 DATE: 08.16.04
 100 Renfrew Drive, Suite 100 PO #:
 Markham, ON CUST ORD. #:
 L3R 6B3
SUMMARY OF TAKE WEIGHT ITEMS: SUB-TOTAL
ITEM/LOT DESCRIPTION AND WEIGHTS QTY NET WT.KGS
D1 Item D1 5 53.83
D2 Item D2 10 1181.56
 ------------------
 15 1235.39
--------------------------------------------------------------------------------
RANDOM WEIGHT FOR LOT: 101 Item D1
 10.45 11.43 12.50 9.45 10.00
TOTAL LOT WEIGHT: 53.83
 TOTAL CASES: 5
--------------------------------------------------------------------------------
RANDOM WEIGHT FOR LOT: 104 Item D2
 12.45 10.34 10.40 11.45 12.67 ???.?? 12.00 12.54 11.66 10.05
TOTAL LOT WEIGHT: 1181.56
 TOTAL CASES: 10
--------------------------------------------------------------------------------

If you use the form code BLTL (Blind Tally), the tally will show one blank line for each unit of the lowest SKU on the receipt. No quantity or location information will be shown and no totals will be calculated. Allocation should be switched off for the flow at which you print the blind tally.
You can print one blank line for each of the highest SKU received versus one blank line for each of the lowest 
SKU received. This option requires setup in both DEAS and CUST. In DEAS create an alternate reporting type code that matches the document code for your tally document; for example, TALY. In the Detail record of 
DEAS create a detail record called HIGH. Then attach your new DEAS code to the appropriate customer(s) in 
CUST.
PRINT FORM NAME: d2002
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

5"--:
1BHFPG
$BSSJFS"#$5SBOTQPSU1653&$&*153
$VTUPNFS%4IJQQFS4".&
$VTUPNFS%4BNF
3FOGSFX%SJWF
.BSLIBN0/-3#.BSLIBN0/-3#
3FDFJQU%BUF3FGFSFODF/VNCFS
5SBJMFS1SPCJMM/VNCFS
-*/&*5&.*5&.%FTDSJQUJPO6OJUT4,6
/FU(SPTT8FJHIU2UZ#SFBLEPXO
-05
1*%
8ITF-PDBUJPO-PDBUJPO2UZ
3FDFJQU3FNBSLT3VTISFDFJQU
%*UFN%$"4&
/(-#41-5$"4& "$"4& "$"4&
*5&..&44"(&
.VTUNBJOUBJOBUBCPWF[FSPEFHSFFT$FMTJVT
 %*UFN%$"4&
/(-#41-5$"4& "$"4&
 5PUBM6OJUT
/FU-#4 (SPTT-#4
&OUFSFE#Z-03/&(PPE1BMMFUT@@@@@@@@@@
6OMPBEFE#Z@@@@@@@@@@@@@@@@@@@1PPS1BMMFUT@@@@@@@@@@
1VU"XBZ#Z@@@@@@@@@@@@@@@@@@@5PUBM1BMMFUT@@@@@@@@@@
1BMMFUT&YDIBOHFE@@@@@@ &/%0'1653&$&*15

### Cold Storage Tally <a id="cold-storage-tally"></a>

This tally is similar to d2002. If you attach the form code BLTL (Blind Tally) to this document, a set of empty boxes will print after each line so that operators can enter manual counts and inventory information. The number of sets of empty boxes printed depends on the number of pallets (or cases, if cases are the highest 
SKU) on the receipt line.
If you attach the process code OREN to the document, the following line will print at the end of the document: 
“Org. Est. # __________________”
PRINT FORM NAME: d2002cs
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

### VICS Bill of Lading <a id="vics-bill-of-lading"></a>

The VICS bill of lading is a standardized BOL that a consortium of shippers and carriers developed to meet the express needs of all parties. It was created to ensure that shippers, carriers and consignees receive the information that they need to process goods through the supply chain.
The VICS bill of lading is restricted to orders belonging to the same customer.
In addition to the normal setup in DOCU, the VICS bill of lading requires a unique EAN UCC prefix number attached to each customer in CUST.
PRINT FORM NAME: DP252
OVERLAYS SUPPORTED: N/A
ADDITIONAL PRINTS SUPPORTED: Y

DATE: STRAIGHT FORM BILL OF LADING PAGE: 1 OF 3
SHIP FROM
SHIP TO
FREIGHT CHARGES BILL TO
Bill Of Lading Number:
Name :
Address :
City/State/Zip:
Name :
Address :
City/State/Zip:
Name :
Address :
Address :
City/State/Zip:
CARRIER NAME:
Trailer Number:
Seal Number(s):
SCAC:
Pro Number:
BOL#:
PO# :
CUSTOMER ORDER INFORMATION
SID#: FOB:
CID#: FOB:
Freight Charge Terms: (freight charges are prepaid unless marked otherwise)
Prepaid _________ Collect ________ 3rd Party ________ P/A ______
Master Bill Of Lading: with attached (check box) underlying Bills Of Lading
SPECIAL INSTRUCTIONS:
SHIP FROM
SHIP TO
FREIGHT CHARGES BILL TO
CUSTOMER ORDER INFORMATION
CARRIER INFORMATION
Commodities requiring special or additional care or attention in handling or slowing must be so marked and packaged as to ensure safe transportation with ordinary care.
CUSTOMER ORDER NUMBER
GRAND TOTAL
#PKGS WEIGHT PALLET/SLIP ADDITIONAL SHIPPER INFO (CIRCLE ONE)
Y N
HANDLING
UNIT PACKAGE COMMODITY DESCRIPTION LTL ONLY
QTY TYPE QTY TYPE WEIGHT H.M.
(X) NMFC# CLASS
GRAND TOTAL
NOTE Liability Limitation for loss of damage in this shipment may be applicable. See 49 U.S.C. 14706(c)(1)(A) and (B)
COD AMOUNT: $
Fee Terms: Collect: Prepaid:
Customer check acceptable:
Where the rate is dependent on value, shippers are required to state specifically in writing the agreed or declared value of the property as follows:
The agreed or declared value of the property is specifically stated by the shipper to be not exceeding
_______________________ per _____________________
RECEIVED, subject to individually determined rates or contracts that have been agreed upon in writing between the carrier and shipper, if applicable, otherwise to the rates, classifications and rules that have been established by the carrier and are available to the shipper, on request. The shipper hereby certifies that he/she is familiar with all the terms and conditions of the NMFC
UNIFORM Straight Bill of Lading, including those on the back thereof, and the said terms and conditions are hereby agreed to by the shipper and accepted for him/herself and his/her assigns.
The carrier shall not make delivery of this shipment without payment of freight and all other lawful charges.
Shipper
Signature
SHIPPER SIGNATURE / DATE CARRIER SIGNATURE / PICKUP DATE Trailer Loaded: Freight Counted: This is to certify the above named materials are properly classified, packaged, marked and labeled, and are in proper condition for transportation according to the applicable regulations of the DOT.
All cargo tendered for transport is subject to inspection. By tendering cargo to carrier, shipper grants consent to such an inspection.
Carrier acknowledges receipt of packages and required placards. Carrier certifies emergency response information was made available and/or carrier has the DOT emergency response guidebook or equivalent documentation in the vehicle By Shipper By Shipper
By Driver By Driver/pallets said to contain
By Driver/pieces
Need Certificate of Analysis
RF Directed 3L Seq Reserve Log
125 Commerce Valley
New RFCH/RFPIC
Youngstown, OH, 44514
Consignee Code 3
Test this for SR
Address Line 2
Youngstown, OH, 44517
11001100000001845
Aldan Transportation
ALDA
04.21.09
See Supplement Page for Details
See Supplement Page for Details
1194 29500.36

### SSRS Documents <a id="ssrs-documents"></a>

The following SSRS documents are supported:
DOCUMENT 
CODE DESCRIPTION REPORT/DOCUMENT NAME
SRTC SRCT — SSRS Receiving Invoice WarehouseReceiptReport_401_MR
STAL STAL — SSRS Receiving Tally ReceiptTallyReport_401_MR
SPIC SPIC — SSRS Pick Ticket PickSheetReport_401_MR
SPAK SPAK — SSRS Packing Slip PackingSlipReport_401_MR
SBOL SBOL — SSRS Bill of Lading StraightBOLReport_401_MR

## Maintaining Your Documents <a id="maintaining-your-documents"></a>

*Manual O — Core Documents*

### Setting Up Your Form Codes in FORM <a id="setting-up-your-form-codes-in-form"></a>

In this program, you set up your form codes. Form codes are attached to documents and reports, and determine the number of lines printed before a page break and the page’s orientation. You attach a form code to a document in the program DOCU (Documents). You attach a form code to a native report in the program 
JOSE (Job Selection Code).
The following form codes are preloaded into FORM and perform a custom function when attached to a particular document: BLDR, BLL1, BLL2, BLL3, BLTL, BOLD, PBPL, PID3, PID4, RCL2 and RCL3. Refer to the appropriate document for further information on these codes.
1 Enter FORM.
2 Click on Enter Criteria then Execute Query to see which forms have already been set up.
FIELD DESCRIPTIONS
Form Code Mandatory
Your form code.
Description Mandatory
This description for your form code.
Horizontal Lines Only available when printing in PDF format using the VIEW printer
The number of horizontal lines for the form. The default number of lines for a portrait form is 66 and for a landscape form 51. AccellosOne 3PL will automatically insert a page break after the number of lines that you specify.
Orientation Only available for native reports
Portrait
Landscape
The form’s orientation.

Form Code (FORM)
3 If you need to create a new form, click on Create Record.
4 Key in your form code and press Enter.
5 Key in a description for your new code and press Enter.
6 Key in the number of lines for your form and press Enter.
7 Select the orientation (portrait or landscape) from the dropdown list.
8 Press the tab key.
9 When you finish setting up your form, click on Return to Main and Exit to exit the program.

### Setting Up Your Document Types in DOTP <a id="setting-up-your-document-types-in-dotp"></a>

In this program, you set up your document types. Document types are attached to documents in DOCU and perform two functions in AccellosOne 3PL:
 they describe a document’s type — that is, whether it is an inbound, outbound, billing, etc. document
 they specify the number of additional copies that will be automatically printed each time that you print a specific document 
DOTP contains all the document types required to print a single copy of any AccellosOne 3PL document. If you wish to print multiple copies of a document without requeuing it in RERE or RERO, you will have to set up a document type in DOTP.
You define multiple prints for a document type by creating a code starting with a number. The number that you specify defines the number of additional copies that will be printed. For example, the code 1PRN will print one additional copy, the code 2PRN will print two additional copies, the code 3PRN will print three additional copies.

EXAMPLE 1
If you wish two extra copies of every inbound and outbound document, create two codes in DOTP: one with a type of 2IN (for Inbound) and one with a type of 2OU for Outbound. Attach the inbound code to your inbound documents and the outbound code to your outbound documents.
EXAMPLE 2
If you wish one extra copy of every renewal invoice, create one code in DOTP with a type of 1BI (for Billing). 
Attach this code to your renewal invoice and attach the standard DOTP code for billing to all other invoices.
Additional prints are not available for the FAX, AFAX, MAIL or VIEW printers. Refer to [LISTING OF CORE 
DOCUMENTS](documentos-impressao.html#listing-of-core-documents) to see which documents support additional prints.
1 Enter DOTP.
2 Click on Enter Criteria then Execute Query to see which document types have already been set up.
FIELD DESCRIPTIONS
Document Type Code Mandatory
Your document type code. The leading numbers in this code indicate the number of additional copies that will print. You can print up to a maximum of 99 additional copies.
If your codes begins with a non-number (for example, LA for Label or BOL2 for 
Bill of Lading), AccellosOne 3PL will print a single copy of the document.
Description Mandatory
The description of your document type code.
Type AD (Adjustment Audit)
IN (Inbound)
OU (Outbound)
BI (Billing)
PH (Physical)
LA (Label)
The type of document.

Document Types (DOTP)
3 If the document type that you need is not set up, click on Create Record.
4 Key in your document type code and press Enter.
5 Key in a new description for your new code and press Enter.
6 Key in your type (AD, IN, OU, BI, PH, LA or AD) and press Enter.
7 Click on Return to Main to exit create mode.
8 Click on Exit to exit.

### Maintaining Your Documents in DOCU <a id="maintaining-your-documents-in-docu"></a>

Documents are set up by your HighJump consultant. You should not attempt to create new documents yourself; however, you may wish to change some of the print options of an existing document. 
FIELD DESCRIPTIONS
Document Code Mandatory
Set up by HighJump.

Description Mandatory
Set up by HighJump.
Document Type Code Mandatory
Set up by HighJump.
Form Code (FORM) Mandatory
The document’s form code.
Allow Reprint N = No
Y = Yes
If you specify No, you can neither reprint the document nor requeue it in 
REOR or RERE. If you specify Yes, you can reprint and requeue the document as often as required. 
Flag Reprint Only available if the Allow Reprint field is set to Yes
N = No
Y = Yes
If you specify No, the document will reprint without a reprint message (for example, “duplicate”). If you specify Yes, the message that you enter in the 
Reprint Message field will appear on the reprinted document.
Reprint Message Only available if the Flag Reprint field is set to Yes
The message to appear on reprinted documents. 
Print Multiple Entry DocumentsReserved for future use.
FIELD DESCRIPTIONS

Reprint All Order Lines/
New Lines Only
Only available for certain outbound documents
A = All
N = New Lines Only
If you set this field to A for All, all order lines will print each time that you reprint an outbound document in REOR. If you set this field to N for New Lines 
Only, you will be prompted to print all lines or new lines only when you reprint an outbound document in REOR (Requeue Order Documents). A new line is any order line added after the previous printing of the document.
If you wish to use the New Lines Only parameter, you must specify this option before printing the document for the first time for any given batch of orders. 
Update Print Status Reserved for future use
Process Code (IPRO) Optional
If you enter a process code in this field, you can print process codes on labels in RELA (Reprint Labels). RELA requires a custom document from HighJump.
Print Form Source Type Mandatory 
Set up by HighJump 
Print Form Name Mandatory 
Set up by HighJump 
Report Name Only required for Oracle and SSRS reports
The name of the Oracle or SSRS report. See [Working With Oracle Reports](documentos-impressao.html#working-with-oracle-reports) for further information on setting up Oracle Reports.
Printer Code (PRIN) Optional
The default printer for this document.
FIELD DESCRIPTIONS

Document Directory Only available for certain audit reports and EDI processes
This field allows you to specify a destination directory for the output file of certain audit reports and EDI processes. Assigning different directories to different reports and EDI processes makes it easier to identify and retrieve these reports and processes.
If you do not specify a destination directory, the output file for the report or EDI process will be stored in the default directory — $DEL4_HOME/usr1/del4/ work/faxlp.
Document File Prefix Only available for certain audit reports and EDI processes
This field allows you to specify a prefix for the report or process’s output file. 
For identification purposes only.
Document File Suffix Only available for certain audit reports and EDI processes
This field allows you to specify a suffix for the report or process’s output file. 
For identification purposes only.
Overlay for Front Pages (FXOL)
Optional
The overlay code used as a template or background for the front pages of the document.
Overlay for Back Pages (FXOL)
Optional
The overlay code used as a template or background for the back pages of the document.
FIELD DESCRIPTIONS

Print Restrictions for 
Load Documents
Only available for the load documents printed in SELO
0 = No restrictions
1 = Load status = “Ready to load”
2 = Load status = “Complete”
3 = Load status = “Complete” and pallet positions captured
The conditions that must be met before loads can be printed in SELO (Set Up 
Load).
Bar Code Directory Set up by HighJump for the MH10 label
The directory in which the bar code file is stored. Also used by the Standard 
Bill of Lading 2 to specify the gross or net weight.
Bar Code File Set up by HighJump for the MH10 label
The name of the bar code file.
Document ID Reserved for future use
Suppress Display in eVista for Client AccountsN = No
Y = Yes
If you set this field to N for No, suppression of display will be deactivated and e-Vista client account users will be able to view the document in e-Vista when it is attached to an inbound or outbound flow. If you set this field to Y for Yes, e-Vista client account users will not be able to view the document in e-Vista.
Signature Capture ActivatedN = No
Y = Yes
If you set this field to N for No, signature capture is deactivated for the document. If you set this field to Y for Yes, signature capture is activated for the document.
See “Signature Capture” in the Guide to ActiveDesktop/AccellosOne 3PL/.
APM / BarTender Label 1/
See [Attaching Your BarTender Label to AccellosOne 3PL](documentos-impressao.html#attaching-your-bartender-label-to-accellosone-3pl) for further information.
BarTender Separator 
Label
See [Attaching Your BarTender Label to AccellosOne 3PL](documentos-impressao.html#attaching-your-bartender-label-to-accellosone-3pl) for further information.
FIELD DESCRIPTIONS

1 Enter DOCU.
2 Click on Enter Criteria then Execute Query to see which documents have already been set up.
Sort Sequence for BarTender LabelsSee [Attaching Your BarTender Label to AccellosOne 3PL](documentos-impressao.html#attaching-your-bartender-label-to-accellosone-3pl) for further information.
Print Company or Warehouse Address
Only available if you invoice by warehouse
C = Company
W = Warehouse
If you set this field to C for Company, the company’s address will print on the invoice. If you set this field to W for Warehouse, the warehouse address will print on the invoice.
SKU Class for Number of 
Labels
See See [Attaching Your BarTender Label to AccellosOne 3PL](documentos-impressao.html#attaching-your-bartender-label-to-accellosone-3pl) for further information.
Rounding Method for 
Number of Labels
See See [Attaching Your BarTender Label to AccellosOne 3PL](documentos-impressao.html#attaching-your-bartender-label-to-accellosone-3pl) for further information.
Print Document Without 
Assigning Locations
N = No
Y = Yes
If you set this field to Y for Yes, you can print a given document without triggering allocation even though the document is attached to a flow in which allocation is activated.If you set this field to N for No, printing a given document will always trigger allocation.
This flag is useful when more than one document is attached to a flow and not all documents should trigger allocation.
Document printing with allocation switched off must be activated in COMP (Company Parameters).
FIELD DESCRIPTIONS

Documents screen for a receiving tally
3 If the document that you require has not been set up, click on Create Record.
4 Key in your document code (up to four alphanumeric characters) and press Enter.
5 Key in a meaningful description for the new code and press Enter.
6 In the Document Type field, use your pick list to select the appropriate document type. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
7 In the Form Code field, use your pick list to select the appropriate form code.
8 In the Allow Reprint field, key in N for No or Y for Yes and press Enter.
9 If you specified Yes in the previous field, key in N for No or Y for Yes to specify your Flag Reprint value and press Enter. If you select Yes, you must enter a reprint message.
10 Press Enter to bypass the Print Multiple Entry Documents field.
11 If you are setting up an outbound document, key in A for All or N for New Lines Only in the Reprint All 
Order Lines/New Lines Only field and press Enter.
12 In the Update Print Status field, key in A for Always and press Enter.
13 If required, key in a process code and press Enter.
14 Key in your print form source type and print form name and press Enter.
15 If required, key in your printer code and press Enter.
16 If required, key in a document directory, document prefix and document suffix.
17 Press Enter twice to bypass the Overlay fields.

18 Press Enter the required number of times to bypass the Bar Code Directory, Bar Code File and Document ID fields.
19 In the Signature Capture Activated field, key in N for No or Y for Yes and press Ente.r
20 Press Enter the required number of times to bypass the BarTender Label fields.
21 In the Print Company or Warehouse Address field, key in C for Company or W for Warehouse and press 
Enter.
22 Press Enter to bypass the SKU Class for Number of Labels field.
23 In the Print Document Without Assigning Locations field, key in Y for Yes or N for No and press Enter.
24 Click on Return to Main and Exit to exit.

### WAREHOUSE PRINTER BLOCK <a id="warehouse-printer-block"></a>

The Warehouse Printer Block allows you to define a default printer for each warehouse. This printer will override the default printer for the document set up in the Header Block of DOCU.
1 Retrieve the document that you wish to set up.
2 Click on Warehouse Printer Block.
3 Key in your warehouse code and press Enter or select your warehouse code from the pick list.
4 Key in the associated printer code and press Enter or select your printer code from the pick list.
5 Repeat the above steps for each additional warehouse code/printer code combination that you wish to set up.
6 When you finish setting up your warehouse printer combinations, click on Save.
Warehouse Printer Block for TALY document showing default printers for each warehouse
7 Click on Exit to exit the Warehouse Printer Block.
8 Click on Exit to exit.

### PRINTER/OPERATOR BLOCK <a id="printer-operator-block"></a>

The Printer/Operator Block allows you to define a default printer for an operator when the operator is printing a specific document. For example, if you define P1 as the default printer for operator A whenever operator A is printing a pick sheet, P1 will automatically appear as the printer code whenever operator A prints the document. Operator A can accept the default printer or manually select an alternate printer.
1 Retrieve the document that you wish to set up.

2 Click on Detail Block.
3 If you already have printer/operator records set up, click on Create Record. 
4 Key in your printer code and press Enter or use the pick list function to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
5 Key in your operator code and press Enter or use the pick list function to select it. You can define a default printer for all operators by keying in .ALL as your operator code. 
6 Press Enter again to position your cursor in the next line. 
7 Repeat the above three steps for each additional printer/operator combination that you wish to define for the document. 
Printer/Operator Block showing WHS1 as the default printer for operator BOB when printing a receiving tally
8 When you finish defining your printer/operator combinations, click on Return to Main and Master Block to return to the Master Block. Then click on Exit to exit. 

### Changing Your Default Printer in ADOP <a id="changing-your-default-printer-in-adop"></a>

In this program, you can change your default printer for auto-printed documents in the event that a printer is down for maintenance. The Header or Operator Block shows each operator and his or her default printer code. The Detail or Document Type Block shows the overrides (if any) of the operator/printer records in the 
Header Block. That is, for this particular document type, use this printer for any document assigned this document type rather than the default printer in the Header Block.
Access to ADOP is as follows:
 system administrators can query, create and update any record regardless of operator
 non-system administrators can query, create and update their own records only
1 Enter ADOP.
2 Do one of the following:
ADOP screen
3 Click in the Document Type field.
4 Key in your document type and press Enter or select your document type from the pick list and press 
Enter.
If you are a system administrator:
If you are not a system administrator:
a) Click on Enter Criteria.
b) Key in the operator code that you wish to query on and click on 
Execute Query.
a) Click on Enter Criteria then 
Execute Query to retrieve your own operator code.

5 In the Printer field, key in your override printer code and press Enter or select your override printer code from the pick list and press Enter.
6 Click on Save to save your changes.
7 Click on Exit to exit.

### REMOVING AN OVERRIDE PRINTER <a id="removing-an-override-printer"></a>

1 Enter ADOP.
2 Do one of the following:
3 Click in the Document Type field of the override printer that you wish to delete.
4 Click on Delete.
5 When prompted to confirm the deletion, click on Yes.
6 Click on Exit to exit.

### Maintaining Your Batch Types in BATP <a id="maintaining-your-batch-types-in-batp"></a>

In this program, you maintain your batch type codes. Batch type codes are required before you can create a batch in BILB. Batch type codes are set up by HighJump and should not be changed or deleted unless you are instructed to do so by a HighJump consultant.
In the Document Block of BATP are all the valid documents for the batch type. The majority of batch types contain at least two documents: one for the invoice and one for the audit report.
If you are a system administrator:
If you are not a system administrator:
a) Click on Enter Criteria.
b) Key in the operator code that you wish to query on and click on 
Execute Query.
a) Click on Enter Criteria then 
Execute Query to retrieve your own operator code.
FIELD DESCRIPTIONS
Batch Type Code ACCE = Accessorial Invoice
DLRE = Daily Invoice Register
EXCH = Extra Charge Rater
IINV = Immediate Invoice
RENW = Renewal Invoice
Your batch type code.

1 Enter BATP.
2 Click on Enter Criteria then Execute Query to retrieve your batch type codes. When the first code is displayed, use your down arrow key to see which batch type codes have already been set up.
Description The description of your batch type code.
Current Number The number that will be assigned to the next batch.
Generate/Create Reserved for future use
Allow Re-Audit Reserved for future use
Control Total Reserved for future use
Enforce Balance Reserved for future use
DOCUMENT BLOCK
Customer Code Set to .ALL.
Document Code (defined in DOCU)
The C program or document code for the batch type code. The majority of batch types contain at least two records: one for the invoice and one for the audit report.
If there are more than two records for a particular batch type (for example, two audit reports and one invoice), the report will be divided into two sections. 
Section 1 will contain the first audit report and section 2 will contain the second audit report.
Audit A = Audit
C = Acceptance
Whether the C program or document code generates an audit batch (A for 
Audit) or an invoice (C for Acceptance).
FIELD DESCRIPTIONS

Batch Type Code ACCE showing one invoice and one audit report
3 When you finish viewing your batch type codes, click on Exit to exit.

### Working With Overlays <a id="working-with-overlays"></a>

Document overlays allow you to produce professional looking documents containing company logos, legal terms and conditions or any other information that might appear on a pre-printed form. You can define up to two overlays for each document: one overlay for the front side of each page and a second overlay for the backside of each page. You define document overlays in FXOL and then attach them to the appropriate document in DOCU.
There are seven standard overlays included in AccellosOne 3PL: 
CODE APPLIES TO NOTES SPECIAL REQUIREMENTS
HBOL Bill of Lading (d301n) No back page overlay N/A
HRIN Receipt Invoice (d303an) No back page overlay required N/A
HRNO Receipt Notice (d303) Front page overlay N/A
TRMS Receipt Notice (d303) Back page overlay N/A
HUAL Accessorial Invoice (ba_203) No back page overlay required  Overlay code must be attached to the dummy document code ACCE.
HUAL Renewal Invoice (ba_203) No back page overlay required  Overlay code must be attached to the dummy document code RENW.
HIMM Immediate Invoice (ba_204) No back page overlay required  Overlay code must be attached to the dummy document code IINV.

These standard overlays are attached to the appropriate documents in DOCU and should not be modified or deleted. Any other overlays must be custom programmed by HighJump.
Document overlays are generated through printer macros that reside in the printer’s memory. The macros are defined by HighJump in a program called PRPF (Print Profile) that is attached to your printer(s) in PRIN. 
Macros must be loaded onto the printer in the program LMPR (Load Macro to Printer). 
FXOL screen showing standard overlays

### PRINTING OVERLAY DOCUMENTS <a id="printing-overlay-documents"></a>

The number of pages printed when you print an overlay document depends on whether the document has a front/back overlay and the type of output (a printer, VIEW, MAIL or FAX).
Example 1 (three-page document with front overlay only)
NOTE If you switch off your printer for any reason, you must reload the printer macros by running LMPR. If you fail to run LMPR, no overlays will print when you print the document.
TYPE OF 
OUTPUT RESULT
Printer Three pages of output
FAX Fax cover page (if any) plus three pages of output
VIEW Three pages of a PDF document
MAIL Same as VIEW

Example 2 (three-page document with front and back overlay)

### Customizing the Accessorial Renewal Invoice <a id="customizing-the-accessorial-renewal-invoice"></a>

There are two customization options for the accessorial invoice:
 you can make the number of inventory levels shown on the accessorial invoice customer dependent for both the renewal and receipt part of the invoice
 you can make the SKU used for reporting quantities customer dependent

### CHANGING THE NUMBER OF INVENTORY LEVELS SHOWN <a id="changing-the-number-of-inventory-levels-shown"></a>

To use this feature, you create the appropriate reporting types codes in DEAS (Depositor Alternate Sort) and then attach your DEAS code to each customer in the Reporting Block of CUST.
Your DEAS code should have two numbers in it; for example, RIR2. The first number will govern the number of inventory levels shown for the renewal part of the invoice and the second number will govern the number of inventory levels shown for the receipt part of the invoice. A code of R1R2 attached to a given customer will mean that the customer's invoice will show renewal charges rolled up to level 1 and receipt charges rolled up to level 2.
If your DEAS code contains a single digit (for example, ABC1), only the renewal part of the invoice will be rolled up. If you DEAS code contains more than two digits (for example, 1234), only the first two digits will be used to roll up the invoice.
If you do not use DEAS codes, the accessorial invoice will show the maximum of inventory levels for a given customer.
TYPE OF 
OUTPUT RESULT
Printer If your printer supports duplex printing, three pages of output with the back overlay printed on the back of each of the three pages. If your printer does NOT support duplex printing, six pages of output (three for the front page of the document and three for the back overlay of the document).
FAX Fax cover page (if any) plus three pages of output plus one additional page for back overlay
VIEW Six pages of a PDF document (three for the front page of the document and three for the back overlay of the document)
MAIL Same as VIEW

DEAS screen showing code of R1R2
CUST screen showing DEAS code of R1R2 in Reporting Block

### CHANGING THE SKU FOR REPORTING QUANTITIES <a id="changing-the-sku-for-reporting-quantities"></a>

You can specify which SKU(s) you want AccellosOne 3PL to use when reporting quantities and make this 
SKU customer dependent. For example, if an item’s quantity breakdown is 100 cases per pallet, you could show a quantity of 2 pallets as 2 pallets for one customer and 200 cases for another customer. 
To show quantities in the lowest SKU (for example, cases), create a single level code in DEAS called SK1 and attach this code to the Reporting Block of CUST. To show quantities in the highest SKU, create a single level code in DEAS called SK2 and attach this code to the Reporting Block of CUST. 
If any of a customer’s items have three SKU's (pallet/case/each), SK1 would represent the lowest SKU or eaches, SK2 would represent cases and SK3 would represent the highest SKU or pallets.

CUST screen showing customer A’s invoices assigned the DEAS code of SK1 for reporting quantities in cases
If you do not set up SK1/2/3 codes in DEAS and attach them to the Reporting Block of CUST, AccellosOne 
3PL will display quantities in mixed SKU. For example, 2 pallets, 20 cases for a pallet/case item or 2 pallets, 
30 cases, 5 eaches for a pallet/case/each item.

### Adding a Remit To Address to Invoices <a id="adding-a-remit-to-address-to-invoices"></a>

If you wish to print a “remit to” address on an invoice that differs from the company address set up in COMP (Company Code), you must create a customer code of REMITTO set up in CUST. 

CUST screen showing customer code of REMITTO

### Working With Oracle Reports <a id="working-with-oracle-reports"></a>

AccellosOne 3PL supports reports and documents built using Oracle Reports Builder. The Oracle report must be saved in .jsp format in the directory $DEL4_HOME/del4/src/rdf.
Documents that print in PRRE/PRRM/PROR/PROM at a given inbound or outbound flow must be set up in 
DOCU like any other document. Documents and reports that print from ActiveDesktop and are not flow dependent must be set up in EXJO, JOSE and OPAC like any other AccellosOne 3PL program.
Oracle reports can be opened to VIEW, e-mailed, sent to the spooler and opened from the Time Block using e-File just like any other AccellosOne 3PL report or document.

list of Oracle Reports
DOCU screen showing packing slip document

### SETTING UP A DOCUMENT TO PRINT IN PRRE/PRRM/PROR/PROM <a id="setting-up-a-document-to-print-in-prre-prrm-pror-prom"></a>

1 Set up your document in DOCU as follows:
Print Form Name = d100id for inbound documents and d100ob for outbound documents

Report Name = your Oracle report name in $DEL4_HOME/del4/src/rdf without the file extension
2 Attach your document to the appropriate inbound or outbound flow in DIFP using the document code in 
DOCU rather than the Oracle Report name.

### SETTING UP A DOCUMENT/REPORT TO PRINT FROM ACTIVEDESKTOP <a id="setting-up-a-document-report-to-print-from-activedesktop"></a>

If you wish to print Oracle Reports from ActiveDesktop, you must set up the report in EXJO, JOSE and OPAC just like any other AccellosOne 3PL program.
1 Enter EXJO and set up your executable job code as follows:
Job Name = user defined
Type = Oracle Reports
External Executable = your Oracle report name in $DEL4_HOME/del4/src/rdf without the file extension
EXJO screen showing report_test setup
2 Enter JOSE and set up your job selection code as follows:
Selection Code = user-defined
Executable Job Code = your executable job code in EXJO

JOSE screen showing report_test setup
3 Enter OPAC and give the appropriate operators access to the job selection code that you set up in JOSE.
OPAC screen showing operators with access to ORTEST

### RUNNING AN ORACLE REPORT <a id="running-an-oracle-report"></a>

1 In ActiveDesktop, click on Oracle Reports.

ActiveDesktop
2 Select the report that you wish to run from the dropdown list.
Oracle Reports parameter screen
3 Enter your report parameters and click on Submit Query.

Oracle Reports output

### Setting Up SSRS Documents <a id="setting-up-ssrs-documents"></a>

The setup in DOCU for SSRS documents is very similar to any other document setup for Oracle Reports. For outbound documents the Print Form Name is d100oAPM, while for inbound documents the Print Form Name is d100iAPM. The Oracle Name field must consist of a valid SSRS report or document name in A1Report.
NOTE The suffix “_MR” cannot be part of the report name.

DOCU screen showing setup for SSRS packing slip

## BarTender Label Printing <a id="bartender-label-printing"></a>

*Manual O — Core Documents*

### Overview <a id="overview"></a>

AccellosOne 3PL-BarTender integration consists of two components: BarTender Enterprise and BarTender 
Label Printing.
BarTender Enterprise allows you to design and code your own labels, add the appropriate bar code components, format the font size, color and position of text and insert logos and other graphic images. It provides full access to the AccellosOne 3PL database using predefined data streams such as Inbound, Outbound, 
Packing and Quick Response. For each data stream, you can define up to three labels: two regular labels and one separator label.
For example, if you are designing an outbound label, the outbound data stream allows you to populate your label(s) with the customer code, shipper code, carrier code, order number, order total weight or any other value related to outbound orders. 
The second component of the integration, BarTender Label Printing, is part of ActiveDesktop. It allows you to query AccellosOne 3PL orders, receipts and waves and to print labels for these orders, receipts and waves.
The Printing Jobs tab in BarTender Label Printing allows you to monitor all label printing both inbound and outbound from a single access point. You can cancel, requeue and reprint entire print jobs or individual labels within a job. When you look up your print jobs, BarTender Label Printing shows complete information about your printed labels including:
 the operator code and company code
 the document number and document code
 the start, finish and elapsed times
 the label count and label status
 the print status and error message (if any)
Status window showing printed, failed, rejected and labels per second counts

### Assigning Access to BarTender Label Printing <a id="assigning-access-to-bartender-label-printing"></a>

You assign operator and company access to BarTender Label Printing in OPAC (Operator Access) and 
COAC (Company Access) by means of the job selection code ADBART (BarTender).
OPAC screen showing job selection code of ADBART under the ACTIVE subsystem
COAC screen showing job selection code of ADBART under the ACTIVE subsystem

### Accessing BarTender Label Printing <a id="accessing-bartender-label-printing"></a>

You access BarTender Label Printing from ActiveDesktop.
1 From ActiveDesktop, click on BarTender Label Printing.
2 Proceed to work in BarTender Label Printing.

### SETTING UP YOUR OUTPUT PARAMETERS <a id="setting-up-your-output-parameters"></a>

There are three output parameters that apply to printing in BarTender Label Printing: chunking, duplication and lock by.
Output fields showing default parameters

### Looking Up Orders and Receipts in BarTender <a id="looking-up-orders-and-receipts-in-bartender"></a>

The Labels command allows you to query orders and receipts by company code, customer code, document number and carton ID. This query retrieves all open and confirmed orders or receipts regardless of print status. That is, the order or receipt line does not require a document in the AccellosOne 3PL print queue in order to be retrieved.
FIELD DESCRIPTIONS
Chunking 50:200
Chunking refers to the number of labels in a given print job. There are two possible chunking values: the first value (usually smaller) is the maximum number of mixed labels in a print job, while the second value (usually larger) is the maximum number of “same” labels in a print job.
Duplication 1
For stress testing or simple duplication, you can override the default value of 1 and print multiple copies of the same label.
NOTE This output parameter applies to printing within BarTender Label 
Printing only. It does NOT apply to printing within AccellosOne 3PL or RF.
Lock by Printer
Service
If you select Printer, no print job will be sent to a printer until the previous job assigned to that printer has finished printing. If you select Service, no print job will be sent to a service or BarTender instance until the previous job assigned to that service has finished printing.

1 Select the appropriate data stream (inbound, outbound, packing, etc.).
2 If you have multiple BarTender services, select the appropriate print host from the dropdown list.
3 Key in your search parameters. The document number is a mandatory search parameter. All other search parameters such as company code, customer code and label are optional search parameters. 
BarTender Label Printing window showing search parameters
4 When you finish entering your search parameters, click on Labels.
BarTender Label Printing window showing search results for company code V6, customer A and document type of inbound
5 If you wish to sort the search results in a particular order, double click on the appropriate heading. The first time that you double click a column, the column will be sorted in ascending (lowest value first) order. 
If you double click the same column again, it will be sorted in descending (highest value first) order.
6 If you want to perform a second search, click on Clear and then proceed with the second search.

### USING THE PICK LIST FUNCTION <a id="using-the-pick-list-function"></a>

You can use the pick list function to select a company code, customer code, document number and document line number. 
1 Click on the field whose value you wish to select from a pick list.
Pick list for customer code
2 If the pick list is too long for a single page, you can click on the Next button to see the next page of codes.
3 When you find the code that you wish to select, click on it and then close the pick list window.

### CLEARING A SEARCH <a id="clearing-a-search"></a>

The Clear command allows you to remove any existing values in your search parameters and perform a fresh search.

### Printing Labels <a id="printing-labels"></a>

You print/reprint labels by performing a query for the order/receipt lines whose labels you wish to print. After retrieving your order/receipt lines, you click on Labels.
You can print to either an AccellosOne 3PL printer (normal procedure) or to a Windows printer (for testing purposes).
1 If you have multiple BarTender services, select the appropriate print host from the dropdown list.
NOTE When you print labels from BarTender Label Printing, the document restrictions set up in DIFP and DOCU do not apply. That is, you can print labels for any open order or receipt regardless of the order or receipt’s flow and regardless of your reprint job restrictions in DOCU. 
Printing/reprinting from BarTender Label Printing is intended for testing purposes only and is not recommended for a production environment.

2 Select the appropriate data stream (inbound, outbound, packing, etc.).
3 Key in your search parameters. The document number is a mandatory search parameter. All other search parameters such as company code, customer, code and label are optional search parameters. 
4 Select your label(s) from the dropdown list(s).
BarTender Label Printing window showing labels for receipt 1425
5 Click on the checkboxes of the labels that you wish to print. If you wish to print all labels, click on the checkbox in the header row.
6 Click on Printer Code to select your AccellosOne 3PL printer from the pick list. If you wish to print to a 
Windows printer instead, click on the Select Printer dropdown list to select your printer.
7 Click on Labels.
8 Click on Print.
Status window showing print queue number

### Monitoring Your Print Jobs <a id="monitoring-your-print-jobs"></a>

The Printing Jobs tab allows you to monitor all label printing both inbound and outbound from a single access point. When you look up your print jobs, BarTender shows the following information:
 the initiator (whether the label was printed from BarTender, AccellosOne 3PL or Wave Manager)
 the operator code and company code
 the document number and document code
 the data stream that the label is based on and the printer name
 the start, finish and elapsed times
 the label count and label status
 the print status and error message (if any)
The Printing Jobs tab shows both active and inactive printing jobs. An active printing job is a job currently printing or in the print queue (that is, about to print). An inactive printing job is a job that has already printed or has attempted to print but failed.

For inactive printing jobs, BarTender Label Printing shows logs and history grouped by date.
1 Click on Printing Jobs.
Printing Jobs window showing Active, Queue and Latest buttons
2 Click on the appropriate button (Active, Queue or Latest) to see your print jobs. 
The Active command will display all jobs currently printing, the Queue command will display all jobs currently in the queue and the Latest command will display that last 100 jobs that successfully printed as well as cancelled jobs.
Latest Printing window
3 If you wish to dynamically activate/deactivate the display of any print job column, right click anywhere in the header column.
Columns window showing currently selected columns
4 Proceed to select/deselect the columns to be displayed. To select/deselect all columns, click in the Columns checkbox.

When you finish selecting your display columns, click on any column name (NOT on the checkbox itself) 
to activate the new display.
5 If you wish to suppress the display of all print jobs except logs and history, click on Refresh.
6 When you finish looking up your printing jobs, click on File > Exit to close the Printing Jobs window.

### CANCELLING AN ACTIVE PRINT JOB <a id="cancelling-an-active-print-job"></a>

You can cancel a print job if it is currently printing or in the print queue. Cancelled jobs are moved to the 
Latest Printing window just as non-cancelled or printed jobs are.
1 Click on the appropriate tab: Active or Queue.
2 Select the job(s) that you wish to cancel and click on Cancel.

### REPRINTING A PRINT JOB <a id="reprinting-a-print-job"></a>

You can reprint labels from any job in the Latest Printing window.
1 Click on Latest.
2 Double click on the job whose labels you wish to reprint.
3 Select the labels that you wish to reprint and click on Print.

### LOOKING UP LOGS AND HISTORY <a id="looking-up-logs-and-history"></a>

Log and history information shows all completed jobs grouped by date. You click on any date to see log and history information for that date.
Logs shows all jobs sent to BarTender on a given date from AccellosOne 3PL and RF including those that were not successfully received. Logs contain technical information for use by HighJump support staff.
History, on the other hand, shows all jobs sent to BarTender and successfully received on a given date including jobs submitted within BarTender. History shows the same information as the Active, Queue and 
Latest commands.
1 Do one of the following:
If you wish to look up your logs:
If you wish to look up your history:
a) Click on the date in the Logs column that you wish to look up.
b) When prompted to open or save the file, click on the option that you prefer. If you selected Save, select a location for the log file and click on Save.
a) Click on the date in the History column that you wish to look up.

Printing Jobs window showing all jobs for 2010-10-26
Notepad window showing log information
2 If you opened a log, select File > Exit to close the Notepad window when you finish looking up your log information.

### LOOKING UP THE STATUS OF YOUR PRINT JOBS <a id="looking-up-the-status-of-your-print-jobs"></a>

The Status window shows the following summary information about your print jobs.
 the status of the printer host (connected or exception)
 your lock by option (by service or printer)
 printing (either resumed or paused)
 the number of labels currently printing
 the number of labels in the queue
 the thread and elapsed time in seconds (system information only)
The Today section shows the printed, failed, rejected and labels per second counts for the current date. The first number in the count is the number of jobs, while the second number is the total number of labels. For example, “3/60” means 60 labels in three jobs or 20 labels per job.
A “failed” label is a label that did not print in BarTender, while a “rejected” label is a label that failed validation in AccellosOne 3PL and was not sent to BarTender.
The section below the Today section shows the date and time that ActiveDesktop was last launched as well as the printed, failed, rejected and labels per second counts since that time.

Status window showing printed, failed, rejected and labels per second counts

### Looking Up Your Wave Labels <a id="looking-up-your-wave-labels"></a>

If you use Wave Manager, you can look up and print/reprint your wave labels. For each wave label, BarTender shows the label count, the label total, the customer name, the carton ID and other order-related information. 
Within Wave Manager, the Cartons tab shows the carton ID, carton sequence number and other carton details for each carton in a given wave.
1 Click on Wave Printing.
Search parameters for wave printing
2 If you have multiple BarTender services, select the appropriate print host from the dropdown list.
3 Click on the Wave ID field and select your wave from the pick list.
4 Select either All Labels or Exception Labels from the dropdown list. Exception labels are additional labels generated by the Wave Manager as a result of exceptions while picking such as shorts and suspended holds.
5 When you finish entering your wave parameters, click on Labels.

Labels window
6 If you want to look up carton information for the wave, click on Cartons.
Cartons window showing carton details such as carton ID and sequence number

### Looking Up a Label’s Configuration <a id="looking-up-a-label-s-configuration"></a>

The Configuration command shows the data stream, csv file, metadata, print form name and label name for each label in BarTender Label Printing.
FIELD DESCRIPTIONS
Data stream Data streams are comma-separated files representing one or more AccellosOne 3PL tables. Data streams are set up by HighJump.
Header The csv file is a csv version of the data stream. You import this file into BarTender Enterprise when you wish to build new labels.
Metadata The metadata file contains the table name, the column name, the column description, the column type, the column length and whether the column is nullable. Metadata is for look-up purposes only and is not used in building new labels.
Print Form Name Print form names, which identify the label in DOCU, are set up by HighJump. 

1 Click on Configuration.
Configuration window showing standard labels
2 If you wish to look up the label’s csv file, click on the appropriate csv file.
3 When prompted to open or save the file in Excel, click on Open.
Excel window showing csv file for outbound label
4 When you finish looking up the label’s csv file, click on File > Exit.
Labels The individual labels that can be generated from a single data stream. You can define up to three labels per data stream/print form name.
FIELD DESCRIPTIONS

5 If you wish to look up a label’s metadata, click on view.
BarTender window showing metadata for inbound label
6 When you finish looking up a label’s configuration, click on File > Exit to close Data Stream Metadata window.

### PRINTING A LABEL’S METADATA <a id="printing-a-label-s-metadata"></a>

1 Click on the view command of the label whose metadata you wish to print.
2 Click on Printer Friendly.
3 Select File > Print.
4 Select your printer and click on Print.
5 Click on Close.

### Building New Labels in BarTender Enterprise <a id="building-new-labels-in-bartender-enterprise"></a>

There are five predefined data streams loaded into BarTender Label Printing. You must import these data streams into BarTender Enterprise before you can build a new label. The five predefined data streams are:
 inbound.csv for inbound labels
 outbound.csv for outbound labels
 packing.csv for packing labels
 freeform.csv for custom labels that do not require AccellosOne 3PL data
 quickresp.csv for Quick Response labels

### IMPORTING THE DATA STREAM INTO BARTENDER ENTERPRISE <a id="importing-the-data-stream-into-bartender-enterprise"></a>

1 In BarTender Label Printing, click on Configuration.

2 Double click on the csv file that you wish to import into BarTender Enterprise.
3 When prompted to open or save the file in Excel, click on Save.
4 Save the csv file to your PC.
5 Click on Close to close the Download Complete window.

### PERFORMING THE DATABASE CONNECTION SETUP <a id="performing-the-database-connection-setup"></a>

When setting up your database connection for the label, use the following options:
 use Text file as your Database Type
 select Comma as your Delimitation Type
 when prompted to confirm that the first record of the text file is the header that contains the names of fields, click on Yes

### SAVING YOUR NEWLY DESIGNED LABEL <a id="saving-your-newly-designed-label"></a>

You save your newly designed label (extension.btw) in the folder C:\accellos\3PL-Home\Bartender Reports. 
The name of your label in this folder must match the name of the label in the BarTender Label 1/2 fields in 
DOCU.

### Setting Up Your BarTender Printers in PRIN <a id="setting-up-your-bartender-printers-in-prin"></a>

In PRIN you define the IP address, port and printer name of your BarTender Enterprise software. If you have two or more instances of Bar Tender Enterprise at different IP addresses, you must define one record in PRIN for each unique address.
PRIN screen showing IP address, port and printer name for BarTender printer

### Attaching Your BarTender Label to AccellosOne 3PL <a id="attaching-your-bartender-label-to-accellosone-3pl"></a>

There are two steps to follow in setting up your BarTender Enterprise labels in AccellosOne 3PL: first you set up your label in DOCU and second you attach your DOCU label to the appropriate inbound/outbound flow in 
DIFP.

### SETTING UP YOUR LABELS IN DOCU <a id="setting-up-your-labels-in-docu"></a>

In DOCU you define one record for each data stream/print form name. Each data stream/print form name can contain up to three labels: two regular labels and one separator label. 
FIELD DESCRIPTIONS
Print Form Name See the Configuration tab in BarTender Label Printing for the correct value to be entered in this field.
BarTender Label 1 The name of label 1 in BarTender Label Printing.
BarTender Label 2 Optional
The name of label 2 in BarTender Label Printing.
BarTender Separator 
Label
Optional
The name of your separator label in BarTender Label Printing. Separator labels print each time that one of the following changes: the order or receipt number, the item code or the location.
Sort Sequence for BarTender Labels (SOSE)
Optional
If you do not specify a sort sequence, AccellosOne 3PL will use the default sort sequence of item code/location code. You define a sort sequence by means of SQL statements.

SKU Class for Number of 
Labels
The SKU class that you want AccellosOne 3PL to use when calculating the number of labels to print. For example, suppose a given item has a quantity breakdown of 50 cases per pallet and your order quantity is 1 pallet or 50 cases. If you set this field to pallets, AccellosOne 3PL will generate one label for one pallet. If you set this field to cases, AccellosOne 3PL will generate 50 labels for 50 cases.
The SKU class that you define in DOCU is your system default. If you define a different SKU class in CARR, it will override the SKU class in DOCU. And if you define a different SKU class in CONS, it will override the SKU classes in 
CARR and DOCU.
Rounding Method for 
Number of Labels
U = Up
D = Down
The rounding method that you want AccellosOne 3PL to use for partial quantities. For example, suppose you set your SKU class to pallets and your order quantity is 2 1/2 pallets. If you select U for Up, AccellosOne 3PL will generate three labels. If you select D for Down, AccellosOne 3PL will generate two labels.
The rounding method that you define in DOCU is your system default. If you define a different rounding method in CARR, it will override the rounding method in DOCU. And if you define a different rounding method in CONS, it will override the rounding methods in CARR and DOCU.
FIELD DESCRIPTIONS

DOCU screen showing setup for standard inbound label

DOCU screen showing BarTender Label 1 name

### ATTACHING YOUR DOCUMENT CODES TO DIFP <a id="attaching-your-document-codes-to-difp"></a>

1 Enter DIFP and attach your document codes for BarTender Label Printing to the appropriate inbound and outbound flows of your Depositor Workflow Profile.
Refer to the Setup Guide for complete instructions on attaching documents to flows in DIFP.

A accessorial audit report 1 5 accessorial invoice 6, 68 additional prints of a document, generating 53
ADOP (Auto-Document Operator Printer Setup) 62
Allow Reprint field (DOCU) 56
B
Bar Code Directory field (DOCU) 58
Bar Code File field (DOCU) 58 accessing 79 assigning access to 79 attaching label to WarehouseLogic 92 building new labels in BarTender Enterprise 90 looking up a label’s configuration 88 looking up orders and receipts in 80 monitoring your print jobs 83 overview 78 printing a test label 82 setting up printers in PRIN 91
Batch Type Code (BATP) 64
BATP (Batch Type Code) 64 bill of lading by broker customer 12 case pick label 13 cold storage pick sheet 30 cold storage tally 46 customizing the accessorial renewal invoice 68 cycle count tickets 13
D
DEAS (Depositor Alternate Sort) 68
Depositor Alternate Sort (DEAS) 68
DOCU (Documents) 55
Document Directory field (DOCU) 57
Document File Prefix field (DOCU) 58
Document File Suffix field (DOCU) 58
Document Type Code field (DOCU) 55
Document Types (DOTP) 53
Documents (DOCU) 55
DOTP (Document Types) 53
E extra charge audit 14
F
FedEx shipping label 15
Flag Reprint field (DOCU) 56
FORM (Form Code) 52
Form Code (FORM) 52
Form Code field (DOCU) 56
H
Horizontal Lines field (FORM) 52 immediate audit report 16 immediate invoice 1 17 immediate invoice 2 18 inbound pallet label 19 inbound weight sheet 20
LMPR (Load Macro to Printer) 66
Load Macro to Printer (LMPR) 66 load plan sheet 21
M master bill of lading 22
MH10/UCC-128 labels 24 multiple prints of a document, generating 53
O
Oracle Reports 70
Orientation field (FORM) 52
