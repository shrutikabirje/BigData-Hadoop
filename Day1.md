# Lab: Using HDFS Commands
## Steps to be performed in this lab.

### * Step1. Viewing the hdfs dfs Command.
![Screenshot from 2020-06-24 22-25-45](https://user-images.githubusercontent.com/64689497/85608752-00415f80-b673-11ea-9071-b401d62d44b8.png)




### * Enter -ls command to view the contents of the HDFS root directory.
![Screenshot from 2020-06-24 22-26-54](https://user-images.githubusercontent.com/64689497/85609087-59a98e80-b673-11ea-8035-df604552b63e.png)

### Step2. 
a) Create a directory in hdfs.

    hdfs dfs -mkdir test
   
b) Verifying that the folder is created.

![Screenshot from 2020-06-24 22-28-37](https://user-images.githubusercontent.com/64689497/85610187-667ab200-b674-11ea-8ca3-8b10508de721.png)

c)Create a couple of subdirectories for test using -p and
view the contents of a folder recursively using -R :

![Screenshot from 2020-06-24 22-29-16](https://user-images.githubusercontent.com/64689497/85611382-86f73c00-b675-11ea-90fd-6b0764cc8468.png)

### Step3. Delete directory
  Delete the test2 folder (and recursively, its subcontents) using the -rm -R command
![Screenshot from 2020-06-24 22-29-48](https://user-images.githubusercontent.com/64689497/85614201-4b11a600-b678-11ea-9d02-09e92b6c2780.png)

![Screenshot from 2020-06-24 22-30-23](https://user-images.githubusercontent.com/64689497/85614242-52d14a80-b678-11ea-818e-d69c5c4eeb82.png)


  
### Step4. Upload a File to HDFS
a. Wget is used to download files from server.

b. Then unzip the labs.zip folder.

![Screenshot from 2020-06-25 00-06-50](https://user-images.githubusercontent.com/64689497/85614267-595fc200-b678-11ea-9490-3a423e93c651.png)

c.By running ls labs command you will get the content of labs folder and pwd will give you the path.
 
 
d. Then by entering the path you will get into Lab2.1.

   This folder contains a file named data.txt to view this file run the following command.
   
   Run the following -put command to copy data.txt into the test folder in HDFS:  
   
       hdfs dfs -put data.txt test
   Verify that the file is in HDFS by listing the contents of test:
   
       hdfs dfs -ls test
   
  
### Step5. Copy a File in HDFS

a. Copy the data.txt file in HDFS using the -cp command.

b. Verifing that the file is in both places by using the -ls -R command on test.
 
c. Deleting the data2.txt file using the -rm command.
  
  
### Step6. View the Contents of a File in HDFS

a. Using the ‐tail command to view the end of a file.

### Step7. Getting a File from HDFS
a. Use the get command to copy test/data.txt from HDFS into your local /tmp folder.



      







