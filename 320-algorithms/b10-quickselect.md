# QuickSort and QuickSelect continued 25/10/2017

QuickSelect: gives kth largest value in a set

The runtime of QuickSelect depends on choice of good pivot

**"probabilistic"** - select: 1/2 chance of good pivot every time

&rArr; O(n) expected behavior with 2 pivot choices n/4th largest cnth largest
for any c < 1...

**"deterministic"** - select: how can we promise a good pivot in the worst case?

&rArr; found mom-median of medians (blocks of size 5). Since the median of
medians is a median itself, the select function can be used (recursion).
Deterministic Select runtime:  
Runtime, plus snipped off remainder, plus time to find medians or...  
T(n) = cn + T(3n/4) + T(n/5)

c'n < 1, in this case 19/20

Now return to the code in b9!