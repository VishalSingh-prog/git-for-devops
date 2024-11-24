# Linux Commands Explained

## `clear`
Description: Clears the terminal screen.  
Syntax:  
```bash
clear
```
Example:  
Before:  
```bash
$ ls  
file1.txt  file2.txt  
$ clear
```
After: The terminal screen is cleared.

---

## `whoami`
**Description:** Displays the username of the current user.  
Syntax:  
```bash
whoami
```
**Example Output:**  
```bash
$ whoami
ubuntu
```

---

## `date`
Description: Displays the current date and time.  
Syntax:  
```bash
date
```
Example Output:  
```bash
$ date
Mon Nov 13 10:45:30 UTC 2024
```

---

## `uptime`
Description: Shows system uptime and load average.  
Syntax:  
```bash
uptime
```
Example Output:  
```bash
$ uptime
 10:46:15 up 3 days,  5:22,  2 users,  load average: 0.15, 0.10, 0.08
```

---

## `cd`  
Description: Changes the current directory.  
Syntax:  
```bash
cd [directory]
```
Example:  
```bash
$ cd /home/ubuntu
$ pwd
/home/ubuntu
```

---

## `ls`  
Description: Lists files and directories in the current directory.  
Syntax:  
```bash
ls [options]
```
Example:  
```bash
$ ls
file1.txt  file2.txt
```
With options:  
```bash
$ ls -l
-rw-r--r-- 1 ubuntu ubuntu 1024 Nov 13 10:30 file1.txt
-rw-r--r-- 1 ubuntu ubuntu 2048 Nov 13 10:35 file2.txt
```

---

## `pwd`
Description: Displays the current directory path.  
Syntax:  
```bash
pwd
```
Example Output:  
```bash
$ pwd
/home/ubuntu
```

---

## `mkdir`
Description: Creates a new directory.  
Syntax:  
```bash
mkdir [directory-name]
```
Example:  
```bash
$ mkdir devops
$ ls
devops
```

---

## `man`
Description: Displays the manual for a command.  
Syntax:  
```bash
man [command]
```
Example:  
```bash
$ man ls
```
Output: Displays a detailed manual for the `ls` command.

---

## `sudo`
Description: Executes a command with superuser privileges.  
Syntax:  
```bash
sudo [command]
```
Example:  
```bash
$ sudo apt update
```
Output: Updates the package list as a superuser.

---

## `useradd`
Description: Adds a new user to the system.  
Syntax:  
```bash
sudo useradd -m [username]
```
Example:  
```bash
$ sudo useradd -m kaleen
$ ls /home
kaleen
```

---

## `passwd`
Description: Sets or updates a user's password.  
Syntax:  
```bash
sudo passwd [username]
```
Example:  
```bash
$ sudo passwd kaleen
Enter new UNIX password:
```

---

## `groupadd`
Description: Adds a new group to the system.  
Syntax:  
```bash
sudo groupadd [group-name]
```
Example:  
```bash
$ sudo groupadd devops
$ cat /etc/group | grep devops
devops:x:1001:
```

---

## `gpasswd`
Description: Adds a user to a group.  
Syntax:  
```bash
sudo gpasswd -a [username] [group-name]
```
Example:  
```bash
$ sudo gpasswd -a user-1 devops
```

---

## `chmod`
Description: Changes file permissions.  
Syntax:  
```bash
chmod [permissions] [file]
```
Example:  
```bash
$ chmod 777 hello.sh
```

---

## `cat`
Description: Displays the contents of a file.  
Syntax:  
```bash
cat [file]
```
Example:  
```bash
$ cat hello.sh
echo "Hello, World!"
```

---

## `vim`
Description: Opens a file for editing using the Vim text editor.  
Syntax:  
```bash
vim [file]
```
Example:  
```bash
$ vim hello.sh
```

---

## `rm`
Description: Removes files or directories.  
Syntax:  
```bash
rm [options] [file/directory]
```
Example:  
```bash
$ rm file1.txt
$ rm -r foldername
```

---

## `tree`
Description: Displays the directory structure in a tree format.  
Syntax:  
```bash
tree [directory]
```
Example:  
```bash
$ tree /home/ubuntu
/home/ubuntu
├── devops
├── file1.txt
└── file2.txt
```

---

## `zip`
**Description: Creates a compressed zip archive.  
Syntax:  
```bash
zip -r [zip-file-name] [directory]
```
Example: 
```bash
$ zip -r backup.zip /home/ubuntu/scripts
```

---

## `crontab`
**Description:** Schedules tasks to run at specified intervals.  
**Syntax:**  
```bash
crontab -e
```
Example:  
Opens the crontab editor to add a scheduled task.

---

## `git`
Description: A version control system to manage code.  
Syntax:  
```bash
git [command]
```
Example:  
Initialize a repository:  
```bash
$ git init
```
Check status:  
```bash
$ git status
```

---

## `systemctl`
Description: Controls and checks the status of system services.  
Syntax:  
```bash
systemctl [command] [service-name]
```
Example:  
```bash
$ systemctl status nginx
```

---

# Git Commands
This Gist contains all the useful commands for Git

Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later.

If you are a developer and want to keep every version of your code/project (which you would most certainly want to), a Version Control System (VCS) is a very wise thing to use.

All the commands used for Git
Compatibility with GitHub
✨Magic ✨

# Commands

## Set global username and email for Git (Locally).
git config --global user.name "<your username>"
git config --global user.email "<your email>"

## Initialise an empty Git Repository
git init

## Clone an existing Git Repository
git clone <repository URL>

## Add file/stage to git
git add <filename>

## Add all the files to git
git add .

## Commit all the staged files to git
git commit -m "<your commit message>"

## Restore the file from being modified to Tracked
git restore <filename>
git checkout <filename>

## Show the status of your Git respository
git status

## Show the branches of your git repository
git branch

## Checkout to a new branch
git checkout -b <branch name>

## Checkout to an existing branch
git checkout <branch name>

## Remove a branch from Git
git branch -d <branch name>

## Show remote origin URL
git remote -v

## Add remote origin URL
git remote add origin <your remote git URL>

## Remove remote origin URL
git remote remove origin 

## Fetch all the remote branches
git fetch

## Push your local changes to remote branch
git push origin <branch name>

## Pull your remote changes to local branch
git pull origin <branch name>

## Check your git commits and logs
git log
