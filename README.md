<div align="center">
        
# UNIX commands

</div>
<div align="left">

<br>

## Topics Covered:

- [**Calendar**](https://github.com/shashi-kant10/unix#calendar)
- [**Change Directory**](https://github.com/shashi-kant10/unix#change-directory)
- [**Make Directory**](https://github.com/shashi-kant10/unix#make-directory)
- [**Remove empty directories**](https://github.com/shashi-kant10/unix#remove-empty-directories)
- [**Touch command**](https://github.com/shashi-kant10/unix#touch-command)
- [**Cat command**](https://github.com/shashi-kant10/unix#cat-command)
- [**ls command**](https://github.com/shashi-kant10/unix#ls-command)
- [**Pwd command**](https://github.com/shashi-kant10/unix#pwd-command)
- [**Echo command**](https://github.com/shashi-kant10/unix#echo-command)
- [**Copy command**](https://github.com/shashi-kant10/unix#cp-command)
- [**Move command**](https://github.com/shashi-kant10/unix#mv-command)
- [**chmod command**](https://github.com/shashi-kant10/unix#chmod-command)

<br>
<hr>
<br>

## Calendar

<br>

cal : Shows current month calendar

<br>

```bash

shashi@Mac-Shashi:/unix$ cal

   December 2020
Su Mo Tu We Th Fr Sa
       1  2  3  4  5
 6  7  8  9 10 11 12
13 14 15 16 17 18 19
20 21 22 23 24 25 26
27 28 29 30 31

```

> cal -3 : Shows n months including, the curent, previous and upcoimng months.

```bash

shashi@Mac-Shashi:/unix$ cal -3

   November 2020         December 2020          January 2021
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa
 1  2  3  4  5  6  7         1  2  3  4  5                  1  2
 8  9 10 11 12 13 14   6  7  8  9 10 11 12   3  4  5  6  7  8  9
15 16 17 18 19 20 21  13 14 15 16 17 18 19  10 11 12 13 14 15 16
22 23 24 25 26 27 28  20 21 22 23 24 25 26  17 18 19 20 21 22 23
29 30                 27 28 29 30 31        24 25 26 27 28 29 30
                                            31

```

> cal -m 7 : Show a particular month.

```bash

shashi@Mac-Shashi:/unix$ cal -m 7

     July 2020
Su Mo Tu We Th Fr Sa
          1  2  3  4
 5  6  7  8  9 10 11
12 13 14 15 16 17 18
19 20 21 22 23 24 25
26 27 28 29 30 31

```

> cal -y 2020 : Shows the whole calendar of the year

```bash

shashi@Mac-Shashi:/unix$ cal -y 2020

```

> cal -m 3 2010 : Show a particular month of a particular year

```bash

shashi@Mac-Shashi:/unix$ cal -m 3 2010

     March 2010
Su Mo Tu We Th Fr Sa
    1  2  3  4  5  6
 7  8  9 10 11 12 13
14 15 16 17 18 19 20
21 22 23 24 25 26 27
28 29 30 31

```

> cal -A 1 : Shows the current month and the next n months. (A - After) <br> cal -B 1 : Shows the current month and the previous n months. (B - Before)

```bash

shashi@Mac-Shashi:/unix$ cal -A 1

   December 2020          January 2021
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa
       1  2  3  4  5                  1  2
 6  7  8  9 10 11 12   3  4  5  6  7  8  9
13 14 15 16 17 18 19  10 11 12 13 14 15 16
20 21 22 23 24 25 26  17 18 19 20 21 22 23
27 28 29 30 31        24 25 26 27 28 29 30
                      31

shashi@Mac-Shashi:/unix$ cal -B 1

   November 2020         December 2020
Su Mo Tu We Th Fr Sa  Su Mo Tu We Th Fr Sa
 1  2  3  4  5  6  7         1  2  3  4  5
 8  9 10 11 12 13 14   6  7  8  9 10 11 12
15 16 17 18 19 20 21  13 14 15 16 17 18 19
22 23 24 25 26 27 28  20 21 22 23 24 25 26
29 30                 27 28 29 30 31

```

<br>
<hr>
<br>

## Change Directory

<br>

cd : Used to change current working directory.

<br>

> cd dir_name : Move inside a subdirectory

```bash

shashi@Mac-Shashi:/unix$ cd newfolder

shashi@Mac-Shashi:/unix/newfolder$

```

> cd .. : Move to the parent of current directory

```bash

shashi@Mac-Shashi:/folder/subfolder$ cd ..

shashi@Mac-Shashi:/folder$ 

```

> cd : Change current directory to home directory

```bash

shashi@Mac-Shashi:/folder$ cd ..

shashi@Mac-Shashi:~$

```

<br>
<hr>
<br>

## Make Directory

<br>

mkdir : Used to create directories

<br>

> mkdir dir_name : Create new directory 

```bash

shashi@Mac-Shashi:/unix$ mkdir newfolder

```

> mkdir dir1 dir2 dir3 : create multiple directories

```bash

shashi@Mac-Shashi:/unix$ mkdir folder1 folder2 folder3

```

> mkdir -p parent_dir/child_dir : create multiple directories and subdirectories 

```bash

shashi@Mac-Shashi:/unix$ mkdir -p parentFolder/childFolder

```

> -v : Print a message for each created directory

```bash

shashi@Mac-Shashi:/unix$ mkdir -p -v parentFolder/childFolder
mkdir: created directory 'parentFolder'
mkdir: created directory 'parentFolder/childFolder'

shashi@Mac-Shashi:/unix$ mkdir -p -v test1/subject1 test2/subject1
mkdir: created directory 'test1'
mkdir: created directory 'test1/subject1'
mkdir: created directory 'test2'
mkdir: created directory 'test2/subject1'

```

<br>
<hr>
<br>

##  Remove empty directories

<br>

rmdir - Used to remove empty directories

<br>

> rmdir dir_name : Remove directory 

```bash

shashi@Mac-Shashi:/unix$ rmdir test1

```

> -v : Print a message for each deleted directory

```bash

shashi@Mac-Shashi:/unix$ rmdir -v test1
rmdir: removing directory, 'test1'

```

> rmdir dir1 dir2: Delete multiple directories 

```bash

shashi@Mac-Shashi:/unix$ rmdir -v test1 test2
rmdir: removing directory, 'test1'
rmdir: removing directory, 'test2'

```

> rmdir -p parent_dir/child_dir: Delete parent and child directories and subdirectories at once 

```bash

shashi@Mac-Shashi:/unix$ rmdir -p -v test2/subject1
rmdir: removing directory, 'test2/subject1'
rmdir: removing directory, 'test2'

```

<br>
<hr>
<br>

## Touch command

<br>

touch : Used to change, modify timestamps of a file

<br>

> touch fileName : Create new file 

```bash

shashi@Mac-Shashi:/unix$ touch file1

```

> Create multiple files at once

```bash

shashi@Mac-Shashi:/unix$ touch file1 file2

```

<br>
<hr>
<br>

## Cat command

<br>

cat : Used to read data from the file and gives the content as output

<br>

> cat fileName : Display content of a file <br>
> (Same as: cat < fileName )

```bash

shashi@Mac-Shashi:/unix$ cat file1
Heading1--
This is file 1
End--

```

> cat file1 file2 : Display content of multiple files  

```bash

shashi@Mac-Shashi:/unix$ cat file3.txt file1      
Heading3--
This is file 3
End--
Heading1--
This is file 1
End--

```

> cat > fileName : Create a new file  

```bash

shashi@Mac-Shashi:/unix$ cat > file3.txt
Heading3--
This is file 3
End--

```

> cat >> fileName : Append an existing file  

```bash

shashi@Mac-Shashi:/unix$ cat >> file3.txt
End of FILE3
^Z
[3]+  Stopped                 cat >> file3.txt

shashi@Mac-Shashi:/unix$ cat file3.txt      
Heading3--
This is file 3
End--
End of FILE3

```

> cat file1 > file2 : Copy contents of one file to another file  

```bash

shashi@Mac-Shashi:/unix$ touch file2

shashi@Mac-Shashi:/unix$ cat file1 > file2        

shashi@Mac-Shashi:/unix$ cat file2
Heading1--
This is file 1
End--

```

> cat file1 >> file2 : Append contents of one file to another file  

```bash

shashi@Mac-Shashi:/unix$ cat file1 >> file2

shashi@Mac-Shashi:/unix$ cat file2
Heading--
This is file 1
End
Heading--
This is file 1
End

```

<br>
<hr>
<br>

## ls command

<br>

ls - Used to list directory contents

<br>

> ls : list all files of current directory

```bash

shashi@Mac-Shashi:/unix$ ls 
README.md  file1.txt  file2  scripting  test1  test2

```

> ls -l : display all information about files and subdirectories 

```bash

shashi@Mac-Shashi:/unix$ ls -l
total 8
-rwxrwxrwx 1 shashi shashi 7024 Dec  1 19:12 README.md
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2    

```

> ls -t : Order files based on last modified time

```bash

shashi@Mac-Shashi:/unix$ ls -t -l
total 8
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1    
-rwxrwxrwx 1 shashi shashi 7024 Dec  1 19:12 README.md
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting

```

> -r : Reverse the order of files

```bash

shashi@Mac-Shashi:/unix$ ls -t -r -l
total 8
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting
-rwxrwxrwx 1 shashi shashi 7024 Dec  1 19:12 README.md
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2    
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2    
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt

```

> ls -S : Order files based on size

```bash

shashi@Mac-Shashi:/unix$ ls -S -l
total 12
-rwxrwxrwx 1 shashi shashi 9432 Dec  1 19:53 README.md
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2

```

> -R : Display files recursively

```bash

shashi@Mac-Shashi:/unix$ ls -l -R
.:
total 12
-rwxrwxrwx 1 shashi shashi 8696 Dec  1 19:50 README.md
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1    
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2    

./scripting:
total 0
-rwxrwxrwx 1 shashi shashi 416 Dec  1 12:05 variables.sh

./test1:
total 0
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 subject1

./test1/subject1:
total 0

./test2:
total 0
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 subject1

./test2/subject1:
total 0

```

> ls -a : Display hidden files

```bash

shashi@Mac-Shashi:/unix$ ls -a -l
total 8
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:30 .
drwxrwxrwx 1 shashi shashi 4096 Nov 30 23:23 ..
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:12 .git
-rwxrwxrwx 1 shashi shashi 7024 Dec  1 19:12 README.md
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:30 file1.txt
-rwxrwxrwx 1 shashi shashi    0 Dec  1 19:29 file2
drwxrwxrwx 1 shashi shashi 4096 Dec  1 11:28 scripting
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:28 test1
drwxrwxrwx 1 shashi shashi 4096 Dec  1 19:29 test2

```

<br>
<hr>
<br>

## pwd command

<br>

pwd -  Print working directory

<br>

> pwd : Used to print absolute path of current directory 

```bash

shashi@Mac-Shashi:~$ pwd
/home/shashi

shashi@Mac-Shashi:~$ cd unix

shashi@Mac-Shashi:/unix$ pwd
/unix

```

<br>
<hr>
<br>

## echo command

<br>

echo - Used to display a line of text

<br>

> echo "string" : Display text 

```bash

shashi@Mac-Shashi:/unix$ echo "Hello"
Hello

```

> \n : Create new line <br>
> -e : Enable interpretation of backslash escape <br>
> \t : Tab Space

```bash

shashi@Mac-Shashi:/unix$ echo -e "Hi, I'm Shashi.\nAndroid Developer."
Hi, I'm Shashi.
Android Developer.

```

> \r : carriage return with backspace interpretor

```bash

shashi@Mac-Shashi:/unix$ echo -e "Hi \rI'm Shashi"        
I'm Shashi

```

> echo * : Prints all files/directory (similar to ls command)

```bash

shashi@Mac-Shashi:/unix$ echo *
README.md file1.txt file2 scripting test1 test2

```

<br>
<hr>
<br>

## cp command

<br>

cp : (Copy) Used to copy files

<br>

> Syntax

```bash

cp [OPTION] Source Directory NewName

```

> Copy file: Test1Subject1.txt into Test1/Subject1

```bash

shashi@Mac-Shashi:/unix$ cp test1subject1.txt /unix/test1/subject1/test1subj1.txt

```

> -i (Interactive): -i option asks the user for confirmation before copying a file that would overwrite an existing file [y : Yes , n : No]

```bash

shashi@Mac-Shashi:/unix$ cp -i test1subj1.txt /unix/test1/subject1
cp: overwrite 'unix/test1/subject1/test1subj1.txt'? y

```

> Rename a file (Copy the file with a different name)

```bash

shashi@Mac-Shashi:/unix$ cp test1subject1.txt test1copied.txt

```

<br>
<hr>
<br>

## mv command

<br>

mv : (Move) Used to move files from one place to another

<br>

> Syntax

```bash

mv [Option] source destination

```

> Move file: Test1Subject2.txt into Test1/Subject2

```bash

shashi@Mac-Shashi:/unix$ mv test1subject2.txt /unix/test1/subject2

```

> -i (Interactive): -i option asks the user for confirmation before moving a file that would overwrite an existing file [y : Yes , n : No]

```bash

shashi@Mac-Shashi:/unix$ mv -i test1subj2.txt /unix/test2/subject2
mv: overwrite '/unix/test2/subject2'? y

```

<br>
<hr>
<br>

## chmod command

<br>

chmod : (Change mode) To change access permissions

<br>

> Syntax

```bash

chmod [reference][operator][mode] file_name

```

> Understanding file permissions <br><br>
When we hit the ls -l commands, we see this string of letters, drwxrwxr-x. This represents the permissions that are set for this folder/file. <br><br>
d-rw-r--r-- <br><br>
First character specifies the type, where <br>
'd' : directory <br>
'-' : file <br><br>
Next 3 characters : Owner/User permissions <br>
Next 3 characters : Owner/User's group permissions <br>
Next 3 characters : Other group permissions <br><br>
Reference:<br>
'u' : user<br>
'g' : group<br>
'o' : other group<br>
'a' : all<br><br>
Operator:<br>
'+' : add a permission<br>
'-' : remove a permission<br>
'=' : remove previous permissions and save current permission<br><br>
Mode:<br>
r : read<br>
w : write<br>
x : execute<br>

```bash

[shashi@ubuntu ~]$ls -l
total 4
drwxrwxr-x. 2 shashi shashi 18 Sep  1 05:58 dir1
drwxrwxr-x. 3 shashi shashi 17 Aug 24 17:51 dir2
-rw-rw-r--. 1 shashi shashi  0 Dec  2 07:32 file1
-rw-rw-r--. 1 shashi shashi  0 Dec  2 07:32 file2
-rw-rw-r--. 1 shashi shashi 17 Dec  2 07:31 t2s1.txt
drwxrwxr-x. 3 shashi shashi 21 Dec  2 07:30 test1
drwxrwxr-x. 3 shashi shashi 21 Dec  2 07:30 test2

```

> Add execute permission to File1

```bash

[shashi@ubuntu ~]$chmod u+x file1 

```

> We can see the difference in permission, when we enter ls -l command<br><br>
Before<br>
-rw-rw-r--. 1 shashi shashi  0 Dec  2 07:32 file1<br><br>
After<br>
-rwxrw-r--. 1 shashi shashi  0 Dec  2 07:32 file1

<br>

> Give multiple permissions

> In this example: we will give write and execute permission to other group for File1

```bash

[shashi@ubuntu ~]$chmod o+wx file1             

```

> We can see the difference in permission, when we enter ls -l command<br><br>
Before<br>
-rw-rw-r--. 1 shashi shashi  0 Dec  2 07:32 file1<br><br>
After<br>
-rwxrw-rwx. 1 shashi shashi  0 Dec  2 07:32 file1

<br>

> Remove permission

> Remove read permission of File1 from others

```bash

[shashi@ubuntu ~]$chmod o-r file1                

```

> We can see the difference in permission, when we enter ls -l command<br><br>
Before<br>
-rwxrw-rwx. 1 shashi shashi  0 Dec  2 07:32 file1<br><br>
After<br>
-rwxrw--wx. 1 shashi shashi  0 Dec  2 07:32 file1

</div>