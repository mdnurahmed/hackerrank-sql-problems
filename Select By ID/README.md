# [Select All](https://www.hackerrank.com/challenges/select-all-sql/problem)

## Problem Description 
Query all columns for a city in CITY with the ID 1661.

The CITY table is described as follows:

| Field                     | Type                       | 
| --------------------------| ---------------------------|
| ID                        | NUMBER                     |
| NAME                      | VARCHAR2(17)               |
| COUNTRYCODE               | VARCHAR2(3)                |
| DISTRICT                  | VARCHAR2(20)               |
| POPULATION                | NUMBER                     |


## My Approach

In this problem,

We need the all the attribute of the matched records from CITY table. We can use all-column wildcard (*) with SELECT clause with FROM clause for this . The condition is where ID of the records are 1661 . We can do this using WHERE clause.  

## Code 
```
SELECT *
FROM CITY
WHERE 
    ID=1661;
```