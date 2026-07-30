---
title: "Administração — Archive, Purge e Conversões"
description: "Arquivamento e expurgo de dados, conversões, carga por interface e programas utilitários."
layout: default
---

# Administração — Archive, Purge e Conversões

Arquivamento e expurgo de dados, conversões, carga por interface e programas utilitários.

**Fluxo principal:** `ARPU/DEAR/PURG (expurgo) | DEPC/PRCO/LOCO/IFFI (conversao)`

> Fonte: manuais L do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Archiving And Purging <a id="archiving-and-purging"></a>

*Manual L — System Administration*

### Overview <a id="overview"></a>

Purging your system of old data is an essential element of system maintenance and must be done on a regular basis to maintain system performance and to avoid running out of disk storage space. For example, every month you remove all records older than one year. If you do not perform a purge on a regular basis, your system performance will suffer considerably.
Archiving and purging in AccellosOne 3PL is a two-step process:
Archiving and purging can be done during normal business hours. However, because system performance may be affected, it is best done during weekends and off hours.
ARPU (Archive/Purge 
Processing)
First, you run ARPU. This program moves the selected data from the regular system tables to the corresponding archive tables. For example, order headers in E_ORD_H are moved to the archive table H_ORD_H.
DEAR (Delete Archive 
Purge)
Second, you run DEAR. This program removes the records physically from the database and deletes the archive file.

SYSTEM ADMINISTRATION GUIDE 4.2* 81
There is a maximum of four steps to follow in archiving and purging:
ARPU
LOOR
LORE
LOEN
DEAR
Look up archived records?
Yes No
The system creates a register for the data and moves the archived data to the appropriate archive table. For example, order header data is moved from E_ORD_H to H_ORD_H.
You archive your receipts, orders, inventory and charge records in ARPU (Archive/Purge Processing). 
If you wish to look up the orders, receipts and inventory records that have been archived, you use the regular look-up programs (LOOR, 
LORE, LOEN).
You purge the records that you archived in step 1 in DEAR (Delete 
Archive Purge). This step is final and cannot be reversed.
Minimum number of months to retain archive data has passed?
Yes
No

### Setting Up Archiving and Purging <a id="setting-up-archiving-and-purging"></a>

There are two setup programs for archiving and purging: COMP (Company Code) and OPER (Operator 
Code).

### COMP (COMPANY CODE) <a id="comp-company-code"></a>

In COMP you define the following:
 the minimum number of months to retain archived data before the data can be purged in DEAR
 whether or not to allow multiple archive/purge selections in ARPU (multiple selections could affect system performance)
COMP screen

### OPER (OPERATOR CODE) <a id="oper-operator-code"></a>

In OPER you give operators permission to look up archived data in LOOR, LORE and LOEN.

SYSTEM ADMINISTRATION GUIDE 4.2* 83
OPER screen

### Archiving Receipts, Orders, Inventory and Charges in ARPU <a id="archiving-receipts-orders-inventory-and-charges-in-arpu"></a>

You archive receipts, orders, inventory, accessorial charges and immediate charges in ARPU (Archive/Purge 
Processing). In this program you specify the customer, if any, whose records you wish to archive and your cut-off date for the archive.
Depending on the option that you selected in the Allow Multiple Archive/Purge Selections field in COMP, you can archive all five types in one operation or you can run ARPU separately for each type of archiving.

### ARCHIVING RECEIPTS AND ORDERS <a id="archiving-receipts-and-orders"></a>

There are three conditions that must be met before you can archive a receipt or order:
 the receipt or order must have a status of confirmed or deleted; if you manually rate receipts, the confirmed receipt must also be rated
 for confirmed receipts and orders, the confirmation date must be less than or equal to the archive’s cutoff date 
 for deleted receipts and orders, the order or receipt date must be less than the archive’s cut-off date 
1 Enter ARPU.

Archive/Purge Processing (ARPU)
2 Click on New to create a new archive.
3 Key in your cut-off date in the To Date field and press Enter. When you enter your date, AccellosOne 3PL will archive all orders or receipts as follows:
for confirmed orders the order confirmation date is less than the cut-off date for deleted orders the order date is less than the cut-off date for confirmed receipts the receipt confirmation date is less than the cut-off date for deleted receipts the receipt date is less than the cut-off date
TIP If you have a lot of data to archive or have not created an archive for a long time, it is recommended that you start with an early date range; for example, one month after the start of business date or one month after the last purge, etc. When you finish your first archive, increment the cut-off date by one month and perform the second archive. By splitting your archives into multiple jobs, you can reduce the affect on system performance.

SYSTEM ADMINISTRATION GUIDE 4.2* 85
4 Key in your customer code and press Enter. Only data for the customer or customers that you enter in this field will be archived. If you leave this field blank, the archive will include data for all customers.
5 Click in the Process Orders or Process Receipts checkbox.
6 Click on Save . AccellosOne 3PL will generate a register number for the archive.

Archive/Purge Processing (ARPU) screen showing register number and status
7 Click on Process .
8 When all records have been archived, ARPU will close and you will be returned to the main menu.

### ARCHIVING INVENTORY <a id="archiving-inventory"></a>

The way in which the archives inventory option works depends upon the number of inventory levels of your inventory. If your inventory is item-level only, the system archives history records only. A history record is any record in the History Block or History Details Block of LOEN. If your inventory has two or more inventory levels, the system archives the entire entity.
NOTE Inventory attributes and inventory level descriptions are excluded from 

See the following for the rules governing item only inventory versus inventory with two or more levels:
When history records are archived, you can no longer run transaction history reports like THIC (Transaction 
History) and THIS (Transaction History Report) for the purged level 2 and higher entities.
Archiving inventory is a two-step process. First you run CNBC (Clear Non-Billing Customer). Then you run 
ARPU (Process Inventory option).
1 Make sure that billing has run for the inventory that you wish to purge. You run billing by generating and confirming a renewal batch in BILB or by running RENW.
2 Enter CNBC.
3 Key in your customer code and press Enter.
For item-only inventory For inventory with two or more levels
The system will evaluate the following conditions:
 there are no open orders or receipts containing the item
 billing has run for all transactions for this item
If all conditions are met for a given item, the system will calculate the brought-forward balances for the available, on-hand, on order, etc. quantities as of the cut-off date and then delete all history records up until this date. If the new brought-forward balance is not zero, the system will create a new history record in LOEN with a type of BF (Brought Forward Balance). If the new brought-forward balance is zero, no new record is created in LOEN.
The system will evaluate the following conditions:
 the inventory balances for the entity are zero
 there are no transactions after the cut-off date
 there are no open orders or receipts containing that inventory entity
 billing has run for all transactions for this entity
If all conditions are met for a given entity, the system will archive the entire entity (for example, item A, lot 10) and all associated records (that is, the Location Block, History Block and Renewal Block).
TIP If you do not use AccellosOne 3PL to generate invoices and track revenue and if you have set the Rate Receipt Automatically flag in DBIP to N for No, you can use the special verification program RATE to “rate” your receipts. When attached to the flow CORE with the Sequence flag is set to A for After, RATE marks confirmed receipts as “rated”, thereby allowing them to be archived in ARPU without running 
CNBC (Clear Non-Billing Customer).
See [SPECIAL VERIFICATION PROGRAMS](administracao.html#special-verification-programs) for further information on setting up special verification programs.

SYSTEM ADMINISTRATION GUIDE 4.2* 87

Clear Non-Billing Customer (CNBC)
4 Click on Process.
5 If the customer has active billing records, a message will appear. Press Enter to acknowledge the message. An active billing record is a charge in ENAC with a status of Active for Active and a charge total that does not equal zero. If there is an active billing record for inventory included in the purge, that inventory cannot be purged. You must delete the record and then rerun CNBC.
6 Enter ARPU.
7 Click on New to create a new archive.
8 Key in your cut-off date in the To Date field and press Enter. For item-only inventory, the system will purge all history records up until this date; for level 2 and higher entities, the system will purge all records in LOEN for the entity (Location Block, History Block and Renewal Block).
9 Key in your customer code and press Enter. Only data for the customer or customers that you enter in this field will be purged. If you leave this field blank, the purge will include data for all customers.
10 Click on the Process Inventory checkbox to select it.
11 Click on Save . AccellosOne 3PL will generate a register number for the new archive.
12 Click on Process .
13 When all records have been archived, ARPU will close and you will be returned to the main menu.

### ARCHIVING ACCESSORIAL AND IMMEDIATE CHARGES <a id="archiving-accessorial-and-immediate-charges"></a>

The charge must be invoiced and posted to the Daily Invoice Register through BILB (Billing Batch) before you can archive it in ARPU. For manual charges, the cut-off date in ARPU is based on the date that the charge was created in ENAC or ENIN. For automatic charges, the cut-off date in ARPU is based on the date that the receipt or order to which the charge is attached was confirmed.
1 Enter ARPU.
2 Click on New to create a new archive.

3 Key in your cut-off date and press Enter.
4 Key in your customer code and press Enter. Only data for the customer or customers that you enter in this field will be purged. If you leave this field blank, the purge will include data for all customers.
5 Click on the Process Accessorial and Process Immediate Invoices checkboxes to select them.
6 Click on Save . AccellosOne 3PL will generate a register number for the new archive.
7 Click on Process .
8 When all records have been archived, ARPU will close and you will be returned to the main menu.

### Looking Up Archived Records <a id="looking-up-archived-records"></a>

You look up your archived data for orders, receipts and inventory in the normal look-up programs; that is, 
LOOR (Look Up Orders), LORE (Look Up Receipts) and LOEN (Look Up Inventory). For orders, receipts and inventory, the archive number will display in the Header Block of LOOR, LORE and LOEN respectively.
Archived accessorial and immediate charges do not display an archive message in ENAC or ENIN.

### LOOKING UP ARCHIVED ORDERS IN LOOR <a id="looking-up-archived-orders-in-loor"></a>

You look up orders that have been archived in LOOR.
1 Enter LOOR.
2 Key in your search criteria and click on Execute Query.

SYSTEM ADMINISTRATION GUIDE 4.2* 89

Look Up Orders (LOOR) screen showing archive 102
3 When you finish looking up your archived orders, click on Exit to exit.

### LOOKING UP ARCHIVED RECEIPTS IN LORE <a id="looking-up-archived-receipts-in-lore"></a>

You look up receipts that have been archived in LORE.
1 Enter LORE.
2 Key in your search criteria and click on Execute Query.

Look Up Receipts (LORE) screen showing archive 103
3 When you finish looking up your archived receipts, click on Exit to exit.

### LOOKING UP ARCHIVED INVENTORY IN LOEN <a id="looking-up-archived-inventory-in-loen"></a>

You look up inventory records that have been archived in LOEN. 
1 Enter LOEN.
2 Key in your search criteria and click on Execute Query.

SYSTEM ADMINISTRATION GUIDE 4.2* 91

Look Up Inventory (LOEN) screen showing archive 2
3 Use your arrow keys to scroll forward and backward through your inventory records.
4 When you finish looking up your archived inventory, click on Exit to exit.

### LOOKING UP ARCHIVE REGISTERS IN ARPU <a id="looking-up-archive-registers-in-arpu"></a>

After creating a new archive register, you can look up the register to find out the run date, the total number of records purged as well as the total number of records purged by individual table.
1 Enter ARPU.
2 Click on Enter Criteria.
3 Key in your register number, cut-off date or customer restriction and click on Execute Query.

Archive/Purge Processing (ARPU) screen showing register number, run date and total number of records archived
4 Click on Table Details to see all tables included in the archive as well as the actual number of records purged from each table.

SYSTEM ADMINISTRATION GUIDE 4.2* 93
ARPU screen showing table details
5 When you finish looking up your archive registers, click on Exit twice to exit.

### Deleting the Archive in DEAR <a id="deleting-the-archive-in-dear"></a>

You perform the actual purge in DEAR (Delete Archive/Purge). This program removes from the database all the records that you archived in ARPU.
You can delete archives in one of two ways: by register number or by cut-off date.
When you delete by register number, DEAR calculates all the possible records in that register that meet the minimum number of months to retain archived data value that you defined in COMP. If all records in the register meet the minimum number of months condition (that is, less than or equal to the current date minus the number of months that you specified in COMP), the records are purged and the register is deleted. If there are newer records in the register, the newer records will not be purged and the register will remain open.
CAUTION This step is final and cannot be reversed. You cannot retrieve the purged records and restore them to the database.

When you delete by cut-off date, DEAR validates that your cut-off date is less than or equal the current date minus the number of months that you specified in COMP. If this condition is met, DEAR performs the following tasks:
 if all records in a given open register meet the minimum number of months condition, the records are purged and the register is delete
 if there are newer records in a given open register, the newer records will not be purged and the register will remain open
1 Enter DEAR.
2 Do one of the following:

Delete Archive/Purge (DEAR)
3 Click on Process .
To delete by register number: To delete by cut-off date:
a) Key in your purge register number and press Enter.a) Press Enter to bypass the Purge 
Register Number field.
b) Key in your cut-off date and press Enter.
c) If your cut-off date is not acceptable, an error message will display in the hint line. Press Delete to clear the date and enter a new cut-off date.

### Miscellaneous Purging <a id="miscellaneous-purging"></a>

SYSTEM ADMINISTRATION GUIDE 4.2* 95

### PURGING THE SPOOLER FILES IN SPPA <a id="purging-the-spooler-files-in-sppa"></a>

Every time that you print a document or report to a printer other than NONE or VIEW, the system creates a file in the print spooler. It is necessary to purge these files on a regular basis in order to ensure that you do not run out of disk space.
You set up your purge parameters in SPPA (Spool Parameters). Based on the parameters that you enter in this program, the system will automatically purge your reports and documents after a given number of days.
In SPPA you set up two things:
 your default purge parameters 
 any exceptions to your defaults; an exception can apply to a particular document or to a particular document printed for a particular customer 
For example, suppose your system default is set up to purge all reports and documents after three days. An exception could be made, however, for your bill of lading document, which would be retained for five days rather than three. A further exception could be made for bill of lading documents produced for ABC 
SUPPLIES, which would be retained for ten days. 
1 Enter SPPA.
2 In the Automatic Purge of Spool Files field, key in Y for Yes and press Enter.
3 In the Number of Days for Purge Retention field, key in the number of days that you wish to keep your spooler files and press Enter. The value that you enter in this field is your system default.
If you wish to add exceptions to your spooler parameters:
If you do NOT wish to add exceptions to your spooler parameters:
a) In the Customer field of the Document Block, key in the customer code for your exception or use 
.ALL for all customers and press 
Enter.
b) In the Type field, key in S for 
Report or D for Document and press Enter.
c) In the Code field, key in your document or report code and press Enter or use your pick list to select it.
d) In the Days to Retain field, key in the number of days that you wish to retain this document or report and press Enter.
e) Repeat the above steps for each additional exception that you wish to add.
a) Proceed to next step.

Spool Parameters showing three exceptions — one for all customers and one for customer A
4 When you finish setting up your spooler parameters, click on Master Block and Exit to exit.

### PURGING WARNINGS AND MESSAGES <a id="purging-warnings-and-messages"></a>

Whenever a warning message is generated in AccellosOne 3PL, the system creates a record in WAME (Look 
Up Warnings/Messages) that allows you to look up this message at any time. Messages remain in WAME until you purge them in PUWM (Purge Warnings/Messages).

### LOOKING UP WARNING MESSAGES (WAME) <a id="looking-up-warning-messages-wame"></a>

You look up your warning messages in WAME (Look Up Warnings/Messages). For each warning message, 
WAME shows:
 the sequence number (a system-generated number that you can use to track a particular message)
 the routine code (the program that was running when the problem was encountered)
 the date and time that the message occurred
 the operator code of the operator who viewed the message
 the date and time that the operator viewed the message
 the message text
There are two look-up options in this program. You can view either new messages or old messages. A new message is a message that has not been previously viewed. An old message is a message that has been previously viewed by any operator. 

SYSTEM ADMINISTRATION GUIDE 4.2* 97
A message is flagged as viewed when you position your cursor beside the sequence number of the message. 
For example, if you use your arrow keys to cursor down through the first five records in WAME, these five records will all be flagged as viewed; however, any remaining records will have a status of unviewed. 
1 Enter WAME.
2 Click on Enter Criteria.
3 Click Execute Query.
TIP If you wish to scroll through your records without flagging them as viewed, use your page up and page down keys — not your arrow keys. When you use your page up and page down keys, only the first message of each page is flagged as viewed.
If … then … you wish to look up all new messages Proceed to next step.
you wish to look up all messages that have been previously viewed
Press Enter until your cursor is positioned in the Viewed by field. Then key in the code 
ALL.
you wish to query on a particular warning message that has NOT been previously viewed
Key in the sequence number (if known), routine code or message date of the message.
you wish to query on a particular warning message that HAS been previously viewed
Key in the sequence number, routine code or message date of the message. Then key in one of the following: a value in the 
Viewed by field (ALL or the code of the actual operator who viewed the message) 
or the date that the message was viewed.

Look Up Warnings/Messages (WAME) screen showing details for sequence number 558168
4 Click on Text Block to enter the Text Block.
5 If the number of lines in the Text Block exceeds 7, use your arrow keys to view the entire message. 
6 When you finish looking up your warning messages, click on Master Block and Exit to exit.

### PURGING WARNING MESSAGES (PUWM) <a id="purging-warning-messages-puwm"></a>

You purge your warning messages in PUWM (Purge Warnings/ Messages). Purging warning messages is a one-step process; no archive file is created and you cannot reverse PUWM and restore the warning messages to the database.
You can only purge previously viewed messages; if the message has not been previously viewed, it will not be purged.
PUWM allows you to specify the number of records that Oracle will process before committing the purge. This option makes it possible to split up a large job into smaller segments. Each segment is performed separately and should your system fail in the middle of a segment, only that segment will have to be rerun — not previous segments.

SYSTEM ADMINISTRATION GUIDE 4.2* 99
Consider the following examples in which you have a total of 1,000 records to purge:
If you specify a small number (say, 50), the purge will take longer but fewer system resources will be consumed and other programs will run faster. If you specify a large number (say, 1,000), the purge will be completely more quickly but more system resources will be consumed and other programs might be affected. 
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
No records will be committed. When you rerun PURB, all 1,000 records will have to be reprocessed.

SYSTEM ADMINISTRATION GUIDE 4.2* 101

## Conversions <a id="conversions"></a>

*Manual L — System Administration*

### Overview <a id="overview"></a>

AccellosOne 3PL’s conversion programs allow you to convert data on customers, items, locations, existing locations, inventory balances, transaction history, consignees, shippers, carriers, ZIP codes and sales revenue from non-AccellosOne 3PL systems. There are nine steps to follow in performing a conversion:
EXCEL
LOCO
MOCO
PRCO
MOCO
A13PL
COER
In LOCO (Load Conversion), you load the appropriate file into A13PL from a csv file. 
This is a temporary table.
You view and if required modify the data in 
MOCO (Modify Conversion Data).
When you are satisfied that the information in MOCO is correct, you process the conversion in PRCO (Process Conversion). 
PRCO loads the information into the A13PL tables so that it is available in the standard menu programs. 
You query all records in MOCO. 
You run COER (Conversion Exception 
Report) to look up the records that were not loaded. Any unloaded records must be corrected in MOCO. 
You verify the converted data by running a 
A13PL report or by looking up the converted data in ITEM, CONS, LOCA, etc. 
Records remain in 
MOCO?
No Yes
You transfer the csv file to the appropriate directory. 
CSV
You create an Excel spreadsheet based on column layouts defined in the control files.
You save your Excel spreadsheet as a csv file. 
FTP

SYSTEM ADMINISTRATION GUIDE 4.2* 103

### Creating Your Excel Spreadsheets <a id="creating-your-excel-spreadsheets"></a>

The following requirements must be met performing a conversion:
 All mandatory fields must be entered.
 Commas and apostrophes are not allowed in any column.
 The lower case “f” is not allowed in any column. Convert “f” to “F” wherever required.
 Columns must not exceed the prescribed length in any circumstances.
 Date columns should be entered in YYMMDD format.
 All columns should be formatted as text and left justified.
 No columns should have any spaces at the end; that is, padded with spaces.
 When entering numbers, no decimal is required unless you are entering a fraction and decimals must not be padded out with zeroes. For example, you can enter 1.07 in one field, 2 in another field, 145.6 in a third field, etc.
The following restrictions apply to code fields. A code field is a field like customer code, consignee code, shipper code, item code, location code, item billing profile code, quantity breakdown code, etc. that is created in an AccellosOne 3PL maintain program like CUST, ITEM, LOCA, SHIP, DBIP, etc.
 Code fields must be converted in uppercase letters. Lowercase or mixed case code fields are not valid. 
All codes should be created and available in AccellosOne 3PL before running LOCO.
 Code fields in AccellosOne 3PL do not support the single quote (’) and double quote (“) special characters. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.

### Creating Your Flat Files <a id="creating-your-flat-files"></a>

AccellosOne 3PL conversion programs require csv (comma-separated values) files. You create your csv files using the Save As command in Excel. You can save the file to your local hard drive or to the Desktop. After saving your file, open it with Notepad and save it under the appropriate name. The naming convention for each csv file that the system looks for during a conversion is shown below:
CAUTION It is essential to carefully check your data before running PRCO. AccellosOne 3PL’s conversion utility provides only limited validation of converted data; for example, the item conversion does not validate that all the profiles required for a given item have been set up correctly in AccellosOne 3PL. If you convert bad data into AccellosOne 3PL, the data must be manually corrected one record at a time.
DESCRIPTION NAMING CONVENTION
Customer Master Details custcsv.dat
Item Master Details itemcsv.dat

Once you have created your csv file, you must move it into your DEL4 directory ($DEL4_HOME/del4/loader/ data). If you are not sure of the location of your DEL4 directory, contact the Platform Group or your HighJump consultant.
You cannot change these file names. All conversion files must be copied to the appropriate file name listed above for conversion.Once data has been copied to a .dat file, the conversion programs in AccellosOne 3PL can be used to complete the conversion.

### Converting Customer Details <a id="converting-customer-details"></a>

In this conversion file, you set up your customer details. The following codes and profiles must be set up before you can perform a customer conversion:
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

SYSTEM ADMINISTRATION GUIDE 4.2* 105
CUST_ADD1 30 Y address line 1
CUST_ADD2 30 address line 2
CUST_ADD3 30 address line 3
ZIP_CODE 10 Y the customer’s ZIP code or postal code (must be set up in ZIPO)
SMAN_CODE 4 Y the salesperson code for the customer
CUST_REPS_CODE 4 Y the customer service representative for the customer
CUST_TP_FLAG 1 Y W = Warehouse (default)
I = Invoice Only
B = Broker the customer’s account type
GL_MODY_CODE 10 the customer’s general ledger modifier code
CUST_CODE_PAY_OFFC 10 Y the customer’s paying office code
CUST_BILL_PROF_CODE 4 Y the customer’s billing profile (must be set up in DBIP)
CUST_OPS_PROF_CODE 4 Y the customer’s shipping and receiving profile code (must be set up in DSRP)
INFO_FLOW_PROF_CODE 4 Y the customer’s workflow profile code (must be set up in DIFP)
CUST_INVT_PROF_CODE 4 Y the customer’s inventory level profile code (must be set up in DILP)
CUST_ITEM_PROF_CODE 4 Y the customer’s item information profile code (must be set up in DITP)
WHSE_CODE 4 the warehouse to which the customer’s product is restricted (must be set up in 
WARE)
FIELD LENGTH MANDATORY NOTES

CUST_START_BUS_DATE 6 Enter 010101 (YYMMDD). This date will allow you to backdate any receipts for the customer in ENRE.
CUST_LAST_ACT_DATE 6 Reserved for future use
EDI_PROF_CODE 4 the customer’s EDI profile code (must be set up in DEDP)
FRT_PAY_OFFC_CODE 10 Reserved for future use
CUST_FRT_PROF_CODE 4 Reserved for future use
CUST_UPC_PREX 6 this field is used to attach a predefined 
UPC prefix (five digits followed by a hyphen) to all of a customer’s item codes
CUST_TRF_PROF_CODE 4 the transfer profile code is used if you wish to transfer product from one customer to another within your warehouse (must be set up in TRPR)
CUST_DEF_RCPT_SKU_FLAG 1 Y H = High
L = Low in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENRE when the SKU type is not specified
CUST_DEF_ORD_SKU_FLAG 1 Y H = High
L = Low in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENOR when the SKU type is not specified
CUST_DEF_ADJ_SKU_FLAG 1 Y H = High
L = Low in this field, you specify how you want 
AccellosOne 3PL to interpret quantities in 
ENAJ when the SKU type is not specified
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 107
CUST_LAB_CAPT_JOB_LEV_FLAG 1 Y N = No
Y = Yes
Set to N for No.
CUST_ORD_LEV_RES_NUM 1 the inventory level at which reserve logic is activated
CUST_CNVC_NUM 1 Reserved for future use
CUST_LAB_STD_MODY_NUM 5 the customer’s labor standard modifier (may have up to two decimals)
EXTRA_CHG_PROF_CODE 4 the customer’s extra charge profile code (must be set up in ECHP)
CUST_ADD4 30 address line 4
COUNTRY_CODE 4 Y the customer’s country code (must be set up in CNTY)
RF_PROF_CODE 4 the customer’s RF profile code (must be set up in MRFP)
INVT_TERMGY_CODE_I1 1 the first inventory terminology code to appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I2 1 the second inventory terminology code to appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I3 1 the third inventory terminology code to appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I4 1 the fourth inventory terminology code to appear in ENRE (must be set in INTE)
INVT_TERMGY_CODE_I5 1 Reserved for future use.
INVT_TERMGY_CODE_O1 1 the first inventory terminology code to appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O2 1 the second inventory terminology code to appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O3 1 the third inventory terminology code to appear in ENOR (must be set in INTE)
FIELD LENGTH MANDATORY NOTES

### Converting Item Details <a id="converting-item-details"></a>

In this conversion file, you set up your item details. The following codes and profiles must be set up before you can perform an item conversion:
 Customer Code (CUST)
 Class Code (CLAS)
 Commodity Code (COMM)
 General Information Profile Code (IINP)
 Item Billing Profile Code (IBIP)
 Quantity Breakdown Profile Code (IQBP)
 Item Shipping Profile Code (ITSH)
 Item Process Profile Code (IPRP)

### ENTERING THE QUANTITY BREAKDOWN <a id="entering-the-quantity-breakdown"></a>

You enter an item’s quantity breakdown in the VAR_QTY_BKD-_QTY1/2/3/4/5 fields. If your item has a single quantity breakdown (for example, cases only), you enter a 1 in the ITEM_QTY_BKD_BASE_NUM field and a 
1 in the VAR_QTY_BKD_QTY1 field. If your item has multiple SKU types in its quantity breakdown, you set the smallest SKU type to 1 and the next highest SKU type to the number of units of the smaller SKU type that fit in the next highest SKU type.
For example, if your quantity breakdown were 10 eaches per case and 60 cases per pallet, you would enter the following:
INVT_TERMGY_CODE_O4 1 the four inventory terminology code to appear in ENOR (must be set in INTE)
INVT_TERMGY_CODE_O5 1 Reserved for future use.
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program to indicate records that have been processed versus those that may have failed and are still pending.
TEL_LIST_CODE 4 the telephone list code (must be set up in 
TETP)
TEL_NUM 20 the telephone number
TEL_CONTACT 30 the contact name
TEL_CONTACT_DES 20 the contact’s position
CUST_STAT 1 Y Set to A for Active
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 109
Quantity Breakdown Level 1 = 60
Quantity Breakdown Level 2 = 10 
Quantity Breakdown Level 3 = 1
CAUTION The value in the Quantity Breakdown Level 1 field must equal the product of the number of layers and the quantity per layer plus the odd layer quantity (if any). For example, if your Quantity Breakdown Level 1 is 60, your number of layers and quantity per layer must equal 5/12, 6/10 or some other combination of numbers whose product is 60.
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
WHSE_CODE 4 your warehouse restriction if any (must be set up in WARE)

ITEM_VAR_QTY_BKD_FLAG 1 Y Y = Yes
N = No (default)
This field allows you to specify whether you wish to allow non-standard quantity breakdowns for the item. If you set this flag to No, the quantity breakdown that you define in the 
Quantity Breakdown Block of this program is standard and cannot be changed for any particular receipt. If you set this flag to Yes, you can change the item’s quantity breakdown on a receipt.
ITEM_WGT_TP_CODE 4 Y Y = Standard Weight
If you set this field to Standard Weight, the system will use the standard weight specified in the Quantity Breakdown Block of this program; you will not be able to modify this weight during receipt entry or order entry. If you wish to enter the weight manually on shipping or receiving or calculate the weight in a different manner, see “Non-Standard 
Weight Options” in the Setup Guide for further information.
ITEM_CODE_SUB 20 your substitute item if any
ITEM_VALUE NUM 13 the item’s value (may have up to four decimals)
PROS_PROF_CODE 4 Y the item’s process profile code (must be set up in IPRP)
SHIP_PROF_CODE 4 Y the item’s shipping profile code (must be set up in ITSH)
ITEM_LOC_PROF_CODE 4 the item’s item location profile code (must be set up in ILOP)
ALT_INVT_REP_TP_CODE 4 the item’s alternate inventory report type (must be set up in ITAS)
ALT_INVT_REP_CODE 20 the item’s alternate reporting type code (must be set up in ITAS)
FIELD LENGTH
MANDA
TORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 111
ALT_INVT_REP_UPC_CODE 20 the item’s UPC code
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program to indicate records that have been processed versus those that may have failed and are still pending.
NUM_OPEN_DAY NUM 3 Y The number of days that an open lot item can remain open. If you do not use open lots, set this field to 0.
ITEM_BILL_PROF_CODE2 4 item billing profile code 2
ITEM_BILL_PROF_CODE3 4 item billing profile code 3
ALLOW_ENTRY_LEV_NUM NUM 1 The number of inventory levels needed for this item. You can enter any number between one and the maximum number of levels for the customer defined in DILP.
COUNTRY_CODE 4 the item’s country code (must be set up in 
CNTY)
TAX_CODE 4 the item’s tax code
PICK_PROF_CODE 4 the item’s picking profile code (must be set up in PIPR)
HAZ_CODE 4 the item’s hazard code (must be set up in 
HAZA)
ITEM_HOLD_PROF_CODE 4 the items’ hold profile code (must be set up in 
IHOP)
EXTRA_CHG_PROF_CODE 4 the items’ extra charge profile code (must be set up in ECHP)
ITEM_CRS_DOCK_FLAG 1 Y = Yes
N = No the item’s cross dock flag
FIELD LENGTH
MANDA
TORY NOTES

ITEM_KIT_FLAG 1 Y Y = Yes
N = No (default)
the item’s kit flag
ITEM_KIT_TP_FLAG 1 Y if 
ITEM_KIT_
FLAG = Y
P = Pending
W = Weight the order line type for kit components
QTY_BKD_PROF_CODE 4 Y must be set up in IQBP
ITEM_QTY_BKD_BASE_NUM NUM 1 Y the quantity breakdown level at which you wish to track an item’s weight and size (for example, if your item’s quantity breakdown is pallet/case/each and you wish to track the item’s weight and size at the each level, you would enter 3 in this column)
VAR_QTY_BKD_QTY1 NUM 4 Y VAR_QTY_BKD_QTY1 is for your largest 
SKU type (for example, pallets), 
VAR_QTY_BKD_ QTY2 is for your next largest SKU type (for example, cases), etc. The number for the larger SKU type indicates how many of the smaller SKU types make up one unit of the larger SKU type.
For example, if your quantity breakdown were 
10 eaches per case and 60 cases per pallet, you would enter the following:
Quantity Breakdown Level 1 = 60
Quantity Breakdown Level 2 = 10
Quantity Breakdown Level 3 = 1
VAR_QTY_BKD_QTY2 NUM 4 Y
VAR_QTY_BKD_QTY3 NUM 4 Y
VAR_QTY_BKD_QTY4 NUM 4 Y
VAR_QTY_BKD_QTY5 NUM 4 Y
ITEM_QTY_BKD_QTY_PER_LAY NUM 3 Y the quantity per layer or tie (use 1 if layer configuration is set to No)
ITEM_QTY_BKD_NUM_LAY 3 Y the number of layers or hi (use 1 if layer configuration is set to No)
ITEM_QTY_BKD_QTY_ODD_LAY 3 the quantity, if any, of your odd layer
FIELD LENGTH
MANDA
TORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 113
ITEM_QTY_BKD_WHOLE_FLAG 1 Y W = Whole (default)
P = Prorate whether to round up partial quantities like 1.5 pallets or whether to charge for the actual quantity stored
WGT_MEAS_CODE 4 Y the item’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
MT = Metric Tonne
LT = Long Tonne
LBS = Imperial Pounds
KG = Kilogram
GM = Grams
OZ = Ounces
TN = Imperial Tons
ITEM_QTY_BKD_WGT_GROSS NUM 15 Y the item’s gross weight (may have up to six decimals)
ITEM_QTY_BKD_WGT_NET NUM 15 Y the item’s net weight (may have up to six decimals)
LINEAR_MEAS_CODE 4 Y your linear measurement code (FT, CM, IN, 
M, etc.) 
ITEM_QTY_BKD_LEN NUM 8 the item’s length (may have up to three decimals)
ITEM_QTY_BKD_WID NUM 8 the item’s width (may have up to three decimals)
ITEM_QTY_BKD_HGT NUM 8 the item’s height (may have up to three decimals)
VOL_MEAS_CODE 4 your volume measurement code (CL, FLOZ, 
GAL, GALI, etc.)
ITEM_QTY_BKD_VOL NUM 15 the item’s volume (may have up to six decimals)
The following columns are all optional and apply to an item’s second SKU when this SKU is not defined as the base SKU for the item’s cube and weight. See the column description for the base SKU for further information. For example, for 
WGT_MEAS_CODE_2, see WGT_MEAS_CODE.
FIELD LENGTH
MANDA
TORY NOTES

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
The following columns are all optional and apply to an item’s third SKU when this SKU is not defined as the base SKU for the item’s cube and weight. See the column description for the base SKU for further information. For example, for WGT_MEAS_CODE_3, see 
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

SYSTEM ADMINISTRATION GUIDE 4.2* 115
LINEAR_MEAS_CODE_3 4
ITEM_QTY_BKD_LEN_3 NUM 8
ITEM_QTY_BKD_WID_3 NUM 8
ITEM_QTY_BKD_HGT_3 NUM 8
VOL_MEAS_CODE_3 4
ITEM_QTY_BKD_VOL_3 NUM 15
The following columns are all optional and apply to an item’s fourth SKU when this SKU is not defined as the base SKU for the item’s cube and weight. See the column description for the base SKU for further information. For example, for 
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
The following columns are all optional and apply to an item’s fifth SKU when this SKU is not defined as the base SKU for the item’s cube and weight. See the column description for the base SKU for further information. For example, for WGT_MEAS_CODE_5, see 
WGT_MEAS_CODE.
FIELD LENGTH
MANDA
TORY NOTES

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
LANG_CODE 4 the item’s language code (only required if you use alternate items and descriptions in ALIT)
ACC_ITEM_DES1 40 an alternate description for the item (only required if you use alternate items and descriptions in ALIT)
ITEM_ALLOW_BAND_FLAG 1 Reserved for future use
ITEM_BAND_SKU_CLASS_NUM 1 Reserved for future use
ITEM_BAND_MAX_QTY 9 Reserved for future use
ITEM_ALLOW_MIX_PLT_FLAG 1 Reserved for future use
SCAN_PARAM_CODE 4 the item’s scan parameter code (must be set up in SCPR)
FIELD LENGTH
MANDA
TORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 117

MOCO screen for pass name of ITEM
ITEM_CODE_MASTER_FLAG 1 Y N = No (default)
Y = Yes
Set to N for No.
FIELD LENGTH
MANDA
TORY NOTES

MOCO screen for pass name of ITEM

### Converting Location Details <a id="converting-location-details"></a>

In this conversion file, you set up your location details. The following codes and profiles must be set up before you can perform a location conversion:
 Company Code (CNTY)
 Warehouse Code (WARE)
 Location Billing Code (LODE)
 Location Type Code (LOTP)
 Isolator Type Code (ISOL)
 SKU Code (SKUS)
 the location’s location structure type code
A location details conversion inserts new records in the database. Existing location records are not touched.
FIELD LENGTH
MANDATORY NOTES
COMP_CODE 2 Y the company code (must be set up in COMP)
WHSE_CODE 4 Y the warehouse code (must be set up in 
WARE)

SYSTEM ADMINISTRATION GUIDE 4.2* 119
LOC_CODE 12 Y the location code
LOC_DES 30 the location description
LOC_STAT 1 Y A = Active or D = Deactivated
LOC_BILL_CODE 4 Y the location’s location billing code (must be set up in LODE)
LINEAR_MEAS_CODE 4 Y the linear measurement code (FT, CM, IN, M, etc.)
LOC_HGT NUM 8 Y the location’s height (may have up to three decimals)
LOC_WID NUM 8 Y the location’s width (may have up to three decimals)
LOC_LEN NUM 8 Y the location’s length (may have up to three decimals)
LOC_CUBE NUM 11 the location’s cube (may have up to three decimals)
LOC_TP_CODE 4 Y the location’s location type (must be set up in 
LOTP)
ISOL_CODE 4 Y the location’s isolator code (must be set up in 
ISOL)
SKU_CODE 4 Y the location’s SKU code (must be set up in 
SKUS)
LOC_MAX_SKU_CAPC NUM 4 Y the maximum capacity for the location
SKU_CAPC_PCENT NUM 6 Reserved for future use
SPACE_CAPC_PCENT NUM 6 Reserved for future use
LOC_PRT_PROF_CODE 4 the location’s location print profile code (must be set up in LPPR)
CYC_CNT_PROF_CODE 4 the location’s cycle count profile code (must be set up in CYCP)
FIELD LENGTH
MANDATORY NOTES

HOLD_CODE 4 the location’s hold code (must be set up in 
HOLD)
LOC_SIZE_CODE 4 the location’s location size code (must be set up in LOCS)
LOC_LAB_STD_MODY
_NUM
NUM 5 the location’s labor standard modifier (may have up to two decimals)
WGT_MEAS_CODE 4 Y the location’s weight measurement code (LBS, KILO, GRAM, TON, etc.)
LOC_WGT NUM 15 Y the location’s weight limit or 0 if there is no weight limit (may have up to six decimals)
LOC_CODE_WGT_
MAST
12 the location’s master location for weight
LOC_STRUCT_TP_
CODE 
4 Y the location’s location structure type:
MHE = MHE Code
STIC = Static/Stationary Locations (default)
LOC_SHIP_UNIT_ID 20 Reserved for future use
PICK_SEQ_NUM 9 See the RF User Guide for further information on configuring the sort sequence for picking tasks in RFPIC.
LOC_VOICE_CHK_DIGIT1 5 the first location check digit for voice picking
LOC_VOICE_CHK_DIGIT2 5 the second location check digit for voice picking
LOC_VOICE_CHK_DIGIT3 5 the third location check digit for voice picking
LOC_VERT_HGT_FACT_CODE 4 the vertical height of the location
LOC_AISLE_REF 4 used to identify aisles when the aisle cannot be extracted from the location code in the 
Location Attributes Block of WARE
LOC_FACING_REF 4 an additional field that can be used for sorting purposes
FIELD LENGTH
MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 121

MOCO screen for pass name of LOC
LOC_FRONT_ALIAS 12 the front location alias
LOC_FRONT_ALIAS_CHK_DIGIT 5 the check digit for the front location alias
LOC_BACK_ALIAS 12 the back location alias
LOC_BACK_ALIAS_CHK_DIGIT 5 the check digit for the back location alias
PUT_SEQ_NUM 9 the put-away/directed move sort sequence number
LOC_USE_LAST_PUT_FLAG 1 Y Y =Yes
N = No (default)
whether or not you can put-away product into this location using the options in the Last 
Location Used group in ILOP
FIELD LENGTH
MANDATORY NOTES

### Converting Existing Locations <a id="converting-existing-locations"></a>

An existing locations conversion is similar to a location details conversion. However, unlike a location details conversion, an existing locations conversion deletes all existing location records in the database before performing an insert based on your new csv file.
The only restriction to an existing locations conversion is location bill code: if you delete and recreate a location record, the original location bill code attached to that location will be retained. Your new location bill code attached to the location will be ignored.

### Converting Consignee Details <a id="converting-consignee-details"></a>

In this conversion, you convert your consignees. The following codes and profiles must be set up before you can perform a consignee conversion:
 the consignee’s ZIP code (ZIPO)
 the consignee’s load analysis code (LDAN)
 the customer code for the consignee (CUST)
FIELD LENGTH
MANDATORY NOTES
LOC_STAT 1 Y U = Update or D = Deactivated
FIELD LENGTH MANDATORY NOTES
CON_CODE 10 Y the consignee code
CON_NAME 30 Y the consignee name
CON_STAT 1 Y Set to A for Active
CON_ADD1 30 Y Address line 1
CON_ADD2 30 Address line 2
CON_ADD3 30 Address line 3
ZIP_CODE 10 Y the consignee’s ZIP code or postal code (must be set up in ZIPO)
MES_CODE 4 the consignee’s bill of lading message code (must be set up in MESS)

SYSTEM ADMINISTRATION GUIDE 4.2* 123
CON_LAST_ACT_DATE 6 Reserved for future use
LOAD_ANAL_CODE 4 Y the consignee’s load analysis code (must be set up in LDAN)
CON_FRT_APPO_FLAG 1 Y Set to N for No
CON_FRT_DISC_PCENT NUM 10 Y Set to zero
FRT_DEST_CODE 10 Y the consignee’s ZIP code or postal code (must be set up in ZIPO)
CUST_CODE 10 the consignee’s customer code (must be set up in CUST) or .ALL for all customers
PICK_PROF_CODE 4 the consignee’s pick profile code (must be set up in PIPR)
INFO_FLOW_PROF_
CODE
4 the consignee’s workflow profile code (must be set up in DIFP)
TEL_LIST_CODE 4 the consignee’s telephone list code (must be set up in TETP)
TEL_NUM 20 the telephone number for the telephone list code (must be set up in TELE)
TEL_CONTACT 30 Y* the contact name
* Only mandatory if you enter a telephone 
number.
TEL_CONTACT_DES 20 the contact’s position
CON_BORD_FLAG 1 Y A = Always
N = Never (default)
whether or not back orders are activated for this consignee
EXT_REF_NUM1 20 miscellaneous reference information about a consignee
EXT_REF_NUM2 20 miscellaneous reference information about a consignee
FIELD LENGTH MANDATORY NOTES

EXT_REF_NUM3 20 miscellaneous reference information about a consignee
EXT_REF_NUM4 20 miscellaneous reference information about a consignee
CON_ALLOW_BANDING_FLAG 1 Reserved for future use
CON_BANDING_SKU_CLASS_NU
M
1 Reserved for future use
CON_CONSL_TP 1 Reserved for future use
PALL_CODE Reserved for future use
CON_SPS_REQ_FLAG 1 whether or not the consignee is marked as having a special requirement
CON_ASN_REP_TP 1 Reserved for future use
CON_MSDS_REQ_FLAG 1 Reserved for future use
LANG_CODE 4 if you have an alternate item and description set up in ALIT (Alternate Item and Language) 
for an item, an alternate item and description will be captured when that item is being shipped to this consignee
SKU_CLASS_NUM 4 the SKU class that AccellosOne 3PL uses to calculate the number of labels to print in BarTender or ShippingLive
SKU_CLASS_NUM_RND_FLAG 1 U = Up
D = Down the rounding method that you want AccellosOne 3PL to use for partial quantities when deciding how many labels to generate
CON_UCC128_LABEL_REQ_FLAG 1 Reserved for future use
CON_COMPL_ORD_FLAG 1 Y N = No (default)
Y = Yes whether or not allocation of fully filled orders only is activated
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 125

MOCO screen for pass name of CON

### Converting Shipper Details <a id="converting-shipper-details"></a>

In this conversion, you convert your shippers. The following codes and profiles must be set up before you can perform a shipper conversion:
 the shipper’s ZIP code (ZIPO)
 the shipper’s load analysis code (LDAN)
 the country code (CNTY)
FIELD LENGTH MANDATORY NOTES
SHIP_CODE 10 Y the shipper code
SHIP_NAME 30 Y the shipper name
SHIP_STAT 1 Y Set to A for Active
SHIP_ADD1 30 Y address line 1
SHIP_ADD2 30 address line 2

SHIP_ADD3 30 address line 3
ZIP_CODE 10 Y the shipper’s ZIP code or postal code (must be set up in ZIPO)
WGT_MEAS_CODE 4 Y the shipper’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
SHIP_LAST_ACT_DATE 6 Reserved for future use
LOAD_ANAL_CODE 4 Y the shipper’s load analysis code (must be set up in LDAN)
FRT_DEST_CODE 10 Reserved for future use
INFO_FLOW_PROF_CODE 4 the shipper’s workflow profile code (must be set up in DIFP)
SHIP_LAB_STD_MODY_NUM 7 the shipper’s labor standard modifier (may have up to two decimals)
EXTRA_CHG_PROF_CODE 4 Reserved for future use
SHIP_ADD4 30 address line 4
COUNTRY_CODE 4 Y the shipper’s country code (must be set up in 
CNTY)
EXT_REF_NUM1 4 miscellaneous information about a shipper
EDI_PROF_CODE 4 the shipper’s EDI profile code (must be set up in DEDP); this profile overrides the default 
EDI profile attached to CUST - Customer 
Setup
SHIP_ESTAB_NUM 20 the shipper’s establishment number
SHIP_TP_CODE 1 Y O = Other
R = Repair
S = Store
V = Vendor
W = Warehouse
Unless otherwise instructed by your 
HighJump consultant, set to W for Warehouse.
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 127

MOCO screen for pass name of SHIP

### Converting Carrier Details <a id="converting-carrier-details"></a>

In this conversion, you convert your carriers. The following codes and profiles must be set up before you can perform a carrier conversion:
 the carrier’s ZIP code
 the carrier’s country code
FIELD LENGTH MANDATORY NOTES
CARR_CODE 10 Y the carrier code
CARR_NAME 30 Y the carrier name
CARR_STAT 1 Y Set to A for Active
CARR_ADD1 30 Y address line 1
CARR_ADD2 30 address line 2
CARR_ADD3 30 address line 3

ZIP_CODE 10 Y the carrier’s ZIP code or postal code (must be set up in ZIPO)
CARR_WGT_MEAS_FLAG 1 Y the carrier’s weight measure (I for Imperial or M for Metric)
MES_CODE 4 the message that will print on the carrier’s bill of lading (must be set up in MESS)
CARR_CODE_PAY 10 Y set to the carrier code in the CARR_CODE column
FRT_TP_CODE 4 Y set to .ALL
CARR_LAST_ACT_DATE 6 Reserved for future use
CARR_STD_ALPHA_CODE 4 Y the carrier’s predefined SCAC code or “X” if the carrier does not have such a code
CARR_TP_CODE 3 Y the freight interface type code (FRT for freight interface or NFR for no freight interface)
EXTRA_CHG_PROF_CODE 4 Reserved for future use
CARR_LAB_STD_MODY_NUM 7 the carrier’s labor standard modifier (may have up to two decimals)
CARR_ADD4 30 address line 4
COUNTRY_CODE 4 Y the carrier’s country code (must be set up in 
CNTY)
EDI_PROF_CODE 4 the carrier’s EDI profile code (must be set up in 
DEDP); this profile overrides the default EDI profile attached to CUST - Customer Setup
TRSPT_MODE_CODE 4 the carrier’s transport mode code (must be set up in TRMO)
CARR_EXT_FRT_FLAG 1 whether or not the carrier’s orders will be available in A1 Transport
GEN_NUM_PROF_CODE 4 Reserved for future use
ISOL_CODE 4 Reserved for future use
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 129
MOCO screen for pass name of CARR

### Converting Transaction History Details <a id="converting-transaction-history-details"></a>

In this conversion, you convert your transaction history records. The following codes and profiles must be set up before you can perform a transaction history conversion:
 Customer Code (CUST)
 Item Code (ITEM)
 Warehouse Code (WARE)
 Location Code (LOCA)
CARR_ALLOW_BANDING_FLAG 1 Reserved for future use
CARR_COMPL_LABEL_FLAG 1 Reserved for future use
CARR_REQ_EDI_FLAG 1 Reserved for future use
TRSPT_UNIT_VAL_HIST_FLAG 1 Reserved for future use
FIELD LENGTH MANDATORY NOTES

 Adjustment Code (ADJU)
These transactions will be created as IF (Information Only) transaction types. They will have no impact on inventory balances.
NOTE You cannot look up transaction history details in MOCO.
FIELD LENGTH MANDATORY NOTES
CUST_CODE VARCHAR2(10) Y the customer code for the transaction
INVT_LEV1 VARCHAR2(40) Y the product’s item code
INVT_LEV2 VARCHAR2(40) Y the item’s level 2 value
INVT_LEV3 VARCHAR2(40) Y the item’s level 3 value
INVT_LEV4 VARCHAR2(40) Y the item’s level 4 value
INVT_LEV5 VARCHAR2(40) Reserved for future use
HOLD_CODE VARCHAR2(4) Y Use an asterisk (“*”) if there is no hold on the product.
WHSE_CODE VARCHAR2(4) Y the product’s warehouse code
LOC_CODE VARCHAR2(12) Y the product’s location code
MVT_EFF_TRANS_DATE DATE Y the date that the transaction took place
MVT_UNIT NUM 9 Y the number of units involved in the transaction 
MVT_CNVC_QTY NUM 6 the number of conveyances involved in the transaction
WGT_MEAS_CODE VARCHAR2(4) Y the product’s weight measure (LBS, KILO, 
GRAM, TON, etc.)
TRANS_WGT NUM 17 Y the product’s gross weight (up to six decimal places)
TRANS_WGT_NET NUM 17 Y the product’s net weight (up to six decimal places)

SYSTEM ADMINISTRATION GUIDE 4.2* 131
LINEAR_MEAS_CODE VARCHAR2(4) Y the product’s linear measurement code (FT, 
CM, IN, M, etc.) 
TRANS_CUBE NUM 17 Y the product’s total cube (up to six decimal places)
DOC_NUM NUM 9 Y the order, receipt or adjustment number
DOC_LINE_NUM NUMBER(4) Y the line number
DOC_LOC_LINE_NUM NUMBER(4) Y the location line number
OP_CODE NUMBER(20) Y the operator who entered the transaction (must be set up in OPER)
MVT_REF1 VARCHAR2(10) Y the consignee (for orders), the shipper (for receipts) or the adjustment code (for adjustments)
CARR_CODE VARCHAR2(10) the transaction’s carrier (orders or receipts only)
LOAD_TP_CODE VARCHAR2(4) the transaction’s load type (orders or receipts only)
DOC_REF1 VARCHAR2(20) the customer order number (for orders) or the reference number (for receipts)
DOC_REF2 VARCHAR2(20) the PO number (for orders) or the probill number (for receipts)
DOC_REF3 VARCHAR2(20) Extra Reference Number 1 (orders and receipts only)
DOC_REF4 VARCHAR2(20) Extra Reference Number 2 (orders and receipts only)
FIELD LENGTH MANDATORY NOTES

### Converting Revenue Master Details <a id="converting-revenue-master-details"></a>

In this conversion file, you convert your sales revenue. The conversion program loads your revenue by revenue analysis code into AccellosOne 3PL. Once loaded you can run any AccellosOne 3PL sales report and look up the revenue that you converted. For example, suppose you had $1,500 in freight revenue in 
January 1999 and you performed a revenue master conversion. When you ran SALE (Sales Report), you would see the amount of 1,500 in the January 1999 column of the report for freight revenue. The columns in this table are separated by tildes. 
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
CONV_UPD_FLAG VARCHAR2(1) Leave this field blank. It is used by the conversion program to indicate records that have been processed versus those that may have failed and are still pending.
FIELD LENGTH MANDATORY NOTES
CUST_CODE VARCHAR2(10) Y the customer code for the revenue (must be set up in CUST)
REVN_ANAL_CODE VARCHAR2(4) Y the revenue analysis code for the revenue (must be set up in REVA)
REVN_DATE DATE Y The date that the revenue was earned. Must be in YYMMDD format.
REVN_AMT VARCHAR2(10) Y the revenue amount
FIELD LENGTH MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 133

MOCO screen for pass name of REVN

### Converting ZIP Codes <a id="converting-zip-codes"></a>

In this conversion, you convert your ZIP codes for countries other than the US and Canada. The following codes and profiles must be set up before you can perform a ZIP code conversion: 
 Country Code (CNTRY)
 State/Province Code (STPR)

MOCO screen for pass name of ZIP

### Converting Inventory Balances <a id="converting-inventory-balances"></a>

In this conversion, you convert your inventory balances. Inventory balances consist of the item code, inventory levels, the weight, on-hand quantity, renewal dates, the original receipt date and the warehouse code/location code. Inventory balances are posted as an adjustment in AccellosOne 3PL and the adjustment date is the date that you processed the conversion in PRCO.
When converting item balances, you must define all items down to the lowest inventory level. For example, if you identify product by item, by lot number and by pallet ID, you must specify an item code, lot number and pallet ID number for each record that you wish to convert. 
The following codes and profiles must be set up before you can perform an inventory balance conversion:
 Warehouse Code (WARE)
 Location Code (LOCA)
NOTE You cannot process multiple records containing the same inventory entity and location; for example, you cannot have in balcsv.dat two records for item A, lot 1, expiry date = June 1 in which the warehouse code and location are the same. You must sum up the inventory balances for the two records and create a single record for that item/level 2/level 3 combination and that location.

SYSTEM ADMINISTRATION GUIDE 4.2* 135

### CONVERTING BILLING INFORMATION <a id="converting-billing-information"></a>

If you are converting billing information, the following pieces of information may be required:
 the item’s next renewal date 
 the item’s last renewal date (for historical data only)
 the item’s original qualifying quantity
 the item’s original qualifying weight
 the number of renewal days (only required if the renewal dates on your old system do not match your 
AccellosOne 3PL renewal dates)
 the item’s location billing profile code (for historical data only)
FIELD LENGTH
MANDATORY NOTES
CUST_CODE 10 Y your customer code (must be set up in CUST)
INVT_LEV1 20 Y your item code (must be set up in ITEM)
INVT_LEV2 40 Y your level 2 value
CONV_UNIT NUM 10 Y The item’s on-hand quantity in the lowest SKU code (for example, if your quantity breakdown is pallets/ cases and you enter 10 in this field, your inventory balance will be recorded as 10 cases). Decimal values are not accepted.
CONV_WGT NUM 17 Y The item’s on-hand gross weight in the weight measure code defined for the item in ITEM (may have up to six decimals).
If you do not know the item’s exact gross weight, enter zero (0) as your weight. AccellosOne 3PL will calculate the weight based on your setup in ITEM. That is, gross weight X CONV_UNIT or on-hand quantity in lowest SKU.
RENW_QTY NUM 10 Reserved for future use 
RENW_WGT NUM 17 Reserved for future use
DATE_NXT 6 Y The item’s next renewal date in YYMMDD format (if you do not use AccellosOne 3PL for billing, enter 
700101). This date cannot be earlier than the conversion processing date in PRCO.
DATE_LAST 6 The item’s last renewal date in YYMMDD format (used for historical data only). This date cannot be later than the conversion processing date in PRCO.

INVT_ORG_RECD_DATE 6 Y The item’s original receipt date in YYMMDD format. 
This date cannot be later than the conversion processing date in PRCO.
INVT_EXPY_DATE 6 The item’s expiry date in YYMMDD format. This date cannot be earlier than the conversion processing date in PRCO.
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
INVT_CLS_FLAG 1 If the lot is open, set this field to N for No. If the lot is closed or if the item cannot be processed as an open lot, leave this field blank.
NUM_CASE_STOR_CALC 6 The item’s original qualifying quantity for renewal storage charges — that is, the number of units that the system uses to look up the per rate. If you do not enter a quantity in this field, the system will use the on-hand quantity.
FIELD LENGTH
MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 137
CONV_WGT_NET 17 Y the item’s on-hand net weight in the weight measure code defined for the item in ITEM (may have up to six decimals)
If you do not know the item’s exact net weight, enter zero (0) as your weight. AccellosOne 3PL will calculate the weight based on your setup in ITEM. That is, net weight X CONV_UNIT or on-hand quantity in lowest SKU.
VAR_QTY_BKD_FACT 30 If the item is a variable quantity breakdown item, you enter its quantity breakdown factor in this field. The factor is always expressed in terms of the lowest SKU type; for example, if your quantity breakdown is 60 cases per pallet and 12 eaches per case, you would enter the following:
000720000012000001
Each breakdown is six characters in length and must be padded out with leading zeroes.
NOTE Entering a value in this field will overwrite the default setup in ITEM and is only required if the item is a variable quantity breakdown.
RENW_ORG_RATE NUM 10 If you set the Original or Current Rate on Renewals flag in DBIP to R for Renewal Original, you must enter your original renewal rate in this field. You can enter up to four decimal places.
ORG_CHG_CODE 4 Reserved for future use.
CONV_UPD_FLAG 1 Leave this field blank. It is used by the conversion program.
NUM_RENW_DAY 1 Y If the renewal date on the system that you are converting from differs from the renewal date in AccellosOne 
3PL, you must adjust the date in this field. For example, if your system uses June 30 for product that actually renews on July 1, you would enter 1 in this field (June 30 + 1 day). 
FIELD LENGTH
MANDATORY NOTES

MOCO screen for pass name of BAL
WGT_STOR_CALC 17 The item’s original qualifying weight for renewal storage charges — that is, the weight that the system uses to look up the per rate. If you do not enter a weight in this field, the system will use the on-hand weight. You can enter up to six decimal places.
ITEM_BILL_PROF_CODE 4 The item billing profile code for this item (used for historical data only). If you do not enter a code in this field, the system will use the item billing profile code attached to ITEM.
CNVC_QTY NUM 6 Reserved for future use
HOLD_SHIP_FLAG 1 Y N = No (default)
Y = Yes
If the product is on hold, whether or not the hold is shippable.
FIELD LENGTH
MANDATORY NOTES

SYSTEM ADMINISTRATION GUIDE 4.2* 139

### Miscellaneous Conversions <a id="miscellaneous-conversions"></a>

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

### Performing the Conversion <a id="performing-the-conversion"></a>

After you have created your csv files, you are ready to perform the conversion.

### STEP 1 — LOADING THE CONVERSION IN LOCO <a id="step-1-loading-the-conversion-in-loco"></a>

In this step, you load the appropriate .dat file into a temporary AccellosOne 3PL table. You can only run 
LOCO once for any given record; if the record that you are loading is already in the conversion table, you will not be able to update it by rerunning LOCO.
LOCO loads the records in a staging table. It does not flag or delete the records in the .dat file. As such, if you rerun LOCO on the same dat file, it will create bad data in the table. LOCO creates records in the table first and at the end it updates the records with the company code from the company in which LOCO was run. As such, if the same record already exists, it will fail as a unique index error.
There are three error conditions that can occur when running LOCO:
 LOCO encounters a duplicate record and stops running
 LOCO encounters a field that exceeds its prescribed length and stops running
 the number of columns in the csv file does not match the number of columns in the control file
If you know Unix and the vi editor, you can easily identify the issue and fix the problem. The error file 
PASScsv.dat.log can be found in the del4/work/faxlp directory where PASS is the LOCO PASS name; for example, bal, item, loc, con, etc. 
Open the appropriate log file in the vi editor to find out what the issue is. Then exit the log file and go to del4/ loader/data and open the appropriate pass.dat file. Go to the specific record causing the problem and fix it. 
Next delete all records before the problem record as these records have already been loaded and cannot be reloaded. Lastly, save file and then rerun LOCO.
1 Make sure that you are in the correct company.
2 Enter LOCO.

3 Select the pass name corresponding to the type of data that you wish to convert and press Enter.
4 Press Enter to display the Begin Loading button.
5 Click on Begin Loading to load the flat file.

Load Conversion (LOCO) screen
6 When you finish loading your records, click on Exit to exit.

### STEP 2 — VIEWING AND MODIFYING THE CONVERSION DATA IN MOCO <a id="step-2-viewing-and-modifying-the-conversion-data-in-moco"></a>

In this step, you view the information that was loaded in the previous step. If required, you can modify the information to correct any errors that occurred during the loading process as well as any values that you have identified as incorrect.
1 Enter MOCO.
2 Key in the pass name of the loaded data from step 1 and press Enter. 
3 Click on Execute Query.
NOTE If the loader encounters any errors in LOCO, the program will abort. Investigate the problem and then attempt to rerun LOCO.

SYSTEM ADMINISTRATION GUIDE 4.2* 141

Modify Conversion screen for pass name of LOC
Depending on the pass name that you entered, the appropriate MOCO screen will appear. MOCO is a query screen that allows you to view and modify the data loaded in the AccellosOne 3PL tables. You may use this screen to view all data or you can perform a query on specific criteria. The total number of records for the query can be seen in the top right hand corner.
4 Check the data in MOCO. If any data is incorrect, you can correct it by overtyping. Then press Enter or 
F12 to commit your changes. Alternatively, you can delete the record in MOCO and manually create the record in the appropriate AccellosOne 3PL program such as ITEM, CONS, CUST or SHIP.
You cannot create new records in MOCO.

### STEP 3 — PROCESSING THE CONVERSION IN PRCO <a id="step-3-processing-the-conversion-in-prco"></a>

Once you have checked the data in MOCO and made any necessary modifications, you are ready to perform the conversion in PRCO. This program loads the information into the AccellosOne 3PL tables so that it is available in the standard menu programs. For example, if you have loaded an item file, the items will be 
CAUTION Code fields in AccellosOne 3PL do not support the single quote (’) and double quote (“) special characters. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported. A code field is a field like customer code, consignee code, shipper code, item code, location code, item billing profile code, quantity breakdown code, etc. that is created in a AccellosOne 3PL maintain program like CUST, 
ITEM, LOCA, SHIP, DBIP, etc.

available in ITEM after PRCO has been run. No AccellosOne 3PL tables are updated or changed until PRCO is run. 
In addition to the pass name, this program requires a run date. This date will be the conversion date for the data in the specified pass file. For example, if inventory balances are being converted, the run date in PRCO will be the date that the inventory is available in AccellosOne 3PL.
1 Enter PRCO.

Process Conversion (PRCO)
2 Select your pass name from the dropdown list and press Enter.
3 If required, make any necessary changes to your run date and press Enter.
4 Click on Process.

### STEP 4 — MODIFYING CONVERSION DATA IN MOCO <a id="step-4-modifying-conversion-data-in-moco"></a>

In this step, you return to MOCO and query all records. If any records remain in MOCO, this means that some records were not converted due to incorrect values or because they already existed in AccellosOne 3PL. Go to Step 5 and run COER (Conversion Exception Report) to find out which records were not converted. If no records remain in MOCO after performing Step 3, then the conversion was successful and you can skip Step 
5 and go directly to Step 6.
CAUTION If you are converting billing data, it is essential that the run date in 
PRCO matches the extraction date — that is, the date that you loaded the conversion in LOCO from your flat files. If the run date in PRCO does not match the extraction date, renewal storage charges may not be calculated correctly.
If you are doing an inventory balance conversion, make sure that your run date is consistent with your DATE_NXT, DATE_LAST and INVT_ORG_RECD_DATE values in balcsv.dat.

SYSTEM ADMINISTRATION GUIDE 4.2* 143

### STEP 5 — RUNNING COER (CONVERSION EXCEPTION REPORT) <a id="step-5-running-coer-conversion-exception-report"></a>

In this step, you run COER to look up records that were not converted in step 3. COER will generate a report describing the problem with each record remaining in MOCO. You should modify the records in MOCO to rectify the problem and then rerun PRCO and COER to ensure that all problems have been rectified. Repeat the process until no records remain in MOCO or COER.
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

### STEP 6 — VERIFYING THE CONVERTED DATA <a id="step-6-verifying-the-converted-data"></a>

Once data has been converted and no records remain in MOCO or on the COER report, the data that has been converted may need to be verified in the AccellosOne 3PL programs. 
You can do this in one to two ways: you can run the applicable reports in AccellosOne 3PL and comparing these reports to reports from the converted system or you can perform a spot check in the applicable look-up programs. 
Refer to the table below for the appropriate look-up programs and reports:

### Transferring Data from One Company to Another <a id="transferring-data-from-one-company-to-another"></a>

You can transfer item details and inventory balances from one AccellosOne 3PL company to another in the program DEPC (Data Extraction Process for Conversion). DEPC is ideal for moving company-specific data from one company to another for testing or other purposes.
The following restrictions apply to an item master extraction in DEPC:
 the item must have a status of Active in ITEM
 mandatory profiles like the location code, warehouse code, item billing profile code, quantity breakdown profile code, etc. must be set up manually in the target system or moved there through COCO (Copy 
Codes Between Companies) before you can run DEPC
The following restrictions apply to an inventory balance extraction in DEPC:
 no inventory history is extracted
 the inventory must have an on-hand quantity greater than zero
 the inventory must be confirmed (inventory on open orders and receipts is not extracted)
 mandatory profiles like the location code, warehouse code, item billing profile code, quantity breakdown profile code, etc. must be set up manually in the target system or moved there through COCO (Copy 
Codes Between Companies) before you can run DEPC csv File Look-Up Program Report itemcsv.dat ITEM ITLI loccsv.dat LOCA EMLO concsv.dat CONS CONL shipcsv.dat SHIP SHIL custcsv.dat CUST CUPR carrcsv.dat CARR CARL zipcsv.dat ZIPO balcsv.dat LOEN INHR, LOCT

SYSTEM ADMINISTRATION GUIDE 4.2* 145
DEPC is restricted to the company that you currently working in. If you run DEPC in company W1, only company W1 data will be extracted. If you wish to extract W2 data as well, you must switch to company W2 and then rerun DEPC for the second company.
1 Make sure that all required codes and profiles are set up in your target AccellosOne 3PL system. 
2 Enter the from company; that is, the company whose data you wish to extract.
3 Enter DEPC.
4 Key in ITEM or BAL and press Enter.
5 If required, key in a customer code restriction and press Enter. If you do not need a customer code restriction, press Enter to bypass this field.
FIELD DESCRIPTIONS
Extract ITEM / BAL ITEM
BAL
The type of data being extracted.
From Customer Optional
If you enter a customer code restriction in this field, only item details and inventory balances for that customer will be extracted.
<C>sv Flat File or Conversion <T>ableC = csv
T = table
The destination for the extracted data. If you select C for csv, the data will be extracted into a csv file and you must run LOCO to load the extracted data. If you select T for Table, the data will loaded directly into a table and will be immediately available in MOCO without the need to run LOCO.
Transfer to Company Only required for a conversion table extraction
Your to company.

6 Do one of the following:

DEPC (Data Extraction Process for Conversion)
7 Click on Process.
8 If you are extracting both item and inventory balance information, repeat steps 2 to 7 for either ITEM or 
BAL.
9 Proceed to [Performing the Conversion](administracao-manutencao.html#performing-the-conversion).
If you wish to extract the data to a flat file:
If you wish to extract the data to a database table:
a) Key in C for csv and press 
Enter.
a) Key in T for Table and press 
Enter.
b) Key in your to company code and press Enter. Your to company is the company where you want to copy the extracted data to.

SYSTEM ADMINISTRATION GUIDE 4.2* 147

## Miscellaneous Programs <a id="miscellaneous-programs"></a>

*Manual L — System Administration*

### Clearing Terminal Locks in CLTL <a id="clearing-terminal-locks-in-cltl"></a>

AccellosOne 3PL uses a system of table locks to ensure that only one user at a time is altering a given table. 
For example, if user 1 is entering an order, then user 2 cannot allocate the same order. Sometimes a system failure will occur when a user is modifying an order and as a result the lock will remain in place instead of being automatically removed. When this happens, AccellosOne 3PL will automatically clear the lock when the 
Oracle session expires and a login event occurs (that is, a user logs in to or logs off from AccellosOne 3PL).
Should you wish to clear the lock manually before the Oracle session expires, you must do so in CLTL. 
CLTL shows the active sessions for all operators currently signed on including any locked sessions. For each session, CLTL shows the terminal ID, the operator code, the company code and the program in which the operator is currently working. If the program field is blank, the operator is currently in the main menu and not using any program.
When you clear a lock, the program name is removed but the terminal ID, operator code and company code remain in CLTL.
The following conditions apply to the clearing of locks in CLTL:
 You must be defined as a system administrator in OPER (Operator Code) before you can clear a terminal lock in CLTL.
 If you wish to clear yourself, you must open a new session.
1 Enter CLTL.
2 Click on Enter Criteria.
3 Key in your terminal ID and/or your operator code and click on Execute Query.

Clear Terminal Locks screen showing four active sessions
4 Position your cursor over the terminal that you wish to clear.
5 Click on Clear Locks. 
CAUTION When clearing terminal locks in CLTL for a user, make sure that the user exits the program being cleared before he or she resumes work in the program. 
Failure to do so could lead to out of balance inventory. 

SYSTEM ADMINISTRATION GUIDE 4.2* 149
6 When the message “User still logged on. Are you sure?” appears, click on Yes to proceed. AccellosOne 
3PL will remove the name of the program from the Current Selection column. However, the terminal ID, operator code and company code will remain in CLTL.
7 Repeat the above two steps for each additional terminal lock that you wish to remove.
8 When you finish removing your terminal locks, click on Exit to exit.

### Copying Item Codes in COIT <a id="copying-item-codes-in-coit"></a>

You can copy all active items from one customer to another in COIT. For example, suppose you have two customers: CUST1 and CUST2. CUST1 has three items (A, B and C) and CUST2 has two items (D and E). If you copy CUST1’s items to CUST2 using COIT, CUST2 will have five items — A, B, C, D and E.
The following requirements must be met before you can copy items:
 customers cannot be invoice type only
 customers cannot be the same
 customers must have the same inventory level profile
COIT is typically used in warehouses in which multiple customers share the same item codes.
1 Enter COIT.
2 Key in your from customer and press Enter.
3 Key in your to customer and press Enter.
NOTE COIT copies item information only such as the item code, description, quantity breakdown, billing profile code, weight, etc. It does not copy lot numbers, inventory balances or transaction history information. If you want to transfer inventory from one customer to another, you must perform a transfer adjustment in ENAJ, ENOR (Transfer type order) or MATR.

Copy Items From One to Another
4 Click on Process.

### Adjusting an Item’s Quantity Breakdown in AEQB <a id="adjusting-an-item-s-quantity-breakdown-in-aeqb"></a>

AEQB allows you to change the quantity breakdown of an item for all product currently in your warehouse. If you change an item’s quantity breakdown in the Quantity Breakdown Block of ITEM, your change will affect new inventory only; that is, only inventory received after you make the change. AEQB, on the other hand, allows you to change the quantity breakdown of product currently in your warehouse.
For example, suppose your original quantity breakdown for a particular item is 10 cases per pallet and you have two pallets (20 cases) in your warehouse. If you change the item’s quantity breakdown to 20 cases per pallet in AEQB, looking up your inventory in LOEN after the change will show one pallet containing a total of 
20 cases in your warehouse.
If an item is defined as a standard quantity breakdown item, you must apply the change to all existing inventory in your warehouse. If, however, an item is defined as a variable quantity breakdown item, you can individually change the quantity breakdown of each inventory entity. For example, lot 101 can have 
10 cases per pallet, lot 102 can have 20 cases per pallet and lot 103 can have 30 cases per pallet.
If you wish to add a breakdown level (for example, from pallets only to pallets/cases) or remove a breakdown level (for example, from pallets/cases to pallets only), you cannot run AEQB. You must contact HighJump for assistance and fill out an authorization form.

SYSTEM ADMINISTRATION GUIDE 4.2* 151

### REPORTS <a id="reports"></a>

If the report shows totals in the lowest SKU (for example, cases), changing an item’s quantity breakdown will have no affect on the report's totals. If, on the other hand, the report shows totals in a higher SKU such as pallets, the way in which AccellosOne 3PL calculates totals will depend on the type of report — inventory or history.
Inventory reports will calculate totals based on the current setup in the ITEM master. For example, if you change your quantity breakdown from 100 cases per pallet to 80 cases per pallet, your pallet total in any inventory report will be based on the new quantity breakdown. Your case total, on the other hand, will not be affected.
History reports will calculate totals on a transaction by transaction basis using the quantity breakdown in effect when the transaction was performed.
CHANGING THE QUANTITY BREAKDOWN OF A STANDARD QUANTITY 
BREAKDOWN ITEM
1 Enter AEQB.

Adjust Entity Quantity Breakdown (AEQB)
2 Key in your customer code and press Enter.
3 Do one of the following:
4 Click on Execute Query.
If you are changing the quantity breakdown of a single item:
If you are changing the quantity breakdown of multiple items:
a) Key in your level 1 value or select if from the item pick list.
a) Proceed to next step.

5 If you did not enter a level 1 value in step 3, click on the appropriate customer/item combination to select the item that you wish to work with. AccellosOne 3PL will populate the Detail Block with all inventory entities for the selected item. 
If you have a large number of records for a given customer and are concerned about performance, you can deselect the Auto Display Inventory Details check box to suppress the display of the inventory details. When you find the item that you wish to work with, click on the Auto Display Inventory Details check box again to select it.

Adjust Entity Quantity Breakdown (AEQB)
6 Click on Update Quantity Breakdown.
Click on the appropriate customer/item combination to select the item that you wish to work with

SYSTEM ADMINISTRATION GUIDE 4.2* 153

Item Quantity Breakdown Details screen
7 Proceed to change the item’s quantity breakdown by entering new values in the Quantity, Number of Layers, Quantity Per Layer and Quantity Odd Layer fields.
8 When you finish making your changes, click on Apply Changes to return to AEQB.

AEQB showing query on level 2 value (lot 102)
9 Click on Select All.
10 Click on Update Selected Records.
11 Check the Update Status message to ensure that your change was successful. If it was, the message “Entity Successfully Updated” will display.
12 Click on Exit to exit AEQB.

CHANGING THE QUANTITY BREAKDOWN OF A VARIABLE QUANTITY 
BREAKDOWN ITEM
1 Enter AEQB.

Adjust Entity Quantity Breakdown (AEQB)
2 Key in your customer code and press Enter.
3 Do one of the following:
4 Click on Execute Query.
5 If you did not enter a level 1 value in step 3, click on the appropriate customer/item combination to select the item that you wish to work with. AccellosOne 3PL will populate the Detail Block with all inventory entities for the selected item. 
If you have a large number of records for a given customer and are concerned about performance, you can deselect the Auto Display Inventory Details check box to suppress the display of the inventory details. When you find the item that you wish to work with, click on the Auto Display Inventory Details check box again to select it.
NOTE You cannot update the quantity breakdown of a specific inventory entity if that inventory entity is on an open order or receipt or is locked by another user.
If you are changing the quantity breakdown of a single item:
If you are changing the quantity breakdown of multiple items:
a) Key in your level 1 value or select if from the item pick list.
a) Proceed to next step.

SYSTEM ADMINISTRATION GUIDE 4.2* 155

Adjust Entity Quantity Breakdown (AEQB)
6 Do one of the following:
If you wish to change the quantity breakdown of new product and existing product:
If you wish to change the quantity breakdown of existing product only:
a) Click on Update Quantity 
Breakdown.
b) Proceed to change the item’s quantity breakdown by entering new values in the Quantity, Number of Layers, Quantity Per Layer and Quantity Odd Layer fields.
c) When you finish making your changes, click on Apply 
Changes to return to AEQB.
a) Proceed to next step.
Click on the appropriate customer/item combination to select the item that you wish to work with

Item Quantity Breakdown Details screen

Adjust Entity Quantity Breakdown (AEQB)
7 Proceed to select the inventory records in the Detail Block that the new quantity breakdown will apply to. 
You individually select records by clicking on them or you can use the Select All and Deselect 
All commands. You can also query on individual level 2, 3 and 4 values by means of the Level 2, Level 3 and Level 4 “Refine Your Query” fields.

SYSTEM ADMINISTRATION GUIDE 4.2* 157

AEQB showing query on level 2 value (lot 102)
8 When you finish selecting your inventory records, click in the PLT field and key in your new quantity breakdown.
9 Click on Update Selected Records.
10 Check the Update Status message to ensure that your change was successful. If it was, the message “Entity Successfully Updated” will display.
11 Click on Exit to exit AEQB.

### Adjusting Location Billing Codes in ADLB <a id="adjusting-location-billing-codes-in-adlb"></a>

This program allows you to change a location’s location billing code. For example, you assigned the location billing code of FREZ to location 101 in warehouse A and you want to change this code to COOL. Changes in 
ADLB are effective immediately; the next time that you generate your batch in the appropriate program, 
AccellosOne 3PL will generate the applicable charges according to the charge code attached to your new location billing code.
You can change the location billing code of a single location, all locations in a single warehouse or all locations assigned to a particular location billing code.
You cannot change a location’s location billing code in LOCA (Locations).
1 Enter ADLB.
2 Proceed to query the appropriate records:
To retrieve all locations in a given warehouse …
Key in your warehouse code and click on Execute Query.

3 Click on Location Bill Block.
4 Key in your new location billing code and press Enter.

Adjust Location Billing Code (ADLB) screen showing change from general to dry
5 Do one of the following:
To retrieve a specific location …
Key in your warehouse code and press Enter. Then key in your location code and click on Execute Query.
To retrieve all locations belonging to a given location billing code …
Press Enter twice to bypass the Warehouse Code and Location 
Code fields. Then key in your location billing code and click on Execute Query.
If you wish to change the location billing code of the currently selected location:
If you wish to change the location billing code of all locations in the header block of 
ADLB:
a) Click on Process One. a) Click on Process All.

SYSTEM ADMINISTRATION GUIDE 4.2* 159

Adjust Location Billing Code (ADLB) screen showing Remarks Block
6 Do one of the following:
7 Click on Exit to exit.

### Adjusting Location Types in ADLT <a id="adjusting-location-types-in-adlt"></a>

You can change your location type for a single location or for a range of locations in ADLT. There are three location restrictions in this program: you can change a location type for all locations in a warehouse, for a given location or for all locations belonging to a given location type.
There are two options in this program: Process One and Process All. Process One will change the location type of the currently selected record only while Process All will change the location type of all records in the 
Header Block. For example, suppose you retrieve ten locations from Warehouse 1. You will have ten records in the Header Block and the record counter will read “1 of 10.” If you select Process One, AccellosOne 3PL will change the location type of record one only; if you select Process All, AccellosOne 3PL will change the location type of all ten records in the Header Block.
1 Enter ADLT.
2 Click on Location Type Block to enter the Location Type Block.
3 Key in your new location type and press Enter.
If you wish to enter a remark:
If you do NOT wish to enter a remark:
a) Enter your remarks.
b) When you finish entering your remarks, click on Return to exit the Remark Block.
a) Click on Return to exit the 
Remark Block.
NOTE If you wish to see your new location billing codes in the Renewal Block of 
LOEN, you must run the renewal preprocessor (RENW).

Adjust Location Type (ADLT) screen showing location type RACK being changed to BULK
4 Do one of the following:
5 Click on Exit to exit ADLT.

### Changing the Company Date in DATE or ALDA <a id="changing-the-company-date-in-date-or-alda"></a>

You can change the application system date for your company or companies in either DATE or ALDA. You use DATE (Change Company Date) when you wish to change the date in the company in which you are currently working; you use ALDA (Change Date for All Companies) when you wish to change the date for all companies on your system whose Default to Master Date flag in COMP has been set to Yes.
Changing the date in DATE or ALDA does not affect the Unix system date. The Unix system date is used to track the date and time of all time-stamping transactions in the Time Block of LOEN.
1 Enter DATE or ALDA.
If you wish to change the location type of the currently selected record in the Header 
Block:
If you wish to change the location type of ALL records in the Header Block:
a) Click on Process One. a) Click on Process All.

SYSTEM ADMINISTRATION GUIDE 4.2* 161

Change Company Date (DATE) screen
2 In the Next Business Day field, key in your new company date and press Enter.
3 Click on Commit.
4 Click on Exit to exit.

### Recalculating Inventory Expiry Dates in REEX <a id="recalculating-inventory-expiry-dates-in-reex"></a>

This program allows you to recalculate the expiry dates of existing inventory after changing your shelf life duration and/or frequency in ITSH (Item Shipping Profile). For example, if you currently calculate the expiry date by adding six months to the production date (inventory level 3) and wish to change this formula to the production date plus eight months, you must run REEX if you wish to apply the change to existing inventory. 
If you change your shelf life duration and/or frequency in ITSH but do not run REEX, your new formula will apply to new inventory only — not existing inventory — and allocation may not pick in correct FIFO/LIFO sequence. 
When recalculating expiry dates, you can exempt from recalculation those items using the current company date as their expiry date in ITSH. You do so by setting the For Items Using Company Date Recalculate the 
Expiry Date with New Company Date (Y/N) field to N for No. If you set this field to Y for Yes, all items including those using the current company date as their expiry date will have their expiry dates recalculated.
When you run REEX, AccellosOne 3PL creates an IF (Information Only) record in the History Block of LOEN for inventory whose expiry date formula was changed. The IF record shows both the original expiry date and the recalculated expiry date.

1 Enter REEX.

Reset Inventory Expiry Date (REEX) screen
2 Key in your customer code and press Enter.
3 If required, key in your item code and press Enter.
4 In the For Items Using Company Date Recalculate the Expiry Date With New Company Date (Y/N) field, press Enter to accept the default value of N for No (recommended) or key in Y for Yes and press Enter.

Reset Inventory Expiry Date (REEX) screen
5 Click on Update Date.
6 Click on Yes when prompted to proceed with update.
7 Do one of the following:
If you wish to add a remark:
If you do NOT wish to add a remark:
a) Key in your remarks.
b) When you finish entering your remarks, click on Return.
a) Click on Return.

SYSTEM ADMINISTRATION GUIDE 4.2* 163
8 Click on Exit to exit.

### Performing Advanced Queries with SQL Statements <a id="performing-advanced-queries-with-sql-statements"></a>

The bind variable “:A” allows you to perform advanced queries on most query fields in AccellosOne 3PL. An advanced query makes it possible to use parameters such as greater than, less than, not equal to, like or any other SQL command in your queries. 
The following list shows some of the more common SQL commands that you can use in a query. If you are querying in an alphanumeric field, you must use single quotes for the query value.
Advanced queries can only be performed on unformatted database fields. An unformatted database field is a field whose value directly corresponds to a column in a database table. For example, the Customer Code field in LORE (Look Up Receipts) is a database field because CUST_CODE is a column in the E_RCPT_H table.
If you wish to perform an advanced query on a date field, the following requirements must be met:
COMMAND DESCRIPTION
> Greater than
< Less than 
!= Not equal to 
= Equal to 
BETWEEN Between
Example
Enter “BETWEEN 123 and 456” to show all receipts in LORE between receipts 123 and 456.
LIKE When used with the wildcard (%) character, this command allows you to query on individual characters in a code or value. For example, if you enter %A, 
AccellosOne 3PL will retrieve all codes ending in the letter A. If you enter A%, 
AccellosOne 3PL will retrieve all codes starting with the letter A. 
Example
Enter “LIKE ‘A&’” to show all codes starting with the letter ‘A’.
NOT LIKE Similar to the “LIKE” command.
Example
Enter “NOT LIKE ‘&01’” to show all codes that do not end with the numbers 
‘01’.

 you must enter the date in the Oracle date format (the AccellosOne 3PL date format is not valid
 you must enter your query in a non-date field and you must use the actual database column name (for example, ORD_CONF_DATE)
1 Enter the program in which you wish to perform the query.
2 Make sure that you are in query mode.
3 Key in :A in the field that you wish to query.

LORE screen showing the bind variable in the Customer Code field
4 Click on Execute Query.
5 In the Query Where window, key in :A followed by your query statement.

SYSTEM ADMINISTRATION GUIDE 4.2* 165

LORE screen showing a receipt query for all receipts in which the customer code does not equal A 
6 Click OK to execute it.
7 When you finish performing your query, click on Exit to exit.

### PERFORMING QUERIES ON MULTIPLE FIELDS <a id="performing-queries-on-multiple-fields"></a>

If you wish to perform SQL queries on two or more fields, use :A for the first field, :B for the second field and so on and so forth.

LOOR screen showing a query on two fields: Customer and Carrier

LOOR screen showing query for customer code equals A and carrier code equals ABC

SYSTEM ADMINISTRATION GUIDE 4.2* 167

### Looking Up Spooler Activity in LOSP <a id="looking-up-spooler-activity-in-losp"></a>

Every time that you print or auto-print a document or report, AccellosOne 3PL creates a file in the print spooler. You can look up these files in LOSP (Look Up Spooler Activity) and print them to a PC printer at any time.
Each file in the print spooler is assigned a five-digit system-generated sequence number. Unless you manually delete them, files remain in the print spooler for the number of days for purge retention that you define in SPPA (Spool Parameters).
1 Enter LOSP. 
2 When you finish entering your search criteria, click on Execute Query to query the report or document that you wish to access. 

Look Up Spooler Activity (LOSP) screen showing files in the print spooler
3 Use your arrow keys to locate the report or document that you wish to access, then press Enter to position your cursor in the Action column. 
4 Key in V for View and press Enter. 
5 Click on Process to process.
NOTE If you set your printer to NONE or VIEW, the report or document will not be sent to the spooler and you will be unable to access it in LOSP.

AccellosOne 3PL will display the document or report that you selected in step 5. You can use the Edit/
Find on this page command to search for the information that you require.
6 If you wish to print the report or document, select File/Print and select the appropriate PC printer. Then click on Print to print.
7 When you finish viewing and/or printing the file, select File/Close to close the window. 
8 Click on Return to Main and Exit to exit.

### LOOKING UP FAX INFORMATION <a id="looking-up-fax-information"></a>

If a file has been faxed, you can look up the faxing information in the Process Block.
1 Enter LOSP.
2 Key in your search criteria and press Enter.
3 Click on Execute Query to query the reports or documents that you wish to look up.
4 Use your arrow keys to locate the report or document that you wish to access, then press Enter to position your cursor in the Action column. 
5 Click on Fax Information.

Look Up Spooler Activity (LOSP) screen showing fax information in Process Block
6 When you finish looking up your fax information, click on Exit and Return to Main. Then click on Exit again to exit.

SYSTEM ADMINISTRATION GUIDE 4.2* 169

### Setting Up Sort Sequence Codes in SOSE <a id="setting-up-sort-sequence-codes-in-sose"></a>

Sort sequence codes allow you to customize the sort sequence of certain lists in AccellosOne 3PL such as the physical inventory tickets that you create in PHTI and the cycle count tickets that you create in CYGT. 
They are currently used a number of programs including ENPH (Enter Physical Parameters), CYEN (Create 
Cycle Count), MRFP (RF Profile Code) and PSPR (RF Substitution Profile Code).
If you do not use sort sequence codes, these lists will be sorted in ascending alphanumeric order; for example, 101, 102, 103, 104.
SOSE supports any valid SQL statement that can follow an “order by” command; since the “order by” clause is automatically added to your statement, it should not be entered in SOSE.
If you know SQL, you can create your own sort sequence codes and attach them to the appropriate program. 
If you do not know SQL, you can contact HighJump for assistance.
1 Enter SOSE.
2 Click on Create Record.
3 Key in your sort sequence code and press Enter.
4 Key in a description for your new code and press Enter.
5 Key in your sequence formula and press tab.
6 Click on Return to Main to exit create record mode.
NOTE SOSE does not check the validity of your SQL statement. If your statement is invalid, you will get an error message when running the program that your sort sequence code is attached to.

SOSE screen showing sort sequence code for sorting location codes in descending order
7 Click on Exit to exit SOSE.
8 Attach your new SOSE code to the appropriate program.

### Looking Up Your Warehouse Utilization in LOWU <a id="looking-up-your-warehouse-utilization-in-lowu"></a>

This program shows the total capacity of each warehouse, the actual number of pallets, cases or other SKU type in the warehouse and the amount of free space as a percentage of the total capacity. Also shown are utilization values for “Today”, “Tomorrow” and “Next Day”.
For each warehouse, you can enter LOLO (Look Up Location Information) and look up capacity information for each location.
The utilization values are calculated as follows:
Utilization % the total on-hand quantity grouped by SKU class for all locations in the warehouse/the total capacity for all locations in the warehouse 
* 100

SYSTEM ADMINISTRATION GUIDE 4.2* 171
1 Enter LOWU.

Enter Query screen
2 Key in your search criteria. You can query by building code, warehouse code, isolator code, location type code or any combination of these search criteria. 
3 When you finish entering your search criteria, click on Execute Query .
Today the actual capacity for “Today” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt date = today
 the total of all non-confirmed R-type order location lines with a to ship date = today
This sum is divided by total capacity of the warehouse and then multiplied by 100 to arrive at today’s utilization.
Tomorrow the actual capacity for “Tomorrow” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt date = today + 1
 the total of all non-confirmed R-type order location lines with a to ship date = today + 1
This sum is divided by total capacity of the warehouse and then multiplied by 100 to arrive at tomorrow’s utilization.
Next Day the actual capacity for “Next Day” is the sum of:
 the total of all non-confirmed receipt location lines with a receipt date = today + 2
 the total of all non-confirmed R-type order location lines with a to ship date = today + 2
This sum is divided by total capacity of the warehouse and then multiplied by 100 to arrive at the next day’s utilization.

Look Up Warehouse Utilization screen showing utilization information for warehouse 1
4 If you wish to look up capacity information for individual locations within a warehouse, use your arrow keys to position the cursor beside the warehouse that you wish to look up and click on Drill Down to 
Locations .

SYSTEM ADMINISTRATION GUIDE 4.2* 173

Look Up Warehouse Utilization screen showing LOLO
5 Proceed to look up your location in LOLO in the normal manner.
6 When you finish looking up your location information, click on Exit to exit LOLO.
7 Click on Exit to exit LOWU.

### Looking Up Your Warehouse Activity in SAM <a id="looking-up-your-warehouse-activity-in-sam"></a>

This program allows you to look up all activity in your warehouse. It shows all inbound receipts, outbound orders, relocations, CRM’s, appointments and outbound loads for the date range that you specify. For outbound and appointment activity, you can specify which date to use (to ship date, to arrive date, etc.) when specifying a date range. For inbound and outbound load activity, the date used in the date range fields cannot be changed.

SAM also shows all current operator activity: that is, each operator currently signed on to AccellosOne 3PL.
TAB DESCRIPTION
Inbound Activity For each receipt, SAM shows the receipt number, level 1 value, number of units, weight, number of pallets, priority number, flow code, warehouse/location, operator code and receipt date.
If the receipt has been deleted, the number of units will be shown as zero.
You can restrict your inbound activity query to show only late or in process receipts. A receipt is considered “late” if the receipt date is less than the current date. A receipt is considered “in process” if the receipt date equals the current date or falls in the future.
Outbound Activity For each order, SAM shows the order number, level 1 value, number of units, weight, number of pallets, priority number, flow code, warehouse/location, operator code and to ship date.
If the order has been deleted, the number of units will be shown as zero.
You can restrict your outbound activity query to show only late or in process orders. An order is considered “late” if the to ship date is less than the current date. An order is considered “in process” if the to ship date equals the current date or falls in the future.
Outbound Loads For each load, SAM shows the load number, the date and time that the load was created, the load’s status, the carrier, the external load number, the building and door, the number of units, the gross and net weight, and the percentage loaded.
If the load has been deleted, the number of units will be shown as zero.
You can restrict your outbound load activity query to show only late or in process loads. A load is considered “late” if the load creation date is less than the current date. A load is considered “in process” if the load creation date equals the current date or falls in the future.
Inventory Activity For each relocation, SAM shows the adjustment number, level 1 value, number of units, number of pallets, status, warehouse/location, operator code and transaction date.
CRM For each CRM, SAM shows the CRM number, customer code, assigned to operator, status, CRM code, date, type and operator.

SYSTEM ADMINISTRATION GUIDE 4.2* 175
1 Enter SAM.

Query window
Appointment For each appointment, SAM shows the appointment number, date, building and door, carrier, whether the appointment is inbound or outbound, document number, load type, number of units, number of pallets and gross weight.
You can restrict your appointment query to show only late appointments. An appointment is considered “late” if the appointment arrival date is later than the appointment start date.
Operator Activity SAM shows each operator currently working in AccellosOne 3PL, the program that the operator is working in and whether or not the program is an RF program.
TAB DESCRIPTION

2 Do one of the following:
3 When you finish entering your search criteria, click on Execute Query .

Supervisory Activity Management screen (SAM) showing inbound activity
4 If you wish to see activity for each line of a given receipt, click on the Receipt/Lines button of the receipt that you wish to look up. When you finish looking up your receipt lines, you can click this button again to toggle back to receipt summary view.
If you wish to enter your search criteria manually:
If you wish to run a personal query:
a) Key in your search criteria. You can query by date range, receipt number, order number, appointment number, CRM number, customer code, item code, operator code, consignee code, carrier code and shipper code. 
b) If you wish to restrict your query to inbound activity, outbound activity, relocation activity, etc., deselect the appropriate check boxes to exclude the activities that you do not wish to see. 
When you deselect an activity, the corresponding tab on query results screen is greyed out.
a) Select your personal query from the My Queries dropdown list.

SYSTEM ADMINISTRATION GUIDE 4.2* 177
You can also perform queries within the Inbound tab by means of the Enter Query and Execute 
Query commands.
5 If the Appointment tab is active, click on it to see your appointment activity.

SAM screen showing appointment activity
6 You can perform queries within the Appointment tab by means of the Enter Query and Execute Query commands.
7 If the CRM tab is active, click on it to see your CRM activity.

SAM screen showing CRM activity

8 You can perform queries within the CRM tab by means of the Enter Query and Execute Query commands.
9 If the Outbound tab is active, click on it to see your outbound activity.

SAM screen showing outbound activity
10 If you wish to see activity for each line of a given order, click on the Order/Lines button of the order that you wish to look up. When you finish looking up your order lines, you can click this button again to toggle back to order summary view.
You can also perform queries within the Outbound tab by means of the Enter Query and Execute Query commands.
11 If the Inventory tab is active, click on it to see your relocation activity.

SYSTEM ADMINISTRATION GUIDE 4.2* 179

SAM screen showing relocation activity
12 If the Outbound Loads tab is activated, click on it to see your outbound load activity.

SAM screen showing outbound load activity
13 You can perform queries within the Outbound Loads tab by means of the Enter Query and 
Execute Query commands.
14 If the Operator Activity tab is active, click on it to see your operator activity.

SAM screen showing operators activity
15 You can perform queries within the Operator Activity tab by means of the Enter Query and 
Execute Query commands.
16 When you finish looking up your warehouse activity, click on Exit to exit SAM.

### LOOKING UP SUMMARY INFORMATION IN SAM <a id="looking-up-summary-information-in-sam"></a>

The Summary window in SAM shows summary information for receipts, orders, CRM’s, relocations and replenishments. The summary information shown is always based on the main or non-summary query.
1 Enter SAM.
2 Enter your search criteria and click on Execute Query.
3 When AccellosOne 3PL retrieves your query results, click on Summary.

SAM screen showing Summary window
4 Click on Return to exit.

SYSTEM ADMINISTRATION GUIDE 4.2* 181

### Working With the Translation Manager in TRMA <a id="working-with-the-translation-manager-in-trma"></a>

The Translation Manager is a powerful field label and message management system that allows you to customize field labels, hint lines, system codes, error messages, menu names, button text and any other text appearing in the AccellosOne 3PL suite of products. The field labels, system codes and error messages that you manage in the Translation Manager apply to ActiveDesktop, AccellosOne 3PL, Standard Reports, eVista, d’Amigo and RF.
There are two update modes in TRMA: single entity update and mass update. In single entity mode, you update individual field labels, system code, button text, etc. one record at a time. In mass update mode, you update all instances of a field label, system code, button text, etc. in a single step.

TRMA query screen
FIELD DESCRIPTIONS (QUERY MODE)
Language Code The language that you wish to update. The update language need not be the same as the query language. For example, you can query by standard text (that is, English) and update Spanish.
Mass Update If you select this option, AccellosOne 3PL will retrieve a single record representing all instances of your search term and any changes that you make will apply to all instances. If you leave this option blank, AccellosOne 3PL will retrieve one record for each instance of your search term and you will have to update each record individually.

Application Code ActiveDesktop
All field labels and error messages used in ActiveDesktop.
Documents
Order and receipt documents set up in DOCU and printed from PROM, 
PROR, PRRE and PRRM.
Dynamic Forms
A dynamic form is a form in which all the field names and dropdown lists are stored in the database rather than in the program. Dynamic forms are used in a small number of maintain programs such MRFP, VOPC and VOPR.
Menus
The name of your menus as set up in JOSE (Job Selection Code).
Messages
All hint lines, pop-up messages, button text and block names used in static forms.
RF
All field labels, system prompts and error messages used in RF.
RF Loading Programs
All field labels, system prompts and error messages used in the RF loading programs.
Static Forms
All field labels used in static forms and standard reports. Static forms represent the vast majority of forms in AccellosOne 3PL. Also includes the output of standard reports.
System Codes
The codes that users select from dropdown and pick lists.
d’Amigo
All field labels, system prompts and error messages used in d’Amigo.
e-Vista
All field labels, system prompts and error messages used in e-Vista. Any changes to e-Vista field labels, system prompts and error messages must be activated in e-Vista before you can see them on your screen.
FIELD DESCRIPTIONS (QUERY MODE)

SYSTEM ADMINISTRATION GUIDE 4.2* 183

### UPDATING A SINGLE ENTITY <a id="updating-a-single-entity"></a>

You update a single entity by leaving the Mass Update checkbox blank. if a single entity has multiple records in TRMA, you will have to update each record individually.
1 Enter TRMA.
2 Select your language code from the dropdown list.
3 If required, select your application code from the dropdown list.
4 If you selected Dynamic Forms, Static Forms or RF as your application code, you can select the appropriate entity code from the dropdown list. If you selected Menus as your application code, you can enter the appropriate JOSE code or message number in the Label Code field.
Entity Code Only useful for Static and Dynamic Forms and RF
The name of the program containing the field label. For example, ENRE, 
CUST, ITEM, etc.
Label Code Only useful when the application code = Menus or Messages. For example, if you enter ENRE, you can change ENRE’s description.
Label Sub-Code For HighJump use only.
Standard Text The standard text word or phrase that you are searching for. If you do not know the full word or phrase, you can use the wildcard character (“%”) to represent the unknown letters or words.
Standard text is in English only and is set up and maintained by HighJump. 
You cannot change standard text. However, you can query by standard text and them make your change to the corresponding language text.
Match Case If you select this option, the case of each letter must match in query. If you do not select this option, the Translation Manager ignores case when performing a query.
Language Text The language text word or phrase that you are searching for. If you do not know the full word or phrase, you can use the wildcard character (“%”) to represent the unknown letters or words.
Language text belongs to a language set up in LANG. You can modify language text at any time and your changes will be seen by all users assigned that language in OPER.
Match Case If you select this option, the case of each letter must match in query. If you do not select this option, the Translation Manager ignores case when performing a query.
FIELD DESCRIPTIONS (QUERY MODE)

5 Do one of the following:
6 If your query is case sensitive, click on the appropriate Match Case checkbox.

TRMA screen showing query for “item code”
7 Click on Execute Query.

TRMA screen showing 78 records in the Header Block containing the word “Item Code”
If you are searching for standard text:
If you are searching for language text:
a) In the Standard Text field, key in the word or phrase that you are searching for.* 
a) In the Language Text field, key in the word or phrase that you are searching for.* 
* If you are not sure of the exact word or phrase, you can use the wildcard character 
(“%”) to represent unknown or missing letters or words.

SYSTEM ADMINISTRATION GUIDE 4.2* 185
8 Click in the Header Block.
9 Use your Up and Down arrow keys to scroll through the list of records in the Header Block.
10 When you reach the record that you wish to change, click in the blank field below and key in your change. If the message is a multi-line message, click on Ctrl + E to enter the Text Editor. Then key in your changes and click Ok to confirm or Cancel to exit without saving your changes.

TRMA screen showing the editing of a multi-line message

TRMA screen showing “Product Code” as the new label for “Item Code” in the program PIIT
11 When you finish making your changes, click on Save.
12 Click on Exit to exit.

### PERFORMING A MASS UPDATE <a id="performing-a-mass-update"></a>

The Mass Update function allows you to update all instances of a field label, system code, button text, etc. in a single step. For example, if you wish to change “Item Code” to “Product Code” in the dozens of programs that this label appears in, you would use the Mass Update function.
When you perform a mass update, TRMA displays the number of labels that will be updated. Also displayed is the Multiple Labels checkbox. If this checkbox is selected, there have been manual overrides to the label that you wish to change and your changes will overwrite them. For example, “Item Code” has already been changed to “Product Code” or some other value in one or more programs and these changes will be lost when you perform your mass update.
1 Enter TRMA.
2 Select your language code from the dropdown list.
3 Click on Mass Update.
4 If required, select your application code from the dropdown list.
5 If you selected Dynamic Forms, Static Forms or RF as your application code, you can select the appropriate entity code from the dropdown list. If you selected Menus as your application code, you can enter the appropriate JOSE code in the Label Code field.
6 Do one of the following:
7 If your query is case sensitive, click on the appropriate Match Case checkbox.
8 Click on Execute Query.

TRMA screen showing seven records for “ITEM CODE” and 79 records for “Item Code”
9 Click in the blank field below the record that you wish to change and key in your changes.
10 When you finish making your changes, click on Save.
11 Click on Exit to exit.
If you are searching for standard text:
If you are searching for language text:
a) In the Standard Text field, key in the word or phrase that you are searching for.* 
a) In the Language Text field, key in the word or phrase that you are searching for.* 
* If you are not sure of the exact word or phrase, you can use the wildcard character 
(“%”) to represent unknown or missing letters or words.

SYSTEM ADMINISTRATION GUIDE 4.2* 187

### Copying Codes Between Companies in COCO <a id="copying-codes-between-companies-in-coco"></a>

This program allows you to copy setup codes and profiles from one company to another. Using COCO it is easy to duplicate your setups for testing purposes and to set up new companies/facilities with the assurance that a given customer in a new facility will have the same billing, allocation and item setup that the customer had in the old facility. 
When you copy a code or profile, any dependencies for that code or profile are automatically copied as well even if you did not select them in COCO. For example, if you copy CUST, all the dependencies of CUST such as DBIP, FLPR, DILP, etc. will be copied as well even if you did not select them and even if they are deactivated profiles.
If you explicitly select a code or profile in COCO, it will only be copied if it is active. The following restrictions apply to COCO:
1 Enter COCO.
PROGRAM RESTRICTIONS
DLVP customer and item details are not copied
DOOR warehouse and locations are not copied
ILOP Mandatory warehouse and locations codes defined in LOCA are copied to the new company. If the location format in the new company differs from the location format in the old company, these copied location codes will require manual adjustment.
IRHP customer and item details are not copied
MRFP warehouse and locations are not copied
LOCA Mandatory warehouse and locations codes defined in LOCA are copied to the new company. If the location format in the new company differs from the location format in the old company, these copied location codes will require manual adjustment.
RATE All rates are copied. If there are any non-.ALL rates in your from company, the customers attached to those non-.ALL rates as well as all the customer’s items and any other dependencies are copied too.
See the Billing and Invoicing Guide for further information on the Use Current 
Effective Date of From Customer (RATE) checkbox.

COCO screen
2 Select your from company from the dropdown list.
3 Select your to company from the dropdown list.
4 Click on the code and profile that you wish to copy. To select multiple codes and profiles, press and hold the Ctrl key while you make your selection. To select a range of codes and profiles, click on the first item in the range. Then press and hold the shift key before clicking on the last item in the range.

SYSTEM ADMINISTRATION GUIDE 4.2* 189

COCO screen showing six selections
5 When you finish making your selections, click on Process.
6 When prompted to confirm the copy, click on Yes.
7 Click on Yes again to acknowledge the “Copy done” message.
8 Click on Exit to exit.

### Performing a Mass Update of an Item Value in IMAS <a id="performing-a-mass-update-of-an-item-value-in-imas"></a>

You can perform a mass update of an item’s item value in IMAS. You select the items to be updated by alternate inventory reporting type and alternate inventory reporting code defined in ITAS (Item Alternate 
Sorts).
1 Enter IMAS.

IMAS screen
2 Select your alternate inventory reporting type from the dropdown list.
3 Select your alternate inventory reporting code from the dropdown list.
4 Key in your new item value.
IMAS screen showing all items assigned the alternate inventory reporting type/code of MEAT/BEEF
5 Click on Process .
6 When prompted to proceed with the update, click on Yes.
7 Click on Exit to exit.

### Importing Orders and Receipts in IFFI <a id="importing-orders-and-receipts-in-iffi"></a>

You can import orders and receipts from CSV files in IFFI.
1 Place the files to be uploaded into the $DEL4_HOME/del4/work/faxlp directory on the Linux server.
2 Enter IFFI.

SYSTEM ADMINISTRATION GUIDE 4.2* 191
IFFI screen
3 Select your file conversion type from the dropdown list.
4 Select your customer from the dropdown list.
5 Key in your file name and click on Process .
6 If the import fails for any reason, click on Yes to acknowledge the error message.

SYSTEM ADMINISTRATION GUIDE 4.2* 193
