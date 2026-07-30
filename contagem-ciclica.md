---
title: "Contagem Cíclica (Cycle Counting)"
description: "Perfis, geração e impressão de tickets, entrada de contagem, reconciliação e relatórios."
layout: default
---

# Contagem Cíclica (Cycle Counting)

Perfis, geração e impressão de tickets, entrada de contagem, reconciliação e relatórios.

**Fluxo principal:** `CYCP -> CYEN -> CYGT -> CYTI -> entrada -> CYCO -> CYUP`

> Fonte: manuais B do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Introduction And Overview <a id="introduction-and-overview"></a>

*Manual B — Cycle Counting*

# Manual B — Cycle Counting Guide (Contagem Cíclica)
> **ID do Manual:** B  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Contagem cíclica completa: setup de perfis (CYCP), criação de contagens (CYEN), geração de tickets (CYGT), impressão (CYTI), entrada de contagens (blind/non-blind), reconciliação, fechamento (CYCO), relatórios (CYBK/CYSR/CYTR/CYPC/CYCR/CYCD). Suporta contagens programadas, arbitrárias e event-driven.
---

### Overview of Cycle Counting <a id="overview-of-cycle-counting"></a>

AccellosOne 3PL’s cycle count system allows you to perform regularly scheduled counts of randomly selected inventory in your warehouse without the time and expense of a full physical inventory. You can perform both item and location counts, you can define the number of times that you wish to count a particular item or location as well as the frequency (for example, daily, weekly, monthly, every second Tuesday, etc.) 
and you can specify the variance that you wish to allow before forcing a recount. 
AccellosOne 3PL supports different cycle count parameters for different items. For example, you can count high value items on a daily basis while counting low value items on a weekly or monthly basis. You can perform both blind and non-blind counts and switch from one system to another as often as required.

### Blind vs. Non-Blind Counts <a id="blind-vs-non-blind-counts"></a>

There are two types of cycle counts in AccellosOne 3PL:
 blind counts
 non-blind counts
Blind counts generate tickets showing the ticket number, location code and customer code, but no item code or inventory level information. If you use preprinted tickets for your cycle count, you must perform a blind count. You cannot perform a non-blind count using preprinted tickets. 
NOTE No automatic adjustment to inventory takes place in cycle counting based on an item or location count. If you want to make adjustments to inventory after performing a cycle count, you must do so manually in CYUP (Cycle Count Update Inventory).

Non-blind counts generate tickets showing the ticket number, customer code and location code. As well, the item code and inventory levels will be shown depending on the options that you select when setting up your cycle count.
Both blind and non-blind counts generate one ticket for each physical inventory unit in each location (that is, multiple tickets for the same location if you have mixed product in that location). 
A physical inventory unit in AccellosOne 3PL is defined as all product belonging to the same customer, placed in the same warehouse and location with the same level 1, level 2, level 3, level 4 values and the same hold code. For example, if you placed two pallets of identical product in the same location and then placed one pallet on hold and left the other pallet with no hold, you would have two physical inventory units on your system for that location:
1) item 1/lot A/warehouse 1/location 101 + hold X
2) item 1/lot A/warehouse 1/location 101

### Blank vs. Non-Blank Tickets <a id="blank-vs-non-blank-tickets"></a>

There are two types of tickets in AccellosOne 3PL:
 non-blank tickets (the default)
 blank tickets
Regular or non-blank tickets show the ticket number, customer code, location and warehouse plus hold code, if any. Depending on which Show flags you set to Yes, the item code and inventory levels will also be printed. Blank tickets, on the other hand, show the ticket number only; no location is printed on the ticket. 
Blank tickets are extra tickets that you use to count inventory found in the wrong location or in an unexpected location.
Ticket Location Warehouse | 
Quantity
----------------------------------
|--------- 
1 A100 1 |
----------------------------------
| 
CUST1 Customer 1 | 
 | 
 | 
 | 
Ticket Location Warehouse | 
Quantity
----------------------------------|--
1 A100 1 |
----------------------------------| 
CUST1 Customer 1 | 
 | 
ITEM-1 Item 1 | 
 | 
101 | 
Ticket for blind count Ticket for non-blind count showing item and lot number

### System Flow Chart for Cycle Counting <a id="system-flow-chart-for-cycle-counting"></a>

There are up to eight steps to follow in performing a cycle count:

CYCP
ITEM LOCA
CYEN
CYGT
CYTI
CYET
RFCY
CYBK (recommended)
CYCO
You set up your cycle count profile in CYCP (Cycle Count 
Profile).
You attach your profile to either the item in ITEM or the location in LOCA.
You create your cycle count in 
CYEN (Create Cycle Count).
You generate your tickets in 
CYGT (Cycle Count Generate 
Tickets).
If you use RF, you enter your cycle counts by means of an 
RF device. If you do not use 
RF, you print your tickets in 
CYTI (Print Cycle Count 
Tickets) and then you enter your counts in CYET (Enter 
Cycle Count Tickets). 
If you performed a dual count, you reconcile your A and B counts in CYAB (Cycle Count 
Ticket Discrepancy).
It is recommended that you run your book report in CYBK (Cycle Count Book Report).
You close your cycle count in 
CYCO (Close Cycle Count).
CYAB

### Understanding Variances <a id="understanding-variances"></a>

AccellosOne 3PL allows you to define variances for each cycle count profile that you set up. A variance is the percentage difference between the book value and the cycle count value. If the variance exceeds the percentage that you allow, the system will prompt you to recount the item until the variance falls within the range that you defined.
The following diagram shows how variances work for an item counted twice a year. 
ITEM A
On-hand = 100 CS
Book = 100 CS
Status = No variance
Number of counts performed = 1
ITEM B
No scheduled count for item B
JANUARY 1 APRIL 1 JULY 1 OCTOBER 1
Cycle count period = I year
Type = item
Number of times you count each item = 2 times a year
Variance allowed = 90% (that is, if the difference between the book and cycle count values exceeds 10%, flag the item as being out of balance)
Number of items counted each time = 1
No scheduled count for item A
On-hand = 100 CS
Book = 150 CS
Status = Difference exceeds variance and therefore count not advanced
Number of counts performed = 0
On-hand = 80 CS
Book = 82 CS
Status = Difference within variance
Number of counts performed = 2
On-hand = 140 CS
Book = 150 CS
Status = Difference within variance
Number of counts performed = 1
No scheduled count for item A
On-hand = 145 CS
Book = 155 CS
Status = Difference within variance
Number of counts performed = 2
In this example, item A is counted twice and is within the variance each time. Item B, on the other hand, exceeds the variance on its first count and therefore you decide to include it in the next scheduled count.
When it is recounted, the difference between the book and cycle count quantities falls within the variance and the number of counts is advanced to 1.
Because item B was out of balance in the
April 1 count, you decide to recount it in the scheduled count for July 1

### AccellosOne 3PL Documentation Set <a id="accellosone-3pl-documentation-set"></a>

The AccellosOne 3PL documentation set includes 12 volumes:
Allocation and Wave 
Manager Guide allocation setup, inbound and outbound allocation, pick lines and replenishment, reserve logic and Wave Manager
Billing and Invoicing 
Guide billing setup, cash posting system, maximum and minimum charges, renewal storage, extra charges, invoicing, accessorial bill later and bill immediate charges, rollup invoicing and billing/invoicing reports
Core Documents 
Guide core documents, maintain programs for core documents, document overlays, customizing the accessorial invoice, Oracle Reports, BarTender Label Printing
Cycle Counting Guide setup and operational programs for cycle counting as well as the cycle counting reports
Guide to ActiveDesktop/A13PLlogging on to and off from ActiveDesktop, the alerts system, e-Filing, selecting your company, working with menus and programs, basic queries, Signature Capture
Standard Reports 
Guide core reports in AccellosOne 3PL
Operations 1 Guide receiving and confirming product, printing receiving documents, shipping R-type and 
P-type orders, printing order documents, entering inventory adjustments, relocating product, entering hold adjustments
Operations 2 Guide appointment planner, back orders, batch picking, manual packing, customer relationship management, EDI, faxing and auto-printing, item substitution, kitting, labor tracking, Operational Board, pallet control, inventory attributes, item process values, outbound load building, quick response labels
Physical Inventory 
Guide setup and operational programs for physical inventory as well as the physical inventory reports
RF Guide setup programs for RF (Radio Frequency), RF receiving, RF picking, entering process values in RF, voice-activated picking, order assignment system, equipment tracking, interleaving, cartonization, outbound pallet building
Setup Guide mandatory setup programs including warehouses and locations, isolators, inventory level profiles, customers, charge codes, item profiles, items, carriers, shippers, consignees
System Administration Guideoperator and menu setup, company and program access, operator restrictions, purging and archiving, conversions, special verify programs, translation manager

## Cycle Count Setup <a id="cycle-count-setup"></a>

*Manual B — Cycle Counting*

### Setting Up Your Cycle Count Profile <a id="setting-up-your-cycle-count-profile"></a>

You set up your cycle count profile(s) in CYCP (Cycle Count Profile). The main parameters that you define in this program are:
 the cycle count period 
 the cycle count type (item or location)
 the number of items or locations to be counted each cycle count
 the number of times during the cycle count period that you wish to count each item or location
 whether or not you wish to cycle count on weekends and holidays
 the variance that you wish to allow before a recount is forced
 how often you want perform cycle counting (daily, weekly, monthly, on a series of irregular dates, etc.)
You can set up as many different cycle count profiles as you need. For example, you can create one profile for high value items and set the frequency of counts to daily and create a second profile for low value items and set the frequency of counts to every two weeks.
The profile that you create in CYCP can be attached to either items in ITEM or locations in LOCA.
FIELD DESCRIPTIONS
Cycle Count Profile Code Mandatory
Your cycle count profile.
Description Mandatory
Your cycle count profile description.
Current Period Start/End 
Date
Mandatory
In these two fields, you define your cycle count period. Your cycle count period should correspond to your period of analysis — usually one year, every six months or every quarter. At the end of the cycle count period, the profile will be deactivated unless you specify the next cycle count period in the Next Period 
Start Date and Next Period End Date fields.
When a profile is deactivated, you cannot use it to perform scheduled cycle counts. Arbitrary or unscheduled cycle counts, however, can still be performed.

If required, you can backdate your cycle count period; for example, your period of analysis is January 01 to December 31 and you perform your first count using AccellosOne 3PL on March 1. See [Entering Cycle Counts Retroactively](contagem-ciclica.html#entering-cycle-counts-retroactively) for further information for further information.
Next Period Start/End 
Date
Optional
In these two fields, you define the next cycle count period. The Next Period 
Start Date field is automatically set to the Current Period End Date value plus one day. The Next Period End Date field is optional and can be set to any future date.
Cycle Count Type I = Item
L = Location
E = Event-Driven
Select I if you wish to count items, select L if you wish to count locations or select E if you wish to generate an event-driven cycle count. 
Number of Item/ Locations to be CountedMandatory
The number of items or locations that you wish to count each time you perform a cycle count.
For example, if you have 50 items attached to this cycle count profile and you want to count only 10 of these 50 each day, enter 10 in this field. 
Number of Times per 
Item/Location
Mandatory
The number of times during the cycle count period that you wish to count each item or location. For example, if you have 100 locations attached to a cycle count profile and you want to count each location three times during the entire cycle count period, enter 3 in this field.
Count on Day A = Any day
W = Skip weekends
H = Skip holidays
S = Skip weekends and holidays
The days on which you wish to perform your cycle count. If you select an option that skips holidays (that is, either H or S), you must set up and maintain your holidays in HOLI (Holidays).
FIELD DESCRIPTIONS

Variance Allowed Mandatory
The percentage variance allowed between the book value and the cycle count value. For example, if a 5% variance is allowed, enter 95 in this field; if no variance is allowed, enter 100.
A variance of 95 means that 5% is the threshold point. If an item or location is below the threshold — say 2% — it is deemed to be in balance and is not flagged. If, however, the item or location is over the threshold — say 10% — it is flagged as having a variance. When an item or location is flagged as having a variance, you can elect to include it in the following count and perform a recount or you can ignore the variance.
Variance based on Quantity/ValueQ = Quantity
V = Value (for item counts only)
If you want to record variances based on quantity, enter Q. If you want to record variances based on value, enter V. 
If you use the quantity option, variances are based on the on-hand quantity shown in LOEN. If you use the Value option, you must enter the item’s value in the Item Value and Value for SKU Code fields in ITEM.
Date Profile Code (defined in DAPR)
Mandatory if you do not specify a frequency
The dates on which you wish to conduct a cycle count. If you have regular schedule for cycle counts (for example, daily, weekly, monthly, etc.), use the 
Frequency Code and Frequency Value fields to specify the frequency. If your cycle count schedule is irregular (for example, the 17th of each month or the third week of each month), you must set up a date profile code in DAPR.
Refer to the Setup Guide for further instructions on setting up DAPR.
FIELD DESCRIPTIONS

### SAMPLE SETUPS <a id="sample-setups"></a>

Cycle Counting by Location
Number of locations attached to profile = 300
Cycle count period = 3 months
Frequency = Daily excluding weekends
Number of items/locations to be counted each time = 50
Number of times per item/location = 10
In this example, you are going to cycle count by location. You will conduct cycle counts daily excluding weekends and each time you count you will count 50 locations. Each location will be counted a total of 10 times every three months (the cycle count period).
Frequency Code Mandatory if you do not specify a date profile code
D = Daily
FRI = Friday
M = Monthly
MON = Monday
SAT = Saturday
SUN = Sunday
THUR = Thursday
TUES = Tuesday
WED = Wednesday
WEEK = Weekly
The frequency of your cycle count — for example, daily, weekly, monthly, every second Thursday, etc. 
Frequency Value Mandatory if you specify a Frequency Code
The number of units of time defined in the Frequency Code field that must pass before a new cycle count is required. 
Frequency Code
D for Daily
M for Monthly
TUES
Frequency Value
Result
Daily
Every 2 months
Every fourth Tuesday
Next Cycle Count Date Only updated for scheduled cycle counts
Calculated by the system.
FIELD DESCRIPTIONS

Cycle Counting by Item
Number of items attached to profile = 60
Cycle count period = 1 year
Frequency = Wed
Number of items/locations to be counted each time = 10
Number of times per item/location = 8
In this example, you are going to cycle count by item. You will conduct cycle counts every Wednesday and each time you count you will count 10 items. Each item will be counted a total of 8 times a year (the cycle count period).

### PROCEDURE <a id="procedure"></a>

1 Enter CYCP.

Cycle Count Profile (CYCP) screen
2 Click on Create Record.
3 Key in your cycle count profile code and press Enter.
4 Key in your cycle count description and press Enter.
5 In the Current Period Start Date field, key in your start date for this cycle count period and press Enter.
6 In the Current Period End Date field, key in your end date for this cycle count period and press Enter.
7 If required key in your end date for the Next Period End Date and press Enter or press Enter without entering an end date to bypass the function.
8 Key in your cycle count type (I for Item or L for Location) and press Enter.

Cycle Count Profile screen showing a cycle count period of one year
9 In the Number of Items/Locations to be Counted field, key in the number of items or locations that you wish to count each time and press Enter.
10 In the Number of times per Item/Location field, key in the number of times during the cycle count period that you wish to count each item or location and press Enter.
11 In the Count on Day field, key in the appropriate value (A for Any day, W for Skip weekends, H for Skip holidays or S for Skip weekends and holidays) and press Enter.
12 In the Variance allowed field, key in your variance and press Enter. For example, if you want to allow a variance of 5 percent, you would key in the number 95.

13 In the Variance based on Quantity/Value field, key in the appropriate value (Q for Quantity or V for Value) 
and press Enter.
14 Click on Return to Main to exit Create Mode. The system will display the date of your first cycle count in the Next Cycle Count Date field.
Cycle Count Profile screen showing a monthly cycle count profile
15 When your profile code is set up, click on Exit the required number of times to exit. 
If you are using date profile codes to specify the dates on which you wish to perform a cycle count:
If you are using frequency codes and values to specify the dates on which you wish to perform a cycle count:
a) In the Date Profile Code field, key in your date profile code and press Enter.
a) Press Enter to bypass the Date 
Profile Code field.
b) In the Frequency Code field, use your pick list (F10 to enter the pick list, F2 to perform your query and F3 to select your code) to select the appropriate frequency code.
c) In the Frequency Value field, key in the number of times the frequency code value must be repeated before a new cycle count must be run and press 
Enter.

### ATTACHING YOUR PROFILE TO ITEM OR LOCA <a id="attaching-your-profile-to-item-or-loca"></a>

You must attach your cycle count profile to all items or to all locations that you wish to include in the cycle count for that profile. You can do this manually or you can request a custom program from HighJump that will perform this task automatically.
You can attach a cycle count profile to an item or location at any time during the cycle count period. For example, if your cycle count period runs from January 1 to December 31 and you add a new item to your warehouse in June, you can attach the profile to the item when you add the item. The system will adjust the number of counts scheduled for the new item to take into account the fact that it was added in the middle of a cycle count period.

### SETTING UP AN EVENT-DRIVEN CYCLE COUNT <a id="setting-up-an-event-driven-cycle-count"></a>

You can generate event-driven cycle counts directly from your RF operations without the need to manually create item or location cycle counts in CYEN (Create Cycle Count). For example, when operators using 
RFPU, RFPIC, RFPK, RFRL and RFRP report variances, AccellosOne 3PL can generate new event-driven cycle count tasks so that another operator can go to the location and check the variance at a later time.
The following RF events will trigger an event-driven cycle count:
You set up event-driven cycle counts in CYEN by setting the cycle count type to E for Event-Driven. Then you attach your new cycle count profile to the Event-Driven Cycle Count Profile field in MRFP (RFPIC -2) tab.
NOTE Make sure that you attach location type profiles to locations only and item type profiles to items only. You cannot attach a location type profile to an item nor can you attach an item type profile to a location.
Event Result the operator requests an alternate location The event-driven cycle count will generate tickets for all inventory entities in the originally suggested location.
the operator indicates that a given location is NOT empty when the last item is picked or moved from that location
The event-driven cycle count will generate blank tickets (that is, no inventory levels shown) for the location.
the operator puts product on suspend hold The event-driven cycle count will generate tickets for all inventory entities in the location.

MRFP screen showing Event-Driven Cycle Count Profile (CYCP) field populated
For inbound event-driven cycle counting, you attach your new cycle count profile to the Event-Driven Cycle 
Count Profile field in MRFP (RFPU) tab.

MRFP screen showing Event-Driven Cycle Count Profile (CYCP) field populated

### SETTING UP A CYCLE COUNT FOR EACH LOCATION VISITED <a id="setting-up-a-cycle-count-for-each-location-visited"></a>

You can set up event-driven cycle counts for each location visited while picking in RFPIC or RFPK. AccellosOne 3PL will generate a cycle count task for each location visited even if the pick quantity is zero.
This type of cycle count is normally performed once at the end of the day for each location visited. For example, during the course of the day the RF operator picks twice from the same location and you want to do a single count at the end of the day for that location and not one count for each pick.
You activate event-driven cycle counting for each location visited by selecting an event-driven cycle count profile code in the Activate Event-Driven Cycle Count in RFPIC field in MIRP. You then attach your MIRP profile to the item(s) that you wish to count.
NOTE You perform event-driven cycle counts in RFCYE rather than RFCY.

MIRP screen showing Activate Event-Driven Cycle Count in RFPIC field

### SETTING UP YOUR CYCLE COUNT PROFILE DEFAULT IN ATMP <a id="setting-up-your-cycle-count-profile-default-in-atmp"></a>

In ATMP (Action Template Setup), you must set up a default cycle count profile for each company that you perform cycle counts in. The default cycle count profile can be any profile set up in CYCP (Cycle Count 
Profile). If there is no record in ATMP for CYEN, you must enter RFCYE and press F2 to create the necessary 
CYEN records.
CAUTION You must assign a real company coode to your default cycle count profile code. 
The .ALL company code cannot be used for this purpose.

ATMP screen showing A11 as default cycle count profile code for company V6

### Setting Up Your Cycle Count Ticket Document <a id="setting-up-your-cycle-count-ticket-document"></a>

The standard document for printing cycle count tickets is CYTI. This document must be set up as follows:
 Print Form Source Type = C
 Print Form Name = DP220

Documents (DOCU) screen for document CYTI (Cycle Count Tickets)

 Cycle Count Tickets
 Cycle Count 70 Type A Counted By ______________
 Entered By ______________
|Ticket Location Whse Hold | Quantity |
+-------------------------------------------------------------+--------------+
| 1 A100 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 2 A100 1 DMG | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 3 A100 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 4 A101 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 5 A101 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 6 A101 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| 7 A102 1 | |
+-------------------------------------------------------------+ |
| D Customer D | |
| | |
+-------------------------------------------------------------+--------------+
| | |

## Cycle Count Operations <a id="cycle-count-operations"></a>

*Manual B — Cycle Counting*

### Creating a Cycle Count <a id="creating-a-cycle-count"></a>

You create your cycle count in CYEN (Create Cycle Count). The main parameters that you define in this program are:
 the number of counts (single or dual) 
 the cycle count type (item or location)
 whether or not the count is arbitrary or scheduled
 your starting ticket number
 whether or not to allow multiple tickets for the same inventory entity 
 whether or not to show inventory levels on tickets (that is, whether to perform a blind or non-blind count)
 the cycle count profile or profiles that you wish to include in your cycle count
You can attach multiple cycle count profiles to the same cycle count. This function allows you to batch your cycle counts so that tickets from different profiles are printed together in the same job. For example, the same cycle count could include tickets for high value items counted every day in your daily cycle count profile and tickets for low value items counted monthly in your monthly cycle count profile.
NOTE Even though you schedule your cycle counts in CYCP, they are not generated automatically. Each time you wish to perform a cycle count, you must enter 
CYEN and create a new record. For example, if you cycle count daily, you must enter 
CYEN every day and create a new cycle count.
FIELD DESCRIPTIONS
A / B Count A = a single count
B = a dual count (not available for RF counting in RFCY)
If you are performing a single count, enter A. If you are performing a dual count, enter B. 
Item / Location / Event 
Type
I = Item
L = Location
E = Event Type (reserved for future use)
When you attach a cycle count profile to this cycle count, your cycle count type in the profile (either item or location) must match the value you enter in this field.

Arbitrary / Scheduled A = Arbitrary
S = Scheduled
If you select A for Arbitrary, the cycle count is an “extra” count that will not be added to the number of cycle counts that you specified in CYCP for the item or location. If you select S for Scheduled, the cycle count will count as a regular cycle count and will be added to the number of counts specified in CYCP.
For example, suppose item X is to be counted six times a year and you have already counted it three times. If you perform an arbitrary count, the system will consider item X to have been counted three times in the current year and will schedule three more counts. If you perform a scheduled count, the system will consider item X to have been counted four times in the current year and will schedule two more counts. 
Starting Ticket Number Mandatory
The ticket number that you wish to start from. For example, if you want your first ticket number to be 5, you would enter 5 in this field. You can assign each cycle count a unique series of numbers or you can reuse the same numbers for each cycle count. If you are using preprinted tickets, you enter the starting number from your preprinted tickets.
Sort Sequence Code (defined in SOSE)
Optional
This field allows you to customize the sort sequence of your locations so that cycle count tickets are printed in an order that makes sense for your warehouse. See [Defining the Sort Sequence of Your Locations](inventario-fisico.html#defining-the-sort-sequence-of-your-locations) for further information.
Document Code Mandatory
The document code for your cycle count tickets (usually CYTI). See [Setting 
Up Your Cycle Count Ticket Document](contagem-ciclica.html#setting-up-your-cycle-count-ticket-document) for further information on setting up this document
FIELD DESCRIPTIONS

Allow Duplicates per 
Location
N = No
Y = Yes
If you specify No, the system will not allow you to enter multiple tickets for the same physical inventory unit in CYET (Enter Cycle Count Tickets) or RFCY (RF - Cycle Count). A multiple ticket means two or more tickets for the same physical inventory unit in the same location. 
If you specify Yes, the system will allow you to enter multiple tickets for the same physical inventory unit. The Yes option is intended for two situations: 
you have a bulk location where the same physical inventory unit might be scattered around in different places or you allow mixed product in the same location. 
See [Blind vs. Non-Blind Counts](contagem-ciclica.html#blind-vs-non-blind-counts) for further information duplicate tickets.
Include Empty Locations Only available if you specify Locations as your Cycle Count type in CYCP. 
N = No
Y = Yes
If you specify No, only locations with an on-hand quantity of greater than 0 will have tickets printed for them. If you specify Yes, the system will print tickets for all locations regardless of their on-hand quantity. 
FIELD DESCRIPTIONS

Unique Inventory Entity 
Count
Only available if you specify Locations as your Cycle Count type in CYCP. 
N = No
Y = Yes
If you select No, unique inventory entity cycle counting will be deactivated and the RF operator will be prompted to enter inventory levels and quantities in 
RFCY. If you select Yes, unique inventory entity cycle counting will be activated and the RF operator will be prompted to enter the number of unique inventory entities per location in RFCY. 
Only if the count of unique inventory entities did not match the system count would the RF operator be required to enter a pallet count.
RFCY screen showing unique inventory entity count of 1 for location A201
FIELD DESCRIPTIONS

Show Level 1/2/3/4 on 
Ticket
N = No
Y = Yes
If you specify No, the inventory level will not be printed on the ticket. If you specify Yes, the inventory level will be printed on the ticket. 
For customers with two or more inventory levels, if you select Yes at one inventory level, all inventory levels “lower” than that level (that is, a higher number) can be set to either Yes or No. If you select No at a particular inventory level, levels “lower” than that level are not available.
If you are performing a non-blind count containing multiple accounts and these accounts have a different number of inventory levels, you should set this flag to Yes for the lowest inventory level in the count. For example, if one account on a cycle count has one inventory level, a second account has two inventory levels and a third account has four inventory levels, you should set the Show Inventory Level 4 on Ticket flag to Yes. 
Status A = Active
S = Skipped
P = Passed
I = Cycle count in progress
The status of the cycle count. A status of Active means that you have created the cycle count in CYEN but have yet to generate any tickets for it in CYGT. 
When you generate your tickets, the status changes from Active to In progress.
See [Looking Up the Status of a Cycle Count](contagem-ciclica.html#looking-up-the-status-of-a-cycle-count) for further information on cycle count statuses.
FIELD DESCRIPTIONS (Profile Block)
Cycle Count Profile Code The cycle count profile code that you defined in CYCP. If required, you can attach multiple cycle count profiles to the same cycle count.
Scheduled Date Scheduled counts only
Generated by the system. 
Actual Date Reserved for future use
FIELD DESCRIPTIONS

Random / Specific R = Random
S = Specific
If you select Random, the system chooses your items or locations based on the profile that you set up in CYCP. If you select Specific, you can choose the items or locations to count. However, if the item or location has already been counted the required number of times during the cycle count period, your choice will be rejected.
Include Item / Locations from Previous Count with 
Variances
N = No
Y = Yes (recommended)
If you select No, items or locations from the previous count that had variances will not be included in the current count. If you select Yes, items or locations from the previous count that had variances will be included in the current count. 
Include Variance Selections in Actual CountOnly available if you select Yes in the Include Item/Locations from previous count with variances field
N = No
Y = Yes
If you selected Yes in the previous field, you can specify in this field whether to adjust the total number of items or locations to be counted in the current count. 
For example, suppose you are scheduled to count 100 items in your current cycle count and you have 25 items with a variance from the previous count. If you select Yes, your total count will be 100 (only 75 new items plus the 25 items with variances from your previous count). If you select No, your total count will be 125 (your 100 new items plus the 25 items with variances from your previous count). 
Projected Item / Locations to CountThis system-generated number shows the number of locations or items that you should be counting in the current cycle count based on the parameters that you set up in CYCP. You can override this number if required by entering a number in the Actual Item/ Locations to Count field.
For arbitrary counts, this field is set to zero.
Actual Item / Locations to 
Count 
The actual number of items or locations that you wish to count for this cycle count. If you enter a value in this field, it will override the number of cycle counts in the Projected Item/Locations to Count field.
FIELD DESCRIPTIONS (Profile Block)

FIELD DESCRIPTIONS (Formula Block)
The Formula Block is only available if you select Specific in the Random/Specific field in the Profile Block. 
The Formula Block appears once only when you enter CYEN in create record mode. You cannot access this block after creating your cycle count.
Customer Code Item cycle counts only
Your customer code restriction.
Item Code Item cycle counts only
Your item code restriction.
Warehouse Code Location cycle counts only
Your warehouse code restriction.
Location Code Location cycle counts only
Your location code restriction.
Location Type Code Location cycle counts only
Your location type code restriction.
Isolator Code Location cycle counts only
Your isolator code restriction.
Zone Code Location cycle counts only
Your zone code restriction.

### CREATING A SCHEDULED CYCLE COUNT <a id="creating-a-scheduled-cycle-count"></a>

1 Make sure that the previous cycle count for the profile that you are using has been closed. You cannot proceed with the next cycle count while the previous one is still in progress.
2 Enter CYEN.

Create Cycle Count (CYEN)
3 Click on Create Record.
4 In the A / B Count field, key in the appropriate value (A if you are performing a single count or B if you are performing the second count of a dual count) and press Enter.
5 In the Item / Location / Event Type field, key in I for Item or L for Location and press Enter.
6 In the Arbitrary / Scheduled field, key in S for Scheduled and press Enter.
7 In the Starting Ticket Number field, key in your starting ticket number and press Enter.
8 If required, key in a sort sequence code and press Enter or press Enter with this field blank to bypass the option.
9 In the Document Code field, key in the document code for your cycle count tickets and press Enter. 
10 In the Allow Duplicates per Location field, key in Y for Yes or N for No and press Enter.
11 In the Include Empty Locations field, key in Y for Yes or N for No and press Enter. The Yes option is only available if you are cycle counting by location.
12 In the Unique Inventory Entity Count field, key in Y for Yes or N for No and press Enter.
13 In the Show Inventory Level 1/2/3/4 fields, key in Y for Yes or N for No and press Enter. If you select No for Level 1, Levels 2, 3 and 4 will automatically be set to No.
14 In the Status field, press Enter to accept the default value of A for Active. The system will display the Profile Block.

Create Cycle Count (CYEN) screen showing Profile Block
15 Click on Create Record.
16 In the Cycle Count Profile Code field, key in the cycle count profile that you created in CYCP and press 
Enter or use your pick list to select it.
The system will display the date scheduled for this cycle count.

Create Cycle Count (CYEN) screen showing Profile Block for scheduled count
17 If you want to select specific locations or items, key in S for Specific in the Random/Specific field and press Enter.
18 In the Include Item/Locations from Previous Count with variances field, key in Y for Yes or N for No and press Enter.
19 In the Include Variance Selection in Actual Count field, key in Y for Yes or N for No and press Enter. The 
Yes option is only available if you selected Yes in the previous field.
20 In the Actual Item/Locations to Count field, press Enter to accept the system value or key in a new value and press Enter. If the system-generated value is 0, you must enter a positive number to proceed.
21 If you wish to attach a second cycle count profile to this cycle count, repeat the above steps. 
22 When you finish adding your cycle count profiles, click on Return to Main.

23 If you are performing a location count, click on Location Block. If you are performing an item count, click on Item Block.
*AccellosOne 3PL supports the following restrictions:
If you selected Random in the 
Random/Specific field:
If you selected Specific in the 
Random/Specific field:
a) Proceed to next step. The system will select your items or locations.
a) When the Formula Block appears, enter your restrictions if any and press Enter at the end of each line. For example, to restrict to warehouse W1, you would enter =W1 in the Warehouse Code field.*
b) When you finish entering your restrictions, click on Return to exit the Formula Block.
c) When you exit, the system will search the database for all locations or items that meet the criteria that you specified. These items or locations will be displayed in the Item or Location 
Block. If you do not enter any restrictions, the system will display all items/locations from the cycle count profiles that you selected.
Restriction Description Example
= match of characters entered =A = all customers codes starting with A
> greater than or equal to >A = all customer codes greater than or equal to A
< less than or equal to <A = all customer codes less than or equal to A
- from X to Y (a range) A-C = Customers A through C

Create Cycle Count (CYEN) screen showing Item Block
24 If you are performing a Random count, the system-selected items or locations will be displayed. If you are performing a Specific count, the locations or items that meet the criteria that you specified will be displayed. If you decided to include in the cycle count items or locations from previous counts with variances, these items or locations will also appear.
You can add to this list as required or you can remove items or locations that you wish to skip for this cycle count. To add an item or location to the list, click on Create Record to enter create record mode. 
Then enter a value in each input field and key in Y for Yes in the Correct field. 
To remove an item or location from the list, press Enter until your cursor is positioned in the Correct field. 
Then click on Delete.
25 If you are in create record mode, click on Return to Main. 
26 Click on Return and Master Block. Then click on Exit to exit.

### TROUBLESHOOTING SCHEDULED CYCLE COUNTS <a id="troubleshooting-scheduled-cycle-counts"></a>

If there is no item or location in the Item or Location Block, there are a number of possible causes that should be investigated:
 you failed to attach the profile code to the item or location 
 the item or location is attached to another cycle count whose status is in progress
 your profile code has expired
If the projected item or locations to count is greater than actual item or locations to count, the item or location has been counted the required number of times during the cycle count period.

### CREATING AN ARBITRARY CYCLE COUNT <a id="creating-an-arbitrary-cycle-count"></a>

An arbitrary count is a one-time non-scheduled count of specific items or locations. You can perform an arbitrary cycle count at any time and it will have no effect on your scheduled cycle counts: the count of the item or location will not be advanced and its variance status will not be updated. 
For example, if you cycle count an item every week on Monday and then perform an arbitrary count on a particular Wednesday, the count scheduled for the following Monday must still be run and cannot be bypassed. If the item was in balance on the previous Monday and found to be out of balance on Wednesday, its status on the following Monday will be in balance — that is, the original status.
1 Enter CYEN.

Create Cycle Count (CYEN)
2 Click on Create Record.
3 In the A / B Count field, key in the appropriate value (A if you are performing a single count or B if you are performing the second count of a dual count) and press Enter.
4 In the Item / Location / Event Type field, key in I for Item or L for Location and press Enter.
5 In the Arbitrary / Scheduled field, key in A for Arbitrary and press Enter.
6 In the Starting Ticket Number field, key in your starting ticket number and press Enter.
7 If required, key in a sort sequence code and press Enter or press Enter with this field blank to bypass the option.
8 In the Document Code field, key in the document code for your cycle count tickets and press Enter. 
9 In the Allow Duplicates per Location field, key in Y for Yes or N for No and press Enter.
10 In the Include Empty Locations field, key in Y for Yes or N for No and press Enter. The Yes option is only available if you are cycle counting by location.
11 In the Show Inventory Level 1/2/3/4 fields, key in Y for Yes to perform a non-blind count or N for No to perform a blind count and press Enter.

12 In the Status field, press Enter to accept the default value of A for Active.
The system will display the Profile Block.

Create Cycle Count (CYEN) screen showing Profile Block
13 Click on Create Record.
14 In the Cycle Count Profile Code field, key in the cycle count profile that you created in CYCP and press 
Enter.
15 In the Random/Specific field, key in S for Specific and press Enter.

Create Cycle Count (CYEN) screen showing Profile Block for arbitrary count
16 In the Include Item/Locations from Previous Count with variances field, key in N for No and press Enter.
17 In the Actual Item/Locations to Count field, key in the number of items or locations that you wish to count and press Enter. 
18 If you wish to attach a second cycle count profile to this cycle count, repeat the above steps. 
19 When you finish adding your cycle count profiles, click on Return to Main to exit Create mode. Then click on Item Block or Location Block to display the Formula Block.

Create Cycle Count (CYEN) screen showing Formula Block for an item count
20 In the Formula Block, enter your restrictions if any and press Enter at the end of each line. The restrictions that you enter on this screen will restrict the items or locations to those that meet the criteria that you enter. 
For example, if you are cycle counting by location and wish to count only locations beginning with the letter A, you would key in =A in the Location Code field. When you access the Location Block, only locations beginning with the letter A attached to the cycle count profiles you selected for this cycle count will be displayed.
AccellosOne 3PL supports the following restrictions:
If you do not wish to specify any restrictions, press Enter to bypass all fields.
21 When you finish entering your restrictions, click on Return to display the Item Block or Location Block.
Restriction Description Example
= match of characters entered =A = all customers codes starting with A
> greater than or equal to >A = all customer codes greater than or equal to A
< less than or equal to <A = all customer codes less than or equal to A
- from X to Y (a range) A-C = Customers A through C

Create Cycle Count (CYEN) screen showing Item Block
22 The Item or Location Block will display all items or locations that met the criteria that you specified in the 
Formula Block. You can add new entries to this screen or you can delete entries that you do not wish to cycle count.
To add an item or location to the list, click on Create Record to enter create record mode. Then enter a value in each input field and key in Y for Yes in the Correct field. 
To remove an item or location from the list, press Enter until your cursor is positioned in the Correct field. 
Then click on Delete.
23 When you finish making your selections, click on Return, Master Block and Exit to exit.

### CANCELLING A CYCLE COUNT <a id="cancelling-a-cycle-count"></a>

When you cancel a cycle count, the next scheduled date is advanced for the item or location, but no inventory information is recorded and no change is made to its variance status. The projected number of items or locations to count for the following cycle count will be adjusted to take into account the items or locations that were missed. 
For example, suppose you count 10 items once a month. If you cancel your January count, the next scheduled count will be your normal February count. However, the projected number of items to count in 
February will be 20 not 10 to make up for the 10 counts that were missed in January. If any variances were discovered in the January count, they will not be carried forward because the count is deemed not to have taken place.
A cycle count must have a status of “in progress” before it can be cancelled. A cycle count is considered to be in progress once you have created it in CYEN and generated tickets for it in CYGT. It remains in progress until you close it in CYCO (Close Cycle Count).

1 Enter CYCC.
2 Key in the cycle count number that you wish to cancel and press Enter. 
3 Click on Process.

### SKIPPING A CYCLE COUNT <a id="skipping-a-cycle-count"></a>

You use the Skip command when you decide ahead of time not to perform a scheduled count. If you have already created your scheduled cycle count in CYEN and then want to skip it, you must use either the Cancel or Delete command.
1 Enter CYEN.
2 Click on Create Record.
3 In the A/B Cycle Count field, key in A and press Enter.
4 In the Item / Location / Event Type field, key in I for Item or L for Location and press Enter.
5 In the Arbitrary/Scheduled field, key in S for Scheduled and press Enter.
6 In the Starting Ticket Number field, key in 1 and press Enter.
7 Press Enter to bypass the Sort Sequence Code field.
8 In the Document Code field, key in the document code for your cycle count tickets and press Enter. 
9 In the Allow Duplicates per Location field, key in N for No and press Enter.
10 In the Include Empty Locations field, key in N for No and press Enter.
11 In the Show Inventory Level 1/2/3/4 fields, key in Y for Yes and press Enter.
12 In the Status field, key in S for Skipped and press Enter.
13 When the Profile Block appears, click on Create Record.
14 Key in the cycle count profile that you created in CYCP in the Cycle Count Profile Code field and press 
Enter.
15 In the remaining four fields in the Profile Block, press Enter to accept the system defaults. 
16 When a blank Profile Block is displayed, click on Master Block and Exit to exit.

### DELETING A CYCLE COUNT <a id="deleting-a-cycle-count"></a>

A cycle count can be deleted at any time in the cycle count process up until the time the count is closed in 
CYCO (Close Cycle Count) or passed in CYEN. When you delete a cycle count, the next scheduled date is not advanced for the item or location and the system considers that the count never took place. You use the 
Delete command when the cycle count has been improperly performed and you wish to redo it from scratch. 
There are two ways of deleting a cycle count; you can
 use the F2 (Delete) command in CYEN to delete the count
 delete the count in CYDE (Delete Cycle Count)
You use the F2 (Delete) command in CYEN to delete a cycle count whose status is active; that is, you have created the count in CYEN but have yet to generate your tickets in CYGT. You use CYDE to delete a cycle count that is in progress; that is, you have created your cycle count in CYEN and generated your tickets in 
CYGT.

### DELETING A CYCLE COUNT IN CYEN <a id="deleting-a-cycle-count-in-cyen"></a>

1 Enter CYEN.

2 Key in the cycle count number you wish to delete and press Enter. 
3 Press Enter once to display the F2 (Delete) command.
4 Click on Delete.
5 Click on Exit to exit.

### DELETING A CYCLE COUNT IN CYDE <a id="deleting-a-cycle-count-in-cyde"></a>

1 Enter CYDE.
2 Key in the cycle count number to be deleted and press Enter. 
3 Click on Process.

### DEFINING THE SORT SEQUENCE OF YOUR LOCATIONS <a id="defining-the-sort-sequence-of-your-locations"></a>

If necessary, you can customize the sort sequence or “snaking” of your locations. If you do not specify a sort sequence, your tickets will be generated in alphanumeric order (for example, locations A101, A102, A103, 
B101, B102, etc.)
Special sort sequences must be set up in SOSE (Sort Sequence Code) before they can be used. They require an “order by” statement in the Sort Sequence Formula field.

### ENTERING CYCLE COUNTS RETROACTIVELY <a id="entering-cycle-counts-retroactively"></a>

If you start using the AccellosOne 3PL cycle count system in the middle of your period of analysis, you must enter retroactively the cycle counts that have already passed. For example, if your period of analysis is 
January 01 to December 31 and you perform your first count using AccellosOne 3PL on March 1, you must create your January and February cycle counts retroactively. 
When you enter cycle counts retroactively, you create your scheduled cycle counts in CYEN using the 
Passed or Skipped command but you do not print tickets or enter any counts. Cycle counts performed before the installation of AccellosOne 3PL cycle counting are assumed to be correct and therefore no variances are recorded for these counts.
In the following example, it is assumed that:
 your cycle count period is Jan 01/08 to Dec 31/08
103 106 109 112
102 105 108 111
101 104 107 110
103 106 109 112
102 105 108 111
101 104 107 110
Tickets generated in numerical order (location 
101, 102, 103, 104, etc.)
Tickets generated using a custom sort sequence (location 103, 106, 109, 112, 111, 108, etc.)

 you cycle count monthly
 you installed the cycle count system on March 1 (current date) and therefore two cycle counts have passed
1 Enter CYCP (Cycle Count Profile) and create your cycle count profile. Enter Jan 01/08 as your current period start date and Dec 31/08 as your current period end date.
2 Enter CYEN (Create Cycle Count) and create a normal cycle count using the following values:
A/B Cycle Count = A
Item/Location Cycle Count Type = L if you are cycle counting by location or I if you are cycle counting by item
Arbitrary/Scheduled = S
Starting Ticket Number = 1
Document Code = your cycle count document
Allow Duplicates per Location = N
Include Empty Locations = N
Show Inventory Level 1/2/3/4 = Y
Create Cycle Count (CYEN) screen showing cursor positioned in Status field
3 In the Status field, key in P for Passed and press Enter. If the cycle count was not actually performed, key in S for Skipped and press Enter.
4 When the Profile Block is displayed, key in the cycle count profile that you created in CYCP in the Cycle 
Count Profile Code field and press Enter.
5 In the remaining four fields in the Profile Block, press Enter to accept the system defaults.
6 If you wish to attach a second cycle count profile to this cycle count, repeat the above steps.

7 When you finish attaching your cycle count profiles to this cycle count, click on Return to Main and Master Block. Then click on Exit to exit.
Your January cycle count has been passed.
8 Repeat steps 2 to 7 for your February cycle count.
9 Enter ADNC (Adjust Number of Cycle Counts) and set the New Count Number field to 3 for all items or locations in your cycle count. Refer to the section [Adjusting the Number of Cycle Counts](contagem-ciclica.html#adjusting-the-number-of-cycle-counts) for instructions on this procedure.
10 Your backdating is now complete. Proceed to perform a regular cycle count for March. Set the Status field to A for Active rather than P for Passed or S for Skipped and complete all the normal cycle count steps such as generating and printing your tickets and entering your counts.

### Generating Your Cycle Count Tickets <a id="generating-your-cycle-count-tickets"></a>

You generate your cycle count tickets in CYGT (Generate Cycle Count Tickets). You generate tickets based on the parameters you set up in CYEN. You can generate two types of tickets in CYGT:
 non-blank tickets 
 blank tickets 
If you are using your own preprinted tickets, you must still run CYGT to generate your tickets but you will not print your tickets in CYTI.
Non-blank tickets show the ticket number, customer code and location. Depending on the parameters you select in CYEN, they also show the item code and inventory levels you specified. Non-blank tickets must always be generated first in CYGT before any blank tickets are generated.
Blank tickets, on the other hand, show the ticket number code only with no location or item/inventory level information. Blank tickets are extra tickets that you use to count inventory found in the wrong location or in an unexpected location. As well, you can use blank tickets to record multiple entities in the same location.
NOTE If you wish to generate both non-blank and blank tickets for the same cycle count, you must do so in two separate batches. First you run CYGT for your nonblank tickets and print the tickets using CYTI. Then you rerun CYGT for your blank tickets and return to CYTI to print your second batch. You cannot generate both types of tickets in the same job and you must generate your non-blank tickets first.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count that you wish to generate tickets for. 

### GENERATING NON-BLANK TICKETS <a id="generating-non-blank-tickets"></a>

Non-blank tickets will show a ticket number, customer code and location. Depending on which of the Show flags you set to Yes in CYEN, item codes and/or inventory levels will also be printed.
1 Enter CYGT.

 Generate Cycle Count Tickets (CYGT)
2 Key in your cycle count number and press Enter.
3 In the Number of Blank Tickets field, key in 0 and press Enter. 
4 Click on Process to generate your tickets.

### GENERATING BLANK TICKETS <a id="generating-blank-tickets"></a>

Blank tickets will show the ticket number only but no location. You can generate as many blank tickets as you need and you can rerun CYGT as often as required to generate additional blank tickets. However, if you are performing a double count, it is best to make sure that you do not allocate too many blank tickets. Unused blank tickets are printed at the end of CYAB (Cycle Count Ticket Discrepancy Report) and large numbers of blank tickets will lead to numerous pages of wasted paper at the end of this report.
Number of Blank Tickets Optional
The number of extra blank tickets (if any) that you wish to print. The blank tickets that you create in this field show the ticket number only; location, item code or inventory level information is not printed. You use this option to count product that has no location or has been placed in the wrong location. You can also use blank tickets to record multiple entities in the same location.
Blank tickets can only be generated after you have generated your non-blank tickets. Therefore, set this field to zero when you run CYGT the first time to generate your non-blank tickets.
FIELD DESCRIPTIONS

1 Make sure that you have generated your non-blank tickets first.
2 Enter CYGT.
3 Key in your cycle count number and press Enter.
4 In the Number of Blank Tickets field, key in the number of blank tickets you require and press Enter. 
5 Click on Process to generate your tickets.

### Printing Your Cycle Count Tickets <a id="printing-your-cycle-count-tickets"></a>

You print the cycle count tickets that you generated in CYGT in CYTI (Print Cycle Count Tickets). In order to print your tickets, you need a print ticket document set up in DOCU (Documents). If you do not have such a document on your system (usually called CYTI), refer to the section [Setting Up Your Cycle Count Ticket 
Document](contagem-ciclica.html#setting-up-your-cycle-count-ticket-document) for further information on setting up this document.
You do not use this program if you enter your counts using an RF device or if you use preprinted tickets.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count that you wish to print tickets for. 
Reprint Tickets Only available if you have printed all tickets at least once.
N = No
Y = Yes
If you specify Yes, you can reprint cycle count tickets. 
Type of Count Only available when reprinting tickets.
A = A Count
B = B Count blank = Both A and B
The type of count whose tickets you are reprinting.
From Ticket Number Only available when reprinting tickets.
Your starting ticket number for reprinting tickets. 

### PRINTING NEW TICKETS <a id="printing-new-tickets"></a>

When you print tickets for the first time, you must print all tickets. You cannot print a range of tickets or tickets belonging to a particular type (A count or B count).
1 Enter CYTI.

Print Cycle Count Tickets (CYTI)
2 Key in your cycle count number and press Enter.
3 Click on Execute Report.
4 Key in your printer code and press Enter.
5 Click Ok.
6 When printing is complete, click on Exit to exit CYTI. If you are printing to screen by means of the VIEW printer code, do not exit CYTI until all your tickets are displayed in Adobe Acrobat.

### REPRINTING TICKETS <a id="reprinting-tickets"></a>

If you have printed all your tickets, you can reprint them as many times as you wish. You can reprint all tickets, all tickets belonging to a particular type of count (A or B) or a specified range of tickets.
The Allow Reprint flag in DOCU must be set to Y for Yes before you can reprint cycle count tickets.
1 Enter CYTI.
2 Key in your cycle count number and press Enter.
3 In the Reprint Tickets field, key in Y for Yes and press Enter.
To Ticket Number Only available when reprinting tickets.
Your ending ticket number for reprinting tickets. 
FIELD DESCRIPTIONS

4 In the Type of Count field, key in the appropriate value (A for your A count only, B for your B count only or blank for both your A and B count) and press Enter.
5 Do one of the following:
6 Key in your printer code and press Enter.
7 Click Ok.
8 When printing is complete, click on Exit to exit CYTI.

### Entering Your Cycle Count Tickets <a id="entering-your-cycle-count-tickets"></a>

You enter your cycle count tickets in CYET (Enter Cycle Count Tickets). If you set your Show flags in CYEN to 
No in order to perform a blind count, you must enter an item code, all inventory levels and a quantity for each ticket. If you set your Show flags in CYEN to Yes, your item codes and lot numbers, etc. will already be entered and you input the quantity only.
You can input your tickets in batches and re-enter CYET as many times as required in order to add another batch or correct or update your ticket count, item code, lot number, warehouse code or hold code. For example, you can count aisle 1 and enter your aisle 1 counts, then count aisle 2 and enter your aisle 2 counts, and continue in this manner aisle by aisle.
There are four scenarios that you may encounter when entering your tickets:
If you wish to specify a range:
If you do NOT wish to specify a range:
a) Key in your starting number and press Enter.
b) Key in your ending number and press Enter.
a) Press Enter twice to bypass the 
From Ticket Number and To 
Ticket Number fields.
If … then … there is no product in a location Enter a count of zero or skip the ticket.
during an item count, the right product is found in a location that was not included in the cycle count
Use a blank ticket to enter the product. 
Then make a manual adjustment in ENAJ, 
RELO or RFAJ.
during a location count, product is found in a location for which there is no ticket
Use a blank ticket to enter the product. 
Then make a manual adjustment in ENAJ or RFAJ.

If you set up a dual count in CYEN (Create Cycle Count), you must input CYET twice: once for your A count and once for your B count.
during a location count, product belonging to a customer not included in the cycle count is found in a location (for example, the cycle count is for Customer A and location 101 is a Customer A location, but you find product for Customer B in that location)
Ignore the product not included in the cycle count.
NOTE You must enter a count for each ticket in CYET for which you have inventory. 
If you only enter a count for certain items (for example, you enter counts for items A and B but not items C, D and E), the system will assume a count of zero for items C, 
D and E. As a result, these items will be incorrectly flagged as out of balance.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count whose tickets you wish to enter. 
Starting Ticket Mandatory
Your starting ticket number. 
Ending Ticket Mandatory
Your ending ticket number. You can improve system performance by entering your CYET counts in batches of 50 or 100. For example, if your starting ticket number is 101, you can enter a batch of 50 by making your ending ticket number 150.
If … then …

### ENTERING A BLIND COUNT <a id="entering-a-blind-count"></a>

You use this procedure if you have set all your Show flags to No in CYEN.
1 Enter CYET.
Count A = A Count
B = B Count
The count whose tickets you are entering.
Warehouse Mandatory for blank tickets only
If you wish to change a warehouse code for a non-blank ticket, press F9 to jump back to the Warehouse field and key in your new code.
Hold Mandatory for blank tickets only
If you wish to correct a hold code that was entered incorrectly for a non-blank ticket, press F9 to jump back to the Hold field and key in your correct code.
Item Code Mandatory 
Your item code.
Level 2/3/4 Mandatory if you have defined the customer as a customer with two, three or four inventory levels.
Your level 2/3/4 values.
Count Mandatory
The number of pallets, cases, etc. for the inventory entity. You can enter quantities of up to six digits for any given ticket in CYET. If you need to enter larger quantities, you must use blank tickets. For example, if your quantity is 
1,345,000, you enter a quantity of 345,000 for your non-blank ticket. Then you create two blank tickets and enter a quantity of 500,000 for each one. 
FIELD DESCRIPTIONS

Enter Cycle Count Tickets (CYET)
2 Key in your cycle count number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your count type (A or B) and press Enter.
TIP You can improve system performance by entering your tickets in batches. You enter your tickets in batches by specifying an ending ticket number in the Ending 
Ticket field. For example, if your starting ticket number is 101, you can enter a batch of 50 by making your ending ticket number 150.

Enter Cycle Count Tickets (CYET) screen for a blind count
6 Key in the item code for your first ticket and press Enter. If you have no product for that location, use your arrow key to skip to the next ticket.
7 If required, key in your level 2, 3 and 4 values (lot number, production date, etc.) and press Enter.
8 Key in your count and press Enter. If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts. 
Regardless of the SKU code that you use, the Adjustment Process flag must be set to Yes in the SKU 
Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.
9 If you need to correct a hold code or a warehouse code, press F9 to jump back to the appropriate field and enter your changes.
10 Repeat steps 6 to 8 for each ticket. If you wish to skip a ticket because there is no product in the location, use your arrow keys to skip the ticket.
11 If you are performing a dual count, repeat the count for your second count type (A or B).
12 When you finish entering your tickets, click on Return to Main and Exit to exit CYET.

### ENTERING A NON-BLIND COUNT <a id="entering-a-non-blind-count"></a>

You use this procedure if you have set one or more of your Show flags to Yes in CYEN.
1 Enter CYET.

Enter Cycle Count Tickets (CYET)
2 Key in your cycle count number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your count type (A or B) and press Enter.
TIP You can improve system performance by entering your tickets in batches. You enter your tickets in batches by specifying an ending ticket number in the Ending 
Ticket field. For example, if your starting ticket number is 101, you can enter a batch of 50 by making your ending ticket number 150.

Enter Cycle Count Tickets (CYET) screen for a non-blind count
If the item code and inventory levels are correct:
If the item code and inventory levels are NOT correct:
a) If the item code and inventory levels are correct (that is, the book value matches the cycle count value), key in your count and press Enter. 
b) If you have no product for that location, use your arrow key to skip to the next ticket or key in a quantity of zero.
c) If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.*
a) If the item code and inventory levels are NOT correct (that is, the book value does not match the cycle count value), press F9 to jump to the previous field. 
Then key in the correct item code and inventory level(s) plus your count and press Enter.
b) If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.*
c) If your item code is not accepted (for example, your count is for customer A and the item belongs to customer B), click on Clear 
Ticket to clear the ticket. 

6 If you need to correct a hold code or a warehouse code, press F9 to jump back to the field that requires modification and key in the correct code.
7 Repeat the above steps for each ticket. If you wish to skip a ticket because there is no product in the location, use your arrow keys to skip the ticket.
8 If you are performing a dual count, repeat the count for your second count type (A or B).
9 When you finish entering your tickets, click on Return to Main and Exit to exit CYET.

### ENTERING A BLANK TICKET <a id="entering-a-blank-ticket"></a>

1 Enter CYET.
2 Key in your cycle count number and press Enter.
3 Key in your starting ticket number and press Enter or press Enter to accept the system default (your first ticket).
4 Key in your ending ticket number and press Enter or press Enter to accept the system default (your last ticket).
5 Key in your count type (A or B) and press Enter.
6 If required, cursor down to the blank ticket.
* Regardless of the SKU code that you use, the Adjustment Process flag must be set 
to Yes in the SKU Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/ EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.
If the item code and inventory levels are correct:
If the item code and inventory levels are NOT correct:

Enter Cycle Count Tickets (CYET) screen for blank tickets
7 Key in your customer code and press Enter.
8 Key in your location code and press Enter.
9 Key in your warehouse code and press Enter.
10 If required, key in your hold code and press Enter.
11 Key in your item code and press Enter.
12 If required, key in your level 2, 3 and 4 values and press Enter.
13 Key in your quantity and press Enter. If you have a multiple quantity breakdown for the item, it is recommended that you use your lowest SKU code for all your counts.
Regardless of the SKU code that you use, the Adjustment Process flag must be set to Yes in the SKU 
Block of IQBP (Item Quantity Breakdown Profile) for that SKU code. For example, if your quantity breakdown is PALLETS/CASES/EACHES and the Adjustment Process flag in IQBP is set to Yes for pallets and cases and set to No for eaches, you must enter your counts in either pallets or cases. You cannot enter any counts in eaches.
14 Repeat steps 6 to 13 for each additional blank ticket that you wish to enter.
15 When you finish entering your blank tickets, click on Return to Main and Exit to exit.

### ENTERING YOUR COUNTS WITH RF <a id="entering-your-counts-with-rf"></a>

If you are entering your tickets by means of an RF device, you use the program RFCY (RF Cycle Count) 
instead of CYET. However, you can still access CYET to look up cycle count tickets and to enter adjustments. 
The following restrictions apply to RFCY:
 You can enter A counts only; you cannot perform a dual count in RFCY.

 You can enter fully blind and fully non-blind counts in RFCY, but you cannot enter partially blind counts. 
A partially blind count is a count in which the lowest inventory level or levels is blind while the higher inventory levels are non-blind; for example, Show Level 1 on Ticket in CYEN is set to Yes and Show 
Level 2 on Ticket is set to No.
You can enter quantities of up to six digits for any given ticket in RFCY. If you need to enter larger quantities, you must use blank tickets. For example, if your quantity is 1,345,000, you enter a quantity of 345,000 for your non-blank ticket. Then you create two blank tickets and enter a quantity of 500,000 for each one. 

### ENTERING A NON-BLIND COUNT <a id="entering-a-non-blind-count"></a>

1 Enter RFCY.
2 Key in your cycle count number and press Enter.
RF Cycle Count (RFCY) screen
3 If you are performing a location count, press Enter with your location field blank to display the first location to be counted. If you are performing an item count, press Enter with your item field blank to display the first item to be counted.
RF Cycle Count (RFCY) screen
4 Key in your location and press Enter.

5 Key in the quantity for this location and press Enter. If you have a multiple quantity breakdown for the item, you must use your lowest SKU code for all your counts. 
6 Repeat steps 4 and 5 for your next ticket. If you do not wish to enter your tickets in the order in which they are displayed in RFCY, use your up and down arrow keys to scroll through your tickets until you find the location or item that you wish to count.
7 When you finish entering all your tickets, you will be prompted with the following message:
RF Cycle Count (RFCY) screen
8 If you enter Y for Yes, a blank RFCY screen will be displayed. Enter your blank ticket and then press F4 the required number of times to exit. If you enter N for No, your count is complete. Press F4 the required number of times to exit.

### ENTERING A BLIND COUNT <a id="entering-a-blind-count"></a>

1 Enter RFCY.
2 Key in your cycle count number and press Enter.
If the cycle count item/quantity matches the book item/ quantity:
If the cycle count quantity does NOT match the book quantity:
If the cycle count item does NOT match the book item:
a) If the item code and inventory levels are correct (that is, the book value matches the cycle count value), key in your count and press Enter. 
 If you have no product for that location, use your arrow key to skip to the next ticket or key in a quantity of zero.
a) The following message will appear: 
b) Key in Y for Yes to acknowledge the message and press 
Enter.
a) Enter a quantity of zero for that item/location. Then press 
F3 (New Ticket) to display a blank ticket screen. Lastly, key in the location and the correct item information and quantity.
b) When you finish entering your blank ticket, press F4 to exit. 
Then key in your cycle count number and press Enter with either the location code or item code field blank to display the next location or item to be counted.

RF Cycle Count (RFCY) screen
3 If you are performing a location count, press Enter with your location field blank to display the first location to be counted. If you are performing an item count, press Enter with your item field blank to display the first item to be counted. AccellosOne 3PL will display the customer code for the product that is supposed to be in that location.
RF Cycle Count (RFCY) screen

4 Do one of the following:
5 Key in your level one value and press Enter.
6 Press Enter to bypass the CU (Customer Code) field.
7 If you use multiple inventory levels, key in your level 2, 3 and 4 values, pressing Enter after each level.
8 If there is a hold on the product, key in your hold code and press Enter.
9 Key in your quantity for this product in this location and press Enter. If you have a multiple quantity breakdown for the item, you must use your lowest SKU code for all your counts.
10 Repeat steps 4 through 9 for your next ticket. If you do not wish to enter your tickets in the order in which they are displayed in RFCY, use your up and down arrow keys to scroll through your tickets until you find the location or item that you wish to count.
11 When you finish entering all your tickets, you will be prompted with the following message:
RF Cycle Count (RFCY) screen
12 If you enter Y for Yes, a blank RFCY screen will be displayed. Enter your blank ticket and then press F4 the required number of times to exit. If you enter N for No, your count is complete. Press F4 the required number of times to exit.
If the customer code is correct:
If the customer code is NOT correct:
If there is no product in the location:
a) Key in your location and press 
Enter.
a) Do not verify the location. 
Press F3 (NT) to create a blank ticket. Then enter the location, item and quantity information for the customer that was not on the cycle count ticket.
b) When you finish entering your blank ticket, press F4 to exit. 
Then key in your cycle count number and press Enter with either the location code or item code field blank to display the next location or item to be counted.
a) Do not verify the location. 
Press your down arrow key to the next ticket and enter the location for that ticket.

### ENTERING AN EVENT-DRIVEN COUNT <a id="entering-an-event-driven-count"></a>

You count event-driven cycle counts in the RF program RFCYE. When you enter RFCYE, AccellosOne 3PL automatically retrieves the first open cycle count so there is no need for you to know the cycle count number. 
If there are no open cycle counts, you can request a new event-driven cycle counting by pressing F2 (Check 
Events); once the count is created, you can start counting right away in RFCYE.
RFCYE screen showing prompt to check events (F2)
RFCYE screen showing prompt to enter location

### ENTERING A UNIQUE INVENTORY ENTITY COUNT <a id="entering-a-unique-inventory-entity-count"></a>

If the count of unique inventory entities in a location matches the system count, the count for that location is complete and RFCY will display the next location to count. If, however, the count of unique inventory entities in a location does NOT match the system count, the RF operator must confirm the location and enter a pallet count for each inventory entity in the location.
1 Enter RFCY.
2 Key in your cycle count number and press Enter.

RFCY screen
3 Press Enter in the LOC field to retrieve the first location to count.
RFCY screen showing prompt for number of unique inventory entities (system count = 1 unique inventory entity in location A200)
4 Key in the number of unique inventory entities in the location and press Enter.

5 Do one of the following:
RFCY screen showing prompt for location
6 Scan in your location. 
If your count matches the system count:
If your count does NOT match the system count:
The following message will appear:
a) Press Enter to acknowledge the message.
b) Proceed to setp 8.
The following message will appear:
a) Press Enter to acknowledge the message.
b) Proceed to setp 6.

RFCY screen showing prompt for pallet quantity
7 Key in your pallet quantity for the inventory entity and press Enter. 
8 RFCY will display the next location to be counted.
RFCY screen showing prompt for number of unique inventory entities
9 Continue to perform your unique inventory count for each location.
10 When you count your last location, the following screen will display.

RFCY screen showing prompt to add new tickets
11 Key in Y for Yes or N for No and press Enter.
12 Do one of the following:

### Reconciling a Dual Count <a id="reconciling-a-dual-count"></a>

If you set up a dual count in CYEN (Create Cycle Count), you must input CYET twice: once for your A count and once for your B count. After you have entered both counts, you must perform a reconciliation in CYAB (Cycle Count Ticket Discrepancy Report). CYAB shows all items where the A count differs from the B count. 
When CYAB is empty, this means that your A count and B count are identical. 
Your A count is the count used to record variances; therefore, it is not essential to correct your B count in 
CYET if your A count is correct.
If you entered No: If you entered Yes:
a) Your cycle count is complete. a) You will be prompted to add a new ticket to the count.

TIP If you have a large number of unused blank tickets, you should clear them in 
CYET before running CYAB. If you do not clear your unused blank tickets in CYET, they will print at the end of CYAB and you will waste paper by printing unnecessary pages.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count whose A and B count you wish to reconcile. 
ABC Warehousing, Inc. Cycle Count No:137 Page 1 of 3
A To B Discrepancies (CYAB) 01.17.05 13:32
------------------------------------------------------------------------------------------------------------------------------------
Ticket Customer Whse Location Item Level 2 Level 3 Description Quantity
------ ---------- ---- --------- -------------------- -------------------- --------------- ------------------ --------------------
2 A D 1 A101 D1 102 GN000255 Item D1 0CASE
2 B D A101 D1 102 GN000255 Item D1 25CASE
4 A D 1 A101 D1 108 GN000261 Item D1 0CASE
4 B D A101 D1 108 GN000261 Item D1 50CASE
9 A D 1 A102 D1 101 GN000254 Item D1 1PLT
9 B D A102 D1 101 GN000254 Item D1 15CASE
11 A D 1 A104 D1 101 GN000254 Item D1 0CASE
11 B D A104 D1 101 GN000254 Item D1 75CASE
12 A D 1 A105 D1 103 GN000259 Item D1 15CASE
12 B D A105 D1 103 GN000259 Item D1 0CASE
14 A D 1 S100 D1 108 GN000263 Item D1 2PLT
14 B D S100 D1 108 GN000263 Item D1 1PLT 70CASE
16 A D 1 S100 D1 108 GN000261 Item D1 0CASE
16 B D S100 D1 108 GN000261 Item D1 2PLT
17 A D 1 S100 D2 105 GN000262 Item D2 2PLT
17 B D S100 D2 105 GN000262 Item D2 0CASE
18 A D 1 S101 D1 104 GN000257 Item D1 1PLT 90CASE
18 B D S101 D1 104 GN000257 Item D1 0CASE

1 Enter CYAB.

Create Cycle Count Ticket Discrepancy Report A (CYAB)
2 Key in your cycle count number and press Enter.
3 If required, key in your item code or location restriction and press Enter.
4 Key in your printer code and press Enter.
5 Click Ok.
6 When the report is printed, note any discrepancies and recount those items to arrive at the correct count.
7 Re-enter CYET and make any necessary corrections to either your A count or your B count.
8 Rerun CYAB to ensure that it is now empty.
Item Code Only available for item counts
If you enter an item code in this field, the report will be restricted to that item. 
Location Code Only available for location counts
If you enter a location code in this field, the report will be restricted to that location. 
FIELD DESCRIPTIONS

### DEALING WITH VARIANCES <a id="dealing-with-variances"></a>

There are a number of options in AccellosOne 3PL for dealing with variances:

### Closing Your Cycle Count <a id="closing-your-cycle-count"></a>

Once you have validated your cycle count and you accept all the variances, you must close the count in 
CYCO (Close Cycle Count). You cannot perform the next cycle count until you close the current one. If you attempt to cycle count an item or location that is already on an unclosed count, the item or location will be “locked” and not available in the Item or Location Block of CYEN.
Closing a cycle count advances the date and the number of counts for each item or location in the count whose quantity fell within the variance you allow in CYCP.
If . . . then . . .
you can explain the cause of the variance (for example, the missing 
100 cases is the result of an unconfirmed order)
You can temporarily suppress the variance in CYFO (Force Cycle Count Balance). The variance will not be reported in CYBK (Cycle Count Book Report) and the item / location will not be recounted if you select Y for Yes in the Include Item/Location from 
Previous Count with Variances field in 
CYEN.
the variance is not serious You can do nothing. The item or location will be flagged as out of balance and will be recounted on the next scheduled cycle count for that item or location.
the variance needs careful monitoringYou can do nothing for current count. However, on your next scheduled count, you can set the Include Item/Locations from previous count with variances flag to Yes. 
This will force the item or location to be recounted.
the variance is serious You can perform an arbitrary count on the item or location to check it again. If the arbitrary count balances, you can set the 
Include Item/Locations from previous count with variances flag to Yes on your next scheduled count. This will force the item or location to be recounted. If it balances on the scheduled count, the count will be advanced for the item or location and its variance status will be set to no variance.

If required, you can close a cycle count that is not complete. For example, if you are supposed to count items 
A, B and C on a particular cycle count but decide not to count item C, you can still close the cycle count in 
CYCO. However, the system will warn you that you are missing one count and the number of counts for item 
C will not be advanced. 
1 Enter CYCO.

Close Cycle Count (CYCO)
2 Key in your cycle count number and press Enter.
3 Click on Process to close your cycle count.
CAUTION Make sure that you run the cycle count book report in CYBK plus any other required reports before closing a cycle count. You cannot print these reports after a cycle count has been closed.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count. 
Status I = In progress
U = Updated for close 
If the status is In progress, the cycle count tickets have been generated and you can close the count. If the status is Updated for close, the cycle count has already been closed.

LOOK-UP AND ADJUSTMENT 
PROGRAMS

## Look-Up And Adjustment Programs <a id="look-up-and-adjustment-programs"></a>

*Manual B — Cycle Counting*

### Looking Up the Status of a Cycle Count <a id="looking-up-the-status-of-a-cycle-count"></a>

You look up the status of a cycle count in CYEN. There are ten possible statuses for a cycle count:
STATUS DESCRIPTION
A Active (you have created the cycle count in CYEN)
C Closed (you have closed your cycle count in CYCO)
D Deleted (you have deleted the cycle count)
G Generated (the cycle count program failed to generate tickets)
I In progress (you have generated tickets in CYGT)
K Cancelled (you have cancelled the cycle count in CYCC)
P Passed (you have used the passed option in CYEN)
S Skipped (you have used the skipped option in CYEN)
U Closing update in progress (the count is in the process of being closed)
X Calculation update in progress (the system is calculating the items or locations to count)
Y Deletion in progress.

Create Cycle Count (CYEN) screen showing status of A for Active
If you want to look up an item or location to find out the last cycle count that it was on, you must use the program ADNC (Adjust Number of Cycle Counts).

### Looking Up the Current Count of an Item or Location <a id="looking-up-the-current-count-of-an-item-or-location"></a>

You can look up the current count of an item or location in ADNC (Adjust Number of Cycle Counts).
1 Enter ADNC.
2 Key in your cycle count type (I for Item or L for Location) and press Enter.
3 Key in your cycle count profile code and press Enter.
4 Click on Change Block.
The system will display the current count number for the item or location that you selected.
If you are cycle counting by item:
If you are cycle counting by location:
a) Key in your customer code and press Enter. 
b) Key in your item code and press 
Enter.
a) Key in your warehouse code and press Enter.
b) Key in your location code and press Enter.

Adjust Number of Cycle Counts (ADNC) showing a current count of 2
5 Click on Return to Main and Exit to exit the program.

### Forcing a Cycle Count Balance <a id="forcing-a-cycle-count-balance"></a>

You can force your cycle count to balance in CYFO (Force Cycle Count Balance); that is, you override your 
CYET or RFCY count and temporarily set the variance to zero. You use CYFO to force a cycle count to balance when you wish to temporarily suppress the variance because you can explain its cause. 
For example, suppose you pick 100 cases from location A101 to fill an order. When you count the location, the book value is 100 because the order is unconfirmed and the actual count is 0. Because the cause of the variance is an unconfirmed order, you can force the cycle count to balance. 
When you force a cycle count to balance, the variance will not be reported in CYBK (Cycle Count Book 
Report) and the item/location will not be recounted if you select Y for Yes in the Include Item/Location from 
Previous Count with Variances field in CYEN.

If you wish to force a dual cycle count to balance, your A count and B count must match. Consider the following examples.
In example 1, the A count and B count match so the cycle count can be balanced. In example 2, the A count (80) does not match the B count (79). You must correct either your A count or B count in CYET before you can force your cycle count to balance in CYFO.
1 Enter CYFO.

Force Cycle Count Balance (CYFO)
2 Key in your cycle count number and press Enter.
3 Press Enter twice to bypass the Starting Ticket and Ending Ticket fields.
EXAMPLE 1 EXAMPLE 2
A Count = 79 A Count = 79
B Count = 79 B Count = 80
Book = 80 Book = 80

Force Cycle Count Balance (CYFO)
4 Press your Up or Down arrow keys until your cursor is positioned on the ticket that you wish to balance.
5 In the Force Balance field, key in Y for Yes and press Enter.
6 If there is more than one ticket with the same inventory, you must repeat the previous step for each ticket.
7 When you finish forcing your cycle count to balance, click on Return to Main and Exit to exit.

### Adjusting the Number of Cycle Counts <a id="adjusting-the-number-of-cycle-counts"></a>

You can manually override the count of an item or location in ADNC (Adjust Number of Cycle Counts). You typically use ADNC in two situations:
 you wish to change the number of counts for an item or location (for example, you start cycle counting item A five times a year and later decide that you only want to count it twice a year)
 you start cycle counting in the middle of your cycle count period and you wish to advance the number of counts to take into account the counts that were skipped or passed

FIELD DESCRIPTIONS
Cycle Count Type I = Item
L = Location
The type of cycle count. 
Cycle Count Profile Code Optional
If required, the cycle count profile code.
Customer Code Mandatory if you select item as your cycle count type
The customer code. 
Item Code Mandatory if you select item as your cycle count type
The item code.
Warehouse Code Mandatory if you select location as your cycle count type
The warehouse code. 
Location Code Mandatory if you select location as your cycle count type
The location code.
FIELD DESCRIPTIONS (Change Block)
Current Count Number The current count number for the item or location. 
New Count Number Mandatory
The new count number for the item or location.

1 Enter ADNC.

Adjust Number of Cycle Counts (ADNC)
2 Key in your cycle count type (I for Item or L for Location) and press Enter.
3 Key in your cycle count profile code and press Enter.
4 Click on Change Block.
5 The system will display the current count number for the item or location that you selected.
If you are cycle counting by item:
If you are cycle counting by location:
a) Key in your customer code and press Enter. 
b) Key in your item code and press 
Enter.
a) Key in your warehouse code and press Enter.
b) Key in your location code and press Enter.

Adjust Number of Cycle Counts (ADNC)
6 In the New Count Number field, key in your new count and press Enter.
7 Click on Process Change to process the change.
8 Click on Exit to exit the program.

### Updating Inventory <a id="updating-inventory"></a>

You can update your inventory in CYUP based on counts entered during a cycle count. CYUP shows the count, on hand quantity, variance quantity and movement status of each ticket after it has been entered in either CYET (Enter Cycle Count Tickets) or RFCY (RF Cycle Count). The Movement flag (Y for Yes or N for 
No) indicates whether there has been any movement in the location since it was last counted.
There are three possible actions in this program for each ticket: Accept, Delete or Manual. The Accept command will adjust your inventory based on the ticket count in your cycle count. The Delete command will exclude the ticket from the adjustment to inventory. The Manual command will exclude the ticket from the adjustment to inventory and flag the ticket as requiring a manual count or adjustment.
NOTE You must assign an action to each ticket in the cycle count before you can update your inventory. You cannot update inventory if the Action field for any ticket is blank.

Updating inventory in CYUP is final and closes the cycle count.
1 Enter CYUP.
CYUP Enter Query screen
2 Key in your cycle count number and press Enter.
3 Key in A for your A count or B for your B count and click on Execute Query to retrieve your cycle count.
CYUP screen showing tickets 17 and 18 with variances
4 Use the arrow keys to position your cursor over the ticket that you wish to update.
5 Key in the appropriate value (A for Accept, D for Delete or M for Manual) and press Enter.
6 If you enter D for Delete, click on Yes to confirm the deletion.
7 Repeat the above step for each ticket in the cycle count.
Alternatively, you can click on Select All to set the Action code for all tickets to A for Accept. If you make a mistake and wish to undo your Select All, you can click on Deselect All to set the Action code for all tickets to blank.
8 When all tickets have been assigned an action, click on Process to update your inventory.

9 When prompted to confirm the update, click on Yes.

## Cycle Count Reports <a id="cycle-count-reports"></a>

*Manual B — Cycle Counting*

### Cycle Count Book Report (CYBK) <a id="cycle-count-book-report-cybk"></a>

This report shows variances between your book count and your cycle count. There are two sections in this report:
 counted inventory
 inventory not counted (only included if the Print Inventory Not Counted flag is set to Yes)
NOTE The book quantity in CYBK is the on-hand quantity of a given location at the time that the cycle count was created in CYEN. It is not the on-hand quantity at the time that you enter your tickets in CYET or you run the cycle count book report in 
CYBK.

Counted inventory includes all inventory that was counted; that is, you entered a ticket — either blank or nonblank — for the entity in CYET. If the quantity for a ticket in CYET is zero, the ticket is still considered counted inventory and will appear in CYBK with a quantity of zero.
Inventory not counted includes the following: 
 cleared tickets
 tickets for which you did not enter a quantity in CYET (non-blind counts only)
 inventory with no ticket because it was not found in that location (blind counts only) 
The non-zero totals in the Difference column show which items had a variance. If the variance exceeds the variance allowed in CYCP, the item will be flagged as having a variance. 

If an item has a variance and has undergone activity since the start of the cycle count (for example, the item has been received, ordered, relocated or adjusted), CYBK will print an extra line showing the type of activity and the number of units affected.
You can generate this report at any inventory level that you wish. For example, if you generate CYBK at the item level, the report will show your cycle count versus book quantities for items only and no level 2, 3 or 4 quantities will be printed. Alternatively, if you generate CYBK at the lot level (level 2), the report will show your cycle count versus book quantities for each lot — not each item.
You can rerun CYBK as many times as you like with different options each time. For example, you can run 
CYBK once with the Report Level 2 flag set to No and once with the Report Level 2 flag set to Yes. However, it is highly recommended to run this report at least once with the Print Inventory Not Counted flag set to Yes. 
You cannot run CYBK for a cycle count that has been closed.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count. 
Print Inventory Not 
Counted
N = No
Y = Yes
In this field, you specify your print options for inventory not counted. Inventory not counted means all cleared tickets plus all tickets that were not counted in 
CYET.
If you specify No, inventory not counted will not appear in the report. If you specify Yes, inventory not counted will be shown at the end of the report after all the inventory that was counted.
GP8526 17 in Monitor 27 42 -15 CASE
 Type Document Units Weight
 ------------------------------------
 ER 1608 15 258.75
 Total : 27 42 -15

Display Variances Only N = No
Y = Yes
If you specify No, all items included in the cycle count will be printed in the report. If you specify Yes, only items with variances will be included on the report. A variance occurs whenever the cycle count quantity, inventory level, location or hold code does not match the book quantity, inventory level, location or hold code.
NOTE Variances in CYBK are not related to the variances that you enter in the Variance Allowed field in CYCP. If you set your variance allowed value to 
90% and your cycle count value differs from your book value by 1%, the item or location will still appear in CYBK as a variance.
Include Balanced Zero 
Quantity
N = No
Y = Yes
If you specify No, items for which the book count and the physical count are both zero will be excluded from the report. If you specify Yes, items for which the book count and the physical count are both zero will be included in the report.
Location Details N = No
Y = Yes
If you specify No, locations will not be printed on the report. If you specify Yes, locations and all inventory levels will be shown for each item. Therefore, when you enter Yes, you will not have access to the Report Level 2, Level 3 and 
Level 4 fields. 
FIELD DESCRIPTIONS

1 Enter CYBK.
2 Click on Enter Criteria. Then key in your cycle count number and click on Execute Query.

Cycle Count Book Report for customer with three inventory levels
Report Level 2/3/4 Only available if your customer has two or more inventory levels.
N = No
Y = Yes
The number of inventory levels displayed depends on the customer whose items you are cycle counting. If you specify No, no level 2/3/4 values (lot number, production date, etc.) will be printed on the report. Only the item and the quantity for that item will be shown and there will no breakdown by inventory level. If you specify Yes, level 2/3/4 values will appear on the report and a quantity shown for each value.
If you specify the No option for any inventory level (for example, No for level 
2), the Yes option is not available for lower inventory levels (for example, level 
3). If you specify the Yes option for any inventory level, you can select either 
Yes or No for lower inventory levels.
FIELD DESCRIPTIONS

3 In the Print Inventory Not Counted field, key in the appropriate value (N for No or Y for Yes) and press 
Enter.
4 In the Display Variances Only field, key in N for No or Y for Yes and press Enter.
5 In the Include Balanced Zero Quantity field, key in N for No or Y for Yes and press Enter.
6 In the Location Details field, key in N for No or Y for Yes and press Enter.
7 If the customer has a second inventory level, key in N for No or Y for Yes in the Report (Lot Number/Production Date, etc.) field and press Enter. Repeat this step for any other inventory levels that the customer may have.
8 In the Printer Code field, key in your printer code and click Ok.

### Cycle Count Summary Report (CYSR) <a id="cycle-count-summary-report-cysr"></a>

This report is a summarized version of CYBK. It shows the cycle count number, the type of count (A or B), the cycle count date, whether it is an item/location count (type = “Planned”) or an event-driven count (type = “Event-generated”), the total number of tickets generated, the number of RF supervisor counts, the number of brokers or customers, the number of unique level 1’s, the number of unique level 4’s, the number of locations counted and the status of the count.
You can restrict this report by start and end cycle count number or start and end cycle count date.
FIELD DESCRIPTIONS
Start Cycle Count NumberYour start cycle count number or blank for no start cycle count number.
End Cycle Count Number Your end cycle count number or blank for no end cycle count number. If you wish to report on a single cycle count, your end cycle count number can be the same as your start cycle count number.
ABC Warehousing, Inc. Date From : 03.04.07 Page 1 of 1
Cycle Count Summary Report (CYSR) Date To : 03.04.10 03.04.10 17:40
------------------------------------------------------------------------------------------------------------------------------------
 Cycle # Count Date Type Stan.Tic. Sup.Tic. Brokers Level1s Level4s Locations Status
 -------- ----- --------- ------------------ --------- -------- ------- ------- ------- --------- ------------------------------
 161 A 09.25.09 Planned 5 2 1 2 100 25 Deleted
 162 A 01.07.10 Planned 7 3 2 5 125 30 Closed
 166 B 03.04.10 Planned 9 1 1 3 115 32 Active
 -------- --------- -------- ------- ------- ------- ---------
 3 Report Totals 21 6 5 10 340 87

1 Enter CYSR.
Start Date Only available if either the Start or End Cycle Count Number field is blank
Your start cycle count date.
End Date Only available if either the Start or End Cycle Count Number field is blank
Your end cycle count date.
FIELD DESCRIPTIONS

2 Do one of the following:
3 Key in your printer code and click Ok.

### Pre-Cycle Count Location Report (PCLR) <a id="pre-cycle-count-location-report-pclr"></a>

This location report shows the location, level 1, 2, 3 and 4 values, quantities on hold with hold code, on order, on hand and available quantities and customer. The report is sorted by warehouse and by location.
If you wish to restrict the report by a range of cycle count numbers:
If you wish to restrict the report by a range of cycle count dates:
a) Key in your start cycle count number and press Enter.
b) Key in your end cycle count number and press Enter.
a) Press Enter twice to position your cursor in the Start Date field.
b) Click on the start date pop-up calendar and select your start date from the date pick list.
c) Click on the end date pop-up calendar and select your end date from the date pick list.
d) Press Enter to confirm your date selections.
ABC Warehousing Inc. From Location: A100 Page 1 of 1
Pre Cycle Count Location Report (PCLR) To Location: Last Order By: Location 04.18.08 11:11
------------------------------------------------------------------------------------------------------------------------------------
Location Item Code Level 2 Level 3 SKU On Hand On Order On Hold Hold Available Customer
------------ -------------------- --------------- ---------- ---- ---------- ---------- ---------- ---- ---------- ----------
Warehouse Code : 1 Warehouse 1
A101 D2 108 GN000266 CASE 185 35 0 159 D
 Item D2
 ---------- ---------- ---------- ----------
Location Total: 185 35 0 159
A107 D2 9 GN000261 CASE 25 0 0 0 D
 Item D2
 ---------- ---------- ---------- ----------
Location Total: 25 0 0 0
S100 D2 108 GN000266 CASE 15 15 0 0 D
 Item D2
 ---------- ---------- ---------- ----------
Location Total: 15 15 0 0
 ---------- ---------- ---------- ----------
Warehouse Total: 225 50 0 159
 ---------- ---------- ---------- ----------
Company Total: 225 50 0 159

FIELD DESCRIPTIONS
Customer Code If you enter a customer code in this field, the report will be restricted to inventory for that customer. If you leave this field blank, the report will show inventory for all customers.
Warehouse Code If you enter a warehouse code in this field, the report will be restricted to inventory in that warehouse. If you leave this field blank, the report will show inventory for all warehouses.
Starting/Ending Location Only product found in the range of locations that you specify will be included in the report.
Item Code If you enter an item code in this field, the report will be restricted to that item. If you leave this field blank, the report will show all items for the customer(s) that you specify.
Level 2 If you enter a level 2 value in this field, the report will be restricted to that item. 
If you leave this field blank, the report will show all level 2 values for the customer(s) that you specify.
Level 3 If you enter a level 3 value in this field, the report will be restricted to that item. 
If you leave this field blank, the report will show all level 3 values for the customer(s) that you specify.
Display Item Description Y = Yes
N = No
If you select Y for Yes, the report will show the item description. If you select N for No, the report will show the item code only with no description.
Display Quantities Y = Display Quantity
N = Suppress Quantity
If you enter Yes, the report will show the quantity. If you enter No, the report will not show the quantity.
Display Count Line Text Only available if Display Quantities is set to Y for Yes
Y = Display the blank line to write the quantity
N = Do not display the blank line
If you enter Yes, the report will print blank lines for writing down your counts. If you enter No, the report will not print blank lines for entering counts. 

1 Enter PCLR.

2 Key in your customer code and press Enter or press Enter with this field blank to report on all customers.
3 Key in your warehouse code and press Enter or press Enter with this field blank to report on all warehouse.
4 Key in your starting location and press Enter or press Enter with this field blank to run the report with no starting location.
5 Key in your ending location code and press Enter or press Enter with this field blank to run the report with no ending location.
6 Key in your item code and press Enter or press Enter with this field blank to report on all items.
7 Key in your level 2 value and press Enter or press Enter with this field blank to report on all level 2 values.
8 Key in your level 3 value and press Enter or press Enter with this field blank to report on all level 3 values.
9 In the Display Item Description field, key in Y for Yes or N for No and press Enter.
Order By L = Location
I = Item
If you enter L for Location, the report will be sorted in location code order. If you enter I for Item, the report will be sorted in item code order.
FIELD DESCRIPTIONS

10 In the Display Quantities field, key in Y for Yes or N for No and press Enter.
11 In the Display Count Line Text field, key in Y for Yes or N for No and press Enter.
12 In the Order By field, key in L for Location or I for Item and press Enter.
13 Key in your printer code and click Ok.

### Cycle Count Ticket List (CYTL) <a id="cycle-count-ticket-list-cytl"></a>

This report shows all your cycle count tickets in ticket number order. It is essentially a printout of the information in CYET (Enter Cycle Count Tickets). You can restrict this listing to tickets for which you entered a non-zero count.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count. 

1 Enter CYTL.

2 Key in your cycle count number and press Enter.
Include Zero Quantity and Non-Entered Tickets
N = No
Y = Yes
If you specify No, the following tickets will be excluded from the report:
 tickets for which you entered a zero count 
 tickets that you did not enter
If you specify Yes, the above tickets will be included in the report.
From Ticket Number Mandatory
Your starting ticket number.
To Ticket Number Mandatory
Your ending ticket number.
FIELD DESCRIPTIONS

3 In the Include Zero Quantity and Non-Entered Tickets, key in Y for Yes or N for No and press Enter.
4 If required, enter a starting and/or ending ticket number and press Enter.
5 Key in your printer code and click Ok.

### Cycle Count Ticket Report (CYTR) <a id="cycle-count-ticket-report-cytr"></a>

This report shows all your cycle count tickets in item code order as well as subtotals for each inventory level and each item.
FIELD DESCRIPTIONS
Cycle Count Number Mandatory
The number of the cycle count. 
Item Code Only available for item counts
If you enter an item code in this field, the report will be restricted to that item. If you leave this field blank, the report will show all items for the customer(s) 
whose inventory you are counting.

1 Enter CYTR.

2 Key in your cycle count number and press Enter.
3 Do one of the following:
4 Key in your printer code and click Ok.
Location Code Only available for location counts
If you enter a location code in this field, the report will be restricted to that location. If you leave this field blank, the report will show all locations for the customer(s) whose inventory you are counting.
If you are performing an item count:
If you are performing a location count:
a) Key in your item code and press 
Enter or press Enter with the field blank to generate a report including all items.
a) Key in your location code and press Enter or press Enter with the field blank to generate a report including all locations.
FIELD DESCRIPTIONS

### Cycle Count by Profile Code (CYPC) <a id="cycle-count-by-profile-code-cypc"></a>

For cycle count profile codes whose type has been set to location, this report shows all locations attached to the profile code. For cycle count profile codes whose type has been set to item, this report shows all items attached to the profile code. For each item or location on the report, CYPC shows two values: the number of times and the count number.
The number of times is the number of times that the item or location has been counted in the current cycle count period (not available for arbitrary counts). The count number is the last or current cycle count for the item or location.
1 Enter CYPC.
FIELD DESCRIPTIONS
Cycle Count Profile Code Mandatory
The cycle count profile code that you wish to report on. 
ABC Warehousing Inc. Page 1 of 1
Cycle Count Profile Code (CYPC) 04.18.08 13:13
--------------------------------------------------------------------------------
Profile Code : W2
Customer : D Customer D - Reserve Logic
 Item Description #Times Count#
 -------------------- ----------------------------------- ------- -------
 D1 Item D1 2 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 2 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D1 Item D1 1 142
 D2 Item D2 2
 D3 Item D3 0

2 Key in your cycle count profile code and press Enter. If you do not enter a cycle count profile code, CYPC will report on all cycle count profile codes.
3 Key in your printer code and click Ok.

### Cycle Count Report (CYCR) <a id="cycle-count-report-cycr"></a>

This report is a worksheet for use in manual cycle counting. You enter your counts on the report itself and compare your counts to the system counts manually. In manual cycle counting, there is no setup in either 
CYCP (Cycle Count Profile) or CYEN (Create Cycle Count) and no tickets are generated. You can restrict 
CYCR by customer, alternate reporting type, warehouse, a range of locations, item and level 2 value. As well, you can specify whether or not to include on-hand quantities.

FIELD DESCRIPTIONS
Customer Code Optional
The customer that you wish to report on. If you leave this field blank, the report will include all customers.
Alternate Reporting Type 
Code (defined in ITAS)
Optional
The alternate reporting type code that you wish to report on. If you leave this field blank, the report will include all items regardless of alternate reporting type code. 
Alternate Reporting Code (defined in ITAS)
Only available if you enter an alternate reporting type code.
The alternate reporting code that you wish to report on. If you leave this field blank, the report will include all items regardless of alternate reporting code.
Seed Database Alternate Reporting Type : Location From : Page 1 of 1
Cycle Count Report (CYCR) Alternate Reporting Code : Location To : 06.12.09 11:02
------------------------------------------------------------------------------------------------------------------------------------
Customer : RF008 RF Non Directed 4Lev Seq
Warehouse Code : 01
Location Hold Item Lot Date Weight WM Date On Hand Quantity Count
 Pallet ID
------------ ---- -------------------- -------------------- --------------- ------------- ---- --------- -------------------- ------
A002B IT001 AA9876 012345678901234 0 LBS 04.24.09 0 .....
A002B IT001 AA9876 0839 0 LBS 03.26.09 0 .....
BL01A IT001 AA9876 0839 0 LBS 03.26.09 0 .....
C001Z IT001 AA9876 0839 0 LBS 03.26.09 0 .....
DK001 IT001 AA9876 0839 0 LBS 06.11.09 0 .....
S100G IT001 AA9876 0839 0 LBS 05.04.09 0 .....
 ------------- --------------------
 Warehouse Total : 0 0
 ------------- --------------------
 Customer Total : 0 0
 ------------- --------------------
 Report Total : 0 0

Warehouse Code Optional
The warehouse that you wish to report on. If you leave this field blank, the report will include all warehouses subject to your customer restrictions.
From Location Code Optional
If you wish to report on a range of locations, enter your starting location in this field. If you leave this field blank, the report will include all locations for the warehouse or warehouses that you specified.
To Location Code Optional
If you wish to report on a range of locations, enter your ending location in this field.
Display Old Locations for 
Item
Y = Yes
N = No
If you enter Y for Yes, the report will include locations that once held product for the customer that you specify but currently contain no product for that customer. If you enter N for No, the report will be limited to locations with an onhand quantity greater than 0 for the customer that you specify.
Item Code Optional
The item that you wish to report on. If you leave this field blank, the report will include all items for the customer or customers that you specified.
Order By L = Location
I = Item Code
O = Only Location
If you select L for Location, the report output will be in location order. If you select I for Item, the report output will be in item order. If you select O for Only by Location, the report output will be in location order and the following will occur:
 the customer will be shown for each line with no break by customer
 if you selected the Weight option in the Display Allocated/ Weight/None field, the customer and level 4 are shown in the first line and the weight is shown in the second line
FIELD DESCRIPTIONS

Display Only Level 1 and 
Description
Y = Yes
N = No
If you select Y for Yes, only the item code and item description will print. If you select N for No, you can print level 2 and level 3 information for the item as well.
Print Item Description Only available if you set Show Item Only to N for No.
Y = Yes
N = No
If you select Y for Yes, the item code and item description will print. If you select N for No, the item code only will print. 
Level 2 Optional
The level 2 value that you wish to report on. 
Extended Level 3 Values Y = Yes
N = No
If you select Y for Yes, the report will print up to 20 characters of any level 3 value. If you select N for No, extended mode will be deactivated and only the first 15 characters of any level 3 value will be printed.
Display On-Hand QuantitiesY = Yes
N = No
If you select Y for Yes, the report will show on-hand quantities for each location plus totals by warehouse, customer and report. If you select N for No, no on-hand quantities or totals will be shown.
Display Quantity in Lowest / Highest SKUOnly available if the Display On-Hand Quantities flag is set to Y for Yes
L = Lowest
H = Highest
If you enter L for Lowest, quantities will be shown in the lowest SKU. If you enter H for Highest, the quantities will be shown in mixed SKU. 
FIELD DESCRIPTIONS

1 Enter CYCR.
Display Allocated / 
Weight / None
A = Allocated
W = Weight
N = None
If you specify A for Allocated, the system will display for each location included in CYCR the quantity of product that is on order. If you specify W for Weight, the system will display for each location included in CYCR the weight of product that is on hand. If you specify N for None, neither the on-order quantity nor the on-hand weight will be displayed in the report.
Display Weight in Lbs / 
Kilos
L = Pounds
K = Kilos
If you select L for pounds, all weights will be shown in pounds. If you select K for Kilos, all weights will be shown in kilos. 
Single / Double Space 
Output
S = Single
D = Double
If you select S for Single, the report will be single spaced. If you select D for 
Double, the report will be double spaced. 
FIELD DESCRIPTIONS

2 If required, key in your customer code and press Enter or press Enter with this field blank to report on all customers.
3 If required, key in your alternate reporting type codes in the Alternate Reporting Type Code and Alternate 
Reporting Code fields and press Enter or press Enter with this field blank to report on all customers.
4 If required, key in your warehouse code in the Warehouse Code field and press Enter or press Enter with this field blank to report on all warehouses.
5 If required, key in your starting and ending location codes in the From Location Code and To Location 
Code fields and press Enter or press Enter with these fields blank to report on all locations.
6 In the Include Empty Locations field, key in Y for Yes or N for No and press Enter.
7 If required, key in your item code in the Item Code field and press Enter or press Enter with this field blank to report on all items.
8 In the Order By field, key in L for Location, I for Item or O for Only by Location.
9 If prompted to do so, key in Y for Yes or N for No in the Display Only Level 1 and Description field and press Enter.
10 If prompted to do so, use your pick list to select your code to select the appropriate level 2 value. If you do not enter a level 2 value, the report will include all level 2 values for the item or items that you specify.
11 In the Extended Level 3 Values field, key in Y for Yes or N for No and press Enter.
12 In the Display On-Hand Quantities field, key in Y for Yes or N for No and press Enter.
13 If prompted to do so, key in L for Lowest or H for Highest in the Display Quantity in Lowest / Highest SKU field and press Enter.
14 In the Display Allocated /Weight/None field, key in A for Allocated, W for Weight or N for None and press 
Enter.

15 In the Display Weight in Lbs / Kilos field, key in L for Pounds or K for Kilos and press Enter.
16 In the Single / Double Space Output field, key in S for Single Spaced or D for Double Spaced and press 
Enter.
17 When the Printer Code block is displayed, key in your printer code and click Ok to generate the report and send it to the printer.

### Closed Cycle Count Detail Report (CYCD) <a id="closed-cycle-count-detail-report-cycd"></a>

This report shows your variances for closed cycle counts. If you count by item, your variances will be based on either quantity or value depending on your setup in CYCP. If you count by location, all variances will be based on quantity only. The sort order of CYCD is customer code, cycle count number and item code or location code. Subtotals are produced for each customer and report totals are produced for each report.
If you track variances by an item’s value, CYCD will show two values for each item: the net value and the gross value. The net value is the difference between the cycle count value and the book value; that is, the cycle count quantity - the book quantity X the item’s value. A negative number indicates that the cycle count quantity was less than the book quantity. A positive number indicates that the cycle count quantity was greater than the book quantity. The gross value is the absolute value of the net value; for example, if the net value is -100, the gross value will be 100. 
You can restrict CYCD to a specific cycle count or you can report on multiple cycle counts falling within a given date range.
ABC Warehousing Inc. From : 04.18.05 Page 1 of 1
Closed Cycle Count Detail Report (CYCD) To : 04.18.08 04.18.08 13:22
------------------------------------------------------------------------------------------------------------------------------------
 Customer: D Customer D - Reserve Logic
 CYCLE COUNT----- Prof SKU Book Count V----A----R----I-----A----N----C----E Gross
 Item Description Number Date Code A/S Unit Cost Code Qty. Qty. Qty. Net Value Gross Value Accuracy
 ------------ ----------- ---------------- ---- --- ----------- ---- ------- ------- ------------------------------------- --------
 D1 Item D1 133 11-NOV-05 W1 S .00 CASE 1265 1725 460 .00 .00 73.33%
 D2 Item D2 133 11-NOV-05 W1 S .00 CASE 200 200 0 .00 .00 100.00%
 D1 Item D1 137 14-NOV-05 W1 S .00 CASE 1065 765 -300 .00 .00 71.83%
 D2 Item D2 137 14-NOV-05 W1 S .00 CASE 200 200 0 .00 .00 100.00%
 D1 Item D1 139 26-JAN-07 W2 S .00 CASE 586 910 324 .00 .00 64.40%
 ------------ ------- ------- ------- -------------- --------------
 5 Sub-Total 3316 3800 484 .00 .00 87.26%
====================================================================================================================================
 Report Totals : Total Count : 5 Total Count Value : .00 Total Net Variance : .00
 Total Misses : 3 Total Book Value : .00 Total Gross Variance : .00
 Total Hits : 2 Hit Accuracy % : .40
 Profile Totals :
 Profile W1 Weekly Cycle Count : 4
 Profile W2 Weekly Cycle Count : 1

1 Enter CYCD.
FIELD DESCRIPTIONS
Item or Location I = Item
L = Location
Select I if you wish to report on an item count or L if you wish to report on a location count.
Display Full Description N = No
Y = Yes
If you select Y for Yes, the report will print two lines for each item/location and the second line will show the full item or location description. If you select N for 
No, the report will print one line for each item/location and the location or item description will be limited to 11 characters.
Cycle Count Start / End 
Date
Optional
Only cycle counts with a transaction date falling within this date range will be reported on. The transaction date of a cycle count is the date that the cycle count was created in CYEN. This date may be very different from the scheduled cycle count date displayed in CYEN.
Close Cycle Count Number
Optional
The closed cycle count that you wish to report on. If you specify a particular cycle count, the transaction date of this cycle count must fall within the range that you define in the Cycle Count Start Date and Cycle Count End Date fields. 

2 In the Item or Location field, key in I for Item or L for Location and press Enter.
3 In the Display Full Description field, key in Y for Yes or N for No and press Enter.
4 Select your cycle count start and dates from the pop-up calendars.
5 If required, key in a cycle count number and press Enter.
6 When the Printer Code block is displayed, key in your printer code and click Ok to generate the report and send it to the printer.

A
A/B Cycle Count field (CYEN) 26 active cycle counts 30
Actual Item/Locations to Count field (CYEN) 31 adjusting the number of cycle counts 78
ADNC (Adjust Number of Cycle Counts) 75, 78
Allow Duplicates per Location field in CYEN 28 arbitrary counts, creating 38
Arbitrary/Scheduled field (CYEN) 27
ATMP (Action Template Setup) 20
B blank tickets entering 57 generating 47 blank versus non-blank tickets 3 blind counts, entering 52 blind versus non-blind counts 3 cancelling a cycle count 42 closing a cycle count 70
Count field (CYET) 52
Count on Day field (CYCP) 11 counted versus not counted inventory in CYBK 87
Current Count Number field (ADNC) 79
Current Period Start/End Date fields (CYCP) 10
Customer Code field (ADNC) 79
Customer Code field (CYEN) 32
CYAB (Cycle Count Ticket Discrepancy) 67
CYBK (Cycle Count Book Report) 86
CYCC (Cancel Cycle Count) 42
CYCD (Closed Cycle Count Detail Report) 107 cycle count profile code (CYCP), attaching to item or location 17
Cycle Count Profile Code field (ADNC) 79
Cycle Count Type field (CYCP) 11
CYCO (Close Cycle Count) 70
CYCP (Cycle Count Profile) 10
CYCR (Cycle Count Report) 101
CYDE (Delete Cycle Count) 44
CYEN (Create Cycle Count) 26
CYET (Enter Cycle Count Tickets) 50
CYFO (Force Cycle Count Balance) 76
CYGT (Generate Cycle Count Tickets) 46
CYPC (Cycle Count by Profile Code) 100
CYSR (Cycle Count Summary Report) 91
CYTI (Print Cycle Count Tickets) 48
CYTL (Cycle Count Ticket List) 96
CYTR (Cycle Count Ticket Report) 98
CYUP (Cycle Count Update Inventory) 81
D
Date Profile Code field (CYCP) 12 deleting a cycle count 43
Display Variances Only field (CYBK) 89
DOCU (Documents) 21
Document Code field in CYEN 27 dual counts, specifying 26 duplicates, allowing 28
E
Ending Ticket field (CYET) 51
Enter Cycle Count Tickets (CYET) 50 event-driven cycle counts entering in RFCYE 63 setting up 17
F forcing a count to balance 76
Frequency Code field (CYCP) 13
Frequency Value field (CYCP) 13
H
Hold field (CYET) 52
