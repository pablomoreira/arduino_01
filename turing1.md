# Turing code 

```
0 0 0 * 1a
0 1 1 * 1a
0 _ _ * halt

1a 0 0 * 0m0
1a 1 1 * 0m1

;;;

0m0 _ _ l 1m0
0m0 0 0 l 1m0
0m0 1 1 l 1m0

1m0 _ _ l 2m0
1m0 0 0 l 2m0
1m0 1 1 l 2m0

2m0 _ _ l 3m0
2m0 0 0 l 3m0
2m0 1 1 l 3m0

3m0 _ _ l 4m0
3m0 0 0 l 4m0
3m0 1 1 l 4m0

4m0 _ _ l 5m0
4m0 0 0 l 5m0
4m0 1 1 l 5m0

5m0 _ _ l sum0
5m0 0 0 l sum0
5m0 1 1 l sum0

;;;;

0m1 _ _ l 1m1
0m1 0 0 l 1m1
0m1 1 1 l 1m1

1m1 _ _ l 2m1
1m1 0 0 l 2m1
1m1 1 1 l 2m1

2m1 _ _ l 3m1
2m1 0 0 l 3m1
2m1 1 1 l 3m1

3m1 _ _ l 4m1
3m1 0 0 l 4m1
3m1 1 1 l 4m1

4m1 _ _ l 5m1
4m1 0 0 l 5m1
4m1 1 1 l 5m1

5m1 _ _ l sum1
5m1 0 0 l sum1
5m1 1 1 l sum1

;;;;;;;;;;;;;;;

sum0 0 0 * rev0
sum0 1 0 * rev0

sum1 0 1 * rev0
sum1 1 1 * rev0

;;;;;;;;;;;;;;;;

rev0 _ _ r rev1
rev0 0 0 r rev1
rev0 1 1 r rev1

rev1 _ _ r rev2
rev1 0 0 r rev2
rev1 1 1 r rev2

rev2 _ _ r rev3
rev2 0 0 r rev3
rev2 1 1 r rev3

rev3 _ _ r rev4
rev3 0 0 r rev4
rev3 1 1 r rev4

rev4 _ _ r 0
rev4 0 0 r 0
rev4 1 1 r 0


```