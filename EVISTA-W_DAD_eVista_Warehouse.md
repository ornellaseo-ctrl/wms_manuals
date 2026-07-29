# Manual EVISTA-W — e-Vista Warehouse Setup Guide

> **ID do Manual:** EVISTA-W  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Configuração do e-Vista para operações de warehouse: setup de armazém, configurações operacionais, integração com o sistema principal.

---

June 2013
3.2.5.2
90 South Cascade Avenue, Suite 1200
Colorado Springs, CO 80903
www.accellos.com
E‐VISTA
SETUP GUIDE:
WAREHOUSE
ONLY-e 
---

Copyright © Accellos, Inc.
All rights reserved
This manual is reserved for licensed users of AccellosOne 3PL and e-Vista. If you are not a licensed user of 
AccellosOne 3PL and e-Vista, no part of this publication may be reproduced, stored in a retrieval system or 
transmitted in any form or by any means electronic, mechanical, recording or otherwise, without the prior 
written consent of Accellos, Inc.
The information in this manual is furnished for informational use only, is subject to change without notice and 
should not be construed as a commitment of Accellos, Inc. Accellos, Inc. assumes no responsibility or liability 
for any errors or inaccuracies that may appear in this manual.-e 
---

E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 i
TABLE OF CONTENTS
ACCELLOSONE 3PL SETUP 1
Overview ........................................................................................................................................... 2
Example of a Unique Set of Company, Customer and e-Vista Job Restrictions ................. 3
Setting Up 3PL Operators ............................................................................................................... 3
A) Setting Up Your Operators in AccellosOne 3PL ............................................................. 4
B) Assigning Company Access, Operator Access and Operator Restrictions..................... 4
C) Activating Your Operators in ActiveDesktop................................................................... 4
Setting Up Your Defaults in ATMP.................................................................................................. 4
Setting Up Your From E-Mail Address for Scheduled Queries.................................................... 6
Setting Up the POD System ............................................................................................................ 7
Adding POD to Your Outbound Flow Profile ....................................................................... 7
Setting Up POD Access for Carriers ................................................................................... 8
Setting Up POD Access for Warehouse and Client Accounts............................................. 8
Setting Up Reason Codes in REAS .................................................................................... 9
Setting Up Broker Customers....................................................................................................... 10
Setting Up Broker Accounts ..........................................................................................................11
Setting Up Suppression of Flows and Order / Receipt Line Details ......................................... 12
Setting Up Suppression of Documents ....................................................................................... 14
SYSTEM ADMINISTRATION TASKS 15
Understanding Accounts............................................................................................................... 16
Setting Up a New Account ............................................................................................................ 17
Adding Users to an Account......................................................................................................... 23
Removing Users from an Account ............................................................................................... 27
Looking Up Your Accounts ........................................................................................................... 28
Modifying an Account ................................................................................................................... 29
Modifying an Account’s 3PL Operator ............................................................................... 29
Deactivating an Account ............................................................................................................... 30
Deactivating/Deleting an Account Through Activation and Expiry Dates .......................... 31
Deleting an Account with the Delete Command ......................................................................... 31
Deleting and Deactivating Users .................................................................................................. 32
Deactivating Users Through Activation and Expiry Dates ................................................. 33
Looking Up Users .......................................................................................................................... 33
Resetting a User’s Password........................................................................................................ 34-e 
---

ii 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Changing a User’s Access............................................................................................................ 35
Sending E-Mail Messages from e-Vista ....................................................................................... 37
Understanding Session Control ................................................................................................... 38
Deleting a User Session .................................................................................................... 39
Activating and Deactivating Session Control..................................................................... 40
Defining Your Time-Out Interval ........................................................................................ 41
Setting Up Your E-Mailing Options............................................................................................... 42
Setting Up System-Generated E-Mailing........................................................................... 42
Setting Up E-Mail Notification of Submitted Orders and Receipts..................................... 45
Setting Up User-to-User E-Mailing .................................................................................... 45
Using Tokens in e-Vista E-Mail ......................................................................................... 46
Changing Your E-Mail Setups in eVistaWhseParam.xml .................................................. 47
Modifying Scheduled Queries ...................................................................................................... 48
Deactivating Scheduled Queries .................................................................................................. 49
Re-Activating Scheduled Queries ................................................................................................ 50
Looking Up Queries in the Scheduled Query Log ...................................................................... 51
Changing Your Warehouse Setups .............................................................................................. 53
Setting Up Warehouse and Client Logos..................................................................................... 56
Setting Up a Warehouse Logo .......................................................................................... 57
Setting Up a Client Logo.................................................................................................... 58
Deleting a Logo ................................................................................................................. 58
Customizing the Splash Screen ........................................................................................ 59
Customizing the Login Screen Logo and Welcome Message ........................................... 59
Deactivating the Pick Lists/Drop-Down Lists for Shippers and Consignees........................... 60
Working With Multilingual Labels................................................................................................. 61
Non-Multilingual Labels ..................................................................................................... 64
Monitoring e-Vista Users............................................................................................................... 64
OPERATIONAL TASKS 67
Signing on for the First Time ........................................................................................................ 68
Changing Your User Settings ....................................................................................................... 68
Resetting Your Labels to Standard............................................................................................... 70
Looking Up Your Configuration.................................................................................................... 71-e 
---

E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 1
ACCELLOSONE 3PL SETUP
Overview .............................................................................................................. 2
Setting Up 3PL Operators .................................................................................. 3
Setting Up Your Defaults in ATMP .................................................................... 4
Setting Up Your From E-Mail Address for Scheduled Queries....................... 6
Setting Up the POD System ............................................................................... 7
Setting Up Broker Customers.......................................................................... 10
Setting Up Broker Accounts ............................................................................ 11
Setting Up Suppression of Flows and Order / Receipt Line Details............. 12
Setting Up Suppression of Documents .......................................................... 14-e 
---

ACCELLOSONE 3PL SETUP
Overview
2 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Overview
Security access in e-Vista is based on 3PL operators defined in the AccellosOne 3PL program OPER 
(Operator Code). A 3PL operator is a group of e-Visa users with the same security access. For example, if 
your customer has two groups of users — group 1 has look-up access only and group 2 has look up, order 
enter and receipt entry access — you would set up two 3PL operators for this customer in OPER.
You can set up as many e-Vista users as you require for each 3PL operator. Each e-Vista user should have a 
separate login and password, but all e-Vista users assigned to the same operator will share the same access 
restrictions.
There are eight job restrictions in e-Vista defined in the AccellosOne 3PL program JOSE (Job Selection 
Code): 
 EVQRY for all e-Vista queries except invoice queries, broker order queries and inventory history queries
 EVHIST for e-Vista inventory history queries
 EVINVO for e-Vista invoice queries
 EVORD for e-Vista order entry 
 EVRCPT for e-Vista receipt entry 
 EVPOD for e-Vista POD queries/entry
 EVBROK for e-Vista broker order queries
 EVIGO for d’Amigo queries
Programs in A13PL define the company, programs and 
customers that an operator has access to.
e-Visa Client 1
User 1
A13PL operator 1
e-Visa Client 1
User 2
e-Visa Client 1
User 3
OPAC
(Operator 
Access)
OPRS
(Operator 
Restrictions)
Look-Up access only Full access
A13PL operator 2
OPAC
(Operator 
Access)
OPRS
(Operator 
Restrictions)-e 
---

ACCELLOSONE 3PL SETUP
Setting Up 3PL Operators
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 3
The number of 3PL operators required for a particular customer depends on the number of company and 
customer restrictions in AccellosOne 3PL as well as the number of e-Vista job restrictions. You need one 3PL 
operator for each unique set of company, customer and e-Vista job restrictions.
EXAMPLE OF A UNIQUE SET OF COMPANY, CUSTOMER AND E-VISTA JOB 
RESTRICTIONS 
Suppose you have a customer called ABC Freezers and this customer has access to two companies: W1 (for 
production) and T1 (for testing). You want two restrictions for this customer:
 Restriction 1 = W1 + ABC, T1 + ABC (full access)
 Restriction 2 = T1 + ABC (access to training company only for new employees)
In this example, you want four combinations of access: EVQRY, EVORD and EVRCPT, EVQRY only, EVQRY 
and EVORD, and EVQRY and EVRCPT. ABC Freezers has 10 users. The following table shows eight 
possible combinations of access spread over 10 users:
In the above setup, operator ABC3 represents a group of two e-Vista users with identical access. Likewise, 
operator ABC4 represents a second group of e-Vista users with identical access.
Setting Up 3PL Operators
There are three steps to follow in setting up 3PL operators:
Restr. 1
EVQRY
Restr. 1
EVINVO
Restr. 1
EVORD
Restr. 1
EVRCPT
Restr. 2
EVQRY
Restr. 2
EVINVO
Restr. 2
EVORD
Restr. 2
EVRCPT Operator
User 1 x x x ABC1
User 2 x ABC2
User 3 x x ABC3
User 4 x x "
User 5 x x ABC4
User 6 x x "
User 7 x x x ABC5
User 8 x ABC6
User 9 x ABC7
User 10 x x ABC8-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Your Defaults in ATMP
4 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
 you set up your operators in OPER
 you assign company access, operator access and operator restrictions in OPAC and OPRS
 you activate your operators in Active Desktop
Refer to the System Administration Guide for further information on setting up operators and giving these 
operators access to particular companies and customers.
A) SETTING UP YOUR OPERATORS IN ACCELLOSONE 3PL
You set up your operators in AccellosOne 3PL in the program OPER (Operator Code). You need one 
operator in AccellosOne 3PL for each unique set of company, customer and e-Vista job restrictions.
For example, if you are setting up three operators for ABC Foods, you might set up ABCFOOD1, ABCFOOD2 
and ABCFOOD3 in OPER.
B) ASSIGNING COMPANY ACCESS, OPERATOR ACCESS AND OPERATOR 
RESTRICTIONS
1 Give each operator access to the required job selection codes in OPAC.
2 Set up your company and customer restrictions in OPRS for each operator.
3 If you use the POD system, set up your operator/carrier restrictions in OPRS.
4 If you are setting up broker customers, see “Setting Up Broker Customers” on page 10. If you are setting 
up a broker account, see “Setting Up Broker Accounts” on page 11.
C) ACTIVATING YOUR OPERATORS IN ACTIVEDESKTOP
1 Log onto ActiveDesktop and proceed to change the operator’s password.
Setting Up Your Defaults in ATMP
If your customer is using e-Vista for receipt or order creation, you must set up defaults in ATMP (Action 
Template Setup) for your shipper code, carrier code, consignee code, etc. These defaults are used when 
your customer enters an inbound receipt or outbound order and fails to enter a value in a mandatory field. For 
example, if you define UNKNOWN as your default carrier in ATMP and your customer enters an inbound 
receipt without a carrier, ATMP will assign the carrier UNKNOWN to the receipt.
Defaults can be company specific or can apply to all companies by using the .ALL code. All defaults set up in 
ATMP must be entered in uppercase letters and must be defined in the appropriate AccellosOne 3PL setup 
program.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Your Defaults in ATMP
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 5
The following table shows the fields in ATMP that require setup.
1 Enter ATMP.
2 Retrieve the block code E_ORD_H (Order Header).
3 Click on Detail Block.
4 Position your cursor on the CON_CODE (Consignee) field code.
5 Make sure that the Req. and Def. fields are set to Y for Yes.
6 Click on Company Block to enter the Company Block.
7 Click on Create Record.
8 Enter your company code and default consignee code. If your default consignee code applies to all companies, key in .ALL as your company code.
9 Repeat the above steps for the SOLDTO_CODE, FRT_TERM_CODE, ORD_PRTY_NUM, 
CARR_CODE and LOAD_TP_CODE fields.
Order Entry (E_ORD_H) Receipt Entry (E_RCPT_H)
CON_CODE (defined in CONS)
SOLDTO_CODE (defined in SOLD)
FRT_TERM_CODE
ORD-PRTY_NUM
CARR_CODE (defined in CARR)
LOAD_TP_CODE (defined in LOAD)
SHIP_CODE (defined in SHIP)
CARR_CODE (defined in CARR)
RCPT_PRTY_NUM
LOAD_TP_CODE (defined in LOAD)
NOTE Make sure that you enter your consignee code(s) in uppercase letters only. 
e-Vista will not work properly if you use any lowercase letters in ATMP. All codes must 
be spelled correctly as neither ATMP nor e-Vista performs any validation. As well, any 
code that you enter in ATMP must be set up in the appropriate AccellosOne 3PL 
setup program.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Your From E-Mail Address for Scheduled Queries
6 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Action Template Setup (ATMP) screen showing UNASSIGNED as the default carrier code for all companies when submitting an outbound order
10 Press F4 until your cursor is positioned in the Header Block and then retrieve the block E_RCPT_H 
(Receipt Header).
11 Set up your inbound receipt defaults for the SHIP_CODE, CARR_CODE, RCPT_PRTY_NUM, 
CUST_CODE_BILL_TO and LOAD_TP_CODE fields.
12 When you finish setting up your defaults in E_ORD_H and E_RCPT_H, press F4 the required number of 
times to exit ATMP.
Setting Up Your From E-Mail Address for Scheduled Queries
Scheduled queries require a from address defined in InitialProperties. txt that is used for all scheduled 
queries regardless of the user who set up the query. This address can be a real e-mail address or can be a 
dummy address such as e-Vista@anywarehouse.com.
1 Go to the directory $E_VISTA_HOME/build/config and open the file InitialProperties.txt.
2 In the FromEmailAddress field, enter your from e-mail address for scheduled queries.
3 Save your changes.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up the POD System
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 7
4 Reboot the server.
Setting Up the POD System
The POD system requires a separate 3PL operator and a separate account for each carrier using POD. 
There are four steps to follow in setting up the POD system:
 you add POD to your outbound flow profile in DIFP 
 you set up your 3PL operator for the carrier
 you define your carrier restrictions for the operator in OPRS
 you define your reason codes in REAS
ADDING POD TO YOUR OUTBOUND FLOW PROFILE
You must add POD to the outbound flow profile of each customer whose orders will be tracked in e-Vista’s 
POD system.
1 If required, create a flow called POD in FLPR (Flow Process).
2 Attach this flow to your outbound flow profile in DIFP after the flow COOR (Confirm Order).
NOTE If the from address is defined as a real e-mail address, the recipient of an email message from an e-Vista scheduled query can reply to the message in the normal manner. If, however, the from address is defined as a dummy e-mail address, the 
recipient cannot reply to the message. This means that if you send a message to an 
incorrect address, you will receive no notification of non-delivery from the e-mail 
server.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up the POD System
8 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Depositor Workflow Profile (DIFP) screen showing flow POD after flow COOR
SETTING UP POD ACCESS FOR CARRIERS
POD access requires a separate 3PL operator for each carrier. 
1 Set up a 3PL operator in OPER for each carrier.
2 Give each 3PL operator access to the job selection code EVPOD in OPAC (Operator Access). Access to 
EVQRY, EVORD, EVRCPT and EVINV should NOT be given to carriers.
3 In OPRS set up your company and customer restrictions for the 3PL operator in the normal manner. If 
the carrier will be used by multiple customers, you must give the operator access to each customer.
4 Set up your operator/carrier restrictions in OPRS.
5 Set up an account for each carrier and add one non-system administrator user to the account. If session 
control is activated, you need to set up one user for each carrier employee using the POD system. If session control is NOT activated, multiple carrier employees can use the same e-Vista login. (See “Understanding Accounts” on page 16 for further information on setting up accounts and users.) 
SETTING UP POD ACCESS FOR WAREHOUSE AND CLIENT ACCOUNTS
1 Add the EVPOD job selection code to the 3PL operator in OPAC (Operator Access).
2 Set up your operator/carrier restrictions in OPRS.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up the POD System
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 9
SETTING UP REASON CODES IN REAS
You set up your reason codes in REAS (Entry Reason Code). You use reason codes when submitting POD’s 
in which the appointment date does not equal the to arrive date or the delivery date/time does not equal the 
appointment date/time.
1 Enter REAS.
Entry Reason Code (REAS) screen
2 Press F1 then F2 to see which reason codes have already been set up.
3 If the code that you require has not been set up, click on Create Record.
4 Key in your reason code and press Enter.
5 Key in a description for your new code and press Enter.
6 Press Enter to bypass the External Reference field.
7 Key in E as your type and press Enter.
8 Key in CARR as your attached to value and press Enter.
9 Repeat the above steps for each additional reason that you wish to set up.
10 When you finish setting up your reason codes, click on Return to Main to exit create mode.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Broker Customers
10 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Entry Reason Code (REAS) screen showing two carrier-type reason codes for the POD system
11 Click on Exit to exit REAS.
Setting Up Broker Customers
Broker customers are warehouse customers whose product is shipped by a broker account.
1 Set up a client account for the customer whose product will be shipped by a broker account.
2 Set up a 3PL operator for the broker customer. In OPRS give this operator access to the appropriate 
company and the broker customer. 
3 In OPAC give the 3PL operator access to the EVQRY and EVBROK tabs. If the broker customer requires 
access to order entry, receipt entry or invoice look-up, give the operator access to the appropriate tabs.
4 Set up your users for the client account. 
CAUTION Do not give the operator access to the broker account. If you do, the 
operator may be able to see inventory belonging to other warehouse customers using 
the same broker account.-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Broker Accounts
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 11
EXAMPLE
Broker 1 is authorized to ship product for ABC Freezers, Northwest Cold Storage and 
Eastern Fish. You would set up three accounts for each of your customers. Each account 
would be assigned a separate 3PL operator. The operator for ABC Freezers would have 
access to ABC Freezers only. The operator for Northwest Cold Storage would have access 
to Northwest Cold Storage only and the operator for Eastern Fish would have access to 
Eastern Fish only.
Setting Up Broker Accounts
A broker account is a customer who is authorized to ship product belonging to broker customers. Refer to the 
table below for the various setup options available for broker accounts:
If … and … e-Vista setup
broker account has no inventory 
of his own and merely ships the 
inventory of other broker customers
N/A e-Vista Jobs
EVQRY
OPRS Setup
access to broker account only
NOTE broker account will have no 
access to the inventory details and 
item setup of the product being 
shipped
broker account has inventory of 
his own and also ships the inventory of other broker customers
you do NOT want the broker 
account to have full access to 
the inventory details and item 
setup of the broker customers 
whose product is being 
shipped
e-Vista Jobs
EVQRY, EVBROK
OPRS Setup
access to broker account only
NOTE broker account cannot create outbound orders for broker customer in Create Outbound Order-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Suppression of Flows and Order / Receipt Line Details
12 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Setting Up Suppression of Flows and Order / Receipt Line Details
You can suppress the display of entire flows as well as order and receipt detail lines in the Order Time and 
Receipt Time Blocks. This suppression applies to e-Vista client accounts only; warehouse users will continue 
to see all flows and any documents attached to these flows in e-Vista.
The purpose of suppression is twofold. First, it allows you to suppress receipt/order lines details that are of no 
interest to your clients. Second, it allows you to suppress confidential documents that you do not want your 
clients and carriers to see.
If you suppress the display of a flow, the flow will not be seen by any e-Vista client accounts. If you suppress 
the display of a detail line, order and receipt lines (for example, line 3 of a given order was picked at 10:00 am 
or the load sheet was printed 4:30 pm) will not be seen by any e-Vista client accounts.
You set up your suppression options in FLPR by setting the flag Suppression Rules for e-Vista Client 
Accounts to the appropriate value: 
 if you set this flag to H for Header, the flow will be suppressed
 if you set this flag to D for Detail, receipt/order detail lines will be suppressed 
 If you leave this field blank, no suppression will take place and e-Vista client accounts will see everything
broker account has inventory of 
his own and also ships the inventory of other broker customers
you want the broker account 
to have full access to the 
inventory details and item 
setup of the broker customers 
whose product is being 
shipped
e-Vista Jobs
EVQRY, EVBROK
OPRS Setup
access to broker account and 
access to broker customers that 
broker account is authorized to ship
NOTE: broker account cannot create outbound orders for broker customer in Create Outbound Order
If … and … e-Vista setup-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Suppression of Flows and Order / Receipt Line Details
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 13
FLPR showing e-Vista Suppression Rules for e-Vista Client Accounts flag set to H for Header
Order Time Block for warehouse account showing detail lines, flows and documents not seen by client 
accounts-e 
---

ACCELLOSONE 3PL SETUP
Setting Up Suppression of Documents
14 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Setting Up Suppression of Documents
You can suppress the display of a document for all e-Vista client accounts by setting the flag in DOCU called 
Suppress Display in e-Visa for Client Accounts to Y for Yes.
DOCU screen showing document suppression activated for the BOL document-e 
---

E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 15
SYSTEM ADMINISTRATION TASKS
Understanding Accounts ................................................................................. 16
Setting Up a New Account ............................................................................... 17
Adding Users to an Account............................................................................ 23
Removing Users from an Account .................................................................. 27
Looking Up Your Accounts.............................................................................. 28
Modifying an Account....................................................................................... 29
Deactivating an Account .................................................................................. 30
Deleting an Account with the Delete Command............................................. 31
Deleting and Deactivating Users ..................................................................... 32
Looking Up Users ............................................................................................. 33
Resetting a User’s Password........................................................................... 34
Changing a User’s Access ............................................................................... 35
Sending E-Mail Messages from e-Vista .......................................................... 37
Understanding Session Control ...................................................................... 38
Setting Up Your E-Mailing Options ................................................................. 42
Modifying Scheduled Queries.......................................................................... 48
Deactivating Scheduled Queries ..................................................................... 49
Re-Activating Scheduled Queries ................................................................... 50
Looking Up Queries in the Scheduled Query Log ......................................... 51
Changing Your Warehouse Setups ................................................................. 53
Setting Up Warehouse and Client Logos........................................................ 56
Deactivating the Pick Lists/Drop-Down Lists for Shippers and Consignees..
60
Working With Multilingual Labels.................................................................... 61
Monitoring e-Vista Users.................................................................................. 64-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Accounts
16 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Understanding Accounts
Security in e-Vista is based on accounts. Each e-Vista user must be attached to the appropriate account 
before being able to log on. There are two kinds of accounts in e-Vista: a single warehouse account and 
multiple client accounts. A warehouse account is an account used by employees of the warehouse. A client 
account is an account used by employees of your customers.
The single warehouse account on your system is preinstalled and you cannot modify or delete it. Client 
accounts, on the other hand, can be added, modified and deleted as required. You must set up one client 
account for each customer using e-Vista.
The following diagram shows the relationships between a warehouse account, multiple client accounts and 
various users attached to these accounts.
If required, you can share the same 3PL operator across multiple accounts. In the following diagram, 3PL 
operator 301 is assigned to two accounts: Account 1 and Account 3.
Warehouse 
Account
Client 
Account 1
User 1
User 2
User 3
Client
Account 2
Client 
Account 4
Client 
Account 3
User 1
User 2
User 3
User 1
User 2
User 3
User 1
User 2
User 1
User 2
User 3
User 4
3PL Operator 102
3PL Operator 101
3PL Operator 201
3PL Operator 202
3PL Operator 301
3PL Operator 501 3PL Operator 401
3PL Operator 502-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 17
User access in e-Vista is determined by two settings: the user’s 3PL operator and the user’s system 
administrator status.
The 3PL operator is set up in OPER (Operator Code) in AccellosOne 3PL. See “Overview” on page 2 for 
further information on 3PL operators.
There are two types of users in e-Vista: system administrators and non-system administrators. 
System administrators can set up new users, delete users, reset passwords and perform a number of other 
system administration tasks. Non-system administrators are limited to changing their user name, passwords, 
e-mail address and other parameters. All other tasks must be performed by a system administrator.
If your customers set up their own users, you must create at least one system administrator for each 
customer. If your customers do not set up their own users, you must create at least one non-system administrator user for each customer. Unique users for each employee of each customer are only required if you 
have activated session monitoring. See “Understanding Session Control” on page 38 for further information 
on this topic.
Setting Up a New Account
When you set up a new account, you define the name of the account as well as the account’s 3PL operators. 
If required, the same 3PL operator can be attached to multiple accounts. You also specify whether the 
Client 
Account 1
Client
Account 2
Client 
Account 4
Client 
Account 3
User 1
User 2
User 3
User 1
User 2
User 3
User 1
User 2
User 1
User 2
User 3
User 4
3PL Operator 201
3PL Operator 202
3PL Operator 301
3PL Operator 501 3PL Operator 401
3PL Operator 301-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
18 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
account can set up new users; if the account cannot set up new users, the warehouse must assume this 
responsibility.
NOTE An account is always restricted to a specific environment. If the same customer operates in two environments, you must create the account and its related 
users twice — once for each environment.
Field Descriptions
Account Name Mandatory
The name of the new account. Account names can consist of 
any combination of numbers or letters. Special characters such 
as #, &, %, etc. are not valid. Nor can you use periods, commas 
or embedded spaces.
Logo File Name Optional
See “Setting Up Warehouse and Client Logos” on page 56.
Maximum Number of 
Users Allowed
Only available if session control is activated
The maximum number of users that can use e-Vista at any 
given time. This limit is per account and per environment.
The maximum number of users does not include the system 
administrator working in the Administrator tab of e-Vista. For 
example, if your limit is five users and five users are currently 
logged on to e-Vista, a sixth user — if he or she is a system 
administrator — can log on. However, the sixth user is restricted 
to the Administrator tab and cannot perform queries, enter 
inbound receipts, etc.
If you leave this field blank, there will be no limit on the maximum number of e-Vista users.
See “Activating and Deactivating Session Control” on page 40 
for instructions on activating this feature.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 19
Administrator PrivilegesY = Yes
N = No
If you set this flag to Y for Yes, the client can set up e-Vista 
users and upload a logo to an account. If you set this flag to N 
for No, the client will not be able to set up e-Vista users and 
upload a logo to an account. When you select the No option, 
any existing users for that account with system administrator 
privileges will lose those privileges.
Process Holds PrivilegesY = Yes
N = No
If you set this flag to Y for Yes, the account can place product in 
the warehouse on hold in the Inventory Balances tab. If you set 
this flag to N for No, the account cannot place product in the 
warehouse on hold in the Inventory Balances tab. 
Job Scheduling PrivilegesY = Yes
N = No
If you click on Yes, the account can set up and maintain scheduled queries. If you click on No, the account cannot set up and 
maintain scheduled queries. The default value of this flag is No; 
it must be set to Yes by a system administrator before e-Visa 
users can set up and maintain scheduled queries.
Status Activated
Deactivated
If you set an account’s status to Activated, any user belonging 
to the account will be able to log on to e-Vista. If you set an 
account’s status to Deactivated, any user belonging to the 
account will not be able to log on until you change the account’s 
status to Activated.
The status of an account overrides the status of a user. If a user 
is activated, but the account to which he or she belongs is deactivated, the user will not be able to log on.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
20 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Suppress Display of 
Pre-Built Kits
Yes
No
If you select Yes, users attached to the account cannot look up 
pre-built kits in Order Search or the corresponding kit-type 
receipts in Receipt Search. Nor can they access the order/
receipt details in Inventory Search/Inventory History.
If you select No, users attached to the account will have full 
access to pre-built kits.
Account Activation 
Date/Account Expiry 
Date
Optional
If you define account activation and/or account expiry dates, 
any user belonging to the account will only be able to log on to 
e-Vista between those dates. If you do not define account activation and expiry dates, any user belonging to the account will 
be able to log on to e-Vista at any time.
If the user has a user activation date or a user expiry date, any 
dates at the account level will override the dates at the user 
level.
Rows Per Page Optional
The maximum number of rows that e-Vista will display on a single page after performing a query. If the number of rows 
retrieved in a query exceeds this number, e-Vista will create a 
second page for the excess rows. If you set this value to a large 
number (say, 1,000), you can print the entire query results on a 
single HTML page.
This value overrides the system default defined in eVistaWhseParam.xml.
If the rows per page value of a user’s account differs from the 
rows per page value of the user, the user value overrides the 
account value.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 21
1 Click on Administration.
Administration tab
2 Click on New Account.
Rows Per Query Optional
The maximum number of records that e-Vista will retrieve in a 
query (excluding pick list queries for consignees and items). If 
the number of records retrieved in a query exceeds this number, 
e-Vista will display the number of records retrieved and prompt 
you to narrow your search.
This value overrides the system default defined in eVistaWhseParam.xml.
Time-Out Interval (in 
minutes)
Optional
The number of minutes of no activity on the part of an e-Vista 
user that is allowed before the user is automatically logged off. 
This value overrides the system default defined in eVistaWhseParam.xml.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up a New Account
22 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Create Account window
3 Key in your account name.
4 If prompted to do so, key in a value in the Maximum Number of Users Allowed field if you wish to define 
a maximum.
5 If required, change the Administrator Privileges flag to No.
6 If required, change the Process Holds Privileges flag to Yes.
7 If required, change the Job Scheduling Privileges flag to Yes.
8 If required, change the Suppress Display of Pre-Built Kits flag to Yes.
9 If required, select an activation date and/or expiry date for the account.
10 If required, enter a value or values in the Rows Per Page, Rows Per Query and Time-Out Interval fields.
11 Click on Save.
12 Click on Attach 3PL Operators.
13 Click on Add 3PL Operator.
Attach 3PL Operator to new account
14 Select the appropriate operator from the drop down list and click on Save.
15 Repeat the above step for each additional operator that you wish to attach to the account.
CAUTION It is extremely important to attach the correct 3PL operator to your 
account. If you select the wrong operator, users attached to the account may have 
access to data that he or she should not see.-e 
---

SYSTEM ADMINISTRATION TASKS
Adding Users to an Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 23
16 If the View Multiple Accounts button appears, click on it to see all accounts to which this operator is 
attached. When you have viewed all accounts for this operator, click on Close to close the Multiple 
Accounts window.
If the same 3PL operator is attached to two or more accounts, all e-Vista users belonging to those 
accounts will have the same access.
17 Click on Return to Edit Account Settings.
Adding Users to an Account
There are six parameters that you must define for a new e-Vista user:
 the user’s account
 a user code
 a user name
 a user e-mail address
 a 3PL operator
 the user’s system administrator status
If your customers set up their own users, you must create at least one system administrator for each 
customer account. If your customers do not set up their own users, you must create one non-system administrator user for each employee of each customer account.
Field Descriptions
User Code Mandatory
The code of the new user. User codes can consist of any combination of numbers or letters. Special characters such as #, &, %, 
etc. are not valid. Nor can you use periods, commas or embedded spaces.
NOTE This code must be unique across e-Vista for all 
accounts. If you receive the message “user already exists” 
when you try to add a new user, this means that the user is 
already set up. The user could be set up in the account that you 
are currently working on or in another account.
User Name Mandatory
The name of the new user.-e 
---

SYSTEM ADMINISTRATION TASKS
Adding Users to an Account
24 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Password This field is preset to “changeIt” and cannot be modified when 
setting up a new user.
Language Code The new user’s language.
e-Mail Address Mandatory
The new user’s e-mail address. If the user e-mails a query, the 
address that you enter in this field will be the user’s from 
address.
A valid e-mail address is required to receive system-generated 
e-mails such as “e-Vista is now running” and user-to-user emails sent by the system administrator.
3PL Operator Mandatory
This field controls which functions in e-Vista the new user will be 
able to perform. There are four possible functions in e-Vista: 
looking up orders, receipts, inventory and items, entering an 
inbound receipt, entering an outbound order or looking up an 
invoice.
CAUTION It is important to attach the correct 3PL operator to 
the new user. If you attach the wrong operator to the user, that 
user might not have access to the correct tabs and functions in 
e-Vista or might be able to see data that he or she should not 
see.
Administrator Administrator privileges are only available if the Administrator 
Required flag for the account is set to Y for Yes
Yes
No
If you set this flag to Y for Yes, the new user will have administrator privileges. If you set this flag to N for No, the new user will 
be a regular operator with no administrator privileges.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Adding Users to an Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 25
1 Click on Administration.
Hold Processing 
Privileges
Hold processing privileges are only available if the Hold Processing Privileges flag for the account is set to Y for Yes
None
Put on Hold and Take off Hold
Put on Hold Only
Take off Hold Only
The user’s hold processing privileges.
NOTE The 3PL operator that the e-Vista user is attached to 
must be attached to a single company/customer in ORPS; eVista hold processing does not support multiple companies or 
customers for the 3PL operator.
Status Activated
Deactivated
If you set a user’s status to Activated, the user will be able to log 
on to e-Vista. If you set a user’s status to Deactivated, the user 
will not be able to log on until you change his or her status to 
Active.
User Activation Date/
User Expiry Date
Optional
If you define user activation and/or user expiry dates, the user 
will only be able to log on to e-Vista between those dates. For 
example, if June 1 is your activation date and June 5 is your 
expiry date, the user will be able to log on at 12:01 am on June 
1 and will lose his or her access at midnight on June 5. If you do 
not define user activation and expiry dates, the user will be able 
to log on to e-Vista at any time.
If the account that you are assigned has an account activation 
date or an account expiry date, these dates override any dates 
that you enter in the User Activation Date and User Expiry Date 
fields.
See “Deactivating Users Through Activation and Expiry Dates”
on page 33 for further information on expiry dates.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Adding Users to an Account
26 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Administration tab
2 Select the appropriate account.
3 Click on New User.
Create User screen
4 Key in your user code.
5 Key in your user name.
6 If required, select a language other than the default language from the drop down list.
7 Key in the e-mail address of the new user.
8 Key in your 3PL operator for the new user or select the appropriate operator from the drop down list. If 
the account is restricted to a single 3PL operator, the value in this field will be preset and you will not be 
able to modify it.
9 Select the appropriate administrator option.
10 Click on Save to save your changes.
11 Click on New User to add another user to the same account or click on Return to Select Option to exit.-e 
---

SYSTEM ADMINISTRATION TASKS
Removing Users from an Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 27
Removing Users from an Account
1 Click on Administration.
2 Select the account to which the user is attached from the Account drop down list and click on User 
Search.
3 Do one of the following:
Users List window
4 Click on the user that you wish to remove.
Edit User Settings window
5 Click on Delete User.
To retrieve all users attached to 
this account:
To retrieve a specific user 
attached to this account:
a) Click on Search Registered 
Users.
a) Key in the appropriate user code, 
user name, e-mail address or 
3PL operator.
b) Click on Search Registered 
Users. -e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Your Accounts
28 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
6 Click OK when prompted to confirm the deletion.
7 Click on Return to Select Option to exit.
Looking Up Your Accounts
When you look up an account, e-Vista shows the account name, its type (warehouse or client), whether it is 
active, the maximum number of users allowed (if applicable), the number of active users and the number of 
registered users that are attached to it. If there are no registered users attached to an account, the word 
“Delete” will appear instead of the number of users.
When looking up accounts, you can also look up the settings of each user attached to the account.
1 Click on Administration.
2 Click on Account Search.
Account Search
3 If you wish to restrict your search by account name, key in the account name. You can also use the wildcard character (%) when performing searches; refer to the “Using Wildcards” section in the e-Vista User 
Guide for further information on this function.
4 If you wish to restrict your search by account type or status, select the appropriate type or status from the 
drop down list.
5 When you finish entering your search parameters, click on Search.
Accounts List window showing four accounts
6 Click on the numbered button in the Registered Users column to see which users are attached to the 
account.-e 
---

SYSTEM ADMINISTRATION TASKS
Modifying an Account
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 29
Users List window
7 You can sort your users in either ascending or descending order by any column in the Users List window. 
Click on Ascending or Descending then click on the column heading by which you wish to sort.
8 If you wish to look up the settings of a user, click on the appropriate user code. When you finish looking 
up your user, click on User Search to exit.
9 Click on Return to Select Option to exit.
Modifying an Account
When you modify an account, the change takes effect the next time that any user attached to the account 
attempts to log on. If the account has an activation or expiry date, this date must be removed or a new one 
entered before you can modify the account.
1 Click on Administration.
2 Select the account that you wish to modify from the Account drop down list and click on Account Search.
Accounts List window
3 Click on the account name that you wish to modify.
4 Proceed to make your changes to the Edit Account Settings screen.
5 Click on Save to save your changes.
6 Click on Return to Select Option to exit.
MODIFYING AN ACCOUNT’S 3PL OPERATOR
Before you can change an account’s 3PL operator, you must make sure that there are no users attached to 
the account. If there are, you must remove the users from the account first and then proceed to modify the 
3PL operator.
1 Click on Administration.
2 Select the account whose 3PL operator you wish to modify from the Account drop down list and click on 
Account Search.-e 
---

SYSTEM ADMINISTRATION TASKS
Deactivating an Account
30 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Accounts List window
3 Click on the account name.
4 Click on Attach.
5 Click on Delete.
6 Click on Add 3PL Operator.
7 Select your new 3PL operator from the drop down list and click on Save.
8 Click on Return to Edit Account Settings.
9 Click on Return to Select Option to exit.
Deactivating an Account
When you deactivate an account, that account remains in e-Vista but users attached to it cannot log on. 
Deactivated accounts must be reactivated before the users attached to it can use e-Vista again. You 
reactivate an account by clicking in the Activated check box.
1 Click on Administration.
2 Select the account that you wish to deactivate from the Account drop down list and click on Account 
Search.
Accounts List window
3 Click on the account name.
4 In the Status field, click on Deactivated.
5 Click on Save.
6 Click on Return to Select Option to exit.
NOTE When you deactivate an account, the change takes effect the next time that 
any user attached to the account attempts to log on.-e 
---

SYSTEM ADMINISTRATION TASKS
Deleting an Account with the Delete Command
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 31
DEACTIVATING/DELETING AN ACCOUNT THROUGH ACTIVATION AND EXPIRY 
DATES
You can automatically deactivate or delete an account by defining an account expiry date for the account on 
the Edit Account Settings screen. For example, suppose you have a new prospect for e-Vista and you wish to 
give them e-Vista free of charge for a two-week trial period. You set up an account for the new prospect and 
define September 1 as the account activation date and September 14 as the account expiry date.
On September 15, one of the following will occur:
 If the warehouse has set the Accounts/Users Cleanup Mode flag to delete, the account as well as all 
users belonging to it will be deleted.
 If the warehouse has set the Accounts/Users Cleanup Mode flag to deactivate, the account will remain 
in e-Vista but no user belonging to it will be able to log on.
You can look up the current setting for this flag by clicking on Show Configuration and paging down to the 
Warehouse Setups section of the file. 
Warehouse Setups showing Accounts/Users Cleanup Mode set to Delete
Deleting an Account with the Delete Command
Before you delete an account with the Delete command, you must make sure that there are no users 
attached to it. If there are, you must remove the users from the account first and then proceed to delete it.
1 Click on Administration.
2 Select the account that you wish to delete from the Account drop down list and click on Account Search.
Accounts List window
3 Click on Delete.
4 Click OK to confirm deletion of the account.
5 Click on Return to Select Option to exit.
TIP You can also delete an account through activation and expiry dates. This 
method of deletion does not require that you remove all users from the account 
before you delete it.-e 
---

SYSTEM ADMINISTRATION TASKS
Deleting and Deactivating Users
32 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Deleting and Deactivating Users
When you delete a user, that user is permanently removed from e-Vista. When you deactivate a user, that 
user remains in e-Vista but cannot log on. Deactivated users must be reactivated before they can use e-Vista 
again. You reactivate a user by changing his or her status from “Deactivated” to “Activated”.
Deleting and deactivating users can only be performed by system administrators. You cannot delete or 
deactivate yourself; this must be done by another system administrator.
1 Click on Administration.
2 If required, select the appropriate account from the drop down list.
3 Click on User Search.
4 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
5 If you wish to restrict your search by administrator status or activated/deactivated status, click on the 
appropriate button.
6 When you finish entering your search parameters, click on Search Registered Users.
Users List window
7 Click on the user that you wish to delete or deactivate.
Edit User Settings window-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Users
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 33
8 Do one of the following:
9 Click on Return to Select Option to exit.
DEACTIVATING USERS THROUGH ACTIVATION AND EXPIRY DATES
You can automatically deactivate a user by defining a user expiry date for the user on the Create User 
screen. For example, suppose you hire a temporary employee who is to start on September 1 for a two-week 
period. You define September 1 as his or her activation date and September 14 as the expiry date.
On September 15, one of the following will occur:
 If the warehouse has set the Accounts/Users Cleanup Mode flag to delete, the user will be deleted.
 If the warehouse has set the Accounts/Users Cleanup Mode flag to deactivate, the user will remain as a 
registered user in e-Vista but will not be able to log on.
You can look up the current setting for this flag by clicking on Show Configuration and paging down to the 
Warehouse Setups section of the file. 
Warehouse Setups showing Accounts/Users Cleanup Mode set to Deactivate
Looking Up Users
You can look up registered users or you can look up active users. A registered user is a user defined in the 
Administration tab of e-Vista. A registered user may have a status of either activated or deactivated. An 
active user is a user who is currently signed on to e-Vista.
You must have system administrator privileges to perform this function. If you wish to look up your own 
settings, refer to the section “Changing Your User Settings” on page 68.
1 Click on Administration.
If you wish to delete the user:
If you wish to deactivate the 
user:
a) Click on Delete User.
b) Click OK when prompted to confirm the deletion.
a) Click on Deactivated.
b) Click on Save.
NOTE When you look up users, your search is restricted to users in the environment to which you are currently logged in. If you operate in two environments, you 
must log in separately to each one in order to see all your e-Vista users.-e 
---

SYSTEM ADMINISTRATION TASKS
Resetting a User’s Password
34 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or active/deactivated status, click on the appropriate button.
5 When you finish entering your search parameters, click on Search Registered Users or Search Active 
Users.
Users List window showing registered users
6 You can sort your users in either ascending or descending order by any column in the Users List window. 
Click on Ascending or Descending then click on the column heading by which you wish to sort.
7 Click on the user that you wish to look up.
8 When you finish looking up your user, click on Return to Select Option to exit.
Resetting a User’s Password
If a user forgets his or her password, the system administrator must reset it. When you reset a user’s 
password, that user will be required to follow the steps described in the section “Signing on for the First Time”
on page 68.
Resetting a user’s password may trigger an automatic e-mail to the user if you have activated this feature.
1 Click on Administration.
2 If required, select the appropriate account from the drop down list.
3 Click on User Search.
4 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
5 If you wish to restrict your search by administrator status or activated/deactivated status, click on the 
appropriate button.
6 When you finish entering your search parameters, click on Search Registered Users.-e 
---

SYSTEM ADMINISTRATION TASKS
Changing a User’s Access
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 35
Users List window
7 Click on the user whose password you wish to reset.
Edit User Settings
8 Click on Reset Password.
9 Click OK to confirm that you wish to reset the password.
10 Click on Return to Select Option to exit.
Changing a User’s Access
You can change a user’s access by making the appropriate modifications to the user’s 3PL operator and/or 
administrator status. This function is only available for other system administrators; you cannot change your 
own access.
When you change a user’s access, the changes take effect the next time that the user logs on.
1 Click on Administration.
2 If required, select the appropriate account from the drop down list.
3 Click on User Search.-e 
---

SYSTEM ADMINISTRATION TASKS
Changing a User’s Access
36 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
4 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
5 If you wish to restrict your search by administrator status or activated/deactivated status, click on the 
appropriate button.
6 When you finish entering your search parameters, click on Search Registered Users.
Users List window
7 Click on the user whose access you wish to change.
Edit User Settings
8 Proceed to make your changes to the 3PL operator or the administrator status of the user. The 3PL operator must be attached to the account before you can assign it to the user.
9 Click on Save to save your changes.
10 Click on Return to Select Option to exit.-e 
---

SYSTEM ADMINISTRATION TASKS
Sending E-Mail Messages from e-Vista
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 37
Sending E-Mail Messages from e-Vista
You can e-mail e-Vista users from the Users List screen by clicking on the Send E-Mail to Listed Users 
button. The e-mail message will go to all users shown in the list. In order to receive an e-mail from a system 
administrator, the recipient must have a valid e-mail address defined on the Edit User Settings screen.
e-Vista e-mails may contain boilerplate text that is automatically placed in the body of the message after it is 
sent. This text is defined at the system level and cannot be changed or deleted by the sender of a message.
User to user e-mail must be activated in the file eVistaWhseParam.xml before you can use this feature. See 
“Setting Up Your E-Mailing Options” on page 42 for further information on activating this feature.
1 Click on Administration.
2 If required, select an account.
3 Click on User Search.
4 Click on Search Registered Users or Search Active Users.
5 When the list of recipients is displayed on your screen, do one of the following:
6 Key in your subject line.
7 If required, key in the text of your e-mail message.
E-mail screen
8 Click on Send.
9 Click on Return to Select Option to exit.
If you wish to send to all listed 
users:
If you wish to send to a single 
user:
a) Click on Send E-Mail to Listed 
Users.
a) Click on the user code that you 
wish to send to.
b) On the Edit User Settings 
screen, click on Send E-Mail.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
38 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Understanding Session Control
Session control allows you to control the number of users who are able to access e-Vista at any given time. 
Session control is environment specific. If you operate in two environments, you can have a different session 
control option in each environment. There are two session control options: 
session control If you activate this option, only one person can use any 
given e-Vista user at any one time. For example, if you 
set up an e-Vista user called OPERATOR1, only one 
person can be logged on to e-Vista as OPERATOR1. If 
a second person tries to log on to e-Vista as 
OPERATOR1, he or she will automatically log off the 
first user. 
CAUTION When users are automatically logged off 
because of session control, there is no confirmation 
prompt or warning message.
If you deactivate this option, any number of people can 
share the same e-Vista user. For example, five different users could log on to e-Vista as OPERATOR1.
maximum number of users per 
account
Only available if session control is activated
If you activate this option, the number of users logged 
on to e-Vista at any given time is limited to a specific 
number. If you deactivate this option, there is no limit to 
the number of users logged on to e-Vista at any given 
time.
This limit is per account and per environment and subject to the number of operators specified in your Accellos licensing agreement.
NOTES 
 Regardless of your session control option and the 
maximum number of users per account, access to eVista is always governed by the number of operators 
specified in your licensing agreement. For example, if 
your maximum number of users per account is five 
and your 3PL operator limit is three, five users 
belonging to three operators can log on simultaneously. However, five users belonging to five operators 
cannot log on because the 3PL operator limit has 
been exceeded.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 39
You can look up your current settings by clicking on Show Configuration and paging down to the Database 
Environment Parameters section of the file. 
Database Environment Parameters showing session control de-activated
DELETING A USER SESSION
If you have defined a maximum number of users for a particular account, you may wish to delete a user 
session in order to allow a new user to log on. For example, if your account is limited to nine users in e-Vista 
at any given time and there are currently nine users logged on, a tenth user will not be able to log on. In order 
to allow the tenth user to enter e-Vista, you will have to delete a user session for one of the nine existing 
users. You can delete any session other than your own.
You delete a user session in the Active Users window. For each active user, this screen shows the user code, 
user name, account name, 3PL Operator, administrator status, login time, the number of minutes that the 
user has been inactive and the number of minutes until expiry.
When you look up active users, your own login will be highlighted with thick horizontal lines. The Selection 
box of your own login will be greyed out as you cannot delete your own session.
1 Click on Administration.
 The maximum number of users does not include the 
system administrator working in the Administration 
tab of e-Vista. For example, if your limit is five users 
and five users are currently logged on to e-Vista, a 
sixth user — if he or she is a system administrator — 
can log on. However, the sixth user is restricted to 
the Administration tab and cannot perform queries, 
enter inbound receipts, update POD information, etc.
CAUTION There are only two ways of exiting e-Vista correctly: you click on either 
Exit or Logoff. If you exit e-Vista in any other manner — for example, you close Internet Explorer or you power off your computer — you will still be logged on to e-Vista 
and you will remain logged on until the system administrator deletes your session or 
e-Vista automatically terminates your session after a period of no activity.
The period of no activity is known as the time-out interval. You can look up this value 
by clicking on Show Configuration and paging down to the Warehouse Setups section of this file.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
40 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or active/deactivated status, click on the appropriate button.
5 When you finish entering your search parameters, click on Search Active Users.
Users List window showing active users with GEORGE highlighted as the user looking up other users
6 You can sort your users in either ascending or descending order by any of the first five columns starting 
from the left in the Users List window. Click on Ascending or Descending then click on the column heading by which you wish to sort.
7 Click in the Select Column of the user whose session you wish to delete.
8 Click on Delete Selected Sessions.
9 Click on Return to Select Option to exit.
ACTIVATING AND DEACTIVATING SESSION CONTROL
You activate session control by setting the maxUsersPerAccFlag to YES. You deactivate session control by 
setting the maxUsersPerAccFlag to NO. Session control is by environment. That means that your change will 
affect all users in all accounts working in that environment.
When you activate session control, the Maximum Number of Users Allowed field appears on the Account 
Settings screen. When you deactivate session control, this field is removed.
1 Go to the build/config directory and open systemId.xml.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 41
2 Set the field called maxUsersPerAccFlag to the appropriate value (YES or No).
3 Save your changes.
4 Reboot the server.
DEFINING YOUR TIME-OUT INTERVAL
There are two ways of ending a session. If an e-Vista user clicks on Log Off or Exit, the session is terminated 
immediately and another user can log on if the maximum number of users has not been reached. If an e-Vista 
user terminates a session by any other means (for example, by closing his or her browser or by switching off 
the computer) or if there is no activity, the session is not terminated until a specific number of minutes or 
hours passes. This variable is known as the time-out interval.
Your time-out interval can vary by environment. For example, you can define a time-out interval of 30 minutes 
for the environment of A7, 60 minutes for A8 and 90 minutes for A9. Your time-out interval can also vary by 
account. For example, your default time-out interval for A7 is 30 minutes, but for account ABC your time-out 
interval is 45 minutes.
<?xme="A9" description="Development"
 contextFactory="org.jnp.interfaces.NamingContextFactory"
 providerUrl="localhost:12729"
 ejbServerUser="admin"
 ejbServerPassword="password"
 jdbcUrl="jdbc:oracle:thin:@172.18.1.29:1521:NDEV"
 jdbcDriver="oracle.jdbc.driver.OracleDriver"
 jdbcInitialConnectionUser ="DEL4DUMB"
 jdbcInitialConnectionPassword="DEL4DUMB"
 securityStyle="A9"
 maxUsersPerAccFlag="NO"
 pdfProvider="http://172.18.1.29:8009/SE2DAD/pdf/del4_pdf.jsp"
 pathFaxOvrl="/u02/app/develop/del4/src/faxdir/overlay/"
 releaseID="2950"
 />
 <system name="A9" description="DEMO"
 contextFactory="org.jnp.interfaces.NamingContextFactory"
 providerUrl="localhost:12729"
 ejbServerUser="admin"
 ejbServerPassword="password"
 jdbcUrl="jdbc:oracle:thin:@172.18.1.29:1521:DEMO"
 jdbcDriver="oracle.jdbc.driver.OracleDriver"
 jdbcInitialConnectionUser ="DEL4DUMB"
 jdbcInitialConnectionPassword="DEL4DUMB"
 securityStyle="A9"
 maxUsersPerAccFlag="NO"
 pdfProvider="http://172.18.1.29:7480/SE2DAD/pdf/del4_pdf.jsp"
 pathFaxOvrl="/u02/app/demo/del4/src/faxdir/overlay/"
 releaseID="2950"
 maxUsersPerAccFlag="YES"
 />
<systemIds>-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
42 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
EXAMPLE
Account ABC has session control activated, has a time-out interval of 30 minutes and is 
limited to 10 users per environment at any given time. There are currently 10 users logged 
on to e-Vista when user 10 unplugs his computer at 10:15. User 10’s session will not expire 
until 10:45 and no other user will be able to log on until that time.
Setting Up Your E-Mailing Options
e-Vista supports both system-generated e-mails that are triggered by a specific e-Vista event as well as userto-user e-mails that can be sent at any time to selected e-Vista users. For system-generated e-mails, the 
subject line and text are fully configurable. For user-to-user e-mails, the body of the message can contain 
manually entered text, boilerplate text or a combination of both.
e-Vista e-mailing also supports tokens. Tokens are variables that represent system information such as a list 
of recipients or the user’s environment as well as user-defined information such as the text entered in the 
body of an e-mail message. 
SETTING UP SYSTEM-GENERATED E-MAILING
There are three options in system-generated e-mailing:
 Create User
 Reset Password
 Startup
Create user, reset password and startup e-mailing are deactivated when e-Vista is first installed and during 
an upgrade. You must activate these options before you can use them.
Create User These options govern the notification message(s) sent 
when new e-Vista users are added to the system.
Sender Flag = Yes
If you set this flag to Yes, the system administrator will 
receive a copy of the notification message. e-Vista system administrators must have a valid e-mail address in 
their user settings before they can receive the message. (If they do not have a valid e-mail address, the 
default e-mail address defined in the file InitialProperties.txt will receive the message.) If you set this flag to 
No, the system administrator will not receive a copy of 
the notification message.
Sender Subject
The subject line of the notification message sent to the 
system administrator.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 43
Sender Text
The text of the notification message sent to the system 
administrator.
Recipient Flag = Yes
If you set this flag to Yes, the new user will receive a 
copy of the notification message. e-Vista users must 
have a valid e-mail address in their user settings 
before they can receive the message. If you set this 
flag to No, the new user will not receive a copy of the 
notification message.
Recipient Subject
The subject line of the notification message sent to the 
recipient.
Recipient Text
The text of the notification message sent to the recipient
Reset Password These options govern the notification message(s) sent 
when you reset a user’s password.
Sender Flag = Yes
If you set this flag to Yes, the system administrator will 
receive a copy of the notification message. e-Vista system administrators must have a valid e-mail address in 
their user settings before they can receive the message. (If they do not have a valid e-mail address, the 
default e-mail address defined in the file InitialProperties.txt will receive the message.) If you set this flag to 
No, the system administrator will not receive a copy of 
the notification message.
Sender Subject
The subject line of the notification message sent to the 
system administrator.
Sender Text
The text of the notification message sent to the system 
administrator.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
44 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Recipient Flag = Yes
If you set this flag to Yes, the user whose password 
has been reset will receive a copy of the notification 
message. e-Vista users must have a valid e-mail 
address in their user settings before they can receive 
the message. If you set this flag to No, the user whose 
password has been changed will not receive a notification message.
Recipient Subject
The subject line of the notification message sent to the 
recipient.
Recipient Text
The text of the notification message sent to the recipient.
Startup These options govern the notification message sent 
when you start up e-Vista. This message includes an 
html attachment listing all registered e-Vista users 
sorted by environment.
Sender Flag = Yes
If you set this flag to Yes, the default e-mail address 
defined in the file InitialProperties.txt will receive a copy 
of the notification message. If you set this flag to No, 
the default e-mail address will not receive a copy of the 
notification message.
Sender Subject
The subject line of the notification message sent to the 
default e-mail address.
Sender Text
The text of the notification message sent to the default 
e-mail address.
Recipient Flag = Yes
If you set this flag to Yes, all e-Vista users with a valid 
e-mail address in their user settings will receive a copy 
of the notification message. If you set this flag to No, 
the user will not receive a copy of the notification message.
If the e-Vista user is set up in more than one environment, only one e-mail message will be sent.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 45
SETTING UP E-MAIL NOTIFICATION OF SUBMITTED ORDERS AND RECEIPTS
You can configure e-Vista so that the warehouse automatically receives an e-mail message whenever a client 
account user submits an order or receipt. The e-mail is sent to the warehouse’s e-mail address as defined in 
the fromEmailAddress parameter of InitialProperties.txt.
SETTING UP USER-TO-USER E-MAILING
You use user-to-user e-mailing to send one-time messages to selected e-Vista users. User-to-user e-mails 
can contain standardized boilerplate text, text that you enter in the body of the e-mail message or a combination of the two.
Recipient Subject
The subject line of the notification message sent to the 
recipient.
Recipient Text
The text of the notification message sent to the recipient.
emailEvistaCreateOrdFlag Value =”No”
If you set this flag to No, no e-mail message will be 
sent to the warehouse when a client account user submits an order.
Value =”Yes”
If you set this flag to Yes, an e-mail message will be 
sent to the warehouse when a client account user submits an order.
emailEvistaCreateRcptFlag Value =”No”
If you set this flag to No, no e-mail message will be 
sent to the warehouse when a client account user submits a receipt.
Value =”Yes”
If you set this flag to Yes, an e-mail message will be 
sent to the warehouse when a client account user submits a receipt.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
46 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
User-to-user e-mailing is deactivated when e-Vista is first installed. You must activate user-to-user e-mailing 
before you can use this function.
USING TOKENS IN E-VISTA E-MAIL
Tokens are variables that represent system information such as a list of recipients or the user’s environment 
as well as user-defined information such as the text entered in the body of an e-mail message. Tokens can be 
arranged in any order in an e-mail template and can be combined with both boilerplate text and text that you 
enter when sending user-to-user e-mail. 
e-Vista supports the following tokens:
User to User Sender Flag = Yes
If you set this flag to Yes, the system administrator will 
receive a copy of the message. e-Vista system administrators must have a valid e-mail address in their user 
settings before they can receive the message. (If they 
do not have a valid e-mail address, the default e-mail 
address defined in the file InitialProperties.txt will 
receive the message.) If you set this flag to No, the 
system administrator will not receive a copy of the 
message that was sent.
Sender Text
The text of the message sent to the system administrator. You can use sender text to define a standard greeting that precedes the body of the e-mail message.
Recipient Flag = Yes
If you set this flag to Yes, all e-Vista users with a valid 
e-mail address in their user settings will receive a copy 
of the message. If you set this flag to No, the Send EMail to Selected Users function on the Users List 
screen will be deactivated and you will not be able to 
use it.
Recipient Text
The text of the message sent to the recipient. You can 
use recipient text to define signature type information; 
for example, “From your e-Vista Administrator”.
##USER_NAME the user’s name as defined in User Settings
##USER_CODE the user’s code as defined in User Settings
##USER_ENV the environment in which the user is working
##USER_LIST a list of all users to which a message was sent-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your E-Mailing Options
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 47
The following table shows which tokens can be used in which templates:
The following example shows a user-to-user sender message.
CHANGING YOUR E-MAIL SETUPS IN EVISTAWHSEPARAM.XML
You change your e-mail setups in the file eVistaWhseParam.xml using the vi editor or any other text editor.
1 Go to the $E_VISTA_HOME/build/config directory and open eVistaWhseParam.xml.
2 Proceed to make your changes.
##USER_TEXT the text that the system administrator types in when 
sending a user-to-user e-mail
E-Mail Template Available Tokens
Create User Sender Text
##USER_NAME
##USER_CODE
##USER_ENV
Recipient Text
##USER_NAME
##USER_CODE
##USER_ENV
Reset Password Same as Create User
Startup Sender Text
N/A
Recipient Text
##USER_NAME
User to User Sender Text
##USER_LIST
##USER_TEXT
Recipient Text
##USER_NAME
##USER_TEXT
all templates You can use the pipe command “|” to represent a new line.
||This is a list of users that an e-mail message has been sent 
to:||##USER_LIST||The text of the message was:|##USER_TEXT-e 
---

SYSTEM ADMINISTRATION TASKS
Modifying Scheduled Queries
48 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
3 Save your changes.
4 Click on Reset Configuration Parameters to activate your changes.
Modifying Scheduled Queries
You can modify the description, cc address(es), activation/expiry dates, frequency, time and output of a 
scheduled query. However, you cannot modify the search criteria. If you wish to change the search criteria of 
a scheduled query, you must delete the query and then recreate it with the correct criteria.
System administrators can modify the scheduled queries of any user.
1 Click on any tab that supports scheduled queries (Order Search, Receipt Search, Inventory Search or 
Invoice Search).
2 Click on Scheduling.
3 Click on Search Scheduled Queries.
Search Scheduled screen
4 Key in the appropriate user code.
5 Select the appropriate type of query from the dropdown list.
6 Select the appropriate status.
7 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query List screen
8 You can sort your scheduled queries in either ascending or descending order by any column in the 
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.
9 Click on the job number that you wish to modify.-e 
---

SYSTEM ADMINISTRATION TASKS
Deactivating Scheduled Queries
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 49
Update Scheduled Query screen
10 Proceed to make your changes.
11 Click on Update.
Deactivating Scheduled Queries
System administrators can deactivate the scheduled queries of any user.
1 Click on any tab that supports scheduled queries (Order Search, Receipt Search, Inventory Search or 
Invoice Search).
2 Click on Scheduling.
3 Click on Search.
4 Select the appropriate user code.
5 Select the appropriate type of query from the dropdown list.
6 Select the Activated option as your status.
7 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query List screen
8 You can sort your scheduled queries in either ascending or descending order by any column in the 
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.-e 
---

SYSTEM ADMINISTRATION TASKS
Re-Activating Scheduled Queries
50 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
9 Click in the Select column for the scheduled queries that you wish to deactivate. If you wish to select all 
queries, click on Select All. If you wish to de-select one of more selected queries, click on Clear All. 
10 Click on Deactivate Selected Jobs.
Re-Activating Scheduled Queries
A deactivated scheduled query can be re-activated at any time. When you re-activate a query, you may need 
to change the activation or expiry dates so that they fall in the future.
System administrators can reactivate the scheduled queries of any user.
1 Click on any tab that supports scheduled queries (Order Search, Receipt Search, Inventory Search or 
Invoice Search).
2 Click on Scheduling.
3 Click on Search.
4 Select the appropriate user code.
5 Select the appropriate type of query from the dropdown list.
6 Select the Deactivated option as your status.
7 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query List screen
8 You can sort your scheduled queries in either ascending or descending order by any column in the 
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.
9 Click on the job number that you wish to reactivate.-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Queries in the Scheduled Query Log
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 51
Update Scheduled Query screen showing deactivated scheduled query
10 Select Activate in the Scheduling Status dropdown list.
11 Click on Update.
Looking Up Queries in the Scheduled Query Log
The Scheduled Query Log allows you to look up your scheduled queries to find what which ones ran successfully and which ones failed. For each query that you look up, e-Vista shows the time slot, start date and time, 
end date and time, job number, job description, job type, user, account name, status and status text. If a 
scheduled query failed, the status text will show either the missing e-mail address (status code -2) or the Java 
exception error (status code -3). You must be a system administration to access this function.
You can query your scheduled query results by date range, account name, job number and description, job 
type, time slot, user code and job status (successful, failed or all). When your query results are retrieved, you 
can click on most column headings to re-sort the query results.
1 Click on Administration.
2 Click on Scheduled Query Search.
NOTE If a scheduled query did not run because e-Vista was down, there will be no 
record for the query in the Scheduled Query Log.-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Queries in the Scheduled Query Log
52 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Scheduled Query List screen
3 Key in your search criteria. You can restrict a scheduled query search by from and to date, account 
name, job number, job description, job type, time slot, user code and job status (All, Successful or 
Failed).
Time slots begin at 12:00 am. For example, a time slot of 0 indicates the time from 12:00 am to 1:00 am 
and a time slot of 1 indicates the time from 1:00 am to 2:00 am.
4 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query Log screen showing results in descending sequence (latest queries first)
5 You can click on most column headings to re-sort the query results and you can click on Ascending to 
show the oldest queries first.
6 When you finish looking up the Scheduled Query Log, click on Return to Administration Select Options.-e 
---

SYSTEM ADMINISTRATION TASKS
Changing Your Warehouse Setups
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 53
Changing Your Warehouse Setups
You change your warehouse setups in the file eVistaWhseParam.xml using the vi editor or any other text 
editor. In this file, you can change a number of system defaults as well as define invalid user codes.
NOTE All changes to warehouse setups are global. That means that any changes 
that you make will affect all users in all accounts in all environments.
Field Descriptions
maxRecords The maximum number of records that e-Vista will retrieve in a 
query (excluding pick list queries for consignees and items). If 
the number of records retrieved in a query exceeds this number, 
e-Vista will display the number of records retrieved and prompt 
you to narrow your search.
You can override this value for a given account by entering a 
value in the Rows Per Query field in the Account screen.
pageSize The maximum number of rows that e-Vista will display on a single page after performing a query. If the number of rows 
retrieved in a query exceeds this number, e-Vista will create a 
second page for the excess rows. If you set this value to a large 
number (say, 1,000), you can print the entire query results on a 
single HTML page.
You can override this value for a given account by entering a 
value in the Rows Per Page field in the Account screen.
Individual users can override this value by entering a value in 
the Rows Per Page field of their User Settings.
accountType2 The description for a level 2 account. This description shows up 
in the top left-hand corner of the screen when the user clicks on 
Administration.
accountType3 The description for a level 3 account. This description shows up 
in the top left-hand corner of the screen when the user clicks on 
Administration.-e 
---

SYSTEM ADMINISTRATION TASKS
Changing Your Warehouse Setups
54 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
sessionLength The number of minutes of no activity on the part of an e-Vista 
user that is allowed before the user is automatically logged off. 
You can override this value for a given account by entering a 
value in the Time-Out Interval field in the Account screen.
monitorRefreshRate The frequency with which your screen refreshes when you perform a search of active users on the User Search screen. For 
example, if you enter 20, your screen will refresh every 20 seconds.
Individual users can override this value by entering a value in 
the Session Monitoring Screen Refresh Rate field of their user 
settings.
userAccCleanUpTime The frequency in hours that e-Vista will automatically clean up 
expired users and accounts.
userAccCleanUpModedeactivate
delete
If you enter delete, expired users and accounts will be deleted. 
If you enter deactivate, the user or account will remain in eVista, but no user belonging to that account will be able to log 
on.
invalidUserCodes If required, you can define invalid user codes. For example, if 
you define ACCELLOS as an invalid user code, no system 
administrator for any account will be able to set up a new user 
called ACCELLOS. If you wish to define multiple invalid codes, 
you use a comma to separate each one; for example, “ACCELLOS, ABC, EASTERN FISH”.
This information is restricted to warehouse accounts; client 
accounts will not see invalid user codes when they click on 
Show Configuration.
invtDescriptionLev2 If you set this parameter to Y for Yes, the level 2 description for 
inventory will be shown when you perform an inventory search. 
To enter a level 2 description, you must set the Description 
Entry field to Y for Yes for your second inventory level in DILP 
(Depositor Inventory Level Profile).
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Changing Your Warehouse Setups
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 55
You can look up your current warehouse setups by clicking on Show Configuration and paging down to the 
Warehouse Setups section of the file. 
Show Configuration window showing default warehouse setups
1 Go to the $E_VISTA_HOME/build/config directory and open eVistaWhseParam.xml.
invtDescriptionLev3 If you set this parameter to Y for Yes, the level 3 description for 
inventory will be shown when you perform an inventory search. 
To enter a level 3 description, you must set the Description 
Entry field to Y for Yes for your third inventory level in DILP 
(Depositor Inventory Level Profile).
invtDescriptionLev4 If you set this parameter to Y for Yes, the level 4 description for 
inventory will be shown when you perform an inventory search. 
To enter a level 4 description, you must set the Description 
Entry field to Y for Yes for your fourth inventory level in DILP 
(Depositor Inventory Level Profile).
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Warehouse and Client Logos
56 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
2 Proceed to make your changes.
3 Save your changes.
4 Click on Reset Configuration Parameters to activate your changes.
Setting Up Warehouse and Client Logos
The default logo for all e-Vista screens is called delfourLogo.gif and is defined in the file eVistaWhseParam.xml. You can define a logo for your warehouse that overrides the default logo and appears on all eVista screens for all accounts. 
<?xml version="1.0" encoding="ISO-8859-1"?>
<eVistaWhseParam>
 <param name="clientLogo" value="delfourLogo.gif"/>
 <param name="maxRecords" value="100000"/>
 <param name="pageSize" value="50"/>
 <param name="accountType1" value="Accellos"/>
 <!-- ENUS -->
 <param name="accountType2" value="Warehouse"/>
 <param name="accountType3" value="Client"/>
 <!-- EXMS Spanish -->
 <!--
 <param name="accountType2" value="Bodega"/>
 <param name="accountType3" value="Cliente"/>
 -->
 <param name="sessionLength" value="30"/>
 <param name="monitorRefreshRate" value="60"/>
 <!-- cleanUp expired accounts and users -->
 <param name="userAccCleanUpTime" value="4"/>
 <param name="userAccCleanUpMode" value="deactivate"/>
 <!--List of Invalid User Codes -->
 <param name="invalidUserCodes" value="|ACCELLOS,ABC|"/>
 <!-- Email engine -->
 <!-- create user -->
 <param name="emailCreateUserSenderFlag" value="No"/>
 <param name="emailCreateUserSenderSubject" value="A new e-Vista User has 
been adde
d"/>
 <param name="emailCreateUserSenderText" value="You have created the 
following:|
User##USER_NAME (##USER_CODE) has been added to environment ##USER_ENV."/>
 <param name="emailCreateUserRecipientFlag" value="No"/>
 <param name="emailCreateUserRecipientSubject" value="Welcome to e-Vista"/>-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Warehouse and Client Logos
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 57
You can also define logos for individual accounts and attach these logos to the appropriate accounts. Only 
users attached to the account will see the account-specific logo. If you do not define a warehouse or client 
logo, the standard Accellos logo will appear on all e-Vista screens for all accounts.
All logos must be in GIF or JPEG format, have a fixed height of 69 pixels and cannot exceed 1 MB in size. 
The width of the logo is not fixed and can be any size.
SETTING UP A WAREHOUSE LOGO
A warehouse logo will replace the Accellos logo on all e-Vista screens. If you have defined a client logo, the 
client logo will override the warehouse logo when users attached to that account log on to e-Vista.
If there is already a warehouse logo, the Upload Logo command will overwrite it with the new logo.
1 Click on Administration.
2 Select your warehouse account from the Account drop down list and click on Account Search. Your 
warehouse account is the account used by the employees of your warehouse.
3 Click on the account name of your warehouse account.
4 Click on Upload Logo.
Upload Logo screen
5 Click on Browse.
6 Select the image that you wish to upload and click on Open in Windows. e-Vista will display the full Windows path for the image that you wish to upload.
7 Click on Upload Logo.
Upload Logo screen showing message that logo has been successfully uploaded
NOTE During an upgrade, eVistaWhseParam.xml is deleted and the default version of the file is re-installed. If you have defined a default logo for your warehouse in 
eVistaWhseParam.xml, you must re-enter it and save your changes.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Warehouse and Client Logos
58 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
8 Click on Logoff. Then relogon to see your new logo.
SETTING UP A CLIENT LOGO
If there is already a client logo for an account, the Upload Logo command will overwrite it with the new logo.
1 Click on Administration.
2 Select the client account from the drop down list whose logo you wish to set up and click on Account 
Search.
3 Click on the account name of your client account.
4 Click on Upload Logo.
Upload Logo screen
5 Click on Browse.
6 Select the image that you wish to upload and click on Open in Windows. e-Vista will display the full Windows path for the image that you wish to upload.
7 Click on Upload Logo.
Upload Logo screen showing message that logo has been successfully uploaded
8 Click on Logoff. Then relogon as a client account user to see your new logo.
DELETING A LOGO
If you delete a warehouse logo, warehouse users will see the Accellos or system-default logo. If you delete a 
client account logo, the users attached to the client account will see the warehouse logo (if any). If there is no 
warehouse logo, the client account users will see the Accellos or system-default logo.
1 Click on Administration.
2 Select the account from the drop down list whose logo you wish to delete and click on Account Search.
3 Click on the account name.
4 On the Edit Account screen, click on Delete Logo.
e-Vista will clear the Logo File Name field.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Warehouse and Client Logos
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 59
5 Do one of the following:
CUSTOMIZING THE SPLASH SCREEN
You can customize the logo and screen message of the splash screen by changing the system defaults 
defined in the file eVistaWhseParam.xml. The default logo is eVistaIntro.gif and the default screen message 
is “You have logged into Accellos e-Vista”. The logo that you specify replaces both the Accellos logo and the 
e-Vista logo on the splash screen.
The splash screen logo must be in GIF or JPEG format, must have dimensions less than 97 x 69 pixels (W x 
H) and cannot exceed 1 MB in size.
1 Upload your image as described in “Setting Up Warehouse and Client Logos” on page 56.
2 Go to the build/config directory and open eVistaWhseParam.xml.
3 Look for the parameter name called splashScreenLogo.
4 Change the value for splashScreenLogo to the name of your splash screen logo file.
5 Make any necessary changes to the value of the splashScreenText parameter.
6 Save your changes.
7 In e-Vista, click on Reset Configuration Parameters.
8 Relog on to e-Vista.
CUSTOMIZING THE LOGIN SCREEN LOGO AND WELCOME MESSAGE
You can customize the login screen logo and welcome message by changing the system defaults defined in 
the file eVistaWhseParam.xml. The system default for the login screen logo is DelfourInitialScreenLogo.gif 
and the system default for the welcome message is welcome_eVista.gif.
All login screen logos and welcome messages must be in GIF or JPEG format, must have dimensions less 
than 97 x 69 pixels (W x H) and cannot exceed 1 MB in size.
1 Upload your image as described in “Setting Up Warehouse and Client Logos” on page 56.
2 Go to the build/config directory and open eVistaWhseParam.xml.
3 Do one of the following:
If you are deleting a warehouse 
logo: If you are deleting a client logo:
a) Click on Logoff.
b) Relogon on to see your changes.
a) Click on Logoff.
b) Relogon as a client account user 
to see your changes.
If you wish to change the login 
screen logo:
If you wish to change the 
welcome message:
a) Look for the parameter name 
called loginScreenLogo.
b) Change the value for loginScreenLogo to the name of your 
login screen logo file.
a) Look for the parameter name 
called LoginScreenText.
b) Change the value for LoginScreenText to the name of your 
welcome message file.-e 
---

SYSTEM ADMINISTRATION TASKS
Deactivating the Pick Lists/Drop-Down Lists for Shippers and Consignees
60 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
4 Save your changes.
5 In e-Vista, click on Reset Configuration Parameters.
6 Relog on to e-Vista.
Deactivating the Pick Lists/Drop-Down Lists for Shippers and 
Consignees
e-Vista supports pick lists/drop-down lists for the shipper in Receipt Search and Create Inbound Receipt and 
for the consignee in Order Search and Create Outbound Order. If required, you can deactivate these lists so 
that users must manually enter their shippers and consignees in the appropriate programs.
You should deactivate your pick lists/drop-down lists in the following cases:
Refer to the table below for restrictions on shipper and consignee pick lists/drop-down lists:
If you have attached the .ALL 
customer code to one or more 
of your shippers in SHIP
Deactivate the shipper pick list/drop-down list. If you do 
not deactivate these lists, all your customers will be 
able to see any shippers attached to the .ALL customer.
If you have attached the .ALL 
customer code to one or more 
of your consignees in CONS
Deactivate the consignee pick list/drop-down list. If you 
do not deactivate these lists, all your customers will be 
able to see any consignees attached to the .ALL customer.
Type of List Restriction
shipper drop-down list in Receipt Search Only available for operators who are restricted to a 
single customer within a single company. If an operator has access to multiple customers/companies, the 
shipper drop-down list will be deactivated for that 
operator.
shipper pick list in Create Inbound 
Receipt
no restrictions
consignee drop-down list in Order 
Search
Only available for operators who are restricted to a 
single customer within a single company. If an operator has access to multiple customers/companies, the 
consignee drop-down list will be deactivated for that 
operator.
consignee pick list in Create Outbound 
Order
no restrictions-e 
---

SYSTEM ADMINISTRATION TASKS
Working With Multilingual Labels
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 61
1 Go to the build/config directory and open eVistaWhseParam.xml.
2 Do one of the following:
3 Save your changes.
4 In e-Vista, click on Reset Configuration Parameters.
5 Relog on to e-Vista.
Working With Multilingual Labels
e-Vista’s powerful label management tools make it easy to maintain your multilingual labels, switch from nonEnglish to English labels with a single click, find out which labels have not been translated and troubleshoot 
general label issues.
When you log on to e-Vista, the system searches for your language code as defined in User Settings. It then 
retrieves from the labels database the field labels for that language and displays them on your screen. If your 
language is other than English and if e-Vista cannot find a translation for a particular field label, it will display 
the English or default term.
The default language in e-Vista is called “Standard”. Standard is based on ENUS (US English). You can 
change ENUS or any other language, but you cannot change Standard. If you do not make changes to ENUS 
in TRMA (Translation Manger), ENUS and Standard will be identical. If you do make changes to ENUS in 
TRMA (Translation Manager), ENUS and Standard will not be the same.
Rest Labels to Test option showing “X” preceding each label (all labels are OK)
If you wish to deactivate the 
shipper pick list:
If you wish to deactivate the 
consignee pick list:
a) Look for the parameter name 
called pickListShipperFlag.
b) Change the value for pickListShipperFlag to N for No.
a) Look for the parameter name 
called pickListConsigneeFlag.
b) Change the value for pickListConsigneeFlag to N for No.-e 
---

SYSTEM ADMINISTRATION TASKS
Working With Multilingual Labels
62 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Show Missing Labels option showing missing Spanish label
Label Description
Reset Multilingual 
Labels
Only available for system administrators attached to a warehouse account
When you click on this button, e-Vista will refresh all labels with 
the latest changes made in TRMA (Translation Manager). If you 
change an e-Vista label in TRMA and do not click on Reset Multilingual Labels, any label changes made in TRMA will not take 
effect until the e-Vista server is rebooted.
NOTE You must be attached to the language to reset multilingual labels. For example, if you are attached to ENUS and 
change your ESMX labels, you will not see the changes; you 
must reset your language to ESMX and then click on Reset Multilingual Labels.-e 
---

SYSTEM ADMINISTRATION TASKS
Working With Multilingual Labels
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 63
1 Click on Administration.
Reset Labels to 
Standard
Only used if you work in a language other than English or if your 
ENUS language has been customized in TRMA (Translation 
Manager)
This button will temporarily switch all labels to Standard, which 
is based on the language ENUS (US English). If you need to 
report an issue to 3PL Support, you can use this command to 
temporarily switch your language to Standard so that Accellos 
support staff can understand which screen or field is causing the 
problem.
When the problem is resolved, you click on Reset Labels to 
Your Language to return to your normal working language.
Reset Labels to Test Only available for system administrators attached to a warehouse account
When you click on this button, e-Vista will display an “X” in front 
of each label found. If there is no “X” displayed before a given 
label, it means that the label was hardcoded in e-Vista rather 
than retrieved from the labels database. Hardcoded labels cannot be translated; therefore, they must be reported to Accellos 
so that they can be corrected.
NOTE If you are working in the language Standard (that is, 
your ENUS language has not been customized) and you see a 
caret (“^”) in front of a label, it means that e-Vista failed to 
retrieve the label from the labels database because it could not 
find it or for some other reason. Labels preceded by a caret 
must be reported to Accellos so that they can be corrected.
Show Missing Labels Only used if you work in a non-English language or your ENUS 
language has been customized in TRMA (Translation Manager)
When you click on this button, e-Vista will display a question 
mark (“?”) in front of all missing labels. For example, if you are 
working in Spanish and a given label does not have a Spanish 
translation, the label will be shown in English preceded by a 
question mark (“?Customer Code”).
Label Description-e 
---

SYSTEM ADMINISTRATION TASKS
Monitoring e-Vista Users
64 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Administration window for system administrator
2 Click on the appropriate button to reset your labels or show missing labels.
3 When you finish your task in the previous step, click on the same button again to revert back to your normal labels. (This step is not required for Reset Multilingual Labels.)
NON-MULTILINGUAL LABELS
There are a few labels in e-Vista that are not multilingual and cannot be modified in TRMA. For example, the 
login screen labels are not based on the language code of any e-Vista user because the e-Vista user is not 
known at the time of login.
These labels are defined by Accellos in the eVistaWhseParam.xml file. They apply to all e-Vista users and the 
language used is the deployment language rather than the e-Vista user language.
Monitoring e-Vista Users
You can monitor e-Vista user activities by means of the Monitor command. This command shows e-Vista 
usage between a date range that you specify. You can monitor e-Vista usage in either summary mode or 
detail/session mode.
Summary mode shows the activity (online or scheduled), the date/time of the first and last sessions, the total 
number of sessions during the reporting period, the total number of hours/minutes for these sessions and the 
average number of hours/minutes for each session. You can also summarize e-Vista usage by account or by 
operator.
Detail or session mode shows the activity (online or scheduled), the operator code/description, the account 
code/description, the account type, the login date/time, the last access date/time and duration of each 
session.
NOTE User activity data is kept for 100 days (default value); any data older than 
100 days is automatically purged from e-Vista. If you wish to retain user data for longer than 100 days, please contact Accellos support for assistance.-e 
---

SYSTEM ADMINISTRATION TASKS
Monitoring e-Vista Users
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 65
1 Click on Monitor.
Field Descriptions
Total Online
Scheduled
You can restrict your query to either online or scheduled queried. If you select Total, you query will include both types of queries.
Summary Summary
Account
Operator
Sessions
If you select Summary, e-Vista will show the activity (online or 
scheduled), the total number of sessions during the reporting 
period, the total number of hours/minutes for these sessions 
and the average number of hours/minutes for each session.
If you select Account, e-Vista will show summary information 
plus the account code, description and type.
if you select Operator, e-Vista will show summary information 
plus the operator code and name in addition to the account 
code, description and type.
If you select Sessions, e-Vista will show the activity (online or 
scheduled), the operator code/description, the account code/
description, the account type, the login date/time, the last 
access date/time and duration of each session.
Account If you select an account, your query will be restricted to that 
account.
Operator If you select an operator, your query will be restricted to that 
operator.
Date From / To The date range for your query. If you do not specify a date 
range, e-Vista will include all user activity records from the date 
of your last purge to the previous day.-e 
---

SYSTEM ADMINISTRATION TASKS
Monitoring e-Vista Users
66 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
e-Vista Monitor screen
2 Enter your search parameters.
3 If you make a mistake and wish to re-enter your search parameters, click on Clear and then re-enter your 
search parameters.
4 When you finish entering your search parameters, click on Search.
Search Results for operator GEORGE
5 If you wish to see your search results in CSV format, click on CSV. Files in CSV format can be opened in 
Excel and saved as an Excel file.
6 When you finish monitoring e-Vista usage, click X (Close).-e 
---

E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 67
OPERATIONAL TASKS
Signing on for the First Time ........................................................................... 68
Changing Your User Settings .......................................................................... 68
Resetting Your Labels to Standard ................................................................. 70
Looking Up Your Configuration....................................................................... 71-e 
---

OPERATIONAL TASKS
Signing on for the First Time
68 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
Signing on for the First Time
When you sign on for the first time, you must change your password from the default password “changeIt” to 
a new password. Passwords in e-Vista are case sensitive: “MyPassword” is not the same as “mypassword”.
1 Open your browser.
2 Connect to the appropriate Internet address. The correct address is defined by your system administrator.
3 Key in your user code.
4 Key in changeIt as your password.
5 Select your environment from the drop down list.
6 Click on Login. e-Vista will display the Edit Your Settings window where you must enter and confirm a 
new password.
Edit Your Settings
7 Key in changeIt as your current password.
8 Key in your new password. Passwords must be a minimum of six characters in length.
9 In the Confirm field, key in your new password again.
10 Click on Save.
11 Relog on using your new password.
Changing Your User Settings
There are five settings that any e-Vista user can change: your user name, language, password, e-mail 
address and rows per page value. If you are a system administrator, you can also change your session 
monitoring refresh rate.-e 
---

OPERATIONAL TASKS
Changing Your User Settings
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 69
1 Click on Administration.
2 Click on Edit Your Settings.
Edit Your Settings screen
Field Descriptions
User Name Your user name. This name is for display purposes only and is 
not used to login. 
Language Code Your language code. 
e-Mail Address Your e-mail address. If you e-mail a query, the address that you 
enter in this field will be your from address. If you set up a 
scheduled query, the query will be sent to this address.
Rows Per Page The maximum number of rows that e-Vista will display on a
single page after performing a query. If the number of rows
retrieved in a query exceeds this number, e-Vista will create
a second page for the excess rows. If you set this value to a
large number (say, 1,000), you can print the entire query
results on a single HTML page.
Session Monitoring 
Refresh Rate (in 
seconds)
Only available for system administrators
The frequency with which your screen refreshes when you
perform a search of active users on the User Search screen.
For example, if you enter 20, your screen will refresh every
20 seconds.-e 
---

OPERATIONAL TASKS
Resetting Your Labels to Standard
70 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY
3 Key in your password.
4 Click on Save to save your changes.
5 If your password change fails because the password that you enter in the New Password field does not 
match the password in the Confirm field, you must re-enter your new password in both fields.
6 Relogon to e-Vista.
Resetting Your Labels to Standard
If you work in a language other than English and if you need to report an issue to 3PL Support, the Reset 
Labels to Standard command allows you to temporarily switch your language to English so that Accellos 
support staff can understand which screen or field is causing the problem.
1 Click on Administration.
Administration window
2 Click on Reset Labels to Standard.
3 When you finish dealing with 3PL Support, click on Reset Labels to Your Language to return to your normal working language.
If you wish to change your 
password:
If you wish to change any other 
user setting:
a) Remove the asterisks in the New 
Password field and then key in 
your new password.
b) Remove the asterisks in the 
Confirm field and then key in 
your new password again.
a) Proceed to make your changes.-e 
---

OPERATIONAL TASKS
Looking Up Your Configuration
E-VISTA SETUP GUIDE: WAREHOUSE ONLY 3.2.5.2 71
Looking Up Your Configuration
The Show Configuration function shows all e-Vista parameters including user setups, warehouse setups, 
database environment parameters, imaging system setups and e-mail parameters. It allows you to accurately 
report configuration information to system administrators and technical support staff so that e-Vista issues 
can be quickly diagnosed and easily resolved.
This function is available to both system administrators and non-system administrators.
1 Click on Administration.
2 Click on Show Configuration.
Setups window
3 When you finish looking up your configuration, click on Close.-e 
---

OPERATIONAL TASKS
Looking Up Your Configuration
72 3.2.5.2 E-VISTA SETUP GUIDE: WAREHOUSE ONLY-e 
---


