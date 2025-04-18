# Shell Scripting Mini-Project Documentation

This document details the process of completing a shell scripting mini-project on an Ubuntu server, as per the lecturer's instructions. The goal is to create a shell script that automates the creation of directories and users. Each step includes commands, outputs, and screenshot placeholders for verification.

---

## Shell Script Code

The script provided by the lecturer:

```bash
#!/bin/bash

# Create directories
mkdir Folder1
mkdir Folder2
mkdir Folder3

# Create users
sudo useradd user1
sudo useradd user2
sudo useradd user3
```

---

## Step 1: Create a Folder on an Ubuntu Server

**Task:** Create a folder named `shell-scripting`.

**Command:**

```bash
mkdir shell-scripting
```

**Output:**

```bash
ls
# Output: shell-scripting
```

**Screenshot:**  
![Screenshot: Terminal showing the mkdir shell-scripting command and ls output](screenshots/step1.png)

---

## Step 2: Create a File Using the Vim Editor

**Task:** Use the Vim editor to create a file called `my_first_shell_script.sh`.

**Command:**

```bash
vim my_first_shell_script.sh
```

**Action:**

- Vim opens in command mode.
- Press `i` to enter insert mode.

**Screenshot:**  
![Screenshot: Terminal showing the vim my_first_shell_script.sh command and Vim editor open](screenshots/step2.png)

---

## Step 3: Add the Shell Script Code

**Task:** Add the shell script code to the new file.

**Code Added in Vim:**

```bash
#!/bin/bash

# Create directories
mkdir Folder1
mkdir Folder2
mkdir Folder3

# Create users
sudo useradd user1
sudo useradd user2
sudo useradd user3
```

**Screenshot:**  
![Screenshot: Vim editor showing the shell script code before saving](screenshots/step3.png)

---

## Step 4: Save the File

**Task:** Save the file in Vim.

**Action:**

- Press `Esc` to exit insert mode.
- Type `:wq` and press `Enter` to save and exit.

**Screenshot:**  
![Screenshot: Vim editor showing the :wq command at the bottom before exiting](screenshots/step4.png)

---

## Step 5: Change into the `shell-scripting` Directory

**Task:** Change into the created directory.

**Command:**

```bash
cd shell-scripting
```

**Output:**

```bash
pwd
# Output: /home/user/shell-scripting
```

**Screenshot:**  
![Screenshot: Terminal showing the cd shell-scripting command and pwd output](screenshots/step5.png)

---

## Step 6: Confirm the File Exists Using `ls -latr`

**Task:** Check for the script file and its permissions.

**Command:**

```bash
ls -latr
```

**Output:**

```bash
total 12
drwxr-xr-x 2 root root 4096 Feb 11 14:36 ..
-rw-r--r-- 1 root root  149 Feb 11 14:35 my_first_shell_script.sh
drwxr-xr-x 2 root root 4096 Feb 11 14:36 .
```

**Observation:**  
Permissions are `rw-r--r--` (no execute permission yet).

**Screenshot:**  
![Screenshot: Terminal showing the ls -latr output with the file and its permissions](screenshots/step6.png)

---

## Step 7: Add Execute Permission for the Owner

**Task:** Make the script executable.

**Command:**

```bash
chmod u+x my_first_shell_script.sh
```

**Verification:**

```bash
ls -l
# Output: -rwxr--r-- 1 root root 149 Feb 11 14:35 my_first_shell_script.sh
```

**Screenshot:**  
![Screenshot: Terminal showing the chmod u+x command and updated ls -l output](screenshots/step7.png)

---

## Step 8: Run the Shell Script

**Task:** Execute the script.

**Command:**

```bash
sudo ./my_first_shell_script.sh
```

**Note:** `sudo` is required for user creation.

**Screenshot:**  
![Screenshot: Terminal showing the sudo ./my_first_shell_script.sh command execution](screenshots/step8.png)

---

## Step 9: Verify Folders Were Created

**Task:** Check for the folders.

**Command:**

```bash
ls
```

**Output:**

```bash
Folder1  Folder2  Folder3  my_first_shell_script.sh
```

**Screenshot:**  
![Screenshot: Terminal showing the ls output with the created folders](screenshots/step9.png)

---

## Step 10: Verify Users Were Created

**Task:** Confirm the users exist.

**Command:**

```bash
cat /etc/passwd | grep user
```

**Output:**

```bash
user1:x:1001:1001::/home/user1:/bin/bash
user2:x:1002:1002::/home/user2:/bin/bash
user3:x:1003:1003::/home/user3:/bin/bash
```

**Screenshot:**  
![Screenshot: Terminal showing the cat /etc/passwd | grep user output with the created users](screenshots/step10.png)

---
