Phase 7: Integration & External 
Access


1. API Limits 

• Salesforce tracks the number of API calls made by external systems or 
integrations.

• In AgriConnect, all major actions (Farmer Registration, Visits, 
Buyer related, Deals etc) are handled inside Salesforce. 

• No external APIs are currently being used in this project, so API limits 
are not a concern. ( Below screenshots shows 123 API requests that is 
because System administrator has some other applications like marketing 
but our CRM don’t)

• You can monitor API usage in Setup → System Overview, but no 
special configuration is required





Phase 8: Data Management & 
Deployment


 Duplicate Management 

Prevent duplicate Farmer records (by Email/Phone/Name) and surface potential 
duplicates during data entry or import. 

1) Create the Matching Rule 

1. Setup → Quick Find → Matching Rules → New Rule. 
2. Object: Farmer
3. Rule Name: Farmer Match (or any name). 
4. Add Matching Criteria: 
o Field = Farmer Name → Matching Method = Exact. 
o Field = Email → Matching Method = Exact. 
o Field = Address → Matching Method = Exact. 
o Field = Phone → Matching Method = Exact. 
5. Save the rule. 
6. Click Activate (only active rules can be used by Duplicate Rules). 


2) Create the Duplicate Rule 

1. Setup → Quick Find → Duplicate Rules → New Rule. 
2. Object: Farmer. (same as that of matching rule)
3. Rule Label: Farmer Duplication Rule
4. Under Matching Rules, click Add and select the ‘Farmer Match’ matching 
rule you just activated. 
5. Action on Create: choose Alert (start in Alert mode while testing). 
6. Action on Edit: choose Alert. 
7. Save, then click Activate.



 Data Backup 


Steps: 

 Go to Setup. 
 In Quick Find, type Data Export → click Data Export. 
 Choose one: 
 Export Now → run a one-time backup. 
 Schedule Export → set weekly/monthly backups. 
 Select the objects you want: 
 Farmer, Visit, crop, Deal, Buyer and any standard objects you use (e.g., 
Users). 
 Click Start Export (for immediate) or Schedule Export (for scheduled). 
 Wait → Salesforce emails you when the backup is ready. 
 Download the .zip file from the export page → extract CSV files. 
 Store the backup securely (encrypted drive, company server, cloud storage).
Extracted ‘ CSV ‘ from zip :

I have Extracted :
crop_c.csv
Deal_c.csv
Visit_c.csv
Buyer_c.csv
Farmer_c.csv
