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
  
### Step4. Upload a File to HDFS
a. Wget is used to download files from server.
b. Then unzip the labs.zip folder.

      







