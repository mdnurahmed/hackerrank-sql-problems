# [Revising the Select Query II](https://www.hackerrank.com/challenges/revising-the-select-query-2/problem)

## Problem Description 
Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.

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
We only need the NAME attribute of the matched records. We can do this using SELECT clause.
We need the records where COUNTRYCODE is USA, meaning the cities are American , POPULATION is greater than 120000.We can use the WHERE clause so that only records satisfying both conditions are returned.

## Code 
```
SELECT NAME
FROM CITY
WHERE 
    COUNTRYCODE = 'USA' 
    AND POPULATION > 120000;
```