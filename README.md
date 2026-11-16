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

51. wget – Download Files

ex: wget https://example.com/file.zip

50. curl – Test HTTP/HTTPS Connectivity -- it is used to show the text directory on the terminal. curl is used to run the script

curl https://google.com
