# Homework 3 - A Simple Shell Pt. 1
## Due: 17 February 2019 : 11:00PM

### Assignment
For part one of this multi-part assignment we'll be implementing a very simple shell. Your shell should be able to execute commands in the foreground. 

### Requirements
* Prompt the user to enter a command with the prompt ```CS361 >```
* Parse user input into a command and a list of arguments
* Launch a process from the command and pass it the list of arguments
* Wait for command to exit
* Display the pid of the finished process and its exit status

Some commands are built into the shell instead of being forked and executed. You will also implement some of these commands. 
* pwd - display the present working directory to stdout
* cd - Change the current working directory to the one specified by the user
* exit - The shell exits with code zero

The shell must run repeatedly until the user types exit at the command line. 

An example run looks like:
```Bash
CS361 >/bin/ls
File1   File2   File3
pid:22765 status:0
CS361 >
```
```Bash
CS361 >pwd
/path/to/my/directory
CS361 >
```

