# Graphs continued

`n = |V| = # of vertices`

`m = |E| = # of edges`

For any directed graph:

0 &le; m &le; n<sup>2</sup>, &radic;m &le; n

Undirected simple graph:

m &le; n(n-1)/2

> A comparison in runtimes is incomplete if one is O and one is &Omega;

|Runtime| |
|---|---|
|f(n) &isin; O(g(n))        |f(n) &le; g(n)|
|f(n) &isin; &Omega;(g(n))  |f(n) &ge; g(n)|
|f(n) &isin; &Theta;(g(n))  |f(n) &isin; O(g(n)) and f(n) &isin; &Omega;(g(n)) |

big-o: exactly when there is a positive real constant c and positive integer
n<sub>0</sub> such that for all integers n ≥ n<sub>0</sub>, f(n) ≤ c · g(n).

little-o: exactly when for all positive real constants c, there is a positive
integer n<sub>0</sub> such that for all integers n ≥ n<sub>0</sub>, f(n) ≤ c ·
g(n).