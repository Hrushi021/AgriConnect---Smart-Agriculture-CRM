Built a data model with 5 custom objects (Farmer, crop, visit, deal, buyer)
used Standard objects such as Account, oppurtunity
Established connections using Master-Detail, Lookup, and Junction object relationships
This makes AgriConnect flexible for farmer support, crop inventory, buyer management
1.Standard & Custom Objects 
➡️Process Flow: Setup → Object Manager → New Custom Object → Add Fields. All 
objects configured in a similar manner, with respective fields as listed  



Standard Objects :

Account (used for buyer or farmer cooperatives)
Opportunity (used for Deals between Farmer & Buyer)
Contact (used for indivisual Farmer and Buyer)


Custom Objects :

Farmer_c

Field LabelSorted Ascending	SortField Name	SortData Type
Address	Address__c	Text Area(255)
Created By	CreatedById	Lookup(User)
crop	crop__c	Picklist
Farmer Name	Name	Text(80)
Last Modified By	LastModifiedById	Lookup(User)
Owner	OwnerId	Lookup(User,Group)
Phone_Number	Phone_Number__c	Phone





Visits_c

Field LabelSorted Ascending	SortField Name	SortData Type
Created By	CreatedById	Lookup(User)
Last Modified By	LastModifiedById	Lookup(User)
Lookup	Lookup__c	Lookup(Farmer)
Owner	OwnerId	Lookup(User,Group)
Purpose	Purpose__c	Text(150)
Visit Date	Visit_Date__c	Date
Visit Name	Name	Text(80)
Visiter name	Visiter_name__c	Text(150)





Crop_c

Field LabelSorted Ascending	SortField Name	SortData Type
Created By	CreatedById	Lookup(User)
crop Name	Name	Text(80)
Harvest Time	Harvest_Time__c	Date
Last Modified By	LastModifiedById	Lookup(User)
Master detail	Master_detail__c	Master-Detail(Farmer)
Prize	Prize__c	Currency(18, 0)
Quantity	Quantity__c	Number(18, 0)





Buyer_c

Field LabelSorted Ascending	SortField Name	SortData Type
Buyer Name	Name	Text(80)
Contact	Contact__c	Phone
Created By	CreatedById	Lookup(User)
Last Modified By	LastModifiedById	Lookup(User)
Owner	OwnerId	Lookup(User,Group)




Deal_c 

Field LabelSorted Ascending	SortField Name	SortData Type
Created By	CreatedById	Lookup(User)
crop	crop__c	Picklist
Deal Name	Name	Text(80)
Farmer	Farmer__c	Lookup(Farmer)
Last Modified By	LastModifiedById	Lookup(User)
Lookup1	Lookup1__c	Lookup(Buyer)
Owner	OwnerId	Lookup(User,Group)
Quantity	Quantity__c	Text(150)
status	status__c	Picklist





2.Page Layouts
 
Configured for Farmer_c as an example: 
Process Flow: Setup → Object Manager → Farmer → Page Layouts → Farmer Layout
→ Drag fields into sections → Save.


RELATIONSHIPS

·  Farmer → Visit (Lookup).
.  Farmer (Master) → Crop (Detail).
·  Crop ↔ Buyer (Many-to-Many via Deal)

