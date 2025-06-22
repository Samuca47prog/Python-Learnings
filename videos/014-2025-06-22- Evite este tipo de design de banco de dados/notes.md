# Evite este tipo de design de banco de dados

## The entity atribute value EAV design
It is super flexible.  
stores name and value of a specific attribute
![Alt text](images\entity_attr.png)

### Drawbacks
* Hard to enforce data types and constraints
* Hard to implement foreign keys
* Slow to query, as it is not normalized

Follows options to avoid the EAV design

## Option 1: A column per atribute
![Alt text](images\1.png)

Good for stable entities, where changes are not commom.

### Pros
* Easy to query data, all is in one record
* Able to enforce data types and constraints
* support indexes

### Cons
* Not flexible to attribute changes
* messy when there are a lot of attributes

## Option 2: A table per group of atributes
Known as Vertical partitioning

![Alt text](images\2.png)

### Pros
* It keeps design normalized
* Easy to query

### Cons
* Not too felxible
* Can grow complex

## Option 3: One main table with childs

![Alt text](images\3.png)

Good to use when there are multiple types of entities that shares the same parent.

### Pros
* Keeps data valid for different types of entities
* Stores less data
* Enforce data types

### Cons
* Need to perform an extra join to get all childs of the parent

## Option 4: Json attribute

![Alt text](images\4.png)

Good to use when the attributes changes a lot

### Pros
* It is super flexible and easy to update
  
### Cons
* Do not perform well as normalized tables
* poorly structured data

## Option 5: 

![Alt text](images\5.png)

### Pros
* Slightly better than EAV design
* Add indexes

### Cons
* Messy!
* Not perform well

## Summary
![Alt text](images\summary.png)