---
title: "Agendamento de Docas e Painel Operacional"
description: "Appointment Planner: prédios, portas, perfis de dia, tipos de carga e quadro operacional."
layout: default
---

# Agendamento de Docas e Painel Operacional

Appointment Planner: prédios, portas, perfis de dia, tipos de carga e quadro operacional.

**Fluxo principal:** `BLDG/DOOR/DAPC (setup) -> APPL (agenda) -> painel operacional`

> Fonte: manuais E do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Appointment Planner <a id="appointment-planner"></a>

*Manual E — Operations 2*

# Manual E — Operations 2 Guide (Operações 2: Funcionalidades Avançadas)
> **ID do Manual:** E  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Funcionalidades avançadas: Appointment Planner (APPL), back orders, batch picking (GEBA/POBA), cargas (SELO/OLOP), cross-docking, packing, process values (IPRO), item substitution, quick response labels, CRM, bonds, inventory attributes, EDI, operational board, labor standards.
---

OPERATIONS 2 GUIDE 4.2* 5

### Overview <a id="overview"></a>

AccellosOne 3PL’s Appointment Planner is a dock door and load scheduling system that supports your management of dock doors, material handling, equipment, labor resources and loads. With the Appointment 
Planner you can:
 schedule inbound and outbound loads for a given time at a given door in order to make the best possible use of your facilities
 set up recurring appointments on a daily, weekly, monthly or yearly basis
 determine daily work loads and predict future work loads
 develop standards for loading and unloading that allow you to improve work load planning
 centralize access of this information to all system users
The Appointment Planner is fully integrated with AccellosOne 3PL time-stamping; when you update your appointment information, a record is automatically created in the Time-Stamping Block of LORE or LOOR to reflect the appointment’s activity.
APPL
Inbound/
Outbound?
ENRE
Inbound
APPL
If the appointment is an inbound appointment, you attach it to a receipt in ENRE or APPL. If the appointment is an outbound appointment, you attach it to an order in ENOR or APPL.
You enter your appointments in APPL (Appointment
Planer).
You update the status of an appointment (arrived, completed, etc.) in APPL (Appointment Planner).
Outbound
ENOR
The completed appointment Is automatically deleted.

### Setting Up the Appointment Planner <a id="setting-up-the-appointment-planner"></a>

There are four setup programs for the appointment planner:
 BLDG (Building)
 DOOR (Door)
 LOAD (Load Type)
 DIFP (Depositor Workflow Profile)

### SETTING UP YOUR BUILDINGS IN BLDG <a id="setting-up-your-buildings-in-bldg"></a>

You set up your buildings in the program BLDG (Building). A building is a single physical structure in your facility. It need not correspond to the warehouses that you set up in WARE (Warehouse and Location 
Format). For example, if you set up multiple warehouses to correspond to different areas in your facility, the same building would contain more than one warehouse.
FIELD DESCRIPTIONS
Building Mandatory
Your building code.
Description Mandatory
A description for your building code.
Appointment Time Slice in Minutes
Optional
The duration in minutes of each time slot in APPL. The minimum value that you can enter in this field is 15 minutes, which is the system default.
Appointment Start / End 
Times
Optional
The start and end times for your building. You cannot enter appointments outside of these times. If you do not enter start and end times for your building, your building will be open 24 hours a day.
Start and end times can span two dates. For example, your building is open for inbound appointments from 10:00 pm until 5:00 am the next morning. 
NOTE If you change your start and end times, existing appointments outside of these times will not display in Calendar View but can be seen in Detail 
View.

OPERATIONS 2 GUIDE 4.2* 7
1 Enter BLDG.
2 Click on New . 
3 Key in your building code and press Enter.
4 If required, key in your appointment time slice in minutes and press Enter.
5 If required, key in a start time for your building.
6 If required, key in a end time for your building.
7 Press Enter three times to bypass the COR Required Flag, Document Code for COR Report and Split 
Inbound Load Across Appointments fields.
8 If required, select or deselect the Door Required for Appointment checkbox.
9 If required, key in a value in the Maximum Number of Appointments per Day field.
10 Click on Save .
COR Required Reserved for future use.
Document Code for COR 
Report
Reserved for future use.
Split Inbound Load 
Across Appointments
Reserved for future use.
Allow Multiple Outbound 
Loads Per Appointment
If you select this option, you can add multiple outbound loads to a single appointment in APPL.
Door Required for 
Appointment
If you select this option, a door is mandatory in APPL when creating an appointment. If you do not select this option, you can enter appointments in 
APPL without specifying a door.
When this option is deactivated, Calendar View in APPL shows one line for appointments without doors with an asterisk (“*”) in the Door column to indicate no door.
Maximum Number of 
Appointments per Day
Optional
If you enter a value in this field, whenever the number of appointments for a given day exceeds this value, the day will be shown as red on the calendar.
FIELD DESCRIPTIONS

Building (BLDG) screen showing setup for building 01
11 When you finish adding your building, click on Exit to exit.

### SETTING UP YOUR LOAD TYPES IN LOAD <a id="setting-up-your-load-types-in-load"></a>

Load types allow you to define the number of minutes needed to load or unload a given quantity of a given load type. AccellosOne 3PL uses this information in APPL to calculate the duration of the appointment required for a given weight or number of units. If required, you can override the system-calculated duration when setting up an appointment.
You can specify quantities by either weight or number of units. For example, you could specify your quantities by weight in the Weight Block:
2,000 lbs > 20 min.
4,000 lbs > 30 min.
8,000 lbs > 40 min.
Alternatively, you could specify your quantities by SKU class in the Quantity Block:
10 pallets > 15 min.
20 pallets > 25 min.
30 pallets > 45 min.
The same load type can have values in both the Weight Block and the Quantity Block if you wish to specify quantities by both weight and SKU class. As well, you can have multiple SKU classes or weights in the same block. For example, you could specify times for pallets and cases: 
10 pallets > 20 min.
20 pallets > 30 min.

OPERATIONS 2 GUIDE 4.2* 9
30 pallets > 40 min.
200 cases > 50 min.
400 cases > 60 min.
NOTE If the number of minutes for your load type does not match the time slice that you defined in BLDG (Building), AccellosOne 3PL will round up the appointment time. 
FIELD DESCRIPTIONS
Load Type Code Mandatory
Your load type code.
Description Mandatory
A description for your load type code.
Labor Standard Modifier See [OPERATIONAL BOARD](agendamento-docas.html#operational-board).
Num of Temp. Only available if temperature capture is activated in MRFP
The number of temperatures to be captured in RF receiving. You can capture up to six different temperatures in RFCH. If you leave this field blank, the default value of four temperatures to capture will display.
Inb. Fixed Minutes The fixed number of minutes added to an inbound appointment for trailer preparation, paperwork, etc. For example, if you enter 15 in this field and in the 
Quantity Block it takes 30 minutes to unload 20 pallets, an inbound load of 20 pallets will have a lapse time in minutes of 45 (15 + 30).
Outb. Fixed Minutes The fixed number of minutes added to an outbound appointment for trailer preparation, paperwork, etc. For example, if you enter 10 in this field and in the Quantity Block it takes 25 minutes to load 20 pallets, an outbound load of 
20 pallets will have a lapse time in minutes of 35 (10 + 25).
Override Pick Method to 
Each
See the Setup Guide.

1 Enter LOAD.
2 Key in your load type code and press Enter.
3 Key in your load type description and press Enter.
4 Press Enter to bypass the Labour Modifier field.
5 In the Num of Temp. field, key in the number of temperatures that you wish to capture and press Enter.
6 In the Inb. Fixed Minutes field, key in the number of fixed minutes for inbound appointments and press 
Enter. If you have no fixed minutes for inbound appointments, press Enter to bypass this field.
7 In the Outb. Fixed Minutes field, key in the number of fixed minutes for outbound appointments and press 
Enter. If you have no fixed minutes for outbound appointments, press Enter to bypass this field.
8 Press Enter three times to bypass the Override Pick Method to Each, Disable Item Substitution from PL and Disable Count Backs fields.
9 Do one of the following:
10 In the Weight Block, you enter your weights if you are scheduling by weight. If you wish to schedule by number of units rather than weight, click on Quantity Block.
11 In either the Weight Block or the Quantity Block, click on Create Record. Then use your pick list to select your weight code or SKU class.
12 In the Quantity field, key in the number of units for your weight or SKU class (for example, 2,000 if your weight unit is pounds or 10 if your SKU class is pallets) and press Enter.
13 In the Minutes field, key in the number of minutes required to load or unload the weight or SKU class quantity that you specified in the previous two fields. Then press Enter.
14 Repeat the above steps for each additional break that you wish to add.
Disable Item Subst. from 
PL
See the Setup Guide.
Disable Countbacks See the Setup Guide.
If you wish to set up an inbound load type:
If you wish to set up an outbound load type:
If you do not wish to use load types to calculate the duration of appointments:
a) Proceed to next step. a) Click on In/Out Block. 
b) Press your down arrow key to display the Outbound option.
c) Click on Weight Block.
a) Click on In/Out Block. Then click on Master Block and Exit to exit LOAD.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 11

Load Type (LOAD) screen showing appointment scheduling by number of pallets
15 When you finish entering your values in the Weight Block of Quantity Block, click on Return to Main to exit create record mode. Then click on Master Block and Exit to exit.

### SETTING UP YOUR DOORS IN DOOR <a id="setting-up-your-doors-in-door"></a>

Once you have set up your buildings in BLDG, you set up your doors in the program DOOR (Door). You should set up one door for each door in your building. In this program, you define the following:
 the door code and description as well as the building to which the door belongs
 the type of door (inbound, outbound or both)
 the times that the door will be open (if you attempt to schedule an appointment at a time that the door is not open, a warning will display in APPL
 the door’s regular and staging location (outbound load building system only)
FIELD DESCRIPTIONS
Building (defined in BLDG)
Mandatory
The building to which the door belongs.
Door Mandatory
Your door code.

Description Mandatory
The description for your door code.
Type I = Inbound (only available for the appointment planner)
O = Outbound
B = Both
The door’s type. 
Inb. Start-End Time Optional
The door’s start and end time for inbound receiving when using the Appointment Planner. If the start and end times for your door fall outside the start and end times of your building, any appointments set up during these non-building times will not display in Calendar View.
This field is only available when the Type field is set to Inbound or Both. If you do not enter inbound start and end times, AccellosOne 3PL will use the building’s start and end times.
Location Code (defined in LOCA)
Only required for outbound load building system
The door’s location code. The product is automatically moved to this location when you load in OLOP. A door location can have any location type set up in 
LOTP.
Warehouse Code (defined in WARE)
Only required for outbound load building system
The warehouse for the door’s location code.
RFID Reader ID Reserved for future use.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 13
1 Enter DOOR.
2 Click on Create Record.
3 Key in your building code and press Enter.
4 Key in your door code and press Enter.
5 Key in your door description and press Enter.
6 Key in your door type (I for Inbound, O for Outbound or B for Both) and press Enter.
7 If you selected either inbound or both as your door type, key in your start and end times for inbound receiving in the Start and End Time fields. You must enter your times using the 24-hour format.
8 If required, key in your door location and press Enter. Then key in your warehouse code and press Enter again. If you have a single warehouse in AccellosOne 3PL, press Enter to accept the default warehouse code.
9 Press Enter to bypass the RFID Reader ID field.
10 If you selected either outbound or both as your door type, key in your start and end times for outbound shipping in the Start and End Time fields. You must enter your times using the 24-hour format.
11 If required, key in your staging location for the door and press Enter. Then key in your warehouse code and press Enter again. If you have a single warehouse in AccellosOne 3PL, press Enter to accept the default warehouse code.
12 Repeat steps 3 to 11 for each additional door that you wish to add.
Outb. Start-End Time Optional
The door’s start and end time for outbound shipping when using the Appointment Planner. If the start and end times for your door fall outside the start and end times of your building, any appointments set up during these non-building times will not display in Calendar View.
This field is only available when the Type field is set to Outbound or Both. If you do not enter outbound start and end times, AccellosOne 3PL will use the building’s start and end times.
Staging Location Code (defined in LOCA)
Only required for outbound load building system
If you unload a load in OLOP, the product will be automatically move to the location that you specify in this field. The staging location can be the same as the door location or can be a different location. A staging location can have any location type set up in LOTP.
Staging Warehouse Code (defined in WARE)
Only required for outbound load building system
The warehouse for the door’s staging location code.
FIELD DESCRIPTIONS

13 When you finish adding your door, click on Return to Main to exit create record mode.

Door (DOOR) screen showing three outbound doors
14 Click on Exit to exit.
ADDING THE SPECIAL VERIFICATION PROGRAMS TO YOUR WORKFLOW 
PROFILE IN DIFP
The following special verify programs must be attached to your workflow profile(s):
 AAPO (Set Arrived Appointment - Outbound)
 AAPR (Set Arrived Appointment - Inbound)
 APOC (Set Complete Appointment - Outbound)
 APRC (Set Complete Appointment - Inbound)
These special verifies perform two functions:
 they update the Time Stamping Blocks in LORE and LOOR with your appointment information
 they mark appointments as arrived or completed when the order/receipt that they are assigned to is advanced passed that flow (if you do not use these special verify programs, you must update the status of appointments manually in APPL)
1 Enter DIFP.
2 Key in your workflow profile code and press Enter.
3 Click on In/Out/Repi/Relo Block. The first record in this block will be your Inbound record.
4 Click on Flow Block.
5 In the Flow Block, use your arrow keys to select the flow at which you want the Time-Stamping Blocks in 
LORE and LOOR updated with your appointment information. You can select any inbound flow that is after ENRE and before CORE.
6 Click on Document Block.

OPERATIONS 2 GUIDE 4.2* 15
7 In the Document Block, click on Special Verify Block.
8 In the Special Verification Block, key in 10 as your sequence number and press Enter.
9 Key in AAPR (Set Arrived Appointment - Receipt) and press Enter.
10 Press Enter to accept the default values in the Complete, Sequence and Display fields.

DIFP screen showing Special Verification Block
11 Click on Return to Main.
12 Click on Document Block, Flow Block and In/Out/Repi/Relo Block.
13 Select the Outbound option.
14 Repeat steps 4 to 7 for the outbound flow at which you want your time-stamping information to be updated. You can select any outbound flow that is after ENOR and before COOR.
15 When you reach the Special Verification Block for your outbound flow, key in 10 as your sequence number and press Enter.
16 Key in AAPO (Set Arrived Appointment - Order) and press Enter.
17 Press Enter to accept the default values in the Complete, Sequence and Display fields.
18 Click on Return to Main. Then repeat the above steps for your APOC and APRC special verify programs.
19 Setup is now complete. Click on Return to Main. Then click on Document Block, Flow Block, In/Out/
Repp/Rely Block, Master Block and Exit to exit.

### CAPO (CREATE APPOINTMENT FROM ORDER) <a id="capo-create-appointment-from-order"></a>

This special verify allows you to automatically generate an appointment for an order in CHOF. The appointment date is the order’s to ship date in ENOR and the lapse time in minutes is the value that you entered in the Appointment Time Slice in Minutes field in BLDG.
CAPO screen

### CAPR (CREATE APPOINTMENT FROM RECEIPT) <a id="capr-create-appointment-from-receipt"></a>

This special verify allows you to automatically generate an appointment for a receipt in CHRF. The appointment date is the receipt’s receipt date in ENRE and the lapse time in minutes is the value that you entered in the Appointment Time Slice in Minutes field in BLDG.
CAPR screen

OPERATIONS 2 GUIDE 4.2* 17

### CABO (CREATE APPOINTMENT FROM ORDER IN BACKGROUND) <a id="cabo-create-appointment-from-order-in-background"></a>

With background processing, no appointment entry screen displays during outbound shipping. The appointment is automatically generated in the background and you must manually enter your door for the appointment in APPL.
The following requirements must be met before you can generate outbound appointments in the background:
 orders must be assigned to buildings in one of two ways: either you define a default building for all appointments in ATMP (Action Template Setup) under the Block Code E_APPO_H or you enter a warehouse code in the header block of ENOR and that warehouse has been assigned a building code in 
WARE
 the Door Required for Appointment flag in BLDG (Building) must be unchecked

### CABR (CREATE APPOINTMENT FROM RECEIPT IN BACKGROUND) <a id="cabr-create-appointment-from-receipt-in-background"></a>

With background processing, no appointment entry screen displays during inbound receiving. The appointment is automatically generated in the background and you must manually enter your door for the appointment in APPL.
The following requirements must be met before you can generate inbound appointments in the background:
 receipts must be assigned to buildings in one of two ways: either you define a default building for all appointments in ATMP (Action Template Setup) under the Block Code E_APPO_H or you enter a warehouse code in the header block of ENRE and that warehouse has been assigned a building code in 
WARE
 the Door Required for Appointment flag in BLDG (Building) must be unchecked

### Setting Up an Appointment <a id="setting-up-an-appointment"></a>

You have two options for setting up appointments. You can enter your receipt or order first and then set up your appointment. Alternately, you can set up your appointment first and then enter the receipt or order. If you set up your appointment first, you must attach it to the appropriate receipt or order in ENRE or ENOR. 
The mandatory fields in APPL are:
 the load type
 whether the appointment is for a receipt, order or load number 
 the customer (if you enter an order or receipt number, this information is filled by AccellosOne 3PL)
 the carrier (if you enter an order or receipt number, this information is filled in by AccellosOne 3PL)
 the building
If you have defined load types in LOAD with weight and quantity breaks, AccellosOne 3PL will automatically calculate an estimate of the appointment’s duration. If you have not defined load types in LOAD with weight and quantity breaks, you will have to enter the appointment’s duration manually.
If required, you can override the system-selected door and time slot and select your own door and time slot. 
When you finish setting up your appointment, AccellosOne 3PL will create an appointment number for it so that you can access the appointment in other AccellosOne 3PL programs.

### ENTERING AN APPOINTMENT WHEN THE RECEIPT OR ORDER IS KNOWN <a id="entering-an-appointment-when-the-receipt-or-order-is-known"></a>

If you have already created your receipt or order, you enter the receipt or order number in the Document 
Number field in APPL. 
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.
APPL screen showing set up appointment mode
4 In the Inbound/Outbound/Load field, select Inbound if the appointment is for a receipt or Outbound if the appointment is for an order.
5 In the Document Number field, key in your receipt or order number and press Enter or select your document from the pick list.
AccellosOne 3PL will populate the Account Type, Code, Carrier Code and Load Type Code with the appropriate values from the receipt or order. If you have set up values in the Weight Block or Quantity 
Block of LOAD (Load Type), the Lapse Time in Minutes field will also be populated with the number of minutes that AccellosOne 3PL estimates will be required to load or unload the load.
If required, you can change the carrier. If you change the carrier in APPL, the carrier will be automatically updated in ENOR.

OPERATIONS 2 GUIDE 4.2* 19
6 Do one of the following.
7 If door entry is mandatory for your appointments, select your door code from the dropdown list.
8 Press Enter to accept the current date as your appointment start date or select a date other than the current date from the pop-up calendar.
9 Key in your start time in 24-hour format and press Enter. Based on your lapse time in minutes, AccellosOne 3PL will populate the End Date and End Time fields with the appropriate values.
10 If required, key in a reference number and press Enter.
11 If required, key in a contact name for the appointment and press Enter.
12 If required, key in the name of the warehouse supervisor and press Enter. If there is no warehouse supervisor for this appointment, press Enter to bypass this field.
13 If required, key in a load description and press Enter.
14 When you finish adding your appointment, click on Save. AccellosOne 3PL will display an appointment number; you use this number if you wish to look up your appointment or make changes to it.
If the load type that you entered is based on weight:
If the load type that you entered is based on SKU class:
If the load type that you entered has no weight or quantity breaks:
a) In the Weight field, press 
Enter to accept the weight that is displayed or key in a new weight and press Enter.
b) In the Lapse Time in Minutes field, AccellosOne 3PL will calculate the appointment’s duration in minutes. Press 
Enter to accept this estimate or key in a new value and press Enter.
a) Key in your quantity for that 
SKU class and press Enter.
b) In the SKU Class Number field, select the appropriate 
SKU class from the dropdown list.
c) In the Lapse Time in Minutes field, AccellosOne 3PL will calculate the appointment’s duration in minutes. Press 
Enter to accept this estimate or key in a new value and press Enter.
a) Press Enter twice to bypass the Weight Measure Code and 
SKU Class fields. 
b) In the Lapse Time in Minutes field, key in the number of minutes required for the appointment and press Enter.
NOTE If AccellosOne 3PL fails to calculate the loading or unloading time and select a time slot and door, check your load type in LOAD and make sure that there is a weight or quantity break for the weight or quantity that you entered. For example, if you enter a weight of 5,100 pounds in APPL but your highest weight break in LOAD is 
5,000 pounds, the system will be unable to calculate a lapse time.

Appointment Planner (APPL) screen showing an inbound appointment for 10 pallets assigned to building 01
15 Do one of the following:

### ENTERING AN APPOINTMENT WHEN THE RECEIPT OR ORDER IS ON A LOAD <a id="entering-an-appointment-when-the-receipt-or-order-is-on-a-load"></a>

If the receipt or order has been added to a load, you can enter the load number in APPL and the appointment will be assigned to all receipts or orders on that load. To add receipts to loads, use RCLO (Receipt Loading); 
to add orders to loads, use SELO (Set Up Load).
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.
4 In the Inbound/Outbound/Load field, select the appropriate value from the dropdown list: Inbound Load or Outbound Load.
5 In the Document Number field, key in your load number and press Enter or select your load number from the pick list.
6 Continue entering your appointment information normally.
To create another appointment: To exit APPL:
a) Click on New.
b) Repeat the above steps for your second appointment.
a) Click on Return.
b) Click on Exit.

OPERATIONS 2 GUIDE 4.2* 21

### CREATING AN INBOUND LOAD <a id="creating-an-inbound-load"></a>

You can create an inbound load and attach receipts to it while working in APPL. You can also create inbound loads in the stand-alone program RCLO (Receipt Loading).
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.
4 In the Inbound/Outbound/Load field, select Inbound Load.
5 Click on Create a Load.
RCLO screen
6 In the Receipt Date field, click on the calendar and select your anticipated receipt date.
7 Select your driver from the driver picklist.
8 If required, key in your carry unit and power unit information.
9 If required, key in your seal number, voyage/vessel, temperature and load reference information.
10 Click on the Receipt field and key in the receipt number for each receipt on the load. The receipt details will auto-populate for each receipt.

RCLO screen showing two receipts on load number 6 
11 Click on Save. 
12 Do one of the following:
To advance the flow of all receipts on the load: To skip this step:
a) Click on CHRF screen.
b) Advance the flow of the receipt(s) in the normal manner.
a) Proceed to next step.

OPERATIONS 2 GUIDE 4.2* 23
CHRF screen showing next flow for inbound load 6
13 Click on Exit to return to APPL.
14 In the Document Number field, click on the pick list to select your recently created inbound load.
15 Continue to enter your inbound appointment information normally.

### CREATING AN OUTBOUND LOAD <a id="creating-an-outbound-load"></a>

You can create an outbound load and attach orders to it while working in APPL. You can also create outbound loads in the stand-alone program SELO (Set Up Load).
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.
4 In the Inbound/Outbound/Load field, select Outbound Load.
5 Click on Create a Load.

SELO screen
6 Proceed to create a load in the normal manner.
7 When you finish creating your load, click on Exit to exit.

### ATTACHING MULTIPLE OUTBOUND LOADS TO AN APPOINTMENT <a id="attaching-multiple-outbound-loads-to-an-appointment"></a>

1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.
4 In the Inbound/Outbound/Load field, select Outbound Load.
5 Create your appointment in the normal manner.
6 Click on Multiple Outbound Loads.
APPL screen showing pick lists for multiple outbound loads
7 Select your outbound loads from the pick lists.
8 Click on Save. 

OPERATIONS 2 GUIDE 4.2* 25
9 Click on Exit .

### ENTERING AN APPOINTMENT WITHOUT A RECEIPT OR AN ORDER <a id="entering-an-appointment-without-a-receipt-or-an-order"></a>

If you wish to set up your appointment before entering your order or receipt, you must specify the following in 
APPL:
 a customer/shipper (inbound only)
 a customer/consignee (outbound only)
 a carrier 
The load type, customer/shipper, customer/consignee and carrier serve as restrictions on your appointment. 
When you enter your receipt or order and wish to assign an appointment to it, only those appointments whose carrier and customer/shipper or customer/consignee match the carrier and customer/shipper or customer/ consignee on the receipt or order will be available.
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Click on Set Up Appointment.

APPL screen showing set up appointment mode
TIP You can set up multiple appointments in APPL — for example, 10 appointments over the next week — and assign them to orders and receipts as they are required.

4 In the Inbound/Outbound/Load field, select the appropriate value from the dropdown list. You select 
Inbound if the appointment is for a receipt, Outbound if the appointment is for an order or Load if the appointment is for an outbound load.
5 In the Account Type field, do one of the following:
6 In the Carrier field, do one of the following:
7 Select your load type code from the dropdown list. 
8 Do one of the following.
9 If door entry is mandatory for your appointments, select your door code from the dropdown list.
10 In the Lapse Time in Minutes field, press Enter to accept the system default for this building or key in a new lapse time in minutes and press Enter.
11 Press Enter to accept the current date as your appointment start date or select a date other than the current date from the pop-up calendar.
If you wish to specify an account type:
If you wish to enter a manual account name:
a) Select the appropriate account type (customer, shipper, consignee) from the dropdown list.
b) In the Code field, select the appropriate code from the dropdown list.
a) Select Manual from the dropdown list.
b) In the Name field, key in your manual name.
If you wish to enter a carrier code:
If you wish to enter a manual carrier name:
a) Select your carrier from the pick list.
a) In the Name field, key in a forward slash (“/”) followed by your carrier name.
If the load type that you entered is based on weight:
If the load type that you entered is based on SKU class:
If the load type that you entered has no weight or quantity breaks:
b) In the Weight field, press 
Enter to accept the weight that is displayed or key in a new weight and press Enter.
c) In the Lapse Time in Minutes field, AccellosOne 3PL will calculate the appointment’s duration in minutes. Press 
Enter to accept this estimate or key in a new value and press Enter.
a) Key in your quantity for that 
SKU class and press Enter.
b) In the SKU Class Number field, select the appropriate 
SKU class from the dropdown list.
c) In the Lapse Time in Minutes field, AccellosOne 3PL will calculate the appointment’s duration in minutes. Press 
Enter to accept this estimate or key in a new value and press Enter. 
a) Press Enter twice to bypass the Weight Measure Code and 
SKU Class fields. 
b) In the Lapse Time in Minutes field, key in the number of minutes required for the appointment and press Enter.

OPERATIONS 2 GUIDE 4.2* 27
12 Key in your start time in 24-hour format and press Enter. Based on your lapse time in minutes, AccellosOne 3PL will populate the End Date and End Time fields with the appropriate values.
13 If required, key in a reference number and press Enter.
14 If required, key in a contact name for the appointment and press Enter.
15 If required, key in the name of the warehouse supervisor and press Enter. If there is no warehouse supervisor for this appointment, press Enter to bypass this field.
16 If required, key in a load description and press Enter.
17 When you finish adding your appointment, click on Save. AccellosOne 3PL will display an appointment number; you use this number if you wish to look up your appointment or make changes to it.

Appointment Planner (APPL) screen showing an inbound appointment for building 01 with no assigned receipt
18 Click on Return to exit set up appointment mode.
19 Click on Exit to exit.
NOTE If AccellosOne 3PL fails to calculate the loading or unloading time and select a time slot and door, check your load type in LOAD and make sure that there is a weight or quantity break for the weight or quantity that you entered. For example, if you enter a weight of 5,100 pounds in APPL but your highest weight break in LOAD is 
5,000 pounds, the system will be unable to calculate a lapse time.

### ASSIGNING A DOOR TO AN APPOINTMENT IN CALENDAR VIEW <a id="assigning-a-door-to-an-appointment-in-calendar-view"></a>

If you set up an appointment with no door assigned, you can assign the appointment to a door in Calendar 
View by double clicking on the appropriate door.
1 Enter APPL
2 Go to Calendar View.
Appointment Planner (APPL) screen showing appointment with no door
3 Click on the appointment that you wish to assign to a door to highlight it.
4 Double click on the appropriate door.
The Set Up Appointment window will display for the appointment in step 3 with the Door Code field populated with the door that you selected.

### ENTERING A STANDING APPOINTMENT <a id="entering-a-standing-appointment"></a>

You create a standing appointment by entering a standard or non-standing appointment with the required customer, carrier, consignee, load type, etc. parameters but no order or receipt number. This appointment is a called a parent appointment. Then you use the Standing Appointment command to specify the frequency (daily, weekly, monthly or yearly) and the end date. AccellosOne 3PL will automatically generated the required number of standing appointments.
1 Enter APPL.
2 If required, select your building from the dropdown list.
3 Create a new appointment that is NOT attached to a specific order or receipt.
4 When you finish adding your new appointment, click on Save to save it. 

OPERATIONS 2 GUIDE 4.2* 29

APPL screen showing set up appointment mode
5 Click on Standing Appointment.
Create Standing Appointment screen
6 Select your appointment frequency from the dropdown list.
7 Select your standing appointment end date from the pop-up calendar.
8 Click on Process.
9 When prompted to proceed with the standing appointment, click on Yes.

### ATTACHING YOUR APPOINTMENT TO A SPECIFIC RECEIPT OR ORDER <a id="attaching-your-appointment-to-a-specific-receipt-or-order"></a>

Once you have created your appointment, you attach it to a specific receipt or order in ENRE or ENOR.
1 Enter ENRE or ENOR.
2 Enter the header information of your receipt or order.

Appointment screen showing two appointments for this receipt or order
3 When the Appointment pick list is displayed, use your arrow keys to position your cursor over the appointment that you wish to select. Then click on Select Code.
4 Enter the line block of your receipt or order normally.
5 When you finish your receipt or order, click on Master Block and Exit to exit.

### CREATING APPOINTMENTS IN CHRF <a id="creating-appointments-in-chrf"></a>

If the special verify program CAPR is attached to the workflow profile of the customer whose product you are receiving, you can create a new appointment in CHRF (Time Stamp and Confirm Receipt).
1 Enter ENRE.
2 Enter your receipt in the normal manner.
3 Do one of the following:
4 When you reach the appropriate flow, the CAPR window will display.
If the special verify program 
CAPR is attached to your ENRE flow:
If the special verify program 
CAPR is attached to a later flow:
a) Proceed to next step. a) Enter CHRF and advance the receipt’s flow in the normal manner.

OPERATIONS 2 GUIDE 4.2* 31
CAPR screen showing receipt number
5 Do one of the following:
CAPR screen showing building, door and appointment number
If you wish to create a new appointment for the receipt:
If you do NOT wish to create a new appointment for the receipt:
a) If required, select your building from the New Building dropdown list.
b) if required, select your door from the New Door list.
c) Click on Process.
a) Proceed to next step.

6 Click on Exit to exit.

### CREATING APPOINTMENTS IN CHOF <a id="creating-appointments-in-chof"></a>

If the special verify program CAPO is attached to the workflow profile of the customer whose product you are receiving, you can create a new appointment in CHOF (Time Stamp and Confirm Order).
1 Enter ENOR.
2 Enter your order in the normal manner.
3 Do one of the following:
4 When you reach the appropriate flow, the CAPO window will display.
CAPO screen showing order number
If the special verify program 
CAPO is attached to your ENOR flow:
If the special verify program 
CAPO is attached to a later flow:
a) Proceed to next step. a) Enter CHOF and advance the order’s flow in the normal manner.

OPERATIONS 2 GUIDE 4.2* 33
5 Do one of the following:
CAPO screen showing building, door and appointment number
6 Click on Exit to exit.

### ADDING REMARKS TO AN APPOINTMENT <a id="adding-remarks-to-an-appointment"></a>

If you add remarks to an appointment, they print in SAPR (Scheduled Appointment Report). You can also look them up in the Time Block of LORE (for inbound appointments) and in the Time Block of LOOR (for outbound appointments). If the appointment is attached to a load, all orders on the load will display the remarks.
The following restrictions apply to APPL remarks:
 no individual “word” can exceed 40 characters
 no individual line can exceed 45 characters
 remarks are added in “append” mode rather than “replace” mode (that is, new remarks are added to existing remarks and do not replace them)
1 In either Calendar View or Detail View, click on the appointment to which you wish to add remarks.
2 Click on Appointment Remarks.
3 Key in your appointment remarks.
If you wish to create a new appointment for the order:
If you do NOT wish to create a new appointment for the order:
a) If required, select your building from the New Building dropdown list.
b) if required, select your door from the New Door list.
c) Click on Process.
a) Proceed to next step.

Remarks screen
4 When you finish adding your appointment remarks, click on Save. 

### Looking Up Your Appointments <a id="looking-up-your-appointments"></a>

There are two ways of looking up appointments in APPL: Calendar View and Detail View. Calendar View shows the current month’s calendar. Days with appointments are green in color while days without appointments are white. At the bottom of the screen are the time slots for each door. If there is an appointment in a given time slot, the appointment number preceded by the appropriate prefix (I for Inbound, O for Outbound or 
L for Load) is shown.
Detail View, on the other hand, shows summary information for your appointments. For each appointment, 
Detail View shows the appointment start time and date, lapse time, appointment number, status, door code, load type, document number, account type, account name and carrier. 
Calendar View vs. Detail View

OPERATIONS 2 GUIDE 4.2* 35

### QUERY FIELDS IN APPL <a id="query-fields-in-appl"></a>

The following query fields are available in APPL:
FIELD DESCRIPTIONS (QUERY MODE)
Building Mandatory
The building whose appointments you wish to look up.
Door Options (Calendar 
View)
Show All Doors
Show Only Doors With Appointments
Show Doors Without Appointments
No Doors
In this field, you specify which doors you want to show in your query: all doors, only doors with appointments, only doors without appointments or no doors.
The “No Doors” option consolidates the lines for each door into a single line and shows an asterisk (“*”) in the Door column. 
Door Code The door whose appointments you wish to look up.
Appointment Number The number of the appointment that you wish to look up. If you specify an appointment number, APPL will bypass Calendar View and open Detail View.
Reference Number The document reference number that you enter when you set up a new appointment. This field is a free-text entry field.
Show Only Late AppointmentsAn appointment is considered late if no arrive date has been entered and if the appointment’s start date is later than the system date.
Range in Days Before 
Selected Date / After
Only available in Detail View
In this field, you can specify a range in days from the selected date when working in Detail View. The selected date is the date that you select in Calendar View. For example, if you enter 1 in the Before field and 2 in the After field and click on today’s date, APPL will show yesterday’s appointments, today’s appointments, tomorrow’s appointments and day after tomorrow’s appointments.
NOTE If you do not enter values in the Before Selected Date and After fields, AccellosOne 3PL will show only the current day’s appointments in 
Detail View.

### LOOKING UP APPOINTMENTS IN CALENDAR VIEW <a id="looking-up-appointments-in-calendar-view"></a>

Calendar View shows your appointments in calendar format. At the top of your screen is a calendar showing the current month. The current day is shown in blue, days with appointments are shown in green and days in which the maximum number appointments allowed has been exceeded are shown in red.
Inbound / Outbound / 
Load
Inbound
Outbound
Load
The type of the appointment that you wish to look up. If you select Inbound, the appointment is for an inbound receipt. If you select Outbound, the appointment is for an outbound order. If you select Load, the appointment is for an outbound load.
Document Number The receipt, order or load number of the appointment that you wish to look up. 
If you specify a document number, APPL will bypass Calendar View and open 
Detail View.
Document Reference 
Number
Only available if you select a value in the Inbound/Outbound/Load field
For inbound appointments, the receipt reference number. For outbound appointments, the customer order number. For loads, any order on the load.
Account Type Consignee
Customer
Shipper
The type of account of the appointment that you wish to look up.
Account Code The account code for the account type that you specified in the previous field.
Carrier Code The carrier for the appointment that you wish to look up.
Load Type Code The load type for the appointment that you wish to look up.
Weight >= If you enter a value in this field, only appointments attached to a receipt or order whose weight is greater than or equal to this value will display. This option requires a weight measure code selected from the Weight Measure 
Code dropdown list.
Quantity >= If you enter a value in this field, only appointments attached to a receipt or order whose quantity is greater than or equal to this value will display. 
FIELD DESCRIPTIONS (QUERY MODE)

OPERATIONS 2 GUIDE 4.2* 37
At the bottom of your screen are shown the time slots for each available door. If the time slot has been assigned an appointment, the appointment number preceded by the appropriate prefix — I for Inbound, O for 
Outbound or L for Load — is displayed.
If the value in the Door column shows an asterisk rather than a door code, the appointments in those time slots have no assigned door.
The time slice for each time slot — 15 minutes, 30 minutes, 1 hour, etc. — is based on the value that you entered in the Appointment Time Slice in Minutes field in BLDG.
1 Enter APPL.
2 If required, select the building code of the building that you wish to look up from the dropdown list.
3 Key in your query value(s); for example, your document number, customer code, door options, door code, etc.
4 When you finish entering your query values, click on Execute Query.

Appointment Planner (APPL) screen showing Calendar View
Inbound appointments are indicated by the prefix I for Inbound, outbound appointments are indicated by the prefix O for Outbound and load appointments are indicated by the prefix L for Load.
NOTE Calendar View does not show appointments marked as “Complete” or “Deleted”. If you wish to look up these types of appointments, you must do so in 
Detail View. 
Click on these tabs to see later times
Appointments with no door
If the same door is listed twice, there are overlapping appointments

If an appointment is late, it is indicated by a plus sign (“+”). If a door is closed during a particular time slot, it is indicated by an “X”.
5 The following navigation is available in Calendar View: 
 click on the calendar to see appointments for a specific day
 click on > to scroll forward by month or >> by year
 click on < to scroll backward by month or << by year
 click on the appropriate tab (08:00, 10:00, 14:00) to see appointments for later time slots.
 use your up and down arrow keys to scroll through the list of doors
 place your mouse over a day on the calendar to see the number of inbound and outbound appointments for that day
Calendar showing three inbound appointments and two outbound appointments
6 If you wish to look up an appointment’s basic details without leaving Calendar View, click on the appointment number and then click in the More field.
Appointment Planner (APPL) screen showing More pop-up window
7 If you want to look up the full details on a specific appointment, double click on it.

OPERATIONS 2 GUIDE 4.2* 39

Appointment Planner (APPL) screen showing appointment details
8 If you double clicked on an appointment to look up the full details, click on Return to close the Set 
Up Appointment window.
9 When you finish looking up your appointments, click on Exit to exit.

### LOOKING UP APPOINTMENTS IN DETAIL VIEW <a id="looking-up-appointments-in-detail-view"></a>

Detail View shows a simple listing of appointments with no calendar, no legend and no time slots for individual doors. Unless you specified values in the Range in Days Before Selected Date and After fields in the Enter 
Query window, Detail View shows the current day’s appointments only.
You can sort your appointments in Detail View by start date/time, arrived date/time, appointment number, etc. 
by clicking on the appropriate button.
1 Enter APPL.
2 Key in your search criteria and click on Execute Query to open Calendar View.
3 In Calendar View, click on the date that you wish to look up and click on Toggle Calendar View/
Detail View.

Appointment Planner (APPL) screen showing Detail View
4 You can sort your appointments by start date/time, arrived date/time, appointment number, door, document number, reference, account type/name and carrier. Click once on the appropriate button to sort your appointments in ascending sequence (lowest value first). Click again on the same button to sort your appointments in descending sequence (highest value first).
5 Do one of the following:
6 If you wish to look up the appointment’s order or receipt, click on the appointment and then click in the 
More field. If the appointment is attached to a load rather than an order, the More command will show all orders on the load.
If you wish to query by status:
If you wish to restrict your query to certain appointments:
a) Select the appropriate status from the Filter by Status dropdown list. 
a) Click on Enter Query and perform a normal query.

OPERATIONS 2 GUIDE 4.2* 41
Detail View showing More pop-up window with receipt number
7 If you wish to look up the details of a particular appointment, double click on it. When you finish looking up the details, click on Return to close the Set Up Appointment window.
8 When you finish looking up your appointments, click on Exit to exit.

### LOOKING UP APPOINTMENTS IN SET UP APPOINTMENTS <a id="looking-up-appointments-in-set-up-appointments"></a>

If the appointment is not completed or deleted, you can look it up in Set Up Appointments.
1 Make sure that you are in Set Up Appointments.
2 Click on Enter Query.

Set Up Appointment window in query mode
3 Key in your search criteria and click on Execute Query. 

4 If the appointment is attached to a receipt, order or load, you can look up the receipt/order/load details by clicking on Order/Receipt/Load Details.
5 When you finish looking up your receipt/order/load details, click on Exit or Return to return to Set Up 
Appointments.

### LOOKING UP ORDERS ON A LOAD <a id="looking-up-orders-on-a-load"></a>

If the appointment is attached to a load rather than an order, you can look up all orders on the load by clicking on the Document Number pick list.
1 Make sure that you are in Set Up Appointments.
2 Click on Enter Query.
3 Key in your search criteria and click on Execute Query. 
4 When you find the load that you are looking for, click on Pick List for the Document Number field.
Document Number pick list in APPL showing orders on load 126
5 Click on Return to exit the pick list.

### Updating the Status of Appointments <a id="updating-the-status-of-appointments"></a>

An appointment can have one of five statuses in AccellosOne 3PL:
STATUS REMARKS
Created the appointment has not been flagged as cancelled, deleted, arrived or complete
Cancelled the appointment was cancelled
Deleted the appointment was deleted

OPERATIONS 2 GUIDE 4.2* 43

### UPDATING THE STATUS OF AN APPOINTMENT <a id="updating-the-status-of-an-appointment"></a>

AccellosOne 3PL tracks two dates for an appointment: the arrival date and the completed date. When you update the status of an appointment, AccellosOne 3PL adds the information to the Time-Stamping Block in 
LORE and LOOR.
1 Enter APPL.
2 Key in your search criteria and click on Execute Query to open Calendar View.
3 In Calendar View, click on the date that you wish to look up.
4 Double click on the appointment whose status you wish to update.

Appointment Planner (APPL) screen showing Change Status dropdown list
5 Select the appropriate option from the Change Status dropdown list.
6 Select your date from the pop-up calendar.
7 If required key in a time. If you do not key in a time, AccellosOne 3PL will use the time 00:00; that is, no time was entered.
8 Click on Save.
Arrived an arrival date was entered for the appointment
Complete a completion date was entered for the appointment
NOTE Completed appointments are automatically deleted.
STATUS REMARKS

Appointment Planner (APPL) screen showing new status
9 Click on Return.
10 Click on Exit to exit.

### CLEARING AN APPOINTMENT <a id="clearing-an-appointment"></a>

If an appointment has a status of Arrived or Completed, you can clear the status so that the appointment is “unarrived” or new.
1 Enter APPL.
2 Key in your search criteria and click on Execute Query to open Calendar View.
3 In Calendar View, click on the date that you wish to look up.
4 Double click on the arrived or completed appointment that you wish to clear.
5 Select Clear from the Change Status dropdown list.
6 Click on Save.
7 Click on Return.
8 Click on Exit to exit.

### DELETING AN APPOINTMENT <a id="deleting-an-appointment"></a>

You delete appointments in the following cases:

OPERATIONS 2 GUIDE 4.2* 45
 You made the appointment in error and you wish to permanently remove it from APPL.
 The appointment was cancelled by the customer, shipper or consignee. If the appointment was cancelled by the carrier, you should use the Cancel function.
When you delete an appointment, the appointment can no longer be attached to a receipt or to an order in 
ENRE or ENOR. Although the appointment remains in Detail View, it does not display in Calendar View. 

### DELETING A STANDING APPOINTMENT <a id="deleting-a-standing-appointment"></a>

When you delete a standing or parent appointment, you have two options: 
 you can delete the parent appointment only and leave all the related child appointments active
 you can delete both the parent appointment as well as all the related child appointments
1 Go to Set Up Appointment.
2 Click on Enter Query.
3 In the Appointment Number field, key in your parent appointment number and click on Execute 
Query.
APPL screen showing parent appointments 175
4 Select Deleted from the Change Status dropdown list.
5 Click on Save.

APPL screen showing prompt to delete all child appointments
6 Do one of the following:

### CANCELLING AN APPOINTMENT <a id="cancelling-an-appointment"></a>

You cancel an appointment when the appointment was cancelled by the carrier. If you entered the appointment in error or if the appointment was cancelled by the customer, shipper or consignee, you should use the Delete function.
A cancelled appointment cannot be assigned to a receipt or to an order. You can undo a cancel at any time by selecting the Clear option from the Change Status dropdown list. When you clear or undo a cancel, the appointment becomes a regular appointment and can be assigned to a receipt or to an order. An appointment with a date in the Arrived Date field cannot be cancelled.

### LOOKING UP AN APPOINTMENT’S HISTORY <a id="looking-up-an-appointment-s-history"></a>

The History window shows each action that was performed on a given appointment, the date and time that this action was performed and the operator who performed it. 
1 In either Calendar View or Detail View, click on the appointment whose history you wish to look up.
2 Click on History.
If you wish to delete all child appointments for the parent appointment:
If you wish to delete the parent appointment only:
a) Click on Yes. a) Click on No.

OPERATIONS 2 GUIDE 4.2* 47
APPL screen showing Time Stamp window
3 When you finish looking up the appointment’s history, click on Click on Return twice.
4 Then click on Exit to exit.

### MODIFYING APPOINTMENT INFORMATION <a id="modifying-appointment-information"></a>

If you wish to modify an appointment (that is, reschedule it to another door or to another time/date or change the quantity), you retrieve the appointment in APPL and make the required changes.

### Reports <a id="reports"></a>

See the Standard Reports Guide.

OPERATIONS 2 GUIDE 4.2* 49

## Operational Board <a id="operational-board"></a>

*Manual E — Operations 2*

Attaching Labor Standards and Labor Standard Modifiers to Workflow Profiles 

### Overview <a id="overview"></a>

The Operational Board is a powerful resource management tool that allows you to look up open orders and receipts to find out what percentage of the work has been completed and what percentage of the work remains to be done. You can restrict your query of open orders and receipts by company code, warehouse code, customer code, carrier code and many other search parameters.
Each query that you perform in the Operational Board will show the following information: 
 the number of open orders and receipts
 the number of lines on those orders and receipts
 the completed quantities and the percentage that the completed quantities represent of the total number of open orders and receipts
 the remaining quantities and the percentage that the remaining quantities represent of the total number of open orders and receipts
If you define labor standards, the Operational Board will use those labor standards to calculate the number of hours and minutes that it took to perform the completed work as well as the number of hours and minutes required to finish the remaining lines.

### UNDERSTANDING LABOR STANDARD MODIFIERS <a id="understanding-labor-standard-modifiers"></a>

Labor standard modifiers are the degree to which a particular customer, item, carrier, consignee, etc. deviates from your labor standards. The default value for all labor standard modifiers is 1.00. For example, suppose it normally takes three minutes to pick a pallet. However, the pallets of Customer A are difficult to pick and you assign them a factor of 1.5. Sometimes Customer A’s pallets are stored in aisle 7 and because this aisle is close to the door, pallets stored in this aisle are easier to pick and you assign them a factor of .85.
The final calculation for picking one pallet for Customer A from aisle 7 would be:
3 minutes (the labor standard) X 1.5 X .85 (the labor standard modifiers) = 3.825 minutes 
Labor standard modifiers can be attached to the following entities. If you do not attach a labor standard modifier to these entities, the system assumes a value of 1 (that is, no modifier).
 customers
 items
 carriers
 locations
 location types
 consignees
 shippers
 warehouses
 warehouse zones
 load types
NOTE The Operational Board can be used with both non-RF or manual labor tracking as well as RF labor tracking. However, if you use non-RF labor tracking, you must advance your receipt and order flows promptly in CHRF/CHOF in order to generate meaningful data in the Operational Board.

OPERATIONS 2 GUIDE 4.2* 285
Labor standard modifiers can be applicable to all processes in the warehouse or they can be limited to processes that you define. For example, the labor standard modifier for Customer ABC is 1.2 but this factor applies only to the loading and unloading processes.
LSOA LSMP
FLPR
CUST
CUST
ITEM
CARR
LOCA
LOTP
CONS
SHIP
WARE
WHZO
LOAD
You set up your labor standards in this program
You activate the modifiers in this program
You define your modifier values in these programs
You attach your labor standards and your modifiers to your flow process

Operational Board screen showing query results for open orders

### UNDERSTANDING OPERATIONAL BOARD CALCULATIONS <a id="understanding-operational-board-calculations"></a>

The completed vs. remaining quantities and percentages are based on the quantities on a given receipt or order line that are currently at a particular flow.
In the following example, there are three receipts from three different customers and each customer has a different DIFP profile. The flows themselves are the same for all profiles, but the sequence of the flows is different. For simplicity’s sake, we assume that each receipt line has one pallet and that according to our labor standard it takes five minutes to unload, put-away, pick and load one pallet.
The sequence of flows in the Flows window is: flow 5, flow 3, flow 6, flow 1, flow 2, flow 4, flow 7 and flow 8. 
This sequence is based on the Inbound Sequence Number field in FLPR. In the following example, we will calculate completed vs. remaining quantities and percentages at flow 5.
RECEIPT 1
All lines on this receipt are at flow 3, which precedes flow 5. Therefore, all five pallets on this receipt are considered to be remaining rather than completed.
General filter Normal mode vs. full-screen mode button Results window

OPERATIONS 2 GUIDE 4.2* 287
RECEIPT 2 (RF LABOR TRACKING ONLY)
Two lines on this receipt are at flow 3 and therefore incomplete. However, four lines on this receipt are at flow 
5 and have been completed.
RECEIPT 3 (RF LABOR TRACKING ONLY)
All lines on this receipt are at flow 1 or 2, which follow flow 5. Therefore, all lines have been completed.
Line # Flow
Lines at 
Flow 5
Completed 
Pallets
Remaining 
Pallets
Completed 
Minutes
Remaining 
Minutes DIFP Profile
1 Flow 3 0 0 1 0 5 Flow 2
Flow 3
Flow 4
Flow 5
Flow 1
2 Flow 3 0 0 1 0 5
3 Flow 3 0 0 1 0 5
4 Flow 3 0 0 1 0 5
5 Flow 3 0 0 1 0 5
Line # Flow
Lines at 
Flow 5
Completed 
Pallets
Remaining 
Pallets
Completed 
Minutes
Remaining 
Minutes DIFP Profile
1 Flow 3 0 0 1 0 5 Flow 6
Flow 1
Flow 2
Flow 3
Flow 5
2 Flow 5 1 1 0 5 0
3 Flow 5 1 1 0 5 0
4 Flow 3 0 0 1 0 5
5 Flow 5 1 1 0 5 0
6 Flow 5 1 1 0 5 0
Line # Flow
Lines at 
Flow 5
Completed 
Pallets
Remaining 
Pallets
Completed 
Minutes
Remaining 
Minutes DIFP Profile
1 Flow 1 0 1 0 5 0 Flow 3
Flow 4
Flow 5
Flow 1
Flow 2
2 Flow 2 0 1 0 5 0
3 Flow 2 0 1 0 5 0
4 Flow 2 0 1 0 5 0

The Operational Board will show the following remaining vs. completed calculations for flow 5:

### ROUNDING RULES FOR SECONDS <a id="rounding-rules-for-seconds"></a>

The Operational Board does not display seconds when showing the number of hours and minutes needed to complete a given activity. If the number of minutes is greater than one, normal rounding rules apply (that is, round up if .5 or more; otherwise, round down). If the number of minutes is less than one (for example, 20 seconds), the number of minutes is rounded up to one minute.
When calculating totals, the Operational Board use hours, minutes and seconds to arrive at a given total. The total is displayed in hours and minutes only and seconds are rounded up or down in the usual manner: that is, if greater than one minute apply normal rounding rules and if less than one minute round up to one minute.

### Setting Up the Operational Board <a id="setting-up-the-operational-board"></a>

There are a maximum of eight steps to follow in setting up the Operational Board:
1 you assign access to the Operational Board in OPAC and COAC
2 you set up your labor standards in LSOA
3 you set up your labor standard modifiers in LSMP (if required)
4 you attach your labor standards and labor standard modifiers to your flows in FLPR
5 if your labor standards and labor standard modifiers vary by customer, you must attach your labor standards to the appropriate workflow profile in DIFP
6 if you use labor standard modifiers, you must define your modifier values in the appropriate program (CUST, ITEM, LOCA, etc.)
7 if you wish to apply your new labor standards to existing orders and receipts, you must run the program 
ULSO (Update Labor Standard for Open Documents)
8 if required, you adjust the Report Process value in IQBP for each SKU type in an item’s quantity breakdown

### SETTING UP ACCESS TO THE OPERATIONAL BOARD <a id="setting-up-access-to-the-operational-board"></a>

You assign access to the Operational Board as you would to any other AccellosOne 3PL program. The 
Operational Board has been assigned the job selection code of ADDASH and you grant access to it by giving your company and operators access to ADDASH. ADDASH is attached to the ACTIVE menu.
Lines at 
Flow 5
Completed 
Pallets
Remaining 
Pallets
Completed 
Minutes
Remaining 
Minutes
Percentage 
Complete
Percentage 
Remaining
4 (receipt 2) 8 (4 from receipt 2 and 4 from receipt 
3)
7 (2 from receipt 2 and 5 from receipt 
1)
40 (5 X 8) 35 (5 X 7) 53.3 (40 divided by 75)
46.7 (100 - 
53.3)

OPERATIONS 2 GUIDE 4.2* 289

### SETTING UP LABOR STANDARDS IN LSOA <a id="setting-up-labor-standards-in-lsoa"></a>

In this program, you define your labor standards. Currently, LSOA supports pieces per man hour only, which has been assigned a UOM (Unit of Measure) code of 3. In the Measure Block, you enter your pieces per man hour code (3) and the number of pieces per hour for the appropriate SKU class (for example, 100 cases per hour or 10 pallets per hour or 350 eaches per hour, etc.).
If certain SKU classes do not apply to your inventory because they are not part of an item’s quantity breakdown or are too small to be received or shipped, set the number of pieces per man hour to zero.
If the labor standards that you define in LSOA apply to all inventory in your warehouse that belongs to the currently selected company, you attach them to the appropriate flows in FLPR (Flow Process). If, on the other hand, your labor standards differ by customer, you must set up a separate labor standard for each customer whose labor standards are unique and then attach this labor standard profile code to the customer’s workflow profile code in DIFP (Depositor Workflow Profile).
You can also define labor standards that are shipper or consignee dependent. That is, the normal labor standard for picking customer A’s product is 100 units per hour, but when shipping to a given consignee the labor standard is 75 units an hour. To set up shipper or consignee-dependent labor standards for a customer, you must define a custom workflow profile in DIFP and attach it to the appropriate shipper or consignee.
1 Enter LSOA.
2 Key in your profile code and press Enter.
3 Key in a description for your profile code and press Enter.
4 In the Weight Measure Code field, select any code from the pick list. This field is reserved for future use.
5 In the Linear Measure Code field, select any code from the pick list. This field is reserved for future use.
6 Press Enter to position your cursor in the Measure Block.
7 In the UOM field, key in 3 and press Enter.
8 In the PLT field (if your highest SKU class is defined as pallets), key in the number of pallets that can be processed in one man hour for the current labor standard profile code and press Enter. If you do not wish to capture labor standards for your SKU class of pallets, key in zero.
9 Repeat the previous step for the remaining four SKU classes.
10 When you finish setting up your labor standards, click on Return to Main to exit create record mode.

LSOA screen showing a labor standard of 10 pallets and 50 cases per man hour 
11 If required, you can assign task profile codes to a UOM code by clicking on Task Profile to enter the Task Profile Block.
LSOA screen showing Task Profile (REGI) Block
12 If required, enter your task profile records for the UOM code.

OPERATIONS 2 GUIDE 4.2* 291
LSOA screen showing different labor standards based on task profile codes
13 If you entered task profile records in the previous step, click on Save to save your new records.
14 Click on Master Block and Exit to exit.

### SETTING UP LABOR STANDARD MODIFIER CODES IN LSMP <a id="setting-up-labor-standard-modifier-codes-in-lsmp"></a>

In this program, you set up your labour standard modifier profile codes. This profile allows you to specify for a given flow in DIFP which labour standard modifiers are activated. For example, you can set up profile 1 in which all modifiers are activated (item, customer, warehouse, etc.) and profile 2 in which only the location and location type modifiers are activated.
The number of labor standard modifier profile codes that you require depends upon which entities (CUST, 
ITEM, LOCA, WARE, etc.) have modifier values and whether these modifier values apply to all flows. For example, if you have modifier values for items and locations only and these values apply to all flows, you would set up a single modifier profile code in LSMP. 
If, on the other hand, you have modifier values for items, locations and carriers and the item/location values apply to picking only while the carrier values apply to loading only, you would have to set up two modifier profile codes in LSMP. 
Codes defined in LSMP are attached to either FLPR (Flow Process) or DIFP (Depositor Workflow Profile).
When you add a new record to LSMP, AccellosOne 3PL will time-stamp it with the date that the record was added and the operator who added it.
FIELD DESCRIPTIONS
Labor Standard Modifier 
Code
Mandatory
Your labor standard modifier code.

1 Enter LSMP.
Description Mandatory
Your description.
ITEM If you select this checkbox, any item modifier values set up in ITEM will be activated.
WARE If you select this checkbox, any warehouse modifier values set up in WARE will be activated.
CUST If you select this checkbox, any customer modifier values set up in CUST will be activated.
SHIP/CONS If you select this checkbox, any shipper or consignee modifier values set up in 
SHIP or CONS will be activated.
OPER Reserved for future use.
LOCA If you select this checkbox, any location modifier values set up in LOCA will be activated.
LOTP If you select this checkbox, any location type modifier values set up in LOTP will be activated.
CARR If you select this checkbox, any carrier modifier values set up in CARR will be activated.
LOAD If you select this checkbox, any load type modifier values set up in LOAD will be activated.
MHET If you select this checkbox, any material handling equipment type modifier values set up in MHET will be activated.
ZONE If you select this checkbox, any warehouse zone modifier values set up in 
ZONE will be activated.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 293

LSMP screen
2 Click on New.
3 Key in your labor standard modifier profile code and press Enter.
4 Key in a description for your new code and press Enter.
5 Proceed to select the checkboxes representing which modifiers you wish to activate for your profile.
6 When you finish activating your modifiers, click on Save.
7 Repeat the above steps for any additional modifier profiles that you wish to set up.

LSMP screen showing two labor standard modifier profiles
8 When you finish setting up your labor standard modifier profiles, click on Exit to exit.

### ATTACHING MODIFIER VALUES TO THE APPROPRIATE ENTITY <a id="attaching-modifier-values-to-the-appropriate-entity"></a>

In these programs, you retrieve the individual record that you wish to modify in CUST, ITEM, WARE, etc. and enter the appropriate modifier value.
1 Enter the program (ITEM, CUST, WARE, etc.) whose modifier values you wish to change.
2 Retrieve the record that you wish to set up.
3 Press Enter until your cursor is positioned in the Labor Standard Modifier field.
4 Key in the appropriate value and press Enter.
Timestamp of new record

CUST screen showing labor standard modifier set to 1.5
5 When you finish entering your value, click on Return to Main and Exit.
ATTACHING LABOR STANDARDS AND LABOR STANDARD MODIFIERS TO 
FLOWS IN FLPR
In this program, you attach your labor standard profile code and labor standard modifier code (if any) to the appropriate flow, specify whether or not you want receipts and orders at the flow that are late to be flagged and the sequence of the flow on the Flows window of the Operational Board.
The labor standard profile codes and labor standard modifier codes that you attach to flows in FLPR are system defaults. You can override these defaults in DIFP. If you do not define defaults in FLPR, you must attach your labor standard profile codes and labor standard modifiers (if any) to flows in DIFP.
You attach your labor standard profile codes and labor standard modifier codes to the flow process code that signifies the end of the activity that you wish to track. For example, if you have two flows for picking — STPI (Start Picking) and FIPI (Finish Picking) — and you wish to track picking, you would attach your labor standard profile code and labor standard modifier code to the FIPI flow.
FIELD DESCRIPTIONS
Flow Process Your flow process code.
Priority Reserved for future use.
Activity Type Reserved for future use.

OPERATIONS 2 GUIDE 4.2* 295
1 Enter FLPR.
Labor Standard Profile 
Code
Optional
The labor standard profile code for this flow process. If you do not attach your labor standard profile code to your flow process in FLPR, you must do so in 
