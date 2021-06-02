# [Top Earners](https://www.hackerrank.com/challenges/earnings-of-employees/problem)

## Problem Description 
We define an employee's total earnings to be their monthly salary X months worked, and the maximum total earnings to be the maximum total earnings for any employee in the Employee table. Write a query to find the maximum total earnings for all employees as well as the total number of employees who have maximum total earnings. Then print these values as  space-separated integers.

Input Format

The Employee table containing employee data for a company is described as follows:

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| emplyee_id                | Integer                    |
| name                      | string                     |
| months                    | Integer                    |
| salary                    | Integer                    |


where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is the their monthly salary.

## My Approach

In this problem, We could use GROUP BY clause with COUNT() .

The GROUP BY statement groups rows that have the same values into summary rows . So while aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) returns total result like total sum ,total count , using aggregate function with group by returns a list where first, rows are grouped by some attribute and then aggregate functions are applied to each group .Meaning if we use aggregate functions  with GROUP BY like COUNT(attribute1) + GROUP BY attribute2 , it returns a list of items where each row is count of attribute1 that have attribute2. 

## Code (MYSQL)
```
SELECT months*salary,COUNT(months*salary) FROM Employee
GROUP BY(months*salary)
ORDER BY months*salary DESC 
LIMIT 1;
```