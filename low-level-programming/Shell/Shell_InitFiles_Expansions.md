
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
