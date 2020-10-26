# MySqlPractice
Enter password: ************
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 19
Server version: 8.0.22 MySQL Community Server - GPL

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
6 rows in set (0.00 sec)

mysql> create payroll_service;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'payroll_service' at line 1
mysql> create database payroll_service;
Query OK, 1 row affected (1.94 sec)

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| payroll_service    |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
7 rows in set (0.07 sec)

mysql> use database payroll_service
ERROR 1049 (42000): Unknown database 'database'
mysql> use databases payroll_service
ERROR 1049 (42000): Unknown database 'databases'
mysql> use payroll_service
Database changed
mysql> create table employee_payroll
    -> create table employee_payroll{
    -> id   INT unsigned NOT NULL AUTO INCREMENT
    -> name VARCHAR (150) NOT NULL,
    -> salary Doble NOT NULL,
    -> start DATE NOT NULL,
    -> PRIMARY KEY (id)
    -> }
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'create table employee_payroll{
id   INT unsigned NOT NULL AUTO INCREMENT
name VA' at line 2
mysql> id   INT unsigned NOT NULL AUTO INCREMENT,
    -> name VARCHAR (150) NOT NULL,
    -> salary Doble NOT NULL,
    -> start DATE NOT NULL,
    -> PRIMARY KEY (id)
    -> }
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'id   INT unsigned NOT NULL AUTO INCREMENT,
name VARCHAR (150) NOT NULL,
salary D' at line 1
mysql> create table employee_payroll{
    -> create table employee_payroll{
    -> id   INT unsigned NOT NULL AUTO INCREMENT,
    -> name VARCHAR (150) NOT NULL,
    -> salary Double NOT NULL,
    -> start DATE NOT NULL,
    -> PRIMARY KEY (id)
    -> }
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '{
create table employee_payroll{
id   INT unsigned NOT NULL AUTO INCREMENT,
name' at line 1
mysql> name VARCHAR(150) NOT NULL,
    -> ;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'name VARCHAR(150) NOT NULL,' at line 1
mysql>
mysql> create table employee_payroll{
    -> id   INT unsigned NOT NULL AUTO_INCREMENT,
    -> name VARCHAR(150) NOT NULL,
    -> salary Double NOT NULL,
    -> start DATE NOT NULL,
    -> PRIMARY KEY (id)
    -> };
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '{
id   INT unsigned NOT NULL AUTO_INCREMENT,
name VARCHAR(150) NOT NULL,
salary ' at line 1
mysql> drop table employee_payroll
    -> drop table employee_payroll;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'drop table employee_payroll' at line 2
mysql> drop table employee_payroll;
ERROR 1051 (42S02): Unknown table 'payroll_service.employee_payroll'
mysql> create table employee_payroll{
    -> id   INT unsigned NOT NULL AUTO INCREMENT,
    ->
    ->
    ->
    -> vnfvbfdn
    -> hfg;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '{
id   INT unsigned NOT NULL AUTO INCREMENT,



vnfvbfdn
hfg' at line 1
mysql> create table employee_payroll(
    -> id   INT unsigned NOT NULL AUTO_INCREMENT,
    -> name VARCHAR(150) NOT NULL,
    -> salary Double NOT NULL,
    -> start DATE NOT NULL,
    -> PRIMARY KEY (id)
    -> )
    -> ;
Query OK, 0 rows affected (2.53 sec)

mysql> describe employee_payroll
    -> ;
+--------+--------------+------+-----+---------+----------------+
| Field  | Type         | Null | Key | Default | Extra          |
+--------+--------------+------+-----+---------+----------------+
| id     | int unsigned | NO   | PRI | NULL    | auto_increment |
| name   | varchar(150) | NO   |     | NULL    |                |
| salary | double       | NO   |     | NULL    |                |
| start  | date         | NO   |     | NULL    |                |
+--------+--------------+------+-----+---------+----------------+
4 rows in set (0.09 sec)

mysql> insert into employee_service(name,salary,start)
    -> Values('Kirti',10000,'2020-09-16'),
    -> ('Deepak',10001,'2020-09-17'),
    -> ('Honey',100000,'2020-10-12');
ERROR 1146 (42S02): Table 'payroll_service.employee_service' doesn't exist
mysql> show databases
    -> ;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| payroll_service    |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
7 rows in set (0.00 sec)

mysql> insert into employee_payroll(name,salary,start)
    -> Values('Kirti',10000,'2020-09-16'),
    -> ('Deepak',10001,'2020-09-17'),
    -> ('Honey',100000,'2020-10-12');
Query OK, 3 rows affected (0.90 sec)
Records: 3  Duplicates: 0  Warnings: 0

mysql> select *from employee_payroll;
+----+--------+--------+------------+
| id | name   | salary | start      |
+----+--------+--------+------------+
|  1 | Kirti  |  10000 | 2020-09-16 |
|  2 | Deepak |  10001 | 2020-09-17 |
|  3 | Honey  | 100000 | 2020-10-12 |
+----+--------+--------+------------+
3 rows in set (0.02 sec)

mysql> select salary from emplyoee_payroll
    -> ;
ERROR 2006 (HY000): MySQL server has gone away
No connection. Trying to reconnect...
Connection id:    20
Current database: payroll_service

ERROR 1146 (42S02): Table 'payroll_service.emplyoee_payroll' doesn't exist
mysql> select salary from emplyoee_payroll;
ERROR 1146 (42S02): Table 'payroll_service.emplyoee_payroll' doesn't exist
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| payroll_service    |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
7 rows in set (1.66 sec)

mysql> select salary from employee_payroll;
+--------+
| salary |
+--------+
|  10000 |
|  10001 |
| 100000 |
+--------+
3 rows in set (0.15 sec)

mysql> select salary from employee_payroll where name='Honey';
+--------+
| salary |
+--------+
| 100000 |
+--------+
1 row in set (0.02 sec)

mysql> ^C
mysql> ^C
mysql> ^C
mysql> select salary from employee_payroll where start between cast('2020-01-01' as date) and date(now());
+--------+
| salary |
+--------+
|  10000 |
|  10001 |
| 100000 |
+--------+
3 rows in set (0.13 sec)

mysql> select salary from employee_payroll where start between cast('2020-09-17' as date) and date(now());
+--------+
| salary |
+--------+
|  10001 |
| 100000 |
+--------+
2 rows in set (0.00 sec)

mysql> select * from employee_payroll where start between cast('2020-09-17' as date) and date(now());
+----+--------+--------+------------+
| id | name   | salary | start      |
+----+--------+--------+------------+
|  2 | Deepak |  10001 | 2020-09-17 |
|  3 | Honey  | 100000 | 2020-10-12 |
+----+--------+--------+------------+
2 rows in set (0.02 sec)

mysql> alter table emplyoee_payroll ADD gender char(1) after name;
ERROR 1146 (42S02): Table 'payroll_service.emplyoee_payroll' doesn't exist
mysql> alter table employee_payroll ADD gender char(1) after name;
Query OK, 0 rows affected (5.39 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql>
mysql> select * from employee_payroll;
+----+--------+--------+--------+------------+
| id | name   | gender | salary | start      |
+----+--------+--------+--------+------------+
|  1 | Kirti  | NULL   |  10000 | 2020-09-16 |
|  2 | Deepak | NULL   |  10001 | 2020-09-17 |
|  3 | Honey  | NULL   | 100000 | 2020-10-12 |
+----+--------+--------+--------+------------+
3 rows in set (0.02 sec)

mysql> update employee_payroll set gender ='M' where name<>'Honey';
Query OK, 2 rows affected (0.26 sec)
Rows matched: 2  Changed: 2  Warnings: 0

mysql> select * from employee_payroll;
+----+--------+--------+--------+------------+
| id | name   | gender | salary | start      |
+----+--------+--------+--------+------------+
|  1 | Kirti  | M      |  10000 | 2020-09-16 |
|  2 | Deepak | M      |  10001 | 2020-09-17 |
|  3 | Honey  | NULL   | 100000 | 2020-10-12 |
+----+--------+--------+--------+------------+
3 rows in set (0.10 sec)

mysql> update employee_payroll set gender ='F' where name='Honey';
Query OK, 1 row affected (0.09 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from employee_payroll;
+----+--------+--------+--------+------------+
| id | name   | gender | salary | start      |
+----+--------+--------+--------+------------+
|  1 | Kirti  | M      |  10000 | 2020-09-16 |
|  2 | Deepak | M      |  10001 | 2020-09-17 |
|  3 | Honey  | F      | 100000 | 2020-10-12 |
+----+--------+--------+--------+------------+
3 rows in set (0.00 sec)

mysql> update employee_payroll set salary=300000.0 where name='Honey';
Query OK, 1 row affected (0.10 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from employee_payroll;
+----+--------+--------+--------+------------+
| id | name   | gender | salary | start      |
+----+--------+--------+--------+------------+
|  1 | Kirti  | M      |  10000 | 2020-09-16 |
|  2 | Deepak | M      |  10001 | 2020-09-17 |
|  3 | Honey  | F      | 300000 | 2020-10-12 |
+----+--------+--------+--------+------------+
3 rows in set (0.08 sec)

mysql> select avg(salary) from employee_payroll;
+-------------+
| avg(salary) |
+-------------+
|      106667 |
+-------------+
1 row in set (0.04 sec)

mysql> select avg(salary) from employee_payroll where gender='M';
+-------------+
| avg(salary) |
+-------------+
|     10000.5 |
+-------------+
1 row in set (0.00 sec)

mysql> select avg(salary) from employee_payroll;
+-------------+
| avg(salary) |
+-------------+
|      106667 |
+-------------+
1 row in set (0.10 sec)

mysql> select avg(salary) from employee_payroll group by gender;
+-------------+
| avg(salary) |
+-------------+
|     10000.5 |
|      300000 |
+-------------+
2 rows in set (0.04 sec)

mysql> select avg(salary) from employee_payroll where gender='M'group by gender;
+-------------+
| avg(salary) |
+-------------+
|     10000.5 |
+-------------+
1 row in set (0.00 sec)

mysql> select gender avg(salary) from employee_payroll group by gender;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(salary) from employee_payroll group by gender' at line 1
mysql> select gender,avg(salary) from employee_payroll group by gender;
+--------+-------------+
| gender | avg(salary) |
+--------+-------------+
| M      |     10000.5 |
| F      |      300000 |
+--------+-------------+
2 rows in set (0.00 sec)

mysql> select gender,count(name) from employee_payroll group by gender;
+--------+-------------+
| gender | count(name) |
+--------+-------------+
| M      |           2 |
| F      |           1 |
+--------+-------------+
2 rows in set (0.02 sec)

mysql> select gender,sum(name) from employee_payroll group by gender;
+--------+-----------+
| gender | sum(name) |
+--------+-----------+
| M      |         0 |
| F      |         0 |
+--------+-----------+
2 rows in set, 3 warnings (0.04 sec)

mysql> select gender,sum(salary) from employee_payroll group by gender;
+--------+-------------+
| gender | sum(salary) |
+--------+-------------+
| M      |       20001 |
| F      |      300000 |
+--------+-------------+
2 rows in set (0.00 sec)

mysql>  select salary from employee_payroll where start between cast('2020-01-01' as date) and cast('2020-09-15' as date);
Empty set (0.00 sec)

mysql> alter table employee_payroll add phone_Number Varchar(120) after name;
Query OK, 0 rows affected (3.08 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add address  Varchar(250) after phone_Number,department varchar(250) not null after address;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'department varchar(250) not null after address' at line 1
mysql> alter table employee_payroll add address  Varchar(250) after phone_Number;
Query OK, 0 rows affected (2.32 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add department varchar(250) not null after address;;
Query OK, 0 rows affected (3.16 sec)
Records: 0  Duplicates: 0  Warnings: 0

ERROR:
No query specified

mysql> alter table employee_payroll alter address default'TBD';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'default'TBD'' at line 1
mysql> alter table employee_payroll alter address default 'TBD';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'default 'TBD'' at line 1
mysql> select *from employee_payroll;
+----+--------+--------------+---------+------------+--------+--------+------------+
| id | name   | phone_Number | address | department | gender | salary | start      |
+----+--------+--------------+---------+------------+--------+--------+------------+
|  1 | Kirti  | NULL         | NULL    |            | M      |  10000 | 2020-09-16 |
|  2 | Deepak | NULL         | NULL    |            | M      |  10001 | 2020-09-17 |
|  3 | Honey  | NULL         | NULL    |            | F      | 300000 | 2020-10-12 |
+----+--------+--------------+---------+------------+--------+--------+------------+
3 rows in set (0.00 sec)

mysql> alter table employee_payroll set address default 'TBD';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'set address default 'TBD'' at line 1
mysql> alter table employee_payroll set address default='TBD';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'set address default='TBD'' at line 1
mysql> alter table employee_payroll set address='TBD' default;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'set address='TBD' default' at line 1
mysql> alter table employee_payroll rename column salary to basic_pay;
Query OK, 0 rows affected (0.54 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add deductions Double Not null after basic_pay;
Query OK, 0 rows affected (3.07 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add taxable_pay Double Not null after deductions;
Query OK, 0 rows affected (2.54 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add tax Double Not null after taxable_pay;
Query OK, 0 rows affected (2.13 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table employee_payroll add net_pay Double Not null after tax;
Query OK, 0 rows affected (1.84 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> select *from employee_payroll;
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------------+
| id | name   | phone_Number | address | department | gender | basic_pay | deductions | taxable_pay | tax | net_pay | start      |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------------+
|  1 | Kirti  | NULL         | NULL    |            | M      |     10000 |          0 |           0 |   0 |       0 | 2020-09-16 |
|  2 | Deepak | NULL         | NULL    |            | M      |     10001 |          0 |           0 |   0 |       0 | 2020-09-17 |
|  3 | Honey  | NULL         | NULL    |            | F      |    300000 |          0 |           0 |   0 |       0 | 2020-10-12 |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------------+
3 rows in set (0.03 sec)

mysql> alter table employee_payroll add demo Double after net_pay;
Query OK, 0 rows affected (3.23 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> select *from employee_payroll;
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
| id | name   | phone_Number | address | department | gender | basic_pay | deductions | taxable_pay | tax | net_pay | demo | start      |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
|  1 | Kirti  | NULL         | NULL    |            | M      |     10000 |          0 |           0 |   0 |       0 | NULL | 2020-09-16 |
|  2 | Deepak | NULL         | NULL    |            | M      |     10001 |          0 |           0 |   0 |       0 | NULL | 2020-09-17 |
|  3 | Honey  | NULL         | NULL    |            | F      |    300000 |          0 |           0 |   0 |       0 | NULL | 2020-10-12 |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
3 rows in set (0.00 sec)

mysql> alter table employee_payroll modify coloumn demo NOT NULL;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'demo NOT NULL' at line 1
mysql> alter table employee_payroll modify coloumn demo NOT NULL;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'demo NOT NULL' at line 1
mysql> alter table employee_payroll modify  demo NOT NULL;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'NOT NULL' at line 1
mysql> alter table employee_payroll modify demo NOT NULL;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'NOT NULL' at line 1
mysql> alter table employee_payroll modify demo Double NOT NULL;
ERROR 1138 (22004): Invalid use of NULL value
mysql> alter table employee_payroll change demo demo varchar(255) Not Null;
ERROR 1265 (01000): Data truncated for column 'demo' at row 1
mysql> select*from employee_payroll;
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
| id | name   | phone_Number | address | department | gender | basic_pay | deductions | taxable_pay | tax | net_pay | demo | start      |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
|  1 | Kirti  | NULL         | NULL    |            | M      |     10000 |          0 |           0 |   0 |       0 | NULL | 2020-09-16 |
|  2 | Deepak | NULL         | NULL    |            | M      |     10001 |          0 |           0 |   0 |       0 | NULL | 2020-09-17 |
|  3 | Honey  | NULL         | NULL    |            | F      |    300000 |          0 |           0 |   0 |       0 | NULL | 2020-10-12 |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
3 rows in set (0.00 sec)

mysql> Alter table employee_payroll modify column demo not null;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'not null' at line 1
mysql> update employee_payroll set department =' ' where department = null;
Query OK, 0 rows affected (0.00 sec)
Rows matched: 0  Changed: 0  Warnings: 0

mysql> Alter table employee_payroll modify column demo not null;
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'not null' at line 1
mysql> update employee_payroll set demo =' ' where demo = null;
Query OK, 0 rows affected (0.33 sec)
Rows matched: 0  Changed: 0  Warnings: 0

mysql> select*from employee_payroll;
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
| id | name   | phone_Number | address | department | gender | basic_pay | deductions | taxable_pay | tax | net_pay | demo | start      |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
|  1 | Kirti  | NULL         | NULL    |            | M      |     10000 |          0 |           0 |   0 |       0 | NULL | 2020-09-16 |
|  2 | Deepak | NULL         | NULL    |            | M      |     10001 |          0 |           0 |   0 |       0 | NULL | 2020-09-17 |
|  3 | Honey  | NULL         | NULL    |            | F      |    300000 |          0 |           0 |   0 |       0 | NULL | 2020-10-12 |
+----+--------+--------------+---------+------------+--------+-----------+------------+-------------+-----+---------+------+------------+
3 rows in set (0.00 sec)

mysql> show tables;
ERROR 2006 (HY000): MySQL server has gone away
No connection. Trying to reconnect...
Connection id:    21
Current database: payroll_service

+---------------------------+
| Tables_in_payroll_service |
+---------------------------+
| employee_payroll          |
+---------------------------+
1 row in set (3.21 sec)

mysql> describe employee_payroll;
+--------------+--------------+------+-----+---------+----------------+
| Field        | Type         | Null | Key | Default | Extra          |
+--------------+--------------+------+-----+---------+----------------+
| id           | int unsigned | NO   | PRI | NULL    | auto_increment |
| name         | varchar(150) | NO   |     | NULL    |                |
| phone_Number | varchar(120) | YES  |     | NULL    |                |
| address      | varchar(250) | YES  |     | NULL    |                |
| department   | varchar(250) | NO   |     | NULL    |                |
| gender       | char(1)      | YES  |     | NULL    |                |
| basic_pay    | double       | NO   |     | NULL    |                |
| deductions   | double       | NO   |     | NULL    |                |
| taxable_pay  | double       | NO   |     | NULL    |                |
| tax          | double       | NO   |     | NULL    |                |
| net_pay      | double       | NO   |     | NULL    |                |
| demo         | double       | YES  |     | NULL    |                |
| start        | date         | NO   |     | NULL    |                |
+--------------+--------------+------+-----+---------+----------------+
13 rows in set (0.68 sec)

mysql>
