# Shell Navigation

### How to navigate in an Unix system

- `pwd` 			print working directory
- `cd`			change directory 
- `.`(dot)			refers to working directory
- `..`(dot dot)		refers to the parent of the working directory

### How to list files and directories

- `ls`			list files and directories
- `ls -l /etc /bin`	list files in `/etc` and `/bin` in long format
- `ls -la ..`		list all (hidden also) files in long format


### How to display the contents of a file
- `less`			lets us view text files
- page up/down to move
- `G` and `1G` to go to the end/beginning of file
- `/characters` allows to search for		`n` to repeat the search 
- `q` to quit
- `file`			lets us know what type the file is 

### How to create a file or directory

- `mkdir`			creates directories						

### How to remove a file or directory 

- `rm` 			removes/deletes files and directories
- `rm -r dir1 dir2`	deletes `dir1` and `dir2` along with their contents

### How to move or copy a file or directory

- `cp`			copies files and directories
- `cp -i file1 file2`	copies file1 to file2 while asking (i-interactive)
`cp -R dir1 dir2`	copies `dir1` to `dir2`. If `dir2` exists, `dir1` inside it
- `mv`			to more or rename files or directories	 
- `mv -i file1 file2`	If `!file2`, rename `file1` to `file2`. Else, replace content

## Emacs

### **Learning objectives:**

### What is Emacs?
- Extensible, customizable, self-documenting, real-time editor

### Who is Richard Stallman
- `R.S` is a free software movement activists who launched `GNU project`, developed `GNU Emacs` and wrote `GNU General Public License`

### How to open and save files
- **`C-x C-f`**		find file
- **`C-x C-s`**		save file
- **`M-x recover-this-file`**	auto save

### What is a buffer and how to switch from one to the other
- A buffer is an object that a file’s text is held in
- **`C-x C-b`**		lists all buffers
- To switch between buffers **`C-x C-f`** to find the new file
- **`C-x b`**			allows to find a buffer
- **`C-X 2`**			create two windows
- **`C-x o`**			moves from one window to another

### How to use the mark and the point to set the region
- Mark is a previous cursor position
- **`C-SPC`**			Set mark to current location
- **`C-x	C-x`**		Swap point and mark
- **`C-u	C-SPC`**		cycle through 16 mark rings
- Mark and point together delineate a region

### How to cut and paste lines and regions
- **`C-k	M-k`**		kill until the end of line/sentence
- **`C-y`**			yank (paste)
- **`M-y`**			yanks back earlier kills of text
- **`M-d`**			kill next word
- **`M-k`**			kill to end of sentence

### How to search forward and backward
- **`C-s	C-r`**		forward / reverse search
- **`M %`**			query replace
- **`C M s`**			regex search

### How to invoke commands by name
- **`M-x name`**		invokes a command by its name

### How to undo
- **`C-/	C-_	C-x u`**	undo

### How to cancel half-entered commands
- **`C-g`**			stop safely

### How to quit Emacs
- **`C-x C-c`**		exit 
- **`C-z`**			exit Emacs temporarily

### Insert and Delete
- **`C-k	M-k`**		kill until the end of line/sentence
- **`C-y`**			yank (paste)
- **`M-y`**			yanks back earlier kills of text

### Important Move-Around Commands
- **`C-f`**			forward one character
- **`C-b`**			backward one character
- **`M-f`**			forward one word
- **`i`**			insert into file
- **`C-n`**			move next line
- **`C-p`**			move previous line
- **`C-a`**			move beginning of line
- **`C-e`**			move end of line
- **`M-a`**			move beginning of sentence
- **`M-e`**			move end of sentence
- **`C-x 1`**			leave only one window

## Git
### What is source code management
- Source code management allows a developer to organize code iterations chronologically, and version it for an application

### What is Git
- Git is a popular approach of a version control system. It stores information in an organized structure that resembles a tree. Merging algorithm is smart - it figures out most conflicts by itself
- You can make several commits - they are local. 
- When you want the team to know, you push (pull first, conflicts resolved on local computer)

### What is GitHub	
- Github is one of the many services that provide
	- A git repository server to push to
	- A web UI and extra features

### What is the difference between Git and GitHub
- Git is a source management system that comes with a command line. GitHub is a popular approach a version control system

### How to create a repository
- git init allows to initialize a local directory as a git repository

### What is a README
- Source of information to tell collaborators and others what the project is about

### How to write good READMEs
- What the project does; why is the project useful; how can users start with the project; how can they get help

### How to commit
- Commits are small atomit iterations made by developers on a branch
- **`git commit -m “Helpful message”`**

### How to write helpful commit messages
- All commits have a one-line sentence describing the commit. It helps to have the project track changes at a glance

### How to push code
- **`git push origin -u main`**

### How to pull updates
- **`git pull origin my_feature`**

### How to create a branch
- **`git branch my_feature`**

### How to merge branches
- **`git checkout main`**
- **`git merge my_feature`**

### How to work as collaborators on a project
- Settings add collaborators from UI

### Which files should and which files should not appear in your repo
- Configurations, keys, password, environment variables do not
- General assets or binary dependencies do not
[Click Here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)

## Vi

### **Learning objectives:**

### What is vi
- Default editor that comes with UNIX operating system

### Who is Bill Joy
Co-founder of Sun Microsystem

### How to start and exit vi
- Start: `vi;` Exit: `:x  :wq  :q :q!`

### What are the command and insert modes, and how to switch from one to the other
- `Esc` 

### How to edit text
- `* u undo`
- `I` insert

### How to cut and paste lines
- **`yy`** and **`p`** 

### How to search forward and backward

### How to undo

### How to quit vi

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

## Shell, Permissions

### **Permissions**
### What do the commands `chmod,` `sudo,` `su,` `chown,` `chgrp` do
- **`chmod`**	modify file access rights
- **`sudo`**		temporarily become the super user
- **`su`**		temporarily become the super user
- **`chown`**	change file ownership
- **`chgrp`**		change a file’s group ownership

### Linux file permissions
- each file and directory is assigned access rights for the owner of the file, the members of a group of related users, and everybody else
- rights can be assigned to read a file, to write a file, and to execute a file

### How to represent each of the three sets of permissions (owner, group, and other) as a single digit
- Represent permissions as bits (0 or 1). Then represent each group of 3 bits as a number in the decimal system. Then group together

### How to change permissions, owner and group of a file
- We can use the **`chmod`** command and provide numbers as arguments where number denote permissions as described above

### Why can’t a normal user chown a file
- Because it has no access rights

### How to run a command with root privileges
- Run it with sudo

### How to change user ID or become superuser

### **Other Man Pages**
### How to create a user
- **`sudo useradd username`**

### How to create a group
- **`sudo groupadd mygroup`**

### How to print real and effective user and group IDs
- **`id`**

### How to print the groups a user is in
- **`groups`**

### How to print the effective userid
- **`id -u`**

## Shell, I/O Redirections

### **Shell, I/O Redirection**
### What do the commands `head,` `tail,` `find,` `wc,` `sort,` `uniq,` `grep,` `tr` do
- **`head`**		print the first 10 lines of each FILE to standard output.
- **`tail`**		print the last N number of data of the given input.
- **`find`**		is a command line utility for walking a file hierarchy.
- **`wc`**		it is used to find out number of lines, word count, byte and characters count in the files specified in the file arguments.		
- **`sort`**		is used to sort a file, arranging the records in a particular order.
- **`uniq`**		is a command-line utility that reports or filters out the repeated lines in a file.
- **`grep`**		searches through the file, looking for matches to the pattern specified.
- **`tr`**		is a command line utility for translating or deleting characters.

### How to redirect standard output to a file
- We can use the `>` notation to redirect to a file (each time, the file is overwritten) or the `>>` notation to append new output
- Both `<` and `>` can be used at the same time

### How to get standard input from a file instead of the keyboard
- To redirect standard input we use the `<` notation

### How to send the output from one program to the input of another program
- We can use **pipelines,** i.e., the output of a command can serve as the input of another

### How to combine commands and filters with redirections
- Filters take standard input, perform an operation and send the result to standard output
	- E.g. **`sort,` `uniq,` `grep,` `fmt,` `pr,` `head,` `tail,` `tr,` `sed,` `awk`**
- Use pipeline

### **Special Characters**
### What are special characters
- Characters that do not have a literal meaning. They carry special instructions. 

### Understand what do the white spaces, single quotes, double quotes, backslash, comment, pipe, command separator, tilde and how and when to use them
- **`White spaces`**		space, tab, new line, carriage return
- **`Single quotes`**		protect the text to have literal meaning
- **`Double quotes`**		do not allow the text to be split
- **`Backslash`**			prevents the next character from being interpreted as a special character
- **`Comment`**			notes of explanation
- **`Pipe`**				send the output of a command as the input of another command
- **`Command separator`**	used to separate multiple commands that are on the same line
- the home directory

## Shell, Init Files, Variables and Expansions

### **General**
### What happens when you type `$ ls -l *.txt`

### **Shell Initialization Files**
### What are the `/etc/profile` file and the `/etc/profile.d` directory
- Instructions that set shell variables such as `PATH,` `USER,` `MAIL,` `HOSTNAME` and `HISTSIZE`
- `/etc/profile.d` contains files configuring system-wide behavior of specific programs

### What is the `~/.bashrc` file

### **Variables**
### What is the difference between a local and a global variable
- Global variables are available in all shell
- Local variables are available only in the current shell

### What is a reserved variable
- BASH uses certain variables that have a reserved specific meaning

### How to create, update and delete shell variables
- Create: **`VARNAME=“value”`** (do not put spaces)

### What are the roles of the following reserved variables: HOME, PATH, PS1
- **`HOME`**		user’s home directory
- **`PATH`**		A list of directories in which shell looks for commands
- **`PS1`**		The primary prompt string

### What are special parameters
- The shell treats several parameters differently. They can only be referenced, but not modified

### What is the special parameter `$?`?

### **Expansions**
### What is expansion and how to use them
- Expansions are a series of processes that happen when a command unfolds. Some examples of expansions are
	- Pathname expansion: e.g., **`echo *`**
	- Tilde expansion: e.g, **`echo ~foo`**
	- Arithmetic expansion: e.g., **`echo$((2+2))`**
	- Brace expansion: e.g., **`echo Front-{A, B, C}-back; echo number_{1..5}`**
	- Parameter expansion: store small chunks of data and give each of them a name
	- Command substitution allows us to use the output of a command as an expansion. 

### What is the difference between single and double quotes and how to use them properly
- Quoting allows us to selectively suppress unwanted expansions
- Double quotes: all special characters lose their meaning, except: **`$ \``**
	- Word-splitting, pathname expansions, tilde expansion and brace expansions **are suppressed**
	- Parameter / arithmetic / command expansions are carried out
- Single quotes are used when we need to suppress all expansions

### How to do command substitution with **`$()`** and backticks

### **Shell Arithmetic**
### How to perform arithmetic operations with the shell
- Shell arithmetic allows to perform mathematical operations inside the shell

### The alias Command
- How to create an alias
- How to list aliases
- How to temporarily disable an alias

### Other help pages
- How to execute commands from a file in the current shellShell Arithmetic
How to perform arithmetic operations with the shell
Shell arithmetic allows to perform mathematical operations inside the shell
The alias Command
How to create an alias
How to list aliases
How to temporarily disable an alias
Other help pages
How to execute commands from a file in the current shell
