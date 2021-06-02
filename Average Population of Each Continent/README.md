# [Average Population of Each Continent](https://www.hackerrank.com/challenges/average-population-of-each-continent/problem)

## Problem Description 
Given the CITY and COUNTRY tables, query the names of all the continents (COUNTRY.Continent) and their respective average city populations (CITY.Population) rounded down to the nearest integer.

Note: CITY.CountryCode and COUNTRY.Code are matching key columns.

# Input Format

CITY table : 

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | NUMBER                     |
| NAME                      | VARCHAR2(17)               |
| COUNTRYCODE               | VARCHAR2(3)                |
| DISTRICT                  | VARCHAR2(20)               |
| POPULATION                | NUMBER                     |


COUNTRY table : 

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| CODE                      | VARCHAR2(3)                |
| NAME                      | VARCHAR2(44)               |
| CONTINENT                 | VARCHAR2(13)               |
| REGION                    | VARCHAR2(25)               |
| POPULATION                | NUMBER                     |
## My Approach

In this problem, We could use JOIN for this problem

## Code (MS SQL)
```
select COUNTRY.CONTINENT, floor(AVG(CITY.POPULATION))
from CITY inner join COUNTRY
on CITY.COUNTRYCODE = COUNTRY.CODE
group by COUNTRY.CONTINENT;
```
