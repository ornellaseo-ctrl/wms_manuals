---
title: "K.Motion Mobile e Outbound (Körber One)"
description: "Guia mobile da geração Körber One: receiving, picking, packing, inventory e expedição."
layout: default
---

# K.Motion Mobile e Outbound (Körber One)

Guia mobile da geração Körber One: receiving, picking, packing, inventory e expedição.

**Fluxo principal:** `Login -> processo inbound/outbound -> tasks no dispositivo`

> Fonte: manuais MOB, OUT do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## K.Motion Mobile <a id="k-motion-mobile"></a>

*Manual MOB — K.Motion Mobile*

# Manual MOB — K.Motion Mobile User Guide (Guia Mobile v6.2)

> **ID do Manual:** MOB  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Guia do usuário mobile Körber One: login, navegação, receiving (check-in, unload, put-away), outbound (picking, packing, loading), inventory management (relocate, adjust, cycle count), label printing. Versão mais recente do sistema (v6.2, 2023).

---

K.Motion Enterprise 3PL Mobile User Guide 5 

### General Processes <a id="general-processes"></a>

There are general tasks you are required to perform regardless of the process in the system. As you navigate through the system, there will be options to type or enter information. Following each action, tap Submit to move to the next step.
Note
Tap Submit when prompted to enter or key in any information. The steps listed in this guide include entering the required information and then tapping the submit button.
This chapter includes the following topics:
• Logging On
• Using Körber One Mobile

### Logging on <a id="logging-on"></a>

### Introduction <a id="introduction"></a>

Logging into a device is the first step to completing any process within the warehouse. You may be logging into a device that uses Körber One Mobile or one that uses a traditional RF configuration.
After entering your username and password, you are required to enter a company code. Instead of entering a company code, you can select from a list by tapping F3:List which displays a list of companies. The company dialog is only available if you are allowed to work for more than one company. The selected company code remains the same for the entirety of the process you are completing. After initially logging in, the last used company code prepopulates when you attempt to log in again.
After the company code, you are prompted to enter an MHE code. Instead of entering an MHE Code, you can select an MHE by tapping F3:List which displays a list of codes. The MHE dialog is only available if you are allowed to work for more than one MHE. 

### Logging on to the Mobile Device <a id="logging-on-to-the-mobile-device"></a>

To log on to the mobile device using Körber One Mobile, complete the following steps:
1. Open the Körber One application.
2. Tap Menu. 
3. Tap Körber One Mobile. 
4. Tap Login. 

6 K.Motion Enterprise 3PL Mobile User Guide
5. Enter login information.
6. Enter the operator code.

K.Motion Enterprise 3PL Mobile User Guide 7 
7. Enter the password.
8. Enter the company code.
Note
If you do not know your company code, then ask your supervisor or tap List to view a company code list to select from the available options.

8 K.Motion Enterprise 3PL Mobile User Guide
9. Enter the MHE code.
Note
If you do not know your MHE code, then ask your supervisor or tap List to view an MHE list to select from the available options.

K.Motion Enterprise 3PL Mobile User Guide 9 
10. If applicable, enter an appropriate response to the safety questions. Repeat this step for each safety question.
Note
If safety questions are not configured for the equipment, then the main menu displays.
If safety questions are configured for the equipment and you answer “No” to one or more questions, then the MHE screen displays, and you are prompted to enter or select an MHE code.

### Using Körber One Mobile <a id="using-korber-one-mobile"></a>

All processes in this documentation are written using Körber One Mobile. Körber One Mobile contains several buttons and options that are available throughout the system regardless of what process you are performing.

### General Function Keys <a id="general-function-keys"></a>

Depending on the screen, you can choose to show or hide the function buttons.
Function Key Description
F1:Cancel Tap F1:Cancel throughout the system to go back to a previous screen.
F2:Execute Tap in a search screen scenario to execute a query.
F2:Select Tap when one of many records displays to select the current record. 
F3:Clear Query Tap to clear the query in a search screen scenario.
F3:List Tap in a scenario when you have to enter a value or choose from a list. 
F4:View Query Tap in a search screen scenario to view the list of the search criteria. 
F4:Prev. Record Tap when one of many records display to browse to the previous record. 
F5:Sort Tap to sort a list. 
F6:Detail Available on screens where more detail information is available. 
F6:Next Page Tap if dialog is divided into more than one page to browse additional pages. 
F7:Print Label Tap to print a label. 
F8:Next Record Tap if one of many records display to browse to the next record. 
F9:Options Tap to show the option dialog. 
F10:OK Tap to confirm a hint, error message, or notification. 
F11:Remarks Tap to display remarks and messages. 

### Option Dialog <a id="option-dialog"></a>

The option dialog displays the current company name, MHE, and process ID. Tap OK to return to the last viewed screen.

### Searching for a Record <a id="searching-for-a-record"></a>

Searching allows you to easily access the type of record you want. To perform a search, navigate to the appropriate search screen. There are several options accessible from the search screen. 

10 K.Motion Enterprise 3PL Mobile User Guide
Query Type Description
Execute Query Displays all search results for the process in which you are currently working.
View Query Displays the selected search parameters. In some cases, allows you to remove individual search parameters.
Note
You cannot clear the Company Code parameter. To change the company code, you must start the process over from the Log On screen.
Clear Query Clears the search criteria and returns to the default query.
To narrow search results, enter the preferred search criteria into the search field. After entering all search parameters, tap Execute Query. The system displays narrowed search results.
Consider the following tips when entering search criteria:
• Use a wildcard search by adding a percent sign (%) to the search criteria in the search field. 
• Entering multiple search criteria for any given query narrows the search. You can enter the customer code as well as the location to find entities for the customer on that location. 
• If the result of your query set up is on record, then the system displays the record.
• If you press F2:Execute Query, then a summary page displays. From there, you can browse through a list of records by tapping F8:Next Record. 

### Navigating within a List of Records <a id="navigating-within-a-list-of-records"></a>

A list of records includes a list of receipts, receipt lines, orders, order lines, or entities.
When you are reviewing and working through records, the following buttons display on the mobile device. 
Option Description
F8:Next Record Displays the first page of the first record. As you advance through the pages of a record, you can also tap F8:Next Record to display the same page number for the next record. For example, if you tap this button while on page two of a record, then page two of the next record displays.
F6:Next Page Displays when record data contains multiple pages.
F4:Previous Record Returns to the previous record. 
F2:Choose Line Selects the current line to allow you to start working with the record.

K.Motion Enterprise 3PL Mobile User Guide 11

### Inbound Processes <a id="inbound-processes"></a>

### Introduction <a id="introduction"></a>

The Inbound processes allow you to process inventory arriving at the warehouse. Inbound includes the following processes:
• Unloading
• Directed Put-Away
• Extra Charges In
• Add Values In (Process Values In)

### Unloading <a id="unloading"></a>

The purpose of the inbound unloading process is to unload inventory from a truck:
• To a staging location when performing two-step put-away 
• To a put-away location when performing one-step put-away
The inventory that needs to be unloaded is shown on a receipt. When processing a receipt, all inventory on the receipt line or lines associated with the receipt must be placed in either a staging or put-away location.
Receipts have a receipt line type of “P” (Post-Receiving) or “U” (Unknown). A “P” type receipt line is considered standard. A “U” type receipt line means the item level or levels on the receipt line or lines are unknown/missing. In this circumstance, you are prompted to enter the missing level information during the unloading process. This process is referred to as “Blind Receiving.”
For a receipt line to be available for processing, the following conditions apply:
• The receipt must be in Driver at Door (DRDO) status
• The receipt line requires at least an item with quantity
If you are unloading and receiving a product that is not listed on the receipt, then you can use 
Unloading to create new line(s) as long as the receipt is open. 
After you select a receipt line to start the unloading process, remarks and messages related to the receipt, selected receipt line, customer, item, or carrier display. When unloading the receipt, you can view a list of remarks by tapping Remarks throughout any process.
Before entering quantity, the system may prompt you to enter an expiration date using the format configured on the Item Shipping Profile page. You can use a variation of formats to display the dates, such as MM/DD/YY or DD/MM/YY. 
After entering quantity, the system may allow you to enter extra charges. You are prompted to enter extra charges of the unloading process: 
• After each receipt line is unloaded
• After all the receipt lines have been unloaded
• After each receipt line and all receipt lines have been unloaded
For more information about entering extra charges, see Extra Charges In. 

12 K.Motion Enterprise 3PL Mobile User Guide
After entering quantity, you are prompted to enter a Hold Code or select from a list. You have the option to leave the Hold Code field blank if there is no hold on inventory.
You are prompted to enter process values before or after entering location, depending how system is configured when to prompt. You can also add process values during the unloading process before the hold code prompt displays. 
You can print a label after selecting a receipt line to work on until you have entered a staging location. 
You can choose to print multiple labels if needed. The label printer, code, and format must be configured to print labels.
Toggle Mode displays during the unloading process. This option changes the mode from “Unload” to “Put Away” and allows you to complete the One-Step Put-Away process.
When you partially unload a receipt line, the system creates a separate receipt line for the unloaded inventory and returns to the main Unloading search screen. The inventory that has not yet been unloaded remains on the original receipt line. You can continue unloading from the same receipt.
When you completely unload a receipt, the Receipt Lines count reduces accordingly.
When you have unloaded the last receipt line on a receipt, the following options display:
• Completed—Tap if the current receipt is completed and you want to continue with other receipts.
• Exit—Tap to return to the Unloading search screen.
When working with temperature-controlled trailers, you are prompted to enter the trailer and pallet information for the receipt. Temperatures that need to be captured include:
• Front
• Middle
• Back
• Set
• Temp-5
• Temp-6

K.Motion Enterprise 3PL Mobile User Guide 13

### Unloading Tasks <a id="unloading-tasks"></a>

The following tasks can be completed from the Unloading menu.
• Entering Quantity
• Unloading a Receipt to a Staging Location
• Creating a Line Under an Existing Receipt
• Adjusting Trailer Temperatures

### Entering Quantity <a id="entering-quantity"></a>

You can enter received quantity from a receipt in three ways:
• Total QTY Method
• Tie, Hi, Loose Method
• Variable Breakdown Method
If there is a difference between the quantity you entered and what is expected, then you are prompted to verify the quantity. If you entered an incorrect quantity, then you can return to the TOTAL QTY screen by tapping N.
TOTAL QTY Method
Entering quantities with TOTAL QTY is the most common option. To use the TOTAL QTY method, complete the following steps:
1. Tap Inbound > Unloading. 
2. Scan the label or record.
3. Tap F2:Choose Line. 
4. Enter the quantity. 
Tie, Hi, Loose Method
Entering Tie, Hi, Loose values is based on how the pallet is structured (how many cases are on the pallet and how the cases are stacked). The quantities originate from the first two SKU codes associated with the item on the receipt. The SKU codes are defined in the Item Quantity Breakdown 

14 K.Motion Enterprise 3PL Mobile User Guide
Profile associated with the item. You can return to the TOTAL QTY screen any time during the process by tapping Enter Qty.

K.Motion Enterprise 3PL Mobile User Guide 15
To use the Tie, Hi, Loose method, complete the following steps:
1. Tap Inbound > Unloading.
2. Scan the label or record.
3. Tap F2:Choose Line.
4. Tap Tie, Hi, Loose.

16 K.Motion Enterprise 3PL Mobile User Guide
5. Enter the number of cases for Tie. 
6. Enter the number of cases for HI. 
7. Enter the number of cases for LOOSE. 
Variable Breakdown Method
You can change the variable breakdown quantity to enter the received breakdown values for the unit of measure. This option is only available on “U” type receipt lines. Changing the variable breakdown does not change the total quantity count. You must enter the updated quantity directly into the TOTAL 
QTY field. The Tie, Hi, Loose method automatically calculates the updated quantity.
To change the variable breakdown, complete the following steps:
1. Tap Inbound > Unloading. 
2. Scan the label or record. 

K.Motion Enterprise 3PL Mobile User Guide 17
3. Tap F2:Choose Line.
4. Tap F5:Change Breakdown.

18 K.Motion Enterprise 3PL Mobile User Guide
5. Tap the appropriate option from the Variable Breakdown list.
6. Enter the quantity. 
The updated quantity displays from Variable Breakdown screen.
7. Tap F1:Cancel to return to the TOTAL QTY screen.

### Unloading a Receipt to a Staging Location <a id="unloading-a-receipt-to-a-staging-location"></a>

You can update and add process values while you are unloading a receipt. To unload a receipt to a staging location, complete the following steps:
1. Tap Inbound > Unloading. 
2. Scan the pallet label or receipt using any search criteria.
3. Tap F2:Choose Line. 

K.Motion Enterprise 3PL Mobile User Guide 19
4. If remarks and messages display, then review the messages and tap F10:OK. If not, proceed to the next step.
5. If capture expiration date message prompts, then it displays the suggested date format that should be entered on next screen. Tap F10:OK.

20 K.Motion Enterprise 3PL Mobile User Guide
6. Enter a Level value.
7. Enter the total quantity received using one of the available methods from Entering Quantity. If the quantity automatically populates with the correct value, then tap Submit. 

K.Motion Enterprise 3PL Mobile User Guide 21
8. Enter the Hold Code. 
9. Scan the staging location. 
Note
You cannot change the mode in the system if the first receipt line is already unloaded at the staging location or put away at the destination location. 
If you are using the Unload mode, then the system populates the staging location based on the configuration. The remaining receipt lines assume the same staging location until you enter a different staging location. If you change the staging location, then the following receipt lines assume the new staging location until you exit the unloading process.
10. Enter N if extra charges prompt displays.
11. Continue unloading receipt lines or tap Completed/Exit. 

### Creating a Line Under an Existing Receipt <a id="creating-a-line-under-an-existing-receipt"></a>

When unloading a receipt and inventory is missing, you can add additional product to the receipt. To add a line to an existing receipt, complete the following steps: 

22 K.Motion Enterprise 3PL Mobile User Guide
1. Tap Inbound. 
2. Tap Unloading. 

K.Motion Enterprise 3PL Mobile User Guide 23
3. Tap F5:New Line. 
4. Enter the receipt number. 

24 K.Motion Enterprise 3PL Mobile User Guide
5. Enter the item code. 
6. Enter the quantity. 

K.Motion Enterprise 3PL Mobile User Guide 25
7. Tap F2:Choose Line.
8. Tap F10:OK.

26 K.Motion Enterprise 3PL Mobile User Guide
9. Enter a Level 2 value.
10. Enter a Level 3 value.

K.Motion Enterprise 3PL Mobile User Guide 27
11. Enter a Level 4 value.
12. Tap Submit to confirm the suggested quantity.

28 K.Motion Enterprise 3PL Mobile User Guide
13. Tap Submit to skip Hold Code assignment.
14. Tap Submit to confirm the suggested location.
15. Tap Completed / Exit. 

### Adjusting Trailer Temperatures <a id="adjusting-trailer-temperatures"></a>

You can use the mobile device to update trailer temperatures. To adjust trailer temperatures, complete the following steps:

K.Motion Enterprise 3PL Mobile User Guide 29
1. Tap Inbound. 
2. Tap Unloading. 

30 K.Motion Enterprise 3PL Mobile User Guide
3. Scan the pallet label or receipt. 
4. Tap F2:Choose Line. 

K.Motion Enterprise 3PL Mobile User Guide 31
5. Enter quantity. 
6. Leave hold code box empty and tap Submit. 

32 K.Motion Enterprise 3PL Mobile User Guide
7. Accept the suggested location or scan desired location.
8. Enter Y or N to answer if the trailer is dirty.

K.Motion Enterprise 3PL Mobile User Guide 33
9. Enter Y or N to answer if the product is dirty.
10. Enter Y or N to answer if there are any off odors or bad smells.

34 K.Motion Enterprise 3PL Mobile User Guide
11. Enter Y or N to answer if there is any evidence of insect infestations.
12. Enter Y or N to answer if there is evidence of rodents or rodent droppings.

K.Motion Enterprise 3PL Mobile User Guide 35
13. Enter Y or N to answer if there are cases or materials damaged or torn.
14. Enter Y or N to answer if there are any non-food items in trailers.

36 K.Motion Enterprise 3PL Mobile User Guide
15. Enter a numeric value or leave the field empty.
16. Enter a numeric value or leave the field empty.

K.Motion Enterprise 3PL Mobile User Guide 37
17. Enter a numeric value or leave the field empty.
18. Enter a numeric value or leave the field empty.

38 K.Motion Enterprise 3PL Mobile User Guide
19. Enter a numeric value or leave the field empty.
20. Enter a numeric value or leave the field empty.

K.Motion Enterprise 3PL Mobile User Guide 39
21. Enter a numeric trailer value or leave the field empty.
22. Enter a numeric seal value or leave field empty. 
23. Tap Completed / Exit. 

40 K.Motion Enterprise 3PL Mobile User Guide

### Adding Inventory Attributes During Unloading <a id="adding-inventory-attributes-during-unloading"></a>

To add inventory attributes unloading, complete the following steps: 
1. Tap Inbound. 
2. Tap Unloading. 
3. Enter the receipt number. 

K.Motion Enterprise 3PL Mobile User Guide 41
4. Tap F2:Chose Line. 
5. Tap F10:OK. 

42 K.Motion Enterprise 3PL Mobile User Guide
6. Enter a value for the inventory attribute requested. 
7. Tap F3:Value List to select one of the suggested values.

K.Motion Enterprise 3PL Mobile User Guide 43
8. Select a value for inventory attribute. 
9. Enter the quantity. 

44 K.Motion Enterprise 3PL Mobile User Guide
10. Leave the HOLD CODE field empty. 
11. If the suggested location is empty tap Submit or enter another staging location. 

K.Motion Enterprise 3PL Mobile User Guide 45
12. Select Completed. 

### Directed Put-Away <a id="directed-put-away"></a>

### Introduction <a id="introduction"></a>

After inventory is received and unloaded in the warehouse, it must be relocated to the designated location. To put away inventory, you can use the following methods:
• One-step Put-Away—The inventory is unloaded and put away directly in its designated location. 
To complete one-step put-away, the receipt line being put away must be in a Driver at Door (DRDO) status.
• Two-step Put-Away—The inventory is unloaded to a staging location and then put away in its designated location. To complete two-step put-away, the receipt line being put away must be in an Inbound Staged (INST) status.
• Mixed Product Put-Away—Put away multiple receipt lines when receiving mixed pallets and receipt lines share the same UI and Item codes.
After you select a receipt line to start the unloading process, the system displays remarks related to the receipt or selected receipt line. Additionally, any messages related to a customer, item, or carrier display, if configured. When putting away the receipt, you can also view a list of remarks by tapping 
Remarks. 
If you need to use a different destination location during two-step, put-away, you can enter a location other than the system-suggested location. You can also tap Next Loc to prompt for the next available location. The system notifies you if it is not configured to display locations or when there are no more available locations to display. After selecting a location, you are prompted to select a warehouse if there are multiple warehouses with the same location code. When you enter the destination location, review the confirmation screen to ensure all information is correct and tap Confirm. 
Supervisor authorization is required when you attempt to override a suggested location. For more information on this topic, see Supervisor Alerts. 

### Put-Away Tasks <a id="put-away-tasks"></a>

The following tasks can be completed from the Put-Away menu.

46 K.Motion Enterprise 3PL Mobile User Guide
• Complete One-Step Put-Away
• Complete Two-Step Put-Away
• Complete Put-Away to a Different Location with Supervisor Approval
• Put Away Mixed Product Pallets

### Completing One-Step Put-Away <a id="completing-one-step-put-away"></a>

You can put away inventory in one step. To complete one-step put-away, complete the following steps:
1. Tap Inbound > Unloading. 
2. Scan the pallet label or identify the receipt. 
3. Tap F2:Choose Line. 
4. Enter the expiration date, if prompted. 

K.Motion Enterprise 3PL Mobile User Guide 47
5. Use Tie, Hi, Loose, Change Breakdown, or enter the total quantity received. 
6. Enter the Hold Code. 

48 K.Motion Enterprise 3PL Mobile User Guide
7. Tap F3:Toggle Mode. 
The mode changes from “Unload” to “Put Away.”
8. Do one of the following:
a) Verify the system-suggested put-away location.
b) Enter a location other than the system-suggested put-away location (if needed).
9. If extra charges are configured, you are prompted to add extra charges. Do one the following:
a) To not add extra charges, enter N. 
b) To add extra charges, enter Y. Enter extra charge values for each prompt as needed. Tap 
F1:Cancel to return to the put-away process.
Note
For more information on extra charges, see Extra Charges. 

K.Motion Enterprise 3PL Mobile User Guide 49
10. Repeat previous steps for additional lines on the receipt. If there are no more lines on the receipt, tap Completed or Exit. 
The Unloading search screen displays.

### Completing Two-Step Put-Away <a id="completing-two-step-put-away"></a>

To complete two-step put-away, complete the following steps:
1. Tap Inbound > Put-Away. 
2. Scan the pallet label or receipt. 
3. Tap F2:Put Away from the appropriate record.
4. If remarks and messages are associated to the receipt, review the messages and tap F10:OK. If not, proceed to the next step.
5. Scan the destination. 

50 K.Motion Enterprise 3PL Mobile User Guide
6. Tap Confirm. 
7. Tap F10:OK. 
8. Repeat previous steps for additional receipt lines.
Receipt Put-Away search screen displays.

### Completing Put-Away to a Different Location with Supervisor Approval <a id="completing-put-away-to-a-different-location-with-supervisor-approval"></a>

You can put product away in a different location when needed with supervisor authorization. To complete a put-away receipt line to a different location than suggested and requires supervisor approval, complete the following steps:
1. Tap Inbound. 

K.Motion Enterprise 3PL Mobile User Guide 51
2. Tap Put-Away.
3. Scan the pallet label or receipt. 

52 K.Motion Enterprise 3PL Mobile User Guide
1. Tap F2:Put Away. 
2. Tap F10:OK.

K.Motion Enterprise 3PL Mobile User Guide 53
3. Enter a location different than suggested. 
4. Enter Y and locate the supervisor. 

54 K.Motion Enterprise 3PL Mobile User Guide
5. Enter supervisor credentials. 
6. Enter the supervisor password. 

K.Motion Enterprise 3PL Mobile User Guide 55
7. Tap F2:Confirm.
8. Tap F10:OK. 

56 K.Motion Enterprise 3PL Mobile User Guide

### Putting Away Mixed Product Pallets <a id="putting-away-mixed-product-pallets"></a>

You can put away mixed product from the Inbound menu when receiving mixed pallets. To put away receipt lines during a mixed pallet put away process, complete the following steps:
1. Tap Inbound > Put-Away. 
2. Scan the pallet label or receipt.
3. Tap UI. 

K.Motion Enterprise 3PL Mobile User Guide 57
4. Enter Y. 
5. If remarks and messages are associated to the receipt, review the messages and tap F10:OK. If not, proceed to the next step.

58 K.Motion Enterprise 3PL Mobile User Guide
6. Enter destination location.
7. Tap F2:Confirm.

K.Motion Enterprise 3PL Mobile User Guide 59
8. Tap F10:OK. 
9. Tap F10:OK. 
The Receipt Put-Away search screen displays.

### Extra Charges In <a id="extra-charges-in"></a>

### Introduction <a id="introduction"></a>

The Extra Charges In process allows you to apply extra charges to a customer’s receipt according to the charge profile set up in the system.
To apply extra charges to a receipt or receipt line, the following conditions apply:
• The receipt cannot be closed. You can only apply extra charges when the receipt is in the following statuses:
− Start Unloading
− Inbound Staged
− Start Put-Away
− Put-Away Complete
• You can apply charges to the receipt itself or to a receipt line.
• If the Line number in the Receipt/Line field is “0,” the extra charges are applied to the receipt itself. 
If the Line number in the Receipt/Line field is “1” or more, the extra charges are applied to the applicable receipt line.
The order of information may differ, but the system generally displays the following information as you advance through the pages of the record: 
• Charge Record Number
• Receipt/Line Number
• Charge Code
• Description
• Quantity
To review the details of a receipt, you can tap Receipt Detail. This option is available on any charge record screen.

60 K.Motion Enterprise 3PL Mobile User Guide

### Applying Extra Charges <a id="applying-extra-charges"></a>

You can apply extra charges to a receipt. To apply the quantity of extra charges, complete the following steps:
1. Tap Inbound > Extra Charges In. 
2. Scan the receipt.

K.Motion Enterprise 3PL Mobile User Guide 61
3. Enter the charge quantity in the NEW QTY field.
4. Repeat previous steps until the quantities are applied to all charge records on the receipt.

### Editing Extra Charges <a id="editing-extra-charges"></a>

To edit the quantity of extra charges, complete the following steps:
1. Tap Inbound > Extra Charges In. 
2. Scan the receipt.
3. Edit the charge quantity in the NEW QTY field.
4. Repeat previous steps until the quantities are applied to all charge records on the receipt.

### Add Values In (Process Values In) <a id="add-values-in-process-values-in"></a>

### Introduction <a id="introduction"></a>

Process Values In allows you to enter or view process values on process codes associated with items. You can only view process code details if all process values for that item have not been entered.
When accessing the Process Value In search screen, the number of available receipt lines display.
For the receipt line to be available for processing, the following conditions apply:
• The process values on process codes associated with an item are fully or partially missing
• The receipt cannot be closed. The receipt line must be in one of the following process flow statuses:
− Inbound Staged (INST)
− Put-Away Complete (PUCO)
To enter process values, you are prompted for information depending on the SKU class. If there are multiple process codes associated with an item and their SKU types match, the system prompts for the first value on all process codes before prompting for the second process value. If the SKU types do not match, you must enter values for one process code at a time. 
After you complete the process and enter the last process value on the last process code associated with an item on the receipt line, the system accepts the value and displays the Process Value In search screen and the receipt line number count decreases by one.
Serial number and weight are two of the most common process values entered. An item’s weight and its unit of measure are saved in the system according to the item quantity breakdown profile. If the

62 K.Motion Enterprise 3PL Mobile User Guide process code is configured by weight and unit of measure, the system prompts you to select a unit of measure. The system currently supports kilograms and pounds.
You can enter weight manually or via the weight discovery process by scanning a barcoded label. To enter by scanning a barcoded label, the following conditions apply:
• The length of every barcode must be the same.
• To continue scanning barcodes and extracting weight values, the system prompts you for the weight location for the first three times while scanning a series of barcodes. This process is called
Weight Discovery. If all three barcodes have the same weight position, the system allows you to continue. If you encounter an error, follow the prompts and rescan.
• When a barcode is scanned and all of the following criteria are met, the system automatically saves the process value for Serial Number:
− The weight and serial number process code is attached to the item.
− The SKU classes match for both process codes.
− The item process code type is equal to the Serial Number in Weight Barcode (SER). 
Note
If you encounter any errors, contact your supervisor.
When using weight as a process value, a tolerance may be configured. If the inventory weight is greater than or less than the configured tolerance percentage, the system rejects the weight and requires you to re-enter the weight.

### Viewing Process Values on a Process Code <a id="viewing-process-values-on-a-process-code"></a>

You can view process values on a process code. To view process code details, complete the following steps:
1. Tap Inbound > Add Values In. 
2. Scan the pallet label or identify the receipt. 
3. Tap Detail Process. 
The system displays the list of process codes needing process values.
4. Tap to select the preferred process code from the list.
The system displays the list of process values entered for the selected process code.
5. Tap F1:Cancel to return to the previous screen.

### Adding a Process Value to an Item on a Receipt Line <a id="adding-a-process-value-to-an-item-on-a-receipt-line"></a>

You can add process values to an item on a receipt line. To add a process value to an item on a receipt line, complete the following steps:
1. Tap Inbound > Add Values In. 
2. Find and access the receipt record by scanning the pallet label or entering a receipt identifier.
The system displays the Process Value In summary screen.
3. Tap F2:Receipt Lines. 
The first process code that needs a process value or values on that line displays.
4. Scan the first process value.
5. Continue until you scan all values for all process codes.
Note
If all process codes associated with an item are configured with the same SKU class, the system continues prompting for values on all process codes in the sequence. If process codes associated with an item are configured with different SKU classes, the system prompts for process values for each process code separately.

K.Motion Enterprise 3PL Mobile User Guide 63

### Adding a Weight Process Value to the Item on a Receipt Line <a id="adding-a-weight-process-value-to-the-item-on-a-receipt-line"></a>

You can add weight values to items on a receipt line. To add a weight process value to an item on a receipt line, complete the following steps:
1. Tap Inbound > Add Values In. 
2. Scan the pallet label or identify the receipt.
3. Tap F2:Receipt Lines. 
4. Select Unit of Measure, if configured.
5. Do one of the following:
a) Enter Y to begin Weight Discovery for barcode scanning.
b) Enter N to begin entering weight manually.
6. Do one of the following.
a) If you entered Y, then scan the first three barcodes and confirm the weight positions. After confirming, continue scanning barcodes for process values.
b) If you entered N, the enter the weight manually. Continue entering values manually.

64 K.Motion Enterprise 3PL Mobile User Guide

### Outbound Processes <a id="outbound-processes"></a>

### Introduction <a id="introduction"></a>

The Outbound processes allow you to prepare inventory to leave the warehouse.
Outbound includes the following processes:
• Default Picking
• Wave Picking
• Replenishment
• Process Value Out
• Extra Charges Out
• Loading
• Carton Sorting
• Merging Pallets
• Relocating Pallets

### Default Picking <a id="default-picking"></a>

Order picking allows you to take product from the shelf in the warehouse to fulfill consignee orders. 
There are four picking modes:
Mode Description
Pallet Picking (NM) Inventory picked as a whole pallet or from a pallet have the same LP/UI as pallet.
Only Pallet Picking Inventory picked as a whole pallet or from a pallet have the same LP/UI as pallet.
Note
If the picking mode is Pallet Picking or Only Pallet Picking and if configured, the UI code is used as the OPID during the picking process. 
Mode Description
Case Picking (CP) The system assigns an OPID (license plate) to cases picked from the pallet. 
Only Case Picking The system assigns an OPID (license plate) to cases picked from the pallet. 
Note
If the picking mode is Only Pallet Picking or Only Case Picking, you cannot switch from one mode to another. The Toggle Mode button is not available when using these modes of picking.
The following pick operations are available:
• Full pallets
• Cases
• Remaining quantity on a pallet, as a full pallet

K.Motion Enterprise 3PL Mobile User Guide 65
Orders to be picked must be in Supervisor Allocated status. To pick an order, you can search using the following criteria:
• Customer Code
• Warehouse Code
• Order Number
• Customer’s Order Number
• Order Reference 1
• Order Reference 2
• Carrier Code
Tap Sort Order before choosing an order to begin picking to change how the order sequence is sorted. Orders can be sorted by:
• Priority: Displays as highest priority to lowest priority
• Ship to Date: Displays oldest date to newest date
• Carrier: Displays in alphabetical order
• Customer: Displays in alphabetical order, by Customer Code
After sorting, the system displays the Outbound Picking summary screen with the new sort order.
After you select an order line to start the picking process, the system displays remarks related to the order, selected order line, or both. When picking an order, you can view a list of remarks or messages by tapping F11:Remarks throughout any process. If configured, any messages related to a customer, item, carrier, or consignee display. 
When you are prompted to scan a location, you must scan the location prior to entering or scanning the UI.
If configured, you can perform inventory count-backs. Count-back conditions are configured in the RF profile, which is associated with the Customer profile.
Multi-line pick allows for picking multiple lines to an OPID. When the user is ready, tap F7:Destination to be prompted for the TO LOC instead of automatically prompting after each picked line. Depending on configured options, your set of prompts may vary, but the looping is what is important.

66 K.Motion Enterprise 3PL Mobile User Guide
You can also perform picking substitution if configured. Picking substitution allows you to pick an item on the order line from a pallet ID other than the allocated pallet ID (if allowed by the system). Some examples of allowed substitute product rules include the following:
• “Substitute product can come from any location”
• “Ignore FIFO requirement for substitute product”
• “Do not use stock allocated to other orders as substitute”
If the original order has a hold code, the substitute product must have the same hold code.
Supervisor authorization is required when you attempt to place product on suspended hold or enter a quantity that is less than the expected quantity. For more information on this topic, see Supervisor 
Alerts. 

### Default Picking Tasks <a id="default-picking-tasks"></a>

The following tasks can be completed from the Default Picking menu.
• Picking an Order with Pallet Picking
• Placing Inventory on Suspended Hold with Supervisor Approval
• Picking Partial Quantity with Supervisor Approval
• Picking an Order with Case Pick and Accumulating Multi-Line Pick

### Picking an Order with Pallet Picking <a id="picking-an-order-with-pallet-picking"></a>

You can pick an order from Default Picking. To pick an order, complete the following steps:
1. Tap Outbound > Picking. 
2. Tap Default Picking. 
The Outbound Picking search screen displays. 

K.Motion Enterprise 3PL Mobile User Guide 67
3. Scan the order label or identify the order.
4. Tap F2:Take This Order.

68 K.Motion Enterprise 3PL Mobile User Guide
5. Tap Pallet Picking.
6. Tap F2:Pick this Line.
7. Do one of the following:
a) If the Review Remarks display, then tap F10:OK. 
b) If no remarks display, then go to the next step. 
8. Scan the current location of the item.

K.Motion Enterprise 3PL Mobile User Guide 69
9. Enter the UI. 
Note
If picking substitution is configured, then scan the substitution UI for the item being picked.
Note
You can select Set OPID on any screen after picking the line until you confirm the quantity.

70 K.Motion Enterprise 3PL Mobile User Guide
10. Enter quantity. 
Notes
- If the system is configured to enter process values during the picking process and you are 
picking either a full pallet or the remaining quantity on a full pallet and the process value you need for the picked inventory exists in the warehouse, then you do not need to separately enter the process values manually. The system automatically transfers the process values and displays an informational message.
- If the system is configured to enter process values during the picking process using the 
case pick method and throw-back is configured, then you must enter the remaining process values that have not been picked.
- If the system is configured to enter process values during the picking process and countbacks are not configured, then you must enter process values when you enter the quantity. 
However, if count-backs are configured, you must enter process values followed by the count-backs entry flow.
11. Enter printer code. 
12. Do one of the following:
a) If count-backs are not configured, then proceed to Step 15.
b) If count-backs are configured, then enter the remaining quantity after picking the quantity needed. 
c) If the quantity does not match the system expected quantity, then the system prompts you to re-enter the quantity. 
Note
You can enter the remaining quantity using Tie, Hi, Loose after picking the quantity needed. If the quantity does not match the system expected quantity, the system prompts you to reenter the quantity.

K.Motion Enterprise 3PL Mobile User Guide 71
13. Do one of the following:
a) If the discrepancy of the remaining quantity is resolved, then enter “Y” in the Resolved field.
b) If the discrepancy of the remaining quantity is not resolved, then enter “N” in the Resolved field.
14. Enter the destination location in the TO LOC field.
15. Enter N.

72 K.Motion Enterprise 3PL Mobile User Guide
16. If more order lines exist in the current pick list, repeat steps for each remaining order line to continue picking the same order. If more order lines in exist in another pick list, the system prompts you to continue with the next picking list of the same order.
17. Tap F10:OK. 
Outbound Picking search screen displays.

### Placing Inventory on Suspended Hold with Supervisor Approval <a id="placing-inventory-on-suspended-hold-with-supervisor-approval"></a>

You can place a hold when the available pick quantity will not fulfil the order. When you place the item on hold, a new order line is created and must be allocated to the proper picking line. To place inventory on suspended hold, complete the following steps:
1. Tap Outbound > Picking. 
2. Tap Default Picking. 

K.Motion Enterprise 3PL Mobile User Guide 73
3. Scan order number.
4. Tap F2:Take This Order.

74 K.Motion Enterprise 3PL Mobile User Guide
5. Tap Case Picking.
6. Tap F2:Pick this Line. 

K.Motion Enterprise 3PL Mobile User Guide 75
7. Scan location.
8. Scan the UI.

76 K.Motion Enterprise 3PL Mobile User Guide
9. Tap F3:Hold.
10. Enter Y and locate supervisor to provide username and password.

K.Motion Enterprise 3PL Mobile User Guide 77
11. Supervisor must enter username and password.
12. Enter Y to approve transaction.
The line is placed on hold and the system advances to the next available pick line.

### Picking Partial Quantity with Supervisor Approval <a id="picking-partial-quantity-with-supervisor-approval"></a>

When you are picking product for an order and need to pick less than the expected quantity, you can do so with supervisor authorization. To pick a partial quantity on an order, complete the following steps:
1. Tap Outbound > Picking. 
2. Tap Default Picking. 
The Outbound Picking search screen displays.
3. Scan the order label or identify the order. 
4. Tap F2:Take This Order. 
5. Tap Case Picking. 

78 K.Motion Enterprise 3PL Mobile User Guide
6. Tap F2:Pick this Line. 
7. Scan location.
8. Scan the UI.

K.Motion Enterprise 3PL Mobile User Guide 79
9. Enter the quantity remaining in inventory. 
Note
Supervisor will be required to login and approve any quantities less than what is expected.
10. Enter Y and locate the supervisor to provide username and password.

80 K.Motion Enterprise 3PL Mobile User Guide
11. Supervisor must enter username and password.
12. Enter Y to approve transaction.
The line is placed on hold and the system advances to the next available pick line.

### Picking an Order with Case Pick and Accumulating Multi-Line Pick <a id="picking-an-order-with-case-pick-and-accumulating-multi-line-pick"></a>

To accumulate multi-line pick, complete the following steps:
1. Tap Outbound > Picking. 
2. Tap Default Picking. 
The Outbound Picking search screen displays.
3. Scan the order label or identify the order. 
4. Tap F2:Take This Order. 
5. Tap Case Picking. 

K.Motion Enterprise 3PL Mobile User Guide 81
6. Tap F2:Pick this Line. 
7. Tap F10:OK. 

82 K.Motion Enterprise 3PL Mobile User Guide
8. Scan location. 
9. Scan the UI.
10. Enter quantity. 

K.Motion Enterprise 3PL Mobile User Guide 83
11. Do one of the following:
a) Tap F7:Destination and proceed to step 16.
b) Tap F2:Pick this Line. 
12. Tap F10:OK. 

84 K.Motion Enterprise 3PL Mobile User Guide
13. Scan location. 
14. Optional: Tap F7:Print Label if needed and configured.
15. Enter pick quantity.

K.Motion Enterprise 3PL Mobile User Guide 85
16. Enter the printer code.
17. Enter the staging location. 
Order completed screen displays.

### Wave Picking <a id="wave-picking"></a>

### Introduction <a id="introduction"></a>

Wave picking allows you to group several orders that can be picked and shipped together. You can use wave picking to allocate all orders grouped by the same wave in one step to avoid processing one order at a time. 
Waves contain multiple orders and have a wave number for identification. In a wave pick, the picker selects a wave and then picks an order that is assigned to it. 

86 K.Motion Enterprise 3PL Mobile User Guide
Each order line is assigned to a pick method once allocation is complete. Pick methods are assigned to order lines in the Wave Manager based on the order line quantity and the item setup. The system determines the appropriate picking method for you. You will see one or more of the following picking methods during a wave pick:
• Batch Pick
• Batch Pallet Pick
• Carton Pick
• Each Case Pallet Pick
• Less Than Pallet Pick
• Case Pick
• Pallet with PickPack
• Pallet without PickPack

### Wave Picking Tasks <a id="wave-picking-tasks"></a>

Access the Wave Picking search screen by completing the following steps and then proceed to the task you need to accomplish.
1. Tap Outbound > Picking. 

K.Motion Enterprise 3PL Mobile User Guide 87
2. Tap Wave Picking. 
3. Select from the following list to go to the task you want to complete:
a) Picking a Wave Batch Pick
b) Picking a Wave Batch Pallet
c) Picking a Wave Carton Pick
d) Picking an Each Case Pallet Pick
e) Picking a Less Than Pallet Pick
f) Picking a Wave Case Pick
g) Picking a Wave Pallet with PickPack
h) Picking a Wave Pallet without PickPack

### Picking a Wave Batch Pick <a id="picking-a-wave-batch-pick"></a>

You can pick across multiple orders when two or more orders in the wave are picked up by the same carrier and carrier type. To pick a wave batch, complete the following steps:
1. Navigate to Wave Picking search screen.

88 K.Motion Enterprise 3PL Mobile User Guide
2. Enter wave number. 
3. Tap BATCH PICK.

K.Motion Enterprise 3PL Mobile User Guide 89
4. Scan the first label.
5. Tap F2:Pick this Line.

90 K.Motion Enterprise 3PL Mobile User Guide
6. Scan OPID.
7. Scan location.

K.Motion Enterprise 3PL Mobile User Guide 91
8. Scan the UI.
9. Scan the last label.

92 K.Motion Enterprise 3PL Mobile User Guide
10. Scan the location.
11. Tap F10:OK.

K.Motion Enterprise 3PL Mobile User Guide 93
12. Repeat previous steps until all orders are complete.
13. Tap F10:OK. 
Wave Picking search screen displays.

### Picking a Wave Batch Pallet <a id="picking-a-wave-batch-pallet"></a>

When a pick consists of partial pallets, the same inventory in a single location, or when the entire inventory entity in the location is picked, the Batch Pallet Picking displays as an option. This enables you to pick batch pallets across multiple orders in the same wave when you need to pick entire pallets. To pick wave batch pallets, complete the following steps:
1. Navigate to Wave Picking search screen.
2. Enter the wave number. 

94 K.Motion Enterprise 3PL Mobile User Guide
3. Tap BATCH PALLET.
4. Scan the Carton ID.

K.Motion Enterprise 3PL Mobile User Guide 95
5. Scan the location.
6. Scan the UI.

96 K.Motion Enterprise 3PL Mobile User Guide
7. Enter the quantity. 
8. Enter the location. 
Wave completed message displays if there are no other orders.
9. Tap F10:OK. 

### Picking a Wave Carton Pick <a id="picking-a-wave-carton-pick"></a>

You can pick directly into cartons for multiple orders with multiple lines during Wave Carton Picking. 
When an order is allocated and the picking method is set to CART, you can begin picking. To pick 
Wave Cartons, complete the following steps:
1. Navigate to Wave Picking search screen.
2. Enter the wave number. 

K.Motion Enterprise 3PL Mobile User Guide 97
3. Tap CARTON PICK.
4. Scan the Carton ID.
5. Enter the slot number.

98 K.Motion Enterprise 3PL Mobile User Guide
6. Repeat previous steps until all cartons and slots are entered.
7. Tap F2:Start Picking.

K.Motion Enterprise 3PL Mobile User Guide 99
8. Scan the Item.
9. Enter the quantity.

100 K.Motion Enterprise 3PL Mobile User Guide
10. Repeat previous steps until all cartons and quantities are entered.
11. Scan the location. 
12. Repeat previous steps to pick additional orders until complete.

### Picking an Each Case Pallet Pick <a id="picking-an-each-case-pallet-pick"></a>

You can use Loose Pick to pick items that are less than a case. To pick each case with Loose Pick, complete the following steps:
1. Navigate to Wave Picking search screen.

K.Motion Enterprise 3PL Mobile User Guide 101
2. Scan the wave number.
3. Tap LOOSE PICK.

102 K.Motion Enterprise 3PL Mobile User Guide
4. Tap F2:Pick this Line.
5. Scan the source location.

K.Motion Enterprise 3PL Mobile User Guide 103
6. Scan the UI.
7. Enter the quantity.

104 K.Motion Enterprise 3PL Mobile User Guide
8. Enter the printer code. 
9. Enter the location. 
10. Enter N. 
11. Tap F10:OK on confirmation screens.

### Picking a Less Than Pallet Pick <a id="picking-a-less-than-pallet-pick"></a>

You can perform wave picking with items that are less than a full pallet. To perform Less Than Pallet 
Picking on a wave with one order, complete the following steps:
1. Navigate to Wave Picking search screen.

K.Motion Enterprise 3PL Mobile User Guide 105
2. Enter the wave number.
3. Tap LESS THAN PALLET.

106 K.Motion Enterprise 3PL Mobile User Guide
4. Enter the number of orders.
5. Scan the Carton.

K.Motion Enterprise 3PL Mobile User Guide 107
6. Tap F2:Choose.
7. Scan the location.

108 K.Motion Enterprise 3PL Mobile User Guide
8. Scan the item.
9. Enter the total quantity.

K.Motion Enterprise 3PL Mobile User Guide 109
10. Rescan the Carton ID.
11. Enter the pack quantity.

110 K.Motion Enterprise 3PL Mobile User Guide
12. Enter the location. 
13. Tap F10:OK. 
Wave Picking search screen displays.

### Picking a Wave Case Pick <a id="picking-a-wave-case-pick"></a>

Case Pick displays when a pick line contains full cases. To pick a wave case, complete the following steps:
1. Navigate to Wave Picking search screen.
2. Enter the wave number. 

K.Motion Enterprise 3PL Mobile User Guide 111
3. Tap CASE PICK.
4. Tap F2:Pick this Line.

112 K.Motion Enterprise 3PL Mobile User Guide
5. Tap F10:OK.
6. Scan the location.

K.Motion Enterprise 3PL Mobile User Guide 113
7. Scan the UI.
8. Enter the quantity.

114 K.Motion Enterprise 3PL Mobile User Guide
9. Enter the printer code.
10. Enter the location.

K.Motion Enterprise 3PL Mobile User Guide 115
11. Enter Y.
12. Enter the new quantity.
Updated quantity displays on Qty line.

116 K.Motion Enterprise 3PL Mobile User Guide
13. Tap F1:Cancel. 
14. Tap F10:OK after each message.
Outbound Picking search screen displays.

### Picking a Wave Pallet with PickPack <a id="picking-a-wave-pallet-with-pickpack"></a>

Wave Pallet Picking with PickPack allows you to search for records using a carton ID. To pick a wave pallet, complete the following steps:
1. Navigate to Wave Picking search screen.
2. Enter the wave number. 

K.Motion Enterprise 3PL Mobile User Guide 117
3. Tap PALLET PICK.
4. Scan the Carton.

118 K.Motion Enterprise 3PL Mobile User Guide
5. Scan the location.
6. Scan the item.

K.Motion Enterprise 3PL Mobile User Guide 119
7. Enter the quantity. 
8. Scan the location. 
9. Follow previous steps to continue picking if there are other items. If not, proceed to the next step.
10. Tap F10:OK. 
Wave Picking search screen displays.

### Picking a Wave Pallet without PickPack <a id="picking-a-wave-pallet-without-pickpack"></a>

Pallet Pick displays when a pick line contains a full pallet as defined by the item breakdown. To pick a wave pallet without PickPack, complete the following steps:
1. Navigate to Wave Picking search screen.

120 K.Motion Enterprise 3PL Mobile User Guide
2. Enter the wave number.
3. Tap PALLET PICK.

K.Motion Enterprise 3PL Mobile User Guide 121
4. Tap F2:Pick this Line.
5. Tap F10:OK.

122 K.Motion Enterprise 3PL Mobile User Guide
6. Scan the location.
7. Scan the UI.

K.Motion Enterprise 3PL Mobile User Guide 123
8. Enter the quantity.
9. Enter the Printer Code.

124 K.Motion Enterprise 3PL Mobile User Guide
10. Enter the location.
11. Enter N.
12. Tap F10:OK.
Wave Picking search screen displays.

K.Motion Enterprise 3PL Mobile User Guide 125

### Replenishment <a id="replenishment"></a>

### Introduction <a id="introduction"></a>

Replenishment allows you to replenish your pick line location using the mobile device. Replenishment takes place during order allocation and performs based off parameters defined in Pick Line-Item
Assignment. When parameters are not defined, the system uses default parameters for picking.
Replenishment must be confirmed through Relocate to Pick Line. There are three replenishment modes to select in Replenishment. The modes allow you to rank replenishments by urgency by performing more urgent replenishments first, less urgent second, and non-urgent last. The three replenishment modes are:
Mode Description
Active Demand Replenishment records display when the on-hand quantity in the pick line is less than the order quantity. 
Threshold Minimum Replenishment records display when the on-hand quantity in the pick line location is less than the minimum quantity as defined in the Pick Line-Item
Assignment. 
All All replenishment records display
Depending on the setup: 
• It is possible to collect several replenishments on the MHE and then distribute them to pick lines. 
• Process a countback in the pick line location.
• Replenishment Countback: When you perform inventory counts on the pick line. 
Supervisor authorization is required when you attempt to cancel a replenishment. The system prompts for approval to delete the replenishment and place the inventory on suspended hold. For more information on this topic, see Supervisor Alerts. 

### Select Replenishment Mode <a id="select-replenishment-mode"></a>

Access the Replenishment search screen by completing the following steps and then proceed to the task you need to accomplish.
1. Tap Outbound > Replenishment. 

126 K.Motion Enterprise 3PL Mobile User Guide
2. Tap the appropriate option from one of the following:
• Active Demand-Replenishment records display when the on-hand quantity of pick line is less than the order quantity. 
• Threshold Minimum-Replenishment records display when the on-hand quantity in the pick line location is less than the minimum quantity as defined in the Pick Line-Item Assignment. 
• All-All replenishment records display.

### Replenishment Tasks <a id="replenishment-tasks"></a>

You can perform the following tasks from the Replenishment menu option:
• Navigating Replenishment Records
• Performing a Basic Replenishment
• Performing a Partial Replenishment
• Performing Multiple Pallet Replenishment with Multiple Tasks
• Performing Inventory Counts on a Pick Line
• Cancelling a Replenishment with Supervisor Authorization

### Navigating Replenishment Records <a id="navigating-replenishment-records"></a>

You can review replenishment inventory in the warehouse. To navigate through replenishment records, complete the following steps:
1. Navigate to the Replenishment search screen.
2. Scan the UI or identify the order. 
3. Tap F6:Next Page to show the available details. 
a) Order date/time
b) Relocation date/time
c) Customer code
d) Level 1 value (item)
e) To location code
f) Quantity

K.Motion Enterprise 3PL Mobile User Guide 127
4. Tap F6:Next Page to show the available details. 
5. Tap F2:Choose Line to start the replenishment. 

### Performing a Basic Replenishment <a id="performing-a-basic-replenishment"></a>

You can replenish inventory in the warehouse to its designated pick location. To perform basic replenishment, complete the following steps:
1. Navigate to the Replenishment search screen.
2. Scan the UI or identify the order.
3. Tap F8:Next Record to find the appropriate record.
4. Tap F2:Choose Line. 

128 K.Motion Enterprise 3PL Mobile User Guide
5. Scan the UI.
6. Enter the quantity. 
7. Enter the destination location. 
The Replenishment search screen or menu displays.

### Performing a Partial Replenishment <a id="performing-a-partial-replenishment"></a>

When the stock is not available to fulfill an order, you can perform a partial replenishment. To confirm a partial replenishment, complete the following steps:
1. Navigate to the Replenishment search screen.

K.Motion Enterprise 3PL Mobile User Guide 129
2. Scan the UI or identify the order.
3. Tap F8:Next Record to locate the appropriate record.
4. Tap F2:Choose Line.

130 K.Motion Enterprise 3PL Mobile User Guide
5. Scan the UI.
6. Enter less quantity than the amount displayed on Replenish field. 

K.Motion Enterprise 3PL Mobile User Guide 131
7. Tap BACK TO ORIG LOC. 
8. Enter destination location. 
9. Enter the source location. 
Replenishment search screen or menu displays.

### Performing Multiple Pallet Replenishment with Multiple Tasks <a id="performing-multiple-pallet-replenishment-with-multiple-tasks"></a>

You can process orders that have more than one replenishment task in a multi-pallet replenishment. 
To perform multiple pallet replenishment with multiple tasks, complete the following steps:
1. Navigate to the Replenishment search screen.

132 K.Motion Enterprise 3PL Mobile User Guide
2. Scan the UI or identify the order. 
3. Tap F2:Choose Line.

K.Motion Enterprise 3PL Mobile User Guide 133
4. Scan the UI.
5. Enter the quantity. 

134 K.Motion Enterprise 3PL Mobile User Guide
6. Tap PICK OTHER.
7. Locate the second replenishment. 
8. Tap F2:Choose Line.

K.Motion Enterprise 3PL Mobile User Guide 135
9. Scan the UI.
Note
A message displays when an item cannot be stacked. Tap Ok to access the Quantity screen.
10. Enter the quantity. 

136 K.Motion Enterprise 3PL Mobile User Guide
11. Tap PROCESS CURRENT.
12. Scan the UI related to the first replenishment. 

K.Motion Enterprise 3PL Mobile User Guide 137
13. Enter the destination location. 
14. Enter the quantity available on pick location. 

138 K.Motion Enterprise 3PL Mobile User Guide
15. Scan the UI related to second replenishment. 
16. Enter the location. 
17. Enter the quantity. 
The Replenishment search screen or menu displays.

### Performing Inventory Counts on a Pick Line <a id="performing-inventory-counts-on-a-pick-line"></a>

You can perform an inventory count on a pick line after completing a replenishment (also called a replenishment countback) using the mobile device. To perform a replenishment countback, complete the following steps:
1. Navigate to the Replenishment search screen.

K.Motion Enterprise 3PL Mobile User Guide 139
2. Scan the UI or identify the order.
3. Tap F2:Choose Line.

140 K.Motion Enterprise 3PL Mobile User Guide
4. Scan the UI. 
5. Enter the quantity. 
6. Enter the TO LOC. 
7. Enter TIE. 
8. Enter HI. 
9. Enter LOOSE. 
10. Repeat previous steps until all records are complete.
The Replenishment search screen displays.

K.Motion Enterprise 3PL Mobile User Guide 141

### Cancelling a Replenishment with Supervisor Authorization <a id="cancelling-a-replenishment-with-supervisor-authorization"></a>

You can cancel a replenishment with supervisor approval. To cancel a replenishment of an inventory, complete the following steps:
1. Tap Outbound. 
2. Tap Replenishment. 
3. Click All. 
4. Tap F2:Execute query. 
5. Tap F5:Cancel Replen. 

142 K.Motion Enterprise 3PL Mobile User Guide
6. Enter Y to notify the supervisor.
7. Supervisor must enter Username and Password. 
Next replenishment record or search screen displays depending on available records.

### Process Value Out <a id="process-value-out"></a>

### Introduction <a id="introduction"></a>

When you access Add Values Out from the menu, it displays the Process Value Out search screen. 
Process Value Out allows you to enter or view process values on process codes associated with items on the outgoing order. 
You can search for order line(s) by entering the order number, the UI code, or the OPID associated with order lines.
For the order line to be available for processing, the following conditions apply:
• The order cannot be closed. 
• The order line must be in type “R” in the Finish (FIPI) flow. 
You can use the process in the following situations: 
• The process values on the process codes associated with an item are fully or partially missing 
• The process values on the process codes associated with an item have completed the entering. 
process, but need to reduce the inventory or remove the label on the inventory of the outgoing order. 
To enter process values, the system prompts you for information depending on the SKU class. If multiple process codes are associated with an item and their SKU types match, the system prompts for the first value on all process codes before prompting for the second process value. If the SKU types do not match, you must enter values for one process code at a time.
If an item on the order is configured to capture process values both ways via Inbound and Outbound and the order is allocated to a full pallet that exists in the warehouse, the system prompts you to transfer associated process values without the need to scan each one.
Serial number and weight are two of the most common process values entered. An item’s weight and its unit of measure are saved in the system according to the item quantity breakdown profile. If the 

K.Motion Enterprise 3PL Mobile User Guide 143 process code is configured by weight type and unit of measure, the system prompts you to select a unit of measure. The system currently supports kilograms and pounds.
Change Mode is available from the Process Value Out menu options and allows you to switch from pallets to cases or cases to pallets. This option is available when you are going through processes with weight discovery.
If the scanned parameter profile configuration exists, you can scan the barcode to capture process values. If the scanned parameter profile configuration has not been established or you are unable to scan the barcode, you have the option to enter process values manually. 
You can enter weight into the system manually or via the weight discovery process by scanning a barcoded label. To enter by using weight discovery, the following conditions apply:
• The length of every barcode must be the same.
• To continue scanning barcodes and extracting weight values, the system prompts you for the weight location for the first three times while scanning a series of barcodes. If all three barcodes have the same weight position after three scans, the system allows you to continue scanning barcodes and extracting the proper weight value out of the scanned barcode. If you encounter an error, follow the prompts and rescan.
When a barcode is scanned and all of the following criteria are met, the system automatically saves the process value for Serial Number:
• The weight and serial number process code is attached to the item.
• The SKU classes match for both process codes.
• The item process code type is equal to the Serial Number in Weight Barcode (SER). 
Note
If you encounter any errors, contact your supervisor.
1. When using weight as a process value, a tolerance may be configured. If the inventory weight is greater than or less than the configured tolerance percentage, the system rejects the weight and requires you to re-enter the weight.
2. After you enter the last process value on the last process code associated with an item on the last order line, the system accepts the value and displays the Process Value Out search screen. 

144 K.Motion Enterprise 3PL Mobile User Guide

### Process Value Out Tasks <a id="process-value-out-tasks"></a>

Access the Process Value Out search screen by completing the following steps and then proceed to the task you need to accomplish.
1. Tap Outbound > Add Values Out. 
2. Scan the order number, OPID, or UI to access the order record.
3. Tap F8:Next Record to find the appropriate record if needed.
4. Select from the following list to go to the task you want to complete:
• Viewing Process Values on a Process Code
• Adding a Process Value to an Item Manually
• Adding a Process Value Using Weight Discovery
• Adding a Process Value Using SCPR
• Adding a Process Value with Change Mode
• Reducing Cases
• Removing and Replacing a Label

### Viewing Process Values on a Process Code <a id="viewing-process-values-on-a-process-code"></a>

You can view or access process values on a process code. To view process code details, complete the following steps:
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Detail Process. 
A list of process codes that need process values displays. 
3. Tap to select the preferred process code from the list. 
The list of process values entered for the selected process code displays.
4. Tap F1:Cancel to return to the previous screen.

### Adding a Process Value to an Item Manually <a id="adding-a-process-value-to-an-item-manually"></a>

You can manually add a process value to an item. To add a process value to an item manually, complete the following steps:
1. Navigate to the Process Value Out search screen and access the appropriate record.

K.Motion Enterprise 3PL Mobile User Guide 145
2. Tap Order Lines. 
If configured, the unit of measure screen displays. If not, skip to the next step to enter the first process code.
Note
After selecting an order line, if an item on the order is configured to capture process values both ways from Inbound and Outbound and the order is allocated to a full pallet that exists in the warehouse, the system prompts you to transfer associated process values without the need to scan each one.
3. Tap the appropriate unit of measure.
4. Scan the first process value. 
5. Scan the second process value. 
Note
If process code is not configured to allow duplicate process values, the system prevents you from entering duplicate process values.
6. Continue until you scan all process code values for an item on the selected order line.

146 K.Motion Enterprise 3PL Mobile User Guide
7. Repeat steps for each additional order line to add process values.

### Assigning a Process Value Using Weight Discovery <a id="assigning-a-process-value-using-weight-discovery"></a>

If configured, you can use the Weight Discovery option to add process values. To assign a process value with weight discovery, complete the following steps:
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Order Lines. 
If configured, the unit of measure screen displays. If not, skip to the next step to enter the first process code.
3. Tap the appropriate unit of measure.

K.Motion Enterprise 3PL Mobile User Guide 147
4. Do one of the following:
a) Enter Y and proceed to Step 5.
b) Enter N for manual entry. Go to the section Assigning a Process Value to an Item Manually. 
5. Scan the appropriate barcode.
Note
If the serial process code is configured to be captured along with the weight barcode scan, the system does not prompt you to enter a serial number. 

148 K.Motion Enterprise 3PL Mobile User Guide
6. Enter the value that specifies the weight in the scanned barcode.
7. Repeat Steps 4 and 5 three times for the system to learn the weight values in the scanned barcode. 
8. Continue scanning barcodes until the last process value on the order line is complete.
Process Value Out search screen displays.

### Adding a Process Value using SCPR <a id="adding-a-process-value-using-scpr"></a>

You can add process values with Scan Parameter Profile configuration (SCPR). To add process values using SCPR, complete the following steps:
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Order Lines. 
If configured, the unit of measure screen displays. If not, skip to the next step to enter the first process code.

K.Motion Enterprise 3PL Mobile User Guide 149
3. Tap the appropriate unit of measure.
4. Scan the appropriate barcode.
Note
If you cannot scan the barcode, you can enter process values manually by tapping Manual 
Entry.
5. Continue scanning barcodes until the last process value on the order line is complete.
Process Value Out search screen displays.

### Adding a Process Value with Change Mode <a id="adding-a-process-value-with-change-mode"></a>

You can use the change mode option while adding process values to switch metric systems. To add a process value to an item with change mode, complete the following steps:

150 K.Motion Enterprise 3PL Mobile User Guide
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Order Lines. 
If configured, the unit of measure screen displays. If not, skip to the next step to enter the first process code.
Note
If an item on the order is configured to capture process values both ways via Inbound and 
Outbound and the order is allocated to a full pallet that exists in the warehouse, the system prompts you to transfer inbound process values.
3. Tap the appropriate unit of measure.

K.Motion Enterprise 3PL Mobile User Guide 151
4. Tap F12:Change Mode to switch from Pallet Mode to Case Mode.
5. Scan the first process value. 
Note
If all process codes associated with an item are configured with the same SKU class, the system continues prompting for values on all process codes in the sequence. If process codes associated with an item are configured with different SKU classes, the system prompts for process values for each process code separately.

152 K.Motion Enterprise 3PL Mobile User Guide
6. Scan the second process value. 
Note
If process code is not configured to allow duplicate process values, the system prevents you from entering duplicate process values for the item on the order line.
7. Continue until you scan all values for all process codes.
8. Repeat steps for each additional order line to add a process value.
Process Values Out search screen displays.

### Reducing Cases <a id="reducing-cases"></a>

You can reduce cases when process values are:
• Not Fully Scanned onto an Order Line
• Fully Scanned onto an Order Line
Not Fully Scanned onto an Order Line
You can reduce cases by reducing the labels that have already been scanned to an order line or remove the remaining quantity from an order line.
To reduce cases to an order line that has not been fully scanned, complete the following steps:
1. Navigate to the Process Value Out search screen and access the appropriate record.

K.Motion Enterprise 3PL Mobile User Guide 153
2. Tap Order Lines.
3. Tap F2:Reduce Cases.

154 K.Motion Enterprise 3PL Mobile User Guide
4. Enter Y. 
5. Do one of the following:
a) Scan the barcode.
Note
When reducing quantities by barcode scanning, you can only scan one barcode at a time. 
You must repeat this step if you need to scan multiple barcodes.
6. Tap F2:Reduce Quantity. 
7. Repeat steps until all required process values are reduced.
Fully Scanned onto an Order Line
You can reduce cases when all process values have been scanned onto an order line. To reduce scanned cases from fully scanned order lines, complete the following steps:

K.Motion Enterprise 3PL Mobile User Guide 155
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Order Lines. 
3. Enter Y. 
4. Scan the barcode to reduce the quantity from the order line.

### Removing and Replacing a Label <a id="removing-and-replacing-a-label"></a>

You can remove and replace a label from the Process Value Out search screen. To replace a previously entered process value from an item on an order line, complete the following steps: 
1. Navigate to the Process Value Out search screen and access the appropriate record.
2. Tap Order Lines. 
3. Scan the process value you want to remove. 
Note
You can only remove and replace a label if you are adding process values to an item. Once process value entries are complete, you cannot replace a label with this process.
4. Tap F3:Remove Label. 

156 K.Motion Enterprise 3PL Mobile User Guide
5. Enter Y. 
6. Scan barcode to remove. 
Note
You must enter a new process value to replace the previously removed process value.
7. Continue entering or scanning the remaining process values for all process codes on the Order 
Line.

### Extra Charges Out <a id="extra-charges-out"></a>

### Introduction <a id="introduction"></a>

Extra Charges Out allows you to apply extra charges to a customer’s order per the charge code profile set up in the system.
To apply extra charges to an order or order line, the following conditions apply:
• The order cannot already be completed. You can only apply extra charges when the order is in the following statuses:
− Start Picking (STPI)
− Finish Picking (FIPI)
− Start Unloading (STLO)
− Finish Unloading (FNLO)
If the Line number in the Order/Line field is “0,” the system applies the extra charges to the order itself. If the Line number in the Order/Line field is “1” or more, the system applies the extra charges to the applicable order line.
The order of information may differ, but the system generally displays the following information as you advance through the pages of the record: 
• Charge Record Number (For example: 1 out of 5)
• Order/Line Number
• Charge Code
• Description
• Quantity

K.Motion Enterprise 3PL Mobile User Guide 157
1. To review the details of a receipt, tap Receipt Detail. You can select this option from any charge record screen.

### Extra Charges Out Tasks <a id="extra-charges-out-tasks"></a>

Access the Extra Charges Out search screen by completing the following steps and then proceed to the task you need to accomplish.
1. Tap Outbound > Extra Charges Out. 
2. Scan the order. 
3. Select from the following list to go to the task you want to complete:
• Applying Extra Charges
• Editing Extra Charges

### Applying Extra Charges <a id="applying-extra-charges"></a>

You can apply extra charges to an order from Extra Charges Out. To apply the quantity of extra charges, complete the following steps: 
1. Navigate to the Extra Charges Out search screen.
2. Find and access the charge record to apply extra charges.
3. Apply the charge quantity in the NEW QTY field. 
The system displays the charge quantity on the QTY line.
4. Repeat steps until you have applied the quantity to all applicable charge records on the order.
5. Tap F1:Cancel to return to the Extra Charges Out search screen.

### Editing Extra Charges <a id="editing-extra-charges"></a>

2. You can edit extra charges from Extra Charges Out. To edit the quantity of extra charges, complete the following steps:
1. Navigate to the Extra Charges Out search screen.
2. Find and access the charge record to edit extra charges.
3. Edit the charge quantity in the NEW QTY field. 
The system displays the edited charge quantity on the QTY line.

158 K.Motion Enterprise 3PL Mobile User Guide
4. Repeat steps until you have edited the quantity of all applicable charge records on the order.
5. Tap F1:Cancel to return to the Extra Charges Out search screen.

### Loading <a id="loading"></a>

### Introduction <a id="introduction"></a>

After an order is picked, it must be loaded from the staging location to the truck/trailer to leave the warehouse. The Loading option allows you to assign loads to specific doors in the warehouse. Stops are used to sequence the load in a logical order. Orders must be loaded in reverse stops sequence. 
If a product is damaged or cannot be shipped, you can still unload it from a load and assign it to another load or return it to the warehouse.
To load an order, the following conditions apply:
• Orders on the load must be picked
• The load status must be set to Ready to Load
• The load cannot be locked
Supervisor authorization is required when you attempt to load a mismatched quantity or in the case of an unsettled inventory count where the order line is under investigation. For more information on supervisor authorization, see Supervisor Alerts. 

### Loading Tasks <a id="loading-tasks"></a>

You can perform the following tasks from the Loading menu option:
• Loading an Order
• Authorizing Unsettled Inventory Count with Supervisor Authorization

### Loading an Order <a id="loading-an-order"></a>

You can load orders from the Outbound Loading menu. To load an order, complete the following steps:
1. Tap Outbound > Loading. 

K.Motion Enterprise 3PL Mobile User Guide 159
2. Scan the load label or enter a load identifier. 
3. Tap to select LookUp Load or LookUp Door. 
Note
This step is optional and only displays if the value entered on previous screens match to 
LookUp Load or LookUp Door values.
4. Scan the OPID or UI. 
5. Do one of the following:
a) If multiple order lines have the same UI code, the tap the appropriate order line and go to 
Step 8. 
b) If multiple order lines have unique UI codes, then go to Step 9. 
6. Tap Confirm. 

160 K.Motion Enterprise 3PL Mobile User Guide
7. Scan the door attached to the load.
8. Tap F10:OK.
9. Repeat steps until all order lines are loaded for additional stops.

K.Motion Enterprise 3PL Mobile User Guide 161

### Authorizing Unsettled Inventory Count with Supervisor Authorization <a id="authorizing-unsettled-inventory-count-with-supervisor-authorization"></a>

You can authorize unsettled inventory counts with supervisor approval. To complete a supervisor authorization when an inventory count is unsettled, complete the following steps:
1. Tap Outbound > Loading. 
2. Scan the load number. 

162 K.Motion Enterprise 3PL Mobile User Guide
3. Scan the OPID or UI. 
4. If the user is a supervisor, enter one of the following responses:
a) N—Back to Enter OPID. 
b) Y—Proceed through transaction. 
5. If the user is not a supervisor, enter one of the following responses:
a) N—Back to Enter OPID. 
b) Y—Move to supervisor prompt and a supervisor notification is generated. 

K.Motion Enterprise 3PL Mobile User Guide 163
6. Enter the supervisor username. 
7. Enter the password. 
8. Enter one of the following responses:
a) N—Back to OPID. 
b) Y—Proceeds through transaction. 

### Carton Sorting <a id="carton-sorting"></a>

### Introduction <a id="introduction"></a>

Carton Sorting allows you to sort product on an outbound order and manually assign a carton ID to the carton containing inventory. A carton may only contain product from a single order. K.Motion 
Enterprise 3PL does not validate manually assigned carton IDs. 

164 K.Motion Enterprise 3PL Mobile User Guide
For the order line to be available for cartonization, order must be in the Finish Picking (FIPI) status.
The manual cartonization process allows inventory on Order Lines that have been picked to be cartonized in individual cartons or cartonized within same carton for the entire order. 
The order of information may differ, but the following information generally displays as you advance through the pages of the record: 
• Order 
• Customer 
• Consignee
• Carton Size
• Quality 
• Units of Measure 
• Length 
• Width 
• Carton ID 
• Height 
• Item Code 
• Gross Weight 

### Process Overview <a id="process-overview"></a>

To start the carton sorting process, search for an order number or outbound pallet ID (OPID) that has been assigned to an order line during the picking process. The picking process supports one OPID associated with multiple order lines across multiple orders. If one OPID is associated with multiple order lines across multiple orders, the system displays a list of orders to choose from that are associated with the OPID. 
As you are working with the cartonization process, consider the following:
After you begin the cartonization process, you must close the current carton before you can move to another task. 
You may need to remove a carton. When you remove a carton, the inventory within that carton is no longer associated with the carton; however, it remains on the order and must be repacked.
If you need to remove a carton on an order and cartonization is in process, select the Carton ID from the list of available cartons or scan/enter the appropriate Carton ID on the order.

### Configuration Options <a id="configuration-options"></a>

As part of customer and item profile set up, the system may be configured to automatically populate information during the manual cartonization process, or the system may display additional prompts.
1. Entering Carton ID
• If configured, the system generates the Carton ID and populates the Carton ID in the Carton ID prompt.
• If not configured, the system does not generate Carton ID and you must need scan the Carton ID.
2. Entering Item Number and Quantity
• If configured, you must enter Item Levels. 
• If configured, you must scan each Item Quantity. 
3. Closing the Carton

K.Motion Enterprise 3PL Mobile User Guide 165
• If configured to change the carton cubic dimensions, you are allowed to enter the carton dimensions and carton weight considering item weight. 
• If configured to only enter the weight, you are allowed to enter the carton weight considering item weight. 
3. Viewing Messages and Remarks
• If Customer, Consignee Carrier, or Item are configured with Messages and the Order header or 
Order line has associated Remarks, the system displays the messages and remarks before you enter the carton details
• Any time you enter an item number or quantity, the Remarks button is available to view associated remarks and messages.

### Carton Sorting Tasks <a id="carton-sorting-tasks"></a>

Access the Cartonization search screen by completing the following steps and then proceed to the task you need to accomplish.
1. Tap Outbound > Carton Sorting. 
2. Scan the order number or OPID to access the order record.
3. Tap F8:Next Record to find the appropriate record if needed.
4. Select from the following list to go to the task you want to complete:
a) Completing Manual Cartonization
b) Removing a Carton
c) Reopening a Carton

### Completing Manual Cartonization <a id="completing-manual-cartonization"></a>

You can manually cartonize orders from Carton Sorting. To manually cartonize an order, complete the following steps:

166 K.Motion Enterprise 3PL Mobile User Guide
1. Navigate to the Cartonization search screen and locate the appropriate record.
2. Enter the Carton Size.

K.Motion Enterprise 3PL Mobile User Guide 167
4. Scan the Carton ID. 
Note
If you want to use the carton previously used in the same order line or a different order line of the same order, scan the appropriate Carton ID or select the appropriate Carton ID from the 
Carton List.
5. Enter the item number. 
6. Enter the quantity. 
7. Tap F3:Close Carton. 
8. Enter the printer code. 
9. Enter a Carton Size to pack the remaining quantity on the order. When complete, tap F10:OK. 

### Removing a Carton <a id="removing-a-carton"></a>

After you add a carton to an order, you may need to remove the carton. When you remove a carton, the inventory within that carton is no longer associated with the carton; however, it remains on the order and must be repacked.
To remove a carton from an order, complete the following steps:
1. Navigate to the Cartonization search screen. 
2. Enter Y. 
3. Scan a Carton ID. 
4. Tap F5:Remove. 
5. Enter the carton size. 
6. Enter the appropriate Carton ID to repack the inventory or accept system generated Carton ID.

### Reopening a Carton <a id="reopening-a-carton"></a>

After you add a carton to an order, you may need to reopen the carton. When you reopen a carton, the carton remains on the order. You can adjust the inventory by adding or removing the inventory and reclosing the carton.
To reopen a carton from an order, complete the following steps:
1. Navigate to the Cartonization search screen. 

168 K.Motion Enterprise 3PL Mobile User Guide
2. Enter Y. 
3. Scan a Carton ID. 
4. Tap F4:Re-Open. 
5. Enter an item. 
6. Enter the appropriate quantity. 
7. Tap F3:Close Carton. 

### Merging Pallets <a id="merging-pallets"></a>

### Introduction <a id="introduction"></a>

The Merging Pallets process allows you to merge two or more Outbound Pallet IDs (OPIDs). During the process, you enter the source OPID or UI to be merged with another OPID. When you successfully finish merging pallets, the source OPID is replaced with a newly generated destination 
OPID or an existing destination OPID.
Before you can merge two outbound pallets, you must obtain a validated source OPID or a source UI along with a validated destination OPID.
Consider the following before merging pallets:
• The source and destination OPIDs must be at the same staging location
• The source and destination OPIDs cannot be the same
• You cannot merge OPIDs that have already been loaded
• Order lines cannot be merged if the status is confirmed
• Unsettled counts must be settled 
• Product must be picked from the same location
• Hazardous products cannot be merged with non-hazardous products
You can merge an OPID to another order by moving the full or partial quantity of an existing OPID to another OPID on a different order. The merged product must be on the same load and assigned to the same stop and group.

K.Motion Enterprise 3PL Mobile User Guide 169

### Merging OPID and UI into a Single Pallet <a id="merging-opid-and-ui-into-a-single-pallet"></a>

1. To merge an OPID and UI into a single pallet, complete the following steps: Tap Outbound >
2. Scan the source OPID or UI to merge.
Note
If more than one order line record is associated with the entered OPID or UI, you must navigate through the available records and select the correct order line to merge.
3. Enter an order line quantity value.
4. Enter the destination OPID.
5. Do one of the following:
a) If the system accepts the destination OPID, then confirm the pallet merge.
b) If the destination OPID is new and you want to create it, the enter Yes and confirm the pallet merge.
c) If the destination OPID is new and you want to create a different OPID, the enter No, enter the new OPID, and confirm the pallet merge. 
Note
If the entered destination OPID matches the Carton ID in the system, an error displays and the system does not accept the entered destination OPID.
6. Tap Confirm to complete the merge. 

### Relocating Pallets <a id="relocating-pallets"></a>

### Introduction <a id="introduction"></a>

Relocating pallets of product on an order line allows you to relocate inventory on an outbound order. 
To perform this program: 
• Product must be picked and assigned an outbound pallet ID in a picking program before it can be moved. 
• Product cannot be moved from a door location. 

170 K.Motion Enterprise 3PL Mobile User Guide
• Order line must be picked in a picking program using Case Picking mode before it can be relocated in Relocating Pallets. 
• If multiple OPIDs are loaded, all outbound pallet IDs are moved to a new location as a single action. 
• Validation for quantity or location can be configured using MRFP parameters. 
There are five configurations for Relocating Pallets that can be set up in the system.
Configuration Description
Allow Multiple Pallet Moves Specifies if the operator can relocate multiple pallets in a single step from the Relocating Pallets field. 
Location Type of To Location Specifies if the To location must be a staging location, pick location, or any location from the Order Move field. 
Suggested Location Rules Defines the suggested or default to location from the Relocating 
Pallets field.
Validate From Location Specifies if the operator must enter the from location of the product being moved from the Order Move field.
Validate Quantity Specifies if the operator must enter the quantity being moved from the Order Move field.

### Relocating a Pallet on an Order Line to a Different Staging Location <a id="relocating-a-pallet-on-an-order-line-to-a-different-staging-location"></a>

You can move pallets on an order line to different staging locations from the Outbound menu. To relocate a pallet to a different staging location, complete the following steps:
1. Tap Outbound. 

K.Motion Enterprise 3PL Mobile User Guide 171
2. Tap Relocating Pallets. 
3. Scan OPID or UI. 
Note
You cannot move an OPID or UI from a door location. 

172 K.Motion Enterprise 3PL Mobile User Guide
4. Tap F3:Destination. 
5. Enter a staging location.
Relocate OPID screen displays, and quantity loaded is zero.
Note
An error message will display if you enter an invalid staging location.

K.Motion Enterprise 3PL Mobile User Guide 173

### Inventory <a id="inventory"></a>

### Introduction <a id="introduction"></a>

The inventory processes allow you to adjust and relocate inventory and add inventory attributes to items in the warehouse. From the inventory menu, you can select from the following options to complete various tasks within each: 
• Inventory Relocation
• Hold Adjustments
• Add Inventory Attributes

### Inventory Relocation <a id="inventory-relocation"></a>

The inventory relocation process allows you to perform a partial or full relocation on warehouse inventory. You can relocate multiple inventories in a single transaction from the summary page.
To relocate inventory, the following conditions must be met:
• The inventory is not on order
• The Warehouse, Company Code, Location, and Customer match
• The Location and Warehouse Code exist in the system
The order of information may differ, but following information generally displays as you advance through the pages of the record: 
• Warehouse Code
• Company Code
• Item Code
• Location
• Available Stock (AV)

174 K.Motion Enterprise 3PL Mobile User Guide
• On Hand Quantity (AH)
• On Order (ORD)
• On Hold (HLD)
• Hold Code
Supervisor authorization is required when you attempt to relocate inventory to a location that is different from the suggested location. For more information on supervisor authorization, see 

### Inventory Relocation Tasks <a id="inventory-relocation-tasks"></a>

You can perform the following tasks from the Relocating menu option:
• Fully Relocating Inventory
• Partially Relocating Inventory
• Relocating Inventory to Any Suggested Location
• Relocating Inventory to a Different Location with Supervisor Approval

### Fully Relocating Inventory <a id="fully-relocating-inventory"></a>

You can relocate inventory using the mobile device. To fully relocate inventory, complete the following steps:
1. Tap Inventory > Relocating. 
2. Find and access the inventory record to relocate.

K.Motion Enterprise 3PL Mobile User Guide 175
3. Tap Relocate. 
4. Scan the destination. 
Note
The Destination location must be within the same Warehouse and Company.

176 K.Motion Enterprise 3PL Mobile User Guide
5. Tap Confirm. 
6. Tap OK. 
The Relocating Inventory search screen displays.

### Partially Relocating Inventory <a id="partially-relocating-inventory"></a>

You can relocate partial inventory from the mobile device. To partially relocate inventory, complete the following steps:
1. Tap Inventory > Relocating. 
The Relocating Inventory search screen displays with the number of inventory records on the 
Entities line.
2. Find and access the inventory record to partially relocate.

K.Motion Enterprise 3PL Mobile User Guide 177
3. Tap F2:Relocate.
4. Tap F4:Partial QTY.

178 K.Motion Enterprise 3PL Mobile User Guide
5. Enter the preferred quantity. 
6. Enter the destination. 

K.Motion Enterprise 3PL Mobile User Guide 179
7. Tap F2:Confirm. 
8. Tap F10:OK. 
The Relocating Inventory search screen displays.

### Relocating Inventory to Any Suggested Location <a id="relocating-inventory-to-any-suggested-location"></a>

To relocate inventory to any suggested location, complete the following steps: 
1. Tap Inventory. 

180 K.Motion Enterprise 3PL Mobile User Guide
2. Tap Relocating
3. Tap F2:Excecute Query. 

K.Motion Enterprise 3PL Mobile User Guide 181
4. Tap F8:Next Record.
5. Tap F2:Relocate. 

182 K.Motion Enterprise 3PL Mobile User Guide
6. Tap F3:Next Loc. 
Note
If you do not want to relocate inventory to the location listed, you can press F3 and the system will provide a given number of location options. 
7. Tap F3:Next Loc. 

K.Motion Enterprise 3PL Mobile User Guide 183
8. Tap F3:Next Loc. 
9. Enter N. 

184 K.Motion Enterprise 3PL Mobile User Guide
10. Enter a location.
11. Tap F2:Confirm. 
12. Tap F10:OK. 

### Relocating Inventory to a Different Location with Supervisor Approval <a id="relocating-inventory-to-a-different-location-with-supervisor-approval"></a>

You can move inventory to different locations when needed. To complete a relocation of an inventory to a different location than the suggested location with supervisor approval, complete the following steps:

K.Motion Enterprise 3PL Mobile User Guide 185
1. Tap Inventory. 
2. Tap Relocating. 

186 K.Motion Enterprise 3PL Mobile User Guide
3. Tap F2:Execute Query. 
4. Tap F8:Next Record to find the inventory to relocate.

K.Motion Enterprise 3PL Mobile User Guide 187
5. Tap F2:Relocate.
6. Enter a different location other than suggested.

188 K.Motion Enterprise 3PL Mobile User Guide
7. Enter Y and locate supervisor to provide credentials.
8. Supervisor must enter credentials and password.

K.Motion Enterprise 3PL Mobile User Guide 189
9. Tap F2: Confirm. 
10. Tap F10:Ok. 

### Hold Adjustments <a id="hold-adjustments"></a>

### Introduction <a id="introduction"></a>

The hold adjustment process allows you to add a hold to or remove a hold from an inventory item. 
You can place a hold on an item for some of the following reasons:
• Inventory discrepancies
• Inventory damages
• Safety concerns
• Manufacturer regulations
The order of information may differ, but the following information generally displays as you advance through the pages of the record: 
• Warehouse Code
• Customer Code
• Item Code
• Location
• Available Stock (AV)
• On Hand (AH)
• On Order (ORD)
• On Hold (HLD)
When you are applying a hold on multiple records, keep in mind:
• The Order QTY must equal 0
• All inventory items must be in the same Location, Warehouse, Customer Code, and Company
• Inventory items are not already allocated to the order

190 K.Motion Enterprise 3PL Mobile User Guide
When you are removing a hold on multiple records, the conditions above apply and the Location and 
Warehouse codes must exist in the system.
A Transaction Complete confirmation message displays after applying, changing, or removing a hold. 

### Applying/Changing a Hold <a id="applying-changing-a-hold"></a>

You can add or change a hold from the Hold Adjustments menu. To apply/change a hold to an inventory record, complete the following steps:
1. Tap Inventory > Hold Adjustment. 
2. Scan the inventory record. 

K.Motion Enterprise 3PL Mobile User Guide 191
3. Tap F2:Adj Code. 
Note
If an asterisk displays next to the Hold label, there is no hold on that inventory item.
4. Enter the hold code.

192 K.Motion Enterprise 3PL Mobile User Guide
5. Tap F2:Confirm to confirm the hold code.
Transaction Complete confirmation message and new hold adjustment number displays.
6. Tap F10:OK. 
The Hold Adjustments search screen displays.

### Removing a Hold <a id="removing-a-hold"></a>

You can remove a hold from a record with the mobile device. To remove a hold from an inventory record, complete the following steps:
1. Tap Inventory > Hold Adjustment.
2. Scan the inventory record. 
3. Tap F2:Adj Code. 
Note
If a hold code displays next to the Hold label, it indicates there is a hold on the inventory record.

K.Motion Enterprise 3PL Mobile User Guide 193
4. Leave empty and tap Submit. 
5. Tap F2:Confirm. 
Transaction Complete confirmation message and new hold adjustment number displays.
Note
If you remove the hold code for multiple inventory entities from the summary screen and those entities have different hold codes, a blank field displays.
7. Tap F10:OK. 
The Hold Adjustments search screen displays.

194 K.Motion Enterprise 3PL Mobile User Guide

### Add Inventory Attributes <a id="add-inventory-attributes"></a>

### Introduction <a id="introduction"></a>

The adding inventory attributes process allows you to add more details to an item in the warehouse. 
You can attach attributes to an item or an item’s inventory. 
To add inventory attributes to an item, the following conditions apply:
• Item must exist
• An Inventory Attribute Profile must be set up and attached to the item
• Inventory for the item must exist in the warehouse

### Adding Inventory Attributes <a id="adding-inventory-attributes"></a>

To add attributes to inventory, complete the following steps:
1. Tap Inventory. 
2. Tap Adding Attributes. 
3. Scan the UI code. 
Note
If more than one inventory records are associated with the scanned UI, select the appropriate record and tap Select. 
4. Enter an attribute value or tap Value List to select the attribute from the list.
5. Continue adding attributes for the scanned UI code as needed.

K.Motion Enterprise 3PL Mobile User Guide 195

### Look Ups <a id="look-ups"></a>

### Introduction <a id="introduction"></a>

The Look Ups Menu allows you to search for and view inventory, processes, and data. You can use the following look up programs from the menu:
• Inventory
• Receipts
• Orders
• Outbound Pallet

### Look Up Inventory <a id="look-up-inventory"></a>

The look up inventory process allows you to view detailed information about inventory entities. You can perform an inventory look up using the following search criteria:
• Customer Code
• Warehouse Code
• Location
• Item Code
• Levels 2, 3, or 4 (L2-L4)
• Hold Code
• Unique Identifier (UI)
Note
The UI is a value that represents the highest level assigned to an inventory entity. UI varies across items. 

196 K.Motion Enterprise 3PL Mobile User Guide
4. After entering the search criteria, a summarized overview of the inventory entity displays the total quantities for:
• Available Quantity (AV)
• On Hand Quantity (OH)
• On Order Quantity (ORD)
• Hold Quantity (HLD)
5. You can browse a list of all inventory entities and view the details. The following information displays as you advance through the pages of the inventory entity record.
• Item Code
• Customer Code
• Location
• Warehouse Code
• Item Code
• Level 2 Code
• Level 3 Code
• Level 4 Code
• Available Quantity (AV)
• On Hand Quantity (OH)
• On Order Quantity (ORD)
• Hold Quantity (HLD)

### Looking Up Inventory <a id="looking-up-inventory"></a>

To look up inventory, complete the following steps:
1. Tap Look Ups. 
2. Tap Inventory. 
The Lookup Inventory search screen displays with the number of inventory records on the Entities line.
3. Find and access the inventory record you want to look up.

K.Motion Enterprise 3PL Mobile User Guide 197
4. Tap F6:Next Page to navigate through the record as needed.
5. Tap F1:Cancel to return to the Lookup Inventory search screen.

### Look Up Receipt <a id="look-up-receipt"></a>

### Introduction <a id="introduction"></a>

The look up receipt process allows you to view detailed information about a receipt, receipt lines, and their inventory locations.
You can perform a receipt look up using the following search criteria:
• Customer Code
• Warehouse Code
• Receipt Code Process Flow
• Receipt Number
• Receipt Probill Number
• Receipt Reference
• Receipt Alternate Reference 1
• Receipt Alternate Reference 2
6. After entering the search criteria, a summarized overview of the receipts displays showing the summarized number of:
• Receipt lines
• Advised receipt lines
• Staged receipt lines
• Stored receipt lines
7. The following information displays as you advance through the pages of the receipt record:
• Receipt Number 
• Number of Lines 
• Flow 

198 K.Motion Enterprise 3PL Mobile User Guide
• Customer 
• Type 
• Rate 
• Priority 
• Reference Numbers
• Probill Number 
• Shipping 
• Carrier 
• Bill To 
• Purchase Order Number 
• Created Date 
• Entered Date 
• Expected Date 
• Received Date 
• Warehouse 
8. For each receipt, you can browse the receipt lines. The following information displays per receipt line:
• Receipt number
• Receipt line number
• Line Type
• Item Code
• Expected Quantity
• Received Quantity
• Hold Code
• Level 2 Code
• Level 3 Code
• Level 4 Code
9. You can browse the receipt line-locations. Per receipt line location, the following information displays:
• Receipt number
• Receipt line number
• Location 
• Warehouse
• Item Code
• Level 2 Code
• Level 3 Code
• Level 4 Code
• Quantity
• Hold Code

### Looking Up Receipts <a id="looking-up-receipts"></a>

Look up a receipt to view all available information about an order. To look up a receipt, complete the following steps:

K.Motion Enterprise 3PL Mobile User Guide 199
1. Tap Look Ups.
2. Tap Receipt.
The Lookup Receipt search screen displays with the number of receipts on the Receipts line.
3. Find and access the receipt record.
4. Tap F6:Next Page to navigate through the record as needed.
5. Tap F2:Receipt Lines to review receipt line details.
6. Tap F2:Show Inventory to review location details.
7. Tap F10:OK or F1:Cancel to return to the Lookup Receipt search screen.

200 K.Motion Enterprise 3PL Mobile User Guide

### Look Up Orders <a id="look-up-orders"></a>

### Introduction <a id="introduction"></a>

The look up order process allows you to view detailed information about an order, order lines, and their locations.
You can perform an order look up using the following search criteria:
• Customer Code
• Warehouse Code
• Order Number
• Carrier Code
• Customer Order Number
• Order Flow Process Code
• Order Reference 1
• Order Reference 2
10. After entering the search criteria, a summarized overview of the order displays showing the summarized number of:
• Order lines
• Case pick lines
• Pallet pick lines
• Pick quantity
11. The following information displays as you advance through the pages of the order record:
• Order Number 
• Number of Pallet Pick Lines 
• Number of Case Pick Lines 
• Destination 
• Warehouse 

K.Motion Enterprise 3PL Mobile User Guide 201
• Customer 
• Flow 
• Customer Order Number 
• Expected Ship Date 
• Consignee 
• Carrier 
• Priority 
• Purchase Order 
• Sold To 
• To Ship Date 
• Ship Date 
• Loc St
• Doc St
• Reference Number 
12. For each order, you can browse the order lines. Each order line the system shows the following information:
• Order number
• Order line number
• Line Type
• Item Code
• Order Quantity
• Ship Quantity
• Level 2 Code
• Level 3 Code
• Level 4 Code
13. You can browse the order line-locations. The following information displays each order line location:
• Order number
• Order line number
• Order location line number 
• Location
• Item Code
• Level 2 Code
• Level 3 Code
• Level 4 Code
• Hold Code
• Quantity
• OPID

### Looking Up Orders <a id="looking-up-orders"></a>

You can look up an order to view all available information about its status. To look up an order, complete the following steps:
1. Tap Look Ups. 

202 K.Motion Enterprise 3PL Mobile User Guide
2. Tap Order. 
The Lookup Order search screen displays with the number of orders on the Orders line.
3. Find and access the order record you want to look up.
4. Tap F6:Next Page to navigate through the record as needed.
5. Tap Order Lines to review order line details.
6. Tap F2:Show Inventory to review location details.
7. Tap F1:Cancel to return to the main screen.

### Look Up Outbound Pallet <a id="look-up-outbound-pallet"></a>

### Introduction <a id="introduction"></a>

The look up outbound pallet (OPID) process allows you to view detailed outbound pallet information.
14. You can perform an OPID look up using the following search criteria:
• OPID
• Order Number
• Location Code
15. The following information displays as you advance through the pages of the order record:
• Location 
• Warehouse 
• Outbound Pallet ID (OPID)
• Order Number 
• Order Line 
• Customer 
• Order Flow 
• Line Flow 
• Item Code 
• Level Code 2 
• Level Code 3

K.Motion Enterprise 3PL Mobile User Guide 203
• Level Code 4 
• Quantity 
• Quantity Breakdown (BD)
• Purchase Order Number 
• Consignee 
• Carrier 

### Looking Up Outbound Pallet Inventory <a id="looking-up-outbound-pallet-inventory"></a>

To look up outbound pallet inventory details, complete the following steps:
1. Tap Lookups. 
2. Tap Outbound Pallet. 
The Lookup OPID search screen displays with the inventory line count.
3. Find and access the inventory record you want to look up.
4. Tap F6:Next Page to navigate through the record as needed.
5. Tap F1:Cancel to return to the main screen.

204 K.Motion Enterprise 3PL Mobile User Guide

### Task Interleaving <a id="task-interleaving"></a>

### Introduction <a id="introduction"></a>

Task Interleaving uses interleave groups to determine how to assign work and the types of work to interleave for each interleave group. Task Interleaving is set up at the Work Queue level so each process in the interleave group is completed before the next one begins. Task Interleaving groups containing work that is assigned based on pick area will prompt for pick area for each work type that requires a pick area.
To use Interleaving on your mobile device:
• Orders can be allocated through Wave Manager or LOOR.
• The RF operator must be set up in RFOP and REGI must be configured.
• The pallet build assignment is performed by Wave Manager during allocation.
If an RF operator chooses to skip a task, K.Motion Enterprise 3PL records the skipped task and the operator who skipped it. The task will not display again in the current RF session.
Task interleaving allows you to optimize the distribution of work in your warehouse to ensure urgent work is performed first, congestion in warehouse aisles and zones is avoided whenever possible, and the discretion of individual RF operators to pick and choose their own work is reduced to a minimum.
To reduce the amount of time spent by RF operators entering individual RF programs such as Picking or Replenishments to pick entire order lines and perform replenishments at their own pace and in a sequence that does not consider the work of other RF operators, they enter a single program, Task 
Interleaving, to work on their first assigned task. 
Task Interleaving supports all the standard functions performed in the following programs:
• Inbound Put-Away
• Relocating Outbound Pallets
• Relocating Inventory
• Replenishment
Supervisor authorization is required when you attempt to relocate inventory or multiple pallets to a different location than what is suggested. For more information on this topic, see Supervisor Alerts. 
When supervisor approval is required through Relocating Pallets, RF operators can select from the following choices when Relocate OPID screen displays:
Type Description
Suspend Task Sends notification to supervisor and requires supervisor username and password. Once entered, the record updates and is cleared.
Continue Task Returns you to the same place in the task
Exit Task Exits Relocating Pallets and goes back to Interleaving region prompt.
Note
Option is only available for supervisor operators. 

K.Motion Enterprise 3PL Mobile User Guide 205

### Task Interleaving Tasks <a id="task-interleaving-tasks"></a>

You can complete the following tasks from the Task Interleaving menu option:
• Performing Put-Away from Task Interleaving
• Completing Replenishment with Task Interleaving
• Relocating Inventory with Task Interleaving and Supervisor Approval
• Relocating Pallets with Task Interleaving

### Performing Put-Away from Task Interleaving <a id="performing-put-away-from-task-interleaving"></a>

You can put away single or mixed pallet of a receipt line from Task Interleaving process. To complete one-step put-away, complete the following steps:
1. Tap Task Interleaving. 

206 K.Motion Enterprise 3PL Mobile User Guide
2. Tap F2:Select Region. 
3. Enter Y. 
Note
This step is optional and only displays with a mixed pallet.
4. Tap F10:OK. 

K.Motion Enterprise 3PL Mobile User Guide 207
5. Enter the location. 
6. Tap F2:Confirm. 
7. Tap F10:OK. 

208 K.Motion Enterprise 3PL Mobile User Guide

### Completing Replenishment with Task Interleaving <a id="completing-replenishment-with-task-interleaving"></a>

You can perform replenishment through Task Interleaving. To complete a replenishment task with 
Task Interleaving, complete following next steps:
1. Tap Task Interleaving. 
2. Tap F2: Select Region. 

K.Motion Enterprise 3PL Mobile User Guide 209
3. Tap F2:Choose Line.
4. Scan the UI.

210 K.Motion Enterprise 3PL Mobile User Guide
5. Enter the quantity. 
6. Enter the destination into the TO LOC field. 
Replenishment task is complete and Task Interleaving screen with region that RF Operation belongs to displays. 
Relocating Inventory with Task Interleaving and Supervisor 
Approval 
You can relocate inventory from Task Interleaving. When you need to relocated inventory to a different location than prompted, you will need supervisor authorization. To relocate inventory with task interleaving and supervisor approval, complete the following steps:
1. Tap Task Interleaving. 

K.Motion Enterprise 3PL Mobile User Guide 211
2. Tap F2:Select Region.
3. Scan location.

212 K.Motion Enterprise 3PL Mobile User Guide
4. Scan the UI.
5. Enter the quantity.

K.Motion Enterprise 3PL Mobile User Guide 213
6. Do one of the following:
a) Enter the provided location to relocate the inventory.
Transaction is complete, and the system returns to Task Interleaving region screen.
b) Enter a different location to relocate the inventory and go to step 7.
7. Do one of the following:
c) Enter N to ignore notification to supervisor.
The system goes back to the TO LOC screen.
d) Enter Y to send supervisor a notification to authorize relocation to a different destination and go to step 8.

214 K.Motion Enterprise 3PL Mobile User Guide
8. Supervisor must enter username and password.
Note
For more information on supervisor authorizations, see Supervisor Alerts. 
9. Do one of the following:
e) Enter N to reject relocation.
The system goes back to the TO LOC screen.
f) Enter Y to continue relocation.
Transaction is complete, and the system returns to Task Interleaving region screen.

### Relocating Pallets with Task Interleaving <a id="relocating-pallets-with-task-interleaving"></a>

You can relocate pallets from Task Interleaving. To relocate pallets with task interleaving, complete the following steps:
1. Tap Task Interleaving. 

K.Motion Enterprise 3PL Mobile User Guide 215
2. Tap F2:Select Region and locate the appropriate record.
3. Scan OPID.

216 K.Motion Enterprise 3PL Mobile User Guide
4. Scan location to move OPID.
The next task displays when more than one task exist.

K.Motion Enterprise 3PL Mobile User Guide 217

### Supervisor Alerts <a id="supervisor-alerts"></a>

### Introduction <a id="introduction"></a>

When a non-supervisor performs an action that requires supervisor approval, the system generates an automatic email notification and sends it to a group email address for supervisors. The email provides a summary of the problem and identify the location. 
A supervisor operator can search alerts from Supervisor Alerts to review notifications requiring approval. While searching, there is an option to apply additional filters based on the process area.
Supervisor Alerts allows you to look up and accept overrides from the following programs:
• Unloading (RFCH)
• Put-Away (RFPU)
• Default Picking (RFPIC)
• Outbound Loading (OLOP)
• Relocation (RFRL)
When an override is accepted, it is deleted and can no longer be accessed.
The following actions trigger email notifications and the creation of an override record in RFSUN when a non-supervisory RF operator:
• Creates a new receipt line in RFCH
• Overrides a suggested put-away location in RFPU
• Records a variance for the put-away quantity in RFPU
• Places product on suspend hold in RFPIC
• Enters a countback quantity in RFPIC that does not match the system quantity
• Enters a loading quantity in OLOP that does not match the system quantity
• Places product on hold in RFRL
You can search notices by:
• Receipt or Order Number
• Created or Accepted Date
• Warehouse Code
• Building Code
• Door Code
• Supervisor Code
• Operator Code

### Supervisor Alerts Tasks <a id="supervisor-alerts-tasks"></a>

You can complete the following tasks from the from the Supervisor Alerts menu option:
• Viewing Supervisor Alert Details
• Searching Supervisor Notices
• Filtering Supervisor Alerts by Activity
• Accepting Supervisor Alerts

218 K.Motion Enterprise 3PL Mobile User Guide

### Viewing Supervisor Alert Details <a id="viewing-supervisor-alert-details"></a>

Supervisor operators can review details about supervisor alerts regarding processes. To view supervisor alert details, complete the following steps:
1. Tap Supervisor Alerts. 
2. Tap F5:Choose Activity. 

K.Motion Enterprise 3PL Mobile User Guide 219
3. Choose one of the following activities:
a) Tap Inbound to display only supervisor alerts related to Put Away transactions. 
b) Tap Outbound to display only supervisor alerts related to Picking or Replenishment transactions. 
c) Tap Inventory to display only supervisor alerts related to Relocation transactions. 
4. Tap F2:Execute Query. 

220 K.Motion Enterprise 3PL Mobile User Guide
5. Tap F8:Next Record. 
6. Tap F6:Next Page to display additional pages. 

K.Motion Enterprise 3PL Mobile User Guide 221

### Searching Supervisor Notices <a id="searching-supervisor-notices"></a>

As a supervisor operator, you can search for alerts that require approval. To search for supervisor notices, complete the following steps:
1. Tap Supervisor Alerts. 
2. Tap F2:Execute Query. 

222 K.Motion Enterprise 3PL Mobile User Guide
3. Tap F1:Cancel. 
4. Tap F5:Choose Activity. 
5. Tap Inbound. 

K.Motion Enterprise 3PL Mobile User Guide 223
6. Tap F4:View Query. 
7. Tap F1:Cancel. 
8. Tap F5:Choose Activity. 

224 K.Motion Enterprise 3PL Mobile User Guide
9. Tap Inventory. 
10. Tap F5:Choose Activity. 
11. Tap Outbound. 

K.Motion Enterprise 3PL Mobile User Guide 225
12. Tap F1: Cancel. 
13. Tap Clear Query. 
Main Supervisor Alerts screen displays.

### Filtering Supervisor Alerts by Activity <a id="filtering-supervisor-alerts-by-activity"></a>

As a supervisor operator, you can apply additional filters based on the process area to search notifications. To filter supervisor alerts by activity, complete the following steps:
1. Tap Supervisor Alerts. 

226 K.Motion Enterprise 3PL Mobile User Guide
2. Tap F5:Choose Activity.
3. Select the appropriate activity to view specified alerts.

K.Motion Enterprise 3PL Mobile User Guide 227

### Accepting Supervisor Alerts <a id="accepting-supervisor-alerts"></a>

As a supervisor operator, you can accept and approve alert notifications from Supervisor Alerts. To accept a supervisor alert, complete the following steps:
1. Select Supervisor Alerts. 
2. Tap F2:Execute Query. 

228 K.Motion Enterprise 3PL Mobile User Guide
3. Tap F8: Next Record. 
4. Tap F2:Choose Alert. 
Note
To review the details of an alert notification, tap F6:Next Page. 

K.Motion Enterprise 3PL Mobile User Guide 229
5. Tap F2: Accept. 

## K.Motion Outbound <a id="k-motion-outbound"></a>

*Manual OUT — K.Motion Outbound*

# Manual OUT — K.Motion Outbound Guide (Guia de Expedição v6.1)

> **ID do Manual:** OUT  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Guia de expedição K.Motion v6.1: processos outbound, picking, shipping, load management. Versão mais recente complementando o Operations 1.

---

---

K.Motion Enterprise 3PL Outbound Guide 1 

### Introduction <a id="introduction"></a>

### Overview <a id="overview"></a>

You can use the K.Motion Enterprise 3PL Outbound page to view and manage the outbound shipping process in the warehouse. The Outbound page is the control center for managing shipping tasks and processing orders. 
The Outbound page allows you to do the following: 
• Work with waves 
• Work with orders 
• Work with draft order entries 
• Work with load management 
• Relocate to pick line 
• Work with RF operator task priorities 

### Accessing the Outbound Menu Options <a id="accessing-the-outbound-menu-options"></a>

You can use the Outbound menu to manage and configure waves, draft order entries and loads. 
To access the Outbound menu, complete the following steps: 
Log into Körber One. 
Select Menu > K.Motion Enterprise 3PL > Outbound. -e 
---

2 K.Motion Enterprise 3PL Outbound Guide
Option Description
Configuration Accesses the following application components for set up:
• Consignee(s)
• Sold to Codes 
• Picking Profile 
• Picking Substitution Profile 
• Pick Line Item Assignments 
• Order Priorities 
• Outbound Process Configuration
• Carton Size Maintenance 
• Packing Station Code 
• Customer Consignee PIPR Override 
• Load Type and Task Configuration 
• Hold Shipping Sequence Profile 
• Shipping Lane Assignment
• Consignee Retail Profile 
Wave Manager Accesses the following application components to manage waves:
• Wave Management 
• Wave Template Management 
• Wave Template Schedule 
• Wave Transactions
Look Up Order(s) Allows you to view, search, and create new orders. 
Draft Order Entry Allows you to create, view, and finalize a drafted order. 
Load Management Allows you to create and manage a load. 
Relocate to Pick Line Allows you to confirm that a replenish is completed and adjust the replenish.
RF Operator Task Assignment Allows you to assign and view outbound related tasks. -e 
---

K.Motion Enterprise 3PL Outbound Guide 3 

### Working with Waves <a id="working-with-waves"></a>

### Overview <a id="overview"></a>

The Wave Manager page allow you to view and manage waves. When working in the Wave Manager page, you can perform the following tasks: 
• Working with Wave Management 
• Working with Wave Template Management 
• Working with Wave Template Schedules
• Working with Wave Transactions
To access the Wave Manager page, select Outbound > Wave Manager. -e 
---

4 K.Motion Enterprise 3PL Outbound Guide

### Working with Wave Management <a id="working-with-wave-management"></a>

The Wave Management page allows you to view and manage waves. 
To view a wave, complete the following steps:
 Select Outbound > Wave Manager > Wave Management. 
Select the wave you want to view. 

### Working with Wave Template Management <a id="working-with-wave-template-management"></a>

When working with the Wave Template Management page, you can perform the following tasks: 
• Creating a Template
• Modifying a Template
• Deleting a Template-e 
---

K.Motion Enterprise 3PL Outbound Guide 5 

### Creating a Template <a id="creating-a-template"></a>

You can create a template using the Wave Template Management page. 
To create a template, complete the following steps:
Select Outbound > Wave Manager > Wave Template Management. 
The Wave Template Manager page displays. 
Click Create New Template on the Action bar.
The Wave Query Wizard page displays. 
Enter the information in the Template Properties fields on the General tab.-e 
---

6 K.Motion Enterprise 3PL Outbound Guide
Click Next. 
Do one of the following:
a) If you know the information, enter the information one or more fields
b) If you need to search for the information, click Modify on the Primary Filters tab.
Click Next.
Enter SQL in the Custom SQL field.-e 
---

K.Motion Enterprise 3PL Outbound Guide 7
Click Finish. 
Click Run Template. 
Click Finish. -e 
---

8 K.Motion Enterprise 3PL Outbound Guide

### Modifying a Template <a id="modifying-a-template"></a>

You can modify a template using the Wave Template Schedules page. 
Note
When you modify a template, the system overrides the previous version.
When you process a wave using the Run Wave command, K.Motion Enterprise 3PL will allocate any unallocated orders in the wave and print the required number of carrier labels.
To modify a template, complete the following steps: 
 Select Outbound > Wave Manager > Wave Template Management. 
The Wave Template Management page displays. 
Click Show Temporary Templates on the Action bar. 
Select the template you want to edit. -e 
---

K.Motion Enterprise 3PL Outbound Guide 9 
Click Run Selected Template. 
Make changes as appropriate. 
Click Finish. 

### Deleting a Template <a id="deleting-a-template"></a>

You can delete a template from the Wave Management page. 
To delete a template, complete the following steps: 
 Select Outbound > Wave Manager > Wave Template Management. 
The Wave Template Management page displays. 
Select the template you want to delete.
Click Delete Template. 
A confirmation message displays.-e 
---

10 K.Motion Enterprise 3PL Outbound Guide
Click Delete Selected Wave Template. 

### Working with Wave Template Schedules <a id="working-with-wave-template-schedules"></a>

You can schedule a template to run automatically at a given time. You must specify a start date for a scheduled template. The end date field for a scheduled template is optional.
When working with the Wave Template Schedule page, you can perform the following tasks:
• Creating a Scheduled Template
• Modifying a Scheduled Template 
• Deleting a Scheduled Template

### Creating a Scheduled Wave Template <a id="creating-a-scheduled-wave-template"></a>

To schedule a wave template, complete the following steps:
Select Outbound > Wave Manger > Wave Template Schedules. 
The Wave Template Schedules page displays. 
Select a template. 
Click Create New Schedule. 
Use the table below to set up values. 
Frequency Minutes Hour Day Month Day of the Week
The 20th minute of each hour
20 Default Default Default Default
The 45th minute of each hour on Wednesdays
45 Default Default Default Wednesday
9 A.M. every day Default 9 A.M. Default Default Default
9 A.M. every Monday Default 9 A.M. Default Default Monday
9 A.M. first of the month Default 9 A.M. 1 Default Default-e 
---

K.Motion Enterprise 3PL Outbound Guide 11
Click Save. 

### Modifying a Scheduled Template <a id="modifying-a-scheduled-template"></a>

You can modify a template from the Wave Manager page. 
To modify a scheduled template, complete the following steps: 
 Select Outbound > Wave Manager > Wave Template Schedules. 
Select the template you want to modify. -e 
---

12 K.Motion Enterprise 3PL Outbound Guide
Click Edit.
The Wave Template Schedule Job Editor page displays.
Make changes as appropriate.
Click Save. -e 
---

K.Motion Enterprise 3PL Outbound Guide 13

### Deleting a Scheduled Template <a id="deleting-a-scheduled-template"></a>

You can delete a scheduled template from the Wave Management page.
To delete a scheduled template, complete the following steps: 
Select Outbound > Wave Manager > Wave Template Schedules. 
Select the wave template you want to delete. 
Click Delete. 
A confirmation message displays. 
Click Delete. -e 
---

14 K.Motion Enterprise 3PL Outbound Guide

### Working with Wave Transactions <a id="working-with-wave-transactions"></a>

You can look for the completion status of a wave by using the Wave Transaction page. 
To view wave transactions, complete the following step, select Outbound > Wave Manager > Wave 
Transactions.
The Wave Transactions page displays. -e 
---

K.Motion Enterprise 3PL Outbound Guide 15

### Working with Look Up Order(s) <a id="working-with-look-up-order-s"></a>

The Look Up Order(s) page allows you to view all orders that have been entered into K.Motion 
Enterprise 3PL, in any status. When working with the Look Up Order(s) page, you can perform the following tasks:
• Searching for an Order
• Creating an Order
• Editing an Order
• Deleting an Order
• Printing an Order
• Using Flow Process 
• Adding Extra Charges 
To access the Look Up Order(s) page, select Outbound > Look Up Order(s). -e 
---

16 K.Motion Enterprise 3PL Outbound Guide

### Searching for an Order <a id="searching-for-an-order"></a>

You can search for orders using various methods in the Look Up Order(s) page. 

### Searching for an Order Using the Search Panel <a id="searching-for-an-order-using-the-search-panel"></a>

You can search for orders or by using the Search panel and entering specific search criteria. 
To search for an order using the search panel, complete the following steps:
Select Outbound > Look Up Order(s). 
Click Search on the Action Bar. 
Search for a task or order by entering any of the following search criteria in the Search fields. 
Click the Search icon. -e 
---

K.Motion Enterprise 3PL Outbound Guide 17

### Searching with Search Mode <a id="searching-with-search-mode"></a>

You can search for orders by using Search Mode. 
To search for an order using Search Mode, complete the following steps:
Select Outbound > Look Up Order(s). 
The Look Up Orders page displays.
Select Search Mode > Additional Search. 
The Additional Search dialog displays. -e 
---

18 K.Motion Enterprise 3PL Outbound Guide
Enter the information in one of the following fields: 
a) Wave Number 
b) Load Number
c) External Load Reference 
Click Search. 

### Creating an Order <a id="creating-an-order"></a>

You can create an order from the Look Up Order(s) page. 
To create an order, complete the following steps:
 Select Outbound > Look Up Order(s). 
The Look Up Order(s) page displays. -e 
---

K.Motion Enterprise 3PL Outbound Guide 19
Select Orders > Add New Orders on the Action bar. 
The Add New Orders page displays.
Enter the customer code in the Customer field. 
Note
The system automatically populates the following fields: Order Date, Order To Ship Date, 
Order To Arrival Date. -e 
---

20 K.Motion Enterprise 3PL Outbound Guide
Click the Additional Info tab. 
Enter information in the following required fields: 
a) Order Miscellaneous
Note
You must select an option from the Load Type field in the Order Miscellaneous section. 
b) Carrier Name 
c) Sold To Code 
d) Consignee Name
Make other changes as appropriate. 
Click Save. -e 
---

K.Motion Enterprise 3PL Outbound Guide 21

### Working with Editing an Order <a id="working-with-editing-an-order"></a>

The Edit Order command allows you to add and delete order lines and change most of the fields in the order header. However, you cannot change either the order type or the order line type.
To edit an order, complete the following steps:
 Select Outbound > Look Up Order(s). 
The Look Up Order(s) page displays. 
Select the order you want to edit.
Click Orders > Edit from the Action bar. 
Make the necessary changes to the order.
Click Save. -e 
---

22 K.Motion Enterprise 3PL Outbound Guide

### Working with Deleting an Order <a id="working-with-deleting-an-order"></a>

You can delete an order using the Look Up Order(s) page. 
To delete an order, complete the following steps. 
 Select Outbound > Look Up Order(s). 
The Look Up Order(s) page displays.
Select the order you want to delete.
Select Orders > Delete. 
Click Delete. 

### Printing an Order <a id="printing-an-order"></a>

You can print an order from the Look Up Order(s) page at any time. You can print an order as follows:
• Printing an Order by Document Code 
• Printing an Order 
• Requeuing an Order-e 
---

K.Motion Enterprise 3PL Outbound Guide 23

### Printing an Order by Document Code <a id="printing-an-order-by-document-code"></a>

You can print an order using a document code from the Look Up Order(s) page at any time. 
To print an order using a document code, complete the following steps:
Select Outbound > Look Up Order(s). 
Select Print Document > Print by Document Code on the Action bar. 

Enter the document code in the Select Document field. 
Select the order you want to print. 
Enter the printer or email location the appropriate field. 
Select one of the following print options. 
a) Print Document to View 
b) Print Documents 
c) Email Document-e 
---

24 K.Motion Enterprise 3PL Outbound Guide

### Printing an Order <a id="printing-an-order"></a>

You can print an order by order from the Look Up Order(s) page at any time. 
To print an order, complete the following steps:
Select Outbound > Orders. 
Select the order you want to print. 
Select Print Document > Print by Order on the Action bar.
Enter the printer or email location the appropriate field. 
Select one of the following print options. 
a) Print Document to View 
b) Print Documents 
c) Email Documents
A notification that the operation was successful will display. -e 
---

K.Motion Enterprise 3PL Outbound Guide 25

### Requeuing an Order <a id="requeuing-an-order"></a>

You can requeue an order from the Look Up Order(s) page at any time. 
To requeue an order, complete the following steps:
Select Outbound > Look Up Order(s). 
Select the order you want to requeue.
Select Print Document > Requeue by Order. 
Complete the following:
a) If you want to print the requeued order enter a printer code in the Select Printer field.
b) If you want to email the requeued order enter an email address in the Email To field.
Select the document you want to requeue.
Select Requeue or Requeue and Print. 
A notification that the operation was successful displays. 

### Using Flow Process <a id="using-flow-process"></a>

Flow process is the defined sequence of steps that an order must follow, for receiving orders and for shipping. 
Note
You can only advance to the next flow and reverse to the previous flow. You cannot advance or revers more than one flow at a time. 

### Using Advancing Flow Process for an Order <a id="using-advancing-flow-process-for-an-order"></a>

You can use the advanced flow process if you want to manually advance the flow of an order, if it has not been confirmed. 
To use the advance flow process, complete the following steps:
Select Outbound > Look Up Order(s). -e 
---

26 K.Motion Enterprise 3PL Outbound Guide
Select the order you want to advance.
Click Flow Process on the Action bar.
Select Advance Flow Process.
Select the order you want to advance.
Click Process Flow to advance the order.
Click Process Flow. -e 
---

K.Motion Enterprise 3PL Outbound Guide 27

### Reversing Flow Process for an Order <a id="reversing-flow-process-for-an-order"></a>

You can change or edit an order after it has advanced in the flow process by reversing the flow process.
To use the reverse flow process, complete the following steps:
Select Outbound > Lok Up Order(s). 
Select the order you want to reverse.
Click Flow Process on the Action bar.
Select Reverse Flow Process. 
Select the order you want to reverse. 
Click Process Flow to reverse the order in the flow. -e 
---

28 K.Motion Enterprise 3PL Outbound Guide

### Adding Extra Charges <a id="adding-extra-charges"></a>

You can add extra charges confirmed orders and accessorial charges to open orders in the Look Up 
Order(s) page. 
Note
Extra charges can only be cancelled when an order is open, if they have been automatically applied. 

### Adding Extra Header Charge <a id="adding-extra-header-charge"></a>

To add extra charges to an order, complete the following steps: 
Note
Charge Code is a required field. 
Select Outbound > Look Up Order(s). 
Select an order to add extra charges. 
Click Misc on the Action bar.-e 
---

K.Motion Enterprise 3PL Outbound Guide 29
Select Add Extra Charge. 
Select the line you want to add extra charges to. 
Click Edit. 
Select Extra Charge on the Action bar. 
Select Order Extra Charge Flag. 
Select Header Extra Charge.
Enter the information in the Main fields on the Header tab.-e 
---

30 K.Motion Enterprise 3PL Outbound Guide
Click Next. 
Enter the information in the Qualifying and Charge fields on the Detail tab. 
Click Save. 

### Adding Extra Line Charge <a id="adding-extra-line-charge"></a>

To add extra charges to an order, complete the following steps: 
Note
Charge Code is a required field. 
Select Outbound > Orders. 
Select an order to add extra charges. 
Click Misc. -e 
---

K.Motion Enterprise 3PL Outbound Guide 31
Select Add Extra Charge. 
Select the line that you want to add extra charges to. 
Click Edit. 
Select Extra Charge on the Action bar. 
Select Order Extra Charge Flag. 
Click Save.
Select Line Extra Charge.
Enter the information in the Main fields on the Header tab.-e 
---

32 K.Motion Enterprise 3PL Outbound Guide
Click Next. 
Enter the information in the Qualifying and Charge fields on the Detail tab. 
Click Save. -e 
---

K.Motion Enterprise 3PL Outbound Guide 33

### Working with Draft Order Entry <a id="working-with-draft-order-entry"></a>

A draft order is a newly-created order that has not yet been verified or committed. 
Note
Draft orders are optional. You can create a committed order in Look Up Orders.
When working with the Draft Order Entry page, you can perform the following tasks: 
• Entering an Order Header
• Editing a Draft Order
• Deleting a Draft Order
• Committing a Draft Order

### Entering an Order Header <a id="entering-an-order-header"></a>

The order header contains general information that applies to the entire order such as the customer code, the consignee, the carrier and the load type. 
To complete an order header, complete the following steps: 
 Select Outbound > Draft Order Entry. 
The Draft Order Entry page displays. -e 
---

34 K.Motion Enterprise 3PL Outbound Guide
On the Basic Info tab, enter the customer code in the Customer field. 
Note
The system automatically populates the following fields: Order Date, Order To Ship Date and 
Order To Arrive Date. 
Click the Order Lines tab. 
Click Add New Record to add a new order line record. 
Enter information into the following fields:
a) Item
b) Line Type
c) Ordered Quantity
Click Save. -e 
---

K.Motion Enterprise 3PL Outbound Guide 35
Click the Additional Info tab.
Click the plus option to expand each section. 
Make updates as needed to each section. 
Click Save. 

### Editing a Draft Order <a id="editing-a-draft-order"></a>

To edit a draft order, complete the following steps: 
 Select Outbound > Draft Order Entry. 
The Draft Order Entry page displays. -e 
---

36 K.Motion Enterprise 3PL Outbound Guide
Click Retrieve. 
Select the order you want to edit.
Click Select.
Make changes as necessary.
Click Save. -e 
---

K.Motion Enterprise 3PL Outbound Guide 37

### Deleting a Draft Order <a id="deleting-a-draft-order"></a>

To delete a draft order, complete the following steps: 
 Select Outbound > Draft Order Entry. 
The Draft Order Entry page displays. 
Click Retrieve. 
Select the order you want to delete. -e 
---

38 K.Motion Enterprise 3PL Outbound Guide
Click Select. 
Click Delete. 
Click Delete on the confirmation dialog.

### Committing a Draft Order <a id="committing-a-draft-order"></a>

To commit a draft order, complete the following steps: 
 Select Outbound > Draft Order Entry. 
The Draft Order Entry page displays.-e 
---

K.Motion Enterprise 3PL Outbound Guide 39
Click Retrieve. 
Select the order you want to commit.
Click Select. 
Click Commit.-e 
---

40 K.Motion Enterprise 3PL Outbound Guide

### Working with Load Management <a id="working-with-load-management"></a>

When creating a load, you can define the door, the building, the warehouse attributes, the orders on the load and the stop sequence. 
You can also enter carrier and consignee information in the Load Manager when you are working with multi-leg trips in which the freight is transported first to a freight pool point or distribution center. The carriers and consignees attached to the orders are used to deliver the freight to its final destination.
When working with the Load Management page, you can perform the following tasks: 
• Creating a Load 
• Editing a Load 
• Using Load Status 
• Suspending, Releasing and Deleting Loads 
To access the Load Management page, select Outbound > Load Management. -e 
---

K.Motion Enterprise 3PL Outbound Guide 41

### Creating a Load <a id="creating-a-load"></a>

To create a load, complete the following steps: 
Note
The following fields are auto populated but can be changed: Building, Warehouse Attribute, and External Reference Code. 
 Select Outbound > Load Management. 
The Load Management page displays. 
Click Create on the Action bar.
Enter information into the Load fields. -e 
---

42 K.Motion Enterprise 3PL Outbound Guide
Click Save. 
Select the Carrier tab.
Enter load information into the Carrier tab fields. 
Click the Orders tab.-e 
---

K.Motion Enterprise 3PL Outbound Guide 43
Click Add New Records. 
The Load Order Editor displays.
Enter information into the following fields:
a) Order Number
b) Stop Number
Click Save to save the order within the load.
Click Close to return to the load list page.
Editing a Load
You can access the Load Management page at any time to edit information in an existing load. 
To edit an existing load, complete the following steps:
Select Outbound > Load Management. 
Select the load you want to edit. -e 
---

44 K.Motion Enterprise 3PL Outbound Guide
Click Edit on the Action bar. 
Make changes as needed.
Click Save. 

### Using Load Status <a id="using-load-status"></a>

You can advance and reverse a load status on the Load Management page. 

### Using Advance Status for a Load <a id="using-advance-status-for-a-load"></a>

You can manually advance the flow of a load. 
To use the advance flow process, complete the following steps:
Select Outbound > Load Management. 
Select the order you want to work with.
Click Advance Status on the Action bar. -e 
---

K.Motion Enterprise 3PL Outbound Guide 45

### Reversing a Load Status <a id="reversing-a-load-status"></a>

You can edit a load status in the reverse load status. 
To use the revere load status, complete the following steps: 
Select Outbound > Load Management. 
The Advanced Load Status message displays. 
Select the load you want to reverse. 
Click Reverse Status. 

### Suspending, Releasing, and Deleting Loads <a id="suspending-releasing-and-deleting-loads"></a>

You can suspend, release and delete loads from the Load Management page. 

### Suspending a Load <a id="suspending-a-load"></a>

You can suspend a load if it has a status of Ready to Load or Loading. 
To suspend a load, complete the following steps:
Select Outbound > Load Management. -e 
---

46 K.Motion Enterprise 3PL Outbound Guide
Select the order that you want to suspend. 
Click Suspend. 
A notification displays confirming the load was suspended. 

### Unsuspending a Load <a id="unsuspending-a-load"></a>

You can unsuspend a load that has previously been suspended. 
To unsuspend a load, complete the following steps:
Select Outbound > Load Management. 
Select the order you want to unsuspend. 
Click UnSuspend. 
A notification will display that the load has been successfully unsuspended. -e 
---

K.Motion Enterprise 3PL Outbound Guide 47

### Deleting a Load <a id="deleting-a-load"></a>

You can delete a load at any time using the Load Management page.
To delete a load, complete the following steps: 
Select Outbound > Load Management. 
Select the order you want to delete. 
Click Delete. 
Click Yes to confirm you want to delete the order. -e 
---

48 K.Motion Enterprise 3PL Outbound Guide

### Working with Relocate to Pick Line <a id="working-with-relocate-to-pick-line"></a>

### Overview <a id="overview"></a>

You can view open replenishments from the Relocate to Pick Line page at any time. When working with the Relocate to Pick Line page, you can perform the following tasks: 
• Processing an Order Replenishment 
• Deleting an Order Replenishment 
To access the Relocate to Pick Line page, select Outbound > Relocate to Pick Line. -e 
---

K.Motion Enterprise 3PL Outbound Guide 49

### Processing an Order Replenishment <a id="processing-an-order-replenishment"></a>

You can manually process a replenishment order by using the Relocate to Pick Line page. 
To process a replenishment order, complete the following steps:
Select Outbound > Relocate to Pick Line. 
The Relocate to Pick Line page displays. 
Select the order you would like to process. 
Select Process on the Action bar. 
A notification appears confirming the order has been processed successfully.-e 
---

50 K.Motion Enterprise 3PL Outbound Guide

### Deleting an Order Replenishment <a id="deleting-an-order-replenishment"></a>

You can manually delete a replenishment order by using the Relocate to Pick Line page. 
To delete a replenishment order, complete the following steps:
Select Outbound > Relocate to Pick Line. 
The Relocate to Pick Line page displays. 
Select the order you would like to delete. 
Select Delete on the Action bar.
A notification appears confirming the order has been deleted. -e 
---

K.Motion Enterprise 3PL Outbound Guide 51
Working with RF Operator Task 
Assignment 

### Overview <a id="overview"></a>

The RF Operator Task Assignment allows the user to assign specific tasks, operators and define a picking sequence. When working with the RF Operator Task Assignment page, you can perform the following tasks:
• Search for Orders or Tasks
• Assign to Orders
To access the RF Operator Task Assignment page, select Outbound > RF Operator Task 
Assignment. -e 
---

52 K.Motion Enterprise 3PL Outbound Guide

### Search for Orders or Tasks <a id="search-for-orders-or-tasks"></a>

You can search for orders or tasks by using the Search panel and entering specific search criteria. 
To search for an order or task, complete the following steps: 
Select Outbound > RF Operator Task Assignment. 
The Search panel displays when the page opens. 
Search for a task or order by entering any of the search criteria. 
Click the Search. 

### Assign to Orders <a id="assign-to-orders"></a>

You can assign a task from the Operator Task Assignments Page at any time. 
To assign a task, complete the following steps: 
Select Outbound > RF Operator Task Assignment. -e 
---

K.Motion Enterprise 3PL Outbound Guide 53
Enter the search criteria in the Search panel. 
Select the Order or task you want to assign. 
Click Assign to Orders. 
Enter information in the Order Assignments fields.
Select an order. 
Click Update. -e 
---

54 K.Motion Enterprise 3PL Outbound Guide

### Assign a Task to an Operator <a id="assign-a-task-to-an-operator"></a>

You can assign a task to a specific operator. 
To assign a task, complete the following steps:
Select Outbound > RF Operator Task Assignment. 
Enter the search criteria in the Search panel. 
Select the order or task you want to assign.-e 
---

K.Motion Enterprise 3PL Outbound Guide 55
Select Assign to Orders.
To assign a task, select an operator from the Operator field.
Click Save. 

### Place Tasks in Sequential Order <a id="place-tasks-in-sequential-order"></a>

You can place tasks in sequential order. 
To place tasks in order, complete the following steps: 
Select Outbound > RF Operator Task Assignment. 
Enter the search criteria in the Search panel. 
Click Search on the Search panel. -e 
---

56 K.Motion Enterprise 3PL Outbound Guide
Select the order for the tasks that you want to place in sequential order. 
Select a task. 
Enter the sequence number of your task in the Sequence Number field. 
Click Save. 
Repeat steps 1 through 6 for each task you would like to label. 

### Suspend a Task <a id="suspend-a-task"></a>

You can suspend a task using the Operator Task Assignment page. 
To suspend a task, complete the following steps: 
Select Outbound > RF Operator Task Assignment. 
Enter the search criteria in the Search panel. -e 
---

K.Motion Enterprise 3PL Outbound Guide 57
Click Search on the Search panel. 
Select the order or task you want to suspend. 
Click Assign to Orders. 
Select the task you want to suspend. 
Check the Suspend Task box. 
Click Update. 
Click Save. 
A message appears to notify you that the operation was successful.-e 
---

58 K.Motion Enterprise 3PL Outbound Guide
Override a Task Priority 
You can override a task priority using the Operator Task Assignment page. 
To override a task priority, complete the following steps: 
Select Outbound > RF Operator Task Assignment. 
Enter the search criteria in the Search panel. 
Click Search on the Search panel.
Select the task you want to view. 
Click Tasks on the Menu bar.-e 
---

K.Motion Enterprise 3PL Outbound Guide 59
Click Assign to Orders.
Select the task you want to prioritize. 
Enter a priority number in the Priority Override field. 
Click Update. 
Click Save. 
A message appears to notify you that the operation was successful. -e 
---
