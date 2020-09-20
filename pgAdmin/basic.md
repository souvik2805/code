
##### 1. Data definition Language (DDL)
##### 2. Data Manipulation Language (DML)
##### 3. Data Control Language (DCL)
##### 4. Data Transaction Control Language (TCL)


### 1. Data definition Language (DDL).

 - Consist of the commands that can be used  to define the data base schema
 - (CREATE, DROP, ALTER)
 

### 2. Data Manipulation Language (DML)

 - The SQL commands that deals with the manipulation of data present in database
 - (SELECT, INSERT, UPDATE, DELETE)


### 3. Data Control Language (DCL)

 -Includes commands which maninly deals with the rights, permissions and other controls of the database system.
 - (GRANT, INVOKE)

### 4.  Data Transaction Control Language (TCL)

 - Includes the commands which mainly deal with the transaction of database.
 - (COMMIT, ROLLBACk, SAVEPOINT)
 - 
 ----------------------------------------
```
 >> postgres=# CREATE SCHEMA information;
CREATE SCHEMA

postgres=# SET search_path TO information;
SET

postgres=# CREATE TABLE students (studentid int, studentname varchar(255));
CREATE TABLE

postgres=# TRUNCATE TABLE students;
TRUNCATE TABLE

postgres=# ALTER TABLE students RENAME TO infostudents;
ALTER TABLE


// Create table in schema testdb
CREATE TABLE testdb.COMPANY(
   ID INT PRIMARY KEY     NOT NULL,
   NAME           TEXT    NOT NULL,
   AGE            INT     NOT NULL,
   ADDRESS        CHAR(50),
   SALARY         REAL
);
 
 ```




