# TASK2_HBase_Practices

1.CONNECT TO THE  THE HBASE  ENVIRONMENT
Verify the “ hbase ” environment is up and running:
docker ps -a
Open a BASH session to the practice environment
docker exec -it hbase /bin/bash


3.GENERAL DETAILS
View the HBase  related scripts in the HBase  “Bin” directory
▪Hint: The location of the base directory  should be in “/opt”
▪You should see ~25 scripts
Enter HBase Shell
Get the HBase status in different levels
▪Retrieve base status, simple status, and detailed status
List all filters
List all tables


4.TABLE AND DATA CREATION  (30)
Create a table with the name: “ employees ” with the following column families
▪personal_data
•Store 2 versions for this column
▪professional_data
•Store 4 versions for this column
List all tables
Insert data for ten employees
▪The id of each employee  must be a unique  value
•Insert employee’s  id to be 1 - 10
▪Fill the following data
•personal_data
•first_name
•surname
•age
•professional_data
•role
•expertise
Scan employee table to print all rows
Get all data of employee with id 7
Update age and role of employee number 3
Get all data of employee with id 3 and make sure updates appliedMastering Advanced  

5.QUREY DATA  (60)
Query all record in employees table
Get all data of employee with id 3 and the 3 last versions of his column families: personal_data, professional_data
Get all data of employees with age bigger or equals to  40
Get only role value of all employees with age bigger than 35
Count the number of all employees
Count the number of employees with age less than 40
Delete the new er age (that updated in topic 4) for employee with id 3
Get the data of employee with id 3 and validate his age reverted to first value

6.DELETE TABLE  (10)
Delete table employees 


