# Lab Report 1(Remote Access and FileSystem Week 1)

 **In this lab report we will be using filesystem commands such as:**
 1)cd 
2)ls 
3)cat

## ```cd``` Command

```
bash $ cd
```
 <img width="499" alt="Screenshot 2024-04-10 at 6 21 58 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/f1a20af8-de62-49c9-8cca-ccf5fcbbe821">

*Working Directory : There is no change to be found in the working directory*

*Output: We are taken to the home directory when ```cd``` without an arguments*


```
$cd /path/to/directory
```
<img width="582" alt="Screenshot 2024-04-10 at 6 23 33 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/4a95c29a-61ac-495d-9c3b-55ba8a4ae705">


*Working Directory : The Working directory ```/path/to/directory``` as the changed working directory.*

*Output : You can now use ```cd``` with a path as an input to navigate to the designated directory.*

```

cd /nonexistent/directory
```

<img width="466" alt="Screenshot 2024-04-10 at 6 24 46 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/f520bcdb-51ba-4d0e-a848-c3b05a68f6ee">

*Working Directory : The working directory seems to change here to now include ```lecture1/```.*

*Output : This Working directory doesn't exist so this causes an error.*


## ```ls``` Command


```
$ ls
```

<img width="731" alt="Screenshot 2024-04-10 at 7 41 35 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/fafe6496-d5ff-4d68-9553-4bb389dba1ec">

*Working Directory: This command lists the files and directories that are currently in the working directory.*

*Output : The result will display the files and directories in the current directory.*


```
$ ls /path/to/directory
```

<img width="538" alt="Screenshot 2024-04-10 at 6 35 29 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/ec739642-6f70-4512-9c19-347f26a3cfd3">

*Working Directory : The directory does not change after this command at all.*

*Output : This command lists the contents of the specified directory.*


```
$ Is /nonexistent/directory

```

<img width="511" alt="Screenshot 2024-04-10 at 6 28 28 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/7e7044fd-7be5-45a7-b383-4d112f71c1ad">

*Working Directory : Again the Working directory is unchanged.*

*Output Explanation : Due to nonexistence of this directory ```/nonexistent/directory``` it does not exist.*

## ```cat``` Command











