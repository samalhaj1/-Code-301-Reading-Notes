# SQL & NoSQL

## Fill in the chart below with five differences between SQL and NoSQL databases:
|num |SQL|NoSQL|
|----|---|-----|
|1.  |  pronounced as “S-Q-L” or as “See-Quel” is primarily called RDBMS or Relational Databases |Non-relational or Distributed Database|
|2.  |databases are table based databases |databases can be document based, key-value pairs, graph databases.|
|3.  | databases are vertically scalable | databases are horizontally scalable. |
|4.  | databases have a predefined schema  | databases use dynamic schema for unstructured data. |
|5.  | requires specialized DB hardware for better performance | uses commodity hardware. |

## 1. What kind of data is a good fit for an SQL database?

SQL databases are better for multi-row transactions, while NoSQL is better for unstructured data like documents or JSON. 

SQL databases are also commonly used for legacy systems that were built around a relational structure.

## 2. Give a real world example.
* Oracle.
* PostgreSQL.
* Microsoft SQL Server.
8 MariaDB.
* IBM Db2.
* Amazon Aurora.
* Google Cloud Spanner.

## 3. What kind of data is a good fit a NoSQL database?
So, if your application requires high availability and scalability, a NoSQL Database built on BASE properties might be suitable. 

Choose NoSQL if you have or need: Semi-structured or Unstructured data / flexible schema. Limited pre-defined access paths and query patterns.
## 4. Give a real world example.
* MongoDB. MongoDB is the most widely used document-based database. ...
* Cassandra. Cassandra is an open-source, distributed database system that was initially built by Facebook (and motivated by Google's Big Table). ...
* ElasticSearch. ...
* Amazon DynamoDB. ...
* HBase.
* 
## 4. Which type of database is best for hierarchical data storage?
the NoSQL database is better suited for hierarchical data storage because it follows the key-value pair method or graph method. 



## 5. Which type of database is best for scalability?
NoSQL database is best for scalability

NoSQL databases are highly preferred for large data sets.


## 6. What does SQL stand for?

SQL (pronounced "ess-que-el") stands for Structured Query Language. SQL is used to communicate with a database. 

According to ANSI (American National Standards Institute), it is the standard language for relational database management systems.
## 7. What is a realational database?

A relational database is a type of database that stores and provides access to data points that are related to one another. 

... The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points.
## 8. What type of structure does a relational database work with?
The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. 

This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure.
## 9. What is a ‘schema’?
A database schema represents the logical configuration of all or part of a relational database. 

It can exist both as a visual representation and as a set of formulas known as integrity constraints that govern a database. 

These formulas are expressed in a data definition language, such as SQL.
## 10. What is a NoSQL database?
NoSQL, also referred to as “not only SQL”, “non-SQL”, is an approach to database design that enables the storage and querying of data outside the traditional structures found in relational databases.
## 11. Howo does it work?
Wide-column stores: Wide-column NoSQL databases store data in tables with rows and columns similar to RDBMS, but names and formats of columns can vary from row to row across the table. ... 

In an RDBMS, the data would be in different rows stored in different places on disk, requiring multiple disk operations for retrieval.

NoSQL databases (aka "not only SQL") are non tabular, and store data differently than relational tables. 

NoSQL databases come in a variety of types based on their data model. ... 

They provide flexible schemas and scale easily with large amounts of data and high user loads.
## 12. What is inside of a Mongo database?
MongoDB makes use of records which are made up of documents that contain a data structure composed of field and value pairs. Documents are the basic unit of data in MongoDB. 

The documents are similar to JavaScript Object Notation, but use a variant called Binary JSON (BSON).

## 13. Which is more flexible - SQL or MongoDB? and why.
While MongoDB is more flexible and ensures high and diverse data availability, a SQL Database operates with the ACID (Atomicity, Consistency, Isolation, and Durability) properties and ensures greater reliability of transactions
## 14. What is the disadvantage of a NoSQL database?
NoSQL databases don't have the reliability functions which Relational Databases have (basically don't support ACID). 

This also means that NoSQL databases offer consistency in performance and scalability.


 	 
 	 
 	 
 	 














