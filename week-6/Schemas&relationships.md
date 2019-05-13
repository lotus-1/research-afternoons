# Schemas and relationships

## **1.What is a schema and why/when would you need one?**

#### A database schema represents the logical configuration of all or part of a relational database. As part of a data dictionary, a database schema indicates how the entities that make up the database relate to one another, including tables, views, stored procedures, and more.
#### A database designer creates a database schema to help programmers whose software will interact with the database. The process of creating a database schema is called data modeling. When following the three-schema approach to database design, this step would follow the creation of a conceptual schema.

![](https://database.guide/wp-content/uploads/2016/06/MySQL_Schema_Music_Example.png)


## **2.What are primary keys and why do we need them?**

#### The PRIMARY KEY constraint uniquely identifies each record in a table. Primary keys must contain UNIQUE values, and cannot contain NULL values. A table can have only ONE primary key; and in the table, this primary key can consist of single or multiple columns.When multiple fields are used as a primary key, they are called a composite key. The primary key uniquely identifies a row.
#### Why do we need them? A primary key is used to ensure data in the specific column is unique. You can only set constraints with primary keys, by setting a foreign key to another column which creates a relationship with the column that has the primary key set. A prime use of a primary key is in the case of a users table.

![](https://i.stack.imgur.com/av4vO.png)

## **3.Create a visual representation of a mock schema for a database about Founders & Coders, using as many different kinds of relationship as you can. Explain the logic behind it.**

![picture](/home/sahar/Lotus/week-6/research-afternoons/week-6/assets/schema.jpeg)
