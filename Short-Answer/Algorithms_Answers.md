#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n)
O(n) because no matter what the input is, the while loop will always run `n` times.

it can be somewhat simplified to:

```python
a = 0
while (a < n):
    a = a + 1
```

b) O(n*log(n))
O(n*log(n)) because the outer loop runs `n` times and the inner loop has a runtime complexity of log(n) : O(n(log(n)) -> O(n*log(n)).

c) O(n)
O(n) because it'll run `bunnies` number of times recursively.

## Exercise II

This was a somewhat weird question and I had a hard time understanding it. The way I interpreted it is that we're trying to find the value of `f` such that the number of eggs dropped and the number of eggs broken are at a minimum.

Pseudocode: (Runtime Commplexity: O(log(n)))

```python
def broken_egg_floor(n):
    curr_floor = n//2 # start @ the halfway point
    last_floor = curr_floor # stores the last floor visited; initialized @ start point
    while True: # endless loop; finding the floor `f` returns floor # and exits the loop
        if egg_drop(curr_floor) == False: # egg breaks
            curr_floor -= curr_floor//2 # move halfway down
        else: # egg survives
            if egg_drop(curr_floor + 1) == False: # if the next floor up breaks the egg, we found `f` !
                return curr_floor # found `f` !
            curr_floor += (n - curr_floor)//2 # move halfway up

```

`broken_egg_floor` takes the total number of floors `n` and finds `f` assuming there is a hidden method `egg_drop` that will return `True` if the egg survives and `False` if the egg breaks
