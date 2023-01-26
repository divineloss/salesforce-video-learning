# Flows

Automated automation tool that is the standard for the platform. Automates processes for end users, particularly more complex ones. 

# Two types of permissions:
1) Manage Flows

2) Rum Flows

# Core Types of Flows

1) Screen Flow - Triggered from othe Flows, Custom Buttons, Links, Lightning Pages, Lightning Web Components, Flow Orchestrator, Web Tab, URL, VisualForce Page. This is a visual that the end user sees and guides them on the screen through the process. It's more streamlined. Can be launched from a lot of places.
2) Triggered Flows 
	- Schedule-Triggered Flow: Triggers at a Specific Time or Frequency
	- Record-Triggered Flow: Does Fast Field Updates, Actions & Related Records. Triggers when a record is created, updated, or deleted. 
	- Platform Event-Triggered Flow: Triggers on a Platform Event. For example, a flow can trigger when you sell something to a customer. 
3) Autolaunched FLow (No trigger) - Flows that are sitting on their own and only triggers on an APEX Call, Another Process, REST APIR, Flow Orchestrator, Web Tabs, Customer Buttons & Links, VisualForce Pages.
4) Flow Orchestrator - Orchestrates flow. Allows to chain multiple flows together in stages. Once flows in a stage are completed, you can move onto the next stage. Can be autolaunched or record-triggered (created, updated, deleted)

# Building Blocks of Flow

Start & End Element - Beginning and End of Flow

Elements - Broken down in to logic, interaction, data elements. 
	- Interaction: Screen
	- Logic: Using decision elements, collection sort, assignment
	- Data: Create, update, get, or delete records
Connectors - Lines on flow or path the flow can take

Resources - Set of items that you've created that can be reused throughout the flow. An example could be multiple chatter posts in every chatter element where you can reuse the text, or reuse that element. 

# Order of Execution

When you save a record in Salesforce, the platform starts evaluating things like evaluation rules, code, etc. it's important to understand the order of execution whenever a record is saved. 

# Main Steps

1) Loads the original record from the database of initalizes the record for an upsert statement.
2) Loads the new record field values from the request and overwrites the old values. 
3) Executes record-triggered flows that are confifgured to run before the record is saved.
4) Executes all <i>before<i> triggers
5) Runs most system validation steps again, such as verrifying that all required fields have a non-null value, and runs any customer validation rules. The only system vlaidataio tht Salesforce doesn't run a second time is the enforcement of specific layout rules.
6) Executes duplicate rules.
7) Saves the record to the database but doesn't commit it yet. 
8) Executes all after triggers (more code)
9) Executes assignment rules.
10) Executes auto-response rules.
11) Executes workflow rules.
12) Executes escalation rules.
13) Executes processes, flows launched by processes, flows launched by workflow rules. All Salesforce Flow automations.
14) Executes entitlement rules,
15) Executes record-triggered flows that are configured to run after the record is saved.
16) Performs calculations if the record contains a roll-up summary field or is part of cross-object workflow
17) If parent record is updated, and a grandparent record contains rollup summary of is part of cross object workflow, calculations occur.
18) Executes criteria-based sharing evaluation.
19) Commits all DML operations to the database. Data is actually committed to database. 
20) After all changes are committed to database, executes post-commit logic such as sending email and executing other steps. These steps are "queued up" in previous steps until this one.

# Breakdown of steps for exam

Required fields
Valiation Rules
Before Flows
Assignment Rules
Auto-Response Rules
Workflow Rules
Processes
Escalation Rules
Flows
After Save Flows
Post Commit Logic

<b>If ANY errors come up before last step, everything is rolled back</b>