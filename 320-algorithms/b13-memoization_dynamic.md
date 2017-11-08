# Dynamic Programming 30/10/2017

Every node has either a lookup or 3 recursive functions

## How many recursive calls for magnitude n for coin problem

n

## How many lookups for magnitude n

2n + 1

If you follow all of the main nodes representing n, each will have 1-3 lookups
underneath it, and in the case of 2 it has a callout underneath and the case of
1 it has two lookups underneath.

There are 3n + 1 total nodes for a full 3-ary tree with n internal nodes.

> needs proof by induction

Proof: 

Consider an arbitray 3-ary full tree with n internal nodes. If n = 0,
then:  
T={r, &empty;, &empty;, &empty;}, O  
no indernal nodes &rArr; 1 leaf only &equiv; 3(o) + 1 = 1.

if a is first of 3 children, b is second and c is third, then:  
a + b + c = n - 1 (1 used as root)

by an IH that says "full 3-ary trees with j<n internals nodes have 3j+1 total
nodes"

T<sub>1</sub> has 3a + 1 nodes  
T<sub>2</sub> has 3b + 1 nodes  
T<sub>3</sub> has 3c + 1 nodes

So T has 1 + 3a + 1 + 3b + 1 + 3c +1 or  
3(a + b + c) + 4

Since a + b + c = n - 1...  
3(a + b + c) + 4 &equiv; 3(n - 1) + 4

Therefore: 3n + 1

Total work is O(n)