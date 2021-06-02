# [Select All](https://www.hackerrank.com/challenges/select-all-sql/problem)

## Problem Description 
Query all columns (attributes) for every row in the CITY table.

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

We need the all the attribute of the matched records from CITY table. We can use all-column wildcard (*) with SELECT clause with FROM clause for this . There is no condition so we gotta return all the records. 

## Code (MYSQL)
```
SELECT *
FROM CITY;
```