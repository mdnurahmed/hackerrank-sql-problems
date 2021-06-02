# [Draw The Triangle 2](https://www.hackerrank.com/challenges/draw-the-triangle-2/problem)

## Problem Description 
P(R) represents a pattern drawn by Julia in R rows. The following pattern represents P(5):
```
* 
* * 
* * * 
* * * * 
* * * * *
```
Write a query to print the pattern P(20).
## My Approach

In this problem, We could use while loop for this problem

## Code (MS SQL)
```
declare @row int = 1
while (@row <= 20)
begin
    print replicate('* ', @row)
    set @row = @row + 1
end
```
