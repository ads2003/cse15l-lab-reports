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

*Output : Due to nonexistence of this directory ```/nonexistent/directory``` it does not exist.*

## ```cat``` Command


```
$ cat
```

<img width="388" alt="Screenshot 2024-04-10 at 6 29 40 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/13fc804b-e04b-48a1-a5c3-8817f5876114">


*Working Directory: This command also does not change the working direcotry at all.*

*Output : When the cat command is used without any parameters, its behavior is determined by the input entered by the user.*


```
$ cat/path/to/dir
```

<img width="504" alt="Screenshot 2024-04-10 at 6 37 10 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/9c951730-760b-4efd-be5b-284f79361e48">

*Working Directory: there is no change in the working directory again.*

*Output : When this command is performed, the contents of the specified file are shown.*


```
$ cat/nonexistent/dir
```

<img width="475" alt="Screenshot 2024-04-10 at 6 31 44 PM" src="https://github.com/ads2003/cse15l-lab-reports/assets/156348741/c8c13c50-3086-4e0c-8f8c-3367e7bc8667">

*Working Directory: The directory remains unchanged again.*

*Output Explanation: Because the  ```/nonexistent/file.txt``` does not exist, this causes an error in the code.*













