# Linux Terminal Basics

## What is the Linux Terminal?

## Commands I Have Learned

### pwd

`pwd` stands for **Print Working Directory**.

It is used when we want to know our current working directory. It is useful when we want to know the exact path of the directory we are currently working on. 
Example:

pwd

the result will give us something like this:- /home/user/Desktop/

### ls

'ls' stands for **lists**

It is used to list the content of current directory. By default, it shows the visible files and directories inside the current directory.

So when type the command **ls** we get to see all the visible files and directory. But if you want to see all the files including the hidden once then we can use command **ls -a** which shows us all the files, directories and hidden files such as **.** and **..**.

But if you want to see all the information of files and directory such as - **Permissions, timestamp, ownership and size** 

If you want to use both the command at the same time you can do so by simply typing **ls -la** this command will show us all the hidden files and details of those files and folders. 

### cd

`cd` stands for **Change Directory**.

It is used to change our current working directory or move from one directory to another.

There are two common ways to use `cd`:

- **Relative path** — the path is given relative to our current directory.
- **Absolute path** — the complete path from the root directory is given.

### Relative path example

If we are currently in: Desktop 
and want to access folder1 in Desktop

You can simply type - cd folder1
As we were already in Desktop we didn't had to go back or any other process.

### Absolute path example

If we are currently in: Documents
and we want to access folder1 in Desktop 

We will have to write - **cd /home/user/Desktop/folder1/
With this we don't have to go back and do the lengthy process 

### mkdir

### touch

### cp

### mv

### rm

### rmdir
