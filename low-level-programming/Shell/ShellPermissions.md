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
