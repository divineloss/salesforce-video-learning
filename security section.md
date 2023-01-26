# Salesforce Security Overview

Controlling Record Access - Ways to control the access to records on a profile and/or user basis

<b>Most restrictive to least restrictive:<b>

OWD (Organization Wide Defaults) --> Role Hierarchy --> Sharing Rules --> Manual Sharing

# Organizational Security Settings

Go into security settings to Health Check to see where the vulnerabilities are in terms of security settings. 

Password policies - Section where you can modify the numever of login attempts, password type, etc.

Session settings - Includes session timeout (how long someone can stay logged in before getting kicked out of session)

Network access - Includes IP range, which is a range of IP addresses that users can log in from without having to verify identity. Users don't have extra questions from Salesforce before logging in. Also called "white-listing". Login IP Ranges are used to only allow users to login using specific IP Addresses and are only available in profiles. Network Access controls the ability to bypass computer authorisation.

Login Access Policies - Setting where you can log in as a user without needing their password. Good for testing out things. If admin logs in as user, you can get audit trail that shows history of user but doesn't specify that it's an admin. 

View setup audit trail - Shows all changes that have happened in Setup. 

Expire All Passwords - ability to expire all users' passwords

Remote Site Settings - if there's a process that has been invoked within Salesforce, this lists which websites can be invoked by said process. You can add new remote site.

Encryption - Two different types:
	- Platform Encyrption
	- Standard Field Encryption

Login History - Can see who is logging in from where, what type of brower, what kind of login, status, application, client version, API type, API version, login URL login time

# Organizational Wide Defaults

Has two default settings:
	- Public Read/Write: Anyone can read and edit object. You have to change model even if you only want to grant access to even one record.

# Record Ownership

If you change ownership of a record, then the person who was the original owner no longer has access to a record. 

Queues: only apply to certain objects (leads, cases). You can assign people to a record using queues. 

When you set an object private, user who creates record is owner. That is assuming there's no sharing rules in place. 

# Role Hierarchies

If one creates records and there's users under that person in the hierarchy, they can't see that record. However, if the users underneath that person create records, that person above them CAN see the records. 

You can control accessibility of records in org in this manner. Anybody on same level of a user in hierarchy can't see anyone elses records on same level. 

# Sharing Rules

Shares records across role hierarchees instead of up and down. 

You share them using (Sharing Rules):
1) Roles
2) Public Groups

Sharing Access Level (Permissions):
1) Private
2) Read Only
3) Read/Write

Criteria based sharing: based on specific data within records. For example, any won opportunities will be shared with entire organization could be a criteria-based sharing rule. 

# Object Permissions & Record Access/User Profiles & Permissions

A user needs to have access to the object to allow them to see the object and for the the OWD sharing rules and everything else to work. They also need to have permissions before you can get to OWD for that object. 

Two main differences between profile & permission set is that one profile can only be assignd per user, while a user can be assigned multiple permission sets. You use the permission sets to give additional functionality to individual people (i.e. creating reports for certain people within a sales team)

# Permission Set Groups

A profile can have multiple permission sets assigned to them. Permission sets were created to get around users being assigned only obe profile. 

Setting the proper permission sets: Prevent spread of malware, decrease large amts of data being expose for attack, and improves user productivity. 

Permission group streamlines the permission set management. 

Muting permission set: removes permissions within a permission set group for a user but can only be used within a permission set group. It can be overriden by the user's profile (i.e. they have Read/Write permissions on the account object but muting permission set has been set, so they would still have read/write permissions despite that)

# Restriction Rules

Restricts fields that users can see. Accessible in the object manager for the object in question. The criteria for who can/can't view the field and type of record is set up. 

# Setup Audit Trail

Audit Trail tracks changes made by admins. It tracks:

General Administration
Profiles
Permission Sets/Groups
Customization
Security & Sharing
Data Management
Development