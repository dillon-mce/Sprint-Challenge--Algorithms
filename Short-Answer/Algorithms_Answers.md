Add your answers to the Algorithms exercises here.

## Exercise I
### A
Answer: **O(n)**

Explanation: The while loop will run until a is greater than or equal to n^3, each time through the loop we increment a by n^2, so it will take n times through the loop to reach the end condition.

Example:
```
n = 2

// Loop 1
a = 0 + 2 * 2
a = 4 // Keep going

// Loop 2
a = 4 + 2 * 2
a = 8 = 2 * 2 * 2 // loop ends after 2 runs (or n) loops
```

### B
Answer: **O(n^3)**

Explanation: The outside (i) loop will run n times, the second (j) loop will run n-1 times, the third (k) loop will run n-2 times, and the fourth (l) loop will run 10 times. That puts the overall complexity at O(n * (n-1) * (n-2) * 10), which reduces to O(n^3).

### C
Answer: **O(n)**

Explanation: Each call to `bunnyEars()` only makes 1 recursive call. So the complexity is O(n).

Example:
```
n = 4

// Main call
bunnyEars(4)

// First recursive call
bunnyEars(3)

// Second recursive call
bunnyEars(2)

// Third recursive call
bunnyEars(1)

// Forth recursive call 
bunnyEars(0)
// returns 0 after 4 (or n) calls total
```

## Exercise II
Algorithm: Basically a binary search
- find the middle between the highest possible floor (n to start) and the lowest possible floor (0 to start)
- try dropping an egg from that floor
    - if it breaks:
        - set the highest possible floor to the one below this one 
    - else:
        - set the lowest possible floor to this one
- repeat until the highest and lowest possible floors are the same. That is the answer.

Discussion: The complexity of this will be O(log(n)), as we cut the possible answers in half with each loop. In reality though, it would probably be faster (and use less eggs) to start at the bottom floor and drop an egg at each floor until it breaks, because I can't imagine egges lasting much past the first floor. That is, you can assume f is pretty low. And if n is high, it is likely that the binary method will take longer.