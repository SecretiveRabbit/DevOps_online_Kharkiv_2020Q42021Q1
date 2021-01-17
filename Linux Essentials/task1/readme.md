Task1.Part1

***

1) Log in to the system as root.  

***

![task 1](screenshots/step1.png)
![task 1](screenshots/step1_1.png)

2) Use the passwd command to change the password. Examine the basic parameters of the command. What system file does it change *?

***

![task 2](screenshots/step2.png)
![task 2](screenshots/step2_1.png)

When I typed "passwd -e vagrant" I logged out and logged in again. After that my shell told me that my password had expired so that I need to change it. 

![task 2](screenshots/step2_2.png)
![task 2](screenshots/step2_3.png)

3) Determine the users registered in the system, as well as what commands they execute. What additional information can be gleaned from the command execution?

![task 2](screenshots/step3.png)
![task 2](screenshots/step3_1.png)

Also I can check all the users existing in my computer with the help of the command "sed 's/:*//' /etc/passwd"

![task 3](screenshots/step3_2.png)

4) Change personal information about yourself.

![task 4](screenshots/step4.png)
![task 4](screenshots/step4_1.png)
![task 4](screenshots/step4_2.png)
![task 4](screenshots/step4_comment.png)

***

5) Become familiar with the Linux help system and the man and info commands. Get help on the previously discussed commands, define and describe any two keys for these commands. Give examples.



![task 5](screenshots/step5_man_info.png)
![task 5](screenshots/step5_man_man.png)
![task 5](screenshots/step5_man_key1.png)
![task 5](screenshots/step5_man_key2.png)

***

6) Explore the more and less commands using the help system. View the contents of files .bash* using commands.



![task 6](screenshots/step6.png)
![task 6](screenshots/step6_1.png)

cd ~ && more -d -c .bashrc:

![task 6](screenshots/step6_2.png)

cd ~ && less -c -N .bashrc

![task 6](screenshots/step6_less.png)

***

7) Describe in plans that you are working on laboratory work 1. Tip: You should read the documentation for the finger command.



![task 7](screenshots/step7.png)
![task 7](screenshots/step71.png)
***

8) List the contents of the home directory using the ls command, define its files and directories. Hint: Use the help system to familiarize yourself with the ls command.



![task 8](screenshots/step81.png)
![task 8](screenshots/step82.png)

***

***

Part2


1) Examine the tree command. Master the technique of applying a template, for example, display all files that contain a character c, or files that contain a specific sequence of characters. List subdirectories of the root directory up to and including the second nesting level. 

tree -L 2 -R | grep c

![part 2 task 1](screenshots/part2step1.png)
![part 2 task 1](screenshots/part2step1_2.png)


***

2 )What command can be used to determine the type of file (for example, text or binary)? Give an example.


Command "file" can be used to determine type of the file:

![part 2 task 2](screenshots/part2step2.png)

***

3) Master the skills of navigating the file system using relative and absolute paths. How can you go back to your home directory from anywhere in the filesystem?

![part 2 task 3](screenshots/part2step3.png)

***

4) Become familiar with the various options for the ls    command. Give examples of listing directories using different keys. Explain the information displayed on the terminal using the -l and -a switches.
option "-a" lets you see even hidden files
option "-l" (long) displays additional information about the files in more readable form
![part 2 task 4](screenshots/step81.png)
![part 2 task 4](screenshots/step82.png)

***

5) Perform the following sequence of operations: 
-  create a subdirectory in the home directory;
-  in this subdirectory create a file containing information about directories located in the root directory (using I/O redirection operations);
-  view the created file;
-  copy the created file to your home directory using relative and absolute addressing.
-  delete the previously created subdirectory with the file requesting removal;
-  delete the file copied to the home directory.

![part 2 task 5](screenshots/part2step5.png)
![part 2 task 5](screenshots/part2step51.png)

***

6) Perform the following sequence of operations:
-  create a subdirectory testin the home directory;
-  copy the .bash_historyfile to this directory while changing its name to labwork2;
-  create a hard and soft link to the labwork2file in the test subdirectory; 
-  how to define soft and hard link, what do theseconcepts;
-  change the data by opening a symbolic link. What changes will happen and why 
-  rename the hard link file to hard_lnk_labwork2;
-  rename the soft link file to symb_lnk_labwork2 file; 
-  then delete the labwork2. What changes have occurred and why?

![part 2 task 6](screenshots/part2step6.png)
![part 2 task 6](screenshots/part2step61.png)
![part 2 task 6](screenshots/part2step62.png)
![part 2 task 6](screenshots/part2step63.png)
![part 2 task 6](screenshots/part2step64.png)

***

7)Using the locate utility, find all files that contain the squid and traceroute sequence.

![part 2 task 7](screenshots/part2step7.png)

***

8)Determine which partitions are mounted in the system, as well as the types of these partitions.

![part 2 task 8](screenshots/part2step8.png)

***

9)Count the number of lines containing a given sequence of characters in a given file.

![part 2 task 9](screenshots/part2step9.png)

***

10)Using the findcommand, find all files in the /etc directory containing the host character sequence.

![part 2 task 10](screenshots/part2step10.png)

***

11)List all objects in /etc that contain the ss character sequence. How can I duplicate a similar command using a bunch of grep? 

![part 2 task 11](screenshots/part2step11.png)

***

12)Organize a screen-by-screen print of the contents of the /etc directory. Hint: You must use stream redirection operations.

![part 2 task 12](screenshots/part2step12.png)

***

13) What are the types of devices and how to determine the type of device? Give examples.

There are exact commands to determine the type of the device. "lshw" is one of them. This command shows all the devices connected to the computer. This command isn't the only one which is enable to check your devices. "lsscsi", "lsspci", "lssusb", "lsscpu" also can do this but they show only partial information about the devices unlikely from "lshw".
For example, let's use "lshw | less":

To list all the types of devices we can use "lshw | grep \*"

![part 2 task 13](screenshots/part2step13.png)

***

14)How to determine the type of file in the system, what types of files are there?

Use command "file" to determine the type of the file. There are such types of files:
regural file
directory
symbolic link
door (dataflow between different processes)
device file
socket (sockets are used to provide a cooperation between two or more separated computers via TCP/IP)

![part 2 task 13](screenshots/part2step14.png)

***

15) List the first 5 directory files that were recently accessed in the /etc directory. 

![part 2 task 13](screenshots/part2step15.png)

***
