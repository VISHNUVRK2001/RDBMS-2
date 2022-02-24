# RDBMS-2
TAMIL NADU POLYTECHNIC EXP-2
QUERIES:
1)Creating the Database and change the database:

mysql>create database socialnetwork;
mysql>use socialnetwork;

2) Creating Table users, friends, userprofile Tables:
mysql>create table users(id int NOT NULL AUTO_INCREMENT, name varchar(40),email varchar(50),address varchar(50),dob TIMESTAMP, isactive tinyint(1),regon TIMESTAMP,logon TIMESTAMP,PRIMARY KEY(id));
mysql> create table friends(id int NOT NULL AUTO_INCREMENT,userid int(10) UNSIGNED  NOT NULL,friendname varchar(30),PRIMARY KEY(id));
mysql>create table userprofile(id int(10),userid int(10),location varchar(20));

3)Verifying the table  using DESCRIBE command:
mysql>describe users;
mysql>describe friends;
mysql>describe userprofile;

4)Inserting the values to the tables:
(i) Setting the limit for auto increment field:
mysql> alter table users auto_increment=101;
mysql>alter table friends auto_increment=11;

(ii) Insert values into the table –users:
mysql>insert into users(name,email,address,dob,isactive,regon,logon)values
('ravi','ravi199@gmail.com','15-gandhi nagar cbe','1995-5-10',1,'2015-6-15','2016-5-9');
mysql>insert into users(name,email,address,dob,isactive,regon,logon)values
('ram','ram1503@gmail.com','25-raja street chennai','1994-10-23',1,'2014-5-1','2017-1-12');
mysql>insert into users(name,email,address,dob,isactive,regon,logon)values
('kumar','kumarkumar@yahoo.com','165-nehru nagar madurai’,'1995-11-23',1,'2016-5-1','20
17-1-25);
mysql>insert into users(name,email,address,dob,isactive,regon,logon)values
('sam','sam1234@gmail.com','25 att colony cbe’,'1993-9-23',1,'2016-6-1','2017-2-25);

(iii)Insert the values into friends table:
mysql>insert into friends(userid,friendname)values(101,’sanjay’);
mysql>insert into friends(userid,friendname)values(101,’mathan’);
mysql>insert into friends(userid,friendname)values(101,’sarath’);
mysql>insert into friends(userid,friendname)values(102,’ajay’);
mysql>insert into friends(userid,friendname)values(102,’gowtham’);
mysql>insert into friends(userid,friendname)values(102,’adhav’);
mysql>insert into friends(userid,friendname)values(103,’pranav’);
mysql>insert into friends(userid,friendname)values(104,’jai’);
mysql>insert into friends(userid,friendname)values(104,’kathir’);
mysql>insert into friends(userid,friendname)values(104,’vijay’);

(iv)Insert the values into userprofile table:
mysql>insert into userprofile values(1,101,’cbe’);
mysql>insert into userprofile values(2,102,’chennai’);
mysql>insert into userprofile values(3,103,’madurai’);
mysql>insert into userprofile values(4,104,’cbe’);

(v) Viewing the inserted values using SELECT statement query:
mysql>select *from users:
mysql>select *from friends;
mysql>select *from userprofile;

5)Adding a new field to the table user:
alter table users add gender char(1);

6)Renaming the table name from friends to user_friends
rename table friends to user_friends;

7)Modify the field name:
alter table users change dob dateofbirth TIMESTAMP;

8)Dropping the field isactive:
alter table users drop isactive;

9)Drop the table userprofile:
drop table userprofile;

