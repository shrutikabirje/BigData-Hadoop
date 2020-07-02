#   LAB 3.1 - Import data from RDBMS to HDFS.

### Step 1: Create a database using Amazon RDS which will be of SQL free tier.

### Step 2: Connect this database with MySQL workbench.

For connection with MySQL Workbench:

a. Give connection name.

b. Hostname will be endpoint of your RDS which you made on AWS.

c. Username & Password will be the same as you entered in AWS RDS.

d. Then test connection, your connection will be made.

### Step 3: Create a salaries table in SQL using the following command.

    create table salaries (gender varchar(1),age int,salary double,zipcode int);
    
Now load the data in salaries.txt file in this salaries table using following command.
  
  load data local infile 'path of your (salaries.txt)file/salaries.txt' into table salaries fields terminated by ',' ;

If you get error while executing this follow the steps:
  
    a. Close your connection.
    
    b. Right cick on your connection and select EDIT CONNECTION.
   
    c. Go to advanced and add following line to Others:
        
        OPT_LOCAL_INFILE=1
        
    d. Now connect to your connection.
    
### Step 4: Connect to your EMR.

Note:-

    While making EMR go to advanced and select SQOOP.
      
    Next delete the last node as we dont need it and keep instances 0 and m4.large cluster.
      
### Step 5: Once your EMR is connected run the following SQOOP command to import data from SQL database to HDFS.


### Step 6: Now check whether the data is present in hdfs or not.


### Step 7: To check the content of the file use cat command.


### Step 8: Now we will try to import only salary and age from the database and put it into new directory named salaries2.


### Step 9: Now writing a Sqoop import command that imports the rows from salaries in MySQL whose salary column is greater than 90,000.00 using split by.


### Step 10: Check whether salaries3 directory is created on hdfs.


### Step 11: View the contents of part‐m‐00000 and part‐m‐00001 use cat command.

