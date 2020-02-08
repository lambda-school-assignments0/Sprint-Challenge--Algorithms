#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n)
O(n) because no matter what the input is, the while loop will always run `n` times.

it can be somewhat simplified to:

```python
a = 0
while (a < n):
    a = a + 1
```


b) O(n^2)
O(n^2) because the outer loop runs `n` times and the inner loop will run `n/2` times : O(n(n/2)) -> O(n^2).


c) O(n)
O(n) because it'll run `bunnies` number of times recursively.


## Exercise II


