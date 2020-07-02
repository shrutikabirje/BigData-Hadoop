# Lab 3.2: Exporting data from HDFS to RDBMS.

### Step 1: Connect to your EMR.

### Step 2: Change directory by giving the path of your files by using following command and View the content of the file salarydata.txt.

### Step 3: Create a new hdfs directory using mkdir command salary2 and put salarydata.txt into this directory by following command.

### Step 4: Check whether the data is been transferred.

### Step 5: Create a new table in database as salaries2 using following SQL command.

    create table salaries2 (gender varchar(1), age int, salary double, zipcode int);
    
### Step 6: Export data from HDFS to Database.

Run the following Sqoop command that exports the salarydata folder in HDFS into the salaries2 table in MySQL.

### Step 7: Verify it by viewing the table’s contents from the MySQL




