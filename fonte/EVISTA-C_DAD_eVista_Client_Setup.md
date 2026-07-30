# Manual EVISTA-C — e-Vista Client Setup Guide

> **ID do Manual:** EVISTA-C  
> **Sistema:** AccellosOne Enterprise 3PL / Körber Supply Chain WMS  
> **Versão:** 4.2 (2016-2017) | K.Motion 6.x (2023) onde indicado  
> **Descrição:** Configuração do cliente web e-Vista: setup de acesso, configurações de interface, parâmetros de conexão. Versão 3.2.5.2 (2013).

---

June 2013
3.2.5.2
90 South Cascade Avenue, Suite 1200
Colorado Springs, CO 80903
www.accellos.com
E‐VISTA
SETUP GUIDE:
CLIENT ONLY-e 
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

E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 i
TABLE OF CONTENTS
OVERVIEW 1
System Administrators vs. Non-System Administrators ............................................................. 2
SYSTEM ADMINISTRATION TASKS 3
Setting Up e-Vista Users ................................................................................................................. 4
Deleting and Deactivating Users .................................................................................................... 7
Deactivating Users Through Activation and Expiry Dates ................................................... 8
Looking Up Users ............................................................................................................................ 9
Understanding Session Control ................................................................................................... 10
Deleting a User Session .................................................................................................... 11
Resetting a User’s Password........................................................................................................ 12
Changing a User’s Access............................................................................................................ 13
Sending E-Mail Messages from e-Vista ....................................................................................... 14
Modifying Scheduled Queries ...................................................................................................... 15
Deactivating Scheduled Queries .................................................................................................. 17
Re-Activating Scheduled Queries ................................................................................................ 17
Looking Up Queries in the Scheduled Query Log ...................................................................... 18
Setting Up Your Logo .................................................................................................................... 20
Setting Up a Logo.............................................................................................................. 20
Deleting a Logo ................................................................................................................. 21
Monitoring e-Vista Users............................................................................................................... 22
OPERATIONAL TASKS 25
Signing on for the First Time ........................................................................................................ 26
Modifying Your Settings................................................................................................................ 26
Resetting Your Labels to Standard............................................................................................... 28
Looking Up Your Configuration.................................................................................................... 28-e 
---

ii 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY-e 
---

E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 1
OVERVIEW
System Administrators vs. Non-System Administrators ................................ 2-e 
---

OVERVIEW
System Administrators vs. Non-System Administrators
2 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
System Administrators vs. Non-System Administrators
There are two types of users in e-Vista: system administrators and non-system administrators. 
System administrators can set up new users, delete users, reset passwords and perform a number of other 
system administration tasks. Non-system administrators are limited to changing their user name, password, 
e-mail address and rows per page value. All other tasks must be performed by a system administrator.
If the warehouse has given you system administrator privileges, you can set up and maintain your users by 
yourself. If the warehouse has not given you system administrator privileges, you are limited to changing your 
user name, password, e-mail address, rows per page and session monitoring screen refresh rate. All other 
tasks must be performed by a system administrator at the warehouse.
NOTE For security reasons, system administrators cannot change their own security settings such as resetting a password or changing their 3PL operator. If your company has system administrator privileges and if a system administrator wishes to 
change his or her security settings, you have two options. You can have another system administrator in your company make the changes or you can have the warehouse make the changes. However, you cannot make the change yourself.-e 
---

E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 3
SYSTEM ADMINISTRATION TASKS
Setting Up e-Vista Users .................................................................................... 4
Deleting and Deactivating Users ....................................................................... 7
Looking Up Users ............................................................................................... 9
Understanding Session Control ...................................................................... 10
Resetting a User’s Password........................................................................... 12
Changing a User’s Access ............................................................................... 13
Sending E-Mail Messages from e-Vista .......................................................... 14
Modifying Scheduled Queries.......................................................................... 15
Deactivating Scheduled Queries ..................................................................... 17
Re-Activating Scheduled Queries ................................................................... 17
Looking Up Queries in the Scheduled Query Log ......................................... 18
Setting Up Your Logo ....................................................................................... 20
Monitoring e-Vista Users.................................................................................. 22-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up e-Vista Users
4 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Setting Up e-Vista Users
There are six parameters that you must define for each e-Vista user:
 a user code
 a user name
 a language
 an e-mail address
 a 3PL operator
 the user’s system administrator status
You must have system administrator privileges to perform this task.
Field Descriptions
User Code Mandatory
The code of the new user. User codes can consist of any combination of numbers or letters. Special characters such as #, &, %, 
etc. are not valid. Nor can you use periods, commas or embedded spaces.
User Name Mandatory
The name of the new user.
Password This field is preset to “changeIt” and cannot be modified when 
setting up a new user.
Language Code The new user’s language.
e-Mail Address Mandatory
The new user’s e-mail address. If the user e-mails a query, the 
address that you enter in this field will be the user’s from 
address.
A valid e-mail address is required to receive system-generated 
e-mails such as “e-Vista is now running” and user-to-user emails sent by the system administrator.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up e-Vista Users
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 5
3PL Operator Mandatory
This field controls which functions in e-Vista the new user will be 
able to perform. There are four possible functions in e-Vista: 
looking up orders, receipts, inventory and items, entering an 
inbound receipt, entering an outbound order and looking up an 
invoice.
The warehouse will tell you which 3PL operator corresponds to 
which e-Vista functions.
Administrator Administrator privileges are only available if they have been 
activated by the warehouse
Yes
No
If you set this flag to Y for Yes, the new user will have administrator privileges. If you set this flag to N for No, the new user will 
be a regular operator with no administrator privileges.
The settings for your account override the value that you enter 
in this field. For example, if the warehouse gives your account 
administrator privileges and you set this flag to Yes for a given 
user, that user will have administrator privileges. Should the 
warehouse later remove administrator privileges for your 
account, the flag will remain set to Yes for the user, but the user 
will no longer have administrator privileges.
Hold Processing 
Privileges
Hold processing privileges are only available if they have been 
activated by the warehouse
None
Put on Hold and Take off Hold
Put on Hold Only
Take off Hold Only
The user’s hold processing privileges.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up e-Vista Users
6 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
1 Click on Administration.
Administration tab
2 Click on New User.
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
fields. Your account settings can only be defined or modified by 
the warehouse.
See “Deactivating Users Through Activation and Expiry Dates”
on page 8 for further information on expiry dates.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
Deleting and Deactivating Users
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 7
Create User screen
3 Key in your user code.
4 Key in your user name.
5 If required, select a language other than the default language from the dropdown list.
6 Key in the e-mail address of the new user.
7 Key in your 3PL operator for the new user or select the appropriate 3PL operator from the drop down list.
8 Select the appropriate administrator option.
9 If required, select the user activation and/or user expiry dates.
10 Click on Save to save your changes.
Deleting and Deactivating Users
When you delete a user, that user is permanently removed from e-Vista. When you deactivate a user, that 
user remains in e-Vista but cannot log on. Deactivated users must be reactivated before they can use e-Vista 
again. You reactivate a user by changing his or her status from “Deactivated” to “Activated”.
Deleting and deactivating users can only be performed by system administrators. You cannot delete or 
deactivate yourself; this must be done by another system administrator.
1 Click on Administration.
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or activated/deactivated status, click on the 
appropriate button.-e 
---

SYSTEM ADMINISTRATION TASKS
Deleting and Deactivating Users
8 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
5 When you finish entering your search parameters, click on Search Registered Users.
Users List window
6 Click on the user that you wish to delete or deactivate.
Edit User Settings window
7 Do one of the following:
8 Click on Return to Select Option to exit.
DEACTIVATING USERS THROUGH ACTIVATION AND EXPIRY DATES
You can automatically deactivate a user by defining a user expiry date for the user on the Create User 
screen. For example, suppose you hire a temporary employee who is to start on September 1 for a two-week 
period. You define September 1 as his or her activation date and September 14 as the expiry date.
On September 15, one of the following will occur:
 If the warehouse has set the Accounts/Users Cleanup Mode flag to delete, the user will be deleted.
If you wish to delete the user:
If you wish to deactivate the 
user:
a) Click on Delete.
b) Click OK when prompted to confirm the deletion.
a) Click on Deactivated.
b) Click on Save.-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Users
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 9
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
settings, refer to the section “Modifying Your Settings” on page 26.
1 Click on Administration.
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
8 When you finish looking up your user, click on Return to Select Option to exit.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
10 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Understanding Session Control
Session control allows you to control the number of users who are able to access e-Vista at any given time. 
Session control is environment specific. If you operate in two environments, you can have a different session 
control option in each environment. There are two session control options:
Both options are defined by the warehouse and cannot be modified. You can look up your current settings by 
clicking on Show Configuration and paging down to the Database Environment Parameters section of the file. 
session control If this option has been activated by the warehouse, 
only one person can use any given e-Vista user at any 
one time. For example, if you set up an e-Vista user 
called OPERATOR1, only one person can be logged 
on to e-Vista as OPERATOR1. If a second person tries 
to log on to e-Vista as OPERATOR1, he or she will 
automatically log off the first user. 
CAUTION When users are automatically logged off 
because of session control, there is no confirmation 
prompt or warning message.
If this option has been deactivated by the warehouse, 
any number of people can share the same e-Vista 
user. For example, five different users could log on to 
e-Vista as OPERATOR1.
maximum number of users per 
account
Only available if session control is activated
If this option has been activated by the warehouse, the 
number of users logged on to e-Vista at any given time 
is limited to a specific number. If this option has been 
deactivated by the warehouse, there is no limit on the 
number of users logged on to e-Vista at any given time.
This limit is per account and per environment.
NOTE The maximum number of users does not 
include the system administrator working in the Administration tab of e-Vista. For example, if your limit is five 
users and five users are currently logged on to e-Vista, 
a sixth user — if he or she is a system administrator — 
can log on. However, the sixth user is restricted to the 
Administrator tab and cannot perform queries, enter 
inbound receipts, etc.-e 
---

SYSTEM ADMINISTRATION TASKS
Understanding Session Control
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 11
Database Environment Parameters showing session control de-activated
DELETING A USER SESSION
If the warehouse has defined a maximum number of users for your account, you may wish to delete a user 
session in order to allow a new user to log on. For example, if your account is limited to nine users in e-Vista 
at any given time and there are currently nine users logged on, a tenth user will not be able to log on. In order 
to allow the tenth user to enter e-Vista, you will have to delete a user session for one of the nine existing 
users.
You delete a user session in the Active Users window. For each active user, this screen shows the user code, 
user name, account name, 3PL operator, administrator status, login time, the number of minutes that the user 
has been inactive and the number of minutes until expiry.
When you look up active users, your own login will be highlighted with thick horizontal lines. The Selection 
box of your own login will be greyed out as you cannot delete your own session.
1 Click on Administration.
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or active/deactivated status, click on the appropriate button.
5 When you finish entering your search parameters, click on Search Active Users.
CAUTION There are only two ways of exiting e-Vista correctly: you click on either 
Exit or Logoff. If you exit e-Vista in any other manner — for example, you close Internet Explorer or you power off your computer — you will still be logged on to e-Vista 
and you will remain logged on until the system administrator deletes your session or 
e-Vista automatically terminates your session after a period of no activity.
The period of no activity is known as the time-out interval. You can look up this warehouse-defined value by clicking on Show Configuration and paging down to the 
Warehouse Setups section of this file.-e 
---

SYSTEM ADMINISTRATION TASKS
Resetting a User’s Password
12 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Users List window showing active users with GEORGE highlighted as the user looking up other users
6 You can sort your users in either ascending or descending order by any of the first five columns starting 
from the left in the Users List window. Click on Ascending or Descending then click on the column heading by which you wish to sort.
7 Click in the Select Column of the user whose session you wish to delete.
8 Click on Delete Selected Sessions.
9 Click on Return to Select Option to exit.
Resetting a User’s Password
If a user forgets his or her password, the system administrator must reset it. When you reset a user’s 
password, that user will be required to follow the steps described in the section “Signing on for the First Time”
on page 26.
Resetting a user’s password may trigger an automatic e-mail to the user if this feature has been activated by 
the warehouse.
1 Click on Administration.
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or active/deactivated status, click on the appropriate button.
5 When you finish entering your search parameters, click on Search Registered Users.
Users List window
6 Click on the user whose password you wish to reset.-e 
---

SYSTEM ADMINISTRATION TASKS
Changing a User’s Access
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 13
Edit User Settings
7 Click on Reset Password.
8 Click OK to confirm that you wish to reset the password.
9 Click on Return to Select Option to exit.
Changing a User’s Access
You can change a user’s access by making the appropriate modifications to the user’s 3PL operator and/or 
administrator status. This function is only available for other system administrators; you cannot change your 
own access.
When you change a user’s access, the changes take effect the next time that the user logs on.
1 Click on Administration.
2 Click on User Search.
3 If you wish to restrict your search by user code, user name, e-mail address or 3PL operator, key in the 
appropriate search criteria. You can also use the wildcard character (%) when performing searches; refer 
to the “Using Wildcards” section in the e-Vista User Guide for further information on this function.
4 If you wish to restrict your search by administrator status or active/deactivated status, click on the appropriate button.
5 When you finish entering your search parameters, click on Search Registered Users.-e 
---

SYSTEM ADMINISTRATION TASKS
Sending E-Mail Messages from e-Vista
14 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Users List window
6 Click on the user whose access you wish to change.
Edit User Settings
7 Proceed to make your changes to the 3PL operator or the administrator status of the user.
8 Click on Save to save your changes.
9 Click on Return to Select Option to exit.
Sending E-Mail Messages from e-Vista
You can e-mail e-Vista users from the Users List screen by clicking on the Send E-Mail to Listed Users 
button. The e-mail message will go to all users shown in the list. In order to receive an e-mail from a system 
administrator, the recipient must have a valid e-mail address defined on the Edit User Settings screen.
e-Vista e-mails may contain boilerplate text that is automatically placed in the body of the message after it is 
sent. This text is controlled by the warehouse and you cannot change or delete it.
E-mailing is restricted to system administrators and is only available if offered by your warehouse.
1 Click on Administration.
2 If required, select an account.-e 
---

SYSTEM ADMINISTRATION TASKS
Modifying Scheduled Queries
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 15
3 Click on User Search.
4 Click on Search Registered Users or Search Active Users.
5 When the list of recipients is displayed on your screen, do one of the following:
6 Key in your subject line.
7 If required, key in the text of your e-mail message.
E-mail screen
8 Click on Send.
9 Click on Return to Select Option to exit.
Modifying Scheduled Queries
You can modify the description, cc address(es), activation/expiry dates, frequency, time and output of a 
scheduled query. However, you cannot modify the search criteria. If you wish to change the search criteria of 
a scheduled query, you must delete the query and then recreate it with the correct criteria.
System administrators can modify the scheduled queries of any user.
1 Click on any tab that supports scheduled queries (Order Search, Receipt Search, Inventory Search or 
Invoice Search).
2 Click on Scheduling.
3 Click on Search Scheduled Queries.
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
Modifying Scheduled Queries
16 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Search Scheduled screen
4 Key in the appropriate user code.
5 Select the appropriate type of query from the dropdown list.
6 Select the appropriate status.
7 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query List screen
8 You can sort your scheduled queries in either ascending or descending order by any column in the 
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.
9 Click on the job number that you wish to modify.
Update Scheduled Query screen
10 Proceed to make your changes.
11 Click on Update.-e 
---

SYSTEM ADMINISTRATION TASKS
Deactivating Scheduled Queries
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 17
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
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.
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
3 Click on Search.-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Queries in the Scheduled Query Log
18 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
4 Select the appropriate user code.
5 Select the appropriate type of query from the dropdown list.
6 Select the Deactivated option as your status.
7 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
Scheduled Query List screen
8 You can sort your scheduled queries in either ascending or descending order by any column in the 
Scheduled Query List window except the Frequency and Time columns. Click on Ascending or Descending then click on the column heading by which you wish to sort.
9 Click on the job number that you wish to reactivate.
Update Scheduled Query screen showing deactivated scheduled query
10 Select Activate in the Scheduling Status dropdown list.
11 Click on Update.
Looking Up Queries in the Scheduled Query Log
The Scheduled Query Log allows you to look up your scheduled queries to find what which ones ran successfully and which ones failed. For each query that you look up, e-Vista shows the time slot, start date and time, 
end date and time, job number, job description, job type, user, account name, status and status text. If a 
scheduled query failed, the status text will show either the missing e-mail address (status code -2) or the Java 
exception error (status code -3). You must be a system administration to access this function.-e 
---

SYSTEM ADMINISTRATION TASKS
Looking Up Queries in the Scheduled Query Log
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 19
You can query your scheduled query results by date range, account name, job number and description, job 
type, time slot, user code and job status (successful, failed or all). When your query results are retrieved, you 
can click on most column headings to re-sort the query results.
1 Click on Administration.
2 Click on Scheduled Query Search.
Scheduled Query List screen
3 Key in your search criteria. You can restrict a scheduled query search by from and to date, account 
name, job number, job description, job type, time slot, user code and job status (All, Successful or 
Failed).
Time slots begin at 12:00 am. For example, a time slot of 0 indicates the time from 12:00 am to 1:00 am 
and a time slot of 1 indicates the time from 1:00 am to 2:00 am.
4 Click on Search. e-Vista will retrieve all scheduled queries that match the criteria that you specified.
NOTE If a scheduled query did not run because e-Vista was down, there will be no 
record for the query in the Scheduled Query Log.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your Logo
20 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Scheduled Query Log screen showing results in descending sequence (latest queries first)
5 You can click on most column headings to re-sort the query results and you can click on Ascending to 
show the oldest queries first.
6 When you finish looking up the Scheduled Query Log, click on Return to Administration Select Options.
Setting Up Your Logo
If system administrator privileges have been activated by your warehouse, you can define a logo for your 
company that appears on all e-Vista screens. If you do not define a logo, the standard logo set up by your 
warehouse will appear on all e-Vista screens.
All logos must be in GIF or JPEG format, have a fixed height of 69 pixels and cannot exceed 1 MB in size. 
The width of the logo is not fixed and can be any size.
SETTING UP A LOGO
If there is already a logo for your account, the Upload Logo command will overwrite it with the new logo.
1 Click on Administration.
2 Click on View Your Account.-e 
---

SYSTEM ADMINISTRATION TASKS
Setting Up Your Logo
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 21
Edit Account screen
3 Click on Upload Logo.
Upload Logo screen
4 Click on Browse.
5 Select the image that you wish to upload and click on Open in Windows. e-Vista will display the full Windows path for the image that you wish to upload.
6 Click on Upload Logo.
Upload Logo screen showing message that logo has been successfully uploaded
7 Click on Logoff. Then relogon to see your new logo.
DELETING A LOGO
If you delete a logo, the users attached to your account will see the warehouse logo.
1 Click on Administration.-e 
---

SYSTEM ADMINISTRATION TASKS
Monitoring e-Vista Users
22 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
2 Click on View Your Account.
3 On the Edit Account screen, click on Delete Logo.
e-Vista will clear the Logo File Name field.
4 Click on Logoff. Relogon to see your changes.
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
100 days is automatically purged from e-Vista. If you wish to retain user data for longer than 100 days, please contact Accellos support for assistance.
Field Descriptions
Total Online
Scheduled
You can restrict your query to either online or scheduled queried. If you select Total, you query will include both types of queries.-e 
---

SYSTEM ADMINISTRATION TASKS
Monitoring e-Vista Users
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 23
1 Click on Monitor.
e-Vista Monitor screen
2 Enter your search parameters.
3 If you make a mistake and wish to re-enter your search parameters, click on Clear and then re-enter your 
search parameters.
4 When you finish entering your search parameters, click on Search.
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
of your last purge to the previous day.
Field Descriptions-e 
---

SYSTEM ADMINISTRATION TASKS
24 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
Search Results for operator GEORGE
5 If you wish to see your search results in CSV format, click on CSV. Files in CSV format can be opened in 
Excel and saved as an Excel file.
6 When you finish monitoring e-Vista usage, click X (Close).-e 
---

E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 25
OPERATIONAL TASKS
Signing on for the First Time ........................................................................... 26
Modifying Your Settings................................................................................... 26
Resetting Your Labels to Standard ................................................................. 28
Looking Up Your Configuration....................................................................... 28-e 
---

OPERATIONAL TASKS
Signing on for the First Time
26 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
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
8 Key in your new password. Passwords must be a minimum of six characters in length and are case sensitive.
9 In the Confirm field, key in your new password again.
10 Click on Save.
11 Relog on using your new password.
Modifying Your Settings
There are five settings that any e-Vista user can change: your user name, language, password, e-mail 
address and rows per page value. If you are a system administrator, you can also change your session 
monitoring refresh rate.-e 
---

OPERATIONAL TASKS
Modifying Your Settings
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 27
There are four settings that any e-Vista user can change: your user name, password, e-mail address and 
rows per page value. If you are a system administrator, you can also change your session monitoring refresh 
rate.
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
Rows Per Page The maximum number of rows that e-Vista will display on a single page after performing a query. If the number of rows 
retrieved in a query exceeds this number, e-Vista will create a 
second page for the excess rows. If you set this value to a large 
number (say, 1,000), you can print the entire query results on a 
single HTML page.
Session Monitoring 
Screen Refresh Rate 
(in seconds)
Only available for system administrators
The frequency with which your screen refreshes when you perform a search of active users on the User Search screen. For 
example, if you enter 20, your screen will refresh every 20 seconds.-e 
---

OPERATIONAL TASKS
Resetting Your Labels to Standard
28 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY
3 Key in your password.
4 Click on Save to save your changes.
5 If your password change fails because the password that you enter in the New Password field does not 
match the password in the Confirm field, you must re-enter your new password in both fields.
Resetting Your Labels to Standard
If you work in a language other than English and if you need to report an issue to 3PL Support, the Reset 
Labels to Standard command allows you to temporarily switch your language to English so that Accellos 
support staff can understand which screen or field is causing the problem.
1 Click on Administration.
Administration window
2 Click on Reset Labels to Standard.
3 When you finish dealing with 3PL Support, click on Reset Labels to Your Language to return to your normal working language.
Looking Up Your Configuration
The Show Configuration function shows all e-Vista parameters including user setups, warehouse setups, 
database environment parameters, imaging system setups and e-mail parameters. It allows you to accurately 
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
E-VISTA SETUP GUIDE: CLIENT ONLY 3.2.5.2 29
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
30 3.2.5.2 E-VISTA SETUP GUIDE: CLIENT ONLY-e 
---


