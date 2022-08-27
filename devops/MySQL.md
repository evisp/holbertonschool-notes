# Database Administration and MySQL

## What is a database

- A database is information that is set up for easy access, management and updating
- Databases are used for storing, maintaining and accessing any sort of data

### Types of Databases

- **Relational**:
  - Relational databases are comprised of tables.
  - Data is placed into predefined categories in those tables.
  - Each table has columns with at least one data category, and rows that have a certain data instance for the categories which are defined in the columns.
  - Relational databases use SQL

- **Distributed**
  - This database stores records or files in several physical locations.
  - Data processing is also spread out and replicated across different parts of the network.

- **Cloud**
  - These databases are built in a public, private or hybrid cloud for a virtualized environment
  - These databases can work with applications deployed as software as a service

- **NoSQL**
  - NoSQL databases are good when dealing with large collections of distributed data.
  - They can address big data performance issues better than relational databases.
  - They also do well analyzing large unstructured data sets

- **Object-Oriented**
  - These databases hold data created using object-oriented programming languages.
  - They focus on organizing objects rather than actions and data rather than logic.

## SQL Replication

If your important data is stored in an SQL database, you can take advantage of some built-in replication features.

### Master-Slave Replication

- You have a main database server, which is referred to as the “master” server.
- This server is responsible for performing all writes and updates.
- The data from this server is copied continuously to a “slave” server.
- This server can be be read from, but not written to.

### Master-Master Replication

- This configuration allows both servers to have “master” abilities.
- This means that each server can accept writes and updates and will transfer the changes to the opposite server.
- This configuration inherits the advantages of the master-slave setup, but also benefits from increased write performance if the writes are properly distributed by a load balancing mechanism.

### Distribution as a Redundancy Alternative

- Distributed systems offer many of the advantages of traditional redundant setups.
- RAID 5 distributes data across a number of drives and also writes the parity of the data across each drive. This means that any kind of transaction can be “rebuilt” from combining the parity information on the other drives if a single drive dies

## How To Install MySQL 5.7 on Ubuntu 20.04

Follow the tutorials provides [here](https://computingforgeeks.com/how-to-install-mysql-on-ubuntu-focal/)
or [here](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)

## How To Set Up Replication in MySQL

Follow the tutorial provided [here](https://www.digitalocean.com/community/tutorials/how-to-set-up-replication-in-mysql)
