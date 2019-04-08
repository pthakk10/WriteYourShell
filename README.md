# Homework 2 - A Simple Shell Pt. 1
## Due: 17 February 2019 : 11:00PM
### Introduction
In our time here at UIC, we've all been working in the BASH shell for a good portion of our assignments, but have you ever thought about how it works? [BASH](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), has some powerful features! BASH is based on the [Bourne Shell](https://en.wikipedia.org/wiki/Bourne_shell) which might make Stephen Bourne cooler than Jason Bourne in my book.

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
### Turn in
* An autograder will be implemented on gradescope. Part 1 will be due 17-Feb @ 11:00PM.
* Submit all files needed to run your program, and a make file. The make file should build your entire project using ```make hw2```
* Your executable should be called hw2
* _Projects that fail to comply with the above will not be graded._ 

### Input
* Commands will be called using its absolute path. IE ls will be called as /bin/ls
* Command line input will be no longer than 128 characters. 
* You can assume that the command and arguments (tokens) will be separated by spaces. There will be no quotations.
