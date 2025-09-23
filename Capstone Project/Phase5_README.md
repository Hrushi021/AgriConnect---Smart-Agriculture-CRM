🌱 Phase 5: Apex Programming

🔹 Create an Apex Class

Example: Utility class to calculate total crop value.

Steps:

1.In Salesforce → Setup → Quick Find → Apex Classes → New.
OR  Developer Console → File → New → Apex Class.

2.Enter Class Name and click OK.

3. Write Apex code implementing the required logic. 

4. Save the class.




🔹 Apex Trigger 

When a Deal is Closed Won, automatically update the available Crop quantity.

Steps to Create Trigger: 

1.Developer Console → File → New → Apex Trigger. 

2.Select Object

3.Write Trigger code . 

4. Save the trigger

Example :Let’s create a Trigger i.e. 
       When a Deal is Closed Won, automatically update the available Crop quantity.

Steps:

Setup → Apex Triggers → New Trigger.
Select Deal__c object.
Add Trigger Code as mentioned in screenshot
Save & Test: Close a Deal → Crop stock reduces





🔹SOQL (Salesforce Object Query Language)
      
          ---- Used to query data inside Apex.

 Example Query:
  
List<Farm__c> farmers = [SELECT Id, Name, Address__c 
                          FROM Farmer__c 
                          WHERE Address_c = 'North'];


‘Queries Can Run in developer console’

i.Enter Ctrl + E to open window for code

ii.Enter Query followed by Debug Command

iii.Click Execute





🔹Collections: List, Set, Map

List: Store multiple Farmers

Set: Unique crop names.

Map: Match Farmer IDs with Names.





🔹Batch Apex 

Batch Apex – Weekly Update Crop Reports : 


🔹Queueable Apex 

Queueable Apex –Visit Reminder : 


🔹Schedule Apex 

Scheduled Apex – Run Every Week : 

Setup → Apex Classes → Schedule Apex or via Developer Console.






🔹Test Classes

Requires 75% code coverage.

  Steps:  
Setup → Apex Test Execution → New Test.
Enter the test class name
Enter test class code 
Save & Run

 Steps to run via setup :
·  Go to Setup → Apex Test Execution.
·  Click Select Tests → Pick VisitReminderQueueableTest.
·  Run Test → Wait for result


succesfully created and implemented apex clases , triggers and also tested
  
Example :  test for CropHelper  (sends remainder for visit) 
