# Linux Terminal Basics

## What is the Linux Terminal?

The Linux terminal is a way to interact with the Linux operating system by typing commands instead of using a graphical interface.

It is very important in Linux because many things can be done directly from the terminal, and later in cybersecurity we will use the terminal a lot.

## Commands I Have Learned

### pwd

`pwd` stands for **Print Working Directory**.

It is used when we want to know our current working directory. It is useful when we want to know the exact path of the directory we are currently working in.

Example:

```bash
pwd
```

The result will give us something like:

```text
/home/user/Desktop
```

### ls

`ls` is used to **list** the contents of the current directory.

By default, it shows the visible files and directories inside the current directory.

Example:

```bash
ls
```

#### ls -a

`ls -a` shows all files and directories, including hidden files.

It also shows special entries such as `.` and `..`.

- `.` means the current directory.
- `..` means the parent directory.

Example:

```bash
ls -a
```

#### ls -l

`ls -l` shows the contents in a detailed or long format. It gives information such as permissions, ownership, size and timestamp.

#### ls -h

`-h` means **human-readable**. When used with the long format, file sizes are shown in a more readable form such as KB, MB or GB.

Example:

```bash
ls -lh
```

#### ls -la

We can combine options together.

`ls -la` shows hidden files as well as detailed information about them.

```bash
ls -la
```

### cd

`cd` stands for **Change Directory**.

It is used to change our current working directory or move from one directory to another.

There are two common ways to use `cd`:

- **Relative path** — the path is given relative to our current directory.
- **Absolute path** — the complete path from the root directory is given.

### Relative path example

If we are currently in:

```text
/home/user/Desktop
```

and want to access `folder1` inside Desktop, we can simply type:

```bash
cd folder1
```

As we were already in Desktop, we didn't have to go back or use the complete path.

### Absolute path example

If we are currently in Documents and want to access `folder1` inside Desktop, we can directly give the complete path:

```bash
cd /home/user/Desktop/folder1
```

With this we don't have to go back and do the lengthy process of changing directories one by one.

### cd ..

`cd ..` is used to move to the **parent directory** of our current directory.

Example:

If we are currently in:

```text
/home/user/Desktop/folder1
```

and type:

```bash
cd ..
```

we will move back to:

```text
/home/user/Desktop
```

### mkdir

`mkdir` stands for **Make Directory**.

It is used to create a new directory.

Example:

```bash
mkdir folder1
```

This creates a directory called `folder1` in our current working directory.

We can also create multiple directories in one command:

```bash
mkdir folder1 folder2 folder3
```

### touch

`touch` is used to create new empty files. It can also update the timestamp of an existing file.

To create a file, we simply type:

```bash
touch file1
```

This creates a file called `file1`.

We can create multiple files in one command:

```bash
touch file1 file2 file3
```

If `file1` already exists, `touch` will not create another file with the same name. Instead, it updates the timestamp of the existing file.

### cp

`cp` stands for **copy**.

It is used to copy files from one location to another.

Example:

```bash
cp file1 backup
```

This copies `file1` into the `backup` directory.

To copy a directory and its contents, we use `-r` (recursive):

```bash
cp -r Projects backup
```

This copies the `Projects` directory and everything inside it into `backup`.

### mv

`mv` stands for **move**.

It is used to move files or directories from one location to another.

Example:

```bash
mv file1 folder1
```

This moves `file1` into `folder1`.

We can also use `mv` to rename a file or directory.

Example:

```bash
mv oldname.txt newname.txt
```

The same command can therefore be used for both **moving and renaming**.

### rm

`rm` stands for **remove**.

It is used to delete files.

Example:

```bash
rm file1
```

This removes `file1`.

We need to be careful with `rm` because deleted files do not normally go to a recycle bin like they do in a graphical file manager.

### rm -r

`rm -r` means remove **recursively**.

It is used when we want to delete a directory and the files or directories inside it.

Example:

```bash
rm -r Projects
```

This deletes the `Projects` directory and its contents.

Because this can delete many files at once, we should check the path carefully before running it.

### rmdir

`rmdir` stands for **Remove Directory**.

It is used to remove a directory, but normally only when the directory is empty.

Example:

```bash
rmdir folder1
```

If `folder1` contains files or other directories, `rmdir` will not remove it.

In that situation, if we intentionally want to remove the directory and everything inside it, we can use:

```bash
rm -r folder1
```

### whoami

`whoami` is used to find out which user account we are currently logged in as.

Example:

```bash
whoami
```

It can be useful when we need to know which user is currently executing commands.

### hostname

`hostname` shows the name of the computer or system we are currently using.

Example:

```bash
hostname
```

### uname -a

`uname` is used to display information about the system.

The `-a` option means to show all available information provided by `uname`.

Example:

```bash
uname -a
```

This can show information such as the kernel name, hostname, kernel version and system architecture.

## Bash Wildcards

Wildcards are useful when we want to work with multiple files without typing every filename individually.

### `*` — zero or more characters

The `*` wildcard matches **zero or more characters**.

For example:

```bash
ls *.txt
```

This can match all files ending in `.txt`.

We can also use it with commands such as `mv`, `cp` and `rm`.

Example:

```bash
mv file* backup/
```

This can match files whose names start with `file`.

`*` can also match directories, because it is matching names, not specifically files.

### `?` — exactly one character

The `?` wildcard matches **exactly one character**.

For example:

```bash
ls file?.txt
```

This can match names such as:

```text
file1.txt
file2.txt
fileA.txt
```

but not:

```text
file10.txt
```

because `10` contains two characters.

### `[]` — one character from a set or range

`[]` is used to match **one character** from a specified set or range.

For example:

```bash
ls file[123].txt
```

This can match:

```text
file1.txt
file2.txt
file3.txt
```

We can also use ranges:

```bash
ls file[1-9].txt
```

This matches one character from `1` through `9`.

Similarly, we can use letters:

```bash
ls file[a-c].txt
```

This can match `filea.txt`, `fileb.txt` and `filec.txt`.

An important thing I learned is that `[ ]` matches **one character**, unlike `*`, which can match zero or more characters.

## What I Have Learned So Far

The main thing I have learned from these commands is how to navigate the Linux filesystem and perform basic operations from the terminal.

I can now:

- Find my current location using `pwd`.
- List files and directories using `ls`.
- View hidden files and detailed information using `ls -a`, `ls -l` and `ls -la`.
- Move between directories using `cd` and `cd ..`.
- Create directories using `mkdir`.
- Create files using `touch`.
- Copy files and directories using `cp` and `cp -r`.
- Move and rename files and directories using `mv`.
- Delete files using `rm`.
- Delete directories using `rmdir` or `rm -r` when appropriate.
- Check the current user using `whoami`.
- Check the system name using `hostname`.
- Get system information using `uname -a`.
- Use Bash wildcards such as `*`, `?` and `[]` to work with multiple filenames.

These are basic commands, but understanding them properly is important because the Linux terminal will be used much more later when I start learning cybersecurity and ethical hacking.