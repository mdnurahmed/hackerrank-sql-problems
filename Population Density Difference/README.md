# [Population Density Difference](https://www.hackerrank.com/challenges/population-density-difference/problem)

## Problem Description 
Query the difference between the maximum and minimum populations in CITY.

Input Format

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | NUMBER                     |
| NAME                      | VARCHAR2(17)               |
| COUNTRYCODE               | VARCHAR2(3)                |
| DISTRICT                  | VARCHAR2(20)               |
| POPULATION                | NUMBER                     |




## My Approach

In this problem, We could use the built-in replace function . 

## Code (MYSQL)
using variables
```
SET @maximum := (SELECT POPULATION FROM CITY ORDER BY POPULATION DESC LIMIT 1);
SET @minimum := (SELECT POPULATION FROM CITY ORDER BY POPULATION ASC LIMIT 1);
SET @result = (@maximum - @minimum);
SELECT @result;
```
using max function 
```
SELECT MAX(Population) - MIN(Population) AS RESULT FROM City;
```