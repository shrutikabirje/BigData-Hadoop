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

![Screenshot from 2020-07-02 12-25-59](https://user-images.githubusercontent.com/64689497/86352298-35593d80-bc83-11ea-8631-1471b5b57c42.png)


### Step 6: Now check whether the data is present in hdfs or not.

![Screenshot from 2020-07-02 12-42-08](https://user-images.githubusercontent.com/64689497/86352313-3c804b80-bc83-11ea-81d7-bddd5721407a.png)



### Step 7: To check the content of the file use cat command.

![Screenshot from 2020-07-02 12-44-34](https://user-images.githubusercontent.com/64689497/86352330-42762c80-bc83-11ea-96d8-eaa442b1c584.png)


### Step 8: Now we will try to import only salary and age from the database and put it into new directory named salaries2.

![Screenshot from 2020-07-02 12-49-06](https://user-images.githubusercontent.com/64689497/86352355-4ace6780-bc83-11ea-8992-8573beda4279.png)

![Screenshot from 2020-07-02 12-49-09](https://user-images.githubusercontent.com/64689497/86352366-51f57580-bc83-11ea-9b60-942c757b6d8f.png)

### Step 9: Now writing a Sqoop import command that imports the rows from salaries in MySQL whose salary column is greater than 90,000.00 using split by.

![Screenshot from 2020-07-02 13-26-47](https://user-images.githubusercontent.com/64689497/86352400-5cb00a80-bc83-11ea-9971-22a443712af0.png)

### Step 10: Check whether salaries3 directory is created on hdfs.

![Screenshot from 2020-07-02 13-17-38](https://user-images.githubusercontent.com/64689497/86352387-57eb5680-bc83-11ea-8004-b2c5b584db21.png)

### Step 11: To view the contents of part‐m‐00000 and part‐m‐00001 use cat command.

![Screenshot from 2020-07-02 13-27-12](https://user-images.githubusercontent.com/64689497/86352415-620d5500-bc83-11ea-9605-bdf6f8d8d4ff.png)

