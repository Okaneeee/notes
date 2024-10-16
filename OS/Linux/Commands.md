# Commands in Linux

## Directory Navigation

### 1. **`pwd`** - Print Working Directory
This command is used to display the path of the current directory. <br>

Example:
  ```bash
  $ pwd
  /home/user
  ```

### 2. **`ls`** - List
This command is used to list the files and directories in the current directory. <br>
Arguments:
- **`-l`** - List files and directories in long format.
- **`-a`** - List all files and directories including hidden files.
- **`-lh`** - List files and directories in long format with readable file size.

Example:
  ```bash
  $ ls
  file1.txt file2.txt directory1
  $ ls -l
  -rw-r--r-- 1 user user 0 Jan 1 00:00 file1.txt
  -rw-r--r-- 1 user user 0 Jan 1 00:00 file2.txt
  drwxr-xr-x 2 user user 4096 Jan 1 00:00 directory1
  $ ls -a
  . .. file1.txt file2.txt .hiddenfile directory1
  $ ls -lh
  -rw-r--r-- 1 user user 0 Jan 1 00:00 file1.txt
  -rw-r--r-- 1 user user 0 Jan 1 00:00 file2.txt
  drwxr-xr-x 2 user user 4.0K Jan 1 00:00 directory1
  ```

### 3. **`cd`** - Change Directory
This command is used to change the current directory. <br>
Arguments:
- **`~`** - Home directory.
- **`..`** - Parent directory.
- **`.`** - Current directory.

Example:
  ```bash
  $ cd /home/user
  $ cd ..
  $ cd directory1
  $ cd directory/subdirectory
  $ cd .
  ```

## File Operations

### 1. **`touch`** - Create File
This command is used to create an empty file. <br>

Example:
  ```bash
  $ touch file.txt
  ```

### 2. **`mkdir`** - Make Directory
This command is used to create directories. <br>

Example:
  ```bash
  $ mkdir directory1
  ```

### 3. **`cat`** - Concatenate
This command is used to display the contents of a file. <br>

Example:
  ```bash
  $ cat file.txt
  example text
  ```

### 4. **`cp`** - Copy
This command is used to copy files and directories. <br>
Arguments:
- **`-r`** - Copy directories recursively.

Example:
  ```bash
  $ cp file.txt file-copy.txt
  $ cp -r directory1 directory-copy
  ```

### 5. **`mv`** - Move
This command is used to move files and directories. <br>

Example:
  ```bash
  $ mv file.txt directory1
  $ mv directory1 directory2
  ```

### 6. **`rm`** - Remove
This command is used to remove files.<br>
Arguments:
- **`-i`** - Interactive mode for confirmation for each file.
- **`-I`** - Interactive mode for confirmation for more than 3 files (ask only once).
- **`-r`** - Remove directories and their contents recursively.
- **`-f`** - Force remove without confirmation.

Example:
  ```bash
  $ rm file.txt
  ```

### 7. **`rmdir`** - Remove Directory
This command is used to remove directories. <br>
Arguments:
- **`-r`** - Remove directories and their contents recursively.

Example:
  ```bash
  $ rmdir directory1
  ```

## File Permissions

### 1. **`chmod`** - Change Mode
This command is used to change the permissions of files and directories. <br>

#### How to use:
```bash
$ chmod args mode file
```

#### Permissions:
| Permission | Symbolic | Octal |
| --- | --- | --- |
| Read | `r` | 4 |
| Write | `w` | 2 |
| Execute | `x` | 1 |
| No Permission | `-` | 0 |

#### Groups:
| Group | Symbolic | Order in command |
| --- | --- | --- |
| User | `u` | 1 |
| Group | `g` | 2 |
| Others | `o` | 3 |
| All | `a` | all |

<br>

#### Example in symbolic mode:
  ```bash
  $ chmod ugo+rw example.txt
  $ chmod a+rw example.txt
  ```

> This command gives read and write permissions to the user, group, and others.


| Permissions before command | Command | Permissions after command |
| --- | --- | --- |
| `-rw-------` | `a+rw` | `-rw-rw-rw-` |
| user: read, write <br> group: no permissions <br>  other: no permissions| a = all <br> + = add permissions <br> r = read <br> w = write | user: read, write <br> group: read, write <br> other: read write |

#### Example in octal mode:
  ```bash
  $ chmod 640 example.txt
  ```

> With the **value 6 in the first position** of the permission mask, the owner retains maximum access rights: 4 (read) + 2 (write). The **second value** of the permission mask specifies the group's access rights: **4** (read). No rights are provided for other users, who are marked in the **third position**, which is therefore coded with a **0**.

#### Arguments:
- **`-R`** - Change permissions recursively.

#### Example:
  ```bash
  $ chmod -R 744 example-directory
  ```

> The following rule applies to all files and subdirectories in the `example-directory` directory: the owner has **full access permissions (7)**, group members and other users have **read-only access (4)**.

<details>
    <summary>Source</summary>
    <a href="https://www.ionos.fr/digitalguide/serveur/know-how/attribution-de-droits-sur-un-repertoire-avec-chmod/" target="_blank">Ionos</a> <em>(French)</em>
</details>

### 2. **`chown`** - Change Owner
Didn't worked with this command yet.

### 3. **`chgrp`** - Change Group
Didn't worked with this command yet.

## File Searching

### 1. **`find`** - Find
This command is used to search for files and directories. <br>
Arguments:
- **`-name`** - Search by name.
- **`-type`** - Search by type (f = file, d = directory).
- **`-exec`** - Execute command on found files.

Example:
  ```bash
  $ find /home/user -name file.txt
  $ find /home/user -type f
  $ find /home/user -type d
  $ find /home/user -name "*.txt" -exec cp {} /home/user/documents \;
  ```

### 2. **`grep`** - Global Regular Expression Print
This command is used to search for text in files. <br>
Arguments:
- **`-i`** - Case insensitive search.
- **`-r`** - Recursive search.
- **`-n`** - Display line numbers.
- **`-v`** - Display lines that do not match.
- **`-c`** - Display count of matching lines.

Example:
  ```bash
  $ grep "example" file.txt
  $ grep -i "example" file.txt
  $ grep -r "example" directory1
  $ grep -n "example" file.txt
  $ grep -v "example" file.txt
  $ grep -c "example" file.txt
  ```

