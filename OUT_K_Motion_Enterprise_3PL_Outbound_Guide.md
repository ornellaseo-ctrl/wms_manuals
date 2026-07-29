# Manual OUT — K.Motion Outbound Guide (Guia de Expedição v6.1)

> **ID do Manual:** OUT  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Guia de expedição K.Motion v6.1: processos outbound, picking, shipping, load management. Versão mais recente complementando o Operations 1.

---

K.Motion Enterprise 
3PL Outbound
User Guide
Version 6.1-e 
---

Körber Supply Chain
5600 W 83rd Street, Suite 600, Minneapolis, Minnesota 55437
T +1.800.328.3271
koerber-supplychain.com
support.sc.msp@koerber-supplychain.com
© Copyright 2022 Körber Supply Chain U.S., Inc. (a successor in interest to HighJump Software Inc.) All Rights 
Reserved. Reproduction and distribution under license only. 
This document and the software it describes are confidential and proprietary information of Körber Supply Chain U.S., 
Inc. and its affiliated entities and are copyrighted properties of Körber Supply Chain U.S., Inc. with all rights reserved. 
Information contained herein is subject to change at any time in Körber Supply Chain U.S., Inc.’s sole discretion. 
Neither this information nor the software may be copied in whole or in part without the prior written consent of Körber 
Supply Chain U.S., Inc. 
This documentation and the related software programs are “commercial computer software” and “commercial 
computer software documentation” pursuant to DFAR Section 227.7202 and FAR Section 12.212 (and any successor 
sections). Use of this documentation or the related software programs, including reproduction and display of them, by 
the United States of America and/or any of its instrumentalities, regardless of form, (collectively, the “Government”), 
is allowed only as governed by terms of a valid license agreement with Körber Supply Chain U.S., Inc. or one of its 
affiliated companies. Under no circumstances shall Körber Supply Chain U.S., Inc. be obligated to comply with any 
Government requirements regarding cost or pricing data or cost accounting requirements. If any Government 
requirement might apply, you must notify Körber Supply Chain U.S., Inc. of the Government requirement and obtain a 
waiver or exemption for the benefit of Körber Supply Chain U.S., Inc. before you may use this documentation or the 
related software programs.
Körber is a trademark of Körber AG, Anckelmannsplatz 1, 20537 Hamburg, Germany. All trademarks used are the 
property of their respective owners.-e 
---

K.Motion Enterprise 3PL Outbound Guide i 
Table of Contents
Introduction.............................................................................................................................. 1
Overview................................................................................................................................................... 1
Accessing the Outbound Menu Options ................................................................................................... 1
Working with Waves ................................................................................................................ 3
Overview................................................................................................................................................... 3
Working with Wave Management............................................................................................................. 4
Working with Wave Template Management............................................................................................. 4
Creating a Template ............................................................................................................................. 5
Modifying a Template ........................................................................................................................... 8
Deleting a Template ............................................................................................................................. 9
Working with Wave Template Schedules ...............................................................................................10
Creating a Scheduled Wave Template...............................................................................................10
Modifying a Scheduled Template .......................................................................................................11
Deleting a Scheduled Template .........................................................................................................13
Working with Wave Transactions ...........................................................................................................14
Working with Look Up Order(s) ............................................................................................ 15
Searching for an Order ...........................................................................................................................16
Searching for an Order Using the Search Panel................................................................................16
Searching with Search Mode..............................................................................................................17
Creating an Order...................................................................................................................................18
Working with Editing an Order................................................................................................................21
Working with Deleting an Order..............................................................................................................22
Printing an Order ....................................................................................................................................22
Printing an Order by Document Code ................................................................................................23
Printing an Order ................................................................................................................................24
Requeuing an Order...........................................................................................................................25
Using Flow Process ................................................................................................................................25
Using Advancing Flow Process for an Order .....................................................................................25
Reversing Flow Process for an Order ................................................................................................27
Adding Extra Charges.............................................................................................................................28
Adding Extra Header Charge .............................................................................................................28
Adding Extra Line Charge ..................................................................................................................30
Working with Draft Order Entry............................................................................................. 33
Entering an Order Header ......................................................................................................................33
Editing a Draft Order...............................................................................................................................35
Deleting a Draft Order.............................................................................................................................37
Committing a Draft Order........................................................................................................................38
Working with Load Management .......................................................................................... 40
Creating a Load ......................................................................................................................................41
Editing a Load.........................................................................................................................................43-e 
---

ii K.Motion Enterprise 3PL Outbound Guide
Using Load Status ..................................................................................................................................44
Using Advance Status for a Load.......................................................................................................44
Reversing a Load Status ....................................................................................................................45
Suspending, Releasing, and Deleting Loads..........................................................................................45
Suspending a Load.............................................................................................................................45
Unsuspending a Load.........................................................................................................................46
Deleting a Load ..................................................................................................................................47
Working with Relocate to Pick Line...................................................................................... 48
Overview.................................................................................................................................................48
Processing an Order Replenishment......................................................................................................49
Deleting an Order Replenishment ..........................................................................................................50
Working with RF Operator Task Assignment....................................................................... 51
Overview.................................................................................................................................................51
Search for Orders or Tasks ....................................................................................................................52
Assign to Orders .....................................................................................................................................52
Assign a Task to an Operator.............................................................................................................54
Place Tasks in Sequential Order........................................................................................................55
Suspend a Task..................................................................................................................................56
Override a Task Priority......................................................................................................................58-e 
---

K.Motion Enterprise 3PL Outbound Guide 1 
Introduction
Overview
You can use the K.Motion Enterprise 3PL Outbound page to view and manage the outbound shipping 
process in the warehouse. The Outbound page is the control center for managing shipping tasks and 
processing orders. 
The Outbound page allows you to do the following: 
• Work with waves 
• Work with orders 
• Work with draft order entries 
• Work with load management 
• Relocate to pick line 
• Work with RF operator task priorities 
Accessing the Outbound Menu Options 
You can use the Outbound menu to manage and configure waves, draft order entries and loads. 
To access the Outbound menu, complete the following steps: 
Log into Körber One. 
Select Menu > K.Motion Enterprise 3PL > Outbound. -e 
---

2 K.Motion Enterprise 3PL Outbound Guide
Option Description
Configuration Accesses the following application 
components for set up:
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
Wave Manager Accesses the following application 
components to manage waves:
• Wave Management 
• Wave Template Management 
• Wave Template Schedule 
• Wave Transactions
Look Up Order(s) Allows you to view, search, and create new 
orders. 
Draft Order Entry Allows you to create, view, and finalize a
drafted order. 
Load Management Allows you to create and manage a load. 
Relocate to Pick Line Allows you to confirm that a replenish is 
completed and adjust the replenish.
RF Operator Task Assignment Allows you to assign and view outbound 
related tasks. -e 
---

K.Motion Enterprise 3PL Outbound Guide 3 
Working with Waves 
Overview 
The Wave Manager page allow you to view and manage waves. When working in the Wave Manager 
page, you can perform the following tasks: 
• Working with Wave Management 
• Working with Wave Template Management 
• Working with Wave Template Schedules
• Working with Wave Transactions
To access the Wave Manager page, select Outbound > Wave Manager. -e 
---

4 K.Motion Enterprise 3PL Outbound Guide
Working with Wave Management
The Wave Management page allows you to view and manage waves. 
To view a wave, complete the following steps:
 Select Outbound > Wave Manager > Wave Management. 
Select the wave you want to view. 
Working with Wave Template Management
When working with the Wave Template Management page, you can perform the following tasks: 
• Creating a Template
• Modifying a Template
• Deleting a Template-e 
---

K.Motion Enterprise 3PL Outbound Guide 5 
Creating a Template
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
Modifying a Template
You can modify a template using the Wave Template Schedules page. 
Note
When you modify a template, the system overrides the previous version.
When you process a wave using the Run Wave command, K.Motion Enterprise 3PL will 
allocate any unallocated orders in the wave and print the required number of carrier labels.
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
Deleting a Template
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
Working with Wave Template Schedules
You can schedule a template to run automatically at a given time. You must specify a start date for a 
scheduled template. The end date field for a scheduled template is optional.
When working with the Wave Template Schedule page, you can perform the following tasks:
• Creating a Scheduled Template
• Modifying a Scheduled Template 
• Deleting a Scheduled Template
Creating a Scheduled Wave Template
To schedule a wave template, complete the following steps:
Select Outbound > Wave Manger > Wave Template Schedules. 
The Wave Template Schedules page displays. 
Select a template. 
Click Create New Schedule. 
Use the table below to set up values. 
Frequency Minutes Hour Day Month Day of the Week
The 20th minute of each
hour
20 Default Default Default Default
The 45th minute of each
hour on Wednesdays
45 Default Default Default Wednesday
9 A.M. every day Default 9 A.M. Default Default Default
9 A.M. every Monday Default 9 A.M. Default Default Monday
9 A.M. first of the month Default 9 A.M. 1 Default Default-e 
---

K.Motion Enterprise 3PL Outbound Guide 11
Click Save. 
Modifying a Scheduled Template
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
Deleting a Scheduled Template
You can delete a scheduled template from the Wave Management page.
To delete a scheduled template, complete the following steps: 
Select Outbound > Wave Manager > Wave Template Schedules. 
Select the wave template you want to delete. 
Click Delete. 
A confirmation message displays. 
Click Delete. -e 
---

14 K.Motion Enterprise 3PL Outbound Guide
Working with Wave Transactions
You can look for the completion status of a wave by using the Wave Transaction page. 
To view wave transactions, complete the following step, select Outbound > Wave Manager > Wave 
Transactions.
The Wave Transactions page displays. -e 
---

K.Motion Enterprise 3PL Outbound Guide 15
Working with Look Up Order(s) 
Overview 
The Look Up Order(s) page allows you to view all orders that have been entered into K.Motion 
Enterprise 3PL, in any status. When working with the Look Up Order(s) page, you can perform the 
following tasks:
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
Searching for an Order
You can search for orders using various methods in the Look Up Order(s) page. 
Searching for an Order Using the Search Panel
You can search for orders or by using the Search panel and entering specific search criteria. 
To search for an order using the search panel, complete the following steps:
Select Outbound > Look Up Order(s). 
Click Search on the Action Bar. 
Search for a task or order by entering any of the following search criteria in the Search fields. 
Click the Search icon. -e 
---

K.Motion Enterprise 3PL Outbound Guide 17
Searching with Search Mode
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
Creating an Order
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
Working with Editing an Order
The Edit Order command allows you to add and delete order lines and change most of the fields in
the order header. However, you cannot change either the order type or the order line type.
To edit an order, complete the following steps:
 Select Outbound > Look Up Order(s). 
The Look Up Order(s) page displays. 
Select the order you want to edit.
Click Orders > Edit from the Action bar. 
Make the necessary changes to the order.
Click Save. -e 
---

22 K.Motion Enterprise 3PL Outbound Guide
Working with Deleting an Order 
You can delete an order using the Look Up Order(s) page. 
To delete an order, complete the following steps. 
 Select Outbound > Look Up Order(s). 
The Look Up Order(s) page displays.
Select the order you want to delete.
Select Orders > Delete. 
Click Delete. 
Printing an Order 
You can print an order from the Look Up Order(s) page at any time. You can print an order as follows:
• Printing an Order by Document Code 
• Printing an Order 
• Requeuing an Order-e 
---

K.Motion Enterprise 3PL Outbound Guide 23
Printing an Order by Document Code
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
Printing an Order 
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
Requeuing an Order
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
Using Flow Process 
Flow process is the defined sequence of steps that an order must follow, for receiving orders and for 
shipping. 
Note
You can only advance to the next flow and reverse to the previous flow. You cannot advance 
or revers more than one flow at a time. 
Using Advancing Flow Process for an Order 
You can use the advanced flow process if you want to manually advance the flow of an order, if it has 
not been confirmed. 
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
Reversing Flow Process for an Order 
You can change or edit an order after it has advanced in the flow process by reversing the flow 
process.
To use the reverse flow process, complete the following steps:
Select Outbound > Lok Up Order(s). 
Select the order you want to reverse.
Click Flow Process on the Action bar.
Select Reverse Flow Process. 
Select the order you want to reverse. 
Click Process Flow to reverse the order in the flow. -e 
---

28 K.Motion Enterprise 3PL Outbound Guide
Adding Extra Charges 
You can add extra charges confirmed orders and accessorial charges to open orders in the Look Up 
Order(s) page. 
Note
Extra charges can only be cancelled when an order is open, if they have been automatically 
applied. 
Adding Extra Header Charge 
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
Adding Extra Line Charge 
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
Working with Draft Order Entry
A draft order is a newly-created order that has not yet been verified or committed. 
Note
Draft orders are optional. You can create a committed order in Look Up Orders.
When working with the Draft Order Entry page, you can perform the following tasks: 
• Entering an Order Header
• Editing a Draft Order
• Deleting a Draft Order
• Committing a Draft Order
Entering an Order Header 
The order header contains general information that applies to the entire order such as the customer 
code, the consignee, the carrier and the load type. 
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
Editing a Draft Order
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
Deleting a Draft Order
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
Committing a Draft Order
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
Working with Load Management
When creating a load, you can define the door, the building, the warehouse attributes, the orders on 
the load and the stop sequence. 
You can also enter carrier and consignee information in the Load Manager when you are working with 
multi-leg trips in which the freight is transported first to a freight pool point or distribution center. The 
carriers and consignees attached to the orders are used to deliver the freight to its final destination.
When working with the Load Management page, you can perform the following tasks: 
• Creating a Load 
• Editing a Load 
• Using Load Status 
• Suspending, Releasing and Deleting Loads 
To access the Load Management page, select Outbound > Load Management. -e 
---

K.Motion Enterprise 3PL Outbound Guide 41
Creating a Load 
To create a load, complete the following steps: 
Note
The following fields are auto populated but can be changed: Building, Warehouse Attribute, 
and External Reference Code. 
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
Using Load Status
You can advance and reverse a load status on the Load Management page. 
Using Advance Status for a Load
You can manually advance the flow of a load. 
To use the advance flow process, complete the following steps:
Select Outbound > Load Management. 
Select the order you want to work with.
Click Advance Status on the Action bar. -e 
---

K.Motion Enterprise 3PL Outbound Guide 45
Reversing a Load Status 
You can edit a load status in the reverse load status. 
To use the revere load status, complete the following steps: 
Select Outbound > Load Management. 
The Advanced Load Status message displays. 
Select the load you want to reverse. 
Click Reverse Status. 
Suspending, Releasing, and Deleting Loads
You can suspend, release and delete loads from the Load Management page. 
Suspending a Load
You can suspend a load if it has a status of Ready to Load or Loading. 
To suspend a load, complete the following steps:
Select Outbound > Load Management. -e 
---

46 K.Motion Enterprise 3PL Outbound Guide
Select the order that you want to suspend. 
Click Suspend. 
A notification displays confirming the load was suspended. 
Unsuspending a Load
You can unsuspend a load that has previously been suspended. 
To unsuspend a load, complete the following steps:
Select Outbound > Load Management. 
Select the order you want to unsuspend. 
Click UnSuspend. 
A notification will display that the load has been successfully unsuspended. -e 
---

K.Motion Enterprise 3PL Outbound Guide 47
Deleting a Load 
You can delete a load at any time using the Load Management page.
To delete a load, complete the following steps: 
Select Outbound > Load Management. 
Select the order you want to delete. 
Click Delete. 
Click Yes to confirm you want to delete the order. -e 
---

48 K.Motion Enterprise 3PL Outbound Guide
Working with Relocate to Pick Line
Overview 
You can view open replenishments from the Relocate to Pick Line page at any time. When working 
with the Relocate to Pick Line page, you can perform the following tasks: 
• Processing an Order Replenishment 
• Deleting an Order Replenishment 
To access the Relocate to Pick Line page, select Outbound > Relocate to Pick Line. -e 
---

K.Motion Enterprise 3PL Outbound Guide 49
Processing an Order Replenishment 
You can manually process a replenishment order by using the Relocate to Pick Line page. 
To process a replenishment order, complete the following steps:
Select Outbound > Relocate to Pick Line. 
The Relocate to Pick Line page displays. 
Select the order you would like to process. 
Select Process on the Action bar. 
A notification appears confirming the order has been processed successfully.-e 
---

50 K.Motion Enterprise 3PL Outbound Guide
Deleting an Order Replenishment 
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
Overview 
The RF Operator Task Assignment allows the user to assign specific tasks, operators and define a 
picking sequence. When working with the RF Operator Task Assignment page, you can perform the 
following tasks:
• Search for Orders or Tasks
• Assign to Orders
To access the RF Operator Task Assignment page, select Outbound > RF Operator Task 
Assignment. -e 
---

52 K.Motion Enterprise 3PL Outbound Guide
Search for Orders or Tasks 
You can search for orders or tasks by using the Search panel and entering specific search criteria. 
To search for an order or task, complete the following steps: 
Select Outbound > RF Operator Task Assignment. 
The Search panel displays when the page opens. 
Search for a task or order by entering any of the search criteria. 
Click the Search. 
Assign to Orders
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
Assign a Task to an Operator 
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
Place Tasks in Sequential Order 
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
Suspend a Task
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


