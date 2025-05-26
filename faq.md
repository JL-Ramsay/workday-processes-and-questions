
## Process Area
### Question
Answer


## User Provisioning
### How is a new user account triggered
Managers need to speak with their HR Business Partners for hiring of Permanent/ casual/ Fixed term employees and if HRBP are not sure, this can be escalated to Director of People Operations (Sian Yates)
The provisioning of new accounts for new starters happens automatically. Based on the details entered into Workday, each new employee is set up with either a Ramsay Business Email Account or a Digital Account. The type of account the new employee will receive is based on their Job Family Group, Job Family and Job Profile.
For Contractors – request can be raised in ServiceNow


## 
### What if someone wants it created sooner than 7d prior to start
Accounts are created 7 days prior to the employee’s start date. Ramsay Business Email Account details are sent to the hiring manager, and Ramsay Digital Account users will receive an activation link in their personal email. 
Accounts cannot be created more than 7 days in advance of the employee’s start date. 
These accounts should only be used once the employee has commenced with Ramsay.


## 
### What if someone is still going through signing paperwork but they want them to “pop in” to acclimate and get a head start so want the account created?
Not possible.


## 
### New Starter has contacted SD as not able to connect to Workday with Pre-hire account details prior to start date
Refer to Workday Support Service Now Queue

Workday issues a pre-hire account to new starter which helps them login to Workday to complete and pre-hire checks.

For any issue with Pre-hire, create a Workday Support ticket in ServiceNow.


## 
### What if the Okta/AD choice is incorrect for this user, in this role at this particular hospital.  Can the choice be overridden to avoid an unnecessary creation/migration?
If you need to change an account type from a Digital Account to a Ramsay Business Email 
Account, a request can be made to IAM Ops via the IAM Service Now Queue. This process typically takes 1-2 days to complete. 
To initiate the change: 
1. Seek Line Manager approval for account change 
2. Raise Service Request using 
3. Provide the following mandatory details in the request: 
• First Name,
• Last Name,
• Manager name,
• Work Location,
• Employee ID,
• Business Justification,
• Approver attachment - Line manager as per Workday

Note: A Ramsay Business Email account is 8 times more costly as compared to a Digital account. [Digital Account costs ~ $ 15 per user per year whereas a Ramsay Business Email Account costs ~ $110 per user per year]


## 
### What if a particular Job Role defaults to Okta and those involved would prefer it to default to AD.
Step 1. Find the row in the spreadsheet  that should be updated to have an AD account . Please do not make any changes to the spreadsheet.
Step 2. Request Katherine and Chris Neal's Approval for the change.
Step 3. Raise a request to IAM Ops via the IAM Service Now Queue with the approval to make changes to the Business Rules.
Note: A Ramsay Business Email account is 8 times more costly as compared to a Digital account. [Digital Account costs ~ $ 15 per user per year whereas a Ramsay Business Email Account costs ~ $110 per user per year]


## 
### What if a user claims to have not been sent a digital account enrolment (activation email)?
Before raising a ticket to IAM, please check whether if Hire date is within 7 days of receiving the issue. If yes, check the Okta broker to see if user profile is present (if present, user have activated their Digital Account and have forgotten about it), if not present, advise the user to check their all inboxes including junk and spam, if issue persists, raise an incident to IAM Service Now Queue capturing all relevant information below.
Full name
Site
Role
Start Date
Employee ID


## 
### What if the user requires their mail account to be a different domain such as Psychology and Gallipoli?
Requests to update domain should be redirected to IAM Service Now queue as these need to be carried out from Okta which includes Primary SMTP.


## 
### How is a users H drive / Email created
Okta creates unique username which is passed to AD as UPN and Primary email address.
At 1 am, ARS creates the mailbox, assigns the default F3 license and provisions the H-drive for the new created user.


## 
### What is the process for fulltime/casual employees (ie. Digital, Transformation contractors) who require ARS accounts but are not employed directly by Ramsay? Example is Gallipoli Medical Research and Pindara Day Procedure Centre in QLD.
Any user not employed directly by Ramsay is not managed by IAM.
For contractor staff, non-RHC staff – these accounts follow  process by SD via ARS.

This process is also applicable to Third Party contractors that are allocated a Ramsay PC (ie. Digital, Transformation contractors).
You must verify that this person has not been given an Okta account.


## 
### 



## Notifications
### What happens if manager doesn’t get notification email for AD creation.  Can it be resent.
It is not possible to resend that notification from IAM.  
SD can manually create an email from this template  and send it to the Line manager.


## 
### What if manager is off on leave and the notification needs to be sent to a team lead or delegate.
It is not possible to resend that notification from IAM.  
SD can manually create an email from this template  and send it to the requested delegate or team lead.


## 
### New hire has been setup with digital account but states they have not received email with details?
Before raising a ticket to IAM, please check whether if Hire date is within 7 days of receiving the issue. If yes, check the Okta broker to see if user profile is present (if present, user have activated their Digital Account and have forgotten about it), if not present, advise the user to check their all inboxes including junk and spam, if issue persists, raise an incident to IAM Service Now Queue capturing all relevant information below.
Full name
Site
Role
Start Date
Employee ID


## 
### 



## Shell account modifications
### What if manager doesn’t read notification and does not request additional groups and/or doesn’t add user to FAM
Notify manager to search for email and fill in a request to add additional groups to user.
Notify manager to get authorisers/owners to add user in FAM.


## 
### 



## Role Changes
### Role changes within the same hospital not requiring account type change.
Once role change happens in Workday, it takes few hours for the update to reach to IAM then to Active directory, the sync is not real time, depending upon when that update comes to IAM, change will happen in overnight run of ARS or the next run
If a role change doesn’t require AD account anymore, AD account remains. There’s no process for AD account to Digital account conversion


## 
### Changes requiring Digital Account to AD conversion.
To initiate the change: 
1. Seek Line Manager approval for account change 
2. Raise Service Request to IAM using 
3. Provide the following mandatory details in the request: 
• First Name,
• Last Name,
• Manager name,
• Work Location,
• Employee ID,
• Business Justification,
• Approver attachment - Line manager as per Workday


## 
### A contractor with an AD account gets converted to a perm FTE status.
A new account will be created for the employee regardless but if the existing account needs to be retained and linked to the user, please raise an incident with the IAM ops to link the existing AD account with the user profile in Okta. 
Please make sure following details are included in the incident: First Name, Last Name, Employee ID, Line Manager, Existing AD account Username.


## 
### A Perm FTE with an AD account gets converted to a Contractor status.
Their existing AD account will be deactivated on their last day of work automatically.
If the account needs to be retained, SD can perform undo deprovisioning and update the following fields in ARS.
EmployeeID must be removed
Employee Type must be updated to Contractor
Update end date for the account
Update line manager, Position details as requested
There is no need to contact IAM Ops as the user is a contractor and no longer available in Okta.


## 
### 



## Location Changes
### Where role remains the same but is just performed from a new location/department but for same “Hospital”.
Once role change happens in Workday, it takes few hours for the update to reach to IAM then to Active directory, the sync is not real time, depending upon when that update comes to IAM, change will happen in overnight run of ARS or the next run.


## 
### Where role remains the same but in a different Hospital.
Once the change is processed in Workday, Okta moves the user to the new OU, within few hours of receiving the update from Workday, the next run of ARS assigns the dynamic distribution, H-drive is not updated automatically. Users can still access their H-drive documents.
If they complain of latency and request to update their H-drive based on new location, 
SD can follow the existing process of updating H-drive.
After making the changes, SD need to share the new path of H-drive with IAM team via the incident ticket to IAM service now queue.
IAM team will manually update the new H-drive path in Okta profile (this is to ensure IAM doesn't override the H-drive path set up by SD).
User should now be able to use the new H:Drive path.
There are some system limitations with automating the H: drive creation on location changes as the user would then loose access to existing documents. This will need further discussion. Also, strategically, we will move away from H: drive once we are on Windows 11.
As a future enhancement to be proactive, a notification email should be send to Service delivery advising them when the location change occurs.


## 
### Where role changes AND location changes in one change.
Once processed in Workday, User doesn't get new employee number or a new account, Okta receives role change and location change update within few hours, and pushes those updates in AD, the next ARS run assigns dynamic distribution list to the AD account.


## 
### 



## Manager Changes
### What happens when a manager leaves or is terminated?
When a manager leaves, manager's manager becomes the reporting manager in Workday record unless the new manager is assigned. Manager change also comes as an update in IAM within few hours of execution at Workday, IAM then pushes this update to Active Directory


## 
### If a manager changes due to a restructure where two managers swap staff does it automatically update all accounts in AD.
Yes, manager gets updated in Okta and Active directory within few hours of making this change in Workday


## 
### If we come across someone in AD with a blank manager what should we do?
Change should be made in Workday as Workday is source of truth
Please ask the user to raise a Support ticket with Workday for Permanent/ Casual/ Fixed term employees
For Contactors/Consultants - raise a ticket with Platform operations.


## 
### If a user reports that they have an incorrect Job Title, what should we do?
Ask the user to raise a support case with HR as Workday is source of truth.


## 
### If there is incorrect employee number in AD, what should we do?
This would need to be notified to IAM ops to be investigated.


## 
### 



## Account Changes
### How do we facilitate a Surname change for marriage/divorce
Name change needs to be requested in Workday via HR business processes.
After successful name change, within few hours IAM sends notification to end user advising their name has been updated in AD however, their username and email address are not updated to prevent any access issue, if required they can raise a modification request to IAM (service catalog available for this under IAM category)
For Display name, it can be updated but needs to be requested via Platform team in the interim.
IAM will update the user's username and email address, new email becomes primary and old email becomes alias, as part of fulfilling this service request.
H-drive is not updated.
If user needs H-drive updated,  
SD can follow the existing process of updating H-drive.
After making the changes, SD need to share the new path of H-drive with IAM team via the incident ticket to IAM service now queue.
IAM team will manually update the new H-drive path in Okta profile (this is to ensure IAM doesn't override the H-drive path set up by SD).
User should now be able to use the new H:Drive path.


## 
### How do we correct the spelling in a firstname/display name (minor that doesn’t impact email)
For Employees, Name changes need to be performed in Workday and will flow through automatically to AD. 
For Display name, it can be updated but needs to be requested via Platform team in the interim.
We are in the process of building a self-service option for the end user to directly update their preferred name in Workday and it will flow through to Okta and to AD.
For Contactors/Consultants, service delivery should update the details as requested.


## 
### How do we correct the spelling in an account where it impacts email or H drive.
Legal Name change needs to be executed in Workday.
After successful name change, within few hours IAM sends notification to end user advising their name has been updated however, their username and email address are not updated to prevent any access issue, if required they can raise a modification request to IAM (service catalog available for this under IAM category)
IAM will update the user's username and email address, new email becomes primary and old email becomes alias, as part of fulfilling this service request.
H-drive is not updated.
If user needs H-drive updated,  
SD can follow the existing process of updating H-drive.
After making the changes, SD need to share the new path of H-drive with IAM team via the incident ticket to IAM service now queue.
IAM team will manually update the new H-drive path in Okta profile (this is to ensure IAM doesn't override the H-drive path set up by SD).
User should now be able to use the new H:Drive path.


## 
### Where a name change impacts email what is the on flowing impact to MFA configuration.
No need to reset password or reset MFA, just use the new username with old password and MFA


## 
### What is the function of preferred name in this setup.
Preferred name will determine user’s display in AD. Currently, currently IAM doesn't source preferred name, once this is implemented, IAM will source preferred name as well and display name in AD will be taken from preferred name. Employees can directly update their preferred names in Workday and this update will reach Okta and AD within few hours; GAL update make take up to two days. Robert can set up Rob and Priya can set up Elly as their preferred names in Workday, there will be no impact on username and email address or H-drive
In the interim, SD can update user’s display name when requested, also ask the user to update their preferred Name.


## 
### Staff are issued with issued with new employee numbers, have an existing AD account and want to retain as changing roles (ie. Worked for Pharmacy and now works for Hospital or vice-versa)
The current process in Workday for a change in Hospital or role is to trigger a job change, where Employee Id doesn’t change.
This job change will automatically be processed in IAM and then reflected in AD within few hours.
Ideally, staff should retain their old employee ID in workday which would mean that the Location and Title will get updated and the AD account will remain active. 
If staff are issued with new Employee ID's, HR business process needs to be validated and hence raise a support ticket with Workday Support queue (Judgement call to be made whether the request is raised by Staff or SD)


## 
### If new employee number is issued, do they get a new blank account?
A new account will be created for the user but if the user wants to retain their old account (given it is still available), then an incident needs to be raised to validate HR business process and assigned to Workday Support queue.


## 
### Employee id discrepancy between what is recorded in Workday and what is recorded in ARS/AD
Ideally, employee Id should match between Workday, Okta and AD if the account is correctly linked.

This would need to be notified to IAM ops to be investigated. SD to raise an incident.


## 
### What if the user works for a different domain within Ramsay such as Psychology or Gallipoli Medical Research? Infrastructure have advised they can no longer convert these accounts to the different SMTP.
Such requests should be sent to IAM ops for changing the domain for employees that are in Workday.


## 
### 



## Job Title
### How does someone change their Job title.
Job titles are changed as part of HR business process during a job change for Ramsay Permanent/ Casual/ Fixed-term employees, if an employee’s job title is incorrect, ask the user to raise a support case with HR as Workday is source of truth.
For Contractors/Consultants - User can raise a User-Account-Modify request which is fulfilled by SD


## 
### What if someone performs multiple roles from one account and has an extended/one off job title.
Primary role details will be updated in AD, if primary role details are not correct, ask the employee to raise a support case with Workday.


## 
### 



## Dual Roles
### What if someone is acting in another role but doesn’t have the appropriate AD account to do so.
An AD account is not automatically created, unless it meets the business rules for AD account creation. 
If someone is acting in a role and needs an AD account as an exception, it would fall in the category of the DA to AD account conversion. Please see process above.
Once a DA gets converted to AD, DA gets deactivated, and employee can only use their AD account for all purposes.


## 
### What if someone performs a role Mo/Tu which needs AD but a different role We/Th/Fr that only needs a digital account.
A person can only have one type of account, either AD or Digital account. If the user has an AD account for one job, the same needs to be used for the other as well.


## 
### What if those two roles are at different hospitals.
For employees having multiple roles, there’s only one primary employee Id in Workday
Okta receives only primary job profile for these employees
DA/AD account creation is based on this primary job profile
If the user requires an exception, can request DA to AD conversion


## 
### 



## Terminations
### Are these triggered by Workday
For Ramsay permanent/casual, Fixed Term employees, terminations are HR- driven process and automatically triggered. SD are not supposed to execute any scripts. These employee types have been descoped from the automation tool for Active Directory as well.
No change in process for removal of access to applications such as Meditech, medical director etc. where access is provisioned using local accounts.
No change in termination process for contractors, contingent works, consultants having AD accounts. User Account – Terminate service Now form can be used for this purpose.


## 
### Will contractors still need to be manually requested.
Yes


## 
### What if an accidental termination occurs, how is that reversed.
Accidental termination if done from workday, needs to be reversed in Workday, there’s no process to terminate a user for a job change, if accidentally happened, needs to be reverted in Workday, if reverted within 21 days, undo deprovisioning will happen automatically. User gets their previous account and assigns AD group memberships back, however if identified after 21 days, a new account will be created for the user after termination is reverted from Workday.
SD should advise manager to get in touch with HR to have it reverted in Workday.


## 
### Contractor staff expiry
No change in current process, contractors are not being managed by Workday or IAM. AD account gets expired based on end date mentioned on User Account – Create request form.
User account – Terminate request is available to request early termination of Contractor.
User account – Modify request is available to request extension in end date of a Contractor.


## 
### 



## Deprovisions
### Will the existing scripted process still continue?
The existing process will continue for Ramsay contractors, consultants and contingent workers which are not managed by Workday, however for Ramsay permanent, casual, fixed term employees, terminations are automated and should not be executed using the scripted process.


## 
### What if an accidental deprovision occurs, how is that reversed.
Accidental termination if done from workday, needs to be reversed in Workday, there’s no process to terminate a user for a job change, if accidentally happened, needs to be reverted in Workday, if reverted within 21 days, undo deprovisioning will happen automatically. User gets their previous account and assigns AD group memberships back, however if identified after 21 days, a new account will be created for the user after termination is reverted from Workday.
SD should advise manager to get in touch with HR to have it reverted in Workday.
Accidental termination of Contractors/Consultants due to delay in raising Modify User request, can be reverted by SD.


## 
### Terminated Accounts SD are unable to see when a user is terminated via the Workday process, as there is no evidence of termination within ARS, the account is disabled.
Following steps can be taken to determine if the account is disabled by IAM based on HR driven termination process in Workday.
Employee type is ‘Permanent/Casual/Fixed-term’
Last password change date time is around 11 PM
Validate the Change History in ARS to confirm if it was done by the automation.


## 
### 



## Exception Reporting
### Will reports be sent to Managers/CEO’s to show accounts in their hospital that don’t have manager.  Would be VERY useful to do this.
Could also send a simple list of all users in the hospital grouped by manager and highlight the ones with none.
Then if the manager is wrong or out of date instructions in report would be to contact HR for it to be updated.
Future Feature request for Workday team to generate exception reporting
If IAM receives a new account that doesn’t have a line manager, there’s an alert notification for IAM Ops


## 
### 



## HR Interactions
### Are we still allowed to manually disable if instructed by HR/CEO
Yes, in case of Emergency termination only. Manually disabling an account is part of emergency termination, which is to be carried out by SD as per current process.
After SD disables the AD account, User's line manager needs to trigger involuntary termination in Workday as HR business process. 
Aside to this emergency termination process, terminations are automated and for users managed by Workday, SD are not supposed to deprovision the account.
Emergency termination for Digital Accounts are to be done by IAM Operations. Refer to IAM Support matrix.


## 
### If we get asked to grant access to email/H drive for currently employed staff member
Follow the current state Process that requires HR/ Higher manager & CEO approval.


## 
### If we get asked to grant access to email/H drive for x employe.
Manager automatically gets assigned full rights to employee’s H-drive post termination.
If someone else needs it, can be assigned by SD based on Higher manager & CEO approval as per current process.

Email: To retain email, please consult Platform Operations.


## 
### If a new hire wants H or Email of previous person.
H Drive – SD can assign based on Line Manager’s approval.
For Email – the account would need to be retained past their termination date, senior manager/ CEO/ HR approval need, contact Platform Operations.


## 
### 



## Troubleshooting
### Employee is having difficulty with their digital identity
Employee to call IT Service desk.
SD to follow the triage process - 
Before raising a ticket to IAM, please check whether if Hire date is within 7 days of receiving the issue. If yes, check the Okta broker to see if user profile is present (if present, user have activated their Digital Account and have forgotten about it), if not present, advise the user to check their all inboxes including junk and spam, if issue persists, raise an incident to IAM Service Now Queue capturing all relevant information below.
Full name
Site
Role
Start Date
Employee ID


## 
### Employee is having difficulty using their digital identity to login to a system that uses that.  Mytime/Workday.
Employee to call IT Service desk.
SD to follow the triage process – assign the ticket to IAM or MyTime application team based on the Triage.


## 
### Employee is having difficulty using their AD account to logon to Mytime/Workday.
Employee to call IT Service desk.
SD to follow the triage process – assign the ticket to IAM or MyTime application team based on the Triage.


## 
### Lookup of RUID and employee id
SD has access to Okta Identity broker where they can check the RUID written against the employee profiles.
The same RUID is also available in Extension attribute1 for Active Directory/ARS.
RUID is populated under other Ids in employee record in Workday.
To look for RUID in Entra Id, check for User properties and then click on view for Extension attributes. Value of Extension Attribute 1 is the RUID.


## 
### 


Support Category | Support Level | Team Responsible | Service Now Queue | Contact | Escalation Point | Hours of Operation

Workday | Level 1 | Workday Helpdesk (Tier1 Support) | Workday Support | Workday Helpdesk Number: 1800-560-556 | Director – People Operations

Email – 
Mobile - +61437508555 | Monday to Friday – 8:00 am to 5:00 pm nationally.

Workday | Level 2 | Workday Tier2 team | Workday Support (Both Tier1 and Tier2 currently have same ServiceNow Queue) | Team DL: 

Functional Lead: Benny Coutinho
Email: 
Mobile: +61477801729

Technical Lead: Vijay Raja
Email: 
Mobile: +61477801729 | Mobile: +61 415 580 045 | After Hours Support Line: 02 9433 1460 (Option 4)

Okta | Level 2 | IAM Operations | IAM | Team DL – iamoperations.rhc@ramsayhealth.com.au | Head of IAM: Hema Tandel

Email: 

Mobile: +61448022957 | After Hours Support Line: 02 9433 1460 (Option 4)

Active Directory/ ARS Workflows | Level 2 | Platform Operations | IT Infrastructure | Tickets are assigned to the below queue depending on the incident –
Infrastructure Services – IT Systems
Infrastructure Services - Cloud | Primary Escalation point: Aaron Fenton (IT Platforms Operations Manager)
 
Email: 
 
Mob: +61 427 943 430
 
Secondary Escalation point: Boris Napernikov (IT Platforms Manager)
 
Email: 
 
Mob: +61 412 485 505 | Monday to Friday: 8:00 am to 5:30 pm AEDT.
 
Service desk number: 1800 243 903, Platforms.
 
Anything outside these hours goes to the person-on call if it’s an emergency.
 
After hours, service desk can call on 02 9433 1460 for escalation/support (IVR with options for multiple teams) Systems is Option 1
