# Lab 3.2: Exporting data from HDFS to RDBMS.

### Step 1: Connect to your EMR.

### Step 2: Change directory by giving the path of your files by using following command and View the content of the file salarydata.txt.

![Screenshot from 2020-07-02 14-12-15](https://user-images.githubusercontent.com/64689497/86355453-4e182200-bc88-11ea-862a-6330aaf9800b.png)

### Step 3: Create a new hdfs directory using mkdir command salary2 and put salarydata.txt into this directory by following command.

![Screenshot from 2020-07-02 14-14-17](https://user-images.githubusercontent.com/64689497/86355484-5a9c7a80-bc88-11ea-9ec1-4137e0d358bf.png)

### Step 4: Check whether the data is been transferred.
    hdfs dfs -ls salary2

### Step 5: Create a new table in database as salaries2 using following SQL command.

    create table salaries2 (gender varchar(1), age int, salary double, zipcode int);
    
### Step 6: Export data from HDFS to Database.

Run the following Sqoop command that exports the salarydata folder in HDFS into the salaries2 table in MySQL.

![Screenshot from 2020-07-02 14-33-13](https://user-images.githubusercontent.com/64689497/86355515-65570f80-bc88-11ea-876b-06b7456a6df6.png)

![Screenshot from 2020-07-02 14-33-19](https://user-images.githubusercontent.com/64689497/86355520-68ea9680-bc88-11ea-8753-b3c730cafbb2.png)

### Step 7: Verify it by viewing the table’s contents from the MySQL

![Screenshot from 2020-07-02 14-37-05](https://user-images.githubusercontent.com/64689497/86355540-73a52b80-bc88-11ea-9a94-860fe6ed42e9.png)




