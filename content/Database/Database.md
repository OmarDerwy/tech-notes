
# 3	Intro
we used to store data in the file system normally


problems:
- repetition
- unorganized
- hard to search

# 4	Design (ERD)
usually seniors design ERD
in small companies, maybe juniors design it but usually the oldest developer available.
ERD is very important for documenation and reference for the developer who works on it.

It's also important for defining your work before making a database that may be wrong
## 4.1	Entities
When some client wants you to make an APP for groceries

Cient:
5 warehouses
10 employees in each warehouse
import


Entities:
warehouses
emplyees
product

personal effort:
![[database - personal effort.excalidraw | 600]]

Instructor solution:

Orders entity or invoice entity


---
sometimes developers may design ERD that is missing entities but they add it later

weak entity is entity that is not related to anything but the 1 other entity i think

#iti/inquire/database about weak entities more
## 4.2	Attributes

double circles inside each other is multivalue
derivative attributes are calculated based on other variables net salary is also derived

![[database - example.excalidraw | 700]]

<iframe src="https://www.geeksforgeeks.org/types-of-attributes-in-er-model/" width="800" height="700"></iframe>


#iti/inquire/database get back in recording to the split attribute

## 4.3	Exercise

client:
online book renting 
- book
- libraries

my attempt:
![[database - practice 2.excalidraw | 700]]
entities according to instructor:
- libraries
- book
- author
- publisher
- category
- customers
- employees
- memberships
- stock
- rental

## 4.4	Relationship

not every entity should be paired with another entity
relationship example

if you're confused then do this relation
[[database - great way to know relationship.excalidraw]]
### 4.4.1	1 to 1
1 to 1 could be something like National ID to Person
### 4.4.2	1 to many
instructor and student -> if only private course then 1 to many
fines to drivers
one department to many employees
### 4.4.3	many to many
category and product -> if something like amazon some products have multi category so they are many to many

### 4.4.4	practise

booking app for hotels

we have rooms that can be rented from the user

a room has a service associated with it like room cleaning.
a person who stays at the room has a from to date
number of persons
how many rooms are available
invoices
one invoice could be multiple rooms


Entities:
- Rooms
- Customers
- Service
- Employees
- Invoices
- Roomcategory

Second Day
---
day will be like dis
- ternary binary relationshop
- normalization
- SQL
### 4.4.5	binary relationship

### 4.4.6	tertiary relationship

![[database - 3 or 4 relationship.excalidraw]]
## 4.5	Normalization
if you do correct ERD then you wouldn't need to do normalization to fix the design

# 5	SQL
## 5.1	categories
- DDL
- DML
- DQL
- DCL we will not talk about this

### 5.1.1	DDL
define database: create alter
`CREATE DATABASE `<database_name`;

`USE iti-test`

```
CREATE TABLE BOOK (
	`id` INT ,
	`name` VARCHAR(255)
)
DESCRIBE TABLE `BOOK`;
DESCRIBE `BOOK`;
```
search on SQL
- DDL
- DML
- DQL
- DCL