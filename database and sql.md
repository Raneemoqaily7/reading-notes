## *Relational Database 
Its a type of Database that store data in tables(schema) two dimintional Rows contain the records
 and Colums contain the name of proporties ,these tables related to each other since you might have 
 information or data in a table that related to another data on another table .
 The most common relationship betwwen these tables is the (ID).

 ## *SQL 
 SQL might seem intimidating but it’s really fairly easy to understand. SQL stands for
Structured Query Language and simply put,it is a standard lannguage for dealing with Relational database ,
 used to insert , update ,rename ,remove , add or delete database records .

 

 #### How to use SQL
 - some SQL keyword:
 - SELECT 
 The first command we're going to learn is SELECT as. There are other starting commands like INSERT and CREATE, 
 but most interactions with databasesare SELECTing data. The SQL Box is therefor you to try running your queries 
 in any language you want.
 
 Used to elect data from database , the data that returned called result-set.
 if you want to select all the data SELECT * FROM my_table
 ![SELECT EXERCISE](./sql_excercise1.png)

 - WHERE
 Limiting queries is one way to filter down result sets, but we can get a lot more specific with the WHERE clause. The WHERE command is followed by the conditions you’d like to
filter by.
Conditions are simply statements that are either true or false. The database takes these
statements and evaluates them across all the rows as it scans through your tables and only
returns the results that are true.
![WHERE](./sql exercise2.png)


- Queries with constraints
SQL supports a number of useful operators to do things like case-insensitive string comparison and wildcard pattern matching

| Operator | Condition|
|----------|:-------------:|
| =	  |Case sensitive exact string comparison|
|!= or <> |Case sensitive exact string inequality comparison|
| LIKE |Case insensitive exact string comparison|
|% |	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)|
|IN (…)	|String exists in a list|
|NOT IN (…)	|String does not exist in a list|
---
![LIKE](./sql exercise 3.png)

- Filtering and sorting Query results
By default results are returned in the order that they’re stored in the database. But
sometimes you’ll want to sort them differently. You can do that with the “ORDER BY”

![ODRDER_BY](./sql exercise 4.png)

When an ORDER BY clause is specified, each row is sorted alpha-numerically based on the specified column's value. In some databases, you can also specify a collation to better sort data containing international text.

- Simple SELECT Queries
![example](./Sql Review .png)

- Multi-table queries with JOINs
Entity data in the real world is often broken down into pieces and stored across multiple orthogonal tables using a process known as normalization.
Database normalization is a database schema design technique, by which an existing schema is modified to minimize redundancy and dependency of data. Normalization split a large table into smaller tables and define relationships between them to increases the clarity in organizing data.
![normalization](./Sql exercise 6.png)

- inserting rows
When inserting data into a database, we need to use an INSERT statement, which declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert. In general, each row of data you insert should contain values for every corresponding column in the table. You can insert multiple rows at a time by just listing them sequentially.

![ex13](./SQL exercise 13.png)

- Updating rows
In addition to adding new data, a common task is to update existing data, which can be done using an UPDATE statement. Similar to the INSERT statement, you have to specify exactly which table, columns, and rows to update. In addition, the data you are updating has to match the data type of the columns in the table schema.
Most people working with SQL will make mistakes updating data at one point or another. Whether it's updating the wrong set of rows in a production database, or accidentally leaving out the WHERE clause (which causes the update to apply to all rows), you need to be extra careful when constructing UPDATE statements.

One helpful tip is to always write the constraint first and test it in a SELECT query to make sure you are updating the right rows, and only then writing the column/value pairs to update.
![ex14](./sql exercise14.png)

- Deleting rows
When you need to delete data from a table in the database, you can use a DELETE statement, which describes the table to act on, and the rows of the table to delete through the WHERE clause.
Like the UPDATE statement from last lesson, it's recommended that you run the constraint in a SELECT query first to ensure that you are removing the right rows. Without a proper backup or test database, it is downright easy to irrevocably remove data, so always read your DELETE statements twice and execute once.
![ex15](./sql exercise 15.png)

- Creating tables
When you have new entities and relationships to store in your database, you can create a new database table using the CREATE TABLE statement.
The structure of the new table is defined by its table schema, which defines a series of columns. Each column has a name, the type of data allowed in that column, an optional table constraint on values being inserted, and an optional default value.

If there already exists a table with the same name, the SQL implementation will usually throw an error, so to suppress the error and skip creating a table if one exists, you can use the IF NOT EXISTS clause.

![ex16](./Sql exercise16.png)

-  Altering tables
As your data changes over time, SQL provides a way for you to update your corresponding tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints.
 - -Adding columns
 The syntax for adding a new column is similar to the syntax when creating new rows in the CREATE TABLE statement. You need to specify the data type of the column along with any potential table constraints and default values to be applied to both existing and new rows.

 ALTER TABLE mytable
ADD column DataType OptionalTableConstraint 
    DEFAULT default_value;


 - -Removing columns
 Dropping columns is as easy as specifying the column to drop, however, some databases (including SQLite) don't support this feature. Instead you may have to create a new table and migrate the data over.

 ALTER TABLE mytable
DROP column_to_be_deleted;

- -Renaming the table
If you need to rename the table itself, you can also do that using the RENAME TO clause of the statement.

ALTER TABLE mytable
RENAME TO new_table_name;

![ex](./sql exercise 17.png)

- -Dropping tables
In some rare cases, you may want to remove an entire table including all of its data and metadata, and to do so, you can use the DROP TABLE statement, which differs from the DELETE statement in that it also removes the table schema from the database entirely.

DROP TABLE IF EXISTS mytable;
![](./sql exercise 18.png)

[Back To Main](./README.md)







 
 


 