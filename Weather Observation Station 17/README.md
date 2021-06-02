# [Weather Observation Station 17](https://www.hackerrank.com/challenges/weather-observation-station-17/problem)

## Problem Description 
Query the Western Longitude (LONG_W) where the smallest Northern Latitude (LAT_N) in STATION is greater than 38.7780. Round your answer to 4 decimal places.

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

We can Round our answer using ROUND() function . We can get the records where LAT_N > 38.7780 using WHERE clause and then order the result by LAT_N in ascending fashion and get the first element only using LIMIT . 

## Code (MYSQL)
```
SELECT ROUND(LONG_W,4) FROM STATION 
WHERE 
    LAT_N > 38.7780 
ORDER BY LAT_N ASC
LIMIT 1;
```