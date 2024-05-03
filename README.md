# Advanced SQL

This activity explores more advanced SQL concepts.

These are some of the concepts covered:
- GROUP BY
- HAVING
- ORDER BY
- LIMIT
- DISTINCT
- Stored Procedures
- Functions


**Requirements**: You should have finished your previous assignment in order to do this assignment as we will be using the shop database.

## Setup

Before starting to work on this activity, make sure to install PostgreSQL first, following the instructions for your Operating System (you can leave all the default settings).

https://www.postgresql.org/download/

This will install two applications:
- `pgAdmin` to run and manage the Postgres database
- `SQL shell (psql)` to connect and interact with the database through the command line

Once the installation is done, open `SQL shell (psql)`, leaving the default values for server, database, port and username. Type the password you configured during your installation.

**Alternatively**, if you already have `psql` installed in your shell, you can connect by running:

``` bash
psql -h localhost -U postgres
```

and typing the password you configured during your installation.

## Connect to your shop database from your previous assignment

![shop](shop.png)

``` sql
\c shop;
```

## Add more data to your tables customer and location 

At least insert **10 more** records to the `customer` table, you can follow this structure:

``` sql

-- Location table INSERT queries
INSERT INTO location (city, country) VALUES ('Los Angeles', 'USA');
INSERT INTO location (city, country) VALUES ('Berlin', 'Germany');
INSERT INTO location (city, country) VALUES ('Rome', 'Italy');
INSERT INTO location (city, country) VALUES ('Seoul', 'South Korea');
INSERT INTO location (city, country) VALUES ('Toronto', 'Canada');
INSERT INTO location (city, country) VALUES ('Moscow', 'Russia');
INSERT INTO location (city, country) VALUES ('Beijing', 'China');
INSERT INTO location (city, country) VALUES ('Dubai', 'UAE');
INSERT INTO location (city, country) VALUES ('Mexico City', 'Mexico');
-- Add more INSERT queries for location table...

-- Customer table INSERT queries
INSERT INTO customer (location_id, name, surname, age) VALUES (1, 'Emma', 'Taylor', 28);
INSERT INTO customer (location_id, name, surname, age) VALUES (2, 'James', 'Anderson', 45);
INSERT INTO customer (location_id, name, surname, age) VALUES (3, 'Olivia', 'Martinez', 33);
INSERT INTO customer (location_id, name, surname, age) VALUES (4, 'William', 'Garcia', 50);
INSERT INTO customer (location_id, name, surname, age) VALUES (5, 'Sophia', 'Hernandez', 22);
INSERT INTO customer (location_id, name, surname, age) VALUES (1, 'Alexander', 'Lopez', 36);
INSERT INTO customer (location_id, name, surname, age) VALUES (2, 'Mia', 'Lee', 29);
INSERT INTO customer (location_id, name, surname, age) VALUES (3, 'Ethan', 'Walker', 41);
INSERT INTO customer (location_id, name, surname, age) VALUES (4, 'Isabella', 'Perez', 27);
INSERT INTO customer (location_id, name, surname, age) VALUES (5, 'Benjamin', 'Moore', 38);
INSERT INTO customer (location_id, name, surname, age) VALUES (6, 'John', 'Doe', 30);
INSERT INTO customer (location_id, name, surname, age) VALUES (7, 'Alice', 'Smith', 25);
INSERT INTO customer (location_id, name, surname, age) VALUES (7, 'Bob', 'Johnson', 40);
INSERT INTO customer (location_id, name, surname, age) VALUES (6, 'Emily', 'Brown', 35);
INSERT INTO customer (location_id, name, surname, age) VALUES (3, 'Michael', 'Williams', 28);
INSERT INTO customer (location_id, name, surname, age) VALUES (6, 'Charlotte', 'Gonzalez', 31);
INSERT INTO customer (location_id, name, surname, age) VALUES (7, 'Aiden', 'Rodriguez', 26);
INSERT INTO customer (location_id, name, surname, age) VALUES (8, 'Amelia', 'Smith', 34);
INSERT INTO customer (location_id, name, surname, age) VALUES (9, 'Lucas', 'Miller', 37);
INSERT INTO customer (location_id, name, surname, age) VALUES (10, 'Harper', 'Davis', 29);
INSERT INTO customer (location_id, name, surname, age) VALUES (6, 'Evelyn', 'Wilson', 43);
INSERT INTO customer (location_id, name, surname, age) VALUES (7, 'Logan', 'Jackson', 32);
INSERT INTO customer (location_id, name, surname, age) VALUES (8, 'Avery', 'White', 25);
INSERT INTO customer (location_id, name, surname, age) VALUES (9, 'Jack', 'Harris', 39);
INSERT INTO customer (location_id, name, surname, age) VALUES (10, 'Sofia', 'Martin', 28);
-- Add more INSERT queries for customer table...
```

## Answer the following questions by writing queries

1. Count the number of customers in each country who are under 30 years old.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
2. Find the average age of customers in each city.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
3. Count the number of customers whose names start with 'A'.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
4. Retrieve the names of customers who are from the same city.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
5. Retrieve the names of customers who have visited more than one location.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
6. Retrieve the names of customers who are from countries where the average age is over 50.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
7. List the countries with at least one customer aged under 20 and at least one customer aged over 60.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
8. Find the names of customers who are older than the average age of customers in their city.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
9. List the cities where the age difference between the oldest and youngest customers is more than 20 years.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
10. List the cities with customers aged over 60, ordered by the number of customers in descending order, showing only the top 3.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
11. Create a stored procedure named `get_customer_age` that takes a customer's name as input and returns their age.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
12. Develop a stored procedure named `update_customer_age` that updates the age of a customer given their ID and the new age as parameters
``` sql
-- Copy here your sql code that you ran in your psql shell

```
13. Construct a stored procedure called `delete_old_customers` that deletes customers who are older than a specified age.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
14. Write a stored procedure named `insert_new_location` that inserts a new location (city and country) into the database.
``` sql
-- Copy here your sql code that you ran in your psql shell

``` 
15. Implement a function named `get_total_customers_in_city` that returns the total number of customers in a specific city.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
16.  Develop a function called `get_customer_location` that retrieves the location (city and country) of a customer based on their id.
``` sql
-- Copy here your sql code that you ran in your psql shell

```
17. Design a function named `get_customer_count_by_country` that returns the number of customers in each country.
``` sql
-- Copy here your sql code that you ran in your psql shell

```

*Don't forget to commit and push your answers!*

## References

https://www.w3schools.com/sql/

https://www.freecodecamp.org/news/sql-having-how-to-group-and-count-with-a-having-statement/

https://learnsql.com/blog/count-group-by/

https://www.w3schools.com/sql/sql_having.asp

https://www.w3schools.com/sqL/sql_ref_sqlserver.asp

https://www.sqltutorial.org/sql-functions/

https://www.w3schools.com/SQL/sql_stored_procedures.asp

https://www.programiz.com/sql/stored-procedures

https://www.sqlservertutorial.net/sql-server-stored-procedures/
