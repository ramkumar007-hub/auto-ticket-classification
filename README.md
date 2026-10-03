# auto-ticket-classification
ServiceNow Flow Designer project that auto-classifies school IT tickets by keyword and emails the caller
Auto Ticket Classification using Flow Designer

A ServiceNow project that automatically classifies school IT helpdesk tickets and emails the caller, with no code.

Problem

IT staff manually read every incident (Wi-Fi, projector, password, slow computer), pick a category, and notify the caller. This is slow and inconsistent.

Solution

The user enters only the Caller and Short Description. When the record is created, a Flow Designer flow checks the description for keywords, sets the Category and Subcategory, and sends a confirmation email.

Short Description contains	Category	Subcategory
Wi-Fi / Network	Network	Wi-Fi
Projector	Hardware	Projector
Forgot password	Access	Forgot Password
Slow computer	Performance	Slow Computer
Contents
sys_remote_update_set_507d9b88187b03107f44ef1706607300.xml: the exported update set
Custom table Incident WorkFlow with auto-numbering
Dependent Category and Subcategory choices
Flow: Auto Classify School IT Tickets
Role and ACLs for the table
How to Import
In ServiceNow, go to System Update Sets, then Retrieved Update Sets.
Click Import Update Set from XML and upload the file.
Open "Project Update Set", then Preview and Commit.
In Flow Designer, make sure the flow is Active.
Test

Create a record in Incident WorkFlow with the short description "WiFi not working in library". After saving and reloading, Category is Network and Subcategory is Wi-Fi, and the caller receives an email.

Built With

ServiceNow (Personal Developer Instance), Flow Designer
