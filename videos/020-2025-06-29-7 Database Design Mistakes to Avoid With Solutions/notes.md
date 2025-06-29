# 7 Database Design Mistakes to Avoid (With Solutions)

## Mistake 1 - Busines field as primary key

### Examples 
Fields that should not be primary keys:
* National Company Numbers
* Part Numbers
* Item Numbers
* Social Security Numbers

### Why?
1. These values might change
2. You don't have control over the field

### Solution:
> **Create a new field just for the primary key - a Surrogate key**

![Alt text](images\1.png)

## Mistake 2 - Storing Redundant Data

### Example
Storing both date of birth and age

If age is also a column, it must be recalculated regularly to make sure it is updated.

### Solution
Calculate it in the application or in a SQL query

> **Every field that can be derrived from the columns don't need to be stored**

## Mistake 3 - Spaces or quotes in table names

> **Never add spaces to table names**


## Mistake 4 - Poor or no referential integrity

Referential Integrety: Data in your database is high-quality.

Constraints can be used to help increase data quality.

> **Use Constraints**
* Primay Key
* Foreign Key
* Unique
* Not Null
* Check


## Mistake 5 - Multiple pieces of information in a single field

**One field = one piece of information**

Split information that can be spplited, like addresses

## Mistake 6 - Storing optional types of data in different columns

Example
![Alt text](images\6.png)

Solution:
![Alt text](images\6-1.png)

Phone numbers grows vertically (adding rows) now, not horizontally (adding columns)

## Mistake 7 - Using the wrong data types and sizes

Generally, 3 types of data:
* Text
* Number
* Date

right data type selection increase:
* Quality
* Performance
* Storage

Date values allow Validation, Sorting, Filtering, which a text stored data doesn't.

