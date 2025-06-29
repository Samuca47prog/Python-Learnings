# Database Normalization 1NF 2NF 3NF


## Data vs Process
A process describes what we do
Data describes who we are

Data is permanent and independent.

## Normalization

> **Normalization gives data meaning by defining its relationships with other data**

Normalization is about connecting the data in the right way.

![Alt text](images\5Ns.png)

Every Normal form is build above the previous one.

So 3NF is done after 2NF, which is done after 1NF.


## 1st Normal Form - 1NF

> **Atomic Values**
> **Unique Identifiers**

Lets normalize this table (also called Entity)

![Alt text](images\example-1nf.png)

### First Normal Form enforces the following Actions:

#### 1. A cell must never vontain more than one value
![Alt text](images\1nf-1.png)

#### 2. Each row must be unique
![Alt text](images\1nf-2.png)

#### 3. Each column name must be unique
![Alt text](images\1nf-3.png)

#### 4. There must be no repeating groups
![Alt text](images\1nf-4.png)

## 2nd Normal Form - 2NF

> **All data must be dependent on the primary key**

![Alt text](images\2nf-1.png)

If a column do not depend on the primary key, it should be moved to another table.

In the example, Skill name relates to skill Id, not to employee id.


## 3nd Normal Form - 3NF

> **The primary Key must fully define all Non-Key columns**
> **and Non-Key columns must not depend on any other key**

![Alt text](images\3nf-1.png)


## Summary
![Alt text](images\summary.png)
