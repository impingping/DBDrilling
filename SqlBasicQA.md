Q: Name a few common DB joins, and their differences.
A:  A join is a SQL instruction to combine data from two sets of data.  There are inner join, left join, right join, and full joins. 
Inner join returns records at the intersection of the two tables. 
Left join can be used to append information from one table  to another table. 
Right join is a mirror version of left join. 
Full join is for a list of all records from both tables. 

Q: What is Union in DB?
A: Union is used to combine results. 
Syntax: 

```
SELECT col_1, col_2
UNION [DISTINCT | ALL]
SELECT col_1, col_2
```
Note: 
- The number of columns appears in the corresponding SELECT statements must be equal. 
- The columns appear in the corresponding positions of each SELECT statement must have the same data type or, at least, convertible data type. 
- By default, the `UNION` operator eliminates duplicate rows from the result. 

Q: Explain the basic CRUD operation. 
A: CRUD stands for: create, read, update, and delete. 

Q: What is ACID? Is it related to concurrency issue in DB? 
A: ACID stands for atomicity, consistency, isolation and durability. It is core to concurrency, but more fundamentally, it deals with data consistency and integrity.

Q: What is DB transaction? How is it related to ACID?
A: Transaction is a sequence of operations performed as a single logical unit of work, which must exhibit the ACID properties. Transaction has to either happen in full, or not at all. 

Q: How many connections can we have for a MySQL database?
A: It depends on the context. 
Q: Assumed the login information is stored in the DB, will it be important for the DB to supple lots of connection at the same time?
A: This question should be understood from a different angle.
Q: Does login information go through these processes: front-end application forwards the username/password to backend application through a HTTP request, load balancer will dispatch this request to one of back-end servers.  The selected backend server will communicate with one of the databases.
A: It all depends on how system gets set up. The concurrent access to multiple replicated DBs can be handled by the load balancer. 

Q: What type of engine exist in MySQL? What is the difference?
A: InnoDB, MyISAM, Memory, CSV, etc. 
InnoDB  is the default storage engine in MySQL. 
MyISAM stems from ISAM(Indexed Sequential Access Method) which enables fast access to required data through indexed key-fields. 
Memory engine is used to call heap engine. It stores all data in RAM. 
CSV: its tables are really text files with comma-separated values.

## Mentioned Topics
1. NoSQL DB questions.
2. Hibernate, Spring and DB.

## References
1. [MySQL engines](http://dev.mysql.com/doc/refman/5.7/en/storage-engines.html)
