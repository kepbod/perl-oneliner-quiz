### Question 1: Add column 1 and column 2 to create colmn 3.
* Input:
```
1 2
```
* Output:
```
1 2 3
```
* Answer:
```
perl -alne 'print "$_\t".($F[0]+$F[1])' question/test1 > answer/result1
```

### Question 2: Output the sum of each column.
* Input:
```
1 2 3
1 2 3
1 2 3
```
* Output:
```
3 6 9
```
