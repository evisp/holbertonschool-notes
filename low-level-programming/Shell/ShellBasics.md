## Shell

### **General**

### What does RTFM mean?
- Internet slang for read the f… manual

### What is a Shebang
- `#!` at the beginning of a script 

### **What is the shell?**

### What is the shell

### What is the difference between a terminal and a shell

### What is the shell prompt

### How to use the history (the basics)

### **Navigation** 
### What do the commands or built-ins `cd,` `pwd,` `ls` do
- `cd` - change working directory; `pwd` - print working directory; `ls` - list files

### How to navigate the filesystem
- Using the above (and other) commands

### What are the `.` and `..` directories
- Current and parent directories

### What is the working directory, how to print it and how to change it
- The directory we are currently working	on; `pwd` 

### What is the root directory
- The directory at the `root/origin directory`

### What is the home directory, and how to go there
- `cd`

### What is the difference between the root directory and the home directory of the user root
- Everything comes under the root directory; home contains user’s data

### What are the characteristics of hidden files and how to list them
Hidden files are denoted by a period `(.)` character. `ls-a` to list them

### **Looking around**
### What do the commands ls, less, file do
- `ls` list files and directories
- `less` view text files
- `file` classify a file’s content 

### How do you use options and arguments with commands
- `command -option arguments` 

### Understand the ls long format and how to display it
- `ls-l`

### **A Guided Tour**
### What does the ln command do
- Create symbolic links

### What do you find in the most common/important directories
- `root` 	is where everything is located
- `/bin`	contains essential user binaries
- `/dev`	device files
- `/etc`	configuration files
- `/home`	contains the home folder for each user

### What is a symbolic link
- A file that contains a reference to another file

### What is a hard link
- A label or a name assigned to a file

### What is the difference between a hard link and a symbolic link
- Hard links are additional pointers to an in-node. They can only exist at the same volume

### **Manipulating files**
### What do the commands `cp,` `mv,` `rm,` `mkdir` do
- `cp`	copy files and directories (cp file1 file2   or    cp file1 dir1)	
- `mv`	move or rename files or directories
- `rm`	remove files and directories
- `mkdir`	create directories

### What are wildcards and how do they work
- Wildcards are special characters that can be used inside commands to perform a series of actions; e.g., rapidly specify a group of files based on patterns 

### How to use wildcards
- `*`			any number of characters
- `?`			any single character
- `[characters]`		matches a predefined set of characters `([:alnum:])`
- `[!characters]`	matches any character that is not part of the set

### **Working with commands**
### What do `type,` `which,` `help,` `man` commands do
- `type`			display information about command type
- `which`			locate a command
- `help`			display reference page for shell builtin
- `man`			display an on-line command reference

### What are the different kinds of commands
- **An executable program** e.g., compiled binaries of programs written in C
- **A command built into the shell itself:** for example **`cd`**
- **A shell function** (miniature shell scripts incorporated in the environment)
- **An alias,** e.g., commands that we define that are built upon other commands

### What is an alias
- A user defined command that is built on top of other commands

### When do you use the command `help` instead of `man`
- **`help`**	is a facility available for shell built-ins. Many executable programs support a help functionality 
- **`man`**	stands for a manual page / documentation. Man pages are often intended as tutorials - they do not contain examples

### **Reading man pages**
### How to read a man page
- Start by reading the name, then the synopsis and move to the general description to understand how the command is executed and the arguments it receives

### What are man page sections
- **`Name`		`Synopsis`	`Description`	`Examples`	`Overview…`**

### What are the section numbers for User commands, System calls and Library functions
- **User commands** 		1
- **System calls**		2
- **Library functions**		3

### **Keyboard shortcuts**
### Common shortcuts for Bash
- **`Ctrl c`**			interrupt (kill) the current foreground process	
- **`Ctrl z`**			suspend the current foreground process	
- **`Ctrl d`**			close the bash shell
- **`Ctrl l`**			clear the screen
- **`Ctrl A`**			beginning of file
- **`Ctrl E`**			end of the file
- **`Ctrl W`**			cut the word before the cursor
- **`Ctrl Y`**			paste/yank the last thing cut

### **`Lts`**
### What does `LTS` mean?
- Long term support
