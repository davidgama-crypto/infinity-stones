CONTENT
---------
*Introduction
*Requirements
*Installation

INTRODUCTION
-------------
The package contains the files necessary to to run the "SOC Publication
Retrieval Service" - Assignment 1.

REQUIREMENTS
---------------
*JDK 1.8+
*MySql Server 1.8+

INSTALLATION
------------
1.-In MySql server create the next database:
  *Database name: dblp


2.-In MySql, create the next user, with the next command:

  *user: dbo_dblp
  *password: dblp_password
  *command: create user 'dbo_dblp' identified by 'dblp_password'


3.- In MySql, Give permission to the new user in the database "dblp"
with the next command:

  *GRANT ALL PRIVILEGES ON dblp.* TO 'dbo_dblp';


4.- After creating the database, run the file "dblp_db.sql" to create the
tables  and insert the information to the database,the command is (the
password of the "root" user is required)

    * mysql -u root -p dblp < dblp_db.sql


5.- In Mysql, we can test the querys of the file "query.sql"


THE JAVA Project
-----------------

The java project has two principal packages "db" and "models",

* "db"      --> classes to connect to the database an persist the information.
* "models"  --> models of the entities Publication, Author and Electronic
                Edition.


The project has two main classes (located on the root path):
1.-DOMParser.java
2.-XQuery.java


DOMParser.java
---------------
Java class in charge to parse the xml file "dblp-soc-papers-V2.xml", and store
the data into de "dblp" database.


XQuery.java
---------------
Java class used to test the different querys in XQUERY required on the
assignment.

The root path contains 4 files with the different queries(each file corresponds
to one query of the assignment):
* 2.1 --> XQyery_2_1.xqy
* 2.2 --> XQyery_2_2.xqy
* 2.3 --> XQyery_2_3.xqy
* 2.4 --> XQyery_2_4.xqy

To test the queries, only is necessary to change the name of the "xqy" file in
the "XQuery.java",  line "23" and run the code, the console will show the
result of the query.
