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
* Answer:
```
perl -alne '$a+=$F[0];$b+=$F[1];$c+=$F[2];END{print "$a\t$b\t$c"}' question/test2 > answer/result2
```

### Question 3: Output the 1th and the -8th to the -2nd columns.
* Input:
```
1 2 3 4 5 6 7 8 9 10
1 2 3 4 5 6 7 8 9 10
1 2 3 4 5 6 7 8 9 10
```
* Output:
```
1 3 4 5 6 7 8 9
1 3 4 5 6 7 8 9
1 3 4 5 6 7 8 9
```
* Answer:
```
perl -alne '$"="\t";print "@F[0, -8..-2]"' question/test3 > answer/result3
```

### Question 4: Fetch rows from test4_2 with the same 1th column with test4_1.
* Input:

test4_1
```
id1
id3
```

test4_2
```
id1 3
id2 5
id3 2
id4 0
id5 1
```
* Output:
```
id1 3
id3 2
```
* Answer:
```
perl -alne 'if($#F==0){$a{$_}++}else{print if $a{$F[0]}}' question/test4_1 question/test4_2 > answer/result4
```

### Question 5: Output the odd rows.
* Input:
```
1
2
3
4
5
6
```
* Output:
```
1
3
5
```
* Answer:
```
perl -alne 'print if $.%2==1' question/test5 > answer/result5
```

### Question 6: Format every rows into specific format.
* Input:
```
38	Symbol a b	239
39	Symbol b b	389
98	Symbol c b	391
```
**Columns are separated by tab**

* Output:
```
Symbol_a_b	38	     239
Symbol_b_b	39	     389
Symbol_c_b	98	     391
```
