## Research afternoon - week 6:
# Database setup and maintenance
![img](http://blogs.bmc.com/wp-content/uploads/2016/06/database-blue.png)
### 1. What is a build script and why do you need one?
#### The build script is a tool that optimizes your code for production use on the web.
#### The build script file will loop through each folder and concatenate each file into one single file.
#### Why use it? Faster page load times
#### comes with a versatile and extensible build system that is integrated into the dev server, allowing files to be built as part of a deploy process but also dynamically as needed during development.

### 2. What is database migration?  
![img](http://www.itisl.com/MainGroup/images/graphDBMigr.jpg)  
#### Database migration explained:
#### Database migration — in the context of enterprise applications — means moving your data from one platform to another. There are many reasons you might want to move to a different platform.
#### For example, a company might decide to save money by moving to a cloud-based database. Or, a company might find that some particular database software has features that are critical for their business needs. Or, the legacy systems are simply outdated. The process of database migration can involve multiple phases and iterations — including assessing the current databases and future needs of the company, migrating the schema, and normalizing and moving the data. Plus, testing, testing, and more testing.

#### Benefits of database migration:
* ####  Costs: One of the primary reasons that companies migrate databases is to save money. Often companies will move from an on-premise database to a cloud database. This saves on infrastructure as well as the manpower and expertise needed to support it.

* #### Modernized software: Another common reason for migration is to move from an outdated system or legacy systems to a system that is designed for modern data needs. In the age of big data, new storage techniques are a necessity. For example, a company might choose to move from a legacy SQL database to a data lake or another flexible system.

* #### One source of truth: Another common reason to migrate data is to move all the data into one place that is accessible by all divisions of the company. Sometimes this occurs after an acquisition when systems need to be combined. Or, it can happen when different systems are siloed throughout a company.  

#### Database Migration Service:
#### Database Migration Service is a service that helps you migrate or transfer your database from one source to the other.
#### AWS Database Migration Service is also one such service that allows you to transfer your data from your on premises environment to the AWS Cloud with more effectiveness, security and very low downtime (the time data on your database cannot be availed by the user).  

![img](https://docs.microsoft.com/en-us/azure/sql-database/media/sql-database-cloud-migrate/azure-sql-migration-sql-db.png)  

### 3. Create a build script for a simple database (one or two tables only):
#### Example:
````
BEGIN;

DROP TABLE IF EXISTS Students CASCADE;

CREATE TABLE Students (
id SERIAL PRIMARY KEY,
first_name VARCHAR(100) NOT NULL,
last_name VARCHAR(100) NOT NULL,
location VARCHAR(100)
);

INSERT INTO Students(first_name, last_name, location) VALUES
  ('Sharon', 'Smith', 'Nazareth'),
  ('John', 'White', 'London'),
  ('Paul', 'Hallam-Wistle', 'London')

COMMIT;
````   


![img](http://www.iconarchive.com/download/i93824/iconleak/cerulean/database.ico)
#### Thank you :rose:
