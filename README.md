# Linux-Tutorial

Linux Basic Commands:
=====================

Linux is case senstive


1. pwd – Print Working Directory 
Meaning: Displays the current directory where you are working

2. ls – List Files and Directories
Meaning: Displays files and directories.

Important options:
================

Command	    Meaning
ls	        List files
ls -l   	Detailed file information
ls -a	    Show hidden files
ls -lh  	Human-readable file sizes
ls -ltr 	Sort by modification time, oldest first
ls -R	    List recursively

Explanation:
- -l = Long listing format.
- -t = Sort by modification time.
- -r = Reverse the orde

3. cd – Change Directory
Meaning: Move from one directory to another.

Command	        Meaning
cd /home	    Go to home directory location
cd ..	        Go one directory backward/up
cd ~	        Go to your home directory
cd /	        Go to root directory
cd -	        Return to previous directory

4. mkdir – Make Directory
Meaning: Create a new directory.

5. touch – Create an Empty File

Meaning: Create a new empty file or update its timestamp.
Create multiple files: ---  touch file1.txt file2.txt file3.txt

6. cat – Display File Content
Meaning: Display the content of a file.

-n = Display line numbers. ---- cat -n test.txt


Multiple files can be displayed together.--cat file1.txt file2.txt 

7. cp – Copy Files and Directories
Meaning: Copy files from one location to another.

ex: cp source.txt destination.txt

8. mv – Move or Rename Files
Meaning: Move files or rename files.

Rename:
mv old.txt new.txt

9. rm – Remove Files and Directories
Meaning: Delete files and directories.

ex: rm test.txt

-r = Remove recursively. ---> ex: rm -r folder

-f = Force deletion without confirmation. ----> ex: rm -f file.txt

-rf = Forcefully remove a directory and its contents ----> ex: rm -rf folder

Important:
===========
 Be very careful with rm -rf, especially when running commands as root. Always verify the path before execution.

10. clear – Clear Terminal Screen
Note : Removes previous terminal output from the visible screen.


 Linux File Permission Commands:
 =================================

Linux permissions are very important in DevOps production environments.

Linux has three permission categories:
Category	Meaning
User (u)	File owner
Group (g)	Group members
Others (o)	All other users

Three basic permissions:
Permission	Meaning	Numeric value
r	Read	4
w	Write	2
x	Execute	1

11. chmod – Change File Permissions

Example:
chmod 755 script.sh


Meaning:
- Owner = 7 (read + write + execute)
- Group = 5 (read + execute)
- Others = 5 (read + execute

Another example:
chmod 644 file.txt


Meaning:
- Owner can read and write.
- Group can only read.
- Others can only read.

12. chown – Change File Ownership
Meaning: Change the owner of a file or directory.
 ex: chown siva file.txt

 13. chgrp – Change Group Ownership
chgrp devops file.txt


Changes the group ownership to devops

Linux File Searching and Text Commands
=========================================

14. find – Find Files and Directories

Find a file:
find / -name "app.log" 2>/dev/null


Find files by extension:
find /var/log -name "*.log"


Find files modified in the last 24 hours:
find /var/log -type f -mtime -1


Find files larger than 100 MB:
find / -type f -size +100M 2>/dev/null


Meaning:
- -name = Search by name.
- -type f = Search files.
- -type d = Search directories.
- -mtime = Modification time.
- -size = File size.




15. grep – Search Text Inside Files
ex: grep "ERROR" app.log

Important options:
=================
grep -i insensitive

Command	Meaning
grep -i	Ignore uppercase/lowercase
grep -n	Display line numbers
grep -r	Search recursively
grep -v	Display non-matching lines
grep -c	Count matching lines

16. head – Display First Lines

ex: head app.log

Display first 20 lines:
ex: head -20 app.log

17. tail – Display Last Lines 

ex: tail app.log

Display last 50 lines:
tail -50 app.log

QUESTION: I want to 10 line tp last 4 line usng commands or how to get lines between the 5-10

cat file name | head -n 10  tail -n 5
cat passwd | head -n 10 | tail -n 4

Follow logs continuously:
ex: tail -f app.log --- how to see running logs

note: Real-time usage: When an application is deployed through Jenkins, use tail -f to monitor application logs and identify errors.


Editor
------

vim --> visually improved

colon mode:

:q --> quit
:wq --> write and quit
:q!  --> dont save the chnages and exit
:set nu  --> display the line numbers
:set nonu --> remove the line of numbers
:/ file name --> searach the file
:? filename  --> search from bottom
:noh --> dont highlight any thing
:%d --> delete everything
:s/which -word/what you want --> replace the word where your cursor is only first occurence
:s/which -word/what you want/g --> all occurence in that line

:3s/which -word/what you want/g --> all occurence in 3rd line
:%s/which -word/what you want/g  --> all occurence in file

:1d --> delete first line
shift + g --> go to end line
gg --> go to top
yy --> copy
p --> paste

18. less – Read Large Files

Meaning: The less command is used to view large files page by page without loading the entire file into the terminal at once.

It is very useful for reading application logs, server logs, Jenkins logs, and troubleshooting production issues.

4. Linux User Management Commands:
===================================

22. whoami – Current User   --> Displays the username currently logged in.
23. who – Logged-in Users --> Displays users currently logged into the server.
24. id – User and Group Information

Example:
uid=1001(siva) gid=1001(siva) groups=1001(siva),1002(devops)


Meaning:
- uid = User ID.
- gid = Primary Group ID.
- groups = Groups the user belongs to.

25. useradd – Create a User
sudo useradd siva


Create a user with a home directory:
sudo useradd -m siva

26. passwd – Set or Change Password  --> Used to set or update the user's password.
sudo passwd siva





51. wget – Download Files

ex: wget https://example.com/file.zip

50. curl – Test HTTP/HTTPS Connectivity -- it is used to show the text directory on the terminal. curl is used to run the script

curl https://google.com


ecz-user@ip-1/2-31-41-210 ~j> echo nttps://raw.githubusercontent.com/daws-ols/notes/main/ session-02.txc | cut -d "/" -f7
session-02.txt
[ec2-user@ip-172-31-41-210 ~]$ echo https://raw.githubusercontent. com/daws-81s/notes/main/session-02. txt | awk -F "/" '{print
$1F3'
ttps:
[ec2-user@ip-172-31-41-210 ~]$ echo https://raw.githubusercontent.com/daws-81s/notes/main/session-02.txt | awk -F "/" "{print
$2F

[ec2-user@ip-172-31-41-210 ~]$ echo https://raw.githubusercontent. com/daws-81s/notes/main/session-02.txt | awk -F "/" '{print $3F}'
aw. githubusercontent.com
[ec2-user@ip-172-31-41-210 ~]$
ec2-user@ip-172-31-41-210 ~]$ echo https://raw.githubusercontent. com/daws-81s/notes/main/session-02.txt | awk -F "/" '{print $NF}'
session-02.txt
