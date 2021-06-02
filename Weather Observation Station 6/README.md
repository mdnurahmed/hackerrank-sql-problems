# [Weather Observation Station 6](https://www.hackerrank.com/challenges/weather-observation-station-6/problem)

## Problem Description 
Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

Input Format

The STATION table is described as follows:

| Field                     | Type                       | 
| --------------------------| ---------------------------|
| ID                        | NUMBER                     |
| CITY                      | VARCHAR2(21)               |
| STATE                     | VARCHAR2(2)                |
| LAT_N                     | NUMBER                     |
| LONG_W                    | NUMBER                     |

where LAT_N is the northern latitude and LONG_W is the western longitude.

## My Approach

We can avoid duplicate cities by using SELECT with DISTINCT() function. For city names that start with vowels we can use regex expression. 

## Code (MYSQL)
```
SELECT DISTINCT(CITY)
FROM STATION 
WHERE 
    CITY REGEXP "^[aeiou].*";
```