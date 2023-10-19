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
