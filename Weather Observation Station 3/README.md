# [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem)

## Problem Description 
Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.
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

In this problem,

We only need the CITY attribute of the matched records from STATION table. We can use SELECT clause with FROM clause for this.To avoid duplicates we can use DISTINCT function. The condition is where ID is even number meaning if we divide the IDs with 2 , the remainder should be 0 . We can do this using WHERE clause.  

## Code (MYSQL)
```
SELECT DISTINCT(CITY) 
FROM STATION 
WHERE 
    (ID%2)=0 ;
```