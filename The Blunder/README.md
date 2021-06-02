# [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem)

## Problem Description 
Samantha was tasked with calculating the average monthly salaries for all employees in the EMPLOYEES table, but did not realize her keyboard's  0 key was broken until after completing the calculation. She wants your help finding the difference between her miscalculation (using salaries with any zeros removed), and the actual average salary.

Write a query calculating the amount of error (i.e.: actual - miscalculated average monthly salaries), and round it up to the next integer.

Input Format

The Employee table containing employee data for a company is described as follows:

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | Integer                    |
| NAME                      | string                     |
| SALARY                    | Integer                    |


Note: Salary is per month.

## Constraints

- 10^3 < salary < 10^5


## My Approach

In this problem, We could use the built-in replace function . 

## Code (MYSQL)
```
SELECT CEIL(AVG(Salary)-AVG(REPLACE(Salary,'0',''))) FROM EMPLOYEES;
```