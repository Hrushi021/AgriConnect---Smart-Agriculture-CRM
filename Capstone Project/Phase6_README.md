Phase 6 User Interface Development

Lightning App Builder 

oThis was the primary tool used for all declarative UI design. Used the Lightning App Builder's drag-and-drop canvas to create and modify the custom pages.

Record Pages 

Various Record pages can be created :

Steps: 
(Same Steps can be applied to all pages)

1.Lightning App Builder → New → Record Page → Object = (select your object) eg : Crop__c → name  eg: Crop Record Page.
2.Template: Choose any Template  (Ex : One Region with Right Sidebar (or Two Columns).
3.Add Components as per requirement into Canvas ( Drag & Drop)
4.Example:
Top: Highlights Panel (compact layout show Crop Name, Quantity, Price).
Main: Record Details (all fields: Variety, Harvest Date, Quantity, Price).
Right sidebar:
Related List — Single: select Deals (show which deals reference this crop)
Report Chart: show a small chart (e.g., Crop sales trend or low-stock chart).
5.Save → Activate → assign app & profiles ( eg : AgriConnect app & profiles.)

i have created :
Farmer Record Page 

Crop Record Page 

Record Page 
 
Deal Record Page 

AgriConnect HomePage 

(This page is a app page not a record page)


Lightning Web Component (LWC) 

(Use LWC when you need custom UI/UX. Below are small, clear examples you can use in AgriConnect)

Step 1: Install & Open

Install the Lightning Studio Chrome extension.
Log in to your Salesforce Org in Chrome.
Open the Lightning Studio extension (you’ll see an editor pop up in the org).

🔹 Step 2: Create a New Component
Click + New → Lightning Web Component.
Give your component a name, e.g., farmerCard.
Select where to save → usually under lwc/farmer Card.
The extension will auto-create 3 files:
farmerCard.html (markup/template)
farmerCard.js (JavaScript logic)
farmerCard.js-meta.xml (exposure config)

🔹 Step 3 : Write Necessary Code

🔹 Step 4: Save & Deploy
In Lightning Studio, click Save → it auto-deploys to your Salesforce org.
If successful, you’ll see a confirmation message.

( This saves the setup and configuration of VS studio or Salesforce CLI ) 

farmerCard.html (markup/template) :
farmerCard.js (JavaScript logic) :
farmerCard.js-meta.xml (exposure config) :


OR, 


Flows 
       ( Flows can be used as an alternative for LWC )
Steps:

1.Navigate to Flows: From the App Launcher, search for Flow
2.Start a New Flow: In the Flows panel, click the New button. 
3.Select Flow Type:  For Example Choose Screen Flow from the options 
4.Add a Screen Element: On the Flow Builder canvas, click the + icon and select the Screen element. 
5.Configure the Screen:
6.Give your screen element a unique API Name and a descriptive Label. 
7.In the left panel, find the desired components (e.g., Text, Lookup, Email) and drag them onto your screen. 
8.For each component, provide a unique API Name and a user-friendly Label. 
9.Set components as required if necessary, using the Configure Footer option to customize button labels (like "Next" or "Finish"). 
10.Add Other Elements (if needed): Use other elements like Create Records or Get Records to interact with Salesforce data and connect them to your screen elements. 
11.Save and Activate : Click the Save button in the Flow Builder to save then click Activate

A Screen Flow for new Entry in the records 

