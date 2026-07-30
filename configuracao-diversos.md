---
title: "Configuração — Códigos Diversos"
description: "Transportadoras, motoristas, países, moedas, feriados, séries numéricas e demais códigos base."
layout: default
---

# Configuração — Códigos Diversos

Transportadoras, motoristas, países, moedas, feriados, séries numéricas e demais códigos base.

**Fluxo principal:** `CARR/DRIV -> CNTY/STPR/ZIPO -> CURR/CURX -> NUSE/DONU`

> Fonte: manuais N do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Miscellaneous Setup <a id="miscellaneous-setup"></a>

*Manual N — Setup Guide*

### Adjustment Type Codes (ADJU) <a id="adjustment-type-codes-adju"></a>

OVERVIEW
In this program, you set up your adjustment type codes. Adjustment type codes are required when you make adjustments to inventory in programs such as ENAJ (Enter Inventory Adjustment), MATR (Massive 
Adjustment) and ENPH (Enter Physical Parameters). These codes specify the type of adjustment; for example, aged product, damaged goods, lost inventory, customer returns, receipt correction, other, etc.
You will need one adjustment type code for each type of adjustment to inventory that you make in your warehouse.
In this program, the following items require definition:
▪ the adjustment code and its description
▪ the reason for the adjustment
▪ the document to be printed whenever an adjustment is made using this adjustment type
▪ whether there any charges associated with the adjustment and whether the current or original date is used for such charges
▪ whether a product’s receipt date changes during an adjustment
▪ the adjustment’s EDI status
The following adjustment type codes are system codes and cannot be modified or deleted: CY (Cycle Count 
Adjustment), HL (Hold Adjustment), IF (Information Only Adjustment), RL (Relocate) and WGT (Weight 
Adjustment).
PREREQUISITES: one document set up in DOCU with a document type of ADJ
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all the reasons why you make adjustments to your inventory
FIELD DESCRIPTIONS
Adjustment Code Mandatory
Your adjustment code. For example, AGED for Aged Product.

Description Mandatory
Your adjustment code description.
Adjustment Analysis 
Description
EXTRNL = External
The adjustment is the result of a customer-related error.
INTNL = Internal
The adjustment is the result of a warehouse-related error.
OTHER = Other
The adjustment is the result of neither a customer-related error nor a warehouse-related error.
Document Code (DOCU) Mandatory
This field allows you to specify a custom document or report that you can print to track your adjustments. Any document code that you enter requires a document type of ADJ in DOCU. If you do not have a custom document for adjustments, you must create a dummy document in DOCU to populate this field.
Enter Charges Y = Yes
N = No
If you select Yes, you will be prompted to enter charges when making an adjustment with this adjustment type. You must select Yes if you intend to charge for this adjustment type.
If there is no charge for this adjustment type, select No.
Effective Date for 
Charges
Only available if Enter Charges = Yes
C = Current
O = Original
If you select Original, the charges for this adjustment type that were in effect the day the product was received will apply. If you select Current, current charges for this adjustment type will apply. 
FIELD DESCRIPTIONS

PROCEDURE
1 Enter ADJU.
2 Click on Enter Criteria then Execute Query to see whether the adjustment types that you require have already been set up. If you need to set up a new adjustment type, click on Create Record.
3 Key in your adjustment code and press Enter.
4 Key in a meaningful description for your adjustment code (for example, Damaged Goods or Lost Inventory) and press Enter.
5 Use your pick list to select the appropriate adjustment analysis description. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
6 Use your pick list to select the appropriate document code for the document or report that you wish to print whenever this adjustment type is made.
7 In the Enter Charges field, key in Y for Yes or N for No and press Enter.
8 In the Effective Date for Charges field, key in O for Original or C for Current and press Enter.
9 In the Date Used for Adjustments / Renewals field, key in O for Original or C for Current and press Enter.
10 In the Send via EDI field, key in Y for Yes or N for No and press Enter.
Date Used for Adjustments / RenewalsC = Current
O = Original
If you select Original, the product to which you are applying this adjustment type will retain its original received date and will renew on that date. If you select Current, the product to which you are applying this adjustment type will be assigned the current date as its received date and will renew on the day that the adjustment was made.
Send via EDI Y = Yes
N = No
Set to Yes if the customer has a need to see the adjustment, the adjustment is recorded on a document or report and the only way the customer can get that document or report is through EDI.
FIELD DESCRIPTIONS

Adjustment Type Codes
11 Repeat the above steps for each additional adjustment type that you wish to add to ADJU.
12 When you finish entering your adjustment codes, click on Return to Main and then Exit to exit.

### Load Type (LOAD) <a id="load-type-load"></a>

OVERVIEW
In this program, you set up your load types. Load types serve four functions in AccellosOne 3PL:
▪ you can use them to apply extra charges such as sorting, freezing, stencilling, unloading, etc. that you incur when receiving or shipping a load 
PREREQUISITES: SKCL
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

▪ you can use them for reporting purposes only to describe the types of loads entering and leaving your warehouse (for example, palletized load, floor-loaded product, slip-sheeted load, etc.)
▪ you can use them in the appointment system to define the number of minutes required to load or unload a given quantity of a given load type
▪ you can use them to define the number of temperatures readings required
You assign a load type to a load in ENRE (for inbounds) and ENOR (for outbounds). If you do not require load types for your warehouse, use AccellosOne 3PL load type called NA (Not Applicable).
FIELD DESCRIPTIONS
Load Type Code Mandatory
Your load type code. For example, FL for Floor Loading.
Description Mandatory
Your load type description.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Num of Temperatures In this field, you define the number of different temperatures readings by load type required for each receipt that you enter in RFCH. 
You can enter any number between 0 and 6 in this field. The number zero indicates no restrictions, while any number between 1 and 6 indicates the exact number of temperatures required in RFCH. 
If you specify a non-zero value in this field and the number of temperature readings that you enter in RFCH does not match this value, the temperature(s) will be rejected and an error message will display.
Inb. Fixed Minutes See the “Appointment Planner” section in the Operations 2 Guide.
Outb. Fixed Minutes See the “Appointment Planner” section in the Operations 2 Guide.
Override Pick Method to 
EACH
All Pick Methods
Case Pick Method Only
No CART Pick Method
Pallet Pick Method Only
In this field, you can override a pick method to EACH. 

PROCEDURE
1 Enter LOAD.
2 Click on Enter Criteria then Execute Query to see whether the load types that you require have already been set up. If you need to set up a new load type, click on Create Record.
3 Key in your load type code and press Enter.
4 Key in a meaningful description for your load type code and press Enter.
5 Press Enter to bypass the Labor Standard Modifier field.
6 If required, key in the number of temperatures required for this load type and press Enter. If you do not require an exact number of temperatures, leave this field blank.
7 If required, key in the number of fixed minutes for inbound appointments for this load type and press 
Enter. If you do not require a number of fixed minutes for inbound appointments, leave this field blank.
8 If required, key in the number of fixed minutes for outbound appointments for this load type and press 
Enter. If you do not require a number of fixed minutes for outbound appointments, leave this field blank.
9 If required, select a pick method from the Override PIck Method to EACH pick list or press Enter to bypass this field.
10 If required, key in Y for Yes in the Disable Item Subst. from PL field and press Enter or press Enter with the field blank to bypass this option.
11 If required, key in Y for Yes in the Disable Count Backs field and press Enter or press Enter with the field blank to bypass this option.
Your cursor will be positioned in the Weight Block.
Disable Item Subst. from 
PL
Y = Yes
N = No
If you enter Y for Yes in this field, allocation and item substitution from pickline type locations will be deactivated for orders assigned to this load type.
Disable Count Backs Y = Yes
N = No
If you enter Y for Yes in this field, count backs in RFPIC will be deactivated for orders assigned to this load type.
WEIGHT/QUANTITY BLOCK
The fields in this block are used to define the number of minutes required to load or unload a given quantity of a given load type. See the appointment system section in the Operations 2 Guide for further information.
FIELD DESCRIPTIONS

Load Type for NA (Not Applicable)
12 Click on In/Out Block to exit create mode. Then click on Master Block and Exit to exit.

### Transport Mode Codes (TRMO) <a id="transport-mode-codes-trmo"></a>

OVERVIEW
In this program, you set up your transport mode codes. Transport mode codes describe how freight is shipped from the warehouse: by air, sea, ground or by all modes. They must be attached to carriers in CARR if you use ShippingLIVE to ship and track your outbound orders. They are also a requirement in the Transport 
Mode Block of ITEM if you wish to capture hazmat information for a given item on an outbound order.
PREREQUISITES: None
ATTACHED TO: ITEM (Item Codes)
CARR (Carriers)
GLOBAL/UNIQUE: Global
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

PROCEDURE
1 Enter TRMO.
2 Click on Enter Criteria then Execute Query to see which codes have already been set up.
3 If you need to set up another code, click on New.
4 Key in your transport mode code and press Enter.
5 Key in a description for your new code and press Enter.
6 If required, key in a reference for your new code.
7 Select the appropriate transport mode type from the dropdown list.
8 Repeat the above four steps for each additional transport mode code that you wish to add.
FIELD DESCRIPTIONS
Code Mandatory
Your transport mode code.
Description Mandatory
Your transport mode description.
Reference Optional
Miscellaneous reference information about your transport mode.
Transport Mode Type All Modes
Ground
Air
Sea
Your transport mode type.

Transport Mode Codes
9 When you finish adding your transport mode codes, click on Save to save your changes.
10 Click on Exit to exit the program.

### Carriers (CARR) <a id="carriers-carr"></a>

OVERVIEW
In this program, you set up your commonly used carriers. You set up the name and address of the carrier, the carrier’s Standard Carrier Alpha Code, whether or not the carrier will be used to carry loads generated through AccellosOne Transport and the message (optional) that you want to print automatically on the carrier’s bill of lading.
The carriers that you create in CARR are attached to loads in ENRE (for inbound loads) and ENOR (for outbound loads). If you do not have any commonly used carriers, it is possible to bypass the Carrier fields in 
ENRE and ENOR.
PREREQUISITES: MESS, TETP
ATTACHED TO: CUST (Customer Setup)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all your commonly used carriers

FIELD DESCRIPTIONS
Carrier Code Mandatory
Your carrier code. A carrier code can consist of any combination of numbers or letters up to 10 characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.
Name Mandatory
The name of your carrier.
Address 1/2/3/4 Mandatory
The address of the carrier
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (Zip/Postal Code), the city, state/province and country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Standard Carrier Alpha 
Code
Mandatory
If the carrier has a predefined SCAC code, enter it in this field. If the carrier does not have a SCAC code, use X to bypass this field.

Weight Measure I = Imperial
M = Metric
The carrier’s weight measure. This weight measure prints on the bill of lading or other shipping document and need not be the same as the item’s weight measure in ITEM. 
External Carrier Flag Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL orders assigned to this carrier will be accessible to a second freight interface. If you set this flag to N for 
No, AccellosOne 3PL orders assigned to this carrier will NOT be accessible to a second freight interface.
Freight Interface Type 
Code
FRT = Freight Interface 
A common carrier who picks up consolidated loads generated through AccellosOne Transport.
NFR = No Freight Interface
A common carrier who carries regular inbound and outbound loads processed in ENRE and ENOR.
Freight Pay Carrier Code (CARR)
Reserved for future use.
Freight Type Code (FRTY)
Only available if Carrier Type Code = FRT
The freight type as defined by US regulatory authorities.
Freight Mileage Rate Reserved for future use.
Freight Minimum PaymentReserved for future use.
Freight Discount PercentageReserved for future use.
Carrier Type Code CPU = Customer Pick-Up
The customer delivers and picks up his own product and does not use a common carrier.
This field is set up by HighJump.
FIELD DESCRIPTIONS

Generated Number Profile CodeReserved for future use.
Transport Mode Code (TRMO)
A transport mode code is needed for ShippingLIVE. It is also a requirement in the Transport Mode Block of ITEM if you wish to capture hazmat information for a given item on an outbound order.
B/L Message Code (MESS)
Optional
The message that you enter here will print on the carrier’s bill of lading.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
SKU Class for Number of 
Labels
Only available for BarTender labels and ShippingLIVE
The SKU class that you enter here overrides the default SKU class defined in 
DOCU (Documents). 
Rounding Method for 
Number of Labels
Only available for BarTender labels and ShippingLIVE
U = Up
D = Down
The Rounding Method that you enter here overrides the default rounding method defined in DOCU (Documents). 
Isolator Code (ISOL) Reserved for future use
Allow Banding Reserved for future use
Compliant Label 
Required
Reserved for future use
EDI Required Flag Reserved for future use
A1 Ship Service The carrier’s A1 Ship service.
FIELD DESCRIPTIONS

INSURANCE BLOCK
The information in this block is for informational purposes only and not used in any other AccellosOne 3PL program.
PROCEDURE
1 Enter CARR.
2 Click on Create Record.
3 Key in your carrier code and press Enter.
4 Key in the name of your new carrier and press Enter.
5 Key in the address of the carrier, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the carrier’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into CARR with the appropriate information filled in.
7 If the carrier has a predefined SCAC code, enter it in this field and press Enter. If the carrier does not have a SCAC code, key in X and press Enter to bypass this field.
8 Key in your carrier’s weight measure (I for Imperial or M for Metric) and press Enter.
9 If required, key in Y for Yes or N for No in the External Carrier Required field and press Enter.
Yard Location Profile 
Code
Reserved for future use
FIELD DESCRIPTIONS
Policy Code The carrier’s policy number.
Description A description of this policy.
Deductible The policy’s deductible.
From Date The date that insurance coverage starts. The format of this date must match the date format in COMP (Company Code).
To Date The date that insurance coverage ends. The format of this date must match the date format in COMP (Company Code).
FIELD DESCRIPTIONS

10 Use your pick list to select the appropriate carrier type code for this carrier. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 

Carrier screen showing prompt for generated number profile
11 Press Enter to bypass the Generated Number Profile Code field.
12 If required, key in your transport mode code in the Transport Mode Code field and press Enter. If your carrier does not require a transport mode code, press Enter to bypass this field.
13 In the B/L Message Code field, you can specify a standard message to print on the carrier’s bill of lading. 
If such a message is required, use your pick list to select the appropriate message code.
14 Press Enter the required number of times to bypass the Extra Charge Profile Code, Labor Standard Modifier, SKU Class for Number of Labels, Isolator Code and Yard Location Profile Code fields.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax numbers and e-mail addresses for this carrier if you choose to do so or you can leave this block blank 
If you enter FRT for Freight: If you enter any other code:
a) Enter the appropriate values in the Freight Pay Carrier Code and 
Freight Type Code fields.
b) Enter the appropriate value in the Freight Type Code field.
c) Press Enter to bypass the 
Freight Mileage Rate, Freight 
Minimum Payment and Freight 
Discount Percentage fields.
a) Proceed to next step.

and not use it. If you do not want to use the Telephone Block at this time, click on Return to Main. Then proceed to step 13. 
15 In the Code field, use your pick list to select the appropriate telephone type. Then key in the telephone number and press Enter. Next key in your contact name for this carrier and press Enter followed by the contact’s position (press Enter again).
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

Telephone Block in CARR
CARR also contains a Motor Carrier Block and an Insurance Block. The Motor Carrier Block is reserved for future use. The Insurance Block allows you to record a carrier’s policy number, deductible and period of coverage.
16 If you wish to record insurance information for the carrier, click on Motor Carrier Block and then Insurance Block to enter the Insurance Block. If you do not wish to set up these blocks at this time, proceed to step 20.
17 Key in the carrier’s policy number and press Enter.
18 Key in a description for this policy and press Enter.
19 Key in the amount of the deductible for the policy and press Enter.
20 Key in the date that insurance coverage starts and press Enter.
21 Key in the date that the insurance coverage ends and press Enter.

Carrier screen showing Insurance Block
22 When you finish entering your insurance information, click on Return to Main to exit create mode. 
23 Click on Master Block and Exit to exit.

### Load Analysis (LDAN) <a id="load-analysis-ldan"></a>

OVERVIEW
In this program, you set up your load analysis codes. You use these codes to track the types of loads that you receive from shippers (inbounds) and the types of loads that you ship to consignees (outbounds). For inbound loads, load analysis codes are reserved for future use and you should use the system load analysis code called NA (Not Applicable) for your shippers.
For outbound loads, load analysis codes are a restriction in Wave Manager; that is, you can filter the orders in a wave by load analysis code. For example, you could assign load analysis codes to consignees by region — 
NE for North-East, SW for South-West, MW for Mid-West, etc. — and filter your waves by consignee region.
PREREQUISITES: None
ATTACHED TO: SHIP (Shippers)
CONS (Consignees)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

PROCEDURE
1 Enter LDAN.
2 Click on Enter Criteria then Execute Query to view your NA (Not Applicable) code.

Load Analysis Codes
3 When you finish viewing your NA code, click on Exit to exit.

### Shippers (SHIP) <a id="shippers-ship"></a>

FIELD DESCRIPTIONS
Load Analysis Code Mandatory
Your load analysis code.
Description Mandatory
Your load analysis description.
PREREQUISITES: LDAN, DIFP, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory

OVERVIEW
In this program, you set up your commonly used shippers. The shippers that you create in SHIP are attached to inbound loads in ENRE. If you do not have any commonly used shippers, it is possible to bypass the 
Shipper field in ENRE.
If the shipper is the same as the customer (that is, your customer is shipping inbound loads from his own facility), you have two options:
▪ you can set up a generic shipper called SAME for all your customers
▪ you can set up individual shippers for each customer in SHIP with the same code as the customer (with this option, the Shipper Code field in ENRE will be automatically populated when receiving product from the customer)
A generic SAME-type shipper requires the following setup in SHIP:
▪ a shipper code of SAME 
▪ a period or slash in the Address 1 field
▪ any valid ZIP code to bypass the ZIP Code field
▪ a customer code of .ALL
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
An individual shipper for each customer requires the following setup in SHIP:
▪ a shipper code that is the same as the customer code (for example, a customer code of ABC_SUP in 
CUST and a shipper code of ABC_SUP in SHIP)
▪ a complete address and valid ZIP code
▪ a customer code of .ALL
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
▪ a workflow profile code (optional)
If the shipper is not the same as the customer (that is, the inbound loads originate from a separate company), you must set up a complete SHIP record. A complete SHIP record requires the following:
▪ a valid shipper code and name
▪ a complete address and valid ZIP code
▪ the customer code 
▪ a weight measure for receipts
▪ a load analysis code
▪ a shipper type of W for Warehouse
▪ a workflow profile code (optional)
OTHER REQUIREMENTS: The names and addresses of your customers’ shippers
NOTE Do not confuse the term shipper with customer or depositor. A shipper in 
AccellosOne 3PL is always a company shipping to your warehouse — that is, the originator of an inbound shipment. The term shipper never refers to an outbound order.

FIELD DESCRIPTIONS
Shipper Code Mandatory
Your shipper code. A shipper code can consist of any combination of numbers or letters up to 10 characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.
Name Mandatory
The name of your shipper.
Address 1/2/3/4 Mandatory
The address of the shipper.
ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (Zip/Postal Code), the city, state/province and country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.

Customer Code (CUST) Mandatory
If you are using the SAME option, use .ALL. If you are setting up real shippers with names and addresses, you can attach a particular customer to a particular shipper or you can use .ALL for all customers. If you attach a particular customer to a particular shipper, only that shipper will be available when receiving product from that customer. If you use .ALL as your customer, the shipper will be available to all customers.
The customer code restrictions that you define in SHIP are subject to the operator restrictions that you set up in OPRS (Operator Restrictions). For example, if a given shipper is available to all customers but a given operator is restricted to three shippers, the operator will only see those three shippers when he or she enters a receipt in ENRE.
Weight Measure Code for 
Receipts
Mandatory
The unit of measure for this shipper (pounds, kilograms, tons, etc.). If you receive a non-standard weight item from this shipper, the weight measure that you enter in this field will override the item’s weight measure (defined in ITEM) 
when you process a receipt in ENRE.
Load Analysis Code (LDAN)
Mandatory
The load analysis code for this shipper.
Shipper Type Set to W for Warehouse.
FIELD DESCRIPTIONS

Workflow Profile Code (DIFP)
Optional
If you enter a DIFP profile in this field, it will override the DIFP profile that you attached to the customer in CUST. If you do not enter a DIFP profile in this field, the system will use the default profile specified in CUST for this shipper / customer. You use this field only if a particular shipper has unique flows or special documents that require printing.
Do not enter a DIFP profile in this field if you are setting up a SAME-type shipper.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each flow, the documents if any attached to the flow as well as any special verify programs.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Item Location Profile 
Code (ILOP)
Optional
If you enter an ILOP profile in this field, product received from this shipper will use this ILOP profile for put-away instead of the ILOP profile attached to the item that you are receiving.
External Reference Number
Optional
You can add any miscellaneous reference information about a shipper in this field.
Establishment Number Reserved for future use.
Country Code - Origin Reserved for future use.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter SHIP.
2 Click on Enter Criteria then Execute Query to see whether the shippers that you require have already been set up. If you need to set up a new shipper, click on Create Record.
3 Key in your shipper code and press Enter.
4 Key in the name of your shipper and press Enter.
5 Key in the address of the shipper, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the shipper’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet in AccellosOne 3PL, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into SHIP with the appropriate information filled in.
7 Key in your customer code and press Enter or use .ALL for all your customers.
8 In the Weight Measurement Code for Receipts field, use your pick list to select the appropriate unit of measure for this shipper. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
Master Shipper Y = Yes
N = No
If you set this flag to for Yes, you can define the shipper as a master shipper and attach non-master shippers to the shipper. A master shipper is merely a way of grouping a number of related shippers. By setting up the appropriate query in d’Amigo for your master shipper(s), you can easily track inventory activity for a group of related shippers; for example, all plants in a certain geographical area belonging to the same customer.
If you set this flag to N for No, the shipper is not a master shipper.
Attached to (SHIP) Only available if the Master Shipper flag = N for No
The master shipper that this shipper is attached to.
Suppress Inventory Attributes
Y = Yes
N = No
If you select Yes, inventory attribute capture for this shipper will be deactivated.
Last Activity Date Reserved for future use.
FIELD DESCRIPTIONS

Shipper screen showing prompt for load analysis code
9 Key in your shipper’s load analysis code and press Enter.
10 Key in W for Warehouse as your shipper type and press Enter.
11 If required, use your pick list to select the appropriate workflow profile code for this shipper. If you do not require an workflow profile code, press Enter to bypass this field.
12 Press Enter to bypass the Extra Charge Profile Code field.
13 Press Enter to bypass the Labor Standard Modifier field.

Shipper screen showing prompt for item location profile code
14 If required, key in an item location profile code for this shipper and press Enter. If no item location profile is required, press Enter with the field blank to bypass this option.
15 If required, key in your external reference number for this shipper and press Enter. If no external reference number is required, press Enter with the field blank to bypass this option.
16 Press Enter twice to bypass the Establishment Number and Country Code - Origin fields.
17 In the Shipper Code Master field, key in the appropriate value (N for No or Y for Yes) and press Enter.
18 If you entered N for No in the previous field, you can specify a master shipper for the shipper. If you wish to attach a master shipper to the shipper, key in the shipper code for the master shipper and press Enter.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax numbers and e-mail addresses for this shipper if you choose to do so or you can leave this block blank and not use it. If you do not want to use the Telephone Block at this time, click on Master Block. Then proceed to step 16. 
19 In the List Code field, use your pick list to select the appropriate telephone type. Then key in the telephone number and press Enter. Next key in your contact name for this carrier and press Enter followed by the contact’s position (press Enter again). 
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

Telephone Block in SHIP
20 Click on Master Block and then Exit to exit.

### Retail Profiles (RETP) <a id="retail-profiles-retp"></a>

OVERVIEW
In this program, you set up your retail profiles. The retail profiles that you create in RETP are attached to consignees in CONS. Retail profiles serve two functions in AccellosOne 3PL:
▪ they allow you to restrict a wave in the Wave Manager by consignee type
▪ they make it possible to report by consignee type in d’Amigo
PREREQUISITES: NONE
ATTACHED TO: CONS (Consignees)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

PROCEDURE
1 Enter RETP.
2 Click on Enter Criteria then Execute Query to see which retail profiles have already been set up.
FIELD DESCRIPTIONS
Retail Profile Code Mandatory
Your retail profile code.
Description Mandatory
Your retail profile code description.
Type Other
Repair
Store
Vendor
Warehouse
Your consignee type.
Home Delivery Reserved for future use
Re-ticketing Reserved for future use

Retail Profiles
3 If you need a new retail profile, click on New to create one.
4 Key in your retail profile code and press Enter.
5 Key in a description for your new retail profile code and press Enter.
6 Select the appropriate consignee type (Other, Repair, Store, Vendor, Warehouse) from the Type dropdown list.
7 Click on Save to save your new profile.
8 Click on Exit to exit RETP.

### Consignees (CONS) <a id="consignees-cons"></a>

OVERVIEW
In this program, you set up your commonly used consignees. The consignees that you create in CONS are attached to outbound loads in ENOR. If your customers do not have any commonly used consignees, you do not need to set up consignees in this program.
PREREQUISITES: CUST, LDAN, MESS, DIFP, PIPR, DAPC, TETP, LANG
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The names and addresses of your customers’ consignees

The main options in CONS are:
▪ the consignee’s name and address
▪ the consignee’s workflow profile (only required if the consignee has special flows or documents that differ from the customer’s flows and documents)
▪ the consignee’s picking profile (only required if the way in which you pick product for this consignee differs from the picking profile defaults; these defaults are set up at the customer level in DSRP and at the item level in ITEM)
▪ the consignee’s item location profile (only required if the way in which you pick product for this consignee differs from the default item location profile attached to the item) 
Consignees can be either customer specific or general. If a consignee is customer specific, only orders belonging to the customer that you specify can be shipped to the consignee. If a consignee is general, any order belonging to any customer can be shipped to the consignee. 
FIELD DESCRIPTIONS
Consignee Code Mandatory
Your consignee code. A consignee code can consist of any combination of numbers or letters up to 10 characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.
Name Mandatory
The name of your consignee.
Address 1/2/3/4 Mandatory
The address of your consignee.

ZIP / Postal Code (ZIPO) Mandatory
The ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (Zip/Postal Code), the city, state/province and country will be filled in by AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Language Code (LANG) Mandatory
If you have an alternate item and description set up in ALIT (Alternate Item and Language) for an item, an alternate item and description will be captured when that item is being shipped to this consignee.
Customer Code (CUST) Mandatory
You can attach a particular customer to a particular consignee or you can use 
.ALL for all customers. If you attach a particular customer to a particular consignee, only that consignee will be available when shipping orders for that customer. If you use .ALL as your customer, the consignee will be available to all customers.
The customer code restrictions that you define in CONS are subject to the operator restrictions that you set up in OPRS (Operator Restrictions). For example, if a given consignee is available to all customers but a given operator is restricted to three consignees, the operator will only see those three consignees when he or she enters an order in ENOR.
B/L Message Code (MESS)
Optional
The message that you enter here will print on the carrier’s bill of lading.
FIELD DESCRIPTIONS

Load Analysis Code (LDAN)
Mandatory
The load analysis code for this consignee.
Freight Destination Code Reserved for future use.
Freight Discount PercentageReserved for future use.
Workflow Profile Code (DIFP)
Optional
If you enter a DIFP profile in this field, it will override the DIFP profile that you attached to the customer in CUST. If you do not enter a DIFP profile in this field, AccellosOne 3PL will use the default profile specified in CUST for this consignee/customer. You use this field only if a particular consignee has unique flows or special documents that require printing.
If you click on the View Flow Chart icon , you can see a flow chart of your profile showing each flow, the documents if any attached to the flow as well as any special verify programs.
Picking Profile Code (PIPR)
Optional
If you enter a PIPR profile in this field, it will override the PIPR profiles that you attached to the consignee’s customer in DSRP and to the item in ITEM (PIPR is optional in ITEM). If you do not enter a PIPR profile in this field, AccellosOne 3PL will use the default profile specified in DSRP for this consignee/ customer — unless you specify a PIPR profile for an item and this item is being shipped to this consignee.
Priority You can filter waves in Wave Manager by consignee priority.
Day Profile Code (DAPC) Only available if you auto-print order documents
See the Operations 2 Guide for further information on day profile codes.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
FIELD DESCRIPTIONS

Retail Profile Code (RETP)
Optional
The consignee’s retail profile code.
Allow Back Orders See the back orders section in the Operations 2 Guide.
External Reference Number
Optional
You can add any miscellaneous reference information about a consignee in this field.
Item Location Profile 
Code (ILOP)
Optional
If you enter an ILOP profile code in this field, product shipped to this consignee will use this ILOP profile code for picking instead of the ILOP profile attached to the item that you are picking.
Ship Only Fully Filled 
Orders
See “Allocating Only Fully Filled Orders” in Allocation and Wave Manager.
Master Consignee Y = Yes
N = No
If you set this flag to for Yes, you can define the consignee as a master consignee and attach non-master consignees to the consignee. A master consignee is merely a way of grouping a number of related consignees. By setting up the appropriate query in d’Amigo for your master consignee(s), you can easily track inventory activity for a group of related consignees; for example, all stores in a certain geographical area belonging to the same customer.
If you set this flag to N for No, the consignee is not a master consignee.
Attached to (CONS) Only available if the Master Consignee flag = N for No
The master consignee that this consignee is attached to.
FIELD DESCRIPTIONS

Appointment Required Y = Yes
N = No
If you set this flag to Yes, an appointment is required for this consignee. If you set this flag to No, no appointment is required for this consignee. The appointments referred to in this field are appointments at the consignee’s premises — not appointments at the warehouse set up in AccellosOne 3PL’s appointment system.
External Reference Number 2/3/4
Optional
You can add any miscellaneous reference information about a consignee in these fields.
Allow Banding Reserved for future use.
Banding SKU Class (SKCL)
Reserved for future use.
Consignee Consolidation 
Type
Reserved for future use.
Pallet Code If you specify a pallet code in this field, RFPICK will validate that any pallet code entered during order picking for that consignee will match the consignee's pallet code. Pallet code validation must be activated in MRFP by setting the Enter Pallet Type flag to Yes.
Special Consignee 
Requirement
Y = Yes
N = No
If you set this flag to Yes, the consignee is marked as having a special requirement. If you set this flag to No, the consignee is considered a normal consignee with no special requirements.
Outbound Type ASN 
Reporting
Reserved for future use.
MSDS Paperwork 
Required
Reserved for future use.
Single Item Per Outbound PalletIf you set this flag to Yes, the Pallet Build engine will check this flag and restrict outbound pallets to a single item. This flag is only supported in RFITLV.
FIELD DESCRIPTIONS

CARRIER BLOCK
The Carrier Block allows you to specify your preferred carriers for each consignee. These carriers are for information purposes only and do not affect the carriers available for a particular consignee during order entry in ENOR.
SKU Class for Number of 
Labels
Only available for BarTender labels and ShippingLIVE
The SKU class that you enter here overrides the default SKU class defined in 
DOCU (Documents) and CARR (Carriers). 
Rounding Method for 
Number of Labels
Only available for BarTender labels and ShippingLIVE
U = Up
D = Down
The Rounding Method that you enter here overrides the default rounding method defined in DOCU (Documents) and CARR (Carriers). 
Maximum Weight RestrictionOnly available if weight restrictions are activated in WAPC (attribute 338)
If you enter a weight restriction and if this weight restriction is exceeded in 
OLOP for this consignee, the RF operator will not be allowed to continue loading.
Generate UCC-128 
Sequence Number
Only available for BarTender labels and ShippingLIVE
Y = Yes
N = No
If you set this flag to Y for Yes, AccellosOne 3PL will generate a UCC-128 sequence number when printing case labels for this consignee. If you set this flag to N for No, no UCC-128 sequence number will be generated when printing case labels for this consignee.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Skip Cartonization Flag See the Cartonization section in the RF Guide.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter CONS.
2 Click on Enter Criteria then Execute Query to see whether the consignees you require have already been set up. If you need to set up a new consignee, click on Create Record.
3 Key in your consignee code and press Enter.
4 Key in the name of your consignee and press Enter.
5 Key in the address of the consignee, pressing Enter at the end of each line.
6 In the ZIP / Postal Code field, key in the consignee’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet on AccellosOne 3PL, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into CONS with the appropriate information filled in.
7 In the Language Code field, use your pick list to select the appropriate language. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. 
Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
8 Key in your customer code and press Enter or use .ALL for all your customers.

Consignee screen showing prompt for B/L message code
9 In the B/L Message Code field, you can specify a standard message to print on the carrier’s bill of lading when shipping to this consignee. If such a message is required, use your pick list to select the appropriate message code. If you do not require such a message, press Enter to bypass this field.
10 Key in your load analysis code and press Enter or use your pick list to select it.

11 In the Freight Destination Code field, AccellosOne 3PL will display the ZIP or postal code that you entered in the Zip Code field. Press Enter to accept it.
12 Press Enter to bypass the Freight Discount Percent field.
13 If required, use your pick list to select the appropriate workflow profile code for this consignee.
14 If required, use your pick list to select the appropriate picking profile code for this consignee.
15 Press Enter five times to bypass the following fields: Priority, Day Profile Code, Extra Charge Profile 
Code, Retail Profile Code and Allow Back Orders.

Consignees screen showing prompt for external reference number
16 If required, key in an external reference number and press Enter. If you do not need an external reference number, press Enter to bypass this field.
17 If required, use your pick list to select the appropriate item location profile code for this consignee.
18 Press Enter to bypass the Ship Only Fully Filled Orders Field.
19 In the Consignee Code Master field, key in the appropriate value (N for No or Y for Yes) and press Enter.
20 If you entered N for No in the previous field, you can specify a master consignee for the consignee. If you wish to attach a master consignee to the consignee, key in the consignee code for the master consignee and press Enter.
21 In the Appointment Required field, key in Y for Yes or N for No and press Enter.
22 Press Enter to bypass the SKU Class for Number of Labels field.
23 Press Enter to bypass the remaining fields on your screen.
AccellosOne 3PL will display the Carrier Block.
24 Click on Telephone Block to enter the Telephone Block. The Carrier Block is reserved for future use.
AccellosOne 3PL will display the Telephone Block. You can enter contact names, telephone and fax numbers and e-mail addresses for this consignee if you choose to do so or you can leave this block blank 

and not use it. If you do not want to create a Telephone Block at this time, click on Return to Main. Then proceed to step 26. 
25 In the List Code field, use your pick list to select the appropriate telephone type. Then key in the telephone number and press Enter. Next key in your contact name for this consignee and press Enter followed by the contact’s position (press Enter again). 
If you have an additional number to enter, repeat the above step for your second number. When you finish entering your telephone numbers, click on Return to Main.

Telephone Block in CONS
26 Click on Master Block and then Exit to exit.

### Sold-To Codes (SOLD) <a id="sold-to-codes-sold"></a>

OVERVIEW
In this program, you set up your sold-to accounts. You use sold-to accounts if you wish to capture sold-to information when shipping an order to a consignee (set up in CONS). For example, if you are shipping product to a large department store, the individual store (for example, store #37) could be the consignee set up in CONS and head office, which is actually paying for the product, could be the sold-to account set up in 
SOLD. 
PREREQUISITES: CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

The sold-to accounts that you create in SOLD are attached to outbound orders in ENOR. If required, sold-to information can be printed on a bill of lading or other document; this capability must be programmed by 
HighJump.
If you do not need to capture sold-to information, create a single code on your system called SAME. For a 
SAME-type code, only the following is required:
▪ a sold-to code of SAME and a sold-to description
▪ a period or slash in the Address 1 field 
▪ any valid ZIP code to bypass the Zip Code field
▪ a customer code of .ALL
FIELD DESCRIPTIONS
Sold-To Code Mandatory
The name of your sold-to code. A sold-to code can consist of any combination of numbers or letters up to 10 characters in length. The single quote (’) and double quote (“) special characters are not valid and should never be used. 
Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. Other special characters are generally supported.
Name Mandatory
The name of your sold-to code.
Address 1/2/3/4 Mandatory
The address of your sold-to account.

ZIP / Postal Code (ZIPO) Mandatory
If you are setting up a sold-to code of SAME, enter any valid ZIP code to bypass this field.
If you are setting up a real sold-to account, enter the ZIP code or postal code of the above address. If the ZIP code or postal code is already defined in ZIPO (Zip/Postal Code), the city, state or province and country will be filled in by 
AccellosOne 3PL.
If the ZIP code or postal code that you enter is not in AccellosOne 3PL, you will have to set it up in ZIPO. You set up a ZIP/postal code in ZIPO by entering the code and then defining the country code, city and state/province to which it belongs.
City Defined in ZIPO.
State Defined in STPR.
Country Code Defined in CNTY.
Language Code (LANG) Optional
If you have an alternate item and description set up in ALIT (Alternate Item and Language) for an item, an alternate item and description will be captured when that item is being shipped to this sold-to account.
Customer Code (CUST) Mandatory
You can attach a particular customer to a particular sold-to account or you can use .ALL for all customers. Use .ALL if you are setting up a sold-to code of 
SAME. 
CAUTION If you are setting up a real sold-to account and if you have given your customers operations access to AccellosOne 3PL, do not use the 
.ALL option. Instead, assign a specific customer to each sold-to account. If you use the .ALL option, each of your customers will be able to see the sold-to accounts of all your other customers when entering an order in ENOR. 
Reference 1/2 Optional
You can record reference information about a sold-to account in this field.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter SOLD.
2 Click on Create Record.
3 Key in your sold-to code and press Enter.
4 Key in your sold-to name and press Enter.
5 Key in the address of your sold-to, pressing Enter at the end of each line. For a SAME-type code, use a single period in the first address line to bypass this field.
6 In the ZIP / Postal Code field, key in the sold-to’s ZIP/postal code and press Enter. 
If the code that you enter is new and not yet on AccellosOne 3PL, your cursor will not advance to the next field and the Enter Criteria button will change to “Create Code”. If this occurs, click on Create Code. 
First key in your country code and press Enter. Press Enter again to accept the new ZIP or postal code. 
Then key in the city for the new ZIP code and press Enter. Next key in the state for the new code and press Enter. You will be brought back into CONS with the appropriate information filled in.
7 If required, key in your language code and press Enter. If no language code is required, press Enter to bypass this field.
8 Key in your customer code and press Enter or use .ALL for all your customers.
External Reference Number
Optional
You can add any miscellaneous reference information about a sold-to account in this field.
Last Activity Date Reserved for future use
FIELD DESCRIPTIONS

Sold-To Codes screen showing SAME-type code
9 If required, key in reference information in the Reference 1/2 fields and press Enter or press Enter with these fields blank to bypass the reference option. 
10 If required, key in your external reference number and press Enter.
11 In the Telephone Block, enter any telephone numbers and contact names that you wish to attach to this sold-to account. When you finish entering your telephone numbers, click on Return to Main to exit create mode.
12 Click on Master Block and then Exit to exit.

### Drivers (DRIV) <a id="drivers-driv"></a>

PREREQUISITES: None
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

OVERVIEW
In this program, you set up your drivers. You use drivers in the Carrier Block of ENRE and ENOR to identify the driver for a receipt or an order. For each driver that you set up, you can track the driver’s percentage, hourly rate and license number. This information is for look-up purposes only and is not used in any other 
AccellosOne 3PL program.
DRIV is intended for drivers who are employees of the warehouse — not drivers who work for outside carriers.
PROCEDURE
1 Enter DRIV.
2 Click on Create Record.
3 Key in your driver code and press Enter.
4 Key in your driver name and press Enter.
5 In the Percentage field, key in the percentage for this driver and press Enter. If there is no percentage for this driver, key in 0 as your percentage.
6 In the Hourly Rate field, key in the driver’s hourly rate and press Enter. 
FIELD DESCRIPTIONS
Code Mandatory
Your driver code.
Name Mandatory
The name of your driver.
Percentage Mandatory
The driver’s percentage. If the driver does not receive a percentage, enter 0.
Hourly Rate Mandatory
The driver’s hourly rate.
License Number Mandatory
The driver’s license number.

7 If the License Number field, key in the driver’s license number and press Enter. 
8 Repeat the above steps for each additional driver that you wish to add to DRIV.

Drivers screen showing three drivers
9 When you finish setting up your drivers, click on Return to Main and then Exit to exit.

### Language Code (LANG) <a id="language-code-lang"></a>

OVERVIEW
In this program, you set up your language codes. Language codes determine the language of field labels, hint lines, system codes, error messages, menu names, button text and any other text appearing in ActiveDesktop, AccellosOne 3PL, standard reports, e-Vista, d’Amigo and RF.
AccellosOne 3PL currently supports three base languages: English (ENUS), English (ENCA) and Spanish (ESMX). A base language is a language that has been fully translated by HighJump. You can create new nonbase languages if you wish to customize a base language. 
For example, if your base language is English (US) and you wish to change “item code” to “product code” in 
AccellosOne 3PL, you would create a language called ENG1 in LANG. Then you would enter TRMA (Translation Manger) and change “item code” to “product code” in the appropriate AccellosOne 3PL programs.
PREREQUISITES: None
ATTACHED TO: ALIT, CONS, SOLD, OPER
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

Languages are operator-specific in AccellosOne 3PL. Different operators can work in different languages within the same system. For example, operator 1 could be defined as English, while operator 2 could be defined as Spanish. You assign languages to operators in OPER (Operator Code).
PROCEDURE
1 Enter LANG.
2 Click on Enter Criteria then Execute Query to see whether the languages that you require have already been set up. If you need to set up a new language, click on New.
FIELD DESCRIPTIONS
Language Code Mandatory
Your code for the language.
Description Mandatory
Your description for the language.
Base A base language is a language that has been fully translated by HighJump. 
Base languages can only be set up by HighJump.
Parent Language Code Mandatory for non-base languages
The base language that your non-base language will inherit from. That means that unless you explicitly change a field label, system code, error message, etc. in TRMA, your new language will inherit all field labels, system codes, error messages, etc. from the base language.

Language Code
3 Key in your language code and press Enter. 
4 Key in your description and press Enter.
5 Select the appropriate base language from the Parent Language Code field.
6 When you finish entering your language, click on Save and then Exit to exit.

### Alternate Item and Language (ALIT) <a id="alternate-item-and-language-alit"></a>

OVERVIEW
In this program, you set up your alternate items and descriptions or aliases. You use alternate items and descriptions when you wish to print foreign language item codes and descriptions on a bill of lading or other shipping document. You can also use this program to set up alternate spellings of an item or item description within the same language. 
For example, you could set up one language code for American English and another language code for 
British English. When you shipped to an American consignee, the item description could be “color blue” and when you shipped to a British consignee the item description could be “color blue.”
PREREQUISITES: LANG, ALTP, CUST, ITEM, SHIP, CONS, CARR, SOLD
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A custom document created by HighJump

ALIT is a setup program for capturing alternate item and description information. If you want to print this information on a bill of lading or other document, you require a custom document programmed by HighJump.
Alternate items and descriptions consist of two elements: an “account to” value and an item. The “account to” 
value is a shipper, carrier, customer, consignee or sold to or any combination of these parties. An item is any item belonging to any customer. When you attach an “account to” value to an item, any order or receipt involving that item and that “account to” value will be assigned the alternate item and description. 
EXAMPLE 1
Account To = Consignee 1
Item = Item A
Language Code = SPANISH
Whenever you ship Item A to Consignee 1, a Spanish alternate item and description will be attached to an 
Item A document.
EXAMPLE 2
Account To = Shipper 2
Item = Item B
Language Code = GERMAN
Whenever you receive Item B from Shipper 2, a German alternate item and description will be attached to an 
Item B document.
NOTE The alternate language attached to an item in ALIT will always override the operator’s language. For example, an item can be attached to the language ENUS while the operator’s language is ENCA.
NOTE If you are setting up an alternate item and description for a consignee or sold to, the language code in ALIT for the consignee or sold-to must match the language code attached to the consignee in CONS or the sold-to in SOLD.
FIELD DESCRIPTIONS
Account To Code Mandatory
The party (customer, consignee, shipper, carrier, or sold-to) that is shipping the item (inbounds), carrying the item or receiving the item (outbounds). 

Customer Code (CUST) Mandatory
The customer code of the item.
Item Code (ITEM) Mandatory
The item to which you wish to attach the alternate item and description.
Level 2/3/4 Optional
If you populate these fields with level 2/3/4 values, you can capture style, size and color information for apparel, furniture, bedding and similar products. For example, you scan in a level 2 or 3 value from a bar code in RFCH and the bar code value of 1234 (the supplier code) is automatically converted to blue shirt (L1), size medium (L2) based on your setup in ALIT.
Level 2/3/4 conversion from a bar code is supported in both RFCH and 
RFPIC.
Alternate Type Code (ALTP) 
Mandatory
The alternate type code for this item. You use alternate type codes to specify the type of bar coding on an item’s label.
Language Code (LANG) Mandatory
The language of the alternate item and description. 
Account Item Code Mandatory
The item’s alternate item code. The alternate item code can be the same as the main item code (for example, A1) or it can be different from the main item code (for example, A1 - SPANISH).
For single inventory level product only, you can receive under an alternate item code in the core RF receiving programs RFCH and RFPU.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter ALIT.
2 Click on Create Record
3 Key in your account to code and press Enter. If you account to value is a consignee or sold to, you must attach the language code that you set up in ALIT to either the consignee in CONS or the sold to in SOLD.
4 Key in the customer code of the item and press Enter.
5 Key in your item code and press Enter.
6 If required, enter your level 2/3/4 values.
7 Use your pick list to select the appropriate alternate type code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
8 Use your pick list to select the appropriate language code.
9 In the Account Item Code field, key in your alternate item code and press Enter.
Account Item Quantity Optional
This field allows you to specify the quantity for DUN-14 labels.
If you leave the Account Item Quantity field blank, the default value of 1 will be used. That is, one scan = a quantity of one. If you enter a value other than one, that value will be used to calculate the quantity received. For example, if the account item quantity is four and you perform two scans for that item, the quantity received will be eight (2 X 4).
Account Item UPC Optional
The UPC code for this item/lot/pallet ID.
Description Mandatory
The alternate description for the item in the language that you specified in the 
Language Code field. 
Alternate Description Optional
If required, you can enter a second alternate description for the item in this field.
FIELD DESCRIPTIONS

10 If required, key in a quantity in the Account Item Quantity field and press Enter or press Enter with the field blank to bypass this function.
11 If required, key in the item’s UPC code in the Account Item UPC field and press Enter or press Enter with the field blank to bypass this function.
12 In the Description field, key in your alternate description for the item and press Enter.

Alternate Item & Language showing item A1 with a Spanish alternate description for Consignee 1
13 If required, key in a second alternate description in the Alternate Description field and press Enter or press Enter to bypass this field.
14 Click on Return to Main and then Exit to exit.

### Telephone Numbers (TELE) <a id="telephone-numbers-tele"></a>

PREREQUISITES: TETP
ATTACHED TO: N/A
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional

OVERVIEW
In CUST, CARR, CONS and SHIP, you added your customer, carrier, consignee and shipper contact names and telephone numbers to the telephone blocks in these programs. In TELE you can add any additional numbers you need that are not related to customers, carriers, consignees and shippers. For example, you could enter the names and telephone numbers of your suppliers, other warehouse staff, etc. 
The telephone numbers that you add to TELE and to the telephone blocks in CUST, CARR, CONS and SHIP can be viewed in LOTE (Look Up Telephone Numbers).
PROCEDURE
1 Enter TELE.
2 Click on Enter Criteria then Execute Query to see whether the telephone numbers that you require have already been set up. If you need to set up a new number, click on Create Record.
3 Use your pick list to select the appropriate telephone type.
4 Key in the telephone number and press Enter. 
5 Key in your contact name for this number and press Enter.
6 If required, key in the contact’s position and press Enter or press Enter with the field blank to bypass this option. 
OTHER REQUIREMENTS: The names and telephone numbers of the people that you wish to add to your telephone list
FIELD DESCRIPTIONS
List Code (TETP) Mandatory
Your telephone list type for the number.
Telephone Mandatory
The telephone number.
Contact Mandatory
The name of the person or company.
Position Optional
The contact’s position.

7 If you have additional numbers to enter, repeat the above steps for each additional number. 

Telephone Numbers
8 When you finish entering your telephone numbers, click on Return to Main and then Exit to exit.

A
Account Item Code field (ALIT) 357
Account Item Quantity field (ALIT) 358
Account To Code field (ALIT) 356
Account Type field (CUST) 142 active status 5
ADIM (Inventory Messages) 272
ADJU (Adjustment Type Codes) 312
Adjustment Analysis Description field (ADJU) 313
Adjustment Process field (IQBP) 230
Adjustment Type Codes (ADJU) 312
ALIT (Alternate Item and Language) 355 allocation, by weight 220
Allow Overpick, Ignore Consignee field (ITEM) 283
Allow Override of Hold Code During Core RF Receiving field (IHOP) 245
Allow Picking in Staging Location field (LOTP) 57
Alternate Billing Group Code field (TERM) 134
Alternate Description field (ALIT) 358
Alternate Inventory Reporting Code field (ITAS) 235
Alternate Item and Language (ALIT) 355
Alternate Reporting Block (ITEM) 300 alternate sorts (depositor) 137 alternate sorts (item) 233
Alternate Type Code field (ALIT) 357 anniversary monthly frequency (IRSP) 203 anniversary weekly frequency (IRSP) 203
Appointment Required field (CONS) 343
Assign Block (DILP) 110
Assign Description to New Entity field (DILP) 103
Assign Location field (DIFP) 80
Assign Profile Code field (DILP) 105
Attached to field (CONS) 342
Attached to field (SHIP) 333
Auto Take-Off field (HOLD) 239 auto-generation of lot numbers 88 automatic printing (DIFP) 82
B
B/L Message Code field (CARR) 323
B/L Message Code field (CONS) 340
BANK (Bank Code) 162
Bank Code (BANK) 162
Base field (LANG) 354
Base for Cube/Weight field (ITEM) 293
Base SKU Code field (SKUS) 14
Billing Entity Minimum Charge Code field (DILP) 107
Billing Entity Minimum Charge Code field (IBIP) 214 billing overview 175 billing periods, non-standard 210
Billing Profile Code field (CUST) 142
Billing Profile Code field (ITAS) 236
Billing Terms (TERM) 122
Bond field (HOLD) 238 break type charge (CHAR) 179
Breakable Inventory field (HOLD) 238
Breakdown Number field (CNTY) 26
Capacity SKU Code field (LOCA) 65
CARR (Carriers) 320
Carrier / Consignee / Shipper Code field (DPME) 268
Carrier Block (CUST) 155
Carrier Type Code field (CARR) 322
Carriers (CARR) 320
Change Zero Pending Line to R-type Line field (DSRP) 117
CHAR (Charge Codes) 175
Character Position field (WARE) 38
Charge Code field (IISP) 197 (IRSP) 205
Charge Definition field (CHAR) 179
Charge Initial and Renewal Storage field (DILP) 107
Charge on SKU Code field (CHAR) 180
Charge on SKU Code field (RATE) 187 charge on SKU code vs. qualify on SKU code, definition of

Charge Type Code field (CHAR) 177
Check Credit Limit field (DBIP) 129
City field (ZIPO) 32
CLAS (Class Codes) 252
CLAS (Freight Class Codes) 252
Class Codes (CLAS) 252
CNTY (Country Codes) 24
Code field (DEAS) 137
COMM (Commodity) 254
Command field (PRIN) 21
Command Type field (PRIN) 21
Commodity (COMM) 254
Commodity Code field (ITEM) 279
Compress Escape Sequence field (PRIN) 22
CONS (Consignees) 338
Consignees (CONS) 338
Consolidation Method for Allocated Lines field (CUST) 144
Contact field (TELE) 360 copying rates in RATE 191
Country Code field (ITEM) 285 country codes 24
Country Codes (CNTY) 24
Credit Limit field (DBIP) 129
Cross Dock field (ITEM) 282
CURR (Currency Codes) 160
Currency Code field (DBIP) 128
Currency Codes (CURR) 160
Current Number field (DONU) 18
CUSE (Customer Service Representatives) 73
CUST (Advanced) 152
CUST (Customer Setup) 139
Customer Code field (CONS) 340 (DLVP) 97 (SHIP) 331 (SOLD) 349
Customer Service Representatives (CUSE) 73
Customer Setup (Advanced) 152
Customer Setup (CUST) 139
Cycle field (DIAP) 92
Cycle field (IRSP) 204
D daily frequency (IRSP) 203
DAPR (Date Profile) 210
Date field (HOLD) 240
Date Format field (IIHO) 248
Date Formula field (IIHO) 248
Date Profile (DAPR) 210
Date Profile Code field (IBIP) 213
Date Used for Adjustments / Renewals field (ADJU) 314
DBIP (Depositor Billing Profile) 128 deactivated status 5
DEAS (Depositor Alternate Sorts) 137
Deassign Location field (DIFP) 80
Default Rate Charge Code field (CHAR) 181
Default SKU Adjustment Entry field (CUST) 145
Default SKU Order Entry field (CUST) 145
Default SKU Receipt Entry field (CUST) 145
Deferred Handling Inbound Percentage field (IINP) 194
DEME (Depositor Messages) 265
Depositor Alternate Sorts) 137
Depositor Billing Profile (DBIP) 128
Depositor Billing Rates (RATE) 185
Depositor Inventory Assign Profile (DIAP) 88
Depositor Inventory Level Profile (DILP) 101
Depositor Item Profile (DITP) 113
Depositor Item Profile Code field (CUST) 144
Depositor Level Validation Profile (DLVP) 95
Depositor Messages (DEME) 265
Depositor Print Messages (DPME) 267
Depositor Shipping and Receiving Profile (DSRP) 116
Depositor Workflow Profile (DIFP) 78
Description field (ALIT) 358 (ITAS) 236 (SKCL) 11
DIAP (Depositor Inventory Assign Profile) 88
DIFP (Depositor Workflow Profile) 78
DILP (Depositor Inventory Level Profile) 101
Directed Picking field (LOTP) 56
Directed Put-Away field (LOTP) 55
Disabled EDI Send field (HOLD) 239
Discount Day field (IISP) 198
Discount Good for X Days field (TERM) 124
Discount Percentage field (IISP) 198
Discount Percentage field (TERM) 124
Discount Profile Code field (ITEM) 284
DITP (Depositor Item Profile) 113
DLVP (Depositor Level Validation Profile) 95
Document Code field (ADJU) 313 (DIFP) 81 (DPME) 268
Document Numbers (DONU) 17
Document Types (DOTP) 10
DONU (Document Numbers) 17
DPME (Depositor Print Messages) 267
DRIV (Drivers) 351
Drivers (DRIV) 351
DSRP (Depositor Shipping and Receiving Profile) 116
E
EDI Profile Code field (CUST) 144
Effective Date field (RATE) 186
Effective Date for Charges field (ADJU) 313
Enable Location Aliases field (LOTP) 55, 67
End Number field (DONU) 18
Ending Number field (NUSE) 87 ending number in a number series (DONU) 17
Enter Charges field (ADJU) 313
Enter Expiry Dates field (ITSH) 219
Entry Required up to Level field (ITEM) 280 e-Vista field (HOLD) 239
Exact Length field (CNTY) 27
Exact Length field (DILP) 111
Exclude From Surcharge Calculations field (RATE) 187 expiry dates 217
