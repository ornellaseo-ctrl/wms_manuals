---
title: "Faturamento — Baixa de Pagamentos e Relatórios"
description: "Cash posting, contas a receber, cross-reference de clientes e relatórios de faturamento."
layout: default
---

# Faturamento — Baixa de Pagamentos e Relatórios

Cash posting, contas a receber, cross-reference de clientes e relatórios de faturamento.

**Fluxo principal:** `CHPO/ARCP (baixa) -> CUCR (cross-ref) -> BIRR/CICR/CRPR (relatorios)`

> Fonte: manuais A do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Cash Posting System <a id="cash-posting-system"></a>

*Manual A — Billing and Invoicing*

### Overview <a id="overview"></a>

The cash posting system allows you to track payments received from your customers and apply these payments to specific invoices. You can apply a payment to one or more invoices, you can receive payment from one customer and apply the payment to another customer and you can run aging reports to show the age of various outstanding accounts.
The cash posting system is linked to the Credit Limit field in DBIP. If you set the Check Credit Limit field to Y for Yes and if the total of all outstanding invoices for a given customer exceeds the customer’s credit limit, you will not be able to create an order for that customer in ENOR.
There are a maximum of four steps to follow when processing a cash payment:

### Setting Up Your Bank in BANK <a id="setting-up-your-bank-in-bank"></a>

If you wish to track the bank and account number when posting payments in CHPO, you must set up a bank and account number in BANK. You need one record in BANK for each bank account that you post to in 
CHPO.
1 Enter BANK.
2 Click on Create Record.
3 Key in your bank code and press Enter.
ARCP
CHPO
CHPO
In CHPO (Check Posting), you assign the payment to a batch.
When you close the batch in CHPO, all the payments on the batch are final and cannot be modified or reversed.
If required, you can run various reports to track your cash payments: CRPR (Cash/
Check Posting Report), ARAR (Accounts 
Receivable Aging Report) and INPR (Invoice Payment Report). 
You enter your payments in ARCP (Check/
Cash Entry). 

4 Key in a description for your new bank code and press Enter.
5 Key in your bank account number and press Enter.
6 Select the appropriate GL account from the dropdown list.
7 Select the appropriate currency from the dropdown list.
8 When you finish setting up your bank, click on Return to Main to exit create record mode.

BANK screen
9 Click on Exit to exit.

### Setting Up Customer Cross References in CUCR <a id="setting-up-customer-cross-references-in-cucr"></a>

Customer cross references allow you to apply a payment to a customer other than the customer issuing the check. For example, suppose you have four accounts: COLA_1, COLA_2, COLA_3 and COLA_4. You receive a check from COLA_1 and you wish to apply a portion of the check to an invoice from COLA_2, a second portion of the check to an invoice from COLA_3 and the remainder of the check to an invoice from 
COLA_4.
You set up customer cross references in CUCR by creating one record for each cross reference. For example, if COLA_1 can pay invoices belonging to COLA_2, COLA_3 and COLA_4, you would set up three records in CUCR:
COLA_1 --> COLA_2 (invoice customer)
COLA_1 --> COLA_3 (invoice customer)
COLA_1 --> COLA_4 (invoice customer)
If the payment customer in your warehouse always equals the invoice customer (that is, you do not apply a payment from one customer to another customer), you do NOT set up customer cross references in CUCR.

1 Enter CUCR.

CUCR screen
2 Click on New.
3 Select your payment customer from the Customer Code pick list.
4 Select the corresponding invoice customer from the Invoice Customer Code pick list.
5 Repeat the above two steps for each additional payment customer/invoice customer relationship that you wish to set up.
6 When you finish setting up your customer cross references, click on Save to save your changes.

CUCR screen showing five customer cross references
7 Click on Exit to exit.

### REMOVING A CROSS REFERENCE <a id="removing-a-cross-reference"></a>

1 Enter CUCR.
2 Select the record in CUCR that you wish to delete.
3 Click on Delete.
4 When prompted to confirm the deletion, click on Yes.
5 Click on Exit to exit.

### Entering a Payment in ARCP <a id="entering-a-payment-in-arcp"></a>

You enter your payments in ARCP (Cash/Check Entry). You can enter both invoice payments and non-invoice payments in ARCP. An invoice payment is a payment related to a specific invoice, while a non-invoice payment is money unrelated to a specific invoice that is placed into an account for future use.
There is a one-to-many relationship between payments and checks. That means that you can apply a single check to as many invoices that the check will pay. You can also enter partial payments; for example, instead of paying one invoice in full, you can partially pay three invoices from one check.
1 Enter ARCP.

ARCP screen
2 Click on New.
3 Key in your customer code and press Enter.
4 Key in the check number and press Enter.
5 Key in your posting date and press Enter or select your posting date from the pop-up calendar.
6 Key in the amount of the check being received and press Enter.
7 If required, select a new currency from the Currency dropdown list.
8 If required, you can add miscellaneous remarks to the payment by clicking on Remarks. After entering your remarks, click on Save to save them or click on Return to exit without saving.

ARCP screen showing check for $100 from customer A
9 In the Detail Block, key in your invoice number and press Enter or select your invoice from pick list. You select an invoice from the pick list by clicking on pick list or pressing F10. When the pick list displays, click on invoice(s) that you wish to select. You can click on Select All to select all invoices or 
 Deselect All to deselect all your selections. When you finish making your selections, click on 
Accept to save them.
AccellosOne 3PL will populate the Entered Amount field with the invoice amount — if the check amount matches or exceeds the invoice amount. You can enter a partial payment by manually keying an amount less than the full invoice amount.
10 If required, you can add miscellaneous remarks to the invoice by clicking on Remarks. After entering your remarks, click on Save to save them or click on Return to exit without saving.
11 If a portion of the check is not being applied to an invoice, key in the non-invoice amount in the NonInvoice Amount field.

ARCP screen showing payments applies to three invoices
12 Repeat the above steps for each additional invoice that you want to pay.
13 When you finish adding your invoices, click on Save to save your changes.
14 Click on Exit to exit.

### DELETING A PAYMENT <a id="deleting-a-payment"></a>

When you delete a payment in ARCP, any invoices linked to the payment are removed from the Invoice Detail 
Block and the payment is deactivated. Deleting a payment is final and cannot be reversed.
1 Enter ARCP.
2 Retrieve the payment that you wish to reverse.
3 Click on Delete.
4 When prompted to confirm the deletion, click on Yes.
5 Click on Exit to exit.

### REMOVING AN INVOICE FROM A PAYMENT <a id="removing-an-invoice-from-a-payment"></a>

When you remove an invoice from a payment, the invoice is considered to be unpaid and once again will appear in the pick list of unpaid invoices in the Invoice Detail Block of ARCP.
1 Enter ARCP.
2 Retrieve the payment that you wish to modify.
3 Select the invoice that you wish to remove.

4 Click on Delete.
5 When prompted to confirm the deletion, click on Yes.
6 Click on Exit to exit.

### UNDERSTANDING THE CHECK, POSTED AND REMAINING AMOUNTS <a id="understanding-the-check-posted-and-remaining-amounts"></a>

There are four amounts in the Header Block of ARCP: the check amount, the non-invoice amount, the posted amount and the remaining amount. The check amount and the non-invoice amount are entered by the operator, while the posted and remaining amounts are system-calculated.
A payment is considered balanced if the check amount equals the invoice amount plus the non-invoice amount.

ARCP screen showing unbalanced payment
Check Amount the amount of the payment as entered by the operator
Non-Invoice Amount the portion of the payment as entered by the operator that is not applied to any invoice
Posted Amount the sum of all entered amounts in the Invoice Detail Block; that is, the total amount applied to all invoices
Remaining Amount the difference between the check amount and posted amount; that is, check amount - non-invoice amount - posted amount = remaining amount 

### LOOKING UP SUMMARY INFORMATION <a id="looking-up-summary-information"></a>

The Summary box in ARCP shows the total number of checks entered on a given date, the total check amount, the total posted amount and the difference (if any). The Summary as of date used in ARCP is the system date when the checks were entered — not the check entry date.

ARCP screen showing Summary box

### Posting a Payment in CHPO <a id="posting-a-payment-in-chpo"></a>

You post a payment in CHPO by assigning the payment to a batch containing similar payments; for example, all payments received from a certain customer or all payments received between a certain date range. As long as the batch remains active, you can add payments to it and remove payments from it. However, once the batch is closed, all payments in the batch are final and cannot be modified or reversed.
There are two tabs in CHPO: the Posted Checks tab and the Unposted Checks tab. The Posted Checks tab shows all payments assigned to a particular batch. The Unposted Checks tab shows all unposted payments that meet the customer and from/to date selection criteria that you enter in the Batch Block of CHPO.
When you post a payment, the check is moved from the Unposted Checks tab to the Posted Checks tab of the appropriate batch.
1 Enter CHPO.
TIP Before posting your payments, it is advisable to run the CRPR report to make sure that all payments have been correctly entered.

CHPO screen
2 Select the customer whose payments you wish to post from the dropdown list or select .ALL for all customers.
3 If required, select your bank from the dropdown list.
4 If required, key in your batch date and press Enter. If you do not enter a batch date, AccellosOne 3PL will use the current date. 
5 Click on Save. AccellosOne 3PL will create a batch number for the new batch and populate the 
Batch Date field with the current date (if you did not manually enter a batch date in the previous step).

CHPO screen showing new batch number for .ALL customer
6 Select your from and to dates from the pop-up calendars. Only payments received between these two dates will be included in the batch.
7 When you finish entering your selection criteria, click on Execute Query. If prompted to save your changes, click on Yes. AccellosOne 3PL will retrieve all unposted checks that meet the criteria that you specified.

CHPO screen showing all unposted checks received between the from and to dates that you specified
8 Proceed to select the checks from the Unposted Checks tab that you wish to post to the batch. You can select checks manually by clicking in the checkbox beside each check or you can click on Select All to select all checks or Deselect All to deselect all your selections. You can also manually deselect a selected check by clicking on the appropriate checkbox.
9 When you finish selecting your checks, click on Save. AccellosOne 3PL will move the selected checks from the Unposted Checks tab to the Posted Checks tab.
10 Click on Exit twice to exit.

### REMOVING PAYMENTS FROM A BATCH <a id="removing-payments-from-a-batch"></a>

When you remove payments from a batch, AccellosOne 3PL moves the payments from the Posted Checks tab to the Unposted Checks tab.
1 Enter CHPO.
2 Retrieve the batch containing the payments that you wish to remove.
3 Click on the Posted Checks tab.

CHPO screen showing Posted Checks tab
4 Proceed to select the checks that you wish to remove. You can select checks manually by clicking in the checkbox beside each check or you can click on Select All to select all checks or Deselect All to deselect all your selections. You can also manually deselect a selected check by clicking on the appropriate checkbox.
5 Click on Save to move the payments from the Posted Checks tab to the Unposted Checks tab.
6 Click on Exit twice to exit.

### DELETING A BATCH <a id="deleting-a-batch"></a>

All posted checks on a batch must be removed before you can delete the batch.
1 Enter CHPO.
2 Retrieve the batch that you wish to delete.
3 Make sure that there are no posted checks on the batch.
4 Click on Delete. The status of the batch will change to “Deleted”.
5 Click on Exit twice to exit.

### CLOSING A BATCH <a id="closing-a-batch"></a>

When you close a batch in CHPO, all the payments on the batch are final and cannot be modified or reversed. 
Posted payments can no longer be accessed in ARCP.
1 Enter CHPO.
2 Retrieve the batch that you wish to close.

3 Click on the Close Batch checkbox to select it.
4 Click on Save.

### PRINTING THE BATCH AUDIT <a id="printing-the-batch-audit"></a>

For each check reported on, the batch audit shows the customer code, check number, entry date, check amount, batch date, batch status, remarks and the AccellosOne 3PL operator who entered the check.
For each invoice that the check was applied to, the Cash/Check Posting Report shows the invoice prefix, invoice number, the invoice type, the invoice amount, the paid amount and remarks.
1 Enter CHPO.
2 Retrieve the batch that you wish to print.
3 Click on Print Report.

### Reports <a id="reports"></a>

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

## Reports And Reference <a id="reports-and-reference"></a>

*Manual A — Billing and Invoicing*

### Reports <a id="reports"></a>

See the Standard Reports Guide.

### BILB (Accessorial Invoicing) <a id="bilb-accessorial-invoicing"></a>

You use this program to generate and print accessorial bill later invoices. The type of charges that appear on these invoices depend on the invoicing option — IND, UALL, UREC or UREN — that you specify in DBIP (Depositor Billing Profile).

FIELD DESCRIPTIONS
Batch Type Accessorial
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).

Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Generation
The batch failed to generate successfully or was changed and will have to be regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been printed.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, no charge created after this date will be included. Second, if AccellosOne 3PL is linked to your accounting system, the Create Date will be the posting date for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.
FIELD DESCRIPTIONS

### BILB (Renewal Invoicing) <a id="bilb-renewal-invoicing"></a>

You use this program to generate and print renewal batches and invoices. 

Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to generate successfully. 
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

FIELD DESCRIPTIONS
Batch Type Renewal
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Confirmation
The batch failed to generate successfully or was changed and will have to be regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been printed to a printer or to screen.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, no charge created after this date will be included. Second, if AccellosOne 3PL is linked to your accounting system, the Create Date will be the posting date for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.

### BILB (Immediate Invoice Invoicing) <a id="bilb-immediate-invoice-invoicing"></a>

You use this program to generate and print accessorial bill immediate invoices. 

Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to generate successfully. 
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

Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated.
Begun Generation
The batch failed to generate successfully or was changed and will have to be regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been printed.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, no charge created after this date will be included. Second, if AccellosOne 3PL is linked to your accounting system, the Create Date will be the posting date for your warehouse revenue.
Last Audit Number The number of times that the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.
Batch The batch number.
Total Entries The number of charges on the batch.
FIELD DESCRIPTIONS

### ENAC (Bill Later - Enter Charges) <a id="enac-bill-later-enter-charges"></a>

The program is used as a bucket to hold charges generated or entered in ENRE, ENOR and BILB. It holds all charges except immediate accessorial charges. You use ENAC to modify or delete charges before confirming and printing your invoice. You can also enter charges directly in ENAC if the receipt or order is already confirmed or if the charge is unrelated to a specific receipt or order.
Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to generate successfully. 
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

FIELD DESCRIPTIONS
Accessorial Entry NumberThis number is system generated.
Bill-To Code The customer who is to be billed for the charge
Department Code Only available if activated in COMP (Company Parameters)
Address 1/2/3 Address information retrieved from customer record set up in CUST.
City/ZIP Code City and ZIP code information retrieved from customer record set up in CUST.

Date to Charge If you enter ENAC through ENRE or ENOR, this field displays the system date and cannot be edited. If you enter ENAC in stand-alone mode, you can modify this field.
For renewal charges, this field shows the date the product renews.
If you enter a date restriction in the Select Block of BILB, a charge may be dropped from the batch based on its Date to Charge date.
If AccellosOne 3PL is linked to your accounting system, the Date to Charge date does not determine the posting date of the charge in your accounting system. The system uses the date the batch was created (the Create Date in 
BILB) as the posting date. 
Reference Description A free format field for internal purposes that does not print on the invoice. If the charge is a renewal storage charge, the renewal date will be shown. If the charge is an extra charge, the following will appear:
EXIN Batch <999> where the number in brackets is the extra charge batch number. If the number in brackets is negative, this indicates that the extra charge was entered through the receipt rater.
Reference Number If you enter ENAC through ENRE or ENOR, the reference number is generated by the system based on the receipt or order number plus type of charge. 
EXAMPLES
Receipt WR - 15 (Initial storage for receipt 15)
Rec 18 (accessorial charge at the header level for receipt 18)
Rec 20 line 3 (accessorial charge for line 3 of receipt 20)
EXIN on WR:190 (extra charge on receipt 190)
Remarks Y = Yes
N = No
If you enter Y for Yes, the Remark Block will be displayed and you can add a remark to the charge. 
Charge Code The charge code for the charge.
Tax Code The tax code for the charge code. This field is only enterable if tax code overrides are activated for the charge code in CHAR.
Location Bill Code The location billing code for the charge.
FIELD DESCRIPTIONS

The following fields are query fields only and do not display when you retrieve a record. 
Qualifying Quantity The quantity you are charging for.
Charge Quantity Display field only.
Rate The rate for this charge.
Total The total for this charge.
FIELD DESCRIPTIONS
Accessorial Batch NumberThe accessorial batch on which the charge was placed. If the charge was deleted, never placed on a batch or is a renewal charge, the value in this field will be zero.
Renewal Batch Number The renewal batch on which the charge was generated. If the charge was deleted, never placed on a batch or is an accessorial charge, the value in this field will be zero.
Source Reference Flag A = Maximum/minimum charges charged when the actual charge is less than the minimum charge or greater than the maximum charge.
E = Extra charges generated automatically in GEXC or ECHP.
F = Freight charges created in A1 Transport.
I = Insurance charges attached to BILB.
O = Order charges entered in ENOR.
R = Receipt charges entered in ENRE or generated automatically in IISP or 
IHAP.
S = Accessorial charges entered through ENAC.
X = Renewal charges created when a renewal batch is generated.
Source Reference NumberThe receipt or order number for the charge (if any).
Source Reference Line 
Number
The line number of the receipt or order for the charge (if any).
Inventory Customer Code The “bill-to” customer code for the charge.
FIELD DESCRIPTIONS

### ENIN (Enter Immediate Invoice) <a id="enin-enter-immediate-invoice"></a>

You use this program to enter immediate accessorial charges.
Inventory Level 1/2/3 If the charge is related to a specific receipt or order, the level 1 and 2 values for the item.
Current Renewal Date For renewal charges only, the product’s last renewal date.
Next Renewal Date For renewal charges only, the product’s next renewal date.
Entered Quantity For unit-based SKU’s, the quantity expressed in the largest SKU type (for example, 1 pallet 40 cases).
Quantity For unit-based SKU’s, the quantity expressed in the smallest SKU type (for example, 100 cases).
Weight Measure Code For unit-based SKU’s, the unit of measure for the weight of the product.
Weight The gross weight of the product.
Net Weight The net weight of product.
Linear Measurement 
Code
For unit-based SKU’s, the unit of measure for the cube of the product.
Cube The cube of the product.
FIELD DESCRIPTIONS

FIELD DESCRIPTIONS
Invoice Number This number is system generated.
Bill-To Code The customer who is to be billed for the charge
Address 1/2/3 Address information retrieved from customer record set up in CUST.
City/ZIP Code City and ZIP code information retrieved from customer record set up in CUST.
Invoice Date If you enter a date restriction in the Select Block of BILB, a charge may be dropped from the batch based on its invoice date.
If AccellosOne 3PL is linked to your accounting system, the invoice date does not determine the posting date of the charge in your accounting system. The system uses the date the batch was created (Create Date in BILB) as the posting date. 
Charge Code The charge code for this charge.
Reference Description A free format field for internal purposes that does not print on the invoice. 

### BILB (Extra Charge Invoicing) <a id="bilb-extra-charge-invoicing"></a>

You use this program to generate accessorial extra charges that have been set up in ECHP (Extra Charge 
Profile) or GEXC (General Extra Charges) and attached to a customer, item, consignee or carrier. If you enter a receipt extra charge manually in ENRE, you do not use this program.

Tax Code The customer’s tax code. This field is only enterable if tax code overrides are activated in CHAR.
Rmk. Y = Yes
N = No
If you enter Y for Yes, the Remark Block will be displayed and you can add a remark to the charge. Remarks are for internal purposes only and do not print on any invoice.
Qualifying Quantity The quantity that you are charging for.
Charge Quantity Display field only.
Rate The rate for this charge.
Total The total for this charge.
FIELD DESCRIPTIONS

FIELD DESCRIPTIONS
Batch Type Extra Order/Receipt Rater
Batch Number This number is system generated.
Attention If you select a name from the dropdown list, it will print on the invoice as an 
Attention To line above the customer’s address. Attention to names are set up in CUSE (Customer Service Representatives).
Status Deleted
The batch has been deleted. When you delete a batch, all charges on it are released and will be picked up on the next batch that you generate. 
Generated
The batch has been generated. If you encounter a status message during generation, the status of the batch will read “Generated” but in reality the batch will not be completely generated and you will have to regenerate it before you can confirm it. The purpose of the “Generated” status is to allow you to print a partial audit report.
Begun Generation
The batch failed to generate successfully or was changed and will have to be regenerated.
Printed
The batch has been generated and an audit report has been printed.
Confirmed
The batch has been generated and confirmed and an invoice has been printed to a printer or to screen.
Description Your description for the batch (for example, “Customer 1”, “All Customers”, etc.).
Create Date This date serves two functions. First, it is the cut-off date for the batch; that is, no charge created after this date will be included. Second, if AccellosOne 3PL is linked to your accounting system, the Create Date will be the posting date for your warehouse revenue.
Last Audit Number The number of times the batch has been printed.
Control Total Reserved for future use.
Entered Total Reserved for future use.

### ADBD (Adjust Billing Data) <a id="adbd-adjust-billing-data"></a>

You use this adjustment program to make changes to your renewal storage charges for existing inventory in your warehouse. You can change the next and last renewal dates, the billing profile code set up in IBIP and the rate for renewal storage.
Batch The batch number.
Total Entries The number of charges on the batch.
Selection REGN (Regenerate)
You use this command to regenerate a batch that was changed or failed to generate successfully.
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

FIELD DESCRIPTIONS
Customer Code The customer whose billing date you wish to adjust.
Item The item whose billing data you wish to adjust.
Period Number The current renewal period.
Alternate Billing Group The customer’s alternate billing group (if any).
Inventory Customer Code The inventory customer when billing subscription is set up and billing records have been created.
Next Renewal Date The product’s next renewal date.
Last Renewal Date The product’s last renewal date.

Base Renewal Date Only used when switching from fixed date renewals to anniversary date renewals
The date that the product was originally received. If you have changed your renewal billing frequency from a fixed date renewal (weekly as of Monday, monthly first of the month, monthly last of the month) to an anniversary renewal (anniversary monthly, anniversary weekly, daily), you may have to adjust this date to make sure that the base renewal date matches the next renewal date.
EXAMPLE — Switch from monthly first of month to anniversary monthly on 
06.10.09 (June 10, 2009)
Next Renewal Date = 06.10.09
Last Renewal Date = 05.01.09
Base Renewal Date = 01.25.09
In the above example, you must change your base renewal date from 
01.25.09 (the date that the product was originally received) to 06.10.09 so that the next renewal date and the base renewal date match.
Discount Profile Code The product’s discount profile code, if any.
Billing Profile Code The product’s billing profile code.
Next Renewal Invoice 
Date
The system-calculated next renewal invoice date. This field is only populated if Number of Days Between Renewal Invoices field in DBIP is set to a value greater than zero.
You should consult with your HighJump 3PL support before you manually override this date as it could affect the future renewal invoice date.
Last Renewal Invoice 
Date
The last renewal invoice date. This field is only populated if Number of Days 
Between Renewal Invoices field in DBIP is set to a value greater than zero.
BILLING DETAIL BLOCK
Location Bill Code The product’s location billing code (display field only).
FIELD DESCRIPTIONS

### LOIN (Look Up Invoices) <a id="loin-look-up-invoices"></a>

You use this program to look up your invoices. A batch must have a status of confirmed before you can look up the invoice in LOIN.

Rate The new rate for renewal storage that will be charged the next time the product renews.
This option is only available if you selected the option R for Renewal Original in the Original or Current Rate on Renewals field in DBIP.
Qualifier Quantity/Weight/
Net Weight/Cube
The qualifier quantity for the new rate. This value is generated by the system.
FIELD DESCRIPTIONS
Invoice Number The invoice number or receipt number.
Invoice Prefix Defined in DONU (Document Numbers).
BILLING DETAIL BLOCK

### LOAC (Look Up Accessorial) <a id="loac-look-up-accessorial"></a>

You use this program to look up all accessorial bill later charges for a given item or level 2/3/4 value. LOAC shows the following information about a charge:
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
Payment Amount If you use the cash posting system, the total of all payments made for this invoice.
Rollup Company Code If you use rollup invoicing, the rollup company code.
Rollup Invoice Number If you use rollup invoicing, the rollup invoice number.
Rollup Invoice Prefix Defined in DONU (Document Numbers).
FIELD DESCRIPTIONS

Records in LOAC are permanent and cannot be deleted except through the program PURA (Purge Accessorial Batch).

FIELD DESCRIPTIONS (HEADER BLOCK)
Customer Code The customer whose charges you wish to look up.
Level 1 The item whose charges you wish to look up.
Level 2/3/4 The level 2/3/4 entity that you wish to look up.
ACCESSORIAL BLOCK
Accessorial Number The accessorial entry number for the charge.
Date The date that the charge was created.

Remarks N = No
Y = Yes
If you entered a remark when you created the accessorial charge, this flag will be set to Y for Yes. If you did not enter a remark when you created the accessorial charge, this flag will be set to N for No.
You can view remarks in LOAC by positioning your cursor in the Remark field and pressing F3 to view the Remarks Block.
Charge Code The charge code for the charge.
Amount The amount of the charge.
Invoice Prefix Invoice prefixes are defined in DONU (Document Numbers).
Invoice Number If the charge has been invoiced, the number of the invoice will appear in this field. If the charge has NOT been invoiced, the following will occur:
 if the charge is associated with a confirmed receipt or order, the receipt or order number will appear
 if the charge is associated with an unconfirmed receipt or order, this field will be blank
 if the charge is confirmed but is not associated with a specific receipt or order (for example, a renewal charge), the number 1 will appear
Total Invoiced The total for invoiced charges. A charge is considered invoiced if the receipt or order associated with the charge has been confirmed.
Total Unbilled The total for unbilled charges. A charge is considered unbilled if the receipt or order associated with the charge has NOT been confirmed.
Total The total invoiced plus the total unbilled.
ACCESSORIAL BLOCK

DETAIL BLOCK
Entered by For manual charges, the operator who entered the charge. For automatic charges, the operator who confirmed the receipt or order.
Audited by If you use accessorial authorization, the operator who authorized the charge.
Source Type Accessorial Entry
Freight
Order
Receipt
Renewal
The type of charge.
Document Number The charge’s receipt or order number. If there is no receipt or order associated with the charge, the document number will be zero. 
Line Number The charge’s receipt or order line number. The line number will be zero in the following cases:
 there is no receipt or order associated with the charge
 the charge was applied to the order or receipt header — not the line

### Troubleshooting Billing and Invoicing <a id="troubleshooting-billing-and-invoicing"></a>

THE RENEWAL DATES OR QUANTITIES IN THE RENEWAL BLOCK OF LOEN ARE 
WRONG
The information in the Renewal Block is not updated in real-time and may show out-of-date information. In the majority of cases, running the renewal preprocessor (RENW) will update the billing information in LOEN. 

### THE RATES SHOWN ON MY INVOICE ARE WRONG <a id="the-rates-shown-on-my-invoice-are-wrong"></a>

If you are using a multi-break charge code, the rate of the charge appearing on the invoice will be averaged. 
For example, if your rate for the first 1,000 lbs. is .60 and for the next 500 lbs. is .50, the rate on an invoice for a receipt of 1,500 lbs. would be .57 (the total charges divided by the total weight).
If you enter a charge code in the Default Rate Charge Code field in CHAR (for example, charge code X has charge code Y as its default rate charge code), charge code X will use charge code Y’s rates. Any rates that you enter for charge code X in RATE will be ignored by the system. 

### THE CHARGES ARE WRONG (WEIGHT-BASED BILLING ONLY) <a id="the-charges-are-wrong-weight-based-billing-only"></a>

If the charges are wrong for weight-based billing, check the item’s weight. An incorrect weight will lead to incorrect charges. You can correct the weight of an item in RESW (Recalculate Standard Weight) or WEAD (Weight Adjustment).
Confirmed N = No
Y = Yes
If the charge was entered when processing a receipt or order and this receipt or order has not been confirmed, this flag will be set to No. In all other cases, this flag will be set to Yes.
Location Bill Code The location billing code for the charge.
SKU Code Qualifier The qualifying SKU code for the charge.
Qualifying Quantity The quantity for qualifying purposes.
SKU Code Charge The charging SKU code for the charge.
Charge Quantity The quantity for charging purposes.
Rate The charge’s rate.
Amount The total amount of the charge.
DETAIL BLOCK

### THERE ARE MISSING CHARGES ON MY AUDIT REPORT OR INVOICE <a id="there-are-missing-charges-on-my-audit-report-or-invoice"></a>

Zero charges do not appear on audit reports and invoices. Look up the quantity and rate for the charge in 
ENAC. If either the quantity or rate of the charge is zero, the charge total will be zero too.
The SKU type that you qualify on and charge on in CHAR must match the SKU type of all items to which the charge applies. For example, you cannot set up a pallet-based charge code in CHAR and attach it to an item whose quantity breakdown is cases only. If you do, the charge quantity will be zero and no charge will be generated.

### NO CHARGES GENERATED FOR A CONFIRMED RECEIPT <a id="no-charges-generated-for-a-confirmed-receipt"></a>

The receipt is confirmed but not rated. Rate the receipt in RCRA (Receipt Rater).

A
ACAL (Accessorial Charges Audit Look-Up) 222
ACAU (Accessorial Authorization) 225
ACCA (Accessorial Charge Changes Report) 222 accessorial audit, printing 148 accessorial batches confirming 149 entering restrictions 61, 145, 152, 157, 204 accessorial bill immediate charges 198 accessorial bill later charges 180 adding to a confirmed order 192 entering in ENAC 190 overview 6 splitting out by means of invoice types 178 accessorial invoice, generating and printing 144 changing other parameters 50 changing renewal storage dates 50 changing renewal storage rates 48 overview and field descriptions 268 allocating costs to an invoice 237 alternate billing groups 93
ARCP (Cash/Check Entry) 243 audit batch restrictions in BILB 160 automatic pre-renewal billing 127
B backdating open orders and receipts 178
BANK (Bank Code) 240 batches deleting 169 looking up charges on 169 modifying a charge on 172 regenerating 169 reprinting 169 troubleshooting 172 overview and field descriptions 254 using 144
BILB (Daily Invoice Register) 163 overview and field descriptions 266 using 155 overview and field descriptions 258 using 203 overview and field descriptions 256 using 150 authorizing your charges 223 changing and deleting charges 219 overview 216 purging change records in PACA 226 setting up 217 tracking changes to ENAC and ENIN charges 221 billing by warehouse 227 billing entities, overview 22
Billing Entity Minimum Charge Code field (IBIP) 19 billing setup programs 10 billing subscription 91 billing/invoicing cycle, overview 8
Bill-To Code field, using 90
Breakdown Number field (INRE) 13
BTCS (Billing Subscription) 91 cancelling a rate change 32 closing a batch in CHPO 250 entering a payment in ARCP 243 overview 240 posting a payment in CHPO 247 printing the audit batch 251 setup 240
CDAV (Daily Average for Customer) 36
CDMX (Customer Daily Maximum) 42

changing renewal storage rates 48 charges deleting from a batch 171 looking up on a batch 169 missing 172 modifying on a batch 172 splitting out 178 charging by physical pallet 81 check-in only billing 35
CHGR (Charge Group) 28
CHPO (Check Posting) 247
CLOL (Close Open Lots) 99 closing open lots 99
COD extra charge 55
Column field (INRE) 13 combination type charges 88 confirming accessorial batches 149 extra charges 84, 159 renewal batches 155 costs, allocating to an invoice 237 credits, entering in ENAC 196 credits, entering in ENIN 201
CRIN (Credit Invoice) 236 cross-docking billing 108
CUCR (Customer Cross Reference) 241
CUDE (Customer Departments) 198
CUFC (Customer Fixed Charges) 123
CURX (Currency Exchange Rates) 124, 125 customer departments 198 customer fixed charges 123
D daily average billing 36
Daily Invoice Register (BILB) 163
DECH (Density Charge Codes) 118 deleting batches 169 deleting charges from a batch 171
DELO (Depositor Load Type Charges) 94
Density Charge Codes (DECH) 118 density rating 118
Description Bottom field (INRE) 13
Description field (INRE) 13
Description Top field (INRE) 13 discounts on initial storage and handling 104
DPRO (Discount Profile Code) 104
E
ECHP (Extra Charge Profile)
field descriptions 71 overview 54
EDEC (EDI Receipt Extra Charge) 83 emailing of confirmed invoices 168 entering a credit in 196 entering charges in 190 entering customer department in 198 looking up charges in 169 overview and field descriptions 260
ENIN (Bill Immediate - Enter Charges)
entering a credit in 201 overview and field descriptions 264 using 198 exceed daily average billing (renewal storage) 40 extra charge audit, printing 158 extra charges activating 83 assigning location billing codes to 59 charging for partial quantities 62 confirming 84, 159 for third party billing 82 generating a batch for 155 group descriptions 55 printing 158 receipt 183 specifying restrictions for 60
F flat rate charges 120
G generating a renewal batch 150 a warehouse receipt invoice 142 accessorial bill immediate charges 198 an accessorial batch 144 an extra charge batch 155
GEXC (General Extra Charges)
field descriptions 65 overview 54
H
Handling Minimum Charge Code field (IBIP) 19 hourly based charges 121
IDRA (Increase/Decrease Rates) 32 immediate accessorial audit, printing 206 immediate accessorial batch, confirming 207 immediate accessorial batch, generating 203
IND invoicing 132, 133
Initial Storage Minimum Charge Code field (IBIP) 19
INRE (Invoice Register Definition) 12 inventory levels, invoicing by 234
Invoice Breakdown Code field (INRE) 13 invoice only customer 90 invoice register definition (INRE), setting up 12 invoice types in BILB 178 invoices allocating costs to 237 emailing 168 looking up 173 printing 174 reprinting 169 invoicing by inventory level 234 invoicing by warehouse 227
