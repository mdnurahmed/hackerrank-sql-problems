# [Placements](https://www.hackerrank.com/challenges/placements/problem)

## Problem Description 
You are given three tables: Students, Friends and Packages. Students contains two columns: ID and Name. Friends contains two columns: ID and Friend_ID (ID of the ONLY best friend). Packages contains two columns: ID and Salary (offered salary in $ thousands per month).

Input Format

Students Table :

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | Integer                    |
| NAME                      | String                     |

Friends Table :

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | Integer                    |
| Friend_ID                 | Integer                    |

Packages Table :

| Column                    | Type                       | 
| --------------------------| ---------------------------|
| ID                        | Integer                    |
| Salary                    | Float                      |

Write a query to output the names of those students whose best friends got offered a higher salary than them. Names must be ordered by the salary amount offered to the best friends. It is guaranteed that no two students got same salary offer.

## My Approach

In this problem, We could use joins to get a table like this  where S is Student table ,
F is Friends table and P1,P2 are packages table . 

S.id | S.name | F.id=s.id |F.fid | P1.id = S.id| P1.salary| P2.id=F.fid| P2.salary 

After that we can have a where clause to get the rows according to the desired condition.

## Code (MS SQL)

```
Select S.Name
From ( Students S join Friends F Using(ID)
       join Packages P1 on S.ID=P1.ID
       join Packages P2 on F.Friend_ID=P2.ID)
Where P2.Salary > P1.Salary
Order By P2.Salary;
```