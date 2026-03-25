
MONGODB PRACTICE 

  
1.NOTES REGARDING THE PRACTICE
When you see the dollar sign in a command you need to execute, note this is just a command prompt indication. You do not
need to actually write the “$”, as it is not part of the command.
For all practices below – write all the commands you have used in a “Practice answers document”.
When you are complete, you can submit this document for review.

2.CONNECT TO THE  THE MONGODB  ENVIRONMENT
Verify the “ MongoDB ” environment is up and running:
docker ps -a
Open a BASH session to the practice environment
docker exec -it Mongo /bin/bash 

  
3.GENERAL DETAILS AND PRACTICE PREPARATION ( 5)
Download the “ products.json ” file to your computer (for example, to “c: \temp”) and copy it to “/data/products.json” in the Docker container.
See the Guidelines documents if you require assistance on this.

4.IMPORT PRODUCTS DATA INTO MONGODB ( 15)
Import the products information from the JSON file you have loaded into MongoDB.
Import into a collection named “products” and a database name “epam”
Specify the default MongoDB port in the relevant parameter
Specify an option so that the collection will be dropped i f it exists before loading  the new data
View the relevant command options using “ --help" to find the relevant option
See the Guidelines documents if you require assistance on this.

5.VERIFY  THE LOADED DATA IN MONGODB (20)
Login to MongoDB
Do we have to spe cify the hostname and port number? Why?
What is the MongoDB version?
Check – what options are available in MongoDB for the following:
Databases
Collection
Find options in collections
See the Guidelines documents if you require assistance on this.
Check – Which databases currently exist in this MongoDB instance?
Switch to use the database named “epam”
Check – Which collections currently exist in the database “epam”?
List all data in the collection “products”
Check – How many documents currently exi st in this collection?     
  
6.CRUD OPERATIONS IN MONGODB COLLECTIONS (40)
Insert the following new document to the “products” collection  with the following attributes :
Product id: “ac9”
Product name: “ AC9 Phone ”
Product brand: “ACME”
Product type:  “phone”
Product price: 333
Product Warranty (in years): 0.25
Product availability: true
Perform queries to display products according to the following requirements :
Query 1:
•Skip the first 2 products  and display the next 10 products in the collection .
•Make the output in an easy to read JSON format. (Each field and its value should  appear in a separate row)  
Query 2:
•Display only the “name” and “brand” fields  for each product .
Query 3:
•Display only the “id” and “limits” fields  for the first 10 products
•Collect the results into a single array , in which each element is both “id” and “limits” of a specific product.
•Examine the result you have received:
Did all “id” values had a matching “limits” value? Why so?
Query 4:
•Display the IDs, names and prices of all products of which prices are greater or equal to 200.
Query 5:
•Display the IDs, names and prices of all products.
•Sort the result according to price in descending order and name in ascen ding order (secondary sort)
Query 6:
•Write a query that displays how many products we have of type “service”. (Check the field which is named
“type”) 

Updating records
General questions
•Can we update the “_id” field? Why so?
•When should we use the “ set” keyword?  What happens if we omit it?
•When shoul d use the “ multi ” keyword?
Please perform a query after each of the following updates to verify you have updates the documents as expected.
Update 1:
•Update product with ID “ac3”, so that he will now have only the following field values:
•company: “EPAM”
•item: “MongoDB”
Update 2:
•Update all products which have “ac3” somewhere in their name, and add a new field to their document –
“subtype” with the value “AC3”.
Note that the “ac3” string in the name can be either lower or upper case.
Deleting records
Remove all records of type “s ervice”.

7.USING INDEXES ( 5)
Create an index for the “price” field
Create a compound index for “type” and “subtype” fields
Create a text index for the “name” field.
What is the benefit of a text index over a regular index?

8.ARCHITECTURE AND MONITORING (15)
Consult the guidelines document if required for assistance on the following requirements.
Run a command which describes the current MongoDB node .
Change the command to display only the local time of the current instance.
Run a command which describes the current state of the database , with all its metrics and stats .
Display information about all currently running operations in the database instance.
Check – are replication sets currently enabled?     
 

