# Dynamic Programming

We have done:

1. Greedy optimization

1. Divide and Conquer

1. Dynamic Programming optimization

## Greedy

Greedy Change

> 1988 SNL First CitiWide Bank

Assuming an unlimited supply of quarters (25 cents), dimes (10 cents), nickels
(5 cents), and pennies (1 cent, once upon a time), give a greedy algorithm to
make change for n &ge; 0 cents using the smallest total number of coins. Prove
your algorithm correct.

### Trivial and Small Examples

**Trivial:** (base case for recursion)

1. n = 0

**Small Example:**

1. n < 5 (only pennies)

1. n = 5 (1 nickel or 5 pennies)

1. n = 10 (1 dime, 2 nickels, 1 nickel and 5 pennies, or 10 pennies)

> The solution is jaggedy, as in when n = 9 it is 5 coins whereas it drops
to a possible 1 coin at 10


```python
GCC(n){
  if n==0:
    return []
  if n>=25:
    return [quarter] + GCC(n - 25)
  else if n >= 10:
}
```

n = 30 -> greedy gives 6 coins (quarter and 5 pennies)  
-> optimal gives 3 (3 dimes)

n = 31 -> greedy gives 7 coins (quarter and 6 pennies)  
-> optimal gives 4 (3 dimes one penny)
