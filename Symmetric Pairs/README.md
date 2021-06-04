# [Symmetric Pairs](https://www.hackerrank.com/challenges/symmetric-pairs/problem)

## Problem Description 
You are given a table, Functions, containing two columns: X and Y.

Input Format

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| X                         | Integer                    |
| Y                         | Integer                    |

Two pairs (X1, Y1) and (X2, Y2) are said to be symmetric pairs if X1 = Y2 and X2 = Y1.

Write a query to output all such symmetric pairs in ascending order by the value of X. List the rows such that X1 ≤ Y1.



## My Approach

To avoid duplicates we can group by the ater ddoing inner join according to the condition.
The first condition of doing group by avoids the duplicates where f1.x = f1.y , and second condition of doing group by avoids duplicates where f1.x != f1.y . Finally to order the result we can use order by clause 

## Code (MS SQL)
```
SELECT f1.X, f1.Y FROM Functions f1
INNER JOIN Functions f2 ON f1.X=f2.Y AND f1.Y=f2.X
GROUP BY f1.X, f1.Y
HAVING COUNT(f1.X)>1 or f1.X<f1.Y
ORDER BY f1.X 
```
