# Data Management

Managing Duplicates

You can create a duplicate rule that alerts users to when they're creating a duplicate record. You can have the system identify whether it's a duplicate record or not by creating a matching rule, which is essentially a conditional rule. This is all done in setup. 

Importing Data

3 ways you can do it:
1) Import Wizard - Not a standalone application and is found in Setup. Prevents duplicates when importing new records and uploads up to 50000 records and can choose whether or not to trigger workflow rules and processes. 
2) Data Loader - Is a standalone application on both MacOS and Windows. Can import up to 5000000 records. Cannot prevent dupliates when importing new records and cannot choose whether or not ot trigger workflow rules and processes. 
3) DataLoader.io

Salesforce ID & External IDs

Salesforce ID is a unique identifier for records in Salesforce

External ID field can be created to import external data

When uploading data, you need to consider:

1) Validataion rules
2) Duplicate Management
3) Code
4) Bad quality data

When importing data, make sure that:

1) You clean data before importing
2) Make sure the fields exist before importing data
3) Make field columns the same names as fields in Salesforce
4) Test in a Sandobx first or small batch of records
5) Understand the limitations of using Excel (the data quality may be bad when importing from an Excel document, like in phone number or date fields)
7) Timeliness of report, cleaning and importing of data
8) Understand the impact to your users
	- Run outside business hours & freeze users
	- Turn off workflow & process rules before running insert, update or upsert operations. 


Two ways to back up data:
1) Backing up actual data (this is important for the exam)
2) Backing up configuration & setup itself

Toolsfor backing up data:
1) Data Loader
2) Manually exporting reports
3) AppExchange Service
4) Data Export (Setup)

# Mass Action Functions

Two different features:
1) Mass Transfer - You can transfer things like accounts, leads, service contracts (only standard objects you can transfer) and custom objects to other owners
2) Mass Delete - Mass deleting records based on criteria

Both take the security setup of users into account. 

Salesforce Content
there is a Salesforce CRM content user option in user info. That should be checked always.

There are two content related things:
1) Content -
2) Libraries - Have things like Popular tags, recent activity, most active contrivbuters, members, top content. You can upload content and give access to different people. 

# Document Folder & File Uploading Review

Chatter can be one way to attach a file (Salesforce files)
Record detail page is also another way to attach a file (page layout) or if it has chatter enabled you can do it that way too
You can contribute content via library
Salesforce documents is another way. You create a folder within the documents section


# Sales and Marketing Applications 

Understand the capabilities aqnd implications of the Sales process
Understaned & identify teh important productivity features
Describe the capabilites of Products & Pricebooks
Identify who to automate lead management
Describe capabilities of campaign management
Describe the capabilities of Activity management

Two types of cloud:
1) Sales Cloud - Manage sales processes and captures sales data (leads, opportunities, accounts, contacts, campaigns)
2) Service cloud

# Sales overview

Starts with getting a Lead (potential customer that you eventually convert into a contact and opportunity)

Lead Sources can be:
 - Emails
 - Website
 - Event
 - Social media
 - Marketing Cloud
These come into Salesforce as a Lead record. Using the info above, the user does a lead conversion which allows an Account, Contact, and/or Opportunity to be created or to be linked to an account/contact if they already exist. Once Opportunity is created, that is when the sales process starts to kick off. 

Campaigns work all across the above process. Allows to track which leads have come in through which campaigns. You can calculate ROI (return on investment) for a particular campaign based on how the opportunity closed. 

Web to Lead - This is a way to bring in a lead where you use a website or online method of bringing in a lead. This is created in Setup and you can add in fields you want to include in the website template for the potential lead to fill out. the lead fills it in and submits it and then it's created as a Lead record in Salesforce. 

# Lead Scoring

Determines what makes a good lead. Some apps within Salesforce can do the scoring but otherwise you can do it yourself. 

# Auto response rules

Auto respond to leads being created. If someone fills in info on website and lead is created, you can create auto response rule that includes an email that is sent to the lead. 

Lead Conversion

Process - You can click the convert button on a lead that open a page where you fill in the information about Account, Opportunity. two things happen:
1) Lead disappears from Salesforce
2) Based on data on lead, there might be certain field data you want to put on the opportunity record or account record. 


Products & pricebooks

When an opportunity is created, we can select a specific price based on what that product is in the pricebook. 


Sales Productivity Features
You got:

- Big Deal Alters: Allows to send email to group that tells the big opportunities in pipeline, based on probability
- Update Reminders: Email that can be sent to managers that lists all opportunities that are open and what was the last activity
- Similar Opportunities: Related list on the opportunity which allows to search for similar opportunities
- Competitors: identifying competitors at beginning of creation of opportunity so we can see strength and weaknesses of competitors
- Team Selling: giving access to opportunity based on the team on it. Allows to set permission such as Read only, read/write for the people on team



Campaign Management

You have many things on campaign objects. Related lists include opportunities reltaed to campaign, campaign members which include leads, contacts. Ex: person at tradshow submits a web to lead form so the tradeshow will be part of the campaign. You can add campaign members onto this campaign to build up list of who to target. 

Campgain influence looks at what multiple things influence a sale in terms of campaigns. Looks at the lead or contact and what they have touched in terms of campaigns during a set of time that you as an admin establish. 

ROI is determined by lead, contact, opportunity. 


Paths

Set up as standard on standard opportunity object. Visual representation of picklist field on the record and in the opportunity object/record, its the stage field

enable path in org
create a path
configure the last path settings in setup
decide where path should appear on the record

Einstein Opportunity & Lead Scoring

AI that is used to score leads and opportunity records. high score represents lead or opportunity that is more likely to convert. 

Forecast Impact in Sales

Grouped around three areas:
User owner changes
opp record changees
territory changes

Sales Pipline - View of all SF opportunities, regaardless of stage they're in
Forecast - Subset of those opportunities and grouped by expected close date of sale

ex: expected revenue = amount/probably percentage

Forecasting can be affected by:
1) Opportunity Changes
	- Owner
	- Stage
	- Amt
	- Close Date
	- Probability
	- Expected Revenue
2) Territory mangement
	- Territory Strcture
	- Account Record Changes
3) Other Changes
	- Proeduct Family
	- Opportunity Splits
	-Overlay Splits
	-Custom Opportunity Field

Global Actions

Actions outside of a specific object and are on nav bar on mobile


Activity Management

From UI interface, you can go into the related list on an account or opp to create a task or an event, which both fall under activities. Otherwise, go into setup for backend. 


Chatter

Users or groups of users collaborting (like facebook) where you can share files and talk about files. Can collaborate on records. 

You get recommendations on the right about who to follow, what records to follow (if you own them)

Broadcast only - only new members can create posts. 


Salesforce App Exchange

Theres Salesforce Lab apps

You also have mapping type components that are free. 

Bulk solutions (main apps), lightning data apps, flow solution apps, lightning components that can install and put on layout. 

You use app exchange when you want to expand a very complex piece of logic that you can't solve using platform tools



# Service & Support Overview

Describe capabilities of CM
ID how to automate CM
Describe capabilities of solution management
Describe the capabilities of Portals
Describe the capabilities of Community Applications
Describe capabilities of Salesforce knowledge

Case Object


Knowledge vs Solutions
Knowldge is sidebar that has articles you can click on. You can post knowledge articles to a URL or community so users can see them or customers can see them from portal. 


Salesforce Communities/Experience Cloud
This is shown as "Digital Experiences" under "Feature Settings" in Setup. 

Customer Community has chatter collaboration, community management, social intelilgence, business data, customisation, platofmr. 

Partner Community has Salesforce Automation, Data SHaring Controls, Marketing and Content. More expensive than previous one and has acess to more objects including custom objects/dashboards. 

Employee Community
Similar to Customer community but has more stuff


