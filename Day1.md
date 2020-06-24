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

![Screenshot from 2020-06-24 22-33-03](https://user-images.githubusercontent.com/64689497/85622100-f2480a80-b683-11ea-8912-5151c302f82d.png)
 
d. Then by entering the path you will get into Lab2.1.

   This folder contains a file named data.txt to view this file run the following command.
   
   ![Screenshot from 2020-06-24 22-34-18](https://user-images.githubusercontent.com/64689497/85622114-f7a55500-b683-11ea-9c19-5c26baed64b4.png)

  Run the following -put command to copy data.txt into the test folder in HDFS:  
   
       hdfs dfs -put data.txt test
   Verify that the file is in HDFS by listing the contents of test:
   
       hdfs dfs -ls test
       
   ![Screenshot from 2020-06-24 22-35-14](https://user-images.githubusercontent.com/64689497/85622122-fc6a0900-b683-11ea-9eb2-e4cb5a3b8eac.png)
   
  
### Step5. Copy a File in HDFS

a. Copy the data.txt file in HDFS using the -cp command.

b. Verifing that the file is in both places by using the -ls -R command on test.

![Screenshot from 2020-06-24 22-36-21](https://user-images.githubusercontent.com/64689497/85618968-3389eb80-b67f-11ea-8861-3e5c95eca212.png)

 c. Deleting the data2.txt file using the -rm command.
 
 ![Screenshot from 2020-06-24 22-37-01](https://user-images.githubusercontent.com/64689497/85618988-3a186300-b67f-11ea-94ce-462e01978a1f.png)
  
### Step6. View the Contents of a File in HDFS

a. Using the ‐tail command to view the end of a file.

![Screenshot from 2020-06-24 22-37-40](https://user-images.githubusercontent.com/64689497/85619000-400e4400-b67f-11ea-8233-c730a26a65bc.png)

### Step7. Getting a File from HDFS 

a. Use the get command to copy test/data.txt from HDFS into your local /tmp folder.

![Screenshot from 2020-06-24 22-39-04](https://user-images.githubusercontent.com/64689497/85619012-456b8e80-b67f-11ea-8a5c-e43e0884af20.png)

### Step 8. The getmerge Command

a. Put the file /home/hadoop/demos/labs/small_blocks.txt into the test folder in HDFS.


![Screenshot from 2020-06-24 22-41-19](https://user-images.githubusercontent.com/64689497/85621179-79947e80-b682-11ea-915c-f0fcb3c944eb.png)

You should now have two files in test: data.txt and small_blocks.txt.

b. Run the following getmerge command:

![Screenshot from 2020-06-24 22-42-42](https://user-images.githubusercontent.com/64689497/85621194-8022f600-b682-11ea-8845-fe2c4d21b6c1.png)

### Step9. Specify the Block Size and Replication Factor

a. Put /home/hadoop/labs/Lab2.1/data.txt into /user/root in HDFS, giving it a blocksize of 1,048,576 bytes.

![Screenshot from 2020-06-24 22-42-42](https://user-images.githubusercontent.com/64689497/85621194-8022f600-b682-11ea-8845-fe2c4d21b6c1.png)

b. Run the following fsck command on data.txt.

![Screenshot from 2020-06-24 22-43-12](https://user-images.githubusercontent.com/64689497/85621204-84e7aa00-b682-11ea-8c0c-ad1914e151f5.png)






      







