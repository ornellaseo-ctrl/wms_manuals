---
title: "Workflow (DIFP) e Labor Tracking"
description: "Perfil de workflow do depositante, flow process, padrões de mão de obra e modificadores."
layout: default
---

# Workflow (DIFP) e Labor Tracking

Perfil de workflow do depositante, flow process, padrões de mão de obra e modificadores.

**Fluxo principal:** `DIFP (workflow) -> FLPR (flow) -> LSOA/LSMP (labor standards)`

> Fonte: manuais E do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Labor Tracking <a id="labor-tracking"></a>

*Manual E — Operations 2*

### Overview of Manual Time-Stamping <a id="overview-of-manual-time-stamping"></a>

Labor tracking with manual time-stamping allows you to track labor productivity for any inbound or outbound process. You can track all inbound/outbound flows in your workflow profile or you can track a specific range of flows (for example, from flow STPI to flow ENPI if you wish to track picking only). You can also track tasks beyond the scope of normal receiving and shipping if labor tracking is activated for the CRM (Customer 
Relationship Management) system.
For each range of flows that you track, AccellosOne 3PL captures the order/receipt number, the operator, the total number of units, the total weight and the total elapsed time.
The total elapsed time is based on the times that you advance the flow in CHRF/CHOF. For example, suppose your outbound flow sequence is ENOR, STPI, ENPI and COOR and your job type covers the flows 
STPI/ENPI. If you advance to the flow STPI at 8:00 am and advance to the flow ENPI at 10:30 am, the total elapsed time for the job type will be two hours 30 minutes.
With this information, you can calculate the number of pieces or weight processed per hour. You report on labor productivity by running the appropriate query in d’Amigo. The standard templates for labor tracking are found in the Labor folder; you access this folder by clicking on Open Template.

### Overview of RF Labor Tracking <a id="overview-of-rf-labor-tracking"></a>

RF labor tracking allows you to track labor productivity for the following RF programs: RFCH, RFPU, RFPIC, 
RFPK, RFRL, RFRP, RFOPS RFIPS and OLOP.
RF labor tracking does not support a range of flows. You can only track a single flow at a time.
NOTE Labor tracking with manual time-stamping tracks labor productivity at the receipt/order header level only. You cannot track labor productivity for individual receipt or order lines. 
For example, suppose you have five lines on an order of which four have been picked and one has not been picked. For labor tracking purposes, the entire order will be considered to be at the flow STPI (Start Picking) even though four of the lines are in fact at the flow ENPI (End Picking).
NOTE RF labor tracking tracks labor productivity at the location line level if the receipt or order line has been assigned a location. If the receipt or order line has not been assigned a location, AccellosOne 3PL will assign the receipt/order header’s flow to the receipt or order line. 

OPERATIONS 2 GUIDE 4.2* 267
RF labor tracking tracks two types of time for each activity: direct time and idle time. Direct time is the time between the start time and end time of a given activity. Idle time, on the other hand, is the time between the end time of the previous activity and the start time of the next activity. 
There are two types of idle time: Sign On/Off Menu time and Log In/Out Program time. Sign On/Off 
Menu time is the time spent on the RF menu without entering an RF program. Log In/Out Program time, on the other hand, is time spent in an RF program without locking an individual record.
Consider the following example in which an operator picks three order lines in RFPIC:
You report on RF labor productivity by running the Labor Productivity Time History Report (LPTH) and Labor 
Productivity Summary History Report (LPOH).

### OVERLAPPING ACTIVITIES <a id="overlapping-activities"></a>

Overlapping activities typically occur in case picking when an operator picks two or more order lines before proceeding to a staging or dock location to drop off the product. For example, suppose an operator picks line 
1 of an order at 8:00 am, line 2 of the same order at 8:10 am and line 3 of the same order at 8:15 am. All three lines are placed in a staging location at 8:20.
 Operator logs into 
 Operator starts picking line 
 Operator finishes picking line 
 Operator starts picking line 
 Operator finishes picking line 
 Operator exits RFPIC
 Operator re-enters RFPIC
 Operator starts picking line 
 Operator finishes picking line 
Sign In/Off Menu time
Direct time
Log In/Off Program time
Direct time
Log In/Off Program time
Sign In/Off Menu time
Log In/Off Program time
Direct time
Total time = time between starting one activity and starting the next activity (that is, direct time plus idle time)

The direct time for all three lines is based on the longest activity — line 1 — and is 20 minutes (8:00 am to 
8:20 am). Indirect time, if any, is based on the end time of the three lines and the start time of the next transaction.
Overlapping activities are indicated by a sequence number in the Sequence column of LPTH. For example, in the previous example, all three orders lines would be assigned the same sequence number:1/1/1 or 5/5/5 or 
10/10/10, etc.

### Overview of CRM Labor Tracking <a id="overview-of-crm-labor-tracking"></a>

The Customer Relationship Management (CRM) system allows you to enter work requests and problems into the system for tracking and resolution purposes. You enter your work requests in CRME (CRM Entry) and manually record the elapsed time taken to complete each work request.
Because CRM labor tracking is designed to track events outside of normal shipping and receiving, it is a manual system that does not take into account AccellosOne 3PL time-stamping in CHRF and CHOF.

### Setting Up Your Job Type Codes in JBTP <a id="setting-up-your-job-type-codes-in-jbtp"></a>

You set up your job type codes in JBTP (Job Type Code). Job type codes define the flow or range of flow codes whose labor productivity you wish to track. You set up one job type code for each flow or range of flows that you wish to track. The job type code that you create in JBTP is attached to the Labor Block of the appropriate profile in DIFP.
The setup of job type codes in JBTP is only required for manual time-stamping. The necessary job type codes for RF labor stamping are preloaded in JBTP and do not require setup.
JOB TYPE CODE ACTIVITY TYPE RF PROGRAM
LO (Loading) Loading OLOP
P1 (Picking) Picking RFPIC
PU (Put-Away) Put-Away RFPU
RE (Replenishment) Replenishment RFRP
RF (Relocation) Relocation RFRL
UN (Unloading inbound) Receiving RFCH
UNO (Unloading outbound) Unloading outbound OLOP unload
LOGM (Log On/Off Menu) Sign In/Off Menu N/A

OPERATIONS 2 GUIDE 4.2* 269
LOGP (Log In/Out Program) Log In/Out Program N/A
FIELD DESCRIPTIONS
Job Type Code Your job type code.
Description A description for your job type code.
Direct Activity Yes
No
A direct activity is any activity directly related to a receipt or order such as restacking pallets while unloading. An indirect activity is a miscellaneous type activity such as a CRM issue or maintenance issue such as changing the battery of a forklift truck.
Activity Type Adjustment (reserved for future use)
Cycle Count (reserved for future use)
Inventory Count Back (reserved for future use)
Item Process Tracking Inbound
Used in RFIPS.
Item Process Tracking Outbound
Used in RFOPS.
Order Move (reserved for future use)
NOTE Activity types are only available if they have not been assigned to a job type. That means that a given activity type cannot be assigned to more than one job type.
CRM Code Only available for incident tracking in RFINC
If you attach a CRM code to a job type, RFINC will create a CRME record for the incident.
Charge Code Only available for incident tracking in RFINC
If you attach a charge code to a job type, RFINC will create an accessorial charge for the incident.
JOB TYPE CODE ACTIVITY TYPE RF PROGRAM

1 Enter JBTP.
2 Click on New.
3 Key in your job type code and press Enter.
4 Key in a description for your code and press Enter.
5 Click on Save to save your changes.
6 Repeat the above steps for each additional job type code that you wish to set up.

JBTP screen showing job type code for manual time-stamping
7 When you finish setting up your job type codes, click on Exit to exit.

### SETTING UP A JOB TYPE CODE FOR RFINC <a id="setting-up-a-job-type-code-for-rfinc"></a>

You set up a job type code for RFINC (RF Incidents) by leaving the Activity Type field blank for miscellaneous. 
The CRM Code and Charge Code fields are both optional.
Location Bill Code Only available for incident tracking in RFINC and if invoicing by warehouse is activated in COMP (Company Parameters)
The charge code’s location bill code.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 271
JBTP screen showing job type for RFINC (Activity Type = blank)

### Attaching Your Job Type Codes to Your Flows in DIFP <a id="attaching-your-job-type-codes-to-your-flows-in-difp"></a>

If you are setting up non-RF or manual labor tracking, you must attach your job type code to the appropriate range of flows in the Labor Block of DIFP. In order to be valid, a range of flows must meet the following conditions:
 the flow must be defined in the Flow Block
 the to flow cannot be the same as the from flow
 the to flow must have a higher sequence number than the from flow
If required, two separate job types can contain a range of overlapping flow codes. For example, your first job type could include all flows between ENOR/COOR while your second job type could be restricted to the flows 
STPI/ENPI to track picking tasks only.
FIELD DESCRIPTIONS
Sequence The sequence number for the job type.
Starting Flow Mandatory
The starting flow for your job type.
Ending Flow Mandatory
The ending flow for your job type. The ending flow cannot be the same as the starting flow.

1 Enter DIFP.
2 Retrieve the workflow profile code that you wish to set up for labor tracking.
3 Click on In/Out/Repi/Relo Block.
4 Select Inbound or Outbound. Then click on Labor Block.

DIFP screen showing Labor Block
5 Click on Create Record.
6 Key in your sequence number and press Enter.
7 Key in your starting flow code and press Enter or use the pick list function to select it.
8 Key in your ending flow code and press Enter or use the pick list function to select it.
9 Key in your job type code and press Enter or use the pick list function to select it.
Job Type Code (defined in JBTP)
Mandatory
The job type for the range of flows.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 273

DIFP screen showing two job types in the Labor Block
10 Repeat the above steps for each additional flow code/job type combination that you wish to set up.
11 When you finish entering your flow code/job type combinations, click on Return to Main and In/Out/Repi/
Relo Block. Then click on Master Block and Exit to exit.

### DELETING FLOWS IN THE FLOW BLOCK <a id="deleting-flows-in-the-flow-block"></a>

If you delete a flow code in the Flow Block, any records in the Labor Block containing that flow code will be automatically deleted.

### Setting Up Labor Tracking for Non-RF Replenishments <a id="setting-up-labor-tracking-for-non-rf-replenishments"></a>

You can track labor productivity for non-RF replenishments by setting up from and to flow codes for replenishment in the Replenishment Block in DIFP. Your from code must be the system code ENRP (Create Replenishment), while your to code must be the system code REPL (Replenishment Complete).
1 Enter JBTP.
2 Make sure that you have job type RE set up and that this job type is attached to the flow process code 
REPL.

JBTP setup for replenishment tracking
3 Enter DIFP.
4 Retrieve the workflow profile that you wish to set up for labor tracking (relocations).
5 Click on In/Out/Repi/Relo Block.
6 Use your arrow keys to select Relocation.
7 Click on Flow Block, then click on Create Record.
8 Key in 10 as your sequence number and press Enter.
9 Key in REPL (Replenishment Complete) and press Enter.
10 Press Enter to bypass the remaining fields in the Flow Block.
11 When you finish adding your flow, click on Return to Main.

OPERATIONS 2 GUIDE 4.2* 275

DIFP screen showing replenishment setup
12 Click on In/Out/Repi/Relo Block.
13 Click on Master Block and Exit.

### Setting Up Labor Tracking for Non-RF Relocations <a id="setting-up-labor-tracking-for-non-rf-relocations"></a>

You can track labor productivity for non-RF relocations by setting up from and to flow codes for relocation in the Relocation Block in DIFP. Your from code must be the system code ENRL (Generate Relocation), while your to code must be the system code RELO (Relocation Complete). 
1 Enter JBTP.
2 Make sure that you have job type RE set up and that this job type is attached to the flow process code 
REPL.

JBTP setup for relocation tracking
3 Enter DIFP.
4 Retrieve the workflow profile that you wish to set up for labor tracking (relocations).
5 Click on In/Out/Repi/Relo Block.
6 Use your arrow keys to select Relocation.
7 Click on Flow Block, then click on Create Record.
8 Key in 10 as your sequence number and press Enter.
9 Key in RELO (Relocation Complete) and press Enter.
10 Press Enter to bypass the remaining fields in the Flow Block.
11 When you finish adding your flow, click on Return to Main.

OPERATIONS 2 GUIDE 4.2* 277

DIFP screen showing relocation setup
12 Click on In/Out/Repi/Relo Block.
13 Click on Master Block and Exit.

### Setting Up Labor Tracking for the CRM System <a id="setting-up-labor-tracking-for-the-crm-system"></a>

You set up labor tracking for the CRM (Customer Relationship Management) system by assigning a job type code to the appropriate CRM code in CRMC (CRM Codes). If you do not assign a job type code to a CRM code, no labor tracking will occur for the CRM code.
If you enter your work request through the Labor Block in ENRE/ENOR, the total elapsed time is based on the time that you advance the flow in CHRF/CHOF. If you enter your work request in CRME, the total elapsed time is the sum of all times entered manually in the Detail Block of CRME.
1 Enter CRMC.
2 Click on Enter Criteria and Execute Query to display your CRM codes.

CRMC screen showing job types assigned to the codes ORD and RCPT
3 Use your arrow keys to position the cursor over the CRM code that you wish to set up for labor tracking.
4 Press Enter twice to position your cursor in the Job Type Code field.
5 Key in your job type code field and press Enter or use the pick list to select it. To select a code using the pick list, press F10 to display the pick list query screen, then click on Execute Query to display the list of codes. Position your cursor over the appropriate code using your arrow keys and click on Select Code to select it.
6 When you finish assigning your job type code to your CRM code, click on Exit. If Exit is not available, click on Return to Main and Exit.

### Looking Up Labor Information in LORE/LOOR <a id="looking-up-labor-information-in-lore-loor"></a>

You can look up labor information for a given receipt or order in LORE/LOOR. For manual time-stamping, you look up labor information in the CRM Labor / Manual Time-Stamping Block. For RF labor tracking, you look up labor information in the RF Labor Block. For CRM labor tracking, you look up labor information in the CRM 
Labor / Manual Time-Stamping Block.

### LOOKING UP MANUAL TIME-STAMPING INFORMATION <a id="looking-up-manual-time-stamping-information"></a>

The CRM Labor / Manual Time-Stamping Block shows the operator, date and time and elapsed time for each job type.
1 Enter LORE/LOOR.
2 Retrieve the receipt or order whose labor information you wish to look up.
3 Click on Time Block then on CRM / Manual Block.

OPERATIONS 2 GUIDE 4.2* 279

LORE screen showing two job types: one for unloading and one for all inbound flows
4 When you finish looking up your labor information, click on Master Block and Exit to exit.

### LOOKING UP RF LABOR INFORMATION <a id="looking-up-rf-labor-information"></a>

The RF Labor Block shows the start date and time, operator, job type, line number, item, quantity and end date and time for each job type/receipt or order line.
1 Enter LORE/LOOR.
2 Retrieve the receipt or order whose labor information you wish to look up.
3 Click on Time Block then on CRM / Manual Block.
4 Click on RF Labor Block.

LOOR screen showing six RF Labor records
5 When you finish looking up your labor information, click on Master Block and Exit to exit.

### LOOKING UP CRM LABOR INFORMATION <a id="looking-up-crm-labor-information"></a>

The CRM Labor / Manual Time-Stamping Block shows the operator, date and time and elapsed time for each job type.
1 Enter LORE/LOOR.
2 Retrieve the receipt or order whose labor information you wish to look up.
3 Click on Time Block then on CRM / Manual Block.

OPERATIONS 2 GUIDE 4.2* 281

LOOR screen showing six CRM Labor records
4 When you finish looking up your labor information, click on Master Block and Exit to exit.

### Labor Productivity Reports <a id="labor-productivity-reports"></a>

See the Standard Reports Guide.

OPERATIONS 2 GUIDE 4.2* 283

## Perfil de Workflow do Depositante (DIFP) <a id="perfil-de-workflow-do-depositante-difp"></a>

*Manual E — Operations 2*

Unit of Measure Set this field to 3.
Labor Standard Modifier 
Profile Code
The labor standard modifier profile code for this flow process. If you do not attach your labor standard modifier profile code to your flow process in FLPR, you must do so in DIFP.
Alert Time Optional
If you enter an alert time in HH:MM format, the Operational Board will flag the receipt or order as late when the number of hours and minutes that you specify has passed without the order or receipt having been advanced to the next flow in the workflow sequence.
Inbound Sequence Number
The order in which the flow process code is displayed on the Flows window of the Operational Board. If you set the inbound sequence number to zero, the flow will not appear on the Operational Board.
Operational Board Outbound Sequence NumberThe order in which the flow process code is displayed on the Flows window of the Operational Board. If you set the outbound sequence number to zero, the flow will not appear on the Operational Board.
FIELD DESCRIPTIONS

FLPR screen
2 Retrieve the flow process code that you wish to modify.
3 In the Labor Standard Profile Code field, key in the profile code that you set up in LSOA. If you do not define a labor standard profile in FLPR, you must do so in DIFP.
4 In the Unit of Measure field, key in 3 and press Enter.
5 In the Labor Standard Modifier Profile Code field, key in the profile code that you set up in LSMP. If you do not define a labor standard modifier profile in FLPR, you must do so in DIFP.
6 If required, key in an alert time in HH:MM format.
7 Key in the appropriate values for the Inbound and Outbound Sequence Number fields.
8 When you finish modifying your flow process code, click on Return to Main to exit create record mode.

OPERATIONS 2 GUIDE 4.2* 297

FLPR screen showing FIPI flow with an alert time of four hours
9 Click on Exit to exit.
ATTACHING LABOR STANDARDS AND LABOR STANDARD MODIFIERS TO 
WORKFLOW PROFILES IN DIFP
This step is only required if your labor standards and your labor standard modifiers differ by customer. For example, the labor standard for picking customer A’s product is 100 units per hour while the labor standard for picking customer B’s product is 200 units per hour. Customer-specific labor standards require multiple labor standard profile codes set up in LSOA.
If your labor standard and labor standard modifier apply to a range of flows (for example, STPI and ENPI), you must attach your LSOA profile to the second flow.
1 Enter DIFP.
2 Retrieve the workflow profile that you wish to set up.
3 Click on In/Out/Repi/Relo Block and select the appropriate option (Inbound or Outbound).
4 Click on Flow Block and select the flow that you wish to set up.
5 In the Labor Standard field, key in your labor standard profile code and press Enter or use the pick list function to select it.
6 In the Unit of measure field, key in your unit of measure and press Enter or use the pick list function to select it.
7 In the Labor Modifier field, key in your labor standard modifier code and press Enter or use the pick list function to select it.
8 If you wish to define an alert time for this workflow profile that differs from the default alert time defined in 
FLPR, key in your new alert time and press Enter. If you do not wish to override the default alert time, press Enter to bypass this field.

DIFP screen showing labor standard PIC1 attached to FIPI flow
9 When you finish modifying your workflow profile code, click on Return to Main to exit modify record mode.
10 Click on In/Out/Repi/Relo Block, Master Block and Exit to exit.

### APPLYING LABOR STANDARDS TO OPEN DOCUMENTS IN ULSO <a id="applying-labor-standards-to-open-documents-in-ulso"></a>

Labor standards defined in LSOA apply only to new orders and receipts that were created after the labor standard profile code was set up. If you wish to apply labor standards to existing orders and receipts, you must run ULSO (Update Labor Standard for Open Documents).
ULSO is typically run after an initial setup and whenever you modify your labor standards and wish to see the results applied to existing open orders and receipts. You can run ULSO for a single receipt or order or you can run the program for all open receipts and orders.
1 Enter ULSO.
2 In the Inbound/Outbound Flag field, key in I for Inbound or O for Outbound and press Enter.
3 Do one of the following:
If you wish to update a single receipt or order:
If you wish to update all receipts or orders:
a) Key in your receipt or order number and press Enter.
b) Click on Process One.
a) Click on Process All.

OPERATIONS 2 GUIDE 4.2* 299

ULSO screen showing status message for order 1567
4 Click on Exit to exit.

### ADJUSTING THE REPORT PROCESS FLAG IN IQBP <a id="adjusting-the-report-process-flag-in-iqbp"></a>

All quantities in the Operational Board are shown in the SKU type or types that are activated in IQBP (Item 
Quantity Breakdown Profile). A SKU type is activated in IQBP when its Report Process flag in the SKU Block is set to Y for Yes.
For example, if an item’s quantity breakdown is pallets/cases and there are 50 cases to a pallet, a quantity of 
75 cases will shown as follows:
 if both pallets and cases have their Report Process flag set to Y for Yes, the quantity will be shown as 1 pallet 25 cases
 if only cases have the Report Process flag set to Y for Yes, the quantity will be shown as 75 cases
1 Enter IQBP.
2 Retrieve the item quantity breakdown profile that you wish to adjust.
NOTE The Report Process flag in IQBP applies to native reports as well. Make sure that any changes to this flag are consistent with how you want to report your quantities in native reports.

IQBP screen showing Report Process flag set to Y for Yes at pallet level
3 Click on SKU Block.
4 Make sure that the Report Process flag is set to the appropriate value for each SKU type.
5 When you finish adjusting your Report Process flags, click on Return to Main, Master Block and Exit to exit.

### Resource Planning with the Operational Board <a id="resource-planning-with-the-operational-board"></a>

The Operational Board allows you to look up open orders and receipts to find out what percentage of the work has been completed and what percentage of the work remains to be done. You can restrict your query of open orders and receipts by company code, warehouse code, customer code, carrier code and many other search parameters.
When you perform your query, the Operational Board retrieves all open orders and receipts that meet your search criteria and displays the Summary window. This window shows the following:
 the total number of open orders and/or receipts
 the total number of lines on these open orders and/or receipts
 the percentage of work completed
 the number of hours and minutes it took to complete the work (if you have defined labor standards)
 the percentage of work remaining 
 the number of hours and minutes needed to complete this work (if you have defined labor standards)
If you click on the Flows tab, the Operational Board will break down the summary data by flow. For each inbound/outbound flow, the Operational Board will show:
 the total number of lines at that flow
 the percentage of work completed

OPERATIONS 2 GUIDE 4.2* 301
 the number of hours and minutes it took to complete the work (if you have defined labor standards)
 the percentage of work remaining 
 the number of hours and minutes needed to complete this work (if you have defined labor standards)

Flows window
 If you click on the Receipts/Orders tab, the Operational Board will break down the summary data by individual receipt/order. For each receipt/order, the Operational Board will show:
 the receipt or order number
 the receipt or order’s current flow and warehouse code
 the number of lines on the receipt or order and the percentage that this number of lines represents out of the total number of lines retrieved in your query
 the number of hours and minutes it took to complete the work (if you have defined labor standards)
 the percentage of work remaining 
 the number of hours and minutes needed to complete this work (if you have defined labor standards)
NOTE If you set the Inbound Sequence Number field in FLPR to zero for a given flow, that flow as well as the quantities on the receipts or orders at that flow will not appear in the Flows window. As a result, the totals for the Summary window will not match the totals for the Flows window because the Flows window will not included the quantities for the missing flow.

Receipts window

### ACCESSING THE OPERATIONAL BOARD <a id="accessing-the-operational-board"></a>

You access the Operational Board from ActiveDesktop.
1 On ActiveDesktop, click on .

### PERFORMING A QUERY USING THE GENERAL FILTER <a id="performing-a-query-using-the-general-filter"></a>

The General filter applies to both inbound receipts and outbound orders. You can restrict your Operational 
Board query by the following General filter criteria: company, warehouse, location type, customer, carrier and open or confirmed orders/receipts. 
If you have defined labor standards for the applicable flows and if you select “Labor Standard” in the Calculation field, the Operational Board will calculate the number of hours and minutes required to finish outstanding orders and/or receipts according to these labor standards.
FIELD DESCRIPTIONS
Inbound Inbound
Outbound
If you select Inbound, the Operational Board will retrieve receipts only. If you select Outbound, the Operational Board will retrieve orders only.
Company Code Mandatory
Your company code for the query.

OPERATIONS 2 GUIDE 4.2* 303
Warehouse Code Optional
If you enter a warehouse code, the Operational Board will restrict the query to order or receipt lines being processed in that warehouse. An order or receipt line is considered to be processed in a particular warehouse if the line has been restricted to that warehouse in ENOR/ENRE or if the line has been picked from or put-away into a location belonging to that warehouse.
If you leave this field blank, the Operational Board will retrieve all order and/or receipt lines regardless of warehouse.
Location Type If you enter a location type, the Operational Board will restrict the query to order or receipt lines that have been put-away to or picked from a location assigned that location type. If you leave this field blank, the Operational Board will retrieve all order or receipt lines regardless of the location type of the putaway or pick location.
Customer Code Optional
If you enter a customer code, the Operational Board will restrict the query to orders or receipts belonging to that customer. If you leave this field blank, the 
Operational Board will retrieve all orders or receipts regardless of customer.
Carrier Code Optional
If you enter a carrier code, the Operational Board will restrict the query to orders or receipts assigned to that carrier. If you leave this field blank, the 
Operational Board will retrieve all orders or receipts regardless of carrier.
Carrier Name Manual Optional
If you enter a manual carrier, the Operational Board will restrict the query to orders or receipts assigned to that manual carrier. If you leave this field blank, the Operational Board will retrieve all orders or receipts regardless of manual carrier.
FIELD DESCRIPTIONS

1 Select Inbound or Outbound from the Inbound dropdown list.
Open/Confirmed Open
Confirmed
Any
If you select Open, the Operational Board will retrieve open orders or receipts only. If you select Confirmed, the Operational Board will retrieve confirmed orders or receipts only. If you select Any, the Operational Board will retrieve both open and confirmed orders or receipts.
NOTE The Confirmed option is useful if you wish to look up historical data to determine how much work was completed in the past for a certain warehouse, customer, carrier, etc.
Calculation Labor Standard
Units
If you select Labor Standard, the Operational Board will calculate the number of hours and minutes required to finish outstanding work based on the applicable labor standard(s). If you select Units, the Flows window will show the percentage of each SKU class that has completed a given flow.
Number of Operators Only available if you have set up labor standards
If you enter the number of operators, the Operational Board will multiple that value by the number of hours to arrive at a total number of man hours. If the number of man hours is insufficient to perform the work represented by your query results, the Operational Board will highlight in red the remaining number of hours/minutes.
Number of Hours Only available if you have set up labor standards
If you enter the number of hours, the Operational Board will highlight the remaining number of hours/minutes in red when the value that you enter is insufficient to perform the work represented by your query results.
NOTE This field is mandatory if you enter a value in the Number of Operators field.
FIELD DESCRIPTIONS

OPERATIONS 2 GUIDE 4.2* 305
Dropdown list for Inbound and Outbound
2 Key in your company code or click on Company Code to display the company code pick list and then click on the appropriate code to select it.
3 Enter any other search parameters such as warehouse code, customer code and carrier code. You can key in your search parameters manually or you can click on the field label to display the pick list.
4 Select the appropriate value (Open, Confirmed or Any) from the Open/Confirmed dropdown list.

General filter
5 When you finish entering your search criteria, click on Query. The Operational Board will display the following:
 the Summary window showing the total number of open orders or receipts
 the total number of lines on these open orders or receipts
 the percentage of work completed
 the number of hours and minutes it took to complete the work (if you have defined labor standards)
 the percentage of work remaining
 the number of hours and minutes needed to complete this work (if you have defined labor standards.

Results window for outbound query
6 Do one of the following:

Flows window
7 If required, use the vertical scroll bar to scroll through the list of flows.
8 If you wish to look up completed vs. remaining data for individual receipts or orders, click on the 
Receipts/Orders tab.
If you wish to look up completed vs. remaining data broken down by flow process:
If you wish to look up completed vs. remaining data for individual receipts or orders:
a) Click on the Flows tab. a) Proceed to step 8.

OPERATIONS 2 GUIDE 4.2* 307
Orders window
9 If required, use the vertical scroll bar to scroll through the list of receipts/orders. If your query retrieves multiple pages, you can click on the “>” symbol to go to the next page or “>>” to go to the last page.
10 When you finish performing your query, click on the Summary tab to return to the Summary window.

### CLEARING A QUERY <a id="clearing-a-query"></a>

If you make a mistake when entering your search criteria, you can use the Clear command to clear all fields in the General filter.

### CHECKING AVAILABLE RESOURCES AGAINST OUTSTANDING WORK <a id="checking-available-resources-against-outstanding-work"></a>

You can check available resources against outstanding work to find out whether you have enough manpower in the warehouse to complete the current day’s orders and receipts. This option is only available if you have defined labor standards in LSOA and FLPR.
You check available resources against outstanding work by entering the appropriate values in the Number of 
Operators and Number of Hours fields in the General Filter. When you run your query, the Operational Board will compare the number of man hours that you specify to the amount of outstanding work. If the number of man hours is insufficient to complete the outstanding work based on the applicable labor standard(s), the 
HH:MM value in the Remaining column will be shown in red. 
1 Select Inbound or Outbound from the Inbound dropdown list.
2 Key in your company code or select your company code from the pick list.

3 Enter any other search parameters such as warehouse code, customer code and carrier code.
4 Select Open from the Open/Confirmed dropdown list.
5 Make sure that Calculation field is set to “Labor Standard”.
6 If required, key in a value for the Number of Operators field. 
7 Key in a value for the number of hours. If you specified a number of operators, the number of hours that you enter represents the number of hours for each operator. If you did not specify a number of operators, the number of hours represents the total number of hours regardless of operator.

General filter
8 When you finish entering your search criteria, click on Query. The Operational Board will display the 
Results window.

Results window showing Remaining HH:MM column in red
9 Check the HH:MM value in the Remaining column. If the value is red, the resources that you have specified are not sufficient to complete the outstanding work. 
10 Repeat the query as often as required with different values in the Number of Operators and Number of 
Hours fields.
11 When you finish checking available resources against outstanding work, click on the Summary tab to return to the Summary window.

### ENTERING RECEIPT- OR ORDER-SPECIFIC SEARCH CRITERIA IN A QUERY <a id="entering-receipt-or-order-specific-search-criteria-in-a-query"></a>

If you click on the Inbound or Outbound filter, you can enter search criteria that are specific to either receipts or orders. For example, you can specify a particular receipt number, flow code, shipper code or name, probill number, extra reference number, load type or date range on the Inbound filter. 
Likewise, you can specify a particular order number, flow process code, consignee code or name, PO number, extra reference number, load number, load type code or date range on the Outbound filter.

OPERATIONS 2 GUIDE 4.2* 309
1 Click on Inbound or Outbound to display the appropriate filter.

Inbound Filter
2 Proceed to enter your inbound or outbound search parameters.
3 If you wish to specify a date range for your query, select the appropriate date from the Date Type dropdown list. Then click on Date From to display the Pop-Up calendar.

Calendar window for Inbound filter
4 If required, select your from month and year from the two dropdown lists.
5 Click on the date that you wish to select.
6 If required, select the appropriate time in hours and minutes from the two dropdown lists.
7 When you finish entering your from date and time, click on Set. If you make a mistake, you can click on 
Clear and then re-enter your date and time.
8 If you enter a from date, repeat the above five steps for your to date.
9 When you finish entering your inbound or outbound search parameters, click on the Summary tab to return to the Summary window.

### PERFORMING A QUERY USING THE “UNITS” PARAMETER <a id="performing-a-query-using-the-units-parameter"></a>

If you set the Calculation field to “Units” rather than “Labor Standard”, the Flows window will show the percentage of each SKU class that is at a given flow.
Consider the following example of an inbound workflow profile consisting of five flows:
The Operational Board will perform the following calculation for the Inbound Staged flow: 4 divided by total number of pallets (20) = 20%. That is, 20 percent of the pallets in the query results are at the Inbound Staged flow.
1 Select Inbound or Outbound from the Inbound dropdown list.
2 Key in your company code or select your company code from the pick list.
3 Enter any other search parameters such as warehouse code, customer code and carrier code.
4 Select “Units” from the dropdown list and click on Query.
5 Click on the Flows tab.

Flows window showing percentage of each SKU class that has completed a given flow
6 If required, use the vertical scroll bar to scroll through the list of flows.
FLOW NUMBER OF PALLETS
Enter Receipt 1
Start Unload 5
Inbound Staged 4
Start Put-Away 5
Put-Away Complete 5

OPERATIONS 2 GUIDE 4.2* 311
7 When you finish performing your up your units-based query, click on the Summary tab to return to the 
Summary window.

### WORKING IN NORMAL MODE VS. FULL-SCREEN MODE <a id="working-in-normal-mode-vs-full-screen-mode"></a>

There are two modes in the Operational Board: normal mode and full-screen mode. Normal mode shows the General filter where you enter your search parameters as well as the Results window where your query results are displayed. Full-screen mode, on the other hand, shows only the Results window.

Normal mode vs. full-screen mode
 You switch from one mode to another by clicking on the appropriate button: for full-screen mode or for normal mode.

### LOOKING UP RECEIPT AND ORDER LINE DETAILS <a id="looking-up-receipt-and-order-line-details"></a>

You can look up receipt and order line details from the Receipts/Orders window. The line details show the flow process code and description, the document type (receipt or order), the document number, the number of order/receipt lines, the number of location lines (if available), the warehouse and location (if available) and the number of units.
If you place your mouse over the receipt or order line’s flow code, you can look up the time stamps and labor standards (if any) for each receipt/order line.
1 Make sure that you are on the Receipt/Orders window.
2 Do one of the following:
If you wish to look up a single receipt or order location line:
If you wish to look up multiple receipt or order location lines:
If you wish to look up all receipt or order location lines:
a) Click on the value in the Lines column.
a) Click on the check box beside each flow or order/receipt whose line details you wish to look up.
b) Click on the value in the Lines column of any selected record.
a) Click on the check box in the column heading.

Location Lines by Receipt window
3 If you wish to sort your location line records, you can sort them by flow process code, document number, warehouse code, location type and location code. Click on the appropriate column to sort the location line records in descending sequence. Click on the same column again to resort in ascending sequence.

Location line details window showing records sorted in descending flow process code sequence
4 If you wish to look up the time stamps and labor standards (if any) for each receipt/order line, place your mouse over the line’s flow code.

Workflow window showing labor standards for FIPI, but no labor standards for STPI, STLO or COOR
Labor standards

OPERATIONS 2 GUIDE 4.2* 313

Workflow window showing customer and item labor modifiers for the flow FIPI
5 When you finish looking up your time stamps and labor standards for each receipt/order line, move your mouse button to close the Workflow window.
6 When you finish looking up your receipt and order line details, click on the Summary tab to return to the 
Summary window.

### LOOKING UP A RECEIPT OR ORDER’S TIME STAMPS <a id="looking-up-a-receipt-or-order-s-time-stamps"></a>

You can look up a receipt or order’s time stamps by positioning your mouse over the individual receipt or order. The Operational Board will display each flow for the receipt or order. If the flow has been completed, the date and time of completion will be shown. If you have attached an alert time to a flow, the number of hours and minutes for the alert will be shown as well as the number of hours and minutes of lateness (if the receipt or order is flagged as “late”).
1 After performing your query, click on the Receipts/Orders tab to retrieve all receipts and/or orders in your query.
2 Place your mouse over the receipt or order number whose time stamps you wish to look up.
TIP You can deactivate the display of the Workflow Details window by clicking on the Show Workflow Details check box to deselect it.
Labor modifiers

Workflow window showing a order’s time stamps
3 When you finish looking up a receipt or order’s time stamps, move your mouse button to close the Workflow window.

### LOOKING UP YOUR QUERY CRITERIA <a id="looking-up-your-query-criteria"></a>

You can click on the Criteria tab to look up your search parameters for a particular query. The Operational 
Board will show your general search criteria as well as your inbound or outbound search criteria, if any.
1 Click on Criteria.

Query Criteria window

### LOOKING UP RECEIPT/ORDER ALERTS <a id="looking-up-receipt-order-alerts"></a>

The Alerts tab shows all receipts and/or orders flagged as late. A receipt or order is considered late when it has not advanced to the next flow within a given number of hours and minutes.
1 Click on the Alerts tab.

Alerts window showing late orders

OPERATIONS 2 GUIDE 4.2* 315
2 To see the receipt or order details, click on the Receipts or Orders tab.
3 When you finish looking up your receipt/order alerts, click on the Summary tab to return to the Summary window.

### PRINTING AND E-MAILING THE QUERY RESULTS <a id="printing-and-e-mailing-the-query-results"></a>

The Print command in the Operational Board generates printer-friendly output for the currently displayed query results. The following information is included in the output: the query criteria, the query summary, the breakdown by flow and the breakdown by receipt and/or order.
You can either print the printer-friendly output on an actual printer or you can e-mail it to any e-mail recipient.
1 Click on Printer Friendly.

Operational Board window showing printer friendly output
2 Do one of the following:
3 Click on the Close button (X) to close the Print Friendly window.
To print your output: To e-mail your output:
a) Select File > Print.
b) Proceed to print your output in the normal manner.
a) Select File > Send > Page by EMail.
b) Proceed to e-mail your output in the normal manner.

### SHOWING QUERY RESULTS IN CHART FORM <a id="showing-query-results-in-chart-form"></a>

You can generate pie and bar charts from the Summary and Flows windows showing Operational Board data in graphical format. The chart capability of the Operational Board requires Adobe’s SVG Viewer.
1 Make sure that you are in either the Summary or Flows window.
2 Click on Chart.
3 Do one of the following:
4 If prompted to accept the software license agreement for Adobe SVG Viewer, click Accept.

Interactive Chart window showing percentage of completed lines for each inbound flow
5 Place your mouse over the section of the pie chart that you wish to look up and the Operational Board will display a description and percentage for the selected section.
6 To see the same query results in bar chart format, click on Bar Chart.
If a pie chart is displayed on your screen:
If your screen remains blank because the SVG Viewer is not installed:
a) Proceed to next step. a) Click on Download Adobe SVG 
Viewer.
b) When the File Download window appears, click on Save (Windows 2000) or Run (Windows XP).
c) If prompted to run the software, click on Run.
d) Click on Summary.

OPERATIONS 2 GUIDE 4.2* 317
7 When you finish looking up your data in chart form, click on the Summary tab to return to the Summary window.

OPERATIONS 2 GUIDE 4.2* 319
