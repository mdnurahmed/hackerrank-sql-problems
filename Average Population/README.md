# [Average Population](https://www.hackerrank.com/challenges/average-population/problem)

## Problem Description 
Query the average population for all cities in CITY, rounded down to the nearest integer.

Input Format

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | NUMBER                     |
| NAME                      | VARCHAR2(17)               |
| COUNTRYCODE               | VARCHAR2(3)                |
| DISTRICT                  | VARCHAR2(20)               |
| POPULATION                | NUMBER                     |




## My Approach

In this problem, We could use ROUND() function for rounding down to nearest integer.

## Code (MYSQL)

```
SELECT ROUND(AVG(POPULATION)) FROM CITY;
```