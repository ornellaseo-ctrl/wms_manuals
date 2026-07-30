---
title: "Configuração — Itens e Perfis de Item"
description: "Cadastro de item (ITEM), SKUs, perfis de manuseio, hold, storage e quantity breakdown."
layout: default
---

# Configuração — Itens e Perfis de Item

Cadastro de item (ITEM), SKUs, perfis de manuseio, hold, storage e quantity breakdown.

**Fluxo principal:** `ITEM -> SKUS -> DITP/IHAP/IHOP/IQBP (perfis)`

> Fonte: manuais N do AccellosOne Enterprise 3PL / Körber Supply Chain WMS.

## Item Profile Setup <a id="item-profile-setup"></a>

*Manual N — Setup Guide*

### Item Information Profile (IINP) <a id="item-information-profile-iinp"></a>

OVERVIEW
In this program, you define your deferred handling percentages. That is, you wish to split your handling revenue into two portions: one portion that is earned when the product is received and another portion that is earned when the product is shipped. Because IINP is a mandatory profile in ITEM, you must create a profile in IINP even if you do not track deferred handling.
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
General Information Item 
Profile Code
Mandatory
Your general information profile code. For example, LBS or KILOS.
Description Mandatory
Your general information profile code description
Deferred Handling 
Inbound Percentage
Mandatory
Set the percentage to 100. For further information on deferred handling, refer to the Standard Reports Guide.
Deferred Handling Outbound PercentageMandatory
Set the percentage to 0.
Calculate Turns Reserved for future use
Calculate Tonnage Reserved for future use

PROCEDURE
1 Enter IINP.
2 Click on Enter Criteria) then Execute Query to see whether the profile that you wish to use has already been set up. If no profile has been set up, click on Create Record.

Item Information Profile
3 In the General Information Item Profile Code field, key in the appropriate code (LBS, KGS, TONS, etc.) 
and press Enter.
4 Key in your description (for example, Standard) and press Enter.
5 In the Deferred Handling Inbound Percentage field, key in 100 and press Enter.
6 In the Record Weight Measure Code field, use your pick list to select the any unit of measure. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
7 In the Record Cube Measure Code field, use your pick list to select the any unit of measure.
Record Weight Measure 
Code
Reserved for future use
Record Cube Measure 
Code
Reserved for future use
Part of Assembly Reserved for future use
Ship Alone Reserved for future use
FIELD DESCRIPTIONS

8 Click on Return to Main and then Exit to exit the program.

### Item Initial Storage Profile (IISP) <a id="item-initial-storage-profile-iisp"></a>

OVERVIEW
In this program, you set up your item initial storage profile(s). The item initial storage profile defines the onetime charges incurred for an item when that item is first received into the warehouse. This profile can be attached to a particular location billing code (for example, one charge for all locations assigned a location billing code of DRY, another charge for all locations assigned a location billing code of COOL, etc.) if you want to set up different charges for initial storage based on location. Alternatively, you can set up one profile that applies to all locations. 
You can also define special discounts on initial storage for product received a specified number of days before the end or after the beginning of your billing period. If you are not using the discount function, you can prorate initial storage based on the number of days that the product has been in your warehouse. 
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not charge for initial storage. 
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
NOTE You cannot use discounts or prorating for open lots. If you process open lots and wish to offer discounts or prorating on non-open lots, you must set up two profiles in IISP: one for open lots and another for non-open lots.
FIELD DESCRIPTIONS
Initial Storage Profile 
Code
Mandatory
Your initial storage profile code. For example, F1 for Freezer Group 1.

Description Mandatory
Your initial storage profile code description
Location Bill Code (LODE)
Mandatory
The location billing code for this profile. If you have the same initial storage rates regardless of location billing code, use .ALL (not ALL without the preceding dot).
If you intend to store the same item in two different locations with two different location billing codes (for example, a product like chocolate that could be either a freezer item or a cooler item depending on its temperature when it was received), you can assign the same initial storage profile two or more location billing codes. This allows you to charge initial storage based on the location billing code. 
For example, if you receive a shipment of chocolate and place half the receipt in your freezer and the other half in your cooler, the freezer portion of the receipt will be charged freezer rates and the cooler portion of the receipt will be charged cooler rates.
TIP You can use the .ALL code to indicate “all other location billing codes.” 
For example, if you assign charge code 1 to your .ALL code and charge code 
2 to your DRY1 location billing code, all location billing codes except DRY1 will be charged the rates defined for charge code 1.
Charge Code (CHAR) Mandatory
The charge code for your initial storage. Make sure that the SKU code that the charge code is based on does not have a value of OCCURRENCE in the 
Qualifier Code field in SKUS (Stock Keeping Units).
FIELD DESCRIPTIONS

Discount Day Optional
Defines the number of days in the billing period that the discount period applies to. If you enter a positive number, you count forward from the day after the day that you specify to the end of the billing period or to the next discount day — whichever comes first. For example, if you enter 15, the discount period will start on the 16th (the day after the day that you specify).
If you enter a negative number (for example, -3), you count backwards from the last day of the billing period to the day that you specify in order to define the discount period.
The billing period in AccellosOne 3PL is determined as follows. If you set up a date profile in DAPR, your billing periods will be determined by the starting dates that you enter in that program. If you do not set up a date profile in 
DAPR, your billing periods will be based on the calendar month in which the receipt was confirmed. For example, if your receipt is confirmed in August, your billing period is Aug. 1 to Aug. 31. If your receipt is confirmed in February, your billing period is Feb. 1 to Feb. 28.
Discount Percentage Optional
The percentage discount that applies to the discount period.
Prorate If you use prorating, you cannot set up discount days and discount percentages
Y = Yes
N = No
If you set this flag to Yes, AccellosOne 3PL will charge initial storage for only the portion of the billing period that the goods are in the warehouse. For example, if your billing period is 30 days and you receive on the 15th day (that is, midway through the period), the prorate function will charge for half the period only.
See the Discount Day field for further information on how the billing period is calculated by AccellosOne 3PL.
FIELD DESCRIPTIONS

EXAMPLES OF DISCOUNT DAYS
PROCEDURE
1 Enter IISP.
2 Click on Enter Criteria then Execute Query to see whether the profile that you wish to use has already been set up. If no profile has been set up, click on Create Record.
3 Key in your initial storage profile code and press Enter.
4 Key in a description for your initial storage profile code and press Enter.
5 If your profile applies to all locations, key in .ALL and press Enter. If your profile is location specific, use your pick list to select the appropriate location bill code. To select a code using a pick list, press F10 to 
Example 1 — split month billing
Discount Day Percentage Meaning
16 50 If product is received during first 16 days of the billing period, full initial storage charges apply. If product is received from the 17th day of the billing period to the last day of the billing period, there is a 50% discount off initial storage charges. 
Example 2
Discount Day Percentage Meaning
-3 60 60% off initial storage for product received during the last three days of 
the billing period. 
Example 3
Discount Day Percentage Meaning
0 0 No discount days.
Example 4
Discount Day Percentage Meaning
15 50 50% off initial storage on product received from the 16th day of the billing period to the third day before the end of the period.
-2 30 30% discount on product received during the last two days of the billing period.

display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
6 In the Charge Code field, key in your charge code and press Enter or use your pick list to select the appropriate charge code. If there is no charge for initial storage, select your NC charge code and click on 
Return to Main to exit create mode. Then click on Master Block and Exit to exit.
7 Key in the number of the discount day and press Enter or key in 0 and press Enter to bypass this field. 
8 Key in the discount percentage and press Enter or key in 0 and press Enter to bypass this field.
9 If you are setting up prorating, key in Y for Yes in the Prorate field and press Enter.
10 If required, repeat steps 7 to 9 to define another discount period and percentage in the Discount Block.
11 When you finish defining your discount period and percentage, click on Return to Main to exit create mode.

Item Initial Storage Profile showing discount days
12 Click on Master Block and Exit to exit the program.
Item Initial Storage Profile
If you wish to set up discount days or prorating:
If you do NOT wish to set up discount days or prorating:
a) Click on Return to Main to redisplay the Location Billing Block.
b) Click on Discount Block.
a) Click on Return to Main to exit create mode. Then click on Master Block and Exit to exit.

### Item Renewal Storage Profile (IRSP) <a id="item-renewal-storage-profile-irsp"></a>

OVERVIEW
In this program, you set up your renewal storage profile(s). Renewal storage is any recurring storage charge that is charged after initial storage. Renewal storage is normally charged for as long as the product remains in the warehouse.
IRSP supports the following types of renewal billing:
▪ Anniversary — Monthly
▪ Anniversary — Weekly 
▪ Daily
▪ Monthly — First of Month 
▪ Monthly — Last of Month 
▪ Weekly as of Monday
If you renew on a special day of each month that the above billing types cannot accommodate (for example, every 30 days, every second week, the 14th of each month, etc.), you must set up your start dates in DAPR (Date Profile).
EXAMPLE 1 — FIRST OF MONTH BILLING
Product gets renewed the first of the month regardless of the day it was originally received.
PERIOD 1
Inbounds: 1,000 cases received on 18th
Outbounds: 700 cases (25th)
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: Any changes to renewal storage take effect at the end of the frequency period. For example, if you change your frequency from anniversary monthly to anniversary weekly, the change will take place at the end of the current month.
OTHER REQUIREMENTS:
18 25 01 01
+1000 CS -700 CS
$ initial storage renewal storage
= 300 CS

Balance: 300 cases (1st)
You receive 1,000 cases of new product on the 18th of the month and your initial storage charge is based on this amount. On the 25th of the month, you ship out 700 cases. On the first of the following month, you have a balance of 300 cases and renewal storage is charged on this quantity.
EXAMPLE 2 — ANNIVERSARY MONTHLY BILLING
Product gets renewed each month on the day it was originally received.
In this type of billing, the initial storage period is zero. You receive 1,000 cases of new product on the 18th of the month and your renewal storage for the first month is based on this amount. On the 25th of the month, you ship out 700 cases. On the 18th of the following month, you have a balance of 300 cases and renewal storage is charged on this quantity.
A profile can consist of a single type of renewal billing or multiple types. If you set up multiple types, you define a period for each renewal whose billing frequency you wish to change. For example, period one could be anniversary monthly, period two could be daily, period three could be weekly as of Monday, etc. For each period that you define, you can set up different charges and rates if required.
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not charge for renewal storage or do not use AccellosOne 3PL to generate invoices or gather billing information. 
Set up a No Charge profile as follows:
Period Number = 1
Frequency Code = any frequency (daily, anniversary monthly, etc.)
Cycle = 1
Reset Date = N
Location Bill Code = .ALL
Charge Code = NC (No charge)
PERIOD 1
Inbounds: 1,000 cases received on 18th
Outbounds: 700 cases (25th)
Balance: 300 cases (1st)
PERIOD 2
Initial balance: 300 cases
Inbounds: 200 cases received on 20th
Balance: 500 cases
NOTE If you receive product on the 31st of a month, product will renew on the last day of the following month if that month does not have 31 days. For example, product received on Jan. 31 will renew on Feb. 28 or 29, March 31, April 30, etc.
18 25 18 18
+1000 CS -700 CS
$ renewal storage renewal storage
= 300 CS
+200 CS

FIELD DESRIPTIONS
FIELD DESCRIPTIONS
Renewal Storage Profile 
Code
Mandatory
Your renewal storage profile code. For example, 35A for 35-40 lb. Anniversary 
Monthly.
Description Mandatory
Your renewal storage profile code description
Period Number Mandatory
You need to set up a separate period for each time your type of billing changes.
Frequency Code AM = Anniversary — Monthly product is renewed each month on the day it was originally received
AW = Anniversary — Weekly product is renewed each week on the day it was originally received
D = Daily product is renewed each day 
MF = Monthly — 1st of Month product is renewed the first of the month regardless of which day it was originally received
ML = Monthly — Last of Month product is renewed the last of the month regardless of which day it was originally received
W = Weekly as of Monday product is renewed every Monday regardless of which day it was originally received

Cycle Mandatory
The number of times the type of billing specified in the Frequency Code field will occur in the current period before AccellosOne 3PL switches to the next period, if any. 
If there is only a single period, the cycle will repeat itself for as long as there is product in the warehouse.
EXAMPLES
Period
Frequency
Anniversary Monthly
Cycle
Product gets renewed each month on the day it was originally received for as long as there is product in the warehouse.
Period
Frequency
Daily
Cycle
Product gets renewed daily from the beginning of the renewal storage period for as long as there is product in the warehouse.
Period
Frequency
Daily
Anniversary Monthly
Cycle
There are two periods in this renewal storage profile. Period 1 lasts seven days starting from the beginning of the renewal storage period. In period 2, product gets renewed each month on the day it was originally received for as long as there is product in the warehouse.
Reset Date Y = Yes
N = No
This flag allows you to reset the original receipt date when you switch from one billing frequency to another. For example, you offer X number of days of free storage and then charge renewal storage based on either the original receipt date or the date that the free storage ended.
EXAMPLE 1
Period
Frequency
Daily
Anniversary Monthly
Cycle
Reset Date
Y
N
FIELD DESCRIPTIONS

If product is received on Feb. 02, the first renewal date will be Feb. 12. At that time, the original receipt date will be reset to Feb. 12. Then the next renewal date will be Mar. 12 based on the new reset date followed by Apr 12, May 12 and so on.
EXAMPLE 2
Period
Frequency
Daily
Anniversary Monthly
Cycle
Reset Date
N
N
If product is received on Feb. 02, the first renewal date will be Feb. 12 and the original receipt date will remain Feb. 02. The next renewal date will be Mar. 02 followed by Apr 02, May 02 and so on.
Location Bill Code (defined in LODE)
Mandatory
The location billing code for the period specified in the Period Number field. If you have the same renewal storage rates for all your locations, use .ALL (not 
ALL without the preceding dot).
If the same item can be stored in two or more locations with different location billing codes and hence different rates (for example, a product like lumber that could be stored either outside in a yard or inside in the warehouse), you must assign multiple location billing codes to the same renewal storage profile. This will allow you to charge different renewal storage rates based on the area in which the product is stored. 
For example, if you receive a shipment of lumber and place half the receipt in your yard and the other half in your warehouse, the yard portion of the receipt will be charged yard rates and the warehouse portion of the receipt will be charged warehouse rates.
TIP You can use the .ALL code to indicate “all other location billing codes.” 
For example, if you assign charge code 1 to your .ALL code and charge code 
2 to your DRY1 location billing code, all location billing codes except DRY1 will be charged the rates defined for charge code 1.
Charge Code (defined in CHAR)
Mandatory
The charge code for the period specified in the Period Number field. Make sure that the SKU code that the charge code is based on does not have a value of OCCURRENCE in the Qualifier Code field in SKUS (Stock Keeping 
Units).
FIELD DESCRIPTIONS

EXAMPLE 1
In this example, the customer’s products are renewed anniversary monthly.

Anniversary monthly billing
In the above example, AccellosOne 3PL will bill anniversary monthly using the charge code R15C. Since only a single period is defined, anniversary monthly billing will continue month after month. In other words, the period one cycle will repeat itself for as long as there is product in the warehouse.
EXAMPLE 2
In this example, there are two renewal storage periods: period 1 and period 2. Period 1 lasts seven days and is followed by period 2, which lasts as long as there is product in the warehouse. 

Two renewal storage periods

In the above example, there are two billing periods. In period 1, AccellosOne 3PL will calculate renewal storage at the end of the seven-day period using charge code NC for no charge (not shown). In period 2, 
AccellosOne 3PL will apply charge code SCS for every month thereafter. Because the Reset Date flag is set to Yes for the first billing period, AccellosOne 3PL will reset the original receipt date to the original receipt date 
+ 7 days.
PROCEDURE
1 Enter IRSP.
2 Click on Enter Criteria then Execute Query to see which renewal storage profiles have been already set up.
3 If the profile that you require has not been set up, click on Create Record.
4 Key in a code to describe the renewal storage profile and press Enter. 
5 Key in a meaningful description for the new profile and press Enter.
6 Key in 1 for your period number and press Enter.
7 Use your pick list to select the appropriate billing frequency code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
If you will be setting up special billing dates in DAPR (Date Profile) and attaching this profile to all your items, you can enter any frequency that you wish. AccellosOne 3PL will ignore the frequency specified in 
IRSP and use the DAPR dates instead. 
8 Key in your cycle number (the number of times that you want period to repeat itself before it moves to the next period) and press Enter. If you are setting up a single period, you set the Cycle field to 1.
9 Key in your reset date value (Y for Yes or N for No) and press Enter.
10 If you require renewal billing with multiple billing frequencies, enter another line for period number 2.
11 When you finish entering all your billing periods, click on Return to Main to exit create mode.
12 Position the cursor over period number 1.
13 Click on Location Bill Block.
14 Key in your location bill code for period 1 and press Enter. You can use .ALL for all locations or you can use your pick list to select the appropriate location bill code.
15 Use your pick list to select the appropriate charge code for this period.
CAUTION If you are setting up two or more billing frequencies, make sure that your cursor is positioned over the correct period number before you enter the Location Bill Block. If you position your cursor by mistake over period 2 rather than period 
1, the location bill code and the charge code will be attached to the wrong period. 

Renewal Storage profile showing anniversary monthly billing
16 If required, enter your second location billing record to the Location Bill Block.
17 When you finish entering your location billing records, click on Return to Main.

### Item Handling Profile (IHAP) <a id="item-handling-profile-ihap"></a>

If you wish to set up a second renewal billing period:
If you do NOT wish to set up a second renewal billing period:
a) Click on Create Record.
b) Repeat the above steps for your second billing period.
a) Click on Frequency Block.
b) Click on Master Block and then 
Exit to exit.
PREREQUISITES: CHAR, LODE
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory

OVERVIEW
In this program, you set up your inbound handling charges for an item. Inbound handling charges are onetime charges that are automatically applied when you confirm a receipt. 
Because this is a mandatory profile for ITEM, you must set up an NC (No Charge) profile code if you do not charge for handling or do not use AccellosOne 3PL to generate invoices or gather billing information. A no charge profile must contain a valid charge code for your inbound handling charges in order to be added to 
AccellosOne 3PL.
PROCEDURE
1 Enter IHAP.
2 Key in your handling profile code and press Enter.
3 Key in a meaningful description for your handling profile code and press Enter.
4 In the Inbound Charge Code field, use your pick list to select the appropriate charge code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select 
Code.
If you are setting up a no charge profile, use your NC charge code in this field.
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Handling Profile Code Mandatory
Your handling profile code. For example, H1 for Handling Charges 1.
Description Mandatory
Your handling profile code description
Inbound Charge Code (CHAR)
Mandatory
You charge code for inbound handling charges. If you are setting up a no charge profile, enter your NC charge code in this field. Make sure that the 
SKU code that the charge code is based on does not have a value of OCCURRENCE in the Qualifier Code field in SKUS (Stock Keeping Units). 

Item Handling Profile showing inbound handling charges
5 Click on Return to Main and then Exit to exit.

### Date Profile (DAPR) <a id="date-profile-dapr"></a>

OVERVIEW
In this program, you set up the starting dates for each renewal period. This program is only required if you have irregular billing periods such as every 25 days, the 17th of each month, the third week of each month, etc. If you bill anniversary monthly, anniversary weekly, daily, first of the month, last of the month or weekly as of Monday, you use the standard frequency codes in IRSP.
In DAPR you key in manually the starting date (month, day and year or day, month and year) of each billing period. During setup you should enter all starting dates for the current year. At the end of the current year, you will have to enter the starting dates for the following year.
PREREQUISITES: None
ATTACHED TO: IBIP (Item Billing Profile) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory only if you use AccellosOne 3PL to generate invoices or gather billing information and you have irregular billing periods
OTHER REQUIREMENTS: A list of your billing periods for the current year

PROCEDURE
1 Enter DAPR.
2 Click on Create Record.
3 Key in your date profile code and press Enter. 
4 Key in a meaningful description for your date profile and press Enter again.
5 In the Dates window, key in the starting date of your first renewal period using the correct date format and press Enter.
6 Press Enter in the Correct column to confirm the starting date and create a new blank line.
7 Repeat the above step for each starting date that you wish to enter. You should enter all dates for a minimum period of one year.
FIELD DESCRIPTIONS
Date Profile Code Mandatory
Your date profile code.
Description Mandatory
Your date profile code description
Starting Date Mandatory
Your starting date for each renewal period. The format of this date must match the date format in COMP (Company Code).
CAUTION Your first starting date should always be one month or billing period back from the current date. For example, if you bill on the 15th of each month and are performing your setup on July 12, 2013, your first starting date should be June 15, 
2013. If you were to make July 15 your first starting date, you would be unable to bill for items renewing before this date.

Date Profile for late 08 and the first two quarters of 2009
8 When you finish entering all your dates, click on Return to Main to exit create mode. Then click on Master 
Block and Exit to exit.

### Item Billing Profile (IBIP) <a id="item-billing-profile-ibip"></a>

OVERVIEW
In this program, you attach your various billing-related profiles (IISP, IRSP, IHAP, etc.) to a new profile called 
IBIP. You then attach IBIP to your items in ITEM. You use IBIP to set up item-related billing only (for example, a minimum initial storage charge that applies to a particular item). If you wish to set up minimum charges that apply to an entire receipt — that is, all items from one customer — you do so in DILP (Depositor Inventory 
Level Profile).
PREREQUISITES: IISP, IRSP, IHAP, CHAR, DAPR
ATTACHED TO: ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

IBIP also allows you to set up “local overrides” for your billing entity minimum charge, renewal storage line minimum charge, initial storage minimum charge and handling minimum charge. A local override is a profile for a single item or a group of items whose billing entity minimum charge, renewal storage line minimum charge, etc. replaces the customer-wide defaults set up in DILP (Depositor Inventory Level Profile).
IBIP profiles can be customer specific or can apply to all customers. If you charge special rates for certain items, you will have to set up multiple item billing profiles for those items. If you do not use AccellosOne 3PL to generate invoices or gather billing information, set up one billing profile called NA (Not Applicable).
FIELD DESCRIPTIONS
Item Billing Profile Code Mandatory
Your item billing profile code. For example, CAS1 for Billing on Cases 1. The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used in an item billing profile.
Description Mandatory
Your item billing profile code description
Initial Storage Profile 
Code (IISP)
Mandatory
The initial storage profile for the items to which this profile is attached.
Renewal Storage Profile 
Code (IRSP)
Mandatory
The renewal storage profile for the items to which this profile is attached.
Handling Profile Code (IHAP)
Mandatory
The handling storage profile for the items to which this profile is attached.
Date Profile Code (DAPR)
Optional
If required, the date profile for the items to which this profile is attached. 

Billing Entity Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Renewal Storage Line 
Minimum Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Initial Storage Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Handling Minimum 
Charge Code (CHAR)
Optional
See Billing and Invoicing Guide.
Create Renewal Invoice at Zero Inventory
This field is an override at the item level of the customer level default established in DBIP. See the Billing and Invoicing Guide.
Original / Current Rate on 
Renewals
C = Current
I = Initial Original
R = Renewal Original
See the field of the same name in Depositor Billing Profile (DBIP). If you enter a value in this field, it will override the customer-level default in DBIP for the items attached to this profile.
Number of Days Between 
Renewal Invoices
This field is an override at the item level of the customer level default established in DBIP. See the Billing and Invoicing Guide.
Rate Qualifier O = Original
B = Balance
See the field of the same name in Depositor Billing Profile (DBIP). If you enter a value in this field, it will override the customer-level default in DBIP for the items attached to this profile.
Invoice Type for AutoProcessingFor custom use only.
Reserve Quantity See Billing and Invoicing Guide.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter IBIP.
2 Click on Enter Criteria then Execute Query to view the item billing profiles that have been already set up.
3 If you need to set up a new item billing profile, click on Create Record.
4 Key in an item billing profile code and press Enter. 
5 Key in a meaningful description for your item billing profile and press Enter again.
6 Use your pick list to select the appropriate profile code for initial storage. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
7 Use your pick list to select the appropriate profile code for renewal storage.
Renewal Summarization 
Code
See Billing and Invoicing Guide.
Ignore Multiple Location 
Bill Codes for Same Billing Entity
Y = Yes
N = No
If the same billing entity is stored in multiple locations with multiple location billing codes, you can bill on a single location bill code or all location billing codes. 
If you set this field to Yes, the billing engine will select the location billing code with the largest quantity to be billed and ignore the other location billing codes. 
If you set this field to No, the billing engine will bill on all location billing codes.
Split Invoice by Alternate 
Reporting Code
N = No
Y = Yes
If you set this field to Yes, you can split invoices based on alternate reporting type and alternate reporting code. If the type and code that you enter in the 
Alternate Reporting Type and Alternate Reporting Code fields in IBIP matches the type and code attached to items in ITEM, AccellosOne 3PL will generate a separate invoice for each alternate reporting type. 
Alternate Reporting Type (ITAS)
Only available if Split Invoice by Alternate Reporting Type Code = Yes
Your alternate reporting type.
Alternate Reporting Code (ITAS)
Only available if Split Invoice by Alternate Reporting Type Code = Yes
Your alternate reporting code.
FIELD DESCRIPTIONS

8 Use your pick list to select the appropriate profile code for handling charges.
9 If required, use your pick list to select the appropriate date profile code.
10 If required, use your pick list to select the appropriate charge codes for the following:
▪ billing entity minimum 
▪ renewal storage minimum
▪ initial storage minimum 
▪ handling charge minimum
If you do not require minimums for these charges or the customer-wide defaults set up in DILP apply to all items, press Enter to bypass these fields.
11 If required, key in the appropriate value (C for Current, I for Initial Original or R for Renewal Original) in the Original /Current Rate on Renewals field and press Enter. If prompted to do so, key in your rate qualifier (O for Original or B for Balance) and press Enter.
12 Press Enter to bypass the remaining fields in IBIP.
13 When you finish setting up your item billing profile, click on Return to Main.

Item Billing Profile with no local overrides for minimum charges
14 Click on Exit to exit.

### Item Shipping Profile (ITSH) <a id="item-shipping-profile-itsh"></a>

OVERVIEW
ITSH serves three main functions. It allows you to:
▪ specify your back order options at the item level (refer to the Operations 2 Guide for further information on back orders)
▪ generate expiry dates and assign them to inbound product
▪ activate allocation by weight for outbound product
ITSH is a mandatory profile for ITEM. If you do not need to use the above options, you must set up a single 
NA (Not Applicable) profile and set the Enter Expiry Dates field to No. If you intend to use one or more of the above options, you may have to set up multiple profiles; for example, one profile with the allocation by weight option switched on and another profile with the allocation by weight option switched off.
EXPIRY DATES
Expiry dates serve two functions in AccellosOne 3PL. You can use them to identify product that will expire as of a specified cut-off date in reports such as EXRE (Aging by Expy/Rcvd. Report). As well, you can specify expiry dates as the basis of your FIFO/LIFO selection when you set up directed picking in PIPR (Picking 
Profile). There are four different options for recording expiry dates for inbound product: 
▪ you can use the receipt date as your expiry or production date
▪ you can enter your expiry dates manually in ENRE or RFCH
▪ your customer supplies expiry dates in a regular date format (MMDDYY, DDYYMM or YYMMDD) or in an encoded production date or date code format
PREREQUISITES: DILP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
CHANGE STATUS: If you change the shelf life duration and/or frequency, the change affects new inventory only. If you wish to change existing inventory as well, you must run REEX (Reset Inventory Expiry Date).
OTHER REQUIREMENTS: If you are converting an inventory level into an expiry date, you will require a formula

▪ your customer supplies an encoded production date or date code and from this date you wish to calculate an expiry date
FORMULA 
REQUIRED
INVENTORY LEVEL 
REQUIRED ITSH SETUP you do not use expiry dates None No inventory level required for expiry date.
Set the Enter Expiry Dates flag to 
No.
you use your receipt date or current system date as your expiry or production date
None No inventory level required for expiry date.
Set the Enter Expiry Dates flag to 
Yes and the Expiry Date Derived from field to CD (Company Date) 
and the Expiry Date Formula field to !CD.
you enter your expiry dates manually in ENRE or RFCHNone No inventory level required for expiry date.
Set the Enter Expiry Dates flag to 
Yes and bypass the Expiry Date 
Derived from field.
you enter a date or date code as an inventory level in ENRE or RFCH and wish to use this date as your expiry date
Formula required to convert code to a MMDDYY format.
Inventory level set up in DILP required for date or date code.
Set the Enter Expiry Dates flag to 
Yes and enter your inventory level and date conversion formula.
you enter a date or date code as an inventory level in ENRE or RFCH and wish to add a specified number of days or months to this date in order to arrive at your expiry date
Formula required to convert code to a MMDDYY format. 
Product’s shelf life added to this date to arrive at the expiry date.
Inventory level set up in DILP required for date or date code.
Set the Enter Expiry Dates flag to 
Yes and enter your inventory level and date conversion formula. Then enter your shelf life duration and frequency values.
FIELD DESCRIPTIONS
Item Shipping Profile 
Code
Mandatory
Your item shipping profile code. For example, EXP1 for Expiry Date 1 or NA for Not Applicable.
Description Mandatory
Your item shipping profile code description
Generate Back Orders at 
Inventory Level
See the back orders section of the Operations 2 Guide for further information on this field.
Allow Future Orders Reserved for future use

Use Substitute Item 
Codes
See the item substitution section in the Operations 2 Guide.
Dynamic Shelf Life Calculation MethodSee the allocating product by shelf life section of Allocation and Wave Manager for further information on this field.
Enter Expiry Dates N = No
Y = Yes
If you set this field to No, no expiry date will be assigned to a receipt line in 
ENRE. If you set this field to Yes, you can enter an expiry date for each receipt line in ENRE. 
Expiry Date Derived from Only available if you set the Enter Expiry Dates field to Yes
CD (Company Date)
LEV2
LEV3
LEV4
RD (Received Date)
If you are using the receipt date or current system date as your expiry date, select CD (Company Date). If your expiry dates are based on an inventory level, you must select the inventory level in this field. If you are using the receipt confirmation date in CHRF/CORL, use RD (Received Date).
NOTE If you rereceive inventory, the new inventory will have the same expiry date as the original inventory. For example, if you receive item A, lot 1, on Jan. 10 and assign it an expiry date of Jan. 30, any further inventory received for this item and lot — regardless of the date that it is received — will expire on Jan. 30.
Expiry Date Formula Only available if you select an option in the Expiry Date Derived from field
If your expiry dates are based on an inventory level that requires decoding, you enter the decoding formula in this field. This formula is normally provided by HighJump.
If you selected Company Date in the previous field, enter !CD as your expiry date formula. If you selected Received Date in the previous field, enter !RD as your expiry date formula.
FIELD DESCRIPTIONS

Expiry Date Format Only available if you select an option in the Expiry Date Derived from field
The format of your expiry dates expressed in Oracle date format (for example, 
YYDDMM, MMDDYYYY, YYDDD, etc.).
NOTE Single-digit year formats such as YDDD are not recommended.
Shelf Life Duration Only available if you select an inventory level in the Expiry Date Derived from field
If you are using production dates/date codes, you can enter a shelf life in days or months to allow AccellosOne 3PL to calculate the expiry date automatically. 
AccellosOne 3PL adds the value that you enter in this field to the production date to arrive at the expiry date.
For example, if a product was produced on July 1 and you set the shelf life to three months, the product will expire on October 1.
If you enter a negative value in this field, you can advance the expiry date to an earlier date. For example, if your customer does not want product shipped if it will expire within two months, you can enter -2 in this field to advance the expiry date. 
If you change your shelf live duration or shelf life frequency and you want the change to apply to existing inventory, you must run REEX (Reset Inventory 
Expiry Date).
Shelf Life Frequency Only available if you enter a shelf life duration
D = Days
M = Months
See Shelf Life Duration field above.
Ship by Weight D = Disallowed
G = Gross
N = Net
If you select either Gross or Net, you can allocate outbound product by weight instead of number of pieces. If you select D for Disallowed, no allocation by weight is allowed. See the section “Allocation by Weight” in Allocation and 
Wave Manager for further information on shipping by weight.
FIELD DESCRIPTIONS

Ship by Weight Rounding MethodD = Down
U = Up
If you select U for Up, allocation will ship one or more additional units of inventory to ensure that the weight to be shipped is always reached. If you select D for Down, allocation will stop allocating additional units of inventory just before the shipping weight is reached. 
For example, if each case weighs 8 lbs and you enter a ship weight of 50 lbs, allocation will ship 7 cases or 56 lbs if you round up. If you select the round down option, allocation will ship 6 cases or 48 lbs.
Automatic Hold Code for 
Expired Inventory
If you specify a hold code for expired product in this field, when inventory belonging to the item that your ITSH profile is attached to expires, AccellosOne 3PL will automatically place it on that hold code.
NOTE Hold codes for expired inventory require a cron job set up by 
HighJump.
Number of Days Identifying Stale ProductThe number of days before expiry that must be reached before a product is considered stale. When the number of days before expiry is reached, the inventory entity is automatically put on “stale” hold. If the inventory entity is still in the warehouse on the expiry date, the “stale” hold code is changed to your “expired” hold code.
NOTE Stale product holds require a cron job set up by HighJump.
Automatic Hold Code for 
Stale Product (HOLD)
The hold that you wish to use to identify stale product. 
FIELD DESCRIPTIONS

The following fields allow you to define expiry/production date rules for product received in ENRE/RFCH and positive adjustments made in ENAJ and MATR. Inbound product that violates these rules (that is, an insufficient shelf life) will be rejected as outside the acceptable date range for this product.
ENRE screen showing out of range message
If you attach the special verify program MMSO (Min/Max Expiry/Prod. Date Supervisor Over.) to your 
CORE flow in DIFP, receipt lines that failed expiry/production date validation in RFCH will display in CHRF. 
If the supervisor override option has been activated, a supervisor will be prompted to logon and authorize the violation of expiry/production date rules.
Assign by Production 
Date or Expiry Date
E = Expiry Date
P = Production Date
The date that you wish to validate.
Shelf Life Duration Reserved for future use.
Supvr. Override Min./
Max. Expiry/Production 
Date
N = No
Y = Yes
If you set this flag to Yes, a supervisor can override violations to expiry date/ production date rules in RF and at receipt confirmation. If you set this flag to 
No, there is no override for violations to expiry date/production date rules.
Minimum Expiry Date 
Days
The minimum range in days to expiry.
Maximum Expiry Date 
Days
The maximum range in days to expiry.
Maximum Production 
Date Days
The maximum range in days from the production date. A value of zero is acceptable.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter ITSH.
2 Click on Enter Criteria then Execute Query to see which item shipping profiles have already been set up.
3 If you need a new item shipping profile, click on Create Record.
4 Key in an item shipping profile code and press Enter.
5 Key in a description for your profile and press Enter.
6 If your cursor is positioned in Generate Back Orders at Inventory Level field, press Enter to bypass this option.
7 Press Enter to bypass the Allow Future Orders field.
8 In the Use Substitute Item Codes field, key in N for No and press Enter.
9 Press Enter to bypass the Dynamic Shelf Life Calculation Method field.
10 In the Enter Expiry Dates field, key in Y for Yes or N for No and press Enter. If you select No, proceed to step 14.
11 In the Expiry Date Derived from field, use your pick list function to select an appropriate inventory level or press Enter to bypass this field if you are not using a formula to convert your date codes. 
To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
12 If you selected an inventory level in the previous step, key in your expiry date formula provided by 
HighJump and press Enter. 
Then key in the format of your expiry dates in the Expiry Date Format field and press Enter.
13 If you need to add a specified number of days or months to your date in order to arrive at an expiry date, key in a shelf life duration and press Enter. If you do not need a shelf life duration, press Enter to bypass this field.
If you specified a shelf life duration, key in your shelf life frequency (D for Days or M for Months) and press Enter.
14 In the Ship by Weight field, key in D for Disallowed and press Enter.
15 In the Automatic Hold Code for Expired Inventory field, key in your hold code for expired product or press 
Enter to bypass this field.
16 if you wish to track stale product, enter the number of days for stale product and press Enter. Then enter your hold code for stale product.
17 Press Enter to bypass the remaining fields in ITSH.
18 When you finish entering your item shipping profile, click on Return to Main.

Item Shipping Profile screen showing expiry dates based on inventory level 3
19 Click on Exit to exit.

### Item Process Profile (IPRP) <a id="item-process-profile-iprp"></a>

OVERVIEW
In this program, you set up an N/A (Not Applicable) item process profile code. An N/A code in IPRP is required because IPRP is a mandatory profile for ITEM. In ITEM you will attach this profile to all your items.
If you use item process codes to capture item-specific information such as serial numbers, catch weights or temperatures, refer to the item process values section of the Operations 2 Guide for complete setup instructions.
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

PROCEDURE
1 Enter IPRP.
2 Click on Enter Criteria then Execute Query to see whether an N/A code has already been set up.
3 If you need a new item process profile, click on Create Record.
4 Key in N/A as your process profile code and press Enter.
5 Key in a description for your code and press Enter.
6 Click on Master Block to exit the Detail Block.

Item Process Profile Code screen
7 Click on Exit to exit.
FIELD DESCRIPTIONS
Process Profile Code Mandatory
Your process profile code. For example, N/A for Not Applicable.
Description Mandatory
Your process profile code description

### Item Quantity Breakdown Profile (IQBP) <a id="item-quantity-breakdown-profile-iqbp"></a>

OVERVIEW
In this program, you set up the quantity breakdowns for your items. The quantity breakdown defines which 
SKU types (pallets, eaches, pieces, barrels, rolls, etc.) you wish to use to record the quantities of an item for tracking and billing purposes. You can define up to five different SKU types in a single quantity breakdown profile. 
Some typical quantity breakdowns are:
▪ pallets/cases
▪ pallets/cases/eaches
▪ cases/retail packs
▪ bales
A quantity breakdown can contain both unit-based SKU types and a unit of measure such as weight or a linear measurement. For example, the following quantity breakdowns are supported:
▪ rolls/meters
▪ totes/pounds
By using meters and pounds in your quantity breakdown, you can ship partial quantities of rolls and totes.
In IQBP you define the SKU types that an item’s quantity can be expressed in; for example, PALLETS/
CASES. In ITEM, you define the relationship between these SKU types or the actual quantities — that is, the number of cases to a pallet, the number of eaches in a box, the number of meters in a roll, etc.
You must set up one quantity breakdown profile for each item with a different quantity breakdown. For example, customer A receives item 123 in cases/pieces but item 456 in cases only. In this case, you would 
PREREQUISITES: SKUS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: A list of all SKU types used by your customers
NOTE Do not confuse the quantity breakdown with inventory levels. The quantity breakdown describes how much do I have of an item; for example, I have 3 pallets and 15 cases of item X. Inventory levels, on the other hand, describe what exactly item X is; for example, the color, size, production date, expiry date, serial number, etc. 
of item X.

need two quantity break-down profiles: one for item 123 (CASES/PIECES) and another for item 456 (CASES). 
IQBP also defines the default SKU types for shipping, receiving, adjustments, etc. The defaults in this profile override any defaults that you set in CUST.
FIELD DESCRIPTIONS
Quantity Breakdown Profile CodeMandatory
Your quantity breakdown profile code. For example, PC for Pallets/Cases or 
CASE for Cases Only.
Description Mandatory
Your quantity breakdown profile code description
Qualifier Code Mandatory
The unit of measure for the SKU type. Use UNIT for SKU types consisting of a physical object such as case, pallet, each, drum, etc.

SKU Block
SKU Code (SKUS) Mandatory
CAUTION The SKU type for this quantity breakdown. The SKU type that you enter in this field (for example, pallets, eaches, cartons, boxes, etc.) must match your billing SKU type for the item IQBP is going to be attached to. If the two SKU types do not match, you may not be able to bill the item.
EXAMPLE
You set up a charge code in CHAR called ABC and your charge on SKU type in that charge code is CS (Cases). Cases are assigned to SKU class 3 (Cases and the like) in SKUS. Then you attach your ABC charge code to your item billing profiles: IISP, IRSP and IHAP. 
In order to be able to bill, one of the SKU types that you enter in IQBP must belonging to the same SKU class (that is, SKU class 3). If, for example, your item billing profiles are charging by pallet (SKU class 1) and your item quantity breakdown profile is defined as boxes (SKU class 3), AccellosOne 3PL will be unable to rate your receipt.
Receipt Process Y = Yes
N = No
If you set this field to Yes, you can receive in the SKU type that you specified in the previous field. If you set this field to No, you cannot receive in the SKU type that you specified in the previous field.
This field must be set to Yes for one SKU type in every profile. If your quantity breakdown is PALLETS/CASES and you set this flag to Yes for pallets and to 
No for cases, you will be able to receive in pallets only. If you wish to receive in pallets and cases, you must set this flag to Yes for both SKU types.
Shipment Process Y = Yes
N = No
If you set this field to Yes, you can ship in the SKU type that you specified in the SKU Code field. If you set this field to No, you cannot ship in the SKU type that you specified in the SKU Code field.
This field must be set to Yes for one SKU type in every profile. If your quantity breakdown is CASES/PIECES and you set this flag to Yes for cases and to No for pieces, you will be able to ship in cases only. If you wish to ship in cases and pieces, you must set this flag to Yes for both SKU types.

Report Process Y = Yes
N = No
If you set this field to Yes, AccellosOne 3PL will show quantities in LOEN in the SKU type that you specified in the SKU Code field. If you set this field to 
No, AccellosOne 3PL will show quantities in LOEN in another SKU type that you specify.
EXAMPLE
Suppose an item has a quantity breakdown of pallets/cases/eaches and there are 10 eaches in a case and 50 cases on a pallet. The available quantity is 
1,015 eaches.
Example 1
Report Process flag = N for Pallets
Report Process flag = N for Cases
Report Process flag = Y for Eaches
Available quantity in LOEN = 1,015 eaches
Example 2
Report Process flag = N for Pallets
Report Process flag = Y for Cases
Report Process flag = Y for Eaches
Available quantity in LOEN = 101 cases 5 eaches
This field must be set to Yes for one SKU type in every profile.
Invoice Report Process Y = Yes
N = No
This field determines which SKU type(s) that you wish to appear on your invoices. For example, if you set this field to Yes for pallets, the word “pallets” 
will appear on your invoices.
If you use non weight-based billing, you must set this field to Yes for whichever SKU type(s) you are billing on as defined in IISP, IRSP and IHAP. If you use weight-based billing, you can set this field to Yes for any SKU type.
SKU Block

Adjustment Process Y = Yes
N = No
This flag refers to the following programs:
ENAJ (Enter Inventory Adjustment)
RELO (Relocate Inventory)
HOAD (Inventory Hold Adjustments)
If you set this field to Yes, you will be able to make adjustments in the above programs in the SKU type that you specified in the SKU Code field. If you set this field to No, you will not be able to make adjustments in this SKU type.
This field must be set to Yes for one SKU type in every profile. 
Layer Configuration 
Required
Y = Yes
N = No
Layer configuration refers to the hi and the tie (that is, the number of layers on a pallet and the number of items per layer). If you set this field to Yes, AccellosOne 3PL will require this information to be entered when you set up an item in ITEM. If you set this field to No, this information will not be required in ITEM.
Layer configuration is not required for single level quantity breakdowns (for example, pallets only) or multi-level quantity breakdowns when one breakdown is a unit of measure rather than a physical object (for example, rolls/ meters).
In all other cases, layer configuration must be set to Yes if you wish to perform directed put-away.
SKU Block

PROCEDURE
1 Enter IQBP.
2 Click on Enter Criteria then Execute Query to see which item quantity breakdown profiles have already been set up.
3 If you need a new item quantity breakdown profile, click on Create Record.
4 Key in an item quantity breakdown code and press Enter.
Rounding Code The Round Up, Truncate and Round Down options are only available for a single SKU type. All other SKU types must be assigned the No Rounding rounding code.
This option is only available for customers with a single inventory level.
R = Round Down (round up if greater than 50%; otherwise round down)
T = Truncate
U = Round Up (always round up)*
N = No Rounding
This field allows you to define how you want to round the shipped quantity of an order so that you avoid the need to break a case, inner pack or some other 
SKU code. For example, suppose your quantity breakdown is as follows:
CASE = 1
INNER PACK = 10 (10 inner packs per case)
EACH = 12 (12 eaches per inner pack)
You receive an order for 100 eaches or 8.3 inner packs. If you select Round 
Down, AccellosOne 3PL will ship 8 inner packs or 96 eaches. If you select 
Truncate, AccellosOne 3PL will ship 8 inner packs or 96 eaches. If you select 
Round Up, AccellosOne 3PL will ship 9 inner packs or 108 eaches.
You set the Rounding Code flag to the appropriate value at the SKU level below the SKU level that you are rounding up or down to. In the example above, you would activate rounding for your eaches SKU — not for your inner pack SKU.
The following conditions must be met before rounding will take place:
▪ the order quantity of the order line must consist of a single SKU type (for example, 100EA not 10CS 5EA)
▪ the Break Quantity at SKU Class field in PIPR must be set to break at any 
SKU class
*Not available for highest SKU.
SKU Block

5 Key in a meaningful description for your code (for example, “pallets and cases” or “pallets/cases/ eaches”) and press Enter.
6 Use your pick list function to select an appropriate qualifier code (usually UNIT). To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code.
AccellosOne 3PL will assign level 1 to this SKU type and position your cursor in the SKU Code field.
7 Use your pick list function to select an appropriate SKU type.
8 In the Receipt Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define which SKU types you wish to receive in.
9 In the Shipment Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define which SKU types you wish to ship in.
10 In the Report Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define which SKU types you wish to report in.
11 In the Invoice Report Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define which SKU types you wish to appear on your invoices. 
12 In the Adjustment Process field, key in the appropriate value (Y for Yes or N for No) and press Enter to define which SKU types you wish to make adjustments to in ENAJ, RELO and HOAD.
13 In the Layer Configuration Required field, key in the appropriate value (Y for Yes or N for No) and press 
Enter.
14 In the Rounding Code field, key in the appropriate value (R for Round Down, T for Truncate or U for 
Round Up) and press Enter.
CAUTION Make sure that the SKU type that you use for the Invoice Report matches the SKU type that you are charging on in your item billing profiles.

Item Quantity Breakdown Profile showing prompt for second SKU type
15 If you are setting up a quantity breakdown profile consisting of a single SKU type, your profile is complete. Press Return to Main to exit create mode. Then click on Master Block and Exit to exit the program. 
If you are setting up a quantity breakdown profile consisting of multiple SKU types (for example, PALLETS/CASES/EACHES or CASES/RETAIL PACKS), you must set up the other SKU types. Enter your next SKU type following the steps outlined above. 
16 When you finish entering all your SKU types for this profile, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit.

### Item Alternate Sorts (ITAS) <a id="item-alternate-sorts-itas"></a>

PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

OVERVIEW
In this program, you define your alternate reporting type codes. Alternate reporting type codes serve three functions:
▪ you can use them in the programs INAS (Inventory Report by Alternate Sort) and INAI (Inventory by 
Alternate Sort - Item Level) to generate consolidated inventory reports showing all product of a specific type regardless of customer
▪ you can use them to rename an item in your inventory reports (for example, you receive an item called 
OFFICE DESK #1 and you wish to list it in an inventory report under another name — say, 497-4678-A)
▪ you can use them to group items for billing purposes (for example, all items belonging to the same product line can be treated as a single item for billing purposes)
The same item can be assigned multiple alternate reporting type codes.
CONSOLIDATED INVENTORY REPORTS
If you have a customer who deals in meat, dairy products and fish, and you want to know how much meat this customer has in your warehouse, you would use ITAS.
You would set up an ITAS code for meat and attach it to all this customer’s meat items. Then you would run an inventory report in INAS specifying the meat code as your alternate reporting type. The report would show all meat items for this customer.
ITAS is similar to DEAS (Depositor Alternate Sorts). ITAS defines alternate sorts at the item level while DEAS defines alternate sorts at the customer level. DEAS is always customer specific while ITAS can be attached to any item belonging to any customer.
The codes that you create in this program can be either single level or double level. For example, if you create a code for ICE CREAM, this is considered a single-level alternate sort. If, however, you want to track both ice cream in general and particular flavours of ice cream, you would have to break down your ICE 
CREAM code into VANILLA, CHOCOLATE and STRAWBERRY. This is considered a double-level alternate sort. 
If you wish to … setup required … generate consolidated inventory reports▪ create a single level or double level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block in ITEM
▪ when you run inventory reports in INAS or INAI, specify the alternate reporting type that you created in ITAS
Item 1 meat
Item 2 fish
Item 3 dairy
Item 4 meat
Item 5 fish
Item 6 meat
MEAT

rename an item in an inventory report▪ create a single level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block in ITEM
▪ when you run inventory reports in INAS or INAI, specify the alternate reporting type that you created in ITAS group items for billing purposesAlternate billing applies to renewal storage only and overrides any renewal storage options that you set up in 
DILP. Alternate billing is not available for initial storage charges.
Alternate billing must be applied to all of a customer’s items. You cannot mix alternate billing and regular billing within the same customer.
▪ create a single level or double level code in ITAS
▪ attach your ITAS code to the Alternate Reporting Block in ITEM for all items in the group
▪ attach the same ITAS code to your DBIP profile
FIELD DESCRIPTIONS
Alternate Inventory 
Reporting Type
Mandatory
Your alternate inventory reporting type code. For example, USDA for USDA 
Tracking.
Description Mandatory
Your alternate inventory reporting type code description
Alternate Inventory 
Reporting Code
Mandatory
If you are setting up a single-level alternate sort, your code in this field will be the same as your code in the Alternate Inventory Reporting Type field. If you are setting up a double-level alternate sort, you would enter your second level alternate sort code in this field.
If you wish to … setup required …

PROCEDURE
1 Enter ITAS.
2 Click on Enter Criteria then Execute Query to see which alternate reporting types have already been set up. 
3 If you need a new alternate reporting type, click on Create Record.
4 Key in an alternate reporting type code and press Enter.
5 Key in your description and press Enter.
6 Key in your second code and a meaningful description and press Enter after each entry.
7 Press Enter to bypass the Billing Code field.
8 Repeat the above steps for each additional second-level code that you wish to add.
Description Mandatory
If you are setting up a single-level alternate sort, your description in this field will be the same as your description for your alternate inventory reporting type code. If you are setting up a double-level alternate sort, you would enter your second level alternate sort description in this field.
Billing Profile Code (defined in IBIP)
Optional
Refer to the section on alternate billing groups in the Billing and Invoicing 
Guide.
If you are creating a single-level alternate sort code:
If you are creating a double-level alternate sort code:
a) Key in the same code and description that you entered in the Main Block and press Enter after each entry. 
b) Press Enter to bypass the Billing 
Code field.
c) Click on Return to Main to exit create mode. Then click on Master Block and Exit to exit.
a) Proceed to next step.
FIELD DESCRIPTIONS

Item Alternate Sorts showing double-level codes
9 When you finish entering your second-level codes for this reporting type, click on Return to Main to exit create mode. Then click on Master Block and Exit to exit.

### Hold Types (HOLD) <a id="hold-types-hold"></a>

OVERVIEW
In this program, you set up your hold codes. You use hold codes to put product on hold in programs like 
POHO and HOAD. You can also attach a hold code to a location in LOCA so that product placed in that location is automatically assigned that hold code. When a product is on hold, it can be either shippable like normal product or non-shippable (non-shippable product is product that cannot be shipped until the hold is removed).
You can use hold codes for product damaged in the warehouse, product damaged in transit, products that need a quality assurance inspection, etc. Some sample hold codes are:
Damaged Hold
Customer Hold
PREREQUISITES: None
ATTACHED TO: LOCA (Locations)
IHOP (Item Hold Profile)
HOSP (Hold Shipping Sequence Profile Code)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: A list of all the reasons why you put product on hold in your warehouse

USDA Inspection
Repair Return
FIELD DESCRIPTIONS
Hold Type Mandatory
Your hold type code.
Description Mandatory
Your hold type description.
Ship If you define a hold type as shippable, the product is shippable despite the hold. If you define a hold type as non-shippable, you will have to remove the hold before you can ship the product.
Renew If you define a hold type as renewable, renewal storage will be charged on product to which this hold type has been attached. If you define a hold type as non-renewable, no renewal storage will be charged on product to which this hold type has been attached.
Bond If you define a hold type as a bond hold, the hold type can be used in the bond system to place product on bond hold. If you define a hold type as a non-bond hold, the hold type is a regular non-bond hold type.
Dmg Reserved for future use.
Breakable Inventory If you define a hold type as breakable, you can relocate and make hold adjustments to partial quantities. For example, if you have 10 cases of product (say, item A, lot 101) on a breakable hold called DMG, you can relocate a partial quantity such as 5 cases to another location in RELO and you can remove a partial quantity such as 3 cases from hold in HOAD.
If you define a hold type as non-breakable, the following will occur:
▪ When relocating a specific inventory entity in RELO, the entire entity on the non-breakable hold must be relocated; you cannot relocate partial quantities. 
▪ When placing a specific inventory entity on non-breakable hold in HOAD, you must place the entire entity on hold.
▪ When removing a specific inventory entity from non-breakable hold in 
HOLD, you must remove the entire entity.
QA Reserved for future use.

Res. Reserved for future use.
Disabled EDI Send If you select this option, the hold type will be excluded from EDI hold adjustment transactions. 
For example, if BL (Blast Hold) is checked, EDI transactions will not report on blast hold transactions for inbound or outbound product. So when the warehouse ABC Foods puts product received from customer A on blast hold, customer A will not be notified of the blast hold activity in its EDI transactions.
e-Vista Activation in e-Vista at both the account and user level required
If you select this option, your customers can place product on hold in the 
Inventory Balances tab of e-Vista using this hold type. If you do not select this option, the hold type will not be available in the Inventory Balances tab of eVista.
Auto Take-Off Only available for non-bond holds
If you define a hold type as non-auto take-off, the hold must be manually removed. If you define a hold type as auto take-off, the hold will be removed after the number of days specified in the Days field has passed or on the date that you specify in the Date field. To activate auto take-off, you must run the program HATO (Holds Auto Take-Off).
Days Only available if Auto Take-Off flag set to Yes
Specifies the number of days for auto take-off holds. AccellosOne 3PL calculates the date by adding the number of days plus one day to the current date. 
For example, if you place product on hold on January 1 and the number of days is 5, the hold will come off on January 7 (January 1 + 5 = January 6 + one day = January 7).
If you wish to set up a 24-hour hold, use zero as your number of days value. 
For example, product is placed on hold on March 10 and the hold is removed at midnight or on March 11.
If you enter a number of days value, you cannot enter a an auto take-off date.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter HOLD.
2 Click on Enter Criteria then Execute Query to see which hold types have already been set up.
Hours Only available if Auto Take-Off flag set to Yes
Specifies the number of hours for auto take-off holds.
Date Only available if Auto Take-Off flag set to Yes
Specifies the auto take-off date. You can change this date whenever required and the change will apply to existing inventory in your warehouse.
If you enter an auto take-off date, you cannot enter a number of days value.
RF Hold Excl From If you select RF Hold Excl From, you cannot remove this hold code from product in RFHO. If you leave this checkbox unselected, there are no restrictions related to this hold code in RFHO. 
RF Hold Excl To If you select RF Hold Excl To, you cannot attach this hold code to product in 
RFHO. If you leave this checkbox unselected, there are no restrictions related to this hold code in RFHO. 
Excl From Count Back If you select this checkbox, any product on this hold code will be excluded from the system count during a count back. If you leave this checkbox unselected, the system count will include all product in a given location regardless of its hold status.
Picking Profile If you attach a picking profile set up in PIPR to a hold type, any order lines placed on that hold type will be allocated according to the hold type’s picking profile; that is, the customer’s item’s or consignee’s picking profile will be overridden by the hold type’s picking profile.
This feature makes it possible to define special picking rules for expired product by creating a hold type for expired product, assigning it a unique picking profile and then attaching your new hold type to your expired inventory. When you run allocation, AccellosOne 3PL will use the hold type’s picking profile rather than the regular picking profile(s) attached to the customer, item or consignee
FIELD DESCRIPTIONS

Hold Types
3 If you need a new hold type, click in the empty Hold field after your last hold type record. If there are no blank lines on your screen, click on New to create one.
4 Key in your hold code and press Enter.
5 Key in a description for your new hold code and press Enter.
6 Click on the appropriate checkboxes to select your hold type options.
7 If you selected the Auto Take-Off option, key in the number of days or the auto take-off date.
8 If required, select the RF Hold Excl From, the RF Hold Excl To and/or the Exclude From Count Back checkbox(es).
9 If required, select a picking profile from the pick list for your new hold type.
10 When you finish entering your hold types, click on Save to save your new hold type.
11 Click on Exit to exit HOLD.

### Hold Shipping Sequence Profile Code (HOSP) <a id="hold-shipping-sequence-profile-code-hosp"></a>

PREREQUISITES: HOLD
ATTACHED TO: IHOP (Item Hold Profile)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:

OVERVIEW
This program allows you to set up order allocation so that AccellosOne 3PL selects inventory entities based on hold codes. You specify in HOSP which hold codes you want to allocate first, which hold codes you want to allocate second and so on and so forth.
EXAMPLE
The allocation routine will attempt to fill the order line by selecting product to which you have assigned the 
Quality A hold. Once all the Quality A product has been allocated, if the order remains unfilled the allocation routine will look for product with a hold code of Quality B. Once all the Quality B product has been allocated, if further product is required the allocation routine will search for Quality C product.
If there remains product to be allocated and the allocation routine runs out of product on holds A, B and C, then the order line is left not fully allocated.
SEQUENCE HOLD CODE
1 Quality A
2 Quality B
3 Quality C
FIELD DESCRIPTIONS
Hold Shipping Sequence 
Profile Code
Mandatory
Your hold shipping sequence profile code.
Description Mandatory
Your hold shipping sequence profile description.
Sequence Number Mandatory
The sequence number for the hold code; for example, 1, 2, 3, 4, etc.

PROCEDURE
1 Enter HOSP.
2 Click on Enter Criteria then Execute Query to see which hold shipping profiles have already been set up. 
If you need a new hold shipping profile, click on Create Record.
3 Key in a profile code and press Enter.
4 Key in a description for your new profile code and press Enter.
5 Starting at 1, key in your sequence number for the hold code and press Enter.
6 Key in your hold code for the sequence and press Enter or use your pick list function to select it. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code.
7 Repeat the above two steps for each additional hold code that you wish to add to the profile.

Hold Ship Profile Code
8 When you finish entering your hold codes for this profile, click on Return to Main to exit create mode. 
Then click on Exit to exit.
Hold Code (HOLD) Mandatory
The hold code for the sequence. Any holds that you enter in this field must be defined as shippable holds in HOLD. The hold code for the first sequence must be the same as the outbound hold code that you define in IHOP.
EXAMPLE 
Sequence in HOSP
Outbound Hold Code in IHOP
FIELD DESCRIPTIONS

### Item Hold Profile (IHOP) <a id="item-hold-profile-ihop"></a>

OVERVIEW
In this program, you set up your item hold profiles. An item hold profile defines your inbound and outbound hold codes. You use an inbound hold code when you wish to place an item on automatic hold whenever it is received in ENRE. You use an outbound hold code when you wish to ship only product that has been assigned that hold code. If required, the same item can be assigned one inbound hold code and on another outbound hold code.
For example, if you have a product that requires blast freezing, you would create an item hold profile for blast freezing. In the profile you would assign your blast freezing hold code as the profile’s inbound hold code. 
Then you would attach the profile to the item in ITEM. 
PREREQUISITES: HOLD, HOSP
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Hold Profile Code Mandatory
Your hold profile code.
Description Mandatory
Your hold profile code description.
Inbound Hold Code (HOLD)
Optional
The hold code that you wish to attach to an item when it is inbound. If you create new inventory in ENAJ (Enter Inventory Adjustment), the hold code will be automatically attached to it.

INBOUND LOCATION TYPE BLOCK
This block allows you to define a relationship between an inbound hold code and location type code. The 
Inbound Location Type block is only available when the Inbound Hold Code field is not populated in the header.
When you confirm the receipt, the hold code defined in the Inbound Location Type Block will be applied to the receipt line/receipt location line if the put-away location's location type matches the location type in the 
Inbound Location Type Block. If a hold code has been assigned to a receipt line or receipt location line in 
ENRE, it will override the hold code defined in the Inbound Location Type Block.
Allow Override of Hold 
Code During Core RF 
Receiving
Only available for core RF receiving
Y = Yes
N = No
If you set this flag to Yes, you can override or remove automatic holds when receiving in RFCH or RFPU. If you set this flag to No, you cannot override or remove automatic holds in RFCH or RFPU.
Outbound Hold Code (HOLD)
Only mandatory if you wish to define a hold ship sequence in HOSP
The hold code that product must be attached to before it can be allocated in an outbound order. The hold code that you enter in this field must match the hold code in your first sequence in HOSP.
Hold Ship Sequence Profile Code (HOSP)
Optional
If you set up a hold ship sequence profile in HOSP, the allocation routine will select product based on hold code. For example, first allocate all product to which you have assigned your Quality A hold, then if the order remains unfulfilled allocate product assigned your Quality B hold. If the order still requires further product, allocate your Quality C hold, etc.
FIELD DESCRIPTIONS

Inbound Location Type Block (IHOP)
PROCEDURE
1 Enter IHOP.
2 Click on Enter Criteria then Execute Query to see which hold profiles have already been set up.
3 If you need a new hold profile, click on Create Record.
4 Key in a hold profile code and press Enter.
5 Key in a description for your new hold profile code and press Enter.
6 If you want the code to be applied to an item when it is inbound, use your pick list function to select the appropriate hold code. To select a code using a pick list, press F10 to display the pick list and click on 
Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
If you do not want an inbound hold code, press Enter to bypass this field.
7 In the Allow Override of Hold Code During Core RF Receiving field, key in Y for Yes or N for No and press Enter.
8 If you want the code to be applied to an item when it is outbound, use your pick list function to select the appropriate hold code.
If you do not want an outbound hold code, press Enter to bypass this field.
9 If required, key in a hold ship profile code in the Hold Ship Sequence Profile Code field and press Enter or press Enter with the field blank to bypass this option.
10 Repeat steps 4 to 9 for each additional hold profile that you wish to add.
11 When you finish entering your hold profiles, click on Return to Main to exit create record mode.

Item Hold Profile
12 Click on Exit to exit.

### Item Incubation Hold Code (IIHO) <a id="item-incubation-hold-code-iiho"></a>

OVERVIEW
In this program, you set up your incubation holds. Incubation holds allow you to define an “incubation” period for inbound product during which the product cannot be shipped because it is not yet considered ready. The incubation period is based on a fixed number of days from the manufacturing or slaughter date. The hold is automatically applied to the product when you confirm the receipt in CHRF. At the end of the incubation period, you must release the incubation hold by running HATO (Holds Auto Take-Off).
In order to use incubation holds, the manufacturing or slaughter date must be embedded in one or more inventory levels and an SQL statement must be written to extract this date.
PREREQUISITES: HOLD, ITEM, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: The special verify program PIIH (Put Item on Incubation Hold) must be attached to the inbound flow CORE (Confirm Receipt) in DIFP

You need to set up one record in IIHO for each item that you wish to place on incubation hold.
PROCEDURE
1 Enter IIHO.
2 Click on Enter Criteria then Execute Query to see which incubation holds have already been set up.
3 If you need a new incubation hold code, click on Create Record.
4 In the Customer Code field, key in your customer code and press Enter.
5 In the Item Code field, key in your item code and press Enter.
6 In the Incubation Hold Code field, key in your incubation hold code and press Enter.
7 In the Number of Days field, key in the number of days that the incubation period will last.
NOTE IIHO is used when each item in your warehouse has different incubation hold rules. If you have multiple items with the same incubation hold rules, IIHP (Incubation Hold Profile) is the recommended setup program to use.
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer whose product will be placed on incubation hold.
Item Code (ITEM) Mandatory
The product that will be placed on incubation hold.
Incubation Hold Code (HOLD)
Mandatory
The incubation hold code for the product. The Auto Take-Off flag in HOLD must be set to Y for Yes for this hold code.
Number of Days The number of days from the manufacturing or slaughter date that the incubation period will last.
Date Formula The SQL statement that will extract the manufacturing or slaughter date from one or more inventory levels.
Date Format The format of the date being extracted.

8 In the Date Formula field, key in your SQL statement for extracting the date and press Enter.
9 In the Date Format field, key in your date format and press Enter.

Item Incubation Hold Code screen showing a three-day incubation period based on inventory level 2
10 Repeat the above steps for any additional items that you want placed on incubation hold.
11 When you finish entering your incubation hold, click on Return to Main and then Exit to exit.
12 Enter DIFP and retrieve the workflow profile code for the customer whose product you wish to place on incubation hold. Make sure that the special verify PIIH is attached to the inbound flow CORE (Confirm 
Receipt).

### Incubation Hold Profile (IIHP) <a id="incubation-hold-profile-iihp"></a>

PREREQUISITES: HOLD, ITEM, CUST
ATTACHED TO: ITEM
GLOBAL/UNIQUE: Unique
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: The special verify program PIIH (Put Item on Incubation Hold) must be attached to the inbound flow CORE (Confirm Receipt) in DIFP

OVERVIEW
IIHP is an alternate version of IIHO. It is used when you have multiple items with the same incubation hold code rules. When you attach an incubation hold profile to an item in ITEM and click on Process, AccellosOne 
3PL will automatically create an IIHO record for that customer/item.
PROCEDURE
1 Enter IIHP.
2 Click on Enter Criteria then Execute Query to see which incubation hold profiles have already been set up.
3 If you need a new incubation hold profile, Click on New.
4 In the Incubation Hold Profile Code field, key in your incubation hold profile code and press Enter.
5 In the Incubation Hold Code (HOLD) field, key in your incubation hold code and press Enter.
6 In the Number of Days field, key in the number of days that the incubation period will last.
7 In the Date Formula field, key in your SQL statement for extracting the date and press Enter.
8 In the Date Format field, key in your date format and press Enter.
FIELD DESCRIPTIONS
Incubation Hold Profile Mandatory
Your incubation hold profile code.
Description Mandatory
Your incubation hold profile description.
Incubation Hold Code (HOLD)
Mandatory
The incubation hold code for the product. The Auto Take-Off flag in HOLD must be set to Y for Yes for this hold code.
Number of Days The number of days from the manufacturing or slaughter date that the incubation period will last.
Date Formula The SQL statement that will extract the manufacturing or slaughter date from one or more inventory levels.
Date Format The format of the date being extracted.

Item Incubation Hold Profile screen showing a three-day incubation period based on inventory level 2
9 When you finish entering your incubation hold, click on Save to save your changes.
10 Click on Exit to exit.
11 Enter DIFP and retrieve the workflow profile code for the customer whose product you wish to place on incubation hold. Make sure that the special verify PIIH is attached to the inbound flow CORE (Confirm 
Receipt).
ATTACHING YOUR INCUBATION HOLD CODE TO AN ITEM
When you attach an incubation hold profile to an item in ITEM and click on Process, AccellosOne 3PL will automatically create an IIHO record for that customer/item.
1 Enter ITEM.
2 Retrieve the item that you wish to set up for incubation holds.
3 Click on IIHO Block.

ITEM screen showing IIHO Block
4 Key in your incubation hold profile code and press Enter.
5 Click on Process.
6 Press F4 to exit.

### Freight Class Codes (CLAS) <a id="freight-class-codes-clas"></a>

OVERVIEW
In this program, you set up your freight class codes. Freight class codes are required for the commodity code or National Motor Freight Class (NMFC) system of freight classification. Freight class and commodity codes are normally printed on your bill of lading.
If you use AccellosOne Transport and charge different rates based on the class of freight, you must set up one class code for each class of freight. If you do not use AccellosOne Transport and do not require commodity codes and class codes on your bill of lading, use AccellosOne 3PL class FAK (Freight All Kinds) 
for all your items. 
PREREQUISITES: None
ATTACHED TO: COMM (Commodity) --> ITEM
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

PROCEDURE
1 Enter CLAS.
2 Click on Enter Criteria then Execute Query to see which freight class codes have already been set up.

Freight Class Codes
3 If you need a new freight class code, click on Create Record.
4 Key in a freight class code and press Enter.
5 Key a description for your new freight class code and press Enter.
6 Repeat steps 4 and 5 for each additional freight class that you wish to enter.
7 When you finish entering your freight class codes, click on Return to Main and then Exit to exit.
FIELD DESCRIPTIONS
Freight Class Code Mandatory
Your freight class code.
Description Mandatory
Your freight class code description.

### Commodities (COMM) <a id="commodities-comm"></a>

OVERVIEW
In this program, you set up your commodity codes. Commodity codes are required for the National Motor 
Freight Class (NMFC) system of freight classification and are used primarily for freight rating purposes in 
AccellosOne Transport. Commodity codes are normally printed on your bill of lading; this requires special programming by HighJump. If required, you can attach message text to your commodity code and print it on your bill of lading.
If you do not need commodity codes on your bill of lading, use AccellosOne 3PL commodity code FAK (Freight All Kinds) for all your items.
PREREQUISITES: CLAS
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:
FIELD DESCRIPTIONS
Commodity Code Mandatory
Your commodity code.
Subcode Mandatory
Your commodity subcode. If you are setting up a single commodity code, use 
00 in this field.
Freight Class (defined in CLAS)
Mandatory
Your freight class code.

PROCEDURE
1 Enter COMM.
2 Click on Enter Criteria then Execute Query to see which class codes have already been set up.

Commodity
3 If you need a new commodity code, click on Create Record.
4 Key in a commodity code (for example, FAK for Freight All Kinds) and press Enter.
5 Key in a subcode (for example, 00) and press Enter.
6 Use your pick list function to select the appropriate freight class code that you created in CLAS. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on 
Select Code. 
Text Block Optional
The message text for your commodity code.
FIELD DESCRIPTIONS

7 Do one of the following:
8 Repeat steps 3 to 7 for each additional commodity code that you wish to enter.
9 When you finish entering your commodity codes, click on Exit to exit.

### Item Location Profile (ILOP) <a id="item-location-profile-ilop"></a>

OVERVIEW
In this program, you set up a single item location profile called NA for passive shipping and receiving. Passive shipping and receiving means that locations for inbound receipts and outbound orders will be manually assigned by the operator.
If you wish to set up active shipping or receiving (that is, AccellosOne 3PL assigns the locations), refer to the 
Allocation and Wave Manager Guide. 
If you wish to attach message text to your commodity code:
If you do NOT wish to attach message text to your commodity code:
a) Type in your text. If you require more than one line of text, press 
Enter at the end of the line to generate a new line. You can enter as many lines as you need. 
b) When you finish entering your last line, press Enter. Then click on Master Block.
a) Click on Master Block to exit the 
Text Block.
PREREQUISITES: ISOL, WARE, LOCA
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS:

PROCEDURE
1 Make sure that the Assign Location flags in DIFP are set to No for the customer to whom your passive 
ILOP profile will be attached.
2 Enter ILOP.
3 Click on Enter Criteria then Execute Query to see which item location profiles have already been set up. 
4 If you need a new item location profile, click on Create Record. If Create Record is not available, click on 
Return to Main to activate it.
5 Key in NA as your item location profile code and press Enter.
6 Key in PASSIVE LOCATOR as your description and press Enter.
7 Use your pick list function to select NA or ALL as your isolator code. To select a code using a pick list, press F10 to display the pick list, use your arrow keys to position your cursor over the appropriate code and click on Select Code to select it. 
FIELD DESCRIPTIONS
Item Location Profile 
Code
Mandatory
Your item location profile code.
Description Mandatory
Your item location profile code description.
Isolator Code (ISOL) Mandatory
Use ALL or NA as your isolator code. This field is not used in passive shipping or receiving.
Overflow Warehouse 
Code (WARE)
Mandatory
Enter any valid warehouse code. This field is not used in passive shipping or receiving.
Overflow Location Code (LOCA)
Mandatory
Enter any valid location code. This field is not used in passive shipping or receiving.

8 Use your pick list function to select any warehouse on your system.
9 Use your pick list function to select any location code on your system.

Item Location Profile for passive locator system
No further input is required. AccellosOne 3PL will display the Type Block.
10 Click on Master Block to exit the Type Block.
11 Click on Exit to exit.

### Item Tare Profile (ITAP) <a id="item-tare-profile-itap"></a>

OVERVIEW
In this program, you set up your tare weight profiles. You use tare weight profiles for items of non-standard weight when the tare weight of an item varies in a non-linear way depending on the weight of product 
PREREQUISITES: None
ATTACHED TO: ITEM (Item)
GLOBAL/UNIQUE: Global 
MANDATORY/OPTIONAL: Optional
OTHER REQUIREMENTS: Standard Weight field in ITEM is set to the appropriate tare weight option

received. For example, the tare weight of one item is 5 lbs. while the tare weight of two items is a value other than 10 lbs.
EXAMPLE
In ITEM, you select “Enter Rcpt Gross Wgt, Calc Rcpt Net Wgt from Tare” as your weight option in the 
Standard Weight field. Then you set up the following ITAP profile and attach it to ITEM.

You receive an item and enter 150 as its gross weight. AccellosOne 3PL will look up the appropriate weight break in ITAP — break 2 — and calculate the net weight from the tare weight (150 - 15 = 135).
BREAK VALUE TARE
1 100 10
2 200 15
3 300 20
FIELD DESCRIPTIONS
Item Tare Profile Code Mandatory
Your item tare profile code.
Description Mandatory
Your item tare profile description.
Weight Measure Code The weight measure code (pounds, kilos, tons, etc.) for your tare profile. This code must match the weight code attached to the item in the Quantity Breakdown Block of ITEM.
Number of Breaks The number of breaks for your tare profile.
Value Mandatory
The weight for this break expressed in terms of the weight measure code that you entered in the Weight Measure Code field. Depending on the standard weight option that you select in ITEM, your weight breaks will be based on either the item’s net weight or gross weight. 
Tare Mandatory
The tare weight for this weight break. 

PROCEDURE
1 Enter ITAP.
2 Click on Create Record.
3 Key in your tare profile code and press Enter.
4 Key in a description for your new tare profile code and press Enter.
5 In the Weight Measure Code field, use your pick list to select the appropriate weight measure for your tare profile.
6 In the Number of Breaks field, key in the number of breaks for this tare profile and press Enter.
7 In the Break Block, key in the weight for your first break and press Enter.
8 In the Tare field, key in your tare weight for this break and press Enter.
9 Repeat the above two steps for each additional break for this profile.

ITAP screen showing four weight breaks for tare profile code 1
10 When you finish setting up your item tare profile code, click on Master Block and then Exit to exit.

## Item Setup <a id="item-setup"></a>

*Manual N — Setup Guide*

### Item (ITEM) <a id="item-item"></a>

OVERVIEW
In this program, you take the codes and profiles that you set up in the previous steps and attach them to your items. You also define the quantity breakdown of the item (x number of eaches per case, y number of cases per pallet, etc.), the base SKU type for tracking the item’s size and weight, and the linear measurements and weight of this base SKU type.
Mandatory fields in this program are:
▪ Customer Code
▪ Item Code
▪ General Information Profile Code
▪ Item Billing Profile Code
▪ Shipping Profile Code
▪ Process Profile Code
▪ Quantity Breakdown Profile Code
▪ Location Profile Code
▪ Commodity Code
▪ Entry Required up to Level
▪ Variable Quantity Breakdown
▪ Standard Weight
▪ Tax Code
There are also a number of fields in the Quantity Breakdown Block that are mandatory.
PREREQUISITES: IINP, IBIP, ITSH, IPRP, IQBP, ILOP, COMM, SKUS, CUST
ATTACHED TO: N/A
GLOBAL/UNIQUE: Unique 
MANDATORY/OPTIONAL: Mandatory
OTHER REQUIREMENTS: The quantity breakdown of the item, the layer configuration (tie and hi), the linear measurements (height, width and length) and the weight
FIELD DESCRIPTIONS
Customer Code (CUST) Mandatory
The customer to whom this item belongs.

Item Code Mandatory
Your item code. An item code can consist of any combination of numbers or letters up to 20 characters in length. Please note the following restrictions on special characters:
▪ The single quote (’) and double quote (") special characters are not valid and should never be used. 
▪ Special characters such as “&”, “%” and “_” may cause problems in certain programs and are not recommended. 
▪ The special characters “(“, “)”, “<“, “>”, “=” and “-” are required to restrict billing batchs in BILB (Billing Batch) and cannot be used.
▪ Other special characters are generally supported.
Description Mandatory
Your item code description. An item code description can consist of any combination of numbers or letters up to 20 characters in length. The special character restrictions for item codes apply equally to item descriptions.
Master Item N = No
Y = Yes
If you select Yes, the item is a master item and can have other non-master items attached to it. Master items are a way of grouping similar items.
Attached to (ITEM) Optional
The item’s master item.
General Information Profile Code (IINP)
Mandatory
This profile specifies the unit of measure that you wish to use for management reporting purposes.
Alternate Description Optional
If required, you can record a secondary description for the item in this field. 
This option can be used for bilingual product descriptions or technical data regarding the item.
FIELD DESCRIPTIONS

Extended Description Optional
This field is an overflow field for the Description field when the description exceeds 40 characters.
Hazardous Material N = No
Y = Yes
If you select Yes, you can open the Hazardous Material Block and enter hazardous material information for the item.
Item Billing Profile Code 1 (IBIP)
Mandatory
This profile controls the initial storage, renewal storage and handling charges for this item. If you wish to change this profile after receiving inventory, the change will apply to new inventory only unless you run ADBD (Adjust Billing 
Data). See the Billing and Invoicing Guide for further information.
Item Billing Profile Code 
2/3
Optional
Reserved for special or seasonal billing. See the Billing and Invoicing Guide for further information.
Extra Charge Profile 
Code (ECHP)
Optional
See the Billing and Invoicing Guide for further information.
Shipping Profile Code (ITSH)
Mandatory
This profile allows you to allocate product to an order based on an expiry date or date code. If you do not require this function for this item, use your NA (Not 
Applicable) profile. If you wish to change this profile after receiving inventory, the change will apply to new inventory only unless you run CHEI (Change 
Entity Information). See the Operations 1 Guide for further information.
FIELD DESCRIPTIONS

Process Profile Code (IPRP)
Mandatory
This profile allows you to attach predefined messages and operator-entered values to an item. If you do not require this feature, use your NA (Not Applicable) profile.
Quantity Breakdown Profile Code (IQBP)
Mandatory
The quantity breakdown for this item (for example, PALLETS/CASES or PALLETS/ CASES/EACHES).
CAUTION Once you receive inventory in a particular item, you cannot change the item’s quantity breakdown profile in ITEM. Should you need to change the profile, you must do so in AEQB (Adjust Entity Quantity Breakdown).
Location Profile Code (ILOP)
Mandatory
This profile specifies the parameters that you wish AccellosOne 3PL to use for active shipping and receiving. If you do manual put-away and picking for this item, use your NA (Not Applicable) profile.
Warehouse Code (WARE)
Optional
If the item is restricted to one warehouse, enter the warehouse code in this field. If the item can be received in any warehouse, leave this field blank.
Hold Profile Code (IHOP) Optional
If you enter a hold profile code in this field, the item will be placed on automatic hold when it is received or shipped.
Commodity Code (COMM)
Mandatory
The item’s commodity code.
FIELD DESCRIPTIONS

Entry Required up to 
Level
Mandatory
The number of inventory levels needed for this item. You can specify any number between the inventory level that you bill at (defined in DILP) and the maximum number of levels for the customer (defined in DILP) attached to this item.
For example, if you set up a customer with three inventory levels (ITEM, LOT and PALLET ID) and bill this customer at level 2, you can set this field to either 
2 (no pallet ID required for a particular item) or 3 (all inventory levels required for this item).
Number of Days for Open 
Lots
Optional
If you wish to process the item as an open lot, enter the number of days that the item can remain open. Open lots are lots that remain open for one or more days and allow you to receive the same entity in multiple receipts.
See “Open Lot Receipts” in the Billing and Invoicing Guide for further information on this field.
Variable Quantity BreakdownN = No
Y = Yes
This field allows you to specify whether you wish to allow non-standard quantity breakdowns for the item. If you set this flag to No, the quantity breakdown that you define in the Quantity Breakdown Block of this program is standard and cannot be changed for any particular receipt. If you set this flag to Yes, you can change the item’s quantity breakdown on a receipt.
EXAMPLE
Your standard quantity breakdown for a particular product is 25 pieces per case. 
If you set this field to No, each time you receive this product in ENRE, AccellosOne 3PL will automatically calculate the total number of pieces using the standard quantity breakdown. For example, if you receive 10 cases, you are receiving 250 pieces.
FIELD DESCRIPTIONS

If you set this field to Yes, each time you receive this product in ENRE, AccellosOne 3PL will prompt you to override the number of pieces per case. For example, you could enter 30 pieces per case (rather than 25) and AccellosOne 3PL would record 300 pieces received (not 250).
NOTE You can only change the quantity breakdown on a receipt if you are receiving the inventory entity for the first time. If the inventory entity has already been received by the warehouse, you cannot change its quantity breakdown. 
Renewal Options for Variable Quantity BreakdownH = High
L = Low
M = Most
S = Standard
In this field, you specify how you want AccellosOne 3PL to calculate renewal storage on variable quantity breakdown items in which the same billing entity has multiple quantity breakdowns. For example, you bill on level 2 or lot and you have four pallets in your warehouse with different quantity breakdowns but the same lot number: 
pallet 1 = 60 cases pallet 2 = 75 cases pallet 3 = 100 cases pallet 4 = 75 cases.
If you select High, AccellosOne 3PL will use the highest quantity breakdown when doing a pallet count (100 cases). If you select Low, AccellosOne 3PL will use the lowest quantity breakdown when doing a pallet count (60 cases). If you select Most, AccellosOne 3PL will use the most common quantity breakdown when doing a pallet count (75 cases). 
If you select Standard, AccellosOne 3PL will use the standard quantity breakdown defined in ITEM.
FIELD DESCRIPTIONS

Standard Weight Y = Standard Weight
F10 = Other Options
If you set this field to Standard Weight, AccellosOne 3PL will use the standard weight specified in the Quantity Breakdown Block of this program; you will not be able to modify this weight during receipt entry or order entry. If you wish to enter the weight manually on shipping or receiving or calculate the weight in a different manner, see “Non-Standard Weight Options” (ver [Item (ITEM)](configuracao-itens.html#item-item)) for further information.
If you wish to change your weight option after receiving inventory, the change will apply to new inventory only unless you run WEAD (Weight Adjustments) 
or RESW (Recalculate Standard Weight). See “Adjusting Weight Details” in the Operations 1 Guide for further information.
Tare Profile Code (ITAP) Optional
Only required if you use tare weight profiles.
Cross Dock Y = Yes
N = No (default)
See “Cross-Dock Billing” in the Billing and Invoicing Guide for further information on this field.
Item Value Optional
For use in export documents. The value that you enter in this field will appear in export documents as the declared value. Also used in cycle counting if you track variances by the item’s value.
Value for SKU Code (SKUS)
Optional
The SKU code that the value applies to.
FIELD DESCRIPTIONS

Hazard Code (HAZA) Optional
If required, the hazard code for this item. The hazard code will print on the standard bill of lading 1 and 2 and the pick document.
If you use AccellosOne Transport and attach a hazard code to an item, that item cannot be placed on the same load as an item with no hazard code attached to it.
Cycle Count Profile Code (CYCP)
Optional
See the Cycle Counting Guide for further information.
Picking Profile Code (PIPR)
Optional
If you attach a PIPR profile to this item, the item will be allocated according to the options that you defined in your PIPR profile. If you do not attach a PIPR profile to this item, the item will be allocated according to the default PIPR profile that you attached to DSRP (Depositor Shipping & Receiving).
Allow Overpick, Ignore 
Consignee
Only available if the Picking Profile Code (PIPR) field is populated with any 
PIPR profile (if this profile has overpick rules, the rules are ignored)
N = No
Y = Yes
If you set this flag to N for No, overpicking in RFPIC is deactivated for this item. If you set this flag to Y for Yes, the picker can overpick an order line in 
RFPIC up to the next full pallet quantity. 
For example, suppose the quantity breakdown of a given item is meters and pallets with a full pallet being defined as 800 meters. If the order quantity is 
500 meters, the picker is allowed to pick 800 meters, overpicking the order line by 300 meters. 
NOTE Overpicking at the item level with no consignee override is intended for facilities that ship to a single consignee. Hence, the need to ignore the consignee’s overpick rules, if any. Allowing the consignee override to take effect through a PIPR profile would force the same overpick rules on all of customer’s items.
FIELD DESCRIPTIONS

Item Discount Flag A = Always
N = No
C = Choose
See the section “Discounts on Initial Storage and Handling” in the Billing and 
Invoicing Guide.
Discount Profile Code (DPRO)
See the section “Discounts on Initial Storage and Handling” in the Billing and 
Invoicing Guide.
Tax Code Mandatory
The tax that you wish to apply to the item. The item’s tax code can be either the same as the customer’s tax code defined in DBIP (Depositor Billing Profile) or can be set to None. For example, if the customer’s tax code is GST 
Only, the item’s tax code can only be GST Only or None for no tax; you cannot enter a tax code of PST Only for any item belonging to this customer.
If you enter a tax code in this field that differs from the tax code in DBIP (Depositor Billing Profile), the tax code at the item level will override the tax code at the customer level.
Message Code (MESS) Optional
If required, the message that you wish to attach to this item. These messages can be printed on any inbound or outbound document (requires special programming by HighJump).
Weight Tolerance Profile 
Code (IWTP)
Reserved for future use
Scan Parameter Code (SCPR)
Optional
If required, the scan parameter code used if you are scanning in your weights or some other process code value from bar coded labels (RF only). 
Location Size Code (LOCS)
Optional
The item’s location size. This field is only used if you are putting away product based on location size.
FIELD DESCRIPTIONS

Put-Away Profile Code (PUPR)
Optional
If you attach a PUPR profile to this item, the item will be put-away according to the options that you defined in your PUPR profile. If you do not attach a PUPR profile to this item, the item will be allocated according to the default PUPR profile (if any) that you attached to DSRP (Depositor Shipping & Receiving).
Pallet Build Restriction 
Code (IPBR)
See Outbound Pallet Building section in the RF Guide.
Cartonization Profile 
Code (ICNP)
See RF Guide.
Country Code (CNTY) Optional
The country in which the item was manufactured. An entry in this field is only required if the item’s country differs from the customer’s country specified in 
CUST.
Kit N = No (default)
Y = Yes
See the kitting section in the Operations 2 Guide for further information.
Order Line Types for Kit 
Components
N = No (default)
Y = Yes
See the kitting section in the Operations 2 Guide for further information.
Processing Area Code (PROA)
Reserved for future use
UPC Optional
The item’s UPC code.
Allow Mixed Pallets in RF Custom use only
Allow Banding Reserved for future use
Banding SKU Class Reserved for future use
FIELD DESCRIPTIONS

Maximum Banding QuantityReserved for future use
Item Value Profile Code Reserved for future use
Item RF Profile Code (MIRP)
See the RF Guide for further information.
Inventory Attribute Profile Code (IAPR)
Optional
See the Inventory Attributes section in the Operations 2 Guide for further information.
Scan Parameter Code for 
Inventory Validation (SCPR)
If you enter a scan parameter code in this field, it will override the customer level default that you established in the Validate Inventory Level from Bar 
Code Using SCPR Code field in MRFP.
Scan Parameter Code for 
Voice (SCPR)
This field allows you to define two SCPR codes for the same item: one for RF scanning and a second one for voice. 
If this field is populated, voice will use this SCPR code rather than the SCPR code in the Scan Parameter Code (SCPR) field. If this field is not populated, voice will use the scan parameter profile in the Scan Parameter Code (SCPR) 
field.
Oversize Flag Only used in A1 Ship integration.
Stackability Indicator 
Code
See the Outbound Pallet Building section in the RF Guide. 
Stackablility Quantity in 
Highest SKU
For outbound stacking, see the Outbound Pallet Building section in the RF 
Guide. For inbound stacking, see the Product Stacking Group (ILOP) in the 
Allocation and Wave Manager Guide.
Pallet Type Height/
Spacer Height
The item’s standard pallet type height and spacer height. The unit of measure for these two fields is the linear measure code selected in the Quantity Breakdown Block for the base SKU. The put-away/directed move engine will consider the height of pallet types and spacers in the calculations for inbound moves, but ignore the height of spacers for inventory moves.
Allocate Pallet by Entity If you set this flag set to Y, when allocation is looking for pallets, all stock for one inventory entity (i.e. one unique inventory level 1, 2, 3, 4) in a location will be treated as a pallet even if the quantity is less than a full pallet or greater than a full pallet. When allocation is not looking for pallets, such stock will be treated as if the flag were set to N.
FIELD DESCRIPTIONS

PROCEDURE
1 Enter ITEM.
2 Click on Enter Criteria then Execute Query to see whether the item has already been set up. If the item has not been set up, click on Create Record.
3 Key in your customer code and press Enter.
4 Key in your item code and press Enter. An item code can consist of any combination of numbers or letters up to 20 characters in length.
5 Key in a description for your item code and press Enter.
6 Press Enter twice to bypass the Master Item and Attached to (ITEM) fields.
7 Use your pick list to select the appropriate general information profile code. To select a code using a pick list, press F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
Velocity Code (IVLP) The item’s velocity code.
Directed Put-Away Zone 
Code (WHZO)
See Allocation and Wave Manager.
Merge Inventory to Location on Replenishment and RFRL
If you select this option, the lowest inventory level of an inventory entity being relocated or replenished to the pick line will be changed to the to location code. For example, if item 1, lot 101, pallet ID 123 is relocated to location 
ABC, it will become item 1, lot 101, pallet ID ABC.
Allow Supvr. Override of 
Min./Max. Expiry/Production Date
An override at the item level of the field of the same name in ITSH.
Minimum Range in Days to Expiry
An override at the item level of the field of the same name in ITSH.
Maximum Range in Days to Expiry
An override at the item level of the field of the same name in ITSH.
Maximum Range in Days from Production Date
An override at the item level of the field of the same name in ITSH.
Labor Standard Modifier See the Operational Board section in the Operations 2 Guide.
Status A = Active
D = Deactivated
If an item is active, you can ship and receive it like any other item. If an item is deactivated, you can ship the item but you cannot receive new inventory for the item.
FIELD DESCRIPTIONS

8 Use your pick list to select the appropriate item billing profile code.
9 Press Enter to bypass the Billing Profile Code 2 and 3 fields.
10 Press Enter to bypass the Extra Charge Profile Code field.
11 Use your pick list to select the following profile codes:
▪ the shipping profile code
▪ the process profile code
▪ the quantity breakdown profile code
▪ the location profile code

Item
12 If you wish to restrict the item to a particular warehouse, enter this warehouse in the Warehouse Code field. If the item can be received in any warehouse or you only have a single warehouse on your system, press Enter to bypass this field.
13 If required, use your pick list to select the appropriate hold profile code. If you do not need a hold profile code, press Enter to bypass this field.
14 If required, key in an alternate description for your item and press Enter. If you do not need an alternate description, press Enter to bypass this field.
15 Use your pick list to select the appropriate commodity code.
16 Press Enter to accept the commodity subcode.
17 In the Entry Required up to Level field, key in the number of inventory levels required for this item and press Enter.
18 Press Enter to accept 0 as the number of days that you want the lot to remain open in the Number of 
Days for Open Lots field and press Enter.

19 Key in the appropriate value in the Variable Quantity Breakdown field (Y for Yes or N for No) and press 
Enter. If you select No, AccellosOne 3PL will use the standard quantity breakdown in ENRE. If you select 
Yes, AccellosOne 3PL will prompt you for the quantity breakdown in ENRE.
20 If you entered Y in the previous field, key in the appropriate value (H for High, L for Low, M for Most or S for Standard) in the Renewal Option for Variable Quantity Breakdown field and press Enter.
21 In the Standard Weight field, key in Y for Yes and press Enter to use the standard weight as defined in 
Quantity Breakdown Block. If you do not want to use a standard weight, press F10 to access a pick list of other weight options.

Item screen showing prompt for tare profile code
22 If required, use your pick list to select the appropriate tare profile code. 
23 Key in the appropriate value in the Cross Dock field and press Enter. If you select No, you will not be able to cross dock the item. If you select Yes, AccellosOne 3PL will permit cross docking of the item.
24 If required, key in a declared value for the item and press Enter or press Enter with the field blank to bypass this option.
25 If you entered a declared value for the item, key in the SKU code that the value applies to and press 
Enter.
26 Use your pick list to select the appropriate hazard code or press Enter to bypass this field.
27 Press Enter to bypass the Cycle Count Profile Code field.
28 Use your pick list to select the appropriate picking profile code or press Enter to bypass this field.
29 In the Item Discount Flag field, key in N for Never and press Enter.

Item screen showing prompt for tax code
30 Use your pick list to select the appropriate tax code.
31 Use your pick list to select the message code or press Enter to bypass this field.
32 Press Enter to bypass the Weight Tolerance Profile Code field.

Item screen showing prompt for scan parameter code
33 If required, use your pick list to select the following optional codes:
▪ scan parameter code
▪ location size code
▪ put-away profile code
▪ country code
34 In the Kit field, key in the N for and press Enter.
35 Press Enter to bypass the Processing Area Code field.
36 If required, key in the item’s UPC code and press Enter.
37 Press Enter the required number of times to bypass the remaining fields in ITEM.
The Quantity Breakdown Block will be displayed. Refer to the section that follows for complete instructions.
QUANTITY BREAKDOWN BLOCK
In this block, you set up: 
▪ the quantity breakdown of the item (that is, the number of units of SKU type X that make up a full SKU type Y)
▪ the layer configuration or tie and hi (optional)
▪ the linear measurements 
▪ the weight 
If you selected a profile in the Quantity Breakdown Profile Code field consisting of a single SKU type (for example, CASES only), AccellosOne 3PL will create a single record in the Quantity Breakdown Block. 

If you selected a profile in the Quantity Breakdown Profile Code field consisting of multiple SKU types (for example, CASES/EACHES or PALLETS/CASES/ EACHES), AccellosOne 3PL will create one record in the 
Quantity Breakdown Block for each SKU type — that is, one for CASES and one for EACHES or one for 
PALLETS, one for CASES and one for EACHES.
When you select a quantity breakdown profile consisting of two or more SKU types, you must specify two things: the number of units of SKU type X that make up a full SKU type of Y and the SKU type that you wish to use to track the item’s weight and size.
CAUTION If you wish to change an item’s quantity breakdown after receiving inventory for that item, refer to “Adjusting an Item’s Quantity Breakdown in AEQB” in the System Administration Guide for further instructions.
FIELD DESCRIPTIONS
SKU Code (SKUS) This value is set by AccellosOne 3PL according to quantity breakdown profile that you defined in IQBP and attached to this item in the Quantity Breakdown 
Profile Code field in this program.
When you first enter the Quantity Breakdown Block, the SKU type of your highest quantity breakdown level is shown.
Quantity Mandatory
If you have a single level quantity breakdown (for example, CASES only), set this field to 1. If your quantity breakdown is CASES/EACHES, you would have two quantities. For your EACHES quantity breakdown, you would enter 1; for your CASES quantity breakdown, you would enter the number of eaches per case (for example, 20 if 20 eaches per case are standard for this item).
If your quantity breakdown were PALLETS/ CASES/EACHES, your quantities would be as follows (example only):
EACHES level = 1 (because lowest level)
CASES level = 10 (10 eaches per standard case)
PALLET level = 60 (60 cases per standard pallet)
NOTE If you are entering the number of layers and the quantity per layer for this quantity breakdown level, the product of the two values (number of layers times quantity per layer) must equal the value that you enter in the Quantity field.

Minimum Quantity Optional
If you enter a minimum quantity in this field, AccellosOne 3PL will not allocate product to an order if the on-hand quantity is less than the minimum quantity. 
You can override minimum quantities for high priority orders by setting the 
Evaluate Minimum flag in ORPR (Order Priorities) to the appropriate value.
A minimum quantity can include more than one SKU in an item’s quantity breakdown. For example, for a pallet/case item you can set up a minimum quantity of one pallet for your pallet SKU and 10 cases for your case SKU. 
AccellosOne 3PL will use the total minimum quantity of all SKU’s — that is, 1 pallet, 10 cases — as the item’s minimum quantity.
Base for Cube/Weight Y = Yes
N = No
If you enter Yes, AccellosOne 3PL will track the item’s weight and cube at this quantity breakdown level. If you enter No, you must specify Yes for another quantity breakdown level.
For example, if the item has a single quantity breakdown level such as 
CASES, you must set this flag to Yes for CASES. If the item’s quantity breakdown is PALLETS/CASES, you must set this flag to Yes for either PALLETS or 
CASES.
If you are setting up a variable quantity breakdown item, you should set this flag to Yes for the lowest SKU.
Whole/Prorate W = Whole (default)
P = Prorate
If you set to Whole, AccellosOne 3PL will round up partial quantities (for example, 1.5 pallets would be billed as two pallets if you were charging by pallet). If you set to Prorate, AccellosOne 3PL will charge for actual quantities stored and will not round up.
FIELD DESCRIPTIONS

Number of Layers Mandatory if you set the Layer Configuration Required Flag to Yes in IQBP
If you set the Layer Configuration Required flag in IQBP to Yes for this quantity breakdown level, you must enter the number of layers or hi for this quantity breakdown level as well as the quantity per layer or tie.
If you set the Layer Configuration Required flag in IQBP to No for this quantity breakdown level, you can press Enter to bypass the layer configuration fields.
NOTE The number of layers times the quantity per layer must always equal the number in the Quantity field.
If you are at your lowest quantity breakdown level or if you do not require layer configuration, set the number of layers and quantity per layer to 1.
Quantity Per Layer Optional
The number of entities or tie per layer.
Quantity Odd Layer Optional
If the number of layers times the quantity per layer does not equal the number in the Quantity field, you must enter the difference in this field so that the quantities balance.
Override Configuration on 
Receipt
Reserved for future use
Volume Measure Code Optional
You can track an item’s volume by entering a volume measure code in this field. 
Volume The item’s volume.
Carton Size Cube Only required if you perform cartonization
The number of units of this item that can fit into a carton.
FIELD DESCRIPTIONS

Linear Measurement 
Code
Mandatory
Feet, inches, meters, etc.
Height Optional
The height of your base quantity breakdown level
Width Optional
The width of your base quantity breakdown level
Length Optional
The length of your base quantity breakdown level
Total Cube Mandatory
If you enter the item’s height, width and length, AccellosOne 3PL will automatically calculate the item’s cube. If you do not enter a height, width and length, enter 1 to bypass the Total Cube field.
Weight Measure Code Mandatory
Pounds, kilograms, tons, etc.
Gross Weight Mandatory
The item’s standard gross weight. If the item has no standard gross weight, enter 1.
Net Weight Mandatory
The item’s standard net weight. If the item has no standard net weight, enter 
1.
FIELD DESCRIPTIONS

PROCEDURE
When you first enter the Quantity Breakdown Block, the SKU type of your highest quantity breakdown level is shown. In the sample screen shown below, the highest quantity breakdown level is PALLET.

Quantity Breakdown Block showing PALLET as the first quantity breakdown level
1 In the Quantity field, key in the appropriate number and press Enter.
2 If required, key in a minimum quantity for this quantity breakdown level and press Enter.
Tare Weight Optional
The item’s tare weight. This weight is only required for non-standard weight options under which the gross or net receipt weight is calculated using the tare weight.
Weight Tolerance % See the RF Guide for further information on catch weight tolerances.
If the quantity breakdown is single level (for example, 
CASES only):
If the quantity breakdown is double-level (for example, 
CASES/EACHES):
If the quantity breakdown is triple level (for example, 
PALLETS/CASES/EACHES):
a) You enter 1. a) You enter the number of eaches per case.
a) You enter the number of cases per pallet.
FIELD DESCRIPTIONS

3 In the Base for Cube/Weight field, key in Y for Yes or N for No to specify whether you want AccellosOne 
3PL to track the item’s size and weight at this quantity breakdown level. If you are entering a single-level quantity breakdown (for example, UNITS), you must enter a Y in this field.
4 In the Whole/Prorate field, key in W for Whole or P for Prorate and press Enter. 
5 If required, key in the number of layers or hi of this quantity breakdown level and press Enter.
6 If required, key in the quantity per layer or tie of this quantity breakdown level and press Enter.
7 If the number of layers times the quantity per layer does not equal the value in the Quantity field, key in the difference in the Quantity Odd Layer field and press Enter.
8 Press Enter to bypass the Override Configuration at Receipt field.
9 If you select No in the Base for Cube/Weight field, AccellosOne 3PL will display the next quantity breakdown level. Repeat the previous steps for the next quantity breakdown level.
If you select Yes in the Base for Cube/Weight field, you must enter the linear and weight measurements for this quantity breakdown level.
10 If required, use your pick list to select the appropriate volume measurement code. Then key in your volume for this quantity breakdown and press Enter.
Quantity Breakdown Block showing PALLET as the base for cube and weight
11 Use your pick list to select the appropriate linear measurement (feet, inches, meters, etc.).
12 Key in the height of the SKU type and press Enter.
13 Key in the width of the SKU type and press Enter.
14 Key in the length of the SKU type and press Enter. AccellosOne 3PL will calculate the cube automatically.
15 Use your pick list to select the appropriate weight measure code (pounds, kilograms, tons, etc.).

16 If there is a standard weight for the item, key in the gross weight of the SKU type and press Enter. If there is no standard weight, you can use 1.
17 If there is a standard weight for the item, key in the net weight of the SKU type and press Enter. If there is no standard weight, you can use 1.
18 If required, key in the tare weight of the SKU type and press Enter.

Quantity Breakdown Block showing PALLET as the base for cube and weight
19 Press Enter to bypass the Weight Tolerance % field.
20 If you are entering a single-level quantity breakdown item, your item is complete. Click on Master Block and Exit to exit.
If you are entering a multi-level quantity breakdown item, AccellosOne 3PL will display the next highest quantity breakdown level. Refer to the table below for further instructions:
If the next highest quantity breakdown level is your last (for example, your breakdown is 
CASES/EACHES and you are at the EACHES level).
Quantity field = 1.
Number Layers and Quantity Per Layer = 1
If you are recording your weight and size at the 
CASE quantity breakdown, the weight and size fields will be bypassed for EACHES.
If the next highest quantity breakdown level is not your last (for example, your breakdown is 
PALLETS/CASES/EACHES and you are at the 
CASE level).
Quantity field = number of eaches per case.
Number Layers = number of layers of eaches in a case
Quantity Per Layer = number of eaches in a layer

Quantity Breakdown Block showing CASE breakdown level
21 Once you have entered all your quantity breakdown levels, click on Master Block and then Exit to exit the program.
CHANGING AN ITEM’S QUANTITY BREAKDOWN
If you wish to change an item’s quantity breakdown (for example, from 50 cases to a pallet to 60) and you want the change to apply to existing inventory, you must run AEQB (Adjust Entity Quantity Breakdown).
CHANGING AN ITEM’S WEIGHT
If you wish to change an item’s weight (for example, from 100 KGS to 90 KGS) and you want the change to apply to existing inventory, you must run RESW (Recalculate Standard Weight).
DELETING AN ITEM
You can delete an item if you have not received any inventory for the item in ENRE or created new inventory in ENAJ. If there are history records for the item, you can deactivate the item but not delete it.
1 Enter ITEM.
2 Retrieve the item that you wish to delete.
3 Press Enter until the Delete button appears.
4 Click on Delete.
5 Click on Exit.

ADDING ADDITIONAL ITEMS
You may use the first item that you set up for this customer as your template for all the other items of this customer.
1 Enter ITEM.
2 Locate the item that you previously set up.
3 Click in the Item Code field.
4 Key in your new item code over the existing item code and press Enter.
5 Key in your new description over the old description and press Enter.
6 Change any information that does not apply to the new item. Some of the profiles or fields that you may have to change are:
▪ Item Quantity Breakdown Profile
▪ Variable Quantity Breakdown
▪ Standard Weight
7 One you are satisfied that you have changed all the required fields and profiles and that the new item is correct, press F12 (Commit).
8 Click on Return to Main to display the new item that you have just committed.
9 Click on Quantity Breakdown to enter the Quantity Breakdown Block of the new item.
You will see the quantities, layer configuration, linear measurements and weight of the original item.
10 Change these quantities, layer configuration, linear measurements and weights for each SKU type as required.
11 Repeat the above steps for each additional item that you wish to add.
12 When you finish entering all your items, click on Master Block and Exit to exit.
ALTERNATE REPORTING BLOCK
In this block, you attach the alternate reporting type codes that you defined in ITAS to the item. When you attach an alternate reporting type code to an item (for example, MEAT), you can run the report program INAS (Inventory Report by Alternate Location). This report will generate a consolidated inventory report showing all meat items regardless of customer to which you have attached the MEAT alternate reporting type code.
You can also use alternate reporting type codes to rename an item and to group items for billing purposes (that is, bill for an entire product line rather than item by item).
1 Enter ITEM.
2 Retrieve the item to which you wish to add the alternate reporting code.
3 Click on Quantity Breakdown Block, Substitute Block and Alternate Reporting Block.
4 Click on Create Record.
5 Use your pick list to select your alternate reporting type code. To select a code using a pick list, press 
F10 to display the pick list and click on Execute Query to retrieve the pick list codes. Then use your arrow keys to position your cursor over the appropriate code and click on Select Code. 
6 Use your pick list to select your alternate reporting code. If you are attaching a single-level reporting type code, you will select the same code that you selected in step 5. If you are attaching a double-level code, you will select the second level of the code that you selected in step 5.

Alternate Reporting Block showing a double-level code — MEAT/PORK
7 If you have another reporting type code to add, repeat steps 5 and 6. 
8 When you finish entering your alternate reporting codes, click on Return to Main to exit create mode. 
Then click on Master Block and Exit to exit ITEM.
HAZARDOUS MATERIAL BLOCK
In the Hazardous Material Block, you define the hazardous material properties of your items. You access the 
Hazardous Material Block by positioning your cursor in the Hazardous Material field, keying in Y for Yes and clicking on Hazardous Material.
AccellosOne 3PL supports the ADR, IATA, DOT and IMO classification systems for hazardous product.

Hazardous Material Block showing various hazmat properties
TRANSPORT MODE BLOCK
In the Transport Mode Block, you can attach a transport mode code — air, sea, ground or all modes — as well as transport mode hazardous properties such as inner packing code type and quantity to an item. The same item can have different transport mode hazardous properties depending on its transport mode code. For example, line 1 is “Sea”, Line 2 is “Air” and Line 3 is “Ground”.
You must save a record in the Hazardous Material Block before you can access the Transport Mode Block by clicking on Details.
FIELD DESCRIPTIONS
Line Number Mandatory
Your line number. You need one line number for each transport mode code.

Transport Mode Block showing item A1 as hazardous when shipped by air transportation
Transport Mode Code (TRMO)
Mandatory
All Modes
Ground
Air
Sea
Your transport mode code.
FIELD DESCRIPTIONS

Hazardous Material Transport block
LANGUAGE BLOCK
In the Language Block, you can define the ADR proper shipping name, hazard text 1, hazard text 2 and hazard text 3 in different languages. You must save a record in the Transport Mode Block before you can access the Language Block.
Language Block showing ENUS proper shipping name and hazard text 1/2/3

NON-STANDARD WEIGHT OPTIONS
AccellosOne 3PL supports a number of different weight options. When receiving product, you can manually enter the unit weight, gross weight or net weight or you can use the item’s tare weight to calculate either the gross weight or the net weight. When shipping product, you can manually enter the product’s gross weight, net weight or both.
You can also combine various inbound and outbound options. For example, you can enter the gross weight and calculate the net weight from the tare weight when receiving and enter the order’s gross weight when shipping.
ENRE Line Block showing all weight fields automatically populated for standard weight item (for nonstandard weight item some or all of these fields are blank and manually enterable)

WEIGHT CODES
A Enter Rcpt Unit Wgt
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will multiply the receipt unit weight by the number of units to arrive at the total gross weight of a receipt line.
This option is not suitable if you wish to track or bill product by net weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.
AT Enter Rcpt Unit Wgt, Calc Rcpt Net Wgt from Tare
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will multiply the receipt unit weight by the number of units to arrive at the total gross weight of a receipt line. The total net weight of the line will be calculated by subtracting the total tare weight from the total gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
B Enter Rcpt Gross Wgt 
With this option, you enter the weight of each receipt line in ENRE. AccellosOne 3PL will calculate the receipt unit weight by dividing the receipt’s gross weight by the number of units received.
This option is not suitable if you wish to track or bill product by net weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.

BT Enter Rcpt Gross Wgt, Calc Rcpt Net Wgt from Tare
With this option, you enter the gross weight of each receipt line in ENRE. AccellosOne 
3PL will calculate the total net weight of the line by subtracting the total tare weight from the total gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
C Enter Rcpt Net Wgt
With this option, you enter the net weight of each receipt line in ENRE. This option is not suitable if you wish to track or bill product by gross weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1*
Tare Weight = N/A
* If required, you can enter an average net weight.
CT Enter Rcpt Net Wgt, Calc Rcpt Gross Wgt from Tare
With this option, you enter the net weight of each receipt line in ENRE. AccellosOne 3PL will calculate the total gross weight of the line by adding the tare weight to the total net weight.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = tare weight
D Enter Rcpt Unit Wgt, Rcpt Net Wgt
With this option, you enter the weight of each unit that you receive in ENRE. AccellosOne 
3PL will calculate the total gross weight of the receipt line. You then enter the total net weight of the line; this weight must be less than or equal to the total gross weight of the line.
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = N/A
WEIGHT CODES

E Enter Rcpt Gross Wgt, Rcpt Net Wgt
With this option, you enter the gross weight and net weight of each receipt line in ENRE. 
Setup in ITEM:
Gross Weight = 1
Net Weight = 1
Tare Weight = N/A
F Enter Ord Gross Wgt
With this option, you enter the gross weight of each order line in ENRE. AccellosOne 3PL will calculate the order unit weight by dividing the order’s gross weight by the number of units shipped.
G Enter Ord Net Wgt
With this option, you enter the net weight of each order line in ENOR. 
H Enter Ord Gross Wgt, Ord Net Wgt
With this option, you enter the gross weight and net weight of each order line in ENOR. 
AccellosOne 3PL will calculate the order unit weight by dividing the order’s gross weight by the number of units shipped.
I Enter Rcpt Unit Wgt, Ord Gross Wgt
See options A and F.
IT Enter Rcpt Unit Wgt, Ord Gross Wgt, Calc Rcpt Net Wgt from Tare
See options AT and F.
J Enter Rcpt Unit Wgt, Ord Net Wgt
See options A and G.
JT Enter Rcpt Unit Wgt, Ord Net Wgt, Calc Rcpt Net Wgt from Tare 
See options AT and G.
K Enter Rcpt Unit Wgt, Ord Gross Wgt, Ord Net Wgt
See options A and H.
WEIGHT CODES

KT Enter Rcpt Unit Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Net Wgt from Tare
See options AT and H.
L Enter Rcpt Gross Wgt, Ord Gross Wgt
See options B and F. 
LT Enter Rcpt Gross Wgt, Ord Gross Wgt, Calc Rcpt Net Wgt from Tare
See options BT and F. 
M Enter Rcpt Gross Wgt, Ord Net Wgt
See options B and G.
MT Enter Rcpt Gross Wgt, Ord Net Wgt, Calc Rcpt Net Wgt from Tare
See options BT and G.
N Enter Rcpt Gross Wgt, Ord Gross Wgt, Ord Net Wgt
See options B and H.
NT Enter Rcpt Gross Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Net Wgt from Tare
See options BT and H.
O Enter Rcpt Net Wgt, Ord Gross Wgt
See options C and F.
OT Enter Rcpt Net Wgt, Ord Gross Wgt, Calc Rcpt Gross Wgt from Tare
See options CT and F. 
P Enter Rcpt Net Wgt, Ord Net Wgt
See options C and G.
PT Enter Rcpt Net Wgt, Ord Net Wgt, Calc Rcpt -Ord Gross Wgt from Tare
See options CT and G.
WEIGHT CODES

Q Enter Rcpt Net Wgt, Ord Gross Wgt, Ord Net Wgt
See options C and H.
QT Enter Rcpt Net Wgt, Ord Gross Wgt/Net Wgt, Calc Rcpt Gross Wgt from Tare
See options CT and H.
S Enter Rcpt Unit Wgt, Rcpt Net Wgt, Ord Gross Wgt
See options D and F.
U Enter Rcpt Unit Wgt, Rcpt Net Wgt, Ord Net Wgt, Ord Gross Wgt
See options D and H.
V Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Gross Wgt
See options E and F.
W Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Net Wgt
See options E and G.
X Enter Rcpt Gross Wgt, Rcpt Net Wgt, Ord Gross Wgt, Ord Net Wgt
See options E and H.
WEIGHT CODES
